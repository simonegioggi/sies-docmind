---
uniqueName: siut-sie-sc-1-0-20191004-schedaintervento-9-adegua
displayName: "SIUT SIE SC 1 0 20191004 Scheda Intervento 9 Adeguamento al SIES DLGS 123 2018 e"
category: "GENERAL"
tags: []
---

# SIUT-SIE-SC-1.0-20191004-Scheda_Intervento-9-Adeguamento_al_SIES_DLGS-123_2018_e_121_2018

> **File originale:** `MEV/SCHEDA_009/SchedaIntervento/SIUT-SIE-SC-1.0-20191004-Scheda_Intervento-9-Adeguamento_al_SIES_DLGS-123_2018_e_121_2018.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
 
Scheda Intervento n° 9 - Adeguamento 
SIES al DLGS 123_2018 e 121_2018 
 
 
 
 
 
 
 
 
 
Versione 1.0 del 04/10/2019

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 2/38 
 
 
 
Il presente documento è stato redatto con la 
collaborazione 
del 
RTI 
Engineering 
Ingegneria 
Informatica S.p.A 
 - Sirfin-PA 
nell’ambito del contratto CIG 73479643B7 per lo 
“SVILUPPO 
DEL 
SISTEMA 
INFORMATIVO 
UNITARIO TELEMATICO, LA MANUTENZIONE 
DEGLI ATTUALI SISTEMI DELL’AREA PENALE 
DEL MINISTERO DELLA GIUSTIZIA E SERVIZI 
CORRELATI. LOTTO 1” e del PLO Scheda Intervento 
n° 9 - Adeguamento SIES al DLGS 123_2018 e 
121_2018.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 3/38 
Elenco approvazioni per versione 
 
 
Versione 
 
V. 1.0 del 04/10/2019 
 
 
Responsabile del Progetto 
Paolo Ceccanti 
Redatto da: 
Vito Bufi 
Verificato da 
Vito Bufi 
Approvato da 
Paolo Ceccanti 
Data approvazione 
04/10/2019 
Livello di riservatezza 
L3

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 4/38 
INDICE DEI CONTENUTI 
1 
INTRODUZIONE ................................................................................................................... 7 
1.1 
SCOPO DEL DOCUMENTO ................................................................................................................... 7 
1.2 
ACRONIMI E DEFINIZIONI .................................................................................................................... 7 
1.2.1 
Acronimi ................................................................................................................................................ 7 
1.2.2 
Definizioni ............................................................................................................................................ 8 
1.3 
RIFERIMENTI .................................................................................................................................... 8 
2 
DEFINIZIONE DELL’OBIETTIVO ........................................................................................... 10 
3 
DESCRIZIONE DELL’INTERVENTO ....................................................................................... 11 
3.1 
AMBITO NORMATIVO ....................................................................................................................... 11 
3.2 
ADEGUAMENTO SISTEMA SIUS DLGS 123/2018 (UFFICI MAGGIORENNI) ........................................... 12 
3.3 
ADEGUAMENTO SISTEMA SIEP DLGS 123/2018 (UFFICI MAGGIORENNI) ........................................... 15 
3.4 
ADEGUAMENTO SISTEMA SIUS D.LGS. 121/2018 (UFFICI MINORENNI) .............................................. 17 
3.5 
ADEGUAMENTO SISTEMA SIEP D.LGS. 121/2018 (UFFICI MINORENNI) ............................................. 20 
3.5.1 
Misure penali di comunità .....................................................................................................................20 
3.5.2 
Emissione Ordine di Esecuzione con Decreto di Sospensione .................................................................. 25 
3.5.3 
Restituzione atti per ulteriore corso .......................................................................................................26 
3.5.4 
Annotazioni su decreto di sospensione .................................................................................................. 27 
3.5.5 
istruttorie/richieste ............................................................................................................................... 27 
3.5.6 
Istanza ................................................................................................................................................28 
3.5.7 
Gestione Notifiche ...................................................................................................................................29 
3.6 
ALTRI INTERVENTI PER SIUS MINORI ................................................................................................. 29 
3.7 
ARGOMENTAZIONI SOSPESE ............................................................................................................. 30 
3.8 
MODULI SW .................................................................................................................................... 30 
3.9 
ARCHITETTURA ............................................................................................................................... 30 
3.10 
INTERFACCE UTENTE ........................................................................................................................ 30 
3.11 
BASI DATI ....................................................................................................................................... 31 
4.1 
WEB SERVICES ............................................................................................................................... 31 
4.2 
XSD .............................................................................................................................................. 31 
4.3 
CONFIGURAZIONE ........................................................................................................................... 31 
4.4 
TUTORIAL....................................................................................................................................... 31 
5 
PIANO DELLE ATTIVITÀ ...................................................................................................... 32 
5.1 
CICLO DI SVILUPPO .......................................................................................................................... 32 
5.2 
PIANO DELLE ATTIVITÀ ..................................................................................................................... 35 
5.3 
GANTT ........................................................................................................................................... 35 
5.4 
VINCOLI ......................................................................................................................................... 36 
5.5 
LUOGO DI LAVORO .......................................................................................................................... 36 
6 
DIMENSIONAMENTO .......................................................................................................... 37 
6.1 
STIMA DELL'EFFORT PREVISTO .......................................................................................................... 37

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 5/38 
6.2 
DETTAGLIO COSTI ........................................................................................................................... 37 
 
 
Lista di distribuzione 
 
Amministrazione: RUP, DEC  
RTI: RUF, Referente tecnico, Referente sviluppo, referente CDC, Referente sicurezza, Referente qualità

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 6/38 
Elenco versioni 
 
Versioni 
Data Versione 
Capitolo 
Modifica 
1.0 
04/10/2019 
 
Prima Emissione

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 7/38 
1 Introduzione 
1.1 Scopo del documento 
La presente Scheda di Intervento costituisce lo strumento di supporto alla gestione complessiva delle 
attività previste per un intervento.  
La Scheda di Intervento si articola in due sezioni: 
Descrizione dell’Intervento, in cui vengono declinati obiettivi, ambito ed approccio progettuale. 
Piano delle attività, in cui viene presentato il piano delle attività con declinazione di tempi e costi 
dell’intervento. 
L’intervento in oggetto rientra nel servizio di Manutenzione Evolutiva, è stato richiesto con comunicazione 
m_dg.DOG07AR.08082019.0000017.U ed è classificato come di seguito riportato: 
 
Scheda di Intervento  
2019_09  
Oggetto  
Adeguamento normativo SIES al DLgs 123/18 e 121/18  
Complessità  
Alta  
Servizio  
MEV  
 
 
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 8/38 
Sigla 
Descrizione 
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
Glossa 
Sinonimo 
Definizione 
 
 
 
 
 
 
 
 
 
1.3 Riferimenti 
Riferimento 
Nome Documento 
Descrizione Documento 
1.  
m_dg.DOG07AR.08082019.0000017.U 
Richiesta Scheda di Intervento 
2.  
ANALISIDECRETON.121-16-12-2018.doc 
 
3.  
Minori_Modifiche_05_12.doc

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 9/38 
4.  
Modificheriferimentinormativi.doc 
 
5.  
SIES-SIEP-
ModificheDecretoLegislativon.123.doc 
 
6.  
SIES-SIUS-
ModificheDecretoLegislativon.123.doc

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 10/38 
2 Definizione dell’Obiettivo 
 
Nell’ambito del progetto SIES si chiede di intervenire per adeguare il sistema a seguito del Dlgs 123/18 e del 
Dlgs 121/18.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 11/38 
3 Descrizione dell’Intervento 
 
3.1 Ambito Normativo 
L’intervento legislativo nel suo complesso ( d.lgs 121/2018 e dlgs 123/2018) ha introdotto l’invocata organica 
disciplina dell’esecuzione della pena nei confronti dei minorenni. 
Il capo II° del dlgs121/2018 disciplina l’esecuzione penale esterna ed in particolar modo le misure penali di 
comunità:  
• 
affidamento in prova al servizio sociale; 
• 
 affidamento con detenzione domiciliare;  
• 
detenzione domiciliare; 
• 
 semilibertà e affidamento in prova in casi particolari. 
 
La misura di comunità ha la stessa durata della pena da eseguire e deve essere corredata da un programma 
di intervento educativo, in relazione della funzione pedagogica della pena che giustifica la preferenza per le 
misure in questione rispetto alla custodia in carcere. 
L’applicazione della misura penale in comunità è disposta, cosi come la revoca, dal Tribunale di 
Sorveglianza. 
Il magistrato di sorveglianza, ex art. 8 comma 4° d.lgs 121/2018, può disporre in via provvisoria la 
sospensione della misura, la quale è tuttavia suscettibile di essere sostituita con altra. 
Il magistrato, inaudita altera parte, emesso il decreto di sospensione trasmette immediatamente gli atti al 
Tribunale di Sorveglianza per le decisioni di competenza che devono avvenire entro 30 giorni dalla ricezione 
degli atti, pena la perdita di efficacia del provvedimento interinale del magistrato. 
In caso di revoca, il periodo trascorso in detenzione domiciliare in semilibertà è scomputato dalla pena 
ancora da espiare: in particolare nell’ affidamento in prova al servizio sociale e dell’affidamento in prova con 
detenzione domiciliare, il Tribunale di Sorveglianza determina la pena da espiare, tenuto conto della durata 
della misura concessa, delle limitazioni imposte al condannato e del suo comportamento durante il periodo 
trascorso. 
Detenzione intramuraria è l’extra ratio del trattamento penitenziario minorile, si rivolge ai:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 12/38 
- 
condannati in via definitiva a pena detentiva (anche residua) superiore ad anni 4, ovvero ad anni 6, 
se tossicodipendenti;  
- 
Coloro che hanno avuto revocato la sospensione dell’esecuzione per difetto di tempestiva richiesta 
di misura alternativa, ovvero per inammissibilità della stessa;   
- 
Coloro che hanno avuto revocata una misura penale di comunità o non sia stata applicata per 
mancanza di condizioni.  
 
Il capo IV del d.lgs 121/2018 regola il progetto di intervento educativo sul quale si struttura la permanenza 
dei condannati negli istituti penali per minorenni.  
Le misure alternative alla detenzione, fruibili dopo l’entrata in vigore del d.lgs 121/2018: 
- 
Liberazione anticipata: competente il magistrato di sorveglianza riduzione di giorni 45 per semestre 
sul presupposto di un corretto comportamento durante il periodo di pena scontata anche mediante 
misura penale di comunità; 
- 
Liberazione condizionale: competenza tribunale di sorveglianza su presupposto di un sicuro 
ravvedimento e prova costante di ottima condotta durante l’esecuzione della pena. 
 
3.2 Adeguamento sistema SIUS dlgs 123/2018 (UFFICI MAGGIORENNI) 
 
In riferimento ai Tribunali di Sorveglianza (uffici TDS), si elencano le attività necessarie ai fine 
dell’adeguamento del sistema SIUS al d.lgs. 123/2018 (UFFICI MAGGIORENNI): 
 
1. Creare una nuova funzione per l’emissione del Decreto presidenziale di designazione. Per la nuova 
funzione prevedere la maschera per l’inserimento, modifica, validazione, stampa e cancellazione. 
Prevedere un nuovo template: il template sarà indicato dall’Amministrazione. 
 
2. Creare una statistica/Scadenzario che elenchi i Procedimenti che entro una determinata data non 
hanno avuto un’ordinanza di Ammissione Provvisoria emessa.  
 
3. Creare una nuova Ordinanza (ordinanza provvisoria).  Quindi prevedere una nuova voce nel menù

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 13/38 
“ordinanze” denominata “Applicazione provvisoria m.a.”. 
 
4. Intervenire sull’aggiornamento della funzione STATISTICHE – MOVIMENTO PROVVEDIMENTI PER 
OGGETTI in modo da integrare anche questa nuova tipologia di ordinanza provvisoria. 
 
5. Aggiornare i servizi esposti lato SIES per Avvocatura in modo tale che tale ordinanza (ordinanza 
provvisoria) possa essere visibile anche agli Avvocati dal sistema Avvocatura Centrale. 
(L’aggiornamento lato Avvocatura Centrale, per la recezione di queste nuove tipologie di ordinanze 
non è conteggiata come parte di questo PLO). 
 
6. Intervenire sull’aggiornamento della funzione Impugnazioni/Opposizioni per poterla annotare sul 
procedimento provvisorio. 
 
7. Modifica della maschera di inserimento e modifica di un procedimento di REVOCA DI MISURA 
ALTERNATIVA prevedendo un checkbox per individuare se il procedimento nasce da una semplice 
proposta ovvero da un provvedimento di sospensione provvisoria della misura da parte del MS. 
 
8. Prevedere una funzione di ricerca per individuare quanti procedimenti nascono da una sospensione 
e quanti da semplice proposta. 
 
9. Prevedere la gestione di un nuovo tipo procedimento di ‘Sospensione Pene Accessorie’. Per la nuova 
funzione prevedere la maschera per l’inserimento, modifica, validazione, stampa e cancellazione. 
Prevedere un nuovo template: il template sarà indicato dall’Amministrazione 
 
 
ATTIVITA’ SULLA BANCA DATI: 
 
1. Creare un nuovo contenuto per TDS: Concessione misure alternative (art. 678 comma 1-ter c.p.p.). 
Creare gli oggetti ed esiti per tale contenuto.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 14/38 
2. Creare un nuovo contenuto per TDS: Revoca ammissione provvisoria misura alternativa – Art. 678 
comma 1 er c.p.p. . Creare gli oggetti ed esiti per tale contenuto. 
 
3. Aggiungere un nuovo esito, che si potrebbe chiamare “sostituisce la misura alternativa” per il 
contenuto di Revoca della misura alternativa. 
 
4. Creare due nuovi contenuti (per TDS e UDS) ed un nuovo oggetto denominati “sospensione pene 
accessorie (art. 51 quater O.P.). Gli esiti saranno “sospende pena accessoria”, “Rigetto”, “NLP”, 
“Inammissibilità” e “Incompetenza”. 
 
5. Aggiungere nella lista dei mittenti presente nella maschera di iscrizione SIUS la voce “gruppo di 
osservazione e trattamento”. 
 
6. Modificare la denominazione del contenuto “Lavoro esterno” in “Lavoro esterno/Lavoro di pubblica 
utilità. 
 
7. Aggiungere un nuovo oggetto denominato “Ammissione Lavoro di pubblica utilità (art. 20 ter O.P.). 
8. Per gli oggetti: 
• 
Revoca Lavoro Esterno - Art. 48 co. 15 D.P.R. n. 230/2000 (Reg.Esec.) 
• 
Modifica Lavoro Esterno (Art. 21 O.P.) - Art. 21 O.P. 
• 
Sospensione lavoro esterno - Art. 21 O.P. 
sostituire la parte “Lavoro esterno” con “Lavoro esterno/Lavoro di pubblica utilità. 
 
9. Prevedere una nuova procedura Oracle per creare la statistica/Scadenzario che elenchi i 
Procedimenti che entro una determinata data non hanno avuto un’ordinanza di Ammissione 
Provvisoria emessa.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 15/38 
3.3 Adeguamento sistema SIEP dlgs 123/2018 (UFFICI MAGGIORENNI) 
 
In riferimento agli uffici Procura (uffici PM), si elencano le attività necessarie ai fini dell’adeguamento del 
sistema SIEP al d.lgs. 123/2018 (UFFICI MAGGIORENNI). 
 
Per le seguenti misure alternative: 
 
• 
Affidamento in prova 
• 
Detenzione domiciliare 
• 
Semilibertà 
• 
Sospensione esecuzione PENA 
 
1. Deve essere gestita la funzione di ‘Applicazione provvisoria misura alternativa - art 678 comma 1 ter 
– art. 4, appoggiandosi sull’attuale funzione di AMMISSIONE PROVVISORIA, già presente per 
alcune 
tipologie 
di 
misure 
alternative, 
modificandola 
in 
AMMISSIONE 
PROVVISORIA/CONCESSIONE art 678 c1 ter. Per la SEMILIBERTA’ la funzione deve essere creata 
ex-novo in quanto ad oggi non ancora gestita. 
 
 
2. Deve essere gestita la funzione di ‘Ratifica di Applicazione provvisoria misura alternativa’. Per tale 
nuova funzione si può fare riferimento alla funzione di CONCESSIONE che deve essere rinominato 
in ‘Concessione/Ratifica (art. 678) della misura’. L’attuale pagina deve essere pertanto 
parametrizzata in modo da assolvere al duplice utilizzo di una Concessione Ordinaria o di una 
Ratifica (art. 678) della misura. 
 
 
3. Deve essere gestita la funzione di ‘Mancata Ratifica’, (non Conferma), da parte del Tribunale 
dell’ammissione provvisoria della misura alternativa. Sul SIEP si deve procede con la sospensione 
dell’esecuzione della misura alternativa.  
 
 
4. Deve essere gestita la funzione di Revoca dell’Ammissione Provvisoria della Misura Alternativa.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 16/38 
Nell’attuale funzione di revoca presente per le diverse misure alternative, occorre gestire anche i 
provvedimenti del magistrato di Sorveglianza e prevedere in SIEP i nuovi oggetti mappati lato 
Sorveglianza. La pagina deve comunque essere parametrizzata in modo tale da non rendere 
obbligatoria la sezione della Rideterminazione della Pena. 
 
 
5. Deve essere gestita la funzione di Sostituzione della Misura. Si tratta di una funzione da creare ex-
novo per tutte le tipologie di Misura Alternativa. La sostituzione si basa sullo stesso concetto della 
concessione, ma deve tener conto del passaggio da una misura ad un’altra misura alternativa. 
 
 
6. Deve essere gestita la Sospensione delle Pene Accessorie. Infatti, in fase di ammissione di misure 
alternative, il Tribunale può sospendere eventuali pene accessorie, pertanto lato Procura di deve 
procedere ad annotare tale sospensione. Occorre intervenire in fase di Concessione della misura e 
contestualmente implementare la gestione della sospensione nel menù Gestione Pene Accessorie 
» Esecuzione P.A.  e  Gestione Pene Accessorie » Comunicazioni di Aggiornamento. 
 
 
Per ognuno dei casi su elencati vanno considerate le seguenti attività correlate: 
• 
Creazione di nuovi tipi di provvedimento. 
• 
Creazione di nuove tipologie di posizioni giuridiche. 
• 
Creazione di nuovi stati procedimento. 
• 
Creazione di nuovi stampati (template) e aggiornamenti di stampati già in utilizzo. 
• 
Aggiornamento della funzione stato esecuzione. 
• 
Aggiornamento delle statistiche lavoro magistrati. 
• 
Aggiornamento della funzione di riepilogo ispettivo. 
 
Inoltre, per ogni funzione è da considerare sempre la gestione dell’attività di: 
• 
Inserimento

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 17/38 
• 
Modifica 
• 
Cancellazione 
• 
Validazione e stampa 
 
3.4 Adeguamento sistema SIUS d.lgs. 121/2018 (UFFICI MINORENNI) 
 
 
ATTIVITA SULLA BANCA DATI: 
 
- 
Creare un nuovo contenuto per TDSM: Concessione misure penali di comunità/misure alternative 
alla detenzione. Creare gli oggetti ed esiti per tale contenuto. 
 
- 
Creare un nuovo contenuto per TDSM: Cessazione misure penali di comunità / misure alternative 
alla detenzione per venir meno dei presupposti. Creare gli oggetti ed esiti per tale contenuto. 
 
- 
Creare un nuovo contenuto per TDSM: Declaratoria inefficacia ordinanza TDS concessiva misura 
alternativa/misura penale di comunità. Creare gli oggetti ed esiti per tale contenuto. 
 
- 
Per il contenuto ‘Declaratoria Estinzione della Pena’ (C006), aggiungere i nuovi oggetti afferenti al  
D. L.vo 121/18 (gli oggetti devono essere visibili agli uffici minorenni). 
 
- 
Creare un nuovo contenuto per TDSM: Decisione su misure penali di comunità /misure alternative 
per sopravvenienza nuovo titolo. Creare gli oggetti ed esiti per tale contenuto. 
 
- 
Per il contenuto ‘Reclamo su Sopravvenienza Nuovo Titolo’ (C045), aggiungere i nuovi oggetti 
afferenti al  D. L.vo 121/18 (gli oggetti devono essere visibili agli uffici minorenni). 
 
- 
Creare un nuovo contenuto per TDSM: Revoca misure alternative / penali di comunità per 
violazione prescrizioni su proposta del Magistrato. Creare gli oggetti ed esiti per tale contenuto.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 18/38 
 
- 
Creare un nuovo contenuto per UDSM: Applicazione Provvisoria di misura alternativa / penale di 
comunità. Creare gli oggetti ed esiti per tale contenuto. 
 
- 
Creare un nuovo contenuto per UDSM: Dichiarazione di inefficacia / cessazione sospensione 
provvisoria / sostituzione misura alternativa / misura penale di comunità. Creare gli oggetti ed 
esiti per tale contenuto. 
 
- 
Creare un nuovo contenuto per UDSM: Esecuzione misure alternative / penali di comunità. Creare 
gli oggetti ed esiti per tale contenuto. 
 
- 
Creare un nuovo contenuto per UDSM: Proposta revoca / sospensione / sostituzione misura 
alternativa / misura penale di comunità per violazione prescrizioni. Creare gli oggetti ed esiti per 
tale contenuto. 
 
- 
Creare un nuovo contenuto per UDSM: Revoca applicazione provvisoria di misura alternativa / 
penale di comunità. Creare gli oggetti ed esiti per tale contenuto. 
 
- 
Creare un nuovo contenuto per UDSM: Rinvio Esecuzione Misura Alternativa / penale di 
comunità. Creare gli oggetti ed esiti per tale contenuto. 
 
- 
Creare un nuovo contenuto per UDSM: Sospensione e revoca della misura alternativa / penale di 
comunità per cessazione dei presupposti. Creare gli oggetti ed esiti per tale contenuto. 
 
- 
Creare un nuovo contenuto per UDSM: Sopravvenienza nuovo titolo per reati commessi da 
minorenne  – art. 13 D. L.vo 121/18. Creare gli oggetti ed esiti per tale contenuto. 
 
- 
Creare un nuovo contenuto per UDSM: Sopravvenienza nuovo titolo per reati commessi da 
maggiorenne – art. 10 c. 1 D. L.vo 121/18. Creare gli oggetti ed esiti per tale contenuto.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 19/38 
 
CREAZIONE E MODIFICHE DI MASCHERE DELL’APPLICATIVO SIUS 
 
1. Per il nuovo contenuto ‘Concessione misure penali di comunità/misure alternative alla detenzione’, 
ed in corrispondenza dell’oggetto “Affidamento in prova con detenzione domiciliare”, se l’esito è 
‘Concede, sulla maschera di inserimento esito deve essere mostrata una nuova sezione per indicare 
le ore nei giorni della settimana della detenzione domiciliare. 
Un esempio di prospetto potrebbe essere il seguente: 
 
Lunedi   
dalle ore __ alle ore___    
dalle ore __ alle ore___ 
Martedì   
dalle ore __ alle ore___    
dalle ore __ alle ore___ 
Mercoledì 
dalle ore __ alle ore___    
dalle ore __ alle ore___    
Giovedì   
dalle ore __ alle ore___    
dalle ore __ alle ore___    
Venerdì   
dalle ore __ alle ore___    
dalle ore __ alle ore___    
Sabato 
dalle ore __ alle ore___    
dalle ore __ alle ore___    
Domenica 
dalle ore __ alle ore___   
dalle ore __ alle ore___    
 
Prevedere inoltre anche un campo a testo libero dove l’utente può specificare il luogo in cui eseguire la 
detenzione domiciliare. 
 
 
2. Per uffici TDSM e UDSM, nella maschera di iscrizione del procedimento, nella lista dei mittenti 
integrare la seguente voce: 
• 
“esercente la responsabilità genitoriale” 
• 
modificare quella denominata “Richiesta UEPE” in Richiesta UEPE/USSM 
 
 
3. Per il nuovo contenuto Proposta revoca / sospensione / sostituzione misura alternativa / misura 
penale di comunità per violazione prescrizioni, in corrispondenza dell’esito ‘sospende misura e la 
sostituisce con altra’, sulla maschera di inserimento e modifica esito, deve essere mostrata una 
nuova sezione per indicare la nuova misura.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 20/38 
3.5 Adeguamento sistema SIEP d.lgs. 121/2018 (UFFICI MINORENNI) 
 
In riferimento alle Procure Minori (uffici PPM e PGM), si elencano le attività necessarie ai fine 
dell’adeguamento del sistema SIEP al d.lgs. 121/2018 - Misure penali di comunità (UFFICI MINORENNI): 
3.5.1 
Misure penali di comunità 
Per ognuna delle seguenti misure alternative: 
 
• 
Affidamento in prova 
• 
Detenzione domiciliare 
• 
Semilibertà 
• 
Sospensione esecuzione PENA 
 
occorre prevedere la gestione di nuove tipologie di provvedimenti. Tali provvedimenti posso essere 
raggruppati in: 
 
1. Provvedimenti Tribunale di Sorveglianza 
 
• 
Concessione misura penali di comunità 
• 
Dichiarazione di Inefficacia ordinanza concessiva  
• 
Sostituzione Misura art. 8 comma 3  
• 
Revoca misura penale di comunità 
• 
Cessazione / Cessazione su Reclamo Art. 8 comma 4    
• 
Ripristino Rigetto Proposta Revoca Misura 
• 
Reclamo Avverso Decisione Magistrato Sorveglianza Art. 10 Comma 2 
• 
Reclamo Cessazione Prosecuzione Della Misura Art 13 Comma 1 
• 
Declaratoria Estinzione della pena 
 
2. Provvedimenti Magistrato di Sorveglianza  
 
• 
Ammissione Provvisoria 
• 
Dichiarazione di Inefficacia ordinanza concessiva Ammissione provvisoria 
• 
Revoca Ammissione provvisoria 
• 
Sospensione provvisoria art 8 comma 4 (51 Ter) 
• 
Perdita efficacia sospensione provvisoria - art 8 comma 4 (51ter) 
• 
Sospensione provvisoria Sostituzione Misura - art. 8 comma 4  
• 
Perdita efficacia Sospensione Provvisoria Art. 8 comma 4 - Ripristino Misura  
• 
Prosecuzione della misura in corso art. 13 comma 1  
• 
Cessazione della misura in corso art. 13 comma1

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 21/38 
• 
Estensione della misura in corso art. 10 comma 1 
• 
Cessazione della misura in corso art. 10 comma1 
 
 
Per alcune tipologie di provvedimenti si tratta di intervenire andando a creare delle maschere ad hoc e quindi 
di creare tutta la gestione ex-novo della funzione, mentre in altri casi occorre ‘rivedere/rimodulare’ funzioni 
già esistenti. Di seguito vengono esplose le varie funzioni: 
 
Provvedimenti del Tribunale Sorveglianza 
 
 
Per i provvedimenti di Concessione misura penali di comunità (TDS) occorre modificare l’attuale maschera 
di Concessione prevedendo nuovi valori nella combo ‘Oggetto Ordinanza’ la quale deve essere arricchita con 
i nuovi oggetti mappati lato Tribunale di Sorveglianza Minori (TDSM) per il contenuto ‘Concessione misure 
penali di comunità/misure alternative alla detenzione’. 
 
Per Affidamento in prova la lista degli oggetti deve avere in più le seguenti voci: 
- 
Affidamento servizio sociale ex art. 94 DPR 309/90 
- 
Affidamento al servizio sociale art. 4 D. L.vo 121/18 
- 
Affidamento in prova con detenzione domiciliare art. 5 D. L.vo 121/18 
 
Per Detenzione domiciliare la lista degli oggetti deve avere in più le seguenti voci: 
Detenzione domiciliare art. 6 D. L.vo 121/18 
 
Per Semilibertà la lista degli oggetti deve avere in più le seguenti voci: 
Semilibertà art. 7 D. L.vo 121/18 
 
Per Sospensione esecuzione Pena la lista degli oggetti deve avere in più le seguenti voci: 
Esecuzione presso domicilio della pena detentiva – Legge 199/2010 
 
 
Inoltre, sulla maschera va prevista la tipologia di espiazione della prova (es: Collocamento in comunità 
oppure Permanenza in Casa) ed ampliare il campo contenente il luogo della prova. Tali informazioni sono 
da recuperare dall’ordinanza della sorveglianza. 
 
Per la misura alternativa di Affidamento in prova con detenzione domiciliare, la maschera di concessione 
deve riportare una nuova sezione che permetta di memorizzare i giorni della settimana per i quali viene 
concessa la detenzione domiciliare determinati nell’ordinanza di concessione. 
 
Rivedere i template, la posizione giuridica, lo stato procedimento e le estrazioni dati per adattarli alla nuova 
normativa.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 22/38 
La Dichiarazione di Inefficacia ordinanza concessiva è una nuova funzionalità da sviluppare sia per 
minorenni che maggiorenni. Deve essere prevista per tutte le misure alternative e deve essere gestita come 
un provvedimento di Revoca. 
Creare i template, la posizione giuridica, lo stato procedimento ed integrare questo nuovo provvedimento 
nelle estrazioni dati. 
 
 
La Sostituzione della Misura art. 8 comma 3 è una nuova funzionalità da sviluppare ex-novo. Gestire 
l’operazione di inserimento, modifica, cancellazione, stampa e validazione. Creare i template, la posizione 
giuridica, lo stato procedimento ed integrare questo nuovo provvedimento nelle estrazioni dati. 
 
Per i provvedimenti Revoca misura penale di comunità occorre modificare l’attuale maschera di Revoca. 
Deve essere gestita in modo opportuno la sezione della Rideterminazione Pena. Inoltre, per ogni tipologia 
di misura devono essere rivisti tutti i conteggi sulla pena residua. Rivedere i template, la posizione 
giuridica, lo stato procedimento e le estrazioni dati per adattarli alla nuova normativa. 
 
 
Per la Cessazione /Cessazione su Reclamo Art. 8 comma 4 è già prevista una maschera di gestione, ma 
deve essere modificata per prevedere le due ipotesi di cessazione della misura in corso d’espiazione, ossia 
se del Tribunale oppure Sorveglianza. In ogni caso la funzione deve essere gestita in tutte le misure. Rivedere 
i template, la posizione giuridica, lo stato procedimento e le estrazioni dati per adattarli alla nuova 
normativa. 
 
Per i provvedimenti di Ripristino- Rigetto Proposta Revoca Misura è già prevista una maschera di gestione, 
ma deve essere modificata per prevedere i nuovi oggetti della Sorveglianza. La gestione comunque va rivista 
per l’adeguamento alla nuova normativa. 
 
Occorre rivedere tutte le fasi gestionali: I template, la posizione giuridica, lo stato procedimento e le 
estrazioni dati. 
 
In ogni maschera prevedere sempre modifica, valida, stampa e torna indietro. 
 
 
Per la gestione del Reclamo avverso la decisione del Magistrato di sorveglianza occorre creare una nuova 
funzione nel menù Decisioni Sorveglianza ed è relativa ai minorenni. Le decisioni della sorveglianza possono 
essere: 
Accoglie reclamo e estende misura con modalità minorenni 
Dispone cessazione della sospensione e restituzione atti al PM 
 
La funzione deve essere simile all’ attuale CESSAZIONE SU RECLAMO 51 BIS. Creare i template, la posizione 
giuridica, lo stato procedimento ed integrare questo nuovo provvedimento nelle estrazioni dati. 
In ogni maschera prevedere sempre modifica, valida, stampa e torna indietro.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 23/38 
 
 
Per la gestione del Reclamo Cessazione Prosecuzione Della Misura Art 13 Comma 1 occorre creare una 
nuova funzione. La funzione deve essere simile all’ attuale CESSAZIONE SU RECLAMO 51 BIS. Creare i 
template, la posizione giuridica, lo stato procedimento ed integrare questo nuovo provvedimento nelle 
estrazioni dati. In ogni maschera prevedere sempre modifica, valida, stampa e torna indietro.  
 
 
Per la Declaratoria Estinzione della pena occorre creare una nuova funzione. Deve essere prevista per tutte 
le misure. È una funzione da creare sia per i minorenni che per i maggiorenni. In merito a ciò occorre rivedere 
anche la funzione di Definizione del Procedimento che dovrebbe essere aggiornata nella combo degli 
oggetti di definizione. Creare i template, la posizione giuridica, lo stato procedimento ed integrare questo 
nuovo provvedimento nelle estrazioni dati. 
In ogni maschera prevedere sempre la funzionalità di modifica, valida, stampa e torna indietro. 
 
 
 
Provvedimenti dell’ufficio Sorveglianza 
 
Prevedere la funzione di Ammissione Provvisoria, ad oggi presente per affidamento in prova e detenzione 
domiciliare, per tutte le altre misure (Differimento e Semilibertà). La maschera deve essere simile alla 
maschera attuale presente per l’Ammissione Provvisoria dell’Affidamento in Prova. 
Occorre intervenire su tutte le fasi gestionali: I template, la posizione giuridica, lo stato procedimento e le 
estrazioni dati. 
 
In ogni maschera prevedere sempre la funzionalità di modifica, valida, stampa e torna indietro. 
 
 
La Dichiarazione di Inefficacia Ordinanza concessiva Applicazione provvisoria è una nuova funzionalità 
da implementare sia per minorenni che maggiorenni e va prevista per tutte le tipologie di misure alternative. 
La dichiarazione di Inefficacia deve essere trattata alla stessa stregua di una Revoca di Misura.  
 
Occorre intervenire su tutte le fasi gestionali: I template, la posizione giuridica, lo stato procedimento e le 
estrazioni dati. 
 
In ogni maschera prevedere sempre la funzionalità di modifica, valida, stampa e torna indietro. 
 
 
La funzione di Revoca Ammissione provvisoria della misura è una nuova funzionalità da implementare per 
minorenni e va prevista per tutte le tipologie di misure alternative applicate provvisoriamente. 
Occorre intervenire su tutte le fasi gestionali: I template, la posizione giuridica, lo stato procedimento e le 
estrazioni dati. 
In ogni maschera prevedere sempre la funzionalità di modifica, valida, stampa e torna indietro.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 24/38 
 
I provvedimenti di Sospensione provvisoria art. 8 comma 4 (51 ter) devono essere gestiti andando a 
rimodulare l’attuale funzione di ‘Sospensione provvisoria 51 ter’. Devono essere riviste tutte le maschere di 
inserimento, modifica ed intervenire su tutte le fasi gestionali, ossia i template, la posizione giuridica, lo 
stato procedimento e le estrazioni dati. 
 
 
 
I provvedimenti di Perdita efficacia sospensione provvisoria - art 8 comma 4 (51ter) devono essere gestiti 
andando a rimodulare l’attuale funzione di ‘Cessazione Sospensione Provvisoria 51 Ter’. Devono essere 
riviste tutte le maschere di inserimento, modifica ed intervenire su tutte le fasi gestionali, ossia i template, 
la posizione giuridica, lo stato procedimento e le estrazioni dati. 
 
 
Per i provvedimenti di Sospensione provvisoria - Sostituzione Misura Art. 8 comma 4 e Perdita efficacia 
Sospensione sostituzione ripristino Misura Art. 8 comma 4 occorre creare una nuova gestione. Tale 
gestione deve essere prevista per ogni tipologia di misura alternativa. Creare i template, la posizione 
giuridica, lo stato procedimento ed integrare questo nuovo provvedimento nelle estrazioni dati. 
 
 
Per la gestione della prosecuzione della misura in corso art. 13 comma 1 occorre prevedere una nuova 
funzione. Tale funzione va creata per tutte le misure alternative (PER I MINORENNI) e deve essere simile 
alla funzione attualmente prevista per i maggiorenni nel menù Decisioni Sorveglianza/Prosecuzione Della 
Misura In Corso 51 Bis. Creare i template, la posizione giuridica, lo stato procedimento ed integrare questo 
nuovo provvedimento nelle estrazioni dati. 
 
 
Per la gestione della Cessazione della misura in corso art. 13 comma 1 occorre prevedere una nuova funzione. 
Tale funzione va creata per tutte le misure alternative (PER I MINORENNI) e deve essere simile alla funzione 
attualmente prevista per i maggiorenni nel menù Decisioni Sorveglianza/Cessazione Della Misura In Corso 
51 Bis. Creare i template, la posizione giuridica, lo stato procedimento ed integrare questo nuovo 
provvedimento nelle estrazioni dati. 
 
Per la gestione della prosecuzione della misura in corso art. 10 comma 1 occorre prevedere una nuova 
funzione. Tale funzione va creata per tutte le misure alternative (PER I MAGGIORENNI) e deve comportarsi 
come quella attuale prevista per i maggiorenni adulti (vedi funzione). Creare i template, la posizione 
giuridica, lo stato procedimento ed integrare questo nuovo provvedimento nelle estrazioni dati. 
 
 
Per la gestione della Cessazione della misura in corso art. 10 comma 1 occorre prevedere una nuova 
funzione. Tale funzione va creata per tutte le misure alternative (PER I MAGGIORENNI) e deve comportarsi

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 25/38 
come quella attuale prevista per i maggiorenni. Creare i template, la posizione giuridica, lo stato 
procedimento ed integrare questo nuovo provvedimento nelle estrazioni dati. 
 
 
3.5.2 
 Emissione Ordine di Esecuzione con Decreto di Sospensione 
Si richiede di intervenite sulla funzione attuale di emissione di ordine di esecuzione con decreto di 
sospensione (menù Sospensione Esecuzione ex art. 656 c.p.p.) per adeguarne l’emissione al D.LGS. 
121/2018. 
 
IMPLEMENTAZIONI PER MINORENNI 
(Art. 8 comma 1 d.lgs. 121/18) 
 
Legislazione (Art.8 comma 1 d.lgs. 121/18) 
L'adozione della misura penale di comunità può essere disposta su richiesta dell'interessato, se maggiorenne, 
o del suo difensore; non può essere disposta d'ufficio. Nel caso in cui il condannato non abbia compiuto la 
maggiore età, la richiesta è presentata dal difensore o dall'esercente la responsabilità genitoriale. L'adozione 
della misura può essere proposta dal pubblico ministero o dall'ufficio di servizio sociale per i minorenni. 
 
In corrispondenza di tale funzione, per un soggetto MINORENNE (per questa casistica per il minore si sta 
chiedendo la sospensione dell’espiazione per l’adozione di una misura penale di comunità), il sistema deve 
proporre un nuovo sottomenù mostrando all’utente la scelta di proseguire tra: 
 
• 
Emissione decreto di sospensione ex art. 656 comma 5 c.p.p. (funzione attualmente presente ma 
da rimodulare per la gestione da minorenni e per quanto riportato al par. successivo relativo Art.10 
comma 5 d.lgs. 121/18) 
• 
Emissione decreto sospensione art. 8 comma 1 d.lgs. 121/18  
 
 
Per l’emissione del decreto sospensione art. 8 comma 1 d.lgs. 121/18 occorre prevedere una nuova sezione 
in cui va gestita l’informazione relativa all’entità da cui viene proposta l’adozione della misura, ossia: 
   
• 
Dal difensore 
• 
Dall’esercente la responsabilità genitoriale 
• 
D’ufficio 
• 
Dal pubblico ministero 
• 
Dall’ufficio di servizio sociale per i minorenni 
 
L’emissione del decreto di sospensione ex art. 656 comma 5 c.p.p., in caso di minorenni, deve basarsi sulla 
stessa maschera utilizzata attualmente per i soggetti maggiorenni a meno degli oggetti ed inoltre vanno 
rivisti tutti i template già esistenti per renderli parametrici ed adattarli alla nuova normativa.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 26/38 
 
 
IMPLEMENTAZIONI PER MAGGIORENNI (giovani adulti) 
(perdita modalità espiazione previste per i minorenni (Art.10 comma 5 d.lgs. 121/18)) 
 
Legislazione (Art.10 comma 5 d.lgs. 121/18) 
Se il condannato per reati commessi da minorenne abbia fatto ingresso in un istituto per adulti in custodia 
cautelare o in espiazione di pena, per reati commessi dopo il compimento del diciottesimo anno di età, non si fa 
luogo all’esecuzione secondo le norme e con le modalità previste per i minorenni. 
 
In ottemperanza a tale legislazione, in corrispondenza dell’emissione del decreto di sospensione ex art. 
656 comma 5 c.p.p., per un soggetto MAGGIORENNE (età >18 e < di anni 25), all’atto dell’emissione 
dell’Ordine di Esecuzione con sospensione (legge 165/98) occorre inserire un avviso in Popup che permetta 
all’utente di scegliere di: 
 
- 
NON Proseguire con l’esecuzione secondo le norme e con le modalità previste per i minorenni. 
- 
PROSEGUIRE con l’esecuzione secondo le norme e con le modalità previste per i minorenni. 
 
In caso di scelta sul NON PROSEGUIRE (Non si fa luogo all’esecuzione secondo le norme e con le modalità 
previste per i minorenni) l’utente prosegue emettendo ordine di esecuzione con decreto di sospensione 
ordinario previsto per gli adulti. 
 
In caso di scelta di PROSEGUIRE (si fa luogo all’esecuzione secondo le norme e con le modalità previste per 
i minorenni) allora il sistema deve mostrare una nuova maschera di emissione dell’Ordine di Esecuzione con 
sospensione (legge 165/98) basata su quella attualmente presente per gli adulti e rimodulata per i minorenni. 
Occorre tener conto poi di tutte le fasi gestionali: I template, la posizione giuridica, lo stato procedimento e 
le estrazioni dati. 
 
 
 
Per la gestione dell’Esercente Responsabilità Genitoriale occorre prevedere una funzione ex-novo per 
permettere all’utente di inserire i dati di chi esercita la responsabilità genitoriale nei confronti del soggetto 
minore. 
 
 
3.5.3 
Restituzione atti per ulteriore corso 
Legislazione  
Articolo 10 comma 4 
Quando l’ordine di esecuzione per il reato commesso da maggiorenne non può essere sospeso, il magistrato di 
sorveglianza per i minorenni trasmette gli atti al pubblico ministero che ha emesso l’ordine per l’ulteriore corso 
dell’esecuzione secondo le norme e con le modalità previste per i maggiorenni.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 27/38 
Per i maggiorenni (giovani adulti, età >18 e < 25 anni), nell’attuale menù Ordini di Esecuzione/Scarcerazione 
» Sospensione Esecuzione ex art. 656 c.p.p. aggiungere un nuovo tabulatore “Restituzione Atti per ulteriore 
corso (Art. 10 comma 4)”. 
 
In corrispondenza di tale funzione creare una nuova maschera per inserire l’annotazione della restituzione 
degli atti dalla Sorveglianza. La maschera può essere simile a quella attualmente utilizzata per la Revoca 
Sospensione Esecuzione ex art. 656 c.p.p. (Reiezione Istanza).  
 
Per la funzione occorre prevedere tutte le fasi gestionali di modifica, cancellazione e stampa prevedendo 
nuovi stampati. 
 
 
3.5.4 
Annotazioni su decreto di sospensione 
Per i maggiorenni (giovani adulti, età >18 e < 25 anni), nell’attuale menù Ordini di Esecuzione/Scarcerazione 
» Sospensione Esecuzione ex art. 656 c.p.p. aggiungere un nuovo tabulatore “Annotazione Art. 10 comma 
1”. 
 
In corrispondenza di tale funzione creare una nuova maschera per inserire l’annotazione riguardante le 
decisioni della sorveglianza in merito alle richieste interlocutorie di: 
 
• 
Richiesta estensione della Misura Penale di Comunità in corso per sopravvenienza nuovo Titolo- art. 
10 c 1 D.lgs. 121/18 
• 
Richiesta cessazione della Misura Penale di Comunità in corso per sopravvenienza nuovo Titolo- art. 
10 c 1 D.lgs. 121/18 
 
 
In corrispondenza di tale funzione creare una nuova maschera per inserire l’annotazione della Sorveglianza.  
 
Per la funzione occorre prevedere tutte le fasi gestionali di modifica, cancellazione e stampa prevedendo 
nuovi stampati. 
 
 
 
3.5.5 
istruttorie/richieste  
Nel menù verticale Istruttorie/Richieste, introdurre una nuova sezione denominata “Trasmissione Richieste 
alla Magistratura di Sorveglianza”. 
 
In questa sezione devono essere presenti tre sotto menù:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 28/38 
1. Richieste - art. 51 bis l. 354/75  (è la funzione attualmente presente nominata Trasmissione Atti / 
Richieste ex art. 51 bis che deve essere ‘migrata’ e ‘rinominata in questa nuova sezione) 
2. Richieste ex art. 13 c 1 D.lgs. 121/18 
3. Richieste ex art. 10 c 1 D.lgs. 121/18 
4. Reato ostativo art. 10 co.4 D.lgs. 121/18 
 
Trasmissione Richieste alla Magistratura di  Sorveglianza 
Richieste art. 51 bis L. 374/75  
Richieste ex art. 10 c 1 D.lgs. 
121/18 
Richieste ex art. 13 c 1 D.lgs. 
121/18 
Reato ostativo art. 10 co.4 D.lgs. 
121/18 
 
 
 
 
La maschera per la gestione è quella già esistente per gestire le “Richieste - art. 51 bis l. 354/75”. 
Nella combo del campo ‘Oggetto Atto’ devono essere aggiunte le seguenti voci: 
 
• 
Richiesta Cessazione Misura Penale di Comunità per sopravvenienza nuovo Titolo - art. 13 c 1 D.lgs. 
121/18 
• 
Richiesta prosecuzione della Misura Penale di Comunità in corso per sopravvenienza nuovo Titolo- 
art. 13 c 1 D.lgs. 121/18 
• 
Richiesta Estensione Misura Penale di Comunità per sopravvenienza nuovo Titolo - art. 10 c 1 D.lgs. 
121/18 
• 
Richiesta Cessazione della Misura Penale di Comunità in corso per sopravvenienza nuovo Titolo- art. 
10 c 1 D.lgs. 121/18 
 
 
Gestire l’operazione di inserimento, modifica, cancellazione, stampa e validazione. Creare i template. 
 
 
3.5.6 
Istanza 
La gestione dell’istanza va modificata e va prevista per tutti i decreti di sospensione. Il sistema deve 
visualizzare, l’eventuale istanza, pervenuta/depositata dalle parti. 
 
Sulla pagina di emissione del decreto di sospensione deve essere mostrato il dettaglio dell’istanza, ma solo 
se è attinente all’oggetto del decreto di sospensione che sto emettendo.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 29/38 
3.5.7 
Gestione Notifiche 
Per la gestione del decreto di sospensione occorre ampliare i soggetti che possono presentare l’istanza. La 
maschera deve proporre due gestioni:   
 
• 
Ordine di esecuzione con sospensione (legge 165/98) (la gestione rimane invariata) 
• 
Ordine Esecuzione con contestuale Sospensione (D.L.vo 121/2018) 
 
Selezionando la voce “Notifiche” sulla maschera vanno inserite due nuove voci: 
 
• 
“Esercente Responsabilità Genitoriale”;  
• 
“U.S.S.M. Ufficio Servizio Sociale Minorenni”. 
 
Il sistema visualizza i dati dell’ufficio destinatario della notifica già presenti nell’applicativo e propone la 
maschera che permette di annotare la data di notifica, con la possibilità di indicare una diversa autorità. 
 
La gestione difensore rimane invariata. 
La gestione delle scadenze rimane invariata, ma va integrata con le due nuove autorità. 
Devono essere variate ed integrate tutte le maschere di gestione delle notifiche del decreto. 
 
Inoltre: 
• 
Modificare le stampe dei riepiloghi 
• 
Integrare la funzione del Riepilogo ispettivo 
• 
Integrare la funzione del Lavoro magistrati  
 
Prevedere gestione foglio complementare casellario (l’eventuale modifica va verificata con casellario). 
 
 
 
3.6 Altri interventi per SIUS minori 
 
 
1. Si chiede di modificare, relativamente al contenuto “Proposta di aggravamento per trasgressione 
obblighi misura di sicurezza”, l’esito “Sostituisce libertà vigilata con detenzione in IPM” con 
“Sostituisce misura di sicurezza con detenzione in IPM”. 
 
 
2. Gestire la funzione “generazione modelli” (sia ordinanze che decreti) per includere sia TDS che MDS.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 30/38 
 
 
 
 
3. Si chiede di aggiornare le Statistiche in modo che non visualizzino gli oggetti che risultano cancellati.  
 
 
3.7 Argomentazioni sospese 
 
• 
In riferimento al sistema SIUS, rimane in sospeso (per quesito alla Sorveglianza) il punto 7 
del documento Minori_Modifiche_05_12.docx relativo all’art. 10 del  d.lgs. 121/2018. 
 
• 
Art. 12 - Trasferimento esecuzione Misura Alternativa per compimento del venticinquesimo 
anno 
 
 
3.8 Moduli sw  
L’elenco dei moduli software sarà indicato puntualmente nel successivo documento di Specifiche di 
Intervento 
3.9 Architettura  
N.A. 
3.10 Interfacce utente 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 31/38 
3.11Basi dati 
4 
N.A. 
4.1 WEB services 
N.A. 
4.2 XSD 
N.A. 
4.3 Configurazione 
N.A. 
4.4 Tutorial 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 32/38 
5 Piano delle attività 
5.1 Ciclo di sviluppo 
La metodologia utilizzata in questo obiettivo sarà Agile e, in particolare, si adotterà Scrum. 
Nell’immagine che segue riportiamo un diagramma delle attività ed oggetti previsti dalla metodologia 
 
La metodologia prevede i seguenti Ruoli: 
 
Ruolo 
Responsabilità 
Ownership 
Agile Team 
Realizza il Prodotto 
Decide le modalità di implementazione e si organizza in maniera 
autonoma 
RTI 
Scrum Master 
Ruolo di facilitatore 
Lavora per rimuovere gli ostacoli che il Team incontra nel 
raggiungere gli obiettivi dello Sprint 
Solitamente un membro del Team 
RTI 
Product Owner 
Decide le caratteristiche del prodotto da realizzare 
Deve avere visione, autorità e disponibilità 
Responsabile del product backlog 
Giustizia 
 
I ruoli qui elencati sono da intendersi come ruoli operativi poiché il governo della fornitura è delegato ai ruoli 
descritti nel piano della qualità generale. 
 
L’approccio prevede i seguenti oggetti

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 33/38 
Oggetto 
Descrizione 
Responsabilità 
User Story 
È l’elemento base dello scrum. Contiene le 
informazioni necessarie per la realizzazione 
del software e la sua verifica (criteri di 
accettazione, oggetti a corredo, ecc…).  
La User Story deve essere, per quanto 
possibile, indipendente, valutabile e piccola 
Stakeholder, Agile Team, Product 
Owner 
Product Backlog 
L’elenco prioritizzato delle User Stories 
Product Owner 
Sprint Backlog 
Viene definito nello Sprint Planning e 
contiene la porzione di Product Backlog che 
deve essere realizzata nello sprint. 
Avviato lo sprint non è modificabile 
Product Owner 
Agile Team 
Prodotto 
(incrementato) 
L’oggetto finale di uno sprint 
Agile Team 
Epic 
Sono delle User Stories di alto livello che, 
normalmente, vengono utilizzate dove non 
si hanno informazioni sufficienti per 
specializzare la situazione 
Stakeholder, Agile Team, Product 
Owner 
 
Infine, sono previste le seguenti riunioni/attività 
Riunione 
Scopo 
Durata 
Partecipanti 
Sprint Planning Riunione iniziale di ciascuno sprint nel quale 
viene condiviso e pianificato l’output dello 
sprint. È in questa fase che viene definito lo 
Sprint Backlog 
0,75gg (per 
sprint di 3 
settimane) 
Product Owner 
Agile Team 
Scrum Master 
Daily Scrum 
Riunione del Team nel quale si fa il punto della 
situazione e si prendono le decisioni per le 
future attività 
15 minuti 
Agile Team 
Scrum Master 
Sprint Review 
Presentazione del lavoro fatto nel corso dello 
Sprint 
0,75gg (per 
sprint di 3 
settimane) 
Product Owner 
Agile Team 
Scrum Master 
Stakeholder 
Sprint 
Retrospective 
Riunione utile alla discussione dell’andamento 
dello Sprint appena terminato e 
all’identificazione delle attività di 
miglioramento 
0,75gg (per 
sprint di 4 
settimane) 
Agile Team 
Scrum Master 
 
 
Nel seguito è descritto l’approccio operativo  
L’obiettivo, per la peculiarità del progetto stesso, seguirà un ciclo di vita ad hoc secondo quanto previsto dal 
PQG.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 34/38 
Fase 
Prodotto di fase 
Criterio di uscita 
Sprint 0 (Definizione) 
Product 
Backlog 
su 
strumento 
di 
condivisione proposto dal RTI (Jira) 
Attivazione 
 
Sprint 1..n 
Codice 
sorgente 
del 
prodotto 
complessivo aggiornato all’iterazione 
Piano di test per quanto realizzato 
nell’iterazione 
Modulo di conteggio (FP) per quanto 
realizzato nell’iterazione 
Consegna dei prodotti di fase 
 
Approvazione del collaudo 
dell’iterazione 
Sprint di chiusura e 
collaudo 
Specifica dei requisiti dell’obiettivo  
Codice 
sorgente 
del 
prodotto 
complessivo 
Piano di test per il collaudo complessivo 
Modulo di conteggio (FP) per quanto 
realizzato nell’iterazione 
Documentazione utente 
Consegna dei prodotti di fase 
 
Approvazione del collaudo 
dell’iterazione 
 
Relativamente alla consuntivazione degli obiettivi si propone di procedere come riportato nella tabella che 
segue 
Fase 
Effort Riconosciuto 
Criterio di uscita 
Definizione 
10% dell’intero obiettivo stimato 
Attivazione 
Iterazione (Lotto) 
Iterazione 0 
0% 
Sprint review 
Iterazione 1..n 
60% di quanto effettivamente realizzato 
nell’iterazione 
Approvazione dei casi d’uso e 
dei casi di test (Verifica di 
conformità): 20% del realizzato 
 
Consegna dei prodotti di fase: 
20% del realizzato 
 
Approvazione del collaudo 
dell’iterazione: 20% del 
realizzato 
Iterazione di 
chiusura 
60% di quanto effettivamente realizzato 
nell’iterazione 
Approvazione dei casi d’uso e 
dei casi di test (Verifica di 
conformità): 20% del realizzato 
 
Consegna dei prodotti di fase: 
20% del realizzato

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 35/38 
Approvazione del collaudo 
dell’iterazione: 20% del 
realizzato 
Collaudo 
99,5% dei FP effettivamente realizzati al 
netto di quanto già fatturato nella fase di 
definizione e delle successive iterazioni 
Accettazione 
(verifica di conformità) 
Avvio in Esercizio 
Sblocco della componente dipendente 
dagli indicatori di prestazioni 
Valutazione qualità del 
software (verifica di 
conformità) 
 
Si riporta di seguito un esempio ipotizzando 4 Sprint: 
 
 
 
5.2 Piano delle attività 
Il Piano di Lavoro sviluppa su un totale di 10 sprint della durata di 3 settimane ciascuno così suddivisi: 
1. Sprint 0: corrispondente alla fase di definizione nel quale sarà predisposto il product backlog 
condiviso attraverso il sistema Jira 
2. Sprint 1-8: sprint di sviluppo nel quale sarà realizzato il sistema complessivo attraverso l’approccio 
iterativo tipico dell’approccio scrum 
3. Sprint 9: sprint di rilascio e collaudo complessivo del sistema nel quale saranno verificate le 
funzionalità del sistema complessivo e saranno prodotti tutti gli artefatti necessari al passaggio in 
esercizio 
5.3 Gantt 
L’articolazione delle attività previste per l'intervento si sviluppa attraverso 10 sprint come precedentemente 
descritto. 
 
FP
Note
Consuntivi
Totale Preventivo
90
A
Definizione/Sprint 0
9
10 % Del Totale Preventivo
B
Sprint 1
19,2
60 % Del Consuntivo Sprint 1
32
C
Sprint 2
16,8
60 % Del Consuntivo Sprint 1
28
D
Sprint 3
21
60 % Del Consuntivo Sprint 1
35
E
Totale Consuntivo
95
F
Collaudo
29
99,5% dei FP effettivamente realizzati al netto di quanto 
già fatturato nella fase di definizione e delle successive 
iterazioni = 99,5%  di (E-(B+C+D)-A)
Totale (A+B+C+D+F)
95

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 36/38 
5.4 Vincoli 
N.A. 
 
5.5 Luogo di lavoro 
 
Le attività saranno espletate presso le sedi del RTI o presso la sede della DGSIA.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 37/38 
6 Dimensionamento 
6.1 Stima dell'effort previsto 
 
La stima prevista a preventivo dell’intero obiettivo è di 229.149 € 
 
 
6.2 Dettaglio costi 
Di seguito si riporta il dettaglio dei costi a preventivo: 
 
 
 
 
ADD - S v i l u p p o   N u o v e   F u n z i o n i 
  
  
  
    
Complessità 
  
Function Types 
  
Low 
Avg 
High 
Function 
  
  
  
    
quantità 
peso 
quantità 
peso 
quantità 
peso 
Point 
External Input 
    
0 
3 
0 
4 
119 
6 
714 
External Output 
  
0 
4 
0 
5 
37 
7 
259 
External Inquiry 
    
0 
3 
0 
4 
30 
6 
180 
Internal Logical File 
  
2 
7 
0 
10 
0 
15 
14 
External Interface 
File 
  
0 
5 
0 
7 
0 
10 
0 
  
  
  
      
  
  
  
  
Totale Function Point (FP) 
1.167 
ADD 
 
 
 
 
 
 
 
 
 
CHGA - F u n z i o n i   M o d i f i c a t e  (After) 
  
  
  
    
Complessità 
  
Function Types 
  
Low 
Avg 
High 
Function 
  
  
  
    
quantità 
peso 
quantità 
peso 
quantità 
peso 
Point 
External Input 
    
0 
3 
0 
4 
52 
6 
312 
External Output 
  
0 
4 
0 
5 
15 
7 
105 
External Inquiry 
    
0 
3 
0 
4 
13 
6 
78 
Internal Logical File 
  
0 
7 
0 
10 
0 
15 
0 
External Interface 
File 
  
0 
5 
0 
7 
0 
10 
0 
  
  
  
      
  
  
  
  
Totale Function Point (FP) 
495 
CHGA

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
 
 
 
SIUT-GEN-SC-1.0-20191004 
Scheda 
Intervento 
n° 
9 
- 
Adeguamento SIES al DLGS 123_2018 e 121_2018 
Ver. 1.0 del 04/10/2019 
Pag. 38/38 
DEL - F u n z i o n i   E l i m i n a t e 
  
  
  
    
Complessità 
  
Function Types 
  
Low 
Avg 
High 
Function 
  
  
  
    
quantità 
peso 
quantità 
peso 
quantità 
peso 
Point 
External Input 
    
0 
3 
0 
4 
0 
6 
0 
External Output 
  
0 
4 
0 
5 
0 
7 
0 
External Inquiry 
    
0 
3 
0 
4 
0 
6 
0 
Internal Logical File 
  
0 
7 
0 
10 
0 
15 
0 
External Interface 
File 
  
0 
5 
0 
7 
0 
10 
0 
  
  
  
      
  
  
  
  
Totale Function Point (FP) 
0 
DEL