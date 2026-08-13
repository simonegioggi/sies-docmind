---
uniqueName: siut-sie-si-1-0-20191218-specifica-intervento-sche
displayName: "SIUT SIE SI 1 0 20191218 Specifica intervento Scheda n 21 SIES Reginde"
category: "GENERAL"
tags: []
---

# SIUT-SIE-SI-1.0-20191218 Specifica intervento Scheda_n.21_SIES_Reginde

> **File originale:** `MEV/SCHEDA_021/Docs/SIUT-SIE-SI-1.0-20191218 Specifica intervento Scheda_n.21_SIES_Reginde.docx`  
> **Tipo:** DOCX

---












Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del sistema informativo unitario telematico, la manutenzione degli attuali sistemi dell’area penale del Ministero della Giustizia e servizi correlati. Lotto 1”


Approvazioni
| Versione | 1.0 del 18/12/2019 |
| --- | --- |
| Redatto da: | Domenico Nania |
| Verificato da | Antonio Pezzilli |
| Approvato da | Paolo Ceccanti |
| Data approvazione | 18/12/2019 |
| Livello di riservatezza | L4 |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Ruolo |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Anna Maria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
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


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 18/12/2019 | Prima Emissione |  |

INDICE DEI CONTENUTI
1.	Introduzione	5
1.1	Scopo del documento	5
1.2	Acronimi e Definizioni	5
1.2.1	Acronimi	5
1.2.2	Definizioni	6
1.3	Riferimenti	6
2	Definizione dell’Obiettivo	7
2.1	Introduzione	7
2.2	Funzionalità	7
3	Architettura del Sistema	8
4	Specifiche dei requisiti	9
4.1	Elenco Requisiti	9
5	Casi d’uso	10
5.1	Tipologie di utenti	10
5.2	Definizione casi d’uso	10
Gestione Difensori su SIES	10
5.2.1	UC-SIE-021-02-01 – Inserimento Difensore	11
5.2.2	UC-SIE-021-03-01 - Ricerca Difensore	14
5.2.3	UC-SIE-021-03-02 – Cancella Difensore	15
5.2.4	UC-SIE-021-03-03 - Modifica Difensore	16
5.2.5	UC-SIE-021-03-04 - Visualizza Difensore	17
5.2.6	UC-SIE-021-01-01 – Ricerca Difensore su REGINDE	18
Associazione Difensori a Fascicoli	22
5.2.7	UC-SIE-021-03-05 – Associa Difensore a Fascicolo SIEP.	22
5.2.8	UC-SIE-021-03-06 – Associa Difensore a Fascicolo SIUS.	24
5.2.9	UC-SIE-021-03-07 – Associa Difensore a Fascicolo SIGE.	26
Bonifica Pregresso	29
5.2.10	UC-SIE-021-04-01 - Batch accorpamento avvocati su SIES	29
5.3	Matrice di tracciabilità	32
6	Dizionario dati	33
6.1	Schema Logico	33
6.2	Schema Fisico	33


Introduzione
## Scopo del documento
Il presente documento riporta le specifiche di intervento sul software, metodologia WATERFALL, al fine di soddisfare i requisiti espressi dall’Amministrazione e descritti nella scheda di intervento SIUT-SIE-SC-1.0-20191108 Scheda intervento Scheda_n.21_SIES_Reginde.
## Acronimi e Definizioni
### Acronimi
| Sigla | Descrizione |
| --- | --- |
| AgID | Agenzia per l’Italia Digitale |
| API | Application Programming Interface |
| CPU | Central Processing Unit |
| CV | Curriculum Vitae |
| DB | Data Base |
| DEC | Direttore Esecutivo Contratto |
| DGSIA | Direzione Generale per o Sistemi Informativi Automatizzati |
| DR | Disaster Recovery |
| ETSI | European Telecommunications Standards Institute |
| FP | Function Point |
| GDPR | General Data Protection Regulation |
| HW | HardWare |
| ICT | Information & Communication Technology |
| ISO | International Organization for Standardization |
| ISP | Information Security Policy |
| IT | Information Technology |
| KPI | Key Performance Indicator |
| MAAC | Mandatory Access Control |
| MAC | MAnutenzione Correttiva |
| MEV | Manutenzione EVolutiva |
| OSWAP | Open Web Application Security Project |
| PA | Pubblica Amministrazione |
| PEC | Posta Elettronica Certificata |
| PDCA | Plan, Do, Check, Act |
| PdQ | Piano della Qualità |
| PdP | Piano di Progetto |
| PdS | Piano della Sicurezza |
| QM | Quality Manager |
| RA | Risk Assessment |
| RID | Riservatezza, Integrità, Disponibilità |
| RM | Resource Manager |
| RPO | Recovery Point Objective |
| RTO | Recovery Time Objective |
| RTI | Raggruppamento Temporaneo di Impresa Engineering – Sirfin-PA |
| RUF | Responsabile Unico Fornitore |
| RUP | Responsabile unico Progetto |
| SGQ | Sistema di Gestione per la Qualità di Engineering Ingegneria Informatica S.p.A. |
| SGSI | Sistema di Gestione della Sicurezza Informatica |
| SICP | Sistema Informativo Cognizione Penale |
| SIU | Sistema Informativo Unitario |
| SLA | Service Level Agreement |
| SM | Security Manager |
| SQL | Structured Query Language |
| SW | SoftWare |
| TT | Trouble Ticketing |
| VPN | Virtual Private Network |

### Definizioni
| Glossa | Sinonimo | Definizione |
| --- | --- | --- |
|  |  |  |


## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| 1.0 | m_dg.DOG07AR.27_09_2019.0000056.U_Nota_ Scheda_n.21_SIES_Regindeocx.docx_signed | Richiesta Scheda di intervento |
| 2.0 | SIUT-SIE-SC-1.0-20191108 Scheda intervento Scheda_n.21_SIES_Reginde.docx | Scheda di intervento |


