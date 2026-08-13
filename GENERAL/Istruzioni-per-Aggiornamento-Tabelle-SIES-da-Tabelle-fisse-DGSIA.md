---
uniqueName: istruzioni-per-aggiornamento-tabelle-sies-da-tabel
displayName: "Istruzioni per Aggiornamento Tabelle SIES da Tabelle fisse DGSIA"
category: "GENERAL"
tags: []
---

# Istruzioni per Aggiornamento Tabelle SIES da Tabelle fisse DGSIA

> **File originale:** `MEV/SCHEDA_021/Docs/consegna docx/ORIGINALS/Aggiornamento Tabelle Fisse_OK/Istruzioni per Aggiornamento Tabelle SIES da Tabelle fisse DGSIA.docx`  
> **Tipo:** DOCX

---

Istruzioni per Aggiornamento Tabella SIES da Tabella fissa DGSIA     OK

Aggiornamento tabella COMUNE

creare tabella d’appoggio COMUNE_TF per import tabella excel Dgsia COMUNE.xlsx

eseguire  contenuto file      Crea Tabella COMUNE_TF.sql

importare il file excel con un tool di gestione di DB Oracle, di seguito si riporta la procedura eseguita con Toad
N.B. E’ possibile bypassare la fase di importazione eseguendo lo script
Insert COMUNE_TF.sql




proseguire


proseguire

proseguire
Attendere la risposta del sistema (alcuni minuti)

proseguire

spuntare tutte le colonne e proseguire

impostare i campi come in figura ed eseguire, dopo alcuni minuti la procedura terminerà, importando 13249 records, di cui 5230 privi di codice catastale e 4742 privi di Cod_SEDE_Giudiziaria

Prima di procedere con le attività di allineamento delle diverse tabelle SIES, bisogna eseguire la seguente procedure plsql
XAT_SALVA_TABELLE_PRE_ALLINEAMENTO.prc
che esegue una copia di backup delle tabella COMUNE, CG_REF_CODES e CODICI_SIES_NSC nelle tabelle COMUNE_SXALLTF, CG_REF_CODES_SXALLTF e CODICI_SIES_NSC_SXALLTF.
Aggiungere alla tabella COMUNE le nuove colonne COD_CATASTALE_COMUNE, DATA_AGGIORNAMENTO_COMUNE, DATA_FINE_VALIDITA_COMUNE          , eseguendo lo script
Alter_Comune.sql
Prima dell’aggiornamento la tabella COMUNE contiene 8112 records.
La tabella COMUNE_TF di Tabelle_Fisse 13249 records, di cui 5230 privi di Codice Catastale, di cui  4742 records privi di COD_SEDE_GIUDIZIARIA.
Compilare ed eseguire la procedure

AGGIORNA_COMUNE.prc

che legge i records dalla tabella COMUNE TF e per ciascun record ricerca nella tabella COMUNE Sies il records avente COD_COMUNE =COD_COMUNE_TF ed effettua le seguenti operazioni:

in caso di esistenza del record effettua l’aggiornamento del valore contenuto in alcune colonne con quello contenuto nella tabella fissa, come di seguito riportato:

COD_PROVINCIA    = V_COD_PROVINCIA_TF,
DESCRIZIONE      = V_DESCRIZIONE_TF,
CAP             = V_CAP_TF,
COD_SEDE_GIUDIZIARIA = V_COD_SEDE_GIUDIZIARIA_TF,
FLAG_VALIDITA = W_FLAG_VALIDITA,
COD_CATASTALE = V_COD_CATASTALE_TF,
DATA_AGGIORNAMENTO = TO_DATE ('05022021','dd/mm/yyyy'),
DATA_FINE_VALIDITA = V_DATA_FINE_VALIDITA_TF
dove W_FLAG_VALIDITA = ‘N’ se DATA_FINE_VALIDITA valorizzata, diversamente = ‘S’
in caso di non esistenza di alcun record, inserisce un nuovo record nella tabella COMUNE Sies:
INSERT INTO COMUNE  VALUES (V_COD_COMUNE_TF, V_COD_PROVINCIA_TF,            V_DESCRIZIONE_TF, V_CAP_TF, SYSDATE, V_COD_SEDE_GIUDIZIARIA_TF, W_FLAG_VALIDITA, V_COD_CATASTALE_TF, SYSDATE, 	V_DATA_FINE_VALIDITA_TF);

Al termine dell’esecuzione della procedura di aggiornamento la tabella COMUNE Sies conterrà  13327 records (13249 della Comune TF + 78 records preesistenti nella tabella SIES ma non in quella TF), di cui 5308 privi di codice catastale e 4742 privi di cod_sede_giudiziaria.

I 78 records preesistenti  (Comuni della Sardegna che dall’1/1/2006 hanno cambiato provincia) sono caratterizzati dall’aver la colonna DATA_AGGIORNAMENTO non valorizzata. Questi records sarebbero da aggiungere nella tabella COMUNE TF, a tale scopo è stato realizzato lo script

