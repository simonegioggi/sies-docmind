---
uniqueName: siut-sies-ct-1-0-20191206-allegato-al-piano-test
displayName: "SIUT SIES CT 1 0 20191206 Allegato al piano test"
category: "GENERAL"
tags: []
---

# SIUT-SIES-CT-1.0-20191206-Allegato-al-piano-test

> **File originale:** `RILASCIO_11.2.3/SIUT-SIES-CT-1.0-20191206-Allegato-al-piano-test.xls`  
> **Tipo:** XLS

---

## Raw_Data_In

| DisplayID | IsFTR | Level1 | Level2 | Level3 | Level4 | Level5 | Level6 | Level7 | Level8 | Level9 | Level10 | Level11 | Level12 | Assigned_To | Description | Status | Time_Est | Prior Internal Testing | Prior External Testing | Impact to Release | Maturity of Function | Complexity of Function | Usage Frequency | Defect Impact | External Testing Effort | Custom Factor 1 | Custom Factor 2 | Custom Factor 3 | FTR Risk | TR Risk | Total_System_Risk | Total_Intgr_Risk | System_Index | Intgr_Index | Cyc1 | Cyc2 | Cyc3 | Cyc4 | Cyc5 | Cyc6 | Cyc7 | Cyc8 | Cyc9 | Cyc10 | Cyc11 | Cyc12 | Cyc13 | Cyc14 | Cyc15 | Cyc16 | Cyc17 | Cyc18 | Cyc19 | Cyc20 | Project_ID | Folder_ID | Req_ID | Desc1 | Desc2 | Desc3 | Desc4 | Desc5 | Desc6 | Desc7 | Desc8 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Descr.fogli lavoro

|  | Descrizione dei fogli di lavoro per la compilazione dell' "Allegato 1 - Tabella dei test" e  dell' "Allegato 2 - Specifiche di test" al Piano di test |
| --- | --- |
| Questo documento Excel contiene i template da utilizzare per la stesura dell' "Allegato 1 - Tabella dei test" e  dell' "Allegato 2 - Specifiche di test" nell'ambito della progettazione dei test in progetti / obiettivi di sviluppo e/o manutenzione software. |  |
| Di seguito si riportano le descrizioni dei vari fogli di lavoro. |  |
| Per ulteriori istruzioni di compilazione della Tabella di test e delle Specifiche di test, si rimanda ai relativi paragrafi del Piano di test. |  |
| Foglio di lavoro | Descrizione |
| Descr.fogli lavoro (**) | Descrizione dei fogli di lavoro per la compilazione dell' "Allegato 1 - Tabella dei test" e  dell' "Allegato 2 - Specifiche di test" al Piano di test |
| Cop.All.1Tab.test | Copertina dell' "Allegato 1 - Tabella dei test", con le informazioni di riferimento al Piano di test. |
| All.1Tab.test | "Allegato 1 - Tabella dei test" al Piano di test, contiene le informazioni dei requisiti e funzionalità ed i casi di test ad essi collegati. Contiene inoltre informazioni aggiuntive per la progettazione dei test, quali i livelli di rischio, i cicli di test ecc. |
| Es.1 (**) | Esempio di Tabella di test compilata. |
| Cop.All.2Spec.test | Copertina dell' "Allegato 2 - Specifiche di test", con le informazioni di riferimento al Piano di test. |
| All.2Spec.test | "Allegato 2 - Specifiche di test" al Piano di test, contiene gli script di test sviluppati per ogni singolo caso di test presente nella Tabella dei test. |
| Es.2 (**) | Esempio di Specifiche di test, con uno script di test compilato e gli altri predisposti (solo intestazione) come dalla tabella dei test (esempio 1) |
| (*) :  Ci si avvarrà di questi fogli di lavoro solo nel caso di utilizzo di macro |  |
| (**) : Fogli di lavoro da eliminare nel deliverable |  |

## Descr.macro

|  | Descrizione delle macro |
| --- | --- |
| Macro da menu |  |
| Get info from 
(Specifiche di test) | Questa macro ricerca all'interno delle 'specifiche di test' il numero di condizioni di test, la versione e la stima durata presenti per ogni script di test inserito e riporta tale valore sul corrispettivo caso di test nella tabella dei test. In caso di più script di test per lo stesso caso di test, sono riportati i corrispettivi totali (stima durata e n. cond. di test). |
| Sort (Tabella dei test) | Effettua un sort della tabella dei test, basato sui livelli di scomposizione. |
| Reset (Tabella dei test) | Elimina tutte le entrate presenti nella tabella dei test e ripropone l'impostazione iniziale. |
| Reset (Specifiche di test) | Elimina tutte le entrate presenti nella specifica dei test e ripropone l'impostazione iniziale. |
| Macro da tasti |  |
| Insert (CTRL-I) | Inserisce una riga vuota. |
| Delete (CTRL-E) | Elimina la riga corrente. |
| Duplicate (CTRL-D) | Duplica la riga corrente mantenendo tutti i valori presenti. |
| Insert Layout (CTRL-A) | Inserisce il layout dello script di test, come presente nel foglio di lavoro 'layout' nei range definiti in  'Macro Settings'. Utilizzando questa macro si assicura il mantenimento dello standard previsto e la rapidita nella stesura delle informazioni. Modificando i paramentri della macro in 'Macro Settings' e il layout in 'Layout' è possibile utilizzare diversi layout predisposti per specifiche necessità, sempre mantenendo la struttura originale pervista dallo standard. Una volta inserito il layout i campi 'Nome Script di test', 'Descrizione', 'Versione', 'Stima Durata' e 'N. cond. di test' cambiano il colore di sfondo in giallo, per dare evidenza dell'inserimento avvenuto. |

## Copertina

|  |  |
| --- | --- |
|  | Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A - Sirfin-PA nell’ambito del contratto CIG 73479643B7 per lo “SVILUPPO DEL SISTEMA INFORMATIVO UNITARIO TELEMATICO, LA MANUTENZIONE DEGLI ATTUALI SISTEMI DELL’AREA PENALE DEL MINISTERO DELLA GIUSTIZIA E SERVIZI CORRELATI LOTTO 1” |
|  | SIUT-SIES-CT-1.0-20191206-Allegato-al-piano-test.xls |
|  | Piano di test |
|  | Ver. 1.0 |
|  | Data: 06/12/2019 |
|  | SIUT |
|  | SIES 11.2.3 |
|  | Allegato al Piano dei Test |

## TabellaTest

| Codice Area |  |  | SIUT |  |  |  | Codifica  Piano di test |  | SIUT-SIES-CT-1.0-20191206-Allegato-al-piano-test.xls | Versione | Ver. 1.0 |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Applicazione |  |  | Funzionalità / Requisiti non funzionali |  |  |  |  |  |  | Caso di test |  |  |  |  |  |  |  |  |  |  |
| Codice Area | Codice Appl. | ID. Requisito | ID | Primo livello | ID | Primo Livello | Risk (1-5) | ID | Secondo livello | ID | Nome del caso di test | Classe di Gravità (1-4) | Ciclo di test | Stima Durata | Descrizione e note | Versione | N. cond. di test | Autom. | Classe di rilevanza (A, B, C) | Esito |
| SIUT | SIES | 20191108014 |  |  | 20191108014.0 | Problema cancellazione note dopo scarico ordinanza di rinvio udienza |  | SIUS | SIUS - Problema cancellazione note dopo scarico ordinanza di rinvio udienza | TF001.SIUS | Verifica: verificare che il campo note sulla maschera di dettaglio del procedimento rimanga valorizzato, se presente, a seguito di emissione di ordinanza di rinvio udienza |  |  |  | Verifica: verificare che il campo note sulla maschera di dettaglio del procedimento rimanga valorizzato, se presente, a seguito di emissione di ordinanza di rinvio udienza | 1.0 |  |  |  |  |
| SIUT | SIES | 20191115013 |  |  | 20191115013.0 | La pagina iniziale del fascicolo non visualizza le date di rinvio delle udienze |  | SIGE | SIGE - La pagina iniziale del fascicolo non visualizza le date di rinvio delle udienze | TF002.SIGE | Verifica: verificare che la data udienza deve essere visibile anche per tipo provvedimento 'Rinvio udienza da verbale' |  |  |  | Verifica: verificare che la data udienza deve essere visibile anche per tipo provvedimento 'Rinvio udienza da verbale' | 1.0 |  |  |  |  |
| SIUT | SIES | 20191112011 |  |  | 20191112011.0 | Emissione liberazione anticipata per detenuto agli arresti domiciliari |  | SIEP | SIEP – Emissione liberazione anticipata per detenuto agli arresti domiciliari | TF003.SIEP | Verifica: verificare che per la posizione giuridica 'Arresti Domiciliare ex art 89 dpr 309/90 - ex art. 656 comma 10 cpp' venga caricata la pagina mostrando la sezione dei destinatari, come previsto per la posizione giuridica 'Arresti domiciliari ex art.656/10' |  |  |  | Verifica: verificare che per la posizione giuridica 'Arresti Domiciliare ex art 89 dpr 309/90 - ex art. 656 comma 10 cpp' venga caricata la pagina mostrando la sezione dei destinatari, come previsto per la la posizione giuridica 'Arresti domiciliari ex art.656/10' | 1.0 |  |  |  |  |
| SIUT | SIES | 20191108016 |  |  | 20191108016 | Soggetto presentante |  | SIGE | Soggetto presentante | TF004.SIGE | Verifica: verificare dalla pagina di dettaglio di un ricorso SIGE che il soggetto presentante corrisponda a quello inserito dall'utente in fase di emissione del ricorso stesso |  |  |  | Verifica: verificare dalla pagina di dettaglio di un ricorso SIGE che il soggetto presentante corrisponda a quello inserito dall'utente in fase di emissione del ricorso stesso | 1.0 |  |  |  |  |
| SIUT | SIES | 201911140122.0 |  |  | 201911140122.0 | Errore bloccante nella generazione della stampa del provvedimento
relativo al "Dettaglio Detenzione Domicilare a Termine" |  | SIEP | Errore bloccante nella generazione della stampa del provvedimento
relativo al "Dettaglio Detenzione Domicilare a Termine" | TF005.SIEP | Verifica: verificare la correttezza della stampa per il provvedimento di "Dettaglio Detenzione Domicilare a Termine" |  |  |  | Verifica: verificare la correttezza della stampa per il provvedimento di "Dettaglio Detenzione Domicilare a Termine" | 1.0 |  |  |  |  |
| SIUT | SIES | 20191128014 |  |  | 20191128014 | Non fornisce lo scadenziario per DS notificato con Decreto Irreperibilita |  | SIEP | Non fornisce lo scadenziario per DS notificato con Decreto Irreperibilita | TF006.SIEP | Verifica: verificare che nello scadenzario dei Decreti di Sospensione siano presenti i procedimenti con Decreto Irreperibilita |  |  |  | Verifica: verificare che nello scadenzario dei Decreti di Sospensione siano presenti i procedimenti con Decreto Irreperibilita | 1.0 |  |  |  |  |
| SIUT | SIES | 20191106018.0 |  |  | 20191106018 | DECRETI IRREPERIBILITA' LEGGE SIMEONE |  | SIEP | DECRETI IRREPERIBILITA' LEGGE SIMEONE | TF007.SIEP | Verifica: verificare che nello scadenzario dei Decreti di Sospensione siano presenti i procedimenti con Decreto Irreperibilita |  |  |  | Verifica: verificare che nello scadenzario dei Decreti di Sospensione siano presenti i procedimenti con Decreto Irreperibilita | 1.0 |  |  |  |  |
| SIUT | SIES | 20191122012.0 |  |  | 20191122012 | Errore bloccante nella generazione della stampa del provvedimento relativo
 al "Dettaglio Detenzione Domicilare a Termine" |  | SIEP | Errore bloccante nella generazione della stampa del provvedimento relativo
 al "Dettaglio Detenzione Domicilare a Termine" | TF008.SIEP | Verifica: verificare la correttezza della stampa per il provvedimento di "Dettaglio Detenzione Domicilare a Termine" |  |  |  | Verifica: verificare la correttezza della stampa per il provvedimento di "Dettaglio Detenzione Domicilare a Termine" | 1.0 |  |  |  |  |
