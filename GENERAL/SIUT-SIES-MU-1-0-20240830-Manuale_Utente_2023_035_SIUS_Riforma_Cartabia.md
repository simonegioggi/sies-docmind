---
uniqueName: siut-sies-mu-1-0-20240830-manualeutente2023035sius
displayName: "SIUT SIES MU 1 0 20240830 Manuale Utente 2023 035 SIUS Riforma Cartabia"
category: "GENERAL"
tags: []
---

# SIUT-SIES-MU-1.0-20240830-Manuale_Utente_2023_035_SIUS_Riforma_Cartabia

> **File originale:** `MEV/SCHEDA_035/ORIGINALI/SIUT-SIES-MU-1.0-20240830-Manuale_Utente_2023_035_SIUS_Riforma_Cartabia.docx`  
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
| Elaborato da | Vito Bufi - Umberto Mignogna |  |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 30/08/2024 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 30/08/2024 | Prima Emissione |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Aurora Garofalo | Amministrazione |  | Responsabile Unico Procedimento |
| Dott. Oris Orlando | Amministrazione |  | Direttore Esecutivo Contratto |
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
2	Descrizione Interventi	7
2.1	Procedimenti riferiti a contenuti che non richiedono esistenza procedimento E.P.S.	7
2.1.1	Applicazione Pene Sostitutive (art. 62 L. 689/81)	7
2.1.2	Programma di trattamento per semilibertà sostitutiva (art. 55 L. 689/81)	10
2.1.3	Revoca e Conversione pena pecuniaria sostitutiva per mancato pagamento	11
2.1.4	Sospensione esecuzione pene accessorie (UDS)	13
2.1.5	Conversione Pene Pecuniarie Principali per mancato pagamento	15
2.1.6	Rinvio dell’esecuzione pena sostitutiva (TDS)	18
2.1.7	Rinvio dell’esecuzione pena sostitutiva derivante da Conversione Pene Pecuniarie (TDS)	21
2.1.8	Sospensione esecuzione pene accessorie (TDS)	23
2.1.9	Reclamo avverso Revoca Pena Sostitutiva   (TDS)	24
2.2	Procedimenti riferiti a contenuti che richiedono esistenza procedimento E.P.S.	26
2.2.1	Esecuzione Pene Sostitutive	26
2.2.2	Sospensione Esecuzione Pene Sostitutive	37
2.2.3	Autorizzazione Pene Sostitutive	41
2.2.4	Modifica Modalità di esecuzione Pene Sostitutive	43
2.2.5	Revoca Autorizzazione/Modifica Prescrizioni Pene Sostitutive	45
2.2.6	Diffida al puntuale rispetto delle prescrizioni – pene sostitutive	47
2.2.7	Sospensione lavoro pubblica utilità sostitutivo	49
2.2.8	Rinvio dell’esecuzione pena sostitutiva (UDS)	51
2.2.9	Rinvio dell’esecuzione pena sostitutiva derivante da Conversione Pene Pecuniarie  (UDS)	53
2.2.10	Sopravvenienza nuovo Titolo esecutivo – Pene Sostitutive	55
2.2.11	Gestione Licenza – Pene Sostitutive	57
2.2.12	Licenza – pene sostitutive - Inosservanza prescrizioni (art. 69 L. 689/81)	59
2.2.13	Conversione pene pecuniarie irrogate dal Giudice di Pace	61
2.2.14	Rateizzazione pene pecuniarie	63
2.2.15	Revoca Pene Sostitutive (artt. 66, 108 L. 689/81)	65
2.2.16	Revoca Pene Sostitutive (art. 72 L. 689/81)	67
2.2.17	Revoca pena sostitutiva conseguente alla conversione p.p. per avvenuto pagamento	69
2.2.18	Gestione Licenze – Pene Sostitutive	70

Introduzione
Scopo del documento
In questo documento saranno descritti tutti gli interventi realizzati nel sottosistema SIUS per gestire  gli adeguamenti legislativi introdotti dalla riforma Cartabia e richiesti dall’Amministrazione con il documento Richiesta_scheda_2023-35_SIES_Cartabia_con_SIUS_signed.pdf.
Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF 1 | m_dg.DOG07AR.04_05_2023.0000747.U_ Richiesta_scheda_2023-35_SIES_Cartabia_con_SIUS_signed.pdf | Richiesta Scheda |
| RIF 2 | SIUT-SIE-SI-1.2-20240318_Specifiche_Intervento_MEV_2023_035_SIUS_Riforma_Cartabia.pdf | Scheda Intervento |

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

Descrizione Interventi
Per la gestione dei requisiti richiesti dall’Amministrazione sono stati inseriti nel sistema SIUS nuovi Contenuti, Oggetti ed Esiti, che consentono l’iscrizione di nuovi procedimenti utilizzando le stesse funzionalità già presenti nel sistema. Per la gestione dell’esecuzione delle pene sostitutive brevi, sulla falsa riga di quanto già avviene per l’esecuzione dei procedimenti di misura alternativa, sanzioni sostitutive e misure di sicurezza, è stata prevista la creazione di un procedimento “padre” (E.P.S.), all’interno del quale si aggregano tutti i procedimenti “figli”, relativi agli atti che possono essere richiesti nel corso della durata dell’esecuzione della pena sostitutiva.
Le tipologie di iscrizione dei procedimenti già presenti in SIUS (da presa in carico atti, da ricerca procedimento SIEP, da soggetto, da collegamento ad altro procedimento SIUS), valgono anche per i nuovi contenuti.
Di seguito saranno descritti i contenuti-oggetti-esiti aggiunti in SIUS, accorpandoli per procedimenti che non richiedono l’esistenza di un fascicolo padre di E.P.S. e per procedimenti che richiedono obbligatoriamente l’esistenza del suddetto fascicolo padre.
Procedimenti riferiti a contenuti che non richiedono esistenza procedimento E.P.S.
Applicazione Pene Sostitutive (art. 62 L. 689/81)
In relazione all’art. 62 L. 689/81 la riforma non parla più di Sanzioni sostitutive ma di Pene Sostitutive nelle form della Semilibertà sostitutiva e Detenzione Domiciliare sostitutiva, che possono essere applicate dal giudice in caso di condanna alla reclusione o all’arresto non superiori a quattro anni. Gli Uffici di Sorveglianza (UDS/UDSM) sono pertanto chiamati a pronunciarsi sull’applicabilità di tali pene sostitutive.
A tal fine per  la gestione di questo nuovo procedimento, nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), è stato aggiunto il contenuto
Applicazione Pene Sostitutive
Al nuovo contenuto sono associati i seguenti oggetti:
Semilibertà sostitutiva (art. 55 - 62 L. 689/1981)
Detenzione domiciliare sostitutiva (art. 56 - 62 L. 689/1981)
e i seguenti esiti
Determina le modalità di esecuzione
Dichiara N.D.P./ N.L.P.
Dichiara inammissibilità
Dispone restituzione atti al PM
Dichiara la propria incompetenza
L’aggiunta dei suddetti elementi permetterà all’Ufficio di poter iscrivere procedimenti di Applicazione Pene Sostitutive, collegandosi direttamente al procedimento SIEP o a seguito di presa in carico di Richiesta Applicazione Pene Sostitutive trasmesse dalle Procure.
Dopo aver proceduto ad iscrivere il nuovo procedimento, ad es. a seguito presa in carico della richiesta della Procura,




