---
uniqueName: applicativi-flussi-pagamento-telematico-tramite-ps
displayName: "APPLICATIVI   Flussi pagamento telematico tramite PST vers  3 1"
category: "GENERAL"
tags: []
---

# APPLICATIVI - Flussi pagamento telematico tramite PST vers. 3.1

> **File originale:** `MEV/SCHEDA_013/Docs/APPLICATIVI - Flussi pagamento telematico tramite PST vers. 3.1.pdf`  
> **Tipo:** PDF

---

Indicazioni Tecnico Operative 
per l'integrazione dei pagamenti pagoPA tramite i servizi del Portale 
dei Servizi Telematici 
(documento per gli applicativi operanti nell’ambito del dominio Giustizia) 
 
 
 
 
 
 
vers. 3.1

Glossario 
PST 
Portale dei Servizi Telematici del Ministero della Giustizia 
PSP 
Prestatori di Servizi di Pagamento (Poste Italiane, banche, ecc...) 
Ente Creditore 
Pubblica Amministrazione a cui devono essere assegnate le somme pagate 
RPT 
Richiesta di Pagamento Telematico (oggetto XML) 
RT 
Ricevuta Telematica (oggetto XML) 
Avviso 
Analogico 
Documento pdf contenente le informazioni per eseguire il pagamento presso gli sportelli fisici o 
virtuali di un PSP, compresa l’app IO 
NodoSPC 
Nodo dei Pagamenti reso disponibile e gestito dalla società pagoPA 
CRS 
Identificativo Univoco di pagamento nell'ambito Giustizia. Corrisponde allo IUV 
indicato nelle Linee Guida pagoPA 
Bruciatura RT 
Contrassegno che si pone sulla RT per significare che è stata usata; procedura che si 
adotta nei casi in cui il pagamento è eseguito spontaneamente dall’utente fuori dal 
flusso di elaborazione dell’applicazione che eroga il servizio

Sommario 
CONTESTO ......................................................................................................................... 4 
FLUSSO PAGAMENTO ...................................................................................................... 5 
FUNZIONALITÀ MINIME .................................................................................................... 7 
SEQUENZA DI INTERAZIONI APPLICATIVO- PST .......................................................... 7 
INDICAZIONI OPERATIVE ............................................................................................... 10 
DATI SCAMBIATI – RICHIESTA DI PAGAMENTO ......................................................... 10 
SERVIZI ESPOSTI DAL PST ............................................................................................ 12 
TABELLA 1 - DATI SPECIFICI RISCOSSIONE ............................................................... 13 
PAGAMENTO BOLLO DIGITALE .................................................................................... 14 
GESTIONE ELEMENTI 'PAGATORE' E 'VERSANTE' ..................................................... 14 
CODICI PER ESITO PAGAMENTO .................................................................................. 15 
AUTENTICAZIONE DEGLI APPLICATIVI ........................................................................ 15 
VERIFICA E BRUCIATURA DI UNA RICEVUTA TELEMATICA ..................................... 16 
dettaglio metodi e struttura daticontesto ....................................................................................................................... 18

Le indicazioni contenute nel documento sono destinate agli applicativi che implementano nel proprio 
flusso di servizio un pagamento eseguito tramite la piattaforma pagoPA. 
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
La connessione con il Nodo dei Pagamenti-SPC è realizzata con il meccanismo delle Porte di 
Dominio.

FLUSSO PAGAMENTO 
Viene di seguito illustrato, in maniera sintetica e ad alto livello, il flusso operativo per l’esecuzione 
di un pagamento pagoPA attraverso le funzionalità rese disponibili dal Portale dei Servizi Telematici. 
Modalità Pagamento on-line 
Nell’ambito della logica di business dell’applicativo, se è necessario richiedere all’utente il 
pagamento di un dato importo, l’applicativo individua gli elementi specifici del pagamento (pagatore, 
importo, 
tipologia 
di 
pagamento, 
causale) 
e 
produce 
un 
file 
strutturato 
(richiestaPagamentoTelamatica.xml) che invia al PST chiedendo la creazione di una posizione 
debitoria per l’utente. Il PST restituisce il file RPT.xml compilato con le informazioni comunicate 
dall’applicativo e con altre informazioni (tra cui l’identificativo univoco di versamento –IUV) 
generate dal PST e relative alla posizione debitoria creata. 
L’applicativo richiede, quindi, al PST di inoltrare il pagamento al NodoSPC e gestisce il 
reindirizzameto dell’utente sull’interfaccia WISP del NodoSPC1. L’utente procede al versamento 
(fase di check-out) e il controlla torna, per il tramite del PST, all’applicativo chiamante che dovrà 
gestire il ritorno secondo la procedura dis eguito indicata.  
L’applicativo può creare più RPT e decidere di inviarle al NodoSPC con un unico invio (viene creato 
un carrello di RPT). Le RPT nel carrello non possono essere più di 5 e devono far capo al medesimo 
Versante o Pagatore. Il carrello deve essere gestito dall’applicativo: le RPT che fanno parte di un 
carrello vengono comunicate al PST come parametri del metodo inviaCarrelloRPT (..). Tutte le RPT 
contenute nel carrello verranno pagate in un’unica soluzione e per ogni RPT verrà restituita da 
pagoPA una specifica RT. 
 
1 è previsto per l’utente l’utilizzo di una interfaccia, unica messa a disposizione dal NododeiPagamenti-SPC, che uniforma 
e migliora la user-experience dell’utente finale. Tale componente prende il nome di WISP (Wizard interattivo Scelta del 
PSP) ed implementa le logiche di selezione del PSP e di completamento del pagamento.

All’esito del pagamento, il NodoSPC restitisce al PST una ricevuta telematica (RT.xml) per ogni 
RPT.xml inviata (per ogni singolo pagamento viene restituita una ricevuta). E’ onere dell’applicativo 
verificare lo stato del pagamento invocando appositi servizi esposti dal PST. 
 
 
 
