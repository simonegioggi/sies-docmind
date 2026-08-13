---
uniqueName: omocodia
displayName: "Omocodia"
category: "GENERAL"
tags: []
---

# Omocodia

> **File originale:** `MEV/SCHEDA_021/Docs/Omocodia.docx`  
> **Tipo:** DOCX

---

# Omocodia
In caso di omocodia la procedura dell'AE consiste nel sostituire uno o più dei sette numeri del codice, a partire da quello più a destra, con delle lettere corrispondenti. Per l’esattezza:
0 = L | 1 = M | 2 = N | 3 = P | 4 = Q
5 = R | 6 = S | 7 = T | 8 = U | 9 = V

Nella procedura plsql che ho fatto per risalire per gli avvocati, contenuti nella tabella ReGIndE fornita dall'Amministrazione, dal codice catastale al codice del comune nascita, mi sono limitato a testare solo gli ultimi 3 numeri a partire da destra e ho recuperato tutti i casi di omocodia. Ti riporto la parte che ho inserito nella procedura, l'ho fatta in maniera molto spartana:
-- sostituire gli ultimi 3 caratteri del codice catastale con
-- 0 = L | 1 = M | 2 = N | 3 = P | 4 = Q | 5 = R | 6 = S | 7 = T | 8 = U | 9 = V
Per la natura stessa del codice fiscale sono sempre possibili, anche se piuttosto rare, le cosiddette omocodie, ovvero quei casi in cui il codice fiscale di due persone diverse, calcolato con l'algoritmo standard, risulta identico.
E' il caso di due o più persone, con nomi identici o simili, nate lo stesso giorno nello stesso Comune, cosa che si verifica più frequentemente in presenza di cognomi diffusi (Rossi, Bianchi ecc.) soprattutto nei Comuni densamente popolati.
Le omocodie non sono molte rispetto al numero totale di codici fiscali generati e si stima che si verifichino circa 1400 nuovi casi all'anno.
In caso di omocodia la legge prevede che il codice fiscale originario sia modificato sostituendo uno o più caratteri numerici con altrettanti caratteri alfabetici.
I caratteri numerici che è possibile sostituire sono i seguenti:
- i 2 caratteri del giorno di nascita,
- i 2 caratteri dell'anno di nascita,
- i 3 caratteri del codice del comune di nascita.
La sostituzione avviene sempre a partire dalla cifra di destra in base alla seguente tabella:
0 = L | 1 = M | 2 = N | 3 = P | 4 = Q | 5 = R | 6 = S | 7 = T | 8 = U | 9 = V
Pertanto, se nel codice fiscale sono presenti delle lettere dove ci aspettiamo dei numeri allora si tratta di uno dei rari casi di codice fiscale modificato per omocodia; in questo caso, prima di calcolare il codice fiscale inverso, sostituire automaticamente le lettere con i corrispondenti numeri della tabella.

# Altre Informazioni
Ho aggiornato su siessvil la tabella COMUNE in cui sono stata aggiunte le seguenti colonne COD_CATASTALE_COMUNE, DATA_AGGIORNAMENTO_COMUNE, DATA_FINE_VALIDITA_COMUNE
​
Ho aggiornato nella CG_REF_CODES il dominio NAZIONE, in cui RV_LOW_VALUE contiene il codice dello stato, RV_HIGH_VALUE il cod_stato_iso, RV_ABBREVIATION il cod_stato_istat, RV_MEANING la descrizione, RV_ALT2_VALUE il codice catastale, RV_ALT3_VALUE la data_fine_validità.
RV_ALT4_VALUE l'ho utilizzata per distinguere i records aggiornati e quelli inseriti, penso di ripulirla al momento del rilascio.
​
Ho aggiornato nella CG_REF_CODES il dominio PROVINCIA, in cui RV_LOW_VALUE contiene il codice della provincia, RV_HIGH_VALUE il cod_regione (sostituisce il precedente cod_comune del capoluogo di Regione), RV_ABBREVIATION il fine_validita, RV_MEANING la descrizione.
RV_ALT2_VALUE l'ho utilizzata per distinguere i records aggiornati e quelli inseriti, penso di ripulirla al momento del rilascio.


# Avvocato Straniero
Penso che nella form di assegnazione/sostituzione/dettaglio dell'avvocato dovremo prevedere anche una combo Stato Estero e gestirla come per il Soggetto.
Ho dato uno sguardo alla form Inserimento Avvocato, ti ricordo che su ReGIndE sono presenti diversi avvocati nati all'estero (codice catastale con iniziale a Z, es. Z404 = Stati Uniti d'America), a tal fine nel dominio Nazione, per quasi tutti i records presenti è stata valorizzata la colonna RV_ALT2_VALUE con i relativi codici catastali.
La form deve contenere 2 nuovi campi Stato Nascita e Luogo Nascita Estero.
Come test puoi ricercare l'avvocato BELLA FRANCESCO del foro di TORINO.

ALTER TABLE AVVOCATO:
COD_STATO_NASCITA_AVV
DESC_LUOGO_NAS_REGINDE