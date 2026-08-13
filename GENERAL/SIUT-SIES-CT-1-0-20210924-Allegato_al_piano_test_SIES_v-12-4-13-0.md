---
uniqueName: siut-sies-ct-1-0-20210924-allegatoalpianotestsiesv
displayName: "SIUT SIES CT 1 0 20210924 Allegato al piano test SIES v 12 4 13 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-CT-1.0-20210924-Allegato_al_piano_test_SIES_v.12.4.13.0

> **File originale:** `RILASCIO_12.4.13.0/SIUT-SIES-CT-1.0-20210924-Allegato_al_piano_test_SIES_v.12.4.13.0.xls`  
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

|  |  |  |
| --- | --- | --- |
|  | Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A - Sirfin-PA nell’ambito del contratto CIG 73479643B7 per lo “SVILUPPO DEL SISTEMA INFORMATIVO UNITARIO TELEMATICO, LA MANUTENZIONE DEGLI ATTUALI SISTEMI DELL’AREA PENALE DEL MINISTERO DELLA GIUSTIZIA E SERVIZI CORRELATI LOTTO 1” |  |
|  | Nome del file | SIUT-SIES-CT-1.0-20210924-Allegato-al-piano-test_SIES_v.12.4.13.0.xls |
|  | Piano di test | SIUT-SIES-PT-1.0-20210924-Piano_dei_Test_SIES_v.12.4.13.0.docx |
|  | Versione | 1.0 |
|  | Data | 44463.0 |
|  | Intervento | SIES v.12.4.13.0 |
|  | Area Applicativa | Penale |
|  | Allegato al Piano dei Test |  |

## TabellaTest

