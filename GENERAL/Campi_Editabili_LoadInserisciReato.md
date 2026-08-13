---
uniqueName: campieditabililoadinseriscireato
displayName: "Campi Editabili LoadInserisciReato"
category: "GENERAL"
tags: []
---

# Campi_Editabili_LoadInserisciReato

## Campi editabili

| Sezione                         | Etichetta campo      | Nome campo (name)              | Tipo     | Obbligatorio   | Note obbligatorietà                                                |
|:--------------------------------|:---------------------|:-------------------------------|:---------|:---------------|:-------------------------------------------------------------------|
| Reato                           | Numero Reato         | CAMPO_PROGR_NUMERO_MANUALE     | text     | nan            | nan                                                                |
| Riferimenti normativi (5 righe) | Fonte                | CAMPO_COD_FONTE                | select   | *              | Almeno una coppia Fonte+Articolo deve essere valorizzata           |
| Riferimenti normativi (5 righe) | Anno                 | CAMPO_ANNO_FONTE               | text     | nan            | nan                                                                |
| Riferimenti normativi (5 righe) | Numero               | CAMPO_NUMERO_FONTE             | text     | nan            | nan                                                                |
| Riferimenti normativi (5 righe) | Articolo             | CAMPO_ARTICOLO                 | text     | *              | Almeno una coppia Fonte+Articolo deve essere valorizzata           |
| Riferimenti normativi (5 righe) | Art. qualificante    | CAMPO_COD_SOTTONUMERAZIONE     | select   | nan            | nan                                                                |
| Riferimenti normativi (5 righe) | Comma                | CAMPO_COMMA                    | text     | *              | Obbligatorio se valorizzato Comma qualificante                     |
| Riferimenti normativi (5 righe) | Comma qualificante   | CAMPO_COMMA_QUALIFICANTE       | select   | nan            | nan                                                                |
| Riferimenti normativi (5 righe) | Lettera              | CAMPO_LETTERA                  | text     | nan            | nan                                                                |
| Riferimenti normativi (5 righe) | Numero               | CAMPO_NUMERO                   | text     | nan            | nan                                                                |
| Checkbox cablati2               | 110 CP               | cablati2                       | checkbox | nan            | nan                                                                |
| Checkbox cablati2               | 56 CP                | cablati2                       | checkbox | nan            | nan                                                                |
| Checkbox cablati2               | 81 CP C1             | cablati2                       | checkbox | nan            | nan                                                                |
| Checkbox cablati2               | 81 CP C2             | cablati2                       | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N1             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N2             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N3             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N4             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N5             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N6             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N7             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N8             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N9             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N10            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N11            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 112 CP C1            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 112 CP C2            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 112 CP C3            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 112 CP C4            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 113 CP               | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 114 CP               | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 116 CP               | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 117 CP               | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N1            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N2            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N3            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N4            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N5            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N6            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N7            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N8            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N9            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N10           | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N11           | cablati                        | checkbox | nan            | nan                                                                |
| Dettaglio reato                 | Tipo Reato           | CAMPO_COD_TIPO_REATO           | select   | nan            | nan                                                                |
| Dettaglio reato                 | Luogo Reato          | CAMPO_DESC_LUOGO               | text     | nan            | Se valorizzato, è obbligatorio indicare anche Periodo Consumazione |
| Dettaglio reato                 | Periodo Consumazione | CAMPO_COD_PERIODO_CONSUMAZIONE | select   | *              | Obbligatorio se è valorizzato Luogo Reato o una delle date         |
| Date                            | Data1 - Giorno       | CAMPO_GIORNO_DATA_INIZIO       | text     | *              | Obbligatorio in base al valore di Periodo Consumazione             |
| Date                            | Data1 - Mese         | CAMPO_MESE_DATA_INIZIO         | text     | nan            | nan                                                                |
| Date                            | Data1 - Anno         | CAMPO_ANNO_DATA_INIZIO         | text     | *              | Obbligatorio in base al valore di Periodo Consumazione             |
| Date                            | Data2 - Giorno       | CAMPO_GIORNO_DATA_FINE         | text     | nan            | nan                                                                |
| Date                            | Data2 - Mese         | CAMPO_MESE_DATA_FINE           | text     | nan            | nan                                                                |
| Date                            | Data2 - Anno         | CAMPO_ANNO_DATA_FINE           | text     | *              | Obbligatorio in base al valore di Periodo Consumazione             |
| Dettaglio reato                 | Note                 | CAMPO_NOTE                     | textarea | nan            | nan                                                                |