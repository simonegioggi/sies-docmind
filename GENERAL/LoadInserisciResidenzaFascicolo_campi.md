---
uniqueName: loadinserisciresidenzafascicolocampi
displayName: "LoadInserisciResidenzaFascicolo campi"
category: "GENERAL"
tags: []
---

# LoadInserisciResidenzaFascicolo_campi

## Campi Residenza Fascicolo

| Campo         | Obbligatorio   | Tipo       | Sezione        | Note                                                                                   |
|:--------------|:---------------|:-----------|:---------------|:---------------------------------------------------------------------------------------|
| Indirizzo     | nan            | input text | Dati Residenza | Stringa max 100 caratteri                                                              |
| Cap           | nan            | input text | Dati Residenza | Numerico, lunghezza esatta 5 cifre (validazione JS)                                    |
| Luogo         | *              | input text | Dati Residenza | Obbligatorio quando Stato = Italia (039); valorizzabile tramite popup selezione comune |
| Comune Estero | *              | input text | Dati Residenza | Obbligatorio quando Stato estero (diverso da 039); non compilare se Stato = Italia     |
| Stato         | *              | select     | Dati Residenza | Sempre obbligatorio; selezione nazione da lista                                        |