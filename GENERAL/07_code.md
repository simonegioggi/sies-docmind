---
uniqueName: 07code
displayName: "07 code"
category: "GENERAL"
tags: []
---

# Code Implementation Details - Progetto SIUS

**Data**: 2026-04-24  
**Versione**: 1.0  
**Autori**: IMPACT AI Agent  
**Audience**: Team tecnico, developer

---

## 1. Code Organization & Structure

### 1.1 Package Root e Gerarchia

Tutto il codice SIUS risiede nel package `siap.sius.*`. La struttura è rigidamente replicata per ciascuno dei 49 domini funzionali:

```
siap.sius.{domain}.action     → HTTP handlers
siap.sius.{domain}.controller → Business logic (+ interfaccia I{Domain})
siap.sius.{domain}.dao        → Data access
siap.sius.{domain}.model      → DTO
```

File di base a livello radice:
- `siap.sius.ActionSius` — base class per tutte le action SIUS
- `siap.sius.SIUSException` — eccezione radice
- `siap.sius.util.SIUSLookupRemote` — service locator

### 1.2 Proporzione Layer

| Layer | File | % totale |
|-------|------|----------|
| Action (HTTP) | 935 | 72% |
| DAO | 110 | 8.5% |
| Controller | 42 | 3.2% |
| Model | 93 | 7.2% |
| Constants/Utils | 114 | 8.8% |

Il layer Action è enormemente sovradimensionato rispetto agli altri: ogni operazione CRUD genera Actions separate (`ActLoad*`, `Act*`, `ActCancella*`, `ActModifica*`, `ActRicerca*`).

---

## 2. Key Implementation Patterns

### 2.1 Action Pattern (HTTP Handler)

Ogni Action è una classe separata che estende `ActionSius` e implementa **un solo metodo**: `processRequest()`. L'Action:
1. Recupera il fascicolo dalla sessione
2. Legge i parametri HTTP tramite F3B helpers
3. Costruisce un Model
4. Chiama il Controller tramite `SIUSLookupRemote`
5. Restituisce il path JSP di redirect

```java
public class ActInserisciRichiestaConversionePP 
    extends ActionSius 
    implements ICostantiSiusPenaPecuniaria {

    public String processRequest() throws F3BException {
        // 1. Session state
        FascicoloGPModel lFasGPMod = 
            (FascicoloGPModel) getSessionAttribute("fascicoloSiusGP");

        // 2. HTTP params → Model
        RichiestaConversioneModel lRicMod = new RichiestaConversioneModel();
        lRicMod.setAnnoPartita(getRequestBigDecimalParameter(CAMPO_ANNO_PARTITA));
        lRicMod.setDataRicezioneAtto(getRequestDateParameter(
            CAMPO_ANNO_DATA_RICEZIONE_ATTO,
            CAMPO_MESE_DATA_RICEZIONE_ATTO,
            CAMPO_GIORNO_DATA_RICEZIONE_ATTO));

        // 3. Boolean flag: "S"/"N" invece di boolean
        if (!isRequestParameterNullObj(CAMPO_FLAG) && isRequestChecked(CAMPO_FLAG))
            lRicMod.setFlag("S");
        else
            lRicMod.setFlag("N");

        // 4. Controller via Service Locator
        IRichiestaConversione ctrl = SIEPLookupRemote.getRichiestaConversioneRemote();
        lRicMod = ctrl.ExInserisciRichiestaConversione(lRicMod);

        // 5. Redirect
        return IWebConstants.PG_MAIN + "?" + IWebConstants.ACTION_FIELD +
               "=siap.sius.penapecuniaria.action.ActLoadDettaglio..." +
               "&" + CAMPO_ID + "=" + lRicMod.getId();
    }
}
```

### 2.2 Controller Pattern (Business Logic + Transaction)

I Controller gestiscono esplicitamente le transazioni JDBC. Il pattern `getDBTransaction()` / `commit()` / `rollback()` / `cleanup()` è uniforme in tutti i 42 controller:

