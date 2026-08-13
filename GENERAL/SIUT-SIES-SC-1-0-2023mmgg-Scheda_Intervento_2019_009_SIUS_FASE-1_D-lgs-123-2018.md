---
uniqueName: siut-sies-sc-1-0-2023mmgg-schedaintervento2019009s
displayName: "SIUT SIES SC 1 0 2023mmgg Scheda Intervento 2019 009 SIUS FASE 1 D lgs 123 2018"
category: "GENERAL"
tags: []
---

# SIUT-SIES-SC-1.0-2023mmgg-Scheda_Intervento_2019_009_SIUS_FASE-1_D.lgs.123-2018

> **File originale:** `MEV/SCHEDA_009/SIUT-SIES-SC-1.0-2023mmgg-Scheda_Intervento_2019_009_SIUS_FASE-1_D.lgs.123-2018.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento per la transizione digitale, analisi statistica e politiche di coesione
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Umberto Mignogna – Andrea Castorino |  |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 17/05/2023 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 21/03/2023 | Prima Emissione |  |
| 1.1 | 24/03/2023 | Seconda Emissione | Par. 2.7.2 secondo le indicazioni ricevute per le vie brevi
2.5.2.1 Dettagliata la funzionalità
Cap.3 a seguito di indicazioni ricevute per le vie brevi |
| 1.2 | 27/03/2023 | Terza Emissione | Eliminato punto 2 del paragrafo 2.7.2 come da indicazioni ricevute per le vie brevi.
Modificato par. 3.1 |
| 1.3 | 29/03/2023 | Quarta Emissione | Modificato il paragrafo 2.7.2 e paragrafo 2.7.3 |
| 1.4 | 05/04/2023 | Quinta Emissione | Aggiornati paragrafi 3.1, 3.2 e 5.1.1 |
| 1.5 | 10/05/2023 | Sesta Emissione | Eliminato paragrafo 2.1 “Iscrizione Procedimento” in quanto era un refuso.
Aggiornato paragrafo 2.6.3 |
| 1.5 | 17/05/2023 | Settima Emissione | Aggiornato paragrafo 2.6.3 |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Aurora Garofalo | Amministrazione |  | Responsabile Unico Procedimento |
| Oris Orlando | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Francesco Rosati | RTI |  | Responsabile Manutenzione Correttiva e Referente Qualità e Sicurezza |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario e Referente Tecnico |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Referente PMO e Qualità |
| Alessandro Falleni | RTI |  | Referente Sicurezza |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |


Indice dei contenuti
Eliminato paragrafo 2.1 “Iscrizione Procedimento” in quanto era un refuso.	3
1	Introduzione	5
1.1	Scopo del documento	5
1.2	Riferimenti	5
1.3	Glossario	5
1.3.1	Acronimi e abbreviazioni	5
2	Interventi su SIES	7
2.1	Iscrizione Pena Complessiva	7
2.2	Modalità Pagamento Pena Pecuniaria	9
2.3	Civilmente Obbligato per la Pena Pecuniaria	12
2.4	Gestione Riscossione Pene Pecuniarie	15
2.4.1	Ordine di ingiunzione Pagamento	16
2.4.2	Gestione Ordine Ingiunzione	18
2.4.3	Gestione Bollettini PagoPA	20
2.5	Base Dati	24
2.6	Integrazione servizio PagoPA	25
2.6.1	Architettura del servizio	25
2.6.2	Configurazione del certificato di comunicazione	26
2.6.3	Batch di verifica stato del Pagamento	27
2.6.4	Descrizione dei servizi WEB PST	29
3	Interventi su RegeWEB	33
3.1	Gestione Oblazione prevista per i procedimenti di competenza del tribunale ordinario	33
3.1.1	Acquisizione stato pagamenti	35
3.2	Gestione Decreto penale per procedimenti di competenza del tribunale ordinario Artt. 459 e 460 cpp	36
3.3	Abilitazione pagamenti tramite PagoPA	38
4	Piano delle attività	39
4.1	Ciclo di sviluppo	39
5	Dimensionamento	40
5.1	Stima dell'effort	40
5.1.1	Attività progettuali a corpo	40

Introduzione
Scopo del documento
Nel documento in oggetto si delineano gli interventi da effettuare sui sistemi SIES e RegeWEB in merito al pagamento delle pene pecuniarie anche attraverso l’interfacciamento del PagoPA/PST mediante l’invocazione dei seguenti servizi:
Servizio per la generazione del Bollettino (quando viene creato un bollettino viene in automatico generato uno stato ad esso associato, identificativo IUV);
Servizio per avere aggiornamenti sullo stato del bollettino.
Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF 1 | m_dg.DOG07AR.14_02_2023.0000226.U_Richiesta_scheda_2023-13_APP-SIES_PAGOPA_v_1.0_signed | Richiesta Scheda |
| RIF 2 | Invio_atti_cognizione_scheda_2023-13_PAGOPA_v_1.0_signedPagoPA_2023-13__cognizione | Atti Cognizione |
| RIF 3 | Documentazione_servizi_web_v1.53 | Servizi esposti dal PST |
| RIF 4 | APPLICATIVI - Flussi pagamento telematico tramite PST vers. 3.1 | Servizi esposti dal PST |

Glossario
Acronimi e abbreviazioni
| Sigla | Descrizione |
| --- | --- |
| API | Application Programming Interface |
| CPU | Central Processing Unit |
| CV | Curriculum Vitae |
| DB | Data Base |
| DEC | Direttore Esecutivo Contratto |
| DGSIA | Direzione Generale per i Sistemi Informativi Automatizzati |
| DR | Disaster Recovery |
| ETSI | European Telecommunications Standards Institute |
| FP | Function Point |
| GdL | Gruppo di Lavoro |
| GDPR | General Data Protection Regulation |
| ICT | Information & Communication Technology |
| ISO | International Organization for Standardization |
| ISP | Information Security Policy |
| IT | Information Technology |
| MAC | MAnutenzione Correttiva |
| MEV | Manutenzione EVolutiva |
| PA | Pubblica Amministrazione |
| PdQ | Piano della Qualità |
| PdS | Piano della Sicurezza |
| PEC | Posta Elettronica Certificata |
| PMO | Program Management Office |
| POO | Program Operating Office |
| RTI | Raggruppamento Temporaneo di Impresa |
| RTO | Recovery Time Objective |
| RUF | Responsabile Unico Fornitore |
| RUP | Responsabile Unico Progetto |
| SAL | Stato Avanzamento Lavori |
| SGQ | Sistema di Gestione per la Qualità di Engineering Ingegneria Informatica S.p.A. |
| SGSI | Sistema di Gestione della Sicurezza Informatica |
| SIU | Sistema Informativo Unitario |
| SLA | Service Level Agreement |
| SM | Security Manager |
| SQL | Structured Query Language |
| SW | SoftWare |
| UTA | Utente Generico Amministrazione |
| VPN | Virtual Private Network |

Interventi su SIES
Iscrizione Pena Complessiva
Nella form di Iscrizione Pene Complessiva sarà aggiunta una nuova sezione per l’acquisizione dei dati relativi alle Pene Sostitutive delle Pene Detentive Brevi



in cui sarà possibile gestire le seguenti tipologie di pena



La valorizzazione della sezione Sanzione Sostituiva sarà alternativa alla valorizzazione della sezione Pene Sostitutive delle Pene Detentive Brevi. La nuova sezione sarà riportata anche nelle form di Dettaglio, quando valorizzata, e Modifica.

A seguito della Conferma il sistema inserirà i dati nella base dati e invierà la form di Dettaglio


in cui, nella combo box delle azioni saranno aggiunte due nuove voci “Modalità Pagamento Pena Pecuniaria”, “Civilmente Obbligato per la Pena Pecuniaria”



Sarà inoltre possibile:

selezionare la azione di Modifica, ricevendo la form



da cui sarà possibile procedere alla modifica dei dati


Selezionare l’azione di cancellazione, ricevendo la form



da cui sarà possibile procedere alla cancellazione dei dati.
Modalità Pagamento Pena Pecuniaria
La funzione consentirà di gestire la modalità di pagamento della pena pecuniaria come stabilita dal giudice della cognizione in sentenza. Per tale motivo la funzione sarà abilitata su procedimento solo in stato di iscritto.

Selezionando questa voce dal Dettaglio della Pena Complessiva



il sistema controllerà se nella base dati risulta già inserita tale informazione. In caso di esistenza presenterà la form di Dettaglio; in caso di assenza presenterà la form di Inserimento, preimpostata sul pagamento in una unica soluzione



se si imposta il radio button su Pagamento Rateizzato, la sezione successivo della form si modificherà nella seguente



con la possibilità di aggiungere ulteriori righe, selezionando il link



Le due modalità di pagamento (unica soluzione o pagamento rateale) saranno ovviamente alternative.
L’importo da pagare sarà uguale alla somma degli importi (visualizzati nella prima parte della form, per la Pena Pecuniaria e per la Pena Pecuniaria sostitutiva) riportati in fase di iscrizione sentenza: sarà comunque modificabile.

L’importo indicato in Pagamento Unica Soluzione o la somma degli importi delle rate indicati in Pagamento Rateizzato dovrebbero essere uguali a quanto indicato in Importo da Pagare. In caso di non corrispondenza il sistema invierà il seguente messaggio


Il numero giorni fissato come termine ultimo per il pagamento del primo versamento sarà un dato obbligatorio.

A seguito della conferma il sistema acquisirà i dati nelle base dati e presenterà la seguente form di Dettaglio



Da cui sarà possibile procedere:

alla Modifica



alla Cancellazione dei dati, in tal caso, prima di procedere all’eliminazione dei dati dalla base dati, invierà il seguente messaggio di Conferma

Civilmente Obbligato per la Pena Pecuniaria
La funzione consentirà di gestire la Persona Fisica/Giuridica civilmente obbligata al pagamento della pena pecuniaria in caso di mancato pagamento da parte del Condannato come indicato dal giudice della cognizione in sentenza . Per tale motivo la funzione sarà abilitata solo su procedimento in stato di iscritto.
Selezionando questa voce dal Dettaglio della Pena Complessiva


il sistema controllerà se nella base dati risulta già inserita tale informazione, in caso di esistenza presenterà la form di Dettaglio, in caso di assenza presenterà la form di inserimento, impostata di default su persona fisica



in cui nella combo box Qualifica saranno presenti le seguenti voci



Selezionando una delle voci differenti da ‘-‘, la form si modificherà presentando i campi per l’inserimento di una seconda persona Civilmente Obbligata


La seconda persona Civilmente obbligata assume la stessa Qualifica della prima persona.
L’inserimento della seconda persona Civilmente obbligata non è obbligatoria.

In caso di selezione del radio button su persona giuridica  la form si modificherà in



In cui nella combo box della qualifica saranno riportate sempre le stesse voci, viste in precedenza, ma in questo caso non sarà presentata una seconda sezione per l’inserimento di una seconda parte Civilmente Obbligata.

A seguito della conferma il sistema acquisirà i dati nella base dati e presenterà la seguente form di Dettaglio



Da cui sarà possibile procedere:

alla Modifica



La cui form sarà bloccata su persona fisica o giuridica, in base alla tipologia di persona inserita nella base dati.

alla Cancellazione dei dati, in tal caso, prima di procedere all’eliminazione dei dati dalla base dati, invierà il seguente messaggio di Conferma



Dalla form di Dettaglio sarà possibile richiamare la funzione di Gestione del Difensore della persona Civilmente Obbligata. Non essendo questa funzione implementata in questa fase, Il link Gestione Difensore sarà solo CLICCABILE, nel qual caso il sistema invierà il seguente messaggio


Gestione Riscossione Pene Pecuniarie
Per la gestione di tutti gli aspetti connessi alla riscossione delle Pene Pecuniarie e delle Pene Sostitutive si interverrà nell’attuale  menu delle funzioni che il sistema presenta selezionando la voce



Che a sua volta presenterà il seguente menu di funzioni, in cui alle preesistenti, saranno aggiunte  due nuove voci, di seguito racchiuse nel riquadro in rosso



Al momento entrambi le voci presenteranno lo stesso menu di funzioni


Ordine di ingiunzione Pagamento
La funzione consentirà di inserire l’Ordine di ingiunzione al pagamento della pena pecuniaria al Condannato, al Civilmente obbligato e ai rispettivi Difensori, verificando che risultino obbligatoriamente già inseriti i dati delle modalità di pagamento



La form presenterà i dati di dettaglio delle modalità di pagamento e del Civilmente Obbligato, se presente, e le autorità destinatarie delegate alla notifica dell’atto al Condannato, al Difensore ed al Civilmente Obbligato.

A seguito della completa compilazione dei campi della form e della relativa Conferma, il sistema inserisce un Ordine Esecuzione di Ingiunzione al pagamento nella base dati e presenta la form di Dettaglio.

Al momento dell’annotazione della data di avvenuta notifica dell’ordine di ingiunzione al condannato il sistema inserirà il procedimento in un scadenzario, calcolando la data di scadenza in base al numero di giorni del termine di scadenza di pagamento della sola prima o unica rata, non essendo stato ritenuto necessario il calcolo da parte dell’ufficio della data scadenza delle singole rate in caso di rateizzazione.


Da questa form sarà possibile procedere:

Alla Modifica dell’ordine



alla stampa dell’Ordine di Ingiunzione al Pagamento, in unica soluzione o rateizzato e successivamente procedere alla validazione del provvedimento. A tal fine saranno realizzati i due template SIEP_PP_OI_PAGAMENTO_UN.rtf e SIEP_PP_OI_PAGAMENTO_RR.rtf, che saranno richiamati automaticamente dal sistema in base alla modalità di pagamento;
alla validazione del provvedimento, a seguito della quale lo stato procedimento sarà impostato a Emesso Ordine esecuzione di Ingiunzione al Pagamento della Pena Pecuniaria;
ad accedere alla funzione Notifiche per annotare le date di avvenuta notifica del provvedimento, cliccando sul link .

Il nuovo provvedimento sarà riportato nell’Elenco Provvedimenti del PM, rispettandone tutte le regole previste per gli altri provvedimenti di SIEP


Gestione Ordine Ingiunzione
Selezionando la voce di menu Gestione Ordine Ingiunzione, il sistema presenterà la seguente form


#### Notifiche
In questa MEV sarà realizzata solo la funzione di Notifiche che permetterà, al momento dell’annotazione della data di avvenuta notifica al condannato, di far scattare gli scadenzari della data di scadenza dell’ unico bollettino o del primo bollettino, in caso di rateizzazione.

La funzione sarà attivabile dal precedente menu o dal dettaglio dell’Ordine di esecuzione di Ingiunzione al Pagamento cliccando sul link . In caso di avvenuta valorizzazione di almeno una data notifica, il sistema presenterà la form di Dettaglio.



Per acquisire la data dell’avvenuta notifica l’utente dovrà valorizzare il campo Data Notifica per ciascuna della parti per cui risulta già effettuata la notifica, spuntando eventualmente la check box  per l’indicazione dell’autorità che ha effettuato la notifica, se diversa da quella indicata nell’Ordine di Ingiunzione. A seguito della Conferma, il sistema acquisirà i dati e invierà la form di Dettaglio.



Da cui selezionando l’icona di modifica si riceverà la precedente form di inserimento che permetterà di valorizzare le date mancanti e di modificare o cancellare le date già valorizzate, impostandole a spazio.
Gestione Bollettini PagoPA
Selezionando la voce di menu Gestione Bollettini PagoPA, il sistema presenterà la seguente form

#### Richiesta Bollettini
Da Richiesta Bollettini sarà possibile inoltrare la Richiesta dei bollettini di  pagamento a PagoPA, preparare  l’elenco dei bollettini da richiedere a PagoPA e rimanere in attesa della risposta. All’arrivo della risposta il sistema acquisirà per ciascun bollettino lo IUV e il relativo documento (formato pdf).

Prerequisito per poter richiedere la generazione dei bollettini a PagoPA è la valorizzazione del Codice Fiscale del condannato, per cui il sistema effettuerà un controllo preventivo sulla presenza del dato nella base dati. In caso di assenza invierà il seguente messaggio


cliccando su OK il sistema presenterà la form di Modifica Soggetto per l’acquisizione del dato. Successivamente sarà possibile rieseguire la funzione.


selezionando l'icona Inoltra  il sistema acquisisce la data della richiesta e prepara l’elenco dei bollettini da trasmettere a PST per l'inoltro a PagoPA e presenta la seguente form

Da cui selezionando il tasto  il sistema inoltrerà la richiesta e rimarrà in attesa della ricezione dei bollettini, in attesa dei quali a video apparirà l’immagine di elaborazione in corso

a conclusione della quale apparirà a video il seguente messaggio

Cliccando su OK, il sistema aggiornerà la base dati di SIES con i dati ricevuti e presenterà la form di richiesta

simile alla prima form, ma con Data Richiesta e Data Ricezione valorizzate e priva del tasto Inoltra, cliccando sull’icona Visualizza il sistema presenterà l’elenco dei bollettini completo dello IUV e del documento pdf

Per ciascun bollettino sarà possibile stampare il documento in formato pdf, selezionando l’icona di stampa.
Se si ritorna nella  form di richiesta, risulteranno valorizzate le date di Richiesta e di Ricezione, non sarà più abilitata l'azione di Inoltra, ma sarà possibile solo la Visualizzazione dei singoli bollettini.
#### Verifica Stato Pagamenti
La funzione richiamabile dal menu di Gestione Bollettini o dalla funzione Richiesta Bollettini fornisce  l’Elenco degli ordini di Ingiunzione validati per cui risultano valorizzate la Data_Richiesta e la Data_Ricezione

Selezionando l’azione Visualizza si riceverà l’Elenco dei Bollettini generati da PagoPA e il relativo Stato Pagamenti

Lo stato del singolo pagamento sarà aggiornato automaticamente, differito di un giorno, da PagoPA man mano che l’utente provvederà al pagamento. In effetti vi sarà lato SIES un’attività batch notturna che interrogherà PST per aggiornare lo stato dei pagamenti.
#### Verifica Stato Bollettino su PagoPA
La funzione permetterà di poter inoltrare e ricevere tramite PST una richiesta in tempo reale sulla stato di pagamento di uno o più bollettini, come risulta su PagoPA. La funzione ricercherà gli ordini di ingiunzione al pagamento con data richiesta e data ricezione valorizzate e presenterà la seguente form:

Da cui selezionando l’azione Visualizza, si riceverà la seguente

In cui l’utente potrà selezionare i bollettini di interesse, spuntando i relativi check box, e provvederà all’Inoltro. Il sistema acquisirà i dati della richiesta e la trasmetterà a PST per l'inoltro a PagoPA e , in attesa dei quali a video apparirà l’immagine di elaborazione in corso

a conclusione della quale apparirà a video il messaggio di avvenuta ricezione dello stato pagamento dei bollettini richiesti. Cliccando su OK, il sistema aggiornerà lo stato dei bollettini sulla base dati di SIES e ripresenterà la form con l’Elenco riportata in precedenza aggiornata.
Base Dati
Saranno aggiunte le seguenti tabelle:

RATEIZZAZIONE_PP      		conterrà i dati relativi alle modalità di pagamento della pena pecuniaria
CIVILMENTE_OBBLIGATO    	conterrà i dati del Civilmente Obbligato al pagamento
BOLLETTINO_PAGOPA    	conterrà i dati del singolo bollettino generato da PagoPA, incluso lo stato di Pagamento
UFFICI_PRODUZIONE	  	conterrà le codifiche degli Uffici Giudiziari, utilizzate da PagoPA, e i relativi valori utilizzati in SIES. Di fatti è una tabella di trascodifica.

Saranno inoltre modificate le seguenti tabelle:

NOTIFICA	aggiunta colonna ID_CIVILMENTE_OBBLIGATO, chiave esterna a
CIVILMENTE_OBBLIGATO
RESIDENZA	aggiunta colonna ID_CIVILMENTE_OBBLIGATO, chiave esterna a
CIVILMENTE_OBBLIGATO
Integrazione servizio PagoPA
Nel presente paragrafo verrà descritta la modalità con la quale SIES verrà collegato al sistema PST e, di riflesso, ai servizi PagoPA.
L’intervento è articolato in due fasi, la prima prevede lo sviluppo di un client che si occupa di invocare un servizio WEB (generaAvviso) che restituisce un bollettino, emesso dall’ente PagoPA, per effettuare un pagamento identificato da un numero univoco (IUV); la seconda prevede lo sviluppo di un batch che, con cadenza giornaliera, interroga un secondo servizio (elencoPagamenti) che, utilizzando l’identificativo di pagamento (IUV) ottenuto in precedenza, è in grado di dire se lo stato del pagamento è eseguito o non ancora eseguito.
Per l’invocazione di entrambi i servizi è necessario implementare un sistema di autenticazione a doppio fattore attraverso un certificato di sicurezza che prevede la condivisione di chiave pubblica tra il sistema chiamante (SIES) ed il sistema ospitante i servizi (PST).

Architettura del servizio
Di seguito si rappresenta brevemente l’architettura di cooperazione del servizio PagoPA/PST con il sistema SIES

In figura troviamo:
Nodi SIES distribuiti sul territorio;
PST, il sistema centralizzato del Portale dei Servizi Telematici (PST) che espone i servizi necessari per generare i bollettini e verifica pagamento.
Configurazione del certificato di comunicazione
Propedeutico alla prosecuzione dei seguenti passi è che il PST fornisca al SIES la chiave pubblica (file in formato “.pem”) associata ai servizi che espongono e che devono essere richiamati; per rendere più chiari i passi descritti di seguito presupporremo che il file si chiami, come in ambiente di collaudo, “processotelematico-giustizia-it.pem”.
Una volta ottenuta la chiave pubblica si dovrà procedere come segue:
Registrazione della chiave pubblica di PagoPA/PST all’interno del Truststore di SIES (sies.jks):
Importare il file processotelematico-giustizia-it.cer in sies.jks
Distribuire il Sies.jks ai vari distretti
Spostare il file sies.jks all’interno del percorso predefinito /var/SIES/CONFIG/certs, sostituendo il precedente file.
Inviare al PST la chiave pubblica contenuta nel Keystore di SIES (serversies.jks): la chiave pubblica è unica per tutti i distretti
Batch di verifica stato del Pagamento
Il batch sviluppato si occuperà, con cadenza giornaliera, di interrogare il servizio esitoPagamenti per conoscere lo stato di un certo pagamento (IUV).
Il batch interrogherà PagoPA per verificare lo stato dei pagamenti dei bollettini presenti sulla tabella “BOLLETTINO_PAGOPA” per i quali non risulta ancora pagato il bollettino (“DATA_AVV_PAGAMENTO” is null e “STATO_PAGAMENTO = NP”) e per i quali le date “DATA_SCADENZA”, “DATA_ULTIMO_CONTROLLO” e  “DATA_GENERAZIONE_BOLLETTINO” soddisfino le condizioni sotto descritte.
Saranno presenti quattro parametri configurabili all’interno del file “f3b.properties”:
inScadenzaTraGiorni = indica il numero di giorni che determinerà l’intervallo di tempo da considerare per selezionare i bollettini, con data scadenza valorizzata, da verificare. La condizione è la seguente:
data_scadenza between sysdate - inScadenzaTraGiorni and sysdate + inScadenzaTraGiorni
Se, quindi, il valore di “inScadenzaTraGiorni” è uguale a 3, si prenderanno in considerazione tutti i bollettini che sono scaduti da massimo tre giorni o che scadranno nei prossimi tre giorni.
Il valore iniziale sarà settato per default a 3.
generatiDaGiorni = indica il numero di giorni che determinerà l’intervallo di tempo da considerare per selezionare i bollettini, privi di Data Scadenza, da verificare.
controllarepergiorni = indica il numero di giorni in cui vanno controllati i bollettini privi di Data Scadenza.
La condizione è la seguente:
or (data_scadenza is null and sysdate >= (data_generazione_bollettino + generatidagiorni)
and sysdate <= (data_generazione_bollettino + generatidagiorni + controllarepergiorni))
Se, quindi, il valore di “generatiDaGiorni” è uguale a 15 e quello di “controllarepergiorni” è pari a 10, si prenderanno in considerazione tutti i bollettini, per i quali non è disponibile la data di scadenza, a partire dal quindicesimo giorno dalla loro generazione e per un massimo di 10 giorni.
Il valore iniziale sarà settato per default a 15 per “generatiDaGiorni” e 10 per “controllarepergiorni”.
controllateDaGiorni = ogni volta che il batch è eseguito, aggiorna per ogni bollettino elaborato, la “DATA_ULTIMO_CONTROLLO” nella tabella “BOLLETTINO_PAGOPA”. Se il valore di “controllateDaGiorni” è diverso da zero, il batch prende in considerazione tutti i bollettini che hanno “DATA_ULTIMO_CONTROLLO < SYSDATE-controllateDaGiorni” di modo da elaborare solo i bollettini che NON sono stati controllati negli ultimi n giorni, di modo da non appesantire le richieste verso PagoPA.
Il valore iniziale sarà settato per default a 0 (ovvero questa condizione non viene presa in considerazione dal batch).
Di seguito un diagramma di flusso che descrive graficamente quanto appena esposto; i parametri “inScadenzaTraGiorni”,  “generatiDaGiorni”, “controllarepergiorni” e “controllateDaGiorni” vengono valorizzati, a titolo esemplificativo, con 3, 15, 10 e 5 rispettivamente.

Il primo parametro, “inScadenzaTraGiorni”, consente di limitare il controllo dello stato del pagamento di un bollettino solo in prossimità della sua scadenza. In assenza della data di scadenza, tramite il secondo parametro, “generatiDaGiorni” ed il terzo parametro “controllarepergiorni”, si può istruire il batch di effettuare comunque il controllo ma solo per un periodo limitato di tempo dal momento della generazione del bollettino. Trascorso tale periodo il bollettino non verrà più controllato dal batch a meno che non venga registrata la data scadenza. Questo per evitare di controllare all'infinito il bollettino. Il controllo potrà comunque essere effettuato manualmente dall'utente direttamente dall'interfaccia del SIEP se e quando ritenuto necessario.
Se un bollettino risulta pagato il batch aggiorna lo stato del pagamento e la data avvenuto pagamento. Inoltre se il pagamento che sta registrando risulterà essere il primo di un pagamento rateizzato, aggiornerà anche la colonna “DATA_SCADENZA” delle altre rate collegate allo stesso ordine di ingiunzione al pagamento. La data scadenza della rate successive è l'ultimo giorno di ogni mese a partire dal mese successivo il pagamento della prima rata.
Questo servizio è stato sviluppato all’interno dello stesso sistema SIES, e verrà schedulato per l’esecuzione attraverso le librerie “quartz” incluse nel progetto stesso.
Verranno aggiunti altri 2 parametri all’interno del file “f3b.properties”, il primo per abilitare/disabilitare il batch ed il secondo per configurarne la schedulazione attraverso la sintassi crontab, che sono:
PagoPaSchedulerEnabled -> True per abilitare il batch/False per disabilitare il batch
PagoPaCronExpression -> Valore espresso attraverso la sintassi crontab. Di default è stata inserita la stringa “0 0 4 * * ?” che rappresenta una schedulazione giornaliera alle 04:00 di ogni giorno.
Di seguito alcuni esempi:

Descrizione dei servizi WEB PST
In questo paragrafo andremo a descrivere i due servizi invocati “elencopagamenti” e “generaAvviso” attraverso l’xsd che li descrive estratto dal relativo wsdl.
Il primo è contenuto all’interno del wsdl ServiziConsultazionePagamentiTelematici.wsdl ed è identificato dal nome unico “elencopagamenti”, mentre il secondo è contenuto in ServiziInvioPagamentiTelematici.wsdl identificato dal nome “generaAvviso”.
#### Servizio elencopagamenti – XSD Request
Il servizio di richiesta (Request) che verrà invocato è il seguente:
<xs:element name='elencoPagamenti' type='tns:elencoPagamenti'/>
È composto dalle seguenti sezioni:
<xs:complexType name='elencoPagamenti'>
<xs:sequence>
<xs:element minOccurs='0' name='codiceCRS' type='xs:string'/>
<xs:element minOccurs='0' name='tipologia' type='xs:string'/>
<xs:element minOccurs='0' name='codiceFiscale' type='xs:string'/>
<xs:element minOccurs='0' name='codiceDistretto' type='xs:string'/>
<xs:element minOccurs='0' name='causale' type='xs:string'/>
<xs:element minOccurs='0' name='stato' type='xs:string'/>
<xs:element minOccurs='0' name='dataRichiestaDa' type='xs:dateTime'/>
<xs:element minOccurs='0' name='dataRichiestaA' type='xs:dateTime'/>
<xs:element name='dimensionePagina' type='xs:int'/>
<xs:element name='numeroPagina' type='xs:int'/>
</xs:sequence>
</xs:complexType>
I primi 5 parametri codiceCRS, tipologia, codiceFiscale, codiceDistretto e causale verranno sempre valorizzati nonostante siano indicati come parametri opzionali.
#### Servizio elencopagamenti – XSD Response
Il servizio di Risposta (Response) è il seguente:
<xs:complexType name='elencoPagamentiResponse'>
Identificato da una sequenza 0…n dei seguenti elementi:
<xs:sequence>
<xs:element minOccurs='0' name='return' type='tns:risultatoRicerca'/>
</xs:sequence>

Ogni elemento di tipo risultatoRicerca è composto da:
<xs:complexType name='risultatoRicerca'>
<xs:sequence>
<xs:element name='count' type='xs:int'/>
<xs:element name='dimensionePagina' type='xs:int'/>
<xs:element maxOccurs='unbounded' minOccurs='0' name='items' type='xs:anyType'/>
<xs:element name='numeroPagina' type='xs:int'/>
</xs:sequence>
</xs:complexType>
#### Servizio generaAvviso – XSD Request
Il servizio di richiesta (Request) che verrà invocato è il seguente:
<xs:element name='generaAvviso' type='tns:generaAvviso'/>
Ed è composto da una sequenza del tipo:
<xs:complexType name='generaAvviso'>
<xs:sequence>
<xs:element minOccurs='0' name='richiestaPagamentoTelematico' type='tns:richiestaPagamentoTelematico'/>
</xs:sequence>
</xs:complexType>
Ognuna articolata come segue:
<xs:complexType name='richiestaPagamentoTelematico'>
<xs:sequence>
<xs:element minOccurs='0' name='codiceDistretto' type='xs:string'/>
<xs:element minOccurs='0' name='codiceUfficio' type='xs:string'/>
<xs:element name='autenticazioneSoggetto' type='xs:string'/>
<xs:element name='soggettoPagatore' type='tns:anagraficaSoggetto'/>
<xs:element minOccurs='0' name='soggettoVersante' type='tns:anagraficaSoggetto'/>
<xs:element name='datiVersamento' type='tns:datiVersamento'/>
<xs:element minOccurs='0' name='dataScadenza' type='xs:dateTime'/>
</xs:sequence>
</xs:complexType>

Questa sezione contiene a sua volta due tipi complessi; il primo anagraficaSoggetto è identificato come segue:
<xs:complexType name='anagraficaSoggetto'>
<xs:sequence>
<xs:element minOccurs='0' name='naturaGiuridica' type='xs:string'/>
<xs:element name='codiceIdentificativoUnivoco' type='xs:string'/>
<xs:element name='nominativo' type='xs:string'/>
<xs:element minOccurs='0' name='indirizzo' type='xs:string'/>
<xs:element minOccurs='0' name='civico' type='xs:string'/>
<xs:element minOccurs='0' name='cap' type='xs:string'/>
<xs:element minOccurs='0' name='localita' type='xs:string'/>
<xs:element minOccurs='0' name='provincia' type='xs:string'/>
<xs:element minOccurs='0' name='regione' type='xs:string'/>
<xs:element minOccurs='0' name='nazione' type='xs:string'/>
<xs:element minOccurs='0' name='email' type='xs:string'/>
</xs:sequence>
</xs:complexType>

Mentre Il secondo datiVersamento è identificato da:
<xs:complexType name='datiVersamento'>
<xs:sequence>
<xs:element name='importoTotale' type='xs:decimal'/>
<xs:element minOccurs='0' name='ibanAddebito' type='xs:string'/>
<xs:element minOccurs='0' name='bicAddebito' type='xs:string'/>
<xs:element maxOccurs='unbounded' name='datiSingoloVersamento' type='tns:datiSingoloVersamento'/>
</xs:sequence>
</xs:complexType>

datiVersamento, a sua volta, contiene il tipo complesso datiSingoloVersamento, articolato in:
<xs:complexType name='datiSingoloVersamento'>
<xs:sequence>
<xs:element name='importo' type='xs:decimal'/>
<xs:element minOccurs='0' name='causale' type='xs:string'/>
<xs:element name='datiSpecificiRiscossione' type='xs:string'/>
<xs:element minOccurs='0' name='datiMarcaBolloDigitale' type='tns:datiMarcaBolloDigitale'/>
</xs:sequence>
</xs:complexType>

Infine, datiSingoloVersamento, contiene il tipo datiMarcaBolloDigitale così descritto:
<xs:complexType name='datiMarcaBolloDigitale'>
<xs:sequence>
<xs:element name='tipoBollo' type='xs:string'/>
<xs:element name='hashDocumento' type='xs:string'/>
<xs:element name='provinciaResidenza' type='xs:string'/>
</xs:sequence>
</xs:complexType>
#### Servizio generaAvviso – XSD Response
Il servizio di Risposta (Response) è il seguente:
<xs:complexType name='generaAvvisoResponse'>
Identificato da una sequenza 0…n dei seguenti elementi:
<xs:sequence>
<xs:element minOccurs='0' name='return' type='tns:esitoGeneraAvviso'/>
</xs:sequence>
Il tipo 'esitoGeneraAvviso' è articolato come segue:
<xs:complexType name='esitoGeneraAvviso'>
<xs:sequence>
<xs:element minOccurs='0' name='bollettino' type='xs:base64Binary'/>
<xs:element minOccurs='0' name='numeroAvviso' type='xs:string'/>
</xs:sequence>
</xs:complexType>
Interventi su RegeWEB
Gestione Oblazione prevista per i procedimenti di competenza del tribunale ordinario
L’Oblazione può essere emessa con ordinanza dal GIP o altro Giudice. Nella schermata di registrazione dell’ordinanza deve essere previsto il campo somma da pagare e la scadenza che devono essere valorizzate dall’utente.
In caso di oblazione per archiviazione totale a seguito di decreto positivo il sistema dovrà modificare la maschera di gestione richieste nel modo seguente, affinché l’utente possa generare il bollettino (pertanto nella casistica specificata il sistema dovrà mostrare il tab “Pagamenti online”):


Figura 1 – Nuova maschera gestione richiesta di oblazione (arch. totale)

Cliccando sull'immagine dell'euro si aprirà la schermata di generazione bollettino:


Figura 2 - Maschera dettaglio per generazione bollettino

N.B.: Sul bollettino viene indicato il totale da pagare (somma da oblare più spese).
Il sistema verificherà se sono stati indicati i dati obbligatori per consentire la generazione del bollettino.
Per produrre l’avviso l’utente deve premere il tasto “Genera Bollettino” e il servizio del PST che genera il bollettino di pagamento (non si prevede rateizzazione in questo caso) provvederà alla restituzione del bollettino e lo IUV che lo identifica univocamente. Il file PDF con il bollettino viene altresì salvato nel sistema associato al decreto e nell’elenco verrà riportato il collegamento al documento che sarà possibile visualizzare.

Figura 3 – Elenco stato di generazione bollettino effettuato

In caso risposta da parte del sistema PST (e quindi di PagoPA) di errori di generazione bollettini, l'applicativo mostrerà l’errore riportato dal servizio.


Figura 4 – Elenco stato di generazione bollettino con errore

Premendo sull’immagine dello stato trasmissione il sistema visualizzerà la maschera con il dettaglio dell’errore generato.

Figura 5 – Dettaglio dell’errore di generazione bollettino
Analogo intervento sarà fatto in caso di richiesta oblazione per archiviazione parziale. Anche in questo caso si accede alla funzione di generazione bollettino dalla maschera di gestione richieste.

Per consentire la generazione degli avvisi, il sistema PST richiede obbligatoriamente la presenza del codice fiscale associato al soggetto e, pertanto, il sistema, qualora il codice fiscale non sia specificato, bloccherà ogni operazione di generazione del bollettino riportando sull’icona un avviso che indica che “Il soggetto non ha il codice fiscale valorizzato”.

Figura 6 – Codice fiscale mancante per il soggetto
L’utente dovrà, quindi accedere ai quadri di gestione dell’imputato cui si riferisce l’oblazione ed inserire il relativo codice fiscale per poi tornare alla funzione di generazione bollettino.
Acquisizione stato pagamenti
Per l’invio della richiesta di pagamento con contestuale degenerazione del relativo identificativo univoco IUV il sistema RGW invocherà un servizio esposto dal PST per generare la richiesta di avvenuto pagamento telematica in base ai parametri specificati derivati dai dati inseriti dagli utenti.
Il batch schedulato, configurabile dal propertiesWS.txt, procederà alla acquisizione delle informazioni dal servizio PST solo nella casistica in cui l’avviso sia stato generato correttamente e registrerà la ricevuta dall’avvenuto pagamento.
Anche nella casistica attuale, qualora siano presenti errori, il sistema riporterà gli errori nell’elenco associato a ciascun avviso riportato in precedenza.


Figura 7 – Stato ricezione con errore
Nella casistica attuale, come per l’errore di generazione del bollettino, si potrà visualizzare il dettaglio dell’errore prodotto premendo sull’icona presente in “Esito Ricezione”


Figura 8 – Dettaglio dell’errore di generazione ricevuta
In caso di esito positivo il sistema visualizzerà l’esito corretto di avvenuto pagamento consentendo all’utente di effettuare il download della ricevuta di avvenuto pagamento.

Figura 9 – Stato di avvenuto corretto pagamento
Gestione Decreto penale per procedimenti di competenza del tribunale ordinario Artt. 459 e 460 cpp
Il decreto penale di condanna viene emesso dal Giudice per le Indagini Preliminari (G.I.P.), su richiesta del Pubblico Ministero (P.M.).
Si dovrà modificare la maschera di gestione richieste come descritto in precedenza per le archiviazioni.
Nel decreto è indicato il totale da pagare con l’avviso che può essere effettuato il pagamento della pena pecuniaria in misura ridotta di un quinto, nel termine di quindici giorni dalla notificazione del decreto, con rinuncia all’opposizione.
In fase di registrazione del dispositivo, qualora siano presenti anche somme provenienti da conversione per sanzioni sostitutive, il sistema considererà l’intero importo cui applicherà la riduzione di 1/5.
Tale importo calcolato, solo nella casistica del Decreto Penale, verrà proposto nel campo “Totale da Pagare” all’atto della generazione del bollettino e la maschera di generazione del bollettino mostrerà il solo campo del totale da pagare in maniera differente rispetto le altre.


Figura 10 - Maschera del dispositivo del decreto penale


Figura 11 - Maschera della generazione bollettino con somma proposta

L’importo specificato dal sistema potrà essere variato dall’utente e procedere alla generazione del bollettino con la somma specificata.

Tale importo, proposto dal sistema o variato dall’utente, verrà indicato come valore per la visualizzazione della “Pena pecuniaria finale esecutiva” nella fase di registrazione dell’attività di “Rinuncia all’opposizione al DP”.

Figura 12 - Maschera dell'attività di rinuncia all’opposizione al DP

Qualora per ciascun indagato\imputato siano presenti più QGF il sistema mostrerà la stessa somma calcolata per tutte le QGF presenti.
Abilitazione pagamenti tramite PagoPA
Il sistema consentirà l’abilitazione della gestione dei pagamenti tramite le funzionalità di PagoPA per le seguenti richieste di:
Archiviazione Totale di Estinzione per oblazione in caso di Decreto Positivo per il giudice unico e giudice di pace
Archiviazione Parziale di Estinzione per oblazione in caso di richiesta accolta per il giudice unico e giudice di pace
Interlocutoria di ammissione all’oblazione per il giudice unico e giudice di pace
Decreto Penale in caso di accoglimento del Decreto Penale
Opposizione al Decreto Penale per ammissione all’oblazione
Piano delle attività
Ciclo di sviluppo
Il ciclo di sviluppo è il classico (waterfall).
Dimensionamento
Stima dell'effort
La stima prevista complessiva è pari a 71. 604,00 €.
Attività progettuali a corpo

|  | N° | € | Totale |
| --- | --- | --- | --- |
|  | REGEWEB | REGEWEB | REGEWEB |
| ADD | 214 | 162 | 34.668,00 € |
| CHG | 14 | 81 | 1.134,00 € |
| DEL | 0 | 16,2 | 0,00 € |
|  | SIES | SIES | SIES |
| ADD | 196 | 162 | 31.752,00 € |
| CHG | 50 | 81 | 4.050,00 € |
| DEL | 0 | 16,2 | 0,00 € |
|  |  |  |  |
|  |  |  | 71.604,00 € |