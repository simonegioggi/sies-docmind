---
uniqueName: par-4-2-3-scheda-intervento
displayName: "par  4 2 3 Scheda Intervento"
category: "GENERAL"
tags: []
---

# par. 4.2.3 Scheda Intervento

> **File originale:** `MEV/SCHEDA_009/par. 4.2.3 Scheda Intervento.docx`  
> **Tipo:** DOCX

---

### REQ-SIE-009-03 TDS/TDSM - Emissione Ordinanza Applicazione Provvisoria
Accedendo al sistema SIUS con utenza Tribunale di Sorveglianza (TDS/TDSM), in corrispondenza del menù ‘Ordinanze’, sarà introdotto un nuovo tasto funzione denominato ‘Applicazione Provvisoria M.A – Conferma Decisione Magistrato Relatore’


Figura 8: Menù Emissione Ordinanza Provvisoria - (TDS e TDSM)

che presenta il seguente sottomenu:


da cui, selezionando la funzione ‘Applicazione Provvisoria M.A.’, il sistema presenterà la form per l’inserimento dell’ordinanza di Applicazione Provvisoria di Misura Alternativa. La tipologia di ordinanza che viene emessa deve essere di tipo ‘ordinanza provvisoria’ e l’emissione di tale ordinanza non deve richiedere la fase di ‘Fissazione’ o ‘Prefissazione’ udienza. Deve essere gestita, quindi, come rito monocratico.
Dal punto di vista funzionale, l’emissione di un’ordinanza di Applicazione Provvisoria M.A. si inserisce a valle dell’inserimento del Decreto Presidenziale di Designazione.
Affinché possa essere emessa un’ordinanza di Applicazione Provvisoria M.A., infatti, il sistema deve controllare che, per il procedimento SIUS in lavorazione, sia stato emesso il Decreto di Designazione del magistrato relatore.
Nella casistica in cui non sia stato emesso il Decreto di Designazione, per dare seguito all’applicazione della misura, si procede con l’emissione dell’ordinanza (rito ordinario) cosi come esplicitato al par. 4.2.1, rientrando quindi nel classico giro del rito ordinario, quindi con la fissazione udienza e con l’emissione dell’ordinanza che applica o meno la misura.

La maschera per l’inserimento dell’ordinanza provvisoria, similmente all’emissione di un ordinanza generica deve permettere di poter inserire le seguenti informazioni:
Data Emissione
Contenuto
Oggetto
oltre all’inserimento del difensore, selezionando l’apposito link .

Figura 9: Emissione Ordinanza Applicazione Provvisoria M.A. - (TDS e TDSM)

mentre, nella pagina di inserimento degli esiti, ossia sulla pagina che il sistema mostra a seguito della ‘Conferma’, oltre alla combo box contenente gli esiti, devono essere previste, in aggiunta, le seguenti informazioni:
Un campo ‘check box’ con accanto la dicitura “ordinanza non emessa – restituzione atti al Presidente”.
Campo note (per eventuali motivazioni della restituzione degli atti).




Figura 10: Pagina esiti Ordinanza Provvisoria - (TDS e TDSM)

Gli esiti da prevedere sono quelli consueti, vale a dire “Applica Provvisoriamente”, “Rigetta”, “NLP”, “Inammissibilità” e “Incompetenza”.
Il magistrato emette ordinanza solo se Applica provvisoriamente la misura richiesta o, in caso di più misure richieste, ne applica una e si esprime negativamente sulle altre. In questo caso il sistema inserisce in base dati una nuova ordinanza, che dovrà essere validata e depositata. A seguito del deposito lo stato del procedimento sarà impostato a “Emessa Ordinanza Applicazione provvisoria”. Per questa nuova ordinanza sarà possibile stampare uno specifico documento, che sarà fornito dall’Amministrazione.
Nel caso in cui il magistrato relatore ritenga di non poter applicare alcuna delle misure concedibili, egli dovrà limitarsi a rimettere gli atti al Presidente del Tribunale di Sorveglianza, il quale provvederà secondo il tradizionale procedimento ex articolo 678, comma 1 del codice di procedura penale, predisponendo il contraddittorio. Anche in questo caso il magistrato utilizzerà la funzione Ordinanza Applicazione Provvisoria, ma si limiterà a valorizzare la Data Emissione, impostare il ‘check box’ Ordinanza non emessa – Atti al Presidente  e a valorizzare eventualmente il campo Note. A seguito della Conferma il sistema si limiterà ad annotare sul procedimento i dati inseriti e a impostare lo stato del procedimento SIUS a ‘Restituiti Atti al Presidente’.
La ‘Non Emissione’ dell’ordinanza determina comunque la chiusura della fase provvisoria in maniera alternativa rispetto alla ordinaria indicazione degli esiti. La procedura a questo punto segue il suo corso normale con l’apertura del dibattito. Quindi il TDS/TDSM fissa udienza ed emette ordinanza.
Caratteristica fondamentale dell’ordinanza del magistrato designato di Applicazione Provvisoria di Misura Alternativa, è la sua non immediata esecutività. Ciò significa che a seguito di esito ‘Applica Provvisoriamente’, l’ordinanza successivamente al deposito e relativa validazione, sarà visibile, come già avviene per tutte le altre ordinanze già disponibili nel sistema, lato SIEP, ma non sarà gestibile in quanto non vi sarà disponibile una specifica funzione che ne permetta la gestione in assenza della data di esecutività. per l’ordinanza in lavorazione, devono essere consentite le fasi di validazione e deposito, ma inibita la trasmissione della stessa verso la Procura. Deve essere possibile, invece, effettuare la stampa dell’ordinanza provvisoria, prevedendo un nuovo template.
L’ordinanza, depositata, diverrà esecutiva una volta trascorsi 10 giorni senza che venga proposta opposizione e, in virtù di ciò, deve essere prevista la possibilità di annotare, ed evidenziare nella maschera di dettaglio del procedimento SIUS, la data di esecutività della stessa. La descrizione di tale funzionalità è esposta nel paragrafo successivo.

Nella casistica, invece, in cui venga presentata opposizione, detta opposizione va annotata sul procedimento “provvisorio” utilizzando l’apposita funzione “Impugnazioni/Opposizioni”. Per la gestione delle impugnazioni, il procedimento SIUS seguirà il medesimo processo di lavorazione già in essere per il contenuto ‘Concessione Misure Alternative Alla Detenzione’ (C001).

In caso di procedimento in stato di ‘Atti Restituiti al Presidente’ per poter gestire correzioni ai dati inseriti o l’annullamento dello stato, sarà realizzata una nuova funzione ‘Gestione Restituzione Atti al Presidente’, che sarà disponibile nell’elenco delle funzioni attivabili dal Dettaglio Procedimento.



La funzione presenterà il Dettaglio dei dati relativi alla restituzione degli atti presenti nella base dati



da questa form sarà possibile selezionare le azioni di Modifica o di Cancellazione.
In caso di cancellazione lo stato del procedimento sarà reimpostato a ‘Emesso Decreto Designazione’.