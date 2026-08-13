---
uniqueName: 04c_non_functional_requirements
displayName: "Non-Functional Requirements"
category: "ANALYSIS"
tags: []
---

# non_functional_requirements

## quality_areas

| quality_area_id | quality_area_name | area_description | related_br_ids |
|---|---|---|---|
| QA-001 | Prestazioni | Tempi di risposta per validazione CF in tempo reale e ricerche bonifica in archivio. | BR-001; BR-003 |
| QA-002 | Disponibilità e Affidabilità | Continuità operativa durante l'orario lavorativo e coerenza dei risultati. | BR-001; BR-002; BR-003 |
| QA-003 | Sicurezza | Controllo accessi alla funzione bonifica in linea con policy di profilazione esistenti. | BR-002 |
| QA-004 | Usabilità | Chiarezza comunicazioni di anomalia CF per correzione autonoma da parte dei funzionari. | BR-001; BR-003 |
| QA-005 | Manutenibilità | Isolamento logica calcolo/validazione CF per aggiornamenti indipendenti dall'algoritmo. | BR-001 |

## requirement_catalog

| nfr_id | quality_area_id | requirement_name | target_or_condition | applies_when | rationale |
|---|---|---|---|---|---|
| NFR-001 | QA-001 | Tempo risposta validazione CF | Esito validazione CF entro 2 secondi dal salvataggio. | Inserimento/modifica soggetto, carico ≤ 100 utenti simultanei. | Funzionari eseguono operazioni in serie; latenze superiori rallentano il processo. |
| NFR-002 | QA-001 | Tempo completamento ricerca bonifica | Ricerca bonifica completata entro 60 secondi su archivio fino a 10.000 soggetti. | Esecuzione ricerca bonifica sull'intero archivio. | Bonifica è operazione una tantum su dimensioni note; tempi superiori la renderebbero impraticabile. |
| NFR-003 | QA-002 | Disponibilità orario lavorativo | Funzionalità operative senza interruzioni non pianificate durante ore lavorative. | Ore lavorative (lunedì–venerdì, orario d'ufficio). | Interruzioni impreviste bloccano l'attività amministrativa integrata nel flusso lavorativo. |
| NFR-004 | QA-002 | Coerenza risultati bonifica | Ricerche producono risultati completi e non troncati per archivi fino a 10.000 soggetti. | Ogni esecuzione ricerca bonifica. | Risultati incompleti compromettono fiducia nel processo e lasciano anomalie non sanate. |
| NFR-005 | QA-003 | Controllo accesso modulo bonifica | Accesso limitato a utenti con profilo autorizzato, conforme a policy accesso esistenti. | Accesso al modulo bonifica archivi. | Bonifica espone l'intero archivio; accesso non controllato è rischio riservatezza dati. |
| NFR-006 | QA-004 | Chiarezza avvisi CF | Avvisi indicano tipologia anomalia e CF atteso per correzione autonoma. | Segnalazione anomalia CF durante inserimento o modifica. | Avviso generico non fornisce informazioni per la correzione; CF atteso riduce le operazioni necessarie. |
| NFR-007 | QA-005 | Isolamento algoritmo calcolo CF | Logica calcolo/validazione CF in modulo dedicato, modificabile indipendentemente. [TO BE REFINED] | Aggiornamento regole calcolo CF ministeriale. | Algoritmo soggetto a variazioni normative; modulo isolato consente aggiornamento senza regressioni. |