Definizione dell’Obiettivo
## Introduzione
Nell’ambito del progetto “Servizi di sviluppo e MEV dei siti web e di software ad hoc, di sicurezza e cooperazione applicativa, di Hosting, di gestione applicativa e web del Ministero della Giustizia” ed in particolare relativamente alle attività previste nel PLO contenuto nella scheda di intervento “SIUT-SIE-SC-1.0-20191108 Scheda intervento Scheda_n.21_SIES_Reginde.docx”, si inseriscono gli interventi descritti nel presente documento.
## Funzionalità
Nel sistema SIES è previsto l’inserimento, ricerca e modifica dell’anagrafica di un avvocato da associare ad un fascicolo SIES, SIUS e SIGE. Attualmente il sistema consente l’inserimento di duplicati di avvocati. Questo è dovuto anche al fatto che il codice fiscale non è considerato un campo obbligatorio. Pertanto si rende necessaria la modifica della gestione anagrafica degli avvocati dopo aver opportunamente bonificata la base dati.
Saranno pertanto apportate le opportune modifiche evolutive scaturite dai requisiti condivisi con l’Amministrazione ed elencati di seguito.


Architettura del Sistema
Il presente obiettivo non ha prodotto modifiche all’architettura del sistema.


Specifiche dei requisiti
## Elenco Requisiti
Si riporta di seguito l’elenco dei requisiti da realizzare con una breve descrizione. Per un maggiore approfondimento si rimanda al documento SIUT-SIE-SC-1.0-20191108 Scheda intervento Scheda_n.21_SIES_Reginde.docx.

| Codice | Descrizione | Riferimenti |
| --- | --- | --- |
| REQ-SIE-021-01 | Inserire la funzione di ricerca dell’avvocato sul sistema ReGIndE | N.A. |
| REQ-SIE-021-02 | In caso di indisponibilità del sistema ReGIndE, o di non presenza dell’avvocato su tale sistema, prevedere l’inserimento manuale dell’anagrafica dell’avvocato sul SIES, introducendo sia l’obbligatorietà del codice fiscale sia gli opportuni controlli per evitare duplicati | N.A. |
| REQ-SIE-021-03 | Modificare l’attuale comportamento del sistema per la gestione degli avvocati in modo da evitare la duplicazione delle anagrafiche nella tabella AVVOCATO. | N.A. |
| REQ-SIE-021-04 | Valutare la bonifica del pregresso (riconciliazione dei duplicati, bonifica solo dei dati anagrafici, ecc.). | N.A. |


Casi d’uso
## Tipologie di utenti
Il sistema SIES contiene tre moduli che dipendono dall’utenza con cui si accede:

SIGE (Sistema Informativo Giudice dell’Esecuzione)
SIUS (Sistema Informativo Ufficio di Sorveglianza)
SIEP (Sistema Informativo Esecuzione Penale)
I casi d’uso sono in funzione del profilo assegnato all’utente; la profilazione utente non è stata oggetto di intervento software.
Di seguito le tipologie di utenti coinvolte per i rispettivi moduli di cui si compone il SIES:

| Utenti | Descrizione |
| --- | --- |
| Superutente per il tribunale di sorveglianza/per ufficio giudice esecuzione/ ufficio di sorveglianza/ per l’esecuzione | L’utente può visualizzare, inserire, modificare, cancellare i dati del modulo di competenza |
| Lettura per l’esecuzione/ per il tribunale di sorveglianza/ per ufficio giudice esecuzione/ | L’utente può visualizzare il dato del modulo di competenza |
| Lettura - Scrittura per l’esecuzione/ per il tribunale di sorveglianza/ per l’ufficio di sorveglianza/ per ufficio giudice esecuzione/ | L’utente può inserire e visualizzare i dati del modulo di competenza |
| Lettura – Scrittura – Modifica per l’esecuzione/ per il tribunale di sorveglianza/ per l’ufficio di sorveglianza/ per ufficio giudice esecuzione | L’utente può inserire modificare e visualizzare i dati del modulo di competenza |


## Definizione casi d’uso
Gestione Difensori su SIES
Attualmente la gestione dell’anagrafica degli avvocati su SIES ha consentito il proliferare di occorrenze relative ad uno stesso soggetto. Con il presente intervento si vuole evitare ciò rendendo obbligatorio il codice fiscale in modo da rendere univoca l’occorrenza relativa ad una stessa persona. Poiché il codice fiscale non sempre è noto, la gestione dell’anagrafica degli avvocati su SIES avverrà tramite l’utilizzo di un servizio Web che consentirà di recuperare i dati dell’avvocato dal sistema ReGIndE (Registro Generale degli Indirizzi Elettronici). E’ previsto l’adeguamento alle nuove funzionalità dell’Help On Line.

| Casi d’uso | Descrizione |
| --- | --- |
| UC-SIE-021-01-01 – Ricerca Difensore su REGINDE | La funzionalità si occupa della ricerca dell’anagrafica di un difensore su ReGIndE |
| UC-SIE-021-02-01 – Inserimento Difensore | La funzionalità si occupa dell’inserimento di un’anagrafica di un difensore |
| UC-SIE-021-03-01 - Ricerca Difensore | La funzionalità si occupa della ricerca di un’anagrafica di un difensore |
| UC-SIE-021-03-02 – Cancella Difensore | La funzionalità si occupa della cancellazione di un’anagrafica di un difensore |
| UC-SIE-021-03-03 - Modifica Difensore | La funzionalità si occupa della modifica di un’anagrafica di un difensore |
| UC-SIE-021-03-04 - Visualizza Difensore | La funzionalità si occupa della visualizzazione di un’anagrafica di un difensore |


Ogni modulo indicato nel paragrafo 3.1 fa riferimento a proprie query oracle e class action java. I casi d’uso descritti di seguito, se non diversamente indicato, si riferiscono a tutti i moduli. Inoltre è previsto il rilascio di uno script oracle propedeutico all’utilizzo delle nuove funzionalità oggetto del presente intervento software.
### UC-SIE-021-02-01 – Inserimento Difensore
La funzionalità viene attivata da Funzioni Amministrative/Gestione Difensori/Inserimento in tutti i moduli di cui SIES è composto.
Viene visualizzata una pagina in cui sono obbligatori i seguenti campi:
Cognome (campo di output)
Nome (campo di output)
Foro (campo di input)
Codice Fiscale (campo di output).
Nella parte superiore della pagina è presente il link con la quale attivare una pop-up di ricerca su ReGIndE per prelevare i dati obbligatori della pagina; la ricerca su ReGIndE avviene tramite Plugin ed è trattata dal caso d’uso UC-SIE-021-01-01 - Ricerca Difensore su Reginde.

L’entità interessata è AVVOCATO. Poiché è prioritaria la ricerca del dato su ReGIndE, alla selezione del pulsante “Conferma”, il sistema verifica se il flag del campo presente nella pagina Dati REGINDE sia valorizzato; il suddetto controllo non viene effettuato solo se il servizio WEB verso ReGIndE è momentaneamente non disponibile. Si possono presentare le due casistiche seguenti:

Flag Dati ReGInDe non valorizzato: il sistema prospetta il messaggio bloccante “Ricercare l’avvocato su ReGInDe tramite l’apposito link”. Il caso d’uso termina.

Flag Dati ReGInDe valorizzato: il sistema effettua i consueti controlli di congruenza ed obbligatorietà sui campi presenti nella pagina; infine verifica, tramite il CODICE_FISCALE, l’univocità dell’occorrenza da inserire in base dati. Se il Codice Fiscale è già presente il sistema prospetta il messaggio bloccante: “L’avvocato risulta già registrato per il Foro indicato”. Il caso d’uso termina.
Viene pertanto impedita l’attuale gestione presente nel SIEP dove se si cerca di inserire un’ anagrafica avvocato (Nome e Cognome) già presente per l’ufficio, il sistema avverte ma poi non impedisce l’inserimento.
Se invece il controllo ha verificato l’assenza dell’occorrenza nell’entità AVVOCATO il sistema inserisce i campi della pagina secondo le seguenti regole:
ID_AVVOCATO = sequence
COGNOME = dato proveniente da REGINDE o di input obbligatorio
NOME = dato proveniente da REGINDE o di input obbligatorio
FORO = dato di input obbligatorio
INDIRIZZO = dato di input facoltativo
TELEFONO = dato di input facoltativo
FAX = dato di input facoltativo
E_MAIL = dato proveniente da REGINDE o di input
COD_COMUNE_RESIDENZA = ricavato dall’entità COMUNE tramite la descrizione selezionata nella pagina dalla pop-up dei comuni.
COD_LUOGO_NASCITA = ricavato dall’entità COMUNE tramite la descrizione selezionata nella pagina dalla pop-up dei comuni.
DATA_NASCITA = dato proveniente da REGINDE o di input
FLAG_CANCELLATO = valorizzato con ‘N’
COD_UFFICIO_APPARTENENZA = posto uguale al codice dell’ufficio che sta eseguendo l’inserimento
COD_OPERATORE_INSERIMENTO = posto uguale al codice utente con cui è avvenuto l’accesso
DATA_INSERIMENTO = data di sistema
COD_UFFICIO_INSERIMENTO = posto uguale al codice dell’ufficio che sta eseguendo l’inserimento
COD_FISCALE = dato proveniente da REGINDE o di input
PROVINCIA = ricavato dall’entità COMUNE tramite il comune di residenza
CAP = ricavato dall’entità COMUNE tramite il comune di residenza
FLAG_VISUALIZZA = valorizzato con ‘1’
FLAG_REGINDE =valorizzato con ‘S’.
Per le altre entità coinvolte nell’inserimento queste saranno trattate con le stesse modalità ante intervento.
Ad inserimento effettuato viene prospettata la pagina di visualizzazione dettaglio descritta dal caso d’uso
UC-SIE-021-03-04 – Visualizza Difensore.
### UC-SIE-021-03-01 - Ricerca Difensore
La funzionalità di ricerca viene attivata da Funzioni Amministrative/Gestione Difensori/Ricerca in tutti i moduli di cui SIES è composto.
La funzione di ricerca, pur contenendo gli stessi controlli di quella attuale, sarà implementata con l’aggiunta del campo CODICE FISCALE. Di seguito la pagina con il nuovo campo:


La ricerca produrrà un elenco paginato con 20 occorrenze per pagina. Nell’elenco, per ogni occorrenza, è possibile effettuare le seguenti azioni:
Dettaglio: vedere il caso d’uso UC-SIE-021-03-04 – Visualizza Difensore;
Modifica: vedere il caso d’uso UC-SIE-021-03-03 – Modifica Difensore;
Cancella: vedere il caso d’uso UC-SIE-021-03-02 – Cancella Difensore.
L’entità interessata è AVVOCATO.
Nella ricerca non deve essere considerato il COD_UFFICIO_APPARTENENZA per consentire la visualizzazione di avvocati inseriti da altri uffici. Attualmente questo non avviene con la conseguente creazione di duplicati.
### UC-SIE-021-03-02 – Cancella Difensore
L’operazione di cancellazione è possibile solo se l'avvocato è stato inserito da un utente dell'ufficio corrente. Per verificare ciò occorre accedere nell’entità UTENTE_UFFICIO con UTE_COD_UTENTE = valore corrente per prelevare UFF_COD_UFFICIO. Quest’ultimo valore deve coincidere con COD_UFFICIO_APPARTENENZA dell’entità AVVOCATO.
Il caso d’uso può essere richiamato da:
UC-SIE-021-03-01 - Ricerca Difensore
tramite la scelta di menu Funzioni Amministrative > Gestione Difensori > Cancella
tramite l’immagine/link “Cancella” presente nella pagina di visualizzazione dettaglio prospettata dopo un inserimento.
Nel primo e terzo caso è possibile effettuare la cancellazione cliccando sull’immagine/link “Cancella”. Viene prospettato il messaggio: “Si conferma la cancellazione?”. Se si risponde “Annulla” non viene effettuato nulla e si resta nella pagina contenente il risultato della ricerca. Se si risponde “Ok” viene visualizzata una pagina di dettaglio con il pulsante “Conferma” la cui selezione consentirà la cancellazione logica dell’occorrenza.
Nel secondo caso invece occorre inserire le informazioni richieste nella pagina. La funzione di cancellazione, pur contenendo gli stessi controlli di quella attuale, sarà implementata con l’aggiunta del campo CODICE FISCALE. Di seguito la pagina con il nuovo campo:

Nel caso le informazioni non consentono di individuare univocamente l’avvocato da cancellare (assenza del codice fiscale) la funzione prospetta il seguente messaggio: “Attenzione: esistono più avvocati con gli stessi dati. Richiamare la funzione di ricerca per cancellare” e la cancellazione avverrà tramite il caso d’uso UCSIE02.
La cancellazione è solo di tipo logica attraverso l’aggiornamento ad “S” dell’attributo FLAG_CANCELLATO dell’entità AVVOCATO accedendo con i campi valorizzati nella pagina.
Per tutti i moduli di cui si compone SIES, propedeutico alla cancellazione è il seguente controllo:
Accedere con l’ID_AVVOCATO e con DATA_FINE_VALIDITA NULL in AVVOCATO_FASCICOLO_SIEP e verificare l’esistenza di occorrenze. In caso affermativo mostrare il messaggio bloccante: ‘Attenzione! E' impossibile cancellare questo difensore perchè ancora assegnato ad alcuni fascicoli SIEP’. Il caso d’uso termina.
Poiché viene levata la condizione di appartenenza all’ufficio, occorre effettuare un analogo controllo anche sulle entità AVVOCATO_FASCICOLO_SIGE e AVVOCATO_FASCICOLO_SIUS. In tal caso il messaggio da mostrare sarà lo stesso con l’eccezione del tipo di fascicolo.
### UC-SIE-021-03-03 - Modifica Difensore
Il caso d’uso è richiamato da UC-SIE-021-03-01 – Ricerca Difensore. Il sistema deve verificare se il FLAG_REGINDE = ‘S’. In tal caso i dati provenienti da ReGIndE non possono essere modificati ovvero:
Cognome
Nome
Data di Nascita
Luogo di Nascita
Foro
Codice Fiscale
Indirizzo PEC
Se il FLAG_REGINDE = ‘N’ sono obbligatori i campi:
Cognome
Nome
Foro
Codice Fiscale
Inoltre, se il FLAG_REGINDE = ‘N’, è presente nella parte superiore della pagina un link con il quale attivare il caso d’uso UC-SIE-021-01-01 – Ricerca Difensore su Reginde:

Una volta modificati i campi della pagina, cliccando su ‘Conferma’ si effettuano i consueti controlli di congruenza e di obbligatorietà e si procede all’aggiornamento dell’entità AVVOCATO che avrà anche valorizzati i seguenti attributi:
COD_UFFICIO_AGGIORNAMENTO = posto uguale al codice dell’ufficio che sta eseguendo l’aggiornamento
COD_OPERATORE_AGGIORNAMENTO = posto uguale al codice dell’operatore che sta eseguendo l’aggiornamento
DATA_AGGIORNAMENTO = data di sistema
Ad aggiornamento effettuato viene prospettata la pagina di visualizzazione dettaglio descritta dal caso d’uso UC-SIE-021-03-04 – Visualizza Difensore.
### UC-SIE-021-03-04 - Visualizza Difensore
Il caso d’uso è richiamato da UC-SIE-021-03-01 – Ricerca Difensore. Tramite i campi presenti nell’occorrenza della lista si accede all’entità AVVOCATO e si estraggono i dati da visualizzare nella pagina:
Cognome = COGNOME
Nome = NOME
Luogo Nascita = DESCRIZIONE che si ricava dall’entità COMUNE accedendo con COD_LUOGO_NASCITA prelevato da AVVOCATO
Data Nascita = DATA_NASCITA
Foro = FORO
Indirizzo = INDIRIZZO
Con Studio in = DESCRIZIONE che si ricava dall’entità COMUNE accedendo con COD_COMUNE_RESIDENZA prelevato da AVVOCATO
Telefono = TELEFONO
Fax = FAX
Email = E_MAIL
Codice Fiscale = CODICE_FISCALE
Nella parte inferiore della pagina è presente anche la nota ‘N.B. Dati anagrafici provenienti da ReGIndE’ se il FLAG_REGINDE = ‘S’.
Infine nella parte superiore della pagina sono presenti tre immagini/link che richiamano dei casi d’uso:

Inserisci: vedere il caso d’uso UC-SIE-021-02-01 – Inserimento Difensore
Modifica: vedere il caso d’uso UC-SIE-021-03-03 – Modifica Difensore
Cancella: vedere il caso d’uso UC-SIE-021-03-02 – Cancella Difensore
### UC-SIE-021-01-01 – Ricerca Difensore su REGINDE
Un requisito utente prevede che la ricerca del dato anagrafico su ReGIndE sia prioritaria rispetto all’inserimento manuale. Tale ricerca avverrà con comunicazione automatica, mediante l'attivazione di servizi web (PLUGIN), tra il SIES ed il sistema ReGIndE per prelevare delle informazioni per l’anagrafica dell’avvocato.
Il caso d’uso è richiamato dalla pagina di inserimento (UC-SIE-021-02-01 – Inserimento Difensore) tramite un link posto nella parte superiore della pagina:

I servizi di Accesso al Reginde consentono di effettuare ricerche di soggetti censiti nel ReGIndE. La fruizione di tali servizi avviene tramite l’esposizione di un web-service.
Per questo web service il namespace da utilizzare è “http://www.giustizia.it/serviziTelematici/reginde/interrogazioniExt”.
Di seguito l’interfaccia dei metodi che verranno utilizzati:


| Operazione: | dettaglioSoggettoPerCodice |
| --- | --- |
| Descrizione: | Ricerca i dettagli di un soggetto per codice fiscale |
| Parametri: | codice fiscale esatto del soggetto |
| Risultato: | soggetto: per maggiori informazioni consultare il wsdl |




| Operazione: | elencoPaginatoSoggetti |
| --- | --- |
| Descrizione: | Restituisce un elenco paginato di soggetti |
| Parametri: | da: indice inizio ricerca
count: numero di soggetti da ricercare |
| Risultato: | soggetto: per maggiori informazioni consultare il wsdl |



| Operazione: | ricercaSoggetto |
| --- | --- |
| Descrizione: | Ricerca lista soggetti per cognome, nome o parti di essi |
| Parametri: | cognome: cognome del soggetto eventualmente seguito dal carattere * 
nome: nome del soggetto eventualmente seguito dal carattere * 
codiceEnte: Non Applicabile |
| Risultato: | lista di soggetti: per maggiori informazioni consultare il wsdl |




| Operazione: | ricercaSoggettoEX |
| --- | --- |
| Descrizione: | Ricerca lista soggetti per codice fiscale e/o indirizzo di PEC o parte di essi. |
| Parametri: | codiceFiscale: codice fiscale da ricercare o parte di esso 
indirizzo: Non Applicabile |
| Risultato: | soggetto: per maggiori informazioni consultare il wsdl |


Per le definizioni tramite WSDL del web service che espone i metodi sopra descritti si rimanda al file ServiziInterrogazioneSoggetto.wsdl allegato.
Il link attiva una pop-up in cui si indicano:
Cognome (Campo Facoltativo)
Nome (Campo Facoltativo)
Codice Fiscale (Campo Facoltativo)
Il Pulsante “Conferma” verifica che siano valorizzati in alternativa Il Cognome, Nome o Codice Fiscale che restituirà le seguenti informazioni:
Cognome
Nome
Data di Nascita
Luogo di Nascita
Codice Fiscale
Indirizzo PEC
Poiché il numero di occorrenze dipende dai parametri inseriti verrà prospettata una lista con una o più occorrenze da cui occorre selezionare il difensore di interesse.
La selezione popola la pagina del caso d’uso UC-SIE-021-02-01 – Inserimento Difensore; i campi provenienti da ReGIndE saranno di output.
Dopo aver eventualmente valorizzato i restanti campi della pagina, selezionando il pulsante “Conferma”, il sistema effettua i consueti controlli di congruenza e di obbligatorietà e verifica, tramite il CODICE_FISCALE, l’univocità dell’occorrenza da inserire in base dati. Se il controllo ha verificato l’assenza dell’occorrenza nell’entità AVVOCATO, il sistema inserisce i campi secondo le regole esposte in UCSIE01 con l’unica eccezione del FLAG_REGINDE che deve essere valorizzato con ‘S’. Il caso d’uso termina.
In particolare si possono verificare tre casistiche:
il Codice Fiscale è già presente; il sistema prospetta il messaggio bloccante: “L’avvocato risulta già registrato per il Foro indicato”. Il caso d’uso termina;
il Servizio Web non è disponibile ed il sistema restituisce il messaggio: “Sistema ReGIndE non disponibile proseguire con l’inserimento manuale dell’anagrafica?” Se si risponde “Si” il sistema prospetta la pagina di input rendendo digitabili i campi di output e l’inserimento avverrà come descritto in UC-SIE-021-02-01 – Inserimento Difensore, altrimenti si ritorna alla Home del SIES ed il caso d’uso termina;
il Servizio Web non restituisce nessuna occorrenza; il sistema prospetta il messaggio: “Il Sistema ReGIndE non ha restituito nessun dato. Proseguire con l’inserimento manuale dell’anagrafica?”. Se si risponde “Si” il sistema prospetta la pagina di input rendendo digitabili i campi di output e l’inserimento avverrà come descritto in UC-SIE-021-02-01 – Inserimento Difensore, altrimenti si ritorna alla Home del SIES ed il caso d’uso termina.

Associazione Difensori a Fascicoli
L’associazione del difensore ad un fascicolo è oggetto di modifica software per evitare la duplicazione nell’anagrafica di un difensore.
E’ previsto l’adeguamento alle nuove funzionalità dell’Help On Line.

| Casi d’uso | Descrizione |
| --- | --- |
| UC-SIE-021-03-05 – Associa Difensore a Fascicolo SIEP. | La funzionalità si occupa dell’associazione di un difensore ad un fascicolo SIEP |
| UC-SIE-021-03-06 – Associa Difensore a Fascicolo SIUP | La funzionalità si occupa dell’associazione di un difensore ad un fascicolo SIUP |
| UC-SIE-021-03-07 – Associa Difensore a Fascicolo SIGE | La funzionalità si occupa dell’associazione di un difensore ad un fascicolo SIGE |


