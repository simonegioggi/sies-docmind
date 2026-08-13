---
uniqueName: siut-sies-ct-1-0-20230224-allegatoalpianotestsiesv
displayName: "SIUT SIES CT 1 0 20230224 Allegato al piano test SIES v 12 4 27 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-CT-1.0-20230224-Allegato_al_piano_test_SIES_v.12.4.27.0

> **File originale:** `RILASCIO_12.4.27.0/SIUT-SIES-CT-1.0-20230224-Allegato_al_piano_test_SIES_v.12.4.27.0.xls`  
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
|  | Nome del file | SIUT-SIES-CT-1.0-20230224-Allegato_al_piano_test_SIES_v.12.4.27.0.xls |
|  | Piano di test | SIUT-SIES-PT-1.0-20230224-Piano_dei_Test_SIES_v.12.4.27.0.docx |
|  | Versione | 1.0 |
|  | Data | 44981.0 |
|  | Intervento | SIES v.12.4.27.0 |
|  | Area Applicativa | Penale |
|  | Allegato al Piano dei Test |  |

## TabellaTest

| Codice Area |  |  | SIES v.12.4.27.0 |  |  |  | Codifica  Piano di test |  | SIUT-SIES-CT-1.0-20230224-Allegato_al_piano_test_SIES_v.12.4.27.0.xls | Versione | 1.0 |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Applicazione |  |  | Funzionalità / Requisiti non funzionali |  |  |  |  |  |  | Caso di test |  |  |  |  |  |  |  |  |  |  |
| Codice Area | Codice Appl. | ID. Requisito | ID | Primo livello | ID | Primo Livello | Risk (1-5) | ID | Secondo livello | ID | Nome del caso di test | Classe di Gravità (1-4) | Ciclo di test | Stima Durata | Descrizione e note | Versione | N. cond. di test | Autom. | Classe di rilevanza (A, B, C) | Esito |
| SIUT | SIES | 20230125017.0 |  |  | 20230125017.0 | SIEP - Impossibile visualizzare alcuni fascicolo mediante ricerca per numero. |  | SIEP | SIEP - SIEP - Impossibile visualizzare alcuni fascicolo mediante ricerca per numero. | TF001.SIEP | Errore nella visualizzazione di un fascicolo mediante l'usuale funzione di ricerca per numero |  |  |  | Verifica: verificare che, dopo aver inserito un provvedimento di "Comunicazione Dichiarazione estinzione libertà controllata" su un fascicolo di Classe VII, quando si effettua la ricerca per numero il procedimento stesso venga visualizzato | 1.0 |  |  |  |  |
| SIUT | SIES | 202301250123.0 |  |  | 202301250123.0 | n. 30004/2021 e n. 30005/2021 SIEP CAMPOBASSO |  | SIEP | SIEP - n. 30004/2021 e n. 30005/2021 SIEP CAMPOBASSO | TF002.SIEP | Errore nella cancellazione di provvedimenti per fascicoli di classe III |  |  |  | Verifica: verificare che quando si cancellano gli eventi per il fascicolo di classe III il sistema non mostri il messaggio di errore | 1.0 |  |  |  |  |
| SIUT | SIES | 20230126014.0 |  |  | 20230126014.0 | Correzione su SIES per SIUS-Avvocati |  | SIUS | SIUS - Correzione su SIES per SIUS-Avvocati | TF001.SIUS | Errore nella ricerca di un evento di fissazione udienza depositato e validato |  |  |  | Verifica: verificare che ricercando un procedimento contenente un evento di fissazione udienza depositato e validato il sistema mostri il fascicolo con il provvedimento | 1.0 |  |  |  |  |
| SIUT | SIES | 20230201017.0 |  |  | 20230201017.0 | Anomalia Sies |  | SIUS | SIUS - Anomalia Sies | TF002.SIUS | Errore nella emissione dell'avviso per ordinanza di rinvio udienza |  |  |  | Verifica: verificare che l'avviso per una ordinanza di rinvio udienza sia visibile all'avvocato solo dopo la validazione del deposito | 1.0 |  |  |  |  |
| SIUT | SIES | 20230202011 |  |  | 20230202011 | Sige - anomalie foglio complementare |  | SIGE | SIGE - Sige - anomalie foglio complementare | TF001.SIGE | Errore nell'annotazione del foglio complementare per il sottosistema SIGE |  |  |  | Verifica: verificare che l'annotazione del foglio complementare sia conforme a quanto riportato nel documento di analisi | 1.0 |  |  |  |  |

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

