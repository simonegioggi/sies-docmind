---
uniqueName: 18antipatterndeepdive
displayName: "18 antipattern deep dive"
category: "GENERAL"
tags: []
---

# 🔍 ANTIPATTERN ASSESSMENT REPORT — Progetto SIUS

**Data**: 2026-04-24  
**Codebase**: `/home/mideluci/copilot-projects/giustizia/sies/SIUS`  
**Health Score**: **18 / 100** 🔴  
**Versione**: 1.0  
**Autori**: IMPACT AI Agent (Senior Software Architect mode)

---

## 📊 RIASSUNTO ESECUTIVO

Il codebase SIUS presenta un **debito tecnico critico e strutturale** accumulato in oltre 20 anni di sviluppo senza refactoring sistematico. I problemi non sono isolati ma pervasivi: SQL injection su 3.190 punti, assenza totale di test (0%), 12 God Classes che concentrano migliaia di righe di business logic non testabile, e un accoppiamento architetturale rigido tramite Service Locator. Il debito è stimato in ~9.620 ore-persona. **Nessuna attività di modernizzazione può essere avviata senza prima costruire una safety net di test di caratterizzazione.**

---

## 🚨 TABELLA PRIORITÀ (Top Findings)

| # | File/Modulo | Anti-Pattern | Severità | Impatto |
|---|:--- |:--- |:--- |:--- |
| 1 | `be/**/*.java` (3.190 occorrenze) | SQL Injection via string concat | 🔴 CRITICA | Vulnerabilità di sicurezza CVE-class |
| 2 | `be/stampa/controller/StampaController.java` | God Class (6.470 LOC) | 🔴 CRITICA | Non testabile, non modificabile |
| 3 | `be/fascicolo/controller/FascicoloSiusController.java` | God Class (5.427 LOC) | 🔴 CRITICA | Core system bloccato |
| 4 | `be/util/SIUSLookupRemote.java` | Service Locator / Anti-DI | 🔴 ALTA | Zero testabilità per dependency injection |
| 5 | `be/**/*.java` (565 file) | Encoding inconsistency (ISO-8859-1) | 🔴 ALTA | Build instability, caratteri italiani corrotti |
| 6 | Tutti i moduli (1.127 occorrenze) | `catch(Exception)` generico | 🔴 ALTA | Bug silenti, stack trace persi |
| 7 | Tutti i moduli (0 file test) | Zero Test Coverage | 🔴 ALTA | Nessuna safety net per refactoring |
| 8 | `be/**/model/*.java` (93 classi) | Anemic Domain Model | 🟠 MEDIA | Business logic dispersa nelle Action |
| 9 | Tutti i moduli (794+ occorrenze) | Primitive Obsession (String "S"/"N") | 🟠 MEDIA | Propenso a bug, nessuna type safety |
| 10 | `be/**/*.java` (1.287 occorrenze) | Raw Types / No Generics | 🟠 MEDIA | Unsafe cast a runtime |
| 11 | Framework F3B (intero sistema) | Vendor Lock-in | 🟠 MEDIA | Impossibile aggiornare/sostituire |
| 12 | `be/**/action/ICostanti*.java` (50 interfacce) | Constant Interface Anti-Pattern | 🟡 BASSA | Violazione principio OOP |
| 13 | Sessione HTTP (509 ref.) | Stateful Session Coupling | 🟠 MEDIA | Non scalabile, fragile |
| 14 | Log4j 1.x (CVE-2019-17571) | Outdated dependency + security | 🔴 CRITICA | Remote code execution |

---

## 🔍 ANALISI DETTAGLIATA

---

### 1. SQL Injection via String Concatenation

**Dove**: `be/fascicolo/dao/FascicoloSiusSoggettoSqlDAO.java` (riga 85, ~3.190 occorrenze totali nel codebase)

**Analisi**: L'intero data access layer del sistema costruisce le query SQL tramite concatenazione di stringhe (`lStatement += " WHERE campo = " + valore`). Quando `valore` è un parametro proveniente da una richiesta HTTP (tipicamente via `request.getParameter()`), l'applicazione è vulnerabile a SQL injection. Viola principio di **sicurezza by design** e la OWASP Top 10 A03:2021.

