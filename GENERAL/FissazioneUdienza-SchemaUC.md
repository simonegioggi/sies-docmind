---
uniqueName: fissazioneudienza-schemauc
displayName: "FissazioneUdienza SchemaUC"
category: "GENERAL"
tags: []
---

# FissazioneUdienza-SchemaUC

> **File originale:** `MEV/Mev15/FissazioneUdienza-SchemaUC.xls`  
> **Tipo:** XLS

---

## Fissazione

| Fissazione Udienza |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Prog | Etichetta | Obbl. | Controlli | Tipo Campo | Descrizione | Default |
| Dati anagrafici |  |  |  |  |  |  |
|  | Magistrato | Si |  | Lista | Nominativo Magistrato |  |
|  | Difensore | No |  | Label | Visualizza il difensore |  |
|  | Tipo Rito | Si |  | Lista | Tipologia rito |  |
|  | Data Emissione Decreto | No |  | Data | Data emissione decreto |  |
|  | Oggetti | Si |  | Label | Elenco Oggetti |  |
|  | Data Udienza | No |  | Data | Data udienza |  |
|  | Sezione | Si | Se il magistrato non ha la sezione assegnata il campo è “-“ | Lista | Descrizione Sezione | Sezione Assegnata al Magistrato |
|  | Aula | No | Se non c’è la sezione, l’utente può selezionare qualsiasi aula. | Lista | Identificazione Aula | Viene caricata la predefinita |
|  | Ingresso | No | Non modificabile | Testo | Identificazione Ingresso |  |
|  | Piano | No | Non Modificabile | Testo | Numero Piano |  |
|  | Ora Inizio | No |  | Testo | Ora inizio udienza diviso: ore : minuti |  |
|  | Ora Fine | No |  | Testo | Ora fine Udienza diviso in ore : minuti |  |
|  | Ordina la traduzione per il condannato | No | Visibile solo se posizione giuridica “Detenuto” | Check box | Selezione traduzione |  |
|  | Luogo Svolgimento | No |  | Testo | Luogo svolgimento udienza | Indirizzo sede giudiziaria relativa all’ufficio dell’utente |
|  | Note | No |  | Testo | Note |  |

## Parti Civili-Offese

