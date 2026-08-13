---
uniqueName: siesmanualpart1-1
displayName: "sies manual part1"
category: "GENERAL"
tags: []
---

# Manuale Utente — SIES v12.9.3.0
### Sistema Informativo dell'Esecuzione Penale e Sorveglianza
**Ministero della Giustizia** — Versione 12.9.3.0

---

> **Documento riservato ad uso interno.**  
> Riproduzione e diffusione non autorizzate sono vietate.  
> Ministero della Giustizia — Direzione Generale per i Sistemi Informativi Automatizzati (DGSIA)

---

## Indice

1. [Introduzione](#1-introduzione)
2. [Accesso al sistema](#2-accesso-al-sistema)
3. [Navigazione e interfaccia](#3-navigazione-e-interfaccia)
4. [SIEP — Sottosistema Informativo Esecuzioni Penali (Procura)](#4-siep--sottosistema-informativo-esecuzioni-penali)
5. [SIUS — Sottosistema Informativo Uffici Sorveglianza](#5-sius--sottosistema-informativo-uffici-sorveglianza)
6. [SIGE — Sottosistema Informativo Gestione Esecuzioni](#6-sige--sottosistema-informativo-gestione-esecuzioni)
7. [SIEPE — SIEP Esterno (UEPE)](#7-siepe--siep-esterno-uepe)
8. [BDMC — Base Dati Magistratura Criminale](#8-bdmc--base-dati-magistratura-criminale)
9. [Funzioni Comuni (SICO)](#9-funzioni-comuni-sico)
10. [Registro SIES (REGESIES)](#10-registro-sies-regesies)
11. [Messaggistica JMS](#11-messaggistica-jms)
12. [Appendice — Glossario](#12-appendice--glossario)

---

## 1. Introduzione

### 1.1 Scopo del documento

Il presente manuale descrive le funzionalità del **Sistema Informativo dell'Esecuzione Penale e Sorveglianza (SIES)**, versione **12.9.3.0**, adottato dal Ministero della Giustizia per la gestione informatizzata dei procedimenti afferenti all'esecuzione penale, alla sorveglianza e alle misure alternative alla detenzione.

Il sistema è utilizzato da:

- **Procure della Repubblica** (modulo SIEP);
- **Uffici di Sorveglianza** (UDS/TDS, modulo SIUS);
- **Tribunali di Sorveglianza** (modulo SIGE);
- **Uffici per l'Esecuzione Penale Esterna** (UEPE, modulo SIEPE);
- **Uffici di cancelleria e amministrazione** per le funzioni comuni (modulo SICO);
- **Personale abilitato alla consultazione** della Base Dati Magistratura Criminale (modulo BDMC).

### 1.2 Ambito di applicazione

SIES integra e coordina i flussi informativi tra i diversi uffici giudiziari coinvolti nell'esecuzione della pena, garantendo:

- la gestione del fascicolo del condannato lungo l'intero ciclo esecutivo;
- il calcolo automatico della pena, degli sconti e dei benefici;
- la trasmissione telematica di atti tra uffici (modulo JMS);
- l'integrazione con sistemi esterni (Re.Ge., PagoPA, BDMC);
- la generazione di statistiche e report per la vigilanza ministeriale.

### 1.3 Requisiti tecnici minimi

| Componente | Requisito minimo |
|---|---|
| Browser | Internet Explorer 11 / Firefox ESR / Chrome 80+ |
| Risoluzione schermo | 1280 × 768 pixel |
| Connessione | Rete intranet ministeriale (VPN) |
| Certificati | Certificato digitale utente (smart card) o credenziali nominali |
| Java Plugin | Non richiesto dalla versione 12.x |

### 1.4 Convenzioni tipografiche

Nel presente manuale sono adottate le seguenti convenzioni:

- **Grassetto**: nomi di campi, pulsanti o etichette dell'interfaccia;
- `Monospazio`: valori tecnici, codici, nomi di parametri interni;
- *Corsivo*: termini normativi o tecnico-giuridici;
- > **Nota**: informazioni operative di rilievo;
- > **Attenzione**: avvertenze su operazioni irreversibili o critiche.

---

## 2. Accesso al sistema

### 2.1 Schermata di Login

La pagina di accesso al sistema, identificata dal titolo **"Login S.I.E.S."**, è il punto di ingresso unico per tutti i moduli della piattaforma. L'URL di accesso è fornito dall'amministratore di sistema di ciascun ufficio.

#### 2.1.1 Campi della schermata di Login

| Campo | Tipo | Obbligatorio | Note |
|---|---|---|---|
| **Username** | Testo (`user_id`) | Sì | Codice utente assegnato dall'amministratore SICO |
| **Password** | Password | Sì | Sensibile alle maiuscole; scade secondo la policy di sicurezza |

L'autenticazione è gestita dall'azione `siap.sico.security.action.ActLogin`. In caso di credenziali errate, il sistema visualizza un messaggio di errore senza indicare quale dei due campi sia scorretto, per ragioni di sicurezza.

#### 2.1.2 Procedura di accesso

1. Aprire il browser e navigare all'URL del portale SIES del proprio ufficio.
2. Inserire il proprio **Username** nel campo corrispondente.
3. Inserire la propria **Password**.
4. Fare clic su **Accedi** (o premere il tasto Invio).
5. In caso di accesso corretto, il sistema reindirizza alla pagina principale del modulo assegnato al profilo utente.

> **Nota**: Dopo un numero configurabile di tentativi di accesso falliti, l'account viene temporaneamente bloccato. Contattare l'amministratore SICO per lo sblocco.

### 2.2 Gestione della sessione

La sessione utente ha una durata massima configurata dall'amministratore di sistema. Allo scadere del timeout di inattività, il sistema reindirizza automaticamente alla pagina di Login. Si raccomanda di salvare sempre il lavoro in corso prima di lasciare la postazione.

### 2.3 Cambio password

La procedura di cambio password è accessibile dalla sezione **Funzioni Comuni (SICO)** → **Sicurezza**. Alla prima configurazione e al rinnovo obbligatorio, il sistema richiede il cambio password prima di consentire l'accesso alle funzionalità operative.

---

## 3. Navigazione e interfaccia

### 3.1 Struttura generale dell'interfaccia

Dopo il login, l'interfaccia di SIES si presenta con una struttura a pannelli articolata in:

- **Barra di navigazione superiore**: accesso ai moduli principali (SIEP, SIUS, SIGE, SIEPE, BDMC, SICO, REGESIES, JMS) in funzione del profilo utente;
- **Pannello di lavoro centrale**: area in cui vengono visualizzate le schermate operative;
- **Barra di stato / notifiche**: eventuali messaggi di sistema, avvisi in scadenza, notifiche JMS in arrivo.

### 3.2 Moduli disponibili

L'accesso ai singoli moduli è governato dal profilo utente assegnato in SICO. La seguente tabella elenca i moduli e gli uffici di riferimento:

| Modulo | Denominazione estesa | Ufficio di riferimento |
|---|---|---|
| **SIEP** | Sottosistema Informativo Esecuzioni Penali | Procura della Repubblica |
| **SIUS** | Sottosistema Informativo Uffici Sorveglianza | UDS / TDS |
| **SIGE** | Sottosistema Informativo Gestione Esecuzioni | Tribunale di Sorveglianza |
| **SIEPE** | SIEP Esterno | UEPE |
| **BDMC** | Base Dati Magistratura Criminale | Accesso trasversale |
| **SICO** | Funzioni Comuni | Amministrazione di sistema |
| **REGESIES** | Registro SIES | Cancelleria / Re.Ge. |
| **JMS** | Messaggistica | Tutti gli uffici |

### 3.3 Funzionalità comuni di navigazione

- **Espandi/Nascondi sezioni**: molte schermate presentano sezioni espandibili/collassabili tramite pulsanti dedicati (effetto *tree*), utili per visualizzare i dati di dettaglio senza sovraccaricare la schermata.
- **Ricerca**: le funzioni di ricerca sono uniformi tra i moduli; supportano la ricerca per chiave (anno/numero), per soggetto (cognome/nome), o per data.
- **Paginazione**: gli elenchi di risultati vengono presentati in pagine navigabili tramite controlli di paginazione standard.
- **Pulsanti Conferma/Annulla**: ogni form di inserimento o modifica prevede il pulsante **Conferma** per salvare e **Annulla** per abbandonare senza modifiche.

---

## 4. SIEP — Sottosistema Informativo Esecuzioni Penali

Il modulo **SIEP** è lo strumento operativo della **Procura della Repubblica** per la gestione dell'esecuzione penale. Consente di seguire il condannato dal momento della definitività della sentenza fino all'estinzione della pena, gestendo fascicoli, sentenze, misure alternative, istanze, cumuli di pena, benefici penitenziari, liberazione anticipata e ordini di esecuzione.

### 4.1 Ricerca Procedimento

**Schermata**: `[S.I.E.S.] - Ricerca Procedimento`

La schermata di ricerca è il punto di accesso a tutti i fascicoli SIEP. Supporta due modalità principali di ricerca.

#### 4.1.1 Ricerca per chiave

| Campo | Nome interno | Tipo | Obbligatorio | Note |
|---|---|---|---|---|
| **Anno (da)** | `CAMPO_CHIAVE_ANNO_INIZIALE` | Numerico | Condizionale | Anno di iscrizione del procedimento |
| **Numero (da)** | `CAMPO_CHIAVE_PROGR_ORIGIN_INIZIALE` | Numerico | Condizionale | Progressivo originario iniziale |
| **Anno (a)** | `CAMPO_CHIAVE_ANNO_FINALE` | Numerico | No | Per ricerca con intervallo |
| **Numero (a)** | `CAMPO_CHIAVE_PROGR_ORIGIN_FINALE` | Numerico | No | Progressivo originario finale |

#### 4.1.2 Ricerca per soggetto

| Campo | Tipo | Note |
|---|---|---|
| **Cognome** | Testo | Ricerca per cognome del soggetto |
| **Nome** | Testo | Ricerca per nome del soggetto |
| **Tipo Ricerca** | Dropdown | Intervallo numerico / Per data iscrizione / Per data iscrizione con intervallo |
| **Giorno iscrizione (da)** | `CAMPO_GIORNO_ISCRIZIONE_INIZIALE` | Numerico (1-31) |
| **Mese iscrizione (da)** | `CAMPO_MESE_ISCRIZIONE_INIZIALE` | Numerico (1-12) |
| **Anno iscrizione (da)** | `CAMPO_ANNO_ISCRIZIONE_INIZIALE` | Numerico |
| **Giorno iscrizione (a)** | `CAMPO_GIORNO_ISCRIZIONE_FINALE` | Numerico (1-31) |
| **Mese iscrizione (a)** | `CAMPO_MESE_ISCRIZIONE_FINALE` | Numerico (1-12) |
| **Anno iscrizione (a)** | `CAMPO_ANNO_ISCRIZIONE_FINALE` | Numerico |

#### 4.1.3 Filtri aggiuntivi

| Campo | Nome interno | Tipo | Note |
|---|---|---|---|
| **Tipo Ufficio** | `CAMPO_CHIAVE_UFFICIO` | Dropdown | Filtra per tipo di ufficio |
| **Distretto** | — | Dropdown | Filtra per distretto giudiziario |
| **Altre BDI** | `altreBDI` | Checkbox | Abilita la ricerca su altre Banche Dati Individuali |

Il pulsante **Ricerca** avvia la query e restituisce l'elenco dei procedimenti corrispondenti ai criteri impostati.

### 4.2 Dettaglio Procedimento

**Schermata**: `[S.I.E.S.] - Dettaglio Procedimento` (`DettaglioFascicoloSiep.jsp`)

Il Dettaglio Procedimento è la schermata centrale del modulo SIEP. Aggrega tutte le informazioni relative al fascicolo del condannato, organizzate in sezioni espandibili.

Le sezioni principali visualizzate sono:

- **Dati soggetto** (`FascicoloSiepModel`): anagrafica, stato giuridico, titolo esecutivo;
- **Pena cumulata** (`PenaCumuloModel`): riepilogo della pena in esecuzione, comprensivo di eventuali cumuli;
- **Ulteriori sanzioni cumulo**: ulteriori pene incluse nel cumulo;
- **Continuazioni**: reati connessi per continuazione;
- **Fascicolo collegato**: riferimenti a fascicoli correlati in altri moduli;
- **Richiesta conversione**: eventuali richieste di conversione della pena;
- **Annotazione manuale**: note libere inserite dall'operatore.

I pulsanti disponibili nella schermata sono:

| Pulsante | Funzione |
|---|---|
| **Espandi/Nascondi** | Mostra o nasconde le sezioni di dettaglio |
| **Calcolo Residuo Pena** | Avvia il calcolo automatico della pena residua da espiare |
| **Disattiva etichetta minorenne** | Rimuove il flag di soggetto minorenne (azione tracciata) |
| **Iscrizione Guidata** | Link visibile se applicabile, avvia la procedura guidata di iscrizione |

### 4.3 Gestione Sentenza

**Schermata**: `[S.I.E.S.] - Gestione Sentenza` (`LoadInserisciSentenza.jsp`)

Questa funzione consente l'inserimento e la modifica delle sentenze associate al fascicolo SIEP.

| Campo | Tipo | Obbligatorio | Note |
|---|---|---|---|
| **Tipo Registro Generale (TipoRG)** | Dropdown | Sì | Tipo di registro generale del procedimento penale |
| **Data Provvedimento — Giorno** | Numerico (1-31) | Condizionale | — |
| **Data Provvedimento — Mese** | Numerico (1-12) | Condizionale | — |
| **Data Provvedimento — Anno** | Numerico | Condizionale | — |
| **Data Provvedimento di Riferimento — Giorno/Mese/Anno** | Numerico | No | Data del provvedimento di riferimento |
| **Tipo Provvedimenti** | Dropdown | No | Tipologia del provvedimento principale |
| **Tipo Provvedimenti Riferimento** | Dropdown | No | Tipologia del provvedimento di riferimento |
| **Tipo Decisione Cassazione** | Dropdown | No | Valorizzabile in caso di sentenza della Cassazione |
| **Autorità Emittente** | Dropdown | Sì | Ufficio giudiziario che ha emesso il provvedimento |
| **Autorità Provv. Rif.** | Dropdown | No | Autorità del provvedimento di riferimento |
| **Flag S/N** | Checkbox/Radio | No | Flag di segnalazione |
| **Tipo Rito 1** | Dropdown | No | Primo tipo di rito processuale |
| **Tipo Rito 2** | Dropdown | No | Secondo tipo di rito processuale |

I pulsanti disponibili sono **Conferma** (salva la sentenza) e **Annulla** (abbandona senza modifiche).

### 4.4 Posizione Giuridica

La sezione **Posizione Giuridica** consente la gestione dello stato giuridico del soggetto in relazione alla sentenza in esecuzione. Comprende la registrazione di: titolo esecutivo, regime detentivo, data inizio espiazione, data fine pena teorica, eventuali sospensioni e informazioni sul regime alternativo.

### 4.5 Misure Alternative

Il modulo SIEP gestisce le **misure alternative alla detenzione** previste dalla normativa vigente (affidamento in prova, detenzione domiciliare, semilibertà, ecc.). Per ciascuna misura è possibile:

- Inserire la misura con data inizio, tipo e autorità concedente;
- Modificare i dati della misura;
- Registrare la revoca o la cessazione della misura;
- Collegare la misura all'istanza corrispondente.

### 4.6 Gestione Istanza

**Schermata**: `[S.I.E.S.] - Gestione Istanza` (`LoadInserisciIstanza.jsp`)

La schermata si articola in due sezioni principali.

#### 4.6.1 Form "Soggetto presentante"

| Campo | Tipo | Obbligatorio | Note |
|---|---|---|---|
| **Cognome** | Testo | Sì (se senza n. proc.) | Obbligatorio in assenza di anno/numero procedimento |
| **Nome** | Testo | Sì (se senza n. proc.) | Obbligatorio in assenza di anno/numero procedimento |
| **Stato Nascita** | Dropdown | No | Se Italia → Comune Nascita diventa obbligatorio |
| **Comune Nascita** | `cod_comune_nascita` | Condizionale | Obbligatorio se Stato Nascita = Italia |
| **Data Nascita — Giorno/Mese/Anno** | Numerico | No | Data di nascita del soggetto |
| **Anno Procedimento** | Numerico | Alternativo al soggetto | In alternativa alla ricerca per anagrafica |
| **Numero Procedimento** | Numerico | Alternativo al soggetto | In alternativa alla ricerca per anagrafica |

#### 4.6.2 Form "Dati dell'Istanza"

| Campo | Nome interno | Tipo | Obbligatorio | Note |
|---|---|---|---|---|
| **Oggetto** | `CAMPO_COD_MOTIVO` | Dropdown | Sì | Tipo/oggetto dell'istanza (decodifica) |
| **Anno Sentenza** | — | Numerico | No | Anno della sentenza a cui si riferisce l'istanza |
| **Numero Sentenza** | — | Numerico | No | Numero della sentenza di riferimento |
| **Data Sentenza** | — | Data | No | Data della sentenza di riferimento |
| **Avvocato** | — | Pulsante ricerca | No | Ricerca e selezione dell'avvocato difensore |

I pulsanti **Ricerca (per soggetto)** e **Ricerca (per oggetto)** consentono di reperire istanze già registrate con criteri distinti.

### 4.7 Ricerca Istanza

**Schermata**: `[S.I.E.S.] - Ricerca Istanza` (`LoadRicercaIstanza.jsp`)

La schermata è composta da due form di ricerca indipendenti:

1. **Per soggetto presentante**: Cognome, Nome → pulsante **Ricerca**;
2. **Per oggetto dell'istanza**: Oggetto (dropdown `CAMPO_COD_MOTIVO`) → pulsante **Ricerca**.

I risultati vengono presentati in un elenco con le colonne: Cognome, Nome, Oggetto, Data Presentazione, Stato, Azioni.

### 4.8 Cumulo Pene e Istruttoria Cumulo

**Schermata**: `[S.I.E.S.] - Gestione Cumulo` (`LoadInserisciIstruttoriaCumulo.jsp`)

La funzione **Apertura Istruttoria Cumulo** consente di avviare la procedura di unificazione di più pene in un unico titolo esecutivo.

> **Nota**: Il sistema verifica automaticamente l'esistenza di un'istruttoria di cumulo già aperta per il soggetto. In caso affermativo, viene visualizzato un avviso con il link all'istruttoria esistente (Anno/Progressivo), per evitare duplicazioni.

Il pulsante **Conferma** avvia formalmente l'istruttoria. La procedura completa di cumulo comprende:

- **Istruttoria cumulo**: raccolta e verifica dei titoli da unificare;
- **Modulo cumulo**: compilazione del provvedimento di cumulo;
- **Calcolo pena cumulata**: calcolo automatico della pena unificata, con applicazione degli sconti e delle riduzioni di legge.

### 4.9 Calcolo Pena e Benefici

Il sistema SIEP include un motore di calcolo automatico della pena che consente di determinare:

- La pena residua da espiare, tenuto conto delle giornate di liberazione anticipata concesse;
- La data fine pena teorica;
- I benefici maturati (permessi premio, semilibertà, affidamento in prova);
- L'applicabilità della liberazione condizionale.

Il **Calcolo Residuo Pena** è accessibile direttamente dalla schermata di Dettaglio Procedimento tramite il pulsante dedicato.

### 4.10 Liberazione Anticipata

**Schermata**: `[S.I.E.S.] - Liberazione Anticipata` (`LoadInserisciLiberazioneAnticipata.jsp`)

La funzione gestisce la registrazione e il calcolo delle ordinanze di liberazione anticipata (L.A.) ai sensi dell'art. 54 O.P.

#### 4.10.1 Tipi di Liberazione Anticipata

| Codice | Tipo |
|---|---|
| **2130** | Liberazione Anticipata ordinaria |
| **2131** | Liberazione Anticipata Speciale (L.A.S.) |
| **2132** | Integrazione Liberazione Anticipata |

La selezione avviene tramite **radio button**.

#### 4.10.2 Campi del form

| Campo | Nome interno | Tipo | Note |
|---|---|---|---|
| **Griglia semestri** | — | Checkbox per semestre | Selezione dei semestri oggetto di L.A. |
| **Giorni L.A. per semestre** | `CAMPO_NUM_GIORNI_LIBANTICIPATA` | Numerico | Giorni di liberazione anticipata per il semestre |
| **Giorni integrazione** | `CAMPO_NUM_GIORNI_LIBANTICIPATA_INT` | Numerico | Giorni di integrazione L.A. per il semestre |
| **Data inizio periodo** | — | Data | Data inizio del semestre |
| **Data fine periodo** | — | Data | Data fine del semestre |
| **Totali** | — | Calcolato | Somma automatica dei giorni concessi |

Il totale complessivo dei giorni di liberazione anticipata viene aggiornato automaticamente all'inserimento dei dati per ciascun semestre.

### 4.11 PagoPA — Gestione Bollettini Pena Pecuniaria

**Schermata**: `[S.I.E.S.] - Gestione Richiesta Bollettini PagoPA` (`LoadGeneraAvvisoPagoPA.jsp`)

Questa funzione consente l'interazione con la piattaforma **PagoPA** per la generazione dei bollettini di pagamento relativi alla pena pecuniaria.

#### 4.11.1 Funzioni disponibili

| Funzione | Descrizione |
|---|---|
| Generazione bollettini pagamento pena pecuniaria | Richiede la generazione dell'intero set di bollettini |
| Generazione primo bollettino pagamento pena pecuniaria | Richiede esclusivamente il bollettino della prima rata |
| Generazione bollettini rate rimanenti | Richiede i bollettini per le rate successive alla prima |

#### 4.11.2 Campi del form

| Campo | Tipo | Note |
|---|---|---|
| **Elenco bollettini da richiedere** | Lista | Visualizza i bollettini selezionabili |
| **Numero bollettini da generare** | Radio button | Tutti (T) / Solo prima rata (P) / Solo rate successive (S) |
| **ID evento** | Hidden | Campo nascosto — id evento associato |
| **Tipo Fascicolo** | Hidden (`tipoFascicolo=SIEP`) | Campo nascosto — identifica il tipo di fascicolo |

Il pulsante **Indietro** (icona `arrowleft24.gif`) consente di tornare alla schermata precedente senza effettuare richieste.

### 4.12 Ordini di Esecuzione

La funzione **Ordine di Esecuzione** gestisce l'emissione dell'ordine di carcerazione o dell'ordine di esecuzione di pena non detentiva. Il sistema supporta:

- Inserimento dell'ordine con dati del soggetto, riferimento alla sentenza e tipo di esecuzione;
- Stampa del documento ufficiale;
- Trasmissione telematica tramite JMS all'istituto penitenziario o all'UEPE competente;
- Registrazione dell'esito (preso in carico, in attesa, eseguito).

### 4.13 Fogli Complementari

I **Fogli Complementari** rappresentano la documentazione aggiuntiva allegata al fascicolo. Permettono la registrazione di atti e provvedimenti che non rientrano nelle categorie principali ma che devono essere tracciati nel sistema.

### 4.14 Notifiche e Scadenzario

Il modulo SIEP include uno **scadenzario** automatico che segnala le scadenze imminenti relative ai fascicoli in gestione:

- Scadenza di misure alternative;
- Date di udienza programmate;
- Termini per presentazione istanze;
- Scadenze di sospensione dell'esecuzione.

Le **notifiche** vengono gestite tramite il modulo JMS e visualizzate nella barra di stato dell'interfaccia.

### 4.15 Statistiche

La sezione **Statistiche** di SIEP fornisce report aggregati sull'attività dell'ufficio, quali:

- Numero di fascicoli aperti/chiusi per periodo;
- Distribuzione per tipo di reato e tipo di pena;
- Statistiche su misure alternative concesse/revocate;
- Monitoraggio dello stato delle esecuzioni.

### 4.16 Revoca e Archiviazione

- **Revoca**: funzione per la registrazione della revoca di una misura alternativa, di una sospensione o di un beneficio. Richiede la specificazione del motivo e della data di revoca.
- **Archiviazione**: procedura per l'archiviazione del fascicolo a seguito dell'estinzione della pena, della morte del condannato o di altro evento estintivo.

### 4.17 Sospensione dell'Esecuzione

La funzione **Sospensione** consente di registrare la sospensione dell'ordine di esecuzione ai sensi dell'art. 656 c.p.p., con indicazione del periodo di sospensione e del provvedimento correlato.

### 4.18 Verbale e Ordine di Scarcerazione

- **Verbale**: inserimento e stampa del verbale di udienza relativo all'esecuzione;
- **Ordine Scarcerazione**: emissione dell'ordine di scarcerazione a seguito di provvedimento di cessazione della pena o di concessione di misura alternativa.

### 4.19 Pena Pecuniaria

Il modulo gestisce la pena pecuniaria (multa/ammenda), incluse le funzioni di:

- Registrazione dell'importo e delle rate;
- Monitoraggio dei pagamenti;
- Integrazione con PagoPA (§ 4.11);
- Conversione della pena pecuniaria in pena detentiva in caso di insolvenza.

### 4.20 Misura Cautelare e Misura di Sicurezza

- **Misura Cautelare**: registrazione e gestione delle misure cautelari connesse al procedimento in esecuzione. Il sistema traccia il tipo di misura (custodia cautelare in carcere, arresti domiciliari, obbligo di presentazione, ecc.), la data di applicazione, l'autorità che ha emesso il provvedimento e la data di cessazione o revoca.
- **Misura di Sicurezza**: inserimento e gestione delle misure di sicurezza (*personali* e *patrimoniali*) applicate in aggiunta o in sostituzione della pena. Per le misure di sicurezza personali (OPG/REMS, casa lavoro, colonia agricola, ecc.) è possibile registrare il tipo, la durata minima, l'istituto di applicazione e i riesami periodici. Per le misure patrimoniali (confisca, cauzione) sono gestiti l'oggetto e l'eventuale restituzione.

### 4.21 Certificato Stato Esecuzione e Posizione Materiale

- **Certificato Stato Esecuzione**: generazione del certificato attestante lo stato di esecuzione della pena per il soggetto selezionato. Il documento include: generalità del condannato, titolo esecutivo, pena irrogata, pena espiata, pena residua, misure alternative in corso, benefici concessi. Il certificato è producibile in formato PDF per la trasmissione o la stampa ufficiale.
- **Posizione Materiale**: gestione della posizione fisica del fascicolo cartaceo (ufficio di deposito, collocazione nello scaffale), utile per il reperimento rapido in cancelleria.

### 4.22 Flusso operativo tipico in SIEP

Il seguente schema descrive il flusso operativo standard dalla ricezione della sentenza definitiva alla chiusura del procedimento:

1. **Ricezione sentenza definitiva** dal sistema Re.Ge. (tramite REGESIES/JMS) → apertura automatica o guidata del fascicolo SIEP;
2. **Verifica posizione giuridica**: controllo di eventuali pene in corso e apertura istruttoria cumulo (§ 4.8) se necessario;
3. **Calcolo pena**: calcolo automatico della data fine pena teorica con eventuale applicazione di detrazioni già concesse;
4. **Emissione ordine di esecuzione** (§ 4.12): trasmissione all'istituto penitenziario o all'UEPE tramite JMS;
5. **Gestione istanze** (§ 4.6): ricezione e trasmissione delle istanze di misura alternativa all'Ufficio di Sorveglianza;
6. **Monitoraggio scadenzario** (§ 4.14): controllo periodico delle scadenze e aggiornamento dello stato;
7. **Liberazione anticipata** (§ 4.10): registrazione delle ordinanze emesse dalla Magistratura di Sorveglianza;
8. **Chiusura fascicolo**: archiviazione (§ 4.16) a seguito dell'estinzione della pena o di altro evento estintivo.

---

## 5. SIUS — Sottosistema Informativo Uffici Sorveglianza

Il modulo **SIUS** è lo strumento operativo degli **Uffici di Sorveglianza** (UDS — Ufficio di Sorveglianza; TDS — Tribunale di Sorveglianza in composizione monocratica) per la gestione dei procedimenti di sorveglianza, delle misure alternative, delle udienze e dei provvedimenti.

### 5.1 Ricerca Procedimento SIUS

**Schermata**: `[S.I.E.S.] - Ricerca Procedimento SIUS` (`LoadRicercaFascicoloSius.jsp`)

#### 5.1.1 Modalità di ricerca

| Modalità | Campi |
|---|---|
| **Per chiave** | Anno (`CAMPO_CHIAVE_ANNO`), Numero (`CAMPO_CHIAVE_PROGR_ORIGIN`) |
| **Per soggetto** | Cognome, Nome; tipo ricerca (intervallo numerico / per data iscrizione / per data iscrizione con intervallo) |

#### 5.1.2 Filtri per tipo ufficio

| Campo | Nome interno | Tipo | Valori |
|---|---|---|---|
| **Tipo Ufficio** | `CAMPO_CHIAVE_UFFICIO` | Dropdown | UDS / UDSM / TDS / TDSM |
| **Comune Ufficio** | — | Pulsante selezione | Apre la lista comuni per il tipo ufficio selezionato |

Le funzioni `ListaTDS_UDS` e `ListaComuniTipoUfficio` supportano la selezione guidata di UDS o Distretti e dei comuni sede di ufficio.

### 5.2 Dettaglio Procedimento SIUS

**Schermata**: `[S.I.E.S.] - Dettaglio Procedimento` (`DettaglioFascicolo.jsp`)

Il Dettaglio Procedimento SIUS aggrega le informazioni del fascicolo di sorveglianza, con riferimento ai modelli dati `FascicoloSiusModel` e `FascicoloGPModel`.

Le sezioni presenti sono:

| Sezione | Contenuto |
|---|---|
| **Soggetto** | Anagrafica, identificativi, posizione giuridica |
| **Sentenza** | Riferimento alla sentenza in esecuzione |
| **Luogo/Istituto Detenzione** | Istituto penitenziario di detenzione corrente |
| **Magistrato assegnatario** | Lista dei magistrati assegnatari del fascicolo |
| **Avvocato** | Lista degli avvocati difensori |
| **Udienza corrente** | Prossima udienza programmata |
| **Fascicoli unificati/collegati** | Riferimenti a fascicoli riuniti o correlati |
| **Note** | Annotazioni libere della cancelleria |
| **Posizione materiale fascicolo** | Collocazione fisica del fascicolo cartaceo |
| **Fascicolo padre (stralcio)** | Riferimento al fascicolo da cui è derivato per stralcio |
| **Tenori stralcio** | Tenori del provvedimento di stralcio |
| **Cancelleria assegnataria** | Ufficio di cancelleria competente |
| **Ulteriori istanze** | Istanze pendenti non ancora definite |
| **Collaboratore** | Eventuale collaboratore di giustizia associato |
| **Licenza libertà anticipata** | Eventuali licenze/liberazione anticipata concesse |
| **Esperto** | Esperto assegnato al fascicolo |

Il pulsante **Espandi/Collassa** (effetto `effettoTree`) controlla la visualizzazione delle sezioni ad albero.

### 5.3 Gestione Udienza SIUS

**Schermata**: `[S.I.E.S.] - GestioneUdienza` (`LoadInserisciUdienza.jsp`)

#### 5.3.1 Campi del form

| Campo | Nome interno | Tipo | Obbligatorio | Note |
|---|---|---|---|---|
| **Data Udienza — Giorno** | `CAMPO_GIORNO_DATA_UDIENZA` | Numerico (1-31) | Sì | — |
| **Data Udienza — Mese** | `CAMPO_MESE_DATA_UDIENZA` | Numerico (1-12) | Sì | — |
| **Data Udienza — Anno** | `CAMPO_ANNO_DATA_UDIENZA` | Numerico | Sì | — |
| **Ora inizio** | — | Numerico (0-23) | No | Ora di inizio udienza |
| **Minuti inizio** | — | Numerico (0-59) | No | — |
| **Ora fine** | — | Numerico (0-23) | No | Ora di fine udienza |
| **Minuti fine** | — | Numerico (0-59) | No | — |
| **Presidente** | `CAMPO_COD_PRESIDENTE` | Dropdown | Condizionale | Presidenza del collegio |
| **Giudice 1** | `CAMPO_COD_GIUDICE_1` | Dropdown | Condizionale | Primo giudice del collegio |
| **Giudice 2** | `CAMPO_COD_GIUDICE_2` | Dropdown | Condizionale | Secondo giudice del collegio |
| **PG — Procuratore Generale** | `CAMPO_COD_PG` | Dropdown | No | Procuratore Generale requirente |
| **Assistente** | `elencoAssistenti` | Dropdown | No | Assistente di cancelleria |
| **Esperto 1** | `CAMPO_COD_ID_ESPERTO_1` | Testo/Ricerca | No | Primo esperto nominato |
| **Esperto 2** | `CAMPO_COD_ID_ESPERTO_2` | Testo/Ricerca | No | Secondo esperto nominato |
| **Numero Collegio** | `CAMPO_NUM_COLLEGIO` | Dropdown | No | Identificativo del collegio giudicante |

> **Nota tecnica (validazione JS)**: Il sistema verifica che tutti i magistrati componenti il collegio (Presidente, Giudice 1, Giudice 2) siano persone diverse. In caso di selezione di un medesimo soggetto in più ruoli, viene mostrato un avviso bloccante prima della conferma.

I pulsanti disponibili sono **Conferma** e **Annulla**.

### 5.4 Misure Alternative (SIUS)

Il modulo SIUS gestisce le misure alternative dal punto di vista dell'Ufficio di Sorveglianza, includendo:

- Ricezione dell'istanza dalla Procura (tramite JMS);
- Fissazione udienza di trattazione;
- Emissione del provvedimento (ordinanza di concessione/rigetto);
- Notifica all'UEPE per la presa in carico (tramite SIEPE);
- Monitoraggio delle scadenze di controllo.

### 5.5 Misure di Sicurezza (SIUS)

La gestione delle **misure di sicurezza** nell'ambito SIUS comprende il riesame periodico, la revisione e la dichiarazione di cessata pericolosità sociale.

### 5.6 Provvedimenti SIUS

La sezione **Provvedimenti** consente di inserire, visualizzare e stampare i provvedimenti del magistrato di sorveglianza (decreti, ordinanze, sentenze monocratiche).

### 5.7 Permessi e Licenze

Il modulo gestisce i permessi premio (art. 30-ter O.P.) e le licenze (semilibertà, art. 52 O.P.), con registrazione di:

- Tipo e durata del permesso/licenza;
- Data inizio e data fine;
- Istituto/luogo di destinazione;
- Esito (regolare rientro, revoca, irreperibilità).

### 5.8 Impugnazioni SIUS

Registrazione e tracciamento delle impugnazioni dei provvedimenti del magistrato di sorveglianza (reclamo al Tribunale di Sorveglianza, ricorso in Cassazione).

### 5.9 Collaboratore, Curatore, Avvocato, Esperto

Il modulo SIUS consente la gestione degli attori del procedimento di sorveglianza:

- **Collaboratore**: soggetto collaboratore di giustizia;
- **Curatore**: curatore speciale nominato;
- **Avvocato**: difensore del condannato, con gestione delle nomine e delle sostituzioni;
- **Esperto**: esperto (psicologo, criminologo, ecc.) nominato per la valutazione del soggetto.

### 5.10 Deposito Ordinanza, Unificazione e Stralcio

- **Deposito Ordinanza**: registrazione del deposito formale del provvedimento emesso;
- **Unificazione**: riunione di fascicoli relativi al medesimo soggetto;
- **Stralcio**: separazione di posizioni all'interno di un fascicolo unitario, con generazione del fascicolo figlio.

### 5.11 Scadenzario e Statistiche SIUS