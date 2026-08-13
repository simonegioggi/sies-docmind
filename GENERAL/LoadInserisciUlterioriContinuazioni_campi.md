---
uniqueName: loadinserisciulterioricontinuazionicampi
displayName: "LoadInserisciUlterioriContinuazioni campi"
category: "GENERAL"
tags: []
---

# LoadInserisciUlterioriContinuazioni_campi

## LoadInserisciUlterioriContinuaz

| Campo                    | Obbligatorio   | Tipo       | Sezione                          | Note                                                                                                        |
|:-------------------------|:---------------|:-----------|:---------------------------------|:------------------------------------------------------------------------------------------------------------|
| Tipo Continuazione (*)   | *              | select     | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio quando la riga è compilata o se sono valorizzati campi R.G.N.R./Reg.Gen. |
| Anno Sentenza (*)        | *              | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio quando la riga è compilata                                               |
| Numero Sentenza (*)      | *              | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio quando la riga è compilata                                               |
| Giorno Data Sentenza (*) | *              | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio quando la riga è compilata con data valida                               |
| Mese Data Sentenza (*)   | *              | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio quando la riga è compilata con data valida                               |
| Anno Data Sentenza (*)   | *              | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio quando la riga è compilata con data valida                               |
| Autorità Sentenza (*)    | *              | select     | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio quando la riga è compilata                                               |
| Luogo Sentenza (*)       | *              | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio quando la riga è compilata                                               |
| Anno R.G.N.R.            | nan            | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - opzionale ma obbligatorio se valorizzato Numero R.G.N.R.                              |
| Numero R.G.N.R.          | nan            | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - opzionale ma obbligatorio se valorizzato Anno R.G.N.R.                                |
| Anno Reg.Gen.            | nan            | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio insieme a Numero Reg.Gen. se Tipo Reg.Gen. è valorizzato                 |
| Numero Reg.Gen.          | nan            | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio insieme a Anno Reg.Gen. se Tipo Reg.Gen. è valorizzato                   |
| Tipo Reg.Gen.            | nan            | select     | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio se sono valorizzati Anno e Numero Reg.Gen.                               |