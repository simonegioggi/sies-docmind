---
uniqueName: siut-sie-sc-1-1-2020xxxx-scheda-intervento-9-adegu
displayName: "SIUT SIE SC 1 1 2020xxxx Scheda intervento 9   Adeguamento al SIES DLGS 123 2018"
category: "GENERAL"
tags: []
---

# SIUT-SIE-SC-1.1-2020xxxx Scheda intervento 9 - Adeguamento al SIES DLGS 123_2018 e 121_2018(Dlgs 123_SIUS_MAGGIORENNI)

> **File originale:** `MEV/SCHEDA_009/scheda_intervento/SIUT-SIE-SC-1.1-2020xxxx Scheda intervento 9 - Adeguamento al SIES DLGS 123_2018 e 121_2018(Dlgs 123_SIUS_MAGGIORENNI).docx`  
> **Tipo:** DOCX

---



| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |  |
| --- | --- |
|  |





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.



Approvazioni
|  | Nominativo |
| --- | --- |
| Elaborato da | Emma Caporizzo, Vito Bufi |
| Verificato da | Vito Bufi |
| Approvato da | Paolo Ceccanti |
| Data approvazione | XX/XX/2020 |
| Livello di riservatezza | L3 |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 04/10/2019 |  | Prima Emissione |
| 1.1 | XX/XX/2020 |  | Seconda Emissione Scheda intervento per nota m_dg.DOG07AR.25_10_2019.0000096.U

Si procede con la definizione e la descrizione analitica degli interventi inerenti al solo Dlgs 123 del 2018 per quel che afferisce agli uffici maggiorenni della Sorveglianza. |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
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
| Fabio Gattamorta | RTI |  | Responsabile PMO |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Edoardo Lamuraglia | RTI |  | Referente qualità |
| Francesco Rosati | RTI |  | Referente qualità |


INDICE DEI CONTENUTI

1	Introduzione	7
1.1	Scopo del documento	7
1.2	Riferimenti	7
1.3	Glossario	8
1.3.1	Definizioni	8
1.3.2	Acronimi e abbreviazioni	8
2	Definizione dell’Obiettivo	10
2.1	Convenzioni	11
2.2	Elenco Requisiti	11
2.2.1	REQ-SIE-009-01	12
2.2.2	REQ-SIE-009-02	12
2.2.3	REQ-SIE-009-03	12
2.2.4	REQ-SIE-009-04	12
2.2.5	REQ-SIE-009-05	12
2.2.6	REQ-SIE-009-06	12
2.2.7	REQ-SIE-009-07	13
2.2.8	REQ-SIE-009-08	13
2.2.9	REQ-SIE-009-09	13
2.2.10	REQ-SIE-009-10	13
2.2.11	REQ-SIE-009-11	13
2.2.12	REQ-SIE-009-12	13
2.2.13	REQ-SIE-009-13	13
2.2.14	REQ-SIE-009-14	14
2.2.15	REQ-SIE-009-15	14
2.2.16	REQ-SIE-009-16	14
2.2.17	REQ-SIE-009-17	14
3	Descrizione dell’Intervento	15
3.1	Ambito Normativo	15
3.1.1	D.lgs. 123/2018	15
3.2	Adeguamento sistema SIUS d.lgs. 123/2018 (UFFICI MAGGIORENNI)	15
3.2.1	REQ-SIE-009-01 TDS - Concessione misure alternative (art. 678 comma 1-ter c.p.p.)	15
3.2.2	REQ-SIE-009-02 TDS - Emissione del Decreto Presidenziale di Designazione	20
3.2.3	REQ-SIE-009-03 TDS - Emissione Ordinanza Applicazione Provvisoria	23
3.2.4	REQ-SIE-009-04 TDS - Registrazione data Esecutività Ordinanza Applicazione Provvisoria	26
3.2.5	REQ-SIE-009-05 TDS - Provvedimento di Conferma Ordinanza Applicazione Provvisoria	28
3.2.6	REQ-SIE-009-06 TDS - Gestione Revoca Ammissione Provvisoria	30
3.2.7	REQ-SIE-009-07 TDS - Gestione Sostituzione della Misura Alternativa	33
3.2.8	REQ-SIE-009-08 UDS - TDS - Gestione Sospensione delle Pene Accessorie	35
3.2.9	REQ-SIE-009-09 - REQ-SIE-009-10 - REQ-SIE-009-11 (Statistiche Misura Alternativa - art. 678 comma 1-ter c.p.p.) )	39
3.2.10	REQ-SIE-009-12 UDS - Introduzione del contenuto ‘Lavoro Pubblica Utilità’	44
3.2.11	REQ-SIE-009-13 UDS - Integrazione del contenuto ‘Lavoro Esterno’	45
3.2.12	REQ-SIE-009-14 (UDS – TDS Integrazione Lista Mittenti)	46
3.2.13	REQ-SIE-009-15 (Aggiornamento Statistica Movimento Provvedimenti per Oggetti)	47
3.2.14	REQ-SIE-009-16 Modifica pagina richiesta atti istruttori	48
3.2.15	REQ-SIE-009-17 Statistica Atti Istruttori con Data Richiesta Restituzione	52
3.3	Moduli sw	54
3.4	Architettura	54
3.5	Interfacce utente	54
3.6	Basi dati	55
3.6.1	Base Dati - REQ-SIE-009-01 (TDS - Concessione misure alternative (art. 678 comma 1-ter c.p.p.))	55
3.6.2	Base Dati - REQ-SIE-009-02 (TDS - Emissione del Decreto Presidenziale di Designazione)	55
3.6.3	Base Dati - REQ-SIE-009-03 (TDS - Emissione Ordinanza Applicazione Provvisoria)	56
3.6.4	Base Dati - REQ-SIE-009-04 (TDS - Registrazione data Esecutività Ordinanza Applicazione Provvisoria)	57
3.6.5	Base Dati - REQ-SIE-009-05 (TDS - Provvedimento di Conferma Ordinanza Applicazione Provvisoria)	57
3.6.6	Base Dati - REQ-SIE-009-06 (TDS - Gestione Revoca Ammissione Provvisoria)	57
3.6.7	Dati - REQ-SIE-009-07 (TDS - Gestione Sostituzione della Misura Alternativa)	58
3.6.8	Base Dati - REQ-SIE-009-08 (UDS e TDS - Gestione Sospensione delle Pene Accessorie)	58
3.6.9	Base Dati - REQ-SIE-009-09	59
3.6.10	Base Dati - REQ-SIE-009-10	59
3.6.11	Base Dati - REQ-SIE-009-11	59
3.6.12	Base Dati - REQ-SIE-009-12 (UDS - Introduzione del contenuto ‘Lavoro Pubblica Utilità)	59
3.6.13	Base Dati - REQ-SIE-009-13 (UDS - Integrazione del contenuto ‘Lavoro Esterno’)	59
3.6.14	Base Dati - REQ-SIE-009-14 (UDS – TDS Integrazione Lista Mittente Atto)	60
3.6.15	Base Dati - REQ-SIE-009- 15 (Aggiornamento Statistica Movimento Provvedimenti per Oggetti)	60
3.6.16	Base Dati - REQ-SIE-009- 16 (Modifica pagina Richiesta Atti Istruttori)	60
3.6.17	Base Dati - REQ-SIE-009- 17 (Statistica Atti Istruttori con Data Restituzione)	60
3.7	WEB services	60
3.8	XSD	60
3.9	Configurazione	60
3.10	Tutorial	61
4	Piano delle attività	62
4.1	Ciclo di sviluppo	62
4.2	Piano delle attività	65
4.3	Gantt	66
4.4	Vincoli	66
4.5	Luogo di lavoro	66
5	Dimensionamento	67
5.1	Stima dell'effort previsto	67
5.2	Dettaglio costi	67




# Introduzione
## Scopo del documento
La presente Scheda di Intervento costituisce lo strumento di supporto alla gestione complessiva delle attività previste per un intervento.
La Scheda di Intervento si articola in due sezioni:
Descrizione dell’Intervento, in cui vengono declinati obiettivi, ambito ed approccio progettuale.
Piano delle attività, in cui viene presentato il piano delle attività con declinazione di tempi e costi dell’intervento.

L’intervento in oggetto rientra nel servizio di Manutenzione Evolutiva, è stato richiesto con comunicazione m_dg.DOG07AR.08082019.0000017.U ed è classificato come di seguito riportato:

| Scheda di Intervento | 2019_09 |
| --- | --- |
| Oggetto | Adeguamento normativo SIES al DLgs 123/18 e 121/18 |
| Complessità | Alta |
| Servizio | MEV |


Nell’ottica di snellire le attività di redazione dei documenti e di verifica degli interventi da parte dell’amministrazione, e di concerto con la stessa, tale scheda espone gli interventi relativi al solo decreto Dlgs.123/18 per MAGGIORENNI e relativamente agi uffici UDS e TDS.

## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF1 | m_dg.DOG07AR.08082019.0000017.U_Nota_ Scheda_n.9.docx.pdf | Richiesta Scheda di Intervento |
| RIF2 | m_dg.DOG07AR.25_10_2019.0000096.U_Richiesta Riemissione _ Nota_Schedanr9SIES.docx_signed.pdf | Nota per Riemissione della Scheda di Intervento |
| RIF3 | SIUT-SIE-SC-1.0-20191004 Scheda intervento 9 - Adeguamento al SIES DLGS 123_2018 e 121_2018.docx | Prima versione della Scheda intervento |
| RIF4 | SIES-SIUS-ModificheDecretoLegislativon.123.doc | Documento dei requisiti fornito dal GdL SIES allegato alla Richiesta Scheda di Intervento |



## Glossario
## Definizioni
| Definizione | Descrizione |
| --- | --- |
|  |  |
|  |  |

## Acronimi e abbreviazioni
| Sigla | Descrizione |
| --- | --- |
| AgID | Agenzia per l’Italia Digitale |
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
| HW | HardWare |
| ICT | Information & Communication Technology |
| ISO | International Organization for Standardization |
| ISP | Information Security Policy |
| IT | Information Technology |
| KPI | Key Performance Indicator |
| MAAC | MAndatory Access Control |
| MAC | MAnutenzione Correttiva |
| MEV | Manutenzione EVolutiva |
| OWASP | Open Web Application Security Project |
| PA | Pubblica Amministrazione |
| PEC | Posta Elettronica Certificata |
| PDCA | Plan, Do, Check, Act |
| PdQ | Piano della Qualità |
| PdP | Piano di Progetto |
| PdS | Piano della Sicurezza |
| PMO | Program Management Office |
| POO | Program Operating Office |
| QM | Quality Manager |
| RA | Risk Assessment |
| RID | Riservatezza, Integrità, Disponibilità |
| RM | Resource Manager |
| RPO | Recovery Point Objective |
| RTO | Recovery Time Objective |
| RTI | Raggruppamento Temporaneo di Impresa |
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
| TT | Trouble Ticketing |
| UTA | Utente Generico Amministrazione |
| VPN | Virtual Private Network |


