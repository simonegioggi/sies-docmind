---
uniqueName: 02-test-rules
displayName: "Test - Validation Rules & Behaviours"
category: "TEST_DRAFT"
tags: []
---

# Test — Validation Rules & System Behaviours

## Progetto: SIES

---

## FA-001 — Validazione Codice Fiscale

**UW-001 — Obbligatorietà CF condizionata al paese**

- **Preconditions:** Scheda soggetto aperta (inserimento o modifica). Campo paese di nascita compilato.
- **Input Constraints:** `paisNascita`: stringa/codice. Valori rilevanti: "ITALIA" vs qualsiasi altro.
- **Validation Rules:** VR-001.1: Se paisNascita = ITALIA → CF obbligatorio. VR-001.2: Se paisNascita ≠ ITALIA → CF opzionale.
- **System Behaviours (Success):** Flag CF-obbligatorio determinato; nessun avviso in questo stadio.
- **System Behaviours (Failure):** N/A.
- **Postconditions:** Flag obbligatorietà CF impostato.
- **Edge/Boundary Conditions:** Paese null/non compilato ⚠️; formato campo paese non specificato ⚠️.
- **Error Handling:** Nessuno.
- **⚠️ Gaps:** Comportamento con paese null non definito; formato del valore "ITALIA" (codice vs testo) non specificato.

---

**UW-002 — Verifica formale del codice fiscale**

- **Preconditions:** CF inserito non è vuoto. País = Italia.
- **Input Constraints:** `codiceFiscale`: stringa, esattamente 16 caratteri alfanumerici, struttura posizionale ministeriale.
- **Validation Rules:** VR-002.1: lunghezza = 16. VR-002.2: struttura posizionale conforme. VR-002.3: carattere di controllo coerente con algoritmo ministeriale.
- **System Behaviours (Success):** Esito "CF valido" → input a UW-004.
- **System Behaviours (Failure):** Esito "CF non valido" → innesca UW-005 tipologia *formato non valido*.
- **Postconditions:** Flag `CF_formalmente_valido` determinato.
- **Edge/Boundary Conditions:** Lunghezza 15/17: fallisce. CF con spazi/caratteri speciali: fallisce. Omocodici ⚠️. Case-sensitivity non specificata ⚠️.
- **Error Handling:** Avviso via UW-005; salvataggio non bloccato.
- **⚠️ Gaps:** Verifica case-sensitive o insensitive? Gestione omocodici non definita.

---

**UW-003 — Calcolo del codice fiscale atteso**

- **Preconditions:** Tutti i dati anagrafici disponibili: cognome, nome, dataNascita, sesso (M/F), codice comune ISTAT o codice stato estero.
- **Input Constraints:** cognome (stringa non vuota), nome (stringa non vuota), dataNascita (data), sesso (M/F), codice comune (4 chars) o stato estero (Z+3 cifre).
- **Validation Rules:** VR-003.1÷VR-003.6: estrazione lettere cognome/nome → anno (2 cifre) → lettera mese (tabella ministeriale) → gg+sesso (+40 per F) → codice comune/stato → carattere di controllo.
- **System Behaviours (Success):** CF atteso = stringa 16 caratteri passata a UW-004 e UW-005.
- **System Behaviours (Failure):** Dati incompleti → ⚠️ comportamento non definito.
- **Postconditions:** CF atteso disponibile internamente.
- **Edge/Boundary Conditions:** Nome 1 lettera (X di completamento). Cognome composto ⚠️. Omocodici ⚠️.
- **⚠️ Gaps:** Comportamento con dati incompleti; gestione omocodici; formato codice comune.

---

**UW-004 — Confronto CF inserito vs CF atteso**

- **Preconditions:** CF inserito valido formalmente (UW-002 OK). CF atteso calcolato (UW-003 OK).
- **Input Constraints:** CF inserito: 16 caratteri. CF atteso: 16 caratteri.
- **Validation Rules:** VR-004.1: confronto case-insensitive. VR-004.2: discrepanza in qualsiasi posizione = non congruente.
- **System Behaviours (Success):** CF inserito = CF atteso → esito "congruente"; nessun avviso.
- **System Behaviours (Failure):** CF inserito ≠ CF atteso → esito "non congruente" → UW-005 tipologia *non congruente*.
- **Postconditions:** Flag `CF_congruente` determinato.
- **Edge/Boundary Conditions:** Differenza solo maiuscolo/minuscolo → congruente (case-insensitive). CF omocodice → non congruente se letteralmente diverso.
- **Error Handling:** Avviso via UW-005; salvataggio non bloccato.

---

**UW-005 — Visualizzazione avviso non bloccante**

