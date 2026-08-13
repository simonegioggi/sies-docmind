---
uniqueName: 06softwarearchitecture
displayName: "06 software architecture"
category: "GENERAL"
tags: []
---

# Software Architecture - Progetto SIUS

**Data**: 2026-04-24  
**Versione**: 1.0  
**Autori**: IMPACT AI Agent  
**Audience**: Team tecnico, architetti, developer

---

## 1. Architecture Style & Patterns

### 1.1 Pattern Principale: Monolith Modulare a 4 Layer

SIUS adotta un'architettura **monolitica modulare** basata sul framework proprietario F3B (sviluppato da Bull/Atos per la piattaforma SIAP). Il pattern è un MVC tradizionale server-side con 4 layer distinti:

| Layer | Responsabilità | Tecnologia |
|-------|---------------|------------|
| **View (JSP)** | Rendering HTML, form input/output | JSP 2.x, HTML 4.01, JavaScript ES3 |
| **Action** | HTTP handler, validazione input, routing | F3B `ActionSius` → `ActionSiap` |
| **Controller** | Business logic, orchestrazione DAO, transazioni | F3B `SiapController`, interfaccia `I{Domain}` |
| **DAO** | SQL execution, mapping result set → model | F3B `SIAPSqlDAO`, SQL concatenato |

### 1.2 Service Locator Pattern

Nessun framework di dependency injection. L'accesso ai controller avviene tramite **Service Locator centralizzato** (`SIUSLookupRemote`):

```java
// Ogni action chiama:
IFascicoloSius ctrl = SIUSLookupRemote.getFascicoloSiusRemote();
// Internamente fa un lookup JNDI-like:
lRef = lookup("siap.sius.fascicolo.controller.FascicoloSiusController");
```

Il Service Locator conosce tutti i 40 controller del modulo SIUS e i controller dei moduli dipendenti (SICO, SIEP, JMS, Avvocatura).

### 1.3 Stateful Session Pattern

Il **fascicolo del procedimento** correntemente aperto è mantenuto in sessione HTTP:

```
Chiave sessione: "fascicoloSiusGP" (FascicoloGPModel)
Referenziata: 509 volte nel codebase
```

`FascicoloGPModel` è un **composite model** che aggrega:
- `FascicoloSiusModel` — dati fascicolo SIUS
- `GeneraleProcedimentoModel` — dati procedimento generale
- Sub-models di udienza, tenore, soggetto, etc.

---

## 2. Containers & Technology Choices

### 2.1 C4 Level 1 — System Context

```mermaid
C4Context
    title System Context — SIUS

    Person(operatore, "Operatore Tribunale/Sorveglianza", "Inserisce e gestisce procedimenti penali di sorveglianza")
    Person(avvocato, "Avvocato difensore", "Riceve notifiche, consulta procedimenti")

    System(sius, "SIUS", "Sistema Informativo Uffici di Sorveglianza\n(Modulo SIAP)")

    System_Ext(siap_sico, "SIAP-SICO", "Anagrafica soggetti, uffici, sicurezza utenti, decodifiche")
    System_Ext(siap_siep, "SIAP-SIEP", "Fascicolo penale esecuzione, sentenze")
    System_Ext(avvocatura, "SIAP-Avvocatura", "Portale avvocati, notifiche")
    System_Ext(oracle, "Oracle DB", "Database condiviso SIAP")
    System_Ext(jms_broker, "JMS Broker", "Messaggistica asincrona")

    Rel(operatore, sius, "Usa", "HTTP/Browser")
    Rel(sius, siap_sico, "Legge dati anagrafici e sicurezza", "Java in-process")
    Rel(sius, siap_siep, "Legge fascicolo SIEP e sentenze", "Java in-process")
    Rel(sius, avvocatura, "Invia notifiche avvisi", "JMS + Java in-process")
    Rel(sius, oracle, "Legge/Scrive dati", "JDBC")
    Rel(sius, jms_broker, "Invia messaggi asincroni", "JMS")
    Rel(avvocato, avvocatura, "Consulta", "HTTP/Browser")
```

### 2.2 C4 Level 2 — Container Diagram

