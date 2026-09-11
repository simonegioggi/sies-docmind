**RISERVATO**

**SIES 2.0**

**PROGRAMMA NAZIONALE DI EVOLUZIONE INTEGRATA**

Sistema Informativo dell'Esecuzione e della Sorveglianza

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th><strong>Proposta rimodulata sugli indirizzi dell’Amministrazione<br />
</strong>Trasformazione unitaria di SIEP, SIUS e SIGE, architettura e dato nazionale centralizzati, sperimentazione graduale dei tre comparti e dismissione dei sistemi legacy entro 24 mesi.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

| **Informazione** | **Valore** |
|:---|:---|
| Cliente | Ministero della Giustizia - DIT |
| Oggetto | Evoluzione integrata dell’ecosistema SIES |
| Stato | Proposta preliminare rimodulata |
| Orizzonte massimo | 24 mesi, inclusi sviluppo, sperimentazione, migrazione e avvio nazionale |
| Prodotto da | Engineering Ingegneria Informatica S.p.A. |
| Data | 10 settembre 2026 |

# Indice dei contenuti

1.  Premessa e finalità del documento

2.  Presupposti e percorso di rimodulazione

3.  Il SIES oggi

4.  Indirizzi dell’Amministrazione e impatti sulla proposta

5.  Visione del SIES di domani

6.  Perimetro funzionale del programma

7.  Metodo di assessment e gap analysis

8.  Proposta realizzativa

9.  Roadmap integrata di 24 mesi

10. Sperimentazione, migrazione e spegnimento dei legacy

11. Portale per utenti esterni

12. Deleghe alla Polizia Giudiziaria

13. Governance, deliverable e criteri di accettazione

14. Quadro economico preliminare

15. Assunzioni, vincoli e rischi

16. Conclusioni e valore della proposta

# 1. Premessa e finalità del documento

Il presente documento descrive la rimodulazione complessiva della proposta di evoluzione del Sistema Informativo dell’Esecuzione e della Sorveglianza (SIES), a seguito degli indirizzi condivisi dall’Amministrazione. La nuova impostazione non costituisce un semplice aggiornamento della precedente roadmap, ma una ridefinizione dei presupposti strategici, funzionali, architetturali, temporali ed economici dell’iniziativa.

La finalità è rappresentare in modo unitario: il punto di partenza; la proposta inizialmente elaborata da Engineering; le indicazioni successivamente formulate dall’Amministrazione; la visione target; il perimetro dei comparti SIEP, SIUS e SIGE; il metodo di analisi; le attività di realizzazione e sperimentazione; il percorso di migrazione e dismissione dei sistemi esistenti; la roadmap massima di 24 mesi; e una stima economica preliminare per comparti.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th><strong>Obiettivo programmatico<br />
</strong>Entro il ventiquattresimo mese devono essere concluse analisi, progettazione, realizzazione, sperimentazione graduale sui tre comparti, migrazione, formazione, roll-out e attivazione del nuovo SIES quale unico sistema nazionale, con contestuale dismissione dei sistemi legacy SIEP, SIUS e SIGE.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

# 2. Presupposti e percorso di rimodulazione

## 2.1 La proposta originaria di Engineering

La proposta originaria di Engineering muoveva dalla conoscenza consolidata dell’attuale ecosistema SIES e prevedeva un percorso progressivo, avviato dalla reingegnerizzazione del SIUS, affiancato da una componente dedicata all’acquisizione delle informazioni provenienti dalla cognizione, e successivamente esteso agli altri domini applicativi.

Tale impostazione valorizzava il SIUS quale ambito iniziale di trasformazione e baseline per il riuso di architetture e componenti. Era inoltre previsto un percorso incrementale di sperimentazione e migrazione, con mantenimento del legacy quale ambiente ufficiale fino al passaggio finale.

## 2.2 Perché la strategia originaria viene superata

Gli indirizzi dell’Amministrazione modificano il presupposto fondante della strategia di reingegnerizzazione, ma non fanno venir meno gli interventi iniziali già individuati sul sistema attuale. Restano quindi validi e parte del programma gli interventi abilitanti, le integrazioni documentali e il percorso dei depositi telematici. Viene invece superata la sequenza che assumeva la Sorveglianza quale punto di partenza autonomo della trasformazione. Il programma deve ora affrontare sin dall’inizio SIEP, SIUS e SIGE come parti di un unico ecosistema nazionale.

- Decade integralmente la scelta di partire dal SIUS come progetto pilota o fase propedeutica, mentre restano validi gli interventi iniziali sul sistema attuale e sui depositi telematici.

