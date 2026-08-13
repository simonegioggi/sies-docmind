---
uniqueName: siepinterventoparte2xxxversione0012014120512-30-p1
displayName: "Siep intervento parte 2 xxx versione 0 0 1 2014 12 05 12 30   p18   desc"
category: "GENERAL"
tags: []
---

# Siep_intervento_parte_2_xxx_versione_0_0_1_2014_12_05_12.30 - p18 - desc

> **File originale:** `MEV/Mev10/Siep_intervento_parte_2_xxx_versione_0_0_1_2014_12_05_12.30 - p18 - desc.docx`  
> **Tipo:** DOCX

---


18.1	Descrizione dell’intervento	2
A) Ufficio Emittente / Autorità Emittente [EMITTENTE]	4
B) UEPE / USSM [CSSA]	6
C) Magistrato di Sorveglianza / Ufficio di Sorveglianza [MAGISTRATO]	8
D) Tribunale di Sorveglianza [TRIBUNALE]	10
E) AUTORITA’ COMPETENTE PER TERRITORIO	11
F) AUTORITA’ DESTINAZIONE	12
G) DESTINATARIO PER ESECUZIONE	13
I) AUTORITA’ PER ESECUZIONE	14
SELEZIONE DEL MAGISTRATO	15
ETICHETTE DETTAGLIO	16



## Descrizione dell’intervento
L’intervento prevede l’adeguamento di tutte le maschere delle decisioni della magistratura di sorveglianza con le caratteristiche peculiari dell’ambito minorile.
L’operatore all’interno del procedimento seleziona dal menu laterale di sinistra la voce “Decisione Sorveglianza) (Figura 1).


Figura  -  Selezione Decisioni Sorveglianza


Il sistema mostra l’interfaccia con le decisioni della sorveglianza (Figura 2).

Figura  - Decisioni Sorveglianza

Le modifiche sono previste per i procedimenti iscritti:
dalla Procura presso il Tribunale per i minorenni (cod_tipo_ufficio = “PMM”)
e dalla Procura generale (cod_tipo_ufficio = “PGCAP”)
presso  di Appello sezione per i minorenni (cod_tipo_ufficio = “CAPSM”)
e devono tener conto del fatto che uffici che svolgono funzioni giurisdizionali simili hanno diverso nome in relazione all’ambito di appartenenza.
Ad esempio, il Tribunale di Sorveglianza per l’ambito degli uffici giudiziari dei minorenni assume il nome “Tribunale per i  Minorenni in Funzione di Tribunale di Sorveglianza”.
Inoltre, sullo stesso procedimento posso essere presenti uffici di entrambi gli ambiti (maggiorenni/minorenni).
Pertanto, è stato richiesto che nella stessa maschera sia possibile avere, in alcuni casi, al posto di una sola etichetta un elenco contenente 2 diverse etichette.

A) Ufficio Emittente / Autorità Emittente [EMITTENTE]

Attualmente, l’ufficio emittente, talvolta, è prevalorizzato e non modificabile dall’operatore:

Figura  – Attuale ufficio emittente prevalorizzato
In qualche caso, l’etichetta è “Autorità Emittente”.

Figura  - Autorità Emittente

In altri casi, è prevalorizzato, ma il sistema permette la selezione da un elenco dell’ufficio emittente:

Figura  – Attuale ufficio emittente modificabile
Anche in questo caso, l’etichetta può essere “Autorità Emittente”.

Figura  - Autorità Emittente

L’intervento prevede nel primo caso della immagine (Figura 3 – Attuale ufficio emittente prevalorizzato) e nel secondo caso della immagine (Figura 5 – Attuale ufficio emittente modificabile) l’inserimento di una casella di selezione (combobox) (

Figura 7) contenente il seguente elenco:
Tribunale di Sorveglianza
Magistrato di Sorveglianza
Tribunale per i  Minorenni in Funzione di Tribunale di Sorveglianza
Magistrato di sorveglianza per i Minorenni.

La relativa funzione di ricerca della sede deve tener conto della selezione effettuata dall’operatore.
Nel caso:
il sistema mostra l’elenco dei Tribunali di Sorveglianza (cod_tipo_ufficio=”TDS”),
il sistema mostra l’elenco dei Magistrati di Sorveglianza (cod_tipo_ufficio=”UDS”),
il sistema mostra l’elenco dei Tribunali per i Minorenni in Funzione di Tribunale di Sorveglianza (cod_tipo_ufficio=”TDSM”),
il sistema mostra l’elenco dei Magistrati di sorveglianza per i Minorenni (cod_tipo_ufficio=”UDSM”).

I 4 casi descritti nelle immagini (Figura 3,Figura 4,Figura 5 e Figura 6) dopo l’intervento sono ridotti a soli 2 (

Figura 7 e Figura 8)


Figura 7 – Ufficio emittente modificabile


Figura  – Autorità emittente modificabile
L’intervento in parola riguarda tutti i procedimenti.

B) UEPE / USSM [CSSA]

