---
uniqueName: adeguamento-della-funzione-concessione-ratifica-af
displayName: "Adeguamento della Funzione Concessione Ratifica aff prova"
category: "GENERAL"
tags: []
---

# Adeguamento della Funzione Concessione-Ratifica aff.prova

> **File originale:** `MEV/SCHEDA_009/Adeguamento della Funzione Concessione-Ratifica aff.prova.docx`  
> **Tipo:** DOCX

---

#### Adeguamento della Funzione ‘Decisioni Sorveglianza’ – SIEP
Il menù ‘Decisioni Sorveglianza’ è oggetto di molteplici interventi. Infatti, al fine di allineare il sistema all’introduzione dell’art. art. 678 comma 1-ter c.p.p., è necessario intervenire in diversi sottomenù presenti nella sezione ‘Misure Alternative’ e nella sezione delle ‘Sospensioni’.
Gli interventi specificati si intendono da applicare nell’ambito degli uffici PM (Procura Ordinaria maggiorenni) e PMM (Procura Ordinaria minorenni).
Nell’immagine che segue ne sono evidenziati i punti:

Figura 58: Sezione misure alternative/sospensioni
Un primo intervento di cui è fatta richiesta è la modifica della Label del tasto funzione di ‘Concessione’ in “Concessione/Ratifica”. Questo intervento va applicato ad ogni tipologia di misura evidenziata nella precedente figura [Figura 58: Sezione misure alternative/sospensioni].
A seguire, invece, si espongono gli interventi da espletare per ogni singola misura alternativa.
4.4.2.2.1	Adeguamento della Funzione Affidamento in Prova al Servizio Sociale
Per il menù ‘Affidamento in Prova al Servizio Sociale’, in corrispondenza del tasto funzione di ‘Concessione/Ratifica' della misura, occorre intervenire affinché la pagina attuale gestisca anche i provvedimenti del Tribunale di Sorveglianza che ‘concedono’ oppure che ‘ratificano’ la misura alternativa ‘Affidamento in prova al servizio sociale (art. 47 O.P. -  art. 678 comma 1-ter c.p.p.)’.

I provvedimenti che devono essere gestiti, in aggiunta a quelli attualmente previsti in questa sezione, hanno le seguenti peculiarità:
Fa riferimento ad un procedimento SIUS con contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ per gli uffici TDS, oppure con contenuto ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 2 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.) ’ per gli uffici TDSM.
Sono caratterizzati dall’esito “Concede” (0001) oppure dall’esito “Conferma Decisione del Magistrato Relatore” (COD_ESITO = 0271).
Nell’attuale form bisognerà prevedere nuovi campi per l’annotazione degli estremi dell’ordinanza di applicazione provvisoria, che però dovranno essere visibili solo in caso di selezione di una ordinanza di Ratifica.
Sono quelle con cod_motivo = 0720, 0721 e cod_esito = 0271 per il TDS, cod_motivo = 0730, 0731, 0732 e cod_esito = 0271 per il TDSM. Quando inseriamo quest’ordinanza, dobbiamo impostare l'eve_id_evento con l'id dell'ordinanza di applicazione provvisoria.
Quelli nella parte superiore sono i dati dell'ordinanza di conferma, i successivi sono gli estremi dell'ordinanza di applicazione provvisoria, confermata.
Nella form, se il soggetto è già in Affidamento Provvisorio, sulla maschera è riportata la data inizio misura:

Nel nostro caso dovrebbe diventare “Data Applicazione Provvisoria” e permetterci di inserire un'annotazione, piuttosto che un provvedimento o una Richiesta sottoposizione agli obblighi (secondo quanto detto nell'ultima call).

