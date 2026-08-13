---
uniqueName: usecasessies
displayName: "useCasesSIES"
category: "GENERAL"
tags: []
---

# Sessione Copilot – sies_Master

**Data:** 2026-04-30  
**Repository:** simonegioggi/sies_Master  
**Branch:** copilot/generate-use-cases-for-siep-sige-siup

---

## Contesto del Progetto

Il repository contiene il sistema **SIES** (Sistema Informativo per l'Esecuzione e la Sorveglianza), composto da due moduli principali:

| Modulo           | Versione       | Data Release |
|------------------|----------------|--------------|
| siesWeb          | 12.9.2.0       | 27/03/2026   |
| siesEsecuzione   | release_12.9.2.0 | 27/03/2026 |

---

## Obiettivo della Sessione

Generazione dei **casi d'uso** per i sottosistemi:

- **SIEP** – Sistema Informativo per l'Esecuzione Penale
- **SIGE** – Sistema Informativo per la Gestione dell'Esecuzione
- **SIUP** – Sistema Informativo Unico Penale

---

## Struttura del Repository

```
sies_Master/
├── comunicazioni.war       # Applicazione web comunicazioni
├── siesWeb/                # Modulo web principale (SIES Web)
│   ├── src/
│   │   ├── it/             # Package Java principali
│   │   ├── siap/           # Sottosistema SIAP
│   │   └── f3b/            # Sottosistema f3b
│   ├── defaultroot/
│   └── info.txt
└── siesEsecuzione/         # Modulo esecuzione (WEB_ESECUZIONE)
    ├── src/
    ├── pom.xml
    ├── readMe.txt
    └── info.txt
```

---

## Scambi della Sessione

### Richiesta 1
> *"salva questa sessione in un file pdf"*

**Risposta:** Non è possibile generare direttamente un file PDF dalla sessione. Sono state proposte alternative:
- Stampa dal browser → Salva come PDF (`Ctrl+P` / `Cmd+P`)
- Copia e incolla in Word/LibreOffice → Esporta PDF
- Screenshot completo della pagina
- Salvataggio del contenuto come file `.md` o `.txt` nel repository

### Richiesta 2
> *"sia .md che .txt grazie"*

**Risposta:** Creazione di entrambi i file (`sessione.md` e `sessione.txt`) nel repository.

---

## Note Tecniche

- Il progetto usa **Maven** come build tool (`pom.xml` in siesEsecuzione)
- Ambiente di sviluppo raccomandato: **Eclipse Kepler** con JDK 1.6 e Tomcat 6
- Connessione SVN: `https://production.eng.it/scm/svnrepos/sies`