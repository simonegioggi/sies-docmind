---
uniqueName: 20210924considerazioniregindesies-con-annotazioni-
displayName: "20210924 Considerazioni Reginde SIES con annotazioni   con risposte  BOZZA "
category: "GENERAL"
tags: []
---

# 20210924_Considerazioni_Reginde_SIES con annotazioni - con risposte (BOZZA)

> **File originale:** `MEV/SCHEDA_021/Docs/20210924_Considerazioni_Reginde_SIES con annotazioni - con risposte (BOZZA).docx`  
> **Tipo:** DOCX

---

In relazione al documento “SIUT-SIE-SI-2.3-20210730-Specifiche-intervento-021-SIES”, si inoltrano le seguenti osservazioni da inoltrare all’RTI.
Paragrafo 6.2 pag. 40: bisogna che l’RTI preveda dei test specifici per simulare il malfunzionamento del Reginde per verificare come avviene la ricerca sulla base dati locale.
Risposta: in realtà il caso richiamato a pag.40 è poi descritto in dettaglio, come già riportato alla riga 6 [Rif. § “6.3 REQ-SIE-021-03_FN.01 - Inserimento Manuale: Indisponibilità ReGIndE o Avvocato Non Presente”), al par. 6.3 pag.74 riga 4 inserita seguente
Nota: Per simulare l’assenza del collegamento a ReGIndE, bisogna modificare il file “f3b.properties”, presente nel percorso “/var/SIES/CONFIG”, commentare col carattere “#” la seguente riga necessaria al collegamento col server nazionale del sistema ReGIndE:
#EndpointAddress=http://reginde.processotelematicotest.giustizia.it

Paragrafo 6.2.5 pag. 71: va indicato l’url corretto del Reginde.
Per il pre-esercizio è http://reginde.processotelematicotest.giustizia.it
Per l’esercizio è http://reginde.processotelematico.giustizia.it.
Risposta: A pag. 71 riga 11 la frase seguente:
L’endpoint di interesse è identificato dalla seguente url:
https://XX.XXX.XXXX.XXX/ServiziInterrogazioneRegindeExt/ServiziInterrogazioneInterni
e l’operazione, servizio applicativo a cui fare accesso, è ‘ricercaSoggettoComplete’.

è stata modificata in

L’endpoint di interesse è identificato dalla seguente url:
http://reginde.processotelematicotest.giustizia.it	(ambiente di pre-esercizio)
http://reginde.processotelematico.giustizia.it	(ambiente di esercizio)
e l’operazione, servizio applicativo a cui fare accesso, è ‘ricercaSoggettoComplete’.

Paragrafo 6.2.5.2 pag. 73 devono essere inseriti gli interventi necessari per l’eventuale funzionamento con il protocollo TLS 1.0
Risposta: Al momento il sistema è configurato per il funzionamento in TLS1.0, infatti nel file “standalone-full.xml” presente nel percorso “/home/SIES/jboss-eap-6.4.Alpha/standalone/configuration” nel paragrafo dedicato alle proprietà di sistema

<property name="jdk.tls.client.protocols" value="SSLv2Hello,SSLv3,TLSv1"/>

è impostato il parametro “TLSv1”, che abilita i protocolli TLSv1, TLSv1.1 e TLSv1.2, quindi non vi è alcun intervento da eseguire.

Paragrafo 6.2.7 pag. 73 va integrato secondo quanto indicato al punto b), indicando anche cosa fare in previsione del passaggio ad https.
Risposta: L’attuale frase:
Per la connessione ai servizi in https sul sistema ReGIndE è da prevedere l’importazione della chiave pubblica (certificato ssl) che mappa il DNS del server su cui è esposto il servizio
ES:  https://reginde/ServiziInterrogazioneRegindeExt/ServiziInterrogazioneInterni
Il certificato deve essere importato nel file keystore del sies (trustore.jks) posizionato al /var/SIES/CONFIG/certs.

sarà modificata in:

Per la connessione ai servizi in https sul sistema ReGIndE è da prevedere l’importazione della chiave pubblica (certificato ssl) che mappa il DNS del server su cui è esposto il servizio
ES:
https://reginde.processotelematicotest.giustizia.it (ambiente di pre-esercizio)
http://reginde.processotelematico.giustizia.it        (ambiente di esercizio)

Il certificato deve essere importato nel file keystore del sies (trustore.jks) posizionato al /var/SIES/CONFIG/certs.

Per una connessione basata su protocollo https:
posizionarsi sotto la cartella: “/var/SIES/CONFIG/certs”;
aggiornare il file trustStore “sies.jks”, importando, con procedura nota all’Amministrazione, la catena di certificati ed il certificato necessari al colloquio con la macchina server che espone il servizio web.
NB: i certificati da importare devono essere resi disponibili dai referenti del sistema REGINDE e correlati all’ambiente predisposto per la verifica di conformità.

