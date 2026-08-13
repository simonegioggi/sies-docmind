---
uniqueName: manualeutentesies12930
displayName: "manuale utente sies 12.9.3.0"
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

Lo **scadenzario** SIUS segnala le scadenze relative a: udienze programmate, permessi in corso, misure da riesaminare, impugnazioni pendenti. Il sistema genera avvisi automatici con anticipo configurabile (es. 30, 15, 7 giorni prima della scadenza), visualizzati nella barra di stato dell'interfaccia e disponibili come lista nello scadenzario.

La sezione **Statistiche** fornisce report sull'attività dell'ufficio di sorveglianza, aggregati per periodo, tipo di misura e tipo di provvedimento. I report disponibili includono:

- **Istanze pervenute**: numero e tipo di istanze ricevute nel periodo;
- **Provvedimenti emessi**: numero e tipo di provvedimenti (concessioni, rigetti, revoche);
- **Udienze celebrate**: numero di udienze con esiti;
- **Misure in corso**: quadro delle misure alternative attive per tipo;
- **Permessi concessi/revocati**: statistiche sui permessi premio e licenze.

### 5.12 Flusso operativo tipico in SIUS

Il flusso operativo standard dell'Ufficio di Sorveglianza segue le fasi:

1. **Ricezione istanza** dalla Procura (SIEP → SIUS tramite JMS) o diretta dal condannato/difensore;
2. **Iscrizione fascicolo SIUS** con associazione alla sentenza in esecuzione (fascicolo SIEP);
3. **Assegnazione magistrato** e fissazione udienza (§ 5.3);
4. **Acquisizione relazione UEPE** (SIEPE → SIUS tramite JMS, § 7.5);
5. **Trattazione in udienza** e **emissione provvedimento** (§ 5.6);
6. **Deposito ordinanza** (§ 5.10) e notifica alle parti;
7. **Trasmissione provvedimento** alla Procura (SIUS → SIEP tramite JMS) e all'UEPE se concessivo;
8. **Monitoraggio della misura** con scadenzario e aggiornamenti periodici.

---

## 6. SIGE — Sottosistema Informativo Gestione Esecuzioni

Il modulo **SIGE** è lo strumento del **Tribunale di Sorveglianza** per la gestione delle udienze collegiali, dei procedimenti di competenza del Tribunale e dei relativi provvedimenti.

### 6.1 Ricerca Fascicolo SIGE

**Schermata**: `Selezionare Procedimento` (`DivRicercaFascicoloBase.jsp`)

| Campo | Tipo | Obbligatorio | Note |
|---|---|---|---|
| **Anno** | Numerico | Sì | Anno del fascicolo SIGE |
| **Numero** | Numerico | No | Numero del fascicolo SIGE |

Il pulsante **Ricerca** restituisce i fascicoli corrispondenti.

### 6.2 Dettaglio Fascicolo SIGE

**Schermata**: `[S.I.A.P.] - Dettaglio Fascicolo Sige` (`DettaglioFascicoloSige.jsp`)

Il dettaglio fascicolo SIGE si basa sui modelli dati `FascicoloSigeModel`, `RichiestaSigeModel` e `MagistratoAssegnatarioModel`.

#### 6.2.1 Dati soggetto

| Campo | Descrizione |
|---|---|
| **Cognome** | Cognome del soggetto |
| **Nome** | Nome del soggetto |
| **CodAfis (CUI)** | Codice identificativo AFIS / Codice Unico Identificativo |

#### 6.2.2 Sezioni del fascicolo

| Sezione | Contenuto |
|---|---|
| **Fascicoli unificati** | Fascicoli riuniti al fascicolo SIGE principale |
| **Note** | Annotazioni libere |
| **Sentenze** | Sentenze collegate al procedimento |
| **Provvedimenti altri** | Provvedimenti di natura diversa dalla sentenza |
| **Pareri** | Pareri resi nel corso del procedimento |
| **Posizione materiale** | Collocazione fisica del fascicolo |
| **Procedimenti SIEP di cumulo** | Lista dei procedimenti SIEP inclusi nel cumulo |
| **Ultima impugnazione** | Riferimento all'ultima impugnazione proposta |
| **Fascicolo collegato** | Fascicoli di altri moduli correlati |
| **Atti in archivio** | Documentazione archiviata |
| **Foglio complementare** | Fogli complementari allegati |

