---
uniqueName: 11-coverage-matrix
displayName: "WBS Coverage Matrix \u2014 Tracciabilit\u00e0 WBS \u00d7 Scenari \u00d7 Feature \u00d7 FR \u00d7 Componenti"
category: "WBS_DRAFT"
tags: []
---

# coverage_matrix

## riepilogo

| metric | value |
|---|---|
| work_packages_analizzati | 16 |
| scenarios_totali | 12 |
| features_totali | 5 |
| fr_totali | 12 |
| components_totali | 5 |
| wbs_coverage_scn | 100% (12/12) |
| wbs_coverage_feat | 100% (5/5) |
| wbs_coverage_fr | 100% (12/12) |
| wbs_coverage_comp | 100% (5/5) |
| gap_count | 0 bloccanti, 2 rischi |

## matrice_copertura_principale

Legenda: ✅ coperto direttamente | 🔗 coperto indirettamente (via dipendenza) | — non applicabile

### Dimensione Scenari (SCN-001÷012)

| Work Package | SCN-001 | SCN-002 | SCN-003 | SCN-004 | SCN-005 | SCN-006 | SCN-007 | SCN-008 | SCN-009 | SCN-010 | SCN-011 | SCN-012 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| F1.D1.WP1 — Ambiente dev | — | — | — | — | — | — | — | — | — | — | — | — |
| F1.D1.WP2 — Schema DB | 🔗 | 🔗 | 🔗 | 🔗 | 🔗 | 🔗 | 🔗 | 🔗 | 🔗 | 🔗 | 🔗 | 🔗 |
| F1.D1.WP3 — Modulo CF struttura | 🔗 | 🔗 | 🔗 | 🔗 | 🔗 | 🔗 | — | — | — | — | — | — |
| F2.D1.WP1 — Algoritmo ministeriale | ✅ | ✅ | ✅ | ✅ | 🔗 | ✅ | — | — | 🔗 | — | — | — |
| F2.D1.WP2 — Verifica formale + congruenza | ✅ | ✅ | ✅ | ✅ | 🔗 | 🔗 | — | 🔗 | 🔗 | — | — | — |
| F2.D1.WP3 — Obbligatorietà condizionata | 🔗 | 🔗 | 🔗 | ✅ | ✅ | ✅ | — | — | — | — | — | — |
| F2.D2.WP1 — Orchestrazione + DAO | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | — | — | — | — | — | — |
| F2.D3.WP1 — UI avvisi CF | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | — | — | — | — | — | — |
| F3.D1.WP1 — Ricerca CF assente | — | — | — | — | — | — | ✅ | — | — | — | — | — |
| F3.D1.WP2 — Ricerca CF non valido | — | — | — | — | — | — | — | ✅ | — | — | — | — |
| F3.D1.WP3 — Ricerca CF non congruente | — | — | — | — | — | — | — | — | ✅ | — | — | — |
| F3.D2.WP1 — Navigazione + re-validazione | — | — | — | — | — | — | — | — | — | ✅ | ✅ | — |
| F3.D2.WP2 — Export CSV | — | — | — | — | — | — | — | — | — | — | — | ✅ |
| F3.D3.WP1 — UI modulo bonifica | — | — | — | — | — | — | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| F4.D1.WP1 — RBAC bonifica | — | — | — | — | — | — | 🔗 | 🔗 | 🔗 | 🔗 | 🔗 | 🔗 |
| F4.D2.WP1 — Prestazioni + audit | 🔗 | — | — | — | — | — | 🔗 | 🔗 | ✅ | — | — | — |

**Copertura scenari:** 12/12 (100%)

### Dimensione Feature (FEAT-001÷005)

| Work Package | FEAT-001 CF obbligatorio | FEAT-002 Verifica CF | FEAT-003 Avvisi non bloccanti | FEAT-004 Ricerche bonifica | FEAT-005 Navigazione+Export |
|---|---|---|---|---|---|
| F1.D1.WP3 | 🔗 | ✅ | — | — | — |
| F2.D1.WP1 | — | ✅ | — | — | — |
| F2.D1.WP2 | — | ✅ | — | — | — |
| F2.D1.WP3 | ✅ | ✅ | — | — | — |
| F2.D2.WP1 | ✅ | ✅ | 🔗 | — | — |
| F2.D3.WP1 | 🔗 | 🔗 | ✅ | — | — |
| F3.D1.WP1 | — | — | — | ✅ | — |
| F3.D1.WP2 | — | — | — | ✅ | — |
| F3.D1.WP3 | — | — | — | ✅ | — |
| F3.D2.WP1 | — | — | — | — | ✅ |
| F3.D2.WP2 | — | — | — | — | ✅ |
| F3.D3.WP1 | — | — | — | ✅ | ✅ |

**Copertura feature:** 5/5 (100%)

### Dimensione Requisiti Funzionali (FR-001÷012)

