**RISERVATO**

**SIES 2.0**

**STRATEGIA DI EVOLUZIONE INTEGRATA**

Sistema Informativo dell'Esecuzione e della Sorveglianza

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th><strong>Versione rimodulata<br />
</strong>La proposta conserva integralmente le evolutive sul sistema attuale e il modello dei depositi telematici già descritti nella versione precedente. La rimodulazione riguarda la strategia di reingegnerizzazione: SIEP, SIUS e SIGE sono affrontati come unico programma nazionale, con sperimentazione graduale e dismissione dei legacy entro 24 mesi.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

| **Informazione** | **Valore** |
|:---|:---|
| Cliente | Ministero della Giustizia - DIT |
| Oggetto | Evoluzione integrata del SIES |
| Versione | 3.0 - proposta rimodulata |
| Orizzonte massimo | 24 mesi, comprensivi di analisi, sviluppo, sperimentazione, migrazione e go-live |
| Prodotto da | Engineering Ingegneria Informatica S.p.A. |
| Data | 10 settembre 2026 |

# Indice dei contenuti

1\. Scopo del documento

2\. Introduzione

3\. Evolutive Sistema Attuale

3.1 Accesso utenti tramite ADN

3.2 Fogli complementari SIEP - SIC Casellario

3.3 Integrazione Firma digitale remota

3.4 Integrazione con Mercurio archivio ufficiale

4\. Integrazioni sul sistema SIES Attuale - Deposito Difensore

4.1 Deposito Incidente di Esecuzione verso Giudice dell’Esecuzione SIGE

4.2 Deposito verso la Sorveglianza

4.3 Modello Evolutivo dei Depositi Telematici per l’Esecuzione Penale e la Sorveglianza

5\. Rimodulazione richiesta dall’Amministrazione

6\. Visione del nuovo SIES

7\. Assessment e gap analysis integrata

8\. Perimetro funzionale SIEP, SIUS e SIGE

9\. Roadmap integrata di 24 mesi

10\. Migrazione, sperimentazione e dismissione

11\. Portale utenti esterni e Deleghe PG

12\. Quadro economico preliminare

13\. Governance, vincoli e rischi

14\. Conclusioni

# 1. Scopo del documento

Il presente documento ha lo scopo di illustrare in modo unitario la proposta di evoluzione del Sistema Informativo dell'Esecuzione e della Sorveglianza (SIES), fornendo una visione complessiva degli interventi previsti, del relativo percorso attuativo e degli investimenti necessari alla loro realizzazione.

La proposta non si limita alla realizzazione di specifiche evolutive tecnologiche, ma definisce un percorso progressivo di trasformazione finalizzato ad accompagnare l'Amministrazione nella costruzione del futuro ecosistema digitale dell'esecuzione penale e della sorveglianza. In tale contesto, alle attività di sviluppo e reingegnerizzazione si affianca un percorso continuativo di confronto e co-progettazione con i Gruppi di Lavoro individuati dall'Amministrazione, volto a raccogliere, analizzare e prioritizzare esigenze operative e nuovi requisiti funzionali che emergeranno nel corso del programma.

Il documento descrive pertanto:

- gli interventi evolutivi sugli attuali sistemi;

- le integrazioni finalizzate all’ampliamento dei servizi digitali rivolti agli utenti interni ed esterni;

- il percorso di reingegnerizzazione del SIES 2.0 e di evoluzione dei processi operativi;

- l’approccio di attuazione, sperimentazione, migrazione e adozione progressiva da parte degli uffici;

- i vincoli, i rischi e le condizioni abilitanti del programma;

- i principi architetturali e tecnologici di riferimento;

- la roadmap temporale, il quadro economico e i razionali delle stime.

L'obiettivo è consentire all'Amministrazione di disporre di una visione integrata, funzionale ed economica, dell'iniziativa, comprendendo non solo cosa viene realizzato, ma anche le modalità attraverso cui il programma potrà essere progressivamente affinato nel tempo.

# 2. Introduzione

Il Sistema Informativo dell’Esecuzione e della Sorveglianza (SIES) rappresenta il principale asset applicativo del Ministero della Giustizia per la gestione dei procedimenti afferenti all’esecuzione penale e alla magistratura di sorveglianza. Il sistema costituisce un elemento cardine dell’ecosistema digitale della Giustizia, fungendo da piattaforma di riferimento per la gestione delle informazioni, dei procedimenti e dei provvedimenti che intervengono nella fase esecutiva del processo penale.

