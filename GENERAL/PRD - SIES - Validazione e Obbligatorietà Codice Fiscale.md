---
uniqueName: prd-sies-validazione-e-obbligatoriet-codice-fiscal
displayName: "PRD   SIES   Validazione e Obbligatoriet\u00e0 Codice Fiscale"
category: "GENERAL"
tags: []
---

# Product Requirements Document (PRD)

> Progetto: SIES — Validazione Codice Fiscale
> Generato dalla pipeline ENGenius — CONCEPT Phase

---

# 1. Panoramica del Progetto

## Contesto Organizzativo
SIES è un sistema informativo in uso presso un ente della Pubblica Amministrazione italiana, impiegato nella gestione anagrafica e amministrativa dei soggetti censiti. Il sistema è utilizzato dagli operatori interni per registrare, aggiornare e consultare i dati anagrafici dei soggetti di competenza dell'ente.

## Criticità Attuali
Il sistema SIES non prevede alcun controllo formale sul codice fiscale dei soggetti registrati, né impone l'obbligatorietà di tale dato in fase di inserimento o aggiornamento. Questa lacuna genera inconsistenze negli archivi: soggetti privi di identificativo fiscale o con codici fiscali non validi compromettono l'affidabilità del patrimonio informativo dell'ente.

## Obiettivo Strategico
L'iniziativa nasce dall'esigenza di garantire la qualità e l'integrità del dato anagrafico, introducendo regole di validazione e obbligatorietà sul codice fiscale in linea con gli standard identificativi della PA italiana.

## Risultati Attesi
L'introduzione del controllo e dell'obbligatorietà del codice fiscale consentirà di disporre di archivi anagrafici affidabili, migliorare l'identificazione univoca dei soggetti e ridurre gli errori nei processi amministrativi che dipendono dalla corretta identificazione degli individui.

---

# 2. Business Requirements

| ID | Nome | Descrizione |
|----|------|-------------|
| BR-001 | Qualità del Dato Anagrafico | Ogni soggetto censito deve essere identificato tramite codice fiscale valido. L'ente deve poter contare su un archivio privo di soggetti con CF mancante o non conforme. |
| BR-002 | Integrità Archivi Preesistenti | Le inconsistenze nei dati già registrati devono essere rilevabili e sanabili. L'ente deve disporre di strumenti per identificare i soggetti con CF mancante o non valido e avviare la bonifica. |
| BR-003 | Riduzione Errori Amministrativi | I procedimenti che dipendono dall'identificazione certa dei soggetti devono beneficiare di dati affidabili, riducendo errori e rilavorazioni. |

---

# 3. Requisiti Funzionali

## 3.1 Validazione del Codice Fiscale
Traces to: BR-001, BR-003

- Il sistema verifica se il paese di nascita del soggetto è Italia; se sì, il CF è obbligatorio.
- Il sistema verifica la correttezza formale del CF (16 caratteri alfanumerici, carattere di controllo valido).
- Il sistema calcola il CF atteso dai dati anagrafici (cognome, nome, data nascita, sesso, comune nascita).
- Il sistema confronta il CF inserito con quello atteso e rileva le discrepanze.
- In caso di CF assente, non valido o non congruente, il sistema mostra un avviso descrittivo all'operatore.
- Il sistema consente il salvataggio del soggetto anche in presenza di avvisi (comportamento non bloccante).
- Se il paese di nascita non è Italia e il CF è assente, il sistema consente il salvataggio senza avvisi.

## 3.2 Bonifica Archivi Preesistenti
Traces to: BR-002

- Il sistema mette a disposizione una ricerca per identificare soggetti con CF assente e paese di nascita Italia.
- Il sistema mette a disposizione una ricerca per identificare soggetti con CF formalmente non valido.
- Il sistema mette a disposizione una ricerca per identificare soggetti con CF non congruente con i dati anagrafici.
- Il sistema consente di accedere direttamente alla scheda di un soggetto dal risultato della ricerca.
- Il sistema presenta i risultati in forma di elenco esportabile con la tipologia di anomalia per ciascun soggetto.

