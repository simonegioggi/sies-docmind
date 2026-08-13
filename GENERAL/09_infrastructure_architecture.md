---
uniqueName: 09infrastructurearchitecture
displayName: "09 infrastructure architecture"
category: "GENERAL"
tags: []
---

# Infrastructure Architecture — Progetto SIUS

**Data**: 2026-04-24  
**Versione**: 1.0  
**Autori**: IMPACT AI Agent  
**Audience**: Architect, SysAdmin, DevOps, DGSIA

> **Nota**: L'infrastruttura fisica non è documentata nel codebase. Le informazioni qui riportate sono **dedotte** dai deployment descriptor, import package, configurazioni nel codice e dalla conoscenza del tipico stack PA italiana.  
> Valori marcati **[NON VALUTABILE]** richiedono verifica con DGSIA/team operativo.

---

## 1. Overview Infrastrutturale

SIUS è un sistema **on-premise**, deployato nella rete intranet del Ministero della Giustizia. Non vi è alcun elemento cloud rilevato nel codebase. Il sistema fa parte dell'EAR SIAP su JBoss Application Server, con Oracle RDBMS come backend.

```
┌─────────────────────────────────────────────────────────────────────────┐
│                   INTRANET GIUSTIZIA (rete PA)                          │
│                                                                         │
│  ┌──────────────┐     ┌──────────────────────────────────────────┐      │
│  │   Client     │     │         Application Tier                 │      │
│  │  (Browser)   │────▶│  JBoss EAP (Application Server)          │      │
│  │  IE/Firefox  │     │  ┌───────────────────────────────────┐   │      │
│  └──────────────┘     │  │  SIAP EAR                         │   │      │
│                        │  │  ├── SICO (base comune)           │   │      │
│  ┌──────────────┐     │  │  ├── SIEP (esecuzione penale)      │   │      │
│  │   Operatori  │     │  │  ├── SIUS (sorveglianza) ◀─ here   │   │      │
│  │   UDS (~165  │     │  │  └── altri moduli                  │   │      │
│  │   sedi)      │     │  └───────────────────────────────────┘   │      │
│  └──────────────┘     └──────────────────────────────────────────┘      │
│                                       │                                  │
│                                       ▼                                  │
│                         ┌────────────────────────┐                      │
│                         │   Oracle Database       │                      │
│                         │   (schema SIAP)         │                      │
│                         └────────────────────────┘                      │
│                                                                         │
│                         ┌────────────────────────┐                      │
│                         │   JMS Broker            │                      │
│                         │   (trasmissioni         │                      │
│                         │    inter-ufficio)        │                      │
│                         └────────────────────────┘                      │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Layer Applicativo

### 2.1 Application Server: JBoss EAP

| Attributo | Valore |
|-----------|--------|
| **Tipo** | JBoss EAP (RedHat/IBM) |
| **Versione** | [NON VALUTABILE] — probabile JBoss EAP 6.x/7.x in base a Java EE 6/7 compatibility |
| **Deployment unit** | EAR (Enterprise Archive) — SIAP EAR include SIUS come modulo |
| **Thread pool** | [NON VALUTABILE] — configurazione JBoss |
| **JNDI datasource** | Configurato su JBoss — accesso da DAO tramite JNDI lookup |
| **JMS** | JMS broker gestito da JBoss (HornetQ o ActiveMQ Artemis embedded) |

### 2.2 Struttura EAR

```
SIAP.ear
├── sico.jar        — base comune (soggetti, utenti, decodifiche)
├── siep.jar        — esecuzione penale
├── sius.jar / sius-web.war — sorveglianza (modulo analizzato)
├── jms-module.jar  — trasmissione messaggi
└── lib/
    ├── f3b-framework.jar     — framework proprietario Bull/Atos
    ├── oracle-jdbc.jar       — driver JDBC Oracle
    ├── log4j-1.x.jar        — logging (CRITICAL: obsoleto)
    └── [altre dipendenze]
