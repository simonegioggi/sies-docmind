---
uniqueName: siut-siav-pt-2-0-20210431-analisi-dei-risultati-de
displayName: "SIUT SIAV PT 2 0 20210431 Analisi dei risultati dei Test di Performance del sist"
category: "GENERAL"
tags: []
---

# SIUT-SIAV-PT-2.0-20210431-Analisi dei risultati dei Test di Performance del sistema SIES-Avvocatura

> **File originale:** `MEV/SCHEDA_006/SIUT-SIAV-PT-2.0-20210431-Analisi dei risultati dei Test di Performance del sistema SIES-Avvocatura.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni

|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Alessio Papi – Julio Fortis –  Riccardo Barcaroli | Engineering |
| Verificato da | Vito Bufi
Alessandro Falleni
Fabio Gattamorta | Responsabile Manutenzione Sistemi Attuali
Referente Sicurezza
Referente PMO e Qualità |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 31/04/2021 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 19/10/2020 | Prima Emissione |  |
| 1.1 | 18/11/2020 | Riesecuzione Test |  |
| 1.2 | 25/02/2021 | Riesecuzione Test |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Salvatore Piazza | RTI |  | Technical Manager |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Francesco Rosati | RTI |  | Responsabile Manutenzione Correttiva
Referente Qualità e Sicurezza |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Responsabile PMO e Qualità |
| Alessandro Falleni | RTI |  | Referente Sicurezza |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |
| Luigi Buglione | RTI |  | Referente Metrico |




INDICE DEI CONTENUTI
1	Introduzione	5
1.1	Scopo del documento	5
1.2	Riferimenti	5
1.3	Glossario	5
1.3.1	Acronimi e abbreviazioni	5
2	Definizione dell’Obiettivo	6
3	Oggetto delle prove	7
4	Sistema Analizzato	9
5	Piano dei test	10
5.1	Software di base e Hardware	10
5.2	Ambiente Dati	10
5.3	Risultati dei test effettuati	11
5.3.1	Test del 16 marzo	11
5.3.2	Test del 17 marzo	13
6	Conclusioni	15
7	Allegati	16

# Introduzione
## Scopo del documento
Il documento riporta l’esito degli stress test condotti nei giorni 16 e 17 marzo sugli Application Server del Sistema Centrale e del distretto di Napoli, nonché sul Database Server, per rilevare il comportamento dell’applicativo SIES-Avvocatura in caso di un elevato carico di lavoro.

## Riferimenti
N.A.

## Glossario
## Acronimi e abbreviazioni
| Definizione | Descrizione |
| --- | --- |
| RNF | Requisito Non Funzionale |
| TNF | Test Non Funzionale |
| PT | Performance Test |
| GdL | Gruppo di Lavoro |


# Definizione dell’Obiettivo
Questo documento descrive la metodologia ed i risultati dell’analisi effettuata dal gruppo di lavoro relativamente ai risultati dei test effettuati sul sistema SIES-Avvocatura del distretto di Napoli in data 16 e 17 marzo 2021.
Lo scopo dei test era quello di verificare l’evoluzione del funzionamento e la capacità di sopportare un carico di lavoro di crescente intensità da parte del sistema SIES-Avvocatura, caratterizzato dalle componenti hardware e software installate presso il distretto di Napoli e presso il sistema centrale, a seguito delle prove già realizzate nel periodo Settembre/Ottobre 2020 e febbraio 2021. A tale scopo un carico di lavoro eterogeneo è stato appositamente generato per simulare l’attività degli utenti agli uffici del distretto di Napoli e degli avvocati con il fine di osservare la risposta del sistema, in termini prestazionali, al variare del numero di utenti concorrenti, così come l’impatto che questo poteva avere sia sui tempi delle risposte agli utenti stessi che sulle percentuali degli errori riportati dagli strumenti di test.
Va comunque precisato che, mentre il carico di lavoro degli utenti agli uffici del distretto di Napoli è stato generato basandosi sull’osservazione della reale attività di quest’ultimi per mezzo di un’analisi svolta sui file di Log collezionati durante due giornate di utilizzo del sistema in pre-esercizio, per quanto riguarda il carico di lavoro degli avvocati non è stato possibile fare una stima di quello che poteva essere il reale livello di concorrenza, ed è stato quindi scelto di far variare gradualmente il numero di utenti concorrenti partendo da un unico avvocato nel sistema fino al raggiungimento di un valore che ritenevamo adeguato per stressare il sistema.

# Oggetto delle prove
Costituiscono oggetto dei test, le funzioni sviluppate o modificate nell’ambito dell’intervento in modo end-to-end.
Non rientrano invece nell’ambito delle prove le funzioni e i meccanismi di interfaccia appartenenti ad altri sistemi o comunque preesistenti o estranei all’intervento in oggetto.
Seguendo la metodologia utilizzata nei test precedenti, i test sono stati eseguiti utilizzando due istanze dello strumento Apache JMeter al fine di simulare in maniera indipendente il carico di lavoro degli utenti agli uffici del distretto di Napoli e degli avvocati. In entrambe le istanze, in ogni istante di tempo sono state inviate le richieste da parte di un determinato numero di utenti concorrenti dipendentemente dal tempo di inizio delle rampe degli accessi per le due tipologie di utenti, dalla durata delle rampe e dal valore massimo impostato per queste due. Ognuno dei suddetti utenti selezionava la successiva azione da eseguire da una delle varie sequenze predefinite di azioni in accordo ad una distribuzione di probabilità che è stata definita sul carico di lavoro.
In particolare, ogni avvocato simulato esegue la seguente sequenza di azioni:

In particolare, ogni avvocato simulato esegue la seguente sequenza di azioni:
Ricerca per Estremi Procedimento
a seconda del risultato della ricerca:
Dettaglio Ordinanza
Dettaglio Decreto
Dettaglio Rinvio Udienza
Ricerca per Estremi Procedimento
Stampa Procedimento
Accesso Dati Soggetto

Per ogni azione sono stati scelti dei valori di think-time basati su una stima calcolata a partire dalla misurazione dei tempi registrati durante la simulazione della navigazione effettuata manualmente da personale esperto della logica di business applicativa.
La distribuzione scelta per i precedenti test era stata calcolata a valle dell’osservazione e successiva computazione dei valori delle media e delle deviazioni standard è quella normale.

| Azione | Media (sec.) | Varianza (sec.) |
| --- | --- | --- |
| Ricerca per Estremi Procedimenti | 12 | 2 |
| Dettaglio Ordinanza
Dettaglio Decreto
Dettaglio Rinvio Udienza | 25 | 8 |
| Ricerca per Estremi Procedimenti | 15 | 5 |
| Stampa Procedimento | 5 | 2 |
| Accesso Dati Soggetto | 5 | 2 |


Per quanto riguarda la simulazione degli utenti agli uffici del distretto di Napoli, le sequenze di azioni da far eseguire in corrispondenza delle richieste inoltrate da questa tipologia di utenti sono state fornite dal GdL di Napoli per i precedenti test di settembre/ottobre. Consistono in 11 sequenze di azioni con differente probabilità di venir selezionate dagli utenti simulati, e che erano state indicate dal GdL di Napoli come maggiormente rappresentanti dalla loro attività.
Insieme al responsabile al D.G.S.I.A che aveva coordinato le attività in gennaio 2019, era stato deciso di eseguire un’analisi diretta su due file di Log raccolti in due giornate di normale operatività degli utenti agli uffici del distretto di Napoli con l’obiettivo di individuare i valori di think-time da associare alle azioni incluse nelle suddette sequenze per poter poi configurare gli script di test in maniera tale da simulare con un certo livello di affidabilità il carico di lavoro generato da questi utenti.
In tale senso era stata prodotta una relazione tecnica con titolo “Profilazione dell’attività degli utenti del sistema SIES-Avvocatura del distretto di Napoli ed identificazione dei valori di think-time” in cui è ampiamente argomentata e motivata la metodologia adottata per l’estrazione di tali valori partendo dalle informazioni contenute nei file di Log.

# Sistema Analizzato
Il sistema SIES-Avvocatura è diviso in:

Sistema Centrale - SIES-Avvocatura
Sistema Distrettuale - SIES

Per quanto riguarda il Sistema Centrale, l’interazione degli avvocati con il sistema SIES-Avvocatura passa per il PST, il quale mette a disposizione il servizio di autenticazione degli utenti (proxy PST) che comunica con il Sistema di Consultazione dei Procedimenti che a sua volta agisce da gateway per le richieste inoltrate dagli avvocati in maniera coerente a quanto riportato nel documento di Analisi Funzionale “Sistema per la Consultazione, da parte degli Avvocati, dei Procedimenti di Sorveglianza” (cod. SIGI-PNL-AF, ver. 2.1, 30/11/2016).

Nell’effettuare i test in oggetto, abbiamo bypassato il proxy accedendo direttamente al SIES-Avvocatura.


# Piano dei test
## Software di base e Hardware
Sulla base degli applicativi oggetto del contratto e delle aree funzionali, la convenzione per l’identificazione dei requisiti è riportata di seguito.

Questa attività è stata eseguita utilizzando il seguente strumento Open Source:
Apache JMeter v5.3

Le caratteristiche tecniche della macchina di controllo utilizzata per l’esecuzione dei test sono:

Processore: 2 processori Intel Xeon E7-4850 v3 @2.20GHz
Memoria: 4GB RAM
Sistema Operativo: Windows Server 2016 (64bit)

## Ambiente Dati
Le prove sono state realizzate dalla macchina con IP: 10.7.111.10.

Le destinazioni del PT sono stati individuati i seguenti target:

Per l’esecuzione dello script SIUS_v3_UDS.jmx il server di destinazione era https://10.6.202.158:8443/PST/SIUS/login

Per l’esecuzione dello script SIEP_SIUS_SIGE.jmx il server di destinazione era http://10.7.111.21:9000/

Internamente l’applicativo SIUS Distrettuale utilizzava il database server Oracle 12.1 usato per le campagne di test, residente sul server 10.7.111.20, aveva le seguenti caratteristiche hardware e software:

| Host Name | Platform | CPUs | Cores | Sockets | Memory (GB) |
| --- | --- | --- | --- | --- | --- |
| nasiesdbsc6 | Linux x86 64-bit | 16 | 16 | 8 | 23.47 |



I CSV con i dati di test utilizzati sono:

Per SIUS_v3_UDS.jmx:

AVV_CON_CF_TDS-UDS.csv

Per SIEP_SIUS_SIGE.jmx:



Per ricavare le istruzioni SQL più pesanti, per ogni singolo lancio dei test è stato usato lo strumento di Oracle:
“AWR Report” abbinato all’”ADDM”.

Si riporta infine il riepilogo dei server coinvolti nei performance test:

|  |
| --- |
| Macchina di Controllo (macchina ponte - 10.7.111.10) |
| CL_NA_SIES_DB_PRO  (macchina DB - 10.7.111.20) |
| CL_NASIESAPP_PRO    (application server - 10.7.111.21) |



## Risultati dei test effettuati
Si riportano di seguito i risultati di sintesi dei performance test effettuati sul sistema SIES-Avvocatura nelle due giornate del 16 e 17 marzo 2021.

## Test del 16 marzo
Nella giornata del 16 marzo sono stati rieffettuati sei differenti test, modulando il numero di utenti distrettuali e quelli centrali.

Si è evidenziato che oltre una certa soglia di utenti centrali, l’Application Server Centrale va in sofferenza (test 5) in quanto viene superata la soglia del massimo numero di processi accettati dal sistema.

| N° | Tipologia Test | Ora Inizio | Ora fine | Esito | Risultato | Note |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | 500 Distrettuali e 500 Centrali | 11:35 | 12:06 | OK | Centrale: Richieste corrette al 99,6%. Tempi in crescita lineari con l'aumento degli utenti. La stampa si assesta intorno ai 18 secondi, la ricerca estremi procedimento intorno agli 80 secondi e dettaglio ordinanza a 124 secondi; la stampa 18 secondi.  Il resto dei tempi di risposta risulta al disotto del secondo.
Distrettuale: Questo lancio presenta un tasso di richieste corrette più basso rispetto al centrale: 96.92%. Picchi anomali in cancellazione procedimento. (318 e 473 sec) e click sorveglianza  si attesta intorno ai 119 secondi. |  |
| 2 | 1000 Centrali | 12:24 | 12:47 | OK | Centrale: Questo lancio presenta un tasso di richieste corrette pari a 99,52%. Presenta dei  tempi di risposta di 294 secondi per "dettaglio ordinanza" e  di 170 secondi per “ricerca estremi procedimento”; la stampa impiega invece solo 3 secondi; il resto dei tempi di risposta risulta al disotto del secondo. |  |
| 3 | 110 Distrettuali e 200 Centrali | 13:07 | 13:37 | OK | Centrale: Richieste corrette al 99,58%,  con tempi di risposta al disotto del secondo, ad esclusione di “Dettaglio ordinanza" che ha risposto in  28 secondi, “ricerca estremi procedimento” in 18 secondi e la stampa in solo 3 secondi.
Distrettuale: Richieste corrette al 96,76%. Tempi in crescita lineari con l'aumento degli utenti e tempi di risposta al disotto dei 5 secondi ad eccezione di "ricerca soggetto che ha impiegato 17 secondi. |  |
| 4 | 110 Distrettuali e 500 Centrali | 13:46 | 14:17 | OK | Centrale: Richieste corrette al 99,56%. Tempi in crescita lineari con l'aumento degli utenti e 
tempi di risposta per “Dettaglio ordinanza” intorno ai 130 secondi, “Ricerca estremi procedimento” 78 secondi, “Stampa” 8 secondi; i tempi di risposta  è al disotto dei 5 secondi. Il resto dei tempi di risposta risulta al disotto del secondo.
Distrettuale: Richieste corrette al 96,76%. Tempi in crescita lineari con l'aumento degli utenti e tempi di risposta per "ricerca soggetto" intorno ai 18 secondi mentre il resto dei processi  è al disotto dei 5 secondi. |  |
| 5 | 500 Centrali | 14:24 | 14:54 | OK | Centrale: Richieste corrette al 99,6%. Tempi in crescita lineari con l'aumento degli utenti e tempi di risposta dei vari processi al di sotto del secondo. Tempi di risposta di 125 secondi per “Dettaglio ordinanza”, 73 secondi per “Ricerca estremi procedimento” ed 8 secondi per la stampa. |  |
| 6 | 550 Distrettuali | 15:02 | 15:32 | OK | Distrettuale: Richieste corrette al 96,69%. Tempi in crescita lineari con l'aumento degli utenti e tempi di risposta al disotto dei 3 secondi ad eccezione di “Ricerca soggetto” che si attesta a 16 secondi. |  |
| 7 | 55 Distrettuali e 50 Centrali | 15:39 | 16:10 | OK | Centrale: Richieste corrette al 99,65%. Tempi di risposta al disotto di un secondo, ad eccezione "ricerca soggetto" (5 secondi) e stampa (2 secondi). Inoltre, il tempo di risposta è costante, ossia 1 utente o 50 non impattano sulle performance del sistema.
Distrettuale: Richieste corrette al 96,67%. Tempi di risposta al disotto dei 4 secondi, ad esclusione di  "ricerca soggetto" che impiega 17 secondi. | Vi è stato un picco anomalo alla fine del test; non vi è stata saturazione del sistema, si suppone che possa essere stato un problema java per distruggere i thread ancora attivi. |
| 8 | 600 Distrettuali | 16:24 | 16:54 | OK | Distrettuale: Richieste corrette al 95,01%. Sono stati testati i seguenti 3 processi: “Ricerca soggetto” che ha impiegato 213 secondi, “click sorveglianza” e “cancellazione provvedimento” che hanno risposto in meno di un secondo. |  |




## Test del 17 marzo
Nella campagna di test del 17 marzo 2021 sono stati effettuati dei test specifici per analizzare le performance del sistema sotto condizioni diverse; ad esempio nei primi due test si analizza il sistema con un RampUp iniziale di 15 minuti, poi 30 minuti di lavoro misto e i Distrettuali abbandonano, infine 15 minuti di lavoro da soli dei Centrali; nei test successivi invece si utilizza un RampUp è di 240 secondi per vedere la risposta a fronte di funzionalità specifica.


| N° | Tipologia Test | Ora Inizio | Ora fine | Esito | Risultato | Note |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | 220 Distrettuali e 200 Centrali | 11:01 | 12:47 | OK | Centrale: Richieste corrette al 99,61%. Tempi in crescita lineari con l'aumento degli utenti e tempi di risposta al disotto del  second0, ad esclusione di “Dettaglio ordinanza” che impiega 27 secondi, “Ricerca estremi procedimento” in 16 e la stampa in 4 secondi.
Distrettuale: Richieste corrette al 96,46%. Tempi in crescita lineari con l'aumento degli utenti e tempi di risposta al disotto dei 4 secondi, eccetto "ricerca soggetto" che si assesta sui 25 secondi. | 200 Centrali con RampUp di 15 minuti, poi 30 minuti di lavoro solo Centrali, poi 220 Distrettuali con RampUp di 15 minuti, poi 30 minuti di lavoro misto e i Distrettuali abbandonano, infine 15 minuti di lavoro da soli dei Centrali |
| 2 | 550 Distrettuali e 500 Centrali | 13:01 | 14:47 | OK | Centrale: Richieste corrette al 99,44%. Tempi in crescita lineari con l'aumento degli utenti e tempi di risposta al disotto del secondo. Tempi maggiori per “Dettaglio ordinanza” (125 secondi) e “Ricerca estremi procedimento” (65 secondi); stampa in 7 secondi.
Distrettuale: Richieste corrette al 94,62%. Tempi in crescita lineari con l'aumento degli utenti e tempi di risposta al disotto di 8 secondi, ad eccezione di  "ricerca soggetto" che impiega 40 secondi. | Test della durata di un’ora e 46 minuti per approfondire il comportamento del Centrale in funzione del carico introdotto dal Distrettuale. 
500 Centrali con RampUp di 15 minuti, poi 30 minuti di lavoro solo Centrali, poi 550 Distrettuali con RampUp di 15 minuti, poi 30 minuti di lavoro misto e i Distrettuali abbandonano, infine 15 minuti di lavoro da soli dei Centrali |
| 3 | 100 Centrali | 15:02 | 15:17 | OK | Centrale: E’ stato testata in particolare la “stampa procedimento” che si è mantenuta entro i 128 millisecondi, così come il login ed il logout che si sono assestate rispettivamente a 244 e 270 millisecondi. |  |
| 4 | 110 Distrettuali | 15:32 | 16:47 | OK | Distrettuale: E’ stata testata specificatamente la funzione “Ricerca soggetto”: i tempi sono stati costanti con risposta di 11 secondi e richieste corrette al 100%. | Vi è stato un picco anomalo alla fine del test; non vi è stata saturazione del sistema, si suppone che possa essere stato un problema java per distruggere i thread ancora attivi. |
| 5 | 500 Centrali | 16:29 | 16:45 | OK | Centrale: Anche in questo caso sono stati effettuati dei test specifici, andando ad analizazre i tempi di risposta di “Dettaglio ordinanza” e “Ricerca estremi procedimento” con tempi di risposta rispettivamente di 100 e 61 secondi. La percentuale di richieste corrette è stata del 98,32% |  |
| 6 | 300 Centrali | 16:54 | 17:09 | OK | Centrale: Test analogo al precedente ma con un numero inferiore di utenti. Sono state perciò  effettuati test specifici solo per “Dettaglio ordinanza” e “Ricerca estremi procedimento” con tempi di risposta rispettivamente di 47 e 30 secondi. La percentuale di richieste corrette è stata del 99,59% |  |

# Conclusioni
Dai risultati dei test condotti e descritti nel documento, emergono le seguenti considerazioni:

I test confermano pienamente la bontà del tuning effettuato a valle dei test del 5 Novembre 2020 e del 16-24 Febbraio 2021
Le percentuali di errore sono ulteriormente diminuite rispetto ai test di febbraio.
Nei test iniziali di ottobre diversi test si sono interrotti a causa di saturazione del sistema, il fenomeno è andato diminuendo nei test di febbraio ma ancora presente in alcuni casi ed ora tutti i test sono andati bene, sia gli application server e sia il database server non sono mai andati in crash né hanno avuto problemi di saturazione della CPU.
I tempi di risposta di tutte le funzionalità si sono ulteriormente ridotti; ad esempio il processo di stampa ad ottobre 2020 impiegava non meno di 220 secondi per passare a febbraio a 32 secondi ed assestarsi sui 10 secondi per il Centrale. Analogamente i tempi relativi al resto dei processi è passato ai 71 secondi di ottobre, ai 6 di febbraio ai 3 secondi degli ultimi test (test con 550 centrali e 550 distrettuali). Restano invece significativi i tempi di “Dettaglio ordinanza” e “Ricerca estremi procedimento”, rispettivamente di 125 e 73 secondi.
Inizialmente il sistema consentiva massimo 100 utenti di picco del Centrale sul sistema di produzione (dati del 2019); negli ultimi test del 16  e 17 marzo ora 300 utenti sul Centrale dell’ambiente di test con tempi di risposta ottimali (maggior parte dei processi risponde entro i 4 secondi)
Ora fino a 550 distrettuali non c’è più influenza sul Centrale.
Rimane inalterato il problema dell’errato uso delle variabili di bind, che impatta inevitabilmente sul consumo di CPU


# Allegati
Sul Portale della Fornitura, nella Cartella:

SIUT > 07 - MEV > 2019_006_Ottimizzazione SIUS Avvocati > 06_Test_Performance > Risultati 16-17 Marzo


sono stati caricati i seguenti documenti contenenti il dettaglio dei test, sia lato application server che lato database.

I documenti sono i seguenti:

AnalisiStressTest_16_17_Marzo_2021.docx
SIES Analisi.rar