---
uniqueName: siut-sies-pr-1-0-20230224-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20230224 Piano di Rilascio SIES v 12 4 27 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20230224-Piano_di_Rilascio_SIES_v.12.4.27.0

> **File originale:** `RILASCIO_12.4.27.0/SIUT-SIES-PR-1.0-20230224-Piano_di_Rilascio_SIES_v.12.4.27.0.docx`  
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
| Data approvazione | 24/02/2023 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 24/02/2023 | Prima Emissione |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
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
6.5	Attività di post-installazione	15


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio del sistema SIES.
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.27.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.4.27.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.
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
| 20230125017 | Procura della Repubblica presso il Tribunale di Sciacca (PA) | L’ufficio segnala che durante l'analisi effettuata dall'assistenza per la soluzione di un ticket aperto da un utente della Procura presso il Tribunale di Sciacca che lamentava l'impossibilità, in SIEP, di visualizzare un fascicolo mediante l'usuale funzione di ricerca per numero (risultato: "nessun elemento trovato"), si è osservato che il risultato deriva dalla struttura della vista “V_FASCICOLO_SIEP” le cui condizioni impediscono di visualizzare fascicoli per i quali il campo della tabella collegata “STATO_PROCEDIMENTO.COD_STATO_PROCEDIMENTO” è valorizzato a '0000'. Si è rilevato che questa circostanza non è imitata al solo fascicolo evidenziato dall'utente, ma ad un gruppo di 57 fascicoli, tutti della stessa sede e tutti con numero fascicolo > 70000, iscritti in vari anni. | Per la risoluzione della problematica è stata modificata l'impostazione del valore "0000" sul codice stato procedimento per il caso specifico e sostituito col valore "0109" (VALIDATO). | Il problema era legato al fatto che, nel codice, per  il caso di “Comunicazione Dichiarazione estinzione libertà controllata” non era stato previsto uno specifico valore bensì un generico ‘0000’; il sistema avrebbe dovuto impostare il valore a '0109' (VALIDATO). Inoltre, l'assenza del valore '0000' nel dominio 'STATO_PROCEDIMENTO' della tabella “CG_REF_CODES”, causa l'assenza dei relativi fascicoli nella vista “V_FASCICOLO_SIEP”.
Classe modificata:
siap.siep.penapecuniaria.action.ActUploadTrasmAnnotazioneProvvedimentoSor.java |  |
| 202301250123 | Procura presso il tribunale di Campobasso | L’ufficio segnala che
dovendo procedere alla cancellazione di due provvedimenti generati per errore  e già validati sui fascicoli  n. 30004/2021 e n. 30005/2021 SIES, il sistema  risponde con un messaggio di errore. | Per la risoluzione della problematica si è intervenuti sul codice; prima di eliminare le annotazioni vanno eliminati eventuali record delle tabelle figlie (“ANNMAN_PENACOMPL”, “PENA_COMPLESSIVA”, “ANNMAN_REATO”, “REATO”). | Il problema era legato al fatto che quando si tentava la cancellazione della annotazione manuale collegata all'evento non si controllava la presenza di record figli della succitata tabella (reato e pena complessiva).
Classi modificate:
siap.siep.ordineesecuzione.controller.OrdineEsecuzioneController.java
siap.siep.penasospesa.dao.AnnmanPenacomplDAO.java
siap.siep.penasospesa.dao.AnnmanReatoDAO.java |  |
| 20230126014 | Referente Applicativo Sistema SIES | L’ufficio segnala un comportamento anomalo rilevato interrogando il prototipo di PA dal SIUS avvocati di prova. | Per la risoluzione della problematica è stata modificata una query all'interno del package body “AVVOCATURA_SIUS (PROCEDURE CERCA_FASIUS_PER_ESTREMI)”. | Il problema era legato al fatto che nel caso di fissazione udienza validata e con deposito validato il sistema non estraeva il record correttamente.
Package modificato;
AVVOCATURA_SIUS |  |
| 20230201017 | Tribunale di Sorveglianza di Roma | L’ufficio segnala che Il difensore non vede il provvedimento del 07/04/2022 benché validato. | Per la risoluzione della problematica è stato gestita l'ordinanza di rinvio udienza come l'ordinanza classica, quindi l'avviso viene visualizzato dall'avvocato solo a valle della validazione del deposito. | Il problema era legato al fatto che, lato codice, in fase di emissione dell’avviso, all’atto della validazione del provvedimento di ordinanza di rinvio udienza, mancava il controllo che ne impediva l’inserimento.
Classi modificate:
siap.sico.evento.controller.EventoController.java
siap.sius.documentoallegato.controller.DocumentoAllegatoController.java |  |
| 20230202011 | Referente Applicativo Sistema SIES | L’ufficio segnala anomalie sull'annotazione del foglio complementare. | Per la risoluzione della problematica sono state gestite funzionalità e specifiche come quelle riportate nel documento di analisi (SIGI_PNL_AF_2015 03 03_1.1_MEV 15 - Revisione SIGE Parte 3 - Analisi Funzionale.doc). | Il problema era legato alla non uniformità tra quanto descritto nel documento di analisi e quanto presente nell’applicativo.
Classi modificate:
siap.sige.fogliocomplementare.action.ActInserisciCompFoglioComp.java
siap.sige.fogliocomplementare.action.ActLoadDettaglioFCTastoFunzione.java
siap.sige.fogliocomplementare.action.ActModificaCompFoglioComp.java
siap.sius.documentoallegato.controller.DocumentoAllegatoController.java
siap\sige\fogliocomplementare\LoadDettaglioCompFoglioComp.jsp
siap\sige\fogliocomplementare\LoadDettaglioCompFoglioCompTastoFunzione.jsp
siap\sige\fogliocomplementare\LoadInserisciCompFoglioCompTastoFunzione.jsp
siap\sige\statistiche\LoadRicercaStatisticheFogliComp.jsp
siap.sige.statistiche.controller.StatisController.java
siap.sige.statistiche.model.StatisticheFogliComplementariContainerModel.java
siap.sige.statistiche.model.StatisticheFogliComplementariModel.java
siap.sige.statistiche.dao.StatisticheFogliComplementariSqlDAO.java
siap\sige\statistiche\StatisticheFogliComplementari.jsp |  |
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
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20230224-Piano_di_Rilascio_SIES_v.12.4.27.0.docx
SIUT-SIES-PT-1.0-20230224-Piano_dei_Test_SIES_v.12.4.27.0.docx
SIUT-SIE-MU-1.4-20230224-Manuale_Utente-Avvocatura_SIES.pdf
SIUT-SIES-CT-1.0-20230224-Allegato_al_piano_test_SIES_v.12.4.27.0.xls |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| aggiorna_db.zip | Database | Aggiornamento versione SIES in tabella “VERSIONE”
Aggiornamento Package Body “Avvocatura_SIUS”
Aggiornamento in tabella “RELAZIONE_FUNZIONE”
Aggiornamento in tabella “stato_procedimento” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.26.0.
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
Creare sul server DB una cartella V_12_4_27_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_4_27_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_27_0 tramite il comando:
chmod 777 V_12_4_27_0
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES...........: siesxx	(dove xx è la sigla del distretto di appartenenza, per esempio: rm per Roma)
Password_SIES.......: siesxx
Nella cartella appena creata (V_12_4_27_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_4_27_0/log/ in cui si può constatare l’esito dell’esecuzione.
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