---
uniqueName: istruzioni-esecuzione-bonifica-difensori
displayName: "Istruzioni esecuzione Bonifica Difensori"
category: "GENERAL"
tags: []
---

# Istruzioni esecuzione Bonifica Difensori

> **File originale:** `MEV/SCHEDA_021/Docs/consegna docx/ORIGINALS/Bonifica_OK/Istruzioni esecuzione Bonifica Difensori.docx`  
> **Tipo:** DOCX

---

Attività da eseguire per la bonifica degli AVVOCATI di SIES con i dati di REGINDE
Eseguire lo script CREA TABELLA XBA_LOG_BONIFICA_AVVOCATI.sql Preparazione della tabella XBA_LOG_BONIFICA_AVVOCATI che conterrà i dettagli delle attività di bonifica.

2) 	Eseguire XBA_SALVA_TABELLE_AVVOCATI.prc      - Effettua il backup con lo stesso nome
delle tabelle coinvolte, con l'aggiunta del suffisso _SXBA (Salvataggio per bonifica Avvocati).
Le tabelle trattate sono: AVVOCATO, AVVOCATO_FASCICOLO_SIEP, AVVOCATO_FASCICOLO_SIUS, AVVOCATO_FASCICOLO_SIGE, PARTI_UDIENZA_DIFENSORE, STORICO_AVVOCATO, AVVISI_AVVOCATO,  NUOVA_ISTANZA.

3)	Eseguire XBA_MODIFICA_AVVOCATO.prc
Aggiunge di 6 colonne (PEC, 	FLAG_REGINDE, DESCR_COMUNE_STUDIO, COD_STATO_NASCITA_AVV, DESC_LUOGO_NAS_REGINDE, ID_AVVOCATO_BONIFICATO), funzionali alla bonifica Avvocati e alla nuova gestione di AVVOCATO con certificazione REGINDE.

4)	Eseguire XBA_CREA_AVV_CON_PENDENZE.prc
Preparazione della tabella XBA_AVVOCATI_CON_PENDENZE, che conterrà i dati di transito per poter eseguire la bonifica Avvocato SIES. La tabella è una immagine della tabella AVVOCATO con l’aggiunta di 3 nuove colonne AMBIENTE, NUM_PENDENZE, ID_AVVA_CERT_REGINDE.

5)  Eseguire XBA_CARICA_AVV_CON_PENDENZE.prc
Caricamento dei dati degli avvocati con pendenze, incrociando le informazioni di AVVOCATO, FASCICOLO_SIEP, FASCICOLO_SIUS, FASCICOLO_SIGE, AVVOCATO_FASCICOLO_SIEP, AVVOCATO_FASCICOLO_SIUS e AVVOCATO_FASCICOLO_SIGE.
La procedura estrae gli avvocati a cui sono collegati procedimenti SIEP,SIUS e SIGE ancora pendenti.
Un procedimento SIEP si considera pendente se non archiviato (COD_STATO_FASCICOLO <> '01').
Un procedimento SIUS si considera pendente se non in stato di Definito o di Emesso Provvedimento o di unificato (COD_STATO_FASCICOLO NOT in ('01', '07', '05')).
Un procedimento SIGE si considera pendente se la data definizione non è valorizzata (DATA_DEFINIZIONE IS NULL).
Per ciascun Avvocato selezionato vengono valorizzate le colonne AMBIENTE (nome sottosistema) e NUM_PENDENZE (totale procedimenti pendenti nell’ambiente).
I records estratti vengono registrati nella tabella XBA_AVVOCATI_CON_PENDENZE.

I risultati della procedure sono riportati nella tabella di logs creata in precedenza, di seguito un esempio:

