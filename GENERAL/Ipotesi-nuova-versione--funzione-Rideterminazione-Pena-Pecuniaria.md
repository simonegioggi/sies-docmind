---
uniqueName: ipotesi-nuova-versione-funzione-rideterminazione-p
displayName: "Ipotesi nuova versione  funzione Rideterminazione Pena Pecuniaria"
category: "GENERAL"
tags: []
---

# Ipotesi nuova versione  funzione Rideterminazione Pena Pecuniaria

> **File originale:** `MEV/SCHEDA_033/Ipotesi nuova versione  funzione Rideterminazione Pena Pecuniaria.docx`  
> **Tipo:** DOCX

---

Ipotesi nuova versione  funzione Rideterminazione Pena Pecuniaria
La funzione di Rideterminazione Pena Pecuniaria realizzata, conformemente a quanto indicato nella Scheda Intervento della MEV-33 Step 1, approvato, è finalizzata a permettere all’ufficio di poter emettere un nuovo provvedimento a fronte di un nuovo importo della pena pecuniaria sostitutiva, a prescindere dalle motivazioni e criteri applicati per determinarlo, permettendo all’ufficio di generare nuovi bollettini e di gestirli.
Nel corso dell’ultima call con il GdL Siep è stato richiesto di valutare invece la realizzazione di una funzione di Rideterminazione della pena pecuniaria sostitutiva che sia in grado di calcolare automaticamente il nuovo importo da pagare a seguito della riduzione della pena detentiva e della pena pecuniaria (multa/arresto).
Si è quindi ipotizzato come possibile form la seguente:

Nell’esempio, siamo in presenza di un procedimento con la seguente pena complessiva:

In cui il giudice ha convertito la pena detentiva 2 mesi e 15 giorni in 12000€ di pena pecuniaria sostitutiva, per cui tenendo conto di 2500€ di multa l’importo da pagare per estinguere l’intera pena pecuniaria è di 14500€.
A seguito di provvedimento di ufficio o di altra autorità (GE/Sorveglianza) si provvede a ridurre la pena detentiva, valorizzando i relativi campi della form (es. 1 mese e 15 giorni e 1500 di multa)

Il sistema va a calcolare sulla form la pena sostitutiva da detrarre, la residua e l’importo da pagare:

In cui i tre importi sono stati calcolati nel modo seguente:
Pena pecuniaria sostitutiva da detrarre = (Pena pecuniaria sostitutiva / numero giorni totali di pena detentiva) x numero giorni totali da detrarre
Pena pecuniaria sostitutiva (residua) = Pena pecuniaria sostitutiva - Pena pecuniaria sostitutiva da detrarre
Importo da pagare = Pena pecuniaria sostitutiva residua + multa residua + ammenda residua
in cui per numero giorni totali di pena detentiva = n.ro anni x 365 + n.ro mesi x30 + n.ro giorni
numero giorni totali da detrarre = n.ro anni x 365 + n.ro mesi x30 + n.ro giorni  ( riferiti ai quantum da sottrarre)
Nell’es. numero giorni totali di pena detentiva = (2 x 30) + 15 = 75
numero giorni totali da detrarre = (1 x 30) + 15 = 45
Pena pecuniaria sostitutiva da detrarre = (12000 / 75) x 45 = 7200
Pena pecuniaria sostitutiva residua = 12000 – 7200 =  4800
Importo da pagare = 4800 + 1000 (multa)
L’utente compila la restante parte della form relativa a modalità di pagamento e magistrato Firmatario:

e conferma, il sistema aggiorna la base dati e presenta la form di Dettaglio, da cui sarà possibile stampare, modificare e validare. A seguito della validazione il sistema potrebbe effettuare il calcolo pena sulla parte detentiva, come avviene adesso, e in più calcolare la pena sostitutiva residua.
Per avere traccia del provvedimento con cui si è ridotta la pena detentiva nel stampa del provvedimento si deve menzionare anche la pena detentiva detratta.
Da tener presente che il provvedimento di rideterminazione pena parte sempre dall’ultima pena residua, per cui nel caso si operasse con i vari provvedimenti presenti in SIEP su questa pena, senza avere la possibilità di aggiornare anche la pena sostitutiva residua, i calcoli effettuati all’interno della funzione di rideterminazione non sarebbero corretti.
ES. se l’utente va a inserire una Rideterminazione pena Altro, che non tiene conto della pena sostitutiva come non teneva conto della sanzione sostitutiva, detraendo dalla pena le stesse quantità dell’esempio su riportato, selezionando la funzione Rideterminazione pena pecuniaria si partirebbe da

Per cui i suddetti calcoli relativi alla pena sostitutiva residua non sarebbero corretti e non ci sarebbe modo l’importo delle Pena pecuniaria sostitutiva, a meno di non consentire di utilizzare la form senza valorizzare i quantum di pena detentiva da detrarre e impostare a mano i campi pena sostitutiva residua e importo da pagare.
#######################################################################################