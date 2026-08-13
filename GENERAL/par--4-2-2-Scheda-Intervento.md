---
uniqueName: par-4-2-2-scheda-intervento
displayName: "par  4 2 2 Scheda Intervento"
category: "GENERAL"
tags: []
---

# par. 4.2.2 Scheda Intervento

> **File originale:** `MEV/SCHEDA_009/par. 4.2.2 Scheda Intervento.docx`  
> **Tipo:** DOCX

---

### REQ-SIE-009-02 TDS/TDSM - Emissione del Decreto Presidenziale di Designazione
Sempre in riferimento al comma 1 ter all’articolo 678 c.p.p., per procedimenti relativi a condanne per pene fino a 18 mesi, l’ufficio Tribunale di Sorveglianza (TDS/TDSM), in tema di semplificazione della procedura, designa il magistrato relatore e fissa un termine entro il quale questi, con ordinanza adottata senza formalità, può applicare in via provvisoria una delle misure menzionate nell'articolo 656, comma 5.
L’adeguamento del sistema SIUS a tale normativa si delinea nell’implementazione che si espone a seguire.
Accedendo al sistema SIUS con utenza Tribunale di Sorveglianza (TDS/TDSM), in corrispondenza del menù ‘Decreti’, sarà introdotto un nuovo tasto funzione denominato ‘Designazione Magistrato Relatore’.


Figura 5: Menù Decreti -  Decreto Presidenziale di Designazione - (TDS e TDSM)
L’accesso alla funzione ‘Designazione Magistrato Relatore’ mostrerà una nuova maschera per inserire il decreto in oggetto, solo in caso dei contenuti riportati di seguito, diversamente invierà un messaggio bloccante all’utente, che ne inibirà l’utilizzo.
Dal punto di vista funzionale il Decreto di Designazione, va inserito dopo l’iscrizione di un procedimento SIUS con contenuto “Concessione misure alternative (art. 678 comma 1-ter c.p.p.)” oppure con contenuto “Concessione misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.)”.

Pertanto, l’utente:
Inserisce un nuovo procedimento SIUS di “Concessione misure alternative (art. 678 comma 1-ter c.p.p.)” per TDS, oppure Inserisce un nuovo procedimento SIUS di “Concessione misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.)” per TDSM;
Emette, nei casi previsti dal decreto, il decreto Presidenziale di Designazione.

Tramite questa funzione il Tribunale di Sorveglianza va a designare il magistrato relatore che può applicare in via provvisoria, in riferimento a procedimenti relativi a condanne per pene fino a 18 mesi, una delle misure menzionate nell'articolo 656, comma 5.
La maschera per l’inserimento del decreto deve permettere pertanto, di poter inserire le seguenti informazioni:
Data Emissione
Magistrato Relatore designato (di default sarà visualizzato il nominativo del magistrato a cui è già stato assegnato il procedimento in fase di iscrizione (secondo la ripartizione tabellare) con la possibilità, ovviamente, di modificare l’originaria assegnazione)
Contenuto (valore fisso, corrispondente al contenuto - Concessione misure alternative (art. 678 comma 1-ter c.p.p.), per TDS, oppure Concessione misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.), per TDSM, selezionato in fase di iscrizione del procedimento SIUS
Oggetto (selezionabile dalla lista degli oggetti associati al contenuto - Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ed al contenuto Concessione misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.)
Data Termine Emissione ordinanza provvisoria/Restituzione atti al presidente (dove indicare il termine entro il quale il magistrato dovrebbe provvedere all’emissione dell’ordinanza di ammissione provvisoria o di restituzione degli atti al Presidente, esprimibile con una data o numero giorni, si tratta di un dato obbligatorio).

Figura 6: Pagina di inserimento del Decreto Designazione Magistrato - (TDS e TDSM)
Caratteristica fondamentale di tale decreto è che a seguito dell’inserimento e validazione dello stesso, il procedimento in lavorazione non deve essere chiuso.
Per tale decreto deve essere creato un documento di stampa ad hoc che sarà fornito dall’Amministrazione.
Si evidenzia che per questo decreto non è necessaria l’avvenuta nomina di un avvocato.
Lo stato del procedimento, a seguito della validazione del Decreto di Designazione, sarà impostato a ‘Emesso Decreto Designazione’, mentre l’esito da associare al decreto è ‘Designa Magistrato art. 678 1-ter c.p.p.’. L’introduzione di un nuovo stato procedimento e nuovo esito si giustifica per la corretta individuazione dei procedimenti SIUS ai fini delle elaborazioni statistiche dettagliate ai par.4.2.6.1 e 4.2.6.3. Per questo decreto, come già avviene per il decreto di Fissazione Udienza, non è obbligatorio procedere.

In caso di procedimento ancora privo di Magistrato assegnatario, nel momento in cui, tramite il Decreto di designazione, viene individuato il Magistrato, il sistema deve aggiornare in automatico il magistrato assegnatario presente nella maschera di dettaglio del procedimento SIUS.
Qualora il magistrato assegnatario del procedimento fosse già stato assegnato precedentemente all’emissione del decreto, e dovesse differire dal magistrato designato con il decreto, il sistema invierà un messaggio di avviso della discrepanza, es.


chiedendo conferma per poter procedere automaticamente alla sostituzione del magistrato assegnatario con quello indicato in maschere, operazione che effettuerà in caso di conferma da parte dell’utente. Nel caso di risposta negativa, il sistema, si riposizionerà sulla form, permettendo d poter selezionare il magistrato relatore corretto e di riconfermare i dati.
Il magistrato, ricevuta la designazione, se ritiene di poter concedere una delle misure alternative previste dall’art. 656 comma 5 c.p.p., e non necessariamente quella richiesta dal condannato, emette de plano un’ordinanza di applicazione provvisoria.

La gestione dell’ordinanza di applicazione provvisoria sarà descritta nel paragrafo successivo.