---
uniqueName: cruscottoerrori
displayName: "CRUSCOTTO ERRORI"
category: "GENERAL"
tags: []
---

# CRUSCOTTO_ERRORI

> **File originale:** `MEV/SCHEDA_013/Docs/Test/CRUSCOTTO_ERRORI.docx`  
> **Tipo:** DOCX

---

# MEV_2023-33: Cruscotto degli Errori
Per la gestione degli errori delle richieste bollettini non andate a buon fine viene proposta la realizzazione di un cruscotto dedito alla visualizzazione di queste richieste.
Per popolare questa form verranno interrogate le tabelle:
BOLLETTINO_PAGOPA:

(aggiungendo una foreign key – BATCH_ID_BATCH_PAGOPA - su tabella BATCH_PAGOPA)
e BATCH_PAGOPA:

E creando una tabella di correlazione dove verranno inseriti oltre alle due primary key anche le informazioni circa l’esito negativo della richiesta:
stato (CARRELLO, ATTESA - che corrisponde agli stati DB INVIATA, OK_CARRELLO, OK_WISP, ERR_WISP, DIFF_WISP, KO_PSP, OK_PSP, GENERATA -, DISPONIBILE, USATO, RIMBORSATO, ERRORE - che corrisponde agli stati DB ERRORE e KO_CARRELLO -, REVOCATO), errore (Errore in fase di verifica + il messaggio dell'eccezione ottenuta), tipo errore (servizio assente oppure errore durante l’elaborazione), esito esecuzione;
Dalla form del cruscotto verrà data la possibilità di reindirizzare sul fascicolo siep per cui si è verificato l’errore, sia per l’interrogazione massiva (previa selezione dei bollettini da verificare) o puntuale del bollettino non verificato.
Di seguito, un esempio di form per il cruscotto degli errori:

Di seguito, la form per la schedulazione del batch in tempo reale:

Attenzione: per il cruscotto degli errori bisogna gestire le profilature per chi può solo visualizzarlo e chi, invece, dopo averlo visualizzato può compiere una azione correttiva (cioè rilanciare la richiesta di verifica stato bollettini).