---
uniqueName: siut-sies-ct-1-0-20200110-allegato-al-piano-test
displayName: "SIUT SIES CT 1 0 20200110 Allegato al piano test"
category: "GENERAL"
tags: []
---

# SIUT-SIES-CT-1.0-20200110-Allegato-al-piano-test

> **File originale:** `RILASCIO_11.2.4/SIUT-SIES-CT-1.0-20200110-Allegato-al-piano-test.xls`  
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
|  | SIUT-SIES-CT-1.0-20200110-Allegato-al-piano-test.xls |
|  | Piano di test |
|  | Ver. 1.0 |
|  | Data: 10/01/2020 |
|  | SIUT |
|  | SIES 11.2.4 |
|  | Allegato al Piano dei Test |

## TabellaTest

| Codice Area |  |  | SIUT |  |  |  | Codifica  Piano di test |  | SIUT-SIES-CT-1.0-20200110-Allegato-al-piano-test.xls | Versione | Ver. 1.0 |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Applicazione |  |  | Funzionalità / Requisiti non funzionali |  |  |  |  |  |  | Caso di test |  |  |  |  |  |  |  |  |  |  |
| Codice Area | Codice Appl. | ID. Requisito | ID | Primo livello | ID | Primo Livello | Risk (1-5) | ID | Secondo livello | ID | Nome del caso di test | Classe di Gravità (1-4) | Ciclo di test | Stima Durata | Descrizione e note | Versione | N. cond. di test | Autom. | Classe di rilevanza (A, B, C) | Esito |
| SIUT | SIES | 20191129017 |  |  | 20191129017 | Rideterminazione Pena |  | SIEP | SIEP - Procura della Repubblica presso il Tribunale dei Minori - Rideterminazione Pena | TF001.SIEP | Verifica form dell'Ordine di scarcerazione per Rideterminazione pena |  |  |  | Verifica: verificare che sia stata personalizzata per i minori la form dell'Ordine di scarcerazione per Rideterminazione pena | 1.0 |  |  |  |  |
| SIUT | SIES | 201912040112 |  |  | 201912040112 | Definizione Procedimento - Provvedimento Sorveglianza |  | SIEP | SIEP - Procura della Repubblica presso il Tribunale dei Minori | TF002.SIEP | Verifica generazione del template |  |  |  | Verifica: verificare che venga generato il template relativo all'inserimento manuale di un provvedimento della sorveglianza | 1.0 |  |  |  |  |
| SIUT | SIES | 20191202018.0 |  |  | 20191202018 | Conversione Pena Pecuniaria |  | SIEP | SIEP - Procura della Repubblica presso il Tribunale Ordinario | TF003.SIEP | Verifica conversione di un procedimento da Classe II a Classe VII |  |  |  | Verifica: Verificare l'avvenuta operazione di conversione di un procedimento SIEP da classe II a classe VII | 1.0 |  |  |  |  |
| SIUT | SIES | 201911260116 |  |  | 201911260116 | Annullamento Provvedimento di cumulo |  | SIEP | SIEP - Anomalia su provvedimento "non validato" | TF004.SIEP | Verifica dell'impossibilità di annullare un provvedimento di cumulo collegato a comunicazioni non validate |  |  |  | Verifica: Verificare che il sistema impedisca l'annullamento di un provvedimento di cumulo se questi ha delle comunicazioni associate non validate | 1.0 |  |  |  |  |
| SIUT | SIES | 201911060112.0 |  |  | 201911060112.0 | Assenza check di validazione |  | SIUS | SIUS - Anomalia su validazione | TF005.SIUS | Verifica presenza check di validazione su icona di upload |  |  |  | Verifica: Verificare che siano visibili il/i Modello/i di stampa e che funzioni la validazione (icona 'Upload Stampa') | 1.0 |  |  |  |  |
| SIUT | SIES | 201912130111.0 |  |  | 201912130111 | Assenza Template |  | SIEP | SIEP - Assenza Template su conversione pene pecuniarie | TF006.SIEP | Verifica generazione del template |  |  |  | Verifica: verificare che venga generato il template nel caso di inserimento nuovo procedimento in gestione altre sanzioni - conversione pene pecuniarie | 1.0 |  |  |  |  |
| SIUT | SIES | 20191210011 |  |  | 20191210011 | Impossibilità di emettere Decreto di Inammissibilità |  | SIGE | SIGE – Decreto di inammissibilità rito collegiale senza udienza | TF007.SIGE | Verifica su Decreto di inammissibilità rito collegiale senza udienza |  |  |  | Verifica: Verificare che possa essere emesso un Decreto di inammissibilità rito collegiale senza udienza | 1.0 |  |  |  |  |
| SIUT | SIES | 20191213011 |  |  | 20191213011 | Impossibile riunire due procedimenti |  | SIGE | SIGE - impossibile riunire due procedimenti | TF008.SIGE | Verifica su errata visualizzazione di un messaggio bloccante. |  |  |  | Verifica: Verificare che il sistema non visualizzi il messaggio bloccante 'il Procedimento da Unificare presenta uno stato incompatibile per l’unificazione: Unificazione Impossibile'. | 1.0 |  |  |  |  |
| SIUT | SIES | 20191128013.0 |  |  | 20191128013.0 | Impossibile validare |  | SIEP | SIEP - Impossibile validare e stampare | TF009.SIEP | Verificare che possa essere effettuata la stampa di un procedimento cumulato che da una posizione giuridica espiazione pena per altra causa in regime di detenzione abbia assunto (in fase di emissione cumulo) la nuova posizione giuridica di espiazione pena in regime carcerario. |  |  |  | Verifica: Verificare che possa essere effettuata la stampa di un procedimento cumulato che da una posizione giuridica espiazione pena per altra causa in regime di detenzione abbia assunto (in fase di emissione cumulo) la nuova posizione giuridica di espiazione pena in regime carcerario. | 1.0 |  |  |  |  |
| SIUT | SIES | 20191213016 |  |  | 20191213016 | Annullamento Provvedimento di cumulo |  | SIEP | SIEP - Anomalia su validazione evento | TF010.SIEP | Verifica dell'impossibilità di annullare un provvedimento di cumulo collegato a comunicazioni non validate |  |  |  | Verifica: Verificare che il sistema impedisca l'annullamento di un provvedimento di cumulo se questi ha delle comunicazioni associate non validate | 1.0 |  |  |  |  |
| SIUT | SIES | 20191024014.0 |  |  | 20191024014.0 | Mancata scadenza sessione |  | SIEP | SIEP - Durata Sessione Utente | TF011.SIEP | Verifica durata della sessione utente |  |  |  | Verifica: Verificare che il sistema visualizzi il messaggio di timeout della sessione allo scadere dei minuti inpostati sul file web.xml | 1.0 |  |  |  |  |
| SIUT | SIES | 20191217019.0 |  |  | 20191217019.0 | Mancata validazione provvedimento di cumulo |  | SIEP | SIEP - Mancata validazione provvedimento di cumulo | TF012.SIEP | Verifica validazione cumulo con pena ergastolo |  |  |  | Verifica: Verificare che dopo l'inserimento del cumulo con pena ergastolo sia permessa la validazione | 1.0 |  |  |  |  |
| SIUT | SIES | 20191126015 |  |  | 20191126015 | impossibilità di scaricare l’ORDINANZA DI INCOMPETENZA |  | SIGE | SIGE - impossibilità di scaricare l’ORDINANZA DI INCOMPETENZA | TF013.SIGE | Verifica su ORDINANZA DI INCOMPETENZA rito collegiale senza udienza |  |  |  | Verifica: Verificare che possa essere emessa un'ORDINANZA DI INCOMPETENZA rito collegiale senza udienza | 1.0 |  |  |  |  |
| SIUT | SIES | 20191129018 |  |  | 20191129018 | Stampa certificato stato esecuzione errata |  | SIEP | SIEP - Stampa certificato stato esecuzione errata | TF014.SIEP | Verifica stampa certificato stato esecuzione in presenza di un'ordinanza relativa a rimedi risarcitori D.L. 92/2014 emessa dall'Ufficio di Sorveglianza |  |  |  | Verifica: Verifica stampa certificato stato esecuzione in presenza di un'ordinanza relativa a rimedi risarcitori D.L. 92/2014 emessa dall'Ufficio di Sorveglianza | 1.0 |  |  |  |  |

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
| Codifica Piano di test |  |  | SIUT-SIES-CT-1.0-20200110-Allegato-al-piano-test.xls |  |  |  |  |  |  |
| ID caso di test | Suffisso Caso di test | Nome Caso di test
Tipo Step |  | Descrizione |  | Versione | Stima tempo | N.cond. di test | Esito |
| TF001.SIEP | 01 | Verifica form dell'Ordine di scarcerazione per Rideterminazione pena |  | Verifica: verificare che sia stata personalizzata per i minori la form dell'Ordine di scarcerazione per Rideterminazione pena |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Bxxxxx (Procura della Repubblica Presso il Tribunale per i Minorenni ) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Navigazione | Rideterminazione pena → Altro |  |  |  |  |  |  |
|  | 2 | Azione | L'utente individua un procedimento per il quale la posizione giuridica sia 'Espiazione Pena in Regime di Affidamento in Prova', seleziona come oggetto 'Rideterminazione Pena' ed  inserisce lo scomputo di 1 mese. Infine conferma. |  | Visualizzazione Pagina di output con unico pulsante attivo : Calcolo Pena |  |  |  |  |
|  | 3 | Azione | L'utente seleziona Calcolo Pena |  | Visualizzazione Pagina del Calcolo Pena |  |  |  |  |
|  | 4 | Azione | L'utente seleziona Conferma |  | Visualizzazione Pagina Dettaglio Rideterminazione Pena Altro |  |  |  |  |
|  | 5 | Azione | L'utente seleziona Stampe |  | Visualizzazione Pagina Provvedimenti e Stampe per Rideterminazione Pena |  |  |  |  |
|  | 6 | Azione | L'utente seleziona 'Rideterminazione pena (ordine di scarcerazione)' |  | Visualizzazione pagina  Ordine di Scarcerazione per Nuova Scadenza Pena |  |  |  |  |
|  | V | Verifica | Verificare che:
Nella list box UEPE sia presente USSM,
Nella list box Magistrato di Sorveglianza sia presente l’autorità relativa ai Minorenni,
Nella listbox Tribunale di Sorveglianza sia presente l’autorità relativa ai Minorenni. |  |  |  |  |  |  |
|  | 7 | Azione | L'utente seleziona nelle list box elencate sopra le autorità relative ai Minorenni e seleziona 'Conferma' |  | Visualizzazione pagina  Dettaglio Comunicazione Rideterminazione Pena |  |  |  |  |
|  | V | Verifica | Verificare che la pagina contenga correttamente i dati inseriti nello step 7 |  |  |  |  |  |  |
|  | 8 | Azione | L'utente tramite l'apposita icona genera la stampa |  | Generazione stampa SIEP_RP_OSRDP |  |  |  |  |
|  | V | Verifica | Verificare che la stampa prodotta contenga le informazioni inserite nello step 7 |  |  |  |  |  |  |
| TF002.SIEP | 01 | Verifica generazione del template |  | Verifica: verificare che venga generato il template relativo all'inserimento manuale di un provvedimento della sorveglianza |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Bxxxxx (Procura della Repubblica Presso il Tribunale dei Minori) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Navigazione | Ricerca Procedimento |  |  |  |  |  |  |
|  | 2 | Azione | Si ricerca un procedimento di Classe VII |  |  |  |  |  |  |
|  | 3 | Azione | Si seleziona dal menu "Gestione Altre Sanzioni" e successivamente cliccare su “Conversione Pene Pecuniarie” |  |  |  |  |  |  |
|  | 4 | Azione | Cliccare su “Definizione procedimento” e successivamente sul link "Inserimento Manuale" |  | Visualizzazione pagina di inserimento del Provvedimento Sorveglianza |  |  |  |  |
|  | 5 | Azione | Inserire i dati dell'odinanza/decreto e cliccare su Conferma |  | Viene visualizzata la pagina di dettaglio |  |  |  |  |
|  | 6 | Azione | Nella pagina di dettaglio cliccare sull'icona di Stampa |  |  |  |  |  |  |
|  | V | Verifica | Verificare che venga prodotto il relativo template |  |  |  |  |  |  |
| TF003.SIEP | 01 | Verifica conversione di un procedimento da Classe II a Classe VII |  | Verifica: Verificare l'avvenuta operazione di conversione di un procedimento SIEP da classe II a classe VII |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Navigazione | Gestione Altre Sanzioni |  | Visualizzazione Pagina Altre Sanzioni |  |  |  |  |
|  | 2 | Azione | Si seleziona Conversione Pene Pecuniarie |  | Visualizzazione Pagina Conversione Pene Pecuniarie |  |  |  |  |
|  | 3 | Azione | Si seleziona Iscrizione Procedimento (richiesta conversione) |  | Visualizzazione Pagina Ricerca Procedimento |  |  |  |  |
|  | 4 | Azione | Si ricerca un procedimento di classe II |  | Visualizzazione pagina di Iscrizione Richiesta Conversione |  |  |  |  |
|  | 5 | Azione | Valorizzare i campi obbligatori, l'anno ed il numero partita, l'importo della multa
Infine cliccare su Conferma |  | Viene visualizzata la pagina di output con i dati inseriti |  |  |  |  |
|  | V | Verifica | Verificare che non venga prodotto il messaggio di errore segnalato e che si acceda alla pagina 'Dettaglio Richiesta Conversione' |  |  |  |  |  |  |
| TF004.SIEP | 01 | Verifica dell'impossibilità di annullare un provvedimento di cumulo collegato a comunicazioni non validate |  | Verifica: Verificare che il sistema impedisca l'annullamento di un provvedimento di cumulo se questi ha delle comunicazioni associate non validate |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Navigazione | Ricerca Istrutturia Cumulo |  | Visualizzazione Pagina Ricerca Procedimento |  |  |  |  |
|  | 2 | Azione | Ricercare un'istrutturia di cumulo con stato "Aperta" |  |  |  |  |  |  |
|  | 3 | Azione | Procedere con la compilazione di tutti i tabulatori della funzione "Dati Finali Cumulo" |  |  |  |  |  |  |
|  | 4 | Azione | Nella pagina corrispondente al tabulatore "Emissione Provvedimento" indicare almeno un destinatario per la comunicazione |  |  |  |  |  |  |
|  | 5 | Azione | Porcedere con il salvataggio dei dati del cumulo, stampare e validare |  | Il sistema mostra la pagina di dettaglio del provvedimento di cumulo |  |  |  |  |
|  | 6 | Azione | Cliccare sul pulsante Uffici Esecuzione Penale/Sorveglianza, selezione il destinario e confermare l'invio della comunicazione SENZA effettuare la stampa e la validazione della stessa |  |  |  |  |  |  |
|  | 7 | Azione | L'utente procede richiamando la funzione "Elelnco Provvedimenti del PM" e procede con l'azione di cancellazione del provvedimento di unificazione pene concorrenti |  | Il sistema risponde con una pop up in cui si segnala la presenza di coumunicazioni non validate per cui non è possibile procedere con la cancellazione |  |  |  |  |
|  | V | Verifica | Verificare che il sistema NON consenta la cancellazione del provvedimento |  |  |  |  |  |  |
| TF005.SIUS | 01 | Verifica presenza check di validazione su icona di upload |  | Verifica: Verificare che siano visibili il/i Modello/i di stampa e che funzioni la validazione (icona 'Upload Stampa') |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIUS | Vxxxxx (Ufficio di Sorveglianza presso il Tribunale per i Minorenni) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Navigazione | Ordinanze → Elenco Provvedimenti Emessi |  |  |  |  |  |  |
|  | 2 | Azione | Ricercare un procedimento del tipo ordinanza con motivo provvedimento "Riesame pericolosita' sociale (art 208/1 C.P.)" da validare |  |  |  |  |  |  |
|  | 3 | Azione | Dall'elenco dei provvedimenti, andare sul dettaglio dell'ordinanza suddetta |  | Visualizzazione Pagina Dettaglio Ordinanza |  |  |  |  |
|  | V | Verifica | Verificare che sia presente il modello di stampa ed il Check per la validazione |  |  |  |  |  |  |
|  | 4 | Azione | Si valida e si seleziona il tasto 'Conferma' |  |  |  |  |  |  |
|  | 5 | Azione | Si ritorna all'elenco ottenuto con lo step 2 |  | Visualizzazione procedimento con le azioni Dettaglio Ordinanza e Visualizza Strampa |  |  |  |  |
|  | 6 | Azione | Si effettua la stampa del provvedimento tramite l'icona visualizza stampa presente tra le azioni. |  | Stampa template SIUS_OR_GENERICOU067.rtf |  |  |  |  |
|  | V | Verifica | Verificare che la stampa prodotta sia congruente con i dati inseriti. |  |  |  |  |  |  |
| TF006.SIEP | 01 | Verifica generazione del template |  | Verifica: verificare che venga generato il template nel caso di inserimento nuovo procedimento in gestione altre sanzioni - conversione pene pecuniarie |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Bxxxxx (Procura della Repubblica Presso il Tribunale dei Minori) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Navigazione | Gestione Altre Sanzioni -> Conversione pene pecuniarie -> Definizione procedimento |  | Visualizzazione Pagina Ricerca Procedimento |  |  |  |  |
|  | 2 | Azione | Si ricerca un procedimento di classe VII |  | Visualizzazione pagina Definizione Procedimento - Provvedimento Sorveglianza |  |  |  |  |
|  | 3 | Azione | Si seleziona il Dettaglio Ordinanza |  | Visualizzazione Pagina Dettaglio Ordinanza |  |  |  |  |
|  | 4 | Azione | Si inseriscono i dati del provvedimento e si seleziona “Conferma” |  | Visualizzazione pagina  Dettaglio Definizione Procedimento - Provvedimento Altra Autorità |  |  |  |  |
|  | 5 | Azione | Si seleziona il pulsante “Generazione stampa” |  | Produzione template SIEP_ARC_GENERICO |  |  |  |  |
|  | V | Verifica | Verificare che la stampa prodotta sia congruente con i dati inseriti. |  |  |  |  |  |  |
| TF007.SIGE | 01 | Verifica su Decreto di inammissibilità rito collegiale senza udienza |  | Verifica: Verificare che possa essere emesso un Decreto di inammissibilità rito collegiale senza udienza |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIGE | Txxxxx (Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Iscrivere un procedimento sige con rito collegiale. |  | Presenza in banca dati di un procedimento Sige con Rito Collegiale |  |  |  |  |
|  | 2 | Navigazione | Decreti --> Deposito --> Notifiche --> Emissione Decreto Inammissibilità |  | Visualizzazione Pagina di Inserimento Decreto Inammissibilità |  |  |  |  |
|  | 3 | Azione | Procedere con l'emissione di un decreto di inammissibilità per un procedimento SIGE con rito collegiale |  | Visualizzazione Pagina di  Dettaglio Decreto Inammissibilità |  |  |  |  |
|  | V | Verifica | Verificare che  il sistema non visualizzi il messaggio di obbligatorietà del collegio successivamente alla selezione del pulsante di 'Conferma' |  |  |  |  |  |  |
|  | 4 | Azione | Selezionare il pulsante per la funzione di modifica |  | Visualizzazione Pagina di Modifica Emissione Decreto Inammissibilità |  |  |  |  |
|  | 5 | Azione | Cliccare su Conferma |  | Visualizzazione Pagina di  Dettaglio Decreto Inammissibilità |  |  |  |  |
|  | V | Verifica | Verificare che anche la funzione di modifica non visualizzi il messaggio di obbligatorietà del collegio. |  |  |  |  |  |  |
| TF008.SIGE | 01 | Verifica su errata visualizzazione di un messaggio bloccante. |  | Verifica: Verificare che il sistema non visualizzi il messaggio bloccante 'il Procedimento da Unificare presenta uno stato incompatibile per l’unificazione: Unificazione Impossibile'. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIGE | Kxxxxx (Corte d'Appello) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Navigazione | Ricerche --> Procedimento SIGE per Estremi Atto |  | Visualizzazione Pagina Ricerca Procedimento SIGE per Estremi Atto |  |  |  |  |
|  | 2 | Azione | Individuare due procedimenti SIGE (uno con stato Iscritto e l'altro con stato Decreto Fissazione Udienza) scegliendo il radio button 'Solo Pendenti'. |  |  |  |  |  |  |
|  | 3 | Navigazione | Unificazioni --> Decreto di Unificazione Procedimenti |  | Visualizzazione Pagina Ricerca Procedimento Unificante |  |  |  |  |
|  | 4 | Azione | Inserire gli estremi (anno/numero) del procedimento individuato nello step 2 che ha lo stato a 'Decreto Fissazione Udienza'. Cliccare su Conferma |  | Visualizzazione pagina Inserimento Decreto Unificazione Sige |  |  |  |  |
|  | 5 | Azione | Inserire nella pagina Inserimento Decreto Unificazione Sige gli estremi del provvedimento SIGE (anno/numero) individuato nello step 2 con stato 'Iscritto'. Cliccare su Avanti |  | Visualizzazione pagina di riepilogo  Inserimento Decreto Unificazione Sige |  |  |  |  |
|  | 6 | Azione | Inserire la Data di Unificazione e cliccare su Conferma. |  | Visualizzazione pagina Dettaglio Decreto Unificazione Sige |  |  |  |  |
|  | V | Verifica | Verificare che il sistema non visualizzi il messaggio bloccante 'il Procedimento da Unificare presenta uno stato incompatibile per l’unificazione: Unificazione Impossibile'. |  |  |  |  |  |  |
| TF009.SIEP | 01 | Verificare che possa essere effettuata la stampa di un procedimento cumulato che da una posizione giuridica espiazione pena per altra causa in regime di detenzione abbia assunto (in fase di emissione cumulo) la nuova posizione giuridica di espiazione pena in regime carcerario. |  | Verifica: Verificare che possa essere effettuata la stampa di un procedimento cumulato che da una posizione giuridica espiazione pena per altra causa in regime di detenzione abbia assunto (in fase di emissione cumulo) la nuova posizione giuridica di espiazione pena in regime carcerario. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario ) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Navigazione | Ricerca Procedimento |  | Visualizzazione Pagina  Ricerca Procedimento |  |  |  |  |
|  | 2 | Azione | Ricercare un Procedimento che abbia come posizione giuridica 'Espiazione Pena per altra causa in regime di detenzione' |  | Visualizzazione pagina Dettaglio Procedimento |  |  |  |  |
|  | 3 | Azione | L'utente procede con l'emissione di un procedimento di cumulo e come posizione giuridica seleziona l'espiazione pena in regime carcerario. Il proicedimento di cumulo deve essere stampato e successivamente validato in modo che l'istruttoria risulti chiusa. |  |  |  |  |  |  |
|  | 4 | Navigazione | Rideterminazione Pena |  | Visualizzazione Pagina  Rideterminazione della pena |  |  |  |  |
|  | 5 | Azione | Cliccare su Altro |  | Visualizzazione Pagina  Rideterminazione della pena - Altro |  |  |  |  |
|  | 6 | Azione | La posizione giuridica deve essere : DETENUTO PER ALTRA CAUSA . Inserire l'Oggetto Rideterminazione Pena ed i restanti campi obbligatori. Cliccare su Conferma. |  | Visualizzazione pagina Dettaglio Rideterminazione Pena Altro |  |  |  |  |
|  | 7 | Azione | Cliccare su Calcolo Pena |  | Visualizzazione pagina Calcolo Pena |  |  |  |  |
|  | 8 | Azione | Cliccare su Conferma |  | Visualizzazione pagina Dettaglio Rideterminazione Pena Altro |  |  |  |  |
|  | 9 | Azione | Cliccare su Stampe |  | Visualizzazione pagina Provvedimenti e Stampe per Rideterminazione Pena |  |  |  |  |
|  | 10 | Azione | Selezionare la stampa Rideterminazione Pena (ordine scarcerazione) |  | Visualizzazione pagina  Ordine di Scarcerazione per Nuova Scadenza Pena |  |  |  |  |
|  | 11 | Azione | Valorizzare i campi obbligatori e cliccare su Conferma |  | Visualizzazione pagina Dettaglio Comunicazione Rideterminazione Pena |  |  |  |  |
|  | 12 | Azione | Cliccare sull'icona stampa |  | Stampa SIEP_RP_OSRDP |  |  |  |  |
|  | V | Verifica | Verificare che venga prodotta la stampa SIEP_RP_OSRDP |  |  |  |  |  |  |
| TF010.SIEP | 01 | Verifica dell'impossibilità di annullare un provvedimento di cumulo collegato a comunicazioni non validate |  | Verifica: Verificare che il sistema impedisca l'annullamento di un provvedimento di cumulo se questi ha delle comunicazioni associate non validate |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Navigazione | Ricerca Istrutturia Cumulo |  | Visualizzazione Pagina Ricerca Procedimento |  |  |  |  |
|  | 2 | Azione | Ricercare un'istrutturia di cumulo con stato "Aperta" |  |  |  |  |  |  |
|  | 3 | Azione | Procedere con la compilazione di tutti i tabulatori della funzione "Dati Finali Cumulo" |  |  |  |  |  |  |
|  | 4 | Azione | Nella pagina corrispondente al tabulatore "Emissione Provvedimento" indicare almeno un destinatario per la comunicazione |  |  |  |  |  |  |
|  | 5 | Azione | Porcedere con il salvataggio dei dati del cumulo, stampare e validare |  | Il sistema mostra la pagina di dettaglio del provvedimento di cumulo |  |  |  |  |
|  | 6 | Azione | Cliccare sul pulsante Uffici Esecuzione Penale/Sorveglianza, selezione il destinario e confermare l'invio della comunicazione SENZA effettuare la stampa e la validazione della stessa |  |  |  |  |  |  |
|  | 7 | Azione | L'utente procede richiamando la funzione "Elelnco Provvedimenti del PM" e procede con l'azione di cancellazione del provvedimento di unificazione pene concorrenti |  | Il sistema risponde con una pop up in cui si segnala la presenza di coumunicazioni non validate per cui non è possibile procedere con la cancellazione |  |  |  |  |
|  | V | Verifica | Verificare che il sistema NON consenta la cancellazione del provvedimento |  |  |  |  |  |  |
| TF011.SIEP | 01 | Verifica durata della sessione utente |  | Verifica: Verificare che il sistema visualizzi il messaggio di timeout della sessione allo scadere dei minuti inpostati sul file web.xml |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Navigazione | Si seleziona una qualunque funzione dal menu |  | Visualizzazione Pagina relativa alla voce di menu |  |  |  |  |
|  | 2 | Azione | Si attende per 30 minuti (valore attuale del timeout) |  | Visualizzazione Messaggio di sessione scaduta |  |  |  |  |
|  | V | Verifica | Verificare che la sessione sia scaduta |  |  |  |  |  |  |
| TF012.SIEP | 01 | Verifica validazione cumulo con pena ergastolo |  | Verifica: Verificare che dopo l'inserimento del cumulo con pena ergastolo sia permessa la validazione |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Cxxxxx (Procura Generale della Repubblica Presso la Corte D'Appello) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Navigazione | Ricerca Procedimento |  | Visualizzazione Pagina Ricerca Procedimento |  |  |  |  |
|  | 2 | Azione | Ricercare un'istruttoria di cumulo in stato "Aperta" e cliccare sul pulsante "Dati Finali Cumulo" |  |  |  |  |  |  |
|  | 3 | Azione | In fase di inserimento dati in "Pene Rideterminate", selezionare la pena detentiva "Ergastolo" e confermare |  |  |  |  |  |  |
|  | 4 | Azione | L'utente procede con l'inserimento dati sugli altri tabulatori, effettua la stampa e procede con la validazione del cumulo |  | Il sistema consente di validare il cumulo |  |  |  |  |
| TF013.SIGE | 01 | Verifica su ORDINANZA DI INCOMPETENZA rito collegiale senza udienza |  | Verifica: Verificare che possa essere emessa un'ORDINANZA DI INCOMPETENZA rito collegiale senza udienza |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIGE | Txxxxx (Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | Iscrivere un procedimento sige con rito collegiale. |  |  |  |  |  |  |
|  | 2 | Navigazione | Ordinanza --> Deposito --> Notifiche --> Incompetenza, NDP/NLP Emissione Ordinanza Incompetenza |  | Visualizzazione Pagina di Inserimento Ordinanza di Incompetenza |  |  |  |  |
|  | 3 | Azione | Procedere con l'emissione di un 'ordinanza di incompetenza per un procedimento SIGE con rito collegiale |  | Visualizzazione Pagina di  Dettaglio Ordinanza Incompetenza |  |  |  |  |
|  | V | Verifica | Verificare che  il sistema non visualizzi il messaggio di obbligatorietà del collegio successivamente alla selezione del pulsante di 'Conferma' |  |  |  |  |  |  |
|  | 4 | Azione | Selezionare il pulsante per la funzione di modifica |  | Visualizzazione Pagina di Modifica Emissione Ordinanza Incompetenza |  |  |  |  |
|  | 5 | Azione | Cliccare su Conferma |  | Visualizzazione Pagina di  Dettaglio Ordinanza Incompetenza |  |  |  |  |
|  | V | Verifica | Verificare che anche la funzione di modifica non visualizzi il messaggio di obbligatorietà del collegio. |  |  |  |  |  |  |
| TF014.SIEP | 01 | Verifica stampa certificato stato esecuzione in presenza di un'ordinanza relativa a rimedi risarcitori D.L. 92/2014 emessa dall'Ufficio di Sorveglianza |  | Verifica: Verifica stampa certificato stato esecuzione in presenza di un'ordinanza relativa a rimedi risarcitori D.L. 92/2014 emessa dall'Ufficio di Sorveglianza |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario ) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Navigazione | Ricerca Procedimento |  | Visualizzazione Pagina Ricerca Procedimento |  |  |  |  |
|  | 2 | Azione | Individuare un procedimento con un fine pena valorizzato, per il quale l'Ufficio di Sorveglianza abbia emesso un'ordinanza di riduzione pena per rimedi risarcitori |  |  |  |  |  |  |
|  | 3 | Navigazione | Decisioni della Sorveglianza --> Rimedi Risarcitori DL 26/06/2014, n°92 |  | Visualizzazione Pagina di Inserimento |  |  |  |  |
|  | 4 | Azione | L'utente procede con la selezione, tramite link, del provvedimento della Sorveglianza e procede con la conferma e la validazione |  |  |  |  |  |  |
|  | 5 | Navigazione | Stato esecuzione --> Certificato esecuzione |  | Visualizzazione Pagina Richiesta Stampa |  |  |  |  |
|  | 6 | Azione | Cliccare sul pulsante Stampa |  | Il sistema restituisce la stampa del certificato dello stato di esecuzione |  |  |  |  |
|  | V | Verifica | Verificare che il documento contenga tutte le informazioni relative all'ordinanza di riduzione pena per rimedi risarcitori |  |  |  |  |  |  |

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