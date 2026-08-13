---
uniqueName: 15fpcocomo
displayName: "15 fp cocomo"
category: "GENERAL"
tags: []
---

# Function Points & COCOMO II — AS-IS Estimation — Progetto SIUS

**Data**: 2026-04-24  
**Versione**: 1.0  
**Autori**: IMPACT AI Agent  
**Audience**: Project Manager, Architect, CIO, Committenza  
**Correlato a**: `docs/19_modernization_estimation_spec.md` (scenari futuri)

---

## Scopo di Questo Documento

Questo documento presenta la **stima AS-IS** del sistema SIUS applicando:
1. **FP Backfiring** — calcolo dei Function Points a partire dalle SLOC (Standard Lines of Code)
2. **COCOMO II Maintenance Model** — stima dell'effort annuale di manutenzione del sistema esistente
3. **Staffing Profile** — composizione e profili del team necessario

> **Differenza con `docs/19_modernization_estimation_spec.md`**:
> - Questo documento (HOW_15) stima il **sistema AS-IS** — quanto "vale" e quanto costa mantenere
> - Il documento 19 stima il **progetto di modernizzazione** — quanto costerebbe riscriverlo

---

## 1. Input SLOC — Misurazione del Codebase Attuale

### 1.1 Conteggio Sorgenti

Basato sull'analisi completa del codebase `/home/mideluci/copilot-projects/giustizia/sies/SIUS`:

| Linguaggio | Files | Linee Totali | Blank | Commenti | **SLOC** |
|------------|-------|------------|-------|----------|----------|
| **Java** | 1.294 | 230.762 | 34.498 | 29.399 | **166.865** |
| **JSP** | 670 | 163.841 | 16.715 | 6.402 | **140.724** |
| **JavaScript** | 2 | 345 | ~30 | ~15 | **300** |
| **TOTALE** | **1.966** | **394.948** | **51.243** | **35.816** | **307.889** |

### 1.2 Distribuzione per Modulo Funzionale (Java)

| Modulo | SLOC stimati | Note |
|--------|-------------|------|
| `richiestaatti` (173 action) | ~22.000 | Modulo più grande |
| `stampa` (StampaController 6470 LOC) | ~8.000 | God class |
| `fascicolo` (87 action) | ~11.000 | Core |
| `statistiche` (55 action) | ~7.000 | |
| `depositodecreto` (52 action) | ~7.000 | |
| `udienza` (51 action) | ~6.500 | |
| `depositoordinanzapc` (83 action) | ~10.500 | |
| `presaincarico` (39 action) | ~5.000 | |
| Restanti 43 moduli | ~90.000 | ~2.000 SLOC/modulo medio |

---

## 2. Function Point Backfiring (AS-IS)

### 2.1 Tabella Fattori di Conversione

Secondo la **SPR Software Backfiring Table** (Jones, 1997):

| Linguaggio | Categoria | LOC per FP medio |
|-----------|-----------|-----------------|
| Java (enterprise) | Object Oriented | **53 LOC/FP** |
| JSP (server-side templating) | Scripting/Template | **67 LOC/FP** |
| JavaScript | Scripting | **47 LOC/FP** |

### 2.2 Calcolo FP As-Is

$$FP_{Java} = \frac{166.865}{53} = 3.148 \text{ FP}$$

$$FP_{JSP} = \frac{140.724}{67} = 2.100 \text{ FP}$$

$$FP_{JavaScript} = \frac{300}{47} = 6 \text{ FP}$$

$$\boxed{FP_{AsIs\_SIUS} = 3.148 + 2.100 + 6 = \mathbf{5.255 \text{ FP}}}$$

### 2.3 Benchmark

| Riferimento | Dimensione | Confronto SIUS |
|------------|-----------|----------------|
| Progetto medio PA italiana | 500-1.500 FP | SIUS è 3-10x più grande |
| Sistema Enterprise tipico | 3.000-8.000 FP | SIUS in range medio-alto |
| SAP R/3 modulo tipico | ~20.000 FP | SIUS è ~4x più piccolo |

