---
uniqueName: 16frontenddeepassessment
displayName: "16 frontend deep assessment"
category: "GENERAL"
tags: []
---

# Frontend Deep Assessment — Progetto SIUS

**Data**: 2026-04-24  
**Versione**: 1.0  
**Autori**: IMPACT AI Agent  
**Audience**: Frontend Developer, Tech Lead, UX Engineer

> **Nota**: SIUS non usa Angular ma JSP/JSTL legacy con HTML 4.01 e JavaScript ES3 minimale. Questo assessment è adattato alla tecnologia effettiva del frontend. Il prompt AGENTS_FE.md è progettato per Angular — le sezioni non applicabili sono sostituite con analisi equivalenti per la tecnologia in uso.

---

## Executive Summary

### Overall Frontend Health Score: 12 / 100 🔴

| Categoria | Score | Dettaglio |
|-----------|-------|-----------|
| Architettura | 20/100 | JSP server-side rendering, no component model |
| Performance | 25/100 | Nessun caching, nessun bundling, no CDN |
| Accessibilità | 10/100 | HTML 4.01, nessun ARIA, no semantic HTML |
| Sicurezza | 20/100 | No CSRF token, XSS possibile via scriptlet |
| Manutenibilità | 15/100 | 660 JSP con scriptlet misti, HTML 4.01 |
| Testabilità | 0/100 | Zero test frontend |

**Top 3 Issues**:
1. 🔴 **Scriptlet Java in JSP**: logica business nelle view → accoppiamento totale
2. 🔴 **HTML 4.01 non semantico**: nessuna accessibilità, non WCAG compliant
3. 🔴 **Zero test frontend**: nessun test di integrazione o E2E

**Top 3 Recommendations**:
1. ✅ Introdurre JSTL expression language per eliminare scriptlet Java dalle JSP
2. ✅ Aggiungere meta viewport + responsive CSS per multi-device support  
3. ✅ Implementare test E2E con Playwright sulle funzionalità critiche

---

## 1. Architettura Frontend

### 1.1 Tecnologia Stack

| Componente | Tecnologia | Versione | Status |
|------------|-----------|---------|--------|
| Template engine | JSP (JavaServer Pages) | 2.1 | 🔴 Legacy (2006) |
| Tag library | JSTL | 1.2 | 🟡 Supportato ma obsoleto |
| HTML version | HTML 4.01 Transitional | — | 🔴 Superseded da HTML5 (2014) |
| JavaScript | ES3 vanilla | — | 🔴 ES2015+ è standard dal 2015 |
| CSS | CSS 2.1 inline/embedded | — | 🔴 No modern CSS |
| Styling framework | Nessuno | — | 🔴 Custom ad-hoc |
| Build system | Nessuno | — | 🔴 No bundling/minification |
| SPA framework | Nessuno | — | Non applicabile |

### 1.2 Struttura View Layer

```
fe/
└── sius/
    ├── avvocato/           # ~20 JSP
    ├── cancassfascsius/    # JSP
    ├── depositoordinanzapc/ # JSP grandi (5.799 LOC max)
    ├── fascicolo/          # ~80 JSP (modulo core)
    ├── stampa/             # JSP per preview stampa
    ├── statistiche/        # JSP report/tabelle
    └── ... (46 moduli totali)
670 file JSP totali / 163.841 linee totali
```

### 1.3 Routing

Non esiste un router frontend. Il routing è interamente server-side tramite HTTP request processing del framework F3B:

```html
<!-- Navigazione tramite form POST o link con ACTION_FIELD -->
<form action="/siap/Dispatcher" method="post">
    <input type="hidden" name="ACTION_FIELD" 
           value="siap.sius.fascicolo.action.ActRicercaFascicolo"/>
    <!-- ... -->
</form>

<!-- Oppure link diretto -->
<a href="/siap/Dispatcher?ACTION_FIELD=siap.sius.fascicolo.action.ActDettaglioFascicolo&id=123">
```

