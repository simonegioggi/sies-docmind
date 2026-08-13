---
uniqueName: siut-sies-pr-1-0-20210521-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20210521 Piano di Rilascio SIES v 12 4 10 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20210521-Piano_di_Rilascio_SIES_v.12.4.10.0

> **File originale:** `RILASCIO_12.4.10.0/SIUT-SIES-PR-1.0-20210521-Piano_di_Rilascio_SIES_v.12.4.10.0.docx`  
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
| Data approvazione | 21/05/2021 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 21/05/2021 | Prima Emissione |  |


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
4.2	Riferimenti ChangeRequest (ADE/MEV)	12
4.2.1	Documenti a corredo della sessione di verifica conformità	12
5	Dettaglio degli elementi oggetto del rilascio	13
6	Installazione	14
6.1	Prerequisiti	14
6.2	Attività di preinstallazione	14
6.3	Attività di installazione	14
6.3.1	Installazione lato DB	14
6.3.1.1	Esecuzione script	14
6.3.2	Installazione applicazione	15
6.3.2.1	Deploy Applicazione	15
6.4	Attività di configurazione	15
6.5	Attività di post-installazione	16


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio del sistema SIES.
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.10.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.4.10.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.

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
| 202104210111 | Tribunale di Torino | L'Ufficio segnala che nella maschera di inserimento avvocato relativo alle parti il sistema non riporta il tasto torna indietro per ritornare sulla maschera di inserimento dati relativo alla parte. | Per la risoluzione della problematica si è intervenuti con la gestione del tasto indietro. Inoltre, è stato corretto l’errore di caricamento del form dopo la cancellazione Parti Udienza. | Sono state modificate le classi:
siap.sige.udienzaparti.controller.PartiUdienzaController.java
in cui è stato attivato il codice che non inseriva la Action nella coda di navigazione;
siap.sige.udienzaparti.action.ActLoadModificaDifensore.java
in cui è stato corretto il controller che recupera i dati dopo la cancellazione delle Parti Udienza. |  |
| 202104230110 | Cisia di Torino | L’ufficio segnala che quando iscrive un procedimento con due ordinanze di concessione (Affidamento in Prova e Liberazione Anticipata) in una istruttoria di cumulo, allora nel dettaglio dello stato di esecuzione viene trascritta solamente l’ordinanza di concessione liberazione anticipata. | Per la risoluzione della problematica si è intervenuti con la correzione della gestione dei Provvedimenti della Sorveglianza in assenza di provvedimenti di esecuzione di Procura. | Sono state modificate le classi:
siap.siep.modulocumulo.controller.StatoEsecTitoloCumulatoController.java
nel metodo “caricaComputiMisuraAlternativaSORV” in cui si dava per scontata la presenza dell'evento SIEP di esecuzione da cui cercava 	di recuperare la pena residua e l'eventuale sospensione (per le sospensioni/revoche della sorveglianza).
In assenza del Provvedimento SIEP il sistema andava in “NullPointer Exception” nella fase di recupero della pena residua. Aggiunto controllo per evitare tale errore. |  |
| 20210430011 | Procura della Repubblica presso il Tribunale di Termini Imerese (PA) | L’ufficio segnala che nell'inserire un provvedimento di liberazione anticipata su un fascicolo SIES, l'applicazione restituisce un errore "NullPointer Exception". | Per la risoluzione della problematica si è intervenuti con la correzione della mancata scrittura del record “ALTRA_CAUSA” in fase di validazione del provvedimento di cumulo. | Sono state modificate le classi:
siap.siep.modulocumulo.action.ActInserisciPosGiuridicaCumulo.java
siap.siep.modulocumulo.action.ActValidaProvvedimentoCumulo.java
siap.siep.modulocumulo.controller.DatiFinaliCumuloController.java
in cui è stata corretta la gestione del flag “ALTRA_CAUSA” sul fascicolo SIEP che è stata spostata in fase di validazione del Cumulo. Inoltre, non inseriva il record “ALTRA_CAUSA” che mandava in errore la funzione segnalata. Aggiunta, quindi, funzionalità di inserimento del record in banca dati. |  |
| 202105030111 (AVVOCATURA SIUS) | DGSIA - Referente Applicativo | L’utente segnala il  disallineamento della visibilità della fissazione dell’udienza tra le diverse maschere consultabili dagli avvocati: l’intervento da effettuare deve andare nella direzione di rendere visibile la fissazione dell’udienza solo dopo la validazione della fissazione a prescindere dal tipo di ricerca che viene effettuata. | Per la risoluzione della problematica si è intervenuti con la modifica della classe e della Store Procedure in cui vengono estratti i dati da inviare al sistema chiamante. | E’ stata modificata la classe:
FascicoloSiusSoggettoSqlDAO.java
modificando la query preposta ad inviare tramite web service i dati al sistema “AVVOCATURA”; in questo caso viene inviata l’informazione circa i procedimenti a carico di un dato soggetto. Inoltre è stato modificato il package:
AVVOCATURA_SIUS
In esso è stata modificata la procedura CERCA_PROVVEDIMENTI, che recupera i dati per i provvedimenti validati di un dato procedimento. |  |
| 202105030112 (AVVOCATURA SIUS) | DGSIA - Referente Applicativo | L’utente segnala un problema emerso durante le ultime verifiche relativo allo stato del procedimento in caso di deposito non validato. Se, infatti, allo stato correttamente non risulta l’emissione del provvedimento sulla stringa che compare a seguito della ricerca da soggetto, nella scheda del procedimento compare lo stato “emesso provvedimento” e questo, ovviamente, non è corretto. Probabilmente l’errore nasce dal fatto che su SIUS lo stato cambia con il semplice deposito del provvedimento anche prima della validazione, ma nell’ambito della visualizzazione da parte degli avvocati, questo non è corretto. | Per la risoluzione della problematica si è intervenuti con la modifica della Store Procedure in cui vengono estratti i dati da inviare al sistema chiamante. | E’ stato modificato il package:
AVVOCATURA_SIUS
In esso è stata modificata la procedura CERCA_FASIUS_PER_ESTREMI, che recupera i dati per un procedimento in cui la dicitura “Emesso Provvedimento” deve apparire solo quando il decreto o l'ordinanza sono depositate ed il deposito sia validato. |  |
| 20210504014 | DGSIA - Referente Applicativo | L’utente segnala che per la tabella "Avvisi_Avvocato" sembra esserci una discrepanza tra la descrizione dei campi "COGNOME_SOGGETTO" e "NOME_SOGGETTO" ed il loro effettivo contenuto. In tali campi  in realtà sono presenti il cognome ed il nome del soggetto del fascicolo e non quelli dell'avvocato. | Per la risoluzione della problematica si è intervenuti con la modifica della tabella nel database e del documento che la descrive. | Sono stati modificati:
tabella “AVVISI_AVVOCATO”
In essa sono stati modificati i commenti ai campi ‘COGNOME_SOGGETTO’ e ‘NOME_SOGGETTO’);
manuale “SIGI_PNL_ML_20210423_1.6_Modello dei Dati_SIES”
E’ stata consegnata la nuova versione 1.7. | SIGI_PNL_ML_20210521_1.7_Modello dei Dati_SIES.pdf |
| 20210506013 | Procura Generale presso la Corte d’Appello di Ancona | L’ufficio segnala che in caso di archiviazione  di fascicoli con ergastolo per assorbimento cumulo, la statistica li cataloga  erroneamente come pendenti. | Per la risoluzione della problematica si è intervenuti con la correzione del package “ISPETTORATO” che riclassificava come pendenti gli ergastoli classificati in un primo momento come archiviati. | E’ stato modificato il package:
ISPETTORATO
In esso è stata modificata la procedura STAT_PROVVEDIMENTI in cui viene valorizzato come archiviato il fascicolo per evitare che venga riclassificato come pendente in caso di ergastolo. |  |
| 20210507017 | Procura della Repubblica presso il Tribunale di Perugia | L’ufficio segnala che nelle ricerche del soggetto il sistema rimane sempre in attesa di risposta. La ricerca del soggetto su altre BDI non va a buon fine. | Per la risoluzione della problematica si è intervenuti con la modifica della classe che all’avvio del SIES è deputata a caricare in memoria l'elenco di tutte le BDI con i relativi codici prelevati dalla tabella “JMS_CODE” per il dominio "BDI". I suddetti codici vengono utilizzati per effettuare le ricerche su tutte le BDI. La procedura amministrativa "Test Sistema" leggeva i dati caricati in memoria e li sovrascriveva erroneamente con il contenuto del dominio CONN_JMS_STRING prelevato sempre dalla tabella JMS_CODE.
Conseguenza di ciò era che il contenuto della variabile, con l'elenco dei codici BDI, era errato e, pertanto, fallivano le successive ricerche su tutte le BDI. Si è intervenuti rimuovendo questa anomalia. | E’ stata modificata la classe:
siap.sico.test.controller.TestController.java
In essa, nel metodo “prelevaDati”, gli veniva passato il contenuto della classe Singleton che mappa i codici BDI e sovrascriveva il codice con la “connection string” al fine di generare la stampa. Dal momento del lancio del test il contenuto del singleton risultava errato e falliva la ricerca in altre BDI in fase di inserimento nella tabella MESSAGGIO.COD_BDI_DESTINATARIA. |  |
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
| c. Specifiche Dati (Schema Concettuale, Schema Logico e Schema Fisico) | SIGI_PNL_ML_20210521_1.7_Modello dei Dati_SIES.pdf | SIUT > 06 - Rilasci Software > SIES > Rilascio SIES 12.4.10.0 2021-05-21 > Documentazione > documentazione.zip |
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
Aggiornamento tabella “AVVISI_AVVOCATO”
Aggiornamento Package “AVVOCATURA_SIUS”
Aggiornamento Package “ISPETTORATO” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20210521-Piano_di_Rilascio_SIES_v.12.4.10.0.docx
SIUT-SIES-PT-1.0-20210521-Piano_dei_Test_SIES_v.12.4.10.0.docx
SIUT-SIES-CT-1.0-20210521-Allegato_al_piano_test_SIES_v.12.4.10.0.xls
SIGI_PNL_ML_20210521_1.7_Modello dei Dati_SIES.pdf |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.9.0.
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
Creare sul server DB una cartella V_12_4_10_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_4_10_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_10_0 tramite il comando:
chmod 777 V_12_4_10_0

In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx

Nella cartella appena creata (V_12_4_10_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_4_10_0/log/ in cui si può constatare l’esito dell’esecuzione.

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