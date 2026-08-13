---
uniqueName: siut-sies-pr-1-0-20210924-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20210924 Piano di Rilascio SIES v 12 4 13 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20210924-Piano_di_Rilascio_SIES_v.12.4.13.0

> **File originale:** `RILASCIO_12.4.13.0/SIUT-SIES-PR-1.0-20210924-Piano_di_Rilascio_SIES_v.12.4.13.0.docx`  
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
| Data approvazione | 24/09/2021 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 24/09/2021 | Prima Emissione |  |


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
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.13.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.4.13.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.
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
| 20210702015 | Procura della Repubblica Presso il Tribunale di Torino | L’ufficio segnala un errore nella visualizzazione del provvedimento di cumulo su procedimento  trasferito da altro Distretto. | Per la risoluzione della problematica si è intervenuti con la correzione del fatto che il tipo di ricerca non trasferisce tutti i dati del fascicolo tra cui i dati dell'istruttoria cumulo. | Corretto il modulo per comportarsi come le altre funzioni di trasferimento.
Classi corrette:
siap.siep.jms.controller.RicercaJMSController.java (metodo ExRicercaFascicoloSiepPerTrasferimento) |  |
| 20210716016 | Procura della Repubblica presso il Tribunale di Torino | L’ufficio segnala che il sistema non aggiorna la misura di sicurezza e di conseguenza  elabora il documento di stampa (SIEP_MS_COMUESP_DET.rtf) errato. | Per la risoluzione della problematica si è intervenuti con il rilascio di uno script per il database. | E’ stato rilasciato il file “20210621016.sql” che consente di colmare a lacuna che nella tabella CG_REF_CODES, dominio “esito_provvedimento” con RV_LOW_VALUE = '0181', mancava la valorizzazione della colonna RV_ALT2_VALUE ad 'MSI', in base alla quale la funzione di Annotazione Decisione della Sorveglianza procede a rendere non valida su SIEP la misura presente e ad inserire la nuova misura applicata dalla Sorveglianza. |  |
| 20210721013 | Procura della Repubblica presso il Tribunale di Torino | L'Ufficio richiede la correzione del Template SIEP_LS_OLQSI. La correzione riguarda la notifica al difensore. | Per la risoluzione della problematica si è intervenuti con il rilascio dei templates opportunamente modificati. | Sono stati rilasciati i documenti:
“NotificaDestinatarioAvvEveCorrente.rtf”
“TestoNotificaExArt148EveCorrente.rtf”
“SIEP_LS_OLQSI.rtf”
Modificati secondo le indicazioni contenute nella segnalazione (eliminazione spazi, testo giustificato, eliminazione frase ripetuta, revisione punti elenco e punteggiatura). |  |
| 202107210117 | N.N. | L’ufficio segnala che nella maschera per la trasmissione della richiesta prosecuzione misura alternativa, pur selezionando correttamente la voce "MAGISTRATO DI SORVEGLIANZA PER I MINORENNI", in fase di stampa il provvedimento riporta la dicitura generica "preposto alla vigilanza", ragion per cui nel confermare l'invio telematico, il sistema rileva ovviamente "ufficio inesistente" senza provvedere alla trasmissione degli atti. | Per la risoluzione della problematica si è intervenuti con la aggiunta della gestione del trasferimento del fascicolo agli uffici minorili sia lato codice che lato documentale. | E’ stato rilasciato il documento:
“SIEP_MA_TRASF_ATTI_51BIS.rtf”
Sono state modificate le classi:
siap.siep.richiesta.actionActLoadTrasferisciRichiestaAttiExArt51Bis.java
siap\siep\richiesta\LoadTrasmissioneAttiExArt51Bis.jsp
in cui sono stati aggiunti controlli per gli uffici minorili e parametrizzate alcune diciture fisse (ovvero sostituite alcune costanti con delle variabili per gestire la comunicazione anche agli uffici dei minorenni). |  |
| 20210728014 | Corte d'Appello di Catania | L’ufficio segnala che non riesce a modificare una udienza collegiale anche se il magistrato è membro del collegio, ed aggiunge che il magistrato in oggetto è stato da poco assegnato alla seconda sezione, prima era in un altra sezione dello stesso ufficio. | Per la risoluzione della problematica si è intervenuti con la correzione della gestione del collegio e della sezione di una udienza collegiale. | Corretta la classe:
siap\sige\udienzacollegiale\LoadInserisciUdienzaCollegialeFix.jsp
poiché era presente un errore Javascript  che non permetteva di recuperare correttamente “id_collegio” e “id_sezione”. |  |
| 20210824013 | Procura Generale presso la Corte d’Appello di Catanzaro | L’ufficio segnala un errore nell'emissione del cumulo. | Per la risoluzione della problematica si è intervenuti con la correzione del problema legato alla presenza di una richiesta di Revoca Beneficio su evento in cui è assente il numero di provvedimento. | Corretta la classe:
siap.siep.istruttoriacumulo.controller.StampaCumuloController.java
in cui è stato aggiunto un controllo di consistenza del dato poiché si eseguiva una istruzione su una variabile che poteva essere nulla. |  |
| 20210825016 | N.N. | L’ufficio segnala che in un procedimento non si riesce ad inviare tramite il registro informatizzato SIEP l’annotazione provvisoria dell’estratto. In pratica nel trasferimento del provvedimento da Sies ad Nsc il sistema restituisce il messaggio: “Il Procedimento N:2020/233 Non è stato trasferito”. Ciò non accade sempre, nella fattispecie trattasi di un provvedimento di Ordine Esecuzione  con contestuale Sospensione - Libero che in ultima pagina genera l'estratto del foglio complementare con notizie relative alla sospensione dell'esecuzione della pena (sentenza). | Per la risoluzione della problematica si è intervenuti con la correzione della classe deputata a raccogliere i dati che devono essere inviati provvisoriamente ad NSC. | E’ stata modificata la classe:
siap.sico.webservice.action.ActPrelevaDatiFascicolo.java
in cui accadeva che l'invio di una sentenza con una impugnazione di primo grado di inammissibilità non era consentita poiché il codice univoco della suddetta impugnazione non era mappato nella tabella DC_TAB7a_RIFERIMENTI proprietaria di NSC.
Per risolvere la problematica siamo intervenuti nel codice java di SIES e nella banca dati di NSC dove abbiamo mappato l'impugnazione 022 - DICHIARA INAMMISSIBILE L'APPELLO CON ORDINANZA EMESSA
col nuovo codice univoco (17) che viene inviato da SIEP.
Quindi, per un corretto funzionamento dell'invio del provvedimento provvisorio, deve essere previsto contemporaneamente al rilascio della nuova versione del SIES (12.4.13.0) anche il rilascio dello script DB per l'applicazione SIC-NSC (per cui è stato aperto il: Ticket#20210831011 - Ticket#20210825016 - foglio completare Iscrizione nel casellario giudiziale locale - ex art. 3 DPR 14 novembre 2002 n. 313 -). |  |
| 20210907019 | Procura della Repubblica Presso il Tribunale di Torino | L’ufficio segnala una diversa impostazione per l’elenco misure sicurezza. | Per la risoluzione della problematica si è intervenuti con il rilascio del template opportunamente modificato. | E’ stato rilasciato il documento “EsecuzioneMisuraSicurezza.rtf” in cui sono state apportate le correzioni secondo le indicazioni contenute nell’allegato alla segnalazione (rivisto elenco Misure Sicurezza, inserendo il ritorno a capo per ciascuna misura, ed eliminati spazi superflui). |  |
| 20210916011 | Procura della Repubblica Presso il Tribunale per i Minorenni di Torino | L’ufficio richiede la correzione del template in oggetto con Variabile CSSA:
all’U.E.P.E. (Ufficio Esecuzione Penale Esterna) competente;
all’U.S.S.M. (Ufficio Servizi Sociali per i minorenni) competente. | Per la risoluzione della problematica si è intervenuti con il rilascio del template opportunamente modificato. | E’ stato rilasciato il documento “SIEP_OS_LARAL.rtf” in cui è stata inserita la gestione dell’Ufficio Servizi Sociali per i Minorenni competente. |  |
| 20210916015 | Procura della Repubblica Presso il Tribunale di Torino | L’ufficio segnala che il template in oggetto non  riporta l'indirizzo completo del destinatario. | Per la risoluzione della problematica si è intervenuti con il rilascio del template opportunamente modificato. | E’ stato rilasciato il documento “SIEP_RICH_GENERICA.rtf” in cui sono state apportate le correzioni secondo le indicazioni contenute nell’allegato alla segnalazione (aggiunto l'indirizzo nella stampa). |  |
| Note-osservazioni | Il ticket 20210825016 per la corretta esecuzione è strettamente legato al ticket 20210831011 dell’applicativo SIC-NSC. Se contestualmente alla installazione della release 12.4.13.0 di SIES non verrà eseguito lo script di aggiornamento dati dell’applicativo NSC, il sistema restituirà lo stesso errore segnalato dall’utente nell’apertura del ticket. | Il ticket 20210825016 per la corretta esecuzione è strettamente legato al ticket 20210831011 dell’applicativo SIC-NSC. Se contestualmente alla installazione della release 12.4.13.0 di SIES non verrà eseguito lo script di aggiornamento dati dell’applicativo NSC, il sistema restituirà lo stesso errore segnalato dall’utente nell’apertura del ticket. | Il ticket 20210825016 per la corretta esecuzione è strettamente legato al ticket 20210831011 dell’applicativo SIC-NSC. Se contestualmente alla installazione della release 12.4.13.0 di SIES non verrà eseguito lo script di aggiornamento dati dell’applicativo NSC, il sistema restituirà lo stesso errore segnalato dall’utente nell’apertura del ticket. | Il ticket 20210825016 per la corretta esecuzione è strettamente legato al ticket 20210831011 dell’applicativo SIC-NSC. Se contestualmente alla installazione della release 12.4.13.0 di SIES non verrà eseguito lo script di aggiornamento dati dell’applicativo NSC, il sistema restituirà lo stesso errore segnalato dall’utente nell’apertura del ticket. | Il ticket 20210825016 per la corretta esecuzione è strettamente legato al ticket 20210831011 dell’applicativo SIC-NSC. Se contestualmente alla installazione della release 12.4.13.0 di SIES non verrà eseguito lo script di aggiornamento dati dell’applicativo NSC, il sistema restituirà lo stesso errore segnalato dall’utente nell’apertura del ticket. |

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
Aggiornamento tabella “CG_REF_CODES” dominio “ESITO_PROVVEDIMENTO” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| template.zip | Template | Template aggiornati:
EsecuzioneMisuraSicurezza.rtf
NotificaDestinatarioAvvEveCorrente.rtf
TestoNotificaExArt148EveCorrente.rtf
SIEP_LS_OLQSI.rtf
SIEP_MA_TRASF_ATTI_51BIS.rtf
SIEP_OS_LARAL.rtf
SIEP_RICH_GENERICA.rtf |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20210924-Piano_di_Rilascio_SIES_v.12.4.13.0.docx
SIUT-SIES-PT-1.0-20210924-Piano_dei_Test_SIES_v.12.4.13.0.docx
SIUT-SIES-CT-1.0-20210924-Allegato_al_piano_test_SIES_v.12.4.13.0.xls |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.12.0.
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
Creare sul server DB una cartella V_12_4_13_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_4_13_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_13_0 tramite il comando:
chmod 777 V_12_4_13_0

In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx

Nella cartella appena creata (V_12_4_13_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_4_13_0/log/ in cui si può constatare l’esito dell’esecuzione.

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
Copiare i files contenuti nella cartella template\import
nella cartella “/var/SIES/template/import” sovrascrivendo quelli precedenti;
Copiare i files contenuti nella cartella template\siep\ls
nella cartella “/var/SIES/template/siep/ls” sovrascrivendo quelli precedenti;
Copiare i files contenuti nella cartella template\siep\ma
nella cartella “/var/SIES/template/siep/ma” sovrascrivendo quelli precedenti;
Copiare i files contenuti nella cartella template\siep\os
nella cartella “/var/SIES/template/siep/os” sovrascrivendo quelli precedenti;
Copiare i files contenuti nella cartella template\siep\rich
nella cartella “/var/SIES/template/siep/rich” sovrascrivendo quelli precedenti;

Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 2.b e 2.e. All’avvio, infatti, tali cartelle verranno ricreate.

Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.