**Impatto manutenibilità**: rinominare una classe Action Java richiede aggiornare tutti i JSP che la referenziano. Non c'è compilazione statica a verificare i link.

---

## 2. JSP Architecture Analysis

### 2.1 Scriptlet Usage

**670 su 670 JSP (100%) contengono scriptlet Java** (`<% ... %>` e `<%= ... %>`):

```jsp
<!-- Pattern tipico — scriptlet in JSP (ANTI-PATTERN) -->
<%
    FascicoloModel fascicolo = (FascicoloModel) request.getAttribute("fascicolo");
    String codStato = fascicolo.getCodStatoFascicolo();
    if ("99".equals(codStato)) {
%>
    <p class="warning">Fascicolo cancellato</p>
<%
    } else {
%>
    <p>Fascicolo attivo</p>
<%  } %>
```

Questo pattern viola la separazione MVC: la view contiene logica Java che dovrebbe stare nel Controller. Le conseguenze:
- Impossibile testare la view indipendentemente dalla logica
- I designer non possono lavorare sulle JSP senza conoscere Java
- Errori di runtime nella view invece che in fase di compilazione

### 2.2 Pattern di Template (JSTL)

JSTL è **assente** nelle JSP SIUS (0 file con `<%@ taglib`). Il 100% delle JSP usa scriptlet Java puri invece di JSTL `<c:if>`, `<c:forEach>`, EL expressions `${...}`.

**Confronto: stato attuale vs best practice JSP:**

```jsp
<!-- STATO ATTUALE (scriptlet) -->
<%
    Collection list = (Collection) request.getAttribute("listaFascicoli");
    Iterator it = list.iterator();
    while (it.hasNext()) {
        FascicoloModel f = (FascicoloModel) it.next();
%>
    <tr><td><%= f.getChiaveAnno() %>/</td></tr>
<%  } %>

<!-- BEST PRACTICE (JSTL) — non usato -->
<c:forEach var="f" items="${listaFascicoli}">
    <tr><td>${f.chiaveAnno}/</td></tr>
</c:forEach>
```

### 2.3 Dimensioni JSP — God Views

| JSP | LOC | Modulo |
|-----|-----|--------|
| ModificaOrdinanzaReclamoLA.jsp | 5.799 | depositoordinanzapc |
| ModificaOrdinanzaRevocaLA.jsp | 5.357 | depositoordinanzapc |
| ModificaOrdinanzaLibAnt.jsp | 3.627 | depositoordinanzapc |
| InserisciOrdinanzaReclamoLA.jsp | 3.305 | depositoordinanzapc |
| InserisciOrdinanzaRevocaLA.jsp | 3.030 | depositoordinanzapc |
| DettaglioFascicolo.jsp | 1.488 | fascicolo |

Le JSP da 3.000-5.800 LOC sono l'equivalente frontend dei God Classes backend: un singolo file misto di HTML, Java scriptlet, SQL inline logic, e form HTML.

---

## 3. HTML & Accessibilità

### 3.1 Struttura HTML

```html
<!-- Doctype tipico nelle JSP SIUS -->
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">
<html>
<head>
    <title>SIUS - Fascicolo</title>
    <!-- Nessun meta charset, nessun meta viewport -->
</head>
<body>
    <!-- Layout a tabelle (pre-CSS layout) -->
    <table width="100%" cellpadding="0" cellspacing="0">
        <tr><td>...</td></tr>
    </table>
</body>
</html>
```

**Problemi identificati:**
- No `<meta charset="UTF-8">` → rischio encoding in browser
- No `<meta name="viewport">` → non responsive su mobile/tablet
- Layout basato su `<table>` → semantica sbagliata, non accessibile
- No landmark HTML5 (`<header>`, `<nav>`, `<main>`, `<footer>`)
- No `<label>` associato ai campi form in molte JSP

### 3.2 Accessibilità (WCAG 2.1)