E’ possibile procedere alla definizione dello stesso emettendo l’ ordinanza, che presenterà i seguenti campi



Dopo la compilazione dei campi di interesse, a seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio



Da cui è possibile procedere alla stampa, alla modifica, alla cancellazione o alla validazione del provvedimento.
Per questo provvedimento sono previsti i seguenti modelli di stampa: SIUS_OR_APPLPENASOST.rtf, SIUS_OR_MODGENERICOAPPS.rtf.

In caso di esito di Determinazione delle modalità di Esecuzione, dopo aver validata e depositata l’ordinanza, l’ufficio provvede a trasmetterla all’ufficio che si occuperà dell’esecuzione della pena sostitutiva.

Programma di trattamento per semilibertà sostitutiva (art. 55 L. 689/81)
In caso di applicazione della semilibertà sostitutiva il semilibero è sottoposto ad un programma di trattamento predisposto dall’UEPE ed approvato dal giudice.
A tal fine per  la gestione di questo nuovo procedimento, nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), è stato aggiunto il contenuto:

Programma di trattamento per semilibertà sostitutiva (art. 55 L. 689/81)

Al nuovo contenuto sono associati i seguenti oggetti:
Approvazione programma di trattamento per semilibertà sostitutiva (art. 55 L. 689/81)
ed i seguenti esiti:
Approva
Restituisce programma
Restituisce programma con osservazioni
Dichiara N.D.P./ N.L.P.
Dichiara inammissibilità
Dichiara la propria incompetenza
Dopo aver proceduto ad iscrivere il nuovo procedimento, con una delle solite funzioni di iscrizione, il sistema presenterà la form di Dettaglio





E’ possibile procedere alla definizione dello stesso emettendo l’ ordinanza, che presenterà i seguenti campi


Oppure con Decreto



Dopo la compilazione dei campi di interesse, a seguito della Conferma, il sistema inserirà la nuova ordinanza o il nuovo decreto nella base dati e presenterà le rispettive form di Dettaglio, dalle quali è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
Per questo provvedimento sono previsti i seguenti modelli di stampa: SIUS_OR_PROGRTRATT.rtf,     SIUS_DE_ PROGRTRATT.rtf

Revoca e Conversione pena pecuniaria sostitutiva per mancato pagamento
L’art.  71 legge 689/1981 prevede che la pena pecuniaria sostitutiva non pagata possa essere convertita nella semilibertà, nella detenzione domiciliare sostitutiva ovvero nel lavoro di pubblica utilità sostitutivo.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), è stato inserito il contenuto:
Revoca e Conversione pena pecuniaria sostitutiva per mancato pagamento (art.71 L. 689/81)
Al nuovo contenuto sono associati i seguenti oggetti:
Revoca e Conversione pena pecuniaria sostitutiva per mancato pagamento (art.71 L. 689/81)
ed i seguenti esiti:
Revoca pena pecuniaria sostitutiva e converte in semilibertà sostitutiva
Revoca pena pecuniaria sostitutiva e converte in detenzione domiciliare sostitutiva
Revoca pena pecuniaria sostitutiva e converte in lavoro di pubblica utilità sostitutivo
Dichiara N.D.P./ N.L.P.
Dichiara inammissibilità
Dichiara la propria incompetenza
Questo tipo di procedimento non presuppone l’esistenza del fascicolo di Esecuzione Pena Sostitutiva, pertanto l’iscrizione, fuori uscendo dalla logica procedimenti “padre” – “figli”, avverrà utilizzando le attuali funzionalità di iscrizione previste in SIUS.

E’ possibile procedere alla definizione di questo procedimento emettendo un’ordinanza di Revoca e Conversione pene pecuniarie sostitutive per mancato pagamento, che presenta la seguente form


In cui l’importo non pagato è quello presente sul provvedimento di avviso mancato pagamento del procedimento SIEP collegato, e il quantum di pena pecuniaria da convertire non viene “precompilato”, ma deve essere digitato dall’utente, in quanto può non coincidere con la somma riportata in Importo non pagato.

Dopo la compilazione dei campi di interesse, a seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio,



dalla quale è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione

Per questo provvedimento sono previsti i seguenti modelli di stampa:  Ordinanza di revoca e conversione, Ordinanza generica.

Template: SIUS_OR_REVCONVPS.rtf, SIUS_OR_MODGENERICOUDS.rtf.

Sospensione esecuzione pene accessorie (UDS)
L’art.  51 quater O.P. (disciplina delle pene accessorie in caso di concessione di misure alternative) prevede  che l’Ufficio di Sorveglianza possa decidere la sospensione dell’esecuzione delle pene accessorie  in caso di misure alternative o di pene sostitutive.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:
Sospensione esecuzione pene accessorie (art. 51-quater O.P.)
Al nuovo contenuto vanno associati i seguenti oggetti:
Sospensione esecuzione pene accessorie – Misure alternative (art. 51-quater O.P.)
Sospensione esecuzione pene accessorie – Pene sostitutive (Art.  76 L. 689/81 – 51-quater O.P.)
ed i seguenti esiti:
Sospende
Non sospende
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza

Questo tipo di procedimento non presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva/Esecuzione Misura Alternativa, pertanto l’iscrizione, fuoriuscendo dalla logica procedimenti “padre” – “figli”, avverrà utilizzando le attuali funzionalità di iscrizione previste in SIUS.

E’ possibile procedere alla definizione di questo procedimento emettendo un’ordinanza di Sospensione Esecuzione pena accessorie, che presenta la seguente form


In cui nella combo box Tipo saranno presenti tutti i tipi di pena accessoria di cui all’art. 19 c.p., e quindi:
1) interdizione dai pubblici uffici;
2) interdizione da una professione o da un'arte;
3) interdizione legale;
4) incapacità di contrattare con la pubblica amministrazione;
4-bis) estinzione del rapporto di impiego o di lavoro;
5) decadenza o la sospensione dall'esercizio della responsabilità genitoriale;
6) sospensione dall'esercizio di una professione o di un'arte;
7) pubblicazione della sentenza penale di condanna
Per quel che concerne la durata della pena accessoria irrogata sarà presente la combo Tipo Durata in cui sarà possibile selezionare tra Perpetua e Durante la pena (per la quale bisognerà indicare la durata nei successivi campi).
A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio

dalla quale è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.

Al momento per questo provvedimento sono previsti due modelli di stampa: ordinanza di sospensione della pena accessoria, ordinanza generica.
Template: SIUS_OR_SOSPENSIONEPA.rtf, SIUS_OR_MODGENERICOUDS.rtf.

Conversione Pene Pecuniarie Principali per mancato pagamento
Gli artt. 102, 103 legge 689/1981 e art. 55 d. lgs. 274/00 prevedono che la pena pecuniaria non pagata possa essere convertita non più nella libertà controllata, bensì nella semilibertà e nella detenzione domiciliare sostitutive, oltre che nel lavoro di pubblica utilità.