Il pulsante **Gestione Oggetti (tenore)** consente la gestione dei tenori degli atti associati al fascicolo.

### 6.3 Fissazione Udienza SIGE

**Schermata**: `LoadInserisciFissazioneUdienza.jsp`

La schermata di fissazione udienza del Tribunale di Sorveglianza è la più articolata del modulo SIGE, raccogliendo tutte le informazioni necessarie per l'organizzazione dell'udienza collegiale.

| Campo | Tipo | Note |
|---|---|---|
| **Data Udienza** | Data | Data dell'udienza da fissare |
| **Aula** | `AulaUdienzaModel` — Dropdown | Aula in cui si terrà l'udienza |
| **Magistrato assegnatario** | Dropdown/Ricerca | Magistrato relatore assegnato |
| **Tipo Giudizio** | Dropdown | Tipologia del giudizio (es. misura alternativa, liberazione condizionale) |
| **Avvocato** | Lista | Avvocati difensori da citare |
| **Tipo Destinatari** | Dropdown | Tipologia dei destinatari delle notifiche |
| **Tenori** | Lista/Selezione | Tenori dei provvedimenti da trattare |
| **Sezioni udienza** | Griglia | Composizione dell'udienza per sezioni |
| **Notifiche avvocato** | Checkbox/Campo | Tipo e modalità di notifica all'avvocato |
| **Notifiche soggetto** | Checkbox/Campo | Tipo e modalità di notifica al soggetto |
| **Notifiche altro** | Checkbox/Campo | Ulteriori destinatari di notifica |
| **Provvedimento collegato** | Riferimento | Eventuale provvedimento già emesso da collegare |

Il pulsante **Conferma** fissa l'udienza e genera le notifiche.

### 6.4 Udienze Collegiali e Monocratiche

Il modulo SIGE distingue tra:

- **Udienza collegiale**: Tribunale di Sorveglianza in composizione collegiale (Presidente + 2 componenti laici); competente per misure di sicurezza, liberazione condizionale, riabilitazione;
- **Udienza monocratica**: Magistrato di sorveglianza in composizione monocratica; competente per permessi premio, riesami, reclami.

### 6.5 Sentenze SIGE

Registrazione e gestione delle sentenze del Tribunale di Sorveglianza, con collegamento al fascicolo SIEP/SIUS e trasmissione telematica tramite JMS.

### 6.6 Impugnazioni SIGE

Gestione delle impugnazioni avverso le sentenze del Tribunale di Sorveglianza (ricorso in Cassazione), con tracciamento dello stato (ricorso proposto, trasmesso, esitato).

### 6.7 Magistrato Assegnatario e Collegio

- **Magistrato assegnatario**: assegnazione del fascicolo a un relatore specifico;
- **Collegio**: composizione del collegio giudicante per le udienze collegiali, con riferimento ai giudici onorari.

### 6.8 Titolo Esecutivo SIGE

Gestione del titolo esecutivo emesso dal Tribunale di Sorveglianza, con trasmissione alla Procura (modulo SIEP) tramite JMS.

### 6.9 Scadenzario e Sessione SIGE

Lo **scadenzario** SIGE segnala scadenze relative alle udienze programmate, ai termini di impugnazione e ai provvedimenti da adottare. La programmazione delle scadenze è automatica per le udienze inserite nel sistema e può essere completata con scadenze manuali.

La **sessione** gestisce la programmazione delle sessioni periodiche del Tribunale di Sorveglianza, ovvero le sedute collegiali programmate con cadenza regolare (settimanale, quindicinale o mensile). Per ciascuna sessione il sistema permette di:

- Definire la data e l'aula della sessione;
- Assegnare i componenti del collegio (Presidente, giudici togati, giudici onorari);
- Inserire i fascicoli da trattare nella sessione;
- Generare il ruolo di udienza;
- Registrare gli esiti al termine della seduta.

### 6.10 Flusso operativo tipico in SIGE

Il flusso operativo standard del Tribunale di Sorveglianza segue le fasi:

1. **Ricezione atti** dall'Ufficio di Sorveglianza (SIUS → SIGE tramite JMS) o diretta (impugnazioni);
2. **Apertura fascicolo SIGE** con associazione al fascicolo SIUS/SIEP;
3. **Assegnazione magistrato relatore** e programmazione della sessione;
4. **Fissazione udienza collegiale** (§ 6.3) con notifiche alle parti;
5. **Trattazione e deliberazione**: il Presidente verbalizza, il Collegio delibera;
6. **Emissione sentenza** (§ 6.5) e deposito in cancelleria;
7. **Notifica alle parti** e trasmissione alla Procura (SIGE → SIEP tramite JMS);
8. **Gestione impugnazioni** (§ 6.6) in caso di ricorso in Cassazione.

---

## 7. SIEPE — SIEP Esterno (UEPE)

Il modulo **SIEPE** è lo strumento degli **Uffici per l'Esecuzione Penale Esterna (UEPE)** per la gestione delle attività di trattamento extramurario, delle relazioni con la Magistratura di Sorveglianza e del monitoraggio delle misure alternative.

### 7.1 Ricerca Procedimenti SIEPE

**Schermata**: `[S.I.E.S.] - Ricerca Procedimenti SIEPE` (`RicercaFascicoloSiepe.jsp`)

La ricerca dei procedimenti SIEPE restituisce una lista con le seguenti colonne:

| Colonna | Descrizione |
|---|---|
| **Numero SIEPE** | Identificativo del fascicolo SIEPE |
| **Descr. Ufficio** | Denominazione dell'UEPE competente |
| **Numero UEPE** | Numero di registro interno UEPE |
| **Tipo Incarico** | Tipologia dell'incarico (relazione, presa in carico, ecc.) |
| **Data Iscriz. Proc.** | Data di iscrizione del procedimento |
| **Cognome** | Cognome del soggetto |
| **Nome** | Nome del soggetto |
| **Data di nascita** | Data di nascita del soggetto |
| **Azioni** | Link alle azioni disponibili (visualizza, modifica) |

### 7.2 Dettaglio Fascicolo SIEPE

Il fascicolo SIEPE contiene le informazioni relative al trattamento extramurario del soggetto, incluse:

- Dati anagrafici e giuridici;
- Tipo e durata della misura alternativa in corso;
- Assistente sociale referente;
- Esperto assegnato;
- Relazioni redatte;
- Attività svolte.

### 7.3 Attività

La sezione **Attività** consente la registrazione delle attività svolte nell'ambito del trattamento: colloqui, visite domiciliari, incontri con servizi sociali, partecipazione a programmi trattamentali.

### 7.4 Assistenti Sociali ed Esperti

Il modulo SIEPE gestisce l'anagrafica degli **assistenti sociali** e degli **esperti** (psicologi, criminologi) assegnati ai fascicoli SIEPE, con le relative specializzazioni e disponibilità.

### 7.5 Relazioni

La funzione **Relazioni** consente la redazione, la registrazione e la trasmissione (tramite JMS) delle relazioni richieste dalla Magistratura di Sorveglianza, quali:

- Relazione di indagine socio-familiare;
- Relazione di aggiornamento sulla misura in corso;
- Relazione finale.

### 7.6 Ricezione Atti e Richieste

- **Ricezione Atti**: gestione degli atti ricevuti dagli uffici giudiziari (SIUS, SIGE) tramite JMS;
- **Richieste**: gestione delle richieste provenienti dalla Magistratura o dall'UEPE stesso.

### 7.7 Sessione SIEPE

La **sessione** SIEPE gestisce i calendari degli assistenti sociali e degli esperti, nonché la programmazione delle attività periodiche dell'UEPE.

### 7.8 Flusso operativo tipico in SIEPE

Il flusso operativo standard dell'UEPE segue le fasi:

1. **Ricezione incarico** dalla Magistratura di Sorveglianza (SIUS → SIEPE tramite JMS): richiesta di relazione socio-familiare o presa in carico del soggetto in misura alternativa;
2. **Apertura fascicolo SIEPE** e assegnazione al responsabile del caso (assistente sociale);
3. **Svolgimento attività** (§ 7.3): colloqui, visite domiciliari, contatti con servizi territoriali;
4. **Redazione relazione** (§ 7.5): il responsabile del caso redige la relazione richiesta nel sistema;
5. **Trasmissione relazione** alla Magistratura (SIEPE → SIUS tramite JMS) entro i termini stabiliti;
6. **Monitoraggio della misura**: aggiornamento periodico dello stato del soggetto, registrazione di criticità o violazioni;
7. **Chiusura incarico**: registrazione dell'esito finale (misura eseguita, revocata, scaduta).