Inizio XBA_CARICA_AVV_CON_PENDENZE. Si estraggono gli avvocati SIES per i quali sussistono fascicoli pendenti in almeno un sottosistema (SIEP, SIUS, SIGE). I dati estratti vengono inseriti nella tabella XBA_AVVOCATI_CON_PENDENZE. 		2021-06-04 14:22:49.0
============================================ 		2021-06-04 14:22:58.0
= Totale Avvocati SIEP con pendenze : 	35997	2021-06-04 14:22:58.0
= Totale Avvocati SIUS con pendenze : 	6386	2021-06-04 14:22:58.0
= Totale Avvocati SIGE con pendenze : 	826	2021-06-04 14:22:58.0
= Totale Fascicoli SIEP pendenti : 	76766	2021-06-04 14:22:58.0
= Totale Fascicoli SIUS pendenti : 	9921	2021-06-04 14:22:58.0
= Totale Fascicoli SIGE pendenti : 	1091	2021-06-04 14:22:58.0
============================================ 		2021-06-04 14:22:58.0
Fine XBA_CARICA_AVV_CON_PENDENZE. 		2021-06-04 14:22:58.0

6) Eseguire XBA_BONIFICA_AVV_CON_PENDENZE.prc
Elaborazione dei dati di avvocati SIES con pendenze, incrociando e assumendo in SIES i dati di REGINDE corrispondenti agli avvocati di SIES. La procedure effettua le seguenti operazioni:
- Scansione degli Avvocati con pendenze dalla tabella XBA_AVVOCATI_CON_PENDENZE, ordinati per COD_FISCALE, DATA_INSERIMENTO e ID_AVVOCATO decrescenti, al fine di individuare prima l'occorrenza di AVVOCATO "capostipite" verso cui far confluire le altre occorrenze afferenti allo stesso AVVOCATO.
- per l’avvocato deputato a essere certificato si ricerca nella tabella AVVOCATO_REGINDE_18112020 un record avente Cognome, Nome, Foro, Codice Fiscale, Luogo e Data Nascita uguali ai corrispondenti dati dell’avvocato deputato. In caso di condizioni verificate sull’avvocato della tabella XBA_AVVOCATI_CON_PENDENZE si procede a valorizzare FLAG_REGINDE = ‘SI’, ID_AVV_CERT_REGINDE con l’id dell’avvocato corrente e le colonne DESCR_COMUNE_STUDIO, COD_STATO_NASCITA_AVV, DESC_LUOGO_NAS_REGINDE, PEC e INDIRIZZO.
Per i records della tabella XBA_AVVOCATI_CON_PENDENZE aventi Cognome, Nome, Foro, Codice Fiscale, Luogo e Data Nascita uguali a quelli dell’avvocato "capostipite", vengono valorizzate le colonne FLAG_REGINDE = ‘NO’,  ID_AVV_CERT_REGINDE=Id dell’avvocato capostipite

Un esempio dei Risultati della procedure:

Inizio XBA_BONIFICA_AVV_CON_PENDENZE. Scansione degli Avvocati con pendenze ordinati per COD_FISCALE, DATA_INSERIMENTO e ID_AVVOCATO decrescenti; si individua così prima l’ AVVOCATO principale.							2021-06-04 17:27:26.0
==================================================		2021-06-04 17:42:38.0
=  Totale Avvocati con pendenze          : 	43209	2021-06-04 17:42:38.0
=  Avvocati presenti in REGINDE          : 	24639	2021-06-04 17:42:38.0
=  Avvocati assenti in REGINDE           : 	18570	2021-06-04 17:42:38.0
=  Avvocati certificati REGINDE          : 	10357	2021-06-04 17:42:38.0
=  Avvocati collegati                    : 	14282	2021-06-04 17:42:38.0
=  Avvocati con pendenze aggiornati      : 	24639	2021-06-04 17:42:38.0
==================================================		2021-06-04 17:42:38.0
Fine XBA_BONIFICA_AVV_CON_PENDENZE. 		2021-06-04 17:42:38.0

