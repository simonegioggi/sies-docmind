---
uniqueName: 02_functional_requirements
displayName: "Requisiti Funzionali"
category: "ANALYSIS"
tags: []
---

# functional_requirements

## functional_areas

| area_id | area_name | area_description | related_br_ids |
|---|---|---|---|
| FA-001 | Validazione Codice Fiscale | Comprende tutte le funzionalità per verificare obbligatorietà, correttezza formale e congruenza anagrafica del CF al momento dell'inserimento o della modifica. | BR-001; BR-003 |
| FA-002 | Bonifica Archivi Preesistenti | Comprende le funzionalità di ricerca, selezione e correzione dei soggetti in archivio con anomalie sul codice fiscale (assente, non valido, non congruente). | BR-002 |

## requirement_catalog

| fr_id | area_id | requirement_name | requirement_description | primary_actor_ids | input_data | output_data | business_rules |
|---|---|---|---|---|---|---|---|
| FR-001 | FA-001 | Obbligatorietà CF condizionata al paese di nascita | Il sistema verifica se il paese di nascita è Italia; se sì, il CF è obbligatorio; altrimenti è facoltativo. | role-001 | Paese di nascita | Esito obbligatorietà | CF obbligatorio se e solo se paese = ITALIA. |
| FR-002 | FA-001 | Verifica formale del codice fiscale | Il sistema verifica che il CF rispetti il formato standard: 16 caratteri alfanumerici, struttura posizionale ministeriale, carattere di controllo valido. | role-001 | CF inserito | Esito verifica formale | CF valido se: lunghezza=16, struttura posizionale corretta, carattere di controllo coerente. |
| FR-003 | FA-001 | Calcolo del CF atteso dai dati anagrafici | Il sistema calcola il CF atteso applicando l'algoritmo ministeriale italiano a: cognome, nome, data nascita, sesso, comune/stato estero nascita. | role-001 | Cognome, nome, data nascita, sesso, comune/stato nascita | CF atteso (16 caratteri) | Algoritmo ministeriale vigente; in caso di omonimia si applica CF alternativo se previsto. |
| FR-004 | FA-001 | Confronto CF inserito vs CF atteso | Il sistema confronta il CF inserito con il CF atteso e segnala la discrepanza. | role-001 | CF inserito, CF atteso | Esito confronto (congruente/non congruente) | Confronto case-insensitive su tutti i 16 caratteri. |
| FR-005 | FA-001 | Avviso non bloccante con tipologia anomalia e CF atteso | In caso di CF assente/non valido/non congruente, il sistema mostra un avviso con tipologia anomalia e CF atteso. | role-001 | Esiti verifiche, CF atteso | Avviso visibile | Avviso non bloccante. CF atteso sempre mostrato quando disponibile. |
| FR-006 | FA-001 | Salvataggio soggetto non bloccato da anomalie CF | Il sistema consente il salvataggio anche con avvisi CF presenti. | role-001 | Dati soggetto (anche con CF anomalo) | Soggetto salvato | Il salvataggio non è mai bloccato da anomalie CF. |
| FR-007 | FA-001 | Esenzione avvisi per soggetti stranieri senza CF | Il sistema consente il salvataggio senza avvisi se paese di nascita ≠ Italia e CF assente. | role-001 | Paese ≠ Italia, CF assente | Salvataggio senza avvisi | Se paese ≠ ITALIA e CF vuoto, nessuna verifica eseguita. |
| FR-008 | FA-002 | Ricerca soggetti con CF assente nati in Italia | Il sistema fornisce una ricerca che restituisce soggetti con paese=Italia e CF assente. | role-002 | Filtro: paese=ITALIA, CF vuoto | Elenco soggetti con anomalia "CF assente" | Ricerca su intero archivio. |
| FR-009 | FA-002 | Ricerca soggetti con CF formalmente non valido | Il sistema fornisce una ricerca che restituisce soggetti con CF non superante la verifica formale. | role-002 | Filtro: CF presente e non valido formalmente | Elenco soggetti con anomalia "CF non valido" | Stessa logica di FR-002 applicata all'archivio. |
| FR-010 | FA-002 | Ricerca soggetti con CF non congruente | Il sistema fornisce una ricerca che restituisce soggetti con CF non coincidente con quello calcolato dai dati anagrafici. | role-002 | Filtro: CF formalmente valido ma non congruente | Elenco soggetti con anomalia "CF non congruente" | Logica di FR-003/FR-004 applicata all'archivio. |
| FR-011 | FA-002 | Navigazione diretta dalla lista bonifica alla scheda soggetto | Il sistema consente di aprire la scheda di un soggetto dalla lista bonifica con un'azione singola. | role-002 | Selezione soggetto dall'elenco | Apertura scheda soggetto | Senza passaggi intermedi. |
| FR-012 | FA-002 | Esportazione elenco risultati bonifica | Il sistema consente l'esportazione dell'elenco bonifica in formato standard (CSV), con dati anagrafici e tipologia anomalia. | role-002 | Elenco risultati bonifica | File CSV esportabile | Esportazione dell'intero set di risultati attivo. |