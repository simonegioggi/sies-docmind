---
uniqueName: loadinseriscidomiciliofascicolocampi
displayName: "LoadInserisciDomicilioFascicolo campi"
category: "GENERAL"
tags: []
---

# LoadInserisciDomicilioFascicolo_campi

## Campi

| Campo         | Obbligatorio   | Tipo       | Sezione   | Note                                                         |
|:--------------|:---------------|:-----------|:----------|:-------------------------------------------------------------|
| Indirizzo     | nan            | input text | Domicilio | Se valorizzato, attiva controlli su Luogo/Comune Estero      |
| Cap           | nan            | input text | Domicilio | Validazione JavaScript: numerico, lunghezza minima 5         |
| Luogo         | *              | input text | Domicilio | Obbligatorio quando Stato = Italia (codice 039)              |
| Comune Estero | *              | input text | Domicilio | Obbligatorio per Stato estero quando è presente un indirizzo |
| Stato         | *              | select     | Domicilio | Obbligatorio (non può essere '-')                            |