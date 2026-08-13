---
uniqueName: siut-sic-pr-1-0-20210924-pianodirilasciosippiv-9-8
displayName: "SIUT SIC PR 1 0 20210924 Piano di rilascio SIPPI v 9 8 1 0"
category: "GENERAL"
tags: []
---

# SIUT-SIC-PR-1.0-20210924-Piano_di_rilascio_SIPPI_v.9.8.1.0

> **File originale:** `RILASCIO_9.8.1.0_SIPPI/ORIGINALI/SIUT-SIC-PR-1.0-20210924-Piano_di_rilascio_SIPPI_v.9.8.1.0.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |




Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Engineering | RTI |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 24/09/2021 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 24/09/2021 | Prima Emissione |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Francesco Rosati | RTI |  | Responsabile Manutenzione Correttiva
Referente Qualità e Sicurezza |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario e Referente Tecnico |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Referente PMO e Qualità |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |
| Luigi Buglione | RTI |  | Referente Metrico |


INDICE DEI CONTENUTI
1	Introduzione	5
1.1	Scopo del documento	5
1.2	Riferimenti	5
1.3	Glossario	5
1.3.1	Definizioni	5
1.3.2	Acronimi e abbreviazioni	5
2	Generalità	6
3	Identificazione degli elementi rilasciati	7
4	Riferimenti degli oggetti del rilascio	8
4.1	Riferimenti Anomalia (MAC)	8
4.2	Riferimenti Change Request (ADE/MEV)	8
4.2.1	Documenti a corredo della sessione di verifica conformità	9
5	Dettaglio degli elementi oggetto del rilascio	10
6	Installazione	11
6.1	Prerequisiti	11
6.2	Attività di preinstallazione	11
6.3	Attività di installazione	11
6.3.1	Installazione DB	11
6.3.1.1	Esecuzione Script	11
6.3.2	Installazione applicazione	11
6.3.2.1	Deploy Applicazione	11


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio del sistema SIC.
Gli interventi in oggetto sono rilasciati nell’ambito della release 9.9.0.0 di SIPPI.
Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio.
## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
|  |  |  |

## Glossario
## Definizioni
| Definizione | Descrizione |
| --- | --- |
|  |  |

## Acronimi e abbreviazioni
| Sigla | Descrizione |
| --- | --- |
| DB | Data Base |
| MAC | Manutenzione Correttiva |
| MEV | Manutenzione Evolutiva |
| PM | Procura della Repubblica presso il Tribunale |
| RTI | Raggruppamento Temporaneo di Impresa |
| ADE | Manutenzione Adeguativa |


# Generalità
Il presente documento descrive il piano di rilascio di SIPPI 9.9.0.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.

Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.

# Identificazione degli elementi rilasciati
| Supporto | Oggetti: | Ver. | Del |
| --- | --- | --- | --- |
| Portale fornitura | SIUT > 06 - Rilasci Software > SIC > Rilascio NSC – SIPPI 9.9.0.0 2021-09-24 | 9.9.0.0 | 24/09/2021 |
| Note-osservazioni |  |  |  |


# Riferimenti degli oggetti del rilascio
## Riferimenti Anomalia (MAC)
| Rif. Ticket OTRS | Sede
Ufficio | Descrizione segnalazione | Descrizione
intervento | Descrizione Tecnica | Manuali corretti |
| --- | --- | --- | --- | --- | --- |
| 20210831011 | Procura della Repubblica presso il Tribunale di Trani | L’utente ha segnalato l’impossibilità di inviare una sentenza con una impugnazione di primo grado di inammissibilità in quanto il codice univoco della suddetta impugnazione non è mappato nella tabella DC_TAB7a_RIFERIMENTI proprietaria di NSC. | Per la risoluzione della problematica si è intervenuti con il rilascio di uno script per il database. | E’ stato rilasciato il file “20210831011.sql” che consente di colmare la mancanza nel Database del collegamento tra la banca dati di NSC dove si è mappata l'impugnazione 022 - DICHIARA INAMMISSIBILE L'APPELLO CON ORDINANZA EMESSA
col nuovo codice univoco (17) che viene inviato da SIEP. |  |
| 20210820011 | Tribunale di Venezia | L’utente ha segnalato l’impossibilità di registrare nel sistema del casellario un soggetto straniero con codice fisdcale | Per la risoluzione della problematica è stato modificato il controllo sul codice di nascita di un soggetto (CODILUOGONASCITA) con codice fiscale valorizzato, che adesso viene effettuato solamente se il soggetto sia nato in ITALIA. | Sono state modificate le classi:
it.mig.sippi.validator.Validator.java;
it.mig.sippi.validator.ValidatorEsecuzione.java;
it.mig.sippi.validator.ValidatorCertificato.java;
it.mig.sippi.business.dao.oracle.type.TypeBuilder.java;
del progetto SIPPI (SippiWeb + SippiEJB). |  |


## Riferimenti Change Request (ADE/MEV)
| Prot. Richiesta o
Rif. Ticket OTRS | Scheda Intervento | Specifica Intervento | Descrizione Breve |
| --- | --- | --- | --- |
|  |  | - |  |


## Documenti a corredo della sessione di verifica conformità
| Tipo Documento | Nome Documento | Directory Portale |
| --- | --- | --- |
| a. Architettura HW e SW | N.A. | N.A. |
| b. Configurazione HW e SW | N.A. | N.A. |
| c. Specifiche Dati (Schema Concettuale, Schema Logico e Schema Fisico) | N.A. | N.A. |
| d. Documento di specifica funzionale del sistema | N.A. | N.A. |
| e. Manuale di installazione del sistema | N.A. | N.A. |
| f. Manuale di Configurazione del sistema | N.A. | N.A. |
| g. Manuale utente del sistema | N.A. | N.A. |
| h. Manuale dell'amministratore del sistema | N.A. | N.A. |
| i. Documento per la definizione dell'ambiente di sviluppo | N.A. | N.A. |


# Dettaglio degli elementi oggetto del rilascio
| Nome File | Path | Motivazione-riferimento |
| --- | --- | --- |
| SIPPI.ear | Applicazione | Implementazione SW java |
| script.zip | Database | Script per aggiornamento base dati:
insert_95233.sql
insert_94545_95449.sql |
| documenti.zip | Documentazione | SIUT-SIC-PR-1.0-20210924-Piano_di_rilascio_SIPPI_v.9.9.0.0.docx
SIUT-SIC-PT-1.0-20210924-Piano_dei_Test_SIPPI_v.9.9.0.0.docx
SIUT-SIC-CT-1.0-20210924-Allegato-al-piano-test_SIPPI_v.9.9.0.0.xlsx |
| sorgenti_nsc.zip | Sorgenti | Sorgenti Software |


# Installazione
## Prerequisiti
Per l’installazione del software SIPPI oggetto di rilascio è necessario aver installato la precedente release v.9.8.0.0.
## Attività di preinstallazione
N.A.
## Attività di installazione
## Installazione DB
## Esecuzione Script
Per eseguire l’aggiornamento degli oggetti del DB interessati al rilascio lanciare i seguenti script:
insert_95233.sql
insert_94545_95449.sql
## Installazione applicazione
## Deploy Applicazione
Prima di compiere questo passaggio è necessario aver eseguito quanto previsto nei paragrafi precedenti, a partire dal 6.1.

Per effettuare il deploy dell’applicazione eseguire i seguenti passi:
Applicazione SIPPI

Collegarsi al server Jenkins presso il Casellario Giudiziale (http://10.5.207.114:8081/) come utente Administrator;
scegliere il tabulatore relativo all’applicativo “SIPPI”;
cliccare sul link “SIPPI_DEPLOY”;
cliccare sul link compila con parametri;
nel menu a tendina  “CASELLARIO_ENV” selezionare la voce “esercizio”;
nel campo “BRANCH_SIPPI”/“BRANCH_NSC”/”BRANCH_ENVPROPERTIES”/”BRANCH_COMMON”/”BRANCH_SICSBRS_CLIENT” indicare il branch “pre_golive”, lasciando gli altri campi con i valori di default;
premere il tasto “Compila”.