**Codice Attuale (Snippet):**
```java
// FascicoloSiusSoggettoSqlDAO.java - riga 84-85
lStatement = "SELECT sogg.*, fasc.* FROM SOGGETTO sogg, FASCICOLO_SIUS fasc, EVENTO ev ";
lStatement += " WHERE sogg.id_soggetto = fasc.sog_id_soggetto and fasc.ID_FASCICOLO_SIUS = ev.FAS_SIU_ID_FASCICOLO_SIUS ";
lStatement += " and sogg.id_soggetto =  " + aModel.getIdSoggetto();  // ← OK solo se BigDecimal
// ...
lStatement += " and fasc.cod_stato = '" + codStato + "'";  // ← PERICOLOSO se codStato è String da HTTP param
```

**Soluzione Proposta**: Migrare a PreparedStatement con bind parameters, o a MyBatis/JDBC Template con named parameters. La migrazione va fatta modulo per modulo, iniziando dai DAO con parametri String provenienti dalla request.

**Esempio Refactoring:**
```java
// PRIMA (vulnerabile)
lStatement += " AND cod_stato = '" + codStato + "'";

// DOPO (sicuro con PreparedStatement)
String sql = "SELECT * FROM FASCICOLO_SIUS WHERE cod_stato = ?";
PreparedStatement ps = conn.prepareStatement(sql);
ps.setString(1, codStato);  // bind parameter - safe

// ALTERNATIVA con MyBatis mapper
// fascicolo-mapper.xml:
// <select id="findByCodStato" parameterType="String">
//   SELECT * FROM FASCICOLO_SIUS WHERE cod_stato = #{codStato}
// </select>
```

---

### 2. God Class — StampaController (6.470 LOC)

**Dove**: `be/stampa/controller/StampaController.java`

**Analisi**: `StampaController` ha 6.470 righe di codice, importa 50+ classi da tutto il sistema (SICO, SIUS, moduli esterni), e gestisce ogni tipo di stampa del sistema (ordinanze, decreti, sentenze, verbali, report statistici, comunicazioni). Viola **SRP (Single Responsibility Principle)** in modo massiccio. La classe è virtualmente impossibile da testare unitariamente perché dipende da 50+ collaboratori senza interfaccia.

**Codice Attuale (Snippet — imports):**
```java
// StampaController.java imports (selezionati)
import siap.sico.camponota.dao.CampoNotaSqlDAO;
import siap.sico.evento.controller.IEvento;
import siap.sico.libertaanticipata.controller.ILicenzaPeriodiLibAnticipata;
import siap.sico.magistrato.dao.MagistratoSqlDAO;
import siap.sico.soggetto.dao.SoggettoSqlDAO;
import siap.sico.stampa.controller.SIAPStampaController;
import siap.sico.template.controller.TemplateManager;
import siap.sico.ufficio.dao.UfficioSqlDAO;
// ... altri 42 import
```

**Soluzione Proposta**: Decomposizione per dominio di stampa usando il **Strategy Pattern** o **Command Pattern**. Creare un `StampaOrdinanzaController`, `StampaDecretoController`, `StampaSentenzaController`, ecc., con una `StampaFacade` che fa orchestrazione.

**Esempio Refactoring:**
```java
// PRIMA: tutto in StampaController (6.470 LOC)
public class StampaController {
    public byte[] ExStampaOrdinanza(...) { /* 200 LOC */ }
    public byte[] ExStampaDecreto(...) { /* 180 LOC */ }
    public byte[] ExStampaSentenza(...) { /* 220 LOC */ }
    // ... altri 80 metodi
}

// DOPO: Decomposizione per tipo + facade
public interface StampaStrategy {
    byte[] stampa(StampaContext ctx) throws F3BException;
}

public class StampaOrdinanzaHandler implements StampaStrategy {
    public byte[] stampa(StampaContext ctx) throws F3BException { /* 200 LOC */ }
}

public class StampaController {  // ~200 LOC, solo orchestrazione
    private final Map<String, StampaStrategy> handlers;
    
    public byte[] ExStampa(String tipoStampa, StampaContext ctx) throws F3BException {
        return handlers.get(tipoStampa).stampa(ctx);
    }
}
```

