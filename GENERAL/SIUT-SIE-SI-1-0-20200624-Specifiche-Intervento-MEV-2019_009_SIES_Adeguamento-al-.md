---
uniqueName: siut-sie-si-1-0-20200624-specifiche-intervento-mev
displayName: "SIUT SIE SI 1 0 20200624 Specifiche Intervento MEV 2019 009 SIES Adeguamento al "
category: "GENERAL"
tags: []
---

# SIUT-SIE-SI-1.0-20200624 Specifiche Intervento MEV 2019_009_SIES_Adeguamento al Dlgs 123_2018 e 121_2018(Dlgs 123_2018 - FASE 1)

> **File originale:** `MEV/SCHEDA_009/specifiche_intervento/SIUT-SIE-SI-1.0-20200624 Specifiche Intervento MEV 2019_009_SIES_Adeguamento al Dlgs 123_2018 e 121_2018(Dlgs 123_2018 - FASE 1).docx`  
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
| Elaborato da | Engineering |
| Verificato da | Vito Bufi |
| Approvato da | Paolo Ceccanti |
| Data approvazione | 24/06/2020 |
| Livello di riservatezza | L3 |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 24/06/2020 |  | Prima Emissione |


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
| Andrea Castorino
Alessandro Lanari | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |
| Luigi Buglione | RTI |  | Referente Metrico |


INDICE DEI CONTENUTI

1	Introduzione	7
1.1	Scopo del documento	7
1.2	Riferimenti	7
1.3	Glossario	8
1.3.1	Definizioni	8
1.3.2	Acronimi e abbreviazioni	8
2	Definizione dell’Obiettivo	10
2.1	Convenzioni	11
2.2	Elenco Requisiti	12
2.2.1	REQ-SIE-009-01 (SIUS)	12
2.2.2	REQ-SIE-009-02 (SIUS)	12
2.2.3	REQ-SIE-009-03 (SIUS)	13
2.2.4	REQ-SIE-009-04 (SIUS)	13
2.2.5	REQ-SIE-009-05 (SIUS)	13
2.2.6	REQ-SIE-009-06 (SIUS)	13
2.2.7	REQ-SIE-009-07 (SIUS)	13
2.2.8	REQ-SIE-009-08 (SIUS)	13
2.2.9	REQ-SIE-009-09 (SIUS)	14
2.2.10	REQ-SIE-009-10 (SIUS)	14
2.2.11	REQ-SIE-009-11 (SIUS)	14
2.2.12	REQ-SIE-009-12(SIEP)	14
2.2.13	REQ-SIE-009-13 (SIEP)	14
2.2.14	REQ-SIE-009-14(SIEP)	14
2.2.15	REQ-SIE-009-15(SIEP)	15
3	Descrizione dell’Intervento	16
3.1	Ambito Normativo	16
3.1.1	D.lgs. 123/2018	16
3.2	Adeguamento D.lgs. 123/2018 – Sottosistema SIUS	16
3.2.1	REQ-SIE-009-01 TDS/TDSM - Concessione misure alternative (art. 678 comma 1-ter c.p.p.)	16
3.2.2	REQ-SIE-009-02 TDS/TDSM - Emissione del Decreto Presidenziale di Designazione	21
3.2.3	REQ-SIE-009-03 TDS/TDSM - Emissione Ordinanza Applicazione Provvisoria	25
3.2.4	REQ-SIE-009-04 TDS/TDSM - Registrazione data Esecutività Ordinanza Applicazione Provvisoria	28
3.2.5	REQ-SIE-009-05 TDS/TDSM - Provvedimento di Conferma Ordinanza Applicazione Provvisoria	31
3.2.6	REQ-SIE-009-06 - REQ-SIE-009-07 (Statistiche Misura Alternativa - art. 678 comma 1-ter c.p.p.) )	33
3.2.7	REQ-SIE-009-08 TDS/TDSM (Aggiornamento Statistica Movimento Provvedimenti per Oggetti)	38
3.2.8	REQ-SIE-009-09 TDS/TDSM Modifica pagina richiesta atti istruttori	39
3.2.9	REQ-SIE-009-10 TDS/TDSM Statistica Atti Istruttori con Data Richiesta Restituzione	42
3.2.10	REQ-SIE-009-11 (UDS/UDSM – TDS/TDSM Integrazione Lista Mittenti)	44
3.3	Adeguamento D.lgs. 123/2018 – Sottosistema SIEP	45
3.3.1	REQ-SIE-009-12 SIEP - ‘Ammissione Provvisoria misure alternative (art. 678 comma 1-ter c.p.p.) ’	48
3.3.2	REQ-SIE-009-13 SIEP – ‘Conferma dell’Ammissione Provvisoria misure alternative (art. 678 comma 1-ter c.p.p.) ’ e    REQ-SIE-009-14 SIEP -  ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’	61
3.3.3	REQ-SIE-009-16 SIEP - Aggiornamento della funzione di riepilogo ispettivo e Statistiche lavoro magistrati	74
3.4	Gestione dei Template – Sottosistema SIUS e SIEP	76
3.5	Moduli sw	78
3.6	Architettura	79
3.7	Interfacce utente	79
3.8	Basi dati	79
3.8.1	Base Dati - REQ-SIE-009-01 (TDS/TDSM - Concessione misure alternative (art. 678 comma 1-ter c.p.p.))	79
3.8.2	Base Dati - REQ-SIE-009-02 (TDS/TDSM - Emissione del Decreto Presidenziale di Designazione)	79
3.8.3	Base Dati - REQ-SIE-009-03 (TDS/TDSM - Emissione Ordinanza Applicazione Provvisoria)	80
3.8.4	Base Dati - REQ-SIE-009-04 (TDS/TDSM - Registrazione data Esecutività Ordinanza Applicazione Provvisoria)	81
3.8.5	Base Dati - REQ-SIE-009-05 (TDS/TDSM - Provvedimento di Conferma Ordinanza Applicazione Provvisoria)	81
3.8.6	Base Dati - REQ-SIE-009- 06 (TDS/TDSM - Statistica Ordinanze Non Emesse (Trasmessi Atti al Presidente))	82
3.8.7	Base Dati - REQ-SIE-009- 07 (TDS/TDSM - Statistica Ordinanze Provvisorie Esecutive senza decisione del Collegio)	82
3.8.8	Base Dati - REQ-SIE-009- 08 (Aggiornamento Statistica Movimento Provvedimenti per Oggetti)	82
3.8.9	Base Dai - REQ-SIE-009- 09 (Modifica pagina Richiesta Atti Istruttori)	82
3.8.10	Base Dati - REQ-SIE-009- 10 (Statistica Atti Istruttori con Data Restituzione)	82
3.8.11	Base Dati - REQ-SIE-009-11 (UDS – TDS Integrazione Lista Mittente Atto)	82
3.8.12	Base Dati - REQ-SIE-009-12 SIEP - ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’	83
3.8.13	Base Dati - REQ-SIE-009-13 SIEP - ‘Ammissione Provvisoria misure alternative (art. 678 comma 1-ter c.p.p.) ’	83
3.8.14	Base Dati - REQ-SIE-009-14 SIEP – ‘Conferma Ammissione Provvisoria misure alternative (art. 678 comma 1-ter c.p.p.) ’	83
3.8.15	Base Dati - REQ-SIE-009-15 SIEP - Aggiornamento della funzione di riepilogo ispettivo e Statistiche lavoro magistrati	83
3.9	WEB services	83
3.10	XSD	83
3.11	Configurazione	84
3.12	Tutorial	84
4	Piano delle attività	85
4.1	Ciclo di sviluppo	85
4.2	Piano delle attività	88
4.3	Gantt	89
4.4	Vincoli	89
4.5	Luogo di lavoro	89
5	Dimensionamento	90
5.1	Stima dell'effort previsto	90
5.2	Dettaglio costi	90

# Introduzione
## Scopo del documento
Il presente documento riporta le specifiche di intervento sul software del sistema SIES, con metodologia WATERFALL, al fine di soddisfare i requisiti espressi dall’Amministrazione in relazione alla richiesta di adeguamento normativo del Sistema, nella sua interezza, al D.lgs. 123/2018 e al D.lgs. 121/2018.

L’intervento in oggetto rientra nel servizio di Manutenzione Evolutiva, è stato richiesto con comunicazione m_dg.DOG07AR.08082019.0000017.U ed è classificato come di seguito riportato:

| Scheda di Intervento | 2019_09 |
| --- | --- |
| Oggetto | Adeguamento normativo SIES al D.lgs. 123/18 e 121/18 |
| Complessità | Alta |
| Servizio | MEV |


Nell’ottica di snellire le attività di redazione dei documenti e di verifica degli interventi da parte dell’Amministrazione, e di concerto con la stessa, tale documento espone gli interventi attinenti ad un sottoinsieme delle funzioni da prevedere nel sistema in base alle novità normative del decreto D.lgs.123/18 (maggiorenni e minorenni).
Con lo scopo di rendere l’intervento coerente ed auto consistente gli interventi saranno relativi ai sottosistemi SIEP e SIUS.

## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF1 | m_dg.DOG07AR.08082019.0000017.U_Nota_ Scheda_n.9.docx.pdf | Richiesta Scheda di Intervento |
| RIF2 | m_dg.DOG07AR.25_10_2019.0000096.U_Richiesta Riemissione _ Nota_Schedanr9SIES.docx_signed.pdf | Nota per Riemissione della Scheda di Intervento |
| RIF3 | SIES-SIUS-ModificheDecretoLegislativon.123.doc | Documento dei requisiti fornito dal GdL SIES allegato alla Richiesta Scheda di Intervento |
| RIF4 | SIES-SIEP-ModificheDecretoLegislativon.123.doc | Documento dei requisiti fornito dal GdL SIES allegato alla Richiesta Scheda di Intervento |
| RIF5 | SIUT-SIES-VR-1.1-20200608 Flussi Decreto 121_123_2018.pdf | Documento dei flussi SIEP –SIUS per D.lgs. 123/2018 e 121/2018 |



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
In caso di emissione dell’ordinanza di concessione di misure alternative, decorso il termine per l’opposizione, il Tribunale si riunisce in camera di consiglio e senza formalità (da intendersi senza la presenza delle parti e presumibilmente con decreto) procede alla conferma del provvedimento provvisorio.
Se il Tribunale decide di non confermare l’ordinanza del magistrato, non emette alcun provvedimento motivato ma fissa l’udienza affinché si proceda con il rito ordinario.

Altre modifiche di rilievo attengono al potere del Tribunale di Sorveglianza, nell’ambito del procedimento di revoca delle misure alternative, di decidere anche in ordine all’eventuale sostituzione della misura con un’altra di diversa natura (art. 51 ter novellato) o il potere dello stesso magistrato di sorveglianza di eseguire (e non solo adottare) il provvedimento di cessazione della misura alternativa divenuta non più ammissibile, con il conseguente accompagnamento in Istituto penitenziario direttamente disposto dal Giudice (art. 51 bis novellato).

Per le pene accessorie (secondo il nuovo articolo 51 quater) è prevista, inoltre, che la loro esecuzione possa esserci anche in pendenza di una misura alternativa e non solo all’esito della stessa, salvo che il giudice di sorveglianza né disponga la sospensione per prevalenti esigenze di reinserimento. In caso di revoca della misura il Tribunale dovrà poi decidere anche sulle pene accessorie, se in corso di esecuzione, ed eventualmente computarne il periodo già espiato.

A seguire si riportano le descrizioni di questa prima fase di intervento inerenti all’adeguamento del sistema SIES limitatamente al D.lgs. 123/18 e alle seguenti macro funzionalità:
Gestione della concessione delle misure alternative alla detenzione relativa dell’introduzione dell’art. 678 c1 ter (per SIUS e per SIEP);
Gestione del decreto di designazione del magistrato (SIUS);
Gestione dell’Ammissione Provvisoria (art. 678 c1 ter) e della sua esecutività (per SIUS e per SIEP);
Gestione della Conferma dell’Ammissione Provvisoria (per SIUS e per SIEP);
Introduzione di nuove funzioni di Estrazione Dati relative alle novità dell’art. 678 c1 ter (SIUS);
Allineamento della Statistica Movimento Provvedimenti Per Oggetti (SIUS);
Integrazione sulle funzioni di Richiesta Atti Istruttori e gestione lista mittenti con “Gruppo Di Osservazione E Trattamento (SIUS);
Allineamento della funzione di Riepilogo Ispettivo in relazione all’Ammissione Provvisoria e all’ordinanza/decreto di Conferma (SIEP);