| Codice Area |  |  | SIES v.12.4.13.0 |  |  |  | Codifica  Piano di test |  | SIUT-SIES-CT-1.0-20210924-Allegato-al-piano-test_SIES_v.12.4.13.0.xls | Versione | 1.0 |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Applicazione |  |  | Funzionalità / Requisiti non funzionali |  |  |  |  |  |  | Caso di test |  |  |  |  |  |  |  |  |  |  |
| Codice Area | Codice Appl. | ID. Requisito | ID | Primo livello | ID | Primo Livello | Risk (1-5) | ID | Secondo livello | ID | Nome del caso di test | Classe di Gravità (1-4) | Ciclo di test | Stima Durata | Descrizione e note | Versione | N. cond. di test | Autom. | Classe di rilevanza (A, B, C) | Esito |
| SIUT | SIES | 20210702015.0 |  |  | 20210702015.0 | Errore - nella visualizzazione del provvedimento di cumulo su procedimento trasferito da altro Distretto |  | SIEP | SIEP - Errore - nella visualizzazione del provvedimento di cumulo su procedimento trasferito da altro Distretto | TF001.SIEP | Verifica corretta  visualizzazione del provvedimento di cumulo su procedimento  trasferito da altro  Distretto. |  |  |  | Verifica: verificare che vengano trasferiti correttamente tutti i dati del fascicolo tra cui i dati dell'istruttoria cumulo di un fascicolo proveniente da altro Distretto. | 1.0 |  |  |  |  |
| SIUT | SIES | 20210716016.0 |  |  | 20210716016.0 | Appello contro provvedimento su misura sicurezza (art 680) Mancato aggiornamento Misura sicurezza - La problematica è presente su tutte le tipologie di misure |  | SIEP | SIEP - Appello contro provvedimento su misura sicurezza (art 680) Mancato aggiornamento Misura sicurezza - La problematica è presente su tutte le tipologie di misure | TF002.SIEP | Verifica elaborazione template corretto |  |  |  | Verifica: verificare che nel caso di appello contro provvedimento su misura sicurezza (art 680)  il sistema elabori il documento corretto | 1.0 |  |  |  |  |
| SIUT | SIES | 20210721013.0 |  |  | 20210721013.0 | SIES -  Correzione Template SIEP_LS_OLQSI - notifiche al difensore |  | SIEP | SIEP - SIES -  Correzione Template SIEP_LS_OLQSI - notifiche al difensore | TF003.SIEP | Verifica template  SIEP_LS_OLQSI |  |  |  | Verifica: verificare che il template  SIEP_LS_OLQSI contenga le modifiche richieste nel ticket (eliminazione spazi, revisione punti elenco, eliminazione frase ripetuta ecc) | 1.0 |  |  |  |  |
| SIUT | SIES | 202107210117.0 |  |  | 202107210117.0 | Impossibilità traferimento richiesta al Magistrato di Sorv. Min. |  | SIEP | SIEP - Impossibilità traferimento richiesta al Magistrato di Sorv. Min. | TF004.SIEP | Verifica corretta trasmissione richiesta al Magistrato di Sorveglianza dei Minori |  |  |  | Verifica: verificare che la richiesta di trasmissione di un procedimento al Magistrato di Sorveglianza dei Minorenni avvenga correttamente e che sia anche riportata correttamente nella stampa SIEP_MA_TRASF_ATTI_51BIS. | 1.0 |  |  |  |  |
| SIUT | SIES | 20210728014.0 |  |  | 20210728014.0 | anomalia inserimento collegio sige - Cap |  | SIGE | SIGE - anomalia inserimento collegio sige - Cap | TF005.SIGE | Verifica corretto inserimento collegio in un procedimento SIGE |  |  |  | Verifica: verificare che in un procedimento SIGE nell'emissione di un'ordinanza l'inserimento di un collegio di Magistrati non vada in errore | 1.0 |  |  |  |  |
| SIUT | SIES | 20210824013.0 |  |  | 20210824013.0 | Emissione Cumulo |  | SIEP | SIEP - Emissione Cumulo | TF006.SIEP | Verifica corretta emissione del provvedimento di cumulo |  |  |  | Verifica: verificare che in presenza di una richiesta di Revoca Beneficio su un evento in cui è assente il numero di provvedimento sia possibile emettere il relativo provvedimento di cumulo. | 1.0 |  |  |  |  |
| SIUT | SIES | 20210825016.0 |  |  | 20210825016.0 | foglio completare Iscrizione nel casellario giudiziale locale - ex art. 3 DPR 14 novembre 2002 n. 313 - |  | SIEP | SIEP - foglio completare Iscrizione nel casellario giudiziale locale - ex art. 3 DPR 14 novembre 2002 n. 313 - | TF007.SIEP | Verifica corretto trasferimento da SIES ad NSC di una sentenza con impugnazione di primo grado. |  |  |  | Verifica: verificare che l'invio da SIES ad NSC di una sentenza con una impugnazione di primo grado di inammissibiltà avvenga correttamente. | 1.0 |  |  |  |  |
| SIUT | SIES | 20210907019.0 |  |  | 20210907019.0 | CORREZIONE IMPORT ESECUZIONE MISURA SICUREZZA |  | SIEP | SIEP - CORREZIONE IMPORT ESECUZIONE MISURA SICUREZZA | TF008.SIEP | Verifica corretta modifica import EsecuzioneMisuraSicurezza.rtf |  |  |  | Verifica: verificare che il contenuto della stampa riporti le modifiche segnalate nel ticket | 1.0 |  |  |  |  |
| SIUT | SIES | 20210916015.0 |  |  | 20210916015.0 | Correzione template SIEP_RICH_GENERICA Autorità destinataria indirizzo |  | SIEP | SIEP - Correzione template SIEP_RICH_GENERICA Autorità destinataria indirizzo | TF009.SIEP | Verifica visualizzazione indirizzo in stampa |  |  |  | Verifica: verificare che la stampa SIEP_RICH_GENERICA riporti l'indirizzo dell'Autorità destinataria. | 1.0 |  |  |  |  |
| SIUT | SIES | 20210916011.0 |  |  | 20210916011.0 | CORREZIONE TEMPLATE SIEP_OS_LARAL |  | SIEP | SIEP - CORREZIONE TEMPLATE SIEP_OS_LARAL | TF010.SIEP | Verifica visualizzazione in stampa della dicitura corretta. |  |  |  | Verifica: verificare che la stampa SIEP_OS_LARAL riporti la dicitura corretta per l'Ufficio Servizi Sociali per i Minorenni. | 1.0 |  |  |  |  |

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

