---
uniqueName: siut-sies-pt-1-0-20210924-pianodeitestsiesv-12-4-1
displayName: "SIUT SIES PT 1 0 20210924 Piano dei Test SIES v 12 4 13 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PT-1.0-20210924-Piano_dei_Test_SIES_v.12.4.13.0

> **File originale:** `RILASCIO_12.4.13.0/SIUT-SIES-PT-1.0-20210924-Piano_dei_Test_SIES_v.12.4.13.0.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A - Sirfin-PA, nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del sistema informativo unitario telematico, la manutenzione degli attuali sistemi dell’area penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Domenico Nania | Analista Funzionale |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi Attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 24/09/2021 |  |
| Livello di riservatezza | L3 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 24/09/2021 | Prima Emissione |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Francesco Rosati | RTI |  | Responsabile Manutenzione Correttiva
Referente Qualità e Sicurezza |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario e Referente Tecnico |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Referente PMO e Qualità |
| Alessandro Falleni | RTI |  | Referente Sicurezza |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |
| Luigi Buglione | RTI |  | Referente Metrico |


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
Il presente documento descrive il piano dei test per la verifica della risoluzione dei ticket indicati nel piano di rilascio: SIUT-SIES-PR-1.0-20210924-Piano_di_Rilascio_SIES_v.12.4.13.0.docx.
## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF1 | SIUT-SIES-PR-1.0-20210924-Piano_di_Rilascio_SIES_v.12.4.13.0.docx | Il documento riporta l’elenco delle funzionalità modificate con gli interventi eseguiti dal servizio di manutenzione forniti con il presente rilascio.
Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio. |
| RIF2 | SIUT-SIES-CT-1.0-20210924-Allegato-al-piano-test_SIES_v.12.4.13.0.xls | Il documento riporta l'elenco dei test eseguiti per la verifica della risoluzione delle anomalie |


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
## Descrizione delle scelte nella definizione dei test
## Entità da testare
L'entità oggetto di verifica è l'applicativo SIES relativamente alle funzionalità oggetto dei ticket indicati nel piano di rilascio SIUT-SIES-PR-1.0-20210924-Piano_di_Rilascio_SIES_v.12.4.13.0.docx. In particolare, per il ticket 20210825016 è propedeutico aver eseguito anche il piano di rilascio SIUT-SIC-PR-1.0-20210924-Piano_di_Rilascio_SIPPI_v.9.8.1.0.docx.
## Entità escluse dal test
Sono oggetto di verifica esclusivamente i casi di test consegnati.
# Esecuzione dei test
Nell’ottica di garantire la completezza dei test sono stati eseguiti test di validità delle singole funzioni realizzate.
# Documentazione esecuzione test
I test sono eseguiti secondo quanto descritto nella relativa scheda contenuta nel documento SIUT-SIES-CT-1.0-20210924-Allegato-al-piano-test_SIES_v.12.4.13.0.xls. In particolare, è stata compilata la colonna ‘Esito’ per indicare l'esito del test.
# Gestione delle anomalie e ripetizione dei test
N.A.

# Ambiente di test
Per l'esecuzione dei test è stata installata la versione 12.4.13.0 di SIES secondo quanto stabilito dal documento di rilascio.
# Configurazione ambiente
## Configurazione hw e sw
N.A.
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
La descrizione di dettaglio di ciascun caso di test è contenuta nel documento SIUT-SIES-CT-1.0-20210924-Allegato-al-piano-test_SIES_v.12.4.13.0.xls a complemento del presente piano dei test.
In particolare:
nella ‘Tabella dei test’ è contenuta la tracciatura a partire dalla segnalazione OTRS fino al singolo caso di test;
nelle ‘Specifiche di test’ ogni caso di test è dettagliato in termini procedurali.