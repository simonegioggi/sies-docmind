---
uniqueName: stimaintegrazionemercurio
displayName: "stima integrazione mercurio"
category: "GENERAL"
tags: []
---

# Stima Economico-Temporale — Integrazione SIES ↔ Mercurio
## Firma digitale e archiviazione documentale (ActUploadDocument)

**Progetto:** SIES (Sistema Informativo Esecuzione e Sorveglianza)
**Modulo interessato:** `siesWeb` — `siap.sico.evento.action.ActUploadDocument`
**Data redazione:** 07/07/2026
**Versione:** 1.0

---

## 1. Contesto e obiettivo

Il flusso attuale in `ActUploadDocument.processRequest()` acquisisce il documento caricato dall'operatore
(variabile `lInput` / `mInStr`), lo memorizza come BLOB Oracle nella tabella `EVENTO` tramite il controller
EJB `IEvento.ExUpdateDocument()` e notifica eventuali avvocati registrati.

**Obiettivo del MEV:** prima di persistere il documento è necessario:

1. **Firmare digitalmente** il file tramite il servizio esposto da Mercurio (firma server-side su documento del Ministero della Giustizia).
2. **Archiviare** il documento firmato nel *Documentale Unico Mercurio* (sistema di gestione e conservazione sostitutiva del Ministero della Giustizia), ottenendo un identificativo univoco di archiviazione.
3. **Salvare** l'identificativo Mercurio nella tabella `EVENTO` per consentire la consultazione/verifica futura del documento dal sistema documentale.

---

## 2. Analisi tecnica dell'intervento

### 2.1 Stack tecnologico attuale

| Componente | Tecnologia |
|---|---|
| Runtime | JBoss EAP (Java EE) |
| Linguaggio | Java 25 (sorgenti legacy Java 8-compatibili) |
| Accesso dati | EJB 3.x + MyBatis + Oracle DB |
| Servizi esterni esistenti | SOAP/WSDL (es. `richiestaStampa`, `ServiziInvioPagamentiTelematici`, `IscriviProvvedimentoProvvisorioPort`) |
| Encoding sorgenti | ISO-8859-1 |

### 2.2 Componenti da realizzare ex-novo

Struttura package proposta:

    siesWeb/src/siap/sico/mercurio/
      ├── client/
      │    ├── MercurioFirmaClient.java
      │    └── MercurioDocumentaleClient.java
      ├── model/
      │    ├── MercurioFirmaRequest.java
      │    ├── MercurioFirmaResponse.java
      │    ├── MercurioArchiviazRequest.java
      │    └── MercurioArchiviazResponse.java
      ├── config/
      │    └── MercurioConfig.java
      └── exception/
           └── MercurioIntegrationException.java

Modifiche ai componenti esistenti:

- `ActUploadDocument.java` — aggiunta del flusso firma + archiviazione prima di `updateTabella()`
- `EventoModel.java` — nuovo campo `idDocMercurio`
- Mapping MyBatis `EventoMapper.xml` — colonna `ID_DOC_MERCURIO`
- `IEvento` / `EventoController` (EJB) — aggiornamento metodo `ExUpdateDocument` per persistere l'ID
- `sies.properties` — parametri endpoint Mercurio
- `pom.xml` — eventuale dipendenza JAX-WS o Apache CXF per generazione stub

### 2.3 Flusso di integrazione target

    ActUploadDocument.processRequest()
      │
      ├─ [esistente] lettura file → lInput → mInStr (byte[])
      │
      ├─ [NUOVO] MercurioFirmaClient.firma(byte[] documento, metadatiFirma)
      │       └─ SOAP/REST → Mercurio Firma Service
      │            └─ ritorna byte[] documentoFirmato (P7M / PAdES / CAdES)
      │
      ├─ [NUOVO] MercurioDocumentaleClient.archivia(byte[] documentoFirmato, MetadatiDocumento)
      │       └─ SOAP/REST → Mercurio Documentale Service
      │            └─ ritorna String idDocMercurio
      │
      ├─ [NUOVO] sostituzione di mInStr con documentoFirmato
      │
      └─ [esistente] updateTabella(lId, lFlgAvvocatura)
              └─ ExUpdateDocument(EventoModel) → Oracle BLOB + ID_DOC_MERCURIO

