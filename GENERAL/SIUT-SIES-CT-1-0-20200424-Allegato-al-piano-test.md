---
uniqueName: siut-sies-ct-1-0-20200424-allegato-al-piano-test
displayName: "SIUT SIES CT 1 0 20200424 Allegato al piano test"
category: "GENERAL"
tags: []
---

# SIUT-SIES-CT-1.0-20200424-Allegato-al-piano-test

> **File originale:** `RILASCIO_12.2.0/SIUT-SIES-CT-1.0-20200424-Allegato-al-piano-test.xls`  
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
|  | SIUT-SIES-CT-1.0-20200424-Allegato-al-piano-test.xls |
|  | Piano di test |
|  | Ver. 1.0 |
|  | Data: 24/04/2020 |
|  | SIUT |
|  | SIES 12.2.0 |
|  | Allegato al Piano dei Test |

## TabellaTest

| Codice Area |  |  | SIUT |  |  |  | Codifica  Piano di test |  | SIUT-SIES-CT-1.0-20200424-Allegato-al-piano-test.xls | Versione | Ver. 1.0 |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Applicazione |  |  | Funzionalità / Requisiti non funzionali |  |  |  |  |  |  | Caso di test |  |  |  |  |  |  |  |  |  |  |
| Codice Area | Codice Appl. | ID. Requisito | ID | Primo livello | ID | Primo Livello | Risk (1-5) | ID | Secondo livello | ID | Nome del caso di test | Classe di Gravità (1-4) | Ciclo di test | Stima Durata | Descrizione e note | Versione | N. cond. di test | Autom. | Classe di rilevanza (A, B, C) | Esito |
| SIUT | SIES | 20200220015.0 |  |  | 20200220015.0 | Cumulo su procedimento archiviato |  | SIEP | SIEP - Cumulo su procedimento archiviato | TF001.SIEP | Verifica Cumulo su procedimento archiviato |  |  |  | Verifica: verificare che nel caso di cumulo su procedimento archiviato il sistema non blocchi l'emissione di qualsiasi altro provvedimento | 1.0 |  |  |  |  |
| SIUT | SIES | 20200220017.0 |  |  | 20200220017.0 | Provvedimento di cumulo comunicazioni non validate |  | SIEP | SIEP - Provvedimento di cumulo comunicazioni non validate | TF002.SIEP | Verifica Provvedimento di cumulo comunicazioni non validate |  |  |  | Verifica: verificare che il messaggio che segnala all'utente che esiste un provvedimento non validato contenga come info la tipologia e la data di inserimento dell'evento | 1.0 |  |  |  |  |
| SIUT | SIES | 20200224011 |  |  | 20200224011 | SIUS - errore F3 stampa certificato esecuzione |  | SIUS | SIUS - SIUS - errore F3 stampa certificato esecuzione | TF003.SIUS | Verifica SIUS - errore F3 stampa certificato esecuzione |  |  |  | Verifica: verificare che venga prodotta la stampa del certificato esecuzione | 1.0 |  |  |  |  |
| SIUT | SIES | 20200220018.0 |  |  | 20200220018.0 | Cumulo con ergastolo. Template e calcolo pena |  | SIEP | SIEP - Cumulo con ergastolo. Template e calcolo pena | TF004.SIEP | Verifica Cumulo con ergastolo. Template e calcolo pena |  |  |  | Verifica: verificare che nel caso di pena irrogata con sentenza di cumulo il sistema nel calcolo e nei template non riporti la pena dell’ergastolo, determinata in cumulo, ma la sola pena temporanea. | 1.0 |  |  |  |  |
| SIUT | SIES | 20200220016.0 |  |  | 20200220016 | Errore assegnazione stato procedimento |  | SIEP | SIEP - Errore assegnazione stato procedimento | TF005.SIEP | Verifica Errore assegnazione stato procedimento |  |  |  | Verifica: verificare che lo stato del fascicolo dopo l'inserimento del Verbale Vane Ricerche deve essere modificato dall'applicativo in 'Emesso Ordine di Esecuzione con Arresto Il dd-MM-yyyy - Verbale Vane Ricerche del : dd-MM-yyyy' | 1.0 |  |  |  |  |
| SIUT | SIES | 20200226013.0 |  |  | 20200226013.0 | SIGE - ricerca omonimi (vedi anche ticket 20200218019 Catania) |  | SIGE | SIGE - SIGE - ricerca omonimi (vedi anche ticket 20200218019 Catania) | TF006.SIGE | Verifica SIGE - ricerca omonimi (vedi anche ticket 20200218019 Catania) |  |  |  | Verifica: verificare che il sistema ricerca nome-cognome-datadinascita-luogodinascita (e, se presenti, anche paternità e maternità) | 1.0 |  |  |  |  |
| SIUT | SIES | 20200303013 |  |  | 20200303013 | Siep Lista destinatari errata |  | SIGE | SIGE - Siep Lista destinatari errata | TF007.SIGE | Verifica Siep Lista destinatari errata |  |  |  | Verifica:  verificare che la lista destinatari sia congruente con la scelta del Giudice dell'esecuzione | 1.0 |  |  |  |  |
| SIUT | SIES | 202003040112 |  |  | 202003040112 | SIEP - Errore in provvedimento revoca sentenza per abolizione reato |  | SIEP | SIEP - SIEP - Errore in provvedimento revoca sentenza per abolizione reato | TF008.SIEP | Verifica SIEP - Errore in provvedimento revoca sentenza per abolizione reato |  |  |  | Verifica:  verificare che avvenga correttamente il provvedimento di revoca della sentenza di abolizione reato | 1.0 |  |  |  |  |
| SIUT | SIES | 20200312016.0 |  |  | 20200312016.0 | Test di sistema: mancanza di un controllo |  | SIES | SIES - Test di sistema: mancanza di un controllo | TF009.SIES | Verifica Test di sistema: mancanza di un controllo |  |  |  | Verifica: verificare che nel documento generato ci sia il controllo Test Connessione WS di Richiesta Certificato | 1.0 |  |  |  |  |
| SIUT | SIES | 20200319016.0 |  |  | 20200319016.0 | Correzione temblate 51 bis |  | SIEP | SIEP - Correzione temblate 51 bis | TF010.SIEP | Verifica Correzione temblate 51 bis |  |  |  | Verifica: verificare che due template inerenti l'art. 51 bis abbiano le corrette diciture volute dall'amministrazione. | 1.0 |  |  |  |  |

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
| Codifica Piano di test |  |  | SIUT-SIES-CT-1.0-20200424-Allegato-al-piano-test.xls |  |  |  |  |  |  |
| ID caso di test | Suffisso Caso di test | Nome Caso di test
Tipo Step |  | Descrizione |  | Versione | Stima tempo | N.cond. di test | Esito |
| TF001.SIEP | 01 | Verifica Cumulo su procedimento archiviato |  | Verifica: verificare che nel caso di cumulo su procedimento archiviato il sistema non blocchi l'emissione di qualsiasi altro provvedimento |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua nuovamente l'accesso al sistema SIES come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Individuare un procedimento con stato ARCHIVIATO | 2010/4 - 2010/6 |  |  |  |  |  |
|  | 2 | Azione | A partire da tale procedimento aprire un'istruttoria di cumulo e proseguire accedendo alla funzione 'dati finali cumulo'. |  | Visualizzazione pagina Dati Finali Cumulo |  |  |  |  |
|  | 3 | Azione | Procedere con la valorizzazione di ogni tabulatore interno sino ad arrivare alla stampa e validazione del provvedimento di pene concorrenti. |  | Visualizazzione pagina   Dettaglio Provvedimento Determinazione Pene Concorrenti |  |  |  |  |
|  | 4 | Azione | Dopo aver validato, andare sul dettaglio del procedimento cumulato e verificare che lo stato del procedimento non sia più ARCHIVIATO. |  | Visualizzazione pagina Dettaglio Procedimento |  |  |  |  |
|  | 5 | Azione | Inserire un qualsiasi provvedimento |  |  |  |  |  |  |
|  | V | Verifica | verificare che il sistema non blocchi l'emissione di qualsiasi altro provvedimento (step 5) |  |  |  |  |  |  |
| TF002.SIEP | 01 | Verifica Provvedimento di cumulo comunicazioni non validate |  | Verifica: verificare che il messaggio che segnala all'utente che esiste un provvedimento non validato contenga come info la tipologia e la data di inserimento dell'evento |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua nuovamente l'accesso al sistema SIES come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | L'utente ricerca un fascicolo che non abbia eventi non validati. | 2010/9 |  |  |  |  |  |
|  | 2 | Azione | A partire da tale procedimento aprire un'istruttoria di cumulo e proseguire accedendo alla funzione 'dati finali cumulo'. |  | Visualizzazione pagina Dati Finali Cumulo |  |  |  |  |
|  | 3 | Azione | L'utente esegue tutti i passi del cumulo fino a Emissione Provvedimento. In particolare:
- tab Posizione Giuridica : selezionare 'Espiazione Pena in Istituto di Detenzione'  ed indicare come posizione giuridica 'Espiazione Pena in Regime Carcerario';
- tab Emissione Provvedimento: selezionare Tribunale di Sorveglianza e Ufficio di Sorveglianza; per la Tipologia del provvedimento: selezionare il valore 'Provvedimento di unificazione di pene concorrenti (generico)';
- Confermare |  | Visualizazzione pagina   Dettaglio Provvedimento Determinazione Pene Concorrenti |  |  |  |  |
|  | 6 | Azione | L'utente procede con la validazione:
Seleziona il pulsante “Upload Stampa”;
Seleziona il pulsante “Generazione Stampa”;
Seleziona il check “Valida Documento” ;
Clicca su "Conferma". |  | Visualizazzione pagina   Dettaglio Provvedimento Determinazione Pene Concorrenti |  |  |  |  |
|  | 4 | Azione | L'utente seleziona il pulsante Uffici Esecuzione Penale/Sorveglianza |  | Visualizzazione pagina Comunicazioni alle Procure e Uffici di Sorveglianza |  |  |  |  |
|  | 5 | Azione | L'utente seleziona gli uffici di sorveglianza e conferma |  | Visualizzazione pagina Dettaglio Comunicazioni di Cumulo alle Procure e Uffici di Sorveglianza |  |  |  |  |
|  | 6 | Navigazione | Ordine di Esecuzione/Scarcerazione-> Ordine di Esecuzione |  |  |  |  |  |  |
|  | 7 | Azione | L'utente inserisce un ordine di scarcerazione -> Decorrenza e Scadenza |  | Visualizzazione messaggio bloccante |  |  |  |  |
|  | V | Verifica | Verificare che il messaggio che blocca l'utente, notificandogli che è presente un evento non validato, contiene le seguenti informazioni relative all'evento: la tipologia e la data di inserimento. In questo caso specifico la tipologia di evento è 'Provvedimento di unificazione di pene concorrenti (Comunicazione alle Procure e Uffici Sorveglianza)'. |  |  |  |  |  |  |
| TF003.SIUS | 01 | Verifica SIUS - errore F3 stampa certificato esecuzione |  | Verifica: verificare che venga prodotta la stampa del certificato esecuzione |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES come Ufficio di Sorveglianza | Exxxxx (Ufficio di Sorveglianza) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | L'utente ricerca un provvedimento dalla voce di menù Ricerche Altre BDI per il quale esista un'istruttoria di cumulo ma non un cumulo | 2020/1 - 2015/1413 | Visualizza pagina Dettaglio Procedimento |  |  |  |  |
|  | 2 | Azione | L'utente seleziona la funzione certificato stato esecuzione |  | Visualizzazione pagina Stampa Certificato Esecuzione |  |  |  |  |
|  | 3 | Azione | L'utente seleziona il pulsante di Generazione stampa PDF |  | Viene prodotto il certificato stato di esecuzione |  |  |  |  |
|  | V | Verifica | Verificare che l'applicativo esegue la stampa del certificato stato di esecuzione. |  |  |  |  |  |  |
| TF004.SIEP | 01 | Verifica Cumulo con ergastolo. Template e calcolo pena |  | Verifica: verificare che nel caso di pena irrogata con sentenza di cumulo il sistema nel calcolo e nei template non riporti la pena dell’ergastolo, determinata in cumulo, ma la sola pena temporanea. |  | 1.0 |  |  |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | L'utente ricerca un provvedimento con pena di cumulo irrogata in sentenza. Entra  in Dettaglio Procedimento | 2015/3 |  |  |  |  |  |
|  | 2 | Azione | L'utente seleziona la funzione Dettaglio Pena Complessiva |  | Visualizazzione pagina Dettaglio Pena Complessiva |  |  |  |  |
|  | 3 | Azione | L'utente va in Gestione Cumulo e clicca sul link Elenco Titoli Coinvolti |  | Visualizzazione pagina Elenco provvedimenti Esecutivi coinvolti |  |  |  |  |
|  | 4 | Azione | L'utente individua la sentenza associata al provvedimento ricercato nello step 1  e clicca su Dettaglio Dati Analitici presente nella colonna delle Azioni. |  | Visualizzazione pagina Gestione Dati analitici |  |  |  |  |
|  | 5 | Azione | L'utente seleziona il pulsante Dati Analitici e successivamente Pena Principale |  | Visualizzazione pagina Pena Complessiva Relativa al Titolo Cumulato |  |  |  |  |
|  | V | Verifica | Verificare che Il sistema non riporti la pena dell’ergastolo, determinata in cumulo, ma la sola pena temporanea. |  |  |  |  |  |  |
|  | 6 | Azione | L'utente deve accedere alla gestione cumulo del provvedimento individuato allo step 1. Cliccare su Elenco Istruttorie e  selezionare l'istruttoria con Provvedimento di cumulo Unificazione di Pene Concorrenti |  | Visualizzazione pagina Dettaglio Provvedimento Determinazione Pene Concorrenti |  |  |  |  |
|  | 7 | Azione | L'utente esegue tutti gli step:
-Dati Finali
-Pene Rideterminate
-Ulteriori sanzioni
-Posizione Giuridica
-Calcolo Pena
-Emissione Provvedimento |  |  |  |  |  |  |
|  | 8 | Azione | L'utente quando accede alle Pene Rideterminate seleziona il link Dettaglio della pena |  | Visualizzazione pagina Dati Finali Cumulo - Pene Determinate in cumulo |  |  |  |  |
|  | V | Verifica | Verificare che il popup visualizzato riporti correttamente sia la pena dell’ergastolo che la sola pena temporanea. |  |  |  |  |  |  |
|  | 9 | Azione | L'utente seleziona  Elenco Provvedimenti del PM |  | Visualizazzione pagina Elenco Provvedimenti PM |  |  |  |  |
|  | 10 | Azione | L'utente individua il provvedimento Provvedimento  di unificazione di pene concorrenti (con contestuale Ordine di Esecuzione Condannato Detenuto - ex Art 656 comma 1 cpp) e tra le azioni esegue la stampa |  | Produzione stampa SIEP_CUMULO_OE_656_DET.rtf. |  |  |  |  |
|  | V | Verifica | Verificare che nella stampa nella sezione OSSERVA vanno riportate tutte le pene calcolate dal sistema nella funzione Pene Rideterminate e nella sezione DETERMINA le pene come validate dall’utente. |  |  |  |  |  |  |
| TF005.SIEP | 01 | Verifica Errore assegnazione stato procedimento |  | Verifica: verificare che lo stato del fascicolo dopo l'inserimento del Verbale Vane Ricerche deve essere modificato dall'applicativo in 'Emesso Ordine di Esecuzione con Arresto Il dd-MM-yyyy - Verbale Vane Ricerche del : dd-MM-yyyy' |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | L'utente inserisce un fascicolo da voce di menu Iscrizione → Sentenza.
Dal dettaglio della sentenza l'utente va in “Assegnazione N. SIEP”, inserisce un procedimento e conferma. |  | Visualizza pagina Dettaglio della sentenza |  |  |  |  |
|  | 2 | Azione | Dal dettaglio della sentenza l'utente inserisce il soggetto e successivamente va in “Assegnazione N. SIEP” ed inserisce un procedimento. Infine conferma. | 2020/22 |  |  |  |  |  |
|  | 3 | Navigazione | Aggiornamento Posizione Giuridica |  |  |  |  |  |  |
|  | 4 | Azione | L'utente Inserisce la posizione giuridica 'Libero' e conferma |  | Visualizzazione pagina Dettaglio Posizione Giuridica |  |  |  |  |
|  | 5 | Azione | L'utente valida il procedimento dopo aver inserito le altre informazioni necessarie alla validazione. |  |  |  |  |  |  |
|  | 5 | Azione | L'utente seleziona 'Gestione Cumulo'-> Apertura istruttoria e conferma l'apertura dell'istruttoria |  |  |  |  |  |  |
|  | 6 | Azione | L'utente seleziona 'Dati finali cumulo', successivamente seleziona 'Emesso con ordinanza' ed inserisce I dati obbligatori.  Infine conferma. |  | Visualizzazione pagina Dati Finali Cumulo |  |  |  |  |
|  | 7 | Azione | L'utente inserisce 'Pene Rideterminate', seleziona 'Reclusione' e conferma. |  | Visualizzazione pagina Dati Finali Cumulo - Pene Determinate in cumulo |  |  |  |  |
|  | 8 | Azione | L'utente inserisce in 'Posizione Giuridica' la posizione 'Libero' e conferma. |  | Visualizzazione pagina Dati Finali Cumulo - Posizione Giuridica |  |  |  |  |
|  | 9 | Azione | L'utente inserisce 'Calcolo Pena' |  | Visualizzazione pagina Dettaglio Provvedimento Determinazione Pene Concorrenti |  |  |  |  |
|  | 10 | Azione | L'utente inserisce nel tab 'Emissione Provvedimento' un provvedimento di tipo 'Ordine di esecuzione per la carcerazione ex Art 656 comma 1 cpp' |  | Visualizzazione pagina Dettaglio Provvedimento Determinazione Pene Concorrenti |  |  |  |  |
|  | 11 | Azione | L'utente procede con la validazione del Provvedimento:
Seleziona il pulsante “Upload Stampa”;
Seleziona il pulsante “Generazione Stampa”;
Seleziona il check “Valida Documento” ;
Clicca su "Conferma". |  | Visualizzazione pagina Dettaglio Provvedimento Determinazione Pene Concorrenti |  |  |  |  |
|  | 12 | Azione | L'utente inserisce un verbale di vane ricerche da voce di menù 'Verbali Arresto/Vane Ricerche Notifica Carcere --> Verbale Vane Ricerche' |  |  |  |  |  |  |
|  | V | Verifica | Verificare che lo stato del fascicolo dopo l'inseriremento del Verbale Vane Ricerche sia modificato dall'applicativo in 'Emesso Ordine di Esecuzione con Arresto Il dd-MM-yyyy - Verbale Vane Ricerche del : dd-MM-yyyy' |  |  |  |  |  |  |
| TF006.SIGE | 01 | Verifica SIGE - ricerca omonimi (vedi anche ticket 20200218019 Catania) |  | Verifica: verificare che il sistema ricerca nome-cognome-datadinascita-luogodinascita (e, se presenti, anche paternità e maternità) |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIGE | Txxxxx (Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | L'utente ricerca un provvedimento con numero sige | 2019/1 | Visualizzazione pagina Dettaglio Procedimento SIGE |  |  |  |  |
|  | 2 | Azione | L'utente seleziona la funzionalità "Elenco Procedimenti SIEP del Soggetto" |  | Visualizzazione pagina  Elenco Procedimenti SIEP del Soggetto |  |  |  |  |
|  | V | Verifica | Verificare che il sistema mostri un elenco in cui la ricerca è avvenuta per nome-cognome-datadinascita-luogodinascita (e, se presenti, anche paternità e maternità). |  |  |  |  |  |  |
| TF007.SIGE | 01 | Verifica Siep Lista destinatari errata |  | Verifica:  verificare che la lista destinatari sia congruente con la scelta del Giudice dell'esecuzione |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Navigazione | Rideterminazione Pena -> Aministia/Indulto |  |  |  |  |  |  |
|  | 2 | Azione | Ricercare un procedimento con beneficio dell'indulto o inserirlo | 2020/2 | Visualizzazione pagina Dettaglio Anticipazioni Amnistia / Indulto |  |  |  |  |
|  | 3 | Azione | Inserire i dati obbligatori e cliccare su Conferma |  | Visualizzazione pagina Dettaglio Anticipazioni Amnistia / Indulto |  |  |  |  |
|  | 3 | Azione | Cliccare sul pulsante STAMPE |  | Visualizazzione pagina  Provvedimenti e Stampe per Rideterminazione Pena |  |  |  |  |
|  | 4 | Azione | Cliccare su Determinazione Pena per Revoca sent. e Incost. |  | Visualizazzione pagina  Richiesta Nuovo Residuo Pena |  |  |  |  |
|  | 5 | Azione | Selezionare Sede Ufficio Emittente |  | Visualizazzione popup con la lista delle sedi ufficio |  |  |  |  |
|  | V | Verifica | Verificare che l'elenco delle sedi sia congruente con la scelta del Giudice dell'Esecuzione. |  |  |  |  |  |  |
| TF008.SIEP | 01 | Verifica SIEP - Errore in provvedimento revoca sentenza per abolizione reato |  | Verifica:  verificare che avvenga correttamente il provvedimento di revoca della sentenza di abolizione reato |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Cxxxxx (Procura Generale della Repubblica Presso la Corte D'Appello) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Navigazione | Decisione del GE -> Incostituzionalità |  | Visualizzazione pagina Ricerca Procedimento |  |  |  |  |
|  | 2 | Azione | L'utente ricerca un procedimento | 2019/10 | Visualizzazione pagina Incostituzionalità |  |  |  |  |
|  | 3 | Azione | L'utente riempie i campi Declaratoria, Ufficio, Sede, +/-  (+) e Reclusione di un anno. Preme il tasto "Conferma". |  | Visualizzazione pagina Dettaglio Incostituzionalità |  |  |  |  |
|  | 4 | Azione | L'utente clicca sul pulsante Calcolo Pena |  | Visualizzazione pagina Calcolo Pena |  |  |  |  |
|  | 5 | Azione | L'utente clicca sul pulsante Conferma |  | Visualizzazione pagina Provvedimenti e Stampe per Decisione del GE |  |  |  |  |
|  | 6 | Azione | L'utente clicca sul pulsante relativo all'ordine di scarcerazione "Revoca sentenza per abolizione del reato dichiarazione incostituzionalità" |  | Visualizzazione pagina Ordine di scarcerazione per nuova scadenza pena |  |  |  |  |
|  | 7 | Azione | L'utente inserisce i campi obbligatori e clicca sul pulsante Conferma |  | Visualizzazione pagina  Dettaglio Ordine Scarcerazione Per Nuova Scadenza Pena |  |  |  |  |
|  | V | Verifica | Verificare il buon esito dell'operazione |  |  |  |  |  |  |
| TF009.SIES | 01 | Verifica Test di sistema: mancanza di un controllo |  | Verifica: verificare che nel documento generato ci sia il controllo Test Connessione WS di Richiesta Certificato |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema come Amministratore del sistema | ADMINTO (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'amministratore di sistema. |  |  |  |  |  |  |
|  | 1 | Azione | L'utente cliccare sul menù Test di Sistema |  | Generazione documento SIES_TEST.rtf |  |  |  |  |
|  | V | Verifica | Verificare  che nel documento generato ci sia il controllo Test Connessione WS di Richiesta Certificato |  |  |  |  |  |  |
| TF010.SIEP | 01 | Verifica Correzione temblate 51 bis |  | Verifica: verificare che due template inerenti l'art. 51 bis abbiano le corrette diciture volute dall'amministrazione. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 2 | Azione | L'utente selezionare un procedimento SIEP con pena residua da espiare valorizzata | 2019/17 |  |  |  |  |  |
|  | 3 | Azione | L'utente apre un'istruttoria di cumulo |  | Visualizzazione pagina Gestione Cumulo |  |  |  |  |
|  | 4 | Azione | L'utente seleziona l'istruttoria aperta e successivamente Dati Finali Cumulo |  | Visualizzazione pagina  Dati Finali Cumulo |  |  |  |  |
|  | 5 | Azione | L'utente valorizza la Data Emissione e conferma |  | Visualizzazione pagina  Dati Finali Cumulo |  |  |  |  |
|  | 6 | Azione | L'uetente seleziona Pene Rideterminate |  | Visualizzazione pagina Dati Finali Cumulo - Pene Determinate in cumulo |  |  |  |  |
|  | 7 | Azione | L'utente seleziono il link Dettaglio della pena |  | Visualizazione popup  Riepilogo delle pene |  |  |  |  |
|  | 8 | Azione | L' utente seleziona il tasto Carica |  | Visualizzazione pagina Dati Finali Cumulo - Pene Determinate in cumulo in cui vengono importatii valori di Totale Pene |  |  |  |  |
|  | 9 | Azione | L'utente seleziona il pulsante Conferma |  | Visualizzazione pagina Dati Finali Cumulo - Pene Determinate in cumulo |  |  |  |  |
|  | 10 | Azione | L'utente seleziona Posizione Giuridica |  | Visualizzazione pagina Dati Finali Cumulo - Posizione Giuridica |  |  |  |  |
|  | 11 | Azione | L'utente seleziona il radio button su Espiazione Pena in Altro Luogo e compila tutti i campi selezionando come posizione giuridica ‘Espiazione Pena in Regime di Affidamento in Prova’ . Infine Conferma |  | Visualizzazione pagina Dati Finali Cumulo - Posizione Giuridica |  |  |  |  |
|  | 12 | Azione | L'utente seleziona Calcolo Pena e successivamente Conferma |  | Visualizzazione pagina Dati Finali Cumulo - Pena Da Eseguire e dopo la conferma visualizzazione pagina Dettaglio Provvedimento Determinazione Pene Concorrenti |  |  |  |  |
|  | 13 | Azione | L'utente compila i campi obbligatori e seleziona come tipologia 'Richiesta cessazione della misura alternativa per sopravvenienza nuovo titolo esecutivo art. 51 Bis legge 354/75' . Infine Conferma. |  | Visualizzazione pagina Dettaglio Provvedimento Determinazione Pene Concorrenti |  |  |  |  |
|  | 14 | Azione | L'utente effettua la stampa |  | Produzione template SIEP_CUMULO_MA_CESS_51BIS |  |  |  |  |
|  | V | Verifica | Verificare che la stampa riporti correttemente la pena residua ad oggi e la nuova dicitura richiesta dall’Amministrazione |  |  |  |  |  |  |
|  | 15 | Azione | Nella pagina Dettaglio Provvedimento Determinazione Pene Concorrenti  clicco sull'icona di modifica |  | Visualizzazione pagina Dati Finali Cumulo - Emissione Provvedimento |  |  |  |  |
|  | 16 | Azione | L'utente modifica la tipologia del modello di stampa selezionando 'Prosecuzione provvisoria della misura alternativa art. 51 Bis legge 354/75' ed infine Conferma |  | Visualizzazione pagina Dettaglio Provvedimento Determinazione Pene Concorrenti |  |  |  |  |
|  | 17 | Azione | L'utente effettua la stampa |  | Produzione template SIEP_CUMULO_MA_PROSEC_51BIS |  |  |  |  |
|  | V | Verifica | Verificare che la stampa riporti correttemente la pena residua ad oggi e la nuova dicitura richiesta dall’Amministrazione |  |  |  |  |  |  |
|  | 01 |  |  |  |  |  |  |  |  |
|  | 01 |  |  |  |  |  |  |  |  |

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