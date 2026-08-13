---
uniqueName: 19modernizationestimationspec
displayName: "19 modernization estimation spec"
category: "GENERAL"
tags: []
---

# Modernization Estimation — Progetto SIUS

**Data**: 2026-04-24  
**Versione**: 1.0  
**Autori**: IMPACT AI Agent  
**Audience**: CIO, Project Manager, Committenza, Architetti

> Questo documento applica il metodo **FP Backfiring + COCOMO II** per stimare l'effort di modernizzazione del sistema SIUS. I valori sono stime ingegneristiche basate su dati reali del codebase — non sostituiscono una stima dettagliata con project planning.

---

## Executive Summary

| Metrica | Valore |
|---------|--------|
| **Function Points As-Is** | **5.255 FP** |
| **SLOC totali analizzati** | 307.889 SLOC (Java + JSP + JS) |
| **Scenario A (Re-platforming)** | ~1.132 persone-mese / 30 mesi / team 38 |
| **Scenario B (Re-architecting)** | ~1.738 persone-mese / 34 mesi / team 51 |
| **Strangler Fig (6 mesi/5 pers)** | ~118 FP realizzabili (2,2% del totale) |

---

## 1. The Scanner — Input SLOC

### 1.1 Conteggio SLOC reale (equivalente cloc)

| Linguaggio | Files | Total Lines | Blank | Comment | **SLOC** | Fattore LOC/FP |
|------------|-------|------------|-------|---------|----------|----------------|
| Java | 1.294 | 230.762 | 34.498 | 29.399 | **166.865** | 53 |
| JSP | 670 | 163.841 | 16.715 | 6.402 | **140.724** | 67* |
| JavaScript | 2 | 345 | ~30 | ~15 | **300** | 47 |
| **TOTALE** | **1.966** | **394.948** | **51.243** | **35.816** | **307.889** | — |

> \* JSP trattati come PHP (server-side templating) per la tabella di backfiring. Fattore 67 LOC/FP.

### 1.2 Noise Reduction applicato

| Tipo esclusione | Applicato | Note |
|----------------|-----------|------|
| `node_modules`, `vendor`, `target` | N/A | Non presente nel repo |
| File minificati (`*.min.js`) | N/A | Non presenti |
| Codice generato (JAXB, XSD) | N/A | Non presente in SIUS |
| Commenti e blank lines | ✅ | Esclusi dal conteggio SLOC |
| Librerie vendor nel repo | ✅ | Nessuna trovata — conteggio pulito |

---

## 2. The Wizard — Discovery & Scoring

### Sezione A: Strategia & Architettura

| Domanda | Risposta selezionata | Score |
|---------|---------------------|-------|
| Q1. Salute codice attuale | **C. Spaghetti code, alta interdipendenza, tecnologie obsolete** | 1.30 |
| Q2. Obiettivo scalabilità | **A. Stabile (Scale-up verticale sufficiente)** — sistema PA intranet | 1.00 |
| Q3. Livello astrazione infrastrutturale | **B. Container / Kubernetes** — roadmap cloud PA | 1.15 |
| **Media Score** | | **1.15** |

> Media > 1.10 → **Scenario B (Re-architecting) suggerito**, ma Scenario A valutato come alternativa conservativa.

### Sezione B: Team Capabilities

| Domanda | Risposta | Moltiplicatore |
|---------|---------|---------------|
| Q4. Conoscenza dominio (giustizia, fascicoli) | B. Settore noto, non questo codice | 1.0 |
| Q5. Conoscenza tech target (Spring Boot, Angular) | B. Conoscenza scolastica / PoC | 1.1 |
| Q6. DevOps & Automation | C. Tutto manuale, nessun test | 1.20 |
| **PDR Multiplier totale** | | **1.32** |

### Sezione C: COCOMO II Drivers

| Driver | Scelta | Valore |
|--------|--------|--------|
| RELY (Affidabilità) | C. Alta — sistema giudiziario critico | 1.26 |
| CPLX (Complessità) | B→C (nominale per re-platform, alta per re-arch) | 1.00 / 1.34 |
| TEAM (Coesione) | B. Team appena formato | +0.05 |

---

## 3. The Engine — Calcoli

### 3.1 FP As-Is (Backfiring)

$$FP_{AsIs} = \frac{166.865}{53} + \frac{140.724}{67} + \frac{300}{47} = 3.148 + 2.100 + 6 = \mathbf{5.255 \text{ FP}}$$

---

### 3.2 Scenario A — Re-platforming (Conservativo)

