---
uniqueName: siut-sies-pr-1-0-20200228-piano-di-rilascio
displayName: "SIUT SIES PR 1 0 20200228 Piano di rilascio"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20200228-Piano di rilascio

> **File originale:** `RILASCIO_12.0.0/SIUT-SIES-PR-1.0-20200228-Piano di rilascio.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
Piano di rilascio SIES Rel. 12.0.0 
 
 
 
 
 
 
 
 
 
Versione 1.0 del 28/02/2020

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200228 Piano di rilascio 
Ver. 1.0 del 28/02/2020 
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
 
 SIUT-SIES-PR-1.0-20200228 Piano di rilascio 
Ver. 1.0 del 28/02/2020 
Pag. 3/13 
Approvazioni 
Nominativo
Elaborato da
Simone Gioggi
Verificato da
Vito Bufi
Approvato da
Paolo Ceccanti
Data approvazione
28/02/2020
Livello di riservatezza
L4
 
Elenco versioni 
Versione
Data 
Motivo
Modifica
1.0
28/02/2020
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
 
 SIUT-SIES-PR-1.0-20200228 Piano di rilascio 
Ver. 1.0 del 28/02/2020 
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
GENERALITÀ ............................................................................................................................ 8 
3 
IDENTIFICAZIONE DEGLI ELEMENTI RILASCIATI ......................................................................... 9 
4 
RIFERIMENTI DEGLI OGGETTI DEL RILASCIO ........................................................................... 10 
4.1 
RIFERIMENTI PER GLI ELEMENTI IN PRIMO RILASCIO .................................................................................. 10 
4.2 
RIFERIMENTI ANOMALIA (MAC) ......................................................................................................... 10 
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
 
 SIUT-SIES-PR-1.0-20200228 Piano di rilascio 
Ver. 1.0 del 28/02/2020 
Pag. 5/13 
1 
Introduzione 
1.1 Scopo del documento 
Il documento descrive il piano di rilascio della release 12.0.0 del sistema SIES. 
In particolare, tale rilascio è il risultato del merge delle due release di seguito indicate: 
• 
11.2.5 
• 
11.3 
la cui installazione è propedeutica alla release oggetto della presente consegna. 
 
Si rimanda, per qualsiasi informazione eccedente quanto riportato nel presente, alla documentazione dei singoli 
rilasci su citati, parte dei quali vengono riportati nella tabella Riferimenti. 
1.2 Riferimenti 
Riferimento 
Nome Documento 
Descrizione Documento 
1
SIUT-SIES-CT-1.0-20200207-Allegato-al-
piano-test.xls 
Allegato Piano dei Test (Rilascio Vers. 11.2.5)
2
SIUT-SIES-PT-1.0-20200207-Piano-dei-
Test.pdf 
Piano dei Test (Rilascio Vers. 11.2.5)
3
SIUT-SIES-PR-1.0-20200207-Piano di rilascio 
SIES.pdf 
Piano di Rilascio (Rilascio Vers. 11.2.5)
4
SIGI_PNL_PT-2019 
07 
02 
-1.0_MEV 
PROBLEMA CODE JMS.xls 
Piano dei Test
(Rilascio 
11.3 
- 
INTERVENTO_PROBLEMA_DBI) 
5
SIGI_PNL_PT_2019 07 02_1.0_MEV 16 -
Interoperabilità SIEP-NSC - Cumulo - Piano di 
Test.xls 
Piano dei Test
(Rilascio 11.3 – MEV_16_CUMULO) 
6
SIGI_PNL_PT-2019 07 02 - 1.0_MEV 39 -
Completamento Misure Sicurezza.xls 
Piano dei Test (Rilascio 11.3 – MEV_39)
7
SIGI_PNL_PT-2019 07 02 -1.0_MEV 56.xls
Piano dei Test (Rilascio 11.3 – MEV_56)
8
SIGI_PNL_PT-2019 07 02 -1.0_MEV 65.xls
Piano dei Test (Rilascio 11.3 – MEV_65)
9
SIGI_PNL_PT-2019 07 02 -1.0_MEV 66.xls
Piano dei Test (Rilascio 11.3 – MEV_66)
10
SIGI_PNL_PT-2019 07 02 -1.0_MEV 67.xls
Piano dei Test (Rilascio 11.3 – MEV_67)
 
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200228 Piano di rilascio 
Ver. 1.0 del 28/02/2020 
Pag. 6/13 
Sigla
Descrizione
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
Manutenzione Evolutiva
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200228 Piano di rilascio 
Ver. 1.0 del 28/02/2020 
Pag. 7/13 
Sigla
Descrizione
UTA
Utente Generico Amministrazione
VPN
Virtual Private Network

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200228 Piano di rilascio 
Ver. 1.0 del 28/02/2020 
Pag. 8/13 
2 
Generalità 
Il presente documento riporta l’elenco degli oggetti in rilascio e le relative istruzioni di installazione in ambiente 
di esercizio.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200228 Piano di rilascio 
Ver. 1.0 del 28/02/2020 
Pag. 9/13 
3 
Identificazione degli elementi rilasciati 
Supporto
n°
Oggetti:
Rev. del
Portale della Fornitura 
1 
SIUT > 06 - Rilasci Software > SIES > Rilascio V12.0.0
2020-02-28 
1.0 
28/02/2020 
Note-osservazioni

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200228 Piano di rilascio 
Ver. 1.0 del 28/02/2020 
Pag. 10/13 
4 
Riferimenti degli oggetti del rilascio 
4.1 Riferimenti per gli elementi in primo rilascio 
N.A. 
4.2 Riferimenti Anomalia (MAC) 
N.A. 
4.3 Riferimenti Change Request (MAD/MEV) 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200228 Piano di rilascio 
Ver. 1.0 del 28/02/2020 
Pag. 11/13 
5 
Dettaglio degli elementi sw oggetto del rilascio 
Nome File 
Path 
Dimensione (MB) Motivazione-riferimento 
aggiorna_db.zip
Database
0,002
Script per il versionamento
template.zip
Template
0,024
Aggiornamento template:
SIEP_MA_DETERM_DET.rtf 
SIEP_RP_OSRDP.rtf 
sies.war
Applicazione
103
Eseguibile dell’applicazione
sorgenti.zip
Sorgenti
100
Sorgenti software
documentazione.zip
Documentazione
0,1
SIUT-SIES-PR-1.0-20200228-
Piano di rilascio.pdf 
Note-osservazioni

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200228 Piano di rilascio 
Ver. 1.0 del 28/02/2020 
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
 
Copiare il file aggiorna_db.zip  in una qualsiasi cartella e scompattarlo, il sistema crea la cartella aggiorna_db 
Creare sul server DB una cartella V_12 sotto la directory /home/oracle/ 
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12/ 
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12 tramite il comando: 
chmod 777 V_12 
 
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta: 
================================================== 
Riassunto dei dati immessi per questa installazione 
Nome ....................: sies 
================================================== 
SID Oracle ..............: sies 
Utente_SIES..............: siesxx 
Password_SIES............: siesxx 
 
Nella cartella appena creata (V_12), lanciare il comando ./aggiorna_db.sh 
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12/log/ in cui si può constatare 
l’esito dell’esecuzione.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20200228 Piano di rilascio 
Ver. 1.0 del 28/02/2020 
Pag. 13/13 
6.3 Installazione applicazione 
6.3.1 Deploy Applicazione 
1 
Aprire una shell linux sul server SIES e loggarsi come utente “root”. 
2 
Eseguire il comando: “cd /etc/init.d” 
3 
Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione 
dell’istruzione tramite il comando: “service jboss status” (già indicato nelle attività preliminari). 
4 
Fermare il processo di gestione delle code tramite il comando: “./imq stop” (già indicato nelle attività 
preliminari). 
5 
Scaricare i files “sies.war” sul server SIES ed eseguire le seguenti operazioni: 
a. posizionarsi sotto la cartella: 
“/opt/jboss-eap-6.4/standalone/deployments”; 
b. cancellare il vecchio eseguibile (se esistente) “sies.war” e la copia deployata “sies.war.deployed”; 
c. copiare, nello stesso percorso, il nuovo eseguibile “sies.war”; 
d. posizionarsi sotto la cartella:  
“/opt/jboss-eap-6.4/standalone”; 
e. cancellare le cartelle “data”, “log” e “tmp” (se esistenti). 
6 
Copiare il file contenuto nella cartella template\siep\ma 
nella cartella “/var/SIES/template/siep/ma” sovrascrivendo quello precedente. 
7 
Copiare il file contenuto nella cartella template\siep\rp 
nella cartella “/var/SIES/template/siep/rp” sovrascrivendo quello precedente. 
 
Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le 
istruzioni ai punti 5.b e 5.e. All’avvio, infatti, tali cartelle verranno ricreate. 
 
8 
Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”. 
Per verificare la partenza delle code si può analizzare il file di log, presente nel percorso 
“/var/mq/instances/imqbroker/log”, “log.txt” controllando al suo interno la presenza della dicitura “Broker 
'imqbroker@nomemacchina:7676' pronto”. 
9 
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione 
dell’istruzione tramite il comando: “service jboss status”.