---
uniqueName: 10deployment
displayName: "10 deployment"
category: "GENERAL"
tags: []
---

# Deployment — Progetto SIUS

**Data**: 2026-04-24  
**Versione**: 1.0  
**Autori**: IMPACT AI Agent  
**Audience**: DevOps, SysAdmin, Team di sviluppo

> **Nota**: Le procedure di deployment non sono documentate nel codebase SIUS. Le informazioni sono dedotte dalla struttura del codice, dai deployment descriptor (jboss-deployment-structure.xml, jboss-web.xml) e dalle convenzioni della piattaforma SIAP.

---

## 1. Overview del Deployment

SIUS è un **modulo dell'EAR SIAP** deployato su **JBoss Application Server** in ambiente on-premise del Ministero della Giustizia. Non è un'applicazione deployabile autonomamente: dipende dalla piattaforma SIAP che fornisce framework F3B, schema Oracle, autenticazione e JMS.

**Deployment model**: Manuale — nessuna pipeline CI/CD rilevata nel codebase.

---

## 2. Artifact e Struttura di Build

### 2.1 Artifact Prodotto

| Tipo | Nome | Descrizione |
|------|------|-------------|
| **EAR** | `SIAP.ear` | Enterprise Archive — contiene tutti i moduli SIAP |
| **JAR/WAR** | `sius.jar` (o `sius-web.war`) | Modulo SIUS all'interno dell'EAR |
| **Build** | Maven (nella piattaforma SIAP) | SIUS non ha pom.xml proprio — incluso nella build SIAP |

### 2.2 Dipendenze Runtime

```
SIAP.ear
├── sius.jar               ← Modulo SIUS (questo sistema)
│   ├── be/**/*.class      ← Business layer compiled Java
│   └── fe/sius/**/*.jsp   ← View layer
├── sico.jar               ← Dipendenza runtime obbligatoria
├── siep.jar               ← Dipendenza runtime obbligatoria
├── f3b-framework.jar      ← Framework proprietario (OBBLIGATORIO)
├── oracle-jdbc.jar        ← Driver JDBC Oracle
└── lib/**                 ← Altre dipendenze condivise
```

---

## 3. Ambienti e Pipeline

### 3.1 Ambienti (dedotti dalla piattaforma SIES correlata)

```
SVN Repository
     │
     │ checkout + build Maven
     ▼
[SVILUPPO] → [COLLAUDO] → [ESERCIZIO (Produzione)]
  (dev)        (test)         (prod)
```

| Ambiente | Scopo | Accesso | Note |
|----------|-------|---------|------|
| **SVILUPPO** | Sviluppo locale sviluppatori | Sviluppatori | JBoss locale, Oracle locale/dev |
| **COLLAUDO** | Test funzionale e integrazione | Team QA, stakeholder | Oracle collaudo, JMS test |
| **ESERCIZIO** | Produzione | Utenti finali PA | Oracle produzione, HA richiesta |

### 3.2 Pipeline (Attuale — Manuale)

```
1. Sviluppatore fa checkout da SVN
2. Build locale con Maven (o ANT) nella piattaforma SIAP
3. Copia manuale del JAR/WAR nel deploy dir di JBoss
4. Restart JBoss Application Server (downtime)
5. Verifica manuale che l'applicazione sia partita (log JBoss)
```

**Punti di dolore**:
- ❌ Downtime durante ogni deploy (restart JBoss obbligatorio)
- ❌ Nessun rollback automatico — necessario ripristinare JAR precedente manualmente
- ❌ Nessun test automatico prima del deploy
- ❌ Nessuna notifica automatica di successo/fallimento deploy

---

## 4. Deployment Descriptor

### 4.1 `jboss-deployment-structure.xml` (da modulo SIES correlato)

Questo file controlla le dipendenze tra moduli nell'EAR e l'accesso al classloader JBoss.

```xml
<!-- Esempio tipico per modulo SIAP -->
<jboss-deployment-structure>
    <deployment>
        <dependencies>
            <module name="com.oracle.jdbc" />
            <module name="org.apache.log4j" />
        </dependencies>
    </deployment>
</jboss-deployment-structure>
```

**Funzione**: garantisce che SIUS acceda alle librerie condivise dell'EAR senza conflitti classloader.

### 4.2 `jboss-web.xml` (da modulo SIES correlato)

```xml
<!-- Esempio tipico -->
<jboss-web>
    <context-root>/sius</context-root>
    <security-domain>siap-security</security-domain>
</jboss-web>
```

**Funzione**: definisce il context root HTTP (`/sius`) e il security domain JBoss.

---

## 5. Configurazione Runtime

### 5.1 Datasource JDBC (configurato su JBoss, non nel codebase SIUS)

```xml
<!-- Da configurare nel JBoss standalone.xml / domain.xml -->
<datasource jndi-name="java:/SIAPDataSource" pool-name="SIAPPool">
    <connection-url>jdbc:oracle:thin:@[HOST]:[PORT]:[SID]</connection-url>
    <driver>oracle</driver>
    <pool>
        <min-pool-size>5</min-pool-size>
        <max-pool-size>50</max-pool-size>
    </pool>
    <security>
        <user-name>[USER]</user-name>
        <password>[PASSWORD]</password>
    </security>
</datasource>
```

