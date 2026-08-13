---
uniqueName: 03-test-scenarios
displayName: "Test - Scenarios & Test Data"
category: "TEST_DRAFT"
tags: []
---

# Test — Scenari e Dati di Test

## Progetto: SIES

---

## FA-001 — Validazione Codice Fiscale

### UW-001 — Obbligatorietà CF condizionata al paese

| TC ID | Scenario | Test Type | Input Data | Expected Result |
| --- | --- | --- | --- | --- |
| UW-001-TC-001 | CF reso obbligatorio per soggetto italiano | Happy Path | paisNascita="ITALIA", CF=vuoto al salvataggio | Avviso "CF assente" con CF atteso al salvataggio; salvataggio consentito |
| UW-001-TC-002 | CF non obbligatorio per soggetto straniero con CF assente | Happy Path | paisNascita="FRANCIA", CF=vuoto | Salvataggio completato senza avvisi CF |
| UW-001-TC-003 | Cambio paese ITALIA→FRANCIA in modifica con CF vuoto | State | Modifica paisNascita da ITALIA a FRANCIA; CF=vuoto | Flag obbligatorietà rimosso; salvataggio senza avvisi CF |
| UW-001-TC-004 | Cambio paese FRANCIA→ITALIA in modifica con CF vuoto | State | Modifica paisNascita da FRANCIA a ITALIA; CF=vuoto | Flag obbligatorietà ripristinato; avviso "CF assente" al salvataggio |
| UW-001-TC-005 | Paese non compilato (null) | Edge | paisNascita=null | ⚠️ Comportamento non specificato — da definire |

### UW-002 — Verifica formale del codice fiscale

| TC ID | Scenario | Test Type | Input Data | Expected Result |
| --- | --- | --- | --- | --- |
| UW-002-TC-001 | CF valido 16 caratteri corretto | Happy Path | CF="RSSMRA85A01H501W" | Verifica superata; nessun avviso formato |
| UW-002-TC-002 | CF di 15 caratteri (sotto limite) | Boundary | CF="RSSMRA85A01H501" | Avviso "formato non valido" con CF atteso |
| UW-002-TC-003 | CF di 17 caratteri (sopra limite) | Boundary | CF="RSSMRA85A01H501WX" | Avviso "formato non valido" |
| UW-002-TC-004 | CF con carattere di controllo errato | Negative | CF="RSSMRA85A01H501A" | Avviso "formato non valido" con CF atteso |
| UW-002-TC-005 | CF con struttura posizionale non conforme | Negative | CF="1234567890123456" | Avviso "formato non valido" |
| UW-002-TC-006 | CF con spazi interni | Edge | CF="RSSMRA85A01H50 W" | Avviso "formato non valido" |
| UW-002-TC-007 | CF con caratteri speciali | Edge | CF="RSSMRA85A01H501!" | Avviso "formato non valido" |
| UW-002-TC-008 | CF in minuscolo (case sensitivity) | Equivalence | CF="rssmra85a01h501w" | ⚠️ Da definire — verifica case-sensitive o no? |

### UW-003 — Calcolo CF atteso

