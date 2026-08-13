---
uniqueName: loadinseriscibeneficioindultocampi
displayName: "LoadInserisciBeneficioIndulto campi"
category: "GENERAL"
tags: []
---

# LoadInserisciBeneficioIndulto_campi

## LoadInserisciBeneficioIndulto_c

| Campo                        |   Obbligatorio | Tipo       | Sezione         | Note                                                                     |
|:-----------------------------|---------------:|:-----------|:----------------|:-------------------------------------------------------------------------|
| Tipo Beneficio               |            nan | select     | Dati beneficio  | Combo valorizzata da tipoBeneficio                                       |
| Provvedimento di Concessione |            nan | select     | Dati beneficio  | Combo valorizzata da listaDPR                                            |
| Applicazione del beneficio   |            nan | select     | Dati beneficio  | Combo sottotipo con onchange CaricaPena()                                |
| Anni Reclusione              |            nan | input text | Reclusione      | Campo ARec con validazione numerica                                      |
| Mesi Reclusione              |            nan | input text | Reclusione      | Campo MRec con validazione numerica                                      |
| Giorni Reclusione            |            nan | input text | Reclusione      | Campo GRec con validazione numerica                                      |
| Multa (parte intera)         |            nan | input text | Reclusione      | Campo Multa con validazione numerica                                     |
| Multa (parte decimale)       |            nan | input text | Reclusione      | Campo Mul_dec con validazione numerica                                   |
| Anni Arresto                 |            nan | input text | Arresto         | Campo AArr con validazione numerica                                      |
| Mesi Arresto                 |            nan | input text | Arresto         | Campo MArr con validazione numerica                                      |
| Giorni Arresto               |            nan | input text | Arresto         | Campo GArr con validazione numerica                                      |
| Ammenda (parte intera)       |            nan | input text | Arresto         | Campo Ammenda con validazione numerica                                   |
| Ammenda (parte decimale)     |            nan | input text | Arresto         | Campo Amm_dec con validazione numerica                                   |
| Note                         |            nan | textarea   | Note            | Campo CAMPO_NOTE                                                         |
| Tipo Pena Accessoria         |            nan | checkbox   | Pene accessorie | Checkbox multiple CAMPO_ID_PENA_ACCESSORIA visibili in base al sottotipo |