## Convenzioni
Sulla base degli ambiti di progetto e dei tipi di requisito, la convenzione per l’identificazione dei requisiti è riportata di seguito.
Ciascun requisito è individuato da un identificativo univoco nella forma [REQ-SIS-nnn-mm], dove:
REQ Requisito;
SIS identifica il sistema (cfr. SIUT-GEN-SN-2.2-20191023-Standard di nomenclatura);
nnn è il numero della scheda di richiesta intervento;
mm è il numero progressivo del requisito espresso dall’Amministrazione.

## Elenco Requisiti
Gli interventi di questo obiettivo possono riassumersi nei requisiti funzionali di seguito descritti, ed attengono a quanto richiesto nel documento “m_dg.DOG07AR.08082019.0000017.U_Nota_ Scheda_n.9.docx.pdf” [RIF1] e fanno riferimento al D.lgs. 2018/123 descritto nella definizione dell’obiettivo.

I requisiti elencati si riferiscono ad interventi da realizzare nell’ambito dei sottosistemi SIUS (Maggiorenni e Minorenni) e SIEP (Maggiorenni e Minorenni) limitatamente alla macro funzioni specificate al paragrafo precedente.
Restano esclusi, in questa prima fase di analisi, e quindi di realizzazione, i requisiti per d.lgs. 123/2018 che afferiscono alla:
Gestione della ‘Revoca dell’Ammissione Provvisoria - art. 678 comma 1-ter c.p.p.’ e relativa funzione di Estrazione Dati;
Sostituzione di una misura alternativa (art. 51 ter O.P.);
Sospensione delle pene accessorie (art. 51 quater O.P.);
Atri interventi SIUS (integrazione Lavoro Pubblica Utilità, Rettifica del Lavoro Esterno);
## REQ-SIE-009-01 (SIUS)
In relazione all’articolo 678 c.p.p. comma 1 ter, introdotto con D.lgs. 123/2018, gli uffici Tribunali di Sorveglianza (TDS/TDSM) devono essere abilitati all’emissione di un’ordinanza di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’.
## REQ-SIE-009-02 (SIUS)
In relazione all’articolo 678 c.p.p. comma 1 ter, il Presidente del Tribunale di Sorveglianza (TDS/TDSM), in tema di semplificazione della procedura, designa, dopo aver acquisito i documenti e le necessarie informazioni, il magistrato relatore per l’emissione un’ordinanza di ammissione provvisoria per una misura alternativa di all'articolo 656, comma 5.
## REQ-SIE-009-03 (SIUS)
Nell’ambito degli uffici Tribunali di Sorveglianza (TDS/TDSM), in relazione all’articolo 678 c.p.p. comma 1 ter, il magistrato designato può emettere un’ordinanza di ammissione provvisoria ad una misura alternativa, di cui all’articolo 656, comma 5.
## REQ-SIE-009-04 (SIUS)
Caratterista fondamentale dell’ordinanza di ammissione provvisoria è la sua non immediata esecutività.
Con il requisito in oggetto il sistema deve prevedere una nuova funzione, nell’ambito degli uffici Tribunali di Sorveglianza (TDS/TDSM), che permetta al magistrato designato di poter inserire la data a partire dalla quale l’ordinanza di ammissione provvisoria della misura diverrà esecutiva.
## REQ-SIE-009-05 (SIUS)
Emissione del provvedimento di Conferma (ratifica) dell’Applicazione Provvisoria della misura da parte del Tribunale di Sorveglianza (TDS/TDSM). Il sistema deve permettere di inserire il provvedimento di conferma sia come Ordinanza che come Decreto.
## REQ-SIE-009-06 (SIUS)
Nell’ambito degli uffici Tribunali di Sorveglianza (TDS/TDSM), prevedere una funzione di estrazione dati per il recupero dei procedimenti SIUS con contenuto ‘Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) ’ per i quali il magistrato designato ha proceduto alla ‘non emissione’ dell’ordinanza trasmettendo gli atti al Presidente.
## REQ-SIE-009-07 (SIUS)
Nell’ambito degli uffici Tribunali di Sorveglianza (TDS/TDSM), prevedere una funzione di estrazione dati per il recupero dei procedimenti SIUS con contenuto ‘Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) ’ con data di esecutorietà inserita, ma privi di decisione da parte del Collegio.
## REQ-SIE-009-08 (SIUS)
Intervenire sull’aggiornamento della funzione STATISTICHE – MOVIMENTO PROVVEDIMENTI PER OGGETTI in modo da integrare anche questa nuova tipologia di ordinanza provvisoria.
## REQ-SIE-009-09 (SIUS)
Intervenire sulle pagine di richiesta di atti istruttori al fine di indicare la data entro cui l’atto deve essere restituito all’ufficio di Sorveglianza che ne ha fatto richiesta.
## REQ-SIE-009-10 (SIUS)
Prevedere una nuova funzione di Ricerca nel menù Statistiche/Monitoraggio che conteggi ed estrapoli la lista dei procedimenti per i quali, in fase di richiesta di un atto istruttorio, sia stata indicata una determinata data di scadenza entro il quale far pervenire l’atto richiesto.
## REQ-SIE-009-11 (SIUS)
Stante quanto prescritto dall’art. 57 O.P., nella maschera di iscrizione di un procedimento SIUS, nella combo box dei mittenti, occorre aggiungere la voce “gruppo di osservazione e trattamento”.
## REQ-SIE-009-12(SIEP)
In relazione ai requisiti REQ-SIE-009-03 e REQ-SIE-009-04 che prevedono l’implementazione di un’ordinanza di ammissione provvisoria secondo quanto previsto all’articolo 678 c.p.p. comma 1 ter, gli uffici PM (Procura della Repubblica Presso il Tribunale Ordinario) e PMM (Procura della Repubblica Presso il Tribunale per i Minorenni) devono poter gestire l’esecuzione dell’ammissione provvisoria della misura alternativa art. 678 c.p.p. comma 1 ter.
## REQ-SIE-009-13 (SIEP)
In relazione ai requisiti REQ-SIE-009-05 che prevedono l’implementazione della Conferma di un’ordinanza di ammissione provvisoria, gli uffici PM (Procura della Repubblica Presso il Tribunale Ordinario) e PMM (Procura della Repubblica Presso il Tribunale per i Minorenni) devono poter gestire la Conferma (Ratifica) dell’ammissione provvisoria della misura alternativa art. 678 c.p.p. comma 1 ter.
## REQ-SIE-009-14(SIEP)
Nell’ambito degli uffici PM (Procura della Repubblica Presso il Tribunale Ordinario) e PMM (Procura della Repubblica Presso il Tribunale per i Minorenni) integrare la gestione dell’ordinanza di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ per rito ordinario.
## REQ-SIE-009-15(SIEP)
Aggiornamento della funzione di riepilogo ispettivo e statistiche lavoro magistrati, in modo da integrare la nuova tipologia di ordinanza di ammissione provvisoria (art. 678 c.p.p. comma 1 ter) e l’ordinanza/decreto di ratifica dell’ammissione provvisoria. Allineare anche lo stato di esecuzione.



# Descrizione dell’Intervento
## Ambito Normativo
### D.lgs. 123/2018
In relazione al Capo II: DISPOSIZIONI PER LA SEMPLIFICAZIONE DEI PROCEDIMENTI, Art. 4: Modifiche al codice di procedura penale in tema di semplificazione, all'articolo 678, viene inserito il comma 1-ter che recita quanto segue:

«1-ter. Quando la pena da espiare non è superiore a un anno e sei mesi, per la decisione sulle istanze di cui all'articolo 656, comma 5, il presidente del tribunale di sorveglianza, acquisiti i documenti e le necessarie informazioni, designa il magistrato relatore e fissa un termine entro il quale questi, con ordinanza adottata senza formalità, può applicare in via provvisoria una delle misure menzionate nell'articolo 656, comma 5. L'ordinanza di applicazione provvisoria della misura è comunicata al pubblico ministero e notificata all'interessato e al difensore, i quali possono proporre opposizione al tribunale di sorveglianza entro il termine di dieci giorni. Il tribunale di sorveglianza, decorso il termine per l'opposizione, conferma senza formalità la decisione del magistrato.
Quando non è stata emessa o confermata l'ordinanza provvisoria, o è stata proposta opposizione, il tribunale di sorveglianza procede a norma del comma 1. Durante il termine per l'opposizione e fino alla decisione sulla stessa, l'esecuzione dell'ordinanza è sospesa.»;

## Adeguamento D.lgs. 123/2018 – Sottosistema SIUS
In riferimento all’’introduzione del comma 1 ter all’articolo 678 c.p.p., l’ufficio Tribunale di Sorveglianza (ufficio TDS) e l’ufficio Tribunale di Sorveglianza dei Minorenni (TDSM), hanno la possibilità di concedere misure alternative, ex art. 656 commi 5 e 6 c.p.p. per procedimenti relativi a condanne per pene fino a 18 mesi.
Nasce, pertanto, l’esigenza di dover gestire un nuovo contenuto in fase di iscrizione di un procedimento SIUS.
### REQ-SIE-009-01 TDS/TDSM - Concessione misure alternative (art. 678 comma 1-ter c.p.p.)
Il contenuto da prevedere nell’ambito dell’ufficio Tribunale di Sorveglianza (ufficio TDS) e dell’ufficio Tribunale di Sorveglianza dei Minorenni (TDSM) è il seguente:

Concessione misure alternative (art. 678 comma 1-ter c.p.p.)

al quale vanno associati i seguenti oggetti:
Affidamento in prova al servizio sociale (art. 47 O.P. -  art. 678 comma 1-ter c.p.p.);
Affidamento in prova al servizio sociale (art. 94 DPR 309/90 - art. 678 comma 1-ter c.p.p.);
Detenzione domiciliare (art. 47 ter O.P. - art. 678 comma 1-ter c.p.p.);
Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.);
Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.);

In corrispondenza della voce “Detenzione domiciliare (art. 47 ter O.P. - art. 678 comma 1-ter c.p.p.)”, occorre prevedere un sotto elenco con le seguenti descrizioni:

Detenzione Domiciliare Donna Incinta o Madre di Prole di Età Inferiore Ad Anni Dieci con Lei Convivente;
Detenzione Domiciliare Padre, Esercente la Potestà, di Prole di Età Inferiore Ad Anni Dieci con Lui Convivente;
Detenzione Domiciliare Persona in Condizioni di Salute Particolarmente Gravi, Che Richiedano Costanti Contatti con i presidi sanitari territoriali;
Detenzione Domiciliare Persona di Età Superiore a Sessanta Anni Se Inabile Anche Parzialmente
Detenzione Domiciliare Persona Minore di Anni Ventuno per Comprovate Esigenze di Salute, di Studio, di Lavoro e di Famiglia;
Detenzione domiciliare (art. 47 ter comma 1 bis O.P. - art. 678 comma 1-ter c.p.p.);
Detenzione domiciliare per ultrasettantenni (art. 47 ter comma 01 O.P. - art. 678 comma 1-ter c.p.p.);

Ciò si traduce nella possibilità di poter scegliere un nuovo contenuto nella pagina di iscrizione di un procedimento SIUS, così come mostrato nella figura che segue:


Figura 1: Pagina iscrizione procedimento SIUS per Concessione misure alternative (art. 678 comma 1-ter c.p.p.)

Parallelamente, in fase di associazione degli oggetti, tramite il pulsante ,  il sistema deve poter permettere di associare le voci su elencate, così come prospettate nella figura che segue:

Figura 2: Elenco oggetti per contenuto Concessione Misure Alternative (art. 678 comma 1-ter c.p.p.)
A seguito dell’iscrizione del procedimento SIUS con il nuovo contenuto “Concessione misure alternative (art. 678 comma 1-ter c.p.p.)”, l’utente procede con l’emissione dell’ordinanza.

In base alla ‘novità’ prevista da d.lgs. 123/2018, ossia l’introduzione di una fase provvisoria, in corrispondenza del contenuto “Concessione misure alternative (art. 678 comma 1-ter c.p.p.)”, si può avere una doppia diramazione per quanto concerne la fase di emissione dell’ordinanza.
Infatti, si può dare ‘inizio’ ad una fase provvisoria che prevede quanto esposto al par. 3.2.2 (Emissione del Decreto Presidenziale di Designazione) ed al par 3.2.3 (Emissione Ordinanza Applicazione Provvisoria) , oppure ad una fase ‘ordinaria’ (con rito dibattimentale), che può incorre nelle casistiche in cui non si dia ‘inizio’ alla fase provvisoria, o nei casi in cui la ‘fase provvisoria’ si concluda con una ‘non conferma’ dell’ordinanza provvisoria emessa dal magistrato designato. Si confluirà nella casistica di ‘rito ordinario’ anche nel caso in cui venga presentata opposizione.