| SIUT | SIES | 201911260110.0 |  |  | 201911260110.0 | Errore su template post patch |  | SIEP | Errore su template post patch | TF009.SIEP | Verifica: verificare che in corrispondenza di un provvedimento di cumulo (Emissione provvedimento di cumulo – Ordine di Esecuzione per la carcerazione con traduzione in carcere) il sistema generi correttamente il template associato |  |  |  | Verifica: verificare che in corrispondenza di un provvedimento di cumulo (Emissione provvedimento di cumulo – Ordine di Esecuzione per la carcerazione con traduzione in carcere) il sistema geeneri correttamente il template associato | 1.0 |  |  |  |  |
| SIUT | SIES | 201911250110.0 |  |  | 201911250110.0 | Errore bloccante Tribunale di Sorveglianza dei Minorenni di Roma il sistema non riconosce l’Ufficio del Magistrato di Sorveglianza per i Minorenni di Roma quando viene formato un fascicolo E.M.A. sul fasc. portante |  | SIUS | Errore bloccante Tribunale di Sorveglianza dei Minorenni di Roma il sistema non riconosce l’Ufficio del Magistrato di Sorveglianza per i Minorenni di Roma quando viene formato un fascicolo E.M.A. sul fasc. portante | TF010.SIUS | Verifica: verificare che in fase di iscrizione di un fascicolo E.M.A. il sistema riconosca la tipologia di ufficio Ufficio del Magistrato di Sorveglianza per i Minorenni |  |  |  | Verifica: verificare che in fase di iscrizione di un fascicolo E.M.A. il sistema riconosca la tipologia di ufficio Ufficio del Magistrato di Sorveglianza per i Minorenni | 1.0 |  |  |  |  |
| SIUT | SIES | 20191122014.0 |  |  | 20191122014.0 | Tribunale Ricorsi in Cassazione |  | SIGE | Sige - Tribunale Ricorsi in Cassazione | TF011.SIGE | Verifica: verificare dalla pagina di dettaglio di un ricorso SIGE che il soggetto presentante corrisponda a quello inseirto dall'utente in fase di emissione del ricorso stesso |  |  |  | Verifica: verificare dalla pagina di dettaglio di un ricorso SIGE che il soggetto presentante corrisponda a quello inseirto dall'utente in fase di emissione del ricorso stesso | 1.0 |  |  |  |  |
| SIUT | SIES | 20191122013.0 |  |  | 20191122013.0 | Corte D'Appello - Errata indicazione del depositante nel ricorso per cassazione |  | SIGE | SIGE - Corte D'Appello - Errata indicazione del depositante nel ricorso per cassazione | TF012.SIGE | Verifica: verificare dalla pagina di dettaglio di un ricorso SIGE che il soggetto presentante corrisponda a quello inseirto dall'utente in fase di emissione del ricorso stesso |  |  |  | Verifica: verificare dalla pagina di dettaglio di un ricorso SIGE che il soggetto presentante corrisponda a quello inseirto dall'utente in fase di emissione del ricorso stesso | 1.0 |  |  |  |  |
| SIUT | SIES | 20191114019 |  |  | 20191114019.0 | mancata registrazione data inizio misura |  | SIEP | SIES - mancata registrazione data inizio misura | TF013.SIEP | Verifica: verificare dalla funzione di Registrazione Inizio Misura che in fase di inserimento della data di inizio il sistema salvi correttemente tale informazione |  |  |  | Verifica: verificare dalla funzione di Registrazione Inizio Misura che in fase di inserimento della data di inizio il sistema salvi correttemente tale informazione | 1.0 |  |  |  |  |
| SIUT | SIES | 20191112019 |  |  | 20191112019.0 | Ancona Procura Minori non fa caricare inizio misura |  | SIEP | SIES - mancata registrazione data inizio misura | TF014.SIEP | Verifica: verificare dalla funzione di Registrazione Inizio Misura che in fase di inserimento della data di inizio il sistema salvi correttemente tale informazione |  |  |  | Verifica: verificare dalla funzione di Registrazione Inizio Misura che in fase di inserimento della data di inizio il sistema salvi correttemente tale informazione | 1.0 |  |  |  |  |

## Es.1