Modalità Pagamento presso PSP (avviso pagoPA) 
L’applicativo può richiedere al PST di creare una posizione debitoria finalizzata al pagamento presso 
PSP: in questo caso, il PST non restituirà il file RPT.xml ma un ‘numero avviso’ e un file in formato 
pdf contenente l’avviso pagoPA da mettere a disposizione dell’utente per la stampa o la 
visualizzazione on-line. 
L’applicativo, per completare il proprio flusso di servizio, richiede al PST lo stato della posizione 
debitoria e, nel caso in cui risulti saldata, scarica il file contenente la RT relativa al pagamento 
eseguito oppure eroga il servizio. 
 
Riepilogando: 
Pagamento On-Line (contestuale) 
Applicativo 
PST 
invia a PST dati per creazione richiesta pagamento (RPT)  
 
restituisce RPT con IUV 
chiede al PST l’invio delle RPT contenute nel carrello 
 
 
gestisce l’invio e i reindirizzamenti

gestisce i reindirizzamenti 
 
 
 
scarica la RT (ricevuta pagamento) o controlla stato 
pagamento 
 
 
Pagamento presso PSP (non contestuale) 
Applicativo 
PST 
invia a PST dati per richiesta pagamento con avviso 
 
 
restituisce NumeroAvviso e PDF con avviso 
mette a disposizione download PDF 
 
........ 
 
 
scarica la RT (ricevuta pagamento) o controlla stato 
del pagamento 
 
 
FUNZIONALITÀ MINIME  
Di seguito, la descrizione delle funzionalità che devono essere presenti in un applicativo per la 
gestione dei pagamenti pagoPA: 
1) Compilazione di una RPT. Le informazioni con cui compilare la richiestaPagamentoTelematica 
da inoltrare al PST sono o note all’applicativo o inserite dall’utente a interfaccia. La struttura del file 
da compilare è riportata al paragrafo DATI SCAMBIATI – R. La generazione dell’intera RPT avviene a 
cura del PST e il file xml (RPT.xml) è restituito dal PST all’applicativo chiamante. L’inoltro della 
RPT al NodoSPC viene eseguita esclusivamente dal PST.  
 
2) 
Scarico (download) della RT o verifica stato del pagamento (verifica della posizione 
debitoria): l’applicazione può, alternativamente, o scaricare la RT (per utilizzi applicativi in cui sia 
necessaria -es: deposito PCT) oppure verificare lo stato del pagamento (stato della posizione debitoria 
creata nel caso di pagamento tramite avviso). La modalità di recupero della RT o di verifica dello 
stato è eseguita in modalità ‘pull’, quindi l’applicativo deve esplicitamente invocare il metodo 
appropriato esposto dal PST. 
 
3) 
Bruciatura/Annullamento della RT: nei casi in cui il pagamento potrebbe essere riutilizzato 
(double-spending), l’applicativo deve provvedere alla bruciatura della RT invocando appositi metodi 
esposti dal PST (vedi paragrafo VERIFICA E BRUCIATURA DI UNA RICEVUTA 
TELEMATICA). Non applicabile nei casi in cui il pagamento è avviato nell’ambito del flusso 
operativo di un servizio informatizzato e si possa garantire che la tipologia del pagamento non possa 
essere utilizzata in altri contesti. 
 
 
SEQUENZA DI INTERAZIONI APPLICATIVO- PST 
Si riporta di seguito la sequenza di invocazioni, da parte di un applicativo, dei servizi esposti dal PST.  
Le specifiche tecniche dei WSDL sono contenute nel documento “Documentazione servizi web 
esposti” 
scaricabile 
dall’area 
documentazione 
del 
Portale 
dei 
Servizi 
Telematici: 
http://pst.giustizia.it/PST/it/pst_26_1.wp?previousPage=pst_26&contentId=DOC568

Pagamento on-line 
La sequenza di invocazione dei servizi è illustrata e descritta nel seguito. 
 
 
1. al momento di creare la posizione debitoria, l’applicativo richiede al PST la generazione del file 
RPT.xml usando il metodo generaRPT(..) che ritorna al chiamante il file xml della richiesta di 
pagamento (i dati relativi alla richiesta e il file RPT.xml vengono memorizzati nel PST). Il codice 
IUV sarà contenuto nell’apposito campo della RPT restituita. L’applicativo può gestire, per conto 
dello stesso utente pagatore, un carrello con al massimo 5 RPT; 
2. l’applicativo può invocare opzionalmente (in ogni momento) il metodo elencoPagamenti (...) per 
conoscere i dettagli delle RPT generate e memorizzate nel PST. L’invocazione di tale metodo e i dati 
restituiti dal PST sono necessari per conoscere i parametri necessari all’invocazione di altri metodi 
esposti dal PST (vedi seguito della descrizione); 
3. quando l’utente o il flusso applicativo sono pronti per l’esecuzione del pagamento, l’applicativo 
invoca il metodo inviaCarrelloRPT(...) esposto dal PST. Al metodo viene passato in input uno/più

IUV relativi alle RPT da pagare. Nel caso l’utente dovesse rinunciare al pagamento, è consigliabile 
invocare il metodo eliminaRichiesta (...) per ‘pulire’ il carrello gestito dal PST. 
Se il carrello non presenta errori, all’applicativo sarà restituito il valore dell’URL verso cui 
reindirizzare la sessione aperta dal soggetto chiamante (reindirizzamento tramite browser). L’URL 
indirizza il componente del NodoSPC (WISP) che gestisce la fase di check-out del pagamento.  
Se il carrello presenta errori, il risultato del’invocazione inviaCarrelloRPT(...) sarà KO seguito da 
una struttura faultBean che sarà riportata all’applicativo. In questo caso, in generale, l’errore non 
dipende dai dati inseriti dall’utente ma da un errore nell’interazione con il NodoSPC: è necessario 
esaminare i dati contenuti nella struttura faultBean per comprendere la natura del problema ed 
eventualmente inviare una segnalazione all’area civile della DGSIA (info-pct@giustizia.it). 
Se a seguito dell’invocazione della inviaCarrelloRPT(...) si riceve una eccezione di timeout (non si 
ottiene l’url del WISP) è necessario ricostituire il carrello ricompilando la RPT del carrello (punto 1. 
del presente  flusso); 
4. Al completamento dell’interazione tra l’utente e il WISP, il PST restituisce l’URL a cui far ritornare 
il browser dell’utente collegato. Tale URL è nella forma <homepage applicativo> 
/giustizia/servizi/pagamenti/esitoPagamento? esito=<esito>   e deve essere gestito all’interno 
dell’applicativo. L’elemento esito può assumere 3 valori: 
 
