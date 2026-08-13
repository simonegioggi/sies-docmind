---
uniqueName: sintesi-flusso-pagopa-sistemi-penali-coinvolti-06-
displayName: "Sintesi Flusso PagoPa Sistemi Penali coinvolti  06 02 2023 "
category: "GENERAL"
tags: []
---

# Sintesi Flusso PagoPa-Sistemi Penali coinvolti (06.02.2023)

> **File originale:** `MEV/SCHEDA_013/Docs/Test/Sintesi Flusso PagoPa-Sistemi Penali coinvolti (06.02.2023).docx`  
> **Tipo:** DOCX

---

# Riforma Cartabia – Pagamenti PagoPA Pene pecuniarie
Sistemi penali coinvolti: WFM (Cognizione) SIES (Esecuzione)
Servizi PST da interfacciare:
Invocare un servizio per la generazione del Bollettino (quando viene creato un bollettino viene in automatico generato uno stato ad esso associato, identificativo IUV).
Invocare un servizio per avere aggiornamenti sullo stato del bollettino.
Flusso:
Generazione bollettino (Sistema Penale -> PST): Quando viene generato un atto esecutivo o provvedimento del giudice con obbligo di pagamento, o altri eventi (ad esempio proroga di un pagamento scaduto) sarà possibile effettuare l’azione “Genera Bollettino”, richiamando il servizio del PST che genera il bollettino di pagamento e eventualmente anche quello rateizzato. Il servizio del PST restituisce il bollettino e lo IUV che lo identifica univocamente.
Il sistema penale mostrerà all’utente (cancelliere?) un record con le informazioni opportune (IUV, scadenza, stato, link al pdf).
Tasto STAMPA: l’utente dovrà poter stampare il bollettino che verrà consegnato al destinatario finale che dovrà procedere al pagamento (online o presso qualsiasi sportello).
Aggiornamento STATO (Sistema Penale -> PST): il sistema penale invocherà il servizio del PST (una volta al giorno) per aggiornare lo stato del pagamento. Infatti, quando verrà effettuato il pagamento il PST (collegandosi a PagoPA) si aggiorna di conseguenza.
I sistemi penali verranno aggiornati in base allo stato del pagamento, ed alla scadenza andrà scatenata un’azione (alert o simili) di notifica sul sistema.
Note:
Se il pagamento scade non è più possibile pagarlo, ed in caso di proroga da parte del giudice sarà necessario generare un nuovo, in questo caso riabilitando il tasto “Genera Bollettino”. Questo dovrà accadere anche in caso di rate non pagate totalmente ( magari capiamo che bollettino va generato in caso di pagamento parziale.
L’IBAN di riferimento sarà uno solo e verrà associato dal servizio che verrà realizzato lato PST appositamente per questa interazione.