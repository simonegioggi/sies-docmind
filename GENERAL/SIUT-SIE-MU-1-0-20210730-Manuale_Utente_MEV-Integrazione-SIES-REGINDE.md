---
uniqueName: siut-sie-mu-1-0-20210730-manualeutentemev-integraz
displayName: "SIUT SIE MU 1 0 20210730 Manuale Utente MEV Integrazione SIES REGINDE"
category: "GENERAL"
tags: []
---

# SIUT-SIE-MU-1.0-20210730-Manuale_Utente_MEV-Integrazione SIES-REGINDE

> **File originale:** `MEV/SCHEDA_021/Docs/consegna docx/ORIGINALS/Documentazione consegna Scheda-21/SIUT-SIE-MU-1.0-20210730-Manuale_Utente_MEV-Integrazione SIES-REGINDE.docx`  
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
| Elaborato da | Engineering | RTI |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 30/07/2021 |  |
| Livello di riservatezza | L3 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 30/07/2021 | Prima emissione |  |
|  |  |  |  |



Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Salvatore Piazza | RTI |  | Technical Manager |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Francesco Rosati | RTI |  | Responsabile Manutenzione Correttiva
Referente Qualità e Sicurezza |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Referente PMO e Qualità |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |
| Luigi Buglione | RTI |  | Referente Metrico |


INDICE DEI CONTENUTI
1.	Introduzione	5
1.1.	Scopo del documento	5
1.2.	Glossario	5
1.2.1.	Definizioni	5
1.2.2.	Acronimi e abbreviazioni	5
2.	Gestione Nuovi Fori ( Napoli Nord)	7
2.1.	Scopo dell’applicativo	7
2.2.	Gestione Alerts per procedimenti con avvocati non certificati ReGIndE	11
2.2.1.	Sottosistema SIEP	12
2.2.2.	Sottosistema SIUS	13
2.2.3.	Sottosistema SIGE	15
3.	Gestione Difensori con certificazione su ReGIndE	18
3.1.	Sottosistema SIEP	18
3.1.1.	Assegnazione Difensore	18
3.1.2.	Sostituzione Difensore	31
3.1.3.	Inserimento Istanza	36
3.2.	Sottosistema SIUS	40
3.2.1.	Assegnazione Difensore	40
3.2.2.	Sostituzione Difensore	55
3.3.	Sottosistema SIGE	60
3.3.1.	Assegnazione Difensore	60
3.3.2.	Sostituzione Difensore	73
3.3.3.	Gestione Difensore su Parti Civili/Offese	78
4.	Gestione DIFENSORI in Funzioni Amministrative	85
4.1.	Eliminazione funzione Inserimento Difensore	85
4.2.	Eliminazione funzione Modifica Difensore	85
5.	Gestione Luogo Nascita Soggetto	88
5.1.	Sottosistema SIEP	88
5.2.	Sottosistema SIUS	96
5.3.	Sottosistema SIGE	97

# Introduzione
## Scopo del documento
Nel documento sono descritti gli interventi realizzati nel sistema SIES con lo scopo finale di ‘abilitare’ i vari sistemi distrettuali del SIES all’interconnessione con il sistema del Registro Generale degli Indirizzi Elettronici (ReGIndE), in modo da avere un’entità DIFENSORE ‘certificata’, e nello stesso tempo di introdurre la gestione dei nuovi fori, in particolare la gestione del FORO di NAPOLI NORD.

L’intervento mira ad una gestione coerente ed auto consistente dell’entità DIFENSORE nell’interezza di tutto il sistema SIES, pertanto le varie dinamiche di implementazione hanno riguardato i tre sottosistemi SIEP, SIUS e SIGE.

Si fa presente che nel prosieguo del documento si farà sempre riferimento ad un’interconnessione, del SIES verso il ReGIndE, in una modalità di tipo ‘diretta’, ossia il sistema SIES, per le casistiche previste dai requisiti, farà un accesso diretto ai servizi esposti dal sistema del Registro Generale degli Indirizzi Elettronici tramite invocazione dei metodi necessari sugli appositi endpoint pubblicati su rete giustizia.

Dal momento dell’installazione della release, che ingloberà le modifiche descritte nel presente documento, i procedimenti SIEP, SIUS e SIGE dovranno essere assegnati a Difensori certificati ReGIndE.



## Glossario
## Definizioni
Si premette un glossario esplicativo delle abbreviazioni e dei termini tecnici e giuridici utilizzati nel documento (Tabella - Glossario dei termini e degli acronimi usati nel documento).

| Definizione | Descrizione |
| --- | --- |
| ReGIndE | Registro Generale degli Indirizzi Elettronici |
| Portal Liferay | Liferay è un entreprise portal free e open Source |
| PDF | Portable Document Format – Standard per scambio documenti elettronici |
| P7M | Estensione file firmato con modalità CAdES, ovvero il documento firmato ed il file con la firma digitale vengono inseriti insieme in una busta. |
| PDF Firmato | Firma digitale apposta con modalità PAdES in cui vengono sfruttate le caratteristiche dei documenti in formato pdf. Il file contenente la firma digitale viene inglobato insieme al documento stesso. |
| Web-based | Un programma in cui tutte le funzioni sono accessibili tramite un normale web-browser come Firefox, Chrome o Explorer. Questo significa che non è necessario effettuare l’installazione di alcun software sui computer dell’azienda che deve utilizzare il programma. |


## Acronimi e abbreviazioni
| Sigla | Descrizione |
| --- | --- |
| GSU | Gestione Servizi UNEP |
| PDOC | Sistema Piattaforma Documentale |
| PEC | Posta Elettronica Certificata |
| PST | Portale dei Servizi Telematici |
| REGE | Registro Generale delle Notizie di Reato |
| RG | Registro Generale |
| SNT | Sistema Notifiche Telematiche |
| UNEP | Ufficio Notificazioni Esecuzioni Protesti |
| XML | eXtensible Markup Language |


# Gestione Nuovi Fori ( Napoli Nord)
## Scopo dell’applicativo
Al fine di poter gestire correttamente l’istituzione di nuovi fori, in particolare il Foro di Napoli NORD, e di svincolare la denominazione del foro dal comune sede del Foro, sono stati fatti diversi interventi sulla base dati e sull’applicazione. Inoltre dovendo il sistema SIES adeguarsi nella gestione degli avvocati al sistema ReGIndE, sono state apportate anche modifiche alle denominazioni di alcuni fori SIES, preesistenti.
In particolare sono state apportate le seguenti modifiche alla tabella di Gestione dei Fori dei difensori:

| Foro | Comune Sede | Tipo di attività esguita |
| --- | --- | --- |
| NAPOLI NORD | AVERSA | Inserito nuovo record |
| FORLÌ-CESENA | FORLI’ | Modificata precedente denominazione “FORLI’ “ |
| MASSA-CARRARA | MASSA | Modificata precedente denominazione “MASSA “ |
| REGGIO EMILIA | REGGIO NELL’EMILIA | Modificata precedente denominazione “REGGIO NELL’EMILIA “ |
| REGGIO CALABRIA | REGGIO DI CALABRIA | Modificata precedente denominazione “REGGIO DI CALABRIA “ |


Pertanto nella combo box dei Fori, presente in varie forms  dell’applicativo, ad es. nella nuova popup di ricerca Difensore su ReGIndE


Figura 1 – Popup Ricerca Difensore su ReGIndE

selezionando il campo foro, nella combo box saranno presenti i su riportati fori









Per effetto dell’associazione del foro al Comune sede del Foro, nelle varie form in cui è presente l’UNEP come soggetto addetto alla notifica al Difensore, il sistema valorizzerà in automatico il campo sede con il comune associato, per cui si passerà dalla precedente valorizzazione