1) OK – indica che il pagamento presso il portale del PSP è stato eseguito con successo; 
2) ERROR – il pagamento presso il Portale PSP non è stato eseguito con successo; 
3) DIFFERITO – l’esito del pagamento eseguito dall’utilizzatore finale presso il Portale PSP sarà 
noto solo al ricevimento della RT. 
 
Si segnala che tale esito è memorizzato nel PST, associato al pagamento, e nell’ambito 
dell’applicativo deve essere gestita la messaggistica per l’utente e le azioni seguenti. A tale proposito, 
si evidenzia che in tutti i casi di esito del pagamento viene sempre generata una RT: si consiglia di 
aspettare la ricezione della RT per essere certi dell’esito effettivo del pagamento. In caso di RT 
negativa, per procedere ad un nuovo tentativo di pagamento è necessario ricompilare la RPT (passo 
1. del presente flusso). 
Il flusso prosegue con il successivo punto 5. 
 
Pagamento presso PSP – modello multi pagamento o multi beneficiario 
Nel caso di pagamento presso PSP tramite generazione di avviso pagamento, l’applicativo invia al 
PST il file richiestaPagamentoTelematica.xml (valorizzando anche più occorrenze di 
datiSingoloVersamento) come parametro del metodo generaAvviso (...); il PST crea la posizione 
debitoria per il pagatore e restituisce al chiamante il file PDF contenente l’avviso di pagamento 
analogico e il NumeroAvviso che contiene l’identificativo univoco del versamento (IUV). Lo IUV si 
ricava eliminando la prima cifra, a sinistra (valore 3), dal numero avviso (es: nel caso di numero 
avviso = 330004475050181849, lo IUV sarà 30004475050181849). 
Il file contenente l’avviso analogico dovrà essere messo a disposizione dell’utente per il download e 
successiva stampa. 
Il flusso prosegue con il successivo punto 5. 
 
Scarico della Ricevuta o verifica dello stato della posizione debitoria 
 
5. per ottenere la Ricevuta Telematica registrata nel PST è necessario utilizzare il metodo 
downloadRicevuta(..).

6. per verificare lo stato della posizione debitoria o di una richiesta di pagamento on-line (nei casi in 
cui non sia necessario scaricare la RT che è comunque conservata del repository del PST) si utilizza 
il metodo elencoPagamenti(...) che restituisce nella struttura statoRichiesta, oltre ad altre 
informazioni, anche i due elementi: stato e stato_nodoPA. 
L’elemento stato contiene l’indicazione dello stato del pagamento nel contesto del PST e può 
assumere uno dei seguenti valori: 
 
 
Il valore DISPONIBILE indica che è presente una Ricevuta Telematica con esito positivo (pagamento 
eseguito). 
INDICAZIONI OPERATIVE 
Relativamente ai servizi che permettono di usufruire delle funzionalità esposte dal PST e relative ai 
Pagamenti Telematici si fa presente che la documentazione, comprensiva dei WSDL, è disponibile 
all’indirizzo http://pst.giustizia.it/PST/it/pst_26_1.wp?previousPage=pst_26&contentId=DOC568   
 
L’applicativo sarà autorizzato all’invocazione dei web service tramite la presentazione di un 
certificato di autenticazione (X.509) su cui il PST eseguirà il controllo. Per i dettagli, si veda il 
paragrafo autenticazione degli applicativi. 
Il certificato deve essere comunicato prima dell’avvio dei test.  
All’applicativo verrà assegnato un identificativo associato in modo univoco al certificato. 
 
L’url del PST da usare nella fase di test è: https:\\servizibe.processotelematicotest.giustizia.it ed è 
accessibile unicamente dall’interno della RUG. Il server è ospitato nella sala Server Balduina; se 
necessario aprire le politiche firewall l’IP è 10.6.212.22 sulle porte 80 e 443. 
 
 
DATI SCAMBIATI – RICHIESTA DI PAGAMENTO  
Si riporta di seguito la struttura del file richiestaPagamentoTelematica.xml che dovrà essere utilizzata 
come input del metodo generaRPT(...) o generaAvviso (...).

• codiceDistretto e codiceUfficio : la valorizzazione dipende dallo specifico applicativo. 
• autenticazione soggetto può assumere i valori 
o CNS, se l’utente è autenticato in maniera ‘forte’  (CIE/CNS/SPID) 
o USR, se utente autenticato con User_Id e Password 
o OTH, se l’utente autenticato in modo diverso 
• soggettoPagatore soggetto debitore nei confronti della PA; 
• soggettoVersante è opzionale (è il soggetto che effettivamente paga, inserire solo se diverso dal 
pagatore) 
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
▪ elemento datiMarcaBolloDigitale – come da paragrafo  PAGAMENTO BOLLO 
DIGITALE . La presenza dell’elemento indica che le informazioni contenute 
nell’elemento datiSingoloVersamento si riferiscono all’acquisto di un bollo 
digitale 
(pertanto 
importo 
sarà 
pari 
esclusivamente 
a 
16.00 
e 
datiSpecificiRiscossione assumerà uno dei valori previsti per il bollo). 
ATTENZIONE: il bollo digitale NON può essere pagato tramite generazione di 
avviso pagoPA. 
 
Nel caso in cui si voglia includere in un singolo pagamento versamenti relativi a tipologie diverse 
(anche nel modello di pagamento con generazione avviso) è necessario istanziare più elementi 
datiSingoloVersamento, ognuno relativo ad una tipologia di pagamento diversa. 
Esempio: nel caso in cui sia necessario pagare un importo di 10,00 euro e un bollo da 16.00 euro, il 
file xml dovrà contenere due occorrenze di datiSingoloVersamento: una per il bollo digitale di 16.00 
euro e una per l’importo di 10.00 euro. 
 
