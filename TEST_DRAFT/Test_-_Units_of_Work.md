---
uniqueName: 01-test-units
displayName: "Test - Units of Work"
category: "TEST_DRAFT"
tags: []
---

# Test — Units of Work
## Progetto: SIES

---

## Functional Area: FA-001 — Validazione Codice Fiscale

| ID | Nome | Descrizione | Actor(s) | Dipendenze |
|---|---|---|---|---|
| UW-001 | Obbligatorietà CF condizionata al paese | Verifica se il paese di nascita è Italia e, solo in quel caso, rende obbligatorio il campo codice fiscale. | Funzionario Amministrativo, Sistema | None |
| UW-002 | Verifica formale del codice fiscale | Controlla che il CF inserito rispetti il formato standard ministeriale (16 caratteri, struttura posizionale, carattere di controllo). | Sistema | UW-001 |
| UW-003 | Calcolo del codice fiscale atteso | Calcola il CF atteso applicando l'algoritmo ministeriale ai dati anagrafici (cognome, nome, data nascita, sesso, comune/stato estero di nascita). | Sistema | None |
| UW-004 | Confronto CF inserito vs CF atteso | Confronta il CF inserito con il CF atteso calcolato e segnala la discrepanza se i valori non coincidono (case-insensitive, tutti i 16 caratteri). | Sistema | UW-002, UW-003 |
| UW-005 | Visualizzazione avviso non bloccante con tipologia anomalia | Mostra un avviso descrittivo con tipologia anomalia (assente / non valido / non congruente) e CF atteso calcolato; il salvataggio rimane sempre consentito. | Funzionario Amministrativo, Sistema | UW-001, UW-002, UW-004 |
| UW-006 | Salvataggio soggetto con avvisi CF presenti | Consente il completamento del salvataggio anche in presenza di avvisi CF, senza bloccare l'operazione. | Funzionario Amministrativo, Sistema | UW-005 |
| UW-007 | Esenzione totale verifiche CF per soggetti stranieri senza CF | Non esegue verifiche né genera avvisi CF quando paese di nascita ≠ Italia e CF è assente. | Sistema | UW-001 |

---

## Functional Area: FA-002 — Bonifica Archivi Preesistenti

| ID | Nome | Descrizione | Actor(s) | Dipendenze |
|---|---|---|---|---|
| UW-008 | Ricerca soggetti con CF assente nati in Italia | Restituisce l'elenco di tutti i soggetti in archivio con paese Italia e codice fiscale vuoto, con indicazione dell'anomalia. | Funzionario Bonifica, Sistema | None |
| UW-009 | Ricerca soggetti con CF formalmente non valido | Restituisce l'elenco di tutti i soggetti il cui CF non supera la verifica formale (stessa logica di UW-002). | Funzionario Bonifica, Sistema | None |
| UW-010 | Ricerca soggetti con CF non congruente con i dati anagrafici | Restituisce l'elenco di tutti i soggetti il cui CF inserito non coincide con il CF calcolato dai dati anagrafici (logica UW-003 + UW-004). | Funzionario Bonifica, Sistema | None |
| UW-011 | Navigazione lista bonifica → scheda soggetto | Consente l'accesso diretto alla scheda soggetto dall'elenco risultati bonifica con un'azione singola, senza passaggi intermedi. | Funzionario Bonifica, Sistema | UW-008, UW-009, UW-010 |
| UW-012 | Esportazione elenco risultati bonifica in formato standard | Genera un file CSV con tutti i soggetti dell'elenco bonifica e la tipologia di anomalia per ciascuno, disponibile per il download. | Funzionario Bonifica, Sistema | UW-008, UW-009, UW-010 |

---

## ⚠️ Ambiguità rilevate

- **UW-003**: comportamento non specificato quando i dati anagrafici sono incompleti (es. comune di nascita mancante): non chiaro se il sistema segnala l'impossibilità di calcolare il CF atteso o salta silenziosamente il confronto.
- **UW-007**: FR-007 copre solo il caso paese ≠ Italia con CF assente. Non specificato se il CF viene validato formalmente per soggetti stranieri che forniscono comunque un CF.