Figura 2 – Valorizzazione Sede UNEP precedente

alla nuova, in cui il sistema recupererà dalla base dati il comune sede del Foro


Figura 3 – Valorizzazione Sede UNEP nuova

Poiché il comune di Napoli Nord non è di fatti esistente, il sistema controllerà in fase di inserimento che il contenuto del campo sede, corrisponda ad un Comune esistente e valido nella Tabella Comune di SIES, in caso contrario il sistema invierà il seguente messaggio bloccante



Si riporta di seguito una funzionalità per ciascun sottosistema dove è possibile verificare le modifiche apportate sul destinatario della Notifica al Difensore tramite UNEP.

SIEP

Si riporta di seguito l’effetto delle modifiche nell’Ordine di Esecuzione


Figura 4: Ordine di Esecuzione con Sezione destinatario Notifica difensore modificata



SIUS

Si riporta di seguito l’effetto delle modifiche nella funzione di Fissazione Udienza


Figura 5: Fissazione Udienza con Sezione destinatario Notifica difensore modificata


SIGE

Si riporta di seguito l’effetto delle modifiche nella funzione di Deposito Ordinanza


Figura 6: Sezione destinatario Notifica - SIGE

## Gestione Alerts per procedimenti con avvocati non certificati ReGIndE
Con il rilascio di questa nuova gestione del Difensore non è più possibile ricercare e associare ad un procedimento un avvocato già presente nel sistema con non sia certificato ReGIndE.
Precedentemente all’avvio della nuova gestione, sarà eseguita sugli archivi SIES distrettuali un’attività di bonifica degli avvocati, che partendo da una tabella contenente gli Avvocati attivi presenti su ReGIndE, cercherà fra gli avvocati SIES, con procedimenti SIEP/SIUS/SIGE pendenti, quelli aventi Cognome, Nome, Luogo e Data nascita, Codice Fiscale uguali a quelli presenti in ReGIndE e li certificherà ReGIndE.
Per i procedimenti collegati ad Avvocati non certificati, il sistema attiverà dei messaggi di avviso (Alerts), per segnalare all’utente la non certificazione dei Difensori e la necessità di procedere alla certificazione degli stessi.
Di seguito si riportano le tipologia di messaggi per i tre sottosistemi per procedimenti con almeno un difensore non certificato ReGIndE.

## Sottosistema SIEP

Selezionando la funzione Dettaglio del procedimento SIEP si riceverà prima il seguente messaggio


Figura 7 – Messaggio Alert su Dettaglio procedimento SIEP con presenza Avvocato non certificato

e successivamente alla conferma nella form di Dettaglio saranno evidenziati in giallo (blinkante) il Cognome, Nome ed il Foro di appartenenza.


Figura 8 – Segnalazione su Dettaglio procedimento SIEP per Avvocato non certificato

Se non si procede alla certificazione dell’avvocato, un messaggio di warning sarà riportato su tutte le form di emissione provvedimento, es.

Figura 9 – Alert su Form Rideterminazione pena per procedimento SIEP con Avvocato non certificato

## Sottosistema SIUS

Selezionando la funzione Dettaglio Procedimento SIUS si riceverà prima il seguente messaggio


Figura 10 – Messaggio Alert su Dettaglio procedimento SIUS con presenza Avvocato non certificato

e successivamente alla conferma nella form di Dettaglio saranno evidenziati in giallo (blinkante) il Cognome, Nome ed il Tipo.


Figura 11 – Segnalazione su Dettaglio procedimento SIUS per Avvocato non certificato

Se non si procede alla certificazione dell’avvocato, un messaggio di warning sarà riportato su tutte le form di emissione provvedimento, es.

Figura 12 – Alert su Form Emissione Ordinanza per procedimento SIUS con Avvocato non certificato

## Sottosistema SIGE

Selezionando la funzione la funzione  Dettaglio Procedimento SIGE si riceverà prima il seguente messaggio


Figura 13 – Messaggio Alert su Dettaglio procedimento SIGE con presenza Avvocato non certificato

e successivamente alla conferma nella form di Dettaglio saranno evidenziati in giallo (blinkante) il Cognome, Nome ed il Foro di appartenenza.


Figura 14 – Segnalazione su Dettaglio procedimento SIGE per Avvocato non certificato

Se non si procede alla certificazione dell’avvocato, un messaggio di warning sarà riportato su tutte le form di emissione provvedimento, es.

Figura 15 – Alert su Form Emissione Ordinanza per procedimento SIGE con Avvocato non certificato



# Gestione Difensori con certificazione su ReGIndE
Per tutti e tre i sottosistemi di SIES sono state riviste le modalità di Gestione dei Difensori, che devono essere certificati con una ricerca preventiva su ReGIndE.
## Sottosistema SIEP
## Assegnazione Difensore

La funzione di Assegnazione/Inserimento Difensore SIEP, raggiungibile dal Dettaglio Procedimento SIGE>>Assegnazione Difensore, è stata modificata e permette solo la ricerca dell’avvocato su ReGIndE


Figura 16 – Form Assegnazione / Inserimento Difensore SIEP

infatti nella form nessun campo è digitabile, ad esclusione della combo ‘Tipo Difensore’, è possibile solo selezionare il link , che apre la popup di ricerca


Figura 17 – Popup Ricerca Difensore su ReGIndE
in cui è possibile compilare:

il campo Cognome (obbligatoriamente)
il campo Nome (non obbligatorio)
il campo Foro, selezionandolo dalla combo box, contenente tutti i fori attivi presenti su SIES e conformi a quelli presenti in ReGIndE
selezionare la check box ‘Tutti i Fori’ per estendere la ricerca dell’avvocato in tutti i Fori.

Dopo aver compilato i dati obbligatori della form, cliccando sul tasto , il sistema, utilizzando un apposito web service di interazione con ReGIndE, innescherà su quel sistema una ricerca puntuale degli Avvocati aventi Cognome, eventualmente il Nome uguali a quelli digitati e appartenenti al foro selezionato o a tutti i fori.

In caso di ricerca con esito positivo nella popup sarà riportato l’elenco degli avvocati presenti in ReGIndE, soddisfacenti le condizioni di ricerca impostati.

Figura 18 – Popup Ricerca Difensore su ReGIndE con esito positivo
Per ciascun avvocato della lista saranno riportati: Cognome, Nome, Codice Fiscale, Foro, Luogo e Data nascita, Indirizzo dello Studio, Stato. Inoltre cliccando sull’icona , presente accanto a Cognome e Nome, il sistema mostra i seguenti dati aggiuntivi (pec, telefono, fax e-mail)



Dall’elenco è possibile selezionare l’avvocato di interesse o modificare i dati di ricerca e innescare una nuova ricerca.

In caso di selezione dell’avvocato dall’elenco, il sistema chiude la popup di ricerca e trasferisce i dati pervenuti da ReGIndE nella form di Inserimento Avvocato.


Figura 19 –Assegnazione / Inserimento SIEP Difensore certificato ReGIndE

L’utente dopo aver selezionato il Tipo Difensore dalla relativa combo box , procede alla Conferma, il sistema effettua le seguenti operazioni:


Poiché in ReGIndE il LUOGO_NASCITA e il COMUNE di RESIDENZA dello studio sono importati, in forma descrittiva, così come inseriti dagli Ordini Forensi, senza alcun controllo sulla corrispondenza della Descrizione rispetto alle Denominazioni ufficialmente riconosciute dei Comuni/Nazioni, per risalire al luogo di nascita corretto il sistema estrae il codice catastale dal codice fiscale e accedendo con il codice catastale alla tabella COMUNE o, per i nati all’estero, al Dominio ‘NAZIONE’ della CG_REF_CODES recupera la descrizione ed il codice del Comune/Nazione. Per tale ragione la descrizione riportata nella form di dettaglio può differire da quella riportata nella precedente popup.
Se non dovesse ritrovare alcun Comune con quel codice fiscale, il sistema invierà all’utente il seguente messaggio di errore



