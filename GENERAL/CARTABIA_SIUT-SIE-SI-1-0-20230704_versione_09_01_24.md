---
uniqueName: cartabiasiut-sie-si-1-0-20230704versione090124
displayName: "CARTABIA SIUT SIE SI 1 0 20230704 versione 09 01 24"
category: "GENERAL"
tags: []
---

# CARTABIA_SIUT-SIE-SI-1.0-20230704_versione_09_01_24

> **File originale:** `MEV/SCHEDA_035/CARTABIA_SIUT-SIE-SI-1.0-20230704_versione_09_01_24.docx`  
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
| Elaborato da | Umberto Mignogna |
| Verificato da | Vito Bufi |
| Approvato da | Paolo Ceccanti |
| Data approvazione | 04/07/2023 |
| Livello di riservatezza | L3 |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 04/07/2023 |  | Prima Emissione |
|  |  |  |  |
|  |  |  |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Aurora Garofalo | Amministrazione |  | Responsabile Unico Procedimento |
| Oris Orlando | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Fabio Mazzocchi | RTI |  | Responsabile Manutenzione Correttiva |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Responsabile PMO |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Edoardo Lamuraglia | RTI |  | Referente qualità |
| Francesco Rosati | RTI |  | Referente qualità |
| Andrea Castorino
Alessandro Lanari | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |


INDICE DEI CONTENUTI

1	Introduzione	6
1.1	Scopo del documento	6
1.2	Riferimenti	6
1.3	Glossario	7
1.3.1	Definizioni	7
1.3.2	Acronimi e abbreviazioni	7
2	Architettura del Sistema	9
2.1	Architettura	9
2.2	WEB services	9
2.3	XSD	9
2.4	Configurazione	9
2.5	Tutorial	9
3	Descrizione dell’Intervento	10
3.1	Applicazione Pene Sostitutive (art. 62 L. 689/81)	10
3.2	Esecuzione Pene Sostitutive	11
3.3	Sospensione Esecuzione Pene Sostitutive	13
3.4	Autorizzazione Pene Sostitutive	16
3.5	Modifica Modalità di esecuzione Pene Sostitutive	17
3.6	Revoca Autorizzazione Pene Sostitutive	18
3.7	Revoca Autorizzazione Pene Sostitutive	20
3.7.1	Sospensione Provvisoria Pena Sostitutiva per inosservanza prescrizioni	21
3.8	Diffida al puntuale rispetto delle prescrizioni – pene sostitutive	22
3.9	Gestione Licenza - pene sostitutive	23
3.10	Licenza - pene sostitutive - Inosservanza prescrizioni (art. 69 L. 689/81)	25
3.11	Sospensione lavoro pubblica utilità sostitutivo	26
3.12	Rinvio dell’esecuzione  pena sostitutiva	27
3.13	Revoca e Conversione pena pecuniaria sostitutiva	28
3.14	Sopravvenienza nuovo Titolo - pene sostitutive	30
3.15	Sospensione esecuzione pene accessorie	31
3.16	Conversione/Rateizzazione Pena Pecuniaria Sostitutiva	32
3.17	Conversione pene pecuniarie irrogate dal Giudice di Pace	34
3.18	Gestione Procedimenti Esecuzione Pene Sostitutive	34
3.19	Gestione Licenze – Pene Sostitutive	36







# Introduzione
## Scopo del documento
Il presente documento riporta le specifiche di intervento che saranno realizzate nell’ambito del sistema SIES, sottosistema SIUS, al fine di soddisfare i requisiti espressi dall’Amministrazione in relazione alla richiesta di adeguamento normativo del Sistema, nella sua interezza, al d.lgs. 10 ottobre 2022, n. 150  cd Riforma Cartabia,  alla Riforma Cartabia.

L’intervento in oggetto è stato richiesto con comunicazione m_dg.DOG07AR.04/05/2023.0000747.U.
Rientra nel servizio di Manutenzione Evolutiva ed è classificato come di seguito riportato:

| Scheda di Intervento | 2023_35 |
| --- | --- |
| Oggetto | Integrazione Cartabia in SIUS |
| Complessità | Alta |
| Servizio | MEV |


Tale documento espone gli interventi attinenti alle funzioni da prevedere nel sistema in base alle novità normative della cd Riforma Cartabia(maggiorenni e minorenni).
Con lo scopo di rendere l’intervento coerente ed auto consistente gli interventi dovranno tener conto dell’integrazione con gli altri sottosistemi (SIEP e SIGE).

## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF1 | m_dg.DOG07AR.04_05_2023.0000747.U_Richiesta_scheda_2023-35_SIES_Cartabia_con_SIUS_signed | Richiesta Scheda di Intervento |
| RIF2 |  |  |
| RIF3 |  |  |
| RIF4 |  |  |
| RIF5 |  |  |
| RIF6 |  |  |


## Glossario
## Definizioni
| Definizione | Descrizione |
| --- | --- |
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