Saranno disabilitati gli esiti inseriti precedentemente nel contenuto Conversione/Rateizzazione Pena Pecuniaria, in quanto per questi procedimenti è obbligatorio l’inserimento della Richiesta Conversione Pena Pecuniaria, con l’indicazione di tutti gli estremi (Anno/Numero Partiva IVA, Campione Penale, Autorità Richiedente, data irrevocabilità Titolo Esecutivo, etc.). Questi dati non sono necessari per la gestione dei procedimenti con Pena Pecuniaria sostitutiva in quanto la Procura si limiterà a trasferire l’importo di Pena Pecuniaria non pagato.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), è stato inserito il contenuto:
Conversione pene pecuniarie principali per mancato pagamento (artt. 102 - 103 L. 689/81 - 55 d. lgs. 274/00)
Al nuovo contenuto sono associati i seguenti oggetti:
Conversione pene pecuniarie principali per mancato pagamento (artt. 102 - 103 L. 689/81)
Conversione pene pecuniarie principali per mancato pagamento (art. 55 d. lgs. 274/00)
ed i seguenti esiti:
Dispone conversione in semilibertà sostitutiva
Dispone conversione in detenzione domiciliare sostitutiva
Dispone conversione in lavoro di pubblica utilità sostitutivo
Dispone conversione pena irrogata dal GdP in lavoro di pubblica utilità
Differisce la conversione
Dichiara NLP per irreperibilità – atti al PM
Dichiara NLP per accertata solvibilità
Dichiara NLP per intervenuta prescrizione
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza
Rateizza pagamento

Questo tipo di procedimento non presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione, fuoriuscendo dalla logica procedimenti “padre” – “figli”, avverrà utilizzando le attuali funzionalità di iscrizione previste in SIUS.

Per questo tipo di procedimento sarà implementata una nuova funzionalità, emissione ordinanza conversione pene pecuniarie sostitutive: la nuova maschera di inserimento, che non richiederà la presenza dei dati della Conversione, sarà implementata sulla base di quella abbozzata di seguito (fare riferimento al contenuto U070).

La nuova maschera si differenzierà in base all’esito del provvedimento, in caso di rateizzazione

In caso di Conversione

A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio



oppure

dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
Al momento per questo provvedimento saranno previsti tre modelli di stampa , che, quando generati, sono memorizzati in un campo BLOB della base dati: ordinanza di conversione pena pecuniaria, ordinanza di rateizzazione della pena pecuniaria, ordinanza generica.
Template: SIUS_OR_GENERICAPENASOST.rtf, SIUS_OR_RATEIZZAPENASOST.rtf, SIUS_OR_MODGENERICOPS.rtf.

Rinvio dell’esecuzione pena sostitutiva (TDS)

L’iscrizione di questo tipo di procedimento segue il normale flusso previsto per l’iscrizione di un qualsiasi procedimento del Tribunale di Sorveglianza.

Nell’ambito del Tribunale di Sorveglianza (TDS/TDSM), è stato aggiunto il contenuto:
Rinvio esecuzione Pena Sostitutiva Ex art. 684 comma 2 c.p.p.
Al nuovo contenuto sono associati i seguenti oggetti:
Differimento Pena Sostitutiva facoltativo art. 147 c.p. - art. 69 L. 689/81
Differimento facoltativo della Pena Sostitutiva in attesa di grazia – Art. 147 n. 1 c.p. - art. 69 L. 689/81
Differimento facoltativo della Pena Sostitutiva per grave infermità – Art. 147 n. 2 c.p. - art. 69 L. 689/81
Differimento facoltativo della Pena Sostitutiva per maternità – Art. 147 n. 3 c.p. - art. 69 L. 689/81
Differimento obbligatorio della Pena Sostitutiva nei confronti di donna incinta – Art. 146 n. 1 c.p. - art. 69 L. 689/81
Differimento obbligatorio della Pena Sostitutiva nei confronti di madre infante di età inferiore ad anni 1 – Art. 146 n. 2 c.p. - art. 69 L. 689/81
Differimento obbligatorio della Pena Sostitutiva nei confronti di persona affetta da malattia – Art. 146 n. 3 c.p. - art. 69 L. 689/81
Applicazione al semilibero della detenzione domiciliare sostitutiva – Art. 69 L. 689/81
ed i seguenti esiti:
Concede per un periodo
Rigetta
Ratifica il provvedimento del mds e concede per un periodo di
Ratifica il provvedimento del mds e rigetta
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza
E’ possibile procedere alla definizione di questo procedimento emettendo un’ordinanza Rinvio Esecuzione Pena sostitutiva, che presenta la seguente form



Dopo la compilazione dei campi di interesse, a seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio,



dalla quale è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione

Per questo provvedimento sono previsti i seguenti modelli di stampa:  Ordinanza generica, Ordinanza Rigetto generica, Ordinanza Rigetto Differimento della Pena

Template: SIUS_DE_MODGENERICO.rtf,  SIUS_OR_RIGETTOGENERICO.rtf, SIUS_OR_RIGETTODIFPENAPS.rtf

Rinvio dell’esecuzione pena sostitutiva derivante da Conversione Pene Pecuniarie (TDS)
L’iscrizione di questo tipo di procedimento segue il normale flusso previsto per l’iscrizione di un qualsiasi procedimento del Tribunale di Sorveglianza.

Nell’ambito del Tribunale di Sorveglianza (TDS/TDSM), è stato aggiunto il contenuto:
Rinvio dell’Esecuzione Pena Sostitutiva derivante da Conversione - artt. 69 – 107 L. 689/81”
Al nuovo contenuto sono associati i seguenti oggetti:
Differimento facoltativo della Pena Sostitutiva derivante da conversione in attesa di grazia – Art. 147 n. 1 c.p. - artt. 69 – 107 L. 689/81
Differimento facoltativo della Pena Sostitutiva derivante da conversione per grave infermità – Art. 147 n. 2 c.p. - artt. 69 – 107 L. 689/81
Differimento facoltativo della Pena Sostitutiva derivante da conversione per maternità – Art. 147 n. 3 c.p. - artt. 69 – 107 L. 689/81
Differimento obbligatorio della Pena Sostitutiva derivante da conversione nei confronti di donna incinta – Art. 146 n. 1 c.p. - artt. 69 – 107 L. 689/81
Differimento obbligatorio della Pena Sostitutiva derivante da conversione nei confronti di madre infante di età inferiore ad anni 1 – Art. 146 n. 2 c.p. - artt. 69 – 107 L. 689/81
Differimento obbligatorio della Pena Sostitutiva derivante da conversione nei confronti di persona affetta da malattia – Art. 146 n. 3 c.p. - artt. 69 – 107 L. 689/81
Applicazione al detenuto sottoposto alla Semilibertà Sostitutiva derivante da Conversione della Detenzione Domiciliare Sostitutiva - artt. 69 – 107 L. 689/81
ed i seguenti esiti:
Concede per un periodo
Proroga per un periodo
Rigetta
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza
E’ possibile procedere alla definizione di questo procedimento emettendo un  decreto Rinvio Esecuzione Pena sostitutiva, che presenta la seguente form



A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio



dalla quale è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.

Al momento per questo provvedimento saranno previsti due modelli di stampa: Ordinanza di rinvio esecuzione pena, Ordinanza generica
Template: SIUS_OR_RINVIOESECPSTDS.rtf, SIUS_OR_MODGENERICO.rtf

Sospensione esecuzione pene accessorie (TDS)
L’art.  51 quater O.P. (disciplina delle pene accessorie in caso di concessione di misure alternative) prevede la sospensione dell’esecuzione delle pene accessorie  in caso di misure alternative possa essere decisa anche dal Tribunale di Sorveglianza.
Nell’ambito dell’Ufficio di Sorveglianza (TDS/TDSM), il contenuto da integrare è il seguente:
Sospensione esecuzione pene accessorie (art. 51-quater O.P.)  (C066)
Al nuovo contenuto vanno associati i seguenti oggetti:
Sospensione esecuzione pene accessorie – Misure alternative (art. 51-quater O.P.)   (9090)
ed i seguenti esiti:
Sospende   (0136)
Non sospende   (0078)
Dichiara N.D.P./ N.L.P   (0004)
Dichiara inammissibilità   (0003)
Dichiara la propria incompetenza  (0005)