Pertanto, per la casistica di ‘rito ordinario’, la pagina di emissione dell’ordinanza sarà uguale alla maschera attualmente utilizzata per il contenuto ‘Concessione Misure Alternative Alla Detenzione’ (C001):


Figura 3: Emissione Ordinanza di Misura Alternativa (art. 678 comma 1-ter c.p.p.)

E gli esiti previsti per lo scarico dell’ordinanza saranno:
Concede
Rigetta
Dichiara L’inammissibilità
Dichiara N.D.P./ N.L.P.
Dichiara La Propria Incompetenza

In fase di stampa dell’ordinanza, saranno agganciati i templati ad oggi già presenti a sistema per le ordinanze di ‘Affidamento in Prova’, ‘Semilibertà, ‘Detenzione Domiciliare e ‘Sospensione Pena’;
Il flusso di lavorazione del procedimento SIUS che abbia il nuovo contenuto ‘Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) ’, per rito ordinario, seguirà quello attualmente in essere per il contenuto ‘Concessione Misure Alternative Alla Detenzione’ (C001) con la gestione della modifica, visualizzazione, cancellazione, stampa, validazione e trasmissione.
Dal punto di vista tecnico-implementativo, per la casistica in esame, le funzioni di modifica, visualizzazione(dettaglio), cancellazione, stampa, e validazione non subiranno interventi, mentre per ciò che attiene la funzione di trasmissione, occorre prevedere l’aggiunta di nuove informazioni sull’xml di scambio. L’aggiunta di ulteriori dati può intervenire nei casi in cui, dopo una prima fase provvisoria, si possa passare a rito ordinario, ad esempio in caso di opposizione oppure in caso di mancata emissione de plano dell’ordinanza nel termine assegnato al magistrato relatore.

La funzione di trasmissione è fondamentale per implementare correttamente lo scambio di informazioni con SIEP e permettere, pertanto, lato Procura, la gestione delle nuova ordinanza di ‘Concessione di Misura Alternativa (art. 678 comma 1-ter c.p.p.) ’. Si evidenzia che questo è uno dei punti di impatto di ‘interconnessione’ del sistema SIUS con il sotto sistema SIEP. Per i dettagli relativi alla gestione dell’ordinanza, lato SIEP, si rimanda al par. 3.3.2.

### REQ-SIE-009-02 TDS/TDSM - Emissione del Decreto Presidenziale di Designazione
Sempre in riferimento al comma 1 ter all’articolo 678 c.p.p., per procedimenti relativi a condanne per pene fino a 18 mesi, l’ufficio Tribunale di Sorveglianza (TDS/TDSM), in tema di semplificazione della procedura, designa il magistrato relatore e fissa un termine entro il quale questi, con ordinanza adottata senza formalità, può applicare in via provvisoria una delle misure menzionate nell'articolo 656, comma 5.

L’adeguamento del sistema SIUS a tale normativa si delinea nell’implementazione che si espone a seguire.

Accedendo al sistema SIUS con utenza Tribunale di Sorveglianza (TDS/TDSM), in corrispondenza del menù ‘Decreti’, sarà introdotto un nuovo tasto funzione denominato ‘Decreto Presidenziale di Designazione’.


Figura 4: Menù Decreto Presidenziale di Designazione

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


Figura 5: Pagina di inserimento del Decreto Designazione Magistrato

Caratteristica fondamentare di tale decreto è che a seguito dell’inserimento e validazione dello stesso, il procedimento in lavorazione non deve essere chiuso.
Per tale decreto deve essere creato un documento di stampa ad hoc che sarà fornito dall’Amministrazione.

Lo stato del procedimento, a seguito della validazione del Decreto di Designazione, sarà impostato a ‘Emesso Decreto Designazione’, mentre l’esito da associare al decreto è ‘Magistrato Designato art. 678 1-ter’. L’introduzione di un nuovo stato procedimento e nuovo esito si giustifica per la corretta individuazione dei procedimenti SIUS ai fini delle elaborazioni statistiche dettagliate ai par.3.2.6.1 e 3.2.6.2.

Nel momento in cui, tramite il Decreto di designazione, viene individuato il Magistrato, il sistema deve aggiornare in automatico il magistrato assegnatario presente nella maschera di dettaglio del procedimento SIUS.  Qualora il magistrato assegnatario del procedimento fosse già stato assegnato precedentemente all’emissione del decreto, e dovesse differire dal magistrato designato con il decreto, il sistema, nella pagina di dettaglio del procedimento SIUS, deve visualizzare un messaggio che avverta della discrepanza tra i due magistrati.


Figura 6: Messaggio Incongruenza Magistrato

A questo punto la cancelleria deve provvedere con la rettifica del magistrato assegnatario. In caso di mancata rettifica, il procedimento non può essere lavorato nelle eventuali fasi successive.

Il magistrato, ricevuta la designazione, se ritiene di poter concedere una delle misure alternative previste dall’art. 656 comma 5 c.p.p., e non necessariamente quella richiesta dal condannato, emette de plano un’ordinanza di applicazione provvisoria.

La gestione dell’ordinanza di applicazione provvisoria sarà descritta nel paragrafo successivo.
### REQ-SIE-009-03 TDS/TDSM - Emissione Ordinanza Applicazione Provvisoria
Accedendo al sistema SIUS con utenza Tribunale di Sorveglianza (TDS/TDSM), in corrispondenza del menù ‘Ordinanze’, sarà introdotto un nuovo tasto funzione denominato ‘Applicazione Provvisoria M.A’.


Figura 7: Menù Emissione Ordinanza Provvisoria

L’accesso alla funzione mostrerà una nuova maschera per inserire un’ordinanza di Applicazione Provvisoria di Misura Alternativa. La tipologia di ordinanza che viene emessa deve essere di tipo ‘ordinanza provvisoria’ e l’emissione di tale ordinanza non deve richiedere la fase di ‘Fissazione’ o ‘Prefissazione’ udienza. Deve essere gestita, quindi, come rito monocratico.
Dal punto di vista funzionale, l’emissione di un’ordinanza di Applicazione Provvisoria M.A. si inserisce a valle dell’inserimento del Decreto Presidenziale di Designazione.
Affinché possa essere emessa un’ordinanza di Applicazione Provvisoria M.A., infatti, il sistema deve controllare che, per il procedimento SIUS in lavorazione, sia stato emesso il Decreto di Designazione del magistrato relatore.
Nella casistica in cui, entro i termini previsti, non si stato emesso il Decreto di Designazione, per dare seguito all’applicazione della misura, si procede con l’emissione dell’ordinanza (rito ordinario) cosi come esplicitato al par. 3.2.1, rientrando quindi nel classico giro del rito dibattimentale, quindi con la fissazione udienza e con l’emissione dell’ordinanza che applica o meno la misura.

La maschera per l’inserimento dell’ordinanza provvisoria, similmente all’emissione di un ordinanza generica deve permettere di poter inserire le seguenti informazioni:
Data Emissione
Contenuto
Oggetto


Figura 8: Emissione Ordinanza Applicazione Provvisoria M.A.

mentre, nella pagina di inserimento degli esiti, ossia sulla pagina che il sistema mostra a seguito della ‘Conferma’, oltre alla combo box contenente gli esiti, devono essere previste, in aggiunta, le seguenti informazioni:
Un campo ‘check box’ con accanto la dicitura “ordinanza non emessa – restituzione atti al Presidente”.
Campo note (per eventuali motivazioni della restituzione degli atti).


Figura 9: Pagina esiti Ordinanza Provvisoria

Gli esiti da prevedere sono quelli consueti, vale a dire “Concede”, “Rigetta”, “NLP”, “Inammissibilità” e “Incompetenza” ed in aggiunta quello denominato “Applica Provvisoriamente”.

Nel caso in cui, dunque, il magistrato relatore ritenga di non poter applicare alcuna delle misure concedibili, egli dovrà limitarsi a rimettere gli atti al Presidente del Tribunale di Sorveglianza, il quale provvederà secondo il tradizionale procedimento ex articolo 678, comma 1 del codice di procedura penale, predisponendo il contraddittorio. Il rigetto dell’istanza è sempre subordinato, pertanto, ad una valutazione di tipo collegiale.

L’introduzione e l’utilizzo del ‘check box’ su indicato determinano, pertanto, la ‘NON EMISSIONE’ dell’ordinanza provvisoria, entro il termine assegnato, e la restituzione degli atti al presidente del Tribunale di Sorveglianza. A questo punto lo stato del procedimento SIUS deve essere impostato a ‘Trasmessi Atti al Presidente’.
La ‘Non Emissione’ dell’ordinanza determina comunque la chiusura della fase provvisoria in maniera alternativa rispetto alla ordinaria indicazione degli esiti. La procedura a questo punto segue il suo corso normale con l’apertura del dibattito. Quindi il TDS/TDSM fissa udienza ed emette ordinanza.
Caratteristica fondamentale dell’ordinanza del magistrato designato di Applicazione Provvisoria di Misura Alternativa, è la sua non immediata esecutività. Ciò significa che a seguito di esito ‘Applica Provvisoriamente’, per l’ordinanza in lavorazione, deve essere inibita la fase di validazione, deposito e trasmissione della stessa verso la Procura. Deve essere possibile, invece, effettuare la stampa dell’ordinanza provvisoria, prevedendo un nuovo template.
L’ordinanza, diverrà esecutiva una volta trascorsi 10 giorni senza che venga proposta opposizione e, in virtù di ciò, deve essere prevista la possibilità di annotare, ed evidenziare nella maschera di dettaglio del procedimento SIUS, la data di esecutività della stessa. La descrizione di tale funzionalità è esposta nel paragrafo successivo.

Nella casistica, invece, in cui venga presentata opposizione, detta opposizione va annotata sul procedimento “provvisorio” utilizzando l’apposita funzione “Impugnazioni/Opposizioni”. Per la gestione delle impugnazioni, il procedimento SIUS seguirà il medesimo processo di lavorazione già in essere per il contenuto ‘Concessione Misure Alternative Alla Detenzione’ (C001).

### REQ-SIE-009-04 TDS/TDSM - Registrazione data Esecutività Ordinanza Applicazione Provvisoria
Per la registrazione della data di esecutività si prevede di aggiungere una nuova voce menù da inserire nella combo box presente nella maschera di dettaglio del procedimento SIUS.


Figura 10: Funzione Esecutività Applicazione Provvisoria m.a.

Dal punto di vista funzionale, l’attività di registrazione della data di esecutività dell’ordinanza di applicazione provvisoria si pone a valle dell’emissione dell’ordinanza provvisoria.
Accedendo alla funzione, il sistema prospetta una nuova pagina in cui deve essere registrata la data di esecutività dell’ordinanza di applicazione provvisoria.
A seguire si mostra un esempio di pagina. Le informazioni da riportare sono:
Dettaglio procedimento SIUS
Dettaglio dati Soggetto
Estremi dell’ordinanza provvisoria di Concessione di Misura Alternativa (art. 678 comma 1 -ter)
Campo ‘Data Esecutività’
Campo note


Figura 11: Pagina Registrazione Esecutività


I campi editabili sono ‘Data Esecutività’ e ‘note, che a seguito del conferma devono essere registrati nella tabella deposito_ordinanza_pc.
Per la data di esecutività, che è dato obbligatorio da inserire, occorre prevedere un controllo che il valore inserito non superi i 10 giorni rispetto alla data di emissione dell’ordinanza provvisoria. Per un data che superi tale limite, visualizzare un messaggio bloccante sulla pagina.

A seguito dell’inserimento, il sistema mostrerà una pagina di dettaglio dell’ordinanza di ammissione provvisoria, mostrando anche la data di esecutività inserita.
Dalla pagina di dettaglio, deve essere possibile accedere alla funzione di modifica della data di esecutività, inoltre deve essere abilitata la stampa, la validazione e la trasmissione telematica verso la Procura titolare del titolo esecutivo per cui è stata presentata istanza di applicazione di misura alternativa. La gestione della ‘recezione’ e ‘lavorazione’ dell’ordinanza di ammissione provvisoria su SIEP è illustrata al par. 3.3.1 [REQ-SIE-009-13].

La data di esecutività impostata, inoltre, dovrà essere visualizzata nella porzione della maschera di dettaglio del procedimento SIUS dedicata ai provvedimenti, come mostrato nella figura che segue:


Figura 12: Sezione Provvedimenti con Data di Esecutività

