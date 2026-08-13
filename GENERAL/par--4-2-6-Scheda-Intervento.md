---
uniqueName: par-4-2-6-scheda-intervento
displayName: "par  4 2 6 Scheda Intervento"
category: "GENERAL"
tags: []
---

# par. 4.2.6 Scheda Intervento

> **File originale:** `MEV/SCHEDA_009/par. 4.2.6 Scheda Intervento.docx`  
> **Tipo:** DOCX

---

### REQ-SIE-009-06 - REQ-SIE-009-07 (Statistiche Misura Alternativa - art. 678 comma 1-ter c.p.p.)
Per i requisiti in oggetto, per i TDS/TDSM, il sistema SIUS deve prevedere due nuove tipologie di statistiche attinenti a procedimenti SIUS con contenuto ‘Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.)’, per TDS, e con contenuto ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.)’ per TDSM.
In particolare in corrispondenza del menù ‘Statistiche/Monitoraggio’ deve essere previsto un nuovo tasto funzione denominato ‘Monitoraggio Misure Alternative (art. 678 comma 1-ter c.p.p.)’ così come raffigurato  nella figura che segue:

Figura 19: Menù Statistiche TDS/TDSM
Inserita nuova funzione:
INSERT INTO FUNZIONE (ID_FUNZIONE, DESCRIZIONE, COD_TIPO_FUNZIONE, AZIONE_CONTESTO_JAVA) VALUES(38105000, 'Monitoraggio Misure Alternative (art. 678 comma 1-ter c.p.p.)', 'A', 'siap.sius.statistiche.action.ActLoadRicercaStatisticaMisureAlter678c1tercpp');
INSERT INTO FUNZIONE_PROFILO (DATA_INIZIO_VALIDITA, DATA_FINE_VALIDITA, FUN_ID_FUNZIONE, PRF_COD_PROFILO, COD_OPERATORE_INSERIMENTO, DATA_INSERIMENTO, COD_OPERATORE_AGGIORNAMENTO, DATA_AGGIORNAMENTO, FLAG_ATTIVO) VALUES(TIMESTAMP '2023-01-28 00:00:00.000000', NULL, 38105000, 14, NULL, NULL, NULL, NULL, 'S');
INSERT INTO FUNZIONE_PROFILO (DATA_INIZIO_VALIDITA, DATA_FINE_VALIDITA, FUN_ID_FUNZIONE, PRF_COD_PROFILO, COD_OPERATORE_INSERIMENTO, DATA_INSERIMENTO, COD_OPERATORE_AGGIORNAMENTO, DATA_AGGIORNAMENTO, FLAG_ATTIVO) VALUES(TIMESTAMP '2023-01-28 00:00:00.000000', NULL, 38105000, 31, NULL, NULL, NULL, NULL, 'S');
INSERT INTO FUNZIONE_PROFILO (DATA_INIZIO_VALIDITA, DATA_FINE_VALIDITA, FUN_ID_FUNZIONE, PRF_COD_PROFILO, COD_OPERATORE_INSERIMENTO, DATA_INSERIMENTO, COD_OPERATORE_AGGIORNAMENTO, DATA_AGGIORNAMENTO, FLAG_ATTIVO) VALUES(TIMESTAMP '2023-01-28 00:00:00.000000', NULL, 38105000, 41, NULL, NULL, NULL, NULL, 'S');
INSERT INTO FUNZIONE_PROFILO (DATA_INIZIO_VALIDITA, DATA_FINE_VALIDITA, FUN_ID_FUNZIONE, PRF_COD_PROFILO, COD_OPERATORE_INSERIMENTO, DATA_INSERIMENTO, COD_OPERATORE_AGGIORNAMENTO, DATA_AGGIORNAMENTO, FLAG_ATTIVO) VALUES(TIMESTAMP '2023-01-28 00:00:00.000000', NULL, 38105000, 51, NULL, NULL, NULL, NULL, 'S');
INSERT INTO RELAZIONE_FUNZIONE (FUN_ID_FUNZIONE, FUN_ID_FUNZIONE_FIGLIA, COD_TIPO_VISUALIZZAZIONE, LABEL_FUNZIONE, ORDINE_VISUALIZZAZIONE, IMMAGINE) VALUES(38100000, 38105000, 'ME', 'Monitoraggio Misure Alternative (art. 678 comma 1-ter c.p.p.)', 5, NULL);

