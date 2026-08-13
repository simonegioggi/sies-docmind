---
uniqueName: mev35-sospensione-pena-accessoria
displayName: "MEV 35   Sospensione Pena Accessoria"
category: "GENERAL"
tags: []
---

# MEV_35 - Sospensione Pena Accessoria

> **File originale:** `MEV/SCHEDA_035/MEV_35 - Sospensione Pena Accessoria.docx`  
> **Tipo:** DOCX

---

3.21 e 3.22	Sospensione esecuzione pene accessorie (UDS) e (TDS)
L’art.  51 quater O.P. (disciplina delle pene accessorie in caso di concessione di misure alternative) prevede che l’Ufficio di Sorveglianza possa decidere la sospensione dell’esecuzione delle pene accessorie in caso di misure alternative o di pene sostitutive.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:
Sospensione esecuzione pene accessorie (art. 51-quater O.P.)

Al nuovo contenuto vanno associati i seguenti oggetti:
Sospensione esecuzione pene accessorie – Misure alternative (art. 51-quater O.P.)
Sospensione esecuzione pene accessorie – Pene sostitutive (Art.  76 L. 689/81 – 51-quater O.P.)
ed i seguenti esiti:
Sospende
Non sospende
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza
Questo tipo di procedimento non presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva/Esecuzione Misura Alternativa, pertanto l’iscrizione, fuoriuscendo dalla logica procedimenti “padre” – “figli”, avverrà utilizzando le attuali funzionalità di iscrizione previste in SIUS.
E’ possibile procedere alla definizione di questo procedimento emettendo un’ordinanza di Sospensione Esecuzione pena accessorie; dobbiamo creare una nuova ordinanza tipo_ordinanza = ‘PA’ valida per U141 e C066. Utilizziamo come base l’ordinanza 35 prevista per il contenuto U134 (Sospensione esecuzione pene sostitutive) ed aggiungiamo la parte evidenziata nel riquadro rosso:

In cui nella combo box Tipo saranno presenti tutti i tipi di pena accessoria di cui all’art. 19 c.p., e quindi:
1) interdizione dai pubblici uffici;
2) interdizione da una professione o da un'arte;
3) interdizione legale;
4) incapacità di contrattare con la pubblica amministrazione;
4-bis) estinzione del rapporto d’impiego o di lavoro;
5) decadenza o la sospensione dall'esercizio della responsabilità genitoriale;
6) sospensione dall'esercizio di una professione o di un'arte;
7) pubblicazione della sentenza penale di condanna.
Bisogna estrarre dal dominio ‘TIPO_PENA_ACCESSORIA’ i records con RV_HIGH_VALUE = ‘PS’.
Per quel che concerne la durata della pena accessoria irrogata sarà presente la combo Tipo Durata in cui sarà possibile selezionare tra Perpetua e Durante la pena (per la quale bisognerà indicare la durata nei successivi campi). (vale quanto previsto nell’iscrizione p.a. SIEP).
Da valutare se, Per la memorizzazione della pena accessoria sospesa, sia opportuno utilizzare la tabella PENA_ACCESSORIA, attualmente collegata solo a fascicolo_siep, collegandola anche a Fascicolo_SIUS in alternativa all’altra FK oppure aggiungere nuove colonne su Deposito_ordinanza_pc od utilizzare colonne già presenti destinate a contenere altre info per altre tipologia di ordinanza.
A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio:

dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
Al momento per questo provvedimento saranno previsti due modelli di stampa, che, quando generati, sono memorizzati in un campo BLOB della base dati: ordinanza di sospensione della pena accessoria, ordinanza generica.
Per completezza riporto di seguito i par. della scheda intervento, in cui vi sono i codici utilizzati.
3.21	Sospensione esecuzione pene accessorie (UDS)
L’art.  51 quater O.P. (disciplina delle pene accessorie in caso di concessione di misure alternative) prevede che l’Ufficio di Sorveglianza possa decidere la sospensione dell’esecuzione delle pene accessorie in caso di misure alternative o di pene sostitutive.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:
Sospensione esecuzione pene accessorie (art. 51-quater O.P.)   			(U141)
Al nuovo contenuto vanno associati i seguenti oggetti:
Sospensione esecuzione pene accessorie – Misure alternative (art. 51-quater O.P.)
(3175)
Sospensione esecuzione pene accessorie – Pene sostitutive (Art.  76 L. 689/81 – 51-quater O.P.)  				(3176)
ed i seguenti esiti:
Sospende   				(0136)
Non sospende   			(0078)
Dichiara N.D.P./ N.L.P   		(0004)
Dichiara inammissibilità   		(0003)
Dichiara la propria incompetenza  	(0005)
Questo tipo di procedimento non presuppone l’esistenza del fascicolo “padre” di Esecuzione Pena Sostitutiva/Esecuzione Misura Alternativa, pertanto l’iscrizione, fuoriuscendo dalla logica procedimenti “padre” – “figli”, avverrà utilizzando le attuali funzionalità di iscrizione previste in SIUS.
Per questo tipo di procedimento sarà implementata una nuova funzionalità, emissione ordinanza sospensione esecuzione pena accessoria: la nuova maschera di inserimento sarà implementata sulla base di quella abbozzata di seguito:

In cui nella combo box Tipo saranno presenti tutti i tipi di pena accessoria di cui all’art. 19 c.p., e quindi:
1) interdizione dai pubblici uffici;
2) interdizione da una professione o da un'arte;
3) interdizione legale;
4) incapacità di contrattare con la pubblica amministrazione;
4-bis) estinzione del rapporto di impiego o di lavoro;
5) decadenza o la sospensione dall'esercizio della responsabilità genitoriale;
6) sospensione dall'esercizio di una professione o di un'arte;
7) pubblicazione della sentenza penale di condanna.
Per quel che concerne la durata della pena accessoria irrogata sarà presente la combo Tipo Durata in cui sarà possibile selezionare tra Perpetua e Durante la pena (per la quale bisognerà indicare la durata nei successivi campi). A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione. Al momento per questo provvedimento saranno previsti due modelli di stampa , che, quando generati, sono memorizzati in un campo BLOB della base dati: ordinanza di sospensione della pena accessoria, ordinanza generica.
3.22	Sospensione esecuzione pene accessorie (TDS)
L’art.  51 quater O.P. (disciplina delle pene accessorie in caso di concessione di misure alternative) prevede la sospensione dell’esecuzione delle pene accessorie  in caso di misure alternative possa essere decisa anche dal Tribunale di Sorveglianza.
Nell’ambito dell’Ufficio di Sorveglianza (TDS/TDSM), il contenuto da integrare è il seguente:
Sospensione esecuzione pene accessorie (art. 51-quater O.P.)  			(C066)
Al nuovo contenuto vanno associati i seguenti oggetti:
Sospensione esecuzione pene accessorie – Misure alternative (art. 51-quater O.P.) (9090)
ed i seguenti esiti:
Sospende   				(0136)
Non sospende   			(0078)
Dichiara N.D.P./ N.L.P   		(0004)
Dichiara inammissibilità   		(0003)
Dichiara la propria incompetenza  	(0005)
Questo tipo di procedimento non presuppone l’esistenza del fascicolo “padre” di Esecuzione Misura Alternativa, pertanto l’iscrizione, fuoriuscendo dalla logica procedimenti “padre” – “figli”, avverrà utilizzando le attuali funzionalità di iscrizione previste in SIUS.
Per questo tipo di procedimento si può ipotizzare la stessa ordinanza descritta al precedente paragrafo:

A seguito della Conferma, il sistema inserirà la nuova ordinanza nella base dati e presenterà la form di Dettaglio, dalla quale sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
Al momento per questo provvedimento saranno previsti due modelli di stampa , che, quando generati, sono memorizzati in un campo BLOB della base dati: ordinanza di sospensione della pena accessoria, ordinanza generica.