| Progetto / Obiettivo Software |  |  | SIES v.12.4.13.0 |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | SIUT-SIES-CT-1.0-20210924-Allegato-al-piano-test_SIES_v.12.4.13.0.xls |  |  |  |  |  |  |
| ID caso di test | Suffisso Caso di test | Nome Caso di test
Tipo Step |  | Descrizione |  | Versione | Stima tempo | N.cond. di test | Esito |
| TF001.SIEP | 01 | Verifica corretta  visualizzazione del provvedimento di cumulo su procedimento  trasferito da altro  Distretto. |  | Verifica: verificare che vengano trasferiti correttamente tutti i dati del fascicolo tra cui i dati dell'istruttoria cumulo di un fascicolo proveniente da altro Distretto. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Tramite l'apposita icona posta in alto 'Ricerca Istruttorie Cumulo', ricercare un fascicolo SIEP con istruttoria cumulo chiusa. |  |  |  |  |  |  |
|  | 2 | Azione | L'utente effettua l'accesso al sistema SIEP da altro Distretto come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | 3 | Azione | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 4 | Navigazione | Ricerche |  |  |  |  |  |  |
|  | 5 | Azione | Selezionare Procedimento |  | Visualizzazione pagina Ricerca Procedimento |  |  |  |  |
|  | 6 | Azione | Indicare gli estremi del procedimento e dell'ufficio dello step 1. Cliccare su Ricerca |  | Visualizzazione messaggio 'Richiesta di ricerca Procedimento sottomessa al Sistema! ' |  |  |  |  |
|  | 7 | Azione | Cliccare sul pulsante OK del messaggio |  | Visualizzazione pagina Dettaglio Procedimento da Trasferire |  |  |  |  |
|  | 8 | Navigazione | Ricerche |  |  |  |  |  |  |
|  | 9 | Azione | Cliccare su Esiti Ricerche Procedimenti |  | Visualizzazione pagina  Esiti Ricerca Fascicolo SIEP da altre BDI |  |  |  |  |
|  | 10 | Azione | Ricercare il procedimento dello step 1 |  | Visualizzazione pagina Elenco Esiti Ricerca Fascicolo SIEP altre BDI |  |  |  |  |
|  | 11 | Azione | avviare la ricerca e procedere alla presa in carico. |  |  |  |  |  |  |
|  | 12 | Azione | Dalla lista compare sul primo rigo la richiesta con esito ELEMENTO TROVATO, selezionare il dettaglio e quindi "Conferma Trasferimento Procedimento" |  | Visualizazzione pagina Dettaglio Trasferimento Procedimento da Altra BDI |  |  |  |  |
|  | V | Verifica | Verificare che nella parte finale del dettaglio del trasferimento siano presenti i record relativi all'istruttoria cumulo per esempio Inserimento Istruttoria_Cumulo con esito Positivo. |  |  |  |  |  |  |
|  | 13 | Azione | Nella stessa form cliccare sul link posto in alto e relativo all' Anno/Num procedimento. |  | Visualizzazione pagina Dettaglio Procedimento |  |  |  |  |
|  | 14 | Azione | Dalla combo delle funzioni selezionare  Elenco Provvedimenti PM |  | Visualizzazione pagina  Elenco Provvedimenti PM |  |  |  |  |
|  | 15 | Azione | Dalla lista selezionare il dettaglio del provvedimento di Unificazione |  |  |  |  |  |  |
|  | V | Verifica | Verificare che il provvedimento di cumulo venga visualizzato correttamente. |  |  |  |  |  |  |
| TF002.SIEP | 01 | Verifica elaborazione template corretto |  | Verifica: verificare che nel caso di appello contro provvedimento su misura sicurezza (art 680)  il sistema elabori il documento corretto |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Ricercare un procedimento di classe 4 Validato e con posizione giuridica 'Libero' avente
misura di sicurezza: 'Espulsione dal territotio dello stato' ;
il Magistrato Assegnatario;
il difensore. |  | Visualizzazione pagina Dettaglio Procedimento |  |  |  |  |
|  | 2 | Azione | L'utente effettua l'accesso al sistema SIUS come Tribunale di Sorveglianza | Dxxxxx (Tribunale di Sorveglianza) |  |  |  |  |  |
|  | 3 | Azione | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 4 | Navigazione | Iscrizione Manuale » Ricerca Titolo Esecutivo per Numero SIEP |  | Visualizzazione pagina Ricerca Titolo Esecutivo |  |  |  |  |
|  | 5 | Azione | Ricercare il procedimento dello step 1 |  | Visualizzazione pagina Dettaglio Procedimento |  |  |  |  |
|  | 6 | Azione | Selezionare dalla combo delle funzionalità Iscrizione procedimento |  | Visualizzazione pagina Iscrizione Procedimento |  |  |  |  |
|  | 7 | Azione | Valorizzare 
Tipo Atto = Istanza;
Contenuto = Appello contro provvedimento su misura di sicurezza (art.680cpp);
Oggetto= Impugnazionecontro provvedimento MdS;
Data arrivo in cancelleria.
Cliccare su Conferma |  | Visualizzazione pagina Dettaglio Procedimento SIUS |  |  |  |  |
|  | 8 | Azione | Cliccare sul link Dettaglio Misure Sicurezza |  | Visualizzazione pagina Elenco Misure Sicurezza |  |  |  |  |
|  | 9 | Azione | Cliccare sull'icona di Inserimento Misura Sicurezza |  | Visualizzazione pagina   Inserimento Misura Sicurezza |  |  |  |  |
|  | 10 | Azione | Valorizzare:
Natura Misura: Non detentiva;
Tipo misura: Espulsione dal territorio dello stato;
Durata misura;
Riferimento Titolo esecutivo.
Cliccare su Conferma. |  | Visualizzazione pagina Dettaglio Misura Sicurezza |  |  |  |  |
|  | 11 | Navigazione | Udienza » Prefissazione Udienza |  | Visualizzazione pagina Prefissazione Udienza |  |  |  |  |
|  | 12 | Azione | Inserire la data udienza e confermare |  | Visualizzazione pagina Prefissazione Udienza |  |  |  |  |
|  | 13 | Navigazione | Ordinanze » Emissione Ordina |  | Visualizzazione pagina Emissione Ordinanza |  |  |  |  |
|  | 14 | Azione | Inserire Data Emissione e confermare |  | Visualizzazione pagina Emissione Ordinanza Appello Contro Provvedimento su Misura Sicurezza |  |  |  |  |
|  | 15 | Azione | Valorizzare:
Oggetto: Impugnazione contro provvedimento MdS;
Esito: Accoglie appello e modifica MdS;
Nuova Misura: Libertà vigilata;
Durata.
Confermare. |  | Visualizzazione pagina Dettaglio Ordinanza |  |  |  |  |
|  | 16 | Azione | Stampare e Validare |  |  |  |  |  |  |
|  | 17 | Navigazione | Ordinanze » Deposito Ordinanza |  | Visualizzazione pagina Deposito Ordinanza SIUS  del gg/mm/aaaa |  |  |  |  |
|  | 18 | Azione | Depositare l'ordinanza.
Confermare |  | Visualizzazione pagina Dettaglio Deposito Ordinanza |  |  |  |  |
|  | 19 | Azione | Stampare e validare |  | Visualizazione pagina Dettaglio Deposito Ordinanza |  |  |  |  |
|  | 20 | Azione | Cliccare sull'icona Trasferisci |  | Visualizzazione pagina Trasferimento Ordinanza |  |  |  |  |
|  | 21 | Azione | Cliccare su conferma |  | Visualizzazione messaggio Trasmissione Ordinanza sottomessa al Sistema! |  |  |  |  |
|  | 22 | Azione | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | 23 | Azione | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 24 | Azione | Ricercare ilprocedimento dello step 1 |  | Visualizzazione pagina Dettaglio Procedimento |  |  |  |  |
|  | 25 | Navigazione | Gestione Misure Sicurezza |  | Visualizzazione pagina Gestione Misure Sicurezza |  |  |  |  |
|  | 26 | Azione | Cliccare su Annotazione Decisione della sorveglianza |  | Visualizzazione pagina Annotazione Decisione della sorveglianza |  |  |  |  |
|  | 27 | Azione | Inserire la data di ricezione , selezionare il provvedimento e cliccare su Conferma |  | Visualizzazione pagina Dettaglio Annotazione Decisione della Sorveglianza |  |  |  |  |
|  | 28 | Azione | Validare |  | Visualizazzione pagina Dettaglio Annotazione Decisione della Sorveglianza |  |  |  |  |
|  | 29 | Azione | Cliccare su Comunicazione |  | Visualizzazione pagina Comunicazione per esecuzione Misure di Sicurezza |  |  |  |  |
|  | 30 | Azione | Inserire Data Emissione , un destinatario e confermare |  | Visualizzazione pagina Dettaglio Comunicazione per Esecuzione Misure di Sicurezza |  |  |  |  |
|  | 31 | Azione | Cliccare sull'icona di stampa |  | Generazione stampa |  |  |  |  |
|  | V | Verifica | Verificare che venga agganciato il template corretto ovvero SIEP_MS_FS_COMUPOL_LIB_NOD.rtf |  |  |  |  |  |  |
| TF003.SIEP | 01 | Verifica template  SIEP_LS_OLQSI |  | Verifica: verificare che il template  SIEP_LS_OLQSI contenga le modifiche richieste nel ticket (eliminazione spazi, revisione punti elenco, eliminazione frase ripetuta ecc) |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Ricercare un procedimento con Posizione Giuridica 'libero', su cui è presente una istanza di Concessione Misure Alternative alla Detenzione (art.678 comma 1 ter cpp). |  | Visualizzazione pagina Dettaglio Procedimento |  |  |  |  |
|  | 2 | Navigazione | Ordini
 di Esecuzione/Scarcerazione »
