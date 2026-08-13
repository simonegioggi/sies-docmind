---
uniqueName: siut-sies-pr-1-0-20201012-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20201012 Piano di Rilascio SIES v 12 4 3 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20201012-Piano_di_Rilascio_SIES_v.12.4.3.0

> **File originale:** `RILASCIO_12.4.3.0/SIUT-SIES-PR-1.0-20201012-Piano_di_Rilascio_SIES_v.12.4.3.0.doc`  
> **Tipo:** DOC

---

Ministero della Giustizia

	Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi

Direzione Generale per i Sistemi Informativi Automatizzati





Ministero della Giustizia

Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi

Direzione Generale per i Sistemi Informativi Automatizzati





Piano di Rilascio

SIES v.12.4.3.0



















Versione 1.0 del 12/10/2020










Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.






Approvazioni





Nominativo

Funzione

Elaborato da

Engineering

RTI

Verificato da

Vito Bufi

Responsabile Manutenzione Sistemi attuali

Approvato da

Paolo Ceccanti

Responsabile Unico Fornitura

Data approvazione

12/10/2020



Livello di riservatezza

L4





Elenco versioni

Versione

Data 

Motivo

Modifica

1.0

12/10/2020

Prima Emissione





Lista di distribuzione

Nominativo

Organizzazione

Ufficio

Funzione

Ing. Giovanni Malesci

Amministrazione



Responsabile Unico Procedimento

Dr.ssa Annamaria Palmieri

Amministrazione



Direttore Esecutivo Contratto

Paolo Ceccanti

RTI



Responsabile Unico Fornitura

Pasquale Lamattina

RTI



Referente Tecnico

Vito Bufi

RTI



Responsabile Manutenzione Sistemi attuali

Fabio Mazzocchi

RTI



Responsabile Manutenzione Correttiva

Andrea Salvaggio

RTI



Responsabile Progetto Sistema Unitario

Antonio Iacobelli

RTI



Responsabile Supporto Specialistico

Antonella Damiani

RTI



Responsabile Centro di Competenza

Fabio Gattamorta

RTI



Responsabile PMO 

Alessandro Falleni

RTI



Referente sicurezza

Edoardo Lamuraglia

RTI



Referente qualità

Francesco Rosati

RTI



Referente qualità

Andrea Castorino

Alessandro Lanari

RTI



Referente Applicativo Gestore Fascicolo Documentale

Luigi Buglione

RTI



Referente Metrico




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

		4.2	Riferimenti ChangeRequest (ADE/MEV)	9

		4.2.1	Documenti a corredo della sessione di verifica conformità	9

		5	Dettaglio degli elementi oggetto del rilascio	10

		6	Installazione	11

		6.1	Prerequisiti	11

		6.2	Attività di preinstallazione	11

		6.3	Attività di installazione	11

		6.3.1	Installazione lato DB	11

		6.3.1.1	Esecuzione script	11

		6.3.2	Installazione applicazione	12

		6.3.2.1	Deploy Applicazione	12

		6.4	Attività di configurazione	13

		6.5	Attività di post-installazione	13






	Introduzione

		Scopo del documento

Il presente documento descrive il piano di rilascio del sistema SIES.

Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.3.0 di SIES.

Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio.

		Riferimenti

Riferimento

Nome Documento

Descrizione Documento

Rif. 1

SIUT-SIES-MG-1.0-20201012 - Correzione fascicoli inseriti ante patch 12.4.3.0.doc

Vademecum contenente i passi da effettuare per la correzione dei fascicoli impattati dall’errore segnalato nel ticket 20200915015

		Glossario

	Definizioni

Definizione

Descrizione





	Acronimi e abbreviazioni

Sigla

Descrizione

DB

Data Base

MAC

Manutenzione Correttiva

MEV

Manutenzione Evolutiva

PM

Procura della Repubblica presso il Tribunale

RTI

Raggruppamento Temporaneo di Impresa

ADE

Manutenzione Adeguativa

	

	Generalità

