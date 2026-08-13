---
uniqueName: siut-sie-pr-1-0-20200407-piano-di-rilascio-avvocat
displayName: "SIUT SIE PR 1 0 20200407 Piano di rilascio AVVOCATURA"
category: "GENERAL"
tags: []
---

# SIUT-SIE-PR-1.0-20200407-Piano di rilascio AVVOCATURA

> **File originale:** `Avvocatura-SIES/Rilascio_MEV20_2020-04-07/Documentazione_AVVOCATURA/SIUT-SIE-PR-1.0-20200407-Piano di rilascio AVVOCATURA.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
Piano di rilascio Avvocatura Rel. 2.0.0 
 
 
 
 
 
 
 
 
 
Versione 1.0 del 07/04/2020

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 2/12 
 
 
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
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 3/12 
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
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 4/12 
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
ATTIVITÀ PRELIMINARI ...................................................................................................................... 11 
6.2 
INSTALLAZIONE LATO DB ORACLE ....................................................................................................... 11 
6.2.1 
ESECUZIONE SCRIPT ....................................................................................................................... 11 
6.3 
INSTALLAZIONE APPLICAZIONE ............................................................................................................ 12 
6.3.1 
DEPLOY APPLICAZIONE .................................................................................................................. 12

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 5/12 
1 Introduzione 
1.1 Scopo del documento 
Il documento descrive il piano di rilascio della release 2.0.0 del sistema AVVOCATURA. In particolare, il 
presente rilascio attiene agli interventi realizzati nell’ambito dell’obiettivo di riferimento [RIF1.]. 
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
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 6/12 
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
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 7/12 
2 Generalità 
Il presente documento riporta l’elenco degli oggetti in rilascio e le relative istruzioni di installazione in 
ambiente di esercizio.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 8/12 
3 Identificazione degli elementi rilasciati 
Supporto
n°
Oggetti:
Rev.
Del
Portale Fornitura 
1 
SIUT > 07 - MEV > 020 - MEV Avvocatura Sede > 03 
- 
Verifica 
di 
Conformità 
> 
Software 
> 
Rilascio_MEV20_AVVOCATURA_SW_2020-04-
07.zip 
1.0 
07/04/2020 
Portale Fornitura 
2 
SIUT > 07 - MEV > 020 - MEV Avvocatura Sede > 03 
- Verifica di Conformità > Documentazione > 
Rilascio_MEV20_AVVOCATURA_DOC_2020-04-
07.zip 
1.0 
07/04/2020 
Note-osservazioni

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 9/12 
4 Riferimenti degli oggetti del rilascio 
 
4.1 Riferimenti per gli elementi in primo rilascio 
Nome Oggetto 
Scheda Intervento 
Specifica Intervento 
Scheda n. 20 
SIUT-SIE-SC-1.0-
20191002_Scheda_Intervento_n.20_Avvocatur
a_SIES_Sede.pdf 
SIUT-SIE-SI-1.3-20200317-
Specifiche_Intervento_Avvocatura.pdf 
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
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 10/12 
5 Dettaglio degli elementi software oggetto del rilascio 
Rilascio_MEV20_AVVOCATURA_SW_2020-04-07.zip 
Nome File 
Path 
Dimensione (MB) 
Motivazione-riferimento 
aggiorna_db.zip 
Database 
0,004 
Script per l’aggiornamento della 
Banca Dati
avvocatura.war 
Applicazione 
26 
Eseguibile dell’applicazione 
sorgenti.zip 
Sorgenti 
6,5 
Sorgenti software 
Rilascio_MEV20_AVVOCATURA_DOC_2020-04-07.zip 
Nome File 
Path 
Dimensione (MB) 
Motivazione-riferimento 
documentazione 
Documentazione 
- 
SIUT-SIE-PR-1.0-20200407-Piano di 
rilascio AVVOCATURA.pdf; 
SIUT-SIE-CT-1.0-20200407-Allegato-
al piano-test AVVOCATURA.xlsx; 
SIUT-SIE-PT-1.0-20200407-Piano dei 
Test AVVOCATURA.pdf; 
SIUT-SIE-PV-1.0-20200407-Piano 
delle verifiche AVVOCATURA.pdf; 
SIUT-SIE-AR-1.0-20200407-Modello 
Dati - AVVOCATURA.pdf; 
SIUT-SIE-MU-1.2-20200407-
Manuale 
Utente-
Avvocatura_SIES.pdf; 
SIUT-SIE-MG-1.0-20200407- 
Definizione 
Ambiente 
sviluppo 
AVVOCATURA.pdf; 
Note-osservazioni

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 11/12 
6 Installazione 
6.1 Attività Preliminari 
1. Verificare che il tnsnames.ora sia presente sul db server e configurato correttamente per 
l’accesso al DB da aggiornare. 
6.2 Installazione lato DB Oracle 
6.2.1 Esecuzione Script 
(E’ consigliato che tale procedura venga eseguita da personale competente in ambiente Oracle) 
Il documento elenca i passi necessari per la corretta esecuzione. 
 
Collegarsi come utente oracle sul db server. 
Impostare le variabili ORACLE_HOME e ORACLE_SID (se non già settate) eseguendo le seguenti 
istruzioni: 
 
(il percorso varia in base all’installazione di oracle) 
export ORACLE_HOME=/u01/app/oracle/product/12.1.0/dbhome_1 
 
(sostituire xxxxx col nome dell’istanza oracle) 
export ORACLE_SID=xxxxx 
 
aggiungere nella variabile PATH il valore $ORACLE_HOME/bin 
 
Esempio: 
 
PATH=$PATH:/u01/app/oracle/product/12.1.0/dbhome_1/bin 
 
Prima di avviare la procedura, accertarsi che sia il listener che il database siano avviati. 
 
Copiare il file aggiorna_db.zip  in una qualsiasi cartella e scompattarlo, il sistema crea la cartella 
aggiorna_db. 
Creare sul server DB una cartella AVV_2_0_0 sotto la directory /home/oracle/ 
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/AVV_2_0_0/ 
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella AVV_2_0_0 tramite il 
comando: 
chmod 777 AVV_2_0_0 
 
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale 
richiesta: 
================================================== 
Riassunto dei dati immessi per questa installazione 
Nome ....................: avvsies 
================================================== 
SID Oracle ..............: xxxx

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-PR-1.0-20200407 Piano di rilascio AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 12/12 
Utente_SIES..............: avvsies 
Password_SIES............: xxxx 
 
Nella cartella appena creata (AVV_2_0_0), lanciare il comando ./aggiorna_db.sh 
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/AVV_2_0_0/log/ in cui si 
può constatare l’esito dell’esecuzione. 
6.3 Installazione applicazione 
6.3.1 Deploy Applicazione 
Attenzione!! La variabile $JBOSS_HOME rappresenta il path di installazione dell’Enterprise Application 
Server 6.4.0 GA. (es: /opt/jboss-eap-6.4/) 
 
1 Aprire una shell linux sul server SIES e loggarsi come utente “root”. 
2 Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione 
dell’istruzione tramite il comando: “service jboss status” (già indicato nelle attività preliminari). 
3 Scaricare i files “avvocatura.war” sul server SIES ed eseguire le seguenti operazioni: 
a. posizionarsi sotto la cartella: 
“$JBOSS_HOME/standalone/deployments”; 
b. cancellare il vecchio eseguibile (se esistente) “avvocatura.war” e la copia deployata 
“avvocatura.war.deployed”; 
c. copiare, nello stesso percorso, il nuovo eseguibile “avvocatura.war”; 
d. posizionarsi sotto la cartella:  
“$JBOSS_HOME/standalone”; 
e. cancellare le cartelle “data”, “log” e “tmp” (se esistenti). 
 
Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti 
seguendo le istruzioni ai punti 3.b e 3.e. All’avvio, infatti, tali cartelle verranno ricreate. 
 
4 Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione 
dell’istruzione tramite il comando: “service jboss status”.