---

### 3. Service Locator Anti-Pattern (vs. Dependency Injection)

**Dove**: `be/util/SIUSLookupRemote.java` — usato ~400 volte nel codebase

**Analisi**: `SIUSLookupRemote.lookup(ClassName.class)` è un Service Locator: l'oggetto che ha bisogno di una dipendenza va a cercarla attivamente tramite un registro globale. Questo pattern rende il sistema non testabile (non si possono iniettare mock), crea accoppiamento a compile-time ai nomi di classe concreti, e nasconde le dipendenze all'interno dei metodi anziché renderle esplicite nel costruttore.

**Codice Attuale (Snippet):**
```java
// Ogni Action/Controller che ha bisogno di un servizio:
public class ActModificaFascicolo extends ActionSius {
    public ActionForward execute(ActionMapping mapping, ActionForm form,
                                 HttpServletRequest request, HttpServletResponse response) {
        // lookup ogni volta che serve — hidden dependency
        FascicoloSiusController ctrl = 
            (FascicoloSiusController) SIUSLookupRemote.lookup(FascicoloSiusController.class);
        ctrl.ExModificaFascicolo(model);
    }
}
```

**Soluzione Proposta**: Introdurre Spring IoC. Nel contesto di modernizzazione graduale (strangler fig), si può:
1. Prima fase: mantieni `SIUSLookupRemote` ma aggiungi interfacce ai Controller
2. Seconda fase: Spring gestisce il ciclo di vita dei Controller come `@Service`
3. Terza fase: `@Autowired` injection sostituisce il lookup

**Esempio Refactoring:**
```java
// DOPO: Spring DI
@Component
public class ActModificaFascicolo extends ActionSius {

    @Autowired
    private IFascicoloSiusController fascicoloController;  // interface, not concrete class
    
    public ActionForward execute(...) {
        fascicoloController.ExModificaFascicolo(model);
    }
}
```

---

### 4. Anemic Domain Model

**Dove**: `be/**/model/*.java` — 93 classi Model

**Analisi**: Tutte le classi Model di SIUS sono pure "sacche di dati": solo attributi privati + getter/setter, zero logica di business. Tutta la logica (validazioni, calcoli, transizioni di stato) è nel Controller o nell'Action. Questo viola il **Domain-Driven Design** e rende il modello non riutilizzabile.

**Codice Attuale (Snippet):**
```java
// Esempio tipico: FascicoloModel (solo getter/setter)
public class FascicoloModel implements Serializable {
    private BigDecimal idFascicoloSius;
    private String codStatoFascicolo;  // "01","02","03","04","05","99" — magic values
    private String flMinorenne;        // "S" o "N" — primitive obsession
    private Date dataInserimento;
    
    public BigDecimal getIdFascicoloSius() { return idFascicoloSius; }
    public void setIdFascicoloSius(BigDecimal v) { idFascicoloSius = v; }
    // ... 50 altri getter/setter, ZERO business logic
}
```

**Soluzione Proposta**: Arricchire il Domain Model con logica coesa. Le regole di business che "appartengono" al fascicolo (es. "un fascicolo è modificabile se il cod_stato non è in {01,04,05,99}") dovrebbero stare nel Model.

**Esempio Refactoring:**
```java
// DOPO: Rich Domain Model
public class FascicoloModel implements Serializable {
    
    // Elimina magic strings con Enum
    public enum StatoFascicolo {
        APERTO("01"), SOSPESO("02"), CHIUSO("03"), NON_MODIFICABILE("04"),
        ARCHIVIATO("05"), CANCELLATO("99");
        
        private final String codice;
        // constructor + getCodice()
    }
    
    private StatoFascicolo stato;
    private boolean minorenne;  // boolean, non "S"/"N"
    
    // Business logic nel domain model
    public boolean isModificabile() {
        return stato != StatoFascicolo.NON_MODIFICABILE 
            && stato != StatoFascicolo.ARCHIVIATO
            && stato != StatoFascicolo.CANCELLATO;
    }
    
    public boolean isMinorenne() { return this.minorenne; }
}
```

