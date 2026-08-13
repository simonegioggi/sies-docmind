---
uniqueName: verifica-stato-pagamenti
displayName: "Verifica Stato Pagamenti"
category: "GENERAL"
tags: []
---

# Verifica Stato Pagamenti

> **File originale:** `MEV/SCHEDA_013/Docs/Test/Verifica Stato Pagamenti.docx`  
> **Tipo:** DOCX

---

Verifica Stato Pagamenti
La funzione richiamabile dal menu di Gestione Bollettini o dalla funzione Richiesta Bollettini fornisce l’Elenco dei Bollettini generati da PagoPA e il relativo Stato Pagamenti
Il sistema ricercherà gli OE di Ingiunzione al pagamento emessi e validati per il procedimento corrente, visualizzando la data di Richiesta e Ricezione Generazione Bollettini PagoPA, presentando per quelli con le due date valorizzate l’icona di Dettaglio

Selezionando l’azione di Dettaglio, il sistema presenterà l’elenco dei bollettini con il relativo stato pagamento

Lo stato del singolo pagamento sarà aggiornato automaticamente, differito di un giorno, da pagoPA man mano che l’utente provvederà al pagamento. In effetti vi sarà lato SIES un’attività batch notturna che interrogherà PST per aggiornare lo stato dei pagamenti.