SERVIZI ESPOSTI DAL PST   
Si riportano di seguito alcuni suggerimenti per l’utilizzo dei metodi esposti dal PST 
Per la creazione del file 
RPT.xml 
nel 
caso 
di 
pagamento contestuale on-line 
invocare il metodo generaRPT passando come parametro la 
struttura 
xml 
RichiestaPagamentoTelematico. 
Lo 
IUV 
(identificativo univoco versamento) sarà contenuto nella struttura 
RPT.xml restituita dal metodo invocato. 
Nel 
PST, 
il 
file 
RPT.xml 
sarà 
memorizzato 
nello 
stato=CARRELLO. 
Per la creazione dell’avviso 
analogico 
nel 
caso 
di 
pagamento presso PSP, non 
contestuale 
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
Per conoscere le richieste del carrello attivo (ancora non pagato) 
è necessario valorizzare in input lo stato=CARRELLO. 
Per esempio: per conoscere l’elenco delle RPT facenti parte del 
carrello di un certo utente con CF = AAA, invocare il metodo 
passando come parametri il CF (AAA) e lo stato=CARRELLO.

Per conoscere lo stato di un determinato pagamento, invocare il 
metodo passando in input l’identificativo del pagamento (IUV) 
Per eliminare una RPT dal 
carrello 
se la RPT è già stata generata (RPT memorizzata sul PST) 
invocare il metodo eliminaRichiesta che provvede a segnare 
come eliminata dal carrello la RPT in questione. Il metodo prende 
in input lo IUV che individua la RPT da considerare eliminata dal 
carrello. 
per ottenere nuovamente il file 
RPT.xml associato ad una 
richiesta (pagamento 
contestuale) 
invocare il metodo downloadRichiesta  
per ottenere nuovamente il file 
PDF contenente l’avviso 
analogico 
invocare il metodo downloadAvviso passando come parametro il 
numeroAvviso 
per procedere al pagamento di 
tutte le richieste contenute nel 
carrello (pagamento 
contestuale) 
invocare il metodo inviaCarrelloRPT passando come input il 
codice fiscale dell’utente pagatore e la lista degli IUV che 
individuano le RPT per le quali procedere al pagamento. La 
funzione si occupa di recuperare i file RPT.xml memorizzati 
PST, che risultano generati dal PDA, e inviarli al Nodo per la fase 
di check-out. 
per visualizzare lo stato di una 
richiesta di pagamento sul 
NododeiPagamenti-SPC 
(pagamento contestuale) 
invocare il metodo verificaRichiesta che riceve in input lo IUV 
del pagamento. La funzione interroga il NododeiPagamenti-SPC 
per conoscere lo stato in cui si trova il pagamento sul Nodo: il 
valore tornato permette di decidere circa il pagamento. 
per ottenere la Ricevuta 
Telematica (RT) 
invocare il metodo downloadRicevuta che restituirà l’intero file 
xml contenente i dati relativi all’esito del pagamento 
 
TABELLA 1 - DATI SPECIFICI RISCOSSIONE 
L'elemento DatiSpecificiRiscossione nella struttura RichiestaPagamentoTelematica.xml assume uno 
dei valori sotto riportati (altri valori saranno aggiunti nel caso di nuove tipologie di pagamenti o 
eventualmente in casi particolari in cui una tipologia di pagamento già presente sia attivata da un 
applicativo-da valutare nell’ambito dello specifico progetto) 
• CONTRIB per Contributo unificato 
• DIRCANC per Diritti di cancelleria 
• DIRCOPIA per Diritti di Copia 
• IFPV per Importo Fisso pubblicazione inserzione su PVP  
• BLOV per marca bollo digitale per Offerta di Vendita 
•  BLCS per marca bollo digitale per Certificato Casellario 
• DIRCAS per diritti di cancelleria nell’ambito del rilascio del Certificato Casellario 
• COAVV per il contributo per la partecipazione al concorso di avvocato 
• TSAVV per la tassa di abilitazione all’esercizio professione avvocato 
• BLAVV per il bollo digitale concorso avvocato 
• COMAG per il contributo per la partecipazione al concorso di magistrato 
• BLNT per il bollo digitale concorso notaio

• TSNOT per la tassa di abilitazione all’esercizio della professione di notaio 
• CONOT per il contributo per la partecipazione al concorso di notaio 
• AVCOPIA nel caso di pagamento diritti di copia per concorso avvocato 
• MGCOPIA nel caso di pagamento diritti di copia per concorso magistrato 
• NTCOPIA nel caso di pagamento diritti di copia per concorso notaio 
 
Esempio: nel caso del Portale Casellario, negli elementi ‘datiSingoloVersamento’ sarà usato il 
valore BLCS per il pagamento del bollo digitale e DIRCAS per i diritti di cancelleria. 
Si precisa che la RPT creata dal PST e restituita all’applicativo chiamante (nel caso di pagamento on-
line) avrà un valore di datiSpecificiRiscossione esteso rispetto ai valori indicati sopra, nel rispetto 
della tassonomia indicata da pagoPA. 
Queste alcune corrispondenze di esempio (si noti come dopo il secondo ‘/’ sia riportata la tipologia 
‘datiSpecificiRiscossione’ 
presente 
nella 
richiestaPagamentoTelematica.xml 
generata 
dall’applicativo). 
 
CONTRIB 
9/0702100SP/CONTRIB 
DIRCANC 
9/0702101SP/DIRCANC 
DIRCOPIA 
9/0702107SP/DIRCOPIA 
IFPV 
9/0702102SP/IFPV 
BLOV 
9/0702103SP/BLOV 
BLCS 
9/0702103SP/BLCS 
DIRCAS 
9/0702101SP/DIRCAS 
 
PAGAMENTO BOLLO DIGITALE 
Nel caso di pagamento di marca da bollo digitale è necessario inserire nel file 
richiestaPagamentoTelematica anche l’elemento ‘datiMarcaBolloDigitale’ con le seguenti 
informazioni: 
 
tipoBollo 
01 
hashDocumento 
 
 
SHA-256 
deve 
essere 
applicato 
alla 
rappresentazione binaria del documento 
provinciaResidenza 
sigla automobilistica 
 
