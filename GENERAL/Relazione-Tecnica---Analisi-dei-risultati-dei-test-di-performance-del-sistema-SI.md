---
uniqueName: relazione-tecnica-analisi-dei-risultati-dei-test-d
displayName: "Relazione Tecnica   Analisi dei risultati dei test di performance del sistema SI"
category: "GENERAL"
tags: []
---

# Relazione Tecnica - Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio 2019

> **File originale:** `MEV/SCHEDA_006/ATTIVITA_JMETER/_x_Julio/Relazione Tecnica - Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio 2019.pdf`  
> **Tipo:** PDF

---

Analisi dei risultati dei test di
performance del sistema SIES
del 23 Gennaio 2019
Relazione Tecnica
Dipartimento di Ingegneria Informatica, Automatica e
Gestionale “Antonio Ruberti” – Sapienza, Università di
Roma

Sommario
1
Scopo del documento...................................................................................................2
2
Descrizione del Sistema...............................................................................................2
3
Descrizione dei Test eseguiti.......................................................................................4
4
Analisi dei Risultati del Test.......................................................................................11
5
Conclusioni.................................................................................................................21
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 1

1 Scopo del documento
Questo documento descrive la metodologia ed i risultati dell’analisi effettuata dal gruppo di
lavoro Sapienza relativamente ai risultati dei test effettuati sul sistema SIES del distretto di
Napoli in data 23 Gennaio 2019.
Lo  scopo  dei  test  era  quello  di  verificare  il  corretto  funzionamento  e  la  capacità  di
sopportare un carico di lavoro di crescente intensità da parte del sistema SIES (ver.
11.1.2), caratterizzato dalle componenti hardware e software installate presso il distretto di
Napoli e presso il sistema centrale. A tale scopo un carico di lavoro eterogeneo è stato
appositamente generato per simulare l’attività degli utenti agli uffici del distretto di Napoli e
degli avvocati con il fine di osservare la risposta, in termini prestazionali, del sistema al
variare del numero di utenti concorrenti, così come l’impatto che questo poteva avere sia
sui tempi delle risposte agli utenti stessi che sulle percentuali degli errori riportati dagli
strumenti di test.
Va comunque precisato che, mentre il carico di lavoro degli utenti agli uffici del distretto di
Napoli è stato generato basandosi sull’osservazione della reale attività di quest’ultimi per
mezzo di un’analisi svolta sui file di Log collezionati durante due giornate di utilizzo del
sistema in pre-esercizio, per quanto riguarda il carico di lavoro degli avvocati non è stato
possibile  fare  una  stima  di  quello  che  poteva  venire  ad  essere  il  reale  livello  di
concorrenza, ed è stato quindi scelto di far variare gradualmente il numero di utenti
concorrenti partendo da un unico avvocato nel sistema fino al raggiungimento di un valore
che ritenevamo adeguato per stressare il sistema.
2 Descrizione del Sistema
Per simulare gli utenti abbiamo utilizzato due macchine virtuali in esecuzione su altrettante
macchine reali predisposte agli uffici della Direzione Generale per i Sistemi Informativi
Automatizzati (D.G.S.I.A) del Ministero della Giustizia appositamente per eseguire i test.
Entrambe le macchine virtuali erano a loro volta equipaggiate della stessa versione dello
strumento Apache JMeter per poter generare indipendentemente le richieste da parte
degli utenti agli uffici al distretto di Napoli e le richieste da parte degli avvocati.
Altre due macchine virtuali predisposte al distretto di Napoli e configurate mantenendo le
medesime  caratteristiche  hardware  e  software  dell’attuale  ambiente  di  pre-esercizio,
ospitavano invece l’applicazione SIES distrettuale.
Nel dettaglio ci riferiamo ad una prima macchina virtuale dotata dell’installazione di una
istanza  dell’Appliation  Server JBoss  conforme  alle  specifiche  Java  EE,  su  cui  viene
eseguita l’applicazione SIES distrettuale che a sua volta si appoggia sia sul framework
Apache Spring per l’implementazione del paradigma di programmazione MVC (model-
view-control) utile per la gestione ed il soddisfacimento delle richieste in ingresso, sia sul
framework MyBatis per l’interfacciamento con le risorse del Database.
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 2