Sospensione Esecuzione ex art. 656 c.p.p.
» Ordine
 di Esecuzione |  | Visualizzazione pagina Ordine di Esecuzione con sospensione (LEGGE 165/98) - CONDANNATO Libero |  |  |  |  |
|  | 3 | Azione | Compilare i campi della form, impostando in particolare:
Notifica al Condannato - Autorità di destinazione : Carabinieri 
Notifica al difensore - Autorità di destinazione : Notifica ai sensi dell'art.148 comma 2bis cpp 
Cliccare su Conferma |  | Visualizzazione pagina  Dettaglio Legge Simeone Libero Istanza Prodotta |  |  |  |  |
|  | 4 | Azione | Cliccare sull'icona di stampa |  | Generazione stampa SIEP_LS_OLQSI |  |  |  |  |
|  | V | Verifica | Verificare che il contenuto della stampa riporti le modifiche segnalate nel ticket |  |  |  |  |  |  |
|  | R1 | Riciclo Test | Ripetere gli step da 1  e 2 |  |  |  |  |  |  |
|  | 5 | Azione | Compilare i campi della form, impostando in particolare:
Notifica al Condannato - Autorità di destinazione : Carabinieri 
Notifica al difensore - Autorità di destinazione : UNEP
Cliccare su Conferma |  | Visualizzazione pagina  Dettaglio Legge Simeone Libero Istanza Prodotta |  |  |  |  |
|  | 6 | Azione | Cliccare sull'icona di stampa |  | Generazione stampa SIEP_LS_OLQSI |  |  |  |  |
|  | V | Verifica | Verificare che il contenuto della stampa riporti le modifiche segnalate nel ticket |  |  |  |  |  |  |
| TF004.SIEP | 01 | Verifica corretta trasmissione richiesta al Magistrato di Sorveglianza dei Minori |  | Verifica: verificare che la richiesta di trasmissione di un procedimento al Magistrato di Sorveglianza dei Minorenni avvenga correttamente e che sia anche riportata correttamente nella stampa SIEP_MA_TRASF_ATTI_51BIS. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale per i Minorenni | Bxxxxx (Procura della Repubblica Presso il Tribunale per i Minorenni) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Ricercare un procedimento di un soggetto con posizione giuridica 'Libero', su cui è sopravvenuto  un nuovo titolo di esecuzione di altra pena detentiva. |  | Visualizzazione pagina Dettaglio Procedimento |  |  |  |  |
|  | 2 | Navigazione | Istruttorie/Richieste >> Trasmissione Atti / Richieste ex art. 51 bis |  | Visualizzazione pagina TRASMISSIONE ATTI |  |  |  |  |
|  | 3 | Azione | Inserire:
Tipologia Atto: Trasmissione;
Oggetto: Richiesta prosecuzione della Misura Alternativa in corso ex art. 51 bis;
Firmatario: Magistrato;
Magistrato di Sorveglianza: Magistrato di Sorveglianza per i Minorenni.
Cliccare su Conferma. |  | Visualizzazione pagina  Dettaglio Richiesta/Comunicazione |  |  |  |  |
|  | 4 | Azione | Cliccare sull'icona di Stampa |  | Generazione stampa SIEP_MA_TRASF_ATTI_51BIS |  |  |  |  |
|  | V | Verifica | Verificare che la stampa contenga nella sezione MANDA la corretta descrizione dell'Ufficio a cui deve essere trasmesso il procedimento. |  |  |  |  |  |  |
|  | 5 | Azione | Validare. |  | Visualizzazione messaggio Aggiornamento Documento Avvenuto Correttamente! |  |  |  |  |
|  | 6 | Azione | Nella pagina Dettaglio Richiesta/Comunicazione cliccare sull'icona Trasferisci |  | Visualizzazione pagina  Trasferimento Atti - Richiesta prosecuzione della Misura Alternativa in corso ex art. 51 bis Legge 26.7.1975 n. 354 e s.m.i. |  |  |  |  |
|  | 7 | Azione | Cliccare su Conferma Trasmissione |  |  |  |  |  |  |
|  | V | Verifica | Verificare che la Trasmissione del procedimento sia avvenuta correttamente |  |  |  |  |  |  |
| TF005.SIGE | 01 | Verifica corretto inserimento collegio in un procedimento SIGE |  | Verifica: verificare che in un procedimento SIGE nell'emissione di un'ordinanza l'inserimento di un collegio di Magistrati non vada in errore |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIGE come Corte d'Appello | Kxxxxx (Corte d'Appello) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Navigazione | Ricerche » Procedimento SIGE per Estremi Atto |  | Visualizzazione pagina Ricerca Procedimento SIGE per Estremi Atto |  |  |  |  |
|  | 2 | Azione | Ricercare un procedimento Sige impostando
Tipo Rito ='Collegiale' 
Stato Procedimento = 'Solo pendenti'.
Indicare una Data Fine Pendenza
Cliccare su Ricerca |  | Visualizzazione pagina Ricerca Procedimento SIGE per Estremi Atto |  |  |  |  |
|  | 3 | Azione | Selezionare dall'elenco risultante un procedimento con Data Udienza valorizzata. |  | Visualizzazione pagina Dettaglio Procedimento SIGE |  |  |  |  |
|  | 4 | Navigazione | Funzioni Amministrative » Gestione Collegi » Ricerca Collegio |  | Visualizzazione pagina Ricerca Collegio |  |  |  |  |
|  | 5 | Azione | Ricercare dei collegi inserendo un intervallo di date udienze con estremi la data udienza indicata nel decreto Fissazione Udienza presente nel Dettaglio del Procedimento SIGE individuato nello step 3 e, per esempio, la data di sistema. |  | Visualizzazione pagina Elenco Collegi |  |  |  |  |
|  | 6 | Azione | Individuare dall'elenco il collegio di interesse e verificare che l'idcollegio (escludendo le ultime 6 cifre numeriche) sia maggiore di 2147. In caso affermativo passare allo step successivo. In caso negativo accedere al DB e modificarne il valore (dove presente) nelle seguenti entità COLLEGIO, COLLEGIO_ESPERTO, COLLEGIO_GIUDICE_POPOLARE, COLLEGIO_MAGISTRATO |  |  |  |  |  |  |
|  | 7 | Navigazione | Ordinanze/Deposito/Notifiche » Emissione Ordinanza |  | Visualizzazione pagina Emissione Ordinanza |  |  |  |  |
|  | 8 | Azione | Cliccare sul link 'Inserimento Udienza - Visualizza Collegio' |  | Visualizzazione pop-up Dettaglio Udienza Collegiale |  |  |  |  |
|  | 9 | Azione | Cliccare sull'icona di Modifica |  | Visualizzazione pop-up Modifica Udienza Collegiale |  |  |  |  |
|  | 10 | Azione | Inserire i giudici del collegio. Cliccare su Conferma. |  |  |  |  |  |  |
|  | V | Verifica | Verificare che non venga visualizzato l'errore segnalato. |  |  |  |  |  |  |
| TF006.SIEP | 01 | Verifica corretta emissione del provvedimento di cumulo |  | Verifica: verificare che in presenza di una richiesta di Revoca Beneficio su un evento in cui è assente il numero di provvedimento sia possibile emettere il relativo provvedimento di cumulo. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Selezionare l'icona 'Ricerca Istruttorie Cumulo' presente in alto |  | Visualizzazione pagina Ricerca Istruttoria Cumulo |  |  |  |  |
|  | 2 | Azione | Ricercare un'istruttoria di cumulo in stato aperta |  | Visualizzazione pagina  Gestione Cumulo |  |  |  |  |
|  | 3 | Azione | Selezionare il link Elenco Titoli Coinvolti |  | Visualizzazione pagina  Elenco Provvedimenti Esecutivi Coinvolti |  |  |  |  |
|  | 4 | Azione | Selezionare il dettaglio di un titolo |  | Visualizzazione pagina Gestione Dati Analitici |  |  |  |  |
|  | 5 | Azione | Cliccare sul pulsante "Attività del GE" |  | Visualizzazione pagina Gestione Dati Analitici |  |  |  |  |
|  | 6 | Azione | Cliccare su Amnistia-Indulto |  | Visualizzazione pagina  Elenco Provvedimenti di Amnistia / Indulto |  |  |  |  |
|  | 7 | Azione | Cliccare su Inserisci Nuovo Provvedimento |  | Visualizzazione pagina  Inserimento annotazione Amnistia/Indulto |  |  |  |  |
|  | 8 | Azione | Inserire i dati tra cui risultano obbligatori Anno e Numero Procedimento SIGE. Confermare. |  | Visualizzazione pagina Dettaglio Annotazione Amnistia / Indulto |  |  |  |  |
|  | 9 | Azione | Ritornare sulla Griglia dell'istruttoria (Gestione Cumulo) e selezionare la voce "Richieste del PM" |  | Visualizzazione pagina  Richieste del PM |  |  |  |  |
|  | 10 | Azione | Selezionare Richieste al Giudice Dell'esecuzione |  | Visualizzazione pagina Richieste del PM al GE |  |  |  |  |
|  | 11 | Azione | Selezionare Richiesta revoca benefici |  | Visualizzazion epagina Richieste al G.E. Revoca Benefici |  |  |  |  |
|  | 12 | Azione | Selezionare il check in corrispondenza della voce "Indulto (P)" e confermare. |  | Visualizzazione pagina  Inserimento Richiesta Revoca Beneficio |  |  |  |  |
|  | 13 | Azione | Selezionare il link "Revocato in relazione al Titolo Esecutivo" |  | Visualizzazione pop-pup Elenco Titoli associati all'Istruttoria |  |  |  |  |
|  | 14 | Azione | Selezionare un titolo |  | Visualizzazione pagina  Inserimento Richiesta Revoca Beneficio |  |  |  |  |
|  | 15 | Azione | Completare i dati con i quantum revocati indicando il segno + nella selezione. Confermare. |  | Visualizzazione pagina  Dettaglio Richiesta Revoca Benefici |  |  |  |  |
|  | 16 | Azione | Tornare alla griglia dell'istruttoria (Gestione Cumulo) e selezionare uno dei 2 tasti dei "Prospetti" per generare la stampa. |  | Generazione stampa |  |  |  |  |
|  | V | Verifica | Verificare che la generazione della stampa non vada in errore. 
Attenzione! L'errore si verificava solo se "Anno e Numero Procedimento SIGE" non erano valorizzati. In form sono obbligatori ma i dati pregressi possono essere null. Per effettuare il test andrebbero messi a null sul DB. |  |  |  |  |  |  |
| TF007.SIEP | 01 | Verifica corretto trasferimento da SIES ad NSC di una sentenza con impugnazione di primo grado. |  | Verifica: verificare che l'invio da SIES ad NSC di una sentenza con una impugnazione di primo grado di inammissibiltà avvenga correttamente. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Navigazione | Iscrizione » Soggetto |  | Visualizzazione pagina Iscrizione Soggetto |  |  |  |  |
|  | 2 | Azione | Iscrivere i dati di un soggetto e confermare. |  | Visualizzazione pagina Dettaglio Soggetto |  |  |  |  |
|  | 3 | Azione | Selezionare dalla combo delle funzioni Iscrizione Sentenza e cliccare sulla lente |  | Visualizzazione pagina  Inserimento Sentenza |  |  |  |  |
|  | 4 | Azione | Iscrivere una sentenza (a carico di un soggetto) contenente una impugnazione di primo grado ed avente nella sezione "Altro grado di giudizio" un tipo provvedimento pari a "Ordinanza di inammissibilità". Confermare. |  | Visualizzazione pagina Dettaglio Sentenza |  |  |  |  |
|  | 5 | Azione | Selezionare dalla combo delle funzioni assegnazione N. SIEP e cliccare sulla lente |  | Visualizzazione pagina Inserimento Procedimento |  |  |  |  |
|  | 6 | Azione | Inserire i dati richiesti e confermare |  | Visualizzazione pagina Dettaglio Procedimento |  |  |  |  |
|  | 7 | Navigazione | Validazione Procedimento |  |  |  |  |  |  |
|  | 8 | Azione | Validare il procedimento SIEP dopo aver inserito la Pena complessiva, il Magistrato assegnatario, il reato. |  | Visualizzazione pagina Dettaglio Procedimento |  |  |  |  |
|  | 9 | Azione | Inviare il procedimento provvisoriamente ad NSC usanto l'apposita icona "Trasferimento Provvedimento da SIES ad NSC". |  |  |  |  |  |  |
|  | V | Verifica | Verificare che il trasferimento ad NSC avvenga correttamente. |  |  |  |  |  |  |
| TF008.SIEP | 01 | Verifica corretta modifica import EsecuzioneMisuraSicurezza.rtf |  | Verifica: verificare che il contenuto della stampa riporti le modifiche segnalate nel ticket |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Ricercare un procedimento con Posizione Giuridica 'Espiazione Pena in Regime di Affidamento in prova', su cui siano presenti almeno due Misure di Sicurezza. |  | Visualizzazione pagina Dettaglio Procedimento |  |  |  |  |
|  | 2 | Navigazione | Decisioni Sorveglianza |  | Visualizzazione pagina Decisioni Sorveglianza |  |  |  |  |
|  | 3 | Azione | Selezionare Liberazione Anticipata |  | Visualizzazione pagina Emissione Ordinanza di Liberazione Anticipata |  |  |  |  |
|  | 4 | Azione | Compilare i campi della form, concedendo almeno 45 gg di L.A. e confermare |  | Visualizzazione pagina Dettaglio Liberazione Anticipata |  |  |  |  |
|  | 5 | Azione | Continuare con il flusso proposto dal sistema (Calcolo Data Fine Pena, Ordine di scarcerazione, fino alla form di Dettaglio dell’OS |  | Visualizazione pagina Dettaglio Ordine di Scarcerazione in regime alternativo |  |  |  |  |
|  | 6 | Azione | Cliccare sull'icona di stampa |  | Generazione documento di stampa |  |  |  |  |
|  | V | Verifica | Verificare che il contenuto della stampa, relativo alle Misure Sicurezza, riporti le modifiche segnalate nel ticket |  |  |  |  |  |  |
| TF009.SIEP | 01 | Verifica visualizzazione indirizzo in stampa |  | Verifica: verificare che la stampa SIEP_RICH_GENERICA riporti l'indirizzo dell'Autorità destinataria. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Ricercare un fascicolo qualunque purché non archiviato. |  | Visualizzazione pagina Dettaglio Procedimento |  |  |  |  |
|  | 2 | Navigazione | Istruttorie/Richieste |  | Visualizzazione pagina Istruttorie/Richieste |  |  |  |  |
|  | 3 | Azione | Selezionare  RICHIESTA/COMUNICAZIONE |  | Visualizzazione pagina  RICHIESTA/COMUNICAZIONE |  |  |  |  |
|  | 4 | Azione | Nella combo "Tipologia Atto"  selezionare "Richiesta". 
Nella combo "Oggetto Atto" selezionare "Restituzione Ordine di Esecuzione". 
Compilare come destinatari gli ultimi 3 campi: "Altro Destinatario", "Sede" e "Indirizzo". 
Confermare |  | Visualizzazione pagina Dettaglio Richiesta/Comunicazione |  |  |  |  |
|  | 5 | Azione | Cliccare sull'icona di stampa. |  | Generazione documento Siep_rich_generica.rtf |  |  |  |  |
|  | V | Verifica | Verificare che sulla stampa venga riportato anche l'indirizzo. |  |  |  |  |  |  |
| TF010.SIEP | 01 | Verifica visualizzazione in stampa della dicitura corretta. |  | Verifica: verificare che la stampa SIEP_OS_LARAL riporti la dicitura corretta per l'Ufficio Servizi Sociali per i Minorenni. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Ricercare un fascicolo con soggetto in espiazione pena in regime di misura alternativa (per esempio Affidamento in Prova) |  | Visualizzazione pagina Dettaglio Procedimento |  |  |  |  |
|  | 2 | Navigazione | Decisioni Sorveglianza |  | Visualizzazione pagina  Decisioni Sorveglianza |  |  |  |  |
|  | 3 | Azione | Selezionare Liberazione anticipata |  | Visualizzazione pagina Emissione Ordinanza di Liberazione Anticipata |  |  |  |  |
|  | 4 | Azione | Compilare i campi della form e confermare. |  | Visualizzazione pagina Dettaglio Liberazione Anticipata |  |  |  |  |
|  | 5 | Azione | Selezionare il pulsante "Calcola Data Fine Pena". |  | Visualizzazione pagina Emissione Ordine di Scarcerazione a seguito di ordinanza Liberazione Anticipata in regime alternativo - Espiazione Pena in Regime di Affidamento in Prova |  |  |  |  |
|  | 6 | Azione | Compilare i campi della form indicando come primo destinatario USSM nella combo. Confermare. |  | Visualizazzione pagina Dettaglio Ordine di Scarcerazione in regime alternativo |  |  |  |  |
|  | 7 | Azione | Cliccare sull'icona di stampa. |  | Generazione documento SIEP_OS_LARAL.rtf |  |  |  |  |
|  | V | Verifica | Verificare che sulla stampa nella sezione MANDA compaia la scritta "All’U.S.S.M. (Ufficio Servizi Sociali per i Minorenni) competente" |  |  |  |  |  |  |

## VerificheConformità

| Progetto / Obiettivo Software |  |  |  | Intervento |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  |  | 23 |  |  |
| ID | Tipo Verifica | Attributo | Indicatore | Descrizione tipo Verifica | Esito Verifica Fornitore | Esito Verifica Amministrazione |

## SogliaAccettazione

| Progetto / Obiettivo Software |  |  | Intervento |  |  |  |
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