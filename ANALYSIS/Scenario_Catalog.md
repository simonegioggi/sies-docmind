---
uniqueName: 04b_scenarios
displayName: "Scenario Catalog"
category: "ANALYSIS"
tags: []
---

# scenario_catalog

## scenarios

| scenario_id | uc_id | scenario_name | scenario_type | related_feature_ids | trigger | expected_outcome | exception_notes |
|---|---|---|---|---|---|---|---|
| SCN-001 | UC-001 | Inserimento soggetto italiano con CF valido e congruente | Main | FEAT-001; FEAT-002; FEAT-003 | Funzionario compila scheda con paese=Italia e CF formalmente valido e congruente. | Soggetto salvato senza avvisi. | — |
| SCN-002 | UC-001 | Inserimento soggetto italiano con CF valido ma non congruente | Alternate | FEAT-001; FEAT-002; FEAT-003 | Funzionario compila scheda con paese=Italia e CF valido formalmente ma non coincidente con CF calcolato. | Sistema mostra avviso non congruenza con CF atteso; funzionario può salvare. | Funzionario decide se correggere o salvare con avviso. |
| SCN-003 | UC-001 | Inserimento soggetto italiano con CF formalmente non valido | Alternate | FEAT-001; FEAT-002; FEAT-003 | Funzionario compila scheda con paese=Italia e CF con formato errato. | Sistema mostra avviso formato non valido con CF atteso; funzionario può salvare. | CF atteso sempre mostrato affiancato all'avviso. |
| SCN-004 | UC-001 | Inserimento soggetto italiano senza CF | Exception | FEAT-001; FEAT-003 | Funzionario compila scheda con paese=Italia e lascia campo CF vuoto. | Sistema mostra avviso CF obbligatorio con CF atteso; funzionario può salvare comunque. | CF atteso mostrato per facilitare correzione. |
| SCN-005 | UC-001 | Inserimento soggetto straniero senza CF | Alternate | FEAT-001; FEAT-003 | Funzionario compila scheda con paese≠Italia e lascia CF vuoto. | Soggetto salvato senza avvisi. | Nessuna verifica CF per soggetti stranieri senza CF. |
| SCN-006 | UC-002 | Modifica dati anagrafici introduce non congruenza CF | Alternate | FEAT-001; FEAT-002; FEAT-003 | Funzionario modifica dati anagrafici di soggetto italiano il cui CF non corrisponde più ai nuovi dati. | Sistema mostra avviso non congruenza con CF atteso aggiornato; funzionario può salvare. | CF atteso ricalcolato dai nuovi dati anagrafici. |
| SCN-007 | UC-003 | Ricerca soggetti con CF assente nati in Italia | Main | FEAT-004 | Funzionario autorizzato seleziona ricerca CF assente e avvia bonifica. | Elenco soggetti con paese=Italia e CF vuoto visualizzato con tipologia anomalia. | Se nessun risultato, messaggio di lista vuota. |
| SCN-008 | UC-003 | Ricerca soggetti con CF formalmente non valido | Alternate | FEAT-004 | Funzionario seleziona ricerca CF non valido formalmente. | Elenco soggetti con CF non superante verifica formale visualizzato con tipologia anomalia. | — |
| SCN-009 | UC-003 | Ricerca soggetti con CF non congruente | Alternate | FEAT-004 | Funzionario seleziona ricerca CF non congruente. | Elenco soggetti con discrepanza CF atteso/inserito visualizzato con tipologia anomalia. | Ricerca può richiedere fino a 60s su 10.000 soggetti. |
| SCN-010 | UC-004 | Correzione CF da lista bonifica con successo | Main | FEAT-004; FEAT-005 | Funzionario seleziona soggetto dalla lista bonifica, corregge CF e salva. | Soggetto salvato senza avvisi CF. Non compare più nella ricerca bonifica per quell'anomalia. | — |
| SCN-011 | UC-004 | Correzione CF con anomalia residua | Exception | FEAT-004; FEAT-005 | Funzionario inserisce CF valido formalmente ma non congruente. | Sistema mostra avviso non congruenza; funzionario può salvare. | Soggetto rimane nella ricerca non congruenza dopo salvataggio. |
| SCN-012 | UC-005 | Esportazione lista bonifica completata | Main | FEAT-005 | Funzionario richiede esportazione lista bonifica corrente. | File CSV generato con tutti i soggetti dell'elenco e tipologia anomalia. | — |

