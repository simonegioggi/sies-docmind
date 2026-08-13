---
uniqueName: 11developmentenvironment
displayName: "11 development environment"
category: "GENERAL"
tags: []
---

# Development Environment — Progetto SIUS

**Data**: 2026-04-24  
**Versione**: 1.0  
**Autori**: IMPACT AI Agent  
**Audience**: Sviluppatori, nuovi membri del team

> **Fonte**: Le istruzioni sono dedotte dalla struttura del codebase, dai file di configurazione Eclipse (`.classpath`, `.project`, `.settings/`), dalla guida `readMe.txt` del modulo SIES correlato e dalle convenzioni della piattaforma SIAP. Verificare con il team per eventuali aggiornamenti.

---

## 1. Panoramica Ambiente di Sviluppo

SIUS è sviluppato con un toolchain **tradizionale PA**:
- IDE: **Eclipse** (rilevato da `.project`, `.classpath`, `.settings/`)
- Build: **Maven** (nella piattaforma SIAP, non in SIUS isolato)
- Version Control: **SVN** (Subversion)
- Application Server locale: **JBoss EAP** o **Tomcat** (per test)
- Database: **Oracle** (client locale o accesso a server dev)
- Java: **1.8 (JDK 8)**

---

## 2. Prerequisiti

### 2.1 Software Obbligatorio

