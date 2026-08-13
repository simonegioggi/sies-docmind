---
uniqueName: siut-sies-pr-1-0-20220624-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20220624 Piano di Rilascio SIES v 12 4 21 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20220624-Piano_di_Rilascio_SIES_v.12.4.21.0

> **File originale:** `RILASCIO_12.4.21.0/SIUT-SIES-PR-1.0-20220624-Piano_di_Rilascio_SIES_v.12.4.21.0.docx`  
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
| Data approvazione | 24/06/2022 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 24/06/2022 | Prima Emissione |  |


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
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.21.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.4.21.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.
Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.
# Identificazione degli elementi rilasciati
| Supporto | Oggetti: | Ver. | Del |
| --- | --- | --- | --- |
| Portale fornitura | SIUT > 06 - Rilasci Software > SIES > Rilascio SIES 12.4.21.0 2022-06-24 | 12.4.21.0 | 24/06/2022 |
| Note-osservazioni |  |  |  |


# Riferimenti degli oggetti del rilascio
## Riferimenti Anomalia (MAC/GAR)
| Rif. Ticket OTRS | Sede
Ufficio | Descrizione segnalazione | Descrizione
intervento | Descrizione Tecnica | Manuali corretti |
| --- | --- | --- | --- | --- | --- |
| 20220530011 | Tribunale di Sorveglianza di Genova | L’ufficio segnala che In fase di emissione di una ordinanza, con oggetto “REVOCA ORDINANZA”, viene selezionato l’esito REVOCA. Confermato l’inserimento il sistema restituisce l’esito “ACCOGLIE PROPOSTA E REVOCA”, attinente ad altro, e diverso, oggetto. Inemendabile. | Per la risoluzione della problematica è stata aggiornata la tabella CG_REF_CODES aggiornando, per il dominio “ESITO_TENORE”, nel record con valore “0158”, il campo “rv_abbreviation” al valore dell’esito corretto (ESITO_PROVVEDIMENTO pari a REVOCA). | Il problema era causato dal fatto che nel database non esisteva una corretta correlazione tra oggetto ed esito.
Tabella modificata:
CG_REF_CODES |  |
| 202206010110 | Nessuno | L’ufficio segnala che la Cautelare indicata sul foglio Complementare è errata. Al SIEP, il periodo di cautelare è stato indicato come NON computabile. Invece, nel Foglio complementare è riportata come cautelare computata. | Per la risoluzione della problematica è stato modificato il template segnalato inserendo un controllo sulla computabilità della misura cautelare, in modo da non menzionare i periodi non computabili. | Il problema era legato alla mancanza del test sul campo del database “flagComputabile” nel Template di stampa.
Template modificato:
SIEP_ARC_ALTRA_AUTORITA.rtf |  |
| 20220606017 | Tribunale per i Minorenni di Roma | L’ufficio segnala la necessità di inserire un alert sul campo "Luogo svolgimento della prova" nella maschera relativa all'emissione di un'ordinanza e del suo dettaglio in quanto ha superato il limite consentito di 100 caratteri ed il sistema prima di confermare l'operazione non l'ha bloccata. Successivamente al momento dell'iscrizione del fascicolo come magistrato di sorveglianza del Tribunale dei minorenni il sistema ha dato il messaggio bloccante ma solo in un secondo tempo. | Per la risoluzione della problematica è stata alterata la tabella “ESECUZIONE_MISURA_ALTERNATIVA” con l'aumento dei caratteri di scrittura del campo “LUOGO_ESECUZIONE_MISURA” da 100 a 2000. | Il problema era causato dalla dimensione della colonna “LUOGO_ESECUZIONE_MISURA” di soli 100 caratteri della tabella “ESECUZIONE_MISURA_ALTERNATIVA” rispetto alla dimensione di 2000 caratteri dell'analoga colonna “LUOGO_SVOLGIMENTO_PROVA” della tabella “DEPOSITO_ORDINANZA_PC”.
Tabella modificata:
ESECUZIONE_MISURA_ALTERNATIVA |  |
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
Aggiornamento in tabella “CG_REF_CODES”
Alterazione della tabella “ESECUZIONE_MISURA_ALTERNATIVA”
Aggiornamento versione SIES in tabella “VERSIONE” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| template.zip | Template | Template aggiornato:
SIEP_ARC_ALTRA_AUTORITA.rtf |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20220624-Piano_di_Rilascio_SIES_v.12.4.21.0.docx
SIUT-SIES-PT-1.0-20220624-Piano_dei_Test_SIES_v.12.4.21.0.docx
SIUT-SIES-CT-1.0-20220624-Allegato_al_piano_test_SIES_v.12.4.21.0.xls |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.20.0.
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
Creare sul server DB una cartella V_12_4_21_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_4_21_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_21_0 tramite il comando:
chmod 777 V_12_4_21_0
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx
Nella cartella appena creata (V_12_4_21_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_4_21_0/log/ in cui si può constatare l’esito dell’esecuzione.
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