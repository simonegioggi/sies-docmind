---
uniqueName: siut-sie-ct-1-0-20210430-allegatoalpianotestsies-a
displayName: "SIUT SIE CT 1 0 20210430 Allegato al piano test SIES ADN Post golive"
category: "GENERAL"
tags: []
---

# SIUT-SIE-CT-1.0-20210430-Allegato_al_piano_test_SIES-ADN-Post-golive

> **File originale:** `MEV/Integrazione SIES-ADN/RILASCIO_MEV_SIES-ADN (POST GO-LIVE)/20210430_1.0/SIUT-SIE-CT-1.0-20210430-Allegato_al_piano_test_SIES-ADN-Post-golive.xlsx`  
> **Tipo:** XLSX

---

## Copertina

## TabellaTest

| Intervento |  | Integrazione SIES-ADN-Post-golive |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  | SIUT-SIE-CT-1.0-20210430-Allegato-al-piano-test_SIES-ADN-Post-golive.xls |  |  |  |  |  |  |  |
| Codice Appl. | ID. Requisito Padre | Lista Requisiti | ID Caso d'uso | Caso d'uso | ID | Scenario di test | Classe di Gravità (1-4) | Classe di rilevanza (A, B, C) | Esito |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC01 | Richiesta certificato penale su SIEP | TF001.UC01 | Verifica: verificare che in ambito SIEP la richiesta del certificato penale avvenga correttamente. | 2 | B |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC02 | Richiesta certificato penale su SIUS | TF001.UC02 | Verifica: verificare che in ambito SIUS la richiesta del certificato penale avvenga correttamente. | 2 | B |  |

## SpecificaTest

| Intervento |  |  | Integrazione SIES-ADN-Post-golive |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | SIUT-SIE-CT-1.0-20210430-Allegato-al-piano-test_SIES-ADN-Post-golive.xls |  |  |  |
| ID caso di test | Requisito |  | Caso d'uso |  | Scenario di test |  |
| TF001.UC01 | REQ-SIC-003 |  | Richiesta certificato penale su SIEP |  | Verifica: verificare che in ambito SIEP la richiesta del certificato penale avvenga correttamente. |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES | L'utente inserisce le proprie credenziali ADN | il sistema effettua un controllo sulla ‘autenticità’ delle informazioni inserite effettuando una chiamata LDAP sul server ADN di giustizia. |  |
|  | P | Stato Base | Il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione delle utenze SIES. |  |  |  |
|  | 1 | Azione | L'utente ha già un'utenza SIEP associata ad utenza ADN |  | Viene visualizzata la pagina con l'utenza SIEP associata con il pulsante Entra | OK |
|  | 2 | Azione | L'utente clicca sul pulsante Entra |  |  |  |
|  | 3 | Azione | L'utente si trova nella pagina principale dell'applicazione SIEP. |  |  |  |
|  | 4 | Navigazione | Istruttorie/Richieste  » Richiesta Certificato Penale |  | Visualizzazione pagina  Ricerca Procedimento |  |
|  | 5 | Azione | L'utente ricerca un procedimento |  | Viene visualizzata la pagina  Richiesta Certificato Penale |  |
|  | 6 | Azione | L'utente clicca sul pulsante Richiesta Certificato |  | In fase di ‘invocazione’ del servizio dal ‘client’ SIES viene passato lo username ADN | OK |
|  | V | Verifica | Verificare che venga prodotto il certificato penale |  |  | OK |
| TF001.UC02 | REQ-SIC-003 |  | Richiesta certificato penale su SIUS |  | Verifica: verificare che in ambito SIUS la richiesta del certificato penale avvenga correttamente. |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES | L'utente inserisce le proprie credenziali ADN | il sistema effettua un controllo sulla ‘autenticità’ delle informazioni inserite effettuando una chiamata LDAP sul server ADN di giustizia. |  |
|  | P | Stato Base | Il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione delle utenze SIES. |  |  |  |
|  | 1 | Azione | L'utente ha già un'utenza SIUS associata ad utenza ADN |  | Viene visualizzata la pagina con l'utenza SIUS associata con il pulsante Entra | OK |
|  | 2 | Azione | L'utente clicca sul pulsante Entra |  |  |  |
|  | 3 | Azione | L'utente si trova nella pagina principale dell'applicazione SIUS. |  |  |  |
|  | 4 | Navigazione | Ricerche e Visualizzazioni » Procedimento per n° SIUS |  | Visualizzazione pagina  Ricerca Procedimento |  |
|  | 5 | Azione | L'utente ricerca un procedimento |  | Visualizzazione pagina Dettaglio Procedimento SIUS |  |
|  | 6 | Azione | Dalla combo posta nella parte superiore della videata e contenente le varie funzionalità l'utente seleziona Richiesta Certificato Penale |  | Visualizzazione pagina Richiesta Certificato Penale |  |
|  | 7 | Azione | L'utente clicca sul pulsante Richiesta Certificato |  | In fase di ‘invocazione’ del servizio dal ‘client’ SIES viene passato lo username ADN | OK |
|  | V | Verifica | Verificare che venga prodotto il certificato penale |  |  | OK |

## VerificheConformità

| Intervento |  |  | Integrazione SIES-ADN-Post-golive |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | SIUT-SIE-CT-1.0-20210430-Allegato-al-piano-test_SIES-ADN-Post-golive.xls |  |  |  |  |
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

| Intervento |  | Integrazione SIES-ADN-Post-golive |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  | SIUT-SIE-CT-1.0-20210430-Allegato-al-piano-test_SIES-ADN-Post-golive.xls |  |  |  |  |  |  |
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