Insert Comuni assenti in Tabelle Fisse.sql

che andrà personalizzato a cura dei tecnici che gestiscono le tabelle fisse.

Per questi stessi comuni vanno valorizzate sulla tabella COMUNE le colonne COD_CATASTALE_COMUNE, DATA_FINE_VALIDITA_COMUNE e FLAG_VALIDITA eseguendo lo script

Aggiornamento Comuni non presenti in COMUNE_TF.sql.

Poiché l’allineamento della tabella COMUNE alla tabella COMUNE_TF, con l’aggiunta del Codice Catastale, è propedeutico alla valorizzazione del corretto luogo di nascita nella tabella Avvocato_ReGIndE, è stata realizzata la procedura plsql

VERIFICA_LN_AVVOCATO.prc

che, estraendo per ciascun avvocato della tabella Avvocato_ReGIndE, già importata in SIES nella tabella AVVOCATO_REGINDE_18112020 (vedi documento su Bonifica Avvocati)  il codice catastale dal codice fiscale, verifica l’esistenza nella tabella COMUNE di un record avente COD_CATASTALE_COMUNE = Codice catastale estratto dal codice fiscale, in caso di esistenza valorizza per l’avvocato corrente le colonne COD_CATASTO, COD_COMUNE con i corrispondenti valori presenti nel record COMUNE.

Al termine dell’elaborazione su 242948 records della tabella AVVOCATO_REGINDE_18112020 4433 records rimanevano privi di COD_CATASTO, di cui 729 erano relativi ad avvocati nati in Italia e 3704 ad avvocati nati all’estero.

I 729 records sono stati estratti con la seguente query

SELECT * FROM AVVOCATO_REGINDE_18112020 WHERE COD_CATASTO IS NULL and substr(codfisc,12,4) not like '%Z%' order by luogo_nascita

e salvati nel file Difensori privi di cod_catasto.xlsx. Sul contenuto di questo file è stata effettuata un’attenta analisi, da cui è emersa l’esistenza di codici fiscali con omocodia (la cui gestione è riportata nel secondo foglio del file), riuscendo a risalire al comune ed al codice catastale corretto, e preparato uno script contenente le queries di aggiornamento dei comuni privi di codice catastale (122 comuni)

AGGIORNAMENTO COMUNI DOPO VERIFICA.sql

Dopo aver eseguito questo aggiornamento, per poter valorizzare i codici catastali dei 729 avvocati della tabella AVVOCATO_REGINDE_18112020, è stata realizzata la procedure plsql

VERIFICA_LN_AVVOCATO_2.prc

in cui è inserita anche la gestione dell’omocodia.

Al termine dell’esecuzione tutti i 729 avvocati risultavano con il codice catastale valorizzato. Rimanevano quindi 3704 avvocati nati all’estero ancora privi di codice catastale (VEDI DI SEGUITO)

Allo scopo di valorizzare il codice catastale di numerosi comuni, con data fine validità valorizzata, dovuta ai cambi di provincia subiti nel tempo dallo stesso comune, si è realizzata la procedure plsql

VALORIZZA_COD_CATASTALE_COMUNE.prc

che estrae tutti i comuni, aventi DATA_FINE_VALIDITA_COMUNE valorizzata e cod_catastale_comune non valorizzato, e per ciascuno ricerca l’eventuale records avente uguale descrizione e cod_catastale_comune valorizzato, in caso di records trovato si procede ad aggiornare il codice catastale del comune estratto con quello trovato.

Poichè la procedura ha causato l’assegnazione di codice catastale improprio a comuni omonimi ma non delle stesse province cambiate nel tempo, si è provveduto a una verifica manuale dei comuni aggiornati, a seguito della quale è stato realizzato lo script

Aggiorna cod_catastale - 2.sql

Dalla analisi della nuova tabella COMUNE è emerso che sussisteva ancora il problema dell’errata impostazione della colonna COD_SEDE_GIUDIZIARIA dei comuni appartenenti alle Circoscrizioni Giudiziarie soppresse nel settembre 2013, per i quali non si era mai proceduto ad aggiornarla con il codice della sede diventata competente, a seguito dell’accorpamento. Si è quindi proceduto a una verifica manuale dei diversi comuni interessati all’aggiornamento, raffrontando la situazione con la tabella Comuni del Casellario.
E’ stato quindi realizzato il seguente script

Aggiorna Sede_Giudiziaria su COMUNE.sql




Aggiornamento Dominio PROVINCIA nella CG_REF_CODES

Dopo aver creato la tabella PROVINCIA_TF, utilizzando lo script

Crea Tabella PROVINCIA_TF.sql

ed avervi importato il contenuto del file PROVINCIA.xls, facente parte delle Tabelle Fisse, fornito dall’Amministrazione,

