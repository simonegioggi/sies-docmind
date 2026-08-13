---
uniqueName: 17backenddeepassessment
displayName: "17 backend deep assessment"
category: "GENERAL"
tags: []
---

# Backend Deep Assessment — Progetto SIUS

**Data**: 2026-04-24  
**Versione**: 1.0  
**Autori**: IMPACT AI Agent  
**Audience**: Backend Architect, Tech Lead, Senior Developer

> **Nota**: SIUS non usa Spring Boot ma il framework proprietario F3B (Bull/Atos). Questo assessment è adattato alla tecnologia effettiva del sistema: Java EE + F3B + MyBatis-less JDBC + JBoss EAR deployment.

---

## Executive Summary

### Overall Health Score: 16 / 100 🔴

| Categoria | Score | Dettaglio |
|-----------|-------|-----------|
| Architettura | 30/100 | Layer chiari ma rigidi e non estendibili |
| Sicurezza | 5/100 | SQL injection sistemica, Log4j EOL |
| Testabilità | 0/100 | Zero test, zero interfacce mockabili |
| Manutenibilità | 20/100 | God classes, raw types, encoding misto |
| Performance | 45/100 | Session stateful, nessun caching, ma Oracle tuned |
| Resilienza | 25/100 | Error handling inconsistente, JMS per async |

**Top 3 Issues**:
1. 🔴 **SQL Injection**: 3.190 punti di concatenazione stringa — vulnerabilità CRITICA
2. 🔴 **Zero Test Coverage**: nessuna safety net per qualsiasi modifica al sistema  
3. 🔴 **Log4j 1.x CVE**: versione EOL con CVE-2019-17571 (RCE via SocketServer)

**Top 3 Recommendations**:
1. ✅ Migrare Log4j → SLF4J/Logback (effort: 3 giorni)
2. ✅ Scrivere Approval Tests per controller critici (effort: 4 settimane)
3. ✅ Sostituire SQL concatenato con PreparedStatement sui DAO con parametri String (effort: 8 settimane)

---

## 1. Architettura Modulare

### 1.1 Struttura Moduli

SIUS non è un progetto Maven autonomo: è un **modulo sorgente** assemblato nel più grande EAR `siap-ear` dal team DevOps. Non esiste un `pom.xml` nel repository SIUS — le dipendenze sono gestite esternamente.

**Struttura fisica del repository:**
```
SIUS/
├── be/                         # Backend Java source (~230K SLOC)
│   ├── ActionSius.java         # Base class globale per tutte le Action
│   ├── SIUSException.java      # Exception hierarchy root
│   ├── util/                   # SIUSLookupRemote, utility globali
│   └── {51 domain modules}/    # avvocato, fascicolo, stampa, ...
│       ├── action/             # HTTP handlers (935 classi)
│       ├── controller/         # Business logic (84 classi)
│       ├── dao/                # Data access (110 classi)
│       └── model/              # Domain objects (93 classi)
└── fe/                         # Frontend JSP source (~164K SLOC)
    └── sius/
        └── {51 domain modules}/
            └── *.jsp
```

**Package root**: `siap.sius.*` (non `it.mig.sies.*` come in siesEsecuzione — sono sistemi diversi)

### 1.2 Organizzazione Packages

SIUS usa **package by feature** (non by layer): ogni dominio ha i propri action/controller/dao/model. Questo è architetturalmente corretto ma ha un problema: le dipendenze cross-dominio passano sempre attraverso il Service Locator, non sono esplicite.

```
siap.sius.fascicolo.action     → usa SIUSLookupRemote → siap.sius.fascicolo.controller
siap.sius.stampa.controller    → usa SICOLookupRemote → siap.sico.evento.controller
siap.sius.presaincarico.action → usa SIUSLookupRemote → siap.sico.fascicolo.controller
```

**Violazione architetturale critica**: `StampaController` importa 50+ classi da `siap.sico.*` — cross-module coupling non mediato da Service Locator.

---

## 2. Domain Model & Business Logic

### 2.1 Analisi Domain-Driven Design

| Concetto DDD | Implementazione SIUS | Score |
|-------------|---------------------|-------|
| Aggregates | Impliciti — FascicoloModel è aggregate root ma non lo sa | 🔴 Assente |
| Value Objects | Assenti — tutto è String/BigDecimal primitivo | 🔴 Assente |
| Domain Services | Controller (business logic implicita) | 🟡 Parziale |
| Domain Events | JMS per alcuni eventi async (TrasmissioneJMSController) | 🟡 Parziale |
| Bounded Contexts | 51 moduli = 51 bounded context impliciti | 🟢 Buono |
| Ubiquitous Language | Naming italiano coerente (fascicolo, udienza, stampa) | 🟢 Buono |

### 2.2 Layer dei Servizi

**Architettura a 4 layer (F3B pattern):**

