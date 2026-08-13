---
uniqueName: siut-sies-ct-1-0-20211011-allegatoalpianotest006si
displayName: "SIUT SIES CT 1 0 20211011 Allegato al piano test 006 SIUS Avvocati"
category: "GENERAL"
tags: []
---

# SIUT-SIES-CT-1.0-20211011-Allegato_al_piano_test_006_SIUS_Avvocati

> **File originale:** `MEV/SCHEDA_006/SIUT-SIES-CT-1.0-20211011-Allegato_al_piano_test_006_SIUS_Avvocati.xlsx`  
> **Tipo:** XLSX

---

## Copertina

## TabellaTest

| Intervento |  | MEV 2019_006 SIUS Avvocati |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  | SIUT-SIES-CT-1.0-20211011-Allegato_al_piano_test_006_SIUS_Avvocati.xlsx |  |  |  |  |  |  |  |  |
| Codice Appl. | ID. Requisito Padre | Lista Requisiti | ID Caso d'uso | Caso d'uso | ID | Scenario di test | Classe di Gravità (1-4) | Classe di rilevanza (A, B, C) | Esito |  |
| SIES | REQ-SIE-006-01 | REQ-SIE-006-01 | UC01 | Esecuzione Stress Test | TF001.UC01 | Verifica di Performance: Eseguire gli stress test sugli Application Server del Sistema Centrale e su un server distrettuale, nonché sul Database Server, per rilevare il comportamento dell’applicativo SIES-Avvocatura in caso di un elevato carico di lavoro. Per la corretta esecuzione dei test utilizzare il software open source Apache JMeter | 3 | C |  |  |
| SIES | REQ-SIE-006-02 | REQ-SIE-006-02 | UC01 | Verifica assenza di errori nel file server.log | TF002.UC01 | Verifica di NON regressione: Verificare che nel file server.log (presente nella cartella "/opt/jboss-eap-6.4/standalone/log") NON sia presente la dicitura "IJ000100: Closing a connection for you." | 3 | C |  |  |
| SIES | REQ-SIE-006-03 | REQ-SIE-006-03 | UC01 | Verifica Inserimento Fissazione Udienza in SIUS per NON regressione dopo modifica query | TF003.UC01 | Verifica di NON regressione: Verificare che nel sottosistema SIUS, nella fase di inserimento fissazione udienza, la ricerca dell'udienza dia risultati congrui con l'installazione precedente | 3 | C |  |  |
| SIES | REQ-SIE-006-03 | REQ-SIE-006-03 | UC02 | Verifica Trasmissione Foglio Complementare al SIC per NON regressione SiesEsecuzione | TF003.UC02 | Verifica di NON regressione: Verificare che nel sottosistema SIUS, nella fase di trasmissione foglio complementare al SIC, l'operazione dia risultati congrui con l'installazione precedente | 3 | C |  |  |
| SIES | REQ-SIE-006-03 | REQ-SIE-006-03 | UC03 | Verifica Impatto indicizzazione tabella STATO_PROCEDIMENTO | TF003.UC03 | Verifica: Verificare che nel sottosistema SIEP, nella fase di ricerca fascicolo avanzata, i tempi di risposta siano migliori rispetto all'installazione precedente | 3 | C |  |  |
| SIES | REQ-SIE-006-03 | REQ-SIE-006-03 | UC04 | Verifica Impatto indicizzazione tabella SOGGETTO | TF003.UC04 | Verifica: Verificare che nel sottosistema SIEP, nella fase di ricerca Procedimento per Soggetto, i tempi di risposta siano migliori rispetto all'installazione precedente | 3 | C |  |  |
| SIES | REQ-SIE-006-03 | REQ-SIE-006-03 | UC05 | Verifica Impatto indicizzazione tabella REATO | TF003.UC05 | Verifica: Verificare che nel sottosistema SIEP, nella fase di ricerca Procedimento per Soggetto, i tempi di risposta siano migliori rispetto all'installazione precedente | 3 | C |  |  |
| SIES | REQ-SIE-006-03 | REQ-SIE-006-03 | UC06 | Verifica Impatto indicizzazione tabelle coinvolte nel package "PULISCI" e procedura "Pulisci_Evento" | TF003.UC06 | Verifica: Verificare che nel sottosistema SIEP, nella fase di cancellazione di un evento di tipo "Ordine di Esecuzione", i tempi di risposta siano migliori rispetto all'installazione precedente | 3 | C |  |  |