GESTIONE ELEMENTI 'PAGATORE' E 'VERSANTE'

Soggetto Pagatore: deve essere sempre presente e coincide, in genere, con il soggetto che utilizza la 
funzionalità di pagamento (tipicamente l'avvocato o un soggetto abilitato esterno) e coincide con 
l'intestatario dello strumento di pagamento che verrà utilizzato.  
 
Soggetto Versante: è valorizzato solo nel caso in cui l'intestatario del conto o dello strumento di 
pagamento sia diverso dal soggetto Pagatore. In altre parole, Versante coincide con colui che 
materialmente esegue il versamento per conto del pagatore. 
 
Esempi: 
1) se Mario Rossi chiede di pagare usando il proprio conto, allora nella RPT sarà valorizzato Mario 
Rossi come Pagatore mentre il Versante non sarà valorizzato  
2) se Mario Rossi chiede di pagare usando il proprio conto ma desidera che il versamento risulti a 
nome del soggetto Verdi, allora il Pagatore sarà Verdi mentre il Versante sarà Mario Rossi. 
 
CODICI PER ESITO PAGAMENTO  
Sono considerati validi gli esiti pagamento con codice 0 (pagamento interamente eseguito con 
successo) e codice 2 (pagamento eseguito parzialmente: si può verificare solo nei casi in cui una 
stessa RPT contenga almeno due differenti versamenti) 
 
AUTENTICAZIONE DEGLI APPLICATIVI   
Il meccanismo di sicurezza application-to-application che verrà previsto nel colloquio tra applicazioni 
e PST sarà un’autenticazione forte basata su certificato.  
Per poter esporre i servizi del PST alle sole applicazioni autorizzate dovrà essere implementato un 
meccanismo di sicurezza di autenticazione forte basata su certificato. Il PST, per i servizi in questione, 
dovrà verificare che il certificato associato alla chiamata ricevuta sia di una CA attendibile e che 
corrisponda ad una delle applicazioni abilitate all’utilizzo di tali servizi, bloccando così l’accesso ad 
applicazioni non autorizzate.  
All’interno della parte apache della macchina del PST-BE e all’interno delle logiche di autenticazione 
ai servizi di jboss del PST-BE verrà previsto un meccanismo di sicurezza application-to-application 
per colloquio tra applicazioni e PST, basato sulla verifica del certificato utilizzato per la chiamata al 
servizio. 
Le applicazioni dovranno quindi munirsi di un certificato di CA attendibile da utilizzare al momento 
dell’invocazione a tali servizi. Tali certificati dovranno essere forniti in fase di sviluppo per poterli 
inserire all’interno del keystore della macchina del PST-BE, per le successive verifiche in fase di 
accesso a tali servizi. 
Il flusso di chiamata ai servizi, che si andrà ad instaurare, sarà: 
1. L’applicazione effettua la chiamata in HTTPS all’url del PST per l’invocazione di uno dei 
servizi ad essa esposti passando il certificato d’autenticazione; 
2. La parte apache della macchina del PST-BE riconosce la chiamata a tali servizi, tramite 
un’apposita Location configurata;

3. Il PST verifica che il certificato sia stato rilasciato da una CA attendibile; 
4. Il PST verifica che il certificato utilizzato per l’autenticazione corrisponde ad uno di quelli 
presenti all’interno del suo keystore relativi a tali servizi; 
5. Nel caso in cui i controlli ai punti 3 e 4 vadano a buon fine si procede all’esecuzione del 
servizio; 
6. Nel caso in cui i controlli terminano in errore verrà bloccata la chiamata e verrà restituito 
l’errore all’applicazione chiamante.  
Alla luce di quanto detto verrà quindi implementata una gestione all’interno della parte apache della 
macchina PST-BE, in modo tale da riconoscere, tramite un’apposita Location, la chiamata relativa ai 
servizi in questione. Nel caso si tratti di uno dei servizi, il PST si occuperà di verificare che il 
certificato associato alla chiamata sia stato rilasciato da una CA attendibile e che corrisponda al 
certificato, relativo all’applicazione chiamante, memorizzato all’interno del keystore. 
In base al risultato di tali controlli sul certificato il PST proseguirà con l’esecuzione del servizio 
oppure restituirà un errore all’applicazione che ha effettuato la chiamata. 
 
VERIFICA E BRUCIATURA DI UNA RICEVUTA TELEMATICA 
(solo nei casi in cui applicabile) 
Si riportano di seguito le operazioni da eseguire in tutti i casi in cui la tipologia di pagamento richieda 
che la RT venga ‘bruciata’ in modo da non poter essere ulteriormente utilizzata. 
La necessità dell’operazione di bruciatura dovrà essere valutata in sede di analisi. Es: in pagamenti 
completamente integrati nel flusso di erogazione di un servizio, non è necessario procedere alla 
bruciatura in quando l’utilizzo della RT è guidato dall’applicativo; diversa situazione nei casi di 
gestione ‘mista’ del servizio e relativo pagamento (file RT.xml di cui è l’utente a fare upload nel 
sistema). 
Fanno eccezione le marche da bollo digitali che riportato il file hash del documento a cui fanno 
riferimento e pertanto l’utilizzo di una RT relativa ad una marca da bollo può essere usata solo in 
associazione al documento a cui fa riferimento. In questo caso, il  file xml contenente la marca da 
bollo rilasciata da Agenzia delle Entrate è contenuto nell’elemento “TestoAllegato” della ricevuta 
RT.xml: l’applicazione si occuperà di estrarre la marca da bollo dal file RT.xml. 
Per la verifica e successiva bruciatura di una ricevuta di pagamento, il PST mette a disposizione degli 
applicativi i seguenti metodi (nel seguito i termini CRS e IUV sono da considerarsi sinonimi). 
- 
prenotaCRS (CRS, datiContesto): “blocca” una ricevuta per il successivo annullamento. Il valore 
del “contesto” permette di gestire sia la concorrenza negli annullamenti sia la correttezza 
dell’operazione, in ambiente distribuito, nel caso di fault dell’applicativo chiamante. La struttura 
di datiContesto e le specifiche del metodo saranno dettagliate di seguito Il metodo restituisce un 
identificativo del contesto. IdContesto. 
 
