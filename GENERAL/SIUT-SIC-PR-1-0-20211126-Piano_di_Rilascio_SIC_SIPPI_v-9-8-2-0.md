---
uniqueName: siut-sic-pr-1-0-20211126-pianodirilasciosicsippiv-
displayName: "SIUT SIC PR 1 0 20211126 Piano di Rilascio SIC SIPPI v 9 8 2 0"
category: "GENERAL"
tags: []
---

# SIUT-SIC-PR-1.0-20211126-Piano_di_Rilascio_SIC_SIPPI_v.9.8.2.0

> **File originale:** `RILASCIO_9.8.2.0_SIPPI/SIUT-SIC-PR-1.0-20211126-Piano_di_Rilascio_SIC_SIPPI_v.9.8.2.0.docx`  
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
| Elaborato da | Simone Gioggi | Analista Programmatore Senior |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 26/11/2021 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 26/11/2021 | Prima Emissione |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Francesco Rosati | RTI |  | Responsabile Manutenzione Correttiva
Referente qualità e sicurezza |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario
Referente Tecnico |
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
Gli interventi in oggetto sono rilasciati nell’ambito della release 9.8.2.0 di SIPPI.
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
Il presente documento descrive il piano di rilascio di SIPPI 9.8.2.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.

Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti interessate in ambiente di esercizio.

# Identificazione degli elementi rilasciati
| Supporto | Oggetti: | Ver. | Del |
| --- | --- | --- | --- |
| Portale fornitura | SIUT > 06 - Rilasci Software > SIC > |  |  |
| Note-osservazioni | Software SIPPI v. | Software SIPPI v. | Software SIPPI v. |


# Riferimenti degli oggetti del rilascio
## Riferimenti Anomalia (MAC)
| Rif. Ticket OTRS | Sede
Ufficio | Descrizione segnalazione | Descrizione
intervento | Descrizione Tecnica | Manuali corretti |
| --- | --- | --- | --- | --- | --- |
| 20211020016 | Tribunale di Lecce | L’ufficio segnala che l'utente non riesce a registrare il foglio complementare restituendo il sistema un "codice esito non gestito: errore interno generico". | Per la risoluzione della problematica è stata gestita la costruzione dell'oggetto dedito al colloquio con il type oracle "TY_CG_PROVVEDIMENTO". | La modifica ha avuto impatto sulla classe:
it.mig.sippi.business.dao.oracle.type.TypeBuilder.java;
del progetto SIPPI (SippiEJB). |  |




## Riferimenti Change Request (ADE/MEV)
| Prot. Richiesta o
Rif. Ticket OTRS | Scheda Intervento | Specifica Intervento | Descrizione Breve |
| --- | --- | --- | --- |
|  |  |  |  |



# Dettaglio degli elementi oggetto del rilascio
| Nome File | Path | Motivazione-riferimento |
| --- | --- | --- |
| SIPPI.ear | Applicazione | Implementazione SW java |
| documentazione.zip | Documentazione | SIUT-SIC-PR-1.0-20211126-Piano_di_Rilascio_SIC_SIPPI_v.9.8.2.0.docx
SIUT-SIC-PT-1.0-20211126-Piano_dei_Test_SIC_SIPPI_v.9.8.2.0.docx
SIUT-SIC-CT-1.0-20211126-Allegato_al_piano_test_SIC_SIPPI_v.9.8.2.0.xls |
| sorgenti.zip | Sorgenti | Sorgenti Software |


# Installazione
## Prerequisiti
Per l’installazione del software oggetto di rilascio è necessario aver installato la precedente release v..
## Attività di preinstallazione
N.A.
## Attività di installazione
## Installazione DB
## Esecuzione Script
## Installazione applicazione
## Deploy Applicazione
Prima di compiere questo passaggio è necessario aver eseguito le istruzioni, se presenti, previste nei paragrafi precedenti, a partire dal 6.1.

Per effettuare il Deploy dell’applicazione eseguire i seguenti passi:

Collegarsi al server Jenkins presso il Casellario Giudiziale (http://10.5.207.114:8081/) come utente Administrator;
scegliere il tabulatore relativo all’applicativo “SIPPI”;
cliccare sul link “SIPPI_DEPLOY”;
cliccare sul link compila con parametri;
selezionare “esercizio” nel menu a tendina “CASELLARIO_ENV”, nel campo “BRANCH_SIPPI” indicare il branch “MAC_”, lasciando gli altri campi con i valori di default;
premere il tasto “Compila”.