```mermaid
C4Container
    title Container Diagram — SIUS nel contesto SIAP

    Person(operatore, "Operatore")

    Container_Boundary(siap_ear, "SIAP EAR (JBoss)") {
        Container(browser, "Browser", "HTML 4.01, JS ES3", "Client thin — form-based")
        Container(sius_war, "SIUS Module", "Java EE, F3B Framework\nJSP + Servlet-like Actions", "Logica di sorveglianza penale")
        Container(sico_mod, "SICO Module", "Java, F3B", "Anagrafica comune")
        Container(siep_mod, "SIEP Module", "Java, F3B", "Esecuzione penale")
        Container(avvoc_mod, "Avvocatura Module", "Java EE, Spring 4.x", "Portale avvocati")
    }

    ContainerDb(oracle_db, "Oracle DB", "Oracle RDBMS", "Schema condiviso SIAP")
    Container(jms, "JMS Broker", "JBoss Messaging / ActiveMQ", "Code messaggi")

    Rel(operatore, browser, "Usa")
    Rel(browser, sius_war, "HTTP POST/GET", "Form submit")
    Rel(sius_war, sico_mod, "Java method call", "Service Locator")
    Rel(sius_war, siep_mod, "Java method call", "Service Locator")
    Rel(sius_war, avvoc_mod, "Java method call + JMS", "Notifiche avvisi")
    Rel(sius_war, oracle_db, "JDBC", "SQL concatenato")
    Rel(sius_war, jms, "JMS send", "Trasmissioni asincrone")
```

---

## 3. Component Diagram (C4 Level 3 — SIUS Module)

```mermaid
graph TD
    subgraph SIUS_Module["SIUS Module (siap.sius.*)"]
        ActionSius["ActionSius\n(base class)\nsiap.sius.ActionSius"]

        subgraph Domains["49 Domain Modules"]
            Fascicolo["fascicolo\nIFascicoloSius"]
            Udienza["udienza\nIUdienza"]
            Tenore["tenore\nITenore"]
            TitoloEsecutivo["titoloesecutivo\nITitoloEsecutivo"]
            EsecuzioneMA["esecuzionemisuraalternativa\nIEsecuzioneMA"]
            Stampa["stampa\nIStampaSius"]
            Statistiche["statistiche\nIStatisticheSius"]
            OtherDomains["... altri 43 domini ..."]
        end

        LookupRemote["SIUSLookupRemote\n(Service Locator)"]

        subgraph Layer["Per ogni dominio"]
            Action["Act*.java\n(HTTP Handler)"]
            Controller["*Controller.java\n(Business Logic)"]
            DAO["*SqlDAO.java\n(Data Access)"]
            Model["*Model.java\n(DTO)"]
        end
    end

    Browser --> ActionSius
    ActionSius --> LookupRemote
    LookupRemote --> Controller
    Controller --> DAO
    DAO --> OracleDB[("Oracle DB")]
    Action --> Session[("HTTP Session\nfascicoloSiusGP")]

    subgraph External["Moduli Esterni"]
        SICO["SICO\nsiap.sico.*"]
        SIEP["SIEP\nsiap.siep.*"]
        Avvocatura_ext["Avvocatura\nit.eng.giustizia.*"]
        JMS_ext["JMS\nsiap.jms.*"]
    end

    LookupRemote --> SICO
    LookupRemote --> SIEP
    LookupRemote --> Avvocatura_ext
    LookupRemote --> JMS_ext
```

### 3.1 Distribuzione per tipo di componente

| Tipo | Conteggio | Pattern |
|------|-----------|---------|
| Action (HTTP handler) | 935 | Estende `ActionSius`, implementa `ICostanti*` |
| Controller (business) | 42 | Estende `SiapController`, implementa `I{Domain}` |
| DAO (data access) | 110 | Estende `SIAPSqlDAO`, SQL concatenato |
| Model (DTO) | 93 | POJO con getter/setter |
| Constants Interface | 50 | Costanti `CAMPO_*` per HTTP params |

### 3.2 Domini senza Controller dedicato (action-only)

10 domini non hanno un `controller/` locale ma utilizzano i controller di altri moduli:
`avvocatura`, `iscrizioneprocedimento`, `luogodetenzione`, `misuraalternativa`, `misuresicurezzarichiestaatti`, `penapecuniaria`, `presaincarico`, `produzioneatti`, `provvedimento`, `ulterioreistanzatenore`

---

## 4. Deployment Diagram