| Progetto / Obiettivo Software |  |  | SISP |  |  |  | Codifica Piano di test |  | CDC-20150009-S14-000-PT-20160129-01-SISP |  | v.1.0 |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Applicazione |  |  | Funzionalità / Requisiti non funzionali |  |  |  |  |  |  | Caso di test |  |  |  |  |  |  |  |  |  |
| Codice Area | Codice Appl. | ID. Requisito | ID | Primo livello | ID | Secondo Livello | Risk (1-5) | ID | Terzo livello | ID | Nome del caso di test | Risk (1-5) | Ciclo di test | Stima Durata | Descrizione e note | Versione | N. cond. di test | Autom. | Classe di rischio |
| 02 | 28 | REF001 | MF001 | Gestione Progetto | F005 | Dati Anagrafici di un Progetto | 4 | FE025 | Inserimento dati anagrafici | 02FE025-TF01 | Funzionalità generalizzate e funzioni accessorie | 1 | 2 | 15 | Dopo aver attivato dal menu di Navigazione il tasto "Inserimento":
- sia presente l'icona di attivazione della maschera di help e, selezionandola, venga mostrata la pagina di help della funzione da cui sia possibile tornare alla maschera chiamante
- sia presente il percorso di navigazione della funzione
- tutti i campi chiave siano editabiliti
-se presenti campi selezionabili da combo, siano valorizzati correttamente
-sia presente il bottone di Salva che, attivato comporti il salvataggio dei campi precedentemente inseriti
-sia presente il bottone Pulisci i Campi che, per il ripristino del valore di default per i tutti i campi editabili
-siano presenti ma non selezionabili tutti i Tab e i sottotab | 1.0 | 7.0 | 0 | Medio bassa |
| 02 | 28 | REF001 | MF001 | Gestione Progetto | F005 | Dati Anagrafici di un Progetto | 4 | FE025 | Inserimento dati anagrafici | 02FE025-TF02 | Inserimento corretto dati anagrafici | 5 | 1,2,5 | 45 | Verifica di tutte le condizioni positive di inserimento dati, compresa la verifica utilizzo dei valori di default, obbligatori, controlli formali, consistenza accesso multiutente. | 1.0 | 8.0 | 0 | Alta |
| 02 | 28 | REF001 | MF001 | Gestione Progetto | F005 | Dati Anagrafici di un Progetto | 4 | FE025 | Inserimento dati anagrafici | 02FE025-TF03 | Inserimento dati duplicati | 5 | 2 | 20 | Verifica l'inserimento di un dato anagrafico già presente | 1.0 | 1.0 | 0 | Alta |
| 02 | 28 | REF001 | MF001 | Gestione Progetto | F005 | Dati Anagrafici di un Progetto | 4 | FE025 | Inserimento dati anagrafici | 02FE025-TF04 | Inserimento dati non validi | 2 | 2 | 20 | Verifica l'inserimento di un dato anagrafico con dati non validi | 1.0 | 5.0 | 0 | Media |
| 02 | 28 | REF001 | MF001 | Gestione Progetto | F005 | Dati Anagrafici di un Progetto | 4 | FE025 | Inserimento dati anagrafici | 02FE025-TNF01 | Verifica Accessibilità | 2 | 4 | 20 | Utilizzo della checklist standard di accessibilità | 1.0 | 6.0 | 0 | Media |
| 02 | 28 | REF001 | MF001 | Gestione Progetto | F005 | Dati Anagrafici di un Progetto | 4 | FE025 | Inserimento dati anagrafici | 02FE025-TNF02 | Verifica Usabilità | 2 | 4 | 40 | Utilizzo della checklist standard di usabilità | 1.0 | 6.0 | 1 | Media |
| 02 | 28 | REF001 | MF001 | Gestione Progetto | F005 | Dati Anagrafici di un Progetto | 4 |  |  | 02F005-TI01 | Ricerca - visualizzazione - modifica e cancellazione anagrafica | 4 | 1,3 | 30 | Scenario di test di integrazione tra le funzioni elementari della funzione dati anagrafici, effettuare la ricerca, la visualizzazione, la modifica e la cancellazione | 1.0 | 3.0 | 1 | Alta |
| 02 | 28 | REF001 | MF001 | Gestione Progetto |  |  | 5 |  |  | 02MF001-TI01 | Creazione progetto, inserimento e modifica anagrafica, stampa resoconto. | 4 | 3 | 40 | Scenario di test di integrazione tra le funzioni di gestione dei dati anagrafici del progetto, creazione progetto, inserimento dati anagrafici, modifica e stampa. | 1.0 | 3.0 | 1 | Alta |
| 02 | 28 | REF001 | MF001 | Gestione Progetto | CDU001 | Ricerca ed elenco progetti | 3 | CDU001.1 | Scenario Main - ricerca elenco progetti | 02CDU001.1-TI01 | Ricerca - visualizzazione elenco progetti | 5 | 3 | 30 | Scenario di test relativo al  flusso main del caso d'uso, prevede la ricerca, visualizzazione dell'elenco dei progetti ricercati, per i quali l'utente risulta abilitato. | 1.0 | 1.0 | 0 | Alta |
| 02 | 28 | REF001 | MF001 | Gestione Progetto | CDU001 | Ricerca ed elenco progetti | 3 | CDU001.2 | Scenario Alternativo 1 - ricerca elenco progetti vuota - annulla | 02CDU001.2-TI01 | Ricerca - lista vuota - annulla | 2 | 3 | 30 | Scenario di test relativo allo scenario del caso d'uso derivato dal flusso alternativo di ricderca con esito lista vuota e richiesta di annullamento della ricerca. | 1.0 | 1.0 | 1 | Media |
| 02 | 28 | RNF012 | RNF012 | Requisito non funzonale di accessibilità | RNF012.1 | Verifica legge Stanca (4/2004) | 5 |  |  | 02RNF012.1-TNF01 | Checklist Accessibilità | 3 | 4 | 60 | Check list per la verifica dei 22 requisiti di accessibilità previsti | 1.0 | 22.0 | 1 | Alta |
| 02 | 28 | RNF031 | RNF031 | Requisito non funzonale di Performance | RNF031.1 | Caricamento liste dati entro massimo 20 secondi | 3 |  |  | 02RNF031.1-TNF01 | Performance Test su ricerca dati progetto | 4 | 4 | 30 | Effettuare test prestazionali in condizioni di carico sulla base delle analisi di utenza, per verificare il tempo di risposta all'utente nel caricamento della lista dei dati. | 1.0 | 1.0 | 0 | Medio alta |

## Descrizioni

| Lvl | Object Type | ID | Name | Risk | Description |
| --- | --- | --- | --- | --- | --- |

## Desc Temp

| Lvl | Object Type | ID | Name | Risk | Description |
| --- | --- | --- | --- | --- | --- |

## Cop.All.2ASpec.test

|  |  |
| --- | --- |
|  | Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A -                         Sirfin-PA     nell’ambito del contratto CIG 73479643B7 per lo “SVILUPPO DEL SISTEMA INFORMATIVO UNITARIO TELEMATICO, LA MANUTENZIONE DEGLI ATTUALI SISTEMI DELL’AREA PENALE DEL MINISTERO DELLA GIUSTIZIA E SERVIZI CORRELATI. LOTTO 1” |
|  | <Codifica Piano di test> |
|  | Piano di test - <fase> |
|  | Ver. x.x |
|  | Data: ../../.. |
|  | <Progetto / Obiettivo Software> |
|  | <Area Applicativa> |
|  | Allegato 2 - Specifiche di Test |

## SpecificaTest