La seconda macchina virtuale era invece dotata dell’istallazione di una istanza del DBMS
Oracle  Database  contenente  lo  schema,  le  tabelle  ed  i  dati  del  database  del  SIES
distrettuale.
In termini di risorse hardware i suddetti server sono così equipaggiati.
Server
Numero CPU
Quantità Memoria
AP
4
12
DB
4
16
In Figura 1 viene riportato il diagramma architetturale complessivo.
Possiamo  osservare  come  l’interazione  degli  avvocati  con  il  sistema  SIES  passa
necessariamente  per  il  sistema  centrale,  il  quale  mette  a  disposizione  il  servizio  di
autenticazione degli utenti (proxy PST) che comunica con il Sistema di Consultazione dei
Procedimenti che a sua volta agisce da gateway per le richieste inoltrate dagli avvocati in
maniera coerente a quanto riportato nel documento di Analisi Funzionale “Sistema per la
Consultazione, da parte degli Avvocati, dei Procedimenti di Sorveglianza” (cod. SIGI-PNL-AF,
ver. 2.1, 30/11/2016) redatto dal fornitore Engineering.
Diversamente,  le  credenziali  degli  utenti  agli  uffici  del  distretto  di  Napoli  sono  già
accreditate al sistema SIES distrettuale e quindi sufficienti ad abilitare l’inoltro diretto delle
richieste una volta stabilita la connessione al sistema.
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 3
Figura 1 - Architettura del sistema

3 Descrizione del Test eseguiti
I suddetti test sono stati eseguiti utilizzando due istanze dello strumento Apache JMeter al
fine di simulare in maniera indipendente il carico di lavoro degli utenti agli uffici del distretto
di Napoli e degli avvocati. In entrambe le istanze, ognuna delle quali installata su una
differente macchina virtuale, ad ogni istante di tempo erano inviate le richieste da parte di
un determinato numero di utenti concorrenti dipendentemente dal tempo di inizio delle
rampe degli accessi per le due tipologie di utenti, dalla durata delle rampe e dal valore
massimo impostato per queste due. Ognuno dei suddetti utenti selezionava la successiva
azione da eseguire da una delle varie sequenze predefinite di azioni in accordo ad una
distribuzione di probabilità che è stata definita sul carico di lavoro.
In particolare, ogni avvocato simulato eseguiva la seguente sequenza di azioni

Ricerca per Estremi Procedimento

a seconda del risultato della ricerca
◦Dettaglio Ordinanza
◦Dettaglio Decreto
◦Dettaglio Rinvio Udienza

Ricerca per Estremi Procedimento

Stampa Procedimento

Accesso Dati Soggetto
per le quali sono stati scelti dei valori di think-time basati su una stima calcolata a partire
dalla misurazione dei tempi registrati durante la simulazione della navigazione effettuata
manualmente da personale esperto della logica di business applicativa. La distribuzione
scelta a valle dell’osservazione e successiva computazione dei valori delle media e delle
deviazioni standard è quella normale, i cui parametri sono mostrati qui di seguito.
Azione
Media (sec.)
Varianza (sec.)
Ricerca per Estremi Procedimenti
12
2
Dettaglio Ordinanza
Dettaglio Decreto
Dettaglio Rinvio Udienza
25
8
Ricerca per Estremi Procedimenti
15
5
Stampa Procedimento
5
2
Accesso Dati Soggetto
5
2
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 4

Per  quanto  riguarda  la  simulazione  degli  utenti  agli  uffici  del  distretto  di  Napoli,  le
sequenze di azioni da far eseguire in corrispondenza delle richieste inoltrate da questa
tipologia di utenti sono state fornite dal GdL di Napoli. Ci riferiamo ad 11 sequenze di
azioni con differente probabilità di venir selezionate dagli utenti simulati, e che sono state
indicate dal GdL di Napoli come maggiormente rappresentanti la loro attività.
Dunque, insieme al responsabile al D.G.S.I.A che ha coordinato le attività, è stato deciso
di  eseguire  un’analisi  diretta  su  due  file  di  Log  raccolti  in  due  giornate  di  normale
operatività degli utenti agli uffici del distretto di Napoli con l’obiettivo di individuare i valori
di  think-time da  associare  alle  azioni  incluse  nelle  suddette  sequenze  per poter poi
configurare gli script di test in maniera tale da simulare con un certo livello di affidabilità il
carico di lavoro generato da questi utenti.
In tale senso il gruppo di lavoro Sapienza ha prodotto la relazione tecnica con titolo
“Profilazione  dell’attività  degli  utenti  del  sistema  SIES  del  distretto  di  Napoli  ed
identificazione dei valori di think-time” in cui è ampiamente argomentata e motivata la
metodologia adottata per l’estrazione di tali valori partendo dalle informazioni contenute
nei file di Log.
Nella tabella che segue sono riportati i valori di think-time associati alle azioni contenute
nelle sopra citate 11 sequenze che sono stati potuti essere estratti a partire dall’analisi
effettuata sui file di Log. Dobbiamo infatti precisare che non per tutte le azioni coinvolte è
stato  possibile  individuare  i  relativi  valori  di  think-time per  mezzo  della  metodologia
documentata nella suddetta relazione, e per alcune di esse è stato possibile solo calcolare
un’approssimazione (indicato con il simbolo ~ come prefisso al valore stimato) adottando
una metodologia differente da quella proposta, mentre per altre azioni ancora non è stato
possibile estrapolare alcun tipo di informazione in merito (indicato ponendo il simbolo X).
Sequenza
Azione
Media (sec.)
1
Login
–
Load Ricerca Fascicolo
58.58
Azione Chiamante Ricerca Fascicolo
~ 88,06
Logout
X
2
Login
–
Load Ricerca Fascicolo
58.58
Ricerca Fascicolo
~ 88.06
Logout
~ 55.18
3
Login
–
Load Ricerca Fascicolo per Soggetto
48.77
Ricerca Fascicolo per Soggetto
73.65
Logout
~ 21.98
Login
–
Load Orizontal Menu
35.57
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 5