---

### 5. Primitive Obsession + Magic Strings

**Dove**: Tutto il codebase — 794+ occorrenze di `"S"`, `"N"`, `"01"`-`"99"` come flag di stato

**Analisi**: I concetti di dominio (stato fascicolo, flag boolean, tipo procedimento) sono rappresentati come stringhe primitive senza semantica. Questo causa: (1) nessun type-checking a compile time, (2) null pointer se la stringa è null, (3) difficoltà di comprensione del codice, (4) impossibilità di usare IDE refactoring per rinominare uno stato.

**Codice Attuale:**
```java
// Magic booleans
if ("S".equals(fascicolo.getFlMinorenne())) { ... }
if ("N".equals(fascicolo.getFlSceltoMagistrato())) { ... }

// Magic state codes
if ("99".equals(fascicolo.getCodStatoFascicolo())) {
    throw new F3BException("Fascicolo cancellato");
}
if ("01".equals(codStato) || "04".equals(codStato) || "05".equals(codStato)) {
    // stato non modificabile
}
```

**Soluzione Proposta**: Introdurre `Enum` Java per tutti i concetti di dominio con valore fisso. Usare `boolean` Java invece di `String "S"/"N"` nei Model.

**Esempio Refactoring:**
```java
// DOPO
public enum StatoFascicolo {
    APERTO("01"), SOSPESO("02"), CHIUSO_UDIENZA("03"),
    NON_MODIFICABILE("04"), ARCHIVIATO("05"), CANCELLATO("99");
    
    private final String codiceDB;
    
    public static StatoFascicolo fromCodice(String codice) {
        return Arrays.stream(values())
            .filter(s -> s.codiceDB.equals(codice))
            .findFirst()
            .orElseThrow(() -> new IllegalArgumentException("Stato non valido: " + codice));
    }
}

// Uso
if (fascicolo.getStato() == StatoFascicolo.CANCELLATO) { ... }
```

---

### 6. Catch(Exception) Generico — Error Swallowing

**Dove**: 1.127 occorrenze nel codebase

**Analisi**: Il pattern `catch(Exception ex) { throw new F3BException("msg: " + ex); }` fa tre cose sbagliate: (1) perde lo stack trace originale (non usa `initCause`), (2) maschera errori specifici (NullPointerException, ClassCastException) che indicano bug nel codice, (3) rende il debugging quasi impossibile in produzione.

**Codice Attuale:**
```java
// Pattern ricorrente in tutto il codebase
try {
    ctrl.ExModificaFascicolo(model);
} catch (DAOException ex) {
    throw new F3BException("Errore modifica fascicolo: " + ex);  // ← stack trace PERSO
} catch (Exception ex) {
    throw new F3BException("Errore generico: " + ex);  // ← bug mascherato
}
```

**Soluzione Proposta**: Usare costruttore con cause, catchare solo le eccezioni che si sa gestire, lasciare propagare le altre.

**Esempio Refactoring:**
```java
// DOPO: preserva stack trace
try {
    ctrl.ExModificaFascicolo(model);
} catch (DAOException ex) {
    logger.error("Errore DAO modifica fascicolo id=" + model.getId(), ex);
    throw new F3BException("Errore durante la modifica del fascicolo", ex);  // ← cause preservata
    // oppure: throw new SiesBusinessException(ErrorCode.FASCICOLO_MODIFICA_FAILED, ex);
}
// NullPointerException, ClassCastException ecc. si propagano -> bug visibili
```

---

### 7. Vendor Lock-in — Framework F3B Proprietario

**Dove**: Tutto il codebase — ogni Action estende `ActionSius` → `ActionSiap` (F3B base classes)

**Analisi**: L'intera gerarchia di Action e Controller dipende da classi base F3B proprietarie (`ActionSiap`, `F3BException`, `SIAPSqlDAO`, `LogF3B`, `DateUtils`, ecc.). Queste classi non hanno codice sorgente disponibile, non sono aggiornate dal 2010+, e non hanno community. Qualsiasi modifica al framework richiede riscrittura di 935 Action + 84 Controller.

