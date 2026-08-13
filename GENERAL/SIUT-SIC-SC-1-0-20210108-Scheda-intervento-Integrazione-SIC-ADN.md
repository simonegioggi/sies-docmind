---
uniqueName: siut-sic-sc-1-0-20210108-scheda-intervento-integra
displayName: "SIUT SIC SC 1 0 20210108 Scheda intervento Integrazione SIC ADN"
category: "GENERAL"
tags: []
---

# SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN

> **File originale:** `MEV/Integrazione SIES-ADN/DOCS/SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 1/46 
 
 
Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
Scheda Intervento Integrazione SIC-ADN 
 
 
 
 
 
Versione 1.0 del 08/01/2021

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 2/46 
 
 
Il presente documento è stato redatto con la 
collaborazione 
del 
RTI 
Engineering 
Ingegneria 
Informatica S.p.A & Sirfin-PA S.r.l. nell’ambito del 
contratto CIG 73479643B7 per lo “Sviluppo del 
sistema 
informativo 
unitario 
telematico, 
la 
manutenzione degli attuali sistemi dell’area penale 
del Ministero della Giustizia e servizi correlati. 
Lotto 1”

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 3/46 
Approvazioni 
 
Nominativo 
Funzione 
Elaborato da 
Emma Caporizzo 
Analista Funzionale 
Verificato da 
Vito Bufi 
Alessandro Falleni 
Fabio Gattamorta 
Responsabile Manutenzione Sistemi attuali 
Referente Sicurezza 
Referente PMO e Qualità 
Approvato da 
Paolo Ceccanti 
Responsabile Unico Fornitura 
Data approvazione 
08/01/2021 
 
Livello di riservatezza 
L4 
 
 
Elenco versioni 
Versione 
Data  
Motivo 
Modifica 
1.0 
08/01/2021 
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
Vito Bufi 
RTI 
 
Responsabile Manutenzione Sistemi attuali 
Sergio Tamburrini 
RTI 
 
Organization Manager 
Salvatore Piazza 
RTI 
 
Technical Manager 
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
 
Responsabile PMO e Qualità 
Alessandro Falleni 
RTI 
 
Referente Sicurezza 
Francesco Rosati 
RTI 
 
Referente Qualità e Sicurezza 
Andrea Castorino 
RTI 
 
Referente Applicativo Gestore Fascicolo 
Documentale 
Luigi Buglione 
RTI 
 
Referente Metrico

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 4/46 
INDICE DEI CONTENUTI 
1 
INTRODUZIONE ............................................................................................................................... 6 
1.1 
SCOPO DEL DOCUMENTO .......................................................................................................................... 6 
1.2 
ACRONIMI E DEFINIZIONI .......................................................................................................................... 6 
1.2.1 
ACRONIMI .......................................................................................................................................... 6 
1.2.2 
DEFINIZIONI ........................................................................................................................................ 7 
1.3 
RIFERIMENTI ........................................................................................................................................... 7 
2 
DEFINIZIONE DELL’OBIETTIVO .......................................................................................................... 8 
2.1 
CONVENZIONI ......................................................................................................................................... 8 
2.2 
ELENCO REQUISITI ................................................................................................................................... 8 
2.2.1 
REQ-SIC-003_2019-01 – MAPPATURA UTENTI SIC – ADN (PRE GO-LIVE) ................................................ 8 
2.2.2 
REQ-SIC-003_2019-02– MAPPATURA UTENTI SIC – ADN (POST GO-LIVE) ............................................... 8 
2.2.3 
REQ-SIC-003_2019-03 – MAPPATURA UTENTI SIC – ADN PER SISTEMA SIPPI/SITMP .............................. 8 
2.2.4 
REQ-SIC- 003_2019-04 – MAPPATURA UTENTI SIC – ADN PER SISTEMA SIES ........................................... 9 
2.2.5 
REQ-SIC-003_2019-05 – MAPPATURA UTENTI SIC – ADN PER SISTEMA CERPA WEB................................. 9 
2.2.6 
REQ-SIC-003_2019-06 – MAPPATURA UTENTI SIES – ADN PER SISTEMA SIES .......................................... 9 
3 
DESCRIZIONE DELL’INTERVENTO .................................................................................................... 11 
3.1 
REQ-SIC-003_2019-01 – MAPPATURA UTENTI SIC – ADN (PRE GO-LIVE) ................................................. 12 
3.1.1 
Verifica corrispondenza username e password ADN ................................................................................ 17 
3.1.2 
Funzione di configurazione/selezione account SIC e verifica corrispondenza username e password di 
accesso al SIC ............................................................................................................................................................ 18 
3.2 
REQ-SIC-003_2019-02 – MAPPATURA UTENTI SIC – ADN (POST GO-LIVE)................................................ 19 
3.2.1 
Funzione di ufficio SIC e verifica corrispondenza utenza per accesso al SIC .............................................. 21 
3.3 
REQ-SIC-003_2019-03 – MAPPATURA UTENTI SIC – ADN PER SISTEMA SIPPI/SITMP ................................ 28 
3.3.1 
Iscrizione di Provvedimenti Principale e dell’Esecuzione di Misure di Prevenzione ................................... 28 
3.3.2 
Richiesta di certificati di tipologia Autorità Giudiziaria (art.21 comma 1 del T.U.) e Pubblico Ministero 
(art.21 comma 1 del T.U.) ......................................................................................................................................... 30 
3.4 
REQ-SIC-003_2019-04 – MAPPATURA UTENTI SIC – ADN PER SISTEMA SIES ............................................. 31 
3.4.1 
Invio Procedimenti (Titoli Esecutivi, Fogli Complementari e Cumuli) ........................................................ 32 
3.4.2 
Modulo di interconnessione WEB ............................................................................................................. 33 
3.4.3 
Servizio di Richiesta Certificati .................................................................................................................. 34 
3.5 
REQ-SIC-003_2019-05 – MAPPATURA UTENTI SIC – ADN PER SISTEMA CERPA WEB .................................. 34 
3.6 
REQ-SIC-003_2019-06 – MAPPATURA UTENTI SIES – ADN PER SISTEMA SIES ........................................... 35 
3.7 
MODULI SW.......................................................................................................................................... 40 
3.8 
ARCHITETTURA ...................................................................................................................................... 40 
3.9 
INTERFACCE UTENTE ............................................................................................................................... 41 
3.10 
BASI DATI ......................................................................................................................................... 41 
3.10.1 
Tabelle associative utenza ADN utenze SIC – SISTEMA SIC ....................................................................... 41 
3.10.2 
Tabelle per il controllo della domanda segreta – SISTEMA SIC ................................................................. 41 
3.10.3 
Tabelle per il controllo utenti SIPPI ed utenti SIES – SISTEMA SIC ............................................................. 42 
3.10.4 
Tabelle per mapping utenza ADN ed utenza SIES – SISTEMA SIES ............................................................ 42 
3.11 
WEB SERVICES .................................................................................................................................. 42 
3.12 
XSD................................................................................................................................................. 43

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 5/46 
3.13 
CONFIGURAZIONE .............................................................................................................................. 43 
3.14 
TUTORIAL ......................................................................................................................................... 44 
4 
PIANO DELLE ATTIVITÀ .................................................................................................................. 45 
4.1 
CICLO DI SVILUPPO ................................................................................................................................. 45 
4.2 
VINCOLI ............................................................................................................................................... 45 
4.3 
LUOGO DI LAVORO ................................................................................................................................. 45 
5 
DIMENSIONAMENTO ..................................................................................................................... 46 
5.1 
STIMA DELL'EFFORT PREVISTO .................................................................................................................. 46

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 6/46 
1 
Introduzione 
1.1 Scopo del documento 
Il presente documento nasce ad integrazione delle attività previste in scheda SIUT-SIC-SC-1.0-20200924-
Scheda intervento Scheda_n.3_2019 Sostituzione IGI.pdf [RIF. 1]. 
In particolare si è delineata la necessità di intervenire, con ulteriori implementazioni rispetto a quanto 
previsto in scheda, sia sul SIC che e su altri applicativi ‘satelliti’ del SIC, che attualmente si poggiano sulle 
funzioni di autenticazione e profilazione ‘offerte’ dall’appliance IGI. 
Gli interventi hanno un duplice scopo: 
➢ Prevedere un’attività di associazione degli utenti ADN con le utenze SIC. 
➢ Garantire una continuità di funzionamento delle interazioni e delle interconnessioni che oggi il SIC 
ha con altri sistemi (SIES e SIPPI/SITMP), a valle della dismissione del sistema IGI. 
 
1.2 Acronimi e Definizioni 
1.2.1 Acronimi 
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
Direzione Generale per o Sistemi Informativi Automatizzati 
DR 
Disaster Recovery 
ETSI 
European Telecommunications Standards Institute 
FP 
Function Point 
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
Mandatory Access Control 
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 7/46 
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
Raggruppamento Temporaneo di Impresa Engineering – Sirfin-PA 
RUF 
Responsabile Unico Fornitore 
RUP 
Responsabile unico Progetto 
SAL 
Stato Avanzamento Lavori 
SGQ 
Sistema di Gestione per la Qualità di Engineering Ingegneria Informatica S.p.A. 
SGSI 
Sistema di Gestione della Sicurezza Informatica 
SICP 
Sistema Informativo Cognizione Penale 
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
VPN 
Virtual Private Network 
1.2.2 Definizioni 
Glossario 
Sinonimo 
Definizione 
 
 
 
1.3 Riferimenti 
Riferimento 
Nome Documento 
Descrizione 
Documento 
RIF.1 
SIUT-SIC-SC-1.0-20200924-Scheda 
intervento 
Scheda_n.3_2019 Sostituzione IGI.pdf 
Scheda di Intervento

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 8/46 
2 
Definizione dell’Obiettivo 
Nell’ambito della realizzazione della scheda di intervento di cui al RIF. 1, relativa alla dismissione e alla 
sostituzione dello strumento di Identity and Access Management, IGI (Ibm Security Identity Governance & 
Intelligence), si inseriscono una serie di interventi per garantire sia la continuità dei servizi ad oggi presenti 
in SIC, sia l’adeguamento di tutta l’infrastruttura al nuovo meccanismo di autenticazione e profilazione. 
 
Prerequisito fondamentale per l’implementazione dell’obiettivo è che ogni utente abbia un’utenza ADN di 
Giustizia. Fa eccezione il requisito definito al par. 2.2.5 che è relativo ad un’applicazione a servizio di Enti di 
Pubblica Amministrazione. 
2.1 Convenzioni 
Sulla base degli ambiti di progetto e dei tipi di requisito, la convenzione per l’identificazione dei requisiti è 
riportata di seguito. 
Ciascun requisito è individuato da un identificativo univoco nella forma [REQ-SIS-nnn-mm], dove: 
• 
REQ Requisito; 
• 
SIS identifica il sistema (cfr. SIUT-GEN-SN-2.2-20191023-Standard di nomenclatura);  
• 
nnn è il numero della scheda di richiesta intervento (da parametro); 
• 
mm è il numero progressivo del requisito espresso dall’Amministrazione. 
 
2.2 Elenco Requisiti 
2.2.1 REQ-SIC-003_2019-01 – Mappatura utenti SIC – ADN (Pre Go-Live) 
L’attività definita come ‘mappatura utenti SIC – ADN (Pre Go-Live) ’ fa riferimento alla ‘rivisitazione’ 
dell’attuale pagina di login del SIC in una fase antecedente alla messa in esercizio (da ciò nasce la 
nomenclatura Pre go-live) degli interventi previsti in scheda di cui al RIF.1. Lo scopo è ‘recuperare’ 
nell’immediato, in modo automatizzato e sotto la diretta responsabilità dell’utente che utilizza la funzione, 
l’utenza ADN e di associarla all’utenza SIC, specifica per ogni ufficio su Casellario. 
 
2.2.2 REQ-SIC-003_2019-02– Mappatura utenti SIC – ADN (Post Go-Live) 
L’attività definita come ‘mappatura utenti SIC – ADN (Post Go-Live) ’ fa riferimento all’introduzione, sul 
sistema SIC, di una nuova funzionalità di associazione/mappatura di un utente ADN con uno specifico 
utente/ufficio del SIC. L’intervento è definito Post go-live, in quanto fa riferimento ad un meccanismo da 
introdurre contestualmente alla messa in esercizio degli interventi previsti in scheda di cui al RIF.1. 
 
2.2.3 REQ-SIC-003_2019-03 – Mappatura utenti SIC – ADN per sistema SIPPI/SITMP 
Per garantire la continuità dei servizi di interconnessione ad oggi presenti tra il sistema SIPPI/SITMP ed il SIC, 
si delinea la necessità di intervenire sugli attuali meccanismi di scambio ‘dati’ tra i due sistemi. 
L’intervento mira all’allineamento dei vari ‘colloqui’ infrastrutturali relativamente alle nuove dinamiche di 
autenticazione e profilazione previste dalla scheda di cui al RIF.1.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 9/46 
I processi di interconnessione presenti tra SIPPI/SITMP ed il SIC sono: 
 
➢ Iscrizione di Provvedimenti Principale di Misure di Prevenzione; 
➢ Iscrizione di Provvedimenti dell'Esecuzione di Misure di Prevenzione; 
➢ Richiesta di certificati di tipologia Autorità Giudiziaria (art.21 comma 1 del T.U.) e Pubblico Ministero 
(art.21 comma 1 del T.U.); 
2.2.4 REQ-SIC- 003_2019-04 – Mappatura utenti SIC – ADN per sistema SIES 
Per garantire la continuità dei servizi di interconnessione ad oggi presenti tra il sistema SIES e SIC, si delinea 
la necessità di intervenire sugli attuali meccanismi di scambio ‘dati’ tra i due sistemi. 
L’intervento mira all’allineamento dei vari ‘colloqui’ infrastrutturali relativamente alle nuove dinamiche di 
autenticazione e profilazione previste dalla scheda di cui al RIF.1.  
 
I processi di interconnessione presenti tra SIES e SIC sono: 
➢ Invio titoli esecutivi da SIES verso il SIC; 
➢ Invio dei fogli complementari da SIES verso il SIC; 
➢ Invio provvedimento di cumulo da SIES verso il SIC; 
➢ Recupero di provvedimenti principali dal SIC sul SIES; 
➢ Richiesta del certificato Penale; 
➢ Accesso al modulo WEB di interconnessione SIES-NSC; 
2.2.5 REQ-SIC-003_2019-05 – Mappatura utenti SIC – ADN per sistema Cerpa WEB 
CERPA WEB è l’applicazione che offre i servizi di Certificazione per le Amministrazioni Pubbliche e i Gestori di 
Pubblici Servizi. Ad oggi tale applicazione è presente sul portale dei Servizi al Cittadino di Casellario Giustizia 
e si appoggia sulle medesime dinamiche di autenticazione e profilazione del SIC, basate sul sistema IGI (Ibm 
Security Identity Governance & Intelligence). In relazione alla dismissione di tale strumento di IAM, si delinea 
la necessità di ‘rivedere’ la modalità di accesso ed utilizzo dell’Applicazione CERPA WEB.  
 
2.2.6 REQ-SIC-003_2019-06 – Mappatura utenti SIES – ADN per sistema SIES 
Con lo scopo di uniformare il comportamento delle applicazioni all’utilizzo dell’utenza ADN, e in ottica di 
garantire quanto esplicitato per il requisito REQ-SIC- 003_2019-04, si delinea la necessità di intervenire 
sull’attuale gestione della login sul sistema SIES. In particolare, alla stregua di quanto si è prospettato di 
implementare per il SIC, anche per l’applicazione del SIES, si propone di integrare la maschera di accesso con 
un ‘ ulteriore sezione per permettere all’utente di inserire le credenziali ADN. A seguito dell’inserimento e 
verifica delle stesse, l’applicativo ‘registrerà’, in apposite tabelle associative la correlazione dell’utenza SIES 
con l’utenza ADN.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 10/46

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 11/46 
3 
Descrizione dell’Intervento 
In riferimento ad ogni requisito individuato, si procederà con l’esplicazione di una proposta operativa 
evidenziando tutti gli aspetti non solo funzionali, ma anche di tipo implementativo. 
Sarà inoltre data evidenza delle interazioni dei vari flussi autorizzativi che intercorreranno tra i sistemi e la 
CAAA nazionale. 
 
Gli interventi sono da intendersi da applicare sul SIC, ma parte di essi hanno un impatto anche sui sistemi 
fonte SIPPI/SITMP e SIES. 
 
In maniera schematica, si riportano i principali punti che costituiscono l’intervento in oggetto: 
 
1. INTERVENTI LATO SIC 
 
a) Modifica pagina di login sul SIC in una fase precedente alla dismissione di IGI [REQ-SIC-003-01]; 
b) Realizzazione Funzione di mapping utente ADN ed ufficio/utenza SIC nella fase successiva alla dismissione 
di IGI [REQ-SIC-003-02]; 
c) Realizzazione di classi client java per la verifica della ‘validazione’ del profilo utente verso la CAAA 
nazionale [REQ-SIC-003-02]; 
d) Adeguamento dei controlli, in ingresso su SIC, dei flussi xml di invio dei provvedimenti Misure 
Prevenzione (SIPPI/SITPM) verso il SIC [REQ-SIC-003-03]; 
e) Gestione del ‘riconoscimento’ ed ‘identificazione’ dell’utente SIPPI/SITMP per l’operazione di Richiesta 
Certificato Penale sul Sic e relativo adeguamento del flusso xml del servizio SOAP di Richiesta Certificato 
[REQ-SIC-003-03]; 
f) Adeguamento dei flussi xml per l’invio dei titoli Esecutivi, Cumuli e Foglio Complementari del SIES verso 
il SIC [REQ-SIC-003-04]; 
g) Gestione del ‘riconoscimento’ ed ‘identificazione’ dell’utente SIES per l’operazione di Richiesta 
Certificato Penale sul Sic e relativo adeguamento del flusso xml del servizio SOAP di Richiesta Certificato 
[REQ-SIC-003-04]; 
h) Gestione del ‘riconoscimento’ ed ‘identificazione’ dell’utente SIES per l’accesso al modulo WEB di 
Interconnessione SIES-NSC WEB [REQ-SIC-003-04]; 
i) 
Individuare la metodologia di accesso all’applicazione CERPA WEB a seguito della dismissione del sistema 
IGI [REQ-SIC-003-05]; 
 
 
2. INTERVENTI LATO SIPPI/SITMP 
 
Quanto definito al requisito REQ-SIC-003_2019-03 riguarda degli interventi da applicare, oltre che sul sistema 
SIC, come definito al punto precedente, anche sul sistema fonte SIPPI/SITMP: 
 
A fronte degli interventi previsti in SIC, nel sistema SIPPI/SITMP occorre adeguare la funzione relativa 
all’invocazione del servizio di Richiesta del Certificato. In particolare, in fase di chiamata del servizio, 
attualmente, vengono passate le credenziali di accesso, username e password, del SIC. La chiamata al servizio 
deve essere ‘modificata’ in modo che il sistema fonte SIPPI/SITMP invii le credenziali ADN Giustizia.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 12/46 
In particolare si richiede che nel SOAP-HEADER del servizio sia inviato lo userName ADN. 
Per il servizio di invio dei provvedimenti di Misure Prevenzione non è prevista nessuna modifica del flusso 
dati. 
 
3. INTERVENTI LATO SIES  
 
Quanto definito in REQ-SIC-003_2019-04 riguarda degli interventi da applicare, oltre che sul sistema SIC, 
come definito al punto 1, anche sul sistema fonte SIES. 
 
A fronte degli interventi previsti in SIC, nel sistema SIES occorre adeguare la funzione relativa all’invocazione 
del servizio di Richiesta del Certificato. In particolare, in fase di chiamata del servizio, attualmente vengono 
passate le credenziali di accesso, username e password, del SIC. La chiamata al servizio deve essere 
‘modificata’ in modo che il sistema fonte SIES invii lo userName ADN Giustizia. 
 
Per l’invio dei provvedimenti dei titoli Esecutivi, Cumuli e Fogli Complementari deve essere prevista una 
modifica alla struttura dati dell’xml per integrare l’invio del valore userName ADN. 
 
Anche per l’interconnessione al modulo SIES-NSC Web deve essere prevista una modifica alla struttura dati 
dell’xml per integrare l’invio del valore userName ADN. 
 
Inoltre, saranno modificati e/o inseriti dei nuovi messaggi di output in ritorno alle chiamate dei vari servizi, 
relativi alla modalità di accesso agli stessi.  
 
Il requisito REQ-SIC-003_2019-06, si intende da applicare esclusivamente sul sistema SIES. Per tale requisito 
nel sistema SIES occorre prevedere una modifica all’attuale pagina di login, in modo tale che l’utente, prima 
di specificare l’utenza di accesso all’applicazione, deve digitare la propria user e password ADN. 
 
 
3.1 REQ-SIC-003_2019-01 – Mappatura utenti SIC – ADN (Pre Go-Live) 
Nell’ottica di predisporre il sistema del Casellario all’integrazione con l’autenticazione basata sulle utenze di 
ADN di Giustizia, si propone di intervenire sulla pagina di accesso al SIC in modo da ‘iniziare’ ad alimentare 
ed arricchire la banca dati del SIC, con le associazioni dell’utenza ADN rispetto all’ufficio o gli ‘n’ uffici con cui 
l’utente è profilato attualmente sul SIC. 
In SIC, ad oggi, non è gestita la multi profilazione, e pertanto, per permettere ad uno stesso utente, 
supponiamo ROSSI MARIO, di poter lavorare in uffici diversi, si è ‘obbligati’ ad associargli diverse utenze di 
accesso, ognuna per il relativo ufficio di lavorazione per cui è abilitato. 
 
Ad esempio l’utente ROSSI MARIO che fa accesso all’ufficio Corte Appello di Roma ha l’utenza mrossiR, e lo 
stesso utente ROSSI MARIO che fa accesso all’ufficio Corte Appello di Milano ha l’utenza mrossiM. 
 
MARIO ROSSI nato a Roma CF:xxxxxxxxxxxxxxxx 
UTENZA ADN 
 
UTENZA SIC 
 
UFFICIO SIC

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 13/46 
mario.rossi 
mrossiR 
Corte Appello di Roma 
mrossiM 
Corte Appello di Milano 
 
 
L’attività che si vuole ‘anticipare’ è la procedura di mapping tra l’utenza ADN di cui ogni utente è proprietario, 
e le utenze che lo stesso utente ha sul sistema SIC. 
La proposta che si vuole avanzare è la seguente: 
 
L’utente si trova sulla pagina di Login del SIC. Il sistema propone la pagina di accesso in cui l’utente sarà 
tenuto ad inserire le proprie credenziali ADN, in deroga a quanto attualmente previsto dal sistema SIC che 
chiede l’inserimento delle credenziali SIC. 
 
In realtà questo ‘nuovo’ modo di lavorare anticipa, in qualche modo, ciò che a tendere avverrà per l’accesso 
unico ai sistemi penali, dove appunto è prevista un’autenticazione basata sulle credenziali ADN Nazionale. 
 
Si riporta di seguito un esempio della pagina di accesso al SIC: 
 
 
Figura 1: Pagina inserimento utenza ADN 
 
A seguito dell’azione di ‘submit’ delle credenziali, il sistema effettua un controllo sulla ‘autenticità’ delle 
informazioni inserite effettuando una chiamata LDAP sul server ADN di giustizia. 
Per dati esatti, il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione 
delle utenze SIC, così come riportato nell’immagine che segue, mentre per dati non corrispondenti, sarà 
visualizzato apposito messaggio di errore.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 14/46 
 
Figura 2: Pagina di configurazione credenziali SIC 
 
Dalla form prospettata, con la selezione della procedura di ‘selezione/configurazione’ dell’account, all’utente 
sarà mostrata la pagina per l’inserimento delle credenziali del SIC: 
 
 
Figura 3: Pagina di configurazione/selezione account del SIC 
 
A seguito dell’inserimento delle credenziali del SIC, il sistema effettuerà i seguenti step: 
• 
Login sul sistema SIC con verifica della corrispondenza username e password per l’accesso al SIC su 
IGI (si ricorda che in questa fase di pre go-live il sistema di autenticazione IBM non risulta ancora 
dismesso); 
• 
Verifica della presenza in sistema dell’associazione utenza SIC specificata ed utenza ADN; 
• 
In caso di NON associazione dell’utenza, il sistema procederà con l’accoppiamento delle utenze 
scrivendo il dato in un’apposita tabella che risiede sul sistema SIC; 
• 
In caso di associazione GIA’ presente, il sistema mostrerà un messaggio di utente riconosciuto per 
l’ufficio scelto; 
• 
In ogni caso l’utente può procedere con la configurazione di eventuale ogni altro account di cui 
dispone per l’accesso al SIC;

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 15/46 
 
 
 
Figura 4: Pagina di associazione con l'ufficio SIC 
 
A questo punto l’utente selezionando il tasto ‘Entra’ sarà ridiretto nella welcome page dell’applicazione del 
SIC: 
 
 
Figura 5: Welcome page del SIC 
 
Proseguendo invece con la funzione di ‘Seleziona/Configura un account SIC’, il sistema mostrerà nuovamente 
la form di inserimento utenza e password SIC:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 16/46 
 
Figura 6: Pagina inserimento credenziali SIC 
 
 
Configurando ogni account, l’utente completerebbe, sotto la propria responsabilità, la procedura di match 
tra la propria utenza ADN con le multi utenze del SIC. 
 
Al successivo accesso, se l’utente ha eseguito delle associazioni, si ritroverà, già configurate, le utenze che 
utilizza solitamente per l’accesso al SIC. Quindi, sempre a valle dell’inserimento dell’utenza ADN, come in 
figura 1, il sistema mostrerà una form di accesso simile alla figura che segue: 
 
 
Figura 7: Pagina di scelta utenza 
 
L’utente pertanto può selezionare l’utenza di interesse, inserire la password ed iniziare la navigazione nel SIC, 
oppure configurare ed entrare con un account diverso. 
 
Descriviamo a seguire il dettaglio dei flussi funzionali e tecnici per il requisito in oggetto.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 17/46 
3.1.1 Verifica corrispondenza username e password ADN 
 
Per l’accesso al SIC, l’utente inserisce le credenziali ADN. Il sistema, a seguito dell’inserimento dell’utenza 
ADN, si farà carico delle verifica delle credenziali digitate. 
Il sistema, implementerà una chiamata al server LDAP di ADN Giustizia, passando in input le credenziali 
specificate. 
Da 
un 
punto 
di 
vista 
più 
tecnico, 
sarà 
effettuata 
una 
chiamata 
su 
contesto 
LDAP 
(com.sun.jndi.ldap.LdapCtxFactory), con protocollo SSL, impostando una SECURITY_AUTHENTICATION con le 
SECURITY_CREDENTIALS. 
In risposta alla chiamata di ‘search’, nella casistica in cui l’autenticazione abbia avuto esito positivo, sarà 
restituita una lista di attributi di identificazione dell’utente. Nella casistica in cui, la chiamata di ‘search’ non 
ha ‘autenticato’ l’utente, l’oggetto di ritorno sarà pari a NULL. 
 
 
 
 
Figura 8: sequence diagram per verifica utenza ADN 
 
 
L’attributo ‘user-name’ recuperato, insieme al Nome e Cognome dell’utente (se disponibili in risposta alla 
verifica LDAP) , saranno mostrati a video con apposito messaggio.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 18/46 
 
 
 
Figura 9: Messaggio di utenza verificata su ADN 
 
3.1.2 Funzione di configurazione/selezione account SIC e verifica corrispondenza username e password di 
accesso al SIC 
La funzione denominata ‘Seleziona/Configura un account SIC’, appare a video solo a seguito di verifica 
positiva dell’utenza ADN. 
Cliccando su questo tasto funzione, il sistema mostrerà la form di inserimento delle credenziali SIC. L’utente 
procede con l’indicazione delle credenziali (username e password) e sottopone la richiesta al sistema. 
 
A questo punto il sistema si interessa di effettuare la consueta procedura di login su IGI, attualmente in uso 
su SIC. Il flusso ad oggi previsto, nella fase di pre-go live, resta immutato. Pertanto il sistema continua a 
verificare: 
• 
Correttezza delle credenziali digitate 
• 
Gestione del cambio password 
• 
Verifica della domanda segreta 
 
Con la verifica della correttezza delle credenziali fornite, il sistema individua univocamente l’utente e l’ufficio 
presso cui l’utente intende lavorare. A valle di ciò, il sistema effettua la redirect ad una nuova pagina, 
mostrando il messaggio di ‘match avvenuto con successo’. A questo punto l’utente può iniziare la navigazione 
in SIC.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 19/46 
 
Figura 10: sequence diagram per verifica credenziali SIC 
 
 
3.2 REQ-SIC-003_2019-02 – Mappatura utenti SIC – ADN (Post Go-Live) 
La fase post go-live si inserisce in uno scenario in cui l’applicazione SIC risulta integrata, a livello tre, con il 
progetto My Giustizia: 
 
• 
Gli utenti, tramite browser, accedono e si autenticano su my.giustizia.it 
• 
Il portale, con la modalità OAuth2, verifica le credenziali ADN fornite ed ottiene il token SSO 
• 
L’utente seleziona l’applicazione e viene reindirizzato all’end-point dal portale 
• 
Se l’applicazione supporta l’SSO, l’utente viene autenticato tramite il token OAuth2 fornito 
  
Si riporta a seguire uno schema in cui vengono illustrati, a grandi linee, le componenti architetturali ed i flussi 
tra le diverse componenti:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 20/46 
 
Figura 11: Architettura My Giustizia 
 
Nello scenario SIC, in aggiunta all’integrazione con My Giustizia, deve essere considerata anche l’integrazione 
con il workflow autorizzativo della CAAA.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 21/46 
 
Figura 12: Architettura CAAA 
 
 
Infatti, come previsto in scheda intervento, la componente CAAA console fornirà una consolle amministrativa 
(realizzata come plug-in della CAAA Admin Consolle) in grado di consultare tutti i dati relativi i profili 
autorizzativi del SIC. 
Inoltre per la modifica e assegnazione di un nuovo profilo, sarà configurata ed opportunamente adeguata, 
per gestire i dettagli della richiesta di assegnazione di un profilo autorizzativo del sistema SIC, l’applicazione 
‘CAAA request manager’. 
Quest’ultima colloquierà con i servizi dell’istanza CAAA ed effettuerà il provisioning dei profili attraverso uno 
strato di servizi REST messi a disposizione dal sistema SIC. 
La CAAA, inoltre, esporrà un servizio per richiedere la ‘certificazione’ di un profilo. 
 
Vediamo ora, come, partendo da tale scenario, occorre intervenire sull’applicazione del SIC, affinché possa 
essere ‘garantita’ la procedura di ‘configurazione’ e quindi di accesso al SIC per uno specifico ufficio. 
 
3.2.1 Funzione di ufficio SIC e verifica corrispondenza utenza per accesso al SIC  
 
Nella fase di post go-live, l’utente ‘atterra’ sull’applicazione SIC, dopo essersi autenticato sul portale My 
Giustizia con la modalità OAuth2, ‘presentandosi’ con un token di accesso contenente la user-name con la 
quale l’utente è stato autenticato su ADN. 
 
Il sistema SIC, partendo dall’identificativo univoco dell’utente e, a valle della consultazione della tabella 
‘associativa’ tra l’utenza ADN e le utenze del SIC, mostrerà una pagina contenente la lista degli uffici già 
configurati/associati all’utenza. In ogni caso la pagina restituita, alla stregua del flusso previsto nella fase pre 
go-live, deve mostrare una funzione per la gestione/mappatura di un nuovo ufficio SIC.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 22/46 
 
Figura 13: sequence diagram lista utenze SIC per utenza ADN 
 
 
Si riporta, un esempio della pagina mostrata all’utente a valle delle sequenze di flusso su descritte: 
 
 
Figura 14: Pagina di scelta ufficio 
 
A partire da tale pagina, l’utente pertanto può selezionare l’account di interesse ed iniziare la navigazione 
nel SIC, oppure ‘mappare’ ed entrare con un account diverso. 
 
Si ricorda che in questa fase di post go-live, il sistema di autenticazione IGI risulterà dismesso e pertanto la 
componente che ‘certifica’ la profilazione di un utente in SIC è la CAAA. Tra la componente CAAA ed il 
‘profilatore’ casellario deve esserci sempre un allineamento e ciò è ‘garantito’ dalle operazioni di 
‘provisioning’ poste in essere dall’istanza CAAA verso il SIC.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 23/46 
Vediamo ora nel dettaglio, quali sono le operazioni da prevedere sul sistema SIC a valle delle varie casistiche 
di accesso al SIC: 
 
1) Accesso al SIC di un utente proprietario di credenziali SIC, che ha già un mapping presente tra utenza 
ADN ed utenza/ufficio SIC o deve configurare altri account in suo possesso; 
2) Accesso al SIC di un utente proprietario di credenziali SIC, ma che NON ha effettuato ancora nessun 
mapping o deve configurare altri account in suo possesso; 
3) Accesso al SIC di un utente non proprietario di credenziali SIC; 
 
Scenario punto 1: 
 
Username_ADN = mario.rossi 
Username_SIC = mrossi001 
 
Questo è il caso in cui un utente SIC ha già effettuato il mapping con l’utenza ADN e l’ufficio o gli n uffici su 
cui è abilitato a lavorare in SIC, nella fase pre go-live delle attività previste in scheda RIF. 1 relative alla 
dismissione di IGI. 
 
Pertanto, il sistema SIC, nella fase antecedente al passaggio in esercizio, ha già registrato nella tabella 
CAS_PROFILE.ASSOC_UTENTE_IGI_ADN (per i dettagli vedi par. 3.10.1), l’associazione ID_PERSON ed 
ID_UTENTE_ADN. 
 
 
Figura 15: schema relazione tabella associativa utenze ADN-SIC 
 
Tali informazioni, e tutti i dati relativi al profilo utente, nella fase di post go-live risulteranno ‘migrate’ e 
presenti anche nella banca dati della CAAA in quanto al tempo t0 del passaggio in produzione è prevista 
un’attività di ‘caricamento’ iniziale delle profilazioni casellario verso la CAAA nazionale.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 24/46 
Definito ciò, pertanto, l’utente mario.rossi effettua l’autenticazione su MyGiustiza con utenza ADN e sulla 
‘scrivania’ del portale trova il link ‘Casellario’. 
L’utente seleziona il link ‘Casellario’ ed il reverse proxy, dopo le opportune verifiche sul token di 
autenticazione, effettua la redirect al sistema SIC. 
L’utente arriva su SIC ‘presentandosi’ con un token di accesso contenente la user-name con la quale l’utente 
è stato autenticato su ADN. 
 
Il sistema SIC, a questo punto va a verificare la presenza di un record per mario.rossi nella tabella 
CAS_PROFILE.UTENTE_ADN e ne individua l’identificativo. Con tale identificativo, per mezzo della tabella 
ASSOC_UTENTE_IGI_ADN, risale all’associazione o alle n associazioni dell’utente SIC con l’ufficio/uffici. 
 
Il sistema, recuperate le varie informazioni mostra la pagina di accesso così come mostrata nella figura che 
segue: 
 
 
 
Figura 16: Pagina di accesso - scenario 1 
 
A partire da tale pagina, l’utente pertanto può selezionare l’account di interesse ed iniziare la navigazione 
nel SIC. 
Qualora l’utente deve configurare altri account in suo possesso, vedere Scenario punto 2. 
 
Scenario punto 2: 
 
Username_ADN = mario.verdi 
Username_SIC = mverdi001 
 
 
Questo è il caso in cui un utente SIC NON ha ancora effettuato il mapping con l’utenza ADN e l’ufficio o gli n 
uffici su cui è abilitato a lavorare in SIC. 
L’utente ha delle credenziali SIC, ma non ha effettuato l’attività di mapping utenza nella fase pre go-live delle 
attività previste in scheda RIF. 1 relative alla dismissione di IGI.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 25/46 
Pertanto, il sistema SIC, nella fase antecedente al passaggio in esercizio, non ha registrato nessuna 
informazione nella tabella CAS_PROFILE.ASSOC_UTENTE_IGI_ADN per mario.verdi. Di conseguenza, il 
profilatore CAAA non è a conoscenza del profilo dell’utente mario.verdi (mverdi0001 su SIC) per l’accesso 
all’applicazione del Casellario. 
 
Definito ciò, pertanto l’utente mario.verdi effettua l’autenticazione su MyGiustiza con utenza ADN e sulla 
‘scrivania’ del portale trova il link ‘Casellario’ (si suppone che il link, per un periodo di tempo da fissare, sia 
aperto a tutti gli utenti giustizia). 
L’utente seleziona il link ‘Casellario’ ed il reverse proxy, dopo le opportune verifiche sul token di 
autenticazione, effettua la redirect al sistema SIC. 
L’utente arriva su SIC ‘presentandosi’ con un token di accesso contenente la user-name con la quale l’utente 
è stato autenticato su ADN. 
 
Il sistema SIC, effettua la verificare della presenza di un record per mario.verdi nella tabella 
CAS_PROFILE.UTENTE_ADN e NON trova nessuna corrispondenza. 
 
Il sistema, a questo punto, propone una schermata per permettere all’utente di configurare l’associazione 
della propria utenza ADN con l’ufficio/uffici per cui è abilitato in SIC. 
 
 
Figura 17: Pagina per la configurazione dell’ufficio SIC 
 
L’utente seleziona il ‘link’ per la configurazione ed il sistema prospetta una maschera in cui l’utente deve 
inserire le credenziali del SIC. 
 
A questo punto si ipotizzano tre possibilità di intervento: 
• 
Proporre una maschera in cui digitare userName e Password del SIC ed effettuare la login a sistema; 
• 
Proporre una maschera in cui digitare userName e Password del SIC ed effettuare una verifica tramite 
algoritmo di criptazione SHA-256 della password; 
• 
Proporre una machera in cui digitare lo userName e a seguire inserire la risposta alla domanda 
segreta di cui ogni utente ne è a conoscenza;

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 26/46 
 
 
La prima proposta si basa sul presupposto di ‘mantenere attivo’ il sistema IGI anche in una fase post go-live, 
in modo da verificare la username e password SIC in fase dell’utilizzo della funzione di ‘Configurazione Ufficio 
SIC’. 
Quindi sostanzialmente si deve preservare il ‘vecchio’ metodo di login per avere la certezza che le credenziali 
del SIC inserite siano veritiere. A valle della verifica, il SIC procederà con l’associazione dall’utenza ADN e 
l’utenza 
SIC 
specificata 
scrivendo 
nelle 
tabelle 
CAS_PROFILE.UTENTE_ADN 
e 
CAS_PROFILE.ASSOC_UTENTE_IGI_ADN. 
Al termine dell’operazione di associazione, il sistema SIC deve ‘propagare’ l’informazione verso il profilatore 
della CAAA Nazionale ed ottenere la ‘certificazione’ del profilo stesso. 
 
 
Per questa proposta, però, ci sono però dei vincoli da considerare: 
• 
Occorre mantenere attiva in esercizio l’istanza dall’appliance IGI; 
• 
Occorre mantenere attiva un istanza di oracle 12 su cui appoggiare IGI, in quanto l’attuale versione 
di IGI (5.2.2.1) non è certificata su oracle 19; 
• 
Eliminare le polices sulle password (es: disabilitazione dopo tot. Tempo di inattività.. ); 
 
 
La seconda proposta, è basata sempre sulla digitazione dello username e password SIC da parte dell’utente. 
In questo caso, però non sarà invocato il metodo di login per il controllo delle credenziali del SIC. 
L’intervento prevede che, a partire dalla password digitata dall’utente, il sistema andrà ad applicare alla 
stessa, la funzione di criptazione SHA-256 e andrà a verificare se l’output ottenuto corrisponde alla password 
‘criptata’ dell’utente ‘registrata’ nella tabelle del nuovo profilatore SIC.  
 
Vincolo da considerare:  
• 
Questa proposta richiede l’utilizzo di una o più librerie per la verifica di cifrature basate sull’algoritmo 
SHA-256.  Si può valutare se appoggiarsi sulle stesse librerie adoperate da IGI o basarsi su altre librerie 
con licenza open.  
 
La terza proposta, per dare ‘garanzia’, alla veridicità dello username SIC inserito dall’utente, prevede 
l’introduzione di una sezione in cui l’utente deve digitare la risposta alla domanda segreta. 
 
Quindi, accedendo alla funzione di ‘Configura ufficio SIC’, il sistema mostra una pagina simile a quanto 
riportato nella figura che segue:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 27/46 
 
Figura 18: Pagina configurazione ufficio SIC 
 
A valle dell’inserimento dello userName SIC, il sistema mostra, quindi, un’ulteriore sezione in cui l’utente 
deve digitare la risposta alla domanda segreta registrata per la sua utenza nel sistema SIC. 
 
 
Figura 19: Pagina per domanda segreta 
 
Il sistema ne verifica la correttezza, effettuando un controllo sulla tabella sy_risp_segr e prosegue con 
l’associazione dall’utenza ADN e l’utenza SIC specificata scrivendo nelle tabelle CAS_PROFILE.UTENTE_ADN 
e CAS_PROFILE.ASSOC_UTENTE_IGI_ADN. 
Nella casistica in cui l’utente non ricordi la domanda segreta, può optare per il recupero della stessa, 
utilizzando la ‘nuova’ funzione di ‘recupero domanda segreta’. In questo caso l’utente deve specificare la sua 
email ed il sistema invia un messaggio contenente la risposta per la sua utenza. 
 
Al termine dell’operazione di associazione, il sistema SIC deve ‘propagare’ l’informazione verso il profilatore 
della CAAA Nazionale per ottenere, eventualmente, la ‘certificazione’ del profilo stesso.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 28/46 
 
Questa ultima proposta è sicuramente quella che offre un livello di sicurezza minore, ma è totalmente 
svincolato dalla componente IGI. In ogni caso, però l’utente che arriva su questa form di ‘riconoscimento’ è 
stato già autenticato su NetIQ dal portale MyGiustizia . 
 
Scenario punto 3: 
 
E’ la casistica in cui l’utente ADN non possiede utenza su SIC (ex utenze IGI). 
In questo deve essere attivata la procedura di richiesta autorizzativa per l’utilizzo dell’applicazione, tramite 
la componente CAAA Request Manager.  
A valle di tutto il flusso autorizzativo, la CAAA propaga l’informazione al sistema SIC il quale provvederà a 
‘registrare’, nelle proprie tabelle le informazioni di interesse.  
Il SIC si interesserà di scrivere pertanto nelle tabelle CAS_PROFILE.PERSON P, CAS_PROFILE.UTENTE_ADN e 
CAS_PROFILE.ASSOC_UTENTE_IGI_ADN, avendo cura di creare un identificativo fittizio per l’utente, in modo 
da ‘garantire’ l’attuale dinamica di multi profilazione ad oggi adottata per l’applicazione del SIC. 
 
A questo punto, l’utente, ottenuta l’autorizzazione e la profilazione necessaria per accedere al SIC, in fase di 
accesso all’applicazione troverà impostato l’ufficio per cui è stato accreditato. La pagina mostrata dal SIC è la 
medesima riportata in Figura 16.  
Per questo scenario, l’utente non potrà usufruire della funzione di ‘Configurazione Ufficio SIC’, in quanto 
l’utente non detiene una vecchia userName SIC. 
 
3.3 REQ-SIC-003_2019-03 – Mappatura utenti SIC – ADN per sistema SIPPI/SITMP 
 
I processi di interconnessione attualmente presenti tra SIPPI/SITMP ed il SIC sono: 
➢ Iscrizione di Provvedimenti Principale di Misure di Prevenzione 
➢ Iscrizione di Provvedimenti dell'Esecuzione di Misure di Prevenzione 
➢ Richiesta di certificati di tipologia Autorità Giudiziaria (art.21 comma 1 del T.U.) e Pubblico Ministero 
(art.21 comma 1 del T.U.) 
3.3.1 Iscrizione di Provvedimenti Principale e dell’Esecuzione di Misure di Prevenzione 
Il sistema SIC fornisce due servizi web che gestiscono rispettivamente la recezione in ingresso di un 
provvedimento principale di misure di prevenzione e di un provvedimento dell’esecuzione di Misure di 
Prevenzione. 
Lo scopo principale di tali servizi è permettere al sistema fonte SIPPI/SITMP di ‘alimentare’ la banca dati del 
Casellario, di provvedimenti relativi ad una misura personale stabilita per un soggetto, quando questa diventa 
definitiva (“evento di definizione”). 
 
Entrambi i servizi prevedono in input l’oggetto ‘DATICHIAMATATRASFERIMENTO’ che si compone delle 
seguenti strutture dati principali: 
• 
DATI_UTENTE

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 29/46 
• 
DATI_OPERAZIONE 
• 
ANAGRAFICA 
 
La Struttura ANAGRAFICA contiene i dati anagrafici del soggetto imputato ed i dati del procedimento oggetto 
di invio da parte di Sippi. La struttura DATI_OPERAZIONE permette di individuare il tipo di operazione 
invocata dal sistema SIPPI (INSERIMENTO, MODIFICA, CANCELLAZIONE), mentre la struttura DATI_UTENTE 
permette di individuare i dati dell’utente e l’ufficio da cui è ‘in arrivo’ il procedimento (principale o di 
esecuzione) di misure di prevenzione. 
 
 
 
Come si può notare, nella struttura dati in arrivo dal sistema SIPPI/SITMP, è previsto anche l’invio dello 
USERNAME_SIPPI che nello specifico corrisponde allo user delle credenziali ADN giustizia. 
 
Nell’ottica di implementare l’attività di mapping tra utenze ADN ed utenze SIC, ed in virtù del fatto che il 
flusso dati di scambio già prevede l’invio dello user name ADN, per il servizio di ‘Iscrizione Provvedimento 
Principale’ e per il servizio di ‘Iscrizione Provvedimento Esecuzione’, non si prevede nessun intervento di 
rettifica allo stub dei servizi esposti. 
 
Il sistema SIC, a valle della recezione dei dati, può trovarsi difronte a due casistiche specifiche: 
• 
Lo USERNAME_SIPPI è già presente nella tabella sy_utenti_sippi e ciò significa che l’utente è già in 
possesso di un’utenza SIC.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 30/46 
Il sistema SIC verifica se esiste una corrispondenza tra user ADN ed user SIC, consultando le tabelle 
CAS_PROFILE.UTENTE_ADN, CAS_PROFILE.ASSOC_UTENTE_IGI_ADN E CAS_PROFILE.PERSON 
 
Per corrispondenza non trovata: 
 
Il SIC procederà con l’associazione dell’utenza ADN con l’utenza SIC individuata per l’utente, 
scrivendo nelle tabelle CAS_PROFILE.UTENTE_ADN, CAS_PROFILE.ASSOC_UTENTE_IGI_ADN e 
CAS_PROFILE.PERSON. 
 
Il sistema a questo punto permetterà di procedere con l’invocazione dei servizi. 
 
• 
Lo USERNAME_SIPPI NON è presente nella tabella sy_utenti_sippi e quindi l’utente NON è in 
possesso di un’utenza SIC. 
Per questo scenario il sistema, attualmente, procede con una creazione automatica dell’utenza SIC e 
contestualmente procede con il suo ‘impiego’ in un specifico ufficio SIC, individuato a partire dai dati 
codice_tipo_ufficio e codice_sede_ufficio specificati nella struttura DATI_UFFICIO presente in 
DATI_UTENTI. Inoltre provvede anche ad un’assegnazione automatica di alcuni ruoli specifici. 
 
Tale meccanismo, in base a quanto previsto con l’introduzione del work flow della CAAA Request 
Manager, sarà eliminato. L’applicativo SIC, non potrà più essere responsabile di un flusso di 
profilazione per un utente e ciò implica che tutti i ‘nuovi’ utenti che vorranno fare accesso ai servizi 
di invio provvedimenti verso il SIC, dovranno effettuare un invio di una richiesta di autorizzazione, 
per mezzo dello strumento di profilazione della CAAA. 
  
Il sistema SIC, pertanto, per un tentativo di accesso ai servizi da parte di utenti non censiti in 
CAS_PROFILE.UTENTE_ADN, 
CAS_PROFILE.ASSOC_UTENTE_IGI_ADN 
e 
CAS_PROFILE.PERSON, 
restituirà un apposito messaggio di ‘accesso negato’. 
 
3.3.2 Richiesta di certificati di tipologia Autorità Giudiziaria (art.21 comma 1 del T.U.) e Pubblico Ministero 
(art.21 comma 1 del T.U.) 
 
L’utente SIPPI ha la possibilità di richiedere il certificato del Casellario richiamando il Web Service (Richiesta 
Certificato) esposto dal sistema SIC. 
Ad oggi, il servizio di richiesta del certificato del Casellario (ART. 21 D.P.R. 14/11/2002 N.313) può essere 
richiesto solo dagli utenti SIPPI censiti su SIC, ossia utenti che sono in possesso delle credenziali di accesso al 
SIC.  
Attualmente, in fase di invocazione di questo servizio è necessario indicare, nel SOAP-HEADER della chiamata, 
due parametri: username e password.  
Ciò che il sistema SIC si aspetta di ricevere, sono la userid e la password dell’utente SIPPI adottate per la login 
nel sistema SIC, quindi le credenziali SIC.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 31/46 
La proposta che si vuole avanzare è quella di fare in modo che in fase di ‘invocazione’ del servizio non vengano 
più passate le credenziali del SIC, ma inviato soltanto lo userName ADN dell’utente. 
 
Essendo il sistema SIPPI/SITMP già integrato con l’autenticazione su ADN, si ha certezza che per lo userName 
ADN che sarà specificato nel SOAP-HEADER, sia relativo ad un utente censito e riconosciuto su LDAP giustizia. 
 
Il sistema target SIC si ‘fiderà’ delle credenziali inviate dal sistema fonte SIPPI/SITMP. 
 
 
Vediamo nello specifico le modifiche da implementare: 
 
 
1. INTERVENTI LATO SITMP/SIPPI 
 
In fase di ‘invocazione’ del servizio di richiesta certificato, il sistema SIPPI/SITMP deve essere modificato in 
modo che, in fase di chiamata del servizio, invii in ‘background’ lo userName ADN, inserendo tale parametro 
nel SOAP-HEADER della chiamata. 
 
2. INTERVENTI LATO SIC 
 
In fase di recezione della chiamata per il servizio di richiesta certificato, il sistema deve ‘recuperare’ il valore 
‘username ADN’ presente nel SOAP-HEADER ed effettuare i seguenti controlli: 
• 
Il sistema SIC deve verificare che ci sia un’associazione, già configurata a sistema, tra utenza ADN ed 
utenza SIC. In caso di NON esistenza di nessuna associazione il sistema deve restituire un errore di 
‘mapping non presente’. 
• 
Nella casistica di ‘mapping’ presente, tra utenza ADN ed utenza SIC, il sistema verifica se l'utente è 
abilitato alla stampa del certificato tramite SIPPI. Se l’utente non risulta abilitato alla stampa, in 
quanto non ha dei precisi ruoli, il sistema restituisce un messaggio di errore. 
• 
Se l’utente risulta assegnatario di ruoli e permessi di stampa, il sistema procede con la stampa del 
certificato richiesto. 
 
3.4 REQ-SIC-003_2019-04 – Mappatura utenti SIC – ADN per sistema SIES 
 
I processi di interconnessione presenti tra SIES e SIC sono: 
• 
Invio titoli esecutivi da SIES verso il SIC 
• 
Invio dei fogli complementari da SIES verso il SIC 
• 
Invio provvedimento di cumulo da SIES verso il SIC 
• 
Richiesta del certificato Penale 
• 
Accesso al modulo WEB di interconnessione SIES-NSC 
• 
Recupero di provvedimenti principali dal SIC sul SIES

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 32/46 
 
3.4.1 Invio Procedimenti (Titoli Esecutivi, Fogli Complementari e Cumuli) 
Per la recezione dei procedimenti da SIES, il sistema SIC espone dei servizi web che prevedono in ingresso 
una struttura dati UTENTE, in cui sono specificate le seguenti informazioni: 
 
 
 
In chiamata del servizio, il sistema SIES invia i dati identificativi dell’ufficio e i dati per il riconoscimento utente. 
 
Attualmente il SIC, a partire da questi dati, va a verificare se esiste un’associazione tra lo username del SIES 
e lo userName del SIC nella tabella sy_utenti_Sies e per dati non trovati, effettua una creazione automatica 
dell’utenza SIC. Contestualmente procede con il suo ‘impiego’ in un specifico ufficio SIC, individuato a partire 
dai dati codiceTipo, codiceSede e codiceDistretto specificati nella struttura UFFICIO.  
 
Tale meccanismo, in base a quanto previsto con l’introduzione del work flow della CAAA Request Manager, 
sarà eliminato. L’applicativo SIC, non potrà più essere responsabile di un flusso di profilazione per un utente 
e ciò implica che tutti i ‘nuovi’ utenti che vorranno fare accesso ai servizi di invio provvedimenti verso il SIC, 
dovranno effettuare un invio di una richiesta di autorizzazione, per mezzo dello strumento di profilazione 
della CAAA. 
  
Il sistema SIC, pertanto, per un tentativo di accesso ai servizi da parte di utenti non censiti nella tabella 
SY_UTENTI_SIES restituirà un apposito messaggio di ‘accesso negato’. 
 
Detto ciò però è necessario intervenire in ogni caso con una modifica dell’attuale struttura dati UTENTI 
passata in INPUT ai servizi di ‘invio’, in modo che venga inviata anche l’utenza ADN associata all’utenza SIES. 
Per i dettagli implementativi per SIES fare riferimento al par. 3.6. 
 
In questo modo, alla stregua di quanto specificato per l’applicazione SIC, nella fase pre go-live, il sistema SIC 
potrà effettuare le associazioni tra le utente SIES e le utenze SIC a partire da una specifica utenza ADN. 
Il sistema, pertanto, a valle del riconoscimento dell’utente nella tabella SY_UTENTI_SIES, potrà procedere 
con l’inserimento nelle tabelle CAS_PROFILE.UTENTE_ADN, CAS_PROFILE.ASSOC_UTENTE_IGI_ADN e 
CAS_PROFILE.PERSON.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 33/46 
Il servizio, quindi continuerà ad essere garantito per le utenze già esistenti in SIC e registrate in uffici di 
tipologia SIES. 
 
3.4.2 Modulo di interconnessione WEB 
L’interconnessione al modulo WEB SIES-NSC, è basato sull’utilizzo del token SAML. In fase di accesso alla 
context root della web-app SIES, il sistema SIC verifica se nella request è presente il parameter ‘tokenSAML’. 
Tale token è cifrato con la chiave pubblica di casellario.giustia.it e contiene i dati identificativi dell’Utente 
SIES che sta richiedendo l’accesso al modulo web SIES-NSC. 
I dati inviati sono: 
• 
codiceSede  
• 
CodTipoUfficio 
• 
CognomeUtente  
• 
NomeUtente  
• 
Distretto  
• 
HostAddress 
• 
IdUtente 
• 
Sistema 
 
A partire da tali dati, il sistema SIC invoca un servizio che controlla se l'utente che sta facendo accesso al 
modulo risulta già registrato a sistema (tabella SY_UTENTI_SIES). In caso di utenza SIC non presente, il sistema 
procede con una creazione automatica dell’utenza SIC e contestualmente procede con il suo ‘impiego’ in un 
specifico ufficio SIC, individuato a partire dai dati CodTipoUfficio  e codiceSede specificati nella struttura 
presente nel token inviato. Inoltre provvede anche ad un’assegnazione automatica di alcuni ruoli specifici. 
 
Tale meccanismo, in base a quanto previsto con l’introduzione del work flow della CAAA Request Manager, 
sarà eliminato. L’applicativo SIC, non potrà più essere responsabile di un flusso di profilazione per un utente 
e ciò implica che tutti i ‘nuovi’ utenti che vorranno fare accesso alla web app di interconnessione verso il SIC, 
dovranno effettuare un invio di una richiesta di autorizzazione, per mezzo dello strumento di profilazione 
della CAAA. 
  
Il sistema SIC, pertanto, per un tentativo di accesso ai servizi da parte di utenti non censiti nella tabella 
SY_UTENTI_SIES restituirà un apposito messaggio di ‘accesso negato’. 
 
Detto ciò però è necessario intervenire in ogni caso con una modifica dell’attuale struttura del token SAML, 
in modo che venga inviata anche l’utenza ADN associata all’utenza SIES. Per i dettagli implementativi per SIES 
fare riferimento al par. 3.6. 
 
In questo modo, alla stregua di quanto specificato per l’applicazione SIC, nella fase pre go-live, il sistema SIC 
potrà effettuare le associazioni tra le utente SIES e le utenze SIC a partire da una specifica utenza ADN.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 34/46 
Il sistema, pertanto, a valle del riconoscimento dell’utente nella tabella SY_UTENTI_SIES, potrà procedere 
con l’inserimento nelle tabelle CAS_PROFILE.UTENTE_ADN, CAS_PROFILE.ASSOC_UTENTE_IGI_ADN e 
CAS_PROFILE.PERSON. 
 
 
3.4.3 Servizio di Richiesta Certificati  
Il servizio di richiesta dei certificati è il medesimo esposto al par. 3.3.2 per il sistema fonte SIPPI/SITMP. 
 
Per il sistema SIES deve essere previsto lo stesso comportamento descritto al paragrafo su indicato. 
La proposta che si avanza quindi è quella di fare in modo che in fase di ‘invocazione’ del servizio dal ‘client’ 
SIES, venga passato lo username ADN invece delle attuali credenziali adottate per la login su SIC. 
 
Tale requisito è correlato a quanto esplicitato al par 3.6 in cui si delineano le attività propedeutiche da 
implementare sul sistema SIES. 
 
Vediamo nello specifico le modifiche da implementare: 
 
 
1. INTERVENTI LATO SIES 
 
In fase di ‘invocazione’ del servizio di richiesta certificato, il sistema SIES deve essere modificato in modo che, 
in fase di chiamata del servizio, invii in ‘background’ lo userName ADN, inserendo tale parametro nel SOAP-
HEADER della chiamata. 
 
2. INTERVENTI LATO SIC 
 
In fase di recezione della chiamata per il servizio di richiesta certificato, il sistema deve ‘recuperare’ i valori 
per ‘username’ e ‘password’ presenti nel SOAP-HEADER ed effettuare i seguenti controlli: 
• 
Il sistema SIC recupera lo userName ADN e deve verificare che ci sia un’associazione, già configurata 
a sistema, tra utenza ADN ed utenza SIC. In caso di NON esistenza di nessuna associazione il sistema 
deve restituire un errore di ‘mapping non presente’. 
• 
Nella casistica di ‘mapping’ presente, tra utenza ADN ed utenza SIC, il sistema verifica se l'utente è 
abilitato alla stampa del certificato tramite SIES. Se l’utente non risulta abilitato alla stampa, in 
quanto non ha dei precisi ruoli, il sistema restituisce un messaggio di errore. 
• 
Se l’utente risulta assegnatario di ruoli e permessi di stampa, il sistema procede con la stampa del 
certificato richiesto. 
 
3.5 REQ-SIC-003_2019-05 – Mappatura utenti SIC – ADN per sistema Cerpa WEB

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 35/46 
In relazione alla dismissione dello strumento IGI (Ibm Security Identity Governance & Intelligence), si delinea 
la necessità di ‘rivedere’ la modalità di accesso ed utilizzo anche dell’Applicazione CERPA WEB. 
 
Tale applicazione è stata creata con lo scopo di permettere a degli Enti di Pubblica Amministrazione, previa 
stipula di apposita convenzione con il Ministero della Giustizia, di ‘registrarsi’ e di poter effettuare la richiesta 
di stampa di un certificato penale. 
 
Nonostante ad oggi questa applicazione sia in linea, non è ancora adottata quale strumento di accesso ai 
servizi posti on-line per gli Enti di Pubblica Amministrazione. 
 
Si ricorda che le utenze abilitate per accedere al servizio del sito sono di 3 tipologie:  
 
• utente Responsabile del Servizio PEC (Referente);  
• utente Responsabile Tecnico PEC;  
• utente Responsabile del Servizio PD; 
 
Tali tipologie di utenze sono identificabili dai seguenti ruoli ad esse associate: 
• 
Responsabile_Tecnico_PEC 
• 
Responsabile_Servizio_PEC 
• 
Responsabile Servizio PD  
 
 
In generale, le utenze che hanno accesso a tale applicazione non sono utenti ADN pertanto sono privi di 
credenziali riconosciute dall’ADN nazionale di Giustizia. 
In virtù di ciò, e nell’ottica delle attività di rifacimento del portale ai Cittadini, per tale applicazione si propone 
di non effettuare nessun intervento specifico. 
 
In ogni caso, per garantire l’accesso ai pochi utenti ad oggi abilitati, a valle della dismissione di IGI, per la 
verifica delle credenziali di accesso, ci si appoggerà alla proposta 2 prevista al par. 3.2.1, ossia effettuare una 
verifica tramite algoritmo di criptazione SHA-256 della password. 
 
 
3.6 REQ-SIC-003_2019-06 – Mappatura utenti SIES – ADN per sistema SIES 
 
Nell’ottica di predisporre il sistema SIES all’integrazione con l’autenticazione basata sulle utenze di ADN di 
Giustizia, e di garantire continuità delle interconnessioni ad oggi in essere verso il SIC, si propone di 
intervenire sulla pagina di accesso al SIES in modo da ‘iniziare’ ad alimentare ed arricchire la banca dati con 
le associazioni dell’utenza ADN rispetto all’ufficio o gli ‘n’ uffici con cui l’utente è profilato attualmente sul 
SIES rispetto anche ai sottosistemi SIEP, SIUS e SIGE. 
 
L’attività che si vuole ‘anticipare’ è la procedura di mapping tra l’utenza ADN di cui ogni utente è proprietario, 
e le utenze che lo stesso utente ha sul sistema SIES.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 36/46 
La proposta che si vuole avanzare è la seguente: 
 
L’utente si trova sulla pagina di Login del SIES. Il sistema propone la pagina di accesso in cui l’utente sarà 
tenuto ad inserire le proprie credenziali ADN, in deroga a quanto attualmente previsto dal sistema SIES che 
chiede l’inserimento delle credenziali SIES. 
In realtà questo ‘nuovo’ modo di lavorare anticipa, in qualche modo, ciò che a tendere avverrà per l’accesso 
unico ai sistemi penali, dove appunto è prevista un’autenticazione basata sulle credenziali ADN Nazionale. 
 
Si riporta di seguito un esempio della pagina di accesso al SIES: 
 
 
Figura 20: Pagina di accesso al SIES 
 
A seguito dell’azione di ‘submit’ delle credenziali, il sistema effettua un controllo sulla ‘autenticità’ delle 
informazioni inserite effettuando una chiamata LDAP sul server ADN di Giustizia (per i dettaglio vedi 3.1.1). 
 
Per dati esatti, il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione 
delle utenze SIES, così come riportato nell’immagine che segue, mentre per dati non corrispondenti, sarà 
visualizzato apposito messaggio di errore.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 37/46 
 
Figura 21: Pagina di selezione Account SIES 
 
Dalla form prospettata, con la selezione della procedura di ‘selezione/configura Account’, all’utente sarà 
mostrata la pagina per l’inserimento delle credenziali del SIES: 
 
 
Figura 22: Pagina per selezione Account 
 
A seguito dell’inserimento delle credenziali del SIES, il sistema effettuerà i seguenti controlli:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 38/46 
• 
Login sul sistema SIES con verifica della corrispondenza username e password inseriti; 
Il sistema si interessa di effettuare la consueta procedura di login su SIES. Non è prevista nessuna 
modifica al flusso implementativo a tale funzione. 
• 
Verifica della presenza a sistema dell’associazione utenza SIES specificata ed utenza ADN; 
Il sistema deve fare accesso alla tabella ASSOC_UTENTE_SIES_ADN e verificare che esista un record 
per lo user SIEP (COD_UTENTE) specificato in fase di login. Per record individuato, il sistema recupera 
i dettagli dell’utente e dell’ufficio e mostra la pagina per l’accesso alla home page del sies (vedi Figura 
22). Per i dettagli delle tabelle interessate, fare riferimento al par. 3.10.4 
• 
In caso di NON associazione dell’utenza, il sistema procederà con l’accoppiamento delle utenze 
scrivendo il dato in un’apposita tabella che sarà creata sul sistema SIES; 
Nella casistica in cui, non esiste nessuna associazione tra utenza SIES ed utenza ADN, il sistema deve 
occuparsi di ‘registrare’ i dati nella tabella ASSOC_UTENTE_SIES_ADN e nella tabella UTENZA_ADN. 
Per i dettagli delle tabelle fare riferimento al par. 3.10.4 
 
• 
In caso di associazione GIA’ presente, il sistema mostrerà un messaggio di utente riconosciuto per 
l’ufficio scelto; 
• 
In ogni caso l’utente può procedere con la configurazione di eventuale ogni altro account di cui 
dispone per l’accesso al SIES; 
 
 
 
Figura 22: Pagina associazione utenza SIES

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 39/46 
A questo punto l’utente selezionando il tasto ‘Entra’ sarà ridiretto nella welcome page dell’applicazione del 
SIES: 
 
 
Figura 23: Welcome page SIES 
 
 
Proseguendo invece con la funzione di ‘Seleziona/Configura un account’, il sistema mostrerà nuovamente la 
form di inserimento utenza e password SIES come alla Figura 22. 
 
Configurando ogni account, l’utente completerebbe, sotto la propria responsabilità, la procedura di match 
tra la propria utenza ADN con le multi utenze del SIES. 
 
Al successivo accesso, se l’utente ha eseguito delle associazioni, si ritroverà, già configurate, le utenze che 
utilizza solitamente per l’accesso al SIES.  
 
Si riporta a seguire un esempio di pagina:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 40/46 
 
Figura 24: Pagina di scelta utenza 
 
L’utente pertanto può selezionare l’utenza di interesse, inserire la password ed iniziare la navigazione nel 
SIES, oppure configurare ed entrare con un account diverso. 
 
3.7 Moduli sw  
I moduli interessati sono: 
Per SIC: 
- 
modulo Page, SICSBRS 
- 
modulo SiesWEB, SiesEJB e SiesSAML 
- 
modulo SippiWEb e SippiEJB. 
Per SIES: 
- 
sies.war 
Per SIPPI/SITMP: 
- 
smp.war 
3.8 Architettura  
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 41/46 
3.9 Interfacce utente 
Per le interfacce utente, fare riferimento alle singole immagini riportate nei paragrafi precedenti. 
 
3.10 Basi dati 
 
3.10.1 Tabelle associative utenza ADN utenze SIC – SISTEMA SIC 
La tabella CAS_PROFILE.ASSOC_UTENTE_IGI_ADN contiene l’associazione tra l’identificativo dell’utenza SIC 
e l’identificativo dell’utenza ADN. 
 
 
La tabella CAS_PROFILE.UTENTE_ADN conserva le informazioni dello username dell’utenza ADN; 
 
Sono tabelle la cui creazione è prevista a seguito della scheda di dismissione IGI (RIF.1). 
 
 
3.10.2 Tabelle per il controllo della domanda segreta – SISTEMA SIC 
La tabella DC_TAB_DOMANDE_SEGRETE e la tabella SY_RISP_SEGR contengono rispettivamente la tipologia 
di domanda segreta che può essere scelta e la risposta alla domanda segreta prescelta per ogni utente. 
Per tali tabelle non sono previste operazioni di ALTER TABLE. Sono utilizzate solo in lettura.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 42/46 
 
3.10.3 Tabelle per il controllo utenti SIPPI ed utenti SIES – SISTEMA SIC 
La tabella SY_UTENTI_SIPPI e la tabella SY_UTENTI_SIES conservano rispettivamente le associazioni tra le 
utente SIC e le utenze di SIPPI e di SIES. 
Per tali tabelle non sono previste operazioni di ALTER TABLE. Sono utilizzate solo in lettura. 
 
3.10.4 Tabelle per mapping utenza ADN ed utenza SIES – SISTEMA SIES 
Nel sistema SIES devono essere previste le seguenti nuove tabelle: 
• 
ASSOC_UTENTE_IGI_ADN 
• 
UTENZA_ADN 
La prima tabella è deputata a ‘conservare’ l’associazione tra la tabella UTENTE e la tabella UTENZA_ADN; 
 
La tabella UTENZA_ADN, conserva le informazioni dello username dell’utenza ADN; 
 
3.11  WEB services 
I web services che vengono modificati da quanto riportato in tale scheda sono esplicitati al par. 3.4.1. 
In particolare i servizi oggetto di modifica alla struttura dati di ingresso sono:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 43/46 
• 
iscriviProvvedimentoProvvisorio 
• 
iscriviProvvedimentoEsecuzione_NEW 
• 
trasferisciFoglioComplementare 
Per tali servizi si prevede di modificare la struttura DATI_UTENTI che in aggiunta dovrà prevedere il tag 
USER_ADN. 
3.12 XSD 
Gli xsd su cui occorre intervenire sono quelli relativi ai servizi esposti al paragrafo precedente. 
Gli xsd interessati sono 3 e la modifica interesserà la struttura DATI_UTENTI che in aggiunta dovrà prevedere 
il tag USER_ADN. 
Esempio: 
<type:DATI_UTENTE> 
<type:DATI_UFFICIO> 
<type:CODICE_TIPO_UFFICIO>301</type:CODICE_TIPO_UFFICIO> 
<type:CODICE_SEDE_UFFICIO>001191</type:CODICE_SEDE_UFFICIO> 
<type:CODI_DISTRETTO>001272</type:CODI_DISTRETTO> 
<type:CODI_SISTEMA>SIEP</type:CODI_SISTEMA> 
</type:DATI_UFFICIO> 
<type:USERNAME>AXXXX</type:USERNAME> 
<type:COGNOME_UTENTE>assistenza</type:COGNOME_UTENTE> 
<type:NOME_UTENTE>siep</type:NOME_UTENTE> 
<type:USER_ADN>nome.cognome</type:USERNAME> 
<type:IP_ADDRESS_SERVER>10.5.207.139:8080</type:IP_ADDRESS_SERVER> 
</type:DATI_UTENTE> 
3.13 Configurazione 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 44/46 
3.14 Tutorial 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 45/46 
4 Piano delle attività 
4.1 Ciclo di sviluppo 
 
Il ciclo di sviluppo utilizzato è quello Waterfall. 
4.2 Vincoli 
N.A. 
4.3 Luogo di lavoro 
 
Le attività saranno espletate presso le sedi del RTI o presso la sede della DGSIA.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN Ver. 1.0 del 08/01/2021 
Pag. 46/46 
5 Dimensionamento 
5.1 Stima dell'effort previsto 
 
La stima in FP prevista sarà consegnata entro il 15 Gennaio.