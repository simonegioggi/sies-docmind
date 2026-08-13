---
uniqueName: 01_business_requirements
displayName: "Business Requirements e Ruoli"
category: "ANALYSIS"
tags: []
---

# business_analysis

## business_requirements

| br_id | br_name | br_description | stakeholder_list |
|---|---|---|---|
| BR-001 | Qualità del Dato Anagrafico | Ogni soggetto censito nel sistema deve essere identificato univocamente tramite un codice fiscale valido e presente. L'ente deve poter contare su un archivio anagrafico privo di soggetti con CF mancante o non conforme, garantendo l'affidabilità dei dati a beneficio degli operatori interni e dei processi amministrativi dell'ente. | role-001; role-003 |
| BR-002 | Integrità degli Archivi Preesistenti | Le inconsistenze nei dati già registrati, dovute all'assenza storica del controllo sul codice fiscale, devono essere rilevabili e sanabili. L'ente deve disporre di strumenti per identificare i soggetti con CF mancante o non valido negli archivi esistenti e avviare attività di bonifica. | role-002; role-003 |
| BR-003 | Riduzione degli Errori Amministrativi | I procedimenti amministrativi che dipendono dall'identificazione certa dei soggetti devono beneficiare di una base dati affidabile. L'eliminazione di CF errati o assenti deve ridurre il numero di errori, anomalie e rilavorazioni nei processi che utilizzano i dati anagrafici di SIES. | role-001; role-003 |

## list_of_roles

| role_id | role_name | role_description |
|---|---|---|
| role-001 | Funzionario Amministrativo | Operatore interno dell'ente che inserisce, aggiorna e consulta i dati anagrafici dei soggetti in SIES. Principale fruitore delle funzionalità di validazione del codice fiscale durante le operazioni ordinarie di gestione soggetti. |
| role-002 | Funzionario con Accesso Bonifica | Funzionario con profilo autorizzato che accede al modulo di ricerca e bonifica degli archivi preesistenti. Può coincidere con il Funzionario Amministrativo quando dotato di abilitazione specifica alla funzione di bonifica. |
| role-003 | Ente PA | L'organizzazione pubblica che gestisce SIES e beneficia della qualità e integrità degli archivi anagrafici. Portatore di interesse primario rispetto a tutti i business requirements; non interagisce direttamente con il sistema. |