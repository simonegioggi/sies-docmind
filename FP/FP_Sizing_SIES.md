---
uniqueName: 04-fp-sizing
displayName: "FP Sizing \u2014 SIES"
category: "FP"
tags: []
---

# FP Sizing — SIES

## Executive Summary

| Voce | Valore |
|---|---|
| Progetto | SIES — Sistema Informativo Enti SIES |
| Perimetro | Validazione CF soggetti + Modulo bonifica archivi |
| Metodo di misurazione | IFPUG + SNAP |
| Totale FP stimati | 29 |
| Totale SNAP Point stimati | 28 |
| Totale COSMIC CFP | — (metodo non selezionato) |
| Stima effort | **34.6 GG/U** (velocity: Medium — 8h/FP) |
| Punti equivalenti totali | 34.6 (FP 29 + SNAP 28 ≈ 5.6 FP eq.) |
| Livello affidabilità stima | Medio (prima stima da ANALYSIS; parametri DET/FTR da raffinare) |
| Modalità calcolo | MCP (engenius-mcp-server) |

---

## Boundary e attori

| Voce | Contenuto |
|---|---|
| Boundary | Applicativo SIES — Java 8, on-premise Linux. Include: gestione soggetti (inserimento/modifica) con validazione CF integrata, modulo bonifica archivi (ricerca per tipologia anomalia, navigazione, esportazione). |
| Attori primari | Funzionario Amministrativo (role-001); Funzionario Bonifica (role-002) |
| Sistemi esterni (EIF) | Nessuno — algoritmo ministeriale CF eseguito internamente |

---

## Catalogo funzioni IFPUG

| ID | Funzione | Tipo | DET | FTR/RET | Complessità | FP | Stato |
|---|---|---|---|---|---|---|---|
| D01 | Archivio Soggetti | ILF | 12 | RET=1 | Low | 7 | Confermato |
| F01 | Inserimento Soggetto con Validazione CF | EI | 10 | FTR=1 | Low | 3 | Confermato |
| F02 | Modifica Soggetto con Validazione CF | EI | 10 | FTR=1 | Low | 3 | Confermato |
| F03 | Ricerca Bonifica — CF Assente nati in Italia | EQ | 6 | FTR=1 | Low | 3 | Confermato |
| F04 | Ricerca Bonifica — CF Formalmente Non Valido | EQ | 6 | FTR=1 | Low | 3 | Confermato |
| F05 | Ricerca Bonifica — CF Non Congruente | EQ | 6 | FTR=1 | Low | 3 | Confermato |
| F06 | Navigazione Lista Bonifica → Scheda Soggetto | EQ | 10 | FTR=1 | Low | 3 | Confermato |
| F07 | Esportazione Lista Bonifica in CSV | EO | 7 | FTR=1 | Low | 4 | Confermato |
| | | | | | **Totale FP** | **29** | |

---

## Catalogo requisiti SNAP

| ID | Requisito | Categoria SNAP | Parametro | SNAP | Stato |
|---|---|---|---|---|---|
| N01 | Avviso CF con tipologia anomalia e CF atteso | 2.1 — Interface Design | 3 tipologie anomalia | 2 | Confermato |
| N02 | Validazione CF — performance < 2 secondi | 3.1 — Multiple Platforms/Temporal | 1 vincolo prestazionale | 8 | Confermato |
| N03 | Ricerca bonifica — performance < 60s su 10.000 soggetti | 3.1 — Multiple Platforms/Temporal | 1 vincolo prestazionale | 8 | Confermato |
| N04 | Controllo accesso modulo bonifica (security) | 4.2 — Multiple I/O Interfaces | 1 livello autorizzazione | 8 | Confermato |
| N05 | Algoritmo CF ministeriale in modulo isolato | 1.2 — Logical/Mathematical Operations | 1 algoritmo | 2 | Confermato |
| | | | **Totale SNAP** | **28** | |

---

## Riepilogo quantitativo

