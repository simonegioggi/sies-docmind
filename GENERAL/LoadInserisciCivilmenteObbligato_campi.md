---
uniqueName: loadinseriscicivilmenteobbligatocampi
displayName: "LoadInserisciCivilmenteObbligato campi"
category: "GENERAL"
tags: []
---

# LoadInserisciCivilmenteObbligato_campi

## LoadInserisciCivilmenteObbligat

| Campo                                             | Obbligatorio   | Tipo       | Sezione                                 | Note                                                                              |
|:--------------------------------------------------|:---------------|:-----------|:----------------------------------------|:----------------------------------------------------------------------------------|
| Tipologia Persona (Fisica/Giuridica)              | *              | radio      | Selezione iniziale                      | Visibile solo in modalità inserimento (modalita = I)                              |
| Qualifica                                         | nan            | select     | Persona Fisica                          | Se valorizzata mostra la sezione "Eventuale Seconda Persona Civilmente Obbligata" |
| Cognome                                           | *              | input text | Persona Fisica                          | Obbligatorio                                                                      |
| Nome                                              | *              | input text | Persona Fisica                          | Obbligatorio                                                                      |
| Sesso                                             | *              | select     | Persona Fisica                          | Obbligatorio                                                                      |
| Giorno Data di Nascita                            | *              | input text | Persona Fisica                          | Obbligatorio                                                                      |
| Mese Data di Nascita                              | *              | input text | Persona Fisica                          | Obbligatorio                                                                      |
| Anno Data di Nascita                              | *              | input text | Persona Fisica                          | Obbligatorio                                                                      |
| Comune di Nascita                                 | *              | input text | Persona Fisica                          | Obbligatorio se Stato di Nascita = Italia (039)                                   |
| Stato di Nascita                                  | nan            | select     | Persona Fisica                          | nan                                                                               |
| Comune di Nascita Estero                          | nan            | input text | Persona Fisica                          | Usato quando Stato di Nascita diverso da Italia                                   |
| Codice Fiscale                                    | nan            | input text | Persona Fisica                          | Validazione alfanumerica                                                          |
| Pec                                               | nan            | input text | Persona Fisica                          | nan                                                                               |
| Email                                             | nan            | input text | Persona Fisica                          | nan                                                                               |
| Indirizzo                                         | nan            | input text | Residenza/Domicilio Persona Fisica      | nan                                                                               |
| Comune di Residenza (Luogo)                       | *              | input text | Residenza/Domicilio Persona Fisica      | Obbligatorio se Stato di Residenza = Italia (039)                                 |
| CAP                                               | nan            | input text | Residenza/Domicilio Persona Fisica      | Validazione numerica                                                              |
| Comune Estero                                     | nan            | input text | Residenza/Domicilio Persona Fisica      | Usato quando Stato di Residenza diverso da Italia                                 |
| Stato di Residenza                                | nan            | select     | Residenza/Domicilio Persona Fisica      | nan                                                                               |
| Cognome Seconda Persona Civilmente Obbligata      | *              | input text | Seconda Persona Civilmente Obbligata    | Sezione condizionale (quando Qualifica diversa da '-')                            |
| Nome Seconda Persona Civilmente Obbligata         | *              | input text | Seconda Persona Civilmente Obbligata    | Sezione condizionale (quando Qualifica diversa da '-')                            |
| Sesso Seconda Persona Civilmente Obbligata        | *              | select     | Seconda Persona Civilmente Obbligata    | Sezione condizionale (quando Qualifica diversa da '-')                            |
| Giorno Data di Nascita Seconda Persona            | *              | input text | Seconda Persona Civilmente Obbligata    | Se compilati Cognome/Nome seconda persona                                         |
| Mese Data di Nascita Seconda Persona              | *              | input text | Seconda Persona Civilmente Obbligata    | Se compilati Cognome/Nome seconda persona                                         |
| Anno Data di Nascita Seconda Persona              | *              | input text | Seconda Persona Civilmente Obbligata    | Se compilati Cognome/Nome seconda persona                                         |
| Comune di Nascita Seconda Persona                 | *              | input text | Seconda Persona Civilmente Obbligata    | Obbligatorio se Stato di Nascita seconda persona = Italia (039)                   |
| Stato di Nascita Seconda Persona                  | nan            | select     | Seconda Persona Civilmente Obbligata    | nan                                                                               |
| Comune di Nascita Estero Seconda Persona          | nan            | input text | Seconda Persona Civilmente Obbligata    | nan                                                                               |
| Codice Fiscale Seconda Persona                    | nan            | input text | Seconda Persona Civilmente Obbligata    | Validazione alfanumerica non esplicita lato client per _ST                        |
| Pec Seconda Persona                               | nan            | input text | Seconda Persona Civilmente Obbligata    | nan                                                                               |
| Email Seconda Persona                             | nan            | input text | Seconda Persona Civilmente Obbligata    | nan                                                                               |
| Indirizzo Seconda Persona                         | nan            | input text | Residenza/Domicilio Seconda Persona     | nan                                                                               |
| Comune di Residenza Seconda Persona (Luogo)       | *              | input text | Residenza/Domicilio Seconda Persona     | Obbligatorio se Stato di Residenza seconda persona = Italia (039)                 |
| CAP Seconda Persona                               | nan            | input text | Residenza/Domicilio Seconda Persona     | nan                                                                               |
| Comune Estero Seconda Persona                     | nan            | input text | Residenza/Domicilio Seconda Persona     | nan                                                                               |
| Stato di Residenza Seconda Persona                | nan            | select     | Residenza/Domicilio Seconda Persona     | nan                                                                               |
| Qualifica                                         | nan            | select     | Persona Giuridica                       | nan                                                                               |
| Società                                           | *              | input text | Persona Giuridica                       | Obbligatorio                                                                      |
| Ragione Sociale                                   | nan            | select     | Persona Giuridica                       | nan                                                                               |
| Provincia                                         | nan            | select     | Persona Giuridica                       | nan                                                                               |
| Partita IVA/Codice Fiscale                        | nan            | input text | Persona Giuridica                       | Validazione alfanumerica                                                          |
| Sede Legale                                       | nan            | input text | Persona Giuridica                       | nan                                                                               |
| Sede Operativa/Indirizzo Attivita                 | nan            | input text | Persona Giuridica                       | nan                                                                               |
| Cognome Legale Rappresentante                     | *              | input text | Legale Rappresentante Persona Giuridica | Obbligatorio                                                                      |
| Nome Legale Rappresentante                        | *              | input text | Legale Rappresentante Persona Giuridica | Obbligatorio                                                                      |
| Sesso Legale Rappresentante                       | *              | select     | Legale Rappresentante Persona Giuridica | Obbligatorio                                                                      |
| Giorno Data di Nascita Legale Rappresentante      | *              | input text | Legale Rappresentante Persona Giuridica | Obbligatorio                                                                      |
| Mese Data di Nascita Legale Rappresentante        | *              | input text | Legale Rappresentante Persona Giuridica | Obbligatorio                                                                      |
| Anno Data di Nascita Legale Rappresentante        | *              | input text | Legale Rappresentante Persona Giuridica | Obbligatorio                                                                      |
| Comune di Nascita Legale Rappresentante           | *              | input text | Legale Rappresentante Persona Giuridica | Obbligatorio se Stato di Nascita = Italia (039)                                   |
| Stato di Nascita Legale Rappresentante            | nan            | select     | Legale Rappresentante Persona Giuridica | nan                                                                               |
| Comune di Nascita Estero Legale Rappresentante    | nan            | input text | Legale Rappresentante Persona Giuridica | nan                                                                               |
| Codice Fiscale Legale Rappresentante              | nan            | input text | Legale Rappresentante Persona Giuridica | nan                                                                               |
| Pec Legale Rappresentante                         | nan            | input text | Legale Rappresentante Persona Giuridica | nan                                                                               |
| Email Legale Rappresentante                       | nan            | input text | Legale Rappresentante Persona Giuridica | nan                                                                               |
| Indirizzo Legale Rappresentante                   | nan            | input text | Residenza/Domicilio Persona Giuridica   | nan                                                                               |
| Comune di Residenza Legale Rappresentante (Luogo) | *              | input text | Residenza/Domicilio Persona Giuridica   | Obbligatorio se Stato di Residenza = Italia (039)                                 |
| CAP Residenza Legale Rappresentante               | nan            | input text | Residenza/Domicilio Persona Giuridica   | Validazione numerica                                                              |
| Comune Estero Residenza Legale Rappresentante     | nan            | input text | Residenza/Domicilio Persona Giuridica   | nan                                                                               |
| Stato di Residenza Legale Rappresentante          | nan            | select     | Residenza/Domicilio Persona Giuridica   | nan                                                                               |