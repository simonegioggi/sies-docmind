---
uniqueName: siut-sie-si-1-0-aaammgg-specifiche-20interventosch
displayName: "SIUT SIE SI 1 0 AAAMMGG Specifiche 20intervento  scheda 8 Adeguamento L 69 2019"
category: "GENERAL"
tags: []
---

# SIUT-SIE-SI-1.0-AAAMMGG-Specifiche%20intervento__scheda_8_Adeguamento_L_69_2019

> **File originale:** `MEV/SCHEDA_008/documenti stefy/SIUT-SIE-SI-1.0-AAAMMGG-Specifiche%20intervento__scheda_8_Adeguamento_L_69_2019.docx`  
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
1.	Introduzione	8
1.1	Scopo del documento	8
1.2	Riferimenti	8
1.3	Acronimi e Definizioni	8
1.3.1	Acronimi	8
1.3.2	Definizioni	9
2.	Definizione dell’Obiettivo	10
3.	Architettura del Sistema	12
4.	Specifiche dei requisiti	13
4.1.	Premessa	13
4.2.	Elenco Requisiti	13
5.	Interfacce	17
6.	Casi d’uso	18
6.1.	Tipologie di utenti	18
6.2.	Definizione casi d’uso	18
6.2.1.	Nuovo obbligo del condannato: Partecipazione a percorsi di recupero	18
Selezione Obbligo condannato	19
Scenari	20
Selezione Obbligo condannato	20
Dettaglio tecnico di intervento	20
Dettaglio Tecnico	20
Requisiti	21
	Pena Sospesa non menzione (ex Art 163-165 c.p.)	21
Scenari	21
Inserimento pena sospesa/non menzione	21
Requisiti	22
Gestione Pene Sospese - Richieste- Adempimento obblighi	22
Scenari	22
Adempimento obblighi in assenza di iscrizione beneficio	22
Adempimento obblighi in presenza di iscrizione beneficio	23
Adempimento obblighi in presenza di iscrizione beneficio - modifica valori	24
Requisiti	24
Stampa Richiesta adempimento obblighi	24
Scenari	25
Adempimento obblighi - stampa	25
Requisiti	26
Gestione Pene Sospese - Richieste-Determinazione termini	26
Scenari	26
Determinazione termini in assenza di iscrizione beneficio	26
Determinazione termini in presenza di iscrizione beneficio	26
Determinazione termini in presenza di iscrizione beneficio - modifica valori	27
Dettaglio tecnico di intervento	28
Requisiti	28
Stampa Richiesta Determinazione Termini	28
Scenari	28
Richiesta determinazione termini - stampa	28
Requisiti	30
Selezione Tipo di Provvedimento	30
Scenari	30
Selezione Tipo Provvedimento	30
Requisiti	31
Gestione Pene Sospese - Richieste - Revoca beneficio ex art.168 c.p. - 674 c.p.p.	31
Scenari	31
Revoca beneficio ex art. 168 c.p.p. in presenza di notizia di mancato adempimento agli obblighi	31
Revoca beneficio ex art. 168 c.p.p. in assenza di notizia di mancato adempimento agli obblighi	32
Requisiti	32
Scadenzario Termini Ottemperanza Obblighi	32
Scenari	33
Scadenzario Termine Ottemperanza Obblighi	33
Scadenzario Termine Ottemperanza Obblighi - revoca	33
Requisiti	33
Scadenzario Termini Sospensione condizionale	33
Scenari	34
Scadenzario Termini Sospensione condizionale	34
Scadenzario Termini Sospensione condizionale - revoca	34
Requisiti	34
Gestione Pene Sospese - estinzione reato	34
Scenari	35
Richiesta Estinzione reato ex art. 167 c.p.	35
Richiesta Estinzione reato ex art. 445 c.2 c.p.p.	35
Requisiti	36
Stampa richiesta estinzione reato	36
Scenari	36
Richiesta estinzione reato - stampa	36
Requisiti	38
Stampa Copertina	38
Scenari	38
Stampa copertina	38
Requisiti	39
Certificato Esecuzione	39
Scenari	40
Certificato Esecuzione	40
Requisiti	40
6.2.2.	Gestione parti offese e difensori	43
Dettaglio procedimento - Menu funzionalità	44
Scenari	45
Utente titolare del procedimento: nuova funzionalità nel menu	45
Utente titolare del cumulo: nuova funzionalità nel menu	45
Utente NON titolare del procedimento: nuova funzionalità nel menu	46
Requisiti	47
Dettaglio procedimento - link	47
Scenari	47
ufficio titolare procedimento - link gestione parte offesa	47
ufficio titolare cumulo - link gestione parte offesa	48
ufficio NON titolare procedimento - link gestione parte offesa	48
Requisiti	49
Inserimento parte offesa	49
Scenari	49
Inserimento prima parte offesa	49
Inserimento altre parti offese	51
Requisiti	52
Visualizzazione dettaglio parte offesa	52
Scenari	52
Visualizzazione dettaglio parte offesa	52
Requisiti	53
Modifica parte offesa	53
Scenari	53
Modifica dati parte offesa	53
Requisiti	53
Cancellazione parte offesa	53
Scenari	54
Cancellazione parte offesa	54
Requisiti	54
Gestione parti offese - elenco	54
Scenari	54
Gestione parti offese - elenco	54
Requisiti	55
Assegnazione difensore parte offesa	55
Scenari	55
Assegnazione primo difensore con nuovi dati	55
Assegnazione difensore presente in banca dati	57
Assegnazione altro difensore	58
Assegnazione difensore oltre numero massimo	58
Requisiti	59
Gestione difensore - Elenco	59
Scenari	59
Gestione Difensore	59
Requisiti	60
Deassegnazione difensore	60
Scenari	60
De assegnazione difensore	60
Requisiti	61
Sostituzione difensore	61
Scenari	61
Sostituzione difensore	61
Requisiti	62
Apertura istruttoria Cumulo - replica parti offese/difensori	62
Scenari	62
Apertura istruttoria Cumulo: replica dati persona offesa e difensori	62
Requisiti	63
Cumulo - Gestione dati analitici	63
Scenari	63
Dettaglio dati analitici - gestione parte offesa/difensore	63
Requisiti	64
Requisiti	64
Trasferimento per competenza	65
Scenari	65
Trasferimento per competenza - visibilità e gestione persona offesa/difensore	65
Requisiti	65
6.2.3.	Notifica Comunicazione alla parte offesa e al difensore	66
Alert comunicazione a persona offesa/difensore	67
Scenari	68
Validazione provvedimento - presenza persona offesa	68
Validazione provvedimento - assenza persona offesa	68
Requisiti	68
Generazione comunicazione	68
Scenari	69
Generazione comunicazione parte offesa/difensore	69
Requisiti	69
Stampa Comunicazione	69
Scenari	70
Stampa comunicazione parte offesa/difensore	70
Requisiti	70
2	Dizionario dati	71
2.1	Schema Logico	71
2.2	Schema Fisico	71


Introduzione
## Scopo del documento
Il presente documento riporta le specifiche di intervento sul software, metodologia WATERFALL, al fine di soddisfare i requisiti espressi dall’Amministrazione e descritti nella scheda di intervento SIUT-SIE-SC-1.1-20191011 Scheda Intervento n.8 legge 69 2019.
## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF1. | SIUT-SIE-SC-1.1-20191011 Scheda Intervento n.8 legge 69 2019 | Scheda di intervento |
|  |  |  |

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
| AR | Architetturale |
| CF | Configurazione |
| FN | Funzionale |
| UI | Interfaccia Utente |
| PR | Prestazionali |
| IN | Interoperabilità |
| SC | Sicurezza |
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
Nel caso fossero oggetto di modifica, le interfacce interessate dall’intervento sono riportate all’interno dei casi d’uso che descrivono ciascun intervento.
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
| Selezione Obbligo condannato | Nel menu a tendina Tipologia Obbligo deve essere presente la nuova tipologia "Partecipazione a percorsi di recupero". |
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
| Scadenzario Termini Sospensione condizionale | Lo scadenzario Termini Sospensione Condizionale deve riportare l'elenco di tutti i procedimenti di classe III, inclusi quelli in cui è previsto il beneficio con il nuovo obbligo (Partecipazione a percorsi di recupero) e non aventi un provvedimento di revoca del beneficio ex art. 168 c.p. e 674 c.p.p..  
Nel tab  'Tutti' e ‘In Scadenza’ sono visualizzati i procedimenti, con beneficio della sospensione pena, che scadono nei 30 giorni successivi alla data di visualizzazione, anziché nei 7 giorni successivi. |
| Gestione Pene Sospese - estinzione reato | All'atto dell'inserimento di un provvedimento di richiesta estinzione reato, il sistema deve aggiornare lo stato del procedimento con i seguenti valori:

