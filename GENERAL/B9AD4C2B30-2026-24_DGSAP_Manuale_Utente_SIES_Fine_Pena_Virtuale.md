---
uniqueName: b9ad4c2b30-2026-24dgsapmanualeutentesiesfinepenavi
displayName: "B9AD4C2B30 2026 24 DGSAP Manuale Utente SIES Fine Pena Virtuale"
category: "GENERAL"
tags: []
---

# B9AD4C2B30-2026-24_DGSAP_Manuale_Utente_SIES_Fine_Pena_Virtuale

> **File originale:** `MEV/SCHEDA_2026-24/B9AD4C2B30-2026-24_DGSAP_Manuale_Utente_SIES_Fine_Pena_Virtuale.docx`  
> **Tipo:** DOCX

---



Ministero della Giustizia
Dipartimento per l’innovazione tecnologica della giustizia

MANUALE UTENTE
INTERVENTI EVOLUTIVI SULL’APPLICAZIONE SIES

| Prospetto Informativo Sintetico | Prospetto Informativo Sintetico |
| --- | --- |
| INTERVENTO | Interventi evolutivi sull’applicazione SIES |
| CONTRATTO DI RIFERIMENTO | Accordo Quadro per l’affidamento di servizi applicativi in ottica cloud e l’affidamento di servizi di demand e PMO per le pubbliche amministrazioni centrali ID 2483 – Seconda Edizione - Lotto 1 – Digitalizzazione Area Penale – CIG B9AD4C2B30 |
| CICLO DI VITA | Ridotto |
| DOCUMENTO | Manuale Utente: B9AD4C2B30-2026-24 |
| FILE | B9AD4C2B30-2026-24_DGSAP_Manuale_Utente_SIES_Fine_Pena_Virtuale |
| DATA DOCUMENTO | 30/01/2026 |
| FORNITORE | RTI - Accenture |


| Elenco versioni | Elenco versioni |
| --- | --- |
| v1 | Prima emissione |


| Referenti | Referenti |
| --- | --- |
| Nominativo | Organizzazione |
| Oris Orlando | DEC - DGSAP |
| Marta Nicoletti Altimari | RUP – DGSAP |
| Michele D’Alessandro | RUAC - RTI Accenture |




Indice


# Premessa
L’intervento in oggetto è stato richiesto a seguito di riunioni on line a cui hanno partecipato i gruppi di lavoro SIEP e SIUS dell’Amministrazione e personale del Fornitore per analizzare le richieste di MEV presentate dai referenti.
Nel documento sono descritti gli interventi urgenti realizzati in SIES, ambiti SIEP e SIUS, per il miglioramento del sistema.
# Interventi SIEP

## Visualizzazione Data Fine Pena Virtuale su Dettaglio Procedimento
La funziona Calcolo Pena DL 92/2024 è stata rivista per permettere di memorizzare nella base dati la Data Fine Pena Virtuale e visualizzarla sulla maschera Dettaglio Procedimento.
Poiché il fine pena virtuale calcolato dalla funzione deve diventare un dato memorizzato e visualizzato sul procedimento, si è ritenuto importante tenere traccia dei dati di input e dei dati prodotti dal calcolo, realizzando una funzione di validazione, e quindi di memorizzazione degli stessi, in modo da avere riscontro nel sistema di eventuali ricalcoli che possano aver modificato i risultati di un precedente calcolo.
Per avere visibilità di tutti i calcoli, validati, effettuati sul procedimento è stato inserito nella maschera iniziale, accanto ai preesistenti tasti Conferma e Pulisci Dati, un ulteriore tasto Storico Calcoli Validati, che presenterà l’elenco di tutti i calcoli eseguiti e validati.

A seguito della Conferma il sistema effettuerà gli attuali calcoli e presenterà la maschera con tutti i dettagli, in maniera uguale all’attuale, ma con i nuovi tasti Valida e Storico Calcoli Validati, accanto al preesistente Ricalcolo:


che memorizzerà nella data base tutti i dati oggetti del calcolo, in particolare la data fine pena virtuale. Le tabelle saranno popolate ad ogni nuovo calcolo, purché validato, e conterranno la storia dei calcoli fine pena virtuale validati.
Cliccando su Valida, il sistema invierà il messaggio:

per la conferma a procedere alla memorizzazione di tutti i dati coinvolti nel calcolo, in particolare la data fine pena virtuale, nella base dati. Dopo la conferma il seguente invia il seguente messaggio:

E si riposiziona sulla pagina di dettaglio del calcolo.
Cliccando su Storico Calcoli Validati, il sistema presenterà l’Elenco di tutti i calcoli già effettuati e validati per il procedimento corrente:

Cliccando sull’icona di Dettaglio presente accanto a una delle righe in Elenco, si riceverà la maschera di Calcolo Dettagliata, come ricevuta al momento del Calcolo, su cui non sarà presente alcun tasto operativo descritto in precedenza.
Cliccando sull’icona di Cancellazione si riceverà il messaggio per procedere alla cancellazione dello storico:

Cliccando su OK il sistema cancellerà i dati dallo storico.
In caso di Calcolo effettuato su procedimento con condannato Libero, validato, lo storico si presenterà come di seguito:

Se tra i dati storicizzati a seguito della funzione di Validazione è presente anche data fine pena virtuale, la form di Dettaglio procedimento riporterà il dato accanto alla data fine pena (reale):

In caso di presenza di più date fine pena virtuale storicizzate, sarà visualizzata quella inserita per ultima.
Dal Dettaglio procedimento, cliccando sul link Fine Pena Virtuale, sarà visualizzata la maschera dettagliata dei dati dello storico a cui fa riferimento.
## Scadenzario Fine pena
E’ stata modificata l’attuale funzione Scadenzario Fine Pena, aggiungendo sulla pagina di Visualizzazione la data Fine Pena Virtuale, se presente sul procedimento:

Poiché la suddetta data non è presente sulla tabella “Scadenzario_SIEP”, su cui lavora la funzione, i criteri di estrazione sono rimasti invariati, cioè continuano a lavorare solo sulla data fine pena presente nello scadenzario.
# Interventi SIUS
## Ricerca Fine Pena Procedimenti Pendenti
La nuova funzionalità permette di ricercare i procedimenti SIUS ancora pendenti (tutti, per anno, scaduti o in scadenza) e collegati a procedimenti SIEP, visualizzerà la data inizio pena, la data fine pena e, se presente, la data fine pena virtuale, rilevandole dai dati presenti sul procedimento SIEP a cui è collegato.
La nuova funzione è stata inserita nel menu Scadenzari:

Selezionandola il sistema invia la seguente form:

in cui è obbligatorio valorizzare:
una delle due tipologie di estrazione dei procedimenti SIUS (Intervallo estremi procedimenti oppure Intervallo Date Iscrizione);
uno dei quattro criteri di ricerca (Tutti, in scadenza, in scadenza oggi, scaduti);
la data di fine pena reale o virtuale su cui deve essere applicato il criterio di ricerca.
Dopo aver impostato i filtri di ricerca e confermato, il sistema estrarrà tutti i procedimenti SIUS pendenti e collegati a procedimenti SIEP, recuperando gli estremi dei due procedimenti, le date inizio pena, fine pena e fine pena virtuale e visualizzerà la form:

L’elenco sarà ordinato per data fine pena reale decrescente o data fine pena virtuale decrescente, in base alla scelta fatta sulla maschera di impostazione dei criteri di estrazione.
Per ciascun elemento dell’Elenco è possibile accedere al Dettaglio Procedimento SIUS e al Dettaglio Procedimento SIEP, cliccando sui rispettivi Anno/Numero.
Se è stata impostata l’estrazione su data fine pena virtuale, il sistema estrarrà solo i procedimenti collegati a procedimenti SIEP con data fine pena virtuale valorizzata.
Dall’elenco è possibile generare il foglio Excel riportante tutti i dati estratti.
## Condivisione Calcolatrice DL 92/2024 di SIEP
A seguito degli interventi realizzati sulla Calcolatrice lato SIEP, descritti al par. 2.1, fermo restando la possibilità da parte della Sorveglianza di poter utilizzare la calcolatrice per verificare la correttezza dei dati pervenuti da SIEP, la maschera finale che riporta tutti i dettagli del calcolo/ricalcolo non presenta il tasto Valida, in quanto il calcolo e la validazione del fine pena virtuale è, al momento, di competenza degli uffici esecuzione.