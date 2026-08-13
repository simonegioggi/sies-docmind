---
uniqueName: siut-sie-ct-1-1-20210531-allegatoalpianotestmev-in
displayName: "SIUT SIE CT 1 1 20210531 Allegato al piano test MEV Integrazione SIES ADN  PRE G"
category: "GENERAL"
tags: []
---

# SIUT-SIE-CT-1.1-20210531-Allegato_al_piano_test_MEV-Integrazione SIES-ADN (PRE-GOLIVE)

> **File originale:** `MEV/Integrazione SIES-ADN/RILASCIO_MEV_SIES-ADN (PRE GO-LIVE)/20210531_1.1/SIUT-SIE-CT-1.1-20210531-Allegato_al_piano_test_MEV-Integrazione SIES-ADN (PRE-GOLIVE).xlsx`  
> **Tipo:** XLSX

---

## Copertina

## TabellaTest

| Intervento |  | MEV-Integrazione SIES-ADN (PRE-GOLIVE) |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  | SIUT-SIE-CT-1.1-20210531-Allegato_al_piano_test_MEV-Integrazione SIES-ADN (PRE-GOLIVE).xlsx |  |  |  |  |  |  |  |  |
| Codice Appl. | ID. Requisito Padre | Lista Requisiti | ID Caso d'uso | Caso d'uso | ID | Scenario di test | Classe di Gravità (1-4) | Classe di rilevanza (A, B, C) | Esito |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC01 | Verifica accesso al sistema SIES dopo associazione utenza ADN e SIES | TF001.UC01 | Verifica: verificare che l'utenza ADN venga associata all' utenza SIES e si acceda correttamente all'applicativo. | 1 | A |  |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC02 | Verifica configurazione utenza ADN e SIES | TF001.UC02 | Verifica: verificare che accedendo all'applicativo SIES tramite utenza ADN è possibile configurare più utenze SIES associate alla stessa utenza ADN | 2 | B |  |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC03 | Verifica di avvenuto trasferimento di un titolo di classe 1 da SIES a NSC | TF002.UC03 | Verifica: verificare che venga trasferito correttamente un titolo di classe 1 dal sistema SIES al sistema NSC | 3 | C |  |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC04 | Verifica di avvenuto trasferimento di un foglio complementare da SIES a NSC | TF001.UC04 | Verifica: verificare che venga trasferito correttamente un foglio complementare dal sistema SIES al sistema NSC | 3 | C |  |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC05 | Verifica accesso al modulo web di interconnessione SIES-NSC | TF002.UC05 | Verifica: verificare che l'accesso al modulo web di interconnessione SIES-NSC avvenga correttamente | 3 | C |  |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC06 | Verifica configurazione utenza ADN e SIES con utenza/password errate | TF001.UC06 | Verifica: verificare il comportamento del sistema dopo accesso tramite utenza ADN quando sia prova a configurare un'utenza/password SIES errate | 2 | B |  |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC07 | Verifica configurazione utenza ADN e SIES con utenza non valida | TF001.UC07 | Verifica: verificare il comportamento del sistema dopo accesso tramite utenza ADN quando sia prova a configurare un'utenza disabilitata | 2 | B |  |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC08 | Verifica creazione nuova utenza SIES | TF001.UC08 | Verifica: Verificare che nel caso sia stata creata una nuova utenza SIES l'utente ADN possa associarla correttamente. | 2 | B |  |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC09 | Verifica modifica utenza SIES | TF001.UC09 | Verifica: Verificare che nel caso sia stata modificata una utenza SIES l'accesso sia congruente alla modifica effettuata. | 2 | B |  |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC10 | Verifica disabilitazione utenza SIES | TF001.UC10 | Verifica: Verificare che nel caso sia stata disabilitata una utenza SIES l'utente ADN non possa più utilizzarla dal giorno successivo. | 4 | C |  |  |
| SIES | REQ-SIC-003 | REQ-SIC-003 | UC11 | Verifica reset password utenza SIES | TF001.UC11 | Verifica: Verificare che nel caso sia stato effettuato il reset password di una utenza SIES, il sistema richieda di associare nuovamente l'utenza ed il cambio password prima di fare accedere al sistema. | 4 | C |  |  |

## SpecificaTest

