---
uniqueName: a05bcbfd00-2024-051-020241031-pianodirilasciosiusr
displayName: "A05BCBFD00 2024 05 1 0 20241031 Piano di Rilascio SIUS Riforma Cartabia"
category: "GENERAL"
tags: []
---

# A05BCBFD00-2024-05_1.0_20241031-Piano_di_Rilascio_SIUS_Riforma_Cartabia

> **File originale:** `MEV/SCHEDA_035/ORIGINALI X NUOVO CONTRATTO/A05BCBFD00-2024-05_1.0_20241031-Piano_di_Rilascio_SIUS_Riforma_Cartabia.docx`  
> **Tipo:** DOCX

---

|  |
| --- |
|  |




Approvazioni

|  | Nominativo |
| --- | --- |
| Elaborato da | Simone Gioggi |
| Verificato da | Vito Bufi |
| Approvato da | Paolo Ceccanti |
| Data approvazione | 31/10/2024 |
| Livello di riservatezza | L4 |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 31/10/2024 | Prima Emissione |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Aurora Garofalo | Amministrazione |  | Responsabile Unico Procedimento |
| Dott. Oris Orlando | Amministrazione |  | Direttore Esecutivo Contratto |
| Michele D’Alessandro | RTI - Accenture |  | Responsabile Unico Fornitura |


INDICE DEI CONTENUTI
1.	Introduzione	4
1.1	Scopo del documento	4
1.2	Riferimenti	4
1.3	Glossario	4
1.3.1	Definizioni	4
1.3.2	Acronimi e abbreviazioni	4
2.	Generalità	5
3.	Identificazione degli elementi rilasciati	6
4.	Riferimenti degli oggetti del rilascio	7
4.1	Riferimenti Anomalia (MAC/GAR)	7
4.2	Riferimenti ChangeRequest (ADE/MEV)	7
5.	Dettaglio degli elementi oggetto del rilascio	8
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
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.6.4.0-MEV_2024_05 di SIES.
Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio.
## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF1. | Specifiche_Intervento_MEV_2024_05_SIUS_Riforma_Cartabia | Specifiche Intervento |

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
Il presente documento descrive il piano di rilascio del software relativo alla MEV 2024-05 - SIUS Riforma Cartabia di SIES, contenente l’integrazione della suddetta MEV con la versione SIES 12.6.4.0.

Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.
# Identificazione degli elementi rilasciati
| Supporto | Oggetti: | Ver. | Del |
| --- | --- | --- | --- |
| Portale fornitura | SIUT > 07 - MEV > Scheda 2023_ 035 - SIUS Riforma Cartabia > 05_Verifica di Conformita' | 1.0 | 31/10/2024 |
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
| - | Specifiche_Intervento_MEV_2024_05_SIUS_Riforma_Cartabia | - | Adeguamento al d.lgs. 10 ottobre 2022, n. 150 |