Paragrafo 6.3.3 pag. 74 lo stile grafico delle interfacce non sembra essere identico a quello dell’attuale SIES.
Risposta: Aggiornato stile grafico del messaggio da Web nella Fig. 46

Paragrafo 6.6.2 pag. 89: si fa riferimento ad una consegna del gruppo Tabelle Fisse di DGSIA. E’ opportuno indicare la data della consegna.
Risposta: Al par. 6.6 pag.88 riga 23 alla frase “con i dati presenti nelle tabelle fisse COMUNE, PROVINCIA, REGIONE e STATO-NAZIONE fornite dalla DGSIA” è stata aggiunta la seguente frase “(tramite e-mail di Anna.Maffucci@giustizia.it a Vito.Bufi@eng.it del 6/11/2020 09:06),”
Paragrafo 6.6.2.2 pag. 91: la prima frase “dovranno essere adottati anche nella tabella REGIONE della DGSIA.” sembra introdurre un obbligo che non può essere mandatorio per il gruppo Tabelle Fisse di DGSIA. Che succede se il gruppo tabelle fisse non cambia il suo file?
Risposta: Sull’argomento era già stato concordato l’allineamento della tabella DGSIA a quella di SIES (e-mail di Maurizio Gatti ai componenti Tabelle Fisse e cc ENG del 6/4/2021 10:31 con ringraziamenti per la segnalazione).
Pertanto nel par. 6.6.2.2 alla pag. 92 riga 40, la precedente frase “Dopo attenta verifica si è stabiliti che le denominazioni dei seguenti records della CG_REF_CODES” è stata modificata in “Dopo attenta verifica si è stabilito, previa approvazione del gruppo Tabelle Fisse (vedi e-mail di Maurizio Gatti ai componenti Tabelle Fisse e cc ENG del 6/4/2021 10:31), che le denominazioni dei seguenti records della CG_REF_CODES”

In generale se dovessero intervenire variazioni future ci si adeguerà a quanto invierà la DGSIA.
Paragrafo 6.6.2.2 paragrafo Pag. 91, frase “Considerando il numero limitato di records da modificare l’allineamento su SIES sarà effettuato manualmente.” - Specificare cosa significa manualmente (tramite strumenti tipo Toads o tramite script)
Risposta: al par. 6.6.2.2 pag. 93 riga 16 alla su riportata frase è stata aggiunta la seguente “, tramite tool di gestione DB (es. TOAD) o eseguendo lo script  Insert_REGIONE.sql.”.
Paragrafo 6.6.2.3 pagina 92: sulla frase “A seguito dell’aggiornamento del dominio NAZIONE della CG_REF_CODES bisognerà aggiornare anche la tabella CODICI_SIES_NSC, utilizzata nel modulo di interoperabilità SIES-NSC, per i records con CO_DOMAIN = ‘NAZIONE’, modificando il valore della colonne CO_SIES_DES per quelli per cui vi sarà una modifica della Denominazione e l’inserimento di nuovi record per quelle NAZIONI aggiunti nella tabella CG_REF_CODES, dopo verifica dell’esistenza degli stessi nella equivalente tabella di NSC (DC_TAB_STATO_ESTERO). Eventuali Nazioni aggiunte nella CG_REF_CODES ed assenti in NSC, saranno segnalate agli amministratori di quel Sistema per le opportune verifiche.”, si suppone che la verifica sia stata fatta dal fornitore, visti gli accordi verbali. Se non fatta, occorre chiarirlo bene, per coinvolgere il Casellario.
Risposta: al par. 6.6.2.3 pag. 94 riga 31 alla frase “dopo verifica dell’esistenza degli stessi nella equivalente tabella di NSC (DC_TAB_STATO_ESTERO)” è stata aggiunta la seguente
“, effettuata dal fornitore.”.
Nel capitolo 6.6., viene detto più volte “In caso di aggiornamento della tabella fissa xxxxxxx, il Gruppo tabelle fisse della DGSIA dovrà trasmettere le modifiche anche a SIES.” Faccio presente che fa parte integrante di questo progetto la fornitura delle opportune procedure per il futuro aggiornamento.
Risposta: A pag. 92 riga 30, pag. 93 riga 19 e pag. 94 riga 42 alla su riportata frase è stata  aggiunta la frase “,come di norma già avviene.”.