## scenario_steps

| scenario_id | step_id | step_order | actor_id | action | system_response |
|---|---|---|---|---|---|
| SCN-001 | STEP-001 | 1 | role-001 | Apre scheda inserimento soggetto con paese=ITALIA. | Sistema rende obbligatorio il campo CF. |
| SCN-001 | STEP-002 | 2 | role-001 | Inserisce CF valido (16 caratteri). | Sistema registra il CF. |
| SCN-001 | STEP-003 | 3 | role-001 | Salva il soggetto. | Sistema calcola CF atteso, confronta, rileva congruenza, salva senza avvisi. |
| SCN-002 | STEP-001 | 1 | role-001 | Compila scheda con paese=ITALIA e inserisce CF formalmente valido. | Sistema registra il CF. |
| SCN-002 | STEP-002 | 2 | role-001 | Salva il soggetto. | Sistema calcola CF atteso, rileva non congruenza, mostra avviso con CF atteso. |
| SCN-002 | STEP-003 | 3 | role-001 | Legge avviso e salva con il CF inserito. | Sistema salva il soggetto. |
| SCN-003 | STEP-001 | 1 | role-001 | Compila scheda con paese=ITALIA e inserisce CF con formato errato. | Sistema registra il CF. |
| SCN-003 | STEP-002 | 2 | role-001 | Salva il soggetto. | Sistema rileva formato non valido, mostra avviso con CF atteso. |
| SCN-003 | STEP-003 | 3 | role-001 | Corregge il CF con quello atteso suggerito e salva. | Sistema riesegue verifiche, rileva congruenza, salva senza avvisi. |
| SCN-004 | STEP-001 | 1 | role-001 | Compila scheda con paese=ITALIA e lascia CF vuoto. | Sistema segnala obbligatorietà CF. |
| SCN-004 | STEP-002 | 2 | role-001 | Salva senza inserire CF. | Sistema mostra avviso CF assente con CF atteso, consente salvataggio. |
| SCN-004 | STEP-003 | 3 | role-001 | Salva confermando. | Sistema salva soggetto con CF vuoto. |
| SCN-005 | STEP-001 | 1 | role-001 | Compila scheda con paese≠ITALIA e lascia CF vuoto. | Sistema non impone obbligatorietà CF. |
| SCN-005 | STEP-002 | 2 | role-001 | Salva il soggetto. | Sistema salva senza eseguire verifiche CF. |
| SCN-007 | STEP-001 | 1 | role-002 | Accede modulo bonifica e seleziona ricerca CF assente. | Sistema esegue ricerca su soggetti con paese=ITALIA e CF vuoto. |
| SCN-007 | STEP-002 | 2 | System | — | Sistema restituisce elenco soggetti con anomalia "CF assente". |
| SCN-007 | STEP-003 | 3 | role-002 | Visualizza i risultati. | Sistema mostra lista con dati anagrafici e tipologia anomalia. |
| SCN-010 | STEP-001 | 1 | role-002 | Seleziona soggetto dalla lista bonifica e apre scheda. | Sistema apre scheda soggetto in modalità modifica. |
| SCN-010 | STEP-002 | 2 | role-002 | Inserisce CF corretto e salva. | Sistema verifica CF, rileva congruenza, salva senza avvisi. |
| SCN-010 | STEP-003 | 3 | System | — | Soggetto non figura più nella ricerca bonifica per quell'anomalia. |
| SCN-012 | STEP-001 | 1 | role-002 | Seleziona azione esportazione dalla lista bonifica. | Sistema genera file di esportazione. |
| SCN-012 | STEP-002 | 2 | System | — | File CSV disponibile per download con soggetti e tipologia anomalia. |