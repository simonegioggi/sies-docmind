---
uniqueName: 03nonfunctionaloverview
displayName: "03 non functional overview"
category: "GENERAL"
tags: []
---

# Non-Functional Overview — Progetto SIUS

**Data**: 2026-04-24  
**Versione**: 1.0  
**Autori**: IMPACT AI Agent  
**Audience**: Architect, Tech Lead, Team di sviluppo  
**Fonte**: Analisi codebase — valori dedotti dal codice, non da SLA documentati

> ⚠️ **Nota metodologica**: Molti requisiti non funzionali non sono documentati nel codebase.  
> Quando non deducibile con certezza, si usa il marker **[NON VALUTABILE]** con note esplicative.  
> Quando deducibile con elementi a rischio, si usa **[RISK]** con severity.

---

## 1. MANIFEST — Requisiti Non Funzionali Primari

### 1.1 Performance

| Attributo | Valore | Fonte | Stato |
|-----------|--------|-------|-------|
| Response time atteso | [NON VALUTABILE] — nessun SLA documentato nel codice | — | ⚠️ |
| Throughput atteso | [NON VALUTABILE] — nessun load test rilevato | — | ⚠️ |
| Max utenti concorrenti | [NON VALUTABILE] — nessun session limit configurato | — | ⚠️ |
| Pool connessioni DB | [NON VALUTABILE] — configurazione in jboss/datasource, non nel codebase | jboss | ⚠️ |

**Osservazioni a rischio performance:**
- `fascicoloSiusGP` referenziato 509 volte: **stato stateful nella sessione HTTP** → rischio memory bloat con molti utenti concorrenti
- SQL dinamico con concatenazione di stringhe (3.190 occorrenze) → impossibilità di query plan caching → degradazione progressiva
- Nessuna paginazione lato server in alcuni moduli statistici (670 JSP senza scroll server-side visibile)
- `StampaController` (6.470 LOC) genera PDF in-process senza job queue → picchi di CPU durante stampe massive
- **[RISK HIGH]** Nessuna cache applicativa (no EhCache, no Redis) → ogni richiesta ri-esegue query DB

---

### 1.2 Scalability

| Attributo | Valore | Stato |
|-----------|--------|-------|
| Scalabilità orizzontale | [NON VALUTABILE] — sessione stateful HTTP impedisce scale-out senza sticky session | ⚠️ |
| Scalabilità verticale | Possibile (JBoss multi-thread) | ✅ |
| Architettura | Monolitica EAR — single deployable unit | — |

**[RISK HIGH]**: La dipendenza da `fascicoloSiusGP` in sessione HTTP lega ogni utente a un nodo specifico di JBoss. Il load balancing richiederebbe **sticky session** obbligatoria.

---

### 1.3 Usability

| Attributo | Valore | Stato |
|-----------|--------|-------|
| Standard di accessibilità dichiarato | [NON VALUTABILE] — nessun attributo ARIA, nessun tag `alt` sistematico trovato nel codebase JSP | ⚠️ |
| Obblighi WCAG 2.1 (AGID) | **APPLICABILE** — PA italiana, D.Lgs. 106/2018 | ❌ Probabilmente non conforme |
| Interfaccia utente | HTML table-based legacy (no responsive, no mobile) | ⚠️ |
| Feedback form validation | Lato server (no client-side validation JavaScript rilevata sistematicamente) | ⚠️ |
| Internazionalizzazione | Solo italiano | ✅ (accettabile per contesto) |
| Accessibilità da screen reader | [NON VALUTABILE] — struttura tabellare vecchio stile | ⚠️ |

---

### 1.4 Reliability

| Attributo | Valore | Fonte | Stato |
|-----------|--------|-------|-------|
| MTTR (Mean Time to Recovery) | [NON VALUTABILE] | — | ⚠️ |
| MTBF (Mean Time Between Failures) | [NON VALUTABILE] | — | ⚠️ |
| Gestione errori applicativa | `SIUSException` propagata; catch in servlet layer | codice | ⚠️ Parziale |
| Transazionalità DB | [NON VALUTABILE] — nessun `@Transactional` (no Spring); gestione manuale connection | codice | ⚠️ |
| Integrità referenziale | Delegata al DB Oracle | DB | ✅ |

