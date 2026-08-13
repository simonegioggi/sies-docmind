---
uniqueName: 14metrics
displayName: "14 metrics"
category: "GENERAL"
tags: []
---

# Metrics - Progetto SIUS

**Data**: 2026-04-24  
**Versione**: 1.0  
**Autori**: IMPACT AI Agent (analisi automatica codebase)  
**Audience**: Team tecnico, architetti, developer, project manager

> 📊 **Nota metodologica**: I conteggi SLOC sono stati prodotti con comandi `find`/`wc -l` (equivalenti a `cloc`) in quanto `cloc` non era disponibile nell'ambiente di analisi. I valori riflettono **total lines** (non SLOC netti); le stime SLOC netti (blank + comment lines sottratte) sono riportate separatamente.

---

## 1. Total Lines of Code

### Analisi per tipo di file (equivalente cloc)

```
Linguaggio     Files    Blank    Comment    Code(SLOC)    Total Lines
─────────────────────────────────────────────────────────────────────
Java           1.294   34.498     29.399       166.865       230.762
JSP              670   16.715      6.402       140.724       163.841
JavaScript         2      n/d        n/d           ~300           345
─────────────────────────────────────────────────────────────────────
TOTALE         1.966   51.213     35.801       307.889       394.948
─────────────────────────────────────────────────────────────────────
```

> **Fonte**: `find be -name "*.java" -exec wc -l {} +`, `find fe -name "*.jsp" -exec wc -l {} +`

### Note metodologiche

- **Blank lines Java**: 34.498 (rilevate con `grep -c "^[[:space:]]*$"`)
- **Comment lines Java**: 29.399 (righe che iniziano con `//` o `/*`)
- **Blank lines JSP**: 16.715
- **Comment lines JSP**: 6.402 (`<%-- ... --%>` + `//`)
- **JavaScript**: 2 file, tutti custom (nessuna libreria bundled rilevata)
- **CSS**: 0 file nel repository (CSS in dipendenze esterne SIAP)

### Librerie incluse nel codice sorgente

| Libreria | Trovata nel repo | Esclusioni applicate |
|---------|-----------------|----------------------|
| jQuery | ❌ No | N/A |
| Bootstrap | ❌ No | N/A |
| commons-io | ❌ No | N/A |
| log4j | ❌ No (dipendenza Maven/classpath) | N/A |
| F3B framework | ❌ No (EAR esterno, non nel repo) | N/A |

**Conclusione**: il repository SIUS non include librerie vendor nel codebase; sono tutte in dipendenze esterne al modulo. Il conteggio SLOC non richiede esclusioni.

---

## 2. Language Distribution

```
┌─────────────────────────────────────────────────────────────────┐
│  Distribuzione SLOC per linguaggio                              │
│                                                                 │
│  Java      ████████████████████████████░░  54,2%  (166.865)    │
│  JSP       ████████████████████████░░░░░░  45,7%  (140.724)    │
│  JavaScript ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   0,1%  (    300)    │
└─────────────────────────────────────────────────────────────────┘
```

### Distribuzione SLOC per layer architetturale (Java)

| Layer | Files | SLOC stimato | % del totale Java |
|-------|-------|-------------|-------------------|
| Action (HTTP handlers) | 985 | ~88.000 | ~53% |
| Controller (Business Logic) | 84 | ~55.000 | ~33% |
| DAO (Data Access) | 110 | ~19.000 | ~11% |
| Model (Domain Objects) | 93 | ~4.500 | ~3% |
| Util + ICostanti | 20 + 50 | ~400 | <1% |

> Note: La stima per layer è derivata proporzionalmente dalla distribuzione dei file e dalla media di 178 LOC/file Java.

---

## 3. Complexity Metrics

### Stima Cyclomatic Complexity (McCabe)

In assenza di uno strumento di analisi statica (SonarQube, PMD), la complessità è stimata basandosi sui conteggi di costrutti condizionali nel codice.