| Software | Versione | Download |
|----------|----------|----------|
| **JDK** | 1.8 (Java 8) | [Oracle JDK 8](https://www.oracle.com/java/technologies/downloads/#java8) |
| **Eclipse IDE** | 2020-06 o superiore (Java EE edition) | [Eclipse IDE for Enterprise Java](https://www.eclipse.org/downloads/) |
| **Subversion (SVN)** | 1.9+ | TortoiseSVN (Windows) o svn CLI |
| **JBoss EAP** | 6.x / 7.x (verificare con DGSIA) | RedHat Customer Portal |
| **Oracle JDBC Driver** | ojdbc8.jar (per Oracle 12c+) | Oracle Technology Network |
| **Oracle SQL*Plus** | (opzionale) | Oracle Instant Client |
| **Maven** | 3.6+ | [Maven Downloads](https://maven.apache.org/download.cgi) |

### 2.2 Accesso Richiesto

| Risorsa | Tipo accesso | Note |
|---------|-------------|------|
| SVN repository SIAP | Read/Write | Credenziali fornite da DGSIA |
| Oracle DB sviluppo | Read/Write su schema SIAP | Credenziali DBA DGSIA |
| JBoss EAP license | — | RedHat subscription (DGSIA) |
| Rete intranet Giustizia (se sviluppo remoto) | VPN | DGSIA IT |

---

## 3. Setup IDE Eclipse

### 3.1 Installazione Eclipse

1. Scaricare **Eclipse IDE for Enterprise Java and Web Developers**
2. Installare plugin aggiuntivi:
   - **Subclipse** (SVN integration): `Help → Eclipse Marketplace → "Subclipse"`
   - **JBoss Tools** (server integration): `Help → Eclipse Marketplace → "JBoss Tools"`

### 3.2 Configurazione JDK in Eclipse

```
Window → Preferences → Java → Installed JREs
→ Add → Standard VM → JRE home: [path JDK 8]
→ Imposta come default
```

### 3.3 Configurazione Encoding

> **CRITICO**: Il codebase ha 565/1294 file in ISO-8859-1. Configurare Eclipse correttamente per evitare corruzione dei sorgenti.

```
Window → Preferences → General → Workspace → Text file encoding → ISO-8859-1
```

> ⚠️ Alternativa: i file UTF-8 sono nella minoranza — verificare con il team quale encoding usare per i **nuovi** file.

---

## 4. Checkout da SVN

```bash
# Checkout della piattaforma SIAP (include SIUS)
svn checkout [SVN_URL_SIAP]/trunk ./siap-workspace

# Oppure del solo modulo SIUS
svn checkout [SVN_URL_SIAP]/trunk/sius ./sius

# Verifica
svn info
svn status
```

> **[NON VALUTABILE]**: URL SVN non presente nel codebase SIUS analizzato. Richiedere a DGSIA o al team.

### 4.1 Import in Eclipse

```
File → Import → Existing Maven Projects (se pom.xml disponibile)
oppure
File → Import → Existing Projects into Workspace → selezionare directory SIUS
```

---

## 5. Configurazione Build (Maven)

> SIUS non ha un `pom.xml` proprio — la build avviene come parte della piattaforma SIAP.

### 5.1 Build dell'intera piattaforma SIAP

```bash
# Dalla root della piattaforma SIAP (con pom.xml)
cd [SIAP_ROOT]

# Build standard
mvn clean install

# Build con profilo sviluppo locale
mvn clean install -P LOCALE

# Skip test (consigliato — zero test esistenti)
mvn clean install -DskipTests

# Build solo modulo SIUS (se modularizzato)
mvn clean install -pl sius -am -DskipTests
```

### 5.2 Profili Maven Rilevanti (da piattaforma SIES correlata)

| Profilo | Ambiente | Note |
|---------|----------|------|
| `LOCALE` | Sviluppo locale (localhost:7001) | Usare per sviluppo |
| `COLLAUDO` | Test | URL collaudo |
| `ESERCIZIO` | Produzione | Non usare in sviluppo |

---

## 6. Configurazione Application Server Locale

### 6.1 JBoss EAP (Setup Locale)

```bash
# Download JBoss EAP dal RedHat Customer Portal
# Estrarre in [JBOSS_HOME]

# Configurare datasource Oracle in standalone.xml
vi [JBOSS_HOME]/standalone/configuration/standalone.xml
# Aggiungere datasource SIAP (vedi docs/10_deployment.md)

# Copiare Oracle JDBC driver
cp ojdbc8.jar [JBOSS_HOME]/standalone/deployments/

# Avvio JBoss
[JBOSS_HOME]/bin/standalone.sh
# oppure su Windows:
[JBOSS_HOME]\bin\standalone.bat
```

### 6.2 Integrazione Eclipse + JBoss

```
Window → Show View → Servers
→ New Server → JBoss EAP [versione]
→ Server home directory: [JBOSS_HOME]
→ Add SIAP.ear al server
→ Start server (pulsante ▶)
```

---

## 7. Configurazione Database Locale

### 7.1 Opzione A: Oracle DB locale

```bash
# Installa Oracle XE (versione gratuita per sviluppo)
# Crea schema SIAP
sqlplus sys as sysdba
SQL> CREATE USER siap IDENTIFIED BY [PASSWORD];
SQL> GRANT CONNECT, RESOURCE TO siap;
SQL> EXIT

# Importa schema da dump (richiedere a DGSIA)
impdp siap/[PASSWORD] DUMPFILE=siap_dev.dmp LOGFILE=import.log
```

### 7.2 Opzione B: Connessione a Oracle dev server DGSIA

- Richiedere credenziali accesso al server Oracle di sviluppo a DGSIA
- Configurare `standalone.xml` con URL del server dev:
```xml
<connection-url>jdbc:oracle:thin:@[DEV_HOST]:[PORT]:[SID]</connection-url>
```

---

## 8. Struttura del Progetto nel Workspace

```
sius/
├── be/                          ← Sorgenti Java (business + DAO + model)
│   ├── ActionSius.java          ← Classe base di tutte le Action
│   ├── SIUSException.java       ← Eccezione applicativa
│   ├── fascicolo/               ← Modulo fascicolo (87 action)
│   ├── udienza/                 ← Modulo udienza (51 action)
│   ├── [49 altri moduli]/
│   └── util/                    ← Utility classes
│
├── fe/sius/                     ← View layer JSP (670 file)
│   ├── fascicolo/               ← View per modulo fascicolo
│   ├── udienza/                 ← View per modulo udienza
│   └── [altri moduli JSP]/
│
└── .settings/                   ← Configurazione Eclipse
    └── org.eclipse.core.resources.prefs
```

---

## 9. Flusso di Lavoro Sviluppo

### 9.1 Workflow quotidiano

```bash
# 1. Aggiorna dalla trunk SVN
svn update

# 2. Modifica il codice in Eclipse

# 3. Build
mvn clean install -DskipTests -P LOCALE

# 4. Deploy su JBoss locale (hot deploy o restart)
cp target/sius.jar [JBOSS_HOME]/standalone/deployments/

# 5. Test manuale nel browser
# http://localhost:7001/sius/

# 6. Commit su SVN (SOLO se tutto funziona)
svn commit -m "SIUS-XXX: descrizione modifica"
```

### 9.2 Convenzione commit SVN

```
[SIUS-TICKET]: [verbo] [cosa] in [dove]
Esempi:
  SIUS-123: Aggiunto campo dataScadenza in FascicoloModel
  SIUS-456: Corretto NullPointerException in ActRicercaFascicolo
```

---

## 10. Risoluzione Problemi Comuni

| Problema | Causa | Soluzione |
|---------|-------|-----------|
| Errori di encoding (caratteri accented) | Mismatch ISO-8859-1 / UTF-8 | Verificare `Window → Preferences → Workspace → Encoding` |
| ClassNotFoundException F3B | f3b-framework.jar non nel classpath | Aggiungere al `.classpath` Eclipse o al pom.xml |
| ORA-12514 (Oracle TNS) | Datasource mal configurato | Verificare URL JDBC in `standalone.xml` |
| JBoss non parte (porta 8080 occupata) | Conflitto porta | Cambiare `jboss.bind.address` o usare `-Djboss.socket.binding.port-offset=100` |
| `SIUSLookupRemote` ClassNotFoundException | Classe non trovata a runtime | Verificare che tutti i JAR SIAP siano nel classpath EAR |
| SVN conflict | Modifica concorrente stessa classe | `svn resolve --accept working [file]` + revisione manuale |

---

## 11. Note per Nuovi Sviluppatori

> **Onboarding checklist** per chi entra nel team SIUS:

- [ ] Installare JDK 8 e configurare `JAVA_HOME`
- [ ] Installare Eclipse Java EE Edition
- [ ] Installare Subclipse e JBoss Tools
- [ ] Richiedere accesso SVN repository SIAP a DGSIA
- [ ] Richiedere credenziali Oracle dev a DGSIA
- [ ] Checkout piattaforma SIAP da SVN
- [ ] Configurare JBoss EAP locale con datasource Oracle
- [ ] Fare build locale con `mvn clean install -DskipTests -P LOCALE`
- [ ] Verificare che JBoss parta correttamente con l'EAR SIAP
- [ ] Leggere `docs/00_deep_dive.md` per overview tecnica
- [ ] Leggere `docs/02_functional_overview.md` per overview funzionale
- [ ] Eseguire una ricerca fascicolo di test per smoke test dell'ambiente

---

## Reference Documents

- `docs/10_deployment.md` — Deploy in collaudo/produzione
- `docs/09_infrastructure_architecture.md` — Infrastruttura
- `docs/00_deep_dive.md` — Analisi tecnica

---

## Change Log

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | 2026-04-24 | IMPACT AI Agent | Prima versione — setup dedotto da Eclipse config e convenzioni SIAP |