| Metrica | Valore |
|---|---|
| Totale FP | 29 |
| Totale SNAP Point | 28 |
| Punti equivalenti totali | 34.6 |
| Effort stimato | **34.6 GG/U** |
| Ore totali stimate | 276.8 h |
| Velocity applicata | Medium — 8h/FP |
| Data stima | 2026-06-16 |

---

## Assunzioni e rischi

| ID | Tipo | Descrizione | Impatto |
|---|---|---|---|
| A01 | Assunzione | L'ILF Soggetti non richiede sub-gruppi logici distinti (RET=1); il dominio CF si aggiunge ai campi esistenti. | Se si aggiungono sottogruppi (es. storico soggetto) il RET aumenterebbe e il peso dell'ILF passerebbe da 7 a 10 FP. |
| A02 | Assunzione | I DET per EI/EQ sono stimati dal perimetro funzionale; una rilevazione dettagliata dei campi schermata potrebbe modificarli. | Impatto basso — variazioni di 1-2 DET non cambiano la complessità per queste funzioni (range Low ancora ampio). |
| A03 | Assunzione | I vincoli prestazionali NFR-001 e NFR-002 sono stati classificati come SNAP 3.1 con parametro=1 ciascuno. | I SNAP 3.1 risultano High (8 punti cad.); se la piattaforma on-premise non richiede ottimizzazione architetturale dedicata, il parametro potrebbe essere ridotto. |
| R01 | Rischio | Il calcolo del CF atteso per 10.000 soggetti (ricerca bonifica UW-010) potrebbe richiedere ottimizzazioni significative (batch processing, indici). | Rischio di under-estimate se l'implementazione richiede più della media; valutare separatamente il sotto-progetto performance. |
| R02 | Rischio | I gap evidenziati nella TEST_SPEC (comportamento dati incompleti, soggetti stranieri con CF, gestione omocodici) potrebbero introdurre nuovi FR non coperti in questa stima. | Potenziale aumento di 2-5 FP se i gap generano nuovi requisiti funzionali. |

---

## Tracciabilità IFPUG

| FP ID | Use Case / Feature / FR | Riferimento ANALYSIS |
|---|---|---|
| D01 | FEAT-001÷005; tutti gli UC | 02_functional_requirements, 03_features |
| F01 | UC-001; FR-001÷007; FEAT-001÷003 | 04_use_cases, 04b_scenarios (SCN-001÷005) |
| F02 | UC-002; FR-001÷007; FEAT-001÷003 | 04_use_cases, 04b_scenarios (SCN-006) |
| F03 | FR-008; UC-003; FEAT-004 | 04b_scenarios (SCN-007) |
| F04 | FR-009; UC-003; FEAT-004 | 04b_scenarios (SCN-008) |
| F05 | FR-010; UC-003; FEAT-004 | 04b_scenarios (SCN-009) |
| F06 | FR-011; UC-004; FEAT-005 | 04b_scenarios (SCN-010÷011) |
| F07 | FR-012; UC-005; FEAT-005 | 04b_scenarios (SCN-012) |

## Tracciabilità SNAP

| SNAP ID | Requisito non funzionale | Riferimento ANALYSIS |
|---|---|---|
| N01 | NFR-006 (QA-004 Usabilità); FR-005 | 04c_non_functional_requirements |
| N02 | NFR-001 (QA-001 Prestazioni) | 04c_non_functional_requirements |
| N03 | NFR-002 (QA-001 Prestazioni) | 04c_non_functional_requirements |
| N04 | NFR-005 (QA-003 Sicurezza) | 04c_non_functional_requirements |
| N05 | NFR-007 (QA-005 Manutenibilità) | 04c_non_functional_requirements |

---

## Prossimi passi

- Promuovere questo documento da `FP_DRAFT` a `FP` per sbloccare la fase DESIGN.
- Raffinare i DET/FTR della scheda soggetto nella fase DESIGN (quando il modello dati sarà definito).
- Rivalutare i SNAP 3.1 (performance) dopo la scelta architetturale (batch processing vs query ottimizzata).
- Verificare con il team tecnico se i gap identificati in TEST_SPEC generano nuovi FR non coperti.