e non procederà all’inserimento. Se invece esiste in SIES un comune con il codice catastale estratto, prosegue con lo step successivo

verifica se nella tabella AVVOCATO di Sies esista già un avvocato, con FLAG_REGINDE = ‘SI’,  con Cognome, Nome e Codice Fiscale uguali a quelli della form;
se lo step 2) ha un risultato positivo, verifica se il foro dell’avvocato già presente in tabella sia uguale a quello presente nella form di assegnazione, in caso di uguaglianza il sistema associa l’avvocato già presente al procedimento e procede all’eventuale aggiornamento dell’indirizzo dello studio, del telefono, del fax, dell’e-mail, della pec, dello stato. In caso di fori differenti, cioè lo stesso avvocato ha cambiato foro, il sistema sull’avvocato già presente in base dati imposta il FLAG_REGINDE = ‘NO’ e esegue lo step successivo;
se lo step 2) ha un risultato negativo oppure è verificata l’ultima condizione del precedente step, il sistema inserisce un nuovo avvocato con i dati provenienti da ReGIndE, impostando FLAG_REGINDE = ‘SI’, e lo associa al procedimento corrente.

Al termine delle operazioni di aggiornamento della base dati, il sistema invia la form di Dettaglio Avvocato


Figura 20 – Form Dettaglio Avvocato SIEP

Nel caso che la ricerca su ReGIndE non estragga alcun difensore, il sistema invierà il seguente messaggio



selezionando OK, nella popup di ricerca sarà visualizzato un nuovo tasto di ricerca del difensore, con i dati già impostati, fra quelli presenti nella tabella AVVOCATO di SIES, ma comunque già certificati (FLAG_REGINDE = ‘SI’)


Figura 21 – Popup Ricerca Difensore su ReGIndE con tasto per ricerca su SIES

Se si modifica uno dei parametri già impostati nella form, il sistema eliminerà dalla form  il tasto .
Se l’utente seleziona la ricerca su SIES, il sistema ricercherà nella tabella AVVOCATO di  SIES tutti i difensori, certificati ReGIndE (FLAG_REGINDE = ‘SI’) del foro indicato o tutti i fori, il cui cognome ed eventualmente Nome, inizino con la stessa sequenza di caratteri digitati, riportando l’elenco degli avvocati


Figura 22 – Popup Ricerca Difensore su ReGIndE a seguito ricerca su SIES

In caso di selezione dell’avvocato dall’elenco, il sistema chiude la popup di ricerca e trasferisce i dati estratti dalla tabella AVVOCATO SIES nella form di Inserimento Avvocato. La form di Inserimento Difensore risulterà compilata in tutte le sue parti e nessun campo sarà editabile, ad eccezione del Tipo Difensore


Figura 23 – Popup Ricerca Difensore certificato a seguito ricerca su SIES

L’utente dopo aver selezionato il Tipo Difensore dalla relativa combo box , procede alla Conferma, il sistema si limita ad associare il difensore già esistente e certificato nella tabella AVVOCATO SIES al procedimento corrente ed invia la form di Dettaglio Avvocato

Nel caso che la ricerca risulti nulla sia su ReGIndE o che ReGIndE  non sia raggiungibile e risulti nulla anche su SIES, il sistema invierà il seguente messaggio



dando la possibilità, per poter procedere con la lavorazione del procedimento, di inserire un avvocato manualmente. Questo tipo di avvocato sarà inserito come non certificato e sarà utilizzato solo dal procedimento corrente, non potrà essere associato ad alcun altro procedimento.

Selezionando OK, il sistema ritorna sulla maschera di Inserimento Avvocato, rendendo digitabili tutti i campi della form, oscurando il tasto Conferma e mostra il tasto


Figura 24 –Form iniziale per Inserimento manuale Difensore non certificato ReGIndE

L’utente compila i campi della form

Figura 25 –Form Inserimento manuale Difensore non certificato ReGIndE compilata manualmente

e clicca il tasto Inserimento .

Il sistema dopo aver effettuato i controlli formali su Comune Nascita e Sede dello studio, inserisce nella base dati un nuovo AVVOCATO, non certificato ReGIndE (FLAG_REGINDE = ‘NO’), associandolo al procedimento corrente e invia la form di Dettaglio. Questo Avvocato non sarà ricercabile per associarlo ad altro procedimento.


Figura 26 –Dettaglio Difensore SIEP non certificato ReGIndE

che riporterà l’Alert per la presenza sul procedimento di Avvocato non certificato.

Eccezioni che possono verificarsi nella ricerca su ReGIndE:

se la ricerca per Cognome e Foro/Fori causa l’estrazione di un numero di records superiore al limite consentito si verifica un errore ( SearchLimitException) che sarà gestito con l’invio del seguente messaggio



cliccando su OK, nella popup di ricerca sarà aggiunto come ulteriore parametro di ricerca il Codice Fiscale



Figura 27 –Popup di Ricerca Avvocato su ReGIndE con codice fiscale

se si valorizza il campo Codice Fiscale la ricerca avviene per questo solo parametro, anche se sono stati valorizzati cognome e nome, ed estesa a tutti i Fori.

se il collegamento con ReGIndE è assente, a causa problemi di rete o per non disponibilità del servizio, al momento in cui si avvia la ricerca, il sistema invierà il seguente messaggio


Figura 28 –Popup di Ricerca Avvocato su ReGIndE in caso di non disponibilità di ReGIndE

selezionando OK, nella popup sarà mostrato il tasto per la Ricerca su SIES



## Sostituzione Difensore

Anche La funzione di Sostituzione Difensore SIEP, raggiungibile dal Dettaglio Procedimento SIGE>>Assegnazione Difensore, è stata modificata e permette solo la ricerca dell’avvocato su ReGIndE



selezionando il tasto , il sistema invierà la form


Figura 29 – Form iniziale di Sostituzione Difensore


nella form nessun campo è digitabile, ad esclusione della combo ‘Tipo Difensore’, è possibile solo selezionare il link , che apre la popup di ricerca


Figura 30 – Popup Ricerca Difensore su ReGIndE
per le tipologie di ricerche e relativo funzionamento, vale quanto riportato al par. 3.1.1.

Successivamente alla selezione del difensore a seguito ricerca su ReGIndE o su SIES, comunque certificato, il sistema travasa i dati nella form di sostituzione, che si compila con i dati del difensore e chiude la popup di ricerca


Figura 31 – Form Sostituzione Difensore SIEP compilata a seguito selezione da ricerca
L’utente dopo aver selezionato il Tipo Difensore dalla relativa combo box , procede alla Conferma, il sistema effettua l’aggiornamento della base dati osservando le stesse regole descritte al par. 3.1.1 relativamente alla gestione dell’Avvocato, l’unica differenza è relativa all’associazione al procedimento corrente che sarà eseguita dopo che il sistema imposta la data fine validità sul record di associazione precedente.
Al termine dell’aggiornamento della base dati il sistema invierà la form di Dettaglio


Figura 32 – Form Dettaglio Difensore SIEP a seguito sostituzione
Nel caso di ricerca nulla su ReGIndE e su SIES, anche per la sostituzione è prevista la possibilità di procedere all’inserimento manuale del Difensore, utilizzando la form


Figura 33 – Form Sostituzione per Inserimento manuale difensore non certificato
Dopo la compilazione dei campi della form, l’utente  clicca il tasto Inserimento .

