---
uniqueName: siut-sies-mu-1-0-20240419-manualeutente2019009siep
displayName: "SIUT SIES MU 1 0 20240419 Manuale Utente 2019 009 SIEP FASE 2 D lgs 123 2018"
category: "GENERAL"
tags: []
---

# SIUT-SIES-MU-1.0-20240419-Manuale_Utente_2019_009_SIEP_FASE-2_D.lgs.123-2018

> **File originale:** `MEV/SCHEDA_009/2019_09-SIEP-Originali/SIUT-SIES-MU-1.0-20240419-Manuale_Utente_2019_009_SIEP_FASE-2_D.lgs.123-2018.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
| MEV2019_009_SIEP_FASE_2-     D.lgs.123/2018 |
|  |





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Engineering | RTI |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 19/04/2024 |  |
| Livello di riservatezza | L3 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 19/04/2024 | Prima emissione |  |



Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Salvatore Piazza | RTI |  | Technical Manager |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Francesco Rosati | RTI |  | Responsabile Manutenzione Correttiva
Referente Qualità e Sicurezza |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Referente PMO e Qualità |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |
| Luigi Buglione | RTI |  | Referente Metrico |


INDICE DEI CONTENUTI
1.	Introduzione	5
1.1.	Scopo del documento	5
1.2.	Glossario	5
1.2.1.	Definizioni	5
1.2.2.	Acronimi e abbreviazioni	5
2.	Ambito Normativo D.lgs. 123/2018	6
3.	Applicazione Provvisoria misure alternative (art. 678 comma 1-ter c.p.p.)	7
3.1	Adeguamento della funzione ‘ammissione provvisoria Affidamento al servizio sociale	8
3.2	Adeguamento della funzione Ammissione provvisoria Detenzione Domiciliare	13
3.3	Funzione ‘Ammissione/Applicazione Provvisoria’ per SEMILIBERTA’ (nuova)	19
3.4	Funzione ‘Applicazione Provvisoria per Sospensione Esecuzione Pena’ (nuova)	26
4.	Concessione misure alternative (art. 678 comma 1-ter c.p.p.) e Conferma dell’Applicazione Provvisoria misure alternative	31
4.1	Adeguamento delle Funzioni di Concessione misure presenti in Decisioni Sorveglianza	32
4.2	Adeguamento della funzione Concessione Affidamento in Prova al Servizio Sociale	33
4.3	Adeguamento della funzione Concessione Detenzione Domiciliare	40
4.4	Adeguamento della funzione Concessione Semilibertà	46
4.5	Adeguamento della funzione Concessione Sospensione Esecuzione Pena	54
5.	Aggiornamento delle funzioni statistiche Statistica Attività Magistrati e Riepilogo Ispettivo	61

# Introduzione
## Scopo del documento
Nel documento sono descritti gli interventi realizzati nel sistema SIES, sottosistema SIEP, con lo scopo di soddisfare i requisiti espressi dall’Amministrazione in relazione alla richiesta di adeguamento normativo del Sistema, nella sua interezza, al D.lgs. 123/2018 e al D.lgs. 121/2018.

Il documento espone gli interventi attinenti alle funzioni previsti nel sistema in base alle novità normative del decreto D.lgs.123/18 (maggiorenni e minorenni), descritte nel documento SIUT-SIE-SI-1.5-20240116_SI_MEV_2019_009_SIES_FASE-1_D.lgs.123-2018.docx.

## Glossario
## Definizioni
Si premette un glossario esplicativo delle abbreviazioni e dei termini tecnici e giuridici utilizzati nel documento (Tabella - Glossario dei termini e degli acronimi usati nel documento).

| Definizione | Descrizione |
| --- | --- |
| ReGIndE | Registro Generale degli Indirizzi Elettronici |
| Portal Liferay | Liferay è un entreprise portal free e open Source |
| PDF | Portable Document Format – Standard per scambio documenti elettronici |
| P7M | Estensione file firmato con modalità CAdES, ovvero il documento firmato ed il file con la firma digitale vengono inseriti insieme in una busta. |
| PDF Firmato | Firma digitale apposta con modalità PAdES in cui vengono sfruttate le caratteristiche dei documenti in formato pdf. Il file contenente la firma digitale viene inglobato insieme al documento stesso. |
| Web-based | Un programma in cui tutte le funzioni sono accessibili tramite un normale web-browser come Firefox, Chrome o Explorer. Questo significa che non è necessario effettuare l’installazione di alcun software sui computer dell’azienda che deve utilizzare il programma. |


## Acronimi e abbreviazioni
| Sigla | Descrizione |
| --- | --- |
| GSU | Gestione Servizi UNEP |
| PDOC | Sistema Piattaforma Documentale |
| PEC | Posta Elettronica Certificata |
| PST | Portale dei Servizi Telematici |
| REGE | Registro Generale delle Notizie di Reato |
| RG | Registro Generale |
| SNT | Sistema Notifiche Telematiche |
| UNEP | Ufficio Notificazioni Esecuzioni Protesti |
| XML | eXtensible Markup Language |


# Ambito Normativo D.lgs. 123/2018
In relazione al Capo II: DISPOSIZIONI PER LA SEMPLIFICAZIONE DEI PROCEDIMENTI, Art. 4: Modifiche al codice di procedura penale in tema di semplificazione, all'articolo 678, viene inserito il comma 1-ter che recita quanto segue:

«1-ter. Quando la pena da espiare non è superiore a un anno e sei mesi, per la decisione sulle istanze di cui all'articolo 656, comma 5, il presidente del tribunale di sorveglianza, acquisiti i documenti e le necessarie informazioni, designa il magistrato relatore e fissa un termine entro il quale questi, con ordinanza adottata senza formalità, può applicare in via provvisoria una delle misure menzionate nell'articolo 656, comma 5. L'ordinanza di applicazione provvisoria della misura è comunicata al pubblico ministero e notificata all'interessato e al difensore, i quali possono proporre opposizione al tribunale di sorveglianza entro il termine di dieci giorni. Il tribunale di sorveglianza, decorso il termine per l'opposizione, conferma senza formalità la decisione del magistrato.
Quando non è stata emessa o confermata l'ordinanza provvisoria, o è stata proposta opposizione, il tribunale di sorveglianza procede a norma del comma 1. Durante il termine per l'opposizione e fino alla decisione sulla stessa, l'esecuzione dell'ordinanza è sospesa.».

Per l’adeguamento alle suddette Disposizioni sono stati effettuati gli adeguamenti di seguito riportati al sottosistema SIEP di SIES.

- In relazione all’introduzione lato Sorveglianza dell’ordinanza di applicazione provvisoria secondo quanto previsto all’articolo 678 c.p.p. comma 1 ter, gli uffici PM (Procura della Repubblica Presso il Tribunale Ordinario) e PMM (Procura della Repubblica Presso il Tribunale per i Minorenni) devono poter gestire l’esecuzione dell’applicazione provvisoria della misura alternativa art. 678 c.p.p. comma 1 ter.
- In relazione all’introduzione dell’ordinanza di Conferma dell’ordinanza di applicazione provvisoria, gli uffici PM (Procura della Repubblica Presso il Tribunale Ordinario) e PMM (Procura della Repubblica Presso il Tribunale per i Minorenni) devono poter gestire la Conferma (Ratifica) dell’applicazione provvisoria della misura alternativa art. 678 c.p.p. comma 1 ter.
- Nell’ambito degli uffici PM (Procura della Repubblica Presso il Tribunale Ordinario) e PMM (Procura della Repubblica Presso il Tribunale per i Minorenni) integrare la gestione dell’ordinanza legata al contenuto SIUS di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ e   ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 2 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.) ’ per rito ordinario.
- Prevedere l’aggiornamento delle funzioni di ‘riepilogo ispettivo’ e ‘statistiche lavoro magistrati’, in modo da integrare la nuova tipologia di ordinanza di applicazione provvisoria (art. 678 c.p.p. comma 1 ter) e l’ordinanza di ratifica dell’applicazione provvisoria. Allineare anche lo stato di esecuzione.

# Applicazione Provvisoria misure alternative (art. 678 comma 1-ter c.p.p.)
La concessione dell’applicazione provvisoria alla misura alternativa è di competenza dei Tribunali di Sorveglianza, che, per mezzo di un magistrato designato, possono ‘applicare provvisoriamente’ la misura alternativa concessa secondo quanto previsto all’art. 678 comma 1 ter c.p.p..
L’ordinanza provvisoria diviene esecutiva trascorsi 10 giorni senza che venga proposta opposizione e, a seguito dell’esecutività della stessa, il Tribunale di Sorveglianza è tenuto a dare tempestiva comunicazione alla Procura. Dal punto di vista applicativo il Tribunale deve effettuare anche la trasmissione telematica della stessa.
Secondo quanto previsto all’art. 678 comma 1 ter introdotto con il d.lgs. 123/2018, l’ordinanza di ammissione provvisoria può essere adottata dal TDS per le seguenti misure alternative:

Affidamento in prova al servizio sociale (art. 47 O.P. -  art. 678 comma 1-ter c.p.p.);
Affidamento in prova al servizio sociale (art. 94 DPR 309/90 - art. 678 comma 1-ter c.p.p.);
Detenzione domiciliare (art. 47 ter O.P. - art. 678 comma 1-ter c.p.p.);
Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.);
Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.);
e dal TDSM per le seguenti misure:

Affidamento in prova al servizio Sociale  (art.4 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.)
Affidamento in prova in casi particolari  (artt.4 D.lgs. 121/2018 -  94 DPR 309/90, art. 678 comma 1 ter c.p.p.)
Affidamento in prova in prova con detenzione domiciliare (art.5 d.lgs. 121/2018, art. 678 comma 1 ter c.p.p.)
Detenzione domiciliare (art.6 d.lgs. 121/2018 , art. 678 comma 1 ter c.p.p.)
Semilibertà (art.7 d.lgs. 121/2018, art. 678 comma 1 ter c.p.p.)
Sospensione dell’esecuzione della pena detentiva (art. 90 D.P.R. 9 ottobre 1990, n. 309, art. 678 comma 1 ter c.p.p.)
L’area funzionale su cui ha impatto la gestione della ‘applicazione provvisoria’ (art. 678 comma 1-ter c.p.p.), è il menù ‘Decisioni della Sorveglianza’. Nello specifico, per ogni tipologia di misura alternativa su elencata, sono state riviste, integrate tutte le funzionalita di ’Ammissione Provvisoria’ e sono state realizzate nuove funzionalità per l’ammissione/applicazione provvisoria Semilibertà e l’Applicazione Provvisoria della  Sospensione dell’esecuzione della pena detentiva.
Si precisa che a fronte dei nuovi oggetti introdotti per la Sorveglianza, sopra riportati, per SIEP  si utilizzeranno i seguenti:
• Applicazione provvisoria Affidamento in prova al servizio sociale (art. 47 O.P. );

• Applicazione provvisoria Affidamento in prova al servizio sociale (art. 94 DPR 309/90);

• Applicazione provvisoria Detenzione domiciliare (art. 47 ter O.P.);

• Applicazione provvisoria Semilibertà (art. 50 comma 1 O.P. );

• Applicazione provvisoria Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 );


## 3.1	Adeguamento della funzione ‘ammissione provvisoria Affidamento al servizio sociale

Per il menù ‘Affidamento in Prova al Servizio Sociale’ l’attuale tasto funzione di ‘Ammissione Provvisoria’ è stato modificato in ‘Ammissione /Applicazione Provvisoria’, per cui il menu si presenta come di seguito

Figura 1: Menu Decisioni Sorveglianza/Affidamento in Prova (PM e PMM)

L’attuale form è stata modificata per poter gestire, oltre ai provvedimenti di Ammissione provvisoria dell’UDS/UDSM,  anche le ordinanze con contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’/ ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 2 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.)’,, relativamente agli oggetti di Affidamento, con esito ‘APPLICA PROVVISORIAMENTE’, del TDS/TDSM.
Le implementazioni realizzato sono relative ai tre punti indicati con la freccia rossa nella figura che segue:

Figura 2: Pagina Ammissione /Applicazione Provvisoria Affidamento in Prova (PM e PMM)


In particolare, per gli uffici PM (Procura Ordinaria maggiorenni), in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare, oltre agli attuali provvedimenti (decreto/ordinanza) di Ammissione provvisoria Affidamento in prova’, anche le ordinanze con esito ‘Applica Provvisoriamente’ e che afferiscono al nuovo contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’, relativamente agli oggetti relativi all’affidamento in prova, mentre per gli uffici PMM (Procura Ordinaria minorenni) il sistema deve permettere di visualizzare e caricare le ordinanze con esito ‘Applica Provvisoriamente’ e che afferiscono al nuovo contenuto ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 2 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.)’, relativamente agli oggetti relativi all’affidamento in prova..
Per quanto riguarda invece il campo ‘Oggetto Decisione’, nella combo box corrispondente, a fronte degli oggetti previsti per la Sorveglianza (vedi par. 3), devono essere previsti i corrispondenti oggetti SIEP.
Le voci da prevedere nella combo box Oggetti Decisione per gli uffici PM saranno



mentre per gli uffici PMM saranno



E’stato poi aggiunto il campo Data Esecutività dell’ordinanza di Applicazione provvisoria della misura.
Si evidenzia che il comportamenti della funzione è rimasto inalterato per gli oggetti preesistenti di Ammissione provvisoria.
Si evidenzia che il comportamento della funzione è rimasto inalterato per gli oggetti preesistenti di Ammissione provvisoria, pertanto i dati da impostare nella sezione ‘Provvedimenti della Sorveglianza’, possono essere recuperati in automatico dal link su descritto, ma possono essere inseriti anche manualmente da parte dell’utente, per cui i campi di tale sezione sono tutti editabili.
In caso di inserimento di Applicazione Provvisoria di una delle misure di affidamento, riportate nella combo box, l’utente clicca sul link Seleziona provvedimento di Sorveglianza dalla lista , il sistema ricerca le ordinanze di applicazione provvisoria di affidamento, emesse dal TDS, per procedimenti SIUS collegati al procedimento SIEP corrente e apre la popup con l’Elenco

da cui, selezionando l’ordinanza di interesse, il sistema importerà tutti i dati necessari alla compilazione della form di Ammissione/Applicazione, che si presenterà come di seguito

Figura 3: Pagina Ammissione /Applicazione Provvisoria Affidamento in Prova (PM e PMM)

Dopo aver compilato i restanti campi della form, indicando se l’ordinanza viene eseguita dalla Procura o se è stata già eseguita dalla Sorveglianza, l’utente conferma. A seguito della Conferma, il sistema inserirà nella base dati un nuovo Evento, di tipo Richiesta Verbale di sottoscrizione obblighi, se Eseguita da Procura, e di tipo Provvedimento, se eseguita da Sorveglianza, e presenterà la form di Dettaglio

Figura 4: Pagina Dettaglio Ammissione /Applicazione Provvisoria Affidamento in Prova

dalla quale è possibile selezionare l’azione di Modifica, di Stampa o di Validazione.
Selezionando l’azione di Modifica  , il sistema presenterà la form

Figura 5: Pagina Modifica Ammissione /Applicazione Provvisoria Affidamento in Prova

da cui è possibile modificare i dati di interesse e Confermare. Il sistema aggiornerà i dati nella base dati e ripresenterà l’azione di Dettaglio aggiornata.
Selezionando l’azione di Stampa  , il sistema genererà uno dei seguenti template:
SIEP_MA_APPLPRO_AFFI_LIB_PROC.rtf     in caso di Richiesta Verbale sottoscrizione obblighi

SIEP_MA_APPLPRO_AFFI_LIB_MDS.rtf      in caso di Provvedimento
Successivamente alla stampa della Richiesta o del Provvedimento, sarà possibile procedere alla Validazione dello stesso, che lo renderà non modificabile e aggiornerà lo stato procedimento e l’ultimo Evento come di seguito riportato, nei riquadri in grigio, nelle successive form di Dettaglio Procedimento

Figura 6: Pagina Dettaglio Procedimento a seguito Applicazione Provvisoria Affidamento in Prova (Esegue PM)


Figura 7: Pagina Dettaglio Procedimento a seguito Applicazione Provvisoria Affidamento in Prova (Esegue Sorv)

In caso di inserimento di Richiesta Verbale di sottoscrizioni obblighi ….., alla ricezione del verbale, l’ufficio dovrà provvedere all’annotazione dello stesso utilizzando la funzione di Registrazione Data Inizio Misura con il conseguente inserimento della Comunicazione Applicazione Provvisoria ad Affidamento al Servizio Sociale.

## 3.2	Adeguamento della funzione Ammissione provvisoria Detenzione Domiciliare
Per il menù ‘Detenzione Domiciliare l’attuale tasto funzione di ‘Ammissione Provvisoria’ è stato modificato in ‘Ammissione /Applicazione Provvisoria’, per cui il menu si presenta come di seguito

Figura 8: Menu Decisioni Sorveglianza/Affidamento in Prova (PM e PMM)

L’attuale form è stata modificata per poter gestire, , oltre ai preesistenti provvedimenti di Ammissione provvisoria dell’UDS/UDSM, anche le ordinanze con oggetto ‘Detenzione Domiciliare (Art. 47 ter O.P. - Art. 678 comma 1-ter c.p.p.)’ e con esito ‘APPLICA PROVVISORIAMENTE’ per gli uffici PM (Procura Ordinaria maggiorenni), oppure con oggetto ‘Detenzione domiciliare (art. 6 d.lgs. 121/2018 , art. 678 comma 1 ter cp.p.)’ sempre con esito ‘APPLICA PROVVISORIAMENTE’ per gli uffici PMM (Procura Ordinaria minorenni).
Le implementazioni realizzate sono relative ai quattro punti indicati con la freccia rossa nella figura che segue:

Figura 9: Pagina Ammissione/Applicazione Detenzione Domiciliare

In particolare, per gli uffici PM (Procura Ordinaria maggiorenni), in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare, oltre agli attuali provvedimenti (decreto/ordinanza) di Ammissione provvisoria Detenzione Domiciliare, anche le ordinanze con esito ‘Applica Provvisoriamente’ e che afferiscono al nuovo oggetto ‘Detenzione Domiciliare (Art. 47 ter O.P. - Art. 678 comma 1-ter c.p.p.)’, mentre per gli uffici PMM (Procura Ordinaria minorenni) il sistema deve permettere di visualizzare e caricare le ordinanze con esito ‘Applica Provvisoriamente’ e che afferiscono al nuovo oggetto ‘Detenzione domiciliare (art. 6 d.lgs. 121/2018 , art. 678 comma 1 ter cp.p.)’, relativamente agli oggetti relativi all’affidamento in prova.
Per quanto riguarda invece il campo ‘Oggetto Decisione’, nella combo box corrispondente, a fronte degli oggetti previsti per la Sorveglianza (vedi par. 3), devono essere previsti i corrispondenti oggetti SIEP.
Le voci da prevedere nella combo box Oggetti Decisione per gli uffici PM saranno



mentre per gli uffici PMM saranno




Sono stati poi aggiunti la combo Tipo Provvedimento (-, Decreto, Ordinanza) e il campo Data Esecutività dell’ordinanza di Applicazione provvisoria della misura.
Si evidenzia che il comportamento della funzione è rimasto inalterato per gli oggetti preesistenti di Ammissione provvisoria, pertanto i dati da impostare nella sezione ‘Provvedimenti della Sorveglianza’, possono essere recuperati in automatico dal link su descritto, ma possono essere inseriti anche manualmente da parte dell’utente, per cui i campi di tale sezione sono tutti editabili.

In caso di inserimento di Applicazione Provvisoria della Detenzione Domiciliare, l’utente clicca sul link Seleziona provvedimento di Sorveglianza dalla lista , il sistema ricerca le ordinanze di applicazione provvisoria di affidamento, emesse dal TDS, per procedimenti SIUS collegati al procedimento SIEP corrente e apre la popup con l’Elenco

da cui, selezionando l’ordinanza di interesse, il sistema importerà tutti i dati necessari alla compilazione della form di Ammissione/Applicazione, che si presenterà come di seguito

Figura 10: Pagina Inserimento Ammissione/Applicazione Detenzione Domiciliare

Dopo aver compilato i restanti campi della form, indicando se l’ordinanza viene eseguita dalla Procura o se è stata già eseguita dalla Sorveglianza, l’utente conferma. A seguito della Conferma, il sistema inserirà nella base dati un nuovo Evento, di tipo Ordine Esecuzione, se ordinanza Eseguita da Procura,

e di tipo Provvedimento, se eseguita da Sorveglianza,

e presenterà la form di Dettaglio

Figura 11: Pagina Dettaglio Ammissione/Applicazione Detenzione Domiciliare

dalla quale è possibile selezionare l’azione di Modifica, di Stampa o di Validazione.
Selezionando l’azione di Modifica  , il sistema presenterà la form

Figura 12: Pagina Modifica Ammissione/Applicazione Detenzione Domiciliare

da cui è possibile modificare i dati di interesse e Confermare. Il sistema aggiornerà i dati nella base dati e ripresenterà l’azione di Dettaglio aggiornata.
Selezionando l’azione di Stampa  , il sistema genererà uno dei seguenti template:
SIEP_MA_APPLPRO_DETD_LIB_PROC.rtf     in caso di Ordine Esecuzione

SIEP_MA_APPLPRO_AFFI_LIB_MDS.rtf      in caso di Provvedimento
Successivamente alla stampa dell’Ordine Esecuzione o del Provvedimento, sarà possibile procedere alla Validazione dello stesso, che lo renderà non modificabile e aggiornerà lo stato procedimento e l’ultimo Evento come di seguito riportato, nei riquadri in grigio, nelle successive form di Dettaglio Procedimento

Figura 13: Pagina Dettaglio Procedimento a seguito Appl.Provv. Detenzione Domiciliare (Esegue PM)


Figura 14: Pagina Dettaglio Procedimento a seguito Appl.Provv. Detenzione Domiciliare (Esegue Sorv)

In caso di inserimento dell’Ordine di Esecuzione ….., alla ricezione del verbale, l’ufficio dovrà provvedere all’annotazione dello stesso utilizzando la funzione di Registrazione Data Inizio Misura con il conseguente inserimento della Ordine Scarcerazione Applicazione Provvisoria ad Affidamento al Servizio Sociale.


## 3.3	Funzione ‘Ammissione/Applicazione Provvisoria’ per SEMILIBERTA’ (nuova)

Nella pagina dei menù relativa alla Semilibertà è stato aggiunto un nuovo tasto dedicato alla gestione dell’Ammissione Provvisoria a Semilibertà (Art. 50 co. 6 O.P. ) e all’ Applicazione Provvisoria per la misura di Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.).

Figura 15: Menu Decisioni Sorveglianza/Semiliberta (PM e PMM)

Tramite l’accesso alla funzione, il sistema mostra la form per permettere all’utente di registrare l’ordinanza di relativa alla Semilibertà e con esito ‘ ammette provvisoriamente’ o ‘applica provvisoriamente’.





Figura 16: Pagina Inserimento Ammissione/Applicazione Provvisoria SEMILIBERTA'

Nella prima sezione devono essere riepilogati i dati del procedimento di classe I cui fa riferimento la decisione della Sorveglianza.
A seguire, va prevista la sezione dei dati del Provvedimento della Sorveglianza:
Anno/Numero SIUS
Anno/Numero del provvedimento
Ufficio Emittente (combo box: TDS, UDS, TDSM, UDSM)
Sede Emittente
Tipologia Provvedimento (ordinanza/decreto)
Oggetto Provvedimento (combo box)
Data emissione
Data esecutività (obbligatoria solo in caso di Applicazione Provvisoria)
Note
Eseguita Procura/Sorveglianza (Radio button)
Data inizio misura (obbligatoria se Esegue Sorveglianza)

A completamento della pagina occorre prevedere:
Sezione Magistrato Firmatario
Sezione Destinatario dell’Esecuzione
Sezione Destinatario per Notifica

Per gli uffici PM (Procura Ordinaria maggiori), in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema ricerca e visualizza i provvedimenti di ‘Ammissione’ e/o ‘Applicazione Provvisoria’,  e che afferiscono al contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ ed hanno come oggetto associato il codice corrispondente alla ‘Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.)’ .

Per gli uffici PMM (Procura Ordinaria minorenni), in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema ricerca e visualizza i provvedimenti di ‘Ammissione’ e/o ‘Applicazione Provvisoria’,  che afferiscono al contenuto ‘Concessione Misure Penali di Comunita' / Misure Alternative alla Detenzione (art. 2 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.)’ ed hanno come oggetto associato il codice corrispondente alla ‘Semiliberta' (art.7 d.lgs. 121/2018, art. 678 comma 1 ter cp.p.)’ .
Per quanto riguarda invece il campo ‘Oggetto Provvedimento’, nella combo box corrispondente devono essere riportati i seguente valori
per PM
per PMM
I dati da impostare nella sezione ‘Provvedimenti della Sorveglianza’, possono essere recuperati in automatico dal link su descritto, ma possono essere inseriti anche manualmente da parte dell’utente. Infatti i campi di tale sezione sono tutti editabili.

In fase di conferma, il sistema verifical’obbligatorietà dei seguenti campi:

Ufficio Emittente
Sede Emittente
Tipologia Provvedimento (ordinanza/decreto)
Oggetto Decisione (Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.))
Inserimento di almeno un Destinatario

Dopo aver compilato i restanti campi della form, indicando se l’ordinanza viene eseguita dalla Procura o se è stata già eseguita dalla Sorveglianza, l’utente conferma. A seguito della Conferma, il sistema inserirà nella base dati un nuovo Evento, la cui Tipologia dipenderà, come riportato nella seguente tabella (in azzurro), dalle posizione giuridica del condannato, dall’oggetto e dall’autorità, che esegue/ha eseguito il provvedimento della Sorveglianza, selezionate nella form

| Oggetto | Posizione Giur. | Esegue Procura o Sorveglianza | Tipo Evento | Template |
| --- | --- | --- | --- | --- |
| Applicazione Provvisoria | qualsiasi | PROCURA | Comunicazione | SIEP_MA_APPLPRO_SEML_LIB_PROC.rtf |
| Applicazione Provvisoria | qualsiasi | SORVEGLIANZA | Provvedimento | SIEP_MA_APPLPRO_SEML_LIB_MDS.rtf |
| Ammissione Provvisoria | Libero | PROCURA | Ordine Esecuzione | SIEP_MA_SEMLPROVV_LIB.rtf |
| Ammissione Provvisoria | Libero | PROCURA | Provvedimento | SIEP_MA_SEMLPROVV_LIB.rtf |
| Ammissione Provvisoria | Detenuto e assimilati | PROCURA | Comunicazione | SIEP_MA_SEMLPROVV_DET.rtf |
| Ammissione Provvisoria | Detenuto e assimilati | SORVEGLIANZA | Provvedimento | SIEP_MA_SEMLPROVV_DET.rtf |
| Ammissione Provvisoria | Arresti domiciliari e assimilati | PROCURA | Ordine Esecuzione | SIEP_MA_SEMLPROVV_ARRD.RTF |
| Ammissione Provvisoria | Arresti domiciliari e assimilati | SORVEGLIANZA | Provvedimento | SIEP_MA_SEMLPROVV_ARRD.RTF |


e presenterà la form di Dettaglio


Figura 17: Pagina Dettaglio Ammissione/Applicazione Provvisoria SEMILIBERTA'

dalla quale è possibile selezionare l’azione di Modifica, di Stampa o di Validazione.
Selezionando l’azione di Modifica  , il sistema presenterà la form

Figura 18: Pagina Modifica Ammissione/Applicazione Provvisoria SEMILIBERTA'

da cui è possibile modificare i dati di interesse e Confermare. Il sistema aggiornerà i dati nella base dati e ripresenterà l’azione di Dettaglio aggiornata.
Selezionando l’azione di Stampa  , il sistema genererà uno dei template riportati nella precedente tabella.
Successivamente alla stampa, sarà possibile procedere alla Validazione del provvedimento generato, che lo renderà non modificabile e aggiornerà lo stato procedimento e l’ultimo Evento come di seguito riportato, nei riquadri in grigio, nelle successive form di Dettaglio Procedimento

Figura 19: Pagina Dettaglio Procedimento a seguito Appl. Provv. SEMILIBERTA' (Esegue PM)


Figura 20: Pagina Dettaglio Procedimento a seguito Appl. Provv. SEMILIBERTA' (Esegue Sorv)

Figura 21: Pagina Dettaglio Procedimento a seguito Ammissione Provvisoria SEMILIBERTA' (Esegue PM)

Il tasto di ‘upload’ ,invece, permette la validazione diretta del provvedimento.

## 3.4	Funzione ‘Applicazione Provvisoria per Sospensione Esecuzione Pena’ (nuova)
L’attuale funzione, presente nel menu Decisioni Sorveglianza è stata rivista completamente


cliccando sul relativo tasto, il sistema presenta un nuovo menu
Figura 22: Menu Decisioni Sorveglianza/Sospensione Esecuzione Pena

in cui la precedente funzione di Concessione è stata rinominata Concessione/Ratifica per gestire oltre ai precedenti provvedimenti di Concessione, anche i nuovi provvedimenti di Conferma dell’applicazione provvisoria della Sospensione. E’ poi presente la nuova funzione di Applicazione Provvisoria della Sospensione.
Selezionandola, il sistema presenta la seguente form

Figura 23: Pagina Inserimento Applicazione Provvisoria Sospensione Esecuzione della Pena

Nella prima sezione sono riepilogati i dati del procedimento di classe I cui fa riferimento la decisione della Sorveglianza.
A seguire, va prevista la sezione dei dati del Provvedimento della Sorveglianza:
Anno/Numero SIUS
Anno/Numero del provvedimento (ordinanza del TDS/TDSM)
Tipo Provvedimento (ordinanza/decreto)
Autorità Emittente (combo box: TDS, UDS, TDSM, UDSM)
Sede Autorità Emittente
Oggetto Provvedimento

Data emissione provvedimento
Motivazioni
Data Sospensione Esecuzione
Radio Button per indicare se condannato è


A completamento della pagina occorre prevedere:
Sezione Magistrato Firmatario
Sezione Destinatari

Per gli uffici PM (Procura Ordinaria maggiorenni), in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare le ordinanze con esito ‘Applica Provvisoriamente’ e che afferiscono al contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ ed hanno come oggetto associato il codice corrispondente alla ‘Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.)’ .
Per gli uffici PMM (Procura Ordinaria minorenni), in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare le ordinanze con esito ‘Applica Provvisoriamente’, e che afferiscono al contenuto ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 2 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.)’ ed hanno come oggetto associato il codice corrispondente alla ‘Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.)’. Selezionando il suddetto link, il sistema apre una popup del tipo

da cui, cliccando sull’icona , relativa al provvedimento di interesse, i dati saranno riportati nella form principale.
I dati da impostare nella sezione ‘Provvedimenti della Sorveglianza’, possono essere recuperati in automatico dal link su descritto, ma possono essere inseriti anche manualmente da parte dell’utente, pertanto i campi di tale sezione sono tutti editabili.
In fase di conferma, il sistema deve verificare l’obbligatorietà dei seguenti campi:

Autorità Emittente
Sede Autorità Emittente
Tipologia Provvedimento (ordinanza/decreto)
Oggetto Provvedimento
Data Emissione
Data Sospensione Esecuzione
Selezione di almeno un destinatario
A seguito del salvataggio deve essere prevista una pagina di dettaglio, attenendosi allo stesso layout delle pagine di dettaglio generate in fase di conferma dell’inserimento dell’ammissione provvisoria di altre tipologie di misure.
Dopo aver compilato i restanti campi della form, indicando se il condannato è da scarcerare o è Libero per avvenuta scarcerazione l’utente conferma. A seguito della Conferma, il sistema inserirà nella base dati un nuovo Evento, di tipo Ordine di scarcerazione, se Eseguita da Procura,

e di tipo Comunicazione, se già eseguita da Sorveglianza,

e presenterà la form di Dettaglio

Figura 24: Pagina Dettaglio Applicazione Provvisoria Sospensione Esecuzione della Pena

dalla quale è possibile selezionare l’azione di Modifica, di Stampa o di Validazione.
Selezionando l’azione di Modifica  , il sistema presenterà la form
Figura 25: Pagina Modifica Applicazione Provvisoria Sospensione Esecuzione della Pena

da cui è possibile modificare i dati di interesse e Confermare. Il sistema aggiornerà i dati nella base dati e ripresenterà l’azione di Dettaglio aggiornata.
Selezionando l’azione di Stampa  , il sistema genererà uno dei seguenti template:
SIEP_MA_APPLPRO_SOSP_LIB_PROC.rtf     in caso di Ordine Scarcerazione

SIEP_MA_APPLPRO_SOSP_LIB_MDS.rtf      in caso di Comunicazioone
Successivamente alla stampa dei suddetti provvedimenti, sarà possibile procedere alla Validazione dello stesso, che lo renderà non modificabile e aggiornerà lo stato procedimento e l’ultimo Evento come di seguito riportato, nei riquadri in grigio, nelle successive form di Dettaglio Procedimento


Figura 26: Pagina Dettaglio Procedimento a seguito Applicazione Provvisoria SEMILIBERTA' (Esegue Sorv)


# Concessione misure alternative (art. 678 comma 1-ter c.p.p.) e Conferma dell’Applicazione Provvisoria misure alternative
Con l’introduzione delle nuove misure alternative (art. 678 comma 1- ter c.p.p.) è sorta l’esigenza di doverli gestire come concessione, se sono gestiti con rito ordinario, o come Conferma dell’Applicazione Provvisoria concessa dal magistrato di Sorveglianza designato.
Si specifica che è possibile incorrere nella casistica del rito ordinario quando, per misura alternativa concessa in relazione all’art. 678 comma 1-ter c.p.p., il magistrato designato non abbia provveduto ad emettere l’ordinanza di ammissione provvisoria nei termini stabiliti, oppure nel caso in cui, il magistrato designato ritenga di non poter applicare alcuna delle misure concedibili rimettendo gli atti al Presidente del Tribunale di Sorveglianza.
Nell’ambito dell’art. 678 comma 1-ter c.p.p., le possibili misure che posso essere concesse dal TDS  sono:
Affidamento in prova al servizio sociale (art. 47 O.P. -  art. 678 comma 1-ter c.p.p.);
Affidamento in prova al servizio sociale (art. 94 DPR 309/90 - art. 678 comma 1-ter c.p.p.);
Detenzione domiciliare (art. 47 ter O.P. - art. 678 comma 1-ter c.p.p.);
Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.);
Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.);
mentre quelle che posso essere concesse dal TDSM  sono:
Affidamento in prova al servizio Sociale  (art.4 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.)
Affidamento in prova in casi particolari  (artt.4 D.lgs. 121/2018 -  94 DPR 309/90, art. 678 comma 1 ter c.p.p.)
Affidamento in prova in prova con detenzione domiciliare (art.5 d.lgs. 121/2018, art. 678 comma 1 ter c.p.p.)
Detenzione domiciliare (art.6 d.lgs. 121/2018 , art. 678 comma 1 ter c.p.p.)
Semilibertà (art.7 d.lgs. 121/2018, art. 678 comma 1 ter c.p.p.)
Sospensione dell’esecuzione della pena detentiva (art. 90 D.P.R. 9 ottobre 1990, n. 309, art. 678 comma 1 ter c.p.p.)

A seguito di emissione di un’ordinanza, sia essa emessa con rito ordinario, che emessa quale ‘conferma’ dell’applicazione provvisoria, il Tribunale di Sorveglianza, dopo aver opportunamente validato e depositato il provvedimento, lo trasmette telematicamente all’ufficio Procura titolare del procedimento SIEP su cui ha provveduto ad iscrivere procedimento SIUS [par. Errore. L'origine riferimento non è stata trovata.];
A questo punto, nell’ambito dei requisiti in oggetto, un primo ‘impatto’ da gestire lato Procura è la ricezione dell’ordinanza/decreto.
## 4.1	Adeguamento delle Funzioni di Concessione misure presenti in Decisioni Sorveglianza
Le attuali funzioni di Concessione relative alla misure alternative, evidenziate con riquadro in rosso, nella form seguente ‘Decisioni Sorveglianza’ sono state oggetto di molteplici interventi. Infatti, al fine di allineare il sistema all’introduzione dell’art. art. 678 comma 1-ter c.p.p.
Gli interventi specificati si intendono realizzati nell’ambito degli uffici PM (Procura Ordinaria maggiorenni) e PMM (Procura Ordinaria minorenni).

Nell’immagine che segue ne sono evidenziati i punti:

Un primo intervento è stata la modifica della Label del tasto funzione di ‘Concessione’ in “Concessione/Ratifica”. Questo intervento è stato applicato ad ogni tipologia di misura evidenziata nella precedente figura [Errore. L'origine riferimento non è stata trovata.].

## 4.2	Adeguamento della funzione Concessione Affidamento in Prova al Servizio Sociale
Per il menù ‘Affidamento in Prova al Servizio Sociale’, l’attuale tasto funzione ‘Concessione’ è stato rinominato in ‘Concessione/Ratifica' della misura, inoltre la form attuale è stata modificata per permettere la gestione dei provvedimenti del Tribunale di Sorveglianza che ‘concedono’ oppure che ‘ratificano’ la misura alternativa ‘Affidamento in prova al servizio sociale (art. 47 O.P. -  art. 678 comma 1-ter c.p.p.)’.


Figura 27: Menu Decisioni Sorveglianza/Affidamento in Prova (PM e PMM)

I provvedimenti che sono gestiti, in aggiunta a quelli attualmente previsti in questa sezione, hanno le seguenti peculiarità:

Fanno riferimento ad un procedimento SIUS con contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ per gli uffici TDS, oppure con contenuto ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 2 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.) ’ per gli uffici TDSM.
Sono caratterizzati dall’esito “Concede” oppure dall’esito “Conferma Decisione del Magistrato Relatore”;

Nell’attuale form sono stati aggiunti nuovi campi (evidenziati in riquadri in rosso) per l’annotazione degli estremi dell’ordinanza di applicazione provvisoria, che però devono essere valorizzati solo in caso di Conferma dell’Applicazione Provvisoria

Figura 28: Pagina Concessione/Ratifica Affidamento in Prova


Nello specifico, per gli uffici PM (Procura Ordinaria maggiorenni), in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare, oltre alle ordinanze di Concessione Misure Alternative, anche le ordinanze con esito ‘Conferma Decisione del Magistrato Relatore’ e che afferiscono al nuovo contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ ed il cui oggetto sia uno dei seguenti:
Conferma appl. provv. Affidamento in Prova al S.S. (Art. 47 O.P. -  Art. 678 comma 1-ter c.p.p.)
Conferma appl. provv. Affidamento in Prova al S.S. (Art. 94 DPR 309/90 - Art. 678 comma 1-ter c.p.p.)

Invece, per gli uffici PMM (Procura Ordinaria minorenni), in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare le ordinanze/decreti con esito ‘Concede’ oppure con esito ‘Conferma Decisione del Magistrato Relatore’ e che afferiscono al nuovo contenuto ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 2 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.)’ ed il cui oggetto sia uno dei seguenti:
Conferma appl. provv. Affidamento in Prova al S.S. (art. 4 D.lgs. 121/2018, art. 678 comma 1 ter cp.p.)
Conferma appl. provv. Affidamento in Prova in casi particolari (artt. 4 D.lgs. 121/2018 -  94 DPR 309/90, art. 678 comma 1 ter cp.p.)
Conferma appl. provv. Affidamento in prova con detenzione domiciliare (art. 5 d.lgs. 121/2018, art. 678 comma 1 ter cp.p.)
Per le ordinanze con esito ‘Conferma Decisione del Magistrato Relatore’ nella pagina di pop-up che si apre dal link su menzionato, vengono visualizzati anche l’anno e numero dell’ordinanza provvisoria.

Per quanto riguarda invece il campo ‘Oggetto Provvedimento’, nella combo box corrispondente devono essere previsti i corrispondenti oggetti introdotti su Sorveglianza in associazione ai contenuti su specificati.
Pertanto la combo box Oggetto Provvedimento presenterà i seguenti valori:

in caso di Procura



In caso di Procura Minori



In caso di selezione dalla lista di un’ordinanza di Conferma, completa dei dati dell’ordinanza di applicazione provvisoria e data esecutività, tutti i campi della form relativi al provvedimento della Sorveglianza si autocompileranno.
Nel caso che l’Ufficio di Procura non ha eseguito l’ordinanza di Applicazione Provvisoria, quindi sul procedimento SIEP non è presente la data di inizio misura, l’utente dovrà compilare manualmente il campo Data Inizio Misura.
In caso di Inserimento di un’ordinanza di Ratifica, come di seguito

A seguito della Conferma il sistema inserirà una Comunicazione


e presenterà la pagina di dettaglio con tutti i dati del provvedimento, in particolare la ‘nuova’ descrizione dell’oggetto dell’ordinanza selezionata e gli estremi (anno/numero) dell’ordinanza provvisoria.

Figura 29: Pagina Dettaglio Concessione/Ratifica Affidamento in Prova


dalla quale è possibile selezionare l’azione di Modifica, di Stampa o di Validazione.
Selezionando l’azione di Modifica  , il sistema presenterà la form
Figura 30: Pagina Modifica Concessione/Ratifica Affidamento in Prova

da cui è possibile modificare i dati di interesse e Confermare. Il sistema aggiornerà i dati nella base dati e ripresenterà l’azione di Dettaglio aggiornata.
Selezionando l’azione di Stampa  , il sistema genererà il template SIEP_MA_AFFI_RATIFICA.rtf.
Successivamente alla stampa della Comunicazione, sarà possibile procedere alla Validazione dello stesso, che lo renderà non modificabile e aggiornerà lo stato procedimento, la posizione giuridica  e l’ultimo Evento come di seguito riportato, nei riquadri in grigio, nelle successive form di Dettaglio Procedimento
Figura 31: Pagina Dettaglio Procedimento a seguito Ratifica Affidamento in Prova


La form di emissione della concessione dell’affidamento al servizio sociale, attualmente prevede l’inserimento manuale del provvedimento e tale comportamento è stato confermato, pertanto tutti i campi della sezione ‘Dati Tribunale della Sorveglianza ‘ sono editabili.
In caso di Concessione, seguendo il rito ordinario, di una delle nuove misure il flusso operativo rimane quello attualmente previsto per la concessione delle misure preesistenti. Si riporta di seguito un esempio per un procedimento con condannato Detenuto
Figura 32: Pagina Inserimento Concessione Affidamento in Prova

A seguito della Conferma il sistema inserisce un ordine scarcerazione e presenta la form di Dettaglio
Figura 33: Pagina Dettaglio Concessione Affidamento in Prova

Da cui selezionando l’azione di stampa il sistema genererà il template Siep-ma-affi-os.rtf. Dopo aver proceduto alla validazione del provvedimento, il Dettaglio del procedimento SIEP si presenta come di seguito

Figura 34: Pagina Dettaglio Procedimento a seguito Concessione Affidamento in Prova


## 4.3	Adeguamento della funzione Concessione Detenzione Domiciliare
La Detenzione domiciliare (art. 47 ter O.P. - art. 678 comma 1-ter c.p.p.), è un’ulteriore misura alternativa prevista dall’art. 656 comma 5, che può essere concessa in relazione all’ art. 678 comma 1-ter c.p.p. introdotto dal D.lgs. 123/2018.
Anche per questa tipologia di misura occorre intervenire affinché il sistema SIEP possa recepire l’ordinanza emessa dal Tribunale di Sorveglianza che concede/ratifica la misura.
A tale scopo l’attuale tasto funzione di ‘Concessione’ relativa al menù’ ‘Detenzione Domiciliare’ sarà rinominato in ‘Concessione/Ratifica’
Figura 35: Menu Decisioni Sorveglianza/Detenzione Domiciliare

I provvedimenti che sono gestiti, in aggiunta a quelli attualmente previsti in questa sezione, hanno le seguenti peculiarità:

Fanno riferimento ad un procedimento SIUS con contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ ed oggetto ‘Detenzione Domiciliare (Art. 47 ter O.P. - Art. 678 comma 1-ter c.p.p.)’ per gli uffici TDS, oppure con contenuto ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 2 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.) ’ ed oggetto ‘Detenzione domiciliare (art. 6 d.lgs. 121/2018 , art. 678 comma 1 ter cp.p.)’ per gli uffici TDSM.
Sono caratterizzati dall’esito “Concede” oppure dall’esito “Conferma Decisione del Magistrato Relatore”;

Nell’attuale form sono stati aggiunti nuovi campi (evidenziati in riquadri in rosso) per l’annotazione degli estremi dell’ordinanza di applicazione provvisoria, che però devono essere valorizzati solo in caso di Conferma dell’Applicazione Provvisoria



Figura 36: Pagina Inserimento Concessione/Ratifica Detenzione Domiciliare

Nello specifico, per gli uffici PM (Procura Ordinaria maggiorenni), in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare, oltre alle ordinanze di Concessione Misure Alternative, anche le ordinanze con esito ‘Conferma Decisione del Magistrato Relatore’ e che afferiscono al nuovo contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ ed il cui oggetto sia ‘Conferma appl. provv. Detenzione Domiciliare (Art. 47 ter O.P. - Art. 678 comma 1-ter c.p.p.)’.
Invece, per gli uffici PMM (Procura Ordinaria minorenni), in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare le ordinanze con esito ‘Concede’ oppure con esito ‘Conferma Decisione del Magistrato Relatore’ e che afferiscono al nuovo contenuto ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 2 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.)’ ed il cui oggetto sia ‘Conferma appl. provv. Detenzione Domiciliare (art. 6 d.lgs. 121/2018 , art. 678 comma 1 ter cp.p.)’.
Per le ordinanze con esito ‘Conferma Decisione del Magistrato Relatore’ nella pagina di pop-up che si apre dal link su menzionato, vengono visualizzati anche l’anno e numero dell’ordinanza provvisoria.

Per quanto riguarda invece il campo ‘Oggetto Provvedimento’, nella combo box corrispondente devono essere previsti i corrispondenti oggetti introdotti su Sorveglianza in associazione ai contenuti su specificati.
Pertanto la combo box Oggetto Provvedimento presenterà i seguenti valori:

in caso di Procura




In caso di Procura Minori



In caso di selezione dalla lista di un’ordinanza di Conferma, completa dei dati dell’ordinanza di applicazione provvisoria e data esecutività, tutti i campi della form relativi al provvedimento della Sorveglianza si autocompileranno.
Nel caso che l’Ufficio di Procura non ha eseguito l’ordinanza di Applicazione Provvisoria, quindi sul procedimento SIEP non è presente la data di inizio misura, l’utente dovrà compilare manualmente il campo Data Inizio Misura.
In caso di Inserimento di un’ordinanza di Ratifica, come di seguito

A seguito della Conferma il sistema inserirà una Comunicazione


e presenterà la pagina di dettaglio con tutti i dati del provvedimento, in particolare la ‘nuova’ descrizione dell’oggetto dell’ordinanza selezionata e gli estremi (anno/numero) dell’ordinanza provvisoria.

Figura 37: Pagina Dettaglio Concessione/Ratifica Detenzione Domiciliare

dalla quale è possibile selezionare l’azione di Modifica, di Stampa o di Validazione.
Selezionando l’azione di Modifica  , il sistema presenterà la form
Figura 38: Pagina Modifica Concessione/Ratifica Detenzione Domiciliare

da cui è possibile modificare i dati di interesse e Confermare. Il sistema aggiornerà i dati nella base dati e ripresenterà l’azione di Dettaglio aggiornata.
Selezionando l’azione di Stampa  , il sistema genererà il template SIEP_MA_DETD_RATIFICA.rtf.
Successivamente alla stampa della Comunicazione, sarà possibile procedere alla Validazione dello stesso, che lo renderà non modificabile e aggiornerà lo stato procedimento, la posizione giuridica  e l’ultimo Evento come di seguito riportato, nei riquadri in grigio, nelle successive form di Dettaglio Procedimento
Figura 39: Pagina Dettaglio Procedimento a seguito Ratifica Detenzione Domiciliare

La form di emissione della concessione della Detenzione Domiciliare, attualmente prevede l’inserimento manuale del provvedimento e tale comportamento è stato confermato, pertanto tutti i campi della sezione ‘Dati Tribunale della Sorveglianza ‘ sono editabili.
In caso di Concessione, seguendo il rito ordinario, di una delle nuove misure il flusso operativo rimane quello attualmente previsto per la concessione delle misure preesistenti. Si riporta di seguito un esempio per un procedimento con condannato Detenuto
Figura 40: Pagina Inserimento Concessione Detenzione Domiciliare


A seguito della Conferma il sistema inserisce un ordine di esecuzione e presenta la form di Dettaglio
Figura 41: Pagina Dettaglio Concessione Detenzione Domiciliare

Da cui selezionando l’azione di stampa il sistema genererà il template SIEP_MA_DETD_LIB.rtf. Dopo aver proceduto alla validazione del provvedimento, il Dettaglio del procedimento SIEP si presenta come di seguito

Figura 42: Pagina Dettaglio Concessione Detenzione Domiciliare

## 4.4	Adeguamento della funzione Concessione Semilibertà
La Semiliberta' (Art. 50 comma 1 O.P. - Art. 678 comma 1-ter c.p.p.) è un’ulteriore misura alternativa, che può essere concessa in relazione all’ art. 678 comma 1-ter c.p.p. introdotto dal D.lgs. 123/2018.
Anche per questa tipologia di misura occorre intervenire affinché il sistema SIEP possa recepire l’ordinanza emessa dal Tribunale di Sorveglianza che concede/ratifica la misura.
A tale scopo l’attuale tasto funzione di ‘Concessione’ relativa al menù’ ‘Semilibertà’ sarà rinominato in ‘Concessione/Ratifica’

Figura 43: Menu Decisioni Sorveglianza/Semilibertà

I provvedimenti che sono gestiti, in aggiunta a quelli attualmente previsti in questa sezione, hanno le seguenti peculiarità:

Fanno riferimento ad un procedimento SIUS con contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ ed oggetto ‘Semiliberta' (Art. 50 comma 1 O.P. - Art. 678 comma 1-ter c.p.p.)’ per gli uffici TDS, oppure con contenuto ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 2 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.) ’ ed oggetto ‘Semiliberta' (art. 7 d.lgs. 121/2018, art. 678 comma 1 ter cp.p.)’ per gli uffici TDSM.
Sono caratterizzati dall’esito “Concede” oppure dall’esito “Conferma Decisione del Magistrato Relatore”;

Nell’attuale form sono stati aggiunti nuovi campi (evidenziati in riquadri in rosso) per l’annotazione degli estremi dell’ordinanza di applicazione provvisoria, che però devono essere valorizzati solo in caso di Conferma dell’Applicazione Provvisoria



Figura 44: Pagina di Concessione/Ratifica Semilibertà

Nello specifico, per gli uffici PM (Procura Ordinaria maggiorenni), in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare, oltre alle ordinanze di Concessione Misure Alternative, anche le ordinanze con esito ‘Conferma Decisione del Magistrato Relatore’ e che afferiscono al nuovo contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ ed il cui oggetto sia ‘Conferma appl. provv. Semiliberta' (Art. 50 comma 1 O.P. - Art. 678 comma 1-ter c.p.p.)’.
Invece, per gli uffici PMM (Procura Ordinaria minorenni), in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare le ordinanze con esito ‘Concede’ oppure con esito ‘Conferma Decisione del Magistrato Relatore’ e che afferiscono al nuovo contenuto ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 2 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.)’ ed il cui oggetto sia ‘Conferma appl. provv. Semiliberta' (art. 7 d.lgs. 121/2018, art. 678 comma 1 ter cp.p.)’.
Per le ordinanze con esito ‘Conferma Decisione del Magistrato Relatore’ nella pagina di pop-up che si apre dal link su menzionato, vengono visualizzati anche l’anno e numero dell’ordinanza provvisoria.

Per quanto riguarda invece il campo ‘Oggetto Provvedimento’, nella combo box corrispondente devono essere previsti i corrispondenti oggetti introdotti su Sorveglianza in associazione ai contenuti su specificati.
Pertanto la combo box Oggetto Provvedimento presenterà i seguenti valori:

in caso di Procura



In caso di Procura Minori



In caso di selezione dalla lista di un’ordinanza di Conferma, completa dei dati dell’ordinanza di applicazione provvisoria e data esecutività, tutti i campi della form relativi al provvedimento della Sorveglianza si autocompileranno.
Nel caso che l’Ufficio di Procura non ha eseguito l’ordinanza di Applicazione Provvisoria, quindi sul procedimento SIEP non è presente la data di inizio misura, l’utente dovrà compilare manualmente il campo Data Inizio Misura.
In caso di Inserimento di un’ordinanza di Ratifica, come di seguito

A seguito della Conferma il sistema inserirà una Comunicazione


e presenterà la pagina di dettaglio con tutti i dati del provvedimento, in particolare la ‘nuova’ descrizione dell’oggetto dell’ordinanza selezionata e gli estremi (anno/numero) dell’ordinanza provvisoria.
Figura 45: Pagina Dettaglio Concessione/Ratifica Semilibertà


dalla quale è possibile selezionare l’azione di Modifica, di Stampa o di Validazione.
Selezionando l’azione di Modifica  , il sistema presenterà la form
Figura 46: Pagina Modifica Concessione/Ratifica Semilibertà

da cui è possibile modificare i dati di interesse e Confermare. Il sistema aggiornerà i dati nella base dati e ripresenterà l’azione di Dettaglio aggiornata.
Selezionando l’azione di Stampa  , il sistema genererà il template SIEP_MA_SEML_RATIFICA.rtf.
Successivamente alla stampa della Comunicazione, sarà possibile procedere alla Validazione dello stesso, che lo renderà non modificabile e aggiornerà lo stato procedimento, la posizione giuridica  e l’ultimo Evento come di seguito riportato, nei riquadri in grigio, nelle successive form di Dettaglio Procedimento
Figura 47: Pagina Dettaglio Procedimento a seguito Ratifica Semilibertà


La form di emissione della concessione della Semilibertà, attualmente prevede l’inserimento manuale del provvedimento e tale comportamento è stato confermato, pertanto tutti i campi della sezione ‘Dati Tribunale della Sorveglianza ‘ sono editabili.
In caso di Concessione, seguendo il rito ordinario, di una delle nuove misure il flusso operativo rimane quello attualmente previsto per la concessione delle misure preesistenti. Si riporta di seguito un esempio per un procedimento con condannato Detenuto
Figura 48: Pagina Inserimento Concessione/Ratifica Semilibertà (Concessione)

A seguito della Conferma il sistema inserisce un ordine scarcerazione e presenta la form di Dettaglio
Figura 49: Pagina Dettaglio Concessione/Ratifica Semilibertà (Concessione)

Da cui selezionando l’azione di stampa il sistema genererà il template SIEP_MA_SEML_DET.rtf. Dopo aver proceduto alla validazione del provvedimento, il Dettaglio del procedimento SIEP si presenta come di seguito


Figura 50: Pagina Dettaglio Procedimento a seguito Concessione Semilibertà



## 4.5	Adeguamento della funzione Concessione Sospensione Esecuzione Pena
La Sospensione dell'Esecuzione della Pena (Art. 90 DPR 309/90 - Art. 678 comma 1-ter c.p.p.) è un’ulteriore misura alternativa, che può essere concessa in relazione all’ art. 678 comma 1-ter c.p.p. introdotto dal D.lgs. 123/2018.
Anche per questa tipologia di misura occorre intervenire affinché il sistema SIEP possa recepire l’ordinanza emessa dal Tribunale di Sorveglianza che concede/ratifica la misura.
A tale scopo l’attuale tasto funzione di ‘Concessione’ relativa al menù’ ‘Sospensione Esecuzione Pena’ sarà rinominato in ‘Concessione/Ratifica’
Figura 51: Menu Decisioni Sorveglianza/Sospensione Esecuzione Pena

I provvedimenti che sono gestiti, in aggiunta a quelli attualmente previsti in questa sezione, hanno le seguenti peculiarità:

Fanno riferimento ad un procedimento SIUS con contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ ed oggetto ‘Sospensione dell'Esecuzione della Pena (Art. 90 DPR 309/90 - Art. 678 comma 1-ter c.p.p.)’ per gli uffici TDS, oppure con contenuto ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 2 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.) ’ ed oggetto ‘Sospensione dell'Esecuzione della Pena (Art. 90 DPR 309/90 - Art. 678 comma 1-ter c.p.p.)’ per gli uffici TDSM.
Sono caratterizzati dall’esito “Concede” oppure dall’esito “Conferma Decisione del Magistrato Relatore”;

Nell’attuale form sono stati aggiunti nuovi campi (evidenziati in riquadri in rosso) per l’annotazione degli estremi dell’ordinanza di applicazione provvisoria, che però devono essere valorizzati solo in caso di Conferma dell’Applicazione Provvisoria


Figura 52: Pagina Inserimento Concessione/Ratifica Sospensione  Esecuzione Pena

Nello specifico, per gli uffici PM (Procura Ordinaria maggiorenni), in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare, oltre alle ordinanze di Concessione Misure Alternative, anche le ordinanze con esito ‘Conferma Decisione del Magistrato Relatore’ e che afferiscono al nuovo contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ ed il cui oggetto sia ‘Conferma appl. provv. Sospensione dell'Esecuzione della Pena (Art. 90 DPR 309/90 - Art. 678 comma 1-ter c.p.p.)’.
Invece, per gli uffici PMM (Procura Ordinaria minorenni), in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare le ordinanze con esito ‘Concede’ oppure con esito ‘Conferma Decisione del Magistrato Relatore’ e che afferiscono al nuovo contenuto ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 2 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.)’ ed il cui oggetto sia ‘Conferma appl. provv. Sospensione dell'Esecuzione della Pena (Art. 90 DPR 309/90 - Art. 678 comma 1-ter c.p.p.)’.
Per le ordinanze con esito ‘Conferma Decisione del Magistrato Relatore’ nella pagina di pop-up che si apre dal link su menzionato, vengono visualizzati anche l’anno e numero dell’ordinanza provvisoria.

Per quanto riguarda invece il campo ‘Oggetto Provvedimento’, nella combo box corrispondente devono essere previsti i corrispondenti oggetti introdotti su Sorveglianza in associazione ai contenuti su specificati.
Pertanto la combo box Oggetto Provvedimento presenterà i seguenti valori:

in caso di Procura



In caso di Procura Minori



In caso di selezione dalla lista di un’ordinanza di Conferma, completa dei dati dell’ordinanza di applicazione provvisoria e data esecutività, tutti i campi della form relativi al provvedimento della Sorveglianza si autocompileranno.
Nel caso che l’Ufficio di Procura non ha eseguito l’ordinanza di Applicazione Provvisoria, quindi sul procedimento SIEP non è presente la data di inizio misura, l’utente dovrà compilare manualmente il campo Data Inizio Misura.
In caso di Inserimento di un’ordinanza di Ratifica, come di seguito

A seguito della Conferma il sistema presenterà una ulteriore form per completare il provvedimento da inserire
 Figura 53: Pagina n. 2 Inserimento Concessione/Ratifica Sospensione  Esecuzione Pena



e presenterà la pagina di dettaglio con tutti i dati del provvedimento, in particolare la ‘nuova’ descrizione dell’oggetto dell’ordinanza selezionata e gli estremi (anno/numero) dell’ordinanza provvisoria.
Figura 54: Pagina Dettaglio Concessione/Ratifica Sospensione  Esecuzione Pena


dalla quale è possibile selezionare l’azione di Modifica, di Stampa o di Validazione.
Selezionando l’azione di Modifica  , il sistema presenterà la form
Figura 55: Pagina Modifica Concessione/Ratifica Sospensione  Esecuzione Pena

da cui è possibile modificare i dati di interesse e Confermare. Il sistema aggiornerà i dati nella base dati e ripresenterà l’azione di Dettaglio aggiornata.
Selezionando l’azione di Stampa  , il sistema genererà il template SIEP_MA_SOSP_RATIFICA.rtf.
Successivamente alla stampa della Comunicazione, sarà possibile procedere alla Validazione dello stesso, che lo renderà non modificabile e aggiornerà lo stato procedimento, la posizione giuridica  e l’ultimo Evento come di seguito riportato, nei riquadri in grigio, nelle successive form di Dettaglio Procedimento
Figura 56: Pagina Dettaglio Procedimento a seguito Ratifica Sospensione  Esecuzione Pena


La form di emissione della concessione della Semilibertà, attualmente prevede l’inserimento manuale del provvedimento e tale comportamento è stato confermato, pertanto tutti i campi della sezione ‘Dati Tribunale della Sorveglianza ‘ sono editabili.
In caso di Concessione, seguendo il rito ordinario, di una delle nuove misure il flusso operativo rimane quello attualmente previsto per la concessione delle misure preesistenti. Si riporta di seguito un esempio per un procedimento con condannato Detenuto
Figura 57: Pagina Inserimento Concessione/Ratifica Sospensione  Esecuzione Pena (Concessione)

A seguito della Conferma il sistema presenta la successiva form
Figura 58: Pagina n.2 Inserimento Concessione/Ratifica Sospensione  Esecuzione Pena (Concessione)

e a seguito della Conferma inserisce un ordine scarcerazione e presenta la form di Dettaglio
Figura 59: Pagina Dettaglio Concessione/Ratifica Sospensione  Esecuzione Pena (Concessione)

Da cui selezionando l’azione di stampa il sistema genererà il template SIEP_SOSP_ART9091.rtf. Dopo aver proceduto alla validazione del provvedimento, il Dettaglio del procedimento SIEP si presenta come di seguito


Figura 60: Dettaglio Procedimento a seguito Concessione Sospensione  Esecuzione Pena

# Aggiornamento delle funzioni statistiche Statistica Attività Magistrati e Riepilogo Ispettivo
A seguito degli interventi descritti nei precedenti paragrafisono state aggiornate le attuali funzioni di
‘Statistica Attività Magistrati’ e ‘Riepilogo Ispettivo’.
Nello specifico, per la statistica attività magistrati, nel file excel generato sono state nuove voci attinenti alle Applicazioni Provvisorie delle Misure Alternative e alle Ratifiche delle Misure Alternative.
Gli interventi specificati si intendono da applicare nell’ambito degli uffici PM (Procura Ordinaria maggiorenni) e PMM (Procura Ordinaria minorenni).
In particolare per la Statistica Attività Magistrati sono state aggiunte le voci riportate di seguito nei riquadri contornati in rosso



Figura 61: file Excel per Statistica Attività Magistrati

Nel riepilogo ispettivo è stata aggiornata la combo box dei provvedimenti estratti con  le nuove voci

Figura 62: Pagina di Ricerca Riepilogo Ispettivo

Nel file excel prodotto, sono stati aggiornati il Foglio Riepilogo


Figura 63: file Excel Riepilogo Ispettivo - Foglio Riepilogo

E’ stato aggiornato anche il foglio Dettagli, inserendo le nuove categorie con l’elenco dei relativi procedimenti

Figura 64: file Excel Riepilogo Ispettivo - Foglio Dettagli


Figura 65: file Excel Riepilogo Ispettivo - Foglio Dettagli