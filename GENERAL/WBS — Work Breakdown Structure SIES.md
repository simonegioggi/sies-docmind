---
uniqueName: wbs-work-breakdown-structure-sies
displayName: "WBS \u2014 Work Breakdown Structure SIES"
category: "GENERAL"
tags: []
---

# wbs

## riepilogo

| metric | value |
|---|---|
| total_phases | 4 |
| total_deliverables | 9 |
| total_work_packages | 16 |
| total_activities | 53 |
| high_priority_phases | 3 |
| high_priority_deliverables | 7 |

## wbs_table

| id | parent_id | level | name | activity_type | priority | predecessor_id | source_refs |
|---|---|---|---|---|---|---|---|
| F1 | — | phase | Fondazione e Adeguamento Sistema SIES | — | Alta | — | 01_business_requirements, 07_components, 08_dependency-map, 09_architecture-design |
| F1.D1 | F1 | deliverable | Bootstrap ambiente e adeguamento schema dati | — | Alta | — | 07_components, 08_dependency-map, 05_logical-entities |
| F1.D1.WP1 | F1.D1 | work_package | Preparare l'ambiente di sviluppo per l'estensione SIES | — | Alta | — | 07_components, 09_architecture-design |
| F1.D1.WP1.A1 | F1.D1.WP1 | activity | Acquisire accesso al codebase SiesWeb EAR e verificare build Maven locale | Architettura/Setup | Alta | — | 07_components, 09_architecture-design |
| F1.D1.WP1.A2 | F1.D1.WP1 | activity | Configurare ambiente di test locale con JBoss EAP 6.4 e Oracle 12.1.0.2 | Architettura/Setup | Alta | F1.D1.WP1.A1 | 09_architecture-design |
| F1.D1.WP1.A3 | F1.D1.WP1 | activity | Predisporre dataset di test Oracle con soggetti campione (inclusi italiani, stranieri, CF validi/non validi) | Architettura/Setup | Alta | F1.D1.WP1.A2 | 05_logical-entities, 04b_scenarios |
| F1.D1.WP2 | F1.D1 | work_package | Adeguare lo schema Oracle SIES per la gestione del codice fiscale | — | Alta | F1.D1.WP1 | 05_logical-entities, 08_dependency-map |
| F1.D1.WP2.A1 | F1.D1.WP2 | activity | Aggiungere colonna codiceFiscale alla tabella soggetti e creare indici composti (paeseNascita, codiceFiscale) | Architettura/Setup | Alta | — | 05_logical-entities |
| F1.D1.WP2.A2 | F1.D1.WP2 | activity | Creare tabella anomalie_codice_fiscale con FK verso soggetti (ent-003) | Architettura/Setup | Alta | F1.D1.WP2.A1 | 05_logical-entities |
| F1.D1.WP2.A3 | F1.D1.WP2 | activity | Creare script di migrazione SQL versionata e validare su ambiente di test | Architettura/Setup | Alta | F1.D1.WP2.A2 | 05_logical-entities, 08_dependency-map |
| F1.D1.WP3 | F1.D1 | work_package | Creare la struttura del modulo Java isolato Validazione CF (comp-002) | — | Alta | F1.D1.WP2 | 07_components, 09_architecture-design |
| F1.D1.WP3.A1 | F1.D1.WP3 | activity | Creare alberatura Maven modulo cf-validator come sub-modulo di SiesWeb EAR | Architettura/Setup | Alta | — | 07_components, 09_architecture-design |
| F1.D1.WP3.A2 | F1.D1.WP3 | activity | Definire interfaccia pubblica del modulo: ValidaCF(Soggetto):RisultatoValidazione (NFR-007) | Architettura/Setup | Alta | F1.D1.WP3.A1 | 07_components, 02_functional_requirements |
| F1.D1.WP3.A3 | F1.D1.WP3 | activity | Definire modello dati del modulo: CodiceFiscale, AnomaliaCodiceFiscale, RisultatoValidazione (ent-002÷004) | Architettura/Setup | Alta | F1.D1.WP3.A2 | 05_logical-entities |
| F2 | — | phase | FA-001 — Validazione Codice Fiscale | — | Alta | F1 | 02_functional_requirements, 03_features, 04_use_cases, 04b_scenarios, 07_components |
| F2.D1 | F2 | deliverable | Algoritmo ministeriale e logica di validazione CF — comp-002 | — | Alta | — | 02_functional_requirements, 03_features, 07_components |
| F2.D1.WP1 | F2.D1 | work_package | Implementare l'algoritmo ministeriale di calcolo del CF atteso (FR-003, FEAT-002) | — | Alta | — | 02_functional_requirements, 03_features |
| F2.D1.WP1.A1 | F2.D1.WP1 | activity | Implementare generazione segmento cognome (regola consonanti/vocali, J sostitutivo) | Implementazione | Alta | — | 02_functional_requirements |
| F2.D1.WP1.A2 | F2.D1.WP1 | activity | Implementare generazione segmento nome (regola 4 consonanti, vocali) | Implementazione | Alta | F2.D1.WP1.A1 | 02_functional_requirements |
| F2.D1.WP1.A3 | F2.D1.WP1 | activity | Implementare generazione segmento data nascita e sesso (AAMMGG+sesso) | Implementazione | Alta | F2.D1.WP1.A2 | 02_functional_requirements |
| F2.D1.WP1.A4 | F2.D1.WP1 | activity | Implementare codice comune/stato estero (lookup tabella Belfiore su Oracle) | Implementazione | Alta | F2.D1.WP1.A3 | 02_functional_requirements, 05_logical-entities |
| F2.D1.WP1.A5 | F2.D1.WP1 | activity | Implementare calcolo carattere di controllo (algoritmo dispari/pari con tabella conversione) | Implementazione | Alta | F2.D1.WP1.A4 | 02_functional_requirements |
| F2.D1.WP1.A6 | F2.D1.WP1 | activity | Scrivere unit test parametrici algoritmo ministeriale (JUnit 4, min. 20 casi) | Qualità e test | Alta | F2.D1.WP1.A5 | 02_functional_requirements, 04_use_cases |
| F2.D1.WP2 | F2.D1 | work_package | Implementare verifica formale del CF e confronto congruenza (FR-002, FR-004, FEAT-002) | — | Alta | F2.D1.WP1 | 02_functional_requirements, 03_features |
| F2.D1.WP2.A1 | F2.D1.WP2 | activity | Implementare verifica formato CF: 16 caratteri, struttura posizionale alfanumerica, case-insensitive | Implementazione | Alta | — | 02_functional_requirements |
| F2.D1.WP2.A2 | F2.D1.WP2 | activity | Implementare confronto CF inserito vs CF atteso e produzione AnomaliaCodiceFiscale con tipologia e CF atteso (ent-003) | Implementazione | Alta | F2.D1.WP2.A1 | 02_functional_requirements, 05_logical-entities |
| F2.D1.WP2.A3 | F2.D1.WP2 | activity | Scrivere unit test verifica formale e confronto congruenza (inclusi: case CF maiuscolo/minuscolo, CF borderline, CF stranieri) | Qualità e test | Alta | F2.D1.WP2.A2 | 04b_scenarios |
| F2.D1.WP3 | F2.D1 | work_package | Implementare logica di obbligatorietà condizionata (FR-001, FR-007, FEAT-001) | — | Alta | F2.D1.WP2 | 02_functional_requirements, 03_features |
| F2.D1.WP3.A1 | F2.D1.WP3 | activity | Implementare regola obbligatorietà: se paeseNascita=ITALIA → CF obbligatorio, altrimenti facoltativo | Implementazione | Alta | — | 02_functional_requirements |
| F2.D1.WP3.A2 | F2.D1.WP3 | activity | Implementare esenzione verifica congruenza per soggetti stranieri senza CF inserito (FR-007) | Implementazione | Alta | F2.D1.WP3.A1 | 02_functional_requirements |
| F2.D1.WP3.A3 | F2.D1.WP3 | activity | Scrivere unit test casistiche obbligatorietà (italiano senza CF, straniero senza CF, straniero con CF, paese null) | Qualità e test | Alta | F2.D1.WP3.A2 | 04b_scenarios |
| F2.D2 | F2 | deliverable | Orchestrazione e persistenza validazione CF — comp-003 + comp-005 | — | Alta | F2.D1 | 02_functional_requirements, 06_business-processes, 07_components |
| F2.D2.WP1 | F2.D2 | work_package | Integrare la validazione CF nel Servizio Gestione Soggetti al salvataggio (FR-001÷006) | — | Alta | — | 02_functional_requirements, 06_business-processes |
| F2.D2.WP1.A1 | F2.D2.WP1 | activity | Aggiungere chiamata al Modulo CF (comp-002) nel flusso di salvataggio del soggetto in comp-003 (dep-002) | Implementazione | Alta | — | 07_components, 08_dependency-map |
| F2.D2.WP1.A2 | F2.D2.WP1 | activity | Propagare RisultatoValidazione al livello di presentazione senza bloccare il salvataggio (FR-005, NFR-003) | Implementazione | Alta | F2.D2.WP1.A1 | 02_functional_requirements |
| F2.D2.WP1.A3 | F2.D2.WP1 | activity | Estendere DAO MyBatis (comp-005) con mapper per scrittura codiceFiscale e anomalie su Oracle (dep-007) | Implementazione | Alta | F2.D2.WP1.A2 | 07_components, 08_dependency-map |
| F2.D2.WP1.A4 | F2.D2.WP1 | activity | Scrivere test di integrazione salvataggio soggetto con e senza anomalie CF (SCN-001÷006) | Qualità e test | Alta | F2.D2.WP1.A3 | 04b_scenarios |
| F2.D3 | F2 | deliverable | UI avvisi CF non bloccanti — comp-001 | — | Alta | F2.D2 | 02_functional_requirements, 03_features, 04b_scenarios |
| F2.D3.WP1 | F2.D3 | work_package | Realizzare interfaccia avvisi CF nella scheda soggetto (FR-005, FR-006, FEAT-003) | — | Alta | — | 02_functional_requirements, 03_features |
| F2.D3.WP1.A1 | F2.D3.WP1 | activity | Progettare mockup avviso CF: banner non bloccante con tipologia anomalia (CF_ASSENTE, CF_NON_VALIDO, CF_NON_CONGRUENTE) e CF atteso | UI/UX e design | Alta | — | 02_functional_requirements |
| F2.D3.WP1.A2 | F2.D3.WP1 | activity | Implementare JSP scheda soggetto: sezione avviso condizionale con testo tipologia e campo CF atteso (FR-006) | Implementazione | Alta | F2.D3.WP1.A1 | 02_functional_requirements |
| F2.D3.WP1.A3 | F2.D3.WP1 | activity | Implementare Action Struts2 per propagare RisultatoValidazione al ValueStack JSP | Implementazione | Alta | F2.D3.WP1.A2 | 07_components |
| F2.D3.WP1.A4 | F2.D3.WP1 | activity | Eseguire test funzionali scenari SCN-001÷006: CF valido, non congruente, formalmente non valido, assente, straniero senza CF, straniero con CF | Qualità e test | Alta | F2.D3.WP1.A3 | 04b_scenarios |
| F3 | — | phase | FA-002 — Bonifica Archivi | — | Alta | F2 | 02_functional_requirements, 03_features, 04b_scenarios, 07_components |
| F3.D1 | F3 | deliverable | Logica ricerche bonifica — comp-004 + comp-005 | — | Alta | — | 02_functional_requirements, 03_features, 06_business-processes |
| F3.D1.WP1 | F3.D1 | work_package | Implementare ricerca soggetti con CF assente (FR-008, FEAT-004) | — | Alta | — | 02_functional_requirements, 03_features |
| F3.D1.WP1.A1 | F3.D1.WP1 | activity | Implementare query MyBatis per soggetti con paeseNascita=ITALIA e CF vuoto/null | Implementazione | Alta | — | 02_functional_requirements, 05_logical-entities |
| F3.D1.WP1.A2 | F3.D1.WP1 | activity | Implementare servizio applicativo ricerca bonifica CF assente (comp-004) e relative action Struts2 | Implementazione | Alta | F3.D1.WP1.A1 | 07_components |
| F3.D1.WP1.A3 | F3.D1.WP1 | activity | Scrivere unit test + test integrazione ricerca CF assente (SCN-007) | Qualità e test | Alta | F3.D1.WP1.A2 | 04b_scenarios |
| F3.D1.WP2 | F3.D1 | work_package | Implementare ricerca soggetti con CF formalmente non valido (FR-009, FEAT-004) | — | Alta | F3.D1.WP1 | 02_functional_requirements, 03_features |
| F3.D1.WP2.A1 | F3.D1.WP2 | activity | Implementare query MyBatis per soggetti italiani con CF presente e verifica formato errato | Implementazione | Alta | — | 02_functional_requirements, 05_logical-entities |
| F3.D1.WP2.A2 | F3.D1.WP2 | activity | Implementare servizio ricerca CF non valido con riuso del motore di verifica formale (comp-002 via dep-006) | Implementazione | Alta | F3.D1.WP2.A1 | 07_components, 08_dependency-map |
| F3.D1.WP2.A3 | F3.D1.WP2 | activity | Scrivere unit test + test integrazione ricerca CF non valido (SCN-008) | Qualità e test | Alta | F3.D1.WP2.A2 | 04b_scenarios |
| F3.D1.WP3 | F3.D1 | work_package | Implementare ricerca soggetti con CF non congruente (FR-010, FEAT-004) | — | Alta | F3.D1.WP2 | 02_functional_requirements, 03_features |
| F3.D1.WP3.A1 | F3.D1.WP3 | activity | Implementare query MyBatis per soggetti italiani con CF presente e calcolo batch CF atteso (riuso comp-002) | Implementazione | Alta | — | 02_functional_requirements, 07_components |
| F3.D1.WP3.A2 | F3.D1.WP3 | activity | Ottimizzare query con indici Oracle (paeseNascita, codiceFiscale) per rispettare NFR-002 (< 60s su 10.000 soggetti) | Implementazione | Alta | F3.D1.WP3.A1 | 04c_non_functional_requirements |
| F3.D1.WP3.A3 | F3.D1.WP3 | activity | Scrivere unit test + test prestazioni ricerca CF non congruente su dataset 10.000 soggetti (SCN-009, NFR-002) | Qualità e test | Alta | F3.D1.WP3.A2 | 04b_scenarios, 04c_non_functional_requirements |
| F3.D2 | F3 | deliverable | Navigazione diretta e export CSV — comp-004 + comp-001 | — | Alta | F3.D1 | 02_functional_requirements, 03_features, 04b_scenarios |
| F3.D2.WP1 | F3.D2 | work_package | Implementare navigazione diretta lista bonifica → scheda soggetto e re-validazione (FR-011, FEAT-005) | — | Alta | — | 02_functional_requirements, 06_business-processes |
| F3.D2.WP1.A1 | F3.D2.WP1 | activity | Implementare Action Struts2 per apertura scheda soggetto da lista bonifica con ritorno contestuale | Implementazione | Alta | — | 07_components |
| F3.D2.WP1.A2 | F3.D2.WP1 | activity | Implementare re-esecuzione validazione CF al salvataggio del soggetto dal contesto bonifica | Implementazione | Alta | F3.D2.WP1.A1 | 02_functional_requirements |
| F3.D2.WP1.A3 | F3.D2.WP1 | activity | Implementare aggiornamento lista bonifica post-correzione (rimozione soggetto se anomalia risolta) | Implementazione | Alta | F3.D2.WP1.A2 | 02_functional_requirements |
| F3.D2.WP1.A4 | F3.D2.WP1 | activity | Eseguire test funzionali SCN-010 (correzione riuscita) e SCN-011 (anomalia residua) | Qualità e test | Alta | F3.D2.WP1.A3 | 04b_scenarios |
| F3.D2.WP2 | F3.D2 | work_package | Implementare esportazione CSV lista bonifica (FR-012, FEAT-005) | — | Alta | F3.D2.WP1 | 02_functional_requirements, 03_features |
| F3.D2.WP2.A1 | F3.D2.WP2 | activity | Implementare generazione CSV con dati anagrafici soggetto, tipologia anomalia e CF atteso | Implementazione | Alta | — | 02_functional_requirements |
| F3.D2.WP2.A2 | F3.D2.WP2 | activity | Implementare Action Struts2 per download file CSV con content-type application/csv (dep-010) | Implementazione | Alta | F3.D2.WP2.A1 | 07_components, 08_dependency-map |
| F3.D2.WP2.A3 | F3.D2.WP2 | activity | Eseguire test funzionale SCN-012: export lista piena + caso lista vuota (gap TEST_SPEC) | Qualità e test | Alta | F3.D2.WP2.A2 | 04b_scenarios |
| F3.D3 | F3 | deliverable | UI modulo bonifica — comp-001 | — | Alta | F3.D2 | 03_features, 04b_scenarios, 07_components |
| F3.D3.WP1 | F3.D3 | work_package | Realizzare interfaccia modulo bonifica: selezione tipologia, lista risultati, navigazione, export (FEAT-004, FEAT-005) | — | Alta | — | 03_features, 04b_scenarios |
| F3.D3.WP1.A1 | F3.D3.WP1 | activity | Progettare mockup modulo bonifica: form selezione tipologia anomalia, tabella risultati paginata, link navigazione, pulsante CSV | UI/UX e design | Alta | — | 03_features |
| F3.D3.WP1.A2 | F3.D3.WP1 | activity | Implementare JSP modulo bonifica con form selezione, tabella risultati, link apertura scheda e pulsante export CSV | Implementazione | Alta | F3.D3.WP1.A1 | 07_components |
| F3.D3.WP1.A3 | F3.D3.WP1 | activity | Implementare Action Struts2 coordinamento modulo bonifica (FR-008÷012) | Implementazione | Alta | F3.D3.WP1.A2 | 07_components |
| F3.D3.WP1.A4 | F3.D3.WP1 | activity | Eseguire test funzionali UI bonifica: ricerca per tipologia, visualizzazione risultati, navigazione, export CSV | Qualità e test | Alta | F3.D3.WP1.A3 | 04b_scenarios |
| F4 | — | phase | Sicurezza, Prestazioni e Rilascio | — | Alta | F3 | 04c_non_functional_requirements, 08_dependency-map, 09_architecture-design |
| F4.D1 | F4 | deliverable | Sicurezza e controllo accessi modulo bonifica | — | Alta | — | 04c_non_functional_requirements, 01_business_requirements |
| F4.D1.WP1 | F4.D1 | work_package | Configurare RBAC JBoss EAP per l'accesso al modulo bonifica (NFR-005, BR-003) | — | Alta | — | 04c_non_functional_requirements, 01_business_requirements, 09_architecture-design |
| F4.D1.WP1.A1 | F4.D1.WP1 | activity | Definire profilo/ruolo bonifica nel security domain JBoss SIES (dep-011) | Architettura/Setup | Alta | — | 08_dependency-map, 09_architecture-design |
| F4.D1.WP1.A2 | F4.D1.WP1 | activity | Implementare interceptor Struts2 per verifica del ruolo bonifica prima dell'accesso al modulo (NFR-005) | Implementazione | Alta | F4.D1.WP1.A1 | 07_components, 04c_non_functional_requirements |
| F4.D1.WP1.A3 | F4.D1.WP1 | activity | Testare accesso negato per operatore senza profilo bonifica e accesso autorizzato per operatore con profilo | Qualità e test | Alta | F4.D1.WP1.A2 | 04b_scenarios |
| F4.D2 | F4 | deliverable | Validazione prestazioni e audit trail | — | Media | F4.D1 | 04c_non_functional_requirements, 09_architecture-design |
| F4.D2.WP1 | F4.D2 | work_package | Validare NFR-001 (validazione CF < 2s) e NFR-002 (bonifica < 60s) e abilitare audit trail (NFR-004) | — | Media | — | 04c_non_functional_requirements |
| F4.D2.WP1.A1 | F4.D2.WP1 | activity | Configurare e eseguire test di carico per validazione CF: 100 utenti simultanei, obiettivo < 2s (NFR-001) | Qualità e test | Media | — | 04c_non_functional_requirements |
| F4.D2.WP1.A2 | F4.D2.WP1 | activity | Eseguire test prestazioni ricerca bonifica su dataset 10.000 soggetti, obiettivo < 60s (NFR-002); ottimizzare indici se necessario | Qualità e test | Media | F4.D2.WP1.A1 | 04c_non_functional_requirements |
| F4.D2.WP1.A3 | F4.D2.WP1 | activity | Configurare tracciatura Logback per audit validazione CF e operazioni bonifica (NFR-004, dep-012) | Architettura/Setup | Media | F4.D2.WP1.A2 | 04c_non_functional_requirements, 08_dependency-map |