4
Load Orizontal Menu
9.71
Load Inserisci Sospensione Esec Pena Disp Pm
1.24
Load Fascicolo in Sessione
~ 192.92
Inserisci Sospensione Esec Pena Disp Pm
X
Logout
X
5
Login
–
Load Orizontal menu
35.57
Load Orizontal Menu
9.71
Load Inserisci Ordine Esecuzione
1.33
Load Fascicolo in Sessione
~ 5.26
Inserisci Ordine Esecuzione
X
Logout
X
6
Login
–
Load Orizontal Menu
35.57
Load Orizontal Menu
9.71
Load Orizontal Menu
9.71
Load Inserisci Ordine Esecuzione Simeone
1.08
Load Fascicolo in Sessione
~ 24.73
Inserisci Ordine Esecuzione Simeone
X
Logout
X
7
Login
–
Load Orizontal Menu
35.57
Griglia Decisioni Sorveglianza
4.00
Misura Alternativa Griglia Sem Lib
~ 8.98
Load Fascicolo in Sessione
X
Load Inserisci MA Semiliberta
X
Load Ricerca Comune Tds
X
Load Lista Istituto Detenzione
37.50
Lista Istituto
0.99
Lista Istituto Detenzione Filtro Tipo
~ 32.38
Load Lista CSSA Filtro Comune
X
Lista CSSA Filtro Comune
~ 52.77
Load Lista UDS
X
Load Ricerca Comune Tds
12.69
Load Ricerca Comune
34.46
Load Lista Prov
1.13
Load Provincia Comune
~ 25.40
Visualizza Comuni
X
Inserisci Concessioni
X
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 6

Logout
X
8
Login
–
Load Orizontal Menu
35.57
Griglia Decisioni Sorveglianze
4.00
Load Inserisci Liberazione Anticipata
4.30
Load Fascicolo in Sessione
~ 21.24
Load Ricerca Comune Tds
X
Inserisci Liberazione Anticipata
~ 59.43
Calcolo Pena Liberazione Anticipata
X
Load Lista Istituto Detenzione
X
Lista Istituto
0.99
Lista Istituto Detenzione Filtro Tipo
~ 32.38
Load Ricerca Comune Tds
X
Inserisci OS Liberazione Anticipata
~ 59.43
Stampa OS Liberazione Anticipata
X
Stampa OS Liberazione Anticipata
60.00
Upload OS Lib Ant
~ 117.60
Dettaglio OS Liberazione Anticipata
X
Logout
~ 148.74
9
Login
–
Load Orizontal Menu
35.57
Load Orizontal Menu
9.71
Load Ricerca Fascicolo
55.99
Ricerca Fascicolo
~ 88.06
Logout
~ 53.18
10
Login
–
Load Orizontal Menu
35.57
Load Orizontal Menu
9.71
Load Ricerca Fascicolo
55.99
Ricerca Fascicolo
~ 88.06
Load Dettaglio Fascicolo
15.23
Load Inserisci Fasciolo
2.03
Load Lista Ogetti
26.80
Inserisci Fasciolo
~ 57.25
Load Orizontal Menu
X
Load Orizontal Menu
9.71
Load FSP Fissazione Udienza
0.99
Load Inserisci Fissazione Udienza
27.99
Load Inserisci Avvocato
14.44
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 7

Load Ricerca Avvocato
6.46
Filtra Avv
0.99
Ricerca Avvocato
~ 63.15
Inserisci Avvocato
X
Load Inserisci Fissazione Udienza
X
Load Ricerca Udienza X Procedimenti
1.97
Elenco Udienze Da Data
~ 117.43
Elenco Udienze Da Data
X
Load Inserisci Udienza
X
Inserisci Udienza
~ 43.72
Load Inserisci Fissazione Udienza
X
Load Ricerca Comune
11.19
Load Lista Prov
1.13
Load Provincia Comune
~ 25.40
Visualizza Comuni
X
Inserisci Fissazione Udienza
X
Load Orizontal Menu
X
Load Orizontal Menu
9.71
Load FSP Emissione Ordinanza UDS
2.95
Load Emissione Ordinanza UDS
~ 58.36
Load Inserisci Magistrato Relatore
~3.96
Load Ricerca Magistrato Lista
3.77
Ricerca Magistrato Lista
~ 28.22
Inserisci Magistrato Relatore
X
Load Emissione Ordinanza UDS
X
Inserisci Emissione Ordinanza UDS
~ 56.96
Inserisci Ordinanza UDS
X
Logout
X
11
Login
–
Load Orizontal Menu
35.57
Load Orizontal Menu
9.71
Load Ricerca Fascicolo SIEP
3.33
Ricerca Fascicolo SIEP
~ 221.69
Load Inserisci Fascicolo
X
Load Ricerca Magistrato Assegnazione Lista
~ 65.86
Load Lista Mag
0.99
Ricerca Magistrato Assegnazione Lista
~ 24.19
Inserisci Fasicolo
X
Load Dettaglio Oggetti Richiesta
X
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 8

