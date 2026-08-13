---
uniqueName: loadinsrevocaindultoapcampi
displayName: "LoadInsRevocaIndultoAP campi"
category: "GENERAL"
tags: []
---

# LoadInsRevocaIndultoAP_campi

## LoadInsRevocaIndultoAP_campi

| Campo                        | Obbligatorio   | Tipo       | Sezione                               | Note                                                  |
|:-----------------------------|:---------------|:-----------|:--------------------------------------|:------------------------------------------------------|
| Provvedimento di Concessione | *              | select     | Tipo Beneficio Revocato               | Campo CAMPO_COD_DPR                                   |
| Tipo Provvedimento           | *              | select     | Estremi del Provvedimento da Revocare | Campo CAMPO_COD_TIPO_PROVVEDIMENTO                    |
| Giorno Data Provvedimento    | *              | input text | Estremi del Provvedimento da Revocare | Parte della data provvedimento                        |
| Mese Data Provvedimento      | *              | input text | Estremi del Provvedimento da Revocare | Parte della data provvedimento                        |
| Anno Data Provvedimento      | *              | input text | Estremi del Provvedimento da Revocare | Parte della data provvedimento                        |
| Giorno Definitivo in Data    | nan            | input text | Estremi del Provvedimento da Revocare | Obbligatorio se Tipo Provvedimento != 03              |
| Mese Definitivo in Data      | nan            | input text | Estremi del Provvedimento da Revocare | Obbligatorio se Tipo Provvedimento != 03              |
| Anno Definitivo in Data      | nan            | input text | Estremi del Provvedimento da Revocare | Obbligatorio se Tipo Provvedimento != 03              |
| Emessa da                    | *              | select     | Estremi del Provvedimento da Revocare | Campo CAMPO_COD_TIPO_AUTORITA_EMITTENTE               |
| Luogo                        | *              | input text | Estremi del Provvedimento da Revocare | Campo CAMPO_COD_LUOGO_EMITTENTE                       |
| Sezione                      | nan            | input text | Estremi del Provvedimento da Revocare | Campo CAMPO_NUM_SEZIONE_AUTORITA_EMITTENTE            |
| Anni Reclusione              | nan            | input text | Eventuale Quantum                     | Campo CAMPO_NUM_ANNI_RECLUSIONE                       |
| Mesi Reclusione              | nan            | input text | Eventuale Quantum                     | Campo CAMPO_NUM_MESI_RECLUSIONE                       |
| Giorni Reclusione            | nan            | input text | Eventuale Quantum                     | Campo CAMPO_NUM_GIORNI_RECLUSIONE                     |
| Multa Intero                 | nan            | input text | Eventuale Quantum                     | Può essere valorizzato da solo o con parte decimale   |
| Multa Decimale               | nan            | input text | Eventuale Quantum                     | Opzionale, ma se valorizzato richiede la parte intera |
| Anni Arresto                 | nan            | input text | Eventuale Quantum                     | Campo CAMPO_NUM_ANNI_ARRESTO                          |
| Mesi Arresto                 | nan            | input text | Eventuale Quantum                     | Campo CAMPO_NUM_MESI_ARRESTO                          |
| Giorni Arresto               | nan            | input text | Eventuale Quantum                     | Campo CAMPO_NUM_GIORNI_ARRESTO                        |
| Ammenda Intero               | nan            | input text | Eventuale Quantum                     | Può essere valorizzato da solo o con parte decimale   |
| Ammenda Decimale             | nan            | input text | Eventuale Quantum                     | Opzionale, ma se valorizzato richiede la parte intera |
| Note                         | nan            | textarea   | Eventuale Quantum                     | Campo CAMPO_NOTE                                      |