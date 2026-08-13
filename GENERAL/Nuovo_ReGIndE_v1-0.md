---
uniqueName: nuovoregindev1-0
displayName: "Nuovo ReGIndE v1 0"
category: "GENERAL"
tags: []
---

# Nuovo_ReGIndE_v1.0

> **File originale:** `MEV/SCHEDA_021/materiale analisi/documentazione_reginde/Nuovo_ReGIndE_v1.0.pdf`  
> **Tipo:** PDF

---

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
Sommario 
 
1 
SCOPO DEL REGINDE ................................................................... 2 
2 
FLUSSI DI ALIMENTAZIONE DEL REGINDE ................................. 3 
2.1 CENSIMENTO DEGLI ENTI CHE INVIANO ALBI ................................................ 6 
2.2 INVIO DELL’ALBO ................................................................................. 6 
2.3 PROFESSIONISTI NON ISCRITTI AD ALCUN ALBO ............................................ 6 
2.4 FORMATO MESSAGGIO DI RICHIESTA .......................................................... 7 
2.5 STRUTTURA XML DI COMUNICAZIONE DELL’ALBO ........................................... 8 
2.6 STRUTTURA XML DI ESITO DI INVIO DELL’ALBO ........................................... 10 
3 
GESTIONE DELLA FASE TRANSITORIA ....................................... 13 
4 
WEB SERVICE ESPOSTI .............................................................. 15 
5 
STRUTTURA DATI ....................................................................... 17

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
1 Scopo del ReGIndE 
Lo scopo principale del ReGIndE è quello di censire ed abilitare i soggetti esterni che 
intendono operare nel contesto del Processo Telematico 
I flussi informativi possono essere riassunti in: 
1. scambi documentali (deposito atti, ricezione notificazioni/comunicazioni di 
cancelleria, copie di atti); 
2. consultazione dei sistemi di gestione dei registri. 
Le operazioni di cui al punto 1. sono permesse solo ai soggetti censiti nel contesto del 
ReGIndE; in particolare gli scambi documentali sono consentiti ai soggetti nel cui 
profilo informativo è presente l‟indicazione della casella di Posta Elettronica 
Certificata (PEC). Nel caso la tipologia del profilo sia quella di avvocato oltre alla 
casella di PEC dovrà essere verificato lo “status” attivo del soggetto.  
Le consultazioni dei registri (punto 2.) sono permesse a tutti i soggetti che accedono 
all‟area privata del portale tramite smart card, la presenza o meno del soggetto 
nell‟anagrafica del ReGIndE e le caratteristiche del profilo censito sono le 
informazioni che permettono al portale di discriminare la tipologia di accesso alle 
informazioni (ad esempio consultazioni con profilo di avvocato se così censito sul 
ReGIndE o con profilo di parte in causa se non censito sul ReGIndE). 
Nel seguito saranno dettagliati i flussi di alimentazione del ReGIndE nonché tutte le 
informazioni coinvolte nella sua gestione, le modalità di consultazione dello stesso, i 
soggetti abilitati a farlo e la progettazione tecnica del modulo; infine, si farà cenno 
alle modalità operative previste per la gestione della fase di coesistenza tra l‟attuale 
ReGIndE (integrato nel contesto del Gestore Centrale) e quello definito e progettato in 
questa sede.

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
2 Flussi di alimentazione del ReGIndE 
Nel contesto della Figura 1 sono illustrate le tre macro categorie di soggetti il cui 
profilo anagrafico va ad alimentare il ReGIndE ed in particolare: 
1. i soggetti appartenenti ad un ente pubblico (ad esempio avvocati e funzionari 
dell‟INPS e dell‟avvocatura di stato); 
2. i professionisti iscritti in albi ed elenchi istituiti con legge dello Stato (ad esempio 
consiglio dell‟ordine degli avvocati di Milano o consiglio nazionale del 
Notariato); 
3. i professionisti effettivamente non iscritti ad alcun albo, o il cui ordine di categoria 
non abbia provveduto ad inviare la copia dell‟albo al Ministero della Giustizia. 
Nel seguito della trattazione le tre macrocategorie di appartenenza dei soggetti sopra 
elencate saranno genericamente definite come “enti”; con ente si intende identificare 
anche la categoria espressa al punto 3 in quanto concettualmente mappato in un “ente 
fittizio” che cataloga, appunto, i professionisti non iscritti ad alcun albo. In questo 
modo è possibile uniformare e semplificare la modalità di alimentazione del 
ReGIndE. Per maggior chiarezza è opportuno sottolineare che, nel seguito del 
documento, quando si farà riferimento all‟albo di un ente si intenderà anche quello 
dell‟ente fittizio, salvo sia specificato diversamente. 
In Figura 1 sono stati evidenziati anche i sistemi interni al dominio giustizia che 
utilizzano il ReGIndE in consultazione al fine di definire politiche di controllo e 
sicurezza sulle funzionalità da essi esposti. Ad esempio il front end di PolisWeb, 
ospitato sul Portale, utilizza le informazioni del registro per definire il profilo di 
consultazione dell‟utente collegato.  
Infine si sono volutamente evidenziati in figura quei registri disponibili alle PP.AA,  il 
cui contenuto occorre ai sistemi del dominio Giustizia, ovvero il registro delle 
imprese, delle pubbliche amministrazioni e dei cittadini; da tali registri potranno 
essere recuperati gli indirizzi di PEC e CEC-PAC rispettivamente delle imprese e dei 
cittadini ivi censiti. 
Si sottolinea che il ReGIndE non gestirà informazioni già presenti in tali registri.     
Nel seguito del paragrafo sono descritte le caratteristiche di alimentazione del 
ReGIndE da parte degli enti coinvolti che si ricorda essere enti pubblici, ordini di 
categoria e l‟ente fittizio attraverso il quale operano i professionisti non iscritti ad un 
albo o i cui dati non sono stati inviati dall‟albo di categoria di appartenenza.

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
 
