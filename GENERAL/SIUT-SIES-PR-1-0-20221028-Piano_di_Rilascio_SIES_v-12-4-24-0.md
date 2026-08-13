---
uniqueName: siut-sies-pr-1-0-20221028-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20221028 Piano di Rilascio SIES v 12 4 24 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20221028-Piano_di_Rilascio_SIES_v.12.4.24.0

> **File originale:** `RILASCIO_12.4.24.0/SIUT-SIES-PR-1.0-20221028-Piano_di_Rilascio_SIES_v.12.4.24.0.docx`  
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
| Data approvazione | 28/10/2022 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 28/10/2022 | Prima Emissione |  |


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
4.2	Riferimenti ChangeRequest (ADE/MEV)	13
4.2.1	Documenti a corredo della sessione di verifica conformità	13
5	Dettaglio degli elementi oggetto del rilascio	14
6	Installazione	15
6.1	Prerequisiti	15
6.2	Attività di preinstallazione	15
6.3	Attività di installazione	15
6.3.1	Installazione lato DB	15
6.3.1.1	Esecuzione script	15
6.3.2	Installazione applicazione	16
6.3.2.1	Deploy Applicazione	16
6.4	Attività di configurazione	16
6.5	Attività di post-installazione	17


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio del sistema SIES.
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.24.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.4.24.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.
Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.
# Identificazione degli elementi rilasciati
| Supporto | Oggetti: | Ver. | Del |
| --- | --- | --- | --- |
| Portale fornitura | SIUT > 06 - Rilasci Software > SIES > Rilascio SIES 12.4.24.0 2022-10-28 | 12.4.24.0 | 28/10/2022 |
| Note-osservazioni |  |  |  |


