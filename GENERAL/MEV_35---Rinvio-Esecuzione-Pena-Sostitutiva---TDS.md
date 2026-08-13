---
uniqueName: mev35-rinvio-esecuzione-pena-sostitutiva-tds
displayName: "MEV 35   Rinvio Esecuzione Pena Sostitutiva   TDS"
category: "GENERAL"
tags: []
---

# MEV_35 - Rinvio Esecuzione Pena Sostitutiva - TDS

> **File originale:** `MEV/SCHEDA_035/MEV_35 - Rinvio Esecuzione Pena Sostitutiva - TDS.docx`  
> **Tipo:** DOCX

---

3.16	Rinvio dell’esecuzione pena sostitutiva (TDS)
Per l’iscrizione questo tipo di procedimento segue il normale flusso previsto per l’iscrizione di un qualsiasi procedimento del Tribunale di Sorveglianza.
Nell’ambito del Tribunale di Sorveglianza (TDS/TDSM), il contenuto da integrare è il seguente:
•	Rinvio esecuzione Pena Sostitutiva Ex art. 684 comma 2 c.p.p.  (C064)
Al nuovo contenuto vanno associati i seguenti otto oggetti:
•	Differimento Pena Sostitutiva facoltativo art. 147 c.p. - art. 69 L. 689/81  		(9011)
•	Differimento facoltativo della Pena Sostitutiva in attesa di grazia – Art. 147 n. 1 c.p. - art. 69 L. 689/81 												(9012)
•	Differimento facoltativo della Pena Sostitutiva per grave infermità – Art. 147 n. 2 c.p. - art. 69 L. 689/81 											(9013)
•	Differimento facoltativo della Pena Sostitutiva per maternità – Art. 147 n. 3 c.p. - art. 69 L. 689/81 												(9014)
•	Differimento obbligatorio della Pena Sostitutiva nei confronti di donna incinta – Art. 146 n. 1 c.p. - art. 69 L. 689/81 										(9015)
•	Differimento obbligatorio della Pena Sostitutiva nei confronti di madre infante di età inferiore ad anni 1 – Art. 146 n. 2 c.p. - art. 69 L. 689/81  							(9016)
•	Differimento obbligatorio della Pena Sostitutiva nei confronti di persona affetta da malattia – Art. 146 n. 3 c.p. - art. 69 L. 689/81  								(9017)
•	Applicazione al semilibero della detenzione domiciliare sostitutiva – Art. 69 L. 689/81	(9018)
ed i seguenti sette esiti:
•	Concede per un periodo  						(0035)
•	Rigetta  								(0002)
•	Ratifica il provvedimento del mds e concede per un periodo di  		(0114)
•	Ratifica il provvedimento del mds e rigetta   				(0115)
•	Dichiara N.D.P./ N.L.P   							(0004)
•	Dichiara inammissibilità   						(0003)
•	Dichiara la propria incompetenza  					(0005)
Per questo tipo di procedimento sarà implementata una nuova funzionalità, emissione ordinanza di Rinvio Esecuzione Pena Sostitutiva: la nuova maschera di inserimento sarà implementata sulla base di quella abbozzata di seguito (utilizzare quella di C014, già allocata e funzionante a meno di alcune modifiche).

N.B.: I campi  saranno valorizzati solo se il procedimento corrente è stato iscritto collegandosi con il procedimento di rinvio dell’UDS.
A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.

IL tipo ordinanza va modificato anche nella form di Modifica
Al momento per questo provvedimento saranno previsti tre modelli di stampa , che, quando generati, sono memorizzati in un campo BLOB della base dati: Ordinanza di Rigetto Generico, Ordinanza di Rigetto Differimento della Pena, Ordinanza generica.

3.18	Rinvio dell’esecuzione pena sostitutiva derivante da Conversione Pene Pecuniarie (TDS)
Per l’iscrizione questo tipo di procedimento segue il normale flusso previsto per l’iscrizione di un qualsiasi procedimento del Tribunale di Sorveglianza.
Nell’ambito del Tribunale di Sorveglianza (TDS/TDSM), il contenuto da integrare è il seguente:
•	Rinvio dell’Esecuzione Pena Sostitutiva derivante da Conversione - artt. 69 – 107 L. 689/81”												(C065)
Al nuovo contenuto vanno associati i seguenti sette oggetti:
•	Differimento facoltativo della Pena Sostitutiva derivante da conversione in attesa di grazia – Art. 147 n. 1 c.p. - artt. 69 – 107 L. 689/81  						(9080)
•	Differimento facoltativo della Pena Sostitutiva derivante da conversione per grave infermità – Art. 147 n. 2 c.p. - artt. 69 – 107 L. 689/81  						(9081)
•	Differimento facoltativo della Pena Sostitutiva derivante da conversione per maternità – Art. 147 n. 3 c.p. - artt. 69 – 107 L. 689/81 							(9082)
•	Differimento obbligatorio della Pena Sostitutiva derivante da conversione nei confronti di donna incinta – Art. 146 n. 1 c.p. - artt. 69 – 107 L. 689/81   				(9083)
•	Differimento obbligatorio della Pena Sostitutiva derivante da conversione nei confronti di madre infante di età inferiore ad anni 1 – Art. 146 n. 2 c.p. - artt. 69 – 107 L. 689/81  	(9084)
•	Differimento obbligatorio della Pena Sostitutiva derivante da conversione nei confronti di persona affetta da malattia – Art. 146 n. 3 c.p. - artt. 69 – 107 L. 689/81  		(9085)
•	Applicazione al detenuto sottoposto alla Semilibertà Sostitutiva derivante da Conversione della Detenzione Domiciliare Sostitutiva - artt. 69 – 107 L. 689/81 			(9086)
ed i seguenti sei esiti:
•	Concede per un periodo   		(0035)
•	Proroga per un periodo   		(0219)
•	Rigetta     				(0002)
•	Dichiara N.D.P./ N.L.P   			(0004)
•	Dichiara inammissibilità   		(0003)
•	Dichiara la propria incompetenza  	(0005)
Per la definizione di questo tipo di procedimento sarà realizzata una nuova funzionalità, emissione dell’ordinanza Rinvio dell’esecuzione pena sostitutiva derivante da Conversione Pene Pecuniarie (TDS);
(utilizzare quella del paragrafo precedente, già allocata e funzionante a meno di alcune modifiche).

Il valore presente nel nuovo campo può essere memorizzato nella colonna SOMMA_RISARC_DANNI, che attualmente è un Number(9,2), da decidere se portarlo a (12,2).
Anche in questo caso va modificato il tipo ordinanza nella form di Dettaglio e Modifica, nel Dettaglio bisogna visualizzare anche la Pena Pecuniaria Convertita.
A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
Al momento per questo provvedimento saranno previsti due modelli di stampa, che, quando generati, sono memorizzati in un campo BLOB della base dati: ordinanza di rinvio esecuzione, ordinanza generica.