Figura 1 – Flussi di alimentazione del ReGIndE e attori coinvolti 
 
Per tutti gli invii si prevede un‟unica modalità, la PEC inviata ad una casella creata ad 
hoc dal Ministero della Giustizia nel contesto del proprio dominio di posta elettronica 
certificata, giustiziacert.it. Le informazioni che alimentano il ReGIndE sono inviate in 
formato strutturato definito da uno specifico XSD descritto nel seguito della 
trattazione al paragrafo 2.5. 
L‟esito dei controlli delle informazioni inviate al ReGIndE vengono inviate dal 
Portale all‟indirizzo del mittente attraverso lo stesso mezzo. L‟esito è anch‟esso un 
file XML in allegato, il cui formato strutturato è definito da uno specifico XSD 
descritto al paragrafo 2.6. L‟esito si riferisce sia ad errori presenti sui dati e, quindi, 
riconducibili alle informazioni dei singoli soggetti (come ad esempio codice fiscale 
inesistente), sia ad errori legati a vincoli e prerequisiti che presuppongono la validità 
dell‟invio di un albo (ad esempio: censimento dell‟ente richiedente e dei soggetti 
abilitati all‟invio dell‟albo). Al capitolo 2.4 sono descritte le regole che il messaggio 
di richiesta deve rispettare per essere correttamente elaborato dal sistema. 
Il flusso di alimentazione del ReGIndE è descritto nelle sue fasi costituenti nei 
diagrammi di attività delle due figure successive, ogni fase e le implicazioni tecniche 
in essa coinvolte saranno descritte in dettaglio nei futuri paragrafi. Si sottolinea che le 
operazioni indicate nella prima swimlane sono svolte da tutti gli enti tranne l‟ente 
fittizio che, in quanto fittizio, non invia i suoi dati in maniera massiva ma si popola 
all‟interno del ReGIndE grazie alle singole iscrizione dei professionisti non iscritti ad 
alcun albo o comunque per i quali l‟ente di appartenenza non provvede all‟invio 
dell‟intero albo. 
Dominio Giustizia
Punto di 
accesso
Gestore
dei servizi
telematici
Registro Generale degli 
Indirizzi Elettronici
(ReGIndE)
Professionista
Non iscritto ad un albo
Portale dei
servizi telematici
Registrazione
Registrazione
Cittadino
(CEC-PAC)
Elenco 
consultabile 
dalle PPAA
Registro 
delle imprese
Impresa
Ente
pubblico
Professionista
Iscritto ad un albo
Ordine
1
3
2

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
L‟invio dell‟albo da parte di un ente deve essere proceduto da una fase di 
“censimento” dell‟ente che coinvolge l‟Amministrazione.  
Durante tale fase, descritta nel prossimo paragrafo, è compito dell‟ente inviare 
all‟Amministrazione i dati necessari al suo censimento nel contesto del registro. La 
Figura 2 descrive graficamente il flusso caratterizzante il censimento. 
ReGIndE
Amministrazione
Ente (non fittizio)
Invio Dati Anagrafici Ente
Verifica Dati Ente
Registrazione Dati Ente
Invio Conferma registrazione
 
Figura 2 - Flusso censimento 
Sarà onere dell‟Amministrazione, previa definizione dei tempi e delle modalità 
tecniche di verifica dei dati inviati dall‟ente, provvedere alla registrazione in 
anagrafica e a dare conferma all‟ente richiedente. 
Terminata la fase di “censimento”, l‟ente è pronto per l‟invio dei dati dell‟albo di 
competenza presso il registro come esemplificato dal diagramma di flusso seguente. 
ReGIndE
Ente (non fittizio)
Invio Dati Albo
Elaborazione
Invio Esito
[ente censito] 
[ente non cesito] 
 
Figura 3 - Flusso alimentazione

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
2.1 Censimento degli enti che inviano albi 
L‟ente che intende abilitare ai servizi del processo telematico i soggetti ad esso 
afferenti, deve inviare preventivamente all‟Amministrazione un documento di 
censimento delle informazioni necessarie ad identificare: 
 l‟ente che richiede di inserire i soggetti a lui afferenti per l‟utilizzo dei servizi 
telematici, attraverso codice ente, descrizione, codice fiscale/partita iva; 
 il nominativo del delegato all‟invio dell‟albo (codice fiscale) che dovrà firmare 
digitalmente l‟albo in trasmissione; se l‟ente richiedente è un ente fittizio, tale 
informazione non è richiesta; 
 la casella di PEC utilizzata per l‟invio dell‟albo. 
