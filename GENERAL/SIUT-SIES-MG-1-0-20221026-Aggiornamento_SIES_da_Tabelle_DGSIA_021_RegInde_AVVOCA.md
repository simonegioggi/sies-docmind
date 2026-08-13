---
uniqueName: siut-sies-mg-1-0-20221026-aggiornamentosiesdatabel
displayName: "SIUT SIES MG 1 0 20221026 Aggiornamento SIES da Tabelle DGSIA 021 RegInde AVVOCA"
category: "GENERAL"
tags: []
---

# SIUT-SIES-MG-1.0-20221026-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_AVVOCATURA

> **File originale:** `MEV/SCHEDA_021/Docs/SIUT-SIES-MG-1.0-20221026-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_AVVOCATURA.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia  
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi Direzione 
Generale per i Sistemi Informativi Automatizzati  
  
  
Aggiornamento AVVOCATURA da Tabelle DGSIA 
MEV 021_2019 RegInde 
 
  
  
  
  
  
  
  
  
  
Versione 1.0 del 26/10/2022

SIUT-SIES-MG-1.0-20221026-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_AVVOCATURA   Ver. 1.0 del26/10/2022   Pag. 2/10 
Ministero della Giustizia  
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi  
Direzione Generale per i Sistemi Informativi Automatizzati  
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

SIUT-SIES-MG-1.0-20221026-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_AVVOCATURA   Ver. 1.0 del26/10/2022   Pag. 3/10 
Ministero della Giustizia  
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi  
Direzione Generale per i Sistemi Informativi Automatizzati  
Approvazioni 
 
Nominativo 
Funzione 
Elaborato da 
Engineering 
RTI 
Verificato da 
Vito Bufi 
Responsabile Manutenzione Sistemi attuali
Approvato da 
Paolo Ceccanti 
Responsabile Unico Fornitura 
Data approvazione 
26/10/2022 
 
Livello di riservatezza 
L4 
 
  
Elenco versioni 
Versione 
Data  
Motivo 
Modifica 
1.0 
26/10/2022 
Prima emissione 
 
  
Lista di distribuzione 
Nominativo 
Organizzazione 
Ufficio 
Funzione 
Ing. Giovanni Malesci 
Amministrazione 
 
Responsabile Unico Procedimento 
Dott. Oris Orlando 
Amministrazione 
 
Direttore Esecutivo Contratto 
Paolo Ceccanti 
RTI 
 
Responsabile Unico Fornitura 
Sergio Tamburrini 
RTI 
 
Organization Manager 
Vito Bufi 
RTI 
 
Responsabile Manutenzione Sistemi attuali 
Francesco Rosati 
RTI 
 
Responsabile Manutenzione Correttiva 
Referente Qualità e Sicurezza 
Andrea Salvaggio 
RTI 
 
Responsabile Progetto Sistema Unitario 
Referente Tecnico 
Antonio Iacobelli 
RTI 
 
Responsabile Supporto Specialistico 
Antonella Damiani 
RTI 
 
Responsabile Centro di Competenza 
Fabio Gattamorta 
RTI 
 
Referente PMO e Qualità 
Alessandro Falleni 
RTI 
 
Referente sicurezza 
Andrea Castorino 
RTI 
 
Referente Applicativo Gestore Fascicolo 
Documentale

SIUT-SIES-MG-1.0-20221026-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_AVVOCATURA   Ver. 1.0 del26/10/2022   Pag. 4/10 
Ministero della Giustizia  
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi  
Direzione Generale per i Sistemi Informativi Automatizzati  
  
INDICE DEI CONTENUTI  
1  
Introduzione .......................................................................................................................................... 5 
1.1 Scopo del documento ....................................................................................................................................... 5 
1.2 Riferimenti ........................................................................................................................................................ 5 
1.3 Glossario ........................................................................................................................................................... 5 
1.3.2 Acronimi e abbreviazioni ............................................................................................................................... 5 
2  
Generalità .............................................................................................................................................. 7 
3  
Descrizione delle Attività per messa in esercizio ...................................................................................... 8 
3.1 Procedura di Aggiornamento Tabella SIES (utente “avvsies”) da Tabella fissa DGSIA ..................................... 8 
3.2 Istruzioni per lancio eseguibili file.sh ................................................................................................................ 8 
3.2.1 Attività di installazione ed esecuzione procedura batch Bonifica Difensori ................................................. 8 
3.3 
Procedura Aggiornamento tabelle COMUNI e STATI di SIES-AVVOCATURA .............................................. 9 
3.3.1 STEP 1 ............................................................................................................................................................. 9 
3.3.2 STEP 2 ........................................................................................................................................................... 10

SIUT-SIES-MG-1.0-20221026-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_AVVOCATURA   Ver. 1.0 del26/10/2022   Pag. 5/10 
Ministero della Giustizia  
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi  
Direzione Generale per i Sistemi Informativi Automatizzati  
1  Introduzione  
1.1 Scopo del documento  
Il presente documento viene rilasciato con lo scopo di dettagliare le attività preliminari prima della messa in 
esercizio della MEV 021_2019 RegInde e sono relative all’aggiornamento Tabelle SIES (utente “avvsies”) da 
Tabelle fisse DGSIA. 
In particolare, nel seguente documento, si forniscono le istruzioni da seguire ed i relativi controlli da effettuare 
in caso di riesecuzione della procedura di allineamento tabelle SIES (utente “avvsies”) da Tabelle Fisse DGSIA.  
Tutti gli scripts e le procedure plsql di seguito menzionate sono contenute nella cartella ../aggiorna_TF che si 
ottiene scompattando il file Aggiornamento Tabelle Fisse.zip, che contiene anche le cartelle csv e xls, all’interno 
delle quali sono presenti i files .xls/.cvs di seguito menzionati. 
1.2 Riferimenti  
Riferimento 
Nome Documento
Descrizione Documento 
RIF1. 
SIUT-SIE-PR-1.2-20220124-Piano_di_rilascio_021_RegInde_SIES 
Piano di rilascio 
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

SIUT-SIES-MG-1.0-20221026-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_AVVOCATURA   Ver. 1.0 del26/10/2022   Pag. 6/10 
Ministero della Giustizia  
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi  
Direzione Generale per i Sistemi Informativi Automatizzati  
Sigla 
Descrizione 
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

SIUT-SIES-MG-1.0-20221026-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_AVVOCATURA   Ver. 1.0 del26/10/2022   Pag. 7/10 
Ministero della Giustizia  
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi  
Direzione Generale per i Sistemi Informativi Automatizzati  
2  Generalità  
Le attività descritte indicano i passi necessari all’allineamento delle tabelle SIES-AVVOCATURA 
avvsies.COMUNI ed avvsies.STATI, e sono preliminari alle attività di installazione del software relativo alla 
MEV 021_2019 RegInde di SIES.

SIUT-SIES-MG-1.0-20221026-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_AVVOCATURA   Ver. 1.0 del26/10/2022   Pag. 8/10 
Ministero della Giustizia  
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi  
Direzione Generale per i Sistemi Informativi Automatizzati  
3  Descrizione delle Attività per messa in esercizio 
Le attività descritte nel paragrafo 3.1 si articolano su scripts .sql e procedures plsql, contenuti nel pacchetto 
aggiorna_db_AVVOCATURA.zip, che va estratto ottenendo la cartella ..\aggiorna_db_AVVOCATURA. 
 
3.1 Procedura di Aggiornamento Tabella SIES (utente “avvsies”) da Tabella fissa DGSIA 
Di seguito l’attività da eseguire per l’aggiornamento delle tabelle SIES (utente “avvsies”) da quelle fornite da 
DGSIA, ricevute tramite e-mail di Anna.Maffucci@giustizia.it a Vito.Bufi@eng.it del 6/11/2020 09:06. 
3.2 Istruzioni per lancio eseguibili file.sh 
1) Aprire una shell linux sul server SIES e loggarsi come utente “root”; 
2) Eseguire il comando: “cd /etc/init.d”; 
3) Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione 
dell’istruzione tramite il comando: “service jboss status”; 
4) Fermare il processo di gestione delle code tramite il comando: “./imq stop”; 
3.2.1 Attività di installazione ed esecuzione procedura batch Bonifica Difensori 
Per le attività lato DB: 
1) Collegarsi come utente oracle sul db server; 
2) Impostare le variabili ORACLE_HOME e ORACLE_SID (se non già settate) eseguendo le seguenti istruzioni: 
a) (il percorso varia in base all’installazione di oracle) 
export ORACLE_HOME=/u01/app/oracle/product/12.1.0/dbhome_1 
b) (sostituire xxxxx col nome dell’istanza oracle) 
export ORACLE_SID=xxxxx 
3) Aggiungere nella variabile PATH $ORACLE_HOME/bin 
Esempio: PATH=$PATH:/u01/app/oracle/product/12.1.0/dbhome_1/bin 
Prima di avviare la procedura, accertarsi che sia il listener che il database siano avviati. 
4) Copiare il file aggiorna_db_AVVOCATURA.zip in una qualsiasi cartella e scompattarlo. il sistema crea la 
cartella aggiorna_db_AVVOCATURA; 
5) Creare sul server DB una cartella MEV-2019_21_AVVOCATURA sotto la directory /home/oracle/; 
6) Copiare la cartella aggiorna_db_AVVOCATURA nella cartella /home/oracle/MEV-2019_21_AVVOCATURA/. 
7) Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella MEV-2019_21_AVVOCATURA 
tramite il comando: 
chmod 777 MEV-2019_21_AVVOCATURA 
 
In fase di esecuzione degli script, di seguito riportati, saranno chiesti alcuni parametri; di seguito un esempio di 
tale richiesta (dove xx è la sigla del distretto di appartenenza, per esempio siesrm per Roma): 
================================================== 
Riassunto dei dati immessi per questa installazione 
Nome ....................: sies 
==================================================

SIUT-SIES-MG-1.0-20221026-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_AVVOCATURA   Ver. 1.0 del26/10/2022   Pag. 9/10 
Ministero della Giustizia  
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi  
Direzione Generale per i Sistemi Informativi Automatizzati  
SID Oracle ..............: sies 
Utente_SIES..............: siesxx 
Password_SIES............: siesxx 
 
8) Posizionarsi nel percorso /home/oracle/MEV-2019_21_AVVOCATURA/ e lanciare sequenzialmente i 
comandi, indicati nel par. 3.3. 
3.3 Procedura Aggiornamento tabelle COMUNI e STATI di SIES-AVVOCATURA 
Di seguito le attività da eseguire per l’aggiornamento delle tabelle avvsies.COMUNI e avvsies.STATI alle tabelle 
fisse COMUNE e STATO-NAZIONE fornite dalla DGSIA. 
N.B. In caso di esito negativo di una o più verifiche riportate nei successivi STEP, affinché si possa ripristinare il 
database alla situazione iniziale, utilizzare lo snapshot del DB creato nel paragrafo 3.2 del documento “SIUT-
SIES-MG-1.6-20221026-Istruzioni_Bonifica_Difensori_021_RegInde_SIES.pdf”. 
3.3.1 STEP 1 
Verificare tramite il comando pwd di trovarsi nel percorso /home/oracle/MEV-2019_21_AVVOCATURA/ ed 
eseguire il comando 
 
./aggiorna_db_AVVOCATURA.sh 
 
Dettaglio del file: 
1. XAT_SALVA_TABELLE_AVVOCATURA.prc = Crea e compila la procedure XAT_SALVA_TABELLE_ 
AVVOCATURA, che esegue una copia di backup delle tabelle avvsies.COMUNI e avvsies.STATI nelle 
tabelle avvsies.COMUNI_SXALLTF e avvsies.STATI_SXALLTF. 
2. ALTER_COMUNI_STATI_AVVOCATURA.sql = lo script .sql aggiunge all’attuale struttura della tabella 
avvsies.COMUNI le nuove colonne COD_CATASTALE_COMUNE, DATA_AGGIORNAMENTO_COMUNE 
e DATA_FINE_VALIDITA_COMUNE; aggiunge all’attuale struttura della tabella avvsies.STATI le nuove 
colonne COD_STATO_ISO, COD_ISTAT_STATO, COD_CATASTALE e DATA_FINE_VALIDITA. 
3. AGGIORNA_COMUNI_AVVOCATURA.prc = La procedure effettua l’aggiornamento della tabella 
avvsies.COMUNI, cancellando  i preesistenti 8112 records e ne inserisce 13327. 
4. AGGIORNA_STATI_AVVOCATURA.sql = Lo script cancella dalla tabella avvsies.STATI e la ricrea 
caricando i nuovi records. Il dominio conterrà 269 records a fronte dei 200 precedenti. 
 
Per ogni punto precedente sono riportati di seguito gli eventuali controlli per verificare la corretta esecuzione di 
aggiorna_db_AVVOCATURA.sh: 
 
- 
Verificare che nel file /home/oracle/MEV-2019_21_AVVOCATURA/log/Log_Aggiorna_DB.log non siano 
riportati errori oracle. 
 
Collegarsi al database con utenza siesxx (dove xx è la sigla del distretto di appartenenza, per esempio siesrm per 
Roma): 
 
1. 
E’ 
possibile 
verificare 
la 
corretta 
esecuzione 
della 
procedura 
XAT_SALVA_TABELLE_AVVOCATURA.prc eseguendo la query: 
 
        SELECT * FROM USER_TABLES A WHERE A.TABLE_NAME LIKE '%_SXALLTF' ORDER BY TABLE_NAME

SIUT-SIES-MG-1.0-20221026-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_AVVOCATURA   Ver. 1.0 del26/10/2022   Pag. 10/10 
Ministero della Giustizia  
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi  
Direzione Generale per i Sistemi Informativi Automatizzati  
        che deve dare come esito anche le seguenti tabelle avvsies.COMUNI_SXALLTF e  
avvsies.STATI_SXALLTF. 
 
2. 
Per verificare l’aggiornamento effettuato al terzo punto eseguire quanto di seguito 
 
SELECT COUNT(*) FROM avvsies.COMUNI            
il risultato deve essere 13327. 
 
3. 
Per verificare l’aggiornamento effettuato al quarto punto eseguire quanto di seguito 
 
SELECT COUNT (*) FROM avvsies.STATI 
 
il risultato deve essere  269. 
 
In caso di esito positivo delle su riportate attività LE TABELLE DI BACKUP CREATE AL PUNTO 1 NON DEVONO 
ESSERE CANCELLATE MA VANNO MANTENUTE PER ALMENO 6 MESI, PER PERMETTERE EVENTUALI ATTIVITÀ DI 
VERIFICA. 
 
Alla fine di queste attività di aggiornamento, passare alle attività di Installazione del Software descritte al  
paragrafo 6.3 del documento “SIUT-SIES-PR-1.3-20221026-Piano_di_Rilascio_021_RegInde_AVVOCATURA.pdf”. 
3.3.2 STEP 2 
In caso di errori verificatisi nell’esecuzione di uno degli step precedenti, a seguito indicazioni dell’help desk del 
fornitore, è necessario ripristinare lo snapshot effettuato all’inizio delle attività di aggiornamento della Base 
Dati.