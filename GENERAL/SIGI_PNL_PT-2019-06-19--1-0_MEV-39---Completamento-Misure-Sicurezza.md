---
uniqueName: sigipnlpt-2019-06-19-1-0mev-39-completamento-misur
displayName: "SIGI PNL PT 2019 06 19  1 0 MEV 39   Completamento Misure Sicurezza"
category: "GENERAL"
tags: []
---

# SIGI_PNL_PT-2019 06 19 -1.0_MEV 39 - Completamento Misure Sicurezza

> **File originale:** `MEV/VERSIONE_SIES_11.3_NEW/MEV_39/SIGI_PNL_PT-2019 06 19 -1.0_MEV 39 - Completamento Misure Sicurezza.xls`  
> **Tipo:** XLS

---

## Copertina

|  |  |  |  |
| --- | --- | --- | --- |
|  | Ministero della Giustizia |  |  |
|  | Piano di Test |  |  |
|  | MEV 39 - Completamento MS |  |  |
|  |  | Codice documento: | SIGI-PNL-PT |
|  |  | Versione: | 1.0 |
|  |  | Data Versione: | 43635.0 |

## Approvazioni_Revisioni

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
|  | Approvazioni |  |  |  |
|  | Titolo | MEV 39 - Completamento MS |  |  |
|  | Codice doc | SIGI-PNL-PT |  |  |
|  | MEV 39 - Completamento MS |  |  | Data |
|  | Redatto da | Emma  Caporizzo |  | 43635.0 |
|  | Verificato | Vito N. Bufi |  | 43635.0 |
|  | Approvato da | Vito N. Bufi |  | 43635.0 |
|  | Responsabile | P. Ceccanti |  |  |
|  | Cliente e/o utenti | Ministero della Giustizia |  | n.a. |
|  | Direzione | SIGI-PNL-PT |  |  |
|  | Revisioni |  |  |  |
|  | Data | Versione | Autore/i | Descrizione |
|  | 43635.0 | 1.0 | Vito N. Bufi | Prima emissione |

## Documenti di riferimento

| Tipo documento | Nome documento |
| --- | --- |
| Piano Lavoro Obiettivo | SIGI_PNL_AF-2017 09 26_1.4_MEV 39 - Completamento MS - Analisi Funzionale.doc |

## Tabella dei Test

