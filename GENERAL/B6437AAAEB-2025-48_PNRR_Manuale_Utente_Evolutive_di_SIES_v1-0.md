---
uniqueName: b6437aaaeb-2025-48pnrrmanualeutenteevolutivedisies
displayName: "B6437AAAEB 2025 48 PNRR Manuale Utente Evolutive di SIES v1 0"
category: "GENERAL"
tags: []
---

# B6437AAAEB-2025-48_PNRR_Manuale_Utente_Evolutive_di_SIES_v1.0

> **File originale:** `MEV/SCHEDA_48/B6437AAAEB-2025-48_PNRR_Manuale_Utente_Evolutive_di_SIES_v1.0.docx`  
> **Tipo:** DOCX

---



Ministero della Giustizia
Dipartimento per l’innovazione tecnologica della giustizia

MANUALE UTENTE
INTERVENTI EVOLUTIVI SULL’APPLICAZIONE SIES

| Prospetto Informativo Sintetico | Prospetto Informativo Sintetico |
| --- | --- |
| INTERVENTO | Interventi evolutivi sull’applicazione SIES |
| CONTRATTO DI RIFERIMENTO | Accordo Quadro per l’affidamento di servizi applicativi in ottica cloud e l’affidamento di servizi di demand e PMO per le pubbliche amministrazioni centrali ID 2483 – Seconda Edizione - Lotto 1 – Digitalizzazione Area Penale – CIG B6437AAAEB |
| Milestone PNRR | M1C1-38 bis 
Interventi già programmati per il 2024 su sistemi complementari ad APP per la digitalizzazione del processo penale di primo grado (B2) |
| CICLO DI VITA | Ridotto |
| DOCUMENTO | Manuale Utente: B6437AAAEB_2025_48 |
| FILE | B6437AAAEB-2025-48_PNRR_Manuale_Utente_Evolutive_di_SIES_v1.0 |
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

Nel documento sono descritti gli interventi urgenti realizzati in SIES, ambiti SIEP e SIUS, per il miglioramento del sistema.
# Interventi SIEP
Di seguito sono riportati gli interventi realizzati sul sottosistema dell’esecuzione.
## Annotazione revoca beneficio ex art.168 c.p. - 674 c.p.p. – pene sospese
La funzione già presente nel sistema è stata modificata consentendo, al momento dell’archiviazione del procedimento di classe III, di poter iscrivere il procedimento in una delle classi previste in SIES, escludendo la classe III.





A seguito della compilazione e della Conferma, il sistema invia il nuovo messaggio

che per il nuovo procedimento non fa più riferimento alla classe I, ma alla classe che l’utente indicherà nella form successiva:

In cui l’utente potrà indicare la nuova classe, ad esclusione della III, in cui inserire il nuovo procedimento, ad es. in caso di classe II presenterà il dettaglio del nuovo procedimento

e contestualmente archivierà il procedimento di classe III

## Archiviazione procedimento per passaggio di classe
La nuova funzione ‘Passaggio di classe’, presente nel menu Definizione Procedimento, effettua l’archiviazione del procedimento iscritto erroneamente e la contestuale iscrizione di un nuovo procedimento nella classe selezionata dall’operatore, bypassando il controllo da parte del sistema di esistenza di un procedimento anche in altra classe con stesso titolo e stesso soggetto, che ne inibisce l’inserimento. Il nuovo procedimento erediterà tutti i dati presenti nel procedimento di provenienza, esclusi gli eventi specifici del procedimento origine.

Selezionando la nuova funzione per un procedimento iscritto erroneamente in una delle classi, gestite al momento in SIES, si riceverà la seguente maschera

Dopo la compilazione della form e la Conferma, il sistema invia la seguente form:

In cui l’utente può modificare la Data arrivo atto e la Data irrevocabilità, precompilate dal sistema, e selezionare la nuova classe di appartenenza in cui iscrivere il nuovo procedimento. A seguito della Conferma il sistema invia il seguente messaggio.

N.B. fino a questa fase nessun aggiornamento è stato ancora eseguito sulla Base Dati




A seguito della conferma a proseguire (OK) il sistema inserirà nella base dati l’evento di  Archiviazione del procedimento corrente, inserirà il nuovo procedimento assegnandogli il primo progressivo libero nell’ambito dell’Anno e della classe e presenterà il Dettaglio dell’Annotazione dell’archiviazione, in cui sarà presente anche il link al nuovo procedimento.

Dalla form di Dettaglio è possibile procedere alla stampa del provvedimento di archiviazione e alla successiva validazione o procedere direttamente alla validazione, senza produrre alcun documento.