Estinzione reato ex art.167 c.p. se l'utente ha selezionato, nel menu a tendina "Articolo", il valore Estinzione reato ex art.167 c.p. ; 
Estinzione reato ex art.445 c.2 c.p.p. se l'utente ha selezionato, nel menu a tendina "Articolo", il valore Estinzione reato ex art.445 c.2 c.p.p.. |
| Certificato Esecuzione | L'utente, nella stampa del certificato esecuzione, ritrova le informazioni sul nuovo obbligo del condannato, il termine adempimento obblighi e la struttura presso cui frequentare il percorso di recupero. |
| Stampa Copertina | L'utente, nella stampa della copertina, ritrova le informazioni sul nuovo obbligo del condannato, il termine adempimento obblighi, il tipo obbligo e la struttura presso cui frequentare il percorso di recupero. |


## Selezione Obbligo condannato
ID: UC-SIE-008-01.01
Nel menu a tendina Tipologia Obbligo deve essere presente la nuova tipologia "Partecipazione a percorsi di recupero".

| Attori |  |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIES.
L'utente è abilitato a gestire i provvedimenti di sospensione condizionale della pena ex art. 163-165 c.p. |
| Punto d'innesco | SIEP\dettaglio procedimento\iscrizione concessione benefici\pena sospesa non menzione (Ex artt. 163 165 c.p.) |
| Stato Base | N/A |

## Scenari
### Selezione Obbligo condannato
| 1. Utente Siep apre il menu a tendina per selezionare l'obbligo del condannato |
| --- |
| 2. SYSTEM visualizza l'elenco degli obblighi. In questo elenco è presente il nuovo obbligo "Partecipazione a percorsi di recupero" |
| 3. Utente Siep seleziona la nuova voce di menu "Partecipazione a percorsi di recupero" |
| 4. SYSTEM Chiude il  menu a tendina e visualizza la selezione dell'utente |



STEP 2
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

| Attori | Utente Siep |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIES.
L'utente è abilitato alla funzione di inserimento di una sospensione  condizionale della pena. |
| Punto d'innesco | SIEP\Dettaglio procedimento\iscrizione concessione benefici\pena sospesa non menzione (Ex artt. 163 165 c.p.) |
| Stato Base | N/A |

## Scenari
### Inserimento pena sospesa/non menzione
| 1. Utente Siep accede alla funzionalità "Concessione benefici\ pena sospesa" e seleziona, nel menu a tendina "Tipo Sospensione" la voce “Il giudice dispone che la pena rimanga sospesa subordinatamente all'adempimento dell'obbligo”. |
| --- |
| 2. SYSTEM visualizza il menu a tendina "Obblighi del condannato". |
| 3. Utente Siep seleziona la nuova voce “Partecipazione a percorsi di recupero”. |
| 4. Utente Siep digita gli anni di sospensione,  il termine adempimento obblighi nei campi "Anni", "Mesi" e "Giorni". |
| 5. Utente Siep digita l’ente (servizi socio-assistenziali del territorio) presso cui effettuare il percorso di recupero  nel campo "Tipologia Obbligo" |
| 6. Utente Siep preme il pulsante "Conferma". |
| 7. SYSTEM memorizza i dati nella banca dati. |


STEP 3-4-5
## Requisiti
REQ-SIE-008-01_FN.02 - Pena Sospesa non menzione (ex Art 163-165 c.p.) nuovo tipo di obbligo
## Gestione Pene Sospese - Richieste- Adempimento obblighi
ID: UC-SIE-008-01.03
L'utente, nella richiesta di adempimento obblighi del condannato, gestisce il nuovo obbligo. I dati del nuovo obbligo sono recuperati dal sistema se è presente il beneficio, altrimenti possono essere inseriti mediante questa funzionalità.

| Attori | Utente Siep |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente è abilitato alla gestione degli adempimenti obblighi del condannato
Il procedimento è stato validato |
| Punto d'innesco | SIEP\Gestione Pene Sospese\Richieste\Notizie adempimento Obblighi |
| Stato Base | N/A |

## Scenari
### Adempimento obblighi in assenza di iscrizione beneficio
| 1. Utente Siep accede alla funzionalità "Gestione pene sospese - Richieste- Notizie Adempimento Obblighi" |
| --- |
| 2. SYSTEM visualizza la maschera dei dati da digitare |
| 3. Utente Siep digita i dati, apre il menu a tendina Tipologia Obbligo del condannato e seleziona la nuova voce “Partecipazione a percorsi di recupero” |
| 4. SYSTEM presenta il nuovo campo Ente/Struttura |
| 5. Utente Siep digita nel nuovo campo Ente/Struttura i dati della struttura presso cui il condannato adempirà all'obbligo, inserisce i campi obbligatori e preme il pulsante "Conferma" |
| 6. SYSTEM memorizza i dati nella banca dati, impostando lo stato del procedimento con il valore "Notizie adempimento obblighi" e presenta la maschera di dettaglio con i dati inseriti. |

### Adempimento obblighi in presenza di iscrizione beneficio
| 1. Utente Siep accede alla funzionalità "Gestione pene sospese - Richieste- Notizie Adempimento Obblighi" |
| --- |
| 2. SYSTEM visualizza la maschera dei dati da digitare. Se esiste il solo beneficio di sospensione condizionale della pena subordinata all'obbligo di "Partecipazione a percorsi di recupero", il sistema visualizza l'obbligo nella voce "Tipologia obbligo" del condannato" e l'ente oppure la struttura di recupero nel nuovo campo "Ente/Struttura". |
| 3. Utente Siep digita gli altri campi obbligatori e preme il pulsante "Conferma" |
| 4. SYSTEM memorizza i dati nella banca dati, impostando lo stato del procedimento con il valore "Notizie adempimento obblighi" e presenta la maschera di dettaglio con i dati inseriti. |



STEP 2

### Adempimento obblighi in presenza di iscrizione beneficio - modifica valori
| 1. Utente Siep accede alla funzionalità "Gestione pene sospese - Richieste- Notizie Adempimento Obblighi" |
| --- |
| 2. SYSTEM visualizza la maschera dei dati da digitare. Se esiste il solo beneficio di sospensione condizionale della pena subordinata all'obbligo di "Partecipazione a percorsi di recupero", il sistema visualizza l'obbligo nella voce "Tipologia obbligo" del condannato e l'ente oppure la struttura di recupero nel nuovo campo "Ente/Struttura". |
| 3. Utente Siep modifica il  valore del campo "Tipologia obbligo" del condannato selezionando un altro valore |
| 4. SYSTEM ripulisce il valore del campo "Ente/Struttura" |
| 5.  Utente Siep digita gli altri campi obbligatori e preme il pulsante "Conferma" |
| 6. SYSTEM visualizza un messaggio informativo che segnala la incongruenza tra i dati digitati e il beneficio presente in banca dati e invita l'utente a scegliere se continuare con l'inserimento oppure annullare l'operazione |
| 7. Utente Siep annulla l'operazione |
| 8. SYSTEM ripristina i valori nei campi obblighi del condannato e, se presente, il valore nel campo Ente/Struttura |
| 9. Utente Siep digita gli altri campi obbligatori e preme il pulsante "Conferma" |
| 10. SYSTEM memorizza i dati nella banca dati, impostando lo stato del procedimento con il valore "Notizie adempimento obblighi" e presenta la maschera di dettaglio con i dati inseriti |

## Requisiti
REQ-SIE-008-01_FN.04 - Notizie Adempimento Obblighi - nuovo tipo di obbligo in assenza di beneficio
REQ-SIE-008-01_FN.03 - Notizie Adempimento Obblighi - nuovo tipo di obbligo in presenza di beneficio presente
## Stampa Richiesta adempimento obblighi
ID: UC-SIE-008-01.04
L'utente, nella stampa della Richiesta di adempimento obblighi, ritrova le informazioni sul nuovo obbligo del condannato e la struttura presso cui il condannato adempirà all'obbligo.

| Attori |  |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente ha inserito una richiesta di adempimento obblighi con un beneficio di sospensione condizionale della pena subordinata all'obbligo di partecipazione a percorsi di recupero. |
| Punto d'innesco | SIEP\Gestione Pene Sospese\Richieste\Notizie adempimento obblighi |
| Stato Base | N/A |