### 5.2 JMS Queue (configurato su JBoss)

```xml
<!-- Esempio configurazione HornetQ/ActiveMQ per trasmissioni -->
<jms-queue name="SIUSTrasmissioneQueue">
    <entry name="java:/jms/SIUSTrasmissioneQueue" />
    <durable>true</durable>
</jms-queue>
```

---

## 6. Procedure di Deploy

### 6.1 Deploy in COLLAUDO

```bash
# 1. Build dell'EAR SIAP (con SIUS incluso)
cd [SIAP_ROOT]
mvn clean install -P COLLAUDO -DskipTests

# 2. Copia artifact
cp target/SIAP.ear [JBOSS_HOME]/standalone/deployments/

# 3. Restart JBoss (downtime!)
[JBOSS_HOME]/bin/standalone.sh restart
# oppure
service jboss restart

# 4. Verifica log
tail -f [JBOSS_HOME]/standalone/log/server.log | grep "SIUS\|ERROR"

# 5. Smoke test manuale
# Accedere al URL del collaudo e verificare login
```

### 6.2 Deploy in ESERCIZIO (Produzione)

```bash
# Stesso processo di COLLAUDO ma:
# 1. Approvazione formale (nota di autorizzazione)
# 2. Finestra di manutenzione (fuori orario lavorativo)
# 3. Backup EAR corrente PRIMA del deploy
cp [JBOSS_HOME]/standalone/deployments/SIAP.ear \
   [BACKUP_DIR]/SIAP_$(date +%Y%m%d_%H%M).ear

# 4. Deploy nuovo EAR
cp target/SIAP.ear [JBOSS_HOME]/standalone/deployments/

# 5. Restart JBoss
# 6. Verifica log
# 7. Smoke test su ambiente di produzione
```

---

## 7. Rollback

### 7.1 Procedura di Rollback Manuale

**Pre-requisito**: backup EAR precedente disponibile.

```bash
# 1. Stop applicazione
[JBOSS_HOME]/bin/standalone.sh stop

# 2. Ripristina EAR precedente
cp [BACKUP_DIR]/SIAP_[PREVIOUS_DATE].ear \
   [JBOSS_HOME]/standalone/deployments/SIAP.ear

# 3. Restart JBoss
[JBOSS_HOME]/bin/standalone.sh start

# 4. Verifica che l'applicazione sia operativa
tail -f [JBOSS_HOME]/standalone/log/server.log
```

**Tempo di rollback stimato**: 15-30 minuti (downtime incluso).

---

## 8. Health Check e Verifica Post-Deploy

Non è presente alcun health check endpoint nel codebase SIUS. Verifica post-deploy:

| Check | Metodo | Come |
|-------|--------|------|
| JBoss avviato | Log | `grep "WildFly\|JBoss.*started" server.log` |
| EAR deployato | Log | `grep "SIAP.*deployed" server.log` |
| DB connesso | Log | Nessun errore JDBC in log |
| Login funzionante | Manuale | Accedere alla URL e fare login |
| Funzionalità critica | Manuale | Test smoke (ricerca fascicolo) |

---

## 9. Alta Disponibilità (HA)

> **[NON VALUTABILE]** — Configurazione HA dipende dall'infrastruttura DGSIA, non dal codebase.

| Componente | Strategia HA | Vincolo |
|-----------|-------------|---------|
| JBoss | Cluster JBoss (opzionale) | Sessione stateful richiede sticky session |
| Oracle | Oracle RAC (on-premise) | Costo licenza, infrastruttura storage |
| JMS | JBoss cluster HA | Configurazione HornetQ cluster |
| Load Balancer | Apache httpd mod_cluster o hardware LB | Sticky session obbligatoria per sessioni SIUS |

**Vincolo critico**: la sessione HTTP stateful (oggetto `fascicoloSiusGP` in sessione) **impedisce** load balancing senza sticky session. In caso di failover di un nodo JBoss, le sessioni attive vengono perse.

---

## 10. Target Deployment (Scenario Modernizzazione)

| Aspetto | Attuale | Target Scenario A | Target Scenario B |
|---------|---------|-------------------|-------------------|
| Artifact | EAR monolitico | WAR + Docker | Docker image per microservizi |
| Deploy | Manuale | Scripted + CI/CD | CI/CD pipeline automatica |
| Rollback | Manuale (30 min) | Automatico (< 5 min) | Blue/Green o Canary |
| Downtime | Sì (restart JBoss) | Ridotto (rolling restart) | Zero downtime (K8s rolling) |
| Health check | Manuale | `/actuator/health` (Spring Boot) | `/health` + readiness/liveness probe |
| Ambienti | Dev/Coll/Prod | Stesso + staging automatico | Dev/QA/Staging/Prod con promozione automatica |

---

## Reference Documents

- `docs/09_infrastructure_architecture.md` — Architettura infrastruttura
- `docs/11_development_environment.md` — Setup ambiente sviluppo
- `docs/12_operation_and_support.md` — Operatività e supporto

---

## Change Log

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | 2026-04-24 | IMPACT AI Agent | Prima versione — deployment dedotto da deployment descriptor e convenzioni SIAP |