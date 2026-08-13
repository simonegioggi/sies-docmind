---
uniqueName: 12-cost-matrix
displayName: "WBS Cost Matrix \u2014 Stima costi per Work Package"
category: "WBS_DRAFT"
tags: []
---

# cost_matrix

## riepilogo

| metric | value |
|---|---|
| total_work_packages | 16 |
| total_activities | 53 |
| stima_totale_gg_con_test | 48.5 |
| stima_totale_gg_implementativa | 37.5 |
| stima_totale_ore | 300 |
| team_velocity | Medium (8h/GG) |
| confronto_fp_sizing | 34.6 GG (delta: +2.9 GG / +8.4%) |
| fasi_analizzate | 4 |

> **Legenda T-shirt sizing** → man-days (Medium team, 8h/GG):
> XS = 0.5 GG | S = 1 GG | M = 3 GG | L = 5 GG | XL = 8 GG

## fattori_di_complessità

| Fattore | Descrizione |
|---|---|
| func_cx | Complessità funzionale (logica di business, regole, condizioni) |
| tech_cx | Complessità tecnica (stack, pattern, algoritmi) |
| integ_cx | Complessità di integrazione (componenti coinvolti, dipendenze) |
| data_cx | Complessità dati (entità, trasformazioni, migrazione) |
| risk | Rischio (incertezza, reversibilità, impatto su codice esistente) |

Scala per ciascun fattore: **1** (bassa) | **2** (media) | **3** (alta)

## matrice_costi_per_wp

| WP ID | Nome | size | func_cx | tech_cx | integ_cx | data_cx | risk | GG |
|---|---|---|---|---|---|---|---|---|
| F1.D1.WP1 | Preparare ambiente di sviluppo | S | 1 | 2 | 2 | 1 | 2 | 1.0 |
| F1.D1.WP2 | Adeguare schema Oracle SIES | M | 2 | 2 | 2 | 3 | 2 | 3.0 |
| F1.D1.WP3 | Struttura modulo Java CF isolato | M | 2 | 2 | 1 | 2 | 1 | 3.0 |
| **F1 subtotal** | | | | | | | | **7.0** |
| F2.D1.WP1 | Algoritmo ministeriale CF atteso | XL | 3 | 3 | 1 | 1 | 2 | 8.0 |
| F2.D1.WP2 | Verifica formale + confronto congruenza | L | 3 | 2 | 1 | 1 | 1 | 5.0 |
| F2.D1.WP3 | Obbligatorietà condizionata | M | 2 | 1 | 1 | 1 | 1 | 3.0 |
| F2.D2.WP1 | Orchestrazione + DAO validazione CF | L | 2 | 2 | 3 | 2 | 2 | 5.0 |
| F2.D3.WP1 | UI avvisi CF non bloccanti | M | 2 | 2 | 2 | 1 | 2 | 3.0 |
| **F2 subtotal** | | | | | | | | **24.0** |
| F3.D1.WP1 | Ricerca bonifica CF assente | S | 1 | 1 | 2 | 1 | 1 | 1.0 |
| F3.D1.WP2 | Ricerca bonifica CF non valido | M | 2 | 2 | 2 | 1 | 1 | 3.0 |
| F3.D1.WP3 | Ricerca bonifica CF non congruente | M | 2 | 2 | 2 | 1 | 2 | 3.0 |
| F3.D2.WP1 | Navigazione lista bonifica + re-validazione | M | 2 | 2 | 3 | 1 | 2 | 3.0 |
| F3.D2.WP2 | Export CSV lista bonifica | S | 1 | 1 | 2 | 1 | 1 | 1.0 |
| F3.D3.WP1 | UI modulo bonifica | M | 2 | 2 | 2 | 1 | 1 | 3.0 |
| **F3 subtotal** | | | | | | | | **14.0** |
| F4.D1.WP1 | RBAC JBoss EAP modulo bonifica | S | 1 | 2 | 2 | 1 | 2 | 1.0 |
| F4.D2.WP1 | Validazione prestazioni + audit trail | M | 1 | 2 | 2 | 1 | 2 | 2.5 |
| **F4 subtotal** | | | | | | | | **3.5** |
| **TOTALE** | | | | | | | | **48.5** |

## distribuzione_per_fase

| Fase | GG | % | Priorità |
|---|---|---|---|
| F1 — Fondazione | 7.0 | 14.4% | Alta |
| F2 — FA-001 Validazione CF | 24.0 | 49.5% | Alta |
| F3 — FA-002 Bonifica Archivi | 14.0 | 28.9% | Alta |
| F4 — Sicurezza e Prestazioni | 3.5 | 7.2% | Alta/Media |
| **Totale** | **48.5** | 100% | |

## distribuzione_per_tipo_attività

| Tipo | GG stimati | % |
|---|---|---|
| Architettura/Setup | 6.5 | 13.4% |
| Implementazione | 29.0 | 59.8% |
| UI/UX e design | 2.0 | 4.1% |
| Qualità e test | 11.0 | 22.7% |
| **Totale** | **48.5** | 100% |

## confronto_fp_sizing

| Metrica | Valore |
|---|---|
| Stima FP_SIZING (IFPUG+SNAP, Medium 8h/FP) | 34.6 GG |
| Stima WBS implementativa pura | 37.5 GG |
| Delta assoluto | +2.9 GG |
| Delta percentuale | +8.4% |
| Valutazione | ✅ Entro soglia ±15% — stime coerenti |
| Stima WBS con test embedded | 48.5 GG |
| Budget raccomandato | 48.5 GG (include QA embedded) |
| Budget con contingency +10% | 53.4 GG |

## analisi_rischi_costo

| Rischio | WP impattati | Probabilità | Impatto GG | Azione |
|---|---|---|---|---|
| risk-001: Edge case algoritmo CF non documentati | F2.D1.WP1, F2.D1.WP2 | Media | +2÷3 GG | Revisione con tabella ministeriale ufficiale in F1 |
| risk-002: Tabella Belfiore mancante su Oracle SIES | F2.D1.WP1 | Bassa | +1 GG | Verificare in F1.D1.WP1; fallback: import file ministeriale |
| risk-003: Modifica JSP esistenti con effetti collaterali | F2.D3.WP1, F3.D3.WP1 | Media | +1÷2 GG | Code review esteso prima del merge |
| risk-004: NFR-002 non raggiunto senza ottimizzazioni | F3.D1.WP3, F4.D2.WP1 | Media | +1÷2 GG | Test prestazioni anticipati su dataset campione |

## note

- Test unitari e funzionali embedded nei WP: non è prevista fase separata di QA
- F2 (FA-001) è il blocco più costoso (49.5%): concentrazione nell'algoritmo ministeriale (WP1 = XL)
- F3 (FA-002) beneficia del riuso comp-002 sviluppato in F2: stima più contenuta rispetto a 5 FR aggiuntivi
- Confronto FP_SIZING coerente: delta +8.4% nella norma, differenza spiegata dal test embedding WBS
- Pianificazione suggerita: 1 senior dev (algoritmo CF) + 1 mid dev (UI + DAO + bonifica) = ~5 settimane parallele
