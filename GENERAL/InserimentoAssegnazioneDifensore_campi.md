---
uniqueName: inserimentoassegnazionedifensorecampi
displayName: "InserimentoAssegnazioneDifensore campi"
category: "GENERAL"
tags: []
---

# InserimentoAssegnazioneDifensore_campi

## InserimentoAssegnazioneDifensor

| Campo                                           | Obbligatorio   | Tipo                             | Sezione                            | Note                                                                |
|:------------------------------------------------|:---------------|:---------------------------------|:-----------------------------------|:--------------------------------------------------------------------|
| Cognome                                         | *              | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Nome                                            | *              | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Comune di Nascita                               | *              | input text + popup comuni        | Dati difensore                     | Obbligatorio se Stato di Nascita = Italia (in inserimento manuale)  |
| Stato di Nascita                                | nan            | select                           | Dati difensore                     | Disabled di default, editabile in inserimento manuale (non reginde) |
| Luogo di Nascita Estero                         | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Giorno Data di nascita                          | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Mese Data di nascita                            | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Anno Data di nascita                            | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Foro                                            | *              | select                           | Dati difensore                     | Disabled di default, editabile in inserimento manuale (non reginde) |
| Indirizzo                                       | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Con Studio in                                   | nan            | input text + popup comuni        | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Telefono                                        | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Fax                                             | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| e-mail                                          | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| pec                                             | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Codice Fiscale                                  | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Stato Difensore                                 | nan            | select                           | Dati difensore                     | Disabled di default, editabile in inserimento manuale (non reginde) |
| Tipo Difensore                                  | *              | select                           | Dati difensore                     | Obbligatorio                                                        |
| Giorno Data di Nomina                           | nan            | input text                       | Nomina (Tipo Difensore = 02)       | Visibile per difensore di fiducia                                   |
| Mese Data di Nomina                             | nan            | input text                       | Nomina (Tipo Difensore = 02)       | Visibile per difensore di fiducia                                   |
| Anno Data di Nomina                             | nan            | input text                       | Nomina (Tipo Difensore = 02)       | Visibile per difensore di fiducia                                   |
| Giorno Data di Designazione                     | nan            | input text                       | Designazione (Tipo Difensore = 01) | Visibile per difensore d'ufficio                                    |
| Mese Data di Designazione                       | nan            | input text                       | Designazione (Tipo Difensore = 01) | Visibile per difensore d'ufficio                                    |
| Anno Data di Designazione                       | nan            | input text                       | Designazione (Tipo Difensore = 01) | Visibile per difensore d'ufficio                                    |
| Motivo della Designazione                       | *              | select                           | Designazione (Tipo Difensore = 01) | Obbligatorio se Tipo Difensore = 01                                 |
| Note                                            | nan            | textarea                         | Designazione (Tipo Difensore = 01) | Visibile solo se Motivo della Designazione = 0008                   |
| Autorità (notifica al Condannato)               | nan            | select                           | Autorità notifica al Condannato    | nan                                                                 |
| Sede (notifica al Condannato)                   | nan            | input text + popup comuni        | Autorità notifica al Condannato    | nan                                                                 |
| Indirizzo (notifica al Condannato)              | nan            | textarea                         | Autorità notifica al Condannato    | nan                                                                 |
| Istituto di Detenzione (notifica al Condannato) | nan            | popup lista istituti + hidden id | Autorità notifica al Condannato    | Valorizzato tramite popup                                           |
| Autorità (notifica al Difensore)                | nan            | select                           | Autorità notifica al Difensore     | nan                                                                 |
| Sede (notifica al Difensore)                    | nan            | input text + popup comuni        | Autorità notifica al Difensore     | nan                                                                 |