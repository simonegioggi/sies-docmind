---
uniqueName: siut-sie-pt-1-1-20210323-pianodeitestsies-adn
displayName: "SIUT SIE PT 1 1 20210323 Piano dei Test SIES ADN"
category: "GENERAL"
tags: []
---

# SIUT-SIE-PT-1.1-20210323-Piano_dei_Test_SIES-ADN

> **File originale:** `MEV/Integrazione SIES-ADN/DOCS/UNUSED/SIUT-SIE-PT-1.1-20210323-Piano_dei_Test_SIES-ADN.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
Piano dei Test 
Integrazione SIES-ADN 
 
 
 
 
 
 
 
 
 
Versione 1.1 del 23/03/2021

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.1-20210323-Piano_dei_Test_SIES-ADN 
Ver.1.1 del 23/03/2021 
Pag.2/13 
 
 
 
Il 
presente 
documento 
è 
stato 
redatto 
con 
la 
collaborazione 
del 
RTI 
Engineering 
Ingegneria 
Informatica S.p.A - Sirfin-PA, nell’ambito del contratto 
CIG 73479643B7 
per 
lo 
“Sviluppo 
del 
sistema 
informativo unitario telematico, la manutenzione degli 
attuali sistemi dell’area penale del Ministero della 
Giustizia e servizi correlati. Lotto 1”.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.1-20210323-Piano_dei_Test_SIES-ADN 
Ver.1.1 del 23/03/2021 
Pag.3/13 
Approvazioni 
 
Nominativo 
Funzione 
Elaborato da 
Domenico Nania 
Analista Funzionale 
Verificato da 
Vito Bufi 
Responsabile Manutenzione Sistemi Attuali 
Approvato da 
Paolo Ceccanti 
Responsabile Unico Fornitura 
Data approvazione 
23/03/2021 
 
Livello di riservatezza 
L3 
 
 
Elenco versioni 
Versione 
Data  
Motivo 
Modifica 
1.0 
12/03/2021 
Prima Emissione 
 
1.1 
23/03/2021 
Seconda Emissione 
Aggiunti altri casi di test a seguito di alcune osservazioni 
da parte di DGSIA 
 
Lista di distribuzione 
Nominativo 
Organizzazione 
Ufficio 
Funzione 
Ing. Giovanni Malesci 
Amministrazione 
 
Responsabile Unico Procedimento 
Dr.ssa Annamaria Palmieri 
Amministrazione 
 
Direttore Esecutivo Contratto 
Paolo Ceccanti 
RTI 
 
Responsabile Unico Fornitura 
Salvatore Piazza 
RTI 
 
Technical Manager 
Sergio Tamburrini 
RTI 
 
Organization Manager 
Vito Bufi 
RTI 
 
Responsabile Manutenzione Sistemi attuali 
Fabio Mazzocchi 
RTI 
 
Responsabile Manutenzione Correttiva 
Andrea Salvaggio 
RTI 
 
Responsabile Progetto Sistema Unitario 
Antonio Iacobelli 
RTI 
 
Responsabile Supporto Specialistico 
Antonella Damiani 
RTI 
 
Responsabile Centro di Competenza 
Fabio Gattamorta 
RTI 
 
Referente PMO e Qualità 
Alessandro Falleni 
RTI 
 
Referente Sicurezza 
Francesco Rosati 
RTI 
 
Referente Qualità e Sicurezza 
Andrea Castorino 
RTI 
 
Referente Applicativo Gestore Fascicolo 
Documentale 
Luigi Buglione 
RTI 
 
Referente Metrico

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.1-20210323-Piano_dei_Test_SIES-ADN 
Ver.1.1 del 23/03/2021 
Pag.4/13 
INDICE DEI CONTENUTI 
1. 
INTRODUZIONE .................................................................................................................................... 5 
1.1. 
SCOPO DEL DOCUMENTO ................................................................................................................................ 5 
1.2. 
RIFERIMENTI ................................................................................................................................................. 5 
1.3. 
GLOSSARIO ................................................................................................................................................... 5 
1.3.1. 
DEFINIZIONI .............................................................................................................................................. 5 
1.3.2. 
ACRONIMI E ABBREVIAZIONI ........................................................................................................................ 5 
2. 
OBIETTIVI E PORTATA DEI TEST ............................................................................................................. 6 
2.1. 
DESCRIZIONE DELLE SCELTE NELLA DEFINIZIONE DEI TEST ....................................................................................... 6 
2.1.1. 
ENTITÀ DA TESTARE .................................................................................................................................... 6 
2.1.2. 
ENTITÀ ESCLUSE DAL TEST ............................................................................................................................ 6 
3. 
ESECUZIONE DEI TEST ........................................................................................................................... 7 
4. 
DOCUMENTAZIONE ESECUZIONE TEST .................................................................................................. 8 
5. 
GESTIONE DELLE ANOMALIE E RIPETIZIONE DEI TEST ............................................................................. 9 
6. 
AMBIENTE DI TEST .............................................................................................................................. 10 
7. 
CONFIGURAZIONE AMBIENTE ............................................................................................................. 11 
7.1. 
CONFIGURAZIONE HW E SW ........................................................................................................................... 11 
7.2. 
SISTEMI ESTERNI .......................................................................................................................................... 11 
7.3. 
VINCOLI TECNICI ED ORGANIZZATIVI ................................................................................................................ 11 
8. 
STRUMENTI ........................................................................................................................................ 12 
8.1. 
DATABASE DEI CASI DI PROVA ........................................................................................................................ 12 
8.2. 
STRUMENTI AUTOMATICI DI SUPPORTO AI TEST ................................................................................................. 12 
9. 
SPECIFICA TEST ................................................................................................................................... 13 
9.1. 
DESCRIZIONE DEI CASI DI TEST ....................................................................................................................... 13

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.1-20210323-Piano_dei_Test_SIES-ADN 
Ver.1.1 del 23/03/2021 
Pag.5/13 
1. Introduzione 
1.1. Scopo del documento 
Il presente documento descrive l’elenco delle funzionalità oggetto di verifica, a valle dell’intervento di 
integrazione delle attività previste nella scheda SIUT-SIC-SC-1.0-20200924-Scheda intervento 
Scheda_n.3_2019 Sostituzione IGI.pdf [RIF.1]. 
In particolare, si è delineata la necessità di intervenire, con ulteriori implementazioni, rispetto a 
quanto previsto nella scheda sia sul SIC che su altri applicativi ‘satelliti’ del SIC che attualmente si 
poggiano sulle funzioni di autenticazione e profilazione ‘offerte’ dall’appliance IGI. 
1.2. Riferimenti 
Riferimento 
Nome Documento 
Descrizione Documento 
RIF.1 
SIUT-SIC-SC-1.0-20200924-Scheda 
intervento 
Scheda_n.3_2019 Sostituzione IGI.pdf  
Scheda di Intervento  
RIF.2 
SIUT-SIC-SC-1.0-20210108 
Scheda 
intervento 
Integrazione SIC-ADN.pdf 
Integrazione Scheda di intervento. 
RIF.3 
SIUT-SIE-PR-1.1-20210323-Piano_di_Rilascio_SIES-
ADN.doc 
Il documento riporta l’elenco delle applicazioni 
oggetto del presente rilascio. Riporta inoltre le 
modalità 
di 
installazione 
delle 
varie 
componenti in ambiente di esercizio. 
RIF.4 
SIUT-SIE-CT-1.1-20210323-Allegato-al-piano-
test_SIES-ADN.xls 
Elenco del piano dei test da eseguire per la 
verifica di conformità 
 
1.3. Glossario 
1.3.1. Definizioni 
Definizione 
Descrizione 
 
 
1.3.2. Acronimi e abbreviazioni 
Sigla 
Descrizione

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.1-20210323-Piano_dei_Test_SIES-ADN 
Ver.1.1 del 23/03/2021 
Pag.6/13 
2. Obiettivi e portata dei test 
Per il requisito riguardante l’applicativo SIES sono stati definiti i casi di test che permettono di 
verificarne il corretto funzionamento secondo le regole funzionali. 
2.1. Descrizione delle scelte nella definizione dei test 
2.1.1. Entità da testare 
L'entità oggetto di verifica è l'applicativo SIES relativamente alle funzionalità oggetto dell’integrazione 
[Rif.2]. 
2.1.2. Entità escluse dal test 
Sono oggetto di verifica esclusivamente i casi di test consegnati.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.1-20210323-Piano_dei_Test_SIES-ADN 
Ver.1.1 del 23/03/2021 
Pag.7/13 
3. Esecuzione dei test 
I test si svolgono nell’ambiente di collaudo dell’Amministrazione secondo le modalità indicate nel 
piano di test e così come dettagliato nel documento SIUT-SIE-CT-1.1-20210323-Allegato-al piano-
test_SIES-ADN.xls [RIF.4].

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.1-20210323-Piano_dei_Test_SIES-ADN 
Ver.1.1 del 23/03/2021 
Pag.8/13 
4. Documentazione esecuzione test 
L’esito dei test sarà indicato nella colonna predisposta, con descrizione ‘Esito’, all’interno del 
documento SIUT-SIE-CT-1.1-20210323-Allegato-al piano-test_SIES-ADN.xls [RIF.4]. 
 
In caso di esito positivo del test, la colonna ‘Esito’ riporterà la dicitura ‘OK’. 
In caso di esito negativo, si rimanda al paragrafo successivo per le indicazioni circa il comportamento 
da seguire.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.1-20210323-Piano_dei_Test_SIES-ADN 
Ver.1.1 del 23/03/2021 
Pag.9/13 
5. Gestione delle anomalie e ripetizione dei test 
Di seguito l’indicazione circa le modalità di esecuzione dei test in base all’esito di ciascuno: 
• Se l’esito del test è positivo, procedere con il test successivo; 
• Se l’esito è negativo, registrare l’anomalia a cui associare il livello di gravità (bloccante, grave, 
non grave); 
• Se l’anomalia è di gravità bloccante, sospendere i test del servizio in corso proseguendo 
eventualmente con il test successivo ripartendo dal punto 1); 
• Dopo la correzione delle anomalie riscontrate, rieseguire tutti i test nuovamente fino all’esito 
positivo di tutti.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.1-20210323-Piano_dei_Test_SIES-ADN 
Ver.1.1 del 23/03/2021 
Pag.10/13 
6. Ambiente di test 
Nell’ambiente di esecuzione dei test sono presenti tutti i moduli software e tutti gli adeguamenti 
della base dati volti alla soddisfazione dei requisiti richiesti.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.1-20210323-Piano_dei_Test_SIES-ADN 
Ver.1.1 del 23/03/2021 
Pag.11/13 
7. Configurazione ambiente 
7.1. Configurazione hw e sw 
Fare riferimento al documento SIUT-SIC-SC-1.0-20210108 Scheda intervento Integrazione SIC-
ADN.pdf [RIF.2] e SIUT-SIE-PR-1.1-20210323-Piano_di_rilascio_SIES-ADN.pdf [RIF.3]. 
7.2. Sistemi esterni 
N.A. 
7.3. Vincoli tecnici ed organizzativi 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.1-20210323-Piano_dei_Test_SIES-ADN 
Ver.1.1 del 23/03/2021 
Pag.12/13 
8. Strumenti 
8.1. Database dei casi di prova 
N.A. 
8.2. Strumenti automatici di supporto ai test 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.1-20210323-Piano_dei_Test_SIES-ADN 
Ver.1.1 del 23/03/2021 
Pag.13/13 
9. Specifica Test 
9.1. Descrizione dei Casi di Test 
La descrizione di dettaglio di ciascun caso di test è contenuta nel documento Allegato al Piano dei 
Test [RIF.4] a completamento del presente. 
In particolare: 
• Nella ‘Tabella dei test’ è contenuta la tracciatura a partire dai requisiti utente fino al singolo 
caso di test; 
• Nelle ‘Specifiche di test’ ogni caso di test è dettagliato in termini procedurali.