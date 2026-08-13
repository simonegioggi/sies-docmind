---
uniqueName: par-4-2-5-scheda-intervento
displayName: "par  4 2 5 Scheda Intervento"
category: "GENERAL"
tags: []
---

# par. 4.2.5 Scheda Intervento

> **File originale:** `MEV/SCHEDA_009/par. 4.2.5 Scheda Intervento.docx`  
> **Tipo:** DOCX

---

### REQ-SIE-009-05 TDS/TDSM - Provvedimento di Conferma Ordinanza Applicazione Provvisoria
A seguito dell’emissione dell’ordinanza provvisoria ed a partire dalla data in cui diviene esecutiva, il Tribunale, con decisione del collegio, conferma la decisione del Magistrato Designato.

Per proseguire con l’emissione del provvedimento di conferma, l’utente TDS/TDSM, dopo aver fissata una data udienza, deve procedere con la funzione di emissione ordinanza conferma decisione sullo stesso procedimento su cui è stata inserita l’ordinanza di applicazione provvisoria della misura (con data esecutività inserita).
In particolare, il requisito in oggetto, REQ-SIE-009-05, va ad estendere quanto già definito al requisito REQ-SIE-009-01 in quanto, per il contenuto “Concessione misure alternative (art. 678 comma 1-ter c.p.p.)” e per il contenuto “Concessione misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.)” devono essere previsti nuovi oggetti ed un nuovo esito.
Gli oggetti da prevedere sono:
Conferma appl. provv. Affidamento in Prova al S.S. (Art. 47 O.P. -  Art. 678 comma 1-ter c.p.p.)
Conferma appl. provv. Affidamento in Prova al S.S. (Art. 94 DPR 309/90 - Art. 678 comma 1-ter c.p.p.)
Conferma appl. provv. Detenzione Domiciliare (Art. 47 ter O.P. - Art. 678 comma 1-ter c.p.p.)
Conferma appl. provv. Semiliberta' (Art. 50 comma 1 O.P. - Art. 678 comma 1-ter c.p.p.)
Conferma appl. provv. Sospensione dell'Esecuzione della Pena (Art. 90 DPR 309/90 - Art. 678 comma 1-ter c.p.p.)
mentre l’esito è		Conferma Decisione del Magistrato Relatore

Per uniformità con la struttura Contenuto-Oggetti-Esiti di SIUS sono stati inseriti nella CG_REF_CODES

OGGETTO_PROCEDIMENTO	MACA		Conferma Misure Alternative brevi - Adulti	SER
OGGETTO_PROCEDIMENTO	MACM		Conferma Misure Alternative brevi -Minorenni		SER
per gli oggetti, in cui è stato inserito nella colonna RV_ALT2_VALUE il corrispondente valore dell’oggetto dell’ordinanza di Appl. Provv.
MOTIVO_PROVVEDIMENTO	0720	MACA		Conferma appl. provv. Affidamento in Prova al S.S. (Art. 47 O.P. -  Art. 678 comma 1-ter c.p.p.)	0680		CONCUM
MOTIVO_PROVVEDIMENTO	0721	MACA		Conferma appl. provv. Affidamento in Prova al S.S. (Art. 94 DPR 309/90 - Art. 678 comma 1-ter c.p.p.)	0681		CONCUM
MOTIVO_PROVVEDIMENTO	0722	MACA		Conferma appl. provv. Detenzione Domiciliare (Art. 47 ter O.P. - Art. 678 comma 1-ter c.p.p.)	0682		CONCUM
MOTIVO_PROVVEDIMENTO	0723	MACA		Conferma appl. provv. Semiliberta' (Art. 50 comma 1 O.P. - Art. 678 comma 1-ter c.p.p.)	0683		CONCUM
MOTIVO_PROVVEDIMENTO	0724	MACA		Conferma appl. provv. Sospensione dell'Esecuzione della Pena (Art. 90 DPR 309/90 - Art. 678 comma 1-ter c.p.p.)	0684		CONCUM
MOTIVO_PROVVEDIMENTO	0730	MACM		Conferma appl. provv. Affidamento in Prova al S.S. (Art. 47 O.P. -  Art. 678 comma 1-ter c.p.p.)	0690		CONCUM
MOTIVO_PROVVEDIMENTO	0731	MACM		Conferma appl. provv. Affidamento in Prova al S.S. (Art. 94 DPR 309/90 - Art. 678 comma 1-ter c.p.p.)	0691		CONCUM
MOTIVO_PROVVEDIMENTO	0732	MACM		Conferma appl. provv. Detenzione Domiciliare (Art. 47 ter O.P. - Art. 678 comma 1-ter c.p.p.)	0692		CONCUM
MOTIVO_PROVVEDIMENTO	0733	MACM		Conferma appl. provv. Semiliberta' (Art. 50 comma 1 O.P. - Art. 678 comma 1-ter c.p.p.)	0693		CONCUM
MOTIVO_PROVVEDIMENTO	0734	MACM		Conferma appl. provv. Sospensione dell'Esecuzione della Pena (Art. 90 DPR 309/90 - Art. 678 comma 1-ter c.p.p.)	0694		CONCUM