**Ipotesi**: Containerizzazione dell'EAR esistente su Kubernetes + upgrade dipendenze (Log4j, Java). Nessuna riscrittura dell'architettura.

$$FP_{A} = 5.255 \times 1.05 = 5.518 \text{ FP}$$

**PDR Method (stima rapida):**

$$PDR_{Final} = 14 \times 1.0 \times 1.0 \times 1.20 = 16.8 \text{ h/FP}$$

$$Effort_{PDR} = 5.518 \times 16.8 = 92.701 \text{ ore} = \mathbf{579 \text{ persone-mese}}$$

**COCOMO II:**

$$KSLOC_{target} = \frac{5.518 \times 53}{1000} = 292 \text{ KSLOC}$$

$$E = 0.91 + 0.01 \times (3.00 + 3.00 + 3.72 + 0.05) = 1.008$$

$$EM = RELY \times CPLX = 1.26 \times 1.00 = 1.26$$

$$PM = 2.94 \times 292^{1.008} \times 1.26 = \mathbf{1.132 \text{ persone-mese}}$$

$$TDEV = 3.67 \times 1.132^{0.29} = \mathbf{30 \text{ mesi}}$$

$$\text{Team size ottimale} = 1.132 / 30 \approx \mathbf{38 \text{ persone}}$$

---

### 3.3 Scenario B — Re-architecting (Aggressivo)

**Ipotesi**: Riscrittura in Spring Boot (microservizi) + Angular frontend. Strangler Fig pattern modulare. Database Oracle mantenuto inizialmente, poi valutazione migrazione.

$$FP_{B} = 5.255 \times 1.30 = 6.832 \text{ FP}$$

**PDR Method:**

$$PDR_{Final} = 14 \times 1.0 \times 1.1 \times 1.20 = 18.5 \text{ h/FP}$$

$$Effort_{PDR} = 6.832 \times 18.5 = 126.392 \text{ ore} = \mathbf{789 \text{ persone-mese}}$$

**COCOMO II:**

$$KSLOC_{target} = \frac{6.832 \times 49}{1000} = 335 \text{ KSLOC}$$

$$EM = RELY \times CPLX = 1.26 \times 1.34 = 1.69$$

$$PM = 2.94 \times 335^{1.008} \times 1.69 = \mathbf{1.738 \text{ persone-mese}}$$

$$TDEV = 3.67 \times 1.738^{0.29} = \mathbf{34 \text{ mesi}}$$

$$\text{Team size ottimale} = 1.738 / 34 \approx \mathbf{51 \text{ persone}}$$

---

## 4. The Strategist — Dashboard Risultati

### Confronto Scenari

```
╔══════════════════════════════════════════════════════════════════╗
║  SCENARIO A: Re-platforming         SCENARIO B: Re-architecting  ║
╠══════════════════════════════════════════════════════════════════╣
║  FP Target:    5.518 FP             FP Target:    6.832 FP       ║
║  Effort PDR:   579 p-mese           Effort PDR:   789 p-mese     ║
║  Effort COCOMO: 1.132 p-mese        Effort COCOMO: 1.738 p-mese  ║
║  Durata TDEV:  30 mesi              Durata TDEV:  34 mesi        ║
║  Team ottimale: 38 persone          Team ottimale: 51 persone    ║
╠══════════════════════════════════════════════════════════════════╣
║  ✅ Costo minore                    ✅ Scalabilità futura         ║
║  ✅ Tempi più brevi                 ✅ Manutenibilità a lungo T.  ║
║  ✅ Rischio ridotto                 ✅ Cloud-native ready          ║
║  ❌ Debito tecnico rimane           ❌ Costo elevato               ║
║  ❌ Framework F3B ancora presente   ❌ Tempi lunghi                ║
║  ❌ Non cloud-native                ❌ Rischio delivery            ║
╚══════════════════════════════════════════════════════════════════╝
```

### Range di Confidenza

Le stime COCOMO II hanno un range di confidenza del **±30%** (industria standard):

| Scenario | PM (pessimistico) | PM (centrale) | PM (ottimistico) |
|----------|------------------|--------------|-----------------|
| A | 1.472 | 1.132 | 793 |
| B | 2.259 | 1.738 | 1.217 |

---

## 5. Strangler Fig Roadmap

### Budget Analysis: 5 persone × 6 mesi

```
Budget disponibile:    5 persone × 6 mesi = 30 persone-mese
FP/persone-mese (B):  6.832 FP / 1.738 p-mese ≈ 3.9 FP/p-mese
FP realizzabili:       30 × 3.9 ≈ 118 FP (2.2% del sistema)
```

### Moduli ordinati per coupling (dal meno al più accoppiato)