```
HTTP Request
     ↓
[Action Layer]          → 985 classi, HTTP param extraction, redirect
     ↓ SIUSLookupRemote
[Controller Layer]      → 84 classi, business logic, Ex* methods
     ↓ new DirectDAO()
[DAO Layer]             → 110 classi, SQL construction, JDBC
     ↓ Oracle JDBC
[Oracle Database]       → schema condiviso con SICO/SIEP
```

**Transazione management**: Il framework F3B gestisce il ciclo di vita della connessione JDBC. La propagazione di transazione è **implicita e non dichiarativa** — i Controller chiamano i DAO in sequenza senza `@Transactional`. In caso di errore dopo il primo `INSERT`, il rollback deve essere chiamato esplicitamente. Trovati solo 6 punti di `rollback()` esplicito in tutto il codebase.

**Problema**: operazioni multi-DAO (es. inserisci fascicolo + inserisci soggetto + inserisci evento) possono lasciare il DB in stato inconsistente se la seconda o terza operazione fallisce senza rollback.

---

## 3. Persistence Layer

### 3.1 Pattern DAO — SIAPSqlDAO

Ogni DAO estende `SIAPSqlDAO` (classe base F3B). Il pattern di costruzione SQL è identico in tutti i 110 DAO:

```java
// Pattern universale nei DAO SIUS
public class FascicoloSiusSqlDAO extends SIAPSqlDAO {
    
    public FascicoloModel getFascicoloById(BigDecimal idFascicolo) throws DAOException {
        String lStatement = "SELECT * FROM FASCICOLO_SIUS f ";
        lStatement += " WHERE f.ID_FASCICOLO_SIUS = " + idFascicolo;  // BigDecimal: safe
        
        // Iterazione manuale su ResultSet
        Collection lCollection = this.select(lStatement);
        Iterator it = lCollection.iterator();  // raw type
        while (it.hasNext()) {
            Hashtable row = (Hashtable) it.next();  // raw Hashtable
            FascicoloModel m = new FascicoloModel();
            m.setIdFascicoloSius((BigDecimal) row.get("ID_FASCICOLO_SIUS"));
            m.setCodStatoFascicolo((String) row.get("COD_STATO_FASCICOLO"));
            // ... mapping manuale di ogni campo
        }
    }
}
```

**Criticità**:
- Nessun ORM — ogni campo mappato manualmente → propenso a errori di naming
- `Hashtable` raw type → unsafe cast a runtime
- Nessuna paginazione nativa — `SELECT *` su tabelle grandi
- SQL concatenato → SQL injection (vedi antipattern assessment)

### 3.2 Query Performance Analysis

| Pattern | Occorrenze | Rischio performance |
|---------|-----------|---------------------|
| `SELECT * FROM` senza WHERE | Stimato ~20% | 🔴 Full table scan su tabelle grandi |
| `lStatement += " WHERE campo = " + val` | 3.190 | 🟠 No bind vars = no query plan cache |
| JOIN espliciti in SQL | Diffuso | 🟢 Accettabile |
| Paginazione (ROWNUM/FETCH FIRST) | Raro | 🟠 Liste non paginate |
| Subquery correlate | Presente | 🟡 Verificare con EXPLAIN PLAN |

### 3.3 Schema Database

L'analisi del data layer è documentata in `docs/08_data.md`. Sommario:
- 43 entità principali nell'ER diagram
- Primary key: `ID_{ENTITY}` come `BigDecimal` (Oracle NUMBER → JDBC BigDecimal)
- FK naming convention: `{PREFIX}_ID_{PARENT_ENTITY}`
- Audit fields su tutte le tabelle (COD_OPERATORE_*, DATA_*)
- Soft delete: `COD_STATO_FASCICOLO = '99'`

---

## 4. Integration Layer

### 4.1 JMS Integration (Async)

Il modulo `be/jms/` gestisce la trasmissione asincrona di messaggi verso altri sistemi della giustizia.

```
be/jms/
├── controller/
│   ├── ITrasmissioneJMS.java          # interfaccia
│   └── TrasmissioneJMSController.java  # 1.657 LOC
└── action/
    ├── ActCancellaMessaggioTrasmesso.java
    ├── ActDettaglioMessaggioTrasmesso.java
    ├── ActListaMessaggiTrasmessi.java
    └── ActListaMessaggiTrasmessiReale.java
```

Questa è l'unica integrazione asincrona del sistema. Il controller gestisce coda JMS (JBoss MQ o ActiveMQ, da inferire dal deployment descriptor) per comunicazioni verso altri sistemi del Ministero.

### 4.2 Cross-Module Integration (SIAP EAR)

```
SIAP EAR (runtime)
├── SIUS module  → accede a siap.sico.* via SICOLookupRemote
├── SICO module  → base condivisa (Fascicolo, Soggetto, Evento)
├── SIEP module  → altro modulo giustizia (cross-join nel SQL)
└── Avvocatura   → avvocato/avvocatura sub-modules in SIUS stesso
```

`StampaController` importa direttamente `siap.sico.*` — tightly coupled al modulo SICO. Questo significa che SIUS non può essere deployato senza SICO.

---

## 5. Security Assessment

