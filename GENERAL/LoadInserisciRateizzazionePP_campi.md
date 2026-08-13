---
uniqueName: loadinseriscirateizzazioneppcampi
displayName: "LoadInserisciRateizzazionePP campi"
category: "GENERAL"
tags: []
---

# LoadInserisciRateizzazionePP_campi

## LoadInserisciRateizzazionePP_ca

| Campo                                            | Obbligatorio   | Tipo       | Sezione                   | Note                                                                             |
|:-------------------------------------------------|:---------------|:-----------|:--------------------------|:---------------------------------------------------------------------------------|
| Importo da pagare - Intero                       | *              | input text | Importo da pagare         | Obbligatorio come valore complessivo (> 0) insieme alla parte decimale           |
| Importo da pagare - Decimale                     | *              | input text | Importo da pagare         | Obbligatorio come valore complessivo (> 0) insieme alla parte intera             |
| Tipo rateizzazione - Unica Soluzione             | nan            | radio      | Tipo Rateizzazione        | Alternativa a Pagamento Rateizzato                                               |
| Tipo rateizzazione - Pagamento Rateizzato        | nan            | radio      | Tipo Rateizzazione        | Alternativa a Unica Soluzione                                                    |
| Importo rata unica - Intero                      | *              | input text | Pagamento Unica Soluzione | Obbligatorio se tipo rateizzazione = Unica Soluzione                             |
| Importo rata unica - Decimale                    | *              | input text | Pagamento Unica Soluzione | Obbligatorio se tipo rateizzazione = Unica Soluzione                             |
| Numero rate (riga attiva i)                      | *              | input text | Pagamento Rateizzato      | Obbligatorio per ogni riga visibile se tipo rateizzazione = Pagamento Rateizzato |
| Importo ciascuna rata - Intero (riga attiva i)   | *              | input text | Pagamento Rateizzato      | Obbligatorio per ogni riga visibile se tipo rateizzazione = Pagamento Rateizzato |
| Importo ciascuna rata - Decimale (riga attiva i) | *              | input text | Pagamento Rateizzato      | Obbligatorio per ogni riga visibile se tipo rateizzazione = Pagamento Rateizzato |