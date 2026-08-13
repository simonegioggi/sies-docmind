---
uniqueName: siut-sies-pr-1-0-20230922-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20230922 Piano di Rilascio SIES v 12 5 3 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20230922-Piano_di_Rilascio_SIES_v.12.5.3.0

> **File originale:** `RILASCIO_12.5.3.0/SIUT-SIES-PR-1.0-20230922-Piano_di_Rilascio_SIES_v.12.5.3.0.docx`  
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
| Data approvazione | 22/09/2023 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 22/09/2023 | Prima Emissione |  |


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
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.5.3.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.5.3.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.
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
| 202107150110 | N.C. | L’ufficio segnala la mancata trascrizione del quantitativo di pena fungibile nei template indicati. | Per la risoluzione della problematica è stata modificata la dicitura all'interno dei template da
"Fungibilita/Periodo" a "Evento[EventoCorrente=&apos;S&apos;]/Fungibilita/StringaFungibilita". | Il problema era legato al fatto che la variabile riguardante il periodo della fungibilità pena era mal riportato nel codice del template.
Template modificati:
siep\am\SIEP_AM_COMPU657_1.rtf
siep\am\SIEP_AM_COMPU657_2.rtf
siep\am\SIEP_AM_COMPU657_MIS.rtf |  |
| 202107150111 | N.C. | L’ufficio segnala la mancata trascrizione del quantitativo di pena fungibile nei template indicati. | Per la risoluzione della problematica è stata modificata la dicitura all'interno dei template da
"Fungibilita/Periodo" a "Evento[EventoCorrente=&apos;S&apos;]/Fungibilita/StringaFungibilita". | Il problema era legato al fatto che la variabile riguardante il periodo della fungibilità pena era mal riportato nel codice del template.
Template modificati:
siep\am\SIEP_AM_COMPU657_1.rtf
siep\am\SIEP_AM_COMPU657_2.rtf
siep\am\SIEP_AM_COMPU657_MIS.rtf |  |
| 202107150112 | N.C. | L’ufficio segnala la mancata trascrizione del quantitativo di pena fungibile nei template indicati. | Per la risoluzione della problematica è stata modificata la dicitura all'interno dei template da
"Fungibilita/Periodo" a "Evento[EventoCorrente=&apos;S&apos;]/Fungibilita/StringaFungibilita". | Il problema era legato al fatto che la variabile riguardante il periodo della fungibilità pena era mal riportato nel codice del template.
Template modificati:
siep\am\SIEP_AM_COMPU657_1.rtf
siep\am\SIEP_AM_COMPU657_2.rtf
siep\am\SIEP_AM_COMPU657_MIS.rtf |  |
| 20230512014 | Tribunale di Sorveglianza di Roma | L’ufficio segnala che per il fascicolo  2021/285  TDS di Roma associato all’Avvocato con C.F. = BRCMRA 73P59G273M e relativo al soggetto “Axxxx”, i dati nel Sius di Roma sembrano consoni alla visualizzazione nel Sius Avvocati ma la ricerca per numero da come risultato “Nessun Fascicolo Trovato” mentre la ricerca per soggetto produce un insieme di risultati come da allegato; cliccando sul numero, però, il risultato è ancora “Nessun Fascicolo Trovato”. | Per la risoluzione della problematica è stato modificato il campo del Type portandolo ad accettare al massimo 100 caratteri. | Il problema era legato al fatto che nel type "TY_PENA" il campo "DESC_PENA_DETENTIVA" accettava descrizioni con al massimo 30 caratteri.
Type modificato:
TY_PENA |  |
| 20230718019 | Procura della Repubblica presso il Tribunale di Torino | L’ufficio segnala che il provvedimento non è presente o è stato annullato. Non si può dare corso alla misura alternativa. | Per la risoluzione della problematica è stato escluso il verbale dal caso in cui l'annullamento di un evento SIEP annulla anche il
provvedimento SIUS puntato. | Il problema era legato al fatto che quando si annullava il verbale di sottoscrizione agli obblighi, la funzione di cancellazione annullava anche l'ordinanza puntata dal verbale. Quindi il provvedimento di esecuzione che puntava la stessa ordinanza si ritrovava a puntare un evento annullato ed inoltre non era più possibile reinserire il verbale perché non trovava più l'ordinanza.
Classe modificata:
siap.siep.ordineesecuzione.action.ActCancellaProvvedimento.java |  |
| 202307240122 | Referente Applicativo DGSIA | L’ufficio segnala che Il sistema visualizza la maschera errata. | Per la risoluzione della problematica è stata corretta la gestione della form di inserimento cessazione per memorizzare la data detenzione e visualizzare correttamente i destinatari. | Il problema era legato al fatto che in fase di apertura della seconda form della funzione "Cessazione/Cessazione su Reclamo 51 Bis" era presente un errore Javascript e si interrompeva il pre caricamento della sezione dei "destinatari" che rimaneva nascosta.
Inoltre si perdeva il campo della data ingresso in istituto se si modificava il radio button.
Classe modificata:
siap/siep/misuraalternativa/LoadInserisciCessazioneMAAffProva.jsp |  |
| 20230817015 | N.C. | L’ufficio segnala l'errore sul modello SIES - SIUS_DE_DECRETOCITAZIONE-UDS.rtf per quanto riguarda la ricerca del magistrato; parte interessata :
<wr:out select="/X/FascicoloSius/MagitratoRelatore/Magistrato/Cognome"/> <wr:out select="/X/FascicoloSius/MagitratoRelatore/Magistrato/Nome"/> è scritto “MagitratoRelatore” invece di “MagistratoRelatore”. | Per la risoluzione della problematica è stata modificata la dicitura all'interno del template da
"MagitratoRelatore" a "MagistratoRelatore". | Il problema era legato al fatto che la variabile riguardante il modello "Magistrato Relatore" era mal riportata nel codice del template.
Template modificati:
sius\de\SIUS_DE_DECRETOCITAZIONE-UDS.rtf
sius\de\SIUS_DE_DECRCITUDSACCPERSOC.rtf
sius\de\SIUS_DE_DECRCITUDSCONVPENPEC.rtf |  |
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
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20230922-Piano_di_Rilascio_SIES_v.12.5.3.0.docx
SIUT-SIES-PT-1.0-20230922-Piano_dei_Test_SIES_v.12.5.3.0.docx
SIUT-SIES-CT-1.0-20230922-Allegato_al_piano_test_SIES_v.12.5.3.0.xls |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| aggiorna_db.zip | Database | Aggiornamento versione SIES in tabella “VERSIONE”
Aggiornamento Type “TY_PENA” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| template.zip | Template | sius\de\SIUS_DE_DECRETOCITAZIONE-UDS.rtf
sius\de\SIUS_DE_DECRCITUDSACCPERSOC.rtf
sius\de\SIUS_DE_DECRCITUDSCONVPENPEC.rtf
siep\am\SIEP_AM_COMPU657_1.rtf
siep\am\SIEP_AM_COMPU657_2.rtf
siep\am\SIEP_AM_COMPU657_MIS.rtf |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.5.2.0 (MEV_2023-38).
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
Creare sul server DB una cartella V_12_5_3_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_5_3_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_5_3_0 tramite il comando:
chmod 777 V_12_5_3_0
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES...........: siesxx	(dove xx è la sigla del distretto di appartenenza, per esempio: rm per Roma)
Password_SIES.......: siesxx
Nella cartella appena creata (V_12_5_3_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_5_3_0/log/ in cui si può constatare l’esito dell’esecuzione.
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
Copiare i files contenuti nella cartella template\sius\de
nella cartella “/var/SIES/template/sius/de” sovrascrivendo quelli precedenti;
Copiare i files contenuti nella cartella template\siep\am
nella cartella “/var/SIES/template/siep/am” sovrascrivendo quelli precedenti;
Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 2.b e 2.e. All’avvio, infatti, tali cartelle verranno ricreate.
Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.