# Architettura del Sistema
## Architettura
L’intervento in oggetto non introduce variazioni architetturali, rispetto al sistema attuale.
## WEB services
N.A.
## XSD
N.A.
## Configurazione
N.A.
## Tutorial
N.A.
# Descrizione dell’Intervento
Di seguito si riportano gli interventi necessari nel sottosistema SIUS per adeguarlo alle modifiche apportate dalla cd “Riforma Cartabia” ai singoli articoli del c.p.p.
Per ciascun provvedimento riportato nei paragrafi successivi dalla form di Dettaglio sarà possibile attivare le funzioni di stampa, validazione, modifica e cancellazione.
## Applicazione Pene Sostitutive (art. 62 L. 689/81)
In relazione all’art. 62 L. 689/81 la riforma non parla più di Sanzioni sostitutive ma di Pene Sostitutive nelle forme di Semilibertà sostitutiva e Detenzione Domiciliare sostitutiva, che possono essere applicate dal giudice in caso di condanna alla reclusione o all’arresto non superiori a quatto anni. Gli Uffici di Sorveglianza (UDS/UDSM) sono pertanto chiamati a pronunciarsi sull’applicabilità di tali pene sostitutive. A tal fine bisognerà prevedere la gestione di un nuovo procedimento con contenuto di “Applicazione Pene Sostitutive”.

Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Applicazione Pene Sostitutive
Al nuovo contenuto vanno associati i seguente oggetti:
Semilibertà sostitutiva (art. 55 - 62 L. 689/1981)
Detenzione domiciliare sostitutiva (art. 56 - 62 L. 689/1981)
e i seguenti esiti
Determina le modalità di esecuzione
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dispone restituzione atti al PM
Dichiara la propria incompetenza
L’aggiunta dei suddetti elementi permetterà all’Ufficio di poter iscrivere procedimenti di Applicazione Pene Sostitutive, collegandosi direttamente al procedimento SIEP o a seguito di presa in carico di Richiesta Applicazione Pene Sostitutive trasmesse dalle Procure.
Per la successiva definizione bisognerà realizzare l’ordinanza di applicazione delle pene sostitutive, che potrebbe riproporre gli stessi campi previsti per l’Applicazione delle sanzioni sostitutive

A seguito della Conferma inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload, Validazione.
L’ordinanza seguirà il normale percorso di altri provvedimenti, verrà quindi depositato e validato per essere trasmesso allo stesso Ufficio o ad altro ufficio, che procederà alla presa in carico e all’iscrizione di un procedimento di esecuzione della pena sostitutiva (cd Fascicolo padre) al quale faranno riferimento tutti i procedimenti afferenti alla gestione dell’esecuzione.
L’ordinanza di applicazione viene trasmessa anche alla Procura perché provveda all’annotazione.
Nella maschera deve essere eliminato il campo “Ufficio competente”
## Esecuzione Pene Sostitutive
Dopo che il Magistrato di Sorveglianza ha determinato le modalità di esecuzione della pena sostitutiva invia l’ordinanza all’Ufficio di Sorveglianza competente per l’esecuzione della pena sostitutiva. L’Ufficio iscrive un fascicolo che farà da collettore per tutti i procedimenti che si apriranno durante l’esecuzione ad essa attinenti. Questa tipologia di procedimento, come già fatto per l’esecuzione delle misure alternative, delle misure di sicurezza e delle sanzioni sostitutive, sarà identificato comunemente come “Fascicolo padre”, mentre tutti i procedimenti relativi ad atti relativi alla fase di esecuzione, che saranno caratterizzati da una doppia numerazione il numero identificativo del procedimento e il numero del fascicolo di Esecuzione Pene Sostitutive, saranno identificati comunemente come “Fascicoli Figli”.

Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Esecuzione Pene Sostitutive
Al nuovo contenuto vanno associati i seguente oggetti:
Semilibertà sostitutiva (art. 55 - 62 L. 689/1981)
Detenzione domiciliare sostitutiva (art. 56 - 62 L. 689/1981)
Lavoro di pubblica utilità sostitutivo (art. 56 bis L. 689/1981 – 55 DL 274/20)
Per questo tipo di procedimento non sono previsti esiti.

Per questo procedimento, come negli altri casi di procedimenti di Esecuzione, il sistema presenterà la seguente form



che in caso di iscrizione da presa in carico dell’ordinanza di applicazione presenterà già precompilati i campi Tipo Atto, Data atto, Mittente, Sede Mittente, Anno e Numero Ordinanza.
La form simile, ma priva di dati precompilati, si presenterà anche in caso di iscrizione da Procedimento SIEP, iscrizione da Soggetto e Iscrizione Procedimento Collegato.

A seguito della Conferma il sistema inserirà un fascicolo “padre” di esecuzione pene sostitutive e presenterà la seguente form


Da questa form cliccando su Anno e Numero Esecuzione Pena Sostitutiva si riceverà la seguente form


da cui sarà possibile Iscrivere un procedimento “figlio” o modificare i dati relativi alla durata ed al luogo di esecuzione della pena sostitutiva.

Si afferma che il semilibero è sottoposto ad un programma di trattamento predisposto dall’Uepe ed approvato dal giudice. Di conseguenza occorre inserire un nuovo contenuto, costituente procedimento “ordinario” e non figlio, che potremmo chiamare “Programma di trattamento per semilibertà sostitutiva (art. 55 L. 689/81)” ed il relativo oggetto “Approvazione programma di trattamento per semilibertà sostitutiva (art. 55 L. 689/81)”. Gli esiti saranno: Approva – Restituisce programma – Restituisce programma con osservazioni – NLP – Incompetenza – Inammissibilità.

