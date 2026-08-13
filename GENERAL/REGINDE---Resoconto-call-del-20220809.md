---
uniqueName: reginde-resoconto-call-del-20220809
displayName: "REGINDE   Resoconto call del 20220809"
category: "GENERAL"
tags: []
---

# REGINDE - Resoconto call del 20220809

> **File originale:** `MEV/SCHEDA_021/Docs/Riscontri DGSIA/2022_docs_errori/REGINDE - Resoconto call del 20220809.docx`  
> **Tipo:** DOCX

---

# SIUT-SIES-MG-1.4-20220525-Istruzioni_Bonifica_Difensori_021_RegInde_SIES.docx
Buongiorno,
nell’incontro odierno sono state chiarite al fornitore le osservazioni inviate sia per le vie brevi sia in via formale.
I punti trattati:

1)  stata ribadita la logica già esplicata nelle varie comunicazioni intercorse nel passato, secondo le seguenti linee di massima:
a) snellire la lettura del documento evitando rimandi avanti ed indietro all’interno dello stesso documento quando non necessario;
b) snellire le frasi;
c) separare le  spiegazioni dalle verifiche vere e proprie;
d) prevedere i controlli sui log per la corretta esecuzione formale degli script;
e) prevedere i controlli opportuni sui DATI pre e post elaborazione per verificare la bontà della logica di bonifica. Le verifiche pre e post bonifica vanno fatte utilizzando sui dati pre ed i dati post elaborazione opportunamente estratti, esplicitando i controlli da fare.
f) i documenti correlati tra loro devono essere coerenti, cioè se in un documento viene referenziato un altro documento occorre che sia citato il nome corretto.
g) controllare gli indici e le numerazioni delle pagine

2) è stato chiarito che la revisione secondo le linee sopra indicate deve riguardare tutti i documenti operativi consegnati per questa MEV, sia per il sistema SIES sia per il sistema SIUS-Avvocati

3) si è chiesto lumi sullo scopo del documento "SIUT-SIES-MG-1.0-20220525-Analisi Procedure Allineamento_021_RegInde_SIES"

Il fornitore ha detto che recepirà le indicazioni, modificando tutti i documenti necessari.
Il fornitore si è riservato di chiarire all'amministrazione lo scopo del documento di cui al punto 3)

Anna Maffucci


Pag. 10 punto 2)  spostare l’esempio dove sono le spiegazioni. In generale:
se c’è uno script che va a buon fine è inutile far fare una select * from xxx
Gli basta il LOG di Oracle che dice se è andata bene o male. Il LOG da garanzia di successo.
Fare la query per verificare le procedure di bonifica, non la creazione di tabelle ex novo.
Vogliono i controlli per verificare i passaggi logici della procedura di bonifica; ovvero solo i controlli sulla differenza tra il prima ed il dopo (verifica a campione).
Pag. 10  Eliminare tabella con inizio ore xxx e fine ore yyy
La select va fatta sulla tabella di partenza non su quella di arrivo (NON SERVE) !
Pag. 13)  accedendo alla tabella PRE_XBA_... OK!
Pag. 14)  Le tabelle trattate … CANCELLARE!
Pag. 16)  il risultato deve essere <> 0 … la query 1 e 3 danno risultati non coerenti, la tre deve essere >= alla 1
Pag. 18)  il punto 5) ci sono verifiche ridondanti; se qualcosa va male che bisogna fare? Perché altrimenti l’utente prosegue con l’installazione. Quindi fare uno screenshot del DB all’inizio e dire se qualcosa va male di fare il ripristino del backup.
In generale fare i controlli sui dati reali e non sulla creazione di tabelle!
PS: nel P.d.R. aggiornare e mettere versione SIES xxx (lasciare in sospeso).