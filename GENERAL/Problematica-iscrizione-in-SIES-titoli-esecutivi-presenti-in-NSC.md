---
uniqueName: problematica-iscrizione-in-sies-titoli-esecutivi-p
displayName: "Problematica iscrizione in SIES titoli esecutivi presenti in NSC"
category: "GENERAL"
tags: []
---

# Problematica iscrizione in SIES titoli esecutivi presenti in NSC

> **File originale:** `MEV/SCHEDA_021/Docs/Problematica iscrizione in SIES titoli esecutivi presenti in NSC.docx`  
> **Tipo:** DOCX

---

# Problematica iscrizione in SIES titoli esecutivi presenti in NSC
Con l’allineamento della tabella COMUNE di SIES alla tabella fissa DGSIA, vari comuni che nel tempo hanno subito variazione della Provincia di appartenenza, sono presenti più volte in tabella con codici_istat differenti, presentando di fatti la storia dei suddetti comuni. I comuni non più attivi sono caratterizzati dall’avere la colonna DATA_FINE_VALIDITA_COMUNE valorizzata.
Es. il comune di ARBUS è presente con tre occorrenze
| Cod_Comune | Provincia | Descrizione | Flag_validita | Cod_catastale | Data fine validità |
| --- | --- | --- | --- | --- | --- |
| 92001 | CA | ARBUS | N | A359 | 2006/1/1 |
| 106001 | VS | ARBUS | N | A359 | 2017/1/1 |
| 111001 | SU | ARBUS | S | A359 |  |

in quanto fino al 31/12/2005 apparteneva alla provincia di Cagliari (092001), dall’1/1/2006 fino al 31/12/2016 apparteneva alla provincia di Medio Campidano (106001), dall’1/1/2017 fa parte della provincia Sud Sardegna (111001).
Con questa struttura di dati si riesce a gestire il luogo di nascita di un soggetto, tenendo conto della storia del Comune, per cui i nati prima dell’ 1/1/2006 sono nati in ARBUS(CA), mentre se risiedono ancora ad ARBUS faranno riferimento ad ARBUS(VS).
In NSC invece il Comune non è storicizzato e non sempre è aggiornato per quel che riguarda il codice ISTAT di riferimento, ad es. il comune di ARBUS fa riferimento ad un codice univoco 01700599 riferito al codice ISTAT 106001.
Nella tabella di transcodifica SIES-NSC CODICI_SIES_NSC il comune in esempio era presente con il seguente record
| CO_DOMAIN | CO_CODCENTR | CO_NSC | CO_NSC_DES | CO_SIES | CO_SIES_DES | CO_VAL1 | CO_VAL2 | CO_VAL3 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| COMUNE | 106001 | 1700599 | ARBUS | 92001 | ARBUS |  |  |  |


per cui il sistema riconoscerebbe nella trasmissione da SIES a NSC come luogo nascita corretto 092001, mentre gli altri non sarebbe riconosciuti validi.
Si è pertanto proceduto all’allineamento della tabella di transcodifica alla luce della tabella COMUNE, successivamente all’allineamento, generando anche in questa tabella più occorrenze per lo stesso comune. Per cui Arbus presenta le seguenti occorrenze
| CO_DOMAIN | CO_CODCENTR | CO_NSC | CO_NSC_DES | CO_SIES | CO_SIES_DES | CO_VAL1 | CO_VAL2 | CO_VAL3 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| COMUNE | 106001 | 1700599 | ARBUS | 92001 | ARBUS |  |  | 2006-01-01 |
| COMUNE | 106001 | 1700599 | ARBUS | 106001 | ARBUS |  |  | 2017-01-01 |
| COMUNE | 106001 | 1700599 | ARBUS | 111001 | ARBUS |  |  |  |


In questo modo i soggetti presenti in SIES, nati in uno dei 3 comuni, sarà correttamente trasferito in NSC dove acquisirà l’unico codice (CO_NSC) riconosciuto in quel sistema.
Viceversa il trasferimento di un’ANAGRAFICA, presente in NSC, nata ad ARBUS al momento viene eseguito senza rilevare errore, ma viene attribuito quale comune di nascita 092001.
Avendo valorizzato in CODICI_SIES_NSC la colonna CO_VAL3 con la data fine validità del comune, bisognerebbe modificare l’attuale codice tenendo conto anche della data nascita del soggetto per la corretta assegnazione del Cod_Comune.
Al momento nel trasferimento dell’Anagrafica NSC a SIES il sistema per individuare il cod_comune da assegnare in SIES esegue la seguente query
SELECT CO_DOMAIN, CO_CODCENTR, CO_NSC, CO_NSC_DES, CO_SIES, CO_SIES_DES, CO_VAL1, CO_VAL2, CO_VAL3  FROM CODICI_SIES_NSC WHERE  CO_CODCENTR = '106001' and CO_DOMAIN = 'COMUNE'
bisognerebbe far precedere la suddetta query dalla seguente
SELECT count (*) FROM CODICI_SIES_NSC WHERE  CO_CODCENTR = '106001' and CO_DOMAIN = 'COMUNE'
se la count è = 1, si procede come è al momento
se la count è > 1, caricare in un vettore il cod_comune e il co_val3 di ciascun record, ordinati per co_val3 crescente
verificare se la data di nascita del soggetto è inferiore a co_val3 del primo record, in caso affermativo selezionare il cod_comune corrispondente e uscire dal ciclo, diversamente verificare se la data di nascita del soggetto è inferiore a co_val3 del secondo record, in caso affermativo selezionare il cod_comune corrispondente e uscire dal ciclo, diversamente continuare il test con il successivo. Se il co_val3 dell’ultimo record non è valorizzato e la data ha superato i precedenti test, selezionare quest’ultimo record.