---
uniqueName: 12operationandsupport
displayName: "12 operation and support"
category: "GENERAL"
tags: []
---

# Operation and Support — Progetto SIUS

**Data**: 2026-04-24  
**Versione**: 1.0  
**Autori**: IMPACT AI Agent  
**Audience**: SysAdmin, Operations, Help Desk, Team di sviluppo

> **Nota**: Le procedure operative non sono documentate nel codebase. Questo documento è dedotto dall'analisi del codice (uso Log4j, gestione eccezioni, struttura JMS) e dalle best practice PA italiana.

---

## 1. Panoramica Operativa

SIUS è un sistema **mission-critical** per gli Uffici di Sorveglianza del Ministero della Giustizia. Un'interruzione blocca l'operatività di ~165 sedi. Le attività operative comprendono:
- Monitoraggio dell'application server JBoss
- Monitoraggio del database Oracle
- Gestione dei log (Log4j 1.x — file-based)
- Supporto agli utenti degli uffici
- Manutenzione pianificata

---

## 2. Logging

### 2.1 Configurazione Log4j

SIUS usa **Log4j 1.x** (versione 1.2.x — EOL 2015) con appender su file locale.

> ⚠️ **CRITICAL**: Log4j 1.x è vulnerabile a CVE-2019-17571 (deserialization RCE via socket appender). Aggiornare a Log4j 2.x / SLF4J urgentemente.

### 2.2 Pattern di Logging nel Codice

```java
// Pattern standard usato in SIUS (da analisi delle Action classes)
private static final Logger logger = Logger.getLogger(NomeClasse.class);

logger.info("Inizio operazione [nome]");
logger.error("Errore in [metodo]: " + ExceptionUtils.getStackTrace(e));
logger.debug("Parametro ricevuto: " + valore);
```

### 2.3 Posizione Log Files

```
[JBOSS_HOME]/standalone/log/
├── server.log          ← log principale JBoss
└── siap.log            ← log applicativo SIAP/SIUS (se configurato separatamente)
```

> **[NON VALUTABILE]**: il file `log4j.properties` / `log4j.xml` è nella configurazione SIAP esterna, non nel codebase SIUS analizzato.

### 2.4 Livelli di Log

| Livello | Uso nel codice SIUS |
|---------|-------------------|
| `INFO` | Inizio/fine operazioni principali, eventi di business |
| `ERROR` | Eccezioni catturate, errori DB, errori JMS |
| `DEBUG` | Parametri HTTP, valori intermedi (solo in sviluppo) |
| `WARN` | [NON VALUTABILE] — uso sporadico rilevato |

### 2.5 Analisi Log per Diagnostica

```bash
# Errori applicativi
grep "ERROR" [JBOSS_HOME]/standalone/log/server.log | tail -100

# Errori SQL/JDBC
grep "ORA-\|SQLException\|DAOException" server.log | tail -50

# Eccezioni SIUS
grep "SIUSException\|F3BException" server.log

# Performance: operazioni lente
grep "Elapsed\|tempo\|time" server.log | grep -E "[0-9]{4,}ms"

# JMS: errori trasmissione
grep "JMS\|trasmission\|MessaggioModel" server.log
```

---

## 3. Monitoraggio

> ⚠️ **Gap critico**: non è presente alcun sistema di monitoraggio nel codebase SIUS. Il monitoraggio è completamente affidato all'infrastruttura DGSIA (se configurata) e al log file manuale.

### 3.1 Check di Salute Correnti

| Check | Metodo | Come |
|-------|--------|------|
| JBoss running | OS process check | `ps aux | grep jboss` oppure `systemctl status jboss` |
| Applicazione deployata | Log JBoss | `grep "SIAP.*deployed" server.log` |
| DB Oracle raggiungibile | JDBC pool | Errori JDBC assenti in log |
| JMS funzionante | Log JMS | Assenza errori HornetQ/ActiveMQ |
| Spazio disco | OS | `df -h [JBOSS_HOME]/standalone/log/` |

### 3.2 Check da Eseguire Quotidianamente (Manuale)

