---
uniqueName: siut-sie-ml-1-0-20200407-modellodatiavvocatura
displayName: "SIUT SIE ML 1 0 20200407 Modello Dati AVVOCATURA"
category: "GENERAL"
tags: []
---

# SIUT-SIE-ML-1.0-20200407-Modello_Dati_AVVOCATURA

> **File originale:** `Docs_CMDBuild_SIES+SIUS_Avvocati/SIUT-SIE-ML-1.0-20200407-Modello_Dati_AVVOCATURA.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
Modello Dati 
 
 
 
 
 
Versione 1.0 del 07/04/2020

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-AR-1.0-20200407-Modello Dati - AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 2/18 
 
 
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
Informatica S.p.A. 
& 
Sirfin-PA 
S.r.l. 
nell’ambito 
del 
contratto CIG 73479643B7 per lo “Sviluppo del Sistema 
Informativo Unitario Telematico, la manutenzione degli 
attuali sistemi dell’area Penale del Ministero della 
Giustizia e servizi correlati. Lotto 1”.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-AR-1.0-20200407-Modello Dati - AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 3/18 
 
APPROVAZIONI 
 
Nominativo 
Funzione 
Elaborato da 
Cosimo Eugenio Bortone 
Analista/ Programmatore SQL 
Verificato da 
Vito Bufi 
Responsabile Manutenzione Sistemi 
attuali 
Approvato da 
Paolo Ceccanti 
Responsabile Unico Fornitura 
Data approvazione 
07/04/2020 
 
Livello di riservatezza 
L3 
 
 
ELENCO VERSIONI 
Versione 
Data 
Motivo 
Modifica 
1.0 
07/04/2020 
Prima Emissione 
 
 
LISTA DI DISTRIBUZIONE 
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
 
 
SIUT-SIE-AR-1.0-20200407-Modello Dati - AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 4/18 
 
INDICE DEI CONTENUTI 
1 
INTRODUZIONE ..................................................................................................................... 6 
1.1 
SCOPO DEL DOCUMENTO ............................................................................................................... 6 
1.2 
RIFERIMENTI ............................................................................................................................... 6 
1.3 
GLOSSARIO ................................................................................................................................. 6 
1.3.1 DEFINIZIONI ................................................................................................................................ 6 
1.3.2 ACRONIMI E ABBREVIAZIONI .......................................................................................................... 6 
2 
ORGANIZZAZIONE DEL DOCUMENTO ..................................................................................... 9 
3 
MODELLI DEI DATI ............................................................................................................... 10 
3.1 
SCHEMA LOGICO ........................................................................................................................ 10 
3.1.1 ELENCO TABELLE SCHEMA LOGICO ................................................................................................. 10 
DISTRETTI ...................................................................................................................................... 10 
COMUNI ........................................................................................................................................ 11 
STATI ............................................................................................................................................. 11 
SERVIZI .......................................................................................................................................... 11 
ATTIVITA’ RICERCHE ..................................................................................................................... 12 
UFFICI DISTRETTO SEDE ............................................................................................................... 12 
TIPO UFFICIO................................................................................................................................. 12 
3.2 
SCHEMA FISICO ......................................................................................................................... 13 
3.2.1 DESCRIZIONE SCHEMA FISICO....................................................................................................... 13 
3.2.2 SCHEMA FISICO – DIAGRAMMA ................................................................................................... 14 
3.2.3 ELENCO TABELLE SCHEMA FISICO ................................................................................................... 15 
DISTRETTI ...................................................................................................................................... 15 
COMUNI ........................................................................................................................................ 16 
STATI ............................................................................................................................................. 16 
SERVIZI .......................................................................................................................................... 16

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-AR-1.0-20200407-Modello Dati - AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 5/18 
 
ATTIVITA_RICERCHE ..................................................................................................................... 17 
UFFICI_DISTRETTO ........................................................................................................................ 17 
TIPO_UFFICIO ............................................................................................................................... 18

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-AR-1.0-20200407-Modello Dati - AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 6/18 
 
1 
Introduzione 
1.1 Scopo del documento 
Il presente documento descrive la banca dati del sistema di Consultazione dei Procedimenti SIUS 
relativamente allo schema AVVSIES. In particolare si descrive il modello logico e fisico dei dati, 
esplicitando per le tabelle descritte i campi, le descrizioni, la tipologia e il dominio. 
Per tutte le tabelle è stata prevista un’attività di pre-caricamento dati. I dati delle tabelle sono 
caricati a partire dai contenuti ad oggi presenti sulle tabelle dei sistemi SIES. Le tabelle interessate 
sono: DISTRETTI, COMUNI, UFFICI E STATI. 
Si sottolinea che l’attività di caricamento dati, così come ogni successivo aggiornamento dei dati, 
sarà fatto esclusivamente per mezzo di script sql. Non è prevista una gestione diversa. Gli script di 
aggiornamento fanno riferimento all’eventuale necessità di aggiungere un nuovo record in ognuna 
delle tabelle previste per il Sistema di Consultazione. 
In merito all’attività di attivazione dei distretti, sarà anche in questo caso necessario uno script per 
gestirne l’attivazione. 
Le interrogazioni alle tabelle presenti nella banca dati saranno possibili solo tramite sql. 
1.2 Riferimenti 
Riferimento 
Nome Documento 
Descrizione Documento 
 
 
 
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-AR-1.0-20200407-Modello Dati - AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 7/18 
 
Sigla 
Descrizione 
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
OSWAP 
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-AR-1.0-20200407-Modello Dati - AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 8/18 
 
Sigla 
Descrizione 
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
 
 
SIUT-SIE-AR-1.0-20200407-Modello Dati - AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 9/18 
 
2 
Organizzazione del documento 
 
In questo paragrafo si elencano brevemente i paragrafi che compongono il documento in oggetto: 
 
 3.1 schema logico del database del sistema di Consulazione Procedimenti SIUS 
 3.2 schema fisico  del database del sistema di Consulazione Procedimenti SIUS

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-AR-1.0-20200407-Modello Dati - AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 10/18 
 
3 
Modelli dei dati  
3.1 Schema Logico 
In questo paragrafo si descrive lo schema logico del sistema di Consultazione Procedimenti SIUS, dando 
un’indicazione puntuale sui campi presenti nelle opportune tabelle corredate da descrizioni, tipologie, 
dominio. 
3.1.1 Elenco Tabelle schema logico 
Si riporta il dettaglio delle entità utilizzate nello schema indicando per ciascuna entità il nome colonna, la 
descrizione della colonna, la tipologia, il suo dominio. 
Le tabelle descritte sono le seguenti: 
• DISTRETTI 
• COMUNI 
• STATI 
• SERVIZI 
• ATTIVITA’ RICERCHE 
• UFFICI DISTRETTO SEDE 
• TIPO_UFFICIO 
 
DISTRETTI 
 
Nome Colonna 
Descrizione della Colonna 
Dominio 
1 
Descrizione 
Descrizione del Distretto 
Alfabetico 
2 
Dns 
Domain Name Service della macchina Server 
del Distretto 
Alfanumerico 
3 
Data inizio attivazione 
Data di inizio attivazione distretto 
Data 
4 
Data fine attivazione 
Data di fine attivazione distretto 
Data

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-AR-1.0-20200407-Modello Dati - AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 11/18 
 
COMUNI 
 
Nome Colonna 
Descrizione della Colonna 
Dominio 
1 
Descrizione 
Descrizione del Comune 
Alfabetico 
2 
Cap 
Codice di avviamento postale 
Numerico 
3 
Data Caricamento  
Data di caricamento 
Data 
4 
Codice sede giudiziaria 
Codice della sede giudiziaria 
Alfanumerico 
5 
Flag validità 
Flag Validità S/N 
Alfabetico 
 
STATI 
 
Nome Colonna 
Descrizione della Colonna 
Dominio 
1 
Descrizione 
Descrizione dello Stato 
Alfabetico 
2 
Data Caricamento  
Data di caricamento 
Data 
3 
Flag validità 
Flag Validità S/N 
Alfabetico 
 
SERVIZI 
 
Nome Colonna 
Descrizione della Colonna 
Dominio 
1 
Descrizione servizio 
Descrizione generica del servizio Web 
Alfabetico 
2 
Nome servizio 
Nome del servizio da invocare 
Alfanumerico 
3 
Versione 
Versione del servizio 
Alfanumerico 
 
Il contenuto della tabella è il seguente: 
Id_Servizio Descrizione_Servizio 
Nome_Servizio 
Version 
1 
Dettaglio del Procedimento 
/ConsultazioneSIUS/DettaglioProcedimento?wsdl 
1.0 
2 
Dettaglio del Decreto 
/ConsultazioneSIUS/DettaglioDecreto?wsdl 
1.0 
3 
Dettaglio dell’Ordinanza 
/ConsultazioneSIUS/DettaglioOrdinazna?wsdl 
1.0 
4 
Elenco Soggetti con Procedimenti 
/ConsultazioneSIUS/ElenocSoggetti?wsdl 
1.0

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-AR-1.0-20200407-Modello Dati - AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 12/18 
 
5 
Elenco 
Procedimenti per Soggetto 
/ConsultazioneSIUS/ElencoProcedimentiPerSoggetto?wsdl 
1.0 
6 
Elenco Avvisi 
/ConsultazioneSIUS/ElenocAvvisi?wsdl 
1.0 
7 
Dettaglio Rinvio Udienza 
/ConsultazioneSIUS/DettaglioRinvioUdienza?wsdl 
1.0 
8 
 Richiesta Stampa 
/ConsultazioneSIUS/RichiestaStampa?wsdl 
1.0 
 
ATTIVITA’ RICERCHE 
 
Nome Colonna 
Descrizione della Colonna 
Dominio 
1 
CF Avvocato 
Codice fiscale dell’avvocato 
Alfanumerico 
2 
Desc Pagina 
Identificativo della pagina da cui parte la 
ricerca 
Alfanumerico 
3 
Dati Pagina  
Dati utilizzati per la ricerca 
Alfanumerico 
4 
Nome servizio 
Nome del servizio invocato 
Alfabetico 
5 
Data Ricerca 
Data in cui è stata fatta la ricerca 
Data 
 
UFFICI DISTRETTO SEDE 
 
Nome Colonna 
Descrizione della Colonna 
Dominio 
1 
Cod Tipo Ufficio 
Codice tipologia ufficio 
Alfabetico 
2 
Cod Comune 
Codice del Comune 
Alfanumerico 
3 
Cod Distretto 
Codice del Distretto 
Alfanumerico 
4 
Data inizio Validità 
Data di inzio validità 
Data 
5 
Data fine Validità 
Data di fine validità 
Data 
 
TIPO UFFICIO 
 
Nome Colonna 
Descrizione della Colonna 
Dominio 
1 
Cod Tipo Ufficio 
Codice tipologia ufficio 
Alfabetico 
2 
Descr Tipo Ufficiio 
Descrizione tipologia ufficio 
Alfanumerico 
3 
Data inizio Validità 
Data di inzio validità 
Data

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-AR-1.0-20200407-Modello Dati - AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 13/18 
 
 
Nome Colonna 
Descrizione della Colonna 
Dominio 
4 
Data fine Validità 
Data di fine validità 
Data 
 
3.2 Schema Fisico 
3.2.1 Descrizione Schema Fisico 
In questo paragrafo si descrive lo schema fisico del sistema di Consultazione Procedimenti SIUS, dando 
un’indicazione puntuale dei campi presenti nelle tabelle con i nomi che troveremo in banca dati, corredate 
da descrizioni, tipologie, dominio e obbligatorietà

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-AR-1.0-20200407-Modello Dati - AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 14/18 
 
3.2.2 Schema Fisico – Diagramma

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-AR-1.0-20200407-Modello Dati - AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 15/18 
 
3.2.3 Elenco tabelle schema fisico 
Si riporta il dettaglio delle entità utilizzate nello schema AVVSIES. Per ciascuna entità si riporta il nome della 
colonna, la descrizione della colonna, la tipologia, il suo dominio e l’obbligatorietà. A differenza dello schema 
logico, il nome dei campi e delle tabelle sono quelli che effettivamente si trovano in banca dati. Inoltre sono 
specificate le primary key, le foreign key e gli eventuali indici utilizzati per le ricerche o per regole di 
cancellazione. 
• DISTRETTI 
• COMUNI 
• STATI 
• SERVIZI 
• ATTIVITA_RICERCHE 
• UFFICI_DISTRETTO 
• TIPO_UFFICIO 
 
DISTRETTI 
 
Nome Colonna 
Descrizione della Colonna 
Tipo 
Dominio 
Obbligatorietà 
1 
COD_DISTRETTO 
Codice del Distretto  
Varchar2(11) 
Alfanumerico 
SI 
2 
DESCRIZIONE 
Descrizione del Distretto 
Varchar2(50) 
Alfanumerico 
SI 
3 
DNS 
Domain Name Service della 
macchina Server del Distretto 
Varchar2(100) 
Alfanumerico 
SI 
4 
Data inizio attivazione 
Data di Inizio Attivazione del 
Distretto 
Date 
Data 
NO 
5 
Data fine attivazione 
Data di fine Attivazione del 
Distretto 
Date 
Data  
NO

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-AR-1.0-20200407-Modello Dati - AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 16/18 
 
COMUNI 
 
Nome Colonna 
Descrizione della Colonna 
Tipo 
Dominio 
Obbligatorietà 
1 
COD_COMUNE 
Chiave primaria (PKJ)della 
tabella – Codice del Comune 
Varchar2(6) 
Alfanumeri
co 
SI 
2 
DESCRIZIONE 
Descrizione del comune 
Varchar2(250) 
Alfanumeri
co 
SI 
3 
CAP 
Codice 
di 
avviamento 
postale 
Varchar2(5) 
Numerico 
NO 
4 
DATA_CARICAMENTO 
Data di caricamento 
Date 
Data 
SI 
5 
COD_SEDE_GIUDIZIARIA 
Codice della sede giudiziaria 
Varchar2(3) 
Numerico 
NO 
6 
FLAG_VALIDITA 
Flag Validità (S/N) 
Varchar2(1) 
Alfabetico 
NO 
 
STATI 
 
Nome Colonna 
Descrizione della Colonna 
Tipo 
Dominio 
Obbligatorietà 
1 
COD_STATO 
Chiave primaria (PK) della 
tabella – Codice dello Stato 
Varchar2(6) 
Numerico 
SI 
2 
DESCRIZIONE 
Descrizione dello Stato  
Varchar2(250) 
Alfabetico 
SI 
3 
DATA_CARICAMENTO 
Data di caricamento 
Date 
Data 
SI 
4 
FLAG_VALIDITA 
Flag Validità (S/N) 
Varchar2(1) 
Alfabetico 
NO 
 
SERVIZI 
 
Nome Colonna 
Descrizione della Colonna 
Tipo 
Dominio 
Obbligatorietà 
1 
ID_SERVIZIO 
Chiave primaria (PKJ)della 
tabella – Identificativo del 
servizio da invocare 
Varchar2(6) 
Alfanumerico 
SI 
2 
DESCRIZIONE_SERVIZIO 
Descrizione 
Generica 
del 
Servizio Wev 
Varchar2(100) 
Alfanumerico 
SI

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-AR-1.0-20200407-Modello Dati - AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 17/18 
 
 
Nome Colonna 
Descrizione della Colonna 
Tipo 
Dominio 
Obbligatorietà 
3 
NOME_SERVIZIO 
Nome 
del 
servizio 
da 
invocare 
Varchar2(100) 
Alfanumerico 
SI 
4 
VERSION 
Versione del servizio 
Varchar2(20) 
Alfanumerico 
NO 
 
ATTIVITA_RICERCHE 
 
Nome Colonna 
Descrizione della Colonna 
Tipo 
Dominio 
Obbligatorietà 
1 
ID_ATTIVITA 
Chiave primaria (PKJ)della 
tabella 
– 
Identificativo 
dell’attività di ricerca 
Number 
Numerico 
SI 
2 
CF_AVVOCATO 
Codice fiscale dell’avvocato 
Varchar2(16) 
Alfanumeri
co 
SI 
3 
DESC_PAGINA 
Identificativo della pagina da 
cui parte la ricerca 
Varchar2(100) 
Alfanumeri
co 
SI 
4 
DATI_PAGINA 
Dati utilizzati per la ricerca 
Varchar2(1000) 
Alfanumeri
co 
SI 
5 
NOME_SERVIZIO 
Nome del servizio invocato 
Varchar2(100) 
ALfanumeri
co 
SI 
6 
DATA_RICERCA 
Data in cui è stata fatta la 
ricerca 
Date 
Data 
NO 
 
UFFICI_DISTRETTO 
 
Nome Colonna 
Descrizione della Colonna 
Tipo 
Dominio 
Obbligatorietà 
1 
COD_UFFICIO 
Codice dell’ufficio 
Varchar2(11) 
Alfanumeri
co 
NO 
2 
COD_TIPO_UFFICIO 
FK alla tabella TIPO_UFFICIO 
Varchar2(10) 
Alfanumeri
co 
SI 
3 
COD_COMUNE 
FK alla tabella COMUNI  
Varchar2(6) 
Alfanumeri
co 
SI 
4 
COD_DISTRETTO 
FK alla tabella DISTRETTI 
Varchar2(11) 
Alfanumeri
co 
SI 
5 
DATA INZIO VALIDITA 
Data inizio validità 
Date 
Data  
SI

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-AR-1.0-20200407-Modello Dati - AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 18/18 
 
 
Nome Colonna 
Descrizione della Colonna 
Tipo 
Dominio 
Obbligatorietà 
6 
DATA FINE VALIDITA 
Data fine validità 
Date 
Data 
NO 
 
TIPO_UFFICIO 
 
Nome Colonna 
Descrizione della Colonna 
Tipo 
Dominio 
Obbligatorietà 
1 
COD_TIPO_UFFICIO 
Codice Tipologia Ufficio 
Varchar2(10) 
Alfanumeri
co 
SI 
2 
DESCR_TIPO_UFFICIO 
Descrizione Tipologia Ufficio  
Varchar2(6) 
Alfanumeri
co 
SI 
3 
DATA INZIO VALIDITA 
Data inizio validità 
Date 
Data  
SI 
4 
DATA FINE VALIDITA 
Data fine validità 
Date 
Data 
NO