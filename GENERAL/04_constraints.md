---
uniqueName: 04constraints
displayName: "04 constraints"
category: "GENERAL"
tags: []
---

# Constraints — Progetto SIUS

**Data**: 2026-04-24  
**Versione**: 1.0  
**Autori**: IMPACT AI Agent  
**Audience**: Architect, Project Manager, Team di sviluppo

---

## 1. Introduzione

Questo documento cataloga i vincoli che condizionano le scelte architetturali, tecnologiche e di progetto per il sistema SIUS. I vincoli sono distinti in **assoluti** (non negoziabili) e **forti** (molto difficili da modificare nel breve termine).

---

## 2. Vincoli Tecnologici

### 2.1 Framework Proprietario F3B

| Vincolo | Dettaglio |
|---------|-----------|
| **Tipo** | Assoluto — imposto dalla piattaforma SIAP |
| **Descrizione** | Tutto il business layer di SIUS estende `ActionSiap → ActionSius` del framework proprietario F3B (Bull/Atos). Le Action classes, il routing HTTP, la gestione della sessione e parte della sicurezza dipendono da F3B. |
| **Impatto** | Impossibile sostituire F3B senza riscrivere tutti e 935 gli Action handler. |
| **Classi chiave** | `f3b.web.IWebConstants`, `f3b.util.F3BException`, `f3b.util.DateUtils`, `f3b.log.LogF3B` |
| **Mitigazione** | Nessuna — per evolvere occorre portare SIUS fuori dalla piattaforma SIAP (scenario re-platforming/re-architecting) |

### 2.2 Oracle Database

| Vincolo | Dettaglio |
|---------|-----------|
| **Tipo** | Assoluto — infrastruttura Ministero della Giustizia |
| **Descrizione** | Il sistema usa Oracle RDBMS con SQL Oracle-specific (ROWNUM per paginazione, NVL, TO_DATE con formato Oracle, DECODE) in centinaia di query. |
| **Impatto** | Portabilità verso PostgreSQL/MySQL richiederebbe riscrittura massiva delle query |
| **Stima impatto migrazione** | ~3.000+ query da riscrivere (3.190 SQL dinamici identificati) |

### 2.3 Java EE / JBoss

| Vincolo | Dettaglio |
|---------|-----------|
| **Tipo** | Forte |
| **Descrizione** | Deployment come componente di un JBoss EAR (Enterprise Archive). Presenza di `jboss-deployment-structure.xml` e `jboss-web.xml` nel modulo siesEsecuzione correlato. |
| **Impatto** | Non deployabile su Tomcat standalone senza modifiche (dipendenze EAR condivise) |
| **Version** | JBoss EAP (versione specifica non determinabile dal sorgente SIUS) |

### 2.4 Java 1.8

| Vincolo | Dettaglio |
|---------|-----------|
| **Tipo** | Forte |
| **Descrizione** | Il codebase è compilato per Java 1.8 (target della piattaforma SIAP). Codice non usa lambda/stream — stile Java 5/6. |
| **Impatto** | Aggiornamento a Java 17/21 LTS possibile ma richiederebbe verifica compatibilità delle dipendenze F3B (chiuse) |

### 2.5 SVN per Version Control

| Vincolo | Dettaglio |
|---------|-----------|
| **Tipo** | Forte |
| **Descrizione** | Codebase gestito con Subversion (SVN). Nessuna migrazione a Git rilevata. |
| **Impatto** | Workflow CI/CD e branching molto più complesso rispetto a Git; difficile onboarding di sviluppatori moderni |

### 2.6 JSP per il Frontend

| Vincolo | Dettaglio |
|---------|-----------|
| **Tipo** | Forte (accoppiato a F3B) |
| **Descrizione** | 670 JSP con JSTL per il view layer. Nessun framework JS moderno (no React, Angular, Vue). |
| **Impatto** | UI non responsiva, nessuna SPA, ricarica pagina completa per ogni azione |

---

## 3. Vincoli Organizzativi / Risorse

### 3.1 Team di Sviluppo

| Vincolo | Dettaglio |
|---------|-----------|
| **Tipo** | Forte |
| **Descrizione** | Team interno DGSIA o fornitore (Atos/Eviden per F3B). Dimensione team non documentata nel codice. |
| **Ipotesi** | Team ridotto (pubblica amministrazione) — probabile 3-8 sviluppatori sul progetto |
| **Impatto** | Capacità di refactoring limitata; manutenzione correttiva prioritaria |

### 3.2 Commitment Budget PA

| Vincolo | Dettaglio |
|---------|-----------|
| **Tipo** | Forte |
| **Descrizione** | Investimenti in digitalizzazione PA soggetti a vincoli di bilancio, PNRR, CIG (Codice Identificativo Gara). |
| **Impatto** | Modernizzazione radicale richiede finanziamento dedicato (stima: 1.132-1.738 p-mese — vedi HOW_15/HOW_19) |

### 3.3 Coordinamento Inter-uffici

| Vincolo | Dettaglio |
|---------|-----------|
| **Tipo** | Forte |
| **Descrizione** | Modifiche al sistema impattano ~165 Uffici di Sorveglianza in Italia. Ogni release richiede coordinamento nazionale. |
| **Impatto** | Frequenza di release bassa; impossibile continuous delivery senza pianificazione estesa |

---

## 4. Vincoli Normativi e Legali

### 4.1 GDPR — Reg. EU 679/2016

