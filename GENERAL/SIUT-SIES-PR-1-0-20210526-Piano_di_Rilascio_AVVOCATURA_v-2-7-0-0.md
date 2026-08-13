---
uniqueName: siut-sies-pr-1-0-20210526-pianodirilascioavvocatur
displayName: "SIUT SIES PR 1 0 20210526 Piano di Rilascio AVVOCATURA v 2 7 0 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20210526-Piano_di_Rilascio_AVVOCATURA_v.2.7.0.0

> **File originale:** `Avvocatura-SIES/RILASCIO_2.7.0.0/SIUT-SIES-PR-1.0-20210526-Piano_di_Rilascio_AVVOCATURA_v.2.7.0.0.docx`  
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
| Data approvazione | 26/05/2021 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 26/05/2021 | Prima Emissione |  |


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
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario
Referente Tecnico |
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
4.1	Riferimenti Anomalia (MAC/GAR)	8
4.2	Riferimenti Change Request (MAD/MEV)	8
4.2.1	Documenti a corredo della sessione di verifica conformità	8
5	Dettaglio degli elementi software oggetto del rilascio	10
6	Installazione	11
6.1	Prerequisiti	11
6.2	Attività di preinstallazione	11
6.3	Installazione lato DB Oracle	11
6.3.1	Esecuzione Script	11
6.3.2	Installazione applicazione	11
6.3.2.1	Deploy Applicazione	11
6.4	Attività di configurazione	11
6.5	Attività di post-installazione	12


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio del sistema AVVOCATURA.
Gli interventi in oggetto sono rilasciati nell’ambito della release 2.7.0.0 di AVVOCATURA.
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
Il presente documento descrive il piano di rilascio di AVVOCATURA 2.7.0.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.
Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.

# Identificazione degli elementi rilasciati
| Supporto | N° | Oggetti | Rev. | Del |
| --- | --- | --- | --- | --- |
| Portale Fornitura | 1 | SIUT > 06 - Rilasci Software > SIES > Rilascio AVVOCATURA 2.7.0.0 2021-05-26 > Documentazione > documentazione.zip | 2.7.0.0 | 26/05/2021 |
| Portale Fornitura | 2 | SIUT > 06 - Rilasci Software > SIES > Rilascio AVVOCATURA 2.7.0.0 2021-05-26 > Applicazione > avvocatura.war | 2.7.0.0 | 26/05/2021 |
| Portale Fornitura | 3 | SIUT > 06 - Rilasci Software > SIES > Rilascio AVVOCATURA 2.7.0.0 2021-05-26 > Sorgenti > sorgenti.zip | 2.7.0.0 | 26/05/2021 |
| Note-osservazioni |  |  |  |  |

# Riferimenti degli oggetti del rilascio
## Riferimenti Anomalia (MAC/GAR)
| Rif. Ticket OTRS | Sede
Ufficio | Descrizione segnalazione | Descrizione
intervento | Descrizione Tecnica | Manuali corretti |
| --- | --- | --- | --- | --- | --- |
| 20210525019 | DGSIA - Referente Applicativo | L’utente segnala che dopo le prove eseguite dal collega della Sorveglianza, continuano ad esserci imprecisioni sulla visibilità della data udienza su SIUS Avvocati in presenza, sul SIES distrettuale, di un decreto di fissazione udienza NON validato. | Per la risoluzione della problematica si è intervenuti con la modifica della classe in cui viene popolato l’elenco dei procedimenti del soggetto impostando nella colonna “Data Udienza” il valore solamente se il provvedimento di fissazione udienza è stato validato. | E’ stata modificata la classe:
“ProcedimentoPerSoggettoXmlUtil.java”
modificando le proprietà impostate per popolare la colonna “Data Udienza” che viene valorizzata solamente in caso di decreto di fissazione validato. |  |
| 202105250111 | DGSIA - Referente Applicativo | L’utente segnala che la prefissazione udienza, inserita sul SIUS distrettuale, presenta problemi di visibilità sul SIUS Avvocati. | Per la risoluzione della problematica si è intervenuti con la modifica della Store Procedure in cui vengono estratti i dati da inviare al sistema chiamante. | E’ stato modificato il package:
•AVVOCATURA_SIUS
In esso sono state modificate le procedure CERCA_UDIENZA e CERCA_MOVIMENTI_UDIENZA, che recuperano i dati per un procedimento in cui la data udienza ed il movimento di prefissazione udienza devono apparire solo quando il decreto viene validato. |  |

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
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20210526-Piano_di_Rilascio_AVVOCATURA_v.2.7.0.0.docx
SIUT-SIES-PT-1.0-20210526-Piano_dei_Test_AVVOCATURA _v.2.7.0.0.docx
SIUT-SIES-CT-1.0-20210526-Allegato_al_piano_test_AVVOCATURA_v.2.7.0.0.xls |
| Note-osservazioni |  |  |


Installazione
## Prerequisiti
Attenzione! La risoluzione dei ticket 20210525019 e 202105250111 che riguardano il dialogo tra i sistemi “AVVOCATURA SIUS” e “SIES”, comporta l’installazione contemporanea dei due applicativi:
AVVOCATURA SIUS (avvocatura.war, presente nell’apposito percorso “/SIUT/06 - Rilasci Software/SIES/Rilascio AVVOCATURA 2.7.0.0 2021-05-26”), versione 2.7.0.0
SIES (aggiorna_db.zip, presente nell’apposito percorso “/SIUT/06 - Rilasci Software/SIES/Rilascio SIES 12.4.10.0 2021-05-21”), versione 12.4.10.0
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