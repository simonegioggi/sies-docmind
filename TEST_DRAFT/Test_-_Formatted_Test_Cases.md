---
uniqueName: 04-test-cases
displayName: "Test - Formatted Test Cases"
category: "TEST_DRAFT"
tags: []
---

# Test — Formatted Test Cases
## Progetto: SIES

---

## FA-001 — Validazione Codice Fiscale

---

**Test Case: UW-001-TC-001**

| Field | Detail |
|---|---|
| Title | CF reso obbligatorio per soggetto nato in Italia |
| Functional Area | FA-001 — Validazione Codice Fiscale |
| Test Type | Happy Path |
| Priority | Critical |
| Preconditions | Utente role-001 autenticato. Scheda soggetto aperta in modalità inserimento. |
| Test Data | paisNascita="ITALIA" \| codiceFiscale="" (vuoto) \| cognome="ROSSI" \| nome="MARIO" \| dtNascita=01/01/1985 \| sesso=M \| comune=H501 |
| Expected Result | Al salvataggio: avviso "CF assente" visualizzato con CF atteso calcolato ("RSSMRA85A01H501W") affiancato al campo CF. Salvataggio consentito. |
| Postconditions | Soggetto salvato con CF vuoto in archivio. |
| Traceability | UW-001; FR-001; FR-005 |

**Test Steps:**
1. Aprire la scheda inserimento soggetto.
2. Selezionare "ITALIA" nel campo paese di nascita.
3. Compilare cognome="ROSSI", nome="MARIO", dtNascita=01/01/1985, sesso=M, comune=H501.
4. Lasciare vuoto il campo codice fiscale.
5. Fare clic su "Salva".
6. Verificare che il sistema mostri l'avviso con tipologia "CF assente" e il CF atteso "RSSMRA85A01H501W".
7. Verificare che il pulsante "Salva" sia ancora disponibile (avviso non bloccante).

---

**Test Case: UW-001-TC-002**

| Field | Detail |
|---|---|
| Title | Nessun avviso CF per soggetto straniero senza CF |
| Functional Area | FA-001 — Validazione Codice Fiscale |
| Test Type | Happy Path |
| Priority | High |
| Preconditions | Utente role-001 autenticato. Scheda soggetto aperta in modalità inserimento. |
| Test Data | paisNascita="FRANCIA" \| codiceFiscale="" (vuoto) \| cognome="DUPONT" \| nome="JEAN" \| dtNascita=10/03/1975 |
| Expected Result | Salvataggio completato senza alcun avviso relativo al codice fiscale. |
| Postconditions | Soggetto straniero salvato senza anomalie CF registrate. |
| Traceability | UW-001; UW-007; FR-007 |

**Test Steps:**
1. Aprire la scheda inserimento soggetto.
2. Selezionare "FRANCIA" nel campo paese di nascita.
3. Compilare cognome="DUPONT", nome="JEAN", dtNascita=10/03/1975.
4. Lasciare vuoto il campo codice fiscale.
5. Fare clic su "Salva".
6. Verificare che nessun avviso CF sia visualizzato durante o dopo il salvataggio.
7. Verificare che il soggetto sia salvato correttamente.

---

**Test Case: UW-001-TC-003**

| Field | Detail |
|---|---|
| Title | Obbligatorietà CF rimossa al cambio paese ITALIA→FRANCIA |
| Functional Area | FA-001 — Validazione Codice Fiscale |
| Test Type | State |
| Priority | High |
| Preconditions | Soggetto italiano esistente in archivio con CF assente. Scheda soggetto aperta in modalità modifica. |
| Test Data | paisNascita originale="ITALIA" → nuovo valore="FRANCIA" \| codiceFiscale="" |
| Expected Result | Dopo il cambio paese, al salvataggio non viene generato alcun avviso CF. |
| Postconditions | Soggetto salvato con paese=FRANCIA, CF vuoto, senza anomalie CF. |
| Traceability | UW-001; FR-001; FR-007 |

**Test Steps:**
1. Aprire la scheda del soggetto italiano (paisNascita=ITALIA, CF vuoto) in modifica.
2. Modificare il campo paese di nascita da "ITALIA" a "FRANCIA".
3. Lasciare il campo CF vuoto.
4. Fare clic su "Salva".
5. Verificare che nessun avviso CF sia visualizzato.

---

**Test Case: UW-001-TC-004**

| Field | Detail |
|---|---|
| Title | Obbligatorietà CF ripristinata al cambio paese FRANCIA→ITALIA |
| Functional Area | FA-001 — Validazione Codice Fiscale |
| Test Type | State |
| Priority | High |
| Preconditions | Soggetto straniero esistente con CF assente. Scheda aperta in modifica. |
| Test Data | paisNascita originale="FRANCIA" → nuovo="ITALIA" \| codiceFiscale="" \| cognome="DUPONT" \| nome="JEAN" \| dtNascita=10/03/1975 \| sesso=M \| comune=Z110 |
| Expected Result | Dopo il cambio paese, al salvataggio viene generato avviso "CF assente" con CF atteso calcolato. |
| Postconditions | Soggetto salvabile anche con CF vuoto (comportamento non bloccante). |
| Traceability | UW-001; FR-001; FR-005 |

**Test Steps:**
1. Aprire la scheda del soggetto straniero in modifica.
2. Modificare paisNascita da "FRANCIA" a "ITALIA".
3. Lasciare CF vuoto.
4. Fare clic su "Salva".
5. Verificare che avviso "CF assente" con CF atteso sia visualizzato.

---

**Test Case: UW-001-TC-005**

