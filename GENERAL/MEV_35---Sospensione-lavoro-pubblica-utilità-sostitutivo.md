---
uniqueName: mev35-sospensione-lavoro-pubblica-utilit-sostituti
displayName: "MEV 35   Sospensione lavoro pubblica utilit\u00e0 sostitutivo"
category: "GENERAL"
tags: []
---

# MEV_35 - Sospensione lavoro pubblica utilità sostitutivo

> **File originale:** `MEV/SCHEDA_035/MEV_35 - Sospensione lavoro pubblica utilità sostitutivo.docx`  
> **Tipo:** DOCX

---

## 3.14		Sospensione lavoro pubblica utilità sostitutivo
L’art.  69 legge 689/1981, al secondo comma, prevede l’applicazione di una particolare forma di sospensione relativa esclusivamente al lavoro di pubblica utilità.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:
Sospensione lavoro di pubblica utilità sostitutivo (art. 69 c. 2 L. 689/81)  	(U137)
Al nuovo contenuto vanno associati i seguenti oggetti:
Sospensione lavoro di pubblica utilità sostitutivo (art. 69 c. 2 L. 689/81)  	(3156)
ed i seguenti esiti:
Sospende   				(0136)
Non sospende   				(0078)
Dichiara N.D.P./ N.L.P   			(0004)
Dichiara inammissibilità   		(0003)
Dichiara la propria incompetenza  	(0005)
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form d’iscrizione  e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto.
INTERVENTO DA REALIZZARE
Per questo tipo di procedimento sarà realizzata una nuova funzionalità, emissione del decreto Sospensione lavoro pubblica utilità sostitutivo: la nuova maschera di inserimento sarà simile a quella mostrata nel paragrafo 3.12 ma con l’aggiunta di alcuni campi come, per esempio, la data e la durata della sospensione.
Utilizziamo lo stesso Decreto Sospensione Esecuzione Pene Sostitutive, già oggetto d’intervento con precedente documento.
Bisogna apportare le seguenti modifiche alla form:


Bisogna aggiornare le diciture anche sul Dettaglio e Modifica.
A seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
Saranno previsti due modelli di stampa, che, quando generati, sono memorizzati in un campo BLOB della base dati: decreto generico e decreto di sospensione LPU.