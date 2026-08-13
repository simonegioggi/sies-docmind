---
uniqueName: cmdbuildeslmanualeutentev1
displayName: "CMDBuild ESL Manuale Utente v1"
category: "GENERAL"
tags: []
---

# CMDBuild_ESL_Manuale_Utente_v1

> **File originale:** `Docs_CMDBuild_SIES+SIUS_Avvocati/CMDBuild_ESL_Manuale_Utente_v1.pdf`  
> **Tipo:** PDF

---

CMDBuild ESL 
Vers.: 1.0 
Stato: Attivo 
Manuale Operativo 
 
CMDBuild_ESL_Manuale_Utente_v1 
Data riferimento 24/06/2022 
Pag. 1 di 15  
 
 
Manuale Operativo  Utente ESL 
Redatto da: 
Atanasio Roberto 
Verificato da: 
Daniele Gagliardi 
Approvato da: 
Fabio Staro Antonio Merighi 
Versione: 
1.0 
Stato: 
Attivo 
Data riferimento: 
23/05/2022 
Numero pagine: 
15 
Distribuzione: 
Nome file: 
CMDBuild_ESL_Manuale_Utente-Ata.odt

CMDBuild ESL 
Vers.: 1.0 
Stato: Attivo 
Manuale Operativo 
 
CMDBuild_ESL_Manuale_Utente_v1 
Data riferimento 24/06/2022 
Pag. 2 di 15  
Sommario 
1 
INFO DOCUMENTO ................................................................................................................................. 3 
1.1 
Scopo e contenuto del documento ...................................................................................................... 3 
1.2 
Storia degli Aggiornamenti ................................................................................................................... 3 
2 
CMDBUILD ESL .......................................................................................................................................... 4 
2.1 
Premessa .................................................................................................................................................. 4 
2.2 
Modalità di Accesso ............................................................................................................................... 4 
3 
OPERATIVITA’ ............................................................................................................................................. 5 
3.1 
Logiche comuni a tutte le schede. ........................................................................................................ 6 
3.2 
Scheda Progetto. ..................................................................................................................................... 9 
3.3 
Scheda Ambiente.................................................................................................................................... 9 
3.4 
Scheda Server ........................................................................................................................................ 10 
3.5 
Scheda Componente ............................................................................................................................ 11 
3.6 
Scheda Servizio piattaforma ............................................................................................................... 12 
3.7 
Scheda Libreria ..................................................................................................................................... 13 
3.8 
Scheda Utenze VPN ............................................................................................................................ 13 
3.9 
Scheda Portatile Sviluppatore ............................................................................................................. 14 
4 
NOTE FINALI ............................................................................................................................................ 15

CMDBuild ESL 
Vers.: 1.0 
Stato: Attivo 
Manuale Operativo 
 
CMDBuild_ESL_Manuale_Utente_v1 
Data riferimento 24/06/2022 
Pag. 3 di 15  
1 INFO DOCUMENTO 
1.1 
 SCOPO E CONTENUTO DEL DOCUMENTO 