| TC ID | Scenario | Test Type | Input Data | Expected Result |
| --- | --- | --- | --- | --- |
| UW-003-TC-001 | Calcolo CF atteso maschio con dati completi | Happy Path | cognome=ROSSI, nome=MARIO, dtNascita=01/01/1985, sesso=M, comune=H501 | CF atteso="RSSMRA85A01H501W" |
| UW-003-TC-002 | Calcolo CF atteso femmina (giorno +40) | Happy Path | cognome=BIANCHI, nome=ANNA, dtNascita=15/06/1990, sesso=F, comune=F205 | CF atteso con gg=55 per il sesso femminile |
| UW-003-TC-003 | Nome con 2 lettere (completamento con X) | Boundary | nome="IO" (2 caratteri) | CF calcolato con X di completamento nelle posizioni nome |
| UW-003-TC-004 | Soggetto nato in stato estero | Equivalence | comune=Z401 (codice Francia) | CF atteso calcolato con codice stato estero Z401 |
| UW-003-TC-005 | Dati anagrafici incompleti — comune mancante | Negative | comuneNascita=vuoto/null | ⚠️ Comportamento non specificato |
| UW-003-TC-006 | Cognome con apostrofo (D'AMICO) | Edge | cognome="D'AMICO" | CF calcolato per la parte alfanumerica (apostrofo ignorato) |

### UW-004 — Confronto CF inserito vs CF atteso

| TC ID | Scenario | Test Type | Input Data | Expected Result |
| --- | --- | --- | --- | --- |
| UW-004-TC-001 | CF inserito identico al CF atteso | Happy Path | CF inserito="RSSMRA85A01H501W", CF atteso="RSSMRA85A01H501W" | Esito congruente; nessun avviso |
| UW-004-TC-002 | CF inserito diverso dal CF atteso (un carattere) | Negative | CF inserito="RSSMRA85A01H501X", CF atteso="RSSMRA85A01H501W" | Avviso "non congruente" con CF atteso mostrato |
| UW-004-TC-003 | CF inserito in minuscolo = CF atteso in maiuscolo | Boundary | CF inserito="rssmra85a01h501w", CF atteso="RSSMRA85A01H501W" | Esito congruente (case-insensitive) |
| UW-004-TC-004 | CF inserito completamente diverso | Negative | CF inserito="BNCNNA90H55F205B", CF atteso="RSSMRA85A01H501W" | Avviso "non congruente" con CF atteso |
| UW-004-TC-005 | CF omocodice | Edge | CF inserito=versione omocodice | Avviso "non congruente" (confronto letterale) |

### UW-005 — Visualizzazione avviso non bloccante

| TC ID | Scenario | Test Type | Input Data | Expected Result |
| --- | --- | --- | --- | --- |
| UW-005-TC-001 | Avviso per CF assente con dati completi | Happy Path | País=ITALIA, CF=vuoto, dati completi | Avviso "CF assente" con CF atteso calcolato affiancato |
| UW-005-TC-002 | Avviso per CF formato non valido | Happy Path | CF="XXXXXXXXXXXXXXXX" | Avviso "formato non valido" con CF atteso |
| UW-005-TC-003 | Avviso per CF non congruente | Happy Path | CF valido ma ≠ CF atteso | Avviso "non congruente" con CF atteso |
| UW-005-TC-004 | Salvataggio rimane possibile con avviso presente | State | Avviso CF presente; operatore clicca "Salva" | Salvataggio completato; soggetto persistito |
| UW-005-TC-005 | CF atteso mostrato affiancato all'avviso | State | Anomalia CF con dati anagrafici completi | CF atteso visibile vicino al campo CF |

### UW-006 — Salvataggio soggetto con avvisi CF

| TC ID | Scenario | Test Type | Input Data | Expected Result |
| --- | --- | --- | --- | --- |
| UW-006-TC-001 | Salvataggio con CF assente dopo avviso | Happy Path | País=ITALIA, CF=vuoto; salvataggio confermato | Soggetto salvato con CF vuoto in archivio |
| UW-006-TC-002 | Salvataggio con CF non valido dopo avviso | Happy Path | CF="12345678901234XX"; salvataggio confermato | Soggetto salvato con CF anomalo; visibile in bonifica UW-009 |
| UW-006-TC-003 | Salvataggio con CF non congruente dopo avviso | Happy Path | CF valido ma ≠ CF atteso; salvataggio confermato | Soggetto salvato; presente in lista bonifica UW-010 |

### UW-007 — Esenzione verifiche CF stranieri senza CF

| TC ID | Scenario | Test Type | Input Data | Expected Result |
| --- | --- | --- | --- | --- |
| UW-007-TC-001 | Soggetto straniero senza CF | Happy Path | paisNascita="GERMANIA", CF=vuoto | Salvataggio completato senza avvisi CF |
| UW-007-TC-002 | Cambio paese straniero→italiano con CF vuoto | State | paisNascita GERMANIA→ITALIA; CF=vuoto | Avviso "CF assente" al salvataggio |
| UW-007-TC-003 | Soggetto straniero con CF presente | Edge | paisNascita="SPAGNA", CF="RSSMRA85A01H501W" | ⚠️ Comportamento non definito in FR-007 |

---

## FA-002 — Bonifica Archivi Preesistenti

### UW-008 — Ricerca CF assente nati in Italia

| TC ID | Scenario | Test Type | Input Data | Expected Result |
| --- | --- | --- | --- | --- |
| UW-008-TC-001 | Ricerca con risultati | Happy Path | Archivio con ≥1 soggetto ITALIA + CF vuoto | Lista con ID, anagrafiche, tipologia="CF assente" |
| UW-008-TC-002 | Ricerca senza risultati | Equivalence | Tutti soggetti italiani con CF compilato | Messaggio "Nessun risultato trovato" |
| UW-008-TC-003 | Ricerca su archivio vuoto | Edge | Archivio=0 soggetti | Messaggio "Nessun risultato trovato" |
| UW-008-TC-004 | Performance — 10.000 soggetti | State | Archivio con 10.000 soggetti | Risultati restituiti entro 60 secondi (NFR-002) |
| UW-008-TC-005 | Accesso con profilo non autorizzato | Negative | Utente role-001 tenta accesso bonifica | Accesso negato (NFR-005) |

### UW-009 — Ricerca CF formalmente non valido

| TC ID | Scenario | Test Type | Input Data | Expected Result |
| --- | --- | --- | --- | --- |
| UW-009-TC-001 | Ricerca con risultati | Happy Path | Archivio con soggetti CF formato errato | Lista con tipologia="CF non valido" |
| UW-009-TC-002 | Ricerca senza risultati | Equivalence | Tutti CF formalmente validi | "Nessun risultato" |
| UW-009-TC-003 | Performance — 10.000 soggetti | State | Archivio 10.000 soggetti con CF | Risultati entro 60 secondi |

### UW-010 — Ricerca CF non congruente

| TC ID | Scenario | Test Type | Input Data | Expected Result |
| --- | --- | --- | --- | --- |
| UW-010-TC-001 | Ricerca con risultati | Happy Path | Archivio con CF valido ma ≠ CF atteso | Lista con tipologia="CF non congruente" |
| UW-010-TC-002 | Ricerca senza risultati | Equivalence | Tutti CF congruenti | "Nessun risultato" |
| UW-010-TC-003 | Performance — 10.000 soggetti | State | 10.000 soggetti; calcolo CF atteso per ognuno | Risultati entro 60 secondi |
| UW-010-TC-004 | Soggetti con dati incompleti | Edge | Soggetti senza comune di nascita | ⚠️ Esclusi o inclusi con anomalia specifica? |

### UW-011 — Navigazione lista bonifica → scheda soggetto

| TC ID | Scenario | Test Type | Input Data | Expected Result |
| --- | --- | --- | --- | --- |
| UW-011-TC-001 | Navigazione diretta dalla lista alla scheda | Happy Path | Clic su soggetto nella lista bonifica | Scheda soggetto aperta in modalità modifica |
| UW-011-TC-002 | Verifica assenza passaggi intermedi | State | Clic su soggetto | Scheda aperta con un'azione singola, nessun step aggiuntivo |
| UW-011-TC-003 | Soggetto eliminato dopo la generazione lista | Edge | ID soggetto non più presente | ⚠️ Comportamento non definito |

### UW-012 — Esportazione lista bonifica

| TC ID | Scenario | Test Type | Input Data | Expected Result |
| --- | --- | --- | --- | --- |
| UW-012-TC-001 | Esportazione lista con 5 soggetti | Happy Path | Lista bonifica 5 soggetti | CSV con ID, cognome, nome, dtNascita, sesso, CF, tipologiaAnomalia |
| UW-012-TC-002 | Completezza — tutti i soggetti inclusi | State | Lista 100 soggetti | CSV con esattamente 100 righe dati + header |
| UW-012-TC-003 | Export lista con 10.000 soggetti | State | Lista piena (10.000) | File CSV completo disponibile per download |
| UW-012-TC-004 | Export lista vuota | Edge | Lista 0 risultati | ⚠️ CSV con solo header o messaggio "nessun dato"? |
