---
uniqueName: pkg-assegna-utente-sql
displayName: "PKG_ASSEGNA_UTENTE.sql"
category: "uncategorized"
tags: ["siessvil-pl-sql-gestione-utenze"]
---

/*==============================================================================
  PKG_ASSEGNA_UTENTE - Package standalone (spec + body)
  Database SIESSVIL - Assegnazione massiva nuove utenze
  ------------------------------------------------------------------------------
  Vedi assegna_utente_siessvil.sql per lo script driver completo (query,
  spiegazione del flusso e blocco di esecuzione interattiva + export CSV/Excel).

  Tipi SQL di supporto (devono esistere PRIMA del package, sono a livello
  schema perché servono per la pipelined function usata in export):
==============================================================================*/

CREATE OR REPLACE TYPE t_riga_utente_creato AS OBJECT (
  cod_utente          VARCHAR2(30),
  cognome             VARCHAR2(60),
  nome                VARCHAR2(60),
  desc_ufficio        VARCHAR2(400),
  descrizione_profilo VARCHAR2(200)
);
/
SHOW ERRORS

CREATE OR REPLACE TYPE t_tab_riga_utente_creato AS TABLE OF t_riga_utente_creato;
/
SHOW ERRORS

CREATE OR REPLACE PACKAGE pkg_assegna_utente AS

  -- p_descrizione : comune/ufficio richiesto all'utente (es. 'MILANO')
  -- p_soggetti    : elenco soggetti nel formato 'COGNOME|NOME;COGNOME|NOME;...'
  --                 (un soggetto per ogni Cognome/Nome da profilare)
  -- Per OGNI soggetto viene creata una utenza per OGNI riga restituita dalla
  -- query di censimento (stessa query prima usata da carica_e_mostra), quindi
  -- il totale utenze create = n. soggetti x n. righe trovate per p_descrizione.
  PROCEDURE crea_utenze (p_descrizione IN VARCHAR2,
                         p_soggetti    IN VARCHAR2);

  -- Espone in formato tabellare (SQL) l'elenco delle utenze create
  -- dall'ultima esecuzione di crea_utenze, per essere interrogato con
  -- SELECT * FROM TABLE(pkg_assegna_utente.get_risultati()) ed esportato
  -- (es. via SPOOL/SET MARKUP CSV) in un file Excel/CSV.
  FUNCTION get_risultati RETURN t_tab_riga_utente_creato PIPELINED;

END pkg_assegna_utente;
/
SHOW ERRORS

