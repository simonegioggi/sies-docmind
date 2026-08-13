---
uniqueName: siut-sie-mu-1-3-20200514-manuale-utente-avvocatura
displayName: "SIUT SIE MU 1 3 20200514 Manuale Utente Avvocatura SIES"
category: "GENERAL"
tags: []
---

# SIUT-SIE-MU-1.3-20200514-Manuale Utente-Avvocatura_SIES

> **File originale:** `SIUT-SIE-MU-1.3-20200514-Manuale Utente-Avvocatura_SIES.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Emma Caporizzo | Analista Programmatore |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 14/05/2020 |  |
| Livello di riservatezza | L3 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.2 | 07/04/2020 | Revisione | Integrazione intervento MEV 2019/020. |
| 1.3 | 14/05/2020 | Revisione | Revisione a seguito dei ticket n° 20200513012 e n° 20200513016:
Par. 1.1: Esplicitate le modalità di accesso al sistema tramite PST e come quest’ultimo è responsabile di tracciare il CF per passarlo in input al sistema di Consultazione;
Par. 2.1: Eliminate le diciture in cui si specificava che l’utente autenticato sul PST fosse esclusivamente un avvocato. Ciò perché il PST, in fase di autenticazione non effettua nessun controllo sul ruolo dell’utente. Inoltre sono state specificate le regole di validità generale per la consultazione sul SIUS;
Par. 3.1: Rettificati i pre-requisiti di accesso al sistema di Consultazione eleminando le diciture in cui si specificava che l’utente autenticato sul PST fosse esclusivamente un avvocato.
Il documento è stato revisionato nella sua completezza in considerazione del fatto che il PST non garantisce che l’utente autenticato sia necessariamente un avvocato. In tal senso, quindi, dove utilizzato il riferimento ad utente avvocato è stata effettuata la sostituzione con utente generico. |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Pasquale Lamattina | RTI |  | Referente Tecnico |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Fabio Mazzocchi | RTI |  | Responsabile Manutenzione Correttiva |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Fabio Gattamorta | RTI |  | PMO |
| Edoardo Lamuraglia | RTI |  | Referente qualità |
| Francesco Rosati | RTI |  | Referente qualità |


INDICE DEI CONTENUTI
1.	Introduzione	6
1.1.	Scopo del documento	6
1.2.	Glossario	6
1.2.1.	Definizioni	6
1.2.2.	Acronimi e abbreviazioni	7
2.	Avvocatura - SIES	9
2.1.	Scopo dell’applicativo	9
3.	ACCESSO Avvocatura - SIES	12
3.1.	Login	12
4.	HOME PAGE	13
5.	RICERCHE	14
5.1.	RICERCA DI PROCEDIMENTO DI SORVEGLIANZA PER ESTREMI PROCEDIMENTO	14
5.1.1.	Pagina di ricerca per estremi del procedimento	14
5.1.2.	Dettaglio Procedimento Sorveglianza	15
5.1.2.1.	Dettaglio Ordinanza	19
5.1.2.2.	Dettaglio Decreto	21
5.1.2.3.	Dettaglio Decreto di citazione (fissazione udienza)	22
5.2.	RICERCA DATI SOGGETTO	24
5.2.1.	Pagina di ricerca soggetti con procedimenti di sorveglianza	24
5.2.2.	Elenco Procedimento Soggetto	26
6.	CONSULTAZIONE	28
6.1.	CONSULTAZIONE AVVISI	28
6.1.1.	Pagina di ricerca Avvisi	28
6.1.2.	Risultato Elenco Avvisi	29

# Introduzione
## Scopo del documento
Questo documento illustra le modalità operative per l’utilizzo del sistema Avvocatura – SIES che espone le funzionalità per la consultazione dei procedimenti di Sorveglianza e degli Avvisi ad essi inerenti.
L’accesso al sistema di Consultazione Avvocatura SIUS avviene tramite il Portale dei Servizi Telematici (PST) [ex artt.6 “Portale dei servizi telematici” e 34 “Specifiche tecniche” del Decreto del Ministro delle Giustizia 21 Febbraio 2011 n. 44], il quale, a seguito di un sistema di autenticazione ‘forte’ basato su token crittografico (esempio: Smart card, chiavetta USB,...), è responsabile di tracciare il Codice Fiscale dell’utente che ha effettuato l’accesso e di passarlo in input all’applicazione in oggetto.

In base al Codice Fiscale, che è, pertanto, dato obbligatorio da acquisire in input dal sistema di autenticazione PST, per mezzo di tale sistema di Consultazione, ciascun utente potrà visualizzare le informazioni riguardanti i fascicoli SIUS per i quali risulta difensore assegnatario.

E’ bene sottolineare che ad oggi non sussiste un controllo specifico per accertare l’identità del ruolo dell’utente che fa accesso al sistema di Consultazione Avvocatura SIES. Il sistema lavora esclusivamente sul valore del Codice Fiscale, il quale è utilizzato per le ‘interrogazioni’ al SIUS. Il sistema SIUS restituisce i dati ricercati dall’utente solo se l’utente è registrato al suo interno quale avvocato attivo ed è associato come difensore ad un procedimento SIUS.
## Glossario
## Definizioni
Si premette un glossario esplicativo delle abbreviazioni e dei termini tecnici e giuridici utilizzati nel documento (Tabella - Glossario dei termini e degli acronimi usati nel documento).

| Definizione | Descrizione |
| --- | --- |
| c.p. | Codice Penale |
| c.p.p. | Codice di Procedura Penale |
| DB | Base dei dati |
| DBMS | Sistema di gestione di una base dei dati |
| DDA | Direzione Distrettuale Antimafia |
| DIB | Dibattimento |
| DPR | Decreto del Presidente della Repubblica |
| Export | Procedura di esportazione dei dati in formati predefiniti |
| Extra – Rege | Dati statistici che non vengono estratti dal Registro Generale |
| Fascicolo penale | Insieme degli atti cartacei relativi ad un procedimento penale |
| GIP | Giudice delle Indagini Preliminari |
| GUP | Giudice dell’Udienza Preliminare |
| MOD. | Modello Statistico |
| PDF XLS CSV | Formati fruibili per l’esportazione dei dati statistici |
| PM | Pubblico Ministero |
| PST | Portale dei Servizi Telematici |
| REGE | Registro Generale delle Notizie di Reato |
| Registro Ignoti | Registro dei reati ascrivibili ad ignoti |
| Registro Noti | Registro dei reati a carico di soggetti noti |
| RG | Registro Generale |


## Acronimi e abbreviazioni
| Sigla | Descrizione |
| --- | --- |
| AgID | Agenzia per l’Italia Digitale |
| API | Application Programming Interface |
| CPU | Central Processing Unit |
| CV | Curriculum Vitae |
| DB | Data Base |
| DEC | Direttore Esecutivo Contratto |
| DGSIA | Direzione Generale per i Sistemi Informativi Automatizzati |
| DR | Disaster Recovery |
| ETSI | European Telecommunications Standards Institute |
| FP | Function Point |
| GdL | Gruppo di Lavoro |
| GDPR | General Data Protection Regulation |
| HW | HardWare |
| ICT | Information & Communication Technology |
| ISO | International Organization for Standardization |
| ISP | Information Security Policy |
| IT | Information Technology |
| KPI | Key Performance Indicator |
| MAAC | MAndatory Access Control |
| MAC | MAnutenzione Correttiva |
| MEV | Manutenzione EVolutiva |
| OWASP | Open Web Application Security Project |
| PA | Pubblica Amministrazione |
| PEC | Posta Elettronica Certificata |
| PDCA | Plan, Do, Check, Act |
| PdQ | Piano della Qualità |
| PdP | Piano di Progetto |
| PdS | Piano della Sicurezza |
| PMO | Program Management Office |
| POO | Program Operating Office |
| PST | Portale dei Servizi Telematici |
| QM | Quality Manager |
| RA | Risk Assessment |
| RID | Riservatezza, Integrità, Disponibilità |
| RM | Resource Manager |
| RPO | Recovery Point Objective |
| RTO | Recovery Time Objective |
| RTI | Raggruppamento Temporaneo di Impresa |
| RUF | Responsabile Unico Fornitore |
| RUP | Responsabile Unico Progetto |
| SAL | Stato Avanzamento Lavori |
| SGQ | Sistema di Gestione per la Qualità di Engineering Ingegneria Informatica S.p.A. |
| SGSI | Sistema di Gestione della Sicurezza Informatica |
| SIU | Sistema Informativo Unitario |
| SIUS | Sistema Informativo per l'Ufficio di Sorveglianza |
| SISTEMA CONSULTAZIONE | Sistema oggetto della fornitura |
| SLA | Service Level Agreement |
| SM | Security Manager |
| SQL | Structured Query Language |
| SW | SoftWare |
| TT | Trouble Ticketing |
| UTA | Utente Generico Amministrazione |
| VPN | Virtual Private Network |



# Avvocatura - SIES
## Scopo dell’applicativo
Il Sistema di Consultazione, a cui fa riferimento il presente manuale utente, si pone come un Nuovo Servizio Telematico posto a disposizione degli utenti Avvocati.

Esso si presenta come Applicazione Web che sarà accessibile tramite la Login posta nella home page del PST (Portale Servizi Telematici).


Figura 1: Accesso tramite PST

A seguito della ‘Login’ su PST, eseguita secondo le modalità esplicitate al par. 1.1, il portale mostrerà un pulsante di accesso all’applicazione ‘Consultazione SIUS distrettuali’.

L’utilizzo di tale pulsante determina l’apertura del sistema di Consultazione Avvisi, facendo transitare dal sistema PST verso il sistema di Consultazione il Codice Fiscale dell’utente autenticato.

Il sistema di Consultazione utilizzerà l’informazione del Codice Fiscale quale discriminante per l’individuazione dei procedimenti del SIUS, pertanto il Codice Fiscale è un dato obbligatorio che il sistema di Consultazione si aspetta in input dal sistema di autenticazione PST.

Il presente documento, descrive le funzionalità inerenti la consultazione dei procedimenti della sorveglianza per i quali, l’utente che ha effettuato l’accesso, risulti difensore. L’utente, inoltre, avrà la possibilità di consultare gli Avvisi che il sistema SIUS genera in fase di validazione di un decreto di citazione (fissazione udienza) oppure al momento del deposito dell'ordinanza o del decreto.

Le ricerche saranno sempre a livello distrettuale. Infatti, a fronte di una ricerca, l’utente deve obbligatoriamente selezionare un distretto di riferimento ed, ove previsto, una sede dell'ufficio del distretto selezionato e poi proseguire con l’inserimento di ulteriori dati di ricerca.

Si rammenda che la consultazione del SIUS distrettuale è soggetta alle seguenti regole di validità generale:

L’utente richiedente deve essere abbinato al fascicolo SIUS di interesse in qualità di avvocato attivo ed, in relazione a tale abbinamento, sul SIUS deve essere censito correttamente il suo codice fiscale;

Le informazioni visibili all’utente richiedente sono relative ai seguenti atti:

Procedimenti SIUS in cui l’utente risulta difensore assegnatario, indipendentemente dallo stato del fascicolo;
Provvedimenti legati al Procedimento SIUS in cui l’utente risulta difensore assegnatario:
Decreto di fissazione udienza (anche non validato);
Decreti il cui deposito sia stato validato;
Ordinanze il cui deposito sia stato validato;
Ordinanze di Rinvio Udienza il cui deposito sia stato validato;

Gli Avvisi visibili all’utente richiedente sono relativi ai seguenti eventi:

Validazione della Fissazione Udienza;
Validazione Ordinanza di Rinvio Udienza;
Validazione del Deposito di un Decreto;
Validazione del Deposito di un’Ordinanza;
Inserimento del Ricorso;
Inserimento di un’Opposizione.

Dopo l’accesso all’applicazione, l’utente avrà a disposizione un menù di consultazione con le seguenti funzionalità:

Ricerca Estremi Procedimento
Ricerca Dati Soggetto
Consultazione Avvisi

La prima tipologia di ricerca, ovvero Ricerca Estremi Procedimento, è una ricerca basata sull’ Anno del Procedimento ed il Numero di Procedimento SIUS. All’utente che farà accesso a questa tipologia sarà prospettata una maschera in cui devono essere obbligatoriamente inseriti l’anno del procedimento, il numero di procedimento, il tipo ufficio, il distretto di interesse e la sede (quest’ultimo dato è obbligatorio solo per uffici UDS). Il risultato della ricerca sarà una pagina di dettaglio del procedimento individuato.

La seconda tipologia di ricerca ovvero Ricerca Dati Soggetto è una ricerca basata sui dati anagrafici del Soggetto.

I dati del Soggetto da valorizzare sono:
Cognome
Nome
Comune di Nascita
Stato di Nascita
Data di Nascita
Paternità
Codice CUI
Distretto

Tramite questa maschera sarà possibile anche effettuare una Ricerca Soggetto andando a valorizzare solo le Iniziali del Cognome del Soggetto.

In ogni caso, il risultato sarà un elenco di Soggetti che soddisfano i criteri di ricerca valorizzati. Dall’elenco dei soggetti poi sarà possibile accedere alla lista dei procedimenti per il soggetto selezionato e dalla lista dei procedimenti arrivare al dettaglio del decreto oppure al dettaglio dell’ordinanza.

Il menù di Consultazione Avvisi, come prima schermata, presenterà una semplice form di ricerca. I filtri proposti per la ricerca sono:

Dal - Al in riferimento alla Data Emissione
Stato Consultazione Avviso (Consultato, Non Consultato, Tutti)
Distretto

Il risultato sarà un elenco in cui saranno visualizzati tutti gli avvisi che soddisfano i filtri di ricerca. Dall’elenco sarà possibile accedere al dettaglio dell’ordinanza o decreto a cui fa riferimento l’avviso.

# ACCESSO Avvocatura - SIES
## Login
Di seguito si elencano le precondizioni per l’accesso all’applicazione di Consultazione:
L’utente che fa accesso deve essere un soggetto censito sul PST (Portale dei Servizi telematici);
L’utente censito su PST deve aver effettuato l’operazione di ‘Login’ sul PST (Portale dei Servizi telematici) secondo quanto specificato al par. 1.1;
Il sistema di autenticazione PST, in fase di accesso al Sistema di Consultazione, deve fornire, come informazione da passare nella request, il codice fiscale dell’utente loggato su PST.
Verificate tali condizioni, l’utente avrà diretto accesso alla "Home Page" del sistema centralizzato di Consultazione.



# HOME PAGE
Con il termine "Home Page" si intende il primo quadro a cui si accede appena effettuato l’accesso o tramite la pressione sul logo “Servizi Online - Sistema di Consultazione procedimenti ed avvisi Sius” presente sulla parte sinistra della barra degli strumenti.

Figura 2 – Home Page

Nella barra del titolo sulla destra è indicata, tramite link, l’utenza ed il codice fiscale con cui è avvenuto l’accesso. Cliccando sul suddetto link è possibile effettuare la Disconnessione/Logout dall’applicazione:

Figura 3 - Barra del Sistema di Consultazione ed avvisi SIUS

Con il Logout dal sistema di Consultazione, l’utente sarà ridiretto al portale dei servizi telematici.

L’Home Page si presenta con due schede principali:

Ricerche
Consultazione

In Ricerche l’utente che accede all’applicazione avrà la possibilità di consultare in tempo reale, tutti i procedimenti del sistema SIUS in cui lui risulta difensore assegnatario.
Con la Consultazione l’utente avrà la possibilità di consultare gli Avvisi che il sistema SIUS genera in fase di validazione di un decreto di citazione (fissazione udienza) oppure al momento del deposito dell'ordinanza o del decreto per un procedimento SIUS in cui lui risulta difensore assegnatario.
# RICERCHE
## RICERCA DI PROCEDIMENTO DI SORVEGLIANZA PER ESTREMI PROCEDIMENTO
Dopo essere stato autenticato sul PST, l’utente accede all’applicazione di Consultazione dei Procedimenti ed accede al menù di Ricerche Estremi Procedimento.
## Pagina di ricerca per estremi del procedimento
La maschera delle ricerche consente di individuare i procedimenti di sorveglianza associati al codice Fiscale dell’utente che ha effettuato l’accesso all’applicazione web. L’utente richiedente deve essere abbinato al fascicolo SIUS di interesse in qualità di avvocato attivo.

Figura 4 – Ricerca Procedimenti di Sorveglianza

I campi presenti nella maschera sono:
a) Anno Procedimento SIUS - Anno del Procedimento che si vuole ricercare; Obbligatorio; Numerico di 4 cifre

b) Numero Procedimento SIUS - Numero del Procedimento che si vuole ricercare; Obbligatorio; Numerico di 14 cifre;

c) Distretto – Distretti attivi; Obbligatorio; Lista di selezione contenente la lista dei distretti ‘attivi’ su cui è possibile effettuare la ricerca;

d) Tipo Ufficio - Tipo di Ufficio del Procedimento che si vuole ricercare; Obbligatorio; Lista di selezione. I possibili valori sono:
Tribunale di Sorveglianza
Ufficio di Sorveglianza

e) Sede – Indica la sede associata al tipo di ufficio ed al distretto selezionati, Obbligatoria solo per gli Uffici di Sorveglianza; Lista di selezione.

La maschera presenta i seguenti pulsanti:


Il pulsante “Cerca” avvia la ricerca del procedimento SIUS con i parametri immessi in maschera.


Il pulsante “Reset” permette di pulire i criteri per impostarne di nuovi.

## Dettaglio Procedimento Sorveglianza
Il risultato della ricerca è presentato in una maschera di dettaglio suddivisa in sezioni a scomparsa.


Figura 5 - Visualizzazione Procedimento di Sorveglianza


Cliccando sull’icona della freccia   è possibile espandere la sezione e visualizzare i dati contenuti.

Si fa presente che i dati mancanti, perché non presenti sul SIUS, saranno esposti con l’etichetta ‘-’.



SEZIONE DETTAGLIO PROCEDIMENTO
Questa sezione riporta i dati che caratterizzano il procedimento di sorveglianza.  Così come previsto delle pagine del sistema SIUS, nella maschera di dettaglio saranno visualizzati di dati relativi a:
Dati del Procedimento
Dati dell’Udienza
Dati del Soggetto
Dati dell’Atto
Dati del Titolo Esecutivo
Contenuto
Oggetto
Magistrati
Note


Figura 6 - Dettaglio Procedimento

Dalla pagina di dettaglio del procedimento, tramite l’icona ‘stampante’

è possibile avere la stampa riepilogativa del procedimento. La stampa non rappresenta un ‘atto processuale’.

SEZIONE ALTRI TITOLI ESECUTIVI
E’ la sezione che contiene il riferimento ad altri titoli esecutivi. Questa sezione al suo interno espone, ove presenti in SIUS, i dati relativi a:
N.SIEP
Data Provvedimento
Autorità Emittente
Data Irrevocabilità
Ufficio
Tipo Provvedimento
Sede Autorità
Anno/Numero Provvedimento


Figura 7- Altri Titoli Esecutivi

SEZIONE DIFENSORI
E’ la sezione che contiene i dati dei difensori. Questa sezione al suo interno esporrà:
Dati dell’Avvocato
Tipo di Difensore

Figura 8 - Difensori

SEZIONE PROVVEDIMENTI
E’ la sezione in cui vengono elencati i provvedimenti legati al procedimento SIUS individuato.
I dati mostrati sono:
Data Emissione
Tipo
Motivo
Esito
Data Depositi
Altre Informazioni
Flag Provvedimento Validato
Flag Deposito Validato

Figura 9 - Provvedimenti

Da questa sezione, cliccando sull’immagine della ‘lente’   posta in corrispondenza di ogni provvedimento, si può scegliere di richiedere il dettaglio di un decreto di citazione (vd. par.5.1.2.3), il dettaglio di un decreto (vd. par.5.1.2.2) oppure il dettaglio di un’ordinanza (vd. par.5.1.2.1).

SEZIONE ALTRI ATTI
E’ la sezione che mostra i dati relativi ad altri atti del procedimento.
Le informazioni mostrate sono:
Data Emissione
Tipo Atto
Motivo
Esito


Figura 10 - Altri Atti

SEZIONE RICHIESTE ISTRUTTORIE
E’ la sezione che mostra la lista delle richieste istruttorie.
Per ogni istruttoria sono riportate le seguenti informazioni:
Tipo atto istruttorio richiesto
Data richiesta
Destinatario
Data restituzione


Figura 11 - Richieste Istruttorie
SEZIONE MOVIMENTI UDIENZA
E’ la sezione che mostra le movimentazione inerenti ad un’udienza:


Figura 12 - Movimenti Udienza

## Dettaglio Ordinanza
In questa pagina sono visualizzati oltre che gli estremi del procedimento, i dati di dettaglio dell’Ordinanza.


Figura 13 - Pagina Dettaglio Ordinanza con sezione a scomparsa “chiusa”

La maschera è rappresentata dalla sezione a scomparsa “Dettaglio Ordinanza” e nella parte inferiore dalla sezione degli ‘Esiti’.


Figura 14 - Pagina Dettaglio Ordinanza con sezione a scomparsa “aperta”

I dati riportati sono:
Numero/Anno del procedimento
Dati del Soggetto
Data dell’udienza
Magistrato relatore
Dati del Procedimento di Riferimento (numero, oggetto, dati soggetto, data udienza)
Tipo di Ordinanza
Data di Emissione
Anno e numero Ordinanza
Data Deposito in Cancelleria
Stato del provvedimento

In fondo alla maschera è presente il pulsante ‘Torna al Procedimento’:
Tramite questo pulsante, dalla pagina di dettaglio dell’ordinanza si torna alla pagina di dettaglio del procedimento.


## Dettaglio Decreto
In questa pagina sono visualizzati oltre che gli estremi del procedimento, i dati di dettaglio del Decreto.


Figura 15 - Pagina Dettaglio Decreto con le sezioni a scomparsa ‘chiuse’


La maschera è rappresentata da sezioni a scomparsa “Dettaglio Decreto”, “Esiti” e “Difensori”.

Figura 16 - Sezione Dettaglio Decreto

I dati riportati sono:
Numero/Anno del procedimento
Dati del Soggetto
Data dell’udienza
Magistrato relatore
Data Emissione Decreto
Anno/Numero del decreto
Data del deposito in cancelleria
Stati del provvedimento
Eventuale Motivazione
Tribunale di Sorveglianza Competente
Ufficio di Sorveglianza Competente

Di seguito le schermate delle altre due sezioni:
Figura 17 - Sezione Esiti


Figura 18 - Sezione Difensori

In fondo alla maschera è presente il pulsante ‘Torna al Procedimento’:
Tramite questo pulsante, dalla pagina di dettaglio del decreto torna alla pagina di dettaglio del procedimento

## Dettaglio Decreto di citazione (fissazione udienza)
La seguente maschera viene mostrata a seguito di una richiesta di visualizzazione del dettaglio di un decreto di citazione (fissazione udienza).


Figura 19 - Maschera Dettaglio Decreto di Fissazione Udienza con sezioni a scomparsa ‘chiuse’

La maschera è rappresentata da sezioni a scomparsa “Dettaglio Decreto”, “Esiti”, “Difensori” e “Destinatari”.

Figura 20 - Sezione Dettaglio Decreto di fissazione Udienza

I dati riportati sono:
Numero/Anno del procedimento
Dati del Soggetto
Procedimento SIEP
Data dell’udienza
Magistrato relatore
Dettaglio Fissazione Udienza (Data Emissione, Data Udienza, Luogo svolgimento, Contenuto)

Di seguito le schermate delle altre tre sezioni:

Figura 21 - Sezione Esiti


Figura 22 - Sezione Difensori


Figura 23 - Sezione Destinatari

In fondo alla maschera è presente il pulsante ‘Torna al Procedimento’:
Tramite questo pulsante, dalla pagina di dettaglio del decreto di fissazione udienza si torna alla pagina di dettaglio del procedimento.

## RICERCA DATI SOGGETTO
Tramite questa funzionalità l’utente ha la possibilità di effettuare la ricerca per i dati anagrafici del soggetto o per iniziali del cognome.

## Pagina di ricerca soggetti con procedimenti di sorveglianza
La maschera delle ricerche consente di trovare i procedimenti di sorveglianza associati ad un soggetto il cui difensore è l’utente che ha effettuato l’accesso all’applicazione. L’utente richiedente deve essere abbinato al fascicolo SIUS di interesse in qualità di avvocato attivo.

La ricerca dei Soggetti con Procedimenti di Sorveglianza, può esser fatta tramite la valorizzazione dei Dati Anagrafici del Soggetto oppure specificando le sole iniziali del Cognome. Le due tipologie di ricerca sono mutuamente esclusive.

Figura 24 – Ricerca Soggetti con Procedimenti di Sorveglianza

I criteri di ricerca sono:

a) Distretto - Distretti attivi; Obbligatorio; Lista di selezione contenente la lista dei distretti ‘attivi’ su cui è possibile effettuare la ricerca;

b) Cognome – Cognome del soggetto che si vuole ricercare; Obbligatorio; lunghezza massima consentita 100 caratteri;

c) Nome – Nome del soggetto che si vuole ricercare; Obbligatorio; lunghezza massima consentita 100 caratteri;

d) Comune di Nascita - comune di Nascita del Soggetto da ricercare; Obbligatorio solo per i soggetti nati in Italia; Lista di selezione con la scelta dei comuni;

e) Stato di Nascita – stato di Nascita del Soggetto da ricercare; Obbligatorio; Lista di selezione con la scelta degli Stati;

e) Data di Nascita – Indica la data di nascita associata al soggetto da ricercare; la valorizzazione della data di nascita è obbligatoria solo per soggetti nati in Italia; campo Data.

e) Paternità – Indica il Nome del padre del Soggetto da ricercare, Facoltativa; lunghezza massima consentita 35 caratteri;

e) Codice CUI – Indica il CUI del soggetto da ricercare, Facoltativo; lunghezza massima consentita 6 caratteri;

e) Cognome (Inserire almeno 3 caratteri) – Inserire le iniziali del cognome del soggetto da ricercare, Obbligatoria solo se non presente nessun dato nell’altra sezione. E’ necessario inserire almeno 3 caratteri; lunghezza massima consentita 100 caratteri.

La maschera presenta i seguenti pulsanti:

Il pulsante “Cerca” avvia la ricerca per dati soggetto con i parametri immessi in maschera.


Il pulsante “Reset” permette di pulire i criteri per impostarne di nuovi.


## Elenco Procedimento Soggetto
Il risultato della ricerca è presentato in una maschera in cui, nella parte superiore sono riepilogati i parametri di ricerca, mentre nella parte inferiore mostra l’elenco dei soggetti trovati in base ai criteri di ricerca inseriti a sistema.

Figura 25 – Risultato della ricerca Soggetti con Procedimenti di Sorveglianza


SEZIONE SOGGETTI CON PROCEDIMENTI
Sezione dedicata alla tabella dei soggetti trovati. Per ogni soggetto, sarà specificato il cognome, nome, data di nascita, luogo di nascita e numero di fascicoli SIUS a suo carico. I campi sono in sola visualizzazione.

In fondo alla maschera è presente il pulsante ‘Torna alla Ricerca’:
Tramite questo pulsante, dalla pagina di elenco soggetti con procedimento, si torna alla pagina di ricerca per dati soggetto.

Il valore riportato in corrispondenza del campo ‘N. di fascicoli SIUS’ è un link che permette all’utente di visualizzare l’elenco dei procedimenti del soggetto.

Figura 26 - Elenco Procedimenti del soggetto

SEZIONE ELENCO PROCEDIMENTI
Sezione dedicata alla tabella dei procedimenti di sorveglianza relativi al soggetto selezionato. Per ogni procedimento, sarà specificato il numero procedimento SIUS, il contenuto, la data udienza, il provvedimento, la data di deposito, l’oggetto del provvedimento, l’esito del provvedimento e l’Ufficio/Sede.
I campi sono in sola visualizzazione.
Il valore riportato in corrispondenza del campo ‘N. SIUS’ è un link che permette all’utente di visualizzare il dettaglio del procedimento (vedi par.5.1.2).

In fondo alla maschera è presente il pulsante ‘Torna Indietro’:
Tramite questo pulsante, dalla pagina di elenco procedimenti del soggetto, si torna alla pagina di elenco soggetti con procedimento.


# CONSULTAZIONE
Cliccando sul foglio CONSULTAZIONE si accede alla sezione dedicata alla consultazione degli avvisi associati a Procedimenti SIUS il cui difensore è l’utente che ha effettuato l’accesso all’applicazione di Consultazione. L’utente richiedente deve essere abbinato al fascicolo SIUS di interesse in qualità di avvocato attivo.

## CONSULTAZIONE AVVISI
La consultazione degli avvisi è rappresentata da una maschera di ricerca in cui attraverso l’inserimento dei parametri di ricerca è possibile trovare gli avvisi da consultare.

## Pagina di ricerca Avvisi
Figura 27- Ricerca consultazione avvisi

I campi presenti nella maschera sono:
a) DAL (Data Emissione) - Data di Emissione dell’avviso da cui partire per la ricerca dell’avviso; Facoltativo; Formato Data

b) AL (Data Emissione) - Data finale di emissione da considerare per la ricerca; Facoltativo; Campo Data;

c) Stato Avviso – stato dell’avviso da ricercare; Obbligatorio; Lista di selezione. I possibili valori sono:
Tutti
Non Consultato
Consultato

c) Distretto – Distretti attivi; Obbligatorio; Lista di selezione contenente la lista dei distretti ‘attivi’ su cui è possibile effettuare la ricerca;

d) Tipo Ufficio - Tipo di Ufficio del Procedimento che si vuole ricercare; Obbligatorio; Lista di selezione. I possibili valori sono:
Tribunale di Sorveglianza
Ufficio di Sorveglianza

La maschera presenta i seguenti pulsanti:

Il pulsante “Ricerca” avvia la ricerca degli avvisi con i parametri immessi in maschera.


Il pulsante “Reset” permette di pulire i criteri per impostarne di nuovi.


## Risultato Elenco Avvisi
La pagina che segue, è la maschera di output alla ricerca di un avviso. In questa maschera sono elencati tutti gli avvisi che soddisfano i criteri di ricerca immessi.


Figura 28- Elenco Avvisi

SEZIONE ELENCO AVVISI
Sezione dedicata all’elenco degli avvisi emessi dal sistema SIUS ed estratti in base ai criteri passati in input. Per ogni avviso, sarà specificato il Tipo Provvedimento a cui fa riferimento l’avviso, il contenuto dell’avviso, l’ufficio che emette l’avviso, la data di deposito del provvedimento, il numero ed anno del procedimento SIUS, i dati del soggetto su cui è iscritto il procedimento, la data dell’udienza ed un flag che indica se l’avviso è stato già consultato o meno. Dopo aver visualizzato un Avviso, il flag Avviso Consultato passa da N a S. I campi sono in sola visualizzazione.
Il valore riportato in corrispondenza del campo ‘Tipo Provvedimento’ è un link che permette all’utente di visualizzare il dettaglio del provvedimento. In particolare, il dettaglio può far riferimento al dettaglio di un decreto di citazione (vd. par.5.1.2.3), al dettaglio di un decreto (vd. par.5.1.2.2) oppure al dettaglio di un’ordinanza (vd. par.5.1.2.1).

In fondo alla maschera è presente il pulsante ‘Torna Indietro’:
Tramite questo pulsante, dalla pagina di elenco avvisi, si torna alla pagina di ricerca avvisi.