---
uniqueName: a05bcbfd00-2024-051-020241031-pianodeitestsiusrifo
displayName: "A05BCBFD00 2024 05 1 0 20241031 Piano dei Test SIUS Riforma Cartabia"
category: "GENERAL"
tags: []
---

# A05BCBFD00-2024-05_1.0_20241031-Piano_dei_Test_SIUS_Riforma_Cartabia

> **File originale:** `MEV/SCHEDA_035/ORIGINALI X NUOVO CONTRATTO/A05BCBFD00-2024-05_1.0_20241031-Piano_dei_Test_SIUS_Riforma_Cartabia.docx`  
> **Tipo:** DOCX

---

|  |
| --- |
|  |





Approvazioni
|  | Nominativo |
| --- | --- |
| Elaborato da | Engineering |
| Verificato da | Vito Bufi |
| Approvato da | Paolo Ceccanti |
| Data approvazione | 31/10/2024 |
| Livello di riservatezza | L4 |

Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 31/10/2024 | Prima Emissione |  |

Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Aurora Garofalo | Amministrazione |  | Responsabile Unico Procedimento |
| Dott. Oris Orlando | Amministrazione |  | Direttore Esecutivo Contratto |
| Michele D’Alessandro | RTI - Accenture |  | Responsabile Unico Fornitura |


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
Il presente documento descrive l’elenco delle funzionalità oggetto di verifica, a valle delle attività previste nel documento Specifiche_Intervento_MEV_2024_05_SIUS_Riforma_Cartabia.pdf [RIF.1].
## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF.1 | Specifiche_Intervento_MEV_2024_05_SIUS_Riforma_Cartabia.pdf | Specifiche di Intervento |
| RIF.2 | Piano_di_Rilascio_2024_05_SIUS_Riforma_Cartabia.pdf | Il documento riporta l’elenco delle applicazioni oggetto del presente rilascio. Riporta inoltre le modalità di installazione delle varie componenti in ambiente di esercizio. |
| RIF.3 | Allegato_al_piano_Test_2024_05_SIUS_Riforma_Cartabia.xlsx | Elenco del piano dei test da eseguire per la verifica di conformità |

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
L'entità oggetto di verifica è l'applicativo SIES relativamente alle funzionalità oggetto delle Specifiche Funzionali [Rif.1].
## Entità escluse dal test
Sono oggetto di verifica esclusivamente i casi di test consegnati.
# Esecuzione dei test
I test si svolgono nell’ambiente di collaudo dell’Amministrazione secondo le modalità indicate nel piano di test e così come dettagliato nel documento Allegato_al_piano_Test_2024_05_SIUS_Riforma_Cartabia.xlsx [RIF.3].
# Documentazione esecuzione test
L’esito dei test sarà indicato nella colonna predisposta, con descrizione ‘Esito’, all’interno del documento Allegato_al_piano_Test_2024_05_SIUS_Riforma_Cartabia.xlsx [RIF.3].

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
Fare riferimento al documento Specifiche_Intervento_MEV_2024_05_SIUS_Riforma_Cartabia.pdf [RIF.1] e Piano_di_Rilascio_2024_05_SIUS_Riforma_Cartabia.pdf [RIF.2].
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
La descrizione di dettaglio di ciascun caso di test è contenuta nel documento Allegato al Piano dei Test [RIF.3] a completamento del presente.
In particolare:
Nella ‘Tabella dei test’ è contenuta la tracciatura a partire dai requisiti utente fino al singolo caso di test;
Nelle ‘Specifiche di test’ ogni caso di test è dettagliato in termini procedurali.