# Definizione dell’Obiettivo
Nell’ambito del progetto SIES si chiede di intervenire per adeguare il sistema a seguito del D.lgs. 123/18 e del D.lgs. 121/18.

In relazione al D.lgs. 123/18, la novità più significativa riguarda l’art. 4 comma 1 lett. B) nr. 3 del suddetto decreto che aggiunge il comma 1 ter all’art. 678 c.p.p.
Esso ridimensiona l’ambito di operatività del procedimento di sorveglianza per quanto riguarda la concessione di misure alternative.
Qualora la pena da scontare per i soggetti che hanno beneficiato della sospensione dell’ordine di esecuzione, ai sensi dell’art. 656 comma 5 c.p.p. (c.d.” liberi sospesi”) non sia superiore a 18 mesi è stata attribuita al magistrato “relatore” (designato secondo le procedure tabellari) il potere di decidere in via provvisoria sulle istanze di misura alternativa, con ordinanza emessa senza formalità, entro un termine assegnato dal Presidente del Tribunale.
Se l’ordinanza viene emessa, la sua esecutività resta sospesa per il termine di giorni 10 entro i quali gli interessati (condannato, suo difensore o pubblico ministero da individuarsi nel procuratore generale ex art. 678 comma 3 c.p.p.) possono fare opposizione nel qual caso si procede con rito ordinario.
Si procede, altresì, con il rito ordinario se il magistrato non emette ordinanza.
In caso di emissione dell’ordinanza di concessione di misure alternative decorso il termine per l’opposizione, il Tribunale si riunisce in camera di consiglio e senza formalità (da intendersi senza la presenza delle parti e presumibilmente con decreto) procede alla conferma del provvedimento provvisorio.
Se il Tribunale decide di non confermare l’ordinanza del magistrato, non emette alcun provvedimento motivato ma fissa l’udienza affinché si proceda con il rito ordinario.

Altre modifiche di rilievo attengono al potere del Tribunale di Sorveglianza, nell’ambito del procedimento di revoca delle misure alternative, di decidere anche in ordine all’eventuale sostituzione della misura con un’altra di diversa natura (art. 51 ter novellato) o il potere dello stesso magistrato di sorveglianza di eseguire (e non solo adottare) il provvedimento di cessazione della misura alternativa divenuta non più ammissibile, con il conseguente accompagnamento in Istituto penitenziario direttamente disposto dal Giudice (art. 51 bis novellato).

Sulle pene accessorie (il nuovo articolo 51 quater) è prevista, inoltre, la loro esecuzione anche in pendenza di una misura alternativa e non solo all’esito della stessa, salvo che il giudice di sorveglianza né disponga la sospensione per prevalenti esigenze di reinserimento. In caso di revoca della misura il Tribunale dovrà poi decidere anche sulle pene accessorie, se in corso di esecuzione, ed eventualmente computarne il periodo già espiato.
Il decreto sopramenzionato ha, anche, inserito il nuovo art. 20 ter dell’ordinamento penitenziario che disciplina il lavoro di pubblica utilità.

A seguire si riportano le descrizioni dell’intervento inerenti all’adeguamento del sistema SIES limitatamente al D.lgs. 123/18 per gli uffici della sorveglianza (TDS e UDS) per maggiorenni.

## Convenzioni
Sulla base degli ambiti di progetto e dei tipi di requisito, la convenzione per l’identificazione dei requisiti è riportata di seguito.
Ciascun requisito è individuato da un identificativo univoco nella forma [REQ-SIS-nnn-mm], dove:
REQ Requisito;
SIS identifica il sistema (cfr. SIUT-GEN-SN-2.2-20191023-Standard di nomenclatura);
nnn è il numero della scheda di richiesta intervento;
mm è il numero progressivo del requisito espresso dall’Amministrazione.

## Elenco Requisiti
Gli interventi di questo obiettivo possono riassumersi nei requisiti funzionali di seguito descritti, ed attengono a quanto richiesto nel documento “m_dg.DOG07AR.08082019.0000017.U_Nota_ Scheda_n.9.docx.pdf” [RIF1] e che fanno riferimento al D.lgs. 2018/123 per gli uffici della sorveglianza (TDS e UDS) per maggiorenni descritto nella definizione dell’obiettivo.
## REQ-SIE-009-01
In relazione all’articolo 678 c.p.p. comma 1 ter, introdotto con D.lgs. 123/2018, gli uffici Tribunali di Sorveglianza (TDS) devono essere abilitati all’emissione di un’ordinanza di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’.
## REQ-SIE-009-02
In relazione all’articolo 678 c.p.p. comma 1 ter, il Presidente del Tribunale di Sorveglianza (TDS), in tema di semplificazione della procedura, designa, dopo aver acquisito i documenti e le necessarie informazioni, il magistrato relatore per l’emissione un’ordinanza di ammissione provvisoria per una misura alternativa di all'articolo 656, comma 5.
## REQ-SIE-009-03
In relazione all’articolo 678 c.p.p. comma 1 ter, introdotto con D.lgs. 123/2018, il magistrato designato può emettere un’ordinanza di ammissione provvisoria ad una misura alternativa, di cui all’articolo 656, comma 5.
## REQ-SIE-009-04
Caratterista fondamentale dell’ordinanza di ammissione provvisoria è la sua non immediata esecutività.
Con il requisito in oggetto il sistema deve prevedere una nuova funzione che permetta al magistrato designato di poter inserire la data a partire dalla quale l’ordinanza di ammissione provvisoria della misura diverrà esecutiva.
## REQ-SIE-009-05
Emissione del provvedimento di conferma dell’applicazione provvisoria della misura da parte del Tribunale di Sorveglianza. Il sistema deve permettere di inserire il provvedimento di conferma sia come Ordinanza che come Decreto.
## REQ-SIE-009-06
In concomitanza all’ammissione provvisoria della misura, il sistema deve prevedere la gestione della revoca dell’ammissione provvisoria. La revoca della misura alternativa può intervenire a seguito di gravi violazioni delle prescrizioni nel corso dell’esecuzione provvisoria oppure perché, ad esempio, il collegio non condivide la decisione del magistrato designato.
## REQ-SIE-009-07
A seguito della nuova formulazione dell’art. 51 ter O.P., il Tribunale di Sorveglianza può decidere non solo, come avviene attualmente, di far proseguire o revocare la misura alternativa, ma anche di sostituirla con un’altra misura. A tale scopo sul sistema deve essere introdotta la funzione che permette di sostituire una misura alternativa.
## REQ-SIE-009-08
Con il D.lgs. 123/18 è stato introdotto l’art. 51 quater O.P.. Tale norma prevede la possibilità, per il giudice che concede la misura alternativa, di sospendere l’esecuzione delle pene accessorie.
## REQ-SIE-009-09
Prevedere una funzione di estrazione dati per il recupero dei procedimenti SIUS con contenuto ‘Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) ’ per i quali il magistrato designato ha proceduto alla ‘non emissione’ dell’ordinanza trasmettendo gli atti al Presidente.
## REQ-SIE-009-10
Prevedere una funzione di estrazione dati per il recupero dei procedimenti SIUS con contenuto ‘Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) ’ con data di esecutorietà inserita, ma privi di decisione da parte del Collegio.
## REQ-SIE-009-11
Prevedere una funzione di estrazione dati per il recupero dei procedimenti SIUS con contenuto di “Revoca ammissione provvisoria misura alternativa – Art. 678 comma 1 ter c.p.p.” che nascono da “Semplice Proposta” oppure a seguito di “Sospensione della Misura” da parte del magistrato.
## REQ-SIE-009-12
Per gli uffici UDS occorre prevedere l’inserimento di un nuovo contenuto denominato ‘Lavoro Pubblica Utilità’. Prevedere parallelamente l’inserimento di oggetti ed esiti.
## REQ-SIE-009-13
Per gli uffici UDS occorre prevedere la rettifica della descrizione del contenuto ‘Lavoro Esterno’, la modifica delle descrizione degli oggetti associati a tale contenuto ed anche l’inserimento di un nuovo oggetto.
## REQ-SIE-009-14
Stante quanto prescritto dall’art. 57 O.P., nella maschera di iscrizione di un procedimento SIUS, nella combo box dei mittenti, occorre aggiungere la voce “gruppo di osservazione e trattamento”.
## REQ-SIE-009-15
Intervenire sull’aggiornamento della funzione STATISTICHE – MOVIMENTO PROVVEDIMENTI PER OGGETTI in modo da integrare anche questa nuova tipologia di ordinanza provvisoria.
## REQ-SIE-009-16
Intervenire sulle pagine di richiesta di atti istruttori al fine di indicare la data entro cui l’atto deve essere restituito all’ufficio di Sorveglianza che ne ha fatto richiesta.
## REQ-SIE-009-17
Prevedere una nuova funzione di Ricerca nel menù Statistiche/Monitoraggio che conteggi ed estrapoli la lista dei procedimenti per i quali, in fase di richiesta di un atto istruttorio, sia stata indicata una determinata data di scadenza entro il quale far pervenire l’atto richiesto.
# Descrizione dell’Intervento
## Ambito Normativo
### D.lgs. 123/2018
In relazione al Capo II: DISPOSIZIONI PER LA SEMPLIFICAZIONE DEI PROCEDIMENTI, Art. 4: Modifiche al codice di procedura penale in tema di semplificazione, all'articolo 678, viene inserito il comma 1-ter che recita quanto segue:

«1-ter. Quando la pena da espiare non è superiore a un anno e sei mesi, per la decisione sulle istanze di cui all'articolo 656, comma 5, il presidente del tribunale di sorveglianza, acquisiti i documenti e le necessarie informazioni, designa il magistrato relatore e fissa un termine entro il quale questi, con ordinanza adottata senza formalità, può applicare in via provvisoria una delle misure menzionate nell'articolo 656, comma 5. L'ordinanza di applicazione provvisoria della misura è comunicata al pubblico ministero e notificata all'interessato e al difensore, i quali possono proporre opposizione al tribunale di sorveglianza entro il termine di dieci giorni. Il tribunale di sorveglianza, decorso il termine per l'opposizione, conferma senza formalità la decisione del magistrato.
Quando non è stata emessa o confermata l'ordinanza provvisoria, o è stata proposta opposizione, il tribunale di sorveglianza procede a norma del comma 1. Durante il termine per l'opposizione e fino alla decisione sulla stessa, l'esecuzione dell'ordinanza è sospesa.»;