Priorità di migrazione per la Strangler Fig:

| Priorità | Modulo | FP stimati | Coupling | Migrabile per primo? |
|---------|--------|-----------|---------|---------------------|
| 1 | `penapecuniaria` | ~35 FP | Basso | ✅ Sì |
| 2 | `collaboratore` | ~25 FP | Basso | ✅ Sì |
| 3 | `esperto` | ~28 FP | Basso | ✅ Sì |
| 4 | `luogodetenzione` | ~20 FP | Basso | ✅ Sì |
| 5 | `remissionedebito` | ~30 FP | Basso-Medio | ✅ Sì |
| — | `fascicolo` | ~530 FP | ALTISSIMO | ❌ Ultimo |
| — | `stampa` | ~390 FP | ALTISSIMO | ❌ Ultimo |
| — | `richiestaatti` | ~1.050 FP | ALTO | ❌ Medio-lungo |

> **Con budget 6 mesi/5 persone** si possono migrare i primi **3-4 moduli** (penapecuniaria, collaboratore, esperto, luogodetenzione = ~108 FP). Il core (fascicolo + stampa) rimane in F3B durante le fasi iniziali.

---

## 6. Raccomandazione Strategica

### Approccio consigliato: **Scenario B (Strangler Fig) con Fase 0 obbligatoria**

```
FASE 0 — Prerequisiti (3 mesi, team 3-4)
├── Migrazione Log4j → SLF4J
├── SQL PreparedStatement (DAO critici)
├── Test di caratterizzazione E2E (Playwright)
├── Encoding ISO-8859-1 → UTF-8
└── CI/CD pipeline base (build + lint)

FASE 1 — Quick Wins (6 mesi, team 5)
├── Moduli a basso coupling (penapecuniaria, collaboratore, esperto)
├── Spring Boot + REST API per ogni modulo
├── Angular stub per le view corrispondenti
└── ~118 FP (2.2% del sistema)

FASE 2 — Moduli Medi (12 mesi, team 10)
├── Moduli medi (udienza, provvedimento, scadenzario)
├── ~500-700 FP (10-13% del sistema)
└── Old JSP/F3B delegano al nuovo servizio (Strangler pattern)

FASE 3 — Core (18-24 mesi, team 20+)
├── fascicolo, stampa, richiestaatti (i più grandi e accoppiati)
├── ~2.000+ FP (40% del sistema)
└── Decomposizione God classes obbligatoria prima

FASE 4 — Completamento (34 mesi totali, team ottimale 51)
└── Decommissioning EAR F3B legacy
```

### Fattori di rischio per la stima

| Rischio | Probabilità | Impatto | Contingenza |
|---------|------------|---------|-------------|
| Scoperta logica business nascosta nel F3B | Alta | +20% effort | +200 p-mese |
| Team turnover durante 34 mesi | Media | +15% effort | +260 p-mese |
| Integrazione Oracle → Cloud complessa | Media | +10% effort | +174 p-mese |
| Scope creep (nuove funzionalità durante migrazione) | Alta | +25% effort | +435 p-mese |
| **Range pessimistico totale** | | **+70%** | **+2.216 p-mese** |

---

## 7. Costo Economico Indicativo

Usando una tariffa media di **500 €/gg** (team misto insourcing/outsourcing PA italiana):

| Scenario | Persone-mese | Gg/persona (~20 gg/mese) | Costo indicativo |
|---------|-------------|--------------------------|-----------------|
| A - Re-platforming | 1.132 | 22.640 | **~11,3 M€** |
| B - Re-architecting | 1.738 | 34.760 | **~17,4 M€** |
| B - Pessimistico (+70%) | 2.955 | 59.100 | **~29,5 M€** |
| Fase 0 + Fase 1 sola | ~50 | 1.000 | **~500.000 €** |

> ⚠️ Questi valori sono **indicativi** (±50%). La stima definitiva richiede analisi dettagliata con project planning, WBS, e offerte di mercato reali.

---

## Reference Documents

- **Deep Dive**: `docs/00_deep_dive.md`
- **Software Architecture**: `docs/06_software_architecture.md`
- **Metrics**: `docs/14_metrics.md`
- **Decision Log**: `docs/13_decision_log.md`
- **Antipattern Assessment**: `docs/18_antipattern_deep_dive.md`
- **Backend Assessment**: `docs/17_backend_deep_assessment.md`
- **Frontend Assessment**: `docs/16_frontend_deep_assessment.md`

---

## Change Log

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | 2026-04-24 | IMPACT AI Agent | Prima versione — FP Backfiring + COCOMO II |