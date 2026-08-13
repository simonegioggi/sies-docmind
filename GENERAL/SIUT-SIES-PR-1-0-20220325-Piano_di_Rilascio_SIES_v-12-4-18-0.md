---
uniqueName: siut-sies-pr-1-0-20220325-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20220325 Piano di Rilascio SIES v 12 4 18 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20220325-Piano_di_Rilascio_SIES_v.12.4.18.0

> **File originale:** `RILASCIO_12.4.18.0/SIUT-SIES-PR-1.0-20220325-Piano_di_Rilascio_SIES_v.12.4.18.0.docx`  
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
| Data approvazione | 25/03/2022 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 25/03/2022 | Prima Emissione |  |


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
4.2	Riferimenti ChangeRequest (ADE/MEV)	9
4.2.1	Documenti a corredo della sessione di verifica conformità	9
5	Dettaglio degli elementi oggetto del rilascio	11
6	Installazione	12
6.1	Prerequisiti	12
6.2	Attività di preinstallazione	12
6.3	Attività di installazione	12
6.3.1	Installazione lato DB	12
6.3.1.1	Esecuzione script	12
6.3.2	Installazione applicazione	13
6.3.2.1	Deploy Applicazione	13
6.4	Attività di configurazione	13
6.5	Attività di post-installazione	13


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio del sistema SIES.
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.18.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.4.18.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.
Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.
# Identificazione degli elementi rilasciati
| Supporto | Oggetti: | Ver. | Del |
| --- | --- | --- | --- |
| Portale fornitura | SIUT > 06 - Rilasci Software > SIES > |  |  |
| Note-osservazioni |  |  |  |


# Riferimenti degli oggetti del rilascio
## Riferimenti Anomalia (MAC/GAR)
| Rif. Ticket OTRS | Sede
Ufficio | Descrizione segnalazione | Descrizione
intervento | Descrizione Tecnica | Manuali corretti |
| --- | --- | --- | --- | --- | --- |
| 20220222015 | Centro di Competenza Sistemi Area Penale | L’ufficio segnala che il sistema non conteggia il visto del Pm per archiviazione. | Per la risoluzione della problematica è stato inserito un nuovo record nella tabella ISP_MOTIVO_ATTIVITA con COD_MOTIVO='0488'; modificato anche il package ISPETTORATO inserendo la gestione del COD_MOTIVO='0488' fra quelli previsti nella tipologia '17' (Visti al PM). | Il problema era legato al fatto che la Stored Procedure non conteggiava la categoria “Visto del PM per archiviazione” poiché il rispettivo codice motivo 0488 non era stato previsto.
Procedura modificata:
ISPETTORATO
Tabella modificata:
ISP_MOTIVO_ATTIVITA |  |
| 20220224014 | Centro di Competenza Sistemi Area Penale | L’ufficio segnala che Il sistema non trasferisce il dato nell'istruttoria cumulo. | Per la risoluzione della problematica è stata aggiornata la tabella CG_REF_CODES correggendo il valore relativo al codice U100 da Stato Esecuzione Ristretto (SER) a Stato Esecuzione Esteso (SEE). | Il problema della mancata impostazione ad 'S' delle colonne FLAG_VIDEO_SIEP e FLAG_STAMPA_SIEP sull'evento è stato individuato nell'errata impostazione a 'SEE'  invece che a 'SER' della colonna RV_ALT2_VALUE nel record della tabella CG_REF_CODES con RV_DOMAIN = 'OGGETTO_PROCEDIMENTO' e RV_LOW_VALUE = 'U100'.
Tabella modificata:
CG_REF_CODES |  |
| 20220224017 | Procura della Repubblica presso il Tribunale per i Minorenni di Catania | L’ufficio segnala che per la statistica “Elenco delle esecuzioni iniziate dopo 90 giorni dall'iscrizione del fascicolo” si riscontrano delle anomalie: nella statistica non viene rilevata la prima attività del PM. | Per la risoluzione della problematica sono stati aggiunti alcuni codici che servivano ad estrarre il dato di interesse; a tal fine sono stati inseriti nella procedura  ISPETTORATO.TEMPI_EMISSIONE i codici degli Ordini di esecuzione introdotti per i minori e per gli arresti domiciliari (5501-5513; 5523-5529; 5533-5537). | Il problema risiedeva nel fatto che mancavano alcuni codici che servivano ad estrarre il dato di interesse.
Procedura modificata:
ISPETTORATO |  |
| 202202280122 | Centro di Competenza Sistemi Area Penale | L’ufficio segnala che il sistema non classifica il  procedimento in differimento pena  nel riepilogo ispettivo. | Per la risoluzione della problematica è stata aggiornata la procedura ISPETTORATO.STAT_PROVVEDIMENTI, modificando la condizione di esclusione della comunicazione provvedimenti di cumulo poiché erroneamente escludeva tutte le comunicazioni. | Il problema era legato all'errata esclusione degli eventi di comunicazione.
Procedura modificata:
ISPETTORATO |  |
| 20220311014 | Procura della Repubblica presso il Tribunale di Verbania | L’ufficio segnala che quando iscrive le pene pecuniari per disposizione dell'ispettore, i procedimenti iscritti in classe 20000 compaiono però nel riepilogo ispettivo come pendenti in fase istruttoria. | Per la risoluzione della problematica è stata aggiornata la procedura ISPETTORATO.STAT_PROVVEDIMENTI, inserendo lo scarto dei procedimenti di classe II. | Il problema era legato alla mancata esclusione dei procedimenti di classe II ovvero quelli aventi chiave progressivo compresa tra 20000 e 29999.
Procedura modificata:
ISPETTORATO |  |
| 20220311015 | Procura della Repubblica presso il Tribunale di Torino | L’ufficio segnala che nel provvedimento di archiviazione manca l'indicazione della data di inizio e fine dell'espiazione pena che occorre al casellario per definire la pratica. | Per la risoluzione della problematica è stato modificato il template segnalato aggiungendo la gestione della posizione giuridica "detenzione domiciliare provvisoria" codice 29 finora non gestita. | Il problema era legato alla mancata gestione della posizione giuridica "Detenzione Domiciliare Provvisoria" (codice 29) al fine di estrarre la data di inizio e fina espiazione pena.
Template modificato:
SIEP_ARC_FOGLIO_COMP_ESP.rtf |  |
| Note-osservazioni |  |  |  |  |  |