## wbs_per_fase

### F1 — Fondazione e Adeguamento Sistema SIES
**Priorità:** Alta  
**Predecessore:** —  
**Deliverable:**
- F1.D1 — Bootstrap ambiente e adeguamento schema dati

### F2 — FA-001: Validazione Codice Fiscale
**Priorità:** Alta  
**Predecessore:** F1  
**Deliverable:**
- F2.D1 — Algoritmo ministeriale e logica di validazione CF (comp-002)
- F2.D2 — Orchestrazione e persistenza validazione CF (comp-003 + comp-005)
- F2.D3 — UI avvisi CF non bloccanti (comp-001)

### F3 — FA-002: Bonifica Archivi
**Priorità:** Alta  
**Predecessore:** F2  
**Deliverable:**
- F3.D1 — Logica ricerche bonifica (comp-004 + comp-005)
- F3.D2 — Navigazione diretta e export CSV (comp-004 + comp-001)
- F3.D3 — UI modulo bonifica (comp-001)

### F4 — Sicurezza, Prestazioni e Rilascio
**Priorità:** Alta  
**Predecessore:** F3  
**Deliverable:**
- F4.D1 — Sicurezza e controllo accessi modulo bonifica
- F4.D2 — Validazione prestazioni e audit trail

## note_dipendenze