```java
public AvvocatoSiusModel ExInserisciAvvocato(...) throws F3BException {
    Connection lConn = null;
    AvvocatoDAO lAvvDao = null;
    try {
        lConn = getDBTransaction();             // Apre connessione + disabilita autocommit
        lAvvDao = new AvvocatoDAO(lConn);
        lAvvDao.setDAOFromModel(aAvvocato);     // Mappa Model → DAO
        BigDecimal lId = lAvvDao.insert();      // Esegue INSERT, ritorna sequence
        aAvvocato.setIdAvvocato(lId);
        commit(lConn);
    } catch (DAOException ex) {
        rollback(lConn);
        throw new F3BException("Metodo: " + ex);
    } catch (Exception e) {
        rollback(lConn);
        throw new F3BException("Metodo: " + e);    // Eccezione troppo generica
    } finally {
        cleanup(lAvvDao);
        cleanup(lConn);
    }
}
```

**Problemi**: `catch(Exception e)` generico mascherante, eccezione re-thrown come `F3BException` perde lo stack trace originale.

### 2.3 DAO Pattern (SQL Concatenazione)

Ogni DAO estende `SIAPSqlDAO` e costruisce SQL per concatenazione. Il mapping result set → model avviene nel metodo `getModel()`:

```java
public class FascicoloSiusSqlDAO extends SIAPSqlDAO {
    public void ricercaFascicoloSius(FascicoloSiusModel aModel) throws DAOException {
        String lStatement = getSqlQuery();         // SQL base dalla configurazione
        lStatement += " WHERE " + setCondizioni(aModel);  // Condizioni concatenate
        setStatement(lStatement);
    }

    public GenericModel getModel() throws DAOException {
        FascicoloSiusModel aModel = new FascicoloSiusModel();
        aModel.setIdFascicoloSius(getBigDecimal("ID_FASCICOLO_SIUS"));
        aModel.setChiaveAnno(getBigDecimal("CHIAVE_ANNO"));
        aModel.setChiaveUfficio(getString("CHIAVE_UFFICIO"));
        aModel.setCodStatoFascicolo(getString("COD_STATO_FASCICOLO"));
        aModel.setDataInserimento(getDate("DATA_INSERIMENTO"));
        // ... 20+ campi
        return aModel;
    }
}
```

### 2.4 Date Field Split Pattern

Le date vengono trasmesse via HTTP come **3 parametri separati** (giorno/mese/anno) e ricomposti nell'Action:

```java
// 481 occorrenze nel codebase
lRicMod.setDataRicezioneAtto(getRequestDateParameter(
    CAMPO_ANNO_DATA_RICEZIONE_ATTO,   // "AnnoDataRicezioneAtto"
    CAMPO_MESE_DATA_RICEZIONE_ATTO,   // "MeseDataRicezioneAtto"
    CAMPO_GIORNO_DATA_RICEZIONE_ATTO  // "GiornoDataRicezioneAtto"
));
```

Questo pattern richiede 3 costanti per ogni campo data: proliferazione di `ICostanti*.java`.

### 2.5 Boolean Flag Pattern ("S"/"N")

I booleani sono rappresentati come `String "S"` / `"N"` nel database e nel Model (317 occorrenze):

```java
if (isRequestChecked(CAMPO_FLAG_IMPRESCRITTIBILE_MULTA))
    lRicMod.setFlagImprescrittibileMulta("S");
else
    lRicMod.setFlagImprescrittibileMulta("N");
```

### 2.6 Naming Convention Business Methods

Tutti i metodi di business nei controller usano il prefisso `Ex` (Execute):
- `ExInserisci{Entity}` — INSERT
- `ExModifica{Entity}` — UPDATE
- `ExCancella{Entity}` — DELETE
- `ExRicerca{Entity}By{Key}` — SELECT per chiave
- `ExRicerca{Entity}Pagina` — SELECT paginata

### 2.7 Redirect Pattern

Le Action restituiscono una stringa di redirect che include l'Action successiva come parametro HTTP:

```java
return IWebConstants.PG_MAIN + "?" 
     + IWebConstants.ACTION_FIELD + "=siap.sius.penapecuniaria.action.ActLoadDettaglio..."
     + "&" + CAMPO_ID + "=" + lRicMod.getId().toString();
```

Il framework F3B intercetta la stringa e instrada alla classe Action specificata. Questo è un **routing via reflection** basato sul fully-qualified class name.

---

## 3. Framework Usage

### 3.1 F3B Framework

Framework proprietario Bull/Atos. La gerarchia delle classi base:

```
f3b.web.ActionF3B
  └── siap.web.ActionSiap          (SIAP common)
        └── siap.sico.web.ActionSiap  (SICO variant)
              └── siap.sius.ActionSius   (SIUS-specific)
```

Metodi F3B utilizzati pervasivamente:

| Metodo | Utilizzo | Occorrenze stimate |
|--------|----------|--------------------|
| `getRequestStringParameter(String)` | Lettura HTTP param → String | >2000 |
| `getRequestBigDecimalParameter(String)` | Lettura HTTP param → BigDecimal | >1000 |
| `getRequestDateParameter(String,String,String)` | Lettura data 3-parti | 481 |
| `isRequestParameterNullObj(String)` | Check null HTTP param | >1500 |
| `isRequestChecked(String)` | Check checkbox HTTP | >200 |
| `getSessionAttribute(String)` | Lettura sessione | >500 |
| `setSessionAttribute(String,Object)` | Scrittura sessione | >200 |
| `setRequestAttribute(String,Object)` | Set attributo request | >300 |

### 3.2 Nessun ORM

Non viene usato alcun ORM (JPA, Hibernate, MyBatis). Il layer DAO è basato su JDBC puro mediato da `SIAPSqlDAO`. Il mapping è completamente manuale nel metodo `getModel()`.

### 3.3 Nessuna Dependency Injection

Nessun Spring, nessun CDI, nessun Guice. L'iniezione avviene tramite Service Locator:
```java
IFascicoloSius ctrl = SIUSLookupRemote.getFascicoloSiusRemote();
```
Il `lookup()` interno usa class reflection: `Class.forName(className).newInstance()`.

---

## 4. Security Implementation

### 4.1 Autenticazione

Gestita dal framework F3B / SICO prima di arrivare al layer SIUS. Nell'Action, l'utente è già autenticato e disponibile via:
- `getCodUtenteConnesso()` — codice operatore
- `getCodUfficioUtenteConnesso()` — codice ufficio dell'operatore
- `getUfficioUtenteConnesso()` → `UfficioModel` con `CodTipoUfficio`

### 4.2 Autorizzazione per Tipo Ufficio

```java
// In ActionSius.getFiltroMinorenni()
Set<String> elenco = new HashSet<String>();
elenco.add("PMM"); elenco.add("DIBM"); elenco.add("GIPM");
elenco.add("GUPM"); elenco.add("CAPSM"); elenco.add("TDSM"); elenco.add("UDSM");
return elenco.contains(tipoUfficio) ? "true" : "false";
```

### 4.3 Fascicolo Modificability Check

Prima di ogni operazione di modifica, l'Action verifica lo stato:
```java
// Stati NON modificabili: "01", "04", "05", "99"
protected boolean IsFascicoloSiusModificabile() throws F3BException {
    FascicoloGPModel lFascicolo = (FascicoloGPModel) getSessionAttribute("fascicoloSiusGP");
    String stato = lFascicolo.getFascicoloSiusModel().getCodStatoFascicolo();
    return !(stato.equals("01") || stato.equals("04") || 
             stato.equals("05") || stato.equals("99"));
}
```

### 4.4 Lock Applicativo

```java
// Prima di operazioni critiche:
lockApplicativo("NomeEntita");
// Implementazione: LockController.lockIfNotLocked(servletContext, entita, idFascicolo, codUtente, sessionId)
// Se già locked → SIUSException con messaggio all'utente
```

### 4.5 Vulnerabilità SQL Injection

**CRITICO**: nessun prepared statement è utilizzato. I parametri utente vengono inclusi direttamente nella stringa SQL tramite `setCondizioni()`:
```java
lStatement += " WHERE ID = " + aModel.getId().toString();  // NO BIND
```
La protezione si basa esclusivamente sul tipo `BigDecimal` per i parametri numerici. I parametri String sono potenzialmente vulnerabili.

---

## 5. Exception Handling & Logging

### 5.1 Exception Hierarchy

```
java.lang.Exception
  └── f3b.util.F3BException
        └── siap.SIAPException
              └── siap.sius.SIUSException
```

Codici di errore definiti in `F3BException`:
- `F3BException.USER_MESSAGE` — messaggio da mostrare all'utente
- `SIUSException.NULL_OBJECT_ERROR` — oggetto nullo in sessione
- `SIUSException.SYSTEM_ERROR` — errore di sistema

### 5.2 Pattern di Logging

**Dichiarazione** (obbligatoria per tutti i componenti):
```java
private static Logger siesLogger = Logger.getLogger(LogF3B.SIES_LOG);
```

**Utilizzo**:
```java
siesLogger.debug(getClass().getName() + ".processRequest: inizio");
// operazione...
siesLogger.debug(getClass().getName() + ".processRequest: fine");
siesLogger.error("Errore in " + getClass().getName(), exception);
```

