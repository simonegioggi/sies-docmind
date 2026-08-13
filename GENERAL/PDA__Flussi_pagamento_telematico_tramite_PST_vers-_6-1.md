---
uniqueName: pdaflussipagamentotelematicotramitepstvers-6-1
displayName: "PDA  Flussi pagamento telematico tramite PST vers  6 1"
category: "GENERAL"
tags: []
---

# PDA__Flussi_pagamento_telematico_tramite_PST_vers._6.1

> **File originale:** `MEV/SCHEDA_013/Docs/PDA__Flussi_pagamento_telematico_tramite_PST_vers._6.1.pdf`  
> **Tipo:** PDF

---

Indicazioni Tecnico Operative 
per erogazione dei pagamenti online tramite i servizi del Portale dei 
Servizi Telematici – modello di pagamento con Avviso 
(documento per i Punti di Accesso operanti nell’ambito del dominio Giustizia) 
 
 
 
 
 
 
vers. 6.1

Glossario 
PST 
Portale dei Servizi Telematici del Ministero della Giustizia 
PSP 
Prestatori di Servizi di Pagamento (Poste Italiane, banche, ecc...) 
Ente Creditore 
Pubblica Amministrazione a cui devono essere assegnate le somme pagate 
RT 
Ricevuta Telematica (oggetto XML) 
Avviso di 
Pagamento 
Documento pdf contenente le informazioni per eseguire il pagamento presso gli sportelli fisici o 
virtuali di un PSP, compresa l’app IO 
NodoSPC 
Nodo dei Pagamenti reso disponibile e gestito dalla società pagoPA 
IUV 
Identificativo Univoco di Versamento

Sommario 
CONTESTO ......................................................................................................................... 4 
FLUSSO PAGAMENTO ...................................................................................................... 5 
SEQUENZA DI INTERAZIONI APPLICATIVO- PST .......................................................... 6 
INDICAZIONI OPERATIVE ................................................................................................. 7 
DATI SCAMBIATI – RICHIESTA DI PAGAMENTO ........................................................... 7 
SERVIZI ESPOSTI DAL PST .............................................................................................. 9 
TABELLA 1 - DATI SPECIFICI RISCOSSIONE ................................................................. 9

Le indicazioni contenute nel documento sono destinate ai Punti di Accesso che espongo alla propria 
utenza i servizi di pagamento online utilizzando le API esposte dal Portale dei Servizi Telematici. 
CONTESTO 
Alla luce dell’articolo 5 del Codice dell’Amministrazione Digitale di cui al D.Lgs. n. 82/2005, le 
Pubbliche Amministrazioni sono obbligate ad accettare i pagamenti spettanti a qualsiasi titolo 
attraverso sistemi di pagamento elettronico. Per il conseguimento degli obiettivi di razionalizzazione 
e contenimento della spesa pubblica in informatica, e al fine di garantire omogeneità di offerta ed 
elevati livelli di sicurezza, le Pubbliche Amministrazioni - ai sensi dell’articolo 15, comma 5 bis, del 
Decreto Legge n. 179/2012, come convertito in legge - sono tenute ad avvalersi dell’infrastruttura 
tecnologica pubblica, meglio conosciuta come Nodo_dei_PagamentiSPC, messa a disposizione da 
PagoPA S.p.A.. 
Il documento “Linee Guida per l’effettuazione dei pagamenti elettronici a favore delle Pubbliche 
Amministrazioni e dei Gestori di Pubblici Servizi” - pubblicato in G.U. n. 152 del 3 luglio 2018 - 
definisce le regole e le modalità di effettuazione dei pagamenti elettronici, tramite il Nodo dei 
Pagamenti, da parte dei soggetti aderenti. Le Linee Guida, in quanto normativa secondaria, hanno 
come presupposto le disposizioni primarie in materia di pagamenti, ivi inclusa la normativa nazionale 
per il recepimento della PSD2. 
Il Portale dei Servizi Telematici (PST) implementa i servizi e gestisce le informazioni specifiche 
previste dalle Linee Guida per il soggetto Ente Creditore. 
Nello specifico: 
- 
realizza la connessione logica e fisica verso il NodoSPC dei pagamenti 
- 
gestisce le posizioni debitorie 
- 
avvia il flusso di pagamento on-line (pagamento immediato tramite la sessione di lavoro) 
- 
avvia e gestisce il flusso di pagamento eseguito presso il PSP (tramite avviso pagoPA) 
- 
gestisce il reindirizzamento per la scelta del canale di pagamento secondo una user-experience 
resa disponibile da pagoPA e unica per tutti gli Enti aderenti 
- 
gestisce la ricezione delle ricevute di pagamento 
- 
gestisce il repository nazionale delle ricevute di pagamento 
- 
gestisce le operazioni di verifica della RT e di ‘bruciatura’ della RT 
- 
gestisce il Giornale degli eventi previsto dalle Linee Guida pagoPA 
- 
esegue le operazioni di verifica della rendicontazione ai fini della riconciliazione 
- 
esegue tutte le operazioni accessorie e di servizio previste dall’integrazione con la piattaforma 
pagoPA. 
 