N.B. E’ possibile bypassare la fase di importazione eseguendo lo script
Insert PROVINCIA_TF finale
per aggiornare il dominio PROVINCIA della CG_REF_CODES bisogna eseguire la procedure plsql

AGGIORNA_DOMINIO_PROVINCIA.prc

che leggendo i records della tabella PROVINCIA_TF, per ciascun record ricerca nella tabella CG_REF_CODES il record avente RV_DOMAIN = ‘PROVINCIA’ e RV_LOW_VALUE = valore della colonna COD_PROVINCIA_TF ed effettua le seguenti operazioni:

se esiste il record procede ad aggiornarlo, impostando i seguenti valori RV_HIGH_VALUE = valore di COD_REGIONE_TF, RV_ABBREVIATION = valore di FINE_VALIDITA_TF, RV_MEANING = valore di DESCRIZIONE_TF, RV_ALT2_VALUE = ‘AGG-data esecuzione’
se il record non esiste procede ad inserire un nuovo record nella tabella CG_REF_CODES, impostando i seguenti valori RV_DOMAIN = ‘PROVINCIA’, RV_LOW_VALUE = valore di COD_PROVINCIA_TF, RV_HIGH_VALUE = valore di COD_REGIONE_TF RV_ABBREVIATION = valore di FINE_VALIDITA_TF, RV_MEANING = valore di DESCRIZIONE_TF, RV_ALT2_VALUE = ‘INS-data esecuzione’

RV_ALT2_VALUE è stata utilizzata per distinguere i records aggiornati e quelli inseriti, probabilmente da ripulire al momento del rilascio e distribuzione nei Distretti.

Da una verifica manuale effettuata succesivamente all’aggiornamento, emerge che

nel Dominio Provincia bisogna aggiornare alcune colonne per le province ES, FO, PS preesistenti in SIES

eseguendo lo script AGGIORNA DOMINIO PROVINCIA dopo allineamento.sql

nella tabella fissa PROVINCIA mancano i seguenti records, presenti nel Dominio di SIES

| Cod_Provincia | Cod_Regione | Fine_Validita | Descrizione |
| --- | --- | --- | --- |
| ES |  |  | ESTERO |
| FO | 08 | SI | FORLI' |
| PS | 11 | SI | PESARO |


che andrebbero aggiunti anche nella tabella PROVINCIA Tabelle Fisse (preparato script Insert PROVINCIA mancanti in Tabelle Fisse.sql eventualmente da personalizzare dai tecnici dell’Amministrazione).

Per preparare il Dominio PROVINCIA allo stato di esercizio, ripulendo la colonna RV_ALT2_VALUE, bisogna eseguire lo script

Ripulisci CG_REF_CODES  COMUNE per distribuzione.sql



Per la distribuzione del dominio Aggiornato nei Distretti è stato preparato il seguente script

Aggiornamento CG_REF_CODES  PROVINCIA esercizio.sql

che cancella i preesistenti records del Dominio PROVINCIA dalla tabella CG_REF_CODES e inserisce i nuovi.

Aggiornamento Dominio NAZIONE nella CG_REF_CODES

Premessa: come si è visto nel paragrafo relativo all’aggiornamento della tabella COMUNE, nella tabella AVVOCATO_REGINDE_18112020 erano rimasti 3704 avvocati nati all’estero, caratterizzati da Codice Catastale valorizzato, da cui decodificando il codice Belfiore, sarebbe possibile risalire allo Stato estero di Nascita. Purtroppo la tabella fissa STATO_NAZIONE non contiene il codice catastale, ma essendo necessario per il recupero dei suddetti avvocati, si è proceduto manualmente a recuperare e valorizzare il codice catastale di ciascun stato estero, attingendo al file Elenco-codici-e-denominazioni Stati Esteri al-31_12_2020.xls dell’Istat e alla tabella DC_TAB_STATO_ESTERO del Casellario. Su 263 records contenuti nella tabella STATO-NAZIONE sono stati valorizzati 245 codici catastali, per i rimanenti 18 non si è riusciti a risalire a tale valore.

Dopo aver creato la tabella STATO_NAZIONE_TF, utilizzando lo script Crea Tabella STATO_NAZIONE_TF.sql, si è importato il contenuto del file STATO-NAZIONE.xls, facente parte delle Tabelle Fisse, fornito dall’Amministrazione, e successivamente si è provveduto ad aggiungere a mano nella colonna COD_CATASTALE_TF i valori dei Codici Catastali.

Per valorizzare il COD_CATASTALE_TF sulla tabella importate bisogna eseguire lo script, in cui sono stati riportati tutti gli aggiornamenti fatti manualmente,

Valorizzazione cod_catastale STATO_NAZIONE

N.B. è possibile bypassare la fase di importazione  e valorizzazione del codice catastale eseguendo lo script

Insert STATO_NAZIONE_TF finale

Per l’aggiornamento del dominio ‘NAZIONE’ bisogna eseguire la procedure plsql

AGGIORNA_DOMINIO_NAZIONE.prc

