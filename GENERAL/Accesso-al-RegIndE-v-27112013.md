---
uniqueName: accesso-al-reginde-v-27112013
displayName: "Accesso al RegIndE v 27112013"
category: "GENERAL"
tags: []
---

# Accesso al RegIndE v.27112013

> **File originale:** `MEV/SCHEDA_021/materiale analisi/documentazione_reginde/Accesso al RegIndE v.27112013.pdf`  
> **Tipo:** PDF

---

Accesso al RegIndE 
 
I servizi di Accesso al Reginde consentono di effettuare ricerche di soggetti ed enti censiti nel 
ReGIndE.   
La fruizione di tali servizi avviene tramite l’esposizione di due web-service. 
Il primo web service di accesso al ReGIndE è descritto nel contesto dell’allegato 
ServiziInterrogazioneSoggetto.wsdl. Per questo web service il namespace da utilizzare è 
“http://www.giustizia.it/serviziTelematici/reginde/interrogazioniExt”.  
Di seguito l’interfaccia dei metodi disponibili.  
 
Operazione: 
dettagliSoggettoPerCodice 
Descrizione: 
Ricerca i dettagli di un soggetto per codice fiscale 
Parametri: 
codice fiscale esatto del soggetto 
Risultato: 
soggetto: 
per maggiori informazioni consultare il wsdl 
 
 
Operazione: 
dettagliSoggettoPerIndirizzo 
Descrizione: 
Ricerca i dettagli di un soggetto per indirizzo 
Parametri: 
indirizzo 
Risultato: 
soggetto: 
per maggiori informazioni consultare il wsdl 
 
Operazione: 
elencoPaginatoSoggetti 
Descrizione: 
Restituisce un elenco paginato di soggetti 
Parametri: 
da: 
indice inizio ricerca 
count: 
numero di soggetti da ricercare 
Risultato: 
lista di soggetti:

per maggiori informazioni consultare il wsdl 
 
Operazione: 
isMembroDi 
Descrizione: 
Verifica che il soggetto appartenga all’Ente 
Parametri: 
codiceFiscale: 
codice fiscale del soggetto 
codiceEnte: 
codice dell’Ente 
Risultato: 
lista ruoli del soggetto censito 
 
Operazione: 
ricercaSoggetto 
Descrizione: 
Ricerca lista soggetti per cognome, nome o parti di essi e/o per 
codice dell'ente 
Parametri: 
cognome: 
cognome del soggetto eventualmente seguito dal carattere * 
nome: 
nome del soggetto eventualmente seguito dal carattere * 
codiceEnte: 
codice dell’Ente 
Risultato: 
lista di soggetti: 
per maggiori informazioni consultare il wsdl 
 
Operazione: 
ricercaSoggettoEx 
Descrizione: 
Ricerca lista soggetti per codice fiscale e/o indirizzo di PEC o 
parte di essi. 
Parametri: 
codiceFiscale: 
codice fiscale da ricercare o parte di esso 
indirizzo: 
indirizzo da ricercare o parte di esso 
Risultato: 
lista di soggetti: 
per maggiori informazioni consultare il wsdl

Il secondo web service è descritto dal file ServiziInterrogazioneEnte.wsdl, sotto si riportano le 
operazioni disponibili.  
Il namespace da utilizzare è:  
“http://www.giustizia.it/serviziTelematici/reginde/interrogazioni”.  
Di seguito l’interfaccia dei metodi disponibili.  
Operazione: 
ricercaEnte 
Descrizione: 
Ricerca Ente per descrizione 
Parametri: 
descrizione: 
descrizione ente 
 
Risultato: 
enti: 
per maggiori informazioni consultare il wsdl 
 
Operazione: 
dettagliEnte 
Descrizione: 
Ricerca Ente per codice 
Parametri: 
codiceEnte: 
codice dell’ente 
 
Risultato: 
enti: 
per maggiori informazioni consultare il wsdl 
 
Per le definizioni tramite WSDL dei web service che espongono  i metodi sopra descritti si rimanda 
agli allegati.