| Progetto / Obiettivo Software |  |  | SIUT |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | SIUT-SIES-CT-1.0-20191206-Allegato-al-piano-test.xls |  |  |  |  |  |  |
| ID caso di test | Suffisso Caso di test | Nome Caso di test
Tipo Step | Istruzioni | Descrizione | Risultati attesi | Versione | Stima tempo | N.cond. di test | Esito |
| TF001.SIUS | 01 | SIUS - Problema cancellazione note dopo scarico ordinanza di rinvio udienza |  | Verifica: verificare che il campo note sulla maschera di dettaglio del procedimento rimanga valorizzato, se presente, a seguito di emissione di ordinanza di rinvio udienza |  | 1.0 | 15.0 | 1.0 | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIUS | Dxxxxx (Tribunale di Sorveglianza ) |  |  |  |  |  |
|  | P | Stato Base |  |  |  |  |  |  |  |
|  | 1 | Navigazione | Ricerche e Visualizzazioni --> Procedimento per n° SIUS |  |  |  |  |  |  |
|  | 2 | Azione | L'utente individua un procedimento con nota valorizzata, per cui è già stato emesso e validato un decreto di fissazione udienza |  |  |  |  |  |  |
|  | 3 | Azione | L'utente naviga nel menu "Udienza/Rinvio Udienza/Ordinanza Rinvio Udienza" |  | Il sistema mostra la pagina per l'inserimento dell'ordinanza di rinvio udienza |  |  |  |  |
|  | 4 | Azione | L'utente valorizza i campi obbligatori e procede con l'inserimento |  | Il sistema mostra la pagina di dettaglio dell'ordinanza di rinvio udienza |  |  |  |  |
|  | 5 | Azione | L'utente valida l'ordinanza |  |  |  |  |  |  |
|  | V | Verifica | Verificare che il campo Note risulti valorizzato sulla pagina di dettaglio del procedimento |  |  |  |  |  |  |
| TF002.SIGE | 01 | SIGE - La pagina iniziale del fascicolo non visualizza le date di rinvio delle udienze |  | Verifica: verificare che la data udienza deve essere visibile anche per tipo provvedimento 'Rinvio udienza da verbale' |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIGE | Txxxxx (Tribunale Ordinario ) |  |  |  |  |  |
|  | P | Stato Base |  |  |  |  |  |  |  |
|  | 1 | Navigazione | Udienze/Fissazione/Rinvio/Ruolo » Ordinanza Rinvio Udienza |  |  |  |  |  |  |
|  | 2 | Azione | Indicare un fascicolo SIGE e cliccare sul pulsante Conferma |  | Pagina contenente L'inserimento Ordinanza Rinvio Udienza |  |  |  |  |
|  | 3 | Azione | Inserire i campi obbligatori e la nuova data di udienza. Cliccare su 'Conferma' |  | Pagina contenente il Dettaglio Ordinanza Rinvio Udienza |  |  |  |  |
|  | 4 | Navigazione | Ricerche » Procedimento per n° SIGE |  |  |  |  |  |  |
|  | 5 | Azione | Indicare il fascicolo SIGE dello step 2 e cliccare sul pulsante Conferma |  | Pagina contenente Dettaglio Procedimento SIGE |  |  |  |  |
|  | V | Verifica | Verificare che nella pagina visualizzata nella parte dei provvedimenti sia indicata correttamente la data invio udienza inserita nello step 3 |  |  |  |  |  |  |
| TF003.SIEP | 01 | SIEP – Emissione liberazione anticipata per detenuto agli arresti domiciliari |  | Verifica: verificare che per la posizione giuridica 'Arresti Domiciliare ex art 89 dpr 309/90 - ex art. 656 comma 10 cpp' venga caricata la pagina mostrando la sezione dei destinatari, come previsto per la posizione giuridica 'Arresti domiciliari ex art.656/10' |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Txxxxx (Tribunale Ordinario ) |  |  |  |  |  |
|  | P | Stato Base |  |  |  |  |  |  |  |
|  | 1 | Navigazione |  |  |  |  |  |  |  |
|  | 2 | Azione | L'utente individua un procedimento per il quale il soggetto collegato ha come posizione giuridica ''Arresti Domiciliare ex art 89 dpr 309/90 - ex art. 656 comma 10 cpp" |  |  |  |  |  |  |
|  | 3 | Azione | L'utente, dal menù Decisioni della Sorveglianza, emette un Ordine di Scarcerazione per Liberazione. |  | Il sistema mostra la pagina corretta per l'inserimento dell' Ordine di Scarcerazione per Liberazione mostrando tutte le sezioni dei destinatari. |  |  |  |  |
| TF004.SIGE | 01 | SIGE - Soggetto presentante |  | Verifica: verificare dalla pagina di dettaglio di un ricorso SIGE che il soggetto presentante corrisponda a quello inserito dall'utente in fase di emissione del ricorso stesso |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIGE | Txxxxx (Tribunale Ordinario ) |  |  |  |  |  |
|  | P | Stato Base |  |  |  |  |  |  |  |
|  | 1 | Navigazione |  |  |  |  |  |  |  |
|  | 2 | Azione | L'utente individua un fascicolo SIGE per cui è presente un ricorso |  |  |  |  |  |  |
|  | 3 | Azione | L'utente naviga nel menu "Opposizioni/Ricorsi/Ricorso" e preme il pulsante "Elenco Ricorsi per il Provvedimento" |  |  |  |  |  |  |
|  | 4 | Azione | L'utente clicca sull'icona dettaglio del ricorso (lentina) |  | Il sistema mostra la pagina di dettaglio |  |  |  |  |
|  | V | Verifica | Verificare che il soggetto presentante sia coerente con quanto inserito precedentemente |  |  |  |  |  |  |
| TF005.SIEP | 01 | SIEP - Errore bloccante nella generazione della stampa del provvedimento
relativo al "Dettaglio Detenzione Domicilare a Termine" |  | Verifica: verificare la correttezza della stampa per il provvedimento di "Dettaglio Detenzione Domicilare a Termine" |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario ) |  |  |  |  |  |
|  | P | Stato Base | L'utente individua un procedimento SIEP con Soggetto in Espiazione Pena in Regime Carcerario con pena residua da espiare |  |  |  |  |  |  |
|  | 1 | Navigazione | L'utente dal menù Decisioni Sorveglianza , seleziona la funzione Differimento Pena nella forme della detenzione domiciliare (concessione) |  | Il sistema mostra la pagina per inserire il Differimento |  |  |  |  |
|  | 2 | Azione | L'utente inserisce i dati i dati in maschera e conferma l'operazione di inserimento. |  | Il sistema mostra la pagina di dettaglio del provvedimento inserito. |  |  |  |  |
|  | 3 | Azione | A seguirte l'utente seleziona l’azione di stampa |  | Il sistema genera la stampa corrispondente al provvedimento (template SIEP_MA_DETERM_DET.rtf) |  |  |  |  |
|  | V | Verifica | Verificare la correttezza del template prodotto |  |  |  |  |  |  |
| TF006.SIEP | 01 | SIEP -Non fornisce lo scadenziario per DS notificato con Decreto Irreperibilita |  | Verifica: verificare che nello scadenzario dei Decreti di Sospensione siano presenti i procedimenti con Decreto Irreperibilita |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario ) |  |  |  |  |  |
|  | P | Stato Base | L'utente individua un procedimento SIEP con soggetto Libero con pena da espiare |  |  |  |  |  |  |
|  | 1 | Navigazione | L'utente naviga al menù Ordini di Esecuzione/Scarcerazione>Sospensione Esecuzione ex art. 656 c.p.p.>Ordine di esecuzione |  |  |  |  |  |  |
|  | 2 | Azione | L'utente inserisce il  provvedimento, stampa e valida |  |  |  |  |  |  |
|  | 3 | Navigazione | A seguire l'utente naviga al menù Ordini di Esecuzione/Scarcerazione>Sospensione Esecuzione ex art. 656 c.p.p.>Gestione Decreto di Sospensione>Notifiche>Difensore |  |  |  |  |  |  |
|  | 4 | Azione | Nella machera che si presenta l'utente inserisce la data notifica |  |  |  |  |  |  |
|  | 5 | Navigazione | A seguire l'utente naviga al menù Verbali Arresto/Vane Ricerche Notifica Carcere>Verbale Vane Ricerche |  |  |  |  |  |  |
|  | 6 | Azione | L'utente prosegue con l' inserimento del verbale |  |  |  |  |  |  |
|  | 7 | Navigazione | A seguire l'utente naviga al menù Ordini di Esecuzione/Scarcerazione>Sospensione Esecuzione ex art. 656 c.p.p.>Gestione Decreto di Sospensione>Irreperibilità>Decreto |  |  |  |  |  |  |
|  | 8 | Azione | L'utente prosegue con l' inserimento del decreto, stampa e valida |  |  |  |  |  |  |
|  | 9 | Navigazione | A seguire l'utente naviga al menù Ordini di Esecuzione/Scarcerazione>Sospensione Esecuzione ex art. 656 c.p.p.>Gestione Decreto di Sospensione>Irreperibilità>Registrazione Notifica |  |  |  |  |  |  |
|  | 10 | Azione | L'utente prosegue con l' inserimento della data di notifica |  |  |  |  |  |  |
|  | 11 | Navigazione | A seguire l'utente naviga al menù Scadenzari>Sospensione Esecuzione ex art. 656 c.p.p |  |  |  |  |  |  |
|  | 12 | Azione | L'utente seleziona la voce 'Tutti' |  | Viene visualizzato un elenco |  |  |  |  |
|  | V | Verifica | Verificare che nell’elenco presentato ci sia  il procedimento lavorato |  |  |  |  |  |  |
| TF007.SIEP | 01 | SIEP - DECRETI IRREPERIBILITA' LEGGE SIMEONE |  | Verifica: verificare che nello scadenzario dei Decreti di Sospensione siano presenti i procedimenti con Decreto Irreperibilita |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario ) |  |  |  |  |  |
|  | P | Stato Base | L'utente individua un procedimento SIEP con soggetto Libero con pena da espiare |  |  |  |  |  |  |
|  | 1 | Navigazione | L'utente naviga al menù Ordini di Esecuzione/Scarcerazione>Sospensione Esecuzione ex art. 656 c.p.p.>Ordine di esecuzione |  |  |  |  |  |  |
|  | 2 | Azione | L'utente inserisce il  provvedimento, stampa e valida |  |  |  |  |  |  |
|  | 3 | Navigazione | A seguire l'utente naviga al menù Ordini di Esecuzione/Scarcerazione>Sospensione Esecuzione ex art. 656 c.p.p.>Gestione Decreto di Sospensione>Notifiche>Difensore |  |  |  |  |  |  |
|  | 4 | Azione | Nella machera che si presenta l'utente inserisce la data notifica |  |  |  |  |  |  |
|  | 5 | Navigazione | A seguire l'utente naviga al menù Verbali Arresto/Vane Ricerche Notifica Carcere>Verbale Vane Ricerche |  |  |  |  |  |  |
|  | 6 | Azione | L'utente prosegue con l' inserimento del verbale |  |  |  |  |  |  |
|  | 7 | Navigazione | A seguire l'utente naviga al menù Ordini di Esecuzione/Scarcerazione>Sospensione Esecuzione ex art. 656 c.p.p.>Gestione Decreto di Sospensione>Irreperibilità>Decreto |  |  |  |  |  |  |
|  | 8 | Azione | L'utente prosegue con l' inserimento del decreto, stampa e valida |  |  |  |  |  |  |
|  | 9 | Navigazione | A seguire l'utente naviga al menù Ordini di Esecuzione/Scarcerazione>Sospensione Esecuzione ex art. 656 c.p.p.>Gestione Decreto di Sospensione>Irreperibilità>Registrazione Notifica |  |  |  |  |  |  |
|  | 10 | Azione | L'utente prosegue con l' inserimento della data di notifica |  |  |  |  |  |  |
|  | 11 | Navigazione | A seguire l'utente naviga al menù Scadenzari>Sospensione Esecuzione ex art. 656 c.p.p |  |  |  |  |  |  |
|  | 12 | Azione | L'utente seleziona la voce 'Tutti' |  | Viene visualizzato un elenco |  |  |  |  |
|  | V | Verifica | Verificare che nell’elenco presentato ci sia  il procedimento lavorato |  |  |  |  |  |  |
| TF008.SIEP | 01 | SIEP - Errore bloccante nella generazione della stampa del provvedimento relativo  al "Dettaglio Detenzione Domicilare a Termine" |  | Verifica: verificare la correttezza della stampa per il provvedimento di "Dettaglio Detenzione Domicilare a Termine" |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario ) |  |  |  |  |  |
|  | P | Stato Base | L'utente individua un procedimento SIEP con Soggetto in Espiazione Pena in Regime Carcerario con pena residua da espiare |  |  |  |  |  |  |
|  | 1 | Navigazione | L'utente dal menù Decisioni Sorveglianza , seleziona la funzione Differimento Pena nella forme della detenzione domiciliare (concessione) |  | Il sistema mostra la pagina per inserire il Differimento |  |  |  |  |
|  | 2 | Azione | L'utente inserisce i dati i dati in maschera e conferma l'operazione di inserimento. |  | Il sistema mostra la pagina di dettaglio del provvedimento inserito. |  |  |  |  |
|  | 3 | Azione | A seguirte l'utente seleziona l’azione di stampa |  | Il sistema genera la stampa corrispondente al provvedimento (template SIEP_MA_DETERM_DET.rtf) |  |  |  |  |
|  | V | Verifica | Verificare la correttezza del template prodotto |  |  |  |  |  |  |
| TF009.SIEP | 01 | SIEP - Errore su template post patch |  | Verifica: verificare che in corrispondenza di un provvedimento di cumulo (Emissione provvedimento di cumulo – Ordine di Esecuzione per la carcerazione con traduzione in carcere) il sistema geeneri correttamente il template associato |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario ) |  |  |  |  |  |
|  | P | Stato Base | L'utente individua un procedimento SIEP validato con pena complessiva |  |  |  |  |  |  |
|  | 1 | Navigazione | L'utente naviga sulla funzione Gestione Cumulo>Apertura Istruttoria |  |  |  |  |  |  |
|  | 2 | Azione | Dal Dettaglio Istruttoria Cumulo>Dati Finali Cumulo effettuare tutti i passaggi previsti in Dati Finali, Pene Rideterminate, Posizione Giuridica |  |  |  |  |  |  |
|  | 3 | Azione | In Posizione Giuridica inserire Collocamento in comunità ex art. 656 comma 10 cpp |  |  |  |  |  |  |
|  | 4 | Azione | Eseguire Calcolo Pena (presente sempre in Dati Finali) |  |  |  |  |  |  |
|  | 5 | Azione | Selezionare Emissione Provvedimento, nella form, in Tipologia selezionare Emissione provvedimento di cumulo – Ordine di Esecuzione per la carcerazione con traduzione in carcere, compilare   gli altri dati obbligatori e inserire il provvedimento |  |  |  |  |  |  |
|  | 6 | Azione | Dalla pagina successiva di Dettaglio, utilizzare la funzione di stampa |  | Il sistema genera il template SIEP_CUMULO_OE_656_LIB_C10_TRAD.rtf |  |  |  |  |
|  | V | Verifica | Verificare che il documento venga generato correttamente |  |  |  |  |  |  |
| TF010.SIUS | 01 | SIUS - Errore bloccante Tribunale di Sorveglianza dei Minorenni di Roma il sistema non riconosce l’Ufficio del Magistrato di Sorveglianza per i Minorenni di Roma quando viene formato un fascicolo E.M.A. sul fasc. portante |  | Verifica: verificare che in fase di iscrizione di un fascicolo E.M.A. il sistema riconosca la tipologia di ufficio Ufficio del Magistrato di Sorveglianza per i Minorenni |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIUS | Vxxxxx (Ufficio di Sorveglianza presso il Tribunale per minorenni ) |  |  |  |  |  |
|  | P | Stato Base |  |  |  |  |  |  |  |
|  | 1 | Navigazione | Presa in carico atti pervenuti » Ricerca per Atti - SIUS |  |  |  |  |  |  |
|  | 2 | Azione | Valorizzare i campi obbligatori ed un fascicolo SIUS. Cliccare su Ricerca |  | Visualizzazione della pagina contenente la Lista Atti Ricevuti |  |  |  |  |
|  | 3 | Azione | Cliccare sulla lente Dettagli presente tra le Azioni |  | Visualizzazione della pagina di dettaglio Ordinanza Ricevuta |  |  |  |  |
|  | 4 | Azione | Cliccare sul pulsante Conferma Presa in Carico |  | Visualizzazione della pagina contenente il messaggio:"Ricezione Ordinanza Completata e Esito Rispedito al Mittente. Iscrivereilprocedimento SIUS!" |  |  |  |  |
|  | 5 | Azione | Cliccare sul pulsante OK |  | Visualizzazione della pagina Presa in Carico atto pervenuto da SIUS |  |  |  |  |
|  | 6 | Azione | Inserire i campi obbligatori:
Contenuto, Data arrivo in cancelleria e Magistrato e poi Cliccare su “Conferma” |  |  |  |  |  |  |
|  | V | Verifica | Verificare che non sipresenti il problema segnalato ovvero che non venga prospettato a seguito dell'ultimo step il messagio di errore 'Ufficio Inesistente' |  |  |  |  |  |  |
| TF011.SIGE | 01 | SIGE - Tribunale Ricorsi in Cassazione |  | Verifica: verificare dalla pagina di dettaglio di un ricorso SIGE che il soggetto presentante corrisponda a quello inserito dall'utente in fase di emissione del ricorso stesso |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIGE | Txxxxx (Tribunale Ordinario ) |  |  |  |  |  |
|  | P | Stato Base |  |  |  |  |  |  |  |
|  | 1 | Navigazione |  |  |  |  |  |  |  |
|  | 2 | Azione | L'utente individua un fascicolo SIGE per cui è presente un ricorso |  |  |  |  |  |  |
|  | 3 | Azione | L'utente naviga nel menu "Opposizioni/Ricorsi/Ricorso" e preme il pulsante "Elenco Ricorsi per il Provvedimento" |  |  |  |  |  |  |
|  | 4 | Azione | L'utente clicca sul dettaglio del ricorso |  |  |  |  |  |  |
|  | V | Verifica | Verificare che il soggetto presentante sia coerente con quanto inserito precedentemente |  |  |  |  |  |  |
| TF012.SIGE | 01 | SIGE - Corte D'Appello - Errata indicazione del depositante nel ricorso per cassazione |  | Verifica: verificare dalla pagina di dettaglio di un ricorso SIGE che il soggetto presentante corrisponda a quello inserito dall'utente in fase di emissione del ricorso stesso |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIGE | Txxxxx (Tribunale Ordinario ) |  |  |  |  |  |
|  | P | Stato Base |  |  |  |  |  |  |  |
|  | 1 | Navigazione |  |  |  |  |  |  |  |
|  | 2 | Azione | L'utente individua un fascicolo SIGE per cui è presente un ricorso |  |  |  |  |  |  |
|  | 3 | Azione | L'utente naviga nel menu "Opposizioni/Ricorsi/Ricorso" e preme il pulsante "Elenco Ricorsi per il Provvedimento" |  |  |  |  |  |  |
|  | 4 | Azione | L'utente clicca sul dettaglio del ricorso |  |  |  |  |  |  |
|  | V | Verifica | Verificare che il soggetto presentante sia coerente con quanto inserito precedentemente |  |  |  |  |  |  |
| TF013.SIEP | 01 | SIEP - mancata registrazione data inizio misura |  | Verifica: verificare dalla funzione di Registrazione Inizio Misura che in fase di inserimento della data di inizio il sistema salvi correttemente tale informazione |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario ) |  |  |  |  |  |
|  | P | Stato Base |  |  |  |  |  |  |  |
|  | 1 | Navigazione | Verbali Arresto/Vane Ricerche Notifica Carcere » Registrazione Data Inizio Misura |  |  |  |  |  |  |
|  | 2 | Azione | Nella pagina inserire La data inizio misura di un procedimento SIEP e salvare il dato |  |  |  |  |  |  |
|  | V | Verifica | Verificare che la data di inizio misura sia registrata correttamente |  |  |  |  |  |  |
| TF014.SIEP | 01 | SIEP - Ancona Procura Minori non fa caricare inizio misura |  | Verifica: verificare dalla funzione di Registrazione Inizio Misura che in fase di inserimento della data di inizio il sistema salvi correttemente tale informazione |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario ) |  |  |  |  |  |
|  | P | Stato Base |  |  |  |  |  |  |  |
|  | 1 | Navigazione | Verbali Arresto/Vane Ricerche Notifica Carcere » Registrazione Data Inizio Misura |  |  |  |  |  |  |
|  | 2 | Azione | Nella pagina inserire La data inizio misura di un procedimento SIEP e salvare il dato |  |  |  |  |  |  |
|  | V | Verifica | Verificare che la data di inizio misura sia registrata correttamente |  |  |  |  |  |  |

