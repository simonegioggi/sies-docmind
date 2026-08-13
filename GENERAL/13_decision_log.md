---
uniqueName: 13decisionlog
displayName: "13 decision log"
category: "GENERAL"
tags: []
---

# Decision Log - Progetto SIUS

**Data**: 2026-04-24  
**Versione**: 1.0  
**Autori**: IMPACT AI Agent (decisioni ricostruite da analisi codebase)  
**Audience**: Team tecnico, architetti, developer

> ⚠️ **Nota metodologica**: Le decisioni qui documentate sono **ricostuite a posteriori** dall'analisi del codice, in assenza di ADR o documentazione tecnica originale. Riflettono il razionale architetturale implicito nel codebase, non decisioni formalmente documentate al momento della loro presa.

---

## 1. Technology Decisions

### TD-01: Adozione del Framework F3B (Proprietario Bull/Atos)

| Campo | Valore |
|-------|--------|
| **Stato** | Accepted (decisione storica, ~2002) |
| **Contesto** | Il sistema SIAP necessitava di un framework MVC per applicazioni Java EE enterprise per la PA italiana |
| **Decisione** | Adottare il framework proprietario F3B sviluppato da Bull (poi Atos) invece di framework open source (Struts, Spring MVC) |
| **Razionale** | Contratto di fornitura con Bull; framework disponibile e collaudato nell'ecosistema Bull/PA; standardizzazione di tutti i moduli SIAP su un unico framework |
| **Conseguenze** | ✅ Uniformità tra tutti i moduli SIAP (SICO, SIEP, SIUS) — ❌ Vendor lock-in totale: impossibile aggiornare o sostituire il framework senza riscrivere tutto |
| **Status attuale** | ⚠️ RISCHIO — framework inattivo, nessuna community, nessun aggiornamento di sicurezza |

---

### TD-02: Oracle come Database Unico per Tutta la Piattaforma SIAP

| Campo | Valore |
|-------|--------|
| **Stato** | Accepted |
| **Contesto** | Schema condiviso tra SICO, SIEP, SIUS e Avvocatura |
| **Decisione** | Un singolo schema Oracle condiviso da tutti i moduli |
| **Razionale** | Semplicità di deployment; join cross-modulo performanti; nessuna gestione di transazioni distribuite; contratto Oracle con Ministero della Giustizia |
| **Conseguenze** | ✅ Join tra FASCICOLO_SIUS e FASCICOLO_SIEP diretti in SQL — ❌ Impossibile scalare moduli indipendentemente; qualsiasi migrazione richiede coordinamento totale |

---

### TD-03: Log4j 1.x come Framework di Logging

| Campo | Valore |
|-------|--------|
| **Stato** | Outdated — da sostituire |
| **Contesto** | Scelta ~2002-2005, standard de facto Java del periodo |
| **Decisione** | Log4j 1.x con custom category `LogF3B.SIES_LOG` |
| **Razionale** | Standard dell'epoca; integrato nel framework F3B |
| **Conseguenze** | ❌ EOL 2015; CVE-2019-17571 (RCE via SocketServer); nessun structured logging |
| **Azione richiesta** | **IMMEDIATA**: migrare a SLF4J + Logback |

---

## 2. Architectural Decisions (ADRs)

### ADR-01: Monolith Modulare invece di Microservices

| Campo | Valore |
|-------|--------|
| **Stato** | Accepted (storico) |
| **Contesto** | Sistema progettato ~2002-2005, prima dell'era microservizi |
| **Decisione** | Architettura monolitica modulare: tutti i moduli (SICO, SIEP, SIUS, Avvocatura) deployati nello stesso EAR JBoss |
| **Razionale** | ✅ Semplicità operativa; ✅ Performance delle chiamate in-process; ✅ Transazioni ACID semplificate; ✅ Tecnologia del periodo |
| **Alternativa scartata** | SOA/Web Services (troppo overhead per il periodo) |
| **Conseguenze** | ✅ Deployment semplice — ❌ Impossibile scalare moduli singoli; ❌ Un bug in un modulo può abbattere tutto; ❌ Non cloud-native |

---

### ADR-02: Service Locator invece di Dependency Injection

