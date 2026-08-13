---
uniqueName: siut-sie-ct-1-1-20210323-allegatoalpianotestsies-a
displayName: "SIUT SIE CT 1 1 20210323 Allegato al piano test SIES ADN"
category: "GENERAL"
tags: []
---

# SIUT-SIE-CT-1.1-20210323-Allegato_al_piano_test_SIES-ADN

> **File originale:** `MEV/Integrazione SIES-ADN/DOCS/UNUSED/SIUT-SIE-CT-1.1-20210323-Allegato_al_piano_test_SIES-ADN.xlsx`  
> **Tipo:** XLSX

---

## Copertina

## TabellaTest

| Intervento |  | Integrazione SIES-ADN |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  | SIUT-SIE-CT-1.0-20210323-Allegato-al-piano-test_SIES-ADN.xls |  |  |  |  |  |  |  |  |
| Codice Appl. | ID. Requisito Padre | Lista Requisiti | ID Caso d'uso | Caso d'uso | ID | Scenario di test | Classe di Gravità (1-4) | Classe di rilevanza (A, B, C) | Esito |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC01 | Verifica accesso al sistema SIES dopo associazione utenza ADN e SIES | TF001.UC01 | Verifica: verificare che l'utenza ADN venga associata all' utenza SIES e si acceda correttamente all'applicativo. | 1 | A |  |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC02 | Verifica configurazione utenza ADN e SIES | TF001.UC02 | Verifica: verificare che accedendo all'applicativo SIES tramite utenza ADN è possibile configurare più utenze SIES associate alla stessa utenza ADN | 2 | B |  |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC03 | Verifica di avvenuto trasferimento di un titolo di classe 1 da SIES a NSC | TF002.UC03 | Verifica: verificare che venga trasferito correttamente un titolo di classe 1 dal sistema SIES al sistema NSC | 3 | C |  |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC04 | Verifica di avvenuto trasferimento di un foglio complementare da SIES a NSC | TF001.UC04 | Verifica: verificare che venga trasferito correttamente un foglio complementare dal sistema SIES al sistema NSC | 3 | C |  |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC05 | Verifica accesso al modulo web di interconnessione SIES-NSC | TF002.UC05 | Verifica: verificare che l'accesso al modulo web di interconnessione SIES-NSC avvenga correttamente | 3 | C |  |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC06 | Verifica configurazione utenza ADN e SIES con utenza/password errate | TF001.UC06 | Verifica: verificare il comportamento del sistema dopo accesso tramite utenza ADN quando sia prova a configurare un'utenza/password SIES errate | 2 | B |  |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC07 | Verifica configurazione utenza ADN e SIES con utenza non valida | TF001.UC07 | Verifica: verificare il comportamento del sistema dopo accesso tramite utenza ADN quando sia prova a configurare un'utenza disabilitata | 2 | B |  |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC08 | Verifica configurazione utenza ADN e SIES con utenza disabilitata dopo associazione | TF001.UC08 | Verifica: verificare il comportamento del sistema dopo accesso tramite utenza ADN quando sia prova ad accedere con un'utenza SIES già associata ma disabilitata successivamente | 2 | B |  |  |

## SpecificaTest

