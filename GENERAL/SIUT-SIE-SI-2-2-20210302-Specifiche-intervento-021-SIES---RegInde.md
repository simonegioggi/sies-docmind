---
uniqueName: siut-sie-si-2-2-20210302-specifiche-intervento-021
displayName: "SIUT SIE SI 2 2 20210302 Specifiche intervento 021 SIES   RegInde"
category: "GENERAL"
tags: []
---

# SIUT-SIE-SI-2.2-20210302-Specifiche-intervento-021-SIES - RegInde

> **File originale:** `MEV/SCHEDA_021/Docs/SIUT-SIE-SI-2.2-20210302-Specifiche-intervento-021-SIES - RegInde.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |







Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Umberto Mignogna | Analista Funzionale |
| Verificato da | Vito Bufi
Alessandro Falleni
Fabio Gattamorta | Responsabile Manutenzione Sistemi attuali
Referente Sicurezza
Referente PMO e Qualità |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 25/01/2021 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 05/08/2020 | Prima Emissione |  |
| 1.1 | 09/10/2020 | Seconda Emissione | Revisione a seguito della e-mail dell’Amministrazione (PO) del 03/09/2020 ore 17:24 – oggetto: ‘SIES Scheda Intervento n.21 Gestione Anagrafica Avvocati - RegInde": 17-SIUT-SIE-SI-1.0-20200805-Specifiche-intervento-021-SIES-RegInde’ :
Al par. 6.1 specificato l’aggiornamento di 4 fori individuati a valle dell’analisi dei dati ReGIndE;
Al par. 6.2.3.1 è stata aggiornata le descrizione della ricerca in caso di searchLimit Exception (punto 3 della e-mail) e descritta la necessità per SIES di visualizzare lo stato dell’Avvocato (punto 6 della e-mail);
Ai par. 6.1.4.1 e 6.2.3.1 sono state inserite le problematiche relative alle tabelle COMUNE di SIES e AVVOCATO di SIES e ReGIndE  e i relativi interventi di soluzione (punto 4 della e-mail);
Al par. 6.2.3.1 pag. 39 è stato precisato che la sovrascrittura dell’indirizzo non rappresenta problema per SIES (punto 5 della e-mail);
Al par. 6.2.5.2 è stato aggiornato il protocollo di sicurezza;
Al par. 6.2.5.7 è stato indicato che ReGIndE fornirà il certificato di chiave pubblica;
Al par. 6.5.1 sono state inserite alcune precisazioni sulle modalità di esecuzione della Bonifica; |
| 2.0 | 15/12/2020 | Terza Emissione | Revisione a seguito della call svoltasi su MS Team tra personale dell’Amministrazione (PO)  e personale del Fornitore in data 10/12/2020 ore 9:30 – oggetto: ‘SIES Scheda Intervento n.21 Gestione Anagrafica Avvocati - RegInde": 17-SIUT-SIE-SI-1.0-20200805-Specifiche-intervento-021-SIES-RegInde’ :
Al par. 6.1  pag. 16 primo capoverso specificato Foro_Avvocati;
Al par. 6.1 pag. 16  specificato che i 4 fori con diversa denominazione dall’attuale saranno trattati con le stesse modalità previste per Napoli Nord;
Al par. 6.2.3.1 pag. 36  specificato che i  risultati saranno filtrati per FORO_AVVOCATI;
par. 6.2.3.1 pag. 38 inserito riferimento a procedura aggiornamento tabelle COMUNE e CG_REF_CODES;
par. 6.2.3.1 pag. 39 specificata la possibilità di inserire manualmente un difensore con codice catastale non presente nella tabella COMUNE aggiornata;
Ai par. 6.2.3.1 pag. 41  specificato che indirizzo sarà sovrascritto anche se non valorizzato su ReGIndE;
Al par. 6.3.3.2 pag. 69 specificate modalità di trattamento avvocato con codice catastale non presente in tabella COMUNE;
Al par. 6.5.1 specificati prerequisiti per attività di bonifica Avvocato;
Alle pagg. 75 e seguenti inserito nuovo cap. 6.6 Aggiornamento Tabelle COMUNE e CF_REF_CODES. |
| 2.1 | 22/1/2021 | Quarta Edizione | Revisione a seguito della call svoltasi su MS Team tra personale dell’Amministrazione (PO)  e personale del Fornitore in data 15/1/2021 ore 16:30 – oggetto: ‘SIES Scheda Intervento n.21 Gestione Anagrafica Avvocati - RegInde": SIUT-SIE-SI-2.0-20201218-Specifiche-intervento-021-SIES-RegInde’ :
Al par. 1.2  pag. 11 nella tabella riferimenti eliminato il documento RIF3  SIGI_PNL_AA_2017 04-12_1.2_ Architettura  SIES.doc perché mai approvato;
Al par. 3.1 pag. 15  eliminata frase con riferimento al documento di cui al precedente punto;
Ai par. 6.2.3.1 pag. 43, par. 6.2.3.2 pag. 52 e par. 6.2.3.3 pag. 62 specificato che in fase di inserimento di un nuovo avvocato importato da ReGIndE il cod_ufficio_appartenenza sarà impostato a ‘00000’;
Al par. 6.2.3.1 pag. 43 specificato comportamento del sistema a seguito scambio dati fra BDI;
Al par. 6.2.3.3 pagg. 61, 64  specificato che l’avvocato del procedimento SIEP selezionato sarà valido anche per il procedimento SIUS;
Al par. 6.2.5.1 pag. 67 inserita precisazione che la fault sarà gestita applicativamente;
Al par. 6.2.7 pag. 67 inserita precisazione relativa alle istruzioni di configurazione;
Ai par. 6.3.3.1 pag. 69  specificato comportamento del sistema in caso di avvocato selezionato da Elenco;
Al par. 6.5.5 pag. 78, in fondo, specificato ‘cancellazione fisica dei records AVVOCATO con ID_AVVOCATO_BONIFICATO valorizzato’;
Ai parr. 6.5.5 pag.78 e 6.6 pag. 79 specificata necessità di eseguire backup prima di inizio attività aggiornamento Base Dati;
Al par. 6.6.1 pag. 80 descritto utilizzo del valore della colonna COD_SEDE_GIUDIZIARIA e aggiornamento tabella CODICI_SIES_NSC con dominio ‘COMUNE’;
Al par. 6.6.1 pag. 81 descritto aggiornamento tabella COMUNI di SIES-Avvocati;
Al par. 6.6.2.1 pag. 82 descritto impatto in SIES dei records PROVINCIA con FINE_VALIDITA = ‘SI’;
Al par. 6.6.2.3 pag. 83 descritto impatto in SIES dei records STATO-NAZIONE con DATA_FINE_VALIDITA valorizzata e aggiornamento tabella CODICI_SIES_NSC con dominio ‘NAZIONE’; 
Al par. 6.6.2.3 pag. 84 descritto aggiornamento tabella STATI di SIES-Avvocati;
Aggiornati parr. 6.6.3, 6.6.5 e 6.6.6; |
| 2.2 | 2/3/2021 | Quinta edizione | Revisione a seguito di richiesta dell’Amministrazione:
Al parr. 6.2.3.1  pag. 38 e seguenti e  al par. 6.2.5.1.pag. 66 eliminati tutti i riferimenti alla ricerca su ReGIndE per ‘like’. |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Salvatore Piazza | RTI |  | Technical Manager |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Fabio Mazzocchi | RTI |  | Responsabile Manutenzione Correttiva |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Referente PMO e Qualità |
| Alessandro Falleni | RTI |  | Referente Sicurezza |
| Francesco Rosati | RTI |  | Referente Qualità e Sicurezza |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |
| Luigi Buglione | RTI |  | Referente Metrico |



INDICE DEI CONTENUTI
1	Introduzione	12
1.1	Scopo del documento	12
1.2	Riferimenti	12
1.3	Glossario	12
1.3.1	Definizioni	12
1.3.2	Acronimi e abbreviazioni	12
2	Definizione dell’Obiettivo	14
3	Architettura del Sistema	15
3.1	Architettura	15
4	Specifiche dei requisiti	15
4.1	Premessa	15
4.2	Elenco Requisiti	16
5	Interfacce	16
6	Descrizione dell’Intervento	17
6.1	REQ-SIE-021-01_FN.01 -  Gestione Nuovi Fori (FORO di NAPOLI NORD)	17
6.1.1	Moduli sw	24
6.1.2	Architettura	28
6.1.3	Interfacce utente	28
6.1.4	Basi dati	31
6.1.4.1	Selezione Lista Fori SIES	31
6.1.4.2	Tabella Avvocati SIES	32
6.1.5	WEB services	32
6.1.6	XSD	32
6.1.7	Configurazione	33
6.1.8	Tutorial	33
6.2	REQ- SIE-021-02_FN.01 -  Ricerca su ReGIndE	33
6.2.1	Moduli sw	34
6.2.2	Architettura	35
6.2.3	Interfacce utente	35
6.2.3.1	Sottosistema SIEP	35
6.2.3.2	Sottosistema SIGE	49
6.2.3.3	Sottosistema SIUS	58
6.2.4	Basi dati	62
6.2.5	WEB services	63
6.2.5.1	Gestione delle fault	65
6.2.5.2	Altre specifiche per il servizio	65
6.2.6	XSD	65
6.2.7	Configurazione	65
6.2.8	Tutorial	65
6.3	REQ- SIE-021-03_FN.01 – Inserimento Manuale: Indisponibilità ReGIndE o Avvocato Non Presente	65
6.3.1	Moduli sw	66
6.3.2	Architettura	66
6.3.3	Interfacce utente	66
6.3.3.1	Inserimento manuale: Indisponibilità ReGIndE o Avvocato Non Presente	66
6.3.3.2	Inserimento manuale avvocato sul sistema SIES	68
6.3.4	Basi dati	70
6.3.5	WEB services	70
6.3.6	XSD	70
6.3.7	Configurazione	70
6.3.8	Tutorial	70
6.4	REQ- SIE-021-04_FN.01 – Interventi su Funzioni SIES di Gestione Avvocati	70
6.4.1	Moduli sw	71
6.4.2	Architettura	71
6.4.3	Interfacce utente	71
6.4.4	Basi dati	72
6.4.5	WEB services	72
6.4.6	XSD	72
6.4.7	Configurazione	72
6.4.8	Tutorial	72
6.5	REQ- SIE-021-05_FN.01 – Bonifica Anagrafica Avvocati SIES	72
6.5.1	Bonifica dei dati presenti nella tabella Avvocato	72
6.5.2	Moduli sw	74
6.5.3	Architettura	74
6.5.4	Interfacce utente	74
6.5.5	Basi dati	74
6.5.6	WEB services	76
6.5.7	XSD	76
6.5.8	Configurazione	76
6.5.9	Tutorial	76
6.6	REQ- SIE-021-06_FN.01 – Aggiornamento Tabelle COMUNE e CG_REF_CODES di SIES	76
6.6.1	Aggiornamento dei dati presenti nella tabella COMUNE di SIES	76
6.6.2	Aggiornamento dei dati presenti nella tabella CG_REF_CODES (domini PROVINCIA,REGIONE,NAZIONE)	79
6.6.2.1	Aggiornamento dominio PROVINCIA	79
6.6.2.2	Aggiornamento dominio REGIONE	80
6.6.2.3	Aggiornamento dominio NAZIONE	80
6.6.3	Moduli sw	82
6.6.4	Architettura	82
6.6.5	Interfacce utente	82
6.6.6	Basi dati	84
6.6.7	WEB services	84
6.6.8	XSD	84
6.6.9	Configurazione	84
6.6.10	Tutorial	84

Figura 1: Architettura del sistema SIES	15
Figura 2: Sezione notifica Difensore	19
Figura 3: Alert per Comune non Esistente	19
Figura 4: Form ricerca su ReGinE	19
Figura 5: Combo-box dei fori	20
Figura 6: [Esempio Template 1]	21
Figura 7: [Esempio Template 2]	22
Figura 8: Alert per variazione foro	23
Figura 9: Form di dettaglio procedimento	23
Figura 10: Form di esempio per messaggio di warning	24
Figura 11: Sezione destinatario Notifica - SIEP	29
Figura 12: Sezione destinatario Notifica - SIUS	30
Figura 13: Sezione destinatario Notifica - SIGE	31
Figura 14: Form inserimento difensore procedimento SIEP - nuova	37
Figura 15: Form di attivazione ricerca su ReGIndE	38
Figura 16: Form di ricerca su ReGIndE con segnalazione di eccessive occorrenze con criteri impostati	39
Figura 17: Form Elenco Avvocati ReGIndE	39
Figura 18: Form dettaglio Avvocato selezionato	41
Figura 19: Form dettaglio avvocato procedimento SIEP	43
Figura 20: Form sostituzione Difensore procedimento SIEP	44
Figura 21: Form Iscrizione Istanza da Soggetto - Attuale	45
Figura 22: popup Ricerca e seleziona Avvocato SIES	46
Figura 23: Form Iscrizione Istanza da Titolo Esecutivo - Attuale	47
Figura 24: Form Iscrizione Istanza da Procedimento SIEP	48
Figura 25: Form sostituzione Assegnazione Difensore procedimento SIGE - Attuale	49
Figura 26: Form sostituzione Assegnazione Difensore procedimento SIGE - Nuova	50
Figura 27: Form Dettaglio Difensore procedimento SIGE - Attuale	51
Figura 28: Form Dettaglio Difensore procedimento SIGE - Nuova	52
Figura 29: Form Sostituzione Difensore procedimento SIGE - Nuova	53
Figura 30: Form Inserimento Difensore procedimento SIGE – Parti in causa	54
Figura 31: Form Inserimento Difensore Parte	55
Figura 32: Form Dettaglio Fissazione Udienza procedimento SIGE	56
Figura 33: Form Inserimento Difensore procedimento SIGE Parti in causa - Nuova	57
Figura 34: Form Assegnazione Difensore procedimento SIUS - Attuale	58
Figura 35: Form Assegnazione Difensore procedimento SIUS - Nuova	59
Figura 36: Form Dettaglio Difensore procedimento SIUS - Attuale	61
Figura 37: Form Dettaglio Difensore procedimento SIUS - Nuova	61
Figura 38: Form Sostituzione Difensore procedimento SIUS - Nuova	62
Figura 39: Form Ricerca Difensore su ReGIndE in caso di assenza collegamento	66
Figura 40: Form Ricerca Difensore su ReGIndE in caso nessun occorrenza trovata	67
Figura 41: Form Elenco Avvocati SIES	67
Figura 42: Form Esito Ricerca Difensori SIES in caso di nessun occorrenza trovata	68
Figura 43: Form Inserimento Difensore in SIES	69
Figura 44: Form Gestione Difensori - Attuale	71
Figura 45: Form Gestione Difensori - Nuova	71
Figura 46: Form Elenco Difensori - Attuale	72
Figura 47: Form Elenco Difensori - Nuova	72


Introduzione
## Scopo del documento
Il presente documento riporta le specifiche di intervento sul software, metodologia WATERFALL, al fine di soddisfare i requisiti espressi dall’Amministrazione e descritti nella scheda di intervento SIUT-SIE-SC-1.3-20200616 Scheda intervento Scheda_n.21_SIES_ReGIndE.pdf.

## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF1 | SIUT-SIE-SC-1.3-20200616 Scheda intervento Scheda_n.21_SIES_ReGIndE.pdf | Scheda di intervento |
| RIF2 | m_dg.DOG07AR.14/07/2020.0001154.U | Approvazione scheda intervento |


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


Definizione dell’Obiettivo

L’intervento in oggetto è stato richiesto con comunicazione m_dg.DOG07AR.27_09_2019.0000056.U  e rientra nel servizio di Manutenzione Evolutiva.

Tale documento espone gli interventi attinenti alle funzioni da prevedere nel sistema SIES con lo scopo finale di ‘abilitare’ i vari sistemi distrettuali del SIES all’interconnessione con il sistema del Registro Generale degli Indirizzi Elettronici, in modo da avere un’entità DIFENSORE ‘certificata’, e nello stesso tempo di introdurre la gestione dei nuovi fori in particolare la gestione del FORO di NAPOLI NORD.

L’intervento mira ad una gestione coerente ed auto consistente dell’entità DIFENSORE nell’interezza di tutto il sistema SIES, pertanto le varie dinamiche di implementazione saranno relative ai tre sottosistemi SIEP, SIUS e SIGE.

Si fa presente che nel prosieguo del documento si farà sempre riferimento ad un’interconnessione, del SIES verso il ReGIndE, in una modalità di tipo ‘diretta’, ossia il sistema SIES, per le casistiche previste dai requisiti, farà un accesso diretto ai servizi esposti dal sistema del Registro Generale degli Indirizzi Elettronici tramite invocazione dei metodi necessari sugli appositi endpoint pubblicati su rete giustizia.
Si esplicita che in un’ottica di implementazione del concetto di ‘Anagrafica Centralizzata’ nell’ambito della reingegnerizzazione del sistema penale in conformità anche al disegno architetturale generale proposto per il progetto Beccaria, quanto specificato in tale documento potrebbe necessitare di attività di refactory, una volta stabilizzata l’architettura Beccaria definitiva.


















Architettura del Sistema
## Architettura
L’intervento in oggetto non introduce variazioni architetturali, rispetto al sistema attuale. Si riporta a titolo esemplificativo lo schema generale attuale del singolo sistema distrettuale del SIES.


Figura 1: Architettura del sistema SIES


Specifiche dei requisiti
## Premessa
Sulla base degli applicativi oggetto del contratto e delle aree funzionali, la convenzione per l’identificazione dei requisiti è riportata di seguito.
Ciascun requisito è individuato da un identificativo univoco nella forma [REQ-SIS-nnn-mm_ZZ.pp], dove la parte evidenziata in grigio riporta il macro-requisito espresso dall’Amministrazione e codificato nella scheda di intervento, i restanti caratteri identificano rispettivamente:

ZZ il tipo requisito (vedere la tabella di seguito riportata);
pp il progressivo requisito nell’ambito del tipo requisito.
| Tipo Requisito | Descrizione |
| --- | --- |
| AM | Ambientale |
| AR | Architetturale |
| CF | Configurazione |
| ES | Esecuzione |
| FN | Funzionale |
| UI | Interfaccia Utente |
| PR | Prestazionali |
| IN | Interoperabilità |
| SC | Sicurezza |
| SI | Sistema |
| TU | Tutorial |
| RG | Relazione Giuridica |


## Elenco Requisiti
| Codice Requisito | Descrizione | Riferimenti |
| --- | --- | --- |
| REQ-SIE-021-01_FN.01 | Gestione Nuovi Fori (FORO di NAPOLI NORD) |  |
| REQ-SIE-021-02_FN.01 | Ricerca su ReGIndE |  |
| REQ-SIE-021-03_FN.01 | Inserimento Manuale: Indisponibilità ReGIndE o Avvocato Non Presente |  |
| REQ-SIE-021-04_FN.01 | Interventi su Funzioni SIES di Gestione Avvocati |  |
| REQ-SIE-021-05_FN.01 | Bonifica Anagrafica Avvocati SIES |  |


Interfacce
Nel caso fossero oggetto della modifica, le interfacce interessate dall’intervento saranno riportate all’interno dei paragrafi che descrivono ciascun intervento.
Le immagini riportate hanno lo scopo di facilitare la comprensione dell’intervento, ma potrebbero differire dalle effettive maschere dell’applicativo.
Descrizione dell’Intervento
In riferimento ai tre sottosistemi di cui si compone l’applicativo SIES è fatta richiesta:

di integrare la gestione di nuovi fori (es. Napoli Nord);
di integrare la ricerca dell’avvocato da associare al procedimento SIEP, SIUS e SIGE andando a recuperare i dati dello stesso dal sistema ReGIndE (Registro Generale degli Indirizzi Elettronici);
di bonificare i dati pregressi, presenti nella tabella Avvocato di SIES, in base ai dati presenti su ReGIndE, al fine di rendere univoci i record delle anagrafiche degli avvocati.

In maniera schematica, si riportano i principali punti che costituiscono l’intervento in oggetto:
Inserimento e gestione nuovi fori, in particolare integrazione del foro di Napoli Nord nelle forms del sistema e nei template che utilizzano l’entità foro avvocato [REQ-SIE-021-01_FN.01];
Modifica pagine per creazione link alla nuova funzione di ricerca su ReGIndE [REQ-SIE-021-02_FN.01];
Realizzazione Funzione di Ricerca su ReGIndE [REQ-SIE-021-02_FN.01];
Inserimento manuale su SIES, per indisponibilità ReGIndE o non trovato su ReGIndE [REQ-SIE-021-03_FN.01];
Modifica dell’attuale comportamento del sistema per la gestione degli avvocati in modo da evitare la duplicazione delle anagrafiche nella tabella AVVOCATO: disattivazione delle funzioni di Inserimento e Modifica Difensore [REQ-SIE-021-04_FN.01];
Bonifica dati pregressi al fine di rendere univoci i record delle anagrafiche degli avvocati [REQ-SIE-021-05_FN.01]:
la bonifica sarà realizzata per tutte le anagrafiche avvocato già presenti su SIES che risultino associate ad almeno un fascicolo con procedimenti in corso.
Per dette anagrafiche, i dati SIES saranno aggiornati con i dati di ReGIndE, a parità di anagrafica trovata.
Tutti i record bonificati saranno contraddistinti dal valore ‘Sì’ del FLAG_REGINDE.

In generale, l’intervento vede come premessa le seguenti regole:
tutti gli avvocati aventi FLAG_REGINDE = ‘SI’ NON devono essere oggetto di alcuna modifica nell’ambito del sistema SIES, considerando i dati provenienti da ReGIndE dati certificati;
tutti gli avvocati aventi FLAG_REGINDE = ‘NO’ NON devono essere più gestiti in alcun modo nel sistema SIES, fatta eccezione per quel che concerne l’attivazione degli alert descritti nei paragrafi successivi.

## REQ-SIE-021-01_FN.01 -  Gestione Nuovi Fori (FORO di NAPOLI NORD)
Il requisito espresso dall’Amministrazione determina un intervento evolutivo per la gestione di un nuovo foro.
Per la descrizione della soluzione si farà riferimento, come esempio, al FORO di NAPOLI NORD.
Si precisa che la soluzione di seguito dettagliata garantirà la gestione di altri eventuali nuovi fori nei tre sottosistemi SIES.
La soluzione per la realizzazione di quanto richiesto verterà nello ‘svincolare’ l’entità del FORO dalla tabella COMUNE, facendo in modo che il dominio ‘FORO_AVVOCATI’, presente nella tabella CG_REF_CODES, sia indipendente ed auto consistente.
Il dominio ‘FORO_AVVOCATI’ sarà ‘responsabile’ di mappare la descrizione del FORO ed il codice del comune sede del FORO (Codice ISTAT).

Il FORO AVVOCATI, così come dettagliato al par. 6.2, sarà utilizzata quale dato di ricerca per l’interrogazione dei servizi web esposti da ReGIndE.

Si segnala che la soluzione che si adotterà in relazione alla risoluzione della problematica FORO NAPOLI NORD non avrà impatto con la gestione già in essere sul sistema SIES del comune NAPOLI NORD, censito nella tabella COMUNE con codice ISTAT fittizio.
Pertanto, il comportamento attuale del sistema circa l’utilizzo dell’entità comune NAPOLI NORD NON SARA’ in alcun modo modificato con l’introduzione della gestione del nuovo FORO NAPOLI NORD.

Il perimetro dell’intervento per l’inserimento e la gestione del nuovo foro attiene esclusivamente all’entità FORO e alla sua relazione con l’AVVOCATO.
Ciò significa che l’entità FORO sarà gestita in tutte le pagine che ad oggi già utilizzano l’informazione del foro di appartenenza di un DIFENSORE, ossia nelle pagine ove è prevista la notifica al DIFENSORE tramite UNEP.

Dalla analisi dei dati relativi all’ultima tabella degli Avvocati estratta da ReGIndE (tabellefisse18novembre2020.xlsx), inviata dall’Amministrazione – Area Civile, è emerso quanto segue:

in ReGIndE sono presenti due fori che pur riferiti nel COA ai Comuni di Forlì (COA040012) e Massa (COA045010) hanno una Descrizione non riferita solo al Comune, infatti fanno riferimento rispettivamente al Foro di FORLÌ-CESENA ed al Foro di MASSA CARRARA, mentre in SIES sono gestiti come Foro di Forlì e Foro di Massa.

in ReGIndE sono presenti i due fori di REGGIO CALABRIA (COA080063) e REGGIO EMILIA  (COA035033), la cui descrizione non corrisponde alla descrizione ufficiale dei comuni, rispettivamente REGGIO DI CALABRIA e REGGIO NELL’EMILIA .

Tali Fori (foro di FORLÌ-CESENA, foro di MASSA CARRARA, foro di REGGIO CALABRIA e foro di REGGIO EMILIA) saranno gestiti in SIES con le stesse modalità previste per il foro di NAPOLI NORD, cioè svincolando la descrizione del FORO dalla descrizione del Comune Sede. I records della tabella AVVOCATO di SIES aventi la colonna FORO valorizzata con le attuali descrizioni (Forlì, Massa, Reggio di Calabria, Reggio nell’Emilia)  saranno aggiornate con le descrizioni utilizzate in ReGIndE.

Nello specifico, nelle varie maschere e template che riportano la descrizione del foro, saranno visualizzate le nuove descrizioni in sostituzione di quelle attuali previste dal SIES. Il codice Istat del comune di riferimento resta invece invariato.


Di seguito la schematizzazione per punti di quanto sarà realizzato:

Per le notifiche al DIFENSORE si utilizzerà come descrizione del FORO associato all’Avvocato quella prevista, cioè NAPOLI NORD [vedere testo sottolineato figura 2]; come sede dell’autorità UNEP relativa al Foro di Napoli Nord, invece, si farà riferimento al comune di AVERSA [vedere riquadro nella figura 2];


Figura 2: Sezione notifica Difensore

Tutti i template che riportano l’informazione della sede UNEP, nei casi in cui la notifica sia inviata ad un avvocato del FORO NAPOLI NORD, mostreranno, ove previsto, come sede di riferimento il comune di AVERSA [vedere immagini di Esempio Template 1 e 2 riportate di seguito];

Per le notifiche al DIFENSORE sarà bloccato il salvataggio della coppia Autorità Destinazione/sede Napoli Nord, per qualsiasi autorità selezionata, con il seguente messaggio:


Figura 3: Alert per Comune non Esistente

Le form che presentano la combo dei fori, in automatico mostreranno la nuova lista dei fori ‘arricchita’ con il nuovo foro ‘NAPOLI NORD’:



Figura 4: Form ricerca su ReGinE

nella combo box Foro sarà presente anche il nuovo foro


Figura 5: Combo-box dei fori

I tre sottosistemi saranno allineati a quanto detto ai punti 1, 2, 3 e 4.

A seguire un esempio di template che contemplano la modifica relativa alla gestione del foro di NAPOLI NORD.




Figura 6: [Esempio Template 1]



Figura 7: [Esempio Template 2]


Nell’ambito della realizzazione del requisito di gestione di un nuovo foro, si rende necessario salvaguardare i dati pregressi relativi ai procedimenti in corso. Considerando la possibilità che un avvocato possa avere una variazione di foro di appartenenza, il sistema gestirà la storicizzazione dell’associazione Anagrafica Avvocato/Foro di Appartenenza già esistente.

Nello specifico, a fronte di un’attività di bonifica dei dati, quindi di un ‘match’ tra i dati presenti sulla tabella AVVOCATI del SIES e dei dati presenti nella tabella ‘SOGGETTI’ del sistema ReGIndE, supponiamo di individuare un dato avvocato che ha tutte le corrispondenze uguali in entrambe le tabelle a meno del foro di appartenenza. In questo caso non si procederà alla bonifica del dato su SIES, ma per il record individuato sarà impostato il campo FLAG_REGINDE =’NO’ ed inoltre sarà settata la data_fine_validità in quanto l’associazione anagrafica avvocato/foro non è più esistente.

Per tali casistiche, sulla pagina di dettaglio del fascicolo sarà attivato, per i dati storicizzati a causa della variazione del Foro e non bonificati (FLAG_REGINDE =’NO’), un alert che NON costituirà errore bloccante ma sarà semplicemente un avviso per l’utente, il quale dovrà procedere a rieseguire l’associazione del difensore al fascicolo in lavorazione, dal momento che il foro di appartenenza risulta variato.
Per le modalità di visualizzazione dell’alert sarà seguita la stessa logica utilizzata per la Nuova Geografia Giudiziaria.

Per cui se si accede al Dettaglio del procedimento SIEP si riceverà prima il seguente messaggio


Figura 8: Alert per variazione foro

e successivamente alla conferma nella form di Dettaglio saranno evidenziati in giallo (blinkante) il Cognome, Nome ed il Foro di appartenenza.


Figura 9: Form di dettaglio procedimento

Se non si procede alla certificazione dell’avvocato, un messaggio di warning sarà riportato su tutte le form di emissione provvedimento, es.

Figura 10: Form di esempio per messaggio di warning

Riassumendo quindi i punti di intervento per la gestione del nuovo foro Napoli Nord sono:

Caratterizzazione del dominio FORO_AVVOCATO su cg_refs_code;
Censimento del nuovo foro nel dominio su specificato;
Intervento su ogni pagina su elencata per ‘aggiornare’ la sezione relativa alla notifica al difensore;
Implementare per ogni pagina su elencata, i controlli che bloccano il salvataggio della coppia UNEP + comune Napoli nord;
Gestire l’Alert dell’avvocato sulla pagina di dettaglio del procedimento;
Gestire il messaggio di ‘avviso warning’ nelle pagine del SIES;

## Moduli sw
Modifica di tutte le seguenti jsp contenenti tra le autorità destinatarie l’UNEP per la notifica agli avvocati per svincolare il Foro dalla sede:

siep
calcolopena
LoadEmissioneProvvedimento.jsp (2 matches)
LoadInsComNuovoResPenaRidetPenaAltro.jsp (2 matches)
LoadInserisciComputoCustodiaCautelare.jsp (2 matches)
LoadInserisciFungibilita.jsp (2 matches)
LoadInsOSNuovoResPenaRidetPenaAltro.jsp (2 matches)
LoadInsOSNuovoResPenaRidetPenaRidimLA.jsp (2 matches)
LoadRidetPenaAltro.jsp (2 matches)
cumulo
LoadInserisciStampaCumulo.jsp (2 matches)
liberazioneanticipata
LoadInsericiComunicazioneErgastolo.jsp (2 matches)
LoadInsericiComunicazioneLibero.jsp (2 matches)
LoadInserisciComunicazioneReclamoRimediRisarcitori.jsp (2 matches)
LoadInserisciComunicazioneRimediRisarcitori.jsp (2 matches)
LoadInserisciOSRimediRisarcitori.jsp (2 matches)
misuraalternativa
LoadInserisciAmmissioneADetDom.jsp (2 matches)
LoadInserisciCessazioneMA.jsp (2 matches)
LoadInserisciCessazioneMAAffProva.jsp (2 matches)
LoadInserisciConcessione.jsp (2 matches)
LoadInserisciMAAmmDetDomSpeAff.jsp (2 matches)
LoadInserisciMAAmmisioneProvvisoria.jsp (2 matches)
LoadInserisciMACessazione51bis.jsp (2 matches)
LoadInserisciMACoLibCond.jsp (2 matches)
LoadInserisciMADetDomSpecAmmiPeriodo.jsp (2 matches)
LoadInserisciMADetDomSpecSospProvv.jsp (2 matches)
LoadInserisciMADetDomTemp.jsp (2 matches)
LoadInserisciMADicEffAffInProva.jsp (2 matches)
LoadInserisciMAProrogaUltPeriodo.jsp (2 matches)
LoadInserisciMAProsecuzione.jsp (2 matches)
LoadInserisciMAProsecuzione51bis.jsp (2 matches)
LoadInserisciMAReLibCond.jsp (2 matches)
LoadInserisciRevocaMA.jsp (2 matches)
LoadInserisciRevocaMAAffProva.jsp (2 matches)
LoadInserisciRigetto.jsp (2 matches)
LoadInserisciRipristinoDetDonSpec.jsp (2 matches)
LoadInserisciUlteriorePeriodoMA.jsp (2 matches)
LoadInsRevocaArrestiDomiciliari.jsp (2 matches)
LoadVariazioneMADecSca.jsp (2 matches)
misurasicurezza
LoadInserisciArchiviazioneManuale.jsp (2 matches)
LoadInserisciArchiviazionePerProvvAltroUfficio.jsp (2 matches)
LoadInserisciArchiviazionePerProvvGEsecuzione.jsp (2 matches)
LoadInserisciArchiviazionePerProvvGiudiceCassazione.jsp (2 matches)
LoadInserisciArchiviazionePerProvvSorveglianza.jsp (2 matches)
LoadInserisciComunicazionePolizia.jsp (2 matches)
LoadInserisciOEInternamento.jsp (2 matches)
LoadInserisciOLDifferimento.jsp (2 matches)
LoadInserisciOLDifferimentoDecreto.jsp (2 matches)
LoadInserisciOrdinediConsegna.jsp (2 matches)
LoadInserisciOrdineLiberazione.jsp (2 matches)
LoadModificaArchiviazioneManualeMS.jsp (3 matches)
LoadModificaArchiviazionePerProvvAltroUfficioMS.jsp (3 matches)
LoadModificaArchiviazionePerProvvGEsecuzioneMS.jsp (3 matches)
LoadModificaArchiviazionePerProvvGiudiceCassazione.jsp (3 matches)
LoadModificaArchiviazionePerProvvSorveglianzaMS.jsp (3 matches)
LoadModificaComunicazioneOrdineConsegnaMS.jsp (3 matches)
LoadModificaOEInternamentoOrdineLiberazioneMS.jsp (3 matches)
LoadModificaOLDifferimento.jsp (3 matches)
LoadModificaOLDifferimentoDecreto.jsp (3 matches)
ordineesecuzione
LoadInserisciComunicazioneL78del2013.jsp (2 matches)
LoadInserisciDecretoSospensioneAlfanoLibero.jsp (2 matches)
LoadInserisciOERidetPenaAltro.jsp (2 matches)
LoadInserisciOrdineEsecuzione.jsp (2 matches)
LoadInserisciOrdineEsecuzioneAlfanoLibero.jsp (2 matches)
LoadInserisciOrdineEsecuzioneAlfanoNonLibero.jsp (2 matches)
LoadInserisciOrdineEsecuzioneL78del2013.jsp (2 matches)
LoadInserisciOrdineEsecuzioneSanSos.jsp (2 matches)
LoadInserisciOrdineEsecuzioneSimeone.jsp (2 matches)
LoadInserisciOrdineEsecuzioneSimeoneSanSos.jsp (2 matches)
LoadInserisciRevocaSospensioneAlfano.jsp (2 matches)
LoadInserisciRevocaSospensioneSimeone.jsp (2 matches)
LoadInserisciVariazioneDecorrenzaScadenza.jsp (2 matches)
LoadInserisciVariazioneDecorrenzaScadenzaQC.jsp (2 matches)
ordinescarcerazione
LoadInserisciOSLiberazioneAnticipata.jsp (2 matches)
revoca
LoadInserisciOrdineEsecuzioneRevoca.jsp (2 matches)
sanzionesostitutiva
LoadInserisciAnnotazione.jsp (2 matches)
LoadInserisciRideterminazionePenaRevocaSS.jsp (2 matches)
sospensione
LoadInserisciAccoglimentoOpEspulsione.jsp (2 matches)
LoadInserisciComunicazioneEspulsione.jsp (2 matches)
LoadInserisciDecretoSospensione.jsp (2 matches)
LoadInserisciDifferimentoOE.jsp (2 matches)
LoadInserisciEspulsioneConcessione.jsp (2 matches)
LoadInserisciNotificheDifferimento.jsp (2 matches)
LoadInserisciNotificheEspulsione.jsp (2 matches)
LoadInserisciRigettoOpEspulsione.jsp (2 matches)
LoadInserisciRinunciaOpEspulsione.jsp (2 matches)
LoadInserisciSospensioneEsecPenaDispPm.jsp (2 matches)
LoadInserisciSospensioneOE.jsp (2 matches)
LoadInserisciSospensionePena.jsp (2 matches)
sige
impugnazione
LoadInserisciEsitoImpugnazioneSige.jsp (2 matches)
provvedimento
InserisciAvvocati.jsp (2 matches)
InserisciNotificaSoggettoPressoDifensore.jsp
LoadEmissioneOrdinanzaSospensione.jsp (2 matches)
LoadInserisciDataDeposito.jsp (2 matches)
provvInterlocutori
LoadInserisciCitazioneTesti.jsp (2 matches)
LoadInserisciNominaPeriti.jsp (2 matches)
udienza
LoadInserisciFissazioneUdienza.jsp (2 matches)
sius
depositodecreto
InserisciAvvocati.jsp (2 matches)
depositoordinanzapc
LoadInserisciRimessioneAtti.jsp (2 matches)
depositosentenza
LoadInserisciRimessioneAtti.jsp (2 matches)
ModificaRimessioneAtti.jsp (2 matches)
udienza
LoadInserisciFissazioneUdienza.jsp (2 matches)

Modifica di tutti i seguenti metodi per inibire l’accoglimento tra le sedi del foro dei comuni con FLAG_VALIDITA a ‘N’ (es. NAPOLI NORD):

sico
libertaanticipata > action
ActInserisciComunicazioneLAErgastolo.java
ActInserisciComunicazioneLALibero.java
ActInserisciComunicazioneReclamoRimediRisarcitori.java
ActInserisciComunicazioneRimediRisarcitori.java
ActInserisciOSRimediRisarcitori.java
siep
ordineesecuzione > action
ActOrdineEsecuzione.java (metodi setNotificheOrdineEsecuzione(), setNotificheL78del2013(), setNotificheVariazioneDecorrenzaScadenza()) x tutte le jsp per "ordineesecuzione"
ActInserisciVariazioneDecorrenzaScadenzaQC.java (metodo setNotificheVariazioneDecorrenzaScadenzaQC())
calcolopena > action
ActInsComNuovoResPenaRidetPenaAltro.java
ActCalcoloPena.java (metodo setNotificheAnnotazioniManuali())
ActInserisciOSRidetPenaAltro.java (metodo setNotifiche())
ActInserisciOSRidetPenaRidimLA.java (metodo setNotifiche())
ActRidetPena.java (metodo setNotificheMisuraAlternativa())
cumulo > action
ActCumulo.java (metodo setNotificheCumuloStampa(...))
misuraalternativa > action
ActMisuraAlternativa.java (metodi setNotificheMisuraAlternativa(), setNotificheRevocaArrestiDomiciliariMisuraAlternativa()) x tutte le jsp per "misuraalternativa"
ActVariazioneMADecSca.java
misurasicurezza > action
ActInserisciArchiviazioneManuale.java
ActInserisciArchiviazionePerProvvSorveglianza.java
ActInserisciArchiviazionePerProvvAltroUfficio.java
ActInserisciArchiviazionePerProvvGEsecuzione.java
ActInserisciArchiviazionePerProvvGiudiceCassazione.java
ActInserisciArchiviazionePerProvvSorveglianza.java
ActInserisciComunicazionePolizia.java
ActInserisciOEInternamento.java
ActInserisciOLDifferimento.java
ActInserisciOLDifferimentoDecreto.java
ActInserisciOrdinediConsegna.java
ActInserisciOrdineLiberazione.java
ActNotificheMS.java (metodo setNotificheMS(...)) x tutte le jsp di modifica per "misurasicurezza"
ordinescarcerazione > action
ActInserisciOSLiberazioneAnticipata.java
revoca > action
ActInserisciOrdineEsecuzioneRevoca.java (metodo setNotifiche(...))
sanzionesostitutiva > action
ActInserisciRideterminazionePenaRevocaSS.java
sospensione > action
ActInserisciDecretoSospensione.java
ActInserisciDifferimentoOE.java (metodo setNotifiche())
ActInserisciNotificheDifferimento.java
ActInserisciNotificheEspulsione.java
ActInserisciSospensioneEsecPenaDispPm.java
ActInserisciSospensioneOE.java
ActInserisciSospensionePena.java
sige
provvedimento > action
ActInserisciDataDepositoProvvedimento.java (metodo leggiNotificheAvvocatiAltroDestinatario(...))
ActInserisciOrdinanzaSospensione.java (metodo creaListaDestinatariNotifiche(...))

## Architettura
N.A.
## Interfacce utente
Poiché le form interessate alla modifica descritta al punto 6.1.1 sono numerose, di seguito si riporta come esempio una form per ciascun sottosistema, il sistema a differenza di quanto avviene adesso, che valorizza il comune con il nome del foro, valorizzerà il comune in base al codice Istat presente nella colonna RV_ALT2_VALUE del record della tabella CG_REF_CODES con RV_DOMAIN = ‘FORO_AVVOCATI’.

SIEP

Figura 11: Sezione destinatario Notifica - SIEP



SIUS

Figura 12: Sezione destinatario Notifica - SIUS


SIGE

Figura 13: Sezione destinatario Notifica - SIGE

## Basi dati
### Selezione Lista Fori SIES
Per svincolare la descrizione del Foro di appartenenza di un avvocato (es: NAPOLI NORD) dal comune sede del circondario competente (es: AVERSA), nella tabella CG_REF_CODES in corrispondenza del dominio ‘FORO_AVVOCATI' sarà prevista la valorizzazione della colonna ‘RV_ALT2_VALUE’ che conterrà il codice Istat della sede (comune) di riferimento del foro (es: 061005). La valorizzazione sarà effettuate su tutti i records del suddetto dominio.
La lista dei fori sarà recuperata dalla tabella CG_REF_CODES in corrispondenza del dominio ‘FORO_AVVOCATI'.

Per la valorizzazione della colonna RV_ALT2_VALUE per tutti i records della CG_REF_CODES con RV_DOMAIN = ‘FORO_AVVOCATI’ e riferiti a sedi giudiziarie non soppresse sarà realizzato ed eseguito uno specifico script (valorizza_codcomune_FORO_AVVOCATI.sql), che per ciascun record della tabella CG_REF_CODES avente RV_DOMAIN = ‘FORO_AVVOCATI’, recupererà nella tabella COMUNE il COD_COMUNE per il record avente DESCRIZIONE = RV_LOW_VALUE del record corrente della CG_REF_CODES e per lo stesso valorizzerà la colonna RV_ALT2_VALUE = COD_COMUNE.

Si fa presente che, a seguito dell’analisi dei dati dell’ultima tabella Avvocati estratta da ReGIndE (tabellefisse18novembre2020.xlsx), inviata dall’Amministrazione – Area Civile, i codici comune (codice Istat), utilizzati in ReGIndE per la costruzione del COA, sono tutti presenti e corrispondenti a quelli della tabella COMUNE di SIES.
Tali valori, pertanto, saranno utilizzati per valorizzare il Codice Istat del Comune sede del Foro (RV_ALT2_VALUE) nel Dominio FORO_AVVOCATI della CG_REF_CODES di SIES.

Per l’inserimento del nuovo foro di Napoli Nord sarà eseguito uno script del tipo inserisci_FORO_NAPOLI_NORD.sql, che inserirà un nuovo record nella tabella CG_REF_CODES per il dominio FORO_AVVOCATI, valorizzando tutte le colonne del record con i valori necessari.

Per la rettifica del nome degli attuali fori di FORLI’, MASSA, REGGIO DI CALABRIA e REGGIO NELL’EMILIA   rispettivamente in FORLI’ – CESENA, MASSA – CARRARA, REGGIO CALABRIA e REGGIO EMILIA   sarà eseguito uno script di aggiornamento della colonna RV_MEANING nella tabella CG_REF_CODES per il dominio FORO_AVVOCATI, per ciascuno dei suddetti records.

### Tabella Avvocati SIES
Per il requisito in oggetto la tabella ‘AVVOCATO’ del SIES avrà un ulteriore attributo: FLAG_REGINDE, che consentirà di distinguere i dati delle anagrafiche degli avvocati importati da ReGIndE da quelli inseriti manualmente su SIES.

I possibili valori saranno:
“SI”  Inserito da ReGIndE;
“NO”  Inserito su SIES.

## WEB services
N.A.
## XSD
N.A.
## Configurazione
N.A.
## Tutorial
N.A.

## REQ- SIE-021-02_FN.01 -  Ricerca su ReGIndE

Il requisito prevede l’implementazione della nuova funzione “Seleziona da ReGIndE”, che consenta in fase di inserimento/assegnazione dell’avvocato, di ricercarlo sulla Base Dati di ReGIndE.
La funzione in oggetto sarà attivata sui tre sottosistemi del SIES, in tutte le form che consentono la ricerca dell’avvocato e la sua associazione ad un procedimento.

Tale funzione, secondo specifica richiesta dell’Amministrazione, sarà la prima opzione di ricerca disponibile per l’utente che debba procedere all’eventuale inserimento di un nuovo avvocato e/o all’associazione di un avvocato ad un procedimento.
Pertanto, la funzione di ricerca attualmente presente sul SIES, che va a consultare la tabella proprietaria degli avvocati, sarà attivata in alternativa alla ricerca di nuova realizzazione, solo e soltanto nel caso di indisponibilità del sistema ReGIndE o nel caso di avvocato non trovato su ReGIndE [Rif. § “6.3 REQ-SIE-021-03_FN.01 - Inserimento Manuale: Indisponibilità ReGIndE o Avvocato Non Presente”).

Di seguito sono riportate, per ciascun sottosistema di SIES, le funzionalità che saranno oggetto di modifica per l’inserimento della Ricerca dell’Avvocato su ReGIndE:

SIEP
Assegnazioni  Difensore;
Assegnazione Difensore (funzione presente nella Form Dettaglio Procedimento SIEP);
Elenco Difensori  Sostituzione (funzione presente nella Form Dettaglio Procedimento SIEP);
Nuova Istanza  Iscrizione da Soggetto, Iscrizione da Titolo Esecutivo, Iscrizione da Procedimento
SIEP;
SIUS
Assegnazione Difensore (funzione presente nella Form Dettaglio Procedimento SIUS);
Elenco Difensori  Sostituzione (funzione presente nella Form Dettaglio Procedimento SIUS);
Udienza  Fissazione Udienza (nella Form è presente il link “Inserimento Difensore”);
Ordinanze  Emissione Ordinanza (nella Form è presente il link “Inserimento Difensore”);
Decreti  Emissione Decreti (nella Form è presente il link “Inserimento Difensore”);
SIGE
Assegnazione Difensore (funzione presente nella Form dettaglio procedimento SIGE);
Ordinanze/Deposito/Notifiche (per tutte le voci dei sottomenu);
Nomina Periti/Citazioni Testi (per tutte le voci dei sottomenu);
Udienze/Fissazione/Rinvio/Ruolo (per tutte le voci dei sottomenu);
Decreti/Deposito/Notifiche (per tutte le voci dei sottomenu).

## Moduli sw
Di seguito l’elenco delle jsp da modificare, suddivise per sottosistema:

siep
avvocato
DettaglioAvvocato.jsp
DettaglioAvvocatoAvvocatoFascicoloSiep.jsp
DettaglioAvvocatoSentenza.jsp
InserimentoAssegnazioneDifensore.jsp
LoadInserisciAvvocato.jsp
SostituzioneDifensore.jsp
FiltraListaAvvocatiPopup.jsp
ListaAvvocatoPopup.jsp

fascicolo
DettaglioFascicoloSiep.jsp

sige
avvocato
DettaglioAvvocatoFascicoloSige.jsp
DettaglioAvvocatoSentenza.jsp
InserimentoAssegnazioneDifensore.jsp
LoadInserisciAvvocato.jsp
SostituzioneDifensore.jsp

sius
avvocato
DettaglioAvvocatoAvvocatoFascicoloSius.jsp
DettaglioAvvocatoSentenza.jsp
LoadRicercaAvvocatoSiep.jsp
LoadInserisciAvvocato.jsp
SostituzioneDifensore.jsp

Di seguito l’elenco delle action.java da modificare, suddivise per sottosistema:

siep
avvocato > action
ActDettaglioAvvocato.java
ActInserisciAvvocato.java
ActLoadDettaglioAvvocato.java
ActLoadDettaglioAvvocatoFascicolo.java
ActLoadInserisciAssegnaAvvocato.java
ActLoadInserisciAvvocato.java
ActLoadSostituzioneDifensore.java
ActSostituzioneDifensore.java
nuovaistanza > action
ActLoadInserisciIstanzaPerProcedimentoSiep.java
ActLoadInserisciIstanzaPerSoggetto.java
ActLoadInserisciIstanzaPerTitoloEsecutivo.java

sige
avvocato > action
ActLoadDettaglioAvvocatoFascicoloSige.java
ActInserisciAvvocato.java
ActLoadInserisciAvvocato.java
ActLoadSostituzioneDifensore.java
ActSostituzioneDifensore.java
udienza > action
ActLoadInserisciFissazioneUdienza.java
udienzaprocedimento > action
ActLoadInserisciOrdinanzaRinvioUdienza.java
ActLoadInserisciVerbaleRinvioUdienza.java
udienzaparti > action
ActLoadInserisciAvvocato.java
ActLoadSostituzioneDifensore.java

sius
avvocato > action
ActLoadDettaglioAvvocatoFascicolo.java
ActInserisciAvvocato.java
ActLoadInserisciAvvocato.java
ActLoadSostituzioneDifensore.java
ActSostituzioneDifensore.java

Saranno realizzati nuovi moduli software per la ricerca dell’Avvocato su ReGIndE.
## Architettura
N.A.
## Interfacce utente
Per l’inserimento della nuova ricerca dell’avvocato su ReGIndE, attraverso l’utilizzo di un Web Services, saranno modificate e realizzate le seguenti interfacce:
### Sottosistema SIEP
L’attuale funzione di Assegnazione/Inserimento Difensore SIEP


Figura 11: Form inserimento difensore procedimento SIEP- attuale

sarà modificata come di seguito riportato:


Figura 14: Form inserimento difensore procedimento SIEP - nuova

Nello specifico, si procederà con la sostituzione dell’attuale link , che permette di selezionare l’avvocato fra quelli già presenti in SIES, con il nuovo link , che permetterà di ricercare l’avvocato nella base dati di ReGIndE.
Inoltre sulla form dei dati avvocato, sarà prevista l’aggiunta del nuovo campo PEC, dato che risulta essere presente in ReGIndE.

Al click di tale link il sistema proporrà la nuova form di ricerca su ReGIndE, descritta di seguito.


Figura 15: Form di attivazione ricerca su ReGIndE

La funzione permetterà, utilizzando un apposito Web Service di interazione con ReGIndE, la ricerca dell’avvocato sul Registro Generale degli Indirizzi Elettronici. La form presenta i campi per la ricerca per Cognome e Nome dell’avvocato, Foro di appartenenza e un check-box per ‘estendere’ la ricerca a tutti i Fori.
I campi obbligatori per la ricerca saranno: Cognome e Foro, o in alternativa, Cognome e check-box ‘Tutti i Fori’.
In particolare, il Foro sarà selezionabile da una listbox, i cui valori corrisponderanno a quelli presenti nella tabella contenente l’elenco dei Fori, utilizzata nel sistema SIES, che sarà resa conforme a quello di ReGIndE. A seguito della selezione del tasto Cerca su ReGIndE il sistema innescherà su ReGIndE una ricerca puntuale degli Avvocati aventi Cognome, eventualmente il Nome uguali a quelli digitati e appartenenti al foro selezionato o a tutti i fori.

I risultati saranno filtrati secondo il codice Ente di ReGIndE (Foro Avvocati), costituito dalla concatenazione della stringa COA e dal codice Istat del Comune sede dello stesso, per questo motivo detto anche semplicemente COA.

Il sistema SIES, all’avvenuta conferma da parte dell’utente dei criteri digitati, attiverà la ricerca su ReGIndE, utilizzando per l’interfaccia i servizi web esposti dall’applicazione ReGIndE, costruendo il client ed altre apposite classi java che permetteranno di effettuare la ricerca vera e propria e di gestire i risultati ottenuti.

Nei casi di indisponibilità del sistema ReGIndE e/o di dati non trovati su ReGIndE, il sistema restituirà, per ciascuno dei casi indicati, un opportuno messaggio di alert e attiverà la funzione di ricerca del difensore su SIES [Rif. § “6.3 REQ-SIE-021-03-FN.01 - Inserimento Manuale: Indisponibilità ReGIndE o Avvocato Non Presente”].

E’ possibile che il servizio di interrogazione/ricerca del soggetto su ReGIndE possa restituire un messaggio di ‘SearchLimitException’, ossia che in fase di ricerca sia stato individuato un numero di soggetti superiore ad un dato limite. In tal caso sarà mostrato un messaggio che invita l’utente a restringere i criteri di ricerca e la form presenta un nuovo campo di ricerca per Codice Fiscale.



Figura 16: Form di ricerca su ReGIndE con segnalazione di eccessive occorrenze con criteri impostati

In questo caso l’utente potrà rieseguire la ricerca valorizzando il nome oppure limitarsi a valorizzare solo il codice fiscale, in quanto anche in presenza della valorizzazione degli altri campi della form, il sistema ricercherà tutti gli avvocati con il codice fiscale indicato in tutti i fori, non considerando il contenuto degli altri campi.

Nel caso, invece, di disponibilità del sistema ReGIndE e di dati trovati su ReGIndE, questi ultimi, dopo essere stati opportunamente recuperati, saranno convogliati in una nuova Form di elenco avvocati estratti da ReGIndE, sempre tramite l’utilizzo dello specifico Web Service.


Figura 17: Form Elenco Avvocati ReGIndE

Nella 	Form di Elenco saranno visualizzati i dati del singolo o di ogni avvocato trovato soddisfacente i parametri di ricerca digitati precedentemente.
I dati che saranno visualizzati per ciascuno saranno: Cognome, Nome Codice Fiscale, Foro di appartenenza, Luogo e Data Nascita, Indirizzo, Stato (attivo, radiato, sospeso, cessato). In riferimento allo Stato dell’avvocato, dato molto utile per l’utente SIES, si sottolinea che al momento questo dato è presente e visibile su ReGIndE, ma che potrebbe essere in futuro oscurato nel risultato delle ricerche. In caso che si verificasse questa ultima evenienza è essenziale che gli amministratori di ReGIndE avvisino per tempo i Referenti SIES per la valutazione di possibili correttivi.

Inoltre, sempre in merito ai dati che saranno visualizzati in elenco, ed alla loro gestione, occorre tener conto di tali osservazioni:

Nel caso che la Ricerca su ReGIndE, in corrispondenza della colonna indirizzo, dovesse fornire più record con tipologia a ‘D’, il sistema SIES, recepirà il primo ottenuto ordinando alfabeticamente la colonna Indirizzo.

Poiché in ReGIndE il LUOGO_NASCITA e il COMUNE di RESIDENZA dello studio sono importati, in forma descrittiva, così come inseriti dagli Ordini Forensi, senza alcun controllo sulla corrispondenza della Descrizione rispetto alle Denominazioni ufficialmente riconosciute dei Comuni, può verificarsi che siano riportate descrizioni non corrispondenti a quelle legalmente riconosciute ( ad es. come luogo di nascita sono riportati: CASERTA  -S. BARBARA-, S.MARIA C.V., ERICE C.S., RIVAROLO C.SE,…).

Al momento nella tabella AVVOCATO di SIES i due dati vengono valorizzati con il codice Istat del Comune, dopo essere stati sottoposti al controllo dell’esistenza della Descrizione inserita nelle form rispetto a quella presente nella tabella COMUNE, quindi il sistema, in fase di inserimento/aggiornamento non li accetterebbe. Per bypassare questo problema nella tabella AVVOCATO di SIES sarà mantenuta la codifica del luogo di nascita, ricavandolo dal codice Belfiore (dal quintultimo al penultimo carattere) del Codice Fiscale, sempre presente in ReGIndE, mentre per il luogo residenza sarà aggiunta una nuova colonna che conterrà la descrizione del Comune sede dello studio come presente in ReGIndE, abbandonando la valorizzazione della colonna COD_COMUNE_RESIDENZA, che resterà per i dati pregressi;

Per poter risalire dal codice Belfiore al codice Istat del Comune, nella tabella COMUNE di SIES sarà aggiunto una nuova colonna di 4 caratteri alfanumerici, che sarà valorizzata con apposita procedura PLSQL con il codice catastale corrispondente, recuperandolo dalla tabella Comune della DGSIA. A tal fine bisognerà procedere preventivamente all’aggiornamento delle tabelle di SIES, COMUNE e CG_REF_CODES, relativamente ai domini Provincia, Regione e Nazione, allineandole alla tabelle fisse COMUNE, PROVINCIA, REGIONE e STATO-NAZIONE della DGSIA. Le attività previste per tale aggiornamento sono descritte dettagliatamente di seguito al par. 6.6.;

In caso di assenza del codice Belfiore nella tabella COMUNE di SIES, l’avvocato non sarà importato, ma, sulla pagina web, sarà inviato specifico messaggio di avviso all’utente della NON PRESENZA del Comune in SIES, con indicazione di segnalarne urgentemente l’assenza al gruppo Tabelle Fisse dell’Amministrazione. Il sistema consentirà comunque di inserire l’avvocato in SIES privo della certificazione ReGIndE , in modalità manuale (vedi par. 6.3.3.2).

A seguito delle suddette modifiche alla base dati, saranno rivisti tutti i moduli SIES, che al momento recuperano la descrizione del comune sede dello studio, attraverso la decodifica del codice ISTAT.

Dalla pagina di elenco, selezionando l’icona del +, presente accanto al nominativo del difensore, sarà possibile visualizzare gli ulteriori dati dell’avvocato (pec, telefono, fax, email), al di sotto di quelli già riportati nella form.

Dalla Form di elenco, l’utente potrà selezionare l’avvocato di interesse ed il sistema lo riporterà sulla Form precedente (la chiamante, cioè la Form da cui è stata attivata la funzione di ricerca su ReGIndE) in cui saranno riportati negli specifici campi della form tutti i dati dell’avvocato selezionato.


Figura 18: Form dettaglio Avvocato selezionato

All’atto della conferma dell’associazione dell’avvocato al fascicolo SIEP in lavorazione, per l’avvocato selezionato dall’elenco, il sistema verificherà la presenza nella tabella ‘AVVOCATO’ del SIES, limitatamente
ai record presenti in tabella aventi il FLAG_REGINDE = ’SI’.

I criteri utilizzati per tale verifica saranno:
COGNOME
NOME
CODICE FISCALE
FORO di appartenenza.
Per nessun dato trovato, i criteri saranno ridotti a:
COGNOME
NOME
FORO di appartenenza.

Il sistema, in base all’esito di tale verifica, eseguirà le seguenti operazioni:
Esito Verifica: Avvocato individuato univocamente nella tabella ‘AVVOCATO’ del SIES:
il sistema aggiornerà i dati del record trovato [Rif. § “6.1.4.2  Tabella Avvocati SIES”] con i dati recuperati da ReGIndE relativamente alla PEC, all’Indirizzo, al Numero di telefono e allo Stato dell’avvocato (ad es. attivo o cancellato) ed assocerà l’identificativo dell’avvocato al fascicolo SIES in lavorazione.
Nel caso in cui la Ricerca su ReGIndE, in corrispondenza del tag indirizzo, dovesse fornire più record con tipologia a ‘D’, sarà selezionato il primo ottenuto ordinando alfabeticamente la colonna Indirizzo.
Si evidenzia che a seguito dell’aggiornamento dell’indirizzo, potrebbe verificarsi che su un procedimento ancora in corso con provvedimenti/atti riferiti all’ indirizzo dell’avvocato precedente all’aggiornamento, rieseguiti/ristampati riporterebbero i dati del nuovo indirizzo. In ogni caso la sovrascrittura del vecchio indirizzo non costituisce un problema per SIES, anche in caso di indirizzo non valorizzato su ReGIndE.
Esito Verifica: Avvocato NON trovato nella tabella ‘AVVOCATO’ del SIES:
il sistema effettuerà l’inserimento nella tabella ‘AVVOCATO’ del SIES utilizzando i dati recuperati da ReGIndE e, l’identificativo del nuovo avvocato inserito, sarà associato al fascicolo SIES in lavorazione. Nell’inserimento del record sulla tabella del SIES sarà impostato il nuovo campo FLAG_REGINDE con il valore ‘Sì’ [Rif. § “6.1.4.2  Tabella Avvocati SIES”] e il COD_UFFICIO_APPARTENENZA = ‘00000’.

È necessario specificare che tutte le ricerche di un avvocato su SIES avverranno per FLAG_REGINDE = ‘SI’.
Di conseguenza, non si incorrerà nella casistica di risultati multipli della ricerca SIES.

A tale proposito si evidenzia che a seguito dello scambio dati fra BDI, L’avvocato importato da altra BDI, anche se già presente nella BDI corrente, dovrà necessariamente essere importato con il suo ID originario, per cui potrebbero crearsi records multipli riferiti allo stesso AVVOCATO certificato su ReGIndE. Per evitare che in fase di assegnazione dell’Avvocato a un procedimento, il sistema non associ al procedimento l’avvocato della BDI corrente, in fase di ricerca nella tabella AVVOCATO SIES, sarà selezionato quello con ID riferito alla BDI corrente.

A seguito dell’acquisizione del dato relativo alla PEC, anche la form attuale di Dettaglio Avvocato del procedimento SIEP sarà modificata così come riportato nella figura che segue:


Figura 19: Form dettaglio avvocato procedimento SIEP

Anche la funzione ‘Sostituzione Difensore’ SIEP sarà modificata alla stessa maniera descritta per la funzione Assegnazione Difensore con l’inserimento nella form del Link  e del campo Pec.


Figura 20: Form sostituzione Difensore procedimento SIEP

Il funzionamento sarà esattamente uguale a quello descritto per funzione ‘Assegnazione Difensore’.

L’attuale funzione di Iscrizione Istanza da Soggetto andrà rivista per sostituire l’attuale popup di selezione Avvocato da SIES con quella di selezione da ReGIndE, descritta in precedenza,


Figura 21: Form Iscrizione Istanza da Soggetto - Attuale

in cui, cliccando , si presenta la seguente popup


Figura 22: popup Ricerca e seleziona Avvocato SIES

che permette di ricercare o inserire il difensore nella tabella Avvocato di SIES. Il link sarà sostituito dalla nuova funzionalità .


Stesso intervento andrà effettuato sulla funzione Iscrizione Istanza da Titolo Esecutivo

Figura 23: Form Iscrizione Istanza da Titolo Esecutivo - Attuale


e sulla funzione Iscrizione Istanza da Procedimento SIEP

Figura 24: Form Iscrizione Istanza da Procedimento SIEP

### Sottosistema SIGE
L’attuale funzione di Assegnazione/Inserimento Difensore SIGE

Figura 25: Form sostituzione Assegnazione Difensore procedimento SIGE - Attuale
sarà modificata come di seguito:


Figura 26: Form sostituzione Assegnazione Difensore procedimento SIGE - Nuova
con l’eliminazione dell’attuale link , che permette di selezionare l’avvocato fra quelli già presenti in SIES, con il nuovo link , che permetterà di ricercare l’avvocato nella base dati di ReGIndE, e con l’aggiunta del nuovo campo PEC, dato che risulta essere presente in ReGIndE.
Al click del link  il sistema proporrà la nuova form di ricerca su ReGIndE, descritta già in precedenza per il sottosistema SIEP, con identico funzionamento.

Dopo aver selezionato dall’elenco degli Avvocati quello di interesse e precompilato la form di inserimento, a seguito della conferma dell’associazione dell’avvocato al fascicolo SIGE in lavorazione, per l’avvocato selezionato dall’elenco, il sistema verificherà la presenza nella tabella ‘AVVOCATO’ del SIES, limitatamente
ai record presenti in tabella aventi il FLAG_REGINDE = ’SI’.

I criteri utilizzati per tale verifica saranno:
COGNOME
NOME
CODICE FISCALE
FORO di appartenenza.
Per nessun dato trovato, i criteri saranno ridotti a:
COGNOME
NOME
FORO di appartenenza.

Il sistema, in base all’esito di tale verifica, eseguirà le seguenti operazioni:
Esito Verifica: Avvocato individuato univocamente nella tabella ‘AVVOCATO’ del SIES:
il sistema aggiornerà i dati del record trovato con i dati recuperati da ReGIndE relativamente alla PEC, all’Indirizzo, al Numero di telefono e allo Stato dell’avvocato (ad es. attivo o cancellato) ed assocerà l’identificativo dell’avvocato al fascicolo SIES in lavorazione. Nel caso che la Ricerca su ReGIndE, in corrispondenza del tag indirizzo, dovesse fornire più record con tipologia a ‘D’, sarà selezionato il primo ottenuto ordinando alfabeticamente la colonna Indirizzo.
Esito Verifica: Avvocato NON trovato nella tabella ‘AVVOCATO’ del SIES:
il sistema effettuerà l’inserimento nella tabella ‘AVVOCATO’ del SIES utilizzando i dati recuperati da ReGIndE e, l’identificativo del nuovo avvocato inserito, sarà associato al fascicolo SIES in lavorazione. Nell’inserimento del record sulla tabella del SIES sarà impostato il nuovo campo FLAG_REGINDE con il valore ‘SI’ e il COD_UFFICIO_APPARTENENZA = ‘00000’.

Si evidenzia che tutte le ricerche di un avvocato su SIES avverranno per FLAG_REGINDE = ‘SI’, pertanto
non si incorrerà nella casistica di risultati multipli della ricerca SIES.

A seguito dell’acquisizione del dato relativo alla PEC, anche l’attuale form di Dettaglio Avvocato del procedimento SIGE

Figura 27: Form Dettaglio Difensore procedimento SIGE - Attuale
sarà modificata, oltre che per la visualizzazione del nuovo dato PEC, anche con la presentazione di dati presenti nella form di Assegnazione ma non presentati in quella di Dettaglio (Luogo nascita, Data Nascita, Comune Residenza, pec). Pertanto la nuova form sarà la seguente:

Figura 28: Form Dettaglio Difensore procedimento SIGE - Nuova
Anche la funzione ‘Sostituzione Difensore’ SIGE sarà modificata alla stessa maniera descritta per la funzione Assegnazione Difensore SIGE con l’inserimento nella form del Link  e del campo Pec.

Figura 29: Form Sostituzione Difensore procedimento SIGE - Nuova
Il funzionamento sarà esattamente uguale a quello descritto per funzione ‘Assegnazione Difensore’.
Anche la funzione Inserimento Difensore Parte

Figura 30: Form Inserimento Difensore procedimento SIGE – Parti in causa
attivabile dal link Gestione Difensore, presente nelle form Inserimento Difensore Parte, raggiungibile dalle funzioni Gestioni Parti Civili e Gestione Parti Offese, presenti in Dettaglio Fissazione Udienza, Dettaglio Rinvio Udienza con Ordinanza, Dettaglio Rinvio Udienza da Verbale, Dettaglio Nomina Periti e in Dettaglio Ordinanza

Figura 31: Form Inserimento Difensore Parte

Figura 32: Form Dettaglio Fissazione Udienza procedimento SIGE
sarà modificata

Figura 33: Form Inserimento Difensore procedimento SIGE Parti in causa - Nuova
alla stessa maniera descritta per la funzione Assegnazione Difensore SIGE con l’inserimento nella form del Link   e del campo Pec. Il funzionamento sarà esattamente uguale a quello descritto per funzione ‘Assegnazione Difensore’.

### Sottosistema SIUS

L’attuale funzione di Assegnazione/Inserimento Difensore   SIUS


Figura 34: Form Assegnazione Difensore procedimento SIUS - Attuale

sarà modificata come di seguito


Figura 35: Form Assegnazione Difensore procedimento SIUS - Nuova

con l’eliminazione dell’attuale link , che permette di selezionare l’avvocato fra quelli già presenti in SIES, con il nuovo link , che permetterà di ricercare l’avvocato nella base dati di ReGIndE, e con l’aggiunta del nuovo campo PEC, dato che risulta essere presente in ReGIndE.

Il link rimarrà, ma la funzione richiamata sarà rivista in quanto ricercherà fra gli avvocati collegati al procedimento SIEP solo quelli importati da ReGIndE, cioè quelli aventi nella tabella AVVOCATO di SIES il FLAG_REGINDE = ‘SI’. Inoltre l’attuale comportamento di SIUS, che a fronte del difensore selezionato, duplica l’informazione inserendo un nuovo record riferito all’ufficio collegato, sarà modificato per cui l’avvocato selezionato sarà collegato anche al procedimento SIUS.

Al click del link  il sistema proporrà la nuova form di ricerca su ReGIndE, descritta già in precedenza per il sottosistema SIEP, con identico funzionamento.

Dopo aver selezionato dall’elenco degli Avvocati quello di interesse e precompilato la form di inserimento, a seguito della conferma dell’associazione dell’avvocato al fascicolo SIUS in lavorazione, per l’avvocato selezionato dall’elenco, il sistema verificherà la presenza nella tabella ‘AVVOCATO’ del SIES, limitatamente
ai record presenti in tabella aventi il FLAG_REGINDE = ’SI’.

I criteri utilizzati per tale verifica saranno:
COGNOME
NOME
CODICE FISCALE
FORO di appartenenza.
Per nessun dato trovato, i criteri saranno ridotti a:
COGNOME
NOME
FORO di appartenenza.

Il sistema, in base all’esito di tale verifica, eseguirà le seguenti operazioni:
Esito Verifica: Avvocato individuato univocamente nella tabella ‘AVVOCATO’ del SIES:
il sistema aggiornerà i dati del record trovato con i dati recuperati da ReGIndE relativamente alla PEC, all’Indirizzo, al Numero di telefono e allo Stato dell’avvocato (ad es. attivo o cancellato) ed assocerà l’identificativo dell’avvocato al fascicolo SIES in lavorazione. Nel caso che la Ricerca su ReGInde, in corrispondenza del tag indirizzo, dovesse fornire più record con tipologia a ‘D’, sarà selezionato il primo ottenuto ordinando alfabeticamente la colonna Indirizzo.

Esito Verifica: Avvocato NON trovato nella tabella ‘AVVOCATO’ del SIES:
il sistema effettuerà l’inserimento nella tabella ‘AVVOCATO’ del SIES utilizzando i dati recuperati da ReGIndE e, l’identificativo del nuovo avvocato inserito, sarà associato al fascicolo SIES in lavorazione. Nell’inserimento del record sulla tabella del SIES sarà impostato il nuovo campo FLAG_REGINDE con il valore ‘SI’ e il COD_UFFICIO_APPARTENENZA = ‘00000’.

Si evidenzia che tutte le ricerche di un avvocato su SIES avverranno per FLAG_REGINDE = ‘SI’, pertanto non si incorrerà nella casistica di risultati multipli della ricerca SIES.

A seguito dell’acquisizione del dato relativo alla PEC, anche l’attuale form di Dettaglio Avvocato del procedimento SIUS


Figura 36: Form Dettaglio Difensore procedimento SIUS - Attuale

sarà modificata, oltre che per la visualizzazione del nuovo dato PEC, anche con la presentazione di dati presenti nella form di Assegnazione ma non presentati in quella di Dettaglio (Luogo nascita, Data Nascita, Comune Residenza, pec). Pertanto la nuova form sarà la seguente:


Figura 37: Form Dettaglio Difensore procedimento SIUS - Nuova

Anche la funzione ‘Sostituzione Difensore’ SIUS sarà modificata alla stessa maniera descritta per la funzione Assegnazione Difensore SIUS con l’inserimento nella form del Link  e del campo Pec.


Figura 38: Form Sostituzione Difensore procedimento SIUS - Nuova

Il link rimarrà, ma la funzione richiamata sarà rivista in quanto ricercherà fra gli avvocati collegati al procedimento SIEP solo quelli importati da ReGIndE, cioè quelli aventi nella tabella AVVOCATO di SIES il FLAG_REGINDE = ‘SI’. Inoltre l’attuale comportamento di SIUS, che a fronte del difensore selezionato, duplica l’informazione inserendo un nuovo record riferito all’ufficio collegato, sarà modificato per cui l’avvocato selezionato sarà collegato anche al procedimento SIUS.

Il funzionamento sarà esattamente uguale a quello descritto per funzione ‘Assegnazione Difensore’.

## Basi dati
La tabella AVVOCATO di SIES sarà modificata con l’aggiunta di tre nuove colonne: PEC, FLAG_REGINDE, DESCR_COMUNE_STUDIO. A tal fine sarà preparato uno script del tipo Alter_Table_Avvocato.sql.



## WEB services
L’implementazione delle ricerca dell’avvocato su ReGIndE, operativamente, è legata all’invocazione di un webservice esposto dal sistema Registro Generale degli Indirizzi Elettronici (ReGIndE).

Nel sistema SIES occorre predisporre un modulo client in java che permetterà di interloquire con gli  endpoint dei servizi ReGIndE attraverso i quali sarà poi raggiungibile il servizio applicativo per le interrogazioni per “Soggetti” (difensori). Nello specifico il sistema SIES si interfaccerà con l’endpoint esposto per ‘chiamate interne’ per sistemi su giustizia.
L’endpoint di interesse è identificato dalla seguente url:

https://XX.XXX.XXXX.XXX/ServiziInterrogazioneRegindeExt/ServiziInterrogazioneInterni

e l’operazione, servizio applicativo a cui fare accesso, è ‘ricercaSoggettoComplete’.

Tale servizio permette una ricerca del soggetto difensore sul sistema Registro Generale degli Indirizzi Elettronici secondo i seguenti parametri:

nome
cognome
codiceFiscale
indirizzoPec
codiceEnte

Nome: indica il nome del difensore di interesse per la ricerca;
Cognome: indica il cognome del difensore di interesse per la ricerca;
Codice Fiscale: indica il codice fiscale del difensore di interesse per la ricerca;
Indirizzo Pec: indica l’indirizzo della PEC del difensore di interesse per la ricerca;
Codice Ente: indica il codice identificativo dell'ente, quindi l’albo, che ha censito l’avvocato in ReGIndE. Per gli avvocati iscritti ad un Consiglio dell'Ordine il codice dell'ente sarà rappresentato da una stringa data dal prefisso COA, al quale viene aggiunto il codice Istat del comune di riferimento del consiglio dell’ordine stesso.


In riferimento al requisito di ricerca su ReGIndE [REQ-SIE-021-02] la ricerca prevede come campi obbligatori il Cognome ed il Foro di appartenenza o in alternativa, Cognome e check-box ‘Tutti i Fori’ che si traduce pertanto in un’interrogazione al servizio senza specificare il codiceEnte.

Il servizio di ‘ricercaSoggettoComplete’ restituisce una lista di oggetti ‘soggetto’ che analizzando il wsdl è così definito:

<xs:complexType name='soggetto'>
<xs:sequence>
<xs:element maxOccurs='unbounded' minOccurs='0' name='ruoliente' type='tns:ruoloente'/>
<xs:element maxOccurs='unbounded' minOccurs='0' name='indirizzi' type='tns:indirizzo'/>
<xs:element minOccurs='0' name='soggetto' type='tns:soggetti'/>
</xs:sequence>
</xs:complexType>

Quindi avremmo, un oggetto di tipo ‘soggetti’ così definito:

<xs:complexType name='soggetti'>
<xs:sequence>
<xs:element minOccurs='0' name='codFisc' type='xs:string'/>
<xs:element minOccurs='0' name='cognome' type='xs:string'/>
<xs:element minOccurs='0' name='dataNascita' type='xs:dateTime'/>
<xs:element minOccurs='0' name='luogoNascita' type='xs:string'/>
<xs:element minOccurs='0' name='nome' type='xs:string'/>
<xs:element minOccurs='0' name='pec' type='xs:string'/>
<xs:element minOccurs='0' name='provNascita' type='xs:string'/>
</xs:sequence>
</xs:complexType>

ed una lista di oggetti ‘ruoloente’ e ‘indirizzo’, a sua volta così definiti:

<xs:complexType name='ruoloente'>
<xs:sequence>
<xs:element minOccurs='0' name='codiceFiscale' type='xs:string'/>
<xs:element minOccurs='0' name='codice' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element name='pubblicaAmministrazione' type='xs:boolean'/>
<xs:element minOccurs='0' name='pec' type='xs:string'/>
<xs:element minOccurs='0' name='partitaIVA' type='xs:string'/>
<xs:element minOccurs='0' name='ruolo' type='xs:string'/>
<xs:element minOccurs='0' name='stato' type='xs:string'/>
</xs:sequence>
</xs:complexType>

<xs:complexType name='indirizzo'>
<xs:sequence>
<xs:element minOccurs='0' name='cap' type='xs:string'/>
<xs:element minOccurs='0' name='comune' type='xs:string'/>
<xs:element minOccurs='0' name='email' type='xs:string'/>
<xs:element minOccurs='0' name='fax' type='xs:string'/>
<xs:element minOccurs='0' name='indirizzo' type='xs:string'/>
<xs:element minOccurs='0' name='prov' type='xs:string'/>
<xs:element minOccurs='0' name='telefono' type='xs:string'/>
<xs:element minOccurs='0' name='tp_indirizzo' type='xs:string'/>
</xs:sequence>
</xs:complexType>


### Gestione delle fault
Dall’analisi del wsdl una possibile eccezione che deve essere gestita è la tipologia di errore denominata ‘SearchLimitException’ che sarà restituita dal servizio nelle casistiche in cui la ricerca estragga una numerosità troppo elevata di occorrenze trovate.

Il problema sarà comunque gestito applicativamente, come già riportato a pag. 38, obbligando l’utente a restringere i criteri di ricerca con un messaggio di warning e con l’inserimento nella form dell’ulteriore campo Codice Fiscale.
### Altre specifiche per il servizio
I messaggi SOAP rivolti a questi servizi non prevedono l’inserimento di parametri specifici all’interno dell’header SOAP e dell’header http e ad oggi si basano su un protocollo di sicurezza basato su TLS 1.2, al momento in fase di collaudo.

Se al momento della messa in esercizio degli interventi previsti in questo documento, su ReGIndE non fosse stato ancora rilasciato il protocollo TLS1.2, si provvederà ad effettuare gli opportuni interventi per il funzionamento con protocollo di sicurezza TLS1.0.
## XSD
N.A.
## Configurazione
Per la connessione ai servizi in https sul sistema ReGIndE è da prevedere l’importazione della chiave pubblica (certificato ssl) che mappa il DNS del server su cui è esposto il servizio

ES:  https:// reginde /ServiziInterrogazioneRegindeExt/ServiziInterrogazioneInterni

Il certificato deve essere importato nel file keystore del SIES (trustore.jks) posizionato al /var/SIES/CONFIG/certs.

L’Amministrazione fornirà il certificato di chiave pubblica del ReGIndE, e tutta la catena necessaria, utilizzato al momento della messa in esercizio degli interventi SIES.

Nel documento di rilascio della release contente gli interventi previsti in questa Scheda, saranno descritte dettagliatamente gli interventi da effettuare a livello di configurazione per la corretta messa in esercizio del nuovo servizio di interoperabilità SIES – ReGIndE.
## Tutorial
N.A.
## REQ- SIE-021-03_FN.01 – Inserimento Manuale: Indisponibilità ReGIndE o Avvocato Non Presente
Nei casi di indisponibilità del sistema ReGIndE o di assenza dell’avvocato su ReGIndE, il sistema dovrà consentire la ricerca del Difensore su SIES.
Inoltre nel caso di assenza del Difensore anche nella base dati di SIES, il sistema consentirà l’inserimento dello stesso in SIES, ma limitandone l’utilizzo solo al procedimento corrente.

## Moduli sw
Nell’ambito dei nuovi moduli che saranno sviluppati per la ricerca Avvocato su ReGIndE, saranno gestite anche i casi relativi alle eccezioni.
## Architettura
N.A.
## Interfacce utente
### Inserimento manuale: Indisponibilità ReGIndE o Avvocato Non Presente

Nei casi di indisponibilità del sistema ReGIndE o di assenza dell’avvocato su ReGIndE, il sistema segnalerà all’utente il tipo di evento intercorso e presenterà nella form di Ricerca il pulsante per la funzione di ricerca dell’avvocato sul sistema SIES, al fine di consentire all’utente di proseguire con le proprie attività.

Si riporta di seguito come si presenterà la form di Ricerca Avvocato su ReGIndE nei due suddetti casi


Figura 39: Form Ricerca Difensore su ReGIndE in caso di assenza collegamento



Figura 40: Form Ricerca Difensore su ReGIndE in caso nessun occorrenza trovata

in cui, oltre a presentare l’esito della Ricerca su ReGIndE, è presente il tasto per avviare la Ricerca su SIES.

La ricerca sarà effettuata sulla tabella ‘AVVOCATO’ del SIES e i parametri di ricerca saranno gli stessi utilizzati per la ricerca su ReGIndE [Rif. § “6.2 Ricerca su ReGIndE”]: Cognome e Nome dell’avvocato e Foro di appartenenza, se specificato, con opzione di ricerca mediante check-box per tutti i fori.
La ricerca sarà relativa ai record che hanno il FLAG_REGINDE=’Sì’.
I campi obbligatori saranno: Cognome e Foro, o in alternativa, Cognome e check-box ‘Tutti i Fori’.

In caso di ricerca con esito positivo il sistema presenterà l’elenco dei difensori soddisfacenti i parametri impostati


Figura 41: Form Elenco Avvocati SIES
l’utente selezionerà l’avvocato di interesse dalla lista, il sistema si limiterà ad associare l’avvocato al procedimento corrente, essendo lo stesso già certificato su ReGIndE.

Nel caso l’esito della ricerca su SIES non producesse alcun risultato, quindi per avvocato non trovato in base ai criteri di ricerca digitati, la form presenterà il messaggio di assenza in SIES di avvocati, soddisfacenti i parametri di ricerca e presenterà il tasto per procedere all’inserimento di un nuovo difensore in SIES.


Figura 42: Form Esito Ricerca Difensori SIES in caso di nessun occorrenza trovata

L’utente potrà scegliere di procedere con l’inserimento manuale dell’avvocato, selezionando il tasto  o potrà avviare una nuova di ricerca su ReGIndE o su SIES.
Se l’utente seleziona l’Inserimento di un nuovo Difensore, il sistema chiuderà la Form di ricerca difensore e presenterà sulla Home Page di SIES la form di Inserimento.

### Inserimento manuale avvocato sul sistema SIES

La funzionalità di inserimento manuale consentirà all’utente di effettuerà l’inserimento dei dati dell’avvocato sulla tabella ‘AVVOCATO’ del SIES. A tal fine il sistema presenterà la seguente form di inserimento

Figura 43: Form Inserimento Difensore in SIES

Il campo Codice Fiscale sarà un dato obbligatorio, su cui il sistema effettuerà il controllo di correttezza formale, fatta eccezione la verifica del carattere di controllo finale.

All’atto della conferma, prima di procedere all’inserimento, il sistema effettuerà nuovamente il controllo di verifica dell’eventuale presenza dell’anagrafica sulla tabella ‘AVVOCATO’ del SIES con FLAG_REGINDE = ‘Sì’.
I criteri utilizzati per il controllo in questa fase saranno:
COGNOME
NOME
LUOGO DI NASCITA
DATA DI NASCITA
CODICE FISCALE
FORO.
Per dati non trovati, la ricerca sarà raffinata progressivamente eliminando, di volta in volta, nell’ordine:
CODICE FISCALE
DATA DI NASCITA
LUOGO DI NASCITA
fino ad effettuare la ricerca con i soli COGNOME, NOME e FORO.

Qualora l’esito di tale controllo fosse “NON TROVATO”, cioè nel caso di anagrafica non trovata, il sistema procederà all’inserimento dei dati dell’avvocato sulla tabella ‘AVVOCATO’ del SIES, impostando anche il nuovo campo FLAG_REGINDE con il valore ‘NO’  e provvederà ad effettuare anche l’associazione al procedimento corrente (SIEP, SIUS, SIGE).
Di conseguenza, il record di anagrafica inserito in questo frangente, avrà valenza solo per la gestione del fascicolo che l’utente sta inserendo in quel momento: l’avvocato inserito NON sarà visibile per la gestione di altri fascicoli.
Qualora, invece, l’esito fosse “TROVATO”, cioè nel caso di anagrafica già presente, il sistema non effettuerà alcun inserimento.

Nel caso che il codice fiscale contenga un codice Belfiore non esistente in SIES, il sistema invierà a video il messaggio di conferma a procedere all’inserimento ‘Comune di nascita non presente in SIES, si vuole procedere comunque all’inserimento?’. L’operatore potrà annullare l’operazione o procedere, in caso di prosecuzione l’avvocato sarà inserito nella base dati con il codice fiscale digitato, ma privo del luogo di nascita.

Nella Form di dettaglio dei fascicoli associati a difensori aventi FLAG_REGINDE = ‘NO’, scaturenti da un inserimento manuale, sarà attivato un alert che NON costituirà errore bloccante ma sarà semplicemente un avviso per l’utente, il quale dovrà procedere a rieseguire l’associazione del difensore al fascicolo in lavorazione a partire da ReGIndE, come già descritto al § 6.1.

## Basi dati
N.A.
## WEB services
N.A.
## XSD
N.A.
## Configurazione
N.A.
## Tutorial
N.A.
## REQ- SIE-021-04_FN.01 – Interventi su Funzioni SIES di Gestione Avvocati

Poiché lo scopo degli interventi descritti nel presente documento è che i dati delle anagrafiche degli avvocati presenti su SIES dovranno essere “importati” dal sistema ReGIndE, sul sistema SIES saranno inibite le funzioni di Inserimento Difensore e Modifica Difensore.
Nello specifico, nel menù Funzioni Amministrative» Gestione Difensori, il tasto ‘Inserimento’ non sarà più visibile, ed inoltre, nello stesso menù, nella Form di elenco Difensori ottenuta dal tasto di ‘ricerca’ sarà eliminata l’azione ‘modifica’.
Nelle pagine corrispondenti ai punti di attivazione della ricerca su ReGIndE sarà eliminato il tasto ‘Inserimento’.
Il sistema abiliterà l’inserimento manuale del difensore, SOLO, per la casistica di cui al par. “6.3.3.2 Inserimento manuale avvocato sul sistema SIES”.

## Moduli sw
N.A.
## Architettura
N.A.
## Interfacce utente
Nell’attuale menu Funzioni Amministrative» Gestione Difensori


Figura 44: Form Gestione Difensori - Attuale

il tasto  sarà oscurato, per cui il menu riporterà le seguenti voci


Figura 45: Form Gestione Difensori - Nuova

Nell’attuale form Elenco Avvocati, risultato dell’attivazione della funzione Ricerca del precedente menu


Figura 46: Form Elenco Difensori - Attuale

sarà oscurata la funzione di modifica dell’avvocato, mentre la funzione di cancellazione, che è riportata solo se l’avvocato non è associato ad alcun procedimento SIES, rimarrà per permettere la cancellazione di avvocati inseriti precedentemente al rilascio degli interventi previsti in questo documento, pertanto la form sarà


Figura 47: Form Elenco Difensori - Nuova
## Basi dati
Per oscurare la funzione di Inserimento Avvocato, sarà realizzato e distribuito un apposito script che provvederà ad aggiornare la colonna DATA_FINE_VALIDITA per i records della tabella FUNZIONE_PROFILO riferiti alle funzioni Inserimento Avvocato e Modifica Avvocato.
## WEB services
N.A.
## XSD
N.A.
## Configurazione
N.A.
## Tutorial
N.A.
## REQ- SIE-021-05_FN.01 – Bonifica Anagrafica Avvocati SIES
### Bonifica dei dati presenti nella tabella Avvocato
Prima di rendere effettiva in esercizio l’integrazione del SIES con il sistema ReGIndE sarà effettuata una bonifica al fine di allineare i dati presenti nella tabella ‘AVVOCATO’ del SIES a quelli presenti su ReGIndE..

Prerequisiti per la realizzazione della bonifica sono:

la messa a disposizione da parte di ReGIndE di un file excel contenente l’estrazione delle anagrafiche degli Avvocati, attivi, presenti su quella base dati. Nel caso che il file contenga più record per lo stesso avvocato, a fronte di più record di indirizzi con tipologia a ‘D’, sarà selezionato il primo ottenuto ordinando alfabeticamente la colonna Indirizzo;
l’aggiornamento della tabella COMUNE di SIES, come descritto nel cap. 6.6.
Come già riportato al par. 6.2.3.1 pag. 39 la descrizione del Luogo Nascita, presente in ReGIndE, non sempre corrisponde a quella legalmente riconosciuta come denominazione di un Comune italiano, per questo motivo il comune di nascita dell’avvocato, sarà ricavato utilizzando il codice Belfiore contenuto nel suo Codice Fiscale, dato sempre presente in ReGIndE.
Questo codice sarà poi utilizzando per estrarre dalla tabella COMUNE di SIES il codice Istat corrispondente, che valorizzerà la colonna COD_LUOGO_NASCITA della tabella AVVOCATO SIES.

Nel caso in cui il codice Belfiore di un AVVOCATO ReGIndE non esista nella tabella COMUNE del SIES, l’AVVOCATO non sarà preso in considerazione ai fini della Bonifica e sarà inserito in una tabella degli Scarti della procedura.
L’Elenco dei Comuni mancanti in SIES sarà inviato all’Amministrazione – Gruppo Tabelle fisse perché provveda ad eseguire gli opportuni accertamenti e a preparare uno script di aggiornamento della tabella COMUNE.

Sarà realizzata una procedure plsql che agirà su tutte le anagrafiche presenti su SIES che risultino associate ad almeno un fascicolo con procedimenti in corso.
In particolare:
Per SIEP, saranno presi in considerazione i procedimenti con stato diverso da Definito/Archiviato;
Per SIUS e SIGE, saranno presi in considerazione i procedimenti pendenti alla data della bonifica;
Per tutti e tre i sottosistemi non saranno considerati i procedimenti provenienti da BDI differenti da quella del Distretto su cui sarà eseguita la bonifica.
Confronterà i dati presenti sui due sistemi e bonificherà i dati anagrafici di ciascun avvocato SIES, compreso il dato relativo al foro di appartenenza, a parità di anagrafica trovata su ReGIndE.
Ogni anagrafica così bonificata avrà il FLAG_REGINDE = ‘Sì’ e sarà associata ad un codice ufficio di appartenenza fittizio ( ‘00000’), in modo tale che l’avvocato risulti visibile al livello distrettuale.

I dati che saranno presi in considerazione per effettuare il confronto saranno:
Cognome
Nome
Luogo di Nascita
Data di Nascita
Foro di Appartenenza
Codice Fiscale
Questo garantirà l’univocità delle anagrafiche sul sistema SIES, ovviando all’attuale duplicazione dovuta al fatto che ad ogni ufficio è permesso l’inserimento di un Avvocato anche se già presente in banca dati.

La procedura in oggetto agirà, previo preventivo backup, sulla tabella ‘AVVOCATO’ del SIES e dovrà essere elaborata su ciascun distretto SIES.

Le anagrafiche che non saranno bonificate in automatico, secondo i criteri su descritti, rimarranno inalterate e, quindi, NON BONIFICATE.
Il FLAG_REGINDE, per queste, sarà valorizzato a ‘No’ e, proprio in base a tale criterio, esse saranno escluse da qualsiasi selezione operata nel sistema.
In sostanza, queste anagrafiche non saranno più visibili né gestite dal sistema SIES e saranno, invece, storicizzate analogamente a quanto indicato al § “6.1 REQ-SIE-021-01_FN.01 - Gestione Nuovi Fori (FORO di NAPOLI NORD)” e “congelate” per come sono.

Effettuata tale operazione, la stessa procedura provvederà a bonificare anche tutte le tabelle che abbiano una relazione con l’avvocato bonificato, aggiornandone il riferimento.

Di seguito, l’elenco delle tabelle interessate dalla bonifica:

AVVOCATO_FASCICOLO_SIEP
AVVOCATO_FASCICOLO_SIUS
AVVOCATO_FASCICOLO_SIGE
PARTI_UDIENZA_DIFENSORE
STORICO_AVVOCATO
AVVISI_AVVOCATO
NUOVA_ISTANZA.

Si ricorda che al momento in SIES il collegamento tra atti ed Avvocato è assicurato tramite chiave esterna all’ID_AVVOCATO. Tutti i riferimenti ai dati dell’Avvocato vengono estratti dal record Avvocato collegato al procedimento (es. sede ed indirizzo studio, riportato in molti template ed alcune forms). A valle dell’analisi e studio di dati estratti e forniti dall’Amministrazione, uno dei motivi di maggiore ricorrenza di duplicazione dell’avvocato in SIES è la non corrispondenza dell’indirizzo dello studio, riportato negli atti, tra quelli presenti in base dati. A seguito della bonifica, non dando valore all’indirizzo ai fini dell’accorpamento, tutti gli avvocati bonificati, aventi i restanti dati indicati in precedenza uguali,  e aventi precedentemente indirizzi differenti, faranno tutti riferimento all’ indirizzo importato da ReGIndE.

## Moduli sw
N.A.
## Architettura
N.A.
## Interfacce utente
N.A.
## Basi dati
Per l’importazione dei dati forniti da ReGIndE sarà creata una nuova tabella di appoggio W_AVV_REGINDE e sarà realizzata una procedure plsql Importa_avv_ReGIndE.

Nella tabella tabellefisse18novembre2020.xlsx, fornita dall’Amministrazione, sono presenti 388221 records di cui 13719 riferiti ad Avvocatura Stato, CNF ed Enti, tali records non saranno presi in considerazione ai fini dell’attività di bonifica.

Alla tabella AVVOCATO di SIES saranno aggiunte nuove colonne: PEC, PROC_PENDENTI, FLAG_REGINDE, ID_AVV_BONIFICATO, DESCR_COMUNE_STUDIO.

Sarà realizzata la procedure PLSQL BONIFICA_AVVOCATI per la bonifica dei dati della tabella AVVOCATO, che eseguirà le seguenti operazioni:

per ciascun record della tabella AVVOCATO di SIES verificherà se ad esso sono collegati procedimenti SIEP o SIUS o SIGE ancora pendenti, in caso affermativo valorizzerà la colonna PROC_PENDENTI a ‘SI’, diversamente a ‘NO’;
per ciascun record della tabella AVVOCATO di SIES verificherà se ad esso sono collegati solamente procedimenti SIEP o SIUS o SIGE non appartenenti alla BDI su cui si sta eseguendo la procedura , in caso affermativo valorizzerà la colonna PROC_PENDENTI a ‘NO’;
per tutti i records AVVOCATO sarà preimpostato il FLAG_REGINDE a ‘NO’;
inizierà la lettura dei records dalla tabella W_AVV_REGINDE, per ciascun record letto saranno ricercati nella tabella AVVOCATO di Sies i records aventi Cognome, Nome, Luogo di Nascita, Data di Nascita, Foro di Appartenenza, Codice Fiscale uguali a quelli del record proveniente da ReGIndE e PROC_PENDENTI = ‘SI’. Poiché ci possono essere su SIES più records AVVOCATO soddisfacenti le suddette condizioni, si procederà ad aggiornare il record con data_inserimento più recente impostando il FLAG_REGINDE = ‘SI’ e FLAG_CANCELLATO = ‘N’, mentre per gli altri records si procederà ad impostare  FLAG_CANCELLATO = ‘S’ e a valorizzare ID_AVVOCATO_BONIFICATO con l’ID dell’avvocato impostato con FLAG_REGINDE = ‘SI’;
al termine della lettura di tutti i records della tabella W_AVV_REGINDE e dell’attività di aggiornamento della tabella avvocato, si procederà, per tutti i records aventi la colonna ID_AVVOCATO_BONIFICATO valorizzata, ad eseguire:
update records tabella AVVOCATO_FASCICOLO_SIUS aventi AVV_ID_AVVOCATO = ID_AVVOCATO impostando AVV_ID_AVVOCATO = ID_AVVOCATO_BONIFICATO;
update records tabella AVVOCATO_FASCICOLO_SIEP aventi AVV_ID_AVVOCATO = ID_AVVOCATO impostando AVV_ID_AVVOCATO = ID_AVVOCATO_BONIFICATO;
update records tabella AVVOCATO_FASCICOLO_SIGE aventi AVV_ID_AVVOCATO = ID_AVVOCATO impostando AVV_ID_AVVOCATO = ID_AVVOCATO_BONIFICATO;
up update records tabella PARTI_UDIENZA_DIFENSORE aventi AVV_ID_AVVOCATO = ID_AVVOCATO impostando AVV_ID_AVVOCATO = ID_AVVOCATO_BONIFICATO;
update records tabella STORICO_AVVOCATO aventi AVV_ID_AVVOCATO = ID_AVVOCATO impostando AVV_ID_AVVOCATO = ID_AVVOCATO_BONIFICATO;
date records tabella AVVISI_AVVOCATO aventi AVV_ID_AVVOCATO = ID_AVVOCATO impostando AVV_ID_AVVOCATO = ID_AVVOCATO_BONIFICATO;
update records tabella NUOVA_ISTANZA aventi AVV_ID_AVVOCATO = ID_AVVOCATO impostando AVV_ID_AVVOCATO = ID_AVVOCATO_BONIFICATO.
E’ da valutare se procedere immediatamente o a distanza di un certo periodo alla cancellazione fisica dei records AVVOCATO con ID_AVVOCATO_BONIFICATO valorizzato o lasciarli nella base dati, essendo comunque cancellati logicamente (FLAG_CANCELLATO = ‘S’ e FLAG_REGINDE =’NO’), quindi non più utilizzabili per nuove assegnazioni.

Chiaramente, come da normale prassi, prima di iniziare le attività di aggiornamento della base dati sarà eseguito un backup di tutte le tabelle interessate.
## WEB services
N.A.
## XSD
N.A.
## Configurazione
N.A.
## Tutorial
N.A.
## REQ- SIE-021-06_FN.01 – Aggiornamento Tabelle COMUNE e CG_REF_CODES di SIES
Prima di procedere alla bonifica dei dati presenti nella tabella ‘AVVOCATO’ del SIES con quelli presenti su ReGIndE, bisognerà aggiornare le tabelle di SIES, COMUNE e CG_REF_CODES, limitatamente ai domini PROVINCIA, REGIONE e NAZIONE, con i dati presenti nelle tabelle fisse COMUNE, PROVINCIA, REGIONE e STATO-NAZIONE fornite dalla DGSIA. Realizzando di fatti un allineamento fra i due ambienti, che permetterà la gestione della tabella COMUNE di SIES da parte del gruppo tabelle fisse dell’Amministrazione.

La tabella COMUNE di SIES aggiornata sarà ridistribuita in tutti i Distretti in sostituzione della preesistente.

Poiché queste attività di aggiornamento sono propedeutiche alle attività relative alla nuova gestione degli avvocati, è ipotizzabile un rilascio delle stesse in due diversi momenti: il primo ingloberebbe le attività di aggiornamento descritte in questo capitolo, il secondo tutte le restanti. In tal modo si avrebbe modo di testare approfonditamente il corretto funzionamento degli interventi relativi all’allineamento alle tabelle fisse.

Chiaramente come da normale prassi, prima di iniziare le attività di aggiornamento della base dati sarà eseguito un backup di tutte le tabelle interessate.

### Aggiornamento dei dati presenti nella tabella COMUNE di SIES
La tabella COMUNE di SIES, sostanzialmente ferma al momento del caricamento iniziale (anno 2003), sarà aggiornata con i dati presenti nella tabella COMUNE della DGSIA, in cui è presente anche il codice catastale, che come indicato nei capitoli 6.2 e 6.5, sarà un dato essenziale per la valorizzazione del comune di nascita dell’avvocato, desumendolo dal codice fiscale importato da ReGIndE.

L’attuale tabella COMUNE di SIES, che contiene al momento  8113 records, non gestisce la storicizzazione dei comuni, attraverso una data fine validità, ma è presente solo un FLAG_VALIDITA, che al momento è valorizzato ad ‘N’ solo per il comune fittizio di ‘NAPOLI NORD’, utilizzato per escludere il comune dalle funzioni di ricerca.

La tabella è cosi strutturata

| Nome Colonna | Contenuto |
| --- | --- |
| COD_COMUNE | Codice Istat |
| COD_PROVINCIA | Codice Provincia |
| DESCRIZIONE | Denominazione Comune |
| CAP | Codice Avviamento Postale |
| DATA_CARICAMENTO_REGE | Data Caricamento in SIES |
| COD_SEDE_GIUDIZIARIA | Codice Circondario Competente |
| FLAG_VALIDITA | ‘S’ se valido, ‘N’ non valido |


La tabella COMUNE DGSIA, contenente 13251 record, gestisce la storicizzazione dei comuni, che hanno subito cambi di provincia, cambi di denominazione, accorpamenti con altro comune, attraverso l’utilizzo di una data fine validità. I Comuni al momento attivi, cioè con data fine validità non valorizzata, sono 7907.

La tabella è cosi strutturata

| Nome Colonna | Contenuto |
| --- | --- |
| COD_COMUNE | Codice Istat |
| COD_PROVINCIA | Codice Provincia |
| COD_SEDE_GIU_TRIB_COMP | Codice Circondario Competente |
| DESC_COMUNE | Denominazione Comune |
| DATA_FINE_VALIDITA | Data fine validità del codice comune |
| CAP | Codice Avviamento Postale |
| COD_CATASTALE | Codice Catastale |


Per poter procedere all’aggiornamento, la tabella COMUNE di SIES sarà modificata con l’aggiunta delle seguenti colonne: DATA_FINE_VALIDITA, COD_CATASTALE, DATA_AGGIORNAMENTO

Per l’aggiornamento della tabella COMUNE SIES saranno realizzate le seguenti attività:

import dei dati della tabella COMUNE DGSIA su una tabella di appoggio SIES COMUNE_DGSIA;
realizzazione di una procedure PLsql che per ciascun record letto nella tabella COMUNE_DGSIA effettuerà le seguenti operazioni:
se nella tabella COMUNE SIES esiste un record avente COD_COMUNE con lo stesso COD_COMUNE in input, il sistema procederà ad aggiornare le colonne COD_PROVINCIA, DESCRIZIONE, CAP, COD_SEDE_GIUDIZIARIA, COD_CATASTALE, DATA_FINE_VALIDITA con i valori presenti nelle colonne  COD_PROVINCIA, DESC_COMUNE, CAP, COD_SEDE_GIU_TRIB_COMP, COD_CATASTALE, DATA_FINE_VALIDITA della tabella della DGSIA. Inoltre, se la DATA_FINE_VALIDITA non è NULL, sarà impostato la colonna FLAG_VALIDITA a ‘N’, negli altri casi a ‘S’;  sarà sempre valorizzata la DATA_AGGIORNAMENTO con la data di elaborazione;
se nella tabella COMUNE SIES non esiste un record avente COD_COMUNE con lo stesso COD_COMUNE in input, il sistema procederà ad inserire un nuovo record valorizzando le colonne COD_COMUNE, COD_PROVINCIA, DESCRIZIONE, CAP, COD_SEDE_GIUDIZIARIA, COD_CATASTALE, DATA_FINE_VALIDITA con i valori presenti nelle colonne  COD_COMUNE, COD_PROVINCIA, DESC_COMUNE, CAP, COD_SEDE_GIU_TRIB_COMP, COD_CATASTALE, DATA_FINE_VALIDITA della tabella della DGSIA. Inoltre, se la DATA_FINE_VALIDITA non è NULL, sarà impostato la colonna FLAG_VALIDITA a ‘N’, negli altri casi a ‘S’; saranno sempre valorizzate le colonne DATA_CARICAMENTO_REGE e DATA_AGGIORNAMENTO con la data di elaborazione.
al termine della procedura di aggiornamento, al fine di avere un perfetto allineamento delle due tabelle, tutti i records della tabella COMUNE SIES con data aggiornamento non valorizzata saranno estratti e trasmessi al Gruppo Tabelle fisse della DGSIA perché provveda all’inserimento dei Comuni nella propria tabella fissa.
La colonna COD_SEDE_GIUDIZIARIA contiene il codice (di 3 cifre), che identifica il Circondario giudiziario, competente per territorio. Sostanzialmente è utilizzato per risalire dal Comune di nascita di un Soggetto alla Sede del Casellario Giudiziale competente alla conservazione delle sentenze di condanna a suo carico, a cui indirizzare i provvedimenti emessi in SIES. Per facilitare l’individuazione del Casellario competente su un soggetto condannato, al momento dell’iscrizione in SIES di un nuovo soggetto, insieme al valore del COD_COMUNE viene riportato anche il valore di COD_SEDE_GIUDIZIARIA. A tale proposito si fa presente che al momento tutti i comuni, appartenenti a Sedi Giudiziarie soppresse (settembre 2013), non risultano aggiornati con il valore della nuova sede competente, per cui nei template risultano destinatari di atti ancora i vecchi Casellari Giudiziari. Il problema è presente anche in Tabella Fissa Comune. Occorrerà approntare degli script per procedere all’aggiornamento della COD_SEDE_GIUDIZIARIA in entrambi gli ambienti. Questo aggiornamento avrà effetto solo sui records SOGGETTO di nuova iscrizione, in quanto l’aggiornamento si limiterà alla sola tabella COMUNE e non riguarderà la tabella SOGGETTO.

A seguito dell’aggiornamento della tabella COMUNE bisognerà aggiornare anche la tabella CODICI_SIES_NSC, utilizzata nel modulo di interoperabilità SIES-NSC, per i records con CO_DOMAIN = ‘COMUNE’, modificando il valore della colonne CO_SIES_DES per quei comuni per cui vi sarà una modifica della Denominazione e l’inserimento di nuovi record per quei comuni aggiunti nella tabella COMUNE.

Nessun intervento dovrà essere effettuato su NSC.
Per quanto riguarda SIUS-Avvocati, è presente nello schema AVVSIES la tabella COMUNI, che è una copia fedele della tabella COMUNE di SIES e quindi si procederà all’aggiornamento anche di questa tabella con le stesse modalità previste per la tabella COMUNE.

Dal momento in cui il Gruppo tabelle fisse prenderà in carico la gestione della tabella COMUNE di SIES, per ogni nuovo aggiornamento, oltre alla trasmissione di tutti i valori inseriti nella tabella COMUNE DGSIA, dovrà valorizzare anche il FLAG_VALIDITA a ‘S’ se DATA_FINE_VALIDITA non valorizzata, a ‘N’ in caso contrario.
### Aggiornamento dei dati presenti nella tabella CG_REF_CODES (domini PROVINCIA,REGIONE,NAZIONE)
Il Gruppo tabelle fisse della DGSIA ha fornito anche le tabelle PROVINCIA, REGIONE, STATO-NAZIONE, che non possono essere adottate nella loro struttura da SIES, in quanto richiederebbero importanti interventi sul software.

In SIES i dati riportati nelle suddette tabelle sono gestite nella tabella delle decodifiche CG_REF_CODES, rispettivamente nei domini PROVINCIA, REGIONE e NAZIONE.

I domini aggiornati saranno ridistribuiti in tutti Distretti in sostituzione di quelli preesistenti.
### Aggiornamento dominio PROVINCIA
La tabella PROVINCIA (DGSIA) è strutturata in records con le colonne COD_PROVINCIA, COD_REGIONE, DESC_PROVINCIA, FINE_VALIDITA.

I records della CG_REF_CODES riferiti alla ‘PROVINCIA’ hanno la colonna RV_DOMAIN = ‘PROVINCIA’, RV_LOW_VALUE= sigla provincia,  RV_MEANING = denominazione Provincia e RV_ABBREVIATION non valorizzato.
Per l’aggiornamento del dominio ‘PROVINCIA’ sarà realizzata una procedura che leggendo i records presenti nella tabella PROVINCIA della DGSIA, importata in una tabella d’appoggio di SIES,  effettuerà le seguenti operazioni:

se nella tabella CG_REF_CODES esiste un record avente RV_DOMAIN = ‘PROVINCIA’ e RV_LOW_VALUE = COD_PROVINCIA del record in  input, il sistema procederà ad aggiornare le colonne RV_MEANING, RV_ABBREVIATION con i valori presenti nelle colonne  DESC_PROVINCIA, COD_REGIONE del record in input;
se nella tabella CG_REF_CODES non esiste un record avente RV_DOMAIN = ‘PROVINCIA’ e RV_LOW_VALUE = COD_PROVINCIA del record in  input, il sistema procederà ad inserire un nuovo record valorizzando le colonne con RV_DOMAIN = ‘PROVINCIA’ e RV_LOW_VALUE, RV_ABBREVIATION, RV_MEANING rispettivamente con i valori contenuti nelle colonne COD_PROVINCIA, COD_REGIONE, DESC_PROVINCIA del record in input;
al termine della procedura di aggiornamento, al fine di avere un perfetto allineamento delle due tabelle, tutti i records della tabella CG_REF_CODES con RV_DOMAIN = ‘PROVINCIA’ e  con RV_ABBREVIATION non valorizzata saranno estratti e trasmessi alla DGSIA perché provveda all’inserimento dei Comuni nella propria tabella fissa.
In SIES non vi è alcuna gestione della Provincia (es. selezione di un Comune dopo aver selezionato la Provincia), il dato viene ereditato direttamente dal Comune (valore del COD_PROVINCIA), pertanto si ritiene che la non gestione della fine validità non abbia alcun impatto. Al solo scopo di tenerne traccia in SIES, nella suddetta procedura per i records PROVINCIA con FINE_VALIDITA = ‘SI’  sarà impostata nella CG_REF_CODES la colonna RV_ALT2_VALUE = ‘N’.

In caso di aggiornamento della tabella fissa PROVINCIA, il Gruppo tabelle fisse della DGSIA dovrà trasmettere le modifiche anche a SIES.
### Aggiornamento dominio REGIONE
I records della CG_REF_CODES riferiti alla ‘REGIONE’ hanno la colonna RV_DOMAIN = ‘REGIONE’ e RV_DOMAIN = Valore Codice Regione, RV_MEANING = Descrizione della Regione.

La tabella REGIONE è strutturata in records con le colonne COD_REGIONE e DESC_REGIONE.

I valori records contenuti nella CG_REF_CODES corrispondono sostanzialmente con i valori dei records contenuti nella tabella REGIONE.

Bisognerà solo aggiornare le denominazioni delle seguenti records della CG_REF_CODES con quelle presenti nella tabella REGIONE

| Attuale denominazione RV_MEANING | Nuova denominazione (presente in REGIONE) |
| --- | --- |
| VALLE D'AOSTA | VAL D'AOSTA |
| TRENTINO-ALTO ADIGE | TRENTINO ALTO ADIGE |
| FRIULI-VENEZIA GIULIA | FRIULI V. GIULIA |
| EMILIA-ROMAGNA | EMILIA ROMAGNA |


Ai fini di un perfetto allineamento di SIES alla tabella DGSIA nella CG_REF_CODES sarà inserito un nuovo record per la Regione ‘LUOGO SCONOSCIUTO’ (codice 21) presente nella tabella fissa.

Viceversa per l’allineamento della tabella REGIONE al contenuto dei records del dominio REGIONE di SIES, bisognerebbe inserire nella tabella fissa un record con COD_REGIONE = ‘-‘ e
DESC_REGIONE =‘-‘.

Considerando il numero limitato di records da modificare l’allineamento su SIES sarà effettuato manualmente.

In caso di aggiornamento della tabella fissa REGIONE, il Gruppo tabelle fisse della DGSIA dovrà trasmettere le modifiche anche a SIES.
### Aggiornamento dominio NAZIONE
I records della CG_REF_CODES riferiti alla ‘NAZIONE’ hanno la colonna RV_DOMAIN = ‘NAZIONE’, RV_LOW_VALUE= codice dello stato  e RV_MEANING = descrizione dello stato.

La tabella STATO-NAZIONE è strutturata in records con le colonne COD_STATO, DESC_STATO, COD_CASELLARIO, DATA _FINE_VALIDITA, COD_STATO_ISO, COD_ISTAT_STATO.

Per l’aggiornamento del dominio ‘NAZIONE’ sarà realizzata una procedura che leggendo i records presenti nella tabella STATO_NAZIONE della DGSIA, importata in una tabella d’appoggio di SIES, effettuerà le seguenti operazioni:

se nella tabella CG_REF_CODES esiste un record avente RV_DOMAIN = ‘NAZIONE’ e RV_LOW_VALUE = COD_STATO del record in  input, il sistema procederà ad aggiornare le colonne RV_MEANING, RV_HIGH_VALUE, RV_ABBREVIATION con i valori presenti nelle colonne  DESC_STATO, COD_STATO_ISO, COD_ISTAT_STATO del record in input;
se nella tabella CG_REF_CODES non esiste un record avente RV_DOMAIN = ‘NAZIONE’ e RV_LOW_VALUE = COD_ STATO del record in  input, il sistema procederà ad inserire un nuovo record valorizzando le colonne con RV_DOMAIN = ‘NAZIONE’ e RV_LOW_VALUE, RV_HIGH_VALUE, RV_ABBREVIATION, RV_MEANING rispettivamente con i valori contenuti nelle colonne COD_ STATO, COD_STATO_ISO, COD_ISTAT_STATO, DESC_STATO del record in input;
al termine della procedura di aggiornamento, al fine di avere un perfetto allineamento delle due tabelle, tutti i records della tabella CG_REF_CODES con RV_DOMAIN = ‘NAZIONE’ e  con RV_HIGH_VALUE non valorizzata saranno estratti e trasmessi alla DGSIA perché provveda all’inserimento degli Stati di SIES nella propria tabella fissa.
In SIES la Nazionalità viene gestita sul SOGGETTO, nella valorizzazione dei campi Stato Cittadinanza e Stato Nascita, e sulla RESIDENZA, nella valorizzazione del campo Stato, e ovviamente al momento vengono estratti tutti i records riferiti al dominio NAZIONE, non essendoci una gestione della validità o meno della stessa. Nella tabella fissa STATO-NAZIONE su 263 records solo 5 risultano con DATA_FINE_VALIDITA valorizzata. Al solo scopo di tenerne traccia in SIES, nella suddetta procedura per i records STATO-NAZIONE con DATA_FINE_VALIDITA sarà impostata nella CG_REF_CODES la colonna RV_ALT2_VALUE = ‘N’.

A seguito dell’aggiornamento del dominio NAZIONE della CG_REF_CODES bisognerà aggiornare anche la tabella CODICI_SIES_NSC, utilizzata nel modulo di interoperabilità SIES-NSC, per i records con CO_DOMAIN = ‘NAZIONE’, modificando il valore della colonne CO_SIES_DES per quelli per cui vi sarà una modifica della Denominazione e l’inserimento di nuovi record per quelle NAZIONI aggiunti nella tabella CG_REF_CODES, dopo verifica dell’esistenza degli stessi nella equivalente tabella di NSC (DC_TAB_STATO_ESTERO). Eventuali Nazioni aggiunte nella CG_REF_CODES ed assenti in NSC, saranno segnalate agli amministratori di quel Sistema per le opportune verifiche.

Nessun intervento dovrà essere effettuato su NSC, a livello applicativo.
Per quanto riguarda SIUS-Avvocati, è presente nello schema AVVSIES la tabella STATI, che è una copia fedele del dominio NAZIONE della tabella CG_REF_CODES di SIES e quindi si procederà all’aggiornamento anche di questa tabella con le stesse modalità previste il suddetto dominio.

In caso di aggiornamento della tabella fissa STATO-NAZIONE, il Gruppo tabelle fisse della DGSIA dovrà trasmettere le modifiche anche a SIES.
## Moduli sw
A seguito della storicizzazione di alcuni Comuni, che nel tempo hanno subito cambi di Provincia di appartenenza, bisognerà modificare i seguenti moduli software per permettere all’utente in fase di inserimento e aggiornamento di un soggetto di poter selezionare il comune di nascita in base alla Provincia di appartenenza dello stesso al momento della nascita:

siap.sico.soggetto.action.ActInserisciSoggetto

siap.sico.decodifiche.dao.ComuneDAO

siap.sico.decodifiche.action.ActVisualizzaComuni

siap.sico.comune.RicercaComune.jsp

siap.sico.soggetto.action.ActModificaSoggetto

siap.siep.fascicolo.action.ActLoadInserisciResidenzaFascicolo

siap.sico.webservice.action.ActNscToSiesLoadSoggetto.java
## Architettura
N.A.
## Interfacce utente
Al momento le funzioni di Inserimento e Modifica soggetto, in fase di conferma, controllano, fra l’altro, l’univocità ed esistenza nella tabella COMUNE di un record avente DESCRIZIONE = comune digitato e FLAG_VALIDITA = ‘S’, in caso di esistenza di comuni omonimi, il sistema invia il seguente messaggio bloccante


In questo caso l’utente deve selezionare il comune dalla popup che si apre cliccando l’apposito link presente sulla form, in cui impostando la ricerca per Comune, riceve la form simile alla seguente



da cui può selezionare il Comune di interesse e proseguire con l’attività di aggiornamento del Soggetto.

A seguito dell’attività di aggiornamento della tabella Comune che comporterà la storicizzazione dei Comuni che hanno subito cambi di Provincia, a differenza dell’attuale situazione, si creeranno diversi Comuni con uguale descrizione, ma con diversa valorizzazione delle colonne FLAG_VALIDITA e DATA_VALIDITA. Ai fini della veridicità dei dati anagrafici di un Soggetto, a parità di descrizione, è significativo poter inputare il Comune con la Provincia di appartenenza, valida al momento della nascita. Pertanto si modificherà l’attuale controllo sulla omonimia di un Comune, estendendola anche ai comuni con  FLAG_VALIDITA = ‘N’, per cui il sistema invierà il messaggio di esistenza di omonimia, anche in caso di comune storicizzato.
Sarà inoltre modificata la popup di selezione dei comuni, riportando nell’elenco dei Comuni omonimi anche la relativa data di Fine Validità



da cui l’utente potrà selezionare il Comune di interesse.
## Basi dati
Alla tabella COMUNE saranno aggiunte le seguenti colonne DATA_FINE_VALIDITA, COD_CATASTALE, DATA_AGGIORNAMENTO.

Per l’aggiornamento della tabella COMUNE sarà realizzata la procedure PLSQL Aggiorna_COMUNE_SIES.

Per l’aggiornamento della tabella CODICI_SIES_NSC, relativamente ai records del domino ‘COMUNE’, sarà realizzata la procedure PLSQL Aggiorna_COMUNE_SIES_NSC.

Per l’aggiornamento della tabella COMUNI sarà realizzata la procedure PLSQL Aggiorna_COMUNI.

Per l’aggiornamento del dominio  PROVINCIA della CG_REF_CODES sarà realizzata la procedure PLSQL Aggiorna_PROVINCIA_SIES.

Per l’aggiornamento del dominio  NAZIONE della CG_REF_CODES sarà realizzata la procedure PLSQL Aggiorna_NAZIONE_SIES.

Per l’aggiornamento della tabella CODICI_SIES_NSC, relativamente ai records del domino ‘NAZIONE, sarà realizzata la procedure PLSQL Aggiorna_NAZIONE_SIES_NSC.

Per l’aggiornamento della tabella STATI sarà realizzata la procedure PLSQL Aggiorna_STATI_SIES_AVV.
## WEB services
N.A.
## XSD
N.A.
## Configurazione
N.A.
## Tutorial
N.A.