**Problemi**:
- Log4j 1.x (EOL)
- Nessun MDC/context (no user/session ID nel log)
- No structured logging
- Debug level usato per entry/exit: rumoroso in produzione

### 5.3 Anti-Pattern: Exception Wrapping con Perdita Stack Trace

```java
// ANTI-PATTERN: perde il tipo originale e il stack trace
} catch (DAOException ex) {
    rollback(lConn);
    throw new F3BException("Metodo.ExInserisci: " + ex);  // ex.toString(), non ex come cause
}
```

Il corretto pattern sarebbe `throw new F3BException("msg", ex)` per preservare la cause chain.

---

## 6. Transaction Management

### 6.1 Gestione Manuale JDBC

Ogni controller gestisce esplicitamente la transazione:

```java
Connection lConn = null;
try {
    lConn = getDBTransaction();    // getConnection() + setAutoCommit(false)
    // ... operazioni DAO ...
    commit(lConn);                 // connection.commit()
} catch (...) {
    rollback(lConn);               // connection.rollback()
} finally {
    cleanup(lConn);                // connection.close()
}
```

**Osservazioni**:
- Non tutti i controller hanno il blocco `finally` con `cleanup()` — rischio connection leak
- Nessun gestione di savepoint o transazioni nested
- Nessun supporto a transazioni distribuite (XA)

### 6.2 Due Modalità di Connessione

```java
lConn = getDBTransaction();  // Con gestione transazionale (autocommit=false)
lConn = getDBConnection();   // Read-only / autocommit=true
```

---

## 7. Configuration Management

### 7.1 Configurazione Runtime

Non presente in questo fragment. La configurazione (datasource, JMS, logger) è gestita a livello di SIAP padre (JBoss AS descriptor + `jboss-web.xml`).

### 7.2 Constants Interface Pattern

Ogni dominio ha un'interfaccia `ICostanti{Domain}` con le costanti dei parametri HTTP:

```java
public interface ICostantiFascicoloSius {
    // HTTP parameter names (form field names)
    String CAMPO_ID_FASCICOLO_SIUS  = "IdFascicoloSius";
    String CAMPO_CHIAVE_ANNO        = "ChiaveAnno";
    String CAMPO_COD_STATO          = "CodStatoFascicolo";
    // ... 50+ costanti per dominio
}
```

50 interfacce × ~50 costanti medie = ~2.500 named constants nel progetto.

### 7.3 Routing Configuration

Il routing Action è **basato su fully-qualified class name** passato come parametro HTTP:
```
GET /siap/main?ACTION_FIELD=siap.sius.fascicolo.action.ActRicercaFascicolo
```
Nessun file di mapping (struts.xml, web.xml per action) — la dispatch è dinamica via reflection.

---

## 8. Testing Strategy

### 8.1 Stato Attuale

**Nessun test automatico rilevato** in questo fragment del codebase:
- Nessuna cartella `test/` o `src/test/`
- Nessuna classe `*Test.java` o `*TestCase.java`
- Nessuna dipendenza a JUnit, Mockito, TestNG, etc.
- Zero coverage verificabile

### 8.2 Difficoltà di Testing Ereditate

Il design attuale rende difficile il testing unitario per struttura:

| Ostacolo | Dettaglio |
|----------|-----------|
| Framework F3B no-mockable | `ActionSius` richiede un HTTP request reale per funzionare |
| Session HTTP accoppiata | `getSessionAttribute("fascicoloSiusGP")` → dipende da sessione HTTP |
| SQL concatenato | DAO non testabile senza DB reale |
| Controller con `new DAO()` | Nessuna injection possibile senza refactoring |
| God classes | `StampaController` (6.470 LOC) impossibile da testare in isolamento |

### 8.3 Strategia di Testing Consigliata per Refactoring

Prima di qualsiasi refactoring introdurre:
1. **Test di integrazione** a livello Controller+DAO con H2 in-memory o Oracle Test
2. **Contract test** per le interfacce `I{Domain}`
3. **Regression test** sulle Action via mock del framework F3B
4. Partire dai controller più stabili e meno dipendenti (es. `UdienzaController`, `TenoreController`)

---

## Reference Documents

- **Deep Dive**: `docs/00_deep_dive.md`
- **Software Architecture**: `docs/06_software_architecture.md`

---

## Change Log

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | 2026-04-24 | IMPACT AI Agent | Creazione documento iniziale |