---
uniqueName: siut-sies-pr-1-0-20200706-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20200706 Piano di Rilascio SIES v 12 3 0 2"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20200706-Piano_di_Rilascio_SIES_v.12.3.0.2

> **File originale:** `RILASCIO_12.3.0.2/SIUT-SIES-PR-1.0-20200706-Piano_di_Rilascio_SIES_v.12.3.0.2.docx`  
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
| Data approvazione | 06/07/2020 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 06/07/2020 | Prima Emissione |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Pasquale Lamattina | RTI |  | Referente Tecnico |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Fabio Mazzocchi | RTI |  | Responsabile Manutenzione Correttiva |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Responsabile PMO |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Edoardo Lamuraglia | RTI |  | Referente qualità |
| Francesco Rosati | RTI |  | Referente qualità |
| Andrea Castorino
Alessandro Lanari | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |
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
4.1	Riferimenti Anomalia (MAC)	8
4.2	Riferimenti ChangeRequest (ADE/MEV)	22
4.2.1	Documenti a corredo della sessione di verifica conformità	22
5	Dettaglio degli elementi oggetto del rilascio	23
6	Installazione	24
6.1	Prerequisiti	24
6.2	Attività di preinstallazione	24
6.3	Attività di installazione	24
6.3.1	Installazione lato DB	24
6.3.1.1	Esecuzione script	24
6.3.2	Installazione applicazione	25
6.3.2.1	Deploy Applicazione	25
6.4	Attività di configurazione	26
6.5	Attività di post-installazione	26


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio del sistema SIES.
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.3.0.2 di SIES.
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
Il presente documento descrive il piano di rilascio di SIES 12.3.0.2 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.

Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.
# Identificazione degli elementi rilasciati
| Supporto | Oggetti: | Ver. | del |
| --- | --- | --- | --- |
| Portale fornitura | Rilascio SIES |  |  |
| Note-osservazioni |  |  |  |