La stessa informazione dovrà essere replicata nella pagina di dettaglio provvedimenti, che il sistema mostra in corrispondenza del link Provvedimenti.


Figura 13: Pagina Dettaglio Provvedimenti con Data di Esecutività


A seguito dell’emissione dell’ordinanza provvisoria e a partire dalla data in cui diviene esecutiva, si possono delineare diverse possibili gestioni operative, tra cui quelle che seguono:

Il Tribunale di Sorveglianza, conferma senza formalità la decisione del magistrato. (REQ-SIES-009-05)
Incorrere in una revoca dell’ammissione provvisoria, nel caso, ad esempio, di gravi violazioni delle prescrizioni nel corso dell’esecuzione provvisoria.

In questa prima fase di implementazione, illustriamo il dettaglio del primo scenario, ossia la casistica di ‘Conferma’ da parte del Tribunale della decisione del magistrato designato.
Lo scenario di cui al punto 2 è rinviato alla successiva fase di sviluppo (D.lgs. 123/2018 - FASE 2).
### REQ-SIE-009-05 TDS/TDSM - Provvedimento di Conferma Ordinanza Applicazione Provvisoria
A seguito dell’emissione dell’ordinanza provvisoria e a partire dalla data in cui diviene esecutiva, il Tribunale, con decisione del collegio, conferma la decisione del Magistrato Designato.

Per proseguire con l’emissione del provvedimento di conferma, l’utente TDS/TDSM deve procedere con la funzione di emissione ordinanza e/o emissione decreto utilizzando il nuovo contenuto “Concessione misure alternative (art. 678 comma 1-ter c.p.p.)”, previsto al requisito REQ-SIE-00901 al par. 3.2.1.

In particolare, il requisito in oggetto, REQ-SIE-009-05, va ad estendere quanto già definito al requisito REQ-SIE-009-01 in quanto, per il contenuto “Concessione misure alternative (art. 678 comma 1-ter c.p.p.)” deve essere previsto un nuovo oggetto ed un nuovo esito.

L’oggetto da prevedere, ed anche il relativo esito devono avere la seguente dicitura:
Conferma Decisione del Magistrato Relatore

Quando, in fase di iscrizione del procedimento SIUS, viene selezionato l’oggetto ‘Conferma Decisione del Magistrato Relatore’, a video deve apparire una sezione ‘Anno/Progressivo del Procedimento di Ammissione Provvisoria della Misura Alternativa’, dove occorre inserire l’identificativo del procedimento SIUS sul quale è stata inserita l’ordinanza di applicazione provvisoria di misura in esecuzione (con data esecutività inserita).

Figura 14: Pagina iscrizione Procedimento di Conferma Decisione Magistrato Relatore

A seguito dell’iscrizione del procedimento con oggetto ‘Conferma Decisione del Magistrato’, l’utente TDS/TDSM prosegue con la funzione di ‘Emissione Ordinanza’ oppure di ‘Emissione Decreto’.
Il sistema, pertanto, deve permettere di utilizzare il contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.)´sia dalla funzione Ordinanze»Emissione Ordinanza  che  dalla funzione Decreti»Emissione Decreto.

Il flusso di lavorazione del procedimento SIUS che abbia il nuovo contenuto ‘Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) ’ ed oggetto ‘Conferma Decisione del Magistrato relatore’, seguirà quello attualmente in essere per il contenuto ‘Concessione Misure Alternative Alla Detenzione’ (C001) con la gestione della modifica, visualizzazione, cancellazione, stampa, validazione e trasmissione. Le pagine di modifica, visualizzazione e la funzione di stampa devono prevedere in aggiunta a quanto ad oggi presente, l’informazione circa il numero e l’anno dell’ordinanza di ammissione provvisoria.
La funzione di trasmissione, deve prevedere l’invio dell’ordinanza di Conferma (Ratifica), verso la Procura titolare del titolo esecutivo per cui è stata presentata istanza di applicazione di misura alternativa.

#### Adeguamento funzione invio/trasmissione ordinanza/decreto di Conferma - SIUS

In merito alla funzione di trasmissione dell’ordinanza di ‘Conferma/Ratifica’, occorre considerare un ulteriore intervento tecnico - funzionale relativamente all’invio dei dati in formato xml.
Nella creazione del messaggio di scambio, per mezzo delle code jms, in concomitanza dell’invio del provvedimento di ‘conferma/ratifica’ è necessario ‘trasmettere’ anche gli estremi dell’ordinanza di ammissione provvisoria. Inoltre occorre tener conto che la tipologia del provvedimento può essere ordinanza oppure decreto.
La gestione della ‘recezione’ e ‘lavorazione’ dell’ordinanza di ‘Conferma’ su SIEP è illustrata al par.3.3.2 [REQ-SIE-009-13].
### REQ-SIE-009-06 - REQ-SIE-009-07 (Statistiche Misura Alternativa - art. 678 comma 1-ter c.p.p.) )
Per i requisiti in oggetto, per gli uffici TDS/TDSM, il sistema SIUS deve prevedere due nuove tipologie di statistiche attinenti a procedimenti SIUS con contenuto ‘Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.)’.
In particolare in corrispondenza del menù ‘Statistiche/Monitoraggio’ deve essere previsto un nuovo tasto funzione denominato ‘Monitoraggio Misure Alternative (art. 678 comma 1-ter c.p.p.)’ così come raffigurato  nella figura che segue:


Figura 15: Menù Statistiche TDS

Con l’accesso alla funzione, il sistema mostrerà un pagina di ricerca tramite la quale l’utente potrà inserire i dati relativi all’intervallo di tempo o estremi del procedimento da verificare, e sceglie la statistica di interesse.

Le statistiche afferenti ai procedimenti di Misure Alternative (art. 678 comma 1-ter c.p.p.) saranno, limitatamente a questa prima fase, di due tipologie:

Statistica Ordinanze Non Emesse – Trasmessi atti al Presidente [requisito REQ-SIE-009-06];
Statistica Ordinanze Emesse con data di esecutorietà inserita, ma privi di decisione da parte del Collegio [requisito REQ-SIE-009-07];

Nella fase successiva di sviluppo sarà prevista un’ulteriore statistica che afferisce alle Ordinanze di Revoca di Ammissione Provvisoria misura alternativa – Art. 678 comma 1 ter c.p.p.
A seguire si prospetta una pagina di esempio per la scelta della statistica di interesse:

Figura 16: Pagina di Ricerca per Statistiche

A seguito dell’inserimento dei criteri di interesse, e con la sottomissione dei dati al sistema, sarà generata una pagina di elenco con i procedimenti trovati.
Dalla pagina di elenco l’utente poi avrà la possibilità di visualizzare il dettaglio di ogni singolo procedimento SIUS trovato e di esportare il risultato ottenuto in un file excel.


Figura 17: Pagina Elenco Procedimenti per statistiche

Il layout della pagina riportata, in linee generali, sarà il medesimo per tutte le tipologie di statistiche previste.
Per quanto riguarda il foglio excel, le informazioni estratte saranno mostrate secondo il seguente formato.


Figura 18: esempio foglio excel

Per tutte le statistiche, si fa presente, che le estrazioni faranno riferimento allo stato in cui si trova il fascicolo nel momento di elaborazione della statistica.

#### REQ-SIE-009-06 TDS/TDSM - Statistica Ordinanze Non Emesse (Trasmessi Atti al Presidente)

La statistica in oggetto va a recuperare la lista dei procedimenti SIUS iscritti da uffici TDS/TDSM con contenuto di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ che hanno un’ordinanza di applicazione provvisoria di misura alternativa il cui esito è ‘Trasmesso Atti al Presidente’.
Tali procedimenti sono individuabili dal flag ‘Atti trasmessi al Presidente’ posto ad ‘on’ sulla dalla tabella deposito_ordinanza_pc  e dallo stato del procedimento che è posto a ‘Atti trasmessi al Presidente’.
Rientrano in questa categoria anche i procedimenti SIUS iscritti da uffici TDS/TDSM con contenuto di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ per quali risulta inserito il decreto di designazione magistrato, ma non sia mai stata emessa ordinanza. Infatti, il magistrato designato qualora ritenga di non poter applicare alcuna misura, non è tenuto ad emettere un’ordinanza di contenuto negativo, ma può semplicemente lasciar decorrere il tempo assegnatoli. Anche quest’ultimi, infatti, ‘ritornano’ al Presidente del Tribunale Sorveglianza.

#### REQ-SIE-009-07 TDS/TDSM - Statistica Ordinanze Provvisorie Esecutive senza decisione del Collegio

La statistica in oggetto va a recuperare la lista dei procedimenti SIUS iscritti da uffici TDS/TDSM con contenuto di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ che hanno un’ordinanza di applicazione provvisoria di misura alternativa il cui esito è ‘Applica Provvisoriamente’ e per i quali manca il decreto e/o ordinanza di ‘Conferma’ da parte del Collegio o comunque una qualsivoglia decisione da parte del Collegio.
Queste ordinanze sono individuabili, oltre che dall’esito dell’ordinanza corrispondente a ‘Applica Provvisoriamente ’, anche dalla presenza di una data di esecutività inserita in corrispondenza del record di interesse sulla tabella deposito_ordinanza_pc.
Inoltre per il procedimento SIUS da estrarre, non deve esistere un evento che lo lega ad un procedimento SIUS con esito ‘Conferma Decisione del Magistrato Relatore’.
I procedimenti di interesse per questa statistica devono essere tutti quelli per i quali è ‘mancante’ una decisione da parte del Collegio.
Per questa tipologia di statistica, sia nella pagina di elenco che nel relativo foglio Excel, in output deve essere mostrata anche la data di inizio esecutività.
### REQ-SIE-009-08 TDS/TDSM (Aggiornamento Statistica Movimento Provvedimenti per Oggetti)
A seguito dei nuovi interventi previsti per la scheda in oggetto, è necessario aggiornare l’attuale funzione ‘STATISTICHE – MOVIMENTO PROVVEDIMENTI PER OGGETTI’ in modo da integrare la nuova tipologia di ordinanza provvisoria emessa dal magistrato designato. Occorre intervenire sulla maschera di ricerca della statistica, vedi immagine successiva, per fare in modo che il contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ appaia nella lista degli oggetti selezionabili.

Figura 19: Statistica movimento provvedimenti per Oggetti
Parallelamente gestire la nuova informazione anche sul file Excel che viene generato a seguito della Conferma della statistica.
### REQ-SIE-009-09 TDS/TDSM Modifica pagina richiesta atti istruttori
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

Figura 20: Pagina Richiesta Atti Istruttori
In fase di conferma, l’informazione aggiuntiva deve essere registrata nella tabella NOTIFICA, come esplicitato al par. 3.8.9.
I dati inseriti devono inoltre essere riportati nella pagina di dettaglio della richiesta così come mostrato nella pagina che segue:

Figura 21: Dettaglio Richiesta Atti Istruttori
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

Figura 22: Esempio template atto istruttorio

### REQ-SIE-009-10 TDS/TDSM Statistica Atti Istruttori con Data Richiesta Restituzione
Per gli uffici UDS, UDSM, TDS e TDSM, con il requisito in oggetto si chiede di integrare nel menù di Statistiche/Monitoraggio » Ricerche una nuova tipologia di ricerca.
Nella pagina a cui si accede dal menù su indicato, deve essere aggiunto un nuovo tasto funzione così come mostrato nella figura che segue:


Figura 23: Funzione Ricerca Atti Istruttori

Il tasto da introdurre, sarà il punto di accesso alla nuova ricerca da implementare la quale si occuperà di recuperare e conteggiare quali siano i procedimenti SIUS per i quali sia stata fatta richiesta di un atto istruttorio e per la quale richiesta è stata inserita una data di consegna.

L’accesso alla funzione mostrerà una pagina di ricerca in cui immettere i dati per avviare la statistica di interesse.


Figura 24: Pagina ricerca Atti Istruttori


I possibili criteri di ricerca saranno:

Intervallo Estremi Procedimenti
Intervallo Date Iscrizione
Intervallo Date di Richiesta Consegna

Con il tasto ‘Ricerca’ sarà attivata la funzione di estrazione dati che va a recuperare gli estremi del procedimento SIUS, la data iscrizione del procedimento, nome e cognome del soggetto, la data di consegna richiesta ed il tipo di atto istruttorio richiesto.

Le informazioni recuperate devono essere mostrate in una pagina di elenco ed inoltre deve essere prevista la funzione di export in formato excel dei risultati ottenuti.


Figura 25: Elenco procedimenti con atti istruttori


Dalla pagina di elenco, l’utente potrà accedere al dettaglio del procedimento SIUS utilizzando il link posto in corrispondenza del Numero/Anno SIUS.
### REQ-SIE-009-11 (UDS/UDSM – TDS/TDSM Integrazione Lista Mittenti)
«Art. 57 (Legittimazione alla richiesta di misure). - 1. Le misure alternative e quelle di cui agli articoli 30, 30-ter, 52, 53 e 54 nonché' all'articolo 6 del decreto del Presidente della Repubblica 30 maggio 2002, n. 115, possono essere richieste dal condannato, dall’internato, dai loro prossimi congiunti, dal difensore, ovvero proposte dal gruppo di osservazione e trattamento.».
Secondo quando disposto all'art. 7 comma 1 lettera b) del D.lgs. 2 ottobre 2018, n. 123, nell’attuale maschera di iscrizione dei procedimenti SIUS, è necessario integrare le voci presenti in combo ‘Mittente’ con una nuova voce denominata ‘Gruppo di Osservazione e Trattamento’.  Verificare che la modifica sia valida da tutti i punti di accesso alla pagina. (Es: Iscrizione da procedimento SIEP e Iscrizione da Soggetto).

Figura 26: Pagina iscrizione Procedimento SIUS





## Adeguamento D.lgs. 123/2018 – Sottosistema SIEP

Gli uffici Procura della Repubblica Presso il Tribunale Ordinario (PM) e Procura della Repubblica Presso il Tribunale per i Minorenni (PMM), nell’ambito del flusso procedurale previsto dall’ordinamento penitenziario, e così come esposto al documento di cui al RIF5, a seguito di presentazione di istanza di misura alternativa da parte del condannato e/o del difensore, attivano la richiesta di ‘Concessione di Misure Alternative alla Detenzione’ inviando la richiesta al Tribunale di Sorveglianza.

Gli step previsti sono:

La Procura emette un Ordine di Esecuzione con sospensione
Per l’emissione dell’Ordine di Esecuzione con contestuale sospensione, non viene introdotta nessuna novità, l’utente utilizza la funzione ‘Ordini di Esecuzione/Scarcerazione>>Sospensione Esecuzione ex art. 656 c.p.p. >>Ordine di Esecuzione’ già presente a sistema.

Iscrizione Istanza
Per l’iscrizione dell’istanza, l’utente utilizza la funzione Ordini di Esecuzione/Scarcerazione » Sospensione Esecuzione ex art. 656 c.p.p. » Istanza (Annotazione Trasmissione) già presente a sistema.

Trasmissione istanza al Tribunale di Sorveglianza
A valle dell’iscrizione dell’istanza, utilizzando sempre la funzione Ordini di Esecuzione/Scarcerazione » Sospensione Esecuzione ex art. 656 c.p.p. » Istanza (Annotazione Trasmissione), l’utente trasmette gli atti all’ufficio Tribunale di Sorveglianza (TDS/TDSM).


A questo punto, gli atti sono a carico dell’ufficio del Tribunale di Sorveglianza(TDS/TDSM) che ha competenza a decidere sulla richiesta di ‘Concessioni di Misure alternative alla Detenzione’.
Tutte le possibili fasi che possono ‘presentarsi’ lato Sorveglianza, sono stati già esplicitati nei precedenti paragrafi.

Riportiamo un grafico riepilogativo delle possibili casistiche in cui si può incorrere lato Sorveglianza a seguito della concessione di misura, e la relativa correlazione con gli uffici Procura:


Figura 27: Flussi di trasmissione Sorveglianza - Procura

Focalizzandoci sulla trasmissione dei possibili provvedimenti che il Tribunale di Sorveglianza può effettuare, si nota che lato Procura, si hanno tre casistiche da gestire:
Il Tribunale di Sorveglianza (TDS/TDSM), per mezzo di un magistrato designato, ‘applica provvisoriamente’ la misura alternativa emettendo un’ordinanza provvisoria. Nel momento in cui diviene esecutiva, il Tribunale di Sorveglianza trasmette l’ordinanza di applicazione provvisoria alla Procura [REQ-SIE-009-02 (SIUS) e REQ-SIE-009-12 (SIEP)];
Il Tribunale di Sorveglianza (TDS/TDSM), emette ordinanza/decreto di Conferma(Ratifica) della misura alternativa (art. 678 comma 1-ter c.p.p.), applicata provvisoriamente, e trasmette il provvedimento alla Procura [REQ-SIE-009-03 (SIUS) e REQ-SIE-009-13 (SIEP)];
Il Tribunale di Sorveglianza (TDS/TDSM) ‘concede’ una delle misure previste all'articolo 656, comma 5, utilizzando il nuovo contenuto di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ e trasmette l’ordinanza, seguendo il ‘rito ordinario’, alla Procura [REQ-SIE-009-01 (SIUS) e REQ-SIE-009-14 (SIEP)];

Nei paragrafi successivi vengono dettagliate le specifiche di implementazione che intervengo nel sottosistema SIEP in riferimento alle tre casistiche su elencate.
### REQ-SIE-009-12 SIEP - ‘Ammissione Provvisoria misure alternative (art. 678 comma 1-ter c.p.p.) ’
La concessione dell’ammissione provvisoria alla misura alternativa è estesa agli uffici Tribunali di Sorveglianza, che, per mezzo di un magistrato designato, può ‘applicare provvisoriamente’ la misura alternativa concessa secondo quanto previsto all’art. 678 comma 1 ter c.p.p..
L’ordinanza provvisoria diviene esecutiva trascorsi 10 giorni senza che venga proposta opposizione e, a seguito dell’esecutività della stessa, il Tribunale è tenuto a dare tempestiva comunicazione alla Procura prevedendo anche la trasmissione telematica della stessa.

A seguito della trasmissione dell’ammissione provvisoria, la Procura prende in carico l’ordinanza e prosegue con l’inserimento del provvedimento di Ammissione provvisoria della misura alternativa.
Per la gestione della presa in carico dell’ordinanza provvisoria, si faccia riferimento al par. 3.3.2.1 (Adeguamento della Funzione di Presa in Carico).

Secondo quanto previsto all’art. 678 comma1 ter introdotto con il d.lgs. 123/128, l’ordinanza di ammissione provvisoria può essere adottata per le seguenti misure alternative:

Affidamento in prova al servizio sociale (art. 47 O.P. -  art. 678 comma 1-ter c.p.p.);
Affidamento in prova al servizio sociale (art. 94 DPR 309/90 - art. 678 comma 1-ter c.p.p.);
Detenzione domiciliare (art. 47 ter O.P. - art. 678 comma 1-ter c.p.p.);
Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.);
Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.);

L’area funzionale su cui ha impatto la gestione della ‘ammissione provvisoria’ (art. 678 comma 1-ter c.p.p.), è il menù ‘Decisioni della Sorveglianza’. Nello specifico, per ogni tipologia di misura alternativa su elencata, occorre rivedere, integrare, ed in alcuni casi come per la Semilibertà e la Sospensione dell’esecuzione della pena detentiva, creare tutta la gestione della funzionalità di ‘Ammissione Provvisoria’.

Un primo intervento da fare, per le tipologie di misura di ‘Affidamento in prova al servizio Sociale’ e di ‘Detenzione Domiciliare’, che già prevedono il ‘tasto funzione’ dell’ammissione provvisoria, è modificare la Label del pulsante da ‘Ammissione Provvisoria’ in ‘Ammissione Provvisoria/Applicazione Provvisoria Art.678 C1 Ter’.

Figura 28: Tasto Ammissione Provvisoria/Applicazione Provvisoria Art.678 C1 Ter

Invece, per quanto riguarda la Semilibertà il menù attuale deve essere integrato con un nuovo tasto funzione come previsto alla figura che segue [Figura 29].


Figura 29: Tasto Ammissione Provvisoria per SEMILIBERTA'
L’inserimento di tale tasto prevede un’implementazione ex-novo di tutta la funzione di gestione dell’ammissione Provvisoria. Per il dettaglio si rimanda al par. [3.3.1.2].

In riferimento alla Sospensione Dell’esecuzione Della Pena Detentiva, oltre a prevedere un’implementazione ex-novo di tutta la funzione di gestione dell’ammissione Provvisoria occorre riorganizzare il menù per allineare tale misura allo stesso layout delle altre sezioni.
Ciò significa che, a partire dal menù Decisioni Sorveglianza>> Sospensione dell’esecuzione della pena, sarà necessario introdurre una pagina in cui vengono mostrati i ‘tasti funzione’ per gestire la ‘Concessione’ e la ‘‘Ammissione Provvisoria Art.678 C1 Ter’’.


Figura 30: Riorganizzazione menù per Sospensione Esecuzione Pena

Nel ‘tasto funzione’ di ‘Concessione’ dovrà convogliare l’attuale pagina di gestione della ‘Sospensione dell’esecuzione della pena’, mentre per quanto riguarda il tasto di ‘Ammissione Provvisoria Art.678 c1 ter’, è necessario prevede un’implementazione ex-novo. Per il dettaglio si rimanda al par. [3.3.1.3].

Come premessa generale ai dettagli esplicativi riportati ai paragrafi successivi, si definisce che:
L’ordinanza di Ammissione Provvisoria (art. 678 comma 1 ter) è emessa dal magistrato designato ed ha le seguenti peculiarità:

Fa riferimento ad un procedimento SIUS con contenuto Concessione misure alternative (art. 678 comma 1-ter c.p.p.);
E’ relativa ad uno degli oggetti previsti al par. 3.2.1;
E’ caratterizzata dall’esito “Applica Provvisoriamente” ed ha una data di esecutività validata;

#### Adeguamento della Funzione ‘Ammissione Provvisoria’ (Affidamento al Servizio Sociale e Detenzione Domiciliare)

Per il menù ‘Affidamento in Prova al Servizio Sociale’ e per il menù ‘Detenzione Domiciliare’ in corrispondenza del tasto funzione di ‘Ammissione Provvisoria/Applicazione Provvisoria Art.678 c1 ter’, occorre intervenire affinché la pagina attuale gestisca anche le ordinanze con contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ e con esito ‘APPLICA PROVVISORIAMENTE’.

Le implementazioni da prevedere sono relativi ai due punti evidenziati nella figura che segue:

Figura 28: Pagina Ammissione Provvisoria/Applicazione Provvisoria Art.678 c1 ter

Nello specifico, in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare le ordinanze con esito ‘Applica Provvisoriamente’ e che afferiscono al nuovo contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’.
Per quanto riguarda invece il campo ‘Oggetto Ordinanza’, nella combo box corrispondente devono essere previsti i corrispondenti oggetti introdotti su Sorveglianza in associazione del contenuto SIUS di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’.

Le voci da prevedere/rettificare per Affidamento in Prova al Servizio Sociale sono:
Affidamento al Servizio Sociale (Art. 47 O.P. - Art. 678 comma 1-ter c.p.p.)
Affidamento Servizio Sociale (ex art. 94 DPR 309/90 - art. 678 comma 1-ter c.p.p.)

Invece, le voci da prevedere/rettificare per Detenzione Domiciliare sono:
Detenzione domiciliare (art. 47 ter O.P. - art. 678 comma 1-ter c.p.p.);
Detenzione domiciliare (art. 47 ter comma 1 bis O.P. - art. 678 comma 1-ter c.p.p.);
Detenzione domiciliare per ultrasettantenni (art. 47 ter comma 01 O.P. - art. 678 comma 1-ter c.p.p.);

La pagina di emissione dell’ammissione provvisoria (sia per affidamento al servizio sociale che per detenzione domiciliare), attualmente prevede l’inserimento manuale del provvedimento e tale comportamento non deve essere precluso.
Al ‘conferma’ dell’inserimento, nella corrispondente pagina di dettaglio, deve essere riportata la ‘nuova’ descrizione dell’oggetto dell’ordinanza selezionata e tale descrizione deve essere allineata anche sull’elenco dei provvedimenti del PM:

Figura 31: Elenco PM

A seguito dell’emissione del provvedimento occorre inoltre prevedere un aggiornamento dello stato del procedimento e della posizione giuridica con una ‘nuova’ descrizione ad hoc.

Figura 32: Dettaglio procedimento SIEP

Infine è necessario introdurre un nuovo template di stampa da associare all’Ammissione Provvisoria per art.678 c1 ter sia per l’Affidamento Al Servizio Sociale che per la Detenzione Domiciliare.

#### Nuova Funzione di ‘Ammissione Provvisoria’ per SEMILIBERTA

Nella pagina dei menù relativa alla Semilibertà, per il requisito in oggetto, occorre prevedere l’aggiunta di un nuovo tasto dedicato alla gestione dell’Ammissione Provvisoria per la misura di Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.).