- 
annullaCRS (IdContesto, RT.xml): prende in input il valore dell’identificativo univoco e il file 
xml della RT e verifica se il file RT.xml coincide con quello conservato nel repository: in questo 
caso infatti la RT è da ritenersi valida in quanto le verifiche sono state eseguite dal PST in fase di 
ricezione della RT da parte del nodoPA. In caso positivo marca come “usato” il CRS in modo che

non sia possibile riutilizzare la stessa ricevuta, altrimenti restituisce al chiamante l’errore rilevato. 
Il metodo controlla anche che il pagamento contenuto nella RT sia coerente con il servizio 
implementato dall’applicazione chiamante (per es: che la RT contenga il pagamento di un importo 
per pubblicazione vendita nel caso in cui il chiamante sia il portale vendite). Le specifiche del 
metodo saranno dettagliate nell’allegato 1. 
 
- 
rilasciaCRS (IdContesto): sblocca un CRS precedentemente prenotato, per gestire eventuali casi 
in cui l’applicazione, dopo aver prenotato, non annulla la ricevuta e intende sbloccare il CRS. Le 
specifiche del metodo saranno dettagliate nell’allegato 1. 
 
- 
ripristinoCRS (crs): nel caso in cui lo stato della RT passata come parametro sia “usato”, riporta 
lo stesso nello stato ”disponibile”. Le specifiche del metodo saranno dettagliate di seguito. 
 
Logica con cui dovrebbe operare l’applicazione che usa una RT: 
o utente carica il file RT.xml tramite interfaccia; 
o applicazione, nel momento in cui stabilisce che il pagamento può essere accettato 
(dipendente dalla logica applicativa specifica dell’applicazione), estrae dal file RT.xml il 
valore del CRS contenuto nell’elemento ‘identificativoUnivoco’ e invoca il metodo 
prenotaCRS passando come paramentri il CRS estratto, l’intero file RT.xml e una struttura 
che permette di identificare univocamente il contesto in cui viene eseguito l’annullamento 
del pagamento; 
o se la prenotazione avviene con successo, l’aplicazione invocherà il metodo annullaCRS 
per marcare la ricevuta come già utilizzata;   
o in caso di problemi tecnici (timeout o fault dell’applicazione chiamante) in una delle 
invocazioni, è possibile richiamare nuovamente sia annullaCRS (se il contesto è noto) che 
prenotaCRS (con lo stesso contesto), a seconda dei mometi del flusso in cui sono stati 
registrati i problemi. Nel caso in cui il contesto sia andato perso è necessario aspettare il 
tempo per lo sblocco applicativo del CRS (10 minuti); 
o nel caso in cui la transazione  legata all’utlizzo della RT venga annullata o per qualsiasi 
altro flusso computazionale che comporti di fatto il non utilizzo della ricevuta,è necessario 
invocare ripristinaCRS(...) in modo che l’utente abbia la possibiltà di riutilizzare la 
ricevuta del pagamento effettuato. 
-

DETTAGLIO METODI E STRUTTURA DATICONTESTO  
 
PrenotaCRS 
Il servizio  “prenotaCRS()” è messo a disposizione alle applicazioni per la prenotazione di un CRS 
che desiderano successivamente annullare. 
In input al servizio le applicazioni  dovranno passare il CRS ed un oggetto “DatiContesto” che 
conterrà delle informazioni relative contesto di annullamento dell’applicazione. 
Il servizio “prenotaCRS()” si occuperà di: 
1. verificare che il CRS sia presente all’interno della Base Dati del PST e che abbia associata 
una RT con esito positivo; 
2. verificare che il CRS non sia già prenotato per altri contesti; 
3. verificare che il CRS non faccia riferimento ad un pagamento di spese giustizia; 
4. memorizzare i dati di contesto; 
5. settare il CRS in stato LOCKED; 
Nel caso i controlli terminino correttamente il servizio si occuperà di inserire il contesto del 
pagamento in questione all’interno della tabella PCT_CONTESTO relativamente al CRS passato, 
inserendo all’interno del campo stato il valore “LOCKED”. In tal caso l’output del servizio 
“prenotaCRS()” sarà l’identificativo del contesto creato, che dovrà essere utilizzato 
dall’applicazione per effettuare l’annullamento del CRS.   
Nel caso in cui i controlli presenti all’interno del metodo “prenotaCRS()” falliscano verrà ritornato 
un FAULTBEAN contenente un codice e una descrizione specifica per ogni casistica. Nella tabella 
seguente sono descritti i FAULTBEAN ritornati dal servizio prenotaCRS() nelle varie casistiche 
esaminate: 
Valore Stato restituito 
Messaggi restituiti 
all’applicazione 
Note 
CRS_RT_TIPOPAG_ERRATO 
 
“Impossibile prenotare un 
pagamento di questa 
tipologia” 
Nel caso in cui il 
CRS faccia 
riferimento ad un 
pagamento di spese 
giustizia. In quanto 
questo è un servizio 
dedicato alla 
prenotazione di 
pagamenti ad importo 
fisso. 
CRS_SCONOSCIUTO 
 
“CRS non presente” 
Nel caso in cui il 
CRS non sia presente 
all’interno della 
Base Dati del PST. 
CRS_LOCKED 
 
“CRS già prenotato” 
Nel caso in cui il 
CRS è già prenotato 
per un contesto 
differente.

CRS_RT_ANNULLATA 
 
“Pagamento già annullato” 
Nel caso in cui il 
pagamento sia già  
nello stato annullato 
(USED) 
 