- SIEP, SIUS e SIGE devono essere analizzati in parallelo e sviluppati come stream coordinati.

- La componente di acquisizione dei dati della cognizione non è un’iniziativa autonoma e non deve essere denominata come sistema separato.

- Il target è una piattaforma unitaria, con architettura centralizzata e dato unico nazionale.

- La roadmap deve indicare in modo chiaro quando i sistemi attuali vengono spenti e il nuovo sistema diviene l’unico ambiente operativo.

## 2.3 Natura della nuova proposta

La presente proposta assume pertanto la forma di un nuovo Programma Nazionale di Evoluzione Integrata del SIES. Essa conserva e valorizza la conoscenza maturata sull’AS IS, ma ridefinisce integralmente il modello di attuazione, la roadmap, la struttura economica e la rappresentazione architetturale.

# 3. Il SIES oggi

Il SIES costituisce il sistema di riferimento per la gestione dei procedimenti dell’esecuzione penale e della sorveglianza ed è articolato in tre sottosistemi funzionalmente distinti ma correlati.

| **Sistema** | **Uffici principali** | **Ambito attuale** | **Criticità da superare** |
|:---|:---|:---|:---|
| SIEP | Procure e uffici esecuzione penale | Titolo esecutivo, ordini di esecuzione e carcerazione, decreti e adempimenti della Procura | Frammentazione, integrazioni limitate, gestione per registri e basi territoriali |
| SIUS | Tribunali e Uffici di Sorveglianza | Fascicoli, istruttoria, udienze, misure alternative, permessi, licenze e provvedimenti | Tecnologie legacy, processi non pienamente digitali, disomogeneità e duplicazioni |
| SIGE | Uffici del Giudice dell’Esecuzione | Incidenti di esecuzione, opposizioni, provvedimenti e relativo fascicolo | Copertura digitale da consolidare, integrazioni e tracciabilità da rafforzare |

## 3.1 Caratteristiche dell’AS IS

- Articolazione applicativa e informativa per sottosistemi e territori.

- Presenza di basi dati e componenti legacy che aumentano complessità e costi evolutivi.

- Logica prevalentemente orientata a registri, procedimenti e singole istanze.

- Interoperabilità non uniforme con i sistemi della cognizione e con gli altri sistemi ministeriali.

- Persistenza di lavorazioni manuali e scambi documentali non pienamente integrati.

- Patrimonio funzionale ampio, che include funzioni effettivamente utilizzate, funzioni scarsamente usate e fabbisogni nuovi non ancora coperti.

## 3.2 Interventi iniziali sul sistema SIES attuale

Gli interventi iniziali già previsti nella proposta precedente non devono essere eliminati. Essi conservano piena validità funzionale e rappresentano una linea di continuità del programma: producono benefici immediati sull’attuale piattaforma e, se progettati secondo principi di riuso e disaccoppiamento, preparano componenti, servizi e modalità operative da preservare nel nuovo SIES.

| **Intervento** | **Finalità nel sistema attuale** | **Valore nel programma target** |
|----|----|----|
| Accesso utenti tramite ADN | Uniformare autenticazione, Single Sign-On, profilazione e controllo degli accessi. | Costituisce il riferimento per identità, autenticazione e autorizzazione del nuovo SIES. |
| Fogli complementari SIEP - SIC Casellario | Digitalizzare e automatizzare i flussi informativi tra esecuzione penale e Casellario. | Anticipa il modello di interoperabilità e condivisione controllata del dato. |
| Firma digitale remota | Integrare la sottoscrizione qualificata dei provvedimenti nel workflow applicativo. | Servizio trasversale riutilizzabile dai comparti SIEP, SIUS e SIGE. |
| Integrazione con Mercurio | Utilizzare il documentale istituzionale quale archivio ufficiale degli atti. | Servizio documentale comune della piattaforma nazionale. |

### 3.2.1 Criterio di continuità e riuso

Tali interventi devono essere governati evitando soluzioni temporanee non recuperabili. Le componenti realizzate o consolidate sull’attuale sistema dovranno essere valutate nella gap analysis e, ove coerenti con l’architettura target, riutilizzate o evolute nel nuovo ecosistema. Il relativo piano economico dovrà distinguere le attività già coperte, quelle necessarie al completamento sull’attuale sistema e quelle da ricomprendere nella piattaforma futura, evitando duplicazioni di costo.

## 3.3 Integrazioni sul sistema SIES attuale - Deposito Difensore