| Intervento |  |  | Integrazione SIES-ADN |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | SIUT-SIE-CT-1.0-20210323-Allegato-al-piano-test_SIES-ADN.xls |  |  |  |
| ID caso di test | Requisito |  | Caso d'uso |  | Scenario di test |  |
| TF001.UC01 | REQ-SIC-003 |  | Verifica accesso al sistema SIES dopo associazione utenza ADN e SIES |  | Verifica: verificare che l'utenza ADN venga associata all' utenza SIES e si acceda correttamente all'applicativo. |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L’utente si trova sulla pagina di Login del SIES. Il sistema propone la pagina di accesso in cui l’utente sarà tenuto ad inserire le proprie credenziali ADN. | L'utente inserisce le proprie credenziali ADN | il sistema effettua un controllo sulla ‘autenticità’ delle informazioni inserite effettuando una chiamata LDAP sul server ADN di giustizia. |  |
|  | P | Stato Base | Il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione delle utenze SIES. |  |  |  |
|  | 1 | Azione | L'utente seleziona la procedura di ‘Seleziona/Configura un account’ |  | Viene visualizzata la pagina per l’inserimento delle credenziali del SIES. | OK |
|  | 2 | Azione | L'utente inserisce le proprie credenziali SIES e clicca su Login |  | IL sistema dopo aver fatto delle verifiche ed associato l'utenza SIC con quella ADN prospetta un messaggio in cui è presente il pulsante Entra e la voce di 'Seleziona/Configura un account' | OK |
|  | 3 | Azione | L'utente clicca su Entra |  |  |  |
|  | V | Verifica | Verificare che Il sistema visualizzi la welcome page dell’applicazione SIES |  |  | OK |
| TF001.UC02 | REQ-SIC-003 |  | Verifica configurazione utenza ADN e SIES |  | Verifica: verificare che accedendo all'applicativo SIES tramite utenza ADN è possibile configurare più utenze SIES associate alla stessa utenza ADN |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L’utente si trova sulla pagina di Login del SIES. Il sistema propone la pagina di accesso in cui l’utente sarà tenuto ad inserire le proprie credenziali ADN. | L'utente inserisce le proprie credenziali ADN | il sistema effettua un controllo sulla ‘autenticità’ delle informazioni inserite effettuando una chiamata LDAP sul server ADN di giustizia. |  |
|  | P | Stato Base | Il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione delle utenze SIES. |  |  |  |
|  | 1 | Azione | L’utente ha eseguito in precedenza delle associazioni. Si ritroverà, già configurate, le utenze che utilizza solitamente per l’accesso al SIES. |  | Viene visualizzata la pagina con le utenze associate con il pulsante Entra ed il link ‘Seleziona/Configura un account’ | OK |
|  | 2 | Azione | L'utente seleziona la procedura di ‘Seleziona/Configura un account’ |  | Viene visualizzata la pagina per l’inserimento delle credenziali del SIES. | OK |
|  | 3 | Azione | L'utente inserisce le proprie credenziali SIES e clicca su Login |  | IL sistema dopo aver fatto delle verifiche ed associato l'utenza SIC con quella ADN prospetta un messaggio in cui è presente il pulsante Entra e la voce di 'Seleziona/Configura un account' | OK |
|  | 4 | Azione | L'utente clicca su Entra |  |  |  |
|  | V | Verifica | Verificare che Il sistema visualizzi la welcome page dell’applicazione SIES |  |  | OK |
| TF002.UC03 | REQ-SIC-003 |  | Verifica di avvenuto trasferimento di un titolo di classe 1 da SIES a NSC |  | Verifica: verificare che venga trasferito correttamente un titolo di classe 1 dal sistema SIES al sistema NSC |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES | L'utente inserisce le proprie credenziali ADN | il sistema effettua un controllo sulla ‘autenticità’ delle informazioni inserite effettuando una chiamata LDAP sul server ADN di giustizia. |  |
|  | P | Stato Base | Il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione delle utenze SIES. |  |  |  |
|  | 1 | Azione | L'utente ha già un'utenza SIEP associata alla sua utenza ADN |  | Viene visualizzata la pagina con l'utenza SIEP associata con il pulsante Entra ed il link ‘Seleziona/Configura un account’ | OK |
|  | 2 | Azione | L'utente clicca sul pulsante Entra |  |  |  |
|  | 3 | Azione | L'utente si trova nella pagina principale dell'applicazione SIEP. |  |  |  |
|  | 4 | Azione | L'utente ricerca e seleziona un procedimento  validato |  | Viene visualizzata la pagina Dettaglio procedimento | OK |
|  | 5 | Azione | L'utente clicca sull'icona posta in alto Trasferimento Provvedimento da SIES a NSC |  | Viene visualizzato un messaggio di Conferma di trasferimento del provvedimento verso il casellario | OK |
|  | 6 | Azione | L'utente Conferma il trasferimento |  |  |  |
|  | V | Verifica | Verificare che il sistema restituisca un messaggio di trasferimento avvenuto con successo |  |  | OK |
| TF001.UC04 | REQ-SIC-003 |  | Verifica di avvenuto trasferimento di un foglio complementare da SIES a NSC |  | Verifica: verificare che venga trasferito correttamente un foglio complementare dal sistema SIES al sistema NSC |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES | L'utente inserisce le proprie credenziali ADN | il sistema effettua un controllo sulla ‘autenticità’ delle informazioni inserite effettuando una chiamata LDAP sul server ADN di giustizia. |  |
|  | P | Stato Base | Il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione delle utenze SIES. |  |  |  |
|  | 1 | Azione | L'utente ha già un'utenza SIUS associata ad utenza ADN |  | Viene visualizzata la pagina con l'utenza SIUS associata con il pulsante Entra ed il link ‘Seleziona/Configura un account’ | OK |
|  | 2 | Azione | L'utente clicca sul pulsante Entra |  |  |  |
|  | 3 | Azione | L'utente si trova nella pagina principale dell'applicazione SIUS. |  |  |  |
|  | 4 | Navigazione | Ricerche e Visualizzazioni » Procedimento per n° SIUS |  | Visualizzazione pagina  Ricerca Procedimento | OK |
|  | 5 | Azione | L'utente ricerca e seleziona un procedimento |  | Viene visualizzata la pagina Dettaglio procedimento | OK |
|  | 6 | Azione | Dalla combo delle Funzioni l'utente seleziona Compilazione Foglio Complementare e clicca sulla lentina |  | Visualizzazione pagina Compilazione Foglio Complementare | OK |
|  | 7 | Azione | L'utente seleziona nella colonna Azioni l'icona Dettagli |  | Visualizzazione pagina Dettaglio Foglio Complementare | OK |
|  | 8 | Azione | L'utente clicca sull'icona posta in alto Trasmissione Foglio Complementare al SIC |  |  |  |
|  | V | Verifica | Verificare che il RISULTATO DELLA TRASMISSIONE DAL SIEP AL SISTEMA INFORMATIVO DEL CASELLARIO (SIC) sia avvenuto correttamente |  |  | OK |
| TF002.UC05 | REQ-SIC-003 |  | Verifica accesso al modulo web di interconnessione SIES-NSC |  | Verifica: verificare che l'accesso al modulo web di interconnessione SIES-NSC avvenga correttamente |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIES | L'utente inserisce le proprie credenziali ADN | il sistema effettua un controllo sulla ‘autenticità’ delle informazioni inserite effettuando una chiamata LDAP sul server ADN di giustizia. |  |
|  | P | Stato Base | Il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione delle utenze SIES. |  |  |  |
|  | 1 | Azione | L'utente ha già un'utenza SIEP associata ad utenza ADN |  | Viene visualizzata la pagina con l'utenza SIEP associata con il pulsante Entra ed il link ‘Seleziona/Configura un account’ | OK |
|  | 2 | Azione | L'utente clicca sul pulsante Entra |  |  |  |
|  | 3 | Azione | L'utente si trova nella pagina principale dell'applicazione SIEP. |  |  |  |
|  | 4 | Navigazione | Interoperabilità con NSC |  | Visualizzazione pagina  Interoperabilita con NSC | OK |
|  | 5 | Azione | L'utente clicca sull'icona Modulo Web NSC-SIES |  |  |  |
|  | V | Verifica | Verificare che il collegamento web con il sistema NSC avvenga correttamente |  |  | OK |
| TF001.UC06 | REQ-SIC-003 |  | Verifica configurazione utenza ADN e SIES con utenza/password errate |  | Verifica: verificare il comportamento del sistema dopo accesso tramite utenza ADN quando sia prova a configurare un'utenza/password SIES errate |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L’utente si trova sulla pagina di Login del SIES. Il sistema propone la pagina di accesso in cui l’utente sarà tenuto ad inserire le proprie credenziali ADN. | L'utente inserisce le proprie credenziali ADN | il sistema effettua un controllo sulla ‘autenticità’ delle informazioni inserite effettuando una chiamata LDAP sul server ADN di giustizia. |  |
|  | P | Stato Base | Il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione delle utenze SIES. |  |  |  |
|  | 1 | Azione | L’utente ha eseguito in precedenza delle associazioni. Si ritroverà, già configurate, le utenze che utilizza solitamente per l’accesso al SIES. |  | Viene visualizzata la pagina con le utenze associate con il pulsante Entra ed il link ‘Seleziona/Configura un account’ | OK |
|  | 2 | Azione | L'utente seleziona la procedura di ‘Seleziona/Configura un account’ |  | Viene visualizzata la pagina per l’inserimento delle credenziali del SIES. | OK |
|  | 3 | Azione | L'utente inserisce delle credenziali SIES errate (Utenza o password) e clicca su Login |  | IL sistema dopo aver fatto delle verifiche prospetta un messaggio | OK |
|  | V | Verifica | Verificare che Il sistema visualizzi il messaggio : "L'utente non esiste" nel caso abbia inserito un'utenza inesistente o "Password errata" nel caso abbia inserito una password sbagliata. |  |  | OK |
| TF001.UC07 | REQ-SIC-003 |  | Verifica configurazione utenza ADN e SIES con utenza non valida |  | Verifica: verificare il comportamento del sistema dopo accesso tramite utenza ADN quando sia prova a configurare un'utenza disabilitata |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L’utente si trova sulla pagina di Login del SIES. Il sistema propone la pagina di accesso in cui l’utente sarà tenuto ad inserire le proprie credenziali ADN. | L'utente inserisce le proprie credenziali ADN | il sistema effettua un controllo sulla ‘autenticità’ delle informazioni inserite effettuando una chiamata LDAP sul server ADN di giustizia. |  |
|  | P | Stato Base | Il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione delle utenze SIES. |  |  |  |
|  | 1 | Azione | L’utente ha eseguito in precedenza delle associazioni. Si ritroverà, già configurate, le utenze che utilizza solitamente per l’accesso al SIES. |  | Viene visualizzata la pagina con le utenze associate con il pulsante Entra ed il link ‘Seleziona/Configura un account’ | OK |
|  | 2 | Azione | L'utente seleziona la procedura di ‘Seleziona/Configura un account’ |  | Viene visualizzata la pagina per l’inserimento delle credenziali del SIES. | OK |
|  | 3 | Azione | L'utente inserisce delle credenziali SIES non più valide e clicca su Login |  | IL sistema dopo aver fatto delle verifiche prospetta un messaggio. | OK |
|  | V | Verifica | Verificare che Il sistema visualizzi il messaggio : "L'utente non esiste" |  |  | OK |
| TF001.UC08 | REQ-SIC-003 |  | Verifica configurazione utenza ADN e SIES con utenza disabilitata dopo associazione |  | Verifica: verificare il comportamento del sistema dopo accesso tramite utenza ADN quando sia prova ad accedere con un'utenza SIES già associata ma disabilitata successivamente |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L’utente si trova sulla pagina di Login del SIES. Il sistema propone la pagina di accesso in cui l’utente sarà tenuto ad inserire le proprie credenziali ADN. | L'utente inserisce le proprie credenziali ADN | il sistema effettua un controllo sulla ‘autenticità’ delle informazioni inserite effettuando una chiamata LDAP sul server ADN di giustizia. |  |
|  | P | Stato Base | Il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione delle utenze SIES. |  |  |  |
|  | 1 | Azione | L’utente ha eseguito in precedenza delle associazioni. Si ritroverà, già configurate, le utenze che utilizza solitamente per l’accesso al SIES. |  | Viene visualizzata la pagina con le utenze associate con il pulsante Entra ed il link ‘Seleziona/Configura un account’ | OK |
|  | 2 | Azione | L'utente clicca sul pulsante Entra in corrispondenza di un'utenza che è stata disabilitata successivamente all'associazione. |  | IL sistema dopo aver fatto delle verifiche prospetta un messaggio | OK |
|  | V | Verifica | Verificare che Il sistema visualizzi il messaggio : "L'utente non esiste" |  |  | OK |

## VerificheConformità

| Intervento |  |  | Integrazione SIES-ADN |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | SIUT-SIE-CT-1.0-20210323-Allegato-al-piano-test_SIES-ADN.xls |  |  |  |  |
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

| Intervento |  | Integrazione SIES-ADN |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  | SIUT-SIE-CT-1.0-20210323-Allegato-al-piano-test_SIES-ADN.xls |  |  |  |  |  |  |
| Verifica Soglia di Accettazione |  |  |  |  |  | In Rosso le difformità che hanno superato il numero massimo ammissibile |  |  |
| Classe di rilevanza | Classe di gravità |  |  |  |  |  |  |  |
|  | 1 | 2 | 3 | 4 |  |  |  |  |
| A |  |  |  |  |  |  |  |  |
| B |  |  |  |  |  |  |  |  |
| C |  |  |  |  |  |  |  |  |
| Numero massimo di difformità ammesse |  |  |  |  |  |  |  |  |
| Classe di rilevanza | Classe di gravità |  |  |  |  |  |  |  |
|  | 1 | 2 | 3 | 4 |  |  |  |  |
| A | 1 |  |  |  |  |  |  |  |
| B |  | 4 |  |  |  |  |  |  |
| C |  |  | 3 |  |  |  |  |  |