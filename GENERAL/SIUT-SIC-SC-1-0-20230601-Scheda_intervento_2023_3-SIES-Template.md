---
uniqueName: siut-sic-sc-1-0-20230601-schedaintervento20233-sie
displayName: "SIUT SIC SC 1 0 20230601 Scheda intervento 2023 3 SIES Template"
category: "GENERAL"
tags: []
---

# SIUT-SIC-SC-1.0-20230601-Scheda_intervento_2023_3-SIES-Template

> **File originale:** `MEV/SCHEDA_038/varie/SIUT-SIC-SC-1.0-20230601-Scheda_intervento_2023_3-SIES-Template.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
Scheda Intervento 2023_38 SIES Template 
 
 
 
 
 
 
 
 
 
Versione 1.0 del 05/06/2023

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20230605-Scheda_intervento_2023_38 
SIES 
Template 
Ver. 1.0 del 05/06/2023 
Pag. 2/8 
 
 
 
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
 
 
 
SIUT-SIC-SC-1.0-20230605-Scheda_intervento_2023_38 
SIES 
Template 
Ver. 1.0 del 05/06/2023 
Pag. 3/8 
Approvazioni 
 
 
Nominativo 
Funzione 
Elaborato da 
Vito Bufi 
Responsabile Manutenzione Sistemi attuali 
Verificato da 
Vito Bufi 
Responsabile Manutenzione Sistemi attuali 
Approvato da 
Paolo Ceccanti 
Responsabile Unico Fornitura 
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
05/06/2023 
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
Stefano Cipriani 
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
  
Responsabile Progetto Sistema Unitario e 
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
  
Referente Sicurezza 
Andrea Castorino 
RTI 
  
Referente Applicativo Gestore Fascicolo 
Documentale

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20230605-Scheda_intervento_2023_38 
SIES 
Template 
Ver. 1.0 del 05/06/2023 
Pag. 4/8 
INDICE DEI CONTENUTI 
1 
INTRODUZIONE ............................................................................................................................... 5 
1.1 
SCOPO DEL DOCUMENTO .......................................................................................................................... 5 
1.2 
RIFERIMENTI ........................................................................................................................................... 5 
1.3 
GLOSSARIO ............................................................................................................................................. 5 
1.3.1 
DEFINIZIONI ........................................................................................................................................ 5 
1.3.2 
ACRONIMI E ABBREVIAZIONI .................................................................................................................. 5 
2 
DEFINIZIONE DELL’OBIETTIVO .......................................................................................................... 6 
3 
PIANO DELLE ATTIVITÀ .................................................................................................................... 7 
3.1 
CICLO DI SVILUPPO ................................................................................................................................... 7 
3.2 
PIANO DELLE ATTIVITÀ .............................................................................................................................. 7 
3.3 
VINCOLI ................................................................................................................................................. 7 
3.4 
LUOGO DI LAVORO ................................................................................................................................... 7 
4 
DIMENSIONAMENTO ....................................................................................................................... 8 
4.1 
STIMA DELL'EFFORT PREVISTO .................................................................................................................... 8 
4.2 
DETTAGLIO COSTI .................................................................................................................................... 8

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20230605-Scheda_intervento_2023_38 
SIES 
Template 
Ver. 1.0 del 05/06/2023 
Pag. 5/8 
1 Introduzione 
1.1 
Scopo del documento 
La presente scheda di intervento costituisce lo strumento di supporto alla gestione complessiva delle attività 
previste per il presente intervento. 
La Scheda di Intervento si articola in due sezioni: 
1 
Descrizione dell’intervento, in cui vengono declinati obiettivi, ambito e approccio progettuale. 
2 
Piano delle attività, in cui viene presentato il piano delle attività con declinazione di tempi e costi 
dell’intervento. 
1.2 
Riferimenti 
Riferimento 
Nome Documento 
Descrizione Documento 
RIF1. 
 
m_dg.DOG07AR.18_05_2023.0000854.U_Richiesta_scheda_2023-
38_SIEP-Template 
Richiesta Scheda 2023_38 
1.3 
Glossario 
1.3.1 Definizioni 
Definizione 
Descrizione 
 
 
1.3.2 Acronimi e abbreviazioni 
Sigla 
Descrizione 
MEV 
Manutenzione Evolutiva 
RTI 
Raggruppamento Temporaneo di Impresa 
DB 
Data Base 
HW 
HardWare 
SW 
SoftWare

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20230605-Scheda_intervento_2023_38 
SIES 
Template 
Ver. 1.0 del 05/06/2023 
Pag. 6/8 
2 Definizione dell’Obiettivo 
Il presente documento è volto a descrivere le attività necessarie per espletare le richieste indicate nella 
scheda m_dg.DOG07AR.18_05_2023.0000854.U_Richiesta_scheda_2023-38_SIEP-Template. 
 
Saranno modificati i template così come indicato nel file “Scheda_SIEP-template”. I template modificati 
saranno:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20230605-Scheda_intervento_2023_38 
SIES 
Template 
Ver. 1.0 del 05/06/2023 
Pag. 7/8 
3 Piano delle attività 
3.1 
Ciclo di sviluppo 
Il ciclo di sviluppo è il classico (waterfall). 
 
3.2 
Piano delle attività 
Si prevede di terminare le attività il 09_06 previa approvazione della scheda di intervento. 
 
3.3 
Vincoli 
 
3.4 
Luogo di lavoro 
Le attività saranno espletate presso le sedi del RTI.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIC-SC-1.0-20230605-Scheda_intervento_2023_38 
SIES 
Template 
Ver. 1.0 del 05/06/2023 
Pag. 8/8 
4 Dimensionamento 
4.1 
Stima dell'effort previsto 
La stima dell’intervento richiesto è di 3.411 €. 
 
4.2 
Dettaglio costi 
 
L’impegno economico previsto per questa scheda è di 7 gg/u in regime di MAD. 
A questa stima si aggiungono due gg/u di attività di coordinamento architetturale, per un totale di 3.411 €