Anche il percorso del Deposito Difensore resta valido e parte integrante del programma. La proposta continua a prevedere la digitalizzazione dei depositi relativi all’incidente di esecuzione verso il Giudice dell’Esecuzione e dei depositi destinati alla Sorveglianza. La rimodulazione riguarda il loro posizionamento: le funzionalità devono produrre benefici immediati sugli attuali SIGE e SIUS e, al tempo stesso, costituire il nucleo riutilizzabile del futuro canale digitale del nuovo SIES.

### 3.3.1 Deposito dell’incidente di esecuzione verso SIGE

- Trasmissione telematica dell’istanza e degli allegati al Giudice dell’Esecuzione.

- Classificazione e instradamento verso l’ufficio e il procedimento competenti.

- Presa in carico da parte della cancelleria, associazione al fascicolo e tracciabilità completa.

- Integrazione iniziale con SIGE e successiva continuità nel comparto SIGE del nuovo SIES.

### 3.3.2 Deposito verso la Sorveglianza

- Deposito telematico di istanze e atti relativi, tra l’altro, a misure alternative, permessi, licenze, pene sostitutive, reclami e ricorsi.

- Acquisizione, classificazione, smistamento e associazione al fascicolo digitale.

- Disponibilità degli atti per magistrati e cancellerie e riduzione delle lavorazioni manuali.

- Integrazione iniziale con SIUS e successiva continuità nel comparto SIUS del nuovo SIES.

### 3.3.3 Accesso tramite PDP, FE e gestione dell’autorizzazione

Il Portale PDP mantiene il ruolo di punto di accesso istituzionale per il difensore e presidia l’autenticazione del professionista, valorizzando i meccanismi già disponibili nell’ecosistema ministeriale e l’integrazione con ReGIndE. Dal PDP il difensore accede alla funzione specialistica di deposito dell’esecuzione penale e della sorveglianza.

La componente FE deve essere esplicitamente considerata nel modello di autorizzazione. L’autenticazione identifica il professionista, mentre l’autorizzazione determina se il difensore possa operare sullo specifico fascicolo o procedimento e nell’interesse del soggetto assistito. FE concorre quindi alla verifica del contesto applicativo e delle condizioni di accesso al fascicolo, evitando che il solo accesso autenticato al PDP abiliti automaticamente il deposito su qualunque posizione.

La verifica deve tenere distinti almeno quattro livelli: identità del professionista; abilitazione professionale e dati disponibili tramite ReGIndE; autorizzazione FE sul fascicolo o procedimento; legittimazione del difensore ad agire per il soggetto assistito. La nomina o procura non è trattata come un semplice allegato, ma come elemento essenziale del processo di deposito e della successiva presa in carico.

| **Presidio** | **Funzione** | **Esito** |
|----|----|----|
| PDP | Accesso istituzionale e autenticazione del professionista. | Utente identificato e sessione autorizzata verso il servizio. |
| ReGIndE | Disponibilità delle informazioni professionali previste dall’ecosistema ministeriale. | Supporto alla verifica del profilo professionale. |
| FE - autorizzazione | Verifica dell’abilitazione ad accedere e operare sullo specifico fascicolo o procedimento. | Accesso consentito o negato in relazione al contesto applicativo. |
| Legittimazione | Verifica della relazione tra difensore, assistito e deposito, sulla base delle informazioni e della documentazione disponibili. | Deposito lavorabile, da integrare o non ammissibile secondo le regole definite. |
| SIES/SIGE/SIUS | Classificazione, instradamento, presa in carico e associazione al fascicolo. | Atto acquisito e tracciato nel procedimento competente. |

Nella fase iniziale, ove non siano disponibili controlli centralizzati completi, la verifica della legittimazione può continuare a basarsi sulla documentazione prodotta dal difensore e sui controlli dell’ufficio competente. Il modello target deve tuttavia consentire la progressiva automatizzazione delle verifiche, valorizzando FE e le informazioni disponibili nei sistemi ministeriali, senza duplicare archivi o introdurre autorizzazioni non governate.

### 3.3.4 Evoluzione verso il nuovo SIES

Il servizio di deposito non deve essere concepito come integrazione puntuale destinata a essere sostituita. Deve essere progettato come componente specialistico riutilizzabile, capace di operare inizialmente con gli attuali SIUS e SIGE e di integrarsi successivamente con i corrispondenti comparti del nuovo SIES. In questo modo gli investimenti iniziali restano parte del programma complessivo e non vengono dispersi nella fase di transizione.

# 4. Indirizzi dell’Amministrazione e impatti sulla proposta