## Sospensione Esecuzione Pene Sostitutive
L’art. 660 c.p.p.	 al comma 15 prevede di richiedere la sospensione dell’esecuzione della pena sostitutiva nel caso che il soggetto chieda  l’ammissione  al  pagamento  rateale  dopo l’inizio dell’esecuzione, d’altra parte l’art. 68 L. 689/81 prevede la Sospensione pena sostitutiva per sopravvenienza misura di sicurezza detentiva (art. 68  L.  689/81), la Sospensione  pena  sostitutiva  per  sopravvenienza  pena  detentiva  (art.  68 L.
689/81).
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Sospensione Esecuzione Pene Sostitutive
Al nuovo contenuto vanno associati i seguente oggetti:
Sospensione pena sostituiva per ammissione al pagamento rateale (art.660 c.15 c.p.p.)
Sospensione pena sostituiva per sopravvenienza misura di sicurezza detentiva (art. 68 L. 689/1981)
Sospensione pena sostituiva per sopravvenienza pena detentiva (art. 68 L. 689/1981)
e i seguenti esiti
Sospende
Non sospende
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS



A seguito della compilazione della form e successiva Conferma, il sistema presenterà la form di Dettaglio del procedimento “figlio” del procedimento di esecuzione pena sostitutiva

Caratterizzata da un proprio Anno e Numero e dal numero del procedimento padre (EPS).
Per i procedimenti di sospensione della sanzione sostitutiva SIUS permette di definire il procedimento con un decreto o una ordinanza, che riportano il seguente contenuto

N.B. ELIMINARE il campo “Tribunale di Sorveglianza competente”
Puo essere adottata la suddetta form anche per la sospensione della pena sostitutiva?  SI
Deve essere prevista la possibilità di esprimersi con ordinanza e decreto?    SI
Al momento per questi provvedimenti sono previsti 6 modelli di stampa: Ordinanza Sospensione per pena detentiva, Ordinanza Sospensione per violazione prescrizione, Ordinanza generica, Decreto Sospensione per pena detentiva, Decreto Sospensione per violazione prescrizione, Decreto generica.  N.B. I template evidenziati in verde vanno eliminati

A questo punto, a mio parere, dobbiamo cogliere l’occasione per rivedere completamente quella che è l’attuale gestione dei differimenti delle esecuzioni delle sanzioni sostitutive. Al momento, infatti, tale gestione è eccessivamente macchinosa e molto complessa da utilizzare da parte dell’utente finale. Deve essere necessariamente rivista e resa più simile a quella relativa all’esecuzione delle misure alternative, soprattutto visto che il numero di pene sostitutive da gestire sarà molto più alto di quello di sanzioni sostitutive attualmente in corso. In pratica, occorre replicare quanto accade nella maschera del fascicolo padre di EMA, dove si può inserire manualmente la data di inizio esecuzione, quella del termine inziale e quella del termine attuale.

## Autorizzazione Pene Sostitutive
L’art. 64 e seguenti legge 689/1981 (vedi anche art. 107 L. 689/81)  prevede di richiedere delle Autorizzazioni nel corso dell’esecuzione della pena sostitutiva.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Autorizzazione Pene Sostitutive
Al nuovo contenuto vanno associati i seguente oggetti:
Autorizzazione Pene Sostitutive
Ulteriore autorizzazione  Pene Sostitutive
e i seguenti esiti
Autorizza
Non autorizza
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto.

Per i procedimenti di autorizzazione della sanzione sostitutiva SIUS permette di definire il procedimento solo con un decreto, che riporta il seguente contenuto


Puo essere adottata la suddetta form anche per l’autorizzazione della pena sostitutiva?  SI
Deve essere prevista la possibilità di esprimersi anche con ordinanza?  NO
Al momento per questo provvedimento sono previsti 3 modelli di stampa: Decreto Autorizzazione generico, Decreto Autorizzazione fuori sede, Decreto Autorizzazione Uso Patente.  SI

## Modifica Modalità di esecuzione Pene Sostitutive
L’art. 64 e seguenti legge 689/1981 (vedi anche art. 107 L. 689/81)  prevede di richiedere la Modifica delle modalità di esecuzione nel corso dell’esecuzione della pena sostitutiva.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Modifica modalità di esecuzione/luogo esecuzione pene sostitutive (art. 64 L. 689/81)
Al nuovo contenuto vanno associati i seguente oggetti:
Modifica modalità esecuzione semilibertà  sostitutiva  (art.  64  L.  689/81)
Modifica luogo esecuzione semilibertà  sostitutiva  (art.  64  L.  689/81)
Modifica modalità esecuzione detenzione   domiciliare sostitutiva  (art.  64  L.  689/81)
Modifica luogo esecuzione detenzione   domiciliare sostitutiva  (art.  64  L.  689/81)

e i seguenti esiti
Modifica permanente prescrizioni
Modifica provvisoria prescrizioni
Modifica luogo esecuzione
Rigetta
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto.

Per i procedimenti di autorizzazione della sanzione sostitutiva SIUS permette di definire il procedimento con decreto o con ordinanza, che riporta il seguente contenuto


Puo essere adottata la suddetta form anche per la modifica modalità di esecuzione della pena sostitutiva?  SI
Deve essere prevista la possibilità di esprimersi anche con ordinanza e decreto?  SI
Al momento per questi provvedimenti sono previsti 4 modelli di stampa: Ordinanza Modifica Permanente Prescrizioni, Ordinanza Generica, Decreto Modifica Permanente Prescrizioni, Decreto Generico.  OK