Il SIES è articolato in tre sottosistemi funzionalmente distinti ma integrati. Il SIEP gestisce il titolo esecutivo e i principali provvedimenti dell’esecuzione penale, quali ordini di esecuzione, ordini di carcerazione e decreti. Il SIUS supporta la Magistratura di Sorveglianza nella trattazione dei procedimenti relativi alle misure alternative alla detenzione, alla liberazione anticipata e ai permessi. Il SIGE è dedicato alla gestione informatizzata delle attività e dei provvedimenti riconducibili alle competenze del Giudice dell’Esecuzione.

Nel contesto dell’evoluzione digitale della Giustizia, il SIES è chiamato a trasformarsi da sistema orientato alla gestione dei singoli registri applicativi a piattaforma integrata dell’esecuzione penale e della sorveglianza, in grado di connettere i sistemi della cognizione penale, il Casellario Giudiziale, il DAP, gli istituti penitenziari, il SIEPE, gli UEPE, il sistema documentale ministeriale e i servizi telematici rivolti a difensori e cittadini, assicurando continuità del dato e digitalizzazione dell’intero ciclo esecutivo.

Il programma conserva tre direttrici coordinate: evolutive sul sistema attuale; integrazioni e depositi telematici; reingegnerizzazione dell’intero ecosistema SIES. Le prime due direttrici restano valide nella formulazione della proposta precedente. La terza viene rimodulata sulla base dell’indirizzo dell’Amministrazione, superando la sequenza centrata inizialmente sul SIUS e assumendo SIEP, SIUS e SIGE come unico programma evolutivo.

# 3. Evolutive Sistema Attuale

Le evolutive sul sistema SIES attualmente in esercizio rappresentano il primo passaggio della roadmap di trasformazione. Introducono funzionalità strategiche, rafforzano l’interoperabilità con i sistemi ministeriali e creano condizioni tecniche e operative per il percorso di reingegnerizzazione. Tali interventi non sono eliminati dalla nuova impostazione e restano parte del programma.

## 3.1 Accesso utenti tramite ADN

L'intervento di Accesso utenti tramite ADN (Autenticazione Digitale Nazionale) è finalizzato ad adeguare il SIES agli standard e ai requisiti di sicurezza definiti dal Ministero della Giustizia per la gestione delle identità digitali e dei meccanismi di autenticazione. L'iniziativa si inserisce nel più ampio percorso di razionalizzazione e uniformazione dell'accesso ai servizi digitali dell'Amministrazione, garantendo maggiore controllo, tracciabilità e conformità alle politiche di sicurezza adottate a livello ministeriale.

L'obiettivo dell'iniziativa è consentire l'accesso al SIES attraverso il sistema ADN, introducendo un modello di autenticazione centralizzato, sicuro e omogeneo rispetto agli altri applicativi dell'ecosistema Giustizia. Tale evoluzione permette di superare logiche di gestione locale delle credenziali, favorendo una governance unificata delle identità digitali e una migliore integrazione con i servizi di sicurezza istituzionali.

Dal punto di vista applicativo, la MEV prevede l'adeguamento dei componenti di accesso del SIES per supportare i protocolli di autenticazione messi a disposizione da ADN, la gestione del Single Sign-On (SSO) e l'associazione automatica degli utenti autenticati ai relativi profili applicativi e autorizzativi presenti nel sistema.

**Benefici attesi**

- Uniformazione delle modalità di autenticazione agli standard ministeriali;

- Introduzione del Single Sign-On per gli utenti SIES;

- Rafforzamento dei livelli di sicurezza e tracciabilità degli accessi;

- Riduzione delle attività amministrative legate alla gestione delle utenze;

- Allineamento architetturale alle future iniziative di reingegnerizzazione del SIES;

- Maggiore interoperabilità con le piattaforme e i servizi digitali del Ministero della Giustizia.

## 3.2 Fogli complementari SIEP - SIC Casellario

L'intervento “Fogli Complementari SIEP - SIC Casellario” è finalizzato al rafforzamento dell'integrazione applicativa tra il Sistema Informativo dell'Esecuzione Penale (SIEP) e il Sistema Informativo del Casellario (SIC), con l'obiettivo di garantire una gestione più efficiente, tempestiva e coerente delle informazioni relative all'esecuzione penale e agli adempimenti di competenza del Casellario Giudiziale.

