---
uniqueName: modifiche-siep-a-seguito-aggiornamento-pst
displayName: "Modifiche SIEP a seguito aggiornamento PST"
category: "GENERAL"
tags: []
---

# Modifiche SIEP a seguito aggiornamento PST

> **File originale:** `MEV/SCHEDA_033/NOTE RILASCIO DGSIA/Modifiche SIEP a seguito aggiornamento PST.docx`  
> **Tipo:** DOCX

---


A seguito delle implementazioni apportate a PST/pagoPA in merito alla generazione bollettini, nella call del 18/10/2023 è stato deciso di apportare le seguenti modifiche lato SIEP:
Modifica controllo su presenza Codice Fiscale del condannato
Al momento, quando in SIEP si chiede di generare i Bollettini PagoPA, il sistema controlla che sul condannato sia obbligatoriamente valorizzato il codice fiscale, inviando in caso di assenza del dato il seguente messaggio bloccante

Non essendo più questo dato obbligatorio per PST, si è deciso di modificare il controllo sulla presenza del Codice Fiscale da obbligatorio a facoltativo, modificando il messaggio come di seguito

Dando quindi la possibilità all’utente di procedere senza valorizzazione del dato (OK) o di valorizzarlo utilizzando la funzione di Modifica Anagrafica (Annulla).
Modifica valorizzazione Data scadenza pagamento
Vista l’impossibilità di poter indicare una data di scadenza reale sui bollettini, essendo la stessa calcolabile solo dopo l’annotazione della data di avvenuta notifica dell’ordine di ingiunzione al condannato, si era deciso nell’ambito della MEV33 di impostare la data di scadenza a 120 gg dall’emissione dell’ordine di ingiunzione in caso di pagamento in unica soluzione e a 60 gg in caso di pagamento rateizzato, prevedendo in quest’ultimo caso di poter generare il primo bollettino al momento dell’emissione dell’ordine di ingiunzione e di generare gli altri successivamente all’avvenuta annotazione nel sistema della data di avvenuta notifica.
Essendo anche la Data scadenza del pagamento un dato non più obbligatorio per PST è stato deciso di non valorizzare su SIEP alcuna data scadenza al momento della generazione del bollettino (pagamento unica soluzione), primo bollettino (pagamento rateizzato) o tutti i bollettini (pagamento rateizzato). In caso di pagamento rateizzato con generazione bollettini in 2 momenti separati, il primo bollettino sarebbe privo di data scadenza, mentre quelli generati successivamente all’annotazione della data di avvenuta notifica riporterebbero la data scadenza reale, calcolata da SIEP.