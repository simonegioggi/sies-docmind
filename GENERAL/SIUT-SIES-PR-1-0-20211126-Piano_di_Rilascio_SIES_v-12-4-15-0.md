---
uniqueName: siut-sies-pr-1-0-20211126-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20211126 Piano di Rilascio SIES v 12 4 15 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20211126-Piano_di_Rilascio_SIES_v.12.4.15.0

> **File originale:** `RILASCIO_12.4.15.0/SIUT-SIES-PR-1.0-20211126-Piano_di_Rilascio_SIES_v.12.4.15.0.docx`  
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
| Data approvazione | 26/11/2021 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 26/11/2021 | Prima Emissione |  |


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
4.2	Riferimenti ChangeRequest (ADE/MEV)	10
4.2.1	Documenti a corredo della sessione di verifica conformità	10
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
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.15.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.4.15.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.
Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.
# Identificazione degli elementi rilasciati
| Supporto | Oggetti: | Ver. | Del |
| --- | --- | --- | --- |
| Portale fornitura | SIUT > 06 - Rilasci Software > SIES > Rilascio SIES 12.4.15.0 2021-11-26 | 12.4.15.0 | 26/11/2021 |
| Note-osservazioni |  |  |  |


# Riferimenti degli oggetti del rilascio
## Riferimenti Anomalia (MAC/GAR)
| Rif. Ticket OTRS | Sede
Ufficio | Descrizione segnalazione | Descrizione
intervento | Descrizione Tecnica | Manuali corretti |
| --- | --- | --- | --- | --- | --- |
| 20211014013 | Tribunale di Genova | L’ufficio segnala che, in generale, nell’emettere ordinanza riguardante la revoca di sospensione condizionale della pena (art. 163 C.P.) concernente più sentenze ben iscritte su un unico procedimento SIGE accade che il sistema di default ne indichi una soltanto; di conseguenza le sentenze mancanti devono essere totalmente riportate nel provvedimento vanificando così il lavoro già svolto durante la registrazione del procedimento. Si chiede perché il sistema ribalta una sola sentenza anziché tutte quelle iscritte. | Per la risoluzione della problematica è stata modificata la costruzione dell'xml di stampa e del template per contemplare il caso di più sentenze legate allo stesso Oggetto. | Il Problema era legato al fatto che nel caso di presenza di più titoli sullo stesso OGGETTO, in fase di stampa dell'ordinanza riportava solo la prima sentenza nella sezione della decisione. Di conseguenza anche il template è stato gestito per accogliere una o più sentenze.
Classe corretta:
siap.sige.stampa.controller.StampaSigeController.java
Template corretto:
SIGE_OR_MODGENERICO.rtf |  |
| 20211019014 | Centro di Competenza Sistemi Area Penale | L’ufficio segnala che nel prendere in carico un procedimento per procedere all'iscrizione in classe IV il sistema lo impedisce. | Per la risoluzione della problematica è stata modificata la funzione di presa in carico per gestire il caso di fascicoli trasferiti privi del record ALTRA_CAUSA. | Corretta la classe:
siap.siep.jms.controller.PresaInCaricoJMSController.java
dove il problema era legato più genericamente alla fase di caricamento di un fascicolo SIEP se presente FLAG_ALTRA_CAUSA = N sul fascicolo ma la posizione giuridica trasferita contiene un puntamento al record ALT_CAU_ID_ALTRA_CAUSA; chi invia aggiunge il record ALTRA_CAUSA solo se FASCICOLO_SIEP.FLAG_ALTRA_CAUSA = S, chi riceve invece si ritrova con il record PG da inserire che punta un record ALTRA_CAUSA non ricevuto e quindi va in errore. Corretto il modulo di acquisizione per ripulire il campo POSIZIONE_GIURIDICA.ALT_CAU_ID_ALTRA_CAUSA prima dell'inserimento se non è stato ricevuto il record ALTRA_CAUSA. |  |
| 20211022013 | Centro di Competenza Sistemi Area Penale | L’ufficio segnala che il template non riporta la decorrenza e scadenza pena dell'arresto. La correzione va estesa su tutti i provvedimenti  con soggetti detenuti in regime di detenzione - o misura alternativa. Nel modulo sono segnalati altre anomalie sulle note di trasmissione. | Per la risoluzione della problematica si è proceduto a correggere il template secondo le indicazioni contenute nel ticket. | Template corretti:
SIEP_CUMULO_OE_656_DET.rtf
NoteDiTrasmissione.rtf
in cui sono state gestite le date di decorrenza e scadenza pena dell’arresto. |  |
| 20211102019 | Centro di Competenza Sistemi Area Penale | L’ufficio segnala che il sistema non estrae tutti i procedimenti e che vi è una errata classificazione dei procedimenti. | Per la risoluzione della problematica si è proceduto con la modifica del Package Body “ISPETTORATO_MS” in cui se un fascicolo è classificato come Archiviato (codice 18) da questo cursore in esecuzione allora viene rimossa una eventuale classificazione dei cursori precedenti. | E’ stato rilasciato uno script:
20211102019.sql
in cui viene modificato il Package Body “ISPETTORATO_MS”. |  |
| 202111150114 | Centro di Competenza Sistemi Area Penale | L’ufficio segnala che il sistema non visualizza l’ordinanza di estinzione della sanzione sostitutiva e di conseguenza non permette di definire il procedimento. | Per la risoluzione della problematica si è proceduto con l’inserimento nella tabella CG_REF_CODES del record avente RV_DOMAIN = 'INSERIMENTO_SS' e RV_VALUE='U063', che consente all'applicazione di creare la struttura dati per l'aggancio del provvedimento della Sorveglianza da parte della funzione SIEP “Definizione Procedimento" presente nel menu di Gestione delle Conversione Pene Pecuniarie. | E’ stato rilasciato uno script:
202111150114.sql
che inserisce un record nella tabella ‘CG_REF_CODES’ e dominio 'INSERIMENTO_SS' e valore 'U063'. |  |
| 20211116019 | Centro di Competenza Sistemi Area Penale | L’ufficio segnala che il sistema non estrae i dati selezionando la funzione Statistica. | Per la risoluzione della problematica si è intervenuti gestendo il passaggio di informazioni ad Oracle in quanto i campi "chiave_ufficio" e "MAG_COD_MAGISTRATO" venivano trattati come "number" quando in realtà sono stati dichiarati come "varchar" | Classi modificate:
src.siap.sige.fascicolo.controller.FascicoloSigeController.java
src.siap.sige.fascicolo.dao.FascicoloSigeSqlDAO.java
dove un paio di campi dichiarati come “stringhe” in oracle erano invece inviati dall’applicativo come “interi”. Per esempio: chiave_ufficio = 123456 piuttosto che ‘123456’. |  |
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
Aggiornamento tabella “CG_REF_CODES”, dominio “INSERIMENTO_SS”
Aggiornamento Package Body “ISPETTORATO_MS” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| template.zip | Template | Template aggiornati:
SIGE_OR_MODGENERICO.rtf
SIEP_CUMULO_OE_656_DET.rtf
NoteDiTrasmissione.rtf |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20211126-Piano_di_Rilascio_SIES_v.12.4.15.0.docx
SIUT-SIES-PT-1.0-20211126-Piano_dei_Test_SIES_v.12.4.15.0.docx
SIUT-SIES-CT-1.0-20211126-Allegato_al_piano_test_SIES_v.12.4.15.0.xls |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.14.0.
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
Creare sul server DB una cartella V_12_4_15_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_4_15_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_15_0 tramite il comando:
chmod 777 V_12_4_15_0

In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx

Nella cartella appena creata (V_12_4_15_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_4_15_0/log/ in cui si può constatare l’esito dell’esecuzione.

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
Copiare i files contenuti nella cartella template\sige\or
nella cartella “/var/SIES/template/sige/or” sovrascrivendo quelli precedenti;
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