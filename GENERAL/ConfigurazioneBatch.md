---
uniqueName: configurazionebatch
displayName: "ConfigurazioneBatch"
category: "GENERAL"
tags: []
---

# ConfigurazioneBatch

> **File originale:** `MEV/SCHEDA_013/Docs/Test/ConfigurazioneBatch.docx`  
> **Tipo:** DOCX

---

Il funzionamento base del batch dovrebbe essere quello di prelevare l'elenco dei bollettini generati e non ancora pagati e controllarli una alla volta ogni volta che il batch gira, ovvero una volta al giorno.
Al fine di contenere il numero di accessi effettuati dal Batch al sistema PST sono state utilizzate le seguenti strategie:
il batch non effettua il controllo puntuale dei bollettini ovvero non effettua una richiesta per ogni bollettino bensì effettua una richiesta per posizione debitoria ovvero Codice Fiscale. Il batch ricerca le Posizioni Debitorie che hanno almeno un bollettino da controllare. In questo modo se per un condannato sono presenti 20 bollettini da pagare verrà effettuata una sola transazione.
un bollettino non viene considerato da controllare per il semplice fatto di essere stato generato e non ancora pagato ma:
si può decidere di iniziare a controllare un bollettino in prossimità della sua scadenza e per  un certo numero di giorni dalla scadenza stessa. Per questo scopo è stato introdotto il parametro INSCADENZATRAGIORNI. AND ( DATA_SCADENZA BETWEEN (SYSDATE -[INSCADENZATRAGIORNI]) AND (SYSDATE + [INSCADENZATRAGIORNI]))
si può evitare di controllare i bollettini tutti i giorni. Tramite il parametro CONTROLLATEDAGIORNI si può istruire il batch di controllare un bollettino solo se è trascorso un certo tempo dall'ultimo controllo. Es 1 gg 2 gg

Va tenuto presente che il controllo del punto 2a è possibile solo in presenza della data di scadenza sul bollettino. Tale data viene valorizzata al momento delle registrazione della notifica al condannato dell'ordine di ingiunzione. Fino alla registrazione nel sistema SIEP di tale notifica, la data scadenza non sarà disponibile e il bollettino non verrà controllato.
E' stato richiesto di controllare comunque i bollettini privi di data scadenza, ovvero di notifica al condannato. Tale controllo quindi scatterebbe dal momento della generazione del bollettino fino al momento della registrazione della notifica. Da questo momento varrebbe la regola del punto 2a. Es genero i bollettini e invio l'ordine di ingiunzione al pagamento restando in attesa della notifica. Il bollettino inizia da subito ad essere controllato dal batch fino al momento della registrazione della notifica che avviene es 10 giorni dopo la generazione del bollettino. Da questo momento scattano i 90 giorni per il pagamento (o meglio dalla data di effettiva notifica ma per semplicità supponiamo che la registrazione sia fatta lo stesso giorno della notifica effettiva). Il bollettino non verrà più controllato per i successivi 87 giorni, e verrà poi controllato per un totale di 6gg in prossimità della scadenza della rata.
La vera domanda da porsi è per quale motivo si ha l'urgenza di controllare il bollettino dal momento della sua generazione (quando è privo di scadenza) fino alla sua notifica e poi non controllarlo più per 87 gg.
Cosa può accedere in quei giorni?
Il risultato è quello di un sovraccarico di chiamate a PagoPA perché un bollettino inizia ad essere controllato dal momento in cui viene generato, senza motivo, proprio ciò che si voleva evitare.
E' possibile limitare il controllo di tali bollettini privi di data scadenza solo per un numero limitato di giorni dalla data di generazione (GENERATIDAGIORNI) dopo la quale comunque si pretende la registrazione della notifica e quindi della data scadenza.
La giustificazione della necessità di tale controllo solo per i primi giorni?
Va considero che il batch, che gira tutti i giorni, è solo uno degli strumenti che ha a disposizioni l'ufficio per verificare se un bollettino sia stato pagato. L'ufficio per verificare l'avvenuto pagamento deve comunque entrare sul dettaglio della funzione "Verifica Stato Pagamento Bollettini per PagoPA" del singolo procedimento. Qui  può comunque lanciare la verifica puntuale dello stato di un pagamento qualora ne abbia la necessità. Es se il batch non lo ha controllato in quanto privo di data scadenza.

Sarebbe il caso di introdurre su tale tabella una ulteriore informazione relativa allo stato del controllo:
Data ultimo controllo.
Infatti l'esito "non pagato" ha senso solo se il controllo è stato effettuato ed ha dato esito negativo. In assenza del controllo non è possibile affermare che non sia stato pagato ma solo che non è stato controllato.
Si potrebbe aggiungere anche una nota che informa l'utente che in assenza della data notifica il bollettino non viene controllato in automatico ma in caso può essere controllato manualmente se ne ha la necessità.