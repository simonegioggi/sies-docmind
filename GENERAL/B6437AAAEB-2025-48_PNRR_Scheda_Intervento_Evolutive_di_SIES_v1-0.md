---
uniqueName: b6437aaaeb-2025-48pnrrschedainterventoevolutivedis
displayName: "B6437AAAEB 2025 48 PNRR Scheda Intervento Evolutive di SIES v1 0"
category: "GENERAL"
tags: []
---

# B6437AAAEB-2025-48_PNRR_Scheda_Intervento_Evolutive_di_SIES_v1.0

> **File originale:** `MEV/SCHEDA_48/B6437AAAEB-2025-48_PNRR_Scheda_Intervento_Evolutive_di_SIES_v1.0.docx`  
> **Tipo:** DOCX

---



Ministero della Giustizia
Dipartimento per l’innovazione tecnologica della giustizia

SCHEDA INTERVENTO
INTERVENTI EVOLUTIVI SULL’APPLICAZIONE SIES

| Prospetto Informativo Sintetico | Prospetto Informativo Sintetico |
| --- | --- |
| INTERVENTO | Interventi evolutivi sull’applicazione SIES |
| CONTRATTO DI RIFERIMENTO | Accordo Quadro per l’affidamento di servizi applicativi in ottica cloud e l’affidamento di servizi di demand e PMO per le pubbliche amministrazioni centrali ID 2483 – Seconda Edizione - Lotto 1 – Digitalizzazione Area Penale – CIG B6437AAAEB |
| Milestone PNRR | M1C1-38 bis 
Interventi già programmati per il 2024 su sistemi complementari ad APP per la digitalizzazione del processo penale di primo grado (B2) |
| CICLO DI VITA | Ridotto |
| DOCUMENTO | Scheda Intervento: B6437AAAEB_2025_48 |
| FILE | B6437AAAEB-2025-48_PNNR_Scheda_Intervento_Evolutive_di_SIES_v1.0 |
| DATA DOCUMENTO | 22/12/2025 |
| FORNITORE | RTI - Accenture |

l
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

Requisito utente:

Intervento:

## Annotazione revoca beneficio ex art.168 c.p. - 674 c.p.p. – pene sospese

Requisito utente: Al momento la funzione effettua l’iscrizione di un nuovo procedimento in classe I con gli stessi dati del procedimento di classe III, si richiede di dare la possibilità di selezionare la classe di appartenenza in cui iscrivere il nuovo procedimento.

Intervento: si modificherà la funzione delegando all’utente la possibilità di selezionare la classe di appartenenza (tra le sette al momento previste in SIEP) in cui iscrivere il nuovo procedimento che viene creato a seguito della revoca del beneficio della sospensione della pena. Il procedimento che sarà iscritto, come già avviene per il classe I, erediterà tutti i dati presenti sul classe III.


## Archiviazione procedimento per passaggio di classe

Requisito utente: Al momento il sistema non permette di iscrivere un nuovo procedimento a carico di un soggetto per lo stesso titolo esecutivo già presenti in base dati. Il problema è rilevante quando la reiscrizione del procedimento è necessaria a seguito di una iscrizione del procedimento in una classe di appartenenza errata. Per aggirare il problema si procede iscrivendo un Titolo con i dati significativi alterati con l’inserimento di caratteri fittizzi.

Intervento: Sarà realizzata una nuova funzione ‘Passaggio di classe’, che sarà inserita nel menu Definizione Procedimento, che effettuerà l’archiviazione del procedimento iscritto erroneamente e la contestuale iscrizione di un nuovo procedimento nella classe selezionata dall’operatore. Il nuovo procedimento erediterà tutti i dati presenti nel procedimento di provenienza.


## Elenco procedimenti assegnati al magistrato
Requisito utente: rivedere la funzione per risolvere le difficoltà di utilizzo in caso di magistrato assegnatario di un grande numero di procedimenti.
Intervento: la funzione, finalizzata alla riassegnazione dei procedimenti da un magistrato all’altro, al momento presenta un Elenco dei procedimenti non impaginato, per cui in caso di un grande numero di procedimenti presenta una pagina molto lunga che è difficoltosa da gestire per l’operatore, inoltre, in caso di selezione dell’opzione tutti, il sistema può andare in errore per esaurimento delle risorse e presenta una pagina di errore di difficile interpretazione da parte dell’utente.
Si interverra sulla funzione presentando un Elenco procedimenti Impaginato (20 per pagina) e sarà aggiunta, alle attuali opzione di selezione singolo procedimento o tutti, l’opzione di selezione di tutti i procedimenti contenuti nella pagina corrente. Inoltre satà gestito l’errore conseguente alla selezione dell’opzione tutti, in caso di migliaia di procedimenti, con un messaggio parlante all’operatore di rieffettuare l’operazione selezionando i procedimenti per singola pagina.