che leggendo i records della tabella STATO_NAZIONE_TF, per ciascun record ricerca nella tabella CG_REF_CODES il record avente RV_DOMAIN = ‘NAZIONE’ e RV_LOW_VALUE = valore della colonna COD_STATO_TF ed effettua le seguenti operazioni:

se esiste il record procede ad aggiornarlo, impostando i seguenti valori RV_HIGH_VALUE = valore di COD_STATO_ISO_TF , RV_ABBREVIATION = valore di COD_STATO_ISTAT_TF, RV_MEANING = valore di DESCRIZIONE_TF, RV_ALT2_VALUE = valore di COD_CATASTALE_TF, RV_ALT3_VALUE = V_DATA_FINE_VALIDITA_TF, RV_ALT4_VALUE = 'AGG-data esecuzione'
se il record non esiste procede ad inserire un nuovo record nella tabella CG_REF_CODES, impostando i seguenti valori RV_DOMAIN = ‘NAZIONE’, RV_LOW_VALUE = valore di COD_STATO_TF, RV_HIGH_VALUE = valore di COD_STATO_ISO_TF , RV_ABBREVIATION = valore di COD_STATO_ISTAT_TF, RV_MEANING = valore di DESCRIZIONE_TF, RV_ALT2_VALUE = valore di COD_CATASTALE_TF, RV_ALT3_VALUE = V_DATA_FINE_VALIDITA_TF, RV_ALT4_VALUE = 'INS-data esecuzione'

RV_ALT4_VALUE è stata utilizzata per distinguere i records aggiornati e quelli inseriti, probabilmente da ripulire al momento del rilascio. Al termine dell’aggiornamento nel dominio ‘Nazione’ sono presenti 269 records di cui 238 con codice catastale (RV_ALT2_VALUE) valorizzato.

Da una verifica manuale effettuata succesivamente all’aggiornamento, emerge che

nel Dominio NAZIONE sono presenti i seguenti records, preesistenti all’aggiornamento,

| 258 |  |  | POLINESIA FRANCESE | Z723 |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 540 |  |  | NUOVA CALEDONIA | Z716 |  |  |  |
| 800 |  |  | PALESTINA | Z161 |  |  |  |
| 998 |  |  | JUGOSLAVIA | Z118 |  |  |  |


che dovrebbero essere aggiunti alla tabella fissa STATO-NAZIONE.

Per verificare che la valorizzazione del codice catastale per il dominio NAZIONE sia sufficiente a recuperare lo stato di nascita dei 3704 avvocati ReGIndE, è stata realizzata la procedure plsql

VERIFICA_LN_AVVOCATO_3.prc

dopo la prima esecuzione per 5 avvocati non era stato valorizzato il codice catastale (Z111), in quanto nella tabella STATO_NAZIONE_TF manca la Repubblica Democratica Tedesca. Si è quindi provveduto ad inserirla nel Dominio NAZIONE e nella tabella STATO_NAZIONE_TF e a rieseguire la procedure. Al termine dell’esecuzione tutti gli avvocati RegIndE risultavano con codice catastale valorizzato.

Per l’inserimento dei records mancanti in STATO-NAZIONE è stato preparato il seguente script

Insert Stati in STATO-NAZIONE.sql

che va modificato in base alle esatte nomenclature delle colonne della suddetta tabella.

Se l’Amministrazione ritiene opportuno aggiungere alla tabella fissa STATO-NAZIONE una ulteriore colonna Codice_catastale per potervi inserire i valori  aggiunti nel Dominio NAZIONE di SIES può utilizzare lo script

Valorizzazione cod_catastale STATO_NAZIONE.sql

che va modificato in base alle esatte nomenclature delle colonne della suddetta tabella.

Per preparare il Dominio Nazione allo stato di esercizio, ripulendo la colonna RV_ALT4_VALUE, bisogna eseguire lo script

Ripulisci CG_REF_CODES  COMUNE per distribuzione.sql



Per la distribuzione del dominio Aggiornato nei Distretti è stato preparato il seguente script

Aggiornamento CG_REF_CODES  NAZIONE esercizio.sql

che cancella i preesistenti records del Dominio NAZIONE dalla tabella CG_REF_CODES e inserisce i nuovi.

Aggiornamento Dominio REGIONE nella CG_REF_CODES

L’analisi del contenuto del file REGIONE.xls fornito dall’Amministrazione e del dominio ‘REGIONE’ della CG_REF_CODES, ha evidenziato che in quest’ultima bisogna aggiungere solo un record per la Regione = LUOGO SCONOSCIUTO, a tela fine bisogna eseguire lo script

Insert REGIONE.sql


Aggiornamento tabella CODICI_SIES_NSC   per   CO_DOMAIN = ‘COMUNE’

Prima di operare sulla tabella bisogna prima modificare la costraints CODICI_SIES_NSC_PK aggiungendo alle attuali colonne CO_DOMAIN, CO_CODCENTR anche la colonna CO_SIES, eseguendo il seguente script