## VerificheConformità

| Progetto / Obiettivo Software |  |  |  | SIUT |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  |  | 23 |  |  |
| ID | Tipo Verifica | Attributo | Indicatore | Descrizione tipo Verifica | Esito Verifica Fornitore | Esito Verifica Amministrazione |

## SogliaAccettazione

| Progetto / Obiettivo Software |  |  | SIUT |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | 23 |  |  |  |
| Verifica Soglia di Accettazione |  |  |  |  |  | In Rosso le difformità che hanno superato il numero massimo ammissibile |
| Classe di rilevanza | Classe di gravità |  |  |  |  |  |
|  | 1.0 | 2.0 | 3.0 | 4.0 |  |  |
| A |  |  |  |  |  |  |
| B |  |  |  |  |  |  |
| C |  |  |  |  |  |  |
| Numero massimo di difformità ammesse |  |  |  |  |  |  |
| Classe di rilevanza | Classe di gravità |  |  |  |  |  |
|  | 1.0 | 2.0 | 3.0 | 4.0 |  |  |
| A |  |  |  |  |  |  |
| B |  |  |  |  |  |  |
| C |  |  |  |  |  |  |

## Automation

|  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Progetto / Obiettivo Software |  |  |  |  |  |  |  |
| Codifica Piano di test |  |  |  |  |  |  |  |
| ID caso di test | VisualTest | Descrizione | Durata Stimata | QADirector Client | QADirector ToolDomain | TestPartner Project | Stima tempo |

## Es.2