| Vincolo | Dettaglio |
|---------|-----------|
| **Tipo** | Assoluto — obbligo di legge UE |
| **Descrizione** | I dati trattati da SIUS sono **dati giudiziari** (art. 9 e 10 GDPR) e dati sensibili dei condannati. Richiedono: pseudonimizzazione ove possibile, audit log degli accessi, diritto all'oblio (con eccezioni giustizia), minimizzazione. |
| **Stato attuale** | **Non conforme** — nessun audit log applicativo rilevato, nessuna pseudonimizzazione |
| **Rischio** | Sanzione fino al 4% del fatturato annuo (per PA: equivalente — art. 83 GDPR) |

### 4.2 D.Lgs. 196/2003 (Codice Privacy)

| Vincolo | Dettaglio |
|---------|-----------|
| **Tipo** | Assoluto |
| **Descrizione** | Codice in materia di protezione dei dati personali (con modifiche post-GDPR). Norme specifiche per trattamento dati in ambito giudiziario. |

### 4.3 CAD — D.Lgs. 82/2005

| Vincolo | Dettaglio |
|---------|-----------|
| **Tipo** | Assoluto — obbligo PA |
| **Descrizione** | Codice dell'Amministrazione Digitale. Obbliga le PA a garantire interoperabilità, accessibilità e conservazione digitale degli atti. |
| **Impatto** | Firma digitale degli atti giudiziari, formato documentale, conservazione a norma |

### 4.4 Accessibilità AGID — D.Lgs. 106/2018

| Vincolo | Dettaglio |
|---------|-----------|
| **Tipo** | Assoluto — obbligo PA |
| **Descrizione** | Le PA devono garantire accessibilità web (WCAG 2.1 livello AA) a tutti i sistemi informatici pubblici. |
| **Stato attuale** | **Non verificabile** — struttura JSP tabellare legacy, nessun attributo ARIA sistematico |
| **Rischio** | Procedimento AGID per non conformità + obbligo dichiarazione di accessibilità |

### 4.5 Ordinamento Penitenziario — L. 354/1975 e D.Lgs. 230/1999

| Vincolo | Dettaglio |
|---------|-----------|
| **Tipo** | Assoluto |
| **Descrizione** | Il sistema deve supportare i procedimenti definiti dall'ordinamento penitenziario: misure alternative, misure di sicurezza, procedura di sorveglianza. |
| **Impatto** | Ogni modifica funzionale richiede valutazione di conformità normativa con la magistratura di sorveglianza |

### 4.6 Legge 241/1990 — Procedimento Amministrativo

| Vincolo | Dettaglio |
|---------|-----------|
| **Tipo** | Assoluto |
| **Descrizione** | Obbligo di tracciabilità e motivazione degli atti amministrativi. |
| **Impatto** | Ogni provvedimento deve avere data certa, autore, motivazione — gestito dal sistema |

---

## 5. Vincoli di Integrazione

### 5.1 Dipendenze dalla Piattaforma SIAP

| Vincolo | Dettaglio |
|---------|-----------|
| **Tipo** | Assoluto (nel contesto attuale) |
| **Descrizione** | SIUS è un modulo dell'EAR SIAP. Condivide: schema Oracle SIAP, classpath JBoss EAR, sessione F3B, autenticazione SICO. |
| **Impatto** | Non deployabile come microservizio standalone senza refactoring massiccio. Ogni modifica alla piattaforma SIAP può impattare SIUS. |

### 5.2 Formato Messaggi JMS

| Vincolo | Dettaglio |
|---------|-----------|
| **Tipo** | Forte |
| **Descrizione** | Il formato dei messaggi JMS inter-ufficio è concordato con altri sistemi (procura, altri UDS). Modifiche richiedono coordinamento con tutti i sistemi riceventi. |

---

## 6. Vincoli di Ambiente

| Vincolo | Dettaglio |
|---------|-----------|
| Rete | Intranet giustizia — non accessibile da Internet pubblico |
| Datacenter | On-premise Ministero della Giustizia (no cloud pubblico) |
| Firewall / DMZ | [NON VALUTABILE] — dipende da infrastruttura |
| Ambiente di test | [NON VALUTABILE] — no CI/CD configurato nel repo |
| Finestre di manutenzione | [NON VALUTABILE] — accordo operativo non nel codebase |

---

## 7. Sintesi Vincoli Prioritari

| Priorità | Vincolo | Tipo | Impatto sulla Modernizzazione |
|----------|---------|------|------------------------------|
| 1 | Framework F3B proprietario | Assoluto | Blocca microservizi, API REST, DI |
| 2 | Oracle DB + SQL dinamico | Assoluto | Blocca cambio RDBMS |
| 3 | GDPR + audit log | Assoluto | Rischio legale alto |
| 4 | JBoss EAR deploy | Forte | Blocca containerizzazione immediata |
| 5 | SVN version control | Forte | Blocca CI/CD moderno |
| 6 | WCAG 2.1 (AGID) | Assoluto | Obbligo legale non rispettato |
| 7 | Java 1.8 | Forte | Incompatibilità futura JDK |

---

## Reference Documents

- `docs/00_deep_dive.md` — Analisi tecnica di base
- `docs/05_principles.md` — Principi architetturali
- `docs/19_modernization_estimation_spec.md` — Scenari di modernizzazione con stima costi

---

## Change Log

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | 2026-04-24 | IMPACT AI Agent | Prima versione — vincoli dedotti da analisi codebase e contesto normativo PA |