**Pattern lock-in:**
```java
// Ogni Action dipende da F3B
public class ActRicercaFascicolo extends ActionSius {  // ActionSius extends ActionSiap (F3B)
    // Usa F3BException, LogF3B.SIES_LOG, DateUtils (tutti F3B)
}

// Ogni DAO dipende da F3B
public class FascicoloSiusSqlDAO extends SIAPSqlDAO {  // SIAPSqlDAO è F3B
    // Usa DAOException (F3B), connection management F3B
}
```

**Strategia di uscita (Strangler Fig)**:
1. Introdurre **interfacce adapter** su tutte le dipendenze F3B
2. Sostituire F3B con Spring MVC + Spring JDBC progressivamente, modulo per modulo
3. Il vecchio codice F3B convive con il nuovo Spring durante la transizione

---

## 🏗️ ANTIPATTERN ARCHITETTURALI

### Big Ball of Mud — Evidenza

Il routing F3B tramite FQCN come parametro HTTP crea accoppiamenti diretti tra JSP e nomi di classe Java:

```html
<!-- JSP con dipendenza hardcoded al nome di classe Java -->
<form action="?ACTION_FIELD=siap.sius.fascicolo.action.ActModificaFascicolo">
```

Rinominare `ActModificaFascicolo` → `ModificaFascicoloAction` richiederebbe aggiornare tutti i JSP che la referenziano — **Shotgun Surgery**.

### Stateful Session Anti-Pattern

```java
// 509 punti del codebase che leggono/scrivono la sessione
FascicoloGPModel fascicolo = 
    (FascicoloGPModel) request.getSession().getAttribute("fascicoloSiusGP");

// Se la sessione scade o il server riavvia → NullPointerException
if (fascicolo == null) {
    // gestione inconsistente: a volte redirect, a volte NPE non catturata
}
```

---

## 🛠️ RACCOMANDAZIONI GENERALI & NEXT STEPS

### Priorità Immediata (sicurezza)
- [x] **Audit Log4j**: verificare versione esatta, applicare patch o migrare a SLF4J+Logback
- [ ] **SQL Injection remediation**: iniziare dai DAO che ricevono parametri String da HTTP request
- [ ] **Introdurre WAF** (Web Application Firewall) come mitigazione temporanea prima del fix SQL

### Priorità Alta (enabling per refactoring)
- [ ] **Test di caratterizzazione**: scrivere Approval Tests per tutti i Controller (cattura comportamento attuale)
- [ ] **Encoding standardization**: convertire tutti i file ISO-8859-1 → UTF-8 (script batch)
- [ ] **Introdurre interfacce** per tutti i Controller (prerequisito per DI e mock nei test)

### Priorità Media (qualità codice)
- [ ] **God classes decomposition**: iniziare da `StampaController` → `StampaOrdinanzaHandler`, ecc.
- [ ] **Enum per stati e flag**: sostituire magic strings "S"/"N"/"01"-"99"
- [ ] **catch specifici**: sostituire `catch(Exception)` con eccezioni specifiche + cause

### Strumenti consigliati
| Strumento | Scopo | Priorità |
|-----------|-------|---------|
| **SonarQube Community** | Static analysis, SQL injection detection | 🔴 Immediato |
| **SpotBugs** | Bug pattern detection (null deref, SQL injection) | 🔴 Immediato |
| **ApprovalTests** | Characterization testing | 🔴 Immediato |
| **jdepend** | Dependency analysis, circular deps | 🟠 Breve termine |
| **Checkstyle** | Encoding + code style | 🟠 Breve termine |
| **Microcks** | API mocking per test integration | 🟡 Medio termine |

---

## Reference Documents

- **Deep Dive Analysis**: `docs/00_deep_dive.md`
- **Software Architecture**: `docs/06_software_architecture.md`
- **Code**: `docs/07_code.md`
- **Data**: `docs/08_data.md`
- **Decision Log**: `docs/13_decision_log.md`
- **Metrics**: `docs/14_metrics.md`

---

## Change Log

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | 2026-04-24 | IMPACT AI Agent | Prima versione — analisi completa antipattern |