---
uniqueName: loadinseriscimisuracautelarecessatecomputabilicamp
displayName: "LoadInserisciMisuraCautelareCessateComputabili campi"
category: "GENERAL"
tags: []
---

# LoadInserisciMisuraCautelareCessateComputabili_campi

## LoadInserisciMisuraCautelareCes

| Campo                                                  | Obbligatorio   | Tipo                        | Sezione                   | Note                                                  |
|:-------------------------------------------------------|:---------------|:----------------------------|:--------------------------|:------------------------------------------------------|
| Anno/Numero RG.N.R. - Anno                             | nan            | input text                  | Dati procedimento         | nan                                                   |
| Anno/Numero RG.N.R. - Numero                           | nan            | input text                  | Dati procedimento         | nan                                                   |
| Tipo Ufficio PM                                        | *              | select                      | Dati procedimento         | Controllo obbligatorietà in VerifyAltreBDI()          |
| Sede PM                                                | *              | input text                  | Dati procedimento         | Compilabile con popup ListaUfficiComuni               |
| Anno/Numero B.D.M.C. - Anno                            | nan            | input text                  | Dati procedimento         | nan                                                   |
| Anno/Numero B.D.M.C. - Numero                          | nan            | input text                  | Dati procedimento         | nan                                                   |
| Anno/Numero Reg. Gen. - Anno                           | nan            | input text                  | Dati procedimento         | nan                                                   |
| Anno/Numero Reg. Gen. - Numero                         | nan            | input text                  | Dati procedimento         | nan                                                   |
| Tipo Ufficio Reg. Gen.                                 | nan            | select                      | Dati procedimento         | nan                                                   |
| Autorità Emittente                                     | *              | select                      | Provvedimento             | Controllo obbligatorietà in VerifyAltreBDI()          |
| Luogo Autorità Emittente                               | nan            | input text                  | Provvedimento             | Compilabile con popup ListaUfficiPerTipo              |
| Data emissione ordinanza - Giorno                      | nan            | input text                  | Provvedimento             | nan                                                   |
| Data emissione ordinanza - Mese                        | nan            | input text                  | Provvedimento             | nan                                                   |
| Data emissione ordinanza - Anno                        | nan            | input text                  | Provvedimento             | nan                                                   |
| Espiazione pena (istituto di detenzione / altro luogo) | nan            | radio                       | Tipologia espiazione      | Selezione modalità                                    |
| Misura cautelare non detentiva                         | *              | select                      | Tipologia espiazione      | Obbligatoria in alternativa alla misura detentiva     |
| Misura cautelare detentiva                             | *              | select                      | Tipologia espiazione      | Obbligatoria in alternativa alla misura non detentiva |
| Data misura "Da" - Giorno                              | *              | input text                  | Periodo misura            | Controllo obbligatorietà in VerifyAltreBDI()          |
| Data misura "Da" - Mese                                | *              | input text                  | Periodo misura            | Controllo obbligatorietà in VerifyAltreBDI()          |
| Data misura "Da" - Anno                                | *              | input text                  | Periodo misura            | Controllo obbligatorietà in VerifyAltreBDI()          |
| Data misura "A" - Giorno                               | *              | input text                  | Periodo misura            | Controllo obbligatorietà in VerifyAltreBDI()          |
| Data misura "A" - Mese                                 | *              | input text                  | Periodo misura            | Controllo obbligatorietà in VerifyAltreBDI()          |
| Data misura "A" - Anno                                 | *              | input text                  | Periodo misura            | Controllo obbligatorietà in VerifyAltreBDI()          |
| Istituto di Detenzione                                 | nan            | input text (readonly+popup) | Espiazione in istituto    | Valorizzabile tramite popup ListaIstitutoDetenzione   |
| Luogo di espiazione                                    | nan            | textarea                    | Espiazione in altro luogo | nan                                                   |
| Autorità competente per territorio                     | nan            | select                      | Espiazione in altro luogo | nan                                                   |
| Sede autorità competente                               | nan            | input text                  | Espiazione in altro luogo | Compilabile con popup ListaComuni                     |
| Indirizzo autorità competente                          | nan            | textarea                    | Espiazione in altro luogo | nan                                                   |