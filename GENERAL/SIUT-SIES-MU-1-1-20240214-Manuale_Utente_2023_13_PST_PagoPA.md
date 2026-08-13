---
uniqueName: siut-sies-mu-1-1-20240214-manualeutente202313pstpa
displayName: "SIUT SIES MU 1 1 20240214 Manuale Utente 2023 13 PST PagoPA"
category: "GENERAL"
tags: []
---

# SIUT-SIES-MU-1.1-20240214-Manuale_Utente_2023_13_PST_PagoPA

> **File originale:** `MEV/SCHEDA_033/SIUT-SIES-MU-1.1-20240214-Manuale_Utente_2023_13_PST_PagoPA.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Vito Bufi - Umberto Mignogna |  |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 14/02/2024 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 27/03/2023 | Prima Emissione |  |
| 1.1 | 14/02/2024 | Seconda Emissione | Aggiornato par. 2.2 
Aggiunto par. 2.4
Aggiornato cap. 3 – Tutto
Aggiunti cap. 4 e 5 |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Aurora Garofalo | Amministrazione |  | Responsabile Unico Procedimento |
| Dott. Oris Orlando | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Francesco Rosati | RTI |  | Responsabile Manutenzione Correttiva
Referente Qualità e Sicurezza |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario e Referente Tecnico |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Referente PMO e Qualità |
| Alessandro Falleni | RTI |  | Referente Sicurezza |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |


Indice dei contenuti
1	Introduzione	6
1.1	Scopo del documento	6
1.2	Riferimenti	6
1.3	Glossario	6
1.3.1	Acronimi e abbreviazioni	6
2	Iscrizione Procedimento	8
2.1	Iscrizione Pena Complessiva	8
2.2	Modalità Pagamento Pena Pecuniaria	10
2.3	Civilmente Obbligato per la Pena Pecuniaria	16
2.4	Dettaglio Procedimento SIEP	19
3	Gestione Riscossione Pene Pecuniarie	22
3.1	Ordine di ingiunzione / Altri Provvedimenti	22
3.1.1	Ordine di ingiunzione Pagamento	23
3.1.2	Nota trasmissione bollettini rate successive alla prima	29
3.1.3	Rideterminazione della pena pecuniaria	30
3.1.4	Avviso Mancato Pagamento	32
3.1.5	Provvedimento Avvenuto Pagamento	34
3.1.6	Trasmissione Atti per la Conversione	36
3.1.7	Definizione Procedimento Pena Pecuniaria	37
3.2	Gestione Notifiche	38
3.2.1	Notifiche	38
3.2.2	Rinnovo Ricerche per Omesse Notifiche	42
3.2.3	Richiesta Informazioni Comma 5	45
3.2.4	Rinnovazione Notifica successiva alla Richiesta Informazioni	46
3.2.5	Solleciti	47
3.3	Gestione Bollettini PagoPA	48
3.3.1	Richiesta Bollettini	49
3.3.2	Verifica Stato Pagamenti	54
3.3.3	Verifica Stato Bollettino su pagoPA	55
3.4	Scadenzari	56
3.4.1	Scadenzario Stato Pagamenti	57
3.5	Ricerca procedimenti per Stato Pagamenti	58
3.6	Gestione Pene Sostitutive Brevi	61
3.6.1	Semilibertà/Detenzione Domiciliare Sostitutive	61
3.7	Gestione errori con pagoPA	68
3.7.1	Informazione per gli uffici	68
3.7.2	Cruscotto per funzionalità web	69
4	Interventi sottosistema SIGE	72
4.1	Aggiornamento template Fissazione Udienza	72
4.2	Integrazione Tabelle Oggetti	72
5	Interventi sottosistema SIUS	74
5.1	Adeguamenti SIUS per gestione Conversione nuove pene sostitutive	74
5.2	Adeguamenti SIUS per gestione Applicazione pene sostitutive	74

Introduzione
Scopo del documento
Nel documento in oggetto si delineano gli interventi effettuati sul sistema SIES in merito al pagamento delle pene pecuniarie anche attraverso l’interfacciamento del PagoPA/PST mediante l’invocazione dei seguenti servizi:
Servizio per la generazione del Bollettino (quando viene creato un bollettino viene in automatico generato uno stato ad esso associato, identificativo IUV);
Servizio per avere aggiornamenti sullo stato del bollettino.
Sono descritti gli interventi effettuati sostanzialmente sul sistema SIEP e alcuni interventi minimali sui sottosistemi SIGE e SIUS nell’abito delle Scheda Intervento 2023_13 e Scheda Intervento 2023_33_Step1.
Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF 1 | m_dg.DOG07AR.14_02_2023.0000226.U_Richiesta_scheda_2023-13_APP-SIES_PAGOPA_v_1.0_signed | Richiesta Scheda |
| RIF 2 | Invio_atti_cognizione_scheda_2023-13_PAGOPA_v_1.0_signedPagoPA_2023-13__cognizione | Atti Cognizione |
| RIF 3 | Documentazione_servizi_web_v1.53 | Servizi esposti dal PST |
| RIF 4 | APPLICATIVI - Flussi pagamento telematico tramite PST vers. 3.1 | Servizi esposti dal PST |
| RIF5 | SIUT-SCCL-SC-1.2-20230327-Scheda_Intervento_2023_13_PST_PagoPA.docx | Scheda Interventi |
| RIF6 | SIUT-SIES-SC-1.3-20231123-Scheda_Intervento_2023_33_PST_PagoPA_Step-1.docx | Scheda Interventi |

Glossario
Acronimi e abbreviazioni
| Sigla | Descrizione |
| --- | --- |
| API | Application Programming Interface |
| CPU | Central Processing Unit |
| CV | Curriculum Vitae |
| DB | Data Base |
| DEC | Direttore Esecutivo Contratto |
| DGSIA | Direzione Generale per i Sistemi Informativi Automatizzati |
| DR | Disaster Recovery |
| ETSI | European Telecommunications Standards Institute |
| FP | Function Point |
| GdL | Gruppo di Lavoro |
| GDPR | General Data Protection Regulation |
| ICT | Information & Communication Technology |
| ISO | International Organization for Standardization |
| ISP | Information Security Policy |
| IT | Information Technology |
| MAC | MAnutenzione Correttiva |
| MEV | Manutenzione EVolutiva |
| PA | Pubblica Amministrazione |
| PdQ | Piano della Qualità |
| PdS | Piano della Sicurezza |
| PEC | Posta Elettronica Certificata |
| PMO | Program Management Office |
| POO | Program Operating Office |
| RTI | Raggruppamento Temporaneo di Impresa |
| RTO | Recovery Time Objective |
| RUF | Responsabile Unico Fornitore |
| RUP | Responsabile Unico Progetto |
| SAL | Stato Avanzamento Lavori |
| SGQ | Sistema di Gestione per la Qualità di Engineering Ingegneria Informatica S.p.A. |
| SGSI | Sistema di Gestione della Sicurezza Informatica |
| SIU | Sistema Informativo Unitario |
| SLA | Service Level Agreement |
| SM | Security Manager |
| SQL | Structured Query Language |
| SW | SoftWare |
| UTA | Utente Generico Amministrazione |
| VPN | Virtual Private Network |

Iscrizione Procedimento
Iscrizione Pena Complessiva
Nella form di Iscrizione Pene Complessiva è stata aggiunta una nuova sezione per l’acquisizione dei dati relativi alle Pene Sostitutive delle Pene Detentive Brevi


in cui è possibile gestire le seguenti tipologie di pena



La valorizzazione della sezione Sanzione Sostituiva è alternativa alla valorizzazione della sezione Pene Sostitutive delle Pene Detentive Brevi. La nuova sezione sarà riportata anche nelle form di Dettaglio, quando valorizzata, e Modifica.

A seguito della Conferma il sistema inserirà i dati nella base dati e invierà la form di Dettaglio


in cui, nella  combo box delle azioni, sono state aggiunte due nuove voci “Modalità Pagamento Pena Pecuniaria”, “Civilmente Obbligato per la Pena Pecuniaria”



Da questa form è inoltre possibile:

selezionare l’azione di Modifica, ricevendo la form



da cui è possibile procedere alla modifica dei dati

Selezionare l’azione di cancellazione, ricevendo la form


da cui è possibile procedere alla cancellazione dei dati.
Modalità Pagamento Pena Pecuniaria
Nella precedente gestione non vi era la storicizzazione della modalità di pagamento, né dei bollettini generati. L’importo da pagare e le modalità di pagamento, unica soluzione o rateizzazione, erano collegati alla pena complessiva, in quanto rappresentavano i dati presenti nella sentenza di condanna. In caso di errata indicazione dell’importo e/o delle modalità di pagamento, l’utente doveva svalidare il procedimento e modificare i dati, senza che ne rimanesse alcuna traccia nella base dati.
Considerando la vita procedurale di un procedimento di gestione della pena pecuniaria, questa impostazione è stata rivista, in base alle seguenti ipotesi operative.
Fermo restando la possibilità di selezionare la funzione dal Dettaglio della Pena Complessiva



è stato deciso di permettere la gestione delle Modalità di Pagamento, anche da fascicolo validato, a tal fine è stata inserita nella tool-bar delle funzionalità attivabili dal Dettaglio procedimento una nuova voce “Gestione Modalità Pagamento”

La funzione gestisce la seguente casistica:
Procedimento privo di Modalità di pagamento
viene presentata la form di Inserimento della Modalità di pagamento



Il campo Importo da pagare deve essere compilato dall’utente, visto che non necessariamente corrisponde alla somma dei valori presenti in sentenza di multa, ammenda e pena pecuniaria sostitutiva.
Il n.ro di giorni entro cui effettuare il pagamento dell’unico bollettino o del primo, in caso di rateizzazione, a partire dalla data di notifica del provvedimento non è più impostabile dall’utente, ma, come previsto dalla norma, è precompilato rispettivamente in 90 e 30.

Procedimento con modalità pagamento inserita e privo di Ordine di ingiunzione al pagamento
viene presentata la form di Dettaglio della Modalità pagamento

da cui è possibile procedere alla modifica o alla cancellazione

Procedimento con Ordine di ingiunzione al pagamento emesso e validato e poi annullato, in quanto errato
viene presentata la form di Dettaglio della Modalità pagamento



che permette solo l’inserimento di una nuova modalità di pagamento, essendo quella già presente oggetto di un provvedimento, anche se annullato.
Si ricorda che l’Importo da pagare riportato nella form è quello calcolato dal sistema sommando la multa, l’ammenda e la pena pecuniaria sostitutiva, è comunque un dato modificabile dall’utente.
In caso di annullamento di un Ordine di ingiunzione, il sistema storicizza i dati della modalità pagamento e i bollettini generati, l’annullamento dovrà essere possibile solo se non risulta già pagato alcun bollettino.
Al momento dell’emissione di un nuovo ordine di ingiunzione, il sistema accorgendosi che non esiste alcuna modalità di pagamento non collegata a un evento valido o non collegata ad alcun evento, invierà il seguente messaggio

L’utente, cliccando su OK riceverà la form di Gestione Modalità Pagamento, da cui potrà procedere all’Inserimento della nuova Modalità Pagamento e successivamente quella di Inserimento dell’Ordine di Ingiunzione al Pagamento, i dati della modalità pagamento e i relativi bollettini faranno riferimento a questo Evento.
A seguito del nuovo inserimento, il sistema presenterà la seguente form di Dettaglio

Da cui sarà possibile procedere alla modifica o alla cancellazione dell’ultima modalità inserita, purché non ancora collegata ad alcun provvedimento
In caso di presenza di più modalità di pagamento già collegate a provvedimenti, si riceverà la seguente form

che permette solo l’inserimento di una nuova modalità di pagamento, essendo quelle già presenti oggetto di provvedimenti.




Le due modalità di pagamento (unica soluzione o pagamento rateale) sono ovviamente alternative. In caso di pagamento rateizzato la form inibisce la sezione relativa al pagamento Unica Soluzione e abilita quella per il Pagamento Rateizzato



L’importo da pagare è uguale alla somma degli importi (riportati nella prima parte della form, per la Pena Pecuniaria e per la Pena Pecuniaria sostitutiva) inseriti in fase di iscrizione sentenza: è comunque modificabile.

Gli importi complessivi indicati in Pagamento Unica Soluzione o Pagamento Rateizzato dovrebbero di norma essere uguali a quanto indicato in Importo da Pagare, ma nel caso che differissero, in fase di Conferma il sistema invia il seguente messaggio:



Che consente di continuare con l’inserimento o annullare l’operazione e correggere i dati in maschera.
Il Numero giorni scadenza è obbligatorio, in caso di non valorizzazione del campo, il sistema invia il seguente messaggio bloccante:




A seguito della conferma il sistema aggiornerà la base dati e presenterà la form di Dettaglio



Da cui sarà possibile procedere alla Modifica o alla Cancellazione dei dati.

Selezionando l’azione di modifica  si riceverà la form


dopo aver aggiornato i dati di interesse, a seguito della Conferma, il sistema aggiornerà la base dati e ripresenterà la form di Dettaglio.

Selezionando l’azione di cancellazione   si riceverà il seguente messaggio per la conferma a procedere alla cancellazione



Cliccando su OK, il sistema aggiornerà la base dati e tornerà sul Dettaglio della Pena Complessiva.
Civilmente Obbligato per la Pena Pecuniaria
La funzione consente di gestire la Persona Fisica/Giuridica civilmente obbligata al pagamento della pena pecuniaria, in caso di mancato pagamento da parte del Condannato, come indicato dal giudice della cognizione in sentenza o successivamente alla decisione della Sorveglianza o del GE. Per tale motivo la funzione sarà abilitata solo su procedimento in stato di iscritto.
Selezionando questa voce dal Dettaglio della Pena Complessiva:



il sistema controlla se nella base dati risulta già inserita tale informazione, in caso di esistenza presenterà la form di Dettaglio, in caso di assenza presenterà la form di inserimento, impostata di default su persona fisica



In cui nella combo box Qualifica saranno presenti le seguenti voci



Selezionando una delle voci differenti da ‘-‘, la form si modifica presentando i campi per l’inserimento di una seconda persona Civilmente Obbligata:



L’inserimento della seconda persona Civilmente obbligata assume la stessa Qualifica della prima persona.
L’inserimento della seconda persona Civilmente obbligata non è obbligatoria.
In caso di selezione del radio button su persona giuridica  la form si modificherà in:



In cui nella combo box della qualifica sono riportate sempre le stesse voci, viste in precedenza, ma in questo caso non sarà presentata una seconda sezione per l’inserimento di una seconda parte Civilmente Obbligata. E’ consentito l’inserimento di una unica persona giuridica civilmente obbligata.

A seguito della conferma il sistema presenterà la seguente form di Dettaglio



Da cui è possibile procedere alla Modifica o alla Cancellazione dei dati oppure richiamare la funzione di Gestione del Difensore della persona Civilmente Obbligata. Il link Gestione Difensore è solo CLICCABILE, nel qual caso il sistema invierà il seguente messaggio



Selezionando l’azione di modifica  si riceve la form



dopo aver aggiornato i dati di interesse, a seguito della Conferma, il sistema aggiornerà la base dati e ripresenterà la form di Dettaglio.

Selezionando l’azione di cancellazione   si riceve il seguente messaggio per la conferma a procedere alla cancellazione



Cliccando su OK, il sistema aggiornerà la base dati e tornerà sul Dettaglio della Pena Complessiva.
Dettaglio Procedimento SIEP
Per facilitare la consultazione dei dati relativi alle modalità di pagamento delle pene pecuniarie e delle persone Civilmente Obbligati al pagamento, nonché lo Stato dei Pagamenti, nella form di Dettaglio del procedimento SIEP sono stati inseriti i seguenti link ,,  che saranno presentati solo in presenza dei relativi dati.

dalla form,  cliccando su   sarà visualizzata la form

Cliccando su  sarà visualizzata la form di Dettaglio Modalità Pagamento Pena Pecuniaria sostitutiva

cliccando su , sarà visualizzata la form verifica stato pagamento bollettini su pagoPA

Da cui sarà possibile accedere alla form di Verifica Stato Pagamento Bollettini su PagoPA relativi al provvedimento selezionato


Gestione Riscossione Pene Pecuniarie
Per la gestione di tutti gli aspetti connessi alla riscossione delle Pene Pecuniarie e delle Pene Sostitutive si è intervenuti nell’attuale  menu delle funzioni che il sistema presenta selezionando la voce Gestione Altre Sanzioni



aggiungendo tre nuove voci, di seguito racchiuse nel riquadro in rosso



Selezionando la voce Riscossione Pene Pecuniarie, il sistema presenta il seguente sottomenu:


Ordine di ingiunzione / Altri Provvedimenti
Selezionando questa voce dal menu, si riceve un ulteriore sottomenu con le voci di tutti i provvedimenti al momento previsti per la gestione delle pene pecuniarie


Ordine di ingiunzione Pagamento
La funzione consente di inserire l’Ordine di ingiunzione al pagamento della pena pecuniaria al Condannato, al Civilmente obbligato e ai rispettivi Difensori, verificando che risultino obbligatoriamente già inseriti i dati delle modalità di pagamento.

In caso di assenza dei suddetti dati, il sistema invia il seguente messaggio

da cui cliccando su OK si riceverà la form per l’inserimento della Modalità di pagamento (vedi par. 2.2).

In caso di presenza dei dati si riceverà la seguente form


La form presenta i dati di dettaglio delle modalità di pagamento e del Civilmente Obbligato, se presente, e le autorità destinatarie delegate alla notifica dell’atto al Condannato, al Difensore ed al Civilmente Obbligato.

A seguito della completa compilazione dei campi della form e della relativa Conferma, il sistema inserisce un Ordine Esecuzione di Ingiunzione al pagamento nella base dati e presenta la form di Dettaglio.


Da questa form è possibile procedere:

Alla Modifica dell’ordine


alla stampa dell’Ordine di Ingiunzione al Pagamento, in unica soluzione o rateizzato e successivamente procedere alla validazione del provvedimento, a seguito della quale il sistema presenta la form di Dettaglio


con due tasti che permettono di richiamare le funzioni di Visualizzazione Notifiche e Richiesta generazione Bollettini.
Quando dal Dettaglio dell’Ordine di esecuzione di ingiunzione al pagamento si richiede la stampa del documento, il sistema in base alla categoria di appartenenza della posizione giuridica del condannato (MISURA ALTERNATIVA è assimilata a LIBERO) ed alla modalità di pagamento (unica soluzione o rateizzato) richiama uno dei seguenti template:
SIEP_PP_OI_PAGAMENTO_UN.RTF		condannato Libero e pagamento unica soluzione
SIEP_PP_OI_PAGAMENTO_UN_DET.RTF	condannato Detenuto e pagamento unica soluzione
SIEP_PP_OI_PAGAMENTO_RR.RTF		condannato Libero e pagamento rateizzato
SIEP_PP_OI_PAGAMENTO_RR_DET.RTF	condannato Detenuto e pagamento rateizzato
Poiché le posizioni giuridiche presenti nel sistema sono numerosissime, si è provveduto a riaggregarle in tre maxi categorie: Libero, Misura  Alternativa e Detenuto, come riportato nella seguente tabella:
| Codice | Descrizione | Categoria aggregata |
| --- | --- | --- |
| 01 | Custodia Cautelare per Questa Causa in Regime di Detenzione | DETENUTO |
| 02 | Custodia Cautelare per Questa Causa in Regime di Arresti Domiciliari | MISURA ALTERNATIVA |
| 03 | Espiazione Pena in Regime Carcerario | DETENUTO |
| 04 | Arresti Domiciliari ex art.656 comma 10 cpp | MISURA ALTERNATIVA |
| 05 | Latitante | LIBERO |
| 06 | Internato | DETENUTO |
| 07 | Libero | LIBERO |
| 08 | Latitante | LIBERO |
| 09 | Internato | DETENUTO |
| 10 | Libero | LIBERO |
| 11 | Espiazione Pena in Regime di Liberazione Condizionale | MISURA ALTERNATIVA |
| 12 | Espiazione Pena in Regime di Detenzione Domiciliare | MISURA ALTERNATIVA |
| 13 | Espiazione Pena in Regime di Affidamento in Prova | MISURA ALTERNATIVA |
| 14 | Espiazione Pena in Regime di Semiliberta' | DETENUTO |
| 15 | Espiazione Pena Sostitutiva (Liberta' Controllata) | MISURA ALTERNATIVA |
| 16 | Libero in Differimento Pena | LIBERO |
| 17 | Libero in Differimento Pena (Provvisorio) | LIBERO |
| 18 | Espiazione Pena Sostitutiva (Lavoro Sostitutivo) | MISURA ALTERNATIVA |
| 19 | Espiazione Pena Sostitutiva (Semidetenzione) | DETENUTO |
| 20 | Evaso | LIBERO |
| 21 | Misura di Sicurezza Liberta' Vigilata | LIBERO |
| 22 | Custodia Cautelare in Regime di Detenzione | DETENUTO |
| 23 | Custodia Cautelare in Regime di Arresti Domiciliari | MISURA ALTERNATIVA |
| 24 | Espiazione Pena Definitiva in Carcere | DETENUTO |
| 25 | Espiazione Pena in Regime di Det. Domiciliare Speciale | MISURA ALTERNATIVA |
| 26 | Espulso | LIBERO |
| 27 | Sospensione Pena ex L. 207/03 | MISURA ALTERNATIVA |
| 28 | Collaboratore Giustizia | MISURA ALTERNATIVA |
| 29 | Detenzione Domiciliare Provvisoria | MISURA ALTERNATIVA |
| 30 | Estradato | DETENUTO |
| 31 | Sospensione Cautelativa 51 Ter (di Det. Domiciliare) | DETENUTO |
| 32 | Sospensione Cautelativa 51 Ter (di Aff. in Prova) | DETENUTO |
| 33 | Sospensione Cautelativa 51 Ter (di Semiliberta') | DETENUTO |
| 34 | Sospensione Cautelativa 51 Ter (di Det. Domiciliare Speciale) | DETENUTO |
| 35 | Sospensione Cautelativa 51 Ter (di Sospensione Pena Ex L. 207/03) | DETENUTO |
| 36 | Sospensione Provvisoria 51 Bis (di Det. Domiciliare) | DETENUTO |
| 37 | Sospensione Provvisoria 51 Bis (di Aff. in Prova) | DETENUTO |
| 38 | Sospensione Provvisoria 51 Bis (di Semiliberta') | DETENUTO |
| 39 | Sospensione Provvisoria 51 Bis (di Det. Domiciliare Speciale) | DETENUTO |
| 40 | Sospensione Provvisoria 51 Bis (di Sospensione Pena Ex L. 207/03) | DETENUTO |
| 41 | Espiazione Pena in Regime di Det.Domiciliare in Prosec.Provv. 51 Bis | MISURA ALTERNATIVA |
| 42 | Espiazione Pena in Regime di Aff. in Prova in Prosec.Provv. 51 Bis | MISURA ALTERNATIVA |
| 43 | Espiazione Pena in Regime di Semiliberta' in Prosec.Provv. 51 Bis | MISURA ALTERNATIVA |
| 44 | Espiazione Pena in Regime di Det. Dom.Speciale in Est. Provv. 51 Bis | MISURA ALTERNATIVA |
| 45 | Sospensione Pena Ex L. 207/03 in Estensione Provvisoria 51 Bis | MISURA ALTERNATIVA |
| 46 | Libero in Sospensione | LIBERO |
| 47 | Libero in Sospensione DPR 309/90 | LIBERO |
| 48 | Deceduto | LIBERO |
| 49 | Sospensione provvisoria Arresti Domiciliari | DETENUTO |
| 50 | Esecuzione presso domicilio della pena detentiva | MISURA ALTERNATIVA |
| 51 | Sospensione cautelativa 51 ter (Esecuzione presso domicilio della pena detentiva) | DETENUTO |
| 52 | Sospensione cautelativa 51 bis (Esecuzione presso domicilio della pena detentiva) | MISURA ALTERNATIVA |
| 53 | Arresti domiciliari - Esecuzione presso domicilio della pena detentiva | MISURA ALTERNATIVA |
| 54 | Affidamento in Prova Provvisorio | MISURA ALTERNATIVA |
| 55 | Custodia cautelare per questa causa in misura di sicurezza provvisoria | DETENUTO |
| 62 | Sospensione provvisoria 51 ter   Arresti Domiciliari ex art. 656 comma 10 | DETENUTO |
| 63 | Sospensione provvisoria 51 ter Domiciliari ex art 89 dpr 309/90 | DETENUTO |
| 64 | Sospensione provvisoria 51 ter Permanenza in Casa | DETENUTO |
| 65 | Sospensione provvisoria 51 ter Collocamento in Comunita' | DETENUTO |
| 67 | Arresti Domiciliari ex art 89 dpr 309/90 | MISURA ALTERNATIVA |
| 68 | Ripristino Permanenza in Casa ex art. 656 comma 10 | MISURA ALTERNATIVA |
| 69 | Ripristino Collocamento in comunita' ex art. 656 comma 10 | MISURA ALTERNATIVA |
| 70 | Custodia Cautelare per Questa Causa in Regime di Arresti Domiciliare ex art 89 dpr 309/90 | MISURA ALTERNATIVA |
| 71 | Custodia Cautelare per Questa Causa in Regime di Permanenza in Casa | MISURA ALTERNATIVA |
| 72 | Custodia Cautelare per Questa Causa in Collocamento in Comunita' | MISURA ALTERNATIVA |
| 73 | Custodia Cautelare per Questa Causa in Misura di Sicurezza Applicata in via Provvisoria | DETENUTO |
| 74 | Espiazione pena per Altra Causa in Regime di Detenzione | DETENUTO |
| 75 | Espiazione pena per Altra Causa in Misura Sicurezza Detentiva (Internato) | DETENUTO |
| 76 | Custodia Cautelare per Altra Causa in Regime di Detenzione | DETENUTO |
| 77 | Espiazione pena per Altra Causa in Misura di Sicurezza Applicata in Via Provvisoria | DETENUTO |
| 78 | Custodia Cautelare per Altra Causa - Regime di Arresti Domiciliari | MISURA ALTERNATIVA |
| 79 | Custodia Cautelare per Altra Causa - Regime Permanenza in Casa | MISURA ALTERNATIVA |
| 80 | Custodia Cautelare per Altra Causa - Collocamento in comunita' | MISURA ALTERNATIVA |
| 81 | Custodia Cautelare per Altra Causa - Regime di Arresti Domiciliari ex art 89 dpr 309/90 | MISURA ALTERNATIVA |
| 84 | Arresti Domiciliare ex art 89 dpr 309/90 - ex art. 656 comma 10 cpp | MISURA ALTERNATIVA |
| 85 | Permanenza in Casa | MISURA ALTERNATIVA |
| 86 | Collocamento in comunita' - Esecuzione presso domicilio della pena detentiva | MISURA ALTERNATIVA |
| 87 | Arresti domiciliare ex art. 89 dpr 309/90 - Esecuzione presso domicilio della pena detentiva | MISURA ALTERNATIVA |
| 88 | Espiazione misura sicurezza non detentiva | MISURA ALTERNATIVA |
| 89 | Libero in Differimento misura di sicurezza | LIBERO |
| 90 | Libero in Differimento misura di sicurezza (Provvisoria) | LIBERO |
| E | Sospensione Cautelativa 51 Ter (di Semiliberta') | DETENUTO |


A seguito della validazione del provvedimento, lo stato procedimento sarà impostato a Emesso Ordine esecuzione di Ingiunzione al Pagamento della Pena Pecuniaria.

Il nuovo provvedimento sarà riportato nell’Elenco Provvedimenti del PM, rispettandone tutte le regole previste per gli altri provvedimenti di SIEP:

Nota trasmissione bollettini rate successive alla prima
Per consentire la trasmissione dei Bollettini di pagamento delle rate successive alla prima (vedi par. 2.6) con le date di scadenza, calcolate dal sistema successivamente all’annotazione della notifica dell’ordine di ingiunzione, bisogna prevedere l’emissione di un Avviso di pagamento che accompagni l’invio degli Avvisi di pagamento cartacei, generati da pagoPA.
La funzione controlla che siano stati generati da pagoPA i bollettini relativi alle rate successive alla prima, in caso di mancata generazione invierà il messaggio bloccante

in caso di avvenuta generazione, il sistema invierà la seguente form

A seguito della Conferma, la funzione inserirà in base dati una Comunicazione Nota trasmissione bollettini rate successive alla prima e presenterà la form di Dettaglio

da cui è possibile selezionare le azioni di Stampa, Validazione, Modifica. Sarà possibile procedere alla Cancellazione dall’Elenco Provvedimenti del PM.
Selezionando l’azione di stampa il sistema produrrà l’avviso che accompagnerà i bollettini pagoPA delle rate successive alla prima (template SIEP_PP_NT_TRASM_BOLL.rtf), che saranno inviati al condannato.
Rideterminazione della pena pecuniaria
A seguito di provvedimento da parte del Giudice dell’esecuzione o a seguito provvedimento di cumulo, l’ufficio esecuzione può avere esigenza di emettere un nuovo OI, riferito a nuovo importo da pagare e con nuove modalità.
Selezionando la funzione , il sistema verificherà se è presente una modalità di pagamento non oggetto di precedenti provvedimenti, in caso di esito negativo invierà a video il seguente messaggio

da cui, cliccando su OK, presenterà la form di Inserimento Modalità Pagamento, che permetterà di inserire nella base dati i nuovi dati, come indicato nel precedente paragrafo. Nella successiva form di Dettaglio, il sistema, verificato che la nuova modalità di pagamento non è collegato ad alcun provvedimento, presenterà due tasti per poter selezionare l’Ordine di ingiunzione o la Rideterminazione Pena

Selezionando  il sistema invierà la form per l’inserimento degli ulteriori dati del provvedimento e ingloberà i dati della modalità di pagamento

in cui sarà possibile annotare gli estremi del provvedimento del Giudice dell’Esecuzione o del provvedimento di cumulo, la data emissione e trasmissione, le autorità destinatarie per la notifica alle parti.
A seguito della conferma il sistema inserirà il nuovo provvedimento e le nuove modalità di pagamento in base dati e presenterà la form di dettaglio

da cui è possibile procedere alla modifica, alla stampa, alla validazione. Sarà possibile procedere alla Cancellazione dall’Elenco Provvedimenti del PM.
Per questo nuovo provvedimento è possibile procedere alla generazione dei bollettini e alla loro gestione, oltre l’utilizzo delle funzioni incluse nel menu Gestione Notifiche.
Selezionando l’azione di stampa il sistema produrrà il provvedimento (template SIEP_PP_PR_RIDET_PP.rtf), che sarà inviato al condannato.
N.B. In caso di presenza di Modalità di pagamento non collegata ad Evento il sistema presenterà direttamente la form di Rideterminazione della Pena Pecuniaria.
A seguito della validazione del provvedimento nella form di Dettaglio saranno riportati i tasti
da cui sarà possibile attivare le relative funzionalità.
Avviso Mancato Pagamento
In caso di procedimento con pagamento rateizzato il mancato pagamento di una o parte delle rate comporta la decadenza del beneficio della rateizzazione, in tal caso l’ufficio deve emettere un provvedimento di Avviso di mancato pagamento che prevede il pagamento del restante importo in un’unica soluzione entro 60 giorni dalla notifica.
Selezionando la funzione , il sistema verificherà preventivamente che siamo in presenza di pagamento rateizzato della pena pecuniaria e che vi siano rate non pagate, al verificarsi di queste condizioni il sistema presenterà la form di Verifica Stato Bollettini

Da cui selezionando il tasto , il Sistema presenterà la form

in cui riporta l’importo da pagare e la modalità di pagamento in un’unica soluzione. A seguito della conferma il sistema inserirà in base dati il nuovo provvedimento, la relativa modalità di pagamento e presenterà la form di Dettaglio

da cui è possibile procedere alla modifica, alla stampa, alla validazione. Sarà possibile procedere alla Cancellazione dall’Elenco Provvedimenti del PM.
Per questo nuovo provvedimento è possibile procedere alla generazione del bollettino e alla loro gestione, oltre l’utilizzo delle funzioni incluse nel menu Gestione Notifiche.
Selezionando l’azione di stampa il sistema produrrà il provvedimento (template SIEP_PP_PR_AVV_MAN_PAG.rtf), che sarà inviato al condannato.
A seguito della validazione del provvedimento nella form di Dettaglio saranno riportati i tasti
da cui è possibile attivare le relative funzionalità.
Provvedimento Avvenuto Pagamento
In caso di procedimento con avvenuto pagamento dell’intero importo, l’ufficio deve emettere un provvedimento di Estinzione della Pena Pecuniaria .
Selezionando la funzione , il sistema verificherà preventivamente che per il procedimento in esame l’importo dell’importo da pagare e il totale dei bollettini pagati corrispondano, in caso di non corrispondenza sarà inviato apposito messaggio bloccante all’utente

in caso di corrispondenza il sistema invierà la seguente form

in cui l’utente valorizzerà le date di emissione e trasmissione, il magistrato e le autorità delegate alla notifica. A seguito della conferma il sistema inserirà in base dati il nuovo provvedimento e presenterà la form di Dettaglio

da cui è possibile procedere alla modifica, alla stampa, alla validazione. Sarà possibile procedere alla Cancellazione dall’Elenco Provvedimenti del PM.
Selezionando l’azione di stampa il sistema produrrà il provvedimento (template SIEP_PP_PR_AVVPAGAM_PP.rtf), che sarà inviato alle autorità delegate alla notifica. Il documento prodotto include anche il foglio complementare per il Casellario Giudiziale.

Trasmissione Atti per la Conversione
In caso di mancato pagamento della pena pecuniaria in unica soluzione il pubblico ministero trasmette gli atti al magistrato di Sorveglianza perché decida in merito alla Conversione della pena.
Selezionando la funzione , il sistema presenterà la seguente form, simile a quella già presente in SIEP per la conversione delle pene pecuniarie (classe 7)

in cui riporterà l’importo non pagato. A seguito della conferma il sistema inserirà in base dati il nuovo evento, presenterà la form di Dettaglio

da cui è possibile procedere alla modifica, alla stampa, alla validazione. Sarà possibile procedere alla Cancellazione dall’Elenco Provvedimenti del PM.
Selezionando l’azione di stampa il sistema produrrà il provvedimento (template SIEP_PP_TRASM_RICH_CONVERSIONE.rtf), che sarà inviato alle autorità delegate alla notifica.
Sarà possibile effettuare la Verifica esito trasmissioni atti per Competenza e Riscontro trasmissione - annotazione della presa in carico.

Definizione Procedimento Pena Pecuniaria
Per l’archiviazione del procedimento con solo pena pecuniaria, successivamente all’emissione del provvedimento di avvenuto pagamento della Pena Pecuniaria, l’utente potrà procedere selezionando la funzione , che presenterà la seguente form

Dopo aver compilato i campi obbligatori della form, a seguito della conferma, il sistema inserirà in base dati il nuovo evento di archiviazione e presenterà la form di Dettaglio:

da cui è possibile procedere alla modifica, alla stampa, alla validazione. Sarà possibile procedere alla Cancellazione dall’Elenco Provvedimenti del PM.
Selezionando l’azione di stampa il sistema produrrà il provvedimento di archiviazione (template SIEP_ARC_FOGLIO_COMP_ESP.rtf). A seguito della validazione il sistema aggiorna lo stato del procedimento in ARCHIVIATO, pertanto si ribadisce che questa funzionalità va utilizzata solo in assenza di pena detentiva residua da espiare.
Gestione Notifiche
Nel menu Gestione Altre Sanzioni>>Riscossione Pene Pecuniarie la precedente voce “Gestione Ordine Ingiunzione” è stata rinominata in “Gestione Notifiche”, in quanto le funzioni, precedentemente previste solo per l’ordine di ingiunzione, possono essere utilizzate anche per annotare le date di avvenuta notifica del provvedimento di Rideterminazione Pena Pecuniaria e del Provvedimento di avviso mancato pagamento.

Tutte le voci presenti nel menu “Gestione Notifiche” sono attive.

A seguito dell’abilitazione delle sopra riportate funzioni ad altre tipologie di provvedimenti, oltre l’ordine di ingiunzione, ogni volta che se ne  selezionerà una il sistema presenterà l’elenco dei provvedimenti

da cui l’utente selezionerà quello di interesse.
Notifiche
La funzione permette di annotare le date di avvenuta notifica dell’ordine ingiunzione alle parti destinatarie man mano che pervengono all’ufficio. Al momento dell’annotazione della data di avvenuta notifica al condannato dell’unico bollettino o del primo bollettino, in caso di rateizzazione, il sistema provvederà a far scattare gli scadenzari , relativi al pagamento dei singoli bollettini.

La funzione è attivabile dal precedente menu o dal dettaglio dell’Ordine di esecuzione di Ingiunzione al Pagamento cliccando sul link . In caso di avvenuta valorizzazione di almeno una data notifica, il sistema presenterà la form di Dettaglio, in assenza di tutte le date di Notifica presenterà la form di Inserimento:


Per acquisire la data dell’avvenuta notifica l’utente dovrà valorizzare il campo Data Notifica per ciascuna della parti per cui risulta già effettuata la notifica, spuntando eventualmente la check box  per l’indicazione dell’autorità che ha effettuato la notifica, se diversa da quella indicata nell’Ordine di Ingiunzione. A seguito della Conferma, il sistema acquisirà i dati e invierà la form di Dettaglio.



Da cui selezionando l’icona di modifica si riceverà la precedente form di inserimento che permetterà di valorizzare le date mancanti e di modificare o cancellare le date già valorizzate, impostandole a spazio.

Al momento dell’annotazione della data di avvenuta notifica al condannato, il sistema procederà al calcolo della data scadenza per il pagamento del primo bollettino e dei restanti bollettini, in caso di rateizzazione , secondo i seguenti principi:
In caso di rata unica  la data di scadenza = data avvenuta notifica + 90 gg. In questo caso sarà calcolata anche la data scadenza per la richiesta di rateizzazione = data avvenuta notifica + 20 gg;
In caso di pagamento rateale la data scadenza prima rata = data avvenuta notifica + 30 gg, le date scadenza delle rate successive dovranno essere impostate sull’ultimo giorno dei mesi successivi alla data di scadenza prima rata (es. Rate da pagare 5, data notifica = 10-05-2023=> data scadenza prima rata 09-06-2023, date scadenze successive 31-07-2023, 31-08-2023, 30-09-2023, 31-10-2023).
Contestualmente al calcolo delle scadenze, il sistema inserirà il procedimento nello scadenzario, cancellando il record preesistente (es. se è il procedimento è già presente nello scadenzario a seguito dell’ordine di ingiunzione, al momento in cui si annoterà la data di avvenuta notifica al condannato di un nuovo provvedimento lo scadenzario farà riferimento alle date scadenze riferite a quest’ultimo).
Al fine di agevolare l’aggancio delle funzionalità successive all’emissione dei provvedimenti relativi al pagamento delle pene pecuniarie, sulle form di Dettaglio dell’Ordine di ingiunzione, del provvedimento di Rideterminazione Pena Pecuniaria e del Provvedimento di avviso mancato pagamento sono stati inseriti due tasti


per permettere di verificare le date di avvenuta notifica del provvedimento
per procedere alla richiesta di generazione dei Bollettini pagoPA

Sulla form di Dettaglio dello stato delle notifiche è presente il link

Rinnovo Ricerche per Omesse Notifiche
La funzione ricalca il funzionamento di quella attualmente disponibile  per l’ordine di esecuzione con decreto sospensione. Selezionandola dal menu presenta la seguente form:

Lasciando impostato il radio button su Omessa notifica Ufficiali giudiziari e compilando i restanti campi necessari, a seguito della conferma il sistema inserirà una richiesta di rinnovo ricerche per omessa notifica e presenterà la form di Dettaglio

da cui sarà possibile generare la stampa del Rinnovo ricerche SIEP_GDS_NOT_UFFG e la successiva  validazione o procedere alla cancellazione. Il Rinnovo viene riportato nella form iniziale

Se nella form si imposta il radio button su Omessa Notifica Forze di Polizia il sistema verifica che sul procedimento sia stato già inserito un verbale di vane ricerche. Nel caso che non sia già presente invia il seguente messaggio

Che consente di passare alla funzione di inserimento di Verbale Vane Ricerche

Che dopo l’inserimento presenta la form di Dettaglio

Da cui selezionando il pulsante  si ritornerà alla form di rinnovo

Lasciando impostato il radio button su Omessa notifica Forze di Polizia e compilando i restanti campi necessari, a seguito della conferma il sistema inserirà una richiesta di rinnovo ricerche per omessa notifica e presenterà la form di Dettaglio, da cui sarà possibile generare la stampa del Rinnovo ricerche SIEP_GDS_OE_RINN_RIC e la successiva  validazione o procedere alla cancellazione. Il Rinnovo viene riportato nella form iniziale

Richiesta Informazioni Comma 5
La form presenta due radio button che trasformano la stessa in base alla valorizzazione degli stessi

Oppure

a seguito della conferma il sistema inserisce un nuovo record nella tabella RINNOVO, collegato alla Notifica, aggiorna lo stato del procedimento e visualizza la funzione di Dettaglio:

da cui è possibile produrre la stampa della richiesta da inviare all’autorità destinataria.
Analogamente si comporterà il sistema in caso di richiesta informazioni ad altri. Le richieste inserite sono riportate nella form iniziale:

Rinnovazione Notifica successiva alla Richiesta Informazioni
La form presenta due radio button che trasformano la stessa in base all’impostazione degli stessi

a seguito della conferma il sistema inserisce un nuovo record nella tabella RINNOVO, collegato alla Notifica, aggiorna lo stato del procedimento e visualizza la funzione di Dettaglio:

da cui è possibile produrre la stampa della richiesta da inviare all’autorità destinataria.
Le richieste inserite sono riportate nella form iniziale:

Solleciti
La form presenta due radio button che non trasformano la form, ma hanno lo scopo di pilotare 2 template differenti

a seguito della conferma il sistema inserisce un nuovo record nella tabella RINNOVO, collegato alla Notifica, aggiorna lo stato del procedimento e visualizza la funzione di dettaglio:
da cui è possibile produrre la stampa del sollecito da inviare all’autorità destinataria oppure procedere alla cancellazione. Le richieste di sollecito inserite sono riportate nella form iniziale.
Gestione Bollettini PagoPA
Nella prima versione della gestione del pagamento delle pena pecuniarie tramite PST/pagoPA era stato necessario impostare la data di scadenza dei bollettini a una data futura fittizia (31/12/2049) per rispettare i seguenti requisiti:
- consentire al condannato di poter pagare il bollettino successivamente alla reale data di scadenza, in presenza del vincolo da parte di pagoPA che il pagamento avvenisse entro la data riportata sull’avviso di pagamento;
- consentire al condannato di poter pagare, anche successivamente alla data di scadenza reale, calcolata successivamente all’avvenuta notifica dell’OE , e fino all’emissione di un nuovo provvedimento che stabilisca nuove modalità di pagamento, come previsto dall’attuale normativa.
Successivamente al rilascio della suddetta versione, PST ha comunicato che, a seguito di aggiornamenti avvenuti su pagoPA, il pagamento del bollettino è consentito anche successivamente al superamento della data scadenza riportata sullo stesso e che è possibile generare il bollettino senza indicare alcuna data scadenza.
Decaduto il vincolo del pagamento entro la data di scadenza, permane il problema di come comunicare al condannato, in caso di pagamento rateizzato della pena pecuniaria, le reali date di scadenza di pagamento delle rate successive alla prima, riportate sul documento cartaceo Bollettino pagoPA, superando l’attuale impostazione di una data futura.
Il GdL Siep ha quindi deciso di poter operare in una delle due seguenti modalità:
modalità 1
successivamente all’emissione dell’ordine di Ingiunzione al pagamento si procede alla richiesta di generazione del bollettino relativo al pagamento in una unica soluzione o di tutti i bollettini, in caso di rateizzazione, non facendo impostare dal sistema alcuna data di scadenza. I criteri di calcolo della data scadenza saranno riportati nel provvedimento a cui saranno allegati. Tutti i bollettini saranno stampati, privi di data scadenza, ed inviati insieme all’Ordine di Ingiunzione per la notifica al condannato;
modalità 2
successivamente all’emissione dell’ordine di Ingiunzione al pagamento si procede alla richiesta di generazione del bollettino relativo al pagamento in una unica soluzione o al pagamento della prima rata, in caso di rateizzazione, non facendo impostare dal sistema alcuna data di scadenza.
successivamente all’annotazione di avvenuta notifica dell’ordine di ingiunzione, il sistema calcola la data di scadenza reale del primo pagamento e, in caso di rateizzazione, calcola le date scadenze delle rate successive impostandole sulle date di fine mese dei mesi successivi alla data di scadenza del primo bollettino. In caso di rateizzazione l’utente procede alla richiesta a PST/pagoPA di generazione dei bollettini successivi al primo, trasferendo le relative date scadenza reali, e, in caso di esito positivo da parte di pagoPA, procede alla stampa di tutti i bollettini, che riporteranno le date scadenza, e all’emissione dell’Avviso pagamento, descritto al precedente paragrafo.
Per effetto di quanto descritto in precedenza è stata rivista la precedente funzione “Richiesta Bollettini”, introducendo la possibilità da parte dell’utente, in base al modus operandi dell’ufficio, di poter richiedere la generazione dei bollettini, secondo le due modalità sopra descritte.
Richiesta Bollettini
Da questa funzione  è possibile richiedere la generazione dell’unico bollettino in caso di pagamento in un’unica soluzione, oppure, in caso di rateizzazione, di poter richiedere la generazione di tutti i bollettini oppure solo del primo oppure dei bollettini restanti, solo se già risulta generato il bollettino della prima rata.
A seguito degli ultimi aggiornamenti apportati a PST/pagoPA, che hanno eliminato l’obbligatorietà del codice fiscale del condannato, l’attuale messaggio bloccante in caso di assenza del suddetto dato è stato modificato in un messaggio di warning, che consente, previa autorizzazione da parte dell’utente di procedere alla generazione dei bollettini anche in assenza del codice fiscale

In caso di generazione dei bollettini rateizzati in due diversi momenti, prima rata e restanti rate, per trasmettere i bollettini delle restanti rate, l’ufficio dovrà generare una Nota trasmissione Bollettini rate successive alla prima (vedi par. 3.1.2).
La funzione, in base alle modalità di pagamento (unica soluzione o rateizzato) presenterà una delle seguenti form

oppure

selezionando l'icona Inoltra  il sistema acquisirà la data della richiesta e visualizzerà i dati del bollettino da trasmettere a PST per l'inoltro a pagoPA e presenterà una delle seguenti form
Pagamento in unica soluzione

Pagamento Rateizzato

In caso di rateizzazione il sistema presenterà tre opzioni per la generazione dei bollettini:
Alla prima richiesta è possibile generare tutti i bollettini o solo il bollettino relativo alla prima rata. In caso di selezione del radio button per la generazione dei Bollettini per rate successive alla prima, il sistema invierà il seguente messaggio bloccante


Alla seconda richiesta, nel caso che nella prima abbia richiesto la generazione solo del bollettino  della prima rata, può effettuare solo la richiesta di generazione dei restanti bollettini.

Sia in caso di unica soluzione, che in caso di rateizzazione, selezionando il tasto  il sistema inoltrerà la richiesta e rimarrà in attesa della ricezione del bollettino/dei bollettini, in attesa del quali a video apparirà l’immagine di elaborazione in corso

a conclusione della quale apparirà a video il seguente messaggio

Cliccando su OK, il sistema aggiornerà la base dati di SIES con i dati ricevuti e presenterà la form di richiesta

simile alla prima form, ma con Data Richiesta e Data Ricezione valorizzate e priva del tasto Inoltra, cliccando sull’icona Visualizza il sistema presenterà , in caso pagamento in unica soluzione, bollettino completo dello IUV e del documento pdf

da cui sarà possibile stampare il documento in formato pdf, selezionando l’icona di stampa.
In caso di pagamento rateizzato, se l’utente ha selezionato l’opzione tutti, riceverà l’elenco di tutti i bollettini completi di IUV e del documento.pdf, ma privi di data di scadenza.

da cui sarà possibile stampare i documenti in formato pdf, relativi a tutti i bollettini, selezionando l’icona di stampa , presente accanto all’intestazione della funzione, oppure stampando ogni singolo bollettino,  selezionando l’icona di stampa presente nella colonna Azioni ad esso relativa.
Nel caso che, in fase di generazione, l’utente avesse selezionato solo quello relativo alla prima rata, il sistema presenterà la seguente form

In quest’ultimo caso, per la stampa dei restanti bollettini, che deve avvenire dopo l’avvenuta annotazione della notifica del primo bollettino al condannato, l’utente seleziona nuovamente la funzione Richiesta bollettini, il sistema verifica che vi siano bollettini ancora da generare, per cui anche in presenza della data richiesta e della data ricezione, presenta il tasto Inoltra

Selezionandolo si riceverà la form, che presenterà l’elenco dei rimanenti bollettini da generare

Da cui selezionando il tasto  il sistema, controlla che sui  bollettini da generare sia valorizzata la data di scadenza, a seguito dell’annotazione nel sistema della data di avvenuta notifica. In caso di assenza invierà il seguente messaggio bloccante:

In caso di avvenuta annotazione nel sistema della data di avvenuta notifica al condannato dell’OE, inoltrerà la richiesta e rimarrà in attesa della ricezione dei bollettini, in attesa del quali a video apparirà l’immagine di elaborazione in corso

a conclusione della quale apparirà a video il seguente messaggio

Cliccando su OK, il sistema aggiornerà la base dati di SIES con i dati ricevuti e presenterà la form di richiesta

simile alla prima form, ma con Data Richiesta e Data Ricezione valorizzate e priva del tasto Inoltra, cliccando sull’icona Visualizza il sistema presenterà i bollettini completi dello IUV e del documento pdf

da cui sarà possibile stampare i documenti in formato pdf, relativi a tutti i bollettini, selezionando l’icona di stampa , presente accanto all’intestazione della funzione, oppure stampando ogni singolo bollettino,  selezionando l’icona di stampa presente nella colonna Azioni ad esso relativa.
Verifica Stato Pagamenti
A seguito delle modifiche apportate alla gestione Modalità di Pagamento, la form di Verifica Stato Pagamenti presenterà l’elenco dei provvedimenti che hanno comportato la generazione di Bollettini pagoPA per ciascun provvedimento, anche di quelli annullati

Per ciascun provvedimento, selezionando l’azione di Dettaglio, sarà mostrata la form con l’elenco di tutti i Bollettini ed il relativo stato di pagamento.
Nella form accanto agli estremi dell’ordine di ingiunzione al pagamento, è stata aggiunta anche la data di notifica dello stesso al condannato.

Lo stato del singolo pagamento sarà aggiornato automaticamente, differito di un giorno, da pagoPA man mano che l’utente provvederà al pagamento. In effetti, vi sarà lato SIES un’attività batch notturna che interrogherà PST per aggiornare lo stato dei pagamenti.
Verifica Stato Bollettino su pagoPA
La funzione permetterà di poter inoltrare e ricevere tramite PST una richiesta in tempo reale sulla stato di pagamento di uno o più bollettini, come risulta su pagoPA. La funzione ricercherà gli ordini di ingiunzione al pagamento con data richiesta e data ricezione valorizzate e presenterà la seguente form:

Da cui selezionando l’azione Visualizza, si riceverà la seguente


In cui l’utente potrà selezionare i bollettini di interesse, spuntando i relativi check box, e provvederà all’Inoltro. Il sistema acquisirà i dati della richiesta e la trasmetterà a PST per l'inoltro a pagoPA e , in attesa dei quali a video apparirà l’immagine di elaborazione in corso

a conclusione della quale apparirà a video il messaggio di avvenuta ricezione dello stato pagamento dei bollettini richiesti

Cliccando su OK, il sistema aggiornerà lo stato dei bollettini sulla base dati di SIES e ripresenterà la form con l’Elenco riportata in precedenza aggiornata:

Scadenzari
Questa voce del menu Riscossione Pene Pecuniarie consente di accedere alle diverse tipologie di scadenzari, previsti per la Gestione delle Pene Pecuniarie:

selezionandola il sistema presenta le ulteriori voci al momento realizzate.

Scadenzario Stato Pagamenti
Come detto al par. 2.3.1 questo scadenzario si attiva al momento in cui l’utente annota la data della notifica al condannato dell’ordine di ingiunzione al pagamento. Il sistema calcola la data di scadenza per il pagamento dell’avviso pagoPA, relativo all’unica soluzione o alla prima rata in caso di rateizzazione, e in quest’ultima caso provvede a calcolare anche le scadenze delle rate successive.
La funzione in esame presenterà la seguente form:

In cui è possibile richiedere una delle seguenti estrazioni dei pagamenti per i quali risulta notificato al condannato il relativo Ordine di esecuzione di Ingiunzione al pagamento:
Tutti            		mostrerà tutti gli avvisi di pagamento scaduti e in scadenza futura;
In scadenza		in questo caso bisognerà indicare la data termine ricerca, che il sistema
calcolerà in base al periodo digitato (anni, mesi e giorni) a partire dalla data di elaborazione; mostrerà tutti gli avvisi di  pagamento con data scadenza <= data termine, non pagati, a partire dalla data elaborazione;
In scadenza oggi	mostrerà tutti gli avvisi di pagamento con data scadenza = data
elaborazione
Scaduti			mostrerà tutti gli avvisi di pagamento, non pagati, con data scadenza <
data elaborazione
E’ possibile restringere le suddette ricerche a un solo procedimento, valorizzando l’anno e numero dello stesso.
Il sistema presenterà i risultati della ricerca in un elenco, impaginato, ordinato per data scadenza crescente:


Chiaramente in caso di rateizzazione lo stesso procedimento potrà essere riportato più volte per rate differenti.
In presenza di istanza di rateizzazione, finché non risulteranno pagate tutte le rate, il procedimento non va considerato come scaduto.
Selezionando l’icona , il sistema estrarrà i dati visualizzati nella diverse pagine della form in un file formato Excel.

Selezionando l’azione di Dettaglio per uno degli elementi della lista, il sistema presenterà la form di Verifica Stato Bollettini:


che in caso di pagamento rateizzato permette di avere lo stato di pagamento di tutti i bollettini.
Ricerca procedimenti per Stato Pagamenti
Al fine di permettere all’ufficio di avere un resoconto dei procedimenti rispetto allo stato dei pagamenti, in base al quale poter poi procedere con l’emissione di specifici provvedimenti è stata realizzata la seguente funzione:


che presenta la seguente form



in cui è possibile impostare  3 seguenti tipologie di procedimenti, restringendo opzionalmente la ricerca per intervallo di estremi Procedimenti o per intervallo Date iscrizioni:

Procedimenti con pene pecuniaria totalmente pagata, in questo caso il sistema ricercherà tutti i procedimenti con pagamento rateizzato o in unica soluzione della pena pecuniaria, non archiviati,  con data ultima scadenza pagamento <= data elaborazione, privi di un Provvedimento Estinzione Pena Pecuniaria, per i quali il totale degli importi pagati coincide con l’importo da pagare e ne presenterà l’elenco


Da cui selezionando l’azione di Dettaglio, si riceverà la form di Verifica Stato Pagamenti.

Procedimenti con pagamento rateizzato con rate non pagate, in questo caso il sistema ricercherà tutti i procedimenti con pagamento rateizzato, non archiviati e per i quali non risulti un Avviso Mancato Pagamento, per i quali la somma pagata non coincide con l’importo da pagare e ne presenterà l’elenco


Da cui selezionando l’azione di Dettaglio, si riceverà la form di Verifica Stato Pagamenti.

Procedimenti con pagamento in unica soluzione non pagata , in questo caso il sistema ricercherà tutti i procedimenti, non archiviati e per i quali non risulti un provvedimento di Trasmissione Atti per la Conversione validato, per i quali l’ importo pagato non  coincide con l’importo da pagare e ne presenterà l’elenco


da cui selezionando l’azione di Dettaglio, si riceverà la form di Verifica Stato Pagamenti.

Sarà possibile generare il contenuto degli Elenchi sopra riportati in formato .xls, selezionando l’icona , presente nella testata dell’Elenco.
Gestione Pene Sostitutive Brevi
Per l’esecuzione delle pene sostitutive brevi di tipo detentive bisognerà selezionare nel menu Gestione Altre Sanzioni la voce Esecuzione Pene Detentive Brevi:

che presenterà a sua volta il seguente menu

N.B. Al momento è attiva solo la prima voce della form.
Semilibertà/Detenzione Domiciliare Sostitutive
Dal menu Esecuzione Pene Sostitutive Brevi, selezionando  si riceverà l’ulteriore menu



in cui sono attive solo le prime due voci.

#### Trasmissione Atti per Esecuzione
La funzione permette di inserire la trasmissione degli atti relativi alla Pena Sostitutiva detentiva all’UDS di Sorveglianza perché provveda ad iscrivere ed esprimersi sull’applicabilità della stessa. Selezionando la voce Trasmissione Atti per Esecuzione il sistema, in base alla posizione giuridica del condannato presenta una delle seguenti form:

Libero, in cui sono comprese le seguenti posizioni giuridiche:
| 7 | Libero | L |
| --- | --- | --- |
| 10 | Libero | L |
| 16 | Libero in Differimento Pena | L |
| 17 | Libero in Differimento Pena (Provvisorio) | L |
| 46 | Libero in Sospensione | L |
| 47 | Libero in Sospensione DPR 309/90 | L |
| 89 | Libero in Differimento misura di sicurezza | L |
| 90 | Libero in Differimento misura di sicurezza (Provvisoria) | L |














arresti domiciliari per questa causa, in cui sono comprese le seguenti posizioni giuridiche:
| 2 | Custodia Cautelare per Questa Causa in Regime di Arresti Domiciliari | EA |
| --- | --- | --- |
| 23 | Custodia Cautelare in Regime di Arresti Domiciliari vecchia gestione | EA |
| 70 | Custodia Cautelare per Questa Causa in Regime di Arresti Domiciliare ex art 89 dpr 309/90 | EA |
| 71 | Custodia Cautelare per Questa Causa in Regime di Permanenza in Casa | EA |
| 72 | Custodia Cautelare per Questa Causa in Collocamento in Comunita' | EA |










Custodia Cautelare per Questa Causa in Regime di Detenzione, in cui sono comprese le seguenti posizioni giuridiche
| 1 | Custodia Cautelare per Questa Causa in Regime di Detenzione | EI |
| --- | --- | --- |
| 22 | Custodia Cautelare in Regime di Detenzione vecchia gestione | EI |
| 55 | Custodia cautelare per questa causa in misura di sicurezza provvisoria | EI |
| 73 | Custodia Cautelare per Questa Causa in Misura di Sicurezza Applicata in via Provvisoria | EI |




Custodia cautelare altra causa Regime di Arresti Domiciliari, in cui sono comprese le seguenti posizioni giuridiche
| 78 | Custodia Cautelare per Altra Causa - Regime di Arresti Domiciliari | EA |
| --- | --- | --- |
| 79 | Custodia Cautelare per Altra Causa - Regime Permanenza in Casa | EA |
| 80 | Custodia Cautelare per Altra Causa - Collocamento in comunita' | EA |
| 81 | Custodia Cautelare per Altra Causa - Regime di Arresti Domiciliari ex art 89 dpr 309/90 | EA |





Custodia cautelare altra causa in regime di detenzione, in cui sono comprese le seguenti posizioni giuridiche
| 75 | Espiazione pena per Altra Causa in Misura Sicurezza Detentiva (Internato) | EI |
| --- | --- | --- |
| 76 | Custodia Cautelare per Altra Causa in Regime di Detenzione | EI |
| 77 | Espiazione pena per Altra Causa in Misura di Sicurezza Applicata in Via Provvisoria | EI |




posizioni giuridiche differenti dalle precedenti




a seguito della Conferma, il sistema inserirà la trasmissione in base dati e presenterà la form di dettaglio:



da cui si potrà modificare la trasmissione o stampare il relativo documento, a seguito della quale, il sistema presenterà gli ulteriori campi



per la validazione  Conferma o per la validazione e contemporanea trasmissione alla Sorveglianza Conferma Trasmissione. A seguito della trasmissione il sistema invierà il messaggio



Per la stampa del provvedimento sono stati realizzati i seguenti template in base alle posizioni giuridiche riportate in precedenza: NOTA_TRASM_PENSOS.rtf per i casi 1 e 6, NOTA_TRASM_PENSOS2.rtf per il caso 2, NOTA_TRASM_PENSOS3.rtf per il caso 3, NOTA_TRASM_PENSOS4.rtf per il caso 4, NOTA_TRASM_PENSOS5.rtf per il caso 5.
#### Riscontro Trasmissione Atti per Esecuzione
La funzione permetterà di verificare lo stato degli atti trasmessi. Selezionando la voce Riscontro Trasmissione Atti per Esecuzione nel menu di cui al par. 2.7.1, il sistema invierà la seguente form


Che consentirà di estrarre gli atti trasmessi alla Sorveglianza e relativi all’esecuzione delle Pene Sostitutive, con la possibilità di impostare vari filtri.
Il sistema ricercherà gli atti trasmessi, soddisfacenti le condizioni impostate, e presenterà la form con l’elenco:



Per ciascun elemento della lista sarà possibile visualizzare il Dettaglio:


Oppure

Gestione errori con pagoPA
E’ stato realizzato un cruscotto per la gestione degli errori che possono verificarsi nell’interfacciamento con la piattaforma PST/PagoPA per le funzionalità web precedentemente descritte.
Informazione per gli uffici
Nella homepage dell’applicativo sarà presente, in caso di errore o malfunzionamento del batch notturno, una icona (Avviso Batch PagoPA) di attenzione (in alto a destra) che segnalerà l’errata esecuzione:

Cliccando sull’icona, il sistema prospetterà la seguente pagina:

Riceverà il messaggio sopra riportato, ma non potrà effettuare alcuna operazione per risolvere l’anomalia.
Cruscotto per funzionalità web
La funzionalità è utilizzabile da parte dell’utente che ha riscontrato l’errore e dagli utenti con profilo di amministratore di ufficio.
Ogni volta che da applicazione verrà invocato uno dei due web services PST/PagoPA, in caso di esito negativo, il sistema memorizzerà gli estremi del procedimento, del provvedimento, dell’utente, del tipo di operazione e del motivo dell’errore nella base dati.
Al momento le funzionalità che invocano i due web services PST/PagoPA sono: “Richiesta Bollettini …” (due voci) e “Verifica stato bollettino su PagoPA”.
La funzione potrà essere richiamata dall’utente, non amministratore di ufficio, dal menù:

Oppure selezionando l’icona    che sarà aggiunta nell’elenco delle funzioni veloci

attivata da uno di questi menù la funzione filtrerà solo le richieste inoltrate dall’utente connesso, per le quali non ci sia stata risposta da PST/PagoPA e presenterà la seguente form:

per ciascun elemento dell’Elenco, cliccando sull’icona di dettaglio, il sistema ripresenta la form della funzione su cui si è verificato l’errore, dando la possibilità di reinnescare l’operazione. Ad esempio, per il primo elemento del sopra riportato elenco:

In caso di esito positivo della richiesta l’elemento sarà cancellato dal cruscotto.
Per l’utente Amministratore di Ufficio si inserirà la nuova voce nel menù laterale verticale

Selezionandola si riceverà la seguente form:

In cui sarà possibile impostare dei filtri per data e per utente, ed a seguito dell’avvio della ricerca il sistema presenterà la seguente form:

Selezionando l’icona di Dettaglio nella colonna “Azioni”, il sistema visualizzerà la form della funzionalità in errore al fine di reinnescarla dal punto precedente al verificarsi dell’errore; ad esempio:

In caso di esito positivo della richiesta l’elemento sarà cancellato dal cruscotto.

Interventi sottosistema SIGE
Aggiornamento template Fissazione Udienza
Sono state aggiornate le descrizioni riportate in alcuni template del Decreto di fissazione udienza.

o Vecchia frase

AVVERTE
il condannato detenuto:
➢ in  luogo  posto  nella circoscrizione  del  Giudice  che  può  chiedere  la  traduzione all’udienza;
➢ in  luogo  posto fuori della circoscrizione del  Giudice, che, se ne farà  richiesta,  sarà sentito,
prima  del  giorno  dell’udienza  dal  Magistrato  di  Sorveglianza  del  luogo  di detenzione,  salvo
che  il  Giudice  dell’esecuzione,  non  ne  disponga  d’ufficio  la traduzione.
o Nuova frase prevista dall’art art. 666, comma 4 c.p.p.

AVVERTE
il condannato detenuto:
➢in luogo posto nella circoscrizione del Giudice che può chiedere la traduzione all’udienza_;
L'interessato che ne fa richiesta è sentito personalmente.  A tal fine si procede   mediante collegamento a distanza, quando una particolare disposizione di legge lo prevede o quando l’interessato vi consente.  Tuttavia, se è detenuto o internato in luogo posto fuori della circoscrizione del giudice e non consente all’audizione mediante   collegamento   a distanza, l'interessato è sentito prima del giorno dell’udienza dal magistrato di  sorveglianza  del  luogo, salvo  che  il  giudice ritenga di disporre la traduzione

I template  SIGE_DE_DECRFISSAZIONEUDIENZA.rtf e SIGE_DE_DECRFISSAZIONEUDIENZA_P1.rtf
Integrazione Tabelle Oggetti
Per effetto della nuova normativa sono stati aggiunti nella base dati i seguenti oggetti ed esiti per consentire l’iscrizione e la gestione dei nuovi procedimenti.
#### Art. 95 disposizioni transitorie in materia di pene sostitutive delle pene detentive
Si è proceduto all’inserimento dei seguenti elementi:
Contenuto:	applicazione pene sostitutive delle pene detentive brevi art. 95. D.lgs. 150/22

Oggetti:	Applicazione della pena in semilibertà sostitutiva;
Applicazione della pena in detenzione domiciliare sostitutiva;
Applicazione della pena il lavoro di pubblica utilità sostitutivo;
Applicazione della pena la pena pecuniaria sostitutiva.
Esiti:		applica la Pena sostitutiva breve
rigetta l’istanza;
dichiara il non luogo a provvedere;
dichiara il non doversi procedere;
dichiara l’inammissibilità;
dichiara la propria la propria incompetenza
Saranno aggiunti nella tabella CG_REF_CODES nuovi records per i domini ‘OGGETTO_PROCEDIMENTO', 'OGGETTO_SIGE', 'ESITO_PROVVEDIMENTO_SIGE', 'ESITO_TENORE_SIGE'.
#### Riduzione pena art. 442, comma 2-bis - D.lgs. 150/22
Si è proceduto all’inserimento dei seguenti elementi:
Contenuto:	riduzione della pena articolo 442, comma 2-bis

Oggetti:	riduzione della pena articolo 442, comma 2-bis

Esiti:		applica riduzione pena
rigetta l’istanza;
dichiara il non luogo a provvedere;
dichiara il non doversi procedere;
dichiara l’inammissibilità;
dichiara la propria la propria incompetenza
Saranno aggiunti nella tabella CG_REF_CODES nuovi records per i domini ‘OGGETTO_PROCEDIMENTO', 'OGGETTO_SIGE', 'ESITO_PROVVEDIMENTO_SIGE', 'ESITO_TENORE_SIGE'.
Interventi sottosistema SIUS
Adeguamenti SIUS per gestione Conversione nuove pene sostitutive
Per permettere la gestione della richiesta di conversione/rateizzazione delle pene pecuniarie sostitutive lato SIUS è stato concordato con il GdL SIUS, in anticipo di quanto proposto nella Scheda-35, ancora in fase di analisi, di aggiungere, per l’attuale contenuto Conversione / Rateizzazione Pena Pecuniaria (U070) e per gli attuali oggetti Conversione pena pecuniaria (2470) e Rateizzazione pena pecuniaria (2471), nuovi esiti e di eliminarne qualcuno superfluo, per cui gli esiti disponibili saranno i seguenti (evidenziati in giallo quelli aggiunti):
| Dispone conversione in lavoro sostitutivo |
| --- |
| Dispone conversione in libertà controllata |
| Dispone conversione in detenzione domiciliare sostitutiva |
| Dispone conversione in semilibertà sostitutiva |
| Dispone conversione in lavoro di pubblica utilità sostitutivo |
| Dispone conversione pena  irrogata  dal GdP in  lavoro  di pubblica utilità |
| Dichiara N.D.P./N.L.P. |
| Rigetta |
| Dichiara la Propria Incompetenza |
| Dichiara L'Inammissibilita' |
| N.L.P. per intervenuta prescrizione |
| N.L.P. per accertata solvibilità |
| N.L.P. per irreperibilità - atti al PM |
| Dichiara estinta la pena per avvenuto pagamento |
| Rateizza pagamento |
| Differisce la conversione |

Adeguamenti SIUS per gestione Applicazione pene sostitutive
Per permettere lato SIUS la gestione della richiesta di Applicazione delle pene sostitutive brevi, trasmessa dalla Procura è stato concordato con il GdL SIUS, in anticipo di quanto proposto nella Scheda-35, ancora in fase di analisi, di aggiungere, i seguenti nuovi Contenuti, Oggetti ed Esiti:
Contenuto Applicazione Pene Sostitutive (U125)
Oggetti
Semilibertà sostitutiva (art. 55 - 62 L. 689/1981)
Detenzione domiciliare sostitutiva (art. 56 - 62 L. 689/1981)

Esiti
Determina le modalità di esecuzione
Dichiara N.D.P./ N.L.P
Dichiara inammissibilità
Dichiara la propria incompetenza
Dispone restituzione atti al PM


E’ stata  rivista la funzione di presa in carico per gestire la nuova operazione di Trasferimento Pena Sostitutiva



e la funzione di Dettaglio della stessa



dalla quale è possibile procedere all’iscrizione del procedimento SIUS di Applicazione Pene Sostitutive.



e la funzione di Dettaglio della stessa


dalla quale sarà possibile procedere all’iscrizione del procedimento SIUS di Applicazione Pene Sostitutive.