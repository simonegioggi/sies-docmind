---
uniqueName: par-4-2-4-scheda-intervento
displayName: "par  4 2 4 Scheda Intervento"
category: "GENERAL"
tags: []
---

# par. 4.2.4 Scheda Intervento

> **File originale:** `MEV/SCHEDA_009/par. 4.2.4 Scheda Intervento.docx`  
> **Tipo:** DOCX

---

### REQ-SIE-009-04 TDS/TDSM - Registrazione data Esecutività Ordinanza Applicazione Provvisoria
Per la registrazione della data di esecutività si prevede di aggiungere una nuova voce menù da inserire nella combo box presente nella maschera di dettaglio del procedimento SIUS.

Figura 11: Funzione Esecutività Applicazione Provvisoria m. a.
Dal punto di vista funzionale, l’attività di registrazione della data di esecutività dell’ordinanza di applicazione provvisoria si pone a valle dell’emissione dell’ordinanza provvisoria.
Accedendo alla funzione, il sistema, solo in caso di esistenza dell’ordinanza di Applicazione Provvisoria depositata e validata (esistenza di un EVENTO con cod_tipo_provvedimento = 03, cod_motivo=0680, cod_esito=0270, flag_documento_registrato = ‘S’ e di un DOCUMENTO_ALLEGATO con cod_tipo_documento =02 e flag_documento_registrato = ‘S’),  prospetta una nuova pagina in cui deve essere registrata la data di esecutività dell’ordinanza di applicazione provvisoria.
A seguire si mostra un esempio di pagina. Le informazioni da riportare sono:
Dettaglio procedimento SIUS
Dettaglio dati Soggetto
Estremi dell’ordinanza provvisoria di Concessione di Misura Alternativa (art. 678 comma 1 -ter)
Campo ‘Data Esecutività’
Campo note

Figura 12: Pagina Registrazione Esecutività - (TDS e TDSM)

I campi editabili sono ‘Data Esecutività’ e ‘note, che a seguito del conferma devono essere registrati nella tabella deposito_ordinanza_pc (colonne DATA_ESECUTIVITA e NOTE_ATTI).
Per la data di esecutività, che è dato obbligatorio da inserire, occorre prevedere, in caso di avvenuta valorizzazione delle date di notifica (operazione non obbligatoria), un controllo che segnali che il valore inserito superi i 10 giorni rispetto alla data dell'ultima notifica. Per una data che superi tale limite, visualizzare un messaggio di avviso sulla pagina con la conferma a procedere comunque con l’inserimento.

A seguito dell’inserimento, il sistema mostrerà una pagina di dettaglio dell’ordinanza di ammissione provvisoria, mostrando anche la data di esecutività inserita.
Dalla pagina di dettaglio, deve essere possibile accedere alla funzione di modifica della data di esecutività, inoltre deve essere abilitata la stampa, la validazione e la trasmissione telematica verso la Procura titolare del titolo esecutivo per cui è stata presentata istanza di applicazione di misura alternativa. La stampa deve includere anche una nuova nota di trasmissione del provvedimento contenente, oltre alla data dell’ordinanza e a quella di deposito, anche quella di esecutività. La gestione della ‘ricezione’ e ‘lavorazione’ dell’ordinanza di ammissione provvisoria su SIEP è illustrata al par. 4.3.1 [REQ-SIE-009-13].
Se è già presente la data di esecutività, il sistema presenterà la form di Dettaglio, da cui sarà possibile modificare o produrre la stampa o tornare al Dettaglio procedimento. Al momento non prevediamo alcuna validazione, a meno che non ci diranno di memorizzare la prima stampa prodotta e validarla. Esiste un template SIUS_OR_COMESECORD, sulla base della Nota Trasmissione dell'impugnazione, per l'annotazione data esecutività. Per il momento lo generiamo a volo ogni volta che cliccano sull'icona di stampa. L'xml da richiamare è lo stesso dell'emissione ordinanza. Far apparire la data di esecutività nell'elenco Provvedimenti (anche sul Dettaglio Procedimento), od aggiungendo una nuova colonna.
La data di esecutività impostata, inoltre, dovrà essere visualizzata nella porzione della maschera di dettaglio del procedimento SIUS dedicata ai provvedimenti, come mostrato nella figura che segue:

Figura 13: Sezione Provvedimenti con Data di Esecutività

La stessa informazione dovrà essere replicata nella pagina di dettaglio provvedimenti, che il sistema mostra in corrispondenza del link Provvedimenti.

Figura 14: Pagina Dettaglio Provvedimenti con Data di Esecutività

A seguito dell’emissione dell’ordinanza provvisoria e a partire dalla data in cui diviene esecutiva, si possono delineare diverse possibili gestioni operative, tra cui quelle che seguono:
Il Tribunale di Sorveglianza, conferma senza formalità la decisione del magistrato. (REQ-SIES-009-05)
Incorrere in una revoca dell’ammissione provvisoria, nel caso, ad esempio, di gravi violazioni delle prescrizioni nel corso dell’esecuzione provvisoria.
In questa prima fase di implementazione, illustriamo il dettaglio del primo scenario, ossia la casistica di ‘Conferma’ da parte del Tribunale della decisione del magistrato designato.
Lo scenario di cui al punto 2 è rinviato alla successiva fase di sviluppo (D.lgs. 123/2018 - FASE 2) cosi come specificato al par.5.2.