---
uniqueName: siut-sies-pr-1-0-20231027-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20231027 Piano di Rilascio SIES v 12 5 4 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20231027-Piano_di_Rilascio_SIES_v.12.5.4.0

> **File originale:** `RILASCIO_12.5.4.0/SIUT-SIES-PR-1.0-20231027-Piano_di_Rilascio_SIES_v.12.5.4.0.docx`  
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
| Data approvazione | 27/10/2023 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 27/10/2023 | Prima Emissione |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Aurora Garofalo | Amministrazione |  | Responsabile Unico Procedimento |
| Dott. Oris Orlando | Amministrazione |  | Direttore Esecutivo Contratto |
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
6.4	Attività di configurazione	14
6.5	Attività di post-installazione	14


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio del sistema SIES.
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.5.4.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.5.4.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.
Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.
# Identificazione degli elementi rilasciati
| Supporto | Oggetti: | Ver. | Del |
| --- | --- | --- | --- |
| Portale fornitura | SIUT > 06 - Rilasci Software > SIES > Rilascio SIES 12.5.4.0 2023-10-27 | 12.5.4.0 | 27/10/2023 |
| Note-osservazioni |  |  |  |


# Riferimenti degli oggetti del rilascio
## Riferimenti Anomalia (MAC/GAR)
| Rif. Ticket OTRS | Sede
Ufficio | Descrizione segnalazione | Descrizione
intervento | Descrizione Tecnica | Manuali corretti |
| --- | --- | --- | --- | --- | --- |
| 20220210013 | Referente Applicativo DGSIA | L’ufficio segnala che occorre verificare, in particolare su soggetti stranieri, l'indicazione del casellario locale di destinazione dei fogli complementari.  Tenendo conto anche degli uffici accorpati.
 "L’ufficio iscrizione" (*) è l'ufficio presso l'autorità giudiziaria che ha emesso il provvedimento giudiziario soggetto a iscrizione o a eliminazione, che ha competenze nella materia del presente testo unico;