### 2.4 Dipendenze e prerequisiti bloccanti

| Prerequisito | Responsabile | Impatto in assenza |
|---|---|---|
| Documentazione API Mercurio (WSDL o Swagger/OpenAPI) | Team Mercurio / DG SIA | Blocca sviluppo client |
| Endpoint e credenziali ambiente di TEST Mercurio | Team Mercurio | Blocca test integrazione |
| Certificati per firma (HSM server-side o p12) | DG SIA / DGCERT | Blocca test firma |
| Specifiche metadati documentali (tipo doc, classificazione) | Referente funzionale | Blocca mapping metadati |
| Schema DB aggiornato (colonna `ID_DOC_MERCURIO`) | DBA | Blocca test E2E |
| Politica di rollback (cosa fare se Mercurio non risponde) | Referente funzionale | Blocca design errori |

---

## 3. Piano di lavoro e stima temporale

**Unità:** giorni lavorativi (gg) = 8 ore/gg
**Profilo:** 1 Sviluppatore Senior Java EE

### Fase 0 — Analisi e design

| Attività | Stima (gg) | Note |
|---|---|---|
| Studio documentazione API Mercurio (firma + archiviazione) | 2 | Dipende da completezza docs |
| Definizione mapping metadati SIES → Mercurio | 1 | Con referente funzionale |
| Progettazione gestione errori / transazionalità / rollback | 1 | Decisione architetturale |
| Redazione specifiche tecniche di dettaglio | 1 | |
| **Totale Fase 0** | **5** | |

### Fase 1 — Setup e scaffolding

| Attività | Stima (gg) | Note |
|---|---|---|
| Generazione stub da WSDL Mercurio (wsimport / wsdl2java) o client REST | 1 | SOAP: wsimport; REST: OpenAPI Generator |
| Creazione package `siap.sico.mercurio` e classi infrastrutturali | 1 | |
| Configurazione dipendenze `pom.xml` (CXF, HttpClient, ecc.) | 0.5 | |
| **Totale Fase 1** | **2.5** | |

### Fase 2 — Sviluppo MercurioFirmaClient

| Attività | Stima (gg) | Note |
|---|---|---|
| Implementazione chiamata al servizio di firma | 2 | |
| Gestione certificati / keystore (TLS mutua autenticazione) | 2 | Dipende da infrastruttura PKI |
| Gestione risposta e formato documento firmato (P7M/PAdES) | 1 | |
| Unit test con mock del servizio | 1 | |
| **Totale Fase 2** | **6** | |

### Fase 3 — Sviluppo MercurioDocumentaleClient

| Attività | Stima (gg) | Note |
|---|---|---|
| Implementazione chiamata al servizio di archiviazione | 2 | |
| Mapping metadati (fascicolo, tipo atto, utente, ufficio, data) | 1.5 | |
| Gestione risposta e parsing idDocMercurio | 0.5 | |
| Unit test con mock del servizio | 1 | |
| **Totale Fase 3** | **5** | |

### Fase 4 — Integrazione in ActUploadDocument e modifiche DB

| Attività | Stima (gg) | Note |
|---|---|---|
| Modifica flusso processRequest() e updateTabella() | 1.5 | |
| Aggiunta campo idDocMercurio a EventoModel | 0.5 | |
| Aggiornamento mapping MyBatis EventoMapper.xml | 0.5 | |
| Script DDL Oracle: ALTER TABLE EVENTO ADD ID_DOC_MERCURIO VARCHAR2(100) | 0.5 | Con DBA |
| Aggiornamento EJB IEvento / EventoController | 1 | |
| Gestione errori: eccezione Mercurio → comportamento di fallback | 1 | |
| **Totale Fase 4** | **5** | |

### Fase 5 — Test di integrazione e sistema

| Attività | Stima (gg) | Note |
|---|---|---|
| Test integrazione con endpoint Mercurio di TEST | 3 | Necessario accesso all'ambiente |
| Test non regressione (upload senza firma, flusso Avvocatura, ecc.) | 2 | |
| Fix bug emersi durante i test | 2 | Stima conservativa |
| **Totale Fase 5** | **7** | |