7) Eseguire XBA_BONIFICA_AVVOCATO.prc					 - Individuazione degli avvocati SIES deputati a divenire "certificati REGINDE" in base a NOME, COGNOME, C.F., LUOGO e DATA di NASCITA.
La procedura estrae da XBA_AVVOCATI_CON_PENDENZE i records aventi ID_AVV_CERT_REGINDE valorizzato (not null), quindi già associati con un avvocato REGINDE,
-- ordinati per ID_AVV_CERT_REGINDE e DATA_INSERIMENTO decrescenti.
-- Il cursore così individua prima le occorrenza di AVVOCATO che saranno certificati REGINDE
e subito dopo le occorrenze collegate allo stesso AVVOCATO ( aventi lo stesso ID_AVV_CERT_REGINDE ) per i quali si procederà a modificare l’AVV_ID_AVVOCATO nelle tabelle di relazione

Per gli avvocati della tabella XBA_AVVOCATI_CON_PENDENZE, certificati REGINDE  (FLAG_REGINDE = ‘SI’) saranno valorizzate le colonne FLAG_CANCELLATO = ‘N’, COD_NON_ATTIVITA = 'A', FLAG_REGINDE = ‘SI’, COD_UFFICIO_APPARTENENZA = ‘00000’, FLAG_REGINDE = ‘SI’, COD_OPERATORE_AGGIORNAMENTO = 'Update Bonifica ReGIndE', DATA_AGGIORNAMENTO = CURRENT_DATE,  mentre le colonne PEC, DESCR_COMUNE_STUDIO , COD_STATO_NASCITA_AVV, DESC_LUOGO_NAS_REGINDE saranno valorizzate con il contenuto delle corrispondenti colonne di DESC_LUOGO_NAS_REGINDE.

Per gli avvocati della tabella XBA_AVVOCATI_CON_PENDENZE, non certificati REGINDE  (FLAG_REGINDE = ‘NO’) ma con  ID_AVV_CERT_REGINDE valorizzato, saranno valorizzate le colonne FLAG_CANCELLATO = ‘S’, FLAG_REGINDE = ‘NO’, ID_AVVOCATO_BONIFICATO = ID_AVV_CERT_REGINDE, COD_OPERATORE_AGGIORNAMENTO = 'Update Bonifica ReGIndE', DATA_AGGIORNAMENTO = CURRENT_DATE.  (ID_AVVOCATO_BONIFICATO contiene il valore dell’avvocato sotto cui migrano i procedimenti pendenti).
Per ognuno di essi si procede a modificare nelle tabella AVVOCATO_FASCICOLO_SIEP,  AVVOCATO_FASCICOLO_SIUS, AVVOCATO_FASCICOLO_SIGE, PARTI_UDIENZA_DIFENSORE, STORICO_AVVOCATO, AVVISI_AVVOCATO, NUOVA_ISTANZA  il valore di AVV_ID_AVVOCATO impostandolo a
ID_AVV_CERT_REGINDE
Un esempio dei Risultati della procedure:

==================================================
Inizio XBA_BONIFICA_AVVOCATO. Individuazione degli avvocati SIES deputati a divenire certificati REGINDE.
==================================================
=  Avvocati con pendenze letti           : 	24639
=  AVVOCATI aggiornati                   : 	24639
=  Avvocati certificati REGINDE          : 	10357
=  Avvocati collegati ai referenti       : 	14282
=  AVVOCATO_FASCICOLO_SIEP aggiornati    : 	32860
=  AVVOCATO_FASCICOLO_SIUS aggiornati    : 	5346
=  AVVOCATO_FASCICOLO_SIGE aggiornati    : 	596
=  PARTI_UDIENZA_DIFENSORE aggiornati    : 	0
=  STORICO_AVVOCATO aggiornati           : 	94171
=  AVVISI_AVVOCATO aggiornati            : 	3
=  NUOVA_ISTANZA aggiornati              : 	2048
==================================================
Fine XBA_BONIFICA_AVVOCATO

8) XBA_RESTORE_TABELLE_AVVOCATI.prc		 - Da utilizzare solo per il ripristino delle tabelle modificate.