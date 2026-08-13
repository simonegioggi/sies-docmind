---
uniqueName: siut-sies-pr-1-0-20210226-pianodirilasciosiesv-12-
displayName: "SIUT SIES PR 1 0 20210226 Piano di Rilascio SIES v 12 4 7 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20210226-Piano_di_Rilascio_SIES_v.12.4.7.0

> **File originale:** `RILASCIO_12.4.7.0/SIUT-SIES-PR-1.0-20210226-Piano_di_Rilascio_SIES_v.12.4.7.0.doc`  
> **Tipo:** DOC

---

Ministero della Giustizia

	Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi

Direzione Generale per i Sistemi Informativi Automatizzati





Ministero della Giustizia

Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi

Direzione Generale per i Sistemi Informativi Automatizzati





Piano di Rilascio

SIES v.12.4.7.0



















Versione 1.0 del 26/02/2021










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

26/02/2021



Livello di riservatezza

L4





Elenco versioni

Versione

Data 

Motivo

Modifica

1.0

26/02/2021

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

Salvatore Piazza

RTI



Technical Manager

Sergio Tamburrini

RTI



Organization Manager

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

Francesco Rosati

RTI



Referente qualità

Andrea Castorino

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

		4.1	Riferimenti Anomalia (MAC/GAR)	8

		4.2	Riferimenti ChangeRequest (ADE/MEV)	10

		4.2.1	Documenti a corredo della sessione di verifica conformità	11

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






	Introduzione

		Scopo del documento

Il presente documento descrive il piano di rilascio del sistema SIES.

Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.7.0 di SIES.

Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio.

		Riferimenti

Riferimento

Nome Documento

Descrizione Documento







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

Il presente documento descrive il piano di rilascio di SIES 12.4.7.0 contenente gli interventi di natura correttiva, eseguiti a fronte di segnalazioni pervenute mediante il sistema di trouble ticketing OTRS.



Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.

	Identificazione degli elementi rilasciati

Supporto

Oggetti:

Ver.

Del

Portale fornitura

SIUT > 06 - Rilasci Software > SIES > Rilascio SIES 12.4.7.0 2021-02-26

12.4.7.0

26/02/2021

Note-osservazioni





	Riferimenti degli oggetti del rilascio

		Riferimenti Anomalia (MAC/GAR)

Rif. Ticket OTRS

Sede

Ufficio

Descrizione segnalazione

Descrizione

intervento

Descrizione Tecnica

Manuali corretti

20210113013

Procura Generale presso la Corte d’Appello di Venezia

L’utente segnala che ad oggi il SIEP, tra le pendenze per fattori interni nel riepilogo ispettivo, riporta quei procedimenti il cui ultimo atto è una "richiesta generica" o "revoca sanzione sostitutiva". L’utente segnala pertanto i procedimenti che non devono essere indicati nelle pendenze per fattori interni: “35/1976 - 167/1997 - 422/2005 - 396/2009 - 385/2010 - 410/2013 - 435/2013 - 425/2017 - 169/2018 - 209/2018”. L’utente evidenzia che molti di suddetti fascicoli provengono da migrazione e chiede se esista e quale sia un eventuale campo in cui inserire la data definizione in modo che la statistica li consideri esauriti.

Per la risoluzione della problematica si è intervenuti con la modifica del package Oracle “Ispettorato”. In esso, infatti, è stato riscontrato un errore nella classificazione di procedimenti aventi ultimi eventi iscritti nello stesso giorno.

E’ stato modificato il package:

Ispettorato (metodo STAT_PROVVEDIMENTI)

In cui è stata corretta la gestione del campo data “data_inserimento” (due occorrenze).



20210127015

Ufficio di Sorveglianza di Bolzano

L’utente segnala che non riesce ad inserire un decreto di irreperibilità perché il sistema indica che esiste già un decreto di irreperibilità.

Per la risoluzione della problematica si è intervenuti con la modifica della classe “ActLoadInserisciDecretoIrreperibilità” in cui è stato corretto il tipo di esito testato (da rigetto ad inammissibilità) ed il messaggio rilanciato. Il sistema citava erroneamente un decreto di irreperibilità.

E’ stata modificata a classe java:

siap.sius.depositodecreto.action.ActLoadInserisciDecretoIrreperibilità

in cui è stato cambiato il messaggio di ritorno ed il codice esito da testare.



202101270113