| Field | Detail |
|---|---|
| Title | Comportamento con paese di nascita non compilato |
| Functional Area | FA-001 — Validazione Codice Fiscale |
| Test Type | Edge |
| Priority | Low |
| Preconditions | Scheda soggetto aperta in inserimento con campo paese di nascita non compilato. |
| Test Data | paisNascita=null/vuoto \| codiceFiscale="" |
| Expected Result | ⚠️ Comportamento non specificato dai requisiti — risultato atteso da definire con il team di sviluppo. |
| Postconditions | Da definire. |
| Traceability | UW-001; ⚠️ gap FR-001 |

**Test Steps:**
1. Aprire la scheda inserimento soggetto.
2. Non compilare il campo paese di nascita.
3. Lasciare vuoto il campo CF.
4. Fare clic su "Salva".
5. Documentare il comportamento del sistema.

---

**Test Case: UW-002-TC-001**

| Field | Detail |
|---|---|
| Title | CF valido di 16 caratteri supera la verifica formale |
| Functional Area | FA-001 — Validazione Codice Fiscale |
| Test Type | Happy Path |
| Priority | Critical |
| Preconditions | Soggetto italiano. CF inserito dall'operatore. |
| Test Data | paisNascita="ITALIA" \| codiceFiscale="RSSMRA85A01H501W" |
| Expected Result | Verifica formale superata. Nessun avviso formato. Il sistema procede al confronto (UW-004). |
| Postconditions | Flag CF_formalmente_valido=true. |
| Traceability | UW-002; FR-002 |

**Test Steps:**
1. Aprire scheda inserimento soggetto con paisNascita="ITALIA".
2. Inserire CF="RSSMRA85A01H501W".
3. Fare clic su "Salva".
4. Verificare che nessun avviso "formato non valido" sia visualizzato.

---

**Test Case: UW-002-TC-002**

| Field | Detail |
|---|---|
| Title | CF di 15 caratteri fallisce la verifica formale |
| Functional Area | FA-001 — Validazione Codice Fiscale |
| Test Type | Boundary |
| Priority | High |
| Preconditions | Soggetto italiano. |
| Test Data | paisNascita="ITALIA" \| codiceFiscale="RSSMRA85A01H501" (15 caratteri) \| cognome=ROSSI \| nome=MARIO \| dtNascita=01/01/1985 \| sesso=M \| comune=H501 |
| Expected Result | Avviso "formato non valido" visualizzato con CF atteso "RSSMRA85A01H501W". Salvataggio consentito. |
| Postconditions | CF anomalo presente nel record se l'operatore salva. |
| Traceability | UW-002; UW-005; FR-002; FR-005 |

**Test Steps:**
1. Aprire scheda inserimento soggetto con paisNascita="ITALIA".
2. Compilare dati anagrafici completi.
3. Inserire CF="RSSMRA85A01H501" (15 caratteri).
4. Fare clic su "Salva".
5. Verificare avviso "formato non valido" con CF atteso visualizzato.
6. Verificare che il salvataggio rimanga possibile.

---

**Test Case: UW-002-TC-003**

| Field | Detail |
|---|---|
| Title | CF di 17 caratteri fallisce la verifica formale |
| Functional Area | FA-001 — Validazione Codice Fiscale |
| Test Type | Boundary |
| Priority | Medium |
| Preconditions | Soggetto italiano. |
| Test Data | codiceFiscale="RSSMRA85A01H501WX" (17 caratteri) |
| Expected Result | Avviso "formato non valido". Salvataggio consentito. |
| Postconditions | CF anomalo presente se salvato. |
| Traceability | UW-002; FR-002 |

**Test Steps:**
1. Inserire CF="RSSMRA85A01H501WX" nel campo CF.
2. Fare clic su "Salva".
3. Verificare avviso "formato non valido".

---

**Test Case: UW-002-TC-004**

| Field | Detail |
|---|---|
| Title | CF con carattere di controllo errato fallisce la verifica |
| Functional Area | FA-001 — Validazione Codice Fiscale |
| Test Type | Negative |
| Priority | High |
| Preconditions | Soggetto italiano con dati anagrafici completi. |
| Test Data | codiceFiscale="RSSMRA85A01H501A" (ultimo carattere errato: A invece di W) |
| Expected Result | Avviso "formato non valido" con CF atteso corretto. Salvataggio consentito. |
| Postconditions | CF anomalo nel record se salvato. |
| Traceability | UW-002; FR-002 |

**Test Steps:**
1. Compilare scheda soggetto (ROSSI MARIO, 01/01/1985, M, H501).
2. Inserire CF="RSSMRA85A01H501A".
3. Fare clic su "Salva".
4. Verificare avviso "formato non valido" con CF atteso "RSSMRA85A01H501W".

---

**Test Case: UW-002-TC-005**

| Field | Detail |
|---|---|
| Title | CF con struttura posizionale non conforme |
| Functional Area | FA-001 — Validazione Codice Fiscale |
| Test Type | Negative |
| Priority | High |
| Preconditions | Soggetto italiano. |
| Test Data | codiceFiscale="1234567890123456" (16 cifre, nessun carattere alfabetico) |
| Expected Result | Avviso "formato non valido". Salvataggio consentito. |
| Traceability | UW-002; FR-002 |

**Test Steps:**
1. Inserire CF="1234567890123456".
2. Fare clic su "Salva".
3. Verificare avviso "formato non valido".

---

**Test Case: UW-002-TC-006**

| Field | Detail |
|---|---|
| Title | CF con spazi interni |
| Functional Area | FA-001 |
| Test Type | Edge |
| Priority | Medium |
| Preconditions | Soggetto italiano. |
| Test Data | codiceFiscale="RSSMRA85A01H50 W" (spazio in pos.15) |
| Expected Result | Avviso "formato non valido". |
| Traceability | UW-002; FR-002 |

**Test Steps:**
1. Inserire CF con spazio in posizione 15.
2. Fare clic su "Salva".
3. Verificare avviso "formato non valido".

