---
uniqueName: mysiut-sies-mu-1-0-20240130-manualeutente202333pst
displayName: "MY SIUT SIES MU 1 0 20240130 Manuale Utente 2023 33 PST PagoPA Step 1"
category: "GENERAL"
tags: []
---

# MY_SIUT-SIES-MU-1.0-20240130-Manuale_Utente_2023_33_PST_PagoPA_Step-1

> **File originale:** `MEV/SCHEDA_033/MY_SIUT-SIES-MU-1.0-20240130-Manuale_Utente_2023_33_PST_PagoPA_Step-1.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Vito Bufi - Umberto Mignogna |  |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 30/01/2024 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 30/01/2024 | Prima Emissione |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Aurora Garofalo | Amministrazione |  | Responsabile Unico Procedimento |
| Dott. Oris Orlando | Amministrazione |  | Direttore Esecutivo Contratto |
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
1	Introduzione	5
1.1	Scopo del documento	5
1.2	Riferimenti	5
1.3	Glossario	5
1.3.1	Acronimi e abbreviazioni	5
2	Iscrizione Procedimento	7
2.1	Iscrizione Pena Complessiva	7
2.2	Modalità Pagamento Pena Pecuniaria	9
2.3	Civilmente Obbligato per la Pena Pecuniaria	12
3	Gestione Riscossione Pene Pecuniarie	16
3.1	Ordine di ingiunzione Pagamento	16
3.2	Gestione Ordine Ingiunzione	19
3.2.1	Notifiche	19
3.3	Gestione Bollettini PagoPA	21
3.3.1	Richiesta Bollettini	21
3.3.2	Verifica Stato Pagamenti	23
3.3.3	Verifica Stato Bollettino su PagoPA	24

Introduzione
Scopo del documento
Nel documento in oggetto si delineano gli interventi effettuati sul sistema SIES in merito al pagamento delle pene pecuniarie anche attraverso l’interfacciamento del PagoPA/PST mediante l’invocazione dei seguenti servizi:
Servizio per la generazione del Bollettino (quando viene creato un bollettino viene in automatico generato uno stato ad esso associato, identificativo IUV);
Servizio per avere aggiornamenti sullo stato del bollettino.
Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF 1 | ? | Richiesta Scheda |
| RIF 2 | ? | Atti Cognizione |

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

Iscrizione Procedimento
Iscrizione Pena Complessiva
Nella form di Iscrizione Pene Complessiva è stata aggiunta una nuova sezione per l’acquisizione dei dati relativi alle Pene Sostitutive delle Pene Detentive Brevi


in cui è possibile gestire le seguenti tipologie di pena



La valorizzazione della sezione Sanzione Sostituiva è alternativa alla valorizzazione della sezione Pene Sostitutive delle Pene Detentive Brevi. La nuova sezione sarà riportata anche nelle form di Dettaglio, quando valorizzata, e Modifica.

A seguito della Conferma il sistema inserirà i dati nella base dati e invierà la form di Dettaglio


in cui, nella  combo box delle azioni, sono state aggiunte due nuove voci “Modalità Pagamento Pena Pecuniaria”, “Civilmente Obbligato per la Pena Pecuniaria”



Da questa form è inoltre possibile:

selezionare l’azione di Modifica, ricevendo la form



da cui è possibile procedere alla modifica dei dati


Selezionare l’azione di cancellazione, ricevendo la form



da cui è possibile procedere alla cancellazione dei dati.
Modalità Pagamento Pena Pecuniaria
La funzione consente di gestire la modalità di pagamento della pena pecuniaria come stabilita dal giudice della cognizione in sentenza. Per tale motivo la funzione è abilitata solo su procedimento in stato di iscritto

Selezionando questa voce dal Dettaglio della Pena Complessiva



il sistema controlla se nella base dati risulta già inserita tale informazione, in caso di esistenza presenterà la form di Dettaglio, in caso di assenza presenterà la form di inserimento



Le due modalità di pagamento (unica soluzione o pagamento rateale) sono ovviamente alternative. In caso di pagamento rateizzato la form inibisce la sezione relativa al pagamento Unica Soluzione e abilita quella per il Pagamento Rateizzato



L’importo da pagare è uguale alla somma degli importi (riportati nella prima parte della form, per la Pena Pecuniaria e per la Pena Pecuniaria sostitutiva) inseriti in fase di iscrizione sentenza: è comunque modificabile.

Gli importi complessivi indicati in Pagamento Unica Soluzione o Pagamento Rateizzato dovrebbero di norma essere uguali a quanto indicato in Importo da Pagare, ma nel caso che differissero, in fase di Conferma il sistema invia il seguente messaggio



Che consente di continuare con l’inserimento o annullare l’operazione e correggere i dati in maschera.

Il Numero giorni scadenza è obbligatorio, in caso di non valorizzazione del campo, il sistema invia il seguente messaggio bloccante



A seguito della conferma il sistema aggiornerà la base dati e presenterà la form di Dettaglio



Da cui sarà possibile procedere alla Modifica o alla Cancellazione dei dati.

Selezionando l’azione di modifica  si riceverà la form


dopo aver aggiornato i dati di interesse, a seguito della Conferma, il sistema aggiornerà la base dati e ripresenterà la form di Dettaglio.

Selezionando l’azione di cancellazione   si riceverà il seguente messaggio per la conferma a procedere alla cancellazione



Cliccando su OK, il sistema aggiornerà la base dati e tornerà sul Dettaglio della Pena Complessiva.
Civilmente Obbligato per la Pena Pecuniaria
La funzione consente di gestire la Persona Fisica/Giuridica civilmente obbligata al pagamento della pena pecuniaria, in caso di mancato pagamento da parte del Condannato, come indicato dal giudice della cognizione in sentenza o successivamente alla decisione della Sorveglianza o del GE. Per tale motivo la funzione sarà abilitata solo su procedimento in stato di iscritto.
Selezionando questa voce dal Dettaglio della Pena Complessiva



il sistema controlla se nella base dati risulta già inserita tale informazione, in caso di esistenza presenterà la form di Dettaglio, in caso di assenza presenterà la form di inserimento, impostata di default su persona fisica



In cui nella combo box Qualifica saranno presenti le seguenti voci



Selezionando una delle voci differenti da ‘-‘, la form si modifica presentando i campi per l’inserimento di una seconda persona Civilmente Obbligata



L’inserimento della seconda persona Civilmente obbligata assume la stessa Qualifica della prima persona.
L’inserimento della seconda persona Civilmente obbligata non è obbligatoria.
In caso di selezione del radio button su persona giuridica  la form si modificherà in



In cui nella combo box della qualifica sono riportate sempre le stesse voci, viste in precedenza, ma in questo caso non sarà presentata una seconda sezione per l’inserimento di una seconda parte Civilmente Obbligata. E’ consentito l’inserimento di una unica persona giuridica civilmente obbligata.

A seguito della conferma il sistema presenterà la seguente form di Dettaglio



Da cui è possibile procedere alla Modifica o alla Cancellazione dei dati oppure richiamare la funzione di Gestione del Difensore della persona Civilmente Obbligata. Il link Gestione Difensore è solo CLICCABILE, nel qual caso il sistema invierà il seguente messaggio



Selezionando l’azione di modifica  si riceve la form



dopo aver aggiornato i dati di interesse, a seguito della Conferma, il sistema aggiornerà la base dati e ripresenterà la form di Dettaglio.

Selezionando l’azione di cancellazione   si riceve il seguente messaggio per la conferma a procedere alla cancellazione



Cliccando su OK, il sistema aggiornerà la base dati e tornerà sul Dettaglio della Pena Complessiva.

Gestione Riscossione Pene Pecuniarie
Per la gestione di tutti gli aspetti connessi alla riscossione delle Pene Pecuniarie e delle Pene Sostitutive si è intervenuti nell’attuale  menu delle funzioni che il sistema presenta selezionando la voce Gestione Altre Sanzioni



aggiungendo due nuove voci, di seguito racchiuse nel riquadro in rosso



Al momento entrambi le voci presenteranno lo stesso nuovo menu di funzioni


Ordine di ingiunzione Pagamento
La funzione consente di inserire l’Ordine di ingiunzione al pagamento della pena pecuniaria al Condannato, al Civilmente obbligato e ai rispettivi Difensori, verificando che risultino obbligatoriamente già inseriti i dati delle modalità di pagamento



La form presenta i dati di dettaglio delle modalità di pagamento e del Civilmente Obbligato, se presente, e le autorità destinatarie delegate alla notifica dell’atto al Condannato, al Difensore ed al Civilmente Obbligato.

A seguito della completa compilazione dei campi della form e della relativa Conferma, il sistema inserisce un Ordine Esecuzione di Ingiunzione al pagamento nella base dati e presenta la form di Dettaglio.



Da questa form è possibile procedere:

Alla Modifica dell’ordine



alla stampa dell’Ordine di Ingiunzione al Pagamento, in unica soluzione o rateizzato e successivamente procedere alla validazione del provvedimento. A tal fine sono stati realizzati i due template SIEP_PP_OI_PAGAMENTO_UN.rtf e SIEP_PP_OI_PAGAMENTO_RR.rtf, che saranno richiamati automaticamente dal sistema in base alla modalità di pagamento;
alla validazione del provvedimento, a seguito della quale lo stato procedimento sarà impostato a Emesso Ordine esecuzione di Ingiunzione al Pagamento della Pena Pecuniaria;
ad accedere alla funzione Notifiche per annotare le date di avvenuta notifica del provvedimento, cliccando sul link .

Il nuovo provvedimento sarà riportato nell’Elenco Provvedimenti del PM, rispettandone tutte le regole previste per gli altri provvedimenti di SIEP


Gestione Ordine Ingiunzione
Selezionando la voce di menu Gestione Ordine Ingiunzione, il sistema presenta la seguente form


Notifiche
La funzione permette di annotare le date di avvenuta notifica dell’ordine ingiunzione alle parti destinarie man mano che pervengono all’ufficio. Al momento dell’annotazione della data di avvenuta notifica al condannato dell’ unico bollettino o del primo bollettino, in caso di rateizzazione, il sistema provvederà a  far scattare gli scadenzari , relativi al pagamento dei singoli bollettini.

La funzione è attivabile dal precedente menu o dal dettaglio dell’Ordine di esecuzione di Ingiunzione al Pagamento cliccando sul link . In caso di avvenuta valorizzazione di almeno una data notifica, il sistema presenterà la form di Dettaglio, in assenza di tutte le date di Notifica presenterà la form di Inserimento



Per acquisire la data dell’avvenuta notifica l’utente dovrà valorizzare il campo Data Notifica per ciascuna della parti per cui risulta già effettuata la notifica, spuntando eventualmente la check box  per l’indicazione dell’autorità che ha effettuato la notifica, se diversa da quella indicata nell’Ordine di Ingiunzione. A seguito della Conferma, il sistema acquisirà i dati e invierà la form di Dettaglio.



Da cui selezionando l’icona di modifica si riceverà la precedente form di inserimento che permetterà di valorizzare le date mancanti e di modificare o cancellare le date già valorizzate, impostandole a spazio.
Gestione Bollettini PagoPA
Selezionando la voce di menu Gestione Bollettini PagoPA, il sistema presenta la seguente form


Richiesta Bollettini
Da Richiesta Bollettini è possibile inoltrare la Richiesta dei bollettini di  pagamento a PagoPA, preparare  l’elenco dei bollettini da richiedere a PagoPA e rimanere in attesa della risposta. All’arrivo della risposta il sistema acquisirà per ciascun bollettino lo IUV e il relativo documento (formato pdf).
Prerequisito per poter richiedere la generazione dei bollettini a PagoPA è la valorizzazione del Codice Fiscale del condannato, per cui il sistema effettuerà un controllo preventivo sulla presenza del dato nella base dati. In caso di assenza invierà il seguente messaggio

cliccando su OK il sistema presenterà la form di Modifica Soggetto per l’acquisizione del dato. Successivamente alla valorizzazione del codice fiscale, sarà possibile rieseguire la funzione, che ricerca l’ordine di ingiunzione al pagamento validato e presenta la form


selezionando l'icona Inoltra  il sistema acquisisce la data della richiesta e prepara l’elenco dei bollettini da trasmettere a PST per l'inoltro a pagoPA e presenta la seguente form

Da cui selezionando il tasto  il sistema inoltrerà la richiesta e rimarrà in attesa della ricezione dei bollettini, in attesa dei quali a video apparirà l’immagine di elaborazione in corso

a conclusione della quale apparirà a video il seguente messaggio

Cliccando su OK, il sistema aggiorna la base dati di SIES con i dati ricevuti e presenta la form di richiesta

simile alla prima form, ma con Data Richiesta e Data Ricezione valorizzate e priva del tasto Inoltra, cliccando sull’icona Visualizza il sistema presenterà l’elenco dei bollettini completi dello IUV e del documento pdf

Per ciascun bollettino sarà possibile stampare il documento in formato pdf, selezionando l’icona di stampa.
Se si ritorna nella  form di richiesta, risulteranno valorizzate le date di Richiesta e di Ricezione, non sarà più abilitata l'azione di Inoltra, ma sarà possibile solo la Visualizzazione dei singoli bollettini.
Verifica Stato Pagamenti
La funzione richiamabile dal menu di Gestione Bollettini o dalla funzione Richiesta Bollettini fornisce  l’Elenco degli ordini di Ingiunzione validati per cui risultano valorizzate la Data_Richiesta e la Data_Ricezione, quindi con Bollettini PagoPA già generati



Selezionando l’azione Visualizza si riceverà l’Elenco dei Bollettini generati da PagoPA e il relativo Stato Pagamenti



Lo stato del singolo pagamento sarà aggiornato automaticamente, differito di un giorno, da PagoPA man mano che l’utente provvederà al pagamento. In effetti vi sarà lato SIES un’attività batch notturna che interrogherà PST per aggiornare lo stato dei pagamenti.
Verifica Stato Bollettino su PagoPA
La funzione permetterà di poter inoltrare e ricevere tramite PST una richiesta in tempo reale sulla stato di pagamento di uno o più bollettini, come risulta su PagoPA. La funzione ricercherà gli ordini di ingiunzione al pagamento con data richiesta e data ricezione valorizzate e presenterà la seguente form:


Da cui selezionando l’azione Visualizza, si riceverà la seguente

In cui l’utente potrà selezionare i bollettini di interesse, spuntando i relativi check box, e provvederà all’Inoltro. Il sistema acquisirà i dati della richiesta e la trasmetterà a PST per l'inoltro a PagoPA e , in attesa dei quali a video apparirà l’immagine di elaborazione in corso

a conclusione della quale apparirà a video il messaggio di avvenuta ricezione dello stato pagamento dei bollettini richiesti

Cliccando su OK, il sistema aggiornerà lo stato dei bollettini sulla base dati di SIES e ripresenterà la form con l’Elenco riportata in precedenza aggiornata