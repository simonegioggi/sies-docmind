---
uniqueName: siut-sies-pr-1-0-20200731-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20200731 Piano di Rilascio SIES v 12 4 1"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20200731-Piano_di_Rilascio_SIES_v.12.4.1

> **File originale:** `RILASCIO_12.4.1.0/SIUT-SIES-PR-1.0-20200731-Piano_di_Rilascio_SIES_v.12.4.1.docx`  
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
| Data approvazione | 31/07/2020 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 31/07/2020 | Prima Emissione |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Pasquale Lamattina | RTI |  | Referente Tecnico |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Fabio Mazzocchi | RTI |  | Responsabile Manutenzione Correttiva |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Responsabile PMO |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Edoardo Lamuraglia | RTI |  | Referente qualità |
| Francesco Rosati | RTI |  | Referente qualità |
| Andrea Castorino
Alessandro Lanari | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |
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
4.1	Riferimenti Anomalia (MAC)	8
4.2	Riferimenti ChangeRequest (ADE/MEV)	12
4.2.1	Documenti a corredo della sessione di verifica conformità	12
5	Dettaglio degli elementi oggetto del rilascio	14
6	Installazione	15
6.1	Prerequisiti	15
6.2	Attività di preinstallazione	15
6.3	Attività di installazione	15
6.3.1	Installazione lato DB	15
6.3.1.1	Esecuzione script	15
6.3.2	Installazione applicazione	16
6.3.2.1	Deploy Applicazione	16
6.4	Attività di configurazione	17
6.5	Attività di post-installazione	17


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio del sistema SIES.
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.1 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.4.1 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.

Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.
# Identificazione degli elementi rilasciati
| Supporto | Oggetti: | Ver. | del |
| --- | --- | --- | --- |
| Portale fornitura | Rilascio SIES | 12.4.1 | 31/07/2020 |
| Note-osservazioni |  |  |  |