# Riferimenti degli oggetti del rilascio
## Riferimenti Anomalia (MAC/GAR)
| Rif. Ticket OTRS | Sede
Ufficio | Descrizione segnalazione | Descrizione
intervento | Descrizione Tecnica | Manuali corretti |
| --- | --- | --- | --- | --- | --- |
| 202209120114 | Nessuna | L’ufficio segnala che il sistema non consente di validare un provvedimento regolarmente inserito e lavorato. Quando si cerca di validarlo, il sistema restituisce l’errore:
java.lang.NullPointerException. | Per la risoluzione della problematica è stata corretta la query in caso in cui si selezioni come autorità emittente "Presidente delle Repubblica" durante la definizione di un procedimento. | Il problema era legato al fatto che, nel caso di Archiviazione Altra Autorità, se si selezionava "Presidente Della Repubblica", il relativo codice “PDR” non veniva risolto quando si faceva la select sulla tabella ARCHIVIAZIONE. Fallendo la join non caricava correttamente il dettaglio e falliva la validazione da cui il “NullPointer”. Il campo “ARCHIVIAZIONE.COD_TIPO_AUTORITA_EMITTENTE” non veniva caricato con i codici di un solo dominio ma di domini differenti ed in alcuni casi con il campo “RV_HIGH_VALUE” e non con il “RV_LOW_VALUE” della tabella “CG_REF_CODES”. La decodifica viene fatta incrociando altri due domini “TIPO_AUTORITA” e “TIPO_UFFICIO” dove il valore "Presidente della Repubblica" non è contenuto e non può essere aggiunto.
Quindi, è stata modificata la query aggiungendo in ‘OR condition’ la decodifica del valore “PDR”.
Classe modificata:
siap.siep.archiviazione.dao.ArchiviazioneSqlDAO.java
\siap\siep\archiviazione\LoadDettaglioProvvAltraAutorita.jsp |  |
| 20220919012 | Procura Generale presso la Corte d’Appello di Napoli (NA) | L’ufficio segnala un’anomalia al sistema, che nel caricare il cumulo, il sistema indica quale sede del Casellario deputato alla iscrizione di provvedimento di cumuli, la sede del luogo di nascita del condannato. A legislazione invariata, si tratta di un errore, che necessita di correzione manuale ogni volta, ammesso che appunto l'operatore se ne avveda, dando per scontato che ci sia indicato il Casellario della sede dell'Ufficio Giudiziario che emette il provvedimento. | Per la risoluzione della problematica è stato corretto il template “NoteDiTrasmissione” modificando la sede del Casellario Giudiziale. | Il problema era legato al fatto che nel template era presente come sede del Casellario Giudiziale quella del luogo di nascita del condannato piuttosto che quella dell’Ufficio emittente.
Template modificato: 
NoteDiTrasmissione.rtf |  |
| 202209190112 | Nessuna | L’ufficio segnala che il sistema non permette di emettere un ordine di esecuzione, poiché non accetta come anno data scadenza pena il valore 2051. | Per la risoluzione della problematica è stato modificato il controllo Javascript sul valore massimo per l'anno portandolo da 2050 a 2099. | Il problema era legato alla presenza nella classe jsp segnalata di un controllo sulle date per cui era stato impostato il valore 2050 come anno limite. Tale valore risulta ad oggi obsoleto. Tale valore, quindi, è stato innalzato.
Classe modificata:
\siap\siep\ordineesecuzione\LoadInserisciOrdineEsecuzione.jsp |  |
| 20221005019 | DGSIA | L’ufficio segnala che nella tabella ‘FUNZIONE’ è presente il campo ‘COD_TIPO_FUNZIONE’ che identifica l'appartenenza al menù gerarchico od al contesto. Deriva dal dominio ‘TIPO_FUNZIONE’, che si presume sia in ‘CG_REF_CODES’.
Nella funzione con codice ‘90110737’, il valore del campo ‘COD_TIPO_FUNZIONE’ è ‘F’.
Nella tabella ‘CG_REF_CODES‘ sembra mancare, tra i valori per cui ‘RV_DOMAIN=TIPO_FUNZIONE’,  la descrizione relativa ad ‘RW_LOW_VALUE=F’. | Per la risoluzione della problematica è stato aggiunto un record nel database. | Il problema era legato al fatto che nella tabella ‘CG_REF_CODES’ e dominio ‘TIPO_FUNZIONE’ mancava la codifica del valore ‘F’ utilizzato nella tabella ‘FUNZIONE’ per il record con valore ‘90110737’ nel campo ‘COD_TIPO_FUNZIONE’.
Tabella modificata: 
CG_REF_CODES |  |
| 202210060112 | Nessuna | L’ufficio segnala un errore nella funzione di copia dei reati. | Per la risoluzione della problematica è stato modificato il controllo Javascript sulla selezione dei reati da copiare. | Il problema era legato al fatto che nella JSP non era gestita la selezione dei reati da copiare nel caso il numero dei reati era maggiore di uno: se non veniva selezionato alcun reato, partiva un array vuoto (senza ID reato) e la classe Java andava in errore. Aggiunta obbligatorietà selezione reato.
Classe modificata:
\jsp\files\siap\siep\reato\RicercaReatiFascicolo.jsp |  |
| 202210060114 | Nessuna | L’ufficio segnala una correzione nel template “SIEP_MS_TRASM_COMP”. | Per la risoluzione della problematica è stato corretto il template secondo le indicazioni dell’utente. | Il problema era legato al fatto che, nella gestione del Titolo Esecutivo associato alla Misura Sicurezza, se esso era differente dal titolo del procedimento allora veniva citato al posto del titolo principale.
Template modificato: 
SIEP_MS_TRASM_COMP.rtf |  |
| 202210130113 | Nessuna | L’ufficio segnala un errore nel messaggio di restituzione degli atti. | Per la risoluzione della problematica è stata aggiunta la gestione del codice di “RIGETTO” che non era gestito. | Il problema era legato al fatto che, nel caso di “RIGETTO” degli atti trasmessi per cumulo, il sistema continuava a visualizzare, sul dettaglio del fascicolo, un messaggio con l'esito del rigetto. Problema causato dalla mancata gestione del codice di rigetto “01007” che doveva essere gestito alla stregua del codice di restituzione atti (“01003”).
Inoltre, il codice “01007” era inserito solo in fase di rigetto sul messaggio e quindi nella fase di annotazione "Esito Atti" automatica, ma non in fase di inserimento manuale dell'annotazione esito. Il codice è stato aggiunto nella combo "Esito Provvedimento".
Classi modificate:
siap.siep.fascicolo.action.ActLoadDettaglioFascicolo
siap.siep.presaincarico.action.ActLoadInsAnnotaEsitoTrasmComp
/jsp/files/siap/siep/presaincarico/LoadInsAnnotazioneEsitoTrasmComp.jsp |  |
| 202210170122 | Procura della Repubblica presso il Tribunale di Mantova | L’ufficio segnala che nel confermare un provvedimento di Concessione detenzione domiciliare a termine (Decisioni sorveglianza - Differimento pena nelle forme della detenzione domiciliare - Concessione) il sistema va in errore. | Per la risoluzione della problematica è stata modificata la gestione della posizione giuridica “Espiazione Pena in Regime di Detenzione Domiciliare” successiva a quella di “Libero” per il calcolo della data di fine misura che viene effettuato anche in questa casistica. | Il problema era legato al fatto che, nel caso di POSIZIONE_GIURIDICA = "12" (“Espiazione Pena in Regime di Detenzione Domiciliare”) e posizione giuridica precedente pari a “LIBERO”, il sistema non impostava la "Data Inizio Misura" così che poi nel calcolo della "Nuova Data Fine Misura" si incorreva in un errore (NullPointer).
Classe modificata:
siap.siep.misuraalternativa.action.ActInserisciMADetDomTemp.java |  |
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
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20221028-Piano_di_Rilascio_SIES_v.12.4.24.0.docx
SIUT-SIES-PT-1.0-20221028-Piano_dei_Test_SIES_v.12.4.24.0.docx
SIUT-SIES-CT-1.0-20221028-Allegato_al_piano_test_SIES_v.12.4.24.0.xls |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| aggiorna_db.zip | Database | Script:
Aggiornamento versione SIES in tabella “VERSIONE”
Inserimento valore nel dominio 'TIPO_FUNZIONE' della tabella “CG_REF_CODES” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| template.zip | Template | Template aggiornati:
NoteDiTrasmissione.rtf
SIEP_MS_TRASM_COMP.rtf |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.23.0.
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
Creare sul server DB una cartella V_12_4_24_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_4_24_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_24_0 tramite il comando:
chmod 777 V_12_4_24_0
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES...........: siesxx	(dove xx è la sigla del distretto di appartenenza, per esempio: rm per Roma)
Password_SIES.......: siesxx
Nella cartella appena creata (V_12_4_24_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_4_24_0/log/ in cui si può constatare l’esito dell’esecuzione.
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
Copiare i files contenuti nella cartella template\siep\cumulo
nella cartella “/var/SIES/template/siep/cumulo” sovrascrivendo quelli precedenti;
Copiare i files contenuti nella cartella template\siep\ms
nella cartella “/var/SIES/template/siep/ms” sovrascrivendo quelli precedenti;
Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 2.b e 2.e. All’avvio, infatti, tali cartelle verranno ricreate.
Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.