Tali informazioni verranno registrate sulla base dati che implementa il ReGIndE dagli 
amministratori di sistema del CMS del Portale attraverso apposite maschere, a seguito 
di tali registrazioni sarà possibile per l‟ente inviare l‟albo.  
2.2 Invio dell’albo 
L‟albo viene inviato come allegato, nel formato ComunicazioniSoggetti.xml descritto 
nel contesto del paragrafo 2.5, attraverso la PEC comunicata dall‟Ente in fase di 
censimento dello stesso. Il Portale provvede ad effettuare i controlli in merito alla 
validazione dell‟ente mittente e del firmatario, se tali controlli sono superati con 
successo, procede all‟elaborazione del file allegato.  
Ad ogni invio corrisponde una risposta tramite PEC (reply alla mail di invio) 
contenente in allegato l‟esito dell‟elaborazione del messaggio con le eventuali 
eccezioni; il formato del messaggio di esito, inviato come allegato al messaggio di 
PEC,  è descritto nel contesto del paragrafo 2.6. 
Ad ogni nuovo indirizzo di PEC registrato nelle anagrafiche a seguito 
dell‟inserimento di un nuovo soggetto o di modifica di uno esistente, verrà inviato un 
messaggio di PEC di cortesia in cui si attesta l‟avvenuta registrazione. 
2.3 Professionisti non iscritti ad alcun albo 
Per professionisti non iscritti all‟albo si intende tutti quei soggetti nominati dal 
giudice come consulenti tecnici d‟ufficio o più in generale ausiliari del giudice non 
appartenenti ad un ordine di categoria o che appartengono ad ente/ordine 
professionale che non ha ancora inviato l‟albo al Ministero della Giustizia. 
I professionisti della suddetta categoria si registrano al ReGIndE attraverso un Punto 
di Accesso o direttamente attraverso il Portale dei Servizi Telematici. 
Nel caso in cui sia il PdA a trasmettere l‟avvenuta registrazione di un ausiliario del 
giudice, provvederà attraverso il medesimo file ComunicazioniSoggetti.xml utilizzato 
dagli ordini professionali. Tale file dovrà essere firmato digitalmente e inviato via 
PEC, i dati del firmatario e la casella di PEC abilitati all‟invio dell‟albo dovranno 
essere censiti al pari dei dati degli enti e saranno mappati sull‟unico ente fittizio.  
È importante sottolineare che da tali indirizzi non sarà possibile attivare l‟operazione 
di invio dell‟intero albo ma solo inserimenti, modifiche e cancellazioni. Tale vincolo 
permette di evitare che un singolo PdA cancelli o sostituisca i dati dell‟intero ente 
fittizio i cui soggetti sono inviati da più mittenti diversi.  Ad esempio, se ipotizziamo

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
di codificare l‟ente fittizio con il codice “99999”, tutti i soggetti inviati dai PdA di 
Milano e Bologna avranno come ente di appartenenza il codice “99999”. Se il PdA di 
Verona, che vuole iscrivere i suoi professionisti, inviasse la comunicazione dei 
soggetti con l‟opzione di intero albo l‟intero albo dell‟ente fittizio, verrebbe sostituito 
con i soli dati di Verona con evidente perdita di informazioni dei PdA Milano e di 
Bologna. 
Nel caso l‟iscrizione del soggetto venga fatta dal soggetto stesso, attraverso il Portale, 
sarà resa disponibile, nell‟area privata accessibile con smart card, una maschera da 
compilare con i dati necessari al ReGIndE; verrà inoltre richiesto l‟upload del file che 
contiene l‟incarico di nomina da parte del giudice firmato digitalmente dal soggetto 
che intende iscriversi. Il submit dei dati da tale maschera attiverà la procedura di 
iscrizione del soggetto nel ReGIndE come appartenente all‟ente fittizio. Si sottolinea 
che la form di registrazione presenterà il campo codice fiscale non modificabile e 
precompilato con quello estratto dalla smart card utilizzata dal soggetto per 
l‟autenticazione all‟area privata.  
Si sottolinea infine che nel caso un soggetto non appartenente ad albo ma censito sul 
ReGIndE si iscriva successivamente ad un albo, e il suo ordine ne invii copia, prevale 
l‟albo, quindi il Portale cancella l‟occorrenza precedente ed invia un messaggio di 
PEC di cortesia al professionista. 
2.4 Formato messaggio di richiesta 
Il messaggio attraverso il quale vengono veicolate le richieste, deve aderire alle 
seguenti specifiche di formato: 
 il messaggio deve essere una e-mail di posta elettronica certificata, non saranno 
considerati i messaggi di posta ordinaria inviati alla casella di PEC deputata a 
ricevere gli albi. 
 L‟indirizzo di PEC mittente deve essere censito tra quelli delegati all‟invio. 
 Deve essere allegato un solo file e tale file deve essere firmato digitalmente nel 
caso l‟ente non sia fittizio. 
Il mancato rispetto di uno o più dei vincoli di cui sopra produrrà un messaggio 
automatico di esito negativo e non sarà innescata la fase di trattamento dell‟allegato 
ComunicazioniSoggetti.xml.  
L‟allegato suddetto deve rispettare i seguenti vincoli: 
 il codice ente specificato nel contesto dell‟allegato deve essere censito tra quelli 
noti al Portale. 
 Il mittente della mail deve essere censito secondo un criterio di corrispondenza tra 
ente e indirizzo stesso della PEC. 
 La firma digitale deve appartenere a un delegato censito secondo un criterio di 
corrispondenza tra delegato (suo codice fiscale)  ed ente per conto del quale sta 
inviando l‟albo. 
 Il file deve essere validato rispetto al relativo XSD di cui al paragrafo 2.5. 
