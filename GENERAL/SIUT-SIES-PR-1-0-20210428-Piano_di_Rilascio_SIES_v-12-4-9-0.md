---
uniqueName: siut-sies-pr-1-0-20210428-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20210428 Piano di Rilascio SIES v 12 4 9 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20210428-Piano_di_Rilascio_SIES_v.12.4.9.0

> **File originale:** `RILASCIO_12.4.9.0/SIUT-SIES-PR-1.0-20210428-Piano_di_Rilascio_SIES_v.12.4.9.0.docx`  
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
| Data approvazione | 28/04/2021 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 28/04/2021 | Prima Emissione |  |


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
6.4	Attività di configurazione	16
6.5	Attività di post-installazione	16


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio del sistema SIES.
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.9.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.4.9.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.

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
| 202103180118 | Procura della Repubblica presso il Tribunale di Varese | L’ufficio segnala che la Procura della Repubblica di Varese sta cercando di cumulare il proprio fascicolo SIEP 2021/22 con il fascicolo SIEP 2020/91 della Procura di Modena, ma al momento della presa in carico del procedimento di Modena si riceve l'errore: "Si è verificato un errore durante il caricamento dell'Atto pervenuto. Riprovare in seguito". Dopo correzione della posizione giuridica del soggetto, il procedimento è stato re-inviato da Modena a Varese. | Per la risoluzione della problematica si è intervenuti con la correzione della Store Procedure per gestire la cancellazione di ALTRA_CAUSA sulla PULISCI_EVENTO. Provava a cancellare tutti i record del fascicolo e non solo quelli collegabili all'evento. | E’ stato modificato il package “PULISCI_ALTRE_BDI” correggendo l’errato comportamento della procedura “PULISCI_EVENTO”. |  |
| 20210322016 | Corte d'Appello di Torino | L'Ufficio segnala che il fascicolo 593/2020 è il fascicolo che unifica in se il 673/2020 e non viceversa. Non si riesce a cancellare il provvedimento di unificazione presente nel 593/2020. Si ha la necessità di fare esattamente l'unificazione in senso contrario. | Per la risoluzione della problematica si è intervenuti con la correzione della cancellazione del Verbale e del Decreto di Unificazione. Corretta la gestione Unificato/Unificante poiché venivano invertiti rispetto a quanto indicato dall'utente in fase di unificazione. | Sono state modificate le classi:
siap.sige.decretounificazione.action.ActLoadConfermaInserisciDecretoUnificazioneSige.java
siap.sige.decretounificazione.action.ActRicercaFSPUnificazioneSige.java
siap.sige.decretounificazione.controller.DecretoUnificazioneSigeController.java
siap.sige.unificazione.action.ActLoadConfermaInserisciVerbaleUnificazioneSige.java
correggendo l’errato comportamento segnalato dall’utente. |  |
| 20210324012 | Procura della Repubblica presso il Tribunale di Torino | L’ufficio segnala che - su ogni fascicolo - la stampa del foglio complementare per il casellario a corredo dell'ordine di esecuzione sospeso presenta, all'interno del medesimo form, più FONT, con conseguente aspetto sciatto della stampa. Si consiglia, per omogeneità, di usare ovunque il FONT Times New Roman. Inoltre è stato emesso il salto pagina, per cui la sola ultima riga compare nella seconda (nel caso indicato, settima sul totale) pagina. | Per la risoluzione della problematica si è intervenuti con la correzione del template indicato. | E’ stato modificato il template:
SIEP_LS_OLQNI.rtf
In cui è stato uniformato il font. |  |
| 20210324015 | Tribunale di Torino | L’ufficio segnala che l'utente nel cercare i procedimenti presenti a sistema e sui quali è stato presentato ricorso/opposizione in fase di ricerca è impossibilitato a verificare la quantità dei procedimenti sui quali pende un ricorso. | Per la risoluzione della problematica si è intervenuti con la modifica della classe in cui vengono estratti i procedimenti con l’aggiunta della gestione dei record nella tabella “IMPUGNAZIONE_SIGE” con “COD_TENORE_DECISIONE” pari a “null”. | E’ stata modificata la classe: 
siap.sige.fascicolo.dao.FascicoloSigeSqlDAO.java
in cui è stata modificata la query di estrazione dei procedimenti sui quali pende un ricorso. |  |
| 20210329018 | Procura della Repubblica presso il Tribunale di Torino | L’ufficio segnala che Il modulo stampa, "SIEP_ARC_FOGLIO_COMP_ESP", non riporta i periodi di custodia cautelare sofferta dal soggetto minorenne: collocamento in comunità e permanenza in casa. | Per la risoluzione della problematica si è intervenuti con la aggiunta nella stampa di tutte le misure cautelari computabili come presenti nello stato esecuzione. | E’ stato modificato il template:
SIEP_ARC_FOGLIO_COMP_ESP.rtf
In cui è stata modificata la gestione delle misure cautelari computabili. |  |
| 202104010118 | Corte d'Appello di Napoli | L’ufficio segnala un paio di problemi: il primo riguarda il monitoraggio dei ricorsi registrati. Infatti non sembra possibile effettuare la ricerca di quanti ricorsi/opposizione siano stati registrati. In particolare, interrogando il sistema circa il numero dei ricorsi presentati nell’anno (intervallo date arrivo in cancelleria) ed inserendo la data iniziale e quella finale, impostando la data di validazione che interessa, il sistema non trova nessun procedimento,  nonostante siano stati registrati ricorsi/opposizioni  nell’anno.
Il secondo riguarda il monitoraggio dei fogli complementari. Infatti  interrogando il sige  circa la pendenza dei fogli complementari, il sistema rileva, quali pendenti e da compilare, anche quei procedimenti definiti con ordinanza di rigetto o di inammissibilità, probabilmente collegando la ricerca all’oggetto del procedimento e non all’esito. | Per la risoluzione della problematica si è intervenuti con la modifica della classe in cui vengono estratti i procedimenti con l’aggiunta della gestione dei record nella tabella “IMPUGNAZIONE_SIGE” con “COD_TENORE_DECISIONE” pari a “null”. | E’ stata modificata la classe: 
siap.sige.fascicolo.dao.FascicoloSigeSqlDAO.java
in cui è stata modificata la query di estrazione dei procedimenti sui quali pende un ricorso. |  |
| 20210408012 | DGSIA - Referente Applicativo | L’utente segnala che la funzione di invio dei FC da SIEP deve essere disattivata per tutti i casi possibili, in attesa di una futura sperimentazione in accordo con il casellario stesso. Da Catania arriva la segnalazione anomala di possibilità di invio. | Per la risoluzione della problematica si è intervenuti con il rilascio di uno script DB che invalida la profilatura per la funzione con ID=90110640. | E’ stata aggiornata la tabella “funzione_profilo” in cui per il record con identificativo pari a 90110640 è stata valorizzata la data di fina validità. |  |
| 202104080110 | DGSIA - Referente Applicativo | L’utente segnala che nel documento del modello logico dei dati, alla pag. 109 è descritta la tabella “FUNZIONE”. In essa il Campo “COD_TIPO_FUNZIONE” è descritto nel seguente modo: "Codice che identifica l'appartenenza al menù gerarchico o al contesto. Deriva da dominio". Non è chiaro cosa significhi tale descrizione né è chiaro come poter recuperare il significato dei valori che tale campo può assumere (es. I, F,...). | Per la risoluzione della problematica si è intervenuti con la correzione del documento “SIGI_PNL_ML_20210423_1.6_Modello dei Dati_SIES”, aggiornando le descrizioni COD_TIPO_FUNZIONE della tabella FUNZIONE e COD_TIPO_VISUALIZZAZIONE della tabella RELAZIONE_FUNZIONE presenti nel documento e rilasciando due script per il database. | Sono stati rilasciati due script per l’aggiornamento della tabella “CG_REF_CODES” ed in particolare dei domini “TIPO_FUNZIONE” e “TIPO_VISUALIZZAZIONE” aggiornandoli con tutti i possibili valori descritti nel documento del modello logico dei dati. |  |
| 20210416017 (AVVOCATURA SIUS) | DGSIA - Referente Applicativo | L’utente segnala che le informazioni visibili siano sempre le stesse, qualunque funzione venga utilizzata (ricerca per procedimento, avvisi, ricerca per soggetto) e la visibilità deve avvenire al momento stabilito in fase di analisi. Per ora, le incongruenze emerse riguardano la  ricerca per soggetto, nel momento in cui sia visualizzato l'elenco dei procedimenti  a carico di un soggetto specifico.
Le informazioni visibili devono essere solo quelle delle colonne indicate nell'elenco e devono essere visibili in modo coerente con la visibilità delle informazioni raggiungibili sia tramite la funzione "avvisi" sia tramite la funzione "ricerca per numero procedimento". | Per la risoluzione della problematica si è intervenuti con la modifica della classe in cui vengono estratti i dati da inviare al sistema chiamante. | E’ stata modificata la classe:
FascicoloSiusSoggettoSqlDAO.java
modificando la query preposta ad inviare tramite web service i dati al sistema “AVVOCATURA”; in questo caso viene inviata l’informazione circa i procedimenti a carico di un dato soggetto. |  |
| 202104270113 (AVVOCATURA SIUS) | DGSIA - Referente Applicativo | L’utente segnala l'errore in visualizzazione di un decreto non ancora depositato. | Per la risoluzione della problematica si è intervenuti con la modifica della classe in cui vengono estratti i dati da inviare al sistema chiamante. | Sono state modificate la classi:
ProcedimentiDelSoggettoMapper.java
FascicoloSiusSoggettoSqlDAO.java
modificando la query preposta ad inviare tramite web service i dati al sistema “AVVOCATURA”; in questo caso viene inviata l’informazione circa i procedimenti a carico di un dato soggetto. |  |
| Note-osservazioni | Per il ticket 20210329018, l’utente aveva segnalato anche l’assenza del periodo espiato in detenzione. La visualizzazione del periodo espiato in detenzione (provvedimento di sospensione) è invece da considerarsi MEV perché il template non prevede il caricamento e visualizzazione dei periodi espiati a seguito di provvedimenti, siano essi interruttivi come segnalato nel ticket (sospensioni) siano essi computi di misure cautelari caricati con provvedimento (evento raro ma possibile). Il template non li ha mai previsti. Si tratta di realizzare una apposita sezione dell'xml di stampa dove ricostruire tuti i periodi di pena espiati in vario modo. A tal proposito è stata aperto ticket MEV (20210401014) collegato al suddetto ticket. | Per il ticket 20210329018, l’utente aveva segnalato anche l’assenza del periodo espiato in detenzione. La visualizzazione del periodo espiato in detenzione (provvedimento di sospensione) è invece da considerarsi MEV perché il template non prevede il caricamento e visualizzazione dei periodi espiati a seguito di provvedimenti, siano essi interruttivi come segnalato nel ticket (sospensioni) siano essi computi di misure cautelari caricati con provvedimento (evento raro ma possibile). Il template non li ha mai previsti. Si tratta di realizzare una apposita sezione dell'xml di stampa dove ricostruire tuti i periodi di pena espiati in vario modo. A tal proposito è stata aperto ticket MEV (20210401014) collegato al suddetto ticket. | Per il ticket 20210329018, l’utente aveva segnalato anche l’assenza del periodo espiato in detenzione. La visualizzazione del periodo espiato in detenzione (provvedimento di sospensione) è invece da considerarsi MEV perché il template non prevede il caricamento e visualizzazione dei periodi espiati a seguito di provvedimenti, siano essi interruttivi come segnalato nel ticket (sospensioni) siano essi computi di misure cautelari caricati con provvedimento (evento raro ma possibile). Il template non li ha mai previsti. Si tratta di realizzare una apposita sezione dell'xml di stampa dove ricostruire tuti i periodi di pena espiati in vario modo. A tal proposito è stata aperto ticket MEV (20210401014) collegato al suddetto ticket. | Per il ticket 20210329018, l’utente aveva segnalato anche l’assenza del periodo espiato in detenzione. La visualizzazione del periodo espiato in detenzione (provvedimento di sospensione) è invece da considerarsi MEV perché il template non prevede il caricamento e visualizzazione dei periodi espiati a seguito di provvedimenti, siano essi interruttivi come segnalato nel ticket (sospensioni) siano essi computi di misure cautelari caricati con provvedimento (evento raro ma possibile). Il template non li ha mai previsti. Si tratta di realizzare una apposita sezione dell'xml di stampa dove ricostruire tuti i periodi di pena espiati in vario modo. A tal proposito è stata aperto ticket MEV (20210401014) collegato al suddetto ticket. | Per il ticket 20210329018, l’utente aveva segnalato anche l’assenza del periodo espiato in detenzione. La visualizzazione del periodo espiato in detenzione (provvedimento di sospensione) è invece da considerarsi MEV perché il template non prevede il caricamento e visualizzazione dei periodi espiati a seguito di provvedimenti, siano essi interruttivi come segnalato nel ticket (sospensioni) siano essi computi di misure cautelari caricati con provvedimento (evento raro ma possibile). Il template non li ha mai previsti. Si tratta di realizzare una apposita sezione dell'xml di stampa dove ricostruire tuti i periodi di pena espiati in vario modo. A tal proposito è stata aperto ticket MEV (20210401014) collegato al suddetto ticket. |
| Note-osservazioni | Per il ticket 202104010118, in merito al secondo punto, si precisa che è da considerarsi una MEV (ticket 202104140118 collegato ad esso). In particolare, sulla MEV l’utente ha indicato le seguenti migliorative da sottoporre all’amministrazione:
la funzione Ricerca Fogli Complementari, presente nel menu Monitoraggio/Ricerche/Estrazione Dati, produce al termine della Ricerca un file Excel. Questo file contiene il foglio Provvedimenti privi FC a cui bisognerebbe apportare le seguenti implementazioni:
sia sempre riportata la descrizione del Provvedimento,
sia aggiunta una colonna con l'esito dello stesso, in modo da consentire all'ufficio di valutare se per quel provvedimento si debba effettivamente procedere alla compilazione del Foglio Complementare. | Per il ticket 202104010118, in merito al secondo punto, si precisa che è da considerarsi una MEV (ticket 202104140118 collegato ad esso). In particolare, sulla MEV l’utente ha indicato le seguenti migliorative da sottoporre all’amministrazione:
la funzione Ricerca Fogli Complementari, presente nel menu Monitoraggio/Ricerche/Estrazione Dati, produce al termine della Ricerca un file Excel. Questo file contiene il foglio Provvedimenti privi FC a cui bisognerebbe apportare le seguenti implementazioni:
sia sempre riportata la descrizione del Provvedimento,
sia aggiunta una colonna con l'esito dello stesso, in modo da consentire all'ufficio di valutare se per quel provvedimento si debba effettivamente procedere alla compilazione del Foglio Complementare. | Per il ticket 202104010118, in merito al secondo punto, si precisa che è da considerarsi una MEV (ticket 202104140118 collegato ad esso). In particolare, sulla MEV l’utente ha indicato le seguenti migliorative da sottoporre all’amministrazione:
la funzione Ricerca Fogli Complementari, presente nel menu Monitoraggio/Ricerche/Estrazione Dati, produce al termine della Ricerca un file Excel. Questo file contiene il foglio Provvedimenti privi FC a cui bisognerebbe apportare le seguenti implementazioni:
sia sempre riportata la descrizione del Provvedimento,
sia aggiunta una colonna con l'esito dello stesso, in modo da consentire all'ufficio di valutare se per quel provvedimento si debba effettivamente procedere alla compilazione del Foglio Complementare. | Per il ticket 202104010118, in merito al secondo punto, si precisa che è da considerarsi una MEV (ticket 202104140118 collegato ad esso). In particolare, sulla MEV l’utente ha indicato le seguenti migliorative da sottoporre all’amministrazione:
la funzione Ricerca Fogli Complementari, presente nel menu Monitoraggio/Ricerche/Estrazione Dati, produce al termine della Ricerca un file Excel. Questo file contiene il foglio Provvedimenti privi FC a cui bisognerebbe apportare le seguenti implementazioni:
sia sempre riportata la descrizione del Provvedimento,
sia aggiunta una colonna con l'esito dello stesso, in modo da consentire all'ufficio di valutare se per quel provvedimento si debba effettivamente procedere alla compilazione del Foglio Complementare. | Per il ticket 202104010118, in merito al secondo punto, si precisa che è da considerarsi una MEV (ticket 202104140118 collegato ad esso). In particolare, sulla MEV l’utente ha indicato le seguenti migliorative da sottoporre all’amministrazione:
la funzione Ricerca Fogli Complementari, presente nel menu Monitoraggio/Ricerche/Estrazione Dati, produce al termine della Ricerca un file Excel. Questo file contiene il foglio Provvedimenti privi FC a cui bisognerebbe apportare le seguenti implementazioni:
sia sempre riportata la descrizione del Provvedimento,
sia aggiunta una colonna con l'esito dello stesso, in modo da consentire all'ufficio di valutare se per quel provvedimento si debba effettivamente procedere alla compilazione del Foglio Complementare. |

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
Aggiornamento Procedura “PULISCI_ALTRE_BDI”
Aggiornamento record in tabella “FUNZIONE_PROFILO”
Aggiornamento Dominio “TIPO_FUNZIONE” in tabella “CG_REF_CODES”
Aggiornamento Dominio “TIPO_VISUALIZZAZIONE” in tabella “CG_REF_CODES” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| template.zip | Template | Template aggiornati:
SIEP_LS_OLQNI.rtf
SIEP_ARC_FOGLIO_COMP_ESP.rtf |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20210428-Piano_di_Rilascio_SIES_v.12.4.9.0.docx
SIUT-SIES-PT-1.0-20210428-Piano_dei_Test_SIES_v.12.4.9.0.docx
SIUT-SIES-CT-1.0-20210428-Allegato_al_piano_test_SIES_v.12.4.9.0.xls
SIGI_PNL_ML_20210423_1.6_Modello dei Dati_SIES.pdf |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.8.0.
Attenzione! La risoluzione del ticket 20210416017 che riguarda il dialogo tra i sistemi “AVVOCATURA SIUS” e “SIES”, comporta l’installazione contemporanea dei due applicativi:
AVVOCATURA SIUS (avvocatura.war, presente nell’apposito percorso “/SIUT/06 - Rilasci Software/SIES/Rilascio AVVOCATURA 2.6.0.0 2021-04-28”), versione 2.6.0.0
SIES (sies.war, presente nell’apposito percorso “/SIUT/06 - Rilasci Software/SIES/Rilascio SIES 12.4.9.0 2021-04-28”), versione 12.4.9.0
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
Creare sul server DB una cartella V_12_4_9_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_4_9_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_9_0 tramite il comando:
chmod 777 V_12_4_9_0

In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx

Nella cartella appena creata (V_12_4_9_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_4_9_0/log/ in cui si può constatare l’esito dell’esecuzione.

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
Copiare i files contenuti nella cartella template\siep\arc
nella cartella “/var/SIES/template/siep/arc” sovrascrivendo quelli precedenti;
Copiare i files contenuti nella cartella template\siep\ls
nella cartella “/var/SIES/template/siep/ls” sovrascrivendo quelli precedenti;

Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 2.b e 2.e. All’avvio, infatti, tali cartelle verranno ricreate.

Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.