Il documento di specifiche non è autoconsistente, in quanto, al suo interno, sono richiamati i documenti di seguito elencati che vanno rivisti nel loro complesso:
SIUT-SIES-MG-1.0-20210730 - Istruzioni_Bonifica_Difensori_021_RegInde_SIES.pdf
SIUT-SIES-MG-1.0-20210730 - Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_SIES.pdf
Risposta: Poiché i due documenti MG, contengono le istruzioni dettagliate e le descrizioni del contenuto delle procedure plsql, si è preferito di estrapolarle dal documento di SI, dove invece sono descritte le specifiche da realizzare. Le istruzioni in essi riportate possono essere eseguite dal gruppo di verifica/collaudo dell’Amministrazione per verificare la correttezza delle attività realizzate dal fornitore, ma non saranno eseguite passo passo nei singoli Distretti.
Per quanto riguarda il contenuto dei documenti, nella call svoltasi il 30-8-2021, si era stabilito che, successivamente all’approvazione del documento di SI 2.3, si sarebbero fissate delle call specifiche per analizzare il contenuto di ciascun documento e capire le eventuali modifiche da apportare agli stessi.

Di seguito, alcune osservazioni non esaustive:
Nel documento n°1, sembrerebbe che il ripristino, in caso di fallimento, sia previsto solo per le tabelle avvocato, in senso lato. Se qualcosa nelle bonifiche non dovesse andare a buon fine, per cui non fosse possibile installare tutta la MEV, il sistema nel suo complesso deve essere ripristinato nello stato precedente. Pertanto, dovrà essere previsto un ripristino di tutte le tabelle coinvolte nel processo di bonifica. E’ opportuno altresì indicare se sia necessario effettuare dei backup puntuali (oltre all’intero backup dell’intera base dati preliminarmente all’inizio delle attività) come ad esempio della tabella “CG_REF_CODES”.
Risposta: tra le procedures plsql contenute nel pacchetto bonifica_db è già presente XBA_RESTORE_TABELLE_AVVOCATI.prc che permette la restore di tutte le tabelle interessate dall’attività di bonifica (AVVOCATO, AVVOCATO_FASCICOLO_SIEP, AVVOCATO_FASCICOLO_SIUS, AVVOCATO_FASCICOLO_SIGE, PARTI_UDIENZA_DIFENSORE, STORICO_AVVOCATO, AVVISI_AVVOCATO,  NUOVA_ISTANZA), ma non prevedeva la restore della CG_REF_CODES. Si è provveduto a realizzare lo script Restore_CGREFCODES_pre_Bonifica.sql, che consente di restorare i 2 domini (FORO_AVVOCATI, NON_ATTIVITA) allo stato pre bonifica. Sarà aggiornato anche il documento di MG.
Sul documento n°1, indicare/valutare se durante le operazioni “bonifica avvocati” ci fossero delle fasi intermedie per controllare l’effetto di quanto appena eseguito. In caso di risposta affermativa la procedura di bonifica dovrà essere redatta in modo tale da permettere il controllo puntuale.
Risposta: saranno introdotte nel documento di MG delle queries sql, a valle dell’esecuzione delle procedure XBA_CARICA_AVV_CON_PENDENZE.prc, XBA_BONIFICA_AVV_CON_PENDENZE.prc e XBA_BONIFICA_AVVOCATO.prc, che permettano di eseguire delle verifiche a campione della correttezza delle stesse.

Nell’attuale documento non è ben chiara la logica del punto 10 a pag. 12 Paragrafo “3.2 Procedura Bonifica Difensori SIES”, dove sarebbe utile mettere un punto di verifica.
Risposta: vale quanto riportato nella risposta al punto precedente.

In entrambi i documenti occorre eliminare i riferimenti ai file di tipo “xlsx”: le tabelle da importare devono essere già pronte; deve essere indicata la fonte da cui si è partiti (file inviato da… il ….).
Risposta: Nei documenti sono state descritte le modalità di importazione dei files originari forniti dall’Amministrazione, nel caso che si volesse ripetere le operazioni. Eliminandole non vi sarebbe alcuna altra traccia dell’attività. Comunque se l’Amministrazione ritiene opportuno tale eliminazione, provvederemo. Nell’attività di aggiornamento dei documenti, provvederemo ad indicare le fonti da cui si è partiti.

In entrambi documenti è necessario, separare le istruzioni relative al “SIES distrettuale” da quelle per “SIUS Avvocati”. Sono sistemi diversi e pertanto devono esserci consegne separate, anche se gli aggiornamenti dovranno essere eseguiti in modo contestuale.
Risposta: Si provvederà a realizzare un documento di rilascio specifico per SIUS Avvocati, eliminando tutti i riferimenti dall’attuale documento di rilascio.

E’ auspicabile che si proceda per gradi, ovvero:
eseguire la bonifica delle Tabelle Fisse con un rilascio
Effettuare la bonifica degli avvocati
Realizzare l’aggancio al Reginde..
Risposta: Purtroppo non è possibile procedere a rilasci separati, poiché l’attività di adeguamento del software ha interessato moduli condivisi sia dalla gestione della nuova struttura delle Tabelle Comune, CG_REF_CODES, Codici_Sies_NSC, a seguito dell’allineamento a tabelle Fisse, sia dalla nuova gestione dell’Avvocato, a seguito dell’interazione con ReGIndE.