# Riferimenti degli oggetti del rilascio
## Riferimenti Anomalia (MAC)
| Rif. Ticket OTRS | Sede
Ufficio | Descrizione segnalazione | Descrizione
intervento | Descrizione Tecnica | Manuali corretti |
| --- | --- | --- | --- | --- | --- |
| 20200508014 | Procura della Repubblica presso il Tribunale di Palermo | L’utente segnala che in fase di stampa di un provvedimento del PM di "Ordine Scarcerazione Nuova scadenza pena a seguito concessione Reclamo Risarcimento Danni D.L. 92/2014" il sistema restituisce un errore java. | L’intervento di correzione consiste nella gestione del codice motivo provvedimento mancante “9154”, in fase di stampa di un provvedimento "Ordine Scarcerazione Nuova scadenza pena a seguito concessione Reclamo Risarcimento Danni D.L. 92/2014”. | Nella classe java responsabile della stampa del template è stato inserito il codice (9154) mancante per i Reclami di concessione. |  |
| 20200610014 | Tribunale per i Minorenni di Messina | L’utente segnala che a seguito di modifica di un procedimento SIUS da contenuto ‘ESECUZIONE PRESSO DOMICILIO DELLA PENA DETENTIVA’ in contenuto ‘ESECUZIONE MISURE ALTERNATIVE’ il sistema genera un numero EMA divergente rispetto al fascicolo oggetto di modifica. | L’intervento di correzione consiste nella rettifica dell’azione di modifica su fascicoli con contenuto EMA. | Nel metodo java responsabile della modifica dell’entità fascicolo SIUS sono state introdotte delle rettifiche per la gestione degli EMA, EMS ed ESS. |  |
| 20200625012 | Procura della Repubblica presso il Tribunale di Cosenza | L’utente segnala che in fase di stampa di un provvedimento del PM di "Ordine Scarcerazione Nuova scadenza pena a seguito concessione Reclamo Risarcimento Danni D.L. 92/2014" il sistema restituisce un errore java. | L’intervento di correzione consiste nella gestione del codice motivo provvedimento mancante “9154”, in fase di stampa di un provvedimento "Ordine Scarcerazione Nuova scadenza pena a seguito concessione Reclamo Risarcimento Danni D.L. 92/2014”. | Nella classe java responsabile della stampa del template è stato inserito il codice (9154) mancante per i Reclami di concessione. |  |
| 20200625014 | Tribunale di Sorveglianza di Catanzaro | L'utente segnala che in fase di “emissione ordinanza” in materia di LIBERAZIONE ANTICIPATA, nonostante venga indicato il periodo relativo alla concessione di un beneficio da parte del Magistrato, nel prosieguo dello scarico, dopo la fase della validazione, il periodo indicato non compare né compaiono i giorni concessi. I dati non risultano visibili né nella pagina riepilogativa né sullo stampato associato. | Con l’intervento di correzione è stata rettificata l’invocazione del metodo java nella relativa classe che gestisce le ordinanze dell’UDS in relazione all’inserimento dei periodi di L.A. | Nella classe java responsabile dell'emissione di una ordinanza di liberazione anticipata è stata ripristinata la corretta invocazione del metodo "inserimento(..)". |  |
| 20200625017 | Procura della Repubblica presso il Tribunale di Catanzaro | L'utente segnala che nella funzione ‘Decisione del GE’, in corrispondenza del menù ‘Altre Ordinanze/Decreti’, nella combo-box dei contenuti, il sistema visualizza dei valori errati. | Con l’intervento di correzione si è proceduto al caricamento corretto della lista dei contenuti del Giudice dell’esecuzione. | In fase di inserimento di una annotazione provvedimento per una decisione del GE, il campo di tipo comboBox "Contenuto" seleziona i contenuti relativi alle autorità GE (Giudice Esecuzione). |  |
| 20200629012 | Procura della Repubblica presso il Tribunale di Verbania | L'utente segnala che nella funzione ‘Decisione del GE’, in corrispondenza del menù ‘Altre Ordinanze/Decreti’, nella combo-box dei contenuti, il sistema visualizza dei valori errati. | Con l’intervento di correzione si è proceduto al caricamento corretto della lista dei contenuti del Giudice dell’esecuzione. | In fase di inserimento di una annotazione provvedimento per una decisione del GE, il campo di tipo comboBox "Contenuto" seleziona i contenuti relativi alle autorità GE (Giudice Esecuzione). |  |
| 20200629015 | Ufficio di Sorveglianza di Alessandria | L'utente segnala che in fase di “emissione ordinanza” in materia di LIBERAZIONE ANTICIPATA, nonostante venga indicato il periodo relativo alla concessione di un beneficio da parte del Magistrato, nel prosieguo dello scarico, dopo la fase della validazione, il periodo indicato non compare né compaiono i giorni concessi. I dati non risultano visibili né nella pagina riepilogativa né sullo stampato associato. | Con l’intervento di correzione è stata rettificata l’invocazione del metodo java nella relativa classe che gestisce le ordinanze dell’UDS in relazione all’inserimento dei periodi di L.A. | Nella classe java responsabile dell'emissione di una ordinanza di liberazione anticipata è stata ripristinata la corretta invocazione del metodo "inserimento(..)". |  |
| 20200629016 | Procura Generale presso la Corte d’Appello di Napoli | L'utente segnala che nella funzione ‘Decisione del GE’, in corrispondenza del menù ‘Altre Ordinanze/Decreti’, nella combo-box dei contenuti, il sistema visualizza dei valori errati. | Con l’intervento di correzione si è proceduto al caricamento corretto della lista dei contenuti del Giudice dell’esecuzione. | In fase di inserimento di una annotazione provvedimento per una decisione del GE, il campo di tipo comboBox "Contenuto" seleziona i contenuti relativi alle autorità GE (Giudice Esecuzione). |  |
| 20200630017 | Procura della Repubblica presso il Tribunale di Lagonegro | L'utente segnala che in fase di stampa di un provvedimento NON VALIDATO di “Ordine Scarcerazione Nuova scadenza pena a seguito concessione Reclamo Risarcimento Danni D.L. 92/2014", il sistema restituisce un errore java. | L’intervento di correzione consiste nella gestione del codice motivo provvedimento mancante “9154”, in fase di stampa di un provvedimento "Ordine Scarcerazione Nuova scadenza pena a seguito concessione Reclamo Risarcimento Danni D.L. 92/2014”. | Nella classe java responsabile della stampa del template è stato inserito il codice (9154) mancante per i Reclami di concessione. |  |
| 20200701018 | Ufficio di Sorveglianza di Palermo | L'utente segnala che in fase di “emissione ordinanza” in materia di LIBERAZIONE ANTICIPATA o di CONVERSIONE PENA PECUNIARIA, nonostante venga indicato il periodo relativo alla concessione di un beneficio da parte del Magistrato, nel prosieguo dello scarico, dopo la fase della validazione, il periodo indicato non compare né compaiono i giorni concessi. I dati non risultano visibili né nella pagina riepilogativa né sullo stampato associato. | Con l’intervento di correzione è stata rettificata l’invocazione del metodo java nella relativa classe che gestisce le ordinanze dell’UDS in relazione all’inserimento dei periodi di L.A. | Nella classe java responsabile dell'emissione di una ordinanza di liberazione anticipata è stata ripristinata la corretta invocazione del metodo "inserimento(..)". |  |
| 20200702012 | Ufficio di Sorveglianza di Taranto | L'utente rileva le seguenti anomalie del sistema: 
1)    nella funzione deposito ordinanze di liberazione anticipata non memorizza i periodi indicati. 
2)    nell’iscrizione dei fascicoli di misura alternativa (EMA) il fascicolo iscritto si collega ad altro fascicolo rendendo impossibile le successive iscrizioni relative alle autorizzazioni.
3)    nell’iscrizione delle esecuzioni sanzioni sostitutive il sistema collega il procedimento ESS ad altro fascicolo rendendo impossibile le iscrizioni successive all’interno del fascicolo padre. | Per il punto 1, con l’intervento di correzione è stata rettificata l’invocazione del metodo java nella relativa classe che gestisce le ordinanze dell’UDS in relazione all’inserimento dei periodi di L.A.