| Progetto / Obiettivo Software |  |  | Gestione Progetto |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | ISC-PDT-C26_M_15 |  |  |  |  |  |
| ID caso di test | Suffisso Script di test | Nome Script di test |  | Descrizione |  | Versione | Stima Durata | N. cond. di test |
| nome del test | 01 | Nome dello script di test |  | Descrizione dello script di test (inserire il layout con la macro CTRL-A) |  |  |  |  |
|  | Step | Tipo Step | Istruzioni | Dati di input | Risultati attesi |  |  |  |
|  | P | Precondizioni | descrivere le precondizioni | i dati per le precondizioni | la verifica delle precondizioni |  |  |  |
|  | P | Stato Base | descrivere il posizionamento dell'applicazione | i dati necessari, esempio login | la verifica dello stato base |  |  |  |
|  | 1.0 | Navigazione | descrivere uno o più pasi di navigazione | i dati se presenti | il risultato al termine della navigazione |  |  |  |
|  | 2.0 | Azione | descrivere la/le azioni dell'utente | i dati utilizzati | i risultati al termine delle azioni |  |  |  |
|  | 3.0 | Navigazione | descrivere uno o più pasi di navigazione | i dati se presenti | il risultato al termine della navigazione |  |  |  |
|  | R1 | Riciclo Test | Indicare lo/gli step sul quale effettuare i cambiamenti e descrivere l'obiettivo del ricicli | i nuovi dati | i risultati al termine delle azioni |  |  |  |
|  | V | Verifica esterna | descrivere eventuali verifiche esterne da effettuare al termine del test per la verifica dello stesso | i dati se presenti | i risultati al termine delle verifiche |  |  |  |
| 02FE025-TF02 | 01 | Inserimento corretto dati anagrafici |  | Verifica di tutte le condizioni positive di inserimento dati, compresa la verifica utilizzo dei valori di default, obbligatori, controlli formali, consistenza accesso multiutente. |  | 1.0 | 45.0 | 8.0 |
|  | Step | Tipo step | Istruzioni | Dati di input | Risultati attesi |  |  |  |
|  | P | Precondizioni | Progetto già definito ma senza informazioni anagrafiche | codice locale progetto : 1234567890 |  |  |  |  |
|  | P | Stato Base | Sessione aperta sull'applicazione, sul menu principale del progetto inserito.. Autenticato con utente 'gestore progetto'. | Profilo utente "Gestore Progetto".
codice locale progetto : 1234567890 | Applicazione aperta sul menu principale |  |  |  |
|  | 1.0 | Navigazione | menu Progetto - Inserimento - Tab Dati Generali - Sottotab Dati Anagrafici |  | appare la maschera d'inserimento dati anagrafici |  |  |  |
|  | 2.0 | Azione | Inserire i dati per nuova anagrafica e selezionare bottone "Salva".
Il bottone “Salva” consente il salvataggio dei valori impostati nella pagina, nell’entità E004 - Progetti. | Codice locale progetto: 1234567890
Titolo = 
Codice Tipologia Operazione = 10
Cup Provvisorio = 
Cup Definitivo = 
Progetto Strategico = S
Codice Procedura = 0001
De Minimis = N | Il sistema mostra un messaggio indicante il mancato inserimento di dati obbligatori (Titolo) in testa alla maschera di Inserimento Dati Anagrafici e imposta i campi valorizzandoli con i dati appena inseriti |  |  |  |
|  | 3.0 | Navigazione | Selezione Tab di uscita, ritorno al menu |  | appare il menu principale |  |  |  |
|  | R1 | Riciclo Script | Rieseguire l'intero script ed inserire i nuovi dati allo step 2. | Codice locale progetto: 1234567890
Titolo = PROGETTO DI TEST
Codice Tipologia Operazione =
Cup Provvisorio = AA
Cup Definitivo = AA
Progetto Strategico = S
Codice Procedura = 0001
De Minimis = N | Il sistema mostra un messaggio indicante il mancato inserimento di dati obbligatori (codice tipologia operazione) in testa alla maschera di Inserimento Dati Anagrafici e imposta i campi valorizzandoli con i dati appena inseriti |  |  |  |
|  | R2 | Riciclo Script | Rieseguire l'intero script ed inserire i nuovi dati allo step 2. | Codice locale progetto: 1234567890
Titolo = PROGETTO DI TEST
Codice Tipologia Operazione = 10
Cup Provvisorio = AA
Cup Definitivo = AA
Progetto Strategico = S
Codice Procedura = 0001
De Minimis = N | Il sistema mostra un messaggio indicante i dati salvati correttamente. |  |  |  |
|  | R3 | Riciclo Script | Rieseguire l'intero script, i dati che il sistema propone allo step 2 non devono essere modificati. | Codice locale progetto: 1234567890
Titolo = PROGETTO DI TEST
Codice Tipologia Operazione = 10
Cup Provvisorio = AA
Cup Definitivo = AA
Progetto Strategico = S
Codice Procedura = 0001
De Minimis = N | Il sistema mostra un messaggio indicante il la mancata modifica e viene ripresentata la stessa schermata con gli stessi dettagli. |  |  |  |
|  | R4 | Riciclo Script | Rieseguire l'intero script da due utenze diverse ed inserire i nuovi dati allo step 2. Il primo utente seleziona il bottone salva.
Il secondo utente seleziona il bottone salva dopo il primo utente | Codice locale progetto: 1234567890
Titolo = PROGETTO DI TEST
Codice Tipologia Operazione = 10
Cup Provvisorio = BB
Cup Definitivo = BB
Progetto Strategico = S
Codice Procedura = 0001
De Minimis = N | Il secondo utente riceve dal sistema il messaggio che i dati sono stati variati da un altro utente, annulla le modifiche e ripresenta i dati correnti. |  |  |  |
|  | R5 | Riciclo Script | Rieseguire l'intero script ed inserire i nuovi dati allo step 2. | Codice locale progetto: 1234567890
Titolo = PROGETTO DI TEST
Codice Tipologia Operazione = 3
Cup Provvisorio = AA
Cup Definitivo = AA
Progetto Strategico = S
Codice Procedura = 0001
De Minimis = | Il sistema mostra un messaggio indicante il la necessita di valorizzare il campo De Minimis  per il codice Tipologia Operazione = 3. |  |  |  |
|  | R6 | Riciclo Script | Rieseguire l'intero script ed inserire i nuovi dati allo step 2. | Codice locale progetto: 1234567890
Titolo = PROGETTO DI TEST
Codice Tipologia Operazione = 3
Cup Provvisorio = AA
Cup Definitivo = AA
Progetto Strategico = S
Codice Procedura = 0001
De Minimis = S | Il sistema mostra un messaggio indicante i dati salvati correttamente. |  |  |  |
|  | R7 | Riciclo Script | Rieseguire l'intero script ed inserire i nuovi dati allo step 2. Selezionare bottone "Rispristina" invece che salva. | Codice locale progetto: 1234567890
Titolo = PROGETTO DI TEST
Codice Tipologia Operazione = 10
Cup Provvisorio = AA
Cup Definitivo = AA
Progetto Strategico = S
Codice Procedura = 0001
De Minimis = N | Il sistema ripropone i dati come presenti nell'ultimo salvataggio |  |  |  |
|  | V | Verifica esterna | Verificare i dati modificati nell'utlimo riciclo con esito positivo, direttamente  sui valori degli attributi dell'occorenza dell'entità E004 - Progetto. | Utilizzare la query "SQL_E004_verifica_dati_anagrafici" consegnata nel piano di test. | Gli attributi per il progetto modificato dal test devono corrispondere all'ultimo riciclo con esito positivo (salvataggio dati). |  |  |  |
| 02FE025-TF03 | 01 | Inserimento dati duplicati |  | Descrizione dello script di test (inserire il layout con la macro CTRL-A) |  |  |  |  |
| 02FE025-TF04 | 01 | Inserimento dati non validi |  | Descrizione dello script di test (inserire il layout con la macro CTRL-A) |  |  |  |  |
| 02FE025-TNF01 | 01 | Verifica Accessibilità |  | Descrizione dello script di test (inserire il layout con la macro CTRL-A) |  |  |  |  |
| 02FE025-TNF02 | 01 | Verifica Usabilità |  | Descrizione dello script di test (inserire il layout con la macro CTRL-A) |  |  |  |  |
| 02F005-TI01 | 01 | Ricerca - visualizzazione - modifica e cancellazione anagrafica |  | Descrizione dello script di test (inserire il layout con la macro CTRL-A) |  |  |  |  |
| 02MF001-TI01 | 01 | Creazione progetto, inserimento e modifica anagrafica, stampa resoconto. |  | Descrizione dello script di test (inserire il layout con la macro CTRL-A) |  |  |  |  |
| 02CDU001.1-TI01 | 01 | Ricerca - visualizzazione elenco progetti |  | Descrizione dello script di test (inserire il layout con la macro CTRL-A) |  |  |  |  |
| 02CDU001.2-TI01 | 01 | Ricerca - lista vuota - annulla |  | Descrizione dello script di test (inserire il layout con la macro CTRL-A) |  |  |  |  |
| 02RNF012.1-TNF01 | 01 | Checklist Accessibilità |  | Descrizione dello script di test (inserire il layout con la macro CTRL-A) |  |  |  |  |
| 02RNF031.1-TNF01 | 01 | Performance Test su ricerca dati progetto |  | Descrizione dello script di test (inserire il layout con la macro CTRL-A) |  |  |  |  |
| 02F018-TF04 | 01 | Corretta esecuzione della modifica delle procedure di attivazione |  | Verifica di tutte le condizioni positive di inserimento dati, compresa la verifica utilizzo dei valori di default |  | 1.0 | 10.0 | 3.0 |
|  | Step | Tipo | Istruzioni | Dati di input | Risultati attesi |  |  |  |
|  | P | Precondizioni | Precaricare il database, o con funzioni di inserimento, con una procedura di attivazione, senza richieste di predisposione dati | Qualsiasi procedura di attivazione senza richieste di predisposizione dati | Deve risultare presente in base dati almeno 1 procedura di attivazione e non devono essere presenti richieste di predisposizione dati |  |  |  |
|  | P | Stato Base | Sessione aperta sull'applicazione, utente 'loggato' con profilo 'amministrazione' | Profilo utente Amministrativo | Applicazione aperta sul menu principale |  |  |  |
|  | 1.0 | Navigazione | Selezione menu "procedure di attivazione" e "ricerca" |  | Appare la finestra di "procedure di attivazione" e poi la finestra "ricerca". |  |  |  |
|  | 2.0 | Azione | Selezione dell'icona 'Visualizza e Modifica"
Modificare i dati presenti nel campo Data Avvio, nessuna modifica.
Selezione  tasto "Salva" | Nessuno | Verificare che venga mostrato il messaggio "Nessun dato modificato" sulla pagina corrente. |  |  |  |
|  | 3.0 | Navigazione | Selezione la funzione di 'uscita' e successivamente di 'logout' |  | Appare la finestra di "procedure di attivazione" e poi la finestra di uscita dall'applicazione. |  |  |  |
|  | R1 | Riciclo Script | Modificare i dati presenti nel campo Data Avvio,  con campo data vuoto (step 2) | Data Avvio (gg/mm/aaaa)* : | Verificare che il sistema mostri il messaggio "Non è possibile effettuare operazione manca dato obbligatorio" in testa alla maschera di Modifica Procedure attivazione e riproponga come valore dei campi i dati appena inseriti. |  |  |  |
|  | R2 | Riciclo Script | Modificare i dati presenti nel campo Data Avvio,  con campo data valido (step 2) | Data Avvio (gg/mm/aaaa)* : 12/04/2007 | Verificare che il sistema mostri il messaggio "Operazione effettuata con successo" sulla maschera di Ricerca/Elenco Procedure attivazione e nella lista si vedano la procedura di attivazione con i dati appena modificati. |  |  |  |
|  | V | Verifica esterna | Verificare i dati modificati nella lista delle procedure di attivazione |  | Una volta modificati i dati il sistema aggiornerà sull'entità E02-Procedure di attivazione gli attributi Codice Utente Ultima Modifica pari all’utente in input alla funzione e Data Ultima Modifica pari alla data di sistema. |  |  |  |