## Dettaglio Procedimento SIEP

Requisito utente: Nell’attuale form Dettaglio Procedimento SIEP, come gia’ avviene per i procedimenti Migrati, etc., si chiede di inserire la dicitura Cartabia se tutti i reati inseriti sul procedimento sono successivi al 30/12/2022

Intervento: Si interverrà nella funzione per effettuare una verifica sulle date commesso reato di tutti i reati presenti nel procedimento, se tutte le date valorizzate sono successive al 30/12/2022, si riportera accanto successivamente all’anno/numero procedimento la dicitura Cartabia.

## Reimpostazione dati utente e password NSC in Richiesta Certificato penale

Requisito utente: Al momento quando si richiede la generazione del Certificato Penale di NSC, dopo aver impostato i dati dell’utente e la relativa pwd alla prima volta che l’utente utilizza la funzione, il sistema non dà più la possibilità di modificarli anche in caso di errori nella digitazione, per cui bisogna poi richiedere l’intervento dell’Assistenza.

Intervento: La funzione sarà rivista mostrando sempre nella form di richiesta i campi Userid e Password con i dati già presenti in SIES o vuoti, se al primo utilizzo, con possibilità di poterli ridigitare e quindi reimpostarli manualmente in autonomia.

## Gestione Confisca per equivalente

Requisito utente: Sarebbe necessario poter evidenziare quando la pena pecuniaria di notevole importo sia conseguente a Confisca per equivalente

Intervento: Le funzioni di inserimento, modifica e dettaglio della pena compelssiva saranno modificate inserendo nelle form un check box da selezionare se l’importo della pena pecuniaria è conseguente a Confisca per equivalente. Sarà rivista anche la funzione Dettaglio procedimento per riportare la nuova dicitura quando presente sulla pena complessiva.


## Presa in carico procedimenti da fuori distretto

Requisito utente: Rivedere la funzione di presa in carico dei procedimenti pervenuti per competenza e presi incarico da altro distretto in presenza di incidente di esecuzione già iscritto nel sottosistema SIGE

Intervento: Al momento se si prende in carico un procedimento proveniente da altro distretto già presente sulla base dati richiedente, a cui è collegato un procedimento SIGE degli uffici giudicanti del distretto richiedente, la procedura di aggiornamento dei dati già presenti in base dati va in errore non potendo eliminare i dati di SIEP (REATO, CIRCOSTANZA, PENA_COMPLESSIVA, BENEFICIO, PENA_ACCESSORIA, MISURA_SICUREZZA) condivisi con il procedimento SIGE.
La procedura sarà modificata duplicando le informazioni SIEP condivise con SIGE e ricreando i collegamenti con i dati duplicati, senza alterare le informazioni originali.

## Template provvedimento determinazione pene concorrenti (Cumulo)
Requisito utente: Aggiornamento sezione rideterminazione della pena relativa all’indicazione  dei   periodi di pena espiata :
Differimento pena;
Rideterminazione pena (altro);
Liberazione anticipata;
Espiazione pregressa;
Periodi di pena espiata per interruzione della pana principale (sospensioni differimenti Ecc.
Pagamento pena pecuniaria

Intervento: le informazioni relative ai punti da a a f sono gestite all’interno dei singoli template, sono a detta dell’Amministrazione tutti dati già presenti nel sistema e trattati all’interno del modulo Cumulo, bisognerà pertanto intervenire nei singoli template (sono gestiti 21 diversi template) apportando le necessarie correzioni.
Considerando la complessita della materia CUMULO, come già evidenziato nel corso delle call svoltesi, è fondamentale il supporto del GdL SIEP nel creare le casistiche con le anomalie lamentate e indicare le opportune correzioni. Questo aspetto vale anche per le segnalazioni ai punti successivi.

## Allineare tutti i template “emissione provvedimento” (Cumulo)

Requisito utente: I dati presenti nella sezione “Osserva”  del “Prospetto Cumulo (Proposta)  vanno replicati sui provvedimenti finali, dopo l’aggiornamento di cui al par. 2.7.

Intervento: per riportare i dati presenti nel Prospetto Cumulo (Proposta)  sono gestite all’interno dei singoli template dei provvedimenti, bisognerà intervenire nei singoli template (sono gestiti 21 diversi template) apportando le necessarie correzioni.

## Revisione e gestione delle frasi inerenti alle richieste del pubblico ministero al giudice dell’esecuzione (Cumulo)
Requisito utente: Per tutte le richieste del PM al GE
a)	Rivedere le motivazioni delle richieste del Pubblico Ministero;
b)	Migliorare l’impaginatura e le frasi delle richieste;
c)		Semplificazione della Gestione delle richieste, differenziando la fase di richiesta al giudice e redazione del cumulo;
d)		Annotazione cumulativa delle ordinanze del giudice dell’esecuzione per tutte le richieste del PM;