Il sistema dopo aver effettuato i controlli formali su Comune Nascita e Sede dello studio, inserisce nella base dati un nuovo AVVOCATO, non certificato ReGIndE (FLAG_REGINDE = ‘NO’), associandolo al procedimento corrente, rende non più valida l’associazione al precedente avvocato, e invia la form di Dettaglio. Questo Avvocato non sarà ricercabile per associarlo ad altro procedimento.


## Inserimento Istanza
Le funzioni Iscrizione Istanza, selezionabili da Istanze >> Iscrizione Istanza sono state modificate per modificare l’attuale selezione dell’avvocato dalla tabella AVVOCATO SIES alla ricerca dell’Avvocato da ReGIndE



Figura 34: Form Iscrizione Istanza da Procedimento SIEP
in cui per la valorizzazione dell’Avvocato bisogna selezionare il link , che apre la popup di ricerca

Figura 35 – Popup Ricerca Difensore su ReGIndE
in cui, come già descritto al par. 3.1.1, è possibile effettuare la Ricerca su ReGIndE oppure, in caso di risultato nullo, effettuare la Ricerca sugli Avvocati certificati già presenti

Figura 36 – Popup Ricerca Difensore su ReGIndE con tasto per ricerca su SIES
in entrambi i casi, selezionando l’avvocato dall’Elenco, il sistema travasa i dati nei campi del Difensore nella form principale.


Figura 37: Form Iscrizione Istanza da Procedimento SIEP con dati Difensore provenienti da ReGIndE

I dati non sono modificabili. Sulla conferma della form, dopo che sia stata compilata in tutte le sue parti obbligatorie, il sistema procederà ad aggiornare la base dati, osservando per l’avvocato i principi già riportati per l’Assegnazione Difensore.

In caso di Difensore proveniente da ReGIndE

verifica se nella tabella AVVOCATO di Sies esista già un avvocato, con FLAG_REGINDE = ‘SI’,  con Cognome, Nome e Codice Fiscale uguali a quelli della form;
se lo step 1) ha un risultato positivo, verifica se il foro dell’avvocato già presente in tabella sia uguale a quello presente nella form di assegnazione, in caso di uguaglianza il sistema associa l’avvocato già presente all’istanza e procede all’eventuale aggiornamento dell’indirizzo dello studio, del telefono, del fax, dell’e-mail, della pec, dello stato. In caso di fori differenti, cioè lo stesso avvocato ha cambiato foro, il sistema sull’avvocato già presente in base dati imposta il FLAG_REGINDE = ‘NO’ e esegue lo step successivo;
se lo step 1) ha un risultato negativo oppure è verificata l’ultima condizione del precedente step, il sistema inserisce un nuovo avvocato con i dati provenienti da ReGIndE, impostando FLAG_REGINDE = ‘SI’, e lo associa all’istanza.

In caso di Difensore certificato selezionato a seguito ricerca su SIES

il sistema si limita ad associare l’id_avvocato all’istanza



Nel caso che le ricerche su ReGIndE e su SIES non producano risultati il sistema invierà il seguente messaggio



consentendo all’utente di procedere all’inserimento nella base dati di un avvocato non certificato, che non potrà essere ricercato per associarlo ad altri procedimenti/istanze. Cliccando su OK, il sistema rende digitabili i campi della form dedicati al Difensore. L’utente compila manualmente i dati, insieme agli altri campi obbligatori delle form è Conferma.
Il sistema procederà ad aggiornare la base dati, inserendo fra l’altro un nuovo record AVVOCATO che sarà associato all’istanza. Al termine della fase di Aggiornamento il sistema invierà la form di Dettaglio Procedimento con gli estremi dell’istanza


Figura 38 – Form Dettaglio Procedimento SIEP con istanza

da cui cliccando sul link del tipo istanza si ottiene il Dettaglio della stessa


Figura 39 – Form Dettaglio Istanza
Le stesse modifiche, riportate in precedenza, sono state apportate anche all’Iscrizione Istanza per Soggetto e all’Iscrizione Istanza per Titolo Esecutivo.
## Sottosistema SIUS
## Assegnazione Difensore
La funzione di Assegnazione/Inserimento Difensore SIUS, raggiungibile dal Dettaglio Procedimento SIUS>>Assegnazione Difensore, è stata modificata e permette solo la ricerca dell’avvocato su ReGIndE o, se il procedimento SIUS è collegato a un procedimento SIEP, di selezionarlo fra gli avvocati associati al procedimento SIEP, purchè risultino certificati su ReGIndE (FLAG_REGINDE = ‘SI’).


Figura 40 – Form Assegnazione / Inserimento Difensore SIUS

infatti nella form nessun campo è digitabile, ad esclusione della combo ‘Tipo Difensore’, è possibile solo selezionare il link , che apre la popup di ricerca, o il link  . Nel primo caso si apre la popup di ricerca


Figura 41 – Popup Ricerca Difensore su ReGIndE
in cui è possibile compilare:

il campo Cognome (obbligatoriamente)
il campo Nome (non obbligatorio)
il campo Foro, selezionandolo dalla combo box, contenente tutti i fori attivi presenti su SIES e conformi a quelli presenti in ReGIndE
selezionare la check box ‘Tutti i Fori’ per estendere la ricerca dell’avvocato in tutti i Fori.

Dopo aver compilato i dati obbligatori della form, cliccando sul tasto , il sistema, utilizzando un apposito web service di interazione con ReGIndE, innescherà su quel sistema una ricerca puntuale degli Avvocati aventi Cognome, eventualmente il Nome uguali a quelli digitati e appartenenti al foro selezionato o a tutti i fori.

In caso di ricerca con esito positivo nella popup sarà riportato l’elenco degli avvocati presenti in ReGIndE, soddisfacenti le condizioni di ricerca impostati.

Figura 42 – Popup Ricerca Difensore su ReGIndE
Per ciascun avvocato della lista saranno riportati: Cognome, Nome, Codice Fiscale, Foro, Luogo e Data nascita, Indirizzo dello Studio, Stato. Inoltre cliccando sull’icona , presente accanto a Cognome e Nome, il sistema mostra i seguenti dati aggiuntivi (pec, telefono, fax e-mail)



Dall’elenco è possibile selezionare l’avvocato di interesse o modificare i dati di ricerca e innescare una nuova ricerca.

Se invece tutti i controlli saranno superati, la form di Inserimento Difensore risulterà compilata in tutte le sue parti e nessun campo sarà editabile, ad eccezione del Tipo Difensore


Figura 43 – Form Assegnazione/Inserimento Avvocato SIUS



L’utente dopo aver selezionato il Tipo Difensore dalla relativa combo box , procede alla Conferma, il sistema effettua le seguenti operazioni:
Poiché in ReGIndE il LUOGO_NASCITA e il COMUNE di RESIDENZA dello studio sono importati, in forma descrittiva, così come inseriti dagli Ordini Forensi, senza alcun controllo sulla corrispondenza della Descrizione rispetto alle Denominazioni ufficialmente riconosciute dei Comuni/Nazioni, per risalire al luogo di nascita corretto il sistema estrae il codice catastale dal codice fiscale e accedendo con il codice catastale alla tabella COMUNE o, per i nati all’estero, al Dominio ‘NAZIONE’ della CG_REF_CODES recupera la descrizione ed il codice del Comune/Nazione. Per tale ragione la descrizione riportata nella form di dettaglio può differire da quella riportata nella precedente popup.
Se non dovesse ritrovare alcun Comune con quel codice fiscale, il sistema invierà all’utente il seguente messaggio di errore



e non procederà all’inserimento. Se invece esiste in SIES un comune con il codice catastale estratto, prosegue con lo step successivo

