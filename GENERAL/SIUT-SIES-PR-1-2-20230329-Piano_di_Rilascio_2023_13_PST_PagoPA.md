---
uniqueName: siut-sies-pr-1-2-20230329-pianodirilascio202313pst
displayName: "SIUT SIES PR 1 2 20230329 Piano di Rilascio 2023 13 PST PagoPA"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.2-20230329-Piano_di_Rilascio_2023_13_PST_PagoPA

> **File originale:** `MEV/SCHEDA_013/SIUT-SIES-PR-1.2-20230329-Piano_di_Rilascio_2023_13_PST_PagoPA.docx`  
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
| Data approvazione | 29/03/2023 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 24/03/2023 | Prima Emissione |  |
| 1.1 | 28/03/2023 | Seconda Emissione | Aggiunto un documento nel rilascio e modificato il paragrafo Generalità |
| 1.2 | 29/03/2023 | Terza Emissione | Modificato il paragrafo Generalità ed il paragrafo Deploy Applicazione (nella parte riguardante il file f3b.properties) |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Aurora Garofalo | Amministrazione |  | Responsabile Unico Procedimento |
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
1.	Introduzione	5
1.1	Scopo del documento	5
1.2	Riferimenti	5
1.3	Glossario	5
1.3.1	Definizioni	5
1.3.2	Acronimi e abbreviazioni	5
2.	Generalità	6
3.	Identificazione degli elementi rilasciati	7
4.	Riferimenti degli oggetti del rilascio	8
4.1	Riferimenti Anomalia (MAC/GAR)	8
4.2	Riferimenti ChangeRequest (ADE/MEV)	8
5.	Dettaglio degli elementi oggetto del rilascio	9
6.	Installazione	10
6.1	Prerequisiti	10
6.2	Attività di preinstallazione	10
6.3	Attività di installazione	10
6.3.1	Installazione lato DB	10
6.3.1.1	Esecuzione script	10
6.3.2	Installazione applicazione	11
6.3.2.1	Deploy Applicazione	11
6.4	Attività di configurazione	13
6.5	Attività di post-installazione	13


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio degli interventi realizzati nell’ambito del Sistema Integrato Esecuzione Sorveglianza per la realizzazione di quanto dettagliato nella scheda di intervento di riferimento.
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.27.0-MEV_2023_13 di SIES.
Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio.
## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF1. | SIUT-SCCL-SC-1.2-20230327-Scheda_Intervento_2023_13_PST_PagoPA.pdf | Scheda Intervento |

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
Il presente documento descrive il piano di rilascio del software relativo alla MEV_2023_13 di SIES, contenente l’integrazione della suddetta MEV con la versione SIES 12.4.27.0.

Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.

Sono stati creati due nuovi file di log reperibili sotto il percorso “/opt/jboss-eap-6.4/standalone/log/sies”:
PagoPaBatch.log;
WSPagoPa.log.
Il primo recepisce tutte le informazioni di debug circa l’esecuzione del batch di verifica stato pagamento (ovvero si occupa, con cadenza giornaliera, di interrogare il servizio “elencoPagamenti” per conoscere lo stato di un certo pagamento (IUV)).
Il secondo recepisce tutte le informazioni di debug delle funzionalità attive nel percorso “Gestione Altre Sanzioni >> Pene Pecuniarie / Pene Sostitutive Brevi”, selezionando uno dei due tabulatori “Riscossione Pene Pecuniarie” oppure “Esecuzione Pene Sostitutive Brevi”.

In caso di errore durante la navigazione delle nuove funzionalità oppure nell’interrogazione dei Web Services sarà possibile consultare i file di log sopra citati o le tabelle di log (tra cui per il batch abbiamo introdotto le colonne “ESITO_ESECUZIONE” ed “ERRORE_ESECUZIONE” nella tabella “BATCH_PAGOPA”) e aprire i ticket secondo i consueti canali dell'amministrazione.

# Identificazione degli elementi rilasciati
| Supporto | Oggetti: | Ver. | Del |
| --- | --- | --- | --- |
| Portale fornitura | SIUT > 07 - MEV > Scheda 2023_13 - PagoPa > 05_Verifica di Conformita' |  |  |
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
| - | SIUT-SCCL-SC-1.2-20230327-Scheda_Intervento_2023_13_PST_PagoPA | - | Integrazione del SIES con PST_PagoPA |

