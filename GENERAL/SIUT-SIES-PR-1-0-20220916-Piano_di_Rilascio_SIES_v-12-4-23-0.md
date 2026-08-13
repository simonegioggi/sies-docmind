---
uniqueName: siut-sies-pr-1-0-20220916-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20220916 Piano di Rilascio SIES v 12 4 23 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20220916-Piano_di_Rilascio_SIES_v.12.4.23.0

> **File originale:** `RILASCIO_12.4.23.0/SIUT-SIES-PR-1.0-20220916-Piano_di_Rilascio_SIES_v.12.4.23.0.docx`  
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
| Data approvazione | 16/09/2022 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 16/09/2022 | Prima Emissione |  |


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
6.4	Attività di configurazione	14
6.5	Attività di post-installazione	15


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio del sistema SIES.
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.23.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.4.23.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.
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
| 20220801013 | Nessuna | L’ufficio segnala un errore nella ricerca per codice CUI  in “Sige Iscrizione manuale » Ricerca Procedimento SIEP per Soggetto”. | Per la risoluzione della problematica è stata corretta la condizione di ricerca nel caso in cui sia presente SOLO il codice AFIS nella ricerca. | Il problema era legato al fatto che nella ricerca se si metteva solo il codice CUI, tale condizione veniva ignorata poiché era in “OR condition” con una espressione sempre vera (quindi la query estraeva tutti i record della tabella “soggetto”).
Classe modificata:
siap.siep.fascicolo.dao.FascicoloSiepSoggettoSqlDAO.java |  |
| 20220801014 | Nessuna | L’ufficio segnala un errore nella “Ricerca Procedimenti Non Validati » Visualizzazione  procedimenti Definiti”. | Per la risoluzione della problematica è stata modificata la condizione di ricerca "non validati". Si testa lo “STATO_FASCICOLO = ‘02’" (iscritto) invece del “FLAG_VALIDATO = N”, in quanto alcune archiviazioni sono possibili anche per procedimenti non validati e dalla ricerca uscivano anche procedimenti non validati ma già archiviati. | Il problema era legato al fatto che nella funzione di ricerca non era impostata la condizione di procedimento iscritto; infatti, dalla ricerca dei fascicoli "NON VALIDATI" uscivano anche fascicoli che risultavano archiviati, principalmente classe 9. Il motivo è che l'archiviazione è consentita anche sui fascicoli non validati per cui il campo flag_validato resta ad “N”. La funzione di ricerca dei non validati testava proprio il “flag_validato = N”.
Classi modificate:
siap.siep.fascicolo.action.ActRicercaFascicoliNonValidati.java
siap.siep.fascicolo.dao.FascicoloSiepOnViewSqlDAO.java |  |
| 202208040112 | GIP di Varese | L’ufficio segnala una problematica relativa al trasferimento di una ordinanza. Quando si clicca il bottone "Trasferisci ordinanza" si ha l'errore "Funzione o classe non disponibile: siap.sige.provvedimento.action.ActLoadTrasferisciProvvedimento". | Per la risoluzione della problematica è stato oscurato il link che implementava la funzionalità di trasferimento. | Il problema era legato alla presenza della icona per la funzione di trasmissione del deposito decreto e deposito ordinanza che risulta essere un refuso della analoga funzione SIUS. In realtà in SIGE non è al momento prevista la trasmissione degli atti tra uffici SIGE, né con gli altri sottosistemi SIES, tanto è vero che mancano anche le funzioni di “Presa in carico”, “Riscontro Trasmissioni” e “Ricerche Altra BDI”.
Classe modificata:
siap/sige/provvedimento/DettaglioDepositoProvvedimentoSige.jsp |  |
| 20220824016 | Ufficio di Sorveglianza di Udine (TS) | L’ufficio segnala che quando si stampa il decreto di estinzione della Libertà Controllata viene riportato per due volte il nome del magistrato referente per il procedimento. | Per la risoluzione della problematica è stato corretto il template “SIUS_DE_ESTINZIONESS.rtf”. | Il problema era legato al fatto che nel template erano presenti due volte le informazioni sul Magistrato di Sorveglianza.
Template modificato: 
SIUS_DE_ESTINZIONESS.rtf |  |
| 20220906012 | Nessuna | L’ufficio segnala di correggere la frase sottostante:
-   a Notifica ai sensi dell'art. 148 co. 2 bis c.p.p. di - per la notifica, nei termini di legge, al difensore. | Per la risoluzione della problematica è stato corretto il template “SIEP_MA_REVO_AFFI_SOSP.rtf”. | Il problema era legato al fatto che nel template non venivano fatte distinzioni per le tre voci tra le Autorità di Notifica (Notifica ai sensi dell'art. 148 co. 2 bis c.p.p.; Notifica ai sensi dell'art. 148 comma 2 bis c.p.p.; Notifica tramite SNT).
Template modificato: 
SIEP_MA_REVO_AFFI_SOSP.rtf |  |
| 20220907011 | Nessuna | L’ufficio richiede l’allineamento delle due estrazioni, per i procedimenti privi di oggetto occorre che siano differenziati  con una dicitura diversa “Oggetto non presente” o riportare un trattino. La stessa integrazione va fatta nella Funzione “Ricerca Procedimento SIGE per Estremi Atto” selezione “oggetto”. | Per la risoluzione della problematica, per i procedimenti privi di oggetto, è stata aggiunta la dicitura  'Oggetto non presente'. | Il problema era legato al fatto che non era gestita l’estrazione di fascicoli privi di oggetto/i.
Classe modificata:
siap.sige.fascicolo.dao.FascicoloSigeSqlDAO.java |  |
| 20220907012 | Nessuna | L’ufficio segnala che nell’effettuare l’estrazione per singola voce “Applicazione indulto”, il sistema visualizza solamente i procedimenti solamente per  singola voce. | Per la risoluzione della problematica è stato corretto, in fase di creazione del foglio statistica, il mancato reset degli oggetti sui procedimenti privi di oggetto. | Il problema era legato al fatto che non era gestita l’estrazione di fascicoli privi di oggetto/i; inoltre Il modulo che ricostruiva la lista oggetti non resettava correttamente la variabile con gli oggetti fascicolo se il fascicolo corrente ne era privo. Risultato: al fascicolo privo di oggetti venivano associati gli oggetti del fascicolo che lo precedeva.
Classi modificate:
siap.sige.fascicolo.controller.FascicoloSigeController.java
siap.sige.fascicolo.dao.FascicoloSigeSqlDAO.java |  |
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
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20220916-Piano_di_Rilascio_SIES_v.12.4.23.0.docx
SIUT-SIES-PT-1.0-20220916-Piano_dei_Test_SIES_v.12.4.23.0.docx
SIUT-SIES-CT-1.0-20220916-Allegato_al_piano_test_SIES_v.12.4.23.0.xls |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| aggiorna_db.zip | Database | Script:
Aggiornamento versione SIES in tabella “VERSIONE” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| template.zip | Template | Template aggiornato:
SIUS_DE_ESTINZIONESS.rtf
SIEP_MA_REVO_AFFI_SOSP.rtf |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.22.0.
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
Creare sul server DB una cartella V_12_4_23_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_4_23_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_23_0 tramite il comando:
chmod 777 V_12_4_23_0
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx
Nella cartella appena creata (V_12_4_23_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_4_23_0/log/ in cui si può constatare l’esito dell’esecuzione.
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
Copiare i files contenuti nella cartella template\sius\de
nella cartella “/var/SIES/template/sius/de” sovrascrivendo quelli precedenti;
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