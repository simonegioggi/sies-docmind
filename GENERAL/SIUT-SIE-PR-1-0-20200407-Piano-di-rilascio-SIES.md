---
uniqueName: siut-sie-pr-1-0-20200407-piano-di-rilascio-sies
displayName: "SIUT SIE PR 1 0 20200407 Piano di rilascio SIES"
category: "GENERAL"
tags: []
---

# SIUT-SIE-PR-1.0-20200407-Piano di rilascio SIES

> **File originale:** `Avvocatura-SIES/Rilascio_MEV20_2020-04-07/Documentazione_SIES/SIUT-SIE-PR-1.0-20200407-Piano di rilascio SIES.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
Piano di rilascio Sies Rel. 12.1.0 
 
 
 
 
 
 
 
 
 
Versione 1.0 del 07/04/2020

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio SIES 
Ver. 1.0 del 07/04/2020 
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
Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del 
contratto CIG 73479643B7 per lo “Sviluppo del Sistema 
Informativo Unitario Telematico, la manutenzione degli 
attuali sistemi dell’area Penale del Ministero della 
Giustizia e servizi correlati. Lotto 1”.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio SIES 
Ver. 1.0 del 07/04/2020 
Pag. 3/13 
Approvazioni 
 
Nominativo 
Elaborato da
Domenico Nania, Simone Gioggi
Verificato da 
Vito Bufi 
Approvato da 
Paolo Ceccanti 
Data approvazione
07/04/2020
Livello di riservatezza 
L4 
 
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio SIES 
Ver. 1.0 del 07/04/2020 
Pag. 4/13 
INDICE DEI CONTENUTI 
1 
INTRODUZIONE .......................................................................................................................... 5 
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
GENERALITÀ ............................................................................................................................... 7 
3 
IDENTIFICAZIONE DEGLI ELEMENTI RILASCIATI ............................................................................ 8 
4 
RIFERIMENTI DEGLI OGGETTI DEL RILASCIO ................................................................................ 9 
4.1 
RIFERIMENTI PER GLI ELEMENTI IN PRIMO RILASCIO .................................................................................... 9 
4.2 
RIFERIMENTI ANOMALIA (MAC) ........................................................................................................... 9 
4.3 
RIFERIMENTI CHANGE REQUEST (MAD/MEV) ........................................................................................ 9 
5 
DETTAGLIO DEGLI ELEMENTI SOFTWARE OGGETTO DEL RILASCIO ............................................. 10 
6 
INSTALLAZIONE ........................................................................................................................ 11 
6.1 
ATTIVITÀ PRELIMINARI ....................................................................................................................... 11 
6.2 
INSTALLAZIONE LATO DB ORACLE ........................................................................................................ 11 
6.2.1 
ESECUZIONE SCRIPT ....................................................................................................................... 11 
6.3 
INSTALLAZIONE APPLICAZIONE ............................................................................................................ 12 
6.3.1 
DEPLOY APPLICAZIONE .................................................................................................................. 12

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio SIES 
Ver. 1.0 del 07/04/2020 
Pag. 5/13 
1 Introduzione 
1.1 Scopo del documento 
Il documento descrive il piano di rilascio della release 12.1.0 del sistema SIES. In particolare, il presente 
rilascio attiene agli interventi realizzati nell’ambito dell’obiettivo di riferimento [RIF1.]. 
1.2 Riferimenti 
Riferimento
Nome Documento
Descrizione Documento
RIF1. 
 
SIUT-SIE-SC-1.0-20191002_Scheda 
di 
intervento 
n.20_Avvocatura_SIES_Sede  
Scheda Intervento 
RIF2. 
SIUT-SIE-SI-1.3-20200317-Specifiche_Intervento_Avvocatura
Specifiche Intervento
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio SIES 
Ver. 1.0 del 07/04/2020 
Pag. 6/13 
Sigla 
Descrizione 
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
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio SIES 
Ver. 1.0 del 07/04/2020 
Pag. 7/13 
2 Generalità 
Il presente documento riporta l’elenco degli oggetti in rilascio e le relative istruzioni di installazione in 
ambiente di esercizio.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio SIES 
Ver. 1.0 del 07/04/2020 
Pag. 8/13 
3 Identificazione degli elementi rilasciati 
Supporto 
n° 
Oggetti: 
Rev. 
Del 
Portale Fornitura
1
SIUT > 07 - MEV > 020 - MEV Avvocatura Sede 
> 03 - Verifica di Conformità> Software > 
Rilascio_MEV20_SIES_SW_2020-04-07.zip 
1.0
07/04/2020
Portale Fornitura 
2 
SIUT > 07 - MEV > 020 - MEV Avvocatura Sede 
> 03 - Verifica di Conformità> Documentazione 
> Rilascio_MEV20_SIES_DOC_2020-04-07.zip 
1.0 
07/04/2020 
Note-osservazioni

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio SIES 
Ver. 1.0 del 07/04/2020 
Pag. 9/13 
4 Riferimenti degli oggetti del rilascio 
 
4.1 Riferimenti per gli elementi in primo rilascio 
Nome Oggetto 
Scheda Intervento 
Specifica Intervento 
Scheda n. 20 
SIUT-SIE-SC-1.0-
20191002_Scheda_Intervento_n.20_Avvocatura_S
IES_Sede.pdf 
SIUT-SIE-SI-1.3-20200317-
Specifiche_Intervento_Avvocatura.p
df 
Note-osservazioni 
 
 
4.2 Riferimenti Anomalia (MAC) 
Rif. Ticket OTRS 
Sede/Ufficio 
Descrizione segnalazione 
Descrizione intervento 
- 
- 
- 
- 
 
4.3 Riferimenti Change Request (MAD/MEV) 
Prot. Richiesta o  
Rif. Ticket OTRS 
Scheda Intervento 
Specifica Intervento 
- 
- 
-

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio SIES 
Ver. 1.0 del 07/04/2020 
Pag. 10/13 
5 Dettaglio degli elementi software oggetto del rilascio 
Rilascio_MEV20_SIES_SW_2020-04-07.zip 
Nome File 
Path 
Dimensione (MB)
Motivazione-riferimento 
aggiorna_db.zip
Database
0,015
Script per il versionamento e 
l’aggiornamento della Banca Dati
template.zip 
Template 
0,017 
Aggiornamento template: 
SIUS_ST_STAMPAFASCICOLO_AV
VOCATURA.rtf 
sies.war
Applicazione
103
Eseguibile dell’applicazione
sorgenti.zip
Sorgenti
99
Sorgenti software
Rilascio_MEV20_SIES_DOC_2020-04-07.zip 
Nome File 
Path 
Dimensione (MB)
Motivazione-riferimento 
Documentazione
Documentazione
-
SIUT-SIE-PR-1.0-20200407-Piano 
di rilascio SIES.pdf; 
SIUT-SIE-AR-2.1-20200407-
Descrizione Servizi Web.pdf; 
SIUT-SIE-MG-1.0-20200407- 
Definizione Ambiente sviluppo 
SIES.pdf 
Note-osservazioni

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio SIES 
Ver. 1.0 del 07/04/2020 
Pag. 11/13 
6 Installazione 
6.1 Attività Preliminari 
1. Arrestare il servizio MessageQueue e stoppare il webserver jboss (dopo avere avvertito gli 
utenti degli uffici che lavorano sul SIES). 
2. Verificare che il tnsnames.ora sia presente sul db server e configurato correttamente per 
l’accesso al DB da aggiornare. 
6.2 Installazione lato DB Oracle 
6.2.1 Esecuzione Script 
(E’ consigliato che tale procedura venga eseguita da personale competente in ambiente Oracle) 
Il documento elenca i passi necessari per la corretta esecuzione. 
 
 Collegarsi come utente oracle sul db server. 
 Impostare le variabili ORACLE_HOME e ORACLE_SID (se non già settate) eseguendo le seguenti 
istruzioni: 
 
(il percorso varia in base all’installazione di oracle) 
export ORACLE_HOME=/u01/app/oracle/product/12.1.0/dbhome_1 
 
(sostituire xxxxx col nome dell’istanza oracle) 
export ORACLE_SID=xxxxx 
 
 aggiungere nella variabile PATH $ORACLE_HOME/bin 
 
Esempio: 
 
PATH=$PATH:/u01/app/oracle/product/12.1.0/dbhome_1/bin 
 
Prima di avviare la procedura, accertarsi che sia il listener che il database siano avviati. 
 
1. Copiare il file aggiorna_db.zip in una qualsiasi cartella e scompattarlo, il sistema crea la cartella 
aggiorna_db. 
2. Creare sul server DB una cartella V_12_1_0 sotto la directory /home/oracle/ 
3. Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_1_0/ 
4. Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_1_0 tramite il 
comando: 
chmod 777 V_12_1_0 
 
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale 
richiesta: 
================================================== 
Riassunto dei dati immessi per questa installazione 
Nome ....................: sies

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio SIES 
Ver. 1.0 del 07/04/2020 
Pag. 12/13 
================================================== 
SID Oracle ..............: sies 
Utente_SIES..............: siesxx 
Password_SIES............: siesxx 
 
5. Nella cartella appena creata (V_12_1_0), lanciare il comando ./aggiorna_db.sh 
6. Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_1_0/log/ in 
cui si può constatare l’esito dell’esecuzione. 
7. N.B. Le segnalazioni del tipo  
a. 
ORA-00001: violata restrizione di unicità 
b. 
ORA-00955: name is already used by an existing object 
c. 
Cartella log già presente 
d. 
ORA-04043: object does not exist 
 
sono da considerarsi warning e non errori. 
8. Accedere ad oracle (con qualsiasi strumento ad. toad, developer…) come utente siesxx e 
compilare tutte le procedure e i package che non risultano compilate. 
ATTENZIONE: la procedura SUPER_SOGGETTO_PREGR e il package CARICA_RES potrebbero 
restare non compilate: non è da considerarsi errore. 
 
6.3 Installazione applicazione 
6.3.1 Deploy Applicazione 
1 Aprire una shell linux sul server SIES e loggarsi come utente “root”. 
2 Eseguire il comando: “cd /etc/init.d” 
3 Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione 
dell’istruzione tramite il comando: “service jboss status” (già indicato nelle attività preliminari). 
4 Fermare il processo di gestione delle code tramite il comando: “./imq stop” (già indicato nelle 
attività preliminari). 
5 Scaricare i files “sies.war” sul server SIES ed eseguire le seguenti operazioni: 
a. posizionarsi sotto la cartella: 
“/opt/jboss-eap-6.4/standalone/deployments”; 
b. cancellare il vecchio eseguibile (se esistente) “sies.war” e la copia deployata 
“sies.war.deployed”; 
c. copiare, nello stesso percorso, il nuovo eseguibile “sies.war”; 
d. posizionarsi sotto la cartella:  
“/opt/jboss-eap-6.4/standalone”; 
e. cancellare le cartelle “data”, “log” e “tmp” (se esistenti). 
6 Copiare il file contenuto nella cartella template\sius\st 
nella cartella “/var/SIES/template/sius/st” sovrascrivendo quello precedente. 
 
Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti 
seguendo le istruzioni ai punti 5.b e 5.e. All’avvio, infatti, tali cartelle verranno ricreate.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio SIES 
Ver. 1.0 del 07/04/2020 
Pag. 13/13 
7 Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”. 
Per verificare la partenza delle code si può analizzare il file di log, presente nel percorso 
“/var/mq/instances/imqbroker/log”, “log.txt” controllando al suo interno la presenza della dicitura 
“Broker 'imqbroker@nomemacchina:7676' pronto”. 
8 Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione 
dell’istruzione tramite il comando: “service jboss status”.