---
uniqueName: siut-sie-ct-1-0-20210806-allegatoalpianotest006siu
displayName: "SIUT SIE CT 1 0 20210806 Allegato al piano test 006 SIUS Avvocati"
category: "GENERAL"
tags: []
---

# SIUT-SIE-CT-1.0-20210806-Allegato_al_piano_test_006_SIUS_Avvocati

> **File originale:** `MEV/SCHEDA_006/SIUT-SIE-CT-1.0-20210806-Allegato_al_piano_test_006_SIUS_Avvocati.xlsx`  
> **Tipo:** XLSX

---

## Copertina

## TabellaTest

| Intervento |  | MEV 2019_006 SIUS Avvocati |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  | SIUT-SIE-CT-1.0-20210806-Allegato_al_piano_test_006_SIUS_Avvocati.xlsx |  |  |  |  |  |  |  |  |
| Codice Appl. | ID. Requisito Padre | Lista Requisiti | ID Caso d'uso | Caso d'uso | ID | Scenario di test | Classe di Gravità (1-4) | Classe di rilevanza (A, B, C) | Esito |  |
| SIES | REQ-SIE-006-01 | REQ-SIE-006-01 | UC01 | Verifica Inserimento Fissazione Udienza in SIUS | TF001.UC01 | Verifica: Verificare che nel sottosistema SIUS, nella fase di inserimento fissazione udienza, la ricerca dell'udienza dia risultati congrui con l'installazione precedente | 3 | C |  |  |

## SpecificaTest

| Intervento |  |  | MEV 2019_006 SIUS Avvocati |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | SIUT-SIE-CT-1.0-20210806-Allegato_al_piano_test_006_SIUS_Avvocati.xlsx |  |  |  |
| ID caso di test | Requisito |  | Caso d'uso |  | Scenario di test |  |
| TF001.UC01 | REQ-SIE-006-01 |  | Verifica Inserimento Fissazione Udienza in SIUS |  | Verifica: Verificare che nel sottosistema SIUS, nella fase di inserimento fissazione udienza, la ricerca dell'udienza dia risultati congrui con l'installazione precedente |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIUS come Tribunale di Sorveglianza | Dxxxxx (Tribunale di Sorveglianza) |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1 | Navigazione | Udienza » Fissazione Udienza |  | Visualizzazione pagina Inserimento Fissazione Udienza |  |
|  | 2 | Azione | Cliccare sul link Lista Udienze |  | Visualizzazione pagina Elenco Udienze |  |
|  | V | Verifica | Verificare che la ricerca dia un risultato non nullo |  |  | OK |
|  | V | Verifica | Se il risultato è non nullo, allora verificare che lo stesso output sia ottenuto con una precedente installazione |  |  | OK |
|  | 3 | Azione | Se il risultato è nullo, allora modificare la data nel campo Visualizza le Udienze a partire dal e premere il tasto Visualizza |  |  |  |
|  | V | Verifica | Se il risultato è non nullo, allora verificare che lo stesso output sia ottenuto con una precedente installazione |  |  | OK |

## VerificheConformità

| Intervento |  |  | MEV 2019_006 SIUS Avvocati |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | SIUT-SIE-CT-1.0-20210806-Allegato_al_piano_test_006_SIUS_Avvocati.xlsx |  |  |  |  |
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

| Intervento |  | MEV 2019_006 SIUS Avvocati |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  | SIUT-SIE-CT-1.0-20210806-Allegato_al_piano_test_006_SIUS_Avvocati.xlsx |  |  |  |  |  |  |
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
| B |  |  |  |  |  |  |  |  |
| C |  |  | 1 |  |  |  |  |  |