La MEV prevede la digitalizzazione e l'automazione dei flussi informativi connessi alla produzione, trasmissione e aggiornamento dei fogli complementari. L'intervento consentirà di ridurre le attività manuali di inserimento e verifica dei dati, limitare il rischio di disallineamenti informativi tra i sistemi e incrementare la qualità complessiva del patrimonio informativo gestito dall'Amministrazione.

Dal punto di vista funzionale, l'evoluzione introduce meccanismi di interoperabilità finalizzati alla trasmissione strutturata delle informazioni generate nell'ambito dei procedimenti di esecuzione penale. Oltre ai benefici operativi immediati, l'intervento anticipa i principi della futura architettura, basata su interoperabilità, unicità dell'informazione e integrazione nativa tra i sistemi della Giustizia.

**Benefici attesi**

- Maggiore integrazione tra SIEP e Sistema Informativo del Casellario;

- Riduzione delle attività manuali di produzione e gestione dei fogli complementari;

- Miglioramento della qualità e della coerenza dei dati condivisi;

- Riduzione dei tempi di aggiornamento delle informazioni;

- Diminuzione delle anomalie derivanti da duplicazioni o disallineamenti;

- Creazione delle basi funzionali e tecnologiche per la reingegnerizzazione del SIES.

## 3.3 Integrazione Firma digitale remota

L’integrazione della firma digitale remota all’interno del sistema SIES rappresenta un passaggio strategico nel percorso di digitalizzazione dei processi della giustizia penale. La soluzione consente la sottoscrizione elettronica qualificata di provvedimenti, verbali, decreti e altri atti direttamente all’interno del workflow applicativo, eliminando la necessità di procedure esterne, dispositivi fisici o operazioni manuali di caricamento e firma.

Dal punto di vista operativo, il documento generato in SIES viene inviato a un servizio centralizzato di firma remota qualificata. Una volta completata la sottoscrizione, il documento firmato viene automaticamente archiviato nel sistema documentale ufficiale dell’Amministrazione, garantendone conservazione, tracciabilità, integrità e reperibilità nel tempo.

Il SIES assume il ruolo di orchestratore dell’intero ciclo di firma digitale, dalla richiesta di sottoscrizione fino alla ricezione dell’esito e all’archiviazione del documento firmato, garantendo evidenza certa e verificabile delle operazioni effettuate e preservando autenticità, integrità, immodificabilità e opponibilità a terzi.

## 3.4 Integrazione con Mercurio archivio ufficiale

L'integrazione con il sistema documentale Mercurio consente di estendere il modello di gestione digitale già adottato dall'Amministrazione, garantendo la continuità del ciclo documentale dalla formazione dell'atto fino alla sua archiviazione e conservazione. L’obiettivo è superare la conservazione locale dei documenti, introducendo un repository documentale unico e istituzionale.

Ogni documento generato o acquisito all’interno di SIES viene trasmesso a Mercurio attraverso servizi di integrazione dedicati. Il sistema documentale provvede all’archiviazione, all’attribuzione di un identificativo univoco e alla gestione del ciclo di vita documentale. Tale identificativo viene registrato in SIES, consentendo agli operatori di richiamare il documento originale senza conservarne copie ridondanti nelle basi dati applicative.

L’integrazione assume ulteriore valore se associata ai servizi di firma digitale remota, consentendo un processo completamente dematerializzato: il documento viene generato da SIES, firmato digitalmente tramite i servizi centrali e immediatamente archiviato in Mercurio.

# 4. Integrazioni sul sistema SIES Attuale - Deposito Difensore

Le integrazioni sul sistema SIES attuale, con particolare riferimento al Deposito Difensore, rappresentano un passaggio intermedio della roadmap: estendono l’operatività digitale dei procedimenti, semplificano l’interazione tra difensori e uffici giudiziari e preparano componenti riutilizzabili nella futura architettura.

## 4.1 Deposito Incidente di Esecuzione verso Giudice dell’Esecuzione SIGE