## Adeguamento sistema SIUS d.lgs. 123/2018 (UFFICI MAGGIORENNI)
In riferimento all’’introduzione del comma 1 ter all’articolo 678 c.p.p., l’ufficio Tribunale di Sorveglianza (ufficio TDS) ha la possibilità di concedere misure alternative, ex art. 656 commi 5 e 6 c.p.p. per procedimenti relativi a condanne per pene fino a 18 mesi.
Nasce, pertanto, l’esigenza di dover gestire un nuovo contenuto in fase di iscrizione di un procedimento SIUS lato Tribunale di Sorveglianza.
### REQ-SIE-009-01 TDS - Concessione misure alternative (art. 678 comma 1-ter c.p.p.)
Il contenuto da prevedere per gli uffici TDS è:

“Concessione misure alternative (art. 678 comma 1-ter c.p.p.)”,

al quale vanno associati i seguenti oggetti:
“Affidamento in prova al servizio sociale (art. 47 O.P. -  art. 678 comma 1-ter c.p.p.)”;
“Affidamento in prova al servizio sociale (art. 94 DPR 309/90 - art. 678 comma 1-ter c.p.p.)”;
“Detenzione domiciliare (art. 47 ter O.P. - art. 678 comma 1-ter c.p.p.)”;

Quest’ultima voce deve prevedere le seguenti sotto voci:

Detenzione Domiciliare Donna Incinta o Madre di Prole di Età Inferiore Ad Anni Dieci con Lei Convivente;
Detenzione Domiciliare Padre, Esercente la Potestà, di Prole di Età Inferiore Ad Anni Dieci con Lui Convivente;
Detenzione Domiciliare Persona in Condizioni di Salute Particolarmente Gravi, Che Richiedano Costanti Contatti con i presidi sanitari territoriali;
Detenzione Domiciliare Persona di Età Superiore a Sessanta Anni Se Inabile Anche Parzialmente
Detenzione Domiciliare Persona Minore di Anni Ventuno per Comprovate Esigenze di Salute, di Studio, di Lavoro e di Famiglia;
Detenzione domiciliare (art. 47 ter comma 1 bis O.P. - art. 678 comma 1-ter c.p.p.);
Detenzione domiciliare per ultrasettantenni (art. 47 ter comma 01 O.P. - art. 678 comma 1-ter c.p.p.);
Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.);
Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.);

Ciò si traduce nella possibilità di poter scegliere un nuovo contenuto nella pagina di iscrizione di un procedimento SIUS, così come mostrato nella figura che segue:


Figura 1: Pagina iscrizione procedimento SIUS

Parallelamente, in fase di associazione degli oggetti, tramite il pulsante ,  il sistema deve poter permettere di associare le voci su elencate, così come prospettate nella pagina che segue:

Figura 2: Elenco oggetti per contenuto Concessione Misure Alternative (art. 678 comma 1-ter c.p.p.)

A seguito dell’iscrizione del procedimento SIUS con il nuovo contenuto “Concessione misure alternative (art. 678 comma 1-ter c.p.p.)”, l’utente procede con l’emissione dell’ordinanza.
La pagina di emissione dell’ordinanza sarà uguale alla maschera attualmente utilizzata per il contenuto ‘Concessione Misure Alternative Alla Detenzione’ (C001):


Figura 3: Emissione Ordinanza di Misura Alternativa (art. 678 comma 1-ter c.p.p.)

E gli esiti previsti per lo scarico dell’ordinanza saranno:
Concede
Rigetta
Dichiara L’inammissibilità
Dichiara N.D.P./ N.L.P.
Dichiara La Propria Incompetenza

In fase di stampa dell’ordinanza sarà associato un nuovo template simile al documento sotto riportato:


Figura 4: Template Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.)

Tale documento è assimilabile all’attuale template previsto per il contenuto ‘Concessione Misure Alternative Alla Detenzione’ (C001), ossia SIUS_OR_AFFIDAMENTO.rtf. Dettagli più specifici saranno forniti dall’Amministrazione.

Il flusso di lavorazione del procedimento SIUS che abbia il nuovo contenuto ‘Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) ’ seguirà quello attualmente in essere per il contenuto ‘Concessione Misure Alternative Alla Detenzione’ (C001) con la gestione della modifica, visualizzazione, cancellazione, stampa, validazione e trasmissione.

La funzione di trasmissione è fondamentale per implementare correttamente lo scambio di informazioni con SIEP e permettere, pertanto, lato Procura, la gestione delle nuova ordinanza di ‘Concessione di Misura Alternativa (art. 678 comma 1-ter c.p.p.) ’. Si evidenzia che questo è uno dei punti di impatto che vede coinvolto il sotto sistema SIUS con il sotto sistema SIEP.

Sempre in riferimento al comma 1 ter all’articolo 678 c.p.p., per procedimenti relativi a condanne per pene fino a 18 mesi, l’ufficio Tribunale di Sorveglianza (TDS), in tema di semplificazione della procedura, designa il magistrato relatore e fissa un termine entro il quale questi, con ordinanza adottata senza formalità, può applicare in via provvisoria una delle misure menzionate nell'articolo 656, comma 5.

L’adeguamento del sistema SIUS a tale normativa si delinea nell’implementazione esposta al paragrafo che segue.
### REQ-SIE-009-02 TDS - Emissione del Decreto Presidenziale di Designazione
Accedendo al sistema SIUS con utenza TDS (Tribunali di Sorveglianza Maggiorenni), in corrispondenza del menù ‘Decreti’, sarà introdotto un nuovo tasto funzione denominato ‘Decreto Presidenziale di Designazione’.


Figura 5: Menù Decreto Presidenziale di Designazione

L’accesso alla funzione mostrerà una nuova maschera per inserire il decreto in oggetto.
Dal punto di vista funzionale il Decreto di Designazione, va inserito dopo l’iscrizione di un procedimento SIUS con contenuto “Concessione misure alternative (art. 678 comma 1-ter c.p.p.)”.

Pertanto, l’utente:
Inserisce un nuovo procedimento SIUS di “Concessione misure alternative (art. 678 comma 1-ter c.p.p.)”
Emette, nei casi previsti dal decreto, il decreto Presidenziale di Designazione