Load Lista Oggetti Sige Per Contenuto
37.92
Load Lista Titoli Esecutivi Sige
11.37
Inserisci Oggetto Richiesta
10.75
Load Dettaglio Oggetto Richiesta
61.41
Load Dettaglio Fascicolo
4.52
Load Inserisci Avvocato
30.97
Load Ricerca Avvocato
6.46
Filtra Avv
0.99
Ricerca Avvocato
~ 63.15
Inserisci Avvocato
X
Load Dettaglio Fascicolo
X
Load F Sige P Fissazione Udienza
~ 63.63
Load Inserisci Udienza Monocratica Sige
194.90
Inserisci Udienza Monocratica Sige
~ 61.89
Inserisci Fissazione Udienza
X
Upload Fissazione Udienza
X
Upload Document
X
Load Dettaglio Fissazione Udienza
X
Load Orizontal Menu
94.43
Load Orizontal Menu
9.71
Load FSP Emissione Ordinanza
2.83
Inserisci Emissione Ordinanza
~ 22.91
Load Modifca Esiti
X
Inserisci Esiti
44.91
Dettaglio Ordinanza
4.47
Upload Document
~ 12.83
Upload Document
X
Dettaglio Ordinanza
X
Load Inserisci Data Deposito
2.76
Inserisci Data Deposito
~ 34.39
Upload Documento Allegato
X
Load Dettaglio Data Deposito
X
Logout
~ 4.17
Per tutte le azioni cui non è stato possibile estrarre dei valori di  think-time per mezzo
dell’analisi effettuata a partire dalle informazioni contenute nei file di Log, il fornitore
insieme  al  coordinatore  delle  attività  al  D.G.S.I.A  hanno  provveduto  ad  eseguire
manualmente la simulazione della navigazione di un utente in maniera tale da individuare
empiricamente una stima di quello che potesse essere il valore di think-time. Al gruppo di
lavoro Sapienza non sono stati comunque passati i risultati di tale simulazione che è stata
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 9

effettuata a valle dell’avvenuta validazione degli script di test. Dunque non verranno inclusi
in questo documento.
Il test ha avuto una durata complessiva di tre ore, dalle 12:45 alle 15:45, durante la quali è
stato scelto di attivare le rampe degli accessi degli utenti agli uffici del distretto di Napoli e
degli avvocati in maniera disgiunta, tale da portare il sistema a lavorare sotto differenti
distribuzioni del carico di lavoro da parte di questi utenti. Più precisamente si voleva far
partire la rampa degli accessi degli avvocati quando erano già attivi un certo numero
(carico medio, e non di punta, osservato per mezzo dell’analisi svolta sui file di Log) di
utenti agli uffici del distretto di Napoli concorrenti.
Durante le prime due ore, dalle 12:45 alle 14:45, era attiva la rampa degli accessi degli
utenti agli uffici del distretto di Napoli fino al raggiungimento di un numero di accessi
concorrenti pari a 100, numero che rappresenta il valore di punta delle sessioni utente
concorrenti osservate per mezzo dell’analisi effettuata sui file di Log. Durante l’ultima ora
di test, dalle 14:45 alle 15:45, il livello di concorrenza di questi utenti rimaneva costante e
pari a tale valore massimo.
Allo scadere della prima ora, e per tutta la durata della successiva seconda ora di test che
va  dalle  13:45  alle  14:45,  era  attiva  la  rampa  degli  accessi  degli  avvocati  fino  al
raggiungimento di un valore massimo pari a 1000 che è stato mantenuto fisso durante
l’ultima ora di test che va dalle 14:45 alle 15:45. Come già menzionato, non essendo noto
il valore massimo da utilizzare per configurare la rampa di questi utenti, questo è stato
scelto  ipotizzando  che potesse essere un  valore sufficientemente elevato  da portare
gradualmente il sistema a lavorare in condizioni di alto carico e di saturazione dell’utilizzo
delle risorse.
In Figura 2 riportiamo in scala logaritmica il grafico con le funzioni di attivazione e crescita
delle rampe nel tempo per le due diverse tipologie di utenti.
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 10
Figura 2 - Numero di utenti agli ufci e numero di avvocati concorrenti