Figura 33: Tasto Funzione di Ammissione Provvisoria Art. 678 c1 per SEMILIBERTA'

Tramite l’accesso alla funzione, il sistema deve mostrare una pagina per permettere all’utente di registrare l’ordinanza di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ relativa alla Semilibertà e con esito ‘applica provvisoriamente’.
Si riporta un esempio di come verrà implementata la pagina:


Figura 34: Pagina Inserimento Ammissione Provvisoria Art. 678 c1 ter - SEMILIBERTA'

Nella prima sezione devono essere riepilogati i dati del procedimento di classe I cui fa riferimento la decisione della Sorveglianza.
A seguire, va prevista la sezione dei dati del Provvedimento della Sorveglianza:
Anno/Numero SIUS
Anno/Numero del provvedimento (ordinanza del TDS/TDSM)
Ufficio Emittente
Sede Emittente
Tipologia Provvedimento (ordinanza/decreto)
Oggetto Decisione (Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.))
Data emissione (preimpostata con data di sistema)
Luogo della Prova
Note
Eseguita Procura/Sorveglianza (Radio button)
Data inizio misura

A completamento della pagina occorre prevedere:
Sezione Magistrato Firmatario
Sezione Destinatario dell’Esecuzione
Sezione Destinatario per Notifica


In corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare le ordinanze con esito ‘Applica Provvisoriamente’ e che afferiscono al contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ ed hanno come oggetto associato il codice corrispondente alla ‘Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.)’.
Per quanto riguarda invece il campo ‘Oggetto Decisione, nella combo box corrispondente deve essere previsto l’oggetto ‘Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.)’.

I dati da impostare nella sezione ‘Provvedimenti della Sorveglianza’, possono essere recuperati in automatico dal link su descritto, ma possono essere inseriti anche manualmente da parte dell’utente. Infatti i campi di tale sezione devono essere tutti editabili.

In fase di conferma, il sistema deve verificare l’obbligatorietà dei seguenti campi:

Ufficio Emittente
Sede Emittente
Tipologia Provvedimento (ordinanza/decreto)
Oggetto Decisione (Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.))
Inserimento di almeno un Destinatario

A seguito del salvataggio deve essere prevista una pagina di dettaglio, attenendosi allo stesso layout delle pagine di dettaglio generate in fase di conferma dell’inserimento dell’ammissione provvisoria di altre tipologie di misure.
Dalla pagina di dettaglio deve essere possibile ‘stampare’ e ‘validare’ l’ordine di esecuzione dell’ammissione provvisoria alla Semilibertà.


Figura 35: Pagina di Dettaglio Ammissione Provvisoria Art. 678 ter c1 - SEMILIBERTA'

Con l’accesso alla funzione di stampa  , il sistema deve generare un nuovo documento i cui dettagli specifici saranno forniti dall’Amministrazione.
Il tasto di ‘upload’ ,invece, deve permettere la validazione diretta dell’ordine di esecuzione.
Dall’elenco dei provvedimenti del PM, l’utente può intervenire per l’eventuale cancellazione dell’ordine di esecuzione, ma ciò deve essere possibile solo se il provvedimento non è ancora stato validato.


Figura 36: Funzione di cancellazione

In concomitanza alla validazione deve essere previsto l’aggiornamento dello stato del procedimento e la posizione giuridica del soggetto. Le descrizioni precise da associare saranno fornite dall’Amministrazione.
Il nuovo ordine di esecuzione deve essere integrato nello stato di esecuzione e deve essere considerato nelle estrazioni del riepilogo ispettivo e lavoro magistrati [3.3.3];

#### Nuova Funzione di ‘Ammissione Provvisoria’ per Sospensione Esecuzione della Pena Detentiva

Nella pagina dei menù relativa alla Sospensione Esecuzione della Pena, per il requisito in oggetto, occorre prevedere l’aggiunta di un nuovo tasto dedicato alla gestione dell’Ammissione Provvisoria per la misura di Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.).


Figura 37: Ammissione Provvisoria Art. 678 c1 ter - Sospensione Esecuzione della Pena

Tramite l’accesso alla funzione, il sistema deve mostrare una pagina per permettere all’utente di registrare l’ordinanza di Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.).
Si riporta un esempio di come deve essere implementata la pagina di inserimento:


Figura 38: Pagina Inserimento Ammissione Provvisoria - Sospensione dell'esecuzione della pena

Nella prima sezione devono essere riepilogati i dati del procedimento di classe I cui fa riferimento la decisione della Sorveglianza.
A seguire, va prevista la sezione dei dati del Provvedimento della Sorveglianza:
Anno/Numero SIUS
Anno/Numero del provvedimento (ordinanza del TDS/TDSM)
Tipo Provvedimento (ordinanza/decreto)
Autorità Emittente
Sede Autorità Emittente
Oggetto Provvedimento
Data emissione provvedimento (preimpostata con data di sistema)
Motivazioni
Data Sospensione Esecuzione

A completamento della pagina occorre prevedere:
Sezione Magistrato Firmatario
Sezione Destinatari

In corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare le ordinanze con esito ‘Applica Provvisoriamente’ e che afferiscono al contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ ed hanno come oggetto associato il codice corrispondente alla ‘Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.)’.
Per quanto riguarda invece il campo ‘Oggetto Ordinanza’, nella combo box corrispondente deve essere previsto l’oggetto ‘Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.))’.

I dati da impostare nella sezione ‘Provvedimenti della Sorveglianza’, possono essere recuperati in automatico dal link su descritto, ma possono essere inseriti anche manualmente da parte dell’utente. Infatti i campi di tale sezione devono essere tutti editabili.

In fase di conferma, il sistema deve verificare l’obbligatorietà dei seguenti campi:

Autorità Emittente
Sede Autorità Emittente
Tipologia Provvedimento (ordinanza/decreto)
Oggetto Provvedimento
Data Emissione
Data Sospensione Esecuzione
Selezione di almeno un destinatario

A seguito del salvataggio deve essere prevista una pagina di dettaglio, attenendosi allo stesso layout delle pagine di dettaglio generate in fase di conferma dell’inserimento dell’ammissione provvisoria di altre tipologie di misure.
Dalla pagina di dettaglio deve essere possibile ‘stampare’ e ‘validare’ l’ordine di esecuzione dell’ammissione provvisoria alla Sospensione dell’esecuzione della pena.


Figura 39: Pagina di Dettaglio Ammissione Provvisoria Art. 678 ter c1 - Sospensione dell’esecuzione della pena
Con l’accesso alla funzione di stampa  , il sistema deve generare un nuovo documento i cui dettagli specifici saranno forniti dall’Amministrazione.
Il tasto di ‘upload’ ,invece, deve permettere la validazione diretta dell’ordine di esecuzione.
Dall’elenco dei provvedimenti del PM, l’utente può intervenire per l’eventuale cancellazione dell’ordine di esecuzione, ma ciò deve essere possibile solo se il provvedimento non è ancora stato validato.

Figura 40: Funzione di cancellazione

In concomitanza alla validazione deve essere previsto l’aggiornamento dello stato del procedimento e la posizione giuridica del soggetto. Le descrizioni precise da associare saranno fornite dall’Amministrazione.
Il nuovo ordine di esecuzione deve essere integrato nello stato di esecuzione e deve essere considerato nelle estrazioni del riepilogo ispettivo e lavoro magistrati [3.3.3];

### REQ-SIE-009-13 SIEP – ‘Conferma dell’Ammissione Provvisoria misure alternative (art. 678 comma 1-ter c.p.p.) ’ e    REQ-SIE-009-14 SIEP -  ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’

I requisiti REQ-SIE-009-13 e REQ-SIE-009-14 sono esposti parallelamente nello stesso paragrafo in quanto, dal punto di vista applicativo, intervengono sulle medesime funzioni.

Il primo requisito [REQ-SIE-009-13] attiene alla gestione della recezione da parte della Procura di un provvedimento (ordinanza/decreto) che il Tribunale di Sorveglianza emette per ‘confermare’ l’ordinanza di ammissione provvisoria [REQ-SIE-009-05 par. 3.2.5].

Per il secondo requisito [REQ-SIE-009-13], invece, siamo nella casistica in cui il Tribunale di Sorveglianza (TDS/TDSM) concede una delle misure previste all'articolo 656, comma 5, utilizzando il nuovo contenuto di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ ma l’ordinanza o il decreto sono emessi con ‘rito ordinario’.
Si specifica che è possibile incorrere nella casistica del rito ordinario quando, per misura alternativa concessa in relazione all’art. 678 comma 1-ter c.p.p., il magistrato designato non abbia provveduto ad emettere l’ordinanza di ammissione provvisoria nei termini stabiliti, oppure nel caso in cui, il magistrato designato ritenga di non poter applicare alcuna delle misure concedibili rimettendo gli atti al Presidente del Tribunale di Sorveglianza.

Nell’ambito dell’art. 678 comma 1-ter c.p.p., le possibili misure che posso essere concesse sono:
Affidamento in prova al servizio sociale (art. 47 O.P. -  art. 678 comma 1-ter c.p.p.);
Affidamento in prova al servizio sociale (art. 94 DPR 309/90 - art. 678 comma 1-ter c.p.p.);
Detenzione domiciliare (art. 47 ter O.P. - art. 678 comma 1-ter c.p.p.);
Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.);
Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.);

A seguito di emissione di un’ordinanza, sia essa emessa con rito ordinario, che emessa quale ‘conferma’ dell’ammissione provvisoria, l’ufficio di Sorveglianza, dopo aver opportunamente validato e depositato il provvedimento, lo trasmette telematicamente all’ufficio Procura titolare del procedimento di classe I – SIEP su cui ha provveduto ad iscrivere procedimento SIUS [par. 3.2.5.1];
A questo punto, nell’ambito dei requisiti in oggetto, un primo ‘impatto’ da gestire lato Procura è la recezione dell’ordinanza/decreto.

#### Adeguamento della Funzione di Presa in Carico Provvedimento – SIEP
Il sistema deve essere allineato al fine di poter recuperare il nuovo provvedimento (ordinanza/decreto) trasmesso telematicamente dagli uffici Tribunale di Sorveglianza.

Nella funzione di Presa in Carico, pertanto, il sistema deve ‘considerare’ la possibilità che tra i messaggi in entrata, tramite le code jms, possano esserci anche provvedimenti legati alla nuova tipologia di contenuto di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’.



Figura 41: Lista atti ricevuti

Dalla lista degli atti ricevuti, l’utente, alla stregua di quanto già è previsto per le altre tipologie di provvedimento, avrà la possibilità di entrare nella funzione di dettaglio dell’ordinanza/decreto ricevuto e proseguire con la presa in carico del provvedimento stesso.

Figura 42: Pagina di Conferma di Presa in Carico
Secondo quanto già specificato al par. 3.2.5.1, nel flusso xml oggetto della trasmissione, unitamente all’ordinanza di ‘conferma’ deve essere recepita e gestita anche l’ordinanza di ammissione provvisoria a cui la ‘conferma’ è relativa.
Procedendo con la ‘Conferma della presa in Carico’, il provvedimento sarà ‘registrato’ negli archivi del distretto di appartenenza dell’ufficio e risulterà ‘lavorabile’ dall’ufficio stesso.

#### Adeguamento della Funzione ‘Decisioni Sorveglianza’ – SIEP

Il menù ‘Decisioni Sorveglianza’ è oggetto di molteplici interventi. Infatti, al fine di allineare il sistema all’introduzione dell’art. art. 678 comma 1-ter c.p.p., è necessario intervenire in diversi sottomenù presenti nella sezione ‘Misure Alternative’ e nella sezione delle ‘Sospensioni’.

Nell’immagine che segue ne sono evidenziati i punti:

Figura 43: Sezione misure alternative/sospensioni

Un primo intervento di cui è fatta richiesta è la modifica della Label del tasto funzione di ‘Concessione’ in “Concessione/Ratifica (art 678) della misura”. Questo intervento va applicato ad ogni tipologia di misura evidenziata nella precedente figura [Figura 43: Sezione misure alternative/sospensioni].

A seguire, invece, si espongono gli interventi da espletare per ogni singola misura alternativa:

Affidamento in Prova al Servizio Sociale
Per il menù ‘Affidamento in Prova al Servizio Sociale’, in corrispondenza del tasto funzione di ‘Concessione/Ratifica (art 678)’ della misura, occorre intervenire affinché la pagina attuale gestisca anche i provvedimenti del Tribunale di Sorveglianza che ‘concedono’ oppure che ‘ratificano’ la misura alternativa ‘Affidamento in prova al servizio sociale (art. 47 O.P. -  art. 678 comma 1-ter c.p.p.)’.