| Progetto / Obiettivo Software |  |  | SIES v.12.4.27.0 |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | SIUT-SIES-CT-1.0-20230224-Allegato_al_piano_test_SIES_v.12.4.27.0.xls |  |  |  |  |  |  |
| ID caso di test | Suffisso Caso di test | Nome Caso di test
Tipo Step |  | Descrizione |  | Versione | Stima tempo | N.cond. di test | Esito |
| TF001.SIEP | SIEP | Errore nella visualizzazione di un fascicolo mediante l'usuale funzione di ricerca per numero |  | Verifica: verificare che, dopo aver inserito un provvedimento di "Comunicazione Dichiarazione estinzione libertà controllata" su un fascicolo di Classe VII, quando si effettua la ricerca per numero il procedimento stesso venga visualizzato |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come "Procura della Repubblica Presso il Tribunale Ordinario" | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione | Ricercare (od iscrivere) un procedimento di Classe VII validato e con una posizione giuridica assegnata |  |  |  |  |  |
|  | 1.0 | Navigazione | Gestione Altre Sanzioni » Conversione Pene Pecuniarie » Iscrizione Procedimento (richiesta conversione) |  | Visualizzazione pagina "Iscrizione Richiesta Conversione" |  |  |  |  |
|  | 2.0 | Azione | Riempire i campi obbligatori e premere il tasto "Conferma" |  | Visualizzazione pagina " Dettaglio Richiesta Conversione" |  |  |  |  |
|  | 3.0 | Navigazione | Gestione Altre Sanzioni » Conversione Pene Pecuniarie » Trasmissione atti per la conversione |  | Visualizzazione pagina "Trasmissione Atti per Conversione" |  |  |  |  |
|  | 4.0 | Azione | Riempire i campi obbligatori e premere il tasto "Conferma" | Destinatario: UDS Competente | Visualizzazione pagina "Dettaglio Trasmissione Richiesta Conversione" |  |  |  |  |
|  | 5.0 | Azione | Cliccare sull'icona di "Generazione Stampa" |  | Visualizzazione pagina "Dettaglio Trasmissione Richiesta Conversione" |  |  |  |  |
|  | 6.0 | Azione | Selezionare il checkbox "Valida Documento" e premere il tasto "Conferma" | Premere il tasto "OK" | Visualizzazione pagina "Dettaglio Trasmissione Richiesta Conversione" |  |  |  |  |
|  | 7.0 | Azione | Cliccare sull'icona di "Trasmissione Provvedimento" |  | Visualizzazione pagina "Trasferimento Conversione Pene Pecuniarie" |  |  |  |  |
|  | 8.0 | Azione | Riempire i campi obbligatori e premere il tasto "Conferma" | Premere il tasto "OK" | Visualizzazione pagina "Dettaglio Procedimento" |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come "Ufficio di Sorveglianza" | Exxxxx (Ufficio di Sorveglianza) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione |  |  |  |  |  |  |
|  | 9.0 | Navigazione | Presa in carico atti pervenuti » Ricerca per Atti - SIEP |  | Visualizzazione pagina "Presa in Carico - Ricerca Atti Per Estremi - SIEP" |  |  |  |  |
|  | 10.0 | Azione | Inserire i dati del fascicolo SIEP di Classe VII di cui sopra e premere il tasto "Ricerca" |  | Visualizzazione pagina "Lista Atti Ricevuti" |  |  |  |  |
|  | 11.0 | Azione | Cliccare sull'icona "Dettagli" nella colonna "Azioni" |  | Visualizzazione pagina "Dettaglio Richiesta Conversione Pene Pecuniarie Ricevuta" |  |  |  |  |
|  | 12.0 | Azione | Premere il tasto "Conferma Presa In Carico" |  | Visualizzazione pagina "Rapporto Trasferimento Atto Conversione Pene Pecuniarie" |  |  |  |  |
|  | 13.0 | Azione | Premere il tasto "Prosegui" |  | Visualizzazione pagina "Presa in carico atto pervenuto da SIEP" |  |  |  |  |
|  | 14.0 | Azione | Riempire i campi obbligatori e premere il tasto "Conferma" | Contenuto "CONVERSIONE / RATEIZZAZIONE PENA PECUNIARIA"; Oggetto "Conversione pena pecuniaria" | Visualizzazione pagina "Dettaglio Procedimento SIUS" |  |  |  |  |
|  | 15.0 | Navigazione | Ordinanze » Emissione Ordinanza |  | Visualizzazione pagina "Emissione Ordinanza" |  |  |  |  |
|  | 16.0 | Azione | Riempire i campi obbligatori e premere il tasto "Conferma" |  | Visualizzazione pagina "Emissione Ordinanza Conversione Pene Pecuniarie" |  |  |  |  |
|  | 17.0 | Azione | Riempire i campi obbligatori e premere il tasto "Conferma" | Esito "DISPONE CONVERSIONE IN LIBERTÀ CONTROLLATA", valorizzare i "Quantum Sanzione Sostitutiva" | Visualizzazione pagina "Dettaglio Ordinanza" |  |  |  |  |
|  | 18.0 | Azione | Validare l'ordinanza, depositarla, validare il deposito e trasmetterla alla Procura ed all'UDS che l'ha emessa |  | Visualizzazione pagina "Dettaglio Procedimento SIUS" |  |  |  |  |
|  | 19.0 | Navigazione | Presa in carico atti pervenuti » Ricerca per Atti - SIUS |  | Visualizzazione pagina "Presa in Carico - Ricerca Atti Per Estremi - SIUS" |  |  |  |  |
|  | 20.0 | Azione | Inserire i dati del fascicolo SIUS corrente e preme il tasto "Ricerca" |  | Visualizzazione pagina "Lista Atti Ricevuti" |  |  |  |  |
|  | 21.0 | Azione | Cliccare sull'icona "Dettagli" nella colonna "Azioni" |  | Visualizzazione pagina "Dettaglio Ordinanza Ricevuta" |  |  |  |  |
|  | 22.0 | Azione | Premere il tasto "Conferma Presa In Carico" | Ricezione Ordinanza Completata e Esito rispedito al Mittente. Iscrivere il procedimento Sius! |  |  |  |  |  |
|  | 23.0 | Azione | Premere il tasto "OK" |  | Visualizzazione pagina "Presa in carico atto pervenuto da SIEP" |  |  |  |  |
|  | 24.0 | Azione | Riempire i campi obbligatori e premere il tasto "Conferma" | Contenuto "Esecuzione Sanzione Sostitutiva"; Oggetto "Libertà Controllata" | Visualizzazione pagina "Dettaglio Procedimento SIUS" |  |  |  |  |
|  | 25.0 | Azione | Cliccare su Numero Procedimento E.S.S. - aaaa/num (Esecuzione Sanzioni Sostitutive) |  | Visualizzazione pagina "Elenco dei Procedimenti relativi all' Esecuzione della Sanzione Sostitutiva" |  |  |  |  |
|  | 26.0 | Azione | Cliccare sull'icona "Iscrizione Procedimento di Esecuzione S.S." |  | Visualizzazione pagina "Iscrizione Procedimento da Soggetto" |  |  |  |  |
|  | 27.0 | Azione | Riempire i campi obbligatori e premere il tasto "Conferma" | Contenuto "DICHIARAZIONE ESTINZIONE LIBERTÀ CONTROLLATA"; Oggetto "Dichiarazione estinzione libertà controllata" | Visualizzazione pagina "Dettaglio Procedimento SIUS" |  |  |  |  |
|  | 28.0 | Navigazione | Decreti » Emissione Decreto |  | Visualizzazione pagina "Emissione Decreto" |  |  |  |  |
|  | 29.0 | Azione | Riempire i campi obbligatori e premere il tasto "Conferma" |  | Visualizzazione pagina "Emissione Decreto Declaratoria Estinzione Sanzioni Sostitutive" |  |  |  |  |
|  | 30.0 | Azione | Riempire i campi obbligatori e premere il tasto "Conferma" | Esito "Dichiara Estinta" | Visualizzazione pagina "Dettaglio Decreto Declaratoria Estinzione Sanzioni Sostitutive" |  |  |  |  |
|  | 31.0 | Azione | Validare il decreto, depositarlo e validare il deposito |  | Visualizzazione pagina "Dettaglio Deposito Decreto" |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come "Procura della Repubblica Presso il Tribunale Ordinario" | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione | Ricercare il procedimento di Classe VII di cui al punto 1 |  |  |  |  |  |
|  | 32.0 | Navigazione | Gestione Altre Sanzioni » Conversione Pene Pecuniarie » Decisioni Ufficio Sorveglianza |  | Visualizzazione pagina "ANNOTAZIONE PROVVEDIMENTI DECISIONI SORVEGLIANZA" |  |  |  |  |
|  | 33.0 | Azione | Cliccare sul link "Seleziona provvedimento di Sorveglianza dalla lista" | Selezionare il "Decreto di Dichiarazione estinzione libertà controllata" | Visualizzazione pagina "ANNOTAZIONE PROVVEDIMENTI DECISIONI SORVEGLIANZA" |  |  |  |  |
|  | 34.0 | Azione | Riempire i campi obbligatori e premere il tasto "Conferma" |  | Visualizzazione pagina "Dettaglio Annotazione Provvedimento Decisioni Sorveglianza" |  |  |  |  |
|  | 35.0 | Azione | Cliccare sull'icona di "Upload Stampa" |  | Visualizzazione pagina "Dettaglio Annotazione Provvedimento Decisioni Sorveglianza" |  |  |  |  |
|  | 36.0 | Azione | Selezionare il checkbox "Valida Documento" e premere il tasto "Conferma" | Premere il tasto "OK" | Visualizzazione pagina "Dettaglio Annotazione Provvedimento Decisioni Sorveglianza" |  |  |  |  |
|  | 37.0 | Navigazione | Ricerca Procedimento |  | Visualizzazione pagina "Ricerca Procedimento" |  |  |  |  |
|  | 38.0 | Azione | Riempire i campi obbligatori e premere il tasto "Conferma" | Ricercare il procedimento di Classe VII di cui ai punti 1 e 32 | Visualizzazione pagina "Dettaglio Procedimento" |  |  |  |  |
|  | V | Verifica | Verificare che il sistema presenti la pagina di dettaglio del procedimento e non il messaggio "Nessun elemento trovato" | Stato del Procedimento "Validato" |  |  |  |  |  |
| TF002.SIEP | SIEP | Errore nella cancellazione di provvedimenti per fascicoli di classe III |  | Verifica: verificare che quando si cancellano gli eventi per il fascicolo di classe III il sistema non mostri il messaggio di errore |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come "Procura della Repubblica Presso il Tribunale per i Minorenni" | Bxxxxx (Procura della Repubblica Presso il Tribunale per i Minorenni) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione | Ricercare (od iscrivere) un procedimento di Classe III validato |  |  |  |  |  |
|  | 1.0 | Navigazione | Gestione Pene Sospese » Richieste » Revoca beneficio ex art 168 c.p - 674 c.p.p. |  | Visualizzazione pagina "Inserimento Richiesta Revoca Beneficio ex art.168 c.p. - 674 c.p.p." |  |  |  |  |
|  | 2.0 | Azione | Selezionare i link "Iscrizione Reati" e "Pena Complessiva", riempire i campi obbligatori e premere il tasto "Conferma" |  |  |  |  |  |  |
|  | 3.0 | Azione | Riempire i campi obbligatori e premere il tasto "Conferma" |  | Visualizzazione pagina "Dettaglio Richiesta Revoca Beneficio ex art.168 c.p. - 674 c.p.p." |  |  |  |  |
|  | 4.0 | Azione | Cliccare sull'icona di "Valida Provvedimento" | Premere "OK" | Visualizzazione pagina "Dettaglio Richiesta Revoca Beneficio ex art.168 c.p. - 674 c.p.p." |  |  |  |  |
|  | 5.0 | Azione | Cliccare sull'icona di "Elenco Provvedimenti del PM" |  | Visualizzazione pagina "Elenco Provvedimenti PM" |  |  |  |  |
|  | 6.0 | Azione | Cliccare sull'icona "Cancella" |  | Visualizzazione pagina "Elenco Provvedimenti PM" |  |  |  |  |
|  | V | Verifica | Verificare che la cancellazione vada a buon fine e non presenti il messaggio di errore |  |  |  |  |  |  |
| TF001.SIUS | SIUS | Errore nella ricerca di un evento di fissazione udienza depositato e validato |  | Verifica: verificare che ricercando un procedimento contenente un evento di fissazione udienza depositato e validato il sistema mostri il fascicolo con il provvedimento |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIUS come "Tribunale di Sorveglianza" | Dxxxxx (Tribunale di Sorveglianza) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione | Iscrivere un procedimento, fissare una udienza, validarla, depositarla e validare il deposito |  |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente ha effettuato l'accesso all’applicazione di Consultazione Procedimenti e avvisi SIUS tramite PST | Login; Password; Codice Fiscale Avvocato |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione |  |  |  |  |  |  |
|  | 1.0 | Navigazione | Ricerche » Dati Soggetto |  | Visualizzazione pagina "Ricerca Soggetti con Procedimenti di Sorveglianza" |  |  |  |  |
|  | 2.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Cerca" | Il soggetto da ricercare è lo stesso del fascicolo SIUS di cui sopra | Visualizzazione pagina "Elenco Soggetti con Procedimenti" |  |  |  |  |
|  | 3.0 | Azione | L'utente clicca, nella sezione dei soggetti trovati, colonna "N. Fascicoli SIUS", l'utente clicca sul link "Numero" |  | Visualizzazione pagina "Elenco Procedimenti per Soggetto" |  |  |  |  |
|  | 4.0 | Azione | L'utente clicca, nella sezione dei risultati trovati, colonna "N. SIUS", l'utente clicca sul link "Anno/Numero" | Il procedimento è quello con il decreto di fissaione udienza di cui sopra |  |  |  |  |  |
|  | V | Verifica | Verificare che la ricerca vada a buon fine e non appaia la dicitura "Nessun Risultato" |  | Visualizzazione pagina "Dettaglio Procedimento" |  |  |  |  |
|  | 5.0 | Navigazione | Ricerche » Estremi Procedimento |  | Visualizzazione pagina "Ricerca Procedimenti di Sorveglianza" |  |  |  |  |
|  | 6.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Cerca" | Il procedimento da ricercare è lo stesso di cui sopra |  |  |  |  |  |
|  | V | Verifica | Verificare che la ricerca vada a buon fine e non appaia la dicitura "Nessun Procedimento Trovato" |  | Visualizzazione pagina "Dettaglio Procedimento" |  |  |  |  |
| TF002.SIUS | SIUS | Errore nella emissione dell'avviso per ordinanza di rinvio udienza |  | Verifica: verificare che l'avviso per una ordinanza di rinvio udienza sia visibile all'avvocato solo dopo la validazione del deposito |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIUS come "Tribunale di Sorveglianza" | Dxxxxx (Tribunale di Sorveglianza) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione | Iscrivere un procedimento, fissare una udienza, ed emettere una ordinanza di Rinvio Udienza e validarla |  |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente ha effettuato l'accesso all’applicazione di Consultazione Procedimenti e avvisi SIUS tramite PST | Login; Password; Codice Fiscale Avvocato |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione |  |  |  |  |  |  |
|  | 1.0 | Navigazione | CONSULTAZIONE » Consultazione avvisi » Avvisi |  | Visualizzazione pagina "Ricerca Avvisi" |  |  |  |  |
|  | 2.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Ricerca" |  | Visualizzazione pagina "Elenco Avvisi" |  |  |  |  |
|  | V | Verifica | Verificare che per l'ordinanza di rinvio udienza validata l'avviso NON venga visualizzato |  |  |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIUS come "Tribunale di Sorveglianza" | Dxxxxx (Tribunale di Sorveglianza) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione | Depositare e validare il deposito dell'ordinanza di Rinvio Udienza di cui sopra |  |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente ha effettuato l'accesso all’applicazione di Consultazione Procedimenti e avvisi SIUS tramite PST (portale servizi telematici) | Login; Password; Codice Fiscale Avvocato |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione |  |  |  |  |  |  |
|  | 3.0 | Navigazione | CONSULTAZIONE » Consultazione avvisi » Avvisi |  | Visualizzazione pagina "Ricerca Avvisi" |  |  |  |  |
|  | 4.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Ricerca" |  | Visualizzazione pagina "Elenco Avvisi" |  |  |  |  |
|  | V | Verifica | Verificare che per l'ordinanza di rinvio udienza validata, depositata e con deposito validato, l'avviso venga visualizzato |  |  |  |  |  |  |
| TF001.SIGE | SIGE | Errore nell'annotazione del foglio complementare per il sottosistema SIGE |  | Verifica: verificare che l'annotazione del foglio complementare sia conforme a quanto riportato nel documento di analisi |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIGE come "Tribunale Ordinario" | Txxxxx (Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione | Ricercare (od Iscrivere) un procedimento (con provvedimenti) definito |  |  |  |  |  |
|  | 1.0 | Azione | L'utente clicca sull'icona del menù orizzontale "Foglio Complementare" |  | Visualizzazione pagina "Compilazione Foglio Complementare" |  |  |  |  |
|  | 2.0 | Azione | L'utente clicca, nella colonna "Azioni", sull'icona di "Inserimento Foglio Complementare" |  | Visualizzazione pagina "Inserimento Foglio Complementare" |  |  |  |  |
|  | 3.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Conferma" |  | Visualizzazione pagina "Dettaglio Foglio Complementare" |  |  |  |  |
|  | V | Verifica | Verificare che nella sezione "Estremi Provvedimento" i dati riportati siano conformi a quanto inserito |  |  |  |  |  |  |
|  | 4.0 | Navigazione | Monitoraggio/Ricerche/Estrazione Dati » Ricerche Fogli Complementari |  | Visualizzazione pagina "Statistiche Fogli Complementari" |  |  |  |  |
|  | 5.0 | Azione | L'utente riempie i campi obbligatori, e preme il pulsante "Conferma" | Tipologia foglio Complementare: Tutti | Visualizzazione pagina "Elenco Fogli Complementari" |  |  |  |  |
|  | 6.0 | Azione | L'utente clicca sull'icona del menù orizzontale "Stampa Excel" |  | Download del file "Documento.xls" |  |  |  |  |
|  | V | Verifica | Verificare che la stampa prodotta sia conforme a quanto riportato nel documento di analisi |  |  |  |  |  |  |

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