verifica se nella tabella AVVOCATO di Sies esista già un avvocato, con FLAG_REGINDE = ‘SI’,  con Cognome, Nome e Codice Fiscale uguali a quelli della form;
se lo step 2) ha un risultato positivo, verifica se il foro dell’avvocato già presente in tabella sia uguale a quello presente nella form di assegnazione, in caso di uguaglianza il sistema associa l’avvocato già presente al procedimento e procede all’eventuale aggiornamento dell’indirizzo dello studio, del telefono, del fax, dell’e-mail, della pec, dello stato. In caso di fori differenti, cioè lo stesso avvocato ha cambiato foro, il sistema sull’avvocato già presente in base dati imposta il FLAG_REGINDE = ‘NO’ e esegue lo step successivo;
se lo step 2) ha un risultato negativo oppure è verificata l’ultima condizione del precedente step, il sistema inserisce un nuovo avvocato con i dati provenienti da ReGIndE, impostando FLAG_REGINDE = ‘SI’, e lo associa al procedimento corrente.

Al termine delle operazioni di aggiornamento della base dati, il sistema invia la form di Dettaglio Avvocato


Figura 44 – Form Dettaglio Avvocato SIUS


Nel caso che la ricerca su ReGIndE non estragga alcun difensore, il sistema invierà il seguente messaggio



selezionando OK, nella popup di ricerca sarà visualizzato un nuovo tasto di ricerca del difensore, con i dati già impostati, fra quelli presenti nella tabella AVVOCATO di SIES, ma comunque già certificati (FLAG_REGINDE = ‘SI’)


Figura 45 – Popup Ricerca Difensore su ReGIndE con tasto per ricerca su SIES

Se si modifica uno dei parametri già impostati nella form, il sistema eliminerà dalla form  il tasto .
Se l’utente seleziona la ricerca su SIES, il sistema ricercherà nella tabella AVVOCATO di  SIES tutti i difensori, certificati ReGIndE (FLAG_REGINDE = ‘SI’) del foro indicato o tutti i fori, il cui cognome ed eventualmente Nome, inizino con la stessa sequenza di caratteri digitati, riportando l’elenco degli avvocati



In caso di selezione dell’avvocato dall’elenco, il sistema chiude la popup di ricerca e trasferisce i dati estratti dalla tabella AVVOCATO SIES nella form di Inserimento Avvocato. La form di Inserimento Difensore risulterà compilata in tutte le sue parti e nessun campo sarà editabile, ad eccezione del Tipo Difensore


Figura 46 – Form Assegnazione/Inserimento Avvocato SIUS

L’utente dopo aver selezionato il Tipo Difensore dalla relativa combo box , procede alla Conferma, il sistema si limita ad associare il difensore già esistente e certificato nella tabella AVVOCATO SIES al procedimento corrente ed invia la form di Dettaglio Avvocato.

Nel caso che la ricerca risulti nulla sia su ReGIndE o che ReGIndE  non sia raggiungibile e risulti nulla anche su SIES, il sistema invierà il seguente messaggio






dando la possibilità, per poter procedere con la lavorazione del procedimento, di inserire un avvocato manualmente. Questo tipo di avvocato sarà inserito come non certificato e sarà utilizzato solo dal procedimento corrente, non potrà essere associato ad alcun altro procedimento.

Selezionando OK, il sistema ritorna sulla maschera di Inserimento Avvocato, rendendo digitabili tutti i campi della form, oscurando il tasto Conferma e mostra il tasto



Figura 47 – Form Inserimento Avvocato SIUS non certificato ReGIndE
L’utente compila i campi della form


Figura 48 – Form Inserimento Avvocato SIUS non certificato ReGIndE compilata manualmente

e clicca il tasto Inserimento .

Il sistema dopo aver effettuato i controlli formali su Comune Nascita e Sede dello studio, inserisce nella base dati un nuovo AVVOCATO, non certificato ReGIndE (FLAG_REGINDE = ‘NO’), associandolo al procedimento corrente e invia la form di Dettaglio. Questo Avvocato non sarà ricercabile per associarlo ad altro procedimento.


Figura 49 – Form Dettaglio  Avvocato SIUS non certificato ReGIndE compilata manualmente

che riporterà l’Alert per la presenza sul procedimento di Avvocato non certificato.

Nel caso che il procedimento SIUS sia collegato a un procedimento SIEP, selezionando nella form iniziale di Assegnazione/Inserimento Difensore il link , il sistema ricercherà gli avvocati collegati al procedimento SIEP e se certificati li mostrerà nella popup


Figura 50 – Popup Elenco  Avvocati certificati collegati al procedimento SIEP

selezionando uno dei nominativi dall’elenco, il sistema li travasa nella form di Assegnazione/Inserimento Difensore, già vista in precedenza.
L’utente seleziona il tipo difensore e Conferma, il sistema si limita ad associare il difensore già esistente e certificato nella tabella AVVOCATO SIES al procedimento corrente ed invia la form di Dettaglio Avvocato.


Eccezioni che possono verificarsi nella ricerca su ReGIndE:

se la ricerca per Cognome e Foro/Fori causa l’estrazione di un numero di records superiore al limite consentito si verifica un errore ( SearchLimitException) che sarà gestito con l’invio del seguente messaggio



cliccando su OK, nella popup di ricerca sarà aggiunto come ulteriore parametro di ricerca il Codice Fiscale


Figura 51 – Popup ricerca Avvocato su  ReGIndE in caso di SearchLimitException

se si valorizza il campo Codice Fiscale la ricerca avviene per questo solo parametro, anche se sono stati valorizzati cognome e nome, ed estesa a tutti i Fori.

se il collegamento con ReGIndE è assente, a causa problemi di rete o per non disponibilità del servizio, al momento in cui si avvia la ricerca, il sistema invierà il seguente messaggio


selezionando OK, nella popup sarà mostrato il tasto per la Ricerca su SIES




## Sostituzione Difensore

Anche La funzione di Sostituzione Difensore SIUS, raggiungibile dal Dettaglio Procedimento SIUS>>Assegnazione Difensore, è stata modificata e permette solo la ricerca dell’avvocato su ReGIndE



selezionando il tasto , il sistema invierà la form


Figura 52 – Form iniziale di Sostituzione Difensore

nella form nessun campo è digitabile, ad esclusione della combo ‘Tipo Difensore’, è possibile solo
selezionare il link , che apre la popup di ricerca


Figura 53 – Popup Ricerca Difensore su ReGIndE
per le tipologie di ricerche e relativo funzionamento, vale quanto riportato al par. 3.2.1.

Successivamente alla selezione del difensore a seguito ricerca su ReGIndE o su SIES, comunque certificato,
il sistema travasa i dati nella form di sostituzione, che si compila con i dati del difensore e chiude la popup
di ricerca


Figura 54 – Form Sostituzione Difensore SIUS compilata a seguito selezione da ricerca
L’utente dopo aver selezionato il Tipo Difensore dalla relativa combo box , procede alla Conferma, il sistema effettua l’aggiornamento della base dati osservando le stesse regole descritte al par. 3.3.1 relativamente alla gestione dell’Avvocato, l’unica differenza è relativa all’associazione al procedimento corrente che sarà eseguita dopo che il sistema imposta la data fine validità sul record di associazione precedente.
Al termine dell’aggiornamento della base dati il sistema invierà la form di Dettaglio


Figura 55 – Form Dettaglio Difensore SIUS a seguito sostituzione

Nel caso di ricerca nulla su ReGIndE e su SIES, anche per la sostituzione è prevista la possibilità di
procedere all’inserimento manuale del Difensore, utilizzando la form