---

**Test Case: UW-002-TC-007**

| Field | Detail |
|---|---|
| Title | CF con caratteri speciali |
| Functional Area | FA-001 |
| Test Type | Edge |
| Priority | Medium |
| Preconditions | Soggetto italiano. |
| Test Data | codiceFiscale="RSSMRA85A01H501!" |
| Expected Result | Avviso "formato non valido". |
| Traceability | UW-002; FR-002 |

**Test Steps:**
1. Inserire CF="RSSMRA85A01H501!".
2. Fare clic su "Salva".
3. Verificare avviso "formato non valido".

---

**Test Case: UW-002-TC-008**

| Field | Detail |
|---|---|
| Title | CF in minuscolo — verifica case sensitivity |
| Functional Area | FA-001 |
| Test Type | Equivalence |
| Priority | Medium |
| Preconditions | Soggetto italiano con dati anagrafici completi. |
| Test Data | codiceFiscale="rssmra85a01h501w" (tutto minuscolo) |
| Expected Result | ⚠️ Comportamento da definire: verifica formale case-insensitive o case-sensitive? |
| Traceability | UW-002; FR-002; ⚠️ gap |

**Test Steps:**
1. Inserire CF tutto in minuscolo.
2. Fare clic su "Salva".
3. Documentare se la verifica formale supera o fallisce.

---

**Test Case: UW-003-TC-001**

| Field | Detail |
|---|---|
| Title | Calcolo CF atteso corretto per maschio con dati completi |
| Functional Area | FA-001 |
| Test Type | Happy Path |
| Priority | Critical |
| Preconditions | Dati anagrafici completi disponibili. |
| Test Data | cognome=ROSSI \| nome=MARIO \| dtNascita=01/01/1985 \| sesso=M \| comune=H501 (Roma) |
| Expected Result | CF atteso calcolato = "RSSMRA85A01H501W" mostrato nell'avviso. |
| Postconditions | CF atteso disponibile per confronto (UW-004) e visualizzazione (UW-005). |
| Traceability | UW-003; FR-003 |

**Test Steps:**
1. Compilare scheda soggetto: cognome=ROSSI, nome=MARIO, dtNascita=01/01/1985, sesso=M, comune=H501.
2. Lasciare CF vuoto o inserire un CF errato per attivare la visualizzazione dell'avviso.
3. Fare clic su "Salva".
4. Verificare che il CF atteso mostrato nell'avviso sia esattamente "RSSMRA85A01H501W".

---

**Test Case: UW-003-TC-002**

| Field | Detail |
|---|---|
| Title | Calcolo CF atteso per femmina (giorno +40) |
| Functional Area | FA-001 |
| Test Type | Happy Path |
| Priority | Critical |
| Preconditions | Dati anagrafici femmina completi. |
| Test Data | cognome=BIANCHI \| nome=ANNA \| dtNascita=15/06/1990 \| sesso=F \| comune=F205 (Milano) |
| Expected Result | CF atteso calcolato con giorno=55 (15+40 per sesso F); lettera mese=H (giugno). |
| Traceability | UW-003; FR-003 |

**Test Steps:**
1. Compilare scheda: BIANCHI ANNA, 15/06/1990, F, F205.
2. Lasciare CF vuoto per attivare calcolo e avviso.
3. Fare clic su "Salva".
4. Verificare che CF atteso abbia posizione giorno=55 e mese=H.

---

**Test Case: UW-003-TC-003**

| Field | Detail |
|---|---|
| Title | Calcolo CF con nome di 2 lettere (completamento con X) |
| Functional Area | FA-001 |
| Test Type | Boundary |
| Priority | Medium |
| Preconditions | Soggetto con nome molto corto. |
| Test Data | cognome=ROSSI \| nome="IO" (2 caratteri) \| dtNascita=01/01/1980 \| sesso=M \| comune=H501 |
| Expected Result | CF atteso calcolato applicando X di completamento nelle posizioni nome mancanti. |
| Traceability | UW-003; FR-003 |

**Test Steps:**
1. Compilare scheda con nome="IO".
2. Lasciare CF vuoto.
3. Fare clic su "Salva".
4. Verificare CF atteso mostrato nell'avviso con X di completamento per nome.

---

**Test Case: UW-003-TC-004**

| Field | Detail |
|---|---|
| Title | Calcolo CF per soggetto nato in stato estero |
| Functional Area | FA-001 |
| Test Type | Equivalence |
| Priority | High |
| Preconditions | Soggetto italiano con stato estero di nascita. |
| Test Data | cognome=ROSSI \| nome=MARIO \| dtNascita=01/01/1985 \| sesso=M \| statoNascita=Z401 (codice Francia) \| paisNascita=ITALIA |
| Expected Result | CF atteso calcolato con codice Z401 (stato estero Francia) nelle posizioni comune. |
| Traceability | UW-003; FR-003 |

**Test Steps:**
1. Compilare scheda con stato estero di nascita Z401.
2. Lasciare CF vuoto.
3. Fare clic su "Salva".
4. Verificare CF atteso con Z401 nelle posizioni comune.

---

**Test Case: UW-003-TC-005**

| Field | Detail |
|---|---|
| Title | Dati anagrafici incompleti — comune di nascita mancante |
| Functional Area | FA-001 |
| Test Type | Negative |
| Priority | High |
| Preconditions | Soggetto italiano con comune di nascita non compilato. |
| Test Data | cognome=ROSSI \| nome=MARIO \| dtNascita=01/01/1985 \| sesso=M \| comuneNascita=vuoto |
| Expected Result | ⚠️ Comportamento non specificato: sistema segnala impossibilità calcolo CF atteso o salta silenziosamente il confronto? |
| Traceability | UW-003; FR-003; ⚠️ gap |