**Rischi reliability identificati:**
- Nessun circuit breaker verso sistemi esterni (JMS, SICO, SIEP)
- Chiamate a `SIUSLookupRemote` (~400 usaggi) senza timeout/retry configurabile dall'applicazione
- Logging via Log4j 1.x (CVE-2019-17571) — **[RISK CRITICAL]**

---

### 1.5 Availability

| Attributo | Valore | Stato |
|-----------|--------|-------|
| SLA dichiarata | [NON VALUTABILE] | ⚠️ |
| Deployment strategy | Manuale (stop/start JBoss) | ❌ |
| Zero-downtime deploy | No (deploy richede restart EAR) | ❌ |
| Health check endpoint | Non rilevato | ❌ |
| Failover automatico | [NON VALUTABILE] — dipende da infrastruttura JBoss cluster | ⚠️ |

---

## 2. OPERATIONAL — Requisiti Operativi

### 2.1 Security

> ⚠️ **AREA CRITICA** — Rischi di sicurezza gravi rilevati nell'analisi del codice

| Categoria | Dettaglio | Severity |
|-----------|-----------|----------|
| **SQL Injection** | 3.190 occorrenze di concatenazione SQL con variabili utente (`" + var + "`) — nessuna prepared statement o parametrizzazione rilevata sistematicamente | **CRITICAL** |
| **Log4j CVE-2019-17571** | Log4j 1.x EOL dal 2015, vulnerabilità remote code execution nota | **CRITICAL** |
| **Autenticazione** | Gestita da SIAP/F3B (fuori scope SIUS diretto); nessun meccanismo custom rilevato | ✅ (delegata) |
| **Autorizzazione** | Controllo ruoli via F3B — `IWebConstants`; logica parzialmente nel framework | ⚠️ |
| **Cifratura dati in transito** | [NON VALUTABILE] — dipende da configurazione infrastruttura (SSL offload sul load balancer) | ⚠️ |
| **Cifratura dati a riposo** | [NON VALUTABILE] — nessuna cifratura applicativa rilevata; dipende da Oracle TDE | ⚠️ |
| **GDPR compliance** | Dati giudiziari = dati sensibili (art. 9 GDPR). Nessun audit log applicativo rilevato | **[RISK HIGH]** |
| **Encoding sorgente** | 565/1.294 classi Java in ISO-8859-1 (non UTF-8) → rischio XSS via dati non escapati | **[RISK MEDIUM]** |
| **Session management** | Sessione HTTP stateful con oggetti grandi (`fascicoloSiusGP`); nessun timeout esplicito rilevato | **[RISK MEDIUM]** |

---

### 2.2 Maintainability

| Metrica | Valore | Stato |
|---------|--------|-------|
| **Health Score** | **18/100** (stima da analisi) | ❌ Critico |
| Test coverage | **0%** — nessun test unitario o di integrazione rilevato | ❌ |
| Complessità ciclomatica (max) | `StampaController`: 6.470 LOC / ~400+ CC | ❌ |
| Coupling | Service Locator pattern (~400 usaggi `SIUSLookupRemote`) — alto coupling implicito | ❌ |
| Code duplication | Stimata alta (51 moduli con struttura simile, copia/incolla evidenti) | ❌ |
| Documentazione inline | Minima — pochi commenti significativi | ❌ |
| Naming convention | Italiana (classi, metodi, variabili) — coerente internamente, difficile per team internazionale | ⚠️ |

---

### 2.3 Observability / Monitoring

| Attributo | Valore | Stato |
|-----------|--------|-------|
| Logging framework | Log4j 1.x (file-based) | ⚠️ (obsoleto) |
| Log format | Testo libero — nessun formato strutturato (no JSON) | ❌ |
| APM (Application Performance Monitoring) | [NON VALUTABILE] — nessun agent rilevato nel codice | ⚠️ |
| Metriche applicative | Nessuna esposizione metrice (no JMX custom, no Micrometer) | ❌ |
| Alerting | [NON VALUTABILE] — dipende da infrastruttura esterna | ⚠️ |
| Distributed tracing | Assente | ❌ |
| Audit log | Nessun audit log applicativo esplicito rilevato (traccia eventi importanti) | **[RISK HIGH]** |

