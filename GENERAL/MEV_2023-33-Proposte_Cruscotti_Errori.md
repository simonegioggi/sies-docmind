---
uniqueName: mev2023-33-propostecruscottierrori
displayName: "MEV 2023 33 Proposte Cruscotti Errori"
category: "GENERAL"
tags: []
---

# MEV_2023-33-Proposte_Cruscotti_Errori

> **File originale:** `MEV/SCHEDA_033/MEV_2023-33-Proposte_Cruscotti_Errori.docx`  
> **Tipo:** DOCX

---

# MEV_2023-33: Cruscotti degli Errori (APPUNTI)
L’ipotesi è di realizzare due cruscotti per la gestione degli errori: uno per il batch ed l’altro per le funzionalità web.
PROPOSTA per il Cruscotto per funzionalità Batch
La funzione dovrebbe essere disponibile solo per l’utente con profilo di Amministratore di sistema.
Per la gestione degli errori delle verifiche, dello stato di pagamento dei bollettini generati, non andate a buon fine, tramite batch, viene proposta la realizzazione di un cruscotto dedito alla visualizzazione di queste verifiche.
Per popolare questa form verranno interrogate le tabelle:
BOLLETTINO_PAGOPA

(aggiungendo una foreign key – BATCH_ID_BATCH_PAGOPA - su tabella BATCH_PAGOPA)
e BATCH_PAGOPA

E creando una tabella di correlazione dove verranno inseriti oltre alle due Primary Key anche le informazioni circa l’esito negativo della richiesta:
Stato della richiesta, che contiene l’indicazione dello stato del pagamento nel contesto del PST e può assumere uno dei seguenti valori:
DISPONIBILE, indica che è presente la RT (sicuramente positiva) e non è stata utilizzata dall’utente
USATO, indica che il pagamento è stato utilizzato
OK_PSP, indica che l’utente ha eseguito un tentativo di pagamento ma ancora non è disponibile la RT
RIMBORSATO, indica che il pagamento è stato rimborsato dall’Amministrazione
errore (errore in fase di verifica più il messaggio dell'eccezione ottenuta)
tipo errore (servizio assente oppure errore durante l’elaborazione)
esito esecuzione
Dalla form del cruscotto verrà data la possibilità di reindirizzare sulla pagina di elenco bollettini controllati per cui si è verificato l’errore, sia per l’interrogazione massiva (previa selezione dei bollettini da verificare) o puntuale del bollettino non verificato.
Di seguito, un esempio di form per il cruscotto degli errori: separare errori con possibilità di schedulare il nuovo evento

Di seguito, la proposta di una eventuale form per la schedulazione del batch in tempo reale:

Attenzione: per il cruscotto degli errori bisogna gestire le profilature per chi può solo visualizzarlo e chi, invece, dopo averlo visualizzato può compiere una azione correttiva (cioè rilanciare la richiesta di verifica stato bollettini).
AMMINISTRATORE DI SISTEMA (1/2 persone) se è il caso di riprovare i batch in errore; Da verificare col gruppo funzionale!


PROPOSTA per il Cruscotto per funzionalità web
La funzionalità dovrebbe essere utilizzabile da parte dell’utente che ha riscontrato l’errore e dagli utenti con profilo di amministratore di ufficio.
Creazione della tabella Errori_SIES_PAGOPA:
| ID_ERRORI_SIES_PAGOPA | Number(38) |
| --- | --- |
| ID_FASCICOLO_SIEP | Number(38) |
| ID_EVENTO | Number(38) |
| AZIONE_CONTESTO_JAVA | VARCHAR2(100) |
| DESCRIZIONE_FUNZIONE | VARCHAR2(100) |
| COD_UTENTE | VARCHAR2(100) |
| COD_UFFICIO | VARCHAR2(11) |
| ERRORE_ESECUZIONE | VARCHAR2(2000) |
| DATA_INSERIMENTO | DATE |
| DATA_VISUALIZZAZIONE | DATE |
| COD_UTENTE_VISUALIZZAZIONE | VARCHAR2(100) |


Il sistema inserirà un record ogni volta che da applicazione verrà invocato il ws PST/PagoPA, il record verrà cancellato in caso di esito positivo della richiesta, in caso di esito negativo verrà valorizzata la colonna ERRORE_ESECUZIONE.
Al momento le funzionalità che invocano il ws PST/PagoPA sono: Richiesta Bollettini e Verifica Stato Bollettino su PagoPA.
La funzione potrà essere richiamata dall’utente, non amministratore di ufficio, dal menu:

attivata da questo menu la funzione filtrerebbe solo le richieste inoltrate dall’utente connesso, per le quali non ci sia stata risposta da PST/PagoPA.
Per l’utente Amministratore di Ufficio si inserirà la nuova voce nel menu verticale

Selezionandola si riceverà la seguente form:

In cui sarà possibile impostare dei filtri per data e per utente, a seguito dell’avvio della ricerca il sistema presenterà la seguente form:

Da verificare se selezionando l’azione di Dettaglio, si è in grado di visualizzare la maschera della funzione per re innescarla dal punto precedente al verificarsi dell’errore.
Da verificare col gruppo funzionale!
-----------------------------------------------------------------------------
TEST DI SISTEMA  aggiungere