Questo tipo di procedimento non presuppone l’esistenza del fascicolo “padre” di Esecuzione Misura Alternativa, pertanto l’iscrizione, fuoriuscendo dalla logica procedimenti “padre” – “figli”, avverrà utilizzando le attuali funzionalità di iscrizione previste in SIUS.

E’ possibile procedere alla definizione di questo procedimento emettendo un’ordinanza di Sospensione Esecuzione pena accessorie, che presenta la seguente form


A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio

dalla quale è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
Al momento per questo provvedimento sono previsti due modelli di stampa: ordinanza di sospensione della pena accessoria, ordinanza generica
Template: SIUS_OR_SOSPENSIONEPA-TDS.rtf, SIUS_OR_MODGENERICO.rtf
Reclamo avverso Revoca Pena Sostitutiva   (TDS)
L’ordinanza di revoca può essere impugnata dinanzi al TDS. Di conseguenza occorre inserire lato TDS un nuovo contenuto/oggetto, denominato “Reclamo avverso Revoca Pene Sostitutive” ed i cui esiti potrebbero essere: Accoglie reclamo; Accoglie reclamo e converte in altra pena sostitutiva; Rigetta; NLP; Inammissibilità; Incompetenza, utilizzando una maschera con alcuni dei dati particolari previsti in quella dell’UDS, vale a dire “Pena sostitutiva più grave” e “Rideterminazione quantum pena da espiare”
Nell’ambito dell’Ufficio di Sorveglianza (TDS/TDSM), è stato aggiunto il contenuto:
Reclamo avverso Revoca Pena Sostitutiva
Al nuovo contenuto vanno associati i seguenti oggetti:
Reclamo avverso Revoca Pena Sostitutiva
ed i seguenti esiti:
Accoglie reclamo
Accoglie reclamo e converte in altra pena sostitutiva
Convoca
Rigetta
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza
E’ possibile procedere alla definizione di questo procedimento emettendo un’ordinanza Reclamo avverso Revoca Pena Sostitutiva, che presenta la seguente form


In cui nella combo box Pena Sostitutiva più grave il sistema presenterà le 3 pene sostitutive previste per il procedimento di esecuzione.

A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio

dalla quale è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.

Sono previsti 3 modelli di stampa: Ordinanza Generica, ordinanza di accoglimento reclamo, ordinanza di rigetto reclamo
Template: SIUS_OR_ACCRECLREVPS.rtf, SIUS_OR_RIGRECLREVPS.rtf, SIUS_OR_MODGENERICO.rtf.

Procedimenti riferiti a contenuti che richiedono esistenza procedimento E.P.S.
Esecuzione Pene Sostitutive
Dopo che il Magistrato di Sorveglianza ha determinato le modalità di esecuzione della pena sostitutiva invia l’ordinanza all’Ufficio di Sorveglianza competente per l’esecuzione della pena sostitutiva. L’Ufficio iscrive un fascicolo che farà da collettore per tutti i procedimenti che si apriranno durante l’esecuzione ad essa attinenti. Questa tipologia di procedimento, come già fatto per l’esecuzione delle misure alternative, delle misure di sicurezza e delle sanzioni sostitutive, sarà identificato comunemente come “Fascicolo padre”, mentre tutti i procedimenti relativi ad atti relativi alla fase di esecuzione, che saranno caratterizzati da una doppia numerazione il numero identificativo del procedimento e il numero del fascicolo di Esecuzione Pene Sostitutive, saranno identificati comunemente come “Fascicoli Figli”.

Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM) è stato aggiunto il contenuto:

Esecuzione Pene Sostitutive
Al nuovo contenuto sono associati i seguenti oggetti:
Semilibertà sostitutiva (art. 55 - 62 L. 689/1981)
Detenzione domiciliare sostitutiva (art. 56 - 62 L. 689/1981)
Lavoro di pubblica utilità sostitutivo (art. 56 bis L. 689/1981 – 55 DL 274/20)
Permanenza Domiciliare
Per questo tipo di procedimento non sono previsti esiti.

Per questo procedimento, come negli altri casi di procedimenti di Esecuzione, il sistema presenterà la seguente form



che in caso di iscrizione da presa in carico dell’ordinanza di applicazione presenterà già precompilati i campi Tipo Atto, Data atto, Mittente, Sede Mittente, Anno e Numero Ordinanza.
La form simile, ma priva di dati precompilati, si presenterà anche in caso di iscrizione da Procedimento SIEP, iscrizione da Soggetto e Iscrizione Procedimento Collegato.

A seguito della Conferma il sistema inserirà un fascicolo “padre” di esecuzione pene sostitutive e presenterà la seguente form di dettaglio dalla quale è possibile attivare le azioni di Modifica e Stampa.





Da questa form cliccando su Anno e Numero Esecuzione Pena Sostitutiva si riceverà la seguente form:

da cui è possibile proseguire con l’inserimento di un nuovo procedimento figlio o con la modifica dei dati relativi alla durata ed al luogo di esecuzione della pena sostitutiva oppure con la consultazione dei periodi di inizio, sospensione e ripresa della pena sostitutiva (link ). Il completamento di tali dati avviene successivamente all’iscrizione del procedimento, quando l’ufficio riceve le ulteriori informazioni.

Selezionando l’azione di Modifica  si riceverà la seguente form



In cui è possibile aggiornare i dati del periodo e del Luogo esecuzione della Pena sostitutiva.
Dalla form   , selezionando l’azione di Inserimento  si riceverà la form che consente l’iscrizione di tutti i procedimenti “figli”, cioè relativi a contenuti, che presuppongono l’esistenza di un procedimento di E.P.S.


La form è già precompilata con l’Anno e Progressivo e con il Magistrato assegnatario del procedimento del procedimento di EPS.
Nella combo box Contenuto il sistema presenta tutti i nuovi contenuti relativi a procedimenti che possono aprirsi nel corso della durata dell’esecuzione della pena sostitutiva


Dal Dettaglio del procedimento di EPS è possibile attivare altre due funzionalità specifiche di questo tipo di procedimento: Inizio/Ripresa Pena Sostitutiva e Annotazione Data Inizio Sospensione, presenti nella tool bar delle funzioni.

#### Inizio/Ripresa Pena Sostitutiva
La funzione permette di acquisire la data di inizio della Pena Sostitutiva o la data di Ripresa, al termine di un periodo di sospensione.


Selezionandola si riceverà la seguente form

In cui l’utente dovrà obbligatoriamente digitare la data inizio esecuzione e l’autorità che ha inviato il verbale e Confermare. Il sistema in base ai dati a sistema calcolerà la data di Fine Pena e presenterà la form per la Validazione della data, che l’utente può eventualmente modificare


A seguito della validazione il sistema presenterà la form di Dettaglio

da cui è possibile eventualmente procedere alla cancellazione della data inizio.


#### Annotazione Data Inizio Sospensione
La data di inizio sospensione delle Pena Sostitutiva dovrebbe essere di norma inserita nel sistema a seguito di un provvedimento di sospensione. La funzione permette di acquisire la data di inizio Sospensione della Pena Sostitutiva, in assenza del suddetto provvedimento.

