---
uniqueName: siut-sies-ct-1-0-20200731-allegato-al-piano-testsi
displayName: "SIUT SIES CT 1 0 20200731 Allegato al piano test SIES v 12 4 1"
category: "GENERAL"
tags: []
---

# SIUT-SIES-CT-1.0-20200731-Allegato-al-piano-test_SIES_v.12.4.1

> **File originale:** `RILASCIO_12.4.1.0/SIUT-SIES-CT-1.0-20200731-Allegato-al-piano-test_SIES_v.12.4.1.xls`  
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
|  | Nome del file | SIUT-SIES-CT-1.0-20200731-Allegato-al-piano-test_SIES_v.12.4.1.xls |
|  | Piano di test | SIUT-SIES-PT-1.0-20200731-Piano_dei_Test_SIES_v.12.4.1.docx |
|  | Versione | 1.0 |
|  | Data | 44043.0 |
|  | Intervento | SIES v.12.4.1 |
|  | Area Applicativa | Penale |
|  | Allegato al Piano dei Test |  |

## TabellaTest

| Codice Area |  |  | SIES v.12.4.1 |  |  |  | Codifica  Piano di test |  | SIUT-SIES-CT-1.0-20200731-Allegato-al-piano-test_SIES_v.12.4.1.xls | Versione | 1.0 |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Applicazione |  |  | Funzionalità / Requisiti non funzionali |  |  |  |  |  |  | Caso di test |  |  |  |  |  |  |  |  |  |  |
| Codice Area | Codice Appl. | ID. Requisito | ID | Primo livello | ID | Primo Livello | Risk (1-5) | ID | Secondo livello | ID | Nome del caso di test | Classe di Gravità (1-4) | Ciclo di test | Stima Durata | Descrizione e note | Versione | N. cond. di test | Autom. | Classe di rilevanza (A, B, C) | Esito |
| SIUT | SIES | 20200525017.0 |  |  | 20200525017.0 | archiviazione - versione 12.x |  | SIEP | SIEP - archiviazione - versione 12.x | TF001.SIEP | Verifica della eliminazione della dicitura di cumulo nel caso di archiviazione manuale del relativo procedimento. |  |  |  | Verifica: verificare che nel caso di archiviazione manuale di un procedimento di cumulo, il sistema non prospetti la dicitura prevista per il cumulo nella pagina di dettaglio dello stesso procedimento | 1.0 |  |  |  |  |
| SIUT | SIES | 20200525013.0 |  |  | 20200525013.0 | correzione template SIES 12.0 |  | SIEP | SIEP - correzione template SIES 12.0 | TF002.SIEP | Verifica corretta generazione di due report per provvedimenti di archiviazione di misure di sicurezza. |  |  |  | Verificare che i report SIEP_MS_ARCH_GE.rtf e SIEP_MS_ARCH_GIU_CAS.rtf siano prospettati secondo le indicazioni fornite dall'utente | 1.0 |  |  |  |  |
| SIUT | SIES | 20200508015.0 |  |  | 20200508015.0 | SIES - Errore in stampa Comunicazione rideterminaizone pena |  | SIEP | SIEP - SIES - Errore in stampa Comunicazione rideterminaizone pena | TF003.SIEP | Verifica corretta generazione della stampa della Comunicazione per Rideterminazione Pena |  |  |  | Verificare che il report SIEP_RP_OSRDP.rtf sia prospettato correttamente | 1.0 |  |  |  |  |
| SIUT | SIES | 20200525014.0 |  |  | 20200525014.0 | emissione cumulo pene |  | SIEP | SIEP - emissione cumulo pene | TF004.SIEP | Verifica che non si generi l'errore in caso di  emissione del provvedimento di cumulo |  |  |  | Verificare che per la posizione giuridica espiazione pena in regime di detenzione domiciliare non si verifichi l'errore in caso di emissione del provvedimento di cumulo. | 1.0 |  |  |  |  |
| SIUT | SIES | 20200528012.0 |  |  | 20200528012.0 | SIGE - inserimento parte civile / offesa su quadro "emissione ordinanza" |  | SIGE | SIGE - SIGE - inserimento parte civile / offesa su quadro "emissione ordinanza" | TF005.SIGE | Verifica che in fase di inserimento delle parti (civili/offese) il sistema non si presenti l'errore java ma mostri un messaggio di alert parlante. |  |  |  | Verifica che in fase di inserimento delle parti (civili/offese) il sistema non si presenti l'errore java ma mostri un messaggio di alert per l'utente. | 1.0 |  |  |  |  |
| SIUT | SIES | 20200708017.0 |  |  | 20200708017.0 | Anomalia riscontrata su SIUS su versione 12.3.0.2 |  | SIUS | SIUS - Anomalia riscontrata su SIUS su versione 12.3.0.2 | TF006.SIUS | Verifica che possa essere annullata un'ordinanza già validata e depositata associata ad un procedimento SIUS |  |  |  | Verificare che in un procedimento SIUS non venga prospettato il messaggio bloccante quando si annulla un'ordinanza associata al procedimento stesso | 1.0 |  |  |  |  |
| SIUT | SIES | 20200709011 |  |  | 20200709011 | Malfunzionamento stampa di notifica "tramite SNT" |  | SIUS | SIUS - Malfunzionamento stampa di notifica "tramite SNT" | TF007.SIUS | Verifica corretta dicitura sulla stampa del template associato al deposito di un decreto. |  |  |  | Verificare che in un procedimento SIUS il template SIUS_DE_DEPOSITODECRETO.rtf non contenga la dicitura della "notifica tramite SNT" duplicata. | 1.0 |  |  |  |  |
| SIUT | SIES | 20200710012 |  |  | 20200710012.0 | SIES -  SIEP - Errore nella stampa ordinanza scarcerazione. |  | SIEP | SIEP - SIES -  SIEP - Errore nella stampa ordinanza scarcerazione. | TF008.SIEP | Verifica del corretto allinemento degli uffici destinatari nella stampa del template emesso in corrispondenza di un ordine di scarcerazione per liberazione anticipata. |  |  |  | Verificare che il template SIEP_OS_LIBAN.rtf riporti correttamente ed in modo allineato gli uffici destinatari . | 1.0 |  |  |  |  |
| SIUT | SIES | 202007070114 |  |  | 202007070114 | assenza proc SIEP nello scadenziario |  | SIEP | SIEP - assenza proc SIEP nello scadenziario | TF009.SIEP | Verifica corretto inserimento/aggiornamento scadenzario fine pena |  |  |  | Verificare che nella validazione della Comunicazione  Concessione Detenzione Domiciliare ex art.47 ter O.P.. venga inserito/aggiornato lo scadenzario fine pena. | 1.0 |  |  |  |  |
| SIUT | SIES | 202007060112 |  |  | 202007060112 | PROVVEDIMENTO DI REVOCA DS PER NLP SU ISTANZA DI MISURA ALTERNATIVA |  | SIEP | SIEP - PROVVEDIMENTO DI REVOCA DS PER NLP SU ISTANZA DI MISURA ALTERNATIVA | TF010.SIEP | Verifica corretta generazione template |  |  |  | Verificare che il template SIEP_RS_DACNI_M.rtf contenga i dati dell'ordinanza di revoca. | 1.0 |  |  |  |  |
| SIUT | SIES | 20200715013 |  |  | 20200715013 | SIES -  Mancata visualizzazione autorità destinatarie trasmissione atti |  | SIEP | SIEP - SIES -  Mancata visualizzazione autorità destinatarie trasmissione atti | TF011.SIEP | Verifica popolamento combo in trasmissione atti |  |  |  | Verificare che nella pagina Trasmissione Atti siano correttamente popolate le combo relative a Magistrato di Sorveglianza, Tribunale di Sorveglianza, UEPE/USSM | 1.0 |  |  |  |  |
| SIUT | SIES | 20200721012.0 |  |  | 20200721012.0 | trasmissione atti SIEP |  | SIEP | SIEP - trasmissione atti SIEP |  |  |  |  |  |  |  |  |  |  |  |
| SIUT | SIES | 20200715018 |  |  | 20200715018.0 | SIES -  Periodi custodia cautelare continuativi |  | SIES | SIES - SIES -  Periodi custodia cautelare continuativi | TF012.SIES | Verifica corretta gestione di due periodi distinti  ma continuativi di Misure Cautelari |  |  |  | Verificare che inserendo due gruppi distinti ma con periodi continuativi di misure cautelari sia presente a video e sulla stampa la corretta gestione dei totali parziali. | 1.0 |  |  |  |  |
| SIUT | SIES | 20200720013 |  |  | 20200720013 | SIEP - mancata generazione documento per evento "Registrazione data inizio misura" |  | SIEP | SIEP - SIEP - mancata generazione documento per evento "Registrazione data inizio misura" | TF013.SIEP | Verifica corretta gestione del codice 0610 del Tribunale di Sorveglianza |  |  |  | Verificare che venga gestito correttamente il codice 0610 e che i template SIEP_MA_ESECDOM_DECSCA.rtf e SIEP_MA_ESECDOM_LIB.rtf vengano generati correttamente. | 1.0 |  |  |  |  |
| SIUT | SIES | 20200715012 |  |  | 20200715012.0 | SIES -  Assenza pena principale dati analitici - caricamento manuale titolo |  | SIEP | SIEP - SIES -  Assenza pena principale dati analitici - caricamento manuale titolo | TF014.SIEP | Verificare che in fase di stampa del cumulo sia gestita l'assenza della pena principale |  |  |  | Verificare che in fase di stampa del cumulo per gestire l'assenza della Pena Principale in presenza delle richieste revoca Sospensione Condizionale. | 1.0 |  |  |  |  |
| SIUT | SIES | 20200723012 |  |  | 20200723012.0 | SIEP - Scadenzari per cumulo con contestuale decreto di sospensione ex art. 656 |  | SIEP | SIEP - SIEP - Scadenzari per cumulo con contestuale decreto di sospensione ex art. 656 | TF015.SIEP | Verificare corretto funzionamento dello scadenzario simeone per provvedimenti di cumulo pene con sospensione per ex 656. |  |  |  | Verificare corretto funzionamento dello scadenzario simeone per provvedimenti di cumulo pene con sospensione per ex 656. | 1.0 |  |  |  |  |

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