.
Per i punti 2 e 3, l’intervento di correzione consiste nella rettifica dell’azione di modifica su fascicoli con contenuto EMA. | Per il punto 1, nella classe java responsabile dell'emissione di una ordinanza di liberazione anticipata è stata ripristinata la corretta invocazione del metodo "inserimento(..)".

Per i punti 2 e 3, Nel metodo java responsabile della modifica dell’entità fascicolo SIUS sono state introdotte delle rettifiche per la gestione degli EMA, EMS ed ESS. |  |
| 20200702018 | Ufficio di Sorveglianza di Padova | Gli utenti segnalano che aprendo un fascicolo SIUS di Esecuzione Misura Alternativa, il sistema presenta a video un Numero procedimento E.M.A. che punta ad un fascicolo diverso. | L’intervento di correzione consiste nella rettifica dell’azione di modifica su fascicoli con contenuto EMA. | Nel metodo java responsabile della modifica dell’entità fascicolo SIUS sono state introdotte delle rettifiche per la gestione degli EMA, EMS ed ESS. |  |
| 20200706012 | Ufficio di Sorveglianza di Siracusa | L'utente segnala la mancata visualizzazione dei periodi di concessione o rigetto della Liberazione Anticipata nella pagina di dettaglio dell’ordinanza. | Con l’intervento di correzione è stata rettificata l’invocazione del metodo java nella relativa classe che gestisce le ordinanze dell’UDS in riferimento all’inserimento dei periodi di L.A. | Nella classe java responsabile dell'emissione di una ordinanza di liberazione anticipata è stata ripristinata la corretta invocazione del metodo "inserimento(..)". |  |
| 20200706014 | Ufficio di Sorveglianza di Perugia | L'utente segnala l'anomalia che, per alcuni fascicoli SIUS con all'interno Esecuzione di Misure Alternative, i dati anagrafici del soggetto ed i dati del fascicolo EMA appartengono ad una altro soggetto anagrafico. | L’intervento di correzione consiste nella rettifica dell’azione di modifica su fascicoli con contenuto EMA. | Nel metodo java responsabile della modifica dell’entità fascicolo SIUS sono state introdotte delle rettifiche per la gestione degli EMA, EMS ed ESS. |  |
| 20200706016 | Ufficio di Sorveglianza di Catania | L’utente segnala la mancata coincidenza del numero del procedimento SIUS con quello del procedimento EMA. | L’intervento di correzione consiste nella rettifica dell’azione di modifica su fascicoli con contenuto EMA. | Nel metodo java responsabile della modifica dell’entità fascicolo SIUS sono state introdotte delle rettifiche per la gestione degli EMA, EMS ed ESS. |  |
| 202007010112 | Procura Generale presso la Corte d’Appello di Taranto | L'utente segnala che nella funzione ‘Decisione del GE’, in corrispondenza del menù ‘Altre Ordinanze/Decreti’, nella combo-box dei contenuti, il sistema visualizza dei valori errati. | Con l’intervento di correzione si è proceduto al caricamento corretto della lista dei contenuti del Giudice dell’esecuzione. | In fase di inserimento di una annotazione provvedimento per una decisione del GE, il campo di tipo comboBox "Contenuto" seleziona i contenuti relativi alle autorità GE (Giudice Esecuzione). |  |
| 202007020110 | Ufficio di Napoli | L'utente segnala che nella funzione ‘Decisione del GE’, in corrispondenza del menù ‘Altre Ordinanze/Decreti’, nella combo-box dei contenuti, il sistema visualizza dei valori errati. | Con l’intervento di correzione si è proceduto al caricamento corretto della lista dei contenuti del Giudice dell’esecuzione. | In fase di inserimento di una annotazione provvedimento per una decisione del GE, il campo di tipo comboBox "Contenuto" seleziona i contenuti relativi alle autorità GE (Giudice Esecuzione). |  |
| 202007020111 | Ufficio di Sorveglianza di Milano | L'utente segnala che nonostante si scarichi correttamente l’ordinanza di liberazione anticipata il sistema (dopo il deposito) non riporta il periodo di concessione né i giorni concessi. | Con l’intervento di correzione è stata rettificata l’invocazione del metodo java nella relativa classe che gestisce le ordinanze dell’UDS in riferimento all’inserimento dei periodi di L.A. | Nella classe java responsabile dell'emissione di una ordinanza di liberazione anticipata è stata ripristinata la corretta invocazione del metodo "inserimento(..)". |  |
| 202007020112 | Tribunale di Sorveglianza di Napoli | L'utente segnala che per le liberazioni anticipate, non risultano memorizzati i periodi di riferimento al beneficio e le ordinanze sono incomplete.
Inoltre, all’atto dell’iscrizione dell’esecuzione di misura memorizza come numero della misura quello dell’ordinanza che ha determinato la misura e si collega a procedimento sbagliato.
Inoltre, in fase di ordinanze di “reclamo permesso” dopo lo scarico dell’esito il sistema visualizza un messaggio bloccante. | Per la problematica dei periodi di concessione di Liberazione anticipata, con l’intervento di correzione è stata rettificata l’invocazione del metodo java nella relativa classe che gestisce le ordinanze dell’UDS in relazione all’ inserimento dei periodi di L.A.


