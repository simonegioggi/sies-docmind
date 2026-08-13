---
uniqueName: siut-sies-ct-1-0-20240802-allegatoalpianotest2024-
displayName: "SIUT SIES CT 1 0 20240802 Allegato al piano test 2024 DNA"
category: "GENERAL"
tags: []
---

# SIUT-SIES-CT-1.0-20240802-Allegato_al_piano_test_2024-DNA

> **File originale:** `MEV/SCHEDA_DNA/SIUT-SIES-CT-1.0-20240802-Allegato_al_piano_test_2024-DNA.xlsx`  
> **Tipo:** XLSX

---

## Copertina

## TabellaTest

| Intervento |  | MEV 2024_DNA |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  | SIUT-SIES-CT-1.0-20240802-Allegato_al_piano_test_2024-DNA.xlsx |  |  |  |  |  |  |  |  |
| Codice Appl. | ID. Requisito Padre | Lista Requisiti | ID Caso d'uso | Caso d'uso | ID | Scenario di test | Classe di Gravità (1-4) | Classe di rilevanza (A, B, C) | Esito |  |
| SIES | TF001 | TF001 | UC01 | Ricerca Fascicolo SIEP altre BDI per utente DNA | TF001.UC01 | Verifica: Verificare nel sottosistema SIUS per utente DNA che dopo l'esecuzione del batch non vi sia traccia della ricerca procedimento effettuata | 2 | B |  |  |
| SIES | TF002 | TF002 | UC01 | Ricerca procedimenti SIEP per Soggetto per utente DNA | TF002.UC01 | Verifica: Verificare nel sottosistema SIUS per utente DNA che dopo l'esecuzione del batch non vi sia traccia della ricerca soggetto effettuata | 2 | B |  |  |

## SpecificaTest

| Intervento |  |  | MEV 2024_DNA |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | SIUT-SIES-CT-1.0-20240802-Allegato_al_piano_test_2024-DNA.xlsx |  |  |  |
| ID caso di test | Requisito |  | Caso d'uso |  | Scenario di test |  |
| TF001.UC01 | TF001 |  | Ricerca Fascicolo SIEP altre BDI per utente DNA |  | Verifica: Verificare nel sottosistema SIUS per utente DNA che dopo l'esecuzione del batch non vi sia traccia della ricerca procedimento effettuata |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIUS come utente DIREZIONE NAZIONALE ANTIMAFIA | Jxxxxx (DIREZIONE NAZIONALE ANTIMAFIA) |  |  |
|  | P | Stato Base | L'utente si trova nella Home Page |  |  |  |
|  | 1 | Navigazione | Ricerche Altre BDI » Ricerca Fascicolo SIEP altre BDI | Ufficio e Sede di altro distretto | Visualizzazione pagina "Ricerca Procedimento" |  |
|  | 2 | Azione | L'utente riempie i campi obbligatori e preme il tasto "Ricerca" | Richiesta di ricerca Procedimento sottomessa al Sistema! | Visualizzazione pagina "Dettaglio Procedimento da Trasferire" |  |
|  | 3 | Azione | L'utente si collega al Database e verifica che nella tabella "MESSAGGIO" sia presente un record con campo "CODICE_UTENTE_MITTENTE" pari a Jxxxxx ovvero l'utente che ha effettuato la ricerca | ID_MESSAGGIO = identificativo | 1 record |  |
|  | V | Verifica | Verificare che, dopo l'esecuzione del batch, non sia più presente nella tabella "MESSAGGIO" la riga corrispondente a "ID_MESSAGGIO = identificativo" | Select count(*) from MESSAGGIO where ID_MESSAGGIO = identificativo | 0 record | OK |
| TF002.UC01 | TF002 |  | Ricerca procedimenti SIEP per Soggetto per utente DNA |  | Verifica: Verificare nel sottosistema SIUS per utente DNA che dopo l'esecuzione del batch non vi sia traccia della ricerca soggetto effettuata |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIUS come utente DIREZIONE NAZIONALE  ANTIMAFIA | Jxxxxx (DIREZIONE NAZIONALE ANTIMAFIA) |  |  |
|  | P | Stato Base | L'utente si trova nella Home Page |  |  |  |
|  | 1 | Navigazione | Ricerche Altre BDI » Ricerca procedimenti SIEP per Soggetto | In altri distretti | Visualizzazione pagina "Ricerca Procedimento per Soggetto" |  |
|  | 2 | Azione | L'utente riempie i campi obbligatori e preme il tasto "Ricerca" | Richiesta di ricerca Soggetto sottomessa al Sistema! | Visualizzazione pagina " Esiti Ricerca Soggetto su altre BDI" |  |
|  | 3 | Azione | L'utente si collega al Database e verifica che nella tabella "MESSAGGIO" sia presente un record con campo "CODICE_UTENTE_MITTENTE" pari a Jxxxxx ovvero l'utente che ha effettuato la ricerca | ID_MESSAGGIO = identificativo | 1 record |  |
|  | V | Verifica | Verificare che, dopo l'esecuzione del batch, non sia più presente nella tabella "MESSAGGIO" la riga corrispondente a "ID_MESSAGGIO = identificativo" | Select count(*) from MESSAGGIO where ID_MESSAGGIO = identificativo | 0 record | OK |