---

# 4. Vincoli Tecnici

## 4.1 Infrastruttura e Hosting
- Ambiente on-premise: SIES è ospitato su server Linux dell'ente. Le modifiche devono essere compatibili con questo ambiente.

## 4.2 Sviluppo e Delivery
- Linguaggio Java 8: tutta la logica di validazione CF deve essere scritta in Java 8.
- Logica interna: l'algoritmo di calcolo CF deve essere implementato internamente, senza servizi esterni.

## 4.3 Integrazione e Interoperabilità
- Nessuna integrazione esterna: la validazione CF non si integra con sistemi esterni (Agenzia Entrate, ANPR, ecc.).

## 4.4 Dati e Conformità
- Nessun vincolo normativo specifico aggiuntivo oltre agli standard ordinari già applicati dall'ente.

---

# 5. Requisiti Non Funzionali

## 5.1 Prestazioni
Traces to: BR-001, BR-003

| ID | Requisito | Target | Applicabile Quando |
|----|-----------|--------|--------------------|
| NFR-001 | Risposta validazione CF | Entro 2 secondi dal salvataggio | Inserimento/modifica soggetto, carico normale (100 utenti) |
| NFR-002 | Ricerca bonifica | Completata entro 60 secondi per 10.000 soggetti | Esecuzione ricerca bonifica |

## 5.2 Disponibilità e Affidabilità
Traces to: BR-001, BR-002, BR-003

| ID | Requisito | Target | Applicabile Quando |
|----|-----------|--------|--------------------|
| NFR-003 | Disponibilità lavorativa | Disponibile senza interruzioni non pianificate | Ore lavorative (lun-ven) |
| NFR-004 | Coerenza risultati bonifica | Risultati completi e coerenti su 10.000 soggetti | Ogni esecuzione bonifica |

## 5.3 Sicurezza
Traces to: BR-002

| ID | Requisito | Target | Applicabile Quando |
|----|-----------|--------|--------------------|
| NFR-005 | Accesso bonifica controllato | Limitato a profili autorizzati, in linea con policy esistenti | Accesso al modulo bonifica |

## 5.4 Usabilità
Traces to: BR-001, BR-003

| ID | Requisito | Target | Applicabile Quando |
|----|-----------|--------|--------------------|
| NFR-006 | Chiarezza avvisi CF | Avviso indica tipologia anomalia (assente/formato/non congruente) per correzione autonoma | Segnalazione anomalia CF |

## 5.5 Manutenibilità
Traces to: BR-001

| ID | Requisito | Target | Applicabile Quando |
|----|-----------|--------|--------------------|
| NFR-007 | Isolamento algoritmo CF | Modulo dedicato modificabile indipendentemente [TO BE REFINED] | Aggiornamento regole calcolo CF |

---

# 6. Requisiti di Customer Experience

## 6.1 Tipologia Utenti e Contesto d'Uso
- I fruitori sono funzionari amministrativi che accedono da postazioni desktop in ufficio.
- L'accesso alla bonifica è riservato ai profili autorizzati.

## 6.2 Interazione con la Scheda Soggetto
- L'avviso CF deve essere visibile in modo evidente nella scheda soggetto, vicino al campo CF.
- L'avviso specifica la tipologia di anomalia per consentire la correzione autonoma.
- L'interfaccia mostra il CF atteso calcolato dai dati anagrafici, affiancato all'avviso.
- La segnalazione compare al salvataggio; nessuna notifica proattiva al di fuori della scheda.

## 6.3 Funzionalità di Bonifica Archivi
- I risultati di bonifica mostrano la tipologia di anomalia per ciascun soggetto.
- Dall'elenco risultati si accede alla scheda soggetto con un'azione singola.
- I risultati sono esportabili in formato standard (es. foglio di calcolo).

> Lingua, brand e accessibilità: non applicabili — backoffice interno a uso esclusivo di funzionari.

---