A seguito dell’invocazione del servizio si possono verificare le seguenti situazioni anomale: 
1. l’applicazione effettua l’invocazione del metodo ma non riceve risposta, a esempio a causa di un 
precedente timeout all’interno di essa; 
2. l’applicazione prenota un CRS ma per non effettua successivamente l’annullamento di esso per 
cui il CRS rimarrà in stato LOCKED e nessun altra applicazione potrà “bruciarlo”; 
Per poter gestire le casistiche elencate verrà inserito un intervallo di tempo all’interno del quale il 
PST gestirà il CRS come prenotato; terminato il lasso di tempo stabilito verrà data la possibilità di 
prenotare nuovamente il CRS in questione. 
Il valore dell’intervallo di tempo di validità di una prenotazione verrà inserito sarà di default 10 
minuti e potrà essere configurabile. 
Al momento dell'invocazione del metodo "prenotaCRS()" verrà effettuato un controllo per cui: 
• se il CRS risulta prenotato con dati di contesto differenti rispetto a quelli della chiamata in 
corso e non risulta essere trascorso l'intervallo di tempo stabilito, verrà ritornato un l’errore 
per cui il CRS è già prenotato (CRS_LOCKED); 
• se il CRS risulta prenotato con gli stessi dati di contesto associati alla chiamata in corso e non 
risulta essere trascorso l'intervallo di tempo stabilito, verrà aggiornata la data di modifica del 
contesto e verrà ritornato al chiamante l’IDCONTESTO memorizzato nel sistema; 
• se il CRS risulta prenotato ed l'intervallo di tempo stabilito risulta essere trascorso, verrà 
eliminata la precedente prenotazione e ne verrà inserita una nuova per tale contesto, ritornando 
al chiamante un nuovo IDCONTESTO. 
L’oggetto “datiContesto” ha la struttura di seguito indicata. Si ricorda che il contesto deve 
permettere di individuare univocamente l’operazione di annullamento: la valorizzazione dei campi 
pertanto è stabilita dall’applicazione (i valori presenti in tabella sono da intendersi come un 
esempio): 
Input 
Descrizione 
Tipo 
Obbligato
rietà  
Note per la valorizzazione 
delle Applicazioni 
codiceServizio 
codice servizio per cui si 
annulla il pagamento 
string 
SI 
Codice del servizio per cui è 
dovuto il pagamento. 
Per esempio: PUBB, nel caso di 
pubblicazione su portale 
vendite. 
CTUISCR nel caso di 
pagamento per iscrizione albo 
CTU 
datiServizio 
valore relativo al codice 
servizio 
string 
SI 
Dati che permettono di 
individuare il servizio specifico 
all’interno del codice inserito 
nel campo precedente.

Esempio:  per PVINS, un 
eventuale identificativo della 
pubblicazione 
per CTUISCR, altro 
identificativo univoco 
dell’operazione di iscrizione 
(es: CF del CTU) 
dominio 
Dominio a cui è associato 
il pagamento 
(es. IFPV e IFAC) 
string 
SI 
Dominio applicativo che 
richiede annullamento del 
pagamento utilizzazione del 
pagamento 
Esempio: PV per portale 
vendite e ACTU per albo CTU 
gruppo 
Ufficio a cui è associato il 
pagamento 
string 
NO 
Non dovrà essere valorizzato 
stato 
Stato del contesto  
string 
NO 
Non deve essere valorizzato 
dataModifica 
Data d’inserimento del 
contesto 
date 
NO 
Non deve essere valorizzata 
utilizzatore 
Note sull’utilizzatore del 
servizio 
string 
SI 
Identificativo dell’applicazione 
chiamante 
Può coincidere, in questo caso, 
con il valore Dominio.  
 
 
RilasciaCRS 
Contestualmente al servizio di prenotazione verrà creato un servizio di “rilascio”, nel caso in cui 
un’applicazione dopo aver effettuato la prenotazione non vuole annullare il CRS ma vuole 
“sbloccare” il CRS per un successivo utilizzo. 
Verrà implementato il servizio “rilasciaCRS()”, prevedendo in input l’id del contesto, il quale si 
occuperà di rendere nuovamente prenotabile il CRS associato. Si precisa che tale servizio prevede 
in input l’id del contesto e non il CRS per poter garantire che un CRS venga rilasciato solo 
dall’applicazione che l’aveva precedentemente prenotato. 
Nel caso di esito positivo il servizio “rilasciaCRS()” ritornerà all’applicazione chiamante il CRS che 
ha ripristinato, in caso contrario verrà ritornato un FAULTBEAN contenente un codice e una 
descrizione specifica per ogni casistica. In particolare l’errore che potrà generare tale servizio è 
dovuto al fatto che non è presente il contesto indicato in input; in questo caso in servizio genererà 
il FAULTBEAN: 
Valore Stato restituito 
Messaggi restituiti 
all’applicazione 
Note 
CONTESTO_SCONOSCIUTO 
 
“Contesto non presente” 
Nel caso in cui il 
contesto specificato 
non è presente 
all’interno della 
Base Dati del PST.

