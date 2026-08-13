---
uniqueName: siut-sic-pr-1-0-20210924-pianodirilasciosicsippiv-
displayName: "SIUT SIC PR 1 0 20210924 Piano di Rilascio SIC SIPPI v 9 8 1 0"
category: "GENERAL"
tags: []
---

# SIUT-SIC-PR-1.0-20210924-Piano_di_Rilascio_SIC_SIPPI_v.9.8.1.0

> **File originale:** `RILASCIO_9.8.1.0_SIPPI/SIUT-SIC-PR-1.0-20210924-Piano_di_Rilascio_SIC_SIPPI_v.9.8.1.0.docx`  
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
| Elaborato da | Gianluca Dell’Olio | Analista Funzionale |
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
| Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Francesco Rosati | RTI |  | Responsabile Manutenzione Correttiva
Referente qualità e sicurezza |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario e Referente Tecnico |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Responsabile PMO e Qualità |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |
| Luigi Buglione | RTI |  | Referente Metrico |


INDICE DEI CONTENUTI
1	Introduzione	5
1.1	Scopo del documento	5
1.1	Riferimenti	5
1.2	Riferimenti	5
1.3	Glossario	5
1.3.1	Definizioni	5
1.3.2	Acronimi e abbreviazioni	5
2	Generalità	6
3	Identificazione degli elementi rilasciati	7
4	Riferimenti degli oggetti del rilascio	8
4.1	Riferimenti Anomalia (MAC)	8
4.2	Riferimenti Change Request (ADE/MEV)	9
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
Il presente documento descrive il piano di rilascio della componente SIPPI dell’ecosistema SIC/NSC.
Gli interventi in oggetto sono rilasciati nell’ambito della release 9.8.1.0 di SIPPI.
Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio.
## Riferimenti
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
| DEC | Direttore Esecutivo Contratto |
| DGSIA | Direzione Generale per i Sistemi Informativi Automatizzati |
| FP | Function Point |
| GdL | Gruppo di Lavoro |
| HW | HardWare |
| MAC | Manutenzione Correttiva |
| MEV | Manutenzione Evolutiva |
| PA | Pubblica Amministrazione |
| PEC | Posta Elettronica Certificata |
| RTI | Raggruppamento Temporaneo di Impresa |
| RUF | Responsabile Unico Fornitore |
| RUP | Responsabile Unico Progetto |
| SW | SoftWare |


# Generalità
Il presente documento descrive il piano di rilascio di SIPPI 9.8.1.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.

Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti interessate in ambiente di esercizio.

# Identificazione degli elementi rilasciati
| Supporto | Oggetti: | Ver. | Del |
| --- | --- | --- | --- |
| Portale fornitura | SIUT > 06 - Rilasci Software > SIC >Rilascio SIC – SIPPI 9.8.1.0 2021-09-24 | 9.8.1.0 | 24/09/2021 |
| Note-osservazioni | Software SIPPI v.9.8.1.0 | Software SIPPI v.9.8.1.0 | Software SIPPI v.9.8.1.0 |


# Riferimenti degli oggetti del rilascio
## Riferimenti Anomalia (MAC)
| Rif. Ticket OTRS | Sede
Ufficio | Descrizione segnalazione | Descrizione
intervento | Descrizione Tecnica | Manuali corretti |
| --- | --- | --- | --- | --- | --- |
| 20210820011 | Tribunale di Venezia | Impossibilità registrazione scheda del casellario | Per la risoluzione della problematica è stato modificato il controllo sul codice di nascita di un soggetto (CODILUOGONASCITA) con codice fiscale valorizzato, che adesso viene effettuato solamente se il soggetto sia nato in ITALIA. | La modifica ha avuto impatto sulle classi:
it.mig.sippi.validator.Validator.java;
it.mig.sippi.validator.ValidatorEsecuzione.java;
it.mig.sippi.validator.ValidatorCertificato.java;
it.mig.sippi.business.dao.oracle.type.TypeBuilder.java;
del progetto SIPPI (SippiWeb + SippiEJB) |  |
| 20210831011 | Procura della Repubblica presso il Tribunale di Trani | L’utente ha segnalato l’impossibilità di inviare una sentenza con una impugnazione di primo grado di inammissibilità in quanto il codice univoco della suddetta impugnazione non è mappato nella tabella DC_TAB7a_RIFERIMENTI proprietaria di NSC. | Per la risoluzione della problematica si è intervenuti con il rilascio di uno script per il database. | E’ stato rilasciato il file “20210831011.sql” che consente di colmare la mancanza nel Database del collegamento tra la banca dati di NSC dove si è mappata l'impugnazione 022 - DICHIARA INAMMISSIBILE L'APPELLO CON ORDINANZA EMESSA
col nuovo codice univoco (17) che viene inviato da SIEP. |  |




## Riferimenti Change Request (ADE/MEV)
| Prot. Richiesta o
Rif. Ticket OTRS | Scheda Intervento | Specifica Intervento | Descrizione Breve |
| --- | --- | --- | --- |
|  |  |  |  |



# Dettaglio degli elementi oggetto del rilascio
| Nome File | Path | Motivazione-riferimento |
| --- | --- | --- |
| SIPPI.ear | Applicazione | Implementazione SW java |
| aggiorna_db.zip | Database | Script per aggiornamento base dati:
20210831011.sql |
| documentazione.zip | Documentazione | SIUT-SIC-PR-1.0-20210924-Piano_di_Rilascio_SIC_SIPPI_v.9.8.1.0.docx
SIUT-SIC-PT-1.0-20210924-Piano_dei_Test_SIC_SIPPI_v.9.8.1.0.docx
SIUT-SIC-CT-1.0-20210924-Allegato_al_piano_test_SIC_SIPPI_v.9.8.1.0.xls |
| sorgenti.zip | Sorgenti | Sorgenti Software |


# Installazione
## Prerequisiti
Per l’installazione del software oggetto di rilascio è necessario aver installato la precedente release v.9.8.0.0.
## Attività di preinstallazione
N.A.
## Attività di installazione
## Installazione DB
## Esecuzione Script
Per eseguire l’aggiornamento degli oggetti del DB interessati al rilascio lanciare i seguenti script:
20210831011.sql
presente nella cartella “V_9_8_1_0” all’interno dell’archivio “aggiorna_db” .
## Installazione applicazione
## Deploy Applicazione
Prima di compiere questo passaggio è necessario aver eseguito le istruzioni, se presenti, previste nei paragrafi precedenti, a partire dal 6.1.

Per effettuare il Deploy dell’applicazione eseguire i seguenti passi:

Collegarsi al server Jenkins presso il Casellario Giudiziale (http://10.5.207.114:8081/) come utente Administrator;
scegliere il tabulatore relativo all’applicativo “SIPPI”;
cliccare sul link “SIPPI_DEPLOY”;
cliccare sul link compila con parametri;
selezionare “esercizio” nel menu a tendina  “CASELLARIO_ENV”, nel campo “BRANCH_SIPPI” indicare il branch “MAC_9_8_1_0”, lasciando gli altri campi con i valori di default;
premere il tasto “Compila”.