## Revoca Autorizzazione/Modifica Prescrizioni Pene Sostitutive
L’art. 64 e seguenti legge 689/1981 (vedi anche art. 107 L. 689/81)  prevede che possa essere richiesta la Revoca dell’autorizzazione o della modifica delle prescrizioni, concessa precedentemente, nel corso dell’esecuzione della pena sostitutiva.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Revoca autorizzazione/Modifica Prescrizioni pene sostitutive
Al nuovo contenuto vanno associati i seguente oggetti:
Revoca autorizzazione pene sostitutive
Revoca Modifica Prescrizioni pene sostitutive
e i seguenti esiti
Revoca
Non revoca
Rigetta
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto.

Per i procedimenti di Revoca autorizzazione della sanzione sostitutiva SIUS permette di definire il procedimento solo con decreto, che riporta il seguente contenuto


Puo essere adottata la suddetta form anche per la Revoca Autorizzazione della pena sostitutiva?  SI, eliminando il campo “Tribunale di Sorveglianza competente”
Deve essere prevista la possibilità di esprimersi anche con ordinanza? SI
Al momento per questo provvedimento è previsto un solo modello di stampa: Decreto Generico. Aggiungere ORDINANZA GENERICA

## Revoca Autorizzazione (cancellare AUTORIZZAZIONE) Pene Sostitutive
Gli artt. 66 – 72 (ELIMINARE IL 72) – 108  legge 689/1981  prevedono un istituto parzialmente nuovo, in quanto in precedenza il MS si limitava a sospendere l’esecuzione delle sanzioni sostitutive e trasmetteva gli atti al TDS (o
trasmetteva al TDS senza sospendere), mentre ora è il Magistrato di Sorveglianza a disporre la revoca/sostituzione delle pene sostitutive, non più con decreto ma con ordinanza.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Revoca pena sostitutiva per inosservanza delle prescrizioni art. 66 – 72 (ELIMINARE IL 72) – 108 L. 689/81
Al nuovo contenuto vanno associati i seguente oggetti:
Revoca detenzione domiciliare sostitutiva per inosservanza prescrizioni (art. 66 - 72 (ELIMINARE IL 72) L. 689/81)
Revoca semilibertà sostitutiva per inosservanza prescrizioni (art. 66 - 72 (ELIMINARE IL 72)L. 689/81)
Revoca detenzione domiciliare sostitutiva derivante da conversione per inosservanza prescrizioni (art. 108 L. 689/81)
Revoca semilibertà sostitutiva derivante da conversione per inosservanza prescrizioni (art. 108 L. 689/81)
e i seguenti esiti
Revoca e converte in pena detentiva
Revoca e converte in altra pena sostitutiva
Non Revoca
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto.

Per questo tipo di procedimento si può ipotizzare un ordinanza del tipo seguente


In cui nella combo box Pena Sostitutiva più grave il sistema presenterà le 3 pene sostitutive previste per il procedimento di esecuzione (vedi par. 3.2).
Da decidere i modelli di stampa da associare.
L’ordinanza di revoca può essere impugnata dinanzi al TDS. Di conseguenza occorre inserire lato TDS un nuovo contenuto/oggetto, denominato “Reclamo avverso Revoca Pene Sostitutive” ed i cui esiti potrebbero essere: Accoglie reclamo; Accoglie reclamo e converte in altra pena sostitutiva; Rigetta; NLP; Inammissibilità; Incompetenza, utilizzando una maschera con alcuni dei dati particolari previsti in quella dell’UDS, vale a dire “Pena sostitutiva più grave” e “Rideterminazione quantum pena da espiare”


Tutto quanto sopra riportato deve essere replicato creando un nuovo contenuto (e relativi oggetti) da utilizzare nel caso in cui la Revoca della pena sostitutiva non derivi dalla inosservanza delle prescrizioni bensì dalla sopravvenienza di una condanna, stante quanto prescritto dall’art. 72 L. 689/81.
Di conseguenza, occorre creare un nuovo contenuto e dei nuovi oggetti dove, al posto della dicitura “per inosservanza delle prescrizioni” si deve riportare la dicitura “per intervenuta condanna” e sostituire l’art. 66 con l’art. 72 come riferimento normativo.
### Sospensione Provvisoria Pena Sostitutiva per inosservanza prescrizioni N.B. TUTTO QUANTO RIPORTATO NEL PRESENTE PARAGRAFO DEVE ESSERE ELIMINATO, IN QUANTO L’ISTITUTO DELLA SOSPENSIONE PER INOSSERVANZA PRESCRIZIONI NON E’ PIU’ UTILIZZATO
Considerato, poi, che la revoca deve essere disposta previa fissazione di una udienza, il Magistrato dovrà avere la possibilità di sospendere provvisoriamente la pena sostitutiva , al fine di evitare che la stessa prosegua nel periodo intercorrente tra la segnalazione e l’udienza.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Sospensione pena sostitutiva per inosservanza prescrizioni
Al nuovo contenuto vanno associati i seguente oggetti:
Sospensione pena sostitutiva per inosservanza prescrizioni
e i seguenti esiti
Sospende
Non Sospende
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto.

Per questo tipo di procedimento si può ipotizzare un ordinanza o un decreto del tipo seguente