---

## 8. BDMC — Base Dati Magistratura Criminale

Il modulo **BDMC** consente l'accesso alla Base Dati Magistratura Criminale, sistema di consultazione trasversale che integra dati provenienti da SIEP, SIUS e SIGE.

### 8.1 Fascicoli SIEP-BDMC

Funzione di consultazione dei fascicoli SIEP registrati nella base dati centralizzata, con accesso alle informazioni sintetiche sul soggetto e sulla pena.

### 8.2 Notifiche SIES

La sezione **Notifiche SIES** consente la visualizzazione e la gestione delle notifiche generate dal sistema SIES verso la BDMC, relative a eventi significativi (emissione ordine di esecuzione, concessione misura alternativa, ecc.).

### 8.3 Prenotazioni

La funzione **Prenotazioni** gestisce le richieste di accesso a dati soggetti a riservatezza rafforzata, con tracciamento dell'utente richiedente e della motivazione dell'accesso.

### 8.4 SBView — Viste sui dati BDMC

Il modulo **sbview** fornisce viste preconfigurate sui principali aggregati informativi della BDMC:

| Vista | Contenuto |
|---|---|
| **Viste Notifiche** | Elenco notifiche SIES verso BDMC per soggetto/periodo |
| **Viste Reati** | Dettaglio reati contestati per soggetto |
| **Viste Pene** | Dettaglio pene irrogate e stato esecutivo |
| **Viste Capi Imputazione** | Capi di imputazione per procedimento |

---

## 9. Funzioni Comuni (SICO)

Il modulo **SICO** raccoglie le funzioni trasversali di amministrazione del sistema, accessibili agli utenti con profilo amministrativo o di gestione.

### 9.1 Gestione Utenti

**Schermata**: `[S.I.E.S.] - Dettaglio Utente` (`LoadInserisciUtente.jsp`)

#### 9.1.1 Funzioni disponibili

- **Inserimento Utente**: creazione di un nuovo account utente;
- **Modifica Utente**: aggiornamento dei dati di un utente esistente.

#### 9.1.2 Campi del form

| Campo | Tipo | Obbligatorio | Note |
|---|---|---|---|
| **Username** | Testo (sola lettura in modifica) | Sì | Codice identificativo dell'utente; non modificabile dopo la creazione |
| **Cognome** | Testo (max 50 caratteri) | Sì | — |
| **Nome** | Testo (max 50 caratteri) | Sì | — |
| **Telefono** | Testo (max 50 caratteri) | No | Numero di telefono dell'utente |
| **Fax** | Testo (max 50 caratteri) | No | Numero fax dell'utente |
| **E-mail** | Testo (max 50 caratteri) | No | Indirizzo di posta elettronica |
| **Ufficio** | Dropdown | Sì | Ufficio di appartenenza dell'utente |
| **Profilo** | Dropdown | Sì | Profilo di autorizzazione assegnato |
| **Data Fine Validità — Giorno** | Numerico | No | Giorno di scadenza dell'account |
| **Data Fine Validità — Mese** | Numerico | No | Mese di scadenza dell'account |
| **Data Fine Validità — Anno** | Numerico | No | Anno di scadenza dell'account |

#### 9.1.3 Pulsanti

| Pulsante | Funzione |
|---|---|
| **Salva** | Salva le modifiche all'utente |
| **Reset Password** | Reimposta la password dell'utente; richiede conferma tramite finestra di dialogo JavaScript |

> **Attenzione**: Il Reset Password genera una password temporanea comunicata all'utente; al primo accesso successivo il sistema richiederà il cambio obbligatorio.

### 9.2 Gestione Profili

**Schermata**: `[S.I.E.S.] - GestioneProfilo` (`LoadInserisciProfilo.jsp`)

#### 9.2.1 Funzioni disponibili