| File | LOC | Stima CC | Categoria |
|------|-----|----------|-----------|
| `StampaController.java` | 6.470 | ~350+ | 🔴 CRITICA |
| `FascicoloSiusController.java` | 5.427 | ~300+ | 🔴 CRITICA |
| `DepositoOrdinanzaPcController.java` | 4.071 | ~200+ | 🔴 ALTA |
| `FascicoloSiusUDSController.java` | 3.548 | ~180+ | 🟠 ALTA |
| `DepositoDecretoController.java` | 3.458 | ~170+ | 🟠 ALTA |
| `FascicoloSiusSoggettoSqlDAO.java` | 3.245 | ~120+ | 🟠 ALTA |
| Media per file Action | ~178 | ~8-12 | 🟢 NORMALE |
| Media per file Controller | ~650 | ~35+ | 🟡 MEDIA |
| Media per file DAO | ~170 | ~12+ | 🟢 NORMALE |

**Soglie di riferimento** (per metodo):
- CC < 10: Bassa complessità (testabile)
- CC 10-20: Moderata (difficile da testare)
- CC > 20: Alta (quasi non testabile)
- CC > 50: Inaccettabile (rifattorizzazione urgente)

### Costrutti che alzano la complessità

| Costrutto | Occorrenze (grep) | Impatto CC |
|-----------|------------------|-----------|
| `if` statements | ~15.000 stimati | +1 per `if` |
| `catch(Exception)` generico | 1.127 | Pattern di soppressione errori |
| `lStatement +=` (SQL concatenato) | 3.190 | Nesting logico elevato |
| TODO/FIXME/STUB | 660 | Logica incompleta |

---

## 4. Module/Component Count

### Distribuzione moduli dominio

| Modulo | Actions | Controller | DAO | Model | Note |
|--------|---------|-----------|-----|-------|------|
| richiestaatti | 174 | 1 | 2 | 3 | Modulo più grande |
| fascicolo | 88 | 2 | 5 | 8 | Core del sistema |
| depositoordinanzapc | 84 | 1 | 3 | 4 | JSP più grandi |
| statistiche | 56 | 1 | 3 | 5 | |
| depositodecreto | 53 | 1 | 3 | 3 | |
| udienza | 52 | 1 | 2 | 3 | |
| presaincarico | 40 | 1 | 2 | 3 | |
| depositosentenza | 36 | 1 | 2 | 3 | |
| provvedimento | 29 | 1 | 2 | 3 | |
| misurasicurezza | 26 | 1 | 1 | 2 | |
| *altri 40 moduli* | ~297 | ~40 | ~89 | ~59 | |
| **TOTALE** | **935** | **52\*** | **114** | **96** | |

> \* Include Controller + ControllerUDS dove presenti

### Totale componenti per tipo

```
┌──────────────────────────────────────────────────────────┐
│  Componenti Java per categoria                           │
│                                                          │
│  Action classes:      935  ████████████████████████████  │
│  ICostanti interfaces: 50  ██                            │
│  DAO classes:         110  ███                           │
│  Model classes:        93  ███                           │
│  Controller classes:   52  ██                            │
│  Util classes:         20  █                             │
│  Total Java files:  1.294                                │
└──────────────────────────────────────────────────────────┘
```

### Distribuzione JSP per modulo

| Modulo | JSP | Linee totale | JSP più grande |
|--------|-----|-------------|---------------|
| depositoordinanzapc | ~35 | ~25.000 | ModificaOrdinanzaReclamoLA.jsp (5.799) |
| fascicolo | ~80 | ~18.000 | DettaglioFascicolo.jsp (1.488) |
| *altri moduli* | ~555 | ~120.000 | — |
| **TOTALE** | **670** | **163.841** | |

---

## 5. Dependency Metrics

### Dipendenze a livello di codice

