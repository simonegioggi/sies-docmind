---
uniqueName: loadinseriscimisurasicurezzacampi
displayName: "LoadInserisciMisuraSicurezza campi"
category: "GENERAL"
tags: []
---

# LoadInserisciMisuraSicurezza_campi

## Campi

| Campo                       | Obbligatorio   | Tipo       | Sezione             | Note                                                                            |
|:----------------------------|:---------------|:-----------|:--------------------|:--------------------------------------------------------------------------------|
| Natura Misura               | nan            | select     | Misura di Sicurezza | Combo filtro; al cambio aggiorna la combo Tipo Misura                           |
| Tipo Misura                 | *              | select     | Misura di Sicurezza | Obbligatorio; caricato dinamicamente in base a Natura Misura                    |
| Durata Misura - Anni        | nan            | input text | Misura di Sicurezza | Numerico, max 2 cifre                                                           |
| Durata Misura - Mesi        | nan            | input text | Misura di Sicurezza | Numerico, max 2 cifre                                                           |
| Durata Misura - Giorni      | nan            | input text | Misura di Sicurezza | Numerico, max 2 cifre                                                           |
| Data Fine Validità - Giorno | nan            | input text | Misura di Sicurezza | Formato gg; se valorizzato richiede validazione data completa e conferma utente |
| Data Fine Validità - Mese   | nan            | input text | Misura di Sicurezza | Formato mm; parte della data fine validità                                      |
| Data Fine Validità - Anno   | nan            | input text | Misura di Sicurezza | Formato aaaa; parte della data fine validità                                    |