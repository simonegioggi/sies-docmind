---
uniqueName: siut-sie-pt-1-0-20200407-piano-dei-test-avvocatura
displayName: "SIUT SIE PT 1 0 20200407 Piano dei Test AVVOCATURA"
category: "GENERAL"
tags: []
---

# SIUT-SIE-PT-1.0-20200407-Piano dei Test AVVOCATURA

> **File originale:** `Avvocatura-SIES/Rilascio_MEV20_2020-04-07/Documentazione_AVVOCATURA/SIUT-SIE-PT-1.0-20200407-Piano dei Test AVVOCATURA.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
Piano dei Test  
Scheda n.20 
Avvocatura Sies Sedi 
 
 
 
 
 
 
 
 
 
Versione 1.0 del 07/04/2020

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PT-1.0-20200407-Piano dei Test AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 2/14 
 
 
 
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
 
 
SIUT-SIE-PT-1.0-20200407-Piano dei Test AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 3/14 
Approvazioni 
 
Nominativo 
Elaborato da 
Domenico Nania 
Verificato da
Vito Bufi
Approvato da 
Paolo Ceccanti 
Data approvazione 
07/04/2020 
Livello di riservatezza 
L3 
 
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
 
 
SIUT-SIE-PT-1.0-20200407-Piano dei Test AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 4/14 
INDICE DEI CONTENUTI 
1. 
INTRODUZIONE ....................................................................................................................... 5 
1.1. SCOPO DEL DOCUMENTO ..................................................................................................................... 5 
RIFERIMENTI ............................................................................................................................................... 5 
1.2. GLOSSARIO ....................................................................................................................................... 5 
1.2.1. 
DEFINIZIONI ................................................................................................................................... 5 
1.2.2. 
ACRONIMI E ABBREVIAZIONI .............................................................................................................. 5 
2. 
OBIETTIVI E PORTATA DEI TEST ............................................................................................... 7 
2.1. DESCRIZIONE DELLE SCELTE NELLA DEFINIZIONE DEI TEST............................................................................. 7 
2.1.1. 
ENTITÀ DA TESTARE ......................................................................................................................... 7 
2.1.2. 
ENTITÀ ESCLUSE DAL TEST ................................................................................................................. 7 
3. 
ESECUZIONE DEI TEST ............................................................................................................. 8 
4. 
DOCUMENTAZIONE ESECUZIONE TEST .................................................................................... 9 
5. 
GESTIONE DELLE ANOMALIE E RIPETIZIONE DEI TEST ............................................................. 10 
6. 
AMBIENTE DI TEST ................................................................................................................ 11 
7. 
CONFIGURAZIONE AMBIENTE ............................................................................................... 12 
7.1. CONFIGURAZIONE HW E SW ............................................................................................................... 12 
7.2. SISTEMI ESTERNI .............................................................................................................................. 12 
7.3. VINCOLI TECNICI ED ORGANIZZATIVI ..................................................................................................... 12 
8. 
STRUMENTI .......................................................................................................................... 13 
8.1. DATABASE DEI CASI DI PROVA ............................................................................................................. 13 
8.2. STRUMENTI AUTOMATICI DI SUPPORTO AI TEST ...................................................................................... 13 
9. 
SPECIFICA TEST ..................................................................................................................... 14 
9.1. DESCRIZIONE DEI CASI DI TEST ............................................................................................................ 14

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PT-1.0-20200407-Piano dei Test AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 5/14 
1. Introduzione 
1.1. Scopo del documento 
Il presente documento descrive il piano dei test per la verifica di conformità dell’intervento attivato con richiesta 
m_dg.DOG07AR.27_09_2019.0000055.U. 
L’applicativo che è stato oggetto della richiesta di intervento è il “Sistema di Consultazione Procedimenti ed Avvisi 
SIUS”. L’obiettivo dell’intervento nasce dall’esigenza dell’Amministrazione di inserire nell’ambito del sistema di 
Consultazione dei procedimenti SIUS la gestione dell’informazione della “Sede”. 
Riferimenti 
Riferimento
Nome Documento
Descrizione Documento
RIF1. 
 
m_dg.DOG07AR.27_09_2019.0000055.U. 
Richiesta scheda nr. 20 Avvocatura 
SIES Sedi 
RIF2. 
 
SIUT-SIE-SC-1.0-20191002_Scheda 
di 
intervento 
n.20_Avvocatura_SIES_Sede 
Scheda Intervento 
RIF3. 
 
m_dg.DOG07AR.05_12_2019.0000268.U 
Approvazione Scheda 
RIF4. 
 
SIUT-SIE-SI-1.3-20200317-Specifiche_Intervento_Avvocatura 
Specifiche Intervento 
RIF5. 
 
Approvazione Scheda nr.20_signed.pdf 
Approvazione Specifiche 
RIF6. 
 
SIUT-SIE-CT-1.0-20200407-Allegato-al 
piano-test 
AVVOCATURA.xls  
Elenco dei test da eseguire per la 
verifica di conformità 
1.2. Glossario 
1.2.1. Definizioni 
Definizione 
Descrizione 
 
 
 
 
1.2.2. Acronimi e abbreviazioni 
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PT-1.0-20200407-Piano dei Test AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 6/14 
Sigla
Descrizione
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
UTA 
Utente Generico Amministrazione 
VPN
Virtual Private Network

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PT-1.0-20200407-Piano dei Test AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 7/14 
2. 
Obiettivi e portata dei test 
Il presente Piano di Test è stato redatto prendendo in considerazione le funzioni utente definite nel documento 
di Specifiche dell’Intervento: “SIUT-SIE-SI-1.3-20200317-Specifiche_Intervento_Avvocatura.pdf” e, per ciascuna 
di esse, individuando le funzioni elementari nelle quali esse si scompongono. 
 
Per ogni funzione elementare sono stati definiti i casi di test che permettono di verificarne il corretto 
funzionamento secondo le regole funzionali. 
2.1. Descrizione delle scelte nella definizione dei test 
2.1.1. Entità da testare 
L’entità oggetto di verifica è l’applicativo Sistema di Consultazione Procedimenti ed Avvisi SIUS, così come definito 
nel documento di Specifiche di Intervento [RIF4.].  
 
In dettaglio, saranno oggetto di verifica: 
• 
le pagine di ricerca e di dettaglio dell’applicazione in cui sarà presente il campo sede; 
• 
la ricerca per numero procedimento che utilizzerà il valore del nuovo campo sede; 
• 
la stampa del dettaglio del procedimento in cui sarà presente il campo sede; 
• 
la pagina di elenco procedimenti per soggetto in cui sarà presente il campo ufficio/sede che ha emesso il 
provvedimento. 
 
Segue elenco dei moduli oggetto del test e del successivo rilascio. 
 
Modulo SW 
Descrizione 
Versione 
sies 
Componenti java 
12.1.0 
avvocatura 
Componenti java 
2.0.0 
 
2.1.2. Entità escluse dal test 
Sono oggetto di verifica esclusivamente i casi di test consegnati.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PT-1.0-20200407-Piano dei Test AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 8/14 
3. 
Esecuzione dei test 
I test si svolgono nell’ambiente di collaudo dell’Amministrazione secondo le modalità indicate nel piano di test e 
così come dettagliato nel documento SIUT-SIE-CT-1.0-20200407-Allegato-al piano-test AVVOCATURA.xlsx 
[RIF6.].

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PT-1.0-20200407-Piano dei Test AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 9/14 
4. 
Documentazione esecuzione test 
L’esito dei test sarà indicato nella colonna predisposta, con descrizione ‘Esito’, all’interno del documento SIUT-
SIE-CT-1.0-20200407-Allegato-al piano-test AVVOCATURA.xlsx [RIF6.]. 
 
In caso di esito positivo del test, la colonna ‘Esito’ riporterà la dicitura ‘OK’. 
In caso di esito negativo, si rimanda al paragrafo successivo per le indicazioni circa il comportamento da seguire.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PT-1.0-20200407-Piano dei Test AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 10/14 
5. 
Gestione delle anomalie e ripetizione dei test 
Di seguito l’indicazione circa le modalità di esecuzione dei test in base all’esito di ciascuno: 
1. Se l’esito del test è positivo, procedere con il test successivo; 
2. Se l’esito è negativo, registrare l’anomalia a cui associare il livello di gravità (bloccante, grave, non grave); 
3. Se l’anomalia è di gravità bloccante, sospendere i test del servizio in corso proseguendo eventualmente con 
il test successivo ripartendo dal punto 1); 
4. Dopo la correzione delle anomalie riscontrate, rieseguire tutti i test nuovamente fino all’esito positivo di tutti.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PT-1.0-20200407-Piano dei Test AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 11/14 
6. 
Ambiente di test 
Nell’ambiente di esecuzione dei test sono presenti tutti i moduli software e tutti gli adeguamenti della base dati 
indicati nelle Specifiche di Intervento [RIF4.] e volti alla soddisfazione dei requisiti richiesti.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PT-1.0-20200407-Piano dei Test AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 12/14 
7. 
Configurazione ambiente 
7.1. Configurazione hw e sw 
N.A. 
7.2. Sistemi esterni 
N.A. 
7.3. Vincoli tecnici ed organizzativi 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PT-1.0-20200407-Piano dei Test AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 13/14 
8. 
Strumenti 
8.1. Database dei casi di prova 
N.A. 
8.2. Strumenti automatici di supporto ai test 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PT-1.0-20200407-Piano dei Test AVVOCATURA 
Ver. 1.0 del 07/04/2020 
Pag. 14/14 
9. 
Specifica Test 
9.1. Descrizione dei Casi di Test 
La descrizione di dettaglio di ciascun caso di test è contenuta nel documento Allegato al Piano dei Test [RIF6.] a 
completamento del presente. 
In particolare: 
- 
Nella ‘Tabella dei test’ è contenuta la tracciatura a partire dai requisiti utente fino al singolo caso di test; 
- 
Nelle ‘Specifiche di test’ ogni caso di test è dettagliato in termini procedurali.