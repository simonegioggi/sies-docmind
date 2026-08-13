---
uniqueName: siut-sies-pr-1-1-20210531-pianodirilasciomev-integ
displayName: "SIUT SIES PR 1 1 20210531 Piano di Rilascio MEV Integrazione SIES ADN  PRE GOLIV"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.1-20210531-Piano_di_Rilascio_MEV-Integrazione SIES-ADN (PRE-GOLIVE)

> **File originale:** `MEV/Integrazione SIES-ADN/RILASCIO_MEV_SIES-ADN (PRE GO-LIVE)/20210531_1.1/SIUT-SIES-PR-1.1-20210531-Piano_di_Rilascio_MEV-Integrazione SIES-ADN (PRE-GOLIVE).docx`  
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
| Data approvazione | 31/05/2021 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 24/03/2021 | Prima Emissione |  |
| 1.1 | 31/05/2021 | Seconda Emissione | Cap. 5 (Dettaglio degli elementi oggetto del rilascio: cambiati i nomi dei files contenuti nella cartella “documentazione”.
Cap. 2 e cap. 6.1: cambiata la versione di SIES con cui è stata integrata la MEV in questione. |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Salvatore Piazza | RTI |  | Technical Manager |
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
1.	Introduzione	5
1.1	Scopo del documento	5
1.2	Riferimenti	5
1.3	Glossario	5
1.3.1	Definizioni	5
1.3.2	Acronimi e abbreviazioni	5
2.	Generalità	6
3.	Identificazione degli elementi rilasciati	7
4.	Riferimenti degli oggetti del rilascio	8
4.1	Riferimenti Anomalia (MAC/GAR)	8
4.2	Riferimenti ChangeRequest (ADE/MEV)	8
5.	Dettaglio degli elementi oggetto del rilascio	9
6.	Installazione	10
6.1	Prerequisiti	10
6.2	Attività di preinstallazione	10
6.3	Attività di installazione	10
6.3.1	Installazione lato DB	10
6.3.1.1	Esecuzione script	10
6.3.2	Installazione applicazione	11
6.3.2.1	Deploy Applicazione	11
6.4	Attività di configurazione	12
6.5	Attività di post-installazione	12


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio degli interventi realizzati nell’ambito del Sistema Integrato Esecuzione Sorveglianza per la realizzazione di quanto dettagliato nella scheda di intervento di riferimento.
Gli interventi in oggetto sono rilasciati nell’ambito della release MEV-Integrazione SIES-ADN (PRE-GOLIVE) di SIES.
Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio.
## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF1. | SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN.pdf | Scheda Intervento |

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
| MAC | MAnutenzione Correttiva |
| MEV | Manutenzione EVolutiva |
| PA | Pubblica Amministrazione |
| PEC | Posta Elettronica Certificata |
| RTI | Raggruppamento Temporaneo di Impresa |
| RUF | Responsabile Unico Fornitore |
| RUP | Responsabile Unico Progetto |
| SW | SoftWare |


# Generalità
Il presente documento descrive il piano di rilascio del software relativo alla MEV Integrazione SIES-ADN (PRE-GOLIVE), contenente l’integrazione della suddetta MEV con la versione SIES 12.4.10.0.

Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.
# Identificazione degli elementi rilasciati
| Supporto | Oggetti: | Ver. | Del |
| --- | --- | --- | --- |
| Portale fornitura | SIUT > 07 - MEV > 2019_002_Casellario_Sostituzione IGI > Verifica Conformità > 02_SIES > pre-golive | 1.1 | 31/05/2021 |
| Note-osservazioni |  |  |  |


# Riferimenti degli oggetti del rilascio
## Riferimenti Anomalia (MAC/GAR)
| Rif. Ticket OTRS | Sede
Ufficio | Descrizione segnalazione | Descrizione
intervento | Descrizione Tecnica | Manuali corretti |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |

## Riferimenti ChangeRequest (ADE/MEV)
| Prot. Richiesta o
Rif. Ticket OTRS | Scheda Intervento | Specifica Intervento | Descrizione Breve |
| --- | --- | --- | --- |
| - | SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-ADN.pdf | - | Integrazione del SIES con le utenze ADN |

# Dettaglio degli elementi oggetto del rilascio
| Nome File | Path | Motivazione-riferimento |
| --- | --- | --- |
| aggiorna_db.zip | Database | Script per aggiornamento base dati: 
Creazione Tabella “UTENZA_ADN”
Creazione Tabella “ASSOC_UTENTE_SIES_ADN”
Creazione Sequence “ASSOC_UTENTE_SIES_ADN_SEQ”
Creazione Sequence “UTENZA _ADN_SEQ”
Aggiornamento versione SIES in tabella “VERSIONE” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| siesEsecuzione.war | Applicazione | Eseguibile dell’applicazione SIES ESECUZIONE |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.1-20210531-Piano_di_Rilascio_MEV-Integrazione SIES-ADN (PRE-GOLIVE).docx
SIUT-SIE-PV-1.1-20210531-Piano delle verifiche_MEV-Integrazione SIES-ADN (PRE-GOLIVE).pdf
SIUT-SIE-MU-1.1-20210312-Manuale_Utente_MEV-Integrazione SIES-ADN (PRE-GOLIVE).pdf
SIGI_PNL_ML_20210521_1.7_Modello dei Dati_SIES.pdf
SIUT-SIES-PT-1.1-20210531-Piano_dei_Test_MEV-Integrazione SIES-ADN (PRE-GOLIVE).pdf
SIUT-SIES-CT-1.1-20210531-Allegato_al_piano_test_MEV-Integrazione SIES-ADN (PRE-GOLIVE).xlsx |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.10.0.

Le macchine server di ognuno dei ventinove distretti SIES devono poter raggiungere, sulla porta 636, i server LDAP individuati dai seguenti indirizzi IP:
10.6.203.3
10.6.203.4
10.3.201.164
10.3.201.165
## Attività di preinstallazione
Aprire una shell linux sul server SIES e loggarsi come utente “root”;
Eseguire il comando: “cd /etc/init.d”;
Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”;
Fermare il processo di gestione delle code tramite il comando: “./imq stop”;
## Attività di installazione
## Installazione lato DB
## Esecuzione script
(E’ consigliato che tale procedura venga eseguita da personale competente in ambiente Oracle)
Il documento elenca i passi necessari per la corretta esecuzione.

Collegarsi come utente oracle sul db server;
Impostare le variabili ORACLE_HOME e ORACLE_SID (se non già settate) eseguendo le seguenti istruzioni:
(il percorso varia in base all’installazione di oracle)
export ORACLE_HOME=/u01/app/oracle/product/12.1.0/dbhome_1
(sostituire xxxxx col nome dell’istanza oracle)
export ORACLE_SID=xxxxx
Aggiungere nella variabile PATH $ORACLE_HOME/bin
Esempio: PATH=$PATH:/u01/app/oracle/product/12.1.0/dbhome_1/bin

Prima di avviare la procedura, accertarsi che sia il listener che il database siano avviati.

Copiare il file aggiorna_db.zip in una qualsiasi cartella e scompattarlo. il sistema crea la cartella aggiorna_db;
Creare sul server DB una cartella MEV_SIES-ADN_Pre-golive sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/MEV_SIES-ADN_Pre-golive/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella MEV_SIES-ADN_Pre-golive tramite il comando:
chmod 777 MEV_SIES-ADN_Pre-golive

In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx

Nella cartella appena creata (MEV_SIES-ADN_Pre-golive), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/MEV_SIES-ADN_Pre-golive/log/ in cui si può constatare l’esito dell’esecuzione.

N.B. Le segnalazioni del tipo:
ORA-00001: violata restrizione di unicità
ORA-00955: name is already used by an existing object
Cartella log già presente
ORA-04043: object does not exist
sono da considerarsi warning e non errori.

Accedere ad oracle (con qualsiasi strumento tipo toad, developer…) come utente siesxx e compilare tutte le procedure e i package che non risultano compilate.
ATTENZIONE: la procedura SUPER_SOGGETTO_PREGR e il package CARICA_RES potrebbero restare non compilate: non è da considerarsi errore.
## Installazione applicazione
## Deploy Applicazione
Aprire una shell linux sul server SIES e loggarsi come utente “root”;
Posizionarsi sotto la cartella:
“/var/SIES/CONFIG”;
Editare il file “f3b.properties” ed aggiungere alla fine del file le seguenti quattro righe:
#MEV INTEGRAZIONE SIES ADN: costanti di configurazione autorità
ldap.domain=usr.root.jus
ldap.dn=dc=usr,dc=root,dc=jus
ldap.provider.url=ldaps://DCBALRMUTE001.usr.root.jus:636 ldaps://DCBALRMUTE002.usr.root.jus:636 ldaps://DCCEDNAUTE001.usr.root.jus:636 ldaps://DCCEDNAUTE002.usr.root.jus:636
Salvare il file modificato;
Scaricare i files “sies.war” sul server SIES ed eseguire le seguenti operazioni:
posizionarsi sotto la cartella:
“/opt/jboss-eap-6.4/standalone/deployments”;
cancellare il vecchio eseguibile (se esistente) “sies.war” e la copia deployata “sies.war.deployed”;
cancellare il vecchio eseguibile (se esistente) “siesEsecuzione.war” e la copia deployata “siesEsecuzione.war.deployed”;
copiare, nello stesso percorso, il nuovo eseguibile “sies.war”;
copiare, nello stesso percorso, il nuovo eseguibile “siesEsecuzione.war”;
posizionarsi sotto la cartella:
“/opt/jboss-eap-6.4/standalone”;
cancellare le cartelle “data”, “log” e “tmp” (se esistenti);

Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 5.b, 5.c e 5.g. All’avvio, infatti, tali cartelle verranno ricreate.

Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.