I provvedimenti che devono essere gestiti, in aggiunta a quelli attualmente previsti in questa sezione, hanno le seguenti peculiarità:

Fanno riferimento ad un procedimento SIUS con contenuto Concessione misure alternative (art. 678 comma 1-ter c.p.p.);
Sono relativi ad uno degli oggetti previsti al par. 3.2.1;
Sono caratterizzati dall’esito “Concede” oppure dall’esito “Conferma Decisione del Magistrato Relatore”;

Le implementazioni da prevedere sono relativi ai punti evidenziati nella figura che segue:

Figura 44: Funzione di 'Concessione/Ratifica art.678 Affidamento in Prova' - SIEP

Nello specifico, in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare le ordinanze/decreti con esito ‘Concede’ oppure con esito ‘Conferma Decisione del Magistrato Relatore’ e che afferiscono al nuovo contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ ed il cui oggetto sia uno dei seguenti:
Affidamento in prova al servizio sociale (art. 47 O.P. -  art. 678 comma 1-ter c.p.p.);
Affidamento in prova al servizio sociale (art. 94 DPR 309/90 - art. 678 comma 1-ter c.p.p.);

Per quanto riguarda invece il campo ‘Oggetto Ordinanza’, nella combo box corrispondente devono essere previsti i corrispondenti oggetti introdotti su Sorveglianza in associazione del contenuto SIUS di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ per ciò che attiene all’Affidamento al Servizio Sociale.
Le voci da prevedere/rettificare sono:
Affidamento al Servizio Sociale (Art. 47 O.P. - Art. 678 comma 1-ter c.p.p.)
Affidamento Servizio Sociale (ex art. 94 DPR 309/90 - art. 678 comma 1-ter c.p.p.)

Su questa stessa pagina, sempre nella sezione ‘dati sorveglianza’ occorre integrare un nuovo campo, di tipologia combo box, denominato ’Tipo Provvedimento’, in cui mostrare le due tipologie di provvedimenti che la sorveglianza può emettere: ordinanza e decreto. L’integrazione è necessaria in quanto per la ‘ratifica’ è fatta richiesta di prevedere la possibilità per il Tribunale di poter emettere sia l’ordinanza che il decreto [REQ-SIE-009-05 par. 3.2.5].
Inoltre, la pagina va integrata anche con i campi anno e numero dell’ordinanza provvisoria a cui la ‘ratifica’ si riferisce. Tali informazioni devono essere recepite dal provvedimento della sorveglianza selezionato in pop-up.

Al ‘conferma’ dell’inserimento, nella pagina di dettaglio del provvedimento di concessione/ratifica (art. 678 c.p.p) di affidamento in prova, deve essere riportata la ‘nuova’ descrizione dell’oggetto dell’ordinanza/decreto selezionato ed, oltre agli estremi dell’ordinanza di ratifica anche gli estremi (anno/numero) dell’ordinanza provvisoria.
La pagina di emissione della concessione dell’affidamento al servizio sociale, attualmente prevede l’inserimento manuale del provvedimento e tale comportamento non deve essere precluso, pertanto tutti i campi della sezione ‘Dati Tribunale della Sorveglianza ‘ devono essere editabili.

La nuova descrizione deve essere prevista anche in fase di stampa ed in virtù di ciò, è necessario introdurre un nuovo template di stampa da associare alla ‘ratifica’ dell’ammissione provvisoria per l’Affidamento al servizio sociale.

A seguito della validazione del provvedimento di Concessione/Ratifica dell’Affidamento in Prova, deve essere allineata anche la descrizione sull’elenco provvedimenti del PM:

Figura 45: Elenco provvedimenti PM

Inoltre, a valle della validazione del provvedimento occorre prevedere un aggiornamento dello stato del procedimento e della posizione giuridica con una ‘nuova’ descrizione ad hoc.

Figura 46: Aggiornamento dello Stato del Procedimento e Posizione Giuridica





Detenzione Domiciliare
La Detenzione domiciliare (art. 47 ter O.P. - art. 678 comma 1-ter c.p.p.), è un’ulteriore misura alternativa prevista dall’art. 656 comma 5, che può essere concessa in relazione all’ art. 678 comma 1-ter c.p.p. introdotto dal D.lgs. 123/2018.
Anche per questa tipologia di misura occorre intervenire affinché il sistema SIEP possa recepire l’ordinanza/decreto emessi dal Tribunale di Sorveglianza che concede/ratifica la misura.

In corrispondenza del tasto funzione di ‘Concessione/Ratifica (art 678)’ relativa al menù’ ‘Detenzione Domiciliare’ evidenziato in [Figura 43: Sezione misure alternative], è necessario intervenire su due punti in particolare:
link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	[Figura 47];
Combo box Oggetto Ordinanza [Figura 47];


Figura 47: Pagina di Concessione/Ratifica art.678  Detenzione Domiciliare
Dal link che apre la pop-up delle ordinanze della Sorveglianza, il sistema deve recuperare ed elencare anche le ordinanze relative alla concessione di Detenzione domiciliare (art. 47 ter O.P. - art. 678 comma 1-ter c.p.p.) e alla ratifica dell’ammissione provvisoria alla Detenzione domiciliare (art. 47 ter O.P. - art. 678 comma 1-ter c.p.p.).
Allo stesso tempo per il campo ‘Oggetto Ordinanza’, nella combo box corrispondente devono essere previsti gli oggetti introdotti su Sorveglianza in associazione del contenuto SIUS di ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ in relazione alla detenzione domiciliare.

Le voci da prevedere/rettificare sono:
Detenzione domiciliare (art. 47 ter O.P. - art. 678 comma 1-ter c.p.p.);
Detenzione domiciliare (art. 47 ter comma 1 bis O.P. - art. 678 comma 1-ter c.p.p.);
Detenzione domiciliare per ultrasettantenni (art. 47 ter comma 01 O.P. - art. 678 comma 1-ter c.p.p.);

Su questa stessa pagina, sempre nella sezione ‘dati sorveglianza’ occorre intervenire anche per integrare un nuovo campo combo box denominato ’Tipo Provvedimento’ in cui mostrare le due tipologie di provvedimenti che la sorveglianza può emettere: ordinanza e decreto.
Inoltre, la pagina va integrata anche con i campi anno e numero dell’ordinanza provvisoria a cui la ‘ratifica’ si riferisce. Tali informazioni devono essere recepite dal provvedimento della sorveglianza selezionato in pop-up.

Al ‘conferma’ dell’inserimento, nella pagina di dettaglio del provvedimento di detenzione domiciliare, deve essere riportata la ‘nuova’ descrizione dell’oggetto dell’ordinanza/decreto selezionato ed, oltre agli estremi dell’ordinanza di ratifica anche gli estremi (anno/numero) dell’ordinanza provvisoria.
La nuova descrizione deve essere prevista anche in fase di stampa ed in virtù di ciò, è necessario introdurre un nuovo template da associare alla ‘ratifica’ dell’ammissione provvisoria per Detenzione Domiciliare.

A seguito della validazione del provvedimento di Concessione/Ratifica della Detenzione Domiciliare, è necessario prevedere l’allineamento delle descrizioni nella funzione di ‘Elenco Provvedimento del PM’, gestire lo stato del procedimento e la posizione giuridica.

Semilibertà
Anche per la concessione/ratifica della misura di Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.), nella pagina mostrata in corrispondenza della funzione di ‘Concessione/Ratifica (art 678) ’ è necessario intervenire su seguenti due punti:
link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ ;
Combo box Oggetto Ordinanza;

Dal link che apre la pop-up delle ordinanze della Sorveglianza, il sistema deve pertanto recuperare ed elencare le ordinanze/decreti relativi alla concessione di Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.) o alla ratifica ammissione Provvisiona della Semilibertà, mentre per il campo ‘Oggetto Ordinanza’, nella combo box corrispondente deve essere prevista la voce ‘Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.)’.

Su questa stessa pagina, sempre nella sezione ‘dati sorveglianza’ occorre intervenire anche per integrare un nuovo campo combo box denominato ’Tipo Provvedimento’ in cui mostrare le due tipologie di provvedimenti che la sorveglianza può emettere: ordinanza e decreto.
Inoltre, la pagina va integrata anche con i campi anno e numero dell’ordinanza provvisoria a cui la ‘ratifica’ si riferisce. Tali informazioni devono essere recepite dal provvedimento della sorveglianza selezionato in pop-up.

Al ‘conferma’ dell’inserimento, nella pagina di dettaglio del provvedimento di semilibertà, deve essere riportata la ‘nuova’ descrizione dell’oggetto dell’ordinanza/decreto selezionato ed, oltre agli estremi dell’ordinanza di ratifica anche gli estremi (anno/numero) dell’ordinanza provvisoria.
La nuova descrizione deve essere prevista anche in fase di stampa ed in virtù di ciò, è necessario introdurre un nuovo template da associare alla ‘ratifica’ della Semilibertà (art. 50 comma 1 O.P. - art. 678 comma 1-ter c.p.p.) .
Cosi come già previsto in merito alle altre misure, anche per la Semilibertà è necessario prevedere l’allineamento delle descrizioni nella funzione di ‘Elenco Provvedimento del PM’, gestire lo stato del procedimento e la posizione giuridica.

Sospensione Esecuzione Pena
Alla stregua di tutte le altre tipologie di misure alternative alle detenzione esposte ai punti precedenti, anche per la casistica della ‘Sospensione dell’esecuzione della pena (art. 90 DPR 309/90) ’ è previsto un intervento per allineare la funzione alla ‘concessione’ e ‘ratifica’ previste in ottemperanza all’ art. 678 comma 1-ter c.p.p. (D.lgs. 123/2018).
I punti in cui intervenire sono:
link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	[Figura 48];
Combo box Oggetto Ordinanza [Figura 48];


Figura 48: Concessione/Ratifica art. 678 Sospensione Esecuzione Pena

Dal link che apre la pop-up delle ordinanze della Sorveglianza, il sistema deve pertanto recuperare ed elencare le ordinanze relative alla concessione della misura di Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.) e i decreti/ordinanze di ‘ratifica’ della misura di Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.) , mentre per il campo ‘Oggetto Ordinanza’, nella combo box corrispondente deve essere prevista la voce ‘Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.) ’.
Inoltre, la pagina va integrata anche con i campi anno e numero dell’ordinanza provvisoria a cui la ‘ratifica’ si riferisce. Tali informazioni devono essere recepite dal provvedimento della sorveglianza selezionato in pop-up.

Al ‘conferma’ dell’inserimento, nella pagina di dettaglio del provvedimento di Sospensione Pena, deve essere riportata la ‘nuova’ descrizione dell’oggetto dell’ordinanza/decreto selezionato ed, oltre agli estremi dell’ordinanza di ratifica anche gli estremi (anno/numero) dell’ordinanza provvisoria.
La nuova descrizione deve essere prevista anche in fase di stampa ed in virtù di ciò, è necessario introdurre un nuovo template di stampa da associare alla ‘ratifica’ dell’ammissione provvisoria alla misura di ‘Sospensione dell’esecuzione della pena (art. 90 DPR 309/90 - art. 678 comma 1-ter c.p.p.) ’.
Cosi come già previsto in merito alle altre misure, è necessario prevedere l’allineamento delle descrizioni nella funzione di ‘Elenco Provvedimento del PM’, gestire lo stato del procedimento e la posizione giuridica.

### REQ-SIE-009-16 SIEP - Aggiornamento della funzione di riepilogo ispettivo e Statistiche lavoro magistrati
A seguito dei nuovi interventi previsti per la scheda in oggetto, è necessario aggiornare l’attuale funzione di
‘Statistica Attività Magistrati’ e ‘Riepilogo Ispettivo’.
Nello specifico, per la statistica attività magistrati, nel file excel generato è richiesto di integrare le sezioni attinenti alle Ammissioni Provvisorie delle Misure Alternative e alle Ratifiche delle Misure Alternative.


Figura 49: file excel per Statistica Attività Magistrati
Invece, per quanto riguarda il riepilogo ispettivo, occorre innanzitutto allineare la pagina attualmente presente con le nuove categorie di provvedimenti legati all’implementazione del d.lgs. 123/2018:
Ammissione Provvisoria a Affidamento in Prova al Servizio Sociale (art. 678 c1 ter);
Ammissione Provvisoria a Detenzione Domiciliare (art. 678 c1 ter);
Ammissione Provvisoria a Semilibertà (art. 678 c1 ter);
Ammissione Provvisoria a Sospensione Esecuzione Pena (art. 678 c1 ter);