| **Indirizzo** | **Conseguenza progettuale** |
|:---|:---|
| Programma unitario SIES | Analisi, progettazione e realizzazione coordinate di SIEP, SIUS e SIGE. |
| Unica base dati nazionale | Superamento delle basi distrettuali e definizione di un modello informativo centralizzato. |
| Sviluppo parallelo dei tre comparti | Stream funzionali distinti, ma governati da architettura, servizi e roadmap comuni. |
| Nessuna coesistenza permanente | Sperimentazione graduale, migrazione controllata e switch finale entro il mese 24. |
| Modello centrato sulla persona | Passaggio da una logica registro-centrica a soggetto, posizione e percorso esecutivo. |
| Integrazione con la cognizione | Servizi interni al nuovo SIES per acquisire dati del soggetto e provvedimenti irrevocabili dai sistemi titolari. |
| Portale esterno nel perimetro, ma successivo | Lotto evolutivo separato dal Core SIES. |
| Deleghe alla PG non prioritarie | Estensione successiva, fuori dal percorso critico dei 24 mesi del Core. |
| Orizzonte massimo di 24 mesi | Durata comprensiva di analisi, sviluppo, sperimentazione, migrazione, formazione e go-live. |

# 5. Visione del SIES di domani

Il nuovo SIES sarà una piattaforma nazionale unitaria dell’esecuzione penale e della sorveglianza. I tre domini SIEP, SIUS e SIGE manterranno la propria riconoscibilità funzionale, ma opereranno su un modello dati condiviso, su servizi trasversali comuni e su un’architettura centralizzata.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th><strong>Visione target<br />
</strong>Un’unica piattaforma nazionale che segue la persona e il relativo percorso esecutivo, acquisisce dai sistemi titolari i dati del soggetto e dei provvedimenti irrevocabili, governa i processi di Procure, Sorveglianza e Giudice dell’Esecuzione e rende possibile la dismissione completa delle soluzioni legacy.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

## 5.1 Principi del modello target

- Dato unico nazionale e responsabilità chiara sulla titolarità delle informazioni.

- Architettura centralizzata presso una sola infrastruttura di riferimento.

- Modello applicativo orientato alla persona, alla posizione esecutiva e alla sequenza degli eventi rilevanti.

- Servizi comuni di identità, autorizzazione, workflow, documentale, firma, audit e monitoraggio.

- Interoperabilità nativa e disaccoppiata con APP, SICP, ReGeWeb, Casellario e ulteriori sistemi ministeriali.

- Sviluppo e sperimentazione progressivi, senza trasformare la gradualità in coesistenza permanente.

## 5.2 Dati del soggetto e provvedimenti irrevocabili

Il nuovo SIES dovrà includere, come parte integrante della propria piattaforma, un modulo di servizi e interfacce per acquisire dai sistemi titolari le informazioni relative al soggetto e ai provvedimenti divenuti irrevocabili, quali sentenze, ordinanze e decreti. La componente non costituisce un progetto o sistema autonomo, ma un insieme di servizi interni di interoperabilità, normalizzazione, verifica e distribuzione del dato ai comparti SIEP, SIUS e SIGE.

## 5.3 Oggi e domani

| **Dimensione** | **Oggi** | **Domani** |
|:---|:---|:---|
| Impostazione | Tre sottosistemi e articolazioni territoriali | Un programma e una piattaforma nazionale integrata |
| Dato | Distribuito e potenzialmente duplicato | Unico, centralizzato e governato |
| Unità logica | Registro, procedimento, istanza | Persona, posizione e percorso esecutivo |
| Integrazioni | Puntuali e differenziate | Servizi standard e interfacce native |
| Rilascio | Evoluzioni dei singoli sistemi | Stream paralleli, sperimentazione graduale e switch unitario |
| Esercizio | Legacy distinti | Nuovo SIES come unico ambiente nazionale |

# 6. Perimetro funzionale del programma

## 6.1 Core SIES

### 6.1.1 Comparto SIEP - Procure

- Gestione del titolo e della posizione esecutiva.

- Ordini di esecuzione, ordini di carcerazione, sospensioni e relativi adempimenti.

- Decreti e provvedimenti della fase esecutiva di competenza della Procura.

- Interazione con dati e provvedimenti provenienti dalla cognizione.

- Comunicazioni e interoperabilità con Sorveglianza, Giudice dell’Esecuzione, Casellario e sistemi interessati.

### 6.1.2 Comparto SIUS - Sorveglianza

- Fascicolo digitale e presa in carico degli atti.

- Istruttoria, udienze, ordinanze, decreti, ricorsi e impugnazioni.

- Misure alternative, permessi, licenze e pene sostitutive.

