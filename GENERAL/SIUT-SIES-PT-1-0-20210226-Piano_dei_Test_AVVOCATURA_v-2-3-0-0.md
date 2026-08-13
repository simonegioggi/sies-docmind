---
uniqueName: siut-sies-pt-1-0-20210226-pianodeitestavvocaturav-
displayName: "SIUT SIES PT 1 0 20210226 Piano dei Test AVVOCATURA v 2 3 0 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PT-1.0-20210226-Piano_dei_Test_AVVOCATURA_v.2.3.0.0

> **File originale:** `Avvocatura-SIES/RILASCIO_2.3.0.0/SIUT-SIES-PT-1.0-20210226-Piano_dei_Test_AVVOCATURA_v.2.3.0.0.docx`  
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
| Data approvazione | 26/02/2021 |  |
| Livello di riservatezza | L3 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 26/02/2021 | Prima Emissione |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Salvatore Piazza | RTI |  | Technical Manager |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Fabio Mazzocchi | RTI |  | Responsabile Manutenzione Correttiva |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Referente PMO e Qualità |
| Alessandro Falleni | RTI |  | Referente Sicurezza |
| Francesco Rosati | RTI |  | Referente Qualità e Sicurezza |
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
Il presente documento descrive il piano dei test per la verifica della risoluzione dei ticket indicati nel piano di rilascio: SIUT-SIES-PR-1.0-20210212-Piano_di_Rilascio_AVVOCATURA_v.2.3.0.0.doc.
## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF1 | SIUT-SIES-PR-1.0-20210226-Piano_di_Rilascio_AVVOCATURA_v.2.3.0.0.doc | Il documento riporta l’elenco delle funzionalità modificate con gli interventi eseguiti dal servizio di manutenzione forniti con il presente rilascio.
Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio. |
| RIF2 | SIUT-SIES-CT-1.0-20210226-Allegato_al_piano_test_AVVOCATURA_v.2.3.0.0.xls | Il documento riporta l'elenco dei test eseguiti per la verifica della risoluzione delle anomalie. |


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
L'entità oggetto di verifica è l'applicativo AVVOCATURA relativamente alle funzionalità oggetto dei ticket indicati nel piano di rilascio SIUT-SIES-PR-1.0-20210226-Piano_di_Rilascio_AVVOCATURA_v.2.3.0.0.doc.
## Entità escluse dal test
Sono oggetto di verifica esclusivamente i casi di test consegnati.
# Esecuzione dei test
Nell’ottica di garantire la completezza dei test sono stati eseguiti test di validità delle singole funzioni realizzate.
# Documentazione esecuzione test
I test sono eseguiti secondo quanto descritto nella relativa scheda contenuta nel documento SIUT-SIES-CT-1.0-20210226-Allegato-al-piano-test_AVVOCATURA_v.2.3.0.0.xls. In particolare, è stata compilata la colonna ‘Esito’ per indicare l'esito del test.
# Gestione delle anomalie e ripetizione dei test
N.A.

# Ambiente di test
Per l'esecuzione dei test è stata installata la versione 2.3.0.0 di AVVOCATURA secondo quanto stabilito dal documento di rilascio.
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
La descrizione di dettaglio di ciascun caso di test è contenuta nel documento SIUT-SIES-CT-1.0-20210226-Allegato_al_piano_test_AVVOCATURA_v.2.3.0.0.xls a complemento del presente piano dei test.
In particolare:
nella ‘Tabella dei test’ è contenuta la tracciatura a partire dalla segnalazione OTRS fino al singolo caso di test;
nelle ‘Specifiche di test’ ogni caso di test è dettagliato in termini procedurali.