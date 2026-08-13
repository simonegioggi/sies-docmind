---
uniqueName: 03_features
displayName: "Feature Catalog"
category: "ANALYSIS"
tags: []
---

# feature_catalog

## features

| feature_id | feature_name | related_br_ids | related_fr_ids | role_list | feature_description | business_value | dependency_notes |
|---|---|---|---|---|---|---|---|
| FEAT-001 | Obbligatorietà CF per Soggetti Nati in Italia | BR-001; BR-003 | FR-001 | role-001 | Il sistema applica la regola di obbligatorietà del CF in modo condizionato: obbligatorio se paese=Italia, facoltativo altrimenti. | Garantisce che i soggetti italiani abbiano sempre un CF, eliminando le lacune per la tipologia più numerosa in archivio. | Dipende dal campo paese di nascita. Prerequisito per FR-003, FR-004, FR-005. |
| FEAT-002 | Verifica Formale e Congruenza CF | BR-001; BR-003 | FR-002; FR-003; FR-004 | role-001 | Il sistema verifica il formato del CF e calcola il CF atteso dai dati anagrafici tramite algoritmo ministeriale, confrontando poi inserito e atteso. | Assicura che i CF in archivio siano validi e coerenti con l'identità del soggetto, non solo formalmente corretti. | Dipende da completezza dati anagrafici. Se incompleti, CF atteso non calcolabile. |
| FEAT-003 | Avviso Non Bloccante con CF Atteso | BR-001; BR-003 | FR-005; FR-006; FR-007 | role-001 | Il sistema mostra avvisi descrittivi con tipologia anomalia e CF atteso. Il salvataggio non è mai bloccato. Nessun avviso per stranieri senza CF. | Informa il funzionario in tempo reale fornendo il dato corretto, senza interrompere il flusso operativo. | Dipende da FEAT-001 e FEAT-002. |
| FEAT-004 | Ricerca Bonifica Archivi per Tipologia Anomalia | BR-002 | FR-008; FR-009; FR-010 | role-002 | Tre ricerche distinte: (a) CF assente con paese=Italia, (b) CF formalmente non valido, (c) CF non congruente. Risultati con tipologia anomalia per soggetto. | Rende operativa la bonifica identificando e prioritizzando i soggetti con anomalie CF senza esame manuale. | Richiede profilo autorizzato. Performance critica: entro 60s su 10.000 soggetti. |
| FEAT-005 | Navigazione e Esportazione Lista Bonifica | BR-002 | FR-011; FR-012 | role-002 | Accesso diretto alla scheda soggetto dalla lista bonifica con azione singola. Esportazione in CSV dell'intero elenco. | Efficienza nel processo di correzione post-bonifica; gestione offline tramite export. | Dipende da FEAT-004. |