L’intervento evolutivo “Deposito dell’Incidente di Esecuzione verso il Giudice dell’Esecuzione” è finalizzato alla digitalizzazione completa delle modalità di trasmissione e gestione delle istanze presentate dai difensori nell’ambito dei procedimenti di competenza del Giudice dell’Esecuzione (SIGE). L’iniziativa si inserisce nel più ampio percorso di modernizzazione del sistema SIES e di progressiva estensione dei servizi telematici rivolti agli operatori della giustizia.

L’evoluzione prevede l’integrazione del Deposito Difensore con il dominio applicativo del Giudice dell’Esecuzione, consentendo la trasmissione telematica delle istanze e della documentazione allegata direttamente nei flussi digitali gestiti dal sistema. Le richieste potranno essere instradate verso il procedimento competente, rese disponibili agli uffici e associate alle informazioni presenti nel fascicolo digitale.

Ogni deposito sarà acquisito, protocollato, classificato e reso disponibile agli operatori autorizzati secondo le regole organizzative e procedurali definite dall’Amministrazione. Il canale digitale integrato migliora il monitoraggio dello stato delle istanze, la tracciabilità e la qualità delle informazioni.

## 4.2 Deposito verso la Sorveglianza

L’intervento “Deposito verso la Sorveglianza” è finalizzato all’estensione dei servizi di deposito telematico agli atti e alle istanze destinati agli Uffici e ai Tribunali di Sorveglianza, nell’ambito della digitalizzazione del SIUS e dei procedimenti di competenza della Magistratura di Sorveglianza.

L’obiettivo è consentire ai difensori di trasmettere in modalità completamente digitale le istanze relative a misure alternative alla detenzione, permessi, licenze, pene sostitutive, reclami, ricorsi e ulteriori richieste previste dall’ordinamento, integrando tali flussi nei processi applicativi gestiti dal sistema.

Gli atti depositati vengono classificati, instradati verso l’ufficio competente e resi disponibili ai magistrati e al personale di cancelleria, favorendo la costituzione di un fascicolo digitale e riducendo le attività manuali di protocollazione, registrazione e smistamento.

## 4.3 Modello Evolutivo dei Depositi Telematici per l’Esecuzione Penale e la Sorveglianza

### 4.3.1 Premessa

La proposta non prevede una mera estensione delle funzionalità oggi disponibili sulla Piattaforma Digitale Processuale (PDP), ma introduce un modello specialistico progettato per le specificità dell'esecuzione penale e della sorveglianza. L'attuale modello di deposito del PDP è infatti orientato ai procedimenti della cognizione penale e alle relative logiche autorizzative, basate sulla presenza del procedimento nei registri di riferimento e sulla gestione di atti processuali tipizzati.

L'ambito dell'esecuzione penale e della sorveglianza presenta caratteristiche differenti: il procedimento può svilupparsi successivamente al passaggio in giudicato, coinvolge attori diversi e richiede la gestione di istanze, richieste e flussi operativi non sempre riconducibili ai modelli della cognizione. Per tale ragione si propone un componente specialistico dedicato, capace di evolvere e accompagnare il percorso di trasformazione del SIES.

### 4.3.2 Un componente specialistico per il deposito digitale

Il modello prevede la realizzazione di un servizio dedicato alla gestione dei depositi, delle istanze e delle comunicazioni digitali afferenti all'esecuzione penale e alla sorveglianza. Il componente viene progettato come elemento autonomo e riutilizzabile, integrato con gli attuali SIUS e SIGE e destinato a rimanere parte integrante del futuro ecosistema SIES.

L'obiettivo non è introdurre una nuova integrazione puntuale con il PDP, ma costruire il futuro servizio di deposito dell'esecuzione penale e della sorveglianza, capace di operare inizialmente con i sistemi attuali e successivamente con le componenti reingegnerizzate della nuova piattaforma.

### 4.3.3 Accesso del difensore, FE, autorizzazione e legittimazione

Il PDP continua a rappresentare il punto di accesso istituzionale per il difensore, valorizzando i meccanismi di autenticazione già presenti nell'ecosistema del Ministero della Giustizia e l'integrazione con ReGIndE. Una volta autenticato, il professionista accede, tramite una specifica funzione resa disponibile nel PDP, ai servizi di deposito dell'esecuzione penale e della sorveglianza.

La componente FE deve presidiare il profilo autorizzativo connesso allo specifico fascicolo o procedimento. L’autenticazione del professionista e la disponibilità del relativo profilo non determinano, da sole, l’autorizzazione a operare su qualsiasi posizione. Il servizio deve verificare, secondo le regole definite dall’Amministrazione, che il difensore sia autorizzato ad accedere al fascicolo interessato e a effettuare il deposito nel relativo contesto.