| Tipo dipendenza | Occorrenze | Impatto |
|----------------|-----------|---------|
| `SIUSLookupRemote.lookup()` | ~400+ | Accoppiamento statico verso Service Locator |
| `fascicoloSiusGP` (session) | 509 | Accoppiamento a sessione HTTP |
| Import non gestiti (classpath SIAP) | n/d | Dipendenza runtime EAR esterno |

### Instability per layer

L'instability (I = Ce / (Ca + Ce)) misura il grado di dipendenza di un layer da altri.

| Layer | Ca (afferente) | Ce (efferente) | I | Note |
|-------|---------------|---------------|---|------|
| Action | Alto | Basso | ~0.2 | Dipende da Controller, usato da nessuno |
| Controller | Basso | Alto | ~0.8 | Dipende da DAO e Model |
| DAO | Nessuno | F3B DAO base | ~0.9 | Dipende solo da DB |
| Model | Nessuno | Nessuno | 0.0 | Puro POJO |

### Fan-out del Service Locator

```java
// SIUSLookupRemote mappa 40+ controller
SIUSLookupRemote.lookup(FascicoloSiusController.class)  // -> be.fascicolo.controller
SIUSLookupRemote.lookup(StampaController.class)         // -> be.stampa.controller
// ... 40 mappings
```

---

## 6. Code Quality Metrics

### Summary score

| Metrica | Valore | Soglia OK | Status |
|---------|--------|-----------|--------|
| Java files con encoding ISO-8859-1 | 565 / 1.294 | < 5% | 🔴 **43,7%** |
| `catch(Exception)` generico | 1.127 | < 50 | 🔴 CRITICO |
| SQL concatenazione string | 3.190 | 0 | 🔴 CRITICO |
| TODO/FIXME nel codice | 660 | < 50 | 🔴 ALTO |
| God Classes (> 1.000 LOC) | 18 stimati | 0 | 🔴 ALTO |
| File con 0 test coverage | 1.294 / 1.294 | < 10% | 🔴 **100%** |
| Classi con generics | ~7 / 1.294 | > 80% | 🔴 <1% |
| Javadoc coverage (metodi pubblici) | ~5% stimato | > 50% | 🔴 BASSO |

### God Classes (> 1.000 LOC — lista parziale)

| File | LOC | Responsabilità |
|------|-----|----------------|
| StampaController.java | 6.470 | Gestione tutta la stampa del sistema |
| FascicoloSiusController.java | 5.427 | CRUD fascicolo + tutta la logica business |
| DepositoOrdinanzaPcController.java | 4.071 | Deposito ordinanze |
| FascicoloSiusUDSController.java | 3.548 | Variante UDS del fascicolo |
| DepositoDecretoController.java | 3.458 | Deposito decreti |
| FascicoloSiusSoggettoSqlDAO.java | 3.245 | DAO soggetti — query complesse |
| StatisticheSiusController.java | 2.506 | Report e statistiche |
| ActModificaProvvedimento.java | 2.390 | Action enorme (violazione SRP) |
| ActInserisciOrdinanzaUDS.java | 1.946 | |
| TrasmissioneJMSController.java | 1.657 | |
| UnificazioneController.java | 1.614 | |
| DepositoSentenzaController.java | 1.451 | |

### Encoding inconsistency

```
Total Java files:     1.294
UTF-8:                  729  (56,3%)
ISO-8859-1 (binary):    565  (43,7%)  ← PROBLEMA
```

> Questo causa problemi di compilazione cross-platform, errori su stringhe con caratteri italiani (àèìòù), e difficoltà di revisione su editor moderni.

### Raw types usage (no generics)

```java
// Pattern tipico trovato in codebase
Vector v = new Vector();           // raw type
Hashtable ht = new Hashtable();    // raw type
ArrayList lista = new ArrayList(); // raw type
Enumeration e = v.elements();      // raw type
```