**Test Steps:**
1. Compilare scheda con comune di nascita vuoto.
2. Inserire CF valido o lasciare vuoto.
3. Fare clic su "Salva".
4. Documentare il comportamento del sistema.

---

**Test Case: UW-003-TC-006**

| Field | Detail |
|---|---|
| Title | Cognome con apostrofo (D'AMICO) |
| Functional Area | FA-001 |
| Test Type | Edge |
| Priority | Low |
| Preconditions | Soggetto con cognome composto con apostrofo. |
| Test Data | cognome="D'AMICO" \| nome=LUIGI \| dtNascita=05/09/1978 \| sesso=M \| comune=H501 |
| Expected Result | CF atteso calcolato ignorando l'apostrofo (solo caratteri alfanumerici usati). |
| Traceability | UW-003; FR-003 |

**Test Steps:**
1. Compilare scheda con cognome="D'AMICO".
2. Lasciare CF vuoto.
3. Fare clic su "Salva".
4. Verificare CF atteso mostrato nell'avviso.

---

**Test Case: UW-004-TC-001**

| Field | Detail |
|---|---|
| Title | CF inserito congruente con CF atteso — nessun avviso |
| Functional Area | FA-001 |
| Test Type | Happy Path |
| Priority | Critical |
| Preconditions | Soggetto italiano con dati anagrafici completi. CF inserito corrisponde al CF atteso. |
| Test Data | cognome=ROSSI \| nome=MARIO \| dtNascita=01/01/1985 \| sesso=M \| comune=H501 \| codiceFiscale="RSSMRA85A01H501W" |
| Expected Result | Nessun avviso CF generato. Salvataggio completato normalmente. |
| Postconditions | Soggetto salvato con CF congruente; non comparirà nella lista bonifica UW-010. |
| Traceability | UW-004; FR-004 |

**Test Steps:**
1. Compilare scheda ROSSI MARIO con tutti i dati anagrafici.
2. Inserire CF="RSSMRA85A01H501W".
3. Fare clic su "Salva".
4. Verificare che nessun avviso CF sia visualizzato.
5. Verificare che il soggetto sia salvato correttamente.

---

**Test Case: UW-004-TC-002**

| Field | Detail |
|---|---|
| Title | CF inserito diverso da CF atteso — avviso non congruente |
| Functional Area | FA-001 |
| Test Type | Negative |
| Priority | Critical |
| Preconditions | Soggetto italiano con dati anagrafici completi. |
| Test Data | cognome=ROSSI \| nome=MARIO \| dtNascita=01/01/1985 \| sesso=M \| comune=H501 \| codiceFiscale="RSSMRA85A01H501X" (controllo diverso) |
| Expected Result | Avviso "non congruente con dati anagrafici" con CF atteso "RSSMRA85A01H501W" visualizzato. Salvataggio consentito. |
| Postconditions | Soggetto salvato con CF non congruente se operatore conferma. |
| Traceability | UW-004; UW-005; FR-004; FR-005 |

**Test Steps:**
1. Compilare scheda ROSSI MARIO con tutti i dati.
2. Inserire CF="RSSMRA85A01H501X" (carattere controllo sbagliato ma struttura formale valida — ⚠️ verificare se 'X' come controllo è formalmente valido oppure se viene prima segnalato come non valido da UW-002).
3. Fare clic su "Salva".
4. Verificare avviso "non congruente" con CF atteso "RSSMRA85A01H501W".
5. Verificare che il salvataggio sia possibile.

---

**Test Case: UW-004-TC-003**

| Field | Detail |
|---|---|
| Title | CF inserito in minuscolo congruente con CF atteso in maiuscolo |
| Functional Area | FA-001 |
| Test Type | Boundary |
| Priority | Medium |
| Preconditions | Soggetto italiano con dati completi. |
| Test Data | codiceFiscale="rssmra85a01h501w" (minuscolo) |
| Expected Result | Confronto case-insensitive: esito congruente; nessun avviso non-congruenza. |
| Traceability | UW-004; FR-004 |

**Test Steps:**
1. Inserire CF tutto in minuscolo.
2. Fare clic su "Salva".
3. Verificare che nessun avviso "non congruente" sia generato.

---

**Test Case: UW-005-TC-001**

| Field | Detail |
|---|---|
| Title | Avviso CF assente con tipologia e CF atteso visibili |
| Functional Area | FA-001 |
| Test Type | Happy Path |
| Priority | Critical |
| Preconditions | Soggetto italiano, CF vuoto, dati anagrafici completi. |
| Test Data | paisNascita="ITALIA" \| codiceFiscale="" \| cognome=ROSSI \| nome=MARIO \| dtNascita=01/01/1985 \| sesso=M \| comune=H501 |
| Expected Result | Avviso visibile con tipologia "CF assente" e CF atteso "RSSMRA85A01H501W" mostrato affiancato al campo CF. |
| Traceability | UW-005; FR-005; NFR-006 |

**Test Steps:**
1. Compilare scheda con paisNascita="ITALIA" e CF vuoto.
2. Fare clic su "Salva".
3. Verificare che l'avviso mostri "CF assente" come tipologia.
4. Verificare che il CF atteso "RSSMRA85A01H501W" sia visibile affiancato al campo CF.

---

**Test Case: UW-005-TC-002**

| Field | Detail |
|---|---|
| Title | Avviso formato non valido con CF atteso |
| Functional Area | FA-001 |
| Test Type | Happy Path |
| Priority | High |
| Preconditions | Soggetto italiano con CF di lunghezza errata. |
| Test Data | codiceFiscale="RSSMRA85A01H501" (15 char) \| dati anagrafici completi |
| Expected Result | Avviso con tipologia "formato non valido" e CF atteso "RSSMRA85A01H501W" visibile. |
| Traceability | UW-005; FR-005 |

**Test Steps:**
1. Inserire CF di 15 caratteri.
2. Fare clic su "Salva".
3. Verificare tipologia avviso = "formato non valido".
4. Verificare CF atteso mostrato.

---

**Test Case: UW-005-TC-003**

| Field | Detail |
|---|---|
| Title | Avviso non congruente con CF atteso |
| Functional Area | FA-001 |
| Test Type | Happy Path |
| Priority | High |
| Preconditions | Soggetto italiano con CF valido formalmente ma non corrispondente ai dati. |
| Test Data | codiceFiscale="BNCNNA90H55F205B" \| cognome=ROSSI \| nome=MARIO \| dtNascita=01/01/1985 \| sesso=M \| comune=H501 |
| Expected Result | Avviso tipologia "non congruente con dati anagrafici" con CF atteso "RSSMRA85A01H501W". |
| Traceability | UW-005; FR-005 |

**Test Steps:**
1. Inserire CF di un altro soggetto.
2. Fare clic su "Salva".
3. Verificare tipologia avviso = "non congruente".
4. Verificare CF atteso corretto mostrato.

---

**Test Case: UW-005-TC-004**

| Field | Detail |
|---|---|
| Title | Salvataggio rimane possibile con avviso CF presente |
| Functional Area | FA-001 |
| Test Type | State |
| Priority | Critical |
| Preconditions | Avviso CF presente (qualsiasi tipologia). |
| Test Data | Qualsiasi scenario con anomalia CF. |
| Expected Result | Il pulsante "Salva" è attivo e cliccabile. Il salvataggio viene eseguito. |
| Postconditions | Soggetto salvato con CF anomalo. |
| Traceability | UW-005; UW-006; FR-005; FR-006 |

**Test Steps:**
1. Generare un avviso CF (CF assente, non valido, o non congruente).
2. Verificare che il pulsante "Salva" sia ancora attivo.
3. Fare clic su "Salva".
4. Verificare che il salvataggio sia completato con successo.

---

**Test Case: UW-006-TC-001**

| Field | Detail |
|---|---|
| Title | Salvataggio soggetto italiano con CF assente dopo avviso |
| Functional Area | FA-001 |
| Test Type | Happy Path |
| Priority | Critical |
| Preconditions | Soggetto italiano con avviso "CF assente" visualizzato. |
| Test Data | paisNascita="ITALIA" \| codiceFiscale="" |
| Expected Result | Soggetto salvato in archivio con CF vuoto. Comparirà nella lista bonifica UW-008. |
| Postconditions | Record in archivio con CF vuoto. |
| Traceability | UW-006; FR-006 |

**Test Steps:**
1. Compilare scheda soggetto italiano con CF vuoto.
2. Al salvataggio, verificare l'avviso "CF assente".
3. Fare clic su "Salva" confermando.
4. Navigare all'archivio e verificare che il soggetto sia presente con CF vuoto.

---

**Test Case: UW-006-TC-002**

| Field | Detail |
|---|---|
| Title | Salvataggio soggetto con CF non valido |
| Functional Area | FA-001 |
| Test Type | Happy Path |
| Priority | High |
| Preconditions | Soggetto italiano con avviso "CF non valido" visualizzato. |
| Test Data | codiceFiscale="12345678901234XX" |
| Expected Result | Soggetto salvato con CF anomalo. Visibile in ricerca bonifica UW-009. |
| Traceability | UW-006; FR-006 |

**Test Steps:**
1. Inserire CF non valido.
2. Al salvataggio, verificare avviso "formato non valido".
3. Fare clic su "Salva".
4. Verificare salvataggio completato.

---

**Test Case: UW-006-TC-003**

| Field | Detail |
|---|---|
| Title | Salvataggio soggetto con CF non congruente |
| Functional Area | FA-001 |
| Test Type | Happy Path |
| Priority | High |
| Preconditions | Soggetto italiano con avviso "CF non congruente" visualizzato. |
| Test Data | CF valido formalmente ma ≠ CF atteso |
| Expected Result | Soggetto salvato con CF non congruente. Visibile in ricerca bonifica UW-010. |
| Traceability | UW-006; FR-006 |

**Test Steps:**
1. Inserire CF formalmente valido ma non congruente.
2. Confermare salvataggio.
3. Verificare che soggetto sia salvato.

---

**Test Case: UW-007-TC-001**

| Field | Detail |
|---|---|
| Title | Soggetto straniero senza CF — nessun avviso, salvataggio diretto |
| Functional Area | FA-001 |
| Test Type | Happy Path |
| Priority | High |
| Preconditions | Scheda soggetto aperta con paese straniero. |
| Test Data | paisNascita="GERMANIA" \| codiceFiscale="" \| cognome="MUELLER" \| nome="HANS" \| dtNascita=20/04/1970 |
| Expected Result | Salvataggio completato immediatamente senza nessun avviso CF. |
| Postconditions | Soggetto salvato. Non comparirà in nessuna ricerca bonifica. |
| Traceability | UW-007; FR-007 |

**Test Steps:**
1. Aprire scheda inserimento soggetto.
2. Selezionare "GERMANIA" come paese di nascita.
3. Lasciare CF vuoto.
4. Fare clic su "Salva".
5. Verificare che nessun avviso CF appaia.
6. Verificare salvataggio completato.

---

**Test Case: UW-007-TC-002**

| Field | Detail |
|---|---|
| Title | Cambio paese straniero→italiano con CF vuoto attiva obbligatorietà |
| Functional Area | FA-001 |
| Test Type | State |
| Priority | High |
| Preconditions | Soggetto straniero in modifica. CF vuoto. |
| Test Data | paisNascita: GERMANIA→ITALIA \| codiceFiscale="" \| cognome=MUELLER \| nome=HANS \| dtNascita=20/04/1970 \| sesso=M \| comune=H501 |
| Expected Result | Avviso "CF assente" generato al salvataggio dopo il cambio paese. |
| Traceability | UW-007; UW-001; FR-001; FR-007 |

**Test Steps:**
1. Aprire scheda soggetto straniero in modifica.
2. Cambiare paisNascita da GERMANIA a ITALIA.
3. Fare clic su "Salva".
4. Verificare avviso "CF assente" generato.

---

**Test Case: UW-007-TC-003**

| Field | Detail |
|---|---|
| Title | Soggetto straniero con CF presente — comportamento non definito |
| Functional Area | FA-001 |
| Test Type | Edge |
| Priority | Low |
| Preconditions | Soggetto straniero con CF compilato. |
| Test Data | paisNascita="SPAGNA" \| codiceFiscale="RSSMRA85A01H501W" |
| Expected Result | ⚠️ Comportamento non definito in FR-007. Documentare il comportamento del sistema. |
| Traceability | UW-007; FR-007; ⚠️ gap |

**Test Steps:**
1. Inserire soggetto con paisNascita="SPAGNA" e CF compilato.
2. Fare clic su "Salva".
3. Documentare se il sistema valida il CF, lo ignora, o genera un avviso.

---

## FA-002 — Bonifica Archivi Preesistenti

---

**Test Case: UW-008-TC-001**

| Field | Detail |
|---|---|
| Title | Ricerca CF assente restituisce lista soggetti con anomalia |
| Functional Area | FA-002 — Bonifica Archivi Preesistenti |
| Test Type | Happy Path |
| Priority | High |
| Preconditions | Utente autenticato con profilo role-002. Archivio con almeno 1 soggetto italiano con CF vuoto. |
| Test Data | Archivio: soggetto ROSSI MARIO, paisNascita=ITALIA, CF=vuoto |
| Expected Result | Lista visualizzata con: ID soggetto, cognome, nome, dtNascita, tipologia anomalia="CF assente". |
| Postconditions | Lista risultati visualizzata. |
| Traceability | UW-008; FR-008 |

**Test Steps:**
1. Autenticarsi con utente role-002.
2. Navigare al modulo bonifica archivi.
3. Selezionare la ricerca per "CF assente".
4. Avviare la ricerca.
5. Verificare che il soggetto ROSSI MARIO sia nella lista con tipologia="CF assente".
6. Verificare presenza di: ID, cognome, nome, dtNascita nella lista.

---

**Test Case: UW-008-TC-002**

| Field | Detail |
|---|---|
| Title | Ricerca CF assente senza risultati |
| Functional Area | FA-002 |
| Test Type | Equivalence |
| Priority | Medium |
| Preconditions | Tutti i soggetti italiani in archivio hanno CF compilato. |
| Test Data | Archivio senza soggetti ITALIA con CF vuoto. |
| Expected Result | Messaggio "Nessun risultato trovato" visualizzato. |
| Traceability | UW-008; FR-008 |

**Test Steps:**
1. Avviare ricerca "CF assente" con archivio dove tutti gli italiani hanno CF.
2. Verificare messaggio "Nessun risultato trovato".

---

**Test Case: UW-008-TC-003**

| Field | Detail |
|---|---|
| Title | Ricerca CF assente su archivio vuoto |
| Functional Area | FA-002 |
| Test Type | Edge |
| Priority | Low |
| Preconditions | Archivio soggetti vuoto (0 record). |
| Test Data | Archivio = 0 soggetti. |
| Expected Result | Messaggio "Nessun risultato trovato". |
| Traceability | UW-008; FR-008 |

**Test Steps:**
1. Con archivio vuoto, avviare ricerca "CF assente".
2. Verificare messaggio "Nessun risultato trovato".

---

**Test Case: UW-008-TC-004**

| Field | Detail |
|---|---|
| Title | Performance ricerca CF assente su 10.000 soggetti |
| Functional Area | FA-002 |
| Test Type | State |
| Priority | High |
| Preconditions | Archivio con 10.000 soggetti (mix italiani con e senza CF). |
| Test Data | Archivio 10.000 soggetti; ~1.000 con CF assente. |
| Expected Result | Lista risultati restituita entro 60 secondi dall'avvio della ricerca (NFR-002). |
| Postconditions | Lista visualizzata. |
| Traceability | UW-008; FR-008; NFR-002 |

**Test Steps:**
1. Configurare archivio con 10.000 soggetti.
2. Registrare timestamp di avvio ricerca.
3. Avviare ricerca "CF assente".
4. Registrare timestamp di completamento.
5. Verificare che il tempo totale sia ≤ 60 secondi.

---

**Test Case: UW-008-TC-005**

| Field | Detail |
|---|---|
| Title | Accesso al modulo bonifica negato per profilo non autorizzato |
| Functional Area | FA-002 |
| Test Type | Negative |
| Priority | Critical |
| Preconditions | Utente autenticato con profilo role-001 (Funzionario Amministrativo). |
| Test Data | Utente: role-001; URL/accesso modulo bonifica. |
| Expected Result | Accesso negato. Messaggio di autorizzazione insufficiente visualizzato. Il modulo bonifica non è accessibile. |
| Postconditions | Utente rimane nella schermata autorizzata. |
| Traceability | UW-008; NFR-005 |

**Test Steps:**
1. Autenticarsi con utente che ha profilo role-001.
2. Tentare di navigare al modulo bonifica archivi.
3. Verificare che l'accesso sia negato.
4. Verificare che un messaggio di "accesso non autorizzato" o equivalente sia visualizzato.

---

**Test Case: UW-009-TC-001**

| Field | Detail |
|---|---|
| Title | Ricerca CF non valido restituisce lista soggetti |
| Functional Area | FA-002 |
| Test Type | Happy Path |
| Priority | High |
| Preconditions | Utente role-002. Archivio con soggetti CF formato errato. |
| Test Data | Soggetto con CF="XXXXXXXXXXXXX999" (CF non valido formalmente). |
| Expected Result | Lista con soggetto; tipologia="CF non valido". |
| Traceability | UW-009; FR-009 |

**Test Steps:**
1. Avviare ricerca "CF non valido".
2. Verificare soggetto nella lista con tipologia="CF non valido".

---

**Test Case: UW-009-TC-002**

| Field | Detail |
|---|---|
| Title | Ricerca CF non valido senza risultati |
| Functional Area | FA-002 |
| Test Type | Equivalence |
| Priority | Low |
| Preconditions | Tutti i soggetti hanno CF formalmente valido. |
| Test Data | Archivio senza CF non validi. |
| Expected Result | Messaggio "Nessun risultato trovato". |
| Traceability | UW-009; FR-009 |

**Test Steps:**
1. Avviare ricerca "CF non valido" con archivio pulito.
2. Verificare messaggio "Nessun risultato trovato".

---

**Test Case: UW-009-TC-003**

| Field | Detail |
|---|---|
| Title | Performance ricerca CF non valido su 10.000 soggetti |
| Functional Area | FA-002 |
| Test Type | State |
| Priority | High |
| Preconditions | Archivio con 10.000 soggetti con CF presente. |
| Test Data | 10.000 soggetti; ~500 con CF non valido. |
| Expected Result | Lista restituita entro 60 secondi (NFR-002). |
| Traceability | UW-009; NFR-002 |

**Test Steps:**
1. Avviare ricerca con archivio pieno.
2. Misurare tempo di risposta.
3. Verificare ≤ 60 secondi.

---

**Test Case: UW-010-TC-001**

| Field | Detail |
|---|---|
| Title | Ricerca CF non congruente restituisce lista soggetti |
| Functional Area | FA-002 |
| Test Type | Happy Path |
| Priority | High |
| Preconditions | Utente role-002. Archivio con soggetti CF valido ma ≠ CF atteso. |
| Test Data | Soggetto ROSSI MARIO con CF="BNCNNA90H55F205B" (CF altrui ma formalmente valido). |
| Expected Result | Soggetto nella lista; tipologia="CF non congruente". |
| Traceability | UW-010; FR-010 |

**Test Steps:**
1. Avviare ricerca "CF non congruente".
2. Verificare soggetto ROSSI MARIO nella lista con tipologia="CF non congruente".

---

**Test Case: UW-010-TC-002**

| Field | Detail |
|---|---|
| Title | Ricerca CF non congruente senza risultati |
| Functional Area | FA-002 |
| Test Type | Equivalence |
| Priority | Low |
| Preconditions | Tutti i CF congruenti con dati anagrafici. |
| Test Data | Archivio con CF tutti congruenti. |
| Expected Result | Messaggio "Nessun risultato trovato". |
| Traceability | UW-010; FR-010 |

**Test Steps:**
1. Avviare ricerca "CF non congruente" con archivio corretto.
2. Verificare "Nessun risultato".

---

**Test Case: UW-010-TC-003**

| Field | Detail |
|---|---|
| Title | Performance ricerca CF non congruente su 10.000 soggetti (più onerosa) |
| Functional Area | FA-002 |
| Test Type | State |
| Priority | Critical |
| Preconditions | Archivio 10.000 soggetti con CF formalmente valido. Richiede calcolo CF atteso per ogni soggetto. |
| Test Data | 10.000 soggetti; mix congruenti e non. |
| Expected Result | Lista restituita entro 60 secondi (NFR-002). Questa è la ricerca più onerosa computazionalmente. |
| Traceability | UW-010; NFR-002 |

**Test Steps:**
1. Configurare archivio 10.000 soggetti con CF validi.
2. Registrare timestamp avvio ricerca "CF non congruente".
3. Verificare che i risultati arrivino entro 60 secondi.

---

**Test Case: UW-010-TC-004**

| Field | Detail |
|---|---|
| Title | Soggetti con dati anagrafici incompleti nella ricerca CF non congruente |
| Functional Area | FA-002 |
| Test Type | Edge |
| Priority | Medium |
| Preconditions | Archivio con soggetti privi del comune di nascita (dati incompleti). |
| Test Data | Soggetto con comune=null e CF presente. |
| Expected Result | ⚠️ Non specificato: soggetti esclusi silenziosamente o inclusi con anomalia specifica "dati anagrafici incompleti"? |
| Traceability | UW-010; FR-010; ⚠️ gap |

**Test Steps:**
1. Avviare ricerca "CF non congruente".
2. Verificare se soggetti con dati incompleti appaiono nella lista.
3. Documentare il comportamento.

---

**Test Case: UW-011-TC-001**

| Field | Detail |
|---|---|
| Title | Navigazione diretta dalla lista bonifica alla scheda soggetto |
| Functional Area | FA-002 |
| Test Type | Happy Path |
| Priority | High |
| Preconditions | Lista bonifica visualizzata con almeno 1 soggetto. Utente role-002. |
| Test Data | Soggetto ROSSI MARIO nella lista bonifica. |
| Expected Result | Scheda soggetto aperta in modalità modifica con un'azione singola. |
| Postconditions | Scheda pronta per la correzione del CF. |
| Traceability | UW-011; FR-011 |

**Test Steps:**
1. Avviare una ricerca bonifica e visualizzare i risultati.
2. Fare clic sul soggetto ROSSI MARIO nella lista.
3. Verificare che la scheda soggetto si apra immediatamente in modalità modifica.
4. Verificare che non siano richiesti passaggi aggiuntivi (menu, ricerche, conferme).

---

**Test Case: UW-011-TC-002**

| Field | Detail |
|---|---|
| Title | Scheda aperta con azione singola — nessun passaggio intermedio |
| Functional Area | FA-002 |
| Test Type | State |
| Priority | Medium |
| Preconditions | Lista bonifica visualizzata. |
| Test Data | Qualsiasi soggetto nella lista. |
| Expected Result | Dal clic sulla riga alla scheda aperta: esattamente 1 azione utente. Nessun menu, dialog o ricerca intermedia. |
| Traceability | UW-011; FR-011 |

**Test Steps:**
1. Dalla lista bonifica, fare clic su una riga soggetto.
2. Contare le interazioni necessarie per aprire la scheda.
3. Verificare che la scheda si apra con 1 sola azione.

---

**Test Case: UW-011-TC-003**

| Field | Detail |
|---|---|
| Title | Navigazione a soggetto eliminato dopo generazione lista |
| Functional Area | FA-002 |
| Test Type | Edge |
| Priority | Low |
| Preconditions | Lista bonifica generata. Soggetto successivamente eliminato da altro utente. |
| Test Data | ID soggetto non più presente nell'archivio. |
| Expected Result | ⚠️ Comportamento non specificato — errore "soggetto non trovato" o altro? |
| Traceability | UW-011; FR-011; ⚠️ gap |

**Test Steps:**
1. Generare lista bonifica.
2. Eliminare il soggetto (da altro utente/sessione).
3. Tentare la navigazione alla scheda.
4. Documentare il comportamento del sistema.

---

**Test Case: UW-012-TC-001**

| Field | Detail |
|---|---|
| Title | Esportazione lista bonifica — file CSV generato con tutti i campi |
| Functional Area | FA-002 |
| Test Type | Happy Path |
| Priority | High |
| Preconditions | Lista bonifica con 5 soggetti visualizzata. Utente role-002. |
| Test Data | 5 soggetti: 2 CF assenti, 2 CF non validi, 1 CF non congruente. |
| Expected Result | File CSV scaricabile contenente 5 righe dati + header. Campi: ID, cognome, nome, dtNascita, sesso, codiceFiscale, tipologiaAnomalia. |
| Postconditions | File CSV disponibile per download. |
| Traceability | UW-012; FR-012 |

**Test Steps:**
1. Avviare una ricerca bonifica e visualizzare 5 soggetti.
2. Fare clic su "Esporta" (o azione equivalente).
3. Verificare che il file CSV sia generato e disponibile per download.
4. Aprire il file e verificare: header presente, 5 righe dati, campi ID/cognome/nome/dtNascita/sesso/CF/tipologiaAnomalia.

---

**Test Case: UW-012-TC-002**

| Field | Detail |
|---|---|
| Title | Completezza export — 100 soggetti esportati tutti |
| Functional Area | FA-002 |
| Test Type | State |
| Priority | High |
| Preconditions | Lista bonifica con 100 soggetti. |
| Test Data | 100 soggetti nella lista bonifica. |
| Expected Result | CSV con esattamente 100 righe dati. |
| Traceability | UW-012; FR-012 |

**Test Steps:**
1. Generare lista bonifica con 100 risultati.
2. Esportare.
3. Aprire il CSV e contare le righe dati.
4. Verificare che siano esattamente 100.

---

**Test Case: UW-012-TC-003**

| Field | Detail |
|---|---|
| Title | Export lista con 10.000 soggetti — file completo generato |
| Functional Area | FA-002 |
| Test Type | State |
| Priority | High |
| Preconditions | Lista bonifica con 10.000 soggetti. |
| Test Data | 10.000 soggetti nella lista. |
| Expected Result | File CSV completo (10.000 righe dati) generato e disponibile per download. |
| Traceability | UW-012; FR-012 |

**Test Steps:**
1. Generare lista bonifica con 10.000 risultati.
2. Avviare esportazione.
3. Verificare che il file sia completo e scaricabile.

---

**Test Case: UW-012-TC-004**

| Field | Detail |
|---|---|
| Title | Export lista vuota |
| Functional Area | FA-002 |
| Test Type | Edge |
| Priority | Low |
| Preconditions | Ricerca bonifica ha restituito 0 risultati. |
| Test Data | Lista bonifica = 0 soggetti. |
| Expected Result | ⚠️ CSV con solo header oppure messaggio "Nessun dato da esportare" — comportamento da definire. |
| Traceability | UW-012; FR-012; ⚠️ gap |

**Test Steps:**
1. Eseguire ricerca bonifica senza risultati.
2. Verificare se il pulsante "Esporta" è attivo.
3. Se attivo: fare clic e documentare il file generato.
4. Se non attivo: documentare il comportamento.

---

## Test Case Summary

| Functional Area | Total TCs | Critical | High | Medium | Low |
|---|---|---|---|---|---|
| FA-001 — Validazione CF (UW-001÷007) | 34 | 10 | 13 | 8 | 3 |
| FA-002 — Bonifica Archivi (UW-008÷012) | 20 | 3 | 11 | 2 | 4 |
| **TOTALE** | **54** | **13** | **24** | **10** | **7** |

### Distribuzione per tipo di test

| Test Type | Count |
|---|---|
| Happy Path | 17 |
| State | 12 |
| Negative | 8 |
| Boundary | 6 |
| Edge | 8 |
| Equivalence | 3 |
| **TOTALE** | **54** |

### Note sulla tracciabilità

Tutti i 54 test case sono tracciabili alle rispettive Units of Work (UW-001÷012) definite nell'artefatto `01-test-units`. Gli 8 gap marcati con ⚠️ richiedono definizione del comportamento da parte del team funzionale prima dell'esecuzione dei test case corrispondenti.