Esempio provvedimento di archiviazione






Si è intervenuti anche sulla statistica Attività Magistrati per contabilizzare anche i procedimenti archiviato per Passaggio classe. A tal fine è stata aggiunta la nuova voce, evidenziata di seguito nel riquadro in rosso, nell’ambito dei procedimenti con Archiviazioni – non luogo a provvedere.


## Elenco procedimenti assegnati al magistrato
La funzione, finalizzata alla riassegnazione dei procedimenti da un magistrato all’altro, è stata modificata per ovviare alle difficoltà di gestione in caso di magistrato con elevato numero di procedimenti assegnati, che presentava  un Elenco su unica pagina, che richiedeva all’operatore un continuo scrolling per individuare i procedimenti di interesse.
La funzione modificata, attivabile sempre dal menu Funzioni Amministrative » Gestione Magistrati » Elenco Procedimenti Assegnati, presenta la form

In cui l’utente indica il magistrato di cui si vuole conoscere l’Elenco dei procedimenti a suo carico, selezionandolo dalla popup che si attiva cliccando sulla cartella. A seguito della conferma il sistema invia l’Elenco impaginato dei procedimenti (20 per pagina)

Per la riassegnazione di parte o di tutti i procedimenti, la form presenta adesso le seguenti opzioni:
Spuntare i procedimenti singolarmente per pagina e Confermare;
Spuntare tutti i procedimenti di una pagina, cliccando su Selezioni tutti nella pagina e Confermare;
Spuntare tutti i procedimenti in carico al magistrato, cliccando Seleziona tutti i NN procedimenti del magistrato e Confermare.
A seguito della Conferma il sistema aggiornerà la base dati riassegnando i procedimenti indicati al nuovo magistrato, indicato nella form e presenterà l’Elenco dei procedimenti riassegnati

Inoltre in caso di numero eccessivo di procedimenti selezionati per cui il sistema potrebbe non completare l’operazione per esaurimento delle risorse allocate, al posto di un messaggio di errore di tipo tecnico non interpretabile dall’utente, è stato inserito il seguente messaggio:

## Dettaglio Procedimento SIEP
La funzione è stata rivista per effettuare una verifica sulle date commesso reato di tutti i reati presenti nel procedimento, se almeno una delle date valorizzate è successiva al 30/12/2022, si riporterà successivamente all’anno/numero procedimento la dicitura Cartabia.


La dicitura sarà riportata nella intestazione di maggior parte delle altre funzioni SIEP
E’ riportato di seguito, per completezza di documentazione, il caso “irreale” di un procedimento migrato con presenza di reati commessi successivamente al 30/12/2022.

## Reimpostazione dati utente e password NSC in Richiesta Certificato penale
La funzione è stata modificata per mostrare sempre nella form di richiesta i campi Userid e Password con i dati già presenti in SIES o vuoti, se al primo utilizzo, con possibilità di poterli ridigitare e quindi reimpostarli manualmente in autonomia.



## Gestione Confisca per equivalente
Le funzioni di inserimento, modifica e dettaglio della pena complessiva sono state modificate per poter evidenziare quando l’importo da pagare della pena pecuniaria include un importo conseguente a confisca per equivalente. A tal fine si è intervenuti nelle suddette funzioni inserendo nelle form un check box da selezionare se l’importo della pena pecuniaria è conseguente a Confisca per equivalente. E’ stata rivista anche la funzione Dettaglio procedimento per riportare la nuova dicitura quando presente sulla pena complessiva.

Nella funzione Inserimento Pena Complessiva è stato aggiunto il Check box Confisca per equivalente

da impostare se una delle pene pecuniarie gestite nella form (multa, ammenda, sanzione sostitutiva – pena pecuniaria, pena pecuniaria sostitutiva) è conseguente a Confisca per equivalente.
Se in fase di inserimento o modifica della pena complessiva è stato impostato il check box, sul dettaglio della pena complessiva sarà riportata in rosso la dicitura

Stessi interventi effettuati anche sulla funzione modifica



In caso di avvenuta selezione del check box sulla pena complessiva, nel Dettaglio Procedimento sarà presente la dicitura indicata di seguito dalla freccia rossa

## Presa in carico procedimenti da fuori distretto
Premessa, la presa in carico di un procedimento SIEP da altra BDI, dovendo prevedere l’aggiornamento dello stesso se già presente sulla base dati richiedente, è realizzata con la cancellazione di tutti i dati preesistenti ed il reinserimento dei dati aggiornati provenienti dalla BDI originaria.

