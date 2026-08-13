---
uniqueName: loadinseriscimisuracautelarecessatenoncomputabilic
displayName: "LoadInserisciMisuraCautelareCessateNonComputabili campi"
category: "GENERAL"
tags: []
---

# LoadInserisciMisuraCautelareCessateNonComputabili_campi

## LoadInserisciMisuraCautelareCes

| Campo                                               | Obbligatorio   | Tipo                            | Sezione                   | Note                                                  |
|:----------------------------------------------------|:---------------|:--------------------------------|:--------------------------|:------------------------------------------------------|
| Anno RG.N.R.                                        | nan            | input text                      | Procedimento              | nan                                                   |
| Numero RG.N.R.                                      | nan            | input text                      | Procedimento              | nan                                                   |
| Tipo Ufficio PM                                     | *              | select                          | Procedimento              | nan                                                   |
| Sede Ufficio PM                                     | *              | input text                      | Procedimento              | nan                                                   |
| Anno B.D.M.C.                                       | nan            | input text                      | Procedimento              | nan                                                   |
| Numero B.D.M.C.                                     | nan            | input text                      | Procedimento              | nan                                                   |
| Anno Reg. Gen.                                      | nan            | input text                      | Procedimento              | nan                                                   |
| Numero Reg. Gen.                                    | nan            | input text                      | Procedimento              | nan                                                   |
| Tipo ufficio Reg. Gen.                              | nan            | select                          | Procedimento              | nan                                                   |
| Autorità Emittente                                  | *              | select                          | Autorità emittente        | nan                                                   |
| Luogo Autorità Emittente                            | nan            | input text                      | Autorità emittente        | nan                                                   |
| Giorno Data emissione Ordinanza                     | nan            | input text                      | Autorità emittente        | nan                                                   |
| Mese Data emissione Ordinanza                       | nan            | input text                      | Autorità emittente        | nan                                                   |
| Anno Data emissione Ordinanza                       | nan            | input text                      | Autorità emittente        | nan                                                   |
| Espiazione pena (istituto detenzione / altro luogo) | nan            | radio                           | Misura cautelare          | nan                                                   |
| Misura non detentiva                                | *              | select                          | Misura cautelare          | Obbligatorio in alternativa alla misura detentiva     |
| Misura detentiva                                    | *              | select                          | Misura cautelare          | Obbligatorio in alternativa alla misura non detentiva |
| Giorno Data inizio misura                           | *              | input text                      | Misura cautelare          | nan                                                   |
| Mese Data inizio misura                             | *              | input text                      | Misura cautelare          | nan                                                   |
| Anno Data inizio misura                             | *              | input text                      | Misura cautelare          | nan                                                   |
| Giorno Data fine misura                             | *              | input text                      | Misura cautelare          | nan                                                   |
| Mese Data fine misura                               | *              | input text                      | Misura cautelare          | nan                                                   |
| Anno Data fine misura                               | *              | input text                      | Misura cautelare          | nan                                                   |
| Istituto di Detenzione                              | nan            | input text (readonly con popup) | Espiazione in istituto    | Campo compilato tramite popup di selezione istituto   |
| Luogo di espiazione                                 | nan            | input text                      | Espiazione in altro luogo | nan                                                   |
| Autorità competente per territorio                  | nan            | select                          | Espiazione in altro luogo | nan                                                   |
| Sede autorità competente                            | nan            | input text                      | Espiazione in altro luogo | nan                                                   |
| Indirizzo autorità competente                       | nan            | textarea                        | Espiazione in altro luogo | nan                                                   |
| Motivo Non Computabilità                            | nan            | select                          | Non computabilità         | nan                                                   |
| Giorno Data provvedimento di Fungibilità            | nan            | input text                      | Non computabilità         | nan                                                   |
| Mese Data provvedimento di Fungibilità              | nan            | input text                      | Non computabilità         | nan                                                   |
| Anno Data provvedimento di Fungibilità              | nan            | input text                      | Non computabilità         | nan                                                   |
| Anno SIEP                                           | nan            | input text                      | Riferimento SIEP          | nan                                                   |
| Numero SIEP                                         | nan            | input text                      | Riferimento SIEP          | nan                                                   |
| Ufficio riferimento                                 | nan            | select                          | Riferimento SIEP          | nan                                                   |
| Sede riferimento                                    | nan            | input text                      | Riferimento SIEP          | nan                                                   |
| Note                                                | nan            | textarea                        | Note                      | nan                                                   |