## Scenari
### Adempimento obblighi - stampa
| 1. Utente Siep accede al dettaglio dell'adempimento. |
| --- |
| 2. Utente Siep preme il pulsante "Stampa". |
| 3. SYSTEM produce la stampa del provvedimento di richiesta. I dati della stampa riportano il nuovo obbligo del condannato, il termine adempimento obbligo e il tipo di obbligo. |




STEP 3
## Requisiti
REQ-SIE-008-01_FN.05 - Notizie Adempimento Obblighi: Stampa
## Gestione Pene Sospese - Richieste-Determinazione termini
ID: UC-SIE-008-01.05
L'utente, nella richiesta di determinazione dei termini per l'obbligo del condannato, gestisce il nuovo obbligo. I dati del nuovo obbligo sono recuperati dal sistema se è presente il beneficio e la richiesta di adempimento, altrimenti possono essere inseriti mediante questa funzionalità.

| Attori | Utente Siep |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente è abilitato alla gestione delle richieste di determinazione termini del condannato |
| Punto d'innesco | Gestione Pene Sospese/Richieste/Determinazione Termini |
| Stato Base | N/A |

## Scenari
### Determinazione termini in assenza di iscrizione beneficio
| 1. Utente Siep accede alla funzionalità "Gestione pene sospese - Richieste - Determinazione Termini" |
| --- |
| 2. SYSTEM visualizza la maschera dei dati da digitare |
| 3. Utente Siep digita i dati, apre il menu a tendina Tipologia Obbligo del condannato e seleziona la nuova voce “Partecipazione a percorsi di recupero” |
| 4. SYSTEM presenta il nuovo campo Ente/Struttura |
| 5. Utente Siep digita nel nuovo campo Ente/Struttura i dati della struttura presso cui il condannato adempirà all'obbligo, inserisce i campi obbligatori e preme il pulsante "Conferma" |
| 6. SYSTEM memorizza i dati nella banca dati, impostando lo stato del procedimento con il valore "Richiesta determinazione termini" e presenta la maschera di dettaglio con i dati inseriti. |

### Determinazione termini in presenza di iscrizione beneficio
| 1. Utente Siep accede alla funzionalità "Gestione pene sospese - Richieste - Determinazione termini" |
| --- |
| 2. SYSTEM visualizza la maschera dei dati da digitare. Se esiste il solo beneficio di sospensione condizionale della pena subordinata all'obbligo di "Partecipazione a percorsi di recupero", il sistema visualizza l'obbligo nella voce "Tipologia obbligo" del condannato", l'ente oppure la struttura di recupero nel nuovo campo "Ente/Struttura" e l'ufficio che ha emesso il provvedimento di esecuzione nel campo "Ufficio del Giudice" . |
| 3. Utente Siep digita gli altri campi obbligatori e preme il pulsante "Conferma" |
| 4. SYSTEM memorizza i dati nella banca dati, impostando lo stato del procedimento con il valore "Richiesta determinazione termini" e presenta la maschera di dettaglio con i dati inseriti. |



STEP 2

### Determinazione termini in presenza di iscrizione beneficio - modifica valori
| 1. Utente Siep accede alla funzionalità "Gestione pene sospese - Richieste- Richiesta Determinazione termini" |
| --- |
| 2. SYSTEM visualizza la maschera dei dati da digitare. Se esiste il solo beneficio di sospensione condizionale della pena subordinata all'obbligo di "Partecipazione a percorsi di recupero", il sistema visualizza l'obbligo nella voce "Tipologia obbligo" del condannato, l'ente oppure la struttura di recupero nel nuovo campo "Ente/Struttura" e l'ufficio che ha emesso il provvedimento di esecuzione nel campo "Ufficio del Giudice". |
| 3. Utente Siep modifica il  valore del campo "Tipologia obbligo" del condannato selezionando un altro valore |
| 4. SYSTEM ripulisce il valore del campo "Ente/Struttura" e il campo "Ufficio del Giudice" |
| 5.  Utente Siep digita gli altri campi obbligatori e preme il pulsante "Conferma" |
| 6. SYSTEM visualizza un messaggio informativo che segnala la incongruenza tra i dati digitati e il beneficio presente in banca dati e invita l'utente a scegliere se continuare con l'inserimento oppure annullare l'operazione |
| 7. Utente Siep annulla l'operazione |
| 8. SYSTEM ripristina i valori nei campi obblighi del condannato e, se presenti, il valore nel campo Ente/Struttura e nel campo "Ufficio de del Giudice" |
| 9. Utente Siep digita gli altri campi obbligatori e preme il pulsante "Conferma" |
| 10. SYSTEM memorizza i dati nella banca dati, impostando lo stato del procedimento con il valore "Richiesta determinazione termini" e presenta la maschera di dettaglio con i dati inseriti |

## Dettaglio tecnico di intervento
## Requisiti
REQ-SIE-008-01_FN.07 - Richiesta Determinazione Termini in assenza di beneficio
REQ-SIE-008-01_FN.06 - Richiesta Determinazione Termini in presenza di beneficio
## Stampa Richiesta Determinazione Termini
ID: UC-SIE-008-01.06
L'utente, nella stampa della Richiesta di  determinazione termini, ritrova le informazioni sul nuovo obbligo del condannato e la struttura presso cui il condannato adempirà all'obbligo.

| Attori |  |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente ha inserito una richiesta di determinazione termini con un beneficio di sospensione condizionale della pena subordinata all'obbligo di partecipazione a percorsi di recupero. |
| Punto d'innesco | Gestione Pene Sospese/Richieste/Determinazione Termini |
| Stato Base | N/A |

## Scenari
### Richiesta determinazione termini - stampa
| 1. Utente Siep accede al dettaglio della richiesta determinazione termini |
| --- |
| 2. Utente Siep preme il pulsante "Stampa". |
| 3. SYSTEM produce la stampa del provvedimento di richiesta. I dati della stampa riportano il nuovo obbligo del condannato, il termine adempimento obbligo e il tipo di obbligo. |



STEP 3

## Requisiti
REQ-SIE-008-01_FN.08 - Richiesta Determinazione Termini in assenza di beneficio - –tampa
## Selezione Tipo di Provvedimento
ID: UC-SIE-008-01.08
Nel menu a tendina Tipo di Provvedimento devono essere presenti due opzioni: "Sentenza", "Provvedimento".

| Attori |  |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP
L'utente è abilitato alla funzionalità di inserimento di revoca beneficio ex art. 168 c.p.p. |
| Punto d'innesco | SIEP\Gestione Pene Sospese\Richieste\Revoca beneficio ex art. 168 c.p.p. |
| Stato Base | N/A |

## Scenari
### Selezione Tipo Provvedimento
| 1. Utente Siep apre il menu a tendina per selezionare il tipo di provvedimento |
| --- |
| 2. SYSTEM visualizza l'elenco dei tipi di provvedimento. In questo elenco sono presenti i valori "Sentenza", "Provvedimento" |
| 3. Utente Siep seleziona la nuova voce di menu "Provvedimento" |
| 4. SYSTEM Chiude il  menu a tendina e visualizza la nuova sezione "Notizia di adempimento agli obblighi" |




STEP 2

## Requisiti
REQ-SIE-008-01_FN.12 - Selezione Tipo di provvedimento: Sentenza, Provvedimento
## Gestione Pene Sospese - Richieste - Revoca beneficio ex art.168 c.p. - 674 c.p.p.
ID: UC-SIE-008-01.07
Nella maschera di gestione della revoca dei benefici l'utente può selezionare due tipi di Provvedimento: Sentenza, Provvedimento.
Se l'utente seleziona "Sentenza", la maschera si presenta come è attualmente; se l'utente seleziona "provvedimento", la maschera presenterà, in sola visualizzazione, i dati della notizia di adempimento obblighi relativi al mancato adempimento degli obblighi del condannato, se presenti in banca dati.


| Attori | Utente Siep |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente è abilitato alla funzionalità di gestione pene sospese. |
| Punto d'innesco | SIEP\Gestione Pene Sospese\Richieste\Revoca beneficio ex art. 168 c.p.p. |
| Stato Base | N/A |

## Scenari
### Revoca beneficio ex art. 168 c.p.p. in presenza di notizia di mancato adempimento agli obblighi
| 1. Utente Siep accede alla funzione di revoca del beneficio e seleziona il tipo di provvedimento "Provvedimento" |
| --- |
| 2. SYSTEM visualizza la nuova sezione in cui sono visualizzati i dati della notizia di adempimento obblighi la cui decisione è "mancato adempimento agli obblighi" |
| 3. Utente Siep inserisce i dati obbligatori e preme il pulsante "Conferma" |
| 4. SYSTEM Memorizza i data nella banca dati |



STEP 2
PER EMMA: NELLA PAGINA RIMANE LA SELEZIONE DEL PROVVEDIMENTO DALLA LISTA? (VEDI LINK SOTTO TIPO PROVVEDIMENTO)
### Revoca beneficio ex art. 168 c.p.p. in assenza di notizia di mancato adempimento agli obblighi
| 1. Utente Siep l'utente ripete lo step 1 del precedente scenario |
| --- |
| 2. SYSTEM non trova la notizia di adempimento obblighi con decisione "Mancato adempimento obblighi" |
| 3. SYSTEM Visualizza un messaggio di errore bloccante che informa l'utente che non esiste un provvedimento di mancato adempimento agli obblighi |
| 4. Utente Siep preme il pulsante OK |
| 5. SYSTEM ritorna alla maschera del provvedimento di revoca |

## Requisiti
REQ-SIE-008-01_FN.13 - Revoca Beneficio ex art. 168 c.p.p. - Provvedimento
## Scadenzario Termini Ottemperanza Obblighi
ID: UC-SIE-008-01.09
Lo scadenzario Termini Ottemperanza Obblighi deve riportare l'elenco di tutti i procedimenti di classe III con beneficio subordinato agli obblighi, inclusi quelli in cui è previsto il nuovo obbligo (Partecipazione a percorsi di recupero) e non aventi un provvedimento di revoca del beneficio ex art. 168 c.p.  e 674 c.p.p.
Nel tab  'Tutti' e ‘In Scadenza’ sono visualizzati i procedimenti, con beneficio subordinato agli obblighi, che scadono nei 30 giorni successivi alla data di visualizzazione, anziché nei 7 giorni successivi.

| Attori | Utente Siep |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
Nella banca dati è presente almeno un procedimento di classe III con scadenza successiva di al massimo 30 giorni alla data di visualizzazione e avente un beneficio subordinato agli obblighi.
Nella banca dati è presente almeno un procedimento di classe III con il beneficio di sospensione e il nuovo obbligo "Partecipazione a percorsi di recupero", avente data scadenza al massimo di 30 giorni successivi alla data di visualizzazione. |
| Punto d'innesco | SIEP\Scadenziari\Termini Ottemperanza Obblighi |
| Stato Base | N/A |

## Scenari
### Scadenzario Termine Ottemperanza Obblighi
| 1. Utente Siep accede alla funzionalità e imposta i criteri di ricerca 'In scadenza' e preme il pulsante "Ricerca" |
| --- |
| 2. SYSTEM visualizza i procedimenti aventi la scadenza entro i 30 giorni dalla data attuale e aventi una richiesta di beneficio della sospensione condizionale della pena subordinata agli obblighi |
| 3. SYSTEM include nell'elenco il procedimento avente una richiesta di sospensione condizionale della pena subordinata al nuovo obbligo "Partecipazione a percorsi di recupero". |

### Scadenzario Termine Ottemperanza Obblighi - revoca
| 1. Utente Siep accede alla funzionalità e imposta i criteri di ricerca 'In scadenza' e preme il pulsante "Ricerca" |
| --- |
| 2. SYSTEM visualizza i procedimenti aventi la scadenza entro i 30 giorni dalla data attuale e aventi una richiesta di beneficio della sospensione condizionale della pena subordinata agli obblighi |
| 3. SYSTEM non include nell'elenco il procedimento avente una richiesta di sospensione condizionale della pena subordinata al nuovo obbligo "Partecipazione a percorsi di recupero" perché per questo procedimento è presente un provvedimento di revoca ex art. 168 c.p. e 674 c.p.p.. |

## Requisiti
REQ-SIE-008-01_FN.14 - Scadenzario Termini Ottemperanza Obblighi - Richieste
REQ-SIE-008-01_FN.15 - Scadenzario Termini Ottemperanza Obblighi - Revoca beneficio ex art. 168 c.p. - 674 c.p.p.
## Scadenzario Termini Sospensione condizionale
ID: UC-SIE-008-01.10
Lo scadenzario Termini Sospensione Condizionale deve riportare l'elenco di tutti i procedimenti di classe III, inclusi quelli in cui è previsto il beneficio con il nuovo obbligo (Partecipazione a percorsi di recupero) e non aventi un provvedimento di revoca del beneficio ex art. 168 c.p. e 674 c.p.p..
Nel tab  'Tutti' e ‘In Scadenza’ sono visualizzati i procedimenti, con beneficio della sospensione pena, che scadono nei 30 giorni successivi alla data di visualizzazione, anziché nei 7 giorni successivi.

| Attori | Utente Siep |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
Nella banca dati è presente almeno un procedimento di classe III con scadenza successiva di al massimo 30 giorni alla data di visualizzazione e avente un beneficio subordinato agli obblighi.
Nella banca dati è presente almeno un procedimento di classe III con il beneficio di sospensione e il nuovo obbligo "Partecipazione a percorsi di recupero", avente data scadenza al massimo di 30 giorni successivi alla data di visualizzazione. |
| Punto d'innesco | SIEP\Scadenzari\Termini Sospensione Condizionale |
| Stato Base | N/A |

## Scenari
### Scadenzario Termini Sospensione condizionale
| 1. Utente Siep accede alla funzionalità e imposta i criteri di ricerca 'In scadenza' e preme il pulsante "Ricerca" |
| --- |
| 2. SYSTEM visualizza i procedimenti aventi la scadenza entro i 30 giorni dalla data attuale e aventi una richiesta di beneficio della sospensione condizionale della pena subordinata agli obblighi |
| 3. SYSTEM include nell'elenco il procedimento avente una richiesta di sospensione condizionale della pena subordinata al nuovo obbligo "Partecipazione a percorsi di recupero". |

### Scadenzario Termini Sospensione condizionale - revoca
| 1. SYSTEM visualizza i procedimenti aventi la scadenza entro i 30 giorni dalla data attuale e aventi una richiesta di beneficio della sospensione condizionale della pena subordinata agli obblighi |
| --- |
| 2. SYSTEM non include nell'elenco il procedimento avente una richiesta di sospensione condizionale della pena subordinata al nuovo obbligo "Partecipazione a percorsi di recupero" perché per questo procedimento è presente un provvedimento di revoca ex art. 168 c.p.. e 674 c.p.p.. |

## Requisiti
REQ-SIE-008-01_FN.16 - Scadenzario Termini Sospensione Condizionale
REQ-SIE-008-01_FN.17 - Scadenzario Termini Sospensione Condizionale - Revoca beneficio ex art. 168 c.p. e 674 c.p.p.
## Gestione Pene Sospese - estinzione reato
ID: UC-SIE-008-01.11
All'atto dell'inserimento di un provvedimento di richiesta estinzione reato, il sistema deve aggiornare lo stato del procedimento con i seguenti valori:
Estinzione reato ex art.167 c.p. se l'utente ha selezionato, nel menu a tendina "Articolo", il valore Estinzione reato ex art.167 c.p. ;
Estinzione reato ex art.445 c.2 c.p.p. se l'utente ha selezionato, nel menu a tendina "Articolo", il valore Estinzione reato ex art.445 c.2 c.p.p.

| Attori | Utente Siep |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente è abilitato alla gestione delle richieste di estinzione reato. |
| Punto d'innesco | SIEP\Gestione Pene Sospese\Richieste\Richiesta Estinzione Reato |
| Stato Base | N/A |

## Scenari
### Richiesta Estinzione reato ex art. 167 c.p.
| 1. Utente Siep accede alla funzionalità e inserisce una richiesta. Nel menu a tendina "Articolo" seleziona "Estinzione reato ex art.167 c.p.", seleziona la motivazione “Per Adempimento obblighi ex art. 165 c.p.”, digita i campi obbligatori e preme il pulsante "Conferma" |
| --- |
| 2. SYSTEM memorizza i campi nella banca dati e aggiorna lo stato del procedimento con il valore "Estinzione reato ex art.167 c.p." |



STEP 1

### Richiesta Estinzione reato ex art. 445 c.2 c.p.p.
| 1. Utente Siep accede alla funzionalità e inserisce una richiesta. Nel menu a tendina "Articolo" seleziona "Estinzione reato ex art. 445 c.2 c.p.p.", digita i campi obbligatori e preme il pulsante "Conferma" |
| --- |
| 2. SYSTEM memorizza i campi nella banca dati e aggiorna lo stato del procedimento con il valore "Estinzione reato ex art. 445 c.2 c.p.p." |

