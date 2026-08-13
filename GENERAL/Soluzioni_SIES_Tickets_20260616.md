---
uniqueName: soluzionisiestickets20260616
displayName: "Soluzioni SIES Tickets 20260616"
category: "GENERAL"
tags: []
---


Documento generato il 16/06/2026 11:40

# 1. Ticket #20260616013 -- Eliminazione presofferto

Creato il 16/06/2026 -- Stato: In attesa di informazioni Assistenza

## 1.1 Intestazione ticket

  -----------------------------------------------------------------------
  **Campo**                           **Valore**
  ----------------------------------- -----------------------------------
  **Numero ticket**                   20260616013

  **Titolo**                          Eliminazione presofferto

  **Stato**                           In attesa di informazioni
                                      Assistenza

  **Priorità**                        2 Low

  **Tipo**                            06 - COT - Consulenza tecnica

  **Coda**                            Desk-RTI

  **Cliente**                         UTA / silvia.zappalorti

  **Fascicolo SIEP**                  2026/320 -- Conti Angelo

  **Creato il**                       16/06/2026 07:54
  -----------------------------------------------------------------------

## 1.2 Descrizione del problema

La Procura di Milano (tramite il Direttore Ufficio Esecuzioni Penale,
Giuseppe Marotta) segnala con urgenza che nel fascicolo SIEP 2026/320
(Conti Angelo) è stato erroneamente inserito due volte lo stesso periodo
di presofferto. Si richiede l\'eliminazione dell\'inserimento duplicato.

## 1.3 Soluzioni simili trovate

### 1.3.1 #202601260148 -- Modifica misure cautelari non possibile

Stato: Closed Successful \| Data: 26/01/2026

Problema: Presofferto inserito come computabile, risultato
dall\'istruttoria non computabile. Impossibile modificare le misure
cautelari.

**Soluzione applicativa:**

1\. Annullare la richiesta inserita dall\'Elenco Provvedimenti del PM
(tasto X).\
2. Modificare le misure cautelari.\
3. Reinserire la richiesta.\
\
NOTA: La modifica diretta su DB non è consigliata se la pena residua è
già stata validata.

### 1.3.2 #20250122018 -- Calcolo presofferto con differenza di 2 giorni

Stato: Closed Successful \| Data: 22/01/2025

Problema: Differenza di 2 giorni tra calcolo su periodo unico vs. due
sottoperiodi.

**Soluzione:**

Il comportamento è corretto: spezzare un periodo in due sottoinsiemi non
garantisce che la somma coincida col totale, a causa della diversa
durata dei mesi (es. febbraio). Se non soddisfacente, richiedere una MEV
all\'Amministrazione.

### 1.3.3 #202409100115 / #20240806016 -- Pena residua non ricalcolata dopo presofferto

Stato: Closed Successful \| Data: 2024

Problema: Dopo rideterminazione pena + computo presofferto, la pena
residua non è corretta.

**Soluzione:**

La misura cautelare era stata inserita dopo il provvedimento di
rideterminazione pena, quindi non computata. L\'OE non ricalcola ma usa
la pena a sistema.\
Azione: Inserire una pena residua manuale.

### 1.3.4 #20200110017 -- Cancellazione periodi di presofferto (bug sw)

Stato: Closed Successful \| Data: 10/01/2020

Problema: Durante emissione di un cumulo, dopo l\'eliminazione di
periodi di misura cautelare, il sistema manteneva comunque il dato nel
riepilogo pene.

**Soluzione:**

Risolto con fix software nella versione 11.2.5.

## 1.4 Raccomandazione operativa

Prima di procedere, verificare con l\'utente se per il SIEP 2026/320 è
già stato emesso un Ordine di Esecuzione:\
• Se OE NON emesso e fascicolo aperto → eliminazione del presofferto
duplicato possibile da applicativo (Elenco Provvedimenti PM → tasto
X/Annulla).\
• Se OE già emesso o fascicolo archiviato → la modifica diretta su DB è
sconsigliata; annotare l\'errore nelle note del procedimento.

