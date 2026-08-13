---
uniqueName: documentazioneserviziwebv1-53
displayName: "Documentazione servizi web v1 53"
category: "GENERAL"
tags: []
---

# Documentazione_servizi_web_v1.53

> **File originale:** `MEV/SCHEDA_013/Docs/Documentazione_servizi_web_v1.53.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
 
 
 
 
 
 
PROGETTAZIONE E REALIZZAZIONE DEL 
“PORTALE DEI SERVIZI TELEMATICI” PER IL 
MINISTERO DELLA GIUSTIZIA 
 
 
 
 
 
Documentazione Servizi Web 
Versione 1.53

2 
 
VER. 
DATA 
MOTIVO/RIFERIMENTO 
1.0 
15/09/2011 
Prima emissione  
1.1 
24/10/2011 
Aggiunti paragrafi 2.2.3 e 6.4 e modificati i paragrafi 6.1, 6.2 e 6.3. 
1.2 
15/02/2012 
Aggiunti servizi volontaria giurisdizione, aggiornati gli allegati e inserito paragrafo Troubleshooting 
1.3 
05/04/2012 
Aggiunti servizi Pagamenti Telematici e RRT. 
1.4 
13/07/2012 
Modifiche al paragrafo 2 e aggiunto il 5.7 
1.5 
31/08/2012 
 
Modificato i paragrafi 2.3 e 2.4. Nella tabella è stata aggiunta il nuovo criterio di consultazione 
(NotificheDaRitirare) 
 
Corretto targehost in targethost 
 
Modificato paragrafo 5.5 inserendo la URL esposta ai PDA; 
 
Modificato paragrafo 5.5 inserendo la URL esposta ai PDA; 
 
Modificato il titolo del manuale da “Documentazione Servizi di Consultazione” in 
Documentazione Servizi Web; 
 
Modificata introduzione per renderla conforme al nuovo titolo più generico 
1.6 
28/01/2013 
 
Modificato paragrafo 5.2 inserendo il servizio getListUGElectroPay 
 
Modificato il riferimento A1 (A1-WSDL-CATALOG-v1.5.zip) 
1.7 
22/03/2013 
 
Modificato capitolo 5.3 ricerca per cognome 
 
Modificato il riferimento A1 (A1-WSDL-CATALOG-v1.7.zip) modificato solo il nome del 
file come da richiesta per uniformare le versioni con questo documento 
1.8 
20/06/2013 
 
Aggiornata la documentazione dei servizi per i pagamenti telematici 
1.9 
11/07/2013 
 
Modifiche al capitolo 6.4 inserendo altri servizi 
 
Specificato nel capitolo 3.1l’utilizzo del download del documento originale 
1.10 
05/08/2013 
 
Eliminato il metodo Download Ricevuta in quanto non più utilizzabile 
1.11 
04/11/2013 
 
Inserito il metodo DownloadRicevuta tra i metodi deprecati cap5.9.1 
1.12 
08/11/2013 
 
Inserito il nuovo servizi di ricerca dei soggetti sul ReGIndE nel par. 5.3 e inserito il servizio 
deprecato in 5.9.1. 
 
Aggiunto nuova ricerca nelle consultazioni dell’Archivio Giurisprudenziale al par. 3.3 
1.13 
12/12/2013 
 
Aggiunto un metodo nel servizio di interrogazione degli enti RegIndE 
1.14 
13/02/2014 
 
Modificato capitolo 5.3 per refuso   
1.15 
04/04/2014 
 
Inserito nuovo servizio per il curatore fallimentare al capitolo 5.7 
 
Aggiornato capitolo 5.3 con la descrizione del metodoricercaIndAbilitati 
 
Aggiornata la tabella all’interno del capitolo 2.1.2 inserendo il valore CUR 
 
Inseriti la tipologia di controlli e gli errori restituiti a fronte dell’operazione 
inoltraRichiestaPagamento. Capitolo 5.5 
 
Inseriti nuovi capitoli 2.6 e 2.7 per servizi di Consultazioni registri anonimizzati. 
1.16 
20/06/2014 
 
Modificato i paragrafi 2.3 e 2.4. Nella tabella sono stati aggiunti i nuovi criteri di consultazione 
(ComunicazioneCancelleria e DettaglioComunicazione) 
 
Modificato il paragrafo2.5. Nella tabella è stata aggiunta il nuovo criterio di consultazione 
(NotificheDaRitirare) 
 
Modificata tabella capitolo 6.4 dove sono stati aggiunti i Servizi ReGIndE 
1.17 
23/07/2014 
 
Aggiornamento/correzione WSDL allegati 
1.18 
07/11/2014 
 
Specifica dei namespace e delle interrogazioni per le consultazioni dei registri penale e civile 
della Cassazione 
 
Specifica dei namespace e dei servizi per il download delle sentenze dei registri civile e penale 
della cassazione 
 
Specifica dei namespace e dei servizi per il download delle ricevute delle notifiche per i registri 
penale e civile della cassazione. 
 
Correzione refusi par. 2.2.2 e 2.2.3 
1.19 
27/02/2015 
 
Specifica del servizio di download comunicazioni/notifiche par. 5.8 
 
Documentata la modifica di funzionalità del servizio di download atti par. 3.1 
 
Aggiunto in servizio di calcolo Hash 3.1 
1.20 
14/04/2015 
 
Aggiunti i servizi di catalogo al proxy delle Software House

3 
 
 
Modifica delle specifiche dei servizi di pagamento telematico 
1.21 
12/10/2015 
 
Aggiunti i servizi di consultazione anonimizzata per i registri civile e penale della Corte di 
Cassazione, par. 2.10 e 2.11 
 
Aggiornato il par. 6.4   con gli wsdl dei servizi di cui sopra. 
 
Aggiornati i cataloghi delle consultazioni in allegato [A-1] aggiornando i tipi ritornati dalla 
consultazioni sui registri sicid/siecic e cassazione. 
1.22 
13/11/2015 
 
Modificati i paragrafi 2.3, 2.4 e 2.5.   Nelle tabelle dei servizi è stata modificata la descrizione 
del servizio “RicercaScadenze”  
 
Modificato il paragrafo 5.5 con l’introduzione di nuove operazioni relativa ai pagamenti 
telematici 
1.23 
11/02/2016 
 
Modificato il paragrafo 3.1 (ex 3.3) con l’indicazione dei parametri specifici allineandolo al 
par. 2.1 
 
Modificato 
il 
paragrafo 
5.5 
introducendo 
nella 
descrizione 
del 
servizio 
“generaRichiestaPagamento” il codice del metodo di pagamento OBEP 
 
Aggiornato il catalogo delle Consultazioni Anonime Cassazione. 
1.24 
01/04/2016 
 
Modificato il paragrafo 2.3 e 2.4 introducendo il servizio di “DettaglioIstanze”; 
 
Inserito il paragrafo 5.10 relativo al nuovo servizio di generazione codice identificativo per i 
creditori esteri 
 
Modificato il riferimento A1 (A1-WSDL-CATALOG-v1.23.zip). 
1.25 
07/04/2016 
 
Modificati i paragrafi 2.2.2 e 3.1.2 inserendo le specifiche dell’InvocationDomain relative ai 
Registri di Cassazione. 
1.26 
15/11/2016 
 
Modificato par. 5.6 
1.27 
17/02/2017 
 
Inserito par. 5.1 e modificato il par.5.7 
 
Inseriti i ruoli di consultazione “CUS” e “DEL” relativa alle consultazioni dei custodi e 
delegati. Modificati i paragrafi 2.2.2, 2.2.3, 3.1.2 e 3.1.3. 
1.28 
07/04/2017 
 
Modificato par. 3.3 
 
Modificato par. 5.5 per l’introduzione del pagamento dei bolli telematici 
1.29 
15/05/2017 
 
Inseriti i ruoli di consultazione “NOT”,” TUT”,” CTU” e “AUS”. Modificati i paragrafi 2.1.2, 
2.1.3, 3.1.2 e 3.1.3. 
1.30 
09/08/2017 
 
Modificato par. 5.7 – "Scambio messaggi tra ausiliari e giudice delegato" 
1.31 
16/10/2017 
 
Modificato par. 3.3.1 – “Archivio Giurisprudenziale Distrettuale” 
1.32 
08/01/2018 
 
Modificato par. 5.2 – “Catalogo degli Uffici Giudiziari” 
1.33 
02/03/2018 
 
Eliminato par. 3.3.1 – “Archivio Giurisprudenziale Distrettuale” 
1.34 
26/03/2018 
 
Modificato il par. 5.5 – “Pagamenti Telematici” 
1.35 
12/07/2018 
 
Modificato il par. 3.3 – “Archivio Giurisprudenziale Nazionale” 
1.36 
07/08/2018 
 
Modificato par. 3.3.1 – “Ricerca provvedimenti” 
1.37 
14/09/2018 
 
Eliminati i par. 5.5 “Pagamenti Telematici” e 5.9.2 “Servizi Deprecati -Pagamenti Telematici” 
 
Inseriti i par. 5.5 “Invio Pagamenti Telematici” e 5.6 “Consultazione pagamenti telematici” 
 
Modificato par. 6.4 “Indirizzi per l’invocazione dei web service” 
1.38 
19/10/2018 
 
Eliminato par.5.7 “Repository Ricevute Telematiche (RRT)” 
 
Modificato par 6.4 “Indirizzi per l’invocazione dei web service” 
 
Modificato il par.5.2 “Catalogo degli Uffici Giudiziari” eliminando il metodo “getOrdini” 
1.39 
08/11/2018 
 
Modificato il par.5.6 “Consultazione pagamenti telematici”: corretto refuso 
1.40 
28/01/2019 
 
Aggiornato il riferimento A1 (A1_WSDL_CATALOG_v1.31.zip)

4 
 
1.41 
28/05/2019 
 
Aggiunta la consultazione QC_FascicoloInformatico alle consultazioni del Registro Civile di 
Cassazione. 
 
Aggiunti servizi di download dei documenti per il registro di Cassazione Civile alla sezione 
‘Accesso ai Documenti’. 
 
Aggiornato il riferimento in Tabella 1 (A1_WSDL_CATALOG_v1.32.zip)  
1.42 
09/08/2019 
 
Eliminato la tabella con la descrizione del metodo listaDatiRisossione all’interno del paragrafo 
5.5 “Invio pagamenti telematici” 
 
Aggiornato il riferimento in Tabella 1 (A1_WSDL_CATALOG_v1.33.zip)  
1.43 
08/11/2019 
 
Modificato il par. 5.3 inserita l’operazione: “ricercaEntiReferente” 
 
Aggiornato il riferimento in Tabella 1 (A1_WSDL_CATALOG_v1.34.zip) 
1.44 
01/09/2020 
 
Aggiunta la consultazione QC_Uffici alle consultazioni anonimizzate del Registro Civile di 
Cassazione par. 2.10 
1.45 
15/10/2020 
 
Aggiornato il riferimento in Tabella 1 (A1_WSDL_CATALOG_v1.35.zip) 
1.46 
27/11/2020 
 
Modificato par. 2.1.1, 3.1.1 e 3.2: integrato il parametro CODICEUNIVOCO tra i parametri 
da necessari per consultare con ruolo Parte di tipo Pubblica Amministrazione. 
1.47 
22/12/2020 
 
Nel par. 5.3 tra i metodi del wsdl ServiziInterrogazioneEnte.wsdl, è stato aggiunto 
RicercaEnteInt. 
 
Modificato il servizio elencoPagamenti introducendo lo stato REVOCATO e inserita la 
descrizione del metodo “elencoPagamentiRevocati” all’interno del paragrafo 5.6 
“Consultazione pagamenti telematici” 
 
Aggiornato il riferimento in Tabella 1 (A1_WSDL_CATALOG_v1.36.zip) 
1.48 
08/06/2021 
 
Aggiornato il riferimento in Tabella 1 (A1_WSDL_CATALOG_v1.37.zip) 
1.49 
21/06/2021 
 
Modificato il servizio elencoPagamenti introducendo gli stati OK_PSP, KO_PSP e 
GENERATA, modificando la descrizione del parametro codiceCRS e modificando la struttura 
dell’oggetto restituito all’interno del paragrafo 5.6 “Consultazione pagamenti telematici” 
 
Modificato il servizio downloadRichiesta modificando la descrizione del parametro 
codiceCRS all’interno del paragrafo 5.6 “Consultazione pagamenti telematici” 
 
Modificato il servizio downloadRicevuta modificando la descrizione del parametro codiceCRS 
all’interno del paragrafo 5.6 “Consultazione pagamenti telematici” 
 
Modificato il servizio invioCarrelloRPT inserendo il parametro areaPubblica all’interno del 
paragrafo 5.5 “Invio pagamenti telematici” 
 
Modificato il servizio registraRispostaWisp specificando che non deve essere utilizzato dagli 
applicativi all’interno del paragrafo 5.5 “Invio pagamenti telematici” 
 
Inserita la descrizione dei metodi “generaAvviso” e “downloadAvviso” all’interno del 
paragrafo 5.5 “Invio pagamenti telematici” 
 
Aggiornato il riferimento in Tabella 1 (A1_WSDL_CATALOG_v1.38.zip) 
 
1.50 
30/09/2021 
 
Modificato par. 5.3 “Accesso al Reginde” 
1.51 
07/03/2022 
 
Inseriti i nuovi metodi “getListaUfficiPenale”, “getNormativa” e “getUfficioPenale” 
all’interno del paragrafo 5.2 “Catalogo degli Uffici Giudiziari” 
 
Modificati i metodi “getTipiUfficio” e “getComuni” all’interno del paragrafo 5.2 “Catalogo 
degli Uffici Giudiziari” 
 
Aggiornato il riferimento in Tabella 1 (A1_WSDL_CATALOG_v1.39.zip) 
 
1.52 
01/04/2022 
 
Rinominato il metodo “ricercaReferenti” con “ricercaReferente” al paragrafo 5.3 “Accesso al 
ReGIndE” 
 
Inserito il nuovo metodo “ricercaEnteComplete” al paragrafo 5.3 “Accesso al ReGIndE” 
 
Aggiornato il riferimento in Tabella 1 (A1_WSDL_CATALOG_v1.40.zip) 
1.53 
24/06/2022 
 
Aggiornato il riferimento in Tabella 1 (A1_WSDL_CATALOG_v1.41.zip)

5 
 
Sommario 
Sommario ....................................................................................................................... 5 
Allegati ....................................................................................................................... 6 
1 
Introduzione ................................................................................................... 7 
1.1 
Guida alla lettura ............................................................................................ 7 
2 
Consultazione dei Registri di Cancelleria ...................................................... 8 
2.1 
Parametri specifici ......................................................................................... 8 
2.2 
Interfaccia del web service ............................................................................. 9 
2.3 
Elenco Interrogazioni Registri SICID .......................................................... 13 
2.4 
Elenco Interrogazioni Registri SIECIC ....................................................... 15 
2.5 
Elenco Interrogazioni Registro SIGP ........................................................... 17 
2.6 
Elenco Interrogazioni Registri SICID (dati anonimizzati) .......................... 19 
2.7 
Elenco Interrogazioni Registri SIECIC (dati anonimizzati) ........................ 20 
2.8 
Elenco Interrogazioni Registro Civile Cassazione ...................................... 21 
2.9 
Elenco Interrogazioni Registro Penale Cassazione ...................................... 22 
2.10 
Elenco Interrogazioni Registri Civile Cassazione (dati anonimizzati) ........ 23 
2.11 
Elenco Interrogazioni Registri Penale Cassazione (dati anonimizzati) ....... 24 
2.12 
Troubleshooting ........................................................................................... 24 
3 
Accesso ai Documenti .................................................................................. 26 
3.1 
Parametri specifici ....................................................................................... 26 
3.2 
Elenco consultazionifascicoloinformatico ................................................... 28 
3.3 
Archivio Giurisprudenziale Nazionale ........................................................ 35 
3.4 
Download sentenze per i registri penale e civile della Cassazione .............. 38 
3.5 
Download ricevute PEC notifiche per i registri civile e penale della 
Cassazione .................................................................................................... 39 
4 
Servizi per le Richieste Copie (servizio ancora non rilasciato) ................... 40 
5 
Altri Servizi .................................................................................................. 42 
5.1 
Parametri specifici ....................................................................................... 42 
5.2 
Catalogo degli Uffici Giudiziari .................................................................. 42 
5.3 
Accesso al ReGIndE .................................................................................... 48 
5.4 
Servizio di configurazione notifiche via SMS (servizio sospeso) ............... 55 
5.5 
Invio pagamenti telematici ........................................................................... 57 
5.6 
Consultazione pagamenti telematici ............................................................ 60

6 
 
5.7 
Scambio messaggi tra ausiliari e giudice delegato ...................................... 65 
5.8 
Download messaggi di notifica e comunicazione ........................................ 68 
5.9 
Servizi Deprecati .......................................................................................... 69 
5.10 
Servizio di generazione codice identificativo univoco per il creditore estero
 ...................................................................................................................... 71 
6 
Accesso ai servizi di consultazione tramite proxy ....................................... 73 
6.1 
Proxy per i Punti di Accesso ........................................................................ 73 
6.2 
Proxy per le software house ......................................................................... 73 
6.3 
Proxy per le Parti in Causa (servizio ancora non rilasciato) ........................ 74 
6.4 
Indirizzi per l’invocazione dei web service ................................................. 74 
 
Allegati 
 
Codice 
Descrizione 
[A-1] 
Archivio compresso contenente WSDL e Catalog. 
Nome file: A1-WSDL-CATALOG-v1.41.zip 
Tabella 1 - Allegati

7 
 
1 Introduzione 
Lo scopo del presente documento è definire quali siano i servizi web messi a 
disposizione di enti terzi e software house per l’utilizzo dei servizi telematici del 
Ministero della Giustizia relativamente al Processo Civile Telematico. 
1.1 Guida alla lettura 
Il presente documento è strutturato, oltre al presente, in sei capitoli di cui si riporta di 
seguito una breve descrizione. 
Il capitolo 2 illustra il meccanismo adottato per invocare tutti i servizi di consultazione 
dei registri di cancelleria, la lista dei servizi disponibili e quali sono le operazioni utili 
a determinare i parametri di input/output per le differenti invocazioni.   
Il capitolo 3 descrive i servizi utili ad ottenere informazioni e dati in merito ai 
documenti elettronici. 
Il capitolo 4 presenta i servizi di richiesta copie ed elenca quali sono le operazioni per 
poterle richiedere. 
Nel capitolo 5 sono descritti altri tipi di servizi a disposizione dei soggetti abilitati 
esterni quali l’accesso ai servizi per l’invio delle notifiche via SMS e il catalogo degli 
uffici giudiziari.   
Il capitolo 6 elenca i vari proxy con cui è possibile interagire e ne descrive le diverse 
modalità. 
Prima di procedere alla lettura del presente documento estrarre il contenuto 
dell’archivio compresso allegato mantenendo la struttura delle directory presenti 
nell’archivio stesso. Si farà infatti riferimento ai file estratti referenziandoli con il patch 
relativo.

8 
 
2 Consultazione dei Registri di Cancelleria 
2.1 Parametri specifici 
2.1.1 
Header http 
Il codice fiscale del soggetto che ha invocato la richiesta è indicato nell’header HTTP 
della request (proprietà X-WASP-User).  
Con la modifica del Registro delle Pubbliche Amministrazione, ogni amministrazione 
viene individuata da una coppia di valori, il codice fiscale e il codice univoco. Se vi 
vuole consultare i fascicolo con il ruolo Parte e la parte è una Pubblica 
Amministrazione, allora sarà necessario inserire nell’header (proprietà X-WASP-User) 
sia il codice fiscale che il codice univoco, nel seguente modo: 
CODICEFISCALE=XXXXX;CODICEUNIVOCO=YYYY 
Il codice univoco se diverso dal codice fiscale, individua articolazioni locali o 
territoriali della Pubblica Amministrazione. Codice fiscale e codice univoco 
corrispondono quando si tratta di una pubblica amministrazione centrale.  
2.1.2 
Header SOAP 
I messaggi SOAP rivolti ai servizi di backend offerti dagli Uffici Giudiziari presentano 
un SOAP header con la seguente forma: 
<soapenv:Header><ws:InvocationDomain name="JPW" role="YYY" 
group=”XXXXXXXX” 
soapenv:mustUnderstand="1" 
soapenv:actor="http://schemas.xmlsoap.org/soap/actor/next
" xmlns:ws="http://www.netserv.it/anag/security"/> 
dove: 
 per poter accedere al servizio che mette a disposizione il catalogo delle tipologie 
di interrogazione (query e relative metainformazioni) dei servizi di back end 
degli Uffici Giudiziari: 
o role: assume il valore “JPW”  
o group: assume il valore “jpwusers” 
 per le richieste di consultazione (metodo execute) invocate dagli utenti esterni 
abilitati: 
o role: assume i valori indicati nella tabella di seguito riportata 
o group: contiene il codice dell’Ufficio Giudiziario destinatario del 
messaggio. 
N.B. Per l’invocazione dei servizi di back end della Corte di Cassazione, all’interno 
dell’Invocation Domain, non deve essere specificato il parametro “group”. 
Elenco dei valori relativi all’attributo role per l’invocazione del metodo execute:

9 
 
SICID 
AVV, CTU, PARTE, NOT, TUT, AUS 
SIECIC 
AVV, CTU, PARTE, CUS, DEL 
SIGP 
AVV, CTU, PARTE 
CASSAZIONE AVV, PARTE 
2.1.3 
Semantica dell’attributo role e del parametro idruolojpw 
Le informazioni presenti nell’header soap sono necessarie alla gestione della sicurezza 
ed in particolare permettono la gestione dell’autorizzazione all’esecuzione dei servizi. 
In particolare il parametro role permette di invocare web service diversi a seconda del 
ruolo specificato e quindi servizi dedicati alle consultazioni di avvocati (AVV), 
consulenti tecnici d’ufficio, periti/esperti e curatori/commissari/liquidatori (CTU), parti 
(PARTE), 
custodi 
(CUS), 
delegati 
(DEL), 
Notai/Ufficiali 
(NOT), 
Curatori/Tutori/Amm. di sostegno (TUT) e Ausiliari Incaricati (AUS). Il valore 
role=JPW è necessario per invocazioni di servizi per cui la specifica del ruolo del 
soggetto non è necessaria ovvero servizi di carattere generale presenti nel sistema di 
consultazione.  
Le problematiche di visibilità sono invece risolte attraverso l’utilizzo del valore 
idruolojpw presente tra i parametri di input delle consultazioni; in pratica tale parametro 
permette di specificare rispetto a quale tipologia di incarico si vogliono filtrare i dati. 
Ad esempio se un CTU è curatore/commissario/liquidatore ma nel parametro 
idruolojpw si indica CTU non vengono restituiti i procedimenti in cui il soggetto è 
incaricato come curatore/commissario/liquidatore (valore CUR) ma solo quelli dove è 
incaricato con altre tipologie di consulenza. Allo stesso modo se un avvocato è anche 
curatore e nel parametro idruolojpw si indica AVV vengono restituiti i soli fascicoli in 
cui il soggetto costituito in giudizio come difensore e non quelli dove il soggetto è 
incaricato come curatore/commissario/liquidatore. Per quest’ultima invocazione dovrà 
utilizzare il valore CUR. 
Rispetto alle logiche generali di cui sopra è necessario sottolineare che nel contesto 
delle consultazioni di SICID e SIGP il parametro idruolojpw nel body del messaggio 
soap è stato omesso e il sistema utilizza direttamente quanto presente nell’header anche 
per le problematiche di visibilità sui dati. Lo stesso discorso vale per la gestione 
l’invocazione dei servizi di accesso al fascicolo informatico in cui si sfrutta anche per 
la visibilità la sola informazione presente nell’header soap. 
Si noti inoltre che nel contesto delle consultazioni SIECIC il parametro 
idruolojpw=AVV comprende anche la visibilità dei delegati (ed è quindi corretto parlare 
di profilo Avvocato/Delegato).  
 
2.2 Interfaccia del web service 
Tutti i servizi di consultazione, relativi alle informazioni contenute nei sistemi di 
gestione dei registri di cancelleria sono realizzati attraverso un servizio generico che

10 
 
permette di attivare un catalogo di query stabilito, e di ottenere metainformazioni su di 
esso. Tramite le operazioni del servizio è possibile: 
 conoscere quante e quali sono le tipologie di interrogazioni messe a disposizione; 
 ottenere meta dati descrittivi della struttura delle query in termini di parametri 
necessari alla loro invocazione e formato dei record in uscita; 
 ottenere meta dati su uno specifico tipo di record in uscita; 
 invocare l’interrogazione specifica. 
La fruizione dei servizi di tale costruttore di query avviene tramite l’esposizione di un 
opportuno web-service nell’infrastruttura SOAP implementata dal Gestore Locale, tale 
web service espone le quattro operazioni sopra elencate.  
Di seguito sono descritte con maggiore dettaglio le interfacce delle operazioni messe a 
disposizione dal servizio dove il valore di NAMESPACE assume valori distinti in base 
al registro scelto per la consultazione: 
 Contenzioso Civile = urn:CONS-SICC-BE (per ragioni di retro compatibilità 
rimane valido anche urn:CONS-SICC-BE-DISTR) 
 Diritto del Lavoro = urn:CONS-SIL-BE (per ragioni di retro compatibilità rimane 
valido anche urn:CONS-SIL-BE-DISTR) 
 Volontaria Giurisdizione =urn:CONS-SIVG-BE 
 Procedure Concorsuali =urn:CONS-SIECIC-BE 
 Esecuzioni Mobiliari = urn:CONS-SIECIC-BE 
 Esecuzioni Immobiliari = urn:CONS-SIECIC-BE 
 Procedimenti davanti al Giudice di Pace = urn:CONS-SIGP-BE 
 Consultazione del Registro Civile della Cassazione = urn:CONS-CASSCI 
 Consultazione del Registro Penale della Cassazione = urn:CONS-CASSPE 
 
 
Per alcuni registri è disponibile la consultazione dei fascicoli in formato anonimizzato. 
Di seguito l’elenco dei registri e il relativo NAMESPACE da utilizzare nel servizio. 
 Contenzioso Civile = urn:CONS-ANONIMA-SICC-BE 
 Diritto del Lavoro = urn:CONS-ANONIMA-SIL-BE 
 Volontaria Giurisdizione =urn:CONS-ANONIMA-SIVG-BE 
 Procedure Concorsuali =urn:CONS-ANONIMA-SIECIC-BE 
 Esecuzioni Mobiliari = urn:CONS-ANONIMA-SIECIC-BE 
 Esecuzioni Immobiliari = urn:CONS-ANONIMA-SIECIC-BE 
 Registro Civile Cassazione = urn:CONS-ANONIMA-CASSCI

11 
 
 Registro Penale Cassazione = urn:CONS-ANONIMA-CASSPE 
 
 
Di seguito l’interfaccia dei metodi disponibili.  
Operazione: 
getServiceNames 
Descrizione: 
ritorna la lista dei nomi dei servizi disponibili 
Parametri: 
nessuno 
Risultato: 
array di stringhe con i nomi delle interrogazioni, codificato da tipo 
XML, presente nel binding SOAP come elemento del body di 
risposta 
 
Operazione: 
getServiceDescriptor 
Descrizione: 
ottiene il descrittore per l’interrogazione specificata 
Parametri: 
serviceName:  
nome del servizio da descrivere, descritto come stringa, presente 
nel binding SOAP come elemento del body di richiesta 
Risultato: 
serviceDescriptorType: 
descrittore del servizio specificato, descritto negli allegati, 
presente nel binding SOAP come elemento del body di risposta 
 
Operazione: 
getRowClassDescriptor 
Descrizione: 
ritorna il descrittore del tipo di record specificato 
Parametri: 
className:  
tipo di record da descrivere, descritto come stringa, presente nel 
binding SOAP come elemento del body di richiesta. 
Risultato: 
rowClassDescriptorType:  
descrittore del record specificato, descritto negli allegati, presente 
nel binding SOAP come elemento del body di risposta.

12 
 
Operazione: 
execute 
Descrizione: 
esegue l’interrogazione specificata 
Parametri: 
name:  
nome dell’interrogazione, descritta come stringa, presente nel 
binding SOAP come elemento del body di richiesta 
valueSet:  
insieme dei parametri necessari all’interrogazione, descritto negli 
allegati, presente nel binding SOAP come elemento del body di 
richiesta 
orderBy:  
ordinamenti dell’insieme dei risultati, descritto negli allegati, 
presente nel binding SOAP come elemento del body di richiesta 
Risultato: 
rowListType: 
Lista di record risultato, descritto negli allegati, presente nel 
binding SOAP come elemento del body di risposta. 
 
Si riporta inoltre in esempio un estratto del messaggio per l’invocazione del servizio 
getServiceNames sul registro Contenzioso Civile: 
 
<soapenv:Body> 
<getServiceNamesxmlns="urn:CONS-SICC-BE"/> 
</soapenv:Body> 
 
Per le operazioni in taluni casi è inoltre richiesto un parametro “registro” che è 
possibile valorizzare come segue: 
 FALL =Procedure Concorsuali 
 ESM =Esecuzioni Mobiliari 
 ESIM =Esecuzioni Immobiliari 
 CC 
=Contenzioso Civile 
 LAV =Diritto del Lavoro 
 VG 
=Volontaria Giurisdizione 
 
Esempio per le Esecuzioni Mobiliari: 
<value name="registro" type="string">ESM</value>

13 
 
 
All’interno del valueSet sono presenti i parametri strettamente necessari alla specifica 
operazione invocata, mentre l’orderBy può essere utilizzato per ordinare i risultati 
ottenuti. Si riporta ad esempio, un ordinamento per gli elementi “annoregistro” e 
“numeroregistro” in modalità ascendente. 
Esempio: 
<orderBy> 
<entry property="annoregistro, numeroregistro" mode="asc"/> 
</orderBy> 
 
Per la definizione tramite WSDL del web service che espone i metodi sopra descritti si 
rimanda agli allegati presenti nella cartella“WSDL\Consultazione Registri”. 
 
2.3 Elenco Interrogazioni Registri SICID 
Di seguito l’elenco delle interrogazioni attivabili attraverso il metodo execute ed una 
breve descrizione delle stesse. Per la descrizione relativa alla semantica dei singoli 
parametri si rimanda agli allegati presenti nella directory “Catalog\Consultazione 
Registri/SICID”. 
Interrogazione 
Descrizione 
RicercaInformazioniFascicoloPerPartiGiudiceDate Ricerca fascicoli per Parti, 
Giudice e Date. 
RicercaInformazioniFascicoloPerTipo 
Ricerca fascicoli per numero di 
registro o sentenza 
Agenda 
Ricerca eventi negli storici 
compresi nelle date stabilite 
RuoliMaterieOggetti 
Ricerca ruoli, materie e oggetti 
di un ufficio 
StoricoFascicolo 
Storico del fascicolo 
RicercaInformazioniFascicoloPerRMO 
Ricerca fascicoli per Ruolo, 
Materia e Oggetto 
DocumentiUtente 
Ricerca 
i 
documenti 
nei 
fascicoli 
DocumentiFascicolo 
Elenco dei documenti di un 
fascicolo

14 
 
TestWS 
Verifica disponibilità servizi 
 
RicercaScadenze 
Ricerca dei termini e udienze. 
Tale 
servizio 
permette 
di 
filtrare i risultati per tipologia 
in 
base 
al 
parametro 
“filtroScadenza”, 
il 
quale 
accetta i valori: 
 “U” per le Udienze 
 “S” per le Scadenze 
 “” per visualizzare tutti 
i risultati 
Ogni altro valore inserito in 
tale 
parametro 
non 
permetterà il ritorno di 
risultati.  
 
ProfiloFascicolo 
Ricerca 
informazioni 
sul 
profilo del fascicolo 
ArchivioFascicoli 
Ricerca dei numeri di registro 
dei fascicoli 
NotificheDaRitirare 
Riporta 
le 
notifiche 
dell’avvocato in consultazione, 
fatte in Cancelleria 
ComunicazioneCancelleria 
Riporta l’elenco di tutte le 
comunicazioni/notificazioni 
fatte dalla Cancelleria in un 
fascicolo 
DettaglioComunicazione 
Riporta il dettaglio di una 
comunicazione/notificazione 
per ogni destinatario della 
stessa 
DettaglioIstanze 
Riporta l’elenco delle istanze, 
ovvero degli eventi messi in 
evidenza al giudice, per il 
fascicolo in questione

15 
 
2.4 Elenco Interrogazioni Registri SIECIC 
Di seguito l’elenco delle interrogazioni attivabili attraverso il metodo execute ed una 
breve descrizione delle stesse. Per la descrizione relativa alla semantica dei singoli 
parametri si rimanda agli allegati presente nella directory “Catalog\Consultazione 
Registri/SIECIC”. 
 
 
 
Interrogazione 
Descrizione 
ProfiloParteEC 
Informazioni sulla Parte per le 
esecuzioni 
ElencoSpese 
Elenco delle spese al fascicolo 
ProfiloLibretto 
Dettagli del libretto 
ElencoPendenze 
Elenco delle pendenze relative 
al fascicolo 
ElencoLibretti 
Elenco dei libretti relativi al 
fascicolo 
ElencoStatoPassivo 
Stato passivo di un fascicolo 
ElencoPartiPC 
Elenco delle parti di un 
fascicolo 
delle 
procedure 
concorsuali 
ProfiloFascicolo 
Ricerca 
informazioni 
sul 
profilo del fascicolo 
ProfiloLotto 
Dettagli del lotto 
StoricoFascicolo 
Storico del fascicolo 
RicercaInformazioniFascicoloPerBene 
Ricerca fascicoli per bene 
ElencoPartiEC 
Elenco delle parti di un 
fascicolo delle esecuzioni 
RicercaInformazioniFascicoloPerPartiGiudiceDate Ricerca fascicoli per Parti , 
Giudice o Date. 
ElencoDocumenti 
Elenco dei documenti associati 
al fascicolo

16 
 
RicercaAgenda 
Ricerca eventi negli storici 
compresi nelle date stabilite 
ProfiloPendenza 
Dettaglio Pendenza 
ProfiloIncarico 
Dettaglio Incarico 
ElencoBeniMobili 
Lista beni mobili associati al 
fascicolo 
RicercaInformazioniFascicoloPerNumero 
Ricerca fascicoli per numero di 
registro o sentenza 
RicercaArchivioEI 
Ricerca dei numeri di registro 
dei fascicoli per le esecuzioni 
ElencoBeniImmobili 
Elenco Beni immobili associati 
al fascicolo 
RicercaScadenze 
Ricerca dei termini e udienze. 
Tale 
servizio 
permette 
di 
filtrare i risultati per tipologia 
in 
base 
al 
parametro 
“filtroScadenza”, 
il 
quale 
accetta i valori: 
 “U” per le Udienze 
 “S” per le Scadenze 
 “” per visualizzare tutti 
i risultati 
Ogni altro valore inserito in 
tale 
parametro 
non 
permetterà il ritorno di 
risultati.  
 
ProfiloPartePC 
Informazioni sulla Parte per le 
procedure concorsuali 
ElencoInsinuazioni 
Lista Insinuazioni del fascicolo 
RicercaInformazioniFascicoloPerOggetto 
Ricerca fascicoli per codice 
oggetto 
RicercaArchivioPC 
Ricerca dei numeri di registro 
dei fascicoli per le procedure 
concorsuali

17 
 
ElencoIncarichi 
Lista Incarichi del fascicolo 
ElencoLotti 
Lista Lotti del fascicolo 
TestWS 
Verifica disponibilità servizi 
DocumentiUtente 
Ricerca 
i 
documenti 
nei 
fascicoli 
NotificheDaRitirare 
Riporta 
le 
notifiche 
dell’avvocato in consultazione, 
fatte in Cancelleria 
ComunicazioneCancelleria 
Riporta l’elenco di tutte le 
comunicazioni/notificazioni 
fatte dalla Cancelleria in un 
fascicolo 
DettaglioComunicazione 
Riporta il dettaglio di una 
comunicazione/notificazione 
per ogni destinatario della 
stessa 
DettaglioIstanze 
Riporta l’elenco delle istanze, 
ovvero degli eventi messi in 
evidenza al giudice, per il 
fascicolo in questione 
2.5 Elenco Interrogazioni Registro SIGP 
Di seguito l’elenco delle interrogazioni attivabili attraverso il metodo execute ed una 
breve descrizione delle stesse. Per la descrizione relativa alla semantica dei singoli 
parametri si rimanda agli allegati presente nella directory “Catalog\Consultazione 
Registri/SIGP”. 
Interrogazione 
Descrizione 
RicercaInformazioniFascicoloPerPartiGiudiceDate Ricerca fascicoli per Parti , 
Giudice e Date. 
ProfiloIncaricoFascicolo 
Dettaglio Incarico del fascicolo 
Agenda 
 
Ricerca eventi negli storici 
compresi nelle date stabilite 
ArchivioFascicoli 
 
Ricerca dei numeri di registro 
dei fascicoli

18 
 
RuoliMaterieOggetti 
 
Ricerca ruoli, materie e oggetti 
di un ufficio 
ElencoDocumentiAG 
 
Ricerca 
elenco 
documenti 
Archivio Giurisprudenziale 
RicercaInformazioniFascicoloPerRMO 
 
Ricerca fascicoli per Ruolo, 
Materia e Oggetto 
ElencoIncarichiFascicolo 
Elenco Incarichi del fascicolo 
ElencoDocumentiPubblicati 
Elenco dei documenti associati 
ad un fascicolo o a sentenza 
ElencoPartiFascicolo 
Elenco delle parti del fascicolo 
ProfiloParte 
Informazioni sulla Parte 
RicercaScadenze 
Ricerca dei termini e udienze. 
Tale 
servizio 
permette 
di 
filtrare i risultati per tipologia 
in 
base 
al 
parametro 
“filtroScadenza”, 
il 
quale 
accetta i valori: 
 “U” per le Udienze 
 “S” per le Scadenze 
 “” per visualizzare tutti 
i risultati 
Ogni altro valore inserito in 
tale 
parametro 
non 
permetterà il ritorno di 
risultati.  
 
RicercaInformazioniFascicoloPerTipo 
Ricerca fascicoli per numero di 
registro o sentenza 
ProfiloFascicolo 
Ricerca 
informazioni 
sul 
profilo del fascicolo 
TipiSentenza 
Elenco tipologie sentenza 
StoricoFascicolo 
Storico del fascicolo 
TestWS 
Verifica disponibilità servizi

19 
 
NotificheDaRitirare 
Riporta 
le 
notifiche 
dell’avvocato in consultazione, 
fatte in Cancelleria 
2.6 Elenco Interrogazioni Registri SICID (dati anonimizzati) 
Di seguito l’elenco delle interrogazioni attivabili attraverso il metodo execute ed una 
breve descrizione delle stesse. Per la descrizione relativa alla semantica dei singoli 
parametri si rimanda agli allegati presenti nella directory “Catalog/Consultazione 
Registri/SICID”. 
 
 
 
Registro Contenzioso Civile: 
Interrogazione 
Descrizione 
RicercaGiudici 
Elenco giudici per ufficio 
RicercaRuoloGenerale 
Ricerca fascicoli per numero di 
registro 
RicercaSentenza 
Ricerca fascicoli per numero di 
sentenza 
RicercaDecretoIngiuntivo 
Ricerca fascicoli per numero di 
decreto ingiuntivo 
RicercaDataIscrizioneRuolo 
Ricerca fascicoli per data di 
iscrizione a ruolo, rito e giudice 
RicercaDataCitazionePrimaUdienza 
Ricerca fascicoli per giudice e 
data citazione/prima udienza 
RicercaDataProssimaUdienza 
Ricerca fascicoli per giudice e 
data prossima udienza 
 
Registro Diritto del Lavoro: 
Interrogazione 
Descrizione 
RicercaGiudici 
Elenco giudici per ufficio 
RicercaRuoloGenerale 
Ricerca fascicoli per numero di 
registro

20 
 
RicercaSentenza 
Ricerca fascicoli per numero di 
sentenza 
RicercaDecretoIngiuntivo 
Ricerca fascicoli per numero di 
decreto ingiuntivo 
RicercaDataIscrizioneRuolo 
Ricerca fascicoli per data di 
iscrizione a ruolo, rito e giudice 
RicercaDataPrimaUdienza 
Ricerca fascicoli per giudice e 
data citazione/prima udienza 
RicercaDataProssimaUdienza 
Ricerca fascicoli per giudice e 
data prossima udienza 
 
 
 
Registro Volontaria Giurisdizione: 
Interrogazione 
Descrizione 
RicercaGiudici 
Elenco giudici per ufficio 
RicercaRuoloGenerale 
Ricerca fascicoli per numero di 
registro 
RicercaDataIscrizioneRuolo 
Ricerca fascicoli per data di 
iscrizione a ruolo, rito e giudice 
RicercaDataProssimaUdienza 
Ricerca fascicoli per giudice e 
data prossima udienza 
2.7 Elenco Interrogazioni Registri SIECIC (dati anonimizzati) 
Di seguito l’elenco delle interrogazioni attivabili attraverso il metodo execute ed una 
breve descrizione delle stesse. Per la descrizione relativa alla semantica dei singoli 
parametri si rimanda agli allegati presenti nella directory “Catalog/Consultazione 
Registri/SIECIC”. 
 
Interrogazione 
Descrizione 
RicercaGiudici 
Elenco giudici per ufficio

21 
 
RicercaRuoloGeneralePC 
Ricerca 
fascicoli 
procedure 
concorsuali 
per 
numero 
di 
registro generale 
RicercaSentenzaPC 
Ricerca 
fascicoli 
procedure 
concorsuali 
per 
numero 
di 
sentenza 
RicercaDebitorePC 
Ricerca 
fascicoli 
procedure 
concorsuali per debitore 
RicercaStatoPassivoPC 
Ricerca 
fascicoli 
procedure 
concorsuali per data prossima 
udienza del passivo e giudice 
RicercaRuoloGeneraleESM 
Ricerca 
fascicoli 
esecuzioni 
mobiliari per numero di registro 
generale 
RicercaVenditeESM 
Ricerca 
fascicoli 
esecuzioni 
mobiliari 
per 
dataudienzadi 
vendita 
RicercaRuoloGeneraleESIM 
Ricerca 
fascicoli 
esecuzioni 
immobiliari per numero di 
registro generale 
RicercaVenditeESIM 
Ricerca 
fascicoli 
esecuzioni 
immobiliari per data udienza di 
vendita 
 
2.8 Elenco Interrogazioni Registro Civile Cassazione 
Di seguito l’elenco delle interrogazioni attivabili attraverso il metodo execute ed una 
breve descrizione delle stesse. Per la descrizione relativa alla semantica dei singoli 
parametri si rimanda agli allegati presenti nella directory “Catalog/Consultazione 
Registri/CASSCI”. 
 
Interrogazione 
Descrizione 
QC_Ricorsi 
Permette la ricerca di ricorsi 
all'interno della base dati del 
registro.

22 
 
QC_ProvvedimentiImpugnati 
Ricerca 
degli 
estremi 
del 
provvedimento impugnato da un 
ricorso 
QC_PartiRicorso 
Elenco delle parti di un ricorso 
QC_DifensoriRicorso 
Elenco dei difensori di un 
ricorso 
QC_ElencoMemorie 
Elenco delle memorie depositate 
di un ricorso 
QC_UdienzeRicorso 
Elenco delle udienze di un 
ricorso. 
QC_EsitoRicorso 
Dettagli dell'esito di un ricorso. 
QC_Controricorso 
Elenco dei contro ricorsi di un 
ricorso. 
QC_SentenzeRicorso 
Elenco dei contro ricorsi di un 
ricorso 
NotificheDaRitirare 
 
QC_Ricorsi105Giorni 
Elenca le notifiche da ritirare in 
cancelleria 
Elenco dei ricorsi iscritti 105 
giorni lavorativi dalla data 
corrente. 
QC_FascicoloInformatico 
 
Dato il ricorso restituisce gli 
identificativi e i metadati dei 
documenti 
depositati 
telematicamente relativi ricorso. 
 
2.9 Elenco Interrogazioni Registro Penale Cassazione 
Di seguito l’elenco delle interrogazioni attivabili attraverso il metodo execute ed una 
breve descrizione delle stesse. Per la descrizione relativa alla semantica dei singoli 
parametri si rimanda agli allegati presenti nella directory “Catalog/Consultazione 
Registri/CASSPE”. 
 
Interrogazione 
Descrizione

23 
 
QP_Ricorsi 
Permette la ricerca di ricorsi 
all'interno della base dati del 
registro. 
QP_ProvvedimentiImpugnati 
Ricerca 
degli 
estremi 
del 
provvedimento impugnato da un 
ricorso 
QP_PartiDifensori 
Elenco delle parti e dei relativi 
difensori di un ricorso. 
QP_UdienzeRicorso 
Elenco delle udienze di un 
ricorso. 
QP_EsitoRicorso 
Dettagli dell'esito di un ricorso. 
QP_ElencoRestituzioni 
Restituzione degli atti legati ad 
un ricorso. 
QP_SentenzeRicorso 
Elenco dei contro ricorsi di un 
ricorso. 
NotificheDaRitirare 
Elenca le notifiche da ritirare in 
cancelleria. 
 
2.10 Elenco Interrogazioni Registri Civile Cassazione (dati 
anonimizzati) 
Di seguito l’elenco delle interrogazioni attivabili attraverso il metodo execute ed una 
breve descrizione delle stesse. Per la descrizione relativa alla semantica dei singoli 
parametri si rimanda agli allegati presenti nella directory “Catalog/Consultazione 
Registri/CASSCI”. 
Registro Civile: 
Interrogazione 
Descrizione 
QC_RicercaRicorsiPerNumero 
Ricerca il ricorso dato il numero 
del ricorso 
QC_RicercaRicorsiPerProvvedimento 
Ricerca il ricorso dato il nuemro 
del provvedimento impugnato. 
QC_DettaglioRicorso 
Dato il ricorso restituisce il 
dettaglio del ricorso. 
QC_Uffici 
Elenco degli uffici nazionali

24 
 
 
 
2.11 Elenco Interrogazioni Registri Penale Cassazione (dati 
anonimizzati) 
Di seguito l’elenco delle interrogazioni attivabili attraverso il metodo execute ed una 
breve descrizione delle stesse. Per la descrizione relativa alla semantica dei singoli 
parametri si rimanda agli allegati presenti nella directory “Catalog/Consultazione 
Registri/CASSPE”. 
Registro Penale: 
Interrogazione 
Descrizione 
QP_RicercaRicorsiPerNumero  
Ricerca il ricorso dato il numero 
del ricorso 
QP_RicercaRicorsiPerProvvedimento 
Ricerca il ricorso dato il numero 
del provvedimento impugnato.  
QP_DettaglioRicorso 
Dato il ricorso restituisce il 
dettaglio del ricorso. 
 
2.12 Troubleshooting 
Vengono riportati i casi più comuni di errore in cui è possibile incorrere con la relativa 
soluzione possibile: 
Errore 
Soluzione 
<faultstring> 
L'utente 
'26D5561EE86C6318E040A8C0091477A0' 
non puo' eseguire l'operazione 'execute' 
</faultstring> 
 Verificare il codice 
ufficio 
inserito 
(nell’headergroup) 
 
 Verificare il codice 
ruolo 
inserito 
(nell’headerrole)  
 
<faultstring> 
Can not set value type 'integer' from string 
</faultstring> 
 
 Verificare che il tipo 
dei parametri di input 
sia 
coerente 
con 
quanto richiesto nel 
getServiceDescriptor

25 
 
<faultstring> 
         Unsupported value type 'stri' 
</faultstring> 
 
 Il tipo di parametro 
inserito in input non è 
riconosciuto 
<faultstring> 
Parameter not resolved 'TIPO' 
</faultstring> 
 Il parametro richiesto 
in input non è stato 
inserito 
 
<faultstring> 
CODICEFISCALE 
</faultstring> 
 Valorizzare il campo 
dell’header X-WASP-
User con il Codice 
Fiscale del soggetto o 
la 
coppia 
Codice 
Fiscale, 
Codice 
Univoco 
 
<faultstring> 
Service 
'RicercaInformazioniFascicoloPerTipoo' 
non trovato 
</faultstring> 
 
 Correggere il nome del 
servizio invocato 
Erroreaperturacursore 
 L’operazione invocata 
ha generato errore nel 
backend.

26 
 
3 Accesso ai Documenti 
3.1 Parametri specifici 
3.1.1 
Header http 
Il codice fiscale del soggetto che ha invocato la richiesta è indicato nell’header HTTP 
della request (proprietà X-WASP-User). Con la modifica del Registro delle Pubbliche 
Amministrazione, ogni amministrazione viene individuata da una coppia di valori, il 
codice fiscale e il codice univoco. Se vi vuole consultare i fascicolo con il ruolo Parte 
e la parte è una Pubblica Amministrazione, allora sarà necessario inserire nell’header 
(proprietà X-WASP-User) sia il codice fiscale che il codice univoco, nel seguente 
modo: 
CODICEFISCALE=XXXXX;CODICEUNIVOCO=YYYY 
Il codice univoco se diverso dal codice fiscale, individua articolazioni locali o 
territoriali della Pubblica Amministrazione. Codice fiscale e codice univoco 
corrispondono quando si tratta di una pubblica amministrazione centrale.  
Header SOAP 
I messaggi SOAP rivolti ai servizi di backend offerti dagli Uffici Giudiziari presentano 
un SOAP header con la seguente forma: 
<soapenv:Header><ws:InvocationDomain name="JPW" role="YYY" 
group=”XXXXXXXX” 
soapenv:mustUnderstand="1" 
soapenv:actor="http://schemas.xmlsoap.org/soap/actor/next
" xmlns:ws="http://www.netserv.it/anag/security"/> 
dove: 
 per poter accedere al servizio che mette a disposizione il catalogo delle tipologie 
di interrogazione (query e relative metainformazioni) dei servizi di back end 
degli Uffici Giudiziari: 
o role: assume il valore “JPW”  
o group: assume il valore “jpwusers” 
 per le richieste di consultazione (metodo execute) invocate dagli utenti esterni 
abilitati: 
o role: assume i valori indicati nella tabella di seguito riportata 
o group: contiene il codice dell’Ufficio Giudiziario destinatario del 
messaggio. 
 
N.B. Per l’invocazione dei servizi di back end della Corte di Cassazione, all’interno 
dell’Invocation Domain, non deve essere specificato il parametro “group”.

27 
 
 
 
 
 
 
 
Elenco dei valori relativi all’attributo role per l’invocazione del metodo execute: 
 
SICID 
AVV,CTU, PARTE, NOT, TUT, AUS 
SIECIC 
AVV,CTU,PARTE, CUS, DEL 
SIGP 
AVV, CTU, PARTE 
CASSAZIONE AVV, PARTE 
3.1.2 
Semantica dell’attributo role e del parametro idruolojpw 
Le informazioni presenti nell’header soap sono necessarie alla gestione della sicurezza 
ed in particolare permettono la gestione dell’autorizzazione all’esecuzione dei servizi. 
In particolare il parametro role permette di invocare web service diversi a seconda del 
ruolo specificato e quindi servizi dedicati alle consultazioni di avvocati (AVV), 
consulenti tecnici d’ufficio, periti/esperti e curatori/commissari/liquidatori (CTU), parti 
(PARTE), 
custodi 
(CUS), 
delegati 
(DEL), 
Notai/Ufficiali 
(NOT), 
Curatori/Tutori/Amm. di sostegno (TUT) e  Ausiliari Incaricati (AUS). Il valore 
role=JPW è necessario per invocazioni di servizi per cui la specifica del ruolo del 
soggetto non è necessaria ovvero servizi di carattere generale presenti nel sistema di 
consultazione.  
Le problematiche di visibilità sono invece risolte attraverso l’utilizzo del valore 
idruolojpw presente tra i parametri di input delle consultazioni; in pratica tale parametro 
permette di specificare rispetto a quale tipologia di incarico si vogliono filtrare i dati. 
Ad esempio se un CTU è curatore/commissario/liquidatore ma nel parametro 
idruolojpw si indica CTU non vengono restituiti i procedimenti in cui il soggetto è 
incaricato come curatore/commissario/liquidatore (valore CUR) ma solo quelli dove è 
incaricato con altre tipologie di consulenza. Allo stesso modo se un avvocato è anche 
curatore e nel parametro idruolojpw si indica AVV vengono restituiti i soli fascicoli in 
cui il soggetto costituito in giudizio come difensore e non quelli dove il soggetto è 
incaricato come curatore/commissario/liquidatore. Per quest’ultima invocazione dovrà 
utilizzare il valore CUR.  
Rispetto alle logiche generali di cui sopra è necessario sottolineare che nel contesto 
delle consultazioni di SICID e SIGP il parametro idruolojpw nel body del messaggio 
soap è stato omesso e il sistema utilizza direttamente quanto presente nell’header anche 
per le problematiche di visibilità sui dati. Lo stesso discorso vale per la gestione

28 
 
l’invocazione dei servizi di accesso al fascicolo informatico in cui si sfrutta anche per 
la visibilità la sola informazione presente nell’header soap. 
Si noti inoltre che nel contesto delle consultazioni SIECIC il parametro 
idruolojpw=AVV comprende anche la visibilità dei delegati (ed è quindi corretto parlare 
di profilo Avvocato/Delegato).  
3.2 Elenco consultazionifascicoloinformatico 
I servizi descritti nel contesto del presente paragrafo consentono di accedere al 
contenuto del fascicolo informatico inteso come insieme dei documenti depositati dalle 
parti, dai consulenti e ausiliari del giudice e dal giudice stesso (compresi gli eventuali 
documenti allegati).  
La fruizione dei servizi di accesso al patrimonio documentale di ogni singolo fascicolo 
avviene tramite l’esposizione di un opportuno web-service nell’infrastruttura SOAP 
implementata dal Gestore Locale.  
Di seguito sono descritte con maggiore dettaglio le interfacce delle operazioni messe a 
disposizione dal servizio dove il valore di NAMESPACE assume valori distinti in base 
al registro scelto per la consultazione: 
 
SICID 
 Contenzioso Civile = urn:BEAFascicoloInformatico-distr 
 Diritto del Lavoro = urn:BEAFascicoloInformatico-distr 
 Volontaria Giurisdizione =urn:BEAFascicoloInformatico-distr 
Di seguito l’interfaccia dei metodi disponibili.  
Operazione: 
download Documento 
Descrizione: 
Estrae contenuto documento 
Parametri: 
idUtenteCorrente: 
codice fiscale del soggetto che effettua la richiesta 
idCat: 
id documento 
original: 
richiesta copia originale (true/false):   
- se valorizzato a “true” : 
 
Se si tratta di documento in formato CAdES restituisce il contenuto 
del documento firmato che si trova nel repository ovvero .p7m 
 
Se si tratta di un documento PAdES restituisce il file contenuto nel 
repository documentale cosi com’è ovvero firmato. 
- se valorizzato a “false” :

29 
 
 
Per il CAdES: restituisce un documento copia di quello nel repository 
dopo la rimozione delle informazioni di firma dall’atto e l’aggiunta 
della coccardina (con le informazioni del firmatario) e delle eventuali 
informazioni in blu.  
 
Per il PAdES: restituisce un documento copia di quello nel repository 
dopo l’aggiunta di eventuali informazioni in blu. 
Risultato: 
download del documento 
 
Operazione: 
calcolaHash 
Descrizione: 
Calcola il hash MD5 del documento 
Parametri: 
idUtenteCorrente: 
codice fiscale del soggetto che effettua la richiesta 
idDoc: 
id documento 
Risultato: 
Stringa del codice hash MD5 calcolato sul documento 
 
Operazione: 
estraiMasterDetailAtto 
Descrizione: 
Ricerca profilo documento eprofiloallegati associati 
Parametri: 
idUtenteCorrente: 
codice fiscale del soggetto che effettua la richiesta 
idDoc: 
id del documento 
registro: 
registro su cui effettuare l’invocazione (paragrafo 2.1) 
ruoloApplicativo: 
ruolo del soggetto che effettua la richiesta 
Risultato: 
BEAMasterUfficialeVO: 
per maggiori informazioni fare riferimento al wsdl 
 
Operazione: 
estraiProfiloDocumento

30 
 
Descrizione: 
Ricerca profilo appartenente al documento 
Parametri: 
idUtenteCorrente: 
codice fiscale del soggetto che effettua la richiesta 
idDoc: 
id del documento 
registro: 
registro su cui effettuare l’invocazione (paragrafo 2.1) 
ruoloApplicativo: 
ruolo del soggetto che effettua la richiesta 
Risultato: 
BEADocumentoUfficialeVO: 
per maggiori informazioni fare riferimento al wsdl 
 
Operazione: 
estraiListaAttiFascicolo 
Descrizione: 
Ricerca profilo atti associati ad un fascicolo 
Parametri: 
idUtenteCorrente: 
codice fiscale del soggetto che effettua la richiesta 
idFascicolo: 
id del repositoryfascicolo 
(“idfascicolo” estratto da  EstraiProfiloDocumento) 
registro: 
registro su cui effettuare l’invocazione(paragrafo 2.1) 
ruoloApplicativo: 
ruolo del soggetto che effettua la richiesta 
Risultato: 
ArrayOfBEADocumentoFascicoloVO: 
per maggiori informazioni fare riferimento al wsdl 
 
Per le definizioni tramite WSDL dei web service che espongono i metodi sopra descritti 
si 
rimanda 
agli 
allegati 
presenti 
nella 
directory 
“WSDL\Accesso 
ai 
Documenti\Fascicolo Informatico/SICID”. 
 
SIECIC

31 
 
 Procedure Concorsuali = http://elsagdatamat.com/bea/pct/siecic/ws/fascicolo 
 Esecuzioni Mobiliari = http://elsagdatamat.com/bea/pct/siecic/ws/fascicolo 
 Esecuzioni Immobiliari = http://elsagdatamat.com/bea/pct/siecic/ws/fascicolo 
 
Per invocare le operazioni è necessario inserire il campo X-WASP-User nell’header 
HTTP della request con il codice fiscale del soggetto che effettua la richiesta, altrimenti 
il sistema segnalerà l’errore “BEA_CLI: ID Utente non impostato”.  
Con la modifica del Registro delle Pubbliche Amministrazione, ogni amministrazione 
viene individuata da una coppia di valori, il codice fiscale e il codice univoco. Se vi 
vuole consultare i fascicolo con il ruolo Parte e la parte è una Pubblica 
Amministrazione, allora sarà necessario inserire nell’header (proprietà X-WASP-User) 
sia il codice fiscale che il codice univoco, nel seguente modo: 
CODICEFISCALE=XXXXX;CODICEUNIVOCO=YYYY 
Il codice univoco se diverso dal codice fiscale, individua articolazioni locali o 
territoriali della pubblica amministrazione. Codice fiscale e codice univoco 
corrispondono quando si tratta di una pubblica amministrazione centrale.  
 
Di seguito l’interfaccia dei metodi disponibili.  
Operazione: 
downloadDocumento 
Descrizione: 
Estrae  contenuto documento 
Parametri: 
idDoc: 
id documento 
original: 
richiesta copia originale (true/false):   
- se valorizzato a “true” : 
 
Se si tratta di documento in formato CAdES restituisce il contenuto 
del documento firmato che si trova nel repository ovvero .p7m 
 
Se si tratta di un documento PAdES restituisce il file contenuto nel 
repository documentale cosi com’è ovvero firmato. 
- se valorizzato a “false” : 
 
Per il CAdES: restituisce un documento copia di quello nel repository 
dopo la rimozione delle informazioni di firma dall’atto e l’aggiunta 
della coccardina (con le informazioni del firmatario) e delle eventuali 
informazioni in blu.  
 
Per il PAdES: restituisce un documento copia di quello nel repository 
dopo l’aggiunta di eventuali informazioni in blu. 
Risultato: 
download del documento

32 
 
 
Operazione: 
calcolaHash 
Descrizione: 
Calcola il hash MD5 del documento 
Parametri: 
idDoc: 
id documento 
Risultato: 
Stringa del codice hash MD5 calcolato sul documento nel 
repository 
 
 
Operazione: 
estraiMasterDetailAtto 
Descrizione: 
Ricerca profilo documento e profilo allegati associati 
Parametri: 
idDoc: 
id del documento 
Risultato: 
BEAMasterUfficialeVO: 
per maggiori informazioni fare riferimento al wsdl 
 
Operazione: 
estraiProfiloDocumento 
Descrizione: 
Ricerca profilo documento 
Parametri: 
idDoc: 
id del documento 
Risultato: 
BEADocumentoUfficialeVO: 
per maggiori informazioni fare riferimento al wsdl 
 
Operazione: 
estraiListaAttiFascicolo 
Descrizione: 
Ricerca profilo atti associati ad un fascicolo 
Parametri: 
idFascicolo: 
id del repository fascicolo

33 
 
(“idfascicolo” estratto da  EstraiProfiloDocumento) 
Risultato: 
ArrayOfBEADocumentoFascicoloVO: 
per maggiori informazioni fare riferimento al wsdl 
 
Per le definizioni tramite WSDL dei web service che espongono i metodi sopra descritti 
si 
rimanda 
agli 
allegati 
presenti 
nella 
directory 
“WSDL\Accesso 
ai 
Documenti\Fascicolo Informatico/SIECIC”. 
 
SIGP 
 Procedimenti davanti al Giudice di Pace = urn:sigp-consultazioneDocumenti 
Di seguito l’interfaccia dei metodi disponibili.  
 
Operazione: 
ricercaAtti 
Descrizione: 
Ricerca gli atti associati al fascicolo informatico 
Parametri: 
numRuolo: 
il numero di ruolo del fascicolo 
annoRuolo: 
anno di iscrizione del fascicolo 
Risultato: 
viene restituito un array con gli identificativi degli atti associati al 
fascicolo ricercato. 
 
Operazione: 
downloadAtto 
Descrizione: 
Restituisce il contenuto del documento ricercato 
Parametri: 
idrepeatto: 
identificativo dell’atto ( restituito dall’invocazione del servizio 
“ricercaAtti”) 
Risultato: 
viene restituito il contenuto del documento nel formato di un 
DataHandler.

34 
 
Per le definizioni tramite WSDL dei web service che espongono i metodi sopra descritti 
si 
rimanda 
agli 
allegati 
presenti 
nella 
directory 
“WSDL\Accesso 
ai 
Documenti\Fascicolo Informatico/SIGP”. 
 
CASSAZIONE 
 Cassazione Civile = http://elsagdatamat.com/bea/pct/cassazione/ws/fascicolo 
 
Di seguito l’interfaccia dei metodi disponibili.  
Operazione: 
download Documento 
Descrizione: 
Estrae contenuto documento 
Parametri: 
idCat: 
id documento 
original: 
richiesta copia originale (true/false):   
- se valorizzato a “true” : 
 
Se si tratta di documento in formato CAdES restituisce il contenuto 
del documento firmato che si trova nel repository ovvero .p7m 
 
Se si tratta di un documento PAdES restituisce il file contenuto nel 
repository documentale cosi com’è ovvero firmato. 
- se valorizzato a “false” : 
 
Per il CAdES: restituisce un documento copia di quello nel repository 
dopo la rimozione delle informazioni di firma dall’atto e l’aggiunta 
della coccardina (con le informazioni del firmatario) e delle eventuali 
informazioni in blu.  
 
Per il PAdES: restituisce un documento copia di quello nel repository 
dopo l’aggiunta di eventuali informazioni in blu. 
Risultato: 
download del documento 
 
Operazione: 
calcolaHash 
Descrizione: 
Calcola il hash MD5 del documento 
Parametri: 
idDoc: 
id documento 
Risultato: 
Stringa del codice hash MD5 calcolato sul documento

35 
 
Per le definizioni tramite WSDL dei web service che espongono i metodi sopra descritti 
si 
rimanda 
agli 
allegati 
presenti 
nella 
directory 
“WSDL\Accesso 
ai 
Documenti\Fascicolo Informatico\Cassazione”. 
 
 
3.3 Archivio Giurisprudenziale Nazionale 
I servizi descritti nel contesto del presente paragrafo consentono di accedere al 
contenuto dell’archivio giurisprudenziale inteso come insieme dei provvedimenti resi 
pubblici dalle cancellerie. 
La fruizione dei servizi di accesso al patrimonio documentale dell’archivio 
giurisprudenziale avviene tramite l’esposizione di due web-service nell’infrastruttura 
SOAP: uno di ricerca dei dati relativi ai provvedimenti pubblicati e uno per il download 
del pdf del documento pubblicato. 
3.3.1 
Ricerca provvedimenti 
Il primo web service è implementato secondo le medesime logiche già descritte al 
paragrafo 2.1 con la differenza che il namespace da utilizzare è il seguente: 
“urn:CMBackEndRd_qb” e gli url di invocazione sono i seguenti: 
 Nel caso specifico del proxy per i PdA la url sarà 
https://pda.processotelematico.giustizia.it/AGN/ricerche 
 
 Nel caso specifico del proxy per le software house la url sarà: 
https://ext.processotelematico.giustizia.it/AGN/ricerche 
Si specifica che questo servizio, come si può dedurre dalle suddette URL, è 
centralizzato a livello nazionale pertanto non è necessario definire un header SOAP 
contenente un elemento InvocationDomain. 
Di seguito l’unica interrogazione disponibile: 
 
Interrogazione 
Descrizione 
giurisprudenza 
Ricerca nell’Archivio Giurisprudenziale 
Nazionale 
Per la definizione tramite WSDL del web service che espone le interrogazioni di cui 
sopra si rimanda al file BEAConsultazioni-giur.wsdl presente nella directory 
“WSDL\Accesso ai Documenti\Archivio Giurisprudenziale\SICID-SIECIC\ricerca”. 
Per la descrizione dei parametri in output si rimanda al file catalog.xml presente nella 
cartella 
“Catalog\Accesso 
ai 
Documenti\Archivio 
Giurisprudenziale\SICID-
SIECIC\ricerca”.

36 
 
Di seguito si riporta una descrizione più dettagliata di alcuni dei parametri di input 
disponibili. 
 
Parametri 
Descrizione 
CODICEUFFICIO, 
CODICEGL, 
CF_GIUDICE, NOMEGIUDICE ... 
Parametri di ricerca che permettono di 
filtrare i risultati in base ai metadati del 
documento. 
DAL_DEPOSITO 
AL_DEPOSITO 
Tramite questi parametri è possibile 
definire la finestra temporale nella quale 
sono 
stati 
depositati 
i 
documenti 
interessati 
PAGENO 
PAGESIZE 
Tramite 
questi 
parametri, 
in 
combinazione con uno o più parametri di 
ordinamento, è possibile controllare la 
paginazione dei risultati. Ad esempio 
selezionando un PAGESIZE di 30, un 
PAGENO pari a uno, ed ordinando i 
risultati 
per 
ATTESTAZIONE 
è 
possibile ottenere i primi 30 documenti 
pubblicati. 
Incrementando 
poi 
PAGENO, si otterranno i secondi 30 e 
così via. I parametri di ordinamento 
disponibili corrispondono con i parametri 
di output del servizio.  
TESTO 
Questo parametro permette la ricerca 
testuale sul contenuto dei documenti 
pubblicati. É possibile usare il carattere * 
come wildcard nella ricerca. In questo 
modo è possibile ad esempio ricercare 
tutte le forme flesse di una parola 
specificandone la radice, seguita da *. Ad 
esempio 
“lavor*” 
restituirà 
una 
corrispondenza, tra le altre, con le parole 
“lavoro”, 
“lavorare”, 
“lavoratore”, 
“lavoratrice”. É possibile inoltre usare 
operatori logici AND e OR. 
TIPOCONTENUTO 
Specificando 
questo 
parametro, 
si 
restringe la ricerca ad un solo tipo di 
documento pubblicato, dove con tipo di 
documento si intende il formato con cui 
questo è stato inserito nell’archivio.  Il

37 
 
tipo TEXT restituisce i documenti pdf il 
cui testo è stato indicizzato, ed é quindi 
ricercabile 
tramite 
parole 
chiave 
all’interno del testo. Il tipo IMG 
restituisce i documenti scansionati, per i 
quali non é disponibile la ricerca testuale.  
Si riporta a titolo di esempio un’interrogazione che recupera i primi 30 documenti, 
ordinati per anno di ruolo, indicizzati come testo e contenenti una qualsiasi parola con 
radice “lavor” oppure la parola civile: 
<soapenv:Envelope 
xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" 
xmlns:urn="urn:CMBackEndRd_qb"> 
   <soapenv:Header/> 
   <soapenv:Body> 
      <urn:execute> 
         <name>giurisprudenza</name> 
         <valueSet> 
           <value name="TESTO" type="string">lavor* OR civile</value> 
 
      <value name="TIPOCONTENUTO" type="string">TEXT</value> 
 
      <value name="PAGESIZE" type="string">30</value> 
 
      <value name="PAGENO" type="string">1</value> 
         </valueSet> 
         <orderBy> 
          <entry property="ANNORUOLO" mode="asc"/> 
         </orderBy> 
      </urn:execute> 
   </soapenv:Body> 
</soapenv:Envelope> 
 
3.3.2 
Download provvedimento 
Per permettere il download del documento pubblicato nell’archivio giurisprudenziale 
sarà necessario invocare un web service specifico adottando le medesime logiche già 
descritte al paragrafo 3.1. 
Operazione: 
downloadArchivioGiur 
Descrizione: 
Download del provvedimento pubblicato nell’archivio.

38 
 
Parametri: 
idCatOriginale: 
Identificativo dell’atto così come restituito dal servizio di ricerca 
descritto al paragrafo 3.3.1 attraverso il parametro di output 
IDATTO 
Risultato: 
Atto richiesto se trovato, null altrimenti. L'atto richiesto è fornito 
in allegato all'envelope di risposta. 
Si specifica che tale servizio, a differenza di quello di ricerca descritto al paragrafo 
3.3.1, è distrettuale, pertanto le URL da usare saranno quelle specificate nel paragrafo 
6. Il codice del distretto (da inserire nella URL) e il codice ufficio (da inserire 
nell’InvocationDomain) relativi all’atto che si vuole scaricare potranno essere ricavati 
dal risultato dal servizio di ricerca descritto al paragrafo 3.3.1. 
Per la definizione tramite WSDL del web service che espone i metodi sopra descritti si 
rimanda al file BEAArchivioGiurisprudenzialeNazionale.wsdl e presente nella 
directory “WSDL\Accesso ai Documenti\Archivio Giurisprudenziale\SICID-SIECIC”. 
3.4 Download sentenze per i registri penale e civile della 
Cassazione 
Il servizio qui di seguito descritto permette il download delle sentenze per i registri 
civile e penale della cassazione. 
Il servizio a seconda del registro di interesse è disponibile rispettivamente ai 
namespace: 
 http://www.giustizia.it/gl/sgr/cassazione/consultazioneSentenzeCiviliper 
il 
registro civile 
 http://www.giustizia.it/gl/sgr/cassazione/consultazioneSentenzePenali per il 
registro penale 
 
Operazione: 
download 
Descrizione: 
Download della sentenza corrispondente agli estremi (anno e 
numero) specificati. 
Parametri: 
annoSentenza: 
Anno della sentenza da richiedere 
numeroSentenza: 
Numero della sentenza da richiedere 
Risultato: 
Atto richiesto se trovato, null altrimenti. L'atto richiesto è fornito 
in allegato all'envelope di risposta.

39 
 
Per la definizione tramite WSDL del web service che espone i metodi sopra descritti si 
rimanda al file consultazione-sentenze.wsdl e presente nella directory “WSDL\Accesso 
ai Documenti\Archivio Giurisprudenziale\Cassazione”. 
3.5 Download ricevute PEC notifiche per i registri civile e 
penale della Cassazione 
Il servizio permette il download della ricevuta PEC (Accettazione, Non Accettazione, 
Mancata o Avvenuta Consegna) che chiude il flusso di notifica per i registri civile e 
penale della Cassazione. 
Per 
entrambi 
registri 
il 
servizio 
è 
esposto 
con 
il 
namespace 
'http://www.giustizia.it/gl/sgr/cassazione/ricevutePEC'. 
 
Operazione: 
download 
Descrizione: 
Download della ricevuta per il messaggio indicato 
Parametri: 
msgId: 
identificatore del messaggio relativo alla notifica. 
Gli identificatori per tali messaggi sono restituiti attraverso il 
servizio di consultazione relativo alle notifiche da ritirare. 
Risultato: 
Messaggio di posta (rfc822) relativo alla ricevuta di PEC che ha 
concluso la notifica relativa al messaggio indicato. 
Per la definizione tramite WSDL del web service che espone i metodi sopra descritti si 
rimanda al file registro-ricevute-pec.wsdl presente nella directory “WSDL\Accesso ai 
Documenti\Fascicolo Informatico\Cassazione”.

40 
 
4 Servizi per le Richieste Copie (servizio 
ancora non rilasciato) 
I servizi di gestione delle richieste copie consentono di richiedere copie dei documenti 
presenti nel contesto del fascicolo informatico nonché di verificare lo stato delle 
richieste effettuate. 
La fruizione di tali servizi avviene tramite l’esposizione di due web-service 
nell’infrastruttura SOAP implementata dal Gestore Locale. 
Il primo web service permette di inoltrare la richiesta e gestire i pagamenti, per questo 
web service il namespace da utilizzare è “urn:RichiestaCopie”. 
Di seguito l’interfaccia dei metodi disponibili.  
Operazione: 
InvioRichiesta 
Descrizione: 
Invio richiesta di copie 
Parametri: 
per informazioni consultare il wsdl 
Risultato: 
identificativo della richiesta 
 
Operazione: 
EstremiPagamento 
Descrizione: 
Inoltra gli estremi del pagamento effettuato per la richiesta copia 
specifica 
Parametri: 
idRichiesta: 
identificativo della richiesta 
tipo: 
tipo del pagamento 
estremi: 
testo libero (dettagli del pagamento) 
importo: 
importo del pagamento 
Risultato: 
nessuno 
 
Operazione: 
RichiestaDocumentazioneFascicolo 
Descrizione: 
Inoltra una richiesta dell’intera documentazione fascicolo

41 
 
Parametri: 
fascicolo: 
informazioni sul fascicolo (numero, anno, sub procedimento…) 
formato: 
formato della richiesta 
numero: 
numero di copie 
procura: 
testo della procura 
Risultato: 
identificativo della richiesta 
 
Per la definizione tramite WSDL del web service che espone i metodi sopra descritti si 
rimanda al file richiesta-copie.wsdl presente nella directory “WSDL\Richieste 
Copie\SICID_SIECIC”. 
Il secondo web service è implementato secondo le medesime logiche già descritte al 
paragrafo 2.1 con la differenza che il namespace da utilizzare è il 
seguente:“urn:RichiestaCopie-consultazioni-distr”.  
Per la descrizione dei parametri si rimanda al file catalog presente nella directory 
“Catalog\Richieste Copie” mentre di seguito è riportato l’elenco delle interrogazioni 
disponibili. 
Di seguito le interrogazioni disponibili. 
Interrogazione 
Descrizione 
ProfiloRichiesta 
Dati descrittivi della richiesta copia 
RicercaRichieste 
Elenco richieste effettuate 
 
Per la definizione tramite WSDL del web service che espone le interrogazioni di cui 
sopra si rimanda al file qbuilder-richiestacopie-distr.wsdl presente nella directory 
“WSDL\Richieste Copie\SICID_SIECIC”.

42 
 
5 Altri Servizi 
5.1 Parametri specifici 
I servizi descritti all’interno del presente capitolo, a differenza di quelli espressi 
all’interno dei capitoli 2 e 3, non sono esposti dai backend degli Uffici Giudiziari, ma 
sono servizi backend offerti dal Portale dei Servizi Telematici e dal REGINDE.  
I messaggi SOAP rivolti a questi servizi non prevedono l’inserimento di parametri 
specifici all’interno dell’header SOAP e dell’header http, essendo servizi di natura 
differente rispetto ai precedenti. 
Gli unici servizi che prevedono l’inserimento di parametri all’interno del messaggio 
SOAP è "Scambio messaggi tra curatore fallimentare e giudice delegato" descritto al 
paragrafo 5.7. dove è presente una descrizione approfondita di come deve essere 
formulato un messaggio SOAP relativo a tali servizi.    
5.2 Catalogo degli Uffici Giudiziari 
I servizi del Catalogo degli Uffici Giudiziari consentono di reperire informazioni sugli 
uffici  giudiziari e i punti di accesso gestiti dal Portale dei Servizi Telematici. 
Il 
namespace 
da 
utilizzare 
è: 
“http://www.giustizia.it/serviziTelematici/serviziGenerici”. 
Di seguito l’interfaccia dei metodi disponibili.  
Operazione: 
getCertificato 
Descrizione: 
Download certificato di un ufficio 
Parametri: 
codice ufficio 
Risultato: 
download certificato 
 
Operazione: 
getComuni 
Descrizione: 
Ricerca elenco comuni 
Parametri: 
codice distretto: 
codice distretto 
gruppo:  
non obbligatorio, valorizzabile con “C” per reperire i comuni di 
appartenenza degli uffici giudiziari del civile o “P” per reperire i 
comuni di appartenenza degli uffici giudiziari penali. Per retro 
compatibilità se non valorizzato il metodo restituisce i comuni di 
appartenenza degli uffici giudiziari del civile.

43 
 
Risultato: 
lista comuni 
 
 
Operazione: 
getDecreto 
Descrizione: 
 Download decreto 
Parametri: 
identificativo decreto 
Risultato: 
download decreto 
 
Operazione: 
getDistretti 
Descrizione: 
Ricerca elenco distretti 
Parametri: 
nessuno 
Risultato: 
lista distretti 
 
Operazione: 
getListaPda 
Descrizione: 
Ricerca elenco enti 
Parametri: 
ordinamento: 
0= ordina per descrizione PdA 
1= ordina per descrizione Ordine 
verso: 
ASC= ascendente 
DESC= discendente 
Risultato: 
lista Pda ordinata 
 
Operazione: 
getListaUfficiGiudiziari 
Descrizione: 
Ricerca elenco uffici giudiziari 
Parametri: 
distretto:

44 
 
distretto di appartenenza dell’ufficio giudiziario 
comune: 
comune di appartenenza dell’ufficio giudiziario 
tipoufficio: 
tipologia ufficio 
 
Risultato: 
lista uffici giudiziari 
 
Operazione: 
getListaUfficiGiudiziariDistretto 
Descrizione: 
Ricerca elenco uffici giudiziari del distretto 
Parametri: 
distretto di appartenenza degli uffici giudiziari 
 
Risultato: 
lista uffici giudiziari 
 
Operazione: 
getListaUfficiPenali 
Descrizione: 
Ricerca elenco uffici giudiziari penali 
Parametri: 
distretto:  
descrizione distretto di appartenenza dell’ufficio giudiziario 
comune: 
comune di appartenenza dell’ufficio giudiziario 
tipoufficio: 
codice tipologia ufficio 
 
Risultato: 
lista uffici giudiziari penali 
 
 
Operazione: 
getListUGElectroPay 
Descrizione: 
Ricerca elenco uffici giudiziari abilitati al Pagamento Telematico

45 
 
Parametri: 
distretto:  
distretto di appartenenza dell’ufficio giudiziario 
comune: 
comune di appartenenza dell’ufficio giudiziario 
tipoufficio: 
tipologia ufficio 
 
Risultato: 
lista uffici giudiziari 
 
Operazione: 
getNormativa 
Descrizione: 
Download normativa atti depositabili negli uffici giudiziali penali 
Parametri: 
idAttiDepositabili: 
identificativo dell’atto reperibile dai servizi getListaUfficiPenali e 
getUfficioPenale 
Risultato: 
download normativa 
 
Operazione: 
getRegioni 
Descrizione: 
Ricerca elenco Regioni 
Parametri: 
nessuno 
Risultato: 
lista Regioni 
 
 
Operazione: 
getRegistriFromUfficio 
Descrizione: 
Ricerca registri disponibili per consultazione pubblica 
Parametri: 
codice ufficio 
Risultato: 
lista registri

46 
 
Operazione: 
getRito 
Descrizione: 
Ricerca elenco Riti 
Parametri: 
codice registro 
Risultato: 
lista riti 
 
Operazione: 
getRuoliConsultazioni 
Descrizione: 
Ricerca informazioni per costruire invocazioni sulle consultazioni 
private 
Parametri: 
codiceFiscale: 
codice fiscale soggetto 
registro: 
registro di consultazione 
Risultato: 
valori per costruire invocazioni sulle consultazioni private, 
si rimanda al wsdl per maggiori informazioni 
 
Operazione: 
getTipiUfficio 
Descrizione: 
Ricercatipologie ufficio 
Parametri: 
comune: 
comune 
gruppo:  
non obbligatorio, valorizzabile con “C” per reperire le tipi civili o 
“P” per reperire i tipi penali. 
Per retro compatibilità se non valorizzo il metodo restituisce i tipi 
civili 
Risultato: 
lista tipologie ufficio 
 
Operazione: 
getTipoRicercaInformazioni 
Descrizione: 
Restituisce 
valori 
validi 
per 
l'input 
"TIPO" 
nella 
RicercaInformazioniFascicoliPerTipo

47 
 
Parametri: 
codice registro 
Risultato: 
lista valori tipo 
 
Operazione: 
getUfficiFromRegioni 
Descrizione: 
Restituisce 
valori 
validi 
per 
l'input 
"TIPO" 
nella 
RicercaInformazioniFascicoliPerTipo 
Parametri: 
codice regione 
Risultato: 
lista uffici 
 
Operazione: 
getUfficioGiudiziario 
Descrizione: 
Ricerca informazioni sull’ufficio giudiziario 
Parametri: 
codice ufficio 
Risultato: 
informazioni sull’ufficio, per maggiori informazioni si consulti il 
wsdl 
 
Operazione: 
getUfficioGiudiziarioByPec 
Descrizione: 
Restituisce ufficio giudiziario a partire dall’indirizzo di PEC 
Parametri: 
Indirizzo PEC 
Risultato: 
Ufficio giudiziario, per maggiori informazioni si consulti il wsdl 
 
Operazione: 
getUfficioPenale 
Descrizione: 
Ricerca informazioni sull’ufficio giudiziario 
Parametri: 
codice ufficio 
Risultato: 
informazioni sull’ufficio, per maggiori informazioni si consulti il 
wsdl

48 
 
 
Operazione: 
ricercaPda 
Descrizione: 
RestituisceelencoPdA 
Parametri: 
Ordine 
Risultato: 
lista PdA, per maggiori informazioni si consulti il wsdl 
 
Per la definizione tramite WSDL del web service che espone i metodi sopra descritti si 
rimanda all’allegato CatalogoServiziBeanService.wsdl presente nella directory 
“WSDL\Altri Servizi\Catalogo UG”. 
5.3 Accesso al ReGIndE 
I servizi di Accesso al Reginde consentono di effettuare ricerche di soggetti ed enti 
censiti nel ReGIndE.  
La fruizione di tali servizi avviene tramite l’esposizione di due web-service. 
Il primo web service di accesso al ReGIndE è descritto nel contesto dell’allegato 
ServiziInterrogazioneSoggetto.wsdl. Per questo web service il namespace da utilizzare 
è “http://www.giustizia.it/serviziTelematici/reginde/interrogazioniExt”. 
 
E' da ritenersi deprecato l'intero WSDL precedente, namespace 
http://www.giustizia.it/serviziTelematici/reginde/interrogazioni, pertanto 
soggetto ad essere eliminato nelle prossime release del ReGIndE. 
Di seguito l’interfaccia dei metodi disponibili.  
 
Operazione: 
dettagliSoggettoPerCodice 
Descrizione: 
Ricerca i dettagli di un soggetto per codice fiscale 
Parametri: 
codice fiscale esatto del soggetto 
Risultato: 
soggetto: 
per maggiori informazioni consultare il wsdl 
 
 
Operazione: 
dettagliSoggettoPerIndirizzo 
Descrizione: 
Ricerca i dettagli di un soggetto per indirizzo

49 
 
Parametri: 
indirizzo 
Risultato: 
soggetto: 
per maggiori informazioni consultare il wsdl 
 
Operazione: 
elencoPaginatoSoggetti 
Descrizione: 
Restituisce un elenco paginato di soggetti 
Parametri: 
da: 
indice inizio ricerca 
count: 
numero di soggetti da ricercare 
Risultato: 
lista di soggetti: 
per maggiori informazioni consultare il wsdl 
 
Operazione: 
isMembroDi 
Descrizione: 
Verifica che il soggetto appartenga all’Ente 
Parametri: 
codiceFiscale: 
codice fiscale del soggetto 
codiceEnte: 
codice dell’Ente 
Risultato: 
lista ruoli del soggetto censito 
 
Operazione: 
ricercaSoggetto 
Descrizione: 
Ricerca lista soggetti per cognome, nome o parti di essi e/o per 
codice dell'ente 
Parametri: 
cognome: 
cognome del soggetto eventualmente seguito dal carattere * 
nome:

50 
 
nome del soggetto eventualmente seguito dal carattere * 
codiceEnte: 
codice dell’Ente 
Risultato: 
lista di soggetti: 
per maggiori informazioni consultare il wsdl 
 
Operazione: 
ricercaSoggettoEx 
Descrizione: 
Ricerca lista soggetti per codice fiscale e/o indirizzo di PEC o 
parte di essi. 
Parametri: 
codiceFiscale: 
codice fiscale da ricercare o parte di esso 
indirizzo: 
indirizzo da ricercare o parte di esso 
Risultato: 
lista di soggetti: 
per maggiori informazioni consultare il wsdl 
 
Il secondo web service è descritto dal fileServiziInterrogazioneEnte.wsdl,sotto si 
riportano le operazioni disponibili.  
Il namespace da utilizzare è: 
“http://www.giustizia.it/serviziTelematici/reginde/interrogazioniExt”. 
 
E' da ritenersi deprecato l'intero WSDL precedente, namespace 
http://www.giustizia.it/serviziTelematici/reginde/interrogazioni, pertanto 
soggetto ad essere eliminato nelle prossime release del ReGIndE. 
Di seguito l’interfaccia dei metodi disponibili.  
Operazione: 
ricercaEnte 
Descrizione: 
Ricerca Ente per descrizione 
Parametri: 
descrizione: 
descrizione ente 
Risultato: 
enti: 
per maggiori informazioni consultare il wsdl

51 
 
 
 
Operazione: 
ricercaEnteEx 
Descrizione: 
Ricerca Ente per descrizione, tipo, codice fiscale e indirizzo pec. 
Descrizione e codice fiscale possono contenere la wild card '%'. 
Parametri: 
tipo: 
Tipo dell'ente da ricercare. Può assumere i valori: 
 Null, per cercare qualsiasi tipologia di ente 
 PPAA, per cercare solo le Pubbliche Amministrazioni 
 ENTE, per cercare solo gli enti. 
descrizione: 
Descrizione/denominazione dell'ente. Può contenere la wild card 
'%' 
codiceFiscale: 
Codice fiscale dell'ente. Può contenere la wild card '%'. 
indirizzoPec: 
Indirizzo Pec dell'ente da cercare. 
Risultato: 
enti: 
per maggiori informazioni consultare il wsdl 
 
Operazione: 
ricercaEnteInt 
Descrizione: 
Ricerca Ente per descrizione, tipo, codice fiscale e indirizzo pec. 
Descrizione e codice fiscale possono contenere la wild card '%'. 
Parametri: 
tipo: 
Tipo dell'ente da ricercare. Può assumere i valori: 
 Null, per cercare qualsiasi tipologia di ente 
 PPAA, per cercare solo le Pubbliche Amministrazioni 
 ENTE, per cercare solo gli enti. 
descrizione: 
Descrizione/denominazione dell'ente. Può contenere la wild card 
'%' 
codiceFiscale:

52 
 
Codice fiscale dell'ente. Può contenere la wild card '%'. 
indirizzoPec: 
Indirizzo Pec dell'ente da cercare. 
 
Risultato: 
enti: 
per maggiori informazioni consultare il wsdl. 
Rispetto al servizio RicercaEnteEx, tra le informazioni restituite 
c’è la tipologia di pubblica amministrazione.  
 
Operazione: 
ricercaEnteComplete 
Descrizione: 
Ricerca Ente per tipo ente, descrizione, codice fiscale, indirizzo 
pec, codice e classe. 
Descrizione e codice fiscale possono contenere la wild card '%'. 
Parametri: 
tipoEnte: 
Tipo dell'ente da ricercare. Può assumere i valori: 
 PPAA, per cercare solo le Pubbliche Amministrazioni 
 ENTE, per cercare solo gli enti. 
idTipologia: 
Identificativo tipologia 
piva: 
Partita iva dell'ente 
descrizione: 
Descrizione/denominazione dell'ente. 
codiceFiscale: 
Codice fiscale dell'ente. 
indirizzoPec: 
Indirizzo Pec dell'ente da cercare. 
codiceEnte: 
Codice dell’ente. 
classe: 
Tipo dell'ente da ricercare. Può assumere i valori: 
 AMM, amministrazione centrale

53 
 
 UOO, unità organizzativa speciale 
 ART, articolazione 
Risultato: 
enti: 
per maggiori informazioni consultare il wsdl. 
 
 
Operazione: 
dettagliEnte 
Descrizione: 
Ricerca Ente per codice 
Parametri: 
codiceEnte: 
codice dell’ente 
codiceFiscale: 
codice fiscale dell’ente 
Risultato: 
enti: 
per maggiori informazioni consultare il wsdl 
 
 
Operazione: 
ricercaReferente 
Descrizione: 
Ricerca i soggetti referenti per un ente. 
 
Parametri: 
codiceEnte: 
Codice dell'ente di cui cercare i referenti, può essere null. 
codiceFiscale: 
Codice dei soggetti da cercare, può essere null. 
pec: 
Indirizzo Pec dei soggetti da cercare, può essere null. 
 
Risultato: 
Referente: 
per maggiori informazioni consultare il wsdl

54 
 
Operazione: 
ricercaEntiReferente 
Descrizione: 
Ricerca degli enti per codice fiscale del referente. 
 
Parametri: 
tipo: 
Tipo dell'ente da ricercare. Può assumere i valori: 
 Null, per cercare qualsiasi tipologia di ente 
 PPAA, per cercare solo le Pubbliche Amministrazioni 
 ENTE, per cercare solo gli enti. 
codiceFiscale: 
Codice dei soggetti da cercare. 
 
Risultato: 
enti: 
per maggiori informazioni consultare il wsdl 
 
 
 
 
Operazione: 
ricercaIndAbilitati 
Descrizione: 
Ricerca degli indirizzi dei referenti abilitati all’invio dell’albo  
 
Parametri: 
pec: 
Indirizzo PEC da ricercare 
codiceEnte: 
codice dell’ente di cui si vuole ricercare i referenti abilitati 
codiceFiscaleFirma: 
il codice fiscale del referente che firma l’invio dell’albo 
 
Risultato: 
indirizzi abilitati: 
la lista degli indirizzi abilitati

55 
 
Per le definizioni tramite WSDL dei web service che espongono i metodi sopra descritti 
si rimanda agli allegati presenti nella directory “WSDL\Altri Servizi\ReGIndE”. 
5.4 Servizio di configurazione notifiche via SMS (servizio 
sospeso) 
Il servizio SMSConfig realizza la registrazione delle configurazioni dell’invio delle 
notifiche via SMS rivolte all’avvocato. Il servizio consiste in un web service per 
l’accesso all’interfaccia che implementa la registrazione delle informazioni inserite 
dall’avvocato attraverso le maschere apposite del Portale dei Servizi Telematici o dei 
Punti di Accesso. 
La fruizione di tale servizio avviene tramite l’esposizione sul Gestore Locale secondo 
le modalità descritte al punto 6.1. 
Il web service di configurazione delle notifiche via sms è descritto nel contesto 
dell’allegato SMSConfig.wsdled è fruibile sia per i registri afferenti il SICID che per 
quelli del SIECIC e SIGP.  
Il namespace da utilizzare è: “http://www.giustizia.it/gl/notifiche/SMSConfig”. 
Di seguito l’interfaccia dei metodi disponibili: 
Operazione: 
setNotificaFascicoli 
Descrizione: 
Il metodo realizza la registrazione della scelta di un avvocato 
identificato con un dato codiceFiscale di ricevere notifiche via 
SMS sull’insieme di fascicoli ed il numero di cellulare passati 
come parametro del metodo. 
Parametri: 
codiceFiscale: 
codice fiscale dell’avvocato;  
fascicoli: 
 insieme dei fascicoli sui quali abilitare la notifica;  
numero: 
numero di cellulare dell’avvocato. 
Risultato: 
Esito positivo dell’invocazione o errore. 
 
Operazione: 
getNotificaFascicoli 
Descrizione: 
Il metodo restituisce per l’avvocato individuato dal codice fiscale 
codiceFiscalel’elenco di fascicoli sui quali è configurata la 
notifica degli eventi tramite SMS. 
Parametri: 
codice Fiscale:

56 
 
codice fiscale dell’avvocato;  
Risultato: 
fascicoli: 
l’elenco di fascicoli sui quali è configurata la notifica degli eventi 
tramite SMS. 
 
Operazione: 
revocaNotificaFascicoli 
Descrizione: 
Il metodo revoca (elimina) l’associazione tra l’avvocato 
identificato dal codiceFiscaleper l’insieme di fascicoli specificato 
come parametro. 
Parametri: 
codiceFiscale: 
 codice fiscale dell’avvocato;  
fascicoli: 
insieme dei fascicoli da eliminare dall’elenco dei fascicoli sui 
quali risulta abilitata la notifica;  
Risultato: 
Esito positivo dell’invocazione o errore. 
 
Operazione: 
setNumero 
Descrizione: 
Il metodo imposta/modifica il numero di cellulare per l’avvocato 
con il codiceFiscale specificato come primo parametro. 
Parametri: 
codiceFiscale: 
codice fiscale dell’avvocato;  
numero: 
numero di cellularedell’avvocato. 
Risultato: 
Esito positivo dell’invocazione o errore. 
 
Operazione: 
getNumero 
Descrizione: 
Il metodo restituisce il numero di cellulare per l’avvocato con il 
codiceFiscale specificato come parametro. 
Parametri: 
codiceFiscale: 
codice fiscale dell’avvocato;

57 
 
Risultato: 
numero: 
 numero di cellulare indicato dall’avvocato per la notifica. 
 
Per la definizione tramite WSDL del web service che espone i metodi sopra descritti si 
rimanda all’allegato presente nella directory “WSDL\Altri Servizi\Notifiche SMS”. 
 
5.5 Invio pagamenti telematici 
I servizi in questione permettono di usufruire delle funzionalità relative al flusso d’invio 
dei Pagamenti Telematici. Per esempio consentono di generare una nuova richiesta di 
pagamento, inoltrare un nuovo carrello di pagamenti e gestire i vari pagamenti. 
 
Il namespace da utilizzare è: http://www.giustizia.it/serviziTelematici/serviziGenerici 
 
Di seguito l’interfaccia dei metodi disponibili. La url esposta ai PDA sarà: 
https://pda.processotelematico.giustizia.it/servizi/ServiziInvioPagamentiTelematici”: 
 
Operazione: 
generaRPT 
Descrizione: 
Genera una richiesta di pagamento telematica in base ai parametri 
specificati. 
Parametri: 
richiestaPagamentoTelematica: 
oggetto composto da tutti i campi necessari alla compilazione di 
una RPT 
Risultato: 
xml della richiesta generata; 
 
Operazione: 
inviaCarrelloRPT 
Descrizione: 
Carica le RPT di un utente indicate nella lista in input, verifica che 
siano correttamente nello stato CARRELLO, verifica che il 
versante sia lo stesso per tutte le RPT e inoltra il carrello al 
NodoPA. 
Parametri: 
codiceFiscale: 
codice fiscale del soggetto; 
crs:

58 
 
lista dei crs; 
areaPubblica: 
booleano che indica se il pagamento è stato effettuato dall’area 
pubblica del SitoWeb PST o se da quella riservata; tale parametro 
è ad uso interno pertanto non dovrà essere valorizzato dai PDA o 
dagli Applicativi. 
Risultato: 
Url del WISP a cui deve essere rediretto l’utente o eccezione in 
caso di errori. 
 
Operazione: 
registraRispostaWisp 
Descrizione: 
Registra l’esito del pagamento per quelle RPT che si riferiscono 
all’idsession ricevuto in input. Si precisa che tale metodo verrà 
invocato dal PST per permettere l’esecuzione corretta del flusso 
di pagamento, ma non dovrà essere invocato né dai PDA né dagli 
applicativi. 
Parametri: 
idsession: 
Id sessione. 
esito: 
esito del pagamento. 
Risultato: 
Esito del pagamento e booleano per identificare se è un pagamento 
di tipologia bollo. 
 
 
Operazione: 
verificaRichiesta 
Descrizione: 
Dà la possibilità all’utente di verificare lo stato di una RPT della 
quale non è ancora pervenuta la Ricevuta di Pagamento. 
Parametri: 
crs: 
codice CRS del pagamento 
Risultato: 
reperisce lo stato di una RPT; 
 
Operazione: 
eliminaRichiesta 
Descrizione: 
Elimina logicamente un pagamento telematico.

59 
 
Parametri: 
crs: 
codice CRS del pagamento 
Risultato: 
elimina il pagamento; 
 
Operazione: 
listaConfNEP 
Descrizione: 
Restituisce la configurazione di pagamento relativa agli Uffici 
NEP. 
Parametri: 
codiceUfficioNEP: 
Codice ufficio NEP 
tipologia: 
Codice tipologia di pagamento 
Risultato: 
restituisce una lista di causalePagamentoNEPConf contenente le 
configurazioni per i pagamenti NEP . 
 
Operazione: 
generaAvviso 
Descrizione: 
Genera un avviso di pagamento base ai parametri specificati. Si 
precisa che tale metodo non dovrà essere invocato dai PDA. 
Parametri: 
RichiestaPagamentoTelematico: 
oggetto composto da tutti i campi necessari alla compilazione di una 
RPT 
Risultato: 
Numero Avviso e PDF dell’AvvisoAnalogico; 
 
Operazione: 
downloadAvviso 
Descrizione: 
Scarica il PDF dell’avviso di pagamento relativo al numero avviso 
specificato. Si precisa che tale metodo non dovrà essere invocato 
dai PDA. 
Parametri: 
numeroAvviso: 
numero avviso di pagamento; 
Risultato: 
PDF dell’avviso analogico se disponibile, NULL altrimenti;

60 
 
 
Per la definizione tramite WSDL del web service che espone  i metodi sopra descritti si 
rimanda all’allegato presente  nella directory “WSDL\Altri Servizi\Pagamenti 
Telematici”. 
5.6 Consultazione pagamenti telematici 
I servizi in questione permettono di usufruire delle funzionalità di consultazione dei 
Pagamenti Telematici. Per esempio consentono di scaricare la richiesta di pagamento, 
di scaricare la ricevuta di pagamento e di reperire l’elenco dei pagamenti. 
 
Il namespace da utilizzare è: http://www.giustizia.it/serviziTelematici/serviziGenerici 
 
Di seguito l’interfaccia dei metodi disponibili. La url esposta ai PDA sarà: 
https://pda.processotelematico.giustizia.it/servizi/ServiziConsultazionePagamentiTele
matici”: 
 
Operazione: 
downloadRichiesta 
Descrizione: 
Scarica la richiesta di pagamento relativa al CRS o numero avviso 
specificato. 
Parametri: 
codiceCRS: 
codice della transazione di pagamento (identificativo pagamento 
o numero avviso);   
Risultato: 
richiesta se disponibile, NULL altrimenti; 
 
Operazione: 
downloadRicevuta 
Descrizione: 
Scarica la ricevuta di pagamento relativa al CRS o numero avviso 
specificato. 
Parametri: 
codiceCRS: 
codice della transazione di pagamento (identificativo pagamento 
o numero avviso);    
originale: 
ricevuta originale 
Risultato: 
ricevuta se disponibile, NULL altrimenti;

61 
 
 
 
Operazione: 
elencoPagamenti 
Descrizione: 
Interroga la base dati per conoscere la lista dei pagamenti 
(compresi gli avvisi di pagamento) che soddisfano i criteri di 
ricerca specificati. 
Parametri: 
codiceCRS: 
codice della transazione di pagamento (identificativo pagamento 
o numero avviso);    
tipologia: 
codice della tipologia di pagamento;  
codiceFiscale: 
codice fiscale del soggetto richiedente;  
codiceDistretto: 
codice del distretto di destinazione; 
causale: 
descrizione della causale di pagamento; 
stato: 
stato del pagamento; Potrà essere valorizzato con: 
 CARRELLO 
 ATTESA, che corrisponde agli stati DB INVIATA, 
OK_CARRELLO, OK_WISP, ERR_WISP, DIFF_WISP, 
KO_PSP, OK_PSP, GENERATA 
 DISPONIBILE 
 USATO 
 RIMBORSATO 
 ERRORE, che corrisponde agli stati DB ERRORE e 
KO_CARRELLO 
 REVOCATO 
dataRichiestaDa: 
limite inferiore per la data di inoltro della richiesta, opzionale; 
dataRichiestaA: 
limite superiore per la data di inoltro della richiesta, opzionale; 
dimensionePagina: 
record per pagina;

62 
 
numeroPagina: 
numero pagina da richiedere 
Risultato: 
pagamenti che soddisfano i criteri di ricerca specificati. 
Oggetto RisultatoRicerca formato da: 
 count: numero di record totali 
 dimensionePagina: numero di record restituiti 
 numeroPagina: numero della pagina restituita 
 vari items di tipo statoRichiestaPagamento contenente tutti 
i dati del pagamento stesso. 
L’oggetto “statoRichiestaPagamento” restituito in output da tale servizio avrà la 
seguente struttura: 
<xs:complexType name="statoRichiestaPagamento"> 
 
<xs:sequence> 
 
 
<xs:element name="causale" type="xs:string"/> 
 
 
<xs:element name="codiceCRS" type="xs:string"/> 
 
 
<xs:element name="codiceDistretto" type="xs:string"/> 
 
 
<xs:element name="dataRicevuta" type="xs:dateTime"/> 
 
 
<xs:element name="dataRichiesta" type="xs:dateTime"/> 
 
 
<xs:element name="denominazionePagatore" type="xs:string"/> 
 
 
<xs:element name="denominazioneVersante" type="xs:string"/> 
 
 
<xs:element name="descrizioneDistretto" type="xs:string"/> 
<xs:element name="descrizioneTipologia" type="xs:string"/> 
 
 
<xs:element name="destinazione" type="xs:string"/> 
 
 
<xs:element name="errore" type="xs:string"/> 
 
 
<xs:element name="id" type="xs:string"/> 
 
 
<xs:element name="importo" type="xs:float"/> 
<xs:element name="numeroAvviso" type="xs: string "/> 
 
 
<xs:element name="pagatore" type="xs:string"/> 
 
 
<xs:element name="ruolo" type="xs:string"/> 
 
 
<xs:element name="stato" type="xs:string"/> 
 
 
<xs:element name="statoNodoPA" type="xs:string"/> 
 
 
<xs:element name="tipologia" type="xs:string"/> 
 
 
<xs:element name="versante" type="xs:string"/> 
 
</xs:sequence> 
</xs:complexType> 
In particolare: 
 causale, testo della causale del pagamento 
 codiceCRS, codice CRS del pagamento

63 
 
 codiceDistretto, codice Distretto 
 dataRicevuta, data in cui è stata pervenuta la ricevuta nel caso sia presente 
 dataRichiesta, data di creazione della richiesta di pagamento 
 denominazionePagatore, nominativo del soggetto pagatore 
 denominazioneVersante, nominativo del soggetto versante 
 descrizioneDistretto, descrizione del Distretto 
 descrizioneTipologia, descrizione tipologia di pagamento contenuta nella 
richiesta 
 destinazione, codice dell’ufficio su cui è stato annullato il pagamento nel caso 
in cui sia stato utilizzato 
 errore, errore restituito dal nodoPA in caso di errori nell’invio del carrello 
 id, identificativo della richiesta di pagamento 
 importo, importo del pagamento 
 numeroAvviso, numero avviso pagamento 
 pagatore, codice fiscale del soggetto pagatore 
 ruolo, numero di ruolo del fascicolo su cui è stato annullato il pagamento nel 
caso in cui sia stato utilizzato 
 stato, stato in cui si trova il pagamento che potrà essere valorizzato con: 
o CARRELLO, indica che la richiesta è nel carrello 
o INVIATA, indica che il pagamento è stato inviato al NodoPA 
o DISPONIBILE, indica che il pagamento è disponibile per 
l’annullamento 
o USATO, indica che il pagamento è stato utilizzato 
o OK_CARRELLO, indica che l’invio del carrello è avvenuto 
correttamente 
o KO_CARRELLO, indica che si sono presentati errori nell’invio del 
carrello 
o OK_WISP, indica che i passaggi all’interno del WISP si sono conclusi 
correttamente 
o ERR_WISP, indica che i passaggi all’interno del WISP si sono conclusi 
con errori 
o DIFF_WISP, indica che il WISP ha restituito lo stato DIFFERITO 
o RIMBORSATO, indica che il pagamento è stato rimborsato 
o ERRORE, indiche che il pagamento è in ERRORE 
o REVOCATO, indica che il pagamento è stato revocato a causa di un 
annullo tecnico 
o OK_PSP, indica che i passaggi di attivazione ed invioRPT dell’avviso 
si sono conclusi correttamente 
o KO_PSP, indica che i passaggi di attivazione ed invioRPT dell’avviso 
si sono conclusi con errori 
o GENERATA, indica che è stato generato l’avviso di pagamento ma non 
è ancora stato attivato 
 statoNodoPA, stato popolato dalla funzionalità verificaRichiesta 
 tipologia, codice tipologia di pagamento contenuta nella richiesta 
 versante, codice fiscale del soggetto versante

64 
 
 
Operazione: 
elencoPagamentiRevocati (SERVIZIO NON DISPONIBILE) 
Descrizione: 
Interroga la base dati per reperire la lista dei pagamenti oggetto di 
revoca che soddisfano i criteri di ricerca specificati. 
Parametri: 
dataRicevutaRevocataDa: 
limite inferiore per la data della ricevuta revocata; 
dataRicevutaRevocataA: 
limite superiore per la data della ricevuta revocata;  
dimensionePagina: 
record per pagina; 
numeroPagina: 
numero pagina da richiedere 
Risultato: 
Pagamenti revocati che soddisfano i criteri di ricerca specificati. 
Oggetto RisultatoRicerca formato da: 
 count: numero di record totali 
 dimensionePagina: numero di record restituiti 
 numeroPagina: numero della pagina restituita 
 vari items di tipo revocaPagamento contenente tutti i dati 
della revoca del pagamento stesso. 
L’oggetto “revocaPagamento” restituito in output da tale servizio avrà la seguente 
struttura: 
<xs:complexType name=" revocaPagamento "> 
 
<xs:sequence> 
 
 
<xs:element name="codiceCRS" type="xs:string"/> 
 
 
<xs:element name="dataRevoca" type="xs:dateTime"/> 
 
 
<xs:element name="importoRevocato" type="xs:float"/> 
 
</xs:sequence> 
</xs:complexType> 
 
In particolare: 
 codiceCRS, conterrà il codice CRS del pagamento 
 dataRevoca, conterrà la data della revoca (dataOraMessaggioRevoca) 
 importoRevocato, conterrà il valore dell’importo revocato

65 
 
Per la definizione tramite WSDL del web service che espone i metodi sopra descritti si 
rimanda all’allegato presente nella directory “WSDL\Altri Servizi\Pagamenti 
Telematici”. 
 
5.7 Scambio messaggi tra ausiliari e giudice delegato 
I servizi di scambio messaggi tra ausiliari e giudice delegato consentono di consultare 
i messaggi inviati agli ausiliari dal giudice e di replicare ai messaggi stessi. 
La fruizione di tali servizi avviene tramite l’esposizione di un web-service 
nell’infrastruttura SOAP implementata dal Gestore Locale. 
All’interno dell’header HTTP della request deve essere indicato il codice fiscale del 
soggetto che ha invocato la richiesta (proprietà X-WASP-User). 
I messaggi SOAP rivolti ai servizi di scambio messaggi tra ausiliari e giudice delegato 
presentano un SOAP header con la seguente forma: 
<soapenv:Header><ws:InvocationDomain name="JPW" role="CTU" 
group="XXXXXXXX" 
soapenv:mustUnderstand="1" 
soapenv:actor="http://schemas.xmlsoap.org/soap/actor/next
" xmlns:ws="http://www.netserv.it/anag/security"/> 
dove: 
o role: deve essere valorizzato con “CTU”,”CUS”,”DEL” o “CUR” 
o name: deve essere valorizzato con “JPW” 
o group: contiene il codice dell’Ufficio Giudiziario. 
 
Il web service permette di consultare i messaggi del giudice e di rispondere ai messaggi 
del 
giudice, 
per 
questo 
web 
service 
il 
namespace 
da 
utilizzare 
è 
“http://www.giustizia.it/serviziInteropAusiliari/MessaggiGiudice”. 
Di seguito l’interfaccia dei metodi disponibili.  
Operazione: 
leggiMessaggi (attuale leggiMsgCur) 
Descrizione: 
Consultazione dei messaggi 
Parametri: 
idFasc: 
eventuale riferimento al fascicolo per la ricerca 
from: 
data di inizio ricerca 
to: 
data di fine ricerca 
soloNuovi:

66 
 
booleano che, se valorizzato a true, permette di ricercare solo i 
messaggi non letti (un messaggio si considera letto se è stato 
invocato il metodo “dettaglioMessaggio” almeno una volta) 
orderBy: 
oggetto che permette l’ordinamento dei risultati restituiti 
Risultato: 
l’elenco dei messaggi che soddisfano la ricerca. Per ogni 
messaggio saranno restituiti i dati relativi al messaggio come data 
del messaggio, oggetto, mittente, destinatario, fascicolo e 
identificativi degli eventuali allegati. 
 
Operazione: 
leggiThreadMessaggi 
Descrizione: 
Consultazione dei messaggi che compongono il thread del 
messaggio in input. 
Parametri: 
idFasc: 
riferimento al fascicolo che contiene il messaggio 
idMsg: 
identificativo del messaggio del quale si vuole visualizzare il 
thread 
Risultato: 
l’elenco dei messaggi “figli” del messaggio in input. Per ogni 
messaggio saranno restituiti i dati relativi al messaggio come data 
del messaggio, oggetto, mittente, destinatario, fascicolo e 
identificativi degli eventuali allegati. 
 
 
Operazione: 
dettaglioMessaggio 
Descrizione: 
Dettaglio di un messaggio. 
Parametri: 
idFasc: 
riferimento al fascicolo che contiene il messaggio 
idMsg: 
identificativo del messaggio del quale si vuole visualizzare il 
dettaglio del messaggio.

67 
 
Risultato: 
I dettagli del messaggio, ovvero data del messaggio, oggetto, 
mittente, destinatario, fascicolo e identificativi degli eventuali 
allegati. 
Segna il messaggio come letto. 
 
Operazione: 
scriviMessaggio 
Descrizione: 
Scrive un nuovo messaggio al giudice del fascicolo 
Parametri: 
idFasc: 
identificativo del fascicolo per il quale si sta inviando il messaggio 
idMsg: 
identificativo del messaggio al quale si sta rispondendo. In caso 
di valore “null”, trattasi di nuovo messaggio. 
oggetto: 
oggetto del messaggio 
testo: 
testo del messaggio 
allegati: 
elenco di eventuali documenti allegati al messaggio 
Risultato: 
identificativo del messaggio. 
 
 
 
Operazione: 
downloadDocumento 
Descrizione: 
Scarica uno specifico documento 
Parametri: 
idFasc: 
identificativo del fascicolo per il quale si sta scaricando il 
documento 
idDocumento: 
identificativo del documento da scaricare

68 
 
Risultato: 
il contenuto del documento il quale viene trasmesso in allegato 
alla risposta. 
 
Per la definizione tramite WSDL del web service che espone i metodi sopra descritti si 
rimanda al file jpw-messaggistica-ausiliari.wsdl presente nella directory “WSDL\Altri 
Servizi\MessaggisticaAusiliari”. 
 
5.8 Download messaggi di notifica e comunicazione 
I servizi di download messaggi di notifica e comunicazione permettono il download dei 
suddetti messaggi tramite Web Service e non da accesso diretto attraverso il link, 
inviato al destinatario nel messaggio di avviso di download. 
La fruizione di tali servizi avviene attraverso il proxy PDA e permette l'accesso al 
messaggio 
attraverso 
la 
specifica 
dei 
parametri 
trasmessi 
nell'allegato 
datiDownload.xml inviato contestualmente all'avviso di download. 
Il servizio deve essere utilizzato per delegare al sistema del PDA l'accesso al messaggio 
che altrimenti deve essere effettuato dal destinatario previa autenticazione presso il 
proxy delle Software House. 
L'interfaccia espone i metodi descritti nella tabella seguente: 
 
 
Operazione: 
download 
Descrizione: 
Scarica il messaggio specificato attraverso. 
Parametri: 
site: 
identificativo del sito (GLPEC) che ha in carico il messaggio. 
Si 
tratta 
del 
valore 
dell'elemento 
<sito> 
del 
xml 
datiDownload.xml trasmesso con l'avviso di download 
 
contentId: 
identificativo del messaggio. 
Si tratta del valore dell'elemento <id> del xml di cui al parametro 
precedente. 
 
user: 
Codice fiscale del destinatario del messaggio.

69 
 
Si tratta del valore dell'attributo destinatario dell'elemento 
<datiDownload> del xml trasmesso con l'avviso di download. 
Risultato: 
Struttura dati con i dettagli del messaggio richiesto: 
name: 
Oggetto della comunicazione 
 
availableDate: 
Data di disponibilità del messaggio. 
 
content: 
Contenuto del messaggio. 
Viene trasmesso in allegato alla risposta. 
 
Per la definizione tramite WSDL del web service che espone i metodi sopra descritti si 
rimanda al file download-notifiche.wsdl presente nella directory “WSDL\Altri 
Servizi\Download Notifiche”. 
 
5.9 Servizi Deprecati 
In questo paragrafo sono elencati i servizi web da considerare deprecati. 
I namespaces in questione sono: 
 urn:CONS-SICC-BE-DISTR 
 urn:CONS-SIL-BE-DISTR 
 http://elsagdatamat.com/bea/pct/siecic/ws/consultazioni 
 urn:BEAConsultazioni-distr 
 urn:BEAProvvedimentiPubblicati-distr 
 urn:RichiestaCopie-consultazioni-distr 
 urn:CONS-ABI-BE 
 
Per completezza si allegano al presente documento i wsdl dei web servicesdeprecati. Si 
veda a tal proposito il contenuto della directory “WSDL\Altri Servizi\Deprecati”. 
 
5.9.1 
Servizi Deprecati – Ricerca soggetti sul ReGIndE 
I servizi seguenti di accesso al Reginde, che consentono di effettuare ricerche di soggetti 
censiti nel ReGIndE, sono deprecati e non saranno più disponibili a partire dal 
01/07/2014.

70 
 
Sono deprecati i metodi del web service di accesso al ReGIndEdescritto nel contesto 
dell’allegato ServiziInterrogazioneSoggetto.wsdl che si trova precisamente in 
“WSDL\Altri Servizi\Deprecati”. Per questo web service il namespaceutilizzatoè 
“http://www.giustizia.it/serviziTelematici/reginde/interrogazioni”. 
Di seguito l’interfaccia dei metodi disponibili.  
Operazione: 
dettagliSoggettoPerCodice 
Descrizione: 
Ricerca i dettagli di un soggetto per codice fiscale 
Parametri: 
codice fiscale esatto del soggetto 
Risultato: 
soggetto: 
per maggiori informazioni consultare il wsdl 
 
Operazione: 
dettagliSoggettoPerCodiceLazy 
Descrizione: 
Ricerca i dettagli di un soggetto per parte del codice fiscale 
Parametri: 
parte del codice fiscale del soggetto 
Risultato: 
lista di soggetti: 
per maggiori informazioni consultare il wsdl 
 
Operazione: 
dettagliSoggettoPerIndirizzo 
Descrizione: 
Ricerca i dettagli di un soggetto per indirizzo 
Parametri: 
indirizzo 
Risultato: 
lista di soggetti: 
per maggiori informazioni consultare il wsdl 
 
Operazione: 
elencoPaginatoSoggetti 
Descrizione: 
Restituisce un elenco paginato di soggetti 
Parametri: 
da: 
indice inizio ricerca 
count:

71 
 
numero di soggetti da ricercare 
Risultato: 
lista di soggetti: 
per maggiori informazioni consultare il wsdl 
 
Operazione: 
isMembroDi 
Descrizione: 
Verifica che il soggetto appartenga all’Ente 
Parametri: 
codiceFiscale: 
codice fiscale del soggetto 
codiceEnte: 
codice dell’Ente 
Risultato: 
lista ruoli del soggetto censito 
 
Operazione: 
ricercaSoggetto 
Descrizione: 
Ricerca lista soggetti per cognome o ente 
Parametri: 
cognome: 
cognome e nome del soggetto seguito dal carattere * 
codiceEnte: 
codice dell’Ente 
Risultato: 
lista di soggetti: 
per maggiori informazioni consultare il wsdl 
5.10 Servizio di generazione codice identificativo univoco per 
il creditore estero 
Il servizio descritto in questo paragrafo consente al curatore di generare un codice con 
cui identificare il creditore/ente creditore estero in modo univoco per singolo 
procedimento in caso quest’ultimo non fosse già in possesso di un codice fiscale 
italiano. 
Il codice così generato sarà anche utilizzato sia dal curatore per l’invio telematico dei 
dati delle domande di ammissione al passivo o di rivendica, sia dal creditore/ente 
creditore per consultare i propri procedimenti sul Portale delle Procedure Concorsuali 
(PPC)

72 
 
La fruizione di tali servizi avviene tramite l’esposizione di un web-service 
nell’infrastruttura SOAP implementata dai servizi backend del PST e sarà esposto sia 
ai PDA che alle software house. 
Il web service permette la generazione del codice identificativo, controllando anche i 
casi di duplicazione di soggetti, e per questo web service il namespace da utilizzare è 
http://www.giustizia.it/serviziTelematici/serviziCuratore.  
L’url esposta ai PDA sarà: 
https://pda.processotelematico.giustizia.it/servizi/ServiziCuratore 
Mentre quella esposta al proxy EXT sarà: 
https://ext.processotelematico.giustizia.it/servizi/ServiziCuratore 
 
 
Di seguito l’interfaccia dei metodi disponibili: 
 
 
 
Operazione: 
generaCodice 
Descrizione: 
genera il codice univoco per il creditore estero 
Parametri: 
DatiCreditore 
Dati anagrafici del creditore/ente estero e la procedura di 
riferimento così come richiesti nel wsdl. 
forzaGenerazione 
un booleano che di default dovrà essere impostato a “false” e potrà 
essere impostato a “true” in caso si voglia generare un nuovo 
codice identificativo di un soggetto già esistente e munito di 
codice.  
Risultato: 
codice identificativo del soggetto 
per maggiori informazioni consultare il wsdl 
 
Per la definizione tramite WSDL del web service che espone i metodi sopra descritti si 
rimanda al file ServiziCuratore.wsdl presente nella directory “WSDL\Altri 
Servizi\GenerazioneCodiceCreditoreEstero”.

73 
 
6 Accesso ai servizi di consultazione tramite 
proxy 
L’accesso ai web service descritti ai capitoli precedenti è consentito solamente 
attraverso i proxy di cui ai paragrafi seguenti; ogni tipologia di proxyverrà esposta 
tramite VirtualHost, sul quale verranno mappati tutti i diversi Gestori Locali e i servizi 
come contesti.  
6.1 Proxy per i Punti di Accesso 
Nel caso specifico del proxyper i PdA la url esposta sarà 
https://pda.processotelematico.giustizia.it/<GL>/<Registro>/backend/rpcrouter 
dove: 
 https://pda.processotelematico.giustizia.it è denominato targetHost 
 <GL>/<Registro>/backend/rpcrouter è denominato targetPath e si compone 
di:  
o <GL> = contesto specifico del singolo Gestore Locale (ad esempio  
GLMI per Milano, GLCC per la Corte di Cassazione) 
o <Registro> = registro di consultazione (es. SICID, SIECIC o SIGP 
oppure ancora Cassazione per la Corte di Cassazione)  
o backend/rpcrouter come parte fissa 
Di seguito un esempio per la consultazione del SICID nel contesto del distretto di 
Milano: 
https://pda.processotelematico.giustizia.it/GLMI/sicid/backend/rpcrouter 
Un ulteriore esempio relativo alla Corte di Cassazione 
https://pda.processotelematico.giustizia.it/GLCC/Cassazione/backend/rpcrouter 
 
Il protocollo https è inteso in mutua autenticazione e quindi il chiamante deve 
presentare il proprio certificato attraverso il quale il proxy verificherà che si tratti di un 
PdA censito. 
Si sottolinea che i frontend dei sistemi JPW-SICID, JPW-SIECIC e JPW-SIGP non 
saranno compatibili con tale configurazione. 
6.2 Proxy per le software house 
Nel caso specifico del proxy per le software house la url esposta sarà: 
https://ext.processotelematico.giustizia.it/pda/pycons/<GL>/<CodiceRegistro> 
dove: 
 https://ext.processotelematico.giustizia.it/pda/pycons è denominato targetHost 
 <GL>/<CodiceRegistro> è denominato targetPath e si compone di:  
o <GL> = contesto specifico del singolo Gestore Locale (es. GLMI per 
Milano)

74 
 
o <CodiceRegistro> = codice del registro di consultazione (es. 
JPW_SICID per il SICID, JPW_SIECIC per il SIECIC, JPW_SIGP per 
il SIGP e JPW_CASS per la Corte di Cassazione)  
Di seguito un esempio per la consultazione del SICID nel contesto del distretto di 
Milano: 
https://ext.processotelematico.giustizia.it/pda/pycons/GLMI/JPW_SICID 
Un ulteriore esempio relativo alla Corte di Cassazione: 
https://ext.processotelematico.giustizia.it/pda/pycons/GLCC/JPW_CASS 
Il protocollo https è inteso in mutua autenticazione e quindi il chiamante deve 
presentare il certificato di un utente censito sul ReGIndE. Il certificato deve essere 
rilasciato da una CA accreditata da DigitPA. 
6.3 Proxy per le Parti in Causa (servizio ancora non 
rilasciato) 
Nel caso specifico del proxy per le parti la url esposta sarà: 
https://pub.processotelematico.giustizia.it/<GL>/<Registro>/backend/rpcrouter 
dove:  
 https://pub.processotelematico.giustizia.it è denominato targetHost 
 <GL>/<Registro>/backend/rpcrouter è denominato targetPath e si compone 
di:  
o <GL> = contesto specifico del singolo Gestore Locale (es. GLMI per 
Milano) 
o <Registro> = registro di consultazione (es. SICID, SIECIC o SIGP) 
o backend/rpcrouter come parte fissa 
Di seguito gli esempi per la consultazione del SICID nel contesto del distretto di Milano 
e la Corte di Cassazione: 
https://pub.processotelematico.giustizia.it/GLMI/SICID/backend/rpcrouter 
https://pub.processotelematico.giustizia.it/GLCC/Cassazione/backend/rpcrouter 
 
Il protocollo https è inteso in mutua autenticazione e quindi il chiamante deve 
presentare il certificato di un utente autorizzato da DGSIA all’accesso al proxy. Il 
certificato deve essere rilasciato da una CA accreditata da DigitPA. 
Si sottolinea che sarà possibile accedere a tale proxy previa registrazione dei dati della 
parte da eseguirsi a carico della DGSIA attraverso il Cruscotto per gli Amministratori. 
6.4 Indirizzi per l’invocazione dei web service 
Nella tabella seguente sono riportate le mappature tra i web service definiti attraverso i 
WSDL allegati [A1] e i Proxy attraverso i quali tali web service sono invocabili al fine 
di permettere la corretta implementazione dell’attributo location dell’elemento 
soap:addressdeiwsdlstessi.

75 
 
Sono infatti elencati nella tabella i wsdl che riportano al loro interno il seguente 
elemento xml: 
<soap:address location="https://targetHost/targetPath"/> 
Dove targetHost e targetPath devono essere istanziati con i valori indicati ai paragrafi 
precedenti a seconda che si tratti di Proxy per i Punti di Accesso (nella tabella Proxy 
PdA), Proxy per le software house (nella tabella Proxy SH) o Proxy per le parti in causa 
(nella tabella Proxy PC). 
 
Tipo Interrogazione 
WSDL 
Invocabile 
da 
ArchivioGiurispruden
ziale SICID-SIECIC 
BEAConsultazioni-giur.wsdl 
Proxy PdA 
Proxy SH 
ArchivioGiurispruden
ziale SICID-SIECIC 
BEADownloadProvvedimenti.wsdl 
Proxy PdA 
Proxy SH 
ArchivioGiurispruden
ziale Cassazione 
consultazione-sentenze.wsdl 
Proxy PdA 
Proxy SH 
FascicoloInformatico 
SICID 
BEAFascicoloInformatico-
distr.wsdl 
Proxy PdA 
Proxy SH 
Proxy PC 
FascicoloInformatico 
SIECIC 
bea-fascicolo-siecic.wsdl 
Proxy PdA 
Proxy SH 
Proxy PC 
FascicoloInformatico 
SIGP 
sigp-consultazioneDocumenti.wsdl 
Proxy PdA 
Proxy SH 
Proxy PC 
FascicoloInformatico
Cassazione 
registro-ricevute-pec.wsdl 
Proxy PdA 
Proxy SH 
Invio 
Pagamenti 
Telematici 
ServiziInvioPagamentiTelematici.w
sdl 
Proxy PdA

76 
 
Consultazione 
Pagamenti Telematici 
ServiziConsultazionePagamentiTele
matici.wsdl 
Proxy PdA 
Notifiche via SMS 
SMSConfig.wsdl 
Proxy PdA 
Proxy SH 
Consultazione 
Registri SICID 
qbuilder-cons-sivg-be-distr.wsdl 
Proxy PdA 
Proxy SH 
Proxy PC 
qbuilder-cons-sicc-be-distr.wsdl 
Proxy PdA 
Proxy SH 
Proxy PC 
qbuilder-cons-sil-be-distr.wsdl 
Proxy PdA 
Proxy SH 
Proxy PC 
Consultazione 
Registri SIECIC 
cons-siecic-be.wsdl 
Proxy PdA 
Proxy SH 
Proxy PC 
Consultazione 
Registri 
civile 
e 
penale Cassazione 
qbuilder-cons-civile.wsdl 
Proxy PdA 
Proxy SH 
Proxy PC 
qbuilder-cons-penale.wsdl 
Proxy PdA 
Proxy SH 
Proxy PC 
Consultazione civile e 
penale 
Cassazione 
anonimizzati 
qbuilder-cons-anonima-civile.wsdl 
Proxy PdA 
Proxy SH 
Proxy PC 
qbuilder-cons-anonima-penale.wsdl 
Proxy PdA 
Proxy SH 
Proxy PC 
qbuilder-cons-anonima-sivg-
be.wsdl 
Proxy PdA

77 
 
Consultazione 
Registri 
SICID 
anonimizzati 
Proxy SH 
Proxy PC 
qbuilder-cons-anonima-sicc-be.wsdl Proxy PdA 
Proxy SH 
Proxy PC 
qbuilder-cons-anonima-sil-be.wsdl 
Proxy PdA 
Proxy SH 
Proxy PC 
Consultazione 
Registri 
SIECIC 
anonimizzati 
cons-anonima-siecic-be.wsdl 
Proxy PdA 
Proxy SH 
Proxy PC 
Consultazione 
Registri SIGP 
cons-sigp-be.wsdl 
Proxy PdA 
Proxy SH 
Proxy PC 
Richieste 
Copie 
SICID e SIECIC 
qbuilder-richiestacopie-distr.wsdl 
Proxy PdA 
Proxy SH 
richiesta-copie.wsdl 
Proxy PdA 
Proxy SH 
ServiziReGIndE 
ServiziInterrogazioneEnte.wsdl 
ServiziInterrogazioneSoggetto.wsdl 
 
Proxy PdA 
Proxy SH 
AltriServizi 
SMSConfig.wsdl 
ServiziInvioPagamentiTelematici.w
sdl 
ServiziConsultazionePagamentiTele
matici.wsdl 
Proxy PdA 
CatalogoServiziBeanService.wsdl 
jpw-messaggistica-curatore.wsdl 
Proxy PdA 
Proxy SH 
ServiziCuratore.wsdl 
Proxy PdA 
Proxy SH

78