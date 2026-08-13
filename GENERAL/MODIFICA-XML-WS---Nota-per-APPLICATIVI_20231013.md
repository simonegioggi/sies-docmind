---
uniqueName: modifica-xml-ws-nota-per-applicativi20231013
displayName: "MODIFICA XML WS   Nota per APPLICATIVI 20231013"
category: "GENERAL"
tags: []
---

# MODIFICA XML WS - Nota per APPLICATIVI_20231013

> **File originale:** `MEV/SCHEDA_033/MODIFICA XML WS - Nota per APPLICATIVI_20231013.pdf`  
> **Tipo:** PDF

---

Nota per applicativi Giustizia – 13/10/2023 
Si comunicano le novità che saranno introdotte con l’attività di aggiornamento del PST del 13/10/2023. 
1) Verranno modificati i metodi generaRPT e generaAvviso revisionando l’elemento in input 
richiestaPagamentoTelematico in modo da aggiornare i controlli sulla valorizzazione degli elementi al 
suo interno in base alle specifiche pagoPA. Verranno apportate le seguenti modifiche: 
 
• 
Verrà eliminato l’elemento soggettoVersante 
• 
Verranno eliminati gli elementi ibanAddebito e bicAddebito 
ATTENZIONE: al momento sarà garantita le retrocompatibilità per gli elementi soggettoVersante, 
ibanAddebito e bicAddebito pertanto l’attuale struttura richiestaPagamentoTelematico.xml sarà 
comunque accettata dal PST. 
 
• 
Verranno adeguati i controlli relativi agli elementi “importo” e “importoTotale” in modo che seguano le 
regole degli elementi corrispondenti di pagoPa, ovvero: 
 
<xsd:simpleType name="stAmountNotZero"> 
<xsd:restriction base="xsd:decimal"> 
<xsd:pattern value="\d+\.\d{2}" /> 
<xsd:minInclusive value="0.01" /> 
<xsd:maxInclusive value="999999999.99" /> 
</xsd:restriction> 
</xsd:simpleType> 
 
• Verranno adeguati i controlli degli elementi presenti in “soggettoPagatore” in modo che rispettino le 
codifiche degli elementi corrispondenti di pagoPa, ovvero: 
o codiceIdentificativoUnivoco sarà obbligatorio ma potrà essere non valorizzato: 
<codiceIdentificativoUnivoco><codiceIdentificativoUnivoco> 
o nominativo dovrà essere una stringa con 70 caratteri di lunghezza massima 
o indirizzo dovrà essere una stringa con 70 caratteri di lunghezza massima 
o civico dovrà essere una stringa con 16 caratteri di lunghezza massima 
o cap dovrà essere una stringa con 16 caratteri di lunghezza massima 
o localita dovrà essere una stringa con 35 caratteri di lunghezza massima 
o provincia dovrà essere una stringa con 35 caratteri di lunghezza massima 
o provincia e nazione dovranno rispettare la seguente codifica: 
<xsd:restriction base="xsd:string"> 
<xsd:pattern value="[A-Z]{2,2}" /> 
</xsd:restriction> 
o email dovrà rispettare la seguente codifica: 
<xsd:restriction base="xsd:string"> 
<xsd:pattern value="[a-zA-Z0-9_\.\+\-]+@[a-zA-Z0-9\-]+(\.[a-zA-Z0-9\-]+)*" /> 
<xsd:maxLength value="256" /> 
</xsd:restriction> 
 
• 
all’interno dell’oggetto richiestaPagamentoTelematico verrà mantenuta l'obbligatorietà del campo 
codiceIdentificativoUnivoco del soggettoPagatore, dando però la possibilità di non 
valorizzarlo, se non è noto, oppure di usare la stringa ANONIMO. In entrambi i casi, sull’avviso di 
pagamento in PDF la sezione relativa al CF resterà vuota.

Nota per applicativi Giustizia – 13/10/2023 
2) Verrà modificata la gestione della data scadenza:  se non valorizzata all’interno della struttura 
richiestaPagamentoTelematica nessuna data di scadenza sarà visualizzata sul PDF dell’avviso di 
pagamento.