---
uniqueName: siut-sies-pt-1-0-20200424-piano-dei-test
displayName: "SIUT SIES PT 1 0 20200424 Piano dei Test"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PT-1.0-20200424-Piano-dei-Test

> **File originale:** `RILASCIO_12.2.0/SIUT-SIES-PT-1.0-20200424-Piano-dei-Test.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A - Sirfin-PA, nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del sistema informativo unitario telematico, la manutenzione degli attuali sistemi dell’area penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Elenco approvazioni
| Versione | V. 1.0 del 24/04/2020 |
| --- | --- |
| Redatto da: | Domenico Nania |
| Verificato da: | Vito Bufi |
| Approvato da: | Vito Bufi |
| Data approvazione: | 24/04/2020 |
| Livello di riservatezza: | L4 |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Ruolo |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Pasquale Lamattina | RTI |  | Referente Tecnico |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Fabio Mazzocchi | RTI |  | Responsabile Manutenzione Correttiva |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Fabio Gattamorta | RTI |  | PMO |
| Edoardo Lamuraglia | RTI |  | Referente qualità |
| Francesco Rosati | RTI |  | Referente qualità |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 24/04/2020 | Prima Emissione |  |

INDICE DEI CONTENUTI
1.	Introduzione	5
1.1.	Scopo del documento	5
1.2.	Acronimi e Definizioni	5
1.2.1.	Acronimi	5
1.2.2.	Definizioni	6
1.3.	Riferimenti	6
2.	Obiettivi e portata dei test	7
2.1.	Descrizione delle scelte nella definizione dei test	7
2.1.1.	Entità da testare	7
2.1.2.	Entità escluse dal test	7
3.	Esecuzione dei test	8
4.	Documentazione esecuzione test	9
5.	Gestione delle anomalie e ripetizione dei test	10
6.	Ambiente di test	11
7.	Strumenti	12
7.1.	Database dei casi di prova	12
7.2.	Strumenti automatici di supporto ai test	12
8.	Specifica Test	13
8.1.	Descrizione dei Casi di Test	13


# Introduzione
## Scopo del documento
Il presente documento descrive il piano dei test per la verifica della risoluzione dei ticket indicati nel piano di rilascio: SIUT-SIES-PR-1.0-20200424-Piano di rilascio SIES.pdf
## Acronimi e Definizioni
### Acronimi
| Sigla | Descrizione |
| --- | --- |
| AgID | Agenzia per l’Italia Digitale |
| API | Application Programming Interface |
| CPU | Central Processing Unit |
| CV | Curriculum Vitae |
| DB | Data Base |
| DEC | Direttore Esecutivo Contratto |
| DGSIA | Direzione Generale per o Sistemi Informativi Automatizzati |
| DR | Disaster Recovery |
| ETSI | European Telecommunications Standards Institute |
| FP | Function Point |
| GDPR | General Data Protection Regulation |
| HW | HardWare |
| ICT | Information & Communication Technology |
| ISO | International Organization for Standardization |
| ISP | Information Security Policy |
| IT | Information Technology |
| KPI | Key Performance Indicator |
| MAAC | Mandatory Access Control |
| MAC | MAnutenzione Correttiva |
| MEV | Manutenzione EVolutiva |
| OSWAP | Open Web Application Security Project |
| PA | Pubblica Amministrazione |
| PEC | Posta Elettronica Certificata |
| PDCA | Plan, Do, Check, Act |
| PdQ | Piano della Qualità |
| PdP | Piano di Progetto |
| PdS | Piano della Sicurezza |
| QM | Quality Manager |
| RA | Risk Assessment |
| RID | Riservatezza, Integrità, Disponibilità |
| RM | Resource Manager |
| RPO | Recovery Point Objective |
| RTO | Recovery Time Objective |
| RTI | Raggruppamento Temporaneo di Impresa Engineering – Sirfin-PA |
| RUF | Responsabile Unico Fornitore |
| RUP | Responsabile unico Progetto |
| SAL | Stato Avanzamento Lavori |
| SGQ | Sistema di Gestione per la Qualità di Engineering Ingegneria Informatica S.p.A. |
| SGSI | Sistema di Gestione della Sicurezza Informatica |
| SICP | Sistema Informativo Cognizione Penale |
| SIU | Sistema Informativo Unitario |
| SLA | Service Level Agreement |
| SM | Security Manager |
| SQL | Structured Query Language |
| SW | SoftWare |
| TT | Trouble Ticketing |
| VPN | Virtual Private Network |

### Definizioni
| Glossa | Sinonimo | Definizione |
| --- | --- | --- |
|  |  |  |
|  |  |  |
|  |  |  |


## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF1 | SIUT-SIES-PR-1.0-20200424-Piano di rilascio SIES.pdf | Il documento riporta l’elenco delle funzionalità modificate con gli interventi eseguiti dal servizio di manutenzione rilasciati con il presente rilascio.
Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio. |
| RIF2 | SIUT-SIES-CT-1.0-20200424-Allegato-al-piano-test.xls | Il documento riporta l'elenco dei test eseguiti per la verifica della risoluzione delle anomalie |


# Obiettivi e portata dei test
## Descrizione delle scelte nella definizione dei test
### Entità da testare
L'entità oggetto di verifica è l'applicativo SIES relativamente alle funzionalità oggetto dei ticket indicati nel piano di rilascio “SIUT-SIES-PR-1.0-20200424-Piano di rilascio SIES.pdf”.
### Entità escluse dal test
Sono oggetto di verifica esclusivamente i casi di test consegnati.
# Esecuzione dei test
Nell’ottica di garantire la completezza dei test sono stati eseguiti test di validità delle singole funzioni realizzate.
# Documentazione esecuzione test
I test sono eseguiti secondo quanto descritto nella relativa scheda contenuta nel documento “SIUT-SIES-CT-1.0-20200424-Allegato-al-piano-test.xls”. In particolare é stata compilata la colonna ‘Esito’ per indicare l'esito del test.
# Gestione delle anomalie e ripetizione dei test
NA

# Ambiente di test
Per l'esecuzione dei test è stata installata la versione 12.2.0 di SIES secondo quanto stabilito dal documento di rilascio.
# Strumenti
## Database dei casi di prova
NA
## Strumenti automatici di supporto ai test
NA
# Specifica Test
## Descrizione dei Casi di Test
La descrizione di dettaglio di ciascun caso di test è contenuta nel documento “SIUT-SIES-CT-1.0-20200424-Allegato-al-piano-test.xls” a complemento del presente piano dei test.
In particolare:
nella ‘Tabella dei test’ è contenuta la tracciatura a partire dalla segnalazione OTRS fino al singolo caso di test;
nelle ‘Specifiche di test’ ogni caso di test è dettagliato in termini procedurali.