---
uniqueName: siut-sies-pr-1-0-20220128-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20220128 Piano di Rilascio SIES v 12 4 16 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20220128-Piano_di_Rilascio_SIES_v.12.4.16.0

> **File originale:** `RILASCIO_12.4.16.0/SIUT-SIES-PR-1.0-20220128-Piano_di_Rilascio_SIES_v.12.4.16.0.docx`  
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
| Data approvazione | 28/01/2022 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 28/01/2022 | Prima Emissione |  |


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
4.2	Riferimenti ChangeRequest (ADE/MEV)	11
4.2.1	Documenti a corredo della sessione di verifica conformità	11
5	Dettaglio degli elementi oggetto del rilascio	12
6	Installazione	13
6.1	Prerequisiti	13
6.2	Attività di preinstallazione	13
6.3	Attività di installazione	13
6.3.1	Installazione lato DB	13
6.3.1.1	Esecuzione script	13
6.3.2	Installazione applicazione	14
6.3.2.1	Deploy Applicazione	14
6.4	Attività di configurazione	15
6.5	Attività di post-installazione	15


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio del sistema SIES.
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.16.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.4.16.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.
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
| 20211129018 | Tribunale di Teramo | L’ufficio segnala che nell'effettuare il rinvio d'udienza l'applicativo restituisce un messaggio bloccante. | Per la risoluzione della problematica si intervenuti gestendo, in caso di esistenza di Provvedimento Definitorio, la possibilità di emettere un altro provvedimento (rinvio udienza o rinvio udienza da verbale) se lo stato del fascicolo è:
Opposizione - Accoglie (fissa l'udienza) = 14
Ricorso convertito in opposizione = 16
Decreto Fissazione Udienza = 20
Ricorso convertito in opposizione (Fissa Udienza) = 21 | Il problema era legato al fatto che nel caso di presenza di provvedimento definitorio non vi era alcun controllo sullo stato del fascicolo. E’ stato, quindi, aggiunto un controllo preventivo per consentire l’emissione di un provvedimento di rinvio udienza da verbale per quattro tipologie di stato del fascicolo.
Classi corrette:
siap/sige/udienzaprocedimento/action/ActLoadInserisciRinvioUdienza.java
siap/sige/web/ActionSige.java |  |
| 20211202015 | Centro di Competenza Sistemi Area Penale | L’ufficio segnala che il sistema, azionando la funzione "trasmissione provvedimento", per trasferire il provvedimento agli uffici di sorveglianza  pur confermando l'avvenuto trasferimento non trasferisce il procedimento. | Per la risoluzione della problematica è stato aggiunto un messaggio di controllo nel caso in cui tra i destinatari della comunicazione non vi siano Uffici di Esecuzione. | Il problema era legato al fatto che il sistema non trasmette digitalmente le comunicazioni alla Sorveglianza ma solo agli uffici esecuzione, per cui è stato fatto un intervento per rendere più chiari i messaggi che il sistema invia all'utente.
La classe modificata é:
siap.siep.modulocumulo.action.ActTrasferisciComunicazioniProcure.java |  |
| 20211216018 | Centro di Competenza Sistemi Area Penale | L’ufficio segnala che il sistema permette ad un utente di modificare, seppur parzialmente, un  procedimento di un altro ufficio. | Per la risoluzione della problematica è stato aggiunto un controllo per inibire le funzioni segnalate se il fascicolo non è di competenza. | Il problema era legato al fatto che il sistema consentiva di inviare comunicazioni a procure ed uffici di sorveglianza dal dettaglio del provvedimento di cumulo di un fascicolo di altro Ufficio. Mancava il controllo sulla competenza.
Classi modificate:
siap.siep.modulocumulo.action.ActLoadComunicazioniEsecSorv.java
/jsp/files/siap/siep/modulocumulo/GrigliaComunicazioniProcure.jsp |  |
| 20211220019 | Centro di Competenza Sistemi Area Penale | L’ufficio segnala che il sistema non classifica correttamente i procedimenti con istruttoria cumulo iniziale - Procedimenti in attesa di emissione provvedimenti del PM- attesa per istruttoria cumulo. | Per la risoluzione della problematica si è provveduto ad effettuare un intervento correttivo nel caso in cui venga effettuata la classificazione residuale utilizzando la tabella di decodifica. Solo per questo specifico caso, si è provveduto a censire sulla tabella di decodifica il codice ‘0340’ associandolo al tipo provvedimento ‘26’ (richiesta) ed alla classificazione statistica "Procedimenti in attesa di emissione provvedimenti del PM - Attesa per Istruttoria Cumulo" come richiesto nella segnalazione. | Il problema era legato al fatto che nella stored procedure (ISPETTORATO) non si teneva conto del tipo provvedimento oltre che del codice motivo.
Modifiche database:
package ISPETTORATO;
tabella STATO_ESECUZIONE_PROCEDIMENTO. |  |
| 20220110012 | Procura Generale presso la Corte d’Appello di Catania | L’ufficio segnala che nel documento di stampa non viene riportata la posizione giuridica del condannato, ancorché la stessa sia esattamente indicata nel programma. | Per la risoluzione della problematica è stato corretto il template segnalato per gestire anche la posizione giuridica '04' oltre alla '02'. | Il problema era legato al fatto che nel documento non veniva gestita la posizione segnalata.
Template modificato:
siep/ls/SIEP_LS_ODARI.rtf |  |
| 20220111017 | Procura della Repubblica presso il Tribunale di Reggio Emilia | L’ufficio segnala che in fase di estrazione dati della "Classe VII" dei procedimenti (riepilogo procedimenti pendenti), il programma restituisce un errore Oracle, qualsiasi intervallo di date venga selezionato. | Per la risoluzione della problematica è stata modificata la Stored Procedure (ISPETTORATO_CPP.stat_provvedimenti_CPP) per gestire la presenza di più record con stessa data che generava l'errore in fase di esecuzione. | Il problema era legato al fatto che la Stored Procedure  non gestiva la presenza di più record ‘PERIODI_ALTRE_SANZIONI’ con stessa ‘DATA_SCADENZA’.
Procedure modificata:
ISPETTORATO_CPP |  |
| 20220111018 | Procura della Repubblica presso il Tribunale di Reggio Emilia | L’ufficio segnala che l'operazione di ricerca degli atti ricevuti da altre procure risulta molto lenta e può impiegare anche 10/15 minuti. | Per la risoluzione della problematica è stata inserita la paginazione nella ricerca. Modificata la query iniziale per recuperare anche il numero di eventuali solleciti presenti sulla singola richiesta in modo da effettuare una ulteriore query per recuperare il dettaglio del sollecito solo se effettivamente presente. | Il problema era legato al fatto che la ricerca produceva in output tutti i risultati ottenuti senza effettuare la paginazione. Inoltre, la tabella MESSAGGIO non era indicizzata.
Classi modificate:
\jsp\files\siap\siep\misurasicurezza\ListaAttiRicevutiDaPrendereInCarico.jsp
siap.siep.misurasicurezza.action.ActRicercaAttiRicevuti
siap.jms.messaggio.model.MessaggioModel
siap.jms.messaggio.dao.MessaggioSqlDAO
\jsp\files\siap\siep\modulocumulo\Attesa_Cumulo.jsp
\jsp\files\siap\siep\misurasicurezza\AttesaRicerca.jsp
siap.siep.misurasicurezza.action.ICostantiMisuraSicurezza.java |  |
| 20220124013 | Centro di Competenza Sistemi Area Penale | L’ufficio segnala che se nel provvedimento di cumulo vengono assorbiti  procedimenti di altri uffici, nel redigere il provvedimento di cumulo, nella nota di trasmissione, questi non vengono riportati come autorità destinatarie. | Per la risoluzione della problematica è stato modificato il template ed il codice che ne caricava i dati. | Il problema era legato al fatto che il template ed il codice non erano predisposti a caricare i dati immessi nella nota di trasmissione del cumulo.
Classe modificata:
siap.siep.modulocumulo.controller.DatiFinaliCumuloController.java
Template modificato:
/siep/cumulo/NoteDiTrasmissione.rtf |  |
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
Inserimento record in tabella “STATO_ESECUZIONE_PROCEDIMENTO”
Aggiornamento Package “Ispettorato”
Aggiornamento Package “Ispettorato_CPP”
Creazione indice in tabella “MESSAGGIO” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| template.zip | Template | Template aggiornati:
SIEP_LS_ODARI.rtf
NoteDiTrasmissione.rtf |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20220128-Piano_di_Rilascio_SIES_v.12.4.16.0.docx
SIUT-SIES-PT-1.0-20220128-Piano_dei_Test_SIES_v.12.4.16.0.docx
SIUT-SIES-CT-1.0-20220128-Allegato_al_piano_test_SIES_v.12.4.16.0.xls |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.15.0.
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
Creare sul server DB una cartella V_12_4_16_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_4_16_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_16_0 tramite il comando:
chmod 777 V_12_4_16_0

In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx

Nella cartella appena creata (V_12_4_16_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_4_16_0/log/ in cui si può constatare l’esito dell’esecuzione.

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
Copiare i files contenuti nella cartella template\siep\ls
nella cartella “/var/SIES/template/siep/ls” sovrascrivendo quelli precedenti;
Copiare i files contenuti nella cartella template\siep\cumulo
nella cartella “/var/SIES/template/siep/cumulo” sovrascrivendo quelli precedenti;

Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 2.b e 2.e. All’avvio, infatti, tali cartelle verranno ricreate.

Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.