D’ altra parte quando si iscrive un procedimento SIGE collegandosi a un procedimento SIEP, alcune informazioni di quest’ultimo (tabelle REATO, CIRCOSTANZA, PENA_COMPLESSIVA, BENEFICIO, PENA_ACCESSORIA, ALTRA_CAUSA. LUOGO_DETENZIONE) vengono condivise con il procedimento SIGE. Quando il procedimento SIGE è collegato a un procedimento appartenente ad altra BDI, al momento in cui un qualsiasi ufficio del Distretto tenta di prendere in carico nuovamente il procedimento SIEP dalla BDI originaria, il sistema va in errore in quanto non riesce a cancellare le informazioni condivise con SIGE, fornendo il seguente messaggio:





E’ stata modificata la procedure plsql PULISCI_ALTRA_BDI, implementando delle nuove sotto procedure, che provvedono a duplicare le informazioni di SIEP condivise, scollegandole da quest’ultimo e rendendole valide solo per il procedimento SIGE, per poter poi procedere alla cancellazione di quelle collegate al procedimento SIEP.

Le sotto procedure realizzate sono

PROCEDURE pulisci_benefici (idfascicolo          IN NUMBER,
esitoPulisciBenefici IN OUT VARCHAR2);
PROCEDURE pulisci_circostanza (idfascicolo             IN NUMBER,
esitoPulisciCircostanza IN OUT VARCHAR2);
PROCEDURE pulisci_reati (idFascicolo       IN NUMBER,
esitoPulisciReati IN OUT VARCHAR2);
PROCEDURE pulisci_pena_complessiva (idFascicolo       IN NUMBER,
esitoPulisciPenaCompl IN OUT VARCHAR2);
PROCEDURE pulisci_pene_accessorie (idFascicolo       IN NUMBER,
esitoPulisciPeneAcc IN OUT VARCHAR2);
PROCEDURE pulisci_luogo_detenzione (idFascicolo       IN NUMBER,
esitoPulisciLuogoDet IN OUT VARCHAR2);
PROCEDURE pulisci_altra_causa (idFascicolo     IN NUMBER,
esitoAltraCausa IN OUT VARCHAR2);

Tutto quanto descritto avviene in modalità trasparente per l’utente finale, per il quale non sono state modificate le attuali modalità operative.
## Template provvedimento determinazione pene concorrenti (Cumulo)
Sono stati rivisti tutti i template relativi ai diversi provvedimenti di cumulo, intervenendo nelle seguenti sezioni degli stessi:
Stato esecuzione Titolo cumulato
Nello stato di esecuzione non sono riportati tutti gli eventi del procedimento coinvolto in cumulo, ma solo quelli ritenuti, al momento della realizzazione, più significativi dal Gruppo di Lavoro SIES ai fini del provvedimento di cumulo. Si è intervenuti per riportare anche i provvedimenti di cumulo e le richieste relative ai benefici. Di seguito un esempio:


Osserva
Al momento in questa sezione sono riportate tutte le richieste del PM al GE e alla Sorveglianza emesse dal momento dell’apertura dell’istruttoria cumulo, senza alcuna annotazione dell’avvenuta emissione della decisione annotata nel sistema, d’altra parte le richieste già decise non dovrebbero essere riportate nella sezione CHIEDE. Per soddisfare questa esigenza, per tutte le richieste con decisione, è stata aggiunta la descrizione della decisione. Di seguito alcuni esempi:

È stata anche modificata la dicitura riportata nelle richieste in caso di Anticipazione degli effetti, che adesso appare come di seguito (scritta in grassetto)

CHIEDE
La sezione, prima riportata subito dopo la sezione Osserva è stata spostata in altra posizione del provvedimento, inoltre, come riportato al punto precedente, in essa non sono più riportate le richieste del PM al GE e alla Sorveglianza che sono già state decise. Di seguito, rifacendoci all’esempio riportato in precedenza per la sezione Osserva, in CHIEDE è riportata solo la seconda, perché priva di decisione:

Pena principale e pena espianda
In questa sezione si è intervenuti per riportare tutti i quantum di pena da detrarre alla Pena principale per arrivare alla pena da espiare. Di seguito un esempio:

Con gli interventi sopra riportati in questa sezione, sono riportati in stampa tutti i quantum riportati nella maschera Riepilogo Pene

## Allineare tutti i template “emissione provvedimento” (Cumulo)
Anche alle stampe dei prospetti

