---
uniqueName: siut-sies-vv-1-0-20200514-analisi-errori-connessio
displayName: "SIUT SIES VV 1 0 20200514 Analisi Errori Connessioni   Scheda 2019 006 Ottimizza"
category: "GENERAL"
tags: []
---

# SIUT-SIES-VV-1.0-20200514 Analisi Errori Connessioni - Scheda 2019_006_Ottimizzazione SIUS Avvocati

> **File originale:** `MEV/SCHEDA_006/SIUT-SIES-VV-1.0-20200514 Analisi Errori Connessioni - Scheda 2019_006_Ottimizzazione SIUS Avvocati.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |



Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Emma Caporizzo – Monia Grippa | Analista funzionale – Team Leader |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 14/05/2020 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 14/05/2020 | Prima Emissione |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Pasquale Lamattina | RTI |  | Referente Tecnico |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Fabio Mazzocchi | RTI |  | Responsabile Manutenzione Correttiva |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Responsabile PMO |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Edoardo Lamuraglia | RTI |  | Referente qualità |
| Francesco Rosati | RTI |  | Referente qualità |


INDICE DEI CONTENUTI
1.	Introduzione	5
1.1.	Scopo del documento	5
1.2.	Riferimenti	5
1.3.	Glossario	5
1.3.1.	Definizioni	5
1.3.2.	Acronimi e abbreviazioni	5
2.	Analisi	6
2.1.	Cronistoria	6
2.2.	Studio del log	6
2.3.	Prospettiva di intervento	8
3.	Piano delle attività	19
3.1.	Ciclo di sviluppo	19
3.2.	Piano delle attività	19
3.3.	Gantt	19
4.	Dimensionamento	21
4.1.	Stima dell'effort previsto	21
4.2.	Dettaglio costi	21


# Introduzione
## Scopo del documento

Nel presente documento si espone l’analisi dei log forniti, delle classi java e le attività da intraprendere per la rimozione degli errori sulle connessioni presenti nell’applicativo SIES.
## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
|  | SIUT-GEN-SC-1.1-20191015 Scheda intervento SIUS_Avvocati.pdf | Scheda di Intervento |
|  | SIUT-SIES-MG-1.1-20200312- Ottimizzazione SIUS.pdf | Configurazione e  monitoraggio |

## Glossario
## Definizioni
| Definizione | Descrizione |
| --- | --- |
|  |  |

## Acronimi e abbreviazioni
| Sigla | Descrizione |
| --- | --- |
| DEC | Direttore Esecutivo Contratto |
| DGSIA | Direzione Generale per i Sistemi Informativi Automatizzati |
| PA | Pubblica Amministrazione |
| PEC | Posta Elettronica Certificata |
| PMO | Program Management Office |
| POO | Program Operating Office |
| QM | Quality Manager |
| RTI | Raggruppamento Temporaneo di Impresa |
| RUF | Responsabile Unico Fornitore |
| RUP | Responsabile Unico Progetto |
| SAL | Stato Avanzamento Lavori |
| SGQ | Sistema di Gestione per la Qualità di Engineering Ingegneria Informatica S.p.A. |
| SIU | Sistema Informativo Unitario |
| SLA | Service Level Agreement |
| SW | SoftWare |



# Analisi
## Cronistoria
In data 24 aprile, (cfr. PEO A. Maffuci – “Scheda 6 - programmazione attività ; data invio log posticipata”), l’Amministrazione, comunica l’attivazione dei parametri di monitoring della Cached Connection Manager secondo quanto riportato al documento SIUT-SIES-MG-1.1-20200312- Ottimizzazione SIUS.pdf

Come distretto deputato al monitoring è stato individuato l’ambiente di esercizio SIES DISTRETTO DI NAPOLI. Lo scopo era recuperare i file di log per poter individuare le cause di saturazione delle connessioni oracle dall’applicativo SIES.

A valle delle attività di utilizzo del sistema, con la ‘registrazione’ delle informazioni nel file server.log, tramite PEO del giovedì 30/04/2020 15:51 (cfr. A. Maffuci – “R: Scheda 6 - programmazione attività; data invio log posticipata”) sono tati forniti il file relativi a 7 giorni di utilizzo su cui, la presente relazione è stata improntata.
## Studio del log

A seguito dell’analisi dei log prodotti dall’applicativo SIES nei giorni che vanno dal 24/04/2020 al 30/04/2020 nell’ambiente di esercizio di NAPOLI, si riportano le classi per le quali si è registrato il messaggio di WARNING restituito dalle api jca.core di jboss (org.jboss.jca.core.api.connectionmanager.ccm.CachedConnectionManager) che evidenziano la presenza di ‘unclosed statement’ (non chiusura di statement Oracle), in fase di rilascio di una connessione.

Le classi registrate con il warning sono:
siap.siep.istruttoriacumulo.controller.IstruttoriaCumuloController.titoloDoppioInIstruttoria (IstruttoriaCumuloController.java:3776)

In questa specifica classe le occorrenze registrate del warning sono 48

siap.sige.tenore.controller.TenoreSigeController.ExRicercaTenoreByRichiesta (TenoreSigeController.java:133)

In questa specifica classe le occorrenze registrate del warning sono 102

siap.sige.tenore.controller.TenoreSigeController.ExControlloDataIrrevocabilita (TenoreSigeController.java:1091)

In questa specifica classe le occorrenze registrate del warning sono 75

siap.sige.tenore.controller.TenoreSigeController.ExRicercaTenoreByProvvedimento (TenoreSigeController.java:1132)

In questa specifica classe le occorrenze registrate del warning sono 8

siap.sige.tenore.controller.TenoreSigeController.ExRicercaSentenzeByRichiestaAndIdTen oreSige(TenoreSigeController.java:1388)

In questa specifica classe le occorrenze registrate del warning sono 103

Con l’analisi del codice corrispondente al punto in cui si presenta il warning si è riusciti a delineare il perimetro di intervento per rimuovere il malfunzionamento registrato.
In particolare ci si è accorti che in corrispondenza della sezione delle classi java predisposta alla chiusura delle connessioni, manca la parte di chiusura del ResultSet e del PrepareStatement.
Genericamente, l’oggetto java PrepareStatement, nella programmazione java, viene utilizzato per ‘preparare’ le istruzioni di interrogazioni alla base dati passando, ad esempio, in input una lista di parametri, mentre il ResultSet è l’oggetto in cui confluiscono i risultati ottenuti dall’interrogazione.

Nella gestione degli accessi alla base dati, il rilascio delle risorse allocate durante le operazioni su database, è particolarmente critica in quanto il numero totale delle connessioni disponibili è limitato e normalmente la connessione al DB non viene rilasciata automaticamente quando non è più utilizzata.
Pertanto, bisogna prestare particolare attenzione a verificare che ogni risorsa, vedi l’oggetto PrepareStatement, ResultSet e non ultimo la Connection vengano correttamente chiuse dopo il loro utilizzo.

## Prospettiva di intervento

In merito a ciò, il lavoro sarà verificare che ogni risorsa utilizzata per l’accesso alla base dati sia stata correttamente rilasciata, e per le casistiche in cui si presenterà l’errore di ‘non rilascio’ della risorsa, si interverrà con la rettifica del codice java.

Si stima che il numero di classi da verificare siano 260. L’intervento sarà individuabile con il seguente commento:
// Scheda Intervento n° 6 - Ottimizzazione SIUS Avvocati

Elenchiamo le classi su cui si interverrà per la verifica e l’eventuale azione correttiva:












# Piano delle attività
## Ciclo di sviluppo

Il ciclo di sviluppo utilizzato è quello Waterfall.
## Piano delle attività
Per il piano delle attività si faccia riferimento al paragrafo 3.3
## Gantt
Di seguito si riporta il gantt delle attività.





# Dimensionamento
## Stima dell'effort previsto

La stima aggiornata prevista è di 13 giorni per un importo pari a euro 4.927,00.

## Dettaglio costi


| Obiettivo | Descrizione Risorsa | Numero GG | Importo giornaliero | Totale |
| --- | --- | --- | --- | --- |
| Scheda_2019_006 | Team leader di sviluppo | 1 | 379 | 379,00 € |
| Scheda_2019_006 | Analista programmatore  senior | 12 | 379 | 4.548,00 € |
| Scheda_2019_006 | Progettista / Software Architect | 0 | 379 | 0,00 € |
| Scheda_2019_006 | DB Administrator | 0 | 379 | 0,00 € |
|  | Totali | 13 |  | 4.927,00 € |