ALTER CODICI_SIES_NSC.sql

per consentire la presenza di più records riferiti allo stesso CO_CODCENTR.

Nella tabella  per il dominio ‘COMUNE’ erano presenti 8145 records.

Con la procedura AGGIORNA_CO_DOMAIN_NSC_COMUNE.prc sono stati aggiornati i records della tabella sulla base dei records della tabella COMUNE allineata, escludendo i records di questa tabella aventi COD_SEDE_GIUDIZIARIA non valorizzata, portando il numero di records a 8621.

La procedura ha provveduto ad

- aggiornare i records, già presenti in tabella, aventi il valore CO_SIES = COD_COMUNE (impostando il CO_VAL1 = AGG-30032021);
- inserire un nuovo record per ciascun COMUNE non presente in tabella, così valorizzato CO_DOMAIN = ‘COMUNE’
CO_CODCENTR = valore COD_COMUNE
CO_NSC = ‘-‘
CO_NSC_DES = ‘-‘
CO_SIES = valore COD_COMUNE
CO_SIES_DES = DESCRIZIONE
CO_VAL1 = INS-30032021

di questi 613 nuovi records, molti sono riferiti a comuni già esistenti nella tabella CODICI_SIES_NSC, che hanno subito cambi di PROVINCIA.

In genere i records di questo dominio hanno il valore della colonna CO_CODCENTR corrispondente a quello di CO_SIES, vi sono però diverse eccezioni, essendo questo codice corrispondente al valore CODICE_UNIVOCO della tabella DC_TAB_COMUNI del Casellario, che lo gestisce (es. per il comune di CALASCA CASTIGLIONE con cod_comune=103014 il codice_univoco=1A3014).

Per valorizzare in maniera corretta i valori di CO_CODCENTR, CO_NSC e CO_NSC_DES di questi records sono state eseguite le seguenti operazioni:

realizzazione della procedure VALORIZZA_CO_DOMAIN_NSC_COMUNE.prc, che ricerca per ciascuno records avente CO_NSC e CO_NSC_DES impostati a ‘-‘ quello già presente nella tabella prima dell’aggiornamento con la stesso valore di  CO_SIES_DES, selezionando i valori presenti nelle tre colonne suddette, con cui provvede alla valorizzazione dei records inseriti. Sono stati recuperati 459 records;
verifica manuale dei rimanenti 154 records che la procedure non è riuscita ad accoppiare  con un record già valorizzato, per cui  le colonne CO_NSC e CO_NSC_DES sono rimaste impostate a ‘-‘ , verificando l’esistenza nella tabella DC_TAB_COMUNI di esercizio del Casellario, recuperandone i valori con cui impostare le suddette 3 colonne.
verifica manuale dei records con più di una occorrenza, per verificare se trattasi di comuni che hanno codici differenti a seguito del cambio provincia e verifica dell’esistenza nella tabella DC_TAB_COMUNI.

Questo lavoro di verifica è sintetizzato nei 2 seguenti script:

Aggiorna CODICI_SIES_NSC COMUNE dopo valorizzazione.sql

che esegue l’aggiornamento di parte dei records che al termine della valorizzazione avevano le colonne CO_NSC e CO_NSC_DES impostati a ‘-‘;

Delete CODICI_SIES_NSC dopo valorizzazione.sql
che esegue la cancellazione dei records che non sono presenti in DC_TAB_COMUNI di NSC o che sono stati impropriamente associati a un comune omonimo, ma appartenente a provincia differente da quella di competenza.

Al termine di tutte le suddette operazioni nel Dominio COMUNE saranno presenti 8607 records.

Infine per permettere alla funzione di intoperabilità SIES-NSC, in fase di iscrizione di un titolo esecutivo da NSC di valorizzare, in caso di comune di nascita con più occorrenze sulla tabella COMUNE e CODICI_SIES_NSC, il luogo di nascita del soggetto con il comune attivo all’epoca della nascita, si procede alla valorizzazione della colonna CO_VAL3 con la data_fine_validita_comune presente nella tabella COMUNE, a tale scopo va eseguito lo script

Valorizza CO_VAL3 con data_fine_validità comune.sql

Per preparare il Dominio Comune allo stato di esercizio, ripulendo le colonne CO_VAL1 e CO_VAL2 e cancellando i records con colonne non valorizzate correttamente, bisogna eseguire lo script

Ripulisci CODICI_SIES_NSC COMUNE per distribuzione.sql


Per la distribuzione del dominio Aggiornato nei Distretti è stato preparato il seguente script

Aggiornamento CODICI_SIES_NSC  COMUNE esercizio.sql

che cancella i preesistenti records del Dominio COMUNE dalla tabella CODICI_SIES_NSC e inserisce i nuovi.


Aggiornamento tabella CODICI_SIES_NSC  per    CO_SIES = ‘NAZIONE’

