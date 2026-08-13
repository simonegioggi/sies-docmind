---
uniqueName: propostegestione-foro-napoli-nord
displayName: "PROPOSTE GESTIONE FORO NAPOLI NORD"
category: "GENERAL"
tags: []
---

# PROPOSTE_GESTIONE FORO NAPOLI NORD

> **File originale:** `MEV/SCHEDA_021/materiale analisi/PROPOSTE_GESTIONE FORO NAPOLI NORD.docx`  
> **Tipo:** DOCX

---

GESTIONE FORO NAPOLI NORD

L’intervento per la gestione del FORO di NAPOLI NORD, verterà nello ‘svincolare’ l’entità del FORO dalla tabella COMUNE, facendo in modo che il dominio ‘FORO_AVVOCATI’ presente nella tabella cg_ref_codes sia indipendente ed auto consistente.
Il dominio ‘FORO_AVVOCATI’ sarà ‘responsabile’ di mappare la descrizione del FORO ed il codice (codice istat) del FORO. Tale informazione, in ottica di integrare le ricerche degli avvocati su RegINDE sarà utilizzata per l’accesso ai servizi di ricerca per FORO su RegINDE. Nello specifico, per il FORO DI NAPOLI NORD il codice ISTAT utilizzato sarà il codice del comune di AVERSA.
Si segnala che con la soluzione che si adotterà in relazione alla problematica FORO NAPOLI NORD non impatta con la gestione attuale che esiste sul sistema SIES in relazione al comune NAPOLI NORD censito nella tabella COMUNE. Pertanto il comportamento attuale circa l’utilizzo dell’entità comune NAPOLI NORD, NON SARA’ in alcun modo modificata con l’introduzione del FORO NAPOLI NORD.
La soluzione adottata delinea un perimetro di intervento che attiene esclusivamente all’entità FORO e la sua relazione con l’AVVOCATO.
Ciò significa che l’entità FORO sarà gestita in tutte le pagine che ad oggi già utilizzano l’informazione del foro di appartenenza di un DIFENSORE, ossia nelle pagine ove è prevista la notifica al DIFENSORE tramite UNEP.

In merito a ciò si espongono le due seguenti proposte:
PRIMA PROPOSTA di SOLUZIONE:
Per le notifiche al DIFENSORE si propone di utilizzare come descrizione del FORO associato all’Avvocato quella prevista, cioè NAPOLI NORD [vedi Esempio pagina testo sottolineato]; come sede dell’autorità UNEP relativa al Foro di Napoli Nord, invece, si propone di utilizzare il comune di AVERSA [vedi Esempio pagina riquadro];
Tutti i template che riportano l’informazione della sede UNEP, nei casi in cui la notifica sia inviata ad un avvocato del FORO NAPOLI NORD, mostreranno, ove previsto, come sede di riferimento il comune di AVERSA [vedere Esempio template 1 e 2 riportati di seguito];
Per le notifiche al DIFENSORE si propone di bloccare il salvataggio della coppia Autorità Destinazione (per qualsiasi autorità selezionata) con la sede NAPOLI NORD, con un messaggio del tipo: ”Attenzione! Napoli Nord non è un Comune Esistente”;
Allineare i tre sottosistemi a quanto detto al punto 1, 2 e 3.
Esempio pagina:


Esempio template 1:




Esempio template 2:



NOTA: La scelta di introdurre il comune di AVERSA come sede dell’autorità UNEP è strettamente correlata a quanto previsto nelle mappe degli Uffici Giudiziari pubblicate dal Ministero della Giustizia, in base alle quali l’UNEP ‘NAPOLI NORD’ è identificato con la seguente nomenclatura giudiziaria: “Unep presso il Tribunale di NAPOLI nord in AVERSA”.
In particolare, il Ministero riporta:
Descrizione dell’autorità: UNEP
Sede autorità giudiziaria: AVERSA
Tale premessa apre, però, ad un discorso più ampio sul sistema SIES, che riguarda anche le tipologie di uffici già censiti e presenti a sistema in corrispondenza del comune ‘fittizio’ di NAPOLI NORD.
Ad oggi, infatti, abbiamo:
Tribunale Ordinario NAPOLI NORD
Gip Presso il Tribunale Ordinario di NAPOLI NORD
Procura della Repubblica Presso il Tribunale Ordinario di NAPOLI NORD
Tutti questi uffici, nella gestione attuale, fanno riferimento alla sede di NAPOLI NORD, censita all’interno del SIES con un codice comune fittizio, mentre in realtà dovrebbero far riferimento alla sede del comune di AVERSA, come riportato negli elenchi degli Uffici Giudiziari pubblicati dal Ministero della Giustizia per cui le sedi degli uffici identificati di NAPOLI NORD fanno sempre capo alla sede giudiziaria di AVERSA.
Allineare il sistema a quanto su esposto nella sua interezza è un intervento ad alto impatto, viste le molteplici funzionalità coinvolte ed in considerazione del fatto che si renderebbe necessaria anche la gestione dei dati pregressi finora inseriti ed associati al comune ‘fittizio’ di NAPOLI NORD.

SECONDA PROPOSTA di SOLUZIONE:
Per le notifiche al DIFENSORE si propone di utilizzare come descrizione del FORO associato all’Avvocato quella prevista, cioè NAPOLI NORD [vedi Esempio pagina testo sottolineato] e come sede dell’autorità UNEP il comune ‘FITTIZIO’ di Napoli Nord [vedi Esempio pagina riquadro];
Per questa casistica, sempre per la sezione delle notifiche al DIFENSORE, occorre modificare il comportamento del tasto di selezione della sede, per fare in modo che la sede di NAPOLI NORD appaia come sede per la tipologia ‘Autorità di Destinazione’ UNEP;
Per le notifiche al DIFENSORE per mezzo UNEP il sistema permetterà di salvare il dato per la coppia Autorità di Destinazione UNEP – Sede NAPOLI NORD;
Tutti i template che riportano l’informazione della sede UNEP, nei casi in cui la notifica sia inviata ad un avvocato del FORO NAPOLI NORD, mostreranno, ove previsto, come sede di riferimento il comune ‘FITTIZIO’ di NAPOLI NORD [vedere Esempio template 1 e 2 riportati di seguito];
Per le notifiche al DIFENSORE per mezzo UNEP, si propone di allineare i sottosistemi SIEP, SIGE e SIUS a quanto specificato al punto 1, 2, 3 e 4.

Esempio pagina:




Esempio template 1:




Esempio template 2:




Dal punto di vista concettuale e di corretta gestione del dato “NAPOLI NORD” nei tre sottosistemi, si suggerisce di perseguire quanto indicato nella prima proposta di soluzione, considerando che quanto esposto nella NOTA non risulta vincolante per l’implementazione suggerita.