AnnullaCRS 
Il  servizio “annullaCRS()” è dedicato all’annullamento dei pagamenti ad importo fisso. Tale servizio 
permetterà di “bruciare” una RT di un pagamento ad importo fisso, marcandola così come già 
utilizzata (USED) e non più utilizzabile per altri pagamenti futuri. 
Il servizio “AnnullaCRS()” sarà esposto alle applicazioni PVG e AlboCTU, le quali dovranno invocare 
l’annullamento, successivamente alla prenotazione del CRS relativo, per indicare che tale 
pagamento è già stato “utilizzato”. 
Non essendo un operazione automatica, ma dovendosi occupare l’utente di scaricare la RT da PST-
FE e caricarla nelle aree dedicate all’interno dell’applicazione, verrà implementato all’interno del 
sevizio di annullamento un controllo per garantire l’autenticità della RT caricata dall’utente stesso. 
In particolare il servizio di annullamento avrà come parametri in input l’IDCONTESTO (reperito 
dalla precedente prenotazione) e la RT per la quale viene richiesto l’annullamento. Le applicazioni 
al momento dell’invocazioni di tale metodo dovranno passare la RT inserita dall’utente che sarà 
quindi quella scaricata dal PST, indipendentemente dal fatto che sia firmata o meno. Pertanto le 
applicazioni non dovranno modificare in nessun modo la ricevuta, per esempio eliminando la firma 
(nel caso in cui sia presente), ma dovranno inoltrarla così com’è al servizio di annullamento. 
Tramite i suddetti parametri in input il servizio di occuperà di verificare se la RT caricata 
corrisponde a quella memorizzata all’interno del PST per il CRS associato al contesto indicato. La 
verifica delle ricevute che effettuerà il sistema consisterà nei seguenti passaggi: 
1. Tramite il contesto, passato in input al servizio di annullamento, il PST ricava la ricevuta 
associata ad esso presente all’interno della tabella PCT_CRS dello schema PST; 
2. Genera l’hash della RT passata in input al servizio; 
3. Genera l’hash della RT memorizzata all’interno del PST (ricavata al punto 1); 
4. Confronta l’hash delle due ricevute per verificare che siano uguali. 
Il servizio di annullamento potrà avere diversi risultati all’esito dei controlli contenuti in esso: 
• In caso di esito positivo verrà ritornato il CRS annullato; 
• Nel caso in cui la RT in input non corrisponda alla RT memorizzata nel PST per il contesto 
dato verrà restituito l’errore “La ricevuta non corrisponde al contesto indicato” 
• Nel caso in cui il contesto in input non sia presente nel DB del PST sarà restituito l’errore 
“Contesto non presente” 
Nel caso in cui tali controlli falliscano verrà ritornato un FAULTBEAN contenente un codice e una 
descrizione specifica per ogni casistica. Nella tabella seguente sono descritti i FAULTBEAN ritornati 
dal servizio annullaCRS nelle varie casistiche esaminate: 
Valore Stato restituito 
Messaggi restituiti 
all’applicazione 
Note

CONTESTO_RT_ERRATE 
 
“La ricevuta non corrisponde al 
contesto indicato” 
Nel caso in cui la RT e il 
contesto non 
corrispondano allo 
stesso pagamento. 
CONTESTO_SCONOSCIUTO 
 
“Contesto non presente” 
Nel caso in cui il 
contesto non sia 
presente all’interno della 
Base Dati del PST. 
CONTESTO_RT_ANNULLATA 
 
“Pagamento già annullato” 
Nel caso in cui il 
pagamento sia già  nello 
stato annullato (USED) 
 
Nel caso i controlli sui dati da annullare terminino correttamente il servizio si occuperà di 
aggiornare il contesto del pagamento in questione all’interno della tabella PCT_CONTESTO 
settando il campo STATO con il valore “USED”. 
 
RipristinoCRS 
Il servizio avrà in input il CRS per il quale è necessario effettuare il ripristino.  Tale servizio si 
occuperà pertanto di rendere nuovamente “disponibile” una RT di cui si era chiesto 
precedentemente l’annullamento ed era sta posta nello stato “già utilizzata”. Per rendere 
nuovamente disponibile il pagamento dovranno essere eliminati i dati del contesto, per cui 
dovranno essere eliminati i dati inseriti all’interno della tabella PCT_CONTESTO. 
All’interno del servizio “ripristinoCRS()”, prima di effettuare realmente il ripristino, verrà 
implementati vari controlli sul CRS passato in input. In particolare sarà presente: 
• il CRS in input deve far riferimento al tipo di pagamento gestito da tale servizio, in particolare 
i caratteri 7-10 al suo interno devono corrispondere ai codici di pagamento ad importo fisso 
(IFPV e IFAC) 
• il CRS deve essere stato precedentemente annullato; 
• il CRS deve essere presente all’interno della base dati del PST; 
Nel caso in cui tali controlli falliscano verrà ritornato un FAULTBEAN contenente un codice e una 
descrizione specifica per ogni casistica. Nella tabella seguente sono descritti i FAULTBEAN ritornati 
dal servizio nelle varie casistiche: 
Valore Stato restituito 
Messaggi restituiti 
all’applicazione 
Note 
CRS_TIPOPAG_ERRATO 
 
 “Il CRS fa riferimento ad una 
tipologia di pagamento non 
gestita” 
Nel caso in cui il CRS fa 
riferimento ad un 
pagamento di spese 
giustizia

CRS_DISPONIBILE 
 
  “Il CRS è già disponibile” 
 Nel caso in cui il CRS 
non risulti annullato. 
CRS_SCONOSCIUTO 
 
  “CRS non presente” 
 Nel caso in cui il CRS 
non sia presente 
all’interno della Base 
Dati del PST. 
 
Riepilogando, le interfacce esposte dal WS serviziAltriPagamenti sono: 
Metodo 
Descrizione 
prenotaCRS (String CRS, DatiContesto ctx)  
Prenota il CRS per l’annullamento, memorizzando il contesto del 
pagamento all’interno della tabella PCT_CONTESTO settando lo 
stato a “LOCKED”.  
 
Parametri in input: 
1. CRS, codice della transazione di pagamento che si vuole 
prenotare; 
2. ctx, oggetto che contiene i dati del contesto della 
prenotazione. 
 
Risultato: IDCONTESTO o un FAULTBEAN 
 
rilasciaCRS (String idContesto)  
Annulla la prenotazione di un pagamento, eliminando il contesto 
passato in input. 
 
Parametri in input: 
1. IDCONTESTO, valore ritornato dal servizio 
“prenotaCRS()”, per il quale si vuole annullare la 
prenotazione 
 
Risultato: codice CRS o un FAULTBEAN 
 
annullaCRS (String idContesto, byte[] RT)  
Annulla la Ricevuta di Pagamento marcando il pagamento come 
già utilizzato, in modo tale che non possa essere riutilizzato in un 
secondo momento. 
Verifica che la RT in input sia la stessa memorizzata sul PST 
relativamente al CRS in input.  
 
Parametri in input: 
1. IDCONTESTO, valore ritornato dal servizio 
“prenotaCRS()”; 
2. RT, ricevuta telematica che si vuole annullare. 
 
Risultato: codice CRS o un FAULTBEAN 
ripristinoCRS ( String CRS) 
Elimina tutte le informazioni di utilizzo di tale pagamento in modo 
tale che la RT risulti nuovamente disponibile e possa essere 
annullata nuovamente. 
 
Parametri in input: 
1. CRS, codice della transazione di pagamento; 
 
Risultato: codice CRS o un FAULTBEAN