Particolare rilevanza assume la verifica della legittimazione del difensore ad operare nell'interesse del soggetto assistito. La nomina non viene quindi considerata esclusivamente come allegato documentale, ma come elemento essenziale del processo di deposito e della successiva trattazione dell'istanza.

| **Livello di controllo** | **Presidio** | **Finalità** |
|:---|:---|:---|
| Identità | PDP | Autenticare il professionista e consentire l’accesso al servizio. |
| Profilo professionale | ReGIndE | Valorizzare le informazioni professionali disponibili nell’ecosistema ministeriale. |
| Autorizzazione al fascicolo/procedimento | FE | Verificare che il difensore possa operare sullo specifico fascicolo o procedimento. |
| Legittimazione | Servizio deposito e ufficio competente | Verificare la relazione tra difensore, assistito, nomina e deposito. |
| Presa in carico | SIES/SIUS/SIGE | Classificare, instradare e associare l’atto al procedimento competente. |

Nella fase iniziale, ove non risultino disponibili controlli automatici centralizzati completi, la verifica della legittimazione può basarsi sulla documentazione prodotta dal difensore e sulle verifiche effettuate dagli uffici competenti. Il modello è tuttavia concepito per evolvere progressivamente, valorizzando FE e le informazioni disponibili nell'ecosistema ministeriale, al fine di ridurre attività manuali e disallineamenti tra procedimenti, nomine e soggetti coinvolti.

### 4.3.4 Integrazione con gli attuali SIUS e SIGE ed evoluzione futura

Nella fase iniziale il componente opera come punto unico di ricezione dei depositi destinati agli uffici dell'esecuzione penale e della sorveglianza. Il personale di cancelleria verifica la lavorabilità, procede alla presa in carico e acquisisce l'istanza nel procedimento di competenza, proseguendo la trattazione negli attuali SIUS e SIGE secondo le modalità operative vigenti.

Con l'avanzare del programma di reingegnerizzazione, il componente di deposito continua a svolgere il medesimo ruolo integrandosi progressivamente con i comparti SIUS e SIGE del nuovo SIES, limitando gli adeguamenti e preservando gli investimenti effettuati.

# 5. Rimodulazione richiesta dall’Amministrazione

Le sezioni 2, 3 e 4 restano parte integrante della proposta. La rimodulazione riguarda la strategia di reingegnerizzazione, la roadmap e la stima economica. Decade la scelta di partire dal SIUS come iniziativa autonoma e propedeutica. L’Amministrazione orienta il programma verso la trasformazione unitaria di SIEP, SIUS e SIGE, da analizzare e sviluppare in parallelo come componenti di un unico ecosistema nazionale.

| **Indirizzo** | **Rimodulazione** |
|:---|:---|
| Programma unitario | SIEP, SIUS e SIGE partono insieme come stream coordinati. |
| Dato unico nazionale | Unica base dati centralizzata e superamento delle basi distrettuali. |
| Modello centrato sulla persona | Dalla logica di registro alla persona, posizione e percorso esecutivo. |
| Interoperabilità interna al SIES | Modulo di servizi e interfacce verso i sistemi titolari dei dati del soggetto e dei provvedimenti irrevocabili. |
| Nessuna coesistenza permanente | Sperimentazione graduale e cut-over finale entro il mese 24. |
| Stima per comparti | Rideterminazione del costo di piattaforma, SIEP, SIUS, SIGE, migrazione e roll-out. |

# 6. Visione del nuovo SIES

Il nuovo SIES sarà una piattaforma nazionale unitaria dell'esecuzione penale e della sorveglianza. I domini SIEP, SIUS e SIGE manterranno la propria riconoscibilità funzionale, ma opereranno su un modello dati condiviso, su servizi trasversali comuni e su un'architettura centralizzata.

La piattaforma comprende un modulo interno di servizi e interfacce per acquisire dai sistemi titolari le informazioni del soggetto e dei provvedimenti divenuti irrevocabili, quali sentenze, ordinanze e decreti. Tale componente non costituisce un’iniziativa o sistema autonomo.