Intervento: le informazioni relative ai punti da a a d sono gestite all’interno dei singoli template delle richieste del PM al GE, sono a detta dell’Amministrazione tutti dati già presenti nel sistema e trattati all’interno del modulo Cumulo, bisognerà pertanto intervenire nei singoli template (sono gestiti 	9 diversi template) apportando le necessarie correzioni.

## Ripristino pene sospese (Cumulo)

Requisito utente: Rendere visibile le pene sospese nella funzione “rideterminazione della pena”, gestire la fase dei conteggi della pena, in presenza dell’annotazione della revoca del beneficio o anticipazione degli effetti. Considerarle anche in assenza della fase di stampa. Sarà realizzata la funzione di validazione anche in assenza della stampa.

Intervento: Si interverrà sulla funzione ‘Pene Rideterminate’ in Dati Finali Cumulo per visualizzare e conteggiare i dati relativi ai procedimenti di classe III, sarà rivisto l’ordinamento con cui vengono presentati i Titoli coinvolti in cumulo ordinandoli per data emissione crescente.
Al momento tutte le richieste PM al Ge e alla Sorveglianza vengono coinvolte nei conteggi solo se validate, operazione che può essere effettuata solo dopo aver stampato le richieste, operazione non sempre effettuata dagli uffici. Per poter validare le suddette richieste anche in assenza di stampa, sarà inserita sul Dettaglio della singola richiesta l’azione di stampa.

## Incongruenza dei dati sulla continuazione e revoca benefici attivare alert visibile all’operatore (Cumulo)

Requisito utente: Il sistema prevede la segnalazione dell’anomalia in caso di revoca benefici in sentenza e pena in continuazione ma è visibile solamente all’interno delle funzioni.
Intervento: Il sistema già segnala l’inconguenza dei dati nella funzione Dettaglio Pena Complessiva relativa al Titolo cumulato visualizzando un triangolino giallo accanto alla sentenza in continuazione, ma non sempre l’operatore presta attenzione alla segnalazione, per cui si interverrà nella funzione Pene Rideterminate in Dati finali cumulo con un messaggio a video  descrittivo dell’anomalia presente sui Dati Finali Cumulo.

## Atti pervenuti per competenza al cumulo

Requisito utente: Tutti gli atti pervenuti per competenza devono:
essere visibili all’operatore, eliminare condizione date criteri di ricerca;
Il sistema deve prendere in carico gli atti pervenuti in automatico, senza l’intervento dell’operatore, per evitare , in caso di aggiornamenti del sistema, una nuova richiesta.

Intervento: limitato solo al punto a) Al momento le funzioni Presa in carico>>Atti ricevuti per competenza>>Elenco Atti Ricevuti e Atti Ricevuti per competenze cumulo (icona AP) limitano la ricerca solo agli atti pervenuti negli ultimi due mesi dalla data di elaborazione. Le funzioni saranno riviste presentando una form in cui sarà possibile impostare uno dei seguenti criteri di ricerca: periodo date ricezione, Ufficio Richiedente, Anno/Numero procedimento trasmesso, Anno/Numero procedimento Cumulante, Cognome e Nome Soggetto con conseguente modifica delle attuali modalità di estrazione.
Per il requisito al punto b) si rimanda a quando sarà affrontato l’annoso argomento della presa in carico automatica di tutti gli atti.

## Prevedere la funzione trasmissione atti per competenza in fase di istruttoria (Cumulo)

