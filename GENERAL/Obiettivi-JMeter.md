---
uniqueName: obiettivi-jmeter
displayName: "Obiettivi JMeter"
category: "GENERAL"
tags: []
---

# Obiettivi JMeter

> **File originale:** `MEV/SCHEDA_006/ATTIVITA_JMETER/JMETER_PSM_20200617/Obiettivi JMeter.docx`  
> **Tipo:** DOCX

---

# Obiettivo dell’intervento
Stressare l’application server distrettuale http://161.27.213.72:8082/ su cui è deployata la release 12.4.0 di SIES e che punta al database di collaudo: 161.27.213.62
SIESTO-PSM =
(DESCRIPTION =
(ADDRESS = (PROTOCOL = TCP)(HOST = 161.27.213.62)(PORT = 1521)
)
(CONNECT_DATA =
(SERVER = DEDICATED)
(SERVICE_NAME = siesto)
)
)
Test richiesti:
Esecuzione di “SIUS_2_noGUI.jmx” che invoca l’applicazione “AVVOCATURA Centrale” che è installata all’indirizzo: http://161.27.213.72:8083/PST/SIUS/; l’applicazione colloquia col Sies distrettuale interrogando il database su citato.
Esecuzione di “SIEP_SIUS_SIGE.jmx” che invoca l’applicazione “SIES distrettuale” (descritta sopra).
Parametri per SIUS – avvocatura:
AVV_CON_CF_TDS.csv
AVV_CON_CF_UDS.csv
Parametri per SIES:
SIEPavanzata.csv
SIEPbase.csv
SIEPesecuzione_decreto_sospensione.csv
SIEPesecuzione_pena.csv
SIEPliberazione_anticipata.csv
SIEPordine_esecuzione.csv
SIEPricerca_per_soggetto.csv
SIEPsemiliberta.csv
SIGE.csv
SIUSfissazione_udienza.csv
SIUSricerca_titolo_iscrizione.csv