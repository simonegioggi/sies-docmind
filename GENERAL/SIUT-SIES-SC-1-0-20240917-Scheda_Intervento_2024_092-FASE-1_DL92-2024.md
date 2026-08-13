---
uniqueName: siut-sies-sc-1-0-20240917-schedaintervento2024092-
displayName: "SIUT SIES SC 1 0 20240917 Scheda Intervento 2024 092 FASE 1 DL92 2024"
category: "GENERAL"
tags: []
---

# SIUT-SIES-SC-1.0-20240917-Scheda_Intervento_2024_092-FASE-1_DL92-2024

> **File originale:** `MEV/SCHEDA_092/SIUT-SIES-SC-1.0-20240917-Scheda_Intervento_2024_092-FASE-1_DL92-2024.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento per l’innovazione tecnologica della giustizia
Direzione generale per i sistemi informativi automatizzati |
| --- |
|  |





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Umberto Mignogna |  |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 17/09/2024 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 17/09/2024 | Prima Emissione |  |
|  |  |  |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Vincenzo De Lisi | Amministrazione |  | Responsabile Unico Procedimento |
| Oris Orlando | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Francesco Rosati | RTI |  | Responsabile Manutenzione Correttiva
Referente Qualità e Sicurezza |
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
2.1	Calcolatrice Pena Ipotetica	7
3	Interventi sottosistema SIUS	10
3.1	Eliminazione Ordinanza Conferma Decisione Magistrato Relatore	10
3.2	Aggiornamento Ordinanza Applicazione Provvisoria	10
3.3	Aggiornamento Compilazione foglio complementare	11
3.4	Aggiornamento Monitoraggio Misure Alternative (art. 678 comma 1-ter c.p.p.)	12
3.5	Aggiornamento Statistica Monitoraggio per oggetti	12

Introduzione
Scopo del documento
L’intervento in oggetto è stato richiesto con comunicazione “prot_10437-24_NOTA_PG_CARCERI_firmato_dig.(1).pdf” e rientra nel servizio di Manutenzione Evolutiva.
Nel documento sono descritti gli interventi urgenti da realizzare in SIES, ambiti SIEP e SIUS, per far fronte alle novità normative introdotte del D.L. 92/2024, in attesa da parte dell’Amministrazione dell’individuazione degli ulteriori interventi necessari.
Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF 1 | prot_10437-24_NOTA_PG_CARCERI_firmato_dig.(1) | Richiesta Scheda |

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
L’esigenza principale richiesta dagli uffici nella fase di gestione dei nuovi procedimenti è di poter calcolare i semestri e i relativi n.ro di giorni di liberazione anticipata usufruibili dal condannato e quindi arrivare al calcolo della pena ipotetica da espiare, se il soggetto aderisce alle opere di rieducazione stabilite dalla Sorveglianza.
Calcolatrice Pena Ipotetica
La funzione permetterà di calcolare per un procedimento, in base ai dati presenti nella base dati, il numero di giorni di liberazione anticipata concedibili sui quantum di pena di presofferto e sui quantum di pena da espiare pervenendo alla cosiddetta pena ipotetica ad esito delle detrazioni dei soli giorni di liberazione anticipata detraibili.

La funzione potrà essere attivata, selezionando una nuova icona, che sarà aggiunta nel menu delle azioni veloci




Selezionandola si riceverà la seguente form



In cui i dati presenti nel riquadro in rosso sono i dati calcolati dal sistema in base a quelli presenti nella base dati per il procedimento corrente. Sono sostanzialmente una sintesi di quelli più dettagliati che si ottengono utilizzando la funziona Dettaglio Pena .
N.B. Sarà possibile modificare i dati riportati nella maschera, in caso di dati a sistema non coincidenti con quelli in possesso dell’ufficio o per poter utilizzare la funzione come una semplice calcolatrice.
A seguito della Conferma il sistema procederà a calcolare:
- per il presofferto, il numero di giorni di L.A. usufruibili, il numero di semestri utili, il numero di giorni di custodia cautelare eccedenti il numero di semestri utili da poter conteggiare sulla pena da espiare;
- per la pena da espiare, il numero di semestri utili di pena ipotetica per l’erogazione della liberazione anticipata, giorni di liberazione anticipata maturata e usufruibili;
- Dati da indicare nel provvedimento di esecuzione, pena ipotetica ottenuta applicando le detrazioni (Anni, Mesi e Giorni), numero di semestri scontati, giorni di l.a. concedibili, giorni di l.a. usufruibili
- Calcoli con data di esecuzione (solo risulta valorizzata la data di Decorrenza nella prima parte della form (es. soggetto detenuto)), data decorrenza pena, data scarcerazione senza l.a., data scarcerazione con l.a. applicata (data fine pena con fungibilità), data scarcerazione con l.a. concessi (data fine pena senza fungibilità), data scarcerazione senza applicare l’ultima semestre (in caso di credito l.a.).
Al termine della fase di elaborazione sarà possibile, selezionando l’icona , richiedere la generazione del foglio Excel, contenente il dettaglio dei passaggi effettuati per arrivare ai numeri sopra riportati, per eventuali verifiche da parte dell’ufficio.
In base alla posizione giuridica del soggetto (libero o detenuto) il sistema genererà un foglio Excel specifico:
Libero


Detenuto

Sempre al termine della fase di elaborazione sarà possibile, selezionando l’icona , richiedere la stampa di un template libero o detenuto, il cui contenuto sarà specificato dall’Amministrazione e che dovrebbe essere utilizzato per integrare gli attuali provvedimenti, prodotti da SIEP, in cui è necessario specificare la pena ipotetica ad esito delle detrazioni usufruibile.

Interventi sottosistema SIUS
Il Dl 92/2024 ha modificato alcune norme introdotte con il decreto 123/2018, che comporta la revisione di alcune funzionalità realizzate con la MEV-09. Sostanzialmente la precedente ordinanza di applicazione provvisoria, non richiede più la successiva fase di Conferma, ma diventa direttamente definitiva.
Eliminazione Ordinanza Conferma Decisione Magistrato Relatore
Il D.lgs 92/2024 abolisce la fase di Conferma della Decisione del Magistrato Relatore da parte del TDS per le misure alternative ex art. 678 comma 1 ter c.p.p., per cui era prevista l’ordinanza collegiale di Conferma. Si provvederà pertanto ad eliminare dal menu

la voce evidenziata in rosso e verrà rinominata la voce “Applicazione Provvisoria M.A.” come descritto nel prossimo paragrafo.
Aggiornamento Ordinanza Applicazione Provvisoria
L’ordinanza di Applicazione Provvisoria, alla stregua di tutte le altre ordinanze, non concederà la misura provvisoriamente ma definitivamente, per cui bisognerà modificare l’attuale comportamento.
Nel menu ordinanze

la voce riportata nel riquadro in rosso sarà modificata in



Applicazione Misure Alternative Dl 123/2018, presenterà l’attuale form, che sarà semplicemente rinominata





Per la funzione rimangono attivi i controlli:
lo stato del procedimento deve essere “Emesso decreto di designazione”;
il luogo di svolgimento della prova deve essere obbligatoriamente valorizzato.
Sarà possibile utilizzare la funzione per inserire la restituzione degli atti al Presidente.

Bisognerà modificare:

l’esito del contenuto da ‘Applica provvisoriamente’ ad ‘Applica ex art. 678 comma 1 ter cpp’
il template SIUS_OR_APPLPROVMA.rtf
il deposito dell’ordinanza, che non dovrà più impostare lo stato a ‘Emessa Ordinanza Applicazione Provvisoria’, che non rappresentava uno stato definitorio del procedimento, ma dovrà impostarlo ad ‘Emesso Provvedimento’, definendo il procedimento.
Aggiornamento Compilazione foglio complementare
Bisognerà modificare l’attuale funzione, vincolando, per i procedimenti con contenuto ‘Concessione Misure Alternative alla Detenzione (art. 678 comma 1 ter c.p.p.)’ (C050 e C051), la possibilità di inserire il Foglio complementare solo se sull’ordinanza di definizione del procedimento è presente la data di esecutività, gestendo uno specifico messaggio in caso di assenza.

Aggiornamento Monitoraggio Misure Alternative (art. 678 comma 1-ter c.p.p.)
Essendo stata abolita l’attività di Conferma dell’ordinanza di applicazione provvisoria l’attuale form:

viene modificata come di seguito:

Bisognerà aggiornare la funzione per gestire il nuovo stato procedimento (Emesso provvedimento invece del precedente Emessa ordinanza di applicazione provvisoria).
Aggiornamento Statistica Monitoraggio per oggetti
Bisognerà aggiornare la funzione Statistiche/Monitoraggio » Monitoraggio Provvedimenti » Per Oggetti modificando nel file excel generato, nella riga di intestazione dei fogli Dettaglio e Totali per Magistrato


la descrizione della colonna, su evidenziata nel riquadro rosso, da Accolti Provvisoriamente in Accolti ex art.678 c.1 ter c.p.p.