Sono state apportate le modifiche descritte al precedente paragrafo.
## Revisione e gestione delle frasi inerenti alle richieste del pubblico ministero al giudice dell’esecuzione (Cumulo)
Sono state riviste le funzioni di stampa delle Richieste del PM al GE e alla Sorveglianza nelle sezioni Osserva e CHIEDE, apportando le stesse modifiche descritte per le suddette sezioni al precedente par. 2.8.
2.10.1	Richiesta Benefici in Attività del PM (Cumulo)
All’interno del menu Attività del PM in Gestione Dati Analitici per un Titolo esecutivo coinvolto in cumulo è stata realizzata la funzione Richiesta Benefici al GE
Selezionandola si riceve la seguente maschera

Cliccando su  il sistema visualizza la form di Inserimento

In cui è possibile selezionare il Tipo di richiesta fra quelle previste nella relativa combo box:

Indicare da data della richiesta, il Giudice dell’esecuzione destinatario, i quantum di pena da detrarre/aggiungere e l’eventuale Anticipazione degli effetti.
A seguito della conferma il sistema inserisce la richiesta nella base dati e presenta la form di Dettaglio

Cliccando sull’icona  , il sistema ripresenta la form iniziale da cui è stato richiesto l’Inserimento, in cui sono riportati gli estremi della richiesta
Per la quale è possibile procedere alla Modifica e alla Cancellazione.


## Ripristino pene sospese (Cumulo)
Al momento per un titolo assorbito in cumulo con pena sospesa condizionalmente es:

la pena complessiva  è correttamente non conteggiata in Riepilogo delle Pene, ma non è visualizzato nella popup. A seguito degli interventi realizzati il titolo è visibile (in grigio) e continua a non essere conteggiato ai fini della Pena Principale in cumulo.

Posizionandosi con il mouse sull’icona , il sistema apre una finestra con l’indicazione sul motivo dell’esclusione.
Nel caso che la sospensione sia stata applicata solo alla pena detentiva, la pena pecuniaria viene conteggiata

E’ stato rivisto anche l’ordinamento dell’Elenco Titoli, che di default è crescente sulla data del Titolo. In ogni caso l’ordinamento è lo stesso di quello presente in Elenco Titoli coinvolti in cumulo

che può essere cambiato cliccando su una delle due icone indicate con la freccia rossa. Pertanto se si cambia l’ordinamento in questa form, cambierà anche in Riepilogo delle pene.
## Incongruenza dei dati sulla continuazione e revoca benefici attivare alert visibile all’operatore (Cumulo)
Prima del rilascio di questa MEV, nel caso in cui su una sentenza in cumulo sia stata indicata la continuazione con un’altra sentenza ma tale legame non fosse stato effettuato, l’anomalia viene segnalato solo sul dettaglio dati analitici della pena complessiva del titolo con il simbolo


Il sistema segnala che la sentenza indicata (inserita in questo caso a mano) non è nel cumulo, o non è stata correttamente agganciata, per cui la pena in continuazione viene calcolata sebbene non avrebbe dovuto in quanto il tipo di continuazione indicato è “Pena Complessiva Ritenuta la continuazione”, ovvero la pena indicata ingloba quella dell’altra sentenza.
Se l’utente non entra nel suddetto dettaglio può non accorgersi del problema.

Dopo gli interventi effettuati, nella sezione dei Dati Finali Cumulo è stato aggiunto un alert non bloccante

L’alert viene mostrato solo per il tipo di continuazione

In quanto impatta sul calcolo della pena, cliccando sul link Modifica Continuazione il sistema presenta la maschera per la modifica dei dati della continuazione

Dopo aver indicato la sentenza correttamente la sentenza assorbita, ritornando in dati finali cumulo non sarà più presente l’alert.
Nella popup del calcolo pena è stata evidenziata la sentenza in cui è indicata la continuazione (“cont”) e riportata quella “assorbita” con indicazione  della sentenza che la ha assorbita e del motivo della mancata visualizzazione dei quantum.
Posizionando il mouse sulla sentenza che dichiara la continuazione vengono evidenziate in giallo le sentenze assorbite

e viceversa posizionando il mouse sulla sentenza assorbita viene evidenziata in verde la sentenza che dichiara la continuazione



## Atti pervenuti per competenza al cumulo
Al momento le funzioni Presa in carico>>Atti ricevuti per competenza>>Elenco Atti Ricevuti e Atti Ricevuti per competenze cumulo (icona AP) ricercano gli atti pervenuti non ancora presi in carico relativi agli ultimi 2 mesi.