4 Analisi dei Risultati del Test
Nelle Figure 3 e 4 sottostanti riportiamo i grafici generati dalle due istanze dello strumento
Apache JMeter relativi al numero di threads attivi nel tempo.
Le due rampe mostrate sopra coprono intervalli di tempo differenti. Più precisamente il
grafico in Figura 4 dovrebbe essere propriamente scalato in maniera tale da poter essere
allineato  temporalmente  con  il  grafico  in  Figura  3.  Possiamo  comunque  facilmente
osservare, prestando attenzione all’orario riportato sull’asse delle ascisse in entrambi i
grafici, come i valori delle due rampe prodotte dallo strumento Apache JMeter a runtime
siano coerenti con i valori delle rampe riportati in Figura 2, a dimostrazione della corretta
configurazione delle rampe degli accessi di entrambe le tipologie di utenti coinvolti nel test.
Andiamo  ora  ad  analizzare  il  comportamento  del  sistema  in  funzione  del  crescente
numero  di  utenti  concorrenti  osservando  per  prima  cosa  l’utilizzazione  delle  risorse
hardware  nelle  due  macchine  virtuali  predisposte  al  distretto  di  Napoli  per  ospitare
l’applicazione SIES distrettuale.
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 11
Figura 3 - Treads associati agli utenti agli ufci del distretto di Napoli
Figura 4 - Treads associati agli avvocati

In Figura 5 sono riportati l’utilizzo della CPU e l’occupazione della memoria fisica della
macchina virtuale su cui è in esecuzione l’Application Server, mentre in Figura 6 sono
riportati l’utilizzo della CPU e l’occupazione della memoria fisica della macchina virtuale su
cui è in esecuzione il Database Server.
Possiamo  osservare  in  Figura  6  come  la  memoria  fisica  del  Database  Server  sia
completamente  occupata  già  prima  dell’inizio  del  test.  Questo  non  è  da  attribuirsi
necessariamente ad una condizione di saturazione della memoria del Database Server,
ma  potrebbe  dipendere  dalla  politica  di  allocazione  dei  buffer  cache  nella  memoria
centrale che è stata scelta per configurare il DB Oracle, il quale tra le varie opzioni offre
anche la possibilità di indicare la quantità di spazio da allocare e mantenere in memoria
centrale. Insieme a questo, vi è poi la possibilità che la macchina virtuale ospitante il
Database Server non sia stata riavviata prima di aver dato inizio al test, lasciando così la
memoria  centrale  completamente  occupata  dai  dati  mantenuti  nei  buffer  cache  del
precedente  utilizzo.  Non  potendo  comunque  inferire  alcunché  sul  reale  utilizzo  della
memoria di questa macchina virtuale tale informazione è stata omessa dal processo di
analisi.
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 12
Figura 5 - Utilizzo della CPU e della Memoria dell'Application Server nel tempo

Sempre facendo riferimento alle due Figure 5 e 6 mostrate sopra, possiamo osservare
come durante la prima ora del test che va dalle 12:45 alle  13:45, e che termina con il
raggiungimento di circa 50 utenti agli uffici del distretto di Napoli concorrentemente attivi, i
valori  di  utilizzo  della  CPU  della  macchina  virtuale  ospitante  il  Database  Server  e
l’occupazione  della  memoria  della  macchina  virtuale  ospitante  l’Application  Server
crescono in maniera lineare con il numero di utenti concorrenti.
Diversamente, con l’inizio della rampa degli accessi degli avvocati avvenuto alle 13:45,
l’utilizzo della CPU della macchina virtuale su cui è in esecuzione il Database Server
esplode  nei  5  minuti  immediatamente  successivi,  e  satura  in  corrispondenza  del
raggiungimento di circa 80 avvocati concorrenti avvenuto alle 13:50. Tale fenomeno si
presenta, anche se in forma più lieve, nell’utilizzo medio della CPU della macchina virtuale
su cui è in esecuzione l’Application Server mostrato nel primo grafico della Figura 5.
Risulta invece essere molto più evidente come all’aumentare delle richieste in ingresso al
sistema, dovuto alla rapida crescita della rampa degli accessi degli avvocati, corrisponda
anche una rapida occupazione dello spazio in memoria della macchina virtuale su cui è in
esecuzione l’Application Server. Ci riferiamo all’intervallo di tempo che intercorre tra le
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 13
Figura 6 - Utilizzo della CPU e della Memoria del Database Server nel tempo