| Campo | Valore |
|-------|--------|
| **Stato** | Accepted (storico) — da riconsiderare |
| **Contesto** | Java EE ~2002: Spring DI non era ancora mainstream nella PA italiana |
| **Decisione** | `SIUSLookupRemote` come Service Locator centralizzato con `lookup()` via reflection |
| **Razionale** | ✅ Pattern Java EE standard del periodo (JNDI lookup); ✅ Già usato in SICO/SIEP |
| **Alternativa scartata** | Spring IoC (non adottato per vincolo di uniformità con framework F3B) |
| **Conseguenze** | ✅ Un punto centrale di accesso ai controller — ❌ Hard coupling; ❌ Non testabile (no mock injection); ❌ Anti-pattern moderno |

---

### ADR-03: HTTP Session come Store dello Stato del Fascicolo

| Campo | Valore |
|-------|--------|
| **Stato** | Accepted (storico) |
| **Contesto** | Applicazione web stateful: l'operatore lavora sempre su un fascicolo "corrente" |
| **Decisione** | Il `FascicoloGPModel` corrente viene salvato in sessione HTTP (`fascicoloSiusGP`) e usato da ogni Action |
| **Razionale** | ✅ Semplifica le Action (non rileggono il DB ad ogni richiesta); ✅ Pattern standard per web app J2EE stateful |
| **Conseguenze** | ✅ Performance lettura DB ridotte — ❌ Session failover = perdita stato; ❌ Dati potenzialmente stale; ❌ 509 punti di coupling in sessione; ❌ Non scalabile orizzontalmente senza session replication |

---

### ADR-04: SQL Costruito per Concatenazione di Stringa

| Campo | Valore |
|-------|--------|
| **Stato** | Accepted (storico) — **da cambiare** |
| **Contesto** | Framework F3B `SIAPSqlDAO` usa pattern `lStatement += " WHERE " + setCondizioni()` |
| **Decisione** | Costruzione dinamica di SQL per concatenazione, senza prepared statement / bind variables |
| **Razionale** | ✅ Semplicità di scrittura per sviluppatori; ✅ Flessibilità nella costruzione dinamica delle WHERE clause |
| **Conseguenze** | ❌ **Rischio SQL injection** su parametri String; ❌ Nessun beneficio del query plan caching Oracle; ❌ 3.190 occorrenze da rifattorizzare |
| **Mitigazione parziale** | Le PK sono `BigDecimal` (tipo safe), riducendo il rischio per i parametri numerici |

---

### ADR-05: Una Action per Operation (Command Pattern)

| Campo | Valore |
|-------|--------|
| **Stato** | Accepted |
| **Contesto** | Ogni operazione utente (inserisci, modifica, cancella, ricerca, carica form, ...) è una Action separata |
| **Decisione** | 935 Action classes — una per ciascuna operazione utente |
| **Razionale** | ✅ Single Responsibility a livello di Action; ✅ Facile aggiungere nuove operazioni senza modificare quelle esistenti |
| **Conseguenze** | ✅ Isolation tra operazioni — ❌ Proliferazione di classi; ❌ Logica comune duplicata tra Action simili |

---

### ADR-06: Rappresentazione Booleana come String "S"/"N"

| Campo | Valore |
|-------|--------|
| **Stato** | Accepted (storico) |
| **Contesto** | Oracle non ha tipo BOOLEAN nativo; legacy applicativo B.D. anni '90-2000 |
| **Decisione** | Flag booleani memorizzati come CHAR(1) con valori `'S'` (Sì) e `'N'` (No) |
| **Razionale** | ✅ Compatibilità con Oracle; ✅ Leggibilità nei report SQL; ✅ Uniformità con resto del DB SIAP |
| **Conseguenze** | ❌ Conversione manuale String↔boolean in ogni Action (317 occorrenze); ❌ Propenso a bug su valori null |

---

## 3. Pattern Decisions

### PD-01: Date Triplicate (Giorno/Mese/Anno) come Parametri HTTP

**Contesto**: I selettori di date nei form HTML degli anni 2000 erano 3 dropdown separati (giorno, mese, anno) per compatibilità con IE6.  
**Effetto**: 481 chiamate `getRequestDateParameter(CAMPO_ANNO, CAMPO_MESE, CAMPO_GIORNO)` — 3× il numero di costanti necessarie.  
**Azione consigliata**: nel refactoring, consolidare a un singolo date picker HTML5 + un solo parametro ISO-8601.

---

### PD-02: Prefisso `Ex` sui Metodi Business

