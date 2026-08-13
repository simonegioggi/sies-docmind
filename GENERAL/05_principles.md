---
uniqueName: 05principles
displayName: "05 principles"
category: "GENERAL"
tags: []
---

# Principles — Progetto SIUS

**Data**: 2026-04-24  
**Versione**: 1.0  
**Autori**: IMPACT AI Agent  
**Audience**: Architect, Tech Lead, Team di sviluppo

> **Nota metodologica**: I principi descritti nella sezione "As-Is" sono **dedotti dall'analisi del codice** (pattern impliciti ricorrenti). Non è stata trovata documentazione esplicita di principi architetturali nel repository. La sezione "Target" contiene principi raccomandati per la modernizzazione.

---

## 1. Principi Architetturali AS-IS (impliciti)

Questi principi emergono dall'analisi di 1.294 classi Java e 670 JSP, riflettendo le pratiche effettive adottate dal team nel corso degli anni.

### 1.1 Command Pattern per Action Handler

**Pattern implicito osservato:**
- Ogni funzionalità è gestita da una o più classi `Act*.java` che estendono `ActionSius`
- Le Action implementano il pattern Command: ogni classe sa "cosa fare" per una specifica operazione HTTP
- Routing tramite nome classe completamente qualificato in query parameter

```
Request HTTP → SIUSLookupRemote (reflection) → Act*.execute() → DAO → Oracle → JSP response
```

**Pro**: Separazione delle responsabilità per feature, aggiunta di nuove funzionalità senza modificare codice esistente  
**Contro**: Nessun DI, accoppiamento forte tramite Service Locator, impossibilità di testare le Action in isolamento

### 1.2 Package-by-Feature

**Pattern**: ogni modulo funzionale ha il suo package con la struttura `action/`, `controller/`, `dao/`, `model/`:

```
be/fascicolo/
  action/      → Act* classes (request handlers)
  controller/  → FascicoloController
  dao/         → FascicoloSqlDAO
  model/       → FascicoloSiusModel, FascicoloGPModel
```

**Valore**: organizzazione del codice attorno al dominio, facilità di navigazione per chi conosce il dominio  
**Limite**: forte dipendenza cross-package non tracciata (no moduli Maven)

### 1.3 Separazione View/Logic (parziale)

- JSP = view pura (prevalentemente), data passato via request attributes
- Action classes = controller + parziale business logic
- DAO = accesso dati
- **Mancanza**: service layer esplicito → business logic talvolta duplicata in DAO o Action

### 1.4 SQL Trasparente (No ORM)

**Scelta implicita**: il team ha scelto SQL diretto anziché ORM (Hibernate, JPA), per massimo controllo sulle query Oracle.

**Pro**: Performance predicibile, SQL Oracle-specific ottimizzato  
**Contro**: SQL construction by string concatenation → SQL injection; zero portabilità; difficile testare

### 1.5 Italian-First Naming

**Convenzione implicita**: tutti i nomi di classi, metodi, variabili, package e schemi DB sono in italiano:
- `FascicoloSiusModel`, `MisuraAlternativaDao`, `ActRicercaFascicolo`
- Query SQL con alias italiani
- Costanti in italiano/abbreviato

**Pro**: coerente con il dominio normativo italiano; accessibile agli esperti di dominio  
**Contro**: difficile onboarding di sviluppatori non italofoni; non standard internazionale

---

## 2. Principi di Sviluppo AS-IS (impliciti)

### 2.1 "Add, Don't Refactor"

**Osservazione**: il codebase mostra aggiunta incrementale di classi Action senza refactoring del codice esistente. God classes come `StampaController` (6.470 LOC) sono state estese anziché decomposta.

### 2.2 Copy-Paste Driven Development

**Osservazione**: struttura identica nei 51 moduli (action/controller/dao/model) suggerisce heavy copy-paste della struttura base, probabilmente da un template iniziale mai aggiornato.

**Effetto**: inconsistenze di implementazione tra moduli simili; difficile evoluzione uniforme.

### 2.3 Defensive Coding via Logging

**Osservazione**: uso abbondante di `logger.info()` / `logger.error()` con `ExceptionUtils.getStackTrace()` come principale meccanismo di debugging. Approccio "log everything and see what happens in prod".

---

## 3. Principi Architetturali TARGET (per modernizzazione)

Questi principi sono raccomandati per guidare l'evoluzione del sistema verso architetture più sostenibili.

### 3.1 SOLID Principles

| Principio | Stato AS-IS | Target |
|-----------|-------------|--------|
| **S** Single Responsibility | ❌ Violato (StampaController 6470 LOC) | Ogni classe ha una sola responsabilità |
| **O** Open/Closed | ⚠️ Parziale (aggiunta Action OK, modifica Controller NO) | Estendere senza modificare |
| **L** Liskov Substitution | ⚠️ Non applicabile con F3B | Interfacce ben definite |
| **I** Interface Segregation | ❌ `ICostanti*` interfacce con 50+ costanti eterogenee | Interfacce specifiche per contesto |
| **D** Dependency Inversion | ❌ Service Locator (SIUSLookupRemote) | Dependency Injection (Spring/CDI) |