- Cooperazione con UEPE, istituti penitenziari, difensori e ulteriori soggetti istituzionali.

- Scadenzari, monitoraggio, tracciabilità e consultazione della posizione esecutiva.

### 6.1.3 Comparto SIGE - Giudice dell’Esecuzione

- Gestione del fascicolo e degli incidenti di esecuzione.

- Opposizioni, istanze, udienze e provvedimenti.

- Collegamento tra provvedimento irrevocabile, titolo e successivi eventi dell’esecuzione.

- Interoperabilità con SIEP, sistemi della cognizione e servizi documentali.

## 6.2 Servizi comuni della piattaforma

| **Servizio** | **Contenuto** |
|:---|:---|
| Soggetto e posizione esecutiva | Anagrafiche, identificazione univoca, posizioni, relazioni e percorso esecutivo. |
| Interoperabilità | Acquisizione e aggiornamento dati da sistemi titolari; API, eventi, controlli e tracciabilità. |
| Workflow | Gestione configurabile dei processi, attività, scadenze, ruoli e stati. |
| Documentale e firma | Produzione, sottoscrizione, classificazione, archiviazione e reperibilità degli atti. |
| Identità e sicurezza | Autenticazione, autorizzazione, profilazione, segregazione dei ruoli e audit. |
| Monitoraggio | Cruscotti, statistiche, indicatori operativi e alimentazione del patrimonio informativo centrale. |
| Migrazione | Strumenti di estrazione, bonifica, riconciliazione, caricamento e verifica dei dati legacy. |

# 7. Metodo di assessment e gap analysis

La conoscenza consolidata dell’AS IS evita un assessment esplorativo generalista. La fase iniziale sarà mirata a verificare l’uso reale delle funzioni, rilevare i gap, definire il modello target e produrre un backlog nazionale approvabile. Le attività saranno svolte in parallelo sui tre comparti.

## 7.1 Classificazione funzionale

| **Classe** | **Definizione** | **Decisione attesa** |
|:---|:---|:---|
| A - Utili e utilizzate | Funzioni operative effettivamente usate e necessarie | Mantenere, semplificare o reingegnerizzare |
| B - Non utili/non usate | Funzioni presenti ma non utilizzate o superate | Eliminare o non riportare nel target |
| C - Mancanti e necessarie | Funzioni non contemplate dall’attuale sistema ma indispensabili | Inserire nel backlog prioritario |
| D - Nice to have | Funzioni migliorative non essenziali al go-live | Posticipare o attivare se compatibili con budget e tempi |

## 7.2 Attività per comparto

- Censimento delle funzioni e dei processi realmente utilizzati.

- Raccolta di evidenze e confronto con utenti rappresentativi dei diversi uffici.

- Identificazione delle varianti territoriali e valutazione della loro effettiva necessità.

- Analisi delle integrazioni, dei dati, dei flussi documentali e delle responsabilità informative.

- Disegno dei processi target e definizione dei requisiti condivisi.

- Prioritizzazione secondo valore, obbligatorietà, frequenza d’uso, rischio e dipendenze.

## 7.3 Deliverable della fase iniziale

| **Deliverable** | **Contenuto** |
|:---|:---|
| Catalogo Funzionale Nazionale SIES | Elenco completo delle funzioni con classificazione A/B/C/D, comparto, utenti, priorità e decisione target. |
| Mappa dei processi AS IS e TO BE | Processi di Procure, Sorveglianza e Giudice dell’Esecuzione, interdipendenze e responsabilità. |
| Modello dati target | Soggetto, posizione esecutiva, provvedimenti, eventi e relazioni. |
| Architettura target | Servizi comuni, domini, integrazioni, sicurezza e collocazione centralizzata. |
| Backlog nazionale prioritizzato | Epiche, funzioni, requisiti, dipendenze e criteri di accettazione. |
| Piano migrazione e sperimentazione | Dati, uffici pilota, wave, criteri di ingresso/uscita e switch finale. |
| Stima economica consolidata | Rideterminazione del costo per comparto sulla base del perimetro approvato. |

# 8. Proposta realizzativa

La realizzazione sarà organizzata in quattro stream coordinati: piattaforma comune, SIEP, SIUS e SIGE. L’analisi parte contemporaneamente sui tre comparti; la progettazione e lo sviluppo procedono per incrementi coordinati; la sperimentazione interessa gradualmente tutti gli uffici rappresentativi; il programma converge su un unico go-live nazionale entro il mese 24.

## 8.1 Stream Piattaforma comune

- Modello dati nazionale centrato su soggetto e percorso esecutivo.

- Servizi di interoperabilità verso i sistemi titolari dei dati.