Tutti i metodi dei Controller usano il prefisso `Ex` (Execute). Decisione stilistica uniformata nella piattaforma SIAP intera.  
**Da mantenere** durante refactoring per minimizzare impatto su codice chiamante.

---

### PD-03: Routing via Fully-Qualified Class Name

Il redirect Action-to-Action usa il FQCN come parametro HTTP:
```
?ACTION_FIELD=siap.sius.fascicolo.action.ActRicercaFascicolo
```
Questo crea un accoppiamento rigido tra JSP e nomi di classe Java.  
**Rischio**: un rename di classe senza aggiornare tutti i JSP causa errori runtime non rilevabili a compile time.

---

## 4. Trade-offs Analysis

| Decisione | Pro | Contro | Impatto Refactoring |
|-----------|-----|--------|---------------------|
| Monolith | Deploy semplice, transaction ACID | Non scalabile, non cloud-native | ALTO — richiede decomposizione modulare |
| F3B Framework | Uniformità SIAP | Vendor lock-in | CRITICO — richiede riscrittura layer web |
| SQL concatenato | Flessibilità | SQL injection, no query plan | ALTO — 3.190 punti da modificare |
| Session state | Performance | Fragile, non scalabile | MEDIO — introduce stateless API |
| Log4j 1.x | — | EOL, CVE attive | BASSO — solo configurazione |
| Un'Action per op. | SRP | Classi esplose (935) | BASSO — refactoring interno |

---

## 5. Alternative Solutions Considered (Retrospettiva)

Queste alternative **non** furono adottate al momento della progettazione (2002-2010), ma sono rilevanti per il piano di modernizzazione:

| Alternativa | Motivo non adottato | Rilevanza oggi |
|-------------|---------------------|----------------|
| Spring MVC + Spring DI | Non maturo/diffuso nella PA 2002; vincolo contrattuale Bull | ✅ Prima scelta per modernizzazione |
| JPA/Hibernate | Framework F3B aveva già DAO custom | ✅ Alternativa a SQL concatenato |
| REST/JSON API | Paradigma non prevalente 2002-2010 | ✅ Necessario per modernizzazione mobile/SPA |
| Microservices | Non esisteva il paradigma (2002) | ⚠️ Valutare se giustificato per dimensioni |
| MyBatis | Disponibile da 2010, non adottato | ✅ Meno invasivo di JPA per legacy DB |

---

## 6. Decision Context & Rationale

### Contesto storico (2002-2010)

SIUS è stato progettato e sviluppato in un'era in cui:
- Java EE 1.4/5 era lo standard enterprise
- Spring DI era "nuovo e non collaudato" per la PA italiana
- I browser dominanti erano Internet Explorer 6/7 (HTML 4.01, JS ES3)
- Il deployment on-premise su JBoss era l'unica opzione
- I contratti PA erano spesso vincolati a fornitori specifici (Bull/Atos)

### Vincoli che hanno guidato le scelte

1. **Contratto Bull/Atos**: imposto l'uso di F3B
2. **Oracle RDBMS**: contratto Ministero con Oracle
3. **Browser target IE6**: ha imposto HTML 4.01, date a 3 parametri, JavaScript ES3
4. **Team di sviluppo**: sviluppatori Java EE tradizionali, non DI/IoC
5. **Uniformità SIAP**: ogni scelta SIUS doveva essere coerente con SICO e SIEP già esistenti

### Implicazioni per la modernizzazione

La stratificazione di vincoli storici crea un **debito tecnico strutturale** che non può essere eliminato con refactoring incrementale puro. È necessaria una strategia di **strangler fig** o di **riscrittura modulare** guidata da priorità di rischio:

```
Priorità 1: Log4j → SLF4J (sicurezza immediata)
Priorità 2: SQL concatenato → prepared statement (sicurezza)
Priorità 3: Test coverage (enabling per tutto il resto)
Priorità 4: God classes decomposition (FascicoloSiusController, StampaController)
Priorità 5: Session state → stateless (scalabilità)
```

---

## Reference Documents

- **Deep Dive**: `docs/00_deep_dive.md`
- **Software Architecture**: `docs/06_software_architecture.md`
- **Code**: `docs/07_code.md`
- **Data**: `docs/08_data.md`

---

## Change Log

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | 2026-04-24 | IMPACT AI Agent | Prima versione, ADR ricostruiti da analisi codebase |