## SpecificaTest

| Intervento |  |  | MEV 2019_006 SIUS Avvocati |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | SIUT-SIES-CT-1.0-20211011-Allegato_al_piano_test_006_SIUS_Avvocati.xlsx |  |  |  |
| ID caso di test | Requisito |  | Caso d'uso |  | Scenario di test |  |
| TF001.UC01 | REQ-SIE-006-01 |  | Esecuzione Stress Test |  | Verifica di Performance: Eseguire gli stress test sugli Application Server del Sistema Centrale e su un server distrettuale, nonché sul Database Server, per rilevare il comportamento dell’applicativo SIES-Avvocatura in caso di un elevato carico di lavoro. Per la corretta esecuzione dei test utilizzare il software open source Apache JMeter |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | N.A. |  |  |  |
|  | P | Stato Base | N.A. |  |  |  |
|  | 1 | Navigazione | N.A. |  |  |  |
|  | 2 | Azione | Eseguire gli stress test utilizzando il software Apache JMeter al fine di simulare in maniera indipendente il carico di lavoro degli utenti degli uffici del sies distrettuale rispetto a quello centrale. |  | Tempi di attesa che maggiormente hanno afflitto i processi utente per rispondere alle richieste inviate dall’applicazione siano ottimizzati; le misure dei tempi di risposta delle istruzioni SQL più onerose siano diminuite. |  |
|  | V | Verifica | Verificare che i test JMeter eseguiti su una installazione (sies.war) e su un database indicizzato siano migliori rispetto agli stessi test eseguiti su precedenti versioni di applicativo (es: 12.4.13.0) e database (versione senza indici nuovi). |  |  |  |
| TF002.UC01 | REQ-SIE-006-02 |  | Verifica assenza di errori nel file server.log |  | Verifica di NON regressione: Verificare che nel file server.log (presente nella cartella "/opt/jboss-eap-6.4/standalone/log") NON sia presente la dicitura "IJ000100: Closing a connection for you." |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | N.A. |  |  |  |
|  | P | Stato Base | N.A. |  |  |  |
|  | 1 | Azione | Fermare il server SIES |  | Server fermato |  |
|  | V | Verifica | Verificare che il server sia fermato |  |  |  |
|  | 2 | Azione | Posizionarsi sotto la cartella del server: "/opt/jboss-eap-6.4/standalone/configuration";
editare il file "standalone-full.xml" e:
a. posizionarsi nel sottosistema "datasources" ed
impostare use-ccm="true" nella riga "datasource":
<subsystem xmlns="urn:jboss:domain:datasources:1.x">
 <datasources>
  <datasource ... enabled="true" … use-ccm="true">;
b. posizionarsi nel sottosistema "jca" ed
aggiungere in coda (prima della chiusura del tag </subsystem>) la riga
<cached-connection-manager debug="true" error="false"/>
e (se presente) cancellare la riga <cached-connection-manager/>:
<subsystem xmlns="urn:jboss:domain:jca:1.x">
...
<cached-connection-manager debug="true" error="false"/>
</subsystem>. |  | File modificato |  |
|  | V | Verifica | Verificare che il file riporti le nuove impostazioni |  |  |  |
|  | 3 | Azione | Avviare il server |  | Server avviato |  |
|  | V | Verifica | Verificare che il server sia attivo |  |  |  |
|  | 4 | Azione | L'utente effettua l'accesso al sistema SIUS come Tribunale di Sorveglianza | Dxxxxx (Tribunale di Sorveglianza) | Accesso effettuato |  |
|  | 5 | Azione | L'utente si trova nella pagina principale dell'applicazione |  |  |  |
|  | 6 | Azione | L'utente naviga l'applicazione seguendo il percorso “Statistiche/Monitoraggio » Monitoraggio Provvedimenti” e scegliendo la statistica “Per Oggetti”. Inserire un "Intervallo di Tempo da verificare" e premere il tasto “Caricamento”. Selezionare l’opzione “Spuntare questa opzione per produrre anche stampa elenco Procedimenti pendenti alla fine del periodo” e premere il tasto “Conferma”. |  | Produzione del file Excel "Documento.xls" |  |
|  | 7 | Navigazione | Statistiche/Monitoraggio » Monitoraggio Provvedimenti |  |  |  |
|  | 8 | Azione | Scegliere la statistica “Per Oggetti”. Inserire un "Intervallo di Tempo da verificare" e premere il tasto “Caricamento”. Selezionare l’opzione “Spuntare questa opzione per produrre anche stampa elenco Procedimenti pendenti alla fine del periodo” e premere il tasto “Conferma”. |  | Produzione del file Excel "Documento.xls" |  |
|  | V | Verifica | Analizzare il file "server.log" e constatare che NON sia presente la dicitura "IJ000100: Closing a connection for you." |  |  |  |
| TF003.UC01 | REQ-SIE-006-03 |  | Verifica Inserimento Fissazione Udienza in SIUS per NON regressione dopo modifica query |  | Verifica di NON regressione: Verificare che nel sottosistema SIUS, nella fase di inserimento fissazione udienza, la ricerca dell'udienza dia risultati congrui con l'installazione precedente |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIUS come Tribunale di Sorveglianza | Dxxxxx (Tribunale di Sorveglianza) |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1 | Navigazione | Udienza » Fissazione Udienza |  | Visualizzazione pagina Inserimento Fissazione Udienza |  |
|  | 2 | Azione | Cliccare sul link Lista Udienze |  | Visualizzazione pagina Elenco Udienze |  |
|  | V | Verifica | Se il risultato della ricerca è non nullo, allora verificare che lo stesso output sia uguale a quello ottenuto con una precedente installazione |  |  |  |
|  | 3 | Azione | Se il risultato è nullo, allora modificare la data nel campo Visualizza le Udienze a partire dal e premere il tasto Visualizza |  |  |  |
|  | V | Verifica | Se il risultato della ricerca è non nullo, allora verificare che lo stesso output sia uguale a quello ottenuto con una precedente installazione |  |  |  |
| TF003.UC02 | REQ-SIE-006-03 |  | Verifica Trasmissione Foglio Complementare al SIC per NON regressione SiesEsecuzione |  | Verifica di NON regressione: Verificare che nel sottosistema SIUS, nella fase di trasmissione foglio complementare al SIC, l'operazione dia risultati congrui con l'installazione precedente |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIUS come Tribunale di Sorveglianza | Dxxxxx (Tribunale di Sorveglianza) |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1 | Navigazione | Ricerche e Visualizzazioni » Procedimento per n° SIUS |  | Visualizzazione pagina Ricerca Procedimento |  |
|  | 2 | Azione | Ricercare un provvedimento con almeno un provvedimento deposistato inserendo "Anno e Numero" negli appositi campi; premere il tasto "Ricerca" |  | Visualizzazione pagina Dettaglio Procedimento SIUS |  |
|  | V | Verifica | Verificare che la ricerca dia un risultato non nullo |  |  |  |
|  | 3 | Azione | Dal menù a scomparsa orizzontale selezionare la voce "Compilazione Foglio Complementare" e premer il tasto "Vai" |  | Visualizzazione pagina Compilazione Foglio Complementare |  |
|  | 4 | Azione | Nella pagina risultante, per il provvedimento depositato, nella colonna "Azioni" cliccare sull'icona "Compilazione Foglio Complementare" |  | Visualizzazione pagina Dettaglio Foglio Complementare |  |
|  | 5 | Azione | Nella pagina risultante cliccare sull'icona "Trasmissione Foglio Complementare al SIC" |  | Trasmissione effettuata |  |
|  | V | Verifica | Analizzare il file "server.log" e constatare che NON sia presente la dicitura "IJ000100: Closing a connection for you." |  |  |  |
|  | V | Verifica | Verificare che lo stesso risultato sia ottenuto anche con la precedente installazione |  |  |  |
| TF003.UC03 | REQ-SIE-006-03 |  | Verifica Impatto indicizzazione tabella STATO_PROCEDIMENTO |  | Verifica: Verificare che nel sottosistema SIEP, nella fase di ricerca fascicolo avanzata, i tempi di risposta siano migliori rispetto all'installazione precedente |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1 | Navigazione | Ricerche » Procedimento |  | Visualizzazione pagina Ricerca Procedimento |  |
|  | 2 | Azione | Scegliere "Avanzata" come Tipo Ricerca, inserire "Intervallo Procedimenti" e premere il tasto "Ricerca" |  | Visualizzazione pagina Elenco Procedimenti |  |
|  | R1 | Riciclo Script | Ripetere lo step precedente se la ricerca da un risultato nullo |  |  |  |
|  | V | Verifica | Se il risultato è non nullo, allora verificare chei tempi di risposta siano migliori rispetto all'installazione precedente |  |  |  |
| TF003.UC04 | REQ-SIE-006-03 |  | Verifica Impatto indicizzazione tabella SOGGETTO |  | Verifica: Verificare che nel sottosistema SIEP, nella fase di ricerca Procedimento per Soggetto, i tempi di risposta siano migliori rispetto all'installazione precedente |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1 | Navigazione | Ricerche » Procedimento Per Soggetto |  | Visualizzazione pagina Ricerca Procedimento per Soggetto |  |
|  | 2 | Azione | Inserire un valore nel campo "Cognome" e premere il tasto "Ricerca" |  | Visualizzazione pagina Elenco Soggetti con Procedimenti |  |
|  | R1 | Riciclo Script | Ripetere lo step precedente se la ricerca da un risultato nullo |  |  |  |
|  | V | Verifica | Se il risultato è non nullo, allora verificare chei tempi di risposta siano migliori rispetto all'installazione precedente |  |  |  |
| TF003.UC05 | REQ-SIE-006-03 |  | Verifica Impatto indicizzazione tabella REATO |  | Verifica: Verificare che nel sottosistema SIEP, nella fase di ricerca Procedimento per Soggetto, i tempi di risposta siano migliori rispetto all'installazione precedente |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1 | Navigazione | Ricerche » Procedimento Per Soggetto |  | Visualizzazione pagina Ricerca Procedimento per Soggetto |  |
|  | 2 | Azione | Inserire un valore nel campo "Cognome" e premere il tasto "Ricerca" |  | Visualizzazione pagina Elenco Soggetti con Procedimenti |  |
|  | R1 | Riciclo Script | Ripetere lo step precedente se la ricerca da un risultato nullo |  |  |  |
|  | V | Verifica | Se il risultato è non nullo, allora verificare chei tempi di risposta siano migliori rispetto all'installazione precedente |  |  |  |
| TF003.UC06 | REQ-SIE-006-03 |  | Verifica Impatto indicizzazione tabelle coinvolte nel package "PULISCI" e procedura "Pulisci_Evento" |  | Verifica: Verificare che nel sottosistema SIEP, nella fase di cancellazione di un evento di tipo "Ordine di Esecuzione", i tempi di risposta siano migliori rispetto all'installazione precedente |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura della Repubblica Presso il Tribunale Ordinario | Axxxxx (Procura della Repubblica Presso il Tribunale Ordinario) |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1 | Navigazione | Ordini di Esecuzione/Scarcerazione » Ordine di Esecuzione |  | Visualizzazione pagina Ricerca Procedimento |  |
|  | 2 | Azione | Inserire i valori (di un procedimento noto non definito) nel campo "Anno/Numero SIEP" e premere il tasto "Conferma" |  | Visualizzazione pagina Emissione Ordine di Esecuzione - Libero |  |
|  | R1 | Riciclo Script | Ripetere lo step precedente se la ricerca da un risultato nullo |  |  |  |
|  | 3 | Azione | Riempire i campi obbligatori della pagina prospettata e premere il tasto "Conferma" |  | Visualizzazione pagina Dettaglio Ordine Esecuzione Condannato … |  |
|  | V | Verifica | Verificare l'effettiva creazione dell'evento |  |  |  |
|  | 4 | Navigazione | Elenco dei Provvedimenti del PM |  | Visualizzazione pagina Elenco Provvedimenti PM |  |
|  | 5 | Azione | Nel campo "Azioni" in corrispondenza del provvedimento di "Ordine Esecuzione  per la carcerazione ..." creato nello step precedente, cliccare sull'icona di "Cancellazione" |  | Visualizzazione pagina Elenco Provvedimenti PM (senza il provvedimento cancellato) oppure pagina di Dettaglio Procedimento se era l'unico provvedimento del fascicolo |  |
|  | V | Verifica | Verificare chei tempi di risposta siano migliori rispetto all'installazione precedente |  |  |  |

## VerificheConformità

| Intervento |  |  | MEV 2019_006 SIUS Avvocati |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | SIUT-SIES-CT-1.0-20211011-Allegato_al_piano_test_006_SIUS_Avvocati.xlsx |  |  |  |  |
| ID | Tipo Verifica | Attributo | Indicatore | Descrizione tipo Verifica | Esito Verifica Fornitore | Esito Verifica Amministrazione |  |
| 001 | Adeguatezza delle funzionalità | Completezza funzionale | Copertura dei requisiti | Verifica del grado di copertura funzionale offerta sulla base dell’analisi dei requisiti, delle funzionalità e degli obiettivi richiesti | OK |  |  |
| 002 | Adeguatezza delle funzionalità | Correttezza funzionale | Aderenza ai requisiti | Verifica del grado con cui le funzionalità implementate rispettano i requisiti richiesti | OK |  |  |
| 003 | Adeguatezza delle funzionalità | Appropriatezza funzionale | Conformità alle normative | Verifica l’aderenza delle funzionalità implementate rispetto alle normative pertinenti | OK |  |  |
| 004 | Affidabilità | Robustezza | Robustezza del software | Verifica della capacità del sistema di gestire condizioni non previste dalle specifiche | OK |  |  |
| 005 | Manutenibilità | Analizzabilità | Leggibilità del codice | Verifica della facilità di comprensione del codice, per esempio con riferimento ai nomi utilizzati per i moduli, le funzioni e le variabili, ai commenti e alla dimensione dei moduli e delle funzioni | OK |  |  |
| 006 | Manutenibilità | Analizzabilità | Copertura documentazione tecnica | Verifica del livello di completezza della documentazione tecnica di moduli e funzioni | OK |  |  |
| 007 | Manutenibilità | Analizzabilità | Adeguatezza documentazione tecnica | Verifica della qualità descrittiva della documentazione tecnica di moduli e funzioni | OK |  |  |
| 008 | Manutenibilità | Verificabilità | Completezza dei test | Verifica del grado di copertura del codice sviluppato da parte di test (di varia natura, come test unitari, test di integrazione, test end-to-end, test di accettazione, test di regressione, test di qualità) | OK |  |  |

## SogliaAccettazione

| Intervento |  | MEV 2019_006 SIUS Avvocati |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  | SIUT-SIES-CT-1.0-20211011-Allegato_al_piano_test_006_SIUS_Avvocati.xlsx |  |  |  |  |  |  |
| Verifica Soglia di Accettazione |  |  |  |  |  | In Rosso le difformità che hanno superato il numero massimo ammissibile |  |  |
| Classe di rilevanza | Classe di gravità |  |  |  |  |  |  |  |
|  | 1 | 2 | 3 | 4 |  |  |  |  |
| A |  |  |  |  |  |  |  |  |
| B |  |  |  |  |  |  |  |  |
| C |  |  |  |  |  |  |  |  |
| Numero massimo di difformità ammesse |  |  |  |  |  |  |  |  |
| Classe di rilevanza | Classe di gravità |  |  |  |  |  |  |  |
|  | 1 | 2 | 3 | 4 |  |  |  |  |
| A |  |  |  |  |  |  |  |  |
| B |  |  |  |  |  |  |  |  |
| C |  |  | 8 |  |  |  |  |  |