| Intervento |  |  | MEV-Integrazione SIES-ADN (PRE-GOLIVE) |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | SIUT-SIE-CT-1.1-20210531-Allegato_al_piano_test_MEV-Integrazione SIES-ADN (PRE-GOLIVE).xlsx |  |  |  |
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
| TF001.UC08 | REQ-SIC-003 |  | Verifica creazione nuova utenza SIES |  | Verifica: Verificare che nel caso sia stata creata una nuova utenza SIES l'utente ADN possa associarla correttamente. |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L’utente si trova sulla pagina di Login del SIES. Il sistema propone la pagina di accesso in cui l’utente sarà tenuto ad inserire le proprie credenziali ADN. L’amministratore di sistema di SIES ha configurato una nuova utenza. | L'utente inserisce le proprie credenziali ADN | il sistema effettua un controllo sulla ‘autenticità’ delle informazioni inserite effettuando una chiamata LDAP sul server ADN di giustizia. |  |
|  | P | Stato Base | Il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione delle utenze SIES. |  |  |  |
|  | 1 | Azione | L’utente si ritroverà le utenze che utilizza solitamente per l’accesso al SIES. |  | Viene visualizzata la pagina in cui è presente il link ‘Seleziona/Configura un account’ | OK |
|  | 2 | Azione | L'utente seleziona la procedura di ‘Seleziona/Configura un account’ |  | Viene visualizzata la pagina per l’inserimento delle credenziali del SIES. | OK |
|  | 3 | Azione | L'utente inserisce le credenziali della nuova utenza con password uguale alla utenza stessa e clicca su Login |  | IL sistema dopo aver fatto delle verifiche ed associato l'utenza SIES con quella ADN prospetta la pagina di Cambio Password | OK |
|  | 4 | Azione | L'utente inserisce la nuova password e clicca sul pulsante Salva Modifiche |  | Viene visualizzato un messaggio in cui viene confermata la corretta associazione della nuova utenza. | OK |
|  | 5 | Azione | L'utente clicca sul pulsante OK del messaggio |  | Viene visualizzata la pagina contenente tutte le utenze associata compresa la nuova. | OK |
|  | 6 | Azione | L'utente clicca su Entra in corrispondenza della nuova utenza |  |  |  |
|  | V | Verifica | Verificare che Il sistema visualizzi la welcome page dell’applicazione SIES relativa al profilo dell'utenza. |  |  | OK |
| TF001.UC09 | REQ-SIC-003 |  | Verifica modifica utenza SIES |  | Verifica: Verificare che nel caso sia stata modificata una utenza SIES l'accesso sia congruente alla modifica effettuata. |  |
|  | P | Attività Preliminari e/o Precondizioni | L’utente si trova sulla pagina di Login del SIES. Il sistema propone la pagina di accesso in cui l’utente sarà tenuto ad inserire le proprie credenziali ADN. | L'utente inserisce le proprie credenziali ADN | il sistema effettua un controllo sulla ‘autenticità’ delle informazioni inserite effettuando una chiamata LDAP sul server ADN di giustizia. |  |
|  | P | Stato Base | Il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione delle utenze SIES. |  |  |  |
|  | 1 | Azione | L’utente ha eseguito in precedenza delle associazioni. Si ritroverà, già configurate, le utenze che utilizza solitamente per l’accesso al SIES. |  | Viene visualizzata la pagina con le utenze associate con il pulsante Entra ed il link ‘Seleziona/Configura un account’ | OK |
|  | 2 | Azione | L'utente clicca su Entra in corrispondenza di una utenza con profilo per esempio di sola lettura |  |  | OK |
|  | V | Verifica | Verificare che Il sistema visualizzi la welcome page dell’applicazione SIES con un menu le cui voci sono relative alla tipologia di profilo associato all'utenza SIES |  |  | OK |
|  | 3 | Azione | L'utente clicca sul link cambia utenza/esci dell'applicazione SIES |  | Viene visualizzata la pagina con le utenze associate con il pulsante Entra ed il link ‘Seleziona/Configura un account’ | OK |
|  | 4 | Azione | L’amministratore di sistema di SIES modifica il profilo della utenza con cui è avvenuto l'accesso nello step 2. |  |  |  |
|  | 5 | Azione | L'utente clicca su Entra in corrispondenza dell'utenza il cui profilo è stato modificato |  |  |  |
|  | V | Verifica | Verificare che Il sistema visualizzi la welcome page dell’applicazione SIES con un menu le cui voci sono relative alla tipologia di profilo associato all'utenza SIES |  |  | OK |
| TF001.UC10 | REQ-SIC-003 |  | Verifica disabilitazione utenza SIES |  | Verifica: Verificare che nel caso sia stata disabilitata una utenza SIES l'utente ADN non possa più utilizzarla dal giorno successivo. |  |
|  | P | Attività Preliminari e/o Precondizioni | L’utente si trova sulla pagina di Login del SIES. Il sistema propone la pagina di accesso in cui l’utente sarà tenuto ad inserire le proprie credenziali ADN. | L'utente inserisce le proprie credenziali ADN | il sistema effettua un controllo sulla ‘autenticità’ delle informazioni inserite effettuando una chiamata LDAP sul server ADN di giustizia. |  |
|  | P | Stato Base | Il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione delle utenze SIES. |  |  |  |
|  | 1 | Azione | L’utente si ritroverà le utenze che utilizza solitamente per l’accesso al SIES. |  | Viene visualizzata la pagina con le utenze associate con il pulsante Entra ed il link ‘Seleziona/Configura un account’ | OK |
|  | 2 | Azione | L’amministratore di sistema di SIES ha disabilitato una utenza associata all'ADN dell'utente. |  | Il sistema disabilita l'utenza a partire dal giorno successivo alla disattivazione | OK |
|  | 3 | Azione | L'utente clicca sul pulsante Entra in corrispondenza dell'utenza disattivata. |  |  |  |
|  | V | Verifica | Verificare che si riesca ad entrare nell'applicazione SIES. |  |  | OK |
|  | 4 | Azione | L'utente clicca sul logout dell'applicazione SIES |  | L’utente si trova sulla pagina di Login del SIES. Il sistema propone la pagina di accesso in cui l’utente sarà tenuto ad inserire le proprie credenziali ADN. | OK |
|  | 5 | Azione | L’amministratore di sistema di SIES modifica la data di disattivazione dell'utenza dello step 2 al giorno precedente. |  |  |  |
|  | 6 | Azione | L'utente inserisce le proprie credenziali ADN |  | il sistema effettua un controllo sulla ‘autenticità’ delle informazioni inserite effettuando una chiamata LDAP sul server ADN di giustizia. | OK |
|  | 7 | Azione | Il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione delle utenze SIES. |  |  |  |
|  | V | Verifica | Verificare che tra le utenze proposte associate all'utenza ADN non compaia l'utenza disattivata allo step 2 e nemmeno si riesce ad associarla con l'apposito link in quanto viene visualizzato il messaggio "L'utente non esiste". |  |  | OK |
| TF001.UC11 | REQ-SIC-003 |  | Verifica reset password utenza SIES |  | Verifica: Verificare che nel caso sia stato effettuato il reset password di una utenza SIES, il sistema richieda di associare nuovamente l'utenza ed il cambio password prima di fare accedere al sistema. |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L’utente si trova sulla pagina di Login del SIES. Il sistema propone la pagina di accesso in cui l’utente sarà tenuto ad inserire le proprie credenziali ADN. | L'utente inserisce le proprie credenziali ADN | il sistema effettua un controllo sulla ‘autenticità’ delle informazioni inserite effettuando una chiamata LDAP sul server ADN di giustizia. |  |
|  | P | Stato Base | Il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione delle utenze SIES. |  |  |  |
|  | 1 | Azione | L’utente si ritroverà le utenze che utilizza solitamente per l’accesso al SIES. |  | Viene visualizzata la pagina con le utenze associate con il pulsante Entra ed il link ‘Seleziona/Configura un account’ | OK |
|  | 2 | Azione | L’amministratore di sistema di SIES ha eseguito il reset password di una delle utenze associate all'ADN dell'utente. |  | Il sistema effettua il reset password. | OK |
|  | 3 | Azione | L'utente clicca su Entra in corrispondenza dell'utenza a cui è stata effettuato il reset password. |  |  |  |
|  | V | Verifica | Verificare che il sistema prospetti il messaggio che l'utente ADN non è più associato alla utenza SIES. |  |  | OK |
|  | 4 | Azione | L'utente clicca sul logout dell'applicazione |  | L’utente si trova sulla pagina di Login del SIES. Il sistema propone la pagina di accesso in cui l’utente sarà tenuto ad inserire le proprie credenziali ADN. | OK |
|  | 5 | Azione | L'utente inserisce le proprie credenziali ADN |  | il sistema effettua un controllo sulla ‘autenticità’ delle informazioni inserite effettuando una chiamata LDAP sul server ADN di giustizia. | OK |
|  | 6 | Azione | Il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione profilazione delle utenze SIES. |  |  |  |
|  | 7 | Azione | L'utente seleziona la procedura di ‘Seleziona/Configura un account’ |  | Viene visualizzata la pagina per l’inserimento delle credenziali del SIES. | OK |
|  | 8 | Azione | L'utente inserisce le credenziali della utenza in cui è stato effettuato il reset password con password uguale alla utenza stessa e clicca su Login |  | Il sistema prospetta la pagina di cambio password | OK |
|  | 9 | Azione | L'utente inserisce la nuova password e clicca sul pulsante Salva Modifiche |  | Viene visualizzata la pagina con le utenze associate ed un messaggio in cui viene confermata la corretta associazione della nuova utenza. | OK |
|  | 10 | Azione | L'utente clicca su Entra in corrispondenza della utenza in cui è stato effettuato in precedenza il reset password |  |  |  |
|  | V | Verifica | Verificare che si riesca ad entrare nell'applicazione SIES. |  |  | OK |

## VerificheConformità

| Intervento |  |  | MEV-Integrazione SIES-ADN (PRE-GOLIVE) |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | SIUT-SIE-CT-1.1-20210531-Allegato_al_piano_test_MEV-Integrazione SIES-ADN (PRE-GOLIVE).xlsx |  |  |  |  |
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

| Intervento |  | MEV-Integrazione SIES-ADN (PRE-GOLIVE) |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  | SIUT-SIE-CT-1.1-20210531-Allegato_al_piano_test_MEV-Integrazione SIES-ADN (PRE-GOLIVE).xlsx |  |  |  |  |  |  |
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
| B |  | 5 |  |  |  |  |  |  |
| C |  |  | 3 | 2 |  |  |  |  |