per l’esito:

ESITO_PROVVEDIMENTO	0271			Conferma Decisione del Magistrato Relatore
ESITO_TENORE			0700	MACA	0271	Conferma Decisione del Magistrato Relatore
ESITO_TENORE			0701	MACM	0271	Conferma Decisione del Magistrato Relatore

per la tipologia:

TIPO_ORDINANZA	CM			Ordinanza Conferma Applicazione Provvisoria Misura D.Lgs. 123/2018


Figura 15: Menù Emissione Ordinanza Provvisoria - (TDS e TDSM)

la voce del sottomenu ‘Applicazione Provvisoria M.A – Conferma Decisione Magistrato Relatore’, che presenta il seguente sottomenu:

da cui, selezionando la funzione ‘Conferma Decisione Magistrato Relatore’, il sistema, dopo aver controllato che sul procedimento risulti inserita l’ordinanza di applicazione provvisoria, la data di esecutività e la data dell’udienza (in caso di assenza di uno dei 3 dati invierà un messaggio bloccante all’operatore), presenterà la form per l’inserimento dell’ordinanza:


Figura 16: Pagina Emissione Ordinanza di Conferma Decisione Magistrato Relatore

che permette di inserire le seguenti informazioni:
Data Emissione (dato obbligatorio);
Eventuale descrizione a testo libero (dato opzionale);
l’oggetto sarà valorizzato automaticamente dal sistema in base al corrispondente oggetto applicato provvisoriamente con la ordinanza da confermare.
II sistema controllerà che la data di emissione sia = o > della data udienza.
A seguito della Conferma dei dati in maschera, il sistema inserirà nella base dati, oltre ai dati dell’ordinanza, il nuovo oggetto ed il nuovo esito. Dopo la validazione dell’ordinanza ed al suo deposito, il procedimento risulterà chiuso, in stato di “Emesso Provvedimento”.
Attenzione: a differenza di quanto avviene per tutti gli altri provvedimenti definitori, che provvedono a valorizzare la DATA_FINE dei precedenti records TENORE, in questo caso per i records della precedente ordinanza di applicazione provvisoria non bisogna valorizzare la DATA_FINE.
Il flusso di lavorazione del procedimento SIUS che abbia il nuovo contenuto ‘Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.)’ oppure ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 678 comma 1 ter c.p.p.)’ ed oggetto ‘Conferma Decisione del Magistrato relatore’, seguirà quello attualmente in essere per il contenuto ‘Concessione Misure Alternative Alla Detenzione’ (C001) con la gestione della modifica, visualizzazione, cancellazione, stampa, validazione e trasmissione. Le pagine di modifica, visualizzazione e la funzione di stampa devono prevedere in aggiunta a quanto ad oggi presente, l’informazione circa il numero e l’anno dell’ordinanza di ammissione provvisoria.
La funzione di trasmissione, deve prevedere l’invio dell’ordinanza di Conferma (Ratifica), verso la Procura titolare del titolo esecutivo per cui è stata presentata istanza di applicazione di misura alternativa.
Per tener conto statisticamente del doppio esito presente per questa tipologia di procedimento, nella statistica Monitoraggio per Oggetti bisognerà aggiungere due nuove colonne “Applicati Provvisoriamente” e “Conferma Decisione Magistrato Relatore”.