Le funzioni  sono state modificate con l’aggiunta nella maschera di nuovi campi di ricerca, pur presentando in apertura il risultato della ricerca limitatamente agli ultimi due mesi.

E’ possibile effettuare la ricerca impostando i seguenti filtri:

Intervallo data ricezione (inizio e fine periodo)
Ufficio Mittente (tipo e sede)
Anno e Numero procedimento trasmesso
Anno e Numero Procedimento Cumulante
Cognome e Nome del Soggetto

Nel caso che il documento inviato non sia più elaborabile (a causa modifica della struttura dati intervenuta successivamente alla data di trasmissione) nella colonna azioni sarà riportata l’icona , invece di quella di Dettaglio.
## Rivedere la gestione delle annotazioni di trasmissione e presa in carico e redazione cumulo
Prima del rilascio di questa MEV la funzione Riscontro Trasmissioni/Solleciti

non prevedeva alcuna funzione di filtro ed estraeva tutte le risposte di riscontro trasmissioni ricevute dall’ufficio elaborato o meno.

Il risultato era che nel tempo il numero di richieste è cresciuto enormemente creando difficoltà nell’utilizzo della funzionalità, che pur essendo paginata risultava inoltre lenta.

La funzione è stata modificata aggiungendo dei filtri di ricerca per i campi presenti in tabella

Di default la ricerca si limita alle risposte ricevute negli ultimi 2 mesi.

E’ possibile impostare i seguenti filtri di ricerca:
Intervallo date di ricerca
Ufficio mittente (Tipo e Sede)
Procedimento trasmesso (Anno e Numero)
Tipo Operazione (Comunicazione cumulo, Esito trasferimento Competenza, Esito seguito Atti).

E’ stata inoltre modificata anche la funzione di validazione dell’annotazione esito per marcare il messaggio come elaborato in modo che non esca più nella ricerca.

E’ stato inoltre ottimizzata la funzione di ricerca per renderla più veloce precaricando l’eventuale presenza di solleciti.

Per la gestione del pregresso, ovvero gli esiti ricevuti ed annotati ma per i quali il sistema non ha provveduto a marcarli come evasi, è stato predisposto uno script di bonifica.

Poiché l’utente potrebbe procedere all’annotazione esito direttamente sul dettaglio dell’evento di trasmissione senza passare per le liste degli esiti ricevuti, il che impedirebbe di marcare il messaggio come evaso, è stato previsto di presentare l’elenco dei messaggi di esito ricevuti anche sul dettaglio della trasmissione.

L’utente potrà quindi selezionare (check) il messaggio per procedere all’annotazione esito, oppure procedere tramite la x e marcare il messaggio come “evaso” in modo che non esca più sulla ricerca.
## Trasferimento e chiusura istruttoria cumulo
La nuova funzionalità “Trasferimento e Chiusura Istruttoria” è stata aggiunta nella griglia dell’istruttoria cumulo e consente di trasferire tutti i dati presenti in una istruttoria cumulo aperta su altro procedimento del proprio ufficio.
La funzione consente di:

Selezionare un nuovo procedimento (stesso ufficio) su cui trasferire l’istruttoria
Trasferire i dati dell’istruttoria in corso limitatamente ai dati dei titoli iscritti in istruttoria
Chiudere l’istruttoria corrente
L’utente deve indicare il fascicolo (proprio ufficio) su cui si vuole trasferire l’istruttoria

Il sistema verifica l’esistenza del fascicolo indicato e l’eventuale presenza di una istruttoria già aperta. Presenta l’elenco dei titolo nell’istruttoria corrente che saranno trasferiti


Se il sistema non trova una istruttoria aperta sul fascicolo di destinazione verrà aperta automaticamente e i fascicoli trasferiti.
Se è già presente una istruttoria aperta sul fascicolo di destinazione il sistema visualizza anche  il contenuto dell’istruttoria di destinazione e trasferirà tutti i fascicoli.

Selezionando il tasto di conferma

Al termine l’istruttoria corrente viene “Chiusa” ovvero annullata con la seguente motivazione



Selezionando il tasto “Apri Istruttoria” verrà aperta l’istruttoria in cui sono stati trasferiti i titoli.

Al termine del trasferimento e dopo la chiusura dell’istruttoria trasferita, se alcuni dei titoli trasferiti sono dell’ufficio il sistema aggiorna automaticamente su tali fascicoli i dati relativi al fascicolo su cui sono attualmente in istruttoria.
Es se il fascicolo 2025/7 è stato trasferito sul 2025/9 e l’istruttoria del 2025/9 viene poi trasferita sul 2025/10