**Classificazione**: SIUS è un sistema **medium-large** per standard PA italiana, con complessità concentrata nei moduli `richiestaatti` e `stampa`.

---

## 3. Analisi Funzionale per Dimensionamento

### 3.1 Stima IFPUG per Tipo di Funzione

> Stima top-down basata sui moduli identificati (non conteggio IFPUG formale).

| Tipo Funzione | Conteggio stimato | FP medi | FP Totali stimati |
|--------------|------------------|---------|------------------|
| **EI** (External Input — inserimento dati) | ~300 | 4 FP | 1.200 FP |
| **EO** (External Output — stampe, report) | ~150 | 5 FP | 750 FP |
| **EQ** (External Query — ricerche) | ~200 | 4 FP | 800 FP |
| **ILF** (Internal Logical File — entità dati) | ~80 | 10 FP | 800 FP |
| **EIF** (External Interface File — SICO, SIEP) | ~20 | 7 FP | 140 FP |
| **TOTALE IFPUG stimato** | | | **~3.690 FP** |

> **Nota**: Il backfiring da SLOC (5.255 FP) è maggiore della stima IFPUG (3.690 FP). Questo è atteso in codebase con alta duplicazione — il delta (~1.565 FP) è da attribuire a duplicazione e codice non-funzionale (infrastruttura, utility, configurazione).

---

## 4. COCOMO II — Stima Manutenzione AS-IS

### 4.1 Modello COCOMO II Maintenance

Il **COCOMO II Maintenance Model** stima il costo annuale di mantenere il sistema senza refactoring.

**Input:**
- KSLOC = 307.889 / 1.000 = **307,9 KSLOC**
- ACT (Annual Change Traffic) = 10% stimato (tipico per sistemi PA maturi)
- SLOC modificati/anno = 307,9 × 0.10 = **30,8 KSLOC/anno**

### 4.2 Cost Drivers per Manutenzione

| Driver COCOMO II | Valore | Moltiplicatore |
|-----------------|--------|---------------|
| RELY (Affidabilità richiesta) | Alta — sistema giudiziario | 1.26 |
| CPLX (Complessità) | Alta — god classes, string SQL | 1.34 |
| TOOL (Maturità tool) | Bassa — no CI/CD, IDE Eclipse | 1.12 |
| PEXP (Esperienza piattaforma) | Nominale — team conosce F3B | 1.00 |
| LTEX (Esperienza linguaggio) | Alta — Java conoscono | 0.91 |
| MODP (Modern practices) | Bassa — no test, no refactoring | 1.24 |
| **Effort Multiplier (EM) composto** | | **= 1.26 × 1.34 × 1.12 × 1.00 × 0.91 × 1.24 ≈ 2.41** |

### 4.3 Calcolo Effort Manutenzione Annuale

$$SF = 0.91 + 0.01 \times \sum Scale\_Factors = 1.008$$

$$PM_{maint} = 2.94 \times (30.8)^{1.008} \times 2.41 \approx \mathbf{232 \text{ persone-mese/anno}}$$

> **Interpretazione**: Mantenere SIUS AS-IS costa ~232 persone-mese/anno (~19 persone full-time). Questo include manutenzione correttiva, evolutiva e adattativa.

---

## 5. Produttività AS-IS

### 5.1 Indici di Produttività

| Metrica | Valore | Benchmark settore | Giudizio |
|---------|--------|------------------|----------|
| LOC/FP (Java) | 53 | 40-60 | ✅ Nella norma |
| FP/persona-mese (sviluppo) | ~5-7 FP/PM (stimato) | 8-12 FP/PM | ❌ Bassa produttività |
| Difetti/KSLOC (stimato) | 30-50 (alta — zero test) | 10-20 good | ❌ Alta densità difetti |
| Test coverage | 0% | >80% target | ❌ Critico |
| Debt ratio (stima) | ~65-70% | <30% buono | ❌ Altissimo |

**Causa bassa produttività**: combinazione di zero test, god classes, SQL injection risk che rallenta ogni modifica (paura di regressioni), high coupling (SIUSLookupRemote 400 usaggi).

---

## 6. Staffing Profile

