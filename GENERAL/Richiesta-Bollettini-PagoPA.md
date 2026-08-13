---
uniqueName: richiesta-bollettini-pagopa
displayName: "Richiesta Bollettini PagoPA"
category: "GENERAL"
tags: []
---

# Richiesta Bollettini PagoPA

> **File originale:** `MEV/SCHEDA_013/Docs/Test/Richiesta Bollettini PagoPA.docx`  
> **Tipo:** DOCX

---

Gestione Bollettini PagoPA
Selezionando la voce di menu Gestione Bollettini PagoPA, il sistema presenterà la seguente form:

Richiesta Bollettini
Da Richiesta Bollettini sarà possibile inoltrare la Richiesta dei bollettini di pagamento a PagoPA, aprendo una popup con la richiesta e rimarrà in attesa della risposta. All’arrivo della risposta l’utente la selezionerà ed il sistema provvederà ad importare i bollettini nella base dati associandoli al procedimento e all’atto.
La funzione presenterà la seguente form, in cui saranno presentati gli ordini di esecuzione di ingiunzione al pagamento validati (EVENTO con cod_tipo_provvedimento = 06 e cod_motivo= 0622) , eventualmente con la data di richiesta e ricezione (da prelevare dalle colonne “DATA_TRASMISSIONE_ATTI” e “DATA_RICEZIONE_ATTI” della tabella “EVENTO”).

I due provvedimenti riportati sono solo l'esempio di una delle due possibili modalità di pagamento riportata nell'Ordine di Ingiunzione. A fronte dell'ordine di interesse, selezionando l'icona “Inoltra”, il sistema acquisisce la data della richiesta e la trasmette a PST per l'inoltro a PagoPA e apre una popup nella quale riceverà i bollettini generati.
Al momento della selezione dell’azione di Inoltra, bisognerà popolare la tabella BOLLETTINO_PAGOPA inserendo un numero di record pari al numero di rate contenute nell’ordine di ingiunzione (records della tabella RATEIZZAZIONE_PP, collegati tramite “EVE_ID_EVENTO” al provvedimento selezionato) + 1 bollettino con l’intero importo, nel caso che il condannato decidesse il pagamento in unica rata.

Da cui selezionando il tasto  li importa in SIES (aggiorna la tabella BOLLETTINO_PAGOPA) e chiude la popup. Il sistema valorizzerà la data di ricezione. Selezionando l'icona “Visualizza”, il sistema richiamerà la funzione Verifica Stato Pagamenti. Se si ritorna nella  form di richiesta, risulteranno valorizzate le date di Richiesta e di Ricezione, non sarà più abilitata l'azione di Inoltra, ma sarà possibile solo la Visualizzazione dei singoli bollettini.
Verifica Stato Pagamenti
La funzione richiamabile dal menu di Gestione Bollettini o dalla funzione Richiesta Bollettini fornisce l’Elenco dei Bollettini generati da PagoPA e il relativo Stato Pagamenti.
Il sistema ricercherà gli OE di Ingiunzione al pagamento emessi e validati per il procedimento corrente, visualizzando la data di Richiesta e Ricezione Generazione Bollettini PagoPA, presentando per quelli con le due date valorizzate l’icona di Dettaglio:

Selezionando l’azione di Dettaglio, il sistema presenterà l’elenco dei bollettini con il relativo stato pagamento:

Lo stato del singolo pagamento sarà aggiornato automaticamente, differito di un giorno, da PagoPA man mano che l’utente provvederà al pagamento. In effetti vi sarà lato SIES un’attività batch notturna che interrogherà PST per aggiornare lo stato dei pagamenti.