Tramite questa funzione il Tribunale di Sorveglianza va a designare il magistrato relatore che può applicare in via provvisoria, in riferimento a procedimenti relativi a condanne per pene fino a 18 mesi, una delle misure menzionate nell'articolo 656, comma 5.
La maschera per l’inserimento del decreto deve permettere pertanto, di poter inserire le seguenti informazioni:
Data Emissione
Magistrato Relatore designato
Contenuto (valore fisso, corrispondente al contenuto - Concessione misure alternative (art. 678 comma 1-ter c.p.p. -  selezionato in fase di iscrizione del procedimento SIUS)
Oggetto (selezionabile dalla lista degli oggetti associati al contenuto - Concessione misure alternative (art. 678 comma 1-ter c.p.p.))
Tribunale Sorveglianza e relativa sede
Termine Emissione (dove indicare il termine entro il quale il magistrato deve provvedere all’emissione dell’ordinanza di ammissione provvisoria).


Figura 6: Pagina di inserimento del Decreto Designazione Magistrato

Caratteristica fondamentare di tale decreto è che a seguito dell’inserimento e validazione dello stesso, il procedimento in lavorazione non deve essere chiuso.
Per tale decreto deve essere creato un documento di stampa ad hoc che sarà fornito dall’Amministrazione.

Lo stato del procedimento, a seguito della validazione del Decreto di Designazione, sarà impostato a ‘Emesso Decreto Designazione’, mentre l’esito da associare al decreto è ‘Magistrato Designato art. 678 1-ter’. L’introduzione di un nuovo stato procedimento e nuovo esito si giustifica per la corretta individuazione dei procedimenti SIUS ai fini delle elaborazioni statistiche.

Nel momento in cui, tramite il Decreto di designazione, viene individuato il Magistrato, il sistema deve aggiornare in automatico il magistrato assegnatario presente nella maschera di dettaglio del procedimento SIUS.  Qualora il magistrato assegnatario del procedimento fosse già stato assegnato precedentemente all’emissione del decreto, e dovesse differire dal magistrato designato con il decreto, il sistema, nella pagina di dettaglio del procedimento SIUS, deve visualizzare un messaggio che avverte della discrepanza tra i due magistrati.


Figura 7: Messaggio Incongruenza Magistrato

A quel punto la cancelleria deve provvedere con la rettifica del magistrato assegnatario. In caso di mancata rettifica, il procedimento non può essere lavorato nelle eventuali fasi successive.

Il magistrato, ricevuta la designazione, se ritiene di poter concedere una delle misure alternative previste dall’art. 656 comma 5 c.p.p., e non necessariamente quella richiesta dal condannato, emette de plano un’ordinanza di applicazione provvisoria.
### REQ-SIE-009-03 TDS - Emissione Ordinanza Applicazione Provvisoria
Accedendo al sistema SIUS con utenza TDS (Tribunale di Sorveglianza Maggiorenni), in corrispondenza del menù ‘Ordinanze’, sarà introdotto un nuovo tasto funzione denominato ‘Applicazione Provvisoria M.A’.


Figura 8: Menù Emissione Ordinanza Provvisoria

L’accesso alla funzione mostrerà una nuova maschera per inserire un’ordinanza di Applicazione Provvisoria di Misura Alternativa. La tipologia di ordinanza che viene emessa deve essere di tipo ‘ordinanza provvisoria’ e l’emissione di tale ordinanza non deve richiedere la fase di ‘Fissazione’ o ‘Prefissazione’ udienza. Deve essere gestita, quindi, come rito monocratico.
Dal punto di vista funzionale, l’emissione di un’ordinanza di Applicazione Provvisoria M.A. si inserisce a valle dell’inserimento del Decreto Presidenziale di Designazione.
Affinché possa essere emessa un’ordinanza di Applicazione Provvisoria M.A., infatti, il sistema deve controllare che, per il procedimento SIUS in lavorazione, sia stato emesso il Decreto di Designazione del magistrato relatore.
Nella casistica in cui, entro i termini previsti, non si stato emesso il Decreto di Designazione, per dare seguito all’applicazione della misura, si procede con l’emissione dell’ordinanza cosi come esplicitato al par. 3.2.1, rientrando quindi nel classico giro del rito dibattimentale, quindi con la fissazione udienza ed emissione dell’ordinanza che applica o meno la misura.

La maschera per l’inserimento dell’ordinanza provvisoria, similmente all’emissione di un ordinanza generica deve permettere di poter inserire le seguenti informazioni:
Data Emissione
Contenuto
Oggetto


Figura 9: Emissione Ordinanza Applicazione Provvisoria M.A.

mentre, nella pagina di inserimento degli esiti, oltre alla combo box contenente gli esiti, devono essere previste in aggiunta le seguenti informazioni:
Un campo ‘check box’ con accanto la dicitura “ordinanza non emessa – restituzione atti al Presidente”.
Campo note (per eventuali motivazioni della restituzione degli atti).


Figura 10: Pagina esiti Ordinanza Provvisoria

Gli esiti da prevedere sono quelli consueti, vale a dire “Concede”, “Rigetta”, “NLP”, “Inammissibilità” e “Incompetenza” ed in aggiunta quello denominato “Applica Provvisoriamente”.

Nel caso in cui, dunque, il magistrato relatore ritenga di non poter applicare alcuna delle misure concedibili, egli dovrà limitarsi a rimettere gli atti al Presidente del Tribunale di Sorveglianza, il quale provvederà secondo il tradizionale procedimento ex articolo 678, comma 1 del codice di procedura penale, predisponendo il contraddittorio. Il rigetto dell’istanza è sempre subordinato, pertanto, ad una valutazione di tipo collegiale.

L’introduzione e l’utilizzo del ‘check box’ su indicato determinano, pertanto, la ‘NON EMISSIONE’ dell’ordinanza provvisoria, entro il termine assegnato, e la restituzione degli atti al presidente del Tribunale di Sorveglianza. A questo punto lo stato del procedimento SIUS deve essere impostato a ‘Trasmessi Atti al Presidente’.
La ‘Non Emissione’ dell’ordinanza determina comunque la chiusura della fase provvisoria in maniera alternativa rispetto alla ordinaria indicazione degli esiti. La procedura a questo punto segue il suo corso normale con l’apertura del dibattito. Quindi il TDS fissa udienza ed emette ordinanza.

Caratteristica fondamentale dell’ordinanza del magistrato designato di Applicazione Provvisoria di Misura Alternativa, è la sua non immediata esecutività.
L’ordinanza diverrà esecutiva una volta trascorsi 10 giorni senza che venga proposta opposizione e, in virtù di ciò, deve essere prevista la possibilità di annotare, ed evidenziare nella maschera di dettaglio del procedimento SIUS, la data di esecutività della stessa.
Nella casistica in cui venga presentata opposizione, detta opposizione va annotata sul procedimento “provvisorio” utilizzando l’apposita funzione “Impugnazioni/Opposizioni”. Il procedimento SIUS seguirà il medesimo processo di lavorazione già in essere per il contenuto ‘Concessione Misure Alternative Alla Detenzione’ (C001).

### REQ-SIE-009-04 TDS - Registrazione data Esecutività Ordinanza Applicazione Provvisoria
Per la registrazione della data di esecutività si prevede di aggiungere una nuova voce menù da inserire nella combo box presente nella maschera di dettaglio del procedimento SIUS.


Figura 11: Funzione Esecutività Applicazione Provvisoria m.a.

Dal punto di vista funzionale, l’attività di registrazione della data di esecutività dell’ordinanza di applicazione provvisoria si pone a valle dell’emissione dell’ordinanza provvisoria.
Accedendo alla funzione, il sistema prospetta una nuova pagina in cui deve essere registrata la data di esecutività dell’ordinanza di applicazione provvisoria.
A seguire si mostra un esempio di pagina. Le informazioni da riportare sono:
Dettaglio procedimento SIUS
Dettaglio dati Soggetto
Estremi dell’ordinanza provvisoria di Concessione di Misura Alternativa (art. 678 comma 1 -ter)
Campo ‘Data Esecutività’
Campo note


Figura 12: Pagina Registrazione Esecutività


I campi editabili sono ‘Data Esecutività’ e ‘note, che a seguito del conferma devono essere registrati nella tabella deposito_ordinanza_pc.
A seguito dell’inserimento, la data di esecutività, dovrà essere visualizzata nella porzione della maschera di dettaglio del procedimento SIUS dedicata ai provvedimenti, come mostrato nella figura che segue:


Figura 13: Sezione Provvedimenti

La stessa informazione dovrà essere replicata nella pagina di dettaglio provvedimenti, che il sistema mostra in corrispondenza del link Provvedimenti.


Figura 14: Pagina Dettaglio Provvedimenti


A seguito dell’emissione dell’ordinanza provvisoria e a partire dalla data in cui diviene esecutiva, si possono delineare diverse possibili gestioni operative, tra cui quelle che seguono:

Il Tribunale di Sorveglianza, conferma senza formalità la decisione del magistrato. (REQ-SIES-009-05)
Incorrere in una revoca dell’ammissione provvisoria, nel caso, ad esempio, di gravi violazioni delle prescrizioni nel corso dell’esecuzione provvisoria. (REQ-SIES-009-06)
Il Tribunale di Sorveglianza, a seguito di comportamenti suscettibili di revoca della misura, potrebbe sostituirla con una di diversa natura (nuova formulazione dell’art. 51 ter O.P.). (REQ-SIES-009-07)

Sono state evidenziate queste specifiche casistiche in quanto direttamente interessate da nuova formulazione giuridica di specifici articoli a mezzo del D.lgs. 123/2018.
### REQ-SIE-009-05 TDS - Provvedimento di Conferma Ordinanza Applicazione Provvisoria
A seguito dell’emissione dell’ordinanza provvisoria e a partire dalla data in cui diviene esecutiva, il Tribunale, con decisione del collegio, conferma la decisione del Magistrato Designato.

Per proseguire con l’emissione del provvedimento di conferma, l’utente TDS deve procedere con la funzione di emissione ordinanza e/o emissione decreto utilizzando il nuovo contenuto “Concessione misure alternative (art. 678 comma 1-ter c.p.p.)”, previsto al requisito REQ-SIE-00901 al par. 3.2.1.

In particolare, il requisito in oggetto, REQ-SIE-009-05, va ad estendere quanto già definito al requisito REQ-SIE-009-01 in quanto, per il contenuto “Concessione misure alternative (art. 678 comma 1-ter c.p.p.)” deve essere previsto un nuovo oggetto ed un nuovo esito.

L’oggetto da prevedere, ed anche il relativo esito devono avere la seguente dicitura:
Conferma Decisione del Magistrato Relatore

Quando, in fase di iscrizione del procedimento SIUS, viene selezionato l’oggetto ‘Conferma Decisione del Magistrato Relatore’, a video deve apparire una sezione ‘Anno/Progressivo del Procedimento di Ammissione Provvisoria della Misura Alternativa’, dove occorre inserire l’identificativo del procedimento SIUS sul quale è stata inserita l’ordinanza di applicazione provvisoria di misura in esecuzione (con data esecutività inserita).


Figura 15: Pagina iscrizione Procedimento di Conferma Decisione Magistrato Relatore

A seguito dell’iscrizione del procedimento con oggetto ‘Conferma Decisione del Magistrato’, l’utente TDS prosegue con la funzione di ‘Emissione Ordinanza’ oppure di ‘Emissione Decreto’.
Il sistema, pertanto, deve permettere di utilizzare il contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.)´sia dalla funzione Ordinanze»Emissione Ordinanza  che  dalla funzione Decreti»Emissione Decreto.

Il flusso di lavorazione del procedimento SIUS che abbia il nuovo contenuto ‘Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) ’ seguirà quello attualmente in essere per il contenuto ‘Concessione Misure Alternative Alla Detenzione’ (C001) con la gestione della modifica, visualizzazione, cancellazione, stampa, validazione e trasmissione. Le pagine di modifica, visualizzazione e la funzione di stampa devono prevedere in aggiunta a quanto ad oggi presente, l’informazione circa il numero e l’anno del provvedimento di ammissione provvisoria.
### REQ-SIE-009-06 TDS - Gestione Revoca Ammissione Provvisoria
Nel D.lgs. 123/18 al capo II, art. 5 è introdotta una nuova formulazione dell’art. 51 ter O.P.:

Art. 51-ter (Sospensione cautelativa delle misure alternative).
C. 1. Se la persona sottoposta a misura alternativa pone in essere comportamenti suscettibili di determinarne la revoca, il magistrato di sorveglianza, nella cui giurisdizione la misura è in esecuzione, ne dà immediata comunicazione al tribunale di sorveglianza affinché ‘decida in ordine alla prosecuzione, sostituzione o revoca della misura.

C. 2. Nell'ipotesi di cui al comma 1, il magistrato di sorveglianza può disporre con decreto motivato la provvisoria sospensione della misura alternativa e ordinare l'accompagnamento in istituto del trasgressore. Il provvedimento di sospensione perde efficacia se la decisione del tribunale non interviene entro trenta giorni dalla ricezione degli atti.


Secondo quanto previsto dell’art. 51 ter O.P., il Tribunale di Sorveglianza, a seguito di comunicazione da parte del magistrato, può decidere in merito alla Revoca di una misura alternativa. Punto innovativo della nuova formulazione dell’art. 51 ter è che la revoca della misura alternativa alla detenzione, come anche la sostituzione, che vedremo al par. successivo, non deve necessariamente essere preceduta da provvedimento di sospensione cautelativa da parte del magistrato.

A questo punto sul sistema occorre considerate due interventi fondamentali:

Prevedere un nuovo contenuto denominato:

“Revoca misura alternativa – Art. 678 comma 1 ter c.p.p.”.

Personalizzare la maschera di creazione procedimento SIUS


A seguito del punto 1, occorre considerare anche la creazione di nuovi oggetti da associare al contenuto. I nuovi oggetti devono essere i seguenti:

“Revoca ammissione provvisoria Affidamento in prova al servizio sociale (art. 47 O.P. - art. 678 comma 1-ter c.p.p.)”;
“Revoca ammissione provvisoria Affidamento in prova al servizio sociale (art. 94 DPR 309/90 - art. 678 comma 1-ter c.p.p.)”;
“Revoca ammissione provvisoria Detenzione domiciliare (art. 47 ter O.P. - art. 678 comma 1-ter c.p.p.)”;
“Revoca ammissione provvisoria Detenzione domiciliare (art. 47 ter comma 1 bis O.P. - art. 678 comma 1-ter c.p.p.)”;
“Revoca ammissione provvisoria Detenzione domiciliare per ultrasettantenni (art. 47 ter comma 01 O.P. - art. 678 comma 1-ter c.p.p.)”;
“Revoca ammissione provvisoria Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.)”;
“Revoca ammissione provvisoria Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.)”.

Gli esiti da prevedere sono:
Ratifica Il Provvedimento Di Sospensione e Non Revoca
Accoglie Proposta e Revoca
Rigetta Proposta e Non Revoca
Ratifica Il Provvedimento Di Sospensione e Revoca
Dichiara N.D.P./ N.L.P.
Dichiara Inammissibile
Dichiara L'incompetenza

a meno del nuovo esito da integrare per il requisito REQ-SIE-009-07 in relazione alla sostituzione della misura.

Il flusso di lavorazione del procedimento di Revoca misura alternativa – Art. 678 comma 1 ter c.p.p. è il medesimo ad oggi previsto per il contenuto “Revoca Misure Alternative Per Violazione Prescrizioni Su Proposta Del Magistrato” (C002). Per il nuovo contenuto, però, deve essere modificata la pagina di inserimento dell’ordinanza di revoca (vedi requisito REQ-SIE-009-07).

Per quanto riguarda la ‘personalizzazione’ della pagina di creazione del procedimento SIUS, in fase di creazione di un procedimento con contenuto di “Revoca ammissione provvisoria misura alternativa – Art. 678 comma 1 ter c.p.p.”, il sistema deve mostrare una nuova sezione in cui l’utente deve segnalare se l’iscrizione della revoca è dovuta ad una semplice ‘Proposta Revoca’ oppure se nasce a seguito di ‘Sospensione Provvisoria’ della misura da parte del magistrato.


Figura 16: pagina di revoca

Tale informazione deve essere mostrata, a seguire, sulla pagina di dettaglio del procedimento SIUS.


Figura 17: dettaglio procedimento revoca


Questa informazione posta a livello di Procedimento SIES è necessaria anche ai fini delle elaborazioni statistiche previste al requisito REQ-SIE-009-11.

### REQ-SIE-009-07 TDS - Gestione Sostituzione della Misura Alternativa
Collegandoci a quanto già esposto nel paragrafo precedente, la gestione della sostituzione della misura alternativa, nasce direttamente dalla nuova formulazione dell’art. 51 ter O.P. previsto in D.lgs. 123/18.
Infatti Il contenuto realmente innovativo della norma esiste proprio nel primo comma, ove si menziona che il Tribunale di Sorveglianza, può decidere in ordine alla sostituzione della misura alternativa.
Per quanto attiene alla sostituzione della misura, sul sistema occorre intervenire con le seguenti implementazioni:

Prevedere un nuovo esito, denominato ‘Sostituisce la Misura Alternativa’ per il contenuto “Revoca misura alternativa – Art. 678 comma 1 ter c.p.p.”;
Rendere dinamica la pagina di emissione dell’ordinanza in base all’esito di sostituzione della misura;

Entrambi gli interventi vertono sul rifacimento della pagina di emissione di ordinanza di revoca:


Figura 18: Pagina Ordinanza per Sostituzione Misura

Infatti nella combo degli Esiti deve apparire la nuova voce ‘Sostituisce la Misura Alternativa’, e nel momento in cui viene selezionato tale esito, in pagina deve apparire la sezione per specificare la nuova misura alternativa.
Confermando, i dati specificati in pagina, devono essere riportati sulla maschera di dettaglio ordinanza di revoca. Il flusso di lavorazione del procedimento SIUS seguirà quello attualmente in essere per il contenuto “Revoca Misure Alternative Per Violazione Prescrizioni Su Proposta Del Magistrato” (C002) con la gestione della modifica, visualizzazione, cancellazione, stampa, validazione e trasmissione. La pagina di modifica e visualizzazione devono riportare la nuova sezione per esito ‘sostituisce la misura’.  Anche nel template di stampa deve essere prevista l’aggiunta della nuova misura in sostituzione.

### REQ-SIE-009-08 UDS - TDS - Gestione Sospensione delle Pene Accessorie
Nel d.lgs. 123/18 al capo II, art. 6 è introdotto l’art. 51 quater O.P. ove si cita:

«Art. 51-quater (Disciplina delle pene accessorie in caso di concessione di misure alternative).
1. In caso di applicazione di una misura alternativa alla detenzione, sono eseguite anche le pene accessorie, salvo che il giudice che ha concesso la misura, tenuto conto delle esigenze di reinserimento sociale del condannato, ne disponga la sospensione.

2. In caso di revoca della misura, ove disposta l'applicazione delle pene accessorie ai sensi del comma 1, l'esecuzione ne viene sospesa, ma il periodo già espiato è computato ai fini della loro durata.».

A seguito di tale articolo, per il sistema SIUS, nasce l’esigenza di dover gestire un nuovo contenuto in fase di iscrizione di un procedimento SIUS, sia lato Tribunale di Sorveglianza (TDS) che lato Ufficio di Sorveglianza (UDS).

Il contenuto da prevedere per gli uffici TDS e UDS è:

Sospensione pene accessorie (art. 51 quater O.P.)

al quale va associato un unico oggetto con la medesima descrizione.

Ciò si traduce nella possibilità di poter scegliere un nuovo contenuto nella pagina di iscrizione di un procedimento SIUS, così come mostrato nella figura che segue:


Figura 19: Iscrizione Procedimento SIUS - Sospensione Pene Accessorie

Parallelamente, in fase di associazione degli oggetti, il sistema deve poter permettere di associare l’unica voce, ‘sospensione pene accessorie (art. 51 quater O.P.)’  così come prospettato nella pagina che segue:




La maschera per l’inserimento dell’ordinanza, similmente all’emissione di un ordinanza generica deve permettere di poter inserire le seguenti informazioni:
Data Emissione
Contenuto
Oggetto


Figura 20: Ordinanza Sospensione Pene Accessorie

mentre, nella pagina di inserimento degli esiti, oltre alla combo box contenente gli esiti, devono essere previste in aggiunta le seguenti informazioni:

elenco pene accessorie irrogate in sentenza e legate al fascicolo SIEP
durata sospensione (anni, mesi e giorno)
oppure Fino Al
Gli esiti da prevedere per lo scarico dell’ordinanza saranno:

Sospende Pena Accessoria
Rigetta
Dichiara L’inammissibilità
Dichiara N.D.P./ N.L.P.
Dichiara La Propria Incompetenza

A partire dall’elenco delle pene accessorie, il sistema deve permettere di far selezionare, all’utente, le sole pene accessorie per le quali sia stata disposta la sospensione.
A questo punto in maschera quindi deve essere mostrato un elenco con le corrispondenti checkbox, così come riportato nella figura che segue:


Figura 21: Ordinanza Sospensione Pene Accessorie

Confermando, i dati specificati in pagina, devono essere riportati sulla maschera di dettaglio ordinanza di sospensione pene accessorie. Il flusso di lavorazione del procedimento SIUS in oggetto, seguirà con la gestione della modifica, visualizzazione, cancellazione, stampa, validazione e trasmissione. La pagina di modifica deve permettere di modificare le pene accessorie modificate e i dati della durata.
Per tale ordinanza deve essere creato un documento di stampa ad hoc come riportato nella figura che segue:

Figura 21: template 51 quater(sospensione pene accessorie)

### REQ-SIE-009-09 - REQ-SIE-009-10 - REQ-SIE-009-11 (Statistiche Misura Alternativa - art. 678 comma 1-ter c.p.p.) )
Per i requisiti in oggetto, per gli uffici TDS, il sistema SIUS deve prevedere tre nuove tipologie di statistiche attinenti a procedimenti SIUS con contenuto ‘Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.)’.

In particolare in corrispondenza del menù ‘Statistiche/Monitoraggio’ deve essere previsto un nuovo tasto funzione denominato ‘Monitoraggio Misure Alternative (art. 678 comma 1-ter c.p.p.)’ così come raffigurato  nella figura che segue:


Figura 22: Menù Statistiche TDS
Con l’accesso alla funzione, il sistema mostrerà un pagina di ricerca tramite la quale l’utente inserisce i dati relativi all’intervallo di tempo o estremi del procedimento da verificare, e sceglie la statistica di interesse.

Le statistiche afferenti ai procedimenti di Misure Alternative (art. 678 comma 1-ter c.p.p.) saranno di tre tipologie:

Statistica Ordinanze Non Emesse – Trasmessi atti al Presidente [requisito REQ-SIE-009-09]
Statistica Ordinanze Emesse con data di esecutorietà inserita, ma privi di decisione da parte del Collegio [requisito REQ-SIE-009-10]
Statistica Revoca ammissione provvisoria misura alternativa – Art. 678 comma 1 ter c.p.p [requisito REQ-SIE-009-11]

A seguire si prospetta una pagina di esempio per la scelta della statistica di interesse:

Figura 23: Pagina di Ricerca per Statistiche

A seguito dell’inserimento dei criteri di interesse, e con la sottomissione dei dati al sistema, sarà generata una pagina di elenco con i procedimenti trovati.
Dalla pagina di elenco l’utente poi avrà la possibilità di visualizzare il dettaglio di ogni singolo procedimento SIUS trovato e di esportare il risultato ottenuto in un file excel.


Figura 24: Pagina Elenco Procedimenti per statistiche

Il layout della pagina riportata, in linee generali, sarà il medesimo per tutte le tipologie di statistiche previste.
Per quanto riguarda il foglio excel, le informazioni estratte saranno mostrate secondo il seguente formato.


Figura 25: esempio foglio excel

Per tutte le statistiche, si fa presente, che le estrazioni faranno riferimento allo stato in cui si trova il fascicolo nel momento di elaborazione della statistica.

#### REQ-SIE-009-09 TDS - Statistica Ordinanze Non Emesse (Trasmessi Atti al Presidente)