Il sistema aggiorna l’indicazione

Sul procedimento dell’istruttoria cumulo trasferita viene inserito il seguente Evento
## Frasi ordine esecuzioni (Cumulo)
In tutti i provvedimenti di cumulo, prima della chiusura (data e firma), sono stati inseriti gli avvisi Cartabia, già presenti negli Ordini di esecuzione. Gli avvisi sono presenti solo se almeno un reato di uno dei Titoli Esecutivi coinvolti in cumulo risulta commesso in data successiva al 30/12/2022.
Gli avvisi sono i seguenti:

   Avvisa altresì la condannata che:
se il processo si è svolto in sua assenza, nel termine di trenta giorni dalla conoscenza della sentenza può chiedere, in presenza dei relativi presupposti, la restituzione nel termine per proporre impugnazione o la rescissione del giudicato, la richiesta va presentata alla Corte di Appello nel cui distretto ha sede il giudice che ha emesso il provvedimento;
in qualsiasi fase dell’esecuzione, l’autorità giudiziaria può disporre l’invio dei condannati e degli internati, previa adeguata informazione e su base volontaria, ai programmi di giustizia riparativa;
entro venti giorni dalla notifica dell’atto, può depositare presso la segreteria del pubblico ministero istanza di pagamento rateale della pena pecuniaria, ai sensi dell’articolo 133 -ter del codice penale.
Si accerti inoltre se la condannata è madre di prole minore e, in caso di esito positivo, si inoltri copia del presente provvedimento, unitamente al verbale di arresto, alla Procura della Repubblica presso il Tribunale per i Minorenni del luogo di esecuzione della sentenza ai sensi del comma 3 bis dell’art. 656 c.p.p.”.
N.B.  Il terzo capoverso sarà presente solo se nella pena da espiare è valorizzata la Multa e/o l’Ammenda, mentre il quarto capoverso è presente solo se il soggetto è femmina.
## Funzione pene rideterminate (Cumulo)
Di seguito sono riportati una serie di interventi fatti su varie funzioni del cumulo.

Elenco Richieste del PM al GE

Nella colonna Titoli è stata aggiunta anche la data


E’ stata  modificata la funzione  Pene Rideterminate riordinando i periodi di presofferto dalla data più vecchia alla più recedente  ed evidenziando eventuali sovrapposizione e visualizzando il Titolo esecutivo di riferimento passando il mouse sopra.

Nella popup delle pene rideterminate allo stato attuale  i periodi sono ordinati in base a:
Tipologia
Presofferti in sentenza
Presofferti disposti con provvedimenti
espiato
titolo
all’interno della tipologia sono ordinati per titolo
data emissione
all’interno della titolo sono ordinato per data emissione provvedimento
Inoltre il sistema non effettua nessun controllo sulla presenza di periodi sovrapposti o periodi continuativi.

Con gli interventi effettuati i periodi sono stati raggruppati in una unica tipologia e ordinati per data inizio periodo, inoltre in presenza di periodi continuativi il sistema calcola un unico periodo di espiazione e segnala eventuali sovrapposizione


Altro intervento ha riguardato l’inserimento della funzione di validazione sul Dettaglio della Richiesta Inviata
Eliminando l’obbligo di passare obbligatoriamente per la stampa della stessa.
Alert Misure di sicurezza – Pene Accessorie
Attuale funzionamento:
Se presenti “Misure di sicurezza” o “Pene Accessorie” su uno dei titoli assorbiti in cumulo viene impostato il segno di spunta sul tasto “Ulteriori sanzioni”. Ovvero tali misure e pene vengono inglobate nei dati finali cumulo di default.
Per escludere bisogna andare in dati finali – Ulteriori sanzione e nel dettaglio per togliere il segno di spunta.

Per le sole MS l’operatore dovrebbe decidere se iscrivere o meno le MS a un fascicolo di classe IV, da creare ex novo o già esistente

Tuttavia potrebbe dimenticare di effettuare una scelta e il sistema attualmente non lo segnala con il risultato che la MS pur essendo portata nei dati finali (di default) di fatto non viene iscritta su un nuovo procedimento.
Intervento:
Il sistema è stato modificato per segnalare la mancata scelta, segnalazione non bloccante.


Sul dettaglio delle ulteriori sanzioni è stata aggiunta la segnalazione della mancata scelta relativamente alla singola MS.

Inoltre nella funzione “Seleziona Misura Sicurezza” è stata aggiunta una ulteriore opzione di scelta:
“Non iscrivere le MS a Procedimento classe IV”.

