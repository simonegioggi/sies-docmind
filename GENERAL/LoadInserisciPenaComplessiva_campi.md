---
uniqueName: loadinseriscipenacomplessivacampi
displayName: "LoadInserisciPenaComplessiva campi"
category: "GENERAL"
tags: []
---

# LoadInserisciPenaComplessiva_campi

## LoadInserisciPenaComplessiva_ca

| Campo                                            |   Obbligatorio | Tipo         | Sezione                               | Note                                                                    |
|:-------------------------------------------------|---------------:|:-------------|:--------------------------------------|:------------------------------------------------------------------------|
| Anni Reclusione                                  |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Mesi Reclusione                                  |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Giorni Reclusione                                |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Intero Multa                                     |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Decimale Multa                                   |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Valuta Multa                                     |            nan | select       | Pena                                  | nan                                                                     |
| Anni Arresto                                     |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Mesi Arresto                                     |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Giorni Arresto                                   |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Intero Ammenda                                   |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Decimale Ammenda                                 |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Valuta Ammenda                                   |            nan | select       | Pena                                  | nan                                                                     |
| Ergastolo / Tipo Pena Detentiva                  |            nan | select       | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Anni Isolamento Diurno                           |            nan | input text   | Pena                                  | nan                                                                     |
| Mesi Isolamento Diurno                           |            nan | input text   | Pena                                  | nan                                                                     |
| Giorni Isolamento Diurno                         |            nan | input text   | Pena                                  | nan                                                                     |
| Giorno Data Prescrizione                         |            nan | input text   | Pena                                  | Data opzionale ma validata                                              |
| Mese Data Prescrizione                           |            nan | input text   | Pena                                  | Data opzionale ma validata                                              |
| Anno Data Prescrizione                           |            nan | input text   | Pena                                  | Data opzionale ma validata                                              |
| Sanzione Sostitutiva                             |            nan | checkbox     | Sanzione Sostitutiva                  | Se selezionata attiva obblighi condizionali                             |
| Tipo Sanzione Sostitutiva                        |            nan | select       | Sanzione Sostitutiva                  | Obbligatorio se checkbox Sanzione Sostitutiva selezionato               |
| Anni Sanzione Sostitutiva                        |            nan | input text   | Sanzione Sostitutiva                  | Obbligatorio in alternativa alla pena pecuniaria secondo il tipo scelto |
| Mesi Sanzione Sostitutiva                        |            nan | input text   | Sanzione Sostitutiva                  | Obbligatorio in alternativa alla pena pecuniaria secondo il tipo scelto |
| Giorni Sanzione Sostitutiva                      |            nan | input text   | Sanzione Sostitutiva                  | Obbligatorio in alternativa alla pena pecuniaria secondo il tipo scelto |
| Intero Pena Pecuniaria Sostitutiva Multa         |            nan | input text   | Sanzione Sostitutiva                  | Obbligatorio per tipo pecuniario se selezionata                         |
| Decimale Pena Pecuniaria Sostitutiva Multa       |            nan | input text   | Sanzione Sostitutiva                  | Obbligatorio per tipo pecuniario se selezionata                         |
| Valuta Pena Pecuniaria Sostitutiva Multa/Ammenda |            nan | select       | Sanzione Sostitutiva                  | nan                                                                     |
| Intero Pena Pecuniaria Sostitutiva Ammenda       |            nan | input text   | Sanzione Sostitutiva                  | Obbligatorio per tipo pecuniario se selezionata                         |
| Decimale Pena Pecuniaria Sostitutiva Ammenda     |            nan | input text   | Sanzione Sostitutiva                  | Obbligatorio per tipo pecuniario se selezionata                         |
| Pena Sostitutiva                                 |            nan | checkbox     | Pene sostitutive Pene Detentive Brevi | Se selezionata attiva obblighi condizionali                             |
| Tipo Pena Sostitutiva                            |            nan | select       | Pene sostitutive Pene Detentive Brevi | Obbligatorio se checkbox Pena Sostitutiva selezionato                   |
| Anni Pena Sostitutiva                            |            nan | input text   | Pene sostitutive Pene Detentive Brevi | Obbligatorio in alternativa alla pena pecuniaria secondo il tipo scelto |
| Mesi Pena Sostitutiva                            |            nan | input text   | Pene sostitutive Pene Detentive Brevi | Obbligatorio in alternativa alla pena pecuniaria secondo il tipo scelto |
| Giorni Pena Sostitutiva                          |            nan | input text   | Pene sostitutive Pene Detentive Brevi | Obbligatorio in alternativa alla pena pecuniaria secondo il tipo scelto |
| Intero Pena Pecuniaria Sostitutiva               |            nan | input text   | Pene sostitutive Pene Detentive Brevi | Obbligatorio per tipo pecuniario se selezionata                         |
| Decimale Pena Pecuniaria Sostitutiva             |            nan | input text   | Pene sostitutive Pene Detentive Brevi | Obbligatorio per tipo pecuniario se selezionata                         |
| Confisca per equivalente                         |            nan | checkbox     | Importo da Pagare Include             | nan                                                                     |
| Continuazione con altre sentenze                 |            nan | checkbox     | Continuazione                         | Se selezionata attiva 2 blocchi continuazione                           |
| Tipo Continuazione riga 1                        |            nan | input/select | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Anno Sentenza riga 1                             |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Numero Sentenza riga 1                           |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Giorno Data Sentenza riga 1                      |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Mese Data Sentenza riga 1                        |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Anno Data Sentenza riga 1                        |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Autorità Sentenza riga 1                         |            nan | select       | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Luogo Sentenza riga 1                            |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Anno R.G.N.R. riga 1                             |            nan | input text   | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Numero R.G.N.R. riga 1                           |            nan | input text   | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Anno Reg. Gen. riga 1                            |            nan | input text   | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Numero Reg. Gen. riga 1                          |            nan | input text   | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Tipo Reg. Gen. riga 1                            |            nan | select       | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Tipo Continuazione riga 2                        |            nan | input/select | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Anno Sentenza riga 2                             |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Numero Sentenza riga 2                           |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Giorno Data Sentenza riga 2                      |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Mese Data Sentenza riga 2                        |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Anno Data Sentenza riga 2                        |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Autorità Sentenza riga 2                         |            nan | select       | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Luogo Sentenza riga 2                            |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Anno R.G.N.R. riga 2                             |            nan | input text   | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Numero R.G.N.R. riga 2                           |            nan | input text   | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Anno Reg. Gen. riga 2                            |            nan | input text   | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Numero Reg. Gen. riga 2                          |            nan | input text   | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Tipo Reg. Gen. riga 2                            |            nan | select       | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |