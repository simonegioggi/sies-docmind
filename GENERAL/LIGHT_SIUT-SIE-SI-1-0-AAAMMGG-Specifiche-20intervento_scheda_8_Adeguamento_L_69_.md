---
uniqueName: lightsiut-sie-si-1-0-aaammgg-specifiche-20interven
displayName: "LIGHT SIUT SIE SI 1 0 AAAMMGG Specifiche 20intervento scheda 8 Adeguamento L 69 "
category: "GENERAL"
tags: []
---

# LIGHT_SIUT-SIE-SI-1.0-AAAMMGG-Specifiche%20intervento_scheda_8_Adeguamento_L_69_2019

> **File originale:** `MEV/SCHEDA_008/documenti stefy/LIGHT_SIUT-SIE-SI-1.0-AAAMMGG-Specifiche%20intervento_scheda_8_Adeguamento_L_69_2019.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |










Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del sistema informativo unitario telematico, la manutenzione degli attuali sistemi dell’area penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
| Versione | 1.0 del xx/xx/2019 |
| --- | --- |
| Redatto da: | Stefania Barca |
| Verificato da | Vito Bufi |
| Approvato da | Paolo Ceccanti |
| Data approvazione | GG/MM/AAAA |
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
| 1.0 | GG/MM/AAAA | Prima Emissione |  |


INDICE DEI CONTENUTI
Introduzione	6
1.1	Scopo del documento	6
1.2	Acronimi e Definizioni	6
1.2.1	Acronimi	6
1.2.2	Definizioni	7
1.3	Riferimenti	7
Definizione dell’Obiettivo	8
Architettura del Sistema	10
Specifiche dei requisiti	11
Premessa	11
Elenco Requisiti	11
Interfacce	16
Casi d’uso	17
Tipologie di utenti	17
Definizione casi d’uso	17
Nuovo obbligo del condannato: Partecipazione a percorsi di recupero	17
Selezione Obbligo condannato	18
Dettaglio tecnico di intervento	19
Dettaglio Tecnico	19
Requisiti	19
Pena Sospesa non menzione (ex Art 163-165 c.p.)	19
Requisiti	20
Gestione Pene Sospese - Richieste- Adempimento obblighi	20
Requisiti	21
Stampa Richiesta adempimento obblighi	21
Requisiti	22
Gestione Pene Sospese - Richieste-Determinazione termini	22
Requisiti	23
Stampa Richiesta Determinazione Termini	23
Requisiti	25
Selezione Tipo di Provvedimento	25
Requisiti	25
Gestione Pene Sospese - Richieste - Revoca beneficio ex art.168 c.p. - 674 c.p.p.	25
Requisiti	26
Scadenzario Termini Ottemperanza Obblighi	26
Requisiti	26
Scadenzario Termini Sospensione condizionale	27
Requisiti	27
Gestione Pene Sospese - estinzione reato	27
Requisiti	27
Stampa richiesta estinzione reato	28
Requisiti	30
Stampa Copertina	30
Requisiti	31
Certificato Esecuzione	31
Requisiti	31
Gestione parti offese e difensori	34
Dettaglio procedimento - Menu funzionalità	35
Requisiti	36
Dettaglio procedimento - link	37
Requisiti	37
Inserimento parte offesa	38
Requisiti	39
Visualizzazione dettaglio parte offesa	39
Requisiti	40
Modifica parte offesa	40
Requisiti	40
Cancellazione parte offesa	40
Requisiti	40
Gestione parti offese - elenco	40
Requisiti	40
Assegnazione difensore parte offesa	41
Requisiti	42
Gestione difensore - Elenco	43
Requisiti	43
Deassegnazione difensore	43
Requisiti	43
Sostituzione difensore	44
Requisiti	44
Apertura istruttoria Cumulo - replica parti offese/difensori	44
Requisiti	44
Cumulo - Gestione dati analitici	44
Requisiti	44
Requisiti	45
Trasferimento per competenza	45
Requisiti	45
Notifica Comunicazione alla parte offesa e al difensore	46
Alert comunicazione a persona offesa/difensore	47
Requisiti	48
Generazione comunicazione	48
Requisiti	48
Stampa Comunicazione	48
Requisiti	48
Dizionario dati	49
Schema Logico	49
Schema Fisico	49


Introduzione
## Scopo del documento
Il presente documento riporta le specifiche di intervento sul software, metodologia WATERFALL, al fine di soddisfare i requisiti espressi dall’Amministrazione e descritti nella scheda di intervento SIUT-SIE-SC-1.1-20191011 Scheda Intervento n.8 legge 69 2019.
## Acronimi e Definizioni
### Acronimi
| Sigla | Descrizione |
| --- | --- |
| AgID | Agenzia per l’Italia Digitale |
| API | Application Programming Interface |
| C.P.U | Central Processing Unit |
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
| SIC.P. | Sistema Informativo Cognizione Penale |
| SIU | Sistema Informativo Unitario |
| SLA | Service Level Agreement |
| SM | Security Manager |
| SQL | Structured Query Language |
| SW | SoftWare |
| TT | Trouble Ticketing |
| VPN | Virtual Private Network |

### Definizioni
| Glossario | Sinonimo | Definizione |
| --- | --- | --- |
|  |  |  |


## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
|  | SIUT-SIE-SC-1.1-20191011 Scheda Intervento n.8 legge 69 2019 | Scheda di intervento |
|  |  |  |


Definizione dell’Obiettivo
Gli interventi descritti nel presente documento saranno effettuati sul Sistema Esecuzione e Sorveglianza, relativamente ai requisiti espressi dall’Amministrazione nella richiesta di intervento e descritti nella scheda di intervento [Rif. 1].

L’Amministrazione ha espresso l’esigenza di adeguare l’applicativo alle nuove disposizioni della legge 69/2019.
Si riporta di seguito un estratto degli articoli di legge di interesse per l’intervento evolutivo.

“LEGGE 19 luglio 2019, n. 69
Modifiche al codice penale, al codice di procedura penale e altre disposizioni in materia di tutela delle vittime di violenza domestica e di genere. (19G00076) (GU n.173 del 25-7-2019)
Art. 6
Modifica all'articolo 165 del codice penale in materia di sospensione condizionale della pena
1. All'articolo 165 del codice penale, dopo il quarto comma e’ inserito il seguente: «Nei casi di condanna per i delitti di cui agli articoli 572, 609-bis, 609-ter, 609-quater, 609-quinquies, 609-octies e 612-bis, nonché agli articoli 582 e 583-quinquies nelle ipotesi aggravate ai sensi degli articoli 576, primo comma, numeri 2, 5 e 5.1, e 577, primo comma, numero 1, e secondo comma, la sospensione condizionale della pena è comunque subordinata alla partecipazione a specifici percorsi di recupero presso enti o associazioni che si occupano di prevenzione, assistenza psicologica e recupero di soggetti condannati per i medesimi reati».
2. Dall'attuazione delle disposizioni di cui al comma 1 non devono derivare nuovi o maggiori oneri a carico della finanza pubblica. Gli oneri derivanti dalla partecipazione ai corsi di recupero di cui all'articolo 165 del codice penale, come modificato dal citato comma 1, sono a carico del condannato.
Art. 15
Modifiche agli articoli 90-ter, 282-ter, 282-quater, 299 e 659 del codice di procedura penale
1. All'articolo 90-ter del codice di procedura penale è aggiunto, in fine, il seguente comma: «1-bis. Le comunicazioni previste al comma 1 sono sempre effettuate alla persona offesa e al suo difensore, ove nominato, se si procede per i delitti previsti dagli articoli 572, 609-bis, 609-ter, 609-quater, 609-quinquies, 609-octies e 612-bis del codice penale, nonché dagli articoli 582 e 583-quinquies del codice penale nelle ipotesi aggravate ai sensi degli articoli 576, primo comma, numeri 2, 5 e 5.1, e 577, primo comma, numero 1, e secondo comma, del codice penale».
2. Al comma 1 dell'articolo 282-ter del codice di procedura penale sono aggiunte, in fine, le seguenti parole: «, anche disponendo l'applicazione delle particolari modalità di controllo previste dall'articolo 275-bis».
3. Al comma 1 dell'articolo 282-quater del codice di procedura penale, dopo le parole: «alla parte offesa» sono inserite le seguenti: «e, ove nominato, al suo difensore».
4. Al comma 2-bis dell'articolo 299 del codice di procedura penale, le parole: «al difensore della persona offesa o, in mancanza di questo, alla persona offesa» sono sostituite dalle seguenti: «alla persona offesa e, ove nominato, al suo difensore».
5. Dopo il comma 1 dell'articolo 659 del codice di procedura penale è inserito il seguente: «1-bis. Quando a seguito di un provvedimento del giudice di sorveglianza deve essere disposta la scarcerazione del condannato per uno dei delitti previsti dagli articoli 572, 609-bis, 609-ter, 609-quater, 609-quinquies, 609-octies e 612-bis del codice penale, nonché dagli articoli 582 e 583-quinquies del codice penale nelle ipotesi aggravate ai sensi degli articoli 576, primo comma, numeri 2, 5 e 5.1, e 577, primo comma, numero 1, e secondo comma, del codice penale, il pubblico ministero che cura l'esecuzione ne dà' immediata comunicazione, a mezzo della polizia giudiziaria, alla persona offesa e, ove nominato, al suo difensore».


Architettura del Sistema
n.a.




Specifiche dei requisiti
Premessa
Sulla base degli applicativi oggetto del contratto e delle aree funzionali, la convenzione per l’identificazione dei requisiti è riportata di seguito.
Ciascun requisito è individuato da un identificativo univoco nella forma [REQ-SIS-nnn-mm_ZZ.pp], dove la parte evidenziata in grigio riporta il macro requisito espresso dall’Amministrazione e codificato nella scheda di intervento, i restanti caratteri identificano rispettivamente:
ZZ il tipo requisito (vedere la tabella di seguito riportata);
pp il progressivo requisito nell’ambito del tipo requisito.

| Tipo Requisito | Descrizione |
| --- | --- |
| AM | Ambientale |
| AR | Architetturale |
| CF | Configurazione |
| FN | Funzionale |
| UI | Interfaccia Utente |
| PR | Prestazionali |
| IN | Interoperabilità |
| SC | Sicurezza |
| SI | Sistema |
| TU | Tutorial |
| RG | Relazione Giuridica |


Elenco Requisiti
| Codice Requisito | Descrizione | Riferimenti |
| --- | --- | --- |
| REQ-SIE-008-01_FN.01 | L'utente deve potere selezionare, nella gestione di un beneficio di sospensione della pena subordinata agli obblighi e in tutte le funzionalità ad esso correlate, il nuovo obbligo del condannato “Partecipazione a percorsi di recupero” . | art.6 co. 1 L. 69/2019 |
| REQ-SIE-008-01_FN.02 | L'utente deve potere gestire, nella funzionalità di inserimento e modifica del Provvedimento di sospensione condizionale della pena ex art. 163-165 c.p.,  i dati relativi al nuovo obbligo del condannato Partecipazione a percorsi di recupero | art.6 co. 1 L. 69/2019 |
| REQ-SIE-008-01_FN.03 | L'utente deve potere visualizzare, nella funzionalità di gestione degli adempimenti agli obblighi del condannato per sospensione condizionale della pena ex art. 163-165 c.p.,  i dati relativi al nuovo obbligo del condannato Partecipazione a percorsi di recupero, in presenza di unico beneficio. | scheda intervento |
| REQ-SIE-008-01_FN.04 | L'utente deve potere inserire, nella funzionalità gestione degli adempimenti agli obblighi del condannato per sospensione condizionale della pena ex art. 163-165 c.p.,  i dati relativi al nuovo obbligo del condannato Partecipazione a percorsi di recupero.   
Al salvataggio dei dati il sistema deve impostare lo stato con il valore "Richiesta adempimento obblighi" | scheda intervento |
| REQ-SIE-008-01_FN.05 | Nella stampa della richiesta di adempimento obblighi del condannato devono essere presenti le informazioni sul nuovo obbligo del condannato e l'ente presso cui adempirà all'obbligo. | scheda intervento |
| REQ-SIE-008-01_FN.06 | L'utente deve potere visualizzare, nella funzionalità di gestione delle richieste di determinazione termini per sospensione condizionale della pena ex art. 163-165 c.p.,  i dati relativi al nuovo obbligo del condannato Partecipazione a percorsi di recupero, in presenza di unico beneficio. | scheda intervento |
| REQ-SIE-008-01_FN.07 | L'utente deve potere inserire, nella funzionalità gestione delle richieste di determinazione termini per sospensione condizionale della pena ex art. 163-165 c.p.,  i dati relativi al nuovo obbligo del condannato Partecipazione a percorsi di recupero.  Al salvataggio dei dati il sistema deve impostare lo stato con il valore "Richiesta determinazione termini" | scheda intervento |
| REQ-SIE-008-01_FN.08 | Nella stampa della richiesta determinazione termini sono presenti le informazioni sul nuovo obbligo del condannato e l'ente presso cui adempirà all'obbligo. | scheda intervento |
| REQ-SIE-008-01_FN.09 | All'atto del salvataggio dei dati di richiesta di estinzione reato ex art. 167 c.p., il sistema deve impostare lo stato con il valore "Richiesta estinzione reato ex art. 167 c.p." | scheda intervento |
| REQ-SIE-008-01_FN.10 | All'atto del salvataggio dei dati di richiesta di estinzione reato ex art. 445 c.2 c.p.p., il sistema deve impostare lo stato con il valore "Richiesta estinzione reato ex art. 445 c.2 c.p.p." | scheda intervento |
| REQ-SIE-008-01_FN.11 | Nella stampa della richiesta estinzione reato devono essere presenti le informazioni sul nuovo obbligo del condannato e l'ente presso cui adempirà all'obbligo. | scheda intervento |
| REQ-SIE-008-01_FN.12 | L'utente deve potere selezionare, nella gestione di una revoca beneficio ex art. 168 c.p.p., una delle opzioni nel menu a tendina "Tipo di Provvedimento": Sentenza, Provvedimento". | scheda intervento |
| REQ-SIE-008-01_FN.13 | L'utente, all'atto dell'inserimento di una revoca di benefico ex art. 168 c.p.p., relativo a un provvedimento di revoca per mancato adempimento agli obblighi, deve potere visualizzare i dati della notizia adempimento obblighi. | scheda intervento |
| REQ-SIE-008-01_FN.14 | Nello Scadenzario Termini Ottemperanza Obblighi, devono essere visualizzati tutti i procedimenti di classe III aventi un beneficio subordinato all'ottemperanza obblighi e aventi solo la richiesta di sospensione della pena. 
Nell'elenco devono essere inclusi i procedimenti aventi una richiesta di beneficio con il nuovo tipo di obbligo.
Inoltre, tutti i procedimenti in scadenza saranno visualizzati solo se la richiesta scade nei 30 giorni successivi alla data di visualizzazione. | scheda intervento |
| REQ-SIE-008-01_FN.15 | Nello scadenzario ottemperanza Obblighi, non devono essere visualizzati i procedimenti di classe III aventi un provvedimento di revoca del beneficio ex art. 168 c.p.. | scheda intervento |
| REQ-SIE-008-01_FN.16 | Nello Scadenzario Termini Sospensione Condizionale, devono essere visualizzati tutti i procedimenti di classe III, aventi solo la richiesta di sospensione della pena, inclusi i procedimenti aventi una richiesta di beneficio con il nuovo tipo di obbligo. 
Inoltre, tutti i procedimenti in scadenza saranno visualizzati solo se la richiesta scade nei 30 giorni successivi alla data di visualizzazione. | scheda intervento |
| REQ-SIE-008-01_FN.17 | Nello scadenzario Termini Sospensione Condizionale, non devono essere visualizzati i procedimenti di classe III aventi un provvedimento di revoca del beneficio. | scheda intervento |
| REQ-SIE-008-01_FN.18 | Nella stampa della copertina sono presenti le informazioni sul nuovo obbligo del condannato, il termine adempimento obblighi e il tipo obbligo. | Scheda intervento |
| REQ-SIE-008-01_FN.19 | Nella stampa del certificato esecuzione sono presenti le informazioni sul nuovo obbligo del condannato, il termine adempimento obblighi e il tipo obbligo. | Scheda intervento |
| REQ-SIE-008-02_FN.01 | L'utente deve avere accesso al nuovo menu di gestione dei dati delle parti offese e dei rispettivi difensori legati a un dato procedimento. | scheda intervento |
| REQ-SIE-008-02_FN.02 | Il sistema deve visualizzare la nuova voce di menu Gestione parte offesa/Difensore solo all'ufficio titolare del procedimento. La voce di menu sarà pertanto visibile solo all'ufficio che ha emesso il procedimento oppure all'ufficio destinatario del trasferimento. | scheda intervento |
| REQ-SIE-008-02_FN.03 | Il sistema deve permettere di inserire i dati anagrafici di una o più parti offese. | scheda intervento |
| REQ-SIE-008-02_FN.04 | Il sistema deve permettere di visualizzare l'elenco delle parti offese associate al procedimento. 
L'elenco deve essere accessibile dal menu del dettaglio procedimento oppure dal link presente sul dettaglio del procedimento. | scheda intervento |
| REQ-SIE-008-02_FN.05 | Il sistema deve permettere di visualizzare il dettaglio dei dati anagrafici della parte offesa. | scheda intervento |
| REQ-SIE-008-02_FN.06 | Il sistema deve permettere di modificare i dati anagrafici di una parte offesa precedentemente inserita. | scheda intervento |
| REQ-SIE-008-02_FN.07 | Il sistema deve permettere di cancellare i dati anagrafici di una parte offesa precedentemente inserita. 
Il sistema deve chiedere espressa conferma all'utente dell'azione di cancellazione. | scheda intervento |
| REQ-SIE-008-02_FN.08 | Nella maschera di dettaglio del procedimento, il sistema deve visualizzare il link "Gestione parte offesa", se è stata associata, al procedimento, almeno una parte offesa. 
Il link deve essere visualizzato nella riga riportante i dati anagrafici del condannato. | scheda intervento |
| REQ-SIE-008-02_FN.09 | Il sistema deve visualizzare il nuovo link Gestione parte offesa solo all'ufficio titolare del procedimento (ufficio che ha emesso il procedimento oppure ufficio destinatario del trasferimento). | scheda intervento |
| REQ-SIE-008-02_FN.10 | Il sistema deve permettere di gestire uno o più difensori della parte offesa. | scheda intervento |
| REQ-SIE-008-02_FN.11 | Il sistema deve permettere di assegnare uno o più difensori alla parte offesa, mediante l'inserimento dei dati di un difensore. | scheda intervento |
| REQ-SIE-008-02_FN.12 | Il sistema deve permettere la ricerca di un difensore censito nel sistema. | scheda intervento |
| REQ-SIE-008-02_FN.13 | Il sistema deve permettere di assegnare il difensore selezionato nella lista. | scheda intervento |
| REQ-SIE-008-02_FN.14 | Il sistema deve impedire di assegnare più di due difensori alla parte offesa | scheda intervento |
| REQ-SIE-008-02_FN.15 | Il sistema deve permettere di eliminare l'assegnazione di un difensore a una parte offesa. | scheda intervento |
| REQ-SIE-008-02_FN.16 | Il sistema deve permettere di sostituire un difensore assegnato a una parte offesa. | scheda intervento |
| REQ-SIE-008-02_FN.17 | Il sistema, all'atto dell'apertura di una istruttoria del cumulo, deve replicare i dati delle persone offese e dei difensori di tutti i procedimenti coinvolti nel cumulo. | scheda intervento |
| REQ-SIE-008-02_FN.18 | Il sistema deve permettere di gestire le persone offese e i difensori dei titoli coinvolti nel cumulo, anche se ancora non validato. | scheda intervento |
| REQ-SIE-008-02_FN.19 | Il sistema deve permettere la visualizzazione, nel dettaglio del Cumulo, della funzionalità di gestione persona offesa/difensore di un cumulo validato. | scheda intervento |
| REQ-SIE-008-02_FN.20 | Il sistema deve prevedere, all'atto del trasferimento per competenza, il trasferimento dei dati della persona offesa e dei rispettivi difensori all'ufficio destinatario. | scheda intervento |
| REQ-SIE-008-03_FN.01 | L'utente, all'atto della validazione dei provvedimenti elencati di seguito, deve visualizzare un messaggio informativo che lo avverte che deve mandare specifica comunicazione alla parte offesa: 
Evasione
Scarcerazione
Estinzione Reato
Estinzione Pena
Concessione, Sostituzione e Revoca di Misure Alternative
Concessione, Sostituzione e Revoca di Misure di Sicurezza
Provvedimenti di Variazione Pena. | art. 15 L. 69/2019 |
| REQ-SIE-008-03_FN.02 | L'utente deve poter generare la comunicazione a ciascuna parte offesa e rispettivi difensori. | scheda intervento |
| REQ-SIE-008-03_FN.03 | L'utente deve potere stampare la comunicazione alla parte offesa relativa all'emissione dei provvedimenti a carico del condannato di: 
Evasione
Scarcerazione
Estinzione Reato
Estinzione Pena
Concessione, Sostituzione e Revoca di Misure Alternative
Concessione, Sostituzione e Revoca di Misure di Sicurezza
Provvedimenti di Variazione Pena | art. 15 L. 69/2019 |


Interfacce
Nel caso siano oggetto di modifica, le interfacce interessate dall’intervento sono riportate all’interno dei casi d’uso che descrivono ciascun intervento.
Le immagini riportate nei casi d’uso hanno lo scopo di facilitare la comprensione dell’intervento, ma potrebbero differire dalle effettive maschere dell’applicativo.

Casi d’uso
Tipologie di utenti
| Utenti | Descrizione |
| --- | --- |
| Utente Siep |  |


Definizione casi d’uso
Nuovo obbligo del condannato: Partecipazione a percorsi di recupero
La Legge 69/2019 introduce un nuovo obbligo del condannato per i reati ivi specificati relativamente alla sospensione condizionale della pena. Detto obbligo consiste nella partecipazione a precorsi di recupero presso enti o associazioni.

| Casi d'uso | Descrizione |
| --- | --- |
| Selezione Obbligo condannato | Nel menu a tendina Tipologia Obbligo sarà presente la nuova tipologia "Partecipazione a percorsi di recupero". |
| Pena Sospesa non menzione (ex Art 163-165 c.p.) | L'utente SIEP può inserire una sospensione condizionale della pena subordinata al nuovo obbligo, selezionando la nuova voce, nel menu a tendina "Obblighi del condannato" - "Partecipazione a percorsi di recupero" e digitare il termine dell'adempimento e l'Ente presso cui sarà effettuato il percorso di recupero. |
| Gestione Pene Sospese - Richieste- Adempimento obblighi | L'utente, nella richiesta di adempimento obblighi del condannato, gestisce il nuovo obbligo. I dati del nuovo obbligo sono recuperati dal sistema se è presente il beneficio, altrimenti possono essere inseriti mediante questa funzionalità. |
| Stampa Richiesta adempimento obblighi | L'utente, nella stampa della Richiesta di adempimento obblighi, ritrova le informazioni sul nuovo obbligo del condannato e la struttura presso cui il condannato adempirà all'obbligo. |
| Gestione Pene Sospese - Richieste-Determinazione termini | L'utente, nella richiesta di determinazione dei termini per l'obbligo del condannato, gestisce il nuovo obbligo. I dati del nuovo obbligo sono recuperati dal sistema se è presente il beneficio e la richiesta di adempimento, altrimenti possono essere inseriti mediante questa funzionalità. |
| Stampa Richiesta Determinazione Termini | L'utente, nella stampa della Richiesta di  determinazione termini, ritrova le informazioni sul nuovo obbligo del condannato e la struttura presso cui il condannato adempirà all'obbligo. |
| Gestione Pene Sospese - Richieste - Revoca beneficio ex art.168 c.p. - 674 c.p.p. | Nella maschera di gestione della revoca dei benefici l'utente può selezionare due tipi di Provvedimento: Sentenza, Provvedimento.
Se l'utente seleziona "Sentenza", la maschera si presenta come è attualmente; se l'utente seleziona "provvedimento", la maschera presenterà, in sola visualizzazione, i dati della notizia di adempimento obblighi relativi al mancato adempimento degli obblighi del condannato, se presenti in banca dati. |
| Stampa richiesta estinzione reato | L'utente, nella stampa della Richiesta di estinzione reato, ritrova le informazioni sul nuovo obbligo del condannato e la struttura presso cui il condannato adempirà all'obbligo. |
| Selezione Tipo di Provvedimento | Nel menu a tendina Tipo di Provvedimento devono essere presenti due opzioni: "Sentenza", "Provvedimento". |
| Scadenzario Termini Ottemperanza Obblighi | Lo scadenzario Termini Ottemperanza Obblighi deve riportare l'elenco di tutti i procedimenti di classe III con beneficio subordinato agli obblighi, inclusi quelli in cui è previsto il nuovo obbligo (Partecipazione a percorsi di recupero) e non aventi un provvedimento di revoca del beneficio ex art. 168 c.p.  e 674 c.p.p..   
Nel tab  'Tutti' e ‘In Scadenza’ sono visualizzati i procedimenti, con beneficio subordinato agli obblighi, che scadono nei 30 giorni successivi alla data di visualizzazione, anziché nei 7 giorni successivi. |
| Scadenzario Termini Sospensione condizionale | Lo scadenzario Termini Sospensione Condizionale deve riportare l'elenco di tutti i procedimenti di classe III, inclusi quelli in cui è previsto il beneficio con il nuovo obbligo (Partecipazione a percorsi di recupero) e non aventi un provvedimento di revoca del beneficio ex art. 168 c.p. e 674 c.p.p. 
Nel tab  'Tutti' e ‘In Scadenza’ sono visualizzati i procedimenti, con beneficio della sospensione pena, che scadono nei 30 giorni successivi alla data di visualizzazione, anziché nei 7 giorni successivi. |
| Gestione Pene Sospese - estinzione reato | All'atto dell'inserimento di un provvedimento di richiesta estinzione reato, il sistema deve aggiornare lo stato del procedimento con i seguenti valori:

Estinzione reato ex art.167 c.p. se l'utente ha selezionato, nel menu a tendina "Articolo", il valore Estinzione reato ex art.167 c.p. ; 
Estinzione reato ex art.445 c.2 c.p.p. se l'utente ha selezionato, nel menu a tendina "Articolo", il valore Estinzione reato ex art.445 c.2 c.p.p. |
| Certificato Esecuzione | L'utente, nella stampa del certificato esecuzione, ritrova le informazioni sul nuovo obbligo del condannato, il termine adempimento obblighi e la struttura presso cui frequentare il percorso di recupero. |
| Stampa Copertina | L'utente, nella stampa della copertina, ritrova le informazioni sul nuovo obbligo del condannato, il termine adempimento obblighi, il tipo obbligo e la struttura presso cui frequentare il percorso di recupero. |


## Selezione Obbligo condannato
ID: UC-SIE-008-01.01
Nel menu a tendina Tipologia Obbligo deve essere presente la nuova tipologia "Partecipazione a percorsi di recupero".



Nuovo obbligo del condannato
## Dettaglio tecnico di intervento
| Dettaglio Tecnico |
| --- |
| ■ Inserimento record nella tabella Obblighi |
| • Inserire un nuovo record nella tabella Obblighi valorizzando il campo descrizione con il valore "Partecipazione a percorsi di recupero" |

## Requisiti
REQ-SIE-008-01_FN.01 - Selezione nuovo obbligo condannato: Partecipazione a percorsi di recupero

## Pena Sospesa non menzione (ex Art 163-165 c.p.)
ID: UC-SIE-008-01.02
L'utente SIEP può inserire una sospensione condizionale della pena subordinata al nuovo obbligo, selezionando la nuova voce, nel menu a tendina "Obblighi del condannato" - "Partecipazione a percorsi di recupero" e digitare il termine dell'adempimento e l'Ente presso cui sarà effettuato il percorso di recupero.


Sospensione condizionale della pena subordinata al nuovo obbligo
## Requisiti
REQ-SIE-008-01_FN.02 - Pena Sospesa non menzione (ex Art 163-165 c.p.) nuovo tipo di obbligo
## Gestione Pene Sospese - Richieste- Adempimento obblighi
ID: UC-SIE-008-01.03
L'utente, nella richiesta di adempimento obblighi del condannato, gestisce il nuovo obbligo. I dati del nuovo obbligo sono recuperati dal sistema se è presente il beneficio, altrimenti possono essere inseriti mediante questa funzionalità. Nella maschera è presente il nuovo campo Ente/Struttura in cui sarà visualizzata, oppure inserita, la struttura di recupero.
Al salvataggio dei dati,  il sistema imposta lo stato del procedimento con il valore "Notizie adempimento obblighi".



Richiesta notizie adempimento obblighi
## Requisiti
REQ-SIE-008-01_FN.04 - Notizie Adempimento Obblighi - nuovo tipo di obbligo in assenza di beneficio
REQ-SIE-008-01_FN.03 - Notizie Adempimento Obblighi - nuovo tipo di obbligo in presenza di beneficio presente
## Stampa Richiesta adempimento obblighi
ID: UC-SIE-008-01.04
L'utente, nella stampa della Richiesta di adempimento obblighi, ritrova le informazioni sul nuovo obbligo del condannato e la struttura presso cui il condannato adempirà all'obbligo.




Proposta di stampa
## Requisiti
REQ-SIE-008-01_FN.05 - Notizie Adempimento Obblighi: Stampa
## Gestione Pene Sospese - Richieste-Determinazione termini
ID: UC-SIE-008-01.05
L'utente, nella richiesta di determinazione dei termini per l'obbligo del condannato, gestisce il nuovo obbligo. I dati del nuovo obbligo sono recuperati dal sistema se è presente il beneficio e la richiesta di adempimento, altrimenti possono essere inseriti mediante questa funzionalità. Nella maschera è presente il nuovo campo Ente/Struttura in cui sarà visualizzata, oppure inserita, la struttura di recupero.
Al salvataggio dei dati,  il sistema imposta lo stato del procedimento con il valore "Richiesta determinazione termini".


Richiesta determinazione termini

## Requisiti
REQ-SIE-008-01_FN.07 - Richiesta Determinazione Termini in assenza di beneficio
REQ-SIE-008-01_FN.06 - Richiesta Determinazione Termini in presenza di beneficio
## Stampa Richiesta Determinazione Termini
ID: UC-SIE-008-01.06
L'utente, nella stampa della Richiesta di  determinazione termini, ritrova le informazioni sul nuovo obbligo del condannato e la struttura presso cui il condannato adempirà all'obbligo.



Proposta di stampa

## Requisiti
REQ-SIE-008-01_FN.08 - Richiesta Determinazione Termini in assenza di beneficio -stampa
## Selezione Tipo di Provvedimento
ID: UC-SIE-008-01.08
Nel menu a tendina Tipo di Provvedimento della funzionalità Revoca beneficio ex art. 168 c.p.p., devono essere presenti due opzioni: "Sentenza", "Provvedimento".


Revoca beneficio ex art. 168 c.p.p. - Tipo Provvedimento
## Requisiti
REQ-SIE-008-01_FN.12 - Selezione Tipo di provvedimento: Sentenza, Provvedimento
## Gestione Pene Sospese - Richieste - Revoca beneficio ex art.168 c.p. - 674 c.p.p.
ID: UC-SIE-008-01.07
Nella maschera di gestione della revoca dei benefici l'utente può selezionare due tipi di Provvedimento: Sentenza, Provvedimento.
Se l'utente seleziona "Sentenza", la maschera si presenta come è attualmente; se l'utente seleziona "provvedimento", la maschera presenterà, in sola visualizzazione, i dati della notizia di adempimento obblighi relativi al mancato adempimento degli obblighi del condannato, se presenti in banca dati.




Nuova sezione per tipo Provvedimento “Provvedimento”

PER EMMA: NELLA PAGINA RIMANE LA SELEZIONE DEL PROVVEDIMENTO DALLA LISTA? (VEDI LINK SOTTO TIPO PROVVEDIMENTO)
## Requisiti
REQ-SIE-008-01_FN.13 - Revoca Beneficio ex art. 168 c.p.p. - Provvedimento
## Scadenzario Termini Ottemperanza Obblighi
ID: UC-SIE-008-01.09
Lo scadenzario Termini Ottemperanza Obblighi deve riportare l'elenco di tutti i procedimenti di classe III con beneficio subordinato agli obblighi, inclusi quelli in cui è previsto il nuovo obbligo (Partecipazione a percorsi di recupero) e non aventi un provvedimento di revoca del beneficio ex art. 168 c.p.  e 674 c.p.p.
Nel tab  'Tutti' e ‘In Scadenza’ sono visualizzati i procedimenti, con beneficio subordinato agli obblighi, che scadono nei 30 giorni successivi alla data di visualizzazione, anziché nei 7 giorni successivi.
## Requisiti
REQ-SIE-008-01_FN.14 - Scadenzario Termini Ottemperanza Obblighi - Richieste
REQ-SIE-008-01_FN.15 - Scadenzario Termini Ottemperanza Obblighi - Revoca beneficio ex art. 168 c.p. - 674 c.p.p.
## Scadenzario Termini Sospensione condizionale
ID: UC-SIE-008-01.10
Lo scadenzario Termini Sospensione Condizionale deve riportare l'elenco di tutti i procedimenti di classe III, inclusi quelli in cui è previsto il beneficio con il nuovo obbligo (Partecipazione a percorsi di recupero) e non aventi un provvedimento di revoca del beneficio ex art. 168 c.p. e 674 c.p.p.
Nel tab  'Tutti' e ‘In Scadenza’ sono visualizzati i procedimenti, con beneficio della sospensione pena, che scadono nei 30 giorni successivi alla data di visualizzazione, anziché nei 7 giorni successivi.
## Requisiti
REQ-SIE-008-01_FN.16 - Scadenzario Termini Sospensione Condizionale
REQ-SIE-008-01_FN.17 - Scadenzario Termini Sospensione Condizionale - Revoca beneficio ex art. 168 c.p. e 674 c.p.p.
## Gestione Pene Sospese - estinzione reato
ID: UC-SIE-008-01.11
All'atto dell'inserimento di un provvedimento di richiesta estinzione reato, il sistema deve aggiornare lo stato del procedimento con i seguenti valori:
Estinzione reato ex art.167 c.p. se l'utente ha selezionato, nel menu a tendina "Articolo", il valore Estinzione reato ex art.167 c.p. ;
Estinzione reato ex art.445 c.2 c.p.p. se l'utente ha selezionato, nel menu a tendina "Articolo", il valore Estinzione reato ex art.445 c.2 c.p.p.


Richiesta Estinzione reato ex art. 167 c.p.
## Requisiti
REQ-SIE-008-01_FN.09 - Richiesta Estinzione reato ex art. 167c.p. - nuovo stato procedimento
REQ-SIE-008-01_FN.10 - Richiesta Estinzione reato ex art.445 c.2 c.p.p. - nuovo stato procedimento
## Stampa richiesta estinzione reato
ID: UC-SIE-008-01.12
L'utente, nella stampa della Richiesta di estinzione reato, ritrova le informazioni sul nuovo obbligo del condannato e la struttura presso cui il condannato adempirà all'obbligo.


Proposta di stampa

PER EMMA: LA STAMPA DA CAMBIARE CON I DATI DELLOBBLIGO è QUELLA RELATIVA ALL’ART. 167, QUANDO SI SELEZIONA ADEMPIMENTO OBBLIGO nella MOTIVAZIONE? (VEDI IMMAGINE SCENARIO PRECEDENTE)
## Requisiti
REQ-SIE-008-01_FN.11 - Richiesta estinzione reato - stampa
## Stampa Copertina
ID: UC-SIE-008-01.13
L'utente, nella stampa della copertina, ritrova le informazioni sul nuovo obbligo del condannato, il termine adempimento obblighi, il tipo obbligo e la struttura presso cui frequentare il percorso di recupero.



Proposta di stampa

## Requisiti
REQ-SIE-008-01_FN.18 - Stampa copertina: dati relativi al nuovo tipo di obbligo
## Certificato Esecuzione
ID: UC-SIE-008-01.14
L'utente, nella stampa del certificato esecuzione, ritrova le informazioni sul nuovo obbligo del condannato, il termine adempimento obblighi e la struttura presso cui frequentare il percorso di recupero.



Proposta di stampa

## Requisiti
REQ-SIE-008-01_FN.19 - Certificato Esecuzione: dati relativi al nuovo tipo di obbligo




#### Matrice tracciabilità



| Requisiti/Use Case | Selezione Obbligo condannato | Pena Sospesa non menzione (ex Art 163-165 c.p.) | Adempimento obblighi - Nuovo obbligo condannato | Gestione Pene Sospese - Richieste - Adempimento obblighi | Stampa Richiesta adempimento obblighi | Gestione Pene Sospese - Richieste-Determinazione termini | Stampa Richiesta Determinazione Termini | Gestione Pene Sospese - Richieste - Revoca beneficio ex art.168 c.p. - 674 c.p.p | Selezione Tipo di Provvedimento | Scadenzario Termini Ottemperanza Obblighi | Scadenzario Termini Sospensione condizionale | Gestione Pene Sospese - estinzione reato | Stampa richiesta estinzione reato | Stampa Copertina | Certificato Esecuzione |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Selezione nuovo obbligo condannato: Partecipazione a percorsi di recupero | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| Pena Sospesa non menzione (ex Art 163-165 c.p.) nuovo tipo di obbligo |  | X |  |  |  |  |  |  |  |  |  |  |  |  |  |
| Notizie Adempimento Obblighi - nuovo tipo di obbligo in presenza di beneficio presente |  |  |  | X |  |  |  |  |  |  |  |  |  |  |  |
| Notizie Adempimento Obblighi - nuovo tipo di obbligo in assenza di beneficio |  |  |  | X |  |  |  |  |  |  |  |  |  |  |  |
| Notizie Adempimento Obblighi: Stampa |  |  |  |  | X |  |  |  |  |  |  |  |  |  |  |
| Richiesta Determinazione Termini in presenza di beneficio |  |  | X |  |  | X |  |  |  |  |  |  |  |  |  |
| Richiesta Determinazione Termini in assenza di beneficio |  |  |  |  |  | X |  |  |  |  |  |  |  |  |  |
| Richiesta Determinazione Termini in assenza di beneficio - stampa |  |  |  |  |  |  | X |  |  |  |  |  |  |  |  |
| Richiesta Estinzione reato ex art. 167cp - nuovo stato procedimento |  |  |  |  |  |  |  |  |  |  |  | X |  |  |  |
| Richiesta Estinzione reato ex art.445 c.2 cpp - nuovo stato procedimento |  |  |  |  |  |  |  |  |  |  |  | X |  |  |  |
| Richiesta estinzione reato - stampa |  |  |  |  |  |  |  |  |  |  |  |  | X |  |  |
| Selezione Tipo di provvedimento: Sentenza, Provvedimento |  |  |  |  |  |  |  |  | X |  |  |  |  |  |  |
| Revoca Beneficio ex art. 168 cpp - Provvedimento |  |  |  |  |  |  |  | X |  |  |  |  |  |  |  |
| Scadenzario Termini Ottemperanza Obblighi - Richieste |  |  |  |  |  |  |  |  |  | X |  |  |  |  |  |
| Scadenzario Termini Ottemperanza Obblighi - Revoca beneficio ex art. 168 cp - 674 cpp |  |  |  |  |  |  |  |  |  | X |  |  |  |  |  |
| Scadenzario Termini Sospensione Condizionale |  |  |  |  |  |  |  |  |  |  | X |  |  |  |  |
| Scadenzario Termini Sospensione Condizionale - Revoca beneficio ex art. 168 cp .674 cpp |  |  |  |  |  |  |  |  |  |  | X |  |  |  |  |
| Stampa copertina: dati relativi al nuovo tipo di obbligo |  |  |  |  |  |  |  |  |  |  |  |  |  | X |  |
| Certificato Esecuzione: dati relativi al nuovo tipo di obbligo |  |  |  |  |  |  |  |  |  |  |  |  |  |  | X |

Gestione parti offese e difensori
La Legge 69/2019 prevede che, all'atto dell'emissione di determinati provvedimenti che colpiscono il condannato in relazione all'esecuzione della pena per reati commessi e compresi nell'elenco incluso nella legge stessa, deve essere sempre data comunicazione alla persona offesa e, ove nominato, al suo difensore.
Nel sistema deve essere pertanto presente, per un dato procedimento, la gestione delle parti offese e dei rispettivi difensori.
È necessario apportare le modifiche alle funzionalità di dettaglio del procedimento, alle funzionalità di gestione delle istruttorie di cumulo e alla funzionalità di trasferimento per competenza.

| Casi d'uso | Descrizione |
| --- | --- |
| Dettaglio procedimento - Menu funzionalità | Il sistema deve permettere di inserire le parti offese e i rispettivi difensori in un procedimento. Il sistema pertanto deve visualizzare, nel menu delle funzioni, la nuova funzionalità di gestione delle parti offese e dei difensori.
La funzionalità deve essere visibile solo all'ufficio titolare del procedimento (ufficio che ha emesso il procedimento oppure ufficio destinatario del trasferimento).
La funzionalità sarà presente anche per il cumulo. |
| Dettaglio procedimento - link | Il sistema deve permettere di richiamare la funzionalità elenco delle parti offese mediante un link posto nella pagina di dettaglio del procedimento.
Il link deve essere visibile solo all'ufficio titolare del procedimento (ufficio che ha emesso il procedimento oppure ufficio destinatario del trasferimento).
Il link deve essere visibile solo se è presente almeno una parte offesa.
Il link è presente anche per il cumulo. |
| Inserimento parte offesa | La nuova funzionalità permette di inserire una o più persone offese. |
| Gestione parti offese - elenco | La funzione permette di visualizzare l'elenco delle parti offese associate al procedimento.
Nella maschera sono presenti i link per il dettaglio, l'inserimento, la modifica  e cancellazione dei dati di una parte offesa e per la modifica dei difensori. |
| Modifica parte offesa | La funzionalità permette di modificare i dati anagrafici di una parte offesa. |
| Cancellazione parte offesa | La funzionalità permette dii cancellare i dati anagrafici di una parte offesa. |
| Gestione difensore - Elenco | La funzionalità permette di visualizzare l'elenco dei difensori della parte offesa.
Nella maschera sono presenti i pulsanti di de assegnazione, assegnazione o sostituzione di un difensore. |
| Assegnazione difensore parte offesa | La funzionalità permette di assegnare un difensore alla parte offesa.
È possibile assegnare al massimo due difensori.
È possibile assegnare un difensore già censito nella banca dati oppure inserire i dati di un nuovo difensore.
Si precisa che nella fase di analisi di dettaglio sarà possibile integrare l'eventuale chiamata al RegInde per il reperimento dei dati degli avvocati censiti nel suddetto registro. |
| Deassegnazione difensore | La funzione permette di eliminare l'assegnazione di un difensore della parte offesa. |
| Sostituzione difensore | La funzionalità deve permettere di sostituire un difensore assegnato alla parte offesa. |
| Visualizzazione dettaglio parte offesa | La funzione permette di visualizzare il dettaglio dei dati anagrafici della parte offesa. |
| Istanza di cumulo - gestione parte offesa/difensore | All'atto dell'apertura di una istruttoria di cumulo, saranno replicati i dati delle persone offese e dei rispettivi difensori, se presenti, di tutti i titoli coinvolti nel cumulo. |
| Apertura istruttoria Cumulo | La funzionalità di apertura Istruttoria Cumulo prevede la replica dei dati delle persone offese e dei rispettivi difensori di tutti i procedimenti coinvolti nel cumulo. |
| Cumulo - Gestione dati analitici | Per ciascun procedimento coinvolto nel Cumulo è possibile gestire i dati delle persone offese e dei rispettivi difensori mediante la nuova funzionalità richiamata mediante il pulsante "Gestione parte offesa/difensore". La funzione è richiamabile dal pulsante Dati Analitici. |
| Trasferimento per competenza | La funzionalità di trasferimento per competenza deve prevedere il trasferimento anche dei dati della persona offesa e dei rispettivi difensori.
L'ufficio destinatario del procedimento diventa pertanto titolare dei dati della persona offesa e del difensore, ha visibilità e possibilità di gestione degli stessi. |

## Dettaglio procedimento - Menu funzionalità
ID: UC-SIE-008-02.01
Il sistema deve permettere di inserire le parti offese e i rispettivi difensori in un procedimento. Il sistema pertanto deve visualizzare, nel menu delle funzioni, la nuova funzionalità di gestione delle parti offese e dei difensori.
La funzionalità deve essere visibile solo all'ufficio titolare del procedimento (ufficio che ha emesso il procedimento oppure ufficio destinatario del trasferimento).
La funzionalità sarà presente anche per il cumulo.


Dettaglio procedimento - Nuova funzionalità



Dettaglio Cumulo - Nuova funzionalità
## Requisiti
REQ-SIE-008-02_FN.02 - Gestione Parte offesa/Difensore - visibilità voce di menu
REQ-SIE-008-02_FN.01 - Gestione Parte offesa/Difensore - Menu
REQ-SIE-008-02_FN.19 - Dettaglio cumulo validato -Menu
## Dettaglio procedimento - link
ID: UC-SIE-008-02.02
Il sistema deve permettere di richiamare la funzionalità elenco delle parti offese mediante un link posto nella pagina di dettaglio del procedimento.
Il link deve essere visibile solo all'ufficio titolare del procedimento (ufficio che ha emesso il procedimento oppure ufficio destinatario del trasferimento).
Il link deve essere visibile solo se è presente almeno una parte offesa.
Il link è presente anche per il cumulo.



Dettaglio Procedimento - link



Dettaglio Cumulo - link
## Requisiti
REQ-SIE-008-02_FN.08 - Dettaglio Procedimento - link Gestione Parte offesa
REQ-SIE-008-02_FN.09 - Dettaglio procedimento - visibilità link Gestione parte offesa

## Inserimento parte offesa
ID: UC-SIE-008-02.03
La nuova funzionalità permette di inserire una o più parti offese.
Per l’inserimento della prima parte offesa il sistema presenta direttamente la pagina con i campi da digitare.
Le successive parti offese avverranno mediante il pulsante di inserimento.



Inserimento parte offesa


Inserimento parte offesa – altri dati


Dettaglio parte offesa

Elenco parti offese con link funzioni

## Requisiti
REQ-SIE-008-02_FN.03 - Inserimento parte offesa
## Visualizzazione dettaglio parte offesa
ID: UC-SIE-008-02.04
La funzione permette di visualizzare il dettaglio dei dati anagrafici della parte offesa.


Dettaglio parte offesa
## Requisiti
REQ-SIE-008-02_FN.05 - Visualizzazione dettaglio parte offesa
## Modifica parte offesa
ID: UC-SIE-008-02.05
La funzionalità permette di modificare i dati anagrafici di una parte offesa.

## Requisiti
REQ-SIE-008-02_FN.06 - Modifica parte offesa
## Cancellazione parte offesa
ID: UC-SIE-008-02.06
La funzionalità permette di cancellare i dati anagrafici di una parte offesa.

## Requisiti
REQ-SIE-008-02_FN.07 - Cancellazione parte offesa
## Gestione parti offese - elenco
ID: UC-SIE-008-02.07
La funzione permette di visualizzare l'elenco delle parti offese associate al procedimento.
Nella maschera sono presenti i link per il dettaglio, l'inserimento, la modifica  e cancellazione dei dati di una parte offesa e per la modifica dei difensori.


Gestione parti offese
## Requisiti
REQ-SIE-008-02_FN.04 - Visualizzazione elenco parti offese
## Assegnazione difensore parte offesa
ID: UC-SIE-008-02.08
La funzionalità permette di assegnare un difensore alla parte offesa.
È possibile assegnare al massimo due difensori.
È possibile assegnare un difensore già censito nella banca dati oppure inserire i dati di un nuovo difensore.
Si precisa che nella fase di analisi di dettaglio sarà possibile integrare l'eventuale chiamata al RegInde per il reperimento dei dati degli avvocati censiti nel suddetto registro.



Inserimento nuovo difensore



Dettaglio difensore




Selezione difensore da una lista


Elenco difensori



Messaggio bloccante
## Requisiti
REQ-SIE-008-02_FN.11 - Assegnazione difensore parte offesa - inserimento dati
REQ-SIE-008-02_FN.12 - Assegnazione difensore parte offesa - selezione da lista
REQ-SIE-008-02_FN.13 - Assegnazione difensore selezionato
REQ-SIE-008-02_FN.14 - Limite numero difensori assegnati
## Gestione difensore - Elenco
ID: UC-SIE-008-02.09
La funzionalità permette di visualizzare l'elenco dei difensori della parte offesa.
Nella maschera sono presenti i pulsanti di de assegnazione, assegnazione o sostituzione di un difensore.


Elenco difensori
## Requisiti
REQ-SIE-008-02_FN.10 - Gestione difensore parte offesa - elenco
## Deassegnazione difensore
ID: UC-SIE-008-02.10
La funzione permette di eliminare l'assegnazione di un difensore della parte offesa.


Deassegnazione difensore


Messaggio di conferma

## Requisiti
REQ-SIE-008-02_FN.15 - De assegnazione difensore parte offesa
## Sostituzione difensore
ID: UC-SIE-008-02.11
La funzionalità deve permettere di sostituire un difensore assegnato alla parte offesa.




Sostituzione difensore
## Requisiti
REQ-SIE-008-02_FN.16 - Sostituzione difensore parte offesa

## Apertura istruttoria Cumulo - replica parti offese/difensori
ID: UC-SIE-008-02.12
La funzionalità di apertura Istruttoria Cumulo, oltre alla replica dei dati del titolo coinvolto, replicherà anche i dati delle persone offese e dei rispettivi difensori.
L'attuale funzionalità sarà pertanto modificata.
## Requisiti

REQ-SIE-008-02_FN.17 - Apertura istruttoria Cumulo - dati persone offese e difensori
## Cumulo - Gestione dati analitici
ID: UC-SIE-008-02.13
Per ciascun procedimento coinvolto nel Cumulo è possibile gestire i dati delle persone offese e dei rispettivi difensori mediante la nuova funzionalità richiamata dal pulsante “Dati Analitici - Gestione parte offesa/difensore".
## Requisiti
REQ-SIE-008-02_FN.18 - Cumulo- dati analitici titoli coinvolti



Cumulo - Dati Analitici - Nuovo pulsante Gestione parte offesa/difensore


Cumulo - Gestione parte offesa/difensore  - elenco persone offese
## Requisiti
REQ-SIE-008-02_FN.18 - Cumulo- dati analitici titoli coinvolti
## Trasferimento per competenza
ID: UC-SIE-008-02.14
La funzionalità di trasferimento per competenza deve prevedere il trasferimento anche dei dati della persona offesa e dei rispettivi difensori.
L'ufficio destinatario del procedimento diventa pertanto titolare dei dati della persona offesa e del difensore, ha visibilità e possibilità di gestione degli stessi.
L’attuale funzionalità deve essere pertanto modificata.
## Requisiti
REQ-SIE-008-02_FN.20 - Trasferimento per competenza - dati persona offesa/difensore

#### Matrice tracciabilità
| Requisiti/Use Case | Dettaglio procedimento - Menu funzionalità | Dettaglio procedimento - link | Inserimento parte offesa | Visualizzazione dettaglio parte offesa | Modifica parte offesa | Cancellazione parte offesa | Gestione parti offese - elenco | Assegnazione difensore parte offesa | Gestione difensore - Elenco | Deassegnazione difensore | Sostituzione difensore | Apertura istruttoria Cumulo - replica parti offese/difensori | Cumulo - Gestione dati analitici | Trasferimento per competenza |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Gestione Parte offesa/Difesore - Menu | X |  |  |  |  |  |  |  |  |  |  |  |  |  |
| Gestione Parte offesa/Difensore - visibilità voce di menu | X |  |  |  |  |  |  |  |  |  |  |  |  |  |
| Inserimento parte offesa |  |  | X |  |  |  |  |  |  |  |  |  |  |  |
| Visualizzazione elenco parti offese |  |  |  |  |  |  | X |  |  |  |  |  |  |  |
| Visualizzazione dettaglio parte offesa |  |  |  | X |  |  |  |  |  |  |  |  |  |  |
| Modifica parte offesa |  |  |  |  | X |  |  |  |  |  |  |  |  |  |
| Cancellazione parte offesa |  |  |  |  |  | X |  |  |  |  |  |  |  |  |
| Dettaglio Procedimento - link Gestione Parte offesa |  | X |  |  |  |  |  |  |  |  |  |  |  |  |
| Dettaglio procedimento - visibilità link Gestione parte offesa |  | X |  |  |  |  |  |  |  |  |  |  |  |  |
| Gestione difensore parte offesa - elenco |  |  |  |  |  |  |  |  | X |  |  |  |  |  |
| Assegnazione difensore parte offesa - inserimento dati |  |  |  |  |  |  |  | X |  |  |  |  |  |  |
| Assegnazione difensore parte offesa - selezione da lista |  |  |  |  |  |  |  | X |  |  |  |  |  |  |
| Assegnazione difensore selezionato |  |  |  |  |  |  |  | X |  |  |  |  |  |  |
| Limite numero difensori assegnati |  |  |  |  |  |  |  | X |  |  |  |  |  |  |
| De assegnazione difensore parte offesa |  |  |  |  |  |  |  |  |  | X |  |  |  |  |
| Sostituzione difensore parte offesa |  |  |  |  |  |  |  |  |  |  | X |  |  |  |
| Apertura istruttoria Cumulo - dati persone offese e difensori |  |  |  |  |  |  |  |  |  |  |  | X |  |  |
| Cumulo- dati analitici titoli coinvolti |  |  |  |  |  |  |  |  |  |  |  |  | X |  |
| Dettaglio cumulo validato - menu | X |  |  |  |  |  |  |  |  |  |  |  |  |  |
| Trasferimento per competenza - dati persona offesa/difensore |  |  |  |  |  |  |  |  |  |  |  |  |  | X |


Notifica Comunicazione alla parte offesa e al difensore
All'atto della validazione di un provvedimento relativo a un delitto che, ai sensi della legge 69/2019, prevede l'obbligo di informare la parte offesa e, ove nominato, il suo difensore, il sistema deve informare l'utente che deve predisporre apposita comunicazione.
Una nuova funzionalità consentirà di predisporre la comunicazione da recapitare alla parte offesa e, se presente, al suo difensore.
La comunicazione sarà prodotta mediante un nuovo template e generata in formato PDF.
NOTA: è a cura dell'Amministrazione stabilire dove visualizzare il pulsante di generazione della comunicazione.
Si fa presente che il fornitore propone di visualizzare il pulsante di generazione della comunicazione nella maschera di dettaglio del provvedimento dopo la validazione e di inserire una nuova funzionalità di visualizzazione comunicazioni alla persona offesa/difensore, legate a un procedimento, nel menu principale visualizzato a sinistra dello schermo.


| Casi d'uso | Descrizione |
| --- | --- |
| Alert comunicazione a persona offesa/difensore | Il sistema visualizza un messaggio informativo, all'atto della validazione di un provvedimento emesso per uno o più delitti interessati dalla riforma e riguardanti:
Evasione
Scarcerazione
Estinzione Reato
Estinzione Pena
Concessione, Sostituzione e Revoca di Misure Alternative
Concessione, Sostituzione e Revoca di Misure di Sicurezza
Provvedimenti di Variazione Pena.
Il messaggio informa l'utente che vi è obbligo di informare la persona offesa e, ove nominato, il difensore. |
| Generazione comunicazione | La nuova funzionalità permette di creare un atto per la comunicazione a ciascuna parte offesa e, ove presente, a ciascun difensore delle parti offese.
NOTA: nel presente documento si propone di richiamare la funzionalità nella maschera di validazione del provvedimento.
Tuttavia, si segnala la necessità di prevedere una funzionalità, inserita nel menu principale, che consenta di generare la comunicazione successivamente. |
| Stampa Comunicazione | La nuova funzionalità  permette la produzione della stampa della comunicazione, utilizzando un nuovo template.
NOTA: si precisa che il template sarà concordato con l'Amministrazione. |

## Alert comunicazione a persona offesa/difensore
ID: UC-SIE-008-03.01
Il sistema visualizza un messaggio informativo, all'atto della validazione di un provvedimento emesso per uno o più delitti interessati dalla riforma e riguardanti:
Evasione
Scarcerazione
Estinzione Reato
Estinzione Pena
Concessione, Sostituzione e Revoca di Misure Alternative
Concessione, Sostituzione e Revoca di Misure di Sicurezza
Provvedimenti di Variazione Pena.
Il messaggio informa l'utente che vi è obbligo di informare la persona offesa e, ove nominato, il difensore con apposita comunicazione.
## Requisiti
REQ-SIE-008-03_FN.01 - Alert comunicazione a persona offesa
## Generazione comunicazione
ID: UC-SIE-008-03.02
La nuova funzionalità permette di creare un atto per la comunicazione a ciascuna parte offesa e, ove presente, a ciascun difensore delle parti offese.
NOTA: nel presente documento si propone di richiamare la funzionalità nella maschera di validazione del provvedimento.
Tuttavia, si segnala la necessità di prevedere una funzionalità, inserita nel menu principale, che consenta di generare la comunicazione successivamente.

## Requisiti
REQ-SIE-008-03_FN.02 - Generazione comunicazione a parte offesa/difensore
## Stampa Comunicazione
ID: UC-SIE-008-03.03
La nuova funzionalità  permette la produzione della stampa della comunicazione, utilizzando un nuovo template.
NOTA: si precisa che il template sarà concordato con l'Amministrazione.
## Requisiti
REQ-SIE-008-03_FN.03 - Stampa comunicazione a persona offesa

#### Matrice tracciabilità

| Requisiti/Use Case | Alert comunicazione a persona offesa/difensore | Generazione comunicazione | Stampa Comunicazione |
| --- | --- | --- | --- |
| Alert comunicazione a persona offesa | X |  |  |
| Generazione comunicazione a parte offesa/difensore |  | X |  |
| Stampa comunicazione a persona offesa |  |  | X |








Dizionario dati
Schema Logico
| Entity Name | Entity Name | Entity Description | Entity Description | Entity Description | Entity Description | Entity Description | Entity Description |
| --- | --- | --- | --- | --- | --- | --- | --- |
|  | Column Name | Column Description | Data Type | Length | Primary Key | Nullable | Unique |
| ENTITA’ | ENTITA’ |  |  |  |  |  |  |
|  | Id |  | int | 0 | true | false | false |
|  | Testo |  | int | 0 | false | true | false |
|  | titolo |  | int | 0 | false | false | false |

Schema Fisico
| Entity Name | Entity Name | Entity Description | Entity Description | Entity Description | Entity Description | Entity Description | Entity Description |
| --- | --- | --- | --- | --- | --- | --- | --- |
|  | Column Name | Column Description | Data Type | Length | Primary Key | Nullable | Unique |
| TABELLA | TABELLA |  |  |  |  |  |  |
|  | K1_ID |  | bigint | 16 | true | false | true |
|  | TS_TITOLO |  | nvarchar | 50 | false | true | false |
|  | TS_TESTO |  | nvarchar | 200 | false | false | false |