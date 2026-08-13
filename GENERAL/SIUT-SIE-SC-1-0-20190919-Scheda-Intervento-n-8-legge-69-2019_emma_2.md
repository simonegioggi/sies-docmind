---
uniqueName: siut-sie-sc-1-0-20190919-scheda-intervento-n-8-leg
displayName: "SIUT SIE SC 1 0 20190919 Scheda Intervento n 8 legge 69 2019 emma 2"
category: "GENERAL"
tags: []
---

# SIUT-SIE-SC-1.0-20190919 Scheda Intervento n.8 legge 69 2019_emma_2

> **File originale:** `MEV/SCHEDA_008/SIUT-SIE-SC-1.0-20190919 Scheda Intervento n.8 legge 69 2019_emma_2.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |



Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A  - Sirfin-PA nell’ambito del contratto CIG 73479643B7 per lo “SVILUPPO DEL SISTEMA INFORMATIVO UNITARIO TELEMATICO, LA MANUTENZIONE DEGLI ATTUALI SISTEMI DELL’AREA PENALE DEL MINISTERO DELLA GIUSTIZIA E SERVIZI CORRELATI. LOTTO 1”.



Elenco approvazioni per versione

| Versione | V. 1.0 del 19/09/2019 |
| --- | --- |
|  |  |
| Responsabile del Progetto | Paolo Ceccanti |
| Redatto da: | Stefania Barca |
| Verificato da | Vito Bufi |
| Approvato da | Vito Bufi |
| Data approvazione | 19/09/2019 |
| Livello di riservatezza | L3 |





INDICE DEI CONTENUTI
1.	INTRODUZIONE	7
1.1.	Scopo del documento	7
1.2.	Acronimi e Definizioni	7
1.2.1.	Acronimi	7
1.2.2.	Definizioni	8
1.2.3.	Riferimenti	8
3.	Definizione dell’Obiettivo	9
3.1.	Dettato normativo	9
3.2.	Convenzioni	10
3.3.	Elenco Requisiti	10
3.3.1.	REQ-AVP_FN.01	11
3.3.2.	REQ-AVP_FN.02	11
3.3.3.	REQ-AVP_FN.03	11
4.	Descrizione dell’Intervento	12
4.1.1.	Descrizione requisito REQ-AVP_FN.01	12
4.1.2.	Descrizione requisito REQ-AVP_FN.02	12
7.1.1.	Descrizione requisito REQ-AVP_FN.03	18
7.2.	Moduli sw	20
7.3.	Architettura	20
7.4.	Interfacce utente	20
7.5.	Basi dati	20
7.6.	WEB services	20
7.7.	XSD	20
7.8.	Configurazione	20
7.9.	Tutorial	20
8.	Piano delle attività	21
8.1.	Ciclo di sviluppo	21
8.2.	Piano delle attività	21
8.3.	Gantt	21
8.4.	Vincoli	23
8.5.	Luogo di lavoro	23
9.	Dimensionamento	24
9.1.	Stima dell'effort previsto	24


Lista di distribuzione

Amministrazione: RUP, DEC
RTI: RUF, Referente tecnico, Referente sviluppo, Referente CDC, Referente sicurezza, Referente qualità

Elenco versioni

| Versioni | Data Versione | Capitolo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 19/09/2019 |  | Prima Emissione |
| 1.1 | 07/10/2019 |  | Esplicitata in modo più dettagliata la realizzazione di ogni requisito |







# INTRODUZIONE
## Scopo del documento
La presente Scheda di Intervento costituisce lo strumento di supporto alla gestione complessiva delle attività previste per il presente intervento.
La Scheda di Intervento si articola in due sezioni:
Descrizione dell’Intervento, in cui vengono declinati obiettivi, ambito e approccio progettuale.
Piano delle attività, in cui viene presentato il piano delle attività con declinazione di tempi e costi dell’intervento.
L’intervento in oggetto rientra nel servizio MEV ed è classificato come “Intervento di adeguamento normativo alla Legge 19 luglio 2019, n. 69”.
## Acronimi e Definizioni
## Acronimi
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
| SAL | Stato Avanzamento Lavori |
| SGQ | Sistema di Gestione per la Qualità di Engineering Ingegneria Informatica S.p.A. |
| SGSI | Sistema di Gestione della Sicurezza Informatica |
| SICP | Sistema Informativo Cognizione Penale |
| SIEP | Sistema Informativo Esecuzione Penale |
| SIU | Sistema Informativo Unitario |
| SLA | Service Level Agreement |
| SM | Security Manager |
| SQL | Structured Query Language |
| SW | SoftWare |
| TT | Trouble Ticketing |
| VPN | Virtual Private Network |

## Definizioni
| Glossa | Sinonimo | Definizione |
| --- | --- | --- |
|  |  |  |
|  |  |  |
|  |  |  |

## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
|  | m_dg.DOG07AR.08082019.0000016.U_Nota_ Scheda_n.8_legge_69_2019 | Richiesta scheda intervento |


# Definizione dell’Obiettivo
Il presente documento è volto a descrivere l’intervento evolutivo da realizzarsi sul sistema SIEP al fine di adeguare il software alle disposizioni contenute nella legge 19 luglio 2019 n. 69. L’intervento non riguarda gli uffici dei minorenni.
## Dettato normativo
La Legge 19 luglio 2019 n. 69, recante “Modifiche al codice penale, al codice di procedura penale e altre disposizioni in materia di tutela delle vittime di violenza domestica e di genere” e denominata “Codice Rosso”, è entrata in vigore il 9 agosto u.s. e agisce su più settori con interventi sul codice penale, su quello di procedura penale, sul c.d. codice antimafia ( D.Lgvo n. 159/2011) e sull’ordinamento penitenziario.
Di seguito si riportano gli articoli della predetta legge, limitatamente agli interventi software richiesti dall’Amministrazione e riportati nella richiesta scheda di intervento [1.2.3 Riferimenti – 1].
“LEGGE 19 luglio 2019, n. 69
Modifiche al codice penale, al codice di procedura penale e altre disposizioni in materia di tutela delle vittime di violenza domestica e di genere. (19G00076) (GU n.173 del 25-7-2019)
Art. 6
Modifica all'articolo 165 del codice penale in materia di sospensione condizionale della pena
1. All'articolo 165 del codice penale, dopo il quarto comma e’ inserito il seguente: «Nei casi di condanna per i delitti di cui agli articoli 572, 609-bis, 609-ter, 609-quater, 609-quinquies, 609-octies e 612-bis, nonche' agli articoli 582 e 583-quinquies nelle ipotesi aggravate ai sensi degli articoli 576, primo comma, numeri 2, 5 e 5.1, e 577, primo comma, numero 1, e secondo comma, la sospensione condizionale della pena e' comunque subordinata alla partecipazione a specifici percorsi di recupero presso enti o associazioni che si occupano di prevenzione, assistenza psicologica e recupero di soggetti condannati per i medesimi reati».
2. Dall'attuazione delle disposizioni di cui al comma 1 non devono derivare nuovi o maggiori oneri a carico della finanza pubblica. Gli oneri derivanti dalla partecipazione ai corsi di recupero di cui all'articolo 165 del codice penale, come modificato dal citato comma 1, sono a carico del condannato.
Art. 15
Modifiche agli articoli 90-ter, 282-ter, 282-quater, 299 e 659 del codice di procedura penale
1. All'articolo 90-ter del codice di procedura penale e' aggiunto, in fine, il seguente comma: «1-bis. Le comunicazioni previste al comma 1 sono sempre effettuate alla persona offesa e al suo difensore, ove nominato, se si procede per i delitti previsti dagli articoli 572, 609-bis, 609-ter, 609-quater, 609-quinquies, 609-octies e 612-bis del codice penale, nonche' dagli articoli 582 e 583-quinquies del codice penale nelle ipotesi aggravate ai sensi degli articoli 576, primo comma, numeri 2, 5 e 5.1, e 577, primo comma, numero 1, e secondo comma, del codice penale».
2. Al comma 1 dell'articolo 282-ter del codice di procedura penale sono aggiunte, in fine, le seguenti parole: «, anche disponendo l'applicazione delle particolari modalita' di controllo previste dall'articolo 275-bis».
3. Al comma 1 dell'articolo 282-quater del codice di procedura penale, dopo le parole: «alla parte offesa» sono inserite le seguenti: «e, ove nominato, al suo difensore».
4. Al comma 2-bis dell'articolo 299 del codice di procedura penale, le parole: «al difensore della persona offesa o, in mancanza di questo, alla persona offesa» sono sostituite dalle seguenti: «alla persona offesa e, ove nominato, al suo difensore».
5. Dopo il comma 1 dell'articolo 659 del codice di procedura penale e' inserito il seguente: «1-bis. Quando a seguito di un provvedimento del giudice di sorveglianza deve essere disposta la scarcerazione del condannato per uno dei delitti previsti dagli articoli 572, 609-bis, 609-ter, 609-quater, 609-quinquies, 609-octies e 612-bis del codice penale, nonche' dagli articoli 582 e 583-quinquies del codice penale nelle ipotesi aggravate ai sensi degli articoli 576, primo comma, numeri 2, 5 e 5.1, e 577, primo comma, numero 1, e secondo comma, del codice penale, il pubblico ministero che cura l'esecuzione ne da' immediata comunicazione, a mezzo della polizia giudiziaria, alla persona offesa e, ove nominato, al suo difensore».
## Convenzioni
Sulla base degli ambiti di progetto e dei tipi di requisito, la convenzione per l’identificazione dei requisiti è riportata di seguito.
Ciascun requisito è individuato da un identificativo univoco nella forma [REQ-M_N.nn], dove:
REQ Requisito;
M identifica l’ambito;
N identifica il tipo di requisito;
nn è un progressivo numerico all’interno del tipo di requisito
In particolare, per il presente progetto verranno utilizzati i codici riportati nella tabella sottostante.
| CODICE AMBITO | CODICE TIPO | TIPO REQUISITO |
| --- | --- | --- |
| AVP | AR | Architetturale |
| AVP | CF | Configurazione |
| AVP | FN | Funzionale |
| AVP | UI | Interfaccia Utente |
| AVP | PR | Prestazionali |
| AVP | IN | Interoperabilità |
| AVP | SC | Sicurezza |
| AVP | TU | Tutorial |
| AVP | RG | Relazione Giuridica |

## Elenco Requisiti
Di seguito si riportano i requisiti espressi dall’Amministrazione  [1.2.3 Riferimenti – 1].
## REQ-AVP_FN.01
Gestire la sospensione condizionale della pena che, per i delitti indicati dalla legge, è subordinata alla partecipazione a specifici percorsi di recupero presso enti o associazioni.
## REQ-AVP_FN.02
Prevedere l’inserimento e la gestione della persona offesa e del suo difensore.
## REQ-AVP_FN.03
Gestire la notifica dell’atto alla persona offesa. In questo ambito dovrà essere prodotto apposito modulo, da concordare con l’Amministrazione.

# Descrizione dell’Intervento
Di seguito sono descritti gli interventi evolutivi individuati per ottemperare alle nuove disposizioni di legge.
## Descrizione requisito REQ-AVP_FN.01

A seguito dell’iscrizione di un procedimento di classe III, ovvero di un procedimento di Pena Sospesa, per l’adempimento di quanto previsto dalla legge in oggetto (legge 69/2019), occorre innanzitutto intervenire nella pagina di iscrizione della concessione del beneficio.

La pagina è accessibile dal menù presente in combo ’Iscrizione concessione benefici’, a partire dalla maschera di dettaglio di un procedimento di classe III, e poi selezionando il tasto Pena Sospesa non menzione (ex Art 163-165 cp).




In questa pagina, Selezionando nel ‘Tipo Sospensione’ il valore “il giudice dispone che la pena rimanga sospesa subordinatamente all'adempimento dell'obbligo”, si apre la combo Obblighi del condannato ex art 165 c.p.
In questa combo occorre aggiungere una nuova voce “Partecipazione percorsi di recupero”. La descrizione dell’ente (servizi socio-assistenziali del territorio presso cui effettuare il percorso di recupero) deve essere inserita nella text area ‘Tipologia Obbligo’, non essendo a conoscenza a priori di eventuali enti preposti a tale scopo sul territorio.
Si propone pertanto di ampliare la text area ad oggi presente per permettere di inserire una descrizione più estesa dell’ente.

Quanto presente in questa pagina: obbligo, tipologia obbligo ed anni/mesi/ giorni dei Termini Adempimento Obbligo dovranno essere riportati nel template della funzione Stampa Copertina (SIEP_COPERTINA.rtf) e nel template della funzione Certificato Esecuzione (Siep-Certificato_Esecuzione.rtf)

La gestione dei procedimenti di classe III è prevista nel menù, Gestione Pene Sospese, già in essere nell’applicazione.
A seguire esplicitiamo ciò che deve essere modificato nelle varie funzioni presenti nel menù Gestione Pene Sospese a seguito dell’introduzione del nuovo obbligo del condannato in relazione ai reati previsti dalla legge in oggetto 69/2019.

Nel maschera relativa al menù Gestione Pene Sospese » Richieste >Notizie Adempimento Obblighi nella combo  ‘Tipologia Obbligo’ occorre prevedere la nuova voce “Partecipazione percorsi di recupero”. Inoltre occorre aggiungere un nuovo campo dove riportare, cioè visualizzare, l’ente scelto in fase di inserimento del beneficio. La voce della ‘Tipologia Obbligo’ deve essere preimpostata con il valore scelto in fase di inserimento del beneficio.



In fase di inserimento di una richiesta di Notizie Adempimento Obblighi, prevedere un nuovo stato del procedimento denominato ‘Richiesta Notizie Adempimento Obblighi’.
L’obbligo e l’ente presso cui si svolge il percorso di recupero, deve essere riportato sulla stampa relativa alla richiesta di adempimento obbligo (SIEP_PS_RIC_NOT_ADE_OBBL.rtf ).

Nel maschera relativa al menù Gestione Pene Sospese » Richieste >Richiesta Determinazione Termini nella combo  ‘Tipologia Obbligo’ occorre prevedere la nuova voce “Partecipazione percorsi di recupero”. Inoltre occorre aggiungere un nuovo campo dove riportare, cioè visualizzare, l’ente scelto in fase di inserimento del beneficio.
La voce della ‘Tipologia Obbligo’ deve essere preimpostata con il valore scelto in fase di inserimento del beneficio, mentre il valore della combo ‘Ufficio del Giudice’ deve essere preimpostato con l’ufficio che ha emesso la sentenza in esecuzione.




In fase di inserimento di una richiesta di Determinazione Termini, prevedere un nuovo stato del procedimento denominato ‘Richiesta Determinazione Termini’.
L’obbligo e l’ente presso cui si svolge il percorso di recupero, deve essere riportato sulla stampa relativa alla richiesta di determinazione termini (SIEP_PS_RIC_DET_TER_ADE_OBBL.rtf ).

La maschera relativa al menù Gestione Pene Sospese » Richieste >Richiesta Estinzione Reato resta invariata.



Deve invece essere parametrizzato lo stampato (SIEP_PS_RIC_EST_REATO.rtf) in modo che venga riportato l’obbligo del condannato e l’ente di recupero.

In fase di inserimento di una Richiesta di Estinzione Reato, prevedere due tipologie di stato del procedimento:
Estinzione reato ex art.167 cp
Estinzione reato ex art.445 c.2 cpp
Lo stato assume un valore o l’altro in base all’articolo scelto in fase di inserimento della richiesta di estinzione del reato.

La maschera relativa alla funzione di Inserimento Richiesta Revoca Beneficio ex art.168 c.p. - 674 c.p.p, deve essere modificata secondo quanto sotto riportato:



Nella combo Tipo Provvedimento devono essere presenti le seguenti voci: ‘-’, ‘Sentenza’ e ‘Provvedimento’.
Se l’utente selezione la voce ‘Sentenza’ in maschera deve essere mostrata la sezione ‘Titolo che Determina la Revoca’ (come nell’ immagine su riportata).
Se l’utente selezione la voce ‘Provvedimento’ in maschera deve essere mostrata una nuova sezione, in sostituzione di quella presente per ‘sentenza’, in cui riportare gli estremi del provvedimento di Annotazione di Adempimento Obbligo, la cui decisione sia stata ‘Il condannato non ha ottemperato gli obblighi’.

La maschera relativa alla funzione Gestione Pene Sospese » Annotazione revoca beneficio ex art.168 c.p. - 674 c.p.p. resta invariata.

Attualmente, il sistema, in fase di inserimento di un’annotazione di revoca di beneficio ex art. 168 c.p.p. crea in automatico un nuovo titolo di classe I. Si è notato che a tale proposito NON tutti i provvedimenti presenti su classe III vengono replicati sul titolo I. Si chiede all’amministrazione se intervenire per fare in modo che tutti i provvedimenti (elenco PM) del titolo in classe III vengano replicati sul titolo di classe I.


I procedimenti di classe III con il beneficio per il nuovo obbligo devono apparire nello scadenziario di Scadenzario Termini Ottemperanza Obblighi e nello Scadenzario Termini Sospensione Condizionale.
Per tali scadenziari, nel tabulatore ‘In Scadenza’ saranno mostrati i procedimenti che scadono nei 30 giorni successivi.

I procedimenti di classe III per cui il condannato ha adempiuto agli obblighi NON devono apparire nello scadenziario Termini Ottemperanza Obblighi (devono essere rimossi in fase di emissione di provvedimento di adempimento obblighi e non in fase di richiesta adempimento obblighi).

Inoltre, il procedimento di classe III deve scomparire dallo Scadenzario Termini Ottemperanza obblighi e Scadenzario Termini Sospensione Condizionale quando venga inserito un provvedimento di revoca beneficio ex art.168 c.p. - 674 c.p.p.

Per quanto riguarda l’inclusione di tali procedimenti (classe III) in istruttoria di cumulo, le regole seguite, saranno le stesse ad oggi in essere per i classe III inclusi in cumulo.

## Descrizione requisito REQ-AVP_FN.02

Per poter gestire la persona offesa col relativo difensore, si prevedono i seguenti interventi:

A partire dalla maschera di Dettaglio Procedimento, sarà aggiunto un nuovo menù nella combo delle funzioni denominato ‘Gestione Parte Offesa/Difensore’.




Accedendo alla funzione ‘Gestione Parte Offesa/Difensore’ sarà mostrata la seguente pagina:



Dopo la Conferma si avrà la maschera:


In cui si avrà il riepilogo dei dati inseriti, il link relativo alla Gestione del Difensore ed una sezione in cui specificare se la comunicazione alla parte offesa debba essere effettuata presso il Domicilio del difensore oppure tramite Forze di Polizia.

Il link Gestione del Difensore riporterà alla maschera:



In cui sarà possibile Inserire o Selezionare un difensore già esistente: questa funzione sarà quella attualmente utilizzata in SIEP per ad esempio l’inserimento del Magistrato.

Dopo aver inserito il Difensore si tornerà alla gestione del difensore come di seguito riportato:



In cui si potrà eliminare l’assegnazione, sostituire il Difensore o Assegnare un nuovo Difensore.

Attraverso il tasto Indietro si tornerà alla maschera:



E dopo il tasto Conferma si avrà la maschera:



Da cui sarà possibile: Modifica la Parte Offesa, Modificare la Parte Offesa e il Difensore, Cancellare la Parte Offesa, Tornare Indietro.


Nella maschera di Dettaglio Procedimento, se è stata inserita una parte offesa, sarà previsto un link ‘Gestione Parte Offesa’ che porterà alla pagina di dettaglio della parte offesa.



Il dettaglio delle informazioni devono essere visibili solo all’ufficio che ha inserito la parte offesa e NON a tutti gli uffici del distretto.

La parte offesa deve essere portata anche sul cumulo qualora il procedimento su cui è stata inserita la parte offesa venga coinvolto in un cumulo.
Se il procedimento su cui è stata inserita una parte offesa viene inviato per competenza ad altro ufficio, e lo si inserisce come titolo in un cumulo, i dati della parte offesa devono essere visibili anche all’ufficio che emette il cumulo. In fase di trasferimento competenza, si deve portare tutto dietro: parte offesa, difensore e forza di polizia.
Quindi anche sul dettaglio del procedimento nato dal cumulo deve apparire il link della parte offesa e deve essere possibile vedere i dati della parte offesa e gestirli.

## Descrizione requisito REQ-AVP_FN.03

Per quanto attiene la gestione della notifica dell’atto alla persona offesa si interverrà nel seguente modo:
In fase di validazione dei seguenti provvedimenti:
Evasione
Scarcerazione
Estinzione Reato
Estinzione Pena
Concessione, Sostituzione e Revoca di Misure Alternative
Concessione, Sostituzione e Revoca di Misure di Sicurezza
Provvedimenti di Variazione Pena
il sistema deve avvertire l’utente che, se presente la parte offesa, deve essere inviata opportuna comunicazione.
E’ da concordare con l’amministrazione l’elenco completo e preciso delle tipologie di provvedimenti per i quali va inviata la comunicazione, il tipo di documento da redigere e dove agganciare la stampa della comunicazione.
Per meglio gestire le comunicazioni dii Fine Pena alla parte offesa, si propone anche di creare uno nuovo scadenziario ‘Scadenziario Parte Offesa’ in cui saranno riportati i procedimenti per i quali è stata inserita una parte offesa. Tale scadenziario è del tutto simile allo scadenziario di Fine Pena ad oggi già presente a sistema, ma che però afferisce solo procedimenti che hanno una parte offesa inserita. Per tale scadenziario può essere proposta anche una funzione di aggiorna quantum, per facilitare gli uffici nella gestione delle tempistiche entro il quale mandare la comunicazione alla parte.
## Moduli sw
L’intervento prevede la modifica dei seguenti moduli sw:
N.A.
## Architettura
N.A.
## Interfacce utente
Le interfacce utente da modificare o realizzare sono riportate nel paragrafo 4. Descrizione dell’intervento.
## Basi dati
Saranno apportate le modifiche alla tabella fascicolo_siep per creare un collegamento tra la persona offesa ed il fascicolo.  Sarà creata una nuova tabella con i dati della persona offesa.
## WEB services
N.A.
## XSD
N.A.
## Configurazione
N.A.
## Tutorial
N.A.



# Piano delle attività
## Ciclo di sviluppo
Il ciclo di sviluppo adottato è il waterfull.

## Piano delle attività
Il Piano di Lavoro si articola su un arco temporale di circa 2 mesi e l’avvio è legato all’approvazione della presente scheda di intervento. Il dettaglio delle attività sono riportate nel paragrafo 8.3
## Gantt
L’articolazione delle attività previste per l'intervento si sviluppa come di seguito indicato:







## Vincoli

N.A.

## Luogo di lavoro
L’intervento evolutivo sarà realizzato presso la sede del fornitore.
# Dimensionamento
## Stima dell'effort previsto

La stima ad oggi prevista è:

| ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  | Complessità | Complessità | Complessità | Complessità | Complessità | Complessità |  |  |
| Function Types | Function Types | Function Types |  |  | Low | Low | Avg | Avg | High | High | Function |  |
|  |  |  |  |  | quantità | peso | quantità | peso | quantità | peso | Point |  |
| External Input | External Input | External Input |  |  | 0 | 3 | 0 | 4 | 6 | 6 | 36 |  |
| External Output | External Output | External Output |  |  | 0 | 4 | 0 | 5 | 1 | 7 | 7 |  |
| External Inquiry | External Inquiry | External Inquiry |  |  | 0 | 3 | 0 | 4 | 3 | 6 | 18 |  |
| Internal Logical File | Internal Logical File | Internal Logical File | Internal Logical File |  | 1 | 7 | 0 | 10 | 0 | 15 | 7 |  |
| External Interface File | External Interface File | External Interface File | External Interface File |  | 0 | 5 | 0 | 7 | 0 | 10 | 0 |  |
|  |  |  |  |  |  |  |  |  |  | Totale Function Point (FP) | 68 | ADD |
|  |  |  |  |  |  |  |  |  |  |  |  |  |
| CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) |  |
|  |  |  |  |  | Complessità | Complessità | Complessità | Complessità | Complessità | Complessità |  |  |
| Function Types | Function Types | Function Types |  |  | Low | Low | Avg | Avg | High | High | Function |  |
|  |  |  |  |  | quantità | peso | quantità | peso | quantità | peso | Point |  |
| External Input | External Input | External Input |  |  | 0 | 3 | 0 | 4 | 3 | 6 | 18 |  |
| External Output | External Output | External Output |  |  | 0 | 4 | 0 | 5 | 0 | 7 | 0 |  |
| External Inquiry | External Inquiry | External Inquiry |  |  | 0 | 3 | 0 | 4 | 3 | 6 | 18 |  |
| Internal Logical File | Internal Logical File | Internal Logical File | Internal Logical File |  | 1 | 7 | 0 | 10 | 0 | 15 | 7 |  |
| External Interface File | External Interface File | External Interface File | External Interface File |  | 0 | 5 | 0 | 7 | 0 | 10 | 0 |  |
|  |  |  |  |  |  |  |  |  |  | Totale Function Point (FP) | 43 | CHGA |
|  |  |  |  |  |  |  |  |  |  |  |  |  |
| DEL - F u n z i o n i   E l i m i n a t e | DEL - F u n z i o n i   E l i m i n a t e | DEL - F u n z i o n i   E l i m i n a t e | DEL - F u n z i o n i   E l i m i n a t e | DEL - F u n z i o n i   E l i m i n a t e | DEL - F u n z i o n i   E l i m i n a t e | DEL - F u n z i o n i   E l i m i n a t e | DEL - F u n z i o n i   E l i m i n a t e | DEL - F u n z i o n i   E l i m i n a t e | DEL - F u n z i o n i   E l i m i n a t e | DEL - F u n z i o n i   E l i m i n a t e | DEL - F u n z i o n i   E l i m i n a t e |  |
|  |  |  |  |  | Complessità | Complessità | Complessità | Complessità | Complessità | Complessità |  |  |
| Function Types | Function Types | Function Types |  |  | Low | Low | Avg | Avg | High | High | Function |  |
|  |  |  |  |  | quantità | peso | quantità | peso | quantità | peso | Point |  |
| External Input | External Input | External Input |  |  | 0 | 3 | 0 | 4 | 0 | 6 | 0 |  |
| External Output | External Output | External Output |  |  | 0 | 4 | 0 | 5 | 0 | 7 | 0 |  |
| External Inquiry | External Inquiry | External Inquiry |  |  | 0 | 3 | 0 | 4 | 0 | 6 | 0 |  |
| Internal Logical File | Internal Logical File | Internal Logical File | Internal Logical File |  | 0 | 7 | 0 | 10 | 0 | 15 | 0 |  |
| External Interface File | External Interface File | External Interface File | External Interface File |  | 0 | 5 | 0 | 7 | 0 | 10 | 0 |  |
|  |  |  |  |  |  |  |  |  |  | Totale Function Point (FP) | 0 | DEL |




per un importo complessivo pari a:


|  | N° | € | Totale |
| --- | --- | --- | --- |
| ADD | 68 | 162 | 11.016,00 € |
| CHG | 43 | 81 | 3.483,00 € |
| DEL | 0 | 16,2 | -   € |
|  |  |  |  |
|  |  |  | 14.499,00 € |