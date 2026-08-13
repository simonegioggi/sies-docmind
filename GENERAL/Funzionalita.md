---
uniqueName: funzionalita
displayName: "Funzionalita"
category: "GENERAL"
tags: []
---

# Funzionalita

> **File originale:** `MEV/LPU/Funzionalita.xls`  
> **Tipo:** XLS

---

## Funzionalità

|  |  | TABELLA EVENTO |  |  |  | TABELLA DECRETO ORDINANZA SIEP |  |  | STATO PROCEDIMENTO | POSIZIONE GIURIDICA |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| FUNZIONE |  | COD TIPO EVENTO | COD TIPO PROVVEDIMENTO | COD MOTIVO | COD ESITO | COD OGGETTO
DECISIONE | COD OGGETTO
PROCEDIMENTO | COD ESITO |  |  |
|  |  |  |  | (MOTIVO) | (ESITO) | (OGGETTO) | (MOTIVO) | (ESITO) | (da valorizzare) | (in evento) |
| GESTIONE PENA |  |  |  |  |  |  |  |  |  |  |
| Annotazione Comunicazione agli Enti | FI2 | 25 | 12 / 25
(selezione) | 9019 | 0760 | G035 | 9019 | 0760 | 0511 (con data consegna impostata)
0529 (con data consegna non impostata) | select in maschera
58 |
| Emissione Provvedimento di Esecuzione | FI3 | 27 | 04 | 9010 | 0760 |  |  |  | 0519 | select in maschera |
| Annotazione Svolgimento Attività | FI5 | 26 | 12 | 9018 | 0760 |  |  |  |  | 59 (se impostata data assolvimento obblighi) |
| ANNOTAZIONE |  |  |  |  |  |  |  |  |  |  |
| Interruzione | FI4.1 | 28 | 12 | 9014 / 9015 / 9016
(selezione) |  |  |  |  | 0513 | 57 |
| Sospensione | FI4.2 | 29 | 12 | 9011 / 9012 / 9013
(selezione) |  |  |  |  | 0512 | 56 |
| Ripristino | FI4.3 | 30 | 12 | 9017 |  |  |  |  | 0520 | 58 |
| RICHIESTE AL GIUDICE DELL'ESECUZIONE |  |  |  |  |  |  |  |  |  |  |
| Modifica modalità di esecuzione | FI6.1 - FI6.4 | 24 | 26 | 9007 |  |  |  |  |  |  |
| Revoca sanzione sostitutiva | FI6.11 - FI6.14 | 21 | 26 | 9008 |  |  |  |  | 0515 | Libero |
| Estinzione Reato | FI6.15 - FI6.18 | 22 | 26 | 9009 |  |  |  |  |  |  |
| Applicazione sanzioni amministrative | FI6.6 - FI6.9 | 23 | 26 | 9006 |  |  |  |  |  |  |
| DECISIONI DEL GE |  |  |  |  |  |  |  |  |  |  |
| Modifica modalità di esecuzione | FI7 - FI7.1 | 24 | 02 / 03
(selezione) | 9007 | 0756 | G032 | 9007 | 0756 |  |  |
| Revoca pena sostitutiva | FI7.3 - FI7.4 | 21 | 02 / 03
(selezione) | 9008 | 0757 | G033 | 9008 | 0757 | 0517
0518 (se non vengono ripristinate le sanzioni amministrative) | Libero |
| Estinzione del Reato | FI7.6 - FI7.4 | 22 | 02 / 03
(selezione) | 9009 | 0758 | G034 | 9009 | 0758 | 0516 | Libero |
| Applicazioni sanzioni amministrative | FI7.9 - FI7.10 | 23 | 02 / 03
(selezione) | 9006 | 0759 | G031 | 9006 | 0759 |  |  |