| Work Package | FR-001 | FR-002 | FR-003 | FR-004 | FR-005 | FR-006 | FR-007 | FR-008 | FR-009 | FR-010 | FR-011 | FR-012 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| F2.D1.WP1 | — | — | ✅ | — | — | — | — | — | — | 🔗 | — | — |
| F2.D1.WP2 | — | ✅ | ✅ | ✅ | — | — | — | — | 🔗 | 🔗 | — | — |
| F2.D1.WP3 | ✅ | 🔗 | 🔗 | 🔗 | — | — | ✅ | — | — | — | — | — |
| F2.D2.WP1 | ✅ | ✅ | ✅ | ✅ | ✅ | 🔗 | ✅ | — | — | — | — | — |
| F2.D3.WP1 | 🔗 | 🔗 | 🔗 | 🔗 | ✅ | ✅ | 🔗 | — | — | — | — | — |
| F3.D1.WP1 | — | — | — | — | — | — | — | ✅ | — | — | — | — |
| F3.D1.WP2 | — | ✅ | ✅ | — | — | — | — | — | ✅ | — | — | — |
| F3.D1.WP3 | — | — | ✅ | — | — | — | — | — | — | ✅ | — | — |
| F3.D2.WP1 | — | — | — | — | — | — | — | — | — | — | ✅ | — |
| F3.D2.WP2 | — | — | — | — | — | — | — | — | — | — | — | ✅ |
| F3.D3.WP1 | — | — | — | — | — | — | — | ✅ | ✅ | ✅ | ✅ | ✅ |

**Copertura FR:** 12/12 (100%)

### Dimensione Componenti (comp-001÷005)

| Work Package | comp-001 Presentation | comp-002 Modulo CF | comp-003 Servizio GS | comp-004 Modulo Bonifica | comp-005 DAL |
|---|---|---|---|---|---|
| F1.D1.WP2 | — | — | — | — | ✅ |
| F1.D1.WP3 | — | ✅ | — | — | — |
| F2.D1.WP1÷3 | — | ✅ | — | — | — |
| F2.D2.WP1 | — | 🔗 | ✅ | — | ✅ |
| F2.D3.WP1 | ✅ | 🔗 | 🔗 | — | — |
| F3.D1.WP1÷3 | — | 🔗 | — | ✅ | ✅ |
| F3.D2.WP1÷2 | ✅ | — | — | ✅ | — |
| F3.D3.WP1 | ✅ | — | — | ✅ | — |
| F4.D1.WP1 | ✅ | — | — | ✅ | — |
| F4.D2.WP1 | — | ✅ | ✅ | ✅ | ✅ |

**Copertura componenti:** 5/5 (100%)

## analisi_gap

### Gap bloccanti
Nessun gap bloccante identificato. Tutti i 12 FR, 5 Feature, 12 SCN e 5 componenti coperti da almeno un WP.

### Rischi di copertura

| Rischio | Descrizione | WP responsabile | Azione suggerita |
|---|---|---|---|
| R-COV-01 | 8 casi TEST_SPEC non coperti da scenari ufficiali: paese null, CF case-sensitivity, stranieri con CF, dati anagrafici incompleti, anomalie multiple, navigazione soggetto cancellato, export lista vuota, UW-010 | F2.D1.WP2, F2.D1.WP3, F2.D3.WP1, F3.D2.WP2 | Aggiungere test di accettazione nei WP indicati |
| R-COV-02 | F1.D1.WP1 non copre scenari funzionali (setup infrastruttura esistente) | F1.D1.WP1 | Documentare assumption: JBoss EAP 6.4 + Oracle 12.1.0.2 già disponibili |

## tracciabilità_wbs_analysis

| WBS ID | SCN coperti | FEAT coperti | FR coperti | comp coinvolti |
|---|---|---|---|---|
| F1.D1 | — | — | — | comp-002, comp-005 |
| F2.D1 | SCN-001÷006 | FEAT-001, FEAT-002 | FR-001÷004, FR-007 | comp-002 |
| F2.D2 | SCN-001÷006 | FEAT-001, FEAT-002 | FR-001÷006, FR-007 | comp-003, comp-005 |
| F2.D3 | SCN-001÷006 | FEAT-003 | FR-005, FR-006 | comp-001 |
| F3.D1 | SCN-007÷009 | FEAT-004 | FR-008÷010 | comp-004, comp-005 |
| F3.D2 | SCN-010÷012 | FEAT-005 | FR-011, FR-012 | comp-004, comp-001 |
| F3.D3 | SCN-007÷012 | FEAT-004, FEAT-005 | FR-008÷012 | comp-001 |
| F4.D1 | — | — | — | comp-001, comp-004 |
| F4.D2 | SCN-009 (NFR-002) | — | — | comp-002÷005 |

## note

- comp-001 (Presentation) attraversa più fasi: risk-001 (modifica JSP esistenti) da monitorare
- NFR-003 (salvataggio non bloccante) coperto in F2.D2.WP1.A2 e F2.D3.WP1.A2
- NFR-006 (HTTPS) non genera WP: garantito dall'infrastruttura JBoss EAP 6.4 esistente