## VerificheConformità

| Intervento |  |  | MEV 2024_DNA |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | SIUT-SIES-CT-1.0-20240802-Allegato_al_piano_test_2024-DNA.xlsx |  |  |  |  |
| ID | Tipo Verifica | Attributo | Indicatore | Descrizione tipo Verifica | Esito Verifica Fornitore | Esito Verifica Amministrazione |  |
| 001 | Adeguatezza delle funzionalità | Completezza funzionale | Copertura dei requisiti | Verifica del grado di copertura funzionale offerta sulla base dell’analisi dei requisiti, delle funzionalità e degli obiettivi richiesti | OK |  |  |
| 002 | Adeguatezza delle funzionalità | Correttezza funzionale | Aderenza ai requisiti | Verifica del grado con cui le funzionalità implementate rispettano i requisiti richiesti | OK |  |  |
| 003 | Adeguatezza delle funzionalità | Appropriatezza funzionale | Conformità alle normative | Verifica l’aderenza delle funzionalità implementate rispetto alle normative pertinenti | OK |  |  |
| 004 | Affidabilità | Robustezza | Robustezza del software | Verifica della capacità del sistema di gestire condizioni non previste dalle specifiche | OK |  |  |
| 005 | Manutenibilità | Analizzabilità | Leggibilità del codice | Verifica della facilità di comprensione del codice, per esempio con riferimento ai nomi utilizzati per i moduli, le funzioni e le variabili, ai commenti e alla dimensione dei moduli e delle funzioni | OK |  |  |
| 006 | Manutenibilità | Analizzabilità | Copertura documentazione tecnica | Verifica del livello di completezza della documentazione tecnica di moduli e funzioni | OK |  |  |
| 007 | Manutenibilità | Analizzabilità | Adeguatezza documentazione tecnica | Verifica della qualità descrittiva della documentazione tecnica di moduli e funzioni | OK |  |  |
| 008 | Manutenibilità | Verificabilità | Completezza dei test | Verifica del grado di copertura del codice sviluppato da parte di test (di varia natura, come test unitari, test di integrazione, test end-to-end, test di accettazione, test di regressione, test di qualità) | OK |  |  |

## SogliaAccettazione

| Intervento |  | MEV 2024_DNA |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  | SIUT-SIES-CT-1.0-20240802-Allegato_al_piano_test_2024-DNA.xlsx |  |  |  |  |  |  |
| Verifica Soglia di Accettazione |  |  |  |  |  | In Rosso le difformità che hanno superato il numero massimo ammissibile |  |  |
| Classe di rilevanza | Classe di gravità |  |  |  |  |  |  |  |
|  | 1 | 2 | 3 | 4 |  |  |  |  |
| A |  |  |  |  |  |  |  |  |
| B |  |  |  |  |  |  |  |  |
| C |  |  |  |  |  |  |  |  |
| Numero massimo di difformità ammesse |  |  |  |  |  |  |  |  |
| Classe di rilevanza | Classe di gravità |  |  |  |  |  |  |  |
|  | 1 | 2 | 3 | 4 |  |  |  |  |
| A |  |  |  |  |  |  |  |  |
| B |  | 2 |  |  |  |  |  |  |
| C |  |  |  |  |  |  |  |  |