Requisito utente: Qualora, in fase di istruttoria, cambia la competenza all’emissione del provvedimento di cumulo  l’ufficio deve essere in grado di trasmettere l’intera istruttoria ad un proprio procedimento o ad altro ufficio gli atti.
Intervento: Nel menu Istruttoria cumulo sarà realizzata una nuova funzione ‘Trasmissione per competenza’ che presenterà una form in cui l’operatore dovrà indicare anno e numero di altro procedimento del proprio ufficio su cui si vogliono trasferire i dati dell’istruttoria ancora aperta, sulla conferma il sistema presenterà i dati del procedimento destinatario e chiederà conferma a procedere. A seguito della conferma il sistema aprirà una nuova istruttoria sul procedimento destinatario in cui trasferirà tutti i dati presenti nell’istruttoria di origine, che verrà chiusa per trasferimento per competenza.
Non ci sarebbero problemi tecnici nell’estendere il trasferimento anche verso procedimenti di altri uffici del Distretto, ma ci sono problemi formali da rispettare con richiesta da parte dell’ufficio che deve aprire la nuova istruttoria e con la trasmissione da parte dell’ufficio che deve trasmettere, attività che al momento rimangono tracciate con le funzionalità già presenti nel sistema.


## Rivedere la gestione delle annotazioni di trasmissione e presa in carico e redazione cumulo

Requisito utente:  Prevedere un’annotazione singola o unica delle tre voci;
Effettuata l’annotazione i dati devono essere eliminati dalle liste;
Eliminazione dei dati pregressi nella funzione;
Rendere obbligatorie le annotazioni passando dalla funzione.

Intervento: saranno riviste le funzioni Riscontro Richieste, Atti ricevuti per competenza, Restituzione Atti, Riscontro Trasmissioni/Solleciti per apportare dei miglioramenti gestionali secondo indicazioni più dettagliate fornite dal GdL SIEP.

## Frasi ordine esecuzioni    (Cumulo)

Requisito utente:        a)	   Introdurre avvisi Cartabia; riportare i rigetti
Nordio Introdurre conteggi liberazioni anticipata sul cumulo apportando modifica  funzione con periodi liberazione anticipata rigettati

Intervento: sarà realizzato un template che riporterà delle frasi statiche relative alla riforma Cartabia e al decreto Nordio, che sarà inserito e richiamato in coda agli attuali template relativi ai provvedimenti di cumulo (21). Sarà cura dell’utente inserire eventuali informazioni aggiuntive.

## Funzione pene rideterminate (Cumulo)

Requisito utente:

Intervento:   	sarà  modificata la funzione  Pene Rideterminate modificando l’ordinamento dei Titoli  in base alla data di emissione crescente,  inglobando nell’elenco anche le sentenze in continuazione, riordinando i periodi di presofferto dalla data più vecchia alla più recedente  ed evidenziando eventuali sovrapposizione e visualizzando il Titolo esecutivo di riferimento passando il mouse sopra.

## Ricerca soggetto da Iscrizione proprio titolo (Cumulo)

Requisito utente: Rivedere i criteri di ricerca soggetti
Intervento:   L’attuale ricerca in cumulo, provenendo dalla form Elenco Titoli cumulati, effettua di default la ricerca dei soggetti aventi gli stessi dati del Soggetto del titolo cumulante, per cui basta una differenza su uno dei dati per avere risultato nullo. La funzione sarà modificata, rivedendo i criteri di ricerca, in presenza del CUI, effetuerà la ricerca per codice CUI, ma sarà possibile nella form selezionare gli altri dati di ricerca: Cognome, Nome, data nascita, Luogo nascita, Stato di Nascita e anche per anno e numero procedimento.


# Interventi SIUS
Di seguito sono riportate alcune richieste/segnalazioni del GdL SIUS su cui si interverrà per la soluzione.

## Aggiunta di un nuovo esito

Requisito utente: Relativamente al contenuto

Conversione pene pecuniarie principali per mancato pagamento (artt. 102 - 103 L. 689/81 - 55 d. lgs. 274/00) (U142)
e ai relativi oggetti

Conversione pene pecuniarie principali per mancato pagamento (artt. 102 - 103 L. 689/81)  (3180)

Conversione pene pecuniarie principali per mancato pagamento (art. 55 d. lgs. 274/00) - art. 55 d. lgs. 274/00	(3181)

Intervento: Sarà aggiunto nella base dati l’esito “Dispone conversione pena irrogata dal Giudice di pace in permanenza domiciliare” , inserendo nella tabella CG_REF_CODES un nuovo record per il dominio ESITO_PROVVEDIMENTO e uno per il dominio ESITO_TENORE.

## Scadenzario monitoraggio misure alternative espiate.

Requisito utente: Occorre implementare la funzione “scadenziari” inserendone uno che punti al fine pena delle EMA, in modo da avere in evidenza le scadenze pena dei condannati in misura alternativa. Il fine pena andrebbe rilevato dal dato presente sul procedimento SIEP collegato al fascicolo di EMA.