### UC-SIE-021-03-05 – Associa Difensore a Fascicolo SIEP.
L’associazione del difensore al fascicolo SIEP rientra tra le funzionalità da modificare per consentire l’univocità del dato all’interno dell’anagrafica degli avvocati presente nel SIES.
Attualmente la presenza di un avvocato difensore duplicato comporta l’associazione dello stesso più volte in un fascicolo. E’ possibile associare ad un Fascicolo due difensori, ma non è possibile associare due volte lo stesso difensore.
L’associazione di un avvocato ad un Fascicolo SIEP può avvenire dalla seguente scelta di menu:
Assegnazioni/Difensore (nella pagina è presente una listbox da cui occorre selezionare “Assegnazione Difensore” e successivamente cliccare sull’icona “Vai”).
Entrambe le voci di menu rimandano ad una pagina in cui sono presenti tre funzionalità:
Dismissione Mandato
Sostituzione
Assegnazione
Si analizzano le modifiche da apportare per ciascuna funzionalità.
Dismissione Mandato. Tramite il relativo pulsante, una volta selezionato il difensore, viene eliminata sull’entità AVVOCATO_FASCICOLO_SIEP l’associazione tra il fascicolo e l’avvocato.
Sostituzione. Occorre selezionare il difensore da sostituire. Tramite il relativo pulsante si accede ad una pagina contenente dei campi di input relativi al difensore da sostituire contenente i seguenti link/pulsanti:
Seleziona dalla lista: il link attiva una pop-up tramite la quale ricercare l’avvocato da associare. La query di ricerca dovrà essere modificata nelle condizioni di ricerca. In particolare deve essere tolta le condizione che si riferisce al COD_UFFICIO_APPARTENENZA. L’entità interessate sono AVVOCATO, CG_REF_CODES e COMUNE.
Conferma: tramite il pulsante si effettua l’associazione tra l’avvocato ed il fascicolo. L’entità interessata è AVVOCATO_FASCICOLO_SIEP. Prima dell’inserimento dell’occorrenza devono essere previsti i controlli di obbligatorietà su:
Cognome
Nome
Foro
Codice Fiscale
Inserimento: il pulsante richiama la pagina di inserimento presente in Funzioni Amministrative/Gestione Difensori/Inserimento la cui funzionalità è stata descritta nel caso d’uso UC-SIE-021-02-01 – Inserimento Difensore.
Assegnazione. Tramite il relativo pulsante si accede ad una pagina contenente dei campi di input relativi al difensore da associare contenente i seguenti link/pulsanti:
Seleziona dalla lista: il link attiva una pop-up tramite la quale ricercare l’avvocato da associare. La query di ricerca dovrà essere modificata nelle condizioni di ricerca. In particolare deve essere tolta le condizione che si riferisce al COD_UFFICIO_APPARTENENZA. L’entità interessate sono AVVOCATO, CG_REF_CODES e COMUNE.
Conferma: tramite il pulsante si effettua l’associazione tra l’avvocato ed il fascicolo. L’entità interessata è AVVOCATO_FASCICOLO_SIEP. Prima dell’inserimento dell’occorrenza devono essere previsti i controlli di obbligatorietà su:
Cognome
Nome
Foro
Codice Fiscale
Inserimento: il pulsante richiama la pagina di inserimento presente in Funzioni Amministrative/Gestione Difensori/Inserimento la cui funzionalità è stata descritta nel caso d’uso UC-SIE-021-02-01 – Inserimento Difensore.
### UC-SIE-021-03-06 – Associa Difensore a Fascicolo SIUS.
L’associazione del difensore al fascicolo SIUS rientra tra le funzionalità da modificare per consentire l’univocità del dato all’interno dell’anagrafica degli avvocati presente nel SIES.
Attualmente la presenza di un avvocato difensore duplicato comporta l’associazione dello stesso più volte in un fascicolo. E’ possibile associare ad un Fascicolo due difensori, ma non è possibile associare due volte lo stesso difensore.
L’associazione di un avvocato ad un Fascicolo SIUS può avvenire dalle seguenti scelte di menu:
Ricerche e Visualizzazioni/Procedimento per n° SIUS (nella pagina è presente una listbox da cui occorre selezionare “Assegnazione Difensore” e successivamente cliccare sull’icona “Vai”);
Ordinanze/Emissione Ordinanza (nella pagina è presente il link “Inserimento Difensore”).
Entrambe le voci di menu rimandano ad una pagina in cui sono presenti tre funzionalità:
Deassegnazione
Sostituzione
Assegnazione
Si analizzano le modifiche da apportare per ciascuna funzionalità.
Deassegnazione. Tramite il relativo pulsante, una volta selezionato il difensore, viene eliminata sull’entità AVVOCATO_FASCICOLO_SIUS l’associazione tra il fascicolo e l’avvocato.
Sostituzione. Occorre selezionare il difensore da sostituire. Tramite il relativo pulsante si accede ad una pagina contenente dei campi di input relativi al difensore da sostituire contenente i seguenti link/pulsanti:
Seleziona dalla lista: il link attiva una pop-up tramite la quale ricercare l’avvocato da associare. La query di ricerca dovrà essere modificata nelle condizioni di ricerca. In particolare deve essere tolta le condizione che si riferisce al COD_UFFICIO_APPARTENENZA. L’entità interessate sono AVVOCATO, CG_REF_CODES e COMUNE.
Seleziona dalla lista SIEP: il link attiva una pop-up tramite la quale ricercare l’avvocato collegato al corrispondente “Titolo esecutivo” (Fascicolo SIEP). Le entità interessate sono AVVOCATO, AVVOCATO_FASCICOLO_SIEP, CG_REF_CODES e COMUNE. Una volta selezionato l’avvocato, viene creata solo una occorrenza su AVVOCATO_FASCICOLO_SIUS tralasciando la creazione su AVVOCATO in quanto risulterebbe un inutile duplicato.
Conferma: tramite il pulsante si effettua l’associazione tra l’avvocato ed il fascicolo. L’entità interessata è AVVOCATO_FASCICOLO_SIUS. Prima dell’inserimento dell’occorrenza devono essere previsti i controlli di obbligatorietà su:
Cognome
Nome
Foro
Codice Fiscale
Inserimento: il pulsante richiama la pagina di inserimento presente in Funzioni Amministrative/Gestione Difensori/Inserimento la cui funzionalità è stata descritta nel caso d’uso UC-SIE-021-02-01 – Inserimento Difensore.
Assegnazione. Tramite il relativo pulsante si accede ad una pagina contenente dei campi di input relativi al difensore da associare contenente i seguenti link/pulsanti:
Seleziona dalla lista: il link attiva una pop-up tramite la quale ricercare l’avvocato da associare. La query di ricerca dovrà essere modificata nelle condizioni di ricerca. In particolare deve essere tolta le condizione che si riferisce al COD_UFFICIO_APPARTENENZA. L’entità interessate sono AVVOCATO, CG_REF_CODES e COMUNE.
Seleziona dalla lista SIEP: il link attiva una pop-up tramite la quale ricercare l’avvocato collegato al corrispondente “Titolo esecutivo” (Fascicolo SIEP). Le entità interessate sono AVVOCATO, AVVOCATO_FASCICOLO_SIEP, CG_REF_CODES e COMUNE. Una volta selezionato l’avvocato, viene creata solo una occorrenza su AVVOCATO_FASCICOLO_SIUS tralasciando la creazione su AVVOCATO in quanto risulterebbe un inutile duplicato.
Conferma: tramite il pulsante si effettua l’associazione tra l’avvocato ed il fascicolo. L’entità interessata è AVVOCATO_FASCICOLO_SIUS. Prima dell’inserimento dell’occorrenza devono essere previsti i controlli di obbligatorietà su:
Cognome
Nome
Foro
Codice Fiscale
Inserimento: il pulsante richiama la pagina di inserimento presente in Funzioni Amministrative/Gestione Difensori/Inserimento la cui funzionalità è stata descritta nel caso d’uso UC-SIE-021-02-01 – Inserimento Difensore.
### UC-SIE-021-03-07 – Associa Difensore a Fascicolo SIGE.
L’associazione del difensore al fascicolo SIGE rientra tra le funzionalità da modificare per consentire l’univocità del dato all’interno dell’anagrafica degli avvocati presente nel SIES.
Attualmente la presenza di un avvocato difensore duplicato comporta l’associazione dello stesso più volte in un fascicolo. E’ possibile associare ad un Fascicolo due difensori, ma non è possibile associare due volte lo stesso difensore.
L’associazione di un avvocato ad un Fascicolo SIGE può avvenire da differenti scelte di menu:
Ricerche/Procedimento per n° SIGE (dopo aver scelto il procedimento SIGE si accede ad una pagina in cui è presente una listbox da cui occorre selezionare “Assegnazione Difensore” e successivamente cliccare sull’icona “Vai”);
Ordinanze/Deposito/Notifiche » Emissione Ordinanza o Incompetenza, NDP/NLP o Ordinanza Conflitto Competenza (dopo aver scelto il procedimento SIGE si accede ad una pagina in cui è presente il link “Inserimento Difensore);
Nomina Periti/Citazioni Testi » Nomina Periti o Citazione Testi (dopo aver scelto il procedimento SIGE si accede ad una pagina in cui è presente il link “Inserimento Difensore”);
Udienze/Fissazione/Rinvio/Ruolo » Fissazione Udienza o Ordinanza Rinvio Udienza o Rinvio Udienza da Verbale o Richiesta Rogatoria MdS (dopo aver scelto il procedimento SIGE si accede ad una pagina di dettaglio udienza. Cliccando sull’immagine di “Modifica Udienza” nella pagina sarà visualizzato il link “Inserimento Difensore”);
Decreti/Deposito/Notifiche » Decreto Latitanza o Decreto Irreperibilità o Emissione Decreto Inammissibilità (dopo aver scelto il procedimento SIGE si accede alla pagina di decreto latitanza in cui sarà visualizzato il link “Inserimento Difensore”).
Le suddette voci di menu rimandano ad una pagina in cui sono presenti tre funzionalità:
Deassegnazione
Sostituzione
Assegnazione
Si analizzano le modifiche da apportare per ciascuna funzionalità.
Deassegnazione. Tramite il relativo pulsante, una volta selezionato il difensore, viene eliminata sull’entità AVVOCATO_FASCICOLO_SIGE l’associazione tra il fascicolo e l’avvocato.
Sostituzione. Occorre selezionare il difensore da sostituire. Tramite il relativo pulsante si accede ad una pagina contenente dei campi di input relativi al difensore da sostituire contenente i seguenti link/pulsanti:
Seleziona dalla lista: il link attiva una pop-up tramite la quale ricercare l’avvocato da associare. La query di ricerca dovrà essere modificata nelle condizioni di ricerca. In particolare deve essere tolta le condizione che si riferisce al COD_UFFICIO_APPARTENENZA. L’entità interessate sono AVVOCATO, CG_REF_CODES e COMUNE.
Conferma: tramite il pulsante si effettua l’associazione tra l’avvocato ed il fascicolo. L’entità interessata è AVVOCATO_FASCICOLO_SIGE. Prima dell’inserimento dell’occorrenza devono essere previsti i controlli di obbligatorietà su:
Cognome
Nome
Foro
Codice Fiscale
Inserimento: il pulsante richiama la pagina di inserimento presente in Funzioni Amministrative/Gestione Difensori/Inserimento la cui funzionalità è stata descritta nel caso d’uso UC-SIE-021-02-01 – Inserimento Difensore.
Assegnazione. Tramite il relativo pulsante si accede ad una pagina contenente dei campi di input relativi al difensore da associare contenente i seguenti link/pulsanti:
Seleziona dalla lista: il link attiva una pop-up tramite la quale ricercare l’avvocato da associare. La query di ricerca dovrà essere modificata nelle condizioni di ricerca. In particolare deve essere tolta le condizione che si riferisce al COD_UFFICIO_APPARTENENZA. L’entità interessate sono AVVOCATO, CG_REF_CODES e COMUNE.
Seleziona dalla lista SIEP: il link attiva una pop-up tramite la quale ricercare l’avvocato del Procedimento SIEP di riferimento. Le entità interessate sono AVVOCATO, AVVOCATO_FASCICOLO_SIEP, CG_REF_CODES e COMUNE. Una volta selezionato l’avvocato, viene creata solo una occorrenza su AVVOCATO_FASCICOLO_SIGE tralasciando la creazione su AVVOCATO in quanto risulterebbe un inutile duplicato.
Conferma: tramite il pulsante si effettua l’associazione tra l’avvocato ed il fascicolo. L’entità interessata è AVVOCATO_FASCICOLO_SIGE. Prima dell’inserimento dell’occorrenza devono essere previsti i controlli di obbligatorietà su:
Cognome
Nome
Foro
Codice Fiscale
Inserimento: il pulsante richiama la pagina di inserimento presente in Funzioni Amministrative/Gestione Difensori/Inserimento la cui funzionalità è stata descritta nel caso d’uso UC-SIE-021-02-01 – Inserimento Difensore.