Il mancato rispetto di uno o più dei vincoli di cui sopra produrrà un messaggio 
automatico di esito negativo e non sarà innescata la fase di trattamento dell‟allegato 
ComunicazioniSoggetti.xml. Si precisa che non vi sono vincoli sull‟oggetto né sul 
body del messaggio, che non vengono quindi considerati nell‟elaborazione.

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
Il formato del messaggio di PEC contenente il dettaglio dell‟eccezione avverrà tramite 
l‟allegato denominato Esiti.xml conforme allo schema descritto al paragrafo 2.6. Il 
messaggio di PEC contenente l‟esito, essendo in risposta al messaggio di invio albo,  
avrà come oggetto  la medesima descrizione del messaggio originale con il suffisso “– 
Esito”. 
2.5 Struttura xml di comunicazione dell’albo 
Il file ComunicazioniSoggetti.xml, è il documento che definisce le informazioni 
strutturate per il censimento dei soggetti cui è permessa l‟attivazione dei flussi 
informativi con il dominio Giustizia. Tale file si basa sul file XML-Schema 
ComunicazioniSoggetti.xsd illustrato in Figura 4.

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
 
Figura 4 - ComunicazioniSoggetti.xsd 
Di seguito la descrizione degli elementi più significativi costituenti la struttura del file 
di comunicazione soggetti. 
Ente mittente: indica il codice identificativo dell'ente mittente, cioè dell‟ente che 
invierà l‟albo. Per gli avvocati iscritti ad un Consiglio dell'Ordine il codice dell'ente 
sarà rappresentato da una stringa data dal prefisso COA, al quale viene aggiunto il 
codice Istat del comune di riferimento del consiglio dell‟ordine stesso. Per tutti gli 
altri enti il codice identificativo sarà rappresentato dalla partita IVA dell'ente. 
Comunicazione intero albo: se valorizzata a true, la comunicazione si intende 
relativa all'intero albo, altrimenti la comunicazione è da intendersi come integrazione

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
di comunicazioni precedenti. Quando l‟invio interessa l‟intero albo, il sistema 
effettuerà prima la cancellazione di tutti i soggetti afferenti all‟ente, e 
successivamente provvederà con l‟inserimento dei soggetti contenuti nel documento 
inviato. Sara garantita l‟atomicità dell‟intera transazione (cancellazione e successivo 
inserimento).  
Comunicazione soggetti: lista dei soggetti interessati dalla comunicazione; 
Operazione richiesta: indica il tipo di operazione inerente il soggetto rispetto al 
ReGIndE; è un tipo enumerato che può assumere i seguenti valori: 
 inserimento: trattasi di un nuovo soggetto da censire nel ReGIndE (valore di 
default); 
 cancellazione: trattasi di una cancellazione di un soggetto già censito nel registro 
degli indirizzi; 
 modifica: trattasi di una modifica di un soggetto censito nel ReGIndE, si sottolinea 
che l‟operazione di modifica implica di fatto l‟eliminazione e il reinserimento dei 
dati del soggetto, non saranno effettuate mai operazioni di modifica “per 
differenza” dei dati di profilo. 
L'elemento viene ignorato se "ComunicazioneInteroAlbo" risulta pari a true. 
Ruolo: indica la posizione che il professionista riveste nel contesto del Processo 
Telematico, anche in questo caso si tratta di un tipo enumerato i cui valori sono: 
 Avvocato. 
 Avvocato Ente Pubblico: è la posizione rivestita dall‟avvocato di una Pubblica 
Amministrazione. 
 Funzionario Ente Pubblico: è la posizione rivestita dal funzionario di una Pubblica 
Amministrazione. 
 Altro Professionista: tutte le categorie di professionisti che operano genericamente 
come ausiliari del giudice. 
Verrà quindi indicato anche lo stato che potrà valere uno dei seguenti valori: 
 attivo; 
 radiato; 
 sospeso; 
 cancellato. 
2.6 Struttura xml di esito di invio dell’albo 
Il risultato dell‟elaborazione del file ComunicazioniSoggetti.xml, viene inviato dal 
Portale all‟ente richiedente attraverso un messaggio di PEC con allegato il file 
Esiti.xml. Tale file si basa sul file XML-Schema Esiti.xsd indicato nella figura 
seguente.

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
 
Figura 5 - XML Schema Esiti.xsd 
Di seguito la descrizione degli elementi più significativi costituenti la struttura del file 
di esito: 
Id Messaggio Mittente: è l‟elemento che contiene l'identificativo del messaggio di 
PEC il cui allegato è il file ComunicazioniSoggetti.xml; 
Ente Destinatario: codice dell‟ente destinatario del messaggio di PEC di risposta alla 
comunicazione invio albo; 
Esito Comunicazione: indica l'esito dell'elaborazione di una comunicazione di 
inserimento soggetti non andata a buon fine.  Viene valorizzato solo nel caso in cui un 
intero file di ComunicazioniSoggetti.xml non è stato elaborato. Il codice dell‟errore è 
caratterizzato dal tipo enumerato CodiceEsitoSoggetto; ad esempio nel caso di 
mancata validazione del file xml il contenuto dell‟elemento riporterà la descrizione 
dell‟errore specifico. I codici errori previsti dal tipo EsitoComunicazioneType sono i 
seguenti: 
 F001 
Firmatario non autorizzato. 
 F002 
Indirizzo mittente di PEC non autorizzato. 
 F003 
