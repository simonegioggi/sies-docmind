---
uniqueName: b6437aaaeb-2025-48pnrrpianodeitestevolutivedisiesv
displayName: "B6437AAAEB 2025 48 PNRR Piano dei Test Evolutive di SIES v1 0"
category: "GENERAL"
tags: []
---

# B6437AAAEB-2025-48_PNRR_Piano_dei_Test_Evolutive_di_SIES_v1.0

> **File originale:** `MEV/SCHEDA_48/B6437AAAEB-2025-48_PNRR_Piano_dei_Test_Evolutive_di_SIES_v1.0.docx`  
> **Tipo:** DOCX

---


Ministero della Giustizia
Dipartimento per l’innovazione tecnologica della giustizia

PIANO DEI TEST
INTERVENTI EVOLUTIVI SULL’APPLICAZIONE SIES

| Prospetto Informativo Sintetico | Prospetto Informativo Sintetico |
| --- | --- |
| INTERVENTO | Interventi evolutivi sull’applicazione SIES |
| CONTRATTO DI RIFERIMENTO | Accordo Quadro per l’affidamento di servizi applicativi in ottica cloud e l’affidamento di servizi di demand e PMO per le pubbliche amministrazioni centrali ID 2483 – Seconda Edizione - Lotto 1 – Digitalizzazione Area Penale – CIG B6437AAAEB |
| Milestone PNRR | M1C1-38 bis 
Interventi già programmati per il 2024 su sistemi complementari ad APP per la digitalizzazione del processo penale di primo grado (B2) |
| CICLO DI VITA | Ridotto |
| DOCUMENTO | Piano dei Test: B6437AAAEB_2025_48 |
| FILE | B6437AAAEB-2025-48_PNNR_Piano_dei_Test_Evolutive_di_SIES_v1.0 |
| DATA DOCUMENTO | 22/12/2025 |
| FORNITORE | RTI - Accenture |

l
| Elenco versioni | Elenco versioni |
| --- | --- |
| v1 | Prima emissione |


| Referenti | Referenti |
| --- | --- |
| Nominativo | Organizzazione |
| Oris Orlando | DEC - DGSAP |
| Marta Nicoletti Altimari | RUP – DGSAP |
| Michele D’Alessandro | RUAC - RTI Accenture |



Indice
1.	Premessa	3
2.	Obiettivi e portata dei test	4
2.1.	Descrizione delle scelte nella definizione dei test	4
2.1.1.	Entità da testare	4
2.1.2.	Entità escluse dal test	4
3.	Esecuzione dei test	5
4.	Documentazione esecuzione test	6
5.	Gestione delle anomalie e ripetizione dei test	7
6.	Ambiente di test	8
7.	Configurazione ambiente	9
7.1.	Configurazione hw e sw	9
7.2.	Sistemi esterni	9
7.3.	Vincoli tecnici ed organizzativi	9
8.	Strumenti	10
8.1.	Database dei casi di prova	10
8.2.	Strumenti automatici di supporto ai test	10
9.	Specifica Test	11
9.1.	Descrizione dei Casi di Test	11


# Premessa
Il presente documento descrive l’elenco delle funzionalità oggetto di verifica, a valle delle attività previste nel documento B6437AAAEB-2025-48_PNRR_Scheda_Intervento_Evolutive_di_SIES_v1.0.pdf.
# Obiettivi e portata dei test
Per l’applicativo SIES sono stati definiti i casi di test che permettono di verificarne il corretto funzionamento secondo le regole funzionali.
## Descrizione delle scelte nella definizione dei test
## Entità da testare
L'entità oggetto di verifica è l'applicativo SIES relativamente alle funzionalità oggetto delle Specifiche Funzionali.
## Entità escluse dal test
Sono oggetto di verifica esclusivamente i casi di test consegnati.
# Esecuzione dei test
I test si svolgono nell’ambiente di collaudo dell’Amministrazione secondo le modalità indicate nel piano di test e così come dettagliato nel documento B6437AAAEB-2025-48_PNRR_Allegato_al_Piano_dei_Test_Evolutive_di_SIES_v1.0.xlsx.
# Documentazione esecuzione test
L’esito dei test sarà indicato nella colonna predisposta, con descrizione ‘Esito’, all’interno del documento B6437AAAEB-2025-48_PNRR_Allegato_al_Piano_dei_Test_Evolutive_di_SIES_v1.0.xlsx.

In caso di esito positivo del test, la colonna ‘Esito’ riporterà la dicitura ‘OK’.
In caso di esito negativo, si rimanda al paragrafo successivo per le indicazioni circa il comportamento da seguire.
# Gestione delle anomalie e ripetizione dei test
Di seguito l’indicazione circa le modalità di esecuzione dei test in base all’esito di ciascuno:
se l’esito del test è positivo, procedere con il test successivo;
se l’esito è negativo, registrare l’anomalia a cui associare il livello di gravità (bloccante, grave, non grave);
se l’anomalia è di gravità bloccante, sospendere i test del servizio in corso proseguendo eventualmente con il test successivo ripartendo dal punto 1);
dopo la correzione delle anomalie riscontrate, rieseguire tutti i test nuovamente fino all’esito positivo di tutti.

# Ambiente di test
Nell’ambiente di esecuzione dei test sono presenti tutti i moduli software e tutti gli adeguamenti della base dati volti alla soddisfazione dei requisiti richiesti.
# Configurazione ambiente
## Configurazione hw e sw
Fare riferimento al documento B6437AAAEB-2025-48_PNRR_Scheda_Intervento_Evolutive_di_SIES_v1.0.pdf e B6437AAAEB-2025-48_PNRR_Piano_di_Rilascio_Evolutive_di_SIES_v1.0.pdf.
## Sistemi esterni
N.A.
## Vincoli tecnici ed organizzativi
N.A.
# Strumenti
## Database dei casi di prova
N.A.
## Strumenti automatici di supporto ai test
N.A.
# Specifica Test
## Descrizione dei Casi di Test
La descrizione di dettaglio di ciascun caso di test è contenuta nel documento Allegato al Piano dei Test a completamento del presente.
In particolare:
Nella ‘Tabella dei test’ è contenuta la tracciatura a partire dai requisiti utente fino al singolo caso di test;
Nelle ‘Specifiche di test’ ogni caso di test è dettagliato in termini procedurali.