13:50, tempo di saturazione dell’utilizzo della CPU della macchina virtuale ospitante il
Database Server, e le 14:03, tempo oltre il quale il rimanente spazio di memoria viene ad
essere gradualmente occupato fino al raggiungimento della completa saturazione alle
14:45, come mostrato nel secondo grafico di Figura 5.
Tale fenomeno è dovuto alla necessità da parte dell’Application Server di allocare ed
occupare maggiore spazio in memoria (nuovi processi, metadati, dati, ecc.) per poter
gestire il crescente numero di richieste in ingresso, e che molto più lentamente verrà
rilasciato  rispetto  alla  prima  ore  di  test  a  causa  della  già  menzionata  saturazione
dell’utilizzo della CPU della macchina virtuale su cui è in esecuzione il Database Server
che, insieme all’aumentato livello di concorrenza, genera una dilatazione generale dei
tempi medi di risposta alle richieste degli utenti, come è anche mostrato nelle Figure 7 e 9
generate dalle strumento Apache JMeter.
In Figura 7 sono riportati i tempi medi di risposta alle richieste degli utenti agli uffici del
distretto di Napoli per le varie azioni coinvolte nelle 11 sequenze di test.
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 14
Figura 7 - Tempi medi di risposta alle richieste degli utenti degli ufci del distretto di Napoli

E’ evidente come il rapido aumento delle richieste in ingresso, avvenuto alle ore 13:45 in
corrispondenza  dell’inizio  della  rampa  degli  accessi  degli  avvocati,  abbia  avuto  un
notevole impatto anche sui tempi medi di risposta alle richieste degli utenti degli uffici del
distretto di Napoli, provocando un sostanziale cambiamento nel trend della crescita delle
curve dei tempi medi di risposta alle richieste di tali utenti nel tempo, e che sono associate
alla gran parte delle azioni incluse nelle 11 sequenze di test prima discusse.
In Figura 8 viene riportato un ingrandimento dello stesso grafico mostrato in Figura 7, con
la differenza che i tempi medi di risposta alle richieste degli utenti agli uffici del distretto di
Napoli sono stati calcolati a partire da campioni aggregati per intervalli di tempo di 10
minuti al fine di ammortizzare le eccessive fluttuazioni riscontrate nel grafico di Figura 7, e
per meglio mettere in evidenza il trend delle curve nell’intervallo compreso tra 0 e 5
secondi dei valori dei tempi medi di risposta.
Si può facilmente osservare come dopo la fase iniziale di test, che va dalle ore 12:45 alle
ore 13:05, si vengono a manifestare gli effetti di caching del sistema con conseguente
giovamento da parte dei tempi medi di risposta che si assestano intorno a valori più stabili
e costanti nel tempo fino alle ore 13:45, cui corrisponde anche il raggiungimento di 50
utenti agli uffici del distretto di Napoli concorrentemente attivi. In questo intervallo di tempo
la gran parte dei tempi medi di risposta alle richieste degli utenti hanno valori che non
superano 1 secondo, mentre alcuni sono compresi tra 1 e 5 secondi e solo due superano i
10 secondi.
Con l’inizio  della  rampa degli accessi  degli avvocati avvenuto alle  ore 13:45 questo
equilibrio si rompe ed i tempi medi di risposta alle richieste degli utenti degli uffici del
distretto di Napoli iniziano a divergere verso valori decisamente superiori, coinvolgendo
anche quelle azioni i cui tempi medi di risposta erano prima inferiori ad 1 secondo.
Il rapido incremento dei tempi di risposta alle richieste degli utenti suggerisce che tale
fenomeno può essere dovuto sia a causa dell’aumento della contesa sulle risorse fisiche,
sia a causa dell’aumento della contesa sulle risorse logiche. Infatti il trend della crescita
delle curve dei tempi medi di risposta alle richieste degli utenti nel tempo successivo alle
ore 13:45 non segue una crescita lineare e proporzionale al numero di utenti concorrenti
che  è tipica  dei  sistemi  in  saturazione, piuttosto  questi  crescono  improvvisamente  e
raggiungono valori decisamente più alti per poi stabilizzarsi ed iniziare a seguire una
crescita  molto  meno  ripida.  Questo  mette  in  evidenza  l’esistenza  di  un’interferenza
nell’accesso a determinate risorse logiche tra gli avvocati e gli utenti agli uffici del distretto
di Napoli, con il risultato di introdurre un dilatamento aggiuntivo nei tempi medi di risposta
alle richieste di entrambe le tipologie degli utenti.
Da tale comportamento si evince dunque la presenza di una problematica prestazionale
connessa all’implementazione delle operazioni effettuate durante l’esecuzione delle azioni
associate alle richieste degli avvocati che, come già evidenziato nella relazione tecnica
con titolo “Analisi dei risultati dei test di SIUS-Avvocatura del 18-19 Maggio 2018”, hanno
un notevole impatto sul carico di sistema.
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 15

Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 16
Figura 8 - Tempi medi di risposta alle richieste degli utenti degli ufci del distretto di Napoli aggregati
per intervalli di 10 minuti

