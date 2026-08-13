---
uniqueName: siut-sies-pr-1-0-20220225-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20220225 Piano di Rilascio SIES v 12 4 17 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20220225-Piano_di_Rilascio_SIES_v.12.4.17.0

> **File originale:** `RILASCIO_12.4.17.0/SIUT-SIES-PR-1.0-20220225-Piano_di_Rilascio_SIES_v.12.4.17.0.docx`  
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
| Data approvazione | 25/02/2022 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 25/02/2022 | Prima Emissione |  |


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
5	Dettaglio degli elementi oggetto del rilascio	10
6	Installazione	11
6.1	Prerequisiti	11
6.2	Attività di preinstallazione	11
6.3	Attività di installazione	11
6.3.1	Installazione lato DB	11
6.3.1.1	Esecuzione script	11
6.3.2	Installazione applicazione	12
6.3.2.1	Deploy Applicazione	12
6.4	Attività di configurazione	12
6.5	Attività di post-installazione	12


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio del sistema SIES.
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.17.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.4.17.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.
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
| 20220124016 | Centro di Competenza Sistemi Area Penale | L’ufficio segnala che il sistema non rileva, nella sezione Procedimenti in fase istruttoria - PROCEDIMENTI ISCRITTI, tutti i procedimenti iscritti e non validati. | Per la risoluzione della problematica è stato modificato il package ISPETTORATO_MS e modificato l'indice ANNO_PROG_UFF_MS (CHIAVE_ANNO, CHIAVE_PROGR, COD_UFFICIO_INSERIMENTO) della tabella ISP_PROVVEDIMENTI_MS, sostituendo la colonna COD_UFFICIO con COD_UFFICIO_INSERIMENTO. | Il problema era legato al fatto che la Stored Procedure estraeva solo procedimenti con stato differente da ISCRITTO; inoltre, i procedimenti privi di movimentazione non venivano estratti. E' stata modificata la condizione sul campo COD_STATO_FASCICOLO ed inserita la gestione di un nuovo cursore per estrarre i procedimenti non trattati dagli altri cursori già presenti.
Procedure modificata:
ISPETTORATO_MS
Tabella modificata:
ISP_PROVVEDIMENTI_MS |  |
| 20220127012 | Procura della Repubblica presso il Tribunale di Palermo | L’ufficio segnala che tentando di aggiungere fascicoli ad una specifica istruttoria di cumulo il click sul bottone "Iscrivi in istruttoria" non ha alcun effetto e non si ottiene nessun messaggio di errore. I fascicoli da unire sono tre, ma lo stesso risultato si ottiene selezionandoli singolarmente. | Per la risoluzione della problematica è stata corretta la funzione Javascript che verificava se un titolo che si stava iscrivendo era già in istruttoria cumulo. | Il problema era legato al fatto che la funzione Javascript testava il valore di un campo che non sempre era valorizzato (solo per determinate condizioni). E’ stato aggiunto un controllo preventivo.
Classi modificate:
/jsp/files/siap/siep/istruttoriacumulo/RicercaProcedimentiUfficio.jsp |  |
| 20220209011 | Procura della Repubblica presso il Tribunale per i Minorenni di Palermo | L’ufficio segnala che nel riepilogo ispettivo si trovano fra i procedimenti "in attesa di definizione" anche i fascicoli iscritti in istruttoria per cumulo ed archiviati a seguito di emissione del provvedimento di cumulo stesso. | Per la risoluzione della problematica è stata corretta la funzione di validazione del Cumulo per aggiungere sull'evento di archiviazione altro ufficio anche i dati di Operatore ed Ufficio Aggiornamento necessari per la corretta gestione della pena residua. | Il problema era legato al fatto che la classe action non valorizzava i campi operatore ed ufficio aggiornamento da passare al controller per la scrittura in banca dati. Tali informazioni sono necessarie poi per il recupero informazioni sulla pena residua.
Classi modificate:
siap.siep.modulocumulo.controller.DatiFinaliCumuloController.java |  |
| 202202160112 | Centro di Competenza Sistemi Area Penale | L’ufficio segnala, per la funzionalità di Cumulo, un Errore della funzione  restituzione fascicoli - funzione esterna. | Per la risoluzione della problematica è stata eliminata la pagina contenente le informazioni del dettaglio del Soggetto e della Sentenza, non pertinente, e che mandava in errore la form di restituzione in assenza di un fascicolo in sessione. | Il problema era legato al fatto che la pagina richiesta richiedeva la presenza in sessione del fascicolo, ma per la funzionalità di restituzione fascicolo tale informazione non è necessaria.
Corretta la classe:
/jsp/files/siap/siep/istruttoriacumulo/LoadRestituzioneFascicolo.jsp |  |
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
Aggiornamento Package “Ispettorato_MS”
Creazione indice in tabella “ISP_PROVVEDIMENTI_MS” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20220225-Piano_di_Rilascio_SIES_v.12.4.17.0.docx
SIUT-SIES-PT-1.0-20220225-Piano_dei_Test_SIES_v.12.4.17.0.docx
SIUT-SIES-CT-1.0-20220225-Allegato_al_piano_test_SIES_v.12.4.17.0.xls |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.16.0.
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
Creare sul server DB una cartella V_12_4_17_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_4_17_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_17_0 tramite il comando:
chmod 777 V_12_4_17_0
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx
Nella cartella appena creata (V_12_4_17_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_4_17_0/log/ in cui si può constatare l’esito dell’esecuzione.
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
Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 2.b e 2.e. All’avvio, infatti, tali cartelle verranno ricreate.
Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.