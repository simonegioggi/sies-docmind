---
uniqueName: siut-sie-si-1-2-20240318specificheinterventomev202
displayName: "SIUT SIE SI 1 2 20240318 Specifiche Intervento MEV 2023 035 SIUS Riforma Cartabi"
category: "GENERAL"
tags: []
---

# SIUT-SIE-SI-1.2-20240318_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia

> **File originale:** `MEV/SCHEDA_035/SIUT-SIE-SI-1.2-20240318_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
 
Specifiche Intervento MEV_2023_035 SIUS 
Riforma Cartabia 
 
 
 
 
 
 
 
 
Versione 1.2 del 18/03/2024

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 2/55 
 
 
 
 
 
 
Il presente documento è stato redatto con la collaborazione 
del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA 
S.r.l. nell’ambito del contratto CIG 73479643B7 per lo 
“Sviluppo del Sistema Informativo Unitario Telematico, la 
manutenzione degli attuali sistemi dell’area Penale del 
Ministero della Giustizia e servizi correlati. Lotto 1”.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 3/55 
Approvazioni 
 
Nominativo 
Elaborato da 
Umberto Mignogna 
Verificato da 
Vito Bufi 
Approvato da 
Paolo Ceccanti 
Data approvazione 
23/02/2024 
Livello di riservatezza 
L3 
 
Elenco versioni 
Versione 
Data  
Motivo 
Modifica 
1.0 
04/07/2023 
 
Prima Emissione 
1.1 
23/02/2024 
 
Rivisto l’intero documento integrandolo con le 
osservazioni del GdL SIUS, contenuto nel 
documento 
CARTABIA_SIUT-SIE-SI-1.0-
20230704_versione_09_01_24.docx 
1.2 
18/03/2024 
 
Pag. 16 par.3.4 – Eliminato “Tribunale di 
Sorveglianza competente” da form ordinanza 
Pag. 28 par.3.13 – Corretta denominazione primo 
oggetto 
Pag. 33 par.3.17 – Modificati i primi due oggetti 
Pag. 35 par.3.19 – Rivisto paragrafo in base a 
punto b) documento Conversioni_Cartabia.docx 
Pag. 41 par.3.23 – Rivisto paragrafo in base a 
punto a) documento Conversioni_Cartabia.docx 
Aggiunti parr. 3.25, 3.26 in base a documento 
Conversioni_Cartabia.docx 
Parr. 3.27, 3.28 – rinumerati precedenti parr. 
3.25 e 3.26 
 
Lista di distribuzione 
Nominativo 
Organizzazione 
Ufficio 
Funzione 
Aurora Garofalo 
Amministrazione 
 
Responsabile Unico Procedimento 
Oris Orlando 
Amministrazione 
 
Direttore Esecutivo Contratto 
Paolo Ceccanti 
RTI 
 
Responsabile Unico Fornitura 
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 4/55 
Francesco Rosati 
RTI 
 
Referente qualità 
Andrea Castorino 
Alessandro Lanari 
RTI 
 
Referente Applicativo Gestore Fascicolo 
Documentale

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 5/55 
INDICE DEI CONTENUTI 
1 
INTRODUZIONE ............................................................................................................................... 7 
1.1 
SCOPO DEL DOCUMENTO .......................................................................................................................... 7 
1.1.1 
Riferimenti .................................................................................................................................................. 7 
1.2 
GLOSSARIO ............................................................................................................................................. 7 
1.2.1 
DEFINIZIONI ........................................................................................................................................ 7 
1.2.2 
ACRONIMI E ABBREVIAZIONI .................................................................................................................. 7 
2 
ARCHITETTURA DEL SISTEMA ......................................................................................................... 10 
2.1 
ARCHITETTURA ...................................................................................................................................... 10 
2.2 
WEB SERVICES ...................................................................................................................................... 10 
2.3 
XSD .................................................................................................................................................... 10 
2.4 
CONFIGURAZIONE .................................................................................................................................. 10 
2.5 
TUTORIAL ............................................................................................................................................. 10 
3 
DESCRIZIONE DELL’INTERVENTO .................................................................................................... 11 
3.1 
APPLICAZIONE PENE SOSTITUTIVE (ART. 62 L. 689/81) ............................................................................... 11 
3.2 
PROGRAMMA DI TRATTAMENTO PER SEMILIBERTÀ SOSTITUTIVA (ART. 55 L. 689/81) ...................................... 12 
3.3 
ESECUZIONE PENE SOSTITUTIVE ............................................................................................................... 13 
3.4 
SOSPENSIONE ESECUZIONE PENE SOSTITUTIVE ........................................................................................... 15 
3.5 
AUTORIZZAZIONE PENE SOSTITUTIVE ........................................................................................................ 18 
3.6 
MODIFICA MODALITÀ DI ESECUZIONE PENE SOSTITUTIVE ............................................................................. 19 
3.7 
REVOCA AUTORIZZAZIONE/MODIFICA PRESCRIZIONI PENE SOSTITUTIVE ......................................................... 21 
3.8 
REVOCA PENE SOSTITUTIVE (ARTT. 66, 108 L. 689/81).............................................................................. 22 
3.9 
REVOCA PENE SOSTITUTIVE (ART. 72 L. 689/81) ....................................................................................... 24 
3.10 
RECLAMO AVVERSO REVOCA PENA SOSTITUTIVA   (PER TDS) .................................................................... 25 
3.11 
DIFFIDA AL PUNTUALE RISPETTO DELLE PRESCRIZIONI – PENE SOSTITUTIVE ................................................... 26 
3.12 
GESTIONE LICENZA - PENE SOSTITUTIVE ................................................................................................. 28 
3.13 
LICENZA - PENE SOSTITUTIVE - INOSSERVANZA PRESCRIZIONI (ART. 69 L. 689/81) ....................................... 29 
3.14 
SOSPENSIONE LAVORO PUBBLICA UTILITÀ SOSTITUTIVO ............................................................................. 30 
3.15 
RINVIO DELL’ESECUZIONE PENA SOSTITUTIVA (UDS) ................................................................................ 31 
3.16 
RINVIO DELL’ESECUZIONE PENA SOSTITUTIVA (TDS) ................................................................................. 32 
3.17 
RINVIO DELL’ESECUZIONE  PENA SOSTITUTIVA DERIVANTE DA CONVERSIONE PENE PECUNIARIE  (UDS) ............ 34 
3.18 
RINVIO DELL’ESECUZIONE PENA SOSTITUTIVA DERIVANTE DA CONVERSIONE PENE PECUNIARIE (TDS) .............. 35 
3.19 
REVOCA E CONVERSIONE PENA PECUNIARIA SOSTITUTIVA ......................................................................... 36 
3.20 
SOPRAVVENIENZA NUOVO TITOLO - PENE SOSTITUTIVE ............................................................................. 37 
3.21 
SOSPENSIONE ESECUZIONE PENE ACCESSORIE (UDS) ................................................................................ 39 
3.22 
SOSPENSIONE ESECUZIONE PENE ACCESSORIE (TDS) ................................................................................ 41 
3.23 
CONVERSIONE/RATEIZZAZIONE PENA PECUNIARIA SOSTITUTIVA ................................................................ 42 
3.24 
CONVERSIONE PENE PECUNIARIE IRROGATE DAL GIUDICE DI PACE .............................................................. 45 
3.25 
GESTIONE PROCEDIMENTI ESECUZIONE PENE SOSTITUTIVE ....................................................................... 48 
3.26 
GESTIONE LICENZE – PENE SOSTITUTIVE ................................................................................................ 50 
4 
PIANO DELLE ATTIVITÀ .................................................................................................................. 53 
4.1 
CICLO DI SVILUPPO ................................................................................................................................. 53

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 6/55 
5 
PIANO DELLE ATTIVITÀ .................................................................................................................. 54 
5.1 
GANTT ................................................................................................................................................. 54 
5.2 
VINCOLI ............................................................................................................................................... 54 
5.3 
LUOGO DI LAVORO ................................................................................................................................. 54 
6 
DIMENSIONAMENTO ..................................................................................................................... 55 
6.1 
STIMA DELL’EFFORT ............................................................................................................................... 55 
6.2 
ATTIVITÀ MISURABILI IN PUNTI FUNZIONE .................................................................................................. 55 
6.3 
DETTAGLIO DEI COSTI ............................................................................................................................. 55

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 7/55 
1 Introduzione 
1.1 
Scopo del documento 
Il presente documento riporta le specifiche di intervento che saranno realizzate nell’ambito del sistema SIES, 
sottosistema SIUS, al fine di soddisfare i requisiti espressi dall’Amministrazione in relazione alla richiesta di 
adeguamento normativo del Sistema, nella sua interezza, al d.lgs. 10 ottobre 2022, n. 150  cd Riforma 
Cartabia,  alla Riforma Cartabia. 
L’intervento in oggetto è stato richiesto con comunicazione m_dg.DOG07AR.04/05/2023.0000747.U. 
Rientra nel servizio di Manutenzione Evolutiva ed è classificato come di seguito riportato: 
 
Scheda di Intervento  
2023_35  
Oggetto  
Integrazione Cartabia in SIUS    
Complessità  
Alta  
Servizio  
MEV  
 
Tale documento espone gli interventi attinenti alle funzioni da prevedere nel sistema in base alle novità 
normative della cd Riforma Cartabia (maggiorenni e minorenni). 
Con lo scopo di rendere l’intervento coerente ed auto consistente gli interventi dovranno tener conto 
dell’integrazione con gli altri sottosistemi (SIEP e SIGE). 
1.1.1 
Riferimenti 
Riferimento 
Nome Documento 
Descrizione Documento 
RIF1 
m_dg.DOG07AR.04_05_2023.0000747.U_Richiesta_scheda_20
23-35_SIES_Cartabia_con_SIUS_signed 
Richiesta Scheda di Intervento 
1.2 
Glossario 
1.2.1 Definizioni 
Definizione 
Descrizione 
 
 
1.2.2 Acronimi e abbreviazioni 
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 8/55 
Sigla 
Descrizione 
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
Sistema di Gestione per la Qualità di Engineering Ingegneria Informatica 
S.p.A. 
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
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 9/55

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 10/55 
2 Architettura del Sistema 
2.1 
Architettura 
L’intervento in oggetto non introduce variazioni architetturali, rispetto al sistema attuale. 
2.2 
WEB services 
N.A. 
2.3 
XSD 
N.A. 
2.4 
Configurazione 
N.A. 
2.5 
Tutorial 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 11/55 
3 Descrizione dell’Intervento 
Di seguito si riportano gli interventi necessari nel sottosistema SIUS per adeguarlo alle modifiche apportate 
dalla cosiddetta “Riforma Cartabia” ai singoli articoli del c.p.p. 
Per ciascun provvedimento riportato nei paragrafi successivi dalla form di Dettaglio sarà possibile attivare le 
funzioni di stampa, validazione, modifica e cancellazione. 
3.1 Applicazione Pene Sostitutive (art. 62 L. 689/81) 
In relazione all’art. 62 L. 689/81 la riforma non parla più di Sanzioni sostitutive ma di Pene Sostitutive nelle 
forme di Semilibertà sostitutiva e Detenzione Domiciliare sostitutiva, che possono essere applicate dal 
giudice in caso di condanna alla reclusione o all’arresto non superiori a quattro anni. Gli Uffici di Sorveglianza 
(UDS/UDSM) sono pertanto chiamati a pronunciarsi sull’applicabilità di tali pene sostitutive. A tal fine 
bisognerà prevedere la gestione di un nuovo procedimento con contenuto di “Applicazione Pene 
Sostitutive”. 
 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Applicazione Pene Sostitutive  
Al nuovo contenuto vanno associati i seguenti oggetti:  
• 
Semilibertà sostitutiva (art. 55 - 62 L. 689/1981)   
• 
 Detenzione domiciliare sostitutiva (art. 56 - 62 L. 689/1981) 
e i seguenti esiti 
• 
Determina le modalità di esecuzione  
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dispone restituzione atti al PM  
• 
Dichiara la propria incompetenza  
L’aggiunta dei suddetti elementi permetterà all’Ufficio di poter iscrivere procedimenti di Applicazione Pene 
Sostitutive, collegandosi direttamente al procedimento SIEP o a seguito di presa in carico di Richiesta 
Applicazione Pene Sostitutive trasmesse dalle Procure. 
Per la successiva definizione bisognerà realizzare l’ordinanza di applicazione delle pene sostitutive. Sarà, 
quindi, implementata una nuova funzionalità, emissione ordinanza applicazione pene sostitutive. La nuova 
maschera di inserimento sarà implementata sulla base di quella abbozzata di seguito.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 12/55 
 
A seguito della Conferma inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio, dalla 
quale sarà possibile attivare le azioni di  Modifica, Cancellazione, Stampa o Upload, Validazione e 
Trasmissione. 
L’ordinanza seguirà il normale percorso di altri provvedimenti, verrà quindi depositata e validata per essere 
trasmesso allo stesso Ufficio o ad altro ufficio, che procederà alla presa in carico e all’iscrizione di un 
procedimento di esecuzione della pena sostitutiva (cd Fascicolo padre) al quale faranno riferimento tutti i 
procedimenti afferenti alla gestione dell’esecuzione. 
L’ordinanza di applicazione viene trasmessa anche alla Procura perché provveda all’annotazione. 
3.2 Programma di trattamento per semilibertà sostitutiva (art. 55 L. 689/81) 
In caso di applicazione della semilibertà sostitutiva il semilibero è sottoposto ad un programma di 
trattamento predisposto dall’UEPE ed approvato dal giudice. Di conseguenza occorre inserire un nuovo 
contenuto, costituente procedimento “ordinario” e non figlio. 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Programma di trattamento per semilibertà sostitutiva (art. 55 L. 689/81)  
Al nuovo contenuto vanno associati i seguenti oggetti:  
• 
Approvazione programma di trattamento per semilibertà sostitutiva (art. 55 L. 689/81) 
ed i seguenti esiti: 
• 
Approva

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 13/55 
• 
Restituisce programma 
• 
Restituisce programma con osservazioni 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Per quanto riguarda i provvedimenti da emettere per questi procedimenti, saranno implementate due nuove 
funzionalità, emissione decreto Programma di trattamento per semilibertà sostitutiva ed emissione 
ordinanza Programma di trattamento per semilibertà sostitutiva, che conterranno dati relativi, 
rispettivamente, al decreto e all’ordinanza: le nuove maschere di inserimento saranno implementate sulla 
base di quella abbozzata di seguito. 
 
 
 
A seguito della Conferma il sistema inserirà la nuova ordinanza e il nuovo decreto nella base dati e presenterà 
le rispettive form di Dettaglio, dalle quali sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa 
o Upload e Validazione, sia per il decreto che per l’ordinanza 
 
Da decidere se, oltre ai template di ordinanza e decreto generico, occorrono template specifici. 
 
3.3 
Esecuzione Pene Sostitutive  
Dopo che il Magistrato di Sorveglianza ha determinato le modalità di esecuzione della pena sostitutiva invia 
l’ordinanza all’Ufficio di Sorveglianza competente per l’esecuzione della pena sostitutiva. L’Ufficio iscrive un 
fascicolo che farà da collettore per tutti i procedimenti che si apriranno durante l’esecuzione ad essa 
attinenti. Questa tipologia di procedimento, come già fatto per l’esecuzione delle misure alternative, delle 
misure di sicurezza e delle sanzioni sostitutive, sarà identificato comunemente come “Fascicolo padre”,

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 14/55 
mentre tutti i procedimenti relativi ad atti relativi alla fase di esecuzione, che saranno caratterizzati da una 
doppia numerazione il numero identificativo del procedimento e il numero del fascicolo di Esecuzione Pene 
Sostitutive, saranno identificati comunemente come “Fascicoli Figli”. 
 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Esecuzione Pene Sostitutive  
Al nuovo contenuto vanno associati i seguenti oggetti:  
• 
 Semilibertà sostitutiva (art. 55 - 62 L. 689/1981)   
• 
Detenzione domiciliare sostitutiva (art. 56 - 62 L. 689/1981) 
• 
Lavoro di pubblica utilità sostitutivo (art. 56 bis L. 689/1981 – 55 DL 274/20) 
Per questo tipo di procedimento non sono previsti esiti. 
 
Per questo procedimento, come negli altri casi di procedimenti di Esecuzione, il sistema presenterà la 
seguente form 
 
 
 
che in caso di iscrizione da presa in carico dell’ordinanza di applicazione presenterà già precompilati i campi 
Tipo Atto, Data atto, Mittente, Sede Mittente, Anno e Numero Ordinanza. 
La form simile, ma priva di dati precompilati, si presenterà anche in caso di iscrizione da Procedimento SIEP, 
iscrizione da Soggetto e Iscrizione Procedimento Collegato.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 15/55 
 
A seguito della Conferma il sistema inserirà un fascicolo “padre” di esecuzione pene sostitutive e presenterà 
la seguente form di dettaglio dalla quale sarà possibile attivare le azioni di Modifica e Stampa. 
 
 
 
 
 
Da questa form cliccando su Anno e Numero Esecuzione Pena Sostitutiva si riceverà la seguente form: 
 
da cui sarà possibile proseguire con l’inserimento di un nuovo procedimento figlio o con la modifica dei dati 
relativi alla durata ed al luogo di esecuzione della pena sostitutiva. Il completamento di tali dati avviene 
successivamente all’iscrizione del procedimento, quando l’ufficio riceve le ulteriori informazioni 
 
3.4 
Sospensione Esecuzione Pene Sostitutive  
L’art. 660 c.p.p.  al comma 15 prevede di richiedere la sospensione dell’esecuzione della pena sostitutiva nel 
caso che il soggetto chieda l’ammissione al pagamento rateale dopo l’inizio dell’esecuzione, d’altra parte 
l’art. 68 L. 689/81 prevede la Sospensione pena sostitutiva per sopravvenienza misura di sicurezza detentiva 
(art. 68  L.  689/81), la Sospensione pena sostitutiva per sopravvenienza pena detentiva (art.  68 L. 689/81).  
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Sospensione Esecuzione Pene Sostitutive  
Al nuovo contenuto vanno associati i seguenti oggetti:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 16/55 
• 
Sospensione pena sostituiva per ammissione al pagamento rateale (art.660 c.15 c.p.p.) 
• 
 Sospensione pena sostituiva per sopravvenienza misura di sicurezza detentiva (art. 68 L. 
689/1981) 
• 
 Sospensione pena sostituiva per sopravvenienza pena detentiva (art. 68 L. 689/1981) 
ed i seguenti esiti: 
• 
Sospende 
• 
Non sospende 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto, l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS 
 
 
 
A seguito della compilazione della form e successiva Conferma, il sistema presenterà la form di Dettaglio del 
procedimento “figlio” del procedimento di esecuzione pena sostitutiva

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 17/55 
 
Caratterizzata da un proprio Anno e Numero e dal numero del procedimento padre (EPS). 
 
Per i procedimenti di sospensione della sanzione sostitutiva, SIUS permetterà di definire il procedimento con 
un decreto o un’ordinanza. Saranno, quindi, implementate due nuove funzionalità, emissione del decreto 
Sospensione Esecuzione Pene Sostitutive ed emissione dell’ordinanza Sospensione Esecuzione Pene 
Sostitutive, che conterranno dati relativi, rispettivamente, al decreto e all’ordinanza. Le nuove due maschere 
saranno implementate sulla base di quella abbozzata di seguito:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 18/55 
L’ordinanza seguirà il normale percorso di altri provvedimenti, verrà validata, quindi depositata e validata 
per essere trasmesso allo stesso Ufficio o ad altro ufficio. 
L’ordinanza di sospensione viene trasmessa anche alla Procura perché provveda all’annotazione. 
Quanto detto per l’ordinanza vale anche per il decreto. 
 
A seguito della Conferma del decreto e dell’ordinanza, il sistema effettuerà il salvataggio dei dati nella base 
dati e presenterà le rispettive form di Dettaglio, dalle quali sarà possibile attivare le azioni di Modifica, 
Cancellazione, Stampa o Upload e Validazione. 
 
Per questi provvedimenti devono essere previsti i seguenti quattro modelli di stampa che sono 
automaticamente memorizzati in un campo BLOB della base dati: Ordinanza Sospensione per pena detentiva, 
Ordinanza generica, Decreto Sospensione per pena detentiva, Decreto generico.  
 
Per quanto riguarda l’esigenza di rivedere la gestione dei differimenti, come realizzata nell’ambito delle 
esecuzioni delle sanzioni sostitutive, adottando una soluzione più semplificata, simile a quella utilizzata 
nell’ambito dell’esecuzioni delle misure alternativa, si rimanda la scelta della soluzione, in base a quanto 
sarà deciso dai magistrati dei GdL SIEP/SIUS in merito alla competenza sulla gestione dell’esecuzione delle 
Pene Sostitutive (Procure o Uffici di Sorveglianza?). 
3.5 
Autorizzazione Pene Sostitutive  
L’art. 64 e seguenti legge 689/1981 (vedi anche art. 107 L. 689/81) prevede di richiedere delle Autorizzazioni 
nel corso dell’esecuzione della pena sostitutiva. 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Autorizzazione Pene Sostitutive  
Al nuovo contenuto vanno associati i seguenti oggetti: 
• 
Autorizzazione Pene Sostitutive 
• 
Ulteriore autorizzazione Pene Sostitutive 
ed i seguenti esiti: 
• 
Autorizza 
• 
Non autorizza 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione e di 
dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 19/55 
Per la definizione di questi procedimenti sarà implementata una nuova funzionalità, emissione decreto 
autorizzazione su pena sostitutiva: la nuova maschera di inserimento sarà implementata sulla base di quella 
abbozzata di seguito. 
 
 
A seguito della Conferma del decreto, il sistema effettuerà il salvataggio dei dati nella base dati e presenterà 
la form di Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload 
e Validazione. 
 
Per questo provvedimento saranno previsti tre modelli di stampa che, quando generati, sono memorizzati in 
un campo BLOB della base dati: Decreto Autorizzazione generico, Decreto Autorizzazione fuori sede, Decreto 
Autorizzazione Uso Patente. 
3.6 
Modifica Modalità di esecuzione Pene Sostitutive  
L’art. 64 e seguenti legge 689/1981 (vedi anche art. 107 L. 689/81)  prevede di richiedere la Modifica delle 
modalità di esecuzione nel corso dell’esecuzione della pena sostitutiva. 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Modifica modalità di esecuzione/luogo esecuzione pene sostitutive (art. 64 L. 689/81)   
Al nuovo contenuto vanno associati i seguenti oggetti: 
• 
Modifica modalità esecuzione semilibertà sostitutiva (art.  64  L.  689/81) 
• 
Modifica luogo esecuzione semilibertà sostitutiva (art.  64  L.  689/81) 
• 
Modifica modalità esecuzione detenzione   domiciliare sostitutiva (art.  64  L.  689/81) 
• 
Modifica luogo esecuzione detenzione   domiciliare sostitutiva (art.  64  L.  689/81) 
ed i seguenti esiti:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 20/55 
• 
Modifica permanente prescrizioni 
• 
Modifica provvisoria prescrizioni  
• 
Modifica luogo esecuzione 
• 
Rigetta 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
Per la definizione questi procedimenti sarà implementata una nuova funzionalità, emissione del decreto 
Modifica Modalità di esecuzione Pene Sostitutive: la nuova maschera di inserimento sarà implementata sulla 
base di quella abbozzata di seguito. 
 
 
A seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio, 
dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione 
 
Per questo decreto saranno previsti quattro modelli di stampa, che, quando generati, sono memorizzati in 
un campo BLOB della base dati: Decreto Modifica Modalità esecuzione, Decreto Modifica Luogo Esecuzione 
per Affidato, Decreto Modifica Luogo Esecuzione per Detenuto Domiciliare, Decreto Generico.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 21/55 
3.7 
Revoca Autorizzazione/Modifica Prescrizioni Pene Sostitutive  
L’art. 64 e seguenti legge 689/1981 (vedi anche art. 107 L. 689/81) prevede che possa essere richiesta la 
Revoca dell’autorizzazione o della modifica delle prescrizioni, concesse precedentemente, nel corso 
dell’esecuzione della pena sostitutiva. 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Revoca autorizzazione/Modifica Prescrizioni pene sostitutive  
Al nuovo contenuto vanno associati i seguenti oggetti: 
• 
Revoca autorizzazione pene sostitutive 
• 
Revoca Modifica Prescrizioni pene sostitutive 
ed i seguenti esiti: 
• 
Revoca 
• 
Non revoca 
• 
Rigetta 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento saranno identiche a quelle descritte al par. 3.3, tranne per il contenuto e 
oggetto. 
 
Per quanto riguarda i provvedimenti da emettere per questi procedimenti, saranno implementate due nuove 
funzionalità, emissione del decreto Revoca Autorizzazione/Modifica Prescrizioni Pene Sostitutive ed 
emissione dell’ordinanza Revoca Autorizzazione/Modifica Prescrizioni Pene Sostitutive, che conterranno dati 
relativi, rispettivamente, al decreto e all’ordinanza. Le nuove maschere di inserimento saranno implementate 
sulla base di quella abbozzata di seguito.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 22/55 
 
A seguito della Conferma il sistema inserirà la nuova ordinanza e il nuovo decreto nella base dati e presenterà 
le rispettive form di Dettaglio, dalle quali sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa 
o Upload e Validazione, sia per il decreto che per l’ordinanza 
 
Per questi provvedimenti saranno previsti 2 modelli di stampa, che, quando generati, sono memorizzati in 
un campo BLOB della base dati: Decreto Generico e Ordinanza Generica.  
3.8 
Revoca Pene Sostitutive (artt. 66, 108 L. 689/81) 
Gli artt. 66 - 108 legge 689/1981 prevedono un istituto parzialmente nuovo, in quanto in precedenza il 
Magistrato di Sorveglianza si limitava a sospendere l’esecuzione delle sanzioni sostitutive e trasmetteva gli 
atti al TDS (o trasmetteva al TDS senza sospendere), mentre ora è il Magistrato di Sorveglianza a disporre la 
revoca/sostituzione delle pene sostitutive, non più con decreto ma con ordinanza. 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Revoca pena sostitutiva per inosservanza delle prescrizioni (art. 66, 108 L. 689/81 
Al nuovo contenuto vanno associati i seguenti oggetti:  
• 
Revoca detenzione domiciliare sostitutiva per inosservanza prescrizioni (art. 66 L. 689/81) 
• 
Revoca semilibertà sostitutiva per inosservanza prescrizioni (art. 66 L. 689/81) 
• 
Revoca detenzione domiciliare sostitutiva derivante da conversione per inosservanza prescrizioni 
(art. 108 L. 689/81)

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 23/55 
• 
Revoca semilibertà sostitutiva derivante da conversione per inosservanza prescrizioni (art. 108 L. 
689/81)   
ed i seguenti esiti: 
• 
Revoca e converte in pena detentiva 
• 
Revoca e converte in altra pena sostitutiva 
• 
Non Revoca 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione e di 
dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
Per questo tipo di procedimento sarà realizzata una nuova funzionalità, emissione dell’ordinanza Revoca 
Pene Sostitutive; la nuova maschera di inserimento sarà implementata sulla base di quella abbozzata di 
seguito. 
 
 
In cui nella combo box Pena Sostitutiva più grave il sistema presenterà le tre pene sostitutive previste per il 
procedimento di esecuzione (vedi par. 3.2). 
 
A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di 
Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e 
Validazione.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 24/55 
 
Saranno previsti 2 modelli di stampa, chesono memorizzati in un campo BLOB della base dati: Ordinanza 
Generica, Ordinanza revoca pena sostitutiva. 
3.9 
Revoca Pene Sostitutive (art. 72 L. 689/81) 
L’art. 72 legge 689/1981 prevede la revoca della pena sostitutiva a seguito sopravvenienza di nuova 
condanna, in questa evenienza è il Magistrato di Sorveglianza a disporre la revoca/sostituzione delle pene 
sostitutive, con ordinanza. 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Revoca pena sostitutiva per intervenuta condanna (art. 72 L. 689/81) 
Al nuovo contenuto vanno associati i seguenti oggetti:  
• 
Revoca detenzione domiciliare sostitutiva per intervenuta condanna (art. 72 L. 689/81) 
• 
Revoca semilibertà sostitutiva per intervenuta condanna (art. 72 L. 689/81) 
ed i seguenti esiti: 
• 
Revoca e converte in pena detentiva 
• 
Revoca e converte in altra pena sostitutiva 
• 
Non Revoca 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
Per questo tipo di procedimento sarà utilizzata la stessa ordinanza del precedente paragrafo

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 25/55 
 
In cui nella combo box Pena Sostitutiva più grave il sistema presenterà le tre pene sostitutive previste per il 
procedimento di esecuzione (vedi par. 3.2). 
 
A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di 
Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e 
Validazione. 
 
Saranno previsti 2 modelli di stampa, che, quando generati, sono memorizzati in un campo BLOB della base 
dati: Ordinanza Generica, Ordinanza revoca pena sostitutiva. 
3.10 Reclamo avverso Revoca Pena Sostitutiva   (per TDS) 
L’ordinanza di revoca può essere impugnata dinanzi al TDS. Di conseguenza occorre inserire lato TDS un 
nuovo contenuto/oggetto, denominato “Reclamo avverso Revoca Pene Sostitutive” ed i cui esiti potrebbero 
essere: Accoglie reclamo; Accoglie reclamo e converte in altra pena sostitutiva; Rigetta; NLP; Inammissibilità; 
Incompetenza, utilizzando una maschera con alcuni dei dati particolari previsti in quella dell’UDS, vale a dire 
“Pena sostitutiva più grave” e “Rideterminazione quantum pena da espiare” 
 
Nell’ambito dell’Ufficio di Sorveglianza (TDS/TDSM), il contenuto da integrare è il seguente: 
• 
Reclamo avverso Revoca Pena Sostitutiva  
Al nuovo contenuto vanno associati i seguenti oggetti:  
• 
Reclamo avverso Revoca Pena Sostitutiva  
ed i seguenti esiti: 
• 
Accoglie reclamo 
• 
Accoglie reclamo e converte in altra pena sostitutiva Convoca 
• 
Rigetta

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 26/55 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Per la definizione del procedimento sarà realizzata una nuova funzionalità, emissione dell’ordinanza Reclamo 
avverso Revoca Pena Sostitutiva (per TDS): la nuova maschera di inserimento sarà implementata sulla base 
di quella abbozzata di seguito. 
 
 
In cui nella combo box Pena Sostitutiva più grave il sistema presenterà le 3 pene sostitutive previste per il 
procedimento di esecuzione (vedi par. 3.2). 
 
A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di 
Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e 
Validazione. 
 
Saranno previsti 3 modelli di stampa, che, quando generati, sono memorizzati in un campo BLOB della base 
dati: Ordinanza Generica, ordinanza di accoglimento reclamo, ordinanza di rigetto reclamo 
3.11 Diffida al puntuale rispetto delle prescrizioni – pene sostitutive  
Considerato che l’istituto delle pene sostitutive dovrebbe avere una ampia diffusione, è opportuno inserire 
anche un contenuto specifico per la diffida, sulla falsariga di quanto accade nel caso di EMA. 
 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Diffida al puntuale rispetto delle prescrizioni - pene sostitutive 
Al nuovo contenuto vanno associati i seguenti oggetti:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 27/55 
• 
Convocazione per puntuale rispetto prescrizioni – pene sostitutive  
• 
Diffida al puntuale rispetto prescrizioni – pene sostitutive  
ed i seguenti esiti: 
• 
Diffida 
• 
Non Diffida 
• 
Convoca 
• 
Non Convoca 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza 
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
Per la definizione questi procedimenti sarà implementata una nuova funzionalità, emissione del decreto 
Diffida al puntuale rispetto delle prescrizioni – pene sostitutive: la nuova maschera di inserimento sarà 
implementata sulla base di quella abbozzata di seguito. 
 
A seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio, 
dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 28/55 
Per quanto riguarda la stampa, saranno previsti due modelli , che, quando generati, sono memorizzati in un 
campo BLOB della base dati: Decreto generico, Decreto diffida puntuale rispetto prescrizioni.   
3.12 Gestione Licenza - pene sostitutive 
L’art.  69 legge 689/1981, al primo comma, prevede un istituto parzialmente nuovo le licenze per i soggetti 
sottoposti a pene sostitutive. 
 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Licenza - pene sostitutive (art. 69 L. 689/81) 
Al nuovo contenuto vanno associati i seguenti oggetti:  
• 
Licenza - pene sostitutive (art. 69 L. 689/81) 
ed i seguenti esiti: 
• 
Concede 
• 
Rigetta 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
Per questo tipo di procedimento sarà implementata una nuova funzionalità, emissione del decreto Gestione 
Licenza - pene sostitutive: la nuova maschera di inserimento sarà implementata sulla base di quella abbozzata 
di seguito.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 29/55 
 
A seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio, 
dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione 
 
Per questo decreto saranno previsti quattro modelli di stampa , che, quando generati, sono memorizzati in 
un campo BLOB della base dati: Decreto generico, Decreto concessione licenza, Decreto Rigetto licenza, 
Decreto Inammissibilità licenza. 
3.13 Licenza - pene sostitutive - Inosservanza prescrizioni (art. 69 L. 689/81) 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Licenza - pene sostitutive – inosservanza prescrizioni (art. 69 L. 689/81) 
Al nuovo contenuto vanno associati i seguenti oggetti:  
• 
Valutazione revoca licenza – pene sostitutive (Art. 53 bis O.P. – 69 L. 689/81  
• 
Esclusione computo Licenza – pene sostitutive (artt. 53 bis O.P. - 69 L. 689/81) 
ed i seguenti esiti: 
• 
Revoca 
• 
Non Revoca 
• 
Dichiara validamente espiata la pena 
• 
Dichiara non validamente espiata la pena 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 30/55 
• 
Dichiara la propria incompetenza  
 
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
Per questo tipo di procedimento sarà implementata una nuova funzionalità, emissione del decreto per la 
Licenza per internati – inosservanza prescrizioni: la nuova maschera di inserimento sarà implementata sulla 
base di quella abbozzata di seguito. 
 
A seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio, 
dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione 
 
Al momento per questo provvedimento saranno previsti due modelli di stampa , che, quando generati, sono 
memorizzati in un campo BLOB della base dati: Decreto revoca licenza, Decreto scomputo licenza. 
3.14 Sospensione lavoro pubblica utilità sostitutivo  
L’art.  69 legge 689/1981, al secondo comma, prevede l’applicazione di una particolare forma di sospensione 
relativa esclusivamente al lavoro di pubblica utilità. 
 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Sospensione lavoro di pubblica utilità sostitutivo (art. 69 c. 2 L. 689/81) 
Al nuovo contenuto vanno associati i seguenti oggetti:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 31/55 
• 
Sospensione lavoro di pubblica utilità sostitutivo (art. 69 c. 2 L. 689/81) 
ed i seguenti esiti: 
• 
Sospende 
• 
Non sospende 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
 
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
Per questo tipo di procedimento sarà realizzata una nuova funzionalità, emissione del decreto Sospensione 
lavoro pubblica utilità sostitutivo: la nuova maschera di inserimento sarà simile a quella mostrata nel 
paragrafo 3.12 ma con l’aggiunta di alcuni campi come, per esempio, la data e la durata della sospensione.   
 
A seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio, 
dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione. 
 
Saranno previsti due modelli di stampa , che, quando generati, sono memorizzati in un campo BLOB della 
base dati: decreto generico e decreto di sospensione LPU 
3.15 Rinvio dell’esecuzione pena sostitutiva (UDS) 
Anche per le pene sostitutive si applica la disciplina prevista dall’art. 684 c.p.p. e, quindi, quella della 
decisione provvisoria del MdS e del successivo passaggio al TdS. Di conseguenza, si può riprendere, con le 
opportune modifiche, quanto già esistente sial lato UDS che lato TDS con riferimento alle SANZIONI 
SOSTITUTIVE.  
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Rinvio esecuzione Pena Sostitutiva Ex art. 684 comma 2 c.p.p.    U003 
Al nuovo contenuto vanno associati i seguenti oggetti:  
• 
Differimento Pena Sostitutiva facoltativo art. 147 c.p. - art. 69 L. 689/81 
• 
Differimento Pena Sostitutiva obbligatorio art. 146 c.p. - art. 69 L. 689/81

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 32/55 
• 
Applicazione al semilibero della detenzione domiciliare sostitutiva – Art. 69 L. 689/81 
ed i seguenti esiti: 
• 
Concede 
• 
Rigetta 
• 
Rinvia Esecuzione Nelle Forme della Detenzione Domiciliare 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Per questo tipo di procedimento sarà implementata una nuova funzionalità, emissione del decreto Rinvio 
dell’esecuzione pena sostitutiva (UDS): la nuova maschera di inserimento sarà implementata sulla base di 
quella abbozzata di seguito. 
 
A seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio, 
dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione. 
 
Al momento per questo provvedimento sono previsti i seguenti sei modelli di stampa , che, quando generati, 
sono memorizzati in un campo BLOB della base dati: Decreto Incompetenza rinvio provvisorio esecuzione 
pena, Decreto Inammissibilità rinvio provvisorio esecuzione pena, Decreto Generico, Decreto NDP/NLP rinvio 
provvisorio esecuzione pena, Decreto Rigetto rinvio provvisorio esecuzione pena, Decreto concessione rinvio 
provvisorio esecuzione pena. 
3.16 Rinvio dell’esecuzione pena sostitutiva (TDS) 
 
Per l’iscrizione questo tipo di procedimento segue il normale flusso previsto per l’iscrizione di un qualsiasi 
procedimento del Tribunale di Sorveglianza.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 33/55 
Nell’ambito del Tribunale di Sorveglianza (TDS/TDSM), il contenuto da integrare è il seguente: 
• 
Rinvio esecuzione Pena Sostitutiva Ex art. 684 comma 2 c.p.p.    U003 
Al nuovo contenuto vanno associati i seguenti oggetti: 
• 
Differimento Pena Sostitutiva facoltativo art. 147 c.p. - art. 69 L. 689/81 
• 
Differimento facoltativo della Pena Sostitutiva in attesa di grazia – Art. 147 n. 1 c.p. - art. 69 L. 
689/81 
• 
Differimento facoltativo della Pena Sostitutiva per grave infermità – Art. 147 n. 2 c.p. - art. 69 L. 
689/81 
• 
Differimento facoltativo della Pena Sostitutiva per maternità – Art. 147 n. 3 c.p. - art. 69 L. 689/81 
• 
Differimento obbligatorio della Pena Sostitutiva nei confronti di donna incinta – Art. 146 n. 1 c.p. - 
art. 69 L. 689/81 
• 
Differimento obbligatorio della Pena Sostitutiva nei confronti di madre infante di età inferiore ad 
anni 1 – Art. 146 n. 2 c.p. - art. 69 L. 689/81 
• 
Differimento obbligatorio della Pena Sostitutiva nei confronti di persona affetta da malattia – Art. 
146 n. 3 c.p. - art. 69 L. 689/81 
• 
Applicazione al semilibero della detenzione domiciliare sostitutiva – Art. 69 L. 689/81 
ed i seguenti esiti: 
• 
Concede per un periodo 
• 
Rigetta 
• 
Ratifica il provvedimento del mds e concede per un periodo di 
• 
Ratifica il provvedimento del mds e rigetta 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Per questo tipo di procedimento sarà implementata una nuova funzionalità, emissione ordinanza di Rinvio 
Esecuzione Pena Sostitutiva: la nuova maschera di inserimento sarà implementata sulla base di quella 
abbozzata di seguito.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 34/55 
 
A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di 
Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e 
Validazione. 
Al momento per questo provvedimento saranno previsti tre modelli di stampa , che, quando generati, sono 
memorizzati in un campo BLOB della base dati: Ordinanza di Rigetto Generico, Ordinanza di Rigetto 
Differimento della Pena, Ordinanza generica.  
3.17 Rinvio dell’esecuzione  pena sostitutiva derivante da Conversione Pene Pecuniarie  (UDS) 
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Rinvio esecuzione Pena Sostitutiva derivante da Conversione - artt. 69 – 107 L. 689/81”  
Al nuovo contenuto vanno associati i seguenti oggetti:  
• 
Differimento Obbligatorio Pena Sostitutiva derivante da Conversione - artt. 69 – 107 L. 689/81 
• 
Differimento Facoltativo Pena Sostitutiva derivante da Conversione - artt. 69 – 107 L. 689/81 
• 
Applicazione al detenuto sottoposto alla Semilibertà Sostitutiva derivante da Conversione della 
Detenzione Domiciliare Sostitutiva - artt. 69 – 107 L. 689/81).  
ed i seguenti esiti: 
• 
Concede  
• 
Proroga

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 35/55 
• 
Rigetta 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Per la definizione di questo tipo di procedimento sarà realizzata una nuova funzionalità, emissione del 
decreto Rinvio dell’esecuzione pena sostitutiva derivante da Conversione Pene Pecuniarie (UDS): la nuova 
maschera di inserimento sarà simile a quella mostrata nel paragrafo 3.15 ma con l’aggiunta dei campi relativi 
alla pena pecuniaria iniziale 
 
A seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio, 
dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione. 
Al momento per questo provvedimento saranno previsti tre modelli di stampa , che, quando generati, sono 
memorizzati in un campo BLOB della base dati: Decreto di rinvio esecuzione, Decreto generico 
3.18 Rinvio dell’esecuzione pena sostitutiva derivante da Conversione Pene Pecuniarie (TDS) 
Per l’iscrizione questo tipo di procedimento segue il normale flusso previsto per l’iscrizione di un qualsiasi 
procedimento del Tribunale di Sorveglianza. 
Nell’ambito del Tribunale di Sorveglianza (TDS/TDSM), il contenuto da integrare è il seguente: 
• 
Rinvio dell’Esecuzione Pena Sostitutiva derivante da Conversione - artt. 69 – 107 L. 689/81”   
Al nuovo contenuto vanno associati i seguenti oggetti:  
• 
Differimento facoltativo della Pena Sostitutiva derivante da conversione in attesa di grazia – Art. 
147 n. 1 c.p. - artt. 69 – 107 L. 689/81 
• 
Differimento facoltativo della Pena Sostitutiva derivante da conversione per grave infermità – Art. 
147 n. 2 c.p. - artt. 69 – 107 L. 689/81 
• 
Differimento facoltativo della Pena Sostitutiva derivante da conversione per maternità – Art. 147 
n. 3 c.p. - artt. 69 – 107 L. 689/81 
• 
Differimento obbligatorio della Pena Sostitutiva derivante da conversione nei confronti di donna 
incinta – Art. 146 n. 1 c.p. - artt. 69 – 107 L. 689/81 
• 
Differimento obbligatorio della Pena Sostitutiva derivante da conversione nei confronti di madre 
infante di età inferiore ad anni 1 – Art. 146 n. 2 c.p. - artt. 69 – 107 L. 689/81 
• 
Differimento obbligatorio della Pena Sostitutiva derivante da conversione nei confronti di persona 
affetta da malattia – Art. 146 n. 3 c.p. - artt. 69 – 107 L. 689/81

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 36/55 
• 
Applicazione al detenuto sottoposto alla Semilibertà Sostitutiva derivante da Conversione della 
Detenzione Domiciliare Sostitutiva - artt. 69 – 107 L. 689/81). 
ed i seguenti esiti: 
• 
Concede per un periodo  
• 
Proroga per un periodo 
• 
Rigetta 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Per la definizione di questo tipo di procedimento sarà realizzata una nuova funzionalità, emissione 
dell’ordinanza Rinvio dell’esecuzione pena sostitutiva derivante da Conversione Pene Pecuniarie (TDS); la 
nuova maschera di inserimento sarà simile a quella mostrata nel paragrafo 3.16 ma con l’aggiunta dei campi 
relativi alla pena pecuniaria iniziale. 
 
A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di 
Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e 
Validazione. 
 
Al momento per questo provvedimento saranno previsti due modelli di stampa , che, quando generati, sono 
memorizzati in un campo BLOB della base dati: ordinanza di rinvio esecuzione, ordinanza generica 
3.19 Revoca e Conversione pena pecuniaria sostitutiva per mancato pagamento 
 
L’art.  71 legge 689/1981 prevede che la pena pecuniaria sostitutiva non pagata possa essere convertita nella 
semilibertà, nella detenzione domiciliare sostitutiva ovvero nel lavoro di pubblica utilità sostitutivo.  
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Revoca e Conversione pena pecuniaria sostitutiva per mancato pagamento (art.71 L. 689/81) 
Al nuovo contenuto vanno associati i seguenti oggetti:  
• 
Revoca e Conversione pena pecuniaria sostitutiva per mancato pagamento (art.71 L. 689/81) 
ed i seguenti esiti: 
• 
Revoca pena pecuniaria sostitutiva e converte in semilibertà sostitutiva  
• 
Revoca pena pecuniaria sostitutiva e converte in detenzione domiciliare sostitutiva  
• 
Revoca pena pecuniaria sostitutiva e converte in lavoro di pubblica utilità sostitutivo

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 37/55 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Questo tipo di procedimento non presuppone l’esistenza del fascicolo di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione, fuori uscendo dalla logica procedimenti “padre” – “figli”, avverrà utilizzando le attuali 
funzionalità di iscrizione previste in SIUS. 
 
Per questo tipo di procedimento sarà implementata una nuova funzionalità, emissione ordinanza revoca e 
conversione pena pecuniaria sostitutiva: la nuova maschera di inserimento sarà implementata sulla base di 
quella abbozzata di seguito. 
 
In cui Il quantum di pena pecuniaria da convertire non deve essere “precompilato”, ma deve essere presente 
un campo dove inserirlo manualmente, in quanto può non coincidere con la somma iniziale. 
A seguito della Conferma, della validazione e deposito di questa ordinanza, l’ufficio iscriverà un procedimento 
di Esecuzione Pena Sostitutiva (vedi par. 3.2).  
A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di 
Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e 
Validazione. 
Al momento per questo provvedimento saranno previsti due modelli di stampa , che, quando generati, sono 
memorizzati in un campo BLOB della base dati: ordinanza di revoca e conversione, ordinanza generica. 
3.20 Sopravvenienza nuovo Titolo - pene sostitutive 
L’art. 76 legge 689/1981 prevede che la sussistenza dei requisiti dell’applicazione della pena sostitutiva 
vengano rivalutati dal magistrato in presenza di nuovi titoli esecutivi. 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 38/55 
• 
Sopravvenienza nuovo titolo - Pene sostitutive (art. 76 L. 689/81 – 51-bis O.P.) 
Al nuovo contenuto vanno associati i seguenti oggetti: 
• 
Valutazione su permanenza  quantum  pena  per  semilibertà  sostitutiva  (Art.  55  L. 689/81 – 51-
bis O.P.) 
• 
Valutazione su permanenza quantum pena per detenzione domiciliare  sostitutiva  (Art.  56  L. 
689/81 – 51-bis O.P.) 
• 
Valutazione su permanenza quantum pena per lavoro di pubblica utilità (Art.  56 bis L. 689/81 – 
51-bis O.P.) 
ed i seguenti esiti: 
• 
Estende la pena sostitutiva 
 
• 
Dischiara inefficace/cessata la pena sostitutiva 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Pena Sostitutiva, e richiederà 
di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e di dettaglio 
del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
In realtà, si tratta di un fascicolo figlio “derivato”, vale a dire non iscritto con le modalità utilizzate per gli altri 
fascicoli figli, ma partendo da una iscrizione ordinaria (vedi “sopravvenienza nuovo titolo” in caso di misura 
alternativa). 
Per quanto riguarda i provvedimenti da emettere per questi procedimenti, saranno implementate due nuove 
funzionalità, emissione del decreto Sopravvenienza nuovo Titolo - pene sostitutive ed emissione 
dell’ordinanza Sopravvenienza nuovo Titolo - pene sostitutive, che conterranno dati relativi, rispettivamente, 
al decreto e all’ordinanza. Le nuove due maschere di inserimento saranno implementate sulla base di quella 
abbozzata di seguito:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 39/55 
 
A seguito della Conferma il sistema inserirà la nuova ordinanza e il nuovo decreto nella base dati e presenterà 
le rispettive form di Dettaglio, dalle quali sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa 
o Upload e Validazione, sia per il decreto che per l’ordinanza. 
 
Al momento per questo provvedimento saranno previsti sei modelli di stampa , che, quando generati, sono 
memorizzati in un campo BLOB della base dati: ordinanza di estensione della pena, ordinanza di cessazione 
della pena, ordinanza generica, decreto di estensione della pena, decreto di cessazione della pena, decreto 
generica 
3.21 Sospensione esecuzione pene accessorie (UDS) 
L’art.  51 quater O.P. (disciplina delle pene accessorie in caso di concessione di misure alternative) prevede  
che l’Ufficio di Sorveglianza possa decidere la sospensione dell’esecuzione delle pene accessorie  in caso di 
misure alternative o di pene sostitutive. 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Sospensione esecuzione pene accessorie (art. 51-quater O.P.) 
Al nuovo contenuto vanno associati i seguenti oggetti:  
• 
Sospensione esecuzione pene accessorie – Misure alternative (art. 51-quater O.P.) 
• 
Sospensione esecuzione pene accessorie – Pene sostitutive (Art.  76 L. 689/81 – 51-quater O.P.) 
ed i seguenti esiti: 
• 
Sospende 
• 
Non sospende 
• 
Dichiara N.D.P./ N.L.P 
• 
Dichiara inammissibilità 
• 
Dichiara la propria incompetenza

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 40/55 
 
Questo tipo di procedimento non presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena 
Sostitutiva/Esecuzione Misura Alternativa, pertanto l’iscrizione, fuoriuscendo dalla logica procedimenti 
“padre” – “figli”, avverrà utilizzando le attuali funzionalità di iscrizione previste in SIUS.  
 
Per questo tipo di procedimento sarà implementata una nuova funzionalità, emissione ordinanza 
sospensione esecuzione pena accessoria: la nuova maschera di inserimento sarà implementata sulla base di 
quella abbozzata di seguito. 
 
In cui nella combo box Tipo saranno presenti tutti i tipi di pena accessoria di cui all’art. 19 c.p., e quindi: 
1) interdizione dai pubblici uffici; 
2) interdizione da una professione o da un'arte; 
3) interdizione legale; 
4) incapacità di contrattare con la pubblica amministrazione; 
4-bis) estinzione del rapporto di impiego o di lavoro; 
5) decadenza o la sospensione dall'esercizio della responsabilità genitoriale; 
6) sospensione dall'esercizio di una professione o di un'arte; 
7) pubblicazione della sentenza penale di condanna

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 41/55 
Per quel che concerne la durata della pena accessoria irrogata sarà presente la combo Tipo Durata in cui sarà 
possibile selezionare tra Perpetua e Durante la pena (per la quale bisognerà indicare la durata nei successivi 
campi). 
A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di 
Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e 
Validazione. 
 
Al momento per questo provvedimento saranno previsti due modelli di stampa , che, quando generati, sono 
memorizzati in un campo BLOB della base dati: ordinanza di sospensione della pena accessoria, ordinanza 
generica 
 
3.22 Sospensione esecuzione pene accessorie (TDS) 
L’art.  51 quater O.P. (disciplina delle pene accessorie in caso di concessione di misure alternative) prevede 
la sospensione dell’esecuzione delle pene accessorie  in caso di misure alternative possa essere decisa anche 
dal Tribunale di Sorveglianza. 
Nell’ambito dell’Ufficio di Sorveglianza (TDS/TDSM), il contenuto da integrare è il seguente: 
• 
Sospensione esecuzione pene accessorie (art. 51-quater O.P.) 
Al nuovo contenuto vanno associati i seguenti oggetti:  
• 
Sospensione esecuzione pene accessorie – Misure alternative (art. 51-quater O.P.) 
ed i seguenti esiti: 
• 
Sospende 
• 
Non sospende 
• 
Dichiara N.D.P./ N.L.P 
• 
Dichiara inammissibilità 
• 
Dichiara la propria incompetenza 
 
Questo tipo di procedimento non presuppone l’esistenza del fascicolo “padre” di Esecuzione Misura 
Alternativa, pertanto l’iscrizione, fuoriuscendo dalla logica procedimenti “padre” – “figli”, avverrà utilizzando 
le attuali funzionalità di iscrizione previste in SIUS.  
 
Per questo tipo di procedimento si può ipotizzare la stessa ordinanza descritta al prec. Paragrafo.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 42/55 
 
A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di 
Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e 
Validazione. 
Al momento per questo provvedimento saranno previsti due modelli di stampa , che, quando generati, sono 
memorizzati in un campo BLOB della base dati: ordinanza di sospensione della pena accessoria, ordinanza 
generica 
3.23 Conversione Pene Pecuniarie Principali per mancato pagamento 
Gli artt. 102, 103 legge 689/1981 e art. 55 d. lgs. 274/00 prevedono che la pena pecuniaria non pagata possa 
essere convertita non 
più nella libertà controllata, bensì nella semilibertà e nella detenzione domiciliare sostitutive, oltre che nel 
lavoro di pubblica utilità. 
 
Non conviene inserire i nuovi oggetti nell’attuale contenuto Conversione Pena Pecuniaria, in quanto per 
questi procedimenti è obbligatorio l’inserimento della Richiesta Conversione Pena Pecuniaria, con 
l’indicazione di tutti gli estremi (Anno/Numero Partiva IVA, Campione Penale, Autorità Richiedente, data 
irrevocabilità Titolo Esecutivo, etc.). Questi dati non sono necessari per la gestione dei procedimenti con Pena 
Pecuniaria sostitutiva in quanto la Procura si limiterà a trasferire l’importo di Pena Pecuniaria non pagato. 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Conversione pene pecuniarie principali per mancato pagamento (artt. 102 - 103 L. 689/81 - 55 d. 
lgs. 274/00) 
Al nuovo contenuto vanno associati i seguenti oggetti:  
• 
Conversione pene pecuniarie principali per mancato pagamento (artt. 102 - 103 L. 689/81) 
• 
Conversione pene pecuniarie principali per mancato pagamento (art. 55 d. lgs. 274/00) 
ed i seguenti esiti:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 43/55 
• 
Dispone conversione in semilibertà sostitutiva 
• 
Dispone conversione in detenzione domiciliare sostitutiva 
• 
Dispone conversione in lavoro di pubblica utilità sostitutivo  
• 
Dispone conversione pena irrogata dal GdP in lavoro di pubblica utilità  
• 
Differisce la conversione 
• 
Dichiara NLP per irreperibilità – atti al PM 
• 
Dichiara NLP per accertata solvibilità 
• 
Dichiara NLP per intervenuta prescrizione 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza 
• 
Rateizza pagamento   
 
Questo tipo di procedimento non presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione, fuoriuscendo dalla logica procedimenti “padre” – “figli”, avverrà utilizzando le attuali 
funzionalità di iscrizione previste in SIUS.  
 
Per questo tipo di procedimento sarà implementata una nuova funzionalità, emissione ordinanza 
conversione pene pecuniarie sostitutive: la nuova maschera di inserimento, che non richiederà la presenza 
dei dati della Conversione, sarà implementata sulla base di quella abbozzata di seguito. 
 
La nuova maschera si differenzierà in base all’esito del provvedimento, in caso di rateizzazione

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 44/55 
 
In caso di Conversione 
 
A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di 
Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e 
Validazione. 
Al momento per questo provvedimento saranno previsti tre modelli di stampa , che, quando generati, sono 
memorizzati in un campo BLOB della base dati: ordinanza di conversione pena pecuniaria, ordinanza di 
rateizzazione della pena pecuniaria, ordinanza generica

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 45/55 
 
3.24 Conversione pene pecuniarie irrogate dal Giudice di Pace  
L’art.  55 D.L. 274/2000 prevede che a richiesta del condannato la pena pecuniaria può essere convertita in 
lavoro di pubblica utilità, In caso di violazione degli obblighi del lavoro di pubblica utilità, la parte           residua 
si converte in obbligo di permanenza domiciliare.  
 
Premessa alla gestione di questo nuovo contenuto è l’inserimento fra gli oggetti del fascicolo padre di ESS di 
un nuovo oggetto: 
• 
Lavoro di pubblica utilità 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Violazione obblighi lavoro pubblica utilità (art. 55 c. 3 DL 274/2000)   
Al nuovo contenuto vanno associati il seguente oggetto:  
• 
Violazione obblighi lavoro pubblica utilità (art. 55 c. 3 DL 274/2000) 
ed i seguenti esiti: 
• 
Converte pena pecuniaria in permanenza domiciliare  
• 
Non converte 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà uguale a quella di tutti gli altri procedimenti figli dell’Esecuzione Pena Sostitutiva. 
 
Per questo tipo di procedimento sarà utilizzata la stessa ordinanza del precedente paragrafo. 
La conversione di cui sopra determina come effetto diretto quello di imporre la creazione di un nuovo oggetto 
all’interno del contenuto ESS, che potremmo denominare 
• 
Permanenza domiciliare 
A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di 
Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e 
Validazione. 
Al momento per questo provvedimento saranno previsti tre modelli di stampa , che, quando generati, sono 
memorizzati in un campo BLOB della base dati: ordinanza di sospensione della pena accessoria, ordinanza 
generica.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 46/55 
3.25 Rateizzazione Pena Pecuniaria 
Considerato che (a quanto pare) la rateizzazione potrà essere concessa dal Magistrato di Sorveglianza solo in 
corso di esecuzione (o, quanto meno, prima dell’inizio ma sempre successivamente all’emissione del 
provvedimento di conversione), quindi dopo l’iscrizione di un procedimento di EPS. 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Rateizzazione pena pecuniaria 
Al nuovo contenuto vanno associati il seguente oggetto:  
• 
Rateizzazione pena pecuniaria 
ed i seguenti esiti: 
• 
Rateizza pagamento 
• 
Rigetta 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà uguale a quella di tutti gli altri procedimenti figli dell’Esecuzione Pena Sostitutiva. 
 
Per questo tipo di procedimento sarà utilizzata la stessa ordinanza del paragrafo 3.23, prevista in caso di 
rateizzazione della pena pecuniaria.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 47/55 
 
A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di 
Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e 
Validazione. 
Al momento per questo provvedimento saranno previsti due modelli di stampa , che, quando generati, sono 
memorizzati in un campo BLOB della base dati: ordinanza di rateizzazione, ordinanza generica. 
 
 
3.26 Revoca pena sostitutiva conseguente alla conversione p.p. per avvenuto pagamento 
Stante quanto prescritto dal comma 15 dell’art. 660 c.p.p., bisogna gestire un nuovo procedimento “figlio” 
nell’ambito dell’EPS, che potremmo denominare, sia nel contenuto che nell’oggetto, “Revoca pena 
sostitutiva conseguente alla conversione pena pecuniaria per avvenuto pagamento”. Gli esiti potrebbero 
essere “Revoca pena sostitutiva”; “Non revoca pena sostitutiva”; “Dichiara NDP/NLP”; Dichiara 
inammissibilità”; “Dichiara incompetenza”. 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
• 
Revoca pena sostitutiva conseguente alla conversione pena pecuniaria per avvenuto pagamento 
(art. 660 co. 15 c.p.p.) 
Al nuovo contenuto va associato il seguente oggetto:  
• 
Revoca pena sostitutiva conseguente alla conversione pena pecuniaria per avvenuto pagamento 
(art. 660 co. 15 c.p.p.) 
ed i seguenti esiti: 
• 
Revoca pena sostitutiva

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 48/55 
• 
Non Revoca pena sostitutiva 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà uguale a quella di tutti gli altri procedimenti figli dell’Esecuzione Pena Sostitutiva. 
 
Per questo tipo di procedimento sarà realizzata una nuova ordinanza, il cui contenuto sarà indicato 
dall’Amministrazione. 
A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di 
Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e 
Validazione. 
Al momento per questo provvedimento sarà previsto un modello di stampa , che, quando generati, sono 
memorizzati in un campo BLOB della base dati: ordinanza generica. 
 
3.27 Gestione Procedimenti Esecuzione Pene Sostitutive 
Come già previsto in SIUS per i procedimenti di Esecuzione Misure Alternative, Esecuzione Sanzioni 
Sostitutive e Esecuzione Misure di Sicurezza, per la gestione dei procedimenti di Esecuzione Pene Sostitutive 
sarà aggiunta nel menu verticale dell’UDS la nuova voce

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 49/55 
 
Che presenterà a sua volta il menu orizzontale: 
 
 
 
Da cui sarà possibile accedere alle seguenti due nuove funzionalità: 
- 
ricercare i procedimenti “padri” di Esecuzione Pene Sostitutive per Anno e Numero o per Intervalli 
di numeri

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 50/55 
 
- 
ricercare i procedimenti “padri” di Esecuzione Pene Sostitutive a carico di un Soggetto: 
 
 
Le due funzionalità seguiranno lo stesso flusso operativo presente in SIUS per gli altri procedimenti di 
Esecuzione. 
3.28 Gestione Licenze – Pene Sostitutive 
Per estendere l’attuale gestione delle Licenze per semilibertà e per internati anche alle Licenze – pene 
sostitutive saranno adeguate tutte le funzionalità, riferite a Licenza, presenti nella voce di menu verticale 
, cioè 
 
- 
Ricerca Licenze per Soggetto 
Nell’attuale form:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 51/55 
 
 
Nella combo box Visualizza solo i provvedimenti relativi a, alle attuali voci “Licenze” e “Licenze per Internati” 
sarà aggiunta la nuova voce “Licenze – pene sostitutive”. Tutto il codice sarà aggiornato per gestire le nuove 
tipologie di Licenza. 
- 
Esecuzione Licenza 
Le attuali funzioni attivabili dalla sottostante form: 
 
 
saranno aggiornate per poter  essere utilizzate anche per le Licenze – pene sostitutive. 
- 
Relazione Trimestrale 
L’attuale form sarà modificata:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 52/55 
 
 
Con l’aggiunta di un nuovo radio button per poter utilizzare la funzione anche per la nuova Licenza con 
conseguente aggiornamento del codice. Il risultato della ricerca calcolerà e mostrerà a video il totale delle 
occorrenze ottenute in base ai criteri di ricerca inseriti

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 53/55 
4 Piano delle attività 
4.1 
Ciclo di sviluppo 
Il ciclo di sviluppo è il classico (waterfall).

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 54/55 
5 Piano delle attività 
Si prevede di terminare le attività il 28_06 qualora la scheda in oggetto sia approvata entro il 26_03 . 
 
5.1 
Gantt 
 
 
5.2 
Vincoli 
 
5.3 
Luogo di lavoro 
Le attività saranno espletate presso le sedi del RTI.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.1-20240223_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia 
Ver. 1.2 del 23/02/2024 
Pag. 55/55 
6 Dimensionamento 
 
6.1 
Stima dell’effort 
6.2 
Attività misurabili in punti funzione 
 
N° 
€ 
Totale 
ADD 
1027 
162 
166.374,00 € 
CHG 
19 
81 
1.539,00 € 
DEL 
0 
16,2  
   0,00 € 
167.913,00 € 
 
Per il dettaglio dell’impegno, misurabile in punti funzione, distinto per la singola funzionalità e/o file 
logici si rimanda al foglio di calcolo dei punti funzione in allegato alla presente Scheda. 
 
 
6.3 
Dettaglio dei costi 
L’importo complessivo dell’obiettivo è di € 167.913,00. 
 
I prezzi sono IVA esclusa. 
 
Sono esclusi dal presente piano le tempistiche ed i costi relativi all’eventuale 
consolidamento/revisione dei requisiti intervenuti successivamente all’emissione del presente 
documento e che potranno essere oggetto di una successiva emissione del presente piano con 
aggiornamento dei tempi e dei costi relativi sia alla fase di analisi, sia a quella di sviluppo.