### Fase 6 — Deployment e configurazione ambienti

| Attività | Stima (gg) | Note |
|---|---|---|
| Configurazione sies.properties per ambienti TEST / COLL / PROD | 0.5 | |
| Deploy in TEST e verifica | 0.5 | |
| Deploy in COLLAUDO e supporto UAT | 1 | |
| Passaggio in PRODUZIONE + post-go-live monitoring | 1 | |
| **Totale Fase 6** | **3** | |

---

## 4. Riepilogo stima

| Fase | Descrizione | Stima (gg) |
|---|---|---|
| Fase 0 | Analisi e design | 5 |
| Fase 1 | Setup e scaffolding | 2.5 |
| Fase 2 | Client firma digitale | 6 |
| Fase 3 | Client archiviazione Mercurio | 5 |
| Fase 4 | Integrazione e modifiche DB | 5 |
| Fase 5 | Test di integrazione e sistema | 7 |
| Fase 6 | Deployment | 3 |
| **TOTALE** | | **33.5** |

**Contingency (+20%):** +6.7 gg → **Totale con contingency: ~40 gg lavorativi (~8 settimane)**

---

## 5. Stima economica indicativa

| Voce | Tariffa | Giorni | Importo |
|---|---|---|---|
| Sviluppatore Senior Java EE | €450/gg | 34 | €15.300 |
| Analista Funzionale (Fase 0 + UAT) | €400/gg | 3 | €1.200 |
| DBA Oracle (Fase 4 + Fase 6) | €380/gg | 2 | €760 |
| Contingency (20%) | — | — | €3.452 |
| **TOTALE STIMATO** | | | **€20.712** |

*Nota: importi indicativi, adattare ai contratti quadro CONSIP / accordo quadro MdG vigenti.*

---

## 6. Rischi principali

| # | Rischio | Probabilità | Impatto | Mitigazione |
|---|---|---|---|---|
| R1 | API Mercurio non disponibili / incomplete | Media | Alto | Richiedere WSDL/Swagger prima dell'avvio |
| R2 | Ambiente TEST Mercurio non disponibile | Alta | Alto | Sviluppo con WireMock/mock SOAP |
| R3 | PKI / certificati di firma non pronti | Media | Alto | Avviare richiesta certificati in parallelo |
| R4 | Latenza servizi Mercurio impatta UX | Media | Medio | Valutare archiviazione asincrona (JMS) |
| R5 | Rollback non atomico (SIES DB vs Mercurio) | Bassa | Alto | Strategia compensativa (cancellazione doc Mercurio in caso di errore DB) |
| R6 | Documenti pre-migrazione (BLOB senza ID Mercurio) | Bassa | Medio | Colonna nullable; batch migrazione separata |

---

## 7. Presupposti

- Il servizio di firma Mercurio è di tipo **server-side** (non richiede smart card dell'operatore).
- I bytes del documento firmato sostituiscono quelli originali anche nel BLOB Oracle.
- L'ID documento Mercurio viene persistito su `EVENTO.ID_DOC_MERCURIO` come VARCHAR2.
- La connettività di rete tra JBoss EAP e gli endpoint Mercurio è già garantita (firewall configurati).
- Il formato firma sarà confermato dal referente Mercurio (si assume CAdES-BES / P7M).
- La stima **non include** la migrazione retroattiva dei documenti già presenti nel BLOB Oracle.

---

## 8. Prossimi passi

1. **[Immediato]** Richiedere al team Mercurio: WSDL servizio firma, WSDL/Swagger servizio archiviazione, credenziali ambiente TEST.
2. **[Immediato]** Richiedere al DBA script DDL per colonna `ID_DOC_MERCURIO` sulla tabella `EVENTO`.
3. **[Immediato]** Chiarire con referente funzionale la politica di rollback in caso di failure Mercurio.
4. **[Settimana 1]** Avvio analisi API e progettazione dettagliata.
5. **[Settimane 2–6]** Sviluppo.
6. **[Settimana 7]** Test integrazione.
7. **[Settimana 8]** UAT e go-live.

---

*Documento redatto con analisi del codice sorgente SIES: `ActUploadDocument.java`, `EventoModel.java`, `pom.xml`, struttura pacchetti.*