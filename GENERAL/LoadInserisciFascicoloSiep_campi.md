---
uniqueName: loadinseriscifascicolosiepcampi
displayName: "LoadInserisciFascicoloSiep campi"
category: "GENERAL"
tags: []
---

# LoadInserisciFascicoloSiep_campi

## LoadInserisciFascicoloSiep_camp

| Campo                                      | Obbligatorio   | Tipo       | Sezione              | Note                                                                    |
|:-------------------------------------------|:---------------|:-----------|:---------------------|:------------------------------------------------------------------------|
| Giorno Data Iscrizione Procedimento        | *              | input text | Dati procedimento    | Obbligatorio in assegnazione manuale, hidden in assegnazione automatica |
| Mese Data Iscrizione Procedimento          | *              | input text | Dati procedimento    | Obbligatorio in assegnazione manuale, hidden in assegnazione automatica |
| Anno Data Iscrizione Procedimento          | *              | input text | Dati procedimento    | Obbligatorio in assegnazione manuale, hidden in assegnazione automatica |
| Giorno Data Arrivo Atto                    | nan            | input text | Dati procedimento    | Data validata da JavaScript                                             |
| Mese Data Arrivo Atto                      | nan            | input text | Dati procedimento    | Data validata da JavaScript                                             |
| Anno Data Arrivo Atto                      | nan            | input text | Dati procedimento    | Data validata da JavaScript                                             |
| Giorno Data IrrevocabilitÃ  / Esecutivo il | nan            | input text | Dati procedimento    | Data validata da JavaScript                                             |
| Mese Data IrrevocabilitÃ  / Esecutivo il   | nan            | input text | Dati procedimento    | Data validata da JavaScript                                             |
| Anno Data IrrevocabilitÃ  / Esecutivo il   | nan            | input text | Dati procedimento    | Data validata da JavaScript                                             |
| Anno Procedimento                          | *              | input text | Assegnazione manuale | Obbligatorio solo se assegnazione_manuale = S                           |
| Numero Procedimento                        | *              | input text | Assegnazione manuale | Obbligatorio solo se assegnazione_manuale = S                           |
| Assegna numerazione speciale               | nan            | checkbox   | Assegnazione manuale | Mostra azioni R.E.S. / P.T. e disabilita anno/numero procedimento       |
| Classe I                                   | nan            | radio      | Classe procedimento  | Opzione radio gruppo tipo                                               |
| Classe II                                  | nan            | radio      | Classe procedimento  | Opzione radio gruppo tipo                                               |
| Classe III                                 | nan            | radio      | Classe procedimento  | Opzione radio gruppo tipo                                               |
| Classe IV                                  | nan            | radio      | Classe procedimento  | Opzione radio gruppo tipo                                               |
| Classe V                                   | nan            | radio      | Classe procedimento  | Opzione radio gruppo tipo                                               |
| Classe VI                                  | nan            | radio      | Classe procedimento  | Opzione radio gruppo tipo                                               |
| Classe VII                                 | nan            | radio      | Classe procedimento  | Opzione radio gruppo tipo                                               |
| Note Procedimento                          | nan            | textarea   | Note                 | nan                                                                     |