## Requisiti
REQ-SIE-008-01_FN.09 - Richiesta Estinzione reato ex art. 167c.p. - nuovo stato procedimento
REQ-SIE-008-01_FN.10 - Richiesta Estinzione reato ex art.445 c.2 c.p.p. - nuovo stato procedimento
## Stampa richiesta estinzione reato
ID: UC-SIE-008-01.12
L'utente, nella stampa della Richiesta di estinzione reato, ritrova le informazioni sul nuovo obbligo del condannato e la struttura presso cui il condannato adempirà all'obbligo.

| Attori |  |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente ha inserito una richiesta di estinzione reato ex art. 167 c.p. per adempimento obbligo di partecipazione a percorsi di recupero |
| Punto d'innesco | Gestione Pene Sospese/Richieste/Estinzione Reato |
| Stato Base | N/A |

## Scenari
### Richiesta estinzione reato - stampa
| 1. Utente Siep accede al dettaglio della richiesta di estinzione reato |
| --- |
| 2. Utente Siep preme il pulsante "Stampa". |
| 3. SYSTEM produce la stampa del provvedimento di richiesta. I dati della stampa riportano il nuovo obbligo del condannato, il termine adempimento obblighi e il tipo di obbligo. |



STEP 3

PER EMMA: LA STAMPA DA CAMBIARE CON I DATI DELLOBBLIGO è QUELLA RELATIVA ALL’ART. 167, QUANDO SI SELEZIONA ADEMPIMENTO OBBLIGO nella MOTIVAZIONE? (VEDI IMMAGINE SCENARIO PRECEDENTE)

## Requisiti
REQ-SIE-008-01_FN.11 - Richiesta estinzione reato - stampa
## Stampa Copertina
ID: UC-SIE-008-01.13
L'utente, nella stampa della copertina, ritrova le informazioni sul nuovo obbligo del condannato, il termine adempimento obblighi, il tipo obbligo e la struttura presso cui frequentare il percorso di recupero.

| Attori | Utente Siep |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente ha inserito una pena sospesa e ha selezionato il nuovo tipo di obbligo "Partecipazione a percorsi di recupero". |
| Punto d'innesco | SIEP\Istruttorie\Richieste - Stampa copertina |
| Stato Base | N/A |

## Scenari
### Stampa copertina
| 1. Utente Siep accede alla funzionalità di stampa del procedimento. |
| --- |
| 2. SYSTEM visualizza la maschera di ricerca del procedimento. |
| 3. Utente Siep imposta i dati di ricerca e preme il pulsante ricerca. |
| 4. SYSTEM visualizza il procedimento |
| 5. Utente Siep preme il pulsante "Stampa". |
| 6. SYSTEM produce la stampa della copertina. I dati della stampa riportano il nuovo obbligo del condannato, il termine adempimento obblighi e il tipo di obbligo. |



STEP 6

## Requisiti
REQ-SIE-008-01_FN.18 - Stampa copertina: dati relativi al nuovo tipo di obbligo
## Certificato Esecuzione
ID: UC-SIE-008-01.14
L'utente, nella stampa del certificato esecuzione, ritrova le informazioni sul nuovo obbligo del condannato, il termine adempimento obblighi e la struttura presso cui frequentare il percorso di recupero.

| Attori | Utente Siep |
| --- | --- |
| Precondizioni | L'utente è abilitato all'acceso al sistema SIEP.
L'utente è abilitato alla funzionalità Stato esecuzione - Certificato esecuzione
Il procedimento deve essere validato |
| Punto d'innesco | SIEP\Stato Esecuzione\Certificato Esecuzione |
| Stato Base | N/A |

## Scenari
### Certificato Esecuzione
| 1. Utente Siep accede alla funzionalità Stato Esecuzione nel menu principale |
| --- |
| 2. SYSTEM mostra il procedimento e il menu orizzontale |
| 3. Utente Siep seleziona la funzionalità Certificato Esecuzione |
| 4. SYSTEM Mostra il pulsante di stampa e i campi in cui specificare la destinazione del file di stampa |
| 5. Utente Siep imposta i dati e preme il pulsante Stampa |
| 6. SYSTEM produce la stampa del certificato esecuzione. I dati della stampa riportano il nuovo obbligo del condannato, il termine adempimento obblighi e il tipo di obbligo. |



STEP 6
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
È necessario pertanto apportare le modifiche alle funzionalità di dettaglio del procedimento, alle funzionalità di gestione delle istruttorie di cumulo e alla funzionalità di trasferimento per competenza.

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

| Attori | Utente Siep |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente ha aperto il dettaglio del Procedimento. |
| Punto d'innesco | SIEP\Dettaglio Procedimento |
| Stato Base | N/A |

## Scenari
### Utente titolare del procedimento: nuova funzionalità nel menu
| 1. Utente Siep apre il menu del dettaglio procedimento |
| --- |
| 2. SYSTEM visualizza l'elenco delle funzionalità disponibili. Nell'elenco è presente la nuova voce "Gestione Parte offesa/Difensore". |



STEP 2

### Utente titolare del cumulo: nuova funzionalità nel menu
| 1. Utente Siep apre il menu del dettaglio cumulo |
| --- |
| 2. SYSTEM visualizza l'elenco delle funzionalità disponibili. Nell'elenco è presente la nuova voce "Gestione Parte offesa/Difensore". |



STEP 2

### Utente NON titolare del procedimento: nuova funzionalità nel menu
| 1. Utente Siep apre il menu del dettaglio procedimento |
| --- |
| 2. SYSTEM visualizza l'elenco delle funzionalità disponibili. Nell'elenco NON  è presente la nuova voce "Gestione Parte offesa/Difensore". |




STEP 2

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

| Attori | Utente Siep |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
Per il procedimento è presente almeno una parte offesa. |
| Punto d'innesco | SIEP |
| Stato Base | N/A |

## Scenari
### ufficio titolare procedimento - link gestione parte offesa
| 1. Utente Siep  ricerca un procedimento |
| --- |
| 2. SYSTEM visualizza il dettaglio del procedimento |
| 3. SYSTEM visualizza, accanto ai dati anagrafici del condannato, il link Gestione Parte offesa |
| 4. Utente Siep l'utente clicca sul link Gestione Parte offesa |
| 5. SYSTEM richiama la funzionalità di visualizzazione dell'elenco delle parti offese associate al procedimento (vedi caso d'uso Gestione parti offese - elenco) in cui è possibile gestire le parti offese |



STEP 3

### ufficio titolare cumulo - link gestione parte offesa
| 1. Utente Siep  ricerca un cumulo |
| --- |
| 2. SYSTEM visualizza il dettaglio del cumulo |
| 3. SYSTEM visualizza, accanto ai dati anagrafici del condannato, il link Gestione Parte offesa |
| 4. Utente Siep l'utente clicca sul link Gestione Parte offesa |
| 5. SYSTEM richiama la funzionalità di visualizzazione dell'elenco delle parti offese associate al procedimento (vedi caso d'uso gestione parti offese - elenco) in cui è possibile gestire le parti offese |



STEP 3
### ufficio NON titolare procedimento - link gestione parte offesa
| 1. Utente Siep  ricerca un procedimento |
| --- |
| 2. SYSTEM visualizza il dettaglio del procedimento |
| 3. SYSTEM NON visualizza, accanto ai dati anagrafici del condannato, il link Gestione Parte offesa |

## Requisiti
REQ-SIE-008-02_FN.08 - Dettaglio Procedimento - link Gestione Parte offesa
REQ-SIE-008-02_FN.09 - Dettaglio procedimento - visibilità link Gestione parte offesa

## Inserimento parte offesa
ID: UC-SIE-008-02.03
La nuova funzionalità permette di inserire una o più parti offese.

| Attori |  |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente appartiene all'ufficio titolare del procedimento. |
| Punto d'innesco | SIEP\Dettaglio Procedimento |
| Stato Base | N/A |

