---
uniqueName: loadinseriscinotiziareatocampi
displayName: "LoadInserisciNotiziaReato campi"
category: "GENERAL"
tags: []
---

# LoadInserisciNotiziaReato_campi

## LoadInserisciNotiziaReato_campi

| Campo                        | Obbligatorio   | Tipo       | Sezione            | Note                                                       |
|:-----------------------------|:---------------|:-----------|:-------------------|:-----------------------------------------------------------|
| Giorno Data Pervenimento     | nan            | input text | Dati Notizia Reato | Campo data (dd)                                            |
| Mese Data Pervenimento       | nan            | input text | Dati Notizia Reato | Campo data (MM)                                            |
| Anno Data Pervenimento       | nan            | input text | Dati Notizia Reato | Campo data (yyyy)                                          |
| Giorno Data Acquisizione     | nan            | input text | Dati Notizia Reato | Campo data (dd)                                            |
| Mese Data Acquisizione       | nan            | input text | Dati Notizia Reato | Campo data (MM)                                            |
| Anno Data Acquisizione       | nan            | input text | Dati Notizia Reato | Campo data (yyyy)                                          |
| Acquisizione Diretta         | nan            | select     | Dati Notizia Reato | Selezione da combo                                         |
| Giorno Data Fatto            | *              | input text | Dati Notizia Reato | Obbligatorio (campo mostrato con asterisco in pagina)      |
| Mese Data Fatto              | *              | input text | Dati Notizia Reato | Parte della Data Fatto obbligatoria                        |
| Anno Data Fatto              | *              | input text | Dati Notizia Reato | Parte della Data Fatto obbligatoria                        |
| Descrizione Fonte            | nan            | input text | Dati Notizia Reato | nan                                                        |
| Comune Fonte                 | *              | input text | Dati Notizia Reato | Obbligatorio                                               |
| Numero Registro Autorità     | nan            | input text | Dati Notizia Reato | nan                                                        |
| Luogo Provenienza            | nan            | input text | Dati Notizia Reato | nan                                                        |
| Numero Ricevuta              | nan            | input text | Dati Notizia Reato | nan                                                        |
| Giorno Data Arresto          | nan            | input text | Dati Notizia Reato | Campo data (dd)                                            |
| Mese Data Arresto            | nan            | input text | Dati Notizia Reato | Campo data (MM)                                            |
| Anno Data Arresto            | nan            | input text | Dati Notizia Reato | Campo data (yyyy)                                          |
| Giorno Data Fermo            | nan            | input text | Dati Notizia Reato | Campo data (dd)                                            |
| Mese Data Fermo              | nan            | input text | Dati Notizia Reato | Campo data (MM)                                            |
| Anno Data Fermo              | nan            | input text | Dati Notizia Reato | Campo data (yyyy)                                          |
| Fotosegnalato                | nan            | select     | Fotosegnalazione   | Se S rende obbligatori i campi del blocco Fotosegnalazione |
| Giorno Data Fotosegnalazione | *              | input text | Fotosegnalazione   | Obbligatorio se Fotosegnalato=S                            |
| Mese Data Fotosegnalazione   | *              | input text | Fotosegnalazione   | Obbligatorio se Fotosegnalato=S                            |
| Anno Data Fotosegnalazione   | *              | input text | Fotosegnalazione   | Obbligatorio se Fotosegnalato=S                            |
| Autorità Fotosegnalazione    | *              | select     | Fotosegnalazione   | Obbligatorio se Fotosegnalato=S                            |
| Comune Fotosegnalazione      | *              | input text | Fotosegnalazione   | Obbligatorio se Fotosegnalato=S                            |