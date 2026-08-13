---
uniqueName: siut-sie-mg-10-20200407-definizione-ambiente-svilu
displayName: "SIUT SIE MG 1.0 20200407  Definizione Ambiente Sviluppo SIES"
category: "GENERAL"
tags: []
---

﻿
| Ministero della GiustiziaDipartimento dell’Organizzazione Giudiziaria, del Personale e dei ServiziDirezione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |



Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni

|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Simone Gioggi | Analista programmatore Senior |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 07/04/2020 |  |
| Livello di riservatezza | L3 |  |


Elenco versioni

| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 30/04/2020 | Prima Emissione |  |


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
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |
| Luigi Buglione | RTI |  | Referente metrico |



INDICE DEI CONTENUTI
1.Introduzione5
1.1Scopo del documento5
1.2Riferimenti5
1.3Glossario5
1.3.1Definizioni5
1.3.2Acronimi e abbreviazioni5
2.Software ambiente di sviluppo7
2.1.Eclipse Java EE IDE7
2.1.1.Configurazione del progetto siesWeb7
2.1.2.Configurazione del progetto siesEsecuzione9
2.1.3.Configurazione JDK10
2.1.4.Configurazione Runtime Environment11
2.1.5.Configurazione USER LIBRARIES13
2.1.6.Configurazione strumenti di delivery (es. ANT, JENKINS, MAVEN, GRADLE, etc.)14
2.1.7.Configurazione generale16
2.2.Application Server18
2.2.1.Configurazione librerie18
2.2.2.Configurazione Datasource18
2.2.3.Installazione report19
2.2.4.Configurazione applicativa19
2.2.5.Configurazione specifica20
2.3.Controllo del software21
2.3.1.Repository remoto21
2.3.2.Repository locale21
2.3.3.Repository Git in Eclipse21
2.3.4.Strumenti di lavoro21
2.3.5.Struttura repository22
2.3.6.Standard di nomenclatura e regole generali22
3.Compilatore e struttura di progetto24
3.1.Struttura del progetto24
3.2.Requisiti ambiente hardware di sviluppo24
4.Standard adottati25



Introduzione
## Scopo del documento

Il presente documento riporta le caratteristiche dell’ambiente di sviluppo utilizzato per la scrittura del codice sorgente, del controllo di versione dello stesso e delle procedure utilizzare per la produzione degli eseguibili.
Le configurazioni descritte nel documento valgono per il progetto siesWeb e siesEsecuzione, se non diversamente specificato.
## Riferimenti


| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
|  | SIUT-GEN-SN-2.2-20191023-Standard di nomenclatura | Documento che contiene gli standard di nomenclatura dei vari sistemi |

## Glossario

### Definizioni


| Definizione | Descrizione |
| --- | --- |
|  |  |

### Acronimi e abbreviazioni


| Sigla | Descrizione |
| --- | --- |
| AgID | Agenzia per l’Italia Digitale |
| API | Application Programming Interface |
| CPU | Central Processing Unit |
| CV | Curriculum Vitae |
| DB | Data Base |
| DEC | Direttore Esecutivo Contratto |
| DGSIA | Direzione Generale per i Sistemi Informativi Automatizzati |
| DR | Disaster Recovery |
| ETSI | European Telecommunications Standards Institute |
| FP | Function Point |
| GdL | Gruppo di Lavoro |
| GDPR | General Data Protection Regulation |
| HW | HardWare |
| ICT | Information & Communication Technology |
| ISO | International Organization for Standardization |
| ISP | Information Security Policy |
| IT | Information Technology |
| KPI | Key Performance Indicator |
| MAAC | MAndatory Access Control |
| MAC | MAnutenzione Correttiva |
| MEV | Manutenzione EVolutiva |
| OWASP | Open Web Application Security Project |
| PA | Pubblica Amministrazione |
| PEC | Posta Elettronica Certificata |
| PDCA | Plan, Do, Check, Act |
| PdQ | Piano della Qualità |
| PdP | Piano di Progetto |
| PdS | Piano della Sicurezza |
| PMO | Program Management Office |
| POO | Program Operating Office |
| QM | Quality Manager |
| RA | Risk Assessment |
| RID | Riservatezza, Integrità, Disponibilità |
| RM | Resource Manager |
| RPO | Recovery Point Objective |
| RTO | Recovery Time Objective |
| RTI | Raggruppamento Temporaneo di Impresa |
| RUF | Responsabile Unico Fornitore |
| RUP | Responsabile Unico Progetto |
| SAL | Stato Avanzamento Lavori |
| SGQ | Sistema di Gestione per la Qualità di Engineering Ingegneria Informatica S.p.A. |
| SGSI | Sistema di Gestione della Sicurezza Informatica |
| SIU | Sistema Informativo Unitario |
| SLA | Service Level Agreement |
| SM | Security Manager |
| SQL | Structured Query Language |
| SW | SoftWare |
| TT | Trouble Ticketing |
| UTA | Utente Generico Amministrazione |
| VPN | Virtual Private Network |


Software ambiente di sviluppo
Eclipse Java EE IDE
Il tool utilizzato per la scrittura del codice sorgente è Eclipse Java EE IDE for Web Developers versione Luna Service Release 2 (4.4.2) o superiore.
Esso è un ambiente di sviluppo integrato multi-linguaggio e multipiattaforma, che supporta i programmatori nello sviluppo del codice del programma, segnalando errori di sintassi del codice direttamente in fase di scrittura, oltre a tutta una serie di strumenti e funzionalità di supporto alla fase di sviluppo e debugging.
È possibile scaricare l’ultima versione da https://www.eclipse.org/downloads/.
Configurazione del progetto siesWeb
Il progetto siesWeb è scaricabile dal repository git come riferito nel par. 4.1Repository remoto.
Per configurare il progetto siesWeb in un progetto web occorre procedere  nel seguente modo:

tasto destro sul progetto siesWeb;
posizionarsi nel menu "Project"->"Properties";
- spostarsinell'albero di navigazione sulla sinistra eselezionare il ramo "Project Facets";
- cliccaresul link "Convert to faceted form";



- selezionare il checkbox"Dynamic Web Module" versione 3.0;
- selezionare il checkbox"Java" versione 1.8;
- selezionare il checkbox"Javascript" versione 1.0;



- cliccare su "Apply";
- selezionare nell'albero di navigazione sulla sinistra il ramo "Deployment Assembly";
- selezionare l’elemento "/WebContent", cliccare su "Remove";
- cliccare su "Add...";
- selezionare l’elemento "Folder" dalla lista "Select Directive Type", cliccare su "Next";
- selezionare l’elemento "defaultroot" dalla lista "Folder", cliccare su "Finish";
- cliccare su "Apply";
- e infine su "OK".


Configurazione del progetto siesEsecuzione
Il progetto siesEsecuzione è scaricabile dal repository git come riferito nel par. 4.1Repository remoto. Il progetto siesEsecuzione è un progetto Maven come riferito ne paragrafo 2.6Configurazione strumenti di delivery (es. ANT, JENKINS, MAVEN, GRADLE, etc.).
Per configurare il progetto siesEsecuzione in un progetto web occorre procedere nel seguente modo:

- tasto destro sul progetto siesEsecuzione;
- cliccare su Configure > Convert to Maven Project;
posizionarsinel menu "Project"->"Properties";
- selezionare nell'albero di navigazione sulla sinistra il ramo "Project Facets";
- cliccaresul link "Convert to faceted form";



- selezionare il checkbox "Dynamic Web Module" versione 3.0;
- selezionare il checkbox"Java" versione 1.8;
- selezionare il checkbox"Javascript" versione 1.0;
- selezionare il checkbox“JavaServer Faces” versione 2.1;
- selezionare il checkbox “JAX-RS (REST Web Services) versione 1.1”