(*) Ufficio Locale
La verifica va effettuata su tutta la gestione della funzione - in quanto sono saltati tutti i controlli tornando alla gestione precedente alla riforma del 2022.
Verificare il template, allegato, in quanto manca il destinatario nella nota di trasmissione | Per la risoluzione della problematica sono stati modificati i template al fine di visualizzare "Casellario Giudiziale di <UfficioUtenteConnesso>" | Il problema era legato al fatto che per soggetti stranieri il sistema proponeva sempre la dicitura "Casellario Giudiziale di Roma".
Template modificati:
import\FoglioComplementareLsRs.rtf
import\FoglioComplementareLsRs_L.199.rtf
import\FoglioComplementareSosp.rtf
siep\ls\SIEP_LS_OLNI.rtf
siep\ls\SIEP_LS_OLQNI.rtf |  |
| 202211110114 | Referente Applicativo DGSIA | L’ufficio segnala che il sistema riporta il valore “Emesso Provvedimento” nella colonna riservata “Motivo Altra Definizione Opposizione / Ricorso” | Per la risoluzione della problematica sono stati riportati solo i valori dello "STATO_FASCICOLO" per i valori ('05', '06', '14', '15', '16', '17', '18', '19', '21') se e solo se la data di definizione non è nulla | Il problema era legato al fatto che il sistema riportava il valore "Emesso Provvedimento" nella colonna 	riservata "Motivo Altra Definizione Opposizione/Ricorso" della statistica "Procedimento SIGE per Estremi Atto".
Classe modificata:
/siesWeb/src/siap/sige/fascicolo/dao/FascicoloSigeSqlDAO.java |  |
| 202303280119 | Referente Applicativo DGSIA | L’ufficio segnala la riclassificazione dei procedimenti oltre al cambiamento della posizione giuridica | Per la risoluzione della problematica, per il dato pregresso, sono stati predisposti due script che sanano le casistiche riguardanti l'errore segnalato | Il problema era legato al fatto che  per i provvedimenti con codice motivo:
•MOTIVO_PROVVEDIMENTO    0019    (archiviazione  per assorbimento in  cumulo stesso ufficio)
•MOTIVO_PROVVEDIMENTO    0356    (Cumulo stesso ufficio)
non vengono impostati correttamente nella tabella "EVENTO" il campo "DATA_AGGIORNAMENTO" e nella tabella collegata "PENA_RESIDUA" il campo "COD_UFFICIO_INSERIMENTO" |  |
| 202309110116 | Tribunale di Busto Arsizio (MI) | L’ufficio segnala che nella ricerca dei procedimenti per singolo soggetto su SIGE, l'esito dell'elenco procedimenti indica che ne sono presenti 2, ma se si va a visualizzare il dettaglio dei procedimenti estratti, il risultato è di un unico fascicolo | Per la risoluzione della problematica è stata modificata la vista “v_soggetto_maggiorenne_new", recuperando i dati direttamente dal soggetto collegato al fascicolo SIGE e, solo in assenza di informazioni, si prova a recuperare la data di nascita dal Soggetto SIEP collegato tramite la tabella "FAS_SIGE_SENTENZA" | Il problema era legato al fatto che il fascicolo SIGE era collegato a due titoli esecutivi relativi
allo stesso soggetto ma con due date di nascita differenti |  |
| 20231010019 | Procura della Repubblica presso il Tribunale di Trieste | L’ufficio segnala che a seguito di trasmissione per competenza di un procedimento SIEP della Procura di Milano, quindi non in carico all’Ufficio segnalante, adesso questi atti risultano "pendenti": non possono essere restituiti e, provando a prenderli in carico, si verifica un errore | Per la risoluzione della problematica sono stati resi visibili solo se procedimento di competenza | Il problema era legato al fatto che su un fascicolo di altra BDI preso in carico andando su elenco provvedimenti del PM e selezionando il dettaglio del provvedimento di trasmissione atti erano
visibili i tasti di:
- trasmissione atti
- Annotazione Esito
- Seguito Atti
anche se il fascicolo non era di competenza dell'ufficio.
Classe modificata:
/siap/siep/richiesta/DettaglioTrasmissioneCompetenza.jsp |  |
| 20231017016 | Referente Applicativo DGSIA | L’ufficio segnala che nella procedura di estrazione, classe I, sono presenti anche i procedimenti di classe II | Per la risoluzione della problematica è stata aggiunta la condizione restrittiva che il fascicolo debba essere solo di classe I | Il problema era legato al fatto che la procedura di estrazione dei fascicoli di classe I,
presentava anche i procedimenti di altre classi |  |
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
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20231027-Piano_di_Rilascio_SIES_v.12.5.4.0.docx
SIUT-SIES-PT-1.0-20231027-Piano_dei_Test_SIES_v.12.5.4.0.docx
SIUT-SIES-CT-1.0-20231027-Allegato_al_piano_test_SIES_v.12.5.4.0.xls |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| aggiorna_db.zip | Database | Aggiornamento versione SIES in tabella “VERSIONE”
Aggiornamento nelle tabelle “EVENTO” e “PENA_RESIDUA”
Aggiornamento vista “V_SOGGETTO_MAGGIORENNE_NEW”
Aggiornamento package body “ISPETTORATO” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| template.zip | Template | sius\de\SIUS_DE_DECRETOCITAZIONE-UDS.rtf
import\FoglioComplementareLsRs.rtf
import\FoglioComplementareLsRs_L.199.rtf
import\FoglioComplementareSosp.rtf
siep\ls\SIEP_LS_OLNI.rtf
siep\ls\SIEP_LS_OLQNI.rtf |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.5.3.0.
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
Creare sul server DB una cartella V_12_5_4_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_5_4_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_5_4_0 tramite il comando:
chmod 777 V_12_5_4_0
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES...........: siesxx	(dove xx è la sigla del distretto di appartenenza, per esempio: rm per Roma)
Password_SIES.......: siesxx
Nella cartella appena creata (V_12_5_4_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_5_4_0/log/ in cui si può constatare l’esito dell’esecuzione.
N.B. Le segnalazioni del tipo:
ORA-00001: violata restrizione di unicità
ORA-00955: name is already used by an existing object
Cartella log già presente
ORA-04043: object does not exist
sono da considerarsi warning e non errori.
Accedere ad oracle (con qualsiasi strumento tipo toad, developer, …) come utente siesxx e compilare tutte le procedure e i package che non risultano compilate.
ATTENZIONE: la procedura “SUPER_SOGGETTO_PREGR” ed il package “CARICA_RES” potrebbero restare non compilate: non è da considerarsi errore.
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
Copiare i files contenuti nella cartella template\import
nella cartella “/var/SIES/template/import” sovrascrivendo quelli precedenti;
Copiare i files contenuti nella cartella template\siep\ls
nella cartella “/var/SIES/template/siep/ls” sovrascrivendo quelli precedenti;
Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 2.b e 2.e. All’avvio, infatti, tali cartelle verranno ricreate.
Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.