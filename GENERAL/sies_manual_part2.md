---
uniqueName: siesmanualpart2-1
displayName: "sies manual part2"
category: "GENERAL"
tags: []
---

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