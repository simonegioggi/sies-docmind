---
uniqueName: procedura-assegnazione-utente-siessvil
displayName: "Procedura Assegnazione Utente SIESSVIL"
category: "uncategorized"
tags: ["siessvil-pl-sql-gestione-utenze"]
---

# Procedura Oracle PL/SQL – Assegnazione Nuovo Utente

Database SIESSVIL

## 1. Obiettivo

Fornire uno script/procedura Oracle PL/SQL per il database “siessvil” che, dato un valore richiesto all’utente per individuare l’ufficio/comune (es. MILANO) e un elenco di soggetti (Cognome/Nome, es. Palazzi Paolo, Albibocchi Maurizio, Marchi Luca), permetta di:

- interrogare l’elenco delle combinazioni ufficio/profilo/utente disponibili per il valore richiesto, tramite la query di censimento (la stessa già usata in precedenza da carica_e_mostra);
- creare, per OGNI soggetto della lista, UNA utenza per OGNI riga restituita dalla query (nell’esempio con MILANO la query restituisce 16 righe profilo/ufficio, quindi per 3 soggetti si creano 16 x 3 = 48 utenze);
- per ciascuna utenza generare un nuovo codice utente concatenando INIZIALE_COD_UTENTE a 5 cifre numeriche casuali, e prendere COD_PROFILO e COD_UFFICIO direttamente dalla riga della query;
- eseguire le 3 INSERT (UTENTE, UTENTE_PROFILO, UTENTE_UFFICIO) nello schema dinamico corretto (‘SIES’ || COD_PROVINCIA_DISTRETTO) per ciascuna utenza creata;
- salvare tutte le utenze create in un file Excel (CSV), con le colonne: cod_utente, cognome, nome, desc_ufficio, descrizione_profilo, esportato tramite SPOOL sulla macchina che esegue lo script (il proprio PC se lanciato in locale; il server remoto se lanciato via SSH/RDP, da trasferire poi manualmente sul proprio Desktop).
Cambio di strategia rispetto alla versione precedente: non è più previsto un passaggio manuale di visualizzazione a video e selezione di una singola riga (la procedura carica_e_mostra non ha più senso ed è stata rimossa); tutte le righe restituite dalla query vengono utilizzate automaticamente, per ciascun soggetto della lista in input.

## 2. Query di censimento (input)

Query di censimento (invariata nella logica), ora filtrata sul valore richiesto all’utente (ud.descr_comune = UPPER(p_descrizione)) e utilizzata per TUTTE le righe restituite (non più solo per la visualizzazione/selezione manuale). La colonna uf.cod_ufficio, presente ma commentata nella versione originale, resta riattivata perché necessaria per il salvataggio.

```sql
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
   AND p.cod_profilo IN (4, 14, 16, 24)
   AND p.cod_profilo = pt.prf_cod_profilo
   AND pt.uff_cod_tipo_ufficio = uf.cod_tipo_ufficio
   AND ud.descr_comune = UPPER(p_descrizione)
 ORDER BY 6, 2
```

## 3. Logica della soluzione

La soluzione è realizzata come package PL/SQL (PKG_ASSEGNA_UTENTE) invocato da uno script driver SQL*Plus/SQLcl, poiché è necessaria l’interazione con l’utente (valore ricerca ufficio/comune, elenco soggetti, percorso file di export) e l’export lato client su file.

1. crea_utenze(p_descrizione, p_soggetti): esegue la query di censimento filtrata su p_descrizione; per ogni soggetto della lista p_soggetti (formato COGNOME|NOME;COGNOME|NOME;...) e per ogni riga trovata, genera <PARAMETRO> = INIZIALE_COD_UTENTE || TRUNC(DBMS_RANDOM.VALUE(10000,100000)), costruisce dinamicamente lo schema target ‘SIES’ || COD_PROVINCIA_DISTRETTO ed esegue le 3 INSERT (UTENTE, UTENTE_PROFILO, UTENTE_UFFICIO); accumula ogni utenza creata (cod_utente, cognome, nome, desc_ufficio, descrizione_profilo) in una collezione di package per il successivo export.
1. split_soggetti(p_soggetti): funzione privata che spezza la stringa in input (delimitata da ‘;’ tra soggetti e ‘|’ tra cognome e nome) in una tabella PL/SQL di record (cognome, nome); solleva errore se il formato non è quello atteso.
1. get_risultati: pipelined function che restituisce, come collezione SQL interrogabile con SELECT * FROM TABLE(...), l’elenco delle utenze create dall’ultima esecuzione di crea_utenze; è il punto di aggancio usato dallo script driver per l’export su file Excel/CSV.
### 3.1 Note e correzioni rispetto al testo originale

