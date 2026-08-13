---
uniqueName: siut-sies-pr-1-0-20200207-piano-di-rilascio-sies
displayName: "SIUT SIES PR 1 0 20200207 Piano di rilascio SIES"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20200207-Piano di rilascio SIES

> **File originale:** `RILASCIO_11.2.5/SIUT-SIES-PR-1.0-20200207-Piano di rilascio SIES.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
Piano di rilascio 
 
 
 
 
 
 
 
 
 
Versione 1.0 del 07/02/2020

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200207 Piano di rilascio SIES 
Ver. 1.0 del 07/02/2020 
Pag. 2/13 
 
 
 
Il 
presente 
documento 
è 
stato 
redatto 
con 
la 
collaborazione 
del 
RTI 
Engineering 
Ingegneria 
Informatica S.p.A - Sirfin-PA, nell’ambito del contratto 
CIG 73479643B7 
per 
lo 
“Sviluppo 
del 
sistema 
informativo unitario telematico, la manutenzione degli 
attuali sistemi dell’area penale del Ministero della 
Giustizia e servizi correlati. Lotto 1”.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200207 Piano di rilascio SIES 
Ver. 1.0 del 07/02/2020 
Pag. 3/13 
Approvazioni 
Nominativo
Elaborato da
Domenico Nania, Simone Gioggi
Verificato da
Fabio Gattamorta
Approvato da
Vito Nicola Bufi
Data approvazione
07/02/2020
Livello di riservatezza
L4
 
Elenco versioni 
Versione
Data 
Motivo
Modifica
1.0
07/02/2020
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200207 Piano di rilascio SIES 
Ver. 1.0 del 07/02/2020 
Pag. 4/13 
 
INDICE DEI CONTENUTI 
1 
INTRODUZIONE ....................................................................................................................... 5 
1.1 
SCOPO DEL DOCUMENTO ...................................................................................................................... 5 
1.2 
RIFERIMENTI ...................................................................................................................................... 5 
1.3 
GLOSSARIO ........................................................................................................................................ 5 
1.3.1 
DEFINIZIONI ................................................................................................................................... 5 
1.3.2 
ACRONIMI E ABBREVIAZIONI .............................................................................................................. 5 
2 
GENERALITÀ ............................................................................................................................ 7 
3 
IDENTIFICAZIONE DEGLI ELEMENTI RILASCIATI ......................................................................... 8 
4 
RIFERIMENTI DEGLI OGGETTI DEL RILASCIO ............................................................................. 9 
4.1 
RIFERIMENTI PER GLI ELEMENTI IN PRIMO RILASCIO .................................................................................... 9 
4.2 
RIFERIMENTI ANOMALIA (MAC) ........................................................................................................... 9 
4.3 
RIFERIMENTI CHANGE REQUEST (MAD/MEV) ...................................................................................... 10 
5 
DETTAGLIO DEGLI ELEMENTI SW OGGETTO DEL RILASCIO ...................................................... 11 
6 
INSTALLAZIONE ..................................................................................................................... 12 
6.1 
ATTIVITÀ PRELIMINARI ....................................................................................................................... 12 
6.2 
INSTALLAZIONE LATO DB ORACLE ........................................................................................................ 12 
6.2.1 
ESECUZIONE SCRIPT ....................................................................................................................... 12 
6.3 
INSTALLAZIONE APPLICAZIONE ............................................................................................................. 13 
6.3.1 
DEPLOY APPLICAZIONE ................................................................................................................... 13

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200207 Piano di rilascio SIES 
Ver. 1.0 del 07/02/2020 
Pag. 5/13 
1 
Introduzione 
1.1 Scopo del documento 
Il documento descrive il piano di rilascio del sistema SIES. 
Gli interventi in oggetto sono rilasciati nell’ambito della release 11.2.5 SIES. 
 
1.2 Riferimenti 
Riferimento 
Nome Documento 
Descrizione Documento 
RIF1
SIUT-SIES-PT-1.0-20200207-Piano-dei-
Test.pdf 
Il documento descrive il piano dei test per la 
verifica della risoluzione dei ticket indicati 
nel presente Piano di Rilascio 
RIF2
SIUT-SIES-CT-1.0-20200207-Allegato-al-
piano-test.xls 
Il documento riporta l'elenco dei test 
eseguiti per la verifica della risoluzione delle 
anomalie 
 
1.3 Glossario 
1.3.1 Definizioni 
Definizione
Descrizione
1.3.2 Acronimi e abbreviazioni 
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200207 Piano di rilascio SIES 
Ver. 1.0 del 07/02/2020 
Pag. 6/13 
Sigla
Descrizione
MEV
Manutenzione EVolutiva
OWASP
Open Web Application Security Project
PA
Pubblica Amministrazione
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
 
 SIUT-SIES-PR-1.0-20200207 Piano di rilascio SIES 
Ver. 1.0 del 07/02/2020 
Pag. 7/13 
2 
Generalità 
Il presente documento riporta l’elenco delle funzionalità modificate con gli interventi eseguiti dal servizio di 
manutenzione rilasciati con il presente rilascio.  
Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200207 Piano di rilascio SIES 
Ver. 1.0 del 07/02/2020 
Pag. 8/13 
3 
Identificazione degli elementi rilasciati 
Supporto
n°
Oggetti:
Rev. del
Portale della Fornitura 
1 
Company Home > SIUT > 06 - Rilasci Software > SIES > 
Rilascio V11.2.5 2020-02-07 
1.0 
07/02/2020 
Note-osservazioni

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200207 Piano di rilascio SIES 
Ver. 1.0 del 07/02/2020 
Pag. 9/13 
4 
Riferimenti degli oggetti del rilascio 
4.1 Riferimenti per gli elementi in primo rilascio 
N.A. 
4.2 Riferimenti Anomalia (MAC) 
Rif. Ticket OTRS 
Sede/Ufficio 
Descrizione segnalazione Descrizione intervento 
202001070115
Procura Generale presso 
la Corte d'Appello 
Stampa Certificato di 
esecuzione (stato di 
esecuzione) da altro 
Ufficio 
Modificato template:
StatoEsecuzione.rtf 
Modificata classe Java: 
StatoEsecuzioneLA.java 
20200107012
Torino/Tribunale
Ordinario 
Deposito e trasmissione 
ordinanza GE 
Modificate classi Java:
siap.siep.notifica.controller.NotificaC
ontroller.java; 
siap.sige.provvedimento.action.ActIn
serisciDataDeposito.java; 
siap.sige.provvedimento.action.ActM
odificaDataDeposito.java 
Modificate pagine JSP: 
ModificaDestinatari.jsp; 
LoadModificaDataDeposito.jsp 
20190805017
Catania/Procura 
Generale presso la Corte 
d'Appello 
Mancata attribuzione dei 
giorni di detrazione 
rimedi risarcitori 
Modificate classi Java:
ActInserisciOSRimediRisarcitori.java; 
CreatorStatoEsecuzione.java; 
LicenzaLibanticipataSqlDAO.java; 
LicenzaPeriodiLibAnticipataController
.java; 
OrdineScarcerazioneController.java; 
StampaController.java; 
StatoEsecuzioneLA.java 
Modificate pagine JSP: 
DettaglioComunicazioneReclamoRim
ediRisarcitori.jsp; 
DettaglioComunicazioneRimediRisarci
tori.jsp; 
DettaglioOSRimediRisarcitori.jsp; 
20200110017
Torino/Procura Generale 
presso la Corte d'Appello
Cancellazione periodi di 
presofferto 
Modificate classi Java:
Siap.siep.modulocumulo.dao.MisuraC
autelareCumuloSqlDAO.java; 
siap.siep.istruttoriacumulo.controller.
IstruttoriaCumuloController.java 
20191210013
Torino/Procura della 
Repubblica presso il 
Tribunale 
Errore del sistema nel 
calcolo pena 
Modificate classi Java:
OrdineEsecuzioneController.java; 
AnnotazioneManualeSqlDAO.java 
20200110018
Torino/Procura Generale 
presso la Corte d'Appello
Cumulo - richieste al 
giude dell'esecuzione - 
sorveglianza 
Modificata pagina JSP:
LoadModRichiestaGERevocaBenefici.j
sp

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200207 Piano di rilascio SIES 
Ver. 1.0 del 07/02/2020 
Pag. 10/13 
Rif. Ticket OTRS 
Sede/Ufficio 
Descrizione segnalazione Descrizione intervento 
20200109018
Napoli/Tribunale di 
Sorveglianza 
Presa in carico atti 
pervenuti 
Modificata classe Java:
siap.sius.fascicolo.controller.Fascicolo
SiusUDSController.java 
20200124013
Mantova/Ufficio di 
Sorveglianza 
Errore iscrizione 
procedimento 
Modificata classe Java:
siap.sius.fascicolo.controller.Fascicolo
SiusUDSController.java 
 
4.3 Riferimenti Change Request (MAD/MEV) 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200207 Piano di rilascio SIES 
Ver. 1.0 del 07/02/2020 
Pag. 11/13 
5 
Dettaglio degli elementi sw oggetto del rilascio 
Nome File 
Path 
Dimensione (MB) Motivazione-riferimento 
aggiorna_db.zip
Database
Script per risoluzione delle 
anomalie 
template.zip
Template
Nuovi template per risoluzione 
anomalie segnalate: 
StatoEsecuzione.rtf 
sies.war
Applicazione
104
 
Eseguibile dell’applicazione
sorgenti.zip
Sorgenti
100
Sorgenti software
documentazione.zip
Documentazione
SIUT-SIES-CT-1.0-20200207-
Allegato-al-piano-test.xls 
 
SIUT-SIES-PR-1.0-20200207-
Piano di rilascio SIES.pdf 
 
SIUT-SIES-PT-1.0-20200207-
Piano-dei-Test.pdf 
Note-osservazioni

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200207 Piano di rilascio SIES 
Ver. 1.0 del 07/02/2020 
Pag. 12/13 
6 
Installazione 
6.1 Attività Preliminari 
1 - Arrestare il servizio MessageQueue e stoppare il webserver jboss (dopo avere avvertito gli utenti degli uffici 
che lavorano sul SIES). 
2 - Verificare che il tnsnames.ora sia presente sul db server e configurato correttamente per l’accesso al DB da 
aggiornare. 
6.2 Installazione lato DB Oracle 
6.2.1 Esecuzione Script 
(E’ consigliato che tale procedura venga eseguita da personale competente in ambiente Oracle) 
Il documento elenca i passi necessari per la corretta esecuzione. 
 
Collegarsi come utente oracle sul db server. 
Impostare le variabili ORACLE_HOME e ORACLE_SID (se non già settate) eseguendo le seguenti istruzioni: 
 
(il percorso varia in base all’installazione di oracle) 
export ORACLE_HOME=/u01/app/oracle/product/12.1.0/dbhome_1 
 
(sostituire xxxxx col nome dell’istanza oracle) 
export ORACLE_SID=xxxxx 
 
aggiungere nella variabile PATH $ORACLE_HOME/bin 
 
Esempio: 
 
PATH=$PATH:/u01/app/oracle/product/12.1.0/dbhome_1/bin 
 
Prima di avviare la procedura, accertarsi che sia il listener che il database siano avviati. 
 
Copiare il file aggiorna_db.zip  in una qualsiasi cartella e scompattarlo, il sistema crea la cartella aggiorna_db. 
Creare sul server DB una cartella V_11_2_5 sotto la directory /home/oracle/ 
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/ V_11_2_5/ 
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_11_2_5 tramite il comando: 
chmod 777 V_11_2_5 
 
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta: 
================================================== 
Riassunto dei dati immessi per questa installazione 
Nome ....................: sies 
================================================== 
SID Oracle ..............: sies 
Utente_SIES..............: siesxx 
Password_SIES............: siesxx 
 
Nella cartella appena creata (V_11_2_5), lanciare il comando ./aggiorna_db.sh 
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/ V_11_2_5/log/ in cui si può 
constatare l’esito dell’esecuzione.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200207 Piano di rilascio SIES 
Ver. 1.0 del 07/02/2020 
Pag. 13/13 
N.B. Le segnalazioni del tipo  
ORA-00001: violata restrizione di unicità 
ORA-00955: name is already used by an existing object 
Cartella log già presente 
ORA-04043: object does not exist 
 
sono da considerarsi warning e non errori. 
 
Accedere ad oracle (con qualsiasi strumento tipo toad, developer…) come utente siesxx e compilare tutte le 
procedure e i package che non risultano compilate. 
ATTENZIONE: la procedura SUPER_SOGGETTO_PREGR e il package CARICA_RES potrebbero restare non 
compilate: non è da considerarsi errore. 
6.3 Installazione applicazione 
6.3.1 Deploy Applicazione 
1. Aprire una shell linux sul server SIES e loggarsi come utente “root”. 
2. Eseguire il comando: “cd /etc/init.d” e fermare il processo di gestione delle code tramite il comando: 
“./imq stop” (già indicato nelle attività preliminari). 
3. Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione 
dell’istruzione tramite il comando: “service jboss status” (già indicato nelle attività preliminari). 
4. Scaricare i files “sies.war” sul server SIES ed eseguire le seguenti operazioni: 
a. posizionarsi sotto la cartella: 
“/opt/jboss-eap-6.4/standalone/deployments”; 
b. cancellare il vecchio eseguibile (se esistente) “sies.war” e la copia deployata 
“sies.war.deployed”; 
c. copiare, nello stesso percorso, il nuovo eseguibile “sies.war”; 
d. posizionarsi sotto la cartella: 
“/opt/jboss-eap-6.4/standalone”; 
e. cancellare le cartelle “data”, “log” e “tmp” (se esistenti). 
5. Copiare il file contenuto nella cartella template\import 
nella cartella “/var/SIES/template/import” sovrascrivendo quello precedente. 
 
Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le 
istruzioni ai punti 4.b e 4.e. All’avvio, infatti, tali cartelle verranno ricreate. 
 
6. Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione 
dell’istruzione tramite il comando: “service jboss status”. 
7. Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.