## Riferimenti ChangeRequest (ADE/MEV)
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

# Dettaglio degli elementi oggetto del rilascio
| Nome File | Path | Motivazione-riferimento |
| --- | --- | --- |
| aggiorna_db.zip | Database | Script: 
Aggiornamento versione SIES in tabella “VERSIONE”
Inserimento in tabella “ISP_MOTIVO_ATTIVITA”
Aggiornamento Package “ISPETTORATO”
Aggiornamento in tabella “CG_REF_CODES” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| template.zip | Template | Template aggiornati:
SIEP_ARC_FOGLIO_COMP_ESP.rtf |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20220325-Piano_di_Rilascio_SIES_v.12.4.18.0.docx
SIUT-SIES-PT-1.0-20220325-Piano_dei_Test_SIES_v.12.4.18.0.docx
SIUT-SIES-CT-1.0-20220325-Allegato_al_piano_test_SIES_v.12.4.18.0.xls |
| Note-osservazioni | L’aggiornamento del package “ISPETTORATO” ha coinvolto quattro ticket (20220222015, 20220224017, 202202280122, 20220311014) | L’aggiornamento del package “ISPETTORATO” ha coinvolto quattro ticket (20220222015, 20220224017, 202202280122, 20220311014) |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.17.0.
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
Creare sul server DB una cartella V_12_4_18_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_4_18_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_18_0 tramite il comando:
chmod 777 V_12_4_18_0
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx
Nella cartella appena creata (V_12_4_18_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_4_18_0/log/ in cui si può constatare l’esito dell’esecuzione.
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
Scaricare i files “sies.war” sul server SIES ed eseguire le seguenti operazioni:
posizionarsi sotto la cartella:
“/opt/jboss-eap-6.4/standalone/deployments”;
cancellare il vecchio eseguibile (se esistente) “sies.war” e la copia deployata “sies.war.deployed”;
copiare, nello stesso percorso, il nuovo eseguibile “sies.war”;
posizionarsi sotto la cartella:
“/opt/jboss-eap-6.4/standalone”;
cancellare le cartelle “data”, “log” e “tmp” (se esistenti);
Copiare i files contenuti nella cartella template\siep\arc
nella cartella “/var/SIES/template/siep/arc” sovrascrivendo quelli precedenti;
Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 2.b e 2.e. All’avvio, infatti, tali cartelle verranno ricreate.
Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.