La statistica in oggetto va a recuperare la lista dei procedimenti SIUS iscritti da uffici TDS con contenuto di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ che hanno un’ordinanza di applicazione provvisoria di misura alternativa il cui esito è ‘Trasmesso Atti al Presidente’.
Tali procedimenti sono individuabili dal flag ‘Atti trasmessi al Presidente’ posto ad ‘on’ sulla dalla tabella deposito_ordinanza_pc  e dallo stato del procedimento che è posto a ‘Atti trasmessi al Presidente’.
Rientrano in questa categoria anche i procedimenti SIUS iscritti da uffici TDS con contenuto di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ per quali risulta inserito il decreto di designazione magistrato, ma non sia mai stata emessa ordinanza. Infatti, il magistrato designato qualora ritenga di non poter applicare alcuna misura, non è tenuto ad emettere un’ordinanza di contenuto negativo, ma può semplicemente lasciar decorrere il tempo assegnatoli. Anche quest’ultimi, infatti, ‘ritornano’ al Presidente del Tribunale Sorveglianza.

#### REQ-SIE-009-10 TDS - Statistica Ordinanze Provvisorie Esecutive senza decisione del Collegio

La statistica in oggetto va a recuperare la lista dei procedimenti SIUS iscritti da uffici TDS con contenuto di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ che hanno un’ordinanza di applicazione provvisoria di misura alternativa il cui esito è ‘Applica Provvisoriamente’ e per i quali manca il decreto e/o ordinanza di ‘Conferma’ da parte del Collegio o comunque una qualsivoglia decisione da parte del Collegio.
Queste ordinanze sono individuabili, oltre che dall’esito dell’ordinanza corrispondente a ‘Applica Provvisoriamente ’, anche dalla presenza di una data di esecutività inserita in corrispondenza del record di interesse sulla tabella deposito_ordinanza_pc.
Inoltre per il procedimento SIUS da estrarre, non deve esistere un evento che lo lega ad un procedimento SIUS con esito ‘Conferma Decisione del Magistrato Relatore’.
I procedimenti di interesse per questa statistica devono essere tutti quelli per i quali è ‘mancante’ una decisione da parte del Collegio.
Per questa tipologia di statistica, sia nella pagina di elenco che nel relativo foglio Excel, in output deve essere mostrata anche la data di inizio esecutività.

#### REQ-SIE-009-11 TDS - Statistica per Revoca ammissione provvisoria misura alternativa – Art. 678 comma 1 ter c.p.p

La statistica in oggetto va a recuperare la lista dei procedimenti SIUS iscritti da uffici TDS con contenuto di ‘Revoca ammissione provvisoria misura alternativa – Art. 678 comma 1 ter c.p.p.’
Per questi procedimenti, la statistica, secondo richiesta, deve dare evidenza del fatto che il procedimento di revoca sia nato come ‘semplice proposta’ oppure a seguito di ‘sospensione misura’ da parte del magistrato.
I procedimenti da conteggiare sono individuabili andando a ‘interrogare’ la tabella generale_procedimento in corrispondenza dei nuovi campi previsti da aggiungere per ‘registrare’ la ‘natura’ del provvedimento di revoca.

Per questa tipologia di statistica, sia nella pagina di elenco che nel relativo foglio Excel, in output deve essere mostrata l’informazione circa la natura del procedimento: nato da semplice proposta o a seguito di sospensione.

### REQ-SIE-009-12 UDS - Introduzione del contenuto ‘Lavoro Pubblica Utilità’
In relazione alle modificazioni dell’art 20 O.P (previste nel D.lgs. 124/18) e nello specifico per l’introduzione dell’Art. 20-ter (Lavoro di pubblica utilità):

Cit.:  I detenuti e gli internati possono chiedere di essere ammessi a prestare la propria attività a titolo volontario e gratuito nell'ambito di progetti di pubblica utilità, tenendo conto anche delle specifiche professionalità e attitudini lavorative.

per gli uffici UDS (Uffici di Sorveglianza) occorre prevedere l’introduzione di un nuovo contenuto ‘Lavoro di pubblica utilità – Art. 20 ter O.P.”.

Parallelamente devono essere inserite le seguenti descrizioni degli oggetti da associare a tale contenuto:

Diciture da creare ex novo:

Ammissione al lavoro di pubblica utilità – Art. 20 ter O.P.
Revoca lavoro di pubblica utilità – Art. 48 D.P.R. 230/2000 (Reg. Esec.)
Modifica lavoro di pubblica utilità – Art. 48 D.P.R. 230/2000 (Reg. Esec.)
Sospensione lavoro di pubblica utilità

Gli esiti da prevedere sono:

Approva
Non Approva
Restituisce Con Osservazioni
Dichiara N.D.P./ N.L.P.
Dichiara La Propria Incompetenza
Dichiara L’inammissibilità
Sospende
Non Sospende
Revoca
Non Revoca

### REQ-SIE-009-13 UDS - Integrazione del contenuto ‘Lavoro Esterno’
Per gli uffici UDS (Uffici di Sorveglianza) occorre prevedere la rettifica della descrizione dell’attuale contenuto ‘Lavoro Esterno’ (U007) in ‘Lavoro all’esterno/lavoro a sostegno delle famiglie delle vittime dei reati ‘.

Parallelamente devono essere modificate le seguenti descrizioni degli oggetti associati a tale contenuto:

Vecchie diciture:

Revoca Lavoro Esterno - Art. 48 co. 15 D.P.R. n. 230/2000 (Reg.Esec.)
Modifica Lavoro Esterno (Art. 21 O.P.) - Art. 21 O.P.
Sospensione lavoro esterno - Art. 21 O.P.

Nuove diciture:

Revoca lavoro all’esterno/lavoro a sostegno delle famiglie delle vittime dei reati – Art. 48 D.P.R. 230/2000 (Reg. Esec.)
Modifica lavoro all’esterno/lavoro a sostegno delle famiglie delle vittime dei reati” – Art. 48 D.P.R. 230/2000 (Reg. Esec.)
Sospensione lavoro all’esterno/lavoro a sostegno delle famiglie delle vittime dei reati

Inoltre occorre prevedere l’inserimento del seguente un nuovo oggetto:

Ammissione al lavoro a sostegno delle famiglie delle vittime dei reati

Gli esiti restano invariati:

Approva
Non Approva
Restituisce Con Osservazioni
Dichiara N.D.P./ N.L.P.
Dichiara La Propria Incompetenza
Dichiara L’inammissibilità
Sospende
Non Sospende
Revoca
Non Revoca

### REQ-SIE-009-14 (UDS – TDS Integrazione Lista Mittenti)
«Art. 57 (Legittimazione alla richiesta di misure). - 1. Le misure alternative e quelle di cui agli articoli 30, 30-ter, 52, 53 e 54 nonché' all'articolo 6 del decreto del Presidente della Repubblica 30 maggio 2002, n. 115, possono essere richieste dal condannato, dall’internato, dai loro prossimi congiunti, dal difensore, ovvero proposte dal gruppo di osservazione e trattamento.».

Secondo quando disposto all'art. 7 comma 1 lettera b) del D.lgs. 2 ottobre 2018, n. 123, nell’attuale maschera di iscrizione dei procedimenti SIUS, è necessario integrare le voci presenti in combo ‘Mittente’ con una nuova voce denominata ‘Gruppo di Osservazione e Trattamento’.  Verificare che la modifica sia valida da tutti i punti di accesso alla pagina. (Es: Iscrizione da procedimento SIEP e Iscrizione da Soggetto).

Figura 26: pagina iscrizione Procedimento SIUS

### REQ-SIE-009-15 (Aggiornamento Statistica Movimento Provvedimenti per Oggetti)
A seguito dei nuovi interventi previsti per la scheda in oggetto, è necessario aggiornare l’attuale funzione ‘STATISTICHE – MOVIMENTO PROVVEDIMENTI PER OGGETTI’ in modo da integrare la nuova tipologia di ordinanza provvisoria emessa dal magistrato designato.
Occorre intervenire sulla maschera di ricerca della statistica, vedi immagine successiva, per fare in modo che il contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ appaia nella lista degli oggetti selezionabili.



Parallelamente gestire la nuova informazione anche sul file Excel che viene generato a seguito della Conferma della statistica.
### REQ-SIE-009-16 Modifica pagina richiesta atti istruttori
Per gli uffici UDS, UDSM, TDS e TDSM, con il requisito in oggetto si chiede di intervenire sulla pagina di inserimento della richiesta di alcuni atti istruttori. La funzione è raggiungibile dal menù Fase istruttoria » Richiesta Atti, e gli atti istruttori interessati dalla modifica sono:
Accertamento progr. terapeutico
Certificato Carichi Pendenti
Conferma disponibilità SER.T
Cumulo
Estratto/Copia Provvedimento
Idoneità progr. terapeutico
Informazioni art. 47 - 4c.
Informazioni detenzione domiciliare
Informazioni su attività lavorativa
InformazioniPS per 47-47 Ter-50- 30 Ter
Ordin/decr. altro TdS/UdS
Relazione sanitaria
Sentenza Integrale
Verifica condotta progr. Ser.T
Visita medica
Altre Istruttorie
Nello specifico, nella pagina di inserimento della richiesta di ognuno di questi atti istruttori, deve essere previsto un nuovo campo ckeckbox, selezionando il quale deve essere mostrata una sezione ove indicare la data di restituzione dell’atto.

Figura 27: Pagina Richiesta Atti Istruttori
In fase di conferma, l’informazione aggiuntiva deve essere registrata nella tabella NOTIFICA, come esplicitato al par. 3.6.16.
I dati inseriti devono inoltre essere riportati nella pagina di dettaglio della richiesta così come mostrato nella pagina che segue:

Figura 28: Dettaglio Richiesta Atti Istruttori
Inoltre sul documento di stampa del modulo di richiesta, deve essere riportata l’informazione registrata, ossia la data entro cui deve essere restituito l’atto istruttorio prevedendo, su ogni template un frase ad ‘hoc’.
A tal proposito sarà necessario intervenire in modifica sui seguenti template:
SIUS_IS_ACCERTPROGTERAPEUT.rtf
SIUS_IS_CERCARICHIPENDENTI.rtf
SIUS_IS_CONFERMDISPONISERT.rtf
SIUS_IS_CUMULO.rtf
SIUS_IS_ESTRATTOSENTENZA.rtf
SIUS_IS_IDONEIPROGCOMTERAP.rtf
SIUS_IS_INFORMAZIONART474C.rtf
SIUS_IS_CONCEDETENZDOMICIL.rtf
SIUS_IS_INFORATTIVITALAVORATIVA.rtf
SIUS_IS_PSPERART47E5030TER.rtf
SIUS_IS_ORDINEDECRETDSUDS.rtf
SIUS_IS_RELAZIONESANITARIA.rtf
SIUS_IS_SENTENZAINTEGRALE.rtf
SIUS_IS_VERIFICONDPROGSERT.rtf
SIUS_IS_VISITAMEDICA.rtf
SIUS_IS_TDSGENERICO1.rtf
Si riporta un esempio di frase da aggiungere su ogni singolo template:

Figura 29: Esempio template atto istruttorio

### REQ-SIE-009-17 Statistica Atti Istruttori con Data Richiesta Restituzione
Per gli uffici UDS, UDSM, TDS e TDSM, con il requisito in oggetto si chiede di integrare nel menù di Statistiche/Monitoraggio » Ricerche una nuova tipologia di ricerca.
Nella pagina a cui si accede dal menù su indicato, deve essere aggiunto un nuovo tasto funzione così come mostrato nella figura che segue:


Figura 30: Funzione Ricerca Atti Istruttori

Il tasto da introdurre, sarà il punto di accesso alla nuova ricerca da implementare la quale si occuperà di recuperare e conteggiare quali siano i procedimenti SIUS per i quali sia stata fatta richiesta di un atto istruttorio e per la quale richiesta è stata inserita una data di consegna.

L’accesso alla funzione mostrerà una pagina di ricerca in cui immettere i dati per avviare la statistica di interesse.


Figura 30: Pagina ricerca Atti Istruttori


I possibili criteri di ricerca saranno:

Intervallo Estremi Procedimenti
Intervallo Date Iscrizione
Intervallo Date di Richiesta Consegna

Con il tasto ‘Ricerca’ sarà attivata la funzione di estrazione dati che va a recuperare gli estremi del procedimento SIUS, la data iscrizione del procedimento, nome e cognome del soggetto, la data di consegna richiesta ed il tipo di atto istruttorio richiesto.

Le informazioni recuperate devono essere mostrate in una pagina di elenco ed inoltre deve essere prevista la funzione di export in formato excel dei risultati ottenuti.


Figura 31:Elenco procedimenti con atti istruttori

Dalla pagina di elenco, l’utente potrà accedere al dettaglio del procedimento SIUS utilizzando il link posto in corrispondenza del Numero/Anno SIUS .
## Moduli sw
L’intervento software riguarderà il progetto SIES. In particolare per quanto attiene a questa prima fase, le classi coinvolte saranno relative soprattutto ai package java relativi a sius.
Il pacchetto interessato è, in ogni caso, il sies.war.
## Architettura
N.A.
## Interfacce utente
Le interfacce utente sono state esplicitate nella descrizione dell’intervento per ogni singolo requisito.
## Basi dati
Nel seguente paragrafo sono elencate le attività inerenti alla banca dati per ogni requisito individuato ai paragrafi precedenti.
### Base Dati - REQ-SIE-009-01 (TDS - Concessione misure alternative (art. 678 comma 1-ter c.p.p.))
Per censire il nuovo contenuto, nella tabella cg_refs_code, deve essere aggiunto un nuovo valore per il dominio OGGETTO_PROCEDIMENTO.
Sempre nella tabella cg_refs_code, devono essere mappati gli oggetti relativi al nuovo contenuto, prevedendo dei nuovi record per il dominio MOTIVO_PROVVEDIMENTO.
Sempre nella tabella cg_refs_code, devono essere mappati gli esiti relativi al nuovo contenuto, prevedendo dei nuovi record per il dominio ESITO_TENORE.
Per la registrazione del nuovo template da associare al contenuto introdotto per il requisito in oggetto, occorre prevedere un nuovo record nella tabella template.
### Base Dati - REQ-SIE-009-02 (TDS - Emissione del Decreto Presidenziale di Designazione)
Per censire la nuova funzione (Decreto Presidenziale di Designazione) occorre registrare l’informazione sulle seguenti tabelle:
funzione
funzione_profilo
relazione_funzioni
In fase di iscrizione del Decreto, il sistema registra i dati nella tabella DEPOSITO_DECRETO, EVENTO e TENORE
La tabella DEPOSITO_DECRETO deve prevedere dei nuovi campi per registrare la data di Termine Emissione dell’ordinanza di Ammissione Provvisoria.
Per censire il nuovo stato procedimento, nella tabella cg_refs_code, deve essere aggiunto un nuovo valore per il dominio STATO_PROCEDIMENTO.
Per censire il nuovo esito, nella tabella cg_refs_code, deve essere aggiunto un nuovo valore per il dominio ESITO_TENORE.
Per censire il nuovo stato procedimento, nella tabella cg_refs_code, deve essere aggiunto un nuovo valore per il dominio TIPO_DECRETO (Decreto Designazione).
Per la registrazione del codice magistrato designato è necessario integrare un nuovo campo nelle seguenti tabelle: EVENTO , TENORE e DEPOSITO_DECRETO.
Per la registrazione del nuovo template da associare al decreto di designazione magistrato, occorre prevedere un nuovo record nella tabella template.
### Base Dati - REQ-SIE-009-03 (TDS - Emissione Ordinanza Applicazione Provvisoria)
Per censire la nuova funzione (Ordinanza Applicazione Provvisoria M.A.) occorre registrare l’informazione sulle seguenti tabelle:
funzione
funzione_profilo
relazione_funzioni
Prevedere una nuova Tipologia Ordinanza: ordinanza provvisoria
Per la creazione della nuova tipologia di ordinanza (ordinan)Censire il dato nella tabella cg_refs_code, nella quale deve essere aggiunto un nuovo valore per il dominio TIPO_ATTO.
Aggiungere nuovi campi in tabella deposito_ordinanza_pc per gestire il flag ‘Atti trasmessi al Presidente’.
Per censire il nuovo stato procedimento, nella tabella cg_refs_code, deve essere aggiunto un nuovo valore per il dominio STATO_PROCEDIMENTO (atti trasmessi al Presidente).
Per la registrazione del nuovo template da associare all’ordinanza di Applicazione Provvisoria, occorre prevedere un nuovo record nella tabella template.
### Base Dati - REQ-SIE-009-04 (TDS - Registrazione data Esecutività Ordinanza Applicazione Provvisoria)
Per censire la nuova funzione (Registrazione data Esecutività Ordinanza Applicazione Provvisoria) occorre registrare l’informazione sulle seguenti tabelle:
funzione
funzione_profilo
relazione_funzioni
Aggiungere nuovi campi in tabella deposito_ordinanza_pc per gestire i campi di Data Esecutività dell’ordinanza.
### Base Dati - REQ-SIE-009-05 (TDS - Provvedimento di Conferma Ordinanza Applicazione Provvisoria)
Per questo requisito sono previsti nuovi valori ad integrazione delle attività già descritte in REQ-SIE-009-01. Quindi per questo requisito sono da considerare le attività del requisito REQ-SIE-009-01.
### Base Dati - REQ-SIE-009-06 (TDS - Gestione Revoca Ammissione Provvisoria)
Per censire il nuovo contenuto, nella tabella cg_refs_code, deve essere aggiunto un nuovo valore per il dominio OGGETTO_PROCEDIMENTO.
Sempre nella tabella cg_refs_code, devono essere mappati gli oggetti relativi al nuovo contenuto, prevedendo dei nuovi record per il dominio MOTIVO_PROVVEDIMENTO.
Sempre nella tabella cg_refs_code, devono essere mappati gli esiti relativi al nuovo contenuto, prevedendo dei nuovi record per il dominio ESITO_TENORE.
Aggiungere nuovi campi in tabella GENERALE_PROCEDIMENTO per gestire l’informazione circa la modalità con cui nasce il procedimento di revoca (semplice proposta oppure a seguito di sospensione). L’informazione sarà necessaria anche ai fini delle rilevazioni statistiche di cui al requisito REQ-SIE-009-11.
Per la registrazione del nuovo template da associare all’ordinanza di Revoca Ammissione Provvisoria, occorre prevedere un nuovo record nella tabella template.
### Dati - REQ-SIE-009-07 (TDS - Gestione Sostituzione della Misura Alternativa)
Per questo requisito è previsto un nuovo esito ad integrazione delle attività già descritte in REQ-SIE-009-06. Quindi per questo requisito sono da considerare le attività del requisito REQ-SIE-009-06.
### Base Dati - REQ-SIE-009-08 (UDS e TDS - Gestione Sospensione delle Pene Accessorie)
Per censire il nuovo contenuto, nella tabella cg_refs_code, deve essere aggiunto un nuovo valore per il dominio OGGETTO_PROCEDIMENTO.
Sempre nella tabella cg_refs_code, devono essere mappati gli oggetti relativi al nuovo contenuto, prevedendo dei nuovi record per il dominio MOTIVO_PROVVEDIMENTO.
Sempre nella tabella cg_refs_code, devono essere mappati gli esiti relativi al nuovo contenuto, prevedendo dei nuovi record per il dominio ESITO_TENORE.
Per la registrazione del nuovo template da associare all’ordinanza di Applicazione Provvisoria, occorre prevedere un nuovo record nella tabella template.
Tutte le attività finora elencate vanno previste sia per TDS che per UDS, quindi ci saranno due contenuti.
E’ da prevedere anche la creazione di una nuova tabella che ‘registri’ le pene accessorie oggetto di sospensione da parte della Sorveglianza.
### Base Dati - REQ-SIE-009-09
Nessun intervento strutturale a tabelle.
### Base Dati - REQ-SIE-009-10
Nessun intervento strutturale a tabelle.

### Base Dati - REQ-SIE-009-11
Nessun intervento strutturale a tabelle.