Figura 59: Funzione di 'Concessione/Ratifica art.678 Affidamento in Prova' – (PM e PMM)
La sezione “anno numero ordinanza provvisoria” si deve auto compilare, in caso di assenza non deve essere bloccante, caricamento manuale. Nel caso di concessione non deve essere presente.
Nello specifico, per gli uffici PM (Procura Ordinaria maggiorenni), in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare, oltre alle ordinanze di Concessione Misure Alternative, anche le ordinanze con esito ‘Conferma Decisione del Magistrato Relatore’ e che afferiscono al nuovo contenuto ‘Concessione misure alternative (art. 678 comma 1-ter c.p.p.) ’ ed il cui oggetto sia uno dei seguenti:
Affidamento in Prova al Servizio Sociale (Art. 47 O.P. -  Art. 678 comma 1-ter c.p.p.) (0680)
Affidamento in Prova al Servizio Sociale (Art. 94 DPR 309/90 - Art. 678 comma 1-ter c.p.p.) (0681)
Conferma appl. provv. Affidamento in Prova al S.S. (Art. 47 O.P. -  Art. 678 comma 1-ter c.p.p.) (0720)
Conferma appl. provv. Affidamento in Prova al S.S. (Art. 94 DPR 309/90 - Art. 678 comma 1-ter c.p.p.) (0721)
Invece, per gli uffici PMM (Procura Ordinaria minorenni), in corrispondenza del link ‘Seleziona provvedimento di Sorveglianza dalla lista  ‘ 	, il sistema deve permettere di visualizzare e caricare le ordinanze/decreti con esito ‘Concede’ oppure con esito ‘Conferma Decisione del Magistrato Relatore’ e che afferiscono al nuovo contenuto ‘Concessione misure penali di comunità/misure alternative alla detenzione (art. 2 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.)’ ed il cui oggetto sia uno dei seguenti:
Affidamento in prova al servizio Sociale  (art.4 D.lgs. 121/2018, art. 678 comma 1 ter c.p.p.) (0690)
Affidamento in prova in casi particolari  (artt.4 D.lgs. 121/2018 -  94 DPR 309/90, art. 678 comma 1 ter c.p.p.) (0691)
Affidamento in prova in prova con detenzione domiciliare (art.5 d.lgs. 121/2018, art. 678 comma 1 ter c.p.p.)  (0692)
Conferma appl. provv. Affidamento in Prova al S.S. (art.4 D.lgs. 121/2018, art. 678 comma 1 ter cp.p.) (0730)
Conferma appl. provv. Affidamento in Prova in casi particolari (artt.4 D.lgs. 121/2018 -  94 DPR 309/90, art. 678 comma 1 ter cp.p.) (0731)
Conferma appl. provv. Affidamento in prova in prova con detenzione domiciliare (art.5 d.lgs. 121/2018, art. 678 comma 1 ter cp.p.)  (0732)
Per le ordinanze con esito ‘Conferma Decisione del Magistrato Relatore’ nella pagina di pop-up che si apre dal link su menzionato, occorre prevedere anche la visualizzazione dell’anno e numero dell’ordinanza provvisoria recepito dalla Sorveglianza.
Per quanto riguarda invece il campo ‘Oggetto Provvedimento’, nella combo box corrispondente devono essere previsti i corrispondenti oggetti introdotti su Sorveglianza in associazione ai contenuti su specificati.
Pertanto la combo box Oggetto Provvedimento presenterà i seguenti valori:
in caso di Procura:

(COD_MOTIVO = 0001,0002,0003,0680,0681,0720,0721)
in caso di Procura Minori:

(COD_MOTIVO = 0001,0002,0003,0690,0691,0692,0730,0731,0732)
Inoltre, la pagina va integrata anche con i campi anno e numero dell’ordinanza provvisoria a cui la ‘ratifica’ si riferisce. Tali informazioni devono essere recepite dal provvedimento della sorveglianza selezionato in pop-up.
Al ‘conferma’ dell’inserimento il sistema inserirà:
In caso di concessione delle nuove misure, quindi in caso di ordinanza con rito ordinario, in maniera simile alle misure già gestite, il sistema inserirà le seguenti richieste (26)
| Cod_Motivo Misura | Cod_Motivo Richiesta | Tipo Richiesta |
| --- | --- | --- |
| 0680 | 5443 | Verbale sottoscrizione obblighi - Affidamento in Prova al Servizio Sociale (Art. 47 O.P. -  Art. 678 comma 1-ter c.p.p.) |
| 0681 | 5444 | Verbale sottoscrizione obblighi - Affidamento in Prova al Servizio Sociale (Art. 94 DPR 309/90 - Art. 678 comma 1-ter c.p.p.) |
| 0690 | 5445 | Verbale sottoscrizione obblighi - Affidamento in Prova al Servizio Sociale (art.4 D.lgs. 121/2018, art. 678 comma 1 ter cp.p.) |
| 0691 | 5446 | Verbale sottoscrizione obblighi - Affidamento in Prova in casi particolari  (artt.4 D.lgs. 121/2018 -  94 DPR 309/90, art. 678 comma 1 ter cp.p.) |
| 0692 | 5447 | Verbale sottoscrizione obblighi - Affidamento in prova in prova con detenzione domiciliare (art.5 d.lgs. 121/2018, art. 678 comma 1 ter cp.p.) |

In caso di Ratifica delle nuove uno dei seguenti provvedimenti (04):
| Cod_Motivo Misura | Cod_Motivo Richiesta | Tipo Richiesta |
| --- | --- | --- |
| 0720 | 5460 | Ratifica Appl. Provv. Affidamento in Prova al Servizio Sociale (Art. 47 O.P. -  Art. 678 comma 1-ter c.p.p.) |
| 0721 | 5461 | Ratifica Appl. Provv. Affidamento in Prova al Servizio Sociale (Art. 94 DPR 309/90 - Art. 678 comma 1-ter c.p.p.) |
| 0730 | 5462 | Ratifica Appl. Provv. Affidamento in Prova al Servizio Sociale (art.4 D.lgs. 121/2018, art. 678 comma 1 ter cp.p.) |
| 0731 | 5463 | Ratifica Appl. Provv. Affidamento in Prova in casi particolari  (artt.4 D.lgs. 121/2018 -  94 DPR 309/90, art. 678 comma 1 ter cp.p.) |
| 0732 | 5464 | Ratifica Appl. Provv. Affidamento in prova in prova con detenzione domiciliare (art.5 d.lgs. 121/2018, art. 678 comma 1 ter cp.p.) |

e presenterà la pagina di dettaglio con tutti i dati del provvedimento, in particolare la ‘nuova’ descrizione dell’oggetto dell’ordinanza selezionata e gli estremi (anno/numero) dell’ordinanza provvisoria.
Penso che potremmo appoggiare i dati nelle colonne DATA_DECISIONE_MA_AT, ANNO_REGISTRO_MA_AT, NUMERO_REGISTRO_MA_AT, che vengono utilizzate in caso di Cod_natura_decisione = ED e EC, nel nostro  caso sarebbe CO. L'Id dell'ordinanza credo che non occorra, visto che è iscritto tutto da SIEP. In alternativa per anno e numero ci sarebbe anche le colonne ANNO_REGISTRO_CONC_PROVV e NUMERO_REGISTRO_CONC_PROVV, che su siesrm e siessvil non risultano mai valorizzate.
Dalla pagina di dettaglio deve essere possibile ‘stampare’, ‘validare’ o ‘modificare’ il provvedimento di concessione/ratifica all’Affidamento, oltre a poter tornare Indietro, tasto  .
La pagina di emissione della concessione dell’affidamento al servizio sociale, attualmente prevede l’inserimento manuale del provvedimento e tale comportamento non deve essere precluso, pertanto tutti i campi della sezione ‘Dati Tribunale della Sorveglianza ‘ devono essere editabili.
La nuova descrizione deve essere prevista anche in fase di stampa ed in virtù di ciò, è necessario modificare i template preesistenti o introdurre un nuovo template di stampa da associare alla ‘ratifica’ dell’ammissione provvisoria per l’Affidamento al servizio sociale.
A seguito della validazione del provvedimento di Concessione/Ratifica dell’Affidamento in Prova, deve essere allineata anche la descrizione sull’elenco provvedimenti del PM:

Figura 60: Elenco provvedimenti PM
Inoltre, a valle della validazione del provvedimento occorre prevedere un aggiornamento dello stato del procedimento e della posizione giuridica con ‘nuove’ descrizioni, concordate con l’Amministrazione.