Figura 56 – Form Sostituzione per Inserimento manuale difensore non certificato
Dopo la compilazione dei campi della form, l’utente  clicca il tasto Inserimento .

Il sistema dopo aver effettuato i controlli formali su Comune Nascita e Sede dello studio, inserisce nella base dati un nuovo AVVOCATO, non certificato ReGIndE (FLAG_REGINDE = ‘NO’), associandolo al procedimento corrente, rende non più valida l’associazione al precedente avvocato, e invia la form di Dettaglio. Questo Avvocato non sarà ricercabile per associarlo ad altro procedimento.


## Sottosistema SIGE
## Assegnazione Difensore


La funzione di Assegnazione/Inserimento Difensore SIGE, raggiungibile dal Dettaglio Procedimento SIGE>>Assegnazione Difensore, è stata modificata e permette solo la ricerca dell’avvocato su ReGIndE o, se il procedimento SIGE è collegato a un procedimento SIEP, di selezionarlo fra gli avvocati associati al procedimento SIEP, purchè risultino certificati su ReGIndE (FLAG_REGINDE = ‘SI’).


Figura 57 – Form Assegnazione / Inserimento Difensore SIGE

infatti nella form nessun campo è digitabile, ad esclusione della combo ‘Tipo Difensore’, è possibile solo selezionare il link , che apre la popup di ricerca, o il link  . Nel primo caso si apre la popup di ricerca


Figura 58 – Popup Ricerca Difensore su ReGIndE
in cui è possibile compilare:

il campo Cognome (obbligatoriamente)
il campo Nome (non obbligatorio)
il campo Foro, selezionandolo dalla combo box, contenente tutti i fori attivi presenti su SIES e conformi a quelli presenti in ReGIndE
selezionare la check box ‘Tutti i Fori’ per estendere la ricerca dell’avvocato in tutti i Fori.

Dopo aver compilato i dati obbligatori della form, cliccando sul tasto , il sistema, utilizzando un apposito web service di interazione con ReGIndE, innescherà su quel sistema una ricerca puntuale degli Avvocati aventi Cognome, eventualmente il Nome uguali a quelli digitati e appartenenti al foro selezionato o a tutti i fori.

In caso di ricerca con esito positivo nella popup sarà riportato l’elenco degli avvocati presenti in ReGIndE, soddisfacenti le condizioni di ricerca impostati.

Figura 59 – Popup Ricerca Difensore su ReGIndE
Per ciascun avvocato della lista saranno riportati: Cognome, Nome, Codice Fiscale, Foro, Luogo e Data nascita, Indirizzo dello Studio, Stato. Inoltre cliccando sull’icona , presente accanto a Cognome e Nome, il sistema mostra i seguenti dati aggiuntivi (pec, telefono, fax e-mail)



Dall’elenco è possibile selezionare l’avvocato di interesse o modificare i dati di ricerca e innescare una nuova ricerca.

Se invece tutti i controlli saranno superati, la form di Inserimento Difensore risulterà compilata in tutte le sue parti e nessun campo sarà editabile, ad eccezione del Tipo Difensore


Figura 60 – Form Assegnazione/Inserimento Avvocato SIGE



L’utente dopo aver selezionato il Tipo Difensore dalla relativa combo box , procede alla Conferma, il sistema effettua le seguenti operazioni:
Poiché in ReGIndE il LUOGO_NASCITA e il COMUNE di RESIDENZA dello studio sono importati, in forma descrittiva, così come inseriti dagli Ordini Forensi, senza alcun controllo sulla corrispondenza della Descrizione rispetto alle Denominazioni ufficialmente riconosciute dei Comuni/Nazioni, per risalire al luogo di nascita corretto il sistema estrae il codice catastale dal codice fiscale e accedendo con il codice catastale alla tabella COMUNE o, per i nati all’estero, al Dominio ‘NAZIONE’ della CG_REF_CODES recupera la descrizione ed il codice del Comune/Nazione. Per tale ragione la descrizione riportata nella form di dettaglio può differire da quella riportata nella precedente popup.
Se non dovesse ritrovare alcun Comune con quel codice fiscale, il sistema invierà all’utente il seguente messaggio di errore



e non procederà all’inserimento. Se invece esiste in SIES un comune con il codice catastale estratto, prosegue con lo step successivo

verifica se nella tabella AVVOCATO di Sies esista già un avvocato, con FLAG_REGINDE = ‘SI’,  con Cognome, Nome e Codice Fiscale uguali a quelli della form;
se lo step 2) ha un risultato positivo, verifica se il foro dell’avvocato già presente in tabella sia uguale a quello presente nella form di assegnazione, in caso di uguaglianza il sistema associa l’avvocato già presente al procedimento e procede all’eventuale aggiornamento dell’indirizzo dello studio, del telefono, del fax, dell’e-mail, della pec, dello stato. In caso di fori differenti, cioè lo stesso avvocato ha cambiato foro, il sistema sull’avvocato già presente in base dati imposta il FLAG_REGINDE = ‘NO’ e esegue lo step successivo;
se lo step 2) ha un risultato negativo oppure è verificata l’ultima condizione del precedente step, il sistema inserisce un nuovo avvocato con i dati provenienti da ReGIndE, impostando FLAG_REGINDE = ‘SI’, e lo associa al procedimento corrente.

Al termine delle operazioni di aggiornamento della base dati, il sistema invia la form di Dettaglio Avvocato


Figura 61 – Form Dettaglio Avvocato SIGE


Nel caso che la ricerca su ReGIndE non estragga alcun difensore, il sistema invierà il seguente messaggio



selezionando OK, nella popup di ricerca sarà visualizzato un nuovo tasto di ricerca del difensore, con i dati già impostati, fra quelli presenti nella tabella AVVOCATO di SIES, ma comunque già certificati (FLAG_REGINDE = ‘SI’)


Figura 62 – Popup Ricerca Difensore su ReGIndE con tasto per ricerca su SIES

Se si modifica uno dei parametri già impostati nella form, il sistema eliminerà dalla form  il tasto .
Se l’utente seleziona la ricerca su SIES, il sistema ricercherà nella tabella AVVOCATO di  SIES tutti i difensori, certificati ReGIndE (FLAG_REGINDE = ‘SI’) del foro indicato o tutti i fori, il cui cognome ed eventualmente Nome, inizino con la stessa sequenza di caratteri digitati, riportando l’elenco degli avvocati



In caso di selezione dell’avvocato dall’elenco, il sistema chiude la popup di ricerca e trasferisce i dati estratti dalla tabella AVVOCATO SIES nella form di Inserimento Avvocato. La form di Inserimento Difensore risulterà compilata in tutte le sue parti e nessun campo sarà editabile, ad eccezione del Tipo Difensore


Figura 63 – Form Assegnazione/Inserimento Avvocato SIGE

L’utente dopo aver selezionato il Tipo Difensore dalla relativa combo box , procede alla Conferma, il sistema si limita ad associare il difensore già esistente e certificato nella tabella AVVOCATO SIES al procedimento corrente ed invia la form di Dettaglio Avvocato.

Nel caso che la ricerca risulti nulla sia su ReGIndE o che ReGIndE  non sia raggiungibile e risulti nulla anche su SIES, il sistema invierà il seguente messaggio






dando la possibilità, per poter procedere con la lavorazione del procedimento, di inserire un avvocato manualmente. Questo tipo di avvocato sarà inserito come non certificato e sarà utilizzato solo dal procedimento corrente, non potrà essere associato ad alcun altro procedimento.

Selezionando OK, il sistema ritorna sulla maschera di Inserimento Avvocato, rendendo digitabili tutti i campi della form, oscurando il tasto Conferma e mostra il tasto



Figura 64 – Form Inserimento Avvocato SIGE non certificato ReGIndE
L’utente compila i campi della form