Per la nuova funzione attingere all’attuale funzione SIUS, raggiungibile da Statistiche/Monitoraggio >> Ricerche >> Con Provvedimenti Non Validati/Depositati (Siap.Sius.Statistiche.Action.ActLoadRicercaProcPerProvviNoValidatiNoDeposito)
Con l’accesso alla funzione, il sistema mostrerà una pagina di ricerca tramite la quale l’utente potrà inserire i dati relativi all’intervallo di tempo o estremi del procedimento da verificare, e sceglie la statistica di interesse.
Le statistiche afferenti ai procedimenti di Misure Alternative (art. 678 comma 1-ter c.p.p.) saranno, limitatamente a questa prima fase, di due quattro tipologie:
Statistica Ordinanze Non Emesse – Trasmessi atti al Presidente [requisito REQ-SIE-009-06];
Statistica Ordinanze Non Emesse [requisito REQ-SIE-009-06];
Statistica Ordinanze Emesse ma prive di data di esecutività;
Statistica Ordinanze Emesse con data di esecutorietà inserita, ma privi di decisione da parte del Collegio [requisito REQ-SIE-009-07];
Nella fase successiva di sviluppo sarà prevista un’ulteriore statistica che afferisce alle Ordinanze di Revoca di Ammissione Provvisoria misura alternativa – Art. 678 comma 1 ter c.p.p.
A seguire si prospetta una pagina di esempio per la scelta della statistica di interesse:

Figura 20: Pagina di Ricerca per Statistiche - (TDS e TDSM)
A seguito dell’inserimento dei criteri di interesse, e con la sottomissione dei dati al sistema, sarà generata una pagina di elenco con i procedimenti trovati.
Dalla pagina di elenco l’utente poi avrà la possibilità di visualizzare il dettaglio di ogni singolo procedimento SIUS trovato e di esportare il risultato ottenuto in un file Excel.


Figura 21: Pagina Elenco Procedimenti per statistiche - (TDS e TDSM)
Il layout della pagina riportata, in linee generali, sarà il medesimo per tutte le tipologie di statistiche previste.
Per quanto riguarda il foglio Excel, le informazioni estratte saranno mostrate secondo il seguente formato.