Intervento: Sarà realizzata una nuova funzionalità che permetterà di ricercare i procedimenti di Esecuzionne Misura Alternativa (tutti, per anno, scaduti o in scadenza) che visualizzerà la data inizio e la data fine misura, rilevandolo dai dati presenti su SIUS e/o sul procedimento SIEP a cui è collegato.

## Gestione permessi

Requisito utente: Dalla statistica trimestrali dei permessi non esce il dato dei permessi di necessità concessi ai detenuti condannati per i delitti previsti dall’art. 51, commi 3 bis e 3 quater cpp e dei detenuti sottoposti al regime di cui all’art. 41 bis OP.
Intervento: il dato richiesto non è al momento presente nella base dati. Si interverrà nella funzione Decreto Permesso aggiungendo nell’attuale form due check box, non obbligatori, che permettano all’utente di indicare se il condannato è detenuto per i delitti previsti dall’art. 51 commi 3 bis e 3 quater cpp o se è sottoposto al regime di cui all’art. 41 bis OP, il nuovo dato sarà acquisito nella base dati. Si interverra negli attuali template del provvedimento evidenziando il dato.
Sarà rivista la funzione di Riepilogo Trimestrale estraendo anche il nuovo dato, che sarà visibile a video e nel relativo template.

## Aggiunta nuovo oggetto
Requisito utente: Occorre aggiungere al contenuto “Sospensione Esecuzione pene sostitutive”, l’oggetto “Sospensione pena sostituiva per arresto o fermo di condannato (art. 68 L. 689/1981) - art. 68 L. 689/1981” .
Intervento: Sarà inserito nel DB nella tabella CG_REF_CODES un nuovo record per il dominio ‘MOTIVO_PROVVEDIMENTO’.

## Elenco Procedimenti Assegnati
Requisito utente: rivedere la funzione per risolvere le difficoltà di utilizzo in caso di magistrato assegnatario di un grande numero di procedimenti.
Intervento: la funzione, finalizzata alla riassegnazione dei procedimenti da un magistrato all’altro, al momento presenta un Elenco dei procedimenti non impaginato, per cui in caso di un grande numero di procedimenti presenta una pagina molto lunga che è difficoltosa da gestire per l’operatore, inoltre, in caso di selezione dell’opzione tutti, il sistema può andare in errore per esaurimento delle risorse e presenta una pagina di errore di difficile interpretazione da parte dell’utente.
Si interverra sulla funzione presentando un Elenco procedimenti Impaginato (20 per pagina) e sarà aggiunta, alle attuali opzione di selezione singolo procedimento o tutti, l’opzione di selezione di tutti i procedimenti contenuti nella pagina corrente. Inoltre satà gestito l’errore conseguente alla selezione dell’opzione tutti, in caso di migliaia di procedimenti, con un messaggio parlante all’operatore di rieffettuare l’operazione selezionando i procedimenti per singola pagina.

## Reimpostazione dati utente e password NSC in Richiesta Certificato penale

Requisito utente: Al momento quando si richiede la generazione del Certificato Penale di NSC, dopo aver impostato i dati dell’utente e la relativa pwd alla prima volta che l’utente utilizza la funzione, il sistema non dà più la possibilità di modificarli anche in caso di errori nella digitazione, per cui bisogna poi richiedere l’intervento dell’Assistenza.

Intervento: La funzione sarà rivista mostrando sempre nella form di richiesta i campi Userid e Password con i dati già presenti in SIES o vuoti, se al primo utilizzo, con possibilità di poterli ridigitare e quindi reimpostarli manualmente in autonomia.


# Pianificazione temporale delle attività

Sono esclusi dal presente piano le tempistiche relative al consolidamento dei requisiti che potranno essere oggetto di una successiva emissione del presente piano con aggiornamento dei tempi relativi sia alla fase di analisi, sia a quella di sviluppo.
A valle del consolidamento dei requisiti, il fornitore si riserva la facoltà di emettere un successivo piano con gli aggiornamenti.
Quanto non esplicitamente indicato nella presente scheda di intervento è da ritenersi non contemplato ed esterno al perimetro della MEV del presente documento.

Il pronti alla verifica di conformità sarà dato entro il 15 12 2025

# Importo intervento

Di seguito si riporta la stima dell’intervento:

| Attività | Giornate
Uomo previste | Tariffa (€) | Valore economico (€) |
| --- | --- | --- | --- |
| MVC | 1750 | 180 € | 315.000,00 € |
| TOTALE |  |  | 315.000,00 € |


Gli importi si intendono iva esclusa.