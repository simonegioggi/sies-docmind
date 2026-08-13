---
uniqueName: 04_use_cases
displayName: "Use Case Catalog"
category: "ANALYSIS"
tags: []
---

# use_case_catalog

## use_cases

| uc_id | use_case_name | primary_actor_ids | supporting_actor_ids | trigger | related_feature_ids | related_fr_ids | goal | preconditions | postconditions |
|---|---|---|---|---|---|---|---|---|---|
| UC-001 | Inserimento Soggetto con Validazione CF | role-001 | — | Il funzionario avvia l'inserimento di un nuovo soggetto compilando dati anagrafici e CF. | FEAT-001; FEAT-002; FEAT-003 | FR-001; FR-002; FR-003; FR-004; FR-005; FR-006; FR-007 | Il soggetto viene inserito correttamente; se presenti anomalie CF, il funzionario viene informato senza blocco. | Accesso a SIES; scheda soggetto in modalità inserimento. | Soggetto salvato. Se anomalie CF, avviso con CF atteso mostrato prima del salvataggio. |
| UC-002 | Modifica Soggetto con Validazione CF | role-001 | — | Il funzionario apre la scheda di un soggetto esistente e modifica dati anagrafici o CF. | FEAT-001; FEAT-002; FEAT-003 | FR-001; FR-002; FR-003; FR-004; FR-005; FR-006; FR-007 | I dati del soggetto vengono aggiornati; eventuali anomalie CF introdotte vengono segnalate senza blocco. | Accesso a SIES; scheda soggetto in modalità modifica. | Soggetto aggiornato. Se anomalie CF, avviso con CF atteso mostrato. |
| UC-003 | Ricerca Soggetti con Anomalia CF per Bonifica | role-002 | — | Il funzionario autorizzato seleziona la tipologia di anomalia CF da ricercare e avvia la bonifica. | FEAT-004 | FR-008; FR-009; FR-010 | Il funzionario ottiene l'elenco soggetti con anomalia CF selezionata e tipologia per ciascuno. | Accesso con profilo autorizzato alla funzione bonifica. | Elenco risultati visualizzato con tipologia anomalia per soggetto. |
| UC-004 | Correzione CF di Soggetto dalla Lista Bonifica | role-002 | — | Il funzionario seleziona un soggetto dall'elenco bonifica e lo apre per correggere il CF. | FEAT-004; FEAT-005 | FR-011; FR-001; FR-002; FR-003; FR-004; FR-005; FR-006 | Il funzionario accede alla scheda, corregge il CF, riceve feedback di validazione e salva. | Elenco risultati bonifica visualizzato (UC-003 completato). | Soggetto aggiornato con CF corretto o con avviso se anomalie persistono. |
| UC-005 | Esportazione Lista Bonifica | role-002 | — | Il funzionario richiede l'esportazione dell'elenco bonifica corrente. | FEAT-005 | FR-012 | Il funzionario ottiene un file CSV con i soggetti e la tipologia anomalia. | Elenco risultati bonifica visualizzato (UC-003 completato). | File di esportazione disponibile per il download. |