| Criterio WCAG | Status | Evidenza |
|-------------|--------|----------|
| 1.1.1 Non-text Content | 🔴 FAIL | Nessun `alt` attribute sulle immagini |
| 1.3.1 Info & Relationships | 🔴 FAIL | Layout a tabelle invece di CSS |
| 2.1.1 Keyboard | 🟡 Parziale | Navigazione tab HTML nativa, senza gestione focus |
| 2.4.4 Link Purpose | 🔴 FAIL | Link "Clicca qui", "Dettaglio" non descrittivi |
| 3.1.1 Language of Page | 🟡 Parziale | lang="it" non sempre specificato |
| 4.1.2 Name, Role, Value | 🔴 FAIL | Nessun ARIA, nessun role attribute |

**Health WCAG**: Stimato ~10-15% conformità. Il sistema non è conforme alle linee guida AGID (Accessibilità PA italiana - D.Lgs 106/2018 e Regolamento AgID).

---

## 4. JavaScript & Form Management

### 4.1 JavaScript

Solo 2 file `.js` presenti nel repository (`~300 SLOC`). Il resto del comportamento client-side è inline `<script>` nei JSP (trovati in 573 su 670 file).

```jsp
<!-- Pattern tipico JS inline in JSP (85% delle JSP) -->
<script language="javascript">
function validaForm() {
    if (document.forms[0].idFascicolo.value == '') {
        alert('ID fascicolo obbligatorio');
        return false;
    }
    return true;
}
</script>
```

**Caratteristiche del JavaScript:**
- ES3 vanilla — `var`, `function`, `document.forms[0]`
- No module system, no `import/export`
- Validazione client-side con `alert()` (UX degradata)
- No framework (jQuery non presente)
- Nessun test JavaScript

### 4.2 Form Architecture

| Metrica | Valore |
|---------|--------|
| JSP con form HTML | 105 |
| Method principalmente usato | POST |
| Validazione client | alert() JS inline |
| Validazione server | ActionSius helper methods |
| Upload file | commons-fileupload (backend) |

---

## 5. Performance Frontend

### 5.1 Loading Performance

| Aspetto | Status | Impatto |
|---------|--------|---------|
| Minification JS/CSS | ❌ Assente | Payload incrementato |
| Gzip compression | Dipende da JBoss config | Non verificabile da codebase |
| Browser caching | Dipende da JBoss config | Non verificabile |
| CDN | ❌ Non presente | Latenza interna PA |
| Lazy loading immagini | ❌ Assente | Caricamento di tutte le immagini |
| HTTP/2 | Dipende da deployment | Non verificabile |

**Stima First Contentful Paint**: Le pagine più grandi (5.800 LOC JSP, layout a tabelle nested) su rete intranet PA (latenza stimata 10-50ms) potrebbero avere FCP intorno a 2-5 secondi.

### 5.2 Server-Side Rendering Performance

Il rendering è interamente server-side: ogni navigazione è una nuova richiesta HTTP che:
1. Passa per F3B Dispatcher
2. Esegue l'Action (query DB via DAO)
3. Renderizza il JSP completo
4. Restituisce HTML completo al browser

Non esiste caching a nessun livello dell'applicazione. La sessione stateful (`fascicoloSiusGP`) evita alcune query ridondanti ma è una forma di caching non controllata.

---

## 6. Security Frontend

### 6.1 XSS Risk

```jsp
<!-- RISCHIO XSS: output non escaped di parametri request -->
<%= request.getParameter("nomeCognome") %>  <!-- potenziale XSS -->

<!-- Corretto (ma assente nelle JSP) -->
<%@ taglib uri="http://java.sun.com/jsp/jstl/functions" prefix="fn" %>
${fn:escapeXml(param.nomeCognome)}
```