Tutte le operazioni eseguite dal PST sono concepite come servizi erogati tramite interfacce applicative 
esposte in appositi Web Services SOAP. L’insieme delle interfacce applicative esposte (API) 
costituisce, pertanto, il punto di ingresso per l’integrazione dei pagamenti pagoPA nelle 
applicazioni/sistemi del dominio Giustizia.

FLUSSO PAGAMENTO 
Secondo le nuove specifiche pagoPA l’unica modalità di pagamento disponibile resterà, a  breve, 
quella tramite generazione di avviso di pagamento. Il c.d. modello 1 (o pagamento online) sarà 
deprecato. 
Il presente documento ha la finalità di illustrare questo nuovo flusso di pagamento e i WS da utilizzare 
per realizzarlo. 
Modalità Pagamento con avviso pagoPA 
Nel seguito si intende per ‘applicativo’ il modulo pagamenti implementato dallo specifico PDA 
Quando un utente necessita di eseguire un pagamento, l’applicativo richiede al PST di creare una 
posizione debitoria: il PST restituisce al chiamante un ‘numero avviso’ (sequenza di cifre che 
contiene all’interno lo IUV, come di seguito dettagliato) e un file in formato pdf contenente l’avviso 
pagoPA da mettere a disposizione dell’utente per la stampa o la visualizzazione online. 
L’utente esegue il pagamento ‘fuori linea’ utilizzando gli sportelli fisici, le applicazioni di home 
banking, l’app IO o l’applicazione web di check out resa disponibile sul sito pagoPA (semplicemente 
inquadrando il QR_code presente sull’avviso o inserendo a mano IUV e CF di Giustizia) 
L’applicativo, per completare il proprio flusso di servizio, può richiedere al PST lo stato della 
posizione debitoria e, nel caso in cui risulti saldata, scarica il file contenente la RT relativa al 
pagamento eseguito. 
A differenza del modello 1 finora implementato, nel caso di pagamento con avviso se nel PST è 
presente la RT allora è sicuramente positiva (non ci saranno RT negative).

Riepilogando: 
Pagamento con avviso (non contestuale) 
Applicativo 
PST 
invia a PST dati per richiesta pagamento con avviso 
 
 
restituisce NumeroAvviso e PDF con avviso 
mette a disposizione download PDF 
 
........ 
 
 
scarica la RT (ricevuta pagamento) o controlla stato 
del pagamento 
 
 
 
SEQUENZA DI INTERAZIONI APPLICATIVO- PST 
Si riporta di seguito la sequenza di invocazioni, da parte di un applicativo, dei servizi esposti dal PST.  
Le specifiche tecniche dei WSDL sono contenute nel documento “Documentazione servizi web 
esposti” scaricabile dall’area documentazione del Portale dei Servizi Telematici:  
https://pst.giustizia.it/PST/it/paginadettaglio.page?contentId=ACC1253  
 
Pagamento tramite avviso 
Nel caso di pagamento tramite generazione di avviso, l’applicativo invia al PST il file 
richiestaPagamentoTelematica.xml (valorizzando anche più occorrenze di datiSingoloVersamento) 
come parametro del metodo generaAvviso (...); il PST crea la posizione debitoria per il pagatore e 
restituisce al chiamante il file PDF contenente l’avviso di pagamento analogico e il NumeroAvviso 
che contiene l’identificativo univoco del versamento (IUV). Lo IUV si ricava eliminando la prima 
cifra, a sinistra (valore 3), dal numero avviso (es: nel caso di numero avviso = 330004475050181849, 
lo IUV sarà 30004475050181849). 
Il file contenente l’avviso analogico dovrà essere messo a disposizione dell’utente per il download e 
successiva stampa. 
 
Scarico della Ricevuta o verifica dello stato della posizione debitoria 
 
per ottenere la Ricevuta Telematica registrata nel PST è necessario utilizzare il metodo 
downloadRicevuta(..).

Per verificare lo stato della posizione debitoria si utilizza il metodo elencoPagamenti(...) che 
restituisce nella struttura statoRichiesta, oltre ad altre informazioni, anche i due elementi: stato e 
stato_nodoPA. 
L’elemento stato contiene l’indicazione dello stato del pagamento nel contesto del PST e può 
assumere uno dei seguenti valori: 
• DISPONIBILE, indica che è presente la RT (sicuramente positiva) e non è stata utilizzata 
dall’utente 
• USATO, indica che il pagamento è stato utilizzato 
• OK_PSP, indica che l’utente ha eseguito un tentativo di pagamento ma ancora non è 
disponibile la RT 
• RIMBORSATO, indica che il pagamento è stato rimborsato dall’Amministrazione 
 
