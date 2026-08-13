---
uniqueName: siut-sies-pr-1-0-20250718-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20250718 Piano di Rilascio SIES v 12 8 1 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20250718-Piano_di_Rilascio_SIES_v.12.8.1.0

> **File originale:** `RILASCIO_12.8.1.0/SIUT-SIES-PR-1.0-20250718-Piano_di_Rilascio_SIES_v.12.8.1.0.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento per l’innovazione tecnologica della giustizia
Direzione generale per i sistemi informativi automatizzati |
| --- |
|  |




Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Simone Gioggi | Analista Programmatore Senior |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 18/07/2025 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 18/07/2025 | Prima Emissione |  |


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
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.8.1.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.8.1.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.
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
| 202506300126 | Procura della Repubblica presso il Tribunale di Gela (CL) | L’ufficio segnala che un utente non riesce a scaricare un’istanza sul fascicolo in oggetto in quanto gli restituisce un errore | Per la risoluzione della problematica è stato aggiunto un controllo sulla valorizzazione dei dati dell'avvocato presentante | Il problema era legato al fatto che mancava un controllo sul campo cognome dell’avvocato presentante.
Classe modificata:
siap.siep.nuovaistanza.action.ActInserisciNuovaIstanza.java |  |
| 202506300135 | Procura generale presso la Corte d’Appello di Cagliari | L’ufficio segnala che il sistema quando elabora ordine esecuzione e ingiunzione pagamento ex art.660 cpp perde il dato dello stato di esecuzione e non riporta che la condanna è assorbita in cumulo | Per la risoluzione della problematica è stato corretto il test di inclusione dello stato esecuzione nel template | Il problema era legato al fatto che il controllo sull’inclusione dello stato esecuzione era maggiore di uno, piuttosto che maggiore di zero.
Template modificati:
/siep/ma/SIEP_MA_DETDPROVV_ARDOM_656_PROCU.rtf
/siep/pp/SIEP_PP_OI_PAGAMENTO_RR.rtf
/siep/pp/SIEP_PP_OI_PAGAMENTO_RR_DET.rtf
/siep/pp/SIEP_PP_OI_PAGAMENTO_UN.rtf
/siep/pp/SIEP_PP_OI_PAGAMENTO_UN_DET.rtf |  |
| 20250707018 | Procura della Repubblica presso il Tribunale di Bergamo (BS) | L’ufficio segnala che NELLA PRATICA SIEP 655/2025, INSERENDO L'AVVOCATO SIGNORELLI FRANCESCA DEL FORO DI BERGAMO, IL SISTEMA COMUNICA CHE IL CODICE DEL COMUNE DEL C.F. E' ERRATO. IN EFFETTI, IL CODICE FISCALE CORRETTO E' SGNFNC80M51A794M E NON SGNFNC80M51A7V4Y | Per la risoluzione della problematica è stato modificato il codice per la decodifica delle omocodie nei codici fiscali | Il problema era legato al fatto che il controllo sul codice catastale si fermava al primo digit piuttosto che verificarli tutti e quattro.
Classe modificata:
siap.sico.util.AvvocatoUtil.java |  |
| 202507140139 | Procura della Repubblica presso il Tribunale di Bolzano | L’ufficio segnala che nell'applicativo SIES il sistema impone di utilizzare i nomi del Comuni della Provincia di Bolzano  presenti  nell'elenco (ovvero bilingui nel formato BOLZANO/BOZEN) ma poi compare messaggio di errore perché non accetta caratteri diversi dai caratteri alfabetici (ovvero: barra /) | Per la risoluzione della problematica è stato modificato il codice togliendo il controllo sui caratteri SOLO alfabetici | Il problema era legato al fatto che esisteva un controllo sulla sede che non consentiva l’immissione di caratteri non alfabetici.
Classe modificata:
siap\siep\ordineesecuzione\LoadInserisciOrdineEsecuzioneSimeone.jsp |  |
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
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20250718-Piano_di_Rilascio_SIES_v.12.8.1.0.docx
SIUT-SIES-PT-1.0-20250718-Piano_dei_Test_SIES_v.12.8.1.0.docx
SIUT-SIES-CT-1.0-20250718-Allegato_al_piano_test_SIES_v.12.8.1.0.xlsx |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| aggiorna_db.zip | Database | Aggiornamento versione SIES in tabella “VERSIONE” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| template.zip | Template | siep\ma\SIEP_MA_DETDPROVV_ARDOM_656_PROCU.rtf
siep\pp\SIEP_PP_OI_PAGAMENTO_RR.rtf
siep\pp\SIEP_PP_OI_PAGAMENTO_RR_DET.rtf
siep\pp\SIEP_PP_OI_PAGAMENTO_UN.rtf
siep\pp\SIEP_PP_OI_PAGAMENTO_UN_DET.rtf |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.8.0.3.
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
Creare sul server DB una cartella V_12_8_1_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_8_1_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_8_1_0 tramite il comando:
chmod 777 V_12_8_1_0
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES...........: siesxx	(dove xx è la sigla del distretto di appartenenza, per esempio: rm per Roma)
Password_SIES.......: siesxx
Nella cartella appena creata (V_12_8_1_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_8_1_0/log/ in cui si può constatare l’esito dell’esecuzione.
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
Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 2.b e 2.e. All’avvio, infatti, tali cartelle verranno ricreate.
Copiare i files contenuti nella cartella template\siep\ma
nella cartella “/var/SIES/template/siep/ma” sovrascrivendo quelli precedenti;
Copiare i files contenuti nella cartella template\siep\pp
nella cartella “/var/SIES/template/siep/pp” sovrascrivendo quelli precedenti;
Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.