La presenza di output di parametri HTTP direttamente nelle JSP senza escaping è un vettore XSS. La severità dipende dal contesto (sistema PA intranet riduce l'exposure, ma non elimina il rischio da insider threat).

### 6.2 CSRF

Nessun CSRF token nei form SIUS. Mitigazione parziale: il sistema richiede autenticazione JAAS, quindi l'attacker deve essere autenticato. Tuttavia, un'applicazione malevola eseguita nel browser dell'utente autenticato potrebbe inviare richieste CSRF valide.

---

## 7. Testing Strategy Frontend

### 7.1 Stato attuale

| Tipo test | Presenza | File |
|-----------|---------|------|
| Unit test (Java) | ❌ 0 | 0 |
| Integration test | ❌ 0 | 0 |
| E2E test (Selenium/Playwright) | ❌ 0 | 0 |
| Visual regression | ❌ 0 | 0 |

### 7.2 Strategia raccomandata

Il frontend JSP non è direttamente testabile con Jest/Jasmine. La strategia raccomandata è:

```
1. E2E Characterization Tests (Playwright)
   → Catturare tutti i flussi utente principali
   → Screenshot comparison come baseline
   → Verifica che le funzionalità esistenti non si rompano
   
2. Integration Tests (Spring Test / Selenium)
   → Test di rendering delle JSP con dati mock
   
3. Accessibility Tests (axe-core via Playwright)
   → Audit automatico WCAG sulle pagine critiche
   
4. Form Validation Tests
   → Test che le validazioni JS funzionino come atteso
```

---

## 8. Technical Debt Frontend

### Priority 1 — Critical

| Issue | Impatto | Effort remediation |
|-------|---------|-------------------|
| Scriptlet Java in tutte le 670 JSP | Non testabili, business in view | 12+ mesi (670 JSP) |
| Nessun test E2E | Regressioni invisibili | 4-6 settimane iniziali |
| CSRF token assente | Security risk | 2 settimane |
| XSS output non escaped | Security risk | 2-4 settimane |

### Priority 2 — Medium

| Issue | Impatto | Effort remediation |
|-------|---------|-------------------|
| HTML 4.01 → HTML5 semantico | Accessibilità AGID | 6+ mesi |
| WCAG 2.1 compliance | Obbligo normativo PA | 8+ mesi |
| Alert() → notifiche UX moderne | UX degradata | 4 settimane |
| Layout tabelle → CSS flexbox/grid | Responsiveness | 4+ mesi |

### Priority 3 — Low/Long Term

| Issue | Impatto | Effort remediation |
|-------|---------|-------------------|
| JSP → framework moderno (Angular/React) | Modernizzazione totale | 18-24 mesi |
| Bundle JS/CSS (Webpack/Vite) | Performance | 2 settimane (build pipeline) |
| CSS framework (Bootstrap 5) | Design system | 2-3 mesi |

---

## 9. Roadmap di Modernizzazione Frontend

### Fase 0 — Security Immediate (1 mese)
- [ ] CSRF token in tutti i form (2 sett)
- [ ] XSS escaping su tutti gli output in JSP (2 sett)

### Fase 1 — Quick Wins (3 mesi)
- [ ] E2E Playwright tests sui 20 flussi più critici (4 sett)
- [ ] Migrare JS `alert()` → CSS toast/modal
- [ ] Aggiungere `<meta charset="UTF-8">` e `<meta viewport>` a tutte le JSP

### Fase 2 — Accessibilità AGID (6-12 mesi)
- [ ] Sostituire `<table>` layout con CSS (pagine per pagina)
- [ ] Aggiungere `<label>` a tutti i campi form
- [ ] Aggiungere `alt` text a tutte le immagini
- [ ] Test automatico axe-core in CI/CD

### Fase 3 — Modernizzazione (12-24 mesi)
- [ ] Introdurre JSTL/EL nelle JSP esistenti (rimuovere scriptlet)
- [ ] Eventuale migrazione a framework SPA (Angular/React) con REST backend

---

## Reference Documents

- **Deep Dive**: `docs/00_deep_dive.md`
- **Software Architecture**: `docs/06_software_architecture.md`
- **Code Patterns**: `docs/07_code.md`
- **Antipattern Assessment**: `docs/18_antipattern_deep_dive.md`
- **Backend Assessment**: `docs/17_backend_deep_assessment.md`
- **Metrics**: `docs/14_metrics.md`

---

## Change Log

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | 2026-04-24 | IMPACT AI Agent | Prima versione — frontend deep assessment |