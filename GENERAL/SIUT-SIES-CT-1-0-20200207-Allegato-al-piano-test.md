---
uniqueName: siut-sies-ct-1-0-20200207-allegato-al-piano-test
displayName: "SIUT SIES CT 1 0 20200207 Allegato al piano test"
category: "GENERAL"
tags: []
---

# SIUT-SIES-CT-1.0-20200207-Allegato-al-piano-test

> **File originale:** `RILASCIO_11.2.5/SIUT-SIES-CT-1.0-20200207-Allegato-al-piano-test.xls`  
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
|  | SIUT-SIES-CT-1.0-20200207-Allegato-al-piano-test.xls |
|  | Piano di test |
|  | Ver. 1.0 |
|  | Data: 07/02/2020 |
|  | SIUT |
|  | SIES 11.2.5 |
|  | Allegato al Piano dei Test |

## TabellaTest

| Codice Area |  |  | SIUT |  |  |  | Codifica  Piano di test |  | SIUT-SIES-CT-1.0-20200207-Allegato-al-piano-test.xls | Versione | Ver. 1.0 |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Applicazione |  |  | Funzionalità / Requisiti non funzionali |  |  |  |  |  |  | Caso di test |  |  |  |  |  |  |  |  |  |  |
| Codice Area | Codice Appl. | ID. Requisito | ID | Primo livello | ID | Primo Livello | Risk (1-5) | ID | Secondo livello | ID | Nome del caso di test | Classe di Gravità (1-4) | Ciclo di test | Stima Durata | Descrizione e note | Versione | N. cond. di test | Autom. | Classe di rilevanza (A, B, C) | Esito |
| SIUT | SIES | 202001070115 |  |  | 202001070115 | Stampa certificato esecuzione in formato PDF |  | SIEP | SIEP - Stampa certificato esecuzione in formato PDF | TF001.SIEP | Verifica Stampa certificato esecuzione in formato PDF |  |  |  | Verifica: verificare che il layout del file pdf stampa certificato esecuzione sia corretto | 1.0 |  |  |  |  |
| SIUT | SIES | 20200107012 |  |  | 20200107012 | Deposito e trasmissione ordinanza GE |  | SIGE | SIGE - Deposito e trasmissione ordinanza GE | TF002.SIGE | Verifica Deposito e trasmissione ordinanza GE |  |  |  | Verifica: verificare che all'atto del deposito e trasmissione di un'ordinaza il sistema riporta correttamente la notifica telematica all'avvocato difensore | 1.0 |  |  |  |  |
| SIUT | SIES | 20190805017 |  |  | 20190805017 | Mancata attribuzione dei giorni di detrazione rimedi risarcitori |  | SIEP | SIEP - Mancata attribuzione dei giorni di detrazione rimedi risarcitori | TF003.SIEP | Verifica Mancata attribuzione dei giorni di detrazione rimedi risarcitori |  |  |  | Verifica: verificare l'esatto conteggio della pena in fase di emissione di un reclamo per rimedi risarcitori (soggetto libero, soggetto detenuto con fine pena defnito e soggetto con ergastolo). | 1.0 |  |  |  |  |
| SIUT | SIES | 20200110017 |  |  | 20200110017 | Cancellazione periodi di presofferto |  | SIEP | SIEP - Cancellazione periodi di presofferto | TF004.SIEP | Verifica Cancellazione periodi di presofferto |  |  |  | Verifica: verificare che il dettaglio della pena del cumulo, nel tabulatore Rideterminazione Pena, tenga conto della cancellazione dei periodi contiuativi di misura cautelare. | 1.0 |  |  |  |  |
| SIUT | SIES | 20191210013.0 |  |  | 20191210013.0 | Errore del sistema nel calcolo pena |  | SIEP | SIEP - Errore del sistema nel calcolo pena | TF005.SIEP | Verifica Errore del sistema nel calcolo pena |  |  |  | Verifica: verificare che nella rideterminazione della pena siano anche presi in considerazione i codici 0987 (Rideterminazione della pena per estinzione delle pene della reclusione e della multa per decorso del tempo ex art. 172 cp) e 0988 (Rideterminazione della pena per estinzione delle pene dell'arresto e dell'ammenda per decorso del tempo ex art. 173 cp) | 1.0 |  |  |  |  |
| SIUT | SIES | 20200110018.0 |  |  | 20200110018.0 | Cumulo - richieste al giude dell'esecuzione - sorveglianza |  | SIEP | SIEP - Cumulo - richieste al giude dell'esecuzione - sorveglianza | TF006.SIEP | Verifica Cumulo - richieste al giude dell'esecuzione - sorveglianza |  |  |  | Verifica: verificare che non ci sia la 'perdita' del dato relativo al titolo che determina la revoca, in sede di modifica di una richiesta di revoca benefici dell’indulto. | 1.0 |  |  |  |  |
| SIUT | SIES | 20200109018 |  |  | 20200109018 | Presa in carico atti pervenuti. |  | SIUS | SIUS - Presa in carico atti pervenuti. | TF007.SIUS | Verifica Presa in carico atti pervenuti. |  |  |  | Verifica: verificare che nella trasmissione tra due distretti diversi di un procedimento SIUS non si produca l'errore di null pointer in fase di iscrizione di un procedimento EMS. | 1.0 |  |  |  |  |
| SIUT | SIES | 20200124013 | 20200124013 | 20200124013 | 20200124013 | Errore iscrizione procedimento |  | SIUS | SIUS - Errore iscrizione procedimento | TF008.SIUS | Verifica Errore iscrizione procedimento |  |  |  | Verifica: verificare che nella trasmissione tra due distretti diversi di un procedimento SIUS non si produca l'errore di null pointer in fase di iscrizione di un procedimento. | 1.0 |  |  |  |  |

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
| Codifica Piano di test |  |  | SIUT-SIES-CT-1.0-20200207-Allegato-al-piano-test.xls |  |  |  |  |  |  |
| ID caso di test | Suffisso Caso di test | Nome Caso di test
Tipo Step |  | Descrizione |  | Versione | Stima tempo | N.cond. di test | Esito |
| TF001.SIEP | 01 | Verifica Stampa certificato esecuzione in formato PDF |  | Verifica: verificare che il layout del file pdf stampa certificato esecuzione sia corretto |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Bxxxxx (Procura della Repubblica Presso il Tribunale per i Minorenni ) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | L'utente individua un fascicolo di classe I con stato procedimento 'Validato' oppure prosegue con un inserimento ex-novo di un fascicolo. (Il fascicolo deve essere a carico di soggetto con un'età >= 18 anni) |  |  |  |  |  |  |
|  | 2 | Navigazione | Decisioni Sorveglianza |  |  |  |  |  |  |
|  | 3 | Azione | L'utente procede con la funzione "Concessione Liberazione Anticipata" |  | Il sistema mostra la Pagina di Emissione Ordinanza di Liberazione Anticipata |  |  |  |  |
|  | 4 | Azione | L'utente compila i dati presenti in maschera e seleziona il check box "Giorni 45" (L.A.: Semestri Concessi) ed indica due semestri di riferimento. |  |  |  |  |  |  |
|  | 5 | Azione | L'utente seleziona Conferma |  | Il sistema mostra la Pagina Dettaglio Liberazione Anticipata. |  |  |  |  |
|  | 6 | Azione | L'utente seleziona la funzione 'Comunicazione'  e continua selezionando il pulsante con label 'Vai' |  | Il sistema mostra la  Pagina Comunicazione Concessione Liberazione Anticipata. |  |  |  |  |
|  | 7 | Azione | L'utente valorizza i campi obbligatori e clicca su 'Conferma' |  | Il sistema mostra la  Pagina di Dettaglio Comunicazione Concessione Liberazione Anticipata. |  |  |  |  |
|  | 8 | Azione | L'utente clicca sul pulsante di Stampa |  | Generazione stampa SIEP_COMU_LALIB in formato RTF |  |  |  |  |
|  | 9 | Azione | L'utente valida il documento e 'Conferma' |  | Visualizzazione messaggio 'Aggiornamento Documento Avvenuto Correttamente! ' |  |  |  |  |
|  | 10 | Azione | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Cxxxxx (Procura Generale della Repubblica Presso la Corte D'Appello) |  |  |  |  |  |
|  | 11 | Navigazione | Ricerche |  |  |  |  |  |  |
|  | 12 | Azione | L'utente seleziona la funzione di  "Ricerca Procedimento" |  |  |  |  |  |  |
|  | 13 | Azione | Nel campo "Anno/Numero Procedimento" inserire il fascicolo gestito con l'utenza "Bxxxxx", in "Ufficio" scegliere "PROCURA DELLA REPUBBLICA PRESSO IL TRIBUNALE PER I MINORENNI" ed in "Sede" indicare la sede opportuna.
Cliccare su 'Ricerca' |  | Il sistema visualizza la pagina di Dettaglio Procedimento |  |  |  |  |
|  | 14 | Navigazione | Stato esecuzione |  |  |  |  |  |  |
|  | 15 | Azione | L'utente seleziona "Certificato esecuzione" |  |  |  |  |  |  |
|  | 16 | Azione | L'utente clicca sul pulsante Generazione Stampa PDF |  | Il sistema genera il Certificato dello stato di Esecuzione in formato PDF |  |  |  |  |
|  | V | Verifica | L'utente verifica che la stampa prodotta riporti correttamente le date relative ai periodi non sovrapponendoli. |  |  |  |  |  |  |
| TF002.SIGE | 01 | Verifica Deposito e trasmissione ordinanza GE |  | Verifica: verificare che all'atto del deposito e trasmissione di un'ordinaza il sistema riporta correttamente la notifica telematica all'avvocato difensore |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIGE | Txxxxx (Tribunale Ordinario ) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | L'utente ricerca un provvedimento che non abbia già un'ordinanza emessa ma abbia un'udienza fissata, validata e depositata. |  |  |  |  |  |  |
|  | 2 | Navigazione | Ordinanze/Deposito/Notifiche --> Emissione Ordinanza |  |  |  |  |  |  |
|  | 3 | Azione | L'utente inserisce per l'ordinanza due avvocati difensori e la Data Emissione.
Successivamente, dopo aver cliccato su 'Conferma', in corrispondenza di 'Oggetti Titoli Esecutivi' - colonna 'Scarico Esito' , selezionare il check 'Unico per Oggetto' |  |  |  |  |  |  |
|  | 4 | Azione | L'utente, nella pagina visualizzata, seleziona un esito presente nella relativa combo.
Cliccare su 'Conferma' . |  | Visualizzazione pagina Dettaglio Oggetto |  |  |  |  |
|  | 5 | Azione | L'utente clicca sul pulsante 'Ritorna su'. |  | Visualizzazione pagina Dettaglio Ordinanza |  |  |  |  |
|  | 6 | Azione | L'utente procede con la validazione:
Seleziona il pulsante “Upload Stampa”;
Seleziona il pulsante “Generazione Stampa”;
Seleziona il check “Valida Documento” ;
Clicca su "Conferma". |  | Visualizzazione pagina Dettaglio Ordinanza |  |  |  |  |
|  | 7 | Azione | L'utente clicca sul pulsante 'Deposito Ordinanza' |  | Visualizzazione pagina Deposito Ordinanza del  xx/xx/xxxx |  |  |  |  |
|  | 8 | Azione | L'utente seleziona il check “Deposito Ordinanza e Trasmissione” ed inserisce TUTTI i destinatari.
Per uno dei due avvocati difensori seleziona il check ”S.N.T. (Sistema Notifiche Telematiche) ” ; per l'altro avvocato difensore, invece,  sceglie UNEP con relativa sede.
Inserisce la Data Deposito in Cancelleria.
Clicca su 'Conferma' |  | Visualizzazione pagina di Dettaglio Deposito Ordinanza |  |  |  |  |
|  | V | Verifica | L'utente verifica che nella pagina visualizzata ci siano tutti i destinatari inseriti precedentemente. |  |  |  |  |  |  |
|  | 9 | Azione | L'utente clicca sul pulsante Modifica Deposito Provvedimento |  | Visualizzazione pagina Deposito Ordinanza del  xx/xx/xxxx |  |  |  |  |
|  | V | Verifica | L'utente verifica che nella pagina di dettaglio il nome della funzione sia corretta (Deposito Ordinanza del xx/xx/xxxx) |  |  |  |  |  |  |
|  | 10 | Azione | L'utente, anche senza apportare modifiche, clicca su 'Conferma' . |  | Visualizzazione pagina di Dettaglio Deposito Ordinanza |  |  |  |  |
|  | V | Verifica | L'utente verifica che la pagina non produca un errore Java e che l'eventuale modifica sia avvenuta correttamente |  |  |  |  |  |  |
|  | 11 | Navigazione | Ordinanze/Deposito/Notifiche --> Stato Notifiche |  |  |  |  |  |  |
|  | 12 | Azione | L'utente, nella pagina di Ricerca Provvedimenti per Notifica, ricerca il provvedimento in esame |  | Visualizzazione pagina Ricerca Provvedimenti |  |  |  |  |
|  | 13 | Azione | L'utente, per l'ordinanza trattata negli step precedenti, sceglie tra le Azioni possibili “Inserimento Date Notifica” |  | Visualizzazione pagina Inserimento date Notifica |  |  |  |  |
|  | V | Verifica | L'utente verifica che la data di invio degli avvocati e dell'altro destinatario corrisponda alla data di trasmissione della notifica inserita predecentemente in fase di deposito e trasmisisone |  |  |  |  |  |  |
| TF003.SIEP | 01 | Verifica Mancata attribuzione dei giorni di detrazione rimedi risarcitori |  | Verifica: verificare l'esatto conteggio della pena in fase di emissione di un reclamo per rimedi risarcitori (soggetto libero, soggetto detenuto con fine pena defnito e soggetto con ergastolo). |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | L'utente individua un procedimento con fine pena valorizzato il cui soggetto si trova nella posizione giuridica di LIBERO |  |  |  |  |  |  |
|  | 2 | Azione | L'utente effettua l'accesso al sistema SIES come Ufficio di Sorveglianza | Exxxxx (Ufficio di Sorveglianza) |  |  |  |  |  |
|  | 3 | Navigazione | Iscrizione Manuale » Ricerca Titolo Esecutivo per Numero SIEP |  |  |  |  |  |  |
|  | 4 | Azione | L'utente, a partire dal procedimento SIEP individuato nel precedente step,  iscrive un procedimento SIUS con contenuto Rimedi Risarcitori per violazione Art.3 CEDU. Emette l'ordinanza indicando il numero di giorni concessi ed il periodo/i periodi di riferimento, valida, deposita e trasmette l'esito alla procura e al tribunale di Sorveglianza. |  |  |  |  |  |  |
|  | 5 | Azione | L'utente effettua nuovamente l'accesso al sistema SIES come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | 6 | Navigazione | Decisioni della Sorveglianza  » Rimedi Risarcitori DL 92/2014 |  |  |  |  |  |  |
|  | 7 | Azione | L'utente ricerca il procedimento SIEP |  | Il sistema visualizzazione la pagina Emissione Provvedimento Rimedi Risarcitori D.L. 92/2014 |  |  |  |  |
|  | 8 | Azione | L'utente procede con l'emissione della comunicazione dopo aver selezionato l'ordinanza dal link 'Seleziona provvedimento di Sorveglianza dalla lista '. Infine conferma, verifica la stampa e poi valida. |  |  |  |  |  |  |
|  | V | Verifica | Sul dettaglio del procedimento verificare che sia riportato il numero di giorni di riduzione pena concessi. |  |  |  |  |  |  |
|  | 9 | Azione | L'utente effettua l'accesso al sistema SIES come Tribunale di Sorveglianza | Dxxxxx (Tribunale di Sorveglianza) |  |  |  |  |  |
|  | 10 | Azione | L'utente, a partire dal procedimento SIEP individuato nel precedente step,  iscrive un procedimento  SIUS con contentuto 'RECLAMO IN MATERIA DI RIMEDI RISARCITORI PER VIOLAZIONE ART.3 CEDU ', emette l'ordinanza indicando il numero di giorni concessi ed il periodo/i periodi di riferimento, valida, deposita e trasmette l'esito alla procura. |  |  |  |  |  |  |
|  | 11 | Azione | L'utente effettua nuovamente l'accesso al sistema SIES come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | 12 | Navigazione | Decisioni della Sorveglianza  » Reclami Rimedi Risarcitori DL 92/2014 |  |  |  |  |  |  |
|  | 13 | Azione | L'utente ricerca il procedimento SIEP |  | Il sistema visualizza la pagina di Emissione Provvedimento Reclami Rimedi Risarcitori D.L. 92/2014 |  |  |  |  |
|  | 14 | Azione | L'utente procede con l'emissione della comunicazione dopo aver selezionato l'ordinanza dal link 'Seleziona provvedimento di Sorveglianza dalla lista '. Infine conferma, verifica la stampa e poi valida. |  |  |  |  |  |  |
|  | V | Verifica | L'utente, sul Dettaglio Comunicazione Concessione Reclamo Risarcimento Danni D.L. 92/2014 - Condannato Libero verifica che sia riportato il numero di giorni di riduzione pena concessi. |  |  |  |  |  |  |
|  | R1 | Riciclo Script | L'utente ripete gli step da 1 a 14, individuando un procedimento con fine pena valorizzato il cui soggetto si trova nella posizione giuridica di DETENUTO |  |  |  |  |  |  |
|  | R2 | Riciclo Script | L'utente ripete gli step da 1 a 14, individuando un procedimento con fine pena valorizzato il cui soggetto si trova nella posizione giuridica di ERGASTOLANO |  |  |  |  |  |  |
| TF004.SIEP | 01 | Verifica Cancellazione periodi di presofferto |  | Verifica: verificare che il dettaglio della pena del cumulo, nel tabulatore Rideterminazione Pena, tenga conto della cancellazione dei periodi contiuativi di misura cautelare. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | L'utente ricerca un procedimento di classe I con stato “Iscritto” |  |  |  |  |  |  |
|  | 2 | Azione | L'utente, dal dettaglio del procedimento, va in “Iscrizione Misura Cautelare” |  |  |  |  |  |  |
|  | 3 | Azione | L'utente, seleziona il pulsante “Cessata al momento del passaggio in giudicato computabili” |  | Visualizzazione pagina  Inserimento Misura Cautelare - COMPUTABILE |  |  |  |  |
|  | 4 | Azione | L'utente procede con l’inserimento di almeno due misure cautelari con Misura = ”Custodia cautelare in carcere”, che abbiano dei periodi continuativi tra loro, cioè ad esempio: una misura dal 01/01/2020 al 20/01/2020 e poi l'altra dal 20/01/2020 al 25/01/2020. |  |  |  |  |  |  |
|  | 5 | Azione | L'utente valida il procedimento tramite l'apposita voce di menu |  |  |  |  |  |  |
|  | 6 | Azione | L'utente procede alla creazione del cumulo con l'apertura di un'istruttoria: Pulsante Gestione Cumulo → Apertura Istruttoria: conferma apertura istruttoria |  |  |  |  |  |  |
|  | 7 | Azione | L'utente accede alla funzione Dati Finali Cumulo e dopo aver inserito la Data Emissione conferma |  |  |  |  |  |  |
|  | 8 | Azione | L'utente, tramite il link “Elenco Titoli Coinvolti”, accede nella pagina contenente  l' Elenco Provvedimenti Esecutivi Coinvolti.
Cliccare sulla lente (Dettaglio Dati Analitici) presente nella colonna azioni. |  |  |  |  |  |  |
|  | 9 | Azione | L'utente seleziona il pulsante Dati Analitici. 
Vengono prospettati dei pulsanti. Cliccare su Misure Cautelari. |  | La pagina mostra l'elenco dei periodi continuativi delle misure cautelari inserite precedentemente |  |  |  |  |
|  | 10 | Azione | L'utente elimina i due periodi selezionando la X sotto la colonna “Azioni”. |  |  |  |  |  |  |
|  | 11 | Azione | L'utente seleziona il pulsante Gestione Cumulo →  Dati Finali Cumulo |  | Visualizzazione pagina Dati Finali Cumulo |  |  |  |  |
|  | 12 | Azione | L'utente seleziona Pene Rideterminate  e clicca sul link “Dettaglio della Pena”. |  | Visualizzazione popup "Riepilogo delle Pene" |  |  |  |  |
|  | V | Verifica | L'utente verifica che non siano visualizzate le misure cautelari eliminate precedentemente. |  |  |  |  |  |  |
| TF005.SIEP | 01 | Verifica Errore del sistema nel calcolo pena |  | Verifica: verificare che nella rideterminazione della pena siano anche presi in considerazione i codici 0987 (Rideterminazione della pena per estinzione delle pene della reclusione e della multa per decorso del tempo ex art. 172 cp) e 0988 (Rideterminazione della pena per estinzione delle pene dell'arresto e dell'ammenda per decorso del tempo ex art. 173 cp) |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | L'utente individua un procedimento con un fine pena definito ed in fase di espiazione. |  |  |  |  |  |  |
|  | 2 | Azione | L'utente procede con la funzione di Rideterminazione Pena >> Altro ed inserisce una riduzione della pena, scegliendo il radio button 'In esecuzione di provvedimento altro ufficio', come autorià emittente 'Giudice Esecuzione' e come oggetto del provvedimento la voce 'Rideterminazione della pena per estinzione delle pene della reclusione e della multa per decorso del tempo ex art. 172 cp'. |  |  |  |  |  |  |
|  | 3 | Azione | L'utente procede con la riduzione della pena e conferma l'operazione |  |  |  |  |  |  |
|  | 4 | Azione | L'utente, nella pagina successiva, procede con la funzione 'Calcolo Pena', conferma e poi prosegue con il pulsante 'Stampe'. |  |  |  |  |  |  |
|  | 5 | Azione | L'utente, nella pagina successiva, procede con la validazione usando il pulsante 'Valida Provvedimento'. |  |  |  |  |  |  |
|  | V | Verifica | L'utente, spostandosi sul dettaglio del procedimento, verifica che il valore per 'Pena da espiare' risulti aggiornata in base alla pena rideterminata. |  |  |  |  |  |  |
|  | 6 | Azione | L'utente si sposta sulla funzione Rideterminazione Pena >> Amnistia/Indulto |  | Visualizzazione pagina Richiesta/Anticipazione Amnistia/Indulto |  |  |  |  |
|  | V | Verifica | L'utente, verifica che nella pagina mostrata sia riportato il corretto valore per Pena in espiazione (deve essere aggiornato in base all'ultimo calcolo pena). |  |  |  |  |  |  |
| TF006.SIEP | 01 | Verifica Cumulo - richieste al giude dell'esecuzione - sorveglianza |  | Verifica: verificare che non ci sia la 'perdita' del dato relativo al titolo che determina la revoca, in sede di modifica di una richiesta di revoca benefici dell’indulto. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | L'utente cerca un procedimento di classe III (pena sospesa condizionalmente) validato |  |  |  |  |  |  |
|  | 2 | Azione | L'utente individua un procedimento di classe I validato e relativo allo stesso soggetto del procedimento di classe III |  |  |  |  |  |  |
|  | 3 | Azione | L'utente apre, per il procedimento di classe I, un'istruttoria di cumulo |  |  |  |  |  |  |
|  | 4 | Azione | L'utente clicca sul link "Elenco Titoli Coinvolti" |  | Visualizzazione pagina  Elenco Provvedimenti Esecutivi Coinvolti |  |  |  |  |
|  | 5 | Azione | L'utente clicca sul pulsante “Iscrizione Proprio Procedimento” |  | Visualizzazione pagina  Ricerca Procedimenti per Titolo e Soggetto |  |  |  |  |
|  | 6 | Azione | L'utente selezionare il procedimento di classe III individuato inizialmente e clicca sul pulsante “Iscrivi In Istruttoria” |  | Visualizzazione pagina Elenco Provvedimenti Esecutivi Coinvolti |  |  |  |  |
|  | 7 | Azione | L'utente entra nel dettaglio del procedimento di classe III e clicca sul pulsante Dati Analitici e successivamente clicca su Benefici (disposti in sentenza) |  | Visualizzazione pagina Elenco Benefici |  |  |  |  |
|  | 8 | Azione | L'utente clicca sul pulsante  “Inserisci Indulto/Amnistia ” |  | Visualizzazione pagina  Inserimento Beneficio Indulto |  |  |  |  |
|  | 9 | Azione | L'utente inserisce il beneficio dell'indulto e conferma |  | Visualizzazione pagina Dettaglio Beneficio Indulto |  |  |  |  |
|  | 10 | Navigazione | Gestione Cumulo → Richieste del PM → Richieste al Giudice dell'Esecuzione → Richiesta Revoca Benefici |  | Visualizzazione pagina Richieste al G.E. Revoca Benefici |  |  |  |  |
|  | 11 | Azione | L'utente seleziona il beneficio da revocare e conferma |  | Visualizzazione pagina  Inserimento Richiesta Revoca Beneficio |  |  |  |  |
|  | 12 | Azione | L'utente inserisce la revoca (seleziona il titolo esecutivo tramite il relativo link;  Articolo=Revoca Beneficio ex. Articolo 168 primo comma n. 1 c.p.; Motivazione:Commissione di un delitto entro cinque anni dal passaggio in giudicato della condanna sospesa; inserisce la Data Richiesta; seleziona “Anticipazione degli effetti”) e conferma |  | Visualizzazione pagina Dettaglio Richiesta Revoca Benefici |  |  |  |  |
|  | 13 | Azione | L'utente, con l'apposito pulsante, ritorna alla pagina precedente. Dalla revoca in elenco seleziona tra le azioni quella relativa alla Modifica |  | Visualizzazione pagina Modifica Richiesta Revoca Beneficio |  |  |  |  |
|  | 14 | Azione | L'utente nella pagina visualizzata clicca sul pulsante di Conferma. |  |  |  |  |  |  |
|  | V | Verifica | L'utente verifica che nel “Dettaglio Richiesta Revoca Benefici” venga visualizzata l'indicazione del Titolo che determina la revoca |  |  |  |  |  |  |
| TF007.SIUS | 01 | Verifica Presa in carico atti pervenuti. |  | Verifica: verificare che nella trasmissione tra due distretti diversi di un procedimento SIUS non si produca l'errore di null pointer in fase di iscrizione di un procedimento EMS. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | L'utente cerca un procedimento di Classe IV validato |  |  |  |  |  |  |
|  | 2 | Azione | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIUS in un distretto diverso da quello di appartenenza del procedimento di Classe IV individuato nello step 1 | Uxxxxx (Ufficio di Sorveglianza) |  |  |  |  |  |
|  | 3 | Navigazione | Ricerche Altre BDI » Ricerca Fascicolo SIEP altre BDI |  |  |  |  |  |  |
|  | 4 | Azione | L'utente ricerca il procedimento individuato nello step 1 |  |  |  |  |  |  |
|  | 5 | Azione | L'utente effettua la presa in carico, l'iscrizione di una Esecuzione Misura Sicurezza ed infine un Procedimento di Riesame. |  |  |  |  |  |  |
|  | 6 | Azione | L'utente emette un'ordinanza, la valida e la trasmette all'Ufficio di Sorveglianza del distretto a cui appartiene il procedimento individuato nello step 1 |  |  |  |  |  |  |
|  | 7 | Azione | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIUS nello stesso distretto a cui appartiene il procedimento di Classe IV individuato nello step 1 | Exxxxx (Ufficio di Sorveglianza) |  |  |  |  |  |
|  | 8 | Navigazione | Presa in carico atti pervenuti » Ricerca per Atti - SIUS |  |  |  |  |  |  |
|  | 9 | Azione | L'utente effettua la ricerca con Tipo Ufficio = Ufficio di Sorveglianza, Sede Ufficio = distretto dello step 2. Infine seleziona "Visualizza anche gli atti già presi in carico " e clicca su Ricerca |  | Visualizzazione pagina Lista Atti Ricevuti |  |  |  |  |
|  | 10 | Azione | L'utente individua nella lista individua il procedimento SIEP di interesse e seleziona il dettaglio presente nella colonna Azioni |  | Visualizzazione pagina Dettaglio Ordinanza Ricevuta |  |  |  |  |
|  | 11 | Azione | L'utente clicca sul pulsante Conferma Presa in Carico |  | Visualizzazione pagina Presa in carico atto pervenuto da SIUS |  |  |  |  |
|  | 12 | Azione | L'utente inserisce il procedimento SIUS. In particolare nel Contenuto inserisce ' Esecuzione Misure Sicurezza' . Clicca su Conferma |  |  |  |  |  |  |
|  | V | Verifica | L'utente verifica che non venga prodotto un errore di null pointer e che il sistema prospetti correttamente la pagina successiva di Dettaglio Procedimento SIUS per proseguire con l'inserimento. |  |  |  |  |  |  |
| TF008.SIUS | 01 | Verifica Errore iscrizione procedimento |  | Verifica: verificare che nella trasmissione tra due distretti diversi di un procedimento SIUS non si produca l'errore di null pointer in fase di iscrizione di un procedimento. |  | 1.0 |  |  | OK |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) |  |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIEP | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |  |  |  |
|  | 1 | Azione | L'utente cerca un procedimento di Classe IV validato |  |  |  |  |  |  |
|  | 2 | Azione | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIUS in un distretto diverso da quello di appartenenza del procedimento di Classe IV individuato nello step 1 | Uxxxxx (Ufficio di Sorveglianza) |  |  |  |  |  |
|  | 3 | Navigazione | Ricerche Altre BDI » Ricerca Fascicolo SIEP altre BDI |  |  |  |  |  |  |
|  | 4 | Azione | L'utente ricerca il procedimento individuato nello step 1 |  |  |  |  |  |  |
|  | 5 | Azione | L'utente effettua la presa in carico, l'iscrizione di una Esecuzione Misura Sicurezza ed infine un Procedimento di Riesame. |  |  |  |  |  |  |
|  | 6 | Azione | L'utente emette un'ordinanza, la valida e la trasmette all'Ufficio di Sorveglianza del distretto a cui appartiene il procedimento individuato nello step 1 |  |  |  |  |  |  |
|  | 7 | Azione | L'utente effettua l'accesso al sistema SIES con opportune credenziali per SIUS nello stesso distretto a cui appartiene il procedimento di Classe IV individuato nello step 1 | Exxxxx (Ufficio di Sorveglianza) |  |  |  |  |  |
|  | 8 | Navigazione | Presa in carico atti pervenuti » Ricerca per Atti - SIUS |  |  |  |  |  |  |
|  | 9 | Azione | L'utente effettua la ricerca con Tipo Ufficio = Ufficio di Sorveglianza, Sede Ufficio = distretto dello step 2. Infine seleziona "Visualizza anche gli atti già presi in carico " e clicca su Ricerca |  | Visualizzazione pagina Lista Atti Ricevuti |  |  |  |  |
|  | 10 | Azione | L'utente individua nella lista individua il procedimento SIEP di interesse e seleziona il dettaglio presente nella colonna Azioni |  | Visualizzazione pagina Dettaglio Ordinanza Ricevuta |  |  |  |  |
|  | 11 | Azione | L'utente clicca sul pulsante Conferma Presa in Carico |  | Visualizzazione pagina Presa in carico atto pervenuto da SIUS |  |  |  |  |
|  | 12 | Azione | L'utente inserisce il procedimento SIUS. In particolare nel Contenuto inserisce ' Esecuzione Misure Sicurezza' . Clicca su Conferma |  |  |  |  |  |  |
|  | V | Verifica | L'utente verifica che non venga prodotto un errore di null pointer e che il sistema prospetti correttamente la pagina successiva di Dettaglio Procedimento SIUS per proseguire con l'inserimento. |  |  |  |  |  |  |

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