L’utente, in presenza di MS selezionate, dovrà indicare esplicitamente cosa vuole fare con tale MS se non scriverle in alcun fascicolo, se iscriverle in un nuovo fascicolo o se aggiungerle a un fascicolo esistente.
Di default, come accade oggi il sistema iscrive tutte le misure nei dati finali, ma non opera una scelta sul come gestirle.
Dopo che l’utente avrà operato esplicitamente una scelta, verrà riportata sul dettaglio eliminando l’alert.


## Ricerca soggetto da Iscrizione proprio titolo (Cumulo)
L’attuale funzione Iscrizione Proprio Procedimento presente nella maschera Elenco Provvedimenti Esecutivi Coinvolti

effettua di default la ricerca dei soggetti aventi gli stessi dati del Soggetto del titolo cumulante, per cui basta una differenza su uno dei dati per avere risultato nullo.

La funzione è stata modificata, rivedendo i criteri di ricerca: in presenza del CUI, effettuerà la ricerca per codice CUI, ma sarà possibile nella form di Ricerca Procedimenti per Titolo e Soggetto

selezionare gli altri dati di ricerca: Cognome, Nome, data nascita, Luogo nascita, Stato di Nascita e anche per anno e numero procedimento, con la possibilità di poter indicare anche l’Ufficio accorpato.

E’ stata corretta gestione della popup comuni: agganciata la popup dei comuni attivi invece dei comuni di nascita creando problemi se l’anagrafica del soggetto era legata a un comune dismesso.
Aggiunta possibilità di escludere i campi dalla ricerca spuntando il relativo check box  o di ripristinare i valori originali, cliccando sull’icona .

E’ stata riformattata la visualizzazione colonna anno e numero per fascicoli di uffici accorpati

## Obbligo valorizzazione Difensore in Istruttoria cumulo
L’apertura dell’istruttoria cumulo richiedeva obbligatoriamente la presenza dell’avvocato nel procedimento SIEP, su richiesta del GdL è stata modificata la funzione eliminando l’attuale controllo che è stato spostato al momento in cui si seleziona la funzione Dati finali Cumulo:








# Interventi SIUS
Di seguito sono riportate alcune richieste/segnalazioni del GdL SIUS su cui si interverrà per la soluzione.
## Aggiunta di un nuovo esito
Per il contenuto UDS:
Conversione pene pecuniarie principali per mancato pagamento (artt. 102 - 103 L. 689/81 - 55 d. lgs. 274/00) (U142)
e relativi oggetti:
Conversione pene pecuniarie principali per mancato pagamento (artt. 102 - 103 L. 689/81)  (3180)
Conversione pene pecuniarie principali per mancato pagamento (art. 55 d. lgs. 274/00) - art. 55 d. lgs. 274/00	(3181)
E’ stato aggiunto nella base dati l’esito “Dispone conversione pena irrogata dal Giudice di pace in permanenza domiciliare” , inserendo nella tabella CG_REF_CODES un nuovo record per il dominio ESITO_PROVVEDIMENTO e uno per il dominio ESITO_TENORE.

Per la gestione del nuovo esito è stata modificata l’ordinanza prevista per il suddetto contenuto

che a seguito delle modifiche, in caso di selezione di uno degli esiti con cui il magistrato Dispone la Conversione, si presenta come di seguito
a seguito della compilazione e della conferma, il sistema aggiornerà la base dati e presenterà la form di Dettaglio:

Per la gestione del nuovo esito sono stati modificati anche i template SIUS_OR_GENERICAPENASOST.rtf, SIUS_OR_MODGENERICOPS.rtf.
## Scadenzario monitoraggio misure alternative espiate.
La  nuova funzione permette di ricercare per i procedimenti di Esecuzione Misura Alternativa le date inizio e fine misura, rilevandole dai dati presenti sul procedimento SIEP ad essi collegato. Ovviamente saranno esclusi dalla ricerca eventuali procedimenti di E.M.A. non collegati a procedimenti SIEP.

La funzione è presente nel menu Esecuzione Misure Alternative, in cui alle attuali funzioni è stata aggiunta la voce Ricerca Data Scadenza Procedimenti Esecuzione M.A.


Selezionandola si riceve la seguente form