In Figura 9 sono invece riportati i tempi medi di risposta alle richieste degli avvocati relativi
alle azioni coinvolte nella loro sequenza di test.
Osservando i tempi medi di risposta alle richieste degli avvocati possiamo notare come
alcune di queste richieste siano caratterizzate da tempi che crescono in maniera lineare
con l’aumentare del numero degli utenti concorrenti fino ad assumere valori nell’ordine dei
minuti, mentre le altre richieste sono caratterizzate da tempi che si mantengo costanti e
maggiormente contenuti, anche se generalmente elevati.
In entrambi i casi i tempi medi di risposta subiscono a partire dalle ore 14:41 circa un crollo
causato  dal  fallimento di un  gran  numero  di  richieste  inoltrate al  sistema, che  nella
stragrande maggioranza hanno ritornato l’errore “SocketException” del package “java.net”
come mostrato nei risultati prodotti da JMeter e riportati in Figura 10.
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 17
Figura 9 - Tempi medi di risposta alle richieste degli avvocati
Figura 10 - Errori campionati da JMeter dalle richieste degli avvocati

Ai fini della completezza riportiamo in Figura 11 anche il numero di occorrenza di tali errori
nel tempo (linea blu). E’ evidente come la gran parte delle richieste che ritornano un
codice di errore appartengono all’intervallo di tempo che ha inizio sempre alle ore 14:41 e
termina con il completamento del test.
Sempre in Figura 11 è riportato il numero di richieste inviate al minuto verso il sistema
centrale da parte degli avvocati e che completano con successo (linea rossa). In Figura 12
lo stesso tipo di grafico, ma che fa riferimento alle richieste completate con successo ed
alle richieste che terminano con errore inoltrate dagli utenti agli uffici del distretto di Napoli.
I grafici mostrati nelle Figure 11 e 12 sono stati generati effettuando un’analisi sui dati
grezzi registrati dalle due istanze dallo strumento Apache JMeter utilizzate per eseguire i
test. Tali istanze agiscono da clients nei confronti del sistema SIES distrettuale e del
sistema centrale che ricevono e servono le richieste ad essi inviate, dunque l’informazione
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 18
Figura 11 - Richieste degli avvocati
Figura 12 - Richieste degli utenti agli ufci del distretto di Napoli

che è stata possibile ricostruire a partire da tali dati fornisce una visione dell’evoluzione
dell’interazione di tipo richiesta-risposta con il sistema limitata al lato client.
Da queste informazioni ricostruite capiamo che lo strumento Apache JMeter, nel simulare
gli avvocati, riesce ad inviare verso il sistema centrale un numero di richieste che cresce in
modo proporzionale all’aumentare del numero di utenti concorrenti fino alle ore 13:55, cui
corrisponde il raggiungimento di circa 165 avvocati concorrenti. Dopo questo tempo il
numero di richieste inviate da parte degli avvocati subisce una battuta d’arresto dovuta
molto probabilmente alla eccessiva dilatazione dei tempi di risposta delle azioni coinvolte
(mostrata in Figura 9) con il conseguente rallentamento dell’attività dei threads attivati
dall’istanza dello strumento Apache JMeter per la simulazione degli avvocati.
Per quanto  riguarda  invece  gli  utenti  agli  uffici  del  distretto  di  Napoli, simulati  dalla
seconda istanza dello strumento Apache JMeter, si capisce che il numero delle richieste
inviate al sistema cresce in maniera proporzionale con l’aumentare del numero di utenti
concorrenti nel tempo, mostrando solo dopo il tempo di inizio della rampa degli accessi
degli avvocati un rallentamento causato anche qui dalla dilatazione dei tempi medi di
risposta alle richieste (mostrato in Figura 7). Diversamente da quanto rilevato per gli
avvocati, per gli utenti agli uffici del distretto di Napoli il numero di richieste fallite a causa
di errori di diversa natura e registrati nei Log dallo strumento Apache JMeter è pressoché
trascurabile.
Passiamo  quindi  ad  analizzare  il  comportamento  del  sistema  centrale  e  del  SIES
distrettuale nel tempo in funzione del numero di richieste entranti nel sistema da parte
degli utenti simulati per mezzo delle due istanze dello strumento Apache JMeter.
In Figura 13 riportiamo il numero di richieste inviate dagli avvocati al sistema centrale che,
come già menzionato nel secondo paragrafo, agisce da gateway reindirizzano le richieste
ricevute verso il SIES distrettuale. Le funzioni mostrate nel grafico sono rispettivamente: il
numero delle richieste che entrano nel sistema centrale al minuto (linea blu); il numero di
richieste  completate  con  successo  al  minuto  (linea  gialla);  ed  il  numero  di  richieste
terminate con errore al minuto (linea verde).
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 19
Figura 13 - Richieste degli avvocati inviate al sistema centrale

