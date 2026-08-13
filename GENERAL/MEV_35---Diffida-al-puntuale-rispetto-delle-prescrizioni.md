---
uniqueName: mev35-diffida-al-puntuale-rispetto-delle-prescrizi
displayName: "MEV 35   Diffida al puntuale rispetto delle prescrizioni"
category: "GENERAL"
tags: []
---

# MEV_35 - Diffida al puntuale rispetto delle prescrizioni

> **File originale:** `MEV/SCHEDA_035/MEV_35 - Diffida al puntuale rispetto delle prescrizioni.docx`  
> **Tipo:** DOCX

---

## 3.11	Diffida al puntuale rispetto delle prescrizioni – pene sostitutive
Considerato che l’istituto delle pene sostitutive dovrebbe avere una ampia diffusione, è opportuno inserire anche un contenuto specifico per la diffida, sulla falsariga di quanto accade nel caso di EMA.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:
Diffida al puntuale rispetto delle prescrizioni - pene sostitutive 	(U133 – S30)
Al nuovo contenuto vanno associati i seguenti oggetti:
Convocazione per puntuale rispetto prescrizioni – pene sostitutive   	(3126)
Diffida al puntuale rispetto prescrizioni – pene sostitutive    		(3127)
ed i seguenti esiti:
Diffida    				(0127)
Non Diffida    				(0274)
Convoca     				(0186)
Non Convoca    			(0187)
Dichiara N.D.P./ N.L.P  			(0004)
Dichiara inammissibilità    		(0003)
Dichiara la propria incompetenza 	(0005)
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form d’iscrizione  e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto.
INTERVENTI DA REALIZZARE
Per la definizione questi procedimenti sarà implementata una nuova funzionalità, emissione del decreto Diffida al puntuale rispetto delle prescrizioni – pene sostitutive: la nuova maschera di inserimento sarà implementata sulla base di quella abbozzata di seguito.

Per questo decreto si può utilizzare quello previsto per contenuto U056, apportando le modifiche evidenziate sull’attuale form in caso di contenuto U133.

A seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
L’attuale Decreto in fase di Inserimento già funziona correttamente, non essendo i campi da eliminare obbligatori.
Modificare anche le forms di Dettaglio e Modifica.



Per quanto riguarda la stampa, saranno previsti due modelli, che, quando generati, sono memorizzati in un campo BLOB della base dati: Decreto generico, Decreto diffida puntuale rispetto prescrizioni.