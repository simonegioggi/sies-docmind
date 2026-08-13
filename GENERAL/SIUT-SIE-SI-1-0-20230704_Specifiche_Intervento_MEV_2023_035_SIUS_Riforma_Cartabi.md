---
uniqueName: siut-sie-si-1-0-20230704specificheinterventomev202
displayName: "SIUT SIE SI 1 0 20230704 Specifiche Intervento MEV 2023 035 SIUS Riforma Cartabi"
category: "GENERAL"
tags: []
---

# SIUT-SIE-SI-1.0-20230704_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia

> **File originale:** `MEV/SCHEDA_035/SIUT-SIE-SI-1.0-20230704_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
Specifiche Intervento MEV 2023_035_SIUS-
Integrazione Riforma Cartabia 
 
 
 
 
 
 
 
 
Versione 1.0 del 04/07/2023

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 2/38 
 
 
 
 
 
 
 
 
Il presente documento è stato redatto con la collaborazione 
del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA 
S.r.l. nell’ambito del contratto CIG 73479643B7 per lo 
“Sviluppo del Sistema Informativo Unitario Telematico, la 
manutenzione degli attuali sistemi dell’area Penale del 
Ministero della Giustizia e servizi correlati. Lotto 1”.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 3/38 
 
 
 
Approvazioni 
Nominativo
Elaborato da
Umberto Mignogna
Verificato da
Vito Bufi
Approvato da
Paolo Ceccanti
Data approvazione
04/07/2023
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
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 4/38 
 
 
INDICE DEI CONTENUTI 
  
1 
INTRODUZIONE ............................................................................................................................... 6 
1.1 
SCOPO DEL DOCUMENTO .......................................................................................................................... 6 
1.2 
RIFERIMENTI ........................................................................................................................................... 6 
1.3 
GLOSSARIO ............................................................................................................................................. 7 
1.3.1 
DEFINIZIONI ........................................................................................................................................ 7 
1.3.2 
ACRONIMI E ABBREVIAZIONI .................................................................................................................. 7 
2 
ARCHITETTURA DEL SISTEMA ........................................................................................................... 9 
2.1 
ARCHITETTURA ........................................................................................................................................ 9 
2.2 
WEB SERVICES ........................................................................................................................................ 9 
2.3 
XSD ...................................................................................................................................................... 9 
2.4 
CONFIGURAZIONE .................................................................................................................................... 9 
2.5 
TUTORIAL ............................................................................................................................................... 9 
3 
DESCRIZIONE DELL’INTERVENTO .................................................................................................... 10 
3.1 
APPLICAZIONE PENE SOSTITUTIVE (ART. 62 L. 689/81) ............................................................................... 10 
3.2 
ESECUZIONE PENE SOSTITUTIVE ............................................................................................................... 11 
3.3 
SOSPENSIONE ESECUZIONE PENE SOSTITUTIVE ........................................................................................... 13 
3.4 
AUTORIZZAZIONE PENE SOSTITUTIVE ........................................................................................................ 16 
3.5 
MODIFICA MODALITÀ DI ESECUZIONE PENE SOSTITUTIVE ............................................................................. 17 
3.6 
REVOCA AUTORIZZAZIONE PENE SOSTITUTIVE ............................................................................................ 18 
3.7 
REVOCA AUTORIZZAZIONE PENE SOSTITUTIVE ............................................................................................ 20 
3.7.1 
Sospensione Provvisoria Pena Sostitutiva per inosservanza prescrizioni .................................................. 21 
3.8 
DIFFIDA AL PUNTUALE RISPETTO DELLE PRESCRIZIONI – PENE SOSTITUTIVE ....................................................... 22 
3.9 
GESTIONE LICENZA - PENE SOSTITUTIVE ..................................................................................................... 23 
3.10 
LICENZA - PENE SOSTITUTIVE - INOSSERVANZA PRESCRIZIONI (ART. 69 L. 689/81) ....................................... 25 
3.11 
SOSPENSIONE LAVORO PUBBLICA UTILITÀ SOSTITUTIVO ............................................................................. 26 
3.12 
RINVIO DELL’ESECUZIONE  PENA SOSTITUTIVA ......................................................................................... 27 
3.13 
REVOCA E CONVERSIONE PENA PECUNIARIA SOSTITUTIVA ......................................................................... 28 
3.14 
SOPRAVVENIENZA NUOVO TITOLO - PENE SOSTITUTIVE ............................................................................. 30 
3.15 
SOSPENSIONE ESECUZIONE PENE ACCESSORIE .......................................................................................... 31 
3.16 
CONVERSIONE/RATEIZZAZIONE PENA PECUNIARIA SOSTITUTIVA ................................................................ 32 
3.17 
CONVERSIONE PENE PECUNIARIE IRROGATE DAL GIUDICE DI PACE .............................................................. 34 
3.18 
GESTIONE PROCEDIMENTI ESECUZIONE PENE SOSTITUTIVE ....................................................................... 34 
3.19 
GESTIONE LICENZE – PENE SOSTITUTIVE ................................................................................................ 36

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 5/38

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 6/38 
 
 
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
normative della cd Riforma Cartabia(maggiorenni e minorenni). 
Con lo scopo di rendere l’intervento coerente ed auto consistente gli interventi dovranno tener conto 
dell’integrazione con gli altri sottosistemi (SIEP e SIGE). 
 
1.2 
Riferimenti 
Riferimen
to 
Nome Documento
Descrizione Documento
RIF1
m_dg.DOG07AR.04_05_2023.0000747.U_Richiesta_sc
heda_2023-35_SIES_Cartabia_con_SIUS_signed 
Richiesta Scheda di Intervento
RIF2
RIF3
RIF4
RIF5
RIF6

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 7/38 
 
 
1.3 
Glossario 
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 8/38 
 
 
Sigla
Descrizione
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
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 9/38 
 
 
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
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 10/38
 
 
3 Descrizione dell’Intervento 
Di seguito si riportano gli interventi necessari nel sottosistema SIUS per adeguarlo alle modifiche apportate 
dalla cd “Riforma Cartabia” ai singoli articoli del c.p.p. 
Per ciascun provvedimento riportato nei paragrafi successivi dalla form di Dettaglio sarà possibile attivare le 
funzioni di stampa, validazione, modifica e cancellazione. 
3.1 
Applicazione Pene Sostitutive (art. 62 L. 689/81) 
In relazione all’art. 62 L. 689/81 la riforma non parla più di Sanzioni sostitutive ma di Pene Sostitutive nelle 
forme di Semilibertà sostitutiva e Detenzione Domiciliare sostitutiva, che possono essere applicate dal 
giudice in caso di condanna alla reclusione o all’arresto non superiori a quatto anni. Gli Uffici di Sorveglianza 
(UDS/UDSM) sono pertanto chiamati a pronunciarsi sull’applicabilità di tali pene sostitutive. A tal fine 
bisognerà prevedere la gestione di un nuovo procedimento con contenuto di “Applicazione Pene 
Sostitutive”. 
 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Applicazione Pene Sostitutive  
Al nuovo contenuto vanno associati i seguente oggetti:  
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
Dichiara la propria incompetenza – dispone restituzione atti al PM  
• 
Dichiara la propria incompetenza – dispone trasmissione atti al MdS  
Att.ne: gli esiti evidenziati in giallo sono quelli validi per l’applicazione delle sanzioni sostitutive, da 
confermare, o sostituire semplicemente con Dichiara la propria incompetenza. 
L’aggiunta dei suddetti elementi permetterà all’Ufficio di poter iscrivere procedimenti di Applicazione Pene 
Sostitutive, collegandosi direttamente al procedimento SIEP o a seguito di presa in carico di Richiesta 
Applicazione Pene Sostitutive trasmesse dalle Procure. 
Per la successiva definizione bisognerà realizzare l’ordinanza di applicazione delle pene sostitutive, che 
potrebbe riproporre gli stessi campi previsti per l’Applicazione delle sanzioni sostitutive

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 11/38
 
 
 
A seguito della Conferma inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio, dalla 
quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload, Validazione. 
L’ordinanza seguirà il normale percorso di altri provvedimenti, verrà quindi depositato e validato per essere 
trasmesso allo stesso Ufficio o ad altro ufficio, che procederà alla presa in carico e all’iscrizione di un 
procedimento di esecuzione della pena sostitutiva (cd Fascicolo padre) al quale faranno riferimento tutti i 
procedimenti afferenti alla gestione dell’esecuzione. 
L’ordinanza di applicazione viene trasmessa anche alla Procura perché provveda all’annotazione. 
 
3.2 
Esecuzione Pene Sostitutive  
Dopo che il Magistrato di Sorveglianza ha determinato le modalità di esecuzione della pena sostitutiva invia 
l’ordinanza all’Ufficio di Sorveglianza competente per l’esecuzione della pena sostitutiva. L’Ufficio iscrive un 
fascicolo che farà da collettore per tutti i procedimenti che si apriranno durante l’esecuzione ad essa 
attinenti. Questa tipologia di procedimento, come già fatto per l’esecuzione delle misure alternative, delle 
misure di sicurezza e delle sanzioni sostitutive, sarà identificato comunemente come “Fascicolo padre”, 
mentre tutti i procedimenti relativi ad atti relativi alla fase di esecuzione, che saranno caratterizzati da una 
doppia numerazione il numero identificativo del procedimento e il numero del fascicolo di Esecuzione Pene 
Sostitutive, saranno identificati comunemente come “Fascicoli Figli”. 
 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Esecuzione Pene Sostitutive  
Al nuovo contenuto vanno associati i seguente oggetti:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 12/38
 
 
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
 
A seguito della Conferma il sistema inserirà un fascicolo “padre” di esecuzione pene sostitutive e presenterà 
la seguente form

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 13/38
 
 
 
 
Da questa form cliccando su Anno e Numero Esecuzione Pena Sostitutiva si riceverà la seguente form 
 
 
da cui sarà possibile Iscrivere un procedimento “figlio” o modificare i dati relativi alla durata ed al luogo di 
esecuzione della pena sostitutiva. 
 
 
3.3 
Sospensione Esecuzione Pene Sostitutive  
L’art. 660 c.p.p.  al comma 15 prevede di richiedere la sospensione dell’esecuzione della pena sostitutiva nel 
caso che il soggetto chieda  l’ammissione  al  pagamento  rateale  dopo l’inizio dell’esecuzione, d’altra parte 
l’art. 68 L. 689/81 prevede la Sospensione pena sostitutiva per sopravvenienza misura di sicurezza detentiva 
(art. 68  L.  689/81), la Sospensione  pena  sostitutiva  per  sopravvenienza  pena  detentiva  (art.  68 L.  
689/81).  
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Sospensione Esecuzione Pene Sostitutive  
Al nuovo contenuto vanno associati i seguente oggetti:  
• 
Sospensione pena sostituiva per ammissione al pagamento rateale (art.660 c.15 c.p.p.) 
• 
 Sospensione pena sostituiva per sopravvenienza misura di sicurezza detentiva (art. 68 L. 689/1981)

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 14/38
 
 
• 
 Sospensione pena sostituiva per sopravvenienza pena detentiva (art. 68 L. 689/1981) 
e i seguenti esiti 
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
pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS 
 
 
 
A seguito della compilazione della form e successiva Conferma, il sistema presenterà la form di Dettaglio del 
procedimento “figlio” del procedimento di esecuzione pena sostitutiva

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 15/38
 
 
 
Caratterizzata da un proprio Anno e Numero e dal numero del procedimento padre (EPS). 
Per i procedimenti di sospensione della sanzione sostitutiva SIUS permette di definire il procedimento con 
un decreto o una ordinanza, che riportano il seguente contenuto

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 16/38
 
 
Puo essere adottata la suddetta form anche per la sospensione della pena sostitutiva? 
Deve essere prevista la possibilità di esprimersi con ordinanza e decreto? 
Al momento per questi provvedimenti sono previsti 6 modelli di stampa: Ordinanza Sospensione per pena 
detentiva, Ordinanza Sospensione per violazione prescrizione, Ordinanza generica, Decreto Sospensione per 
pena detentiva,Decreto Sospensione per violazione prescrizione, Decreto generica. 
 
3.4 
Autorizzazione Pene Sostitutive  
L’art. 64 e seguenti legge 689/1981 (vedi anche art. 107 L. 689/81)  prevede di richiedere delle Autorizzazioni 
nel corso dell’esecuzione della pena sostitutiva. 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Autorizzazione Pene Sostitutive  
Al nuovo contenuto vanno associati i seguente oggetti:  
• 
Autorizzazione 
• 
Ulteriore autorizzazione 
e i seguenti esiti 
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
pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
 
Per i procedimenti di autorizzazione della sanzione sostitutiva SIUS permette di definire il procedimento solo 
con un decreto, che riporta il seguente contenuto

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 17/38
 
 
 
 
Puo essere adottata la suddetta form anche per l’autorizzazione della pena sostitutiva? 
Deve essere prevista la possibilità di esprimersi anche con ordinanza? 
Al momento per questo provvedimento sono previsti 3 modelli di stampa: Decreto Autorizzazione generico, 
Decreto Autorizzazione fuori sede, Decreto Autorizzazione Uso Patente. 
 
3.5 
Modifica Modalità di esecuzione Pene Sostitutive  
L’art. 64 e seguenti legge 689/1981 (vedi anche art. 107 L. 689/81)  prevede di richiedere la Modifica delle 
modalità di esecuzione nel corso dell’esecuzione della pena sostitutiva. 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Modifica modalità di esecuzione pene sostitutive (art. 64 L. 689/81)   
Al nuovo contenuto vanno associati i seguente oggetti:  
• 
Modifica prescrizioni semilibertà  sostitutiva  (art.  64  L.  689/81) 
• 
Modifica prescrizioni detenzione   domiciliare sostitutiva  (art.  64  L.  689/81) 
e i seguenti esiti 
• 
Modifica permanente prescrizioni 
• 
Modifica provvisoria prescrizioni  
• 
Rigetta 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 18/38
 
 
• 
Dichiara la propria incompetenza  
 
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
 
Per i procedimenti di autorizzazione della sanzione sostitutiva SIUS permette di definire il procedimento con 
decreto o con ordinanza, che riporta il seguente contenuto 
 
 
Puo essere adottata la suddetta form anche per la modifica modalità di esecuzione della pena sostitutiva? 
Deve essere prevista la possibilità di esprimersi anche con ordinanza e decreto? 
Al momento per questi provvedimenti sono previsti 4 modelli di stampa: Ordinanza Modifica Permanente 
Prescrizioni, Ordinanza Generica, Decreto Modifica Permanente Prescrizioni, Decreto Generico. 
 
3.6 
Revoca Autorizzazione Pene Sostitutive  
L’art. 64 e seguenti legge 689/1981 (vedi anche art. 107 L. 689/81)  prevede che possa essere richiesta la 
Revoca dell’autorizzazione, concessa precedentemente, nel corso dell’esecuzione della pena sostitutiva. 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Revoca autorizzazione pene sostitutive  
Al nuovo contenuto vanno associati i seguente oggetti:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 19/38
 
 
• 
Revoca autorizzazione pene sostitutive  
e i seguenti esiti 
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
pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
 
Per i procedimenti di Revoca autorizzazione della sanzione sostitutiva SIUS permette di definire il 
procedimento solo con decreto, che riporta il seguente contenuto 
 
 
Puo essere adottata la suddetta form anche per la Revoca Autorizzazione della pena sostitutiva? 
Deve essere prevista la possibilità di esprimersi anche con ordinanza? 
Al momento per questo provvedimento è previsto un solo modello di stampa: Decreto Generico.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 20/38
 
 
 
3.7 
Revoca Autorizzazione Pene Sostitutive  
Gli artt. 66 – 72 – 108  legge 689/1981  prevedono un istituto parzialmente nuovo, in quanto in precedenza 
il MS si limitava a sospendere l’esecuzione delle sanzioni sostitutive e trasmetteva gli atti al TDS (o  
trasmetteva al TDS senza sospendere), mentre ora è il Magistrato di Sorveglianza a disporre la 
revoca/sostituzione delle pene sostitutive, non più con decreto ma con ordinanza. 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Revoca pena sostitutiva per inosservanza delle prescrizioni art. 66 – 72 – 108 L. 689/81 
Al nuovo contenuto vanno associati i seguente oggetti:  
• 
Revoca pena sostitutiva per inosservanza prescrizioni (art. 66 - 72 L. 689/81) 
• 
Revoca pena sostitutiva per inosservanza prescrizioni (art. 108 L. 689/81)   
e i seguenti esiti 
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
pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
 
Per quetso tipo di procedimento si può ipotizzare un ordinanza del tipo seguente

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 21/38
 
 
 
In cui nella combo box Pena Sostitutiva più grave il sistema presenterà le 3 pene sostitutive previste per il 
procedimento di esecuzione (vedi par. 3.2). 
Da decidere i modelli di stampa da associare. 
 
3.7.1 
Sospensione Provvisoria Pena Sostitutiva per inosservanza prescrizioni 
Considerato, poi, che la revoca deve essere disposta previa fissazione di una udienza, il Magistrato dovrà 
avere la possibilità di sospendere provvisoriamente la pena sostitutiva , al fine di evitare che la stessa 
prosegua nel periodo intercorrente tra la segnalazione e l’udienza.  
 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Sospensione pena sostitutiva per inosservanza prescrizioni   
Al nuovo contenuto vanno associati i seguente oggetti:  
• 
Sospensione pena sostitutiva per inosservanza prescrizioni 
e i seguenti esiti 
• 
Sospende 
• 
Non Sospende 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 22/38
 
 
 
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
 
Per questo tipo di procedimento si può ipotizzare un ordinanza o un decreto del tipo seguente 
 
 
Da decidere i modelli di stampa da associare. 
 
3.8 
Diffida al puntuale rispetto delle prescrizioni – pene sostitutive  
Considerato che  l’istituto  della  pene  sostitutive  dovrebbe  avere  una  ampia diffusione, è opportuno 
inserire anche un contenuto specifico per la diffida, sulla falsariga di quanto accade nel caso di EMA. 
 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Diffida al puntuale rispetto delle prescrizioni  - pene sostitutive 
Al nuovo contenuto vanno associati i seguente oggetti:  
• 
Convocazione per puntuale rispetto prescrizioni – pene sostitutive  
• 
Diffida al puntuale rispetto prescrizioni – pene sostitutive  
e i seguenti esiti 
• 
Diffida 
• 
Non Diffida

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 23/38
 
 
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
pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
 
Per questo tipo di procedimento si può ipotizzare un decreto del tipo di quello previsto per l’EMA 
 
Puo essere adottata la suddetta form anche per il procedimento in esame? 
Deve essere prevista la possibilità di esprimersi anche con ordinanza? 
Al momento per questo provvedimento sono previsti 2 modelli di stampa: Decreto generico, Decreto diffida 
puntuale rispetto prescrizioni. 
 
3.9 
Gestione Licenza - pene sostitutive  
L’art.  69 legge 689/1981, al primo comma,  prevede un istituto parzialmente nuovo le licenze per i soggetti 
sottoposti a pene sostitutive.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 24/38
 
 
 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Licenza - pene sostitutive (art. 69 L. 689/81) 
Al nuovo contenuto vanno associati i seguente oggetti:  
• 
Licenza - pene sostitutive (art. 69 L. 689/81) 
e i seguenti esiti 
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
pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
 
Per questo tipo di procedimento si può ipotizzare un decreto simile a quello già previsto in SIUS per le altre 
tipologie di licenza, es. 
 
 
Puo essere adottata la suddetta form anche per il procedimento in esame?

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 25/38
 
 
Al momento per questo provvedimento sono previsti 5 modelli di stampa: Decreto generico, Decreto 
concessione licenza semilibero, Decreto Non Luogo a Provvedere licenza semilibero, Decreto Rigetto licenza 
semilibero, Decreto Inammissibilità licenza semilibero, Decreto Incompetenza licenza semilibero. 
 
3.10 Licenza - pene sostitutive - Inosservanza prescrizioni (art. 69 L. 689/81) 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Licenza - pene sostitutive – inosservanza prescrizioni (art. 69 L. 689/81) 
Al nuovo contenuto vanno associati i seguente oggetti:  
• 
Valutazione  revoca  Licenza – pene  sostitutive  (artt. 53  bis  O.P. - 69  L.  689/81) 
• 
Esclusione computo Licenza – pene sostitutive (artt. 53 bis O.P. - 69 L. 689/81) 
e i seguenti esiti 
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
• 
Dichiara la propria incompetenza  
 
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
 
Per questo tipo di procedimento si può ipotizzare un decreto simile a quello già previsto in SIUS per la Licenza 
per internati – inosservanza prescrizioni

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 26/38
 
 
 
 
Puo essere adottata la suddetta form anche per il procedimento in esame? 
Al momento per questo provvedimento sono previsti 2 modelli di stampa: Decreto revoca licenza internato, 
Decreto scomputo licenza internato. 
 
3.11 Sospensione lavoro pubblica utilità sostitutivo  
L’art.  69 legge 689/1981, al secondo comma,  prevede l’applicazione di una particolare forma di sospensione 
relativa esclusivamente al lavoro di pubblica utilità. 
 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Sospensione lavoro di pubblica utilità sostitutivo (art. 69 c. 2 L. 689/81) 
Al nuovo contenuto vanno associati i seguente oggetti:  
• 
Sospensione lavoro di pubblica utilità sostitutivo (art. 69 c. 2 L. 689/81) 
e i seguenti esiti 
• 
Sospende

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 27/38
 
 
• 
Non sospende 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
 
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
 
Per questo tipo di procedimento si può ipotizzare un decreto simile a quello già previsto in SIUS per le altre 
tipologie di licenza, vedi par. 3.9. 
 
3.12 Rinvio dell’esecuzione  pena sostitutiva  
L’art.  69 legge 689/1981, Al comma 3, invece, prevede l’applicazione del  rinvio dell’esecuzione della pena 
ex artt.  146  e  147  c.p. anche  alle pene  sostitutive;  rinvio  che  viene  disposto  direttamente  dal Magistrato 
con ordinanza e che, nel caso di semilibertà, può anche essere disposto nelle forme della  detenzione  
domiciliare  (o  meglio,  si  può  sostituire  la  semilibertà  con  la  detenzione domiciliare). 
 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Rinvio dell’esecuzione pena sostitutiva (art. 69 L. 689/81 – 684 c.p.p ) 
Al nuovo contenuto vanno associati i seguente oggetti:  
 
• 
Differimento facoltativo pena sostitutiva ( Art. 69 L. 689/81 – 147 c.p.) 
• 
Differimento obbligatorio  pena  sostitutiva  (  Art.  69  L.  689/81 – 146  c.p.) 
• 
Applicazione  detenzione domiciliare sostitutiva per semilibero (art. 69 L. 689/81)     
e i seguenti esiti 
• 
Concede per un periodo 
• 
Proroga per un periodo 
• 
Applica detenzione domiciliare 
• 
Rigetta 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 28/38
 
 
• 
Dichiara la propria incompetenza  
 
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
 
Per questo tipo di procedimento si può ipotizzare un decreto simile a quello già previsto in SIUS per il Rinvio 
esecuzione sanzione sostitutiva 
 
 
Puo essere adottata la suddetta form anche per il procedimento in esame? 
Al momento per questo provvedimento è previsto solo 1 modello di stampa: Decreto generico. 
 
3.13 Revoca e Conversione pena pecuniaria sostitutiva  
L’art.  71 legge 689/1981 prevede  che  la  pena  pecuniaria sostitutiva non  pagata  possa  essere  convertita  
nella  semilibertà,  nella  detenzione  domiciliare  sostitutive  ovvero  nel  lavoro  di pubblica utilità sostitutivo.  
 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Revoca e Conversione pena pecuniaria  sostitutiva (art.71 L. 689/81) 
Al nuovo contenuto vanno associati i seguente oggetti:  
 
• 
Revoca e Conversione pena pecuniaria sostitutiva per mancato pagamento  (art.71 L. 689/81) 
 
e i seguenti esiti

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 29/38
 
 
• 
Revoca  e  converte  in  semilibertà  sostitutiva  
• 
Revoca  e  converte  in  detenzione domiciliare sostitutiva  
• 
Revoca e  converte in  lavoro di  pubblica utilità sostitutivo  
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
 
Questo tipo di procedimento non presuppone l’esistenza del fascicolo di Esecuzione Pena Sostitutiva, 
pertanto l’iscrizione, fuoriuescendo dalla logica procedimenti “padre” – “figli”, avverrà utilizzando le attuali 
funzionalità di iscrizione previste in SIUS. 
 
Per questo tipo di procedimento si può ipotizzare un’ordinanza, simile a quello già previsto in SIUS per la 
Conversione della pena pecuniaria, 
 
 
A seguito della Conferma, della validazione e deposito di questa ordinanza, l’ufficio iscriverà un procedimento 
di Esecuzione Pena Sostitutiva (vedi par. 3.2).

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 30/38
 
 
3.14 Sopravvenienza nuovo Titolo - pene sostitutive  
L’art.  76 legge 689/1981 prevede  che  la sussistenza dei requisiti dell’applicazione della  pena  sostitutiva 
vengano rivalutati dal magistrato in presenza di nuovi  titoli esecutivi. 
 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Sopravvenienza nuovo titolo - Pene sostitutive (art. 76 L. 689/81 – 51-bis O.P.) 
Al nuovo contenuto vanno associati i seguente oggetti:  
 
• 
Valutazione su permanenza  quantum  pena  per  semilibertà  sostitutiva  (Art.  55  L. 689/81 – 51-bis 
O.P.) 
• 
Valutazione su permanenza quantum pena per detenzione domiciliare  sostitutiva  (Art.  56  L. 689/81 
– 51-bis O.P.) 
e i seguenti esiti 
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
pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
 
Per questo tipo di procedimento si può ipotizzare un’ordinanza, simile a quello già previsto in SIUS per la 
Misura Aletrnativa, es.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 31/38
 
 
 
 
L’Amministrazione fornirà i modelli di stampa necessari. 
 
3.15 Sospensione esecuzione pene accessorie  
L’art.  51 quater O.P. ( disciplina delle pene accessorie in caso di concessione di misure alternative) prevede  
che  la sospensione dell’esecuzione delle pene accessorie  in caso di misure alternative o di pene sostitutive. 
 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Sospensione esecuzione pene accessorie (art. 51-quater O.P.) 
Al nuovo contenuto vanno associati i seguente oggetti:  
 
• 
Sospensione esecuzione pene accessorie – Misure alternative (art. 51-quater O.P.) 
• 
Sospensione esecuzione pene accessorie –  Pene sostitutive (Art.  76  L. 689/81 – 51-bis O.P.) 
e i seguenti esiti 
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
 
Questo tipo di procedimento non presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena 
Sostitutiva/Esecuzione Misura Alternativa, pertanto l’iscrizione, fuoriuscendo dalla logica procedimenti 
“padre” – “figli”, avverrà utilizzando le attuali funzionalità di iscrizione previste in SIUS.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 32/38
 
 
Per questo tipo di procedimento si può ipotizzare un ordinanza del tipo seguente 
 
 
L’Amministrazione fornirà i modelli di stampa necessari. 
 
 
3.16 Conversione/Rateizzazione Pena Pecuniaria Sostitutiva  
Gli artt. 102, 103 legge 689/1981  prevedono  che la pena pecuniaria non pagata possa essere convertita non  
 
più nella libertà controllata, bensì nella semilibertà e nella detenzione domiciliare sostitutive,  
 
oltre che nel lavoro di pubblica utilità. 
 
Non è possibile inserire i nuovi oggetti nell’attuale contenuto Conversione Pena Pecuniaria, in quanto per 
questi procedimenti è obbligatorio l’inserimento della Richiesta Conversione Pena Pecuniaria, con 
l’indicazione di tutti gli estremi (Anno/Numero Partiva IVA, Campione Penale, Autorità Richiedente, data 
irrevocabilità Titolo Esecutivo, etc.). Questi dati non sono necessari per la gestione dei procedimenti con Pena 
Pecuniaria sostitutiva. 
 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Conversione / Rateizzazione pena pecuniaria sostitutiva (artt. 102, 103 legge 689/1981 ) 
Al nuovo contenuto vanno associati i seguente oggetti: 
  
• 
Conversione pena pecuniaria 
• 
Rateizzazione  pena pecuniaria

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 33/38
 
 
e i seguenti esiti 
• 
Dispone conversione in semilibertà sostitutiva 
• 
Dispone conversione in detenzione domiciliare sostitutiva 
• 
Dispone conversione in lavoro di pubblica utilità sostitutivo  
• 
Dispone conversione pena irrogata dal GdP in lavoro di pubblica utilità  
• 
Rateizza       (da confermare) 
• 
Rigetta 
• 
Dichiara N.D.P./ N.L.P   
• 
Dichiara inammissibilità  
• 
Dichiara la propria incompetenza  
 
Questo tipo di procedimento non presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena 
Sostitutiva/Esecuzione Misura Alternativa, pertanto l’iscrizione, fuoriuscendo dalla logica procedimenti 
“padre” – “figli”, avverrà utilizzando le attuali funzionalità di iscrizione previste in SIUS.  
 
Per questo tipo di procedimento si può ipotizzare un ordinanza del tipo seguente 
 
 
L’Amministrazione fornirà i modelli di stampa necessari.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 34/38
 
 
 
3.17 Conversione pene pecuniarie irrogate dal Giudice di Pace  
L’art.  55 D.L. 274/2020 prevede che a richiesta del condannato la pena pecuniaria può essere convertita in 
lavoro di pubblica utilità, In  caso  di  violazione  degli  obblighi  del  lavoro  di  pubblica  utilità,  la  parte           
residua si converte in obbligo di permanenza domiciliare. Occorre, quindi, inserire un nuovo contenuto 
“figlio” specifico nel contenuto EPS.   
 
 
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente: 
 
• 
Violazione obblighi lavoro pubblica utilità (art. 55 c. 3 DL 274/2020)   
Al nuovo contenuto vanno associati i seguente oggetti:  
 
• 
Violazione obblighi lavoro pubblica utilità (art. 55 c. 3 DL 274/2020) 
e i seguenti esiti 
 
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
pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e 
richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e 
di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto. 
 
Per questo tipo di procedimento si può ipotizzare una ordinanza simile a quella proposta al precedente 
paragrafo. 
Non è chiaro cosa avviene nella gestione del procedimento di EPS.  
 
3.18 Gestione Procedimenti Esecuzione Pene Sostitutive 
Come già previsto in SIUS per i procedimenti di Esecuzione Misure Alternative, Esecuzione Sanzioni 
Sostitutive e Esecuzione Misure di Sicurezza, per la gestione dei procedimenti di Esecuzione Pene Sostitutive 
sarà aggiunta nel menu verticale dell’UDS la nuova voce

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 35/38
 
 
 
 
Che presenterà a sua volta il menu orizzontale  
 
 
 
Da cui sarà possibile  
 
- 
ricercare i procedimenti “padri” di Esecuzione Pene Sostitutive per Anno e Numero o per Intervalli di 
numeri

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 36/38
 
 
 
 
 
- 
ricercare i procedimenti “padri” di Esecuzione Pene Sostitutive a carico di un Soggetto 
 
 
 
Le due funzionalità seguiranno lo stesso flusso operativo presente in SIUS per gli altri procedimenti di 
Esecuzione. 
 
3.19 Gestione Licenze – Pene Sostitutive 
Per estendere l’attuale gestione delle Licenze per semilibertà e per internati anche alle Licenze – pene 
sostitutive saranno adeguate tutte le funzionalità, riferite a Licenza, presenti nella voce di menu verticale 
, cioè

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 37/38
 
 
 
 
- 
Ricerca Licenze per Soggetto 
Nell’attuale form 
 
 
 
Nella combo box Visualizza solo i provvedimenti relativi a, alle attuali voci “Licenze” e “Licenze per Internati” 
sarà aggiunta la nuova voce “Licenze – pene sostitutive”. Tutto il codice sarà aggiornato per gestire le nuove 
tipologie di Licenza. 
 
- 
Esecuzione Licenza 
Le attuali funzioni attivabili dalla sottostante form

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.2-
20230517_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 
1.0 
del 
04/07/2023 
Pag. 38/38
 
 
saranno aggiornate per poter  essere utilizzate anche per le Licenze – pene sostitutive. 
 
- 
Relazione Trimestrale  
L’attuale form sarà modificata 
 
 
 
Con l’aggiunta di un nuovo radio button per poter utilizzare la funzione anche per la nuova Licenza con 
conseguente aggiornamento del codice.