Per la problematica relativa ai procedimenti EMA l’intervento ha consistito nella rettifica dell’azione di modifica su fascicoli con contenuto EMA.

Per la problematica del ‘Reclamo Permesso, si è intervenuti sulla gestione del messaggio nella classe che gestisce le ordinanze dell’USD. | Per la prima problematica, nella classe java responsabile dell'emissione di una ordinanza di liberazione anticipata è stata ripristinata la corretta invocazione del metodo "inserimento(..)".

Per la problematica EMA, nel metodo java responsabile della modifica dell’entità fascicolo SIUS sono state introdotte delle rettifiche per la gestione degli EMA, EMS ed ESS.

Per la gestione dell’errore del Reclamo Permesso si è intervenuti nella classe java responsabile dell'emissione di una ordinanza. |  |
| 202007020115 | Ufficio di Sorveglianza di Spoleto | L'utente segnala che il numero procedimento EMA o EMS o ESS non è allineato al numero del fascicolo principale. | Per la problematica relativa ai procedimenti EMA l’intervento ha consistito nella rettifica dell’azione di modifica su fascicoli con contenuto EMA. | Per la problematica EMA, nel metodo java responsabile della modifica dell’entità fascicolo SIUS sono state introdotte delle rettifiche per la gestione degli EMA, EMS ed ESS. |  |
| 202007020117 | Ufficio di Sorveglianza di Frosinone | L'utente segnala che all’atto dello scarico delle ordinanze di liberazione anticipata, il semestre che normalmente viene inserito, non compare ne sul modulo che si estrapola dal sistema ne compare sulla relativa schermata del dettaglio ordinanza. | Per la problematica dei periodi di concessione di Liberazione anticipata, con l’intervento di correzione è stata rettificata l’invocazione del metodo java nella relativa classe che gestisce le ordinanze dell’UDS in relazione all’ inserimento dei periodi di L.A. | Nella classe java responsabile dell'emissione di una ordinanza di liberazione anticipata è stata ripristinata la corretta invocazione del metodo "inserimento(..)". |  |
| 202007060111 | Ufficio di Sorveglianza di Massa | L'utente segnala che il sistema, in fase di emissione di un’ordinanza di liberazione anticipata non mantiene i dati della liberazione anticipata né i gg totali. Inoltre non vengono riportati nella stampa. | Per la problematica dei periodi di concessione di Liberazione anticipata, con l’intervento di correzione è stata rettificata l’invocazione del metodo java nella relativa classe che gestisce le ordinanze dell’UDS in relazione all’ inserimento dei periodi di L.A. | Nella classe java responsabile dell'emissione di una ordinanza di liberazione anticipata è stata ripristinata la corretta invocazione del metodo "inserimento(..)". |  |


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
Aggiornamento versione SIES |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20200706-Piano_di_Rilascio_SIES_v.12.3.0.2.docx 
SIUT-SIES-PT-1.0-20200706-Piano_dei_Test_SIES_v.12.3.0.2.docx
SIUT-SIES-CT-1.0-20200706-Allegato_al_piano_test_SIES_v.12.3.0.2.xlsx |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.3.0.1.
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
Creare sul server DB una cartella V_12_3_0_2 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/ V_12_3_0_2/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_3_0_2 tramite il comando:
chmod 777 V_12_3_0_2

In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx

Nella cartella appena creata (V_12_3_0_2), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/ V_12_3_0_2/log/ in cui si può constatare l’esito dell’esecuzione.

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