# Riferimenti degli oggetti del rilascio
## Riferimenti Anomalia (MAC)
| Rif. Ticket OTRS | Sede
Ufficio | Descrizione segnalazione | Descrizione
intervento | Descrizione Tecnica | Manuali corretti |
| --- | --- | --- | --- | --- | --- |
| 20200508015 | Procura della Repubblica presso il Tribunale di Palermo | L’utente segnala che il sistema in fase di stampa di un provvedimento di "Comunicazione Rideterminazione della pena a seguito di ordinanza ex. art. 671 c.p.p. e art 81 c.p." restituisce un errore java. | Per la risoluzione della problematica si è intervenuti sulla rettifica di una import sul template SIEP_RP_OSRDP.rtf. | Aggiornato il template SIEP_RP_OSRDP.rtf. |  |
| 20200525013 | Segnalato dall’Amministrazione | Per i template SIEP_MS_ARCH_GE" e "SIEP_MS_ARCH_GIU_CAS, si segnala la mancanza di un testo giustificato dopo la dicitura ‘COMUNICA’; Inoltre si segnala la presenza della dicitura ‘per la durata’ anche in assenza di una quantificazione di durata per le misure di sicurezza. Nella sezione ‘MANDA’ dei template specificati è presente la dicitura ‘ e all’esecuzione’ che non deve essere presente. | Si è proceduto alla ‘giustificazione’ del testo dopo la dicitura ‘COMUNICA’. Inoltre è stata eliminata la dicitura ’durata’ per le misure di sicurezza se non quantificata. Infine è stata eliminata la dicitura "e all'esecuzione" nella sezione "MANDA". | I template SIEP_MS_ARCH_GE" e "SIEP_MS_ARCH_GIU_CAS sono stati rettificati secondo quanto specificato alla descrizione dell’intervento. |  |
| 20200525014 | Procura della Repubblica presso il Tribunale di Perugia | L’utente segnala che il sistema in fase di stampa di un provvedimento di "Cumulo Pene”, restituisce un errore java. | Per la correzione dell’anomalia segnalata si è intervenuti nel modulo java per gestire l’eccezione nelle casistiche in cui la proprietà ‘flag_piu_meno’ non sia valorizzata. | La correzione ha coinvolto la classe StampaCumuloController.java nel metodo ‘appendStatoEsecuzioneTitoloCum’. |  |
| 20200525017 | Segnalato dall’Amministrazione | Si segnala che il sistema, a seguito di archiviazione manuale di un procedimento ‘Trasmesso per Assorbimento in Cumulo’ non elimina la dicitura prevista per il cumulo: ‘Procedimento trasmesso per assorbimento in cumulo…..’ . | Nella pagina di dettaglio del procedimento, è stata eliminata la dicitura prevista per il cumulo "Procedimento trasmesso per assorbimento in cumulo ..." a seguito di archiviazione manuale del procedimento. | La correzione ha coinvolto il file "DettaglioSoggettoSentenzaCompleto.jsp”. |  |
| 20200528012 | Corte D’Appello di Bolzano | Per il sottosistema SIGE, l’utente segnala che in fase di inserimento parte civile/offesa, nella pagina relativa all'emissione dell’ordinanza, al momento della conferma il sistema prospetta un messaggio di errore java. | In fase di inserimento di una ordinanza è stato inserito un messaggio che avverte l’utente che l’inserimento della parte civile e/o offesa deve essere effettuata a valle dell'inserimento del decreto di fissazione udienza. | La correzione ha coinvolto la classe ActInserisciParteUdienza.java. |  |
| 202007060112 | Procura della Repubblica presso il Tribunale di Torino | L’ufficio segnala che pur inserendo i dati dell'ordinanza del Tribunale di sorveglianza che ha dichiarato NLP sull'istanza di misura alternativa, nel provvedimento elaborato risulta come motivazione della revoca del Decreto di Sospensione, il non aver presentato istanza nei termini. | Il template SIEP_RS_DACNI_M.rtf è stato rettificato in modo che visualizzi correttamente i dati dell’ordinanza di revoca. | Aggiornato il template SIEP_RS_DACNI_M.rtf |  |
| 202007070114 | Procura presso il Tribunale dei Minorenni di Bari | L’utente segnala l’assenza d un   procedimento con una scadenza pena definita, nello scadenziario di fine pena. | Corretto modulo di validazione della Comunicazione Concessione Detenzione Domiciliare ex art.47 ter O.P. Non inseriva/aggiornava lo scadenzario fine pena. | La correzione ha coinvolto la classe siap.sico.misuraalternativa.controller.MisuraAlternativaController |  |
| 20200708017 | Segnalato dall’Amministrazione | Per il sottosistema SIUS, si segnala che in fase di cancellazione di una ordinanza validata e depositata, il sistema fornisce un messaggio ‘bloccante’ e non attinente alla funzione. | Per la correzione dell’anomalia segnalata si è intervenuti sulla costruzione di una query più specifica andando ad aggiungere una ‘and condition’ sull’idEvento coinvolto. | La correzione ha coinvolto la classe siap.sico.evento.dao.EventoSqlDAO.java |  |
| 20200709011 | Ufficio di Sorveglianza di Agrigento | L’utente segnala che in fase di stampa della lettera di trasmissione atti, se viene
utilizzata la funzione "notifica tramite SNT", nella lettera di trasmissione atti creata, viene inserito due volte come destinatario la dicitura "notifica tramite SNT" | Nel template SIUS_DE_DEPOSITODECRETO.rtf è stato gestito il codice ‘C1’ e ‘C0’ così come previsto per codice ‘22’ (UNEP). | Aggiornato il template SIUS_DE_DEPOSITODECRETO.rtf secondo quanto specificato in ‘descrizione intervento’. |  |
| 20200710012 | Procura Generale presso la Corte d’Appello di Palermo | L’utente segnala che nel template generato in corrispondenza di un Ordine di Scarcerazione a seguito liberazione anticipata per i detenuti, nella parte in cui sono indicati i destinatari, l’elenco non è correttamente allineato. | Nel template SIEP_OS_LIBAN.rtf è stato correttamente allineato l’elenco dei destinatari. | Aggiornato il template SIEP_OS_LIBAN.rtf secondo quanto specificato in ‘descrizione intervento’. |  |
| 20200715012 | Procura della Repubblica presso il Tribunale di Torino | L’utente segnala che in fase di stampa dei prospetti di cumulo, nel caso in cui si provvede ad inserire manualmente un titolo esecutivo caratterizzato dall’assenza di una pena principale, il sistema restituisce un errore java. | Aggiunto controllo in fase di stampa per gestire l'assenza della Pena Principale in presenza delle richieste revoca Sospensione Condizionale. | La correzione ha coinvolto la classe siap.siep.istruttoriacumulo.controller.StampaCumuloController.java |  |
| 20200715013 | Procura della Repubblica presso il Tribunale di Torino | L'Ufficio segnala che il sistema non visualizza le autorità destinatarie per la trasmissione atti. | Per la correzione dell’anomalia segnalata si è intervenuti per popolare le combo interessate. | La correzione ha coinvolto la classe ActLoadInserisciTrasmissione.java |  |
| 20200715018 | Procura della Repubblica presso il Tribunale di Torino | L’utente segnala un’anomalia del calcolo dei periodi di custodia cautelare continuativi. | Per la correzione dell’anomalia segnalata si è intervenuti per gestire il giusto calcolo in caso di 2 gruppi distinti ma adiacenti di Misure Cautelari in continuazione. | La correzione ha coinvolto la classe ActRicercaMisuraCautelare.java e l’aggiornamento del template MisuraCautelare.rtf |  |
| 20200720013 | Procura della Repubblica presso il Tribunale di Bolzano | L’utente segnala che nell’utilizzare la funzione di "Registrazione provvedimento decorrenza scadenza" il programma non produce la stampa del template, ma resta bloccato sulla pagina. | Per la correzione dell’anomalia segnalata si è intervenuto con la gestione del codice 0610 del TDS alla stessa stregua del codice 2630 dell'UDS. | La correzione ha coinvolto i file DettaglioPenaResiduaVerbaleSottoscrizione.jsp e RegistraPenaVerbaleSottoscrizione.jsp ed i template SIEP_MA_ESECDOM_DECSCA.rtf e SIEP_MA_ESECDOM_LIB.rtf |  |
| 20200721012 | Procura della Repubblica presso il Tribunale di Spoleto | L'Ufficio segnala che il sistema non visualizza le autorità destinatarie per la trasmissione atti nella funzione Trasmissione atti/richieste ex art. 51 bis. | Per la correzione dell’anomalia segnalata si è intervenuti per popolare le combo interessate. | La correzione ha coinvolto la classe ActLoadInserisciTrasmissione.java |  |
| 20200723012 | Procura della Repubblica presso il Tribunale dei minorenni di Milano | L’utente segnala che a seguito di emissione di provvedimento di cumulo di pene con sospensione per ex 656, tale provvedimento non appare nello scadenziario L. 165/98. | L’intervento di correzione consiste nell’adeguamento del trigger già esistente CANCELLA_SCADENZIARIO.sql alla casistica di emissione cumulo con sospensione per ex 656. | Aggiornamento del  trigger CANCELLA_SCADENZIARIO.sql |  |


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
Trigger per gestione della cancellazione di alcuni eventi da scadenziario
Aggiornamento versione SIES |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| template.zip | Template | Template aggiornati:
SIEP_MS_ARCH_GE.rtf
SIEP_MS_ARCH_GIU_CAS.rtf
SIEP_RP_OSRDP.rtf
SIUS_DE_DEPOSITODECRETO.rtf
SIEP_OS_LIBAN.rtf
SIEP_RS_DACNI_M.rtf
MisuraCautelare.rtf
SIEP_MA_ESECDOM_DECSCA.rtf
SIEP_MA_ESECDOM_LIB.rtf |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20200731-Piano_di_Rilascio_SIES_v.12.4.1.docx 
SIUT-SIES-PT-1.0-20200731-Piano_dei_Test_SIES_v.12.4.1.docx
SIUT-SIES-CT-1.0-20200731-Allegato_al_piano_test_SIES_v.12.4.1.xlsx |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.0.
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
Creare sul server DB una cartella V_12_4_1 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/ V_12_4_1/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_1 tramite il comando:
chmod 777 V_12_4_1

In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx

Nella cartella appena creata (V_12_4_1), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/ V_12_4_1/log/ in cui si può constatare l’esito dell’esecuzione.

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

Copiare i file contenuti nella cartella template\import
nella cartella “/var/SIES/template/import” sovrascrivendo quelli precedenti;
Copiare i file contenuti nella cartella template\siep\ms nella cartella “/var/SIES/template/siep/ms” sovrascrivendo quelli precedente;
Copiare il file contenuto nella cartella template\siep\rp nella cartella “/var/SIES/template/siep/rp” sovrascrivendo quello precedente;
Copiare il file contenuto nella cartella template\sius\de nella cartella “/var/SIES/template/sius/de” sovrascrivendo quello precedente;
Copiare il file contenuto nella cartella template\siep\os nella cartella “/var/SIES/template/siep/os” sovrascrivendo quello precedente;
Copiare i file contenuti nella cartella template\siep\ma nella cartella “/var/SIES/template/siep/ma” sovrascrivendo quelli precedente;
Copiare il file contenuto nella cartella template\siep\rs nella cartella “/var/SIES/template/siep/rs” sovrascrivendo quello precedente;

Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 2.b e 2.e. All’avvio, infatti, tali cartelle verranno ricreate.

Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.

## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.