---
uniqueName: siut-sies-pr-1-0-20211022-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20211022 Piano di Rilascio SIES v 12 4 14 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20211022-Piano_di_Rilascio_SIES_v.12.4.14.0

> **File originale:** `RILASCIO_12.4.14.0/SIUT-SIES-PR-1.0-20211022-Piano_di_Rilascio_SIES_v.12.4.14.0.docx`  
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
| Data approvazione | 22/10/2021 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 22/10/2021 | Prima Emissione |  |


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
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.14.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.4.14.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.
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
| 20210922015 | Procura della Repubblica Presso il Tribunale per i Minorenni di Bari | L’ufficio segnala che nella procedura di trasmissione della comunicazione della scadenza del termine fissato per poter richiedere l'estinzione della pena non è contemplato l'ufficio recupero crediti presso il tribunale per i minorenni. | Per la risoluzione della problematica si è intervenuti con l’aggiunta nella combo degli "Uffici Recupero Credito Presso" anche le voci: "Tribunale per i Minorenni" e "Sezione di Corte di Appello per i minorenni". | Corretto il modulo per far apparire le voci richieste.
Classi corrette:
siap.siep.sospensione.action.ActCalcolaAvvenutaEspulsione.java |  |
| 20210924018 | Procura Generale della Repubblica Presso la Corte D'Appello di Bari | L'Ufficio segnala che, in relazione ad un determinato fascicolo della Procura Generale della Repubblica di Bari, si proceda alla eliminazione delle pene accessorie caricate nel fascicolo.  L’ufficio non riesce in autonomia ad eliminarle in quanto compare un errore Oracle “ORA-02292”. | Per la risoluzione della problematica è stato aggiunto un controllo in fase di cancellazione di una Pena Accessoria lato SIEP. Viene verificato se agganciata da uno o più fascicoli SIGE (PENA_ACCESSORIA_SENTENZA_SIGE). In caso affermativo viene mostrato un messaggio utente per avvertire che la Pena Accessoria non è cancellabile. | Sono state modificate le classi:
siap.sige.fascicolo.dao.FascicoloSigeSqlDAO.java
siap.siep.penaaccessoria.controller.PenaAccessoriaController.java
siap.siep.penaaccessoria.action.ActCancellaPenaAccessoria.java
al fine di evitare di restituire un errore Oracle. L’utente sarà informato che non sarà possibile cancellare le pene accessorie. |  |
| 20210928015 | Tribunale Ordinario di Torino | L’ufficio segnala che Il sistema SIGE duplica gli oggetti nel modulo estrazione dati. | Per la risoluzione della problematica si è intervenuti con la modifica della query deputata all’estrazione dei dati poiché duplicava i tenori in presenza di più udienze. | Il Problema era legato alla funzione LISTAGG che non poteva essere utilizzata per questo tipo di estrazione.
Modificata la query ed effettuata l'aggregazione dei tenori stesso fascicolo 
nella classe java.
Classe corretta:
siap.sige.fascicolo.dao.FascicoloSigeSqlDAO.java |  |
| 202109290111 | Procura della Repubblica Presso il Tribunale per i Minorenni di Torino | L’ufficio segnala una statistica inesatta. | Per la risoluzione della problematica si è intervenuti con la correzione del fatto che non veniva visualizzata la scheda Altre Posizioni. | Corrette le classi:
siap.siep.statis.action.ActCreaStatisticaRiepilogoMovimentoProcedimenti.java
in cui è stato corretto il ciclo che non faceva caricare correttamente il Foglio Excel.
siap.siep.statis.controller.StatisticheMSController.java
in cui è stata corretta una costante che riportava una descrizione errata nel foglio Excel. |  |
| 20210930015 | Procura della Repubblica Presso il Tribunale di Torino | L’ufficio segnala la necessità di migliorie di formattazione in un template. | Per la risoluzione della problematica si è intervenuti con il rilascio del template opportunamente modificato. | E’ stato rilasciato il documento “SIEP_MA_TRASF_ATTI_51BIS.rtf” in cui è stato giustificato il testo in alcuni punti e modificata una frase (“preposto alla vigilanza”) come da richiesta (“per quanto di competenza”). |  |
| 20211006019 | Procura della Repubblica Presso il Tribunale di Perugia | L’ufficio segnala l’impossibilità di modificare i dati di un titolo esecutivo, al quale è stata associata una richiesta di misura alternativa. Il messaggio di warning denuncia la presenza di un EVENTO non validato. | Per la risoluzione della problematica si è intervenuti con la correzione della classe deputata alla gestione dell’elenco dei provvedimenti del Giudice Esecuzione e della Sorveglianza dovuto al fallimento della query di join con il dominio 'OGGETTO_PROCEDIMENTO'. | E’ stata modificata la classe:
siap.sico.decodifiche.dao.DecodificheSqlDAO.java
in cui è stata cambiata l’azione di caricamento della combo “Oggetto procedimento” che deve filtrare per valore X001 e non più U001.
A tal proposito è stato rilasciato il file “20211006019.sql” che consente di modificare, nella tabella CG_REF_CODES (dominio “MOTIVO_PROVVEDIMENTO”), il valore ‘U001’ con ‘X001' per i codici ('2000' e '2001'). |  |
| 20211011015 | Procura della Repubblica Presso il Tribunale di Torino | L’ufficio segnala un errore Javascript (“org.apache.jasper.JasperException”) nella pagina “LoadVariazioneDecorrenzaScadenza.jsp”. | Per la risoluzione della problematica si è intervenuti con la correzione della classe in cui andava in errore la funzione di variazione decorrenza e scadenza Pena in quanto la classe selezionava la pagina  predisposta per “Altra causa” e tale pagina al suo interno cercava il record “AltraCausa“ associato alla posizione giuridica non trovandolo. | E’ stata modificata la classe:
siap.siep.ordineesecuzione.action.ActLoadVariazioneDecorrenzaScadenza
In alcuni casi restava il “flagAltraCausa” sul fascicolo anche se la posizione giuridica diventava “in esecuzione questa causa”. Aggiunto ulteriore controllo nella classe per verificare se al record Posizione Giuridica viene effettivamente associato il record altra causa. |  |
| 202110140115 | Procura della Repubblica Presso il Tribunale di Trani | L’ufficio segnala che al momento della stampa del modello “SIEP_OE_LIB” a seguito di provvedimento di ordine di esecuzione per la carcerazione, non appare il numero del Tribunale conseguentemente a quello di RGNR (invece riportato nel modello). | Per la risoluzione della problematica si è intervenuti con il rilascio del template opportunamente modificato. | E’ stato rilasciato il documento “SentenzaComune.rtf” in cui sono state apportate le modifiche al fine di stampare i dati della sentenza in cui non veniva gestito anno/numero Reg. Gen. se relativo al GUP. |  |
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
Aggiornamento tabella “CG_REF_CODES” dominio “MOTIVO_PROVVEDIMENTO” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| template.zip | Template | Template aggiornati:
SentenzaComune.rtf
SIEP_MA_TRASF_ATTI_51BIS.rtf |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20211022-Piano_di_Rilascio_SIES_v.12.4.14.0.docx
SIUT-SIES-PT-1.0-20211022-Piano_dei_Test_SIES_v.12.4.14.0.docx
SIUT-SIES-CT-1.0-20211022-Allegato_al_piano_test_SIES_v.12.4.14.0.xls |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.13.0.
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
Creare sul server DB una cartella V_12_4_14_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_4_14_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_14_0 tramite il comando:
chmod 777 V_12_4_14_0

In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx

Nella cartella appena creata (V_12_4_14_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_4_14_0/log/ in cui si può constatare l’esito dell’esecuzione.

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
Copiare i files contenuti nella cartella template\siep\ma
nella cartella “/var/SIES/template/siep/ma” sovrascrivendo quelli precedenti;

Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 2.b e 2.e. All’avvio, infatti, tali cartelle verranno ricreate.

Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.