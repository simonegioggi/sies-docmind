---
uniqueName: siut-sies-sc-1-0-20230609-schedaintervento202333ps
displayName: "SIUT SIES SC 1 0 20230609 Scheda Intervento 2023 33 PST PagoPA Step 1"
category: "GENERAL"
tags: []
---

# SIUT-SIES-SC-1.0-20230609-Scheda_Intervento_2023_33_PST_PagoPA_Step-1

> **File originale:** `MEV/SCHEDA_033/SIUT-SIES-SC-1.0-20230609-Scheda_Intervento_2023_33_PST_PagoPA_Step-1.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Umberto Mignogna | Analista Funzionale Senior |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 05/05/2023 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 05/05/2023 | Prima Emissione |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Aurora Garofalo | Amministrazione |  | Responsabile Unico Procedimento |
| Oris Orlando | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Francesco Rosati | RTI |  | Responsabile Manutenzione Correttiva e Referente Qualità e Sicurezza |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario e Referente Tecnico |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Referente PMO e Qualità |
| Alessandro Falleni | RTI |  | Referente Sicurezza |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |


Indice dei contenuti
1	Introduzione	5
1.1	Scopo del documento	5
1.2	Riferimenti	5
1.3	Glossario	5
1.3.1	Acronimi e abbreviazioni	5
2	Interventi su SIEP	7
2.1	Completamento dei Template dell’ordine di Ingiunzione	7
2.2	Dettaglio Procedimento SIEP	7
2.3	Gestione ordine di Ingiunzione	9
2.3.1	Notifiche	10
2.3.2	Rinnovo Ricerche per Omesse Notifiche	11
2.3.3	Richiesta Informazioni Comma 5	13
2.3.4	Rinnovazione Notifica successiva alla Richiesta Informazioni	14
2.3.5	Solleciti	15
2.3.6	Verbale Vane Ricerche	15
2.4	Nota trasmissione  Bollettini rate successive alla prima	15
2.4.1	Ordine Ingiunzione Pagamento	16
2.4.2	Nota trasmissione bollettini rate successive alla prima	17
2.5	Gestione Bollettini pagoPA	18
2.5.1	Richiesta Bollettini	19
2.5.2	Modifica Gestione Bollettini Pagamento e relativa storicizzazione	24
2.6	Verifica Stato Bollettini	29
2.7	Scadenzari	29
2.7.1	Scadenzario Stato Pagamenti	29
2.7.2	Ricerca procedimenti per Stato Pagamenti	31
2.8	Gestione Pene Sostitutive Brevi	33
2.8.1	Semilibertà/Detenzione Domiciliare Sostitutive	33
2.9	Batch di verifica stato del Pagamento	37
2.10	Interventi sottosistema SIGE	37
2.10.1	Aggiornamento template Fissazione Udienza	37
2.10.2	Integrazione Tabelle Oggetti	38
2.11	Gestione errori con pagoPA	38
2.11.1	Cruscotto per funzionalità Batch	39
2.11.2	Cruscotto per funzionalità web	41
2.12	Test di Sistema	43

Introduzione
Scopo del documento
Considerando i numerosi interventi previsti nella Scheda Intervento 2023_33 per l’adeguamento del sistema SIES in merito al pagamento delle pene pecuniarie in base alle modifiche introdotte dalla riforma Cartabia e al completamento dell’interfacciamento del PagoPA/PST, si è deciso con il GdL SIEP di suddividere gli interventi in più STEP, in base alla priorità degli stessi per rendere gli uffici più operativi.
In questo documento sono descritti gli interventi facenti parte dello STEP-1 della Scheda.
Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF 1 | m_dg.DOG07AR.14_02_2023.0000226.U_Richiesta_scheda_2023-13_APP-SIES_PAGOPA_v_1.0_signed | Richiesta Scheda |
| RIF 2 | Invio_atti_cognizione_scheda_2023-13_PAGOPA_v_1.0_signedPagoPA_2023-13__cognizione | Atti Cognizione |
| RIF 3 | Documentazione_servizi_web_v1.53 | Servizi esposti dal PST |
| RIF 4 | APPLICATIVI - Flussi pagamento telematico tramite PST vers. 3.1 | Servizi esposti dal PST |

Glossario
Acronimi e abbreviazioni
| Sigla | Descrizione |
| --- | --- |
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
| ICT | Information & Communication Technology |
| ISO | International Organization for Standardization |
| ISP | Information Security Policy |
| IT | Information Technology |
| MAC | MAnutenzione Correttiva |
| MEV | Manutenzione EVolutiva |
| PA | Pubblica Amministrazione |
| PdQ | Piano della Qualità |
| PdS | Piano della Sicurezza |
| PEC | Posta Elettronica Certificata |
| PMO | Program Management Office |
| POO | Program Operating Office |
| RTI | Raggruppamento Temporaneo di Impresa |
| RTO | Recovery Time Objective |
| RUF | Responsabile Unico Fornitore |
| RUP | Responsabile Unico Progetto |
| SAL | Stato Avanzamento Lavori |
| SGQ | Sistema di Gestione per la Qualità di Engineering Ingegneria Informatica S.p.A. |
| SGSI | Sistema di Gestione della Sicurezza Informatica |
| SIU | Sistema Informativo Unitario |
| SLA | Service Level Agreement |
| SM | Security Manager |
| SQL | Structured Query Language |
| SW | SoftWare |
| UTA | Utente Generico Amministrazione |
| VPN | Virtual Private Network |

Interventi su SIEP
Su tutte le form Dettaglio, relative alle funzioni descritte di seguito, l’Amministrazione ha richiesto che sia sempre presente il tasto Torna Indietro , selezionandolo il sistema dovrà riposizionarsi sulla voce di menu Gestione Riscossione Pene Pecuniarie.
Completamento dei Template dell’ordine di Ingiunzione
Vanno integrati gli attuali template prodotti nella parte dispositiva con la disposizione del giudice  sulla tipologia di pagamento, unica soluzione o rateizzata.
Sono stati presentati 2 template (01_pagamento unica soluzione condannato detenuto.rtf, 01_pagamento unica soluzione condannato libero.rtf) per pagamento unica soluzione e 2 per pagamento rateizzato (02_pagamento rateale condannato libero.rtf, 02_pagamento rateale detenuto.rtf) da generare in base alla posizione giuridica libero o detenuto del condannato.
Non essendo possibile intervenire, nell’ambito di questo Step, nell’attuale gestione della posizione giuridica, si procederà all’aggancio dei template in base all’aggregazione, effettuata dal GdL dell’Amministrazione, delle attuali 84 posizioni presenti nella base dati su 3 tipologie: Libero, Misura_Alternativa e Detenuto, valorizzando per ciascun record della CG_REF_CODES (RV_DOMAIN=’POSIZIONE_GIURIDICA’) la colonna RV_ALT5_VALUE, rispettivamente  con i codici L, EA e EI.

Ai fini dell’aggancio del template il condannato sarà considerato Detenuto se RV_ALT5_VALUE=’EI’, negli altri due casi sarà considerato Libero.
Dettaglio Procedimento SIEP
Per facilitare la consultazione dei dati relativi alle modalità di pagamento delle pene pecuniarie e delle persone Civilmente Obbligati al pagamento, nonché lo Stato dei Pagamenti, nella form di Dettaglio del procedimento SIEP saranno apportate le seguenti implementazioni:
La descrizione della Pena Sostitutiva, in caso di Pena Pecuniaria Sostitutiva, sarà cliccabile, permettendo di accedere alla maschera di Dettaglio delle Modalità di pagamento delle pene pecuniarie;
Dopo la riga con i dati del Difensore, sarà inserito il link  , che saranno visualizzati solo in presenza di questi dati sul procedimento;
Prima della sezione Ultimi Eventi sarà inserito il link , che permetterà di accedere alla visualizzazione di tutti i bollettini, relativi all’ultimo ordine di Ingiunzione al pagamento, con il relativo stato di pagamento.


Selezionandoli il sistema visualizzerà le funzioni





Gestione ordine di Ingiunzione
Realizzazione delle funzioni presenti nel menu Gestione Ordine Ingiunzione

Escludendo la funzione Notifiche già realizzata, che andrà comunque rivista, bisognerà realizzare le altre quattro voci presente nel seguente menu

per tutte le voci, a differenza di come avviene adesso per la voce Notifiche, per la quale il sistema si posiziona sull’ultimo ordine di ingiunzione emesso sul procedimento, considerando, che alla luce di quanto riportato nella Richiesta della Scheda- 33, sullo stesso procedimento potranno essere emessi più ordini di ingiunzione, il sistema prima di presentare la form della funzione selezionata, presenterà prima l’elenco degli Ordini di Ingiunzione  e degli Avvisi emessi e validati.

da cui l’utente selezionerà quello di interesse.
N.B. Alle funzionalità presenti in questo menu sono collegati diversi template (più di una decina), che bisognerebbe modificare per adattarli all’OE di Ingiunzione. Bisognerà valutare se servono tutti o accorparli in numero più esiguo.
Notifiche
La funzione, già realizzata nell’ambito della Scheda 2023-13, sarà modificata per gestire anche l’Avviso pagamento per rate successive alla prima e per il calcolo delle date scadenza.
Per quanto riguarda il calcolo date scadenze, al momento dell’annotazione della data di avvenuta notifica al condannato, il sistema dovrà procedere al calcolo della data scadenza per il pagamento del primo bollettino e dei restanti bollettini, in caso di rateizzazione , secondo i seguenti principi:
In caso di rata unica  la data di scadenza = data avvenuta notifica + 90 gg. In questo caso sarà calcolata anche la data scadenza per la richiesta di rateizzazione = data avvenuta notifica + 20 gg;
In caso di pagamento rateale la data scadenza prima rata = data avvenuta notifica + 30 gg, le date scadenza delle rate successive dovranno essere impostate sull’ultimo giorno dei mesi successivi alla data di scadenza prima rata (es. Rate da pagare 5, data notifica = 10-05-2023=> data scadenza prima rata 09-06-2023, date scadenze successive 31-07-2023, 31-08-2023, 30-09-2023, 31-10-2023, 30-11-2023).
Contestualmente al calcolo delle scadenze, il sistema inserirà il procedimento nello scadenzario.
In caso di annotazione delle Notifiche per l’Avviso pagamento, il sistema si limiterà ad annotare le date di avvenuta notifica, ma non effettuerà alcun calcolo e non gestirà alcuno scadenzario.
Sulla form di Dettaglio delle Notifiche sarà inserito il link , per permettere di verificare le date di scadenza sui bollettini ed eventualmente procedere alla richiesta di generazione degli stessi, nel caso di generazione in due momenti separati.

Rinnovo Ricerche per Omesse Notifiche
La funzione ricalcherà quella attualmente disponibile  per l’ordine di esecuzione con decreto sospensione. Bisognerà verificare che l’attuale comportamento, descritto di seguito, sia valido anche per l’ordine di Ingiunzione al pagamento.
La funzione presuppone che sia stato già inserito un verbale vane ricerche, nel caso che non sia già presente invia il seguente messaggio

Che consente di passare alla funzione di inserimento di Verbale Vane Ricerche, che al momento non riconosce l’Ordine di Ingiunzione come provvedimento per cui possa essere emesso tale verbale.


Il sistema consente di inserire anche in assenza di un verbale di vane ricerche, la form presenta vari radio button che trasformano la stessa in base alla valorizzazione degli stessi

Oppure

oppure
Su questa form sarà inserita l’annotazione dell’esito della notifica (positivo o negativo) da parte degli Ufficiali Giudiziari

oppure

a seguito della conferma il sistema inserisce un nuovo record nella tabella RINNOVO, collegato al Verbale e alla Notifica, aggiorna lo stato del procedimento e visualizza la funzione di Dettaglio

da cui sarà possibile produrre la stampa della comunicazione da inviare all’autorità destinataria (template SIEP_GDS_OE_RINN_RIC, SIEP_GDS_OE_RINN_RIC ed altri). I Template andranno rivisti per renderli utilizzabili anche per l’OE Ingiunzione al pagamento ed eventualmente accorpati.
Richiesta Informazioni Comma 5
La funzione ricalcherà quella attualmente disponibile  per l’ordine di esecuzione con decreto sospensione. Bisognerà verificare che l’attuale comportamento, descritto di seguito, sia valido anche per l’ordine di Ingiunzione al pagamento.
La form presenta due radio button che trasformano la stessa in base alla valorizzazione degli stessi

Oppure

a seguito della conferma il sistema inserisce un nuovo record nella tabella RINNOVO, collegato alla Notifica, aggiorna lo stato del procedimento e visualizza la funzione di Dettaglio, da cui è possibile produrre la stampa della comunicazione da inviare all’autorità destinataria.
Anche questa funzione prevede la gestione di diversi template, che andranno rivisti per renderli utilizzabili anche per l’OE Ingiunzione al pagamento.
Rinnovazione Notifica successiva alla Richiesta Informazioni
La funzione ricalcherà quella attualmente disponibile  per l’ordine di esecuzione con decreto sospensione. Bisognerà verificare che l’attuale comportamento, descritto di seguito, sia valido anche per l’ordine di Ingiunzione al pagamento.
La form attuale presenta due radio button che non trasformano la form, ma hanno lo scopo di pilotare 2 template differenti

a seguito della conferma il sistema inserisce un nuovo record nella tabella RINNOVO, collegato alla Notifica, aggiorna lo stato del procedimento e visualizza la funzione di Dettaglio, da cui è possibile produrre la stampa della comunicazione da inviare all’autorità destinataria.
Anche questa funzione prevede la gestione di due template (SIEP_GDS_RIN_UFFG.rtf, SIEP_GDS_RIN_POL.rtf) che andranno rivisti per renderli utilizzabili anche per l’OE Ingiunzione al pagamento.
Solleciti
La funzione ricalcherà quella attualmente disponibile  per l’ordine di esecuzione con decreto sospensione. Bisognerà verificare che l’attuale comportamento, descritto di seguito, sia valido anche per l’ordine di Ingiunzione al pagamento.
La form attuale presenta due radio button che non trasformano la form, ma hanno lo scopo di pilotare 2 template differenti

a seguito della conferma il sistema inserirà un nuovo record nella tabella RINNOVO, collegato alla Notifica, aggiorna lo stato del procedimento e visualizza la funzione di dettaglio, da cui è possibile produrre la stampa della sollecito da inviare all’autorità destinataria.
Anche questa funzione prevede la gestione di due template (SIEP_GDS_SOLL01.rtf, SIEP_GDS_SOLL02.rtf) che andranno rivisti per renderli utilizzabili anche per l’OE Ingiunzione al pagamento.
Verbale Vane Ricerche
La funzione andrà rivista per consentirne l’uso anche per l’ordine di esecuzione di Ingiunzione al Pagamento della Pena Pecuniaria.
Nota trasmissione  Bollettini rate successive alla prima
Per consentire la trasmissione dei Bollettini di pagamento delle rate successive alla prima con le date di scadenza, calcolate dal sistema successivamente all’annotazione della notifica dell’ordine di ingiunzione, bisogna prevedere l’emissione di un Avviso di pagamento che accompagni l’invio degli Avvisi di pagamento cartacei, generati da pagoPA.
A tale scopo l’attuale voce , presente nel menu Gestione Riscossione Pene Pecuniarie, sarà modificato in , selezionandolo il sistema presenterà le seguenti voci

da cui sarà possibile attivare le relative funzioni.
Ordine Ingiunzione Pagamento
Nella form di inserimento dell’ordine il n.ro di giorni entro cui effettuare il pagamento dell’unico bollettino o del primo, in caso di rateizzazione, a partire dalla data di notifica del provvedimento è riportato in base al dato inserito dall’utente in fase di valorizzazione delle modalità di pagamento della pena pecuniaria. Come previsto dalla norma il n.ro giorni è fissato rispettivamente in 90 e 30, pertanto, al momento dell’inserimento Modalità di Pagamento Pena, questo dato dovrà essere preimpostato dal sistema e non dovrà essere modificabile



Nota trasmissione bollettini rate successive alla prima
La funzione controllerà che siano stati generati da pagoPA i bollettini relativi alle rate successive alla prima, in caso di mancata generazione invierà il messaggio bloccante

in caso di avvenuta generazione, il sistema invierà la seguente form

La funzione inserirà in base dati una Comunicazione Nota trasmissione bollettini rate successive alla prima e presenterà la form di Dettaglio da cui sarà possibile selezionare le azioni di Stampa, Validazione, Modifica e Cancellazione.
Selezionando l’azione di stampa il sistema produrrà l’avviso che accompagnerà i bollettini pagoPA delle rate successive alla prima (SIEP 2023-44_avviso pagamento e invio bollettini PagoPA.rtf), che saranno inviati al condannato.
Da valutare, in caso di generazione di tutti i bollettini successivamente all’emissione dell’OI, se inserire la nota di trasmissione come allegato al documento dell’ordine di ingiunzione. Bisogna inoltre decidere se va annotata l’avvenuta notifica della nota di trasmissione.
Gestione Bollettini pagoPA
Nella prima versione della gestione del pagamento delle pena pecuniarie tramite PST/pagoPA era stato necessario impostare la data di scadenza dei bollettini a una data futura fittizia (31/12/2049) per rispettare i seguenti requisiti:
- consentire al condannato di poter pagare il bollettino successivamente alla reale data di scadenza, in presenza del vincolo da parte di pagoPA che il pagamento avvenisse entro la data riportata sull’avviso di pagamento;
- consentire al condannato di poter pagare, anche successivamente alla data di scadenza reale, calcolata successivamente all’avvenuta notifica dell’OE , e fino all’emissione di un nuovo provvedimento che stabilisca nuove modalità di pagamento, come previsto dall’attuale normativa.
Successivamente al rilascio della suddetta versione, PST ha comunicato che, a seguito di aggiornamenti avvenuti su pagoPA, il pagamento del bollettino è consentito anche successivamente al superamento della data scadenza riportata sullo stesso.
Decaduto il vincolo del pagamento entro la data di scadenza, permane il problema di come comunicare al condannato, in caso di pagamento rateizzato della pena pecuniaria, le reali date di scadenza di pagamento delle rate successive alla prima, riportate sul documento cartaceo Bollettino pagoPA, superando l’attuale impostazione di una data futura.
Il GdL Siep ha quindi deciso di poter operare in una delle due seguenti modalità:
modalità 1
successivamente all’emissione dell’ordine di Ingiunzione al pagamento si procede alla richiesta di generazione del bollettino relativo al pagamento in una unica soluzione o di tutti i bollettini, in caso di rateizzazione, facendo impostare dal sistema una data di scadenza del primo bollettino, che tenga conto dei tempi necessari per la  notifica e dei giorni previsti per legge per il pagamento dopo l’avvenuta notifica  (90 giorni in caso di pagamento in unica rata e 30 giorni in caso di pagamento rateale); per cui si è deciso di calcolare la data scadenza rispettivamente a 120 gg e a 60 gg dalla data emissione del provvedimento, tenendo conto anche di possibili ritardi nella fase di notifica. In caso di rateizzazione, il sistema imposterà le date scadenza delle rate successive sull’ultimo giorno dei mesi successivi alla data di scadenza prima rata. Tutti i bollettini saranno stampati ed inviati insieme all’Ordine di Ingiunzione per la notifica al condannato;
modalità 2
successivamente all’emissione dell’ordine di Ingiunzione al pagamento si procede alla richiesta di generazione del bollettino relativo al pagamento in una unica soluzione o al pagamento della prima rata, in caso di rateizzazione, facendo impostare dal sistema una data di scadenza, che tenga conto dei tempi necessari per la  notifica e dei giorni previsti per legge per il pagamento dopo l’avvenuta notifica  (90 giorni in caso di pagamento in unica rata e 30 giorni in caso di pagamento rateale); per cui si è deciso di calcolare la data scadenza rispettivamente a 120 gg e a 60 gg dalla data emissione del provvedimento, tenendo conto anche di possibili ritardi nella fase di notifica;
successivamente all’annotazione di avvenuta notifica dell’ordine di ingiunzione, il sistema calcola la data di scadenza reale del primo pagamento e, in caso di rateizzazione, calcola le date scadenze delle rate successive impostandole sulle date di fine mese dei mesi successivi alla data di scadenza del primo bollettino. In caso di rateizzazione l’utente procede alla richiesta a PST/pagoPA di generazione dei bollettini successivi al primo e, in caso di esito positivo da parte di pagoPA, procede alla stampa di tutti i bollettini e all’emissione dell’Avviso pagamento, descritto al precedente paragrafo.
Per effetto di quanto descritto in precedenza è stata rivista la precedente funzione “Richiesta Bollettini”, introducendo la possibilità da parte dell’utente, in base al modus operandi dell’ufficio, di poter richiedere la generazione dei bollettini, secondo le due modalità sopra descritte.

Richiesta Bollettini
Da questa funzione  sarà possibile richiedere la generazione dell’unico bollettino in caso di pagamento in un’unica soluzione, oppure ,in caso di rateizzazione, di poter richiedere la generazione di tutti i bollettini oppure solo del primo oppure dei bollettini restanti, solo se già risulta generato il bollettino della prima rata.
In caso di generazione dei bollettini rateizzati in due diversi momenti, prima rata e restanti rate, per trasmettere i bollettini delle restanti rate, l’ufficio dovrà generare un Avviso di pagamento di accompagnamento.
La funzione, in base alle modalità di pagamento (unica soluzione o rateizzato) presenterà una della seguenti form:

oppure

selezionando l'icona Inoltra  il sistema acquisisce la data della richiesta e visualizza i dati del bollettino da trasmettere a PST per l'inoltro a pagoPA e presenta una delle seguenti form
Rata unica

Oppure
Rateizzazione pagamento

In caso di rateizzazione il sistema presenta 3 opzioni per la generazione dei bollettini:
Alla prima richiesta è possibile generare tutti i bollettini o solo il bollettino relativo alla prima rata
Alla seconda richiesta, nel caso che nella prima abbia richiesto la generazione solo del bollettino  della prima rata, può effettuare solo la richiesta di generazione dei restanti bollettini.
Sia in caso di unica soluzione, che in caso di rateizzazione, selezionando il tasto  il sistema inoltrerà la richiesta e rimarrà in attesa della ricezione del bollettino/dei bollettini, in attesa del quali a video apparirà l’immagine di elaborazione in corso

a conclusione della quale apparirà a video il seguente messaggio

Cliccando su OK, il sistema aggiornerà la base dati di SIES con i dati ricevuti e presenterà la form di richiesta

simile alla prima form, ma con Data Richiesta e Data Ricezione valorizzate e priva del tasto Inoltra, cliccando sull’icona Visualizza il sistema presenterà , in caso pagamento in unica soluzione, bollettino completo dello IUV e del documento pdf

da cui sarà possibile stampare il documento in formato pdf, selezionando l’icona di stampa.
In caso di pagamento rateizzato, se l’utente ha selezionato l’opzione tutti, riceverà l’elenco di tutti i bollettini completi di IUV e del documento.pdf

da cui sarà possibile stampare i documenti in formato pdf, relativi a tutti i bollettini, selezionando l’icona di stampa , presente accanto all’intestazione della funzione, oppure stampando ogni singolo bollettino,  selezionando l’icona di stampa presente nella colonna Azioni ad esso relativa.
Nel caso che, in fase di generazione, l’utente avesse selezionato solo quello relativo alla prima rata, il sistema presenterà la seguente form

In quest’ultimo caso, per la stampa dei restanti bollettini, che dovrebbe avvenire dopo l’avvenuta annotazione della notifica del primo bollettino al condannato (da decidere se inserire un controllo bloccante sull’avvenuta valorizzazione della suddetta data), l’utente seleziona nuovamente la funzione richiesta bollettini, il sistema verifica che vi siano bollettini ancora da generare, per cui anche in presenza della data richiesta e della data ricezione, presenta il tasto Inoltra

Selezionandolo si riceverà la form, che presenterà l’elenco dei rimanenti bollettini da generare

Da cui selezionando il tasto  il sistema inoltrerà la richiesta e rimarrà in attesa della ricezione dei bollettini, in attesa del quali a video apparirà l’immagine di elaborazione in corso

a conclusione della quale apparirà a video il seguente messaggio

Cliccando su OK, il sistema aggiornerà la base dati di SIES con i dati ricevuti e presenterà la form di richiesta

simile alla prima form, ma con Data Richiesta e Data Ricezione valorizzate e priva del tasto Inoltra, cliccando sull’icona Visualizza il sistema presenterà i bollettini completi dello IUV e del documento pdf

da cui sarà possibile stampare i documenti in formato pdf, relativi a tutti i bollettini, selezionando l’icona di stampa , presente accanto all’intestazione della funzione, oppure stampando ogni singolo bollettino,  selezionando l’icona di stampa presente nella colonna Azioni ad esso relativa.
Di seguito possibili controlli da poter inserire sulla generazione dei rimanenti bollettini:
All’attivazione della funzione il sistema effettuerà il controllo sulla presenza della data di notifica al condannato, in caso di assenza di questa data si riceverà il seguente messaggio bloccante

poi controllerà la presenza dello IUV sul bollettino della prima rata, in caso di assenza si riceverà il seguente messaggio bloccante


Modifica Gestione Bollettini Pagamento e relativa storicizzazione
Al momento non vi è la storicizzazione della modalità di pagamento, né dei bollettini generati. L’importo da pagare e le modalità di pagamento, unica soluzione o rateizzazione, sono collegati alla pena complessiva, in quanto rappresentano i dati presenti nella sentenza di condanna. In caso di errata indicazione dell’importo e/o delle modalità di pagamento, l’utente deve svalidare il procedimento e modificare i dati, senza che rimanga alcuna traccia nella base dati.
Considerando la vita procedurale di un procedimento di gestione della pena pecuniaria, questa impostazione andrà rivista, in base alle seguenti ipotesi operative.
Procedimento privo di Ordine di ingiunzione al pagamento
La modifica dei dati della modalità pagamento si effettua, secondo le attuali regole: svalidazione procedimento, modifica dei dati e nessuna storicizzazione dei dati.
Procedimento con Ordine di ingiunzione al pagamento emesso e validato e poi annullato, in quanto errato
In questo caso al momento dell’annullamento dell’OI, il sistema storicizza i dati della modalità pagamento e i bollettini generati, l’annullamento deve essere possibile solo se non risulta già pagato alcun bollettino.
Al momento dell’emissione di un nuovo ordine di ingiunzione, il sistema accorgendosi che non esiste alcuna modalità di pagamento non collegata a un evento valido o non collegata ad alcun evento, riproporrà la form di Inserimento Modalità Pagamento e successivamente quella di Inserimento dell’Ordine di Ingiunzione al Pagamento, i dati della modalità pagamento e i relativi bollettini faranno riferimento a questo Evento.
#### Rideterminazione della pena pecuniaria
A seguito di provvedimento da parte del Giudice dell’esecuzione o a seguito provvedimento di cumulo, l’ufficio esecuzione può avere esigenza di emettere un nuovo OI, riferito a nuovo importo da pagare e con nuove modalità.
Selezionando la funzione , il sistema presenterà la form di Inserimento Modalità Pagamento, che inserirà nella base dati i nuovi dati, che faranno riferimento al provvedimento che sarà inserito con la form che il sistema presenterà dopo l’inserimento delle modalità pagamento

in cui sarà possibile annotare gli estremi del provvedimento del Giudice dell’Esecuzione o del provvedimento di cumulo, la data emissione e trasmissione, le autorità destinatarie per la notifica alle parti.
A seguito della conferma il sistema inserirà il nuovo provvedimento e le nuove modalità di pagamento in base dati e presenterà la form di dettaglio, da cui sarà possibile procedere alla modifica, alla stampa, alla validazione e alla cancellazione.
Per questo nuovo provvedimento sarà possibile procedere alla generazione dei bollettini e alla loro gestione.
Per questo provvedimento deve essere prevista la funzione di Annotazione data avvenuta notifica.

#### Avviso Mancato Pagamento
In caso di procedimento con pagamento rateizzato il mancato pagamento di una o parte delle rate comporta la decadenza del beneficio della rateizzazione, in tal caso l’ufficio deve emettere un provvedimento di Avviso di mancato pagamento che prevede il pagamento del restante importo in un’unica soluzione entro 60 giorni dalla notifica.
Selezionando la funzione , il sistema verificherà preventivamente che siamo in presenza di pagamento rateizzato della pena pecuniaria e che vi siano rate non pagate, al verificarsi di queste condizioni il sistema presenterà la form di Verifica Stato Bollettini

Da cui selezionando il tasto , il Sistema presenterà la form

in cui riporterà l’importo da pagare e la modalità di pagamento in un’unica soluzione. A seguito della conferma il sistema inserirà in base dati il nuovo provvedimento, la relativa modalità di pagamento e presenterà la form di Dettaglio, da cui sarà possibile procedere alla modifica, alla stampa, alla validazione e alla cancellazione.
Per questo nuovo procedimento sarà possibile procedere alla generazione del bollettino e alla sua gestione.
Per questo provvedimento deve essere prevista la funzione di Annotazione data avvenuta notifica.

#### Provvedimento Estinzione della Pena Pecuniaria
In caso di procedimento con avvenuto pagamento dell’intero importo, l’ufficio deve emettere un provvedimento di Estinzione della Pena Pecuniaria .
Selezionando la funzione , il sistema verificherà preventivamente che per il procedimento in esame l’importo dell’importo da pagare e il totale dei bollettini pagati corrispondano, in caso di non corrispondenza sarà inviato apposito messaggio bloccante all’utente, in caso di corrispondenza il sistema invierà la seguente form

in cui l’utente valorizzerà le date di emissione e trasmissione, il magistrato e le autorità delegate alla notifica. A seguito della conferma il sistema inserirà in base dati il nuovo provvedimento e presenterà la form di Dettaglio, da cui sarà possibile procedere alla modifica, alla stampa, alla validazione e alla cancellazione.

#### Trasmissione Atti per la Conversione
In caso di mancato pagamento della pena pecuniaria in unica soluzione il pubblico ministero trasmette gli atti al magistrato di Sorveglianza perché decida in merito alla Conversione della pena.
Selezionando la funzione , il sistema presenterà una form simile a quella già presente in SIEP per la conversione delle pene pecuniarie (classe 7)


in cui riporterà l’importo non pagato. A seguito della conferma il sistema inserirà in base dati il nuovo evento, presenterà la form di Dettaglio, da cui sarà possibile procedere alla modifica, alla stampa, alla validazione e alla cancellazione.
Sarà possibile effettuare la Verifica esito trasmissioni atti per Competenza e Riscontro trasmissione - annotazione della presa in carico.
#### Definizione Procedimento Pena Pecuniaria
Per l’archiviazione del procedimento, successivamente all’emissione del provvedimento di estinzione della Pena Pecuniaria, si adatterà l’attuale funzione di Definizione Procedimento>Fine espiazione

Inserendo nella combo box  Oggetto Definizione la voce Archiviazione a seguito Estinzione della Pena Pecuniaria. A seguito della conferma il sistema inserirà in base dati il nuovo evento di archiviazione, presenterà la form di Dettaglio, da cui sarà possibile procedere alla modifica, alla stampa, alla validazione e alla cancellazione.
Verifica Stato Bollettini
Nella form bisognerà inserire, accanto agli estremi dell’ordine di ingiunzione al pagamento, anche la data di notifica dello stesso al condannato. Pertanto nella maschera sarà riportata l’informazione, come appare di seguito nel riquadro in rosso

la dicitura “notificato il” sarà riportata anche se per il provvedimento non risulta ancora valorizzata.
Scadenzari
Questa voce del menu Riscossione Pene Pecuniarie consentirà di accedere alle diverse tipologie di scadenzari, previsti per la Gestione delle Pene Pecuniarie

selezionandola il sistema presenterà l’ulteriore form

Scadenzario Stato Pagamenti
Come detto al par. 2.3.1 questo scadenzario si attiva al momento in cui l’utente annota la data della notifica al condannato dell’ordine di ingiunzione al pagamento. Il sistema calcola la data di scadenza per il pagamento dell’avviso PagoPA, relativo all’unica soluzione o alla prima rata in caso di rateizzazione, e in quest’ultima caso provvede a calcolare anche le scadenze delle rate successive.
La funzione in esame presenterà la seguente form:


In cui sarà possibile richiedere una delle seguenti estrazioni dei pagamenti per i quali risulta notificato al condannato il relativo Ordine di esecuzione di Ingiunzione al pagamento:
Tutti            		mostrerà tutti gli avvisi di pagamento scaduti e in scadenza futura;
In scadenza		in questo caso bisognerà indicare la data termine ricerca, che il sistema
calcolerà in base al periodo digitato (anni, mesi e giorni) a partire dalla data di elaborazione; mostrerà tutti gli avvisi di  pagamento con data scadenza <= data termine, non pagati, a partire dalla data elaborazione;
In scadenza oggi	mostrerà tutti gli avvisi di pagamento con data scadenza = data
elaborazione
Scaduti			mostrerà tutti gli avvisi di pagamento, non pagati, con data scadenza < data
elaborazione
Sarà possibile restringere le suddette ricerche a un solo procedimento, valorizzando l’anno e numero dello stesso.
Il sistema presenterà i risultati della ricerca in un elenco, impaginato, ordinato per data scadenza crescente



Chiaramente in caso di rateizzazione lo stesso procedimento potrà essere riportato più volte per rate differenti.
In presenza di istanza di rateizzazione, finché non risulteranno pagate tutte le rate, il procedimento non va considerato come scaduto.
Selezionando l’azione di Dettaglio per uno degli elementi della lista, il sistema presenterà la form di Verifica Stato Bollettini



che in caso di pagamento rateizzato permette di avere lo stato di pagamento di tutti i bollettini.
Ricerca procedimenti per Stato Pagamenti
Al fine di permettere all’ufficio di avere un resoconto dei procedimenti rispetto allo stato dei pagamenti, in base al quale poter poi procedere con l’emissione di specifici provvedimenti sarà realizzata la seguente funzione



in cui è possibile impostare 3 seguenti tipologie di procedimenti, restringendo opzionalmente la ricerca per intervallo di estremi Procedimenti o per intervallo Date iscrizioni:

Procedimenti con pene pecuniaria totalmente pagata, in questo caso il sistema ricercherà tutti i procedimenti con pagamento rateizzato della pena pecuniaria, non archiviati,  con data ultima scadenza pagamento <= data elaborazione, privi di un Avviso mancato pagamento validato, per i quali il totale degli importi pagati non coincida con l’importo da pagare e ne presenterà l’elenco

Da cui selezionando l’azione di Dettaglio, si riceverà la form del Provvedimento Estinzione Pena Pecuniaria (vedi par. 2.5.2.3).

Procedimenti con pagamento in unica soluzione non pagata, in questo caso il sistema ricercherà tutti i procedimenti con pagamento in unica soluzione, non archiviati e per i quali non risulti una Trasmissione Atti per la Conversione, per i quali la somma pagata non i coincida con l’importo da pagare e ne presenterà l’elenco

Da cui selezionando l’azione di Dettaglio, si riceverà la form dell’Avviso Mancato Pagamento (vedi par. 2.5.2.2).

Procedimenti con pagamento rateizzato con rate non pagate, in questo caso il sistema ricercherà tutti i procedimenti, non archiviati e per i quali non risulti un provvedimento di estinzione della pena pecuniaria validato, per i quali il totale degli importi pagati coincida con l’importo da pagare e ne presenterà l’elenco

Da cui selezionando l’azione di Dettaglio, si riceverà la form di Trasmissione Atti per la Conversione (vedi par. 2.5.2.4).

Sarà possibile generare il contenuto degli Elenchi sopra riportati in formato .xls.
Gestione Pene Sostitutive Brevi
Per l’esecuzione delle pene sostitutive brevi di tipo detentive bisognerà selezionare nel menu Gestione Altre Sanzioni la voce Esecuzione Pene Detentive Brevi

che presenterà a sua volta il seguente menu

Semilibertà/Detenzione Domiciliare Sostitutive
Dal menu Esecuzione Pene Sostitutive Brevi, selezionando
si riceverà l’ulteriore menu

#### Trasmissione Atti per Esecuzione
La funzione permetterà di inserire la trasmissione degli atti relativi alla Pena Sostitutiva all’UDS di Sorveglianza perché provveda ad iscrivere ed esprimersi sull’applicabilità della stessa. Selezionando la voce Trasmissione Atti per Esecuzione il sistema invierà la seguente form



oppure in caso di condannato in misura o detenuto



che, a seguito della Conferma, inserirà la trasmissione in base dati e presenterà la form di dettaglio



Modificare la trasmissione o stampare il relativo documento,  a seguito della quale, il sistema presenterà gli ulteriori campi



per la validazione  Conferma o per la validazione e contemporanea trasmissione alla Sorveglianza Conferma Trasmissione.
Bisognerà rivedere anche i template SIEP_SANSOST_RITRASMATTI.rtf e NOTA_TRASMISSIONE.rtf, facendo riferimento alle pene sostitutive nei punti in cui fanno riferimento alle sanzioni sostitutive.
Per la gestione di questo nuovo atto, da parte della Sorveglianza, conformemente a quanto riportato nella Scheda_35, saranno aggiunti in SIUS un nuovo contenuto “Applicazione pene sostitutive” e i relativi oggetti ed esiti. Sarà inoltre rivista la funzione di presa in carico e la funzione di presentazione del procedimento di iscrizione SIUS.
#### Riscontro Trasmissione Atti per Esecuzione
La funzione permetterà di verificare lo stato degli atti trasmessi. Selezionando la voce Riscontro Trasmissione Atti per Esecuzione nel menu di cui al par. 2.7.1, il sistema invierà la seguente form


Che consentirà di estrarre gli atti trasmessi alla Sorveglianza e relativi all’esecuzione delle Pene Sostitutive, con la possibilità di impostare vari filtri.
Il sistema ricercherà gli atti trasmessi, soddisfacenti le condizioni impostate, e presenterà la form con l’elenco



Per ciascun elemento della lista sarà possibile visualizzare il Dettaglio




Oppure


Batch di verifica stato del Pagamento
A seguito dei ripensamenti sul calcolo data scadenza dei bollettini, che sarà calcolata solo a seguito della valorizzazione della data di notifica al condannato dell’ordine di ingiunzione, il batch sarà modificato eliminando il calcolo, in caso di rateizzazione, delle date scadenze dei bollettini relativi alle rimanenti rate al momento della registrazione dell’avvenuto pagamento del primo bollettino.
Interventi sottosistema SIGE
Aggiornamento template Fissazione Udienza
È necessario modificare la dicitura presente nell’attuale documento per adeguarlo alla nuova normativa.

o Vecchia frase

AVVERTE
il condannato detenuto:
➢ in  luogo  posto  nella circoscrizione  del  Giudice  che  può  chiedere  la  traduzione all’udienza;
➢ in  luogo  posto fuori della circoscrizione del  Giudice, che, se ne farà  richiesta,  sarà sentito,
prima  del  giorno  dell’udienza  dal  Magistrato  di  Sorveglianza  del  luogo  di detenzione,  salvo
che  il  Giudice  dell’esecuzione,  non  ne  disponga  d’ufficio  la traduzione.
o Nuova frase prevista dall’art art. 666, comma 4 c.p.p.

AVVERTE
il condannato detenuto:
➢in luogo posto nella circoscrizione del Giudice che può chiedere la traduzione all’udienza_;
L'interessato che ne fa richiesta è sentito personalmente.  A tal fine si procede   mediante collegamento a distanza, quando una particolare disposizione di legge lo prevede o quando l’interessato vi consente.  Tuttavia, se è detenuto o internato in luogo posto fuori della circoscrizione del giudice e non consente all’audizione mediante   collegamento   a distanza, l'interessato è sentito prima del giorno dell’udienza dal magistrato di  sorveglianza  del  luogo, salvo  che  il  giudice ritenga di disporre la traduzione.
Integrazione Tabelle Oggetti
Per effetto della nuova normativa bisognerà aggiungere nella base dati i seguenti oggetti ed esiti per consentire l’iscrizione e la gestione dei nuovi procedimenti.
#### Art. 95 disposizioni transitorie in materia di pene sostitutive delle pene detentive
Si procederà all’inserimento dei seguenti elementi:
Contenuto:	applicazione pene sostitutive delle pene detentive brevi art. 95. D.lgs. 150/22

Oggetti:	Applicazione della pena in semilibertà sostitutiva;
Applicazione della pena in detenzione domiciliare sostitutiva;
Applicazione della pena il lavoro di pubblica utilità sostitutivo;
Applicazione della pena la pena pecuniaria sostitutiva.
Esiti:		applica la Pena sostitutiva breve
rigetta l’istanza;
dichiara il non luogo a provvedere;
dichiara il non doversi procedere;
dichiara l’inammissibilità;
dichiara la propria la propria incompetenza
#### Riduzione pena art. 442, comma 2-bis - D.lgs. 150/22
Si procederà all’inserimento dei seguenti elementi:
Contenuto:	riduzione della pena articolo 442, comma 2-bis

Oggetti:	riduzione della pena articolo 442, comma 2-bis

Esiti:		applica riduzione pena
rigetta l’istanza;
dichiara il non luogo a provvedere;
dichiara il non doversi procedere;
dichiara l’inammissibilità;
dichiara la propria la propria incompetenza
Gestione errori con pagoPA
L’ipotesi è di realizzare due cruscotti per la gestione degli errori: uno per il batch e l’altro per le funzionalità web.
Cruscotto per funzionalità Batch
La funzione è disponibile solo per l’utente con profilo di Amministratore di sistema.
Per la gestione degli errori delle verifiche, dello stato di pagamento dei bollettini generati, non andate a buon fine, tramite batch, viene realizzato un cruscotto dedito alla visualizzazione di queste verifiche.
Per popolare questa form verranno interrogate le tabelle:
BOLLETTINO_PAGOPA (aggiungendo una foreign key – BATCH_ID_BATCH_PAGOPA - su tabella BATCH_PAGOPA) e BATCH_PAGOPA.
Verrà creata, inoltre, una tabella di correlazione dove verranno inseriti oltre alle due Primary Key anche le informazioni circa l’esito della richiesta:
Stato della richiesta, che contiene l’indicazione dello stato del pagamento nel contesto del PST e può assumere uno dei seguenti valori:
•	DISPONIBILE, indica che è presente la RT (sicuramente positiva) e non è stata utilizzata dall’utente:
•	USATO, indica che il pagamento è stato utilizzato;
•	OK_PSP, indica che l’utente ha eseguito un tentativo di pagamento ma ancora non è disponibile la RT;
•	RIMBORSATO, indica che il pagamento è stato rimborsato dall’Amministrazione;
errore (errore in fase di verifica più il messaggio dell'eccezione ottenuta);
tipo errore (servizio assente oppure errore durante l’elaborazione);
esito esecuzione.
Dalla form del cruscotto verrà data la possibilità di reindirizzare sulla pagina di elenco bollettini controllati per cui si è verificato l’errore, sia per l’interrogazione massiva (previa selezione dei bollettini da verificare) o puntuale del bollettino non verificato.
Di seguito, un esempio di form per il cruscotto degli errori:

Di seguito, la proposta di una eventuale form per la schedulazione del batch in tempo reale:


Tale funzionalità dovrebbe essere usufruibile solo dall’Amministratore di sistema se si ritiene il caso di riprovare i batch che sono andati in errore, ovvero compiere una azione correttiva (cioè rilanciare la richiesta di verifica stato bollettini).
Premendo l’icona di modifica si ottiene la seguente form:

La modifica della schedulazione del batch PagoPA ha effetto solo per il tempo di durata della sessione di SIES, quindi fino allo stop di JBoss.
Per il resto, rimane valida la schedulazione impostata nel file f3b.properties.
#### Informazione per gli uffici
Nella homepage dell’applicativo sarà presente, in caso di errore o malfunzionamento del batch notturno, una icona (Avviso Batch PagoPA) di attenzione (in alto a destra) che segnalerà l’errata esecuzione:

Cliccando sull’icona, il sistema prospetterà la seguente pagina:

dove, cliccando sull’icona “Verifica Batch PagoPA”, il sistema indirizzerà alla pagina di dettaglio esecuzione batch, dove sarà possibile decidere se riavviare il batch stesso:

Cruscotto per funzionalità web
La funzionalità è utilizzabile da parte dell’utente che ha riscontrato l’errore e dagli utenti con profilo di amministratore di ufficio.
Creazione della tabella “ERRORI_SIES_PAGOPA”:
| ID_ERRORI_SIES_PAGOPA | Number(38) |
| --- | --- |
| ID_FASCICOLO_SIEP | Number(38) |
| ID_EVENTO | Number(38) |
| AZIONE_CONTESTO_JAVA | VARCHAR2(100) |
| DESCRIZIONE_FUNZIONE | VARCHAR2(100) |
| COD_UTENTE | VARCHAR2(100) |
| COD_UFFICIO | VARCHAR2(11) |
| ERRORE_ESECUZIONE | VARCHAR2(2000) |
| DATA_INSERIMENTO | DATE |
| DATA_VISUALIZZAZIONE | DATE |
| COD_UTENTE_VISUALIZZAZIONE | VARCHAR2(100) |

Il sistema inserirà un record ogni volta che da applicazione verrà invocato uno dei due web services PST/PagoPA; il record verrà cancellato in caso di esito positivo della richiesta, in caso di esito negativo verrà valorizzata la colonna “ERRORE_ESECUZIONE”.
Al momento le funzionalità che invocano i due web services PST/PagoPA sono: “Richiesta Bollettini …” (due voci) e “Verifica stato bollettino su PagoPA”.
La funzione potrà essere richiamata dall’utente, non amministratore di ufficio, dal menù:

attivata da questo menù la funzione filtrerà solo le richieste inoltrate dall’utente connesso, per le quali non ci sia stata risposta da PST/PagoPA.
Per l’utente Amministratore di Ufficio si inserirà la nuova voce nel menù laterale verticale

Selezionandola si riceverà la seguente form:

In cui sarà possibile impostare dei filtri per data e per utente, ed a seguito dell’avvio della ricerca il sistema presenterà la seguente form:


Selezionando l’icona di Dettaglio nella colonna “Azioni”, il sistema visualizzerà la form della funzionalità in errore al fine di re innescarla dal punto precedente al verificarsi dell’errore.
Test di Sistema
È necessario aggiungere due controlli alla funzionalità “Test Sistema” (fruibile solo per l’Amministratore di sistema) per verificare la connessione ai due servizi esposti dal PST per PagoPA:
https://servizibe.processotelematico.giustizia.it/servizi/ServiziInvioPagamentiTelematici
https://servizibe.processotelematico.giustizia.it/servizi/ServiziConsultazionePagamentiTelematici
Nella sezione dei Web Services del file “SIES_TEST.rtf” saranno presenti le due nuove frasi (esempio in caso di errore):