## Scenari
### Inserimento prima parte offesa
| 1. Utente Siep accede al dettaglio del procedimento e apre il menu delle funzionalità |
| --- |
| 2. SYSTEM visualizza l'elenco delle funzionalità disponibili. nel menu è presente la funzionalità Gestione parte offesa/Difensore |
| 3. Utente Siep seleziona la voce di menu Gestione parte offesa/Difensore |
| 4. SYSTEM visualizza la maschera di inserimento dei dati anagrafici della parte offesa |
| 5. Utente Siep inserisce i dati obbligatori e preme il pulsante Conferma |
| 6. SYSTEM presenta la maschera di dettaglio della parte offesa in cui sono presenti le informazioni appena inserite e quelle da inserire riguardanti la domiciliazione delle notifiche al difensore |
| 7. SYSTEM presenta anche il link Gestione Difensore |
| 8. Utente Siep preme il pulsante Conferma |
| 9. SYSTEM memorizza i dati anagrafici della parte offesa e presenta il dettaglio delle informazioni |
| 10.  Utente Siep preme il pulsante per ritornare indietro |
| 11. SYSTEM  presenta la maschera con l’elenco delle persone offese e tasti Azione (vedi caso d’uso Gestione parti offese - elenco) |



STEP 4


STEP 6-7


STEP 9

STEP 11

### Inserimento altre parti offese
| 1. Utente Siep accede al dettaglio del procedimento e apre il menu delle funzionalità |
| --- |
| 2. SYSTEM visualizza l'elenco delle funzionalità disponibili. Nel menu è presente la funzionalità Gestione parte offesa/Difensore |
| 3. Utente Siep seleziona la voce di menu Gestione parte offesa/Difensore |
| 4. SYSTEM visualizza l'elenco delle parti offese associate al procedimento |
| 5. Utente Siep clicca sul pulsante Inserimento |
| 6. SYSTEM presenta la maschera di inserimento dei dati anagrafici della parte offesa. |
| 7. Utente Siep inserisce i dati obbligatori e preme il pulsante Conferma |
| 8. SYSTEM presenta la maschera di dettaglio della parte offesa in cui sono presenti le informazioni da inserire riguardanti la domiciliazione delle notifiche al difensore |
| 9. SYSTEM visualizza anche il link Gestione difensore |
| 10. Utente Siep preme il pulsante Conferma |
| 11. SYSTEM memorizza i dati nella banca dati e visualizza il dettaglio delle informazioni |
| 12. Utente Siep preme il link per ritornare indietro |
| 13. SYSTEM presenta l’elenco delle parti offese associate al procedimento (vedi caso d'uso Gestione parti offese - elenco) |
|  |



STEP 4

STEP 13
## Requisiti
REQ-SIE-008-02_FN.03 - Inserimento parte offesa
## Visualizzazione dettaglio parte offesa
ID: UC-SIE-008-02.04
La funzione permette di visualizzare il dettaglio dei dati anagrafici della parte offesa.

| Attori |  |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente appartiene all'ufficio titolare del procedimento.
L'utente ha aperto il dettaglio del Procedimento e ha selezionato "Gestione parte offesa/difensore" oppure ha cliccato sul link "Gestione Parte offesa" presente sul procedimento.
L'utente ha inserito almeno una parte offesa. |
| Punto d'innesco | SIEP\Dettaglio Procedimento\Gestione Parte offesa/Difensore oppure 
SIEP\Dettaglio Procedimento\link Gestione Parte offesa |
| Stato Base | N/A |

## Scenari
### Visualizzazione dettaglio parte offesa
| 1. Utente Siep clicca sul link “Dettagli” in corrispondenza di un nominativo presente nell'elenco |
| --- |
| 2. SYSTEM visualizza la maschera di dettaglio dei dati anagrafici della parte offesa. i dati sono solo in visualizzazione. |
| 3. SYSTEM visualizza, nella parte bassa della maschera, l'elenco dei difensori, se associati |
| 4. Utente Siep preme l'icona per ritornare indietro |
| 5. SYSTEM chiude la maschera al ritorna alla maschera di elenco delle persone offese |



STEP 2-3
## Requisiti
REQ-SIE-008-02_FN.05 - Visualizzazione dettaglio parte offesa
## Modifica parte offesa
ID: UC-SIE-008-02.05
La funzionalità permette di modificare i dati anagrafici di una parte offesa.

| Attori |  |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente appartiene all'ufficio titolare del procedimento.
L'utente ha aperto il dettaglio del Procedimento e ha selezionato "Gestione parte offesa/difensore" oppure ha cliccato sul link "Gestione Parte offesa" presente sul procedimento.
L'utente ha inserito almeno una parte offesa. |
| Punto d'innesco | SIEP\Dettaglio Procedimento\Gestione Parte offesa/Difensore oppure 
SIEP\Dettaglio Procedimento\link Gestione Parte offesa |
| Stato Base | N/A |

## Scenari
### Modifica dati parte offesa
| 1. Utente Siep seleziona una parte offesa e clicca sul link "Modifica" |
| --- |
| 2. SYSTEM presenta la maschera di dettaglio dei dati anagrafici della parte offesa. Tutti i campi sono editabili. |
| 3. Utente Siep modifica i dati e preme il pulsante "Conferma" |
| 4. SYSTEM aggiorna i dati nella banca dati e presenta la maschera di dettaglio della parte offesa aggiornando i dati |

## Requisiti
REQ-SIE-008-02_FN.06 - Modifica parte offesa
## Cancellazione parte offesa
ID: UC-SIE-008-02.06
La funzionalità permette di cancellare i dati anagrafici di una parte offesa.

| Attori |  |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente appartiene all'ufficio titolare del procedimento.
L'utente ha aperto il dettaglio del Procedimento e ha selezionato "Gestione parte offesa/difensore" oppure ha cliccato sul link "Gestione Parte offesa" presente sul procedimento.
L'utente ha inserito almeno una parte offesa. |
| Punto d'innesco | SIEP\Dettaglio Procedimento\Gestione Parte offesa/Difensore oppure 
SIEP\Dettaglio Procedimento\link Gestione Parte offesa |
| Stato Base | N/A |

## Scenari
### Cancellazione parte offesa
| 1. Utente Siep seleziona una parte offesa e clicca sul link "Cancella" |
| --- |
| 2. SYSTEM  chiede all'utente conferma dell'operazione di cancellazione. |
| 3. Utente Siep conferma |
| 4. SYSTEM effettua la cancellazione dei dati della parte offesa, i dati di associazione a uno o più difensori, aggiornando i dati presenti nell'elenco |

## Requisiti
REQ-SIE-008-02_FN.07 - Cancellazione parte offesa
## Gestione parti offese - elenco
ID: UC-SIE-008-02.07
La funzione permette di visualizzare l'elenco delle parti offese associate al procedimento.
Nella maschera sono presenti i link per il dettaglio, l'inserimento, la modifica  e cancellazione dei dati di una parte offesa e per la modifica dei difensori.
| Attori |  |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente appartiene all'ufficio titolare del procedimento.
L'utente ha aperto il dettaglio del Procedimento e ha selezionato "Gestione parte offesa/difensore" oppure ha cliccato sul link "Gestione Parte offesa" presente sul procedimento.
L'utente ha inserito almeno una parte offesa. |
| Punto d'innesco | SIEP\Dettaglio Procedimento\Gestione Parte offesa/Difensore oppure
SIEP\Dettaglio Procedimento\link "Gestione Parte offesa" |
| Stato Base | N/A |

## Scenari
### Gestione parti offese - elenco
| 1. SYSTEM visualizza l'elenco delle parti offese associate al procedimento. |
| --- |
| 2. SYSTEM visualizza, in corrispondenza di ciascun nominativo, il link per il dettaglio, l’inserimento, la Modifica, Cancellazione di una parte offesa e per la modifica dei difensori |




STEP 2
## Requisiti
REQ-SIE-008-02_FN.04 - Visualizzazione elenco parti offese
## Assegnazione difensore parte offesa
ID: UC-SIE-008-02.08
La funzionalità permette di assegnare un difensore alla parte offesa.
È possibile assegnare al massimo due difensori.
È possibile assegnare un difensore già censito nella banca dati oppure inserire i dati di un nuovo difensore.
Si precisa che nella fase di analisi di dettaglio sarà possibile integrare l'eventuale chiamata al RegInde per il reperimento dei dati degli avvocati censiti nel suddetto registro.

| Attori |  |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente appartiene all'ufficio titolare del procedimento.
L'utente ha inserito almeno una parte offesa. |
| Punto d'innesco | SIEP\Dettaglio procedimento\Gestione parte offesa |
| Stato Base | N/A |

## Scenari
### Assegnazione primo difensore con nuovi dati
| 1. Utente Siep clicca sul link Gestione Difensore |
| --- |
| 2. SYSTEM visualizza la maschera di inserimento o selezione di un difensore |
| 3. Utente Siep preme il pulsante Inserimento |
| 4. SYSTEM  presenta la maschera di inserimento dei dati |
| 5. Utente Siep inserisce i dati obbligatori e preme il pulsante Associa |
| 6. SYSTEM memorizza i dati del difensore e presenta la maschera di dettaglio del difensore e i campi in cui integrare le informazioni |
| 7. Utente Siep seleziona "Di fiducia" |
| 8. SYSTEM presenta il campo di nomina con la data corrente, editabile |
| 9. Utente Siep preme il pulsante Conferma |
| 10. SYSTEM assegna il difensore alla parte offesa e presenta la maschera di dettaglio dei dati del difensore |
| 11. Utente Siep preme il pulsante per ritornare alla pagina precedente |
| 12. SYSTEM presenta la maschera contenente in testa i dati della parte offesa e l'elenco dei difensori della parte offesa (Vedi caso d'uso Difensori parte offesa - elenco) |



