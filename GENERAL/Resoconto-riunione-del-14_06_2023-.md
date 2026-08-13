---
uniqueName: resoconto-riunione-del-14062023
displayName: "Resoconto riunione del 14 06 2023 "
category: "GENERAL"
tags: []
---

# Resoconto riunione del 14_06_2023 

> **File originale:** `MEV/SCHEDA_033/Resoconto riunione del 14_06_2023 .docx`  
> **Tipo:** DOCX

---


Ministero della Giustizia
Gruppo di lavoro esecuzione e sorveglianza


S.I.E.P.

SISTEMA INFORMATIVO  ESECUZIONE PENALE
riforma cartabia

1.	Gestione pene pecuniarie	4
2.	Funzione non presente nella scheda.	6
3.	Interventi conseguenti alle decisioni del giudice dell’esecuzione	7
4.	Gestione pene detentive brevi	8
5.	Interventi sige	9



Oggetto: Resoconto riunione del 14/06/2023 –
Tavolo tecnico - m_dg.DOG07AR.14/02/2023.0000226.U - MEV 2023-13 - Pagamenti PagoPA per pene pecuniarie.

# Gestione pene pecuniarie
Si approva l’ultima versione della scheda pervenuta venerdì 09/06/2023 con l’integrazione delle sottostanti osservazioni.
Nel corso della riunione sono emerse delle osservazioni che riporto di seguito:
L’inserimento su tutte le schede di dettaglio la funzione ritorna indietro   che riporti alla scheda del menu “Gestione Riscossione Pene Pecuniarie”;

Migliorare la generazione dei bollettini dopo l’annotazione delle notifiche, creando un tasto funzionale, che nel caso della rata unica mi porti a consultare la scadenza del pagamento della rata.
Nel caso di generazione del bollettino, solo prima rata, alla generazione dei restanti bollettini con la scadenza già calcolata.

Eliminazione obbligatorietà del codice fiscale per la generazione del bollettino. Ci si riserva di tornare sull’argomento successivamente, ad oggi gli uffici non sono in grado di reperire il codice certificato, la presenza ad oggi è sui procedimenti iscritti tramite SNC.

Nota di trasmissione dei bollettini\o (argomento non discusso nel corso della riunione). Sarebbe opportuno creare una nota di accompagnamento. Si richiede di verificare fattibilità.

Nel corso della verifica è emersa una problematica, esposta durante la riunione, dovuta all’annullamento dell’ordine di ingiunzione in quanto errato. Si ipotizza l’errata indicazione della pena e rate.
Il sistema permette l’emissione del nuovo ordine di ingiunzione ed azzera:
la data di richiesta; data ricezione

| Data Richiesta | Data Ricezione |
| --- | --- |

Ma mantiene l’elenco dei bollettini

E permette la generazione di altri bollettini, in base ai nuovi parametri


La stressa ipotesi si può avere nel caso di rideterminazione della pena da parte del giudice dell’esecuzione e un eventuale cumulo.
Occorre rivedere la gestione:
Nel caso in esame la procedura dovrebbe essere legata all’ingiunzione e mantenere il dato precedente e memorizzarlo, in questo caso si perde il dato storico, annullare i bollettini su pagoPa, secondo le modalità ancora da stabilire, e creare un nuovo evento ed elenco generazione bollettini.
Il sistema non conteggia correttamente le scadenze delle rate,
Annotazione notifica

Scadenza errata.



# Funzione non presente nella scheda.
Ma che sarebbe opportuno realizzare per terminare tutta la parte relativa alla gestione delle pene pecuniarie
Scadenziario pagamenti
Si è convenuti, la funzione è stata più volte richiesta, di predisporre due funzioni di ricerca
Accertato pagamento della pena pecuniaria
La ricerca è finalizzata per poter emettere il provvedimento di estinzione
mancato pagamento della pena pecuniaria
La ricerca è finalizzata alla trasmissione degli atti al magistrato di 	sorveglianza per l’eventuale revoca.
Mancato pagamento di una delle rate
Il mancato pagamento, di una delle rate comporta la decadenza del beneficio del pagamento rateale, il sistema dopo l’annotazione del mancato pagamento, emette un nuovo provvedimento (Avviso di pagamento) con l’obbligo di pagare la parte residua della somma in un’unica soluzione entro i 60 giorni successivi dalla notifica dell’avviso.
Va creata una gestione simil ordine di ingiunzione (Avviso di mancato pagamento) con notifica al condannato,) difensore ed eventualmente al CO, generazione bollettino, Scadenziario. per la definizione della fase vale quanto detto sopra.
Scadenziario pagamenti
Si convenuti, la funzione è stata più volte richiesta, di predisporre due funzioni di ricerca:
Accertato pagamento della pena pecuniaria
La ricerca è finalizzata per poter emettere il provvedimento di estinzione
mancato pagamento della pena pecuniaria
La ricerca è finalizzata alla trasmissione degli atti al magistrato di 	sorveglianza per l’eventuale revoca.


# Interventi conseguenti alle decisioni del giudice dell’esecuzione

Art. 95 disposizioni transitorie in materia di pene sostitutive delle pene detentive;
Riduzione pena art. 442, comma 2-bis - D.lgs. 150/22
Le ordinanze emesse dal giudice dell’esecuzione di sostituzione pena, nella frase transitoria non trovano applicazione nell’applicativo Siep.
Dal momento che arrivano molteplici provvedimenti emessi dal giudice dell’esecuzione, sarebbe opportuno informatizzare le funzioni.
# Gestione pene detentive brevi
Per ottimizzare la trasmissione della nota al Magistrato di Sorveglianza si è richiesto di ottimizzare la gestione:
eliminando un passaggio intermedio per emettere la nota;
Integrare la maschera con ulteriori destinatari, sarà fornito un file specifico dove vengono esplicitare, in base alla posizione giuridica le autorità destinatarie del provvedimento;
Rivedere la gestione dell’emissione della nota e la successiva trasmissione al magistrato di sorveglianza.
Fornitura dei template per la gestione della misura secondo la posizione giuridica:
Libero;
Detenuto in custodia cautelare per questa causa;
Detenuto in custodia cautelare per questa causa in regime di arresti domiciliari\permanenza in casa\collocamento in comunità;
Custodia cautelare per altra questa causa in regime di detenzione
Detenuto in Custodia cautelare altra causa in regime di arresti domiciliari\permanenza in casa\collocamento in comunità;
Si segnala la necessità, improrogabile, su tutta la gestione scambio dati tra i due applicativi, Siep e Sius. La procedura di trasmissione attuale e su base volontaria, il risultato di conseguenza, è che solo il 5% dei provvedimenti perviene in elettronico.
L’esigenza è dovuta al fatto di tenere sempre il procedimento aggiornato per un eventuale provvedimento di cumulo.
# Interventi sige
Integrazione tabella oggetti
Contenuto:	Questioni relative alla iscrizione sul casellario (già presente)
Oggetto:	cancellazione iscrizioni (art. 5 comma 1 lettera c DPR 313/2002)
Esiti:		accoglie l’istanza
rigetta l’istanza;
dichiara il non luogo a provvedere;
dichiara il non doversi procedere;
dichiara l’inammissibilità;
dichiara la propria la propria incompetenza