- Identity and access management, sicurezza, audit e logging.

- Documentale, firma digitale e gestione degli atti.

- Workflow, notifiche, scadenze e servizi trasversali.

- Framework di migrazione, data quality e riconciliazione.

## 8.2 Stream applicativi

Gli stream SIEP, SIUS e SIGE sviluppano le funzioni di dominio selezionate nel catalogo funzionale, riusando servizi comuni e mantenendo allineati modello dati, criteri di progettazione, sicurezza, esperienza utente e standard di interoperabilità.

# 9. Roadmap integrata di 24 mesi

La durata di 24 mesi rappresenta il limite massimo dell’intero programma e include tutte le attività necessarie a rendere il nuovo SIES l’unico ambiente nazionale di esercizio. Le fasi sono sovrapposte in modo controllato per evitare che sperimentazione e migrazione siano rinviate dopo lo sviluppo.

| **Fase** | **Periodo** | **Attività principali** | **Risultato** |
|:---|:---|:---|:---|
| 1\. Gap analysis e disegno target | M1-M5 | Analisi parallela SIEP/SIUS/SIGE; catalogo A/B/C/D; processi target; architettura; backlog; piano dati | Perimetro e baseline approvati |
| 2\. Fondazioni e primi incrementi | M4-M10 | Core platform; modello dati; interoperabilità; workflow; sicurezza; primi incrementi dei tre comparti | Piattaforma comune e funzioni iniziali testabili |
| 3\. Realizzazione completa per comparti | M8-M17 | Sviluppo parallelo SIEP, SIUS e SIGE; integrazioni; test; migrazione tecnica iterativa | Copertura funzionale prioritaria completa |
| 4\. Sperimentazione graduale | M12-M20 | Piloti e wave su Sorveglianza, Procure e Giudice esecuzione; formazione; feedback; correzioni | Soluzione validata nei tre contesti operativi |
| 5\. Roll-out e migrazione finale | M19-M24 | Estensione nazionale; migrazione definitiva; formazione; cut-over; supporto intensivo | Nuovo SIES unico sistema e legacy dismessi |

## 9.1 Milestone

| **Milestone** | **Termine massimo** | **Evidenza** |
|:---|:---|:---|
| M1 - Baseline funzionale e architetturale | Mese 5 | Catalogo funzionale, processi target, architettura e backlog approvati. |
| M2 - Core platform disponibile | Mese 10 | Servizi comuni e primi incrementi dei tre comparti negli ambienti di test. |
| M3 - Copertura prioritaria completa | Mese 17 | Funzioni Core SIES realizzate e integrate per SIEP, SIUS e SIGE. |
| M4 - Sperimentazione conclusa | Mese 20 | Esiti pilota, correzioni, data quality e readiness al roll-out. |
| M5 - Go-live nazionale | Mese 24 | Nuovo SIES operativo, migrazione conclusa e sistemi legacy dismessi. |

# 10. Sperimentazione, migrazione e spegnimento dei legacy

## 10.1 Sperimentazione graduale su tutti i comparti

La sperimentazione non riguarda un solo sistema e non è una fase successiva ai 24 mesi. È parte integrante della roadmap e coinvolge progressivamente Uffici di Sorveglianza, Procure e Uffici del Giudice dell’Esecuzione. Le ondate saranno avviate quando ciascun incremento raggiunge i criteri minimi di completezza, sicurezza, qualità dati e usabilità.

| **Wave** | **Ambito** | **Obiettivi** |
|:---|:---|:---|
| Wave A | Sorveglianza - SIUS | Validare fascicolo, istruttoria, provvedimenti, misure e cooperazione con soggetti esterni. |
| Wave B | Procure - SIEP | Validare titolo, ordini, adempimenti, integrazioni e gestione della posizione esecutiva. |
| Wave C | Giudice dell’Esecuzione - SIGE | Validare incidenti, opposizioni, udienze, provvedimenti e collegamenti informativi. |

## 10.2 Migrazione

- Profilazione, bonifica e riconciliazione dei dati fin dalle fasi iniziali.

- Migrazioni selettive per i piloti, con dati rappresentativi e controllati.

- Verifica della qualità e validazione da parte degli uffici.

- Prove ripetute di migrazione e cut-over prima del passaggio finale.

- Conservazione e consultabilità dello storico secondo la strategia approvata.

## 10.3 Dismissione

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th><strong>Milestone vincolante<br />
</strong>Entro il mese 24 il nuovo SIES deve essere aperto come unico sistema nazionale per Procure, Sorveglianza e Giudice dell’Esecuzione. Il cut-over finale comprende migrazione definitiva, attivazione dei servizi, supporto all’avvio e spegnimento dei legacy SIEP, SIUS e SIGE.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