STEP 4


STEP 6


STEP 10


STEP 12

### Assegnazione difensore presente in banca dati
| 1. Utente Siep clicca sul link Gestione parte offesa |
| --- |
| 2. SYSTEM visualizza la maschera di inserimento o selezione dei dati del difensore. |
| 3. Utente Siep preme il link Seleziona dalla lista |
| 4. SYSTEM apre la maschera di ricerca di un difensore |
| 5. Utente Siep inserisce i dati di ricerca e preme il pulsante Cerca |
| 6. SYSTEM presenta l'elenco dei difensori corrispondenti ai criteri di ricerca impostati |
| 7. Utente Siep seleziona un difensore dalla lista |
| 8. SYSTEM ritorna alla pagina di inserimento dei dati del difensore e presenta il menu a tendina per selezionare il tipo difensore |
| 9. Utente Siep seleziona "Di fiducia" |
| 10. SYSTEM presenta il campo di nomina con la data corrente, editabile |
| 11. Utente Siep preme il pulsante Conferma |
| 12. SYSTEM assegna il difensore alla parte offesa e presenta la maschera di dettaglio dei dati del difensore |
| 13. Utente Siep preme il pulsante per ritornare alla pagina precedente |
| 14. SYSTEM presenta la maschera contenente in testa i dati della parte offesa e l'elenco dei difensori della parte offesa (Vedi caso d'uso Gestione difensore parte offesa - elenco) |


STEP 6


STEP 14

### Assegnazione altro difensore
| 1. Utente Siep seleziona una parte offesa e preme il link Modifica difensore |
| --- |
| 2. SYSTEM presenta la maschera contenente l'elenco dei difensori della parte offesa (vedi caso d'uso Gestione difensore - elenco) |
| 3. Utente Siep preme il pulsante Assegnazione |
| 4. SYSTEM apre la maschera di inserimento di un difensore mediante la digitazione di nuovi dati oppure mediante la selezione di un difensore già censito nel sistema (vedi scenari precedenti) |


### Assegnazione difensore oltre numero massimo
| 1. Utente Siep seleziona una parte offesa e preme il link Modifica Difensore |
| --- |
| 2. SYSTEM presenta la maschera contenente l'elenco dei difensori della parte offesa (vedi caso d'uso Gestione difensore - elenco) |
| 3. Utente Siep preme il pulsante Assegnazione |
| 4. SYSTEM controlla il numero dei difensori assegnati alla parte offesa e verificato che sono presenti già due difensori presenta un messaggio di errore che informa l'utente che il numero massimo di difensori è due |



STEP 4
## Requisiti
REQ-SIE-008-02_FN.11 - Assegnazione difensore parte offesa - inserimento dati
REQ-SIE-008-02_FN.12 - Assegnazione difensore parte offesa - selezione da lista
REQ-SIE-008-02_FN.13 - Assegnazione difensore selezionato
REQ-SIE-008-02_FN.14 - Limite numero difensori assegnati
## Gestione difensore - Elenco
ID: UC-SIE-008-02.09
La funzionalità permette di visualizzare l'elenco dei difensori della parte offesa.
Nella maschera sono presenti i pulsanti di de assegnazione, assegnazione o sostituzione di un difensore.

| Attori |  |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente appartiene all'ufficio titolare del procedimento.
L'utente ha inserito almeno una parte offesa. |
| Punto d'innesco | SIEP\Dettaglio Procedimento\Gestione Parte offesa/Difensore\Gestione parti offese - elenco
SIEP\Dettaglio Procedimento\link Gestione Parte offesa\Gestione parti offese – elenco |
| Stato Base | N/A |

## Scenari
### Gestione Difensore
| 1. Utente Siep clicca sul link Modifica difensore in corrispondenza del nominativo di una parte offesa presente nell'elenco |
| --- |
| 4. SYSTEM apre la maschera contenente l'elenco dei difensori associati alla parte offesa. Sono presenti i pulsanti di Assegnazione, Deassegnazione, Sostituzione |


STEP 2
## Requisiti
REQ-SIE-008-02_FN.10 - Gestione difensore parte offesa - elenco
## Deassegnazione difensore
ID: UC-SIE-008-02.10
La funzione permette di eliminare l'assegnazione di un difensore della parte offesa.

| Attori |  |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente appartiene all'ufficio titolare del procedimento.
L'utente ha inserito almeno una parte offesa. |
| Punto d'innesco | SIEP\Dettaglio procedimento\Gestione parte offesa |
| Stato Base | N/A |

## Scenari
### De assegnazione difensore
| 1. Utente Siep clicca sul link Modifica difensore di una parte offesa |
| --- |
| 2. SYSTEM presenta la maschera con l'elenco dei difensori |
| 3. Utente Siep seleziona un difensore e clicca sul pulsante "Deassegnazione" |
| 6. SYSTEM effettua la cancellazione dell'associazione tra il difensore e la parte offesa e visualizza un messaggio informativo |
| 7. Utente Siep preme OK |
| 8. SYSTEM chiude la maschera e ritorna all'elenco dei difensori aggiornando i dati |



STEP 2


STEP 6



STEP 8
## Requisiti
REQ-SIE-008-02_FN.15 - De assegnazione difensore parte offesa
## Sostituzione difensore
ID: UC-SIE-008-02.11
La funzionalità deve permettere di sostituire un difensore assegnato alla parte offesa.

| Attori |  |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente appartiene all'ufficio titolare del procedimento.
L'utente ha inserito almeno una parte offesa. |
| Punto d'innesco | SIEP\Dettaglio procedimento\Gestione parte offesa |
| Stato Base | N/A |