Selezionandola si riceverà la seguente form

In cui l’utente dovrà obbligatoriamente digitare la data inizio sospensione, la durata, indicare se il periodo della sospensione e da recuperare o meno ai fini del calcolo del fine pena, l’autorità che ha concesso la sospensione e Confermare. Il sistema in base ai dati a sistema calcolerà la data di Fine Sospensione Pena e presenterà la form di Dettaglio.

Da cui è possibile procedere alla cancellazione.
Le date di inizio/ripresa della pena sostitutiva e le date di sospensione sono visibili dai Link , presente nella form di Dettaglio E.P.S., e , presente nelle form di Inizio/Ripresa e Annotazione Data Sospensione


#### Gestione procedimenti Esecuzione Pene Sostitutive
Per la gestione dei nuovi procedimenti di Esecuzione Pene Sostitutive viene aggiunta nel menu verticale di SIUS per gli uffici UDS/UDSM una nuova voce

Selezionandola il sistema presenta un menu orizzontale

Con due tipologie di ricerca: per estremi procedimento e per soggetto.

Ricerca Procedimento di Esecuzione Pene Sostitutive

La funzione presenta la seguente form



Dalla quale è possibile effettuare una ricerca del singolo procedimento e un range di procedimenti di E.P.S.

In caso di ricerca puntuale, se il procedimento non è di E.P.S. si riceverà il seguente messaggio



Se il procedimento è di E.P.S. si riceverà la form di Dettaglio Procedimento.

In caso di ricerca per range di procedimenti, il sistema invierà la form con l’Elenco dei procedimenti di EPS compresi tra Anno e Numero Iniziale e Anno e Numero Finale



Ricerca Procedimento di Esecuzione Pene Sostitutive per Soggetto
La funzione ricerca i procedimenti E.P.S a carico di un soggetto e presenta la seguente form


N.B. Il funzionamento dei filtri aggiuntivi impostabili nella form, è identico a quello della funzione Ricerca procedimenti di Esecuzione Sanzione Sostitutiva, già presente in SIUS da diverso tempo.

L’utente digita, ad es., le iniziali del cognome e avvia la ricerca, il sistema invia la form con i dati del soggetto e il numero di procedimenti di E.P.S. a suo carico



Da questa form, cliccando sull’icona di Dettaglio, si riceve l’Elenco Dettagliato dei procedimenti



Sospensione Esecuzione Pene Sostitutive
L’art. 660 c.p.p.	 al comma 15 prevede di richiedere la sospensione dell’esecuzione della pena sostitutiva nel caso che il soggetto chieda l’ammissione al pagamento rateale dopo l’inizio dell’esecuzione, d’altra parte l’art. 68 L. 689/81 prevede la Sospensione pena sostitutiva per sopravvenienza misura di sicurezza detentiva (art. 68  L.  689/81), la Sospensione pena sostitutiva per sopravvenienza pena detentiva (art.  68 L. 689/81).
A tal fine per la gestione di questo nuovo procedimento, nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), è stato aggiunto il contenuto:
Sospensione Esecuzione Pene Sostitutive
Al nuovo contenuto sono associati i seguenti oggetti:
Sospensione pena sostituiva per ammissione al pagamento rateale (art.660 c.15 c.p.p.)
Sospensione pena sostituiva per sopravvenienza misura di sicurezza detentiva (art. 68 L. 689/1981)
Sospensione pena sostituiva per sopravvenienza pena detentiva (art. 68 L. 689/1981)
ed i seguenti esiti:
Sospende
Non sospende
Dichiara N.D.P./ N.L.P.
Dichiara inammissibilità
Dichiara la propria incompetenza
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS



A seguito della compilazione della form e successiva Conferma, il sistema presenterà la form di Dettaglio del procedimento “figlio” del procedimento di esecuzione pena sostitutiva


Caratterizzata da un proprio Anno e Numero e dal numero del procedimento padre (EPS).

E’ possibile procedere alla definizione di questo procedimento emettendo l’ordinanza o il decreto, che presentano rispettivamente le seguente form





Dopo la compilazione dei campi di interesse, a seguito della Conferma il sistema effettuerà il salvataggio dei dati nella base dati e presenterà la form di Dettaglio





Da cui è possibile procedere alla stampa, alla modifica, alla cancellazione o alla validazione del provvedimento.

Per questi provvedimenti sono previsti i seguenti modelli di stampa: Ordinanza Sospensione per pena detentiva, Ordinanza generica, Decreto Sospensione per pena detentiva, Decreto generico.

TEMPLATE: SIUS_OR_SOSPPSPENADET.rtf, SIUS_OR_MODGENERICOPS.rtf, SIUS_DE_SOSPPSPENADET.rtf, SIUS_DE_MODGENERICOPS.rtf

L’ordinanza o il decreto seguiranno il normale percorso di altri provvedimenti, verranno validati, quindi depositati e validati per essere trasmessi allo stesso Ufficio o ad altro ufficio.

I dati relativi alla decorrenza e alla durata della sospensione sono riportati nella funzione Elenco Periodi Pena Sostitutiva, in maniera alternativa all’inserimento manuale, come descritto al precedente par. 2.2.1.3.
Autorizzazione Pene Sostitutive
L’art. 64 e seguenti legge 689/1981 (vedi anche art. 107 L. 689/81) prevede di richiedere delle Autorizzazioni nel corso dell’esecuzione della pena sostitutiva.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM),è stato aggiunto il contenuto:
Autorizzazione Pene Sostitutive
Al nuovo contenuto sono associati i seguenti oggetti:
Autorizzazione Pene Sostitutive
Ulteriore autorizzazione Pene Sostitutive
ed i seguenti esiti:
Autorizza
Non autorizza
Dichiara N.D.P./ N.L.P.
Dichiara inammissibilità
Dichiara la propria incompetenza
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 2.2.2, tranne per il contenuto e oggetto.
E’ possibile procedere alla definizione di questo procedimento emettendo un decreto autorizzazione su pena sostitutiva che presenta la seguente form



Dopo la compilazione dei campi di interesse, a seguito della Conferma del decreto, il sistema effettuerà il salvataggio dei dati nella base dati e presenterà la form di Dettaglio



dalla quale è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.

Per questo provvedimento sono previsti tre modelli di stampa: Decreto Autorizzazione generico, Decreto Autorizzazione fuori sede, Decreto Autorizzazione Uso Patente.
TEMPLATE: SIUS_DE_AUTORIZZAGENERICOPS.rtf, SIUS_DE_AUTORIZZAUSOPATENTEPS.rtf, SIUS_DE_AUTORIZZAFUORISEDEPS.rtf.

Modifica Modalità di esecuzione Pene Sostitutive
L’art. 64 e seguenti legge 689/1981 (vedi anche art. 107 L. 689/81)  prevede di richiedere la Modifica delle modalità di esecuzione nel corso dell’esecuzione della pena sostitutiva.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM) è stato aggiunto il contenuto:
Modifica modalità di esecuzione/luogo esecuzione pene sostitutive (art. 64 L. 689/81)
Al nuovo contenuto sono associati i seguenti oggetti:
Modifica modalità esecuzione semilibertà sostitutiva (art.  64  L.  689/81)
Modifica luogo esecuzione semilibertà sostitutiva (art.  64  L.  689/81)
Modifica modalità esecuzione detenzione   domiciliare sostitutiva (art.  64  L.  689/81)
Modifica luogo esecuzione detenzione   domiciliare sostitutiva (art.  64  L.  689/81)
ed i seguenti esiti:
Modifica permanente prescrizioni
Modifica provvisoria prescrizioni
Modifica luogo esecuzione
Rigetta
Dichiara N.D.P./ N.L.P.
Dichiara inammissibilità
Dichiara la propria incompetenza
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 2.2.2, tranne per il contenuto e oggetto.
E’ possibile procedere alla definizione di questo procedimento emettendo un decreto di
Modifica Modalità esecuzione/Luogo esecuzione pene sostitutive, che presenta la seguente form