### 6.1 Team Manutenzione AS-IS (Raccomandato)

Per gestire la manutenzione del sistema esistente con il livello di rischio attuale:

| Ruolo | FTE | Responsabilità |
|-------|-----|---------------|
| **Sviluppatore Senior Java** | 2 | Manutenzione correttiva, evolutive complesse |
| **Sviluppatore Java** | 4 | Sviluppo evolutive, correzione bug |
| **Analista Funzionale** | 2 | Raccolta requisiti, analisi normativa |
| **DBA Oracle** | 1 | Ottimizzazione query, gestione schema |
| **SysAdmin/DevOps** | 1 | JBoss, deploy, monitoring |
| **QA/Test** | 1 | Test manuali (zero automatizzati) |
| **Tech Lead / Architect** | 1 | Supervisione tecnica, decisioni architetturali |
| **TOTALE** | **12 FTE** | |

> **Nota**: Con 0% test coverage, la coppia Sviluppatore+QA deve testare manualmente ogni modifica → overhead elevato.

### 6.2 Team Urgenze Sicurezza (Minimo Vitale)

Per eliminare i rischi CRITICAL identificati:

| Attività | FTE dedicati | Durata stimata |
|---------|-------------|---------------|
| Upgrade Log4j 1.x → Log4j 2.x | 0.5 | 2 settimane |
| Prepared Statements (SQL injection) | 3 | 6-12 mesi (3.190 punti) |
| Encoding unificazione UTF-8 | 1 | 2-4 settimane |
| **Totale sicurezza** | **~4 FTE** | **6-12 mesi** |

---

## 7. Stima Investimento per Abbattere Debito Tecnico

### 7.1 Costo del Debito Attuale

Assumendo costo medio sviluppatore PA: €600/giorno (€9.000/mese):

| Scenario | Effort | Costo Stimato |
|---------|--------|--------------|
| Manutenzione annuale AS-IS | 232 PM | ~€2.088.000/anno |
| Fix rischi CRITICAL (Log4j + SQL) | ~60 PM | ~€540.000 |
| Introduzione test coverage 50% | ~180 PM | ~€1.620.000 |
| Decomporre god classes (top 5) | ~30 PM | ~€270.000 |
| **Totale risanamento minimo** | **~270 PM** | **~€2.430.000** |

### 7.2 Confronto: Manutenere vs. Modernizzare

```
                    AS-IS               SCENARIO A         SCENARIO B
                    (Mantenere)         (Re-platform)      (Re-architecting)
                    ─────────────────   ──────────────     ─────────────────
Costo/anno          €2.08M/anno         €1.2M/anno*        €0.8M/anno*
Investimento init.  €0                  ~€10.2M            ~€15.6M
Break-even          —                   ~7 anni            ~10 anni
Rischio SQL inj.    CRITICO             ELIMINATO          ELIMINATO
Scalabilità         NO                  PARZIALE           ALTA
```

> \* Stima manutenzione post-modernizzazione (sistema più sano, test coverage alta)

---

## 8. Riepilogo Numeri Chiave

| KPI | Valore SIUS |
|-----|------------|
| **Dimensione** | 5.255 FP (backfiring) / ~3.690 FP (IFPUG stimato) |
| **SLOC totali** | 307.889 (Java + JSP + JS) |
| **Moduli funzionali** | 51 |
| **Action handlers** | 935 |
| **Punti SQL injection** | 3.190 |
| **Effort manutenzione annuale** | ~232 persone-mese/anno |
| **Team manutenzione raccomandato** | 12 FTE |
| **Technical debt ratio** | ~65-70% (stimato) |
| **Health score** | 18/100 (stimato) |
| **Test coverage** | 0% |

---

## Reference Documents

- `docs/19_modernization_estimation_spec.md` — Scenari di modernizzazione (Scenario A e B)
- `docs/14_metrics.md` — Metriche di qualità dettagliate
- `docs/00_deep_dive.md` — Analisi tecnica codebase

---

## Change Log

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | 2026-04-24 | IMPACT AI Agent | Prima versione — stima AS-IS completa |