Il presente documento descrive il piano di rilascio di SIES 12.4.3.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.



Il documento in oggetto fa anche riferimento ad una procedura di correzione di fascicoli con l'anomalia segnalata con il TT 20200915015 [Rif. 1].



Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.

	Identificazione degli elementi rilasciati

Supporto

Oggetti:

Ver.

Del

Portale fornitura

Rilascio SIES

12.4.3.0

12/10/2020

Note-osservazioni





	Riferimenti degli oggetti del rilascio

		Riferimenti Anomalia (MAC)

Rif. Ticket OTRS

Sede

Ufficio

Descrizione segnalazione

Descrizione

intervento

Descrizione Tecnica

Manuali corretti

20200902016

Procura della Repubblica presso il Tribunale di Mantova

L’utente segnala un’anomalia in ambito SIEP. L'utente riferisce che non si può trasmettere la Richiesta di accertamento pericolosità se non viene inserito l'avvocato. 

L’errore era dovuto ad una errata gestione di un controllo relativo alla valorizzazione degli estremi del difensore. Nel codice dell’applicazione era presente un refuso legato ad altre tipologie di trasmissione. Si è intervenuti eliminando il controllo per questa specifica trasmissione.

La correzione ha coinvolto la classe:

"siap.siep.misurasicurezza.action.ActConfermaTrasmissioneRichiestaAccertaPericoloSociale.java”.

Nella classe è stato commentato il controllo che imponeva l'obbligatorietà dell'avvocato in fase di trasmissione di tipo richiesta.



																20200915014

																Procura della Repubblica presso il Tribunale di Bolzano

L’utente richiede supporto per risolvere un errore in fase di presa in carico atti per competenza. 

L’errore è determinato da una errata sequenza di istruzioni all’interno della procedura Oracle “PULISCI_ALTRE_BDI”. E’ stata introdotta la corretta sequenza.

La correzione ha coinvolto la procedura Oracle “PULISCI_ALTRE_BDI”. Nel codice della Stored Procedure è stato invertito ordine di cancellazione tra le tabelle “POSIZIONE_GIURIDICA” e “ALTRA_CAUSA”.



																20200915015

																Tribunale di Sorveglianza di Perugia

L’utente segnala l'impossibilità di trasferire Procedimenti SIEP sul DB SIUS di Perugia, provenienti da altre sedi d'Italia.

L’errore è determinato dal fatto che veniva inserito lo stato procedimento a "validato" in fase di generazione del fascicolo di classe 7 a partire da un fascicolo di classe 1. L'errore consisteva nel fatto che in fase di “Conversione Pene Pecuniarie” veniva generato un fascicolo di classe 7 il cui stato procedimento si” agganciava" erroneamente all'evento del fascicolo di origine.

La correzione ha coinvolto la classe: “siap.siep.penapecuniaria.controller.RichiestaConversioneController.java”. Nella classe è stata commentata la riga che collegava il record “STATO_PROCEDIMENTO” del fascicolo di classe 7 al record “EVENTO” del fascicolo di origine.

Tuttavia, tale intervento evita che si verifichino altri casi del genere, in caso di nuove iscrizioni, ma non rimuove l’anomalia sui procedimenti, di tale tipologia, già presenti a sistema. Per questo motivo, nella consegna della patch che rimuove l’errore software, è previsto il rilascio di uno script che correggerà l’errore su procedimenti già presenti dopo averli storicizzati in una tabella di appoggio.





		Riferimenti ChangeRequest (ADE/MEV)

Prot. Richiesta o

Rif. Ticket OTRS

Scheda Intervento

Specifica Intervento

Descrizione Breve











	Documenti a corredo della sessione di verifica conformità

Tipo Documento

Nome Documento

Directory Portale

a. Architettura HW e SW

N.A.

N.A.

b. Configurazione HW e SW

N.A.

N.A.

c. Specifiche Dati (Schema Concettuale, Schema Logico e Schema Fisico)