Figura 61: Aggiornamento dello Stato del Procedimento e Posizione Giuridica
MOMENTANEAMENTE UTILIZZIAMO GLI STATI PROCEDIMENTO E LE POSIZIONI GIURIDICHE PREVISTE PER LE MISURE ATTUALI.
Al momento per i cod_motivo 0001, 0002, 0003 sono gestiti i seguenti template:
| SIEP_MA_AFFI_ARRD.rtf | Concessione affidamento in prova art.94 - da arr.dom. | 01 | 03 | 0001 | 4 |
| --- | --- | --- | --- | --- | --- |
| SIEP_MA_AFFI_ARRD_SCARC.rtf | Concessione affidamento in prova art.94 - arr.dom.già scarc. | 01 | 03 | 0001 | 8 |
| SIEP_MA_AFFI_DETD.rtf | Concessione affidamento in prova art.94 - da det.dom. | 01 | 03 | 0001 | 3 |
| SIEP_MA_AFFI_DETD_SCARC.rtf | Concessione affidamento in prova art.94 - det.dom.già scarc. | 01 | 03 | 0001 | 7 |
| SIEP_MA_AFFI_DET_SCARC.rtf | Concessione affidamento in prova art.94 - det.già scarc. | 01 | 03 | 0001 | 6 |
| SIEP_MA_AFFI_DS.rtf | Concessione affidamento in prova art.94 - libero | 01 | 03 | 0001 | 0 |
| SIEP_MA_AFFI_ESECDOM.rtf | Concessione affidamento in prova art.94 - Da ESECDOM. | 01 | 03 | 0001 | B |
| SIEP_MA_AFFI_ESECDOM_SCARC.rtf | Concessione affidamento in prova art.94 - Da ESECDOM .già scarc. | 01 | 03 | 0001 | C |
| SIEP_MA_AFFI_OS.rtf | Concessione affidamento in prova art.94 - det | 01 | 03 | 0001 | 2 |
| SIEP_MA_AFFI_PASSAGGIO.rtf | Affidamento Servizio Sociale ex art. 94 DPR 309/90 | 01 | 03 | 0001 | A |
| SIEP_MA_AFFI_SEML.rtf | Concessione affidamento in prova art.94 - da semil. | 01 | 03 | 0001 | 5 |
| SIEP_MA_AFFI_SEML_SCARC.rtf | Concessione affidamento in prova art.94 - semil.già scarc. | 01 | 03 | 0001 | 9 |
| SIEP_MA_AFFI_SOTTO.rtf | affidamento 94 - richiesta verbale obblighi | 01 | 03 | 0001 | 1 |

Gestione Template
| COD_MOTIVO = 0001,0002,0003 | COD_MOTIVO = 0001,0002,0003 | COD_MOTIVO = 0001,0002,0003 | COD_MOTIVO = 0001,0002,0003 |
| --- | --- | --- | --- |
| Flag_Scarcerato | Posizioni_Giuridiche | FLAG_TEMPLATE |  |
|  | (13 e IEveAFP != null e ‘’), 54 | A | Espiazione Pena in Regime di Affidamento in Prova, Ammissione/Applicazione Affidamento in prova Provvisorio |
|  | aPosPrec != null && aPosPrec.getCodPosizioneGiuridica() != null && aPosPrec.isLibero()
&& aMisMod.getDataInizioMisura() != null && aPosizioneGiu.equals("13") | 0 |  |
|  | 7,10,16,17,20,26,30,46,47 | 1 |  |
| PROC | 03 | 2 |  |
| PROC | 04,82,83,84,85,86,87 | 4 |  |
| PROC | 50,53 | B |  |
| PROC | 12,29 | 3 |  |
| PROC | 14 | 5 |  |
| SORV | 03 | 6 |  |
| SORV | 50,53 | C |  |
| SORV | 12,29 | 7 |  |
| SORV | 04,82,83,84,85,86,87 | 8 |  |
| SORV | 14 | 9 |  |