Da decidere i modelli di stampa da associare.

## Diffida al puntuale rispetto delle prescrizioni – pene sostitutive
Considerato che  l’istituto  della  pene  sostitutive  dovrebbe  avere  una  ampia diffusione, è opportuno inserire anche un contenuto specifico per la diffida, sulla falsariga di quanto accade nel caso di EMA.

Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Diffida al puntuale rispetto delle prescrizioni  - pene sostitutive
Al nuovo contenuto vanno associati i seguente oggetti:
Convocazione per puntuale rispetto prescrizioni – pene sostitutive
Diffida al puntuale rispetto prescrizioni – pene sostitutive
e i seguenti esiti
Diffida
Non Diffida
Convoca
Non Convoca
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto.

Per questo tipo di procedimento si può ipotizzare un decreto del tipo di quello previsto per l’EMA

Puo essere adottata la suddetta form anche per il procedimento in esame? SI, però bisogna eliminare i campi: Tribunale di Sorveglianza competente e Ufficio di Sorveglianza Competente.
Deve essere prevista la possibilità di esprimersi anche con ordinanza?  NO
Al momento per questo provvedimento sono previsti 2 modelli di stampa: Decreto generico, Decreto diffida puntuale rispetto prescrizioni.  OK
## Gestione Licenza - pene sostitutive
## L’art.  69 legge 689/1981, al primo comma,  prevede un istituto parzialmente nuovo le licenze per i soggetti sottoposti a pene sostitutive.

Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Licenza - pene sostitutive (art. 69 L. 689/81)
Al nuovo contenuto vanno associati i seguente oggetti:
Licenza - pene sostitutive (art. 69 L. 689/81)
e i seguenti esiti
Concede
Rigetta
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto.

Per questo tipo di procedimento si può ipotizzare un decreto simile a quello già previsto in SIUS per le altre tipologie di licenza, es.


Puo essere adottata la suddetta form anche per il procedimento in esame?  SI
Al momento per questo provvedimento sono previsti 5 modelli di stampa: Decreto generico, Decreto concessione licenza semilibero, Decreto Non Luogo a Provvedere licenza semilibero, Decreto Rigetto licenza semilibero, Decreto Inammissibilità licenza semilibero, Decreto Incompetenza licenza semilibero.
N.B. CANCELLARE le diciture e i modelli di stampa evidenziati in verde
## Licenza - pene sostitutive - Inosservanza prescrizioni (art. 69 L. 689/81)
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Licenza - pene sostitutive – inosservanza prescrizioni (art. 69 L. 689/81)
Al nuovo contenuto vanno associati i seguente oggetti:
Valutazione  revoca  Licenza – pene  sostitutive  (artt. 53  bis  O.P. - 69  L.  689/81)
Esclusione computo Licenza – pene sostitutive (artt. 53 bis O.P. - 69 L. 689/81)
e i seguenti esiti
Revoca
Non Revoca
Dichiara validamente espiata la pena
Dichiara non validamente espiata la pena
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto.

Per questo tipo di procedimento si può ipotizzare un decreto simile a quello già previsto in SIUS per la Licenza per internati – inosservanza prescrizioni


Puo essere adottata la suddetta form anche per il procedimento in esame?  SI
Al momento per questo provvedimento sono previsti 2 modelli di stampa: Decreto revoca licenza internato, Decreto scomputo licenza internato.
N.B. CANCELLARE le diciture evidenziate in verde


## Sospensione lavoro pubblica utilità sostitutivo
L’art.  69 legge 689/1981, al secondo comma,  prevede l’applicazione di una particolare forma di sospensione relativa esclusivamente al lavoro di pubblica utilità.

Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Sospensione lavoro di pubblica utilità sostitutivo (art. 69 c. 2 L. 689/81)
Al nuovo contenuto vanno associati i seguente oggetti:
Sospensione lavoro di pubblica utilità sostitutivo (art. 69 c. 2 L. 689/81)
e i seguenti esiti
Sospende
Non sospende
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto.

Per questo tipo di procedimento si può ipotizzare un decreto simile a quello già previsto in SIUS per le altre tipologie di licenza, vedi par. 3.9.

