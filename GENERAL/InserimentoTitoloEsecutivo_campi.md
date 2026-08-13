---
uniqueName: inserimentotitoloesecutivocampi
displayName: "InserimentoTitoloEsecutivo campi"
category: "GENERAL"
tags: []
---

# InserimentoTitoloEsecutivo_campi

## MainInserimentoTitolo_campi

| Campo                                 | Obbligatorio   | Tipo       | Sezione                 | Note                                                                   | Unnamed: 5                                            |
|:--------------------------------------|:---------------|:-----------|:------------------------|:-----------------------------------------------------------------------|:------------------------------------------------------|
| Anno R.G.N.R.                         | *              | input text | Dati generali           | Parte di "Anno/Numero R.G.N.R."                                        | nan                                                   |
| Numero R.G.N.R.                       | *              | input text | Dati generali           | Parte di "Anno/Numero R.G.N.R."                                        | nan                                                   |
| Anno Reg.Gen.                         | nan            | input text | Dati generali           | Parte di "Anno/Numero Reg.Gen."                                        | nan                                                   |
| Numero Reg.Gen.                       | nan            | input text | Dati generali           | Parte di "Anno/Numero Reg.Gen."                                        | nan                                                   |
| Tipo Registro Generale                | *              | select     | Dati generali           | Obbligatorio da controllo JavaScript Verify()                          | nan                                                   |
| Sede PM                               | *              | input text | Dati generali           | Marcato con (*) in pagina                                              | talvolta readonly poiché già preinserito nella pagina |
| Giorno Data Sentenza                  | *              | input text | Sentenza da Eseguire    | Parte di "Data Sentenza"                                               | nan                                                   |
| Mese Data Sentenza                    | *              | input text | Sentenza da Eseguire    | Parte di "Data Sentenza"                                               | nan                                                   |
| Anno Data Sentenza                    | *              | input text | Sentenza da Eseguire    | Parte di "Data Sentenza"                                               | nan                                                   |
| Anno Sentenza                         | *              | input text | Sentenza da Eseguire    | Parte di "Anno/Numero Sentenza"                                        | nan                                                   |
| Numero Sentenza                       | *              | input text | Sentenza da Eseguire    | Parte di "Anno/Numero Sentenza"                                        | nan                                                   |
| Autorità Emittente                    | *              | select     | Sentenza da Eseguire    | nan                                                                    | nan                                                   |
| Tipo Rito                             | nan            | select     | Sentenza da Eseguire    | Visibile solo per alcune autorità emittenti                            | nan                                                   |
| Luogo Emittente                       | *              | input text | Sentenza da Eseguire    | nan                                                                    | nan                                                   |
| Sezione Autorità Emittente            | nan            | input text | Sentenza da Eseguire    | nan                                                                    | nan                                                   |
| Tipo Provvedimento                    | nan            | select     | Altro Grado di Giudizio | nan                                                                    | nan                                                   |
| Tipo Sentenza                         | nan            | select     | Altro Grado di Giudizio | Condizionalmente obbligatorio se si compila la sentenza di riferimento | nan                                                   |
| Giorno Data Sentenza di Riferimento   | nan            | input text | Altro Grado di Giudizio | Condizionalmente obbligatorio se si compila la sentenza di riferimento | nan                                                   |
| Mese Data Sentenza di Riferimento     | nan            | input text | Altro Grado di Giudizio | Condizionalmente obbligatorio se si compila la sentenza di riferimento | nan                                                   |
| Anno Data Sentenza di Riferimento     | nan            | input text | Altro Grado di Giudizio | Condizionalmente obbligatorio se si compila la sentenza di riferimento | nan                                                   |
| Anno Sentenza/Ordinanza Riferimento   | nan            | input text | Altro Grado di Giudizio | nan                                                                    | nan                                                   |
| Numero Sentenza/Ordinanza Riferimento | nan            | input text | Altro Grado di Giudizio | nan                                                                    | nan                                                   |
| Autorità Sentenza Riferimento         | nan            | select     | Altro Grado di Giudizio | Condizionalmente obbligatorio se si compila la sentenza di riferimento | nan                                                   |
| Tipo Rito Riferimento                 | nan            | select     | Altro Grado di Giudizio | Visibile solo per alcune autorità emittenti                            | nan                                                   |
| Luogo Sentenza Riferimento            | nan            | input text | Altro Grado di Giudizio | Condizionalmente obbligatorio se si compila la sentenza di riferimento | nan                                                   |
| Sezione Autorità Riferimento          | nan            | input text | Altro Grado di Giudizio | nan                                                                    | nan                                                   |
| Tipo Provvedimento Cassazione         | nan            | select     | Decisione Cassazione    | nan                                                                    | nan                                                   |
| Anno Re.Ge. Cassazione                | nan            | input text | Decisione Cassazione    | Campo name=ANNOREGECAS                                                 | nan                                                   |
| Numero Re.Ge. Cassazione              | nan            | input text | Decisione Cassazione    | Campo name=NUMREGECAS                                                  | nan                                                   |
| Anno Sentenza Cassazione              | nan            | input text | Decisione Cassazione    | nan                                                                    | nan                                                   |
| Numero Sentenza Cassazione            | nan            | input text | Decisione Cassazione    | nan                                                                    | nan                                                   |
| Anno Raccolta Generale                | nan            | input text | Decisione Cassazione    | nan                                                                    | nan                                                   |
| Numero Raccolta Generale              | nan            | input text | Decisione Cassazione    | nan                                                                    | nan                                                   |
| Dispositivo Cassazione                | nan            | select     | Decisione Cassazione    | nan                                                                    | nan                                                   |
| Note                                  | nan            | textarea   | Note Aggiuntive         | nan                                                                    | nan                                                   |