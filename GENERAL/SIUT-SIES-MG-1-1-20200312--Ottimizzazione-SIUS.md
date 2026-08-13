---
uniqueName: siut-sies-mg-1-1-20200312-ottimizzazione-sius
displayName: "SIUT SIES MG 1 1 20200312  Ottimizzazione SIUS"
category: "GENERAL"
tags: []
---

# SIUT-SIES-MG-1.1-20200312- Ottimizzazione SIUS

> **File originale:** `MEV/SCHEDA_006/SIUT-SIES-MG-1.1-20200312- Ottimizzazione SIUS.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A - Sirfin-PA, nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del sistema informativo unitario telematico, la manutenzione degli attuali sistemi dell’area penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo |
| --- | --- |
| Elaborato da | Simone Gioggi, Emma Caporizzo |
| Verificato da | Vito Bufi |
| Approvato da | Paolo Ceccanti |
| Data approvazione | 12/03/2020 |
| Livello di riservatezza | L4 |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 21/02/2020 | Prima Emissione |  |
| 1.1 | 12/03/2020 | Seconda Emissione | Integrazioni Osservazioni in riferimento alla nota:
m_dg.DOG07AR.10/03/2020.0000506.U

Paragrafi:
5 Attività Post-Configurazione
7 Attività post Monitoraggio
Inserite sequenze di stop/start dei servizi in relazione alla release dell’applicativo in esercizio al momento dell’esecuzione del presente piano di attività.
Correzione comandi stop/start relativi alle code.
Correzione percorsi e nomi file su server. |


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
1.3.1	Definizioni	5
1.3.2	Acronimi e abbreviazioni	5
2	Generalità	7
3	Attività Pre-Configurazione	8
4	Attività di Configurazione	9
4.1	Connessione alla jboss-cli (command line interface)	9
4.2	Impostazione livello di debug	9
4.3	Abilitazione CMM (cached connection manager)	9
4.4	Abilitazione use-ccm (cached connection manager) per datasource	9
5	Attività Post-Configurazione	11
6	Attività di Monitoraggio	13
7	Attività post Monitoraggio	14


# Introduzione
## Scopo del documento
Il presente documento viene rilasciato su richiesta dell’Amministrazione, in riferimento. alla nota m_dg.DOG07AR.11/02/2020.0000158.U.
Lo scopo è quello di dettagliare le attività relative alla fase 1 indicata nella Scheda di Intervento nr. 6 del 2019, inerente all’ottimizzazione SIUS Avvocati.
In particolare, si forniscono le istruzioni per la configurazione ed il relativo monitoraggio.
## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
|  | m_dg.DOG07AR.31-07-2019.0000003.U | Richiesta Scheda di Intervento |
|  | SIUT-GEN-SC-1.1-20191015 Scheda intervento SIUS_Avvocati.pdf | Scheda di Intervento |
|  | m_dg.DOG07AR.05/12/2019.0000268.U
m_dg.DOG07AR.20/12/2019.0000309.U | Note Approvazione Scheda |


## Glossario
## Definizioni
| Definizione | Descrizione |
| --- | --- |
| CCM | Cached Connection Manager |
| CLI | Command-Line Interface |

## Acronimi e abbreviazioni
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



# Generalità
Al fine di avviare le attività relative alla fase 1 descritta nella Scheda di Intervento di riferimento, di seguito si riportano gli step da eseguire per la configurazione dell’application server jboss-eap-6.4 e per le successive attività di monitoraggio del log.
# Attività Pre-Configurazione
Come attività preliminare all’intervento in oggetto, è necessario verificare che il server sia nello stato ‘running’.
Ciò perché l’attivazione della jboss-cli (command line interface) presuppone che il server target sia in esecuzione.
Pertanto procedere con i seguenti step:

Aprire una shell linux sul server SIES e loggarsi come utente “root”;
Eseguire il comando: “cd /etc/init.d” e controllare che il server sia in esecuzione tramite il comando: “service jboss status”;

A video deve apparire la seguente dicitura:
jboss  is running

Nella casistica in cui il server sia nel stato “jboss  is not running” , procedere con le istruzioni per l’avvio del server, tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”;

# Attività di Configurazione
Partendo dalla Shell Linux, già aperta per le operazioni di controllo previsti al paragrafo precedente, eseguire le operazioni che seguono:

## Connessione alla jboss-cli (command line interface)

Posizionarsi sotto la cartella: “/opt/jboss-eap-6.4/bin” ed eseguire il comando:
./jboss-cli.sh --connect --controller=xxx.xxx.xxx.xxx

(dove xxx.xxx.xxx.xxx è l’indirizzo IP della macchina che ospita il server Jboss)

A seguito dell’esecuzione del comando appare una dicitura del tipo: “[standalone@ xxx.xxx.xxx.xxx:9999 /]”;

## Impostazione livello di debug

Eseguire il comando:
/subsystem=logging/logger=org.jboss.jca:add(category=org.jboss.jca,level=DEBUG)

Sulla shell apparirà il messaggio:
{"outcome" => "success"}

Il comando imposta il livello di logging del package “org.jboss.jca” a “DEBUG”;

## Abilitazione CMM (cached connection manager)

Eseguire il comando:
/subsystem=jca/cached-connection-manager=cached-connection-manager:write-attribute(name=debug,value=true)

Sulla shell apparirà il messaggio:
{"outcome" => "success"}

L’abilitazione della proprietà Cached Connection Manager (CCM) permetterà di verificare se, le connessioni che l’application server effettua verso la banca dati, vengono utilizzate e rilasciate correttamente dall'applicazione.

## Abilitazione use-ccm (cached connection manager) per datasource

Eseguire il comando:
/subsystem=datasources/data-source=oracleds:write-attribute(name=use-ccm,value=true)

Sulla shell apparirà il messaggio:
{
"outcome" => "success",
"response-headers" => {
"operation-requires-reload" => true,
"process-state" => "reload-required"
}
}

Terminate le operazioni di configurazione dall’attuale path “[standalone@ xxx.xxx.xxx.xxx:9999 /]”, ossia sulla cli di jboss, eseguire il comando exit.

# Attività Post-Configurazione
Affinché le attività di configurazione abbiano effetto, occorre proseguire con lo ‘stop’ e successivo ‘start’ del sistema.

Si riportano di seguito le istruzioni da eseguire per lo stop dei servizi, indicandone la diversa sequenza in relazione alla release di SIES installata in esercizio al momento dell’esecuzione delle attività riportate nel presente documento.

Nel caso di release 11.2.5 e/o 11.2.6, procedere allo stop come segue:
Partendo dalla Shell Linux, già aperta per le operazioni di configurazione (nel caso fosse stata chiusa riaprire la shell linux sul server SIES e loggarsi come utente “root”), eseguire il comando: “cd /etc/init.d” e fermare il processo di gestione delle code tramite il comando: “./imq stop”;

Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”;

Nel caso di release 12.0.0 e/o successive, procedere allo stop come segue:
Partendo dalla Shell Linux, già aperta per le operazioni di configurazione (nel caso fosse stata chiusa riaprire la shell linux sul server SIES e loggarsi come utente “root”), eseguire il comando: “cd /etc/init.d” e fermare il server jboss tramite il comando: “service jboss stop”. Controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”;

Fermare il processo di gestione delle code tramite il comando: “./imq stop”;

Proseguire quindi come segue:
Posizionarsi sotto la cartella:“/opt/jboss-eap-6.4/standalone” e cancellare le cartelle “data”, “log” e “tmp” (se esistenti).

Si riportano di seguito le istruzioni da eseguire per lo start dei servizi, indicandone la diversa sequenza in relazione alla release di SIES installata in esercizio al momento dell’esecuzione delle attività riportate nel presente documento.

Nel caso di release 11.2.5 e/o 11.2.6, procedere allo start come segue:
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”;

Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.

Nel caso di release 12.0.0 e/o successive, procedere allo start come segue:
Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”;

Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
Proseguire quindi come segue:
Posizionarsi sotto la cartella “opt/jboss-eap-6.4/standalone/configuration” e verificare che nel file standalone.xml siano presenti i seguenti frammenti xml:

In corrispondenza del tag  xml <subsystem xmlns="urn:jboss:domain:logging:1.x">

Deve essere presente il tag <logger> per la category = org.jboss.jca impostato a DEBUG, nel seguente modo:

<logger category="org.jboss.jca">
<level name="DEBUG"/>
</logger>;

In corrispondenza del tag xml <subsystem xmlns="urn:jboss:domain:jca:1.x">

Deve essere presente il tag <cached-connection-manager/> impostato con la proprietà debug = true, nel seguente modo:
<cached-connection-manager debug="true"/>;

In corrispondenza del tag xml <subsystem xmlns="urn:jboss:domain:datasources:1.x">

Deve essere presente il tag <datasource> impostato con la proprietà  use-ccm="true";

# Attività di Monitoraggio
Per monitorare e controllare il corretto funzionamento dell’attivazione del Cached Connection Manager bisogna esaminare il file server.log presente nella cartella “/opt/jboss-eap-6.4/standalone/log”.

N.B.: nella stessa cartella vengono conservati anche i file server.log dei giorni precedenti; se il file server.log riporta il resoconto del giorno corrente, il file server.log.AAAA.MM.GG riporterà il resoconto del giorno indicato dall’estensione AAAA = anno, MM = mese, GG = giorno (esempio: server.log.20200101 si riferisce alla tracciatura avvenuta il primo gennaio).

Si riporta di seguito un esempio di tracciatura nel file di log dell’errore intercettato dal Cached Connection Manager:

INFO  [org.jboss.jca.core.api.connectionmanager.ccm.CachedConnectionManager] (http-localhost/127.0.0.1:8080-4) IJ000100: Closing a connection for you. Please close them yourself: org.jboss.jca.adapters.jdbc.jdk6.WrappedConnectionJDK6@3f6fb5f6: java.lang.Throwable: STACKTRACE
at org.jboss.jca.core.connectionmanager.ccm.CachedConnectionManagerImpl.registerConnection(CachedConnectionManagerImpl.java:269)
at org.jboss.jca.core.connectionmanager.AbstractConnectionManager.allocateConnection(AbstractConnectionManager.java:541)
at org.jboss.jca.adapters.jdbc.WrapperDataSource.getConnection(WrapperDataSource.java:143)
at f3b.controller.GenericController.getDBConnection(GenericController.java:92) [classes:]
at siap.siep.statistiche.controller.StatisticheSiepController.ExCountEstraiStatisticheFogliComplementari(StatisticheSiepController.java:94) [classes:]
at siap.siep.statistiche.action.ActRicercaFogliComplementari.handlePagination(ActRicercaFogliComplementari.java:93) [classes:]
at siap.siep.statistiche.action.ActRicercaFogliComplementari.processRequest(ActRicercaFogliComplementari.java:73) [classes:]
at org.apache.jsp.jsp.Main_jsp._jspService(Main_jsp.java:229).

Il file di log attivato con le indicazioni del cached connection manager potrebbe crescere notevolmente: per monitorare il file di consiglia di seguire i seguenti passi:

Dopo 30 minuti dall’attivazione, verificare la dimensione del file
In base alla dimensione fare una proiezione di crescita
Eventualmente svuotare il file stesso, riportando la sua dimensione a 0, previo backup del file

Per ovviare a possibili sovra dimensionamenti del file di log si può prevedere uno script shell, tramite pianificazione dei comandi (crontab) dei sistemi operativi UNIX, che in funzione dei tempi di riempimento del FileSystem effettuerà una copia sotto un altro FileSystem e azzererà il file di log del monitoring.

# Attività post Monitoraggio
Al termine delle operazioni di monitoraggio, stabilite pari a 3 giorni di utilizzo dell’applicativo con le opzioni per il debug attivate, procedere con le operazioni di ‘restore’ delle opzioni alla situazione di partenza, seguendo le istruzioni a seguire.

Si riportano di seguito le istruzioni da eseguire per lo stop dei servizi, indicandone la diversa sequenza in relazione alla release di SIES installata in esercizio al momento dell’esecuzione delle attività riportate nel presente documento.

Nel caso di release 11.2.5 e/o 11.2.6, procedere allo stop come segue:
Aprire una shell linux sul server SIES e loggarsi come utente “root”;
Eseguire il comando: “cd /etc/init.d” e fermare il processo di gestione delle code tramite il comando: “./imq stop”;
Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”;

Nel caso di release 12.0.0 e/o successive, procedere allo stop come segue:
Aprire una shell linux sul server SIES e loggarsi come utente “root”;
Eseguire il comando: “cd /etc/init.d” e fermare il server jboss tramite il comando: “service jboss stop”. Controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”;
Fermare il processo di gestione delle code tramite il comando: “./imq stop”;

Proseguire quindi come segue:
Posizionarsi sotto la cartella “opt/jboss-eap-6.4/standalone/configuration” editare il file standalone.xml eliminando i seguenti frammenti xml:

In corrispondenza del tag  xml <subsystem xmlns="urn:jboss:domain:logging:1.x">

Eliminare  il seguente frammento:

<logger category="org.jboss.jca">
<level name="DEBUG"/>
</logger>;

In corrispondenza del tag xml <subsystem xmlns="urn:jboss:domain:jca:1.x">

Eliminare la dicitura debug="true"  nel tag che segue:
<cached-connection-manager debug="true"/>

Il tag deve rimanare nel seguente stato  <cached-connection-manager/>

In corrispondenza del tag xml <subsystem xmlns="urn:jboss:domain:datasources:1.x">

nel tag <datasource>  modificare la proprietà  use-ccm impostandola a false nel seguente modo:
use-ccm="false"

Posizionarsi sotto la cartella “/opt/jboss-eap-6.4/standalone” e cancellare le cartelle “data”, “log” e “tmp” (se esistenti).

Si riportano di seguito le istruzioni da eseguire per lo start dei servizi, indicandone la diversa sequenza in relazione alla release di SIES installata in esercizio al momento dell’esecuzione delle attività riportate nel presente documento.

Nel caso di release 11.2.5 e/o 11.2.6, procedere allo start come segue:
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”;

Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.

Nel caso di release 12.0.0 e/o successive, procedere allo start come segue:
Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”;

Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.