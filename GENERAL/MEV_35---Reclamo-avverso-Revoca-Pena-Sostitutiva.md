---
uniqueName: mev35-reclamo-avverso-revoca-pena-sostitutiva
displayName: "MEV 35   Reclamo avverso Revoca Pena Sostitutiva"
category: "GENERAL"
tags: []
---

# MEV_35 - Reclamo avverso Revoca Pena Sostitutiva

> **File originale:** `MEV/SCHEDA_035/MEV_35 - Reclamo avverso Revoca Pena Sostitutiva.docx`  
> **Tipo:** DOCX

---

3.10	Reclamo avverso Revoca Pena Sostitutiva (per TDS)
L’ordinanza di revoca può essere impugnata dinanzi al TDS. Di conseguenza occorre inserire lato TDS un nuovo contenuto/oggetto, denominato “Reclamo avverso Revoca Pene Sostitutive” ed i cui esiti potrebbero essere: Accoglie reclamo; Accoglie reclamo e converte in altra pena sostitutiva; Rigetta; NLP; Inammissibilità; Incompetenza, utilizzando una maschera con alcuni dei dati particolari previsti in quella dell’UDS, vale a dire “Pena sostitutiva più grave” e “Rideterminazione quantum pena da espiare”.
Nell’ambito dell’Ufficio di Sorveglianza (TDS/TDSM), il contenuto da integrare è il seguente:
Reclamo avverso Revoca Pena Sostitutiva						(C063)
Al nuovo contenuto va associato il seguente oggetto:
Reclamo avverso Revoca Pena Sostitutiva   						(9010)
ed i seguenti sette esiti:
Accoglie reclamo    									(0269)
Accoglie reclamo e converte in altra pena sostitutiva   				(0273)
Convoca   										(0186)
Rigetta											(0002)
Dichiara N.D.P./ N.L.P  								(0004)
Dichiara inammissibilità    								(0003)
Dichiara la propria incompetenza 	  						(0005)
Per la definizione del procedimento sarà realizzata una nuova funzionalità, emissione dell’ordinanza Reclamo avverso Revoca Pena Sostitutiva (per TDS): la nuova maschera d’inserimento sarà implementata sulla base di quella abbozzata di seguito (bisogna creare un nuovo TIPO_ORDINANZA: RC OGGETTO_PROCEDIMENTO	 C063 S01 RC Reclamo avverso Revoca Pena Sostitutiva che si potrebbe adattare, duplicando quella realizzata per U131/U132).
Essendo un’ordinanza del TDS deve avere i controlli specifici, es. deve essere valorizzata la data udienza:

In cui nella combo box Pena Sostitutiva più grave il sistema presenterà le 3 pene sostitutive previste per il procedimento di esecuzione (vedi par. 3.2).

A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
Saranno previsti tre modelli di stampa, che, quando generati, sono memorizzati in un campo BLOB della base dati: Ordinanza Generica, ordinanza di accoglimento reclamo, ordinanza di rigetto reclamo.