## Rinvio dell’esecuzione  pena sostitutiva
N.B. C’è stato un errore nelle indicazioni fornite dal GdL, in quanto anche per le pene sostitutive si applica la disciplina prevista dall’art. 684 c.p.p. e, quindi, quella della decisione provvisoria del MdS e del successivo passaggio al TdS. Di conseguenza, si può riprendere, con le opportune modifiche, quanto già esistente sial lato UDS che lato TDS con riferimento alle SANZIONI SOSTITUTIVE.
Di conseguenza, occorre inserire:
lato UDS, il contenuto “Rinvio esecuzione Pena Sostitutiva Ex art. 684 comma 2 c.p.p.” e gli oggetti: “Differimento Pena Sostitutiva facoltativo art. 147 c.p. - art. 69 L. 689/81” - “Differimento Pena Sostitutiva obbligatorio art. 146 c.p. - art. 69 L. 689/81” – “Applicazione al semilibero della detenzione domiciliare sostitutiva – Art. 69 L. 689/81”
lato TDS, il contenuto “Rinvio dell’Esecuzione Pena Sostitutiva Ex art. 684 c.p.p.” e gli oggetti  “Differimento facoltativo della Pena Sostitutiva in attesa di grazia – Art. 147 n. 1 c.p. - art. 69 L. 689/81” - “Differimento facoltativo della Pena Sostitutiva per grave infermità – Art. 147 n. 2 c.p. - art. 69 L. 689/81” - “Differimento facoltativo della Pena Sostitutiva per maternità – Art. 147 n. 3 c.p. - art. 69 L. 689/81” - “Differimento obbligatorio della Pena Sostitutiva nei confronti di donna incinta – Art. 146 n. 1 c.p. - art. 69 L. 689/81” - “Differimento obbligatorio della Pena Sostitutiva nei confronti di madre infante di età inferiore ad anni 1 – Art. 146 n. 2 c.p. - art. 69 L. 689/81” - “Differimento obbligatorio della Pena Sostitutiva nei confronti di persona affetta da malattia – Art. 146 n. 3 c.p. - art. 69 L. 689/81” - “Applicazione al semilibero della detenzione domiciliare sostitutiva – Art. 69 L. 689/81”,
Per quel che concerne, invece, le pene sostitutive derivanti da Conversione di pene pecuniarie, considerato che andrebbero replicati tutti gli oggetti esistenti all’interno dei contenuti TDS/UDS inserendo il relativo riferimento normativo, si rischierebbe di rendere troppo corposa la maschera degli oggetti (soprattutto lato TDS). Di conseguenza, proporrei di inserire nuovi contenuti/oggetti, denominati:
lato UDS, “Rinvio esecuzione Pena Sostitutiva derivante da Conversione - artt. 69 – 107 L. 689/81”  e “Differimento Pena Sostitutiva derivante da Conversione - artt. 69 – 107 L. 689/81” - “Differimento Pena Sostitutiva derivante da Conversione - artt. 69 – 107 L. 689/81” – “Applicazione al detenuto sottoposto alla Semilibertà Sostitutiva derivante da Conversione della Detenzione Domiciliare Sostitutiva - artt. 69 – 107 L. 689/81). Per quello che concerne gli esiti, si possono replicare quelli utilizzati nell’altro tipo di Rinvio della pena sostitutiva, che vanno bene sia nel caso di decisione monocratica “definitiva” che “provvisoria”
lato TDS, “Rinvio dell’Esecuzione Pena Sostitutiva derivante da Conversione - artt. 69 – 107 L. 689/81”  e “Differimento facoltativo della Pena Sostitutiva derivante da conversione in attesa di grazia – Art. 147 n. 1 c.p. - artt. 69 – 107 L. 689/81” - “Differimento facoltativo della Pena Sostitutiva derivante da conversione per grave infermità – Art. 147 n. 2 c.p. - artt. 69 – 107 L. 689/81” - “Differimento facoltativo della Pena Sostitutiva derivante da conversione per maternità – Art. 147 n. 3 c.p. - artt. 69 – 107 L. 689/81” - “Differimento obbligatorio della Pena Sostitutiva derivante da conversione nei confronti di donna incinta – Art. 146 n. 1 c.p. - artt. 69 – 107 L. 689/81” - “Differimento obbligatorio della Pena Sostitutiva derivante da conversione nei confronti di madre infante di età inferiore ad anni 1 – Art. 146 n. 2 c.p. - artt. 69 – 107 L. 689/81” - “Differimento obbligatorio della Pena Sostitutiva derivante da conversione nei confronti di persona affetta da malattia – Art. 146 n. 3 c.p. - artt. 69 – 107 L. 689/81” - “Applicazione al detenuto sottoposto alla Semilibertà Sostitutiva derivante da Conversione della Detenzione Domiciliare Sostitutiva - artt. 69 – 107 L. 689/81).  Per quello che concerne gli esiti, si possono replicare quelli utilizzati nell’altro tipo di Rinvio della pena sostitutiva.

e i seguenti esiti:
lato UDS
Concede
Proroga
Rigetta
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

lato TDS
Concede per un periodo
Proroga per un periodo
Rigetta
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto.

Per questo tipo di procedimento si può ipotizzare un decreto simile a quello già previsto in SIUS per il Rinvio esecuzione sanzione sostitutiva


Puo essere adottata la suddetta form anche per il procedimento in esame? Occorre utilizzare le form già esistenti, sia lato TDS che UDS, per il Rinvio Esecuzione Pena
Al momento per questo provvedimento è previsto solo 1 modello di stampa: Decreto generico. OK lato UDS, per il TDS riprendere quelli del Rinvio esecuzione della pena

## Revoca e Conversione pena pecuniaria sostitutiva
L’art.  71 legge 689/1981 prevede  che  la  pena  pecuniaria sostitutiva non  pagata  possa  essere  convertita  nella  semilibertà,  nella  detenzione  domiciliare  sostitutive  ovvero  nel  lavoro  di pubblica utilità sostitutivo.

Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Revoca e Conversione pena pecuniaria  sostitutiva (art.71 L. 689/81)
Al nuovo contenuto vanno associati i seguente oggetti:

Revoca e Conversione pena pecuniaria sostitutiva per mancato pagamento (art.71 L. 689/81)

e i seguenti esiti
Revoca  e  converte  pena sostitutiva in  semilibertà  sostitutiva
Revoca  e  converte pena sostitutiva in  detenzione domiciliare sostitutiva
Revoca e  converte pena sostitutiva in  lavoro di  pubblica utilità sostitutivo
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

