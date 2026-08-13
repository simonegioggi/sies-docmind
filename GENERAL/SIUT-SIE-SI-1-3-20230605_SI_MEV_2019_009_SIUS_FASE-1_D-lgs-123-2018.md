---
uniqueName: siut-sie-si-1-3-20230605simev2019009siusfase-1d-lg
displayName: "SIUT SIE SI 1 3 20230605 SI MEV 2019 009 SIUS FASE 1 D lgs 123 2018"
category: "GENERAL"
tags: []
---

# SIUT-SIE-SI-1.3-20230605_SI_MEV_2019_009_SIUS_FASE-1_D.lgs.123-2018

> **File originale:** `MEV/SCHEDA_009/SIUT-SIE-SI-1.3-20230605_SI_MEV_2019_009_SIUS_FASE-1_D.lgs.123-2018.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
 
Specifiche Intervento MEV 
2019_009_SIUS_FASE_1-D.lgs.123/2018 
 
 
 
 
 
 
 
 
Versione 1.3 del 05/06/2023

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 2/68 
 
 
 
 
 
 
 
 
Il presente documento è stato redatto con la collaborazione 
del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA 
S.r.l. nell’ambito del contratto CIG 73479643B7 per lo 
“Sviluppo del Sistema Informativo Unitario Telematico, la 
manutenzione degli attuali sistemi dell’area Penale del 
Ministero della Giustizia e servizi correlati. Lotto 1”.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 3/68 
 
 
 
Approvazioni 
 
Nominativo 
Elaborato da 
Umberto Mignogna 
Verificato da 
Vito Bufi 
Approvato da 
Paolo Ceccanti 
Data approvazione 
05/06/2023 
Livello di riservatezza 
L3 
 
Elenco versioni 
Versione 
Data  
Motivo 
Modifica 
1.0 
07/07/2020 
 
Prima Emissione 
1.1 
24/09/2020 
 
Seconda Emissione 
Revisione 
a 
seguito 
della 
nota 
dell’Amministrazione del 04/09/2020 - Riscontro 
Scheda 2019_9 Fase 1.docx.pdf_signed.pdf (SIUS) 
e nota dell’Amministrazione del 17/09/2020 -
Integrazione 
Scheda 
Sies 
2019_9(1).docx.pdf_signed.pdf (SIEP) 
Integrazioni SIUS 
- 
Nel cap.  2 a pag. 11 sostituita la parola 
‘Giudice di sorveglianza’ con ‘Tribunale di 
sorveglianza’; 
- 
 Al par. 4.2.1 alla pag. 20 è stato 
esplicitato che la scelta dell’oggetto non è 
obbligatoria; 
- 
 Al par. 4.2.2 alla pag. 27 modificata la fig.
6 e la sua descrizione, eliminando 
l’obbligatorietà in corrispondenza del 
difensore e rimossa la sezione per 
l’indicazione del Tribunale Competente;

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 4/68 
 
 
- 
 Al par. 4.2.3 a pag.29 eliminato la frase “, 
entro i termini previsti,” riferita al Decreto 
di Designazione; 
- 
Al par. 4.2.3 a pag. 31 eliminata la frase “Il 
rigetto dell’istanza è sempre subordinato, 
pertanto, ad una valutazione di tipo 
collegiale”;  
- 
Al par. 4.2.3 a pag. 32 modificata la frase 
“deve essere inibita la fase di validazione, 
deposito e trasmissione”; 
- 
Al par. 4.2.4 a pag. 33 esplicitata la non 
obbligatorietà per la data di esecutività; 
- 
Al par. 4.2.5 rivista tutta la gestione del 
procedimento in caso di emissione 
Ordinanza 
di 
conferma 
Decisione 
Magistrato Relatore; 
- 
Al par. 4.2.6 alle pag. 40 e 41 è stata 
prevista la suddivisione tra le statistiche di 
‘Trasmette Atti al Presidente’ e di 
‘Ordinanze non Emesse’; 
- 
 Al par. 4.2.8 e 4.2.9 eliminata la dicitura 
’URGENTE’ nella figura del template di 
esempio e specificato che la statistica è 
solo per TDS e TDSM; 
- 
 
Integrazioni SIEP 
- 
Al par. 4.3.1 alla pag. 56 è stata introdotta 
la richiesta di sdoppiare le descrizioni tra 
SIUS e SIEP in riferimento agli oggetti per

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 5/68 
 
 
il ‘Concessione misure alternative (art. 
678 comma 1-ter c.p.p.)’; 
- 
Al par. 4.3.1 alla pag. 56 recepito 
l’allineamento della Label del pulsante in 
Ammissione/Applicazione provvisoria; 
- 
Al par. 4.3.1.1 alla pag. 59, previsto in 
campo esito ordinanza; Aggiornate anche 
la fig. 41 a pag. 63, la fig. 45 pag. 68; 
- 
Alle pag. 60, 64, 68, 77, 82, 83, 86 è stato 
esplicitato che le interfacce devono 
contenere i tasti funzionali di Torna 
Indietro, modifica, cancella e validazione; 
- 
Al par. 4.3.2.2 alla pag. 74 recepito 
l’allineamento della Label del pulsante in 
Concessione/Ratifica; 
- 
Al par. 4.3.3 a pag. 88 recepito quanto
richiesto per la funzione di statistiche 
lavoro magistrati e riepilogo ispettivo; 
- 
Al par. 4.7.12 aggiunta la gestione del 
mapping in tabella cg_ref_codes per
l’integrazione per SIEP di cui al punto 1; 
1.2 
20/04/2023 
 
- 
Revisione di tutto il cap. 4.2; 
1.3 
05/06/2023 
 
- 
Modificato 
parag. 
4.2.7 
per 
aggiornamenti pervenuti via PEC

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 6/68 
 
 
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
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 7/68 
 
 
INDICE DEI CONTENUTI 
  
1 
INTRODUZIONE ............................................................................................................................... 9 
1.1 
SCOPO DEL DOCUMENTO .......................................................................................................................... 9 
1.2 
RIFERIMENTI ........................................................................................................................................... 9 
1.3 
GLOSSARIO ........................................................................................................................................... 10 
1.3.1 
DEFINIZIONI ...................................................................................................................................... 10 
1.3.2 
ACRONIMI E ABBREVIAZIONI ................................................................................................................ 10 
2 
DEFINIZIONE DELL’OBIETTIVO ........................................................................................................ 12 
2.1 
CONVENZIONI ....................................................................................................................................... 14 
2.2 
ELENCO REQUISITI ................................................................................................................................. 14 
2.2.1 
REQ-SIE-009-01 (SIUS) ................................................................................................................... 14 
2.2.2 
REQ-SIE-009-02 (SIUS) ................................................................................................................... 14 
2.2.3 
REQ-SIE-009-03 (SIUS) ................................................................................................................... 15 
2.2.4 
REQ-SIE-009-04 (SIUS) ................................................................................................................... 15 
2.2.5 
REQ-SIE-009-05 (SIUS) ................................................................................................................... 15 
2.2.6 
REQ-SIE-009-06 (SIUS) ................................................................................................................... 15 
2.2.7 
REQ-SIE-009-07 (SIUS) ................................................................................................................... 15 
2.2.8 
REQ-SIE-009-08 (SIUS) ................................................................................................................... 15 
2.2.9 
REQ-SIE-009-09 (SIUS) ................................................................................................................... 16 
2.2.10 
REQ-SIE-009-10 (SIUS) ................................................................................................................... 16 
2.2.11 
REQ-SIE-009-11 (SIUS) ................................................................................................................... 16 
3 
ARCHITETTURA DEL SISTEMA ......................................................................................................... 17 
3.1 
ARCHITETTURA ...................................................................................................................................... 17 
3.2 
WEB SERVICES ...................................................................................................................................... 17 
3.3 
XSD .................................................................................................................................................... 17 
3.4 
CONFIGURAZIONE .................................................................................................................................. 17 
3.5 
TUTORIAL ............................................................................................................................................. 17 
4 
DESCRIZIONE DELL’INTERVENTO .................................................................................................... 18 
4.1 
AMBITO NORMATIVO ............................................................................................................................. 18 
4.1.1 
D.lgs. 123/2018 ......................................................................................................................................... 18 
4.2 
ADEGUAMENTO D.LGS. 123/2018 – SOTTOSISTEMA SIUS ......................................................................... 18 
4.2.1 
REQ-SIE-009-01 TDS - Concessione misure alternative (art. 678 comma 1-ter c.p.p.) e TDSM - Concessione 
misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.) ................................. 18 
4.2.2 
REQ-SIE-009-02 TDS/TDSM - Emissione del Decreto Presidenziale di Designazione ................................. 24 
4.2.3 
REQ-SIE-009-03 TDS/TDSM - Emissione Ordinanza Applicazione Provvisoria /Restituzione Atti al 
Presidente ................................................................................................................................................................. 29 
4.2.4 
REQ-SIE-009-04 TDS/TDSM - Registrazione data Esecutività Ordinanza Applicazione Provvisoria .......... 36 
4.2.5 
REQ-SIE-009-05 TDS/TDSM - Provvedimento di Conferma Ordinanza Applicazione Provvisoria .............. 39 
4.2.6 
REQ-SIE-009-06 - REQ-SIE-009-07 (Statistiche Misura Alternativa - art. 678 comma 1-ter c.p.p.) ) ......... 44 
4.2.7 
REQ-SIE-009-08 TDS/TDSM (Aggiornamento Statistica Movimento Provvedimenti per Oggetti) ............ 48

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 8/68 
 
 
4.2.8 
REQ-SIE-009-09 TDS/TDSM Modifica pagina richiesta atti istruttori ........................................................ 52 
4.2.9 
REQ-SIE-009-10 TDS/TDSM Statistica Atti Istruttori con Data Restituzione ............................................. 56 
4.2.10 
REQ-SIE-009-11 (UDS/UDSM – TDS/TDSM Integrazione Lista Mittenti) ................................................... 58 
4.3 
GESTIONE DEI TEMPLATE – SOTTOSISTEMA SIUS ........................................................................................ 59 
4.4 
MODULI SW.......................................................................................................................................... 61 
4.5 
INTERFACCE UTENTE ............................................................................................................................... 62 
4.6 
BASI DATI ............................................................................................................................................. 62 
4.6.1 
Base Dati - REQ-SIE-009-01 TDS - Concessione misure alternative (art. 678 comma 1-ter c.p.p.) e TDSM - 
Concessione misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.) ............. 62 
4.6.2 
Base Dati - REQ-SIE-009-02 (TDS/TDSM - Emissione del Decreto Presidenziale di Designazione) ............ 62 
4.6.3 
Base Dati - REQ-SIE-009-03 (TDS/TDSM - Emissione Ordinanza Applicazione Provvisoria/Restituzione Atti 
al Presidente) ............................................................................................................................................................ 63 
4.6.4 
Base Dati - REQ-SIE-009-04 (TDS/TDSM - Registrazione data Esecutività Ordinanza Applicazione 
Provvisoria) ............................................................................................................................................................... 64 
4.6.5 
Base Dati - REQ-SIE-009-05 (TDS/TDSM - Provvedimento di Conferma Ordinanza Applicazione Provvisoria)
 
64 
4.6.6 
Base Dati - REQ-SIE-009- 06 (TDS/TDSM - Statistica Ordinanze Non Emesse (Trasmessi Atti al Presidente))
 
64 
4.6.7 
Base Dati - REQ-SIE-009- 07 (TDS/TDSM - Statistica Ordinanze Provvisorie Esecutive senza decisione del 
Collegio) 64 
4.6.8 
Base Dati - REQ-SIE-009- 08 (Aggiornamento Statistica Movimento Provvedimenti per Oggetti) ........... 65 
4.6.9 
Base Dai - REQ-SIE-009- 09 (Modifica pagina Richiesta Atti Istruttori) .................................................... 65 
4.6.10 
Base Dati - REQ-SIE-009- 10 (Statistica Atti Istruttori con Data Restituzione) .......................................... 65 
4.6.11 
Base Dati - REQ-SIE-009-11 (UDS – TDS Integrazione Lista Mittente Atto) .............................................. 65 
5 
PIANO DELLE ATTIVITÀ .................................................................................................................. 66 
5.1 
CICLO DI SVILUPPO ................................................................................................................................. 66 
5.2 
PIANO DELLE ATTIVITÀ ............................................................................................................................ 66 
5.3 
GANTT ................................................................................................................................................. 66 
5.4 
VINCOLI ............................................................................................................................................... 67 
5.5 
LUOGO DI LAVORO ................................................................................................................................. 67 
6 
DIMENSIONAMENTO ..................................................................................................................... 68 
6.1 
STIMA DELL'EFFORT PREVISTO .................................................................................................................. 68 
6.2 
DETTAGLIO COSTI .................................................................................................................................. 68

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 9/68 
 
 
1 Introduzione 
1.1 
Scopo del documento 
Il presente documento riporta le specifiche di intervento che sarà realizzato nell’ambito del sistema SIES al 
fine di soddisfare i requisiti espressi dall’Amministrazione in relazione alla richiesta di adeguamento 
normativo del Sistema, nella sua interezza, al D.lgs. 123/2018 e al D.lgs. 121/2018. 
 
L’intervento in oggetto è stato richiesto con comunicazione m_dg.DOG07AR.08082019.0000017.U. 
Rientra nel servizio di Manutenzione Evolutiva ed è classificato come di seguito riportato: 
 
Scheda di Intervento  
2019_09  
Oggetto  
Adeguamento normativo SIES al D.lgs. 123/18 e 
121/18  
Complessità  
Alta  
Servizio  
MEV  
 
Tale documento espone gli interventi attinenti alle funzioni da prevedere nel sistema in base alle novità 
normative del decreto D.lgs.123/18 (maggiorenni e minorenni). 
Con lo scopo di rendere l’intervento coerente ed auto consistente gli interventi saranno relativi ai 
sottosistemi SIEP e SIUS. 
 
1.2 
Riferimenti 
Riferimen
to 
Nome Documento 
Descrizione Documento 
RIF1 
m_dg.DOG07AR.08082019.0000017.U_Nota_ 
Scheda_n.9.docx.pdf 
Richiesta Scheda di Intervento 
RIF2 
m_dg.DOG07AR.25_10_2019.0000096.U_Richiesta 
Riemissione _ Nota_Schedanr9SIES.docx_signed.pdf 
Nota per Riemissione della 
Scheda di Intervento 
RIF3 
SIES-SIUS-ModificheDecretoLegislativon.123.doc 
Documento dei requisiti fornito 
dal GdL SIES allegato alla 
Richiesta Scheda di Intervento 
RIF4 
SIES-SIEP-ModificheDecretoLegislativon.123.doc 
Documento dei requisiti fornito 
dal GdL SIES allegato alla 
Richiesta Scheda di Intervento 
RIF5 
SIUT-SIES-VR-1.2-20200626 
Flussi 
Decreto 
121_123_2018.pdf 
Documento dei flussi SIEP –SIUS 
per D.lgs. 123/2018 e 121/2018

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 10/68 
 
 
Riferimen
to 
Nome Documento 
Descrizione Documento 
RIF6 
SIGI_PNL_AA_2017 04 12_1.2_Architettura SIES.doc 
Documento di Architettura 
 
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 11/68 
 
 
Sigla 
Descrizione 
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
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 12/68 
 
 
2 
Definizione dell’Obiettivo 
Nell’ambito del progetto SIES si chiede di intervenire per adeguare il sistema, a seguito del D.lgs. 123/18 e 
del D.lgs. 121/18. 
 
In relazione al D.lgs. 123/18, la novità più significativa riguarda l’art. 4 comma 1 lett. B) nr. 3 del suddetto 
decreto che aggiunge il comma 1 ter all’art. 678 c.p.p. 
Esso ridimensiona l’ambito di operatività del procedimento di Sorveglianza per quanto riguarda la 
concessione di misure alternative. 
Qualora la pena da scontare, per i soggetti che hanno beneficiato della sospensione dell’ordine di esecuzione 
ai sensi dell’art. 656 comma 5 c.p.p. (c.d.” liberi sospesi”) non sia superiore a 18 mesi, è stata attribuita al 
magistrato “relatore” (designato secondo le procedure tabellari) il potere di decidere in via provvisoria sulle 
istanze di misura alternativa, con ordinanza emessa senza formalità, entro un termine assegnato dal 
Presidente del Tribunale. 
Se l’ordinanza viene emessa, la sua esecutività resta sospesa per il termine di giorni 10, entro i quali, gli 
interessati (condannato, suo difensore o pubblico ministero da individuarsi nel procuratore generale ex art. 
678 comma 3 c.p.p.) possono fare opposizione nel qual caso si procede con rito ordinario. 
Si procede, altresì, con il rito ordinario se il magistrato non emette ordinanza. 
In caso di emissione dell’ordinanza di concessione di misure alternative, decorso il termine per l’opposizione, 
il Tribunale si riunisce in camera di consiglio e senza formalità (da intendersi senza la presenza delle parti e 
con ordinanza) procede alla conferma del provvedimento provvisorio. 
Se il Tribunale decide di non confermare l’ordinanza del magistrato, non emette alcun provvedimento 
motivato ma fissa l’udienza affinché si proceda con il rito ordinario. 
 
Altre modifiche di rilievo attengono al potere del Tribunale di Sorveglianza, nell’ambito del procedimento di 
revoca delle misure alternative, di decidere anche in ordine all’eventuale sostituzione della misura con 
un’altra di diversa natura (art. 51 ter novellato) o il potere dello stesso magistrato di sorveglianza di eseguire 
(e non solo adottare) il provvedimento di cessazione della misura alternativa divenuta non più ammissibile, 
con il conseguente accompagnamento in Istituto penitenziario direttamente disposto dal Giudice (art. 51 bis 
novellato).

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 13/68 
 
 
Per le pene accessorie (secondo il nuovo articolo 51 quater) è prevista, inoltre, che la loro esecuzione possa 
esserci anche in pendenza di una misura alternativa e non solo all’esito della stessa, salvo che il Tribunale di 
Sorveglianza ne disponga la sospensione per prevalenti esigenze di reinserimento. In caso di revoca della 
misura il Tribunale dovrà poi decidere anche sulle pene accessorie, se in corso di esecuzione, ed 
eventualmente computarne il periodo già espiato. 
 
A seguire si riportano gli ambiti di intervento relativi alla prima fase di realizzazione inerente all’adeguamento 
del sistema SIES limitatamente al D.lgs. 123/18 e alle seguenti macro funzionalità: 
- 
Gestione della concessione delle misure alternative alla detenzione relativa dell’introduzione dell’art. 
678 c1 ter (per SIUS e per SIEP); 
- 
Gestione del decreto di designazione del magistrato (SIUS); 
- 
Gestione dell’Ammissione Provvisoria (art. 678 c1 ter) e della sua esecutività (per SIUS e per SIEP); 
- 
Gestione della Conferma dell’Ammissione Provvisoria (per SIUS e per SIEP); 
- 
Introduzione di nuove funzioni di Estrazione Dati relative alle novità dell’art. 678 c1 ter (SIUS); 
- 
Allineamento della Statistica Movimento Provvedimenti Per Oggetti (SIUS); 
- 
Integrazione sulle funzioni di Richiesta Atti Istruttori e gestione lista mittenti con “Gruppo Di 
Osservazione E Trattamento (SIUS); 
- 
Allineamento della funzione di Riepilogo Ispettivo in relazione all’Ammissione Provvisoria e 
all’ordinanza/decreto di Conferma (SIEP). 
 
Restano esclusi, in questa prima fase di analisi e realizzazione, i requisiti relativi al D.lgs. 123/2018 che 
afferiscono alla: 
- 
Gestione della ‘Revoca dell’Ammissione Provvisoria - art. 678 comma 1-ter c.p.p.’ e relativa funzione 
di Estrazione Dati; 
- 
Sostituzione di una misura alternativa (art. 51 ter O.P.); 
- 
Sospensione delle pene accessorie (art. 51 quater O.P.); 
- 
Atri interventi SIUS (integrazione Lavoro Pubblica Utilità, Rettifica del Lavoro Esterno).

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 14/68 
 
 
2.1 
Convenzioni 
Sulla base degli ambiti di progetto e dei tipi di requisito, la convenzione per l’identificazione dei requisiti è 
riportata di seguito. 
Ciascun requisito è individuato da un identificativo univoco nella forma [REQ-SIS-nnn-mm], dove: 
• 
REQ Requisito; 
• 
SIS identifica il sistema (cfr. SIUT-GEN-SN-2.2-20191023-Standard di nomenclatura);  
• 
nnn è il numero della scheda di richiesta intervento; 
• 
mm è il numero progressivo del requisito espresso dall’Amministrazione. 
 
2.2 
Elenco Requisiti 
Gli interventi di questo obiettivo possono riassumersi nei requisiti funzionali di seguito descritti, ed attengono 
a quanto richiesto nel documento “m_dg.DOG07AR.08082019.0000017.U_Nota_ Scheda_n.9.docx.pdf” 
[RIF1] e fanno riferimento al D.lgs. 123/2018 descritto nella definizione dell’obiettivo. 
 
I requisiti elencati si riferiscono ad interventi da realizzare nell’ambito dei sottosistemi SIUS (Maggiorenni e 
Minorenni) e SIEP (Maggiorenni e Minorenni) limitatamente alla macro funzioni specificate al paragrafo 
precedente. 
2.2.1 REQ-SIE-009-01 (SIUS) 
In relazione all’articolo 678 c.p.p. comma 1 ter, introdotto con D.lgs. 123/2018, i Tribunali di Sorveglianza 
maggiorenni (TDS) devono essere abilitati all’emissione di un’ordinanza con contenuto di ‘Concessione 
misure alternative (art. 678 comma 1-ter c.p.p.) ’, mentre i Tribunali di Sorveglianza minorenni (TDSM) 
devono essere abilitati all’emissione di un’ordinanza con contenuto di ‘Concessione misure penali di 
comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.) ’. 
2.2.2 REQ-SIE-009-02 (SIUS) 
In relazione all’articolo 678 c.p.p. comma 1 ter, il Presidente del Tribunale di Sorveglianza (TDS/TDSM), in 
tema di semplificazione della procedura, designa, dopo aver acquisito i documenti e le necessarie 
informazioni, il magistrato relatore per l’emissione un’ordinanza di ammissione provvisoria per una misura 
alternativa di all'articolo 656, comma 5.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 15/68 
 
 
2.2.3 REQ-SIE-009-03 (SIUS) 
Nell’ambito dei Tribunali di Sorveglianza (TDS/TDSM), in relazione all’articolo 678 c.p.p. comma 1 ter, il 
magistrato designato può emettere un’ordinanza di ammissione provvisoria ad una misura alternativa di cui 
all’articolo 656, comma 5 oppure restituire gli atti al Presidente. 
2.2.4 REQ-SIE-009-04 (SIUS) 
Caratterista fondamentale dell’ordinanza di ammissione provvisoria è la sua non immediata esecutività. 
Con il requisito in oggetto il sistema deve prevedere una nuova funzione, nell’ambito dei Tribunali di 
Sorveglianza (TDS/TDSM), che permetta al magistrato designato di poter inserire la data a partire dalla quale 
l’ordinanza di ammissione provvisoria della misura diverrà esecutiva.  
2.2.5 REQ-SIE-009-05 (SIUS) 
Emissione del provvedimento di Conferma (ratifica) dell’Applicazione Provvisoria della misura da parte del 
Tribunale di Sorveglianza (TDS/TDSM). Il sistema deve permettere di inserire il provvedimento di conferma 
come Ordinanza. 
2.2.6 REQ-SIE-009-06 (SIUS) 
Nell’ambito dei Tribunali di Sorveglianza (TDS/TDSM), prevedere una funzione di estrazione dati per il 
recupero dei procedimenti SIUS con contenuto ‘Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) 
’, nel caso dei maggiorenni (TDS), o con contenuto ‘Concessione misure penali di comunità/misure 
alternative alla detenzione (art. 678 comma 1 ter c.p.p.)’, per i minorenni (TDSM),  per i quali il magistrato 
designato ha proceduto alla ‘non emissione’ dell’ordinanza trasmettendo gli atti al Presidente. 
2.2.7 REQ-SIE-009-07 (SIUS) 
Nell’ambito dei Tribunali di Sorveglianza (TDS/TDSM), prevedere una funzione di estrazione dati per il 
recupero dei procedimenti SIUS con contenuto ‘Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) 
’, nel caso dei maggiorenni (TDS), o con contenuto ‘Concessione misure penali di comunità/misure 
alternative alla detenzione (art. 678 comma 1 ter c.p.p.)’, per i minorenni (TDSM),  con data di esecutività 
inserita, ma privi di decisione da parte del Collegio. 
2.2.8 REQ-SIE-009-08 (SIUS) 
Intervenire sull’aggiornamento della funzione STATISTICHE – MOVIMENTO PROVVEDIMENTI PER OGGETTI in 
modo da integrare la nuova tipologia di ordinanza provvisoria di cui al requisito REQ-SIE-009-03.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 16/68 
 
 
2.2.9 REQ-SIE-009-09 (SIUS) 
Intervenire sulle pagine di richiesta di atti istruttori al fine di indicare la data entro cui l’atto deve essere 
restituito all’ufficio di Sorveglianza che ne ha fatto richiesta. 
2.2.10 REQ-SIE-009-10 (SIUS) 
Prevedere una nuova funzione di estrazione dati, nel menù Statistiche/Monitoraggio, che conteggi ed 
estrapoli la lista dei procedimenti per i quali, in fase di richiesta di un atto istruttorio, sia stata indicata una 
determinata data di scadenza entro il quale far pervenire l’atto richiesto. 
2.2.11 REQ-SIE-009-11 (SIUS) 
Stante quanto prescritto dall’art. 57 O.P., nella maschera di iscrizione di un procedimento SIUS, nella combo 
box dei mittenti, occorre aggiungere la voce “gruppo di osservazione e trattamento”.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 17/68 
 
 
3 Architettura del Sistema 
3.1 
Architettura 
L’intervento in oggetto non introduce variazioni architetturali, rispetto al sistema attuale. 
3.2 
WEB services 
N.A. 
3.3 
XSD 
N.A. 
3.4 
Configurazione 
N.A. 
3.5 
Tutorial 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 18/68 
 
 
4 Descrizione dell’Intervento 
4.1 
Ambito Normativo 
4.1.1 
D.lgs. 123/2018 
In relazione al Capo II: DISPOSIZIONI PER LA SEMPLIFICAZIONE DEI PROCEDIMENTI, Art. 4: Modifiche al codice 
di procedura penale in tema di semplificazione, all'articolo 678, viene inserito il comma 1-ter che recita 
quanto segue:  
 
«1-ter. Quando la pena da espiare non è superiore a un anno e sei mesi, per la decisione sulle istanze di cui all'articolo 
656, comma 5, il presidente del tribunale di sorveglianza, acquisiti i documenti e le necessarie informazioni, designa il 
magistrato relatore e fissa un termine entro il quale questi, con ordinanza adottata senza formalità, può applicare in via 
provvisoria una delle misure menzionate nell'articolo 656, comma 5. L'ordinanza di applicazione provvisoria della misura 
è comunicata al pubblico ministero e notificata all'interessato e al difensore, i quali possono proporre opposizione al 
tribunale di sorveglianza entro il termine di dieci giorni. Il tribunale di sorveglianza, decorso il termine per l'opposizione, 
conferma senza formalità la decisione del magistrato.  
Quando non è stata emessa o confermata l'ordinanza provvisoria, o è stata proposta opposizione, il tribunale di 
sorveglianza procede a norma del comma 1. Durante il termine per l'opposizione e fino alla decisione sulla stessa, 
l'esecuzione dell'ordinanza è sospesa.»; 
 
4.2 Adeguamento D.lgs. 123/2018 – Sottosistema SIUS 
In riferimento all’’introduzione del comma 1 ter all’articolo 678 c.p.p., il Tribunale di Sorveglianza (TDS) e il 
Tribunale di Sorveglianza dei Minorenni (TDSM), per mezzo di un magistrato designato, possono applicare in 
via provvisoria misure alternative ex art. 656 commi 5 e 6 c.p.p. (TDS) e misure penali di comunità (TDSM), 
per procedimenti relativi a condanne per pene fino a 18 mesi. 
 
Nasce, pertanto, l’esigenza di dover gestire due nuovi contenuti in fase di iscrizione di un procedimento SIUS, 
uno per TDS e l’altro per TDSM. 
4.2.1 
REQ-SIE-009-01 TDS - Concessione misure alternative (art. 678 comma 1-ter c.p.p.) e 
TDSM - Concessione misure penali di comunità/misure alternative alla detenzione 
(art. 678 comma 1 ter c.p.p.) 
 
Nell’ambito dell’ufficio Tribunale di Sorveglianza (TDS), il contenuto da integrare è il seguente: 
 
• 
Concessione misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.)

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 19/68 
 
 
 
mentre nell’ambito dell’ufficio Tribunale di Sorveglianza dei Minorenni (TDSM), il contenuto da integrare è il 
seguente: 
 
• 
Concessione misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter 
c.p.p.) 
 
Per entrambi i contenuti vanno associati i seguenti oggetti:  
- 
Affidamento in prova al servizio sociale (art. 47 O.P. -  art. 678 comma 1-ter c.p.p.);  
- 
Affidamento in prova al servizio sociale (art. 94 DPR 309/90 - art. 678 comma 1-ter c.p.p.); 
- 
Detenzione domiciliare (art. 47 ter O.P. - art. 678 comma 1-ter c.p.p.); 
- 
Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.); 
- 
Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.); 
 
 
In corrispondenza della voce “Detenzione domiciliare (art. 47 ter O.P. - art. 678 comma 1-ter c.p.p.)”, occorre 
prevedere un sotto elenco con le seguenti descrizioni, la cui selezione, come già avviene attualmente, non 
sarà obbligatoria: 
 
- 
Detenzione Domiciliare Donna Incinta o Madre di Prole di Età Inferiore Ad Anni Dieci con Lei 
Convivente; 
- 
Detenzione Domiciliare Padre, Esercente la Potestà, di Prole di Età Inferiore Ad Anni Dieci con Lui 
Convivente; 
- 
Detenzione Domiciliare Persona in Condizioni di Salute Particolarmente Gravi, Che Richiedano 
Costanti Contatti con i presidi sanitari territoriali; 
- 
Detenzione Domiciliare Persona di Età Superiore a Sessanta Anni Se Inabile Anche Parzialmente (solo 
per TDS, non visibile per TDSM) 
- 
Detenzione Domiciliare Persona Minore di Anni Ventuno per Comprovate Esigenze di Salute, di 
Studio, di Lavoro e di Famiglia; 
- 
Detenzione domiciliare (art. 47 ter comma 1 bis O.P. - art. 678 comma 1-ter c.p.p.);

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 20/68 
 
 
- 
Detenzione domiciliare per ultrasettantenni (art. 47 ter comma 01 O.P. - art. 678 comma 1-ter c.p.p.) 
(solo per TDS, non visibile per TDSM). 
 
NB: per le implementazioni delle misure penali di comunità, cosi come normate dal d.lgs. 121/2018, si 
rimanda alla fase successiva di realizzazione come indicato nella tabella al par. 5.2. 
L’introduzione dei due contenuti, uno per TDS e l’altro per TDSM, operativamente si traduce nella possibilità 
di poter scegliere una nuova voce nella combo-box dei contenuti nella pagina di iscrizione di un procedimento 
SIUS, così come mostrato nella figura che segue: 
 
 
Figura 1: Pagina iscrizione procedimento SIUS per Concessione misure alternative (art. 678 comma 1-ter c.p.p.) per TDS 
 
Nell’ambito di un ufficio TDSM, in contenuto avrà la nomenclature prevista di ‘Concessione misure penali di 
comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.) ’, per cui la form di iscrizione e 
uguale a quella del TDS, varierà solo per la descrizione del contenuto:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 21/68 
 
 
 
A valle della selezione del contenuto, in fase di associazione degli oggetti, tramite il pulsante 
,  il sistema 
deve poter permettere di associare le voci su elencate, così come prospettate nella figura che segue: 
 
Figura 2: Elenco oggetti per contenuto Concessione Misure Alternative (art. 678 comma 1-ter c.p.p.) e Concessione misure penali 
di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.) 
 
che varierà solo in caso di selezione dell’oggetto Detenzione Domiciliare per l’elenco dell’ulteriore Dettaglio 
 
 
Figura 3: Elenco descrizioni per  Detenzione Domiciliare ( art. 47 ter O.P. -art. 678 comma 1-ter c.p.p.) per TDS 
 
 
Figura 4: Elenco descrizioni per  Detenzione Domiciliare ( art. 47 ter O.P. -art. 678 comma 1-ter c.p.p.) per TDSM 
 
A seguito dell’iscrizione del procedimento SIUS con il nuovo contenuto “Concessione misure alternative (art. 
678 comma 1-ter c.p.p.)”, oppure con il nuovo contenuto ‘Concessione misure penali di comunità/misure 
alternative alla detenzione (art. 678 comma 1 ter c.p.p.) ’, l’utente procede con l’emissione dell’ordinanza.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 22/68 
 
 
 
In base alla ‘novità’ prevista da d.lgs. 123/2018, ossia l’introduzione di una fase provvisoria, in corrispondenza 
della selezione di uno dei suddetti contenuti, si può avere una doppia diramazione per quanto concerne la 
fase di emissione dell’ordinanza. 
Infatti, si può dare ‘inizio’ ad una fase provvisoria che prevede quanto esposto al par. 4.2.2 (Emissione del 
Decreto Presidenziale di Designazione) ed al par 4.2.3 (Emissione Ordinanza Applicazione Provvisoria) , 
oppure ad una fase ‘ordinaria’ (con rito dibattimentale), che può incorre nelle casistiche in cui non si dia 
‘inizio’ alla fase provvisoria, o nei casi in cui la ‘fase provvisoria’ si concluda con una ‘non conferma’ 
dell’ordinanza provvisoria emessa dal magistrato designato. Si confluirà nella casistica di ‘rito ordinario’ 
anche nel caso in cui venga presentata opposizione. 
 
Pertanto, per la casistica di ‘rito ordinario’, sia per i TDS che per i TDSM, la pagina di emissione dell’ordinanza 
sarà uguale alla maschera attualmente utilizzata per il contenuto ‘Concessione Misure Alternative Alla 
Detenzione’ (C001):

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 23/68 
 
 
 
Figura 5: Emissione Ordinanza di Misura Alternativa (art. 678 comma 1-ter c.p.p.)  - (TDS e TDSM) 
 
E gli esiti previsti per lo scarico dell’ordinanza saranno: 
• 
Concede   
• 
Rigetta 
• 
Dichiara L’inammissibilità 
• 
Dichiara N.D.P./ N.L.P. 
• 
Dichiara La Propria Incompetenza 
 
In fase di stampa dell’ordinanza, saranno agganciati i template ad oggi già presenti a sistema per le ordinanze 
di ‘Affidamento in Prova’, ‘Semilibertà, ‘Detenzione Domiciliare e ‘Sospensione Pena’;

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 24/68 
 
 
Il flusso di lavorazione del procedimento SIUS che abbia il nuovo contenuto ‘Concessione Misura Alternativa 
(art. 678 comma 1-ter c.p.p.) ’ oppure ‘Concessione misure penali di comunità/misure alternative alla 
detenzione (art. 678 comma 1 ter c.p.p.) ’, per rito ordinario, seguirà quello attualmente in essere per il 
contenuto ‘Concessione Misure Alternative Alla Detenzione’ (C001) con la gestione della modifica, 
visualizzazione, cancellazione, stampa, validazione e trasmissione. 
Dal punto di vista tecnico-implementativo, per la casistica in esame, le funzioni di modifica, 
visualizzazione(dettaglio), cancellazione, stampa, e validazione non subiranno interventi, mentre per ciò che 
attiene la funzione di trasmissione, occorre prevedere l’aggiunta di nuove informazioni sull’xml di scambio. 
L’aggiunta di ulteriori dati può intervenire nei casi in cui, dopo una prima fase provvisoria, si possa passare a 
rito ordinario, ad esempio in caso di opposizione oppure in caso di mancata emissione de 
plano dell’ordinanza nel termine assegnato al magistrato relatore. 
 
La funzione di trasmissione è fondamentale per implementare correttamente lo scambio di informazioni con 
SIEP e permettere, pertanto, lato Procura, la gestione delle nuova ordinanza di ‘Concessione di Misura 
Alternativa (art. 678 comma 1-ter c.p.p.) ’. Si evidenzia che questo è uno dei punti di impatto di 
‘interconnessione’ del sistema SIUS con il sotto sistema SIEP. Per i dettagli relativi alla gestione 
dell’ordinanza, lato SIEP, si rimanda al par. Errore. L'origine riferimento non è stata trovata..  
 
4.2.2 
REQ-SIE-009-02 TDS/TDSM - Emissione del Decreto Presidenziale di Designazione 
Sempre in riferimento al comma 1 ter all’articolo 678 c.p.p., per procedimenti relativi a condanne per pene 
fino a 18 mesi, l’ufficio Tribunale di Sorveglianza (TDS/TDSM), in tema di semplificazione della procedura, 
designa il magistrato relatore e fissa un termine entro il quale questi, con ordinanza adottata senza formalità, 
può applicare in via provvisoria una delle misure menzionate nell'articolo 656, comma 5. 
 
L’adeguamento del sistema SIUS a tale normativa si delinea nell’implementazione che si espone a seguire. 
 
Accedendo al sistema SIUS con utenza Tribunale di Sorveglianza (TDS/TDSM), in corrispondenza del menù 
‘Decreti’, sarà introdotto un nuovo tasto funzione denominato ‘Designazione Magistrato Relatore’.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 25/68 
 
 
 
Figura 6: Menù Decreti -  Decreto Presidenziale di Designazione - (TDS e TDSM) 
 
 
L’accesso alla funzione ‘Designazione Magistrato Relatore’ mostrerà una nuova maschera per inserire il 
decreto in oggetto, solo in caso dei contenuti riportati di seguito, diversamente invierà un messaggio 
bloccante all’utente, che ne inibirà l’utilizzo.  
Dal punto di vista funzionale il Decreto di Designazione, va inserito dopo l’iscrizione di un procedimento SIUS 
con contenuto “Concessione misure alternative (art. 678 comma 1-ter c.p.p.)” oppure con contenuto 
“Concessione misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.)”. 
 
Pertanto, l’utente: 
 Inserisce un nuovo procedimento SIUS di “Concessione misure alternative (art. 678 comma 1-ter c.p.p.)” 
per TDS, oppure Inserisce un nuovo procedimento SIUS di “Concessione misure penali di comunità/misure 
alternative alla detenzione (art. 678 comma 1 ter c.p.p.)” per TDSM; 
 Emette, nei casi previsti dal decreto, il decreto Presidenziale di Designazione. 
 
Tramite questa funzione il Tribunale di Sorveglianza va a designare il magistrato relatore che può applicare 
in via provvisoria, in riferimento a procedimenti relativi a condanne per pene fino a 18 mesi, una delle misure 
menzionate nell'articolo 656, comma 5. 
La maschera per l’inserimento del decreto deve permettere pertanto, di poter inserire le seguenti 
informazioni: 
- 
Data Emissione

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 26/68 
 
 
- 
Magistrato Relatore designato (di default sarà visualizzato il nominativo del magistrato a cui è già 
stato assegnato il procedimento in fase di iscrizione (secondo la ripartizione tabellare) con la 
possibilità, ovviamente, di modificare l’originaria assegnazione. 
- 
Contenuto (valore fisso, corrispondente al contenuto - Concessione misure alternative (art. 678 
comma 1-ter c.p.p.), per TDS, oppure Concessione misure penali di comunità/misure alternative alla 
detenzione (art. 678 comma 1 ter c.p.p.), per TDSM, selezionato in fase di iscrizione del procedimento 
SIUS 
- 
Oggetto (selezionabile dalla lista degli oggetti associati al contenuto - Concessione misure alternative 
(art. 678 comma 1-ter c.p.p.) ed al contenuto Concessione misure penali di comunità/misure 
alternative alla detenzione (art. 678 comma 1 ter c.p.p.) 
- 
Data Termine Emissione ordinanza provvisoria/Restituzione atti al presidente    (dove indicare il 
termine entro il quale il magistrato dovrebbe provvedere all’emissione dell’ordinanza di ammissione 
provvisoria o di restituzione degli atti al Presidente, esprimibile con una data o numero giorni, si 
tratta di un dato non obbligatorio.). 
 
 
Figura 7: Pagina di inserimento del Decreto Designazione Magistrato - (TDS e TDSM) 
 
Caratteristica fondamentale di tale decreto è che a seguito dell’inserimento e validazione dello stesso, il 
procedimento in lavorazione non deve essere chiuso. 
Per tale decreto deve essere creato un documento di stampa ad hoc che sarà fornito dall’Amministrazione. 
Si evidenzia che per questo decreto non è necessaria l’avvenuta nomina di un avvocato.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 27/68 
 
 
Lo stato del procedimento, a seguito della validazione del Decreto di Designazione, sarà impostato a ‘Emesso 
Decreto Designazione’, mentre l’esito da associare al decreto è ‘Designa Magistrato art. 678 1-ter c.p.p.’. 
L’introduzione di un nuovo stato procedimento e nuovo esito si giustifica per la corretta individuazione dei 
procedimenti SIUS ai fini delle elaborazioni statistiche dettagliate ai par.4.2.6.2 e 4.2.6.5. Per questo decreto, 
come già avviene per il decreto di Fissazione Udienza, non è obbligatorio procedere al deposito. 
Al momento della conferma il sistema effettua i seguenti controlli: 
- 
La data emissione non può essere inferiore alla data di arrivo in cancelleria, in caso di condizione 
verificata, viene inviato il seguente messaggio 
 
 
 
- 
In caso di procedimento ancora privo di Magistrato assegnatario, nel momento in cui, tramite il 
Decreto di designazione, viene individuato il Magistrato, il sistema aggiorna  in automatico    
magistrato assegnatario, riportato nella maschera di dettaglio del procedimento SIUS.  
Qualora il magistrato assegnatario del procedimento fosse già stato assegnato precedentemente 
all’emissione del decreto, e dovesse differire dal magistrato designato con il decreto, il sistema 
invierà un messaggio di avviso della discrepanza 
 
 
chiedendo conferma per poter procedere automaticamente alla sostituzione del magistrato 
assegnatario con quello indicato in maschera, operazione che effettuerà in caso di conferma da parte

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 28/68 
 
 
dell’utente. Nel caso di risposta negativa, il sistema, si riposizionerà sulla form, permettendo di poter 
selezionare il magistrato relatore corretto e di riconfermare i dati. 
- 
sui campi della form dove indicare la data o il numero di giorni entro cui il magistrato dovrà emettere 
l’ordinanza di applicazione provvisoria, pur non essendo obbligatori, il sistema segnala l’eventuale 
assenza, inviando il messaggio 
 
 
 
A seguito della Conferma, il sistema inserirà il Decreto di Designazione del Magistrato relatore e presenterà 
la form di Dettaglio 
 
Figura 8: Pagina di Dettaglio del Decreto Designazione Magistrato - (TDS e TDSM)

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 29/68 
 
 
Da cui sarà possibile procedere alla stampa del template SIUS_DE_DECRDESMAGREL.rtf, oppure alla 
validazione, modifica o cancellazione del decreto. A seguito della validazione il sistema aggiornerà lo stato 
procedimento 
 
Figura 9: Stato Procedimento a seguito Decreto Designazione Magistrato - (TDS e TDSM) 
 
La cancellazione del decreto, successivamente alla svalidazione dello stesso, o l’annullamento, in caso di 
decreto depositato e validato, riportano lo stato del procedimento in stato di Iscritto. 
Il magistrato, ricevuta la designazione, se ritiene di poter concedere una delle misure alternative previste 
dall’art. 656 comma 5 c.p.p., e non necessariamente quella richiesta dal condannato, emette de plano 
un’ordinanza di applicazione provvisoria. 
La gestione dell’ordinanza di applicazione provvisoria è descritta nel paragrafo successivo. 
 
 
4.2.3 
REQ-SIE-009-03 TDS/TDSM - Emissione Ordinanza Applicazione Provvisoria 
/Restituzione Atti al Presidente 
Il magistrato relatore designato, entro il termine stabilito nel decreto, può alternativamente: 
 
- 
Emettere l’ordinanza di Applicazione Provvisoria di una delle Misure Alternative; 
- 
Restituire gli Atti al Presidente, senza emissione di alcun provvedimento. 
4.2.3.1 
Emissione Ordinanza Applicazione Provvisoria 
Accedendo al sistema SIUS con utenza Tribunale di Sorveglianza (TDS/TDSM), in corrispondenza del 
menù ‘Ordinanze’, sarà introdotto un nuovo tasto funzione denominato ‘Applicazione Provvisoria 
M.A – Conferma Decisione Magistrato Relatore’

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 30/68 
 
 
 
Figura 10: Menù Emissione Ordinanza Provvisoria - (TDS e TDSM) 
 
che presenta il seguente sottomenu: 
 
 
da cui, selezionando la funzione ‘Applicazione Provvisoria M.A. , il sistema presenterà la form per 
l’inserimento dell’ordinanza di Applicazione Provvisoria di Misura Alternativa. La tipologia di ordinanza che 
viene emessa deve essere di tipo ‘ordinanza provvisoria’ e l’emissione di tale ordinanza non deve richiedere 
la fase di ‘Fissazione’ o ‘Prefissazione’ udienza. Deve essere gestita, quindi, come rito monocratico. 
Dal punto di vista funzionale, l’emissione di un’ordinanza di Applicazione Provvisoria M.A. si inserisce a valle 
dell’inserimento del Decreto Presidenziale di Designazione. 
Affinché possa essere emessa un’ordinanza di Applicazione Provvisoria M.A., infatti, il sistema deve 
controllare che, per il procedimento SIUS in lavorazione, sia stato emesso il Decreto di Designazione del 
magistrato relatore. 
Nella casistica in cui non sia stato emesso il Decreto di Designazione, per dare seguito all’applicazione della 
misura, si procede con l’emissione dell’ordinanza (rito ordinario) cosi come esplicitato al par. 4.2.1, 
rientrando quindi nel classico giro del rito ordinario, quindi con la fissazione udienza e con l’emissione 
dell’ordinanza che applica o meno la misura. 
Nel caso che l’utente selezioni la funzione di Ordinanza di Applicazione, senza che sia presente il Decreto di 
Designazione, il sistema invierà il seguente messaggio

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 31/68 
 
 
 
 
La maschera per l’inserimento dell’ordinanza provvisoria, similmente all’emissione di un ordinanza generica 
deve permettere di poter inserire le seguenti informazioni: 
- 
Data Emissione 
- 
Contenuto  
- 
Oggetto 
oltre all’inserimento del difensore, selezionando l’apposito link 
. 
 
Figura 11: Emissione Ordinanza Applicazione Provvisoria M.A. - (TDS e TDSM)

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 32/68 
 
 
mentre, nella pagina di inserimento degli esiti, ossia sulla pagina che il sistema mostra a seguito della 
‘Conferma’, oltre alla combo box contenente gli esiti, devono essere previste, in aggiunta, le seguenti 
informazioni: 
- 
Un campo ‘check box’ con accanto la dicitura “Ordinanza non emessa – restituzione atti al 
Presidente”. 
- 
Campo Ulteriore Descrizione (per eventuali motivazioni della restituzione degli atti o riguardanti 
l’ordinanza di applicazione). 
 
Figura 12: Pagina esiti Ordinanza Provvisoria - (TDS e TDSM) 
 
Gli esiti da prevedere sono quelli consueti, vale a dire “Applica Provvisoriamente”, “Rigetta”, “NLP”, 
“Inammissibilità” e “Incompetenza”. 
Il magistrato emette ordinanza solo se Applica provvisoriamente la misura richiesta o, in caso di più misure 
richieste, ne applica una e si esprime negativamente sulle altre. In questo caso il sistema inserisce in base 
dati una nuova ordinanza, che dovrà essere validata e depositata. A seguito del deposito lo stato del 
procedimento sarà impostato a “Emessa Ordinanza Applicazione provvisoria”. Per questa nuova ordinanza

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 33/68 
 
 
sarà 
possibile 
stampare 
uno 
specifico 
documento, 
che 
sarà 
fornito 
dall’Amministrazione 
(SIUS_OR_APPLPROVMA.rtf). 
Se si seleziona il check-box “Ordinanza non emessa – restituzione atti al Presidente” il sistema inibisce la 
compilazione di tutti gli altri campi della form, ad eccezione di “Ulteriore Descrizione”, in quanto il sistema 
non procederà all’emissione di alcuna ordinanza (vedi par. 4.2.3.1). 
Caratteristica fondamentale dell’ordinanza del magistrato designato di Applicazione Provvisoria di Misura 
Alternativa, è la sua non immediata esecutività. Ciò significa che a seguito di esito ‘Applica 
Provvisoriamente’, l’ordinanza successivamente al deposito e relativa validazione, sarà visibile, come già 
avviene per tutte le altre ordinanze già disponibili nel sistema, lato SIEP, ma non sarà gestibile in quanto non 
vi sarà disponibile una specifica funzione che ne permetta la gestione in assenza della data di esecutività.  
L’ordinanza, depositata, diverrà esecutiva una volta trascorsi 10 giorni senza che venga proposta opposizione 
e, in virtù di ciò, deve essere prevista la possibilità di annotare, ed evidenziare nella maschera di dettaglio del 
procedimento SIUS, la data di esecutività della stessa. La descrizione di tale funzionalità è esposta nel 4.2.4. 
Nella casistica, invece, in cui venga presentata opposizione, detta opposizione va annotata sul procedimento 
“provvisorio” utilizzando l’apposita funzione “Impugnazioni/Opposizioni”. Per la gestione delle impugnazioni, 
il procedimento SIUS seguirà il medesimo processo di lavorazione già in essere per il contenuto ‘Concessione 
Misure Alternative Alla Detenzione’ (C001). 
4.2.3.2 
Restituzione Atti Al Presidente 
Nel caso in cui il magistrato relatore ritenga di non poter applicare alcuna delle misure concedibili, egli dovrà 
limitarsi a rimettere gli atti al Presidente del Tribunale di Sorveglianza, il quale provvederà secondo il 
tradizionale procedimento ex articolo 678, comma 1 del codice di procedura penale, predisponendo il 
contraddittorio. Per annotare la restituzione degli atti  sarà possibile utilizzare una della seguenti funzionalità: 
- 
Emissione Ordinanza di Applicazione Provvisoria; 
- 
Gestione Restituzione Atti al Presidente. 
Nel primo caso l’utente accederà alla funzione descritta al precedente paragrafo, limitandosi a valorizzare la 
data di emissione e selezionando il check box Ordinanza non emessa – Atti al Presidente  e a valorizzare 
eventualmente il campo Ulteriore Descrizione.  
A seguito della Conferma il sistema invierà il seguente messaggio per ulteriore conferma da parte 
dell’utente di voler procedere alla restituzione degli atti

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 34/68 
 
 
 
 
 Dopo l’ulteriore conferma da parte dell’utente il sistema si limiterà ad annotare sul procedimento i dati 
inseriti e a impostare lo stato del procedimento SIUS a ‘Restituiti Atti al Presidente’. 
 
Nel secondo caso sarà possibile annotare la restituzione degli atti accedendo al Dettaglio Procedimento SIUS 
e selezionando dalla tool bar la nuova funzione ‘Gestione Restituzione Atti al Presidente’ 
 
 
che, se non è già presente una data di restituzione, presenterà la form per l’Inserimento 
 
Figura 13: Pagina Inserimento Restituzione Atti al Presidente - (TDS e TDSM) 
 
In cui l’utente dovrà inserire la data di restituzione e le eventuali motivazioni (campo a testo libero). A seguito 
della conferma il sistema presenterà la form di Dettaglio del Procedimento, in cui risulterà aggiornato lo stato 
del procedimento e sarà riportata la data di restituzione

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 35/68 
 
 
                       
Figura 14: Pagina Dettaglio Procedimento SIUS a seguito Restituzione Atti - (TDS e TDSM) 
 
In caso di procedimento in stato di ‘Atti Restituiti al Presidente’ , selezionando la funzione ‘Gestione 
Restituzione Atti al Presidente’, il sistema presenterà il Dettaglio dei dati relativi alla restituzione degli atti 
presenti nella base dati 
 
Figura 15: Pagina  Dettaglio Restituzione Atti al Presidente - (TDS e TDSM) 
 
da cui sarà possibile selezionare le azioni di Modifica o di Cancellazione. 
 
In caso di cancellazione lo stato del procedimento sarà reimpostato a ‘Emesso Decreto Designazione’. 
 
La ‘Non Emissione’ dell’ordinanza determina comunque la chiusura della fase provvisoria in maniera 
alternativa rispetto alla ordinaria indicazione degli esiti. La procedura a questo punto segue il suo corso 
normale con l’apertura del dibattito. Quindi il TDS/TDSM fissa udienza ed emette ordinanza.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 36/68 
 
 
 
 
4.2.4 
REQ-SIE-009-04 TDS/TDSM - Registrazione data Esecutività Ordinanza Applicazione 
Provvisoria 
Per la registrazione della data di esecutività si prevede di aggiungere una nuova voce menù da inserire nella 
combo box presente nella maschera di dettaglio del procedimento SIUS.   
 
Figura 16: Funzione Esecutività Applicazione Provvisoria m.a. 
 
Dal punto di vista funzionale, l’attività di registrazione della data di esecutività dell’ordinanza di applicazione 
provvisoria si pone a valle dell’emissione dell’ordinanza provvisoria. 
Accedendo alla funzione, il sistema, verifica l’ esistenza dell’ordinanza di Applicazione Provvisoria, 
validata,depositata e deposito validato, in caso di non sussistenza delle suddette condizioni, invierà il 
seguente messaggio 
 
In caso di esito positivo  prospetta una nuova pagina in cui deve essere registrata la data di esecutività 
dell’ordinanza di applicazione provvisoria. 
A seguire si mostra un esempio di pagina. Le informazioni da riportare sono: 
- 
Dettaglio procedimento SIUS 
- 
Dettaglio dati Soggetto 
- 
Estremi dell’ordinanza provvisoria di Concessione di Misura Alternativa (art. 678 comma 1 -ter) 
- 
Campo ‘Data Esecutività’ 
- 
Campo note 
- 
Destinatari  (quelli già inseriti nel Deposito Ordinanza) 
- 
Ulteriori destinatari

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 37/68 
 
 
 
 
 
Figura 17: Pagina Registrazione Esecutività - (TDS e TDSM) 
 
I campi editabili sono ‘Data Esecutività’ e ‘note, che a seguito del conferma devono essere registrati nella 
tabella deposito_ordinanza_pc, data trasmissione e ulteriori destinatari (gli stessi previsti nel deposito 
ordinanza). 
Per la data di esecutività, che è dato obbligatorio da inserire, occorre prevedere, in caso di avvenuta 
valorizzazione delle date di notifica (operazione non obbligatoria), un controllo che segnali che il valore 
inserito superi i 10 giorni rispetto alla data dell'ultima notifica. Per una data che superi tale limite, visualizzare 
un messaggio di avviso sulla pagina con la conferma a procedere comunque con l’inserimento.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 38/68 
 
 
A seguito dell’inserimento, il sistema mostrerà una pagina di dettaglio dell’ordinanza di ammissione 
provvisoria, mostrando anche la data di esecutività inserita, la data trasmissione, gli eventuali destinatari 
 
Dalla pagina di dettaglio, deve essere possibile accedere alla funzione di modifica della data di esecutività, 
inoltre deve essere abilitata la stampa, la validazione e la trasmissione telematica verso la Procura titolare 
del titolo esecutivo per cui è stata presentata istanza di applicazione di misura alternativa. La stampa deve 
includere anche una nuova nota di trasmissione del provvedimento contenente, oltre alla data dell’ordinanza 
e a quella di deposito, anche quella di esecutività. La gestione della ‘ricezione’ e ‘lavorazione’ dell’ordinanza 
di ammissione provvisoria su SIEP è illustrata al par. Errore. L'origine riferimento non è stata trovata. [REQ-S
IE-009-13]. 
Per quanto riguarda la trasmissione verso la Procura, si ricorda che nell’ambito della stessa BDI 
l’aggiornamento sul titolo esecutivo avviene automaticamente, per cui non vi è bisogno di alcuna azione 
aggiuntiva, mentre nel caso di trasmissione verso altra BDI è possibile ritrasmettere l’ordinanza accedendo 
al Dettaglio Deposito Ordinanza.  
La data di esecutività impostata, inoltre, dovrà essere visualizzata nella porzione della maschera di dettaglio 
del procedimento SIUS dedicata ai provvedimenti, come mostrato nella figura che segue: 
 
 
Figura 18: Sezione Provvedimenti con Data di Esecutività 
 
 
La stessa informazione dovrà essere replicata nella pagina di dettaglio provvedimento, che il sistema mostra 
in corrispondenza del link Provvedimenti.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 39/68 
 
 
 
 
Figura 19: Pagina Dettaglio Provvedimenti con Data di Esecutività 
 
 
A seguito dell’emissione dell’ordinanza provvisoria e a partire dalla data in cui diviene esecutiva, si possono 
delineare diverse possibili gestioni operative, tra cui quelle che seguono: 
 
- 
Il Tribunale di Sorveglianza, conferma senza formalità la decisione del magistrato (REQ-SIES-009-05) 
- 
Incorrere in una revoca dell’ammissione provvisoria, nel caso, ad esempio, di gravi violazioni delle 
prescrizioni nel corso dell’esecuzione provvisoria.  
 
In questa prima fase di implementazione, illustriamo il dettaglio del primo scenario, ossia la casistica di 
‘Conferma’ da parte del Tribunale della decisione del magistrato designato. 
Lo scenario di cui al punto 2 è rinviato alla successiva fase di sviluppo (D.lgs. 123/2018 - FASE 2) cosi come 
specificato al par.5.2. 
4.2.5 
REQ-SIE-009-05 TDS/TDSM - Provvedimento di Conferma Ordinanza Applicazione 
Provvisoria 
A seguito dell’emissione dell’ordinanza provvisoria e a partire dalla data in cui diviene esecutiva, il Tribunale, 
con decisione del collegio, conferma la decisione del Magistrato Designato. 
 
Per proseguire con l’emissione del provvedimento di conferma, l’utente TDS/TDSM, dopo aver fissata una 
data udienza, deve procedere con la funzione di emissione ordinanza conferma decisione sullo stesso 
procedimento su cui è stata inserita l’ordinanza di applicazione provvisoria della misura (con data esecutività 
inserita).

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 40/68 
 
 
In particolare, il requisito in oggetto, REQ-SIE-009-05, va ad estendere quanto già definito al requisito REQ-
SIE-009-01 in quanto, per il contenuto “Concessione misure alternative (art. 678 comma 1-ter c.p.p.)” e per 
il contenuto “Concessione misure penali di comunità/misure alternative alla detenzione (art. 678 comma 
1 ter c.p.p.)” devono essere previsti nuovi oggetti ed un nuovo esito. 
Gli oggetti da prevedere sono: 
- 
Conferma appl. provv. Affidamento in Prova al S.S. (Art. 47 O.P. -  Art. 678 comma 1-ter c.p.p.) 
- 
Conferma appl. provv. Affidamento in Prova al S.S. (Art. 94 DPR 309/90 - Art. 678 comma 1-ter c.p.p.) 
- 
Conferma appl. provv. Detenzione Domiciliare (Art. 47 ter O.P. - Art. 678 comma 1-ter c.p.p.) 
- 
Conferma appl. provv. Semiliberta' (Art. 50 comma 1 O.P. - Art. 678 comma 1-ter c.p.p.) 
- 
Conferma appl. provv. Sospensione dell'Esecuzione della Pena (Art. 90 DPR 309/90 - Art. 678 comma 
1-ter c.p.p.) 
mentre l’esito è 
Conferma Decisione del Magistrato Relatore 
 
Per emettere l’ordinanza bisogna selezionare nel menu Ordinanze  
 
 
Figura 20: Menù Emissione Ordinanza Provvisoria - (TDS e TDSM) 
 
la funzione ‘Applicazione Provvisoria M.A – Conferma Decisione Magistrato Relatore’, che presenta il 
seguente sottomenu: 
 
 
da cui, selezionando la funzione ‘Conferma Decisione Magistrato Relatore’ , il sistema, dopo aver controllato 
che sul procedimento risulti inserita l’ordinanza di applicazione provvisoria, la data di esecutività e la data 
dell’udienza (in caso di assenza di uno dei 3 dati invierà un messaggio bloccante all’operatore), in particolare:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 41/68 
 
 
 
- 
in caso di assenza della data di esecutività dell’ordinanza di Applicazione Provvisoria 
 
 
- 
in caso che l’ordinanza di Applicazione Provvisoria non sia validata o deposita o il deposito non 
validato 
 
 
- 
nel caso che non sia stata prefissata l’udienza 
 
Poiché l’udienza di Conferma è di tipo camerale, per indicare la data di svolgimento bisogna utilizzare la 
funzione di Prefissazione. Nel caso che l’utente selezioni la funzione di Fissazione udienza, il sistema invierà 
il seguente messaggio.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 42/68 
 
 
 
Se la data dell’udienza è precedente alla data esecutività il sistema invierà il seguente messaggio 
 
 
Superati tutti controlli, il sistema presenterà la form per l’inserimento dell’ordinanza 
 
 
Figura 21: Pagina Emissione Ordinanza di Conferma Decisione Magistrato Relatore 
 
che permette di inserire le seguenti informazioni: 
- 
Data Emissione (dato obbligatorio) 
- 
Eventuale descrizione a testo libero (dato opzionale). 
da notare che l’oggetto sarà valorizzato automaticamente dal sistema in base al corrispondente oggetto 
applicato provvisoriamente con la ordinanza da confermare.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 43/68 
 
 
 
A seguito della Conferma dei dati in maschera, il sistema inserirà nella base dati, oltre ai dati dell’ordinanza, 
il nuovo oggetto ed il nuovo esito e presenterà la form di Dettaglio 
 
 
 
Dopo la validazione dell’ordinanza ed al suo deposito, il procedimento risulterà chiuso, in stato di “Emesso 
Provvedimento”. 
 
Il flusso di lavorazione del procedimento SIUS che abbia il nuovo contenuto ‘Concessione Misura Alternativa 
(art. 678 comma 1-ter c.p.p.) ’ oppure ‘Concessione misure penali di comunità/misure alternative alla 
detenzione (art. 678 comma 1 ter c.p.p.)’ ed oggetto ‘Conferma Decisione del Magistrato relatore’, seguirà 
quello attualmente in essere per il contenuto ‘Concessione Misure Alternative Alla Detenzione’ (C001) con 
la gestione della modifica, visualizzazione, cancellazione, stampa, validazione e trasmissione. Le pagine di 
modifica, visualizzazione e la funzione di stampa devono prevedere in aggiunta a quanto ad oggi presente, 
l’informazione circa il numero e l’anno dell’ordinanza di applicazione provvisoria. 
La funzione di trasmissione, deve prevedere l’invio dell’ordinanza di Conferma (Ratifica), verso la Procura 
titolare del titolo esecutivo per cui è stata presentata istanza di applicazione di misura alternativa. 
 
4.2.5.1 
Adeguamento funzione invio/trasmissione ordinanza/decreto di Conferma - SIUS 
In merito alla funzione di trasmissione dell’ordinanza di ‘Conferma/Ratifica’, occorre considerare un ulteriore 
intervento tecnico - funzionale relativamente all’invio dei dati in formato xml.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 44/68 
 
 
Nella creazione del messaggio di scambio, per mezzo delle code jms, in concomitanza dell’invio del 
provvedimento di ‘conferma/ratifica’ è necessario ‘trasmettere’ anche gli estremi dell’ordinanza di 
applicazione provvisoria.  
La gestione della ‘ricezione’ e ‘lavorazione’ dell’ordinanza di ‘Conferma’ su SIEP è illustrata al par.Errore. L
'origine riferimento non è stata trovata. [REQ-SIE-009-13].  
4.2.6 
REQ-SIE-009-06 - REQ-SIE-009-07 (Statistiche Misura Alternativa - art. 678 comma 1-
ter c.p.p.) ) 
Per i requisiti in oggetto, per i TDS/TDSM, il sistema SIUS deve prevedere due nuove tipologie di statistiche 
attinenti a procedimenti SIUS con contenuto ‘Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) ’, 
per TDS, e con contenuto ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 
678 comma 1 ter c.p.p.) ’ per TDSM. 
In particolare in corrispondenza del menù ‘Statistiche/Monitoraggio’ deve essere previsto un nuovo tasto 
funzione denominato ‘Monitoraggio Misure Alternative (art. 678 comma 1-ter c.p.p.)’ così come raffigurato  
nella figura che segue: 
 
 
Figura 22: Menù Statistiche TDS/TDSM 
 
Con l’accesso alla funzione, il sistema mostrerà una pagina di ricerca tramite la quale l’utente potrà inserire 
i dati relativi all’intervallo di tempo o estremi del procedimento da verificare, e sceglie la statistica di 
interesse. 
Le statistiche afferenti ai procedimenti di Misure Alternative (art. 678 comma 1-ter c.p.p.) saranno, 
limitatamente a questa prima fase, di cinque tipologie:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 45/68 
 
 
 
- 
Statistica Procedimenti privi di provvedimenti 
- 
Statistica Ordinanze Non Emesse – Trasmessi atti al Presidente [requisito REQ-SIE-009-06]; 
- 
Statistica Ordinanze Non Emesse [requisito REQ-SIE-009-06]; 
- 
Statistica Ordinanze Emesse ma prive di data di esecutività; 
- 
Statistica Ordinanze Emesse con data di esecutorietà inserita, ma privi di decisione da parte del 
Collegio [requisito REQ-SIE-009-07]; 
 
Nella fase successiva di sviluppo sarà prevista un’ulteriore statistica che afferisce alle Ordinanze di Revoca di 
Ammissione Provvisoria misura alternativa – Art. 678 comma 1 ter c.p.p.. 
A seguire si prospetta una pagina di esempio per la scelta della statistica di interesse: 
 
 
Figura 23: Pagina di Ricerca per Statistiche - (TDS e TDSM) 
 
A seguito dell’inserimento dei criteri di interesse, e con la sottomissione dei dati al sistema, sarà generata 
una pagina di elenco con i procedimenti trovati. 
Dalla pagina di elenco l’utente poi avrà la possibilità di visualizzare il dettaglio di ogni singolo procedimento 
SIUS trovato e di esportare il risultato ottenuto in un file excel.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 46/68 
 
 
 
Figura 24: Pagina Elenco Procedimenti per statistiche - (TDS e TDSM) 
 
Il layout della pagina riportata, in linee generali, sarà il medesimo per tutte le tipologie di statistiche previste. 
Per quanto riguarda il foglio excel, le informazioni estratte saranno mostrate secondo il seguente formato. 
 
 
Figura 25: esempio foglio excel 
 
Per tutte le statistiche, si fa presente, che le estrazioni faranno riferimento allo stato in cui si trova il fascicolo 
nel momento di elaborazione della statistica; il totale dei fascicoli conteggiati sarà calcolato e mostrato 
direttamente a video. 
 
4.2.6.1 
REQ-SIE-009-06 TDS/TDSM - Statistica Procedimenti privi di provvedimenti 
La statistica in oggetto estrae tutti i procedimenti in stato di iscritto, senza data udienza (anche prefissata) e 
privi di provvedimenti (decreto/ordinanza).

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 47/68 
 
 
4.2.6.2 
REQ-SIE-009-06 TDS/TDSM - Statistica Ordinanze Non Emesse (Restituiti Atti al Presidente) 
La statistica in oggetto va a recuperare la lista dei procedimenti SIUS iscritti dai TDS con contenuto di 
‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ e dai TDSM con contenuto ‘Concessione 
misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.)’ , per i quali 
risulta valorizzata la DATA_RESTITUZIONE sulla tabella  Generale_Procedimento, inserita tramite 
un’ordinanza di applicazione provvisoria di misura alternativa il cui esito è ‘Restituiti Atti al Presidente’ o con 
la funzione Gestione Restituzione Atti al Presidente. 
Tali procedimenti sono individuabili anche dallo stato del procedimento che è posto a ‘Atti restituiti al 
Presidente’. 
 
4.2.6.3 
REQ-SIE-009-06 TDS/TDSM - Statistica Ordinanze Non Emesse  
 
Rientrano in questa categoria i procedimenti SIUS iscritti da TDS/TDSM, rispettivamente con contenuto di 
‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ e ‘Concessione misure penali di 
comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.) ‘, per i quali risulta inserito il 
decreto di designazione magistrato, ma non sia mai stata emessa ordinanza. Infatti, il magistrato designato 
qualora ritenga di non poter applicare alcuna misura, non è tenuto ad emettere un’ordinanza di contenuto 
negativo, ma può semplicemente lasciar decorrere il tempo assegnatogli. Anche quest’ultimi, infatti, 
‘ritornano’ al Presidente del Tribunale Sorveglianza. 
 
4.2.6.4 
REQ-SIE-009-06 TDS/TDSM - Statistica Ordinanze emesse ma prive di data esecutività  
Rientrano in questa categoria i procedimenti SIUS iscritti da TDS/TDSM, rispettivamente con contenuto di 
‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ e ‘Concessione misure penali di 
comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.) ‘,per i quali risulta inserita 
un’ordinanza di applicazione provvisoria di misura alternativa il cui esito è ‘Applica provvisoriamente’ la 
misura ma non risulta inserita la data di esecutività.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 48/68 
 
 
4.2.6.5 
REQ-SIE-009-07 TDS/TDSM - Statistica Ordinanze Provvisorie Esecutive senza decisione del 
Collegio 
 
La statistica in oggetto va a recuperare la lista dei procedimenti SIUS iscritti dai TDS con contenuto di 
‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ e dai TDSM con contenuto ‘Concessione 
misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.)’ , per i quali 
risulta inserita un’ordinanza di applicazione provvisoria di misura alternativa il cui esito è ‘Applica 
Provvisoriamente’ e la relativa data di esecutività, ma sono privi dell’ ordinanza di ‘Conferma’ da parte del 
Collegio o comunque una qualsivoglia decisione da parte del Collegio. 
Queste ordinanze sono individuabili, oltre che dall’esito dell’ordinanza corrispondente a ‘Applica 
Provvisoriamente ’, anche dalla presenza di una data di esecutività inserita in corrispondenza del record di 
interesse sulla tabella deposito_ordinanza_pc.  
Inoltre per il procedimento SIUS da estrarre, non deve esistere un evento che lo lega ad un procedimento 
SIUS con esito ‘Conferma Decisione del Magistrato Relatore’.  
I procedimenti di interesse per questa statistica devono essere tutti quelli per i quali è ‘mancante’ una 
decisione da parte del Collegio. 
Per questa tipologia di statistica, sia nella pagina di elenco che nel relativo foglio Excel, in output deve essere 
mostrata anche la data di inizio esecutività. 
4.2.7 
REQ-SIE-009-08 TDS/TDSM (Aggiornamento Statistica Movimento Provvedimenti per 
Oggetti) 
A seguito dei nuovi interventi previsti per la scheda in oggetto, sarà necessario aggiornare le attuali funzioni 
Statistiche basate sul conteggio per oggetti, in modo da integrare la nuova tipologia di definizione con 
ordinanza provvisoria emessa dal magistrato designato. 
4.2.7.1 
Monitoraggio Provvedimenti per Oggetti 
Occorrerà intervenire sulla maschera di ricerca della statistica, vedi immagine successiva, per fare in modo 
che il contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’, in caso di TDS, oppure 
‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.) ’, 
per TDSM, appaia nella lista degli oggetti selezionabili.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 49/68 
 
 
 
Figura 26: Statistica movimento provvedimenti per Oggetti 
Parallelamente gestire la nuova informazione anche suI files Excel che vengono generati a seguito della 
Conferma della statistica. In particolare sui fogli Dettaglio, Totali per Magistrato ed ElencoProc.PerOggetto. 
Nel foglio Dettaglio verrà aggiunta la nuova colonna Accolti Provvisoriamente per  tener conto degli oggetti 
definiti con l’ordinanza di Applicazione Provvisoria, che saranno conteggiati ai fini dei definiti e dei pendenti 
fine periodo

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 50/68 
 
 
 
Figura 27: Statistica movimento provvedimenti per Oggetti - Dettaglio 
Analogamente si interverrà nel foglio Totali per Magistrato 
 
 
Figura 28: Statistica movimento provvedimenti per Oggetti – Totali per Magistrato 
 
Nel foglio ElencoProc.PerOggetto si interverrà per estrarre i procedimenti relativi ai nuovi oggetti, anche in 
assenza dell’ordinanza di Conferma dell’applicazione provvisoria da parte del collegio, catalogarli come 
definiti in presenza della sola applicazione provvisoria e distinguerli da quelli definiti con rito ordinario

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 51/68 
 
 
 
Figura 29: Elenco procedimenti per oggetto 
 
4.2.7.2 
Statistica Comparata Magistrati 
La funzione sarà aggiornata per aggiungere  il conteggio degli oggetti definiti con ordinanza di applicazione 
provvisoria della misura e tenerne conto nel calcolo dei procedimenti definiti e dei pendenti a fine periodo. 
A tal fine sarà aggiunta alla form che presenta il risultato dell’elaborazione la nuova colonna Accolti 
Provvisoriamente 
 
Figura 30: Statistica Comparta Magistrati (Videata)

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 52/68 
 
 
 
Analogamente si è interverrà nel foglio excel, che è possibile generare dalla precedente form 
 
Figura 31: Statistica Comparta Magistrati (file excel) 
 
4.2.8 
REQ-SIE-009-09 TDS/TDSM Modifica pagina richiesta atti istruttori 
Per gli UDS, UDSM, TDS e TDSM, con il requisito in oggetto si chiede di intervenire sulla pagina di inserimento 
della richiesta di alcuni atti istruttori. La funzione è raggiungibile dal menù Fase istruttoria » Richiesta Atti, e 
gli atti istruttori interessati dalla modifica sono: 
1) Accertamento progr. terapeutico 
 
2) Certificato Carichi Pendenti 
3) Conferma disponibilità SER.T 
4) Cumulo 
5) Estratto/Copia Provvedimento  
6) Idoneità progr. terapeutico 
7) Informazioni art. 47 - 4c. 
8) Informazioni detenzione domiciliare 
9) Informazioni su attività lavorativa 
10) InformazioniPS per 47-47 Ter-50- 30 Ter 
11) Ordin/decr. altro TdS/UdS 
12) Relazione sanitaria 
13) Relazione CSSA 
14) Sentenza Integrale 
15) Verifica condotta progr. Ser.T

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 53/68 
 
 
16) Visita medica   
17) Altre Istruttorie 
Nello specifico, nella pagina di inserimento della richiesta di ognuno di questi atti istruttori, deve essere 
previsto un nuovo campo ckeckbox, selezionando il quale deve essere mostrata una sezione ove indicare la 
data di restituzione dell’atto. 
 
Figura 32: Pagina Richiesta Atti Istruttori 
In fase di conferma, l’informazione aggiuntiva deve essere registrata nella tabella EVENTO, come esplicitato 
al par. 4.6.9. A tal fine sarà aggiunta la nuova colonna DATA_RESTITUZIONE_AI.  
I dati inseriti devono inoltre essere riportati nella pagina di dettaglio della richiesta così come mostrato nella 
pagina che segue:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 54/68 
 
 
 
Figura 33: Dettaglio Richiesta Atti Istruttori 
 
La data di restituzione dell’atto, più recente, già valorizzata in una delle sopra elencate richieste, deve essere 
riproposta (precompilata) nelle maschere delle successive richieste, con possibilità di essere modificata. 
Inoltre sul documento di stampa del modulo di richiesta, deve essere riportata l’informazione registrata, ossia 
la data entro cui deve essere restituito l’atto istruttorio prevedendo, su ogni template una frase ad ‘hoc’.  
A tal proposito sarà necessario intervenire in modifica sui seguenti template: 
• 
SIUS_IS_ACCERTPROGTERAPEUT.rtf 
• 
SIUS_IS_CERCARICHIPENDENTI.rtf 
• 
SIUS_IS_CONFERMDISPONISERT.rtf 
• 
SIUS_IS_CUMULO.rtf 
• 
SIUS_IS_ESTRATTOSENTENZA.rtf 
• 
SIUS_IS_IDONEIPROGCOMTERAP.rtf 
• 
SIUS_IS_INFORMAZIONART474C.rtf 
 
• 
SIUS_IS_CONCEDETENZDOMICIL.rtf 
 
• 
SIUS_IS_INFORATTIVITALAVORATIVA.rtf 
• 
SIUS_IS_PSPERART47E5030TER.rtf 
• 
SIUS_IS_ORDINEDECRETDSUDS.rtf 
• 
SIUS_IS_RELAZIONESANITARIA.rtf 
• 
SIUS_IS_RELAZIONECSSA.rtf

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 55/68 
 
 
• 
SIUS_IS_SENTENZAINTEGRALE.rtf 
• 
SIUS_IS_VERIFICONDPROGSERT.rtf 
• 
SIUS_IS_VISITAMEDICA.rtf 
• 
SIUS_IS_TDSGENERICO1.rtf 
• 
SIUS_IS_TDSGENERICO2.rtf 
• 
SIUS_IS_TDSGENERICO3.rtf 
• 
SIUS_IS_TDSGENERICO4.rtf 
• 
SIUS_IS_TDSGENERICO5.rtf 
• 
SIUS_IS_TDSGENERICO6.rtf 
• 
SIUS_IS_TDSGENERICO7.rtf 
• 
SIUS_IS_TDSGENERICO8.rtf 
• 
SIUS_IS_TDSGENERICO9.rtf 
• 
SIUS_IS_TDSGENERICO10.rtf 
Si riporta un esempio di frase da aggiungere su ogni singolo template: 
N. SIUS    XXXX/YYYYY 
- TDS TORINO 
 
 
TRIBUNALE DI SORVEGLIANZA DI TORINO 
VIA BOLOGNA, 47 - 10152 - TORINO  
_____________________________________ 
 
Tel. 011-4327812/011-4327814/011-4327877 - Fax - 011-4327834 
 
 
TORINO, 04-04-2020 
 
Servizio Tossicodipendenze Presso Asl - PINEROLO 
 
 
 
INFORMAZIONI COMUNITA’ 
 
 
N. 2016/6 Declaratoria Estinzione della Pena

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 56/68 
 
 
 
relativo a:  
 
XXX CCCCC 
luogo di nascita: 
PETROSANI(ROMANIA) 
data di nascita:  
17-10-1982 
 
residente in : 
 
in via Boccardo n. 26 bis TORINO 
 
 
Al fine eventuale concessione beneficio affidamento in prova al servizio sociale (art. 94 T.U. 309/90) pregasi 
comunicare con cortese urgenza se il soggetto sotto generalizzato sia attualmente ospite di codesta Comunità 
o se segua (o abbia seguito) programma terapeutico. 
 
In caso positivo, pregasi far pervenire: 
 
❑ Certificazione di tossicodipendenza relativa al nominato di cui sopra rilasciata da una struttura 
sanitaria pubblica. 
❑ Copia del programma terapeutico concordato con l'interessato, con l'attestazione di idoneità della 
U.S.L. competente. 
❑ Relazione sull'andamento del piano terapeutico di recupero. 
 
 
Si chiede di restituire l’atto richiesto entro il giorno    28-05-2020 
 
Rispondere stesso mezzo al nr. fax : 011-4327834 
 
Figura 34: Esempio template atto istruttorio 
 
4.2.9 
REQ-SIE-009-10 TDS/TDSM Statistica Atti Istruttori con Data Restituzione 
Per i TDS e TDSM, con il requisito in oggetto si chiede di integrare nel menù di Statistiche/Monitoraggio » 
Ricerche una nuova tipologia di ricerca ‘Atti istruttori con data restituzione’. 
Nella pagina a cui si accede dal menù su indicato, deve essere aggiunto un nuovo tasto funzione così come 
mostrato nella figura che segue:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 57/68 
 
 
 
 
Figura 35: Funzione Ricerca Atti Istruttori con data restituzione 
 
Il tasto da introdurre, sarà il punto di accesso alla nuova ricerca da implementare la quale si occuperà di 
recuperare e conteggiare quali siano i procedimenti SIUS per i quali sia stata fatta richiesta di un atto 
istruttorio e per la quale richiesta è stata inserita una data di restituzione. Il totale dei fascicoli conteggiati 
sarà calcolato e mostrato direttamente a video. 
L’accesso alla funzione mostrerà una pagina di ricerca in cui immettere i dati per avviare la statistica di 
interesse. 
 
 
Figura 36: Pagina ricerca Atti Istruttori con data restituzione 
 
 
I possibili criteri di ricerca saranno: 
 
- 
Intervallo Estremi Procedimenti 
- 
Intervallo Date Iscrizione 
- 
Intervallo Date di Restituzione

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 58/68 
 
 
Con il tasto ‘Ricerca’ sarà attivata la funzione di estrazione dati che va a recuperare gli estremi del 
procedimento SIUS, la data emissione della richiesta istruttoria, la data restituzione, cognome  e nome del 
soggetto, contenuto del procedimento, il tipo di atto istruttorio richiesto e lo stato del procedimento. 
 
Le informazioni recuperate devono essere mostrate in una pagina di elenco ed inoltre deve essere prevista 
la funzione di export in formato excel dei risultati ottenuti. 
 
 
Figura 37: Elenco procedimenti con atti istruttori con data restituzione 
 
Dalla pagina di elenco, l’utente potrà accedere al dettaglio del procedimento SIUS utilizzando il link posto in 
corrispondenza del Numero/Anno SIUS.  
4.2.10 
REQ-SIE-009-11 (UDS/UDSM – TDS/TDSM Integrazione Lista Mittenti) 
«Art. 57 (Legittimazione alla richiesta di misure). - 1. Le misure alternative e quelle di cui agli articoli 30, 30-
ter, 52, 53 e 54 nonché' all'articolo 6 del decreto del Presidente della Repubblica 30 maggio 2002, n. 115, 
possono essere richieste dal condannato, dall’internato, dai loro prossimi congiunti, dal difensore, ovvero 
proposte dal gruppo di osservazione e trattamento.». 
Secondo quando disposto all'art. 7 comma 1 lettera b) del D.lgs. 2 ottobre 2018, n. 123, nell’attuale maschera 
di iscrizione dei procedimenti SIUS, è necessario integrare le voci presenti in combo ‘Mittente’ con una nuova 
voce denominata ‘Gruppo di Osservazione e Trattamento’.  Verificare che la modifica sia valida da tutti i 
punti di accesso alla pagina. (Es: Iscrizione da procedimento SIEP e Iscrizione da Soggetto).

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 59/68 
 
 
 
Figura 38: Pagina iscrizione Procedimento SIUS 
 
 
 
 
 
 
 
 
 
 
4.3 
Gestione dei Template – Sottosistema SIUS  
Con lo scopo di facilitare l’individuazione degli interventi affini al ‘modulo’ dei template, per ogni requisito si 
esplicita la necessità di creazione di nuovi template o alla modifica di template già esistenti. 
 
REQ-SIE-009-01 TDS/TDSM - Concessione misure alternative (art. 678 comma 1-ter c.p.p.)

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 60/68 
 
 
- 
Per provvedimenti con contenuto di Concessione misure alternative (art. 678 comma 1-ter c.p.p.) 
che seguono, per varie ipotesi il ‘rito ordinario’, saranno agganciati i templati ad oggi già presenti a 
sistema per le ordinanze di ‘Affidamento in Prova’, ‘Semilibertà, ‘Detenzione Domiciliare e 
‘Sospensione Pena’; 
 
REQ-SIE-009-02 TDS/TDSM - Emissione del Decreto Presidenziale di Designazione 
- 
Creazione di un nuovo template per ‘Decreto di Designazione’ da agganciare alla stampa del dettaglio 
del decreto; 
- 
Integrazione di informazioni su template di stampa fascicolo (SIUS_ST_STAMPAFASCICOLO.rtf) per 
visualizzare il magistrato designato; 
 
REQ-SIE-009-03 TDS/TDSM - Emissione Ordinanza Applicazione Provvisoria  
- 
Creazione di un nuovo template per ‘Ordinanza di Ammissione Provvisoria’ per Affidamento al 
Servizio Sociale 
- 
Creazione di un nuovo template per ‘Ordinanza di Ammissione Provvisoria’ per Detenzione 
Domiciliare 
- 
Creazione di un nuovo template per ‘Ordinanza di Ammissione Provvisoria’ per Semilibertà 
- 
Creazione di un nuovo template per ‘Ordinanza di Ammissione Provvisoria’ per Sospensione 
Esecuzione Pena 
 
REQ-SIE-009-04 TDS/TDSM - Registrazione data Esecutività Ordinanza Applicazione Provvisoria 
- 
Intervenire sui template di cui al REQ-SIE-009-03, prevedendo la stampa della data di esecutività 
inserita a sistema. 
- 
Integrazione di informazioni sul template di stampa fascicolo (SIUS_ST_STAMPAFASCICOLO.rtf) per 
visualizzare la data di esecutività. 
 
REQ-SIE-009-05 TDS/TDSM - Provvedimento di Conferma Ordinanza Applicazione Provvisoria 
- 
Creazione di un nuovo template per ordinanza di ‘Conferma’ per Concessione Misura Alternativa (art. 
678 comma 1-ter c.p.p.) relativamente all’ Affidamento al Servizio Sociale

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 61/68 
 
 
- 
Creazione di un nuovo template per decreto di ‘Conferma’ per Concessione Misura Alternativa (art. 
678 comma 1-ter c.p.p.) relativamente all’ Affidamento al Servizio Sociale 
- 
Creazione di un nuovo template per ordinanza di ‘Conferma’ per Concessione Misura Alternativa (art. 
678 comma 1-ter c.p.p.) relativamente alla Detenzione Domiciliare; 
- 
Creazione di un nuovo template per decreto di ‘Conferma’ per Concessione Misura Alternativa (art. 
678 comma 1-ter c.p.p.) relativamente alla Detenzione Domiciliare; 
- 
Creazione di un nuovo template per ordinanza di ‘Conferma’ per Concessione Misura Alternativa (art. 
678 comma 1-ter c.p.p.) relativamente alla Semilibertà; 
- 
Creazione di un nuovo template per decreto di ‘Conferma’ per Concessione Misura Alternativa (art. 
678 comma 1-ter c.p.p.) relativamente alla Semilibertà; 
- 
Creazione di un nuovo template per ordinanza di ‘Conferma’ per Concessione Misura Alternativa (art. 
678 comma 1-ter c.p.p.) relativamente alla Sospensione dell’Esecuzione della Pena; 
- 
Creazione di un nuovo template per decreto di ‘Conferma’ per Concessione Misura Alternativa (art. 
678 comma 1-ter c.p.p.) relativamente alla Sospensione dell’Esecuzione della Pena; 
- 
Integrazione di informazioni su template di stampa fascicolo (SIUS_ST_STAMPAFASCICOLO.rtf) per 
visualizzare la decisione di conferma. 
 
REQ-SIE-009-09 TDS/TDSM Modifica pagina richiesta atti istruttori 
Per questo requisito si rimanda al par. 4.2.8, dove esiste già un elenco completo dii template da 
modificare. 
 
Ci si riserva, in ogni caso, la possibilità di dover intervenire per ulteriori integrazioni. 
Inoltre ci si riserva di verificare, in fase di realizzazione della MEV, la necessità di creare nuovi template 
piuttosto che intervenire, utilizzando delle variabili ad hoc, sui template già esistenti. 
 
4.4 
Moduli sw  
L’intervento software riguarderà il progetto SIES. In particolare per quanto attiene a questa prima fase, le 
classi coinvolte saranno relative soprattutto ai package java relativi a sius e siep. 
Il pacchetto interessato è, in ogni caso, il sies.war.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 62/68 
 
 
4.5 
Interfacce utente 
Le interfacce utente sono state esplicitate nella descrizione dell’intervento per ogni singolo requisito. 
4.6 
Basi dati 
Nel seguente paragrafo sono elencate le attività inerenti alla banca dati per ogni requisito individuato ai 
paragrafi precedenti. 
4.6.1 
Base Dati - REQ-SIE-009-01 TDS - Concessione misure alternative (art. 678 comma 1-
ter c.p.p.) e TDSM - Concessione misure penali di comunità/misure alternative alla 
detenzione (art. 678 comma 1 ter c.p.p.) 
Per censire i due nuovi contenuti, nella tabella cg_ref_codes, devono essere aggiunti due nuovi valori per il 
dominio OGGETTO_PROCEDIMENTO. 
Sempre nella tabella cg_ref_codes, devono essere mappati gli oggetti relativi ai nuovi contenuti, prevedendo 
dei nuovi record per il dominio MOTIVO_PROVVEDIMENTO.  
Sempre nella tabella cg_ref_codes, devono essere mappati gli esiti relativi ai nuovi contenuti, prevedendo 
dei nuovi record per i domini ESITO_TENORE ed ESITO_PROVVEDIMENTO. 
4.6.2 
Base Dati - REQ-SIE-009-02 (TDS/TDSM - Emissione del Decreto Presidenziale di 
Designazione) 
Per censire la nuova funzione (Decreto Presidenziale di Designazione) occorre registrare l’informazione sulle 
seguenti tabelle: 
✓ funzione  
✓ funzione_profilo  
✓ relazione_funzioni 
In fase di iscrizione del Decreto, il sistema registra i dati nella tabella DEPOSITO_DECRETO, EVENTO e TENORE

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 63/68 
 
 
La tabella DEPOSITO_DECRETO deve prevedere dei nuove colonne per registrare la data di Termine  o il 
numero giorni entro cui Emettere l’ordinanza di Applicazione Provvisoria (DATA_TERMINE_EMISSIONE, 
NUM_GIORNI_TERMINE_EMISSIONE). 
Per censire il nuovo stato procedimento, nella tabella cg_ref_codes, deve essere aggiunto un nuovo valore 
per il dominio STATO_FASCICOLO (22, Emesso Decreto Designazione). 
Per censire il nuovo esito, nella tabella cg_ref_codes, deve essere aggiunto un nuovo valore per il domini0 
ESITO_PROVVEDIMENTO   (0610, Designa Magistrato  art. 678 1-ter). 
Per censire il nuovo stato procedimento, nella tabella cg_ref_codes, deve essere aggiunto un nuovo valore 
per il dominio TIPO_DECRETO (Decreto Designazione). 
Per la registrazione del nuovo template da associare al decreto di designazione magistrato, occorre 
prevedere un nuovo record nella tabella TEMPLATE. 
4.6.3 
Base Dati - REQ-SIE-009-03 (TDS/TDSM - Emissione Ordinanza Applicazione 
Provvisoria/Restituzione Atti al Presidente) 
Per censire la nuova funzione (Ordinanza Applicazione Provvisoria M.A.) occorre registrare l’informazione 
sulle seguenti tabelle: 
✓ funzione  
✓ funzione_profilo  
✓ relazione_funzioni 
Prevedere una nuova Tipologia Ordinanza: ordinanza provvisoria  
Per la creazione della nuova tipologia di ordinanza (ordinanza provvisoria), censire il dato nella tabella 
cg_ref_codes, nella quale deve essere aggiunto un nuovo valore per il dominio TIPO_ATTO. 
Aggiungere nuove colonne in tabella GENERALE_PROCEDIMENTO per gestire la data ‘Atti trasmessi al 
Presidente’ e le eventuali note (DATA_RESTITUZIONE, DESCR_RESTITUZIONE).

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 64/68 
 
 
Per censire il nuovo stato procedimento, nella tabella cg_ref_codes, devono essere aggiunti due nuovi valori 
per il dominio STATO_FASCICOLO (‘23, Restituiti Atti al Presidente’, ’24, Emessa Ordinanza Applicazione 
Provvisoria’). 
Per la registrazione i nuovi template da associare alle ordinanze di Applicazione Provvisoria, occorre 
prevedere nuovi record nella tabella template. 
4.6.4 
Base Dati - REQ-SIE-009-04 (TDS/TDSM - Registrazione data Esecutività Ordinanza 
Applicazione Provvisoria) 
Per censire la nuova funzione (Registrazione data Esecutività Ordinanza Applicazione Provvisoria) occorre 
registrare l’informazione sulle seguenti tabelle: 
✓ funzione  
✓ funzione_profilo  
✓ relazione_funzioni 
Aggiungere nuove colonne in tabella deposito_ordinanza_pc per gestire i campi di Data Esecutività 
dell’ordinanza (DATA_ESECUTIVITA, NOTE_DATA_ESECUTIVITA). 
4.6.5 
Base Dati - REQ-SIE-009-05 (TDS/TDSM - Provvedimento di Conferma Ordinanza 
Applicazione Provvisoria) 
Per questo requisito sono previsti nuovi valori ad integrazione delle attività già descritte in REQ-SIE-009-01. 
Quindi per questo requisito sono da considerare le attività del requisito REQ-SIE-009-01. 
4.6.6 
Base Dati - REQ-SIE-009- 06 (TDS/TDSM - Statistica Ordinanze Non Emesse (Trasmessi 
Atti al Presidente)) 
Nessun intervento strutturale a tabelle. 
4.6.7 
Base Dati - REQ-SIE-009- 07 (TDS/TDSM - Statistica Ordinanze Provvisorie Esecutive 
senza decisione del Collegio) 
Nessun intervento strutturale a tabelle.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 65/68 
 
 
4.6.8 
Base Dati - REQ-SIE-009- 08 (Aggiornamento Statistica Movimento Provvedimenti per 
Oggetti) 
Modificare la procedura stato_oggetti_sius presente nel package Oracle ISPETTORATO_SIUS. 
4.6.9 
Base Dai - REQ-SIE-009- 09 (Modifica pagina Richiesta Atti Istruttori) 
Per registrare il valore del nuovo campo previsto per il requisito in oggetto, nella tabella EVENTO, deve essere 
aggiunto una nuova colonna DATA_RESTITUZIONE_AI. 
4.6.10 
Base Dati - REQ-SIE-009- 10 (Statistica Atti Istruttori con Data Restituzione) 
Per censire la nuova funzione (Statistica Atti Istruttori) occorre registrare l’informazione sulle seguenti 
tabelle: 
✓ funzione  
✓ funzione_profilo  
✓ relazione_funzioni 
4.6.11 
Base Dati - REQ-SIE-009-11 (UDS – TDS Integrazione Lista Mittente Atto) 
Per censire la nuova voce da visualizzare nella combo box ‘mittente’, nella tabella cg_ref_codes, deve essere 
aggiunto un nuovo valore per il dominio MITTENTE_ATTO.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 66/68 
 
 
5 Piano delle attività 
5.1 
Ciclo di sviluppo 
 
Il ciclo di sviluppo utilizzato è quello Waterfall. 
 
5.2 
Piano delle attività 
 
L’avvio delle attività è legato all’approvazione del presente documento.  
La prima FASE si occuperà della realizzazione dei requisiti relativi al sottosistema SIUS (REQ-SIE-009-1 / 
REQ-SIE-009-11). 
 
Fase 
Descrizione  attività 
Data Inizio Attività 
Data Consegna Prevista 
FASE 1 
Realizzazione di quanto 
previsto nel presente 
documento in relazione al 
d.lgs. 123/2018 per SIUS  
Data di approvazione del presente 
documento 
Fare riferimento al GANTT 
FASE 2 
Realizzazione delle 
funzionalità di revoca e 
sostituzione delle misure 
alternative secondo 
quanto introdotto dal 
d.lgs. 123/2018 per SIUS e 
SIEP 
Successiva al termine dalla FASE 1  
 
n.a 
FASE 3 
Realizzazione interventi 
per d.lgs. 121/2018. 
Per quest’ultima fase ci si 
riserva di suddividere 
ulteriormente l’intervento 
in più sotto fasi.  
Successiva al termine dalla FASE 2  
 
n.a 
 
5.3 
Gantt 
Di seguito si riporta il gantt delle attività.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 67/68 
 
 
 
5.4 
Vincoli 
N.A. 
 
5.5 
Luogo di lavoro 
Le attività saranno espletate presso le sedi del RTI o presso la sede della DGSIA.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-SI-1.3-
20230605_Specifiche_Intervento_MEV_2019_009_SIUS_FASE-
1_D.lgs.123-2018 
      Ver. 1.3 del 05/06/2023 
Pag. 68/68 
 
 
6 Dimensionamento 
6.1 
Stima dell'effort previsto 
 
Il conteggio è relativo solo ai requisiti relativi al sottosistema SIUS (REQ-SIE-009-1 / REQ-SIE-009-11). 
La stima prevista per l’obiettivo in esame è di 75.556,00 € 
 
6.2 
Dettaglio costi 
 
Si riportano di seguito il dettaglio dei costi: 
 
 
 
N° 
€ 
Totale 
ADD 
256 
162 
41.472,00 €       
CHG 
374 
81 
30.294,00 €       
DEL 
0 
16,2  
                   -   €  
Totale 
 
 
71.766,00 €       
 
 
A questa stima si aggiungono 10 gg/u di attività di coordinamento architetturale, per un totale di 75.556,00 
€