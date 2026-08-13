---
uniqueName: loadinseriscicircostanzacampi
displayName: "LoadInserisciCircostanza campi"
category: "GENERAL"
tags: []
---

# LoadInserisciCircostanza_campi

## LoadInserisciCircostanza_campi

| Campo                                 | Obbligatorio   | Tipo       | Sezione              | Note                                                                               |
|:--------------------------------------|:---------------|:-----------|:---------------------|:-----------------------------------------------------------------------------------|
| Fonte (riga 1-5)                      | *              | select     | Definizione articolo | Obbligatorio con Articolo: se uno dei due è valorizzato deve esserci anche l'altro |
| Anno Fonte (riga 1-5)                 | nan            | input text | Definizione articolo | Numerico (4 cifre), compilabile solo se presente la coppia Fonte/Articolo          |
| Numero Fonte (riga 1-5)               | nan            | input text | Definizione articolo | Alfanumerico, compilabile solo se presente la coppia Fonte/Articolo                |
| Articolo (riga 1-5)                   | *              | input text | Definizione articolo | Obbligatorio con Fonte: se uno dei due è valorizzato deve esserci anche l'altro    |
| Articolo qualificante (riga 1-5)      | nan            | select     | Definizione articolo | Compilabile solo se presente la coppia Fonte/Articolo                              |
| Comma (riga 1-5)                      | *              | input text | Definizione articolo | Obbligatorio se Comma qualificante è valorizzato                                   |
| Comma qualificante (riga 1-5)         | nan            | select     | Definizione articolo | Se valorizzato richiede Comma                                                      |
| Lettera (riga 1-5)                    | nan            | input text | Definizione articolo | Compilabile solo se presente la coppia Fonte/Articolo                              |
| Numero (riga 1-5)                     | nan            | input text | Definizione articolo | Compilabile solo se presente la coppia Fonte/Articolo                              |
| 99 CP C1                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 99 CP C2 N1                           | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 99 CP C2 N2                           | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 99 CP C2 N3                           | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 99 CP C3                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 99 CP C4                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 102 CP                                | nan            | checkbox   | Circostanze cablate  | Checkbox                                                                           |
| 103 CP                                | nan            | checkbox   | Circostanze cablate  | Checkbox                                                                           |
| 104 CP                                | nan            | checkbox   | Circostanze cablate  | Checkbox                                                                           |
| 105 CP                                | nan            | checkbox   | Circostanze cablate  | Checkbox                                                                           |
| 108 CP                                | nan            | checkbox   | Circostanze cablate  | Checkbox                                                                           |
| 62 CP N1                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 62 CP N2                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 62 CP N3                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 62 CP N4                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 62 CP N5                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 62 CP N6                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 62 BIS CP                             | nan            | checkbox   | Circostanze cablate  | Checkbox                                                                           |
| Sentenza di applicazione pena         | nan            | checkbox   | Campi comuni         | In modifica può risultare non editabile (renderizzato come hidden)                 |
| Bilanciamento circostanze             | nan            | select     | Campi comuni         | In modifica può risultare non editabile (renderizzato come hidden)                 |
| Annotazioni Bilanciamento circostanze | nan            | textarea   | Campi comuni         | nan                                                                                |
| Giudizio abbreviato                   | nan            | checkbox   | Campi comuni         | In modifica può risultare non editabile (renderizzato come hidden)                 |