Questo tipo di procedimento non presuppone l’esistenza del fascicolo di Esecuzione Pena Sostitutiva, pertanto l’iscrizione, fuoriuescendo dalla logica procedimenti “padre” – “figli”, avverrà utilizzando le attuali funzionalità di iscrizione previste in SIUS.

Per questo tipo di procedimento si può ipotizzare un’ordinanza, simile a quello già previsto in SIUS per la Conversione della pena pecuniaria,


N.B. Il quantum di pena da convertire non deve essere “prestampato”, ma deve essere presente un campo dove inserirlo manualmente, in quanto può non coincidere con la somma iniziale.
A seguito della Conferma, della validazione e deposito di questa ordinanza, l’ufficio iscriverà un procedimento di Esecuzione Pena Sostitutiva (vedi par. 3.2).





## Sopravvenienza nuovo Titolo - pene sostitutive
L’art.  76 legge 689/1981 prevede  che  la sussistenza dei requisiti dell’applicazione della  pena  sostitutiva vengano rivalutati dal magistrato in presenza di nuovi  titoli esecutivi.

Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Sopravvenienza nuovo titolo - Pene sostitutive (art. 76 L. 689/81 – 51-bis O.P.)
Al nuovo contenuto vanno associati i seguente oggetti:

Valutazione su permanenza  quantum  pena  per  semilibertà  sostitutiva  (Art.  55  L. 689/81 – 51-bis O.P.)
Valutazione su permanenza quantum pena per detenzione domiciliare  sostitutiva  (Art.  56  L. 689/81 – 51-bis O.P.)
Valutazione su permanenza quantum pena per lavoro di pubblica utilità (Art.  56 bis L. 689/81 – 51-bis O.P.)

e i seguenti esiti
Estende la pena sostitutiva
Dischiara inefficace/cessata la pena sostitutiva
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà simile a quella dei procedimenti  figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione  e di dettaglio del procedimento sono identiche a quelle descritte al par. 3.3, tranne per il contenuto e oggetto.

In realtà, si tratta di un fascicolo figlio “derivato”, vale a dire non iscritto con le modalità utilizzate per gli altri fascicoli figli, ma partendo da una iscrizione ordinaria (vedi “sopravvenienza nuovo titolo”)
Per questo tipo di procedimento si può ipotizzare un’ordinanza, simile a quello già previsto in SIUS per la Misura Alternativa, es.



L’Amministrazione fornirà i modelli di stampa necessari.

## Sospensione esecuzione pene accessorie
L’art.  51 quater O.P. (disciplina delle pene accessorie in caso di concessione di misure alternative) prevede  la sospensione dell’esecuzione delle pene accessorie  in caso di misure alternative o di pene sostitutive.

Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Sospensione esecuzione pene accessorie (art. 51-quater O.P.)
Al nuovo contenuto vanno associati i seguente oggetti:

Sospensione esecuzione pene accessorie – Misure alternative (art. 51-quater O.P.)
Sospensione esecuzione pene accessorie –  Pene sostitutive (Art.  76  L. 689/81 – 51-quater O.P.)
e i seguenti esiti
Sospende
Non sospende
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

Questo tipo di procedimento non presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva/Esecuzione Misura Alternativa, pertanto l’iscrizione, fuoriuscendo dalla logica procedimenti “padre” – “figli”, avverrà utilizzando le attuali funzionalità di iscrizione previste in SIUS.

Per questo tipo di procedimento si può ipotizzare un ordinanza del tipo seguente

Per l’indicazione del tipo di pena accessoria, direi di inserire un menu a tendina contenente tutti i tipi di pena accessoria di cui all’art. 19 c.p., e quindi:

1) interdizione dai pubblici uffici;
2) interdizione da una professione o da un'arte;
3) interdizione legale;
5) incapacità di contrattare con la pubblica amministrazione;
5-bis) estinzione del rapporto di impiego o di lavoro;
6) decadenza o la sospensione dall'esercizio della responsabilità genitoriale;
7) sospensione dall'esercizio di una professione o di un'arte;
8) pubblicazione della sentenza penale di condanna
Per quel che concerne la durata della pena accessoria irrogata, andrà inserito un campo libero e un flag per l’indicazione di quella perpetua.

L’Amministrazione fornirà i modelli di stampa necessari.

