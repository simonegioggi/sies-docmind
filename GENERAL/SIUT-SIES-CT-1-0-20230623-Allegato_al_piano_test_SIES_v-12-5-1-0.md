---
uniqueName: siut-sies-ct-1-0-20230623-allegatoalpianotestsiesv
displayName: "SIUT SIES CT 1 0 20230623 Allegato al piano test SIES v 12 5 1 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-CT-1.0-20230623-Allegato_al_piano_test_SIES_v.12.5.1.0

> **File originale:** `RILASCIO_12.5.1.0/SIUT-SIES-CT-1.0-20230623-Allegato_al_piano_test_SIES_v.12.5.1.0.xls`  
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
|  | Nome del file | SIUT-SIES-CT-1.0-20230623-Allegato_al_piano_test_SIES_v.12.5.1.0.xls |
|  | Piano di test | SIUT-SIES-PT-1.0-20230623-Piano_dei_Test_SIES_v.12.5.1.0.docx |
|  | Versione | 1.0 |
|  | Data | 45100.0 |
|  | Intervento | SIES v.12.5.1.0 |
|  | Area Applicativa | Penale |
|  | Allegato al Piano dei Test |  |

## TabellaTest

| Codice Area |  |  | SIES v.12.5.1.0 |  |  |  | Codifica  Piano di test |  | SIUT-SIES-CT-1.0-20230623-Allegato_al_piano_test_SIES_v.12.5.1.0.xls | Versione | 1.0 |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Applicazione |  |  | Funzionalità / Requisiti non funzionali |  |  |  |  |  |  | Caso di test |  |  |  |  |  |  |  |  |  |  |
| Codice Area | Codice Appl. | ID. Requisito | ID | Primo livello | ID | Primo Livello | Risk (1-5) | ID | Secondo livello | ID | Nome del caso di test | Classe di Gravità (1-4) | Ciclo di test | Stima Durata | Descrizione e note | Versione | N. cond. di test | Autom. | Classe di rilevanza (A, B, C) | Esito |
| SIUT | SIES | 20230224014.0 |  |  | 20230224014.0 | errata stampa su dettaglio ruolo udienza |  | SIGE | SIGE - errata stampa su dettaglio ruolo udienza | TF001.SIGE | Errore nella stampa del template di dettaglio ruolo udienza |  |  |  | Verifica: verificare che nella stampa del dettaglio ruolo udienza non vengano riportati tutti i fascicoli del Magistrato ma solo quello selezionato | 1.0 |  |  |  |  |
| SIUT | SIES | 202302280124.0 |  |  | 202302280124.0 | estrazione classe IV. Singolo anno contro vari anni |  | SIEP | SIEP - estrazione classe IV. Singolo anno contro vari anni | TF001.SIEP | Errore nella statistica dei fascicoli di classe IV |  |  |  | Verifica: verificare che per la statistica di classe IV i dati estratti siano coerenti | 1.0 |  |  |  |  |
| SIUT | SIES | 20230302017.0 |  |  | 20230302017.0 | SIES per SIUS-Avvocati - (legato a 20230201017 o a 20230126014) URGENTE |  | SIUS | SIUS - SIES per SIUS-Avvocati - (legato a 20230201017 o a 20230126014) URGENTE | TF001.SIUS | Errore nella visualizzazione del procedimento senza magistrato |  |  |  | Verifica: verificare che la ricerca del procedimento senza magistrato vada a buon fine | 1.0 |  |  |  |  |
| SIUT | SIES | 20230328019.0 |  |  | 20230328019.0 | SIEP : Data visualizzata Istanza non corretta |  | SIEP | SIEP - SIEP : Data visualizzata Istanza non corretta | TF002.SIEP | Errore nella visualizzazione della data di presentazione istanza |  |  |  | Verifica: verificare che per la data di presentazione istanza sia visualizzata la data corretta e non la data di sistema | 1.0 |  |  |  |  |
| SIUT | SIES | 20230405011.0 |  |  | 20230405011.0 | Apertura Ticket su Sies Tribunale Sorveglianza Roma per Sius Avvocati |  | SIUS | SIUS - Apertura Ticket su Sies Tribunale Sorveglianza Roma per Sius Avvocati | TF002.SIUS | Errore nella visualizzazione del procedimento |  |  |  | Verifica: verificare che la ricerca del procedimento vada a buon fine | 1.0 |  |  |  |  |
| SIUT | SIES | 20230419018.0 |  |  | 20230419018.0 | RITM0352453 - SIUS - Sheet names must not begin or end with (') |  | SIUS | SIUS - RITM0352453 - SIUS - Sheet names must not begin or end with (') | TF003.SIUS | Errore nella produzione del file Excel delle statistiche comparate dei Magistrati |  |  |  | Verifica: verificare che per la statistica comparata dei Magistrati venga prodotto il file Excel | 1.0 |  |  |  |  |
| SIUT | SIES | 202304210120.0 |  |  | 202304210120.0 | SIUS 2023/2395 - UDS SALERNO |  | SIUS | SIUS - SIUS 2023/2395 - UDS SALERNO | TF004.SIUS | Errore nella validazione del decreto |  |  |  | Verifica: verificare che la validazione del decreto per il procedimento con oggetto "SEMILIBERTA' - Modifica attività lavorativa" non presenti più il messaggio di errore ma vada a buon fine | 1.0 |  |  |  |  |
| SIUT | SIES | 20230427016.0 |  |  | 20230427016.0 | Assegnazione Magistrato su P.P SIGE |  | SIGE | SIGE - Assegnazione Magistrato su P.P SIGE | TF002.SIGE | Errore nell'inserimento del nominativo di un Magistrato |  |  |  | Verifica: verificare che l'inserimento del Magistrato in questione vada a buon fine invece di presentare il messaggio di errore bloccante | 1.0 |  |  |  |  |
| SIUT | SIES | 202305050125.0 |  |  | 202305050125.0 | richiesta pervenuta da Santa Maria Capua Vetere |  | SIUS | SIUS - richiesta pervenuta da Santa Maria Capua Vetere | TF005.SIUS | Errore nella valorizzazione del campo "Data Restituzione" |  |  |  | Verifica: verificare che per le "Richieste Istruttorie" la "Data Restituzione" sia valorizzata correttamente | 1.0 |  |  |  |  |
| SIUT | SIES | 202305250112.0 |  |  | 202305250112.0 | SIUS UDS MASSA-scadenziario indica anche i procedimenti dell'UDS di Genova |  | SIUS | SIUS - SIUS UDS MASSA-scadenziario indica anche i procedimenti dell'UDS di Genova | TF006.SIUS | Errore nella gestione dello scadenzario |  |  |  | Verifica: verificare che i procedimenti visualizzati nello scadenzario siano solo quelli dell'ufficio che effettua la ricerca | 1.0 |  |  |  |  |

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