# Dettaglio degli elementi oggetto del rilascio
| Nome File | Path | Motivazione-riferimento |
| --- | --- | --- |
| aggiorna_db.zip | Database | Script per aggiornamento base dati: 
Aggiornamento, inserimento e alterazione in varie tabelle
Aggiornamento versione SIES in tabella “VERSIONE” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.2-20230329-Piano_di_Rilascio_2023_13_PST_PagoPA.pdf
SIUT-SIE-CT-1.0-20230327-Allegato_al_piano_test_2023_13_PST_PagoPA.xlsx
SIUT-SIE-PT-1.0-20230327-Piano_dei_Test_2023_13_PST_PagoPA.pdf
SIUT-SIE-MU-1.0-20230327-Manuale_Utente_2023_13_PST_PagoPA.pdf
SIUT_SIES_ML_20230324_1.8_Modello_dei_Dati_2023_13_PST_PagoPA.pdf |
| Template.zip | Template | NotificaDestinatarioAvvEveCorrente.rtf
PenaComplessivaSoloPecuniaria.rtf
Soggetto.rtf
Variabili.rtf
SIEP_PP_OI_PAGAMENTO_RR.rtf
SIEP_PP_OI_PAGAMENTO_UN.rtf |
| log.zip | Sorgenti | logback.xml |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.27.0.
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
Creare sul server DB una cartella MEV_2023_13 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/MEV_2023_13/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella MEV_2023_13 tramite il comando:
chmod 777 MEV_2023_13
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES...........: siesxx	(dove xx è la sigla del distretto di appartenenza, per esempio: rm per Roma)
Password_SIES.......: siesxx
Nella cartella appena creata (MEV_2023_13), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/MEV_2023_13/log/ in cui si può constatare l’esito dell’esecuzione.
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
Posizionarsi sotto la cartella:
“/var/SIES/CONFIG”;
Editare il file “f3b.properties” ed aggiungere alla fine del file le seguenti righe:
#MEV_2023_13: Endpoint Address PagoPA
EAPPA_SIPT=https://servizibe.processotelematico.giustizia.it/servizi/ServiziInvioPagamentiTelematici
EAPPA_SCPT=https://servizibe.processotelematico.giustizia.it/servizi/ServiziConsultazionePagamentiTelematici
#true: batch attivo; false: batch spento
PagoPaSchedulerEnabled=true
PagoPaCronExpression=0 0 0 * * ?
# parametri per esecuzione Batch
CONTROLLATEDAGIORNI=0
INSCADENZATRAGIORNI=3
#FINE MEV_2023-13
inScadenzaTraGiorni indica il numero di giorni che determinerà l’intervallo di tempo da considerare per selezionare i bollettini da verificare. La condizione è la seguente:
data_scadenza between sysdate - inScadenzaTraGiorni and sysdate + inScadenzaTraGiorni
Se, quindi, il valore di inScadenzaTraGiorni è uguale a 3, si prenderanno in considerazione tutti i bollettini che sono scaduti da tre giorni o che scadranno tra tre giorni.
Il valore iniziale sarà settato per default a 3.
controllateDaGiorni indica che ogni volta che il batch viene eseguito, aggiorna per ogni bollettino elaborato, il campo “DATA_ULTIMO_CONTROLLO” nella tabella “BOLLETTINO_PAGOPA”. Se il valore di controllateDaGiorni è diverso da zero, il batch prende in considerazione tutti i bollettini che hanno “DATA_ULTIMO_CONTROLLO< SYSDATE-controllateDaGiorni“ di modo da elaborare solo i bollettini che NON sono stati controllati negli ultimi n giorni, di modo da non appesantire le richieste verso PagoPA.
Il valore iniziale sarà settato per default a 0.

Di seguito alcuni esempi per configurare la stringa “PagoPaCronExpression”:

Posizionarsi sotto la cartella:
“/var/SIES/CONFIG/certs”;
Proseguire con l’aggiornamento del file trustStore “sies.jks”, importando, con procedura nota
all’Amministrazione, la catena di certificati ed il certificato necessari al colloquio con la macchina server
che espone il servizio web.
NB: i certificati da importare devono essere resi disponibili dai referenti del sistema PST_PagoPA e correlati all’ambiente predisposto per la verifica di conformità.
Scaricare il file “logback.xml”, contenuto nell’archivio “log.zip”, sul server SIES ed eseguire le seguenti operazioni:
posizionarsi sotto la cartella:
“/opt/jboss-eap-6.4/modules/config/log/main”;
copiare, nello stesso percorso, il nuovo file “logback.xml” sovrascrivendo quello precedente;
Scaricare il file “sies.war” sul server SIES ed eseguire le seguenti operazioni:
posizionarsi sotto la cartella:
“/opt/jboss-eap-6.4/standalone/deployments”;
cancellare il vecchio eseguibile (se esistente) “sies.war” e la copia deployata “sies.war.deployed”;
copiare, nello stesso percorso, il nuovo eseguibile “sies.war”;
posizionarsi sotto la cartella:
“/opt/jboss-eap-6.4/standalone”;
cancellare le cartelle “data”, “log” e “tmp” (se esistenti);
Copiare i files contenuti nella cartella template\import
nella cartella “/var/SIES/template/import” sovrascrivendo quelli precedenti;
Copiare i files contenuti nella cartella template\siep\pp
nella nuova cartella “/var/SIES/template/siep/pp”, da creare tramite i seguenti comandi:
cd /var/SIES/template/siep
mkdir pp
chmod 777 pp
Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 7.b e 7.e. All’avvio, infatti, tali cartelle verranno ricreate.
Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.