- Dipendenze tra Activity presenti **solo all'interno dello stesso Work Package** (regola 1 rispettata)
- F3.D1.WP2 e F3.D1.WP3 riusano comp-002 tramite dep-006: dipendenza modellata a livello F3.D1 → F2.D1
- F3 dipende da F2 per disponibilità del Modulo CF già testato: dipendenza promossa a livello fase
- F4 dipende da F3 per completezza implementativa: dipendenza promossa a livello fase
- Il sistema SIES è un'estensione di un applicativo esistente: non include bootstrap infrastrutturale completo

## note

- La Fase F1 è limitata all'adeguamento del sistema esistente: Maven, JBoss EAP, Oracle già presenti in produzione
- La colonna Belfiore (F2.D1.WP1.A4) richiede accesso alla tabella di lookup esistente in Oracle SIES
- 8 gap TEST_SPEC documentati: paese null, CF case-sensitivity, straniero con CF presente, dati anagrafici incompleti, anomalie multiple, navigazione soggetto cancellato, export lista vuota, UW-010 soggetti con dati incompleti
- NFR-006 (HTTPS) non genera WP: garantito dall'infrastruttura JBoss EAP 6.4 esistente

WBS_COMPLETED: 4 phases, 9 deliverables, 16 work packages, 53 activities