Stima: 1.287+ occorrenze di raw `Vector`/`Collection`/`Hashtable` (da analisi precedente).

---

## 7. Test Coverage Metrics

### Stato attuale

| Metrica | Valore |
|---------|--------|
| File di test presenti | **0** |
| Classi con test | **0** |
| Test coverage (linee) | **0%** |
| Test coverage (branch) | **0%** |

### Analisi gap

```
Files Java totali:          1.294
Files di test (JUnit):          0  ← ZERO
Coverage totale:             0,0%
```

### Impatto sulla refactorizzazione

La **assenza totale di test** è il singolo fattore di rischio più elevato per qualsiasi attività di refactoring:

1. **Nessuna safety net**: ogni modifica può introdurre regressioni silenti
2. **Nessuna caratterizzazione del comportamento**: il comportamento atteso non è formalmente documentato
3. **Stima costi refactoring**: +40-60% di effort aggiuntivo per scrivere test di caratterizzazione prima di refactoring

### Strategia di testing raccomandata

Prima di qualsiasi refactoring, seguire questa priorità:

```
1. Characterization Tests (Approval Testing)
   → Catturare l'output attuale come "golden master"
   → Strumenti: ApprovalTests, Combinatorial Testing

2. Integration Tests (DB)
   → DAO layer: test con Oracle in-memory (H2 in Oracle compat mode)
   → Copertura minima: tutti i DAO, almeno happy path

3. Unit Tests (Action/Controller)
   → Mockito per SIUSLookupRemote
   → JUnit 5 (upgrade da JUnit 3.8.1 necessario)

4. Coverage target
   → Phase 1 (pre-refactoring): 30% coverage
   → Phase 2 (during refactoring): 60% coverage
   → Phase 3 (post-refactoring): 80% coverage
```

---

## 8. Technical Debt Quantification

### SQALE-inspired estimate

Usando la regola empirica **10 minuti per LOC di debito tecnico** applicata ai problemi critici:

| Categoria | Volume | Effort stimato |
|-----------|--------|---------------|
| Test coverage (0% → 60%) | 185K SLOC | ~5.500 ore |
| SQL injection fixes (prepared stmt) | 3.190 | ~1.600 ore |
| Encoding unification (ISO→UTF-8) | 565 file | ~280 ore |
| God classes decomposition | 12 classi | ~960 ore |
| Raw types → Generics | 1.287 | ~640 ore |
| catch(Exception) specifico | 1.127 | ~560 ore |
| Log4j → SLF4J migration | 1 config | ~80 ore |
| **TOTALE DEBITO TECNICO** | | **~9.620 ore** |

> ~9.620 ore ≈ **240 settimane-persona** (1 developer) ≈ **4,6 anni** a 1 developer, **24 mesi** a 5 developer.

### Indice di Manutenibilità (MI — formula SEI)

```
MI = MAX(0, (171 - 5.2 × ln(HV) - 0.23 × CC - 16.2 × ln(LOC)) × 100 / 171)
```

Stima approssimativa per i componenti più critici:

| Componente | MI stimato | Giudizio |
|------------|-----------|---------|
| God classes (StampaController, ...) | 10-25 | 🔴 Non manutenibile |
| Controller medi (300-700 LOC) | 30-45 | 🟠 Bassa manutenibilità |
| Action medie (100-200 LOC) | 55-70 | 🟡 Media manutenibilità |
| DAO semplici (<150 LOC) | 70-85 | 🟢 Buona manutenibilità |

---

## Reference Documents

- **Deep Dive Analysis**: `docs/00_deep_dive.md`
- **Software Architecture**: `docs/06_software_architecture.md`
- **Code**: `docs/07_code.md`
- **Data**: `docs/08_data.md`
- **Decision Log**: `docs/13_decision_log.md`

---

## Change Log

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | 2026-04-24 | IMPACT AI Agent | Prima versione — metriche da analisi statica codebase |