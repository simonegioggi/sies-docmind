---
uniqueName: interventi-su-modalit-pagamento
displayName: "Interventi su Modalit\u00e0 Pagamento"
category: "GENERAL"
tags: []
---

# Interventi su Modalità Pagamento

> **File originale:** `MEV/SCHEDA_033/Interventi su Modalità Pagamento.docx`  
> **Tipo:** DOCX

---

Interventi su Modalità Pagamento
L’attuale funzione attivabile dal Dettaglio Pena Complessiva rimane inalterata, bisogna però permettere la gestione della stessa, anche su procedimento validato, per cui si aggiungerà nella tool bar del Dettaglio Procedimento, la voce

Selezionandola il Sistema richiamerà l’attuale Dettaglio Modalità pagamento p.p., che in caso di assenza di records RATEIZZAZIONE_PP, invierà la form di Inserimento (l’attuale)

Con la differenza che il campo Importo da pagare sarà precompilato, solo se provengo da Dettaglio Pena Complessiva, negli altri casi sarà vuoto, ma obbligatorio da compilare.
In caso di esistenza di precedenti Modalità di pagamento la form di Dettaglio potrebbe presentarsi come di seguito

oppure

In cui la funzione di Inserimento è attivabile solo se al procedimento non vi sono RATEIZZAZIONE_PP, con provvedimento emesso (EVE_ID_EVENTO  valorizzato e con Evento validato o annullato) oppure prive di RATEIZZAZIONE_PP.
Le funzioni di modifica e di cancellazione saranno attivabili sull’ultima modalità di pagamento dell’elenco, se la stessa risulta priva di provvedimento. Es.

Nella funzione di rideterminazione pena, al momento della selezione, il sistema deve controllare se sia già presente un Ordine di Ingiunzione  (06- 0622  validato) recupera l’importo da pagare, calcola l’importo pagato e presenta la form di inserimento descritta in precedenza, in cui saranno visualizzati i suddetti importi, il campo Importo da Pagare non valorizzato e Tipo Rateizzazione bloccata su Unica soluzione

A seguito della Conferma il sistema invierà la form di Rideterminazione pena, realizzata da Simone.
Segnalo che quando si seleziona la funzione Rideterminazione Pena, scatta il seguente controllo

che non permette di proseguire con la compilazione della form.
Il controllo (“è già stato emesso OI per tutte le rate previste”) dovrebbe scattare quando sull’ultima rateizzazione_pp, collegata ad un ordine di ingiunzione validato, l’importo_pagato = importo da pagare (2023 / 20007).