# 11. Portale per utenti esterni

Il portale rivolto a difensori, cittadini e altri soggetti interessati resta nella visione complessiva, ma è proposto come lotto evolutivo successivo e finanziabile separatamente rispetto al Core SIES. Il Portale PDP mantiene il ruolo di punto di accesso istituzionale e di gestione dell’autenticazione e autorizzazione; le funzionalità specialistiche dell’esecuzione sono erogate dal portale SIES collegato.

## 11.1 Perimetro indicativo

- Accesso profilato e collegamento dal PDP.

- Presentazione di istanze e depositi con allegati.

- Consultazione delle pratiche e dello stato delle richieste.

- Comunicazioni, notifiche e ricevute.

- Verifica della legittimazione e gestione delle deleghe dell’utente esterno.

- Integrazione con fascicolo, documentale, pagamenti o ulteriori servizi ove previsti.

La stima deve riflettere la natura di un vero canale digitale specialistico, e non di una semplice pagina di accesso. Per questo viene indicata una forchetta preliminare separata compresa tra 0,5 e 0,8 milioni di euro, da consolidare dopo la definizione dei casi d’uso e delle integrazioni.

# 12. Deleghe alla Polizia Giudiziaria

L’integrazione con il Portale NDR per la gestione delle deleghe alla Polizia Giudiziaria non rientra nel percorso critico del Core SIES. È trattata come estensione successiva, da attivare in funzione delle priorità dell’Amministrazione e della disponibilità finanziaria.

- Emissione e trasmissione digitale della delega.

- Presa in carico e monitoraggio dello stato.

- Gestione delle comunicazioni e degli esiti.

- Collegamento al fascicolo e alla posizione esecutiva.

- Tracciabilità, notifiche e audit.

La stima preliminare separata è compresa tra 0,2 e 0,4 milioni di euro, da consolidare sulla base dei flussi e delle integrazioni effettivamente richieste.

# 13. Governance, deliverable e criteri di accettazione

## 13.1 Governance proposta

| **Livello** | **Finalità** | **Partecipanti indicativi** |
|:---|:---|:---|
| Steering Committee | Decisioni su perimetro, priorità, rischi, budget e milestone | Amministrazione, Engineering, referenti strategici |
| Program Management | Pianificazione integrata, dipendenze, avanzamento, qualità e reporting | PM, responsabili stream, responsabili migrazione e test |
| Tavoli di comparto | Processi, requisiti, validazione funzionale e priorità | Referenti SIEP, SIUS, SIGE e utenti rappresentativi |
| Tavolo architettura e dati | Architettura, interoperabilità, sicurezza, modello dati e ambienti | Architetti e titolari dei sistemi coinvolti |

## 13.2 Deliverable principali

- Catalogo funzionale nazionale e backlog prioritizzato.

- Architettura della soluzione e modello dati target.

- Specifiche di interoperabilità e sicurezza.

- Piano di migrazione, data quality e cut-over.

- Incrementi software dei tre comparti e servizi comuni.

- Evidenze di test, sperimentazione e accettazione.

- Materiali formativi, manualistica e piano di supporto.

- Verbale di go-live e piano di dismissione dei legacy.

# 14. Quadro economico preliminare

La stima economica è programmatica e deve essere consolidata al termine della gap analysis. Essa è costruita per comparti e include nel Core SIES tutte le attività necessarie al go-live entro 24 mesi: analisi, progettazione, sviluppo, integrazioni, test, sperimentazione, migrazione, formazione e roll-out. La forchetta dovrà inoltre ricomprendere e riconciliare gli interventi iniziali sul sistema attuale e sul Deposito Difensore che restano parte del programma, distinguendo attività già finanziate o realizzate, completamenti necessari e componenti riutilizzabili nel target.

## 14.1 Lotto prioritario - Core SIES

| **Macro-ambito** | **Stima minima k€** | **Stima massima k€** | **Contenuto** |
|:---|---:|---:|:---|
| Assessment e gap analysis integrata | 250 | 300 | Analisi parallela, catalogo funzionale, processi target, backlog e stima consolidata. |
| Core platform e servizi comuni | 650 | 750 | Dato nazionale, interoperabilità, workflow, documentale, sicurezza, audit e monitoraggio. |
| Comparto SIEP | 600 | 700 | Processi e funzioni delle Procure e dell’esecuzione penale. |
| Comparto SIUS | 800 | 900 | Processi e funzioni della Sorveglianza. |
| Comparto SIGE | 250 | 350 | Processi e funzioni del Giudice dell’Esecuzione. |
| Migrazione, sperimentazione, formazione e roll-out | 450 | 550 | Data quality, wave pilota, avvio nazionale, supporto e dismissione legacy. |
| TOTALE CORE SIES | 3.000 | 3.550 | Forchetta preliminare da ricondurre, in sede di consolidamento, all’obiettivo programmatico 3,0-3,5 M€. |