| Progetto / Obiettivo Software |  |  | SIES v.12.5.1.0 |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | SIUT-SIES-CT-1.0-20230623-Allegato_al_piano_test_SIES_v.12.5.1.0.xls |  |  |  |  |  |  |
| ID caso di test | Suffisso Caso di test | Nome Caso di test
Tipo Step |  | Descrizione |  | Versione | Stima tempo | N.cond. di test | Esito |
| TF001.SIGE | SIGE | Errore nella stampa del template di dettaglio ruolo udienza | 23 | Verifica: verificare che nella stampa del dettaglio ruolo udienza non vengano riportati tutti i fascicoli del Magistrato ma solo quello selezionato |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIGE come "Tribunale Ordinario" | Txxxxx (Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione |  |  |  |  |  |  |
|  | 4.0 | Navigazione | Udienze/Fissazione/Rinvio/Ruolo » Dettaglio Ruolo » Per Data |  | Visualizzazione pagina "Visualizza Procedimenti fissati per Udienza" |  |  |  |  |
|  | 5.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Conferma" | Tipo rito: Monocratico; inserire una "Data Udienza" che restituisca più di un risultato | Visualizzazione pagina "Elenco Procedimenti Fissati all'Udienza del gg-mm-aaaa" |  |  |  |  |
|  | 6.0 | Azione | L'utente, nella colonna "Stampa Verbale", clicca sull'icona "Stampa Verbale Udienza" di uno qualsiasi dei procedimenti restituito dalla ricerca |  | Download del file "Documento.rtf" |  |  |  |  |
|  | V | Verifica | Verificare che il template prodotto contenga la stampa del solo procedimento selezionato |  |  |  |  |  |  |
| TF001.SIEP | SIEP | Errore nella statistica dei fascicoli di classe IV | 23 | Verifica: verificare che per la statistica di classe IV i dati estratti siano coerenti |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come "Procura della Repubblica Presso il Tribunale Ordinario" | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione |  |  |  |  |  |  |
|  | 1.0 | Navigazione | Statistiche/Monitoraggio » Statistiche - Estrazione Dati » Classe IV » Procedimenti Pendenti nel Periodo |  | Visualizzazione pagina "STATISTICHE - ESTRAZIONE DATI" |  |  |  |  |
|  | 2.0 | Azione | Premere il tasto "Conferma" |  | Visualizzazione pagina "RICERCA PROCEDIMENTI CLASSE IV" |  |  |  |  |
|  | 3.0 | Azione | Inserire un intervallo di date di interesse e premere il tasto "Conferma" | Come esempio, selezionare come "Intervallo Date" un periodo a cavallo di più anni (01/01/2013 - 31/12/2023) | Elaborazione documento Excel |  |  |  |  |
|  | 4.0 | Azione | Inserire un intervallo di date di interesse e premere il tasto "Conferma" | Come esempio, selezionare come "Intervallo Date" un periodo di un singolo anno (01/01/2017 - 31/12/2017) | Elaborazione documento Excel |  |  |  |  |
|  | V | Verifica | Verificare che nel file prodotto "Documento.xls" i dati siano coerenti |  | Il risultato atteso è che sul primo foglio, "Riepilogo Procedimenti Pendenti", ci sia coerenza tra i pendenti fine periodo di un anno ed i pendenti inizio periodo dell'anno successivo. Inoltre, sul singolo anno i pendenti fine periodo siano coerenti con gli altri dati (pendenti inizio periodo + sopravvenuti nel periodo - esauriti nel periodo = pendenti fine periodo) |  |  |  |  |
| TF001.SIUS | SIUS | Errore nella visualizzazione del procedimento senza magistrato | 23 | Verifica: verificare che la ricerca del procedimento senza magistrato vada a buon fine |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIUS come "Tribunale di Sorveglianza" | Dxxxxx (Tribunale di Sorveglianza) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione | Iscrivere o ricercare un fascicolo in stato iscritto; NON associare un magistrato relatore;  inserire un decreto di fissazione udienza (e dopo eventualmente anche un rinvio udienza da verbale) | Fascicolo "YYYY/TDS1" |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente ha effettuato l'accesso all’applicazione di Consultazione Procedimenti e avvisi SIUS tramite PST | Login; Password; Codice Fiscale Avvocato |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione |  |  |  |  |  |  |
|  | 1.0 | Navigazione | Ricerche » Dati Soggetto |  | Visualizzazione pagina "Ricerca Soggetti con Procedimenti di Sorveglianza" |  |  |  |  |
|  | 2.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Cerca" | Il soggetto da ricercare è lo stesso del fascicolo "YYYY/TDS1" | Visualizzazione pagina "Elenco Soggetti con Procedimenti" |  |  |  |  |
|  | 3.0 | Azione | L'utente clicca, nella sezione dei soggetti trovati, colonna "N. Fascicoli SIUS", l'utente clicca sul link "Numero" |  | Visualizzazione pagina "Elenco Procedimenti per Soggetto" |  |  |  |  |
|  | 4.0 | Azione | L'utente clicca, nella sezione dei risultati trovati, colonna "N. SIUS", l'utente clicca sul link "Anno/Numero" | Il procedimento è il "YYYY/TDS1" |  |  |  |  |  |
|  | V | Verifica | Verificare che la ricerca vada a buon fine ed il fascicolo sia visualizzato correttamente |  | Visualizzazione pagina "Dettaglio Procedimento" |  |  |  |  |
|  | 5.0 | Navigazione | Ricerche » Estremi Procedimento |  | Visualizzazione pagina "Ricerca Procedimenti di Sorveglianza" |  |  |  |  |
|  | 6.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Cerca" | Il procedimento è il "YYYY/TDS1" |  |  |  |  |  |
|  | V | Verifica | Verificare che la ricerca vada a buon fine ed il fascicolo sia visualizzato correttamente |  | Visualizzazione pagina "Dettaglio Procedimento" |  |  |  |  |
| TF002.SIEP | SIEP | Errore nella visualizzazione della data di presentazione istanza | 23 | Verifica: verificare che per la data di presentazione istanza sia visualizzata la data corretta e non la data di sistema |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come "Procura della Repubblica Presso il Tribunale Ordinario" | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione | L'utente seleziona un fascicolo in stato NON archiviato |  |  |  |  |  |
|  | 1.0 | Navigazione | Istanze » Iscrizione Istanza » Iscrizione Istanza per Procedimento SIEP |  | Visualizzazione pagina "Iscrizione Istanza per Procedimento SIEP" |  |  |  |  |
|  | 2.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Conferma" | Annotarsi la data inserita nel campo "Pervenuta in data" | Visualizzazione pagina "Dettaglio Procedimento" |  |  |  |  |
|  | V | Verifica | Verificare che per la data di presentazione istanza sia visualizzata la data corretta e non la data di sistema |  | Il risultato atteso è che nella pagina di dettaglio del fascicolo sia riportata la dicitura "Presentata Istanza il : " con la data inserita nel campo "Pervenuta in data" |  |  |  |  |
| TF002.SIUS | SIUS | Errore nella visualizzazione del procedimento | 23 | Verifica: verificare che la ricerca del procedimento vada a buon fine |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente ha effettuato l'accesso all’applicazione di Consultazione Procedimenti e avvisi SIUS tramite PST | Login; Password; Codice Fiscale Avvocato |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione | Iscrivere o ricercare un fascicolo di "Concessione Misure Sicurezza - Semilibertà" completare fino al deposito dell'ordinanza di concessione. |  |  |  |  |  |
|  | 1.0 | Navigazione | Ricerche » Dati Soggetto |  | Visualizzazione pagina "Ricerca Soggetti con Procedimenti di Sorveglianza" |  |  |  |  |
|  | 2.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Cerca" | I soggetti da ricercare sono gli stessi dei fascicoli di cui sopra | Visualizzazione pagina "Elenco Soggetti con Procedimenti" |  |  |  |  |
|  | 3.0 | Azione | L'utente clicca, nella sezione dei soggetti trovati, colonna "N. Fascicoli SIUS", l'utente clicca sul link "Numero" |  | Visualizzazione pagina "Elenco Procedimenti per Soggetto" |  |  |  |  |
|  | 4.0 | Azione | L'utente clicca, nella sezione dei risultati trovati, colonna "N. SIUS", l'utente clicca sul link "Anno/Numero" | I fascicoli da ricercare sono gli stessi di cui sopra |  |  |  |  |  |
|  | V | Verifica | Verificare che la ricerca vada a buon fine ed il fascicolo sia visualizzato correttamente |  | Visualizzazione pagina "Dettaglio Procedimento" |  |  |  |  |
|  | 5.0 | Navigazione | Ricerche » Estremi Procedimento |  | Visualizzazione pagina "Ricerca Procedimenti di Sorveglianza" |  |  |  |  |
|  | 6.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Cerca" | I fascicoli da ricercare sono gli stessi di cui sopra |  |  |  |  |  |
|  | V | Verifica | Verificare che la ricerca vada a buon fine ed il fascicolo sia visualizzato correttamente |  | Visualizzazione pagina "Dettaglio Procedimento" |  |  |  |  |
| TF003.SIUS | SIUS | Errore nella produzione del file Excel delle statistiche comparate dei Magistrati | 23 | Verifica: verificare che per la statistica comparata dei Magistrati venga prodotto il file Excel |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIUS come "Tribunale di Sorveglianza" | Dxxxxx (Tribunale di Sorveglianza) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione |  |  |  |  |  |  |
|  | 1.0 | Navigazione | Statistiche/Monitoraggio » Statistica Comparata Magistrati |  | Visualizzazione pagina "Comparazione Attività Magistrati per Oggetto" |  |  |  |  |
|  | 2.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Ricerca" | Scegliere GATTELLI MARILU' come magistrato da comparare | Visualizzazione pagina "Statistica Comparata Magistrati per Specifici Oggetti" |  |  |  |  |
|  | 3.0 | Azione | L'utente clicca sull'icona "Stampa Excel" |  | Elaborazione documento Excel |  |  |  |  |
|  | V | Verifica | Verificare che il foglio Excel venga prodotto |  | Il risultato atteso è che il nome delle schede non contenga l'apostrofo dell'accentata del nome del magistrato come ultima lettera |  |  |  |  |
| TF004.SIUS | SIUS | Errore nella validazione del decreto | 23 | Verifica: verificare che la validazione del decreto per il procedimento con oggetto "SEMILIBERTA' - Modifica attività lavorativa" non presenti più il messaggio di errore ma vada a buon fine |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIUS come "Tribunale di Sorveglianza" | Dxxxxx (Tribunale di Sorveglianza) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione | Iscrivere o ricercare un fascicolo di "Concessione Misure Alternative Alla Detenzione - Semilibertà" in cui sia presente l'ordinanza di concessione validata, depositata e validato il deposito | Creazione fascicolo 2023/tds1 |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIUS come "Ufficio di Sorveglianza" | Exxxxx (Ufficio di Sorveglianza) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione | Iscrivere un fascicolo di "Esecuzione Misure Alternative - Semilibertà" | Creazione fascicolo 2023/uds1 |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione | Iscrivere un fascicolo di "Semiliberta' - Modifica Attività Lavorativa - Modifica Attività Lavorativa" collegandolo al fascicolo 2023/uds1 | Creazione fascicolo 2023/uds2 |  |  |  |  |
|  | 1.0 | Navigazione | Assegnazione Difensore |  | Visualizzazione pagina "Inserimento Difensore" |  |  |  |  |
|  | 2.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Conferma" |  | Visualizzazione pagina "Dettaglio Avvocato" |  |  |  |  |
|  | 3.0 | Navigazione | Decreti » Emissione Decreto |  | Visualizzazione pagina "Emissione Decreto" |  |  |  |  |
|  | 4.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Conferma" |  | Visualizzazione pagina "Emissione Decreto di Modifica Attività Lavorativa" |  |  |  |  |
|  | 5.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Conferma" |  | Visualizzazione pagina "Dettaglio Decreto di Modifica Attività Lavorativa" |  |  |  |  |
|  | 6.0 | Azione | L'utente dopo aver premuto il tasto "Upload Stampa" per la validazione del decreto, riempie i campi obbligatori, e preme il pulsante "Conferma" |  | Visualizzazione pagina "Dettaglio Decreto di Modifica Attività Lavorativa" |  |  |  |  |
|  | V | Verifica | Verificare che nella pagina di dettaglio decreto i due avvocati siano visualizzati correttamente |  |  |  |  |  |  |
| TF002.SIGE | SIGE | Errore nell'inserimento del nominativo di un Magistrato | 23 | Verifica: verificare che l'inserimento del Magistrato in questione vada a buon fine invece di presentare il messaggio di errore bloccante |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIGE come "Tribunale Ordinario" | Txxxxx (Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione | Ricercare magistrato che compare come procuratore su una udienza di un altro ufficio e che non sia tra i magistrati dell'ufficio stesso.
SELECT DISTINCT MAGISTRATO.NOME, MAGISTRATO.COGNOME
FROM UDIENZA_SIGE, MAGISTRATO
WHERE 1=1
AND UDIENZA_SIGE.COD_PROCURATORE = MAGISTRATO.COD_MAGISTRATO
AND MAGISTRATO.COD_UFFICIO_APPARTENENZA <> 'cod_ufficio' |  |  |  |  |  |
|  | 4.0 | Navigazione | Funzioni Amministrative » Gestione Magistrati » Inserisci Magistrato |  | Visualizzazione pagina "Inserimento di un Magistrato" |  |  |  |  |
|  | 5.0 | Azione | L'utente preme il pulsante "Seleziona dalla Lista" | Scegliere il Magistrato ricercato in precedenza | Visualizzazione popup di ricerca Magistrato |  |  |  |  |
|  | 6.0 | Azione | L'utente preme il pulsante "Conferma" |  | Visualizzazione pagina "Dettaglio Magistrato" |  |  |  |  |
|  | V | Verifica | Verificare che l'inserimento del Magistrato vada a buon fine e non presenti il messaggio di errore |  | Visualizzazione pagina "Dettaglio Magistrato" |  |  |  |  |
| TF005.SIUS | SIUS | Errore nella valorizzazione del campo "Data Restituzione" | 23 | Verifica: verificare che per le "Richieste Istruttorie" la "Data Restituzione" sia valorizzata correttamente |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIUS come "Tribunale di Sorveglianza" | Dxxxxx (Tribunale di Sorveglianza) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione | Iscrivere o ricercare un procedimento in stato iscritto; seguire il percorso "Fase istruttoria » Richiesta Atti" e scegliere, per esempio, la voce "Certificato Casellario"; riempire i campi obbligatori e confermare; seguire il percorso "Fase istruttoria » Stato Atti Richiesti / Solleciti" ed inserire una "Data Restituzione" e confermare. | Fascicolo "YYYY/TDS1" |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente ha effettuato l'accesso all’applicazione di Consultazione Procedimenti e avvisi SIUS tramite PST | Login; Password; Codice Fiscale Avvocato |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione |  |  |  |  |  |  |
|  | 1.0 | Navigazione | Ricerche » Dati Soggetto |  | Visualizzazione pagina "Ricerca Soggetti con Procedimenti di Sorveglianza" |  |  |  |  |
|  | 2.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Cerca" | Il soggetto da ricercare è lo stesso del fascicolo SIUS di cui sopra | Visualizzazione pagina "Elenco Soggetti con Procedimenti" |  |  |  |  |
|  | 3.0 | Azione | L'utente clicca, nella sezione dei soggetti trovati, colonna "N. Fascicoli SIUS", l'utente clicca sul link "Numero" |  | Visualizzazione pagina "Elenco Procedimenti per Soggetto" |  |  |  |  |
|  | 4.0 | Azione | L'utente clicca, nella sezione dei risultati trovati, colonna "N. SIUS", l'utente clicca sul link "Anno/Numero" | Il procedimento è il "YYYY/TDS1" |  |  |  |  |  |
|  | V | Verifica | Verificare che la ricerca vada a buon fine e, nella sezione "Richiesta Istruttorie", i campi "Data Richiesta" e "Data Restituzione" siano entrambi visibili e valorizzati correttamente |  | Visualizzazione pagina "Dettaglio Procedimento" |  |  |  |  |
|  | 5.0 | Navigazione | Ricerche » Estremi Procedimento |  | Visualizzazione pagina "Ricerca Procedimenti di Sorveglianza" |  |  |  |  |
|  | 6.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Cerca" | Il procedimento è il "YYYY/TDS1" |  |  |  |  |  |
|  | V | Verifica | Verificare che la ricerca vada a buon fine e, nella sezione "Richiesta Istruttorie", i campi "Data Richiesta" e "Data Restituzione" siano entrambi visibili e valorizzati correttamente |  | Visualizzazione pagina "Dettaglio Procedimento" |  |  |  |  |
| TF006.SIUS | SIUS | Errore nella gestione dello scadenzario |  | Verifica: verificare che i procedimenti visualizzati nello scadenzario siano solo quelli dell'ufficio che effettua la ricerca |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIUS come "Ufficio di Sorveglianza" | Exxxxx (Ufficio di Sorveglianza) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione |  |  |  |  |  |  |
|  | 1.0 | Navigazione | Scadenzari » Consultazione Scadenzari |  | Visualizzazione pagina "Consultazione Scadenzari" |  |  |  |  |
|  | 2.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Ricerca" | Selezionare la voce "Termine sanzione sostitutiva" ed "In scadenza entro: Anni  2" | Visualizzazione pagina "Consultazione Scadenzario di Termine Sanzione Sostitutiva - Criterio: In Scadenza" |  |  |  |  |
|  | V | Verifica | Verificare che la ricerca vada a buon fine e che i procedimenti estratti siano solo quelli dell'ufficio dell'utente connesso |  |  |  |  |  |  |

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