---

## 3. DEVELOPMENT — Requisiti di Sviluppo

### 3.1 Testability

| Attributo | Valore | Stato |
|-----------|--------|-------|
| Unit test framework | Non presente nel codebase SIUS | ❌ |
| Test di integrazione | Non presente | ❌ |
| Mock/Stub | Nessun meccanismo di mocking rilevato | ❌ |
| CI/CD pipeline | [NON VALUTABILE] — no Jenkinsfile, no .gitlab-ci.yml nel repo | ⚠️ |
| Code coverage target | [NON VALUTABILE] — 0% attuale | ❌ |

---

### 3.2 Deployability

| Attributo | Valore | Stato |
|-----------|--------|-------|
| Build system | Maven (nella piattaforma SIAP EAR) — non presente in SIUS isolato | ⚠️ |
| Artifact | Parte di JBoss EAR (no WAR/JAR standalone) | ⚠️ |
| Deploy procedure | Manuale (copia file + restart JBoss) | ❌ |
| Rollback procedure | [NON VALUTABILE] — presumibilmente manuale (backup EAR precedente) | ⚠️ |
| Ambienti | SVILUPPO → COLLAUDO → ESERCIZIO (presumibili, non documentati nel codebase) | ⚠️ |

---

### 3.3 Portability

| Attributo | Valore | Stato |
|-----------|--------|-------|
| Java version | 1.8 (compiled — dalla piattaforma SIAP) | ✅ |
| Application Server | JBoss (hardcoded deployment descriptors) | ⚠️ |
| Database | Oracle — SQL specifico Oracle (ROWNUM, NVL, TO_DATE) | ⚠️ Lock-in |
| OS | [NON VALUTABILE] | — |
| Container | Non containerizzato (no Dockerfile) | ❌ |

---

## 4. EVOLUTIONARY — Requisiti di Evoluzione

### 4.1 Modificabilità / Estensibilità

| Attributo | Valore | Stato |
|-----------|--------|-------|
| Aggiungere nuovo modulo funzionale | Necessario creare package + Action class + JSP + DAO | ⚠️ Alto costo |
| Aggiungere nuova query | SQL string nel DAO → modifica fragile | ❌ |
| Cambiare framework UI | Fortissimo lock-in su JSP/F3B | ❌ |
| Cambiare DB | Lock-in Oracle (NVL, ROWNUM, date functions Oracle-specific) | ❌ |
| Integrare API REST | Richiede refactoring significativo (nessun REST layer) | ❌ |

---

## 5. Risk Summary — NFR

| Risk | Severity | Categoria | Note |
|------|----------|-----------|------|
| SQL Injection (3.190 punti) | **CRITICAL** | Security | Priorità massima — exploit potenziale |
| Log4j 1.x CVE-2019-17571 | **CRITICAL** | Security | Upgrade urgente a Log4j 2.x / SLF4J |
| Zero test coverage | **HIGH** | Maintainability | Ogni modifica è regressione potenziale |
| God classes (StampaController 6470 LOC) | **HIGH** | Maintainability | Refactoring obbligatorio |
| Sessione stateful HTTP | **HIGH** | Scalability | Impossibilità scale-out senza sticky session |
| Assenza audit log | **HIGH** | Compliance (GDPR) | Dati giudiziari senza traccia eventi |
| Encoding misto ISO-8859-1 | **MEDIUM** | Security | Rischio XSS + correttezza dati |
| WCAG 2.1 non compliance | **MEDIUM** | Usability/Legal | Obbligo normativo AGID/PA |
| 0% CI/CD | **MEDIUM** | Deployability | Deploy manuale = errore umano frequente |

---

## Reference Documents

- `docs/00_deep_dive.md` — Analisi tecnica dettagliata
- `docs/18_antipattern_deep_dive.md` — Antipattern identificati
- `docs/14_metrics.md` — Metriche di qualità

---

## Change Log

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | 2026-04-24 | IMPACT AI Agent | Prima versione — requisiti NF ricostruiti da analisi codebase |