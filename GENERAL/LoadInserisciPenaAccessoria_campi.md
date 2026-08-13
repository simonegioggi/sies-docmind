---
uniqueName: loadinseriscipenaaccessoriacampi
displayName: "LoadInserisciPenaAccessoria campi"
category: "GENERAL"
tags: []
---

# LoadInserisciPenaAccessoria_campi

## LoadInserisciPenaAccessoria_cam

| Campo                                     | Obbligatorio   | Tipo       | Sezione                                                        | Note                                                                     |
|:------------------------------------------|:---------------|:-----------|:---------------------------------------------------------------|:-------------------------------------------------------------------------|
| Tipo di Pena Accessoria                   | *              | select     | Generale                                                       | Obbligatorio sempre (validazione req)                                    |
| Descrizione Altre P.A.                    | nan            | input text | Generale                                                       | Visibile/editabile quando Tipo di Pena Accessoria = "Altre" (codice 999) |
| Tipo Durata                               | nan            | select     | Generale                                                       | nan                                                                      |
| Anni Durata                               | nan            | input text | Durata                                                         | nan                                                                      |
| Mesi Durata                               | nan            | input text | Durata                                                         | nan                                                                      |
| Giorni Durata                             | nan            | input text | Durata                                                         | nan                                                                      |
| Giorno Data Fine Validità                 | nan            | input text | Data Fine Validità                                             | nan                                                                      |
| Mese Data Fine Validità                   | nan            | input text | Data Fine Validità                                             | nan                                                                      |
| Anno Data Fine Validità                   | nan            | input text | Data Fine Validità                                             | nan                                                                      |
| Giorno Data Ordinanza GE                  | nan            | input text | Estremi Ordinanza Applicazione del GE                          | nan                                                                      |
| Mese Data Ordinanza GE                    | nan            | input text | Estremi Ordinanza Applicazione del GE                          | nan                                                                      |
| Anno Data Ordinanza GE                    | nan            | input text | Estremi Ordinanza Applicazione del GE                          | nan                                                                      |
| Anno Ordinanza GE                         | nan            | input text | Estremi Ordinanza Applicazione del GE                          | nan                                                                      |
| Numero Ordinanza GE                       | nan            | input text | Estremi Ordinanza Applicazione del GE                          | nan                                                                      |
| Autorità Ordinanza GE                     | nan            | select     | Estremi Ordinanza Applicazione del GE                          | nan                                                                      |
| Luogo Ordinanza GE                        | nan            | input text | Estremi Ordinanza Applicazione del GE                          | Valorizzabile anche da lookup comuni                                     |
| Tenore                                    | nan            | select     | Estremi Ordinanza Condono/Revoca/Sostituzione/Depenalizzazione | nan                                                                      |
| Giorno Data Ordinanza PA                  | nan            | input text | Estremi Ordinanza Condono/Revoca/Sostituzione/Depenalizzazione | nan                                                                      |
| Mese Data Ordinanza PA                    | nan            | input text | Estremi Ordinanza Condono/Revoca/Sostituzione/Depenalizzazione | nan                                                                      |
| Anno Data Ordinanza PA                    | nan            | input text | Estremi Ordinanza Condono/Revoca/Sostituzione/Depenalizzazione | nan                                                                      |
| Anno Ordinanza PA                         | nan            | input text | Estremi Ordinanza Condono/Revoca/Sostituzione/Depenalizzazione | nan                                                                      |
| Numero Ordinanza PA                       | nan            | input text | Estremi Ordinanza Condono/Revoca/Sostituzione/Depenalizzazione | nan                                                                      |
| Autorità Emittente PA                     | nan            | select     | Estremi Ordinanza Condono/Revoca/Sostituzione/Depenalizzazione | nan                                                                      |
| Luogo Ordinanza PA                        | nan            | input text | Estremi Ordinanza Condono/Revoca/Sostituzione/Depenalizzazione | Valorizzabile anche da lookup comuni                                     |
| Fonte                                     | nan            | select     | Estremi Condono/Depenalizzazione/Amnistia                      | nan                                                                      |
| Anno Fonte                                | nan            | input text | Estremi Condono/Depenalizzazione/Amnistia                      | nan                                                                      |
| Numero Fonte                              | nan            | input text | Estremi Condono/Depenalizzazione/Amnistia                      | nan                                                                      |
| Articolo Fonte                            | nan            | input text | Estremi Condono/Depenalizzazione/Amnistia                      | nan                                                                      |
| Art.qualificante                          | nan            | select     | Estremi Condono/Depenalizzazione/Amnistia                      | nan                                                                      |
| Comma                                     | nan            | input text | Estremi Condono/Depenalizzazione/Amnistia                      | nan                                                                      |
| Lettera                                   | nan            | input text | Estremi Condono/Depenalizzazione/Amnistia                      | nan                                                                      |
| Numero (articolo)                         | nan            | input text | Estremi Condono/Depenalizzazione/Amnistia                      | nan                                                                      |
| Tipo di Pena Accessoria (in sostituzione) | *              | select     | Estremi Pena Accessoria in Sostituzione                        | Obbligatorio se Tenore = "S" o "T"                                       |
| Revoca Condono                            | nan            | checkbox   | Revoca Condono                                                 | nan                                                                      |
| Giorno Data Sentenza Revoca               | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Mese Data Sentenza Revoca                 | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Anno Data Sentenza Revoca                 | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Anno Sentenza Revoca                      | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Numero Sentenza Revoca                    | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Autorità Sentenza Revoca                  | nan            | select     | Revoca Condono                                                 | nan                                                                      |
| Luogo Sentenza Revoca                     | nan            | input text | Revoca Condono                                                 | Valorizzabile anche da lookup comuni                                     |
| Anno Re.Ge. PM Revoca                     | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Numero Re.Ge. PM Revoca                   | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Anno Re.Ge. GIP Revoca                    | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Numero Re.Ge. GIP Revoca                  | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Anno Re.Ge. DIB Revoca                    | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Numero Re.Ge. DIB Revoca                  | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Anno Re.Ge. CAS Revoca                    | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Numero Re.Ge. CAS Revoca                  | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Anno Re.Ge. CAP Revoca                    | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Numero Re.Ge. CAP Revoca                  | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Anno Re.Ge. CASAP Revoca                  | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Numero Re.Ge. CASAP Revoca                | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Falsità di documenti                      | nan            | checkbox   | Revoca Condono                                                 | nan                                                                      |
| Note                                      | nan            | textarea   | Revoca Condono                                                 | nan                                                                      |