In cui l’utente può:
compilare, non obbligatoriamente i campi per restringere la ricerca ad un intervallo procedimenti EMA (Anno/Numero Iniziale - Anno/Numero Finale) o ad un Intervallo Date Iscrizione (Data Iscrizione Iniziale – Data Iscrizione Finale);
selezionare, obbligatoriamente, uno dei radio button per estrarre i dati in base alla data scadenza della misura alternativa: Tutti (scaduti e non), In scadenza entro un certo tempo, In scadenza Oggi, Scaduti.
Dopo aver cliccato sul tasto Ricerca, il sistema esegue l’estrazione dei dati che soddisfino i criteri impostati e presenta l’elenco dei procedimenti impaginati (20 per pagina) e ordinati per anno e numero procedimento SIUS crescenti.

per ciascun elemento della lista è possibile selezionare il Dettaglio del procedimento SIUS o il Dettaglio del procedimento SIEP.
Da questa form è possibile generare il file Excel contenete tutti i procedimenti estratti, con gli stessi dati riportati a video.

## Gestione permessi
Per poter estrarre  nella statistica trimestrale dei permessi il dato dei permessi concessi ai detenuti condannati per i delitti previsti dall’art. 51, commi 3 bis e 3 quater c.p.p. e dei detenuti sottoposti al regime di cui all’art. 41 bis OP, è stata modificata la funzione Emissione Decreto Permesso, introducendo due nuovi check box:
Il nuovo dato non è obbligatorio, ma il sistema non permette che i due check box siano settati contemporaneamente. A seguito della compilazione e della Conferma, il sistema dopo aver aggiornato la base dati invia la form di Dettaglio

A seguito della disponibilità in base dati del nuovo dato sono state aggiornate le funzioni relative alla relazione trimestrale permessi

Nella form di presentazione del risultato dell’estrazione, sono stati contabilizzati anche il numero di permessi relativi a soggetti condannati per i delitti previsti dall’art. 51, commi 3 bis e 3 quater c.p.p. e dei detenuti sottoposti al regime di cui all’art. 41 bis OP, eliminata la colonna Esito, aggiunte le due nuove colonne relativi ai motivi/stato detenzione.

Le stesse modifiche sono state apportate anche alla stampa della relazione trimestrale.



E’ stata inoltre aggiornata la funzione Dettaglio Esecuzione Permesso con la visualizzazione del nuovo dato


## Aggiunta nuovo oggetto
Per il contenuto “Sospensione Esecuzione pene sostitutive”,  è stato aggiunto nella base dati nella tabella CG_REF_CODES per il dominio ‘MOTIVO_PROVVEDIMENTO’ il nuovo record “Sospensione pena sostituiva per arresto o fermo di condannato (art. 68 L. 689/1981)”.
## Elenco Procedimenti Assegnati
La funzione, finalizzata alla riassegnazione dei procedimenti da un magistrato all’altro, è stata modificata per ovviare alle difficoltà di gestione in caso di magistrato con elevato numero di procedimenti assegnati, che presentava  un Elenco su unica pagina, che richiedeva all’operatore un continuo scrolling per individuare i procedimenti di interesse.
La funzione modificata attivabile sempre dal menu Funzioni Amministrative » Gestione Magistrati » Elenco Procedimenti Assegnati, presenta la form

In cui l’utente indica il magistrato di cui si vuole conoscere l’Elenco dei procedimenti a suo carico, selezionandolo dalla popup che si attiva cliccando sulla cartella. A seguito della conferma il sistema invia l’Elenco impaginato dei procedimenti (20 per pagina)

Per la riassegnazione di parte o di tutti i procedimenti, la form presenta adesso le seguenti opzioni:
Spuntare i procedimenti singolarmente per pagina e Confermare;
Spuntare tutti i procedimenti di una pagina, cliccando su Selezioni tutti nella pagina e Confermare;
Spuntare tutti i procedimenti in carico al magistrato, cliccando Seleziona tutti i XX procedimenti del magistrato e Confermare.
A seguito della Conferma il sistema aggiornerà la base dati riassegnando i procedimenti indicati al nuovo magistrato, indicato nella form e presenterà l’Elenco dei procedimenti riassegnati

Inoltre in caso di numero eccessivo di procedimenti selezionati per cui il sistema potrebbe non completare l’operazione per esaurimento delle risorse allocate, al posto di un messaggio di errore di tipo tecnico non interpretabile dall’utente, è stato inserito il seguente messaggio:

## Reimpostazione dati utente e password NSC in Richiesta Certificato penale
La funzione è stata modificata per mostrare sempre nella form di richiesta i campi Userid e Password con i dati già presenti in SIES o vuoti, se al primo utilizzo, con possibilità di poterli ridigitare e quindi reimpostarli manualmente in autonomia.