```mermaid
graph TD
    subgraph OnPremise["On-Premise Data Center (Ministero della Giustizia)"]
        subgraph JBossCluster["JBoss AS Cluster"]
            JBoss1["JBoss Node 1\nSIAP EAR\n(SIUS + SICO + SIEP + Avvocatura)"]
            JBoss2["JBoss Node N\nSIAP EAR (replica)"]
        end
        Oracle[("Oracle RAC\nSchema SIAP")]
        JMSBroker["JBoss Messaging\n/ ActiveMQ"]
        LB["Load Balancer / Reverse Proxy\n(Apache/Nginx — TBD)"]
    end

    Browser["Browser Utente\n(Internet Explorer / Chrome)"]
    Browser --> LB
    LB --> JBoss1
    LB --> JBoss2
    JBoss1 --> Oracle
    JBoss2 --> Oracle
    JBoss1 --> JMSBroker
    JBoss2 --> JMSBroker
```

> **Nota**: la configurazione infrastrutturale esatta è TBD — non sono presenti file di deployment o configurazione infrastrutturale in questo fragment.

---

## 5. Integration Architecture

### 5.1 Dipendenze In-Process (compile-time)

```mermaid
graph LR
    SIUS --> SICO["siap.sico\n(3.167 import)"]
    SIUS --> SIEP["siap.siep\n(871 import)"]
    SIUS --> ENG["it.eng.giustizia\n(5 import)"]
    SIUS --> F3B["f3b.*\n(Framework base)"]
    SICO --> F3B
    SIEP --> F3B
```

Dipendenze per numero di import:
- `siap.sico.*` — **3.167 import** (modulo più accoppiato)
- `siap.siep.*` — **871 import**
- `it.eng.giustizia.*` — **5 import** (integrazione Avvocatura recente)

### 5.2 Dipendenze Asincrone (JMS)

Il modulo `jms/` gestisce la trasmissione asincrona di eventi:
- **TrasmissioneJMSController** (`ITrasmissioneJMS`) — invio eventi a code JMS
- Usato per: notifiche al modulo Avvocatura, presaincarico, trasmissione atti
- Pattern: fire-and-forget (nessun reply handler rilevato)

### 5.3 Avvocatura Integration

Il sub-modulo `avvocatura/` (package `siap.sius.avvocatura.*`) coordina:
- `ICostantiAvvisiAvvocato`: tipi di evento (FISSAZIONE_UDIENZA, RINVIO_UDIENZA, EMISSIONE_DECRETO, etc.)
- `AvvisiAvvocatoDAO` / `AvvisiAvvocatoSqlDAO`: persistenza degli avvisi
- Notifiche triggered da azioni SIUS su udienze, decreti, ordinanze

---

## 6. Architectural Risks Mitigation

### 6.1 Rischi identificati e raccomandazioni

| Rischio | Gravità | Descrizione | Mitigazione Raccomandata |
|---------|---------|-------------|--------------------------|
| **Session single point of failure** | ALTA | `fascicoloSiusGP` in sessione HTTP: failover di nodo = perdita stato utente | Introdurre session replication JBoss o externalizzare stato (Redis/DB) |
| **SQL injection** | ALTA | 3.190 SQL costruiti per concatenazione, nessun prepared statement | Refactoring progressivo a parametri bind; scanner SAST immediato |
| **God classes** | ALTA | StampaController (6.470 LOC), FascicoloSiusController (5.427 LOC) | Decomposizione per responsabilità — almeno 3-5 classi ciascuna |
| **Zero test coverage** | ALTA | Nessun test automatico: ogni modifica è rischiosa | Introdurre JUnit per controller; mock DAO; partire dai componenti stabili |
| **Log4j 1.x CVE** | CRITICA | EOL 2015, CVE-2019-17571 | Upgrade a SLF4J + Logback immediatamente |
| **Coupling SICO altissimo** | MEDIA | 3.167 import: ogni cambio API SICO può rompere SIUS | Introdurre Anti-Corruption Layer o facade per SICO |
| **No health check** | MEDIA | Impossibile rilevare nodi in stato anomalo | Esporre endpoint `/health` JBoss o custom servlet |

---

## Reference Documents

- **Deep Dive Analysis**: `docs/00_deep_dive.md`

---

## Change Log

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | 2026-04-24 | IMPACT AI Agent | Creazione documento iniziale |