Figura 22: esempio foglio Excel
Per tutte le statistiche, si fa presente, che le estrazioni faranno riferimento allo stato in cui si trova il fascicolo nel momento di elaborazione della statistica.
#### REQ-SIE-009-06 TDS/TDSM - Statistica Ordinanze Non Emesse (Restituiti Atti al Presidente)
La statistica in oggetto va a recuperare la lista dei procedimenti SIUS iscritti dai TDS con contenuto di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ e dai TDSM con contenuto ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.)’ , per i quali risulta inserita un’ordinanza di applicazione provvisoria di misura alternativa il cui esito è ‘Restituiti Atti al Presidente’.
Tali procedimenti sono individuabili dalla valorizzazione della colonna DATA_RESTITUZIONE sulla tabella GENERALE_PROCEDIMENTI  e dallo stato del procedimento che è posto a ‘Atti restituiti al Presidente’.
(STATO_FASCICOLO	23	Utilizzato in SIUS a seguito restituzione atti art. 678 c. 1-ter c.p.p.	Restituiti Atti al Presidente)
Una possibile query su cui poter lavorare:
SELECT fasc.ID_FASCICOLO_SIUS, fasc.CHIAVE_ANNO, fasc.CHIAVE_PROGR, sog.COGNOME, sog.NOME, fasc.DATA_ISCRIZIONE, GP.DATA_CAMERA_CONSIGLIO DATA_UDIENZA, GP.DATA_RESTITUZIONE, GP.DESCR_RESTITUZIONE, CODSTA.RV_MEANING STATO_FASCICOLO, CODMOV.RV_MEANING OGGETTO, FASC.COD_STATO_FASCICOLO FROM FASCICOLO_SIUS fasc, CG_REF_CODES CODMOV, CG_REF_CODES CODSTA, SOGGETTO SOG, GENERALE_PROCEDIMENTO GP WHERE fasc.CHIAVE_UFFICIO = '00127201301' AND fasc.CHIAVE_ANNO >= 2022 AND fasc.CHIAVE_ANNO <= 2023 AND fasc.CHIAVE_PROGR >= 1 AND fasc.CHIAVE_PROGR <= 500 AND GP.FAS_SIU_ID_FASCICOLO_SIUS = fasc.ID_FASCICOLO_SIUS AND GP.COD_OGGETTO_PROCEDIMENTO IN ('C050','C051') AND GP.DATA_RESTITUZIONE IS NOT NULL AND (GP.COD_OGGETTO_PROCEDIMENTO = CODMOV.RV_LOW_VALUE AND CODMOV.RV_DOMAIN = 'OGGETTO_PROCEDIMENTO') AND (FASC.COD_STATO_FASCICOLO = CODSTA.RV_LOW_VALUE AND CODSTA.RV_DOMAIN = 'STATO_FASCICOLO') AND sog.id_soggetto = fasc.sog_id_soggetto ORDER BY fasc.CHIAVE_ANNO,fasc.CHIAVE_PROGR;
#### REQ-SIE-009-06 TDS/TDSM - Statistica Ordinanze Non Emesse
Rientrano in questa categoria i procedimenti SIUS iscritti da TDS/TDSM, rispettivamente con contenuto di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ e ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.) ‘, per i quali risulta inserito il decreto di designazione magistrato, ma non sia mai stata emessa ordinanza. Infatti, il magistrato designato qualora ritenga di non poter applicare alcuna misura, non è tenuto ad emettere un’ordinanza di contenuto negativo, ma può semplicemente lasciar decorrere il tempo assegnatogli. Anche quest’ultimi, infatti, ‘ritornano’ al Presidente del Tribunale Sorveglianza.
Una possibile query su cui poter lavorare:
SELECT fasc.ID_FASCICOLO_SIUS, fasc.CHIAVE_ANNO, fasc.CHIAVE_PROGR, sog.COGNOME, sog.NOME, fasc.DATA_ISCRIZIONE, GP.DATA_CAMERA_CONSIGLIO DATA_UDIENZA, DD.DATA_TERMINE_EMISSIONE, DD.NUM_GIORNI_TERMINE_EMISSIONE, CODSTA.RV_MEANING STATO_FASCICOLO, CODMOV.RV_MEANING OGGETTO, FASC.COD_STATO_FASCICOLO FROM FASCICOLO_SIUS fasc, CG_REF_CODES CODMOV, CG_REF_CODES CODSTA, SOGGETTO SOG, GENERALE_PROCEDIMENTO GP, DEPOSITO_DECRETO DD, EVENTO EV WHERE fasc.CHIAVE_UFFICIO = '00127201301' AND fasc.CHIAVE_ANNO >= 2022 AND fasc.CHIAVE_ANNO <= 2023 AND fasc.CHIAVE_PROGR >= 1 AND fasc.COD_STATO_FASCICOLO = '22' AND fasc.CHIAVE_PROGR <= 500 AND GP.FAS_SIU_ID_FASCICOLO_SIUS = fasc.ID_FASCICOLO_SIUS AND GP.COD_OGGETTO_PROCEDIMENTO IN ('C050','C051') AND (GP.COD_OGGETTO_PROCEDIMENTO = CODMOV.RV_LOW_VALUE AND CODMOV.RV_DOMAIN = 'OGGETTO_PROCEDIMENTO') AND (FASC.COD_STATO_FASCICOLO = CODSTA.RV_LOW_VALUE AND CODSTA.RV_DOMAIN = 'STATO_FASCICOLO') AND sog.id_soggetto = fasc.sog_id_soggetto AND NOT EXISTS (SELECT 1 FROM EVENTO EV WHERE EV.FAS_SIU_ID_FASCICOLO_SIUS=fasc.ID_FASCICOLO_SIUS AND EV.COD_TIPO_PROVVEDIMENTO = '03' AND EV.COD_ESITO='0270') AND EV.FAS_SIU_ID_FASCICOLO_SIUS = fasc.ID_FASCICOLO_SIUS AND EV.COD_TIPO_PROVVEDIMENTO = '02' AND EV.COD_ESITO = '0610' AND EV.FLAG_DOCUMENTO_REGISTRATO = 'S' AND DD.ID_EVENTO_GENERATO = EV.ID_EVENTO ORDER BY fasc.CHIAVE_ANNO,fasc.CHIAVE_PROGR;
#### REQ-SIE-009-06 TDS/TDSM - Statistica Ordinanze emesse ma prive di data esecutività
Rientrano in questa categoria i procedimenti SIUS iscritti da TDS/TDSM, rispettivamente con contenuto di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ e ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.) ‘,per i quali risulta inserita un’ordinanza di applicazione provvisoria di misura alternativa il cui esito è ‘Applica provvisoriamente’ la misura ma non risulta inserita la data di esecutività.
Una possibile query su cui poter lavorare:
SELECT fasc.ID_FASCICOLO_SIUS, fasc.CHIAVE_ANNO, fasc.CHIAVE_PROGR, sog.COGNOME, sog.NOME, fasc.DATA_ISCRIZIONE, DO.DATA_CAMERA_CONSIGLIO DATA_EMISSIONE, DO.DATA_DEPOSITO, DO.DATA_ESECUTIVITA, CODSTA.RV_MEANING STATO_FASCICOLO, CODMOV.RV_MEANING OGGETTO, FASC.COD_STATO_FASCICOLO FROM FASCICOLO_SIUS fasc, CG_REF_CODES CODMOV, CG_REF_CODES CODSTA, SOGGETTO SOG, GENERALE_PROCEDIMENTO GP, DEPOSITO_ORDINANZA_PC DO, EVENTO EV WHERE fasc.CHIAVE_UFFICIO = '00127201301' AND fasc.CHIAVE_ANNO >= 2022 AND fasc.CHIAVE_ANNO <= 2023 AND fasc.CHIAVE_PROGR >= 1 AND fasc.COD_STATO_FASCICOLO = '24' AND fasc.CHIAVE_PROGR <= 500 AND GP.FAS_SIU_ID_FASCICOLO_SIUS = fasc.ID_FASCICOLO_SIUS AND GP.COD_OGGETTO_PROCEDIMENTO IN ('C050','C051') AND (GP.COD_OGGETTO_PROCEDIMENTO = CODMOV.RV_LOW_VALUE AND CODMOV.RV_DOMAIN = 'OGGETTO_PROCEDIMENTO') AND (FASC.COD_STATO_FASCICOLO = CODSTA.RV_LOW_VALUE AND CODSTA.RV_DOMAIN = 'STATO_FASCICOLO') AND sog.id_soggetto = fasc.sog_id_soggetto AND EV.FAS_SIU_ID_FASCICOLO_SIUS = fasc.ID_FASCICOLO_SIUS AND EV.COD_TIPO_PROVVEDIMENTO = '03' AND EV.COD_ESITO = '0270' AND EV.FLAG_DOCUMENTO_REGISTRATO = 'S' AND DO.ID_EVENTO_GENERATO = EV.ID_EVENTO AND DO.DATA_ESECUTIVITA IS NULL ORDER BY fasc.CHIAVE_ANNO,fasc.CHIAVE_PROGR;
#### REQ-SIE-009-07 TDS/TDSM - Statistica Ordinanze Provvisorie Esecutive senza decisione del Collegio
La statistica in oggetto va a recuperare la lista dei procedimenti SIUS iscritti dai TDS con contenuto di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ e dai TDSM con contenuto ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.)’ , per i quali risulta inserita un’ordinanza di applicazione provvisoria di misura alternativa il cui esito è ‘Applica Provvisoriamente’ e la relativa data di esecutività, ma sono privi dell’ ordinanza di ‘Conferma’ da parte del Collegio o comunque una qualsivoglia decisione da parte del Collegio.
Queste ordinanze sono individuabili, oltre che dall’esito dell’ordinanza corrispondente a ‘Applica Provvisoriamente ’, anche dalla presenza di una data di esecutività inserita in corrispondenza del record di interesse sulla tabella deposito_ordinanza_pc.
Inoltre per il procedimento SIUS da estrarre, non deve esistere un evento che lo lega ad un procedimento SIUS con esito ‘Conferma Decisione del Magistrato Relatore’.
I procedimenti di interesse per questa statistica devono essere tutti quelli per i quali è ‘mancante’ una decisione da parte del Collegio.
Per questa tipologia di statistica, sia nella pagina di elenco che nel relativo foglio Excel, in output deve essere mostrata anche la data di inizio esecutività.
Una possibile query su cui poter lavorare:
SELECT fasc.ID_FASCICOLO_SIUS, fasc.CHIAVE_ANNO, fasc.CHIAVE_PROGR, sog.COGNOME, sog.NOME, fasc.DATA_ISCRIZIONE, DO.DATA_CAMERA_CONSIGLIO DATA_EMISSIONE, DO.DATA_DEPOSITO, DO.DATA_ESECUTIVITA, CODSTA.RV_MEANING STATO_FASCICOLO, CODMOV.RV_MEANING OGGETTO, FASC.COD_STATO_FASCICOLO FROM FASCICOLO_SIUS fasc, CG_REF_CODES CODMOV, CG_REF_CODES CODSTA, SOGGETTO SOG, GENERALE_PROCEDIMENTO GP, DEPOSITO_ORDINANZA_PC DO, EVENTO EV WHERE fasc.CHIAVE_UFFICIO = '00127201301' AND fasc.CHIAVE_ANNO >= 2022 AND fasc.CHIAVE_ANNO <= 2023 AND fasc.CHIAVE_PROGR >= 1 AND fasc.COD_STATO_FASCICOLO <> '07'AND fasc.CHIAVE_PROGR <= 500 AND GP.FAS_SIU_ID_FASCICOLO_SIUS = fasc.ID_FASCICOLO_SIUS AND GP.COD_OGGETTO_PROCEDIMENTO IN ('C050','C051') AND (GP.COD_OGGETTO_PROCEDIMENTO = CODMOV.RV_LOW_VALUE AND CODMOV.RV_DOMAIN = 'OGGETTO_PROCEDIMENTO') AND (FASC.COD_STATO_FASCICOLO = CODSTA.RV_LOW_VALUE AND CODSTA.RV_DOMAIN = 'STATO_FASCICOLO') AND sog.id_soggetto = fasc.sog_id_soggetto AND EXISTS (SELECT EV.ID_EVENTO FROM EVENTO EV WHERE EV.FAS_SIU_ID_FASCICOLO_SIUS=fasc.ID_FASCICOLO_SIUS AND EV.COD_TIPO_PROVVEDIMENTO = '03' AND EV.COD_ESITO='0270' AND EV.FLAG_DOCUMENTO_REGISTRATO='S') AND EV.FAS_SIU_ID_FASCICOLO_SIUS = fasc.ID_FASCICOLO_SIUS AND EV.COD_TIPO_PROVVEDIMENTO = '03' AND EV.COD_ESITO = '0270' AND EV.FLAG_DOCUMENTO_REGISTRATO = 'S' AND DO.ID_EVENTO_GENERATO = EV.ID_EVENTO AND DO.DATA_ESECUTIVITA IS NOT NULL ORDER BY fasc.CHIAVE_ANNO,fasc.CHIAVE_PROGR;