N.A.

N.A.

d. Documento di specifica funzionale del sistema

N.A.

N.A.

e. Manuale di installazione del sistema

N.A.

N.A.

f. Manuale di Configurazione del sistema

N.A.

N.A.

g. Manuale utente del sistema

N.A.

N.A.

h. Manuale dell'amministratore del sistema

N.A.

N.A.

i. Documento per la definizione dell'ambiente di sviluppo

N.A.

N.A.



	Dettaglio degli elementi oggetto del rilascio

Nome File

Path

Motivazione-riferimento

aggiorna_db.zip

Database

Script: 

Inserimento record nella Tabella “VERSIONE” (aggiornamento versione SIES)

Aggiornamento codice Procedura “PULISCI_ALTRE_BDI”

sorgenti.zip

Sorgenti

Sorgenti software

sies.war

Applicazione

Eseguibile dell’applicazione SIES

documentazione.zip

Documentazione

SIUT-SIES-PR-1.0-20201012-Piano_di_Rilascio_SIES_v.12.4.3.0.doc

SIUT-SIES-PT-1.0-20201012-Piano_dei_Test_SIES_v.12.4.3.0.doc

SIUT-SIES-CT-1.0-20201012-Allegato_al_piano_test_SIES_v.12.4.3.0.xls

SIUT-SIES-MG-1.0-20201012 - Correzione fascicoli inseriti ante patch 12.4.3.0.doc

Note-osservazioni



	Installazione

	Prerequisiti

Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.2.0.

	Attività di preinstallazione

Aprire una shell linux sul server SIES e loggarsi come utente “root”;

Eseguire il comando: “cd /etc/init.d”;

Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”;

Fermare il processo di gestione delle code tramite il comando: “./imq stop”;



	Attività di installazione

	Installazione lato DB

Esecuzione script

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



Eseguire gli step descritti nel documento SIUT-SIES-MG-1.0-20201012 - Correzione fascicoli inseriti ante patch 12.4.3.0.doc. Occorre passare al punto successivo solo se le istruzioni riportate nel suddetto documento terminano in modo corretto, altrimenti, se così non fosse, la procedura di installazione si può ritenere conclusa con esito negativo. Se conclusa con esito negativo, tralasciare il resto delle istruzioni e passare direttamente al punto 3 del paragrafo 6.3.2.1 per il riavvio del server.

Copiare il file aggiorna_db.zip in una qualsiasi cartella e scompattarlo. il sistema crea la cartella aggiorna_db;

Creare sul server DB una cartella V_12_4_3_0 sotto la directory /home/oracle/;

Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/ V_12_4_3_0/;

Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_3_0 tramite il comando:

chmod 777 V_12_4_3_0



In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:

==================================================

Riassunto dei dati immessi per questa installazione

Nome ....................: sies

==================================================

SID Oracle ..............: sies

Utente_SIES..............: siesxx

Password_SIES............: siesxx



Nella cartella appena creata (V_12_4_3_0), lanciare il comando:

./aggiorna_db.sh

Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/ V_12_4_3_0/log/ in cui si può constatare l’esito dell’esecuzione.



N.B. Le segnalazioni del tipo:

ORA-00001: violata restrizione di unicità

ORA-00955: name is already used by an existing object

Cartella log già presente

ORA-04043: object does not exist

sono da considerarsi warning e non errori.



Accedere ad oracle (con qualsiasi strumento tipo toad, developer…) come utente siesxx e compilare tutte le procedure e i package che non risultano compilate.

ATTENZIONE: la procedura SUPER_SOGGETTO_PREGR e il package CARICA_RES potrebbero restare non compilate: non è da considerarsi errore.



	Installazione applicazione

Deploy Applicazione

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



	Attività di configurazione

N.A.

	Attività di post-installazione

N.A.

		SIUT-SIES-PR-1.0-20201012-Piano_di_Rilascio_SIES_v.12.4.3.0

Ver. 1.0 del 12/10/2020

Pag. 13/13