# 2. Ticket #20260612015 -- Impossibile generare provvedimento di Liberazione Anticipata

Creato il 12/06/2026 -- Stato: In attesa di informazioni Assistenza
(presa in carico)

## 2.1 Intestazione ticket

  -----------------------------------------------------------------------
  **Campo**                           **Valore**
  ----------------------------------- -----------------------------------
  **Numero ticket**                   20260612015

  **Titolo**                          Non riusciamo a generare un
                                      provvedimento di liberazione
                                      anticipata

  **Stato**                           In attesa di informazioni
                                      Assistenza

  **Priorità**                        2 Low

  **Tipo**                            04 - MAC - Manutenzione correttiva

  **Coda**                            Desk-RTI

  **Cliente**                         UTA / stefano.anselmi

  **Fascicolo SIEP**                  654/2024

  **Ufficio Sorveglianza**            Napoli

  **Creato il**                       12/06/2026 09:22
  -----------------------------------------------------------------------

## 2.2 Descrizione del problema

Impossibile generare un provvedimento di Liberazione Anticipata per il
fascicolo SIEP 654/2024: il sistema non consente di caricare
l\'Ordinanza dell\'Ufficio di Sorveglianza di Napoli, nemmeno con
inserimento manuale.

## 2.3 Attività di analisi in corso

Il 16/06/2026 Simone Gioggi ha inviato all\'utente due query
diagnostiche in attesa di risposta:

**Query 1 -- LICENZA_LIBANTICIPATA (EVE_ID_EVENTO = 4607699232026):**

SELECT ID_LICENZA_LIBANTICIPATA, COD_TIPO_LICENZA, NUMERO_GIORNI,\
DATA_INIZIO, DATA_FINE, FLAG_CONCESSO, FLAG_ELABORATO,\
ANNO_ORDINANZA, NUMERO_ORDINANZA, COD_UFFICIO_EMITTENTE,\
DATA_EMISSIONE_ORDINANZA, GIORNI_SCOMPUTATI, COD_ESITO\
FROM LICENZA_LIBANTICIPATA\
WHERE EVE_ID_EVENTO = 4607699232026;

**Query 2 -- PERIODO_LIBANTICIPATA (LIC_ID = 469988232026):**

SELECT ID_PERIODO_LIBANTICIPATA, DATA_INIZIO, DATA_FINE,\
FLAG_CONCESSO, DATA_INSERIMENTO, LIC_ID_LICENZA_LIBANTICIPATA\
FROM PERIODO_LIBANTICIPATA\
WHERE LIC_ID_LICENZA_LIBANTICIPATA = 469988232026\
ORDER BY DATA_INIZIO;

## 2.4 Soluzioni simili trovate

### 2.4.1 #202412190127 -- Belluno: problema visualizzazione giorni LA

Stato: Closed Successful \| Data: 19/12/2024

Problema: Visualizzazione errata giorni di liberazione anticipata e di
riduzione pena, impossibile proseguire la lavorazione del fascicolo.

**Soluzione -- Script DB eseguito:**

DELETE FROM LICENZA_LIBANTICIPATA\
WHERE ID_LICENZA_LIBANTICIPATA IN (206748122024, 206749122024);\
\
DELETE FROM PENA_RESIDUA\
WHERE ID_PENA_RESIDUA = 708728122024;\
\
COMMIT;

Dopo l\'esecuzione, l\'utente ha ripreso la lavorazione del fascicolo
regolarmente.

### 2.4.2 #202503170135 -- Modifica giorni LA con DELETE su LICENZA_LIBANTICIPATA

Stato: Closed Successful \| Data: 17/03/2025

Problema: Giorni di LA non modificabili da applicativo; record da
cancellare e reinserire.

**Fase 1 -- Query diagnostiche:**