Si precisa che, finché l'utente non ha una conferma del PSP sul buon esito della transazione di 
pagamento dell’avviso, la ricevuta telematica non potrà essere disponibile. 
Pertanto, si richiede l’implementazione, all’interno dell’applicativo PDA, di una soluzione secondo 
la quale sia l’utente a richiamare il servizio di verifica o download della ricevuta; sono vietati  
automatismi all’interno degli applicativi che generino polling continui ai servizi elencoPagamenti e 
downloadRicevuta.   
 
 
INDICAZIONI OPERATIVE 
Relativamente ai servizi che permettono di usufruire delle funzionalità esposte dal PST e relative ai 
Pagamenti Telematici si fa presente che la documentazione, comprensiva dei WSDL, è disponibile 
all’indirizzo https://pst.giustizia.it/PST/it/paginadettaglio.page?contentId=ACC1253   
 
La url a cui risponde tale proxy di test è  la seguente. 
 
proxy PDA: https://pda.processotelematicotest.giustizia.it 
 
 
 
DATI SCAMBIATI – RICHIESTA DI PAGAMENTO  
Si riporta di seguito la struttura del file richiestaPagamentoTelematica.xml che dovrà essere utilizzata 
come input del metodo generaAvviso (...). Il file è il medesimo utilizzato nell’invocazione dell’attuale 
generaRPT (..)

• codiceDistretto e codiceUfficio . 
• autenticazione soggetto può assumere i valori 
o CNS, se l’utente è autenticato in maniera ‘forte’  (CIE/CNS/SPID) 
o USR, se utente autenticato con User_Id e Password 
o OTH, se l’utente autenticato in modo diverso 
• soggettoPagatore soggetto debitore nei confronti della PA; 
• soggettoVersante è opzionale (è il soggetto che effettivamente paga, inserire solo se diverso dal 
pagatore). Nel modello con avviso non viene preso in considerazione; 
• datiVersamento è una struttura composta da:  
 
o importoTotale: somma degli elementi ‘importo’ contenuti nei singoli versamenti. Il 
valore deve contenere obbligatoriamente le due cifre decimali con separatore il ‘.’ 
o ibanAddebito – se valorizzato, nel WISP l’utente potrà selezionare, come metodo di 
pagamento, anche l’addebito sul conto corrente specificato. Da non valorizzare nel caso 
in cui il file debba essere usato in generaAvviso(..)

o datiSingoloVersamento (da 1 a 5 occorrenze) in cui specificare: 
▪ importo: l’importo deve contenere obbligatoriamente le due cifre decimali con 
elemento separatore il ‘.’ 
▪ causale: massimo 100 caratteri e con il seguente formato 
“/<importo>/TXT/<descr causale>”. Es: “/139.0/TXT/pagamento per xxxxx” 
▪ datiSpecificiRiscossione: come da TABELLA 1 - dati specifici riscossione 
definisce la tipologia del pagamento secondo una specifica codifica. 
▪ elemento datiMarcaBolloDigitale – deve essere ignorato dai PDA  
 
La compilazione del file sopra indicato resta identica a quella finora utilizzata. 
 
SERVIZI ESPOSTI DAL PST   
Si riportano di seguito alcuni suggerimenti per l’utilizzo dei metodi esposti dal PST 
Per la creazione dell’avviso di 
pagamento 
invocare il metodo generaAvviso passando come parametro la 
struttura 
xml 
RichiestaPagamentoTelematico. 
Il 
metodo 
restituirà il NumeroAvviso (corrisponde all’identificativo 
univoco del pagamento) e un file pdf contenente l’avviso da usare 
per pagare presso un PSP 
 
Per ottenere informazioni circa 
i pagamenti memorizzati sul 
PST (tra cui lo stato del 
pagamento 
o 
posizione 
debitoria) 
invocare il metodo elencoPagamenti valorizzando in modo 
opportuno i dati di input. La funzione restituisce le informazioni 
su tutti i pagamenti memorizzati nel PST, generati dal PDA 
invocante e in uno stato diverso da ELIMINATO, che soddisfano 
i criteri passati come input. 
per ottenere nuovamente il file 
PDF contenente l’avviso 
analogico 
invocare il metodo downloadAvviso passando come parametro il 
numeroAvviso 
per ottenere la Ricevuta 
Telematica (RT) 
invocare il metodo downloadRicevuta che restituirà l’intero file 
xml contenente i dati relativi all’esito del pagamento 
 
Tutte gli altri metodi saranno deprecati. 
 
TABELLA 1 - DATI SPECIFICI RISCOSSIONE 
L'elemento DatiSpecificiRiscossione nella struttura RichiestaPagamentoTelematica.xml assume uno 
dei valori sotto riportati  
• CONTRIB per Contributo unificato 
• DIRCANC per Diritti di cancelleria 
• DIRCOPIA per Diritti di Copia 
 
All’interno del singolo avviso/posizione debitoria restano valide le combinazioni attualmente 
permesse: 
 
Contributo Unif 
Diritti Cancelleria 
Diritti Copia

SI 
SI 
NO 
NO 
NO 
SI 
SI 
NO 
NO 
NO 
SI 
NO