| Parti Civili-Offese |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Persona Fisica |  |  |  |  |  |  |
| Prog | Etichetta | Obbl. | Controlli | Tipo Campo | Descrizione | Default |
| Inserimento Nuova Parte |  |  |  |  |  |  |
| 1.0 | Persona Fisica/Parte Giuridica | Si |  | Radio Button | Identifica la tipologia di parte che si vuole inserire |  |
| 2.0 | Cognome | Si |  | Testo | Cognome Parte |  |
| 3.0 | Nome | Si |  | Testo | Nome Parte |  |
| 4.0 | Sesso | Si | Accetta solo i valori F/M | Testo | Sesso |  |
| 5.0 | Data di Nascita | Si | Controlli validità data | Data | Data di nascita parte |  |
| 6.0 | Comune di Nascita | Si |  | Lista | Comune di nascita parte |  |
| 7.0 | Stato Nascita | No |  | Lista | Stato Nascita |  |
| 8.0 | Comune Nascita Estero | No |  | Testo | Comune nascita estero |  |
| 9.0 | Codice Fiscale | No | Controlli validità codice fiscale | Testo | Codice fiscale |  |
| 10.0 | Indirizzo | No |  | Testo | Indirizzo |  |
| 11.0 | Luogo | No |  | Lista | Luogo |  |
| 12.0 | CAP | No | Controlli validità CAP | Testo | CAP |  |
| 13.0 | Comune Estero | No |  | Testo | Comune estero |  |
| 14.0 | Stato | No |  | Lista | Stato |  |
| 15.0 | Convocazione Udienza | Si | Accetta solo valori S/N | Testo | Convocazione Udienza | ‘N’ |
| 16.0 | Domiciliato presso il difensore | No |  | Check box | Se selezionato il soggetto non è interessato alla notifica | Vuoto |
| Per la notifica all’avvocato |  |  |  |  |  |  |
| 17.0 | Nominativo | No |  | Testo | Nominativo Avvocato |  |
| 18.0 | Autorità | No |  | Lista | Autorità |  |
| 19.0 | Sede | No |  | Lista | Sede |  |
| 20.0 | Indirizzo | No |  | Testo | Indirizzo |  |
| Per la notifica al soggetto |  |  |  |  |  |  |
| 21.0 | Autorità | No |  | Lista | Autorità |  |
| 22.0 | Sede | No |  | Lista | Sede |  |
| 23.0 | Indirizzo | No |  | Testo | Indirizzo |  |
| Persona Giuridica |  |  |  |  |  |  |
| Prog | Etichetta | Obbl. | Controlli | Tipo Campo | Descrizione | Default |
| Inserimento Nuova Parte |  |  |  |  |  |  |
| 1.0 | Persona Fisica/Persona Giuridica | Si |  | Radio Button | Identifica la tipologia di parte che si vuole inserire |  |
| 2.0 | Società | Si |  | Testo | Denominazione |  |
| 3.0 | Ragione Sociale | No |  | Lista | Ragione sociale (spa,srl….) |  |
| 4.0 | Provincia | No |  | Lista | Elenco Provincie |  |
| 5.0 | Partita IVA/Codice Fiscale | No |  | Testo | Partita iva o Codice Fiscale |  |
| 6.0 | Sede Legale | No |  | Testo | Sede legale |  |
| 7.0 | Indirizzo | No |  | Testo | Indirizzo |  |
| Inserimento Legale Rappresentate |  |  |  |  |  |  |
| 8.0 | Cognome | Si |  | Testo | Cognome Legale Rappresentante |  |
| 9.0 | Nome | Si |  | Testo | Nome |  |
| 10.0 | Sesso | Si |  | Testo | Sesso |  |
| 11.0 | Data di Nascita | Si |  | Data | Data di nascita |  |
| 12.0 | Comune di Nascita | Si |  | Test | Comune |  |
| 13.0 | Stato di Nascita | No |  | Testo | Stato |  |
| 14.0 | Comune Nascita Estero | No |  | Testo | Comune Estero |  |
| 15.0 | Codice Fiscale | No |  | Testo | Codice Fiscale |  |
| Residenza/domicilio |  |  |  |  |  |  |
| 16.0 | Indirizzo | No |  | Testo | Indirizzo |  |
| 17.0 | Luogo | No |  | Lista | Luogo |  |
| 18.0 | CAP | No | Controlli validità CAP | Testo | CAP |  |
| 19.0 | Comune Estero | No |  | Testo | Comune estero |  |
| 20.0 | Stato | No |  | Lista | Stato |  |
| 21.0 | Convocazione Udienza | Si | Accetta solo valori S/N | Testo | Convocazione Udienza | ‘N’ |
| 22.0 | Domiciliato presso il difensore | No |  | Check box | Se selezionato il soggetto non è interessato alla notifica | Vuoto |
| Per la notifica all’avvocato |  |  |  |  |  |  |
| 23.0 | Nominativo | No |  | Testo | Nominativo Avvocato |  |
| 24.0 | Autorità | No |  | Lista | Autorità |  |
| 25.0 | Sede | No |  | Lista | Sede |  |
| 26.0 | Indirizzo | No |  | Testo | Indirizzo |  |
| Per la notifica al soggetto |  |  |  |  |  |  |
| 27.0 | Autorità | No |  | Lista | Autorità |  |
| 28.0 | Sede | No |  | Lista | Sede |  |
| 29.0 | Indirizzo | No |  | Testo | Indirizzo |  |

## Monocratica

| Udienza Monocratica |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Prog | Etichetta | Obbl. | Controlli | Tipo Campo | Descrizione | Default |
| Parti Inserite |  |  |  |  |  |  |
| 1.0 | Data Udienza | Si |  | Data | Data udienza |  |
| 2.0 | Sezione | Si |  | Lista | Sezione | Viene selezionata la sezione di appartenenza del Magistrato Assegnatario con la possibilità di modificarla |
| 2.0 | Giudice | Si |  | Lista | Nominativo Magistrato | Viene riportato il nominativo del Magistrato Assegnatario con la possibilità di modificarlo. |
| 3.0 | Procuratore della Repubblica | No |  | Lista | Nominativo Procuratore della Repubblica |  |
| 4.0 | Cancelliere | No |  | Lista | Nominativo Cancelliere |  |

## Coll-CAT