- **Preconditions:** Almeno una anomalia: CF assente (con obbligo), CF non valido, CF non congruente.
- **Input Constraints:** `tipologiaAnomalia` ∈ {CF_ASSENTE, CF_NON_VALIDO, CF_NON_CONGRUENTE}. `cfAtteso` (quando disponibile).
- **Validation Rules:** VR-005.1: avviso indica la tipologia. VR-005.2: CF atteso sempre affiancato se disponibile. VR-005.3: salvataggio sempre possibile.
- **System Behaviours (Success):** Avviso visibile con tipologia + CF atteso; operatore può procedere o correggere.
- **System Behaviours (Failure):** N/A.
- **Postconditions:** Operatore informato; soggetto salvabile via UW-006.
- **Edge/Boundary Conditions:** CF atteso non calcolabile (dati incompleti) ⚠️. Anomalie multiple ⚠️.
- **⚠️ Gaps:** Avviso senza CF atteso se dati incompleti; gestione anomalie multiple.

---

**UW-006 — Salvataggio soggetto con avvisi CF presenti**

- **Preconditions:** Operatore ha visto l'avviso CF e decide di salvare.
- **Validation Rules:** VR-006.1: salvataggio mai bloccato da anomalie CF.
- **System Behaviours (Success):** Soggetto persistito in archivio con CF nella forma inserita (anche anomala).
- **Postconditions:** Soggetto salvato; visibile nelle ricerche bonifica.

---

**UW-007 — Esenzione verifiche CF per stranieri senza CF**

- **Preconditions:** País ≠ Italia. CF vuoto/null.
- **Validation Rules:** VR-007.1: bypass totale UW-001÷005. VR-007.2: nessun avviso generato.
- **System Behaviours (Success):** Salvataggio diretto senza avvisi CF.
- **Postconditions:** Soggetto salvato senza anomalie CF registrate.
- **Edge/Boundary Conditions:** Straniero con CF presente ⚠️.
- **⚠️ Gaps:** Comportamento soggetto straniero con CF fornito non definito.

---

## FA-002 — Bonifica Archivi Preesistenti

**UW-008 — Ricerca CF assente nati in Italia**

- **Preconditions:** Utente role-002 con accesso modulo bonifica. Archivio soggetti accessibile.
- **Validation Rules:** VR-008.1: ricerca sull'intero archivio. VR-008.2: filtro paisNascita=ITALIA AND CF=vuoto.
- **System Behaviours (Success):** Elenco soggetti con ID, dati anagrafici principali, tipologia = "CF assente".
- **System Behaviours (Failure):** Nessun risultato → messaggio "nessun risultato".
- **Edge/Boundary Conditions:** Archivio vuoto → "nessun risultato". 10.000 soggetti → &lt; 60s. Timeout ⚠️. Paginazione ⚠️.

---

**UW-009 — Ricerca CF formalmente non valido**

- **Preconditions:** Stesse di UW-008.
- **Validation Rules:** VR-009.1: stessa logica verifica formale UW-002 applicata a tutto l'archivio (solo soggetti con CF presente).
- **System Behaviours (Success):** Elenco soggetti; tipologia = "CF non valido".
- **Edge/Boundary Conditions:** Performance &lt; 60s (NFR-002). Timeout ⚠️.

---

**UW-010 — Ricerca CF non congruente**

- **Preconditions:** Stesse di UW-008.
- **Validation Rules:** VR-010.1: calcolo CF atteso + confronto per ogni soggetto con CF presente e formalmente valido.
- **System Behaviours (Success):** Elenco soggetti; tipologia = "CF non congruente".
- **Edge/Boundary Conditions:** Ricerca più onerosa. Performance &lt; 60s. Soggetti con dati incompleti ⚠️.
- **⚠️ Gaps:** Trattamento soggetti con dati anagrafici incompleti nella ricerca non definito.

---

**UW-011 — Navigazione lista bonifica → scheda soggetto**

- **Preconditions:** Lista bonifica visualizzata. Soggetto selezionato.
- **Validation Rules:** VR-011.1: navigazione con un'azione singola, senza passaggi intermedi.
- **System Behaviours (Success):** Scheda soggetto aperta in modalità modifica.
- **System Behaviours (Failure):** Soggetto eliminato nel frattempo ⚠️.
- **⚠️ Gaps:** Gestione concorrenza non definita.

---

**UW-012 — Esportazione lista bonifica**

- **Preconditions:** Lista bonifica visualizzata. Utente role-002.
- **Validation Rules:** VR-012.1: esportazione completa. VR-012.2: CSV include ID, dati anagrafici, tipologia anomalia.
- **System Behaviours (Success):** File CSV disponibile per download.
- **System Behaviours (Failure):** Errore generazione file ⚠️.
- **Edge/Boundary Conditions:** Lista vuota ⚠️. 10.000 soggetti: performance export non definita ⚠️.
- **⚠️ Gaps:** Lista vuota; performance export; errore generazione.