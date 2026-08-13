---
uniqueName: siut-sies-pt-1-0-20230707-pianodeitest202338riform
displayName: "SIUT SIES PT 1 0 20230707 Piano dei Test 2023 38 Riforma Cartabia"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PT-1.0-20230707-Piano_dei_Test_2023_38_Riforma_Cartabia

> **File originale:** `MEV/SCHEDA_038/documentazione/SIUT-SIES-PT-1.0-20230707-Piano_dei_Test_2023_38_Riforma_Cartabia.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. - Sirfin-PA, nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del sistema informativo unitario telematico, la manutenzione degli attuali sistemi dell’area penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Engineering | RTI |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi Attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 07/07/2023 |  |
| Livello di riservatezza | L4 |  |

Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 07/07/2023 | Prima Emissione |  |

Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Aurora Garofalo | Amministrazione |  | Responsabile Unico Procedimento |
| Dott. Oris Orlando | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Francesco Rosati | RTI |  | Responsabile Manutenzione Correttiva
Referente Qualità e Sicurezza |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario e Referente Tecnico |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Referente PMO e Qualità |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |


INDICE DEI CONTENUTI
1.	Introduzione	5
1.1.	Scopo del documento	5
1.2.	Riferimenti	5
1.3.	Glossario	5
1.3.1.	Definizioni	5
1.3.2.	Acronimi e abbreviazioni	5
2.	Obiettivi e portata dei test	6
2.1.	Descrizione delle scelte nella definizione dei test	6
2.1.1.	Entità da testare	6
2.1.2.	Entità escluse dal test	6
3.	Esecuzione dei test	7
4.	Documentazione esecuzione test	8
5.	Gestione delle anomalie e ripetizione dei test	9
6.	Ambiente di test	10
7.	Configurazione ambiente	11
7.1.	Configurazione hw e sw	11
7.2.	Sistemi esterni	11
7.3.	Vincoli tecnici ed organizzativi	11
8.	Strumenti	12
8.1.	Database dei casi di prova	12
8.2.	Strumenti automatici di supporto ai test	12
9.	Specifica Test	13
9.1.	Descrizione dei Casi di Test	13


# Introduzione
## Scopo del documento
Il presente documento descrive l’elenco delle funzionalità oggetto di verifica.
## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF.1 | SIUT-SIES-PR-1.0-20230707-Piano_di_Rilascio_2023_38_Riforma_Cartabia.pdf | Il documento riporta l’elenco delle applicazioni oggetto del presente rilascio. Riporta inoltre le modalità di installazione delle varie componenti in ambiente di esercizio. |
| RIF.2 | SIUT-SIE-CT-1.0-20230707-Allegato_al_piano_test_2023_38_Riforma_Cartabia.xlsx | Elenco del piano dei test da eseguire per la verifica di conformità |

## Glossario
## Definizioni
| Definizione | Descrizione |
| --- | --- |
|  |  |

## Acronimi e abbreviazioni
| Sigla | Descrizione |
| --- | --- |
|  |  |


# Obiettivi e portata dei test
Per l’applicativo SIES sono stati definiti i casi di test che permettono di verificarne il corretto funzionamento secondo le regole funzionali.
## Descrizione delle scelte nella definizione dei test
## Entità da testare
L'entità oggetto di verifica è l'applicativo SIES relativamente alle funzionalità oggetto dei vari template.
## Entità escluse dal test
Sono oggetto di verifica esclusivamente i casi di test consegnati.
# Esecuzione dei test
I test si svolgono nell’ambiente di collaudo dell’Amministrazione secondo le modalità indicate nel piano di test e così come dettagliato nel documento SIUT-SIE-CT-1.0-20230707-Allegato_al_piano_test_2023_38_Riforma_Cartabia.xlsx [RIF.2].
# Documentazione esecuzione test
L’esito dei test sarà indicato nella colonna predisposta, con descrizione ‘Esito’, all’interno del documento SIUT-SIE-CT-1.0-20230707-Allegato_al_piano_test_2023_38_Riforma_Cartabia.xlsx [RIF.2].

In caso di esito positivo del test, la colonna ‘Esito’ riporterà la dicitura ‘OK’.
In caso di esito negativo, si rimanda al paragrafo successivo per le indicazioni circa il comportamento da seguire.
# Gestione delle anomalie e ripetizione dei test
Di seguito l’indicazione circa le modalità di esecuzione dei test in base all’esito di ciascuno:
Se l’esito del test è positivo, procedere con il test successivo;
Se l’esito è negativo, registrare l’anomalia a cui associare il livello di gravità (bloccante, grave, non grave);
Se l’anomalia è di gravità bloccante, sospendere i test del servizio in corso proseguendo eventualmente con il test successivo ripartendo dal punto 1);
Dopo la correzione delle anomalie riscontrate, rieseguire tutti i test nuovamente fino all’esito positivo di tutti.

# Ambiente di test
Nell’ambiente di esecuzione dei test sono presenti tutti i moduli software e tutti gli adeguamenti della base dati volti alla soddisfazione dei requisiti richiesti.
# Configurazione ambiente
## Configurazione hw e sw
Fare riferimento al documento SIUT-SIES-PR-1.0-20230707-Piano_di_Rilascio_2023_38_Riforma_Cartabia.pdf [RIF.1].
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
La descrizione di dettaglio di ciascun caso di test è contenuta nel documento Allegato al Piano dei Test [RIF.2] a completamento del presente.
In particolare:
Nella ‘Tabella dei test’ è contenuta la tracciatura a partire dai requisiti utente fino al singolo caso di test;
Nelle ‘Specifiche di test’ ogni caso di test è dettagliato in termini procedurali.