| Udienza Collegiale - Corte Appello e Tribunale |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Prog | Etichetta | Obbl. | Controlli | Tipo Campo | Descrizione | Default |
| Parti Inserite |  |  |  |  |  |  |
| 1.0 | Data Udienza | Si |  | Data | Data udienza |  |
| 2.0 | Sezione | No |  | Lista | Lista Sezioni | Impostata con la sezione del magistrato assegnatario, modificabile |
| 3.0 | Presidente | No |  | Lista | Nominativo Magistrato | Impostato con il nominativo del magistrato assegnatario |
| 4.0 | Consigliere | No |  | Lista | Nominativo Magistrato |  |
| 5.0 | Consigliere | No |  | Lista | Nominativo Magistrato |  |
| 6.0 | Procuratore Generale | No |  | Lista | Nominativo Procuratore |  |
| 7.0 | Cancelliere | No |  | Lista | Nominativo Cancelliere |  |

## Coll-GupMino

| Udienza Collegiale - GUP Tribunale Minorenni |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Prog | Etichetta | Obbl. | Controlli | Tipo Campo | Descrizione | Default |
| Parti Inserite |  |  |  |  |  |  |
| 1.0 | Data Udienza | Si | Controlli formali validità data | Data | Data udienza |  |
| 2.0 | Sezione | Si |  | Lista | Lista Sezioni | Sezione di Appartenenza del Magistrato Assegnatario, modificabile |
| 2.0 | Presidente | Si |  | Lista | Nominativo Magistrato | Selezione Magistrati in base alla sezione selezionata. |
| 3.0 | Giudice Onorario | No |  | Lista | Nominativo Magistrato |  |
| 4.0 | Giudice Onorario | No |  | Lista | Nominativo Magistrato |  |
| 5.0 | Procuratore Generale | No |  | Lista | Nominativo Procuratore |  |
| 6.0 | Cancelliere | No |  | Lista | Nominativo Cancelliere |  |

## Coll-TribMino

| Udienza Collegiale - Tribunale Minorenni |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Prog | Etichetta | Obbl. | Controlli | Tipo Campo | Descrizione | Default |
| Parti Inserite |  |  |  |  |  |  |
| 1.0 | Data Udienza | Si | Controlli formali validità data | Data | Data Udienza |  |
| 2.0 | Sezione | No |  | Lista | Lista Sezioni | Impostata con la sezione di appartenenza del Magistrato Assegnatario |
| 3.0 | Presidente | No |  | Lista | Nominativo Magistrato |  |
| 4.0 | Giudice Relatore | No |  | Lista | Nominativo Magistrato |  |
| 5.0 | Giudice Onorario | No |  | Lista | Nominativo Magistrato |  |
| 6.0 | Giudice Onorario | No |  | Lista | Nominativo Magistrato |  |
| 7.0 | Procuratore Generale | No |  | Lista | Nominativo Procuratore |  |
| 8.0 | Cancelliere | No |  | Lista | Nominativo Cancelliere |  |

## Coll-AssApp

| Udienza Collegiale - Corte Assise e Corte Appello |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Prog | Etichetta | Obbl. | Controlli | Tipo Campo | Descrizione | Default |
| Parti Inserite |  |  |  |  |  |  |
| 1.0 | Data Udienza | Si | Controlli Formali validità data | Data | Data udienza |  |
| 2.0 | Sezione | No |  | Lista | Lista Sezioni | Sezione di Appartenenza del Magistrato Assegnatario. |
| 3.0 | Presidente | No |  | Lista | Nominativo Magistrato |  |
| 4.0 | Giudice Relatore | No |  | Lista | Nominativo Magistrato |  |
| 5.0 | Giudice Popolare | No |  | Elenco | Nominativo Giudice Popolare |  |
| 6.0 | Ruolo | No |  | Elenco | Ruolo |  |

## Coll-AppMino

| Udienza Collegiale - Sezione Minorenni e Corte Appello |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Prog | Etichetta | Obbl. | Controlli | Tipo Campo | Descrizione | Default |
| Parti Inserite |  |  |  |  |  |  |
| 1.0 | Data Udienza | Si | Controlli formali validità data | Data | Data udienza |  |
| 2.0 | Sezione | No |  | Lista | Lista Sezioni | Sezione di Appartenenza del Magistrato Assegnatario. |
| 3.0 | Presidente | No |  | Lista | Nominativo Magistrato |  |
| 4.0 | Consigliere | No |  | Lista | Nominativo Magistrato |  |
| 5.0 | Consigliere | No |  | Lista | Nominativo Magistrato |  |
| 6.0 | Giudice Onorario | No |  | Lista | Nominativo Magistrato |  |
| 7.0 | Giudice Onorario | No |  | Lista | Nominativo Magistrato |  |
| 8.0 | Procuratore Generale | No |  | Lista | Nominativo Procuratore |  |
| 9.0 | Cancelliere | No |  | Lista | Nominativo Cancelliere |  |