- cliccare su "Apply".
Configurazione JDK
Per la compilazione dei sorgenti è stata utilizzata la JDK 1.8.0_45 (https://www.oracle.com/java/technologies/javase/javase8-archive-downloads.html).Tale configurazione è valida per entrambi i progetti.
In Eclipse per configurare la JDK occorre:

posizionarsi nel menu "Window"->"Preferences";
nell'albero di navigazione sulla sinistra, selezionare il ramo "Java → Installed JREs";
cliccare sul pulsante "Add";
selezionare la voce "Standard VM" e cliccare sul pulsante "Next";
nel campo "JRE home arguments" inserire il path alla JDK;
dare un nome a "JRE name" e cliccare su "Finish";
spuntare dalla lista "Installed JREs" il jre aggiunto e infine cliccare su "OK";
spostarsi sulla voce di menù "Project"->"Properties";
selezionare l'elemento "Java Build Path";
posizionarsi sul tab "Libraries";
selezionare l'elemento "JRE System Library";
premere il pulsante "Edit..." posizionato sulla destra;
selezionare "Alternate JRE" e "jdk1.8_45";
cliccare su "Finish" e infine su "OK".



Successivamente, selezionare la voce Java > Installed JREs> Execution Environments ed associare alla voce JAVA-SE1.8 la JDK precedentemente installata, come nell’immagine seguente:


Configurazione Runtime Environment
È stato impostato un Server Runtime Environment denominato JBoss EAP 6.1+ Runtime al quale è stata associata un’istanza di Red Hat JBoss Enterprise Application Platform - Version 6.4.0.GA, Server base directory standalone e Configuration file standalone.xml, con Execution Environment la JDK precedentemente installata. Questa configurazione è valida per entrambi i progetti.
In Eclipse per installarlo occorre:
andare nel menu "Window"->"Preferences";
selezionare nell'albero di navigazione sulla sinistra il ramo "Server → Runtime Environments";
cliccare sul pulsante "Add" e scegliere dalla categoria "Red Hat JBoss Middleware" il runtime "JBoss Enterprise Application Platform 6.1 + Runtime" e premere il pulsante "Next";
in "Home Directory" mettere il path alla cartella di Jboss;
nel riquadro "Runtime JRE" selezionare "Execution Environment" e "JavaSE-1.8" come JDK;
in "Configuration file" indicare il file di configurazione "standalone.xml" che si trova sotto la  cartella "<Home Directory>\standalone\configuration" di JBoss;
cliccare su "Finish" e infine su "OK".



Per entrambi i progettioccorre effettuare la seguente configurazione aggiuntiva:
selezionare il progetto;
andare nel menu "Project"->"Properties";
selezionarenell'albero di navigazione sulla sinistra il ramo "Targeted Runtimes";
cliccare "JBoss EAP 6 + 1 Runtime";
cliccare su "Apply", infine cliccare su "OK".



Per aggiungere il server JBoss:
selezionare "Window"->"View"->"Servers";
nel tab Server cliccare il tasto destro del mouse, "New"->"Server";
aprire"Red Hat JBoss Middleware" sull'albero di selezione del server, selezionare "JBoss Enterprise Application Platform 6.1 + Runtime", cliccare su "Next", poi di nuovo "Next";
aggiungere al server entrambi i progetti, premere "Finish".
Configurazione USER LIBRARIES
E’ stata configurata la user library ojdbc6.
Il progetto siesWeb necessita di librerie aggiuntive rispetto a quelle di base presenti nell’installazione di jboss-eap-6.4. Configurare il build path in modo da aggiungere il jar con il driver Oracle al classpath nel seguente modo:

selezionare il progetto siesWeb;
selezionare "Project"->"Properties";
selezionare l'elemento "Java Build Path";
posizionarsi sul tab "Libraries";
premere il pulsante "Add Library..." posizionato sulla destra;
selezionare "User Library";
cliccare su "User Library";
cliccare su "New";
in "User Library Name" digitare "ojdbc6", cliccare su "OK";
cliccare "Add External JARs..";
aggiungere il file ojdbc6.jarjar(presente nel percorso “/home/SIES/jboss-eap-6.4.Alpha/modules/oracle/jdbc/main”), cliccare "Finish", infine premere "OK".


Configurazione strumenti di delivery (es. ANT, JENKINS, MAVEN, GRADLE, etc.)
Per quanto riguarda il progetto siesWeb, al fine di distribuire tutto l'applicativo software sviluppato, viene creato un file con estensione .war, acronimo di Web application ARchive, cioèl’archivio usato in Java per raggruppare diversi tipi di files dando vita ad un'applicazione o progetto Web. Per fare ciò, viene utilizzata la funzione di Eclipse Export  WAR file:



attivabile cliccando col tasto destro del mouse sul progetto siesWeb.
Una volta scelta la destinazione di salvataggio del file, premere il tasto “Finish”.



Per quanto riguarda il progetto siesEsecuzione, al fine di effettuare il packaging degli eseguibili e l’esportazione dei sorgenti è stato utilizzato ApacheMaven.Maven utilizza un repository locale per risolvere le dipendenze definite nei progetti. Questo repository locale viene aggiornato e popolato ogni volta che una nuova dipendenza, non presente localmente, viene trovata nel pom.xml del progetto. Per far puntare ad Eclipse il file di configurazione (settings.xml) di Maven occorre eseguire i seguenti step:
Spostarsinel menù "Window"->"Preferences";
Dall’albero di navigazione,selezionare sulla sinistra il ramo "Maven → User Settings";
Nel campo "User Settings", indicare il file di configurazione "settings.xml";
Cliccare su "Apply", infine premere "OK".



Per distribuire tutto l'applicativo software sviluppato, viene creato un file con estensione .war, acronimo di Web Application Archive.
Per fare ciò, viene utilizzata la funzione Run As  Maven install di Eclipse:


Configurazione generale
È stato introdotto uno standard per i commenti utilizzati nel codice, valido per entrambi i progetti, sia per le MAC che per le MEV, secondo l’xml seguente:

Per le MEV:

<?xml version="1.0" encoding="UTF-8"?>
<templates>
<template autoinsert="true" context="java" deleted="false" description="comment on ISSUE MEV" enabled="true" name="MEV">
/* &#13;
 * ISSUE MEV : ${descrizione_intervento}&#13;
 * Numero MEV : ${numero_MEV}&#13;
 * Autore: ${user}&#13;
 * Data: ${date}&#13;
 * Branch: MEV_${numero_MEV}&#13;
 */&#13;
 ${line_selection}${cursor}&#13;
 //***** FINE INTERVENTO MEV_${numero_MEV} *****//&#13;
</template>
</templates>

Per le MAC:

<?xml version="1.0" encoding="UTF-8"?>
<templates>
<template autoinsert="true" context="java" deleted="false" description="comment on ISSUE MAC" enabled="true" name="MAC">
/* &#13;
 * ISSUE MAC : ${descrizione_intervento}&#13;
 * Numero MAC : ${numero_MAC}&#13;
 * Autore: ${user}&#13;
 * Data: ${date}&#13;
 * Branch: MAC_${numero_MAC}&#13;
 */&#13;
 ${line_selection}${cursor}&#13;
 //***** FINE INTERVENTO MAC_${numero_MAC} *****//&#13;
</template>
</templates>

In Eclipse per utilizzare i template comuni per la generazione dei commenti occorre caricare gli xml citati, precedentemente salvati in file .xml, nel seguente modo:

selezionare "Window"->"Preferences";
selezionare nell'albero di navigazione sulla sinistra il ramo "Java → Editor → Templates";
cliccare sul pulsante "Import", aggiungere il file .xml del template;
premere "Apply", infine premere "OK".


Application Server
L’application server utilizzato è Red Hat JBoss Enterprise Application Platform - Version 6.4.0.GA, Server base directory standalone e Configuration file standalone.xml.
Configurazione librerie
I progetti siesWeb e siesEsecuzione hanno bisogno di alcune configurazioni aggiuntive. Nella cartella di installazione del server JBoss “/home/SIES/jboss-eap-6.4.Alpha/modules”, sono presenti due cartelle nominate:



e contenenti librerie aggiuntive a quelle standard.
La cartella config contiene i files necessari alla configurazione per la scrittura dei file di log:



La cartella oracle contiene la libreriaojdbc6.jarche costituisce il driver JDBC lato client di Oracle compatibile con Java 6 e successive:


Configurazione Datasource
Il datasource applicativo deve essere configurato nel file standalone.xml presente nella cartella di installazione del server JBoss: /home/SIES/jboss-eap-6.4.Alpha/standalone/configuration.

<subsystem xmlns="urn:jboss:domain:datasources:1.2">
<datasources>
<datasourcejta="true" jndi-name="java:jboss/jdbc/oracleds" pool-name="oracleds" enabled="true" use-java-context="true" use-ccm="false">
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
Installazione report
Non Applicabile.
Configurazione applicativa
Nel filestandalone.xml del server sono state aggiunte proprietà di sistema aggiuntive rispetto all’originale nativo del server:

<property name="path.properties" value="/var/SIES/CONFIG"/>
<property name="WindwardReports.properties.filename" value="/var/SIES/CONFIG/WindwardReports.properties"/>
<property name="javax.net.ssl.trustStore" value="/var/SIES/CONFIG/certs/sies.jks"/>
<property name="javax.net.ssl.trustStorePassword" value="trustStorePassword"/>
<property name="javax.net.ssl.keyStore" value="/var/SIES/CONFIG/certs/serversies.jks"/>
<property name="javax.net.ssl.keyStorePassword" value="keyStorePassword"/>
<property name="org.apache.tomcat.util.http.Parameters.MAX_COUNT" value="8192"/>
<property name="jdk.tls.client.protocols" value="SSLv2Hello,SSLv3,TLSv1"/>
<property name="javax.net.debug" value="ssl"/>

Inoltre nella sezione “urn:jboss:domain:web:2.2” è stata aggiunta la configurazione per il connettore https, necessarioper installare e configurare il supporto SSL (Secure Sockets Layer) per JBoss.

<subsystem xmlns="urn:jboss:domain:web:2.2" default-virtual-server="default-host" native="false">
            <connector name="http" protocol="HTTP/1.1" scheme="http" socket-binding="http"/>
            <connector name="https" protocol="HTTP/1.1" scheme="https" socket-binding="https" enable-lookups="false" secure="true">
                <ssl name="https" key-alias="1" password="password" certificate-key-file="/home/SIES/jboss-eap-6.4.Alpha/standalone/configuration/serversies.jks" protocol="SSLv2Hello,SSLv3,TLSv1"/>
            </connector>
            <virtual-server name="default-host" enable-welcome-root="false">
                <alias name="localhost"/>
</virtual-server>
</subsystem>
Configurazione specifica
N.A.

Controllo del software
Come strumento di version control viene usato Git.
Repository remoto
Il repository remoto è raggiungibile all’indirizzo https://production.eng.it/gitlab/giustizia-siut/sies/sviluppo, tramite autenticazione e autorizzazione. Soltanto gli utenti autorizzati potranno accedere al codice sorgente.
Repository locale
Per configurare il repository locale è necessario aprire una shell Git Bash (scaricare il programma GIT dal sito https://git-scm.com/downloads) nella posizione desiderata (es. D:\workspaces\sies\sviluppo) ed utilizzare il seguente comando:

git clone -b MEV_20 https://production.eng.it/gitlab/giustizia-siut/sies/sviluppo.git

Il comando clona il branch “MEV_20” (-b MEV_20) del repository remoto (git clone <url>) nella cartella corrente desiderata.
Repository Git in Eclipse
Se il repository locale corrisponde al workspace di Eclipse, nella prospettiva Git (selezionabile e attivabile dal menu "Window > Perspective > Open Perspective > Other…") dal pannello Git Repositoriesrisulterà già censito il repository locale, come nell’immagine seguente:

Se invece il workspace di Eclipse non corrisponde al repository locale, questo va definito, cliccando sull’icona evidenziata nell’immagine seguente (sempre dal pannello Git Repositories) e selezionando il percorso del repository locale:

Strumenti di lavoro
Per le interazioni con il repositoryvengono utilizzati i seguenti strumenti:
- Git Bash (https://git-scm.com/downloads), attraverso istruzioni da riga di comando;
- SourceTree 3.3.8 (https://www.sourcetreeapp.com/), tool visuale utile per fare comparazioni, analizzare i branch e i vari commit;
- Plugin Git integrati in Eclipse, in alternativa a SourceTree.
Struttura repository
Il repository presenta 2 branch perenni:
- mastercontiene l’ultima release consegnata;
- developcontiene l’ultima release consegnata ed è il punto di partenza per gli sviluppi
di MAC e MEV e per i rilasci; può contenere hot-fixes (modifiche banali e lampanti che vanno rilasciate senza dubbio).

Il repository presenta anche branch temporanei:
- mac-otrs-numeroper lo sviluppo delle mac, es. mac-otrs-20200220016;
- MEV_numeroper lo sviluppo delle mev, es. MEV_20;
- major.minor.patchper irilasci, es. release_12.2.1.

Il repository presenta un tag per ogni consegna effettuata, nel formato:
- major.minor.patches. VERSIONE_SIES_12.0.0.

I singoli sviluppi per MAC e MEV vengono effettuati su branch distinti, che una volta testati e collaudati vanno integrati (git merge) nel branch dei rilasci major.minor.patch. Alla fine della fase di test e dopo il rilascio del software viene eseguito il merge del branch di release sui branch master e develop. Successivamente si procede alla cancellazione dei branch temporanei (mac, mev, e release appena integrati nel branch master).
Standard di nomenclatura e regole generali
È stata adottata la seguente convenzione:
- i branch per gli sviluppi delle MAC sono denominati mac-otrs-numero, dove numero corrisponde al numero del ticket su OTRS, es. mac-otrs-20200220016;
- i branch per gli sviluppi delle MEV sono denominati MEV_numero, dove numero corrisponde al numero della scheda, es. MEV_20;
- i branch per i rilasci sono denominati major.minor.patch, dove major.minor.patch corrisponde al numero di versione del software, es. 12.2.1.
Nell’immagine seguente esempi di nomi attribuiti a branch per mac, mev e rilasci, nonché i branch perenni, master e develop:

I commit effettuati sui branch di mac e di mev devono assumere per convenzione il seguente formato:

<nome-branch>: <testo>

Di seguito alcuni esempi:
- mac-otrs-20200220016: modifica controllo sul fascicolo;
- MEV_20: aggiunta proprietà Sede nel dettaglio del provvedimento.

Compilatore e struttura di progetto
N.A.
Struttura del progetto
N.A.
Requisiti ambiente hardware di sviluppo
N.A.

Standard adottati
N.A.