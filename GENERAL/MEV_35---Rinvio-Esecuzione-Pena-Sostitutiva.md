---
uniqueName: mev35-rinvio-esecuzione-pena-sostitutiva
displayName: "MEV 35   Rinvio Esecuzione Pena Sostitutiva"
category: "GENERAL"
tags: []
---

# MEV_35 - Rinvio Esecuzione Pena Sostitutiva

> **File originale:** `MEV/SCHEDA_035/MEV_35 - Rinvio Esecuzione Pena Sostitutiva.docx`  
> **Tipo:** DOCX

---

## 3.15		Rinvio dell’esecuzione pena sostitutiva (UDS)
Anche per le pene sostitutive si applica la disciplina prevista dall’art. 684 c.p.p. e, quindi, quella della decisione provvisoria del MdS e del successivo passaggio al TdS. Di conseguenza, si può riprendere, con le opportune modifiche, quanto già esistente sial lato UDS che TDS con riferimento alle SANZIONI SOSTITUTIVE.
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form d’iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne che per il contenuto e oggetto.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:
Rinvio esecuzione Pena Sostitutiva Ex art. 684 comma 2 c.p.p.    			(U138)
Al nuovo contenuto vanno associati i seguenti tre oggetti:
Differimento Pena Sostitutiva facoltativo art. 147 c.p. - art. 69 L. 689/81   	(3160)
Differimento Pena Sostitutiva obbligatorio art. 146 c.p. - art. 69 L. 689/81   	(3161)
Applicazione al semilibero della detenzione domiciliare sostitutiva – Art. 69 L. 689/81  (3162)
ed i seguenti sei esiti:’
Concede   								(0001)
Rigetta  								(0002)
Rinvia Esecuzione Nelle Forme della Detenzione Domiciliare  	(0041)
Dichiara N.D.P./ N.L.P   						(0004)
Dichiara inammissibilità   						(0003)
Dichiara la propria incompetenza  					(0005)
Per questo tipo di procedimento sarà implementata una nuova funzionalità, emissione del decreto Rinvio dell’esecuzione pena sostitutiva (UDS): la nuova maschera d’inserimento sarà implementata sulla base di quella abbozzata di seguito (fare riferimento a U003 Tipo_Decreto = 13).

A seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
Bisogna aggiornare anche le form di Dettaglio e Modifica, se necessario.
Al momento per questo provvedimento sono previsti i seguenti sei modelli di stampa, che, quando generati, sono memorizzati in un campo BLOB della base dati:
Decreto Incompetenza rinvio provvisorio esecuzione pena,
Decreto Inammissibilità rinvio provvisorio esecuzione pena,
Decreto Generico,
Decreto NDP/NLP rinvio provvisorio esecuzione pena,
Decreto Rigetto rinvio provvisorio esecuzione pena,
Decreto concessione rinvio provvisorio esecuzione pena.

## 3.17	Rinvio dell’esecuzione pena sostitutiva derivante da Conversione Pene Pecuniarie (UDS)
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form d’iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne che per il contenuto e oggetto.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:
Rinvio esecuzione Pena Sostitutiva derivante da Conversione - artt. 69 – 107 L. 689/81” (U139)
Al nuovo contenuto vanno associati i seguenti tre oggetti:
Differimento Obbligatorio Pena Sostitutiva derivante da Conversione - artt. 69 – 107 L. 689/81 	(3165)
Differimento Facoltativo Pena Sostitutiva derivante da Conversione - artt. 69 – 107 L. 689/81  	(3166)
Applicazione al detenuto sottoposto alla Semilibertà Sostitutiva derivante da Conversione della Detenzione Domiciliare Sostitutiva - artt. 69 – 107 L. 689/81   	(3167)
ed i seguenti sei esiti:
Concede  					(0001)
Proroga   					(0165)
Rigetta    					(0002)
Dichiara N.D.P./ N.L.P   			(0004)
Dichiara inammissibilità   			(0003)
Dichiara la propria incompetenza  		(0005)
Per la definizione di questo tipo di procedimento sarà realizzata una nuova funzionalità, emissione del decreto Rinvio dell’esecuzione pena sostitutiva derivante da Conversione Pene Pecuniarie (UDS): la nuova maschera d’inserimento sarà simile a quella mostrata nel paragrafo 3.15 ma con l’aggiunta dei campi concernenti la pena pecuniaria iniziale.
Si deve lavorare sulla stessa form del precedente paragrafo, ma in caso del presente contenuto la form deve presentare un ulteriore campo.


Il valore presente nel nuovo campo può essere memorizzato nella colonna SOMMA_RISARC_DANNI, che attualmente è un Number(9,2), da decidere se portarlo a (12,2).
A seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
Bisogna aggiornare anche le form di Dettaglio e Modifica, se necessario.
Al momento per questo provvedimento saranno previsti tre due modelli di stampa, che, quando generati, sono memorizzati in un campo BLOB della base dati:
Decreto di rinvio esecuzione,
Decreto generico.