Dopo aver compilato i campi di interesse, a seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio, dalla quale è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione



Per questo provvedimento sono previsti i seguenti modelli di stampa: Decreto Modifica Modalità esecuzione, Decreto Modifica Luogo Esecuzione per Semilibero, Decreto Modifica Luogo Esecuzione per Detenuto Domiciliare, Decreto Generico.

TEMPLATE : SIUS_DE_MODPRESCPERMPS.rtf, SIUS_DE_MODPRESCRPS.rtf, SIUS_DE_MODLUOESECSL.rtf, SIUS_DE_MODLUOESEDDPS.rtf

Revoca Autorizzazione/Modifica Prescrizioni Pene Sostitutive
L’art. 64 e seguenti legge 689/1981 (vedi anche art. 107 L. 689/81) prevede che possa essere richiesta la Revoca dell’autorizzazione o della modifica delle prescrizioni, concesse precedentemente, nel corso dell’esecuzione della pena sostitutiva.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM) è stato aggiunto il contenuto:
Revoca autorizzazione/Modifica Prescrizioni pene sostitutive
Al nuovo contenuto sono associati i seguenti oggetti:
Revoca autorizzazione pene sostitutive
Revoca Modifica Prescrizioni pene sostitutive
ed i seguenti esiti:
Revoca
Non revoca
Rigetta
Dichiara N.D.P./ N.L.P.
Dichiara inammissibilità
Dichiara la propria incompetenza
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 2.2.2, tranne per il contenuto e oggetto.
E’ possibile procedere alla definizione di questo procedimento emettendo una ordinanza o un  decreto di
Revoca autorizzazione/Modifica Prescrizioni pene sostitutive, che presentano rispettivamente le seguenti form





Dopo la compilazione dei campi di interesse, a seguito della Conferma il sistema inserirà la nuova ordinanza o il nuovo decreto nella base dati e presenterà le rispettive form di Dettaglio





dalle quali è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
Per questi provvedimenti sono previsti i seguenti modelli di stampa: Ordinanza Generica, Decreto Generico.

TEMPLATE : SIUS_OR_MODGENERICOUDS.rtf, SIUS_DE_MODGENERICO.rtf

Diffida al puntuale rispetto delle prescrizioni – pene sostitutive
Considerato che l’istituto delle pene sostitutive dovrebbe avere una ampia diffusione, è opportuno inserire anche un contenuto specifico per la diffida, sulla falsariga di quanto accade nel caso di EMA.

Considerato che l’istituto delle pene sostitutive dovrebbe avere una ampia diffusione, è opportuno inserire anche un contenuto specifico per la diffida.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM) è stato aggiunto il contenuto:
Diffida al puntuale rispetto delle prescrizioni - pene sostitutive
Al nuovo contenuto sono associati i seguenti oggetti:
Convocazione per puntuale rispetto prescrizioni – pene sostitutive
Diffida al puntuale rispetto prescrizioni – pene sostitutive
ed i seguenti esiti:
Diffida
Non Diffida
Convoca
Non Convoca
Dichiara N.D.P./ N.L.P.
Dichiara inammissibilità
Dichiara la propria incompetenza
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 2.2.2, tranne per il contenuto e oggetto.
E’ possibile procedere alla definizione di questo procedimento emettendo un  decreto di Diffida al puntuale rispetto delle Prescrizioni pene sostitutive, che presenta la seguente form



Dopo la compilazione dei campi di interesse, a seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio,



dalla quale è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione

Per questo provvedimento sono previsti i seguenti modelli di stampa:  Decreto generico, Decreto diffida puntuale rispetto prescrizioni.

Template: SIUS_DE_DIFFIDARISPPRESCRPS.rtf, SIUS_DE_MODGENERICO.rtf

Sospensione lavoro pubblica utilità sostitutivo
L’art.  69 legge 689/1981, al secondo comma, prevede l’applicazione di una particolare forma di sospensione relativa esclusivamente al lavoro di pubblica utilità.

Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), è stato aggiunto il contenuto:
Sospensione lavoro di pubblica utilità sostitutivo (art. 69 c. 2 L. 689/81)
Al nuovo contenuto sono associati i seguenti oggetti:
Sospensione lavoro di pubblica utilità sostitutivo (art. 69 c. 2 L. 689/81)
ed i seguenti esiti:
Sospende
Non sospende
Dichiara N.D.P./ N.L.P.
Dichiara inammissibilità
Dichiara la propria incompetenza
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 2.2.2, tranne per il contenuto e oggetto.
E’ possibile procedere alla definizione di questo procedimento emettendo un  decreto Sospensione lavoro pubblica utilità sostitutivo, che presenta la seguente form



Dopo la compilazione dei campi di interesse, a seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio,



dalla quale è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione

Per questo provvedimento sono previsti i seguenti modelli di stampa:  Decreto generico, Decreto sospensione lavoro pubblica utilità.

Template: SIUS_DE_SOSPPSLAVPU.rtf, SIUS_DE_MODGENERICOPS.rtf

Rinvio dell’esecuzione pena sostitutiva (UDS)
Anche per le pene sostitutive si applica la disciplina prevista dall’art. 684 c.p.p. e, quindi, quella della decisione provvisoria del MdS e del successivo passaggio al TdS.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), è stato aggiuntovil contenuto:
Rinvio esecuzione Pena Sostitutiva Ex art. 684 comma 2 c.p.p.
Al nuovo contenuto vanno associati i seguenti oggetti:
Differimento Pena Sostitutiva facoltativo art. 147 c.p. - art. 69 L. 689/81
Differimento Pena Sostitutiva obbligatorio art. 146 c.p. - art. 69 L. 689/81
Applicazione al semilibero della detenzione domiciliare sostitutiva – Art. 69 L. 689/81
ed i seguenti esiti:
Concede
Rigetta
Rinvia Esecuzione Nelle Forme della Detenzione Domiciliare
Dichiara N.D.P./ N.L.P.
Dichiara inammissibilità
Dichiara la propria incompetenza
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 2.2.2, tranne per il contenuto e oggetto.

E’ possibile procedere alla definizione di questo procedimento emettendo un  decreto Rinvio Esecuzione Pena sostitutiva, che presenta la seguente form



Dopo la compilazione dei campi di interesse, a seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio,



dalla quale è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione

Per questo provvedimento sono previsti i seguenti modelli di stampa:  Decreto generico, Decreto Rinvio Esecuzione Pena Sostitutiva

Template: SIUS_DE_MODGENERICOPS.rtf, SIUS_DE_RINVIOESECPENAPS.rtf