- **Inserimento di un Profilo**: creazione di un nuovo profilo di autorizzazione;
- **Modifica di un Profilo**: aggiornamento di un profilo esistente.

#### 9.2.2 Campi del form

| Campo | Tipo | Obbligatorio | Note |
|---|---|---|---|
| **Descrizione** | Testo (size=80, max 60 caratteri) | Sì | Denominazione del profilo |
| **Data Fine Validità — Giorno/Mese/Anno** | Numerico | No | Data di scadenza del profilo (opzionale) |

#### 9.2.3 Lista Profili

La lista dei profili esistenti riporta le colonne: **Descrizione**, **Data Fine Validità**, **Azioni** (modifica).

### 9.3 Gestione Magistrati

Il modulo consente la gestione dell'anagrafica dei **magistrati** e dei **magistrati competenti** per i diversi uffici, incluse le assegnazioni per competenza territoriale e le date di validità degli incarichi.

### 9.4 Gestione Soggetti

La sezione **Soggetti** in SICO fornisce un accesso centralizzato all'anagrafica dei soggetti registrati nel sistema, con funzioni di:

- Ricerca e visualizzazione del soggetto;
- Gestione dei **soggetti storici** (soggetti con dati anagrafici modificati nel tempo);
- Gestione delle **residenze** (storico degli indirizzi del soggetto).

### 9.5 Decodifiche

La sezione **Decodifiche** gestisce le tabelle di riferimento utilizzate dai dropdown e dalle liste del sistema (tipi di reato, tipi di pena, tipi di ufficio, tipi di provvedimento, ecc.). Le modifiche alle decodifiche hanno impatto su tutte le funzioni che le utilizzano.

### 9.6 Log ed Eventi

- **Log**: visualizzazione del log degli accessi e delle operazioni significative eseguite dagli utenti nel sistema;
- **Eventi**: gestione della tabella eventi, utilizzata per la generazione di notifiche automatiche e scadenzario.

### 9.7 Gestione Uffici

La funzione **Uffici** consente di gestire l'anagrafica degli uffici giudiziari registrati nel sistema, con le informazioni di sede, tipo, distretto e referenti.

### 9.8 Sicurezza

La sezione **Sicurezza** raccoglie le funzioni di configurazione della sicurezza applicativa:

- Policy di scadenza password;
- Regole di complessità password;
- Gestione dei blocchi account;
- Configurazione del timeout di sessione.

### 9.9 Libertà Anticipata (SICO)

La funzione centralizzata di **Libertà Anticipata** in SICO consente la gestione amministrativa dei provvedimenti di liberazione anticipata a livello di sistema, inclusa la generazione di report aggregati per la vigilanza ministeriale.

### 9.10 Template

La gestione dei **template** consente la configurazione dei modelli documentali utilizzati per la generazione automatica di atti (ordinanze, decreti, comunicazioni) dal sistema SIES.

### 9.11 Webservice e Calendario

- **Webservice**: configurazione e monitoraggio dei servizi web esposti e consumati da SIES verso/da sistemi esterni (Re.Ge., PagoPA, BDMC);
- **Calendario**: gestione del calendario delle udienze e delle sessioni, condiviso tra i moduli SIUS e SIGE.

### 9.12 Invio Segnalazioni

La funzione **Invio Segnalazioni** consente agli utenti di inviare segnalazioni operative (anomalie, richieste di supporto) direttamente dall'interfaccia SIES, con tracciamento dello stato di lavorazione.

### 9.13 Calendario Udienze

Il **Calendario** è uno strumento condiviso tra i moduli SIUS e SIGE che permette la visualizzazione mensile/settimanale delle udienze programmate. Gli utenti con opportuni diritti possono:

- Visualizzare tutte le udienze dell'ufficio per giorno/settimana/mese;
- Identificare conflitti di agenda tra udienze programmate nella stessa aula o con gli stessi magistrati;
- Esportare il calendario in formato stampabile.

### 9.14 Best practice amministrative

Si raccomanda agli amministratori SICO di:

- Verificare periodicamente la validità degli account utente e disabilitare quelli non più necessari impostando la **Data Fine Validità**;
- Aggiornare tempestivamente l'anagrafica dei magistrati in caso di trasferimenti o cessazioni;
- Mantenere aggiornate le **decodifiche** in accordo con le circolari ministeriali di aggiornamento;
- Conservare i log di accesso per il periodo previsto dalla normativa sulla protezione dei dati personali;
- Effettuare periodicamente il controllo degli **scarti** in REGESIES per garantire la completezza della base dati.

---

## 10. Registro SIES (REGESIES)

Il modulo **REGESIES** gestisce i dati del Registro Generale (Re.Ge.) integrati nel sistema SIES, consentendo la consultazione e la gestione delle informazioni provenienti dal sistema Re.Ge. del Ministero della Giustizia.

### 10.1 Soggetti Re.Ge.

**File**: `ElencoRegeSoggetto.jsp`, `DettaglioRegeSoggetto.jsp`, `ModificaRegeSoggetto.jsp`

La gestione dei **soggetti Re.Ge.** comprende:

- **Elenco**: lista dei soggetti registrati nel Re.Ge. collegati a SIES;
- **Dettaglio**: visualizzazione delle informazioni complete del soggetto (anagrafica, posizione giuridica);
- **Modifica**: aggiornamento dei dati del soggetto Re.Ge. nel perimetro SIES.

### 10.2 Sentenze Re.Ge.

Gestione delle sentenze registrate nel Re.Ge. e trasmesse a SIES, con verifica della coerenza dei dati e gestione delle eventuali discrepanze.

### 10.3 Circostanze

Gestione delle circostanze aggravanti ed attenuanti associate ai reati registrati nel Re.Ge., rilevanti per il calcolo della pena.

### 10.4 Notizie di Reato

Consultazione e gestione delle notizie di reato acquisite dal Re.Ge., con possibilità di collegamento ai fascicoli SIEP corrispondenti.

### 10.5 Residenze

Gestione dello storico delle residenze dei soggetti registrati nel Re.Ge., con allineamento alle residenze gestite in SICO.

### 10.6 Avvocati

Anagrafica degli avvocati difensori registrati nel Re.Ge., con informazioni su abilitazione, ordine di appartenenza e recapiti.

### 10.7 Scarti

La sezione **Scarti** gestisce i casi in cui i dati trasmessi dal Re.Ge. non sono stati acquisiti correttamente da SIES, consentendo la visualizzazione dell'errore e la richiesta di re-invio o correzione manuale.

---

## 11. Messaggistica JMS

Il modulo **JMS** (Java Message Service) costituisce il sottosistema di **messaggistica asincrona** di SIES, che gestisce la trasmissione telematica di atti e comunicazioni tra i diversi uffici giudiziari e tra SIES e i sistemi esterni.

### 11.1 Elenco Atti Trasmessi

**Schermata**: `ListaMessaggiTrasmessi.jsp` — "Elenco Atti Trasmessi"

#### 11.1.1 Parametri di ricerca

| Parametro | Tipo | Descrizione |
|---|---|---|
| **dataRicercaInizio** | Data | Data inizio dell'intervallo di ricerca |
| **dataRicercaFine** | Data | Data fine dell'intervallo di ricerca |
| **codUtente** | Testo | Codice utente che ha effettuato la trasmissione |
| **tipoUtente** | Dropdown | Tipo di utente mittente |
| **tipoEsito** | Dropdown | Esito della trasmissione (successo, errore, in attesa) |
| **codTipoOperazione** | Dropdown | Tipo di operazione trasmessa |

L'elenco risultante mostra per ogni atto: data/ora trasmissione, tipo operazione, ufficio mittente, ufficio destinatario, esito, azioni disponibili.

### 11.2 Lista Atti Ricevuti

**Schermata**: `ListaMessaggiRicevuti.jsp` — "Lista Atti Ricevuti"

#### 11.2.1 Parametri di ricerca

| Parametro | Tipo | Descrizione |
|---|---|---|
| **codUfficio** | Testo | Codice dell'ufficio destinatario |
| **annoSiep** | Numerico | Anno del fascicolo SIEP collegato |
| **progrSiep** | Numerico | Progressivo del fascicolo SIEP collegato |
| **flagIncludeInCarico** | Checkbox | Se attivo, include gli atti già presi in carico |

### 11.3 Lista Atti Ricevuti SIUS