Si può notare come alle ore 14:41, in accordo con quanto osservato nel grafico del
numero di richieste inviate nel tempo dagli avvocati simulati per mezzo dello strumento
Apache JMeter (mostrato in Figura 11), un sostanziale numero di richieste ricevute dal
sistema termina con codice di errore. Quelle che osserviamo sono comunque solo una
sottoparte delle richieste fallite che sono state rilevate dallo strumento Apache JMeter.
Questo perché l’analisi è stata condotta a partire dai file di Log registrati dall’Application
Server del sistema centrale il quale non colleziona eventuali errori di più basso livello, ma
che sappiamo a questo punto verificarsi per via della sostanziale differenza nella quantità
di errori rilevati. Non avendo però a disposizione informazioni riguardanti l’utilizzo delle
risorse hardware al sistema centrale non possiamo fare altre deduzioni in merito.
Passiamo dunque ad analizzare il comportamento del sistema SIES distrettuale partendo
dalle informazioni dei Log raccolti dall’Application Server al distretto di Napoli. In Figura 14
sono riportate le funzioni relative al numero di richieste che sono ricevute dal sistema
SIES distrettuale con la stessa semantica di quelle mostrate per il sistema centrale.
In accordo a quanto avevamo detto in merito all’utilizzo delle risorse hardware sulle due
macchine virtuali predisposte al distretto di Napoli, nella prima ora del test, che va dalle
ore 12:45 alle ore 13:45, le richieste inviate dagli utenti agli uffici del distretto di Napoli
vengono smaltite con la stessa frequenza con cui queste vengono inviate al sistema dagli
utenti simulati per mezzo dello strumento Apache JMeter (Figura 12). Questo perché il
fattore di utilizzazione delle risorse hardware delle due macchine virtuali predisposte al
distretto di Napoli è molto basso, e mediamente vi sono sempre risorse disponibili che
possono essere impegnate al fine di soddisfare le nuove richieste entranti nel sistema.
Con l’inizio della rampa degli accessi degli avvocati, e con riferimento all’intervallo di
tempo compreso tra le 13:45 e le 14:00, il sistema perde il passo in termini di numero di
richieste completate per unità di tempo, anche noto come throughput, rispetto al numero di
reali richieste inviate dagli utenti simulati per mezzo delle due istanze dello strumento
Apache JMeter, e che divergono fino al raggiungimento dei valori osservati nei grafici delle
Figure 11 e 12 già discussi. Si può infatti notare come a partire dalle 13:45 il valore del
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 20
Figura 14 - Richieste degli utenti inviate al SIES distrettuale

throughput subisca un’impennata in concomitanza con il rapido incremento della quantità
di lavoro pendente nel sistema che deve essere evaso, ma il cui trend comincia a variare
intorno alle ore 13:50, ora in cui l’utilizzo della CPU della macchina virtuale ospitante il
Database Server e lo spazio di memoria della macchina virtuale ospitante l’Application
Server hanno saturato, ripiegando verso quei punti della curva dove il valore della derivata
prima è in costante decremento. A partire quindi dalle 13:50 il throughput di sistema
subisce una decelerazione che si conclude con l’assestamento di quest’ultimo intorno ad
un valore che è ben lontano dal numero di richieste inviate dagli utenti per unità di tempo
in tutti gli istanti successivi, le quali subiranno dei ritardi di servizio esagerati o saranno
addirittura vittime dei timeout imposti sulle connessioni ed errori dovuti alla saturazione
delle risorse come abbiamo già visto.
5 Conclusioni
Dalle simulazioni effettuate risulta che la frequenza con cui il sistema riesce ad evadere il
lavoro pendente è proporzionale alla frequenza con cui le richieste da parte degli utenti
fanno ingresso nel sistema solo fino alle ore 13:50. Si fa riferimento a quell’intervallo di
tempo che va dalle ore 13:45, in cui abbiamo solo 50 utenti agli uffici del distretto di Napoli
concorrenti, alle ore 13:50, in cui abbiamo 54 utenti agli uffici del distretto di Napoli più 83
avvocati concorrentemente attivi. Dopo questo tempo il fattore di utilizzazione delle risorse
fisiche è tale da portare il sistema in condizioni di saturazione, e non è quindi più in grado
di smaltire il crescente numero di richieste in ingresso.
I risultati dei test evidenziano comunque un notevole impatto sul carico di sistema da parte
delle richieste degli avvocati. Tale aspetto, già messo in evidenza nella relazione tecnica
con  titolo  “Analisi  dei  risultati  dei  test  di  SIUS-Avvocatura  del  18-19  Maggio  2018”,
suggerisce di procedere ad un’analisi dell’implementazione delle varie funzioni invocate
dalle suddette richieste, ai fini di valutare possibili interventi atti a ridurne l’impatto in
termini di costo computazionale sia sull’Application Server che sul Database Server di
SIES.
Analisi dei risultati dei test di performance del sistema SIES del 23 Gennaio
2019
Pag. 21