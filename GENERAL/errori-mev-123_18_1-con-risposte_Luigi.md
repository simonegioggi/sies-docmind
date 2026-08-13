---
uniqueName: errori-mev-123181-con-risposteluigi
displayName: "errori mev 123 18 1 con risposte Luigi"
category: "GENERAL"
tags: []
---

# errori mev 123_18_1 con risposte_Luigi

> **File originale:** `MEV/SCHEDA_009/errori mev 123_18_1 con risposte_Luigi.docx`  
> **Tipo:** DOCX

---

Nella maschera di deposito dell’ordinanza provvisoria (non esecutiva) compare anche di default il PM competente per l’esecuzione che, ovviamente, appare anche nella nota di trasmissione. In questa fase il PM dovrebbe scomparire per poi ricomparire quando l’ordinanza diventa esecutiva (divenendo visibile sulla conseguente nota di trasmissione)
Allo stesso modo, nella maschera successiva (vedi sotto) viene data la possibilità di effettuare la trasmissione telematica che invece, prima dell’esecutività, deve essere inibita
Per i punti 1 e 2 ribadiamo che la presenza della funzione di trasmissione non produce alcun effetto lato esecuzione, dove, come già avviene al momento per qualsiasi tipologia di procedimento SIUS, nell’Elenco procedimenti della Sorveglianza, disponibile in SIEP,  è riportato solo l’anno e numero del procedimento e il Contenuto, ma non vi è alcun riferimento all’avvenuta emissione dell’Ordinanza di applicazione provvisoria, come è possibile vedere nel seguente caso di test, in cui per il proc. 2022/133 del TDS è stata emessa, depositata e validata la suddetta ordinanza

Inoltre, al momento, non è stata ancora sviluppata alcuna funzionalità SIEP che possa gestire l’ordinanza di applicazione provvisoria. Quando svilupperemo la funzionalità di gestione, daremo la possibilità di operare solo su quelle in cui sia stata valorizzata la data esecutività.
Il deposito dell’ordinanza di applicazione provvisoria utilizza la preesistente funzionalità, valida per qualsiasi tipologia di procedimento. Se si vogliono realizzare le modifiche riportate nelle vostre segnalazioni, dobbiamo realizzare delle modifiche anche alla funzione di deposito.
Ricordavo che lato Siep era stata inibita la possibilità di gestire le nostre ordinanze provvisorie, però almeno il punto 1) andrebbe preso in considerazione, nel senso di eliminare il PM sia sulla maschera che sul relativo template.


Non è possibile modificare una ordinanza una volta depositata (manca l’icona di modifica nella stringa del provvedimento)
Abbiamo modificato la funzione Elenco Provvedimenti, allineando il comportamento dell’ordinanza di applicazione provvisoria e di conferma alle altre ordinanze   OK

La data entro la quale devono essere restituite le richieste istruttorie, correttamente inserita nella relativa maschera, non compare nel template
Non avevamo allineato i template sul Casellario, adesso dovrebbe essere riportata. OK
Mancano le icone di modifica e di cancellazione nella maschera “gestione restituzione atti al presidente”.
Confermo che è possibile modificare/cancellare la data restituzione, se sul procedimento, dovendo procedere con il rito ordinario, non sia stata già fissata o prefissata l’udienza. La funzione è attivabile da una delle due voci, contornate in rosso, nella successiva form
OK. ORA LE ICONE COMPAIONO

Dopo l’esecutività l’ordinanza deve essere nuovamente notificata alle parti ed alle altre Autorità competenti. Al momento è necessario svalidare il deposito e rientrare nella maschera dove è possibile inserire i destinatari. Sarebbe meglio, solo nel caso di ordinanza provvisoria esecutiva, riaccedere alla maschera di deposito direttamente dalla funzione ”Deposito ordinanza” senza svalidare nulla
Su questo punto non vi era stata un’analisi approfondita, avevamo dato la possibilità di produrre un nuovo template, il cui contenuto andava rivisto, alla luce dei test fatti da voi.

Quindi vi invitiamo ad apportare le necessarie modifiche al template e inviarcelo. Se c’è l’esigenza di agganciare gli stessi destinatari, inseriti al momento del Deposito possiamo già farlo, operando solo sul template.
Se poi vi è l’esigenza di inserire i destinatari, perché non indicati al momento del deposito, aggiungerne di nuovi, bisogna modificare l’attuale form di valorizzazione della data esecutività, visualizzando  i destinatari già indicati al momento del deposito e dando la possibilità di aggiungerne di nuovi. Da decidere se i destinatari indicati in fase di esecutività possano essere condivisi dalla funzione di Deposito.
LA MODIFICA DA EFFETTUARE E’ PROPRIO QUEST’ULTIMA, CON CONDIVISIONE DEI DESTINATARI
Quando si emette una ordinanza di “Conferma decisione …” nella maschera di emissione compare un nuovo oggetto “Conferma applicazione provvisoria …” e su questo viene indicato l’esito. Se si tratta di una scelta “tecnica”, si può lasciare; in caso contrario non si potrebbe lasciare solo l’oggetto precedente?
Si tratta di una scelta tecnica, in SIUS per lo stesso procedimento un oggetto viene conteggiato una sola volta, per cui in caso di Applicazione provvisoria e Conferma non sarebbe stato possibile conteggiarlo 2 volte.
OK
La maschera delle statistiche manca della parte dove è possibile selezionare le varie opzioni di ricerca
Ci si riferisce a questa form ?

Sul nostro server appaiono le 4 opzioni. Potreste inviarci la form che vi appare?
Io ho trovato tra le ricerche solo quella di cui alla maschera sottostante, ma non riesco a capire dove si trova quella di cui all’immagine precedente.