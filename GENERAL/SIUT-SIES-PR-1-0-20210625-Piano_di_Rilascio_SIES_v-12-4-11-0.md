---
uniqueName: siut-sies-pr-1-0-20210625-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20210625 Piano di Rilascio SIES v 12 4 11 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20210625-Piano_di_Rilascio_SIES_v.12.4.11.0

> **File originale:** `RILASCIO_12.4.11.0/SIUT-SIES-PR-1.0-20210625-Piano_di_Rilascio_SIES_v.12.4.11.0.docx`  
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
| Data approvazione | 25/06/2021 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 25/06/2021 | Prima Emissione |  |


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
6.4	Attività di configurazione	17
6.5	Attività di post-installazione	17


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio del sistema SIES.
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.11.0 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.4.11.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.

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
| 20210514015 | Procura della Repubblica Presso il Tribunale di Torino | L’Ufficio chiede la risoluzione del problema di cui in oggetto: “Errore in Ricerca procedimento Sige per titolo esecutivo”. | Per la risoluzione della problematica si è intervenuti con l’aggiunta del test su assenza numero registro GUP e CAPSM sulla sentenza. | E’ stata modificata la classe:
siap.sige.sentenza.RicercaSentenzaPerSige.jsp
in cui è stato implementato il controllo sui campi “NumeroRegeGup” e “getNumeroRegeCapsm” al fine di evitare errori di NullPointer. |  |
| 20210514016 | Procura della Repubblica Presso il Tribunale di Torino | L'Ufficio chiede la risoluzione del problema sui Fogli complementari Sige e la mancata visibilità degli oggetti. | Per la risoluzione della problematica si è intervenuti con la gestione della colonna "Provvedimento" nella quale è stata riportata la descrizione dell'Oggetto invece che dell'evento, assente per la maggior parte dei provvedimenti SIGE. | Sono state modificate le classi:
siap.sige.statistiche.StatisticheFogliComplementari.jsp
in cui è stata modificata la visualizzazione dei risultati della ricerca;
siap.sige.statistiche.dao.StatisticheFogliComplementariSqlDAO.java
in cui è stata modificata la query che recupera la descrizione dell'oggetto dall'evento dove il codice motivo era quasi sempre non valorizzato; ora la query lo recupera dal dominio “tenore”. |  |
| 20210514018 | Procura della Repubblica Presso il Tribunale di Torino | L’ufficio segnala che quando iscrive un soggetto nel sottosistema Sige valorizzando i campi nome e cognome della madre, nella risultante pagina di dettaglio tali campi non sono riportati correttamente. | Per la risoluzione della problematica si è intervenuti con la correzione della pagina di dettaglio presentata dopo l’iscrizione di un soggetto per il sottosistema Sige. | E’ stata modificata la classe:
siap.sico.soggetto.DettaglioSoggetto.jsp
nella quale i campi nome e cognome della madre sono stati separati su due righe differenti. |  |
| 202105200113 | Ufficio di Sorveglianza di Milano | L’ufficio segnala che dopo aver preso in carico un procedimento SIEP, se si tenta di utilizzare la funzione Stato Esecuzione dal menu principale si ottengono due risultati:
1) Richiesta atti per competenza (per emissione provvedimento cumulo);
2) Provvedimento di unificazione di pene concorrenti prosecuzione dell'espiazione nel regime attuale di espiazione (art. 51 Bis legge 354/75 affidamento in prova).
Quando si tenta di stampare il provvedimento di unificazione si ottiene l'errore:
org.apache.tika.exception.TikaException. Se invece si tenta di visualizzare il provvedimento di cumulo si ottiene l'errore: “Funzione 'siap.siep.modulocumulo.action.ActLoadDettaglioProvvedimentoCumulo' non disponibile per il profilo abilitato!”. | Per la risoluzione della problematica si è intervenuti con il rilascio di uno script per il database. | E’ stato rilasciato il file “202105200113.sql” che consente di ampliare la possibilità di poter consultare il dettaglio del provvedimento di cumulo che finora era solo associato ai profili 4,40,50.
Tale script consente di abilitare la funzione ‘siap.siep.modulocumulo.action.ActLoadDettaglioProvvedimentoCumulo' anche ai profili TDS e UDS ed al profilo di sola lettura dell'esecuzione. |  |
| 20210521012 | Procura della Repubblica Presso il Tribunale di Torino | L’ufficio segnala che nell'inserire la data di spedizione, diversa da quella di creazione del documento, il sistema ha poi riconvertito la data in quella del provvedimento, di fatto alterando la variazione operata. | Per la risoluzione della problematica si è intervenuti con la correzione della funzione di inserimento e dettaglio dei provvedimenti di Ordine di scarcerazione per Liberazione Anticipata da detenuto ed in Misura, poiché inserivano il campo Data Trasmissione della form nel campo "sbagliato" ovvero su “EVENTO.DATA_TRASMISSIONE_ATTI“ invece di “NOTIFICA.DATA_INVO” come gli altri provvedimenti. La funzione di Modifica Magistrato legge e scrive la data trasmissione da “NOTIFICA_DATA_INVIO” per cui falliva l'aggiornamento. Per l'Ordine di scarcerazione per Liberazione Anticipata in Misura Alternativa inoltre il sistema ignorava completamente il campo Data Trasmissione della form. | Sono state modificate le classi:
siap.siep.ordinescarcerazione.action.ActInserisciOSLiberazioneAnticipata.java
in cui è stata impostata correttamente la data di invio;
siap.siep.ordinescarcerazione.DettaglioOSLiberazioneAnticipata.jsp
in cui alla data trasmissione atti è stata sostituita la data di invio;
siap.siep.ordinescarcerazione.action.ActInserisciOSLiberazioneAnticipataMA.java
in cui è stata impostata correttamente la data di invio. |  |
| 202105240111 | Ufficio di Sorveglianza di Milano | L’ufficio segnala che durante la presa in carico di un procedimento di un'altra BD si ottiene l'errore "ERRORE GENERICO Impossibile inserire Record Sospensione!". | Per la risoluzione della problematica si è intervenuti con la modifica alla funzione di trasferimento per evitare di trasferire record SOSPENSIONE non collegati ad eventi e pene validate. | Sono state modificate le classi:
siap.siep.sospensione.dao.SospensioneSqlDAO.java
siap.siep.sospensione.controller.SospensioneController.java
in cui è stato modificato il metodo che recupera i record “SOSPENSIONE” da trasferire. Esso infatti recuperava tutte le “SOSPENSIONI” collegate al fascicolo indipendentemente se erano collegate a pene residue ed eventi validati. Aggiunta join con le tabelle “PENA_RESIDUA” ed “EVENTO” e test sul campo “FLAG_VALIDATO". |  |
| 20210526011 | Procura della Repubblica presso il Tribunale di Messina | L’ufficio segnala che al momento dell'Archiviazione di un Fascicolo: effettuato il visto del PM, nel passaggio di archiviazione vero e proprio nella generazione del foglio complementare, da trasmettere al casellario, il sistema NON riporta nel documento le date di inizio e fine espiazione pena, che invece sono presenti a sistema. | Per la risoluzione della problematica si è intervenuti con il rilascio del template opportunamente modificato. | E’ stato rilasciato il documento “SIEP_ARC_FOGLIO_COMP_ESP.rtf” in cui è stata aggiunta al suo interno la gestione della posizione giuridica segnalata dall’ufficio (04 - arresti in comma 10). |  |
| 20210531014 | Corte d’Appello di Firenze | L’ufficio segnala che l'elaborazione della statistica, dei procedimenti SIEP di classe IV, pendenti, genera errore. Selezionando Statistiche/Monitoraggio-Statistiche: Estrazione Dati - Classe Procedimento IV - Procedimenti Pendenti nel Periodo, per ogni periodo selezionato, il sistema restituisce il messaggio: Errore nell'elaborazione dei dati presenti nel database! | Per la risoluzione della problematica si è intervenuti con la modifica delle funzioni di estrazione dati per gestire un numero elevato di risultati. | Sono state modificate le classi:
siap.siep.statis.dao.StatisticheMSSqlDAO.java
src.siap.siep.statis.controller.StatisticheMSController.java
src.siap.siep.statis.model.StatisticheMSModel.java
in cui è stato verificato che le statistiche SIEP per i fascicoli di classe IV - Riepilogo Iscrizioni e Tipologia Misura - Procedimenti Pendenti nel Periodo, facevano uso dell'istruzione “LISTAGG” per aggregare il numero di fascicolo estratti dalle query. Tale funzione Oracle ha un limite di 4000 caratteri ed andava in overflow. Corrette quindi le 2 funzioni di ricerca per estrarre la lista non aggregata dei fascicoli. |  |
| 202106080116 | Procura della Repubblica Presso il Tribunale di Torino | L’ufficio richiede di correggere il testo motivazione revoca beneficio nel template in: “art. 168 primo comma n. 2 c.p. Revoca Beneficio ex art. 168 secondo comma c.p. Revoca Consumazione di un delitto in epoca anteriore alla data di passaggio in giudicato della condanna condizionalmente sospesa la cui pena cumulata superi i limiti di cui all'art. 163 c.p.”. | Per la risoluzione della problematica si è intervenuti con il rilascio del template opportunamente modificato. | E’ stato rilasciato il documento “RichiestePmInCumuloRevocaBenefici.rtf” in cui è stata modificata la dicitura: "Dispone, in via provvisoria, la revoca del beneficio, prima che sia definitivamente ordinato con provvedimento del giudice dell’esecuzione"
in
"Dispone, in via provvisoria, la revoca del beneficio, prima che sia definitivamente ordinata con provvedimento del giudice dell’esecuzione". |  |
| 20210610017 | Procura della Repubblica Presso il Tribunale di Torino | L’ufficio segnala un errore nel contenuto del template che allega al ticket. | Per la risoluzione della problematica si è intervenuti con il rilascio del template opportunamente modificato. | E’ stato rilasciato il documento “SIGE_OR_CONFLCOMPETENZA” in cui sono stati eliminati alcuni caratteri “sporchi” che conteneva ed è stata sistemata la formattazione di una tabella non formattata correttamente al suo interno. |  |
| 20210615018 | Procura della Repubblica Presso il Tribunale di Torino | L’ufficio segnala che Il sistema nel prendere in carico gli atti pervenuti da altra base dati fuori distretto va in errore: “Exception di altro tipo:
org.apache.jasper.JasperException: java.lang.NullPointerException”. | Per la risoluzione della problematica si è intervenuti con la correzione del controllo sulla presenza del titolo in istruttoria nel caso che fosse stato iscritto manualmente senza indicare il procedimento. | E’ stata modificata la classe:
siap.siep.presaincarico.DettaglioPresaincaricoCompetenzaRicevuta.jsp
in cui è stata gestito il caso in cui un eventuale titolo già in istruttoria era privo di provvedimento (iscrizione manuale). |  |
| 20210618011 | Tribunale di Sorveglianza di Catania | L’ufficio segnala che nella pagina in cui compare l'elenco delle udienze in "Funzioni amministrative" se il collegio è composto dal Presidente e due magistrati relatori, il secondo relatore non compare nella stampa dell'elenco udienze. | Per la risoluzione della problematica si è intervenuti con la modifica della classe interessata per visualizzare tutti i Giudici Relatori. | E’ stata modificata la classe:
siap.sius.udienza.RicercaUdienza.jsp
in cui nella funzione di Ricerca Udienza SIUS, nella tabella dei risultati, veniva visualizzato un solo Giudice relatore anche se ne erano presenti 2. E’ stata quindi aggiunta la visualizzazione del secondo Giudice Relatore. |  |
| Note-osservazioni | Il ticket 20210531013 (fuori da questa lista) contiene due problematiche già trattate in precedenti ticket: 20210514015 descritto nell’elenco di cui sopra, e 20210514014 trattato come MEV. | Il ticket 20210531013 (fuori da questa lista) contiene due problematiche già trattate in precedenti ticket: 20210514015 descritto nell’elenco di cui sopra, e 20210514014 trattato come MEV. | Il ticket 20210531013 (fuori da questa lista) contiene due problematiche già trattate in precedenti ticket: 20210514015 descritto nell’elenco di cui sopra, e 20210514014 trattato come MEV. | Il ticket 20210531013 (fuori da questa lista) contiene due problematiche già trattate in precedenti ticket: 20210514015 descritto nell’elenco di cui sopra, e 20210514014 trattato come MEV. | Il ticket 20210531013 (fuori da questa lista) contiene due problematiche già trattate in precedenti ticket: 20210514015 descritto nell’elenco di cui sopra, e 20210514014 trattato come MEV. |

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
| c. Specifiche Dati (Schema Concettuale, Schema Logico e Schema Fisico) | SIGI_PNL_ML_20210521_1.7_Modello dei Dati_SIES.pdf | SIUT > 06 - Rilasci Software > SIES > Rilascio SIES 12.4.11.0 2021-06-25 > Documentazione > documentazione.zip |
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
Aggiornamento tabella “FUNZIONE_PROFILO” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| template.zip | Template | Template aggiornati:
SIEP_ARC_FOGLIO_COMP_ESP.rtf
RichiestePmInCumuloRevocaBenefici.rtf
SIGE_OR_CONFLCOMPETENZA.rtf |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20210625-Piano_di_Rilascio_SIES_v.12.4.11.0.docx
SIUT-SIES-PT-1.0-20210625-Piano_dei_Test_SIES_v.12.4.11.0.docx
SIUT-SIES-CT-1.0-20210625-Allegato_al_piano_test_SIES_v.12.4.11.0.xls |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.10.0.
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
Creare sul server DB una cartella V_12_4_11_0 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_4_11_0/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_11_0 tramite il comando:
chmod 777 V_12_4_11_0

In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx

Nella cartella appena creata (V_12_4_11_0), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_4_11_0/log/ in cui si può constatare l’esito dell’esecuzione.

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
Copiare i files contenuti nella cartella template\siep\arc
nella cartella “/var/SIES/template/siep/arc” sovrascrivendo quelli precedenti;
Copiare i files contenuti nella cartella template\sige\or
nella cartella “/var/SIES/template/sige/or” sovrascrivendo quelli precedenti;

Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 2.b e 2.e. All’avvio, infatti, tali cartelle verranno ricreate.

Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.