Nella tabella  CODICI_SIES_NSC per il dominio CO_DOMAIN= ‘NAZIONE’ erano presenti 201 records.

Per aggiornare  questo dominio sono stati sulla base dei records della tabella CG_REF_CODES del dominio ‘NAZIONE’  bisogna eseguire la procedure plsql

AGGIORNA_CO_DOMAIN_NSC_NAZIONE.prc

che aggiunge ai preesistenti ulteriori 69 records  (N.B. prima di eseguire la procedure bisogna eliminare il record doppio (CO_SIES = ‘254’) con CO_CODCENTR = 25401).

La procedura provvede ad

- aggiornare i records, già presenti in tabella, aventi il valore CO_SIES = RV_LOW_VALUE dei records della  CG_REF_CODES aventi RV_DOMAIN = ‘NAZIONE’ (impostando il CO_VAL1 = AGG-30032021);
- inserire un nuovo record per ciascun record del dominio NAZIONE non presente in tabella, così valorizzato
CO_DOMAIN = ‘NAZIONE’
CO_CODCENTR = valore RV_LOW_VALUE record della CG_REF_CODES con RV_DOMAIN = ‘NAZIONE’
CO_NSC = ‘-‘
CO_NSC_DES = valore RV_MEANING record della CG_REF_CODES con RV_DOMAIN = ‘NAZIONE’
CO_SIES = CO_CODCENTR
CO_SIES_DES = CO_NSC_DES
CO_VAL1 = INS-30032021

Per valorizzare in maniera corretta i valori di CO_CODCENTR, CO_NSC e CO_NSC_DES di questi records è stata eseguita una verifica manuale di tutti i 69 records per accertarsi della presenza degli stessi nella tabella DC_TAB_ESTERO di esercizio del Casellario, recuperandone i valori con cui impostare le suddette 3 colonne. Dalla verifica è emerso che nella tabella DC_TAB_ESTERO sono assenti i seguenti stati (32), che pertanto saranno momentaneamente eliminati dalla tabella CODICI_SIES_NSC (durante l’attività di verifica per questi records è stato impostato la colonna CO_VAL2 = ‘NO NSC’)

