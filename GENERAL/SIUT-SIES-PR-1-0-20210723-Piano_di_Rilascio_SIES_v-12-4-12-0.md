---
uniqueName: siut-sies-pr-1-0-20210723-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20210723 Piano di Rilascio SIES v 12 4 12 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20210723-Piano_di_Rilascio_SIES_v.12.4.12.0

> **File originale:** `RILASCIO_12.4.12.0/SIUT-SIES-PR-1.0-20210723-Piano_di_Rilascio_SIES_v.12.4.12.0.docx`  
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
| Data approvazione | 23/07/2021 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 23/07/2021 | Prima Emissione |  |


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
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario e Referente Tecnico |
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
5	Dettaglio degli elementi oggetto del rilascio	13
6	Installazione	14
6.1	Prerequisiti	14
6.2	Attività di preinstallazione	14
6.3	Attività di installazione	14
6.3.1	Installazione lato DB	14
6.3.1.1	Esecuzione script	14
6.3.2	Installazione applicazione	15
6.3.2.1	Deploy Applicazione	15
6.4	Attività di configurazione	16
6.5	Attività di post-installazione	16


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio del sistema SIES.
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.12.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.4.12.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.

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
| 20210621016 | Procura della Repubblica presso il Tribunale di Torino | L’ufficio segnala l'assenza della funzione di dettaglio per la consultazione dei procedimenti presenti nell’elenco impedendo la visione del dettaglio del procedimento. | Per la risoluzione della problematica si è intervenuti con il rilascio di uno script per il database. | E’ stato rilasciato il file “20210621016.sql” che consente di colmare la mancanza nel Database del collegamento tra la funzione di dettaglio e la funzione di ricerca fascicolo (action “ActListaFascicoloPerSoggettoCodCui”) |  |
| 20210622011 | Procura della Repubblica presso il Tribunale di Torino | L'Ufficio segnala che selezionando la funzione selezione per annotazione l'ordinanza del giudice dell’esecuzione  per  concessione indulto  con opzione "in conformità" il sistema nei campi di quantificazione della pena li compila con la dicitura "Null". | Per la risoluzione della problematica si è intervenuti con la correzione del fatto che non venivano recuperati correttamente i campi dalla tabella delle richieste al GE presenti in maschera. | Sono state modificate le classi nelle form delle Decisioni del GE (Amnistia/Indulto, Depenalizzazione, Incostituzionalità) in cui erano state commentate le righe che precaricavano i dati delle richieste.
Quando si selezionava la richiesta del GE ed il radio button "In conformità" la funzione Javascript non trovando i dati caricava i campi con "undefined" o "NaN". Su indicazione dell’utente sono stati ripristinati i campi.
Classi corrette:
siap\siep\calcolopena\LoadAnnotazioniManualiBenefici.jsp
siap\siep\calcolopena\LoadGEDepen.jsp
siap\siep\calcolopena\LoadGEIncost.jsp
Corretta anche la popup delle richieste, che andava in errore Javascript nel caso di Amnistia/Indulto.
Referenziava i campi della classe della depenalizzazione:
siap\siep\richiesta\ListaRichiesteAlGE.jsp
Aggiunto GUP nella combo autorità
siap.siep.calcolopena.action.ActLoadInserisciAnnotazioniManuali.java |  |
| 202106220110 | Procura della Repubblica presso il Tribunale di Palermo | L’ufficio segnala che in un fascicolo SIEP della Procura di Palermo, il tentativo di stampa del decreto di irreperibilità genera l'errore:
--> F3BException --> Eccezione di sistema:
EventoController.ExStampaDocumento: f3b.util.F3BException: StatoEsecuzioneController.appendStatoEsecuzione: java.lang.NullPointerException. | Per la risoluzione della problematica si è intervenuti con la aggiunta di controlli di obbligatorietà dei dati nel form. Corretta funzione di recupero “RINNOVI” per prendere in considerazione solo i rinnovi validati con data rinnovo valorizzata. | E’ stata modificata la classe:
siap/siep/notifica/LoadRinnovazioneNotifica.jsp
in cui è stata corretta la funzione Javascript di rinnovazione che consentiva l'inserimento senza controllo dei dati.
Resa obbligatoria Data e Destinatario.
Modificato il modulo di stampa che prelevava il record RINNOVAZIONE senza controllare la presenza della DATA (unico dato di interesse):
siap.siep.statoesecuzione.controller.StatoEsecuzioneController.java
Modificato il metodo “appendStatoEsecuzione” nella classe:
siap.siep.rinnovo.dao.RinnovoSqlDAO.java
Aggiunto un metodo per recuperare solo i “RINNOVI” con “DATA_RINNOVO” valorizzata (per gestire il progresso). Nella classe:
siap.siep.rinnovo.controller.IRinnovo.java
aggiunto il metodo “ExRicercaUltimoRinnovoByKeyEvento”;
Nella classe:
siap.siep.rinnovo.controller.IRinnovoController.java
aggiunto il metodo “ExRicercaUltimoRinnovoByKeyEvento”. |  |
| 20210624014 | Tribunale di Sorveglianza di Perugia | L’ufficio segnala l'errore su un fascicolo SIUS al momento della conferma dell'emissione di un'Ordinanza o di una Misura di sicurezza: al momento dell'inserimento della Misura di sicurezza abbiamo l'errore bloccante “java.lang.NullPointerException”. | Per la risoluzione della problematica si è intervenuti con la modifica alla query per recuperare il tipo di iscrizione della misura di sicurezza. | E’ stato corretto l’errore in fase di recupero del “RIFERIMENTO_FASCICOLO_SIEP” che decodificava il “flag_ms_SN” sempre ad “N”. Modificata la classe:
siap.sius.rifasiep.dao.RiferimentoFascicoloSiepSqlDAO.java
Corretta anche la classe:
siap/sius/misurasicurezza/DettaglioSiusMisuraSicurezza.jsp
poiché se si inseriva un riferimento ad una misura di sicurezza indicava che era una pena pecuniaria.
Corretta anche la classe:
siap/sius/rifasiep/LoadInserisciRifFascicoloSiep.jsp
poiché era presente un errore Javascript per due variabili con nome errato e veniva fatto un controllo non pertinente sull'anagrafica anche se non selezionata. |  |
| 20210709014 | Procura Generale presso la Corte d’Appello di Catania | L’ufficio segnala che nella stampa del foglio complementare, non compaiono i dati precedentemente inseriti riguardanti l'espiazione della pena. | Per la risoluzione della problematica si è intervenuti con il rilascio del template opportunamente modificato. | E’ stato rilasciato il documento “SIEP_ARC_FOGLIO_COMP_ESP.rtf” in cui è stata aggiunta al suo interno la gestione della posizione “50” equivalente ad “Esecuzione presso domicilio della pena detentiva”. |  |
| 20210709019 | Tribunale per i Minorenni di Roma | L’ufficio segnala che come da verifiche eseguite da applicativo l'utente non ha la possibilità di modificare o cancellare le "definizioni del procedimento" effettuate manualmente.
L'utente afferma che nonostante sia "Superutente SIES",  non ha possibilità di cancellare l'iscrizione indicata nell’allegato per cui si richiede urgentemente un intervento. | Per la risoluzione della problematica si è intervenuti con la correzione della classe che visualizzava i bottoni. Non gestiva correttamente gli uffici “TDSM” ed “UDSM”. | E’ stata modificata la classe:
siap\sico\security\toolbar_header.jsp
in cui esisteva la gestione per gli uffici “UDS” e “TDS” ma non per quelli “TDSM” ed “UDSM” motivo per cui non visualizzava alcuni bottoni collegati alle funzionalità di modifica e cancellazione. |  |
| 20210715018 | Procura della Repubblica Presso il Tribunale di Torino | L’ufficio segnala un errore sul template in cui risulta mancante la trascrizione del quantitativo di  pena fungibile. | Per la risoluzione della problematica si è intervenuti con il rilascio del template opportunamente modificato. | E’ stato rilasciato il documento “SIEP_AM_COMPU657_3.rtf” in cui è stata corretta la sezione riguardante il caricamento dei giorni di pena fungibile computati. |  |
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
Aggiornamento tabella “RELAZIONE_FUNZIONE” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| template.zip | Template | Template aggiornati:
SIEP_AM_COMPU657_3.rtf
SIEP_ARC_FOGLIO_COMP_ESP.rtf |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20210723-Piano_di_Rilascio_SIES_v.12.4.12.0.docx
SIUT-SIES-PT-1.0-20210723-Piano_dei_Test_SIES_v.12.4.12.0.docx
SIUT-SIES-CT-1.0-20210723-Allegato_al_piano_test_SIES_v.12.4.12.0.xls |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.11.0.
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
Creare sul server DB una cartella V_12_4_12_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_4_12_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_12_0 tramite il comando:
chmod 777 V_12_4_12_0

In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx

Nella cartella appena creata (V_12_4_12_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_4_12_0/log/ in cui si può constatare l’esito dell’esecuzione.

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
Copiare i files contenuti nella cartella template\siep\am
nella cartella “/var/SIES/template/siep/am” sovrascrivendo quelli precedenti;
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