| **Dimensione** | **Oggi** | **Domani** |
|:---|:---|:---|
| Impostazione | Tre sottosistemi e articolazioni territoriali | Un programma e una piattaforma nazionale integrata |
| Dato | Distribuito e potenzialmente duplicato | Unico, centralizzato e governato |
| Unità logica | Registro, procedimento e istanza | Persona, posizione e percorso esecutivo |
| Integrazioni | Puntuali e differenziate | Servizi standard e interfacce native |
| Esercizio | Legacy distinti | Nuovo SIES quale unico ambiente nazionale |

# 7. Assessment e gap analysis integrata

La conoscenza consolidata dell'AS IS consente una fase iniziale mirata, svolta in parallelo sui tre comparti. L’obiettivo è produrre un catalogo funzionale nazionale e non replicare automaticamente tutte le funzioni dei sistemi esistenti.

| **Classe** | **Contenuto** | **Decisione** |
|:---|:---|:---|
| A - Utili e utilizzate | Funzioni operative necessarie ed effettivamente usate | Mantenere, semplificare o reingegnerizzare |
| B - Non utili/non usate | Funzioni superate o non utilizzate | Eliminare dal target |
| C - Mancanti e necessarie | Funzioni oggi assenti ma indispensabili | Inserire nel backlog prioritario |
| D - Nice to have | Funzioni migliorative non essenziali | Posticipare o finanziare se compatibili |

- Catalogo Funzionale Nazionale SIES;

- Mappa dei processi AS IS e TO BE;

- Modello dati target;

- Architettura target;

- Backlog nazionale prioritizzato;

- Piano di migrazione e sperimentazione;

- Stima economica consolidata per comparti.

# 8. Perimetro funzionale SIEP, SIUS e SIGE

| **Comparto** | **Principali ambiti** |
|:---|:---|
| SIEP - Procure | Titolo e posizione esecutiva; ordini di esecuzione e carcerazione; decreti; adempimenti; integrazioni con cognizione, Casellario e altri sistemi. |
| SIUS - Sorveglianza | Fascicolo, istruttoria, udienze, ordinanze, decreti, ricorsi, misure alternative, permessi, licenze, pene sostitutive. |
| SIGE - Giudice dell’Esecuzione | Incidenti di esecuzione, opposizioni, istanze, udienze, provvedimenti e fascicolo. |
| Servizi comuni | Soggetto e posizione; workflow; documentale; firma; identità; sicurezza; audit; monitoraggio; interoperabilità; migrazione. |

# 9. Roadmap integrata di 24 mesi

I 24 mesi rappresentano il limite massimo dell’intero programma e comprendono analisi, progettazione, realizzazione, integrazioni, sperimentazione graduale dei tre comparti, migrazione, formazione, roll-out e dismissione dei sistemi legacy.

| **Fase** | **Periodo** | **Attività** | **Risultato** |
|:---|:---|:---|:---|
| 1\. Gap analysis e disegno target | M1-M5 | Analisi parallela SIEP/SIUS/SIGE, catalogo A/B/C/D, processi, architettura, backlog e piano dati. | Baseline approvata |
| 2\. Fondazioni e primi incrementi | M4-M10 | Piattaforma comune, modello dati, interoperabilità, workflow, sicurezza e primi incrementi. | Funzioni iniziali testabili |
| 3\. Realizzazione completa | M8-M17 | Sviluppo parallelo dei tre comparti, integrazioni, test e migrazioni iterative. | Copertura prioritaria completa |
| 4\. Sperimentazione graduale | M12-M20 | Piloti su Sorveglianza, Procure e Giudice dell’Esecuzione, formazione, feedback e correzioni. | Tre contesti validati |
| 5\. Roll-out e migrazione finale | M19-M24 | Estensione nazionale, migrazione definitiva, formazione, cut-over e supporto. | Nuovo SIES unico sistema |

# 10. Migrazione, sperimentazione e dismissione

La sperimentazione è parte integrante della roadmap e interessa gradualmente tutti i comparti. Le migrazioni selettive alimentano gli uffici pilota; le prove di cut-over, la verifica della qualità e la validazione degli utenti precedono la migrazione definitiva.