```

### 2.3 Client

| Attributo | Valore |
|-----------|--------|
| **Tipo** | Browser web (thin client) |
| **Browser supportati** | [NON VALUTABILE] — probabilmente IE11/Edge Legacy (tipico PA italiana legacy) |
| **Accesso** | Tramite URL intranet (non accessibile da Internet) |
| **Autenticazione** | Tramite SICO/F3B (gestita a livello piattaforma SIAP) |

---

## 3. Layer Dati

### 3.1 Oracle Database

| Attributo | Valore |
|-----------|--------|
| **RDBMS** | Oracle Database |
| **Versione** | [NON VALUTABILE] — SQL Oracle-specific rilevato (ROWNUM, NVL, DECODE) |
| **Schema** | Schema condiviso SIAP (tabelle accessibili da tutti i moduli) |
| **Accesso** | JDBC diretto via JNDI datasource JBoss |
| **Connessioni** | Pool configurato su JBoss [NON VALUTABILE dimensionamento] |
| **Backup** | [NON VALUTABILE] — procedure operative esterne al codebase |
| **HA** | [NON VALUTABILE] — Oracle RAC possibile su infrastruttura Ministero |

### 3.2 Persistenza JMS

| Attributo | Valore |
|-----------|--------|
| **Broker** | JMS integrato in JBoss (HornetQ/ActiveMQ Artemis) |
| **Persistenza messaggi** | [NON VALUTABILE] — configurazione JBoss |
| **Pattern** | Point-to-point o publish-subscribe per trasmissioni inter-ufficio |

---

## 4. Topologia di Rete

### 4.1 Rete Intranet PA

Il sistema opera esclusivamente nella **rete intranet del Ministero della Giustizia** (RUPA — Rete Unitaria della Pubblica Amministrazione o SPC — Sistema Pubblico di Connettività).

```
Internet (pubblico)
        │
        │ (NO accesso)
        ✗
        │
   Firewall perimetrale
        │
   Intranet Giustizia (SPC/RUPA)
        │
   ┌────┴──────────────────────────────────────┐
   │  ~165 Uffici di Sorveglianza              │
   │  Postazioni client (browser)              │
   └───────────────────┬───────────────────────┘
                       │ HTTP/HTTPS (intranet)
                       ▼
            [Load Balancer? NON VALUTABILE]
                       │
            JBoss Application Server
                       │
            Oracle DB (JDBC)
                       │
            JMS Broker (messaggi)
```

### 4.2 Accesso Inter-ufficio

| Canale | Uso | Protocollo |
|--------|-----|------------|
| Browser HTTP | Operatori UDS locali | HTTP/HTTPS intranet |
| JMS messages | Trasmissione fascicoli tra UDS | JMS (asincrono) |
| DB Oracle | Accesso dati | JDBC/SQL |

---

## 5. Ambienti

Basandosi sulle convenzioni della piattaforma SIES correlata (da `readMe.txt` SIES), gli ambienti presumibili sono:

| Ambiente | Descrizione | URL Presumibile |
|----------|------------|-----------------|
| **SVILUPPO** | Ambiente locale sviluppatori | localhost:7001 o simile |
| **COLLAUDO** | Test funzionale/integrazione | rete interna test |
| **ESERCIZIO** | Produzione | URL intranet Ministero |

> ⚠️ La configurazione degli ambienti per SIUS non è nel repo analizzato (è nella piattaforma SIAP esterna).

---

## 6. Componenti Infrastrutturali — Matrice

| Componente | Tecnologia | Versione | Owner | Criticità |
|-----------|-----------|----------|-------|-----------|
| Application Server | JBoss EAP | [NON VALUTABILE] | DGSIA/Atos | ALTA |
| Database | Oracle RDBMS | [NON VALUTABILE] | DGSIA | ALTA |
| JMS Broker | HornetQ/ActiveMQ (in JBoss) | [NON VALUTABILE] | DGSIA | MEDIA |
| Logging | Log4j 1.x file-based | 1.2.x | App team | ALTA (CVE) |
| Rete | SPC/RUPA intranet | — | DGSIA/AgID | ALTA |
| Client | Browser (IE11/Edge) | — | Utenti PA | MEDIA |
| Load Balancer | [NON VALUTABILE] | — | DGSIA | ALTA |

---

## 7. Limitazioni Infrastrutturali Attuali

| Limitazione | Impatto |
|------------|---------|
| Nessuna containerizzazione (no Docker/K8s) | Deploy lento, dipendenze manuali, no scalabilità orizzontale |
| Sessione HTTP stateful | Impossibile scale-out senza sticky session sul load balancer |
| Log file-based su disco locale JBoss | Log non centralizzati, difficile correlazione inter-nodo |
| Nessuna observability (no APM, no metrics) | Diagnosi problemi solo a posteriori da log |
| Deploy manuale EAR | Rischio umano, downtime inevitabile |
| Oracle on-premise | Nessuna elasticità; scalabilità limitata da hardware fisico |

---

## 8. Target Infrastrutturale (per Scenario B — Re-Architecting)

> **Nota**: Non è una roadmap approvata, ma una raccomandazione IMPACT basata sulle best practice PA italiana e PagoPA/CloudPA.

| Componente | Stato Attuale | Target Raccomandato |
|-----------|--------------|---------------------|
| Deploy | JBoss EAR manuale | Docker + Kubernetes (o OpenShift) |
| Database | Oracle on-premise | Oracle mantenuto + connection pooling (HikariCP) |
| Logging | Log4j 1.x file | ELK Stack (Elasticsearch + Logstash + Kibana) o Grafana Loki |
| Monitoring | Assente | Prometheus + Grafana |
| CI/CD | Assente | GitLab CI / Jenkins pipeline |
| Source Control | SVN | Git (migrazione consigliata) |
| API Gateway | Assente | Kong / AWS API GW (per future API) |
| Auth | F3B SIAP | Keycloak / SPID integration |

---

## Reference Documents

- `docs/00_deep_dive.md` — Analisi tecnica completa
- `docs/10_deployment.md` — Deployment procedures
- `docs/06_software_architecture.md` — Architettura software

---

## Change Log

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | 2026-04-24 | IMPACT AI Agent | Prima versione — infrastruttura dedotta da analisi codebase e contesto PA |