Lo stesso genere di procedura deve essere replicata anche lato TDS, in quanto le misure alternative possono essere concesse sia dal MDS che dal TDS, con la sostanziale differenza che il TDS può disporre la sospensione della pena accessoria solo nel caso di concessione di misure alternative. Di conseguenza, si può replicare tutto quanto previsto per l’UDS, tranne il secondo oggetto (Sospensione esecuzione pene accessorie –  Pene sostitutive (Art.  76  L. 689/81 – 51-quater O.P.)

## Conversione/Rateizzazione Pena Pecuniaria Sostitutiva
Gli artt. 102, 103 legge 689/1981 prevedono  che la pena pecuniaria non pagata possa essere convertita non

più nella libertà controllata, bensì nella semilibertà e nella detenzione domiciliare sostitutive,

oltre che nel lavoro di pubblica utilità.

Non è possibile inserire i nuovi oggetti nell’attuale contenuto Conversione Pena Pecuniaria, in quanto per questi procedimenti è obbligatorio l’inserimento della Richiesta Conversione Pena Pecuniaria, con l’indicazione di tutti gli estremi (Anno/Numero Partiva IVA, Campione Penale, Autorità Richiedente, data irrevocabilità Titolo Esecutivo, etc.). Questi dati non sono necessari per la gestione dei procedimenti con Pena Pecuniaria sostitutiva.
In realtà nell’attuale gestione, per procedere è sufficiente inserire solo il quantum di pena da convertire; di conseguenza credo si possa utilizzare quanto già esistente.

Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Conversione / Rateizzazione pena pecuniaria sostitutiva (artt. 102, 103 legge 689/1981 )
Al nuovo contenuto vanno associati i seguente oggetti:


Conversione pena pecuniaria
Rateizzazione  pena pecuniaria
e i seguenti esiti N.B. Mantenere l’ordine sottostante
Dispone conversione in semilibertà sostitutiva
Dispone conversione in detenzione domiciliare sostitutiva
Dispone conversione in lavoro di pubblica utilità sostitutivo
Dispone conversione pena irrogata dal GdP in lavoro di pubblica utilità
Dispone conversione in libertà controllata
Dispone conversione in lavoro sostitutivo
Rateizza  pagamento     (da confermare) SI
Rigetta
Differisce la conversione
Dichiara NLP per irreperibilità – atti al PM
Dichiara NLP per accertata solvibilità
Dichiara NLP per intervenuta prescrizione
Dichiara estinta la pena per avvenuto pagamento
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

Questo tipo di procedimento non presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva/Esecuzione Misura Alternativa, pertanto l’iscrizione, fuoriuscendo dalla logica procedimenti “padre” – “figli”, avverrà utilizzando le attuali funzionalità di iscrizione previste in SIUS.

Per questo tipo di procedimento si può ipotizzare un ordinanza del tipo seguente

N.B. Eliminare la dicitura “sostitutiva” nell’oggetto
L’Amministrazione fornirà i modelli di stampa necessari.




## Conversione pene pecuniarie irrogate dal Giudice di Pace
L’art.  55 D.L. 274/2000 prevede che a richiesta del condannato la pena pecuniaria può essere convertita in lavoro di pubblica utilità, In  caso di violazione  degli  obblighi  del  lavoro  di  pubblica  utilità,  la  parte           residua si converte in obbligo di permanenza domiciliare. Occorre, quindi, inserire un nuovo contenuto “figlio” specifico nel contenuto EPS (ESS e non EPS).
A monte deve essere inserito anche il relativo oggetto nel contenuto “Esecuzione Sanzioni sostitutive”, che possiamo denominare “Lavoro di pubblica utilità”

Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:

Violazione obblighi lavoro pubblica utilità (art. 55 c. 3 DL 274/2000)
Al nuovo contenuto vanno associati il seguente oggetto:

Violazione obblighi lavoro pubblica utilità (art. 55 c. 3 DL 274/2000)
e i seguenti esiti

Converte pena pecuniaria in permanenza domiciliare
Non converte
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Sanzione Sostitutiva, pertanto l’iscrizione sarà uguale a quella di tutti gli altri procedimenti  figli dell’Esecuzione Sanzione Sostitutiva.

Per questo tipo di procedimento si può ipotizzare una ordinanza simile a quella proposta al precedente paragrafo.
Non è chiaro cosa avviene nella gestione del procedimento di ESS.
La conversione di cui sopra determina come effetto diretto quello di imporre la creazione di un nuovo oggetto all’interno del contenuto ESS, che potremmo denominare “Permanenza domiciliare”

## Gestione Procedimenti Esecuzione Pene Sostitutive
Come già previsto in SIUS per i procedimenti di Esecuzione Misure Alternative, Esecuzione Sanzioni Sostitutive e Esecuzione Misure di Sicurezza, per la gestione dei procedimenti di Esecuzione Pene Sostitutive sarà aggiunta nel menu verticale dell’UDS la nuova voce


Che presenterà a sua volta il menu orizzontale



Da cui sarà possibile

ricercare i procedimenti “padri” di Esecuzione Pene Sostitutive per Anno e Numero o per Intervalli di numeri



ricercare i procedimenti “padri” di Esecuzione Pene Sostitutive a carico di un Soggetto



Le due funzionalità seguiranno lo stesso flusso operativo presente in SIUS per gli altri procedimenti di Esecuzione.

## Gestione Licenze – Pene Sostitutive
Per estendere l’attuale gestione delle Licenze per semilibertà e per internati anche alle Licenze – pene sostitutive saranno adeguate tutte le funzionalità, riferite a Licenza, presenti nella voce di menu verticale , cioè


Ricerca Licenze per Soggetto
Nell’attuale form



Nella combo box Visualizza solo i provvedimenti relativi a, alle attuali voci “Licenze” e “Licenze per Internati” sarà aggiunta la nuova voce “Licenze – pene sostitutive”. Tutto il codice sarà aggiornato per gestire le nuove tipologie di Licenza.

Esecuzione Licenza
Le attuali funzioni attivabili dalla sottostante form


saranno aggiornate per poter  essere utilizzate anche per le Licenze – pene sostitutive.

Relazione Trimestrale
L’attuale form sarà modificata



Con l’aggiunta di un nuovo radio button per poter utilizzare la funzione anche per la nuova Licenza con conseguente aggiornamento del codice.