| **Wave** | **Ambito** | **Obiettivo** |
|:---|:---|:---|
| A | Sorveglianza - SIUS | Validare fascicolo, istruttoria, provvedimenti, misure e depositi. |
| B | Procure - SIEP | Validare titolo, ordini, adempimenti, integrazioni e posizione esecutiva. |
| C | Giudice dell’Esecuzione - SIGE | Validare incidenti, opposizioni, udienze, provvedimenti e depositi. |

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th><strong>Milestone vincolante<br />
</strong>Entro il mese 24 il nuovo SIES deve essere l’unico sistema nazionale per Procure, Sorveglianza e Giudice dell’Esecuzione, con migrazione conclusa e spegnimento dei legacy SIEP, SIUS e SIGE.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

# 11. Portale utenti esterni e Deleghe alla Polizia Giudiziaria

Il portale per difensori, cittadini e soggetti interessati resta nella visione complessiva, ma è proposto come lotto evolutivo separato rispetto al Core SIES. Il PDP mantiene il punto di accesso istituzionale; il portale SIES eroga i servizi specialistici, inclusi depositi, consultazione, comunicazioni e notifiche.

L’integrazione con il Portale NDR per le deleghe alla Polizia Giudiziaria è collocata in una fase successiva. Il perimetro potrà includere emissione e trasmissione della delega, presa in carico, monitoraggio, comunicazioni, esiti, collegamento al fascicolo e audit.

# 12. Quadro economico preliminare

La stima è programmatica e sarà consolidata al termine della gap analysis. Le evolutive sul sistema attuale e il Deposito Difensore restano parte del programma. Il consolidamento economico dovrà distinguere attività già finanziate o realizzate, completamenti necessari e componenti riutilizzabili nel target, evitando duplicazioni.

| **Macro-ambito** | **Min k€** | **Max k€** | **Contenuto** |
|:---|---:|---:|:---|
| Assessment e gap analysis | 250 | 300 | Analisi parallela, catalogo, processi target, backlog e stima consolidata. |
| Core platform e servizi comuni | 650 | 750 | Dato nazionale, interoperabilità, workflow, documentale, sicurezza e monitoraggio. |
| Comparto SIEP | 600 | 700 | Processi e funzioni delle Procure. |
| Comparto SIUS | 800 | 900 | Processi e funzioni della Sorveglianza. |
| Comparto SIGE | 250 | 350 | Processi e funzioni del Giudice dell’Esecuzione. |
| Migrazione, sperimentazione, formazione e roll-out | 450 | 550 | Data quality, piloti, formazione, avvio e dismissione. |
| TOTALE CORE SIES | 3.000 | 3.550 | Obiettivo programmatico: 3,0-3,5 M€ da consolidare. |

| **Lotto successivo**             | **Stima preliminare** |
|:---------------------------------|:----------------------|
| Portale utenti esterni           | 0,5-0,8 M€            |
| Deleghe alla Polizia Giudiziaria | 0,2-0,4 M€            |

# 13. Governance, vincoli e rischi

| **Elemento** | **Presidio** |
|:---|:---|
| Perimetro | Approvazione del catalogo funzionale e del backlog nazionale. |
| Governance | Steering Committee, Program Management, tavoli SIEP/SIUS/SIGE e tavolo architettura-dati. |
| Dati | Profilazione, bonifica, riconciliazione e prove iterative di migrazione. |
| Sistemi esterni | Accordi di integrazione, specifiche condivise e disponibilità degli ambienti. |
| Uffici pilota | Individuazione anticipata di referenti e calendario delle sperimentazioni. |
| Cut-over | Criteri go/no-go, prove generali, supporto intensivo e piano di rollback controllato. |

# 14. Conclusioni

La proposta mantiene integralmente la parte iniziale relativa alle evolutive sul sistema attuale e ai depositi telematici. Tali interventi conservano il loro valore e sono ricondotti nel programma nazionale come componenti di continuità e riuso.

La rimodulazione riguarda la strategia della reingegnerizzazione: decade la partenza autonoma dalla Sorveglianza e l’intero SIES viene affrontato come piattaforma nazionale unitaria, con analisi parallela di SIEP, SIUS e SIGE, dato centralizzato, modello orientato alla persona e sperimentazione graduale dei tre comparti.

Entro 24 mesi il programma deve portare al nuovo SIES quale unico ambiente di esercizio e alla dismissione dei sistemi legacy. Il Core SIES è collocato in una forchetta preliminare di 3,0-3,5 milioni di euro; il Portale esterno e le Deleghe alla Polizia Giudiziaria sono mantenuti come lotti successivi e separatamente finanziabili.