|  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  | Caso di test |  |  |
| SISTEMA | ID | Secondo Livello | ID | Terzo livello | ID | Nome del caso di test | Descrizione e note |
| Sistema SIEP | 0001 (cap. 2 A.F) | UC1.01 Menù: Gestione Misure di Sicurezza | F001 | Funzione: Restituzione Ordine di Consegna | 0001 (cap. 2 A.F)F001-TF01 | Verifica: Corretto funzionamento della funzionalità di Richiesta Restituzione Ordine di Consegna | L'utente tramite la funzione in oggetto può inserire e gestire la richiesta di restituzione di un ordine di consegna |
| Sistema SIEP | 0002 (cap. 3- par. 3.1  A.F) | UC1.01 Menù: Gestione Misure di Sicurezza | F002 | Funzione: Archiviazione per Provvedimento di Cumulo | 0002 (cap. 3- par. 3.1  A.F)F002-TF01 | Verifica: Corretto funzionamento della funzionalità di Archiviazione per Assorbimento in Cumulo | L'utente tramite la funzione in oggetto può inserire e gestire l'annotazione di Archiviazione per Assorbimento in Cumulo. |
| Sistema SIEP | 0003  (cap. 3- par. 3.6  A.F) | UC1.01 Menù: Gestione Misure di Sicurezza | F003 | Funzione: Archiviazioni | 0003  (cap. 3- par. 3.6  A.F)F003-TF01 | Verifica: Presenza di un nuovo pulsante che rimanda alla funzione 'Restituzione Ordine di Consegna'. | Per tutte le tipologie di Archiviazione previste nella sezione 'Definizione Procedimento' del menù Gestione Misure di Sicuezza, deve essere presente un nuovo pulsante che rimanda alla funzione 'Restituzione Ordine di Consegna'. |
| Sistema SIEP | 0004 (cap. 3- par. 3.7  A.F) | UC1.01 Menù: Gestione Misure di Sicurezza | F004 | Funzione: Archiviazione Manuale | 0004 (cap. 3- par. 3.7  A.F)F004-TF01 | Verifica: Presenza di nuovi motivi di Archiviazione | L'utente in fase di inserimento di un'annotazione di Archiviazione Manuale  deve visualizzare le seguenti nuove tipologie di 'Oggetto Definizione' |
| Sistema SIEP (da verificare) | 0005 (cap. 4  A.F.) | UC1.01 Menù: Gestione Misure di Sicurezza | F005 | Funzione:  Comunicazione, Ordine di Consegna, Ordine di Esecuzione per Internamento, Ordine di Liberazione, Richiesta al Dap di Designazione Istituto , Comunicazione Avvenuta Designazione | 0005 (cap. 4  A.F.)F005-TF01 | Verifica: Template per Procedimenti di Applicazione di Misure di Sicurezza Applicate Provvisoriamente | In fase di generazione della stampa, per le funzioni dichiarate, verificare che il documento generato presenti delle parametrizzazioni specifiche in base alla casistica in cui il procedimento si  riferito a  Misure di Sicurezza Applicate Provvisoriamente o Disposte Fuori Sentenza |
| Sistema SIEP | 0006  (cap. 4- par. 4.7, 4.8 , 4.9  A.F) | SIGI-PNL-PT | F006 | Funzione:  Dettaglio Comunicazione, Ordine di Consegna, Ordine di Liberazione, Richiesta al Dap di Designazione Istituto , Comunicazione Avvenuta Designazione | 0006  (cap. 4- par. 4.7, 4.8 , 4.9  A.F)F006-TF01 | Verifica: La pagina di dettaglio deve presentare i tasti funzioni per l'upload(validazione) e cancellazione. | Nella pagina di dettaglio di emissione di una Comunicazione ,di un Ordine di Consegna, di un Ordine di Liberazione, di Richiesta al Dap di Designazione Istituto , di Comunicazione Avvenuta Designazione  deve essere prevista l’introduzione dell’icona di upload che permetta la validazione del provvedimento, e dell’icona di cancellazione per permettere di eliminare (annullare) il provvedimento appena inserito. |
| Sistema SIEP | 0007 (cap. 4- par. 4.10.3  A.F) | 1.0 | F007 | Funzione:  Inserimento di Ordine Esecuzione per Internamento a seguito di Disignazione di Istituto. | 0007 (cap. 4- par. 4.10.3  A.F)F007-TF01 | Verifica: Il dato dell’istituto designato deve essere riportato in automatico sulla maschera per l’emissione dell’ordine di esecuzione. | Dopo l'inserimento di Richiesta al DAP, dalla pagina di riepilogo,  qualora l’utente scelga di proseguire con l’emissione dell' Ordine Esecuzione per Internamento , il dato dell’istituto designato deve essere riportato in automatico sulla maschera per l’emissione dell’ordine di esecuzione. |
| Sistema SIEP | 0008 (cap. 5- par. 5.2  A.F) | 23/03/2018 | F008 | Funzione: Scadenziario>>Aggiorna Scadenza Misura di Sicurezza | 0008 (cap. 5- par. 5.2  A.F)F008-TF01 | Verificare la nuova funzione Aggiorna Scadenza Misura di Sicurezza | Nella pagina di Aggiorna Scadenza Misura di Sicurezza l'utente inserisce i giorni, mesi o anni per parametrizzare la data di scadenza per la comunicazione della Misura di Sicurezza alla Sorveglianza rispetto alla Data di Fine Pena nello Scadenziario 'Data Scadenza Comunicazione Misura Sicurezza ' |
| Sistema SIEP | 0009 (cap. 5- par. 5.3  A.F) | UC1.01 Menù: Gestione Misure di Sicurezza | F009 | Funzione: Scadenziario>>Data Scadenza Comunicazione Misura Sicurezza | 0009 (cap. 5- par. 5.3  A.F)F009-TF01 | Verificare lo scadenziario di  'Data Scadenza Comunicazione Misura Sicurezza ' | Verificare che la data Scadenza Comunicazione di tale scadenziario si aggiorni in base al quantum inserito per ufficio ed in base al Fine Pena. Verificare che il risultato sia esportabile su foglio excel e che le iconcine di 'Scaduto', 'In Scadenza' e 'In scadenza Oggi' siano linkabili come filtro. |
| Sistema SIEP | 0010 (cap. 5- par. 5.1  A.F) | UC1.01 Menù: Gestione Misure di Sicurezza | F010 | Funzione: Scadenziario>>Scadenzario Differimento Misure Sicurezza | 0010 (cap. 5- par. 5.1  A.F)F010-TF01 | Verificare lo scadenziario di  'Scadenzario Differimento Misure Sicurezza ' | Verificare che in elenco appaiano i procedimenti di classe IV per i quali è stato inserito un ordine di Liberazione per Differimento della Misura di Sicurezza. |
| Sistema SIEP | 0011 (cap. 6  A.F) | UC1.01 Menù: Gestione Misure di Sicurezza | F011 | Funzione: Ordine di Liberazione per Differimento | 0011 (cap. 6  A.F)F011-TF01 | Verificare l'inserimento di un Ordine di Liberazione per Differimento | Il sistema deve permettere l'inserimento di un Ordine di Liberazione per differimento delle Misura di Sicurezza. Se esistente, in automatico devono essere preimpostati i dati dell'ultima Ordinanza di Rinvio Esecuzione MS per Differimento della misura. |
| Sistema SIEP | 0012 (cap. 7- par. 7.1.2  A.F) | UC1.01 Menù: Istruttorie/Richieste | F012 | Funzione: Richiesta di dichiarazione di abituabilità/professionalità nel reato | 0012 (cap. 7- par. 7.1.2  A.F)F012-TF01 | Verificare la trasmissione telematica di una richiesta di dichiarazione di abituabilità/professionalità nel reato. | Il sistema deve permettere la trasmissione telematica all'ufficio di sorveglianza a seguito di Richiesta di abituabilità/professionalità nel reato. |
| Sistema SIEP | 0013  (cap. 7- par. 7.1.1  A.F) | UC1.01 Menù: Istruttorie/Richieste | F013 | Funzione: Richiesta di dichiarazione di abituabilità/professionalità nel reato | 0013  (cap. 7- par. 7.1.1  A.F)F013-TF01 | Verificare la stampa del template per la Richiesta di abituabilità/professionalità nel reato. | A seguito di una Richiesta  di abituabilità/professionalità nel reato, verificare che la frase 'Considerato che il condannato sta scontando una pena di Anni XXX di XXX con decorrenza dal XXX e scadenza fissata al XXX’  appare solo per posizione giuridica diverso da Libero. |
| Sistema SIEP | 0014 (cap. 7- par. 7.2  A.F) | UC1.01 Menù: Gestione Misure di Sicurezza | F014 | Funzione: Iscrizione Procedimento Misura Sicurezza disposta fuori sentenza | 0014 (cap. 7- par. 7.2  A.F)F014-TF01 | Verificare che nella funzione 'Iscrizione Procedimento Misura Sicurezza Disposta fuori Sentenza' appaiano anche i procedimenti di Appello contro Misure di Sicurezza emessi dal TDS. | A seguito di un'iscrizione di un Procedimento di Appello contro Misure di Sicurezza da parte del Tribunale di Sorveglianza e trasmesso alla Procura, verificare che il sistema mostri tale ordinanza nell'elenco sottostante alla funzione di 'Iscrizione Procedimento Misura Sicurezza Disposta fuori Sentenza'. |
| Sistema SIEP | 0015 (cap. 7- par. 7.2.1  A.F) | UC1.01 Menù: Gestione Misure di Sicurezza | F015 | Funzione: Pagina di dettaglio procedimento di classe IV | 0015 (cap. 7- par. 7.2.1  A.F)F015-TF01 | Verifica del link sulla Misura di Sicurezza riportata sulla pagina di dettaglio di un procedimento di classe IV. | Dopo aver cercato un procedimento di classe IV per cui è presente una misura di sicurezza, l'utente verifica che cliccando sul campo 'tipo misura' venga richiamata la funzione 'elenco misure di sicurezza' mostrando la pagina per l'associazione del titolo esecutivo. |
| Sistema SIEP | 0016 (cap. 7- par. 7.3  A.F) | UC1.01 Menù: Gestione Misure di Sicurezza | F016 | Funzione: Annotazione Decisione della Sorveglianza | 0016 (cap. 7- par. 7.3  A.F)F016-TF01 | Verificare che nella funzione 'Annotazione Decisione Sorveglianza' appaiano anche i procedimenti di Appello contro Misure di Sicurezza emessi dal TDS. | A seguito di un'iscrizione di un Procedimento di Appello contro Misure di Sicurezza da parte del Tribunale di Sorveglianza e trasmesso alla Procura, verificare che il sistema mostri tale ordinanza nell'elenco sottostante alla funzione di 'Annotazione Decisione Sorveglianza'. |
| Sistema SIEP | 0017 (cap. 7- par. 7.5  A.F) | UC1.01 Menù: Gestione Misure di Sicurezza | F017 | Funzione: Annotazione Decisione della Sorveglianza | 0017 (cap. 7- par. 7.5  A.F)F017-TF01 | Stampa Comunicazione/Ordine Consegna a seguito provvedimento impugnazione. | Verificare la parametrizzazione dei template per emissione di un provvedimento di Comunicazione/Ordine Consegna a seguito provvedimento impugnazione. |
| Sistema SIEP | 0018 (cap. 7- par. 7.6  A.F) | UC1.01 Menù: Gestione Misure di Sicurezza | F018 | Funzione: Annotazione Decisione della Sorveglianza | 0018 (cap. 7- par. 7.6  A.F)F018-TF01 | Stampa Ordine Esecuzione per Internamento a seguito provvedimento impugnazione. | Verificare la parametrizzazione dei template per emissione di un Ordine Esecuzione per Internamento a seguito provvedimento di impugnazione. |
| Sistema SIEP | 0019 (cap. 7- par. 7.7  A.F) | UC1.01 Menù: Gestione Misure di Sicurezza | F019 | Funzione: Annotazione Decisione della Sorveglianza | 0019 (cap. 7- par. 7.7  A.F)F019-TF01 | Stampa Ordine Liberazione a seguito provvedimento impugnazione. | Verificare la parametrizzazione dei template per emissione di un Ordine di Liberazione a seguito provvedimento di impugnazione |
| Sistema SIEP | 0020 (cap. 8- par. 8.4.1  A.F) | UC1.01 Menù: Statistiche/Monitoraggio | F020 | Statistiche - Estrazione Dati per procedimenti di classe IV | 0020 (cap. 8- par. 8.4.1  A.F)F020-TF01 | Statistica Riepilogo Iscrizioni e Tipologia Misura per procedimenti di classe IV. | Verificare l'output della statistica di tipologia 'Riepilogo Iscrizioni e Tipologia Misura' relativa a procedimenti di classe IV. |
| Sistema SIEP | 0021 (cap. 8- par. 8.4.2  A.F) | UC1.01 Menù: Statistiche/Monitoraggio | F021 | Statistiche - Estrazione Dati per procedimenti di classe IV | 0021 (cap. 8- par. 8.4.2  A.F)F021-TF01 | Statistica 'Procedimenti Pendenti nel Periodo' per procedimenti di classe IV. | Verificare l'output della statistica di tipologia 'Procedimenti Pendenti nel Periodo' relativa a procedimenti di classe IV. |
| Sistema SIEP | 0022 (cap. 8- par. 8.4.3  A.F) | UC1.01 Menù: Statistiche/Monitoraggio | F022 | Statistiche - Estrazione Dati per procedimenti di classe IV | 0022 (cap. 8- par. 8.4.3  A.F)F022-TF01 | Statistica 'Movimento procedimenti (Riepilogo Procedimenti Pendenti)'  per procedimenti di classe IV. | Verificare l'output della statistica di tipologia 'Movimento procedimenti (Riepilogo Procedimenti Pendenti)' relativa a procedimenti di classe IV. |
| Sistema SIEP | 0023  (cap. 8- par. 8.4.4  A.F) | UC1.01 Menù: Statistiche/Monitoraggio | F023 | Statistiche - Estrazione Dati per procedimenti di classe IV | 0023  (cap. 8- par. 8.4.4  A.F)F023-TF01 | Statistica 'Attività Magistrati' per procedimenti di classe IV. | Verificare l'output della statistica di tipologia 'Attività Magistrati' relativa a procedimenti di classe IV. |
| Sistema SIEP | 0024 (cap. 9- par. 9.1  A.F) | UC1.01 Menù: Statistiche/Monitoraggio | F024 | R.E.M.S. (Residenza per l'esecuzione delle Misure di Sicurezza) | 0024 (cap. 9- par. 9.1  A.F)F024-TF01 | Funzione di Inserimento Misure di Sicurezza. | Verificare la presenza della misura di sicurezza R.E.M.S. (Residenza per l'esecuzione delle Misure di Sicurezza) nella maschera di inserimento delle misure di sicurezza. |
| Sistema SIEP | 0025 (cap. 9- par. 9.2  A.F) | UC1.01 Menù: Statistiche/Monitoraggio | F025 | Espulsione dallo Stato | 0025 (cap. 9- par. 9.2  A.F)F025-TF01 | Funzione di Inserimento Misure di Sicurezza. | Verificare la presenza delle seguenti nuove misura di sicurezza nella maschera di inserimento delle misure di sicurezza:                                                                                                                              1. ESPULSIONE DELLO STRANIERO (ART. 235 C.P.)
2. ESPULSIONE DELLO STRANIERO DALLO STATO (ART. 312 C.P.)
3. ALLONTANAMENTO DELLO STRANIERO DALLO STATO (ART. 235 C.P.)
4. ALLONTANAMENTO DELLO STRANIERO DALLO STATO (ART. 312 C.P.) |
| Sistema SIUS | 0026  (cap. 10- par. 10.1 - 10.2  A.F) | UC1.01 Menù: Emissione Ordinanza UDS | F026 | Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 cpp c. 2 | 0026  (cap. 10- par. 10.1 - 10.2  A.F)F026-TF01 | Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 cpp c. 2 | Verificare che per il contenuto U082 (Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 cpp c. 2 ) gli oggetti associati siano:• Differimento della misura di sicurezza facoltativa attesa grazia
• Differimento della misura di sicurezza facoltativo grave infermità
• Differimento della misura di sicurezza facoltativo maternità
• Differimento della misura di sicurezza obbligatoria nei confronti di madre di infante di età inferiore ad anni uno
• Differimento della misura di sicurezza obbligatoria nei confronti di donna incinta
• Differimento della misura di sicurezza obbligatoria nei confronti di persona affetta da malattia |
| Sistema SIUS | 0027 (cap. 10- par. 10.2  A.F) | UC1.01 Menù: Emissione Decreto UDS | F027 | Decreto di Rinvio esecuzione misura sicurezza ex art. 684 cpp c. 2 (U082) | 0027 (cap. 10- par. 10.2  A.F)F027-TF01 | Decreto di Rinvio esecuzione misura sicurezza ex art. 684 cpp c. 2 | Verificare che il sistema SIUS permette di inserire anche un decreto per il contenuto 'Rinvio esecuzione misura sicurezza ex art. 684 cpp c. 2 ' |
| Sistema SIUS | 0028 (cap. 10- par. 10.4  A.F) | UC1.01 Menù: Emissione Decreto UDS | F028 | Decreto di Rinvio esecuzione misura sicurezza ex art. 684 cpp (U077) | 0028 (cap. 10- par. 10.4  A.F)F028-TF01 | Decreto di Rinvio esecuzione misura sicurezza ex art. 684 cpp (U077) | Verificare che nella pagina di inserimento di un decreto per il contenuto 'Rinvio esecuzione misura sicurezza ex art. 684 cpp ' siano presenti i campi                                                                      • Data decorrenza differimento esecuzione
• Rinvio fino al 
• Rinvio nella misura di
per i seguenti esiti:                                                                                                                                                                                                                                                                                                                                             • RINVIA ESECUZIONE E ORDINA IL RICOVERO IN UNA CASA DI CURA O IN UN ALTRO LUOGO DI CURA (ART. 211 BIS C.P.)
• DIFFERISCE PROVVISORIAMENTE LA MISURA DI SICUREZZA |
| Sistema SIUS  (vedi par. 10.6 dell'AF) | 0029 (cap. 10- par. 10.6  A.F) | UC1.01 Menù: Trasmissione ordinanze/decreti per UDS (U077 e U082) | F029 | Trasmissione ordinanze/decreti per UDS (U077 e U082) | 0029 (cap. 10- par. 10.6  A.F)F029-TF01 | Trasmissione ordinanze/decreti per UDS (U077 e U082) | Verificare che nella pagina di trasferimento decreto/ordinanza per un pocediemento di Rinvio esecuzione misura sicurezza ex art. 684 cpp e Rinvio esecuzione misura sicurezza ex art. 684 cpp c. 2 , tra gli ufficio destinatari del procedimento appaia l'ufficio titolare del procedimento di classe I (se presente) , di classe IV (se presente) e l'autorità Procura Generale. |
| Sistema SIUS | 0030 (cap. 11 - par. 11.1  A.F) | UC1.01 Menù: Emissione Ordinanza TDS | F030 | Rinvio dell'esecuzione della misura sicurezza ex art. 684 | 0030 (cap. 11 - par. 11.1  A.F)F030-TF01 | Rinvio dell'esecuzione della misura sicurezza ex art. 684 | Verificare che la pagina di inserimento emissione ordinanza,  per il contenuto (Rinvio dell'esecuzione della misura sicurezza ex art. 684 )  consenta di inserire i seguenti dati: 
• Per l’esito ‘CONCEDE PER UN PERIODO’ (ESITO_TENORE = 0259) deve essere prevista la sezione dei dati del differimento (Data Decorrenza Differimento Esecuzione + Rinvio Fino al + Giorni, Mesi ed Anni di rinvio della misura)                                                                                                                                                                                                                                                                       • Per l’esito ‘CONCEDE E ORDINA IL RICOVERO IN UNA CASA DI CURA O IN ALTRO LUOGO DI CURA’ (ESITO_TENORE = 0260) deve essere previsto un ulteriore campo a testo libero per annotare la casa di cura o luogo di cura. |
| Sistema SIUS | 0031  (cap. 11 - par. 11.2 A.F) | UC1.01 Menù: Emissione Ordinanza TDS | F031 | Pagina di dettaglio Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 | 0031  (cap. 11 - par. 11.2 A.F)F031-TF01 | Pagina di dettaglio Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 | Verificare che  sulla pagina di dettaglio di Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 siano riportati i campi Data Decorrenza Differimento Esecuzione + Rinvio Fino al + Giorni + Mesi ed Anni di rinvio della misura + Luogo Ricovero. |
| Sistema SIUS | 0032  (cap. 11 - par. 11.3  A.F) | UC1.01 Menù: Emissione Ordinanza TDS | F032 | Pagina di modifica Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 | 0032  (cap. 11 - par. 11.3  A.F)F032-TF01 | Pagina di modifica Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 | Verificare che  sulla pagina di modifica di Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 siano riportati i campi Data Decorrenza Differimento Esecuzione + Rinvio Fino al + Giorni + Mesi ed Anni di rinvio della misura + Luogo Ricovero e siano editabili. |
| Sistema SIUS | 0033  (cap. 11 - par. 11.4  A.F) | UC1.01 Menù: Stampa Ordinanza TDS | F033 | Stampa Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 | 0033  (cap. 11 - par. 11.4  A.F)F033-TF01 | Stampa Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 | Verificare che la stampa vada a buon fine. |
| Sistema SIUS | 0034  (cap. 11 - par. 11.5  A.F) | UC1.01 Menù: Trasmissione Ordinanza TDS | F034 | Trasmissione Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 | 0034  (cap. 11 - par. 11.5  A.F)F034-TF01 | Trasmissione Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 | Verificare che nella pagina di trasferimento ordinanza per un procedimento di Rinvio esecuzione misura sicurezza ex art. 684 cpp , tra gli ufficio destinatari del procedimento appaia l'ufficio titolare del procedimento di classe I (se presente) , di classe IV (se presente) e l'autorità Procura Generale. |
| Sistema SIUS | 0035 (cap. 12 - da par. 12.1   A.F) | UC1.01 Menù: Inserimento Ordinanza Procedimento SIUS | F035 | Pagina  inserimento ordinanza per procedimento di Appello Contro Provvedimento su Misura di Sicurezza (Art.  680 Cpp) | 0035 (cap. 12 - da par. 12.1   A.F)F035-TF01 | Pagina  inserimento ordinanza per procedimento di Appello Contro Provvedimento su Misura di Sicurezza (Art.  680 Cpp) | Verificare che la pagina di inserimento emissione ordinanza,  per il contenuto ((Appello Contro Provvedimento su Misura di Sicurezza (Art.  680 Cpp) )  consenta di inserire i seguenti dati: • Estremi del provvedimento impugnato ; • Dati della misura di sicurezza irrogata\in esecuzione.  ; • Sezione per inserire una ‘nuova misura’ |
| Sistema SIUS | 0035 (cap. 12 - da par. 12.4   A.F) | UC1.01 Menù: Trasferimento Procedimento SIUS | F035 | Pagina  trasferimento procedimento per il contenuto C029 (Appello Contro Provvedimento su Misura di Sicurezza (Art.  680 Cpp)) | 0035 (cap. 12 - da par. 12.4   A.F)F035-TF01 | Pagina  trasferimento procedimento per il contenuto C029 (Appello Contro Provvedimento su Misura di Sicurezza (Art.  680 Cpp)) | Verificare che nella pagina di trasferimento ordinanza per un procedimento di Appello Contro Provvedimento su Misura di Sicurezza (Art.  680 Cpp) , tra gli ufficio destinatari del procedimento appaia l'ufficio titolare del procedimento di classe I (se presente) , di classe IV (se presente) e l'autorità Procura Generale. |
| Sistema SIUS | 0035 (cap. 12 - par. 12.5  A.F) | UC1.01 Menù: Dettaglio Procedimento SIUS | F035 | Pagina  dettaglio procedimento per il contenuto C029 (Appello Contro Provvedimento su Misura di Sicurezza (Art.  680 Cpp)) | 0035 (cap. 12 - par. 12.5  A.F)F035-TF01 | Pagina  dettaglio procedimento per il contenuto C029 (Appello Contro Provvedimento su Misura di Sicurezza (Art.  680 Cpp)) | Verificare che nella pagina dettaglio procedimento per il contenuto C029 (Appello Contro Provvedimento su Misura di Sicurezza (Art.  680 Cpp)) sia  presente il link 'Misure di Sicurezza' e che mostri il dettaglio della misura. |
| Sistema SIUS | 0036  (cap. 13 - par. 13.1.1  A.F) | UC1.01 Menù: Inserimento Misura di Sicurezza | F036 | Pagina di Inserimento Misura di Sicurezza | 0036  (cap. 13 - par. 13.1.1  A.F)F036-TF01 | Pagina di Inserimento Misura di Sicurezza | Verificare che nella pagina di inserimento della misura di sicurezza ci sia la voce R.E.M.S. (Residenza per l'esecuzione delle Misure di Sicurezza) |
| Sistema SIUS | 0037 (cap. 13 - par. 13.1.2  A.F) | UC1.01 Menù: 13.1.2  Emissione Ordinanza | F037 | Pagine Emissione Ordinanza | 0037 (cap. 13 - par. 13.1.2  A.F)F037-TF01 | Pagine Emissione Ordinanza | Verificare che nella pagina di emissione ordinanza per i contenuti U067 (Riesame pericolosità sociale) e U023 (Applicazione Misura Sicurezza), l’elenco delle misure mostrato nella pagina deve essere aggiornato con la nuova misura R.E.M.S. (Residenza per l'esecuzione delle Misure di Sicurezza) |
| Sistema SIUS | 0038 (cap. 13 - par. 13.1.3  A.F) | UC1.01 Menù: 13.1.2   Inserimento Procedimento SIUS | F038 | Pagina Inserimento Procedimento SIUS. | 0038 (cap. 13 - par. 13.1.3  A.F)F038-TF01 | Inserimento Procedimento SIUS - Nuovo Oggetto per Esecuzione Misure di Sicurezza | Verificare che per il contenuto U024 (Esecuzione Misura Sicurezza), deve essere previsto un nuovo oggetto con denominazione R.E.M.S. (Residenza per l'esecuzione delle Misure di Sicurezza). Pertanto in fase iscrizione di un procedimento di Esecuzione Misura Sicurezza, in fase di selezione dell’oggetto, la pagina di elenco in popup deve mostrare anche la nuova misura R.E.M.S. (Residenza per l'esecuzione delle Misure di Sicurezza) |

## Dettaglio Test

| ID caso di test | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
| --- | --- | --- | --- | --- | --- | --- |
| 0001F001-TF01 | 01 | Verifica: Corretto funzionamento della funzionalità di Richiesta Restituzione Ordine di Consegna |  | L'utente tramite la funzione in oggetto può inserire e gestire la richiesta di restituzione di un ordine di consegna |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente si sposta sul menù Gestione Misure di Sicurezza |  | Il sitema mostra la pagina per inserire anno e numero del procedimento di interesse . |  |
|  | 2.0 | Azione | L'utente sceglie un procedimento di misure di sicurezza di classe IV per cui ha iscrittto almeno un provvedimento di Ordine di Consenga o di Internamento. |  | Il sistema mostra il dettaglio del procedimento scelto. |  |
|  | 3.0 | Azione | L'utente selezione il menù Restituzione Ordine di Consegna |  | Il sistema mostra la pagina per inserire la richiesta di restituzione di un ordine di consegna. In particolare mostra una lista dei provvedimenti che sono idonei per una richiesta di restituzione. |  |
|  | 4.0 | Azione | L'utente seleziona il provvedimento per cui vuole fare richiesta di restituzione e va avanti cliccando sul tasto conferma. |  | Il sistema mostra la pagina dettaglio della richiesta inserita, mostrando anche i tasti funzione per procedere con la validazione , modifica o cancellazione della richiesta appena inserita. |  |
|  | 5.0 | Azione | L'utente selezione il pulsante per la modifica della richiesta. |  | Il sistema mostra la pagina di inserimento della richiesta per permettere all'utente di poter modificare il provvedimento scegliendo un nuovo provvedimento di ordine di consegna, oppure di modificare l'unico campo editabile NOTE. |  |
|  | 6.0 | Azione | L'utente seleziona il pulsante per la validazione. |  | Il sistema mostra la pagina dettaglio della richiesta inserita. La richiesta non è più modificabile. |  |
|  | 7.0 | Azione | L'utente dalla lsita dei provvedimenti del PM seleziona l'icona di cancellazione. |  | Il sistema mostra la pagina per inserire la motivazione dell'annullamento e procede con l'eliminazione della richiesta di restituzione dell'ordine di consegna. |  |
| 0002F002-TF01 | 01 | SIGI-PNL-PT |  | L'utente tramite la funzione in oggetto può inserire e gestire l'annotazione di Archiviazione per Assorbimento in Cumulo. |  |  |
|  | Step | Tipo | 1.0 | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | 23/03/2018 |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente si sposta sul menù Gestione Misure di Sicurezza |  | Il sistema mostra la pagina per inserire anno e numero del procedimento di interesse . |  |
|  | 2.0 | Azione | L'utente sceglie un procedimento di misure di sicurezza di classe IV NON coinvolto in un trasferimento di competenza per Assorbimento in Cumulo. |  | Il sistema mostra il dettaglio del procedimento scelto. |  |
|  | 3.0 | Azione | L'utente selezione la funzione Archiviazione per Provvedimento di Cumulo sotto Gestione Misure di Sicurezza |  | Il sistema visualizza un messaggio che inibisce il prosieguo della funzione perché il procedimento di classe IV non risulta coinvolto in nessun trasferimento dii competenza per Assorbimento in cumulo. |  |
|  | 4.0 | Azione | L'utente sceglie un procedimento di misure di sicurezza di classe IV coinvolto in un trasferimento di competenza per Assorbimento in Cumulo. |  | Il sistema mostra il dettaglio del procedimento scelto. |  |
|  | 5.0 | Azione | L'utente selezione la funzione Archiviazione per Provvedimento di Cumulo sotto Gestione Misure di Sicurezza |  | Il sistema mostra la pagina per inserire l'annotazione precompilando in automatico i dati dell'ultimo provvedimento di cumulo in cui è stato coinvolto il titolo di classe IV prescelto (proprio ufficio o altro ufficio) |  |
|  | 6.0 | Azione | L'utente compila i dati obbligatori e procede cliccando sul tasto Conferma. |  | Il sistema inserisce un'annotazione di Archiviazione per Assorbimento in cumulo e mostra la pagina di dettaglio. |  |
|  | 7.0 | Azione | Dalla pagina di dettaglio l'utente selezione il pulsante per la modifica dell'annotazione. |  | Il sistema mostra la pagina con i dati immessi permettendoo la sola modifica del campo Data di definizione e Motivazione. |  |
|  | 8.0 | Azione | L'utente seleziona il pulsante per la validazione. |  | Il sistema mostra la pagina dettaglio dell'annotazione inserita e mostra il pulsante 'Restituzione Ordine di Consegna' . |  |
|  | 9.0 | Azione | L'utente dalla lsita dei provvedimenti del PM seleziona l'icona di cancellazione. |  | Il sistema mostra la pagina per inserire la motivazione dell'annullamento e procede con l'eliminazione dell'annotazione. |  |
| 0003F003-TF01 | 01 | Verifica: Presenza di un nuovo pulsante che rimanda alla funzione 'Restituzione Ordine di Consegna' |  | Per tutte le tipologie di Archiviazione previste nella sezione 'Definizione Procedimento' del menù Gestione Misure di Sicuezza, deve essere presente un nuovo pulsante che rimanda alla funzione 'Restituzione Ordine di Consegna' |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente si sposta sul menù Gestione Misure di Sicurezza |  | Il sitema mostra la pagina per inserire anno e numero del procedimento di interesse . |  |
|  | 2.0 | Azione | L'utente sceglie un procedimento di misure di sicurezza di classe IV |  | Il sistema mostra il dettaglio del procedimento scelto. |  |
|  | 3.0 | Azione | L'utente selezione il menù Archiviazione Manuale. |  | Il sistema mostra la pagina per inserire i dati per l'inserimento dell'annotazione di Archiviazione del procedimento. |  |
|  | 4.0 | Azione | L'utente completa il form di inserimento e va avanti cliccando sul tasto conferma. |  | Il sistema mostra la pagina dettaglio dell'annotazione di archiviazione inserita. |  |
|  | 5.0 | Azione | L'utente valida il provvedimento. |  | Il sistema mostra la pagina di riepilogo presentando il nuovo pulsante 'Restituzione Ordine di Consegna'. |  |
|  | 6.0 | Azione | L'utente ripete i punti 3, 4, e 5 per le altre tipologie di archiviazione. |  | Il sistema mostra per ogni fuznione il nuovo pulsante 'Restituzione Ordine di Consegna'. |  |
| 0004F004-TF01 | 01 | Verifica: Presenza di nuovi motivi di Archiviazione |  | L'utente in fase di inserimento di un'annotazione di Archiviazione Manuale  deve visualizzare le seguenti nuove tipologie di 'Oggetto Definizione' |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente si sposta sul menù Gestione Misure di Sicurezza |  | Il sistema mostra la pagina per inserire anno e numero del procedimento di interesse . |  |
|  | 2.0 | Azione | L'utente sceglie un procedimento di misure di sicurezza di classe IV |  | Il sistema mostra il dettaglio del procedimento scelto. |  |
|  | 3.0 | Azione | L'utente selezione il menù Archiviazione Manuale. |  | Il sistema mostra la pagina per inserire i dati per l'inserimento dell'annotazione di Archiviazione del procedimento e nella lista degli 'Oggetti Definizione' presenta le nuove voci:                                                                                                                                                                                                                                                                                                                                                          1. Riunione ad altro procedimento                                                                                                                                                                                                                                                                                                           2. Applicazione definitiva con sentenza di condanna                                                                                                                                                                                                                                                            3. Misura di sicurezza non applicata dal giudice con sentenza di condanna |  |
| 0005F005-TF01 | 01 | Verifica: Template per Procedimenti di Applicazione di Misure di Sicurezza Applicate Provvisoriamente |  | In fase di generazione della stampa, per le funzioni dichiarate, verificare che il documento generato presenti delle parametrizzazioni specifiche in base alla casistica in cui il procedimento si  riferito a  Misure di Sicurezza Applicate Provvisoriamente o Disposte Fuori Sentenza |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente si sposta sul menù Gestione Misure di Sicurezza |  | Il sistema mostra la pagina per inserire anno e numero del procedimento di interesse . |  |
|  | 2.0 | Azione | L'utente sceglie un procedimento di misure di sicurezza di classe IV |  | Il sistema mostra il dettaglio del procedimento scelto. |  |
|  | 3.0 | Azione | L'utente selezione il menù Gestione Misure di Sicurezza/Comunicazione |  | Il sistema mostra la pagina per inserire i dati per l'inserimento della comunicazione. |  |
|  | 4.0 | Azione | L'utente inserisce i dati e prosegue con la conferma del form. |  | Il sistema inserisce la comunicazione e mostra la pagina di dettaglio del provvedimeno appena inserito. |  |
|  | 5.0 | Azione | L'utente prosegue con la generazione del documento. |  | Il sistema genera il documento associato e parametrizza il titolo se è relativo a Misure Applicate Provvisoriamente o Applicate Fuori Sentenza. |  |
|  | 6.0 | Azione | L'utente ripete il flusso per ogni funzione dichiarata in verifica. |  |  |  |
| 0006F006-TF01 | 01 | Verifica: La pagina di dettaglio deve presentare i tasti funzioni per l'upload(validazione) e cancellazione. |  | Nella pagina di dettaglio di emissione di una Comunicazione ,di un Ordine di Consegna, di un Ordine di Liberazione, di Richiesta al Dap di Designazione Istituto , di Comunicazione Avvenuta Designazione  deve essere prevista l’introduzione dell’icona di upload che permetta la validazione del provvedimento, e dell’icona di cancellazione per permettere di eliminare (annullare) il provvedimento appena inserito. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente si sposta sul menù Gestione Misure di Sicurezza |  | Il sistema mostra la pagina per inserire anno e numero del procedimento di interesse . |  |
|  | 2.0 | Azione | L'utente sceglie un procedimento di misure di sicurezza di classe IV |  | Il sistema mostra il dettaglio del procedimento scelto. |  |
|  | 3.0 | Azione | L'utente selezione il menù Gestione Misure di Sicurezza/Comunicazione |  | Il sistema mostra la pagina per inserire i dati per l'inserimento della comunicazione. |  |
|  | 4.0 | Azione | L'utente inserisce i dati e prosegue con la conferma del form. |  | Il sistema inserisce la comunicazione e mostra la pagina di dettaglio, mostrando i pulsanti per la stampa, validazione e modifica del provvedimeno appena inserito. |  |
|  | 5.0 | Azione | L'utente prosegue con l'utilizzo del tasto funzione di Upload (validazione) |  | Il sistema aggiorna correttamente il provvedimento. |  |
|  | 6.0 |  | L'utente prosegue con l'utilizzo del tasto funzione di Cancellazione. |  | Il sistema elimina il provvedimento. |  |
|  | 7.0 | Azione | L'utente ripete il flusso per ogni funzione dichiarata in verifica. |  |  |  |
| 0007F007-TF01 | 01 | Verifica: Il dato dell’istituto designato deve essere riportato in automatico sulla maschera per l’emissione dell’ordine di esecuzione. |  | Dopo l'inserimento di Richiesta al DAP, dalla pagina di riepilogo,  qualora l’utente scelga di proseguire con l’emissione dell' Ordine Esecuzione per Internamento , il dato dell’istituto designato deve essere riportato in automatico sulla maschera per l’emissione dell’ordine di esecuzione. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente richiama la funzione di ricerca procedimento. |  | Il sistema mostra la pagina per inserire anno e numero del procedimento di interesse . |  |
|  | 2.0 | Azione | L'utente sceglie un procedimento di misure di sicurezza di classe IV |  | Il sistema mostra il dettaglio del procedimento scelto. |  |
|  | 3.0 | Azione | L'utente si sposta sul menù Gestione Misure di Sicurezza/Richiesta DAP |  | Il sistema mostra la pagina per inserire i dati per l'inserimento della richiesta |  |
|  | 4.0 | Azione | L'utente inserisce i dati e prosegue con la conferma del form. |  | Il sistema inserisce la richiesta e mostra la pagina di dettaglio. |  |
|  | 5.0 | Azione | L'utente prosegue con l'utilizzo del tasto funzione di 'Ordine di Esecuzione per Internamento'. |  | Il sistema mostra la pagina per l'inserimento della richiesta di Internamento riportando in automatico la struttura designata prescelta nella funzione precedente. |  |
| 0008F008-TF01 | 01 | Verificare la nuova funzione 'Aggiorna Scadenza Misura di Sicurezza' |  | Nella pagina di Aggiorna Scadenza Misura di Sicurezza l'utente inserisce i giorni, mesi o anni per parametrizzare la data di scadenza per la comunicazione della Misura di Sicurezza alla Sorveglianza rispetto alla Data di Fine Pena nello Scadenziario 'Data Scadenza Comunicazione Misura Sicurezza ' |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente richiama la funzione Scadenziario |  | Il sistema mostra la pagina con le varie sotto funzioni di Scadenziario. |  |
|  | 2.0 | Azione | L'utente sceglie la funzione  'Aggiorna Scadenza Misura di Sicurezza' |  | Il sistema mostra la pagina per inserire i giorni, mesi o anni . |  |
|  | 3.0 | Azione | L'utente inserisce i giorni, mesi o anni  di interesse per la comunicazione di Scadenza della Misura di Sicurezza e Conferma con il relativo tasto. |  | Il sistema memorizza il dato e ripresenta la pagina con i valori prescelti. |  |
| 0009F009-TF01 | 01 | Verificare lo scadenziario di  'Data Scadenza Comunicazione Misura Sicurezza ' |  | Verificare che la data Scadenza Comunicazione di tale scadenziario si aggiorni in base al quantum inserito per ufficio ed in base al Fine Pena. Verificare che il risultato sia esportabile su foglio excel e che le iconcine di 'Scaduto', 'In Scadenza' e 'In scadenza Oggi' siano linkabili come filtro. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente richiama la funzione Scadenziario |  | Il sistema mostra la pagina con le varie sotto funzioni di Scadenziario. |  |
|  | 2.0 | Azione | L'utente sceglie la funzione  ' Data Scadenza Comunicazione Misura Sicurezza  ' |  | Il sistema mostra la pagina per scegliere la scedenza di interesse : 'Tutti', 'In Scadenza'… |  |
|  | 3.0 | Azione | L'utente sceglie l'opzione 'Tutti' e Conferma la ricerca. |  | Il sistema mostra l'elenco dei procedimenti di classe IV previsti per tale scadenziario. (Procedimenti di classe IV validati e non Archiviati con misura di sicurezza e per i quali non è stata fatta richiesta di Pericolosità Sociale o Trasmissione atti per Competenza.)La data scadenza comunicazione viene calcolata aggiungendo il quantum prescelto al Fine Pena. |  |
|  | 4.0 | Azione | L'utente clicca sull'icona  'Scarica in Excel' |  | Il sistema apre il foglio excel riportando l'elenco presente in scadenziario. |  |
|  | 5.0 | Azione | L'utente clicca sull'icona  'Scaduti' |  | Il sistema filtra l'elenco mostrando solo i procedimenti con Scadenza Comunicazione Misura Scaduta. |  |
| 0010F010-TF01 | 01 | Verificare lo scadenziario di  'Scadenzario Differimento Misure Sicurezza ' |  | Verificare che in elenco appaiano i procedimenti di classe IV per i quali è stato inserito un ordine di Liberazione per Differimento della Misura di Sicurezza. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente richiama la funzione Scadenziario |  | Il sistema mostra la pagina con le varie sotto funzioni di Scadenziario. |  |
|  | 2.0 | Azione | L'utente sceglie la funzione  ' Differimento Misura Sicurezza' |  | Il sistema mostra la pagina per scegliere la scedenza di interesse : 'Tutti', 'In Scadenza'… |  |
|  | 3.0 | Azione | L'utente sceglie l'opzione 'Tutti' e Conferma la ricerca. |  | Il sistema mostra l'elenco dei procedimenti di classe IV  per i quali è stato inserito un ordine di Liberazione per Differimento della Misura di Sicurezza. |  |
|  | 4.0 | Azione | L'utente clicca sull'icona  'Scarica in Excel' |  | Il sistema apre il foglio excel riportando l'elenco presente in scadenziario. |  |
|  | 5.0 | Azione | L'utente clicca sull'icona  'Scaduti' |  | Il sistema filtra l'elenco mostrando solo i procedimenti con Scadenza Comunicazione Misura Scaduta. |  |
| 0011F011-TF01 | 01 | Verificare l'inserimento di un Ordine di Liberazione per Differimento |  | Il sistema deve permettere l'inserimento di un Ordine di Liberazione per differimento delle Misura di Sicurezza. Se esistente, in automatico devono essere preimpostati i dati dell'ultima Ordinanza di Rinvio Esecuzione MS per Differimento della misura. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente richiama la funzione 'Gestione Misure di Sicurezza' |  | Il sistema mostra la pagina con le varie sotto funzioni. |  |
|  | 2.0 | Azione | L'utente sceglie la funzione  ' Ordine di Liberazione per Differimento' |  | Il sistema mostra la pagina per inserire il provvedimento di Ordine di Liberazione. Se è presente l'ordinanza della Sorveglianza gli estremi dell'ordinanza devono essere preimpostati in automatico. |  |
|  | 3.0 | Azione | L'utente imposta tutti i campi e conferma l'inserimento cliccando sul tasto 'Conferma'. |  | Il sistema inserisce il provvedimento e mostra la pagina di dettaglio. |  |
|  | 4.0 | Azione | L'utente procede con la validazione tramite il pulsante di upload. |  | Il sistema aggiorna lo stato del procedimento e mostra la pagina di dettaglio. |  |
| 0012F012-TF01 | 01 | Verificare la trasmissione telematica di una richiesta di dichiarazione di abituabilità/professionalità nel reato. |  | Il sistema deve permettere la trasmissione telematica all'ufficio di sorveglianza a seguito di Richiesta di  Richiesta di abituabilità/professionalità nel reato . |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente richiama la funzione 'Istruttorie/Richieste ' |  | Il sistema mostra la pagina con le varie sotto funzioni. |  |
|  | 2.0 | Azione | L'utente sceglie la funzione  'Richiesta/Comunicazione' |  | Il sistema mostra la pagina per inserire la richiesta. |  |
|  | 3.0 | Azione | L'utente seleziona la voce 'Richiesta' come 'Tipologia Atto'  e come 'Oggetto Atto' sceglie 'abituabilità/professionalità nel reato'. L'utente prosegue con la selezione del destinatario (Ufficio Sorveglianza) ed effettua l'inserimento con il tasto 'Conferma'. |  | Il sistema inserisce la richiesta e mostra la pagina di dettaglio. |  |
|  | 4.0 | Azione | L'utente procede con la validazione/stampa della richiesta. |  | Il sistema aggiorna il  procedimento e riporta sulla pagina di dettaglio mostrando l'icona per il trasferimento telematico (computerini). Dopo il trasferimento l'ufficio di Sorveglianza si ritroverà la richiesta nel  menù (Presa in carico atti pervenuti » Ricerca per Atti - SIEP ) |  |
| 0013F013-TF01 | 01 | Verificare la stampa del template per la Richiesta di abituabilità/professionalità nel reato. |  | A seguito di una Richiesta  di abituabilità/professionalità nel reato, verificare che la frase 'Considerato che il condannato sta scontando una pena di Anni XXX di XXX con decorrenza dal XXX e scadenza fissata al XXX’  appare solo per posizione giuridica diverso da Libero. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente richiama la funzione 'Istruttorie/Richieste ' |  | Il sistema mostra la pagina con le varie sotto funzioni. |  |
|  | 2.0 | Azione | L'utente sceglie la funzione  'Richiesta/Comunicazione' |  | Il sistema mostra la pagina per inserire la richiesta. |  |
|  | 3.0 | Azione | L'utente seleziona la voce 'Richiesta' come 'Tipologia Atto'  e come 'Oggetto Atto' sceglie 'abituabilità/professionalità nel reato'. L'utente prosegue con la selezione del destinatario (Ufficio Sorveglianza) ed effettua l'inserimento con il tasto 'Conferma'. |  | Il sistema inserisce la richiesta e mostra la pagina di dettaglio. |  |
|  | 4.0 | Azione | L'utente procede con la stampa della richiesta. |  | Il sistema apre il documento di stampa riportando la frase 'Considerato che il condannato sta scontando una pena di Anni XXX di XXX con decorrenza dal XXX e scadenza fissata al XXX’ solo se la posizione giuridica del soggetto è diverso da Libero. |  |
| 0014F014-TF01 | 01 | Verificare che nella funzione 'Iscrizione Procedimento Misura Sicurezza Disposta fuori Sentenza' appaiano anche i procedimenti di Appello contro Misure di Sicurezza emessi dal TDS. |  | A seguito di un'iscrizione di un Procedimento di Appello contro Misure di Sicurezza da parte del Tribunale di Sorveglianza e trasmesso alla Procura, verificare che il sistema mostri tale ordinanza nell'elenco sottostante alla funzione di 'Iscrizione Procedimento Misura Sicurezza Disposta fuori Sentenza'. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente richiama la funzione 'Gestione Misure di Sicurezza' |  | Il sistema mostra la pagina con le varie sotto funzioni. |  |
|  | 2.0 | Azione | L'utente sceglie la funzione  'Iscrizione Procedimento per Misura di Sicurezza applicata con ordinanza dal Magistrato di Sorveglianza e/o in sede di impugnazione dal Tribunale di Sorveglianza' |  | Il sistema mostra la pagina per inserire un filtro di ricerca per date. |  |
|  | 3.0 | Azione | L'utente imposta una data di interesse (può anche non specificare una data di interesse) e conferma la ricerca. |  | Il sistema effettua la ricerca e mostra l'elenco delle ordinanze/decreti emessi dalla Sorveglianza che applicano la Ms oppure ordinanze di Appello Contro Misure di Sicurezza. In caso di DBI diverse in riferimento alla Procura e Sorveglianza, per visualizzare i procedimenti di Applicazione di MS o di Appello Contro MS , la sorveglianza deve effettuare la trasmissione telematica del procedimento alla Procura. |  |
|  | 4.0 | Azione | L'utente seleziona il procedimento di interesse e continua l'inserimento. |  |  |  |
| 0015F015-TF01 | 01 | Verifica del link sulla Misura di Sicurezza riportata sulla pagina di dettaglio di un procedimento di classe IV. |  | Dopo aver cercato un procedimento di classe IV per cui è presente una misura di sicurezza, l'utente verifica che cliccando sul campo 'tipo misura' venga richiamata la funzione 'elenco misure di sicurezza' mostrando la pagina per l'associazione del titolo esecutivo. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente richiama la funzione 'Ricerca Procedimento' |  | Il sistema mostra la pagina di ricerca del procedimento per anno e numero. |  |
|  | 2.0 | Azione | L'utente inserisce anno e numero di un procedimento di classe IV che ha delle misure di sicurezza già inserite. |  | Il sistema mostra la pagina di dettaglio del procedimento trovato. |  |
|  | 3.0 | Azione | L'utente clicca sul campo 'Tipo Misura' |  | Il sistema mostra la pagina di dettaglio misure di sicurezza e la funzione 'Sostituzione Titolo Esecutivo Associato' |  |
| 0016F016-TF01 | 01 | Verificare che nella funzione 'Annotazione Decisione Sorveglianza' appaiano anche i procedimenti di Appello contro Misure di Sicurezza emessi dal TDS. |  | A seguito di un'iscrizione di un Procedimento di Appello contro Misure di Sicurezza da parte del Tribunale di Sorveglianza e trasmesso alla Procura, verificare che il sistema mostri tale ordinanza nell'elenco sottostante alla funzione di 'Annotazione Decisione Sorveglianza'. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente richiama la funzione 'Gestione Misure di Sicurezza' |  | Il sistema mostra la pagina con le varie sotto funzioni. |  |
|  | 2.0 | Azione | L'utente sceglie la funzione  'Annotazione Decisione Sorveglianza' |  | Il sistema mostra la pagina di ricerca procedimento. |  |
|  | 3.0 | Azione | L'utente inserisce un numero/anno di procedimento di classe IV per cui esiste un provvedimento di sorveglianza, in particolare un procedimento di appello contro MS. |  | Il sistema effettua la ricerca e mostra l'elenco delle ordinanze/decreti emessi dalla Sorveglianza che applicano la Ms oppure ordinanze di Appello Contro Misure di Sicurezza. In caso di DBI diverse in riferimento alla Procura e Sorveglianza, per visualizzare i procedimenti di Applicazione di MS o di Appello Contro MS , la sorveglianza deve effettuare la trasmissione telematica del procedimento alla Procura. |  |
|  | 4.0 | Azione | L'utente seleziona il procedimento di interesse e continua l'inserimento dell'annotazione. |  |  |  |
| 0017F017-TF01 | 01 | Stampa Comunicazione/Ordine Consegna a seguito provvedimento impugnazione. |  | Verificare la parametrizzazione dei template per emissione di un provvedimento di Comunicazione/Ordine Consegna a seguito provvedimento impugnazione. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente richiama la funzione 'Gestione Misure di Sicurezza' |  | Il sistema mostra la pagina con le varie sotto funzioni. |  |
|  | 2.0 | Azione | L'utente sceglie la funzione  'Annotazione Decisione Sorveglianza' |  | Il sistema mostra la pagina di ricerca procedimento. |  |
|  | 3.0 | Azione | L'utente inserisce un numero/anno di procedimento di classe IV per cui esiste un provvedimento di sorveglianza, in particolare un procedimento di appello contro MS. |  | Il sistema effettua la ricerca e mostra l'elenco delle ordinanze/decreti emessi dalla Sorveglianza che applicano la Ms oppure ordinanze di Appello Contro Misure di Sicurezza. |  |
|  | 4.0 | Azione | L'utente seleziona il procedimento di interesse e continua l'inserimento dell'annotazione. |  | Il sistema mosta la pagina di dettaglio. |  |
|  | 5.0 | Azione | L'utente stampa/valida il procedimento. |  | Il sistema mosta la pagina di dettaglio con i tasti per proseguire con l'emissione di un Ordine di Consegna, Ordine di Liberazione, Ordine di Internamento… |  |
|  | 6.0 | Azione | L'utente prosegue con l'emissione di un ordine di Consegna |  | Il sistema mosta la pagina di inserimento di un ordine di Consegna |  |
|  | 7.0 | Azione | L'utente inserisce i dati e prosegue con la conferma del form. Poi effettua la stampa del procedimento |  | Il sistema apre il documento di stampa parametrizzato per un provvedimento di appello. |  |
| 0018F018-TF01 | 01 | Stampa Ordine Esecuzione per Internamento a seguito provvedimento impugnazione. |  | Verificare la parametrizzazione dei template per emissione di un Ordine Esecuzione per Internamento a seguito provvedimento di impugnazione. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente richiama la funzione 'Gestione Misure di Sicurezza' |  | Il sistema mostra la pagina con le varie sotto funzioni. |  |
|  | 2.0 | Azione | L'utente sceglie la funzione  'Annotazione Decisione Sorveglianza' |  | Il sistema mostra la pagina di ricerca procedimento. |  |
|  | 3.0 | Azione | L'utente inserisce un numero/anno di procedimento di classe IV per cui esiste un provvedimento di sorveglianza, in particolare un procedimento di appello contro MS. |  | Il sistema effettua la ricerca e mostra l'elenco delle ordinanze/decreti emessi dalla Sorveglianza che applicano la Ms oppure ordinanze di Appello Contro Misure di Sicurezza. |  |
|  | 4.0 | Azione | L'utente seleziona il procedimento di interesse e continua l'inserimento dell'annotazione. |  | Il sistema mosta la pagina di dettaglio. |  |
|  | 5.0 | Azione | L'utente stampa/valida il procedimento. |  | Il sistema mosta la pagina di dettaglio con i tasti per proseguire con l'emissione di un Ordine di Consegna, Ordine di Liberazione, Ordine di Internamento… |  |
|  | 6.0 | Azione | L'utente prosegue con l'emissione di un ordine di Esecuzione per Internamento |  | Il sistema mosta la pagina di inserimento di un ordine di Esecuzione di Internamento. |  |
|  | 7.0 | Azione | L'utente inserisce i dati e prosegue con la conferma del form. Poi effettua la stampa del procedimento |  | Il sistema apre il documento di stampa parametrizzato per un provvedimento di appello. |  |
| 0019F019-TF01 | 01 | Stampa Ordine Liberazione a seguito provvedimento impugnazione. |  | Verificare la parametrizzazione dei template per emissione di un Ordine di Liberazione a seguito provvedimento di impugnazione. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente richiama la funzione 'Gestione Misure di Sicurezza' |  | Il sistema mostra la pagina con le varie sotto funzioni. |  |
|  | 2.0 | Azione | L'utente sceglie la funzione  'Annotazione Decisione Sorveglianza' |  | Il sistema mostra la pagina di ricerca procedimento. |  |
|  | 3.0 | Azione | L'utente inserisce un numero/anno di procedimento di classe IV per cui esiste un provvedimento di sorveglianza, in particolare un procedimento di appello contro MS. |  | Il sistema effettua la ricerca e mostra l'elenco delle ordinanze/decreti emessi dalla Sorveglianza che applicano la Ms oppure ordinanze di Appello Contro Misure di Sicurezza. |  |
|  | 4.0 | Azione | L'utente seleziona il procedimento di interesse e continua l'inserimento dell'annotazione. |  | Il sistema mosta la pagina di dettaglio. |  |
|  | 5.0 | Azione | L'utente stampa/valida il procedimento. |  | Il sistema mosta la pagina di dettaglio con i tasti per proseguire con l'emissione di un Ordine di Consegna, Ordine di Liberazione, Ordine di Internamento… |  |
|  | 6.0 | Azione | L'utente prosegue con l'emissione di un ordine di Liberazione. |  | Il sistema mosta la pagina di inserimento di un ordine di Liberazione. |  |
|  | 7.0 | Azione | L'utente inserisce i dati e prosegue con la conferma del form. Poi effettua la stampa del procedimento |  | Il sistema apre il documento di stampa parametrizzato per un provvedimento di appello. |  |
| 0020F020-TF01 | 01 | Statistica Riepilogo Iscrizioni e Tipologia Misura per procedimenti di classe IV. |  | Verificare l'output della statistica di tipologia 'Riepilogo Iscrizioni e Tipologia Misura' relativa a procedimenti di classe IV. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente richiama la funzione 'Statistiche/Monitoraggio - Statistiche - Estrazione Dati' |  | Il sistema mostra la pagina per la scelta della classe di interesse per la statistica. |  |
|  | 2.0 | Azione | L'utente sceglie la 'classe IV' e la statistica 'Riepilogo Iscrizioni e Tipologia Misura' |  | Il sistema mostra la pagina per inserire il periodo di interesse della statistica. |  |
|  | 3.0 | Azione | L'utente imposta una data di interesse e conferma la ricerca. |  | Il sistema genera un file .xsl con i risultati della statistica. |  |
| 0021F021-TF01 | 01 | Statistica 'Procedimenti Pendenti nel Periodo' per procedimenti di classe IV. |  | Verificare l'output della statistica di tipologia 'Procedimenti Pendenti nel Periodo' relativa a procedimenti di classe IV. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente richiama la funzione 'Statistiche/Monitoraggio - Statistiche - Estrazione Dati' |  | Il sistema mostra la pagina per la scelta della classe di interesse per la statistica. |  |
|  | 2.0 | Azione | L'utente sceglie la 'classe IV' e la statistica  'Procedimenti Pendenti nel Periodo' . |  | Il sistema mostra la pagina per inserire il periodo di interesse della statistica. |  |
|  | 3.0 | Azione | L'utente imposta una data di interesse e conferma la ricerca. |  | Il sistema genera un file .xsl con i risultati della statistica. |  |
| 0022F022-TF01 | 01 | Statistica 'Movimento procedimenti (Riepilogo Procedimenti Pendenti)'  per procedimenti di classe IV. |  | Verificare l'output della statistica di tipologia 'Movimento procedimenti (Riepilogo Procedimenti Pendenti)' relativa a procedimenti di classe IV. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente richiama la funzione 'Statistiche/Monitoraggio - Statistiche - Estrazione Dati' |  | Il sistema mostra la pagina per la scelta della classe di interesse per la statistica. |  |
|  | 2.0 | Azione | L'utente sceglie la 'classe IV' e la statistica  'Movimento Procedimenti (Riepilogo Procedimenti Pendenti)' . |  | Il sistema mostra la pagina per inserire il periodo di interesse della statistica. |  |
|  | 3.0 | Azione | L'utente imposta una data di interesse e conferma la ricerca. |  | Il sistema mostra la pagina con la lista delle macro categorie di stati procedimenti disponibili per la classe IV. |  |
|  | 4.0 | Azione | L'utente seleziona una particolare categoria e procede con la richiesta della statistica. |  | Il sistema genera un file .xsl con i risultati della statistica. |  |
| 0023F023-TF01 | 01 | Statistica 'Attività Magistrati' per procedimenti di classe IV. |  | Verificare l'output della statistica di tipologia 'Attività Magistrati' relativa a procedimenti di classe IV. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente richiama la funzione 'Statistiche/Monitoraggio - Statistiche - Estrazione Dati' |  | Il sistema mostra la pagina per la scelta della classe di interesse per la statistica. |  |
|  | 2.0 | Azione | L'utente sceglie la 'classe IV' e la statistica  'Attività Magistrati' . |  | Il sistema mostra la pagina per inserire il periodo di interesse della statistica. |  |
|  | 3.0 | Azione | L'utente imposta una data di interesse e conferma la ricerca. |  | Il sistema mostra una pagina presentando dei check di selezione per la tipologia di statistica 'Procedimenti Pendenti nel Periodo per Magistrati' e 'Attività Magistrati' |  |
|  | 4.0 | Azione | L'utente seleziona una particolare tipologia e seleziona il magistrato di interesse. |  | Il sistema genera un file .xsl con i risultati della statistica. |  |
| 0024F024-TF01 | 01 | Funzione di Inserimento Misure di Sicurezza. |  | Verificare la presenza della misura di sicurezza R.E.M.S. (Residenza per l'esecuzione delle Misure di Sicurezza) nella maschera di inserimento delle misure di sicurezza. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente ricerca un procedimento di classe I non validato. |  | Il sistema mostra la pagina di dettaglio del procedimento trovato. |  |
|  | 2.0 | Azione | L'utente, dal menù centrale, seleziona la funzione 'Inserisci Misura di Sicurezza' |  | Il sistema mostra la pagina per gestire l'inserimento della misura di sicurezza. |  |
|  | 3.0 | Azione | L'utente sceglie come tipologia 'detentiva' e nella combo delle misure appare anche la voce 'R.E.M.S. (Residenza per l'esecuzione delle Misure di Sicurezza)'. |  |  |  |
| 0025F025-TF01 | 01 | Funzione di Inserimento Misure di Sicurezza. |  | Verificare la presenza delle seguenti nuove misura di sicurezza nella maschera di inserimento delle misure di sicurezza:                                                                                                                              1. ESPULSIONE DELLO STRANIERO (ART. 235 C.P.)
2. ESPULSIONE DELLO STRANIERO DALLO STATO (ART. 312 C.P.)
3. ALLONTANAMENTO DELLO STRANIERO DALLO STATO (ART. 235 C.P.)
4. ALLONTANAMENTO DELLO STRANIERO DALLO STATO (ART. 312 C.P.) |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente ricerca un procedimento di classe I non validato. |  | Il sistema mostra la pagina di dettaglio del procedimento trovato. |  |
|  | 2.0 | Azione | L'utente, dal menù centrale, seleziona la funzione 'Inserisci Misura di Sicurezza' |  | Il sistema mostra la pagina per gestire l'inserimento della misura di sicurezza. |  |
|  | 3.0 | Azione | L'utente sceglie come tipologia 'non detentiva' e nella combo delle misure appaiono le nuove voci per esplulsione dallo stato. |  |  |  |
| 0026F026-TF01 | 01 | Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 cpp c. 2 . |  | Verificare che per il contenuto U082 (Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 cpp c. 2 ) gli oggetti associati siano:• Differimento della misura di sicurezza facoltativa attesa grazia
• Differimento della misura di sicurezza facoltativo grave infermità
• Differimento della misura di sicurezza facoltativo maternità
• Differimento della misura di sicurezza obbligatoria nei confronti di madre di infante di età inferiore ad anni uno
• Differimento della misura di sicurezza obbligatoria nei confronti di donna incinta
• Differimento della misura di sicurezza obbligatoria nei confronti di persona affetta da malattia |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIUS |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione e clicca sulla funzione 'Iscrizione Manuale'/'Ricerca titolo Esecutivo' |  | Il sistema mostra la pagina di ricerca del procedimento SIEP. |  |
|  | 1.0 | Navigazione | L'utente inserisce anno/numero di un titolo esecutivo SIEP esiste  e conferma la ricerca. |  | Il sistema mostra la pagina di dettaglio del procedimento trovato. |  |
|  | 2.0 | Azione | L'utente, dal menù centrale, seleziona la funzione 'Inserisci Procedimento' |  | Il sistema mostra la pagina per gestire l'inserimento del procedimento SIUS. |  |
|  | 3.0 | Azione | L'utente sceglie come CONTENTUTO la voce ' Rinvio esecuzione misura sicurezza ex art. 684 cpp c. 2 '  e clicca sul lla cartellina degli oggetti per contenuto. |  | Il sistema apre la pop-up con nuovi oggetti definiti per questo contenuto. |  |
| 0027F027-TF01 | 01 | Decreto di Rinvio esecuzione misura sicurezza ex art. 684 cpp c. 2 |  | Verificare che il sistema SIUS permette di inserire anche un decreto per il contenuto 'Rinvio esecuzione misura sicurezza ex art. 684 cpp c. 2 ' |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIUS |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione e clicca sulla funzione 'Iscrizione Manuale'/'Ricerca titolo Esecutivo' |  | Il sistema mostra la pagina di ricerca del procedimento SIEP. |  |
|  | 1.0 | Navigazione | L'utente inserisce anno/numero di un titolo esecutivo SIEP esiste  e conferma la ricerca. |  | Il sistema mostra la pagina di dettaglio del procedimento trovato. |  |
|  | 2.0 | Azione | L'utente, dal menù centrale, seleziona la funzione 'Inserisci Procedimento' |  | Il sistema mostra la pagina per gestire l'inserimento del procedimento SIUS. |  |
|  | 3.0 | Azione | L'utente sceglie come CONTENTUTO la voce ' Rinvio esecuzione misura sicurezza ex art. 684 cpp c. 2 '. Inserisce gli altri dati obbligatori e conferma l'operazioen di inserimento del procedimento SIUS. |  | Il sistema mostra il dettaglio del procedimento appena inserito. |  |
|  | 4.0 | Azione | L'utente si sposta sulla funzione 'Decreto/Emissione Decreto' |  | Il sistema mostra la pagina di inserimento del decreto. |  |
|  | 5.0 | Azione | L'utente inserisce i dati e conferma. |  |  |  |
| 0028F028-TF01 | 01 | Decreto di Rinvio esecuzione misura sicurezza ex art. 684 cpp (U077) |  | Verificare che nella pagina di inserimento di un decreto il contenuto 'Rinvio esecuzione misura sicurezza ex art. 684 cpp ' siano presenti i campi                                                                      • Data decorrenza differimento esecuzione
• Rinvio fino al 
• Rinvio nella misura di
per i seguenti esiti:                                                                                                                                                                                                                                                                                                                                             • RINVIA ESECUZIONE E ORDINA IL RICOVERO IN UNA CASA DI CURA O IN UN ALTRO LUOGO DI CURA (ART. 211 BIS C.P.)
• DIFFERISCE PROVVISORIAMENTE LA MISURA DI SICUREZZA |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIUS |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione e clicca sulla funzione 'Iscrizione Manuale'/'Ricerca titolo Esecutivo' |  | Il sistema mostra la pagina di ricerca del procedimento SIEP. |  |
|  | 1.0 | Navigazione | L'utente inserisce anno/numero di un titolo esecutivo SIEP esiste  e conferma la ricerca. |  | Il sistema mostra la pagina di dettaglio del procedimento trovato. |  |
|  | 2.0 | Azione | L'utente, dal menù centrale, seleziona la funzione 'Inserisci Procedimento' |  | Il sistema mostra la pagina per gestire l'inserimento del procedimento SIUS. |  |
|  | 3.0 | Azione | L'utente sceglie come CONTENTUTO la voce 'Rinvio esecuzione misura sicurezza ex art. 684 cpp'. Inserisce gli altri dati obbligatori e conferma l'operazione di inserimento del procedimento SIUS. |  | Il sistema mostra il dettaglio del procedimento appena inserito. |  |
|  | 4.0 | Azione | L'utente si sposta sulla funzione 'Decreto/Emissione Decreto' |  | Il sistema mostra la pagina di inserimento del decreto. |  |
|  | 5.0 | Azione | L'utente inserisce i dati e conferma. |  | Il sistema mostra la pagina per l'inserimento dell'esito. |  |
|  | 6.0 | Azione | L'utente sceglie l'esito 'DIFFERISCE PROVVISORIAMENTE LA MISURA DI SICUREZZA' |  | Il sistema mostra i nuovi campi                                                                                                                                                                                                                                                                                                                 •  Data decorrenza differimento esecuzione
• Rinvio fino al 
• Rinvio nella misura di |  |
| 0029F029-TF01 | 01 | Trasmissione ordinanze/decreti per UDS (U077 e U082) |  | Verificare che nella pagina di trasferimento decreto/ordinanza per un pocediemento di Rinvio esecuzione misura sicurezza ex art. 684 cpp e Rinvio esecuzione misura sicurezza ex art. 684 cpp c. 2 , tra gli ufficio destinatari del procedimento appaia l'ufficio titolare del procedimento di classe I (se presente) , di classe IV (se presente) e l'autorità Procura Generale. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIUS |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione e clicca sulla funzione 'Iscrizione Manuale/Ricerca titolo Esecutivo per numero SIEP' |  | Il sistema mostra la pagina di ricerca del procedimento SIEP. |  |
|  | 1.0 | Navigazione | L'utente inserisce anno/numero di un titolo esecutivo SIEP di classe IV che esiste  e conferma la ricerca. |  | Il sistema mostra la pagina di dettaglio del procedimento trovato. |  |
|  | 2.0 | Azione | L'utente, dal menù centrale, seleziona la funzione 'Inserisci Procedimento' |  | Il sistema mostra la pagina per gestire l'inserimento del procedimento SIUS. |  |
|  | 3.0 | Azione | L'utente inserisce un procedimento di ' Rinvio esecuzione misura sicurezza ex art. 684 cpp c. 2 '  e conferma. |  | Il sistema mostra la pagina di dettaglio del procedimento inserito |  |
|  | 4.0 | Azione | L'utente prosegue con l'emissione dell'ordinanza e con il deposito. |  | Il sistema mostra la pagina di dettaglio con l'icona del trasferimento (computer) |  |
|  | 5.0 | Azione | L'utente prosegue con la funzione di trasmissione. |  | Il sistema mostra la pagina di preparazione alla trasmissione mostrando tra le altre cose la lista degli uffici destinatari (classe I, classe IV e procura generale) con il relativo checkbx di selezione per la trasmissione. |  |
| 0030F030-TF01 | 01 | Ordinanza di Rinvio dell'esecuzione della misura sicurezza ex art. 684 |  | Verificare che la pagina di inserimento emissione ordinanza,  per il contenuto (Rinvio dell'esecuzione della misura sicurezza ex art. 684 )  consenta di inserire i seguenti dati: 
• Per l’esito ‘CONCEDE PER UN PERIODO’ (ESITO_TENORE = 0259) deve essere prevista la sezione dei dati del differimento (Data Decorrenza Differimento Esecuzione + Rinvio Fino al + Giorni, Mesi ed Anni di rinvio della misura)                                                                                                                                                                                                                                                                       • Per l’esito ‘CONCEDE E ORDINA IL RICOVERO IN UNA CASA DI CURA O IN ALTRO LUOGO DI CURA’ (ESITO_TENORE = 0260) deve essere previsto un ulteriore campo a testo libero per annotare la casa di cura o luogo di cura. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | Per l'esecuzione di questo test, si suppone che un ufficio UDS abbia trasmesso al TDS un procedimento di  Rinvio dell'esecuzione della misura sicurezza ex art. 684. |  |  |  |
|  | P | Stato Base | L'utente si logga sul sistema SIUS |  |  |  |
|  | P | Navigazione | L'utente si trova nella pagina principale dell'applicazione e clicca sulla funzione ' Presa in carico atti pervenuti » Ricerca per Atti - SIUS '
' |  | Il sistema mostra l'elenco degli atti SIUS pervenuti e disponibili al TDS |  |
|  | 1.0 | Azione | L'utente seleziona il procedimento di   Rinvio dell'esecuzione della misura sicurezza ex art. 684 ricevuto da UDS e procede con l'iscrizione di un suo procedimento di  Rinvio dell'esecuzione della misura sicurezza ex art. 684. (C036) |  |  |  |
|  | 2.0 | Azione | L'utente, dopo aver fissato l'udienza, si trova sulla pagina di inserimento dell'ordinanza. |  | Il sistema mostra la pagina per gestire l'inserimento dell'ordinanza. |  |
|  | 3.0 | Azione | L'utente inserisce la data, sceglie l'oggetto e prosegue con il tasto 'Confema'. |  | Il sistema mostra la pagina di inserimento dell'esito. |  |
|  | 4.0 | Azione | L'utente seleziona l'esito 'CONCEDE PER UN PERIODO'. |  | Il sistema sulla pagina di inserimento mostra ulterio campi, ossia: Data Decorrenza Differimento Esecuzione + Rinvio Fino al + Giorni, Mesi ed Anni di rinvio della misura |  |
|  | 5.0 | Azione | L'utente seleziona l'esito 'CONCEDE E ORDINA IL RICOVERO IN UNA CASA DI CURA O IN ALTRO LUOGO DI CURA'. |  | Il sistema sulla pagina di inserimento mostra ulterio campi, ossia: Data Decorrenza Differimento Esecuzione + Rinvio Fino al + Giorni + Mesi ed Anni di rinvio della misura + Luogo Ricovero. |  |
| 0031F031-TF01 | 01 | Pagina di dettaglio Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 |  | Verificare che  sulla pagina di dettaglio di Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 siano riportati i campi Data Decorrenza Differimento Esecuzione + Rinvio Fino al + Giorni + Mesi ed Anni di rinvio della misura + Luogo Ricovero. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente ha inserito già un'ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente ricerca il procedimento SIUS per il quale è stata emessa l'Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 |  | Il sistema mostra la pagina di dettaglio del procedimento trovato. |  |
|  | 2.0 | Azione | L'utente dlla lista dei provvediemtni, seleziona l'ordinanza  di Rinvio esecuzione misura sicurezza ex art. 684 |  | Il sistema mostra la pagina di dettaglio dell'ordinanza e visualizza i nuovi campi Data Decorrenza Differimento Esecuzione + Rinvio Fino al + Giorni + Mesi ed Anni di rinvio della misura + Luogo Ricovero. |  |
| 0032F032-TF01 | 01 | Pagina di modifica Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 |  | Verificare che  sulla pagina di modifica di Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 siano riportati i campi Data Decorrenza Differimento Esecuzione + Rinvio Fino al + Giorni + Mesi ed Anni di rinvio della misura + Luogo Ricovero e siano editabili. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente ha inserito già un'ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente ricerca il procedimento SIUS per il quale è stata emessa l'Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 |  | Il sistema mostra la pagina di dettaglio del procedimento trovato. |  |
|  | 2.0 | Azione | L'utente dlla lista dei provvediementi, seleziona l'ordinanza  (non validata) di Rinvio esecuzione misura sicurezza ex art. 684 |  | Il sistema mostra la pagina di dettaglio dell'ordinanza. |  |
|  | 3.0 | Azione | L'utente seleziona il pulsante per la modifica. |  | Il sistema mostra la pagina di modifica dell'ordinanza riportando i campi Data Decorrenza Differimento Esecuzione + Rinvio Fino al + Giorni + Mesi ed Anni di rinvio della misura + Luogo Ricovero  editabili. |  |
| 0033F033-TF01 | 01 | Stampa Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 |  | Verificare che la stampa vada a buon fine. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente ha inserito già un'ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 |  |  |  |
|  | P | Stato Base | L'utente si trova nella pagina principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente ricerca il procedimento SIUS per il quale è stata emessa l'Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 |  | Il sistema mostra la pagina di dettaglio del procedimento trovato. |  |
|  | 2.0 | Azione | L'utente dlla lista dei provvediementi, seleziona l'ordinanza  (non validata) di Rinvio esecuzione misura sicurezza ex art. 684 |  | Il sistema mostra la pagina di dettaglio dell'ordinanza. |  |
|  | 3.0 | Azione | L'utente seleziona il pulsante per la stampa. |  | Il sistema apre il documento associato. |  |
| 0034F034-TF01 | 01 | Trasmissione Ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 (C036) |  | Verificare che nella pagina di trasferimento ordinanza per un procedimento di Rinvio esecuzione misura sicurezza ex art. 684 cpp , tra gli ufficio destinatari del procedimento appaia l'ufficio titolare del procedimento di classe I (se presente) , di classe IV (se presente) e l'autorità Procura Generale. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIUS (TDS)  e L'utente ha inserito già un'ordinanza di Rinvio esecuzione misura sicurezza ex art. 684 |  |  |  |
|  | 1.0 | Navigazione | L'utente si trova nella pagina principale dell'applicazione e clicca sulla funzione 'Ordinanza/Deposito Ordinanza' |  | Il sistema mostra la pagina di ricerca del procedimento SIUS |  |
|  | 2.0 | Azione | L'utente inserisce anno/numero del procedimento SIUS  di Rinvio esecuzione misura sicurezza ex art. 684 (C036). |  | Il sistema mostra la pagina di dettaglio per il deposito dell'ordinanza. |  |
|  | 3.0 | Azione | L'utente prosegue con il deposito dell'ordinanza |  | Il sistema mostra la pagina di dettaglio con l'icona del trasferimento (computer) |  |
|  | 4.0 | Azione | L'utente prosegue con la funzione di trasmissione. |  | Il sistema mostra la pagina di preparazione alla trasmissione mostrando tra le altre cose la lista degli uffici destinatari (classe I, classe IV e procura generale) con il relativo checkbx di selezione per la trasmissione. |  |
| 0035F035-TF01 (01) | 01 | Pagina  inserimento ordinanza per procedimento di Appello Contro Provvedimento su Misura di Sicurezza (Art.  680 Cpp) |  | Verificare che la pagina di inserimento emissione ordinanza,  per il contenuto ((Appello Contro Provvedimento su Misura di Sicurezza (Art.  680 Cpp) )  consenta di inserire i seguenti dati: • Estremi del provvedimento impugnato ; • Dati della misura di sicurezza irrogata\in esecuzione.  ; • Sezione per inserire una ‘nuova misura’ |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIUS (TDS) |  |  |  |
|  | P | Navigazione | L'utente si trova nella pagina principale dell'applicazione e clicca sulla funzione 'Ricerche e Visualizzazioni » Procedimento per n° SIUS ' |  |  |  |
|  | 1.0 | Azione | L'utente inserisce anno/numero di un procedimento SIUS  di Appello Contro Provvedimento su Misura di Sicurezza (Art. 680 Cpp) per cui ancra non è stata inserita un'ordinanza |  | Il sistema mostra la pagina di dettaglio del procedimento. |  |
|  | 2.0 | Azione | L'utente,  prosegue con la fissazione udienza e si sposta sulla funzione di inserimento dell'ordinanza. |  | Il sistema mostra la pagina per gestire l'inserimento dell'ordinanza. |  |
|  | 3.0 | Azione | L'utente inserisce la data, sceglie l'oggetto e prosegue con il tasto 'Confema'. |  | Il sistema mostra la pagina di inserimento dell'esito. |  |
|  | 4.0 | Azione | L'utente seleziona l'esito 'Accoglie Appello e Modifica Mds '. |  | Il sistema sulla pagina di inserimento mostra i nuovi campi, ossia: Estremi del provvedimento impugnato ; Dati della misura di sicurezza irrogata\in esecuzione e la sezione per inserire la  ‘nuova misura’. |  |
|  | 5.0 | Azione | L'utente compila i dati obbligatori e procede cliccando sul tasto Conferma. |  | Il sistema mostra la pagina di  dettaglio dell'ordinanza inserita. |  |
|  | 6.0 | Azione | L'utente clicca sul tasto di modifica. |  | Il sistema mostra la pagina di modifica con i campi editabili. |  |
| 0035F035-TF01 (02) | 01 | Pagina  trasferimento procedimento per il contenuto C029 (Appello Contro Provvedimento su Misura di Sicurezza (Art.  680 Cpp)) |  | Verificare che nella pagina di trasferimento ordinanza per un procedimento di Appello Contro Provvedimento su Misura di Sicurezza (Art.  680 Cpp) , tra gli ufficio destinatari del procedimento appaia l'ufficio titolare del procedimento di classe I (se presente) , di classe IV (se presente) e l'autorità Procura Generale. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIUS (TDS)  e L'utente ha inserito già un'ordinanza di Appello Contro Provvedimento su Misura di Sicurezza (Art.  680 Cpp) |  |  |  |
|  | 1.0 | Navigazione | L'utente si trova nella pagina principale dell'applicazione e clicca sulla funzione 'Ordinanza/Deposito Ordinanza' |  | Il sistema mostra la pagina di ricerca del procedimento SIUS |  |
|  | 2.0 | Azione | L'utente inserisce anno/numero del procedimento SIUS  di Appello Contro Provvedimento su Misura di Sicurezza (Art.  680 Cpp) |  | Il sistema mostra la pagina di dettaglio per il deposito dell'ordinanza. |  |
|  | 3.0 | Azione | L'utente prosegue con il deposito dell'ordinanza |  | Il sistema mostra la pagina di dettaglio con l'icona del trasferimento (computer) |  |
|  | 4.0 | Azione | L'utente prosegue con la funzione di trasmissione. |  | Il sistema mostra la pagina di preparazione alla trasmissione mostrando tra le altre cose la lista degli uffici destinatari (classe I, classe IV e procura generale) con il relativo checkbx di selezione per la trasmissione. |  |
| 0035F035-TF01 (03) | 01 | Pagina  dettaglio procedimento per il contenuto C029 (Appello Contro Provvedimento su Misura di Sicurezza (Art.  680 Cpp)) |  | Verificare che nella pagina dettaglio procedimento per il contenuto C029 (Appello Contro Provvedimento su Misura di Sicurezza (Art.  680 Cpp)) sia  presente il link 'Misure di Sicurezza' e che mostri il dettaglio della misura. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIUS (TDS) |  |  |  |
|  | 1.0 | Navigazione | L'utente si trova nella pagina principale dell'applicazione e clicca sulla funzione 'Ricerche e Visualizzazioni » Procedimento per n° SIUS ' |  | Il sistema mostra la pagina di ricerca del procedimento SIUS |  |
|  | 2.0 | Azione | L'utente inserisce anno/numero di un procedimento SIUS  di Appello Contro Provvedimento su Misura di Sicurezza (Art. 680 Cpp) |  | Il sistema mostra la pagina di dettaglio del procedimento presentando il nuovo link 'Dettaglio Misure Sicurezza' |  |
|  | 3.0 | Azione | L'utente seleziona il link  'Dettaglio Misure Sicurezza' |  | Il sistema mostra la pagina di dettaglio con l'icona per l'inserimento. |  |
| 0036F036-TF01 | 01 | Pagina di Inserimento Misura di Sicurezza |  | Verificare che nella pagina di inserimento della misura di sicurezza ci sia la voce R.E.M.S. (Residenza per l'esecuzione delle Misure di Sicurezza) |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIUS (TDS) |  |  |  |
|  | 1.0 | Navigazione | L'utente si trova nella pagina principale dell'applicazione e clicca sulla funzione 'Ricerche e Visualizzazioni » Procedimento per n° SIUS ' |  | Il sistema mostra la pagina di ricerca del procedimento SIUS |  |
|  | 2.0 | Azione | L'utente inserisce anno/numero di un procedimento SIUS  di Appello Contro Provvedimento su Misura di Sicurezza (Art. 680 Cpp), oppure U023 (Applicazione Misura Sicurezza), U067 (Riesame pericolosità sociale) e U086 (Dichiarazione delinquenza abituale, professionale e per tendenza) |  | Il sistema mostra la pagina di dettaglio del procedimento pesentando il nuovo link 'Dettaglio Misure Sicurezza' |  |
|  | 3.0 | Azione | L'utente seleziona il link  'Dettaglio Misure Sicurezza' |  | Il sistema mostra la pagina di dettaglio con l'icona per l'inserimento. |  |
|  | 4.0 | Azione | L'utente seleziona la funzione 'Inserimento Misura di Sicurezza' |  | Il sistema mostra la pagina di inserimento della misura. |  |
|  | 5.0 | Azione | L'utente seleziona la natua  'misura detentiva' |  | Nella combo delle misure per tipologia detentiva, il sistema mostra la voce  R.E.M.S. (Residenza per l'esecuzione delle Misure di Sicurezza) |  |
|  | 6.0 | Azione | L'utente inserisce la durata della misura e conferma. |  |  |  |
| 0037F037-TF01 | 01 | Pagine Emissione Ordinanza |  | Verificare che nella pagina di emissione ordinanza per i contenuti U067 (Riesame pericolosità sociale) e U023 (Applicazione Misura Sicurezza), l’elenco delle misure mostrato nella pagina deve essere aggiornato con la nuova misura R.E.M.S. (Residenza per l'esecuzione delle Misure di Sicurezza) |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIUS (UDS) |  |  |  |
|  | 1.0 | Navigazione | L'utente si trova nella pagina principale dell'applicazione e clicca sulla funzione 'Iscrizione Manuale' |  |  |  |
|  | 2.0 | Azione | L'utente inserisce un procedimento di Riesame pericolosità sociale (U067) |  | Il sistema mostra la pagina di dettaglio del procedimento. |  |
|  | 3.0 | Azione | L'utente prosegue con l'emissione dell'ordinanza. |  | Il sistema mostra la pagina per gestire l'inserimento dell'ordinanza. |  |
|  | 4.0 | Azione | L'utente inserisce la data e l'oggetto e conferma. |  | Il sistema nella pagina per l'inserimento dell'esito. |  |
|  | 5.0 | Azione | L'utente seleziona l'esito 'SOSTITUISCE LA MISURA'. |  | Nella combo della nuova misura, il sistema mostra la voce  R.E.M.S. (Residenza per l'esecuzione delle Misure di Sicurezza). |  |
|  | 6.0 | Azione | L'utente inserisce la durata della misura e conferma. |  |  |  |
| 0038F038-TF01 | 01 | Inserimento Procedimento SIUS - Nuovo Oggetto per Esecuzione Misure di Sicurezza |  | Verificare che per il contenuto U024 (Esecuzione Misura Sicurezza), deve essere previsto un nuovo oggetto con denominazione R.E.M.S. (Residenza per l'esecuzione delle Misure di Sicurezza). Pertanto in fase iscrizione di un procedimento di Esecuzione Misura Sicurezza, in fase di selezione dell’oggetto, la pagina di elenco in popup deve mostrare anche la nuova misura R.E.M.S. (Residenza per l'esecuzione delle Misure di Sicurezza) |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente si logga sul sistema SIUS (UDS) |  |  |  |
|  | 1.0 | Navigazione | L'utente si trova nella pagina principale dell'applicazione e clicca sulla funzione 'Iscrizione Manuale' |  |  |  |
|  | 2.0 | Azione | L'utente inserisce un procedimento con contenuto Esecuzione Misura Sicurezza (U024) e clicca sull'icona per associare l'oggetto al contenuto scelto. |  | Il sistema apre la pagina di pop-up mostrandoo la lista degli oggetti per il contenuto Esecuzione Misura Sicurezza (U024). Nella lista deve essere presente la voce R.E.M.S. (Residenza per l'esecuzione delle Misure di Sicurezza) |  |