# Dettaglio degli elementi oggetto del rilascio
| Nome File | Path | Motivazione-riferimento |
| --- | --- | --- |
| aggiorna_db.zip | Database | Script per aggiornamento base dati: 
Aggiornamento, inserimento e alterazione in varie tabelle
Aggiornamento versione SIES in tabella “VERSIONE” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| documentazione.zip | Documentazione | A05BCBFD00-2024-05_1.0-20241031-Piano_di_Rilascio_SIUS_Riforma_Cartabia.pdf
Allegato_al_piano_Test_2024_05_SIUS_Riforma_Cartabia.xlsx
Piano_dei_Test_2024_05_SIUS_Riforma_Cartabia.pdf
Manuale_Utente_2024_05_SIUS_Riforma_Cartabia.pdf
Modello_dei_Dati_2024_05_SIUS_Riforma_Cartabia.pdf |
| template.zip | Template | sius\de\SIUS_DE_AUTORIZZAFUORISEDEPS.rtf
sius\de\SIUS_DE_AUTORIZZAGENERICOPS.rtf
sius\de\SIUS_DE_AUTORIZZAUSOPATENTEPS.rtf
sius\de\SIUS_DE_CONCLICPS.rtf
sius\de\SIUS_DE_DIFFIDARISPPRESCRPS.rtf
sius\de\SIUS_DE_INAMMLICPS.rtf
sius\de\SIUS_DE_MODGENERICO.rtf
sius\de\SIUS_DE_MODGENERICOPS.rtf
sius\de\SIUS_DE_MODLUOESECSL.rtf
sius\de\SIUS_DE_MODLUOESEDDPS.rtf
sius\de\SIUS_DE_MODPRESCRPERMPS.rtf
sius\de\SIUS_DE_MODPRESCRPS.rtf
sius\de\SIUS_DE_PROGRTRATT.rtf
sius\de\SIUS_DE_PROSPROVPS.rtf
sius\de\SIUS_DE_REVOCALICPS.rtf
sius\de\SIUS_DE_RIGETTOLICPS.rtf
sius\de\SIUS_DE_RINVIOESECPENAPS.rtf
sius\de\SIUS_DE_RINVIOESECPENAPSDC.rtf
sius\de\SIUS_DE_SCOMPUTOLICPS.rtf
sius\de\SIUS_DE_SOSPPROVPS.rtf
sius\de\SIUS_DE_SOSPPSLAVPU.rtf
sius\or\SIUS_OR_ACCRECLREVPS.rtf
sius\or\SIUS_OR_APPLPENASOST.rtf
sius\or\SIUS_OR_GENERICAPENASOST.rtf
sius\or\SIUS_OR_MODGENERICOAPPS.rtf
sius\or\SIUS_OR_MODGENERICOPS.rtf
sius\or\SIUS_OR_PROGRTRATT.rtf
sius\or\SIUS_OR_PROSPROVPS.rtf
sius\or\SIUS_OR_RATEIZZAPENASOST.rtf
sius\or\SIUS_OR_REVCONVPS.rtf
sius\or\SIUS_OR_REVOCAPENASOST.rtf
sius\or\SIUS_OR_RIGETTODIFPENAPS.rtf
sius\or\SIUS_OR_RIGRECLREVPS.rtf
sius\or\SIUS_OR_RINVIOESECPSTDS.rtf
sius\or\SIUS_OR_SOSPENSIONEPA.rtf
sius\or\SIUS_OR_SOSPENSIONEPA-TDS.rtf
sius\or\SIUS_OR_SOSPPROVPS.rtf
sius\or\SIUS_OR_SOSPPSPENADET.rtf
sius\or\SIUS_OR_SOSPSSPENADET.rtf
sius\st\SIUS_ST_RELTRIMPERMESSI.rtf
sius\st\SIUS_ST_STAMPACOPERTINE.rtf
sius\st\SIUS_ST_STAMPAFASCICOLO.rtf |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.6.4.0.
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
Creare sul server DB una cartella MEV_2024_05 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/MEV_2024_05/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella MEV_2024_05 tramite il comando:
chmod 777 MEV_2024_05
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES...........: siesxx	(dove xx è la sigla del distretto di appartenenza, per esempio: rm per Roma)
Password_SIES.......: siesxx
Nella cartella appena creata (MEV_2024_05), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/MEV_2024_05/log/ in cui si può constatare l’esito dell’esecuzione.
N.B. Le segnalazioni del tipo:
ORA-00001: violata restrizione di unicità
ORA-00955: name is already used by an existing object
Cartella log già presente
ORA-04043: object does not exist
sono da considerarsi warning e non errori.
Accedere ad oracle (con qualsiasi strumento tipo toad, developer…) come utente siesxx e compilare tutte le procedure e i package che non risultano compilate.
ATTENZIONE: la procedura SUPER_SOGGETTO_PREGR ed il package CARICA_RES potrebbero restare non compilate: non è da considerarsi errore.
## Installazione applicazione
## Deploy Applicazione
Aprire una shell linux sul server SIES e loggarsi come utente “root”;
Scaricare il file “sies.war” sul server SIES ed eseguire le seguenti operazioni:
posizionarsi sotto la cartella:
“/opt/jboss-eap-6.4/standalone/deployments”;
cancellare il vecchio eseguibile (se esistente) “sies.war” e la copia deployata “sies.war.deployed”;
copiare, nello stesso percorso, il nuovo eseguibile “sies.war”;
posizionarsi sotto la cartella:
“/opt/jboss-eap-6.4/standalone”;
cancellare le cartelle “data”, “log” e “tmp” (se esistenti);
Copiare i files contenuti nella cartella template\sius\de
nella cartella “/var/SIES/template/sius/de” sovrascrivendo quelli precedenti;
Copiare i files contenuti nella cartella template\sius\or
nella cartella “/var/SIES/template/sius/or” sovrascrivendo quelli precedenti;
Copiare i files contenuti nella cartella template\sius\st
nella cartella “/var/SIES/template/sius/st” sovrascrivendo quelli precedenti;
Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 2.b e 2.e. All’avvio, infatti, tali cartelle verranno ricreate.
Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.