Rinvio dell’esecuzione pena sostitutiva derivante da Conversione Pene Pecuniarie  (UDS)
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), è stato aggiunto il contenuto:
Rinvio esecuzione Pena Sostitutiva derivante da Conversione - artt. 69 – 107 L. 689/81
Al nuovo contenuto vanno associati i seguenti oggetti:
Differimento Obbligatorio Pena Sostitutiva derivante da Conversione - artt. 69 – 107 L. 689/81
Differimento Facoltativo Pena Sostitutiva derivante da Conversione - artt. 69 – 107 L. 689/81
Applicazione al detenuto sottoposto alla Semilibertà Sostitutiva derivante da Conversione della Detenzione Domiciliare Sostitutiva - artt. 69 – 107 L. 689/81
ed i seguenti esiti:
Concede
Proroga
Rigetta
Dichiara N.D.P./ N.L.P.
Dichiara inammissibilità
Dichiara la propria incompetenza
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 2.2.2, tranne per il contenuto e oggetto.

E’ possibile procedere alla definizione di questo procedimento emettendo un  decreto Rinvio Esecuzione Pena sostitutiva derivante da Conversione Pene Pecuniarie , che presenta la seguente form



Dopo la compilazione dei campi di interesse, a seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio,



dalla quale è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione

Per questo provvedimento sono previsti i seguenti modelli di stampa:  Decreto generico, Decreto Rinvio esecuzione pena a seguito conversione

Template: SIUS_DE_MODGENERICOPS.rtf, SIUS_DE_RINVIOESECPENAPSDC.rtf


Sopravvenienza nuovo Titolo esecutivo – Pene Sostitutive
L’art. 76 legge 689/1981 prevede che la sussistenza dei requisiti dell’applicazione della pena sostitutiva vengano rivalutati dal magistrato in presenza di nuovi titoli esecutivi.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), è stato aggiunto il contenuto:
Sopravvenienza nuovo titolo - Pene sostitutive (art. 76 L. 689/81 – 51-bis O.P.)
Al nuovo contenuto sono associati i seguenti oggetti:
Valutazione su permanenza  quantum  pena  per  semilibertà  sostitutiva  (Art.  55  L. 689/81 – 51-bis O.P.)
Valutazione su permanenza quantum pena per detenzione domiciliare  sostitutiva  (Art.  56  L. 689/81 – 51-bis O.P.)
Valutazione su permanenza quantum pena per lavoro di pubblica utilità (Art.  56 bis L. 689/81 – 51-bis O.P.)
ed i seguenti esiti:
Estende la pena sostitutiva
Dischiara inefficace/cessata la pena sostitutiva
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 2.2.2, tranne per il contenuto e oggetto.

E’ possibile procedere alla definizione di questo procedimento emettendo l’ordinanza o il decreto, che presentano rispettivamente le seguente form

Oppure


A seguito della Conferma il sistema inserirà la nuova ordinanza o il nuovo decreto nella base dati e presenterà le rispettive form di Dettaglio



Oppure


dalle quali sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione, sia per il decreto che per l’ordinanza.

Al momento per questi provvedimento saranno previsti sei modelli di stampa: ordinanza di estensione della pena, ordinanza di cessazione della pena, ordinanza generica, decreto di estensione della pena, decreto di cessazione della pena, decreto generico.

Template: SIUS_OR_PROSPROVPS.rtf, SIUS_OR_SOSPPROVPS.rtf, SIUS_OR_MODGENERICOUDS.rtf, SIUS_DE_PROSPROVPS.rtf, SIUS_DE_SOSPPROVPS.rtf,	 SIUS_DE_MODGENERICO.rtf.




Gestione Licenza – Pene Sostitutive
L’art.  69 legge 689/1981, al primo comma, prevede un istituto parzialmente nuovo le licenze per i soggetti sottoposti a pene sostitutive.

Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), è stato inserito il contenuto:
Licenza - pene sostitutive (art. 69 L. 689/81)
Al nuovo contenuto sono associati i seguenti oggetti:
Licenza - pene sostitutive (art. 69 L. 689/81)
ed i seguenti esiti:
Concede
Rigetta
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 2.2.2, tranne per il contenuto e oggetto.

E’ possibile procedere alla definizione di questo procedimento emettendo un  decreto Licenza Pena sostitutiva, che presenta la seguente form


A seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio



dalla quale è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione

Per questo decreto sono previsti quattro modelli di stampa: Decreto generico, Decreto concessione licenza, Decreto Rigetto licenza, Decreto Inammissibilità licenza.

Template: SIUS_DE_CONCLICPS.rtf, SIUS_DE_INAMMLICPS.rtf, SIUS_DE_RIGETTOLICPS.rtf, SIUS_DE_MODGENERICO.rtf

Licenza – pene sostitutive - Inosservanza prescrizioni (art. 69 L. 689/81)
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), è stato aggiunto il contenuto:
Licenza - pene sostitutive – inosservanza prescrizioni (art. 69 L. 689/81)
Al nuovo contenuto sono associati i seguenti oggetti:
Valutazione revoca licenza – pene sostitutive (Art. 53 bis O.P. – 69 L. 689/81
Esclusione computo Licenza – pene sostitutive (artt. 53 bis O.P. - 69 L. 689/81)
ed i seguenti esiti:
Revoca
Non Revoca
Dichiara validamente espiata la pena
Dichiara non validamente espiata la pena
Dichiara N.D.P./ N.L.P

Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 2.2.2, tranne per il contenuto e oggetto.

E’ possibile procedere alla definizione di questo procedimento emettendo un  decreto Esclusione Computo Pene Sostitutive, che presenta la seguente form



A seguito della Conferma, il sistema inserirà il nuovo decreto nella base dati e presenterà la form di Dettaglio



dalla quale è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.

Al momento per questo provvedimento saranno previsti due modelli di stampa: Decreto revoca licenza, Decreto scomputo licenza.

Template: SIUS_DE_SCOMPUTOLICPS.rtf, SIUS_DE_REVOCALICPS.rtf.

Conversione pene pecuniarie irrogate dal Giudice di Pace

L’art.  55 D.L. 274/2000 prevede che a richiesta del condannato la pena pecuniaria può essere convertita in lavoro di pubblica utilità, In caso di violazione degli obblighi del lavoro di pubblica utilità, la parte residua si converte in obbligo di permanenza domiciliare.

Premessa alla gestione di questo nuovo contenuto è l’inserimento fra gli oggetti del fascicolo padre di ESS di un nuovo oggetto:
Lavoro di pubblica utilità
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), è stato aggiunto il contenuto:
Violazione obblighi lavoro pubblica utilità (art. 55 c. 3 DL 274/2000)
Al nuovo contenuto è associato il seguente oggetto:
Violazione obblighi lavoro pubblica utilità (art. 55 c. 3 DL 274/2000)
ed i seguenti esiti:
Converte pena pecuniaria in permanenza domiciliare
Non converte
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 2.2.2, tranne per il contenuto e oggetto.

E’ possibile procedere alla definizione di questo procedimento emettendo una ordinanza  Conversione Pene Pecuniarie irrogare dal GdP, che presenta la seguente form



A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio



dalla quale è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.

Al momento per questo provvedimento sono previsti due modelli di stampa: ordinanza di conversione pena sostitutiva, ordinanza generica.

Template: SIUS_OR_MODGENERICOPS.rtf, SIUS_OR_GENERICAPENASOST.rtf.

La conversione di cui sopra determina come effetto diretto quello di iscrivere un procedimento di ESS relativa a  Permanenza domiciliare.