### 5.1 Autenticazione & Autorizzazione

| Aspetto | Implementazione | Score |
|---------|----------------|-------|
| Autenticazione | JAAS/JBoss Security (EAR level) | 🟡 Non verificabile da codebase |
| Autorizzazione | `getUtenteModel().getCodRuolo()` (5 punti nel codice) | 🔴 BASSA copertura |
| Session security | `fascicoloSiusGP` in sessione HTTP | 🟠 Session hijacking risk |
| Input validation | Nessuna framework validation | 🔴 ASSENTE |
| CSRF protection | Nessuna | 🔴 ASSENTE |
| SQL Injection | 3.190 punti di String concat | 🔴 CRITICO |

### 5.2 Filtro Minorenne

Una delle poche protezioni di sicurezza nel codice è il filtro applicato ai fascicoli di minori:

```java
// ActionSius.java
protected Collection getFiltroMinorenni(HttpServletRequest request) {
    // Applica filtro sui dati se il soggetto è minorenne
    // Richiede ruolo specifico per vedere dati di minori
}
```

Questo è corretto ma è implementato solo in alcune Action — non è un filtro trasversale garantito.

---

## 6. Osservabilità & Resilienza

### 6.1 Logging

```java
// Pattern attuale — Log4j 1.x
private static Logger logger = Logger.getLogger(StampaController.class);
logger.info("Inizio stampa ordinanza id=" + idOrdinanza);
logger.error("Errore stampa", ex);
```

**Problemi**:
- Log4j 1.x è EOL (agosto 2015) — CVE-2019-17571
- No structured logging (JSON) — non integrabile con log aggregation (ELK, Splunk)
- No correlation ID — impossibile tracciare una singola richiesta attraverso i log
- Log a livello INFO/ERROR, nessun livello WARN sistematico

### 6.2 Error Handling

```java
// Pattern ricorrente — stack trace perso
} catch (DAOException ex) {
    throw new F3BException("Errore: " + ex);  // ex.getMessage() solo, no cause
}

// Pattern corretto (raro)
} catch (DAOException ex) {
    logger.error("Errore DAO", ex);
    throw new SiesWsException(ex);  // causa preservata
}
```

### 6.3 Transaction Resilience

**Rollback non garantito**: Con sole 6 occorrenze di `rollback()` esplicito in un codebase da 1.294 file, la maggior parte delle operazioni multi-step non gestisce il rollback. Se un `INSERT` di un evento fallisce dopo che il fascicolo è già stato aggiornato, il DB rimane in stato inconsistente.

---

## 7. Backend Health Score Dettagliato

| Dimensione | Peso | Score | Weighted |
|------------|------|-------|---------|
| Architettura layer | 15% | 40 | 6.0 |
| Sicurezza | 25% | 5 | 1.25 |
| Testabilità | 20% | 0 | 0.0 |
| Error handling | 15% | 20 | 3.0 |
| Performance | 10% | 45 | 4.5 |
| Manutenibilità | 15% | 20 | 3.0 |
| **TOTALE** | **100%** | | **17.75 / 100** |

---

## 8. Refactoring Priority Matrix

| Priorità | Issue | Effort | Impatto | ROI |
|---------|-------|--------|---------|-----|
| 🔴 P1 | Log4j → SLF4J | 3gg | ALTO (sicurezza) | ⭐⭐⭐⭐⭐ |
| 🔴 P1 | Approval Tests (controller critici) | 4 sett | ALTO (safety net) | ⭐⭐⭐⭐⭐ |
| 🔴 P1 | SQL PreparedStatement (String params) | 8 sett | CRITICO (sicurezza) | ⭐⭐⭐⭐⭐ |
| 🟠 P2 | Encoding ISO → UTF-8 | 1 sett | MEDIO (build) | ⭐⭐⭐⭐ |
| 🟠 P2 | Interfacce per tutti i Controller | 3 sett | ALTO (DI, testability) | ⭐⭐⭐⭐ |
| 🟠 P2 | Rollback esplicito su operazioni multi-DAO | 2 sett | ALTO (data integrity) | ⭐⭐⭐⭐ |
| 🟡 P3 | God classes decomposizione | 6 mesi | ALTO (manutenibilità) | ⭐⭐⭐ |
| 🟡 P3 | Enum per stati/flag | 4 sett | MEDIO (type safety) | ⭐⭐⭐ |
| 🟡 P3 | Spring DI migration (strangler fig) | 12+ mesi | MOLTO ALTO | ⭐⭐⭐ |

---

## Reference Documents

- **Deep Dive**: `docs/00_deep_dive.md`
- **Software Architecture**: `docs/06_software_architecture.md`
- **Code Patterns**: `docs/07_code.md`
- **Data Architecture**: `docs/08_data.md`
- **Antipattern Assessment**: `docs/18_antipattern_deep_dive.md`
- **Metrics**: `docs/14_metrics.md`

---

## Change Log

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | 2026-04-24 | IMPACT AI Agent | Prima versione — backend deep assessment |