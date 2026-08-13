---
uniqueName: b9ad4c2b30-2026-24dgsapschedainterventosiesfinepen
displayName: "B9AD4C2B30 2026 24 DGSAP Scheda Intervento SIES Fine Pena Virtuale"
category: "GENERAL"
tags: []
---

# B9AD4C2B30-2026-24_DGSAP_Scheda_Intervento_SIES_Fine_Pena_Virtuale

> **File originale:** `MEV/SCHEDA_2026-24/B9AD4C2B30-2026-24_DGSAP_Scheda_Intervento_SIES_Fine_Pena_Virtuale.docx`  
> **Tipo:** DOCX

---



Ministero della Giustizia
Dipartimento per l’innovazione tecnologica della giustizia

SCHEDA INTERVENTO
INTERVENTI EVOLUTIVI SULL’APPLICAZIONE SIES

| Prospetto Informativo Sintetico | Prospetto Informativo Sintetico |
| --- | --- |
| INTERVENTO | Interventi evolutivi sull’applicazione SIES |
| CONTRATTO DI RIFERIMENTO | Accordo Quadro per l’affidamento di servizi applicativi in ottica cloud e l’affidamento di servizi di demand e PMO per le pubbliche amministrazioni centrali ID 2483 – Seconda Edizione - Lotto 1 – Digitalizzazione Area Penale – CIG B9AD4C2B30 |
| CICLO DI VITA | Ridotto |
| DOCUMENTO | Scheda Intervento: B9AD4C2B30-2026-24 |
| FILE | B9AD4C2B30-2026-24_DGSAP_Scheda_Intervento_SIES_Fine_Pena_Virtuale |
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
Nel documento sono descritti gli interventi urgenti da realizzare in SIES, ambiti SIEP e SIUS, per il miglioramento del sistema.
# Interventi SIEP
Di seguito sono riportate alcune richieste/segnalazioni del GdL SIEP su cui si interverrà per la soluzione.

## Visualizzazione Data Fine Pena Virtuale su Dettaglio Procedimento
Requisito utente: Al momento la Data Fine Pena Virtuale è visibile solo all’interno della funzione Calcolatrice Nordio e non è conseguente ad alcun provvedimento SIEP. Occorre annotare sul procedimento SIEP la suddetta data, riportandola nel Dettaglio Procedimento.
Intervento: Poiché il fine pena virtuale calcolato dalla Calcolatrice Nordio deve diventare un dato memorizzato e visualizzato sul procedimento, si ritiene che sia importante tenere traccia dei dati di input e dei dati prodotti dal calcolo, realizzando una funzione di validazione dello stesso, in modo da tenere traccia sul sistema di eventuali ricalcoli che possano aver modificato i risultati del calcolo.
Si modificherà la funzione Calcolatrice Nordio, inserendo nella form di visualizzazione del calcolo, accanto all’attuale testo ‘Ricalcolo’, un nuovo tasto ‘Validazione”, che renderà la data fine pena virtuale valida a livello del procedimento e memorizzerà su apposite nuove tabelle di data base tutti i dati oggetti del calcolo. Le tabelle saranno popolate ad ogni nuovo calcolo, purché validato, e conterranno la storia dei calcoli fine pena virtuale validati.
Per avere visibilità di tutti i calcoli, validati, effettuati sul procedimento sarà inserito un ulteriore tasto, accanto ai tasti di cui sopra “Storico calcoli”, che presenterà l’elenco di tutti i calcoli fatti e per ciascuno presenterà tutti i dati di dettaglio.
Sarà modificata la funzione Dettaglio procedimento per visualizzare la data fine pena virtuale accanto alla data fine pena.

Di seguito sono descritte puntualmente le funzionalità su cui si interverrà:


Cliccando su Valida, il sistema invierà il messaggio per la conferma a procedere alla memrizzazione di tutti i dati coinvolti nel calcolo su nuove tabelle e a memorizzare a livello di procedimento la data fine pena virtuale.
Cliccando su Storico Calcoli Validati il sistema presenterà l’Elenco di tutti i calcoli già effettuati e validati per il procedimento corrente:
Cliccando su una delle righe in Elenco, si riceverà la maschera di Calcolo Dettagliata, come ricevuta al momento del Calcolo, su cui non saranno riportati i tasti di Ricalcolo, Validazione e Storico Calcoli Validati.
A seguito della memorizzazione sul procedimento della data fine pena virtuale, la form di Dettaglio procedimento riporterà il dato accanto alla data fine pena (reale):

## Scadenzario Fine pena
Requisito utente: Aggiungere sull’attuale Scadenzario Fine Pena una nuova colonna con Data Fine Pena Virtuale.
Intervento: Sarà modificato l’attuale funzione Scadenzario Fine Pena, aggiungendo sulla pagina di Visualizzazione la data Fine Pena Virtuale, presente sul procedimento :

Poiché la suddetta data non è presente sulla tabella “Scadenzario_SIEP”, su cui lavora la funzione, i criteri di estrazione rimarranno invariati, cioè continueranno a lavorare sulla data fine pena presente nello scadenzario.

# Interventi SIUS
Di seguito sono riportate alcune richieste/segnalazioni del GdL SIUS su cui si interverrà per la soluzione.
## Scadenzario monitoraggio Fine pena.
Requisito utente: Occorre implementare la funzione “scadenziari” inserendone uno che punti al fine pena, in modo da avere in evidenza le scadenze pena dei condannati. Il fine pena andrebbe rilevato dal dato presente sul procedimento SIEP collegato al fascicolo SIUS.
Intervento: Sarà realizzata una nuova funzionalità che permetterà di ricercare i procedimenti SIUS ancora pendenti (tutti, per anno, scaduti o in scadenza) e collegati a procedimenti SIEP, che visualizzerà la data inizio e la data fine pena, rilevandole dai dati presenti sul procedimento SIEP a cui è collegato.
La nuova funzione sarà inserita nel menu Scadenzari:

Selezionandola il sistema invierà la seguente form:

Dopo aver impostato i filtri di ricerca e confermato, il sistema estrarrà tutti i procedimenti SIUS pendenti e collegati a procedimenti SIEP, recuperando gli estremi dei due procedimenti, le date inizio pena, fine pena e fine pena virtuale e visualizzerà la form:

Per ciascun elemento dell’Elenco è possibile accedere al Dettaglio Procedimento SIUS e al Dettaglio Procedimento SIEP, cliccando sui rispettivi Anno/Numero.
Se è stata impostata l’estrazione su data fine pena virtuale, il sistema estrarrà solo i procedimenti collegati a procedimenti SIEP con data fine pena virtuale valorizzata.
## Condivisione Calcolatrice Nordio di SIEP
Requisito utente: Inserire la Calcolatrice Nordio anche in SIUS.
Intervento: la richiesta è stata già realizzata e rilasciata. Ma a seguito degli interventi che saranno realizzati sulla Calcolatrice, descritti al par. 2.1, fermo restando la possibilità da parte della Sorveglianza di poter utilizzare la calcolatrice per verificare la correttezza dei dati pervenuti da SIEP, bisognerà intervenire sulla funzione eliminando dalla maschera finale della stessa il tasto Valida, in quanto il calcolo e la validazione del fine pena virtuale è di competenza degli uffici esecuzione.
Da decidere con i GdL dell’Amministrazione se abilitare la validazione del fine pena virtuale per i procedimenti SIEP, collegati a procedimenti SIUS di Esecuzione Pena Sostitutiva, in tal caso il calcolo della data fine pena virtuale eseguito da SIUS, sarebbe validato su SIEP.