L’etichetta “UEPE” deve essere modificata in una casella di selezione contenente i seguenti 2 valori:
UEPE (valore di default)
USSM.
La relativa funzione di ricerca deve tener conto della selezione effettuata dall’operatore.
Nel caso:
il sistema mostra l’elenco degli UEPE (cod_tipo_ufficio=”UEPE” oppure ”UEPESS”),
il sistema mostra l’elenco degli USSM  (cod_tipo_ufficio=”USSM” oppure ”USSMSS”).


Figura  - Attuale UEPE


Figura  - USSM per i minorenni

Quando l’etichetta “UEPE” è seguita dall’indicazione dell’ufficio in sola lettura presente in archivio (Figura 11), l’etichetta deve essere visualizzata a seconda del codice tipo ufficio (vedi maschera “Variazione Data Inizio Misura”).


Figura  – attuale etichetta UEPE

Figura  - Ricerca UEPE

C) Magistrato di Sorveglianza / Ufficio di Sorveglianza [MAGISTRATO]

L’etichetta “Ufficio di Sorveglianza” deve essere modificata in una casella di selezione contenente i seguenti 2 valori:
Ufficio di Sorveglianza (valore di default)
Magistrato di Sorveglianza per i Minorenni.


Figura  - Attuale Ufficio di Sorveglianza

In alcuni casi l’etichetta è “Magistrato di Sorveglianza”.
In questi casi, l’etichetta “Magistrato di Sorveglianza” deve essere modificata in una casella di selezione contenente i seguenti 2 valori:
Magistrato di Sorveglianza (valore di default)
Magistrato di Sorveglianza per i Minorenni.


Figura  - Attuale Ufficio di Sorveglianza


Figura  - Magistrato di Sorveglianza per i minorenni

La relativa funzione di ricerca deve tener conto della selezione effettuata dall’operatore.
Nel caso:
il sistema mostra l’elenco degli uffici di sorveglianza (cod_tipo_ufficio=”UDS”),
il sistema mostra l’elenco dei magistrati di sorveglianza per i minorenni (cod_tipo_ufficio=”UDSM”).

Nella finestra (Figura 16) nel primo caso l’etichetta è “Lista Uffici Di Sorveglianza”, nel secondo caso “Lista Magistrati Di Sorveglianza per i Minorenni”.


Figura  -  Funzione selezione ufficio di sorveglianza

D) Tribunale di Sorveglianza [TRIBUNALE]

L’etichetta “Tribunale di Sorveglianza” deve essere modificata in una casella di selezione contenente i seguenti 2 valori:
Tribunale di Sorveglianza (valore di default)
Tribunale per i  Minorenni in funzione di Tribunale di Sorveglianza.


Figura  - Attuale Tribunale di sorveglianza


Figura  -  Tribunale per i  Minorenni in funzione di Tribunale di Sorveglianza

La relativa funzione di ricerca deve tener conto della selezione effettuata dall’operatore.
Nel caso:
il sistema mostra l’elenco dei Tribunali di sorveglianza (cod_tipo_ufficio=”TDS”),
il sistema mostra l’elenco Tribunale per i  Minorenni in funzione di Tribunale di Sorveglianza (cod_tipo_ufficio=”TDSM”).

Nella finestra (Figura 19) nel primo caso l’etichetta è “Elenco Tribunali Di Sorveglianza”, nel secondo caso “Elenco Tribunali per i Minorenni in funzione di Tribunale Di Sorveglianza”.


Figura  -  Funzione selezione Tribunale di sorveglianza

E) AUTORITA’ COMPETENTE PER TERRITORIO

Negli elenchi delle autorità di destinazione devono essere presenti anche la tipologia dell’Ufficio Servizi Sociali Minorenni (cod_tipo_ufficio = “USSM”) e la voce “SNT”.


Figura  - Autorità competente per territorio

F) AUTORITA’ DESTINAZIONE

Negli elenchi delle autorità di destinazione devono essere presenti anche la tipologia dell’Ufficio Servizi Sociali Minorenni (cod_tipo_ufficio = “USSM”) e la voce “SNT”.


Figura  - Autorità destinazione

G) DESTINATARIO PER ESECUZIONE

Negli elenchi del destinatario per l’esecuzione devono essere presenti anche la tipologia dell’Ufficio Servizi Sociali Minorenni (cod_tipo_ufficio = “USSM”) e la voce “SNT”.


Figura  - Destinatario per esecuzione


Figura  - Destinatario per esecuzione

I) AUTORITA’ PER ESECUZIONE

Negli elenchi della Autorità per la restituzione devono essere presenti anche la tipologia dell’Ufficio Servizi Sociali Minorenni (cod_tipo_ufficio = “USSM”) e la voce “SNT”.


Figura  - Autorità per la Restituzione

SELEZIONE DEL MAGISTRATO

La selezione per magistrato deve tener correttamente conto dell’ufficio di appartenenza.
Pertanto, l’operatore della Procura presso il Tribunale per i minorenni può selezionare un magistrato associato all’ufficio della Procura presso il Tribunale per i minorenni.


Figura  -  Magistrato firmatario

ETICHETTE DETTAGLIO

Inoltre, sono da modificare le etichette delle maschere di dettaglio richiamate dopo la conferma delle informazioni inserite nelle maschere di inserimento.