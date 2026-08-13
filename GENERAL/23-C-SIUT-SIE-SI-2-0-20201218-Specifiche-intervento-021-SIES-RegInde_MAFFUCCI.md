---
uniqueName: 23-c-siut-sie-si-2-0-20201218-specifiche-intervent
displayName: "23 C SIUT SIE SI 2 0 20201218 Specifiche intervento 021 SIES RegInde MAFFUCCI"
category: "GENERAL"
tags: []
---

# 23-C-SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-SIES-RegInde_MAFFUCCI

> **File originale:** `MEV/SCHEDA_021/Docs/23-C-SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-SIES-RegInde_MAFFUCCI.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
 
Specifiche Intervento Scheda n. 021 
 
SIES - ReGIndE 
 
 
 
 
 
 
 
Versione 2.0 del 18/12/2020

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 2/81 
 
 
 
 
 
 
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
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 3/81 
 
Approvazioni 
 
Nominativo 
Funzione 
Elaborato da 
Umberto Mignogna 
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
18/12/2020 
 
Livello di riservatezza 
L4 
 
 
Elenco versioni 
Versione 
Data  
Motivo 
Modifica 
1.0 
05/08/2020 
Prima Emissione 
 
1.1 
09/10/2020 
Seconda Emissione 
 
Revisione 
a 
seguito 
della 
e-mail 
dell’Amministrazione (PO) del 03/09/2020 ore 
17:24 – oggetto: ‘SIES Scheda Intervento n.21 
Gestione Anagrafica Avvocati - RegInde": 17-
SIUT-SIE-SI-1.0-20200805-Specifiche-
intervento-021-SIES-RegInde’ : 
• 
Al par. 6.1 specificato l’aggiornamento 
di 4 fori individuati a valle dell’analisi 
dei dati ReGInde; 
• 
Al par. 6.2.3.1 è stata aggiornata le 
descrizione della ricerca in caso di 
searchLimit Exception (punto 3 della e-
mail) e descritta la necessità per SIES di 
visualizzare lo stato dell’Avvocato 
(punto 6 della e-mail); 
• 
Ai par. 6.1.4.1 e 6.2.3.1 sono state 
inserite le problematiche relative alle 
tabelle COMUNE di SIES e AVVOCATO 
di SIES e ReGIndE  e i relativi interventi 
di soluzione (punto 4 della e-mail); 
• 
Al par. 6.2.3.1 pag. 39 è stato precisato 
che la sovrascrittura dell’indirizzo non 
rappresenta problema per SIES (punto 
5 della e-mail); 
• 
Al par. 6.2.5.2 è stato aggiornato il 
protocollo di sicurezza; 
• 
Al par. 6.2.5.7 è stato indicato che 
ReGIndE fornirà il certificato di chiave 
pubblica;

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 4/81 
 
Versione 
Data  
Motivo 
Modifica 
• 
Al par. 6.5.1 sono state inserite alcune 
precisazioni 
sulle 
modalità 
di 
esecuzione della Bonifica; 
2.0 
15/12/2020 
Terza Emissione 
    Revisione a seguito della call svoltasi su MS 
Team tra personale dell’Amministrazione (PO) 
e personale del Fornitore in data 10/12/2020 
ore 9:30 – oggetto: ‘SIES Scheda Intervento 
n.21 Gestione Anagrafica Avvocati - RegInde": 
17-SIUT-SIE-SI-1.0-20200805-Specifiche-
intervento-021-SIES-RegInde’ : 
• 
Al par. 6.1  pag. 16 primo capoverso 
specificato Foro_Avvocati; 
• 
Al par. 6.1 pag. 16  specificato che i 4 
fori 
con 
diversa 
denominazione 
dall’attuale saranno trattati con le 
stesse modalità previste per Napoli 
Nord; 
• 
Al par. 6.2.3.1 pag. 36  specificato che i 
risultati 
saranno 
filtrati 
per 
FORO_AVVOCATI; 
• 
par. 
6.2.3.1 
pag. 
38 
inserito 
riferimento 
a 
procedura 
aggiornamento tabelle COMUNE e 
CG_REF_CODES; 
• 
par. 6.2.3.1 pag. 39 specificata la 
possibilità di inserire manualmente un 
difensore con codice catastale non 
presente 
nella 
tabella 
COMUNE 
aggiornata; 
• 
Ai par. 6.2.3.1 pag. 41  specificato che 
indirizzo sarà sovrascritto anche se non 
valorizzato su ReGIndE; 
• 
Al par. 6.3.3.2 pag. 69 specificate 
modalità di trattamento avvocato con 
codice catastale non presente in 
tabella COMUNE; 
• 
Al par. 6.5.1 specificati prerequisiti per 
attività di bonifica Avvocato;

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 5/81 
 
Versione 
Data  
Motivo 
Modifica 
• 
Alle pagg. 75 e seguenti inserito nuovo 
cap. 
6.6 
Aggiornamento 
Tabelle 
COMUNE e CF_REF_CODES. 
 
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
Salvatore Piazza 
RTI 
 
Technical Manager 
Sergio Tamburrini 
RTI 
 
Organization Manager 
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
 
Referente PMO e Qualità 
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
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 6/81 
 
INDICE DEI CONTENUTI 
1 
INTRODUZIONE ........................................................................................................................ 10 
1.1 
SCOPO DEL DOCUMENTO........................................................................................................... 10 
1.2 
RIFERIMENTI .......................................................................................................................... 10 
1.3 
GLOSSARIO ............................................................................................................................ 10 
1.3.1 
DEFINIZIONI ........................................................................................................................ 10 
1.3.2 
ACRONIMI E ABBREVIAZIONI ................................................................................................... 10 
2 
DEFINIZIONE DELL’OBIETTIVO .................................................................................................. 12 
3 
ARCHITETTURA DEL SISTEMA ................................................................................................... 13 
3.1 
ARCHITETTURA ....................................................................................................................... 13 
4 
SPECIFICHE DEI REQUISITI ........................................................................................................ 14 
4.1 
PREMESSA ............................................................................................................................. 14 
4.2 
ELENCO REQUISITI ................................................................................................................... 15 
5 
INTERFACCE ............................................................................................................................. 15 
6 
DESCRIZIONE DELL’INTERVENTO .............................................................................................. 16 
6.1 
REQ-SIE-021-01_FN.01 -  GESTIONE NUOVI FORI (FORO DI NAPOLI NORD) ................................ 16 
6.1.1 
MODULI SW ....................................................................................................................... 23 
6.1.2 
ARCHITETTURA .................................................................................................................... 27 
6.1.3 
INTERFACCE UTENTE ............................................................................................................. 27 
6.1.4 
BASI DATI ........................................................................................................................... 30 
6.1.4.1 
Selezione Lista Fori SIES ............................................................................................ 30 
6.1.4.2 
Tabella Avvocati SIES ................................................................................................ 31 
6.1.5 
WEB SERVICES .................................................................................................................... 31 
6.1.6 
XSD ................................................................................................................................. 31 
6.1.7 
CONFIGURAZIONE ................................................................................................................ 32 
6.1.8 
TUTORIAL ........................................................................................................................... 32 
6.2 
REQ- SIE-021-02_FN.01 -  RICERCA SU REGINDE ....................................................................... 32 
6.2.1 
MODULI SW ....................................................................................................................... 32 
6.2.2 
ARCHITETTURA .................................................................................................................... 34 
6.2.3 
INTERFACCE UTENTE ............................................................................................................. 34 
6.2.3.1 
Sottosistema SIEP ..................................................................................................... 34 
6.2.3.2 
Sottosistema SIGE ..................................................................................................... 48 
6.2.3.3 
Sottosistema SIUS ..................................................................................................... 58 
6.2.4 
BASI DATI ........................................................................................................................... 63 
6.2.5 
WEB SERVICES .................................................................................................................... 64 
6.2.5.1 
Gestione delle fault ................................................................................................... 65 
6.2.5.2 
Altre specifiche per il servizio .................................................................................... 66 
6.2.6 
XSD ................................................................................................................................. 66 
6.2.7 
CONFIGURAZIONE ................................................................................................................ 66

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 7/81 
 
6.2.8 
TUTORIAL ........................................................................................................................... 66 
6.3 
REQ- SIE-021-03_FN.01 – INSERIMENTO MANUALE: INDISPONIBILITÀ REGINDE O AVVOCATO NON 
PRESENTE ....................................................................................................................................... 66 
6.3.1 
MODULI SW ....................................................................................................................... 66 
6.3.2 
ARCHITETTURA .................................................................................................................... 67 
6.3.3 
INTERFACCE UTENTE ............................................................................................................. 67 
6.3.3.1 
Inserimento manuale: Indisponibilità ReGIndE o Avvocato Non Presente .................. 67 
6.3.3.2 
Inserimento manuale avvocato sul sistema SIES ....................................................... 69 
6.3.4 
BASI DATI ........................................................................................................................... 70 
6.3.5 
WEB SERVICES .................................................................................................................... 70 
6.3.6 
XSD ................................................................................................................................. 70 
6.3.7 
CONFIGURAZIONE ................................................................................................................ 70 
6.3.8 
TUTORIAL ........................................................................................................................... 70 
6.4 
REQ- SIE-021-04_FN.01 – INTERVENTI SU FUNZIONI SIES DI GESTIONE AVVOCATI ............................. 71 
6.4.1 
MODULI SW ....................................................................................................................... 71 
6.4.2 
ARCHITETTURA .................................................................................................................... 71 
6.4.3 
INTERFACCE UTENTE ............................................................................................................. 71 
6.4.4 
BASI DATI ........................................................................................................................... 72 
6.4.5 
WEB SERVICES .................................................................................................................... 72 
6.4.6 
XSD ................................................................................................................................. 72 
6.4.7 
CONFIGURAZIONE ................................................................................................................ 73 
6.4.8 
TUTORIAL ........................................................................................................................... 73 
6.5 
REQ- SIE-021-05_FN.01 – BONIFICA ANAGRAFICA AVVOCATI SIES ................................................ 73 
6.5.1 
Bonifica dei dati presenti nella tabella Avvocato .......................................................... 73 
6.5.2 
MODULI SW ....................................................................................................................... 75 
6.5.3 
ARCHITETTURA .................................................................................................................... 75 
6.5.4 
INTERFACCE UTENTE ............................................................................................................. 75 
6.5.5 
BASI DATI ........................................................................................................................... 75 
6.5.6 
WEB SERVICES .................................................................................................................... 76 
6.5.7 
XSD ................................................................................................................................. 76 
6.5.8 
CONFIGURAZIONE ................................................................................................................ 76 
6.5.9 
TUTORIAL ........................................................................................................................... 76 
6.6 
REQ- SIE-021-06_FN.01 – AGGIORNAMENTO TABELLE COMUNE E CG_REF_CODES DI SIES........... 76 
6.6.1 
Aggiornamento dei dati presenti nella tabella COMUNE di SIES ................................... 76 
6.6.2 
Aggiornamento dei dati presenti nella tabella CG_REF_CODES (domini PROVINCIA, 
REGIONE, NAZIONE) ................................................................................................................. 78 
6.6.2.1 
Aggiornamento dominio PROVINCIA ......................................................................... 78 
6.6.2.2 
Aggiornamento dominio REGIONE ............................................................................ 79 
6.6.2.3 
Aggiornamento dominio NAZIONE ............................................................................ 80 
6.6.3 
MODULI SW ....................................................................................................................... 80 
6.6.4 
ARCHITETTURA .................................................................................................................... 81 
6.6.5 
INTERFACCE UTENTE ............................................................................................................. 81 
6.6.6 
BASI DATI ........................................................................................................................... 81

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 8/81 
 
6.6.7 
WEB SERVICES .................................................................................................................... 81 
6.6.8 
XSD ................................................................................................................................. 81 
6.6.9 
CONFIGURAZIONE ................................................................................................................ 81 
6.6.10 
TUTORIAL ....................................................................................................................... 81 
 
Figura 1: Architettura del sistema SIES ............................................................................................ 14 
Figura 2: Sezione notifica Difensore ................................................................................................ 18 
Figura 3: Alert per Comune non Esistente ....................................................................................... 18 
Figura 4: Form ricerca su ReGinE ..................................................................................................... 18 
Figura 5: Combo-box dei fori ........................................................................................................... 19 
Figura 6: [Esempio Template 1] ....................................................................................................... 20 
Figura 7: [Esempio Template 2] ....................................................................................................... 21 
Figura 8: Alert per variazione foro ................................................................................................... 22 
Figura 9: Form di dettaglio procedimento ....................................................................................... 22 
Figura 10: Form di esempio per messaggio di warning .................................................................... 23 
Figura 11: Sezione destinatario Notifica - SIEP ................................................................................. 28 
Figura 12: Sezione destinatario Notifica - SIUS ................................................................................ 29 
Figura 13: Sezione destinatario Notifica - SIGE ................................................................................ 30 
Figura 14: Form inserimento difensore procedimento SIEP - nuova ................................................ 36 
Figura 15: Form di attivazione ricerca su ReGIndE ........................................................................... 37 
Figura 16: Form di ricerca su ReGIndE con segnalazione di eccessive occorrenze con criteri impostati
 ....................................................................................................................................................... 38 
Figura 17: Form Elenco Avvocati ReGIndE ....................................................................................... 38 
Figura 18: Form dettaglio Avvocato selezionato .............................................................................. 41 
Figura 19: Form dettaglio avvocato procedimento SIEP................................................................... 43 
Figura 20: Form sostituzione Difensore procedimento SIEP ............................................................. 44 
Figura 21: Form Iscrizione Istanza da Soggetto - Attuale.................................................................. 45 
Figura 22: popup Ricerca e seleziona Avvocato SIES ........................................................................ 46 
Figura 23: Form Iscrizione Istanza da Titolo Esecutivo - Attuale ....................................................... 47 
Figura 24: Form Iscrizione Istanza da Procedimento SIEP ................................................................ 48 
Figura 25: Form sostituzione Assegnazione Difensore procedimento SIGE - Attuale ........................ 49 
Figura 26: Form sostituzione Assegnazione Difensore procedimento SIGE - Nuova ......................... 50 
Figura 27: Form Dettaglio Difensore procedimento SIGE - Attuale .................................................. 52 
Figura 28: Form Dettaglio Difensore procedimento SIGE - Nuova .................................................... 53 
Figura 29: Form Sostituzione Difensore procedimento SIGE - Nuova ............................................... 54 
Figura 30: Form Inserimento Difensore procedimento SIGE – Parti in causa .................................... 55 
Figura 31: Form Inserimento Difensore Parte .................................................................................. 56 
Figura 32: Form Dettaglio Fissazione Udienza procedimento SIGE .................................................. 57 
Figura 33: Form Inserimento Difensore procedimento SIGE Parti in casusa - Nuova ........................ 58 
Figura 34: Form Assegnazione Difensore procedimento SIUS - Attuale............................................ 59 
Figura 35: Form Assegnazione Difensore procedimento SIUS - Nuova ............................................. 60 
Figura 36: Form Dettaglio Difensore procedimento SIUS - Attuale .................................................. 62 
Figura 37: Form Dettaglio Difensore procedimento SIUS - Nuova .................................................... 62

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 9/81 
 
Figura 38: Form Sostituzione Difensore procedimento SIUS - Nuova ............................................... 63 
Figura 39: Form Ricerca Difensore su ReGIndE in caso di assenza collegamento ............................. 67 
Figura 40: Form Ricerca Difensore su ReGIndE in caso nessun occorrenza trovata .......................... 67 
Figura 41: Form Elenco Avvocati SIES .............................................................................................. 68 
Figura 42: Form Esito Ricerca Difensori SIES in caso di nessun occorrenza trovata .......................... 68 
Figura 43: Form Inserimento Difensore in SIES ................................................................................ 69 
Figura 44: Form Gestione Difensori - Attuale ................................................................................... 71 
Figura 45: Form Gestione Difensori - Nuova .................................................................................... 72 
Figura 46: Form Elenco Difensori - Attuale ...................................................................................... 72 
Figura 47: Form Elenco Difensori - Nuova ........................................................................................ 72

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 10/81 
 
1 INTRODUZIONE 
1.1 Scopo del documento 
Il presente documento riporta le specifiche di intervento sul software, metodologia WATERFALL, al fine di 
soddisfare i requisiti espressi dall’Amministrazione e descritti nella scheda di intervento SIUT-SIE-SC-1.3-
20200616 Scheda intervento Scheda_n.21_SIES_ReGIndE.pdf. 
 
1.2 Riferimenti 
Riferimento 
Nome Documento 
Descrizione Documento 
RIF1 
SIUT-SIE-SC-1.3-20200616 Scheda intervento 
Scheda_n.21_SIES_ReGIndE.pdf 
Scheda di intervento 
RIF2 
m_dg.DOG07AR.14/07/2020.0001154.U 
 
Approvazione scheda intervento 
RIF3 
SIGI_PNL_AA_2017 04 12_1.2_Architettura SIES.doc 
Documento di Architettura 
 
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
Manutenzione EVolutiva

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 11/81 
 
Sigla 
Descrizione 
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
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 12/81 
 
2 DEFINIZIONE DELL’OBIETTIVO 
 
L’intervento in oggetto è stato richiesto con comunicazione m_dg.DOG07AR.27_09_2019.0000056.U  e rientra 
nel servizio di Manutenzione Evolutiva. 
 
Tale documento espone gli interventi attinenti alle funzioni da prevedere nel sistema SIES con lo scopo finale 
di ‘abilitare’ i vari sistemi distrettuali del SIES all’interconnessione con il sistema del Registro Generale degli 
Indirizzi Elettronici, in modo da avere un’entità DIFENSORE ‘certificata’, e nello stesso tempo di introdurre la 
gestione dei nuovi fori in particolare la gestione del FORO di NAPOLI NORD. 
 
L’intervento mira ad una gestione coerente ed auto consistente dell’entità DIFENSORE nell’interezza di tutto il 
sistema SIES, pertanto le varie dinamiche di implementazione saranno relative ai tre sottosistemi SIEP, SIUS e 
SIGE. 
 
Si fa presente che nel prosieguo del documento si farà sempre riferimento ad un’interconnessione, del SIES 
verso il ReGIndE, in una modalità di tipo ‘diretta’, ossia il sistema SIES, per le casistiche previste dai requisiti, 
farà un accesso diretto ai servizi esposti dal sistema del Registro Generale degli Indirizzi Elettronici tramite 
invocazione dei metodi necessari sugli appositi endpoint pubblicati su rete giustizia.  
Si esplicita che in un’ottica di implementazione del concetto di ‘Anagrafica Centralizzata’ nell’ambito della 
reingegnerizzazione del sistema penale in conformità anche al disegno architetturale generale proposto per il 
progetto Beccaria, quanto specificato in tale documento potrebbe necessitare di attività di refactory, una volta 
stabilizzata l’architettura Beccaria definitiva.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 13/81 
 
3 ARCHITETTURA DEL SISTEMA 
3.1 
Architettura 
L’intervento in oggetto non introduce variazioni architetturali, rispetto al sistema attuale. Si riporta a titolo 
esemplificativo lo schema generale attuale del singolo sistema distrettuale del SIES.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 14/81 
 
Application Server SIES
Web Service
per interoperabilità 
e per Avvocatura
Moduli Funzionalità
Sistema 
SIES
Postazione utente
Web Browser
HTTP/HTTPS
Server JMS
Code messaggi
per interoberabilità
nodi 
SIES
JDBC
JMS
Base Dati SIES
RDBMS
JDBC
 
Figura 1: Architettura del sistema SIES 
 
Per la descrizione dettagliata sull’architettura del sistema SIES si rimanda al documento architetturale [RIF3]. 
 
4 SPECIFICHE DEI REQUISITI 
4.1 Premessa 
Sulla base degli applicativi oggetto del contratto e delle aree funzionali, la convenzione per l’identificazione dei 
requisiti è riportata di seguito.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 15/81 
 
Ciascun requisito è individuato da un identificativo univoco nella forma [REQ-SIS-nnn-mm_ZZ.pp], dove la 
parte evidenziata in grigio riporta il macro-requisito espresso dall’Amministrazione e codificato nella scheda di 
intervento1, i restanti caratteri identificano rispettivamente: 
 
• ZZ il tipo requisito (vedere la tabella di seguito riportata); 
• pp il progressivo requisito nell’ambito del tipo requisito. 
Tipo Requisito 
Descrizione  
AM 
Ambientale 
AR 
Architetturale 
CF 
Configurazione 
ES 
Esecuzione 
FN 
Funzionale 
UI 
Interfaccia Utente 
PR 
Prestazionali 
IN 
Interoperabilità 
SC 
Sicurezza 
SI 
Sistema 
TU 
Tutorial 
RG 
Relazione Giuridica 
 
4.2 Elenco Requisiti 
Codice Requisito 
Descrizione 
Riferimenti  
REQ-SIE-021-01_FN.01 
Gestione Nuovi Fori (FORO di NAPOLI NORD) 
REQ-SIE-021-02_FN.01 
Ricerca su ReGIndE 
REQ-SIE-021-03_FN.01 
Inserimento Manuale: Indisponibilità ReGIndE o Avvocato Non 
Presente 
REQ-SIE-021-04_FN.01 
Interventi su Funzioni SIES di Gestione Avvocati 
REQ-SIE-021-05_FN.01 
Bonifica Anagrafica Avvocati SIES 
 
5 INTERFACCE 
Nel caso fossero oggetto della modifica, le interfacce interessate dall’intervento saranno riportate all’interno 
dei paragrafi che descrivono ciascun intervento. 
Le immagini riportate hanno lo scopo di facilitare la comprensione dell’intervento, ma potrebbero differire 
dalle effettive maschere dell’applicativo. 
 
1 Si riporta la codifica dei macro-requisiti espressi dall’Amministrazione presente nella scheda di 
intervento: 
• 
REQ Requisito; 
• 
SIS identifica il sistema (cfr. SIUT-GEN-SN-2.2-20191023-Standard di nomenclatura);  
• 
nnn è il numero della scheda di richiesta intervento; 
• 
mm è il numero progressivo del requisito espresso dall’Amministrazione.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 16/81 
 
6 DESCRIZIONE DELL’INTERVENTO 
In riferimento ai tre sottosistemi di cui si compone l’applicativo SIES è fatta richiesta: 
 
✓ di integrare la gestione di nuovi fori (es. Napoli Nord); 
✓ di integrare la ricerca dell’avvocato da associare al procedimento SIEP, SIUS e SIGE andando a recuperare 
i dati dello stesso dal sistema ReGIndE (Registro Generale degli Indirizzi Elettronici); 
✓ di bonificare i dati pregressi, presenti nella tabella Avvocato di SIES, in base ai dati presenti su ReGIndE, al 
fine di rendere univoci i record delle anagrafiche degli avvocati. 
 
In maniera schematica, si riportano i principali punti che costituiscono l’intervento in oggetto: 
a) Inserimento e gestione nuovi fori, in particolare integrazione del foro di Napoli Nord nelle forms del 
sistema e nei template che utilizzano l’entità foro avvocato [REQ-SIE-021-01_FN.01]; 
b) Modifica pagine per creazione link alla nuova funzione di ricerca su ReGIndE [REQ-SIE-021-02_FN.01]; 
c) Realizzazione Funzione di Ricerca su ReGIndE [REQ-SIE-021-02_FN.01]; 
d) Inserimento manuale su SIES, per indisponibilità ReGIndE o non trovato su ReGIndE [REQ-SIE-021-
03_FN.01]; 
e) Modifica dell’attuale comportamento del sistema per la gestione degli avvocati in modo da evitare la 
duplicazione delle anagrafiche nella tabella AVVOCATO: disattivazione delle funzioni di Inserimento e 
Modifica Difensore [REQ-SIE-021-04_FN.01]; 
f) Bonifica dati pregressi al fine di rendere univoci i record delle anagrafiche degli avvocati [REQ-SIE-021-
05_FN.01]:  
la bonifica sarà realizzata per tutte le anagrafiche avvocato già presenti su SIES che risultino associate ad 
almeno un fascicolo con procedimenti in corso. 
Per dette anagrafiche, i dati SIES saranno aggiornati con i dati di ReGIndE, a parità di anagrafica trovata. 
Tutti i record bonificati saranno contraddistinti dal valore ‘Sì’ del FLAG_REGINDE. 
 
In generale, l’intervento vede come premessa le seguenti regole: 
✓ tutti gli avvocati aventi FLAG_REGINDE = ‘SI’ NON devono essere oggetto di alcuna modifica nell’ambito 
del sistema SIES, considerando i dati provenienti da ReGIndE dati certificati; 
✓ tutti gli avvocati aventi FLAG_REGINDE = ‘NO’ NON devono essere più gestiti in alcun modo nel sistema 
SIES, fatta eccezione per quel che concerne l’attivazione degli alert descritti nei paragrafi successivi. 
 
6.1 REQ-SIE-021-01_FN.01 -  Gestione Nuovi Fori (FORO di NAPOLI NORD) 
Il requisito espresso dall’Amministrazione determina un intervento evolutivo per la gestione di un nuovo foro. 
Per la descrizione della soluzione si farà riferimento, come esempio, al FORO di NAPOLI NORD. 
Si precisa che la soluzione di seguito dettagliata garantirà la gestione di altri eventuali nuovi fori nei tre 
sottosistemi SIES. 
La soluzione per la realizzazione di quanto richiesto verterà nello ‘svincolare’ l’entità del FORO dalla tabella 
COMUNE, facendo in modo che il dominio ‘FORO_AVVOCATI’, presente nella tabella CG_REF_CODES, sia 
indipendente ed auto consistente. 
Il dominio ‘FORO_AVVOCATI’ sarà ‘responsabile’ di mappare la descrizione del FORO ed il codice del comune 
sede del FORO (Codice ISTAT).

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 17/81 
 
Il FORO AVVOCATI, così come dettagliato al par. 6.2, sarà utilizzata quale dato di ricerca per l’interrogazione 
dei servizi web esposti da ReGIndE. 
 
Si segnala che la soluzione che si adotterà in relazione alla risoluzione della problematica FORO NAPOLI NORD 
non avrà impatto con la gestione già in essere sul sistema SIES del comune NAPOLI NORD, censito nella tabella 
COMUNE con codice ISTAT fittizio. 
Pertanto, il comportamento attuale del sistema circa l’utilizzo dell’entità comune NAPOLI NORD NON SARA’ in 
alcun modo modificato con l’introduzione della gestione del nuovo FORO NAPOLI NORD. 
 
Il perimetro dell’intervento per l’inserimento e la gestione del nuovo foro attiene esclusivamente all’entità 
FORO e alla sua relazione con l’AVVOCATO. 
Ciò significa che l’entità FORO sarà gestita in tutte le pagine che ad oggi già utilizzano l’informazione del foro 
di appartenenza di un DIFENSORE, ossia nelle pagine ove è prevista la notifica al DIFENSORE tramite UNEP. 
 
Dalla 
analisi 
dei 
dati 
relativi 
all’ultima 
tabella 
degli 
Avvocati 
estratta 
da 
ReGIndE 
(tabellefisse18novembre2020.xlsx), inviata dall’Amministrazione – Area Civile, è emerso quanto segue: 
 
- 
in ReGIndE sono presenti due fori che pur riferiti nel COA ai Comuni di Forlì (COA040012) e Massa 
(COA045010) hanno una Descrizione non riferita solo al Comune, infatti fanno riferimento 
rispettivamente al Foro di FORLÌ-CESENA ed al Foro di MASSA CARRARA, mentre in SIES sono gestiti 
come Foro di Forlì e Foro di Massa.  
 
- 
in ReGIndE sono presenti i due fori di REGGIO CALABRIA (COA080063) e REGGIO EMILIA (COA035033), 
la cui descrizione non corrisponde alla descrizione ufficiale dei comuni, rispettivamente REGGIO DI 
CALABRIA e REGGIO NELL’EMILIA.  
 
Tali Fori (foro di FORLÌ-CESENA, foro di MASSA CARRARA, foro di REGGIO CALABRIA e foro di REGGIO EMILIA) 
saranno gestiti in SIES con le stesse modalità previste per il foro di NAPOLI NORD, cioè svincolando la 
descrizione del FORO dalla descrizione del Comune Sede. I records della tabella AVVOCATO di SIES aventi la 
colonna FORO valorizzata con le attuali descrizioni (Forlì, Massa, Reggio di Calabria, Reggio nell’Emilia) saranno 
aggiornate con le descrizioni utilizzate in ReGIndE. 
 
Nello specifico, nelle varie maschere e template che riportano la descrizione del foro, saranno visualizzate le 
nuove descrizioni in sostituzione di quelle attuali previste dal SIES. Il codice Istat del comune di riferimento 
resta invece invariato. 
 
 
Di seguito la schematizzazione per punti di quanto sarà realizzato: 
 
1. Per le notifiche al DIFENSORE si utilizzerà come descrizione del FORO associato all’Avvocato quella 
prevista, cioè NAPOLI NORD [vedere testo sottolineato figura 2]; come sede dell’autorità UNEP relativa al 
Foro di Napoli Nord, invece, si farà riferimento al comune di AVERSA [vedere riquadro nella figura 2];

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 18/81 
 
 
Figura 2: Sezione notifica Difensore 
 
2. Tutti i template che riportano l’informazione della sede UNEP, nei casi in cui la notifica sia inviata ad un 
avvocato del FORO NAPOLI NORD, mostreranno, ove previsto, come sede di riferimento il comune di 
AVERSA [vedere immagini di Esempio Template 1 e 2 riportate di seguito]; 
 
3. Per le notifiche al DIFENSORE sarà bloccato il salvataggio della coppia Autorità Destinazione/sede Napoli 
Nord, per qualsiasi autorità selezionata, con il seguente messaggio:  
 
 
Figura 3: Alert per Comune non Esistente 
 
4. Le form che presentano la combo dei fori, in automatico mostreranno la nuova lista dei fori ‘arricchita’ con 
il nuovo foro ‘NAPOLI NORD’: 
 
 
 
Figura 4: Form ricerca su ReGinE 
 
nella combo box Foro sarà presente anche il nuovo foro

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 19/81 
 
 
 
Figura 5: Combo-box dei fori 
 
 
I tre sottosistemi saranno allineati a quanto detto ai punti 1, 2, 3 e 4. 
 
A seguire un esempio di template che contemplano la modifica relativa alla gestione del foro di NAPOLI NORD.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 20/81 
 
 
Figura 6: [Esempio Template 1]

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 21/81 
 
 
Figura 7: [Esempio Template 2] 
 
 
Nell’ambito della realizzazione del requisito di gestione di un nuovo foro, si rende necessario salvaguardare i 
dati pregressi relativi ai procedimenti in corso. Considerando la possibilità che un avvocato possa avere una 
variazione di foro di appartenenza, il sistema gestirà la storicizzazione dell’associazione Anagrafica 
Avvocato/Foro di Appartenenza già esistente. 
 
Nello specifico, a fronte di un’attività di bonifica dei dati, quindi di un ‘match’ tra i dati presenti sulla tabella 
AVVOCATI del SIES e dei dati presenti nella tabella ‘SOGGETTI’ del sistema ReGIndE, supponiamo di individuare 
un dato avvocato che ha tutte le corrispondenze uguali in entrambe le tabelle a meno del foro di appartenenza. 
In questo caso non si procederà alla bonifica del dato su SIES, ma per il record individuato sarà impostato il 
campo FLAG_REGINDE =’NO’ ed inoltre sarà settata la data_fine_validità in quanto l’associazione anagrafica 
avvocato/foro non è più esistente.  
 
Per tali casistiche, sulla pagina di dettaglio del fascicolo sarà attivato, per i dati storicizzati a causa della 
variazione del Foro e non bonificati (FLAG_REGINDE =’NO’), un alert che NON costituirà errore bloccante ma 
sarà semplicemente un avviso per l’utente, il quale dovrà procedere a rieseguire l’associazione del difensore 
al fascicolo in lavorazione, dal momento che il foro di appartenenza risulta variato. 
Per le modalità di visualizzazione dell’alert sarà seguita la stessa logica utilizzata per la Nuova Geografia 
Giudiziaria.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 22/81 
 
 
Per cui se si accede al Dettaglio del procedimento SIEP si riceverà prima il seguente messaggio 
 
 
Figura 8: Alert per variazione foro 
 
e successivamente alla conferma nella form di Dettaglio saranno evidenziati in giallo (blinkante) il Cognome, 
Nome ed il Foro di appartenenza. 
 
 
Figura 9: Form di dettaglio procedimento 
 
Se non si procede alla certificazione dell’avvocato, un messaggio di warning sarà riportato su tutte le form di 
emissione provvedimento, es.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 23/81 
 
 
Figura 10: Form di esempio per messaggio di warning 
 
Riassumendo quindi i punti di intervento per la gestione del nuovo foro Napoli Nord sono: 
 
- 
Caratterizzazione del dominio FORO_AVVOCATO su cg_refs_code; 
- 
Censimento del nuovo foro nel dominio su specificato; 
- 
Intervento su ogni pagina su elencata per ‘aggiornare’ la sezione relativa alla notifica al difensore; 
- 
Implementare per ogni pagina su elencata, i controlli che bloccano il salvataggio della coppia UNEP + 
comune Napoli nord; 
- 
Gestire l’Alert dell’avvocato sulla pagina di dettaglio del procedimento; 
- 
Gestire il messaggio di ‘avviso warning’ nelle pagine del SIES; 
 
6.1.1 Moduli sw  
Modifica di tutte le seguenti jsp contenenti tra le autorità destinatarie l’UNEP per la notifica agli avvocati per 
svincolare il Foro dalla sede:   
 
siep 
 
 calcolopena 
 
 
LoadEmissioneProvvedimento.jsp (2 matches) 
 
 
LoadInsComNuovoResPenaRidetPenaAltro.jsp (2 matches) 
 
 
LoadInserisciComputoCustodiaCautelare.jsp (2 matches) 
 
 
LoadInserisciFungibilita.jsp (2 matches) 
 
 
LoadInsOSNuovoResPenaRidetPenaAltro.jsp (2 matches) 
 
 
LoadInsOSNuovoResPenaRidetPenaRidimLA.jsp (2 matches) 
 
 
LoadRidetPenaAltro.jsp (2 matches)

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 24/81 
 
 
 cumulo 
 
 
LoadInserisciStampaCumulo.jsp (2 matches) 
 
 liberazioneanticipata 
 
 
LoadInsericiComunicazioneErgastolo.jsp (2 matches) 
 
 
LoadInsericiComunicazioneLibero.jsp (2 matches) 
 
 
LoadInserisciComunicazioneReclamoRimediRisarcitori.jsp (2 matches) 
 
 
LoadInserisciComunicazioneRimediRisarcitori.jsp (2 matches) 
 
 
LoadInserisciOSRimediRisarcitori.jsp (2 matches) 
 
 misuraalternativa 
 
 
LoadInserisciAmmissioneADetDom.jsp (2 matches) 
 
 
LoadInserisciCessazioneMA.jsp (2 matches) 
 
 
LoadInserisciCessazioneMAAffProva.jsp (2 matches) 
 
 
LoadInserisciConcessione.jsp (2 matches) 
 
 
LoadInserisciMAAmmDetDomSpeAff.jsp (2 matches) 
 
 
LoadInserisciMAAmmisioneProvvisoria.jsp (2 matches) 
 
 
LoadInserisciMACessazione51bis.jsp (2 matches) 
 
 
LoadInserisciMACoLibCond.jsp (2 matches) 
 
 
LoadInserisciMADetDomSpecAmmiPeriodo.jsp (2 matches) 
 
 
LoadInserisciMADetDomSpecSospProvv.jsp (2 matches) 
 
 
LoadInserisciMADetDomTemp.jsp (2 matches) 
 
 
LoadInserisciMADicEffAffInProva.jsp (2 matches) 
 
 
LoadInserisciMAProrogaUltPeriodo.jsp (2 matches) 
 
 
LoadInserisciMAProsecuzione.jsp (2 matches) 
 
 
LoadInserisciMAProsecuzione51bis.jsp (2 matches) 
 
 
LoadInserisciMAReLibCond.jsp (2 matches) 
 
 
LoadInserisciRevocaMA.jsp (2 matches) 
 
 
LoadInserisciRevocaMAAffProva.jsp (2 matches) 
 
 
LoadInserisciRigetto.jsp (2 matches) 
 
 
LoadInserisciRipristinoDetDonSpec.jsp (2 matches) 
 
 
LoadInserisciUlteriorePeriodoMA.jsp (2 matches) 
 
 
LoadInsRevocaArrestiDomiciliari.jsp (2 matches) 
 
 
LoadVariazioneMADecSca.jsp (2 matches) 
 
 misurasicurezza 
 
 
LoadInserisciArchiviazioneManuale.jsp (2 matches) 
 
 
LoadInserisciArchiviazionePerProvvAltroUfficio.jsp (2 matches) 
 
 
LoadInserisciArchiviazionePerProvvGEsecuzione.jsp (2 matches) 
 
 
LoadInserisciArchiviazionePerProvvGiudiceCassazione.jsp (2 matches) 
 
 
LoadInserisciArchiviazionePerProvvSorveglianza.jsp (2 matches) 
 
 
LoadInserisciComunicazionePolizia.jsp (2 matches) 
 
 
LoadInserisciOEInternamento.jsp (2 matches) 
 
 
LoadInserisciOLDifferimento.jsp (2 matches) 
 
 
LoadInserisciOLDifferimentoDecreto.jsp (2 matches) 
 
 
LoadInserisciOrdinediConsegna.jsp (2 matches) 
 
 
LoadInserisciOrdineLiberazione.jsp (2 matches) 
 
 
LoadModificaArchiviazioneManualeMS.jsp (3 matches) 
 
 
LoadModificaArchiviazionePerProvvAltroUfficioMS.jsp (3 matches) 
 
 
LoadModificaArchiviazionePerProvvGEsecuzioneMS.jsp (3 matches) 
 
 
LoadModificaArchiviazionePerProvvGiudiceCassazione.jsp (3 matches) 
 
 
LoadModificaArchiviazionePerProvvSorveglianzaMS.jsp (3 matches) 
 
 
LoadModificaComunicazioneOrdineConsegnaMS.jsp (3 matches) 
 
 
LoadModificaOEInternamentoOrdineLiberazioneMS.jsp (3 matches) 
 
 
LoadModificaOLDifferimento.jsp (3 matches)

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 25/81 
 
 
 
LoadModificaOLDifferimentoDecreto.jsp (3 matches) 
 
 ordineesecuzione 
 
 
LoadInserisciComunicazioneL78del2013.jsp (2 matches) 
 
 
LoadInserisciDecretoSospensioneAlfanoLibero.jsp (2 matches) 
 
 
LoadInserisciOERidetPenaAltro.jsp (2 matches) 
 
 
LoadInserisciOrdineEsecuzione.jsp (2 matches) 
 
 
LoadInserisciOrdineEsecuzioneAlfanoLibero.jsp (2 matches) 
 
 
LoadInserisciOrdineEsecuzioneAlfanoNonLibero.jsp (2 matches) 
 
 
LoadInserisciOrdineEsecuzioneL78del2013.jsp (2 matches) 
 
 
LoadInserisciOrdineEsecuzioneSanSos.jsp (2 matches) 
 
 
LoadInserisciOrdineEsecuzioneSimeone.jsp (2 matches) 
 
 
LoadInserisciOrdineEsecuzioneSimeoneSanSos.jsp (2 matches) 
 
 
LoadInserisciRevocaSospensioneAlfano.jsp (2 matches) 
 
 
LoadInserisciRevocaSospensioneSimeone.jsp (2 matches) 
 
 
LoadInserisciVariazioneDecorrenzaScadenza.jsp (2 matches) 
 
 
LoadInserisciVariazioneDecorrenzaScadenzaQC.jsp (2 matches) 
 
 ordinescarcerazione 
 
 
LoadInserisciOSLiberazioneAnticipata.jsp (2 matches) 
 
 revoca 
 
 
LoadInserisciOrdineEsecuzioneRevoca.jsp (2 matches) 
 
 sanzionesostitutiva 
 
 
LoadInserisciAnnotazione.jsp (2 matches) 
 
 
LoadInserisciRideterminazionePenaRevocaSS.jsp (2 matches) 
 
 sospensione 
 
 
LoadInserisciAccoglimentoOpEspulsione.jsp (2 matches) 
 
 
LoadInserisciComunicazioneEspulsione.jsp (2 matches) 
 
 
LoadInserisciDecretoSospensione.jsp (2 matches) 
 
 
LoadInserisciDifferimentoOE.jsp (2 matches) 
 
 
LoadInserisciEspulsioneConcessione.jsp (2 matches) 
 
 
LoadInserisciNotificheDifferimento.jsp (2 matches) 
 
 
LoadInserisciNotificheEspulsione.jsp (2 matches) 
 
 
LoadInserisciRigettoOpEspulsione.jsp (2 matches) 
 
 
LoadInserisciRinunciaOpEspulsione.jsp (2 matches) 
 
 
LoadInserisciSospensioneEsecPenaDispPm.jsp (2 matches) 
 
 
LoadInserisciSospensioneOE.jsp (2 matches) 
 
 
LoadInserisciSospensionePena.jsp (2 matches) 
sige 
 
 impugnazione 
 
 
LoadInserisciEsitoImpugnazioneSige.jsp (2 matches) 
 
 provvedimento 
 
 
InserisciAvvocati.jsp (2 matches) 
 
 
InserisciNotificaSoggettoPressoDifensore.jsp 
 
 
LoadEmissioneOrdinanzaSospensione.jsp (2 matches) 
 
 
LoadInserisciDataDeposito.jsp (2 matches) 
 
 provvInterlocutori 
 
 
LoadInserisciCitazioneTesti.jsp (2 matches) 
 
 
LoadInserisciNominaPeriti.jsp (2 matches) 
 
 udienza 
 
 
LoadInserisciFissazioneUdienza.jsp (2 matches) 
sius 
 
 depositodecreto 
 
 
InserisciAvvocati.jsp (2 matches)

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 26/81 
 
 
 depositoordinanzapc 
 
 
LoadInserisciRimessioneAtti.jsp (2 matches) 
 
 depositosentenza 
 
 
LoadInserisciRimessioneAtti.jsp (2 matches) 
 
 
ModificaRimessioneAtti.jsp (2 matches) 
 
 udienza 
 
 
LoadInserisciFissazioneUdienza.jsp (2 matches) 
 
Modifica di tutti i seguenti metodi per inibire l’accoglimento tra le sedi del foro dei comuni con FLAG_VALIDITA 
a ‘N’ (es. NAPOLI NORD): 
 
 
sico 
 
 libertaanticipata > action 
 
 
ActInserisciComunicazioneLAErgastolo.java 
 
 
ActInserisciComunicazioneLALibero.java 
 
 
ActInserisciComunicazioneReclamoRimediRisarcitori.java 
 
 
ActInserisciComunicazioneRimediRisarcitori.java 
 
 
ActInserisciOSRimediRisarcitori.java 
 
siep 
 
 ordineesecuzione > action 
ActOrdineEsecuzione.java 
(metodi 
setNotificheOrdineEsecuzione(), 
setNotificheL78del2013(), 
setNotificheVariazioneDecorrenzaScadenza()) x tutte le jsp per "ordineesecuzione" 
ActInserisciVariazioneDecorrenzaScadenzaQC.java 
(metodo 
setNotificheVariazioneDecorrenzaScadenzaQC()) 
 
 calcolopena > action 
 
 
ActInsComNuovoResPenaRidetPenaAltro.java 
 
 
ActCalcoloPena.java (metodo setNotificheAnnotazioniManuali()) 
 
 
ActInserisciOSRidetPenaAltro.java (metodo setNotifiche()) 
 
 
ActInserisciOSRidetPenaRidimLA.java (metodo setNotifiche()) 
 
 
ActRidetPena.java (metodo setNotificheMisuraAlternativa()) 
 
 cumulo > action 
 
 
ActCumulo.java (metodo setNotificheCumuloStampa(...)) 
 
 misuraalternativa > action 
ActMisuraAlternativa.java 
(metodi 
setNotificheMisuraAlternativa(), 
setNotificheRevocaArrestiDomiciliariMisuraAlternativa()) x tutte le jsp per "misuraalternativa" 
 
 
ActVariazioneMADecSca.java 
 
 misurasicurezza > action 
 
 
ActInserisciArchiviazioneManuale.java 
 
 
ActInserisciArchiviazionePerProvvSorveglianza.java 
 
 
ActInserisciArchiviazionePerProvvAltroUfficio.java 
 
 
ActInserisciArchiviazionePerProvvGEsecuzione.java 
 
 
ActInserisciArchiviazionePerProvvGiudiceCassazione.java 
 
 
ActInserisciArchiviazionePerProvvSorveglianza.java 
 
 
ActInserisciComunicazionePolizia.java 
 
 
ActInserisciOEInternamento.java 
 
 
ActInserisciOLDifferimento.java 
 
 
ActInserisciOLDifferimentoDecreto.java 
 
 
ActInserisciOrdinediConsegna.java 
 
 
ActInserisciOrdineLiberazione.java 
 
 
ActNotificheMS.java (metodo setNotificheMS(...)) x tutte le jsp di modifica per "misurasicurezza" 
 
 ordinescarcerazione > action

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 27/81 
 
 
 
ActInserisciOSLiberazioneAnticipata.java 
 
 revoca > action 
 
 
ActInserisciOrdineEsecuzioneRevoca.java (metodo setNotifiche(...)) 
 
 sanzionesostitutiva > action 
 
 
ActInserisciRideterminazionePenaRevocaSS.java 
 
 sospensione > action 
 
 
ActInserisciDecretoSospensione.java 
 
 
ActInserisciDifferimentoOE.java (metodo setNotifiche()) 
 
 
ActInserisciNotificheDifferimento.java 
 
 
ActInserisciNotificheEspulsione.java 
 
 
ActInserisciSospensioneEsecPenaDispPm.java 
 
 
ActInserisciSospensioneOE.java 
 
 
ActInserisciSospensionePena.java 
 
sige 
 
 provvedimento > action 
 
 
ActInserisciDataDepositoProvvedimento.java (metodo leggiNotificheAvvocatiAltroDestinatario(...)) 
 
 
ActInserisciOrdinanzaSospensione.java (metodo creaListaDestinatariNotifiche(...)) 
 
6.1.2 Architettura  
N.A. 
6.1.3 Interfacce utente 
Poiché le form interessate alla modifica descritta al punto 6.1.1 sono numerose, di seguito si riporta come 
esempio una form per ciascun sottosistema, il sistema a differenza di quanto avviene adesso, che valorizza il 
comune con il nome del foro, valorizzerà il comune in base al codice Istat presente nella colonna 
RV_ALT2_VALUE del record della tabella CG_REF_CODES con RV_DOMAIN = ‘FORO_AVVOCATI’.  
 
- 
SIEP

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 28/81 
 
 
Figura 11: Sezione destinatario Notifica - SIEP 
 
 
 
- 
SIUS

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 29/81 
 
 
Figura 12: Sezione destinatario Notifica - SIUS 
 
 
- 
SIGE

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 30/81 
 
 
Figura 13: Sezione destinatario Notifica - SIGE 
 
6.1.4 Basi dati 
6.1.4.1 
Selezione Lista Fori SIES 
Per svincolare la descrizione del Foro di appartenenza di un avvocato (es: NAPOLI NORD) dal comune sede del 
circondario competente (es: AVERSA), nella tabella CG_REF_CODES in corrispondenza del dominio 
‘FORO_AVVOCATI' sarà prevista la valorizzazione della colonna ‘RV_ALT2_VALUE’ che conterrà il codice Istat

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 31/81 
 
della sede (comune) di riferimento del foro (es: 061005). La valorizzazione sarà effettuate su tutti i records del 
suddetto dominio. 
La lista dei fori sarà recuperata dalla tabella CG_REF_CODES in corrispondenza del dominio ‘FORO_AVVOCATI'. 
 
Per la valorizzazione della colonna RV_ALT2_VALUE per tutti i records della CG_REF_CODES con RV_DOMAIN 
= ‘FORO_AVVOCATI’ e riferiti a sedi giudiziarie non soppresse sarà realizzato ed eseguito uno specifico script 
(valorizza_codcomune_FORO_AVVOCATI.sql), che per ciascun record della tabella CG_REF_CODES avente 
RV_DOMAIN = ‘FORO_AVVOCATI’, recupererà nella tabella COMUNE il COD_COMUNE per il record avente 
DESCRIZIONE = RV_LOW_VALUE del record corrente della CG_REF_CODES e per lo stesso valorizzerà la colonna 
RV_ALT2_VALUE = COD_COMUNE. 
 
Si fa presente che, a seguito dell’analisi dei dati dell’ultima tabella Avvocati estratta da ReGIndE 
(tabellefisse18novembre2020.xlsx), inviata dall’Amministrazione – Area Civile, i codici comune (codice Istat), 
utilizzati in ReGIndE per la costruzione del COA, sono tutti presenti e corrispondenti a quelli della tabella 
COMUNE di SIES. 
Tali valori, pertanto, saranno utilizzati per valorizzare il Codice Istat del Comune sede del Foro 
(RV_ALT2_VALUE) nel Dominio FORO_AVVOCATI della CG_REF_CODES di SIES. 
 
Per 
l’inserimento 
del 
nuovo 
foro 
di 
Napoli 
Nord 
sarà 
eseguito 
uno 
script 
del 
tipo 
inserisci_FORO_NAPOLI_NORD.sql, che inserirà un nuovo record nella tabella CG_REF_CODES per il dominio 
FORO_AVVOCATI, valorizzando tutte le colonne del record con i valori necessari. 
 
Per la rettifica del nome degli attuali fori di FORLI’, MASSA, REGGIO DI CALABRIA e REGGIO NELL’EMILIA   
rispettivamente in FORLI’ – CESENA, MASSA – CARRARA, REGGIO CALABRIA e REGGIO EMILIA   sarà eseguito 
uno script di aggiornamento della colonna RV_MEANING nella tabella CG_REF_CODES per il dominio 
FORO_AVVOCATI, per ciascuno dei suddetti records. 
 
6.1.4.2 
Tabella Avvocati SIES 
Per il requisito in oggetto la tabella ‘AVVOCATO’ del SIES avrà un ulteriore attributo: FLAG_REGINDE, che 
consentirà di distinguere i dati delle anagrafiche degli avvocati importati da ReGIndE da quelli inseriti 
manualmente su SIES. 
 
I possibili valori saranno: 
✓ “SI” → Inserito da ReGIndE; 
✓ “NO” → Inserito su SIES. 
 
6.1.5 WEB services 
N.A. 
6.1.6 XSD 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 32/81 
 
6.1.7 Configurazione 
N.A. 
6.1.8 Tutorial 
N.A. 
 
6.2 REQ- SIE-021-02_FN.01 -  Ricerca su ReGIndE 
 
Il requisito prevede l’implementazione della nuova funzione “Seleziona da ReGIndE”, che consenta in fase di 
inserimento/assegnazione dell’avvocato, di ricercarlo sulla Base Dati di ReGIndE. 
La funzione in oggetto sarà attivata sui tre sottosistemi del SIES, in tutte le form che consentono la ricerca 
dell’avvocato e la sua associazione ad un procedimento. 
 
Tale funzione, secondo specifica richiesta dell’Amministrazione, sarà la prima opzione di ricerca disponibile per 
l’utente che debba procedere all’eventuale inserimento di un nuovo avvocato e/o all’associazione di un 
avvocato ad un procedimento. 
Pertanto, la funzione di ricerca attualmente presente sul SIES, che va a consultare la tabella proprietaria degli 
avvocati, sarà attivata in alternativa alla ricerca di nuova realizzazione, solo e soltanto nel caso di indisponibilità 
del sistema ReGIndE o nel caso di avvocato non trovato su ReGIndE [Rif. § “6.3 REQ-SIE-021-03_FN.01 - 
Inserimento Manuale: Indisponibilità ReGIndE o Avvocato Non Presente”). 
 
Di seguito sono riportate, per ciascun sottosistema di SIES, le funzionalità che saranno oggetto di modifica per 
l’inserimento della Ricerca dell’Avvocato su ReGIndE: 
 
• 
SIEP 
- 
Assegnazioni → Difensore; 
- 
Assegnazione Difensore (funzione presente nella Form Dettaglio Procedimento SIEP); 
- 
Elenco Difensori → Sostituzione (funzione presente nella Form Dettaglio Procedimento SIEP); 
- 
Nuova Istanza → Iscrizione da Soggetto, Iscrizione da Titolo Esecutivo, Iscrizione da Procedimento SIEP 
• 
SIUS 
- 
Assegnazione Difensore (funzione presente nella Form Dettaglio Procedimento SIUS); 
- 
Elenco Difensori → Sostituzione (funzione presente nella Form Dettaglio Procedimento SIUS); 
- 
Udienza → Fissazione Udienza (nella Form è presente il link “Inserimento Difensore”); 
- 
Ordinanze → Emissione Ordinanza (nella Form è presente il link “Inserimento Difensore”); 
- 
Decreti → Emissione Decreti (nella Form è presente il link “Inserimento Difensore”); 
• 
SIGE 
- 
Assegnazione Difensore (funzione presente nella Form dettaglio procedimento SIGE); 
- 
Ordinanze/Deposito/Notifiche (per tutte le voci dei sottomenu); 
- 
Nomina Periti/Citazioni Testi (per tutte le voci dei sottomenu); 
- 
Udienze/Fissazione/Rinvio/Ruolo (per tutte le voci dei sottomenu); 
- 
Decreti/Deposito/Notifiche (per tutte le voci dei sottomenu). 
 
6.2.1 Moduli sw  
Di seguito l’elenco delle jsp da modificare, suddivise per sottosistema:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 33/81 
 
 
siep 
 
avvocato 
 
 
DettaglioAvvocato.jsp 
 
 
DettaglioAvvocatoAvvocatoFascicoloSiep.jsp 
 
 
DettaglioAvvocatoSentenza.jsp 
 
 
 
InserimentoAssegnazioneDifensore.jsp 
 
 
LoadInserisciAvvocato.jsp 
 
 
SostituzioneDifensore.jsp  
 
 
FiltraListaAvvocatiPopup.jsp 
 
 
ListaAvvocatoPopup.jsp 
 
 
fascicolo 
 
 
DettaglioFascicoloSiep.jsp 
 
sige 
 
avvocato 
 
 
DettaglioAvvocatoFascicoloSige.jsp 
 
 
 
DettaglioAvvocatoSentenza.jsp 
 
 
InserimentoAssegnazioneDifensore.jsp 
 
 
LoadInserisciAvvocato.jsp 
 
 
SostituzioneDifensore.jsp  
 
sius 
 
avvocato 
 
 
DettaglioAvvocatoAvvocatoFascicoloSius.jsp 
 
 
 
DettaglioAvvocatoSentenza.jsp 
 
 
LoadRicercaAvvocatoSiep.jsp 
 
 
LoadInserisciAvvocato.jsp 
 
 
SostituzioneDifensore.jsp  
 
 
 
Di seguito l’elenco delle action.java da modificare, suddivise per sottosistema: 
 
 
siep 
 
 avvocato > action 
ActDettaglioAvvocato.java 
ActInserisciAvvocato.java 
ActLoadDettaglioAvvocato.java 
ActLoadDettaglioAvvocatoFascicolo.java 
ActLoadInserisciAssegnaAvvocato.java 
ActLoadInserisciAvvocato.java 
ActLoadSostituzioneDifensore.java 
ActSostituzioneDifensore.java 
 
 nuovaistanza > action 
ActLoadInserisciIstanzaPerProcedimentoSiep.java 
ActLoadInserisciIstanzaPerSoggetto.java 
ActLoadInserisciIstanzaPerTitoloEsecutivo.java 
 
 
 sige 
 
 avvocato > action 
ActLoadDettaglioAvvocatoFascicoloSige.java

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 34/81 
 
ActInserisciAvvocato.java 
ActLoadInserisciAvvocato.java 
ActLoadSostituzioneDifensore.java 
ActSostituzioneDifensore.java 
udienza > action 
ActLoadInserisciFissazioneUdienza.java 
 udienzaprocedimento > action 
ActLoadInserisciOrdinanzaRinvioUdienza.java 
ActLoadInserisciVerbaleRinvioUdienza.java 
 udienzaparti > action 
ActLoadInserisciAvvocato.java 
ActLoadSostituzioneDifensore.java 
 
 
sius 
 
 avvocato > action 
ActLoadDettaglioAvvocatoFascicolo.java 
ActInserisciAvvocato.java 
ActLoadInserisciAvvocato.java 
ActLoadSostituzioneDifensore.java 
ActSostituzioneDifensore.java 
 
Saranno realizzati nuovi moduli software per la ricerca dell’Avvocato su ReGIndE. 
 
 
6.2.2 Architettura  
N.A. 
6.2.3 Interfacce utente 
Per l’inserimento della nuova ricerca dell’avvocato su ReGIndE, attraverso l’utilizzo di un Web Services, saranno 
modificate e realizzate le seguenti interfacce: 
 
6.2.3.1 
Sottosistema SIEP 
 
L’attuale funzione di Assegnazione/Inserimento Difensore SIEP

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 35/81 
 
 
Figura 11: Form inserimento difensore procedimento SIEP- attuale 
 
sarà modificata come di seguito riportato:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 36/81 
 
 
Figura 14: Form inserimento difensore procedimento SIEP - nuova 
 
Nello specifico, si procederà con la sostituzione dell’attuale link 
, che permette di 
selezionare l’avvocato fra quelli già presenti in SIES, con il nuovo link 
, che 
permetterà di ricercare l’avvocato nella base dati di ReGIndE. 
Inoltre sulla form dei dati avvocato, sarà prevista l’aggiunta del nuovo campo PEC, dato che risulta essere 
presente in ReGIndE. 
 
Al click di tale link il sistema proporrà la nuova form di ricerca su ReGIndE, descritta di seguito.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 37/81 
 
 
Figura 15: Form di attivazione ricerca su ReGIndE 
 
La funzione permetterà, utilizzando un apposito Web Service di interazione con ReGIndE, la ricerca 
dell’avvocato sul Registro Generale degli Indirizzi Elettronici. La form presenta i campi per la ricerca per 
Cognome e Nome dell’avvocato, Foro di appartenenza e un check-box per ‘estendere’ la ricerca a tutti i Fori. 
I campi obbligatori per la ricerca saranno: Cognome e Foro, o in alternativa, Cognome e check-box ‘Tutti i Fori’. 
In particolare, il Foro sarà selezionabile da una listbox, i cui valori corrisponderanno a quelli presenti nella 
tabella contenente l’elenco dei Fori, utilizzata nel sistema SIES, che sarà resa conforme a quello di ReGIndE. A 
seguito della selezione del tasto Cerca su ReGIndE il sistema innescherà su ReGIndE una ricerca puntuale degli 
Avvocati aventi Cognome, eventualmente il Nome uguali a quelli digitati e appartenenti al foro selezionato o 
a tutti i fori. 
 
I risultati saranno filtrati secondo il codice Ente di ReGIndE (Foro Avvocati), costituito dalla concatenazione 
della stringa COA e dal codice Istat del Comune sede dello stesso, per questo motivo detto anche 
semplicemente COA. 
 
Sarà inoltre possibile effettuare la ricerca sul cognome anche per like, valorizzando i primi 3 caratteri del 
cognome seguiti dal carattere %. In questo caso il sistema ricercherà tutti gli avvocati aventi il cognome con i 
primi 3 caratteri corrispondenti a quelli digitati. 
 
A proposito della ricerca in like va osservato quanto segue: L'utente dovrebbe conoscere sempre nome e 
cognome dell'avvocato, è presente sull'atto. Il problema che rende necessaria la ricerca in like è legato alla 
possibilità che il cognome/nome possano essere inseriti nel sistema REGINDE con delle varianti legate alle 
accentate, agli apostrofi o ai nome con dieresi (tedeschi), in genere a tutte le lettere speciali degli alfabeti 
stranieri. Le regole di traslitterazione non sono note all'utente (sempre che esistano) per cui la ricerca puntuale 
potrebbe non restituire risultati. In questo caso sull'atto l'avvocato potrebbe essere indicato con il cognome 
Rodotà mentre su Reginde è caricato come Rodota' Oppure Ferdinand Piüch potrebbe essere caricato come 
Ferdinand Piuech. 
 
Il sistema SIES, all’avvenuta conferma da parte dell’utente dei criteri digitati, attiverà la ricerca su ReGIndE, 
utilizzando per l’interfaccia i servizi web esposti dall’applicazione ReGIndE, costruendo il client ed altre 
apposite classi java che permetteranno di effettuare la ricerca vera e propria e di gestire i risultati ottenuti.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 38/81 
 
Nei casi di indisponibilità del sistema ReGIndE e/o di dati non trovati su ReGIndE, il sistema restituirà, per 
ciascuno dei casi indicati, un opportuno messaggio di alert e attiverà la funzione di ricerca del difensore su SIES 
[Rif. § “6.3 REQ-SIE-021-03-FN.01 - Inserimento Manuale: Indisponibilità ReGIndE o Avvocato Non Presente”]. 
 
E’ possibile che il servizio di interrogazione/ricerca del soggetto su ReGIndE, soprattutto in caso di ricerca per 
like, possa restituire un messaggio di ‘SearchLimitException’, ossia che in fase di ricerca sia stato individuato 
un numero di soggetti superiore ad un dato limite. In tal caso sarà mostrato un messaggio che invita l’utente 
a restringere i criteri di ricerca e la form presenta un nuovo campo di ricerca per Codice Fiscale. 
 
 
 
Figura 16: Form di ricerca su ReGIndE con segnalazione di eccessive occorrenze con criteri impostati  
 
In questo caso l’utente potrà rieseguire la ricerca aumentando i caratteri della stringa che precede il carattere 
%, valorizzando il nome oppure limitarsi a valorizzare solo il codice fiscale, in quanto anche in presenza della 
valorizzazione degli altri campi della form, il sistema ricercherà tutti gli avvocati con il codice fiscale indicato in 
tutti i fori, non considerando il contenuto degli altri campi.  
 
Nel caso, invece, di disponibilità del sistema ReGIndE e di dati trovati su ReGIndE, questi ultimi, dopo essere 
stati opportunamente recuperati, saranno convogliati in una nuova Form di elenco avvocati estratti da 
ReGIndE, sempre tramite l’utilizzo dello specifico Web Service 
 
 
Figura 17: Form Elenco Avvocati ReGIndE

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 39/81 
 
 
 
Nella  Form di Elenco saranno visualizzati i dati del singolo o di ogni avvocato trovato soddisfacente i 
parametri di ricerca digitati precedentemente. 
I dati che saranno visualizzati per ciascuno saranno: Cognome, Nome Codice Fiscale, Foro di appartenenza, 
Luogo e Data Nascita, Indirizzo, Stato (attivo, radiato, sospeso, cessato). In riferimento allo Stato dell’avvocato, 
dato molto utile per l’utente SIES, si sottolinea che al momento questo dato è presente e visibile su ReGIndE, 
ma che potrebbe essere in futuro oscurato nel risultato delle ricerche. In caso che si verificasse questa ultima 
evenienza è essenziale che gli amministratori di ReGIndE avvisino per tempo i Referenti SIES per la valutazione 
di possibili correttivi. 
 
Inoltre, sempre in merito ai dati che saranno visualizzati in elenco, ed alla loro gestione, occorre tener conto 
di tali osservazioni: 
 
- 
Nel caso che la Ricerca su ReGInde, in corrispondenza della colonna indirizzo, dovesse fornire più 
record con tipologia a ‘D’, il sistema SIES, recepirà il primo ottenuto ordinando alfabeticamente la 
colonna Indirizzo. 
 
- 
Poiché in ReGIndE il LUOGO_NASCITA e il COMUNE di RESIDENZA dello studio sono importati, in forma 
descrittiva, così come inseriti dagli Ordini Forensi, senza alcun controllo sulla corrispondenza della 
Descrizione rispetto alle Denominazioni ufficialmente riconosciute dei Comuni, può verificarsi che 
siano riportate descrizioni non corrispondenti a quelle legalmente riconosciute ( ad es. come luogo di 
nascita sono riportati: CASERTA  -S. BARBARA-, S.MARIA C.V., ERICE C.S., RIVAROLO C.SE,…). 
 
- 
Al momento nella tabella AVVOCATO di SIES i due dati vengono valorizzati con il codice Istat del 
Comune, dopo essere stati sottoposti al controllo dell’esistenza della Descrizione inserita nelle form 
rispetto 
a 
quella 
presente 
nella 
tabella 
COMUNE, 
quindi 
il 
sistema, 
in 
fase 
di 
inserimento/aggiornamento non li accetterebbe. Per bypassare questo problema nella tabella 
AVVOCATO di SIES sarà mantenuta la codifica del luogo di nascita, ricavandolo dal codice Belfiore (dal 
quintultimo al penultimo carattere) del Codice Fiscale, sempre presente in ReGIndE, mentre per il 
luogo residenza sarà aggiunta una nuova colonna che conterrà la descrizione del Comune sede dello 
studio 
come 
presente 
in 
ReGIndE, 
abbandonando 
la 
valorizzazione 
della 
colonna 
COD_COMUNE_RESIDENZA, che resterà per i dati pregressi; 
 
- 
Per poter risalire dal codice Belfiore al codice Istat del Comune, nella tabella COMUNE di SIES sarà 
aggiunto una nuova colonna di 4 caratteri alfanumerici, che sarà valorizzata con apposita procedura 
PLSQL con il codice catastale corrispondente, recuperandolo dalla tabella Comune della DGSIA. A tal 
fine bisognerà procedere preventivamente all’aggiornamento delle tabelle di SIES, COMUNE e 
CG_REF_CODES, relativamente ai domini Provincia, Regione e Nazione, allineandole alle tabelle fisse 
COMUNE, PROVINCIA, REGIONE e STATO-NAZIONE della DGSIA. Le attività previste per tale 
aggiornamento sono descritte dettagliatamente di seguito al par. 6.6.;

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 40/81 
 
- 
In caso di assenza del codice Belfiore nella tabella COMUNE di SIES, l’avvocato non sarà importato, ma, 
sulla pagina web, sarà inviato specifico messaggio di avviso all’utente della NON PRESENZA del Comune 
in SIES, con indicazione di segnalarne urgentemente l’assenza al gruppo Tabelle Fisse 
dell’Amministrazione. Il sistema consentirà comunque di inserire l’avvocato in SIES privo della 
certificazione ReGIndE, in modalità manuale (vedi par. 6.3.3.2). 
 
A seguito delle suddette modifiche alla base dati, saranno rivisti tutti i moduli SIES, che al momento recuperano 
la descrizione del comune sede dello studio, attraverso la decodifica del codice ISTAT. 
  
Dalla pagina di elenco, selezionando l’icona del +, presente accanto al nominativo del difensore, sarà possibile 
visualizzare gli ulteriori dati dell’avvocato (pec, telefono, fax, email), al di sotto di quelli già riportati nella form.  
 
Dalla Form di elenco, l’utente potrà selezionare l’avvocato di interesse ed il sistema lo riporterà sulla Form 
precedente (la chiamante, cioè la Form da cui è stata attivata la funzione di ricerca su ReGIndE) in cui saranno 
riportati negli specifici campi della form tutti i dati dell’avvocato selezionato.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 41/81 
 
 
Figura 18: Form dettaglio Avvocato selezionato 
 
All’atto della conferma dell’associazione dell’avvocato al fascicolo SIEP in lavorazione, per l’avvocato 
selezionato dall’elenco, il sistema verificherà la presenza nella tabella ‘AVVOCATO’ del SIES, limitatamente  
ai record presenti in tabella aventi il FLAG_REGINDE = ’SI’. 
 
I criteri utilizzati per tale verifica saranno: 
• 
COGNOME 
• 
NOME 
• 
CODICE FISCALE 
• 
FORO di appartenenza. 
Per nessun dato trovato, i criteri saranno ridotti a: 
• 
COGNOME 
• 
NOME 
• 
FORO di appartenenza.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 42/81 
 
Il sistema, in base all’esito di tale verifica, eseguirà le seguenti operazioni: 
• 
Esito Verifica: Avvocato individuato univocamente nella tabella ‘AVVOCATO’ del SIES: 
il sistema aggiornerà i dati del record trovato [Rif. § “6.1.4.2 Tabella Avvocati SIES”] con i dati recuperati 
da ReGIndE relativamente alla PEC, all’Indirizzo, al Numero di telefono e allo Stato dell’avvocato (ad es. 
attivo o cancellato) ed assocerà l’identificativo dell’avvocato al fascicolo SIES in lavorazione. 
Nel caso in cui la Ricerca su ReGInde, in corrispondenza del tag indirizzo, dovesse fornire più record con 
tipologia a ‘D’, sarà selezionato il primo ottenuto ordinando alfabeticamente la colonna Indirizzo. 
 
Si evidenzia che a seguito dell’aggiornamento dell’indirizzo, potrebbe verificarsi che su un procedimento 
ancora in corso con provvedimenti/atti riferiti all’ indirizzo dell’avvocato precedente all’aggiornamento, 
rieseguiti/ristampati riporterebbero i dati del nuovo indirizzo. In ogni caso la sovrascrittura del vecchio 
indirizzo non costituisce un problema per SIES, anche in caso di indirizzo non valorizzato su ReGIndE. 
• 
Esito Verifica: Avvocato NON trovato nella tabella ‘AVVOCATO’ del SIES: 
il sistema effettuerà l’inserimento nella tabella ‘AVVOCATO’ del SIES utilizzando i dati recuperati da 
ReGIndE e, l’identificativo del nuovo avvocato inserito, sarà associato al fascicolo SIES in lavorazione. 
Nell’inserimento del record sulla tabella del SIES sarà impostato il nuovo campo FLAG_REGINDE con il 
valore ‘Sì’ [Rif. § “6.1.4.2 Tabella Avvocati SIES”]. 
 
È necessario specificare che tutte le ricerche di un avvocato su SIES avverranno per FLAG_REGINDE = ‘SI’. 
Di conseguenza, non si incorrerà nella casistica di risultati multipli della ricerca SIES. 
 
A seguito dell’acquisizione del dato relativo alla PEC, anche la form attuale di Dettaglio Avvocato del 
procedimento SIEP sarà modificata così come riportato nella figura che segue:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 43/81 
 
 
Figura 19: Form dettaglio avvocato procedimento SIEP 
 
Anche la funzione ‘Sostituzione Difensore’ SIEP sarà modificata alla stessa maniera descritta per la funzione 
Assegnazione Difensore con l’inserimento nella form del Link 
 e del campo Pec.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 44/81 
 
 
Figura 20: Form sostituzione Difensore procedimento SIEP 
 
Il funzionamento sarà esattamente uguale a quello descritto per funzione ‘Assegnazione Difensore’. 
 
L’attuale funzione di Iscrizione Istanza da Soggetto andrà rivista per sostituire l’attuale popup di selezione 
Avvocato da SIES con quella di selezione da ReGIndE, descritta in precedenza,

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 45/81 
 
 
Figura 21: Form Iscrizione Istanza da Soggetto - Attuale

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 46/81 
 
 
in cui, cliccando 
, si presenta la seguente popup 
 
 
Figura 22: popup Ricerca e seleziona Avvocato SIES 
 
che permette di ricercare o inserire il difensore nella tabella Avvocato di SIES. Il link sarà sostituito dalla nuova 
funzionalità 
. 
 
 
Stesso intervento andrà effettuato sulla funzione Iscrizione Istanza da Titolo Esecutivo

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 47/81 
 
 
Figura 23: Form Iscrizione Istanza da Titolo Esecutivo - Attuale 
 
 
e sulla funzione Iscrizione Istanza da Procedimento SIEP

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 48/81 
 
 
Figura 24: Form Iscrizione Istanza da Procedimento SIEP 
 
6.2.3.2 
Sottosistema SIGE 
 
L’attuale funzione di Assegnazione/Inserimento Difensore SIGE

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 49/81 
 
 
Figura 25: Form sostituzione Assegnazione Difensore procedimento SIGE - Attuale 
 
 
 
sarà modificata come di seguito:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 50/81 
 
 
Figura 26: Form sostituzione Assegnazione Difensore procedimento SIGE - Nuova 
 
con l’eliminazione dell’attuale link 
, che permette di selezionare l’avvocato fra quelli 
già presenti in SIES, con il nuovo link 
, che permetterà di ricercare l’avvocato nella 
base dati di ReGIndE, e con l’aggiunta del nuovo campo PEC, dato che risulta essere presente in ReGIndE. 
 
 
Al click del link 
 il sistema proporrà la nuova form di ricerca su ReGIndE, descritta 
già in precedenza per il sottosistema SIEP, con identico funzionamento. 
 
Dopo aver selezionato dall’elenco degli Avvocati quello di interesse e precompilato la form di inserimento, a 
seguito della conferma dell’associazione dell’avvocato al fascicolo SIGE in lavorazione, per l’avvocato 
selezionato dall’elenco, il sistema verificherà la presenza nella tabella ‘AVVOCATO’ del SIES, limitatamente  
ai record presenti in tabella aventi il FLAG_REGINDE = ’SI’.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 51/81 
 
I criteri utilizzati per tale verifica saranno: 
• 
COGNOME 
• 
NOME 
• 
CODICE FISCALE 
• 
FORO di appartenenza. 
Per nessun dato trovato, i criteri saranno ridotti a: 
• 
COGNOME 
• 
NOME 
• 
FORO di appartenenza. 
 
Il sistema, in base all’esito di tale verifica, eseguirà le seguenti operazioni: 
• 
Esito Verifica: Avvocato individuato univocamente nella tabella ‘AVVOCATO’ del SIES: 
il sistema aggiornerà i dati del record trovato con i dati recuperati da ReGIndE relativamente alla PEC, 
all’Indirizzo, al Numero di telefono e allo Stato dell’avvocato (ad es. attivo o cancellato) ed assocerà 
l’identificativo dell’avvocato al fascicolo SIES in lavorazione. Nel caso che la Ricerca su ReGInde, in 
corrispondenza del tag indirizzo, dovesse fornire più record con tipologia a ‘D’, sarà selezionato il primo 
ottenuto ordinando alfabeticamente la colonna Indirizzo. 
• 
Esito Verifica: Avvocato NON trovato nella tabella ‘AVVOCATO’ del SIES: 
il sistema effettuerà l’inserimento nella tabella ‘AVVOCATO’ del SIES utilizzando i dati recuperati da 
ReGIndE e, l’identificativo del nuovo avvocato inserito, sarà associato al fascicolo SIES in lavorazione. 
Nell’inserimento del record sulla tabella del SIES sarà impostato il nuovo campo FLAG_REGINDE con il 
valore ‘SI’- 
 
Si evidenzia che tutte le ricerche di un avvocato su SIES avverranno per FLAG_REGINDE = ‘SI’, pertanto 
non si incorrerà nella casistica di risultati multipli della ricerca SIES. 
 
 
A seguito dell’acquisizione del dato relativo alla PEC, anche l’attuale form di Dettaglio Avvocato del 
procedimento SIGE

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 52/81 
 
 
Figura 27: Form Dettaglio Difensore procedimento SIGE - Attuale 
 
sarà modificata, oltre che per la visualizzazione del nuovo dato PEC, anche con la presentazione di dati presenti 
nella form di Assegnazione ma non presentati in quella di Dettaglio (Luogo nascita, Data Nascita, Comune 
Residenza, pec). Pertanto la nuova form sarà la seguente:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 53/81 
 
 
Figura 28: Form Dettaglio Difensore procedimento SIGE - Nuova 
 
Anche la funzione Sostituzione Difensore SIGE sarà modificata alla stessa maniera descritta per la funzione 
Assegnazione Difensore SIGE con l’inserimento nella form del Link 
 e del campo 
Pec.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 54/81 
 
 
Figura 29: Form Sostituzione Difensore procedimento SIGE - Nuova 
 
Il funzionamento sarà esattamente uguale a quello descritto per funzione ‘Assegnazione Difensore’. 
 
 
Anche la funzione Inserimento Difensore Parte

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 55/81 
 
 
Figura 30: Form Inserimento Difensore procedimento SIGE – Parti in causa 
 
attivabile dal link Gestione Difensore, presente nelle form Inserimento Difensore Parte, raggiungibile dalle 
funzioni Gestioni Parti Civili e Gestione Parti Offese, presenti in Dettaglio Fissazione Udienza, Dettaglio Rinvio 
Udienza con Ordinanza, Dettaglio Rinvio Udienza da Verbale, Dettaglio Nomina Periti e in Dettaglio Ordinanza

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 56/81 
 
 
Figura 31: Form Inserimento Difensore Parte

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 57/81 
 
 
Figura 32: Form Dettaglio Fissazione Udienza procedimento SIGE  
 
sarà modificata

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 58/81 
 
 
Figura 33: Form Inserimento Difensore procedimento SIGE Parti in casusa - Nuova 
 
alla stessa maniera descritta per la funzione Assegnazione Difensore SIGE con l’inserimento nella form del Link 
  e del campo Pec. Il funzionamento sarà esattamente uguale a quello descritto per 
funzione ‘Assegnazione Difensore’. 
 
6.2.3.3 
Sottosistema SIUS 
 
L’attuale funzione di Assegnazione/Inserimento Difensore   SIUS

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 59/81 
 
 
Figura 34: Form Assegnazione Difensore procedimento SIUS - Attuale 
 
sarà modificata come di seguito

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 60/81 
 
 
Figura 35: Form Assegnazione Difensore procedimento SIUS - Nuova 
 
con l’eliminazione dell’attuale link 
, che permette di selezionare l’avvocato fra quelli 
già presenti in SIES, con il nuovo link 
, che permetterà di ricercare l’avvocato nella 
base dati di ReGIndE, e con l’aggiunta del nuovo campo PEC, dato che risulta essere presente in ReGIndE. 
 
Il link 
rimarrà, ma la funzione richiamata sarà rivista in quanto ricercherà fra gli 
avvocati collegati al procedimento SIEP solo quelli importati da ReGIndE, cioè quelli aventi nella tabella 
AVVOCATO di SIES il FLAG_REGINDE = ‘SI’. 
 
Al click del link 
 il sistema proporrà la nuova form di ricerca su ReGIndE, descritta 
già in precedenza per il sottosistema SIEP, con identico funzionamento. 
 
Dopo aver selezionato dall’elenco degli Avvocati quello di interesse e precompilato la form di inserimento, a 
seguito della conferma dell’associazione dell’avvocato al fascicolo SIUS in lavorazione, per l’avvocato 
selezionato dall’elenco, il sistema verificherà la presenza nella tabella ‘AVVOCATO’ del SIES, limitatamente  
ai record presenti in tabella aventi il FLAG_REGINDE = ’SI’.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 61/81 
 
 
I criteri utilizzati per tale verifica saranno: 
• 
COGNOME 
• 
NOME 
• 
CODICE FISCALE 
• 
FORO di appartenenza. 
Per nessun dato trovato, i criteri saranno ridotti a: 
• 
COGNOME 
• 
NOME 
• 
FORO di appartenenza. 
 
Il sistema, in base all’esito di tale verifica, eseguirà le seguenti operazioni: 
• 
Esito Verifica: Avvocato individuato univocamente nella tabella ‘AVVOCATO’ del SIES: 
il sistema aggiornerà i dati del record trovato con i dati recuperati da ReGIndE relativamente alla PEC, 
all’Indirizzo, al Numero di telefono e allo Stato dell’avvocato (ad es. attivo o cancellato) ed assocerà 
l’identificativo dell’avvocato al fascicolo SIES in lavorazione. Nel caso che la Ricerca su ReGInde, in 
corrispondenza del tag indirizzo, dovesse fornire più record con tipologia a ‘D’, sarà selezionato il primo 
ottenuto ordinando alfabeticamente la colonna Indirizzo. 
 
• 
Esito Verifica: Avvocato NON trovato nella tabella ‘AVVOCATO’ del SIES: 
il sistema effettuerà l’inserimento nella tabella ‘AVVOCATO’ del SIES utilizzando i dati recuperati da 
ReGIndE e, l’identificativo del nuovo avvocato inserito, sarà associato al fascicolo SIES in lavorazione. 
Nell’inserimento del record sulla tabella del SIES sarà impostato il nuovo campo FLAG_REGINDE con il 
valore ‘SI’- 
 
Si evidenzia che tutte le ricerche di un avvocato su SIES avverranno per FLAG_REGINDE = ‘SI’, pertanto non si 
incorrerà nella casistica di risultati multipli della ricerca SIES. 
 
A seguito dell’acquisizione del dato relativo alla PEC, anche l’attuale form di Dettaglio Avvocato del 
procedimento SIUS

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 62/81 
 
 
Figura 36: Form Dettaglio Difensore procedimento SIUS - Attuale 
 
sarà modificata, oltre che per la visualizzazione del nuovo dato PEC, anche con la presentazione di dati presenti 
nella form di Assegnazione ma non presentati in quella di Dettaglio (Luogo nascita, Data Nascita, Comune 
Residenza, pec). Pertanto la nuova form sarà la seguente: 
 
 
Figura 37: Form Dettaglio Difensore procedimento SIUS - Nuova

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 63/81 
 
Anche la funzione ‘Sostituzione Difensore’ SIUS sarà modificata alla stessa maniera descritta per la funzione 
Assegnazione Difensore SIUS con l’inserimento nella form del Link 
 e del campo Pec. 
 
 
Figura 38: Form Sostituzione Difensore procedimento SIUS - Nuova 
 
Il link 
rimarrà, ma la funzione richiamata sarà rivista in quanto ricercherà fra gli 
avvocati collegati al procedimento SIEP solo quelli importati da ReGIndE, cioè quelli aventi nella tabella 
AVVOCATO di SIES il FLAG_REGINDE = ‘SI’. 
 
Il funzionamento sarà esattamente uguale a quello descritto per funzione ‘Assegnazione Difensore’. 
 
6.2.4 Basi dati 
La tabella AVVOCATO di SIES sarà modificata con l’aggiunta di tre nuove colonne: PEC, FLAG_REGINDE, 
DESCR_COMUNE_STUDIO. A tal fine sarà preparato uno script del tipo Alter_Table_Avvocato.sql.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 64/81 
 
6.2.5 WEB services 
L’implementazione delle ricerca dell’avvocato su ReGIndE, operativamente, è legata all’invocazione di un 
webservice esposto dal sistema Registro Generale degli Indirizzi Elettronici (ReGIndE). 
 
Nel sistema SIES occorre predisporre un modulo client in java che permetterà di interloquire con gli endpoint 
dei servizi ReGIndE attraverso i quali sarà poi raggiungibile il servizio applicativo per le interrogazioni per 
“Soggetti” (difensori). Nello specifico il sistema SIES si interfaccerà con l’endpoint esposto per ‘chiamate 
interne’ per sistemi su giustizia. 
L’endpoint di interesse è identificato dalla seguente url: 
 
https://XX.XXX.XXXX.XXX/ServiziInterrogazioneRegindeExt/ServiziInterrogazioneInterni 
 
e l’operazione, servizio applicativo a cui fare accesso, è ‘ricercaSoggettoComplete’. 
 
Tale servizio permette una ricerca del soggetto difensore sul sistema Registro Generale degli Indirizzi 
Elettronici secondo i seguenti parametri: 
 
• 
nome 
• 
cognome 
• 
codiceFiscale 
• 
indirizzoPec 
• 
codiceEnte  
 
Nome: indica il nome del difensore di interesse per la ricerca; 
Cognome: indica il cognome del difensore di interesse per la ricerca; 
Codice Fiscale: indica il codice fiscale del difensore di interesse per la ricerca; 
Indirizzo Pec: indica l’indirizzo della PEC del difensore di interesse per la ricerca; 
Codice Ente: indica il codice identificativo dell'ente, quindi l’albo, che ha censito l’avvocato in ReGIndE. Per gli 
avvocati iscritti ad un Consiglio dell'Ordine il codice dell'ente sarà rappresentato da una stringa data dal 
prefisso COA, al quale viene aggiunto il codice Istat del comune di riferimento del consiglio dell’ordine stesso.  
 
 
In riferimento al requisito di ricerca su ReGIndE [REQ-SIE-021-02] la ricerca prevede come campi obbligatori il 
Cognome ed il Foro di appartenenza o in alternativa, Cognome e check-box ‘Tutti i Fori’ che si traduce pertanto 
in un’interrogazione al servizio senza specificare il codiceEnte. 
 
 
Il servizio di ‘ricercaSoggettoComplete’ restituisce una lista di oggetti ‘soggetto’ che analizzando il wsdl è così 
definito: 
 
   <xs:complexType name='soggetto'> 
    <xs:sequence> 
     <xs:element maxOccurs='unbounded' minOccurs='0' name='ruoliente' type='tns:ruoloente'/> 
     <xs:element maxOccurs='unbounded' minOccurs='0' name='indirizzi' type='tns:indirizzo'/> 
     <xs:element minOccurs='0' name='soggetto' type='tns:soggetti'/> 
    </xs:sequence> 
   </xs:complexType>

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 65/81 
 
 
Quindi avremmo, un oggetto di tipo ‘soggetti’ così definito: 
 
<xs:complexType name='soggetti'> 
    <xs:sequence> 
     <xs:element minOccurs='0' name='codFisc' type='xs:string'/> 
     <xs:element minOccurs='0' name='cognome' type='xs:string'/> 
     <xs:element minOccurs='0' name='dataNascita' type='xs:dateTime'/> 
     <xs:element minOccurs='0' name='luogoNascita' type='xs:string'/> 
     <xs:element minOccurs='0' name='nome' type='xs:string'/> 
     <xs:element minOccurs='0' name='pec' type='xs:string'/> 
     <xs:element minOccurs='0' name='provNascita' type='xs:string'/> 
    </xs:sequence> 
   </xs:complexType> 
 
ed una lista di oggetti ‘ruoloente’ e ‘indirizzo’, a sua volta così definiti: 
 
   <xs:complexType name='ruoloente'> 
    <xs:sequence> 
     <xs:element minOccurs='0' name='codiceFiscale' type='xs:string'/> 
     <xs:element minOccurs='0' name='codice' type='xs:string'/> 
     <xs:element minOccurs='0' name='descrizione' type='xs:string'/> 
     <xs:element name='pubblicaAmministrazione' type='xs:boolean'/> 
     <xs:element minOccurs='0' name='pec' type='xs:string'/> 
     <xs:element minOccurs='0' name='partitaIVA' type='xs:string'/> 
     <xs:element minOccurs='0' name='ruolo' type='xs:string'/> 
     <xs:element minOccurs='0' name='stato' type='xs:string'/> 
    </xs:sequence> 
   </xs:complexType> 
 
   <xs:complexType name='indirizzo'> 
    <xs:sequence> 
     <xs:element minOccurs='0' name='cap' type='xs:string'/> 
     <xs:element minOccurs='0' name='comune' type='xs:string'/> 
     <xs:element minOccurs='0' name='email' type='xs:string'/> 
     <xs:element minOccurs='0' name='fax' type='xs:string'/> 
     <xs:element minOccurs='0' name='indirizzo' type='xs:string'/> 
     <xs:element minOccurs='0' name='prov' type='xs:string'/> 
     <xs:element minOccurs='0' name='telefono' type='xs:string'/> 
     <xs:element minOccurs='0' name='tp_indirizzo' type='xs:string'/> 
    </xs:sequence> 
   </xs:complexType> 
 
 
6.2.5.1 
Gestione delle fault 
Dall’analisi del wsdl una possibile eccezione che deve essere gestita è la tipologia di errore denominata 
‘SearchLimitException’ che sarà restituita dal servizio nelle casistiche in cui la ricerca estragga una numerosità 
troppo elevata di occorrenze trovate.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 66/81 
 
A tal proposito si evidenzia che non sarà possibile inibire la ricerca degli avvocati per like, in quanto se l’utente 
SIES non conosce la esatta descrizione dell’avvocato in ReGIndE, deve poter innescare tale tipo di ricerca. 
 
 
6.2.5.2 
Altre specifiche per il servizio 
 
I messaggi SOAP rivolti a questi servizi non prevedono l’inserimento di parametri specifici all’interno 
dell’header SOAP e dell’header http e ad oggi si basano su un protocollo di sicurezza basato su TLS 1.2, al 
momento in fase di collaudo. 
 
Se al momento della messa in esercizio degli interventi previsti in questo documento, su ReGIndE non fosse 
stato ancora rilasciato il protocollo TLS1.2, si provvederà ad effettuare gli opportuni interventi per il 
funzionamento con protocollo di sicurezza TLS1.0. 
 
6.2.6 XSD 
N.A. 
6.2.7 Configurazione 
Per la connessione ai servizi in https sul sistema ReGIndE è da prevedere l’importazione della chiave pubblica 
(certificato ssl) che mappa il DNS del server su cui è esposto il servizio 
 
ES:  https:// reginde /ServiziInterrogazioneRegindeExt/ServiziInterrogazioneInterni 
 
Il certificato deve essere importato nel file keystore del sies (trustore.jks) posizionato al 
/var/SIES/CONFIG/certs. 
 
L’Amministrazione fornirà il certificato di chiave pubblica del RegIndE, e tutta la catena necessaria, utilizzato 
al momento della messa in esercizio degli interventi SIES. 
6.2.8 Tutorial 
N.A. 
 
6.3 REQ- SIE-021-03_FN.01 – Inserimento Manuale: Indisponibilità ReGIndE o Avvocato Non Presente 
Nei casi di indisponibilità del sistema ReGIndE o di assenza dell’avvocato su ReGIndE, il sistema dovrà 
consentire la ricerca del Difensore su SIES. 
Inoltre nel caso di assenza del Difensore anche nella base dati di SIES, il sistema consentirà l’inserimento dello 
stesso in SIES, ma limitandone l’utilizzo solo al procedimento corrente. 
 
6.3.1 Moduli sw  
Nell’ambito dei nuovi moduli che saranno sviluppati per la ricerca Avvocato su ReGIndE, saranno gestite anche 
i casi relativi alle eccezioni.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 67/81 
 
6.3.2 Architettura  
N.A. 
6.3.3 Interfacce utente 
6.3.3.1 
Inserimento manuale: Indisponibilità ReGIndE o Avvocato Non Presente 
 
Nei casi di indisponibilità del sistema ReGIndE o di assenza dell’avvocato su ReGIndE, il sistema segnalerà 
all’utente il tipo di evento intercorso e presenterà nella form di Ricerca il pulsante per la funzione di ricerca 
dell’avvocato sul sistema SIES, al fine di consentire all’utente di proseguire con le proprie attività. 
 
Si riporta di seguito come si presenterà la form di Ricerca Avvocato su ReGIndE nei due suddetti casi 
 
 
Figura 39: Form Ricerca Difensore su ReGIndE in caso di assenza collegamento 
 
 
 
Figura 40: Form Ricerca Difensore su ReGIndE in caso nessun occorrenza trovata

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 68/81 
 
 
in cui, oltre a presentare l’esito della Ricerca su ReGIndE, è presente il tasto per avviare la Ricerca su SIES. 
 
La ricerca sarà effettuata sulla tabella ‘AVVOCATO’ del SIES e i parametri di ricerca saranno gli stessi utilizzati 
per la ricerca su ReGIndE [Rif. § “6.2 Ricerca su ReGIndE”]: Cognome e Nome dell’avvocato e Foro di 
appartenenza, se specificato, con opzione di ricerca mediante check-box per tutti i fori. 
La ricerca sarà relativa ai record che hanno il FLAG_REGINDE=’Sì’. 
I campi obbligatori saranno: Cognome e Foro, o in alternativa, Cognome e check-box ‘Tutti i Fori’. 
 
 
Figura 41: Form Elenco Avvocati SIES 
 
Nel caso l’esito della ricerca su SIES non producesse alcun risultato, quindi per avvocato non trovato in base ai 
criteri di ricerca digitati, la form presenterà il messaggio di assenza in SIES di avvocati, soddisfacenti i parametri 
di ricerca e presenterà il tasto per procedere all’inserimento di un nuovo difensore in SIES. 
 
 
Figura 42: Form Esito Ricerca Difensori SIES in caso di nessun occorrenza trovata

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 69/81 
 
 
 L’utente potrà scegliere di procedere con l’inserimento manuale dell’avvocato, selezionando il tasto 
 o potrà avviare una nuova di ricerca su ReGIndE o su SIES. 
Se l’utente seleziona l’Inserimento di un nuovo Difensore, il sistema chiuderà la Form di ricerca difensore e 
presenterà sulla Home Page di SIES la form di Inserimento. 
 
6.3.3.2 
Inserimento manuale avvocato sul sistema SIES 
 
La funzionalità di inserimento manuale consentirà all’utente di effettuerà l’inserimento dei dati dell’avvocato 
sulla tabella ‘AVVOCATO’ del SIES. A tal fine il sistema presenterà la seguente form di inserimento 
Figura 43: Form Inserimento Difensore in SIES 
 
Il campo Codice Fiscale sarà un dato obbligatorio, su cui il sistema effettuerà il controllo di correttezza formale, 
fatta eccezione la verifica del carattere di controllo finale.  
 
All’atto della conferma, prima di procedere all’inserimento, il sistema effettuerà nuovamente il controllo di 
verifica dell’eventuale presenza dell’anagrafica sulla tabella ‘AVVOCATO’ del SIES con FLAG_REGINDE = ‘Sì’. 
I criteri utilizzati per il controllo in questa fase saranno: 
• 
COGNOME

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 70/81 
 
• 
NOME 
• 
LUOGO DI NASCITA 
• 
DATA DI NASCITA 
• 
CODICE FISCALE 
• 
FORO. 
Per dati non trovati, la ricerca sarà raffinata progressivamente eliminando, di volta in volta, nell’ordine: 
• 
CODICE FISCALE 
• 
DATA DI NASCITA 
• 
LUOGO DI NASCITA 
fino ad effettuare la ricerca con i soli COGNOME, NOME e FORO. 
 
Qualora l’esito di tale controllo fosse “NON TROVATO”, cioè nel caso di anagrafica non trovata, il sistema 
procederà all’inserimento dei dati dell’avvocato sulla tabella ‘AVVOCATO’ del SIES, impostando anche il nuovo 
campo FLAG_REGINDE con il valore ‘NO’ e provvederà ad effettuare anche l’associazione al procedimento 
corrente (SIEP, SIUS, SIGE). 
Di conseguenza, il record di anagrafica inserito in questo frangente, avrà valenza solo per la gestione del 
fascicolo che l’utente sta inserendo in quel momento: l’avvocato inserito NON sarà visibile per la gestione di 
altri fascicoli. 
Qualora, invece, l’esito fosse “TROVATO”, cioè nel caso di anagrafica già presente, il sistema non effettuerà 
alcun inserimento. 
 
Nel caso che il codice fiscale contenga un codice Belfiore non esistente in SIES, il sistema invierà a video il 
messaggio di conferma a procedere all’inserimento ‘Comune di nascita non presente in SIES, si vuole procedere 
comunque all’inserimento?’. L’operatore potrà annullare l’operazione o procedere, in caso di prosecuzione 
l’avvocato sarà inserito nella base dati con il codice fiscale digitato, ma privo del luogo di nascita. 
 
Nella Form di dettaglio dei fascicoli associati a difensori aventi FLAG_REGINDE = ‘NO’, scaturenti da un 
inserimento manuale, sarà attivato un alert che NON costituirà errore bloccante ma sarà semplicemente un 
avviso per l’utente, il quale dovrà procedere a rieseguire l’associazione del difensore al fascicolo in lavorazione 
a partire da ReGIndE, come già descritto al § 6.1. 
 
6.3.4 Basi dati 
N.A. 
6.3.5 WEB services 
N.A. 
6.3.6 XSD 
N.A. 
6.3.7 Configurazione 
N.A. 
6.3.8 Tutorial 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 71/81 
 
6.4 REQ- SIE-021-04_FN.01 – Interventi su Funzioni SIES di Gestione Avvocati 
 
Poiché lo scopo degli interventi descritti nel presente documento è che i dati delle anagrafiche degli avvocati 
presenti su SIES dovranno essere “importati” dal sistema ReGIndE, sul sistema SIES saranno inibite le funzioni 
di Inserimento Difensore e Modifica Difensore. 
Nello specifico, nel menù Funzioni Amministrative» Gestione Difensori, il tasto ‘Inserimento’ non sarà più 
visibile, ed inoltre, nello stesso menù, nella Form di elenco Difensori ottenuta dal tasto di ‘ricerca’ sarà 
eliminata l’azione ‘modifica’. 
Nelle pagine corrispondenti ai punti di attivazione della ricerca su ReGIndE sarà eliminato il tasto ‘Inserimento’. 
Il sistema abiliterà l’inserimento manuale del difensore, SOLO, per la casistica di cui al par. “6.3.3.2 Inserimento 
manuale avvocato sul sistema SIES”. 
 
6.4.1 Moduli sw  
N.A. 
6.4.2 Architettura  
N.A. 
6.4.3 Interfacce utente 
Nell’attuale menu Funzioni Amministrative» Gestione Difensori 
 
 
Figura 44: Form Gestione Difensori - Attuale

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 72/81 
 
il tasto 
 sarà oscurato, per cui il menu riporterà le seguenti voci 
 
 
Figura 45: Form Gestione Difensori - Nuova 
 
Nell’attuale form Elenco Avvocati, risultato dell’attivazione della funzione Ricerca del precedente menu 
 
 
Figura 46: Form Elenco Difensori - Attuale 
 
sarà oscurata la funzione di modifica dell’avvocato, mentre la funzione di cancellazione, che è riportata solo se 
l’avvocato non è associato ad alcun procedimento SIES, rimarrà per permettere la cancellazione di avvocati 
inseriti precedentemente al rilascio degli interventi previsti in questo documento, pertanto la form sarà  
 
 
Figura 47: Form Elenco Difensori - Nuova 
 
6.4.4 Basi dati 
Per oscurare la funzione di Inserimento Avvocato, sarà realizzato e distribuito un apposito script che 
provvederà ad aggiornare la colonna DATA_FINE_VALIDITA per i records della tabella FUNZIONE_PROFILO 
riferiti alle funzioni Inserimento Avvocato e Modifica Avvocato. 
 
 
6.4.5 WEB services 
 
N.A. 
6.4.6 XSD 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 73/81 
 
6.4.7 Configurazione 
N.A. 
6.4.8 Tutorial 
N.A. 
 
6.5 REQ- SIE-021-05_FN.01 – Bonifica Anagrafica Avvocati SIES 
6.5.1 Bonifica dei dati presenti nella tabella Avvocato 
Prima di rendere effettiva in esercizio l’integrazione del SIES con il sistema ReGIndE sarà effettuata una bonifica 
al fine di allineare i dati presenti nella tabella ‘AVVOCATO’ del SIES a quelli presenti su ReGIndE. 
 
Prerequisiti per la realizzazione della bonifica sono: 
 
- 
 la messa a disposizione da parte di ReGIndE di un file excel contenente l’estrazione delle anagrafiche 
degli Avvocati, attivi, presenti su quella base dati. Nel caso che il file contenga più record per lo stesso 
avvocato, a fronte di più record di indirizzi con tipologia a ‘D’, sarà selezionato il primo ottenuto 
ordinando alfabeticamente la colonna Indirizzo; 
- 
l’aggiornamento della tabella COMUNE di SIES, come descritto nel cap. 6.6. 
Come già riportato al par. 6.2.3.1 pag. 39 la descrizione del Luogo Nascita, presente in ReGIndE, non sempre 
corrisponde a quella legalmente riconosciuta come denominazione di un Comune italiano, per questo motivo 
il comune di nascita dell’avvocato, sarà ricavato utilizzando il codice Belfiore contenuto nel suo Codice Fiscale, 
dato sempre presente in ReGIndE.  
Questo codice sarà poi utilizzando per estrarre dalla tabella COMUNE di SIES il codice Istat corrispondente, che 
valorizzerà la colonna COD_LUOGO_NASCITA della tabella AVVOCATO SIES.  
 
Nel caso in cui il codice Belfiore di un AVVOCATO ReGIndE non esista nella tabella COMUNE del SIES, 
l’AVVOCATO non sarà preso in considerazione ai fini della Bonifica e sarà inserito in una tabella degli Scarti 
della procedura. 
L’Elenco dei Comuni mancanti in SIES sarà inviato all’Amministrazione – Gruppo Tabelle fisse perché provveda 
ad eseguire gli opportuni accertamenti e a preparare uno script di aggiornamento della tabella COMUNE. 
 
Sarà realizzata una procedure plsql che agirà su tutte le anagrafiche presenti su SIES che risultino associate ad 
almeno un fascicolo con procedimenti in corso. 
In particolare: 
• 
Per SIEP, saranno presi in considerazione i procedimenti con stato diverso da Definito/Archiviato; 
• 
Per SIUS e SIGE, saranno presi in considerazione i procedimenti pendenti alla data della bonifica; 
• 
Per tutti e tre i sottosistemi non saranno considerati i procedimenti provenienti da BDI differenti da quella 
del Distretto su cui sarà eseguita la bonifica. 
Confronterà i dati presenti sui due sistemi e bonificherà i dati anagrafici di ciascun avvocato SIES, compreso il 
dato relativo al foro di appartenenza, a parità di anagrafica trovata su ReGIndE. 
Ogni anagrafica così bonificata avrà il FLAG_REGINDE = ‘Sì’ e sarà associata ad un codice ufficio di appartenenza 
fittizio (ad es. ‘00000’), in modo tale che l’avvocato risulti visibile al livello distrettuale.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 74/81 
 
 
I dati che saranno presi in considerazione per effettuare il confronto saranno: 
✓ Cognome 
✓ Nome 
✓ Luogo di Nascita 
✓ Data di Nascita 
✓ Foro di Appartenenza 
✓ Codice Fiscale 
Questo garantirà l’univocità delle anagrafiche sul sistema SIES, ovviando all’attuale duplicazione dovuta al fatto 
che ad ogni ufficio è permesso l’inserimento di un Avvocato anche se già presente in banca dati. 
 
La procedura in oggetto agirà, previo preventivo backup, sulla tabella ‘AVVOCATO’ del SIES e dovrà essere 
elaborata su ciascun distretto SIES. 
 
Le anagrafiche che non saranno bonificate in automatico, secondo i criteri su descritti, rimarranno inalterate 
e, quindi, NON BONIFICATE. 
Il FLAG_REGINDE, per queste, sarà valorizzato a ‘No’ e, proprio in base a tale criterio, esse saranno escluse da 
qualsiasi selezione operata nel sistema. 
In sostanza, queste anagrafiche non saranno più visibili né gestite dal sistema SIES e saranno, invece, 
storicizzate analogamente a quanto indicato al § “6.1 REQ-SIE-021-01_FN.01 - Gestione Nuovi Fori (FORO di 
NAPOLI NORD)” e “congelate” per come sono. 
 
Effettuata tale operazione, la stessa procedura provvederà a bonificare anche tutte le tabelle che abbiano una 
relazione con l’avvocato bonificato, aggiornandone il riferimento. 
 
Di seguito, l’elenco delle tabelle interessate dalla bonifica: 
 
• 
AVVOCATO_FASCICOLO_SIEP 
• 
AVVOCATO_FASCICOLO_SIUS 
• 
AVVOCATO_FASCICOLO_SIGE 
• 
PARTI_UDIENZA_DIFENSORE 
• 
STORICO_AVVOCATO 
• 
AVVISI_AVVOCATO 
• 
NUOVA_ISTANZA. 
 
Si ricorda che al momento in SIES il collegamento tra atti ed Avvocato è assicurato tramite chiave esterna 
all’ID_AVVOCATO. Tutti i riferimenti ai dati dell’Avvocato vengono estratti dal record Avvocato collegato al 
procedimento (es. sede ed indirizzo studio, riportato in molti template ed alcune forms). A valle dell’analisi e 
studio di dati estratti e forniti dall’Amministrazione, uno dei motivi di maggiore ricorrenza di duplicazione 
dell’avvocato in SIES è la non corrispondenza dell’indirizzo dello studio, riportato negli atti, tra quelli presenti 
in base dati. A seguito della bonifica, non dando valore all’indirizzo ai fini dell’accorpamento, tutti gli avvocati 
bonificati, aventi i restanti dati indicati in precedenza uguali e aventi precedentemente indirizzi differenti, 
faranno tutti riferimento all’ indirizzo importato da ReGIndE.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 75/81 
 
6.5.2 Moduli sw  
N.A. 
6.5.3 Architettura  
N.A. 
6.5.4 Interfacce utente 
N.A. 
6.5.5 Basi dati 
Per l’importazione dei dati forniti da ReGIndE sarà creata una nuova tabella di appoggio W_AVV_REGINDE e 
sarà realizzata una procedure plsql Importa_avv_ReGIndE. 
 
Nella tabella tabellefisse18novembre2020.xlsx, fornita dall’Amministrazione, sono presenti 388221 records di 
cui 13719 riferiti ad Avvocatura Stato, CNF ed Enti, tali records non saranno presi in considerazione ai fini 
dell’attività di bonifica. 
 
Alla tabella AVVOCATO di SIES saranno aggiunte nuove colonne: PEC, PROC_PENDENTI, FLAG_REGINDE, 
ID_AVV_BONIFICATO, DESCR_COMUNE_STUDIO. 
 
Sarà realizzata la procedure PLSQL BONIFICA_AVVOCATI per la bonifica dei dati della tabella AVVOCATO, che 
eseguirà le seguenti operazioni: 
 
- 
per ciascun record della tabella AVVOCATO di SIES verificherà se ad esso sono collegati procedimenti 
SIEP o SIUS o SIGE ancora pendenti, in caso affermativo valorizzerà la colonna PROC_PENDENTI a ‘SI’, 
diversamente a ‘NO’;  
- 
per ciascun record della tabella AVVOCATO di SIES verificherà se ad esso sono collegati solamente 
procedimenti SIEP o SIUS o SIGE non appartenenti alla BDI su cui si sta eseguendo la procedura, in caso 
affermativo valorizzerà la colonna PROC_PENDENTI a ‘NO’;  
- 
per tutti i records AVVOCATO sarà preimpostato il FLAG_REGINDE a ‘NO’; 
- 
inizierà la lettura dei records dalla tabella W_AVV_REGINDE, per ciascun record letto saranno ricercati 
nella tabella AVVOCATO di Sies i records aventi Cognome, Nome, Luogo di Nascita, Data di Nascita, 
Foro di Appartenenza, Codice Fiscale uguali a quelli del record proveniente da ReGIndE e 
PROC_PENDENTI = ‘SI’. Poiché ci possono essere su SIES più records AVVOCATO soddisfacenti le 
suddette condizioni, si procederà ad aggiornare il record con data_inserimento più recente 
impostando il FLAG_REGINDE = ‘SI’ e FLAG_CANCELLATO = ‘N’, mentre per gli altri records si procederà 
ad impostare FLAG_CANCELLATO = ‘S’ e a valorizzare ID_AVVOCATO_BONIFICATO con l’ID 
dell’avvocato impostato con FLAG_REGINDE = ‘SI’; 
- 
al termine della lettura di tutti i records della tabella W_AVV_REGINDE e dell’attività di aggiornamento 
della tabella avvocato, si procederà, per tutti i records aventi la colonna ID_AVVOCATO_BONIFICATO 
valorizzata, ad eseguire: 
- 
update records tabella AVVOCATO_FASCICOLO_SIUS aventi AVV_ID_AVVOCATO = ID_AVVOCATO 
impostando AVV_ID_AVVOCATO = ID_AVVOCATO_BONIFICATO;

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 76/81 
 
- 
update records tabella AVVOCATO_FASCICOLO_SIEP aventi AVV_ID_AVVOCATO = ID_AVVOCATO 
impostando AVV_ID_AVVOCATO = ID_AVVOCATO_BONIFICATO; 
- 
update records tabella AVVOCATO_FASCICOLO_SIGE aventi AVV_ID_AVVOCATO = ID_AVVOCATO 
impostando AVV_ID_AVVOCATO = ID_AVVOCATO_BONIFICATO; 
- 
up update records tabella PARTI_UDIENZA_DIFENSORE aventi AVV_ID_AVVOCATO = ID_AVVOCATO 
impostando AVV_ID_AVVOCATO = ID_AVVOCATO_BONIFICATO; 
- 
update records tabella STORICO_AVVOCATO aventi AVV_ID_AVVOCATO = ID_AVVOCATO impostando 
AVV_ID_AVVOCATO = ID_AVVOCATO_BONIFICATO; 
- 
date records tabella AVVISI_AVVOCATO aventi AVV_ID_AVVOCATO = ID_AVVOCATO impostando 
AVV_ID_AVVOCATO = ID_AVVOCATO_BONIFICATO; 
- 
update records tabella NUOVA_ISTANZA aventi AVV_ID_AVVOCATO = ID_AVVOCATO impostando 
AVV_ID_AVVOCATO = ID_AVVOCATO_BONIFICATO. 
E’ da valutare se procedere immediatamente o a distanza di un certo periodo alla cancellazione fisica dei 
records AVVOCATO con ID_AVVOCATO_BONIFICATO o lasciarli nella base dati, essendo comunque cancellati 
logicamente (FLAG_CANCELLATO = ‘S’ e FLAG_REGINDE =’NO’), quindi non più utilizzabili per nuove 
assegnazioni. 
 
6.5.6 WEB services 
N.A. 
6.5.7 XSD 
N.A. 
6.5.8 Configurazione 
N.A. 
6.5.9 Tutorial 
N.A. 
6.6 REQ- SIE-021-06_FN.01 – Aggiornamento Tabelle COMUNE e CG_REF_CODES di SIES 
Prima di procedere alla bonifica dei dati presenti nella tabella ‘AVVOCATO’ del SIES con quelli presenti su 
ReGIndE, bisognerà aggiornare le tabelle di SIES, COMUNE e CG_REF_CODES, limitatamente ai domini 
PROVINCIA, REGIONE e NAZIONE, con i dati presenti nelle tabelle fisse COMUNE, PROVINCIA, REGIONE e 
STATO-NAZIONE fornite dalla DGSIA. Realizzando di fatti un allineamento fra i due ambienti, che permetterà 
la gestione della tabella COMUNE di SIES da parte del gruppo tabelle fisse dell’Amministrazione. 
 
La tabella COMUNE di SIES aggiornata sarà ridistribuita in tutti i Distretti in sostituzione della preesistente. 
 
6.6.1 Aggiornamento dei dati presenti nella tabella COMUNE di SIES 
La tabella COMUNE di SIES, sostanzialmente ferma al momento del caricamento iniziale (anno 2003), sarà 
aggiornata con i dati presenti nella tabella COMUNE della DGSIA, in cui è presente anche il codice catastale,

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 77/81 
 
che come indicato ai capp. 6.2 e 6.5, sarà un dato essenziale per la valorizzazione del comune di nascita 
dell’avvocato, desumendolo dal codice fiscale importato da ReGIndE. 
 
L’attuale tabella COMUNE di SIES, che contiene al momento 8113 records, non gestisce la storicizzazione dei 
comuni, attraverso una data fine validità, ma è presente solo un FLAG_VALIDITA, che al momento è valorizzato 
ad ‘N’ solo per il comune fittizio di ‘NAPOLI NORD’, utilizzato per escludere il comune dalle funzioni di ricerca. 
 
La tabella è cosi strutturata 
 
Nome Colonna 
Contenuto 
COD_COMUNE 
Codice Istat  
COD_PROVINCIA 
Codice Provincia 
DESCRIZIONE 
Denominazione Comune 
CAP 
Codice Avviamento Postale 
DATA_CARICAMENTO_REGE 
Data Caricamento in SIES 
COD_SEDE_GIUDIZIARIA 
Codice Circondario Competente 
FLAG_VALIDITA 
‘S’ se valido, ‘N’ non valido 
 
La tabella COMUNE DGSIA, contenente 13251 record, gestisce la storicizzazione dei comuni, che hanno subito 
cambi di provincia, cambi di denominazione, accorpamenti con altro comune, attraverso l’utilizzo di una data 
fine validità. I Comuni al momento attivi, cioè con data fine validità non valorizzata, sono 7907.  
 
La tabella è cosi strutturata 
 
Nome Colonna 
Contenuto 
COD_COMUNE 
Codice Istat  
COD_PROVINCIA 
Codice Provincia 
COD_SEDE_GIU_TRIB_COMP 
Codice Circondario Competente 
DESC_COMUNE 
Denominazione Comune 
DATA_FINE_VALIDITA 
Data fine validità del codice comune 
CAP 
Codice Avviamento Postale 
COD_CATASTALE 
Codice Catastale 
 
Per poter procedere all’aggiornamento, la tabella COMUNE di SIES sarà modificata con l’aggiunta delle 
seguenti colonne: DATA_FINE_VALIDITA, COD_CATASTALE, DATA_AGGIORNAMENTO 
 
Per l’aggiornamento della tabella COMUNE SIES saranno realizzate le seguenti attività: 
 
- 
import dei dati della tabella COMUNE DGSIA su una tabella di appoggio SIES COMUNE_DGSIA; 
 
- 
realizzazione di una procedure PLsql che per ciascun record letto nella tabella COMUNE_DGSIA 
effettuerà le seguenti operazioni: 
 
o se nella tabella COMUNE SIES esiste un record avente COD_COMUNE con lo stesso 
COD_COMUNE in input, il sistema procederà ad aggiornare le colonne COD_PROVINCIA, 
DESCRIZIONE, CAP, COD_SEDE_GIUDIZIARIA, COD_CATASTALE, DATA_FINE_VALIDITA con i

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 78/81 
 
valori 
presenti 
nelle 
colonne 
 
COD_PROVINCIA, 
DESC_COMUNE, 
CAP, 
COD_SEDE_GIU_TRIB_COMP, COD_CATASTALE, DATA_FINE_VALIDITA della tabella della 
DGSIA. Inoltre, se la DATA_FINE_VALIDITA non è NULL, sarà impostato la colonna 
FLAG_VALIDITA a ‘N’, negli altri casi a ‘S’; sarà sempre valorizzata la DATA_AGGIORNAMENTO 
con la data di elaborazione; 
o se nella tabella COMUNE SIES non esiste un record avente COD_COMUNE con lo stesso 
COD_COMUNE in input, il sistema procederà ad inserire un nuovo record valorizzando le 
colonne COD_COMUNE, COD_PROVINCIA, DESCRIZIONE, CAP, COD_SEDE_GIUDIZIARIA, 
COD_CATASTALE, DATA_FINE_VALIDITA con i valori presenti nelle colonne  COD_COMUNE, 
COD_PROVINCIA, DESC_COMUNE, CAP, COD_SEDE_GIU_TRIB_COMP, COD_CATASTALE, 
DATA_FINE_VALIDITA della tabella della DGSIA. Inoltre, se la DATA_FINE_VALIDITA non è 
NULL, sarà impostato la colonna FLAG_VALIDITA a ‘N’, negli altri casi a ‘S’; saranno sempre 
valorizzate le colonne DATA_CARICAMENTO_REGE e DATA_AGGIORNAMENTO con la data di 
elaborazione. 
o al termine della procedura di aggiornamento, al fine di avere un perfetto allineamento delle 
due tabelle, tutti i records della tabella COMUNE SIES con data aggiornamento non valorizzata 
saranno estratti e trasmessi al Gruppo Tabelle fisse della DGSIA perché provveda 
all’inserimento dei Comuni nella propria tabella fissa. 
Dal momento in cui il Gruppo tabelle fisse prenderà in carico la gestione della tabella COMUNE di SIES, per 
ogni nuovo aggiornamento, oltre alla trasmissione di tutti i valori inseriti nella tabella COMUNE DGSIA, dovrà 
valorizzare anche il FLAG_VALIDITA a ‘S’ se DATA_FINE_VALIDITA non valorizzata, a ‘N’ in caso contrario. 
 
6.6.2 Aggiornamento dei dati presenti nella tabella CG_REF_CODES (domini PROVINCIA, REGIONE, 
NAZIONE) 
Il Gruppo tabelle fisse della DGSIA ha fornito anche le tabelle PROVINCIA, REGIONE, STATO-NAZIONE, 
che non possono essere adottate nella loro struttura da SIES, in quanto richiederebbero importanti 
interventi sul software. 
 
In SIES i dati riportati nelle suddette tabelle sono gestite nella tabella delle decodifiche 
CG_REF_CODES, rispettivamente nei domini PROVINCIA, REGIONE e NAZIONE. 
 
I domini aggiornati saranno ridistribuiti in tutti Distretti in sostituzione di quelli preesistenti. 
 
6.6.2.1 
Aggiornamento dominio PROVINCIA 
 
La tabella PROVINCIA (DGSIA) è strutturata in records con le colonne COD_PROVINCIA, 
COD_REGIONE, DESC_PROVINCIA, FINE_VALIDITA. 
 
I records della CG_REF_CODES riferiti alla ‘PROVINCIA’ hanno la colonna RV_DOMAIN = ‘PROVINCIA’, 
RV_LOW_VALUE= sigla provincia, RV_MEANING = denominazione Provincia e RV_ABBREVIATION non 
valorizzato.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 79/81 
 
Per l’aggiornamento del dominio ‘PROVINCIA’ sarà realizzata una procedura che leggendo i records 
presenti nella tabella PROVINCIA della DGSIA, importata in una tabella d’appoggio di SIES, effettuerà 
le seguenti operazioni: 
 
o se nella tabella CG_REF_CODES esiste un record avente RV_DOMAIN = ‘PROVINCIA’ e 
RV_LOW_VALUE = COD_PROVINCIA del record in input, il sistema procederà ad aggiornare le 
colonne 
RV_MEANING, 
RV_ABBREVIATION 
con 
i 
valori 
presenti 
nelle 
colonne 
DESC_PROVINCIA, COD_REGIONE del record in input; 
o se nella tabella CG_REF_CODES non esiste un record avente RV_DOMAIN = ‘PROVINCIA’ e 
RV_LOW_VALUE = COD_PROVINCIA del record in  input, il sistema procederà ad inserire un 
nuovo record valorizzando le colonne con RV_DOMAIN = ‘PROVINCIA’ e RV_LOW_VALUE, 
RV_ABBREVIATION, RV_MEANING rispettivamente con i valori contenuti nelle colonne 
COD_PROVINCIA, COD_REGIONE, DESC_PROVINCIA del record in input; 
o al termine della procedura di aggiornamento, al fine di avere un perfetto allineamento delle 
due tabelle, tutti i records della tabella CG_REF_CODES con RV_DOMAIN = ‘PROVINCIA’ e con 
RV_ABBREVIATION non valorizzata saranno estratti e trasmessi alla DGSIA perché provveda 
all’inserimento dei Comuni nella propria tabella fissa. 
In caso di aggiornamento della tabella fissa PROVINCIA, il Gruppo tabelle fisse della DGSIA dovrà 
trasmettere le modifiche anche a SIES.  
6.6.2.2 
Aggiornamento dominio REGIONE 
I records della CG_REF_CODES riferiti alla ‘REGIONE’ hanno la colonna RV_DOMAIN = ‘REGIONE’ e 
RV_DOMAIN = Valore Codice Regione, RV_MEANING = Descrizione della Regione. 
 
La tabella REGIONE è strutturata in records con le colonne COD_REGIONE e DESC_REGIONE. 
 
I valori records contenuti nella CG_REF_CODES corrispondono sostanzialmente con i valori dei 
records contenuti nella tabella REGIONE. 
 
Bisognerà solo aggiornare le denominazioni delle seguenti records della CG_REF_CODES con quelle 
presenti nella tabella REGIONE 
 
Attuale denominazione RV_MEANING 
Nuova denominazione (presente in REGIONE) 
VALLE D'AOSTA 
VAL D'AOSTA 
TRENTINO-ALTO ADIGE 
TRENTINO ALTO ADIGE 
FRIULI-VENEZIA GIULIA 
FRIULI V. GIULIA 
EMILIA-ROMAGNA 
EMILIA ROMAGNA 
 
Ai fini di un perfetto allineamento di SIES alla tabella DGSIA nella CG_REF_CODES sarà inserito un 
nuovo record per la Regione ‘LUOGO SCONOSCIUTO’ (codice 21) presente nella tabella fissa. 
 
Viceversa per l’allineamento della tabella REGIONE al contenuto dei records del dominio REGIONE di 
SIES, bisognerebbe inserire nella tabella fissa un record con COD_REGIONE = ‘-‘ e

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 80/81 
 
DESC_REGIONE =‘-‘. 
 
Considerando il numero limitato di records da modificare l’allineamento su SIES sarà effettuato 
manualmente. 
 
In caso di aggiornamento della tabella fissa REGIONE, il Gruppo tabelle fisse della DGSIA dovrà 
trasmettere le modifiche anche a SIES.  
 
6.6.2.3 
Aggiornamento dominio NAZIONE 
 
I records della CG_REF_CODES riferiti alla ‘NAZIONE’ hanno la colonna RV_DOMAIN = ‘NAZIONE’, 
RV_LOW_VALUE= codice dello stato e RV_MEANING = descrizione dello stato. 
 
La tabella STATO-NAZIONE è strutturata in records con le colonne COD_STATO, DESC_STATO, 
COD_CASELLARIO, DATA _FINE_VALIDITA, COD_STATO_ISO, COD_ISTAT_STATO. 
 
Per l’aggiornamento del dominio ‘NAZIONE’ sarà realizzata una procedura che leggendo i records 
presenti nella tabella STATO_NAZIONE della DGSIA, importata in una tabella d’appoggio di SIES, 
effettuerà le seguenti operazioni: 
 
o se nella tabella CG_REF_CODES esiste un record avente RV_DOMAIN = ‘NAZIONE’ e 
RV_LOW_VALUE = COD_STATO del record in input, il sistema procederà ad aggiornare le 
colonne RV_MEANING, RV_HIGH_VALUE, RV_ABBREVIATION con i valori presenti nelle 
colonne  DESC_STATO, COD_STATO_ISO, COD_ISTAT_STATO del record in input; 
o se nella tabella CG_REF_CODES non esiste un record avente RV_DOMAIN = ‘NAZIONE’ e 
RV_LOW_VALUE = COD_ STATO del record in  input, il sistema procederà ad inserire un nuovo 
record valorizzando le colonne con RV_DOMAIN = ‘NAZIONE’ e RV_LOW_VALUE, 
RV_HIGH_VALUE, RV_ABBREVIATION, RV_MEANING rispettivamente con i valori contenuti 
nelle colonne COD_ STATO, COD_STATO_ISO, COD_ISTAT_STATO, DESC_STATO del record in 
input; 
o al termine della procedura di aggiornamento, al fine di avere un perfetto allineamento delle 
due tabelle, tutti i records della tabella CG_REF_CODES con RV_DOMAIN = ‘NAZIONE’ e  con 
RV_HIGH_VALUE non valorizzata saranno estratti e trasmessi alla DGSIA perché provveda 
all’inserimento degli Stati di SIES nella propria tabella fissa. 
 
In caso di aggiornamento della tabella fissa STATO-NAZIONE, il Gruppo tabelle fisse della DGSIA dovrà 
trasmettere le modifiche anche a SIES.  
 
6.6.3 Moduli sw  
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-
SIES - RegInde 
Ver.2.0 del 18/12/2020 
Pag. 81/81 
 
6.6.4 Architettura  
N.A. 
6.6.5 Interfacce utente 
N.A. 
6.6.6 Basi dati 
Alla tabella COMUNE saranno aggiunte le seguenti colonne DATA_FINE_VALIDITA, COD_CATASTALE, 
DATA_AGGIORNAMENTO. 
 
Per l’aggiornamento della tabella COMUNE sarà realizzata la procedure PLSQL Aggiorna_COMUNE_SIES. 
 
Per l’aggiornamento del dominio PROVINCIA della CG_REF_CODES sarà realizzata la procedure PLSQL 
Aggiorna_PROVINCIA_SIES. 
 
Per l’aggiornamento del dominio NAZIONE della CG_REF_CODES sarà realizzata la procedure PLSQL 
Aggiorna_NAZIONE_SIES. 
 
 
6.6.7 WEB services 
N.A. 
6.6.8 XSD 
N.A. 
6.6.9 Configurazione 
N.A. 
6.6.10 Tutorial 
N.A.