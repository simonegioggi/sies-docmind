---
uniqueName: siut-sie-mg-1-0-20200407-definizioneambientesvilup
displayName: "SIUT SIE MG 1 0 20200407 Definizione Ambiente Sviluppo SIES"
category: "GENERAL"
tags: []
---

# SIUT-SIE-MG-1.0-20200407-Definizione_Ambiente_Sviluppo_SIES

> **File originale:** `Docs_CMDBuild_SIES+SIUS_Avvocati/SIUT-SIE-MG-1.0-20200407-Definizione_Ambiente_Sviluppo_SIES.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
Definizione Ambiente di Sviluppo 
 
SIES 
 
 
 
 
 
 
 
Versione 1.0 del 07/04/2020

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 2/25 
 
 
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
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 3/25 
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
30/04/2020 
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
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 4/25 
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
Configurazione del progetto siesWeb ................................................................................ 7 
2.1.2. 
Configurazione del progetto siesEsecuzione ...................................................................... 9 
2.1.3. 
Configurazione JDK........................................................................................................... 10 
2.1.4. 
Configurazione Runtime Environment ............................................................................. 11 
2.1.5. 
Configurazione USER LIBRARIES ....................................................................................... 13 
2.1.6. 
Configurazione strumenti di delivery (es. ANT, JENKINS, MAVEN, GRADLE, etc.) ........... 14 
2.1.7. 
Configurazione generale .................................................................................................. 16 
2.2. APPLICATION SERVER .................................................................................................................... 18 
2.2.1. 
Configurazione librerie ..................................................................................................... 18 
2.2.2. 
Configurazione Datasource .............................................................................................. 18 
2.2.3. 
Installazione report .......................................................................................................... 19 
2.2.4. 
Configurazione applicativa............................................................................................... 19 
2.2.5. 
Configurazione specifica .................................................................................................. 20 
2.3. CONTROLLO DEL SOFTWARE ........................................................................................................... 21 
2.3.1. 
Repository remoto ............................................................................................................ 21 
2.3.2. 
Repository locale .............................................................................................................. 21 
2.3.3. 
Repository Git in Eclipse ................................................................................................... 21 
2.3.4. 
Strumenti di lavoro ........................................................................................................... 21 
2.3.5. 
Struttura repository .......................................................................................................... 22 
2.3.6. 
Standard di nomenclatura e regole generali ................................................................... 22 
3. 
COMPILATORE E STRUTTURA DI PROGETTO ...................................................................... 24 
3.1. STRUTTURA DEL PROGETTO ............................................................................................................ 24 
3.2. REQUISITI AMBIENTE HARDWARE DI SVILUPPO.................................................................................... 24 
4. 
STANDARD ADOTTATI ....................................................................................................... 25

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 5/25 
1. INTRODUZIONE 
1.1 Scopo del documento 
Il presente documento riporta le caratteristiche dell’ambiente di sviluppo utilizzato per la scrittura 
del codice sorgente, del controllo di versione dello stesso e delle procedure utilizzare per la 
produzione degli eseguibili. 
Le configurazioni descritte nel documento valgono per il progetto siesWeb e siesEsecuzione, se non 
diversamente specificato. 
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 6/25 
Sigla 
Descrizione 
PEC 
Posta Elettronica Certificata 
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
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 7/25 
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
Configurazione del progetto siesWeb 
Il progetto siesWeb è scaricabile dal repository git come riferito nel par. 2.3.1 Repository remoto. 
Per configurare il progetto siesWeb in un progetto web occorre procedere  nel seguente modo: 
 
1) tasto destro sul progetto siesWeb; 
2) posizionarsi nel menu "Project"->"Properties"; 
3) spostarsi nell'albero di navigazione sulla sinistra e selezionare il ramo "Project Facets"; 
4) cliccare sul link "Convert to faceted form"; 
 
 
 
5) selezionare il checkbox "Dynamic Web Module" versione 3.0; 
6) selezionare il checkbox "Java" versione 1.8; 
7) selezionare il checkbox "Javascript" versione 1.0;

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 8/25 
 
 
8) cliccare su "Apply"; 
9) selezionare nell'albero di navigazione sulla sinistra il ramo "Deployment Assembly"; 
10) selezionare l’elemento "/WebContent", cliccare su "Remove"; 
11) cliccare su "Add..."; 
12) selezionare l’elemento "Folder" dalla lista "Select Directive Type", cliccare su "Next"; 
13) selezionare l’elemento "defaultroot" dalla lista "Folder", cliccare su "Finish"; 
14) cliccare su "Apply"; 
15) e infine su "OK".

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 9/25 
2.1.2. 
Configurazione del progetto siesEsecuzione 
Il progetto siesEsecuzione è scaricabile dal repository git come riferito nel par. 2.3.1 Repository 
remoto. Il progetto siesEsecuzione è un progetto Maven come riferito ne paragrafo 2.1.6 
Configurazione strumenti di delivery (es. ANT, JENKINS, MAVEN, GRADLE, etc.). 
Per configurare il progetto siesEsecuzione in un progetto web occorre procedere nel seguente 
modo: 
 
1) tasto destro sul progetto siesEsecuzione; 
2) cliccare su Configure > Convert to Maven Project; 
3) posizionarsi nel menu "Project"->"Properties"; 
4) selezionare nell'albero di navigazione sulla sinistra il ramo "Project Facets"; 
5) cliccare sul link "Convert to faceted form"; 
 
 
 
6) selezionare il checkbox "Dynamic Web Module" versione 3.0; 
7) selezionare il checkbox "Java" versione 1.8; 
8) selezionare il checkbox "Javascript" versione 1.0; 
9) selezionare il checkbox “JavaServer Faces” versione 2.1; 
10) selezionare il checkbox “JAX-RS (REST Web Services) versione 1.1”

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 10/25 
 
 
11) cliccare su "Apply". 
2.1.3. 
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
Tale 
configurazione è valida per entrambi i progetti. 
In Eclipse per configurare la JDK occorre: 
 
1) posizionarsi nel menu "Window"->"Preferences"; 
2) nell'albero di navigazione sulla sinistra, selezionare il ramo "Java → Installed JREs"; 
3) cliccare sul pulsante "Add"; 
4) selezionare la voce "Standard VM" e cliccare sul pulsante "Next"; 
5) nel campo "JRE home arguments" inserire il path alla JDK; 
6) dare un nome a "JRE name" e cliccare su "Finish"; 
7) spuntare dalla lista "Installed JREs" il jre aggiunto e infine cliccare su "OK"; 
8) spostarsi sulla voce di menù "Project"->"Properties"; 
9) selezionare l'elemento "Java Build Path"; 
10) posizionarsi sul tab "Libraries"; 
11) selezionare l'elemento "JRE System Library"; 
12) premere il pulsante "Edit..." posizionato sulla destra; 
13) selezionare "Alternate JRE" e "jdk1.8_45"; 
14) cliccare su "Finish" e infine su "OK".

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 11/25 
 
 
Successivamente, selezionare la voce Java > Installed JREs > Execution Environments ed associare 
alla voce JAVA-SE1.8 la JDK precedentemente installata, come nell’immagine seguente: 
 
 
2.1.4. 
Configurazione Runtime Environment 
È stato impostato un Server Runtime Environment denominato JBoss EAP 6.1+ Runtime al quale è 
stata associata un’istanza di Red Hat JBoss Enterprise Application Platform - Version 6.4.0.GA, 
Server base directory standalone e Configuration file standalone.xml, con Execution Environment la 
JDK precedentemente installata. Questa configurazione è valida per entrambi i progetti.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 12/25 
In Eclipse per installarlo occorre: 
1) andare nel menu "Window"->"Preferences"; 
2) selezionare nell'albero di navigazione sulla sinistra il ramo "Server → Runtime 
Environments"; 
3) cliccare sul pulsante "Add" e scegliere dalla categoria "Red Hat JBoss Middleware" il runtime 
"JBoss Enterprise Application Platform 6.1 + Runtime" e premere il pulsante "Next"; 
4) in "Home Directory" mettere il path alla cartella di Jboss; 
5) nel riquadro "Runtime JRE" selezionare "Execution Environment" e "JavaSE-1.8" come JDK; 
6) in "Configuration file" indicare il file di configurazione "standalone.xml" che si trova sotto la  
cartella "<Home Directory>\standalone\configuration" di JBoss; 
7) cliccare su "Finish" e infine su "OK". 
 
 
 
Per entrambi i progetti occorre effettuare la seguente configurazione aggiuntiva: 
1) selezionare il progetto; 
2) andare nel menu "Project"->"Properties";

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 13/25 
3) selezionare nell'albero di navigazione sulla sinistra il ramo "Targeted Runtimes"; 
4) cliccare "JBoss EAP 6 + 1 Runtime"; 
5) cliccare su "Apply", infine cliccare su "OK". 
 
 
 
Per aggiungere il server JBoss: 
1) selezionare "Window"->"View"->"Servers"; 
2) nel tab Server cliccare il tasto destro del mouse, "New"->"Server"; 
3) aprire "Red Hat JBoss Middleware" sull'albero di selezione del server, selezionare "JBoss 
Enterprise Application Platform 6.1 + Runtime", cliccare su "Next", poi di nuovo "Next"; 
4) aggiungere al server entrambi i progetti, premere "Finish". 
2.1.5. 
Configurazione USER LIBRARIES 
E’ stata configurata la user library ojdbc6. 
Il progetto siesWeb necessita di librerie aggiuntive rispetto a quelle di base presenti 
nell’installazione di jboss-eap-6.4. Configurare il build path in modo da aggiungere il jar con il driver 
Oracle al classpath nel seguente modo: 
 
1) selezionare il progetto siesWeb; 
2) selezionare "Project"->"Properties"; 
3) selezionare l'elemento "Java Build Path"; 
4) posizionarsi sul tab "Libraries"; 
5) premere il pulsante "Add Library..." posizionato sulla destra; 
6) selezionare "User Library"; 
7) cliccare su "User Library"; 
8) cliccare su "New";

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 14/25 
9) in "User Library Name" digitare "ojdbc6", cliccare su "OK"; 
10) cliccare "Add External JARs.."; 
11) aggiungere il file ojdbc6.jar jar (presente nel percorso “/home/SIES/jboss-eap-
6.4.Alpha/modules/oracle/jdbc/main”), cliccare "Finish", infine premere "OK". 
 
 
2.1.6. 
Configurazione strumenti di delivery (es. ANT, JENKINS, MAVEN, GRADLE, etc.) 
Per quanto riguarda il progetto siesWeb, al fine di distribuire tutto l'applicativo software sviluppato, 
viene creato un file con estensione .war, acronimo di Web application ARchive, cioè l’archivio usato 
in Java per raggruppare diversi tipi di files dando vita ad un'applicazione o progetto Web. Per fare 
ciò, viene utilizzata la funzione di Eclipse Export  WAR file: 
 
 
 
attivabile cliccando col tasto destro del mouse sul progetto siesWeb. 
Una volta scelta la destinazione di salvataggio del file, premere il tasto “Finish”.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 15/25 
 
 
Per quanto riguarda il progetto siesEsecuzione, al fine di effettuare il packaging degli eseguibili e 
l’esportazione dei sorgenti è stato utilizzato Apache  Maven. Maven utilizza un repository locale 
per risolvere le dipendenze definite nei progetti. Questo repository locale viene aggiornato e 
popolato ogni volta che una nuova dipendenza, non presente localmente, viene trovata nel 
pom.xml del progetto. Per far puntare ad Eclipse il file di configurazione (settings.xml) di Maven 
occorre eseguire i seguenti step: 
1) Spostarsi nel menù "Window"->"Preferences"; 
2) Dall’albero di navigazione, selezionare sulla sinistra il ramo "Maven → User Settings"; 
3) Nel campo "User Settings", indicare il file di configurazione "settings.xml"; 
4) Cliccare su "Apply", infine premere "OK".

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 16/25 
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
 
 
2.1.7. 
Configurazione generale 
È stato introdotto uno standard per i commenti utilizzati nel codice, valido per entrambi i progetti, 
sia per le MAC che per le MEV, secondo l’xml seguente: 
 
Per le MEV: 
 
<?xml version="1.0" encoding="UTF-8"?> 
<templates> 
 
<template autoinsert="true" context="java" deleted="false" description="comment on ISSUE MEV" 
enabled="true" name="MEV"> 
 
 
/* &#13; 
 
 
 * ISSUE MEV : ${descrizione_intervento}&#13; 
 
 
 * Numero MEV : ${numero_MEV}&#13;

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 17/25 
 
 
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
 
<template autoinsert="true" context="java" deleted="false" description="comment on ISSUE MAC" 
enabled="true" name="MAC"> 
 
 
/* &#13; 
 
 
 * ISSUE MAC : ${descrizione_intervento}&#13; 
 
 
 * Numero MAC : ${numero_MAC}&#13; 
 
 
 * Autore    : ${user}&#13; 
 
 
 * Data      : ${date}&#13; 
 
 
 * Branch    : MAC_${numero_MAC}&#13; 
 
 
 */&#13; 
 
 
 ${line_selection}${cursor}&#13; 
 
 
 //***** FINE INTERVENTO MAC_${numero_MAC} *****//&#13; 
 
</template> 
</templates> 
 
In Eclipse per utilizzare i template comuni per la generazione dei commenti occorre caricare gli xml 
citati, precedentemente salvati in file .xml, nel seguente modo: 
 
1) selezionare "Window"->"Preferences"; 
2) selezionare nell'albero di navigazione sulla sinistra il ramo "Java → Editor → Templates"; 
3) cliccare sul pulsante "Import", aggiungere il file .xml del template; 
4) premere "Apply", infine premere "OK".

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 18/25 
2.2. Application Server 
L’application server utilizzato è Red Hat JBoss Enterprise Application Platform - Version 6.4.0.GA, 
Server base directory standalone e Configuration file standalone.xml. 
2.2.1. 
Configurazione librerie 
I progetti siesWeb e siesEsecuzione hanno bisogno di alcune configurazioni aggiuntive. Nella cartella 
di installazione del server JBoss “/home/SIES/jboss-eap-6.4.Alpha/modules”, sono presenti due 
cartelle nominate: 
 
 
 
e contenenti librerie aggiuntive a quelle standard. 
La cartella config contiene i files necessari alla configurazione per la scrittura dei file di log: 
 
 
 
La cartella oracle contiene la libreria ojdbc6.jar che costituisce il driver JDBC lato client di Oracle 
compatibile con Java 6 e successive: 
 
 
2.2.2. 
Configurazione Datasource 
Il datasource applicativo deve essere configurato nel file standalone.xml presente nella cartella di 
installazione del server JBoss: /home/SIES/jboss-eap-6.4.Alpha/standalone/configuration. 
 
<subsystem xmlns="urn:jboss:domain:datasources:1.2"> 
 
<datasources> 
 
 
<datasource jta="true" jndi-name="java:jboss/jdbc/oracleds" pool-name="oracleds" enabled="true" use-java-context="true" 
use-ccm="false">

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 19/25 
 
 
 
<connection-url>jdbc:oracle:thin:@indirizzoServerDB:nomeServizio</connection-url> 
 
 
 
<driver-class>oracle.jdbc.OracleDriver</driver-class> 
 
 
 
<driver>OracleJDBCDriver</driver> 
 
 
 
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
Nel file standalone.xml del server sono state aggiunte proprietà di sistema aggiuntive rispetto 
all’originale nativo del server: 
 
<property name="path.properties" value="/var/SIES/CONFIG"/> 
<property name="WindwardReports.properties.filename" value="/var/SIES/CONFIG/WindwardReports.properties"/> 
<property name="javax.net.ssl.trustStore" value="/var/SIES/CONFIG/certs/sies.jks"/> 
<property name="javax.net.ssl.trustStorePassword" value="trustStorePassword"/> 
<property name="javax.net.ssl.keyStore" value="/var/SIES/CONFIG/certs/serversies.jks"/> 
<property name="javax.net.ssl.keyStorePassword" value="keyStorePassword"/> 
<property name="org.apache.tomcat.util.http.Parameters.MAX_COUNT" value="8192"/> 
<property name="jdk.tls.client.protocols" value="SSLv2Hello,SSLv3,TLSv1"/> 
<property name="javax.net.debug" value="ssl"/> 
 
Inoltre nella sezione “urn:jboss:domain:web:2.2” è stata aggiunta la configurazione per il 
connettore https, necessario per installare e configurare il supporto SSL (Secure Sockets Layer) per 
JBoss. 
 
<subsystem xmlns="urn:jboss:domain:web:2.2" default-virtual-server="default-host" native="false"> 
            <connector name="http" protocol="HTTP/1.1" scheme="http" socket-binding="http"/> 
            <connector name="https" protocol="HTTP/1.1" scheme="https" socket-binding="https" enable-lookups="false" secure="true"> 
                <ssl 
name="https" 
key-alias="1" 
password="password" 
certificate-key-file="/home/SIES/jboss-eap-
6.4.Alpha/standalone/configuration/serversies.jks" protocol="SSLv2Hello,SSLv3,TLSv1"/> 
            </connector> 
            <virtual-server name="default-host" enable-welcome-root="false"> 
                <alias name="localhost"/> 
</virtual-server>

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 20/25 
</subsystem> 
2.2.5. 
Configurazione specifica 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 21/25 
2.3. Controllo del software 
Come strumento di version control viene usato Git. 
2.3.1. 
Repository remoto 
Il repository remoto è raggiungibile all’indirizzo https://production.eng.it/gitlab/giustizia-
siut/sies/sviluppo, tramite autenticazione e autorizzazione. Soltanto gli utenti autorizzati potranno 
accedere al codice sorgente. 
2.3.2. 
Repository locale 
Per configurare il repository locale è necessario aprire una shell Git Bash (scaricare il programma 
GIT 
dal 
sito 
https://git-scm.com/downloads) 
nella 
posizione 
desiderata 
(es. 
D:\workspaces\sies\sviluppo) ed utilizzare il seguente comando: 
 
git clone -b MEV_20 https://production.eng.it/gitlab/giustizia-siut/sies/sviluppo.git 
 
Il comando clona il branch “MEV_20” (-b MEV_20) del repository remoto (git clone <url>) nella 
cartella corrente desiderata. 
2.3.3. 
Repository Git in Eclipse 
Se il repository locale corrisponde al workspace di Eclipse, nella prospettiva Git (selezionabile e 
attivabile dal menu "Window > Perspective > Open Perspective > Other…") dal pannello Git 
Repositories risulterà già censito il repository locale, come nell’immagine seguente: 
 
Se invece il workspace di Eclipse non corrisponde al repository locale, questo va definito, cliccando 
sull’icona evidenziata nell’immagine seguente (sempre dal pannello Git Repositories) e selezionando 
il percorso del repository locale: 
 
2.3.4. 
Strumenti di lavoro 
Per le interazioni con il repository vengono utilizzati i seguenti strumenti: 
1) Git Bash (https://git-scm.com/downloads), attraverso istruzioni da riga di comando;

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 22/25 
2) SourceTree 3.3.8 
(https://www.sourcetreeapp.com/), tool visuale utile per fare 
comparazioni, analizzare i branch e i vari commit; 
3) Plugin Git integrati in Eclipse, in alternativa a SourceTree. 
2.3.5. 
Struttura repository 
Il repository presenta 2 branch perenni: 
1) master 
contiene l’ultima release consegnata; 
2) develop 
contiene l’ultima release consegnata ed è il punto di partenza per gli sviluppi  
di MAC e MEV e per i rilasci; può contenere hot-fixes (modifiche banali e 
lampanti che vanno rilasciate senza dubbio). 
 
Il repository presenta anche branch temporanei: 
1) mac-otrs-numero 
per lo sviluppo delle mac, es. mac-otrs-20200220016; 
2) MEV_numero  
per lo sviluppo delle mev, es. MEV_20; 
3) major.minor.patch per i rilasci, es. release_12.2.1. 
 
Il repository presenta un tag per ogni consegna effettuata, nel formato: 
1) major.minor.patch es. VERSIONE_SIES_12.0.0. 
 
I singoli sviluppi per MAC e MEV vengono effettuati su branch distinti, che una volta testati e 
collaudati vanno integrati (git merge) nel branch dei rilasci major.minor.patch. Alla fine della fase di 
test e dopo il rilascio del software viene eseguito il merge del branch di release sui branch master e 
develop. Successivamente si procede alla cancellazione dei branch temporanei (mac, mev, e release 
appena integrati nel branch master). 
2.3.6. 
Standard di nomenclatura e regole generali 
È stata adottata la seguente convenzione: 
1) i branch per gli sviluppi delle MAC sono denominati mac-otrs-numero, dove numero 
corrisponde al numero del ticket su OTRS, es. mac-otrs-20200220016; 
2) i branch per gli sviluppi delle MEV sono denominati MEV_numero, dove numero corrisponde 
al numero della scheda, es. MEV_20; 
3) i branch per i rilasci sono denominati major.minor.patch, dove major.minor.patch 
corrisponde al numero di versione del software, es. 12.2.1. 
Nell’immagine seguente esempi di nomi attribuiti a branch per mac, mev e rilasci, nonché i branch 
perenni, master e develop:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 23/25 
I commit effettuati sui branch di mac e di mev devono assumere per convenzione il seguente 
formato: 
 
<nome-branch>: <testo> 
 
Di seguito alcuni esempi: 
1) mac-otrs-20200220016: modifica controllo sul fascicolo; 
2) MEV_20: aggiunta proprietà Sede nel dettaglio del provvedimento.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-MG-1.0-20200407- Definizione Ambiente Sviluppo 
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 24/25 
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
SIES 
Ver. 1.0 del 07/04/2020 
Pag. 25/25 
4. Standard adottati 
N.A.