## Settings

|  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Parametri per l'utilizzo delle macro QACenter di gestione della tabella dei test e delle specifiche di test e caricamento nel database
far riferimento alle guide operative Compuware per il loro utilizzo |  |  |  |  |  |  |  |  |  |  |  |  |
| Versione 3.2.4 | Project Settings |  |  |  |  |  |  |  |  |  |  |  |
|  | --- |  |  |  |  |  |  |  |  |  |  |  |
| ProjectID | --- |  |  |  |  |  |  |  |  |  |  |  |
| FolderID | 1.0 |  |  |  |  |  |  |  |  |  |  |  |
| DefaultUserID | Unassigned |  |  |  |  |  |  |  |  |  |  |  |
| Status | In Progress |  |  |  |  |  |  |  |  |  |  |  |
| Cycles | 10.0 |  |  | (1 to 20) |  |  |  |  |  |  |  |  |
| Level's Max Depth | 4.0 |  |  |  |  |  |  |  |  |  |  |  |
| First Data Row | 4.0 |  |  |  |  |  |  |  |  |  |  |  |
| Risk Model |  |  |  |  |  |  |  |  |  |  |  |  |
| DisplayID Assembly |  |  |  |  |  |  |  |  |  |  |  |  |
| Unique Progressive Key |  |  |  |  |  |  |  |  |  |  |  |  |
| Digit Number | 4.0 |  |  |  |  |  |  |  |  |  |  |  |
| Start From |  |  |  |  |  |  |  |  |  |  |  |  |
| Counter Gap | 1.0 |  |  |  |  |  |  |  |  |  |  |  |
| Preview | 0000 |  |  |  |  |  |  |  |  |  |  |  |
| Level 1 Requirement |  |  |  |  |  |  |  |  |  |  |  |  |
| Part ID | Value | Type | Length | Delimiter |  |  |  |  |  |  |  |  |
| Element 1 | N/A | Counter | 4.0 | b |  |  |  |  |  |  |  |  |
| Element 2 | RQ | String | 2.0 | - |  |  |  |  |  |  |  |  |
| Element 3 | E | column | 22.0 |  |  |  |  |  |  |  |  |  |
| Element 4 |  | None |  |  |  |  |  |  |  |  |  |  |
| Preview | 0000 RQ- | TOT Length |  | 30.0 |  |  |  |  |  |  |  |  |
| Level 2 Requirement |  |  |  |  |  |  |  |  |  |  |  |  |
| Part ID | Value | Type | Length | Delimiter |  |  |  |  |  |  |  |  |
| Element 1 | N/A | Counter | 4.0 | b |  |  |  |  |  |  |  |  |
| Element 2 | RQ | String | 2.0 | - |  |  |  |  |  |  |  |  |
| Element 3 | G | Column | 22.0 |  |  |  |  |  |  |  |  |  |
| Element 4 |  | None |  |  |  |  |  |  |  |  |  |  |
| Preview | 0000 RQ- | TOT Length |  | 30.0 |  |  |  |  |  |  |  |  |
| Level 3 Requirement |  |  |  |  |  |  |  |  |  |  |  |  |
| Part ID | Value | Type | Length | Delimiter |  |  |  |  |  |  |  |  |
| Element 1 | N/A | Counter | 4.0 | b |  |  |  |  |  |  |  |  |
| Element 2 | RQ | String | 2.0 | - |  |  |  |  |  |  |  |  |
| Element 3 | I | Column | 12.0 | - |  |  |  |  |  |  |  |  |
| Element 4 | J | Column | 9.0 |  |  |  |  |  |  |  |  |  |
| Preview | 0000 RQ-- | TOT Length |  | 30.0 |  |  |  |  |  |  |  |  |
| Test |  |  |  |  |  |  |  |  |  |  |  |  |
| Part ID | Value | Type | Length | Delimiter |  |  |  |  |  |  |  |  |
| Element 1 | N/A | Counter | 4.0 | b |  |  |  |  |  |  |  |  |
| Element 2 | TEST | String | 4.0 | - |  |  |  |  |  |  |  |  |
| Element 3 | K | Column | 20.0 |  |  |  |  |  |  |  |  |  |
| Element 4 |  | None |  |  |  |  |  |  |  |  |  |  |
| Preview | 0000 TEST- | TOT Length |  | 30.0 |  |  |  |  |  |  |  |  |
| Test Plan Columns Map |  |  |  |  |  |  |  |  |  |  |  |  |
| Element | Value | Type |  |  |  |  |  |  |  |  |  |  |
| Area Id | A | Column |  |  |  |  |  |  |  |  |  |  |
| Application Id | B | Column |  |  |  |  |  |  |  |  |  |  |
| Custom Requirement Id | C | Column |  |  |  |  |  |  |  |  |  |  |
| Lvl1 Requirement Id | D | Column |  |  |  |  |  |  |  |  |  |  |
| Lvl1 Requirement | E | Column |  |  |  |  |  |  |  |  |  |  |
| Lvl2 Requirement Id | F | Column |  |  |  |  |  |  |  |  |  |  |
| Lvl2 Requirement | G | Column |  |  |  |  |  |  |  |  |  |  |
| Requirement Area Risk | H | Column |  |  |  |  |  |  |  |  |  |  |
| Lvl3 Requirement Id | I | Column |  |  |  |  |  |  |  |  |  |  |
| Lvl3 Requirement | J | Column |  |  |  |  |  |  |  |  |  |  |
| Test Case Id | K | Column |  |  |  |  |  |  |  |  |  |  |
| Test Case Name | L | Column |  |  |  |  |  |  |  |  |  |  |
| Test Case Description | P | Column |  |  |  |  |  |  |  |  |  |  |
| Test Case Risk | M | Column | Column |  |  |  |  |  |  |  |  |  |
| Test Case Cycles | N | Column |  |  |  |  |  |  |  |  |  |  |
| Test Case Estimated Time | O | Column |  |  |  |  |  |  |  |  |  |  |
| Script Version | Q | Column |  |  |  |  |  |  |  |  |  |  |
| Test Conditions N | R | Column |  |  |  |  |  |  |  |  |  |  |
| Is Test Automated | S | Column |  |  |  |  |  |  |  |  |  |  |
| Risk Class | T | Column |  |  |  |  |  |  |  |  |  |  |
| Risk Class (Formula) | IF(H4*M4<1,"Nessuna",(IF(H4*M4<=2,"Bassa",(IF(H4*M4<=4,"Sotto la media",(IF(H4*M4<=9,"Media",(IF(H4*M4<=12,"Sopra la media","Alta"))))))))) | Formula |  |  |  |  |  |  |  |  |  |  |
| Lvl1 Req Display Id | AF | Hidden Column |  |  |  |  |  |  |  |  |  |  |
| Lvl2 Req Display Id | AG | Hidden Column |  |  |  |  |  |  |  |  |  |  |
| Lvl3 Req Display Id | AH | Hidden Column |  |  |  |  |  |  |  |  |  |  |
| Test Case Display Id | AI | Hidden Column |  |  |  |  |  |  |  |  |  |  |
| FA1 Auto Risk | AJ | Hidden Column |  |  |  |  |  |  |  |  |  |  |
| Test Script Layout |  |  |  |  |  |  | Calcolo classe di rischio - matrice valori |  |  |  |  |  |
| Test Script Layout Sheet | Layout | macro invoked |  |  |  |  |  | Funzione o requisito |  |  |  |  |
| Layout Detailed Range | A5:I12 | CTRL-A PasteScriptLayout() |  |  |  |  | Caso test | 1.0 | 2.0 | 3.0 | 4.0 | 5.0 |
| Layout Vague Range |  | CTRL_S PasteScriptLayoutVague() |  |  |  |  | 1.0 | 1.0 | 2.0 | 3.0 | 4.0 | 5.0 |
| Test Script Sheet OUT | All.2Spec.test | Text |  |  |  |  | 2.0 | 2.0 | 4.0 | 6.0 | 8.0 | 10.0 |
| Test Script Status |  |  |  |  |  |  | 3.0 | 3.0 | 6.0 | 9.0 | 12.0 | 15.0 |
| Script Header |  |  |  |  |  |  | 4.0 | 4.0 | 8.0 | 12.0 | 16.0 | 20.0 |
| Test Case ID | A | Column (Layout Sheet) |  |  |  |  | 5.0 | 5.0 | 10.0 | 15.0 | 20.0 | 25.0 |
| Script Suffix | B | Column (Layout Sheet) |  |  |  |  | Condizioni per la formula |  |  |  |  |  |
| Test Case Name | C | Column (Layout Sheet) |  |  |  |  | se < 1 |  |  | nessuna |  |  |
| Description | E | Column (Layout Sheet) |  |  |  |  | se <= 2 |  |  | bassa |  |  |
| Script Version | G | Column (Layout Sheet) |  |  |  |  | se <= 4 |  |  | sotto media |  |  |
| Script Time | H | Column (Layout Sheet) |  |  |  |  | se <=9 |  |  | media |  |  |
| Test Conditions | I | Column (Layout Sheet) |  |  |  |  | se <= 16 |  |  | sopra la media |  |  |
| Script ID Delimiter Char | . | Char |  |  |  |  | altri casi |  |  | alta |  |  |
| Script Details |  |  |  |  |  |  | Formula per cella Classe di rischio |  |  |  |  |  |
| Step Number | B | Column (Layout Sheet) |  |  |  |  | SE(H4*M4<1;"Nessuna";SE(H4*M4<=2;"Bassa";SE(H4*M4<=4;"Sotto la media";SE(H4*M4<=9;"Media";SE(H4*M4<=12;"Sopra la media";"Alta"))))) |  |  |  |  |  |
| Step Type | C | Column (Layout Sheet) |  |  |  |  |  |  |  |  |  |  |
| Instructions Text | D | Column (Layout Sheet) |  |  |  |  |  |  |  |  |  |  |
| Associated Data | E | Column (Layout Sheet) |  |  |  |  |  |  |  |  |  |  |
| Expected Result | F | Column (Layout Sheet) |  |  |  |  |  |  |  |  |  |  |
| More Script Settings |  |  |  |  |  |  |  |  |  |  |  |  |
| Script Details Row | 4.0 | Row (Layout Sheet) |  |  |  |  |  |  |  |  |  |  |
| Steps Details Row | 5.0 | Row (Layout Sheet) |  |  |  |  |  |  |  |  |  |  |
| Default Step's BG Color |  | Cell BGColor |  |  |  |  |  |  |  |  |  |  |
| Default Step's Type | Istruzione | Text |  |  |  |  |  |  |  |  |  |  |
|  |  | Not Needed |  |  |  |  |  |  |  |  |  |  |
| QAC Data Source Settings |  |  |  |  |  |  |  |  |  |  |  |  |
| DSN Name | QADirector60 |  |  |  |  |  |  |  |  |  |  |  |
| Authentication |  |  |  |  |  |  |  |  |  |  |  |  |
| Username | testware |  |  |  |  |  |  |  |  |  |  |  |
| Password | *********** |  |  |  |  |  |  |  |  |  |  |  |
|  | AA |  |  |  |  |  |  |  |  |  |  |  |
|  | AB |  |  |  |  |  |  |  |  |  |  |  |
|  | AC |  |  |  |  |  |  |  |  |  |  |  |
|  | AD |  |  |  |  |  |  |  |  |  |  |  |

