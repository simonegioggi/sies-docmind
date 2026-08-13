---
uniqueName: mev35-modifica-modalit-esecuzione-pene-sostitutive
displayName: "MEV 35   Modifica modalit\u00e0 Esecuzione Pene Sostitutive"
category: "GENERAL"
tags: []
---

# MEV_35 - Modifica modalità Esecuzione Pene Sostitutive

> **File originale:** `MEV/SCHEDA_035/MEV_35 - Modifica modalità Esecuzione Pene Sostitutive.docx`  
> **Tipo:** DOCX

---

## Modifica Modalità di esecuzione Pene Sostitutive
L’art. 64 e seguenti legge 689/1981 (vedi anche art. 107 L. 689/81) prevede di richiedere la Modifica delle modalità di esecuzione nel corso dell’esecuzione della pena sostitutiva.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:
Modifica modalità di esecuzione/luogo esecuzione pene sostitutive (art. 64 L. 689/81)  (U129 – S30)
Al nuovo contenuto vanno associati i seguenti oggetti:
Modifica modalità esecuzione semilibertà sostitutiva (art.  64  L.  689/81)   		(2925)
Modifica luogo esecuzione semilibertà sostitutiva (art.  64  L.  689/81)    		(2926)
Modifica modalità esecuzione detenzione   domiciliare sostitutiva (art.  64  L.  689/81)	(2927)
Modifica luogo esecuzione detenzione   domiciliare sostitutiva (art.  64  L.  689/81)   	(2928)
ed i seguenti esiti:
Modifica permanente prescrizioni   	(0264)
Modifica provvisoria prescrizioni      	(0265)
Modifica luogo esecuzione        		(0266)
Rigetta   				(0002)
Dichiara N.D.P./ N.L.P  			(0004)
Dichiara inammissibilità   		(0003)
Dichiara la propria incompetenza   	(0005)
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form d’iscrizione  e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto.
Per la definizione di questi procedimenti sarà implementata una nuova funzionalità, emissione del decreto Modifica Modalità di esecuzione Pene Sostitutive: la nuova maschera di inserimento sarà implementata sulla base di quella abbozzata di seguito. (fare riferimento al decreto previsto per U035)

A seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.

Per questo decreto saranno previsti quattro modelli di stampa, che, quando generati, sono memorizzati in un campo BLOB della base dati:
Decreto Modifica Modalità esecuzione
Decreto Modifica Luogo Esecuzione per Affidato
Decreto Modifica Luogo Esecuzione per Detenuto Domiciliare
Decreto Generico.

Interventi da realizzare sull’ordinanza e decreto

Al momento al contenuto U129 è stata associata la form utilizzata per il contenuto U035 Tipo_Decreto = 19
Dal debug sembra che in ambedue i casi venga richiamata /jsp/files/siap/sius/depositodecreto/InserisciDecretoModificaAttLuogoDet.jsp
La form presentata va sostanzialmente bene, andrebbero effettuate le modifiche riportate nei riquadri in rosso


La fase di inserimento è tutto OK, c’è da rivedere la form di Dettaglio



Stesso intervento anche sulla Modifica