### Base Dati - REQ-SIE-009-12 (UDS - Introduzione del contenuto ‘Lavoro Pubblica Utilità)
Per censire il nuovo contenuto, nella tabella cg_refs_code, deve essere aggiunto un nuovo valore per il dominio OGGETTO_PROCEDIMENTO.
Sempre nella tabella cg_refs_code, devono essere mappati gli oggetti relativi al nuovo contenuto, prevedendo dei nuovi record per il dominio MOTIVO_PROVVEDIMENTO.
Sempre nella tabella cg_refs_code, devono essere mappati gli esiti relativi al nuovo contenuto, prevedendo dei nuovi record per il dominio ESITO_TENORE.
### Base Dati - REQ-SIE-009-13 (UDS - Integrazione del contenuto ‘Lavoro Esterno’)
Le attività di tipo Base Dati per questo requisito sono attività di modifica di diciture attuali nella tabella cg_refs_code,  per il dominio OGGETTO_PROCEDIMENTO in corrispondenza del contenuto (rv_low_value) U007.
La stessa attività di ‘rettifica’ va fata sempre nella cg_refs_code,  per il dominio MOTIVO_PROVVEDIMENTO in corrispondenza del contenuto (rv_high_value) U007.
### Base Dati - REQ-SIE-009-14 (UDS – TDS Integrazione Lista Mittente Atto)
Per censire la nuova voce da visualizzare nella combo box ‘mittente’, nella tabella cg_refs_code, deve essere aggiunto un nuovo valore per il dominio MITTENTE_ATTO.
### Base Dati - REQ-SIE-009- 15 (Aggiornamento Statistica Movimento Provvedimenti per Oggetti)
Modificare la procedura stato_oggetti_sius presente nel package Oracle ISPETTORATO_SIUS.
### Base Dati - REQ-SIE-009- 16 (Modifica pagina Richiesta Atti Istruttori)
Per registrare il valore del nuovo campo previsto per il requisito in oggetto, nella tabella NOTIFICA, deve essere aggiunto un nuovo campo DATA_RESTITUZIONE_ATTO.
### Base Dati - REQ-SIE-009- 17 (Statistica Atti Istruttori con Data Restituzione)
Per censire la nuova funzione (Statistica Atti Istruttori) occorre registrare l’informazione sulle seguenti tabelle:
funzione
funzione_profilo
relazione_funzioni

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
La metodologia utilizzata in questo obiettivo sarà Agile e, in particolare, si adotterà Scrum.
Nell’immagine che segue riportiamo un diagramma delle attività ed oggetti previsti dalla metodologia

La metodologia prevede i seguenti Ruoli:

| Ruolo | Responsabilità | Ownership |
| --- | --- | --- |
| Agile Team | Realizza il Prodotto
Decide le modalità di implementazione e si organizza in maniera autonoma | RTI |
| Scrum Master | Ruolo di facilitatore
Lavora per rimuovere gli ostacoli che il Team incontra nel raggiungere gli obiettivi dello Sprint
Solitamente un membro del Team | RTI |
| Product Owner | Decide le caratteristiche del prodotto da realizzare
Deve avere visione, autorità e disponibilità
Responsabile del product backlog | Giustizia |


I ruoli qui elencati sono da intendersi come ruoli operativi poiché il governo della fornitura è delegato ai ruoli descritti nel piano della qualità generale.

L’approccio prevede i seguenti oggetti
| Oggetto | Descrizione | Responsabilità |
| --- | --- | --- |
| User Story | È l’elemento base dello scrum. Contiene le informazioni necessarie per la realizzazione del software e la sua verifica (criteri di accettazione, oggetti a corredo, ecc…). 
La User Story deve essere, per quanto possibile, indipendente, valutabile e piccola | Stakeholder, Agile Team, Product Owner |
| Product Backlog | L’elenco prioritizzato delle User Stories | Product Owner |
| Sprint Backlog | Viene definito nello Sprint Planning e contiene la porzione di Product Backlog che deve essere realizzata nello sprint.
Avviato lo sprint non è modificabile | Product Owner
Agile Team |
| Prodotto (incrementato) | L’oggetto finale di uno sprint | Agile Team |
| Epic | Sono delle User Stories di alto livello che, normalmente, vengono utilizzate dove non si hanno informazioni sufficienti per specializzare la situazione | Stakeholder, Agile Team, Product Owner |


Infine, sono previste le seguenti riunioni/attività
| Riunione | Scopo | Durata | Partecipanti |
| --- | --- | --- | --- |
| Sprint Planning | Riunione iniziale di ciascuno sprint nel quale viene condiviso e pianificato l’output dello sprint. È in questa fase che viene definito lo Sprint Backlog | 0,75gg (per sprint di 3 settimane) | Product Owner
Agile Team
Scrum Master |
| Daily Scrum | Riunione del Team nel quale si fa il punto della situazione e si prendono le decisioni per le future attività | 15 minuti | Agile Team
Scrum Master |
| Sprint Review | Presentazione del lavoro fatto nel corso dello Sprint | 0,75gg (per sprint di 3 settimane) | Product Owner
Agile Team
Scrum Master
Stakeholder |
| Sprint Retrospective | Riunione utile alla discussione dell’andamento dello Sprint appena terminato e all’identificazione delle attività di miglioramento | 0,75gg (per sprint di 4 settimane) | Agile Team
Scrum Master |



Nel seguito è descritto l’approccio operativo
L’obiettivo, per la peculiarità del progetto stesso, seguirà un ciclo di vita ad hoc secondo quanto previsto dal PQG.

| Fase | Fase | Prodotto di fase | Criterio di uscita |
| --- | --- | --- | --- |
| Sprint 0 (Definizione) | Sprint 0 (Definizione) | Product Backlog su strumento di condivisione proposto dal RTI (Jira) | Attivazione |
|  | Sprint 1..n | Codice sorgente del prodotto complessivo aggiornato all’iterazione
Piano di test per quanto realizzato nell’iterazione
Modulo di conteggio (FP) per quanto realizzato nell’iterazione | Consegna dei prodotti di fase

Approvazione del collaudo dell’iterazione |
|  | Sprint di chiusura e collaudo | Specifica dei requisiti dell’obiettivo 
Codice sorgente del prodotto complessivo
Piano di test per il collaudo complessivo
Modulo di conteggio (FP) per quanto realizzato nell’iterazione
Documentazione utente | Consegna dei prodotti di fase

Approvazione del collaudo dell’iterazione |


Relativamente alla consuntivazione degli obiettivi si propone di procedere come riportato nella tabella che segue
| Fase | Fase | Effort Riconosciuto | Criterio di uscita |
| --- | --- | --- | --- |
| Definizione | Definizione | 10% dell’intero obiettivo stimato | Attivazione |
| Iterazione (Lotto) | Iterazione 0 | 0% | Sprint review |
| Iterazione (Lotto) | Iterazione 1..n | 60% di quanto effettivamente realizzato nell’iterazione | Approvazione dei casi d’uso e dei casi di test (Verifica di conformità): 20% del realizzato

Consegna dei prodotti di fase: 20% del realizzato

Approvazione del collaudo dell’iterazione: 20% del realizzato |
| Iterazione (Lotto) | Iterazione di chiusura | 60% di quanto effettivamente realizzato nell’iterazione | Approvazione dei casi d’uso e dei casi di test (Verifica di conformità): 20% del realizzato

Consegna dei prodotti di fase: 20% del realizzato

Approvazione del collaudo dell’iterazione: 20% del realizzato |
| Collaudo | Collaudo | 99,5% dei FP effettivamente realizzati al netto di quanto già fatturato nella fase di definizione e delle successive iterazioni | Accettazione
(verifica di conformità) |
| Avvio in Esercizio | Avvio in Esercizio | Sblocco della componente dipendente dagli indicatori di prestazioni | Valutazione qualità del software (verifica di conformità) |


Si riporta di seguito un esempio ipotizzando 4 Sprint:



## Piano delle attività
Il Piano di Lavoro sviluppa su un totale di 10 sprint della durata di 3 settimane ciascuno così suddivisi:
Sprint 0: corrispondente alla fase di definizione nel quale sarà predisposto il product backlog condiviso attraverso il sistema Jira
Sprint 1-8: sprint di sviluppo nel quale sarà realizzato il sistema complessivo attraverso l’approccio iterativo tipico dell’approccio scrum
Sprint 9: sprint di rilascio e collaudo complessivo del sistema nel quale saranno verificate le funzionalità del sistema complessivo e saranno prodotti tutti gli artefatti necessari al passaggio in esercizio
## Gantt
L’articolazione delle attività previste per l'intervento si sviluppa attraverso 10 sprint come precedentemente descritto.

INSERIRE GANTT

## Vincoli
N.A.

## Luogo di lavoro

Le attività saranno espletate presso le sedi del RTI o presso la sede della DGSIA.

# Dimensionamento
## Stima dell'effort previsto

La stima prevista a preventivo dell’intero obiettivo è di xxxx €


## Dettaglio costi
Di seguito si riporta il dettaglio dei costi a preventivo:




| ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i | ADD - S v i l u p p o   N u o v e   F u n z i o n i |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  | Complessità | Complessità | Complessità | Complessità | Complessità | Complessità |  |  |
| Function Types | Function Types | Function Types |  |  | Low | Low | Avg | Avg | High | High | Function |  |
|  |  |  |  |  | quantità | peso | quantità | peso | quantità | peso | Point |  |
| External Input | External Input | External Input |  |  | 0 | 3 | 0 | 4 | 119 | 6 | 714 |  |
| External Output | External Output | External Output |  |  | 0 | 4 | 0 | 5 | 37 | 7 | 259 |  |
| External Inquiry | External Inquiry | External Inquiry |  |  | 0 | 3 | 0 | 4 | 30 | 6 | 180 |  |
| Internal Logical File | Internal Logical File | Internal Logical File | Internal Logical File |  | 2 | 7 | 0 | 10 | 0 | 15 | 14 |  |
| External Interface File | External Interface File | External Interface File | External Interface File |  | 0 | 5 | 0 | 7 | 0 | 10 | 0 |  |
|  |  |  |  |  |  |  |  |  |  | Totale Function Point (FP) | 1.167 | ADD |
|  |  |  |  |  |  |  |  |  |  |  |  |  |
| CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) | CHGA - F u n z i o n i   M o d i f i c a t e  (After) |  |
|  |  |  |  |  | Complessità | Complessità | Complessità | Complessità | Complessità | Complessità |  |  |
| Function Types | Function Types | Function Types |  |  | Low | Low | Avg | Avg | High | High | Function |  |
|  |  |  |  |  | quantità | peso | quantità | peso | quantità | peso | Point |  |
| External Input | External Input | External Input |  |  | 0 | 3 | 0 | 4 | 52 | 6 | 312 |  |
| External Output | External Output | External Output |  |  | 0 | 4 | 0 | 5 | 15 | 7 | 105 |  |
| External Inquiry | External Inquiry | External Inquiry |  |  | 0 | 3 | 0 | 4 | 13 | 6 | 78 |  |
| Internal Logical File | Internal Logical File | Internal Logical File | Internal Logical File |  | 0 | 7 | 0 | 10 | 0 | 15 | 0 |  |
| External Interface File | External Interface File | External Interface File | External Interface File |  | 0 | 5 | 0 | 7 | 0 | 10 | 0 |  |
|  |  |  |  |  |  |  |  |  |  | Totale Function Point (FP) | 495 | CHGA |
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