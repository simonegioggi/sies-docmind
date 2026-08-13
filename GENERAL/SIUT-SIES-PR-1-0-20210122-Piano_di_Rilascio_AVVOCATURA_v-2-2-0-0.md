---
uniqueName: siut-sies-pr-1-0-20210122-pianodirilascioavvocatur
displayName: "SIUT SIES PR 1 0 20210122 Piano di Rilascio AVVOCATURA v 2 2 0 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20210122-Piano_di_Rilascio_AVVOCATURA_v.2.2.0.0

> **File originale:** `Avvocatura-SIES/RILASCIO_2.2.0.0/SIUT-SIES-PR-1.0-20210122-Piano_di_Rilascio_AVVOCATURA_v.2.2.0.0.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |




Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo |
| --- | --- |
| Elaborato da | Simone Gioggi |
| Verificato da | Vito Bufi |
| Approvato da | Paolo Ceccanti |
| Data approvazione | 22/01/2021 |
| Livello di riservatezza | L4 |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 22/01/2021 | Prima Emissione |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Salvatore Piazza | RTI |  | Technical Manager |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Fabio Mazzocchi | RTI |  | Responsabile Manutenzione Correttiva |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Responsabile PMO |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Francesco Rosati | RTI |  | Referente qualità |
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
4.1	Riferimenti Anomalia (MAC/GAR)	8
4.2	Riferimenti Change Request (MAD/MEV)	8
4.2.1	Documenti a corredo della sessione di verifica conformità	8
5	Dettaglio degli elementi software oggetto del rilascio	9
6	Installazione	10
6.1	Prerequisiti	10
6.2	Attività di preinstallazione	10
6.3	Installazione lato DB Oracle	10
6.3.1	Esecuzione Script	10
6.3.2	Installazione applicazione	10
6.3.2.1	Deploy Applicazione	10
6.4	Attività di configurazione	10
6.5	Attività di post-installazione	10


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio del sistema AVVOCATURA.
Gli interventi in oggetto sono rilasciati nell’ambito della release 2.2.0.0 di AVVOCATURA.
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
Il presente documento descrive il piano di rilascio di AVVOCATURA 2.2.0.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.
Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.

# Identificazione degli elementi rilasciati
| Supporto | N° | Oggetti | Rev. | Del |
| --- | --- | --- | --- | --- |
| Portale Fornitura | 1 | SIUT > 06 - Rilasci Software > SIES > Rilascio AVVOCATURA 2.2.0.0 2021-01-22 > Documentazione > documentazione.zip | 2.2.0.0 | 22/01/2021 |
| Portale Fornitura | 2 | SIUT > 06 - Rilasci Software > SIES > Rilascio AVVOCATURA 2.2.0.0 2021-01-22 > Applicazione > avvocatura.war | 2.2.0.0 | 22/01/2021 |
| Portale Fornitura | 3 | SIUT > 06 - Rilasci Software > SIES > Rilascio AVVOCATURA 2.2.0.0 2021-01-22 > Sorgenti > sorgenti.zip | 2.2.0.0 | 22/01/2021 |
| Note-osservazioni |  |  |  |  |

# Riferimenti degli oggetti del rilascio
## Riferimenti Anomalia (MAC/GAR)
| Rif. Ticket OTRS | Sede
Ufficio | Descrizione segnalazione | Descrizione
intervento | Descrizione Tecnica | Manuali corretti |
| --- | --- | --- | --- | --- | --- |
| 20210120013 | DGSIA - Referenti Applicativi | L’utente segnala un errore quando entra nel dettaglio di un provvedimento e nella pagina del dettaglio, preme il tasto “indietro” | Per la risoluzione della problematica si è intervenuti con la modifica della jsp contenente l’errore aggiungendo la proprietà mancante (“ufficiDistretto”) nella chiamata al metodo “dettaglioProcedimentoSoggetto” | Sono state modificate le pagine:
“dettaglioOrdinanzaSoggetto.jsp”
dettaglioRinvioUdienzaSoggetto.jsp
dettaglioDecretoSoggetto.jsp
aggiungendo la proprietà mancante (“ufficiDistretto”) nella chiamata al metodo “dettaglioProcedimentoSoggetto” |  |
|  |  |  |  |  |  |

## Riferimenti Change Request (MAD/MEV)
| Prot. Richiesta o
Rif. Ticket OTRS | Scheda Intervento | Specifica Intervento | Descrizione Breve |
| --- | --- | --- | --- |
|  |  |  |  |

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


# Dettaglio degli elementi software oggetto del rilascio
| Nome File | Path | Motivazione-riferimento |
| --- | --- | --- |
| sorgenti.zip | Sorgenti | Sorgenti software |
| avvocatura.war | Applicazione | Eseguibile dell’applicazione AVVOCATURA |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20210122-Piano_di_Rilascio_AVVOCATURA_v.2.2.0.0.doc
SIUT-SIES-PT-1.0-20210122-Piano_dei_Test_AVVOCATURA _v.2.2.0.0.doc
SIUT-SIES-CT-1.0-20210122-Allegato_al_piano_test_AVVOCATURA_v.2.2.0.0.xls |
| Note-osservazioni |  |  |


Installazione
## Prerequisiti
Per l’installazione della release AVVOCATURA, oggetto del presente rilascio, è necessario aver installato la precedente release 2.1.0.0.
## Attività di preinstallazione
Aprire una shell linux sul server Avvocatura_SIES e loggarsi come utente “root”;
Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Installazione lato DB Oracle
## Esecuzione Script
N.A.
## Installazione applicazione
## Deploy Applicazione
Attenzione!! La variabile $JBOSS_HOME rappresenta il path di installazione dell’Enterprise Application Server 6.4.0 GA. (es: /opt/jboss-eap-6.4/)

Aprire una shell linux sul server Avvocatura_SIES e loggarsi come utente “root”.
Scaricare su una qualsiasi cartella del server Avvocatura_SIES il file “avvocatura.war” ed eseguire le seguenti operazioni:
posizionarsi sotto la cartella:
“$JBOSS_HOME/standalone/deployments”;
cancellare il vecchio eseguibile (se esistente) “avvocatura.war” e la copia deployata “avvocatura.war.deployed”;
copiare, nello stesso percorso, il nuovo eseguibile “avvocatura.war”;
posizionarsi sotto la cartella:
“$JBOSS_HOME/standalone”;
cancellare le cartelle “data”, “log” e “tmp” (se esistenti).

Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 2.b e 2.e. All’avvio, infatti, tali cartelle verranno ricreate.

Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.