CREATE OR REPLACE PACKAGE BODY pkg_assegna_utente AS

  TYPE t_riga IS RECORD (
    tipo_ufficio            cg_ref_codes.rv_low_value%TYPE,
    iniziale_cod_utente     cg_ref_codes.rv_abbreviation%TYPE,
    desc_ufficio            VARCHAR2(400),
    cod_provincia           ufficio_descr.cod_provincia%TYPE,
    cod_provincia_distretto ufficio_descr.cod_provincia%TYPE,
    cod_profilo             utente_profilo.prf_cod_profilo%TYPE,
    descrizione_profilo     profilo.descrizione%TYPE,
    cod_ufficio             ufficio.cod_ufficio%TYPE
  );

  TYPE t_soggetto IS RECORD (
    cognome VARCHAR2(60),
    nome    VARCHAR2(60)
  );

  TYPE t_tab_soggetti IS TABLE OF t_soggetto INDEX BY PLS_INTEGER;

  -- Stato di sessione: elenco delle utenze create dall'ultima crea_utenze,
  -- usato da get_risultati per l'export.
  g_risultati t_tab_riga_utente_creato := t_tab_riga_utente_creato();

  ----------------------------------------------------------------------
  -- Spezza p_soggetti ('COGNOME|NOME;COGNOME|NOME;...') in una tabella
  -- di record (cognome, nome).
  ----------------------------------------------------------------------
  FUNCTION split_soggetti (p_soggetti IN VARCHAR2) RETURN t_tab_soggetti IS
    v_tab     t_tab_soggetti;
    v_str     VARCHAR2(4000) := p_soggetti;
    v_tok     VARCHAR2(400);
    v_pos     PLS_INTEGER;
    v_sep_pos PLS_INTEGER;
    v_idx     PLS_INTEGER := 0;
  BEGIN
    WHILE v_str IS NOT NULL LOOP
      v_pos := INSTR(v_str, ';');
      IF v_pos = 0 THEN
        v_tok := v_str;
        v_str := NULL;
      ELSE
        v_tok := SUBSTR(v_str, 1, v_pos - 1);
        v_str := SUBSTR(v_str, v_pos + 1);
      END IF;

      v_tok := TRIM(v_tok);
      IF v_tok IS NOT NULL THEN
        v_sep_pos := INSTR(v_tok, '|');
        IF v_sep_pos = 0 THEN
          RAISE_APPLICATION_ERROR(-20004,
            'Formato soggetto non valido (atteso COGNOME|NOME): ' || v_tok);
        END IF;

        v_idx := v_idx + 1;
        v_tab(v_idx).cognome := TRIM(SUBSTR(v_tok, 1, v_sep_pos - 1));
        v_tab(v_idx).nome    := TRIM(SUBSTR(v_tok, v_sep_pos + 1));

        IF v_tab(v_idx).cognome IS NULL OR v_tab(v_idx).nome IS NULL THEN
          RAISE_APPLICATION_ERROR(-20004,
            'Cognome e Nome non possono essere vuoti: ' || v_tok);
        END IF;
      END IF;
    END LOOP;

    RETURN v_tab;
  END split_soggetti;

  ----------------------------------------------------------------------
  PROCEDURE crea_utenze (p_descrizione IN VARCHAR2,
                         p_soggetti    IN VARCHAR2) IS

    CURSOR c_uffici IS
      SELECT DISTINCT t.rv_low_value AS tipo_ufficio,
                      t.rv_abbreviation AS iniziale_cod_utente,
                      t.rv_meaning || ' di ' || ud.descr_comune AS desc_ufficio,
                      ud.cod_provincia AS cod_provincia,
                      ud2.cod_provincia AS cod_provincia_distretto,
                      up.prf_cod_profilo AS cod_profilo,
                      p.descrizione AS descrizione_profilo,
                      uf.cod_ufficio AS cod_ufficio
        FROM cg_ref_codes        t,
             utente_profilo      up,
             utente_ufficio      uu,
             ufficio             uf,
             profilo             p,
             ufficio_descr       ud,
             ufficio_descr       ud2,
             profilo_tipoufficio pt
       WHERE t.rv_domain LIKE 'UFFICIO_LOGIN'
         AND t.rv_meaning NOT LIKE '%Esterna%'
         AND t.rv_meaning NOT LIKE 'Direzione%'
         AND uf.cod_tipo_ufficio = t.rv_low_value
         AND uf.cod_ufficio = uu.uff_cod_ufficio
         AND p.cod_profilo = up.prf_cod_profilo
         AND p.descrizione NOT LIKE '%ESTERNA%'
         AND p.descrizione NOT LIKE '%DIREZIONE%'
         AND up.ute_cod_utente = uu.ute_cod_utente
         AND ud.cod_ufficio = uf.cod_ufficio
         AND ud2.cod_ufficio = uf.cod_distretto
            --AND p.cod_profilo <> 90
            -- SUPERUTENTE PER L' ESECUZIONE (4)
            -- SUPERUTENTE PER IL TRIBUNALE DI SORVEGLIANZA (14)
            -- SUPERUTENTE PER UFFICIO GIUDICE ESECUZIONE (16)
            -- SUPERUTENTE PER L' UFFICIO DI SORVEGLIANZA (24)
         AND p.cod_profilo IN (4, 14, 16, 24)
         AND p.cod_profilo = pt.prf_cod_profilo
         AND pt.uff_cod_tipo_ufficio = uf.cod_tipo_ufficio
         AND ud.descr_comune = UPPER(p_descrizione)
       ORDER BY 6, 2;

    v_soggetti  t_tab_soggetti;
    v_random5   NUMBER;
    v_parametro VARCHAR2(30);
    v_schema    VARCHAR2(60);
    v_cod_oper  VARCHAR2(30);
    v_sql       VARCHAR2(4000);
    v_oggi      DATE := TRUNC(SYSDATE);
    v_tot       PLS_INTEGER := 0;
    v_righe     PLS_INTEGER := 0;
  BEGIN
    g_risultati := t_tab_riga_utente_creato();

    v_soggetti := split_soggetti(p_soggetti);
    IF v_soggetti.COUNT = 0 THEN
      RAISE_APPLICATION_ERROR(-20005, 'Nessun soggetto fornito.');
    END IF;

    FOR s IN 1 .. v_soggetti.COUNT LOOP
      v_righe := 0;

      FOR r IN c_uffici LOOP
        v_righe   := v_righe + 1;
        v_random5 := TRUNC(DBMS_RANDOM.VALUE(10000, 100000));
        v_parametro := r.iniziale_cod_utente || v_random5;

        v_schema   := 'SIES' || r.cod_provincia_distretto;
        v_cod_oper := 'ADMIN' || r.cod_provincia_distretto || 'E';

        -- 1) UTENTE
        v_sql := 'INSERT INTO ' || v_schema || '.UTENTE ' ||
                 '(COD_UTENTE, COGNOME, NOME, COD_OPERATORE_INSERIMENTO, DATA_INSERIMENTO) ' ||
                 'VALUES (:1, :2, :3, :4, :5)';
        EXECUTE IMMEDIATE v_sql
          USING v_parametro, v_soggetti(s).cognome, v_soggetti(s).nome, v_cod_oper, v_oggi;

        -- 2) UTENTE_PROFILO
        v_sql := 'INSERT INTO ' || v_schema || '.UTENTE_PROFILO ' ||
                 '(DATA_INIZIO_VALIDITA, UTE_COD_UTENTE, PRF_COD_PROFILO, COD_OPERATORE_INSERIMENTO, DATA_INSERIMENTO) ' ||
                 'VALUES (:1, :2, :3, :4, :5)';
        EXECUTE IMMEDIATE v_sql
          USING v_oggi, v_parametro, r.cod_profilo, v_cod_oper, v_oggi;

        -- 3) UTENTE_UFFICIO
        v_sql := 'INSERT INTO ' || v_schema || '.UTENTE_UFFICIO ' ||
                 '(DATA_INIZIO_VALIDITA, UTE_COD_UTENTE, UFF_COD_UFFICIO, COD_UTENTE_INSERIMENTO, DATA_INSERIMENTO) ' ||
                 'VALUES (:1, :2, :3, :4, :5)';
        EXECUTE IMMEDIATE v_sql
          USING v_oggi, v_parametro, r.cod_ufficio, v_cod_oper, v_oggi;

        v_tot := v_tot + 1;
        g_risultati.EXTEND;
        g_risultati(v_tot) := t_riga_utente_creato(
                                v_parametro,
                                v_soggetti(s).cognome,
                                v_soggetti(s).nome,
                                r.desc_ufficio,
                                r.descrizione_profilo);
      END LOOP;

      IF v_righe = 0 THEN
        RAISE_APPLICATION_ERROR(-20006,
          'Nessuna riga trovata per la descrizione: ' || p_descrizione);
      END IF;
    END LOOP;

    COMMIT;

    DBMS_OUTPUT.PUT_LINE('Creati ' || v_tot || ' utenze: ' || v_soggetti.COUNT ||
                          ' soggetti x ' || v_righe || ' profili/uffici per "' ||
                          UPPER(p_descrizione) || '".');
  EXCEPTION
    WHEN OTHERS THEN
      ROLLBACK;
      DBMS_OUTPUT.PUT_LINE('Errore durante la creazione utenze: ' || SQLERRM);
      RAISE;
  END crea_utenze;

  ----------------------------------------------------------------------
  FUNCTION get_risultati RETURN t_tab_riga_utente_creato PIPELINED IS
  BEGIN
    FOR i IN 1 .. g_risultati.COUNT LOOP
      PIPE ROW (g_risultati(i));
    END LOOP;
    RETURN;
  END get_risultati;

END pkg_assegna_utente;
/
SHOW ERRORS
