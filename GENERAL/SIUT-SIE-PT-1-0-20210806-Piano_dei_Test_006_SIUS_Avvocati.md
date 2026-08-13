---
uniqueName: siut-sie-pt-1-0-20210806-pianodeitest006siusavvoca
displayName: "SIUT SIE PT 1 0 20210806 Piano dei Test 006 SIUS Avvocati"
category: "GENERAL"
tags: []
---

# SIUT-SIE-PT-1.0-20210806-Piano_dei_Test_006_SIUS_Avvocati

> **File originale:** `MEV/SCHEDA_006/SIUT-SIE-PT-1.0-20210806-Piano_dei_Test_006_SIUS_Avvocati.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
Piano dei Test 
MEV 2019_006 SIUS Avvocati 
 
 
 
 
 
 
 
 
 
Versione 1.0 del 06/08/2021

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.0-20210806-Piano_dei_Test_006_SIUS_Avvocati 
Ver.1.0 del 06/08/2021 
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
 
 
 SIUT-SIE-PT-1.0-20210806-Piano_dei_Test_006_SIUS_Avvocati 
Ver.1.0 del 06/08/2021 
Pag.3/13 
Approvazioni 
 
Nominativo 
Funzione 
Elaborato da 
Engineering 
RTI 
Verificato da 
Vito Bufi 
Responsabile Manutenzione Sistemi Attuali 
Approvato da 
Paolo Ceccanti 
Responsabile Unico Fornitura 
Data approvazione 
06/08/2021 
 
Livello di riservatezza 
L3 
 
 
Elenco versioni 
Versione 
Data  
Motivo 
Modifica 
1.0 
06/08/2021 
Prima Emissione 
 
 
 
 
 
 
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
Sergio Tamburrini 
RTI 
 
Organization Manager 
Vito Bufi 
RTI 
 
Responsabile Manutenzione Sistemi attuali 
Francesco Rosati 
RTI 
 
Responsabile Manutenzione Correttiva 
Referente Qualità e Sicurezza 
Andrea Salvaggio 
RTI 
 
Responsabile Progetto Sistema Unitario e Referente 
Tecnico 
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
 
Referente sicurezza 
Andrea Castorino 
RTI 
 
Referente Applicativo Gestore Fascicolo Documentale
Luigi Buglione 
RTI 
 
Referente Metrico

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.0-20210806-Piano_dei_Test_006_SIUS_Avvocati 
Ver.1.0 del 06/08/2021 
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
 
 
 SIUT-SIE-PT-1.0-20210806-Piano_dei_Test_006_SIUS_Avvocati 
Ver.1.0 del 06/08/2021 
Pag.5/13 
1. Introduzione 
1.1. Scopo del documento 
Il presente documento descrive l’elenco delle funzionalità oggetto di verifica, a valle delle attività 
previste nella scheda SIUT-GEN-SC-1.1-20191015 Scheda intervento SIUS_Avvocati.pdf [RIF.1] e 
dalle successive analisi dei risultati SIUT-SIAV-PT-1.0-20201020-Analisi dei risultati dei Test di 
Performance del sistema SIES-Avvocatura.pdf [RIF. 2]. 
. 
1.2. Riferimenti 
Riferimento 
Nome Documento 
Descrizione Documento 
RIF.1 
SIUT-GEN-SC-1.1-20191015 
Scheda 
intervento 
SIUS_Avvocati.pdf 
Scheda di Intervento  
RIF.2 
SIUT-SIAV-PT-1.0-20201020-Analisi dei risultati dei 
Test 
di 
Performance 
del 
sistema 
SIES-
Avvocatura.pdf 
Analisi dei Risultati 
RIF.3 
SIUT-SIES-PR-1.0-20210806-
Piano_di_Rilascio_006_SIUS_Avvocati.docx 
Il documento riporta l’elenco delle applicazioni 
oggetto del presente rilascio. Riporta inoltre le 
modalità 
di 
installazione 
delle 
varie 
componenti in ambiente di esercizio. 
RIF.4 
SIUT-SIE-CT-1.0-20210806-
Allegato_al_piano_test_006_SIUS_Avvocati.xlsx 
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
 
 
 SIUT-SIE-PT-1.0-20210806-Piano_dei_Test_006_SIUS_Avvocati 
Ver.1.0 del 06/08/2021 
Pag.6/13 
2. Obiettivi e portata dei test 
Per l’applicativo SIES sono stati definiti i casi di test che permettono di verificarne il corretto 
funzionamento secondo le regole funzionali. 
2.1. Descrizione delle scelte nella definizione dei test 
2.1.1. Entità da testare 
L'entità oggetto di verifica è l'applicativo SIES relativamente alle funzionalità oggetto delle Analisi dei 
Risultati [Rif.2]. 
2.1.2. Entità escluse dal test 
Sono oggetto di verifica esclusivamente i casi di test consegnati.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.0-20210806-Piano_dei_Test_006_SIUS_Avvocati 
Ver.1.0 del 06/08/2021 
Pag.7/13 
3. Esecuzione dei test 
I test si svolgono nell’ambiente di collaudo dell’Amministrazione secondo le modalità indicate nel 
piano 
di 
test 
e 
così 
come 
dettagliato 
nel 
documento 
SIUT-SIE-CT-1.0-20210806-
Allegato_al_piano_test_006_SIUS_Avvocati.xlsx [RIF.4].

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.0-20210806-Piano_dei_Test_006_SIUS_Avvocati 
Ver.1.0 del 06/08/2021 
Pag.8/13 
4. Documentazione esecuzione test 
L’esito dei test sarà indicato nella colonna predisposta, con descrizione ‘Esito’, all’interno del 
documento SIUT-SIE-CT-1.0-20210806-Allegato_al_piano_test_006_SIUS_Avvocati.xlsx [RIF.4]. 
 
In caso di esito positivo del test, la colonna ‘Esito’ riporterà la dicitura ‘OK’. 
In caso di esito negativo, si rimanda al paragrafo successivo per le indicazioni circa il comportamento 
da seguire.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.0-20210806-Piano_dei_Test_006_SIUS_Avvocati 
Ver.1.0 del 06/08/2021 
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
 
 
 SIUT-SIE-PT-1.0-20210806-Piano_dei_Test_006_SIUS_Avvocati 
Ver.1.0 del 06/08/2021 
Pag.10/13 
6. Ambiente di test 
Nell’ambiente di esecuzione dei test sono presenti tutti i moduli software e tutti gli adeguamenti 
della base dati volti alla soddisfazione dei requisiti richiesti.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.0-20210806-Piano_dei_Test_006_SIUS_Avvocati 
Ver.1.0 del 06/08/2021 
Pag.11/13 
7. Configurazione ambiente 
7.1. Configurazione hw e sw 
Fare riferimento al documento SIUT-SIAV-PT-1.0-20201020-Analisi dei risultati dei Test di 
Performance 
del 
sistema 
SIES-Avvocatura.pdf 
[RIF.2] 
e 
SIUT-SIES-PR-1.0-20210806-
Piano_di_Rilascio_006_SIUS_Avvocati.docx [RIF.3]. 
7.2. Sistemi esterni 
N.A. 
7.3. Vincoli tecnici ed organizzativi 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.0-20210806-Piano_dei_Test_006_SIUS_Avvocati 
Ver.1.0 del 06/08/2021 
Pag.12/13 
8. Strumenti 
8.1. Database dei casi di prova 
N.A. 
8.2. Strumenti automatici di supporto ai test 
N.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 SIUT-SIE-PT-1.0-20210806-Piano_dei_Test_006_SIUS_Avvocati 
Ver.1.0 del 06/08/2021 
Pag.13/13 
9. Specifica Test 
9.1. Descrizione dei Casi di Test 
La descrizione di dettaglio di ciascun caso di test è contenuta nel documento Allegato al Piano dei 
Test [RIF.4] a completamento del presente. 
In particolare: 
• Nella ‘Tabella dei test’ è contenuta la tracciatura a partire dai requisiti utente fino al singolo 
caso di test; 
• Nelle ‘Specifiche di test’ ogni caso di test è dettagliato in termini procedurali.