### 3.2 Don't Repeat Yourself (DRY)

- **AS-IS**: copie di logica simile nei 51 DAO (SQL identici parametrizzati diversamente)
- **Target**: query centralizzate, componenti riutilizzabili, librerie condivise per logica comune

### 3.3 Fail Fast

- **AS-IS**: errori catturati e loggati ma spesso l'utente non riceve feedback chiaro
- **Target**: validazione input immediata (client + server), errori espliciti, feedback utente chiaro

### 3.4 Dependency Injection over Service Locator

- **AS-IS**: `SIUSLookupRemote.lookup("className")` — 400 occorrenze, testing impossibile
- **Target**: Spring `@Autowired` / CDI `@Inject` — dependencies esplicite, testabili, sostituibili

### 3.5 Separation of Concerns

- **AS-IS**: DAO con logica di business, Action con SQL diretto in alcuni casi
- **Target**: Controller → Service → Repository — strati ben definiti, interfacce tra strati

### 3.6 Infrastructure as Code

- **AS-IS**: deploy manuale
- **Target**: pipelines CI/CD (Jenkins/GitLab CI), Dockerfile, procedure automatizzate

---

## 4. Principi di Coding Target

| Area | Principio | Descrizione |
|------|-----------|-------------|
| **SQL** | Prepared Statements obbligatori | Nessuna concatenazione SQL — usare `?` parametri o named params |
| **Logging** | SLF4J + Logback/Log4j2 | Formato strutturato (JSON), livelli corretti, no Log4j 1.x |
| **Encoding** | UTF-8 ovunque | Tutti i file sorgente, JSP, configurazioni in UTF-8 |
| **Test** | Test-first o almeno test coverage > 80% | JUnit 5, Mockito, TestContainers per integrazione DB |
| **Naming** | English naming (opzione) | Per allineamento con standard internazionali — ma compatibile con dominio italiano |
| **Null handling** | Optional<T> o annotazioni @Nullable | No NullPointerException silente |
| **Error handling** | Eccezioni tipizzate, no catch-all | Catch `SIUSException` specifico, no `catch(Exception e) { logger.error }` cieco |

---

## 5. Technology Selection Principles

| Dimensione | AS-IS | Target Scenario A (Re-platform) | Target Scenario B (Re-architect) |
|-----------|-------|--------------------------------|----------------------------------|
| Persistence | SQL dinamico + Oracle | MyBatis/JDBC con Prepared Stmt | JPA/Hibernate o MyBatis mapper XML |
| DI Container | Nessuno (F3B Service Locator) | Spring Framework | Spring Boot |
| Web Layer | F3B + JSP | Spring MVC + JSP (transitorio) | Spring Boot + REST API + Angular/React |
| Build | Manuale (EAR SIAP) | Maven + CI/CD pipeline | Maven/Gradle + Docker + CI/CD |
| Logging | Log4j 1.x | Log4j 2.x / SLF4J+Logback | SLF4J + structured logging |
| Test | Nessuno | JUnit 5 + Mockito | JUnit 5 + Mockito + TestContainers |
| Version Control | SVN | SVN o migrazione Git | Git + GitFlow |

### 5.1 Buy vs Build

| Componente | Decisione | Motivazione |
|-----------|-----------|-------------|
| Database | **Buy** (Oracle/PostgreSQL) | Nessun vantaggio a costruire DB engine |
| App Server | **Buy** (JBoss/Tomcat) | Standard PA — contratto esistente |
| UI Framework | **Buy** (Angular/React) | Ecosistema maturo; no build interno |
| ORM | **Buy** (MyBatis/JPA) | Maturità, community, sicurezza |
| Auth/AuthZ | **Buy** (Keycloak/LDAP) | Standard PA; conformità SPID |
| Business Logic | **Build** | Core del dominio — know-how specifico magistratura |
| Stampa documenti | **Buy** (JasperReports/iText) | Standard per PDF legali |

---

## 6. Anti-Patterns da Evitare (nella modernizzazione)

| Anti-Pattern | Rischio | Regola |
|-------------|---------|--------|
| Big Bang Rewrite | Altissimo rischio di fallimento | Migrare incrementalmente modulo per modulo |
| God Class | Manutenzione impossibile | Max 300 LOC per classe; decomporre se > 500 |
| Service Locator | Testing impossibile, coupling opaco | Usare DI; zero new SIUSLookupRemote |
| SQL String Concatenation | SQL Injection CRITICAL | Zero concatenazione SQL — solo parametri |
| Copy-Paste Module | Divergenza e inconsistenze | Template + generazione o libreria base condivisa |

---

## Reference Documents

- `docs/04_constraints.md` — Vincoli che condizionano la scelta dei principi
- `docs/18_antipattern_deep_dive.md` — Antipattern presenti nel codice AS-IS
- `docs/19_modernization_estimation_spec.md` — Scenari di modernizzazione

---

## Change Log

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | 2026-04-24 | IMPACT AI Agent | Prima versione — principi dedotti dall'analisi del codebase |