---
uniqueName: mev35-gestione-licenza-ps
displayName: "MEV 35   Gestione Licenza PS"
category: "GENERAL"
tags: []
---

# MEV_35 - Gestione Licenza PS

> **File originale:** `MEV/SCHEDA_035/MEV_35 - Gestione Licenza PS.docx`  
> **Tipo:** DOCX

---

## 3.12	Gestione Licenza - pene sostitutive
L’art. 69 legge 689/1981, al primo comma, prevede un istituto parzialmente nuovo per le licenze per i soggetti sottoposti a pene sostitutive.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:
Licenza - pene sostitutive (art. 69 L. 689/81)   	(U135)
Al nuovo contenuto vanno associati i seguenti oggetti:
Licenza - pene sostitutive (art. 69 L. 689/81)  	(3130)
ed i seguenti cinque esiti:
Concede  					(0001)
Rigetta   					(0002)
Dichiara N.D.P./ N.L.P  				(0004)
Dichiara inammissibilità    			(0003)
Dichiara la propria incompetenza 	  	(0005)
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form d’iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne che per il contenuto e oggetto.
Per questo tipo di procedimento sarà implementata una nuova funzionalità, emissione del decreto Gestione Licenza - pene sostitutive: la nuova maschera d’inserimento sarà implementata sulla base di quella abbozzata di seguito.  (utilizzare decreto per U006, già allocato e funzionante)
Bisogna aggiungere nell’intestazione dell’Emissione Decreto il riferimento a PENE SOSTITUTIVE in caso di U135:

Stessa implementazione anche sul Dettaglio
In fase d’inserimento del Decreto, quando s’inserisce il record LICENZA_LIBANTICIPATA, la colonna COD_TIPO_LICENZA = ‘LP’ invece di LC o di LI. Anche sul Dettaglio, se serve, deve recuperare questo tipo di licenza.
A seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
Per questo decreto saranno previsti quattro modelli di stampa, che, quando generati, sono memorizzati in un campo BLOB della base dati:
Decreto generico,
Decreto concessione licenza,
Decreto Rigetto licenza,
Decreto Inammissibilità licenza.
Template:
SIUS_DE_CONCLICPS.rtf,
SIUS_DE_INAMMLICPS.rtf,
SIUS_DE_RIGETTOLICPS.rtf,
SIUS_DE_MODGENERICO.rtf

## 3.13	Licenza - pene sostitutive - Inosservanza prescrizioni (art. 69 L. 689/81)
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:
Licenza - pene sostitutive – inosservanza prescrizioni (art. 69 L. 689/81)  		(U136)
Al nuovo contenuto vanno associati i seguenti oggetti:
Valutazione revoca licenza – pene sostitutive (Art. 53 bis O.P. – 69 L. 689/81		(3150)
Esclusione computo Licenza – pene sostitutive (artt. 53 bis O.P. - 69 L. 689/81)   	(3151)
ed i seguenti cinque esiti:
Revoca   					(0006)
Non Revoca   					(0008)
Dichiara validamente espiata la pena   		(0012)
Dichiara non validamente espiata la pena   	(0013)
Dichiara N.D.P./ N.L.P  				(0004)
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form d’iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne che per il contenuto e oggetto.
Per questo tipo di procedimento sarà implementata una nuova funzionalità, emissione del decreto per la Licenza per internati – inosservanza prescrizioni: la nuova maschera d’inserimento sarà implementata in conformità a quella abbozzata di seguito (utilizzare il decreto per U069/U033, già allocato e funzionante).

In fase di Inserimento dovrebbero essere valide tutte le operazioni già eseguite nell’attuale Decreto, sempre che non vi sia, ma non penso, riferimento al “cod_tipo_licenza”.
A seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
Al momento per questo provvedimento saranno previsti due modelli di stampa, che, quando generati, sono memorizzati in un campo BLOB della base dati:
Decreto revoca licenza,
Decreto scomputo licenza.
Template:
SIUS_DE_SCOMPUTOLICPS.rtf,
SIUS_DE_REVOCALICPS.rtf
Bisogna inserire la stampa del tag DescrTipoProcuraEsecuzione, dopo l’avvenuta modifica dell’XML, in cui nel ramo <DepositoDescreto> oltre al tag <DescrProcuraEsecuzione> bisognerebbe aggiungerne uno nuovo con la descrizione del tipo procura o inserire tutto nell’attuale tag, in modo da avere es. PROCURA DELLA REPUBBLICA PRESSO IL TRIBUNALE ORDINARIO TORINO.