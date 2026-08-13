---
uniqueName: manualeutentesies
displayName: "MANUALE UTENTE SIES"
category: "GENERAL"
tags: []
---

# MANUALE UTENTE SISTEMA SIES
## Sistema Informativo per l'Esecuzione Penale e la Sorveglianza

**Versione:** VSCI_12.8.5.0  
**Data:** Febbraio 2026  
**Ambiente:** Visual Studio Code - Insiders  

---

## INDICE

1. [Introduzione](#1-introduzione)
2. [Premessa](#2-premessa)
3. [Architettura del Sistema](#3-architettura-del-sistema)
4. [Moduli Applicativi](#4-moduli-applicativi)
5. [Requisiti Tecnici](#5-requisiti-tecnici)
6. [Installazione e Configurazione](#6-installazione-e-configurazione)
7. [Accesso al Sistema](#7-accesso-al-sistema)
8. [Interfaccia Utente](#8-interfaccia-utente)
9. [Modulo SIEP - Sistema Informativo Esecuzione Penale](#9-modulo-siep---sistema-informativo-esecuzione-penale)
10. [Modulo SIUS - Sistema Informativo Uffici Sorveglianza](#10-modulo-sius---sistema-informativo-uffici-sorveglianza)
11. [Modulo AMMINISTRAZIONE](#11-modulo-amministrazione)
12. [Funzionalità Comuni](#12-funzionalità-comuni)
13. [Integrazione con Sistemi Esterni](#13-integrazione-con-sistemi-esterni)
14. [Glossario](#14-glossario)
15. [Supporto e Contatti](#15-supporto-e-contatti)

---

## 1. INTRODUZIONE

Il Sistema Informativo per l'Esecuzione penale e la Sorveglianza (SIES) è un'applicazione web-based progettata per automatizzare e digitalizzare l'attività nella fase esecutiva del processo penale in Italia.

### 1.1 Scopo del Sistema

SIES nasce per diventare il Sistema unico di gestione, a livello nazionale, per tutti gli uffici coinvolti nell'esecuzione penale, tra cui:
- **Procure della Repubblica**
- **Tribunali di Sorveglianza**
- **Uffici di Sorveglianza**
- **Magistrature di Distretto**

### 1.2 Obiettivi Principali

- ✓ Garantire la **condivisione dei dati** tra uffici di esecuzione e sorveglianza
- ✓ **Produrre documenti** in modo automatizzato
- ✓ **Supportare le decisioni** dei P.M. e dei vari giudici coinvolti nel procedimento
- ✓ **Semplificare le attività** di ricerca di informazioni all'interno dei vari uffici
- ✓ **Eliminare duplicazioni** di dati attraverso un database centralizzato distrettuale
- ✓ **Ridurre errori** e omissioni attraverso procedure controllate e guidate

---

## 2. PREMESSA

### 2.1 Contesto

La situazione attuale relativa agli uffici coinvolti nell'esecuzione penale e nella sorveglianza si presenta quanto mai disomogenea e complessa. Ogni ufficio coinvolto nel Sistema gestisce gli atti e le procedure in modo autonomo e con software spesso personalizzati o adattati alle proprie esigenze, ma comunque diversi da città a città e da ufficio ad ufficio.

### 2.2 Soluzione SIES

Il SIES ha il compito di semplificare la gestione e lo scambio dei dati all'interno degli uffici, evitando di duplicare le informazioni, grazie all'**utilizzo di un Database centralizzato a livello distrettuale** da cui ogni operatore è in grado di attingere in tempo reale informazioni, sempre aggiornate.

### 2.3 Vantaggi per l'Utente

I vantaggi più evidenti sono:

- **Conoscenza in tempo reale** dell'attuale stato del titolo esecutivo e degli eventi dell'esecuzione
- **Consultazione dei provvedimenti** emessi dai vari uffici e dei documenti prodotti
- **Acquisizione elettronica** dei titoli esecutivi archiviati dagli uffici di esecuzione
- **Scambio elettronico** di dati, informazioni e documenti tra gli uffici giudiziari
- **Integrazione** con il Dipartimento per l'Amministrazione Penitenziaria (DAP)
- **Supporto alle attività ispettive** ordinarie e straordinarie
- **Maggiore efficienza** ed efficacia nelle attività degli uffici

---

## 3. ARCHITETTURA DEL SISTEMA

### 3.1 Concetti Base

Il progetto SIES realizza una **banca dati dei titoli esecutivi su base distrettuale** in grado di raccogliere tutte le informazioni che si vanno formando nel corso dell'esecuzione penale.

### 3.2 Architettura Tecnica

L'architettura tecnica di riferimento si basa su:

- **Sistema distrettuale** alimentato dai sottosistemi dei vari Uffici Giudiziari
- **Banca Dati Integrata (BDI)** che consolida tutti i dati
- **29 basi dati distribuite** sul territorio nazionale
- **Architettura Web** accessibile tramite browser

### 3.3 Interconnessione

L'architettura è referenziata su base distrettuale, ma interconnessa a livello nazionale attraverso cui è possibile:
- Lo scambio automatico delle informazioni tra i diversi domini della giustizia
- L'alimentazione sistematica delle basi dati nazionali (Casellario, DAP)
- La "circolarità informativa" obbligatoria

### 3.4 Elemento Centrale: Il Titolo Esecutivo

Si è scelto, quale elemento su cui convogliare le informazioni, il **titolo esecutivo**. Il sistema prevede:
- Memorizzazione di tutti gli eventi dell'esecuzione (qualunque sia l'ufficio fonte)
- Gestione dei provvedimenti sia in fase di produzione (office automation) che di archiviazione
- Arricchimento incrementale della base informativa distrettuale e nazionale

---

## 4. MODULI APPLICATIVI

SIES è suddiviso in tre moduli applicativi principali:

### 4.1 SIEP - Sistema Informativo Esecuzione Penale
**Destinato a:** Procure della Repubblica  
**Funzione:** Gestione dell'attività di esecuzione penale

### 4.2 SIUS - Sistema Informativo Uffici Sorveglianza
**Destinato a:** Tribunali e Uffici di Sorveglianza  
**Funzione:** Gestione della sorveglianza e delle misure alternative

### 4.3 AMMINISTRAZIONE (AMM)
**Destinato a:** Amministratori di sistema  
**Funzione:** Gestione utenti, profili, configurazioni di sistema

---

## 5. REQUISITI TECNICI

### 5.1 Requisiti Server

**Software richiesto:**
- Java Development Kit (JDK) 21
- Server applicativo compatibile (Tomcat/JBoss)
- Database Oracle (con driver JDBC 23.6.0.24.10 o superiore)

**Librerie principali:**
- Apache POI 3.17 (gestione documenti Excel)
- MyBatis 3.5.16 (mappatura database)
- Log4j 2.24.3 (logging)
- Apache Tika 2.9.2 (parsing documenti)

### 5.2 Requisiti Client

**Browser supportati:**
- Internet Explorer 11 o superiore
- Mozilla Firefox (versione recente)
- Google Chrome (versione recente)
- Microsoft Edge

**Requisiti minimi:**
- Connessione di rete stabile
- Risoluzione minima schermo: 1024x768
- JavaScript abilitato
- Cookies abilitati

### 5.3 Requisiti di Rete

- Connessione alla rete giudiziaria (Intranet)
- Accesso al database distrettuale
- Porte necessarie configurate per comunicazioni JMS

---

## 6. INSTALLAZIONE E CONFIGURAZIONE

### 6.1 Struttura del Progetto

Il progetto SIES è composto da due moduli principali:

#### siesWeb
Applicazione web principale contenente tutti i moduli SIEP, SIUS e AMM.

**Struttura directory:**
```
siesWeb/
├── src/                          # Codice sorgente Java
│   ├── siap/                     # Package principale applicazione
│   │   ├── bdmc/                 # Banca Dati Misure Cautelari
│   │   ├── controller/           # Controller applicativi
│   │   ├── dao/                  # Data Access Objects
│   │   ├── jms/                  # Java Message Service
│   │   ├── regesies/             # Registro Generale
│   │   ├── sico/                 # Sistema Informativo Comune
│   │   ├── sige/                 # Sistema Informativo Gestione Esecuzione
│   │   ├── siep/                 # Sistema Informativo Esecuzione Penale
│   │   ├── siepe/                # Sistema Informativo Esecuzione Pene
│   │   ├── sius/                 # Sistema Informativo Uffici Sorveglianza
│   │   └── util/                 # Utilità
│   └── it/eng/mig/               # Package Engineering
├── defaultroot/                  # Root web application
│   ├── css/                      # Fogli di stile
│   ├── images/                   # Immagini
│   ├── jsp/                      # Java Server Pages
│   ├── help/                     # File di aiuto HTML
│   ├── WEB-INF/                  # Configurazione web
│   │   ├── web.xml               # Deployment descriptor
│   │   └── lib/                  # Librerie JAR
│   └── login.jsp                 # Pagina di login
└── pom.xml                       # Configurazione Maven
```

#### siesEsecuzione
Modulo per il trasferimento dei fogli complementari verso NSC (No Cumulo).

### 6.2 Configurazione Database

**File di configurazione:** `sies.properties`

Configurare i seguenti parametri:
```properties
# Database Oracle
db.url=jdbc:oracle:thin:@[HOST]:[PORT]:[SID]
db.username=[USERNAME]
db.password=[PASSWORD]
db.driver=oracle.jdbc.OracleDriver
```

### 6.3 Configurazione Application Server

#### Per Tomcat:
1. Copiare il file `siesWeb.war` nella cartella `webapps` di Tomcat
2. Configurare il datasource in `context.xml`
3. Avviare Tomcat

#### Per JBoss:
1. Deployare l'applicazione tramite console amministrativa
2. Configurare il datasource nel file `standalone.xml`
3. Configurare le code JMS necessarie

### 6.4 Configurazione JMS

**File di configurazione:** `sies.properties`

```properties
# JMS Configuration
JMS_LOCAL_MITTENTE=[NOME_UFFICIO]
JMS_QUEUE_NAME=[NOME_CODA]
JMS_CONNECTION_FACTORY=[FACTORY_NAME]
```

### 6.5 Configurazione Logging

Il sistema utilizza Log4j 2. Configurare il file `log4j2.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Configuration status="WARN">
    <Appenders>
        <File name="File" fileName="logs/sies.log">
            <PatternLayout pattern="%d{yyyy-MM-dd HH:mm:ss} %-5p %c{1}:%L - %m%n"/>
        </File>
    </Appenders>
    <Loggers>
        <Root level="info">
            <AppenderRef ref="File"/>
        </Root>
    </Loggers>
</Configuration>
```

---

## 7. ACCESSO AL SISTEMA

### 7.1 Pagina di Login

Per accedere al sistema SIES:

1. Aprire il browser web
2. Digitare l'URL fornito dall'amministratore di sistema (es. `https://sies.giustizia.it/siesWeb/`)
3. Verrà visualizzata la pagina di login

### 7.2 Credenziali di Accesso

La pagina di login richiede:

- **Utente:** Username fornito dall'amministratore
- **Password:** Password personale

**Nota:** Le credenziali sono fornite dall'amministratore di sistema del proprio distretto.

### 7.3 Informazioni sulla Pagina di Login

Nella pagina di login sono visibili:
- **Server di:** Identificativo del server di appartenenza
- **Versione:** Versione corrente del software SIES
- **Comunicazioni di servizio:** Area dedicata a comunicazioni e avvisi importanti

### 7.4 Primo Accesso

Al primo accesso, il sistema potrebbe richiedere:
1. La modifica della password temporanea
2. L'accettazione delle policy di sicurezza
3. La configurazione di preferenze personali

### 7.5 Sicurezza

**Regole importanti:**
- Non condividere mai le proprie credenziali
- Utilizzare password complesse (minimo 8 caratteri, maiuscole, minuscole, numeri)
- Effettuare sempre il logout al termine della sessione
- Cambiare periodicamente la password

### 7.6 Problemi di Accesso

In caso di problemi:
- **Password dimenticata:** Contattare l'amministratore di sistema
- **Account bloccato:** Attendere 30 minuti o contattare l'amministratore
- **Errori tecnici:** Verificare connessione di rete e browser utilizzato

---

## 8. INTERFACCIA UTENTE

### 8.1 Struttura Generale

L'interfaccia di SIES è organizzata in diverse aree funzionali:

```
┌─────────────────────────────────────────────────────┐
│  HEADER - Logo e Informazioni Utente               │
├─────────────────────────────────────────────────────┤
│  MENU ORIZZONTALE - Pulsanti di Navigazione        │
├──────────┬──────────────────────────────────────────┤
│          │                                          │
│  MENU    │      AREA OPERATIVA                      │
│  VERTI-  │      (Contenuto Principale)              │
│  CALE    │                                          │
│          │                                          │
│          │                                          │
├──────────┴──────────────────────────────────────────┤
│  FOOTER - Informazioni di Sistema                  │
└─────────────────────────────────────────────────────┘
```

### 8.2 Area di Navigazione

#### 8.2.1 Menu Orizzontale

Il menu orizzontale è sempre presente e contiene i pulsanti principali:

| Pulsante | Funzione |
|----------|----------|
| ![Home](images/P_Home.jpg) **Home** | Ritorna alla pagina iniziale |
| ![Indietro](images/P_Indietro.jpg) **Indietro** | Ritorna alla pagina precedente |
| ![Stampa](images/P_Stampa.jpg) **Stampa** | Stampa la pagina corrente |
| ![Help](images/P_Help.jpg) **Help** | Visualizza l'aiuto contestuale |
| ![Logout](images/P_Logout.jpg) **Logout** | Esce dal sistema |

#### 8.2.2 Menu Verticale

Il menu verticale cambia in base al modulo e al profilo utente. Contiene le funzioni principali accessibili dall'utente per il modulo corrente.

**Caratteristiche:**
- Organizzato per categorie funzionali
- Icone intuitive per ogni funzione
- Accessibile da qualsiasi pagina

#### 8.2.3 Percorso Applicativo (Breadcrumb)

Nella parte superiore dell'area operativa viene visualizzato il percorso che l'utente ha effettuato:

```
Home > Titoli Esecutivi > Ricerca > Dettaglio
```

**Funzionalità:** Cliccando su una delle voci si può navigare rapidamente a quella sezione.

### 8.3 Area Operativa

#### 8.3.1 Descrizione

L'area operativa è la porzione centrale dell'interfaccia dove vengono visualizzati:
- Moduli di inserimento dati
- Risultati di ricerca
- Dettagli dei documenti
- Elenchi e tabelle

#### 8.3.2 Menu a Tendina

In molte funzioni sono presenti menu a tendina che permettono di:
- Selezionare valori da liste predefinite
- Filtrare risultati
- Scegliere opzioni specifiche

**Utilizzo:**
1. Cliccare sulla freccia del menu
2. Scorrere le opzioni disponibili
3. Cliccare sull'opzione desiderata

#### 8.3.3 Pulsanti di Uso Comune

| Pulsante | Funzione | Descrizione |
|----------|----------|-------------|
| **Cerca** | Esegue una ricerca | Avvia la ricerca con i criteri impostati |
| **Pulisci** | Cancella i campi | Azzera tutti i campi del form |
| **Salva** | Salva i dati | Memorizza le informazioni inserite |
| **Annulla** | Annulla l'operazione | Torna alla schermata precedente senza salvare |
| **Modifica** | Modifica record | Permette la modifica dei dati visualizzati |
| **Elimina** | Elimina record | Cancella il record selezionato |
| **Stampa** | Genera documento | Crea un documento stampabile |
| **Valida** | Valida documento | Conferma e valida il documento |

#### 8.3.4 Liste e Tabelle

Le liste di risultati presentano:
- **Intestazioni colonne:** Indicano il contenuto
- **Ordinamento:** Cliccando sull'intestazione si ordina la lista
- **Paginazione:** Navigazione tra le pagine di risultati
- **Selezione:** Checkbox per selezionare uno o più record
- **Azioni rapide:** Icone per operazioni dirette (visualizza, modifica, elimina)

### 8.4 Ricerca da Lista Predefinita

Molti campi presentano un pulsante ![Lente](images/P_Lente.jpg) che permette di:

1. Cliccare sul pulsante lente
2. Si apre una finestra popup con lista valori
3. Selezionare il valore desiderato
4. Il campo viene automaticamente popolato

**Vantaggi:**
- Riduce errori di digitazione
- Garantisce valori validi
- Velocizza l'inserimento

### 8.5 Validazione Campi

Il sistema effettua validazioni in tempo reale:

| Indicatore | Significato |
|------------|-------------|
| Campo con bordo **rosso** | Campo obbligatorio vuoto |
| Messaggio di **errore** | Formato non valido |
| Campo con bordo **verde** | Validazione corretta |
| **Asterisco (*)** | Campo obbligatorio |

### 8.6 Messaggi di Sistema

#### 8.6.1 Tipi di Messaggio

- **Informativo (ℹ️):** Conferma di operazione eseguita
- **Attenzione (⚠️):** Richiede attenzione dell'utente
- **Errore (❌):** Operazione non riuscita
- **Conferma (❓):** Richiede conferma prima di procedere

#### 8.6.2 Gestione Messaggi

- Leggere sempre attentamente i messaggi
- I messaggi di conferma richiedono una scelta (OK/Annulla)
- I messaggi informativi si chiudono automaticamente o con OK

---

## 9. MODULO SIEP - SISTEMA INFORMATIVO ESECUZIONE PENALE

### 9.1 Descrizione Modulo

Il modulo SIEP è destinato alle **Procure della Repubblica** per la gestione dell'attività di esecuzione penale.

### 9.2 Funzionalità Principali

#### 9.2.1 Gestione Titoli Esecutivi

**Funzioni disponibili:**

- **Iscrizione Titolo Esecutivo**
  - Inserimento nuovo titolo
  - Dati anagrafici condannato
  - Dati sentenza
  - Reati e pene

- **Ricerca Titolo Esecutivo**
  - Ricerca per numero registro
  - Ricerca per soggetto
  - Ricerca per reato
  - Ricerca avanzata

- **Gestione e Modifica**
  - Visualizzazione dettaglio
  - Modifica dati
  - Aggiornamento stato
  - Storico modifiche

#### 9.2.2 Gestione Soggetti

**Anagrafica Condannato:**
- Dati anagrafici completi
- Residenza/Domicilio
- Documenti identità
- Fotografia e impronte digitali
- Unificazione soggetti duplicati

**Difensori:**
- Anagrafica avvocato
- Associazione al condannato
- Storico difensori

#### 9.2.3 Gestione Reati

- **Inserimento reati**
  - Codice penale
  - Articoli
  - Circostanze aggravanti/attenuanti

- **Calcolo pena**
  - Pena detentiva
  - Pena pecuniaria
  - Pene accessorie

#### 9.2.4 Atti e Provvedimenti

**Tipi di atti gestiti:**
- Ordine di esecuzione
- Sospensione esecuzione
- Estinzione pena
- Revoca benefici
- Mandato di cattura

**Operazioni:**
- Redazione documento
- Validazione
- Trasmissione
- Stampa

#### 9.2.5 Comunicazioni

**Comunicazioni verso:**
- Uffici di Sorveglianza
- Casellario Giudiziale
- DAP (Dipartimento Amministrazione Penitenziaria)
- Altri Uffici Giudiziari

**Modalità:**
- Trasmissione telematica (JMS)
- Generazione documenti PDF
- Ricevuta di trasmissione

### 9.3 Menu Verticale SIEP

Il menu verticale del modulo SIEP presenta le seguenti voci principali:

```
📂 TITOLI ESECUTIVI
  ├─ Iscrizione
  ├─ Ricerca
  └─ Statistiche

📂 SOGGETTI
  ├─ Anagrafica
  ├─ Ricerca Soggetto
  └─ Unificazione Soggetti

📂 PROVVEDIMENTI
  ├─ Ordine Esecuzione
  ├─ Sospensione
  ├─ Estinzione
  └─ Revoca

📂 COMUNICAZIONI
  ├─ Trasmissione Atti
  ├─ Stato Trasmissioni
  └─ Messaggi Ricevuti

📂 STAMPE E REPORT
  ├─ Registro Esecuzione
  ├─ Statistiche
  └─ Report Personalizzati
```

### 9.4 Casi d'Uso Principali

#### 9.4.1 Iscrizione di un Nuovo Titolo Esecutivo

**Procedura:**

1. **Accesso alla funzione**
   - Menu Verticale > Titoli Esecutivi > Iscrizione

2. **Inserimento dati generali**
   - Numero registro generale
   - Data iscrizione
   - Tipo procedimento
   - Ufficio giudiziario

3. **Inserimento dati sentenza**
   - Autorità giudiziaria
   - Data sentenza
   - Numero sentenza
   - Data irrevocabilità

4. **Inserimento soggetto condannato**
   - Se già presente: ricerca e associazione
   - Se nuovo: inserimento anagrafica completa

5. **Inserimento reati e pene**
   - Reati contestati
   - Articoli di legge
   - Pena detentiva
   - Pena pecuniaria
   - Pene accessorie

6. **Salvataggio**
   - Verifica dati
   - Salvataggio definitivo
   - Stampa/Esportazione

#### 9.4.2 Ricerca e Consultazione Titolo Esecutivo

**Procedura:**

1. **Accesso alla funzione**
   - Menu Verticale > Titoli Esecutivi > Ricerca

2. **Impostazione criteri di ricerca**
   - Numero registro (es. 1234/2025)
   - Nome/Cognome condannato
   - Data nascita
   - Codice fiscale
   - Stato esecuzione

3. **Esecuzione ricerca**
   - Clic su pulsante "Cerca"
   - Visualizzazione lista risultati

4. **Visualizzazione dettaglio**
   - Selezione del titolo dalla lista
   - Apertura scheda dettaglio

5. **Operazioni disponibili**
   - Visualizzazione dati completi
   - Modifica (se permesso)
   - Stampa
   - Trasmissione

#### 9.4.3 Emissione Ordine di Esecuzione

**Procedura:**

1. **Selezione titolo esecutivo**
   - Ricerca e apertura del titolo

2. **Accesso funzione**
   - Menu > Provvedimenti > Ordine Esecuzione

3. **Compilazione ordine**
   - Dati automaticamente precompilati dal sistema
   - Verifica e integrazione informazioni
   - Motivazione (se necessaria)

4. **Generazione documento**
   - Anteprima documento
   - Correzioni eventuali
   - Generazione PDF

5. **Validazione**
   - Firma digitale (se configurata)
   - Validazione definitiva

6. **Trasmissione**
   - Selezione destinatari
   - Trasmissione telematica
   - Verifica ricevuta

---

## 10. MODULO SIUS - SISTEMA INFORMATIVO UFFICI SORVEGLIANZA

### 10.1 Descrizione Modulo

Il modulo SIUS è destinato ai **Tribunali e Uffici di Sorveglianza** per la gestione della sorveglianza e delle misure alternative alla detenzione.

### 10.2 Funzionalità Principali

#### 10.2.1 Presa in Carico Atti Pervenuti

**Funzioni:**
- Visualizzazione atti ricevuti
- Presa in carico
- Assegnazione a magistrato
- Cambio stato pratica

**Procedura:**
1. Menu > Presa in Carico Atti Pervenuti
2. Visualizzazione lista atti non ancora presi in carico
3. Selezione atto
4. Assegnazione magistrato relatore
5. Conferma presa in carico

#### 10.2.2 Gestione Procedimenti

**Procedimenti gestiti:**
- Misure alternative (affidamento sociale, detenzione domiciliare, semilibertà)
- Liberazione condizionale
- Riabilitazione
- Permessi premio
- Licenze
- Sospensione pena
- Rinvio esecuzione

**Operazioni:**
- Iscrizione procedimento
- Istruttoria
- Fissazione udienza
- Emissione provvedimento
- Comunicazione esito

#### 10.2.3 Gestione Udienze

**Funzionalità:**
- **Fissazione udienza**
  - Selezione data e ora
  - Assegnazione magistrato/collegio
  - Convocazione parti

- **Calendario udienze**
  - Vista giornaliera/settimanale/mensile
  - Filtri per magistrato
  - Filtri per tipo udienza

- **Verbale udienza**
  - Compilazione verbale
  - Registrazione presenze
  - Decisione
  - Dispositivo

- **Rinvio udienza**
  - Motivazione rinvio
  - Nuova data
  - Comunicazioni

#### 10.2.4 Emissione Provvedimenti

**Tipi di provvedimenti:**
- Ordinanza ammissione/rigetto misura alternativa
- Ordinanza concessione/revoca benefici
- Ordinanza sospensione/revoca misura
- Decreto
- Sentenza

**Processo:**
1. Selezione modello provvedimento
2. Compilazione automatica dati da pratica
3. Integrazione parte motivazionale
4. Generazione bozza
5. Revisione e correzioni
6. Validazione e firma
7. Deposito
8. Comunicazione alle parti

#### 10.2.5 Richieste e Comunicazioni

**Richieste verso enti esterni:**
- Richiesta relazione UEPE (Ufficio Esecuzione Penale Esterna)
- Richiesta casellario giudiziale
- Richiesta certificato DAP
- Richiesta residenza anagrafica
- Richiesta relazione sanitaria
- Richiesta relazione di sintesi
- Richiesta verifica condotta
- Richiesta stato esecuzione

**Gestione:**
- Compilazione richiesta
- Trasmissione telematica
- Tracking richiesta
- Ricezione risposta
- Archiviazione documentale

#### 10.2.6 Stato Esecuzione

**Monitoraggio:**
- Visualizzazione stato attuale esecuzione pena
- Calcolo pena residua
- Detrazioni
- Benefici in corso
- Cronologia eventi

**Informazioni disponibili:**
- Data inizio esecuzione
- Data fine pena teorica
- Data fine pena con benefici
- Giorni scontati
- Giorni residui
- Periodi di detenzione
- Periodi in misura alternativa

### 10.3 Menu Verticale SIUS

```
📂 GESTIONE ATTI
  ├─ Presa in Carico Atti Pervenuti
  ├─ Ricerca Procedimento
  └─ Statistiche Atti

📂 PROCEDIMENTI
  ├─ Iscrizione Procedimento
  ├─ Affidamento in Prova al Servizio Sociale
  ├─ Detenzione Domiciliare
  ├─ Semilibertà
  ├─ Liberazione Condizionale
  ├─ Riabilitazione
  └─ Altri Procedimenti

📂 UDIENZE
  ├─ Fissazione Udienza
  ├─ Calendario Udienze
  ├─ Verbale Udienza
  └─ Rinvio Udienza

📂 PROVVEDIMENTI
  ├─ Ordinanza
  ├─ Decreto
  ├─ Sentenza
  └─ Ricerca Provvedimenti

📂 RICHIESTE
  ├─ Richiesta Relazione UEPE
  ├─ Richiesta Casellario
  ├─ Richiesta Stato Esecuzione
  ├─ Altre Richieste
  └─ Stato Richieste

📂 STATO ESECUZIONE
  ├─ Visualizza Stato Esecuzione
  ├─ Calcolo Pena
  └─ Cronologia Eventi

📂 SOGGETTI
  ├─ Anagrafica
  ├─ Ricerca Soggetto
  ├─ Unificazione Soggetti
  └─ Sostituzione Difensore

📂 STAMPE E DOCUMENTI
  ├─ Registro Sorveglianza
  ├─ Statistiche
  └─ Modelli Documenti
```

### 10.4 Casi d'Uso Principali

#### 10.4.1 Gestione Istanza di Affidamento in Prova

**Scenario:** Un detenuto presenta istanza per affidamento in prova al servizio sociale.

**Procedura completa:**

1. **Ricezione e Presa in Carico**
   - Atto pervenuto appare in "Presa in Carico Atti Pervenuti"
   - Cancelliere prende in carico l'atto
   - Assegnazione a magistrato relatore

2. **Iscrizione Procedimento**
   - Menu > Procedimenti > Affidamento in Prova
   - Inserimento numero registro
   - Associazione al titolo esecutivo
   - Inserimento data istanza

3. **Richieste Istruttorie**
   - Menu > Richieste > Richiesta Relazione UEPE
     - Compilazione richiesta
     - Trasmissione a UEPE competente
   - Menu > Richieste > Richiesta Casellario
   - Menu > Richieste > Richiesta Stato Esecuzione

4. **Fissazione Udienza**
   - Menu > Udienze > Fissazione Udienza
   - Selezione data disponibile
   - Assegnazione magistrato (se monocratico) o collegio
   - Generazione convocazioni automatiche:
     - Convocazione interessato
     - Avviso al difensore
     - Avviso al P.M.
     - Avviso al DAP (se detenuto)

5. **Udienza**
   - Menu > Udienze > Verbale Udienza
   - Registrazione presenze
   - Inserimento dichiarazioni
   - Decisione:
     - Ammissione
     - Rigetto
     - Rinvio

6. **Emissione Ordinanza**
   - Menu > Provvedimenti > Ordinanza
   - Selezione tipo: "Affidamento in Prova"
   - Sistema precompila i dati
   - Inserimento motivazione
   - Generazione documento
   - Validazione

7. **Comunicazioni**
   - Sistema genera automaticamente:
     - Comunicazione all'interessato
     - Comunicazione al difensore
     - Comunicazione al P.M.
     - Comunicazione UEPE (se ammesso)
     - Comunicazione DAP (se detenuto)
   - Trasmissione telematica
   - Verifica ricevute

8. **Monitoraggio**
   - Menu > Stato Esecuzione
   - Visualizzazione misura in corso
   - Aggiornamenti periodici da UEPE

#### 10.4.2 Fissazione e Gestione Udienza

**Procedura:**

1. **Accesso al Calendario**
   - Menu > Udienze > Calendario Udienze
   - Visualizzazione agenda magistrato/collegio

2. **Fissazione Nuova Udienza**
   - Menu > Udienze > Fissazione Udienza
   - Selezione fascicolo/procedimento
   - Verifica disponibilità aula
   - Selezione data e ora
   - Conferma

3. **Preparazione Udienza**
   - Verifica documentazione istruttoria
   - Verifiche relazioni pervenute
   - Controllo convocazioni inviate

4. **Giorno dell'Udienza**
   - Menu > Udienze > Verbale Udienza
   - Selezione udienza dal calendario
   - Apertura maschera verbale

5. **Compilazione Verbale**
   - Dati automatici:
     - Data, ora, luogo
     - Magistrato/Collegio
     - Cancelliere
   - Registrazione presenze:
     - Interessato (presente/assente)
     - Difensore (presente/assente/rinuncia)
     - P.M. (presente/assente)
   - Inserimento dichiarazioni
   - Decisione:
     - Ammissione/Rigetto
     - Rinvio (con nuova data)
     - Dispositivo
   - Firma digitale

6. **Post-Udienza**
   - Generazione automatica provvedimento
   - Comunicazioni parti
   - Aggiornamento calendario
   - Archiviazione documentale

#### 10.4.3 Richiesta Relazione UEPE

**Procedura:**

1. **Accesso alla Funzione**
   - Menu > Richieste > Richiesta Relazione UEPE

2. **Selezione Procedimento**
   - Ricerca fascicolo
   - Selezione soggetto

3. **Compilazione Richiesta**
   - Tipo relazione:
     - Relazione sociale
     - Relazione di sintesi
     - Relazione finale
     - Aggiornamento relazione
   - Termine per invio (giorni)
   - Note e richieste specifiche

4. **Identificazione UEPE Competente**
   - Sistema identifica automaticamente UEPE competente per territorio
   - Possibilità di modifica manuale

5. **Trasmissione**
   - Generazione documento richiesta
   - Trasmissione telematica via JMS
   - Protocollo automatico

6. **Monitoraggio**
   - Menu > Richieste > Stato Richieste
   - Visualizzazione richieste pendenti
   - Sollecito automatico se scaduti termini
   - Verifica ricezione risposta

7. **Ricezione Relazione**
   - Notifica automatica a ricezione
   - Associazione automatica al fascicolo
   - Disponibilità per consultazione

---

## 11. MODULO AMMINISTRAZIONE

### 11.1 Descrizione Modulo

Il modulo Amministrazione è riservato agli **amministratori di sistema** per la configurazione e gestione del sistema SIES.

### 11.2 Accesso al Modulo

**Requisiti:**
- Profilo utente "Amministratore"
- Credenziali specifiche di amministrazione

### 11.3 Funzionalità Principali

#### 11.3.1 Gestione Utenti

**Operazioni disponibili:**

- **Inserimento Nuovo Utente**
  - Dati anagrafici
  - Username
  - Password iniziale (temporanea)
  - Email
  - Ufficio di appartenenza
  - Data scadenza account

- **Ricerca Utenti**
  - Per cognome/nome
  - Per username
  - Per ufficio
  - Per stato (attivo/disabilitato)

- **Modifica Utente**
  - Aggiornamento dati anagrafici
  - Cambio ufficio
  - Reset password
  - Disabilitazione/Abilitazione account

- **Eliminazione Utente**
  - Disabilitazione logica (non cancellazione fisica)
  - Mantenimento storico attività

**Procedura Inserimento Nuovo Utente:**

1. Menu > Gestione Utenti > Inserisci Utente
2. Compilazione form:
   - Cognome *
   - Nome *
   - Codice Fiscale *
   - Username * (univoco)
   - Email *
   - Ufficio * (da lista)
3. Assegnazione profili (vedi sezione successiva)
4. Salvataggio
5. Sistema genera password temporanea
6. Invio credenziali all'utente

#### 11.3.2 Gestione Profili

I profili definiscono i permessi e le funzionalità accessibili agli utenti.

**Profili Predefiniti:**

| Profilo | Descrizione | Moduli Accessibili |
|---------|-------------|-------------------|
| **Amministratore Distrettuale** | Accesso completo amministrazione | AMM, SIEP, SIUS |
| **Amministratore Locale** | Amministrazione locale ufficio | AMM (limitato), SIEP o SIUS |
| **Magistrato EP** | Magistrato Procura | SIEP |
| **Cancelliere EP** | Cancelliere Procura | SIEP (limitato) |
| **Magistrato US** | Magistrato Ufficio Sorveglianza | SIUS |
| **Cancelliere US** | Cancelliere Ufficio Sorveglianza | SIUS (limitato) |
| **Operatore UEPE** | Operatore servizi sociali | SIUS (consultazione) |
| **Consultazione** | Solo lettura | SIEP o SIUS (sola lettura) |

**Operazioni sui Profili:**

- **Visualizzazione Profili**
  - Lista profili esistenti
  - Dettaglio permessi per profilo

- **Creazione Nuovo Profilo**
  - Nome e descrizione profilo
  - Selezione moduli accessibili
  - Selezione funzioni specifiche per modulo
  - Permessi (lettura, scrittura, cancellazione, validazione)

- **Modifica Profilo**
  - Aggiunta/Rimozione permessi
  - Modifica configurazione

- **Associazione Profili a Utenti**
  - Un utente può avere più profili
  - Selezione profilo attivo al login

#### 11.3.3 Gestione Uffici

**Anagrafica Uffici:**

- **Inserimento Ufficio**
  - Codice ufficio (univoco)
  - Denominazione
  - Tipo ufficio:
    - Procura della Repubblica
    - Tribunale di Sorveglianza
    - Ufficio di Sorveglianza
    - UEPE
    - Altro
  - Distretto di appartenenza
  - Indirizzo completo
  - Telefono/Fax
  - Email/PEC
  - Codice IPA

- **Configurazione Ufficio**
  - Moduli abilitati
  - Parametri specifici
  - Modelli documenti
  - Numerazione registri

- **Periodi Feriali**
  - Inserimento periodi di chiusura ufficio
  - Date inizio/fine
  - Descrizione
  - Impatto su termini processuali

#### 11.3.4 Gestione Cancellerie

Per uffici con più cancellerie:

- **Inserimento Cancelleria**
  - Codice identificativo
  - Denominazione
  - Materia di competenza
  - Magistrati assegnati

- **Modifica Cancelleria**
  - Aggiornamento dati
  - Riassegnazione magistrati

#### 11.3.5 Gestione Posizioni Materiali

Per la gestione della collocazione fisica dei fascicoli:

- **Inserimento Posizione**
  - Codice posizione
  - Descrizione (es. Armadio 5, Scaffale 3)
  - Capienza
  - Ufficio

- **Assegnazione Fascicoli**
  - Associazione fascicolo a posizione
  - Storico movimenti

#### 11.3.6 Decodifiche e Tabelle

Gestione delle tabelle di decodifica utilizzate dal sistema:

**Tabelle principali:**
- Reati (codice penale)
- Circostanze
- Tipi provvedimento
- Stati procedimento
- Modalità notifica
- Esiti udienze
- Motivi rinvio
- Enti esterni

**Operazioni:**
- Visualizzazione tabelle
- Inserimento nuovi valori
- Modifica valori esistenti
- Disabilitazione valori obsoleti

#### 11.3.7 Log Attività

**Monitoraggio Sistema:**

- **Visualizzazione Log**
  - Filtri per:
    - Data/periodo
    - Utente
    - Tipo operazione
    - Modulo
  - Esportazione log

- **Informazioni Registrate**
  - Data e ora operazione
  - Utente
  - IP origine
  - Operazione eseguita
  - Dati modificati (prima/dopo)
  - Esito operazione

#### 11.3.8 Statistiche e Report

**Report Disponibili:**

- Numero utenti attivi per ufficio
- Distribuzione utenti per profilo
- Attività utenti (accessi, operazioni)
- Procedimenti per ufficio
- Tempi medi procedimenti
- Udienze per magistrato
- Provvedimenti emessi

**Esportazione:**
- Formato Excel
- Formato PDF
- Formato CSV

### 11.4 Menu Verticale Amministrazione

```
📂 GESTIONE UTENTI
  ├─ Inserimento Utente
  ├─ Ricerca Utente
  ├─ Modifica Utente
  └─ Reset Password

📂 GESTIONE PROFILI
  ├─ Lista Profili
  ├─ Inserimento Profilo
  ├─ Modifica Profilo
  └─ Associazione Profili a Utenti

📂 GESTIONE UFFICI
  ├─ Inserimento Ufficio
  ├─ Ricerca Ufficio
  ├─ Modifica Ufficio
  ├─ Gestione Cancellerie
  └─ Periodi Feriali

📂 GESTIONE POSIZIONI MATERIALI
  ├─ Inserimento Posizione
  ├─ Ricerca Posizione
  └─ Assegnazione Fascicoli

📂 DECODIFICHE
  ├─ Reati
  ├─ Circostanze
  ├─ Tipi Provvedimento
  ├─ Stati Procedimento
  └─ Altre Tabelle

📂 LOG E AUDIT
  ├─ Visualizza Log Attività
  ├─ Ricerca Log
  └─ Esportazione Log

📂 STATISTICHE
  ├─ Statistiche Utenti
  ├─ Statistiche Procedimenti
  └─ Report Personalizzati

📂 CONFIGURAZIONE SISTEMA
  ├─ Parametri Generali
  ├─ Configurazione JMS
  └─ Backup e Manutenzione
```

### 11.5 Casi d'Uso Amministrativi

#### 11.5.1 Creazione Nuovo Utente Completa

**Scenario:** Nuovo cancelliere assunto presso Tribunale di Sorveglianza

**Procedura:**

1. **Login come Amministratore**

2. **Verifica Ufficio**
   - Menu > Gestione Uffici > Ricerca Ufficio
   - Verifica esistenza ufficio di destinazione
   - Se non esiste: creazione ufficio

3. **Creazione Utente**
   - Menu > Gestione Utenti > Inserimento Utente
   - Compilazione dati:
     - Cognome: Rossi
     - Nome: Mario
     - CF: RSSMRA80A01H501Z
     - Username: m.rossi
     - Email: mario.rossi@giustizia.it
     - Ufficio: Tribunale Sorveglianza Roma

4. **Assegnazione Profilo**
   - Selezione profilo: "Cancelliere US"
   - Conferma

5. **Salvataggio**
   - Sistema genera password temporanea: Temp2026!

6. **Comunicazione Credenziali**
   - Email automatica all'utente con:
     - Username
     - Password temporanea
     - Link accesso sistema
     - Istruzioni primo accesso

7. **Verifica**
   - Menu > Gestione Utenti > Ricerca Utente
   - Verifica utente creato correttamente
   - Verifica profilo assegnato

8. **Follow-up**
   - Monitoraggio primo accesso
   - Verifica cambio password

#### 11.5.2 Reset Password Utente

**Scenario:** Utente ha dimenticato la password

**Procedura:**

1. **Ricerca Utente**
   - Menu > Gestione Utenti > Ricerca Utente
   - Criteri ricerca (es. Username: "m.rossi")
   - Visualizzazione dettaglio utente

2. **Reset Password**
   - Pulsante "Reset Password"
   - Conferma operazione
   - Sistema genera nuova password temporanea

3. **Comunicazione**
   - Email automatica all'utente
   - Oppure: comunicazione telefonica/verbale

4. **Registrazione Log**
   - Sistema registra automaticamente:
     - Data/ora reset
     - Amministratore che ha effettuato reset
     - Username interessato

---

## 12. FUNZIONALITÀ COMUNI

### 12.1 Ricerca Soggetti

La ricerca soggetti è una funzionalità trasversale accessibile da SIEP e SIUS.

**Modalità di Ricerca:**

#### 12.1.1 Ricerca Anagrafica Semplice

**Criteri:**
- Cognome
- Nome
- Data di nascita
- Luogo di nascita

**Procedura:**
1. Menu > Soggetti > Ricerca Soggetto
2. Inserire almeno cognome e nome
3. Click su "Cerca"
4. Visualizzazione lista risultati
5. Selezione soggetto per dettaglio

#### 12.1.2 Ricerca Avanzata

**Criteri aggiuntivi:**
- Codice fiscale
- Sesso
- Cittadinanza
- Documento identità
- Indirizzo/Residenza
- Numero registro
- Stato (detenuto, libero, ricercato)

#### 12.1.3 Ricerca Fonetica

Per gestire variazioni nell'ortografia dei nomi:
- Sistema cerca somiglianze fonetiche
- Utile per nomi stranieri
- Suggerimenti automatici

### 12.2 Unificazione Soggetti

Quando esistono duplicazioni anagrafiche dello stesso soggetto.

**Procedura:**

1. **Identificazione Duplicati**
   - Menu > Soggetti > Ricerca Soggetto
   - Sistema segnala eventuali soggetti simili

2. **Accesso Funzione**
   - Menu > Soggetti > Unificazione Soggetti

3. **Selezione Soggetti**
   - Soggetto principale (da mantenere)
   - Soggetti da unificare (da eliminare)

4. **Verifica Dati**
   - Confronto dati anagrafici
   - Integrazione informazioni mancanti

5. **Unificazione**
   - Sistema unifica:
     - Tutti i titoli esecutivi
     - Tutti i procedimenti
     - Tutte le comunicazioni
     - Tutto lo storico
   - Soggetti duplicati vengono disattivati

6. **Conferma**
   - Verifica finale
   - Conferma unificazione
   - Operazione irreversibile

### 12.3 Gestione Documenti

#### 12.3.1 Tipi di Documento

Il sistema gestisce:
- Documenti generati (ordinanze, decreti, verbali)
- Documenti acquisiti (istanze, relazioni, certificati)
- Allegati (documentazione varia)

#### 12.3.2 Upload Documenti

**Procedura:**

1. Accesso alla scheda fascicolo/procedimento
2. Sezione "Documenti"
3. Pulsante "Carica Documento"
4. Selezione file (formato supportato)
5. Tipo documento (da menù a tendina)
6. Data documento
7. Descrizione/Note
8. Upload
9. Conferma caricamento

**Formati supportati:**
- PDF (preferito)
- DOC/DOCX
- XLS/XLSX
- Immagini (JPG, PNG)
- File firmati digitalmente (P7M)

**Limiti:**
- Dimensione massima file: 10 MB
- Numero massimo allegati: 50 per fascicolo

#### 12.3.3 Consultazione Documenti

- Lista documenti in fascicolo
- Ordinamento per data/tipo
- Visualizzazione online (PDF)
- Download documento
- Stampa

#### 12.3.4 Firma Digitale

Se configurata:
1. Selezione documento da firmare
2. Pulsante "Firma Digitale"
3. Autenticazione con token/smart card
4. Apposizione firma
5. Documento firmato sostituisce originale

### 12.4 Stampe e Report

#### 12.4.1 Stampa Documenti Singoli

**Da qualsiasi schermata di dettaglio:**
1. Pulsante "Stampa" o icona stampante
2. Anteprima PDF
3. Opzioni:
   - Stampa fisica (su stampante)
   - Salvataggio PDF
   - Invio email

#### 12.4.2 Stampe Registro

**SIEP - Registro Esecuzione:**
- Menu > Stampe e Report > Registro Esecuzione
- Filtri:
  - Periodo (da data - a data)
  - Stato esecuzione
  - Magistrato
- Formato: PDF, Excel

**SIUS - Registro Sorveglianza:**
- Menu > Stampe e Report > Registro Sorveglianza
- Filtri:
  - Periodo
  - Tipo procedimento
  - Magistrato/Collegio
- Formato: PDF, Excel

#### 12.4.3 Report Statistici

**Disponibili:**
- Numero procedimenti per periodo
- Tempi medi di definizione
- Esiti procedimenti
- Udienze per magistrato
- Provvedimenti emessi

**Generazione Report:**
1. Menu > Stampe e Report > Report Statistici
2. Selezione tipo report
3. Impostazione parametri (date, filtri)
4. Generazione
5. Visualizzazione/Download

#### 12.4.4 Esportazione Dati

**Per analisi esterne:**
- Formato Excel (XLS/XLSX)
- Formato CSV
- Formato PDF

**Procedura:**
1. Eseguire ricerca/filtro desiderato
2. Pulsante "Esporta"
3. Selezione formato
4. Download file

### 12.5 Cambio Password

**Procedura:**

1. Click su nome utente (in alto a destra)
2. Menù a tendina > "Cambia Password"
3. Form cambio password:
   - Password attuale
   - Nuova password
   - Conferma nuova password
4. Requisiti password:
   - Minimo 8 caratteri
   - Almeno una maiuscola
   - Almeno una minuscola
   - Almeno un numero
   - Almeno un carattere speciale
5. Conferma
6. Messaggio di successo
7. Logout automatico
8. Re-login con nuova password

**Note:**
- Password deve essere cambiata ogni 90 giorni
- Non riutilizzare ultime 5 password
- Dopo 3 tentativi errati, account bloccato per 30 minuti

---

## 13. INTEGRAZIONE CON SISTEMI ESTERNI

### 13.1 Sistemi Integrati

SIES si integra con diversi sistemi esterni del dominio giustizia:

#### 13.1.1 Casellario Giudiziale Nazionale

**Funzionalità:**
- Richiesta certificato penale
- Richiesta carichi pendenti
- Invio informazioni su nuove condanne
- Ricezione aggiornamenti

**Modalità:**
- Comunicazione telematica automatica
- Web service
- Tracciabilità richieste

#### 13.1.2 DAP - Dipartimento Amministrazione Penitenziaria

**Funzionalità:**
- Richiesta stato detenzione
- Invio ordini di carcerazione
- Ricezione informazioni detenuti
- Comunicazione provvedimenti

**Sistema Esecuzione (modulo siesEsecuzione):**
- Trasferimento fogli complementari
- Gestione cumulo pene
- Comunicazione verso NSC (Nuovo Sistema Casellario)

#### 13.1.3 UEPE - Uffici Esecuzione Penale Esterna

**Funzionalità:**
- Richiesta relazioni sociali
- Invio provvedimenti di affidamento
- Ricezione aggiornamenti su misure alternative
- Comunicazione violazioni

#### 13.1.4 Altri Uffici Giudiziari

**Comunicazioni inter-distrettuali:**
- Trasferimento competenza
- Richieste informazioni
- Invio copie atti
- Deleghe

### 13.2 Tecnologie di Integrazione

#### 13.2.1 JMS - Java Message Service

**Utilizzo:**
- Code messaggi per comunicazioni asincrone
- Garanzia consegna messaggio
- Tracciabilità completa

**Configurazione:**
```
JMS_LOCAL_MITTENTE: Identificativo ufficio mittente
JMS_QUEUE_NAME: Nome coda messaggi
JMS_CONNECTION_FACTORY: Factory di connessione
```

#### 13.2.2 Web Services SOAP

**Servizi esposti:**
- Interrogazione titoli esecutivi
- Interrogazione procedimenti
- Ricezione atti

**WSDL disponibili:**
- esecuzione_NEW.wsdl
- trasferisciFoglioComplementare.wsdl

#### 13.2.3 Formati Dati

**XML Schema:**
- ProvvedimentoEsecuzione_NEW.xsd
- FoglioComplementare.xsd
- FoglioComplementare.xsd_CUMULO

### 13.3 Monitoraggio Comunicazioni

**Menu > Comunicazioni > Stato Trasmissioni**

Visualizzazione:
- Data/ora invio
- Destinatario
- Tipo messaggio
- Stato:
  - ✓ Inviato
  - ⏳ In attesa
  - ❌ Errore
  - ✓✓ Ricevuta consegna
- Possibilità ri-invio in caso errore

---

## 14. GLOSSARIO

### Termini Giuridici

- **Affidamento in prova ai servizi sociali:** Misura alternativa alla detenzione che prevede lo svolgimento di attività rieducative con controllo dei servizi sociali.

- **Casellario Giudiziale:** Registro nazionale che raccoglie informazioni su sentenze penali, provvedimenti e carichi pendenti.

- **Condanna:** Provvedimento con cui il giudice dichiara l'imputato colpevole e determina la pena.

- **DAP:** Dipartimento dell'Amministrazione Penitenziaria, gestisce gli istituti penitenziari italiani.

- **Detenzione domiciliare:** Misura alternativa che permette di scontare la pena presso la propria abitazione.

- **Esecuzione penale:** Fase del processo penale in cui vengono attuate le pene inflitte con sentenza definitiva.

- **Foglio complementare:** Documento che contiene informazioni aggiuntive sul titolo esecutivo.

- **Liberazione condizionale:** Beneficio che consente la scarcerazione anticipata del condannato.

- **Misura alternativa:** Modalità di esecuzione della pena diversa dalla detenzione in carcere.

- **Ordine di esecuzione:** Provvedimento con cui il P.M. dispone l'esecuzione di una sentenza penale.

- **Provvedimento:** Atto giudiziario (ordinanza, decreto, sentenza).

- **Riabilitazione:** Beneficio che estingue le pene accessorie e gli effetti penali della condanna.

- **Semilibertà:** Misura alternativa che permette di trascorrere parte della giornata fuori dal carcere.

- **Sospensione dell'esecuzione:** Rinvio dell'inizio dell'esecuzione della pena per determinati motivi.

- **Titolo esecutivo:** Sentenza penale definitiva che costituisce titolo per l'esecuzione della pena.

- **UEPE:** Ufficio di Esecuzione Penale Esterna, struttura del Ministero della Giustizia che segue le misure alternative.

- **Ufficio di Sorveglianza:** Organo giurisdizionale che vigila sull'esecuzione delle pene e decide su misure alternative.

### Termini Tecnici

- **Action:** Classe Java che gestisce le richieste HTTP e implementa la logica applicativa.

- **BDI:** Banca Dati Integrata, database centralizzato distrettuale.

- **Controller:** Componente che gestisce la logica di business dell'applicazione.

- **DAO (Data Access Object):** Pattern di programmazione per l'accesso ai dati del database.

- **Distretto:** Ambito territoriale di competenza di una Corte d'Appello.

- **JMS (Java Message Service):** Tecnologia per lo scambio di messaggi tra applicazioni.

- **JSP (Java Server Pages):** Tecnologia per la creazione di pagine web dinamiche.

- **Maven:** Strumento di gestione del ciclo di vita del software e gestione dipendenze.

- **MyBatis:** Framework per la mappatura oggetti-relazionali.

- **POM (Project Object Model):** File XML di configurazione Maven.

- **Registry/Registro:** Numerazione progressiva dei procedimenti.

- **SOAP:** Protocollo per lo scambio di messaggi tra web services.

- **VO (Value Object):** Oggetto Java che rappresenta i dati.

- **Web Service:** Servizio software accessibile via rete tramite protocolli standard.

- **WSDL (Web Services Description Language):** Linguaggio XML per descrivere web services.

- **XSD (XML Schema Definition):** Definizione della struttura di un documento XML.

---

## 15. SUPPORTO E CONTATTI

### 15.1 Help Online

**Aiuto Contestuale:**
- Pulsante "?" presente in ogni pagina
- Help specifico per la funzione corrente
- Esempi pratici

**Documentazione:**
- Manuali in formato PDF
- Guide operative
- Tutorial video (se disponibili)

### 15.2 Assistenza Tecnica

#### Livello 1 - Assistenza Locale

**Amministratore Locale Ufficio:**
- Problemi di accesso
- Reset password
- Configurazioni utente
- Problemi comuni

#### Livello 2 - Assistenza Distrettuale

**Amministratore Distrettuale:**
- Problemi configurazione
- Errori applicativi
- Gestione profili
- Problemi integrazione

#### Livello 3 - Assistenza Nazionale

**Help Desk Centrale:**
- Problemi sistemistici
- Bug applicativi
- Richieste evolutive
- Assistenza specialistica

### 15.3 Segnalazione Problemi

**Procedura:**

1. **Identificare il Problema**
   - Cosa si stava facendo
   - Errore visualizzato
   - Screenshot (se possibile)

2. **Verificare:**
   - Problema già noto?
   - Altri utenti hanno stesso problema?
   - Consultare FAQ

3. **Segnalare:**
   - Contattare amministratore locale
   - Fornire:
     - Descrizione dettagliata
     - Passi per riprodurre errore
     - Screenshot
     - Data/ora
     - Username (senza password!)

4. **Follow-up:**
   - Annotare numero ticket
   - Verificare risoluzione
   - Feedback su soluzione

### 15.4 Richieste di Modifica/Evoluzione

**Per funzionalità aggiuntive:**

1. Descrivere esigenza
2. Motivazione
3. Benefici attesi
4. Proposta tramite amministratore distrettuale
5. Valutazione a livello centrale
6. Eventuale pianificazione in release future

### 15.5 Formazione

**Corsi disponibili:**
- Corso base utilizzo SIES
- Corso avanzato per operatori
- Corso amministratori
- Webinar di aggiornamento

**Richiesta formazione:**
- Tramite amministratore distrettuale
- Organizzazione corsi locali
- Formazione on-the-job

### 15.6 Aggiornamenti Sistema

**Rilasci:**
- Release maggiori: 2 volte l'anno
- Patch correttive: quando necessario
- Comunicazione anticipata
- Finestre di manutenzione programmate

**Cosa fare:**
- Leggere note di rilascio
- Partecipare a sessioni informative
- Testare nuove funzionalità
- Segnalare eventuali anomalie

### 15.7 Best Practices

**Utilizzo Ottimale del Sistema:**

1. **Accesso:**
   - Logout sempre al termine
   - Non lasciare sessione incustodita
   - Cambio password periodico

2. **Inserimento Dati:**
   - Accuratezza dati anagrafici
   - Verifica dati prima di salvare
   - Utilizzo decodifiche corrette

3. **Ricerche:**
   - Utilizzare criteri specifici
   - Evitare ricerche troppo ampie
   - Salvare ricerche frequenti

4. **Documenti:**
   - Formato PDF preferito
   - Denominazione chiara file
   - Verificare dimensioni

5. **Comunicazioni:**
   - Verificare destinatari
   - Controllare ricevute
   - Solleciti se necessario

6. **Backup Locale:**
   - Esportare periodicamente dati critici
   - Stampa/salvataggio documenti importanti
   - Non sostituisce backup di sistema

### 15.8 FAQ - Domande Frequenti

**D: Ho dimenticato la password, cosa faccio?**  
R: Contatta l'amministratore locale che effettuerà il reset. Riceverai una password temporanea via email.

**D: Il sistema è lento, perché?**  
R: Possibili cause: connessione di rete lenta, troppe applicazioni aperte, manutenzione in corso. Verifica connessione e chiudi applicazioni non necessarie. Se persiste, contatta assistenza.

**D: Posso accedere da casa?**  
R: Solo se configurato VPN. Verificare con amministratore locale.

**D: Posso delegare il mio accesso a un collega?**  
R: No, le credenziali sono personali e non cedibili. Il collega deve avere un proprio account.

**D: Quanto tempo restano i dati nel sistema?**  
R: I dati sono conservati permanentemente per esigenze storico-giuridiche.

**D: Posso modificare un dato inserito tempo fa?**  
R: Dipende dai permessi del profilo e dallo stato del procedimento. Alcune modifiche potrebbero essere bloccate o richiedere autorizzazioni.

**D: Come recupero un documento cancellato per errore?**  
R: Contattare immediatamente assistenza tecnica. Alcuni documenti potrebbero essere recuperabili da backup.

**D: Il sistema mi dà un errore, cosa faccio?**  
R: Fare screenshot dell'errore, annotare cosa si stava facendo, contattare assistenza fornendo questi dettagli.

---

## APPENDICI

### Appendice A - Codici Errore Comuni

| Codice | Descrizione | Soluzione |
|--------|-------------|-----------|
| ERR-001 | Sessione scaduta | Effettuare nuovamente login |
| ERR-002 | Permessi insufficienti | Verificare profilo assegnato |
| ERR-003 | Dati obbligatori mancanti | Compilare tutti i campi con asterisco (*) |
| ERR-004 | Formato dati non valido | Verificare formato (es. data gg/mm/aaaa) |
| ERR-005 | Record già esistente | Verificare duplicati |
| ERR-006 | Errore database | Contattare assistenza |
| ERR-JMS-001 | Errore trasmissione JMS | Verificare connessione, riprovare |

### Appendice B - Tasti Rapidi da Tastiera

| Combinazione | Funzione |
|--------------|----------|
| Ctrl + S | Salva |
| Ctrl + P | Stampa |
| Ctrl + F | Cerca |
| Esc | Annulla/Chiudi |
| F1 | Help contestuale |

### Appendice C - Formati Data e Ora

**Formato Data:** gg/mm/aaaa (es. 24/02/2026)  
**Formato Ora:** hh:mm (es. 14:30)  
**Formato Data/Ora completo:** gg/mm/aaaa hh:mm

### Appendice D - Riferimenti Normativi

- Codice di Procedura Penale (art. 655 e seguenti - Esecuzione)
- Legge 26 luglio 1975, n. 354 (Ordinamento penitenziario)
- D.P.R. 30 giugno 2000, n. 230 (Regolamento esecuzione O.P.)
- Codice dell'Amministrazione Digitale (CAD)

---

## CRONOLOGIA VERSIONI

| Versione | Data | Descrizione Modifiche |
|----------|------|----------------------|
| 12.8.5.0 | Gen 2026 | Upgrade tecnologico Visual Studio Code, Java 21 |
| 12.8.3.0 | Lug 2025 | Gestione trasferimento fogli complementari NSC |
| 12.8.2.0 | 2025 | Versione precedente |

---

## NOTE FINALI

Questo manuale è soggetto a modifiche e aggiornamenti in base all'evoluzione del sistema SIES. Gli utenti saranno informati tempestivamente di eventuali modifiche sostanziali.

Per segnalazioni di errori o suggerimenti per il miglioramento di questo manuale, contattare l'amministratore distrettuale.

---

**Documento:** MANUALE_UTENTE_SIES.md  
**Versione Manuale:** 1.0  
**Data Pubblicazione:** Febbraio 2026  
**Redatto per:** Sistema SIES - Ministero della Giustizia Italiano