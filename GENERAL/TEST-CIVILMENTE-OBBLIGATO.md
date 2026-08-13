---
uniqueName: test-civilmente-obbligato
displayName: "TEST CIVILMENTE OBBLIGATO"
category: "GENERAL"
tags: []
---

# TEST CIVILMENTE OBBLIGATO

> **File originale:** `MEV/SCHEDA_013/Docs/Test/TEST CIVILMENTE OBBLIGATO.docx`  
> **Tipo:** DOCX

---

TEST CIVILMENTE OBBLIGATO
INSERIMENTO PERSONA FISICA
Singola:
accetta la valorizzazione sia del comune di nascita Italia, che del comune nascita estero dovrebbero essere alternativi e legati allo stato nascita. Analogo problema sulla residenza.
Se non valorizzo la residenza, il sistema inserisce comunque un record quasi vuoto in residenza, collegato al civilmente obbligato. Dobbiamo controllare che l’inserimento avvenga solo se sono valorizzati l’indirizzo e il comune o il comune estero.
Doppia:
Stessi problemi dell’inserimento singola persona, nel Dettaglio mi presenta le due persone nell’ordine inverso dell’inserimento, secondo me dobbiamo ordinarle per id_civilmente_obbligato.
Non inserisce le due residenze se le valorizzo.
MODIFICA
Singola:
Non presenta la residenza se presente in base dati, se la rivalorizza in maschera ne inserisce un’altra, che in ogni caso non ripresenta.
Non effettua mai la modifica dei dati della residenza, va sempre in inserimento.
Doppia:
Stessi problemi dell’inserimento singola persona, nella form mi presenta le due persona nell’ordine inverso all’inserimento, secondo me dobbiamo ordinarle per id_civilmente_obbligato.
Non inserisce le due residenze se le valorizzo. Se le valorizzo nuovamente e confermo ne acquisisce solo una.
Non effettua mai la modifica dei dati della residenza, va sempre in inserimento.
DETTAGLIO
Non presenta la residenza del secondo CIVILMENTE OBBLIGATO, probabilmente a causa delle problematiche a livello di inserimento della stessa.
Ordinare i records CIVILMENTE_OBBLIGATO per id_civilmente_obbligato.
CANCELLAZIONE
OK
INSERIMENTO PERSONA GIURIDICA
Dopo aver compilato la form alla conferma ricevo il seguente errore:
F3BException --> Eccezione di sistema:
Il parametro 'Cognome_ST' non esiste nella FORM
Ho verificato che ha correttamente inserito i dati nella tabella CIVILMENTE_OBBLIGATO, ma nessun record in RESIDENZA.
Nella combo box "Ragione Sociale" della persona giuridica vanno tolte le attuali voci e inserito il '-' ed 'Ente'!!!