Procura Generale della Repubblica Presso la Corte D'Appello di Bari

L’utente segnala di voler di riportare lo stato di lavorazione della cartella PM attualmente visualizzabile alla data del 13/02/2020, in particolare ripristinando le voci del 31.01.2020 e del 13.02.2020 : si precisa che le successive lavorazioni che l'ufficio ha erroneamente lavorato hanno riportato sul sistema una pena residua errata che l'ufficio non riesce più a ricostruire (molti di questi provvedimenti peraltro l'ufficio gli ha resi anche non visibili).
Dopo le lavorazioni errate da parte dell'ufficio tale pena residua è diventata di anni 1 mesi 5 e giorni 9 collegando al procedimento anche una liberazione anticipata di giorni 45 che il realtà il sistema aveva già acquisito e quindi non doveva più considerare.
Pertanto l'ufficio richiede come poter aggiornare correttamente la pena residua che nell’ ultimo provvedimento lavorato nel siep e notificato al condannato era pari ad anni 1 mesi 3 giorni 23 e che a causa di lavorazioni nel siep inesatte, il sistema non produce più tale residuo pena ma ne dà uno sbagliato come sopra indicato.
Richiede altresì di annullare i provvedimenti visibili inseriti in data 27/01/2021 che  il sistema non permette più all’ utente di eliminarli autonomamente.

Per la risoluzione della problematica si è intervenuti con la correzione della query che estraeva la count sul numero di provvedimenti. Aggiunto filtro sul TIPO_PROVVEDIMENTO 50 - Rinvio udienza da verbale. Usciva erroneamente nelle ricerche SIEP ma è un evento SIUS.

Sono state modificate le classi java: 

siap.siep.ordineesecuzione.action.ActRicercaProvvedimenti

siap.sico.evento.controller.IEventoSimeone

siap.sico.evento.controller. EventoSimeoneController

siap.sico.evento.dao.EventoSqlDAO

siap.siep.fascicolo.controller.FascicoloSiepController

aggiungendo il codice “50” tra i Tipi di Provvedimento da escludere tra gli eventi del PM ed adeguando la query di conteggio e quella di estrazione dei campi.



20210208018

Procura della Repubblica presso il Tribunale per i Minorenni di Torino

L’utente segnala la mancata visualizzazione sedi altri distretti.

Per la risoluzione della problematica si è intervenuti con la correzione della pagina di visualizzazione in cui non veniva caricata la descrizione nella combo altra BDI.

E’ stata modificata a classe jsp:

jsp.files.siap.sico.soggetto.DettaglioSoggetto.jsp

in cui è stata aggiunta la descrizione accanto al campo codice.



20210212012

Procura della Repubblica presso il Tribunale per i Minorenni di Torino

L’utente segnala che il sistema non visualizza Anno/Numero Reg.Gen. Gup Presso il Tribunale per i Minorenni, che non è presente in Dettaglio il Titolo Cumulato ma presente in Dettaglio Sentenza siep.

Per la risoluzione della problematica si è intervenuti con la correzione della classe “TitoloCumulatoModel” in cui è stata aggiunta la  mappatura del GUP e CAPSM nel modulo Cumulo.

E’ stata modificata a classe java:

siap.siep.modulocumulo.model.TitoloCumulatoModel

in cui è stato aggiunta l’impostazione delle proprietà “Anno Registro Generale” e “Numero Registro Generale” per le autorità “GUP” e “CAPSM”.



20210212019 (GAR - Manutenzione in garanzia)

DGSIA - Referenti Applicativi

L’utente segnala esito dei test è negativo come da documenti allegati per il rilascio della patch 12.4.6.0: in pratica nel ticket 202012020116 veniva segnalata la problematica che il sistema non riportava i dati relativi alla revoca della misura alternativa e che il controllo andava esteso a tutte le tipologie di  misure alternative.

Per la risoluzione della problematica si è intervenuti con la correzione della classe “StatoEsecTitoloCumulatoController” in cui è stata cambiata la gestione del campo “DataInizioMisura” ampliando la casistica anche alle misure alternative che NON rideterminano la pena (es: Detenzione Domiciliare - Semilibertà - Arresti Domiciliari art. 656 c. 10). Inoltre in accordo con i referenti SIES dell’ufficio di Torino sono state apportate modifiche di forma ai templates indicati.

E’ stata modificata la classe:

siap.siep.modulocumulo.controller.StatoEsecTitoloCumulatoController.java

nella quale è stata cambiata la gestione della data di fine misura.

Sono stati anche modificati i template:

RichiestePmCumInviateGERevocaBenefici.rtf, 

RichiestePmInCumuloApplicazBenefici.rtf,

RichiestePmInCumuloRevocaBenefici.rtf,

RichiestePmInCumuloRevocaPenaPrinc.rtf;

RichiestePmInCumuloRevocaSS.rtf



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

Aggiornamento versione SIES in tabella “Versione”

Inserimento record in tabella “CG_REF_CODES”

Aggiornamento procedura “Ispettorato”

sorgenti.zip

Sorgenti

Sorgenti software

sies.war

Applicazione

Eseguibile dell’applicazione SIES

template.zip

Template

Template aggiornati:

SIEP_CUMULO_PROSPETTO_PROPOSTA.rtf

RichiestePmCumInviateGERevocaBenefici.rtf

RichiestePmInCumuloApplicazBenefici.rtf

RichiestePmInCumuloRevocaBenefici.rtf

RichiestePmInCumuloRevocaPenaPrinc.rtf

RichiestePmInCumuloRevocaSS.rtf

documentazione.zip

Documentazione

SIUT-SIES-PR-1.0-20210226-Piano_di_Rilascio_SIES_v.12.4.7.0.doc

SIUT-SIES-PT-1.0-20210226-Piano_dei_Test_SIES_v.12.4.7.0.doc

SIUT-SIES-CT-1.0-20210226-Allegato_al_piano_test_SIES_v.12.4.7.0.xls

Note-osservazioni



	Installazione

	Prerequisiti

Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.5.0.

Nota circa il mancato rilascio della patch 12.4.6.0

La patch in questione è stata bloccata per problemi riguardanti i due ticket che la componevano:

202012020116-Provvedimento di cumulo revoca misura alternativa in cui veniva segnalato "correzione da fare per tutte le misure". Quindi, nel rilascio della 12.4.7.0 è stata effettuata la modifica per tutte le tipologie di misura. 

20201204019-Calcolo errato revoca benefici applicati con sentenza di condanna in cui veniva segnalato che "sul template non risultava fatto quanto richiesto". In questo caso si segnala che il ticket era stato suddiviso in due parti (una MAC ed una MEV); la parte MAC è stata risolta correttamente, mentre la segnalazione di errore riguardava la parte MEV e quindi vi sarà una modifica strutturale in futuro. Come da richiesta utente, con la patch 12.4.7.0 sono state apportate delle modifiche formali su alcuni template.

Per mantenere, comunque, una continuità temporale nel sistema di versioning del progetto, nello script consegnato “aggiorna_versione.sql” vengono inseriti in tabella “Versione” due record comprendenti la versione 12.4.6.0 con data di sistema -1 e versione 12.4.7.0 con data di sistema.

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



Copiare il file aggiorna_db.zip in una qualsiasi cartella e scompattarlo. il sistema crea la cartella aggiorna_db;

Creare sul server DB una cartella V_12_4_7_0 sotto la directory /home/oracle/;

Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/V_12_4_7_0/;

Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_12_4_7_0 tramite il comando:

chmod 777 V_12_4_7_0



In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:

==================================================

Riassunto dei dati immessi per questa installazione

Nome ....................: sies

==================================================

SID Oracle ..............: sies

Utente_SIES..............: siesxx

Password_SIES............: siesxx



Nella cartella appena creata (V_12_4_7_0), lanciare il comando:

./aggiorna_db.sh

Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/V_12_4_7_0/log/ in cui si può constatare l’esito dell’esecuzione.



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

Copiare i file contenuti nella cartella template\siep\cumulo

nella cartella “/var/SIES/template/siep/cumulo” sovrascrivendo quelli precedenti;

Copiare i file contenuti nella cartella template\import

nella cartella “/var/SIES/template/import” sovrascrivendo quelli precedenti;



Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 2.b e 2.e. All’avvio, infatti, tali cartelle verranno ricreate.



Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.

Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;

Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.

	Attività di configurazione

N.A.

	Attività di post-installazione

N.A.





		SIUT-SIES-PR-1.0-20210226-Piano_di_Rilascio_SIES_v.12.4.7.0

Ver. 1.0 del 26/02/2021

Pag. 15/15