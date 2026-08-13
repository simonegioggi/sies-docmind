---
uniqueName: inserimentosoggettocampi
displayName: "InserimentoSoggetto campi"
category: "GENERAL"
tags: []
---

# InserimentoSoggetto_campi

## LoadInserisciSoggetto_campi_edi

| Etichetta                    | Nome tecnico                     | Tipo       | Obbligatorio   | Condizione                    | Note                                                 |
|:-----------------------------|:---------------------------------|:-----------|:---------------|:------------------------------|:-----------------------------------------------------|
| Cognome                      | CAMPO_COGNOME                    | input text | *              | Sempre                        | Max 35 caratteri                                     |
| Nome                         | CAMPO_NOME                       | input text | *              | Sempre                        | Max 35 caratteri                                     |
| Sesso                        | CAMPO_SESSO                      | select     | *              | Sempre                        | nan                                                  |
| Data di nascita - Giorno     | CAMPO_GIORNO_DATA_NASCITA        | input text | nan            | Condizionale                  | Parte della data di nascita                          |
| Data di nascita - Mese       | CAMPO_MESE_DATA_NASCITA          | input text | nan            | Condizionale                  | Parte della data di nascita                          |
| Data di nascita - Anno       | CAMPO_ANNO_DATA_NASCITA          | input text | nan            | Condizionale                  | Parte della data di nascita                          |
| Data Presunta                | CAMPO_DATA_NASCITA_PRESUNTA      | select     | nan            | Condizionale                  | Valori gestiti da select                             |
| Età Presunta - Anni          | CAMPO_ETA_PRESUNTA_ANNI          | input text | nan            | Condizionale                  | Richiesta se manca la data di nascita in alcuni casi |
| Età Presunta - Mesi          | CAMPO_ETA_PRESUNTA_MESI          | input text | nan            | Condizionale                  | Deve essere minore di 12                             |
| Data commesso reato - Giorno | CAMPO_GIORNO_DATA_COMMESSO_REATO | input text | nan            | Condizionale                  | Presente solo per alcuni profili/uffici              |
| Data commesso reato - Mese   | CAMPO_MESE_DATA_COMMESSO_REATO   | input text | nan            | Condizionale                  | Presente solo per alcuni profili/uffici              |
| Data commesso reato - Anno   | CAMPO_ANNO_DATA_COMMESSO_REATO   | input text | nan            | Condizionale                  | Presente solo per alcuni profili/uffici              |
| Comune Nascita               | CAMPO_COD_COMUNE_NASCITA         | input text | *              | Se Stato di Nascita = Italia  | Con lookup comuni                                    |
| Stato Cittadinanza           | CAMPO_NAZIONALITA                | select     | nan            | Facoltativo                   | nan                                                  |
| Stato di Nascita             | CAMPO_COD_STATO_NASCITA          | select     | nan            | Facoltativo                   | nan                                                  |
| Luogo di Nascita Estero      | CAMPO_DESC_COMUNE_NASCITA_ESTERO | input text | nan            | Se Stato di Nascita != Italia | Comune estero testuale                               |
| Paternità                    | CAMPO_PATERNITA                  | input text | nan            | Facoltativo                   | Max 35 caratteri                                     |
| Cognome Madre                | CAMPO_COGNOME_MADRE              | input text | nan            | Facoltativo                   | Max 35 caratteri                                     |
| Nome Madre                   | CAMPO_NOME_MADRE                 | input text | nan            | Facoltativo                   | Max 35 caratteri                                     |
| Codice Fiscale               | CAMPO_COD_FISCALE                | input text | nan            | Facoltativo                   | Max 16 caratteri                                     |
| Atto Nascita                 | CAMPO_ATTO_NASCITA               | input text | nan            | Facoltativo                   | Max 10 caratteri                                     |
| Codice CUI                   | CAMPO_COD_AFIS                   | input text | nan            | Facoltativo                   | Max 7 caratteri                                      |
| Note                         | CAMPO_NOTE                       | textarea   | nan            | Facoltativo                   | nan                                                  |