La forchetta di riferimento proposta per il Lotto Core è pertanto pari a 3,0-3,5 milioni di euro. Il valore puntuale sarà definito all’esito della classificazione funzionale, eliminando dal target le funzioni non utili o non utilizzate e distinguendo le funzioni necessarie dalle componenti nice to have. Il consolidamento dovrà dare evidenza separata delle evolutive sul sistema attuale e dei depositi telematici, verificando che non siano conteggiate due volte nelle voci di piattaforma comune, SIEP, SIUS e SIGE.

## 14.2 Lotti evolutivi successivi

| **Lotto** | **Stima preliminare** | **Note** |
|:---|:---|:---|
| Portale per utenti esterni | 0,5-0,8 M€ | Canale specialistico per difensori, cittadini e soggetti interessati; integrazione con PDP e Core SIES. |
| Deleghe alla Polizia Giudiziaria | 0,2-0,4 M€ | Workflow e integrazione con Portale NDR; priorità successiva. |

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th><strong>Separazione economica<br />
</strong>Il valore del Core SIES non include Portale esterno e Deleghe alla Polizia Giudiziaria. Le due componenti sono oggetto di lotti separati e attivabili successivamente.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

# 15. Assunzioni, vincoli e rischi

| **Elemento** | **Assunzione o rischio** | **Misura di governo** |
|:---|:---|:---|
| Perimetro funzionale | Ampiezza effettiva da consolidare sui tre comparti | Catalogo A/B/C/D e approvazione della baseline. |
| Tempi | 24 mesi massimi includono tutte le fasi | Sovrapposizione controllata di analisi, sviluppo, migrazione e sperimentazione. |
| Dati legacy | Qualità, completezza e riconciliazione possono incidere sul piano | Data profiling anticipato e prove iterative. |
| Uffici pilota | Disponibilità necessaria per validare processi e soluzione | Pianificazione preventiva e referenti nominati. |
| Sistemi esterni | Dipendenza da servizi, dati e ambienti dei sistemi titolari | Accordi di integrazione, specifiche condivise, mock e test di contratto. |
| Infrastruttura | Necessità di ambienti centralizzati e canali sicuri | Piano ambienti e readiness infrastrutturale nelle prime milestone. |
| Change management | Ampiezza e varietà della platea nazionale | Key user, formazione progressiva e supporto intensivo. |
| Cut-over | Nessuna coesistenza permanente, ma switch da governare | Piano di cut-over, prove generali, criteri go/no-go e rollback controllato. |

# 16. Conclusioni e valore della proposta

La rimodulazione proposta recepisce integralmente l’indirizzo di trasformare l’intero ecosistema SIES come programma unitario. La scelta originaria di partire dalla Sorveglianza viene abbandonata; SIEP, SIUS e SIGE sono affrontati fin dall’avvio attraverso analisi parallele, stream coordinati e un’unica architettura nazionale.

Il nuovo SIES non è la somma di tre riscritture, ma una piattaforma integrata centrata sulla persona e sul percorso esecutivo, dotata di servizi comuni e di interfacce interne per acquisire dai sistemi titolari le informazioni del soggetto e dei provvedimenti irrevocabili. La conoscenza dell’AS IS viene utilizzata per una gap analysis mirata, capace di evitare la replica automatica di funzioni obsolete e di concentrare l’investimento sulle funzioni effettivamente necessarie.

La roadmap massima di 24 mesi comprende l’intero ciclo di trasformazione, fino alla sperimentazione graduale sui tre comparti, alla migrazione definitiva, all’avvio nazionale e allo spegnimento dei sistemi legacy. Il Core SIES è collocato in una forchetta economica preliminare di 3,0-3,5 milioni di euro, mentre Portale esterno e Deleghe alla Polizia Giudiziaria sono mantenuti come lotti successivi e finanziabili separatamente.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th><strong>Risultato atteso<br />
</strong>Una piattaforma nazionale unica, operativa entro 24 mesi per Procure, Sorveglianza e Giudice dell’Esecuzione, con dato centralizzato, processi integrati, interoperabilità nativa e dismissione dei sistemi esistenti.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>