## Scenari
### Sostituzione difensore
| 1. Utente Siep clicca sul link Modifica difensore di una parte offesa |
| --- |
| 2. SYSTEM presenta la maschera contenente l'elenco dei difensori della parte offesa (vedi caso d'uso Gestione difensori - Elenco) |
| 3. Utente Siep seleziona un difensore e preme il pulsante Sostituzione |
| 4. SYSTEM apre la maschera di assegnazione di un difensore mediante la digitazione di nuovi dati oppure mediante la selezione di un difensore già censito nel sistema (vedi caso d'uso Assegnazione difensore) |
| 5. Utente Siep effettua i passi descritti in uno degli scenari del caso d'uso Assegnazione difensore |
| 6. SYSTEM elimina l'associazione tra il difensore selezionato e la parte offesa |
| 7. Utente Siep preme l'icona per tornare indietro |
| 8. SYSTEM chiude la maschera e ritorna all'elenco aggiornato dei difensori |




STEP 2


STEP 8
## Requisiti
REQ-SIE-008-02_FN.16 - Sostituzione difensore parte offesa

## Apertura istruttoria Cumulo - replica parti offese/difensori
ID: UC-SIE-008-02.12
La funzionalità di apertura Istruttoria Cumulo, oltre alla replica dei dati del titolo coinvolto, replicherà anche i dati delle persone offese e dei rispettivi difensori.
L'attuale funzionalità sarà pertanto modificata.

| Attori | Utente Siep |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente appartiene all'ufficio titolare del procedimento.
Il procedimento coinvolto nel cumulo contiene almeno una parte offesa. |
| Punto d'innesco | SIEP |
| Stato Base | N/A |

## Scenari
### Apertura istruttoria Cumulo: replica dati persona offesa e difensori
| 1. Utente Siep preme il pulsante Cumulo |
| --- |
| 2. SYSTEM apre la maschera di ricerca del procedimento da inserire nel cumulo |
| 3. Utente Siep ricerca il procedimento e, nella maschera presentata dal sistema, preme il pulsante "Apertura Istruttoria" |
| 4. SYSTEM presenta la maschera di riepilogo dei dati del procedimento da inserire nel cumulo  e il pulsante di conferma apertura Istruttoria |
| 5. Utente Siep preme il pulsante "Conferma" |
| 6. SYSTEM replica i dati del titolo coinvolto nel Cumulo e replica anche i dati delle persone offese e dei rispettivi difensori |
| 7. Utente Siep apre l'istruttoria e clicca sul link Elenco titoli coinvolti |
| 8. SYSTEM presenta la maschera con l'elenco dei titoli coinvolti |
| 9. Utente Siep clicca sul link dettaglio di un procedimento dell'elenco |
| 10. SYSTEM presenta la maschera con i pulsanti funzione |
| 11. Utente Siep preme il pulsante "Dati Analitici" |
| 12. SYSTEM presenta la maschera con i pulsanti funzione. È presente il nuovo pulsante "Gestione parte offesa/Difensore" |

## Requisiti

REQ-SIE-008-02_FN.17 - Apertura istruttoria Cumulo - dati persone offese e difensori
## Cumulo - Gestione dati analitici
ID: UC-SIE-008-02.13
Per ciascun procedimento coinvolto nel Cumulo è possibile gestire i dati delle persone offese e dei rispettivi difensori mediante la nuova funzionalità richiamata mediante il pulsante " Dati Analitici - Gestione parte offesa/difensore".

| Attori | Utente Siep |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente appartiene all'ufficio titolare del cumulo.
Il procedimento coinvolto nel cumulo contiene almeno una parte offesa. |
| Punto d'innesco | SIEP\Dettaglio Cumulo\Elenco titoli coinvolti\Dettaglio dati analitici |
| Stato Base | N/A |

## Scenari
### Dettaglio dati analitici - gestione parte offesa/difensore
| 1. Utente Siep preme il pulsante Dati Analitici |
| --- |
| 2. SYSTEM visualizza i pulsanti di gestione. È  presente il nuovo pulsante "Gestione parte offesa/difensore" |
| 3. Utente Siep clicca sul pulsante "Gestione parte offesa/difensore" |
| 4. SYSTEM visualizza l'elenco delle parti offese. Nella colonna "Azioni" sono presenti i link per l’inserimento, la modifica, la modifica dei difensori e la cancellazione della parte offesa |
| 5. Utente Siep preme il link "Modifica Difensore" in corrispondenza di una parte offesa |
| 6. SYSTEM visualizza l'elenco dei difensori e i pulsanti "Deassegnazione", Sostituzione", "Assegnazione" |
| 7. Utente Siep apporta le modifiche e conferma |
| 8. SYSTEM memorizza i dati legati al cumulo, lasciando invariati i dati originari |


## Requisiti

REQ-SIE-008-02_FN.18 - Cumulo- dati analitici titoli coinvolti



STEP 2


STEP 4
## Requisiti
REQ-SIE-008-02_FN.18 - Cumulo- dati analitici titoli coinvolti
## Trasferimento per competenza
ID: UC-SIE-008-02.14
La funzionalità di trasferimento per competenza deve prevedere il trasferimento anche dei dati della persona offesa e dei rispettivi difensori.
L'ufficio destinatario del procedimento diventa pertanto titolare dei dati della persona offesa e del difensore, ha visibilità e possibilità di gestione degli stessi.
L’attuale funzionalità sarà pertanto modificata

| Attori | Utente Siep |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente appartiene all'ufficio titolare del procedimento.
Il procedimento coinvolto contiene almeno una parte offesa e un difensore. |
| Punto d'innesco | SIEP/Istruttorie Richieste |
| Stato Base | N/A |

## Scenari
### Trasferimento per competenza - visibilità e gestione persona offesa/difensore
| 1. Utente Siep clicca sul pulsante Trasmissione per competenza/Seguito Atti |
| --- |
| 2. SYSTEM presenta la maschera in cui inserire i dati per il trasferimento |
| 3. Utente Siep esegue tutti i passi per trasferire il procedimento |
| 4. Utente Siep ufficio destinatario prende in carico il procedimento |
| 5. Utente Siep ufficio destinatario visualizza il link Persone Offese |
| 6. Utente Siep ufficio destinatario visualizza il link  Gestione Difensore |


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
Il messaggio informa l'utente che vi è obbligo di informare la persona offesa e, ove nominato, il difensore mediante apposita comunicazione.

| Attori | Utente Siep |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente è titolare del procedimento.
L'utente ha inserito un provvedimento di:
Evasione  
Scarcerazione  
Estinzione Reato  
Estinzione Pena  
Concessione, Sostituzione e Revoca di Misure Alternative  
Concessione, Sostituzione e Revoca di Misure di Sicurezza  
Provvedimenti di Variazione Pena
per almeno un reato interessato dalla legge 69/2019. |
| Punto d'innesco | SIEP |
| Stato Base | N/A |

## Scenari
### Validazione provvedimento - presenza persona offesa
| 1. Utente Siep preme il pulsante Valida. |
| --- |
| 2. SYSTEM Il sistema visualizza il messaggio che informa l'utente di inviare comunicazione alla persona offesa e, ove nominato al suo difensore e chiede conferma di lettura messaggio |
| 3. Utente Siep preme il pulsante ok |
| 4. SYSTEM valida il provvedimento |


### Validazione provvedimento - assenza persona offesa
| 1. Utente Siep preme il pulsante Valida. |
| --- |
| 2. SYSTEM valida il provvedimento |

## Requisiti
REQ-SIE-008-03_FN.01 - Alert comunicazione a persona offesa
## Generazione comunicazione
ID: UC-SIE-008-03.02
La nuova funzionalità permette di creare un atto per la comunicazione a ciascuna parte offesa e, ove presente, a ciascun difensore delle parti offese.
NOTA: nel presente documento si propone di richiamare la funzionalità nella maschera di validazione del provvedimento.
Tuttavia, si segnala la necessità di prevedere una funzionalità, inserita nel menu principale, che consenta di generare la comunicazione successivamente.

| Attori |  |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente è titolare del procedimento.
L'utente ha validato un provvedimento di:
Evasione  
Scarcerazione  
Estinzione Reato  
Estinzione Pena  
Concessione, Sostituzione e Revoca di Misure Alternative  
Concessione, Sostituzione e Revoca di Misure di Sicurezza  
Provvedimenti di Variazione Pena
per almeno un reato interessato dalla legge 69/2019. |
| Punto d'innesco | SIEP |
| Stato Base | N/A |

## Scenari
### Generazione comunicazione parte offesa/difensore
| 1. Utente Siep preme il pulsante Comunicazione parte offesa/difensore |
| --- |
| 2. SYSTEM apre una pagina per inserire i dati obbligatori propedeutici alla creazione del documento da stampare |
| 3. Utente Siep inserisce le informazioni (Autorità destinazione) e preme il pulsante Conferma |
| 4. SYSTEM salva i dati nella banca dati associando l'evento stampa al provvedimento |
| 5. SYSTEM presenta la pagina con i dati della stampa in sola visualizzazione e l'icona Stampa |

## Requisiti
REQ-SIE-008-03_FN.02 - Generazione comunicazione a parte offesa/difensore
## Stampa Comunicazione
ID: UC-SIE-008-03.03
La nuova funzionalità  permette la produzione della stampa della comunicazione, utilizzando un nuovo template.
NOTA: si precisa che il template sarà concordato con l'Amministrazione.

| Attori |  |
| --- | --- |
| Precondizioni | L'utente è abilitato all'accesso al sistema SIEP.
L'utente è titolare del procedimento.
L'utente ha validato un provvedimento di:
Evasione  
Scarcerazione  
Estinzione Reato  
Estinzione Pena  
Concessione, Sostituzione e Revoca di Misure Alternative  
Concessione, Sostituzione e Revoca di Misure di Sicurezza  
Provvedimenti di Variazione Pena
per almeno un reato interessato dalla legge 69/2019. |
| Punto d'innesco | SIEP |
| Stato Base | N/A |

## Scenari
### Stampa comunicazione parte offesa/difensore
| 1. Utente Siep clicca sul link Stampa Comunicazione parte offesa |
| --- |
| 2. SYSTEM produce la stampa utilizzando un nuovo template per ciascuna parte offesa e difensore. |

## Requisiti
REQ-SIE-008-03_FN.03 - Stampa comunicazione a persona offesa

#### Matrice tracciabilità

| Requisiti/Use Case | Alert comunicazione a persona offesa/difensore | Generazione comunicazione | Stampa Comunicazione |
| --- | --- | --- | --- |
| Alert comunicazione a persona offesa | X |  |  |
| Generazione comunicazione a parte offesa/difensore |  | X |  |
| Stampa comunicazione a persona offesa |  |  | X |



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