```bash
# 1. Verifica JBoss running
systemctl status jboss-eap

# 2. Errori critici nelle ultime 24h
grep "ERROR" server.log | grep "$(date +%Y-%m-%d)" | wc -l

# 3. Eccezioni application-level
grep "SIUSException\|FATAL\|NullPointer" server.log | grep "$(date +%Y-%m-%d)"

# 4. Dimensione log (evitare disco pieno)
du -sh [JBOSS_HOME]/standalone/log/

# 5. Status JMS queue
# (accesso JBoss Management Console: http://localhost:9990)
```

### 3.3 Alert Critici (da implementare)

| Condizione | Azione |
|-----------|--------|
| JBoss non risponde | Restart immediato; notifica DGSIA |
| Disco > 85% (log) | Archiviazione/rotazione log urgente |
| Oracle unreachable | Verifica rete/DB; escalation DBA |
| Numero errori > soglia | Analisi log; potenziale rollback |

---

## 4. Gestione Configurazione

### 4.1 File di Configurazione Principali

| File | Posizione | Responsabilità |
|------|-----------|---------------|
| `standalone.xml` / `domain.xml` | `[JBOSS_HOME]/standalone/configuration/` | Datasource, JMS, security domain |
| `log4j.properties` / `log4j.xml` | In EAR SIAP (classpath) | Livelli log, appender, file output |
| `web.xml` | Nel WAR/JAR SIUS | Servlet mapping, session timeout |
| `jboss-web.xml` | Nel WAR/JAR SIUS | Context root, security domain |
| `jboss-deployment-structure.xml` | Nel WAR/JAR SIUS | Dipendenze moduli JBoss |

### 4.2 Gestione Password DB

> ⚠️ Le credenziali Oracle sono in `standalone.xml` in chiaro (plain text). Raccomandazione: usare JBoss Vault per cifrare le password.

```bash
# Cifratura con JBoss Vault (JBoss EAP 7+)
[JBOSS_HOME]/bin/vault.sh
# Poi in standalone.xml usare: ${VAULT::DS::password::1}
```

---

## 5. Backup e Restore

### 5.1 Cosa Fare Backup

| Asset | Frequenza | Metodo |
|-------|-----------|--------|
| **Oracle DB SIAP** | Daily + pre-deploy | Oracle RMAN o Data Pump Export |
| **JBoss EAR** | Pre ogni deploy | Copia file `SIAP.ear` |
| **Configurazione JBoss** | Ad ogni modifica | Copia `[JBOSS_HOME]/standalone/configuration/` |
| **Log files** | Weekly rotation | Compressione + archiviazione |

### 5.2 Procedura Restore Database

```bash
# Restore da Data Pump (richiedere a DBA Oracle DGSIA)
impdp siap/[PASSWORD] DUMPFILE=backup_[DATE].dmp \
      LOGFILE=restore.log TABLE_EXISTS_ACTION=REPLACE
```

### 5.3 Procedura Restore Applicazione

```bash
# 1. Stop JBoss
systemctl stop jboss-eap

# 2. Ripristina EAR dal backup
cp [BACKUP_DIR]/SIAP_[DATE].ear [JBOSS_HOME]/standalone/deployments/

# 3. Avvia JBoss
systemctl start jboss-eap

# 4. Verifica
tail -f [JBOSS_HOME]/standalone/log/server.log
```

---

## 6. Manutenzione Pianificata

### 6.1 Attività di Manutenzione Ordinaria

| Frequenza | Attività |
|-----------|---------|
| **Daily** | Verifica log errori, check spazio disco |
| **Weekly** | Archiviazione log vecchi, verifica backup DB |
| **Monthly** | Review errori ricorrenti, aggiornamento decodifiche |
| **Pre-release** | Backup completo, smoke test su collaudo, finestra di manutenzione |
| **Annuale** | Revisione sicurezza, verifica compliance GDPR |

### 6.2 Rotazione Log

```bash
# Rotazione manuale log JBoss
cd [JBOSS_HOME]/standalone/log/
gzip server.log
mv server.log.gz archive/server_$(date +%Y%m%d).log.gz
# JBoss creerà automaticamente un nuovo server.log
```

> **Raccomandazione**: Configurare `logrotate` su Linux per automazione.

---