SELECT \* FROM LIB_ANTICIPATA_CUMULO c\
WHERE c.TIT_ID_TITOLO_CUMULATO IN (\
SELECT tc.ID_TITOLO_CUMULATO FROM TITOLO_CUMULATO tc\
WHERE tc.ISTR_ID_ISTRUTTORIA_CUMULO IN (\
SELECT ic.ID_ISTRUTTORIA_CUMULO FROM ISTRUTTORIA_CUMULO ic\
WHERE ic.FAS_SIE_ID_FASCICOLO_SIEP IN (\
SELECT fs.ID_FASCICOLO_SIEP FROM FASCICOLO_SIEP fs\
WHERE fs.CHIAVE_ANNO = 2025 AND fs.CHIAVE_PROGR = 121\
AND fs.CHIAVE_UFFICIO = \'02704202104\')));\
\
SELECT \* FROM LICENZA_LIBANTICIPATA ll\
WHERE ll.FAS_SIE_ID_FASCICOLO_SIEP IN (\
SELECT fs.ID_FASCICOLO_SIEP FROM FASCICOLO_SIEP fs\
WHERE fs.CHIAVE_ANNO = 2025 AND fs.CHIAVE_PROGR = 121\
AND fs.CHIAVE_UFFICIO = \'02704202104\');

**Fase 2 -- Script risolutivo:**

DELETE FROM LICENZA_LIBANTICIPATA\
WHERE ID_LICENZA_LIBANTICIPATA = 210300122025;\
\
COMMIT;

### 2.4.3 #202503240120 -- SIEP 205-2024: LA non emettibile per mancanza Fine Pena

Stato: Closed Successful \| Data: 24/03/2025

Problema: Impossibile emettere il provvedimento di LA perché il
fascicolo non ha un FINE PENA: il programma non riesce a calcolare il
nuovo fine pena con la decurtazione dei giorni di LA.

**Soluzione:**

1\. Eseguire un Calcolo Pena oppure inserire una Pena Residua Manuale
(menù Assegnazioni).\
2. Una volta presente il Fine Pena validato, riprovare con
l\'inserimento della Liberazione Anticipata.

### 2.4.4 #20240613014 -- Modifica esito/periodi LA da applicativo

Stato: Closed Successful \| Data: 13/06/2024

Problema: Esito e periodi della Liberazione Anticipata da correggere.

**Soluzione applicativa (senza intervento DB):**

1\. Da Elenco Provvedimenti → cliccare icona Modifica.\
2. Nella form, nella parte bassa, modificare l\'esito e i periodi.\
3. Spuntare la checkbox abilitata, azzerare/modificare i valori.\
4. Cliccare Conferma.

### 2.4.5 #202511240119 -- Correzione giorni LA con UPDATE su DEPOSITO_ORDINANZA_PC

Stato: Closed Successful \| Data: 24/11/2025

Problema: Numero giorni LA errato (45 invece di 90).

**Soluzione:**

1\. Da Elenco Provvedimenti: annullare il deposito dell\'ordinanza.\
2. Dalla colonna Azioni → icona Modifica → campo \"Totale giorni
concessi\" → inserire 90.\
3. Aggiornare anche il campo DB:

DEPOSITO_ORDINANZA_PC.NUM_GIORNI_LIBANTICIPATA

Per trovare il record: cercare in DEPOSITO_ORDINANZA_PC dove\
ID_EVENTO_GENERATO = EVE_ID_EVENTO di LICENZA_LIBANTICIPATA.

## 2.5 Raccomandazione operativa

In attesa dei risultati delle query diagnostiche, il percorso di analisi
suggerito è:\
\
1. Verificare se LICENZA_LIBANTICIPATA ha record incompleti o corrotti
per EVE_ID_EVENTO = 4607699232026.\
→ Se sì: DELETE del record + COMMIT, poi ricreare da applicativo.\
\
2. Verificare la presenza di un FINE PENA validato nel fascicolo SIEP
654/2024 (tabella PENA_RESIDUA con FLAG_VALIDATO = \'S\').\
→ Se assente: far eseguire Calcolo Pena o Pena Residua Manuale.\
\
3. Se i dati sono corretti ma l\'ordinanza di Napoli non è caricabile:
tentare inserimento manuale da Elenco Provvedimenti → Modifica.

────────────────────────────────────────────────────────────

Documento generato automaticamente da analisi OTRS DB

Centro di Competenza Sistemi Area Penale -- ENG