Errore file non conforme allo schema. 
 F004 
Ente non autorizzato all‟invio dell‟intero albo. 
 F005 
Formato messaggio non conforme. 
 F999 
Errore generico del sistema. 
Esiti Soggetti: specifica per ogni soggetto del file di ComunicazioniSoggetti.xml 
l'esito della comunicazione; il codice dell‟errore viene indicato nell‟attributo Codice 
Esito Soggetto che indica l‟esito dell‟operazione richiesta per ciascun soggetto; 
l‟esito 
è 
caratterizzato 
da 
un 
codice 
appartenente 
al 
tipo 
enumerato 
EsitoSoggettoType; la semantica utilizzata per questa tipologia di esito prevede il 
carattere “S” come iniziale per i gli esiti positivi, “W” per i messaggi di warning e “E” 
per gli errori. 
 S000 
Operazione eseguita correttamente.

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
 W001  
Inserimento soggetto già presente in altro ente, il soggetto è stato  
 
 
legato anche al nuovo ente ma il suo profilo anagrafico non è stato  
 
 
modificato, per quest‟ultima operazione è necessaria una richiesta  
 
 
esplicita di modifica. 
 E001 
PEC soggetto non valida. 
 E002 
Dati anagrafici del soggetto non validi. 
 
 E003 
Impossibile inserire il soggetto in quanto già presente nell‟ente  
 
 
mittente. 
 E004 
Impossibile cancellare il soggetto in quanto non presente nell‟ente  
 
 
mittente. 
 E005 
Impossibile modificare i dati del soggetto in quanto non presente  
 
 
nell‟ente mittente. 
 E999 
Errore generico durante l‟operazione. 
Al fine di rendere immediatamente evidenti al destinatario del messaggio di PEC le 
eventuali eccezioni, nel body del messaggio stesso saranno inserite le stesse 
informazioni di dettaglio riportate nell‟allegato Esito.xml, limitatamente agli esiti 
negativi.

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
3 Gestione della fase transitoria 
La figura illustra la situazione attuale (parte bassa) e la situazione nuova (parte alta): 
 