Il documento descrive il modello dati e le procedure operative per consentire ai project manager e technical 
leader di censire le informazioni di configurazione dei propri progetti all’interno di un CMDB (Configuration 
Management DataBase) predisposto esclusivamente per questo scopo. Il prodotto utilizzato è CMDBuild 
(https://www.cmdbuild.org/it), una soluzione open source prodotta da Tecnoteca, azienda italiana del gruppo 
Zucchetti (https://www.tecnoteca.com/it). 
CMDBuild è stato installato in un server dedicato all’interno della ESL Server farm, ospitata in uno dei data 
center di Digital Hub, accessibile all’indirizzo https://production.eng.it/cmdbuild_esl/, previa autenticazione con 
le proprie credenziali aziendali (quelle utilizzate per la compilazione del RAS). La versione installata è la 3.4, 
l’ultima disponibile alla data di stesura di questo documento (https://www.cmdbuild.org/it/download/ultima-
versione). 
Le informazioni da censire costituiscono una scheda anagrafica del progetto, riguardante il cliente, il relativo 
contratto di riferimento, le principali persone coinvolte (Responsabile del contratto, Capo Progetto, Team 
Leader), gli ambienti, i server e i principali strumenti utilizzati (ad esempio repository di codice, server di 
continuous integration/continuous delivery, ecc), gli artefatti prodotti (applicazioni, web service, batch, ecc) con 
le relative dipendenze (librerie di terze parti) ed eventuali dipendenze tra artefatti. 
In dettaglio il documento contiene le informazioni di base per il censimento di nuovi: 
• 
Progetti 
• 
Ambienti 
• 
Server 
• 
Artefatti di progetto, denominati Componenti 
• 
Servizi di Piattaforma 
• 
Librerie 
• 
Utenze VPN 
• 
Portatile sviluppatore 
e come questi si relazionano tra di loro. 
Questo documento non sostituisce invece il manuale utente, del CMDBuild che è possibile invece scaricare 
in lingua italiana dal sito ufficiale del prodotto dall’url: 
https://www.cmdbuild.org/it/documentazione/manuali/user-manual. 
 
1.2 
 STORIA DEGLI AGGIORNAMENTI 
 
Versione 
Data 
Motivo 
Autore 
1.0 
23/05/2022 Prima Emissione
Roberto Atanasio

CMDBuild ESL 
Vers.: 1.0 
Stato: Attivo 
Manuale Operativo 
 
CMDBuild_ESL_Manuale_Utente_v1 
Data riferimento 24/06/2022 
Pag. 4 di 15  
2  CMDBUILD ESL 
2.1 
 PREMESSA 
CMDBuild è un sistema su cui è possibile configurare applicazioni personalizzate per l'Asset Management, 
gestendo in modo efficiente e strutturato le varie entità e le relazioni tra esse, al fine di individuare le 
dipendenze tra oggetti e persone. 
L’utilizzo dello strumento permette: 
1. L’archiviazione e consultazione delle informazioni che descrivono e riguardano i Progetti gestiti dalle ESL. 
2. Ottenere risposte immediate e organizzate a domande relative alla sua composizione ad es: 
• 
da cosa è composto? 
• 
quali librerie usa? 
• 
questa libreria in quali progetti è utilizzata? 
• 
Ecc ecc. 
2.2 
 MODALITÀ DI ACCESSO   
Al prodotto si accede dal seguente link: 
• 
https://production.eng.it/cmdbuild_esl 
 
Con l’utenza e pwd aziendale.

CMDBuild ESL 
Vers.: 1.0 
Stato: Attivo 
Manuale Operativo 
 
CMDBuild_ESL_Manuale_Utente_v1 
Data riferimento 24/06/2022 
Pag. 5 di 15  
3  OPERATIVITA’ 
All’accesso al sistema sulla spalla di sinistra si visualizzano in ordine le schede (in CMDBuild sono definite  
Classi) che l’utente dovrà compilare partendo dalla scheda “Progetto”. Andranno compilate solo quelle che 
abbiano un senso per il tuo progetto. 
 
Solitamente un Progetto può disporre, per le attività di sviluppo, test, collaudo e per i rilasci in produzione, di 
un certo numero di Ambienti e i relativi Server: un Ambiente può essere basato su uno o più Server, i quali a 
loro volta possono ospitare uno o più Componenti, così come uno o più Servizi di Piattaforma (ad esempio un 
API gateway) e così via. I vincoli  tra le classi attualmente configurati verranno indicati scheda per scheda. Per 
maggior chiarezza, di seguito vengono riportate anche le schede visualizzate e configurate dai soli 
amministratori del sistema. 
• 
Cliente 
• 
Mercato 
• 
Impiegato 
 
Attenzione: nel caso in cui si riscontrasse la necessità di introdurre nuovi attributi in tali schede, o si avessero 
problemi d’accesso allo strumento, o si avesse bisogno di supporto (ad esempio per caricamenti massivi di 
dati tipo le librerie di terze parti) ti invitiamo ad aprire una segnalazione in Jira sul progetto Supporto Servizi 
Comuni (ALMESL) utilizzando il link: 
https://production.eng.it/jira/secure/CreateIssue.jspa?pid=12290&issuetype=26 
che apre direttamente in Jira il modulo per l’inserimento della richiesta. Si ricorda che nel campo “Componente” 
la voce da selezionare dovrà essere CMDBuild. 
Nel caso si richieda il caricamento massivo di dati, questi dovranno essere allegati alla richiesta nel formato 
CSV. Nel caso di caricamenti massivi di librerie (l’attuale configurazione prevede tre colonne, rispettivamente  
il GroupId una sorta di contenitore logico delle singole librerie, il Nome della libreria e la Versione; se non avete 
il concetto di GroupId, potete mettere il contenitore in cui quella libreria si trova ad esempio 'framework 
Dot.NET 4') invece, è possibile in alternativa al file CSV allegare il file utilizzato dal proprio sistema di build 
(per esempio per i progetti Java Maven il file pom.xml).

CMDBuild ESL 
Vers.: 1.0 
Stato: Attivo 
Manuale Operativo 
 
CMDBuild_ESL_Manuale_Utente_v1 
Data riferimento 24/06/2022 
Pag. 6 di 15  
3.1 
 LOGICHE COMUNI A TUTTE LE SCHEDE. 
Selezionando la voce “Progetto” nel menù di sinistra, si apre l’elenco di tutte le schede progetto già censite 
nel sistema. Selezionando un progetto, ne viene visualizzato il dettaglio, suddiviso in diverse sezioni. La prima 
sezione, denominata “Scheda” (ottenibile cliccando sull’icona con tooltip “apri scheda” come evidenziato in 
Figura 1), è composta da varie sotto-sezioni che ne rendono più agevole la lettura del contenuto. In particolare 
è presente una sezione “Note” con eventuali informazioni aggiuntive non strutturate, ma ugualmente 
significative, e una prima panoramica delle relazioni più significative con altre schede. Le icone a destra 
permettono di: 
• 
visualizzare la scheda 
• 
entrare in modifica della stessa 
• 
cancellarla 
• 
clonarla 
• 
visualizzare graficamente le relazioni con altre schede 
• 
stamparla 
 
A seguire troviamo altri 6 Tab Dettagli, Note, Relazioni, Storia, Email, Allegati che vengono resi disponibili 
anche entrando in visualizzazione sulla spalla sinistra della singola scheda. 
Figura 1 - Scheda dettaglio progetto

CMDBuild ESL 
Vers.: 1.0 
Stato: Attivo 
Manuale Operativo 
 
CMDBuild_ESL_Manuale_Utente_v1 
Data riferimento 24/06/2022 
Pag. 7 di 15  
 
Il secondo Tab “Dettagli” permette di visualizzare quanto già presente a livello di relazioni (solo quelle 
“navigabili”) con altre schede con la possibilità di aggiungerne di nuove generando in automatico la relazione 
tra la scheda di partenza e quella nuova. In Figura 3 possiamo notare che l’ambiente di sviluppo del progetto 
SIT MP ha già una relazione con la scheda “Server” dove è stato definito il server “plutone” collegamento 
visibile perché sulla spalla di destra siamo posizionati proprio sul quel tipo di collegamento. Nello stesso modo 
in alto a sinistra si attiva il Tab “Aggiungi dettaglio Server” da cui agire per censire una nuova scheda. 
 
La stessa logica si replica per tutti i tipi di collegamento presenti sulla spalla di sinistra per quella scheda. 
 
 
Figura 2 - Scheda di dettaglio con le azioni possibili sulla sinistra 
Figura 3 - Dettaglio relazione "Server" 
Figura 4 - Dettaglio relazione "Servizi di Piattaforma"

CMDBuild ESL 
Vers.: 1.0 
Stato: Attivo 
Manuale Operativo 
 
CMDBuild_ESL_Manuale_Utente_v1 
Data riferimento 24/06/2022 
Pag. 8 di 15  
I successivi Tab “parlanti” elencati in precedenza rimandano a sezioni che contengono se presenti tali 
informazioni. Come punto di attenzione nel Tab “Relazioni” si visualizzano tutte quelle presenti per quella 
scheda. E’ sempre possibile agire ove il vincolo lo permetta, in visualizzazione, modifica o cancellazione della 
relazione e per le sole previste entrare in modifica della scheda collegata tra quelle già in essere. 
 
Eventuali nuove relazioni possono essere attivate dal Tab “Aggiungi relazioni” tra quelle disponibili per quella 
tipologia di scheda e secondo la cardinalità 1:N o N:N definite. 
 
Nei paragrafi successivi le indicazioni per ogni scheda prevista date da: 
1. un‘immagine che visualizza i vari campi che la compongono. Tutti i campi contrassegnati con 
l’asterisco sono obbligatori; sono presenti anche campi chiave in sola lettura che si compilano in 
automatico. Esistono inoltre campi che si visualizzano in base a risposte date su altri campi. 
2. una tabella dove vengono riportate in dettaglio, se presenti, le relazioni con le altre schede. Tali 
relazioni sono suddivise tra quelle “navigabili” dal Tab “Dettagli”(individuabili dallo sfondo verde) e 
l’insieme visibile tutte dal Tab “Relazioni”. 
 
Figura 5 - Dettaglio delle relazioni di una scheda progetto 
Figura 6 - Relazioni possibili con la scheda progetto

CMDBuild ESL 
Vers.: 1.0 
Stato: Attivo 
Manuale Operativo 
 
CMDBuild_ESL_Manuale_Utente_v1 
Data riferimento 24/06/2022 
Pag. 9 di 15  
3.2 
SCHEDA PROGETTO. 
La scheda Progetto è il dato principale. Essa permette di censire le principali informazioni anagrafiche di 
progetto, tra cui i referenti principali, interni ed esterni. Le sue relazioni con le altre schede permettono di avere 
di ogni progetto una visione completa di tutti gli aspetti. 
 
Nello specifico la scheda Progetto si relaziona con le altre schede secondo questo tipo di relazioni: 
Scheda 1
Scheda 2
Descrizione Diretta
Descrizione Inversa
Cardinalità
Impiegato 
Progetto 
Responsabile contratto 
Ha responsabile contratto 
1:N 
Impiegato 
Progetto 
Capo progetto di 
Ha capo progetto 
1:N 
Impiegato 
Progetto 
Team leader di 
Ha team leader 
1:N 
Mercato 
Progetto 
Ha progetto 
Per mercato 
1:N 
Cliente 
Progetto 
Ha progetto 
E' del cliente 
1:N 
Progetto 
Ambiente 
Dispone di ambienti 
Usato per progetto 
1:N 
Progetto 
Utenze VPN 
Fa uso di 
E' usata per 
1:N 
 
3.3 
SCHEDA AMBIENTE 
La scheda ambiente ha lo scopo di modellare di diversi ambienti utilizzati da un progetto per le proprie 
attività di sviluppo, test, collaudo ed esercizio (produzione). 
Figura 7 - Scheda “Progetto”

CMDBuild ESL 
Vers.: 1.0 
Stato: Attivo 
Manuale Operativo 
 
CMDBuild_ESL_Manuale_Utente_v1 
Data riferimento 24/06/2022 
Pag. 10 di 15  
 
Questa scheda si relaziona con le altre schede secondo questo tipo di relazioni: 
Scheda 1
Scheda 2
Descrizione Diretta
Descrizione Inversa
Cardinalità
Progetto 
Ambiente 
Dispone di ambienti 
Usato per progetto 
1:N 
Ambiente 
Componente 
Ospita 
E’ installato in 
1:N 
Ambiente 
Server 
Utilizza server 
Utilizzato in ambiente 
1:N 
Ambiente 
Servizio Piattaforma Ospita 
E’ ospitato in 
1:N 
 
3.4 
SCHEDA SERVER 
La scheda server permette di modellare gli eventuali server che definiscono i diversi ambienti (ogni ambiente 
sarà caratterizzato dall’avere uno o più server in cui sono rilasciati i diversi artefatti o componenti di progetto 
e le relative librerie. 
 
Figura 8 - Scheda “Ambiente”

CMDBuild ESL 
Vers.: 1.0 
Stato: Attivo 
Manuale Operativo 
 
CMDBuild_ESL_Manuale_Utente_v1 
Data riferimento 24/06/2022 
Pag. 11 di 15  
 
La scheda Server si relaziona con le altre schede secondo questo tipo di relazioni: 
Scheda 1
Scheda 2
Descrizione Diretta
Descrizione Inversa
Cardinalità
Ambiente 
Server 
Utilizza server 
Utilizzato in ambiente 
1:N 
Portatile sviluppatore Server 
Si connette a 
Acceduto da 
N:N 
Componente 
Server 
E’ installato 
Ospita 
N:N 
 
3.5 
SCHEDA COMPONENTE 
La scheda Componente permette di rappresentare gli artefatti di progetto (librerie, applicativi, web service, 
processi batch, stored procedure, ecc). Risulta essere legata univocamente con il relativo ambiente, in modo 
da modellare correttamente la situazione secondo cui in ogni ambiente risultano di volta in volta installate 
versioni diverse di uno stesso Componente (in sviluppo ci sarà una versione, o “build”, che solitamente sarà 
diversa dalla versione installata in collaudo o in produzione). Ciò significa che, se per il proprio progetto si è 
deciso di tracciare più ambienti, sarà necessario replicare il censimento dei propri componenti per ogni 
ambiente tracciato. L’obbligatorietà del campo “Ambiente” supporta questa stretta relazione. Inoltre, come si 
vedrà, il codice del componente è costruito dinamicamente dal sistema durante il censimento, 
giustapponendo il nome del componente al nome dell’ambiente. È naturalmente sempre possibile cambiare 
l’associazione di un componente e del relativo ambiente: il sistema provvederà ad aggiornare il codice, 
modificandolo con il nuovo ambiente. 
Il censimento di diverse occorrenze di uno stesso componente su più ambienti è agevolato dalla funzione 
nativa di clonazione di CMDBuild, che rende dunque molto meno gravosa la corretta modellazione del 
binomio componente-ambiente. 
 
Figura 9 - Scheda “Server”

CMDBuild ESL 
Vers.: 1.0 
Stato: Attivo 
Manuale Operativo 
 
CMDBuild_ESL_Manuale_Utente_v1 
Data riferimento 24/06/2022 
Pag. 12 di 15  
 
La scheda Componente si relaziona con le altre schede secondo questo tipo di relazioni: 
Scheda 1
Scheda 2
Descrizione Diretta
Descrizione Inversa
Cardinalità
Ambiente 
Componente 
Ospita 
E’ installato in 
1:N 
Componente 
Server 
Utilizza 
E’ utilizzata da 
N:N 
Componente 
Libreria 
E’ installato in 
Ospita 
N:N 
Componente 
Componente 
Utilizza 
E’ utilizzato da 
N:N 
Come si può vedere, è possibile anche censire interdipendenze tra i di versi componenti di progetto. 
 
3.6 
SCHEDA SERVIZIO PIATTAFORMA 
Questa scheda permette di censire eventuali servizi di piattaforma (ad esempio un API Gateway) installati 
sui server che a loro volta costituiscono i diversi ambienti. 
 
 
Questa scheda si relaziona con le altre schede secondo questo tipo di relazioni: 
Figura 10 - Scheda "Componente" 
Figura 11 - Scheda "Servizio di Piattaforma"

CMDBuild ESL 
Vers.: 1.0 
Stato: Attivo 
Manuale Operativo 
 
CMDBuild_ESL_Manuale_Utente_v1 
Data riferimento 24/06/2022 
Pag. 13 di 15  
 
Scheda 1
Scheda 2
Descrizione Diretta Descrizione Inversa Cardinalità
Ambiente 
Servizio Piattaforma 
Ospita 
E’ ospitato in 
1:N 
Portatile Sviluppatore Servizio Piattaforma 
Acceda a 
Acceduto da 
N:N 
 
3.7 
SCHEDA LIBRERIA 
Questa scheda permette di censire le eventuali dipendenze da librerie di terze parti (open source o 
proprietarie) utilizzate dai diversi componenti di progetto. 
Nota: per caricamenti massivi vedi “Attenzione” nel paragrafo Operatività    
 
 
Questa scheda si relaziona con le altre schede secondo questo tipo di relazioni: 
 
Scheda 1
Scheda 2
Descrizione Diretta Descrizione Inversa Cardinalità
Componente 
Libreria 
Utilizza 
E’ utilizzata da 
N:N 
3.8 
SCHEDA UTENZE VPN 
Questa scheda permette di tracciare le eventuali utenze VPN fornite dal cliente per l’accesso, tramite una 
propria VPN, agli eventuali ambienti utilizzati dal progetto. 
 
 
Questa scheda si relaziona con le altre schede secondo questo tipo di relazioni: 
 
Figura 12 - Scheda "Libreria" 
Figura 13 - Scheda "Utenza VPN"

CMDBuild ESL 
Vers.: 1.0 
Stato: Attivo 
Manuale Operativo 
 
CMDBuild_ESL_Manuale_Utente_v1 
Data riferimento 24/06/2022 
Pag. 14 di 15  
Scheda 1
Scheda 2
Descrizione Diretta Descrizione Inversa Cardinalità
Impiegato 
Utenze VPN 
Utilizza 
E’ utilizzato da 
1:N 
Progetto 
Utenze VPN 
Fa uso di Utenze VPN E’ usata per progetto 
1:N 
 
3.9 
SCHEDA PORTATILE SVILUPPATORE 
In questa scheda NON intendiamo riportare le configurazioni di tutti i portatili di tutti gli sviluppatori che 
lavorano al progetto. In questa scheda vogliamo riportare la configurazione standard del portatile di uno 
sviluppatore se questo portatile è parte integrante dell'ambiente che stiamo descrivendo. Ad esempio solo se 
sui portatili degli sviluppatori gira l'application server e questo si collega ad un DB presso il cliente o presso i 
nostri data center, allora il portatile, con il suo application server, è parte integrante dell'ambiente e va 
descritto. Altro esempio è se il portatile si connette via VPN agli ambienti del cliente (database, api gateway). 
 
 
Questa scheda si relaziona con le altre schede secondo questo tipo di relazioni: 
 
Scheda 1
Scheda 2
Descrizione Diretta Descrizione Inversa Cardinalità
Portatile Sviluppatore Server 
Si connette a 
Acceduto da 
N:N 
Portatile Sviluppatore Servizio Piattaforma 
Accede a 
Acceduto da 
N:N 
 
 
 
Figura 14 - Scheda Portatile Svilppatore

CMDBuild ESL 
Vers.: 1.0 
Stato: Attivo 
Manuale Operativo 
 
CMDBuild_ESL_Manuale_Utente_v1 
Data riferimento 24/06/2022 
Pag. 15 di 15  
 
4 NOTE FINALI 
 
Per ulteriori informazioni si rimanda alla documentazione ufficiale di CMDBuild reperibile al link: 
https://www.cmdbuild.org/it/documentazione/manuali