Bonifica Pregresso
Prima dell’integrazione con il sistema ReGIndE, dovrà essere prevista una bonifica sull’entità AVVOCATO che elimini i duplicati ad oggi esistenti.
Infatti, attualmente in SIES, è permesso ad ogni ufficio l’inserimento di un Avvocato anche se già presente in banca dati. Questo porta ad un proliferare delle informazioni relative ad una stessa anagrafica.
Pertanto si prevede di progettare e realizzare un batch che accorpi gli avvocati per:

Cognome
Nome
Foro
Codice Fiscale (ove presente)
e produca in output la tabella “schiacciata” per questi dati.

Di conseguenza dovranno essere bonificate le entità che hanno un legame con l’Identificativo Avvocato ovvero:

AVVOCATO_FASCICOLO_SIEP
AVVOCATO_FASCICOLO_SIGE
AVVOCATO_FASCICOLO_SIUS
PARTI_UDIENZA_DIFENSORE
STORICO_AVVOCATO
AVVISI_AVVOCATO
NUOVA_ISTANZA

| Casi d’uso | Descrizione |
| --- | --- |
| UC-SIE-021-03-05 – Associa Difensore a Fascicolo SIEP. | Batch di accorpamento dati pregressi su entità AVVOCATO |


### UC-SIE-021-04-01 - Batch accorpamento avvocati su SIES
Il Batch è una procedura ORACLE che dovrà essere eseguita prima della messa in esercizio. Le occorrenze duplicate non verranno eliminate fisicamente ma solo logicamente tramite l’attributo FLAG_CANCELLAZIONE. La procedura dovrà essere eseguita in tutti i 29 distretti e prima della sua esecuzione dovrà essere previsto un backup delle entità interessate. Non verranno presi in considerazione i difensori che hanno il FLAG_CANCELLAZIONE uguale a NULL in quanto tali occorrenze non vengono considerate negli applicativi SIES.