Figura 6 – Gestione fare transitoria 
Per “fase transitoria” si intende la coesistenza della situazione attuale (flussi di 
trasmissione via PdA/CPECPT) con la situazione nuova (flussi di trasmissione via 
PEC). 
L‟obiettivo primario della fase transitoria è quello di evitare qualsiasi discontinuità 
nell‟invio delle comunicazioni/notificazioni telematiche a valore legale (ex art. 51 del 
decreto-legge 25 giugno 2008, n. 112, convertito con modificazioni, dalla legge 6 
agosto 2008, n. 133), che interessano circa 10.000 avvocati (in aumento); in altre 
parole, l‟avvocato che attualmente riceve le comunicazioni attraverso la CPECPT, le 
riceverà nella sua casella PEC non appena questa sarà inserita nel nuovo ReGIndE. 
Lo “switch-off” interessa il singolo professionista: il suo ordine invierà l‟XML con 
l‟indirizzo di PEC al Portale e non appena sarà aggiornato il nuovo ReGIndE, il 
Gestore Locale: 
a) invierà comunicazioni/notificazioni solo alla PEC, quindi il nuovo ReGIndE 
prevarrà sull‟attuale; 
b) consentirà la ricezione di atti solo tramite PEC, pertanto se verrà utilizzato 
l‟attuale flusso via PdA, il deposito sarà rifiutato; 
In merito alle consultazioni a seguito della registrazione di un soggetto sul ReGIndE 
sarà possibile per il soggetto stesso utilizzare le funzioni di consultazione messe a 
Dominio Giustizia
Punto di 
accesso
Professionisti
iscritti ad albi
Gestore
Centrale
Attuale
ReGIndE
Nuovo
ReGIndE
(PEC)
Albo
Gestore
locale
@GiustiziaCert
Gestore di PEC
soggetto esterno
Nuovo
Attuale
Dati soggetto
Status (difensore)
ID PdA
CPECPT
Dati soggetto
Status (difensore)
PEC
Soggetto
abilitato
esterno
Punto di 
accesso
Professionisti
non iscritti ad albi

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
disposizione dal Portale dei Servizi Telematici sia attraverso la nuova interfaccia in 
esso integrata sia attraverso i proxy messi a disposizione dei PdA o dei software di 
studio. 
Appena sarà attivo sul nuovo ReGIndE, il Portale invierà un messaggio di PEC al 
professionista interessato, comunicandogli l‟avvenuta attivazione e che dovrà usare il 
solo canale PEC per invii e ricezioni. Il Portale invierà inoltre un messaggio di PEC 
alla casella di servizio del PdA (ove la stessa risulti registrata sul catalogo dei PdA, al 
fine di mettere nelle condizioni il PdA stesso di avvisare l‟utente che dovrà utilizzare 
esclusivamente il nuovo canale della PEC per le ricezioni e gli invii documentali. Il 
Portale utilizzerà le informazioni presenti sull‟attuale ReGIndE (integrato nel Gestore 
Centrale) per risalire dal codice fiscale del soggetto al PdA su cui il soggetto stesso è 
censito. 
È stata scartata l‟ipotesi di obbligare l‟ordine ad inviare una cancellazione sull‟attuale 
ReGIndE prima del‟invio dell‟inserimento sul nuovo perché comporta un “buco 
temporale” per l‟avvocato che deve ricevere comunicazioni/notificazioni solo in 
forma telematica. 
Prerequisito della fase transitoria è l‟installazione del GL-PEC su tutti i distretti già 
telematici: tutti debbono essere infatti pronti a ricevere/inviare PEC dal momento in 
cui si avvia la fase di transizione.

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
4 Web service esposti 
I web service esposti risolvono le interrogazioni previste dai requisiti identificati in 
analisi e permettono di ottenere informazioni sulle due entità principali mantenute 
nelle anagrafiche e cioè enti e soggetti abilitati. 
I web service saranno messi a disposizione in prima istanza dei Gestori Locali, dei 
Punti di Accesso e del front-end del Portale.  
La figura seguente diagramma le classi responsabili dell‟implementazione dei servizi 
di interrogazione. 
 
«SessionBean»
ServiziInterrogazioneEnteBean
«interfaccia»
Interrogazioni::ServiziInterrogazioneEnte
«SessionBean»
ServiziInterrogazioneSoggettoBean
«interfaccia»
Interrogazioni::ServiziInterrogazioneSoggetto
 
Figura 7 - Web Service di interrogazione 
 
 ServiziInterrogazioneEnte, interfaccia che modella il web service per 
l‟interrogazione degli enti definiti nel registro; 
 
Metodo 
Descrizione 
dettagliEnte( 
  String codiceEnte 
):Ente 
Restituisce i dettagli dell’ente 
identificato dal codice passato come 
parametro. 
ricercaEnte( 
  String descrizione 
):Ente[] 
Restituisce la lista degli enti che 
corrispondono ai criteri di ricerca 
specificati. 
La descrizione può contenere caratteri 
jolly (*,?) e nel caso i criteri di 
ricerca identifichino un numero di enti 
superiore ad un limite configurabile il 
servizio restituirà eccezione invitando 
il chiamante a restringere i criteri di 
ricerca. 
 
 ServiziInterrogazioneEnteBean, implementazione dei servizi di interrogazione; 
 ServiziInterrogazioneSoggetto, interfaccia che modella il web service per 
l‟interrogazione dei soggetti; 
 
Metodo 
Descrizione 
dettagliSoggettoPerCodice( 
  String codiceFiscale 
):Soggetto 
Restituisce i dettagli del soggetto 
identificato dal codice fiscale passato 
come parametro. 
dettagliSoggettoPerIndirizzo( 
  String indirizzo 
):Soggetto 
Restituisce i dettagli del soggetto 
identificato dall’indirizzo di PEC 
passato come parametro.

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
ricercaSoggetto( 
  String cognome, 
  String codiceEnte 
):Soggetto[] 
Restituisce la lista dei soggetti che 
rispondono ai criteri di ricerca 
specificati. 
Il cognome può contenere caratteri jolly 
(*,?) mentre il codice dell’ente e’ 
opzionale. 
Nel caso i criteri di ricerca 
identifichino un numero di soggetti 
superiore ad un limite configurabile il 
servizio restituirà eccezione invitando 
il chiamante a restringere i criteri di 
ricerca. 
elencoPaginatoSoggetti ( 
  int da, 
  int count 
):Soggetto[] 
Restituisce la lista dei soggetti 
memorizzati nel registro a partire 
dall’entrata indicata nel parametro ‘da’. 
La posizione dell’entrata è stabilita 
lato registro attraverso l’ordine di 
memorizzazione del RDBMS in utilizzo. 
È altresì importante sottolineare che il 
servizio è orientato prettamente ai 
sistemi del dominio Giustizia. 
isMembroDi( 
  String codiceFiscale, 
  String codiceEnte 
):String 
Verifica se il soggetto specificato dal 
codice fiscale è membro dell’ente 
identificato dal codice passato come 
parametro. 
In caso di successo ritorna la funzione 
rivestita dal soggetto nel contesto 
dell’ente, null altrimenti. 
 
 ServiziInterrogazioneSoggettoBean, implementazione dei servizi di ricerca 
anagrafica dei soggetti. 
Nella descrizione dei servizi sopra elencati il tipo Soggetto rappresenta l‟insieme delle 
informazioni mantenute dall‟entità „Soggetti‟, „Indirizzi‟, „Enti‟, „Ruoli‟ e „Status‟ 
descritte al paragrafo successivo. Si noti che non state inserite le informazioni 
contenute nell‟entità „IndirizziAbilitati‟ perché utili solo alla gestione dei flussi di 
manutenzione del registro.

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
5 Struttura dati 
Le informazioni gestite dal ReGIndE sono modellate nel contesto di una base dati che 
oltre ha contenere le informazioni di profilo del soggetto censito in tale registro 
contengono anche informazioni di configurazione e di servizio necessarie alla 
gestione applicativa del ReGIndE quali ad esempio i dati di censimento degli enti. 
Considerata la dimensione dello schema in termini di entità, relazioni e numero di 
attributi per ogni entità si è scelto di schematizzare la base dati attraverso l‟utilizzo di 
un formalismo E/R non direttamente riconducibile ad uno schema concettuale o 
logico ma una versione intermedia di entrambi. Si è scelto infatti di eliminare le 
gerarchie e le associazioni N:M in modo che tutte e sole le entità presenti siano 
traducibili in tabelle dello schema fisico. Nello schema sono inoltre presenti 
opportune tabelle per la transcodifica e per la gestione delle problematiche di 
storicizzazione.   
 
Figura 8 – Modellazione dello schema DB del ReGIndE 
 ENTI: censisce tutti gli enti istituzionali che possono interagire con il ReGIndE, 
come ad esempio i Consigli dell‟Ordine di categoria. Nel contesto di questa entità 
viene censito (preconfigurato) anche l‟unico ente fittizio a cui afferiscono tutti i 
professionisti non appartenenti ad un ente (albo di categoria) o per i quali l‟ente di 
appartenenza non invia al Ministero della Giustizia l‟elenco dei suoi iscritti.   
 SOGGETTI: è l‟entità che modella i professionisti censiti nel ReGIndE. 
 INDIRIZZI: modella le informazioni legate all‟indirizzo; un soggetto deve avere 
almeno l‟indirizzo del Domicilio Legale. l‟attributo TIPO INDIRIZZO specializza 
la tipologia dell‟indirizzo codificato nella riga: R (indirizzo di residenza) e D 
(domicilio legale). Deve esistere almeno un indirizzo riferito al domicilio legale. 
Enti
Identificativo Ente
Codice
Descrizione
Codice Fiscale
Partita Iva
Variable characters (32)
Variable characters (50)
Variable characters (256)
Variable characters (16)
Variable characters (11)
<M>
<M>
<M>
Soggetti
Identificativo Soggetto
Nome
Cognome
Data di Nascita
Luogo di Nascita
Provincia di Nascita
Codice Fiscale
Pec
Variable characters (32)
Variable characters (256)
Variable characters (256)
Date
Variable characters (256)
Variable characters (4)
Variable characters (16)
Variable characters (256)
<M>
<M>
<M>
<M>
Indirizzi
Identificativo Indirizzo
Indirizzo
Cap
Comune
Provincia
Telefono
Fax
Email
Variable characters (32)
Variable characters (1000)
Variable characters (5)
Variable characters (256)
Variable characters (4)
Number (15)
Number (15)
Variable characters (256)
<M>
<M>
<M>
<M>
Indirizzi Abilitati
Identificativo PEC abiljtata
Pec
Codice Fiscale Firmatario
Variable characters (32)
Variable characters (256)
Variable characters (16)
<M>
<M>
<M>
Soggetti per Ente
Identificativo Soggetto Ente
Variable characters (32) <M>
Status
Identificativo Stato
Descrizione Stato
Integer
Variable characters (50)
<M>
<M>
Ruoli
Identificativo Ruolo
Descrizione Ruolo
Integer
Variable characters (50)
<M>
<M>
Storico Soggetti
Identificato Storico Soggeto
Data Evento
Variable characters (32)
Date & Time
<M>
<M>

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
 INDIRIZZI ABILITATI: è l‟entità che censisce gli indirizzi di PEC abilitati 
all‟invio dell‟albo e le firme che nel certificano la validità. 
 SOGGETTI PER ENTE: è la tabella di relazione che permette allo schema DB 
di gestire le situazioni in cui un soggetto appartiene a più ENTI e nel contesto di 
ognuno può avere status e ruoli differenti. Tale modellazione avviene attraverso le 
relazioni obbligatorie con SOGGETTI, ENTI, RUOLI e STATUS. Si specifica 
inoltre  che tale entità rappresenta la “fotografia” della situazione attuale valida di 
ogni soggetto. Si sottolinea che non saranno implementate logiche di congruenza 
tra ruolo e ente ovvero un ruolo “avvocato” può essere legato ad un ordine di 
categoria diverso da un consiglio dell‟ordine di avvocati, la base dati si limita 
infatti a rendere persistenti le informazioni inviate al ReGIndE ma non entra nel 
merito delle stesse.  
 RUOLI: tabella di transcodifica, l‟elenco dei valori è “avvocato”, “avvocato ente 
pubblico”, “funzionario ente pubblico”, “altro professionista”. Un ruolo può 
essere censito nella tabella ma non ancora assegnato ad alcun soggetto censito nel 
RegIndE (nessun ente tra quelli memorizzati censisce un soggetto in quel ruolo). 
 STATUS: tabella di transcodifica, l‟elenco dei valori è: attivo, radiato, sospeso o 
cancellato. Uno status può essere censito nella tabella ma non ancora assegnato a 
nessun soggetto censito nel RegIndE (nessun ente tra quelli memorizzati censisce 
un soggetto in quello status). 
 STORICO SOGGETTI: Permette di storicizzare per ogni soggetto tutte le 
modifiche che coinvolgono l‟appartenenza ad un ente, lo status e il ruolo. La 
scelta di modellare la storicizzazione in un‟entità specifica, è motivata soprattutto 
dal fatto di rendere più semplice l‟entità che associa il soggetto all‟ente: 
SOGGETTI per ENTE; infatti su tale entità si è deciso di non indicare il periodo 
temporale di validità del soggetto nell‟ente, nel ruolo e nello status,  ma di 
registrare una nuova occorrenza per ogni modifica, delle suddette informazioni, 
nell‟entità STORICO SOGGETTI. Essa rappresenta una sorta di registro dei 
soggetti nel RegIndE, che, grazie all‟indicazione della data di  ogni modifica, 
permette di conoscere la storia di ogni singolo soggetto censito attraverso una 
semplice interrogazione per ordine di data.  
Di seguito l‟elenco dettagliato delle entità descritte nella figura precedente dove per 
ognuna di esse sono riportati i nomi fisici delle tabelle e dei singoli attributi. 
Nome Tabella: ENTI 
Nome fisico 
Tipo di dati 
Obbl. PK 
Note 
IDENTE 
VARCHAR2(32) 
SI 
SI 
Identificativo dell‟ente 
CODICE 
VARCHAR2(50) 
SI 
 
Codice ente 
DESC 
VARCHAR2(256) 
SI 
 
Descrizione Ente 
CODFISC 
VARCHAR2(16) 
 
 
Codice fiscale dell‟ente 
PIVA 
VARCHAR2(11) 
 
 
Partita Iva dell‟ente 
Tabella 1 - Tabella Enti

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
Nome Tabella: SOGGETTI 
Nome fisico 
Tipo di dati 
Obbl. PK 
Note 
IDSOGGETTO 
VARCHAR2(32) 
SI 
SI 
Identificativo soggetto 
IDENTE 
VARCHAR2(32) 
SI 
 
FK – Identificativo ente 
NOME 
VARCHAR2(256) 
SI 
 
Nome del soggetto 
COGNOME 
VARCHAR2(256) 
SI 
 
Cognome del soggetto 
DT_NASCITA 
DATE 
 
 
Data di nascita 
LUOGO_NASCITA 
VARCHAR2(256) 
 
 
Luogo di nascita 
PROV_NASCITA 
VARCHAR2(4) 
 
 
Provincia di nascita 
CODFISC 
VARCHAR2(16) 
SI 
 
Codice fiscale 
PEC 
VARCHAR2(256) 
 
 
Indirizzo di PEC 
Tabella 2 - Tabella Soggetti 
Nome Tabella: INDIRIZZI 
Nome fisico 
Tipo di dati 
Obbl. PK 
Note 
IDINDIRIZZO 
VARCHAR2(32) 
SI 
SI 
Identificativo indirizzo 
IDSOGGETTO 
VARCHAR2(32) 
SI 
 
FK – Soggetto 
INDIRIZZO 
VARCHAR2(100
0) 
SI 
 
Indirizzo 
TP_INDIRIZZO 
CHAR 
SI 
 
Tipologia: 
Residenza, 
Domicilio legale 
CAP 
VARCHAR2(5) 
SI 
 
CAP 
COMUNE 
VARCHAR2(256) 
SI 
 
Comune 
PROV 
VARCHAR2(4) 
SI 
 
Provincia  
TELEFONO 
NUMBER(15) 
 
 
Numero telefono 
FAX 
NUMBER(15) 
 
 
Numero fax 
EMAIL 
VARCHAR2(256) 
 
 
Indirizzo ordinario posta 
elettronica 
Tabella 3 - Tabella Indirizzi 
Nome tabella: IND_ABILITATI 
Nome fisico 
Tipo di dati 
Obbl. PK 
Note 
IDPEC 
VARCHAR(32) 
SI 
SI 
Identificativo PEC 
IDENTE 
VARCHAR2(32) 
SI 
 
FK- Ente 
PEC 
VARCHAR2(256) 
SI 
 
Indirizzo di PEC 
CODFISC_FIRMA 
VARCHAR2(16) 
SI 
 
Codice fiscale del 
firmatario albo 
Tabella 4 - Tabella indirizzi PEC abilitati all’invio

Nuova infrastruttura dei servizi telematici 
Nuovo Registro Generale degli Indirizzi Elettronici (ReGIndE) 
Versione 1.0 
 
Nome tabella: RUOLI 
Nome fisico 
Tipo di dati 
Obbl. PK 
Note 
IDRUOLO 
VARCHAR(32) 
SI 
SI 
Identificativo ruolo 
DESC 
VARCHAR2(256) 
SI 
 
Descrizione ruolo 
Tabella 5 – Tabella di transcodifica dei ruoli 
Nome tabella: STATUS 
Nome fisico 
Tipo di dati 
Obbl. PK 
Note 
IDSTATUS 
VARCHAR(32) 
SI 
SI 
Identificativo status 
DESC 
VARCHAR2(256) 
SI 
 
Descrizione status 
Tabella 6 – tabella di transcodifica dello status 
Nome tabella: SOGGETTI_ENTE 
Nome fisico 
Tipo di dati 
Obbl. PK 
Note 
IDSOGGETTIENTE VARCHAR(32) 
SI 
SI 
Identificativo tabella 
IDENTE 
VARCHAR2(32) 
SI 
 
FK- Ente 
IDSOGGETTO 
VARCHAR2(32) 
SI 
 
FK- Soggetto 
IDRUOLO 
VARCHAR2(32) 
SI 
 
FK- Ruolo 
IDSTATUS 
VARCHAR2(32) 
SI 
 
FK- Status 
Tabella 7 – Tabella Soggetti per ente 
Nome tabella: STORICO_SOGGETTI 
Nome fisico 
Tipo di dati 
Obbl. PK 
Note 
IDSTORICOSOGG
ETTI 
VARCHAR(32) 
SI 
SI 
Identificativo tabella 
IDENTE 
VARCHAR2(32) 
SI 
 
FK- Ente 
IDSOGGETTO 
VARCHAR2(32) 
SI 
 
FK- Soggetto 
IDRUOLO 
VARCHAR2(32) 
SI 
 
FK- Ruolo 
IDSTATUS 
VARCHAR2(32) 
SI 
 
FK- Status 
DTEVENTO 
DATE 
SI 
 
Data 
evento 
da 
storicizzare 
Tabella 8 – Tabella Storico Soggetti