| Progetto / Obiettivo Software |  |  | a |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | SIUT-SIES-CT-1.0-20200731-Allegato-al-piano-test_SIES_v.12.4.1.xls |  |  |  |  |  |  |
| ID caso di test | Suffisso Caso di test | Nome Caso di test
Tipo Step |  | Descrizione |  | Versione | Stima tempo | N.cond. di test | Esito |
| TF001.SIEP | 01 | Verifica della eliminazione della dicitura di cumulo nel caso di archiviazione manuale del relativo procedimento. |  | Verifica: verificare che nel caso di archiviazione manuale di un procedimento di cumulo, il sistema non prospetti la dicitura prevista per il cumulo nella pagina di dettaglio dello stesso procedimento |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Individuare un procedimento di classe IV validato e proseguire con la trasmissione per competenza/seguito atti utilizzando il menù  Istruttorie/Richieste. Scegliere come oggetto dell'atto la voce 'emissione provvedimento di cumulo' e prroseguire con la validazione e la trasmissione. |  | Sulla pagina di dettaglio del procedimento di classe IV il sistema mostra il messaggio: "Procedimento trasmesso per assorbimento in cumulo…." |  |  |  |  |
|  | 2 | Navigazione | Gestione Misure Sicurezza > Archiviazione Manuale |  | Visualizzazione pagina Definizione Procedimento - Archiviazione Manuale |  |  |  |  |
|  | 3 | Azione | Valorizzare i campi di  input obbligatori:
Data Definizione
Oggetto Definizione (Archiviazione per applicazione definitiva con sentenza di condanna) 
Magistrato Firmatario
Infine cliccare sul pulsante Conferma |  | Visualizzazione pagina Dettaglio Archiviazione Manuale |  |  |  |  |
|  | 4 | Azione | Effettuare la procedura di Validazione |  |  |  |  |  |  |
|  | 5 | Azione | Ricercare il procedimento |  | Visualizzazione pagina Dettaglio Procedimento |  |  |  |  |
|  | V | Verifica | Verificare che la dicitura (in rosso) "Procedimento trasmesso per assorbimento in cumulo..." non sia più presente mentre sarà presente la dicitura "ARCHIVIATO". |  |  |  |  |  |  |
|  | R1 | Riciclo Test | Ripetere il caso di test dallo step 1  allo step 5 scegliendo un'altra voce presente nel sottomenù "Definizione Procedimento" in Gestione Misure di Sicurezza |  |  |  |  |  |  |
|  | V | Verifica esterna | Verificare che la dicitura (in rosso) "Procedimento trasmesso per assorbimento in cumulo..." non sia più presente mentre sarà presente la dicitura "ARCHIVIATO". |  |  |  |  |  |  |
| TF002.SIEP | 01 | Verifica corretta generazione di due report per provvedimenti di archiviazione di misure di sicurezza. |  | Verificare che i report SIEP_MS_ARCH_GE.rtf e SIEP_MS_ARCH_GIU_CAS.rtf siano prospettati secondo le indicazioni fornite dall'utente |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Individuare un fascicolo iscritto in classe IV non archiviato |  | Visualizzazione pagina Dettaglio Procedimento |  |  |  |  |
|  | 2 | Navigazione | Gestione Misure Sicurezza > Definizione Procedimento |  |  |  |  |  |  |
|  | 3 | Azione | Selezionare Archiviazione per Provvedimento del Giudice Esecuzione |  | Visualizzazione pagina Definizione Procedimento - Archiviazione per Provvedimento del Giudice Esecuzione |  |  |  |  |
|  | 4 | Azione | Valorizzare i campi di  input obbligatori
Infine cliccare sul pulsante Conferma |  | Visualizzazione pagina Dettaglio Definizione Procedimento - Archiviazione per Provvedimento del G.E. |  |  |  |  |
|  | 5 | Azione | Premere il  pulsante Stampa |  | Viene generato il documento |  |  |  |  |
|  | V | Verifica | Verificare che venga prodotto correttamente il report SIEP_MS_ARCH_GE.rtf |  |  |  |  |  |  |
|  | R1 | Riciclo Test | Ripetere il caso di test dallo step 1  allo step 4 scegliendo in Gestione Misure di Sicurezza, nel sottomenù "Definizione Procedimento",  la voce Archiviazione per Provvedimento del Giudice / Cassazione |  | Visualizzazione pagina Definizione Procedimento - Archiviazione per Provvedimento del Giudice / Cassazione |  |  |  |  |
|  | 6 | Azione | Valorizzare i campi di  input obbligatori
Infine cliccare sul pulsante Conferma |  | Visualizzazione pagina Dettaglio Definizione Procedimento - Archiviazione per Provvedimento del Giudice/Cassazione |  |  |  |  |
|  | 7 | Azione | Premere il  pulsante Stampa |  | Viene generato il documento |  |  |  |  |
|  | V | Verifica esterna | Verificare che venga prodotto correttamente il report SIEP_MS_ARCH_GIU_CAS.rtf |  |  |  |  |  |  |
| TF003.SIEP | 01 | Verifica corretta generazione della stampa della Comunicazione per Rideterminazione Pena |  | Verificare che il report SIEP_RP_OSRDP.rtf sia prospettato correttamente |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Individuare un procedimento il cui soggetto si trova in 'Espiazione Pena in Regime Carcerario' |  |  |  |  |  |  |
|  | 2 | Navigazione | Rideterminazione Pena>>Altro |  | Visualizzazione pagina Rideterminazione della Pena - Altro |  |  |  |  |
|  | 3 | Azione | Emettere il provvedimento inserendo  i campi obbligatori e successivamente cliccare su Conferma |  | Visualizzazione pagina Dettaglio Rideterminazione Pena Altro |  |  |  |  |
|  | 4 | Azione | Cliccare sul pulsante Calcolo Pena |  | Visualizazzione pagina Calcolo Pena |  |  |  |  |
|  | 5 | Azione | Cliccare su Conferma |  | Visualizzazione pagina  Dettaglio Rideterminazione Pena Altro |  |  |  |  |
|  | 6 | Azione | Cliccare su Stampe |  | Visualizazzione pagina Provvedimenti e Stampe per Rideterminazione Pena |  |  |  |  |
|  | 7 | Azione | Selezionare Rideterminazione Pena (Ordine di scarcerazione) |  | Visualizzazione pagina Ordine di Scarcerazione per Nuova Scadenza Pena |  |  |  |  |
|  | 8 | Azione | Inserire i dati obbligatori.
Successivamente cliccare su Conferma |  | Visualizzazione pagina Dettaglio Comunicazione Rideterminazione Pena |  |  |  |  |
|  | 9 | Azione | Cliccare su Stampa |  | Viene generata la stampa |  |  |  |  |
|  | V | Verifica esterna | Verificare che venga prodotta correttamente la stampa SIEP_RP_OSRDP |  |  |  |  |  |  |
| TF004.SIEP | 01 | Verifica che non si generi l'errore in caso di  emissione del provvedimento di cumulo |  | Verificare che per la posizione giuridica espiazione pena in regime di detenzione domiciliare non si verifichi l'errore in caso di emissione del provvedimento di cumulo. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Individuare un procedimento per il quale sia stato emessa una decisione del GE di applicazione amnistia/indulto. |  |  |  |  |  |  |
|  | 2 | Navigazione | Gestione cumulo > Apertura Istruttoria |  |  |  |  |  |  |
|  | 3 | Azione | Aprire una istruttoria di cumulo cliccando sul pulsante Conferma |  | Visualizzazione Pagina Apertura Istruttoria Cumulo |  |  |  |  |
|  | 4 | Azione | Tornare nella pagina Gestione Cumulo ed andare in Dati Finali Cumulo |  | Visualizzazione pagina  Dati Finali Cumulo |  |  |  |  |
|  | 5 | Azione | Inserire Data Emissione e cliccare su Conferma |  | Visualizzazione pagina contenente una serie di tabulatori |  |  |  |  |
|  | 6 | Azione | Riempire i dati obbligatori per ogni tabulatore |  |  |  |  |  |  |
|  | 7 | Azione | Arrivati alla pagina Dettaglio Provvedimento Determinazione Pene Concorrenti cliccare sul pulsante di Stampa |  | Viene generata la stampa |  |  |  |  |
|  | V | Verifica esterna | Verificare che venga prodotta correttamente la stampa SIEP_CUMULO_OE_656_C5_SOSP |  |  |  |  |  |  |
| TF005.SIGE | 01 | Verifica che in fase di inserimento delle parti (civili/offese) il sistema non si presenti l'errore java ma mostri un messaggio di alert parlante. |  | Verifica che in fase di inserimento delle parti (civili/offese) il sistema non si presenti l'errore java ma mostri un messaggio di alert per l'utente. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIGE come Corte d'Appello | Kxxxxx (Corte d'Appello) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Navigazione | Ordinanze/Deposito/Notifiche » Emissione Ordinanza |  |  |  |  |  |  |
|  | 2 | Azione | Inserire un numero SIGE (Anno e Numero) per cui non sia ancora fissata udienza. |  | Visualizzazione pagina Emissione Ordinanza |  |  |  |  |
|  | 3 | Azione | Cliccare sul link Gestione Parti Civili |  | Visualizzazione pagina Inserimento Parte Civile |  |  |  |  |
|  | 4 | Azione | Riempire i campi obbligatori  e cliccare su Conferma |  | Visualizzazione pagina Inserimento Difensore Parte |  |  |  |  |
|  | 5 | Azione | Cliccare su Conferma |  | Visualizzazione pagina Dettaglio Parte Fisica Civile |  |  |  |  |
|  | V | Verifica esterna | Verificare che non venga prodotto l'errore java ma che il sistema mostri un messaggio per come procedere per l'inserimento delle parti. |  |  |  |  |  |  |
|  | R1 | Riciclo Test | Ripetere il test con il link Gestione Parti Offese |  | Visualizzazione pagina Inserimento Parte Offesa |  |  |  |  |
|  | 6 | Azione | Riempire i campi obbligatori  e cliccare su Conferma |  | Visualizzazione pagina Inserimento Difensore Parte |  |  |  |  |
|  | 7 | Azione | Cliccare su Conferma |  | Visualizzazione pagina Dettaglio Parte Fisica Offesa |  |  |  |  |
|  | V | Verifica esterna | Verificare che non venga prodotto l'errore java ma che il sistema mostri un messaggio per come procedere per l'inserimento delle parti. |  |  |  |  |  |  |
| TF006.SIUS | 01 | Verifica che possa essere annullata un'ordinanza già validata e depositata associata ad un procedimento SIUS |  | Verificare che in un procedimento SIUS non venga prospettato il messaggio bloccante quando si annulla un'ordinanza associata al procedimento stesso |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIUS come Tribunale di Sorveglianza | Dxxxxx (Tribunale di Sorveglianza) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | L'utente individua un procedimento con deposito validato utilizzando
 la funzione 'Ricerche e Visualizzazioni » Estremi atto' con filtro su 'Procedimenti Definiti'. |  | Visualizzazione pagina Dettaglio Procedimento SIUS |  |  |  |  |
|  | 2 | Azione | Dal dettaglio del procedimento SIUS, l'utente si sposta sull'elenco dei provvedimenti |  | Visualizzazione pagina Ricerca Provvedimenti |  |  |  |  |
|  | 3 | Azione | L'utente utilizza la funzione di cancellazione posta in corrispondenza della riga dell'ordinanza. |  | Visualizzazione del Messaggio di conferma |  |  |  |  |
|  | 4 | Azione | L'utente conferma l'annullamento |  | Visualizzazione pop-up in cui si chiede di inserire la motivazione dell'annullamento |  |  |  |  |
|  | 5 | Azione | L'utente compila il campo note con la motivazione dell'annullamento e conferma |  |  |  |  |  |  |
|  | V | Verifica esterna | Verificare che il provvedimento venga annullato |  |  |  |  |  |  |
| TF007.SIUS | 01 | Verifica corretta dicitura sulla stampa del template associato al deposito di un decreto. |  | Verificare che in un procedimento SIUS il template SIUS_DE_DEPOSITODECRETO.rtf non contenga la dicitura della "notifica tramite SNT" duplicata. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIUS come Ufficio di Sorveglianza | Exxxxx (Ufficio di Sorveglianza) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | L'utente iscrive un procedimento SIUS (es: con contenuto Accertamento Ex Art. 58 Ter O.P )ed inserisce il decreto. |  |  |  |  |  |  |
|  | 2 | Azione | L'utente prosegue l'emissione del decreto e lo valida, |  |  |  |  |  |  |
|  | 3 | Navigazione | Decreti >> Deposito Decreto |  |  |  |  |  |  |
|  | 4 | Azione | L'utente inserisce la data del deposito e conferma. |  | Il sistema mostra la pagina  dettaglio. |  |  |  |  |
|  | 5 | Azione | L'utente seleziona il radio button 'Deposito Decreto e Trasmissione' |  | Il sistema mostra la pagina per inserire i dati della trasmissione. |  |  |  |  |
|  | 6 | Azione | L'utente prosegue con l'inserimento dei dati obbligatori.
In particolare, nella sezione dei destinatari verificare che per la notifica all'avvocato sia selezionata la voce "Notifica tramite SNT". |  |  |  |  |  |  |
|  | 7 | Azione | Cliccare su Conferma. |  | Visualizzazione pagina Dettaglio Deposito Decreto |  |  |  |  |
|  | 8 | Azione | Cliccare su Stampa |  | Generazione documento SIUS_DE_DEPOSITODECRETO.rtf |  |  |  |  |
|  | V | Verifica esterna | Verificare che la dicitura "Notifica tramite SNT" non sia duplicata. |  |  |  |  |  |  |
| TF008.SIEP | 01 | Verifica del corretto allinemento degli uffici destinatari nella stampa del template emesso in corrispondenza di un ordine di scarcerazione per liberazione anticipata. |  | Verificare che il template SIEP_OS_LIBAN.rtf riporti correttamente ed in modo allineato gli uffici destinatari . |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Individuare un procedimento il cui soggetto si trova in 'Espiazione Pena in Regime Carcerario' |  |  |  |  |  |  |
|  | 2 | Navigazione | Decisioni Sorveglianza >> Liberazione Anticipata |  |  |  |  |  |  |
|  | 3 | Azione | Nella pagina Emissione Ordinanza di Liberazione Anticipata  inserire i dati obbligatori e cliccare su Conferma |  | Visualizzazione pagina Dettaglio Liberazione Anticipata |  |  |  |  |
|  | 4 | Azione | Cliccare su Calcolo data fine pena |  | Visualizzazione pagina  Ordine di Scarcerazione a seguito di ordinanza Liberazione Anticipata |  |  |  |  |
|  | 5 | Azione | Inserire i dati obbligatori e cliccare su Conferma |  | Visualizzazionepagina Dettaglio Ordine di Scarcerazione a seguito di ordinanza liberazione anticipata - Espiazione Pena in Regime Carcerario |  |  |  |  |
|  | 6 | Azione | Cliccare sul pulsante di Stampa |  | Viene generata la stampa |  |  |  |  |
|  | V | Verifica esterna | Verificare che il template generato SIEP_OS_LIBAN riporti  l'elenco dei destinatari (UDS/TDS) allineati correttamente. |  |  |  |  |  |  |
| TF009.SIEP | 01 | Verifica corretto inserimento/aggiornamento scadenzario fine pena |  | Verificare che nella validazione della Comunicazione  Concessione Detenzione Domiciliare ex art.47 ter O.P.. venga inserito/aggiornato lo scadenzario fine pena. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Iscrivere un procedimento da Libero |  |  |  |  |  |  |
|  | 2 | Azione | Emettere Ordine di Esecuzione. |  |  |  |  |  |  |
|  | 3 | Azione | Registrare il verbale di arresto. |  |  |  |  |  |  |
|  | 4 | Azione | Emettere ordine di scarcerazione  decorrenza/scadenza. Validare |  |  |  |  |  |  |
|  | 5 | Navigazione | Decisioni della Sorveglianza -Detenzione Domiciliare - Concessione. |  |  |  |  |  |  |
|  | 6 | Azione | Compilare i dati mettendo la spunta su "Scarcerato" ed indicando la data di scarcerazione. |  |  |  |  |  |  |
|  | 7 | Azione | Procedere alla validazione del provvedimento |  |  |  |  |  |  |
|  | V | Verifica esterna | Verificare che Il sistema inserisca lo scadenzario fine pena. |  |  |  |  |  |  |
| TF010.SIEP | 01 | Verifica corretta generazione template |  | Verificare che il template SIEP_RS_DACNI_M.rtf contenga i dati dell'ordinanza di revoca. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Iscrivere un procedimento per soggetto detenuto altra causa in regime di arresti domiciliari. |  |  |  |  |  |  |
|  | 2 | Navigazione | Ordini di Esecuzione/Scarcerazione » Sospensione esecuzione ex art.656 c.p.p. |  |  |  |  |  |  |
|  | 3 | Azione | Emettere Ordine di Esecuzione con sospensione. |  | Visualizzazione pagina Ordine di Esecuzione con sospensione (LEGGE 165/98) - DETENUTO PER ALTRA CAUSA |  |  |  |  |
|  | 4 | Navigazione | Ordini di Esecuzione/Scarcerazione » Sospensione Esecuzione ex art. 656 c.p.p. » Gestione Decreto di Sospensione |  |  |  |  |  |  |
|  | 5 | Azione | Selezionare il pulsante Notifiche e registrare le notifiche al Condannato e agli Avvocati. |  | Visualizzazione pagina  Gestione Notifiche Decreto Sospensione |  |  |  |  |
|  | 6 | Navigazione | Ordini di Esecuzione/Scarcerazione » Sospensione Esecuzione ex art. 656 c.p.p. » Istanza (Annotazione Trasmissione) |  |  |  |  |  |  |
|  | 7 | Azione | Iscrivere l'istanza di ammissione alle misure alternative. |  | Visualizzazione pagina    Iscrizione Istanza per Procedimento SIEP |  |  |  |  |
|  | 8 | Navigazione | Ordini di Esecuzione/Scarcerazione» Sospensione esecuzione ex art.656 c.p.p. » Revoca Sospensione Esecuzione ex art. 656 c.p.p.. |  |  |  |  |  |  |
|  | 9 | Azione | Registrare il provvedimento di revoca della sospensione |  | Visualizzazione pagina   Revoca Decreto Sospensione (legge 165/98) |  |  |  |  |
|  | 10 | Azione | Selezionare nella form come "Motivo Revoca" l'opzione "Reiezione Istanza" e completare i campi obbligatori. Infine procedere alla stampa. |  | Viene generata la stampa |  |  |  |  |
|  | V | Verifica esterna | Verificare che il sistema produce la stampa del modello SIEP_RS_DACNI_M.rtf riportante i dati dell'ordinanza di revoca. |  |  |  |  |  |  |
| TF011.SIEP | 01 | Verifica popolamento combo in trasmissione atti |  | Verificare che nella pagina Trasmissione Atti siano correttamente popolate le combo relative a Magistrato di Sorveglianza, Tribunale di Sorveglianza, UEPE/USSM |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Ricercare un procedimento di classe I |  |  |  |  |  |  |
|  | 2 | Navigazione | Istruttorie/richieste |  |  |  |  |  |  |
|  | 3 | Azione | Cliccare su Trasmissione Atti ex art. 51 bis |  | Visualizzazione pagina Trasmissione Atti |  |  |  |  |
|  | V | Verifica esterna | Verificare che le combo relative a Magistrato di Sorveglianza, Tribunale di Sorveglianza, UEPE/USSM siano popolate |  |  |  |  |  |  |
| TF012.SIES | 01 | Verifica corretta gestione di due periodi distinti  ma continuativi di Misure Cautelari |  | Verificare che inserendo due gruppi distinti ma con periodi continuativi di misure cautelari sia presente a video e sulla stampa la corretta gestione dei totali parziali. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Iscrivere un procedimento di classe I. |  | Visualizzazione pagina Dettaglio Procedimento |  |  |  |  |
|  | 2 | Azione | Dalla combo del Dettaglio selezionare Iscrizione Misura Cautelare |  | Visualizzazione pagina Misure Cautelari |  |  |  |  |
|  | 3 | Azione | Selezionare Cessata al momento del passaggio in giudicato computabili |  | Visualizzazione pagina Inserimento Misura Cautelare - COMPUTABILE |  |  |  |  |
|  | 4 | Azione | Inserire un periodo di Misure cautelari e cliccare su Conferma |  | Visualizzazione pagina Elenco Misure Cautelari |  |  |  |  |
|  | 5 | Azione | Tramite il link Inserimento Ulteriori Misure Cautelari inserire altri periodi creando 2 "gruppi" con  misure in continuazione (es 2 periodi contigui e altri 2 periodi contigui). |  |  |  |  |  |  |
|  | V | Verifica esterna | Verificare che nella pagina Elenco Misure Cautelari la colonna Totale deve riportare 2 totali parziali relativi ai 2 gruppi. |  |  |  |  |  |  |
|  | 7 | Navigazione | Istruttorie/Richieste |  |  |  |  |  |  |
|  | 8 | Azione | Cliccare su Stampa Copertina |  | Visualizzazione pagina Stampa Copertina fascicolo |  |  |  |  |
|  | 9 | Azione | Cliccare sull'icona di Stampa |  | Viene generata la stampa MisuraCautelare.rtf |  |  |  |  |
|  | V | Verifica esterna | Verificare che la stampa  riporti i totali parziali sotto l'ultimo rigo di ogni gruppo di periodi in continuazione. |  |  |  |  |  |  |
| TF013.SIEP | 01 | Verifica corretta gestione del codice 0610 del Tribunale di Sorveglianza |  | Verificare che venga gestito correttamente il codice 0610 e che i template SIEP_MA_ESECDOM_DECSCA.rtf e SIEP_MA_ESECDOM_LIB.rtf vengano generati correttamente. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Creare un fascicolo di classe I per soggetto libero. |  |  |  |  |  |  |
|  | 2 | Azione | Emettere Ordine di Esecuzione con sospensione. |  |  |  |  |  |  |
|  | 3 | Azione | Trasmettere il fascicolo al tribunale di Sorveglianza |  |  |  |  |  |  |
|  | 4 | Azione | L'utente effettua l'accesso al sistema SIUS come Tribunale di Sorveglianza | Dxxxxx (Tribunale di Sorveglianza) |  |  |  |  |  |
|  | 5 | Azione | L'utente crea un fascicolo con contenuto "Concessione Misure Alternative Alla Detenzione" ed oggetto "Esecuzione presso domicilio della pena detentiva ( TdS )" collegato a fascicolo SIEP precedentemente creato. |  |  |  |  |  |  |
|  | 6 | Azione | Emettere ordinanza di concessione "Esecuzione presso domicilio della pena detentiva ( TdS ) - Legge 199/2010". |  |  |  |  |  |  |
|  | 7 | Azione | Depositare l'ordinanza e la trasmette alla Procura. |  |  |  |  |  |  |
|  | 8 | Azione | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | 9 | Navigazione | Decisioni Sorveglianza |  |  |  |  |  |  |
|  | 10 | Azione | Cliccare su Esecuzione pena presso il domicilio |  | Visualizzazione pagina  Espiazione Pena Presso Domicilio |  |  |  |  |
|  | 11 | Azione | Cliccare su Concessione |  | Visualizzazione pagina  Concessione Espiazione Pena presso Domicilio |  |  |  |  |
|  | 12 | Azione | Selezionare il "provvedimento di Sorveglianza dalla lista" ed emettere l'ordine di esecuzione validandolo. |  | Visualizzazione pagina  Espiazione Pena presso Domicilio |  |  |  |  |
|  | V | Verifica esterna | Verificare che la stampa che si genera prima della validazione riporti il Tribunale di Sorveglianza |  |  |  |  |  |  |
|  | 13 | Navigazione | Verbali Arresto/Vane ricerche Notifica carcere |  |  |  |  |  |  |
|  | 14 | Azione | Cliccare su Registrazione Data inizio misura |  |  |  |  |  |  |
|  | 15 | Azione | Procedere con l'emissione della Comunicazione |  |  |  |  |  |  |
|  | V | Verifica esterna | Verificare che il sistema non si blocchi e che la stampa riporti correttamente il Tribunale di Sorveglianza. |  |  |  |  |  |  |
| TF014.SIEP | 01 | Verificare che in fase di stampa del cumulo sia gestita l'assenza della pena principale |  | Verificare che in fase di stampa del cumulo per gestire l'assenza della Pena Principale in presenza delle richieste revoca Sospensione Condizionale. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Iscrivere un fascicolo SIEP di classe I. |  |  |  |  |  |  |
|  | 2 | Azione | Cliccare sull'icona  Gestione cumulo |  | Visualizzazione pagina  Gestione Cumulo |  |  |  |  |
|  | 3 | Azione | Cliccare su Apertura Istruttoria |  | Visualizzazione pagina Apertura Istruttoria Cumulo |  |  |  |  |
|  | 4 | Azione | Cliccare su Conferma e successivamente sull'icona per tornare indietro |  | Visualizzazione pagina Gestione Cumulo |  |  |  |  |
|  | 5 | Azione | Cliccare sul link Elenco Titoli Coinvolti |  | Visualizzazione pagina Elenco Provvedimenti Esecutivi Coinvolti |  |  |  |  |
|  | 6 | Azione | Cliccare sull'icona Dettaglio Dati Analitici presente nella colona Azioni |  | Visualizzazione pagina Gestione Dati Analitici |  |  |  |  |
|  | 7 | Azione | Cliccare sul pulsante Dati Analitici e successivamente su Benefici (disposti in sentenza) |  | Visualizzazione pagina  Elenco Benefici |  |  |  |  |
|  | 8 | Azione | Cliccare su Inserisci pena sospesa  - non menzione |  | Visualizzazione pagina  Inserimento Beneficio In Sentenza |  |  |  |  |
|  | 9 | Azione | Inserire i campi obbligatori e cliccare su Conferma |  |  |  |  |  |  |
|  | 10 | Azione | Tornare sul dettaglio dell'istruttoria, selezionare Richieste del PM |  | Visualizzazione pagina Richieste del PM |  |  |  |  |
|  | 11 | Azione | Selezionare Richieste al Giudice dell'esecuzione |  | Visualizzazione pagina Richieste del PM al GE |  |  |  |  |
|  | 12 | Azione | Selezionare Richiesta Revoca Benefici |  | Visualizazione pagina  Richieste al G.E. Revoca Benefici |  |  |  |  |
|  | 13 | Azione | Selezionare il Tipo Beneficio Sospensione Condizionale e cliccare su Conferma |  | Visualizzazione pagina Inserimento Richiesta Revoca Beneficio |  |  |  |  |
|  | 14 | Azione | Procedere alla revoca del beneficio della sospensione condizionale. |  |  |  |  |  |  |
|  | 15 | Azione | Tornare al dettaglio Istruttoria e provvedere ad effettuare la stampa dei due prospetti  Prospetto Provvedimenti coinvolti e Prospetto cumulo (proposta) |  |  |  |  |  |  |
|  | V | Verifica esterna | Verificare che i due prospetti gestiscono correttamente l'assenza della pena principale non generando l'errore della stampa dei prospetti. |  |  |  |  |  |  |
| TF015.SIEP | 01 | Verificare corretto funzionamento dello scadenzario simeone per provvedimenti di cumulo pene con sospensione per ex 656. |  | Verificare corretto funzionamento dello scadenzario simeone per provvedimenti di cumulo pene con sospensione per ex 656. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Iscrivere un fascicolo SIEP di classe I con pena detentiva. |  |  |  |  |  |  |
|  | 2 | Azione | Cliccare sull'icona  Gestione cumulo |  | Visualizzazione pagina  Gestione Cumulo |  |  |  |  |
|  | 3 | Azione | Cliccare su Apertura Istruttoria |  | Visualizzazione pagina Apertura Istruttoria Cumulo |  |  |  |  |
|  | 4 | Azione | Emettere Provvedimento di Cumulo |  |  |  |  |  |  |
|  | 5 | Azione | In Gestione Cumulo cliccare su Dati Finali Cumulo |  | Visualizzazione pagina Dati Finali Cumulo |  |  |  |  |
|  | 6 | Azione | Inserire Data Emissione e cliccare su Conferma |  | Visualizzazione pagina Dati Finali Cumulo con i vari TAB |  |  |  |  |
|  | 7 | Azione | Inserire nei vari tab la pena,la Posizione giuridica Libero, procedere al calcolo pena ed infine emettere il provvedimento "di unificazione di pene concorrenti (con contestuale Decreto di Sospensione ex art. 656 Comma 5 CPP)" e validare. |  |  |  |  |  |  |
|  | 8 | Navigazione | Ordini di Esecuzione/Scarcerazione » Sospensione Esecuzione ex art. 656 c.p.p. » Ricerca Decreti in corso di Definizione |  |  |  |  |  |  |
|  | 9 | Azione | Ricercare il provvedimento di unificazione inserito precedentemente. |  |  |  |  |  |  |
|  | V | Verifica esterna | Verificare che il fascicolo sia presente in elenco. |  |  |  |  |  |  |
|  | 10 | Navigazione | Ordini di Esecuzione/Scarcerazione » Sospensione Esecuzione ex art. 656 c.p.p. »  Gestione Decreto di Sospensione |  |  |  |  |  |  |
|  | 11 | Azione | Cliccare su Notifiche e successivamente su Difensore |  |  |  |  |  |  |
|  | 12 | Azione | Registrare la notifica all'avvocato |  |  |  |  |  |  |
|  | 13 | Navigazione | Verbali Arresto/Vane Ricerche Notifica Carcere |  |  |  |  |  |  |
|  | 14 | Azione | Cliccare su Verbale Vane Ricerche |  | Visualizzazione pagina Inserimento Verbale Vane Ricerche |  |  |  |  |
|  | 15 | Azione | Inserire il Verbale Vane Ricerche e Confermare |  |  |  |  |  |  |
|  | 16 | Navigazione | Ordini di Esecuzione/Scarcerazione » Sospensione Esecuzione ex art. 656 c.p.p. »  Gestione Decreto di Sospensione |  |  |  |  |  |  |
|  | 17 | Azione | Cliccare su Irreperibilità |  | Visualizzazione pagina Irreperibilità |  |  |  |  |
|  | 18 | Azione | Nella pagina di Irreperibilità cliccare su Decreto ed inserire il decreto |  |  |  |  |  |  |
|  | 19 | Azione | Nella pagina di Irreperibilità cliccare su Registrazione Notifica ed inserire la notifica del decreto di irreperibilità |  |  |  |  |  |  |
|  | 20 | Navigazione | Scadenzario |  |  |  |  |  |  |
|  | 21 | Azione | Cliccare su Sospensione Esecuzione ex art. 656 c.p.p. |  | Visualizzazione pagina Consultazione Scadenzario L.165/98 |  |  |  |  |
|  | 22 | Azione | Selezionare 'Tutti'. Cliccare su Ricerca |  |  |  |  |  |  |
|  | V | Verifica esterna | Verificare che il procedimento sia presente nel risultato della ricerca |  |  |  |  |  |  |

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