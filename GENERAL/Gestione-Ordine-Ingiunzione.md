---
uniqueName: gestione-ordine-ingiunzione
displayName: "Gestione Ordine Ingiunzione"
category: "GENERAL"
tags: []
---

# Gestione Ordine Ingiunzione

> **File originale:** `MEV/SCHEDA_013/Docs/Test/Gestione Ordine Ingiunzione.docx`  
> **Tipo:** DOCX

---

Gestione Riscossione Pene Pecuniarie
Per la gestione di tutti gli aspetti connessi alla Riscossione delle Pene Pecuniarie ed all’Esecuzione delle Pene Sostitutive brevi, nell’attuale menu delle funzioni che il sistema presenta selezionando la voce “Gestione Altre Sanzioni”:

si aggiungeranno due nuove voci, di seguito racchiuse nel riquadro in rosso:

Al momento entrambe le voci presenteranno lo stesso menu di funzioni:

Gestione Ordine Ingiunzione
Selezionando la voce di menu Gestione Ordine Ingiunzione, il sistema presenterà la seguente form:

Notifiche
In questa MEV sarà realizzata solo la funzione di Notifica che permetterà, al momento dell’annotazione della data di avvenuta notifica al condannato, di far scattare gli scadenzari e che provvederà ad annotare nella base dati SIES le date di scadenza dei singoli bollettini.
La funzione è la stessa già disponibile per la gestione dell’ordine esecuzione con sospensione:


A differenza di quest’ultimo, che presenta l’ulteriore menu:

Che prevede l’annotazione separata della notifica al difensore e al Condannato, nel caso in esame, selezionando la voce Notifiche, il sistema presenterà la form   (caso di test  2021/14 PM Torino).
La funzione deve ricercare l’ultimo ordine esecuzione di ingiunzione al pagamento validato (EVENTO con cod_tipo_provvedimento = ‘06’ e cod_motivo = ‘0622’) , recuperare le relative notifiche e presentare la form:

In cui sarà possibile annotare l’avvenuta notifica al condannato, al difensore ed ai Civilmente Obbligati.
ARGOMENTO ANCORA DA APPROFONDIRE: Con l’annotazione dell’avvenuta notifica al condannato il sistema inserirà il procedimento nello scadenzario di pagamento della prima o unica rata, calcolando la data scadenza in base al n.ro giorni termine fissato per il pagamento della rata nell’ordine di ingiunzione (data avvenuta notifica + n.ro giorni termine).