Rateizzazione pene pecuniarie
Considerato che (a quanto pare) la rateizzazione potrà essere concessa dal Magistrato di Sorveglianza solo in corso di esecuzione (o, quanto meno, prima dell’inizio ma sempre successivamente all’emissione del provvedimento di conversione), quindi dopo l’iscrizione di un procedimento di EPS.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), è stato aggiunto il contenuto:
Rateizzazione pena pecuniaria
Al nuovo contenuto è associato il seguente oggetto:
Rateizzazione pena pecuniaria
ed i seguenti esiti:
Rateizza pagamento
Rigetta
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 2.2.2, tranne per il contenuto e oggetto.

E’ possibile procedere alla definizione di questo procedimento emettendo una ordinanza  Rateizzazione Pene Pecuniarie, che presenta la seguente form



A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio



dalla quale è possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.

Al momento per questo provvedimento sono previsti due modelli di stampa: ordinanza di rateizzazione, ordinanza generica.

Template: SIUS_OR_MODGENERICOPS.rtf, SIUS_OR_RATEIZZAPENASOST.rtf.



Revoca Pene Sostitutive (artt. 66, 108 L. 689/81)
Gli artt. 66 - 108 legge 689/1981 prevedono un istituto parzialmente nuovo, in quanto in precedenza il Magistrato di Sorveglianza si limitava a sospendere l’esecuzione delle sanzioni sostitutive e trasmetteva gli atti al TDS (o trasmetteva al TDS senza sospendere), mentre ora è il Magistrato di Sorveglianza a disporre la revoca/sostituzione delle pene sostitutive, non più con decreto ma con ordinanza.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), è stato aggiunto il contenuto:
Revoca pena sostitutiva per inosservanza delle prescrizioni (art. 66, 108 L. 689/81)
Al nuovo contenuto sono associati i seguenti oggetti:
Revoca detenzione domiciliare sostitutiva per inosservanza prescrizioni (art. 66 L. 689/81)
Revoca semilibertà sostitutiva per inosservanza prescrizioni (art. 66 L. 689/81)
Revoca detenzione domiciliare sostitutiva derivante da conversione per inosservanza prescrizioni (art. 108 L. 689/81)
Revoca semilibertà sostitutiva derivante da conversione per inosservanza prescrizioni (art. 108 L. 689/81)
ed i seguenti esiti:
Revoca e converte in pena detentiva
Revoca e converte in altra pena sostitutiva
Non Revoca
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 2.2.2, tranne per il contenuto e oggetto.

E’ possibile procedere alla definizione di questo procedimento emettendo una ordinanza  Revoca Pena Sostitutiva, che presenta la seguente form



In cui nella combo box Pena Sostitutiva più grave il sistema presenterà le tre pene sostitutive previste per il procedimento di esecuzione (vedi par. 2.2.1).

A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio



dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.

Per questo provvedimento sono previsti 2 modelli di stampa: Ordinanza Generica, Ordinanza revoca pena sostitutiva.
Template: SIUS_OR_MODGENERICOUDS.rtf, SIUS_OR_REVOCAPENASOST.rtf.

Revoca Pene Sostitutive (art. 72 L. 689/81)
L’art. 72 legge 689/1981 prevede la revoca della pena sostitutiva a seguito sopravvenienza di nuova condanna, in questa evenienza è il Magistrato di Sorveglianza a disporre la revoca/sostituzione delle pene sostitutive, con ordinanza.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), è stato aggiunto il contenuto:
Revoca pena sostitutiva per intervenuta condanna (art. 72 L. 689/81)
Al nuovo contenuto sono associati i seguenti oggetti:
Revoca detenzione domiciliare sostitutiva per intervenuta condanna (art. 72 L. 689/81)
Revoca semilibertà sostitutiva per intervenuta condanna (art. 72 L. 689/81)
ed i seguenti esiti:
Revoca e converte in pena detentiva
Revoca e converte in altra pena sostitutiva
Non Revoca
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS. Le form di iscrizione e di dettaglio del procedimento sono identiche a quelle descritte al par. 2.2.2, tranne per il contenuto e oggetto.

E’ possibile procedere alla definizione di questo procedimento emettendo una ordinanza  Revoca Pena Sostitutiva, che è quella del precedente paragrafo


In cui nella combo box Pena Sostitutiva più grave il sistema presenterà le tre pene sostitutive previste per il procedimento di esecuzione (vedi par. 3.2).

A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio


dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.

Sono  previsti due modelli di stampa: Ordinanza Generica, Ordinanza revoca pena sostitutiva.

Template: SIUS_OR_MODGENERICOUDS.rtf, SIUS_OR_REVOCAPENASOST.rtf.

Revoca pena sostitutiva conseguente alla conversione p.p. per avvenuto pagamento
Stante quanto prescritto dal comma 15 dell’art. 660 c.p.p., bisogna gestire un nuovo procedimento “figlio” nell’ambito dell’EPS, che potremmo denominare, sia nel contenuto che nell’oggetto, “Revoca pena sostitutiva conseguente alla conversione pena pecuniaria per avvenuto pagamento”. Gli esiti potrebbero essere “Revoca pena sostitutiva”; “Non revoca pena sostitutiva”; “Dichiara NDP/NLP”; Dichiara inammissibilità”; “Dichiara incompetenza”.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:
Revoca pena sostitutiva conseguente alla conversione pena pecuniaria per avvenuto pagamento (art. 660 co. 15 c.p.p.)  U146
Al nuovo contenuto va associato il seguente oggetto:
Revoca pena sostitutiva conseguente alla conversione pena pecuniaria per avvenuto pagamento (art. 660 co. 15 c.p.p.)  (3200)
ed i seguenti esiti:
Revoca pena sostitutiva   (0285)
Non Revoca pena sostitutiva    (0286)
Dichiara N.D.P./ N.L.P  (0004)
Dichiara inammissibilità  (0003)
Dichiara la propria incompetenza  (0005)
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva, pertanto l’iscrizione sarà uguale a quella di tutti gli altri procedimenti figli dell’Esecuzione Pena Sostitutiva.

E’ possibile procedere alla definizione di questo procedimento emettendo una ordinanza  Revoca Pena Sostitutiva conseguente alla conversione pena pecuniaria



A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio


dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.

Per questo provvedimento è previsto un unico modello di stampa: ordinanza generica.
Template: SIUS_OR_MODGENERICOUDS.rtf.

Gestione Licenze – Pene Sostitutive

Per estendere l’attuale gestione delle Licenze per semilibertà e per internati anche alle Licenze – pene sostitutive saranno adeguate tutte le funzionalità, riferite a Licenza, presenti nella voce di menu verticale , cioè


Ricerca Licenze per Soggetto
Nell’attuale form:



Nella combo box Visualizza solo i provvedimenti relativi a, alle attuali voci “Licenze” e “Licenze per Internati” è stata aggiunta la nuova voce “Licenze – pene sostitutive”. Tutto il codice è stato aggiornato per gestire le nuove tipologie di Licenza.
Esecuzione Licenza
Le attuali funzioni attivabili dalla sottostante form:


Sono state aggiornate per poter  essere utilizzate anche per le Licenze – pene sostitutive.
Relazione Trimestrale
L’attuale form è stata modificata:



Con l’aggiunta di un nuovo radio button per poter utilizzare la funzione anche per la nuova Licenza con conseguente aggiornamento del codice. Il risultato della ricerca calcolerà e mostrerà a video il totale delle occorrenze ottenute in base ai criteri di ricerca inseriti.