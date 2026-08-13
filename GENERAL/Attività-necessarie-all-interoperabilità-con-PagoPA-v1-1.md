---
uniqueName: attivit-necessarie-all-interoperabilit-con-pagopa-
displayName: "Attivit\u00e0 necessarie all interoperabilit\u00e0 con PagoPA v1 1"
category: "GENERAL"
tags: []
---

# Attività necessarie all'interoperabilità con PagoPA-v1.1

> **File originale:** `MEV/SCHEDA_013/Docs/Test/Attività necessarie all'interoperabilità con PagoPA-v1.1.docx`  
> **Tipo:** DOCX

---

Attività necessarie all’adeguamento di SIEP per interoperabilità con PagoPA
Iscrizione Procedimento

1a	Iscrizione Pena Complessiva
Aggiornamento delle attuali form Inserimento, Modifica e Dettaglio con l’aggiunta del “Lavoro pubblica utilità” nella combo-box delle Sanzioni Sostitutive

Nella form di Dettaglio Pena Complessiva,nella combo box delle azioni saranno aggiunte due nuove voci “Modalità Pagamento Pena Pecuniaria”, “Civilmente Obbligato Pena Pecuniria”

1b	Modalità Pagamento Pena Pecuniaria
La funzione consentirà di gestire la modalità di pagamento della pena pecuniaria come stabilità dal giudice della cognizione in sentenza o successivamente alla decisione della Sorveglianza o del GE. Per tale motivo la funzione sarà abilitata sia su procedimento in stato di iscritto, sia su procedimento già validato.
Selezionando questa voce, il sistema controllerà se nella base dati risulta già inserita tale informazione, in caso di esistenza presenterà la form di Dettaglio, in caso di assenza presenterà la form di inserimento

In cui le due modalità di pagamento sono ovviamente alternative. Gli importi complessivi indicati in pagamento unica soluzione o rateizzato deve essere uguale a quanto indicato in importo da pagare.

Quesito: l’importo da pagare è sempre uguale alla somma degli importi riportati, nella prima parte della form, per la pena pecuniara e per la Pena Pecuniaria sostitutiva?
A seguito della conferma il sistema presenterà la seguente form di Dettaglio

Da cui sarà possibile procedere alla Modifica o alla Cancellazione dei dati.
1c	Civilmente Obbligato Pena Pecuniaria
La funzione consentirà di gestire la Persona Fisica/Giuridica civilmente obbligata al pagamento della pena pecuniaria in caso di mancato pagamento da parte del Condannato come indicato dal giudice della cognizione in sentenza o successivamente alla decisione della Sorveglianza o del GE. Per tale motivo la funzione sarà abilitata sia su procedimento in stato di iscritto, sia su procedimento già validato.
Selezionando questa voce, il sistema controllerà se nella base dati risulta già inserita tale informazione, in caso di esistenza presenterà la form di Dettaglio, in caso di assenza presenterà la form di inserimento

Quesito: vi può essere più di una occorrenza?
A seguito della conferma il sistema presenterà la seguente form di Dettaglio

Da cui sarà possibile procedere alla Modifica o alla Cancellazione dei dati oppure richiamare la funzione di Gestione del Difensore della persona Civilmente obbligata (n.b. la funzione non sarà realizzata entro il 15 marzo).




1d	Ulteriori interventi da realizzare al di fuori  della MEV 2023-13
inserimento di form intermedia per quantificazione dettagliata della sanzione che si sostituisce, aggiunta del Lavoro pubblica utilità nelle tipologie Sanzioni Sostitutive. Conseguente aggiornamento funzioni Dettaglio, Modifica, Cancellazione
gestione quantificazione Lavoro pubblica utilità (inserimento, dettaglio, modifica, cancellazione)

Gestione Riscossione Pene Pecuniarie

Per la gestione di tutti gli aspetti connessi alla riscossione delle PenePecuniarie si aggiungerà nella parte bassa del menu verticale di SIEP una nuova voce



Che a sua volta presenterà il seguente menu orizzontale


2a	Ordine di ingiunzione Pagamento
La funzione consentirà di inserire l’Ordine di ingiunzione al pagamento della pena pecuniaria al Condannato, al Civilmente obbligato e ai rispettivi Difensori, verificando che risultino obbligatoriamente già inseriti i dati delle modalità di pagamento

La form presenta i dati di dettaglio delle modalità di pagamento, dando la possibilità di accedere alla form di modifica degli stessi, lo specifico link, e i dati del Civilmente Obbligato, se presente, dando la possibilità di inserirlo o modificarlo, selezionando l’apposito link.
A seguito della completa compilazione dei campi della form e della relativa Conferma, il sistema inserisce un Ordine Esecuzione di Ingiunzione al pagamento e presenta la form di Dettaglio

Da cui sarà possibile  inoltrare la Richiesta dei bollettini di  pagamento a pagoPA, cliccando sullo specifico link, che aprirà una popup con la richiesta e rimarrà in attesa della risposta. All’arrivo della risposta l’utente la selezionerà, il sistema provvederrà ad importare i bollettini nella base dati associandoli al procedimento e all’atto.
Solo dopo la ricezione dei bollettini di pagamento sarà possibile a procedere alla stampa dell’Ordine di Ingiunzione al Pagamento, in unica soluzione o rateizzato, e dei relativi bollettini, e procedere alla validazione del provvedimento.
Il nuovo provvedimento sarà riportato nell’Elenco Provvedimenti del PM

2b	Gestione Ordine Ingiunzione

Selezionando la voce di menu Gestione Ordine Ingiunzione, il sistema presenterà la seguente form



In questa MEV sarà realizzata solo la funzione di Notifica che permetterà di far scattare gli scadenzari e che provvederà ad annotare nella base dati SIES le date di scadenza dei singoli bollettini.
2c	Gestione Bollettini PagoPA
Selezionando la voce di menu Gestione Ordine Ingiunzione, il sistema presenterà la seguente form


In questa MEV saranno realizzate solo le funzioni Richiesta Bollettini, Verifica Stato Pagamenti, Annotazione Avvenuto Pagamento.
2d	Scadenzari – in questa MEV solo Bollettini in scadenza entro tot n.ro giorni
2e	Conversione Pene Pecuniarie (richiamo delle attuali funzionalità disponibili in Gestione
Altre Sanzioni, che dovranno essere aggiornate per la gestione anche del Lavoro Pubblica 	utilità)

Realizzazione infrastruttura, web services e quant’altro.