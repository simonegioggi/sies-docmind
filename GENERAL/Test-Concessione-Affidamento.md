---
uniqueName: test-concessione-affidamento
displayName: "Test Concessione Affidamento"
category: "GENERAL"
tags: []
---

# Test Concessione Affidamento

> **File originale:** `MEV/SCHEDA_009/Test Concessione Affidamento.docx`  
> **Tipo:** DOCX

---

Test Concessione/Ratifica Affidamento
Concessione con rito ordinario nuovo oggetto, compilazione form manuale

A seguito inserimento il sistema presenta la seguente form di Dettaglio

Ha inserito correttamente una Richiesta verbale …..

Se provo a stampare mi genera SIEP_VUOTO, che probabilmente dovrebbe essere stato risolto con l’inserimento dei template.
In caso di Detenuto (2017/804), sempre con inserimento manuale dei dati della Sorveglianza, relativi a rito ordinario per i nuovi oggetti, il sistema inserisce un OS ma con cod_motivo = 5443 generando un evento: (Ordine Scarcerazione  Verbale sottoscrizione obblighi - Affidamento in Prova al Servizio Sociale (Art. 47 O.P. - Art. 678 comma 1-ter c.p.p.) )

Che fa riferimento erroneamente al Verbale sottoscrizione…., mentre dovrebbe far riferimento a 0680 in modo da avere Ordine Scarcerazione Affidamento in Prova al Servizio Sociale (Art. 47 O.P. -  Art. 678 comma 1-ter c.p.p.).
Il Dettaglio si presenta senza intestazione, come il precedente.
Ho verificato che se modifico il cod_motivo da 5443 a 0680, nel dettaglio appare l’intestazione.
Quindi in pratica, a parte quando è previsto l’inserimento della Richiesta Verbale…, negli altri casi Concessione con rito ordinario, il sistema deve gestire i codici 0680, 0681, 0690, 0691, 0692 alla stessa maniera di come vengono gestiti gli attuali codici 0001,0002,0003 anche ai fini della gestione dei template.
Per quanto riguarda la gestione dei template, Diego ha già applicato la suddetta gestione in caso di ammissione provvisoria ad affidamento in prova. Se serve raccordati con lui.
#####################################################################################
Proc. 2010/863 PM Roma - Concessione/Ratifica affidamento in prova,
quando si seleziona dalla lista non estrae l'ordinanza di Conferma della Sorveglianza!
Potresti ordinare la combo box degli oggetti alfabeticamente asc!
In caso di Ratifica (vedi. 2001/325) in fase di inserimento il cod_tipo_provvedimento deve essere 12 invece di 26, l'aggancio dei template per i cod_motivo da 5460 a 5464 deve avvenire cercando nella tabella template direttamente con questi codici e non attraverso il codice dell'evento dell'ordinanza.