## 7. Diagnostica e Troubleshooting

### 7.1 Problemi Comuni

#### JBoss non si avvia

```bash
# Verifica log di avvio
tail -200 [JBOSS_HOME]/standalone/log/server.log
# Cerca: "ERROR\|FATAL\|Exception\|caused by"

# Cause comuni:
# - Porta 8080 già occupata → kill processo o cambia porta
# - Datasource Oracle non raggiungibile → verifica Oracle
# - ClassNotFoundException → JAR mancante nel deployment
```

#### Utente non riesce a fare login

```bash
# Verifica sicurezza F3B
grep "authentication\|login\|SICO\|security" server.log | tail -50

# Cause comuni:
# - Session timeout scaduta
# - Problema LDAP/SICO (autenticazione SIAP)
# - Cookie problema browser
```

#### Errori "ORA-" nel log

```bash
# Errori Oracle comuni
grep "ORA-" server.log | sort | uniq -c | sort -rn | head -20

# ORA-01000: max open cursors → connection leak nel codice
# ORA-00942: table not found → schema DB diverso dall'atteso
# ORA-12514: TNS → Oracle non raggiungibile
# ORA-01017: invalid username/password → credenziali errate
```

#### JMS: messaggi in coda non processati

```bash
# Accedere alla JBoss Management Console
# http://[SERVER]:9990/console
# → Subsystems → Messaging → Queues → SIUSTrasmissioneQueue
# Verificare messaggi in coda, dead letter queue, errori consumer
```

### 7.2 Escalation Matrix

| Livello | Chi | Quando | Come |
|---------|-----|--------|------|
| **L1** | Help Desk PA | Problemi utente (login, navigazione) | Ticket sistema DGSIA |
| **L2** | Team SIUS / Fornitore | Errori applicativi, bug | Ticket + analisi log |
| **L3** | DGSIA IT Infrastruttura | JBoss down, Oracle issues, rete | Escalation urgente |
| **L3+** | DBA Oracle | Corruzione dati, performance DB | Escalation DGSIA |

---

## 8. Incident Management

### 8.1 Severity Levels

| Severity | Descrizione | SLA risposta | Esempio |
|----------|------------|-------------|---------|
| **P1 — Critico** | Sistema completamente non operativo | < 1 ora | JBoss down, Oracle irraggiungibile |
| **P2 — Alto** | Funzionalità core non funzionante | < 4 ore | Impossibile depositare ordinanze |
| **P3 — Medio** | Funzionalità secondaria degradata | < 1 giorno | Report statistici lenti |
| **P4 — Basso** | Anomalia minore | < 5 giorni | Messaggio di errore poco chiaro |

### 8.2 Procedura Incident P1

```
1. Identificazione: log JBoss o segnalazione utente
2. Notifica: DGSIA IT + Fornitore + Responsabile applicativo
3. Diagnosi: check log, check Oracle, check JBoss
4. Azione: restart JBoss / rollback / escalation
5. Verifica: smoke test post-recovery
6. Post-mortem: analisi causa root, azione correttiva
```

---

## 9. Gap Operativi Critici (da Colmare)

| Gap | Rischio | Priorità |
|-----|---------|----------|
| Log4j 1.x (CVE-2019-17571) | RCE remoto via socket appender | **CRITICO** |
| Nessun monitoring automatico | Outage rilevato solo da utenti | **ALTO** |
| Nessun health check endpoint | Impossibile load balancer health probe | **ALTO** |
| Log non centralizzati | Diagnosi lenta in caso di multi-nodo | **MEDIO** |
| Password DB in plain text | Rischio credenziali esposte | **ALTO** |
| Backup procedure non documentate | Rischio perdita dati in caso di incidente | **ALTO** |
| Nessun audit log applicativo | Non conformità GDPR | **CRITICO** |

---

## Reference Documents

- `docs/09_infrastructure_architecture.md` — Infrastruttura
- `docs/10_deployment.md` — Procedure di deploy
- `docs/03_non_functional_overview.md` — Requisiti non funzionali (security, monitoring)

---

## Change Log

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | 2026-04-24 | IMPACT AI Agent | Prima versione — procedure dedotte da analisi codebase |