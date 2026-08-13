---
uniqueName: mev35-sospensione-esecuzione-pene-sostitutive
displayName: "MEV 35   Sospensione Esecuzione Pene Sostitutive"
category: "GENERAL"
tags: []
---

# MEV_35 - Sospensione Esecuzione Pene Sostitutive

> **File originale:** `MEV/SCHEDA_035/MEV_35 - Sospensione Esecuzione Pene Sostitutive.docx`  
> **Tipo:** DOCX

---

## Sospensione Esecuzione Pene Sostitutive
L’art. 660 c.p.p. al comma 15 prevede di richiedere la sospensione dell’esecuzione della pena sostitutiva nel caso che il soggetto chieda l’ammissione al pagamento rateale dopo l’inizio dell’esecuzione, d’altra parte l’art. 68 L. 689/81 prevede la Sospensione pena sostitutiva per sopravvenienza misura di sicurezza detentiva (art. 68  L.  689/81), la Sospensione pena sostitutiva per sopravvenienza pena detentiva (art.  68 L. 689/81).
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:
Sospensione Esecuzione Pene Sostitutive (U134 – S30)
Al nuovo contenuto vanno associati i seguenti oggetti:
Sospensione pena sostituiva per ammissione al pagamento rateale (art.660 c.15 c.p.p.) (3135)
Sospensione pena sostituiva per sopravvenienza misura di sicurezza detentiva (art. 68 L. 689/1981)
(3136)
Sospensione pena sostituiva per sopravvenienza pena detentiva (art. 68 L. 689/1981) (3137)
ed i seguenti esiti:
Sospende (0136)
Non sospende (0078)
Dichiara N.D.P. / N.L.P. (0004)
Dichiara inammissibilità (0003)
Dichiara la propria incompetenza (0005)
Questo tipo di procedimento presuppone l’esistenza del fascicolo “padre” di Esecuzione Pene Sostitutive (U126), pertanto, l’iscrizione sarà simile a quella dei procedimenti figli dell’Esecuzione Sanzione Sostitutiva, e richiederà di indicare obbligatoriamente l’Anno e Numero del Procedimento di EPS:

A seguito della compilazione della form e successiva Conferma, il sistema presenterà la form di Dettaglio del procedimento “figlio” del procedimento di esecuzione pena sostitutiva


Caratterizzata da un proprio Anno e Numero e dal numero del procedimento padre (EPS).
Per i procedimenti di sospensione della sanzione pena sostitutiva, SIUS permetterà di definire il procedimento con un decreto o un’ordinanza. Saranno, quindi, implementate due nuove funzionalità, emissione del decreto Sospensione Esecuzione Pene Sostitutive ed emissione dell’ordinanza Sospensione Esecuzione Pene Sostitutive, che conterranno dati relativi, rispettivamente, al decreto e all’ordinanza. Le nuove due maschere saranno implementate sulla base di quella abbozzata di seguito (rifarsi ai provvedimenti utilizzati per U060):

L’ordinanza seguirà il normale percorso di altri provvedimenti, verrà validata, quindi depositata e validata per essere trasmesso allo stesso Ufficio o ad altro ufficio.
L’ordinanza di sospensione viene trasmessa anche alla Procura perché provveda all’annotazione.
Quanto detto per l’ordinanza vale anche per il decreto.
A seguito della Conferma del decreto e dell’ordinanza, il sistema effettuerà il salvataggio dei dati nella base dati e presenterà le rispettive form di Dettaglio, dalle quali sarà possibile attivare le azioni di Modifica, Cancellazione, Stampa o Upload e Validazione.
Per questi provvedimenti devono essere previsti i seguenti quattro modelli di stampa che sono automaticamente memorizzati in un campo BLOB della base dati: Ordinanza Sospensione per pena detentiva, Ordinanza generica, Decreto Sospensione per pena detentiva, Decreto generico.

SIUS_OR_SOSPPSPENADET.rtf, SIUS_OR_MODGENERICOPS.rtf, SIUS_DE_SOSPPSPENADET.rtf, SIUS_DE_MODGENERICOPS.rtf

Per quanto riguarda l’esigenza di rivedere la gestione dei differimenti, come realizzata nell’ambito delle esecuzioni delle sanzioni sostitutive, adottando una soluzione più semplificata, simile a quella utilizzata nell’ambito dell’esecuzioni delle misure alternativa, si rimanda la scelta della soluzione, in base a quanto sarà deciso dai magistrati dei GdL SIEP/SIUS in merito alla competenza sulla gestione dell’esecuzione delle Pene Sostitutive (Procure o Uffici di Sorveglianza?).

Interventi da realizzare sull’ordinanza e decreto
Al momento al contenuto U134 è stata associata la form utilizzata per il contenuto U060 Tipo_Decreto = 35 e TIPO_ORDINANZA = 35
Dal debug sembra che in ambedue i casi venga richiamata /jsp/files/siap/sius/depositodecreto/InserisciDecretoSospensioneEsecuzioneSanzioniSostitutive.jsp
La form presentata va sostanzialmente bene, andrebbero effettuate le modifiche riportate nei riquadri in rosso

La fase di inserimento è tutto OK, c’è da rivedere la form di Dettaglio, in cui bisogna modificare tutte le diciture ‘Sanzione’ in ‘Pena’


Stesso intervento anche sulla Modifica



(Stessi interventi vanno fatti anche sul Decreto)