**Schermata**: `ListaMessaggiRicevutiSius.jsp` — "Lista Atti ricevuti"

Rispetto alla lista standard, aggiunge i parametri:

| Parametro aggiuntivo | Tipo | Descrizione |
|---|---|---|
| **annoSius** | Numerico | Anno del fascicolo SIUS collegato |
| **progrSius** | Numerico | Progressivo del fascicolo SIUS collegato |
| **data1** | Data | Data inizio intervallo di ricezione |
| **data2** | Data | Data fine intervallo di ricezione |

### 11.4 Presa in Carico e Trasmissione per Competenza

**Schermata**: `ListaMessaggiPresincaricoTrasmissioneCompetenza.jsp`

Questa schermata gestisce due operazioni fondamentali nel ciclo di vita di un messaggio JMS:

- **Presa in carico**: l'ufficio destinatario accetta formalmente l'atto ricevuto, avviando la lavorazione interna;
- **Trasmissione per competenza**: l'ufficio ricevente trasmette l'atto a un altro ufficio (es. da UDS a TDS) quando la competenza non è propria.

### 11.5 Contatore Atti Ricevuti

**Schermata**: `ContaMessaggiRicevutiTrasmissioneCompetenza.jsp`

Visualizza il **contatore** degli atti ricevuti in attesa di presa in carico o di trasmissione per competenza, utile per il monitoraggio del carico di lavoro dell'ufficio.

### 11.6 Messaggi SIUS

Il sottosistema JMS-SIUS gestisce la messaggistica specifica dell'Ufficio di Sorveglianza, inclusi:

- Trasmissione di relazioni dall'UEPE (SIEPE → SIUS);
- Trasmissione di provvedimenti alla Procura (SIUS → SIEP);
- Ricezione di istanze dalla Procura (SIEP → SIUS);
- Comunicazioni con il Tribunale di Sorveglianza (SIUS ↔ SIGE).

### 11.7 Elenco Esiti Ricerca Fascicolo SIEP — Altre BDI

**Schermata**: `ListaEsitiRicercaFascAltreBDI.jsp` — "Elenco Esiti Ricerca Fascicolo SIEP altre BDI"

Questa schermata visualizza i risultati delle ricerche effettuate su **altre Banche Dati Individuali** (BDI) nell'ambito della ricerca del fascicolo SIEP, consentendo l'acquisizione di dati da sistemi esterni collegati.

### 11.8 Note operative sulla messaggistica

> **Nota**: Il modulo JMS opera in modalità **asincrona**: la trasmissione di un atto non implica la ricezione immediata da parte del destinatario. Il mittente può verificare l'esito della trasmissione nella schermata "Elenco Atti Trasmessi".

> **Attenzione**: La presa in carico di un atto è un'operazione **irreversibile**: una volta preso in carico, l'atto non può essere re-inviato automaticamente. In caso di errore, contattare l'amministratore di sistema.

### 11.9 Ciclo di vita di un messaggio JMS

Il seguente schema descrive il ciclo di vita standard di un atto trasmesso tramite JMS:

| Stato | Descrizione |
|---|---|
| **In coda** | Il messaggio è stato generato e posto in coda di trasmissione |
| **Trasmesso** | Il messaggio è stato inviato al destinatario; in attesa di presa in carico |
| **Ricevuto** | Il destinatario ha ricevuto il messaggio nel proprio inbox |
| **Preso in carico** | L'ufficio destinatario ha formalmente accettato l'atto e avviato la lavorazione |
| **Per competenza** | L'atto è stato girato a un terzo ufficio per competenza |
| **Esitato** | L'ufficio destinatario ha fornito un esito (accettato, rigettato, ecc.) |
| **Errore** | Si è verificato un errore tecnico nella trasmissione; richiede intervento |

### 11.10 Tipi di operazione gestiti da JMS

Le principali tipologie di atti gestiti dal modulo JMS in SIES sono:

| Tipo operazione | Mittente | Destinatario | Descrizione |
|---|---|---|---|
| Trasmissione Ordine Esecuzione | SIEP (Procura) | Istituto Penitenziario | Ordine di carcerazione |
| Trasmissione Istanza | SIEP (Procura) | SIUS (UDS) | Istanza di misura alternativa |
| Richiesta Relazione | SIUS (UDS) | SIEPE (UEPE) | Richiesta relazione socio-familiare |
| Trasmissione Relazione | SIEPE (UEPE) | SIUS (UDS) | Relazione dell'UEPE |
| Trasmissione Provvedimento | SIUS/SIGE | SIEP (Procura) | Ordinanza/Sentenza di sorveglianza |
| Notifica Sentenza TdS | SIGE | SIEP / SIUS | Sentenza del Tribunale di Sorveglianza |
| Comunicazione Scarcerazione | SIEP (Procura) | Istituto Penitenziario | Ordine di scarcerazione |

---

## 12. Appendice — Glossario

| Termine | Definizione |
|---|---|
| **AFIS** | Automated Fingerprint Identification System — sistema biometrico di identificazione |
| **Beneficio penitenziario** | Misura premiale prevista dall'Ordinamento Penitenziario (permesso premio, semilibertà, ecc.) |
| **BDI** | Banca Dati Individuale — archivio informatizzato relativo a un soggetto |
| **BDMC** | Base Dati Magistratura Criminale |
| **Cumulo pene** | Unificazione di più pene detentive in un unico titolo esecutivo |
| **CUI** | Codice Unico Identificativo del soggetto in SIES |
| **Data fine pena** | Data teorica di conclusione dell'espiazione della pena |
| **DGSIA** | Direzione Generale per i Sistemi Informativi Automatizzati |
| **GP** | Giudice di Pace |
| **Istruttoria cumulo** | Procedura preliminare alla definizione del cumulo di pene |
| **JMS** | Java Message Service — sistema di messaggistica asincrona |
| **LA / LAS** | Liberazione Anticipata / Liberazione Anticipata Speciale |
| **Misura alternativa** | Istituto che consente di scontare la pena fuori dal carcere (affidamento, detenzione domiciliare, ecc.) |
| **Misura di sicurezza** | Provvedimento applicato in aggiunta o in alternativa alla pena per soggetti pericolosi |
| **Ordinamento Penitenziario (O.P.)** | Legge 26 luglio 1975, n. 354, e successive modificazioni |
| **Ordine di esecuzione** | Provvedimento con cui la Procura dispone l'esecuzione della pena definitiva |
| **PagoPA** | Piattaforma nazionale per i pagamenti verso la PA |
| **Pena pecuniaria** | Sanzione pecuniaria (multa o ammenda) irrogata in sentenza |
| **Posizione giuridica** | Insieme dei dati che descrivono lo stato giuridico del condannato |
| **Posizione materiale** | Collocazione fisica del fascicolo cartaceo nell'archivio |
| **Procura della Repubblica** | Ufficio del Pubblico Ministero |
| **Re.Ge.** | Registro Generale delle notizie di reato |
| **SICO** | Sottosistema delle Funzioni Comuni |
| **SIES** | Sistema Informativo dell'Esecuzione Penale e Sorveglianza |
| **SIGE** | Sottosistema Informativo Gestione Esecuzioni (Tribunale Sorveglianza) |
| **SIEP** | Sottosistema Informativo Esecuzioni Penali (Procura) |
| **SIEPE** | SIEP Esterno (UEPE) |
| **SIUS** | Sottosistema Informativo Uffici Sorveglianza |
| **Stralcio** | Separazione di una posizione da un fascicolo unitario |
| **TDS** | Tribunale di Sorveglianza |
| **Tenore** | Testo/oggetto di un provvedimento giudiziario |
| **Timeout sessione** | Periodo di inattività oltre il quale la sessione utente viene chiusa automaticamente |
| **Titolo esecutivo** | Sentenza passata in giudicato che costituisce il fondamento dell'esecuzione penale |
| **UDS** | Ufficio di Sorveglianza |
| **UEPE** | Ufficio per l'Esecuzione Penale Esterna |
| **Unificazione fascicoli** | Riunione di fascicoli distinti relativi allo stesso soggetto |

---

*Fine del Manuale Utente SIES v12.9.3.0*

---

> **Versione documento**: 12.9.3.0  
> **Data di emissione**: 2024  
> **Classificazione**: Uso interno — Ministero della Giustizia  
> **Redatto da**: Direzione Generale per i Sistemi Informativi Automatizzati (DGSIA)