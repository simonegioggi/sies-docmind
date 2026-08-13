---
uniqueName: siut-sies-pr-1-0-20230428-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20230428 Piano di Rilascio SIES v 12 4 28 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20230428-Piano_di_Rilascio_SIES_v.12.4.28.0

> **File originale:** `RILASCIO_12.4.28.0/SIUT-SIES-PR-1.0-20230428-Piano_di_Rilascio_SIES_v.12.4.28.0.docx`  
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
| Data approvazione | 28/04/2023 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 28/04/2023 | Prima Emissione |  |


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
4.2	Riferimenti ChangeRequest (ADE/MEV)	10
4.2.1	Documenti a corredo della sessione di verifica conformità	10
5	Dettaglio degli elementi oggetto del rilascio	11
6	Installazione	12
6.1	Prerequisiti	12
6.2	Attività di preinstallazione	12
6.3	Attività di installazione	12
6.3.1	Installazione lato DB	12
6.3.1.1	Esecuzione script	12
6.3.2	Installazione applicazione	13
6.3.2.1	Deploy Applicazione	13
6.4	Attività di configurazione	13
6.5	Attività di post-installazione	13


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio del sistema SIES.
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.28.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.4.28.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.
Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.
# Identificazione degli elementi rilasciati
| Supporto | Oggetti: | Ver. | Del |
| --- | --- | --- | --- |
| Portale fornitura | SIUT > 06 - Rilasci Software > SIES > Rilascio SIES 12.4.28.0 2023-04-28 | 12.4.28.0 | 28/04/2023 |
| Note-osservazioni |  |  |  |


# Riferimenti degli oggetti del rilascio
## Riferimenti Anomalia (MAC/GAR)
| Rif. Ticket OTRS | Sede
Ufficio | Descrizione segnalazione | Descrizione
intervento | Descrizione Tecnica | Manuali corretti |
| --- | --- | --- | --- | --- | --- |
| 20230224014 | Tribunale Ordinario di Cagliari | L’ufficio segnala che nel sige tribunale dopo aver selezionato il dettaglio ruolo udienza per data, facendo clic su verbale udienza relativamente ad un singolo procedimento, come in allegato, la stampa prodotta riporta i verbali di tutti i procedimenti fissati per quella data anziché il solo selezionato. | Per la risoluzione della problematica è stato corretto il link sull'icona di stampa che faceva stampare erroneamente il verbale per tutti i fascicoli. | Il problema era legato al fatto che il collegamento sull’icona di stampa produceva la stampa di tutti i procedimenti del Magistrato (“idMagistrato” valorizzato) invece che del singolo fascicolo.
Classe modificata:
\jsp\files\siap\sige\udienzaprocedimento\dettaglioruolo\ListaProcedimentixUdienza.jsp |  |
| 202302280124 | Referente Applicativo Sistema SIES | L’ufficio segnala che dal percorso funzionale “Statistiche/Monitoraggio->Statistiche - Estrazione Dati, classe IV, procedimenti pendenti nel periodo”, indicando nella sezione "intervallo anno", in un caso gli anni dal 2013 al 2023 e nel secondo caso il solo anno 2017, i risultati per l'anno 2017 variano se facciamo l'estrazione per singolo anno oppure per un intervallo di anni. A logica non c'è motivo per cui ciò debba accadere. | Per la risoluzione della problematica sono state corrette le query di estrazione dati sia a livello applicativo che sulle viste per evitare la esclusione dei riaperti dal conteggio dei sopravvenuti e degli esauriti. | Il problema era legato al fatto che venivano considerati pendenti anche gli archiviati senza considerare l'anno di riferimento.
Classe modificata:
siap.siep.statis.dao.StatisticheMSSqlDAO.java
Viste modificate:
VW_MS_PROCEDIMENTI
VW_MS_PROC_ESAURITI
VW_MS_PROC_ESAURITI_MAG |  |
| 20230328019 | Procura Generale presso la Corte d'Appello di Perugia | L’ufficio segnala che sul procedimento 2023/38 nel campo "stato procedimento" -> presentata istanza il 23-3-2023, non è corretto, l'istanza è del 16-3-2023. La data del 23-3-2023 corrisponde alla Data Ordine Esecuzione. | Per la risoluzione della problematica è stato corretto l'inserimento della data per lo stato procedimento e la visualizzazione della data nomina difensore sul dettaglio dell'istanza. | Il problema era legato al fatto che come data istanza veniva impostata la data corrente (sysdate).
Classi modificati:
siap.siep.nuovaistanza.controller.NuovaIstanzaController.java
/jsp/files/siap/siep/nuovaistanza/DettaglioNuovaIstanza.jsp |  |
| 20230419018 | Tribunale di Sorveglianza di Bologna | L’ufficio segnala che non riesce ad ottenere dal programma sius del TDS Bologna le statistiche comparate dei magistrati. Il sistema non rilascia il file Excel ma restituisce un messaggio di errore. | Per la risoluzione della problematica è stata modificata la gestione del nome delle schede nei fogli Excel. | Il problema era legato al fatto che nella creazione del nome della scheda del foglio Excel viene utilizzato il nome del magistrato.
Se contiene caratteri non accettabili per il nome di una scheda Excel va in errore la generazione del foglio.
Nel caso specifico era l'apostrofo del nome del magistrato (MARILU'). Il nome della scheda NON può terminare o iniziare con tale carattere.
Classi modificate: 
f3b.util.StringUtils.java
siap.sius.statistiche.util.excel.StatisticaComparataMagistratiExcel.java |  |
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
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20230428-Piano_di_Rilascio_SIES_v.12.4.28.0.docx
SIUT-SIES-PT-1.0-20230428-Piano_dei_Test_SIES_v.12.4.28.0.docx
SIUT-SIES-CT-1.0-20230428-Allegato_al_piano_test_SIES_v.12.4.28.0.xls |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| aggiorna_db.zip | Database | Aggiornamento versione SIES in tabella “VERSIONE”
Aggiornamento Vista “VW_MS_PROCEDIMENTI”
Aggiornamento Vista “VW_MS_PROC_ESAURITI”
Aggiornamento Vista “VW_MS_PROC_ESAURITI_MAG” |
| sorgenti.zip | Sorgenti | Sorgenti software |
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
Creare sul server DB una cartella V_12_4_28_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_4_28_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_28_0 tramite il comando:
chmod 777 V_12_4_28_0
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES...........: siesxx	(dove xx è la sigla del distretto di appartenenza, per esempio: rm per Roma)
Password_SIES.......: siesxx
Nella cartella appena creata (V_12_4_28_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_4_28_0/log/ in cui si può constatare l’esito dell’esecuzione.
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