- Il nome schema/tabella non è bindabile in SQL dinamico: viene costruito come testo e concatenato nella stringa SQL, mentre i valori (Cognome, Nome, date, codici) restano sempre bind variable (USING) per evitare SQL injection.
- L’espressione originale TO_DATE(sysdate, ‘DD/MM/YYYY’) è ridondante (sysdate è già una DATE): sostituita con TRUNC(SYSDATE).
- COD_UFFICIO, non selezionato nella query originale (era commentato), è stato riattivato perché richiesto esplicitamente per il salvataggio.
- La procedura carica_e_mostra e la procedura seleziona(indice) sono state rimosse: con la nuova strategia bulk, la visualizzazione/selezione manuale di una singola riga non ha più senso, poiché vengono utilizzate automaticamente tutte le righe trovate, per ciascun soggetto in input.
- Introdotti i tipi SQL t_riga_utente_creato (oggetto) e t_tab_riga_utente_creato (collezione), necessari per esporre l’elenco delle utenze create tramite la pipelined function get_risultati, interrogabile con una normale SELECT.
- Le INSERT per ogni singola utenza restano racchiuse in un’unica transazione complessiva con COMMIT finale e ROLLBACK automatico in caso di errore (gestione eccezioni con RAISE per propagare l’errore).
- L’export su Excel/CSV è realizzato lato client con SPOOL (SQL*Plus/SQLcl), non con UTL_FILE: UTL_FILE scriverebbe sul filesystem del server database. SPOOL scrive invece sul filesystem della macchina su cui gira il processo SQL*Plus/SQLcl: se tale processo gira in locale il file compare sul proprio Desktop, se invece SQL*Plus/SQLcl viene lanciato su un server remoto (SSH/RDP) il file resta su quel server e va poi trasferito manualmente (scp/sftp/WinSCP o funzione di trasferimento file del client RDP) sul proprio Desktop.
## 4. Utilizzo

Connettersi al database siessvil con SQL*Plus o SQLcl ed eseguire lo script assegna_utente_siessvil.sql (che crea/compila anche i tipi SQL di supporto e il package PKG_ASSEGNA_UTENTE). Lo script:

- chiede il valore di ricerca ufficio/comune (es. MILANO);
- chiede l’elenco dei soggetti nel formato COGNOME|NOME;COGNOME|NOME;... (es. PALAZZI|PAOLO;ALBIBOCCHI|MAURIZIO;MARCHI|LUCA per Palazzi Paolo, Albibocchi Maurizio, Marchi Luca);
- crea automaticamente una utenza per ogni soggetto x ogni riga trovata dalla query (es. 3 soggetti x 16 righe = 48 utenze) ed esegue le relative INSERT, confermando a video il totale di utenze create;
- chiede il percorso completo del file di export VALIDO SULLA MACCHINA CHE ESEGUE LO SCRIPT (es. /tmp/utenze_create.csv su un server Linux remoto, oppure C:\Users\<utente>\Desktop\utenze_create.csv se lo script gira in locale) e salva l’elenco di tutte le utenze create in formato CSV apribile con Excel, con le colonne cod_utente, cognome, nome, desc_ufficio, descrizione_profilo; se lo script gira su un server remoto, il file va poi trasferito manualmente (scp/sftp/RDP) sul proprio Desktop prima di aprirlo.
In alternativa, il package PKG_ASSEGNA_UTENTE.sql può essere compilato una sola volta e richiamato manualmente in sessioni successive con le chiamate:

```sql
EXEC pkg_assegna_utente.crea_utenze('MILANO', 'PALAZZI|PAOLO;ALBIBOCCHI|MAURIZIO;MARCHI|LUCA');
SET MARKUP CSV ON QUOTE OFF
SPOOL /tmp/utenze_create.csv  -- oppure C:\Users\<utente>\Desktop\utenze_create.csv se in locale
SELECT * FROM TABLE(pkg_assegna_utente.get_risultati());
SPOOL OFF
SET MARKUP CSV OFF
```

## 5. Package PL/SQL: PKG_ASSEGNA_UTENTE

File: PKG_ASSEGNA_UTENTE.sql

```sql
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
```

## 6. Script driver completo

File: assegna_utente_siessvil.sql (crea i tipi SQL di supporto, il package e avvia il flusso interattivo completo di creazione massiva ed export)

```sql
/*==============================================================================
  ASSEGNAZIONE MASSIVA NUOVE UTENZE - Database SIESSVIL
  ------------------------------------------------------------------------------
  Flusso (nuova strategia):
    1) Viene chiesto all'utente il valore di ricerca ufficio/comune
       (es. MILANO): è lo stesso filtro prima usato da carica_e_mostra.
    2) Viene chiesto un elenco di soggetti (Cognome/Nome) da profilare,
       nel formato COGNOME|NOME;COGNOME|NOME;... (es. per Palazzi Paolo,
       Albibocchi Maurizio, Marchi Luca:
       'PALAZZI|PAOLO;ALBIBOCCHI|MAURIZIO;MARCHI|LUCA').
    3) Per OGNI soggetto viene creata una utenza per OGNI riga restituita
       dalla query di censimento filtrata sul valore al punto 1 (in un caso
       tipico, es. MILANO, la query restituisce 16 righe profilo/ufficio:
       con 3 soggetti si ottengono quindi 3 x 16 = 48 utenze). Per ciascuna
       riga vengono presi INIZIALE_COD_UTENTE, COD_PROFILO e COD_UFFICIO.
    4) Per ogni utenza viene generato <PARAMETRO> = INIZIALE_COD_UTENTE ||
       5 cifre random (TRUNC(DBMS_RANDOM.VALUE(10000,100000))) ed eseguite
       le 3 INSERT nello schema dinamico 'SIES'||COD_PROVINCIA_DISTRETTO
       (Utente, Utente_Profilo, Utente_Ufficio).
    5) Tutte le utenze create vengono esportate in un file Excel/CSV sul
       Desktop della macchina da cui viene lanciata la procedura, con le
       colonne: cod_utente, cognome, nome, desc_ufficio, descrizione_profilo.

  NOTE:
   - La procedura "carica_e_mostra" (visualizzazione manuale a video con
     selezione di UNA riga) non ha più senso con la nuova strategia bulk e
     NON è più presente: le informazioni (INIZIALE_COD_UTENTE, COD_PROFILO,
     COD_UFFICIO) sono lette direttamente, per tutte le righe, dalla stessa
     query prima usata da carica_e_mostra.
   - Il nome schema/tabella non è bindabile: viene costruito come testo e
     eseguito con EXECUTE IMMEDIATE (i VALORI restano sempre bindati con
     USING per evitare SQL injection su Cognome/Nome).
   - Nella query originale "uf.cod_ufficio" era commentato: qui è stato
     riattivato perché richiesto per il salvataggio.
   - "TO_DATE(sysdate, 'DD/MM/YYYY')" del testo originale è ridondante
     (sysdate è già una DATE): sostituito con TRUNC(SYSDATE).
   - L'export Excel/CSV viene realizzato con SPOOL lato client (SQL*Plus/
     SQLcl): il file viene scritto sul filesystem della macchina da cui
     gira il processo SQL*Plus/SQLcl (non sul server database). Se tale
     processo gira in locale, il file compare davvero sul proprio Desktop;
     se invece SQL*Plus/SQLcl viene lanciato su un SERVER REMOTO (SSH/RDP),
     il file resta su quel server ed è necessario trasferirlo manualmente
     sul proprio Desktop (scp/sftp/WinSCP o funzione di trasferimento file
     del client RDP) dopo l'esecuzione dello script. "SET MARKUP CSV ON"
     produce comunque un file .csv standard apribile direttamente con Excel.
   - Eseguire con SQL*Plus (o SQLcl) perché usa ACCEPT per l'input utente
     e lo stato del package persiste per tutta la sessione.
==============================================================================*/

SET SERVEROUTPUT ON SIZE UNLIMITED
SET FEEDBACK OFF
SET VERIFY OFF

/*------------------------------------------------------------------------
  0) TIPI SQL DI SUPPORTO (per l'export tabellare via TABLE())
------------------------------------------------------------------------*/
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

/*------------------------------------------------------------------------
  1) PACKAGE SPEC
------------------------------------------------------------------------*/
CREATE OR REPLACE PACKAGE pkg_assegna_utente AS

  -- p_descrizione : comune/ufficio richiesto all'utente (es. 'MILANO')
  -- p_soggetti    : elenco soggetti nel formato 'COGNOME|NOME;COGNOME|NOME;...'
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

/*------------------------------------------------------------------------
  2) PACKAGE BODY
------------------------------------------------------------------------*/
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

/*------------------------------------------------------------------------
  3) DRIVER INTERATTIVO (SQL*Plus / SQLcl)
------------------------------------------------------------------------*/
ACCEPT v_descrizione CHAR PROMPT 'Su quale Ufficio/Comune vuoi profilare le UTENZE? (es: MILANO): '
ACCEPT v_soggetti    CHAR PROMPT 'Elenco soggetti Cognome/Nome, formato COGNOME|NOME;COGNOME|NOME;... : '

EXEC pkg_assegna_utente.crea_utenze('&v_descrizione', '&v_soggetti');

/*------------------------------------------------------------------------
  IMPORTANTE - Dove viene scritto il file di export
  ------------------------------------------------------------------------
  SPOOL scrive SEMPRE sul filesystem della macchina su cui gira il processo
  SQL*Plus/SQLcl che esegue questo script, NON necessariamente sul PC/Desktop
  dell'utente:
    - se SQL*Plus/SQLcl gira in locale sul proprio PC Windows, un percorso
      tipo C:\Users\<utente>\Desktop\utenze_create.csv finisce davvero sul
      Desktop locale;
    - se invece ci si collega e si lancia SQL*Plus/SQLcl su un SERVER
      REMOTO (es. via SSH/PuTTY o sessione RDP/Citrix), il file viene creato
      sul disco di QUEL server, in un percorso valido per il SUO sistema
      operativo (es. /tmp/utenze_create.csv su server Linux). In questo caso,
      per portare il file sul proprio Desktop occorre un passaggio aggiuntivo
      di trasferimento DOPO l'esecuzione dello script, ad es.:
        * SSH/terminale: da un'altra shell sul proprio PC,
          scp utente@server:/tmp/utenze_create.csv C:\Users\<utente>\Desktop\
          (o sftp/WinSCP/FileZilla con le stesse credenziali);
        * Desktop remoto (RDP/Citrix): usare la cartella condivisa/redirect
          del client oppure la funzione "trasferisci file" del client RDP.
  Indicare quindi un percorso di export VALIDO SUL SISTEMA OPERATIVO DELLA
  MACCHINA CHE ESEGUE QUESTO SCRIPT (server remoto incluso).
------------------------------------------------------------------------*/
ACCEPT v_percorso_export CHAR PROMPT 'Percorso completo file export SULLA MACCHINA CHE ESEGUE LO SCRIPT (es: /tmp/utenze_create.csv oppure C:\Users\<utente>\Desktop\utenze_create.csv se locale): '

SET MARKUP CSV ON QUOTE OFF
SPOOL &v_percorso_export
SELECT cod_utente, cognome, nome, desc_ufficio, descrizione_profilo
  FROM TABLE(pkg_assegna_utente.get_risultati());
SPOOL OFF
SET MARKUP CSV OFF

PROMPT File esportato su questa macchina in: &v_percorso_export
PROMPT Se questo script gira su un server remoto, trasferire ora il file sul proprio Desktop (scp/sftp/RDP) prima di aprirlo con Excel.
```