Figura 65 – Form Inserimento Avvocato SIGE non certificato ReGIndE compilata manualmente

e clicca il tasto Inserimento .

Il sistema dopo aver effettuato i controlli formali su Comune Nascita e Sede dello studio, inserisce nella base dati un nuovo AVVOCATO, non certificato ReGIndE (FLAG_REGINDE = ‘NO’), associandolo al procedimento corrente e invia la form di Dettaglio. Questo Avvocato non sarà ricercabile per associarlo ad altro procedimento.


Figura 66 – Form Dettaglio  Avvocato SIGE non certificato ReGIndE compilata manualmente

che riporterà l’Alert per la presenza sul procedimento di Avvocato non certificato.

Nel caso che il procedimento SIGE sia collegato a un procedimento SIEP, selezionando nella form iniziale di Assegnazione/Inserimento Difensore il link , il sistema ricercherà gli avvocati collegati al procedimento SIEP e se certificati li mostrerà nella popup


Figura 67 – Popup Elenco  Avvocati certificati collegati al procedimento SIEP

selezionando uno dei nominativi dall’elenco, il sistema li travasa nella form di Assegnazione/Inserimento Difensore, già vista in precedenza.
L’utente seleziona il tipo difensore e Conferma, il sistema si limita ad associare il difensore già esistente e certificato nella tabella AVVOCATO SIES al procedimento corrente ed invia la form di Dettaglio Avvocato.


Eccezioni che possono verificarsi nella ricerca su ReGIndE:

se la ricerca per Cognome e Foro/Fori causa l’estrazione di un numero di records superiore al limite consentito si verifica un errore ( SearchLimitException) che sarà gestito con l’invio del seguente messaggio



cliccando su OK, nella popup di ricerca sarà aggiunto come ulteriore parametro di ricerca il Codice Fiscale



Figura 68 – Popup ricerca Avvocato su  ReGIndE in caso di SearchLimitException

se si valorizza il campo Codice Fiscale la ricerca avviene per questo solo parametro, anche se sono stati valorizzati cognome e nome, ed estesa a tutti i Fori.

se il collegamento con ReGIndE è assente, a causa problemi di rete o per non disponibilità del servizio, al momento in cui si avvia la ricerca, il sistema invierà il seguente messaggio



selezionando OK, nella popup sarà mostrato il tasto per la Ricerca su SIES



## Sostituzione Difensore
Anche La funzione di Sostituzione Difensore SIGE, raggiungibile dal Dettaglio Procedimento SIGE>>Assegnazione Difensore, è stata modificata e permette solo la ricerca dell’avvocato su ReGIndE



selezionando il tasto , il sistema invierà la form

Figura 69 – Form iniziale di Sostituzione Difensore

nella form nessun campo è digitabile, ad esclusione della combo ‘Tipo Difensore’, è possibile solo
selezionare il link , che apre la popup di ricerca


Figura 70 – Popup Ricerca Difensore su ReGIndE
per le tipologie di ricerche e relativo funzionamento, vale quanto riportato al par. 3.3.1.

Successivamente alla selezione del difensore a seguito ricerca su ReGIndE o su SIES, comunque certificato,
il sistema travasa i dati nella form di sostituzione, che si compila con i dati del difensore e chiude la popu
di ricerca


Figura 71 – Form Sostituzione Difensore SIGE compilata a seguito selezione da ricerca
L’utente dopo aver selezionato il Tipo Difensore dalla relativa combo box , procede alla Conferma, il sistema effettua l’aggiornamento della base dati osservando le stesse regole descritte al par. 3.3.1 relativamente alla gestione dell’Avvocato, l’unica differenza è relativa all’associazione al procedimento corrente che sarà eseguita dopo che il sistema imposta la data fine validità sul record di associazione precedente.
Al termine dell’aggiornamento della base dati il sistema invierà la form di Dettaglio


Figura 72 – Form Dettaglio Difensore SIGE a seguito sostituzione

Nel caso di ricerca nulla su ReGIndE e su SIES, anche per la sostituzione è prevista la possibilità di
procedere all’inserimento manuale del Difensore, utilizzando la form


Figura 73 – Form Sostituzione per Inserimento manuale difensore non certificato
Dopo la compilazione dei campi della form, l’utente  clicca il tasto Inserimento .

Il sistema dopo aver effettuato i controlli formali su Comune Nascita e Sede dello studio, inserisce nella base dati un nuovo AVVOCATO, non certificato ReGIndE (FLAG_REGINDE = ‘NO’), associandolo al procedimento corrente, rende non più valida l’associazione al precedente avvocato, e invia la form di Dettaglio. Questo Avvocato non sarà ricercabile per associarlo ad altro procedimento.


## Gestione Difensore su Parti Civili/Offese


Anche l’attuale gestione del Difensore sulle parti civili/offese di un procedimento SIGE è stata rivista per allinearla alla necessità di assegnare Difensori certificati ReGIndE.

Per un Procedimento SIGE su cui risulta già caricata un parte civile/offesa, dalla form di Dettaglio/Modifica Difensore e Convocazione


Figura 74 – Form Modifica Difensore e Convocazione Parte Fisica

L’utente seleziona il link , il sistema, in presenza di avvocati per la parte invia la form





mentre in assenza di avvocato invia direttamente la form per l’Assegnazione/Inserimento del Difensore alla parte civile/offesa


Figura 75 – Form Assegnazione Difensore su Parte Civile/Offesa
La form non presenta campi digitabili, a parte il Tipo Difensore, per cui bisogna procedere selezionando il link , che apre la popup di ricerca



per quanto riguarda il funzionamento e le tipologie di ricerca, che è possibile effettuare vale quanto riportato al par. 3.3.1. Dopo che l’utente avrà selezionato il difensore a seguito di una delle ricerche possibili, il sistema travasa i dati del Difensore dalla popup alla form principale

Figura 76 – Form Assegnazione Difensore su Parte Civile/Offesa a seguito ricerca su ReGIndE/SIES

L’utente valorizza il Tipo Difensore e conferma, il sistema dopo aver effettuato tutti i controlli e i passaggi  descritti al par. 3.3.1, con la differenza che nel caso in esame i collegamenti sono fra Avvocato e Parti Civili/Offese, invia la form di Dettaglio.


Figura 77 – Form Dettaglio  Difensore su Parte Civile/Offesa

In caso di ricerca nulla sia su ReGIndE sia su SIES, si può procedere con l’iscrizione manuale dell’avvocato


Figura 78 – Form Inserimento Manuale  Difensore su Parte Civile/Offesa

A seguito della compilazione e della conferma  dei dati il sistema inserirà nella base dati un nuovo avvocato non certificato.

# Gestione DIFENSORI in Funzioni Amministrative
Poiché lo scopo degli interventi descritti nel presente documento è che i dati delle anagrafiche degli avvocati presenti su SIES dovranno essere “importati” dal sistema ReGIndE, sul sistema SIES saranno inibite le funzioni di Inserimento Difensore e Modifica Difensore.
Nello specifico, nel menù Funzioni Amministrative» Gestione Difensori, il tasto ‘Inserimento’ non sarà più visibile, ed inoltre, nello stesso menù, nella Form di elenco Difensori ottenuta dal tasto di ‘ricerca’ sarà eliminata l’azione ‘modifica’.

## Eliminazione funzione Inserimento Difensore
Si è intervenuti nella Gestione Difensori Eliminando la funzione ‘Inserimento’, per cui il menu Gestione Difensori si presenterà come di seguito


Figura 79 – Menu Gestione Difensori