Di seguito ciò che la procedura Oracle dovrà effettuare per ogni entità:
AVVOCATO:
Caso 1 (presenza di un master): Ciclare sui record duplicati per Cognome, Nome, Foro, Codice Fiscale, Flag_Cancellato diverso da Null. Per ogni gruppo di occorrenze duplicate occorre individuare quelle con cod_ufficio_appartenenza diverso da '00000'. A queste occorrenze aggiornare il Flag_Cancellato =‘S’ mentre il master (quello con cod_ufficio_appartenenza uguale a '00000') avrà Flag_Cancellato =‘N’. Le occorrenze cancellate devono essere inserite anche su STORICO_AVVOCATO con Flag_Cancellato =‘S’.
Caso 2 (assenza di un master): Ciclare sui record duplicati per Cognome, Nome, Foro, Codice Fiscale, Flag_Cancellato diverso da Null. Per ogni gruppo di occorrenze duplicate individuare quella inserita prima che avrà Flag_Cancellato =‘N’ mentre tutte le altre occorrenze verranno cancellate logicamente aggiornando ad ‘S’ il Flag_Cancellato. Le occorrenze cancellate devono essere inserite anche su STORICO_AVVOCATO con Flag_Cancellato =‘S’.
Prevedere una entità di appoggio (LOG_BONIFICA_AVVOCATO) contenente tutte le occorrenze trattate dalla procedura ed in cui indicare le occorrenze accorpate (FLAG_ACCORPATA=’A’).
AVVOCATO_FASCICOLO_SIEP
Per ogni occorrenza trattata su AVVOCATO, individuare su AVVOCATO_FASCICOLO_SIEP gli AVV_ID_AVVOCATO corrispondenti che verranno aggiornati con l’ID_AVVOCATO che li raggruppa (quello con Flag_Cancellato = ‘N’ su AVVOCATO).
Prevedere una entità di appoggio (LOG_AVVOCATO_FASCICOLO_SIEP) contenente tutte le occorrenze trattate dalla procedura ed in cui indicare ID_FASCICOLO_SIEP, AVV_ID_AVVOCATO_OLD, AVV_ID_AVVOCATO_NEW.
AVVOCATO_FASCICOLO_SIGE
Per ogni occorrenza trattata su AVVOCATO individuare su AVVOCATO_FASCICOLO_SIGE gli AVV_ID_AVVOCATO corrispondenti che verranno aggiornati con l’ID_AVVOCATO che li raggruppa (quello con Flag_Cancellato = ‘N’ su AVVOCATO).
Prevedere una entità di appoggio (LOG_AVVOCATO_FASCICOLO_SIGE) contenente tutte le occorrenze trattate dalla procedura ed in cui indicare ID_FASCICOLO_SIGE, AVV_ID_AVVOCATO_OLD, AVV_ID_AVVOCATO_NEW.
AVVOCATO_FASCICOLO_SIUS
Per ogni occorrenza trattata su AVVOCATO individuare su AVVOCATO_FASCICOLO_SIUS gli AVV_ID_AVVOCATO corrispondenti che verranno aggiornati con l’ID_AVVOCATO che li raggruppa (quello con Flag_Cancellato = ‘N’ su AVVOCATO).
Prevedere una entità di appoggio (LOG_AVVOCATO_FASCICOLO_SIUS) contenente tutte le occorrenze trattate dalla procedura ed in cui indicare ID_FASCICOLO_SIUS, AVV_ID_AVVOCATO_OLD, AVV_ID_AVVOCATO_NEW.
PARTI UDIENZA DIFENSORE
Per ogni occorrenza trattata su AVVOCATO individuare su PARTI_UDIENZA_DIFENSORE gli AVV_ID_AVVOCATO corrispondenti che verranno aggiornati con l’ID_AVVOCATO che li raggruppa (quello con Flag_Cancellato = ‘N’ su AVVOCATO).
Prevedere una entità di appoggio (LOG_PARTI_UDIENZA_DIFENSORE) contenente tutte le occorrenze trattate dalla procedura ed in cui indicare ID_AVVOCATO_PARTE_UDIENZA, AVV_ID_AVVOCATO_OLD, AVV_ID_AVVOCATO_NEW.
AVVISI_AVVOCATO
Per ogni occorrenza trattata su AVVOCATO individuare su AVVISI_AVVOCATO gli ID_AVVOCATO corrispondenti che verranno aggiornati con l’ID_AVVOCATO che li raggruppa (quello con Flag_Cancellato = ‘N’ su AVVOCATO).
Prevedere una entità di appoggio (LOG_AVVISI_AVVOCATO) contenente tutte le occorrenze trattate dalla procedura ed in cui indicare ID_AVVISO, ID_AVVOCATO_OLD, ID_AVVOCATO_NEW.
NUOVA ISTANZA
Per ogni occorrenza trattata su AVVOCATO individuare su NUOVA_ISTANZA gli AVV_ID_AVVOCATO e l’AVV_ID_AVVOCATO_PRESENTANTE corrispondenti che verranno aggiornati con l’ID_AVVOCATO che li raggruppa (quello con Flag_Cancellato = ‘N’ su AVVOCATO).
Prevedere una entità di appoggio (LOG_NUOVA_ISTANZA) contenente tutte le occorrenze trattate dalla procedura ed in cui indicare ID_NUOVA_ISTANZA, AVV_ID_AVVOCATO_OLD, AVV_ID_AVVOCATO_NEW, AVV_ID_AVVOCATO_PRESENTANTE_OLD, AVV_ID_AVVOCATO_PRESENTANTE_NEW.


## Matrice di tracciabilità
Di seguito viene riportata la matrice di tracciabilità che contiene la relazione fra i requisiti e casi d’uso.

#### SIES -REGINDE
|  | UC-SIE-021-02-01 | UC-SIE-021-03-01 | UC-SIE-021-03-02 | UC-SIE-021-03-03 | UC-SIE-021-03-04 | UC-SIE-021-01-01 | UC-SIE-021-03-05 | UC-SIE-021-03-06 | UC-SIE-021-03-07 | UC-SIE-021-04-01 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| REQ-SIE-021-01 |  |  |  |  |  |  |  |  |  |  |
| REQ-SIE-021-02 |  |  |  |  |  |  |  |  |  |  |
| REQ-SIE-021-03 |  |  |  |  |  |  |  |  |  |  |
| REQ-SIE-021-04 |  |  |  |  |  |  |  |  |  |  |



# Dizionario dati
## Schema Logico
| Entity Name | Entity Name | Entity Description | Entity Description | Entity Description | Entity Description | Entity Description | Entity Description |
| --- | --- | --- | --- | --- | --- | --- | --- |
|  | Column Name | Column Description | Data Type | Length | Primary Key | Nullable | Unique |
| ENTITA’ | ENTITA’ |  |  |  |  |  |  |
|  | Id |  | int | 0 | true | false | false |
|  | Testo |  | int | 0 | false | true | false |
|  | titolo |  | int | 0 | false | false | false |

## Schema Fisico
| Entity Name | Entity Name | Entity Description | Entity Description | Entity Description | Entity Description | Entity Description | Entity Description |
| --- | --- | --- | --- | --- | --- | --- | --- |
|  | Column Name | Column Description | Data Type | Length | Primary Key | Nullable | Unique |
| TABELLA | TABELLA |  |  |  |  |  |  |
|  | K1_ID |  | bigint | 16 | true | false | true |
|  | TS_TITOLO |  | nvarchar | 50 | false | true | false |
|  | TS_TESTO |  | nvarchar | 200 | false | false | false |