---
uniqueName: sigipnlpt-2019-06-19-1-0mev-problema-code-jms
displayName: "SIGI PNL PT 2019 06 19  1 0 MEV PROBLEMA CODE JMS"
category: "GENERAL"
tags: []
---

# SIGI_PNL_PT-2019 06 19 -1.0_MEV PROBLEMA CODE JMS

> **File originale:** `MEV/VERSIONE_SIES_11.3_NEW/INTERVENTO_PROBLEMA_DBI/SIGI_PNL_PT-2019 06 19 -1.0_MEV PROBLEMA CODE JMS.xls`  
> **Tipo:** XLS

---

## Copertina

|  |  |  |  |
| --- | --- | --- | --- |
|  | Ministero della Giustizia |  |  |
|  | Piano di Test |  |  |
|  | MEV PROBLEMA CODE JMS |  |  |
|  |  | Codice documento: | SIGI-PNL-PT |
|  |  | Versione: | 1.0 |
|  |  | Data Versione: | 19/06/2019 |

## Approvazioni_Revisioni

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
|  | Approvazioni |  |  |  |
|  | Titolo | MEV PROBLEMA CODE JMS |  |  |
|  | Codice doc | SIGI-PNL-PT |  |  |
|  | MEV PROBLEMA CODE JMS |  |  | Data |
|  | Redatto da | Vito N. Bufi |  | 19/06/2019 |
|  | Verificato | Vito N. Bufi |  | 19/06/2019 |
|  | Approvato da | Vito N. Bufi |  | 19/06/2019 |
|  | Responsabile | P. Ceccanti |  |  |
|  | Cliente e/o utenti | Ministero della Giustizia |  | n.a. |
|  | Direzione | SIGI-PNL-PT |  |  |
|  | 1.0 |  |  |  |
|  | Revisioni |  |  |  |
|  | Data | Versione | Autore/i | Descrizione |
|  | 43635.0 | 1.0 | Vito N. Bufi | Prima emissione |

## Documenti di riferimento

| Tipo documento | Nome documento |
| --- | --- |
| Richiesta PEC | SEGNALAZIONE m_dg.DOG07.06-08-2018.0025591.U |

## Tabella dei Test

|  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Tabella dei Test |  |  |  |  |  |  |  |  |
| Funzionalità / Requisiti |  |  |  |  |  | Caso di test |  |  |
| ID. Requisito | MEV PROBLEMA CODE | ID | Secondo Livello | ID | Terzo livello | ID | Nome del caso di test | Descrizione e note |
| Ricerca Soggetto altre DBI | Sistema SIEP | 0001 | Ricerche » Procedimento per Soggetto | F001 | Ricerche » Procedimento per Soggetto » In altri distretti | 0001F001-TF01 | Verifica della gestione dell'errore delle code jms dovuto a diseallineamento dei deploy tra due diversi distretti. | Procedere con la ricerca di un soggetto in altri distretti. Il distretto destinatario deve avere una versione diversa del sies. Il sistema deve restituire l'errore 'ISTALLAZIONI INCOMPATIBILI'. |

## Dettaglio Test

| ID caso di test | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
| --- | --- | --- | --- | --- | --- | --- |
| 0001F001-TF01 | 01 | Verifica della gestione dell'errore delle code jms dovuto a diseallineamento dei deploy tra due diversi distretti. |  | Procedere con la ricerca di un soggetto in altri distretti. Il distretto destinatario deve avere una versione diversa del sies. Il sistema deve restituire l'errore 'ISTALLAZIONI INCOPATIBILI'. |  |  |
|  | Step | Tipo | Istruzioni
(text) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esecuzione test |
|  | P | Attività Preliminari e/o Precondizioni | L'utente deve effettuare l'accesso al sistema SIEP |  |  |  |
|  | P | Stato Base | L'utente è sulla maschera principale dell'applicazione. |  |  |  |
|  | 1.0 | Navigazione | L'utente si sposta sul menù Ricerche. Poi procede con la funzione 'Procedimento per Soggetto' e sceglie l'opzione 'In altri distretti'. |  | Il sistema prospetta la maschera per inserire i dati del soggetto e scegliere la BDI di ricerca. |  |
|  | MEV PROBLEMA CODE JMS | Azione | Il soggetto inserisce i dati di un soggetto (anche non reale) e deve scegliere una BDI di ricerca che abbia un deploy diverso (successivo alla versione oggetto del collaudo). |  | Il sistema sottomette la richiesta a sistema. |  |
|  | 3.0 | Azione | L’utente prosegue con la ricerca degli 'esiti' dal menù 'Esiti Ricerca Soggetto su altre BDI '. |  | Il sistema mostra la pagina con l'elenco dei messaggio con i relativi esiti. Deve essere presente anche un messaggio con il seguente esito 'Installazione locale del SIES incompatibile rispetto al distretto corrente'. |  |