## Hidden Settings

|  |  |
| --- | --- |
| DSN Password | testware |

## Layout

| Layout predefinito Specifiche di Test per macro INSERT LAYOUT (definire il range di celle in Setting - Test Script Layout) |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ID caso di test | Suffisso Script di test | Nome Script di test
Tipo Step | Istruzioni | Descrizione | Risultati attesi | Versione | Stima tempo | N.cond. di test |
| TF.001 | 01 | Caso di test 1 |  | Descrizione |  | 1.0 |  |  |
|  | Step | Tipo | Istruzioni 
(text) | Dati di input
 (Associated Data) | Risultati attesi
 (Expected Result) |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | descrivere le precondizioni | i dati per le precondizioni | la verifica delle precondizioni |  |  |  |
|  | P | Stato Base | descrivere il posizionamento dell'applicazione | i dati necessari, esempio login | la verifica dello stato base |  |  |  |
|  | 1.0 | Navigazione | descrivere uno o più pasi di navigazione | i dati se presenti | il risultato al termine della navigazione |  |  |  |
|  | 2.0 | Azione | descrivere la/le azioni dell'utente | i dati utilizzati | i risultati al termine delle azioni |  |  |  |
|  | 3.0 | Navigazione | descrivere uno o più pasi di navigazione | i dati se presenti | il risultato al termine della navigazione |  |  |  |
|  | R1 | Riciclo Script | Indicare lo/gli step sul quale effettuare i cambiamenti e descrivere l'obiettivo del ricicli | i nuovi dati | i risultati al termine delle azioni |  |  |  |
|  | V | Verifica esterna | descrivere eventuali verifiche esterne da effettuare al termine del test per la verifica dello stesso | i dati se presenti | i risultati al termine delle verifiche |  |  |  |
| TF.001 | 01 | Catena di test 1 |  |  |  |  |  |  |
|  | Step | Tipo | Istruzioni 
(text) | Dati di input
 (Associated Data) | Risultati attesi
 (Expected Result) |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni |  |  |  |  |  |  |
|  | P | Stato Base |  |  |  |  |  |  |
|  | 1.0 | Navigazione |  |  |  |  |  |  |
|  | 2.0 | Azione |  |  |  |  |  |  |
|  | 3.0 | Navigazione |  |  |  |  |  |  |
|  | 4.0 | Link Test TF002.1 | Eseguire il test indicato variando le informazioni in input nel passo di inserimento | nuovo Input | nuovo outpiut |  |  |  |
|  | 5.0 | Link Test TF0014.4 | Eseguire il test indicato variando le informazioni in input nel passo di inserimento | in inserimento : nuovo Input
In variazione: nuovo input | nuovo outpiut |  |  |  |
|  | V | Verifica esterna |  |  |  |  |  |  |
| TF.001 | 01 | layout Checklist  1 |  |  |  |  |  |  |
|  | Step | Tipo Step | Istruzioni | Dati di input | Risultati attesi |  |  |  |
|  | P | Precondizioni |  |  |  |  |  |  |
|  | P | Stato Base |  |  |  |  |  |  |
|  | 1.0 | Navigazione |  |  |  |  |  |  |
|  | 2.0 | Azione |  |  |  |  |  |  |
|  | 3.0 | Navigazione |  |  |  |  |  |  |
|  | 4.0 | Check | Indicare la verifica da eseguire |  |  |  |  |  |
|  | 5.0 | Check | Indicare la verifica da eseguire |  |  |  |  |  |
|  | V | Verifica esterna |  |  |  |  |  |  |
| Standard variabile |  |  |  |  |  |  |  |  |
| ID caso di test | Suffisso Script di test | Nome Script di test |  | Descrizione |  | Versione | Stima tempo | N.cond. di test |
| TF.001 | 01 | Caso di test 1 |  |  |  |  |  |  |
|  | Step | Tipo | Istruzioni 
(text) | Dati di input
 (Associated Data) | Risultati attesi
 (Expected Result) |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | assente |  |  |  |  |  |
|  | P | Stato Base | assente |  |  |  |  |  |
|  | 1.0 | Navigazione / Azione |  |  |  |  |  |  |
|  | 2.0 | Navigazione / Azione |  |  |  |  |  |  |
|  | 3.0 | Navigazione / Azione |  |  |  |  |  |  |
|  | R1 | Riciclo step 2 | non codificato |  |  |  |  |  |
|  | V | Verifica esterna | non codificato |  |  |  |  |  |
| Progetto / Obiettivo Software |  |  |  |  |  |  |  |  |
| Identificativo documento |  |  |  |  |  |  |  |  |
| ID caso di test | Suffisso Script di test | Nome Script di test |  | Descrizione |  | Versione | Stima tempo | N.cond. di test |
|  | Step | Tipo | Istruzioni 
(text) | Dati di input
 (Associated Data) | Risultati attesi
 (Expected Result) |  |  |  |

## Validation Log

| [All.1Tab.test] Validation Failures |
| --- |

## ReqID_Table

| IsFTR | Level | ID | Description | ReqID | Risk | DisplayID |
| --- | --- | --- | --- | --- | --- | --- |

## Temp_Data_Out

| Lvl | Display ID | Req Type | Req Name (1) | Req Name (2) | Req Name (3) | Req Name (4) | Req Name (5) | Req Name (6) | Req Name (7) | Req Name (8) | Req Name (9) | Req Name (10) | Req Name (11) | Req Name (12) | Assigned To | Description | Status | Time Est. | Prior Internal Testing | Prior External Testing | Impact to Release | Maturity of Function | Complexity of Function | Usage Frequency | Defect Impact | External Testing Effort | Custom Factor 1 | Custom Factor 2 | Custom Factor 3 | Functional Area Risk Weight | Test Requirement Risk Weight | System Score | Intgr. Score | System Risk | Intgr. | Cyc 1 | Cyc 2 | Cyc 3 | Cyc 4 | Cyc 5 | Cyc 6 | Cyc 7 | Cyc 8 | Cyc 9 | Cyc 10 | Cyc 11 | Cyc 12 | Cyc 13 | Cyc 14 | Cyc 15 | Cyc 16 | Cyc 17 | Cyc 18 | Cyc 19 | Cyc 20 | Project ID | Folder ID | Req. ID | User ID |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |