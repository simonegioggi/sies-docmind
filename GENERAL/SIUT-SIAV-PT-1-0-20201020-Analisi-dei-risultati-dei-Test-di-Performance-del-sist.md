---
uniqueName: siut-siav-pt-1-0-20201020-analisi-dei-risultati-de
displayName: "SIUT SIAV PT 1 0 20201020 Analisi dei risultati dei Test di Performance del sist"
category: "GENERAL"
tags: []
---

# SIUT-SIAV-PT-1.0-20201020-Analisi dei risultati dei Test di Performance del sistema SIES-Avvocatura

> **File originale:** `MEV/SCHEDA_006/SIUT-SIAV-PT-1.0-20201020-Analisi dei risultati dei Test di Performance del sistema SIES-Avvocatura.docx`  
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
| Elaborato da | Alessio Papi – Riccardo Barcaroli – Julio Fortis |  |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi Attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 20/10/2020 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 19/10/2020 | Prima Emissione |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Pasquale Lamattina | RTI |  | Referente Tecnico |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Fabio Mazzocchi | RTI |  | Responsabile Manutenzione Correttiva |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Responsabile PMO |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Edoardo Lamuraglia | RTI |  | Referente qualità |
| Francesco Rosati | RTI |  | Referente qualità |


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
5.3	Risultati di sintesi	12
5.3.1	Application Server	12
5.3.2	Database Server	14
5.3.2.1	Query con ordinamenti onerosi e con Hash Join	14
5.3.2.2	Il binding delle variabili	22
5.4	Risultati di dettaglio	22
5.4.1	Test n°1: 50 utenti Distrettuali e 50 Avvocati per un intervallo di 1 ora	23
5.4.1.1	Sistema Centrale	23
5.4.1.2	Sistema Distrettuale	25
5.4.1.3	Database	30
5.4.2	Test n°2: 110 utenti Distrettuali e 200 Avvocati per un intervallo di 1 ora	33
5.4.2.1	Sistema Centrale	33
5.4.2.2	Sistema Distrettuale	35
5.4.2.3	Database	42
5.4.3	Test n°3: 110 utenti Distrettuali e 500 Avvocati per un intervallo di 1 ora	44
5.4.3.1	Sistema Centrale	44
5.4.3.2	Database	46
5.4.4	Test n°4: 500 Avvocati per un intervallo di 30 minuti	48
5.4.4.1	Sistema Centrale	48
5.4.4.2	Database	51
5.4.5	Test n°5: 550 utenti Distrettuali per un intervallo di 30 minuti	53
5.4.5.1	Sistema Distrettuale	53
5.4.5.2	Database	59
5.4.6	Test n°6: 1000 Avvocati per un intervallo di 30 minuti	62
5.4.6.1	Sistema Centrale	62
5.4.6.2	Database	64
5.4.7	Test n°7: 110 utenti Distrettuali e 500 Avvocati per un intervallo di 2 ore	66
5.4.7.1	Sistema Centrale	66
5.4.7.2	Sistema Distrettuale	69
5.4.7.3	Database	75
6	Conclusioni	78

# Introduzione
## Scopo del documento
Il documento riporta l’esito degli stress test condotti nei giorni 30 Settembre, 1 Ottobre e 5 Ottobre sull’Application Server e sul Database Server, per rilevare il comportamento dell’applicativo SIES-Avvocatura in caso di un elevato carico di lavoro.

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
Questo documento descrive la metodologia ed i risultati dell’analisi effettuata dal gruppo di lavoro relativamente ai risultati dei test effettuati sul sistema SIES-Avvocatura del distretto di Napoli in data 30 Settembre 2020, 1 e 5 Ottobre 2020.
Lo scopo dei test era quello di verificare l’evoluzione del funzionamento e la capacità di sopportare un carico di lavoro di crescente intensità da parte del sistema SIES-Avvocatura, caratterizzato dalle componenti hardware e software installate presso il distretto di Napoli e presso il sistema centrale. A tale scopo un carico di lavoro eterogeneo è stato appositamente generato per simulare l’attività degli utenti agli uffici del distretto di Napoli e degli avvocati con il fine di osservare la risposta, in termini prestazionali, del sistema al variare del numero di utenti concorrenti, così come l’impatto che questo poteva avere sia sui tempi delle risposte agli utenti stessi che sulle percentuali degli errori riportati dagli strumenti di test.
Va comunque precisato che, mentre il carico di lavoro degli utenti agli uffici del distretto di Napoli è stato generato basandosi sull’osservazione della reale attività di quest’ultimi per mezzo di un’analisi svolta sui file di Log collezionati durante due giornate di utilizzo del sistema in pre-esercizio previste nei precedenti test del 23/01/2019, per quanto riguarda il carico di lavoro degli avvocati non è stato possibile fare una stima di quello che poteva venire ad essere il reale livello di concorrenza, ed è stato quindi scelto di far variare gradualmente il numero di utenti concorrenti partendo da un unico avvocato nel sistema fino al raggiungimento di un valore che ritenevamo adeguato per stressare il sistema.

# Oggetto delle prove
Costituiscono oggetto dei test, le funzioni sviluppate o modificate nell’ambito dell’intervento in modo end-to-end.
Non rientrano invece nell’ambito delle prove le funzioni e i meccanismi di interfaccia appartenenti ad altri sistemi o comunque preesistenti o estranei all’intervento in oggetto.
Seguendo la metodologia utilizzata nei test precedenti del 23/01/2019, i test sono stati eseguiti utilizzando due istanze dello strumento Apache JMeter al fine di simulare in maniera indipendente il carico di lavoro degli utenti agli uffici del distretto di Napoli e degli avvocati. In entrambe le istanze, ad ogni istante di tempo sono state inviate le richieste da parte di un determinato numero di utenti concorrenti dipendentemente dal tempo di inizio delle rampe degli accessi per le due tipologie di utenti, dalla durata delle rampe e dal valore massimo impostato per queste due. Ognuno dei suddetti utenti selezionava la successiva azione da eseguire da una delle varie sequenze predefinite di azioni in accordo ad una distribuzione di probabilità che è stata definita sul carico di lavoro.
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
La distribuzione scelta per i precedenti test del 23/01/2019 era stata calcolata a valle dell’osservazione e successiva computazione dei valori delle media e delle deviazioni standard è quella normale.

| Azione | Media (sec.) | Varianza (sec.) |
| --- | --- | --- |
| Ricerca per Estremi Procedimenti | 12 | 2 |
| Dettaglio Ordinanza
Dettaglio Decreto
Dettaglio Rinvio Udienza | 25 | 8 |
| Ricerca per Estremi Procedimenti | 15 | 5 |
| Stampa Procedimento | 5 | 2 |
| Accesso Dati Soggetto | 5 | 2 |


Per quanto riguarda la simulazione degli utenti agli uffici del distretto di Napoli, le sequenze di azioni da far eseguire in corrispondenza delle richieste inoltrate da questa tipologia di utenti sono state fornite dal GdL di Napoli per i precedenti test del 23/01/2019. Consistono in 11 sequenze di azioni con differente probabilità di venir selezionate dagli utenti simulati, e che erano state indicate come maggiormente rappresentanti dalle attività svolte sul distretto..
Insieme al responsabile al D.G.S.I.A che aveva coordinato le attività in gennaio 2019, era stato deciso di eseguire un’analisi diretta su due file di Log raccolti in due giornate di normale operatività degli utenti agli uffici del distretto di Napoli con l’obiettivo di individuare i valori di think-time da associare alle azioni incluse nelle suddette sequenze per poter poi configurare gli script di test in maniera tale da simulare con un certo livello di affidabilità il carico di lavoro generato da questi utenti.
In tale senso era stata prodotta una relazione tecnica con titolo “Relazione Tecnica - Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio 2019” in cui è ampiamente argomentata e motivata la metodologia adottata per l’estrazione di tali valori partendo dalle informazioni contenute nei file di Log.

# Sistema Analizzato
Il sistema SIES-Avvocatura è diviso in:
Sistema Centrale
Sistema Distrettuale

L’interazione degli avvocati con il sistema SIES-Avvocatura passa per il sistema centrale, il quale mette a disposizione il servizio di autenticazione degli utenti (proxy PST) che comunica con il Sistema di Consultazione dei Procedimenti che a sua volta agisce da gateway per le richieste inoltrate dagli avvocati in maniera coerente a quanto riportato nel documento di Analisi Funzionale “Sistema per la Consultazione, da parte degli Avvocati, dei Procedimenti di Sorveglianza” (cod. SIGI-PNL-AF, ver. 2.1, 30/11/2016) redatto da Engineering.
Diversamente, le credenziali degli utenti agli uffici del distretto di Napoli sono già accreditate al sistema SIES-Avvocatura distrettuale e quindi sufficienti ad abilitare l’inoltro diretto delle richieste una volta stabilita la connessione al sistema.

Si presenta a continuazione il diagramma architetturale del sistema:


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

Internamente l’applicativo SIUS utilizzava il database server Oracle 12.1 usato per le campagne di test, residente sul server 10.7.111.20, aveva le seguenti caratteristiche hardware e software:

| Host Name | Platform | CPUs | Cores | Sockets | Memory (GB) |
| --- | --- | --- | --- | --- | --- |
| nasiesdbsc6 | Linux x86 64-bit | 16 | 16 | 8 | 23.47 |



I CSV con i dati di test utilizzati sono:

Per SIUS_v3_UDS.jmx:

AVV_CON_CF_TDS-UDS.csv

Per SIEP_SIUS_SIGE.jmx:



Per ricavare le istruzioni SQL più pesanti, per ogni singolo lancio dei test è stato usato lo strumento di Oracle:
“AWR Report” abbinato all’”ADDM”.

Da quanto raccolto dagli “AWR Report” per ogni campagna di test, nel capitolo seguente si mostrano sia le metriche più significative, che meglio descrivono l’impatto del carico di lavoro generato dagli stress test sull’istanza, sia le istruzioni SQL più onerose con i relativi tempi di esecuzione e, infine, lo stato del sistema operativo durante il picco di attività rilevate sul sistema.

Si riporta infine il riepilogo dei server coinvolti nei perforance test:

|  |
| --- |
| Macchina di Controllo (macchina ponte - 10.7.111.10) |
| CL_NA_SIES_DB_PRO  (macchina DB - 10.7.111.20) |
| CL_NASIESAPP_PRO    (application server - 10.7.111.21) |



## Risultati di sintesi
Si riportano di seguito i risultati di sintesi dei performance test effettuati sull’Application Server e sul database Server.

## Application Server
Analizzando il comportamento del sistema in funzione del crescente numero di utenti concorrenti osservando per prima cosa l’utilizzazione delle risorse nelle macchine predisposte per ospitare l’applicazione SIES-Avvocatura distrettuale e quelli centrali si osservano i seguenti tempi di risposta:



È evidente come il rapido aumento delle richieste in ingresso abbia avuto un notevole impatto anche sui tempi medi di risposta alle richieste degli utenti del sistema centrale, provocando un sostanziale cambiamento nel trend della crescita delle curve dei tempi medi di risposta alle richieste di tali utenti nel tempo.

In particolare, da tale comportamento si evince dunque la presenza di una problematica prestazionale connessa all’implementazione delle operazioni effettuate durante l’esecuzione dei processi associati a “ricerca procedimenti stampa”.

Osservando i tempi medi di risposta alle richieste degli altri processi analizzati, possiamo notare come siano caratterizzate da tempi che crescono in maniera lineare con l’aumentare del numero degli utenti concorrenti fino ad assumere valori nell’ordine dei minuti, per esempio “dettaglio del soggetto” e “dettaglio ordinanza”, mentre altre richieste, come quelle legate al login o alla ricerca dei soggetti, sono caratterizzate da tempi che si mantengono costanti e maggiormente contenuti, anche se generalmente elevati.


Per quanto riguarda invece gli utenti degli uffici del distretto di Napoli nel sistema distrettuale, il numero delle richieste inviate al sistema cresce in maniera proporzionale con l’aumentare del numero di utenti concorrenti nel tempo, ma esiste una problematica prestazionale connessa all’implementazione delle operazioni effettuate durante l’esecuzione dei processi associati alla ricerca del soggetto:



Se osserviamo i tempi medi di risposta alle richieste degli altri processi analizzati del sistema distrettuale, possiamo notare come in questo caso siano caratterizzate da tempi che crescono in maniera lineare con l’aumentare del numero degli utenti concorrenti fino ad assumere valori comunque in generale al di sotto del minuto (per esempio “ricerca singolo procedimento”.
In particolare, i tempi medi di risposta per il click sulla ricerca e la ricerca avanzata, aumentano inizialmente con il numero di utenti, per dopo ridursi a un valore costante nell’ordine dei 5 secondi.

Infine, le altre richieste, come quelle legate al login, agli inserimenti, all’iscrizione del procedimento, all’ordine di esecuzione o anche le ricerche, sono caratterizzate da tempi che si mantengono costanti e generalmente bassi.




Nella tabella seguente sono elencate le pagine testate con evidenti problemi prestazionali in relazione all’intervento in oggetto:
| Funzionalità | Funzionalità | Media dei tempi massimi di risposta |
| --- | --- | --- |
| Elenco di funzionalità che presentano problemi di performance | Elenco di funzionalità che presentano problemi di performance | Elenco di funzionalità che presentano problemi di performance |
| 1 | /PST/SIUS/ricerca/procedimenti/stampa (stampa procedimento) | 222291ms |
| 2 | /jsp/Main (ricerca soggetto) | 303460ms |
| 3 | /PST/SIUS/ricerca/procedimenti/dettaglio (dettaglio ordinanza) | 132114ms |
| 4 | /PST/SIUS/ricerca/procedimenti/exec (ricerca estremi procedimento) | 77719ms |
| 5 | /PST/SIUS/ricerca/procedimenti/dettaglio (dettaglio procedimento) | 79161ms |



## Database Server
Nei paragrafi seguenti vengono riportati i due aspetti che si è visto avere maggior impatto sui risultati dei performance test.

## Query con ordinamenti onerosi e con Hash Join
Nella tabella seguente si riportano le query che nelle campagne di test evidenziano ordinamenti ed un numero di hash join importanti ed eseguite molte volte, tanto da assurgere tra le query con il più alto consumo di tempo speso dal database nell’esecuzione di istruzioni SQL in generale. L’onerosità è indotta da un lato dal numero elevato dei campi in SELECT e dalla loro tipologia per gli ordinamenti (ci sono da 45 a più di 55 campi molti dei quali alfanumerici piuttosto grandi), e dall’altro al numero di hash join usati nei piani di esecuzione delle query. Nella tabella non si riportano tutte le istruzioni SQL segnalate dai report AWR e che richiedono ordinamenti o hash join, ma un campione rappresentativo in quanto le stesse non sfruttando il bind delle variabili, puntualmente costringono il database ad effettuarne il parsing (hard parse), sebbene la struttura delle query sia identica ad altre query già ottimizzate (cambiano infatti solamente i valori in chiaro delle variabili (literal) nei filtri).
Alcune delle query con ordinamenti importanti e con hash join servono per restituire i dati ordinati in blocchi di 20 occorrenze, al fine di consentire la paginazione all’utente che utilizza l’applicazione: ad esempio la query ‘4k0t94xwxyubm’. Queste query hanno ben 45 campi in SELECT, anche di tipo VARCHAR2, rendendo dispendioso l’ordinamento anche di sole poche occorrenze. Osservando bene questa tipologia di query, si può constatare che l’ordinamento così come scandito dalla clausola “order by” non produce effetti aldilà del semplice consumo di risorse: infatti i campi indicati per l’ordinamento sono campi a valore fisso in quanto sono gli stessi campi filtrati nella clausola where dell’istruzione SQL. Di fatto si esegue l’ordinamento rispetto a due campi che assumono il medesimo valore per tutte le occorrenze ritornate; dunque o l’ordinamento deve essere perfezionato aggiungendo altri campi alla clausola “order by” oppure può essere rimosso, riducendo così il numero di ordinamenti onerosi inviati al database.
Questo tipo di query si può ottimizzare riducendo, se possibile, i campi soggetti ad ordinamento e tramite indici opportuni o con suggerimenti per l’ottimizzatore, hint, per ridurre il numero di hash join.
Altre query, come ad esempio quella identificata dal codice ‘45s6ah4bhak7d’, servono unicamente per trovare il numero (count()) di occorrenze tornate dalle query usate per paginare i dati come quella descritta al paragrafo precedente. Due sono le anomalie riscontrate in questo caso:
non serve effettuare alcun ordinamento se serve il solo conteggio delle occorrenze totali che l’applicazione deve paginare, quindi la clausola “order by” si può togliere dall’istruzione SQL senza compromettere il risultato finale
la query in realtà non è necessaria, in quanto per conoscere le occorrenze totali trovate dalle query di paginazione è sufficiente inserire direttamente in queste ultime un campo in più contenente l’istruzione “count(*) over()”, evitando così l’esecuzione, tra l’altro onerosa, di una query ad hoc per contare le occorrenze trovate

| SQL ID | Istruzione SQL |
| --- | --- |
| g3w1xqyu26u2q | SELECT /*+ optimizer_features_enable('12.1.0.2') */ DISTINCT GP.ID_GENERALE_PROCEDIMENTO, FASC.ID_FASCICOLO_SIUS ID_FASCICOLO_SIUS, FASC.FAS_SIE_ID_FASCICOLO_SIEP ID_FASCICOLO_SIEP, FASC.CHIAVE_ANNO CHIAVE_ANNO, FASC.DATA_ISCRIZIONE DATA_ISCRIZIONE, FASC.CHIAVE_PROGR CHIAVE_PROGR, SOGG.ID_SOGGETTO ID_SOGGETTO, SOGG.COGNOME COGNOME, SOGG.NOME NOME, TO_CHAR(SOGG.DATA_NASCITA, 'dd/mm/yyyy') DATA_NASCITA, DECODE(DESCR_COM_NASCITA.DESCRIZIONE, NULL, DESC_COMUNE_NASCITA_ESTERO, DESCR_COM_NASCITA.DESCRIZIONE) DESCR_COMUNE_NASCITA, SOGG.COD_PROVINCIA_NASCITA, NAZIONE.RV_MEANING NAZIONE_NASCITA, SOGG.COD_FISCALE, SOGG.COD_AFIS, SOGG.ANNO_NASCITA, SOGG.MESE_NASCITA, ETA_PRESUNTA_ANNI, ETA_PRESUNTA_MESI, DATA_NASCITA_PRESUNTA, SOGG.PATERNITA, SOGG.COGNOME_MADRE, SOGG.NOME_MADRE, SOGG.SESSO, SOGG.NOTE, FLAG_PRESENZA_FASCICOLO, DESCR_OGGETTO_PROCEDIMENTO.RV_MEANING CONTENUTO, POS_GIURIDICA.RV_MEANING DESCR_POS_GIURIDICA, DESCR_COM_UFF.DESCRIZIONE DESCR_COMUNE_UFFICIO , GP.COD_POSIZIONE_GIURIDICA, GP.COD_OGGETTO_PROCEDIMENTO, NVL(GP.DESCR_MITTENTE, '-') DESCR_MITTENTE, GP.DATA_FINE_PENA, ID.DESCRIZIONE, ISD.RV_MEANING || ' DI ' || ID.DESCRIZIONE IST_DET_ID_ISTITUTO_DETENZIONE, LD.NOTE NOTE_DETENZIONE, LD.DATA_INIZIO_DETENZIONE, LD.DATA_FINE_DETENZIONE, LD.ALTRO_LUOGO, TIPO_ATTO.RV_MEANING DESCR_TIPO_ATTO, GP.DATA_RICHIESTA, GP.DATA_ARRIVO_CANCELLERIA, MITTENTE_ATTO.RV_MEANING DESCR_TIPO_MITTENTE, DESCR_COM_MIT.DESCRIZIONE DESCR_SEDE_MITTENTE, GP.DATA_DEFINIZIONE, GP.TIPO_DEFINIZIONE, GP.DESCR_DEFINIZIONE, M.COGNOME COGNOME_MAG, M.NOME NOME_MAG, NVL(UD.DATA_UDIENZA, GP.DATA_CAMERA_CONSIGLIO) DATA_UDIENZA, UD.ID_UDIENZA ID_UD, DECODE(UP.FLAG_RINVIATA, 'P', 'PREFISSATA') FLAG_RINVIATA, STATO_FASCICOLO.RV_MEANING DESCR_STATO_FASCICOLO, TIPO_REGISTRO.RV_MEANING DESCR_TIPO_REGISTRO, GP.ANNO_S1, GP.PROGR_S1, FASC.FAS_SIU_ID_FASCICOLO_SIUS, FASC.ID_FASCICOLO_SIUS_ORIGINE FROM SOGGETTO SOGG, GENERALE_PROCEDIMENTO GP LEFT OUT ER JOIN UDIENZA_PROCEDIMENTO UP ON (UP.GEN_PRID_GENERALE_PROCEDIMENTO = GP.ID_GENERALE_PROCEDIMENTO) LEFT OUTER JOIN UDIENZA UD ON (UD.ID_UDIENZA = GP.UDI_ID_UDIENZA), TENORE TEN, CG_REF_CODES DESCR_OGGETTO_PROCEDIMENTO, CG_REF_CODES POS_GIURIDICA, CG_REF_CODES NAZIONE, UFFICIO UFF, CG_REF_CODES STATO_FASCICOLO, COMUNE DESCR_COM_UFF, COMUNE DESCR_COM_NASCITA, CG_REF_CODES TIPO_ATTO, CG_REF_CODES MITTENTE_ATTO, CG_REF_CODES TIPO_REGISTRO, COMUNE DESCR_COM_MIT, MAGISTRATO_RELATORE MAG, MAGISTRATO M, AVVOCATO AVV, AVVOCATO_FASCICOLO_SIUS AVV_FAS, FASCICOLO_SIUS FASC LEFT OUTER JOIN V_SOGSIUS_ETA VSE ON (FASC.ID_FASCICOLO_SIUS = VSE.ID_FASCICOLO_SIUS) LEFT OUTER JOIN LUOGO_DETENZIONE LD ON (FASC.ID_FASCICOLO_SIUS = LD.FAS_SIU_ID_FASCICOLO_SIUS) LEFT OUTER JOIN ISTITUTO_DETENZIONE ID ON (LD.IST_DET_ID_ISTITUTO_DETENZIONE = ID.ID_ISTITUTO_DETENZIONE) LEFT OUTER JOIN CG_REF_CODES ISD ON (ISD.RV_LOW_VALUE = ID.COD_TIPO_ISTITUTO AND ISD.RV_DOMAIN = 'TIPO_ISTITUTO') WHERE FASC.S OG_ID_SOGGETTO = SOGG.ID_SOGGETTO AND FASC.ID_FASCICOLO_SIUS = GP.FAS_SIU_ID_FASCICOLO_SIUS AND DESCR_OGGETTO_PROCEDIMENTO.RV_DOMAIN = 'OGGETTO_PROCEDIMENTO' AND GP.COD_OGGETTO_PROCEDIMENTO = DESCR_OGGETTO_PROCEDIMENTO.RV_LOW_VALUE AND POS_GIURIDICA.RV_DOMAIN = 'POSIZIONE_GIURIDICA' AND (NVL(GP.COD_POSIZIONE_GIURIDICA, '-') = POS_GIURIDICA.RV_LOW_VALUE) AND UFF.COD_UFFICIO = FASC.CHIAVE_UFFICIO AND UFF.COD_COMUNE = DESCR_COM_UFF.COD_COMUNE AND SOGG.COD_COMUNE_NASCITA = DESCR_COM_NASCITA.COD_COMUNE AND FASC.ID_FASCICOLO_SIUS = VSE.ID_FASCICOLO_SIUS AND CHIAVE_PROGR = :B4 AND CHIAVE_ANNO = :B3 AND UFF.COD_UFFICIO IN ( CASE WHEN :B2 IS NULL THEN ( SELECT U.COD_UFFICIO FROM UFFICIO U, COMUNE C WHERE U.COD_TIPO_UFFICIO = :B6 AND U.COD_COMUNE = C.COD_COMUNE AND U.COD_DISTRETTO = :B5 ) ELSE (:B2 ) END ) AND ((NVL(VSE.ETA_ORA, 18) >= 18) OR FASC.COD_UFFICIO_INSERIMENTO IN ( CASE WHEN :B2 IS NULL THEN ( SELECT U.COD_UFFICIO FROM UFFICIO U, COMUNE C WHERE U.COD_TIPO_UFFICIO = :B6 AND U.CO D_COMUNE = C.COD_COMUNE AND U.COD_DISTRETTO = :B5 ) ELSE (:B2 ) END ) ) AND NAZIONE.RV_DOMAIN = 'NAZIONE' AND NAZIONE.RV_LOW_VALUE = SOGG.COD_STATO_NASCITA AND NVL(LD.DATA_INSERIMENTO, TO_DATE('01/01/1900', 'dd/mm/yyyy')) = NVL((SELECT MAX(DATA_INSERIMENTO) FROM LUOGO_DETENZIONE WHERE FAS_SIU_ID_FASCICOLO_SIUS = FASC.ID_FASCICOLO_SIUS), TO_DATE('01/01/1900', 'dd/mm/yyyy')) AND (TIPO_ATTO.RV_DOMAIN = 'TIPO_ATTO' AND NVL(GP.COD_TIPO_ATTO, '-') = TIPO_ATTO.RV_LOW_VALUE) AND (MITTENTE_ATTO.RV_DOMAIN = 'MITTENTE_ATTO' AND NVL(GP.COD_TIPO_MITTENTE_ATTO, '-') = MITTENTE_ATTO.RV_LOW_VALUE) AND (GP.COD_SEDE_MITTENTE = DESCR_COM_MIT.COD_COMUNE) AND (TEN.GEN_PRID_GENERALE_PROCEDIMENTO = GP.ID_GENERALE_PROCEDIMENTO) AND MAG.FAS_SIU_ID_FASCICOLO_SIUS = FASC.ID_FASCICOLO_SIUS AND MAG.DATA_FINE IS NULL AND M.COD_MAGISTRATO = MAG.MAG_COD_MAGISTRATO AND M.DATA_FINE_VALIDITA IS NULL AND AVV.ID_AVVOCATO = AVV_FAS.AVV_ID_AVVOCATO AND FASC.ID_FASCICOLO_SIUS = AVV_FAS.FAS_SIU_ID_FASCICOLO_SIUS AND AVV _FAS.DATA_FINE_VALIDITA IS NULL AND AVV.COD_FISCALE = UPPER(:B1 ) AND (STATO_FASCICOLO.RV_DOMAIN = 'STATO_FASCICOLO' AND NVL(STATO_FASCICOLO.RV_LOW_VALUE, '-') = FASC.COD_STATO_FASCICOLO) AND (TIPO_REGISTRO.RV_DOMAIN = 'TIPO_REGISTRO' AND NVL(GP.COD_TIPO_REGISTRO, '-') = TIPO_REGISTRO.RV_LOW_VALUE) |
| f92dm8jbg1spx | SELECT DISTINCT FSIEP.ANNO_FASCICOLO_UNIONE, FSIEP.CHIAVE_ANNO, FSIEP.CHIAVE_PROGR, FSIEP.CHIAVE_UFFICIO, DESCR_TIPO_UFF.RV_MEANING DESCR_TIPO_UFFICIO, DESCR_COM_UFF.DESCRIZIONE DESCR_COMUNE_UFFICIO, DESCR_TIPO_UFF.RV_LOW_VALUE COD_TIPO_UFFICIO, FSIEP.COD_MOTIVO_ARCHIVIAZIONE, MOTIVO_ARCHIVIAZIONE.RV_MEANING DESCR_MOTIVO_ARCHIVIAZIONE, FSIEP.COD_OPERATORE_AGGIORNAMENTO, FSIEP.COD_OPERATORE_INSERIMENTO, FSIEP.COD_STATO_FASCICOLO, STATO_FASCICOLO.RV_MEANING DESCR_STATO_FASCICOLO, FSIEP.COD_TIPO_POS_LIBERO, TIPO_POS_LIBERO.RV_MEANING DESCR_TIPO_POS_LIBERO, FSIEP.COD_UFFICIO_AGGIORNAMENTO, FSIEP.COD_UFFICIO_INSERIMENTO, FSIEP.DATA_AGGIORNAMENTO, FSIEP.DATA_ARCHIVIAZIONE, FSIEP.DATA_INSERIMENTO, FSIEP.DATA_ISCRIZIONE, FSIEP.DATA_UNIONE, FSIEP.FAS_SIE_ID_FASCICOLO_SIEP, FSIEP.FLAG_VALIDATO, FSIEP.ID_FASCICOLO_SIEP, FSIEP.LETTERA_FASCICOLO, FSIEP.NOTE NOTE_FASCICOLO, FSIEP.NUM_FASCICOLO_UNIONE, FSIEP.SEN_ID_SENTENZA, FSIEP.SOG_ID_SOGGETTO, FSIEP.FLAG_ALTRA_CAUS A, FSIEP.DATA_IRREVOCABILITA, FSIEP.FLAG_CUMULANTE, FSIEP.FLAG_CUMULATO, FSIEP.COD_UFFICIO_UNIONE, DESCR_TIPO_UFFUNIONE.RV_MEANING DESCR_TIPO_UFFICIO_UNIONE, DESCR_COM_UFFUNIONE.DESCRIZIONE DESCR_COMUNE_UFFICIO_UNIONE, FSIEP.KEY_PROVV_NSC , FSIEP.DATA_ARRIVO_ATTO , FSIEP.CHIAVE_PROGR_ORIG , UFFINSERIMENTO.COD_TIPO_UFFICIO COD_TIPO_UFFICIO_INS, DESCR_TIPO_UFFINSERIMENTO.RV_MEANING DESCR_TIPO_UFFICIO_INS, DESCR_COM_UFFINSERIMENTO.DESCRIZIONE DESCR_COMUNE_UFFICIO_INS , UFFINSERIMENTO.FLAG_ACCORP FLAG_UFFICIO_ACCORPATO , FSIEP.VISIBILITA_EX_MINORENNE FROM FASCICOLO_SIEP FSIEP, CG_REF_CODES MOTIVO_ARCHIVIAZIONE, CG_REF_CODES STATO_FASCICOLO, CG_REF_CODES TIPO_POS_LIBERO, FASCICOLO_SIUS FASC, GENERALE_PROCEDIMENTO GP, FASCICOLO_SIUS FASC2, GENERALE_PROCEDIMENTO GP2, UFFICIO UFF, CG_REF_CODES DESCR_TIPO_UFF, COMUNE DESCR_COM_UFF, UFFICIO UFFUNIONE, CG_REF_CODES DESCR_TIPO_UFFUNIONE, COMUNE DESCR_COM_UFFUNIONE , UFFICIO UFFINSERIMENTO , CG_REF_CODES DESCR_TIPO_ UFFINSERIMENTO, COMUNE DESCR_COM_UFFINSERIMENTO WHERE FASC.ID_FASCICOLO_SIUS = '592636232019' AND FSIEP.COD_UFFICIO_INSERIMENTO = UFFINSERIMENTO.COD_UFFICIO AND UFFINSERIMENTO.COD_TIPO_UFFICIO = DESCR_TIPO_UFFINSERIMENTO.RV_LOW_VALUE AND DESCR_TIPO_UFFINSERIMENTO.RV_DOMAIN = 'TIPO_UFFICIO' AND UFFINSERIMENTO.COD_COMUNE = DESCR_COM_UFFINSERIMENTO.COD_COMUNE AND (FASC2.FAS_SIE_ID_FASCICOLO_SIEP <> FASC.FAS_SIE_ID_FASCICOLO_SIEP AND FASC2.FAS_SIE_ID_FASCICOLO_SIEP = FSIEP.ID_FASCICOLO_SIEP) AND FASC.CHIAVE_UFFICIO = FASC2.CHIAVE_UFFICIO AND FASC.ID_FASCICOLO_SIUS = GP.FAS_SIU_ID_FASCICOLO_SIUS AND FASC2.ID_FASCICOLO_SIUS = GP2.FAS_SIU_ID_FASCICOLO_SIUS AND GP.ANNO_S1 = GP2.ANNO_S1 AND GP.PROGR_S1 = GP2.PROGR_S1 AND GP.COD_TIPO_REGISTRO = GP2.COD_TIPO_REGISTRO AND (MOTIVO_ARCHIVIAZIONE.RV_DOMAIN = 'MOTIVO_ARCHIVIAZIONE' AND MOTIVO_ARCHIVIAZIONE.RV_LOW_VALUE = FSIEP.COD_MOTIVO_ARCHIVIAZIONE) AND (STATO_FASCICOLO.RV_DOMAIN = 'STATO_FASCICOLO' AND STATO_FASCICOLO.RV_LOW_VALUE = FS IEP.COD_STATO_FASCICOLO) AND (DESCR_TIPO_UFF.RV_DOMAIN = 'TIPO_UFFICIO' AND UFF.COD_TIPO_UFFICIO = DESCR_TIPO_UFF.RV_LOW_VALUE) AND FSIEP.CHIAVE_UFFICIO = UFF.COD_UFFICIO AND UFF.COD_COMUNE = DESCR_COM_UFF.COD_COMUNE AND (DESCR_TIPO_UFFUNIONE.RV_DOMAIN = 'TIPO_UFFICIO' AND UFFUNIONE.COD_TIPO_UFFICIO = DESCR_TIPO_UFFUNIONE.RV_LOW_VALUE) AND (FSIEP.COD_UFFICIO_UNIONE = UFFUNIONE.COD_UFFICIO) AND (UFFUNIONE.COD_COMUNE = DESCR_COM_UFFUNIONE.COD_COMUNE) AND TIPO_POS_LIBERO.RV_DOMAIN = 'TIPO_POS_LIBERO' AND TIPO_POS_LIBERO.RV_LOW_VALUE = FSIEP.COD_TIPO_POS_LIBERO |
| gy7846jd1jxtk | SELECT DISTINCT FSIEP.ANNO_FASCICOLO_UNIONE, FSIEP.CHIAVE_ANNO, FSIEP.CHIAVE_PROGR, FSIEP.CHIAVE_UFFICIO, DESCR_TIPO_UFF.RV_MEANING DESCR_TIPO_UFFICIO, DESCR_COM_UFF.DESCRIZIONE DESCR_COMUNE_UFFICIO, DESCR_TIPO_UFF.RV_LOW_VALUE COD_TIPO_UFFICIO, FSIEP.COD_MOTIVO_ARCHIVIAZIONE, MOTIVO_ARCHIVIAZIONE.RV_MEANING DESCR_MOTIVO_ARCHIVIAZIONE, FSIEP.COD_OPERATORE_AGGIORNAMENTO, FSIEP.COD_OPERATORE_INSERIMENTO, FSIEP.COD_STATO_FASCICOLO, STATO_FASCICOLO.RV_MEANING DESCR_STATO_FASCICOLO, FSIEP.COD_TIPO_POS_LIBERO, TIPO_POS_LIBERO.RV_MEANING DESCR_TIPO_POS_LIBERO, FSIEP.COD_UFFICIO_AGGIORNAMENTO, FSIEP.COD_UFFICIO_INSERIMENTO, FSIEP.DATA_AGGIORNAMENTO, FSIEP.DATA_ARCHIVIAZIONE, FSIEP.DATA_INSERIMENTO, FSIEP.DATA_ISCRIZIONE, FSIEP.DATA_UNIONE, FSIEP.FAS_SIE_ID_FASCICOLO_SIEP, FSIEP.FLAG_VALIDATO, FSIEP.ID_FASCICOLO_SIEP, FSIEP.LETTERA_FASCICOLO, FSIEP.NOTE NOTE_FASCICOLO, FSIEP.NUM_FASCICOLO_UNIONE, FSIEP.SEN_ID_SENTENZA, FSIEP.SOG_ID_SOGGETTO, FSIEP.FLAG_ALTRA_CAUS A, FSIEP.DATA_IRREVOCABILITA, FSIEP.FLAG_CUMULANTE, FSIEP.FLAG_CUMULATO, FSIEP.COD_UFFICIO_UNIONE, DESCR_TIPO_UFFUNIONE.RV_MEANING DESCR_TIPO_UFFICIO_UNIONE, DESCR_COM_UFFUNIONE.DESCRIZIONE DESCR_COMUNE_UFFICIO_UNIONE, FSIEP.KEY_PROVV_NSC , FSIEP.DATA_ARRIVO_ATTO , FSIEP.CHIAVE_PROGR_ORIG , UFFINSERIMENTO.COD_TIPO_UFFICIO COD_TIPO_UFFICIO_INS, DESCR_TIPO_UFFINSERIMENTO.RV_MEANING DESCR_TIPO_UFFICIO_INS, DESCR_COM_UFFINSERIMENTO.DESCRIZIONE DESCR_COMUNE_UFFICIO_INS , UFFINSERIMENTO.FLAG_ACCORP FLAG_UFFICIO_ACCORPATO , FSIEP.VISIBILITA_EX_MINORENNE FROM FASCICOLO_SIEP FSIEP, CG_REF_CODES MOTIVO_ARCHIVIAZIONE, CG_REF_CODES STATO_FASCICOLO, CG_REF_CODES TIPO_POS_LIBERO, FASCICOLO_SIUS FASC, GENERALE_PROCEDIMENTO GP, FASCICOLO_SIUS FASC2, GENERALE_PROCEDIMENTO GP2, UFFICIO UFF, CG_REF_CODES DESCR_TIPO_UFF, COMUNE DESCR_COM_UFF, UFFICIO UFFUNIONE, CG_REF_CODES DESCR_TIPO_UFFUNIONE, COMUNE DESCR_COM_UFFUNIONE , UFFICIO UFFINSERIMENTO , CG_REF_CODES DESCR_TIPO_ UFFINSERIMENTO, COMUNE DESCR_COM_UFFINSERIMENTO WHERE FASC.ID_FASCICOLO_SIUS = '582513232019' AND FSIEP.COD_UFFICIO_INSERIMENTO = UFFINSERIMENTO.COD_UFFICIO AND UFFINSERIMENTO.COD_TIPO_UFFICIO = DESCR_TIPO_UFFINSERIMENTO.RV_LOW_VALUE AND DESCR_TIPO_UFFINSERIMENTO.RV_DOMAIN = 'TIPO_UFFICIO' AND UFFINSERIMENTO.COD_COMUNE = DESCR_COM_UFFINSERIMENTO.COD_COMUNE AND (FASC2.FAS_SIE_ID_FASCICOLO_SIEP <> FASC.FAS_SIE_ID_FASCICOLO_SIEP AND FASC2.FAS_SIE_ID_FASCICOLO_SIEP = FSIEP.ID_FASCICOLO_SIEP) AND FASC.CHIAVE_UFFICIO = FASC2.CHIAVE_UFFICIO AND FASC.ID_FASCICOLO_SIUS = GP.FAS_SIU_ID_FASCICOLO_SIUS AND FASC2.ID_FASCICOLO_SIUS = GP2.FAS_SIU_ID_FASCICOLO_SIUS AND GP.ANNO_S1 = GP2.ANNO_S1 AND GP.PROGR_S1 = GP2.PROGR_S1 AND GP.COD_TIPO_REGISTRO = GP2.COD_TIPO_REGISTRO AND (MOTIVO_ARCHIVIAZIONE.RV_DOMAIN = 'MOTIVO_ARCHIVIAZIONE' AND MOTIVO_ARCHIVIAZIONE.RV_LOW_VALUE = FSIEP.COD_MOTIVO_ARCHIVIAZIONE) AND (STATO_FASCICOLO.RV_DOMAIN = 'STATO_FASCICOLO' AND STATO_FASCICOLO.RV_LOW_VALUE = FS IEP.COD_STATO_FASCICOLO) AND (DESCR_TIPO_UFF.RV_DOMAIN = 'TIPO_UFFICIO' AND UFF.COD_TIPO_UFFICIO = DESCR_TIPO_UFF.RV_LOW_VALUE) AND FSIEP.CHIAVE_UFFICIO = UFF.COD_UFFICIO AND UFF.COD_COMUNE = DESCR_COM_UFF.COD_COMUNE AND (DESCR_TIPO_UFFUNIONE.RV_DOMAIN = 'TIPO_UFFICIO' AND UFFUNIONE.COD_TIPO_UFFICIO = DESCR_TIPO_UFFUNIONE.RV_LOW_VALUE) AND (FSIEP.COD_UFFICIO_UNIONE = UFFUNIONE.COD_UFFICIO) AND (UFFUNIONE.COD_COMUNE = DESCR_COM_UFFUNIONE.COD_COMUNE) AND TIPO_POS_LIBERO.RV_DOMAIN = 'TIPO_POS_LIBERO' AND TIPO_POS_LIBERO.RV_LOW_VALUE = FSIEP.COD_TIPO_POS_LIBERO |
| 45s6ah4bhak7d | SELECT COUNT(*) NUM FROM ( SELECT FASC.ANNO_FASCICOLO_UNIONE, FASC.CHIAVE_ANNO, FASC.CHIAVE_PROGR, FASC.CHIAVE_UFFICIO, DESCR_TIPO_UFF.RV_MEANING DESCR_TIPO_UFFICIO, DESCR_COM_UFF.DESCRIZIONE DESCR_COMUNE_UFFICIO, DESCR_TIPO_UFF.RV_LOW_VALUE COD_TIPO_UFFICIO, FASC.COD_MOTIVO_ARCHIVIAZIONE, MOTIVO_ARCHIVIAZIONE.RV_MEANING DESCR_MOTIVO_ARCHIVIAZIONE, FASC.COD_OPERATORE_AGGIORNAMENTO, FASC.COD_OPERATORE_INSERIMENTO, FASC.COD_STATO_FASCICOLO, STATO_FASCICOLO.RV_MEANING DESCR_STATO_FASCICOLO, FASC.COD_TIPO_POS_LIBERO, TIPO_POS_LIBERO.RV_MEANING DESCR_TIPO_POS_LIBERO, FASC.COD_UFFICIO_AGGIORNAMENTO, FASC.COD_UFFICIO_INSERIMENTO, FASC.DATA_AGGIORNAMENTO, FASC.DATA_ARCHIVIAZIONE, FASC.DATA_INSERIMENTO, FASC.DATA_ISCRIZIONE, FASC.DATA_UNIONE, FASC.FAS_SIE_ID_FASCICOLO_SIEP, FASC.FLAG_VALIDATO, FASC.ID_FASCICOLO_SIEP, FASC.LETTERA_FASCICOLO, FASC.NOTE NOTE_FASCICOLO, FASC.NUM_FASCICOLO_UNIONE, FASC.SEN_ID_SENTENZA, FASC.SOG_ID_SOGGETTO, FASC.FLAG_ALTRA_CAUSA, FAS C.DATA_IRREVOCABILITA, FASC.FLAG_CUMULANTE, FASC.FLAG_CUMULATO, FASC.COD_UFFICIO_UNIONE, DESCR_TIPO_UFFUNIONE.RV_MEANING DESCR_TIPO_UFFICIO_UNIONE, DESCR_COM_UFFUNIONE.DESCRIZIONE DESCR_COMUNE_UFFICIO_UNIONE, FASC.KEY_PROVV_NSC , FASC.DATA_ARRIVO_ATTO , FASC.CHIAVE_PROGR_ORIG , UFFINSERIMENTO.COD_TIPO_UFFICIO COD_TIPO_UFFICIO_INS, DESCR_TIPO_UFFINSERIMENTO.RV_MEANING DESCR_TIPO_UFFICIO_INS, DESCR_COM_UFFINSERIMENTO.DESCRIZIONE DESCR_COMUNE_UFFICIO_INS , UFFINSERIMENTO.FLAG_ACCORP FLAG_UFFICIO_ACCORPATO , FASC.VISIBILITA_EX_MINORENNE FROM FASCICOLO_SIEP FASC LEFT OUTER JOIN UFFICIO UFF ON (FASC.CHIAVE_UFFICIO = UFF.COD_UFFICIO ) LEFT OUTER JOIN CG_REF_CODES DESCR_TIPO_UFF ON (UFF.COD_TIPO_UFFICIO = DESCR_TIPO_UFF.RV_LOW_VALUE AND DESCR_TIPO_UFF.RV_DOMAIN = 'TIPO_UFFICIO') LEFT OUTER JOIN COMUNE DESCR_COM_UFF ON (UFF.COD_COMUNE = DESCR_COM_UFF.COD_COMUNE) LEFT OUTER JOIN UFFICIO UFFUNIONE ON (FASC.COD_UFFICIO_UNIONE = UFFUNIONE.COD_UFFICIO ) LEFT OUTER JOIN CG_REF_CODES D ESCR_TIPO_UFFUNIONE ON (UFFUNIONE.COD_TIPO_UFFICIO = DESCR_TIPO_UFFUNIONE.RV_LOW_VALUE AND DESCR_TIPO_UFFUNIONE.RV_DOMAIN = 'TIPO_UFFICIO') LEFT OUTER JOIN COMUNE DESCR_COM_UFFUNIONE ON (UFFUNIONE.COD_COMUNE = DESCR_COM_UFFUNIONE.COD_COMUNE) LEFT OUTER JOIN CG_REF_CODES STATO_FASCICOLO ON (FASC.COD_STATO_FASCICOLO = STATO_FASCICOLO.RV_LOW_VALUE AND STATO_FASCICOLO.RV_DOMAIN = 'STATO_FASCICOLO') LEFT OUTER JOIN CG_REF_CODES MOTIVO_ARCHIVIAZIONE ON (FASC.COD_MOTIVO_ARCHIVIAZIONE = MOTIVO_ARCHIVIAZIONE.RV_LOW_VALUE AND MOTIVO_ARCHIVIAZIONE.RV_DOMAIN = 'MOTIVO_ARCHIVIAZIONE') LEFT OUTER JOIN CG_REF_CODES TIPO_POS_LIBERO ON (FASC.COD_TIPO_POS_LIBERO = TIPO_POS_LIBERO.RV_LOW_VALUE AND TIPO_POS_LIBERO.RV_DOMAIN = 'TIPO_POS_LIBERO') LEFT OUTER JOIN UFFICIO UFFINSERIMENTO ON (FASC.Cod_Ufficio_Inserimento = UFFINSERIMENTO.COD_UFFICIO ) LEFT OUTER JOIN CG_REF_CODES DESCR_TIPO_UFFINSERIMENTO ON (UFFINSERIMENTO.COD_TIPO_UFFICIO = DESCR_TIPO_UFFINSERIMENTO.RV_LOW_VALUE AND DESCR_TIPO_UFFINSERIMENTO. RV_DOMAIN = 'TIPO_UFFICIO') LEFT OUTER JOIN COMUNE DESCR_COM_UFFINSERIMENTO ON (UFFINSERIMENTO.COD_COMUNE = DESCR_COM_UFFINSERIMENTO.COD_COMUNE) LEFT OUTER JOIN V_SOGGETTO_ETA vse ON (FASC.id_fascicolo_siep = vse.FAS_SIE_ID_FASCICOLO_SIEP) WHERE FASC.ID_FASCICOLO_SIEP is not NULL AND (CHIAVE_PROGR = 478) AND (CHIAVE_ANNO = 2013) AND (UFF.COD_UFFICIO = nvl('', UFF.COD_UFFICIO ) ) AND (UFF.COD_TIPO_UFFICIO = nvl('PM', UFF.COD_TIPO_UFFICIO ) ) and ( (nvl(vse.eta_ora, 18) >= 18 ) or (FASC.cod_ufficio_inserimento = '06304901302') ) AND FLAG_VALIDATO = 'S' ORDER BY 2, 3 ) |
| 4k0t94xwxyubm | SELECT * FROM (SELECT INNER.* , ROWNUM rn FROM ( SELECT FASC.ANNO_FASCICOLO_UNIONE, FASC.CHIAVE_ANNO, FASC.CHIAVE_PROGR, FASC.CHIAVE_UFFICIO, DESCR_TIPO_UFF.RV_MEANING DESCR_TIPO_UFFICIO, DESCR_COM_UFF.DESCRIZIONE DESCR_COMUNE_UFFICIO, DESCR_TIPO_UFF.RV_LOW_VALUE COD_TIPO_UFFICIO, FASC.COD_MOTIVO_ARCHIVIAZIONE, MOTIVO_ARCHIVIAZIONE.RV_MEANING DESCR_MOTIVO_ARCHIVIAZIONE, FASC.COD_OPERATORE_AGGIORNAMENTO, FASC.COD_OPERATORE_INSERIMENTO, FASC.COD_STATO_FASCICOLO, STATO_FASCICOLO.RV_MEANING DESCR_STATO_FASCICOLO, FASC.COD_TIPO_POS_LIBERO, TIPO_POS_LIBERO.RV_MEANING DESCR_TIPO_POS_LIBERO, FASC.COD_UFFICIO_AGGIORNAMENTO, FASC.COD_UFFICIO_INSERIMENTO, FASC.DATA_AGGIORNAMENTO, FASC.DATA_ARCHIVIAZIONE, FASC.DATA_INSERIMENTO, FASC.DATA_ISCRIZIONE, FASC.DATA_UNIONE, FASC.FAS_SIE_ID_FASCICOLO_SIEP, FASC.FLAG_VALIDATO, FASC.ID_FASCICOLO_SIEP, FASC.LETTERA_FASCICOLO, FASC.NOTE NOTE_FASCICOLO, FASC.NUM_FASCICOLO_UNIONE, FASC.SEN_ID_SENTENZA, FASC.SOG_ID_SOGGETTO, FASC .FLAG_ALTRA_CAUSA, FASC.DATA_IRREVOCABILITA, FASC.FLAG_CUMULANTE, FASC.FLAG_CUMULATO, FASC.COD_UFFICIO_UNIONE, DESCR_TIPO_UFFUNIONE.RV_MEANING DESCR_TIPO_UFFICIO_UNIONE, DESCR_COM_UFFUNIONE.DESCRIZIONE DESCR_COMUNE_UFFICIO_UNIONE, FASC.KEY_PROVV_NSC , FASC.DATA_ARRIVO_ATTO , FASC.CHIAVE_PROGR_ORIG , UFFINSERIMENTO.COD_TIPO_UFFICIO COD_TIPO_UFFICIO_INS, DESCR_TIPO_UFFINSERIMENTO.RV_MEANING DESCR_TIPO_UFFICIO_INS, DESCR_COM_UFFINSERIMENTO.DESCRIZIONE DESCR_COMUNE_UFFICIO_INS , UFFINSERIMENTO.FLAG_ACCORP FLAG_UFFICIO_ACCORPATO , FASC.VISIBILITA_EX_MINORENNE FROM FASCICOLO_SIEP FASC LEFT OUTER JOIN UFFICIO UFF ON (FASC.CHIAVE_UFFICIO = UFF.COD_UFFICIO ) LEFT OUTER JOIN CG_REF_CODES DESCR_TIPO_UFF ON (UFF.COD_TIPO_UFFICIO = DESCR_TIPO_UFF.RV_LOW_VALUE AND DESCR_TIPO_UFF.RV_DOMAIN = 'TIPO_UFFICIO') LEFT OUTER JOIN COMUNE DESCR_COM_UFF ON (UFF.COD_COMUNE = DESCR_COM_UFF.COD_COMUNE) LEFT OUTER JOIN UFFICIO UFFUNIONE ON (FASC.COD_UFFICIO_UNIONE = UFFUNIONE.COD_UFFICIO ) LEFT OU TER JOIN CG_REF_CODES DESCR_TIPO_UFFUNIONE ON (UFFUNIONE.COD_TIPO_UFFICIO = DESCR_TIPO_UFFUNIONE.RV_LOW_VALUE AND DESCR_TIPO_UFFUNIONE.RV_DOMAIN = 'TIPO_UFFICIO') LEFT OUTER JOIN COMUNE DESCR_COM_UFFUNIONE ON (UFFUNIONE.COD_COMUNE = DESCR_COM_UFFUNIONE.COD_COMUNE) LEFT OUTER JOIN CG_REF_CODES STATO_FASCICOLO ON (FASC.COD_STATO_FASCICOLO = STATO_FASCICOLO.RV_LOW_VALUE AND STATO_FASCICOLO.RV_DOMAIN = 'STATO_FASCICOLO') LEFT OUTER JOIN CG_REF_CODES MOTIVO_ARCHIVIAZIONE ON (FASC.COD_MOTIVO_ARCHIVIAZIONE = MOTIVO_ARCHIVIAZIONE.RV_LOW_VALUE AND MOTIVO_ARCHIVIAZIONE.RV_DOMAIN = 'MOTIVO_ARCHIVIAZIONE') LEFT OUTER JOIN CG_REF_CODES TIPO_POS_LIBERO ON (FASC.COD_TIPO_POS_LIBERO = TIPO_POS_LIBERO.RV_LOW_VALUE AND TIPO_POS_LIBERO.RV_DOMAIN = 'TIPO_POS_LIBERO') LEFT OUTER JOIN UFFICIO UFFINSERIMENTO ON (FASC.Cod_Ufficio_Inserimento = UFFINSERIMENTO.COD_UFFICIO ) LEFT OUTER JOIN CG_REF_CODES DESCR_TIPO_UFFINSERIMENTO ON (UFFINSERIMENTO.COD_TIPO_UFFICIO = DESCR_TIPO_UFFINSERIMENTO.RV_LOW_VALUE AND DES CR_TIPO_UFFINSERIMENTO.RV_DOMAIN = 'TIPO_UFFICIO') LEFT OUTER JOIN COMUNE DESCR_COM_UFFINSERIMENTO ON (UFFINSERIMENTO.COD_COMUNE = DESCR_COM_UFFINSERIMENTO.COD_COMUNE) LEFT OUTER JOIN V_SOGGETTO_ETA vse ON (FASC.id_fascicolo_siep = vse.FAS_SIE_ID_FASCICOLO_SIEP) WHERE FASC.ID_FASCICOLO_SIEP is not NULL AND (CHIAVE_PROGR = 2260) AND (CHIAVE_ANNO = 2011) AND (UFF.COD_UFFICIO = nvl('', UFF.COD_UFFICIO ) ) AND (UFF.COD_TIPO_UFFICIO = nvl('PM', UFF.COD_TIPO_UFFICIO ) ) and ( (nvl(vse.eta_ora, 18) >= 18 ) or (FASC.cod_ufficio_inserimento = '06304901302') ) AND FLAG_VALIDATO = 'S' ORDER BY 2, 3 ) INNER ) WHERE rn between 1 AND 20 |
| 4qx8u6vdb731t | SELECT * FROM (SELECT INNER.* , ROWNUM rn FROM ( SELECT FASC.ANNO_FASCICOLO_UNIONE, FASC.CHIAVE_ANNO, FASC.CHIAVE_PROGR, FASC.CHIAVE_UFFICIO, DESCR_TIPO_UFF.RV_MEANING DESCR_TIPO_UFFICIO, DESCR_COM_UFF.DESCRIZIONE DESCR_COMUNE_UFFICIO, DESCR_TIPO_UFF.RV_LOW_VALUE COD_TIPO_UFFICIO, FASC.COD_MOTIVO_ARCHIVIAZIONE, MOTIVO_ARCHIVIAZIONE.RV_MEANING DESCR_MOTIVO_ARCHIVIAZIONE, FASC.COD_OPERATORE_AGGIORNAMENTO, FASC.COD_OPERATORE_INSERIMENTO, FASC.COD_STATO_FASCICOLO, STATO_FASCICOLO.RV_MEANING DESCR_STATO_FASCICOLO, FASC.COD_TIPO_POS_LIBERO, TIPO_POS_LIBERO.RV_MEANING DESCR_TIPO_POS_LIBERO, FASC.COD_UFFICIO_AGGIORNAMENTO, FASC.COD_UFFICIO_INSERIMENTO, FASC.DATA_AGGIORNAMENTO, FASC.DATA_ARCHIVIAZIONE, FASC.DATA_INSERIMENTO, FASC.DATA_ISCRIZIONE, FASC.DATA_UNIONE, FASC.FAS_SIE_ID_FASCICOLO_SIEP, FASC.FLAG_VALIDATO, FASC.ID_FASCICOLO_SIEP, FASC.LETTERA_FASCICOLO, FASC.NOTE NOTE_FASCICOLO, FASC.NUM_FASCICOLO_UNIONE, FASC.SEN_ID_SENTENZA, FASC.SOG_ID_SOGGETTO, FASC .FLAG_ALTRA_CAUSA, FASC.DATA_IRREVOCABILITA, FASC.FLAG_CUMULANTE, FASC.FLAG_CUMULATO, FASC.COD_UFFICIO_UNIONE, DESCR_TIPO_UFFUNIONE.RV_MEANING DESCR_TIPO_UFFICIO_UNIONE, DESCR_COM_UFFUNIONE.DESCRIZIONE DESCR_COMUNE_UFFICIO_UNIONE, FASC.KEY_PROVV_NSC , FASC.DATA_ARRIVO_ATTO , FASC.CHIAVE_PROGR_ORIG , UFFINSERIMENTO.COD_TIPO_UFFICIO COD_TIPO_UFFICIO_INS, DESCR_TIPO_UFFINSERIMENTO.RV_MEANING DESCR_TIPO_UFFICIO_INS, DESCR_COM_UFFINSERIMENTO.DESCRIZIONE DESCR_COMUNE_UFFICIO_INS , UFFINSERIMENTO.FLAG_ACCORP FLAG_UFFICIO_ACCORPATO , FASC.VISIBILITA_EX_MINORENNE FROM FASCICOLO_SIEP FASC LEFT OUTER JOIN UFFICIO UFF ON (FASC.CHIAVE_UFFICIO = UFF.COD_UFFICIO ) LEFT OUTER JOIN CG_REF_CODES DESCR_TIPO_UFF ON (UFF.COD_TIPO_UFFICIO = DESCR_TIPO_UFF.RV_LOW_VALUE AND DESCR_TIPO_UFF.RV_DOMAIN = 'TIPO_UFFICIO') LEFT OUTER JOIN COMUNE DESCR_COM_UFF ON (UFF.COD_COMUNE = DESCR_COM_UFF.COD_COMUNE) LEFT OUTER JOIN UFFICIO UFFUNIONE ON (FASC.COD_UFFICIO_UNIONE = UFFUNIONE.COD_UFFICIO ) LEFT OU TER JOIN CG_REF_CODES DESCR_TIPO_UFFUNIONE ON (UFFUNIONE.COD_TIPO_UFFICIO = DESCR_TIPO_UFFUNIONE.RV_LOW_VALUE AND DESCR_TIPO_UFFUNIONE.RV_DOMAIN = 'TIPO_UFFICIO') LEFT OUTER JOIN COMUNE DESCR_COM_UFFUNIONE ON (UFFUNIONE.COD_COMUNE = DESCR_COM_UFFUNIONE.COD_COMUNE) LEFT OUTER JOIN CG_REF_CODES STATO_FASCICOLO ON (FASC.COD_STATO_FASCICOLO = STATO_FASCICOLO.RV_LOW_VALUE AND STATO_FASCICOLO.RV_DOMAIN = 'STATO_FASCICOLO') LEFT OUTER JOIN CG_REF_CODES MOTIVO_ARCHIVIAZIONE ON (FASC.COD_MOTIVO_ARCHIVIAZIONE = MOTIVO_ARCHIVIAZIONE.RV_LOW_VALUE AND MOTIVO_ARCHIVIAZIONE.RV_DOMAIN = 'MOTIVO_ARCHIVIAZIONE') LEFT OUTER JOIN CG_REF_CODES TIPO_POS_LIBERO ON (FASC.COD_TIPO_POS_LIBERO = TIPO_POS_LIBERO.RV_LOW_VALUE AND TIPO_POS_LIBERO.RV_DOMAIN = 'TIPO_POS_LIBERO') LEFT OUTER JOIN UFFICIO UFFINSERIMENTO ON (FASC.Cod_Ufficio_Inserimento = UFFINSERIMENTO.COD_UFFICIO ) LEFT OUTER JOIN CG_REF_CODES DESCR_TIPO_UFFINSERIMENTO ON (UFFINSERIMENTO.COD_TIPO_UFFICIO = DESCR_TIPO_UFFINSERIMENTO.RV_LOW_VALUE AND DES CR_TIPO_UFFINSERIMENTO.RV_DOMAIN = 'TIPO_UFFICIO') LEFT OUTER JOIN COMUNE DESCR_COM_UFFINSERIMENTO ON (UFFINSERIMENTO.COD_COMUNE = DESCR_COM_UFFINSERIMENTO.COD_COMUNE) LEFT OUTER JOIN V_SOGGETTO_ETA vse ON (FASC.id_fascicolo_siep = vse.FAS_SIE_ID_FASCICOLO_SIEP) WHERE FASC.ID_FASCICOLO_SIEP is not NULL AND (CHIAVE_PROGR = 1978) AND (CHIAVE_ANNO = 2017) AND (DESCR_COM_UFF.DESCRIZIONE = 'NAPOLI') AND (UFF.COD_UFFICIO = nvl('06304902102', UFF.COD_UFFICIO ) ) AND (UFF.COD_TIPO_UFFICIO = nvl('', UFF.COD_TIPO_UFFICIO ) ) and ( (nvl(vse.eta_ora, 18) >= 18 ) or (FASC.cod_ufficio_inserimento = '06304902203') ) AND FLAG_VALIDATO = 'S' ORDER BY 2, 3 ) INNER ) WHERE rn between 1 AND 20 |


## Il binding delle variabili
In ambiente transazionale garantire il riuso, soft parsing, delle istruzioni SQL di volta in volta inviate dall’applicazione, significa limitare il consumo di risorse del database e quindi scalare linearmente al meglio se aumenta il carico di lavoro. Purtroppo, l’applicazione SIES-Avvocatura usa molto poco il binding delle variabili nel codice java preposto all’invio di istruzioni SQL al database, determinando l’hard parsing di gran parte delle istruzioni SQL. Ciò implica un maggior consumo di CPU e tempi di attesa più lunghi per accedere alle risorse condivise del database (ad es. la SGA). In diversi report AWR viene espressamente indicato il mancato binding delle variabili come un contribuito importante nel consumo di risorse, per esempio dal primo lancio:

Finding 3: Hard Parse Due to Literal Usage
Impact is .68 active sessions, 12.32% of total activity.
--------------------------------------------------------
SQL statements were not shared due to the usage of literals. This resulted in
additional hard parses which were consuming significant database time.

## Risultati di dettaglio
Nella tabella seguente si elencano gli stress test condotti sul sistema SIES-Avvocatura per data di lancio del test, la tipologia e ora di inizio e fine.

| N° | Data Lancio | Tipologia Test | Ora Inizio | Ora Fine |
| --- | --- | --- | --- | --- |
| 1 | 30/09/2020 | 50 Distrettuali e 50 Avvocati | 14:20 | 15:32 |
| 2 | 30/09/2020 | 110 Distrettuali e 200 Avvocati | 16:32 | 17:26 |
| 3 | 01/10/2020 | 110 Distrettuali e 500 Avvocati | 12:37 | 13:37 |
| 4 | 05/10/2020 | 500 Avvocati | 09:48 | 10:06 |
| 5 | 05/10/2020 | 550 Distrettuali | 10:18 | 10:47 |
| 6 | 05/10/2020 | 1000 Avvocati | 10:58 | 11:34 |
| 7 | 05/10/2020 | 110 Distrettuali e 500 Avvocati senza “Ricerca soggetto” e senza “Stampa Procedimenti” | 13:47 | 16:13 |


In allegato al presente documento vengono forniti anche i file denominati “Risultati_JMeter.rar” e “AWR_Report_SIES_Avvocatura.zip” contenenti i risultati dei singoli casi di test, lato Application Server e Database Server.

## Test n°1: 50 utenti Distrettuali e 50 Avvocati per un intervallo di 1 ora
## Sistema Centrale
Tempo di risposta medio:


Utenti concorrenti:


Latenza:

Throughput:

Statistiche:
| Requests | Executions | Executions | Executions | Time |
| --- | --- | --- | --- | --- |
| Label | #Samples | KO | Error % | Average |
| Total | 24174 | 88 | 0.36% | 2160.19 |
| 1 /PST/SIUS/login | 3307 | 0 | 0.00% | 66.61 |
| 67 /PST/SIUS/j_spring_security_check;jsessionid= | 3307 | 9 | 0.27% | 81.13 |
| 114 /PST/SIUS/ricerca/procedimenti/exec | 3294 | 39 | 1.18% | 1026.97 |
| 119 /PST/SIUS/ricerca/procedimenti/dettaglio | 779 | 0 | 0.00% | 1709.27 |
| 120 /PST/SIUS/ricerca/procedimenti/exec | 778 | 0 | 0.00% | 680.37 |
| 121 /PST/SIUS/ricerca/procedimenti/dettaglio | 1436 | 1 | 0.07% | 1474.55 |
| 122 /PST/SIUS/ricerca/procedimenti/exec | 1436 | 0 | 0.00% | 689.32 |
| 123 /PST/SIUS/ricerca/procedimenti/stampa | 3273 | 39 | 1.19% | 11522.71 |
| 124 /PST/SIUS/ricerca/soggetti | 3257 | 0 | 0.00% | 1492.89 |
| 177 /PST/SIUS/j_spring_security_logout | 3257 | 0 | 0.00% | 212.76 |
| Accesso dati soggetto | 3267 | 0 | 0.00% | 1488.32 |
| Dettaglio decreto | 1444 | 1 | 0.07% | 1466.38 |
| Dettaglio ordinanza | 789 | 0 | 0.00% | 1708.21 |
| Landing login | 3307 | 0 | 0.00% | 66.61 |
| Login | 3307 | 9 | 0.27% | 81.13 |
| Logout | 3257 | 0 | 0.00% | 212.76 |
| Ricerca estremi procedimenti | 5521 | 39 | 0.71% | 887.89 |
| Stampa procedimento | 3275 | 39 | 1.19% | 11525.26 |


## Sistema Distrettuale
Statistiche:
| Requests | Executions | Executions | Executions | Time |
| --- | --- | --- | --- | --- |
| Label | #Samples | KO | Error % | Average |
| Total | 837 | 5 | 0.60% | 1178.02 |
| 1 / | 59 | 0 | 0.00% | 170.32 |
| 1 /jsp/Main.jsp | 5 | 0 | 0.00% | 1479.80 |
| 4 /jsp/Main.jsp | 1 | 0 | 0.00% | 5.00 |
| 4 /login.jsp | 1 | 0 | 0.00% | 7.00 |
| 5 /jsp/Main.jsp | 2 | 0 | 0.00% | 47.00 |
| 6 /jsp/Main.jsp | 1 | 0 | 0.00% | 18.00 |
| 9 /jsp/Main.jsp | 59 | 0 | 0.00% | 72.03 |
| 10 /frame.htm | 59 | 0 | 0.00% | 8.56 |
| 11 /jsp/files/logo.jsp | 59 | 0 | 0.00% | 10.69 |
| 11 /jsp/Main.jsp | 1 | 0 | 0.00% | 48.00 |
| 12 /frame.htm | 1 | 0 | 0.00% | 18.00 |
| 12 /jsp/files/up.jsp | 59 | 0 | 0.00% | 22.27 |
| 12 /jsp/Main.jsp | 1 | 0 | 0.00% | 9.00 |
| 13 /jsp/files/logo.jsp | 1 | 0 | 0.00% | 59.00 |
| 13 /jsp/files/menu.jsp | 59 | 0 | 0.00% | 23.51 |
| 13 /jsp/Main.jsp | 1 | 0 | 0.00% | 78.00 |
| 14 /jsp/files/content_frame.jsp | 59 | 0 | 0.00% | 13.17 |
| 14 /jsp/files/up.jsp | 1 | 0 | 0.00% | 3.00 |
| 15 /jsp/files/menu.jsp | 1 | 0 | 0.00% | 3.00 |
| 15 /jsp/Main.jsp | 1 | 1 | 100.00% | 13.00 |
| 16 /jsp/files/content_frame.jsp | 1 | 0 | 0.00% | 2.00 |
| 22 /html/blank.htm | 1 | 0 | 0.00% | 5.00 |
| 23 /html/blank.htm | 59 | 0 | 0.00% | 9.85 |
| 23 /jsp/Main.jsp | 1 | 0 | 0.00% | 184.00 |
| 24 /html/blankGray.htm | 59 | 0 | 0.00% | 6.39 |
| 25 /jsp/files/fastAccessMenu.jsp | 59 | 0 | 0.00% | 16.75 |
| 28 /jsp/files/fastAccessMenu.jsp | 1 | 0 | 0.00% | 2.00 |
| 29 /html/blankGray.htm | 1 | 0 | 0.00% | 10.00 |
| 29 /jsp/Main.jsp | 1 | 0 | 0.00% | 7.00 |
| 33 /jsp/Main.jsp | 1 | 0 | 0.00% | 13.00 |
| 35 /jsp/Main.jsp | 1 | 0 | 0.00% | 13553.00 |
| 38 /jsp/Main.jsp | 1 | 0 | 0.00% | 23.00 |
| 41 /jsp/Main.jsp | 1 | 0 | 0.00% | 13.00 |
| 42 /jsp/Main.jsp | 1 | 0 | 0.00% | 34638.00 |
| 43 /jsp/Main.jsp | 1 | 0 | 0.00% | 5.00 |
| 44 /jsp/Main.jsp | 51 | 0 | 0.00% | 4795.59 |
| 45 /jsp/Main.jsp | 2 | 0 | 0.00% | 1216.00 |
| 47 /jsp/Main.jsp | 1 | 0 | 0.00% | 4.00 |
| 49 /jsp/Main.jsp | 1 | 0 | 0.00% | 31.00 |
| 51 /jsp/files/Stampa.jsp | 1 | 0 | 0.00% | 10.00 |
| 51 /jsp/Main.jsp | 1 | 0 | 0.00% | 265.00 |
| 55 /jsp/Main.jsp | 51 | 0 | 0.00% | 12420.02 |
| 56 /jsp/Main.jsp | 2 | 0 | 0.00% | 1176.50 |
| 57 /jsp/Main.jsp | 1 | 0 | 0.00% | 196.00 |
| 60 /jsp/Main.jsp | 1 | 0 | 0.00% | 54.00 |
| 62 /jsp/Main.jsp | 1 | 0 | 0.00% | 271.00 |
| 64 /jsp/Main.jsp | 1 | 0 | 0.00% | 7.00 |
| 67 /jsp/Main.jsp | 1 | 0 | 0.00% | 6.00 |
| 68 /jsp/files/siap/sico/Calendario.jsp | 1 | 0 | 0.00% | 3.00 |
| 68 /jsp/Main.jsp | 1 | 0 | 0.00% | 5435.00 |
| 72 /jsp/Main.jsp | 1 | 0 | 0.00% | 9.00 |
| 74 /jsp/Main.jsp | 1 | 0 | 0.00% | 132.00 |
| 75 /html/blank.htm | 1 | 0 | 0.00% | 0.00 |
| 76 /jsp/Main.jsp | 1 | 0 | 0.00% | 9.00 |
| 79 /jsp/Main.jsp | 55 | 0 | 0.00% | 52.93 |
| 82 /jsp/Main.jsp | 1 | 0 | 0.00% | 299.00 |
| 86 /jsp/Main.jsp | 1 | 0 | 0.00% | 6.00 |
| 89 /jsp/Main.jsp | 1 | 0 | 0.00% | 5.00 |
| 91 /jsp/Main.jsp | 1 | 0 | 0.00% | 15651.00 |
| 92 /jsp/Main.jsp | 1 | 0 | 0.00% | 24.00 |
| 101 /jsp/Main.jsp | 1 | 0 | 0.00% | 9.00 |
| 104 /jsp/Main.jsp | 1 | 0 | 0.00% | 15.00 |
| 107 /jsp/Main.jsp | 1 | 1 | 100.00% | 21.00 |
| 119 /jsp/Main.jsp | 2 | 0 | 0.00% | 4.50 |
| 121 /jsp/Main.jsp | 2 | 0 | 0.00% | 9.00 |
| 125 /jsp/Main.jsp | 1 | 0 | 0.00% | 18.00 |
| 130 /jsp/Main.jsp | 1 | 0 | 0.00% | 40.00 |
| 133 /jsp/Main.jsp | 1 | 0 | 0.00% | 57.00 |
| 144 /jsp/Main.jsp | 1 | 0 | 0.00% | 11.00 |
| 147 /jsp/Main.jsp | 1 | 1 | 100.00% | 46.00 |
| 186 /jsp/Main.jsp | 1 | 0 | 0.00% | 17.00 |
| 191 /jsp/Main.jsp | 1 | 0 | 0.00% | 53.00 |
| 205 /jsp/Main.jsp | 1 | 1 | 100.00% | 63.00 |
| 227 /jsp/Main.jsp | 2 | 0 | 0.00% | 6.50 |
| 231 /jsp/Main.jsp | 2 | 0 | 0.00% | 7.50 |
| 233 /jsp/Main.jsp | 2 | 0 | 0.00% | 28.50 |
| 240 /jsp/Main.jsp | 1 | 0 | 0.00% | 198.00 |
| 441 /jsp/Main.jsp | 1 | 0 | 0.00% | 13.00 |
| 445 /jsp/Main.jsp | 1 | 0 | 0.00% | 8.00 |
| 449 /jsp/Main.jsp | 1 | 0 | 0.00% | 19.00 |
| 454 /jsp/Main.jsp | 1 | 0 | 0.00% | 12.00 |
| 460 /jsp/Main.jsp | 1 | 0 | 0.00% | 8.00 |
| 464 /jsp/files/siap/sico/cssa/FiltraCssaLista.jsp | 1 | 0 | 0.00% | 2.00 |
| 469 /jsp/Main.jsp | 1 | 0 | 0.00% | 14.00 |
| 472 /jsp/Main.jsp | 1 | 0 | 0.00% | 14.00 |
| 476 /jsp/Main.jsp | 1 | 0 | 0.00% | 13.00 |
| 480 /jsp/Main.jsp | 1 | 0 | 0.00% | 7.00 |
| 484 /jsp/Main.jsp | 1 | 0 | 0.00% | 12.00 |
| 492 /jsp/Main.jsp | 1 | 0 | 0.00% | 8.00 |
| 495 /jsp/Main.jsp | 1 | 0 | 0.00% | 21.00 |
| 500 /jsp/Main.jsp | 1 | 1 | 100.00% | 11.00 |
| cerca autorita competente | 1 | 0 | 0.00% | 48.00 |
| cerca istituto di detenzione | 1 | 0 | 0.00% | 27.00 |
| cerca sede uepe | 1 | 0 | 0.00% | 24.00 |
| cerca UDS | 1 | 0 | 0.00% | 27.00 |
| click calcola data fine pena | 1 | 0 | 0.00% | 184.00 |
| click calendario | 1 | 0 | 0.00% | 3.00 |
| click concessione | 1 | 0 | 0.00% | 57.00 |
| click decisioni di sorveglianza | 2 | 0 | 0.00% | 13.50 |
| click iscrizione manuale | 3 | 0 | 0.00% | 6.00 |
| click iscrizione procedimento | 1 | 0 | 0.00% | 271.00 |
| click istituto di detenzione | 1 | 0 | 0.00% | 20.00 |
| click liberazione anticipata | 1 | 0 | 0.00% | 17.00 |
| click lista oggetto | 1 | 0 | 0.00% | 11.00 |
| click magistrato | 1 | 0 | 0.00% | 36.00 |
| click oggetti | 1 | 0 | 0.00% | 24.00 |
| click ok popup aggiornamento | 1 | 0 | 0.00% | 54.00 |
| click ordine di esecuzione | 1 | 0 | 0.00% | 5441.00 |
| click ricerca procedimento per numero | 1 | 0 | 0.00% | 35.00 |
| click ricerca titolo per numero | 2 | 0 | 0.00% | 36.00 |
| click scegli TDS | 1 | 0 | 0.00% | 13.00 |
| click scelta oggetto | 1 | 0 | 0.00% | 9.00 |
| click sede | 1 | 0 | 0.00% | 14.00 |
| click sede TDS | 1 | 0 | 0.00% | 13.00 |
| click semiliberta | 1 | 0 | 0.00% | 18.00 |
| click stampa | 1 | 0 | 0.00% | 1395.00 |
| click su ordine di esecuzione | 1 | 0 | 0.00% | 23.00 |
| click su ordini di esecuzione-scarcerazione | 2 | 0 | 0.00% | 7.50 |
| click su ricerca | 50 | 0 | 0.00% | 12640.72 |
| click su sospensione esecuzione 656 cpp | 1 | 0 | 0.00% | 7.00 |
| click titolo esecutivo | 1 | 0 | 0.00% | 15.00 |
| conferma concessione semiliberta | 1 | 1 | 100.00% | 16.00 |
| conferma inserimento | 1 | 0 | 0.00% | 299.00 |
| conferma liberazione | 1 | 0 | 0.00% | 80.00 |
| conferma oggetto | 1 | 1 | 100.00% | 21.00 |
| conferma ordine di scarcerazione | 1 | 0 | 0.00% | 120.00 |
| conferma ordine esecuzione | 1 | 1 | 100.00% | 64.00 |
| dettaglio procedimento | 1 | 0 | 0.00% | 265.00 |
| filtra istituto di dentenzione | 1 | 0 | 0.00% | 23.00 |
| filtra istituto di detenzione | 1 | 0 | 0.00% | 12.00 |
| home page | 60 | 0 | 0.00% | 167.60 |
| iscrizione procedimento | 1 | 0 | 0.00% | 196.00 |
| login | 60 | 0 | 0.00% | 182.67 |
| logout | 54 | 0 | 0.00% | 53.57 |
| pagina ricerca per soggetto | 1 | 0 | 0.00% | 13553.00 |
| ricerca avanzata | 1 | 0 | 0.00% | 7358.00 |
| ricerca procedimento | 56 | 0 | 0.00% | 4413.27 |
| ricerca singolo procedimento | 2 | 0 | 0.00% | 1255.00 |
| ricerca soggetto | 1 | 0 | 0.00% | 34638.00 |
| salva iscrizione procedimento | 1 | 1 | 100.00% | 48.00 |
| scelta sede | 1 | 1 | 100.00% | 48.00 |
| sospensione/revoca | 1 | 0 | 0.00% | 15656.00 |
| sospensioni/interruzioni del PM | 1 | 0 | 0.00% | 6.00 |
| valida documento | 1 | 0 | 0.00% | 88.00 |



## Database
Visto l’elevato numero di accessi al database, è normale che la CPU sia al primo posto in quanto risorsa più richiesta dai tanti processi concorrenti durante il test. La seconda metrica per tempo di attesa è “direct path write temp” che indica il tempo aspettato per eseguire IO su aree temporanee usate dal database per la normale esecuzione delle query, tipicamente per eseguire o ordinamenti, clausola “order by”, “distinct” e “union” delle istruzioni SQL, o per eseguire il join di tipo hash tra le tabelle della clausola “from” delle istruzioni SQL.


Tabella 1: Tempi di attesa (Wait Times)
| Event | Waits | Total Wait Time (sec) | Wait Avg(ms) | % DB time | Wait Class |
| --- | --- | --- | --- | --- | --- |
| DB CPU |  | 27.8K |  | 74.2 |  |
| direct path write temp | 2,325,126 | 6017.8 | 2.59 | 16.1 | User I/O |
| direct path read | 338,272 | 2198.9 | 6.50 | 5.9 | User I/O |
| latch: cache buffers chains | 90,729 | 328.8 | 3.62 | .9 | Concurrency |
| log file sync | 943 | 199.4 | 211.50 | .5 | Commit |
| direct path read temp | 2,394,098 | 197.1 | 0.08 | .5 | User I/O |
| latch: row cache objects | 8,670 | 113.6 | 13.10 | .3 | Concurrency |
| db file sequential read | 86,570 | 92.4 | 1.07 | .2 | User I/O |
| latch: shared pool | 10,534 | 19 | 1.80 | .1 | Concurrency |
| read by other session | 56 | 17.2 | 306.83 | .0 | User I/O |

A seguire, le istruzioni SQL con i tempi di risposta più lunghi registrati durante il test. In prima posizione la procedura PL/SQL “AVVOCATURA_SIUS.CERCA_FASIUS_PER_ESTREMI” che è stata eseguita per 5513 volte spendendo complessivamente 683,09 secondi, in seconda posizione la query con l’identificativo alfanumerico “SQL_ID = 95jt2quqwc0vn”, che è stata eseguita per 5868 volte impiegando complessivamente 547,62 secondi.

Tabella 2: Istruzioni SQL con i tempi di risposta maggiori
| Elapsed Time (s) | Executions | Elapsed Time per Exec (s) | %Total | %CPU | %IO | SQL Id | SQL Module | SQL Text |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 683.09 | 5,513 | 0.12 | 1.83 | 85.71 | 10.64 | 6qk3tkcw4rzaq | JDBC Thin Client | BEGIN AVVOCATURA_SIUS.CERCA_FA... |
| 547.62 | 5,868 | 0.09 | 1.46 | 95.94 | 0.01 | 95jt2quqwc0vn | JDBC Thin Client | SELECT /*+ optimizer_features_... |
| 148.10 | 105 | 1.41 | 0.40 | 46.56 | 53.09 | dfffkcnqfystw | MMON_SLAVE | WITH MONITOR_DATA AS (SELECT I... |
| 116.48 | 109 | 1.07 | 0.31 | 51.67 | 48.22 | 0w26sk6t6gq98 | MMON_SLAVE | SELECT XMLTYPE(DBMS_REPORT.GET... |
| 78.11 | 93 | 0.84 | 0.21 | 65.03 | 34.87 | fhf8upax5cxsz | MMON_SLAVE | BEGIN sys.dbms_auto_report_int... |
| 65.35 | 115 | 0.57 | 0.17 | 4.87 | 0.70 | 4phvdvx32a3mf |  | begin prvt_ilm.stopjobs(-1, tr... |
| 41.78 | 5,514 | 0.01 | 0.11 | 18.03 | 81.55 | g3w1xqyu26u2q | JDBC Thin Client | SELECT /*+ optimizer_features_... |
| Elapsed Time (s) | Executions | Elapsed Time per Exec (s) | %Total | %CPU | %IO | SQL Id | SQL Module | SQL Text |
| 39.46 | 50 | 0.79 | 0.11 | 0.76 | 0.03 | a6ygk0r9s5xuj |  | SELECT A.JOB_NAME, ( CASE A.ST... |
| 31.25 | 83 | 0.38 | 0.08 | 96.70 | 2.96 | 8mdz49zkajhw3 | MMON_SLAVE | SELECT /*+ OPT_PARAM('_fix_con... |
| 28.91 | 2 | 14.45 | 0.08 | 49.24 | 51.90 | f92dm8jbg1spx | JDBC Thin Client | SELECT DISTINCT FSIEP.ANNO_FAS... |

Osservando il comportamento del sistema operativo in questo lancio, il database server non mostra segni di sofferenza: né la CPU ha mai raggiunto il 100% nè il carico di lavoro ha superato la soglia oltre la quale i tempi di risposta si allungano in modo non lineare. Infatti, come mostra la tabella seguente contenente i dati estratti nella fase più onerosa che il sistema ha sopportato durante il lancio, i parametri salienti sono tutti nei limiti.

Tabella 3: Consumo delle risorse hardware rilevate con il comando TOP
| top - 14:44:11 up 48 days, 56 min,  2 users,  load average: 10.63, 10.70, 9.13
Tasks: 715 total,   8 running, 707 sleeping,   0 stopped,   0 zombie
Cpu(s): 54.1%us,  1.6%sy,  0.0%ni, 35.2%id,  8.9%wa,  0.0%hi,  0.2%si,  0.0%st
Mem:  24608844k total, 22801300k used,  1807544k free,   357784k buffers
Swap: 16650232k total,    10616k used, 16639616k free, 19069552k cached |
| --- |
| top - 14:45:12 up 48 days, 57 min,  2 users,  load average: 15.82, 12.11, 9.71
Tasks: 717 total,   1 running, 716 sleeping,   0 stopped,   0 zombie
Cpu(s): 34.2%us,  1.1%sy,  0.0%ni, 31.4%id, 33.3%wa,  0.0%hi,  0.1%si,  0.0%st
Mem:  24608844k total, 22763008k used,  1845836k free,   358072k buffers
Swap: 16650232k total,    10580k used, 16639652k free, 19086644k cached |
| top - 14:46:12 up 48 days, 58 min,  2 users,  load average: 10.70, 11.42, 9.62
Tasks: 715 total,   9 running, 706 sleeping,   0 stopped,   0 zombie
Cpu(s): 38.9%us,  1.0%sy,  0.0%ni, 49.4%id, 10.6%wa,  0.0%hi,  0.1%si,  0.0%st
Mem:  24608844k total, 22801888k used,  1806956k free,   358316k buffers
Swap: 16650232k total,    10580k used, 16639652k free, 19084636k cached |
| top - 14:47:12 up 48 days, 59 min,  2 users,  load average: 11.29, 11.44, 9.74
Tasks: 715 total,  11 running, 704 sleeping,   0 stopped,   0 zombie
Cpu(s): 49.3%us,  1.5%sy,  0.0%ni, 34.1%id, 15.0%wa,  0.0%hi,  0.1%si,  0.0%st
Mem:  24608844k total, 23153552k used,  1455292k free,   358488k buffers
Swap: 16650232k total,    10580k used, 16639652k free, 19089068k cached |


Tabella 4: Legenda del comando TOP
| 1° Riga | 2° Riga | 3° Riga | 4° e 5° Riga |
| --- | --- | --- | --- |
| current time 
uptime of the machine 
users sessions logged in 
average load on the system, the 3 values refer to the last minute, five minutes and 15 minutes | Processes running in totals (73 total)
Processes running (2 running)
Processes sleeping (71 sleeping)
Processes stopped (0 stopped)
Processes waiting to be stoppati from the parent process (0 zombie) | Percentage of the CPU for user processes us
Percentage of the CPU for system processes sy
Percentage of the CPU processes with priority upgrade nice ni
Percentage of the CPU not used id
Percentage of the CPU processes waiting for I/O operations wa
Percentage of the CPU serving hardware interrupts hi 
Percentage of the CPU serving software interrupts si
The amount of CPU ‘stolen’ from this virtual machine by the hypervisor for other tasks (such as running another virtual machine) this will be 0 on desktop and server without Virtual machine st | Total physical memory (RAM/Swap)
Used physical memory/swap
Free physical memory/swap
Used physical memory/swap
 Total buffers cached. |


## Test n°2: 110 utenti Distrettuali e 200 Avvocati per un intervallo di 1 ora
## Sistema Centrale
Tempo di risposta medio:

Utenti concorrenti:

Latenza:

Throughput:

Statistiche:
| Requests | Executions | Executions | Time | Time |
| --- | --- | --- | --- | --- |
| Label | #Samples | KO | Error % | Average |
| Total | 10504 | 312 | 2.97% | 3078.70 |
| 1 /PST/SIUS/login | 1634 | 0 | 0.00% | 56.68 |
| 67 /PST/SIUS/j_spring_security_check;jsessionid= | 1568 | 4 | 0.26% | 106.22 |
| 114 /PST/SIUS/ricerca/procedimenti/exec | 1511 | 108 | 7.15% | 1889.14 |
| 119 /PST/SIUS/ricerca/procedimenti/dettaglio | 145 | 2 | 1.38% | 2531.63 |
| 120 /PST/SIUS/ricerca/procedimenti/exec | 143 | 18 | 12.59% | 1273.99 |
| 121 /PST/SIUS/ricerca/procedimenti/dettaglio | 493 | 3 | 0.61% | 1994.78 |
| 122 /PST/SIUS/ricerca/procedimenti/exec | 490 | 34 | 6.94% | 1282.43 |
| 123 /PST/SIUS/ricerca/procedimenti/stampa | 1451 | 142 | 9.79% | 14492.53 |
| 124 /PST/SIUS/ricerca/soggetti | 1435 | 0 | 0.00% | 3395.73 |
| 177 /PST/SIUS/j_spring_security_logout | 1434 | 1 | 0.07% | 318.19 |
| Accesso dati soggetto | 1437 | 0 | 0.00% | 3392.76 |
| Dettaglio decreto | 510 | 3 | 0.59% | 2051.04 |
| Dettaglio ordinanza | 154 | 2 | 1.30% | 2626.06 |
| Landing login | 1634 | 0 | 0.00% | 56.73 |
| Login | 1568 | 4 | 0.26% | 106.22 |
| Logout | 1434 | 1 | 0.07% | 318.19 |
| Ricerca estremi procedimenti | 2201 | 160 | 7.27% | 1755.36 |
| Stampa procedimento | 1456 | 142 | 9.75% | 14487.00 |


## Sistema Distrettuale
Tempo di risposta medio:

Utenti concorrenti:

Latenza:


Throughput:

Statistiche:
| Requests | Executions | Executions | Executions | Time |
| --- | --- | --- | --- | --- |
| Label | #Samples | KO | Error % | Average |
| Total | 936057 | 45148 | 4.82% | 47.76 |
| 1 / | 45665 | 0 | 0.00% | 2.07 |
| 1 /jsp/Main.jsp | 791 | 0 | 0.00% | 294.13 |
| 4 /jsp/Main.jsp | 255 | 0 | 0.00% | 4.05 |
| 4 /login.jsp | 1419 | 0 | 0.00% | 2.27 |
| 5 /jsp/Main.jsp | 321 | 0 | 0.00% | 92.08 |
| 6 /jsp/Main.jsp | 253 | 4 | 1.58% | 454.95 |
| 9 /jsp/Main.jsp | 45665 | 0 | 0.00% | 32.32 |
| 10 /frame.htm | 45663 | 0 | 0.00% | 0.99 |
| 11 /jsp/files/logo.jsp | 45663 | 0 | 0.00% | 0.99 |
| 11 /jsp/Main.jsp | 1419 | 0 | 0.00% | 30.42 |
| 12 /frame.htm | 1419 | 0 | 0.00% | 1.08 |
| 12 /jsp/files/up.jsp | 45663 | 0 | 0.00% | 1.06 |
| 12 /jsp/Main.jsp | 152 | 0 | 0.00% | 12.74 |
| 13 /jsp/files/logo.jsp | 1419 | 0 | 0.00% | 1.18 |
| 13 /jsp/files/menu.jsp | 45663 | 0 | 0.00% | 1.23 |
| 13 /jsp/Main.jsp | 248 | 86 | 34.68% | 253.14 |
| 14 /jsp/files/content_frame.jsp | 45663 | 0 | 0.00% | 0.97 |
| 14 /jsp/files/up.jsp | 1419 | 0 | 0.00% | 1.05 |
| 15 /jsp/files/menu.jsp | 1419 | 0 | 0.00% | 1.29 |
| 15 /jsp/Main.jsp | 152 | 152 | 100.00% | 16.46 |
| 16 /jsp/files/content_frame.jsp | 1419 | 0 | 0.00% | 1.09 |
| 22 /html/blank.htm | 1419 | 0 | 0.00% | 1.07 |
| 23 /html/blank.htm | 45663 | 0 | 0.00% | 0.91 |
| 23 /jsp/Main.jsp | 169 | 101 | 59.76% | 371.01 |
| 24 /html/blankGray.htm | 45663 | 0 | 0.00% | 0.96 |
| 25 /jsp/files/fastAccessMenu.jsp | 45663 | 0 | 0.00% | 1.26 |
| 28 /jsp/files/fastAccessMenu.jsp | 1419 | 0 | 0.00% | 1.19 |
| 29 /html/blankGray.htm | 1419 | 0 | 0.00% | 0.92 |
| 29 /jsp/Main.jsp | 68 | 0 | 0.00% | 10.41 |
| 33 /jsp/Main.jsp | 68 | 0 | 0.00% | 257.12 |
| 35 /jsp/Main.jsp | 52 | 0 | 0.00% | 720.35 |
| 38 /jsp/Main.jsp | 68 | 0 | 0.00% | 16.82 |
| 41 /jsp/Main.jsp | 68 | 0 | 0.00% | 17.40 |
| 42 /jsp/Main.jsp | 49 | 0 | 0.00% | 54213.45 |
| 43 /jsp/Main.jsp | 1419 | 0 | 0.00% | 4.39 |
| 44 /jsp/Main.jsp | 116 | 0 | 0.00% | 372.45 |
| 45 /jsp/Main.jsp | 1161 | 0 | 0.00% | 7968.76 |
| 47 /jsp/Main.jsp | 1419 | 0 | 0.00% | 4.16 |
| 49 /jsp/Main.jsp | 1419 | 0 | 0.00% | 33.47 |
| 51 /jsp/files/Stampa.jsp | 68 | 0 | 0.00% | 1.31 |
| 51 /jsp/Main.jsp | 1084 | 0 | 0.00% | 278.92 |
| 55 /jsp/Main.jsp | 128 | 0 | 0.00% | 4677.23 |
| 56 /jsp/Main.jsp | 1486 | 0 | 0.00% | 5851.77 |
| 57 /jsp/Main.jsp | 1084 | 0 | 0.00% | 214.92 |
| 60 /jsp/Main.jsp | 67 | 0 | 0.00% | 74.33 |
| 62 /jsp/Main.jsp | 1410 | 0 | 0.00% | 221.29 |
| 64 /jsp/Main.jsp | 165 | 0 | 0.00% | 127.72 |
| 67 /jsp/Main.jsp | 164 | 3 | 1.83% | 67.56 |
| 68 /jsp/files/siap/sico/Calendario.jsp | 1410 | 0 | 0.00% | 1.99 |
| 68 /jsp/Main.jsp | 161 | 0 | 0.00% | 275.61 |
| 72 /jsp/Main.jsp | 1410 | 0 | 0.00% | 27.85 |
| 74 /jsp/Main.jsp | 161 | 9 | 5.59% | 675.87 |
| 75 /html/blank.htm | 1410 | 0 | 0.00% | 0.94 |
| 76 /jsp/Main.jsp | 1410 | 0 | 0.00% | 12.50 |
| 79 /jsp/Main.jsp | 3238 | 0 | 0.00% | 50.85 |
| 82 /jsp/Main.jsp | 1410 | 9 | 0.64% | 401.12 |
| 86 /jsp/Main.jsp | 44 | 0 | 0.00% | 6.32 |
| 89 /jsp/Main.jsp | 44 | 0 | 0.00% | 126.11 |
| 91 /jsp/Main.jsp | 44 | 0 | 0.00% | 808.64 |
| 92 /jsp/Main.jsp | 1401 | 0 | 0.00% | 63.31 |
| 97 /jsp/Main.jsp | 35 | 3 | 8.57% | 1634.29 |
| 101 /jsp/Main.jsp | 1400 | 0 | 0.00% | 13.18 |
| 104 /jsp/Main.jsp | 1400 | 0 | 0.00% | 21.16 |
| 107 /jsp/Main.jsp | 1400 | 1400 | 100.00% | 11.05 |
| 119 /jsp/Main.jsp | 42281 | 0 | 0.00% | 4.05 |
| 121 /jsp/Main.jsp | 42281 | 0 | 0.00% | 17.93 |
| 122 /jsp/Main.jsp | 32 | 32 | 100.00% | 18.81 |
| 125 /jsp/Main.jsp | 41862 | 0 | 0.00% | 24.52 |
| 130 /jsp/Main.jsp | 41860 | 24949 | 59.60% | 37.39 |
| 133 /jsp/Main.jsp | 16910 | 0 | 0.00% | 41.36 |
| 144 /jsp/Main.jsp | 1083 | 0 | 0.00% | 30.39 |
| 147 /jsp/Main.jsp | 1083 | 1083 | 100.00% | 65.39 |
| 186 /jsp/Main.jsp | 416 | 0 | 0.00% | 25.23 |
| 191 /jsp/Main.jsp | 416 | 247 | 59.38% | 130.36 |
| 205 /jsp/Main.jsp | 162 | 162 | 100.00% | 273.32 |
| 227 /jsp/Main.jsp | 2726 | 0 | 0.00% | 4.43 |
| 231 /jsp/Main.jsp | 2726 | 0 | 0.00% | 4.34 |
| 233 /jsp/Main.jsp | 2726 | 0 | 0.00% | 27.06 |
| 240 /jsp/Main.jsp | 1633 | 0 | 0.00% | 5980.02 |
| 441 /jsp/Main.jsp | 16910 | 0 | 0.00% | 19.75 |
| 445 /jsp/Main.jsp | 16910 | 0 | 0.00% | 11.27 |
| 449 /jsp/Main.jsp | 16910 | 0 | 0.00% | 16.43 |
| 454 /jsp/Main.jsp | 16910 | 0 | 0.00% | 14.03 |
| 460 /jsp/Main.jsp | 16909 | 0 | 0.00% | 13.11 |
| 464 /jsp/files/siap/sico/cssa/FiltraCssaLista.jsp | 16909 | 0 | 0.00% | 1.11 |
| 469 /jsp/Main.jsp | 16909 | 0 | 0.00% | 19.51 |
| 472 /jsp/Main.jsp | 16909 | 0 | 0.00% | 20.83 |
| 476 /jsp/Main.jsp | 16909 | 0 | 0.00% | 19.20 |
| 480 /jsp/Main.jsp | 16909 | 0 | 0.00% | 12.04 |
| 484 /jsp/Main.jsp | 16909 | 0 | 0.00% | 17.55 |
| 492 /jsp/Main.jsp | 16909 | 0 | 0.00% | 11.08 |
| 495 /jsp/Main.jsp | 16908 | 0 | 0.00% | 32.46 |
| 500 /jsp/Main.jsp | 16908 | 16908 | 100.00% | 15.35 |
| cerca autorita competente | 16908 | 0 | 0.00% | 73.07 |
| cerca istituto di detenzione | 16910 | 0 | 0.00% | 27.70 |
| cerca sede uepe | 16909 | 0 | 0.00% | 33.72 |
| cerca UDS | 16909 | 0 | 0.00% | 40.03 |
| click calcola data fine pena | 169 | 101 | 59.76% | 371.22 |
| click calendario | 1410 | 0 | 0.00% | 1.99 |
| click concessione | 16910 | 0 | 0.00% | 41.36 |
| click decisioni di sorveglianza | 42281 | 0 | 0.00% | 21.99 |
| click iscrizione manuale | 4145 | 0 | 0.00% | 4.41 |
| click iscrizione procedimento | 1410 | 0 | 0.00% | 221.29 |
| click istituto di detenzione | 68 | 0 | 0.00% | 267.53 |
| click liberazione anticipata | 416 | 0 | 0.00% | 25.23 |
| click lista oggetto | 1083 | 0 | 0.00% | 30.39 |
| click magistrato | 1410 | 0 | 0.00% | 59.81 |
| click oggetti | 1401 | 0 | 0.00% | 63.31 |
| click ok popup aggiornamento | 67 | 0 | 0.00% | 74.33 |
| click ordine di esecuzione | 164 | 3 | 1.83% | 338.14 |
| click ricerca procedimento per numero | 1419 | 0 | 0.00% | 37.64 |
| click ricerca titolo per numero | 2726 | 0 | 0.00% | 31.40 |
| click scegli TDS | 16910 | 0 | 0.00% | 19.75 |
| click scelta oggetto | 1400 | 0 | 0.00% | 13.18 |
| click sede | 169 | 0 | 0.00% | 22.70 |
| click sede TDS | 68 | 0 | 0.00% | 17.40 |
| click semiliberta | 41862 | 0 | 0.00% | 24.52 |
| click stampa | 68 | 0 | 0.00% | 3755.03 |
| click su ordine di esecuzione | 255 | 4 | 1.57% | 455.44 |
| click su ordini di esecuzione-scarcerazione | 435 | 0 | 0.00% | 122.18 |
| click su ricerca | 66 | 0 | 0.00% | 5203.52 |
| click su sospensione esecuzione 656 cpp | 168 | 0 | 0.00% | 125.44 |
| click titolo esecutivo | 1400 | 0 | 0.00% | 21.16 |
| conferma concessione semiliberta | 16908 | 16908 | 100.00% | 15.47 |
| conferma inserimento | 1410 | 9 | 0.64% | 401.12 |
| conferma liberazione | 169 | 0 | 0.00% | 154.20 |
| conferma oggetto | 1400 | 1400 | 100.00% | 11.25 |
| conferma ordine di scarcerazione | 68 | 0 | 0.00% | 548.63 |
| conferma ordine esecuzione | 162 | 162 | 100.00% | 273.50 |
| conferma sospensione | 32 | 32 | 100.00% | 18.94 |
| dettaglio procedimento | 1084 | 0 | 0.00% | 278.92 |
| filtra istituto di dentenzione | 68 | 0 | 0.00% | 16.82 |
| filtra istituto di detenzione | 16910 | 0 | 0.00% | 14.03 |
| home page | 47084 | 0 | 0.00% | 2.08 |
| iscrizione procedimento | 1084 | 0 | 0.00% | 214.92 |
| login | 47084 | 0 | 0.00% | 40.64 |
| logout | 1842 | 0 | 0.00% | 75.21 |
| pagina ricerca per soggetto | 53 | 0 | 0.00% | 706.75 |
| ricerca avanzata | 50 | 0 | 0.00% | 3468.10 |
| ricerca procedimento | 44271 | 25294 | 57.13% | 238.99 |
| ricerca singolo procedimento | 2726 | 0 | 0.00% | 6962.51 |
| ricerca soggetto | 52 | 0 | 0.00% | 58188.46 |
| salva iscrizione procedimento | 1083 | 1083 | 100.00% | 65.60 |
| scelta sede | 152 | 152 | 100.00% | 67.23 |
| sospensione/revoca | 44 | 0 | 0.00% | 934.75 |
| sospensioni/interruzioni del PM | 45 | 0 | 0.00% | 6.18 |
| valida documento | 67 | 0 | 0.00% | 141.34 |


## Database
I tempi di attesa del test sono molto simili a quanto misurato nel test precedente ma con un contributo raddoppiato della metrica “direct path write temp”.

Tabella 5: Tempi di attesa (Wait Times)
| Event | Waits | Total Wait Time (sec) | Wait Avg(ms) | % DB time | Wait Class |
| --- | --- | --- | --- | --- | --- |
| DB CPU |  | 28.4K |  | 44.2 |  |
| direct path write temp | 6,600,045 | 19.7K | 2.98 | 30.6 | User I/O |
| log file sync | 585,468 | 4154.8 | 7.10 | 6.5 | Commit |
| latch: cache buffers chains | 407,578 | 3355.8 | 8.23 | 5.2 | Concurrency |
| db file sequential read | 119,901 | 1487.7 | 12.41 | 2.3 | User I/O |
| direct path read | 1,400,354 | 734.2 | 0.52 | 1.1 | User I/O |
| direct path read temp | 9,123,590 | 434.4 | 0.05 | .7 | User I/O |
| read by other session | 14,107 | 167.6 | 11.88 | .3 | User I/O |
| latch: row cache objects | 20,113 | 79.7 | 3.96 | .1 | Concurrency |
| buffer exterminate | 5,356 | 58.7 | 10.95 | .1 | Other |


In questo test ai primi cinque posti si trovano istruzioni SQL molto simili, effetto dell’errato binding delle variabili, eseguite quasi 220 volte ciascuna.

Tabella 6: Istruzioni SQL con i tempi di risposta maggiori
| Elapsed Time (s) | Executions | Elapsed Time per Exec (s) | %Total | %CPU | %IO | SQL Id | SQL Module | SQL Text |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1,315.09 | 218 | 6.03 | 2.05 | 39.11 | 55.98 | 45s6ah4bhak7d | JDBC Thin Client | SELECT COUNT(*) NUM FROM ( SEL... |
| 1,282.48 | 219 | 5.86 | 1.99 | 40.18 | 54.97 | 72vth0ghu7rdg | JDBC Thin Client | SELECT COUNT(*) NUM FROM ( SEL... |
| 1,271.24 | 218 | 5.83 | 1.98 | 40.46 | 54.15 | 4k0t94xwxyubm | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,268.38 | 219 | 5.79 | 1.97 | 40.68 | 54.07 | 203vwndv2n974 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,263.24 | 219 | 5.77 | 1.96 | 40.96 | 54.04 | 4dc1xabckf67v | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,234.82 | 218 | 5.66 | 1.92 | 41.66 | 53.16 | a9rqy8nahghmy | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,161.06 | 2,320 | 0.50 | 1.81 | 22.17 | 69.83 | 6qk3tkcw4rzaq | JDBC Thin Client | BEGIN AVVOCATURA_SIUS.CERCA_FA... |
| 663.10 | 109 | 6.08 | 1.03 | 38.78 | 55.84 | 4x8vwt5funyf3 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 657.36 | 109 | 6.03 | 1.02 | 39.09 | 56.11 | bxa49q64h4p3u | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 651.97 | 109 | 5.98 | 1.01 | 39.51 | 55.83 | 5fxqm4z1q4ym4 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 651.28 | 109 | 5.98 | 1.01 | 39.53 | 55.61 | affrxkrq0h4ba | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |


Osservando il comportamento del sistema operativo in questo lancio, il database server mostra segni di sofferenza: sebbene la CPU non abbia mai raggiunto il 100% di utilizzo, il carico di lavoro ha superato la soglia oltre la quale i tempi di risposta non aumentano più in modo lineare. Infatti, come mostra la tabella seguente contenente i dati estratti nella fase più onerosa che il sistema ha sopportato durante il lancio, il load avarage sale considerevolmente in proporzione all’aumentato numero di Tasks.

Tabella 7: Consumo delle risorse hardware rilevate con il comando TOP
| top - 17:29:41 up 48 days,  3:42,  2 users,  load average: 43.64, 38.22, 26.65
Tasks: 1070 total,  29 running, 1041 sleeping,   0 stopped,   0 zombie
Cpu(s): 82.6%us,  9.9%sy,  0.0%ni,  0.7%id,  3.7%wa,  0.0%hi,  3.0%si,  0.0%st
Mem:  24608844k total, 24361412k used,   247432k free,   110648k buffers
Swap: 16650232k total,    27940k used, 16622292k free, 16193168k cached |
| --- |
| top - 17:30:41 up 48 days,  3:43,  2 users,  load average: 47.25, 40.03, 27.99
Tasks: 1068 total,  20 running, 1048 sleeping,   0 stopped,   0 zombie
Cpu(s): 85.5%us,  9.8%sy,  0.0%ni,  0.3%id,  1.5%wa,  0.0%hi,  2.9%si,  0.0%st
Mem:  24608844k total, 24358880k used,   249964k free,   110956k buffers
Swap: 16650232k total,    28008k used, 16622224k free, 16184288k cached |
| top - 17:31:41 up 48 days,  3:44,  2 users,  load average: 43.09, 40.50, 28.91
Tasks: 1068 total,  11 running, 1057 sleeping,   0 stopped,   0 zombie
Cpu(s): 85.2%us,  8.5%sy,  0.0%ni,  2.0%id,  2.0%wa,  0.0%hi,  2.3%si,  0.0%st
Mem:  24608844k total, 24331088k used,   277756k free,   111236k buffers
Swap: 16650232k total,    28136k used, 16622096k free, 16100668k cached |
| top - 17:32:41 up 48 days,  3:45,  2 users,  load average: 24.10, 35.32, 27.85
Tasks: 1068 total,  20 running, 1048 sleeping,   0 stopped,   0 zombie
Cpu(s): 46.5%us,  2.1%sy,  0.0%ni, 40.1%id, 11.2%wa,  0.0%hi,  0.2%si,  0.0%st
Mem:  24608844k total, 24028772k used,   580072k free,    86340k buffers
Swap: 16650232k total,    28240k used, 16621992k free, 15836384k cached |


## Test n°3: 110 utenti Distrettuali e 500 Avvocati per un intervallo di 1 ora
## Sistema Centrale
Tempo di risposta medio:

Utenti concorrenti:

Latenza:


Throughput:

Statistiche:
| Requests | Executions | Executions | Executions | Time |
| --- | --- | --- | --- | --- |
| Label | #Samples | KO | Error % | Average |
| Total | 6722 | 25 | 0.37% | 26695.97 |
| 1 /PST/SIUS/login | 1197 | 0 | 0.00% | 102.06 |
| 67 /PST/SIUS/j_spring_security_check;jsessionid= | 975 | 4 | 0.41% | 124.79 |
| 114 /PST/SIUS/ricerca/procedimenti/exec | 962 | 10 | 1.04% | 1448.41 |
| 119 /PST/SIUS/ricerca/procedimenti/dettaglio | 75 | 1 | 1.33% | 2591.39 |
| 120 /PST/SIUS/ricerca/procedimenti/exec | 75 | 0 | 0.00% | 1220.43 |
| 121 /PST/SIUS/ricerca/procedimenti/dettaglio | 299 | 0 | 0.00% | 2614.46 |
| 122 /PST/SIUS/ricerca/procedimenti/exec | 299 | 0 | 0.00% | 1392.40 |
| 123 /PST/SIUS/ricerca/procedimenti/stampa | 944 | 10 | 1.06% | 131618.87 |
| 124 /PST/SIUS/ricerca/soggetti | 698 | 0 | 0.00% | 1663.98 |
| 177 /PST/SIUS/j_spring_security_logout | 698 | 0 | 0.00% | 403.07 |
| Accesso dati soggetto | 706 | 0 | 0.00% | 1645.12 |
| Dettaglio decreto | 310 | 0 | 0.00% | 2521.69 |
| Dettaglio ordinanza | 78 | 1 | 1.28% | 2491.72 |
| Landing login | 1197 | 0 | 0.00% | 102.26 |
| Login | 975 | 4 | 0.41% | 124.79 |
| Logout | 698 | 0 | 0.00% | 403.07 |
| Ricerca estremi procedimenti | 1349 | 10 | 0.74% | 1418.74 |
| Stampa procedimento | 946 | 10 | 1.06% | 132619.49 |




## Database
In questo test si sperimenta un notevole accodamento dei processi utenti, in numero nettamente più alto, per l’accesso dell’area di memoria condivisa, SGA, in particolare alla buffer cache “latch: cache buffers chains”. Anche in questo caso i tempi di attesa seguono lo stesso schema dei test precedenti.

Tabella 8: Tempi di attesa (Wait Times)
| Event | Waits | Total Wait Time (sec) | Wait Avg(ms) | % DB time | Wait Class |
| --- | --- | --- | --- | --- | --- |
| latch: cache buffers chains | 1,140,019 | 87.1K | 76.38 | 51.1 | Concurrency |
| DB CPU |  | 25.6K |  | 15.0 |  |
| direct path write temp | 3,758,737 | 15K | 3.98 | 8.8 | User I/O |
| direct path read temp | 5,510,282 | 3598 | 0.65 | 2.1 | User I/O |
| log file sync | 566,623 | 2683.8 | 4.74 | 1.6 | Commit |
| latch: row cache objects | 77,525 | 1766.9 | 22.79 | 1.0 | Concurrency |
| direct path read | 1,444,361 | 945.4 | 0.65 | .6 | User I/O |
| db file sequential read | 117,115 | 286.9 | 2.45 | .2 | User I/O |
| latch: shared pool | 21,725 | 198.5 | 9.14 | .1 | Concurrency |
| cursor: pin S wait on X | 249 | 36.5 | 146.63 | .0 | Concurrency |


In questo test ai primi sette posti si trovano istruzioni SQL molto simili, effetto dell’errato binding delle variabili, eseguite più di 230 volte ciascuna. Si manifesta il medesimo andamento del test precedente.

Tabella 9: Istruzioni SQL con i tempi di risposta maggiori
| Elapsed Time (s) | Executions | Elapsed Time per Exec (s) | %Total | %CPU | %IO | SQL Id | SQL Module | SQL Text |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1,528.61 | 234 | 6.53 | 0.90 | 37.72 | 33.38 | cyp92py4wxpz0 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,519.31 | 233 | 6.52 | 0.89 | 37.75 | 33.43 | 4k0t94xwxyubm | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,516.53 | 233 | 6.51 | 0.89 | 37.85 | 33.28 | a9rqy8nahghmy | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,510.56 | 234 | 6.46 | 0.89 | 38.23 | 33.46 | 72vth0ghu7rdg | JDBC Thin Client | SELECT COUNT(*) NUM FROM ( SEL... |
| 1,506.64 | 234 | 6.44 | 0.88 | 38.24 | 33.00 | 203vwndv2n974 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,503.74 | 234 | 6.43 | 0.88 | 38.37 | 32.78 | 4dc1xabckf67v | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,480.69 | 233 | 6.35 | 0.87 | 38.87 | 32.97 | 45s6ah4bhak7d | JDBC Thin Client | SELECT COUNT(*) NUM FROM ( SEL... |
| 824.06 | 1,337 | 0.62 | 0.48 | 19.25 | 7.39 | 6qk3tkcw4rzaq | JDBC Thin Client | BEGIN AVVOCATURA_SIUS.CERCA_FA... |
| 751.36 | 113 | 6.65 | 0.44 | 37.13 | 33.81 | bxa49q64h4p3u | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 744.88 | 113 | 6.59 | 0.44 | 37.64 | 33.02 | 5fxqm4z1q4ym4 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |


Osservando il comportamento del sistema operativo in questo lancio, il database server mostra segni di notevole sofferenza: la CPU raggiunge il 100% di utilizzo e il carico di lavoro ha superato la soglia oltre la quale i tempi di risposta non aumentano più in modo lineare. Infatti, come mostra la tabella seguente contenente i dati estratti nella fase più onerosa che il sistema ha sopportato durante il lancio, il load avarage sale considerevolmente in proporzione all’aumentato numero di Tasks. Il sistema è in notevole difficoltà.

Tabella 10: Consumo delle risorse hardware rilevate con il comando TOP
| top - 13:09:17 up 48 days, 23:21,  2 users,  load average: 93.68, 82.70, 51.86
Tasks: 914 total,  57 running, 857 sleeping,   0 stopped,   0 zombie
Cpu(s): 92.8%us,  6.0%sy,  0.0%ni,  0.0%id,  0.0%wa,  0.0%hi,  1.3%si,  0.0%st
Mem:  24608844k total, 24405504k used,   203340k free,     1484k buffers
Swap: 16650232k total,   199680k used, 16450552k free, 17697552k cached |
| --- |
| top - 13:10:16 up 48 days, 23:22,  2 users,  load average: 92.80, 84.83, 54.54
Tasks: 916 total,  65 running, 851 sleeping,   0 stopped,   0 zombie
Cpu(s): 92.7%us,  6.0%sy,  0.0%ni,  0.0%id,  0.0%wa,  0.0%hi,  1.2%si,  0.0%st
Mem:  24608844k total, 24406512k used,   202332k free,     3632k buffers
Swap: 16650232k total,   217972k used, 16432260k free, 17929296k cached |
| top - 13:11:17 up 48 days, 23:23,  2 users,  load average: 70.97, 80.49, 54.97
Tasks: 914 total,  30 running, 884 sleeping,   0 stopped,   0 zombie
Cpu(s): 82.5%us, 10.8%sy,  0.0%ni,  0.3%id,  3.3%wa,  0.0%hi,  3.1%si,  0.0%st
Mem:  24608844k total, 24387772k used,   221072k free,     4184k buffers
Swap: 16650232k total,   227924k used, 16422308k free, 18347488k cached |
| top - 13:12:16 up 48 days, 23:24,  2 users,  load average: 30.38, 67.57, 52.15
Tasks: 914 total,   1 running, 913 sleeping,   0 stopped,   0 zombie
Cpu(s):  0.1%us,  0.1%sy,  0.0%ni, 99.8%id,  0.0%wa,  0.0%hi,  0.0%si,  0.0%st
Mem:  24608844k total, 24237608k used,   371236k free,     4764k buffers
Swap: 16650232k total,   228464k used, 16421768k free, 18352656k cached |


## Test n°4: 500 Avvocati per un intervallo di 30 minuti
## Sistema Centrale
Tempo di risposta medio:

Utenti concorrenti:

Latenza:


Throughput:

Statistiche:
| Requests | Executions | Executions | Executions | Time |
| --- | --- | --- | --- | --- |
| Label | #Samples | KO | Error % | Average |
| Total | 10713 | 35 | 0.33% | 24546.92 |
| 1 /PST/SIUS/login | 1639 | 0 | 0.00% | 112.23 |
| 67 /PST/SIUS/j_spring_security_check;jsessionid= | 1639 | 4 | 0.24% | 113.11 |
| 114 /PST/SIUS/ricerca/procedimenti/exec | 1610 | 15 | 0.93% | 1513.54 |
| 119 /PST/SIUS/ricerca/procedimenti/dettaglio | 186 | 1 | 0.54% | 3403.14 |
| 120 /PST/SIUS/ricerca/procedimenti/exec | 174 | 0 | 0.00% | 1825.60 |
| 121 /PST/SIUS/ricerca/procedimenti/dettaglio | 580 | 0 | 0.00% | 2433.42 |
| 122 /PST/SIUS/ricerca/procedimenti/exec | 571 | 0 | 0.00% | 1551.33 |
| 123 /PST/SIUS/ricerca/procedimenti/stampa | 1521 | 15 | 0.99% | 120967.34 |
| 124 /PST/SIUS/ricerca/soggetti | 1153 | 0 | 0.00% | 2237.29 |
| 177 /PST/SIUS/j_spring_security_logout | 1140 | 0 | 0.00% | 535.31 |
| Accesso dati soggetto | 1161 | 0 | 0.00% | 2275.24 |
| Dettaglio decreto | 603 | 0 | 0.00% | 2681.61 |
| Dettaglio ordinanza | 199 | 1 | 0.50% | 4898.67 |
| Landing login | 1639 | 0 | 0.00% | 112.23 |
| Login | 1639 | 4 | 0.24% | 113.11 |
| Logout | 1140 | 0 | 0.00% | 535.31 |
| Ricerca estremi procedimenti | 2384 | 15 | 0.63% | 1582.22 |
| Stampa procedimento | 1525 | 15 | 0.98% | 121828.89 |


## Database
In questo test si sperimenta un notevole accodamento dei processi utenti, in numero comunque alto, per l’accesso dell’area di memoria condivisa, SGA, in particolare alla buffer cache “latch: cache buffers chains”. In questo caso i tempi di attesa per l’accesso alle aree temporanee di lavoro del database sono meno importanti rispetto ai test precedenti, ma rimangono tra i primi dopo l’attesa per accedere alla CPU.

Tabella 11: Tempi di attesa (Wait Times)
| Event | Waits | Total Wait Time (sec) | Wait Avg(ms) | % DB time | Wait Class |
| --- | --- | --- | --- | --- | --- |
| latch: cache buffers chains | 676,046 | 84.5K | 125.01 | 81.5 | Concurrency |
| DB CPU |  | 5092.1 |  | 4.9 |  |
| direct path read temp | 939,086 | 4337.2 | 4.62 | 4.2 | User I/O |
| direct path write temp | 661,233 | 2689.3 | 4.07 | 2.6 | User I/O |
| latch: row cache objects | 16,883 | 288.5 | 17.09 | .3 | Concurrency |
| direct path read | 39,494 | 77.4 | 1.96 | .1 | User I/O |
| db file sequential read | 9,240 | 63.3 | 6.85 | .1 | User I/O |
| latch: shared pool | 3,824 | 31.3 | 8.18 | .0 | Concurrency |
| wait list latch free | 3,069 | 15 | 4.89 | .0 | Other |
| cursor: pin S wait on X | 58 | 8.4 | 144.45 | .0 | Concurrency |

Poiché sono stati utilizzati solo utenti di tipo “Avvocato” le istruzioni SQL più onerose sono diverse rispetto ai test precedenti, ma molto simili tra loro in quanto non si è fatto un uso ottimale del binding delle variabili. Importante il tempo speso per due sole esecuzioni della medesima query.

Tabella 12: Istruzioni SQL con i tempi di risposta maggiori
| Elapsed Time (s) | Executions | Elapsed Time per Exec (s) | %Total | %CPU | %IO | SQL Id | SQL Module | SQL Text |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 459.52 | 2 | 229.76 | 0.44 | 3.68 | 7.89 | 9vr29725rcbdp | JDBC Thin Client | SELECT DISTINCT FSIEP.ANNO_FAS... |
| 429.99 | 2 | 214.99 | 0.41 | 3.85 | 6.91 | 7dnwhrvwnmzx4 | JDBC Thin Client | SELECT DISTINCT FSIEP.ANNO_FAS... |
| 424.52 | 2 | 212.26 | 0.41 | 3.90 | 7.58 | cpsjjwfs8a2u2 | JDBC Thin Client | SELECT DISTINCT FSIEP.ANNO_FAS... |
| 421.37 | 2 | 210.68 | 0.41 | 3.98 | 8.05 | 19rwb5tvd5fuz | JDBC Thin Client | SELECT DISTINCT FSIEP.ANNO_FAS... |
| 406.71 | 2 | 203.35 | 0.39 | 4.09 | 9.00 | 40w5z4v6yut3t | JDBC Thin Client | SELECT DISTINCT FSIEP.ANNO_FAS... |
| 388.05 | 2 | 194.03 | 0.37 | 4.28 | 7.94 | 7qr854nx74a2c | JDBC Thin Client | SELECT DISTINCT FSIEP.ANNO_FAS... |
| 388.01 | 2 | 194.01 | 0.37 | 4.30 | 7.18 | 5byxw6whcj10f | JDBC Thin Client | SELECT DISTINCT FSIEP.ANNO_FAS... |
| 380.24 | 2 | 190.12 | 0.37 | 4.40 | 6.85 | cr18d0rc63zvc | JDBC Thin Client | SELECT DISTINCT FSIEP.ANNO_FAS... |
| 376.98 | 2 | 188.49 | 0.36 | 4.41 | 7.69 | bbuswn2aza45n | JDBC Thin Client | SELECT DISTINCT FSIEP.ANNO_FAS... |
| 338.02 | 687 | 0.49 | 0.33 | 24.54 | 8.25 | 6qk3tkcw4rzaq | JDBC Thin Client | BEGIN AVVOCATURA_SIUS.CERCA_FA... |

Osservando il comportamento del sistema operativo in questo lancio, il database server mostra segni di notevole sofferenza: la CPU raggiunge il 100% di utilizzo e il carico di lavoro ha superato la soglia oltre la quale i tempi di risposta non aumentano più in modo lineare. Infatti, come mostra la tabella seguente contenente i dati estratti nella fase più onerosa che il sistema ha sopportato durante il lancio, il load avarage sale considerevolmente in proporzione all’aumentato numero di Tasks. Il sistema è in notevole difficoltà.

Tabella 13: Consumo delle risorse hardware rilevate con il comando TOP
| top - 10:02:57 up 52 days, 20:15,  2 users,  load average: 63.88, 52.88, 28.99
Tasks: 988 total,  66 running, 922 sleeping,   0 stopped,   0 zombie
Cpu(s): 94.7%us,  4.1%sy,  0.0%ni,  0.2%id,  0.3%wa,  0.0%hi,  0.7%si,  0.0%st
Mem:  24608844k total, 24406044k used,   202800k free,     1724k buffers
Swap: 16650232k total,   413844k used, 16236388k free, 16161960k cached |
| --- |
| top - 10:03:58 up 52 days, 20:16,  2 users,  load average: 67.79, 55.68, 31.43
Tasks: 988 total, 107 running, 881 sleeping,   0 stopped,   0 zombie
Cpu(s): 92.9%us,  5.4%sy,  0.0%ni,  0.0%id,  0.5%wa,  0.0%hi,  1.2%si,  0.0%st
Mem:  24608844k total, 24413924k used,   194920k free,     1704k buffers
Swap: 16650232k total,   433228k used, 16217004k free, 16241468k cached |
| top - 10:04:57 up 52 days, 20:17,  2 users,  load average: 62.47, 56.23, 33.01
Tasks: 990 total,  72 running, 918 sleeping,   0 stopped,   0 zombie
Cpu(s): 96.6%us,  2.0%sy,  0.0%ni,  0.5%id,  0.5%wa,  0.0%hi,  0.3%si,  0.0%st
Mem:  24608844k total, 24405136k used,   203708k free,     1668k buffers
Swap: 16650232k total,   438200k used, 16212032k free, 16752268k cached |
| top - 10:05:56 up 52 days, 20:18,  2 users,  load average: 40.31, 51.94, 33.04
Tasks: 988 total,   1 running, 987 sleeping,   0 stopped,   0 zombie
Cpu(s):  0.1%us,  0.1%sy,  0.0%ni, 99.8%id,  0.0%wa,  0.0%hi,  0.0%si,  0.0%st
Mem:  24608844k total, 24247208k used,   361636k free,     3096k buffers
Swap: 16650232k total,   438196k used, 16212036k free, 17662308k cached |


## Test n°5: 550 utenti Distrettuali per un intervallo di 30 minuti
## Sistema Distrettuale
Tempo di risposta medio:

Utenti concorrenti:


Latenza:


Throughput:


Statistiche:
| Requests | Executions | Executions | Executions | Time |
| --- | --- | --- | --- | --- |
| Label | #Samples | KO | Error % | Average |
| Total | 1205415 | 63597 | 5.28% | 111.98 |
| 1 / | 64251 | 0 | 0.00% | 3.68 |
| 1 /jsp/Main.jsp | 3471 | 0 | 0.00% | 653.87 |
| 4 /jsp/Main.jsp | 558 | 0 | 0.00% | 8.84 |
| 4 /login.jsp | 923 | 0 | 0.00% | 3.10 |
| 5 /jsp/Main.jsp | 2453 | 0 | 0.00% | 400.79 |
| 6 /jsp/Main.jsp | 557 | 10 | 1.80% | 59.41 |
| 9 /jsp/Main.jsp | 64250 | 0 | 0.00% | 80.25 |
| 10 /frame.htm | 64240 | 0 | 0.00% | 1.83 |
| 11 /jsp/files/logo.jsp | 64240 | 0 | 0.00% | 1.72 |
| 11 /jsp/Main.jsp | 923 | 0 | 0.00% | 69.18 |
| 12 /frame.htm | 923 | 0 | 0.00% | 1.70 |
| 12 /jsp/files/up.jsp | 64240 | 0 | 0.00% | 1.77 |
| 12 /jsp/Main.jsp | 318 | 0 | 0.00% | 21.51 |
| 13 /jsp/files/logo.jsp | 923 | 0 | 0.00% | 1.44 |
| 13 /jsp/files/menu.jsp | 64240 | 0 | 0.00% | 2.06 |
| 13 /jsp/Main.jsp | 547 | 215 | 39.31% | 985.56 |
| 14 /jsp/files/content_frame.jsp | 64240 | 0 | 0.00% | 1.69 |
| 14 /jsp/files/up.jsp | 923 | 0 | 0.00% | 1.46 |
| 15 /jsp/files/menu.jsp | 923 | 0 | 0.00% | 1.53 |
| 15 /jsp/Main.jsp | 318 | 318 | 100.00% | 30.64 |
| 16 /jsp/files/content_frame.jsp | 923 | 0 | 0.00% | 1.31 |
| 22 /html/blank.htm | 923 | 0 | 0.00% | 1.50 |
| 23 /html/blank.htm | 64240 | 0 | 0.00% | 1.62 |
| 23 /jsp/Main.jsp | 2128 | 2008 | 94.36% | 538.84 |
| 24 /html/blankGray.htm | 64236 | 0 | 0.00% | 1.70 |
| 25 /jsp/files/fastAccessMenu.jsp | 64238 | 0 | 0.00% | 2.08 |
| 28 /jsp/files/fastAccessMenu.jsp | 923 | 0 | 0.00% | 1.57 |
| 29 /html/blankGray.htm | 923 | 0 | 0.00% | 1.61 |
| 29 /jsp/Main.jsp | 120 | 0 | 0.00% | 21.53 |
| 33 /jsp/Main.jsp | 120 | 0 | 0.00% | 48.17 |
| 35 /jsp/Main.jsp | 80 | 0 | 0.00% | 39.31 |
| 38 /jsp/Main.jsp | 120 | 0 | 0.00% | 34.93 |
| 41 /jsp/Main.jsp | 120 | 0 | 0.00% | 39.34 |
| 42 /jsp/Main.jsp | 71 | 0 | 0.00% | 200092.93 |
| 43 /jsp/Main.jsp | 923 | 0 | 0.00% | 7.86 |
| 44 /jsp/Main.jsp | 252 | 0 | 0.00% | 105.70 |
| 45 /jsp/Main.jsp | 845 | 0 | 0.00% | 27124.62 |
| 47 /jsp/Main.jsp | 923 | 0 | 0.00% | 7.37 |
| 49 /jsp/Main.jsp | 923 | 0 | 0.00% | 38.83 |
| 51 /jsp/files/Stampa.jsp | 120 | 0 | 0.00% | 1.83 |
| 51 /jsp/Main.jsp | 675 | 0 | 0.00% | 602.07 |
| 55 /jsp/Main.jsp | 235 | 0 | 0.00% | 20635.82 |
| 56 /jsp/Main.jsp | 1041 | 0 | 0.00% | 20561.08 |
| 57 /jsp/Main.jsp | 675 | 0 | 0.00% | 583.27 |
| 60 /jsp/Main.jsp | 118 | 0 | 0.00% | 146.08 |
| 62 /jsp/Main.jsp | 880 | 0 | 0.00% | 557.83 |
| 64 /jsp/Main.jsp | 360 | 0 | 0.00% | 18.79 |
| 67 /jsp/Main.jsp | 350 | 5 | 1.43% | 20.73 |
| 68 /jsp/files/siap/sico/Calendario.jsp | 877 | 0 | 0.00% | 2.28 |
| 68 /jsp/Main.jsp | 345 | 0 | 0.00% | 61.52 |
| 72 /jsp/Main.jsp | 877 | 0 | 0.00% | 26.34 |
| 74 /jsp/Main.jsp | 345 | 20 | 5.80% | 4709.29 |
| 75 /html/blank.htm | 877 | 0 | 0.00% | 1.75 |
| 76 /jsp/Main.jsp | 877 | 0 | 0.00% | 23.38 |
| 79 /jsp/Main.jsp | 1916 | 0 | 0.00% | 33.20 |
| 82 /jsp/Main.jsp | 877 | 24 | 2.74% | 1497.65 |
| 86 /jsp/Main.jsp | 110 | 0 | 0.00% | 23.91 |
| 89 /jsp/Main.jsp | 109 | 0 | 0.00% | 15.20 |
| 91 /jsp/Main.jsp | 109 | 0 | 0.00% | 74.83 |
| 92 /jsp/Main.jsp | 850 | 0 | 0.00% | 54.33 |
| 97 /jsp/Main.jsp | 70 | 9 | 12.86% | 6863.66 |
| 101 /jsp/Main.jsp | 850 | 0 | 0.00% | 24.82 |
| 104 /jsp/Main.jsp | 850 | 0 | 0.00% | 36.32 |
| 107 /jsp/Main.jsp | 849 | 849 | 100.00% | 19.29 |
| 119 /jsp/Main.jsp | 61249 | 0 | 0.00% | 8.66 |
| 121 /jsp/Main.jsp | 61245 | 0 | 0.00% | 23.38 |
| 122 /jsp/Main.jsp | 59 | 59 | 100.00% | 37.81 |
| 125 /jsp/Main.jsp | 54752 | 0 | 0.00% | 46.61 |
| 130 /jsp/Main.jsp | 54740 | 36626 | 66.91% | 67.46 |
| 133 /jsp/Main.jsp | 18112 | 0 | 0.00% | 75.00 |
| 144 /jsp/Main.jsp | 675 | 0 | 0.00% | 29.44 |
| 147 /jsp/Main.jsp | 675 | 675 | 100.00% | 93.40 |
| 186 /jsp/Main.jsp | 6488 | 0 | 0.00% | 52.67 |
| 191 /jsp/Main.jsp | 6488 | 4347 | 67.00% | 311.49 |
| 205 /jsp/Main.jsp | 331 | 331 | 100.00% | 1583.30 |
| 227 /jsp/Main.jsp | 1504 | 0 | 0.00% | 9.15 |
| 231 /jsp/Main.jsp | 1504 | 0 | 0.00% | 7.71 |
| 233 /jsp/Main.jsp | 1504 | 0 | 0.00% | 47.40 |
| 240 /jsp/Main.jsp | 779 | 0 | 0.00% | 30473.72 |
| 441 /jsp/Main.jsp | 18109 | 0 | 0.00% | 39.84 |
| 445 /jsp/Main.jsp | 18109 | 0 | 0.00% | 22.54 |
| 449 /jsp/Main.jsp | 18109 | 0 | 0.00% | 41.89 |
| 454 /jsp/Main.jsp | 18109 | 0 | 0.00% | 27.13 |
| 460 /jsp/Main.jsp | 18106 | 0 | 0.00% | 22.11 |
| 464 /jsp/files/siap/sico/cssa/FiltraCssaLista.jsp | 18105 | 0 | 0.00% | 1.83 |
| 469 /jsp/Main.jsp | 18105 | 0 | 0.00% | 37.49 |
| 472 /jsp/Main.jsp | 18105 | 0 | 0.00% | 47.23 |
| 476 /jsp/Main.jsp | 18105 | 0 | 0.00% | 39.22 |
| 480 /jsp/Main.jsp | 18103 | 0 | 0.00% | 21.95 |
| 484 /jsp/Main.jsp | 18103 | 0 | 0.00% | 35.80 |
| 492 /jsp/Main.jsp | 18103 | 0 | 0.00% | 22.24 |
| 495 /jsp/Main.jsp | 18103 | 0 | 0.00% | 65.20 |
| 500 /jsp/Main.jsp | 18101 | 18101 | 100.00% | 23.96 |
| cerca autorita competente | 18103 | 0 | 0.00% | 145.20 |
| cerca istituto di detenzione | 18109 | 0 | 0.00% | 64.43 |
| cerca sede uepe | 18105 | 0 | 0.00% | 61.43 |
| cerca UDS | 18105 | 0 | 0.00% | 86.45 |
| click calcola data fine pena | 2128 | 2008 | 94.36% | 539.45 |
| click calendario | 877 | 0 | 0.00% | 2.28 |
| click concessione | 18112 | 0 | 0.00% | 75.00 |
| click decisioni di sorveglianza | 61245 | 0 | 0.00% | 32.04 |
| click iscrizione manuale | 2427 | 0 | 0.00% | 8.66 |
| click iscrizione procedimento | 880 | 0 | 0.00% | 557.83 |
| click istituto di detenzione | 120 | 0 | 0.00% | 69.70 |
| click liberazione anticipata | 6488 | 0 | 0.00% | 52.67 |
| click lista oggetto | 675 | 0 | 0.00% | 29.44 |
| click magistrato | 877 | 0 | 0.00% | 90.30 |
| click oggetti | 850 | 0 | 0.00% | 54.33 |
| click ok popup aggiornamento | 118 | 0 | 0.00% | 146.08 |
| click ordine di esecuzione | 350 | 5 | 1.43% | 81.37 |
| click ricerca procedimento per numero | 923 | 0 | 0.00% | 46.20 |
| click ricerca titolo per numero | 1504 | 0 | 0.00% | 55.11 |
| click scegli TDS | 18109 | 0 | 0.00% | 39.84 |
| click scelta oggetto | 850 | 0 | 0.00% | 24.82 |
| click sede | 2135 | 0 | 0.00% | 49.57 |
| click sede TDS | 120 | 0 | 0.00% | 39.34 |
| click semiliberta | 54752 | 0 | 0.00% | 46.61 |
| click stampa | 120 | 0 | 0.00% | 10517.68 |
| click su ordine di esecuzione | 558 | 10 | 1.79% | 68.14 |
| click su ordini di esecuzione-scarcerazione | 998 | 0 | 0.00% | 20.53 |
| click su ricerca | 137 | 0 | 0.00% | 26186.25 |
| click su sospensione esecuzione 656 cpp | 365 | 0 | 0.00% | 18.53 |
| click titolo esecutivo | 850 | 0 | 0.00% | 36.32 |
| conferma concessione semiliberta | 18101 | 18101 | 100.00% | 24.12 |
| conferma inserimento | 877 | 24 | 2.74% | 1497.66 |
| conferma liberazione | 2135 | 0 | 0.00% | 454.24 |
| conferma oggetto | 849 | 849 | 100.00% | 19.49 |
| conferma ordine di scarcerazione | 120 | 0 | 0.00% | 792.90 |
| conferma ordine esecuzione | 331 | 331 | 100.00% | 1583.55 |
| conferma sospensione | 59 | 59 | 100.00% | 37.95 |
| dettaglio procedimento | 675 | 0 | 0.00% | 602.07 |
| filtra istituto di dentenzione | 120 | 0 | 0.00% | 34.93 |
| filtra istituto di detenzione | 18109 | 0 | 0.00% | 27.13 |
| home page | 65174 | 0 | 0.00% | 3.67 |
| iscrizione procedimento | 675 | 0 | 0.00% | 583.27 |
| login | 65173 | 0 | 0.00% | 94.51 |
| logout | 1075 | 0 | 0.00% | 27.50 |
| pagina ricerca per soggetto | 86 | 0 | 0.00% | 36.57 |
| ricerca avanzata | 115 | 0 | 0.00% | 18563.03 |
| ricerca procedimento | 63433 | 41217 | 64.98% | 468.90 |
| ricerca singolo procedimento | 1504 | 0 | 0.00% | 30960.23 |
| ricerca soggetto | 80 | 0 | 0.00% | 209986.71 |
| salva iscrizione procedimento | 675 | 675 | 100.00% | 93.66 |
| scelta sede | 318 | 318 | 100.00% | 121.11 |
| sospensione/revoca | 109 | 0 | 0.00% | 90.03 |
| sospensioni/interruzioni del PM | 118 | 0 | 0.00% | 22.29 |
| valida documento | 118 | 0 | 0.00% | 441.22 |


## Database
In questo test si sperimenta un notevole incremento del tempo di attesa “direct path write temp”, superando il tempo speso per accedere alla CPU. Le aree di lavoro temporanee hanno sperimento un enorme traffico di IO, sono al primo posto nella tabella, tale da provocare tempi di attesa tanto più lunghi quanti più processi utenti concorrono ad eseguire ordinamenti e hash join.

Tabella 14: Tempi di attesa (Wait Times)
| Event | Waits | Total Wait Time (sec) | Wait Avg(ms) | % DB time | Wait Class |
| --- | --- | --- | --- | --- | --- |
| direct path write temp | 4,036,479 | 24,6K | 6.10 | 24.3 | User I/O |
| DB CPU |  | 14,3K |  | 14.1 |  |
| log file sync | 736,975 | 4888 | 6.63 | 4.8 | Commit |
| latch: row cache objects | 84,220 | 4650,1 | 55.21 | 4.6 | Concurrency |
| direct path read temp | 6,925,521 | 1337,1 | 0.19 | 1.3 | User I/O |
| latch: shared pool | 28,761 | 571,5 | 19.87 | .6 | Concurrency |
| direct path read | 577,543 | 215,1 | 0.37 | .2 | User I/O |
| db file sequential read | 56,118 | 154,3 | 2.75 | .2 | User I/O |
| library cache: mutex X | 5,159 | 88,1 | 17.07 | .1 | Concurrency |
| enq: TX - index contention | 3,663 | 69,7 | 19.02 | .1 | Concurrency |


Tutte le istruzioni SQL in tabella sono molto simili, effetto dell’errato binding delle variabili.

Tabella 15: Istruzioni SQL con i tempi di risposta maggiori
| Elapsed Time (s) | Executions | Elapsed Time per Exec (s) | %Total | %CPU | %IO | SQL Id | SQL Module | SQL Text |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 3,317.21 | 145 | 22.88 | 3.27 | 12.16 | 37.03 | 4k0t94xwxyubm | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 3,247.56 | 145 | 22.40 | 3.20 | 12.44 | 37.65 | a9rqy8nahghmy | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 3,212.11 | 145 | 22.15 | 3.17 | 12.60 | 37.69 | 4dc1xabckf67v | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 3,206.86 | 145 | 22.12 | 3.16 | 12.54 | 37.83 | cyp92py4wxpz0 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 3,187.54 | 145 | 21.98 | 3.14 | 12.63 | 37.95 | 203vwndv2n974 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 3,122.89 | 145 | 21.54 | 3.08 | 12.84 | 38.25 | 72vth0ghu7rdg | JDBC Thin Client | SELECT COUNT(*) NUM FROM ( SEL... |
| 3,040.80 | 145 | 20.97 | 3.00 | 13.16 | 38.04 | 45s6ah4bhak7d | JDBC Thin Client | SELECT COUNT(*) NUM FROM ( SEL... |
| 1,657.14 | 71 | 23.34 | 1.63 | 12.00 | 36.58 | bxa49q64h4p3u | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,654.89 | 71 | 23.31 | 1.63 | 11.99 | 36.32 | 2k6ba798xmj9h | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,602.23 | 71 | 22.57 | 1.58 | 12.36 | 37.22 | affrxkrq0h4ba | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,595.54 | 71 | 22.47 | 1.57 | 12.41 | 37.84 | d3y6uwgqs1wbs | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,591.68 | 71 | 22.42 | 1.57 | 12.42 | 37.86 | 59wkz50fxrv4y | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,589.53 | 71 | 22.39 | 1.57 | 12.42 | 37.90 | frv53z7tapkvy | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,588.95 | 70 | 22.70 | 1.57 | 12.25 | 37.54 | 3jx8z516n6t54 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,586.08 | 71 | 22.34 | 1.56 | 12.49 | 37.34 | 5tvc04xwszh7c | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,578.56 | 71 | 22.23 | 1.56 | 12.51 | 38.08 | 5fxqm4z1q4ym4 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,568.44 | 71 | 22.09 | 1.55 | 12.61 | 38.01 | 9j9bx7kazvg7q | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,558.98 | 70 | 22.27 | 1.54 | 12.48 | 38.48 | 82jzsgyr9nxnz | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,550.94 | 71 | 21.84 | 1.53 | 12.72 | 38.58 | 4x8vwt5funyf3 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,545.67 | 71 | 21.77 | 1.52 | 12.69 | 38.68 | 4qx8u6vdb731t | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |

Osservando il comportamento del sistema operativo in questo lancio, il database server mostra segni di notevole sofferenza: la CPU raggiunge il 100% di utilizzo e il carico di lavoro supera di gran lungo la soglia oltre la quale i tempi di risposta non aumentano più in modo lineare. Infatti, come mostra la tabella seguente contenente i dati estratti nella fase più onerosa che il sistema ha sopportato durante il lancio, il load avarage sale considerevolmente in proporzione all’aumentato numero di Tasks. Il sistema è in notevole difficoltà.

Tabella 16: Consumo delle risorse hardware rilevate con il comando TOP
| top - 10:32:59 up 52 days, 20:45,  2 users,  load average: 198.61, 140.71, 77.00
Tasks: 989 total, 169 running, 820 sleeping,   0 stopped,   0 zombie
Cpu(s): 89.3%us,  8.3%sy,  0.0%ni,  0.0%id,  0.0%wa,  0.0%hi,  2.3%si,  0.0%st
Mem:  24608844k total, 24344640k used,   264204k free,    24056k buffers
Swap: 16650232k total,   458348k used, 16191884k free, 16869900k cached |
| --- |
| top - 10:33:59 up 52 days, 20:46,  2 users,  load average: 213.92, 155.28, 85.98
Tasks: 989 total, 206 running, 783 sleeping,   0 stopped,   0 zombie
Cpu(s): 89.8%us,  8.1%sy,  0.0%ni,  0.0%id,  0.0%wa,  0.0%hi,  2.2%si,  0.0%st
Mem:  24608844k total, 24407744k used,   201100k free,    24520k buffers
Swap: 16650232k total,   459460k used, 16190772k free, 16897936k cached |
| top - 10:34:59 up 52 days, 20:47,  2 users,  load average: 114.93, 139.77, 85.12
Tasks: 990 total,   8 running, 982 sleeping,   0 stopped,   0 zombie
Cpu(s): 42.1%us,  0.9%sy,  0.0%ni, 57.0%id,  0.0%wa,  0.0%hi,  0.0%si,  0.0%st
Mem:  24608844k total, 23845736k used,   763108k free,    25164k buffers
Swap: 16650232k total,   459460k used, 16190772k free, 16938844k cached |
| top - 10:35:58 up 52 days, 20:48,  2 users,  load average: 42.65, 114.45, 79.84
Tasks: 988 total,   1 running, 987 sleeping,   0 stopped,   0 zombie
Cpu(s):  0.1%us,  0.1%sy,  0.0%ni, 99.8%id,  0.0%wa,  0.0%hi,  0.0%si,  0.0%st
Mem:  24608844k total, 23731320k used,   877524k free,    25704k buffers
Swap: 16650232k total,   459460k used, 16190772k free, 16941900k cached |


## Test n°6: 1000 Avvocati per un intervallo di 30 minuti
## Sistema Centrale
Tempo di risposta medio:

Utenti concorrenti:


Latenza:


Throughput:

Statistiche:
| Requests | Executions | Executions | Executions | Executions | Time |
| --- | --- | --- | --- | --- | --- |
| Label | #Samples | KO | Error % | Average | Average |
| Total | 14149 | 139 | 0.98% | 38252.84 | 38252.84 |
| 1 /PST/SIUS/login | 2599 | 16 | 0.62% | 561.15 | 561.15 |
| 67 /PST/SIUS/j_spring_security_check;jsessionid= | 2598 | 25 | 0.96% | 1674.57 | 1674.57 |
| 114 /PST/SIUS/ricerca/procedimenti/exec | 2557 | 44 | 1.72% | 71140.53 | 71140.53 |
| 119 /PST/SIUS/ricerca/procedimenti/dettaglio | 349 | 2 | 0.57% | 157863.99 | 157863.99 |
| 120 /PST/SIUS/ricerca/procedimenti/exec | 195 | 3 | 1.54% | 93913.75 | 93913.75 |
| 121 /PST/SIUS/ricerca/procedimenti/dettaglio | 893 | 2 | 0.22% | 84563.30 | 84563.30 |
| 122 /PST/SIUS/ricerca/procedimenti/exec | 743 | 3 | 0.40% | 87217.75 | 87217.75 |
| 124 /PST/SIUS/ricerca/soggetti | 1615 | 19 | 1.18% | 9657.71 | 9657.71 |
| 177 /PST/SIUS/j_spring_security_logout | 1600 | 18 | 1.13% | 1112.98 | 1112.98 |
| Accesso dati soggetto | 1624 | 19 | 1.17% | 9643.49 | 9643.49 |
| Dettaglio decreto | 924 | 2 | 0.22% | 85670.28 | 85670.28 |
| Dettaglio ordinanza | 365 | 2 | 0.55% | 161282.87 | 161282.87 |
| Landing login | 2599 | 16 | 0.62% | 561.15 | 561.15 |
| Login | 2598 | 25 | 0.96% | 1674.57 | 1674.57 |
| Logout | 1600 | 18 | 1.13% | 1112.98 | 1112.98 |
| Ricerca estremi procedimenti | 3534 | 50 | 1.41% | 76107.12 | 76107.12 |


## Database
In questo test si sperimenta un notevole incremento del tempo di attesa “direct path write temp”, superando il tempo speso per accedere alla CPU. Le aree di lavoro temporanee hanno sperimento un enorme traffico di IO, tale da provocare tempi di attesa tanto più lunghi quanti più processi utenti concorrono ad eseguire ordinamenti e hash join.

Tabella 17: Tempi di attesa (Wait Times)
| Event | Waits | Total Wait Time (sec) | Wait Avg(ms) | % DB time | Wait Class |
| --- | --- | --- | --- | --- | --- |
| direct path write temp | 4,153,836 | 34,9K | 8.41 | 27.0 | User I/O |
| DB CPU |  | 14,8K |  | 11.4 |  |
| latch: row cache objects | 88,094 | 4319,6 | 49.03 | 3.3 | Concurrency |
| log file sync | 481,915 | 3138,4 | 6.51 | 2.4 | Commit |
| direct path read | 1,346,701 | 2166 | 1.61 | 1.7 | User I/O |
| direct path read temp | 7,730,451 | 2159,2 | 0.28 | 1.7 | User I/O |
| latch: shared pool | 42,117 | 943,4 | 22.40 | .7 | Concurrency |
| cursor: pin S wait on X | 1,580 | 691,7 | 437.81 | .5 | Concurrency |
| library cache: mutex X | 6,807 | 170,7 | 25.08 | .1 | Concurrency |
| latch: cache buffers chains | 2,177 | 43,8 | 20.13 | .0 | Concurrency |


Tutte le istruzioni SQL in tabella sono molto simili, effetto dell’errato binding delle variabili.
Proprio come nel test precedente.

Tabella 18: Istruzioni SQL con i tempi di risposta maggiori
| Elapsed Time (s) | Executions | Elapsed Time per Exec (s) | %Total | %CPU | %IO | SQL Id | SQL Module | SQL Text |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 5,844.57 | 189 | 30.92 | 4.51 | 9.55 | 38.08 | 4k0t94xwxyubm | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 5,723.71 | 186 | 30.77 | 4.42 | 9.60 | 37.95 | cyp92py4wxpz0 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 5,692.61 | 187 | 30.44 | 4.40 | 9.67 | 38.35 | 203vwndv2n974 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 5,299.14 | 176 | 30.11 | 4.09 | 9.78 | 38.13 | 4dc1xabckf67v | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 5,239.88 | 172 | 30.46 | 4.05 | 9.67 | 37.70 | a9rqy8nahghmy | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 5,053.63 | 176 | 28.71 | 3.90 | 10.14 | 38.36 | 72vth0ghu7rdg | JDBC Thin Client | SELECT COUNT(*) NUM FROM ( SEL... |
| 4,881.79 | 172 | 28.38 | 3.77 | 10.31 | 38.32 | 45s6ah4bhak7d | JDBC Thin Client | SELECT COUNT(*) NUM FROM ( SEL... |
| 3,196.53 | 97 | 32.95 | 2.47 | 9.07 | 38.27 | 5tvc04xwszh7c | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 3,036.51 | 95 | 31.96 | 2.35 | 9.27 | 38.41 | 4x8vwt5funyf3 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 2,923.58 | 93 | 31.44 | 2.26 | 9.44 | 38.25 | 3jx8z516n6t54 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 2,916.14 | 92 | 31.70 | 2.25 | 9.35 | 38.22 | 9j9bx7kazvg7q | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 2,690.97 | 86 | 31.29 | 2.08 | 9.46 | 37.88 | 59wkz50fxrv4y | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 2,683.46 | 87 | 30.84 | 2.07 | 9.59 | 38.53 | 2k6ba798xmj9h | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 2,636.79 | 86 | 30.66 | 2.04 | 9.59 | 38.44 | 5fxqm4z1q4ym4 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 2,439.42 | 81 | 30.12 | 1.88 | 9.81 | 38.61 | 4qx8u6vdb731t | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 2,437.47 | 80 | 30.47 | 1.88 | 9.70 | 37.99 | affrxkrq0h4ba | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 2,432.57 | 80 | 30.41 | 1.88 | 9.70 | 38.15 | bxa49q64h4p3u | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 2,354.45 | 79 | 29.80 | 1.82 | 9.95 | 38.29 | 82jzsgyr9nxnz | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 2,210.00 | 74 | 29.86 | 1.71 | 9.90 | 37.76 | d3y6uwgqs1wbs | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,885.09 | 67 | 28.14 | 1.46 | 10.42 | 38.10 | frv53z7tapkvy | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |

Osservando il comportamento del sistema operativo in questo lancio, il database server non mostra segni di sofferenza: né la CPU ha mai raggiunto il 100% nè il carico di lavoro ha superato la soglia oltre la quale i tempi di risposta si allungano in modo non lineare. Infatti, come mostra la tabella seguente contenente i dati estratti nella fase più onerosa che il sistema ha sopportato durante il lancio, i parametri salienti sono tutti nei limiti.

Tabella 19: Consumo delle risorse hardware rilevate con il comando TOP
| top - 11:00:54 up 52 days, 21:13,  2 users,  load average: 0.69, 1.19, 16.18
Tasks: 989 total,   2 running, 987 sleeping,   0 stopped,   0 zombie
Cpu(s):  2.2%us,  0.7%sy,  0.0%ni, 96.8%id,  0.3%wa,  0.0%hi,  0.0%si,  0.0%st
Mem:  24608844k total, 24159948k used,   448896k free,    37792k buffers
Swap: 16650232k total,   459460k used, 16190772k free, 17241400k cached |
| --- |
| top - 11:01:54 up 52 days, 21:14,  2 users,  load average: 3.93, 1.83, 15.45
Tasks: 988 total,   1 running, 987 sleeping,   0 stopped,   0 zombie
Cpu(s): 10.7%us,  4.3%sy,  0.0%ni, 83.4%id,  1.4%wa,  0.0%hi,  0.1%si,  0.0%st
Mem:  24608844k total, 24221196k used,   387648k free,    38072k buffers
Swap: 16650232k total,   459460k used, 16190772k free, 17280416k cached |
| top - 11:02:55 up 52 days, 21:15,  2 users,  load average: 1.87, 1.63, 14.53
Tasks: 988 total,   1 running, 987 sleeping,   0 stopped,   0 zombie
Cpu(s):  2.0%us,  0.8%sy,  0.0%ni, 97.0%id,  0.2%wa,  0.0%hi,  0.0%si,  0.0%st
Mem:  24608844k total, 24265340k used,   343504k free,    38392k buffers
Swap: 16650232k total,   459460k used, 16190772k free, 17315600k cached |
| top - 11:03:54 up 52 days, 21:16,  2 users,  load average: 1.06, 1.45, 13.65
Tasks: 988 total,   4 running, 984 sleeping,   0 stopped,   0 zombie
Cpu(s):  4.1%us,  1.2%sy,  0.0%ni, 94.5%id,  0.2%wa,  0.0%hi,  0.0%si,  0.0%st
Mem:  24608844k total, 24320708k used,   288136k free,    38712k buffers
Swap: 16650232k total,   459460k used, 16190772k free, 17344284k cached |


## Test n°7: 110 utenti Distrettuali e 500 Avvocati per un intervallo di 2 ore
## Sistema Centrale
Tempo di risposta medio:


Utenti concorrenti:

Latenza:


Throughput:


Statistiche:
| Requests | Executions | Executions | Executions | Time |
| --- | --- | --- | --- | --- |
| Label | #Samples | KO | Error % | Average |
| Total | 90942 | 929 | 1.02% | 20172.23 |
| 1 /PST/SIUS/login | 13708 | 73 | 0.53% | 185.38 |
| 67 /PST/SIUS/j_spring_security_check;jsessionid= | 13708 | 89 | 0.65% | 215.85 |
| 114 /PST/SIUS/ricerca/procedimenti/exec | 13559 | 316 | 2.33% | 39027.58 |
| 119 /PST/SIUS/ricerca/procedimenti/dettaglio | 5333 | 24 | 0.45% | 83317.40 |
| 120 /PST/SIUS/ricerca/procedimenti/exec | 5243 | 26 | 0.50% | 46946.04 |
| 121 /PST/SIUS/ricerca/procedimenti/dettaglio | 6427 | 22 | 0.34% | 43209.30 |
| 122 /PST/SIUS/ricerca/procedimenti/exec | 6352 | 61 | 0.96% | 41833.78 |
| 124 /PST/SIUS/ricerca/soggetti | 13224 | 162 | 1.23% | 4314.32 |
| 177 /PST/SIUS/j_spring_security_logout | 13208 | 156 | 1.18% | 467.50 |
| Accesso dati soggetto | 13231 | 162 | 1.22% | 4318.66 |
| Dettaglio decreto | 6446 | 22 | 0.34% | 43138.70 |
| Dettaglio ordinanza | 5346 | 24 | 0.45% | 83215.82 |
| Landing login | 13708 | 73 | 0.53% | 185.38 |
| Login | 13708 | 89 | 0.65% | 215.85 |
| Logout | 13208 | 156 | 1.18% | 467.50 |
| Ricerca estremi procedimenti | 25187 | 403 | 1.60% | 41347.81 |


## Sistema Distrettuale
Tempo di risposta medio:


Utenti concorrenti:


Latenza:


Throughput:


Statistiche:
| Requests | Executions | Executions | Executions | Time |
| --- | --- | --- | --- | --- |
| Label | #Samples | KO | Error % | Average |
| Total | 5571632 | 293006 | 5.26% | 58.58 |
| 1 / | 292821 | 0 | 0.00% | 2.14 |
| 1 /jsp/Main.jsp | 16219 | 0 | 0.00% | 143.06 |
| 4 /jsp/Main.jsp | 1676 | 0 | 0.00% | 6.05 |
| 4 /login.jsp | 8272 | 0 | 0.00% | 2.29 |
| 5 /jsp/Main.jsp | 13140 | 0 | 0.00% | 146.02 |
| 6 /jsp/Main.jsp | 1675 | 29 | 1.73% | 88.35 |
| 9 /jsp/Main.jsp | 292818 | 0 | 0.00% | 40.67 |
| 10 /frame.htm | 292818 | 0 | 0.00% | 1.09 |
| 11 /jsp/files/logo.jsp | 292817 | 0 | 0.00% | 1.04 |
| 11 /jsp/Main.jsp | 8272 | 0 | 0.00% | 47.28 |
| 12 /frame.htm | 8272 | 0 | 0.00% | 1.12 |
| 12 /jsp/files/up.jsp | 292817 | 0 | 0.00% | 1.14 |
| 12 /jsp/Main.jsp | 1009 | 0 | 0.00% | 13.14 |
| 13 /jsp/files/logo.jsp | 8272 | 0 | 0.00% | 1.11 |
| 13 /jsp/files/menu.jsp | 292817 | 0 | 0.00% | 1.32 |
| 13 /jsp/Main.jsp | 1646 | 651 | 39.55% | 330.77 |
| 14 /jsp/files/content_frame.jsp | 292817 | 0 | 0.00% | 1.02 |
| 14 /jsp/files/up.jsp | 8272 | 0 | 0.00% | 1.11 |
| 15 /jsp/files/menu.jsp | 8272 | 0 | 0.00% | 1.25 |
| 15 /jsp/Main.jsp | 1009 | 1009 | 100.00% | 40.05 |
| 16 /jsp/files/content_frame.jsp | 8272 | 0 | 0.00% | 1.09 |
| 22 /html/blank.htm | 8272 | 0 | 0.00% | 1.02 |
| 23 /html/blank.htm | 292817 | 0 | 0.00% | 1.01 |
| 23 /jsp/Main.jsp | 12131 | 12131 | 100.00% | 586.88 |
| 24 /html/blankGray.htm | 292816 | 0 | 0.00% | 1.02 |
| 25 /jsp/files/fastAccessMenu.jsp | 292816 | 0 | 0.00% | 1.35 |
| 28 /jsp/files/fastAccessMenu.jsp | 8272 | 0 | 0.00% | 1.32 |
| 29 /html/blankGray.htm | 8272 | 0 | 0.00% | 1.00 |
| 35 /jsp/Main.jsp | 894 | 1 | 0.11% | 93.93 |
| 43 /jsp/Main.jsp | 8272 | 0 | 0.00% | 5.85 |
| 44 /jsp/Main.jsp | 736 | 0 | 0.00% | 181.38 |
| 45 /jsp/Main.jsp | 6800 | 0 | 0.00% | 8394.00 |
| 47 /jsp/Main.jsp | 8272 | 0 | 0.00% | 5.50 |
| 49 /jsp/Main.jsp | 8272 | 0 | 0.00% | 24.86 |
| 51 /jsp/Main.jsp | 6790 | 0 | 0.00% | 546.51 |
| 55 /jsp/Main.jsp | 414 | 0 | 0.00% | 6641.98 |
| 56 /jsp/Main.jsp | 8272 | 0 | 0.00% | 6525.34 |
| 57 /jsp/Main.jsp | 6790 | 0 | 0.00% | 283.01 |
| 62 /jsp/Main.jsp | 8264 | 0 | 0.00% | 272.05 |
| 64 /jsp/Main.jsp | 1091 | 0 | 0.00% | 32.16 |
| 67 /jsp/Main.jsp | 1090 | 16 | 1.47% | 31.52 |
| 68 /jsp/files/siap/sico/Calendario.jsp | 8264 | 0 | 0.00% | 2.23 |
| 68 /jsp/Main.jsp | 1073 | 0 | 0.00% | 103.01 |
| 72 /jsp/Main.jsp | 8264 | 0 | 0.00% | 17.95 |
| 74 /jsp/Main.jsp | 1073 | 64 | 5.96% | 1055.91 |
| 75 /html/blank.htm | 8264 | 0 | 0.00% | 1.24 |
| 76 /jsp/Main.jsp | 8264 | 0 | 0.00% | 16.61 |
| 79 /jsp/Main.jsp | 16243 | 0 | 0.00% | 45.15 |
| 82 /jsp/Main.jsp | 8264 | 144 | 1.74% | 668.21 |
| 86 /jsp/Main.jsp | 267 | 0 | 0.00% | 33.19 |
| 89 /jsp/Main.jsp | 267 | 0 | 0.00% | 47.25 |
| 91 /jsp/Main.jsp | 267 | 0 | 0.00% | 55.93 |
| 92 /jsp/Main.jsp | 8118 | 0 | 0.00% | 36.66 |
| 97 /jsp/Main.jsp | 260 | 31 | 11.92% | 1569.25 |
| 101 /jsp/Main.jsp | 8118 | 0 | 0.00% | 16.42 |
| 104 /jsp/Main.jsp | 8118 | 0 | 0.00% | 26.01 |
| 107 /jsp/Main.jsp | 8118 | 8118 | 100.00% | 16.49 |
| 119 /jsp/Main.jsp | 274943 | 0 | 0.00% | 5.29 |
| 121 /jsp/Main.jsp | 274943 | 0 | 0.00% | 14.55 |
| 122 /jsp/Main.jsp | 229 | 229 | 100.00% | 72.67 |
| 125 /jsp/Main.jsp | 238515 | 0 | 0.00% | 28.92 |
| 130 /jsp/Main.jsp | 238515 | 159009 | 66.67% | 58.15 |
| 133 /jsp/Main.jsp | 79504 | 0 | 0.00% | 49.91 |
| 144 /jsp/Main.jsp | 6790 | 0 | 0.00% | 21.82 |
| 147 /jsp/Main.jsp | 6790 | 6790 | 100.00% | 58.10 |
| 186 /jsp/Main.jsp | 36428 | 0 | 0.00% | 28.45 |
| 191 /jsp/Main.jsp | 36428 | 24287 | 66.67% | 1381.85 |
| 205 /jsp/Main.jsp | 995 | 995 | 100.00% | 397.93 |
| 227 /jsp/Main.jsp | 13177 | 0 | 0.00% | 5.73 |
| 231 /jsp/Main.jsp | 13177 | 0 | 0.00% | 5.42 |
| 233 /jsp/Main.jsp | 13177 | 0 | 0.00% | 30.82 |
| 240 /jsp/Main.jsp | 6377 | 0 | 0.00% | 9845.35 |
| 441 /jsp/Main.jsp | 79502 | 0 | 0.00% | 22.95 |
| 445 /jsp/Main.jsp | 79502 | 0 | 0.00% | 14.10 |
| 449 /jsp/Main.jsp | 79502 | 0 | 0.00% | 21.30 |
| 454 /jsp/Main.jsp | 79502 | 0 | 0.00% | 16.44 |
| 460 /jsp/Main.jsp | 79502 | 0 | 0.00% | 13.52 |
| 464 /jsp/files/siap/sico/cssa/FiltraCssaLista.jsp | 79502 | 0 | 0.00% | 1.23 |
| 469 /jsp/Main.jsp | 79502 | 0 | 0.00% | 23.93 |
| 472 /jsp/Main.jsp | 79502 | 0 | 0.00% | 25.53 |
| 476 /jsp/Main.jsp | 79502 | 0 | 0.00% | 23.25 |
| 480 /jsp/Main.jsp | 79502 | 0 | 0.00% | 14.01 |
| 484 /jsp/Main.jsp | 79502 | 0 | 0.00% | 22.50 |
| 492 /jsp/Main.jsp | 79502 | 0 | 0.00% | 13.80 |
| 495 /jsp/Main.jsp | 79502 | 0 | 0.00% | 41.83 |
| 500 /jsp/Main.jsp | 79502 | 79502 | 100.00% | 15.31 |
| cerca autorita competente | 79502 | 0 | 0.00% | 92.14 |
| cerca istituto di detenzione | 79502 | 0 | 0.00% | 35.40 |
| cerca sede uepe | 79502 | 0 | 0.00% | 38.67 |
| cerca UDS | 79502 | 0 | 0.00% | 48.78 |
| click calcola data fine pena | 12131 | 12131 | 100.00% | 588.14 |
| click calendario | 8264 | 0 | 0.00% | 2.23 |
| click concessione | 79504 | 0 | 0.00% | 49.91 |
| click decisioni di sorveglianza | 274943 | 0 | 0.00% | 19.85 |
| click iscrizione manuale | 21449 | 0 | 0.00% | 5.77 |
| click iscrizione procedimento | 8264 | 0 | 0.00% | 272.05 |
| click liberazione anticipata | 36428 | 0 | 0.00% | 28.45 |
| click lista oggetto | 6790 | 0 | 0.00% | 21.82 |
| click magistrato | 8264 | 0 | 0.00% | 60.57 |
| click oggetti | 8118 | 0 | 0.00% | 36.66 |
| click ordine di esecuzione | 1090 | 16 | 1.47% | 132.93 |
| click ricerca procedimento per numero | 8272 | 0 | 0.00% | 30.36 |
| click ricerca titolo per numero | 13177 | 0 | 0.00% | 36.24 |
| click scegli TDS | 79502 | 0 | 0.00% | 22.95 |
| click scelta oggetto | 8118 | 0 | 0.00% | 16.42 |
| click sede | 12131 | 0 | 0.00% | 63.79 |
| click semiliberta | 238515 | 0 | 0.00% | 28.92 |
| click su ordine di esecuzione | 1676 | 29 | 1.73% | 94.35 |
| click su ordini di esecuzione-scarcerazione | 2783 | 0 | 0.00% | 28.87 |
| click su ricerca | 420 | 0 | 0.00% | 6547.09 |
| click su sospensione esecuzione 656 cpp | 1091 | 0 | 0.00% | 32.16 |
| click titolo esecutivo | 8118 | 0 | 0.00% | 26.01 |
| conferma concessione semiliberta | 79502 | 79502 | 100.00% | 15.48 |
| conferma inserimento | 8264 | 144 | 1.74% | 668.22 |
| conferma liberazione | 12131 | 0 | 0.00% | 156.17 |
| conferma oggetto | 8118 | 8118 | 100.00% | 16.70 |
| conferma ordine esecuzione | 995 | 995 | 100.00% | 399.48 |
| conferma sospensione | 229 | 229 | 100.00% | 72.86 |
| dettaglio procedimento | 6790 | 0 | 0.00% | 546.51 |
| filtra istituto di detenzione | 79502 | 0 | 0.00% | 16.44 |
| home page | 301093 | 0 | 0.00% | 2.14 |
| iscrizione procedimento | 6790 | 0 | 0.00% | 283.01 |
| login | 301090 | 0 | 0.00% | 49.85 |
| logout | 7985 | 0 | 0.00% | 66.21 |
| pagina ricerca per soggetto | 901 | 1 | 0.11% | 93.20 |
| ricerca avanzata | 316 | 0 | 0.00% | 4473.69 |
| ricerca procedimento | 286943 | 184042 | 64.14% | 419.76 |
| ricerca singolo procedimento | 13177 | 0 | 0.00% | 9096.38 |
| salva iscrizione procedimento | 6790 | 6790 | 100.00% | 58.51 |
| scelta sede | 1009 | 1009 | 100.00% | 129.30 |
| sospensione/revoca | 267 | 0 | 0.00% | 103.19 |
| sospensioni/interruzioni del PM | 270 | 0 | 0.00% | 32.82 |


## Database
In questo test si sperimenta al secondo posto il tempo di attesa “direct path write temp”, al primo si trova il tempo speso per accedere alla CPU.

Tabella 20: Tempi di attesa (Wait Times)
| Event | Waits | Total Wait Time (sec) | Wait Avg(ms) | % DB time | Wait Class |
| --- | --- | --- | --- | --- | --- |
| DB CPU |  | 44,7K |  | 39.2 |  |
| direct path write temp | 8,824,497 | 23K | 2.61 | 20.2 | User I/O |
| log file sync | 1,425,800 | 6145,7 | 4.31 | 5.4 | Commit |
| latch: row cache objects | 798,864 | 4175,4 | 5.23 | 3.7 | Concurrency |
| direct path read | 3,548,852 | 2212,6 | 0.62 | 1.9 | User I/O |
| latch: shared pool | 618,441 | 1562,8 | 2.53 | 1.4 | Concurrency |
| library cache: mutex X | 105,366 | 747,3 | 7.09 | .7 | Concurrency |
| direct path read temp | 9,436,613 | 504,8 | 0.05 | .4 | User I/O |
| enq: KO - fast object checkpoint | 2,284 | 226,4 | 99.12 | .2 | Application |
| db file sequential read | 150,900 | 88 | 0.58 | .1 | User I/O |


Tutte le istruzioni SQL in tabella sono molto simili, effetto dell’errato binding delle variabili.

Tabella 21: Istruzioni SQL con i tempi di risposta maggiori
| Elapsed Time (s) | Executions | Elapsed Time per Exec (s) | %Total | %CPU | %IO | SQL Id | SQL Module | SQL Text |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 3,653.38 | 541 | 6.75 | 3.20 | 36.89 | 39.18 | a9rqy8nahghmy | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 3,650.52 | 542 | 6.74 | 3.20 | 37.02 | 39.02 | 72vth0ghu7rdg | JDBC Thin Client | SELECT COUNT(*) NUM FROM ( SEL... |
| 3,638.34 | 541 | 6.73 | 3.19 | 37.04 | 38.47 | 4k0t94xwxyubm | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 3,626.12 | 542 | 6.69 | 3.18 | 37.29 | 38.80 | 45s6ah4bhak7d | JDBC Thin Client | SELECT COUNT(*) NUM FROM ( SEL... |
| 3,617.11 | 541 | 6.69 | 3.17 | 37.18 | 38.89 | 4dc1xabckf67v | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 3,601.80 | 541 | 6.66 | 3.16 | 37.38 | 38.30 | cyp92py4wxpz0 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 3,599.35 | 541 | 6.65 | 3.16 | 37.40 | 38.47 | 203vwndv2n974 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 2,563.62 | 9,776 | 0.26 | 2.25 | 38.67 | 34.87 | 6qk3tkcw4rzaq | JDBC Thin Client | BEGIN AVVOCATURA_SIUS.CERCA_FA... |
| 1,746.99 | 257 | 6.80 | 1.53 | 36.61 | 38.95 | 4x8vwt5funyf3 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,738.70 | 257 | 6.77 | 1.52 | 36.84 | 39.07 | 9j9bx7kazvg7q | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,738.53 | 257 | 6.76 | 1.52 | 36.82 | 39.18 | d3y6uwgqs1wbs | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,736.25 | 257 | 6.76 | 1.52 | 36.84 | 38.48 | 2k6ba798xmj9h | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,718.56 | 257 | 6.69 | 1.51 | 37.18 | 38.84 | 3jx8z516n6t54 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,717.14 | 256 | 6.71 | 1.51 | 37.21 | 38.32 | affrxkrq0h4ba | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,715.97 | 257 | 6.68 | 1.50 | 37.18 | 38.61 | 4qx8u6vdb731t | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,715.41 | 257 | 6.67 | 1.50 | 37.16 | 39.02 | 59wkz50fxrv4y | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,713.05 | 257 | 6.67 | 1.50 | 37.32 | 37.42 | 82jzsgyr9nxnz | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,706.92 | 256 | 6.67 | 1.50 | 37.23 | 38.10 | bxa49q64h4p3u | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,704.79 | 256 | 6.66 | 1.50 | 37.34 | 37.38 | 5tvc04xwszh7c | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,699.45 | 257 | 6.61 | 1.49 | 37.63 | 37.88 | frv53z7tapkvy | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |
| 1,599.80 | 239 | 6.69 | 1.40 | 37.17 | 38.37 | 5fxqm4z1q4ym4 | JDBC Thin Client | SELECT * FROM (SELECT INNER.* ... |

Osservando il comportamento del sistema operativo in questo lancio, il database server mostra segni di sofferenza: la CPU non raggiunge il 100% di utilizzo e il carico di lavoro supera di gran lungo la soglia oltre la quale i tempi di risposta non aumentano più in modo lineare. Infatti, come mostra la tabella seguente contenente i dati estratti nella fase più onerosa che il sistema ha sopportato durante il lancio, il load avarage sale considerevolmente in proporzione all’aumentato numero di Tasks.

Tabella 22: Consumo delle risorse hardware rilevate con il comando TOP
| top - 15:46:05 up 53 days,  1:58,  2 users,  load average: 44.66, 43.04, 42.53
Tasks: 688 total,  39 running, 649 sleeping,   0 stopped,   0 zombie
Cpu(s): 90.9%us,  7.0%sy,  0.0%ni,  0.2%id,  0.2%wa,  0.0%hi,  1.7%si,  0.0%st
Mem:  24608844k total, 24190080k used,   418764k free,   156644k buffers
Swap: 16650232k total,   464296k used, 16185936k free, 20782428k cached |
| --- |
| top - 15:47:04 up 53 days,  1:59,  2 users,  load average: 46.35, 43.85, 42.84
Tasks: 688 total,  44 running, 644 sleeping,   0 stopped,   0 zombie
Cpu(s): 89.0%us,  8.4%sy,  0.0%ni,  0.1%id,  0.9%wa,  0.0%hi,  1.7%si,  0.0%st
Mem:  24608844k total, 24235592k used,   373252k free,   157032k buffers
Swap: 16650232k total,   464388k used, 16185844k free, 20746436k cached |
| top - 15:48:05 up 53 days,  2:00,  2 users,  load average: 43.13, 43.42, 42.76
Tasks: 688 total,  44 running, 644 sleeping,   0 stopped,   0 zombie
Cpu(s): 91.4%us,  7.1%sy,  0.0%ni,  0.0%id,  0.0%wa,  0.0%hi,  1.4%si,  0.0%st
Mem:  24608844k total, 24133896k used,   474948k free,   157644k buffers
Swap: 16650232k total,   464388k used, 16185844k free, 20760792k cached |
| top - 15:49:04 up 53 days,  2:01,  2 users,  load average: 20.11, 37.22, 40.70
Tasks: 688 total,   1 running, 687 sleeping,   0 stopped,   0 zombie
Cpu(s):  0.2%us,  0.1%sy,  0.0%ni, 99.8%id,  0.0%wa,  0.0%hi,  0.0%si,  0.0%st
Mem:  24608844k total, 23797144k used,   811700k free,   158200k buffers
Swap: 16650232k total,   464388k used, 16185844k free, 20765828k cached |







# Conclusioni
Nei test eseguiti dal 30/09/2020 al 5/10/2020 dalle simulazioni effettuate risulta che la frequenza con cui il sistema riesce ad evadere il lavoro pendente è proporzionale alla frequenza con cui le richieste da parte degli utenti fanno ingresso nel sistema solo fino al momento dove vi sono 54 utenti agli uffici del distretto di Napoli più 83 avvocati concorrentemente attivi.

I risultati evidenziano un notevole impatto sul carico di sistema da parte delle richieste degli avvocati; tale aspetto suggerisce di procedere ad un’analisi dell’implementazione delle varie funzioni invocate dalle suddette richieste. Il comportamento del sistema presenta tempi medi di risposta caratterizzati da una crescita lineare con l’aumentare del numero degli utenti concorrenti senza arrivare a un punto di saturazione specifico.

Il sistema centrale:
Senza collegamenti concorrenti degli utenti dal sistema distrettuale regge almeno 1000 utenti senza saturarsi.
Con 59 utenti concorrenti collegati, il sistema già presenta tempi di risposta non accettabili (che crescono velocemente dal minuto ai 4 minuti di attesa) in quasi tutti i suoi processi. In particolare, il sistema centrale con solo 100 utenti concorrenti presenta già problemi serissimi di performance con il processo della stampa del procedimento.

Il sistema distrettuale:
Senza collegamenti concorrenti degli utenti dal sistema centrale regge almeno 550 utenti senza saturarsi, con tempi di risposta sempre inferiori al minuto tranne per la ricerca soggetto.
Con 99 utenti concorrenti collegati, la ricerca soggetto ha già tempi di risposta superiori al minuto. Con 550 utenti, i tempi medi di risposta sono di circa 5 minuti.

Durante il test con il collegamento contemporaneo degli utenti di entrambi sistemi, il sistema Centrale collassa dopo circa un’ora (15:30) di lavoro a carico massimo, quando il fattore di utilizzazione delle risorse fisiche è tale da portare il sistema in condizioni dove non è più in grado di smaltire il crescente numero di richieste in ingresso e si produce una caduta del throughput del sistema.

In contrasto, il sistema Distrettuale presenta tempi di risposta a carico massimo nell’ordine dei 12 secondi non arrivando mai a una situazione di saturazione totale. Il sistema presenta durante il test due cadute del throughput (“singhiozzi”) alle 14:40 e alle 15:40 che, dovuto alla ricorrenza oraria, potrebbero essere vincolati a qualche task in background o processo automatico schedulato nel server.

Più specificamente, si osserva:
Con 110 utenti distrettuali concorrenti con 500 utenti del sistema centrale, il sistema distrettuale funziona “correttamente” con tempi di risposta massimi inferiori a 2 minuti (a eccezione del problema già evidenziato della ricerca soggetto).
Con 500 utenti centrali concorrenti con 110 utenti del sistema distrettuale, il sistema centrale si satura e si “rompe” dopo circa un’ora a carico massimo (cosa che non succede con il sistema distrettuale, che continua a funzionare normalmente).

In sintesi:
Il punto di rottura del sistema centrale si trova fra 50 utenti distrettuali + 50 avvocati e 110 utenti distrettuali + 200 avvocati concorrenti.
Senza gli utenti distrettuali, 1000 avvocati possono lavorare in contemporanea senza saturare il sistema. I tempi crescono linearmente al numero di utenti concorrenti.

Indipendentemente degli avvocati, fino a 550 utenti distrettuali possono lavorare in contemporanea senza saturare il sistema. I tempi crescono linearmente al numero di utenti concorrenti.

Lato Database Server, in particolare, si è osservato che complessivamente tutti gli stress test eseguiti hanno evidenziato due principali criticità nell’esecuzione delle query SQL:
un numero ragguardevole di operazioni di ordinamento dei dati (sort) e di hash join inducendo un elevato carico sulle risorse di IO del database
il mancato utilizzo delle variabili di bind nelle istruzioni SQL, incidendo sul consumo di CPU e sui tempi di attesa (wait time) dei processi nell’eseguirle

Entrambe le criticità diminuiscono la capacità del sistema di assorbire carichi di lavoro maggiori, in quanto le risorse del sistema non sono utilizzate in modo ottimale.

Si suggerisce di procedere ad un’analisi dell’implementazione delle varie funzioni elencate come problematiche nei risultati di sintesi e di valutare possibili interventi atti a ridurne l’impatto in termini di costo computazionale sia sull’Application Server che sul Database Server di SIES-Avvocatura.

La tabella seguente riassume le attività pianificabili per ottimizzare i tempi di risposta delle query SQL pesanti.

Tabella 23: Interventi migliorativi
| Tipo attività | Stima in gg/u | Descrizione |
| --- | --- | --- |
| Studio e tuning delle query onerose | 5 g | Per ogni query onerosa si studia il modo per ottimizzarle: indici nuovi, riscrittura della query, aggiunta di hint per l’ottimizzatore, eliminazione della query |
| Creazione indice | 1 g | Creazione di un nuovo indice nella basedati |
| Riscrittura query | 10 g | Individuazione della query nel codice java e riscrittura della query |
| Eliminazione query | 5 g | Individuazione della query nel codice java, eliminazione della query e contestuale adeguamento di altre query per lasciare inalterato il risultato finale |
| Hint per l’ottimizzatore | 5 g | Individuazione della query nel codice java e aggiunta dell’hint alla query |
| Creazione Foreign Key | 3 g | Creazione di Foreing Key mancanti, a tutto vantaggio dell’integrità del dato e per aiutare l’ottimizzatore nello creazione dei piani di esecuzione delle query |
| Uso delle variabili di bind | Attività molto invadente: da stimare | Su tutta l’applicazione o per la sola parte più usata dagli utenti, riscrivere il codice java affinché tutte le istruzioni SQL inviate al database facciano uso delle variabili di bind |
| Test | 10 g | Verifica sulle attività svolte |