Ratifica dell’Applicazione Provvisoria a Affidamento in Prova al Servizio Sociale (art. 678 c1 ter);
Ratifica dell’Applicazione Provvisoria a Detenzione Domiciliare (art. 678 c1 ter);
Ratifica dell’Applicazione Provvisoria a Semilibertà (art. 678 c1 ter);
Ratifica dell’Applicazione Provvisoria Sospensione Esecuzione Pena (art. 678 c1 ter);


Figura 50: Pagina di Ricerca Riepilogo Ispettivo

Poi, in base alla categoria selezionata, integrare il file excel riportando le informazioni così come previsto per le categorie già presenti a sistema. A seguire un esempio dii output del file.

Figura 51: file Excel per riepilogo ispettivo

## Gestione dei Template – Sottosistema SIUS e SIEP
Con lo scopo di facilitare l’individuazione degli interventi affini al ‘modulo’ dei template, per ogni requisito si esplicita la necessità di creazione di nuovi template o alla modifica di template già esistenti.

REQ-SIE-009-01 TDS/TDSM - Concessione misure alternative (art. 678 comma 1-ter c.p.p.)
Per provvedimenti con contenuto di Concessione misure alternative (art. 678 comma 1-ter c.p.p.) che seguono, per varie ipotesi il ‘rito ordinario’, saranno agganciati i templati ad oggi già presenti a sistema per le ordinanze di ‘Affidamento in Prova’, ‘Semilibertà, ‘Detenzione Domiciliare e ‘Sospensione Pena’;

REQ-SIE-009-02 TDS/TDSM - Emissione del Decreto Presidenziale di Designazione
Creazione di un nuovo template per ‘Decreto di Designazione’ da agganciare alla stampa del dettaglio del decreto;
Integrazione di informazioni su template di stampa fascicolo (SIUS_ST_STAMPAFASCICOLO.rtf) per visualizzare il magistrato designato;

REQ-SIE-009-03 TDS/TDSM - Emissione Ordinanza Applicazione Provvisoria
Creazione di un nuovo template per ‘Ordinanza di Ammissione Provvisoria’ per Affidamento al Servizio Sociale
Creazione di un nuovo template per ‘Ordinanza di Ammissione Provvisoria’ per Detenzione Domiciliare
Creazione di un nuovo template per ‘Ordinanza di Ammissione Provvisoria’ per Semilibertà
Creazione di un nuovo template per ‘Ordinanza di Ammissione Provvisoria’ per Sospensione Esecuzione Pena

REQ-SIE-009-04 TDS/TDSM - Registrazione data Esecutività Ordinanza Applicazione Provvisoria
Intervenire sui template di cui al REQ-SIE-009-03, prevedendo la stampa della data di esecutività inserita a sistema.
Integrazione di informazioni sul template di stampa fascicolo (SIUS_ST_STAMPAFASCICOLO.rtf) per visualizzare la data di esecutività.

REQ-SIE-009-05 TDS/TDSM - Provvedimento di Conferma Ordinanza Applicazione Provvisoria
Creazione di un nuovo template per ordinanza di ‘Conferma’ per Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) relativamente all’ Affidamento al Servizio Sociale
Creazione di un nuovo template per decreto di ‘Conferma’ per Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) relativamente all’ Affidamento al Servizio Sociale
Creazione di un nuovo template per ordinanza di ‘Conferma’ per Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) relativamente alla Detenzione Domiciliare;
Creazione di un nuovo template per decreto di ‘Conferma’ per Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) relativamente alla Detenzione Domiciliare;
Creazione di un nuovo template per ordinanza di ‘Conferma’ per Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) relativamente alla Semilibertà;
Creazione di un nuovo template per decreto di ‘Conferma’ per Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) relativamente alla Semilibertà;
Creazione di un nuovo template per ordinanza di ‘Conferma’ per Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) relativamente alla Sospensione dell’Esecuzione della Pena;
Creazione di un nuovo template per decreto di ‘Conferma’ per Concessione Misura Alternativa (art. 678 comma 1-ter c.p.p.) relativamente alla Sospensione dell’Esecuzione della Pena;
Integrazione di informazioni su template di stampa fascicolo (SIUS_ST_STAMPAFASCICOLO.rtf) per visualizzare la decisione di conferma.

REQ-SIE-009-09 TDS/TDSM Modifica pagina richiesta atti istruttori
Per questo requisito si rimanda al par. 3.2.8, dove esiste già un elenco completo dii template da modificare.

REQ-SIE-009-12 SIEP - ‘Ammissione Provvisoria misure alternative (art. 678 comma 1-ter c.p.p.) ’
Creazione di nuovo template di stampa da associare al provvedimento SIEP relativo all’Ammissione Provvisoria art.678 c1 ter per l’Affidamento;
Creazione di nuovo template di stampa da associare al provvedimento SIEP relativo all’Ammissione Provvisoria art.678 c1 ter per la Detenzione Domiciliare;
Creazione di nuovo template di stampa da associare al provvedimento SIEP relativo all’Ammissione Provvisoria art.678 c1 ter per Semilibertà;
Creazione di nuovo template di stampa da associare al provvedimento SIEP relativo all’Ammissione Provvisoria art.678 c1 ter per Sospensione Esecuzione della Pena;

REQ-SIE-009-13 SIEP – ‘Conferma dell’Ammissione Provvisoria misure alternative (art. 678 comma 1-ter c.p.p.) ’
Creazione di nuovo template di stampa da associare al provvedimento SIEP relativo alla ‘Conferma dell’Ammissione Provvisoria art.678 c1 ter’ per l’Affidamento
Creazione di nuovo template di stampa da associare al provvedimento SIEP relativo alla ‘Conferma dell’Ammissione Provvisoria art.678 c1 ter’ per la Detenzione Domiciliare.
Creazione di nuovo template di stampa da associare al provvedimento SIEP relativo alla ‘Conferma dell’Ammissione Provvisoria art.678 c1 ter’ per Semilibertà
Creazione di nuovo template di stampa da associare al provvedimento SIEP relativo alla ‘Conferma dell’Ammissione Provvisoria art.678 c1 ter’ per Sospensione Esecuzione della Pena

REQ-SIE-009-14 SIEP -  ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’
Per provvedimenti con contenuto di Concessione misure alternative (art. 678 comma 1-ter c.p.p.) che, lato Sorveglianza, hanno seguito per varie ipotesi il ‘rito ordinario’, lato Procura, saranno agganciati i templati ad oggi già presenti a sistema per le comunicazioni/ordini di esecuzione per ‘Affidamento in Prova’, ‘Semilibertà, ‘Detenzione Domiciliare e ‘Sospensione Pena’;
Si riserva, in ogni caso, la possibilità di dover intervenire per ulteriori integrazioni.
## Moduli sw
L’intervento software riguarderà il progetto SIES. In particolare per quanto attiene a questa prima fase, le classi coinvolte saranno relative soprattutto ai package java relativi a sius e siep.
Il pacchetto interessato è, in ogni caso, il sies.war.
## Architettura
N.A.
## Interfacce utente
Le interfacce utente sono state esplicitate nella descrizione dell’intervento per ogni singolo requisito.
## Basi dati
Nel seguente paragrafo sono elencate le attività inerenti alla banca dati per ogni requisito individuato ai paragrafi precedenti.
### Base Dati - REQ-SIE-009-01 (TDS/TDSM - Concessione misure alternative (art. 678 comma 1-ter c.p.p.))
Per censire il nuovo contenuto, nella tabella cg_refs_code, deve essere aggiunto un nuovo valore per il dominio OGGETTO_PROCEDIMENTO.
Sempre nella tabella cg_refs_code, devono essere mappati gli oggetti relativi al nuovo contenuto, prevedendo dei nuovi record per il dominio MOTIVO_PROVVEDIMENTO.
Sempre nella tabella cg_refs_code, devono essere mappati gli esiti relativi al nuovo contenuto, prevedendo dei nuovi record per il dominio ESITO_TENORE.
### Base Dati - REQ-SIE-009-02 (TDS/TDSM - Emissione del Decreto Presidenziale di Designazione)
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
### Base Dati - REQ-SIE-009-03 (TDS/TDSM - Emissione Ordinanza Applicazione Provvisoria)
Per censire la nuova funzione (Ordinanza Applicazione Provvisoria M.A.) occorre registrare l’informazione sulle seguenti tabelle:
funzione
funzione_profilo
relazione_funzioni
Prevedere una nuova Tipologia Ordinanza: ordinanza provvisoria
Per la creazione della nuova tipologia di ordinanza (ordinanza provvisoria), censire il dato nella tabella cg_refs_code, nella quale deve essere aggiunto un nuovo valore per il dominio TIPO_ATTO.
Aggiungere nuovi campi in tabella deposito_ordinanza_pc per gestire il flag ‘Atti trasmessi al Presidente’.
Per censire il nuovo stato procedimento, nella tabella cg_refs_code, deve essere aggiunto un nuovo valore per il dominio STATO_PROCEDIMENTO (atti trasmessi al Presidente).
Per la registrazione i nuovi template da associare alle ordinanze di Applicazione Provvisoria, occorre prevedere nuovi record nella tabella template.
### Base Dati - REQ-SIE-009-04 (TDS/TDSM - Registrazione data Esecutività Ordinanza Applicazione Provvisoria)
Per censire la nuova funzione (Registrazione data Esecutività Ordinanza Applicazione Provvisoria) occorre registrare l’informazione sulle seguenti tabelle:
funzione
funzione_profilo
relazione_funzioni
Aggiungere nuovi campi in tabella deposito_ordinanza_pc per gestire i campi di Data Esecutività dell’ordinanza.
### Base Dati - REQ-SIE-009-05 (TDS/TDSM - Provvedimento di Conferma Ordinanza Applicazione Provvisoria)
Per questo requisito sono previsti nuovi valori ad integrazione delle attività già descritte in REQ-SIE-009-01. Quindi per questo requisito sono da considerare le attività del requisito REQ-SIE-009-01.
### Base Dati - REQ-SIE-009- 06 (TDS/TDSM - Statistica Ordinanze Non Emesse (Trasmessi Atti al Presidente))
Nessun intervento strutturale a tabelle.
### Base Dati - REQ-SIE-009- 07 (TDS/TDSM - Statistica Ordinanze Provvisorie Esecutive senza decisione del Collegio)
Nessun intervento strutturale a tabelle.
### Base Dati - REQ-SIE-009- 08 (Aggiornamento Statistica Movimento Provvedimenti per Oggetti)
Modificare la procedura stato_oggetti_sius presente nel package Oracle ISPETTORATO_SIUS.
### Base Dai - REQ-SIE-009- 09 (Modifica pagina Richiesta Atti Istruttori)
Per registrare il valore del nuovo campo previsto per il requisito in oggetto, nella tabella NOTIFICA, deve essere aggiunto un nuovo campo DATA_RESTITUZIONE_ATTO.
### Base Dati - REQ-SIE-009- 10 (Statistica Atti Istruttori con Data Restituzione)
Per censire la nuova funzione (Statistica Atti Istruttori) occorre registrare l’informazione sulle seguenti tabelle:
funzione
funzione_profilo
relazione_funzioni
### Base Dati - REQ-SIE-009-11 (UDS – TDS Integrazione Lista Mittente Atto)
Per censire la nuova voce da visualizzare nella combo box ‘mittente’, nella tabella cg_refs_code, deve essere aggiunto un nuovo valore per il dominio MITTENTE_ATTO.
### Base Dati - REQ-SIE-009-12 SIEP - ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’
Nessun intervento strutturale a tabelle.
### Base Dati - REQ-SIE-009-13 SIEP - ‘Ammissione Provvisoria misure alternative (art. 678 comma 1-ter c.p.p.) ’
Per la registrazione dei nuovi template da associare al contenuto introdotto per il requisito in oggetto, occorre prevedere dei record nella tabella template.
### Base Dati - REQ-SIE-009-14 SIEP – ‘Conferma Ammissione Provvisoria misure alternative (art. 678 comma 1-ter c.p.p.) ’
Aggiungere nuovi campi in tabella misura_alternativa per gestire i nuovi campi per anno e numero dell’ordinanza provvisoria.
Per la registrazione dei nuovi template da associare al contenuto introdotto per il requisito in oggetto, occorre prevedere dei record nella tabella template.
### Base Dati - REQ-SIE-009-15 SIEP - Aggiornamento della funzione di riepilogo ispettivo e Statistiche lavoro magistrati
Modificare la procedura Attivita_Magistrati e stat_provvedimenti presente nel package Oracle ISPETTORATO.
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