## Eliminazione funzione Modifica Difensore
Si è intervenuti nella funzione di Ricerca di Gestione Difensori limitando la ricerca solo agli avvocati non certificati. Nella form di Elenco Difensori susseguente alla Ricerca


Figura 80 – Form Elenco Avvocati

è stata eliminata la funzione di modifica, per cui sarà possibile procedere solo alla cancellazione di quegli avvocati non certificati  a cui non è collegato alcun procedimento.

La funzione di modifica è stata eliminata anche dal Dettaglio del Difensore


Figura 81 – Form Dettaglio Avvocato




# Gestione Luogo Nascita Soggetto

A seguito dell’attività di allineamento della tabella COMUNE di SIES alla Tabella COMUNE della DGSIA, che contiene la storicizzazione di diversi Comuni, adesso anche in SIES sono presenti Comuni che hanno subito cambi di provincia, comuni soppressi o che hanno subito modifica della denominazione. Pertanto a fronte di una denominazione possono essere presenti nella tabella COMUNE di SIES più occorrenze.

Facciamo l’esempio del COMUNE di ARBUS, che ha fatto parte della provincia di Cagliari (CA) fino al 31/12/2015, della provincia di Medio Campidano (VS, poi abolita) fino al 31/12/2016 e attualmente confluita nella provincia Sud Sardegna (SU)

| COD_COMUNE | COD_PROVINCIA | DESCRIZIONE | FLAG_VALIDITA | COD_CATASTALE_COMUNE | DATA_FINE_VALIDITA_COMUNE |
| --- | --- | --- | --- | --- | --- |
| 092001 | CA | ARBUS | N | A359 | 01/01/2006 |
| 106001 | VS | ARBUS | N | A359 | 01/01/2017 |
| 111001 | SU | ARBUS | S | A359 |  |


e del Comune di SAN TEODORO, in cui a differenza del precedente esempio vi sono tre comuni omonimi che rappresentano lo stesso comune delle Sardegna che ha subito 3 cambi di provincia (NU, OT, SS) e un comune con la stessa denominazione, appartenente alla provincia di Messina

| COD_COMUNE | COD_PROVINCIA | DESCRIZIONE | FLAG_VALIDITA | COD_CATASTALE_COMUNE | DATA_FINE_VALIDITA_COMUNE |
| --- | --- | --- | --- | --- | --- |
| 091076 | NU | SAN TEODORO | N | I329 | 01/01/2005 |
| 104023 | OT | SAN TEODORO | N | I329 | 01/01/2017 |
| 090092 | SS | SAN TEODORO | S | I329 |  |
| 083090 | ME | SAN TEODORO | S | I328 |  |


poiché per quanto riguarda il Luogo di Nascita di un soggetto è importante indicare con esattezza anche la provincia di appartenenza dello stesso al momento della nascita, sono state modificate le funzionalità in cui è gestito il luogo di nascita di un condannato.
Pertanto è stato modificato il precedente controllo sulla omonimia di un Comune, estendendola anche ai comuni con  FLAG_VALIDITA = ‘N’, per cui il sistema invierà il messaggio di esistenza di omonimia, anche in caso di comune storicizzato.
Le modifiche hanno riguardato tutti e 3 i sottosistemi SIES. Poiché le modalità di intervento sono state simili per tutte le funzionalità interessate, di seguito si descrivono dettagliatamente le modifiche operative apportate per le funzioni di Iscrizione e modifica soggetto lato SIEP, mentre si riporta l’elenco delle altre funzionalità modificate.

## Sottosistema SIEP

Iscrizione e Modifica Soggetto

Figura 82 – Form Iscrizione Soggetto

a seguito della Conferma, il sistema verifica l’esistenza nella tabella COMUNE di più records con denominazione ARBUS e invia il seguente messaggio bloccante



L’utente deve selezionare l’icona , presente accanto al campo Comune Nascita, e nella successiva popup che si apre


Figura 83 – Popup Ricerca Comuni per Provincia

digita ARBUS nel campo  e seleziona Filtra, il sistema effettuerà una nuova ricerca nella tabella COMUNE e aggiornerà la popup


Figura 84 – Popup Ricerca Comune

con l’elenco dei comuni soddisfacenti il parametro impostato, riportando per ciascun Comune la provincia di appartenenza e la data di fine validità. L’utente, in base alla data di nascita, seleziona il Comune di interesse (nel ns. es. ARBUS(CA)). Il sistema travasa il comune selezionato nella form di iscrizione soggetto e chiude la popup.
L’utente Conferma i dati della form, il sistema inserirà in Banca Dati un nuovo soggetto con il Comune di nascita selezionato nella popup, come è possibile verificare nella successiva form di Dettaglio Soggetto


Figura 85 – Form Dettaglio Soggetto

Anche nella funzione di Modifica soggetto, attivabile dal Dettaglio, si è intervenuti con le stesse modalità


Figura 86 – Form Modifica Soggetto

supponendo di voler modificare il Comune Nascita da Arbus in San Teodoro, a seguito della Conferma il sistema verifica che vi sono più records nella tabella COMUNE con questa denominazione e invia il seguente messaggio bloccante



L’utente deve selezionare l’icona , presente accanto al campo Comune Nascita, e nella successiva popup che si apre



filtra i Comuni per SAN TEODORO, il sistema effettuerà una nuova ricerca nella tabella COMUNE e aggiornerà la popup





con l’elenco dei comuni soddisfacenti il parametro impostato, riportando per ciascun Comune la provincia di appartenenza e la data di fine validità. L’utente, in base alla data di nascita, seleziona il Comune di interesse (nel ns. es. SAN TEODORO(OT)). Il sistema travasa il comune selezionato nella form di modifica soggetto e chiude la popup.
L’utente Conferma i dati della form, il sistema inserirà in Banca Dati un nuovo soggetto con il Comune di nascita selezionato nella popup, come è possibile verificare nella successiva form di Dettaglio Soggetto




Le modifiche per la gestione dei comuni storicizzati sono state implementate anche sulle seguenti funzioni:

Ricerche/Ricerca Soggetto

Ricerche/Procedimento per soggetto

Ricerche/Titolo Esecutivo per Soggetto

Gestione Misure Sicurezza/Iscrizione Procedimento Esecuzione Misura Sicurezza Fuori Sentenza

Gestione Misure Sicurezza/Iscrizione Procedimento Esecuzione Misura Sicurezza Applicazione Provvisoria

Iscrizione Istanze/Iscrizione Istanza per Soggetto

## Sottosistema SIUS

Sono state modificate, con le stesse modalità operative descritte per il sottosistema SIEP, le seguenti funzionalità:

Iscrizione e Modifica Soggetto

Iscrizione Manuale/Ricerca Soggetto con procedimenti Sorveglianza

Iscrizione Manuale/Ricerca Titolo Esecutivo per Soggetto

Ricerche e Visualizzazioni/Ricerca Sportello

Esecuzione Misure Alternative/Ricerca Procedimenti di Esecuzione per Soggetto

Esecuzione Sanzioni Sostitutive/Ricerca Procedimenti di Esecuzione sanzioni Sostitutive
per Soggetto

Esecuzione Misure Sicurezza/Ricerca Procedimenti di Esecuzione M.S. per Soggetto

Gestione Permessi e Licenze/Ricerca Permessi per Soggetto

Gestione Permessi e Licenze/Ricerca Licenze per Soggetto

Gestione Permessi e Licenze/Ricerca Licenze per Soggetto

## Sottosistema SIGE
Sono state modificate, con le stesse modalità operative descritte per il sottosistema SIEP, le seguenti funzionalità:

Iscrizione e Modifica Soggetto

Iscrizione Manuale/Ricerca Procedimenti SIEP per Soggetto

Ricerche/Ricerca Procedimenti SIGE per Soggetto