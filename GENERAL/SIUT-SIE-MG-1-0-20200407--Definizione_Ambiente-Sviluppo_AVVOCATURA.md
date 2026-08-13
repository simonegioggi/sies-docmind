---
uniqueName: siut-sie-mg-1-0-20200407-definizioneambiente-svilu
displayName: "SIUT SIE MG 1 0 20200407  Definizione Ambiente Sviluppo AVVOCATURA"
category: "GENERAL"
tags: []
---

# SIUT-SIE-MG-1.0-20200407- Definizione_Ambiente-Sviluppo_AVVOCATURA

> **File originale:** `Docs_CMDBuild_SIES+SIUS_Avvocati/SIUT-SIE-MG-1.0-20200407- Definizione_Ambiente-Sviluppo_AVVOCATURA.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
Definizione Ambiente di sviluppo 
 
Avvocatura-SIUS 
 
 
 
 
 
 
 
Versione 1.0 del 07/04/2020

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 2/17 
 
 
Il presente documento è stato redatto con la 
collaborazione 
del 
RTI 
Engineering 
Ingegneria 
Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del 
contratto 
CIG 73479643B7 
per 
lo 
“Sviluppo 
del 
Sistema 
Informativo 
Unitario 
Telematico, 
la 
manutenzione degli attuali sistemi dell’area Penale 
del Ministero della Giustizia e servizi correlati. Lotto 
1”.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 3/17 
Approvazioni 
 
Nominativo 
Funzione 
Elaborato da 
Monica Giraldi, Simone Gioggi 
Analista programmatore 
Programmatore
Verificato da 
Vito Bufi 
Responsabile Manutenzione Sistemi attuali 
Approvato da 
Paolo Ceccanti 
Responsabile Unico Fornitura 
Data approvazione 
07/04/2020 
 
Livello di riservatezza 
L3 
 
 
Elenco versioni 
Versione
Data 
Motivo
Modifica
1.0 
07/04/2020 
Prima Emissione 
 
 
Lista di distribuzione 
Nominativo
Organizzazione
Ufficio
Funzione
Ing. Giovanni Malesci 
Amministrazione
 
Responsabile Unico Procedimento 
Dr.ssa Annamaria Palmieri 
Amministrazione
 
Direttore Esecutivo Contratto 
Paolo Ceccanti
RTI
Responsabile Unico Fornitura
Pasquale Lamattina 
RTI 
 
Referente Tecnico 
Vito Bufi 
RTI 
 
Responsabile Manutenzione Sistemi attuali 
Fabio Mazzocchi
RTI
Responsabile Manutenzione Correttiva
Andrea Salvaggio 
RTI 
 
Responsabile Progetto Sistema Unitario 
Antonio Iacobelli 
RTI 
 
Responsabile Supporto Specialistico 
Antonella Damiani
RTI
Responsabile Centro di Competenza
Fabio Gattamorta 
RTI 
 
Responsabile PMO  
Alessandro Falleni 
RTI 
 
Referente sicurezza 
Edoardo Lamuraglia 
RTI 
 
Referente qualità 
Francesco Rosati 
RTI 
 
Referente qualità 
Andrea Castorino
RTI
Referente Applicativo Gestore Fascicolo Documentale
Luigi Buglione 
RTI 
 
Referente metrico

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 4/17 
INDICE DEI CONTENUTI 
1. 
INTRODUZIONE ................................................................................................................... 5 
1.1 
SCOPO DEL DOCUMENTO ................................................................................................................. 5 
1.2 
RIFERIMENTI ................................................................................................................................. 5 
1.3 
GLOSSARIO ................................................................................................................................... 5 
1.3.1 
Definizioni ........................................................................................................................... 5 
1.3.2 
Acronimi e abbreviazioni .................................................................................................... 5 
2. 
SOFTWARE AMBIENTE DI SVILUPPO .................................................................................... 7 
2.1. ECLIPSE JAVA EE IDE ...................................................................................................................... 7 
2.1.1. 
Configurazione JDK............................................................................................................. 7 
2.1.2. 
Configurazione Runtime Environment ............................................................................... 8 
2.1.3. 
Configurazione USER LIBRARIES ....................................................................................... 10 
2.1.4. 
Configurazione strumenti di delivery (es. ANT, JENKINS, MAVEN, GRADLE, etc.) ........... 10 
2.1.5. 
Configurazione generale .................................................................................................. 11 
2.2. APPLICATION SERVER .................................................................................................................... 12 
2.2.1. 
Configurazione librerie ..................................................................................................... 12 
2.2.2. 
Configurazione Datasource .............................................................................................. 12 
2.2.3. 
Installazione report .......................................................................................................... 13 
2.2.4. 
Configurazione applicativa............................................................................................... 13 
2.2.5. 
Configurazione specifica .................................................................................................. 13 
2.3. CONTROLLO DEL SOFTWARE ........................................................................................................... 13 
2.3.1. 
Repository remoto ............................................................................................................ 13 
2.3.2. 
Repository locale .............................................................................................................. 13 
2.3.3. 
Repository SVN in Eclipse ................................................................................................. 14 
2.3.4. 
Strumenti di lavoro ........................................................................................................... 15 
2.3.5. 
Struttura repository .......................................................................................................... 15 
2.3.6. 
Standard di nomenclatura e regole generali ................................................................... 15 
3. 
COMPILATORE E STRUTTURA DI PROGETTO ...................................................................... 16 
3.1. STRUTTURA DEL PROGETTO ............................................................................................................ 16 
3.2. REQUISITI AMBIENTE HARDWARE DI SVILUPPO.................................................................................... 16 
4. 
STANDARD ADOTTATI ....................................................................................................... 17

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 5/17 
1. INTRODUZIONE 
1.1 Scopo del documento 
Il presente documento riporta le caratteristiche dell’ambiente di sviluppo utilizzato per la scrittura 
del codice sorgente, del controllo di versione dello stesso e delle procedure utilizzare per la 
produzione degli eseguibili. 
1.2 Riferimenti 
Riferimento 
Nome Documento 
Descrizione Documento 
RIF1. 
 
SIUT-GEN-SN-2.2-20191023-Standard di nomenclatura 
Documento 
che 
contiene 
gli 
standard di nomenclatura dei vari 
sistemi 
1.3 Glossario 
1.3.1 
Definizioni 
Definizione
Descrizione
 
 
1.3.2 
Acronimi e abbreviazioni 
Sigla 
Descrizione 
AgID 
Agenzia per l’Italia Digitale 
API 
Application Programming Interface 
CPU
Central Processing Unit
CV 
Curriculum Vitae 
DB
Data Base
DEC 
Direttore Esecutivo Contratto 
DGSIA
Direzione Generale per i Sistemi Informativi Automatizzati
DR 
Disaster Recovery 
ETSI
European Telecommunications Standards Institute
FP 
Function Point 
GdL
Gruppo di Lavoro
GDPR 
General Data Protection Regulation 
HW
HardWare
ICT 
Information & Communication Technology 
ISO
International Organization for Standardization
ISP 
Information Security Policy 
IT
Information Technology
KPI 
Key Performance Indicator 
MAAC
MAndatory Access Control
MAC 
MAnutenzione Correttiva 
MEV
Manutenzione EVolutiva
OWASP 
Open Web Application Security Project 
PA 
Pubblica Amministrazione 
PEC 
Posta Elettronica Certificata

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 6/17 
Sigla 
Descrizione 
PDCA 
Plan, Do, Check, Act 
PdQ 
Piano della Qualità 
PdP 
Piano di Progetto 
PdS
Piano della Sicurezza
PMO 
Program Management Office 
POO
Program Operating Office
QM 
Quality Manager 
RA
Risk Assessment
RID 
Riservatezza, Integrità, Disponibilità 
RM
Resource Manager
RPO 
Recovery Point Objective 
RTO
Recovery Time Objective
RTI 
Raggruppamento Temporaneo di Impresa 
RUF
Responsabile Unico Fornitore
RUP 
Responsabile Unico Progetto 
SAL
Stato Avanzamento Lavori
SGQ 
Sistema di Gestione per la Qualità di Engineering Ingegneria Informatica S.p.A. 
SGSI
Sistema di Gestione della Sicurezza Informatica
SIU 
Sistema Informativo Unitario 
SLA
Service Level Agreement
SM 
Security Manager 
SQL 
Structured Query Language 
SW 
SoftWare 
TT 
Trouble Ticketing 
UTA 
Utente Generico Amministrazione 
VPN 
Virtual Private Network

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 7/17 
2. Software ambiente di sviluppo  
2.1. Eclipse Java EE IDE 
Il tool utilizzato per la scrittura del codice sorgente è Eclipse Java EE IDE for Web Developers 
versione Luna Service Release 2 (4.4.2) o superiore. 
Esso è un ambiente di sviluppo integrato multi-linguaggio e multipiattaforma, che supporta i 
programmatori nello sviluppo del codice del programma, segnalando errori di sintassi del codice 
direttamente in fase di scrittura, oltre a tutta una serie di strumenti e funzionalità di supporto alla 
fase di sviluppo e debugging. 
È possibile scaricare l’ultima versione da https://www.eclipse.org/downloads/. 
2.1.1. 
Configurazione JDK 
Per 
la 
compilazione 
dei 
sorgenti 
è 
stata 
utilizzata 
la 
JDK 
1.8.0_45 
(https://www.oracle.com/java/technologies/javase/javase8-archive-downloads.html). 
 
Per configurare la JDK in Eclipse occorre eseguire i seguenti step: 
1) Posizionarsi nel menu "Window"->"Preferences"; 
2) Nell'albero di navigazione sulla sinistra, selezionare il ramo "Java → Installed JREs"; 
3) Cliccare sul pulsante "Add"; 
4) Selezionare la voce "Standard VM" e cliccare sul pulsante "Next"; 
5) Nel campo "JRE home arguments" inserire il path alla JDK; 
6) Dare un nome a "JRE name" e cliccare su "Finish"; 
7) Spuntare dalla lista "Installed JREs" il jre aggiunto e infine cliccare su "OK"; 
8) Spostarsi sulla voce di menù "Project"->"Properties"; 
9) Selezionare l'elemento "Java Build Path"; 
10) Posizionarsi sul tab "Libraries"; 
11) Selezionare l'elemento "JRE System Library"; 
12) Premere il pulsante "Edit..." posizionato sulla destra; 
13) Selezionare "Alternate JRE" e "jdk1.8_45"; 
14) Clicclare su "Finish" e infine su "OK".

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 8/17 
 
 
Successivamente, selezionare la voce Java > Installed JREs > Execution Environments ed associare 
alla voce JAVA-SE1.8 la JDK precedentemente installata, come nell’immagine seguente: 
 
 
2.1.2. 
Configurazione Runtime Environment 
È stato impostato un Server Runtime Environment denominato JBoss EAP 6.1+ Runtime al quale è 
stata associata un’istanza di Red Hat JBoss Enterprise Application Platform - Version 6.4.0.GA, 
Server base directory standalone e Configuration file standalone.xml, con Execution Environment la 
JDK precedentemente installata.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 9/17 
Per configurare ed installare il server in Eclipse occorre eseguire i seguenti step: 
 
1) Posizionarsi nel menu "Window"->"Preferences"; 
2) Nell’albero di navigazione sulla sinistra selezionare il ramo "Server → Runtime 
Environments"; 
3) Cliccare sul pulsante "Add" e, dalla categoria "Red Hat JBoss Middleware", scegliere come 
runtime la voce "JBoss Enterprise Application Platform 6.1 + Runtime" e premere il pulsante 
"Next"; 
4) Nel campo "Home Directory” inserire il percorso del file system alla cartella di installazione 
di Jboss; 
5) Nel riquadro "Runtime JRE" selezionare "Execution Environment" e "JavaSE-1.8" come JDK; 
6) Nel campo "Configuration file" indicare il file di configurazione "standalone.xml" che si trova 
sotto la cartella "<Home Directory>\standalone\configuration" di Jboss; 
7) Cliccare su "Finish" e infine su "OK". 
 
 
 
Per aggiungere il server Jboss all’ambiente id sviluppo, eseguire i seguenti step: 
1) Selezionare "Window"->"View"->"Servers"; 
2) Nel tab Server cliccare il tasto destro del mouse, "New"->"Server";

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 10/17 
3) Aprire "Red Hat JBoss Middleware", sull'albero di selezione del server, selezionare "JBoss 
Enterprise Application Platform 6.1 + Runtime", cliccare su "Next", poi di nuovo "Next"; 
4) Aggiungere l'applicazione alle risorse, premere "Finish". 
2.1.3. 
Configurazione USER LIBRARIES 
Non sono state utilizzate USER LIBRARIES. 
2.1.4. 
Configurazione strumenti di delivery (es. ANT, JENKINS, MAVEN, GRADLE, etc.) 
Per effettuare il packaging degli eseguibili e l’esportazione dei sorgenti è stato utilizzato Apache  
Maven. 
Maven utilizza un repository locale per risolvere le dipendenze definite nei progetti. Questo 
repository locale viene aggiornato e popolato ogni volta che una nuova dipendenza, non presente 
localmente, viene trovata nel pom.xml del progetto.  
Per far puntare Eclipse al file di configurazione (settings.xml) di Maven occorre eseguire i seguenti 
step: 
1) Spostarsi nel menù "Window"->"Preferences"; 
2) Dall’albero di navigazione, selezionare sulla sinistra il ramo "Maven → User Settings"; 
3) Nel campo "User Settings", indicare il file di configurazione "settings.xml"; 
4) Cliccare su "Apply", infine premere "OK". 
 
Per 
distribuire 
tutto 
l'applicativo 
software 
sviluppato, 
viene 
creato 
un 
file 
con estensione  .war, acronimo di Web Application Archive. 
Per fare ciò, viene utilizzata la funzione Run As  Maven install di Eclipse:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 11/17 
 
2.1.5. 
Configurazione generale 
È stato introdotto uno standard per i commenti utilizzati nel codice, sia per le MAC che per le MEV, 
secondo l’xml seguente: 
 
Per le MEV: 
 
<?xml version="1.0" encoding="UTF-8"?> 
<templates> 
 
<template autoinsert="true" context="java" deleted="false" description="comment on ISSUE 
MEV" enabled="true" name="MEV"> 
 
 
/* &#13; 
 
 
 * ISSUE MEV : ${descrizione_intervento}&#13; 
 
 
 * Numero MEV : ${numero_MEV}&#13; 
 
 
 * Autore    : ${user}&#13; 
 
 
 * Data      : ${date}&#13; 
 
 
 * Branch    : MEV_${numero_MEV}&#13; 
 
 
 */&#13; 
 
 
 ${line_selection}${cursor}&#13; 
 
 
 //***** FINE INTERVENTO MEV_${numero_MEV} *****//&#13; 
 
</template> 
</templates> 
 
Per le MAC: 
 
<?xml version="1.0" encoding="UTF-8"?> 
<templates> 
 
<template autoinsert="true" context="java" deleted="false" description="comment on ISSUE 
MAC" enabled="true" name="MAC"> 
 
 
/* &#13; 
 
 
 * ISSUE MAC : ${descrizione_intervento}&#13; 
 
 
 * Numero MAC : ${numero_MAC}&#13; 
 
 
 * Autore    : ${user}&#13; 
 
 
 * Data      : ${date}&#13; 
 
 
 * Branch    : MAC_${numero_MAC}&#13;

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 12/17 
 
 
 */&#13; 
 
 
 ${line_selection}${cursor}&#13; 
 
 
 //***** FINE INTERVENTO MAC_${numero_MAC} *****//&#13; 
 
</template> 
</templates> 
 
In Eclipse per utilizzare i template comuni per la generazione dei commenti occorre caricare gli xml 
citati, precedentemente salvati in file .xml, nel seguente modo: 
 
1) Selezionare "Window"->"Preferences"; 
2) Dall’albero di navigazione sulla sinistra, selezionare il ramo "Java → Editor → Templates"; 
3) Cliccare sul pulsante "Import", aggiungere il file .xml del template; 
4) Cliccare "Apply", infine premere "OK". 
 
 
2.2. Application Server 
L’application server utilizzato è Red Hat JBoss Enterprise Application Platform - Version 6.4.0.GA, 
Server base directory standalone e Configuration file standalone.xml. 
2.2.1. 
Configurazione librerie 
L’applicativo non necessita di librerie aggiuntive rispetto a quelle di base presenti nell’installazione 
di Jboss6.4.0.GA. 
2.2.2. 
Configurazione Datasource 
Il datasource applicativo deve essere configurato nel file standalone.xml presente nella cartella di 
installazione del server JBoss: /home/SIES/jboss-eap-6.4.Alpha/standalone/configuration. 
 
<subsystem xmlns="urn:jboss:domain:datasources:1.2"> 
 
<datasources> 
 
 
<datasource jta="true" jndi-name="java:jboss/jdbc/oracleds" pool-name="oracleds" enabled="true" use-java-context="true" 
use-ccm="false"> 
 
 
 
<connection-url>jdbc:oracle:thin:@indirizzoServerDB:nomeServizio</connection-url> 
 
 
 
<driver-class>oracle.jdbc.OracleDriver</driver-class> 
 
 
 
<driver>OracleJDBCDriver</driver>

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 13/17 
 
 
 
<pool> 
 
 
 
 
<min-pool-size>10</min-pool-size> 
 
 
 
 
<max-pool-size>1024</max-pool-size> 
 
 
 
 
<prefill>false</prefill> 
 
 
 
 
<use-strict-min>false</use-strict-min> 
 
 
 
 
<flush-strategy>FailingConnectionOnly</flush-strategy> 
 
 
 
</pool> 
 
 
 
<security> 
 
 
 
 
<user-name>username</user-name> 
 
 
 
 
<password>psw</password> 
 
 
 
</security> 
 
 
 
<validation> 
 
 
 
 
<check-valid-connection-sql>SELECT 1 FROM DUAL</check-valid-connection-sql> 
 
 
 
 
<validate-on-match>false</validate-on-match> 
 
 
 
 
<background-validation>false</background-validation> 
 
 
 
</validation> 
 
 
 
<statement> 
 
 
 
 
<share-prepared-statements>false</share-prepared-statements> 
 
 
 
</statement> 
 
 
</datasource> 
 
 
<drivers> 
 
 
 
<driver name="OracleJDBCDriver" module="oracle.jdbc"/> 
 
 
</drivers> 
 
</datasources> 
</subsystem> 
2.2.3. 
Installazione report 
Non Applicabile. 
2.2.4. 
Configurazione applicativa 
Non Applicabile. 
2.2.5. 
Configurazione specifica 
Non Applicabile. 
2.3. Controllo del software 
Come strumento di version control viene usato SVN. 
2.3.1. 
Repository remoto 
Il 
repository 
remoto 
è 
raggiungibile 
all’indirizzo 
https://production.eng.it/scm/svnrepos/sigi/avvocatura-sies, 
tramite 
autenticazione 
e 
autorizzazione. Soltanto gli utenti autorizzati potranno accedere al codice sorgente. 
2.3.2. 
Repository locale 
Per configurare il repository locale è necessario scaricare il programma TortoiseSVN 
(https://tortoisesvn.net/downloads.html) e scaricare il progetto nella posizione desiderata (es. 
D:\workspaces\avvocatura\sviluppo) tramite il comando TortoiseSVN > Importa:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 14/17 
 
 
Il comando scarica il progetto del repository remoto nella cartella corrente. 
2.3.3. 
Repository SVN in Eclipse 
Se il repository locale corrisponde al workspace di Eclipse, nella prospettiva SVN Repository 
Exploring (selezionabile e attivabile dal menù Window > Perspective > Open Perspective > Other…) 
dal pannello SVN Repositories risulterà già censito il repository locale, come nell’immagine 
seguente: 
 
 
 
Se invece il workspace di Eclipse non corrisponde al repository locale, questo va definito, (New  
Repository) cliccando sull’icona evidenziata nell’immagine seguente (sempre dal pannello SVN 
Repositories) e selezionando il percorso del repository locale:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 15/17 
 
A questo punto selezionare all’interno del repository il progetto di cui si vuole fare il checkout, 
cliccare tasto dentro e selezionare la voce “Check out as Maven Project...". 
2.3.4. 
Strumenti di lavoro 
Per le interazioni con il repository viene utilizzato il plug-in Subversive - SVN Team Provider versione 
4.0.5 da integrare in Eclipse nel seguente modo: 
1) Spostarsi nel menu "Help"->"Eclipse Marketplace"; 
2) Nella barra di ricerca, digitare Subclipse e cliccare infine su Install (è necessario spuntare 
tutte le opzioni di installazione). 
2.3.5. 
Struttura repository 
Il repository presenta un branch perenne: 
• trunk  
contiene la prima release consegnata. 
 
Il repository presenta anche branches temporanei: 
• branches 
per la realizzazione delle varie MEV. 
 
I singoli sviluppi per MAC e MEV vengono effettuati su branch distinti, che una volta testati e 
collaudati vanno integrati (SVN merge) nel branch trunk. Alla fine della fase di test e dopo il rilascio 
del software viene eseguito il merge del branch di release sui branch trunk. 
2.3.6. 
Standard di nomenclatura e regole generali 
È stata adottata la seguente convenzione: 
• i branch per gli sviluppi delle MAC sono denominati mac-otrs-numero, dove numero 
corrisponde al numero del ticket su OTRS, es. mac-otrs-20200310016 
• i branch per gli sviluppi delle MEV sono denominati MEV_numero, dove numero corrisponde 
al numero della scheda, es. MEV_20 
• i branch per i rilasci sono denominati major.minor.patch, dove major.minor.patch 
corrisponde al numero di versione del software, es. 3.0.6. 
 
I commit effettuati sui branch di mac e di mev devono assumere per convenzione il seguente 
formato: 
 
<nome-branch>: <testo> 
 
Di seguito alcuni esempi: 
mac-otrs-20200114013: modificata query ricerca provvedimenti; 
MEV_20: aggiunto campo Sede nella ricerca dei provvedimenti.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 16/17 
3. Compilatore e struttura di progetto 
N.A. 
3.1. Struttura del progetto 
N.A. 
3.2. Requisiti ambiente hardware di sviluppo 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 17/17 
4. Standard adottati 
N.A.