| CO_CODCENTR | CO_NSC | CO_NSC_DES | CO_SIES | CO_SIES_DES |
| --- | --- | --- | --- | --- |
|  |  |  | 312 | CHRISTMAS ISLAND |
|  |  |  | 318 | COCOS(KEELING) ISLAND |
|  |  |  | 338 | TIMOR LESTE |
|  |  |  | 439 | MAYOTTE (ISOLA) |
|  |  |  | 520 | GROENLANDIA |
|  |  |  | 528 | MONTSERRAT (ISOLA) |
|  |  |  | 537 | TURKS E CAICOS |
|  |  |  | 714 | MIDWAY (ISOLE) |
|  |  |  | 718 | NUOVA CALEDONIA(ISOLE) |
|  |  |  | 717 | NORFOLK ISLAND |
|  |  |  | 729 | TOKELAU (ISOLE DELL'UNIONE) |
|  |  |  | 811 | ALAND (ISOLE) |
|  |  |  | 813 | ASCENSION(ISOLA) |
|  |  |  | 814 | BOUVET (ISOLA) |
|  |  |  | 815 | CLIPPERTON (ISOLA) |
|  |  |  | 816 | CURACAO |
|  |  |  | 819 | HEARD E MCDONALD (ISOLE) |
|  |  |  | 821 | SINT MAARTEN |
|  |  |  | 822 | SUD GEORGIA E ISOLE SANDWICH |
|  |  |  | 823 | SVALBARG E JAN MAYEN |
|  |  |  | 824 | TERRITORI BRIT.OCEANO INDIANO |
|  |  |  | 825 | TRISTAN DA CUNHA |
|  |  |  | 826 | DIEGO GARCIA |
|  |  |  | 827 | BONAIRE S.EUSTACHIUS E SABA |
|  |  |  | 888 | RICONOSCIUTI NN CITTAD.LETTONI |
|  |  |  | 904 | SAINT MARTIN SETTENTRIONALE |
|  |  |  | 906 | SAINT BARTHELEMY |
|  |  |  | 926 | ARUBA |
|  |  |  | 939 | SARK |
|  |  |  | 988 | TERRE AUSTR.E ANTART.FRANCESI |
|  |  |  | 0 | STATO SCONOSCIUTO |
|  |  |  | 100 | NESSUN LUOGO |



I suddetti records sono stati salvati nei files Nazione-SIES-NSC assenti in NSC.xls e Nazione-SIES-NSC assenti in NSC.sql.

Inoltre dei rimanenti records inseriti, i seguenti 32 records, pur presenti in DC_TAB_ESTERO non presentano alcun valore nelle colonne CODICE_UNIVOCO, utilizzato per la valorizzazione della colonna CO_CODCENTR (durante l’attività di verifica per questi records è stato impostato la colonna CO_VAL2 = ‘VER NSC’)

| CO_CODCENTR | CO_NSC | CO_NSC_DES | CO_SIES | CO_SIES_DES |
| --- | --- | --- | --- | --- |
|  | 09617168 | FAROER | 213 | FAER OER (ISOLE) |
|  | 09615713 | GIBILTERRA | 218 | GIBILTERRA |
|  | 09640048 | KOSOVO | 272 | KOSOVO |
|  | 09610572 | U.R.S.S. | 352 | UNIONE REP.SOC.SOVIETICHE |
|  | 09629097 | REUNION (LA) | 445 | REUNION (ISOLE) |
|  | 09630651 | SAINT ELENA (ISOLA) | 447 | SAINT ELENA (ISOLA) |
|  | 09640058 | SUD SUDAN | 467 | SUD SUDAN |
|  | 09631039 | ANGUILLA | 502 | ANGUILLA |
|  | 09613482 | ANTILLE OLANDESI | 504 | ANTILLE OLANDESI |
|  | 09614258 | BERMUDA (ISOLE) | 508 | BERMUDA (ISOLE) |
|  | 09630942 | CAYMAN (ISOLE) | 511 | CAYMAN (ISOLE) |
|  | 09616004 | GUADALUPA | 521 | GUADALUPA |
|  | 09618138 | MARTINICA | 526 | MARTINICA |
|  | 09612318 | PORTORICO | 531 | PORTORICO |
|  | 09640079 | SAINT PIERRE ET MIQUELON | 535 | SAINT PIERRE ET MIQUELON |
|  | 09630360 | VERGINI AMERICANE (ISOLE) | 538 | VERGINI AMERICANE (ISOLE) |
|  | 09629875 | VERGINI BRITANNICHE (ISOLE) | 539 | VERGINI BRITANNICHE (ISOLE) |
|  | 09629681 | FALKLAND O MALVINE (ISOLE) | 610 | FALKLAND O MALVINE (ISOLE) |
|  | 09629487 | COOK (ISOLE) | 702 | COOK (ISOLE) |
|  | 09630554 | MARIANNE SETTENTR.LI (ISOLE) | 711 | MARIANNE SETTENTR.LI (ISOLE) |
|  | 09629390 | NIUE | 716 | NIUE |
|  | 09629584 | PITCAIRN (ISOLE) | 723 | PITCAIRN (ISOLE) |
|  | 09630748 | AMERICAN SAMOA | 726 | AMERICAN SAMOA |
|  | 09630166 | WALLIS E FUTUNA (ISOLE) | 734 | WALLIS E FUTUNA (ISOLE) |
|  | 09616780 | HONG KONG | 740 | HONG KONG |
|  | 09629972 | MACAO | 743 | MACAO |
|  | 09616101 | GUAM | 817 | GUAM |
|  | 09630263 | SAHARA OCCIDENTALE | 820 | SAHARA OCCIDENTALE |
|  | 09613482 | ANTILLE OLANDESI (ISOLE) | 907 | ANTILLE OLANDESI (ISOLE) |
|  | 09629778 | JERSEY (CHANNEL ISLANDS) | 925 | JERSEY (CHANNEL ISLANDS) |
|  | 09630457 | GUERNSEY | 940 | GUERNESEY (CHANNEL ISLANDS) |
|  | 09629293 | MAN | 959 | MAN (ISOLA DI) |


.
I suddetti records sono stati momentaneamente eliminati dalla tabelle CODICI_SIES_NSC in attesa di verifica da parte del Casellario e sono stati salvati nei files Nazione-SIES-NSC privi di Codice_Univoco.xls e Nazione-SIES-NSC privi di Codice_Univoco.sql.

Tra gli stati aggiunti dalla procedure, sono stati correttamente valorizzati solo i seguenti:

| CO_DOMAIN | CO_CODCENTR | CO_NSC | CO_NSC_DES | CO_SIES | CO_SIES_DES |
| --- | --- | --- | --- | --- | --- |
| NAZIONE | 25701 | 09601745 | CECOSLOVACCHIA | 210 | CECOSLOVACCHIA |
| NAZIONE | 21700 | 09640063 | REPUBBLICA DEMOCRATICA TEDESCA | 217 | REPUBBLICA DEMOCRATICA TEDESCA |
| NAZIONE | 25800 | 09619302 | POLINESIA FRANCESE | 724 | POLINESIA FRANCESE |
| NAZIONE | 61201 | 09616489 | GUYANA FRANCESE | 818 | GUYANA FRANCESE |


la valorizzazione di questi record può essere effettuata eseguendo lo script

Aggiorna CODICI_SIES_NSC NAZIONE dopo valorizzazione.sql

Per preparare il Dominio Nazione allo stato di esercizio, ripulendo le colonne CO_VAL1 e CO_VAL2 e cancellando i records con colonne non valorizzate correttamente, bisogna eseguire lo script

Ripulisci CODICI_SIES_NSC NAZIONE per distribuzione.sql


Per la distribuzione del dominio Aggiornato nei Distretti è stato preparato il seguente script

Aggiornamento CODICI_SIES_NSC  NAZIONE esercizio.sql

che cancella i preesistenti records del Dominio NAZIONE dalla tabella CODICI_SIES_NSC e inserisce i nuovi.


Aggiornamento tabella COMUNI e STATI   di SIES-AVVOCATURA

Per l’allineamento delle tabelle COMUNI e STATI si procederà ad adeguare la loro struttura a quella della tabella COMUNE di SIES e ai dati gestiti nel dominio NAZIONE della CG_REF_CODES.

Per le modifiche alla struttura delle tabelle bisogna eseguire lo script:

Alter_COMUNI e STATI.sql

e successivamente gli scrpt

Aggiorna TABELLA  COMUNI SIES-AVVOCATURA.sql

e

Aggiorna TABELLA  STATI SIES-AVVOCATURA.sql



Messa in esercizio

Per la messa in esercizio della tabella COMUNE, dei Domini PROVINCIA, REGIONE e NAZIONE della tabella CG_REF_CODES, dei Domini COMUNE e NAZIONE della tabella CODICI_SIES_NSC e delle tabelle COMUNI e STATI di SIES-AVVOCATURA non ci sarà bisogno di eseguire le procedure di allineamento riportate nei precedenti paragrafi, ma si distribuiranno degli eseguibili che permetteranno di effettuare l’aggiornamento utilizzando il risultato finale delle procedure che sono state eseguite già a livello centrale. Ogni Distretto dovrà eseguire nell’ordine le seguenti operazioni:

Prima di procedere con le attività di allineamento delle diverse tabelle SIES, bisogna eseguire la seguente procedure plsql

XAT_SALVA_TABELLE_PRE_ALLINEAMENTO.prc

che esegue una copia di backup delle tabella COMUNE, CG_REF_CODES e CODICI_SIES_NSC nelle tabelle COMUNE_SXALLTF, CG_REF_CODES_SXALLTF e CODICI_SIES_NSC_SXALLTF.

eseguire lo script	Alter_Comune.sql

che aggiunge all’attuale struttura della tabella COMUNE le nuove colonne  COD_CATASTALE_COMUNE, DATA_AGGIORNAMENTO_COMUNE, DATA_FINE_VALIDITA_COMUNE.

eseguire lo script 	Aggiornamento TABELLA COMUNE esercizio.sql

che cancella i records preesistenti 8112 e ne inserisce 13327.

eseguire lo script	Aggiornamento CG_REF_CODES  PROVINCIA esercizio.sql
che cancella dalla tabella CG_REF_CODES i records aventi RV_DOMAIN = ‘PROVINCIA’ e carica i nuovi records. Il dominio conterrà 117 records a fronte dei 105 precedenti.

eseguire lo script	Insert REGIONE.sql

inserisce un nuovo record (LUOGO_SCONOSCIUTO) nella tabella CG_REF_CODES per RV_DOMAIN = ‘REGIONE’

eseguire lo script	Aggiornamento CG_REF_CODES  NAZIONE esercizio.sql
che cancella dalla tabella CG_REF_CODES i records aventi RV_DOMAIN = ‘NAZIONE’ e carica i nuovi records. Il dominio conterrà 269 records a fronte dei 200 precedenti.

eseguire lo script 	Alter_CODICI_SIES_NSC.sql
che modifica la constraint attuale, che è costituita dalle colonne (CO_DOMAIN, CO_CODCENTR), alla nuova costituita da (CO_DOMAIN, CO_CODCENTR,  CO_SIES) per permettere la gestione di comuni omonimi, che pur avendo lo stesso valore di CO_CODCENTR hanno diverso valore del CO_SIES.

eseguire lo script	Aggiornamento CODICI_SIES_NSC  COMUNE esercizio.sql
che cancella dalla tabella CODICI_SIES_NSC i records aventi CO_DOMAIN = ‘COMUNE’ e carica i nuovi records. Il dominio conterrà 8607 records a fronte degli 8145 precedenti.

eseguire lo script	Alter_COMUNI e STATI.sql

che aggiunge all’attuale struttura della tabella COMUNI le nuove colonne  COD_CATASTALE_COMUNE, DATA_AGGIORNAMENTO_COMUNE, DATA_FINE_VALIDITA_COMUNE e all’attuale struttura della tabella STATI le nuove colonne COD_STATO_ISO,   COD_ISTAT_STATO,   COD_CATASTALE e
DATA_FINE_VALIDITA

eseguire lo script 	Aggiorna TABELLA  COMUNI SIES-AVVOCATURA.sql

che cancella i records preesistenti 8112 e ne inserisce 13327.

eseguire lo script 	Aggiorna TABELLA  STATI SIES-AVVOCATURA.sql

che cancella i records preesistenti 200 e ne inserisce 269.