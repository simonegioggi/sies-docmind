---
uniqueName: mev35-conversione-pene-pecuniarie-principali-per-m
displayName: "MEV 35   Conversione Pene Pecuniarie Principali per mancato pagamento"
category: "GENERAL"
tags: []
---

# MEV_35 - Conversione Pene Pecuniarie Principali per mancato pagamento

> **File originale:** `MEV/SCHEDA_035/MEV_35 - Conversione Pene Pecuniarie Principali per mancato pagamento.docx`  
> **Tipo:** DOCX

---

3.23	Conversione Pene Pecuniarie Principali per mancato pagamento
Gli artt. 102, 103 legge 689/1981 e art. 55 d. lgs. 274/00 prevedono che la pena pecuniaria non pagata possa essere convertita non più nella libertà controllata, bensì nella semilibertà e nella detenzione domiciliare sostitutive, oltre che nel lavoro di pubblica utilità.
Non conviene inserire i nuovi oggetti nell’attuale contenuto Conversione Pena Pecuniaria, in quanto per questi procedimenti è obbligatorio l’inserimento della Richiesta Conversione Pena Pecuniaria, con l’indicazione di tutti gli estremi (Anno/Numero Partiva IVA, Campione Penale, Autorità Richiedente, data irrevocabilità Titolo Esecutivo, etc.). Questi dati non sono necessari per la gestione dei procedimenti con Pena Pecuniaria sostitutiva in quanto la Procura si limiterà a trasferire l’importo di Pena Pecuniaria non pagato.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:
Conversione pene pecuniarie principali per mancato pagamento (artt. 102 - 103 L. 689/81 - 55 d. lgs. 274/00)   										U142
Al nuovo contenuto vanno associati i seguenti due oggetti:
Conversione pene pecuniarie principali per mancato pagamento (artt. 102 - 103 L. 689/81)	(3180)
Conversione pene pecuniarie principali per mancato pagamento (art. 55 d. lgs. 274/00)   	(3181)
ed i seguenti dodici esiti:
Dispone conversione in semilibertà sostitutiva  						(0276)
Dispone conversione in detenzione domiciliare sostitutiva   				(0277)
Dispone conversione in lavoro di pubblica utilità sostitutivo  				(0278)
Dispone conversione pena irrogata dal GdP in lavoro di pubblica utilità 			(0279)
Differisce la conversione  									(0158)
Dichiara NLP per irreperibilità – atti al PM  							(0150)
Dichiara NLP per accertata solvibilità    							(0151)
Dichiara NLP per intervenuta prescrizione   							(0152)
Dichiara N.D.P./ N.L.P  									(0004)
Dichiara inammissibilità  									(0003)
Dichiara la propria incompetenza  								(0005)
Rateizza pagamento  									(0159)
Questo tipo di procedimento non presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione, fuoriuscendo dalla logica procedimenti “padre” – “figli”, avverrà utilizzando le attuali funzionalità di iscrizione previste in SIUS.
Per questo tipo di procedimento sarà implementata una nuova funzionalità, emissione ordinanza conversione pene pecuniarie sostitutive (TIPO_ORDINANZA = ‘SR’): la nuova maschera di inserimento, che non richiederà la presenza dei dati della Conversione, sarà implementata sulla base di quella abbozzata di seguito (fare riferimento al contenuto U070 (Conversione/rateizzazione Pene Pecuniarie) per l’impostazione delle forms. A differenza di come funziona la suddetta ordinanza, per questo procedimento non bisogna ricercare il record RICHIESTA_CONVERSIONE, ma, se il procedimento è collegato a un procedimento SIEP, l’importo non pagato è quello presente sul provvedimento di avviso mancato pagamento del procedimento SIEP collegato, e il quantum di pena pecuniaria da convertire non viene “precompilato”, ma deve essere digitato dall’utente, in quanto può non coincidere con la somma riportata in Importo non pagato (questa ricerca è già stata fatta in Revoca e Conversione Pena Pecuniaria Sostitutiva).
La nuova maschera si differenzierà in base all’esito del provvedimento, in caso di rateizzazione:

Nella form bisogna gestire la rateizzazione come fatto in SIEP per le modalità di pagamento e si potrebbe acquisire i dati inserendo i records RATEIZZAZIONE_PP, collegata a FASCICOLO_SIUS, per cui bisognerà aggiungere un ulteriore colonna (FAS_SIU_ID_FASCICOLO_SIUS).
In caso di Conversione:

A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
Non inserendo più il record RICHIESTA_CONVERSIONE bisognerà aggiungere una colonna COD_TIPO_SANZIONE (in deposito_ordinanza_pc) per memorizzare il tipo di sanzione comminata.
Al momento per questo provvedimento saranno previsti tre modelli di stampa, che, quando generati, sono memorizzati in un campo BLOB della base dati:
ordinanza di conversione pena pecuniaria,
ordinanza di rateizzazione della pena pecuniaria,
ordinanza generica.
3.24	Conversione pene pecuniarie irrogate dal Giudice di Pace
L’art.  55 D.L. 274/2000 prevede che a richiesta del condannato la pena pecuniaria può essere convertita in lavoro di pubblica utilità, In caso di violazione degli obblighi del lavoro di pubblica utilità, la parte           residua si converte in obbligo di permanenza domiciliare.
Premessa alla gestione di questo nuovo contenuto è l’inserimento fra gli oggetti del fascicolo padre di ESS di un nuovo oggetto:
Lavoro di pubblica utilità
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:
Violazione obblighi lavoro pubblica utilità (art. 55 c. 3 DL 274/2000)  	U143
Al nuovo contenuto vanno associati il seguente oggetto:
Violazione obblighi lavoro pubblica utilità (art. 55 c. 3 DL 274/2000)  	(3185)
ed i seguenti cinque esiti:
Converte pena pecuniaria in permanenza domiciliare 			(0281)
Non converte   								(0212)
Dichiara N.D.P./ N.L.P  							(0004)
Dichiara inammissibilità  							(0003)
Dichiara la propria incompetenza  						(0005)
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà uguale a quella di tutti gli altri procedimenti figli dell’Esecuzione Pena Sostitutiva.
Per questo tipo di procedimento sarà utilizzata la stessa ordinanza del precedente paragrafo, solo nella modalità conversione e prevedere come pena sostitutiva solo la permanenza domiciliare.

La conversione di cui sopra determina come effetto diretto quello di imporre la creazione di un nuovo oggetto all’interno del contenuto ESS, che potremmo denominare “Permanenza domiciliare”.
A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
Al momento per questo provvedimento saranno previsti tre modelli di stampa, che, quando generati, sono memorizzati in un campo BLOB della base dati: ordinanza di sospensione della pena accessoria, ordinanza generica.
3.25	Rateizzazione Pena Pecuniaria
Considerato che (a quanto pare) la rateizzazione potrà essere concessa dal Magistrato di Sorveglianza solo in corso di esecuzione (o, quanto meno, prima dell’inizio ma sempre successivamente all’emissione del provvedimento di conversione), quindi dopo l’iscrizione di un procedimento di EPS.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:
Rateizzazione pena pecuniaria    	(U145)
Al nuovo contenuto vanno associati il seguente oggetto:
Rateizzazione pena pecuniaria   	(3195)
ed i seguenti cinque esiti:
Rateizza pagamento   		(0159)
Rigetta     				(0002)
Dichiara N.D.P./ N.L.P  		(0004)
Dichiara inammissibilità  		(0003)
Dichiara la propria incompetenza  	(0005)
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà uguale a quella di tutti gli altri procedimenti figli dell’Esecuzione Pena Sostitutiva.
Per questo tipo di procedimento sarà utilizzata la stessa ordinanza del paragrafo 3.23, prevista in caso di rateizzazione della pena pecuniaria. Modificare la intestazione della funzione in base all’oggetto.

A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
Al momento per questo provvedimento saranno previsti due modelli di stampa , che, quando generati, sono memorizzati in un campo BLOB della base dati: ordinanza di rateizzazione, ordinanza generica.