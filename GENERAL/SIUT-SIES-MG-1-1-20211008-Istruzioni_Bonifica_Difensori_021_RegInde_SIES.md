---
uniqueName: siut-sies-mg-1-1-20211008-istruzionibonificadifens
displayName: "SIUT SIES MG 1 1 20211008 Istruzioni Bonifica Difensori 021 RegInde SIES"
category: "GENERAL"
tags: []
---

# SIUT-SIES-MG-1.1-20211008-Istruzioni_Bonifica_Difensori_021_RegInde_SIES

> **File originale:** `MEV/SCHEDA_021/Docs/consegna docx/ORIGINALS/SIUT-SIES-MG-1.1-20211008-Istruzioni_Bonifica_Difensori_021_RegInde_SIES.docx`  
> **Tipo:** DOCX

---


Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi Direzione Generale per i Sistemi Informativi Automatizzati


Istruzioni Bonifica Difensori










Versione 1.1 del 08/10/2021





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Engineering | RTI |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 08/10/2021 |  |
| Livello di riservatezza | L3 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 30/07/2021 | Prima emissione |  |
|  |  |  |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Salvatore Piazza | RTI |  | Technical Manager |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Francesco Rosati | RTI |  | Responsabile Manutenzione Correttiva
Referente Qualità e Sicurezza |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Referente PMO e Qualità |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |
| Luigi Buglione | RTI |  | Referente Metrico |




INDICE DEI CONTENUTI
1 	Introduzione	5
1.1 Scopo del documento	5
1.2 Riferimenti	5
1.3 Glossario	5
1.3.1 Definizioni	5
1.3.2 Acronimi e abbreviazioni	5
2 	Generalità	7
3 	Descrizione delle Attività	8
3.1 Importazione tabella Avvocati ReGIndE in SIES	8
3.2 Procedura Bonifica Difensori SIES	9
3.2 Esecuzione Procedura Bonifica Difensori SIES in un unico passaggio	22

# 1 	Introduzione
## 1.1 Scopo del documento
Il presente documento viene rilasciato con lo scopo di dettagliare le attività preliminari da eseguire prima della messa in esercizio della MEV 21 RegInde e sono relative alla bonifica dei difensori sulla base dell’estrazione degli avvocati presenti in ReGInde, fornita dall’Amministrazione.
In particolare, nel seguente documento, si forniscono le istruzioni da seguire ed i relativi controlli da effettuare prima della messa in esercizio della MEV 21.
## 1.2 Riferimenti
| Riferimento | Nome Documento | Nome Documento |  |  | Descrizione Documento |
| --- | --- | --- | --- | --- | --- |
| RIF1. | SIUT-SIE-PR-1.1-20211008-Piano_di_rilascio_021_RegInde_SIES | SIUT-SIE-PR-1.1-20211008-Piano_di_rilascio_021_RegInde_SIES | SIUT-SIE-PR-1.1-20211008-Piano_di_rilascio_021_RegInde_SIES | SIUT-SIE-PR-1.1-20211008-Piano_di_rilascio_021_RegInde_SIES | Piano di rilascio |
| 1.3 Glossario 
1.3.1 Definizioni | 1.3 Glossario 
1.3.1 Definizioni | 1.3 Glossario 
1.3.1 Definizioni |  |  |  |
| Definizione | Definizione | Descrizione |  |  |  |
|  |  |  |  |  |  |


## 1.3.2 Acronimi e abbreviazioni
| Sigla | Descrizione |
| --- | --- |
| AgID | Agenzia per l’Italia Digitale |
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
| HW | HardWare |
| ICT | Information & Communication Technology |
| ISO | International Organization for Standardization |
| ISP | Information Security Policy |
| IT | Information Technology |
| KPI | Key Performance Indicator |
| MAAC | MAndatory Access Control |
| MAC | MAnutenzione Correttiva |
| MEV | Manutenzione EVolutiva |
| OWASP | Open Web Application Security Project |
| PA | Pubblica Amministrazione |
| PEC | Posta Elettronica Certificata |
| PDCA | Plan, Do, Check, Act |
| PdQ | Piano della Qualità |
| PdP | Piano di Progetto |
| PdS | Piano della Sicurezza |
| PMO | Program Management Office |
| POO | Program Operating Office |
| QM | Quality Manager |
| RA | Risk Assessment |
| RID | Riservatezza, Integrità, Disponibilità |
| RM | Resource Manager |
| RPO | Recovery Point Objective |
| RTO | Recovery Time Objective |
| RTI | Raggruppamento Temporaneo di Impresa |
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
| TT | Trouble Ticketing |
| UTA | Utente Generico Amministrazione |
| VPN | Virtual Private Network |


# 2 	Generalità
Le attività descritte sono preliminari alle attività di installazione del software relativo alla MEV-2019_21 di SIES descritte nel documento SIUT-SIES-PR-1.1-20211008-Piano_di_Rilascio_021_RegInde_SIES.doc.
# 3 	Descrizione delle Attività
Le attività descritte nel paragrafo 3.1 si articolano su scripts.sql e procedures plsql, contenuti nel pacchetto bonifica_db.zip, che va estratto ottenendo la cartella ..\bonifica_db\bonifica.
## 3.1 Importazione tabella Avvocati ReGIndE in SIES
La prima attività da eseguire è l’importazione in SIES  della tabella Avvocati Reginde, fornita dall’Amministrazione,
tabellefisse18novembre2020.xls, contenente 388221 records (disponibilità del file comunicato via e-mail da annamaria.palmieri@giustizia.ii a vito.bufi@eng.it il 23/11/2020 13:05) . Poiché nella tabella vi sono avvocati riferite ad Enti non di interesse di SIES, righe duplicate per lo stesso Difensore, si procede prima a trattamento dei dati effettuando le seguenti operazioni:

Applicare filtro su tutte le colonne
sulla colonna ODA, aprire il filtro e selezionare solo quelli non riferiti a ODA (es. Avvocatura, Consigli nazionali, Enti, vuote). Eliminare tutte le righe.
sulla colonna ODA, aprire il filtro e selezionare tutti gli  ODA
ordinare la tabella per codice fiscale cresc, tipo_indirizzo cresc, comune residenza cresc, indirizzo cresc
Scegliere Dati > Rimuovi duplicati e in Colonne selezionare la colonna Codice Fiscale. Fare clic su OK.
Salvare il file con nuovo nome  (es. tabellefisse18novembre2020-senza duplicati.xls, contenente 242948 records).
I due files .xls sono contenuti all’interno della cartella bonifica.

Bisogna quindi creare in SIES la tabella in cui importare i dati, eseguendo lo script

Crea_tabella_AVVOCATO_REGINDE_18112020.sql

che contiene le seguenti istruzioni Oracle

CREATE TABLE "AVVOCATO_REGINDE_18112020"
(	"NOME" VARCHAR2(256),
"COGNOME" VARCHAR2(256),
"CODFISC" VARCHAR2(16),
"DT_NASCITA" DATE,
"LUOGO_NASCITA" VARCHAR2(256),
"PROV_NASCITA" VARCHAR2(2),
"PEC" VARCHAR2(256),
"DESCR" VARCHAR2(256),
"CODICE" VARCHAR2(256),
"DESCR_1" VARCHAR2(256),
"TP_INDIRIZZO" VARCHAR2(1),
"INDIRIZZO" VARCHAR2(256),
"CAP" VARCHAR2(5),
"COMUNE" VARCHAR2(256),
"PROV" VARCHAR2(2),
"COD_CATASTO" VARCHAR2(4),
"COD_COMUNE" VARCHAR2(6),
"COD_NAZIONE" VARCHAR2(4)
) SEGMENT CREATION IMMEDIATE
PCTFREE 10 PCTUSED 40 INITRANS 1 MAXTRANS 255
NOCOMPRESS LOGGING
STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
TABLESPACE "SIESDIN" ;
COMMIT;

che oltre a creare tutte le colonne presenti nel file di input, aggiunge anche le colonne COD_CATASTO, COD_COMUNE e COD_NAZIONE, che saranno valorizzate successivamente con procedure plsql previste all’interno della procedura di aggiornamento della tabelle COMUNE, CG_REF_CODES e CODICI_SIES_NSC (vedi SIUT-SIES-MG-1.1-20211008 - Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_SIES). La valorizzazione delle suddette 3 colonne è un prerequisito all’avvio della procedura di Bonifica Avvocati.

Poi importare i dati utilizzando uno dei tools a disposizione (Toad, pls/developer, DbEaver,…). Questa attività deve essere eseguita a livello centrale, in modo da permettere la distribuzione nei Distretti della tabella AVVOCATO_REGINDE_18112020 già precaricata.

Nella cartella di distribuzione della procedura di bonifica è presente il file AVVOCATO_REGINDE_18112020.dmp, che va semplicemente importato in SIES.

## 3.2 Procedura Bonifica Difensori SIES
Di seguito le attività da eseguire per la bonifica degli AVVOCATI di SIES con i dati di REGINDE.


Eseguire lo script CREA_TABELLA_XBA_LOG_BONIFICA_AVVOCATI.sql Preparazione della tabella XBA_LOG_BONIFICA_AVVOCATI che conterrà i dettagli delle attività di bonifica.
Eseguire XBA_SALVA_TABELLE_AVVOCATI.prc      - Effettua il backup con lo stesso nome delle tabelle coinvolte, con l'aggiunta del suffisso _SXBA (Salvataggio per bonifica Avvocati).
Le tabelle trattate sono: AVVOCATO, AVVOCATO_FASCICOLO_SIEP, AVVOCATO_FASCICOLO_SIUS, AVVOCATO_FASCICOLO_SIGE, PARTI_UDIENZA_DIFENSORE, STORICO_AVVOCATO, AVVISI_AVVOCATO,  NUOVA_ISTANZA, CG_REF_CODES.
Le stesse tabelle, ad esclusione della  CG_REF_CODES, vengono duplicate anche con l’aggiunta del suffisso _BONIF, per loggare i records che vengono aggiornati dalla procedura. Al termine dell’attività di Bonifica queste tabelle conterranno solo i records aggiornati.

Eseguire lo script Aggiorna_AVVOCATO_FORO.sql, modifica le attuali descrizioni di alcuni fori ('REGGIO DI CALABRIA', 'REGGIO NELL''EMILIA', 'MASSA',  'CARRARA', 'FORLI''', 'CESENA') in quelle gestite in ReGIndE(‘REGGIO CALABRIA’, 'REGGIO EMILIA', 'MASSA CARRARA', 'FORLÌ-CESENA').

Eseguire lo script Aggiorna_CG_REF_CODES_NON_ATTIVITA.sql, aggiunge nuovi Stati del Difensore (A, C ,R , S) nel dominio NON_ATTIVITA della CG_REF_CODES.

Eseguire lo script Inserisci_CG_REF_CODES_FORO_AVVOCATI.sql, effettua l’aggiornamento del dominio FORO_AVVOCATI della CG_REF_CODES eliminando i preesistenti e inserendo i nuovi records, predisposti per gestire il comune sede di un Foro svincolato dalla Descrizione e con le nuove Descrizioni di alcuni fori.

Eseguire XBA_MODIFICA_AVVOCATO.prc
Aggiunge di 6 colonne (PEC, 	FLAG_REGINDE, DESCR_COMUNE_STUDIO, COD_STATO_NASCITA_AVV, DESC_LUOGO_NAS_REGINDE, ID_AVVOCATO_BONIFICATO), funzionali alla bonifica Avvocati e alla nuova gestione di AVVOCATO con certificazione REGINDE. Aggiunge anche la colonna AVV_ID_AVVOCATO_NEW su tutte le tabelle di log (con estensione _BONIF).

7)	Eseguire XBA_CREA_AVV_CON_PENDENZE.prc
Preparazione della tabella XBA_AVVOCATI_CON_PENDENZE, che conterrà i dati di transito per poter eseguire la bonifica Avvocato SIES. La tabella è una immagine della tabella AVVOCATO con l’aggiunta di 3 nuove colonne AMBIENTE, NUM_PENDENZE, ID_AVV_CERT_REGINDE.

8)  Eseguire XBA_CARICA_AVV_CON_PENDENZE.prc
Caricamento dei dati degli avvocati con pendenze, incrociando le informazioni di AVVOCATO, FASCICOLO_SIEP, FASCICOLO_SIUS, FASCICOLO_SIGE, AVVOCATO_FASCICOLO_SIEP, AVVOCATO_FASCICOLO_SIUS e AVVOCATO_FASCICOLO_SIGE.
La procedura ricerca il codice del Distretto su cui viene eseguita, in base al raggruppamento per ordine decrescente dei records FASCICOLO_SIUS, sulla base del sestultimo e quintultimo carattere della colonna ID_FASCICOLO_SIUS.
La procedura estrae gli avvocati a cui sono collegati procedimenti SIEP, SIUS e SIGE ancora pendenti, appartenenti a uffici del Distretto.
Un procedimento SIEP si considera pendente se non archiviato (COD_STATO_FASCICOLO <> '01').
Un procedimento SIUS si considera pendente se non in stato di Definito o di Emesso Provvedimento o di unificato (COD_STATO_FASCICOLO NOT in ('01', '07', '05')).
Un procedimento SIGE si considera pendente se la data definizione non è valorizzata (DATA_DEFINIZIONE IS NULL).
Per ciascun Avvocato selezionato vengono valorizzate le colonne AMBIENTE (nome sottosistema) e NUM_PENDENZE (totale procedimenti pendenti nell’ambiente).
I records estratti vengono registrati nella tabella XBA_AVVOCATI_CON_PENDENZE.

I risultati della procedure o eventuali errori sono riportati nella tabella XBA_LOG_BONIFICA_AVVOCATI creata in precedenza, di seguito un esempio:

Inizio XBA_CARICA_AVV_CON_PENDENZE. Si estraggono gli avvocati SIES per i quali sussistono fascicoli pendenti in almeno un sottosistema (SIEP, SIUS, SIGE). I dati estratti vengono inseriti nella tabella XBA_AVVOCATI_CON_PENDENZE. 		2021-06-04 14:22:49.0
============================================ 		2021-06-04 14:22:58.0
= Totale Avvocati SIEP con pendenze : 	35997	2021-06-04 14:22:58.0			(A)
= Totale Avvocati SIUS con pendenze : 	6386	2021-06-04 14:22:58.0			(B)
= Totale Avvocati SIGE con pendenze : 	826	2021-06-04 14:22:58.0			(C)
= Totale Fascicoli SIEP pendenti : 	76766	2021-06-04 14:22:58.0			(D)
= Totale Fascicoli SIUS pendenti : 	9921	2021-06-04 14:22:58.0			(E)
= Totale Fascicoli SIGE pendenti : 	1091	2021-06-04 14:22:58.0			(F)
============================================ 		2021-06-04 14:22:58.0
Fine XBA_CARICA_AVV_CON_PENDENZE. 		2021-06-04 14:22:58.0

Possibili verifiche sui dati estratti:

verificare la corrispondenza del numero di records presenti nella tabella  XBA_AVVOCATI_CON_PENDENZE con la somma dei numeri (A)+(B)+(C), riportati nella tabella XBA_LOG_BONIFICA_AVVOCATI dopo l’esecuzione della procedure
SELECT count(*) FROM XBA_AVVOCATI_CON_PENDENZE

verificare la corrispondenza dei numeri riportati in (D), (E) e (F) rispettivamente con le seguenti queries, in cui bisogna sostituire il parametro ‘valore id Avvocato’  con il valore del codice BDI su cui si sta operando

select count(*) "Pendenze SIEP x AVV" from avvocato a
JOIN AVVOCATO_FASCICOLO_SIEP ON(afs.AVV_ID_AVVOCATO = a.ID_AVVOCATO AND SUBSTR(afs.FAS_SIE_ID_FASCICOLO_SIEP,-6, 2) = ‘valore id Avvocato’)
JOIN FASCICOLO_SIEP fs ON (fs.ID_FASCICOLO_SIEP = afs.FAS_SIE_ID_FASCICOLO_SIEP
and  fs.COD_STATO_FASCICOLO <> '01' )



select count(*) "Pendenze SIUS x AVV" from avvocato a
JOIN AVVOCATO_FASCICOLO_SIUS afs ON (afs.AVV_ID_AVVOCATO = a.ID_AVVOCATO AND SUBSTR(afs.FAS_SIU_ID_FASCICOLO_SIUS,-6, 2) = ‘valore id Avvocato’)
JOIN FASCICOLO_SIUS fs ON (fs.ID_FASCICOLO_SIUS = afs.FAS_SIU_ID_FASCICOLO_SIUS
and  fs.COD_STATO_FASCICOLO  NOT IN ('01','05','07') )

select count(*) "Pendenze SIGE x AVV" from avvocato a
JOIN AVVOCATO_FASCICOLO_SIGE afs ON (afs.AVV_ID_AVVOCATO = a.ID_AVVOCATO AND SUBSTR(afs.FAS_SIGE_ID_FASCICOLO_SIGE,-6, 2) = ‘valore id Avvocato’)
JOIN FASCICOLO_SIGE fs ON (fs.ID_FASCICOLO_SIGE = afs.FAS_SIGE_ID_FASCICOLO_SIGE
and  DATA_DEFINIZIONE IS NULL )

controllare, a campione, la correttezza degli avvocati selezionati dalla procedure come candidati ad una possibile certificazione ReGIndE, eseguendo le seguenti queries

SELECT acp.COD_FISCALE, acp.ID_AVVOCATO, acp.DATA_INSERIMENTO , acp.FLAG_REGINDE, acp.NUM_PENDENZE, acp.AMBIENTE, acp.ID_AVV_CERT_REGINDE   FROM XBA_AVVOCATI_CON_PENDENZE acp  WHERE acp.FLAG_REGINDE IS NOT NULL
ORDER BY acp.COD_FISCALE , acp.DATA_INSERIMENTO DESC, acp.ID_AVVOCATO DESC;

che presenta l’elenco degli avvocati estratti dalla tabella XBA_AVVOCATI_CON_PENDENZE, riportando per ciascun record COD_FISCALE, ID_AVVOCATO, DATA_INSERIMENTO, FLAG_REGINDE, NUM_PENDENZE, AMBIENTE

BAIMRC74H03H501C	222691012009	2007-10-02 16:42:38.0	NO	1	SIEP
BBBMNC65E67G535S	252824222013	2007-09-27 10:54:18.0	NO	1	SIEP
BBDNTN44M22H501C	219849012009	2007-10-02 16:42:53.0	NO	1	SIEP
BBDNTN44M22H501C	879853242011	2007-09-17 18:59:15.0	NO	1	SIEP
BBLFDR58E52M018D	241572012013	2007-10-02 16:37:44.0	NO	1	SIGE
BBLFDR58E52M018D	220634012009	2007-10-02 16:37:44.0	NO	23	SIEP
BBLFNC69P10E472I	229500012011	2011-02-02 09:16:33.0	NO	1	SIEP
BBMSLL77L52D150V	182712102008	2008-02-12 14:32:27.0	NO	1	SIEP
BBNGPL63H22D121K	349845012016	2007-10-02 16:42:18.0	NO	1	SIUS
BBNGPL63H22D121K	349120012016	2007-10-02 16:42:18.0	NO	1	SIEP

dalla lista selezionare, a campione, un avvocato (ID_AVVOCATO) e in base al valore della colonna AMBIENTE eseguire una delle seguenti queries, in cui bisogna valorizzare ‘valore id Avvocato’ e 'valore codice BDI'

per AMBIENTE = SIEP

SELECT afs.ID_AVVOCATO_FASCICOLO_SIEP, afs.FAS_SIE_ID_FASCICOLO_SIEP, chiave_anno, chiave_progr, chiave_ufficio, cod_stato_fascicolo
FROM avvocato_fascicolo_SIEP afs, FASCICOLO_SIEP fs WHERE afs.avv_id_avvocato = ‘valore id Avvocato’ AND fs.ID_FASCICOLO_SIEP = afs.FAS_SIE_ID_FASCICOLO_SIEP
AND SUBSTR(afs.FAS_SIE_ID_FASCICOLO_SIEP,-6, 2) = 'valore codice BDI' AND fs.COD_STATO_FASCICOLO NOT IN ('01')

per AMBIENTE = SIUS

SELECT afs.ID_AVVOCATO_FASCICOLO_SIUS, afs.FAS_SIU_ID_FASCICOLO_SIUS, chiave_anno, chiave_progr, chiave_ufficio, cod_stato_fascicolo
FROM avvocato_fascicolo_sius afs, FASCICOLO_SIUS fs WHERE afs.avv_id_avvocato = ‘valore id Avvocato’ AND fs.ID_FASCICOLO_SIUS = afs.FAS_SIU_ID_FASCICOLO_SIUS
AND SUBSTR(afs.FAS_SIU_ID_FASCICOLO_SIUS,-6, 2) = 'valore codice BDI' AND fs.COD_STATO_FASCICOLO NOT IN ('01','05','07')

per AMBIENTE = SIGE

SELECT afs.ID_AVVOCATO_FASCICOLO_SIGE, afs.FAS_SIGE_ID_FASCICOLO_SIGE, chiave_anno, chiave_progr, chiave_ufficio, cod_stato_fascicolo
FROM avvocato_fascicolo_siGE afs, FASCICOLO_SIGE fs WHERE afs.avv_id_avvocato = ‘valore id Avvocato’ AND fs.ID_FASCICOLO_SIGE = afs.FAS_SIGE_ID_FASCICOLO_SIGE
AND SUBSTR(afs.FAS_SIGE_ID_FASCICOLO_SIGE,-6, 2) = 'valore codice BDI' AND fs.DATA_DEFINIZIONE IS NULL


9) Eseguire XBA_BONIFICA_AVV_CON_PENDENZE.prc

Elaborazione dei dati di avvocati SIES con pendenze, incrociando e assumendo in SIES i dati di REGINDE corrispondenti agli avvocati di SIES. La procedure effettua le seguenti operazioni:
- Scansione degli Avvocati con pendenze dalla tabella XBA_AVVOCATI_CON_PENDENZE, ordinati per COD_FISCALE, DATA_INSERIMENTO e ID_AVVOCATO decrescenti, al fine di individuare prima l'occorrenza di AVVOCATO "capostipite" verso cui far confluire le altre occorrenze afferenti allo stesso AVVOCATO.
- per l’avvocato deputato a essere certificato si ricerca nella tabella AVVOCATO_REGINDE_18112020 un record avente Cognome, Nome, Foro, Codice Fiscale, Luogo e Data Nascita uguali ai corrispondenti dati dell’avvocato deputato. In caso di condizioni verificate sull’avvocato della tabella XBA_AVVOCATI_CON_PENDENZE si procede a valorizzare FLAG_REGINDE = ‘SI’, ID_AVV_CERT_REGINDE con l’id dell’avvocato corrente e le colonne DESCR_COMUNE_STUDIO, COD_STATO_NASCITA_AVV, DESC_LUOGO_NAS_REGINDE, PEC e INDIRIZZO con i valori delle corrispondenti colonne del record AVVOCATO_REGINDE_18112020-
Per i records della tabella XBA_AVVOCATI_CON_PENDENZE aventi Cognome, Nome, Foro, Codice Fiscale, Luogo e Data Nascita uguali a quelli dell’avvocato "capostipite", vengono valorizzate le colonne FLAG_REGINDE = ‘NO’,  ID_AVV_CERT_REGINDE=Id dell’avvocato capostipite.

Un esempio dei Risultati della procedure:

Inizio XBA_BONIFICA_AVV_CON_PENDENZE. Scansione degli Avvocati con pendenze ordinati per COD_FISCALE, DATA_INSERIMENTO e ID_AVVOCATO decrescenti; si individua così prima l’ AVVOCATO principale.							2021-06-04 17:27:26.0
==================================================		2021-06-04 17:42:38.0
=  Totale Avvocati con pendenze          : 	43209	2021-06-04 17:42:38.0			(A)
=  Avvocati presenti in REGINDE          : 	24639	2021-06-04 17:42:38.0			(B)
=  Avvocati assenti in REGINDE           : 	18570	2021-06-04 17:42:38.0			(C)
=  Avvocati certificati REGINDE          : 	10357	2021-06-04 17:42:38.0			(D)
=  Avvocati collegati                    : 	14282	2021-06-04 17:42:38.0			(E)
=  Avvocati con pendenze aggiornati      : 	24639	2021-06-04 17:42:38.0		(F)
==================================================		2021-06-04 17:42:38.0
Fine XBA_BONIFICA_AVV_CON_PENDENZE. 		2021-06-04 17:42:38.0

Possibili verifiche sui dati estratti:

verificare la corrispondenza del numero di records presenti nella tabella  XBA_AVVOCATI_CON_PENDENZE con il numero (A), riportato nella tabella XBA_LOG_BONIFICA_AVVOCATI dopo l’esecuzione della procedure
SELECT count(*) FROM XBA_AVVOCATI_CON_PENDENZE

verificare la corrispondenza del numero di records presenti nella tabella  XBA_AVVOCATI_CON_PENDENZE con il numero (B) ed (F), riportati nella tabella XBA_LOG_BONIFICA_AVVOCATI dopo l’esecuzione della procedure
SELECT  count(*) FROM XBA_AVVOCATI_CON_PENDENZE WHERE ID_AVV_CERT_REGINDE IS NOT NULL

verificare la corrispondenza del numero di records presenti nella tabella  XBA_AVVOCATI_CON_PENDENZE con il numero (C), riportato nella tabella XBA_LOG_BONIFICA_AVVOCATI dopo l’esecuzione della procedure
SELECT  count(*) FROM XBA_AVVOCATI_CON_PENDENZE WHERE ID_AVV_CERT_REGINDE IS NULL

verificare la corrispondenza del numero di records presenti nella tabella  XBA_AVVOCATI_CON_PENDENZE con il numero (D), riportato nella tabella XBA_LOG_BONIFICA_AVVOCATI dopo l’esecuzione della procedure
SELECT  count(*) FROM XBA_AVVOCATI_CON_PENDENZE WHERE ID_AVV_CERT_REGINDE IS NOT NULL AND FLAG_REGINDE = 'SI'

verificare la corrispondenza del numero di records presenti nella tabella  XBA_AVVOCATI_CON_PENDENZE con il numero (E), riportato nella tabella XBA_LOG_BONIFICA_AVVOCATI dopo l’esecuzione della procedure
SELECT  count(*) FROM XBA_AVVOCATI_CON_PENDENZE WHERE ID_AVV_CERT_REGINDE IS NOT NULL AND FLAG_REGINDE = 'NO'
verificare l’aggregazione dei records XBA_AVVOCATI_CON_PENDENZE
SELECT acp.COD_FISCALE, acp.ID_AVVOCATO, acp.FLAG_REGINDE, acp.NUM_PENDENZE, acp.AMBIENTE, acp.ID_AVV_CERT_REGINDE   FROM XBA_AVVOCATI_CON_PENDENZE acp
WHERE acp.FLAG_REGINDE IS NOT NULL AND ID_AVV_CERT_REGINDE IS NOT null
ORDER BY acp.COD_FISCALE , acp.DATA_INSERIMENTO DESC, acp.ID_AVVOCATO DESC;
COD_FISCALE,	ID_AVVOCATO,	FLAG_REGINDE, NUM_PENDENZE, AMBIENTE, ID_AVV_CERT_REGINDE

BBRGLG78M17H501C	353168012017	SI	2	SIEP	353168012017
BBRGLG78M17H501C	244113012013	NO	2	SIUS	353168012017
BBRRRT64A29H501M	247492012014	SI	2	SIEP	247492012014
BBTCRL51S07H501V	223366012009	SI	1	SIEP	223366012009
BBTFBR50P30D810D	347471012016	SI	1	SIEP	347471012016
BBTFBR50P30D810D	242473012013	NO	1	SIUS	347471012016
BBTFBR50P30D810D	238034012012	NO	1	SIEP	347471012016
BBTFBR50P30D810D	234262012012	NO	2	SIEP	347471012016
BBTFBR50P30D810D	225328012010	NO	1	SIEP	347471012016

legenda: l’avvocato BBRGLG78M17H501C con id 353168012017 essendo l’ultimo inserito in ordine di tempo è deputato ad essere l’avvocato certificato ReGIndE, mentre i 2 procedimenti SIUS pendenti riferiti all’avvocato con uguale codice fiscale subiranno la modifica dell’avvocato di riferimenti da 244113012013 a 353168012017

10) Eseguire XBA_BONIFICA_AVVOCATO.prc					 - Individuazione degli avvocati SIES deputati a divenire "certificati REGINDE" in base a NOME, COGNOME, Codice Fiscale., LUOGO e DATA di NASCITA.
La procedura estrae da XBA_AVVOCATI_CON_PENDENZE i records aventi ID_AVV_CERT_REGINDE valorizzato (not null), quindi già associati con un avvocato REGINDE,
-- ordinati per ID_AVV_CERT_REGINDE e DATA_INSERIMENTO decrescenti.
-- Il cursore così individua prima le occorrenza di AVVOCATO che saranno certificati REGINDE
e subito dopo le occorrenze collegate allo stesso AVVOCATO ( aventi lo stesso ID_AVV_CERT_REGINDE ) per i quali si procederà a modificare l’AVV_ID_AVVOCATO nelle tabelle di relazione

Per gli avvocati della tabella XBA_AVVOCATI_CON_PENDENZE, certificati REGINDE  (FLAG_REGINDE = ‘SI’) saranno valorizzate le colonne FLAG_CANCELLATO = ‘N’, COD_NON_ATTIVITA = 'A', FLAG_REGINDE = ‘SI’, COD_UFFICIO_APPARTENENZA = ‘00000’, FLAG_REGINDE = ‘SI’, COD_OPERATORE_AGGIORNAMENTO = 'Update Bonifica ReGIndE', DATA_AGGIORNAMENTO = CURRENT_DATE,  mentre le colonne PEC, DESCR_COMUNE_STUDIO , COD_STATO_NASCITA_AVV, DESC_LUOGO_NAS_REGINDE saranno valorizzate con il contenuto delle corrispondenti colonne di DESC_LUOGO_NAS_REGINDE.

Per gli avvocati della tabella XBA_AVVOCATI_CON_PENDENZE, non certificati REGINDE  (FLAG_REGINDE = ‘NO’) ma con  ID_AVV_CERT_REGINDE valorizzato, saranno valorizzate le colonne FLAG_CANCELLATO = ‘S’, FLAG_REGINDE = ‘NO’, ID_AVVOCATO_BONIFICATO = ID_AVV_CERT_REGINDE, COD_OPERATORE_AGGIORNAMENTO = 'Update Bonifica ReGIndE', DATA_AGGIORNAMENTO = CURRENT_DATE.  (ID_AVVOCATO_BONIFICATO contiene il valore dell’avvocato sotto cui migrano i procedimenti pendenti).
Per ogni AVVOCATO aggiornato si procede ad aggiornare sul corrispondente record della tabella AVVOCATO_BONIF la colonna AVV_ID_AVVOCATO_NEW con il valore ID_AVV_CERT_REGINDE.

Per ogni AVVOCATO con ID_AVVOCATO_BONIFICATO valorizzato (not null)  si procede a modificare nelle tabella AVVOCATO_FASCICOLO_SIEP,  AVVOCATO_FASCICOLO_SIUS, AVVOCATO_FASCICOLO_SIGE, i records aventi AVV_ID_AVVOCATO=ID_AVVOCATO e relativi a procedimenti pendenti impostando AVV_ID_AVVOCATO = ID_AVVOCATO_BONIFICATO, per cui i procedimenti precedentemente collegati all’avvocato non certificato saranno collegati all’avvocato certificato ReGIndE (FLAG_REGINDE=’SI’).
Per i corrispondenti records delle tabelle di log AVVOCATO_FASCICOLO_SIEP_BONIF,  AVVOCATO_FASCICOLO_SIUS_BONIF, AVVOCATO_FASCICOLO_SIGE_BONIF si procede ad  aggiornare la colonna AVV_ID_AVVOCATO_NEW con il valore ID_AVVOCATO_BONIFICATO.

Per ogni AVVOCATO con ID_AVVOCATO_BONIFICATO valorizzato (not null) si procede a modificare nelle tabelle
PARTI_UDIENZA_DIFENSORE, STORICO_AVVOCATO, AVVISI_AVVOCATO, NUOVA_ISTANZA  il valore di AVV_ID_AVVOCATO impostandolo a ID_AVVOCATO_CERTIFICATO, per cui queste entità prima collegate a un avvocato non certificato saranno collegate a un avvocato certificato ReGIndE (FLAG_REGINDE=’SI’).

Per i corrispondenti records delle tabelle di log PARTI_UDIENZA_DIFENSORE_BONIF, STORICO_AVVOCATO_BONIF, AVVISI_AVVOCATO_BONIF, NUOVA_ISTANZA_BONIF  si procede ad  aggiornare la colonna AVV_ID_AVVOCATO_NEW con il valore ID_AVVOCATO_BONIFICATO.

Un esempio dei Risultati della procedure:

==================================================
Inizio XBA_BONIFICA_AVVOCATO. Individuazione degli avvocati SIES deputati a divenire certificati REGINDE.
==================================================
=  Avvocati con pendenze letti           : 	24639			(A)
=  AVVOCATI aggiornati                   : 	24639			(B)
=  Avvocati certificati REGINDE          : 	10357			(C)
=  Avvocati collegati ai referenti       : 	14282			(D)
=  AVVOCATO_FASCICOLO_SIEP aggiornati    : 	32860		(E)
=  AVVOCATO_FASCICOLO_SIUS aggiornati    : 	5346		(F)
=  AVVOCATO_FASCICOLO_SIGE aggiornati    : 	596		(G)
=  PARTI_UDIENZA_DIFENSORE aggiornati    : 	0		(H)
=  STORICO_AVVOCATO aggiornati           : 	94171		(J)
=  AVVISI_AVVOCATO aggiornati            : 	3		(K)
=  NUOVA_ISTANZA aggiornati              : 	2048			(L)
==================================================
Fine XBA_BONIFICA_AVVOCATO

Le tabelle di logs (estensione _BONIF)  prima descritte conterranno un numero di records pari a quello riportato nel riepilogo dei risultati.


Possibili verifiche sui dati estratti:

verificare la corrispondenza del numero di records presenti nella tabella  XBA_AVVOCATI_CON_PENDENZE con il numero (A), riportati nella tabella XBA_LOG_BONIFICA_AVVOCATI dopo l’esecuzione della procedure
SELECT  count(*) FROM XBA_AVVOCATI_CON_PENDENZE WHERE ID_AVV_CERT_REGINDE IS NOT NULL

verificare la corrispondenza del numero di records presenti nella tabella  AVVOCATO con il numero (B) , riportatO nella tabella XBA_LOG_BONIFICA_AVVOCATI dopo l’esecuzione della procedure
SELECT  count(*) FROM AVVOCATO a WHERE FLAG_REGINDE = 'SI' OR ID_AVVOCATO_BONIFICATO IS NOT NULL

verificare la corrispondenza del numero di records presenti nella tabella  AVVOCATO con il numero (C), riportato nella tabella XBA_LOG_BONIFICA_AVVOCATI dopo l’esecuzione della procedure
SELECT  count(*) FROM AVVOCATO a WHERE FLAG_REGINDE = 'SI'

verificare la corrispondenza del numero di records presenti nella tabella AVVOCATO con il numero (D), riportato nella tabella XBA_LOG_BONIFICA_AVVOCATI dopo l’esecuzione della procedure, che rappresenta il numero di avvocati per i quali si è proceduto all’aggiornamento dei records delle tabelle riportate nel riepilogo nei punti da (E) a (L),  sostituendo il precedete valore della colonna AVV_ID_AVVOCATO con il valore riportato nella colonna ID_AVVOCATO_BONIFICATO
SELECT  count(*) FROM AVVOCATO a WHERE ID_AVVOCATO_BONIFICATO IS NOT NULL

verificare la corrispondenza del numero di records presenti nella tabella  AVVOCATO_FASCICOLO_SIEP_BONIF con il numero (E), riportati nella tabella XBA_LOG_BONIFICA_AVVOCATI dopo l’esecuzione della procedure
SELECT  count(*) FROM AVVOCATO_FASCICOLO_SIEP_BONIF

per ciascun record della tabella è riportato nella colonna AVV_ID_AVVOCATO_NEW l’ID dell’avvocato certificato con cui sono collegati i records dopo la bonifica.
Questo numero corrisponde anche alla somma dei procedimenti SIEP pendenti (NUM_PENDENZE) e per AMBIENTE = ‘SIEP’,  degli avvocati non certificati (FLAG_REGINDE = ‘NO’) ma assimilabili ad altro avvocato certificato (ID_AVV_CERT_REGINDE valorizzato)

SELECT sum(num_pendenze) FROM XBA_AVVOCATI_CON_PENDENZE xacp WHERE ambiente = 'SIEP' AND ID_AVV_CERT_REGINDE IS NOT NULL AND FLAG_REGINDE = 'NO'

verificare la corrispondenza del numero di records presenti nella tabella  AVVOCATO_FASCICOLO_SIUS_BONIF con il numero (F), riportati nella tabella XBA_LOG_BONIFICA_AVVOCATI dopo l’esecuzione della procedure
SELECT  count(*) FROM AVVOCATO_FASCICOLO_SIUS_BONIF

per ciascun record della tabella è riportato nella colonna AVV_ID_AVVOCATO_NEW l’ID dell’avvocato certificato con cui sono collegati i records dopo la bonifica.
Questo numero corrisponde anche alla somma dei procedimenti SIEP pendenti (NUM_PENDENZE) e per AMBIENTE = ‘SIUS’,  degli avvocati non certificati (FLAG_REGINDE = ‘NO’) ma assimilabili ad altro avvocato certificato (ID_AVV_CERT_REGINDE valorizzato)

SELECT sum(num_pendenze) FROM XBA_AVVOCATI_CON_PENDENZE xacp WHERE ambiente = 'SIUS' AND ID_AVV_CERT_REGINDE IS NOT NULL AND FLAG_REGINDE = 'NO'

verificare la corrispondenza del numero di records presenti nella tabella  AVVOCATO_FASCICOLO_SIGE_BONIF con il numero (G), riportati nella tabella XBA_LOG_BONIFICA_AVVOCATI dopo l’esecuzione della procedure
SELECT  count(*) FROM AVVOCATO_FASCICOLO_SIGE_BONIF

per ciascun record della tabella è riportato nella colonna AVV_ID_AVVOCATO_NEW l’ID dell’avvocato certificato con cui sono collegati i records dopo la bonifica.
Questo numero corrisponde anche alla somma dei procedimenti SIEP pendenti (NUM_PENDENZE) e per AMBIENTE = ‘SIUS’,  degli avvocati non certificati (FLAG_REGINDE = ‘NO’) ma assimilabili ad altro avvocato certificato (ID_AVV_CERT_REGINDE valorizzato)

SELECT sum(num_pendenze) FROM XBA_AVVOCATI_CON_PENDENZE xacp WHERE ambiente = 'SIGE' AND ID_AVV_CERT_REGINDE IS NOT NULL AND FLAG_REGINDE = 'NO'


verificare la corrispondenza del numero di records presenti nella tabella  PARTI_UDIENZA_DIFENSORE_BONIF con il numero (H), riportati nella tabella XBA_LOG_BONIFICA_AVVOCATI dopo l’esecuzione della procedure
SELECT  count(*) FROM PARTI_UDIENZA_DIFENSORE_BONIF

per ciascun record della tabella è riportato nella colonna AVV_ID_AVVOCATO_NEW l’ID dell’avvocato certificato con cui sono collegati i records dopo la bonifica

verificare la corrispondenza del numero di records presenti nella tabella STORICO_AVVOCATO_BONIF con il numero (J), riportati nella tabella XBA_LOG_BONIFICA_AVVOCATI dopo l’esecuzione della procedure
SELECT  count(*) FROM STORICO_AVVOCATO_BONIF

per ciascun record della tabella è riportato nella colonna AVV_ID_AVVOCATO_NEW l’ID dell’avvocato certificato con cui sono collegati i records dopo la bonifica
verificare la corrispondenza del numero di records presenti nella tabella AVVISI_AVVOCATO_BONIF con il numero (K), riportati nella tabella XBA_LOG_BONIFICA_AVVOCATI dopo l’esecuzione della procedure
SELECT  count(*) FROM AVVISI_AVVOCATO_BONIF

per ciascun record della tabella è riportato nella colonna AVV_ID_AVVOCATO_NEW l’ID dell’avvocato certificato con cui sono collegati i records dopo la bonifica

verificare la corrispondenza del numero di records presenti nella tabella NUOVA_ISTANZA_BONIF con il numero (L), riportati nella tabella XBA_LOG_BONIFICA_AVVOCATI dopo l’esecuzione della procedure
SELECT  count(*) FROM AVVISI_AVVOCATO_BONIF

per ciascun record della tabella è riportato nella colonna AVV_ID_AVVOCATO_NEW l’ID dell’avvocato certificato con cui sono collegati i records dopo la bonifica

verificare che nella tabella AVVOCATO bonificato non vi siano records con FLAG_REGINDE = 'SI' e Codici Fiscali uguali
SELECT count(*), COD_fiscale FROM AVVOCATO a WHERE FLAG_REGINDE = 'SI' GROUP BY COD_fiscale  HAVING count(*)>1 ORDER BY 1 DESC

verificare l’aggregazione dei records AVVOCATO aggiornati
SELECT acp.COD_FISCALE, acp.ID_AVVOCATO, acp.FLAG_REGINDE, acp.ID_AVVocato_BONIFICATO   FROM AVVOCATO acp  WHERE acp.FLAG_REGINDE = 'SI' OR ID_AVVOCATO_BONIFICATO IS NOT null ORDER BY acp.COD_FISCALE , acp.DATA_INSERIMENTO DESC, acp.ID_AVVOCATO DESC;

di seguito un esempio di un sottinsieme dell’ estrazione della query

| COD_FISCALE | ID_AVVOCATO |  | ID_AVVOCATO_BONIFICATO |
| --- | --- | --- | --- |
| BBTFBR50P30D810D | 347471012016 | SI |  |
| BBTFBR50P30D810D | 242473012013 | NO | 347471012016 |
| BBTFBR50P30D810D | 238034012012 | NO | 347471012016 |
| BBTFBR50P30D810D | 234262012012 | NO | 347471012016 |
| BBTFBR50P30D810D | 225328012010 | NO | 347471012016 |


in cui l’avvocato con id 347471012016 è stato certificato ReGIndE, gli altri 4 sono quelli non certificati ma ad esso collegati. Per questi ultimi avvocati la procedura ha modificato  nelle tabelle di relazione l’AVV_ID_AVVOCATO con il valore riportato in ID_AVVOCATO_BONIFICATO

Per avere un riscontro dei procedimenti SIEP per i quali si è proceduto ad aggiornare AVVOCATO_FASCICOLO_SIEP, si possono eseguire la seguente queries:

SELECT id_avvocato_fascicolo_siep, AVV_ID_AVVOCATO, fs.chiave_anno , fs.chiave_progr , fs.cod_stato_fascicolo FROM AVVOCATO_FASCICOLO_SIEP_SXBA av, FASCICOLO_SIEP fs WHERE
avv_id_avvocato IN (347471012016, 242473012013, 238034012012, 234262012012, 225328012010)
AND fs.ID_FASCICOLO_SIEP = av.FAS_SIE_ID_FASCICOLO_SIEP  ORDER BY AVV_ID_AVVOCATO

che estraendo dalla tabella AVVOCATO_FASCICOLO_SIEP_SXBA, salvata precedentemente alla BONIFICA, fornisce l’elenco dei procedimenti collegati ai 5 avvocati

| ID_AVVOCATO_FASCICOLO_SIEP | AVV_ID_AVVOCATO | CHIAVE_ANNO | CHIAVE_PROGR | COD_STATO_FASCICOLO |
| --- | --- | --- | --- | --- |
| 170196012012 | 225328012010 | 1998 | 30462 | 3 |
| 123869012010 | 225328012010 | 2010 | 347 | 1 |
| 196520012014 | 225328012010 | 2014 | 651 | 1 |
| 175197012013 | 234262012012 | 2013 | 30028 | 3 |
| 166712012012 | 234262012012 | 2012 | 441 | 1 |
| 183170012013 | 234262012012 | 2013 | 30248 | 3 |
| 175203012013 | 234262012012 | 2013 | 20001 | 1 |
| 153127012012 | 234262012012 | 2012 | 30014 | 1 |
| 166226012012 | 238034012012 | 2012 | 90 | 3 |
| 225347012016 | 347471012016 | 2016 | 2349 | 3 |


in cui in giallo sono evidenziati i procedimenti pendenti, che sono gli unici a dover essere aggiornati

SELECT id_avvocato_fascicolo_siep, AVV_ID_AVVOCATO, fs.chiave_anno , fs.chiave_progr , fs.cod_stato_fascicolo  FROM AVVOCATO_FASCICOLO_SIEP av, FASCICOLO_SIEP fs WHERE
avv_id_avvocato IN (347471012016, 242473012013, 238034012012, 234262012012, 225328012010)
AND fs.ID_FASCICOLO_SIEP = av.FAS_SIE_ID_FASCICOLO_SIEP  ORDER BY AVV_ID_AVVOCATO

che estraendo dalla tabella AVVOCATO_FASCICOLO_SIEP, fornisce l’elenco dei procedimenti collegati ai 5 avvocati successivamente alla bonifica


| ID_AVVOCATO_FASCICOLO_SIEP | AVV_ID_AVVOCATO | CHIAVE_ANNO | CHIAVE_PROGR | COD_STATO_FASCICOLO |
| --- | --- | --- | --- | --- |
| 196520012014 | 225328012010 | 2014 | 651 | 1 |
| 123869012010 | 225328012010 | 2010 | 347 | 1 |
| 153127012012 | 234262012012 | 2012 | 30014 | 1 |
| 175203012013 | 234262012012 | 2013 | 20001 | 1 |
| 166712012012 | 234262012012 | 2012 | 441 | 1 |
| 175197012013 | 347471012016 | 2013 | 30028 | 3 |
| 225347012016 | 347471012016 | 2016 | 2349 | 3 |
| 183170012013 | 347471012016 | 2013 | 30248 | 3 |
| 166226012012 | 347471012016 | 2012 | 90 | 3 |
| 170196012012 | 347471012016 | 1998 | 30462 | 3 |


si evidenzia che i procedimenti pendenti fanno adesso riferimento all’avvocato certificato, mentre i procedimenti definiti fanno riferimento all’avvocato originario.

In maniera analoga si possono operare le verifiche su AVVOCATO_FASCICOLO_SIUS e AVVOCATO_FASCICOLO_SIGE utilizzando le seguenti queries:

SELECT id_avvocato_fascicolo_sius, AVV_ID_AVVOCATO, chiave_anno fs, chiave_progr fs, cod_stato_fascicolo fs FROM AVVOCATO_FASCICOLO_SIUS_SXBA av, FASCICOLO_SIUS fs WHERE
avv_id_avvocato IN (347471012016, 242473012013, 238034012012, 234262012012, 225328012010)
AND fs.ID_FASCICOLO_SIUS = av.FAS_SIU_ID_FASCICOLO_SIUS

SELECT id_avvocato_fascicolo_sius, AVV_ID_AVVOCATO, chiave_anno fs, chiave_progr fs, cod_stato_fascicolo fs FROM AVVOCATO_FASCICOLO_SIUS av, FASCICOLO_SIUS fs WHERE
avv_id_avvocato IN (347471012016, 242473012013, 238034012012, 234262012012, 225328012010)
AND fs.ID_FASCICOLO_SIUS = av.FAS_SIU_ID_FASCICOLO_SIUS


SELECT id_avvocato_fascicolo_sige, AVV_ID_AVVOCATO, chiave_anno fs, chiave_progr fs, cod_stato_fascicolo fs FROM AVVOCATO_FASCICOLO_SIGE_SXBA  av, FASCICOLO_SIGE fs WHERE
avv_id_avvocato IN (347471012016, 242473012013, 238034012012, 234262012012, 225328012010)
AND fs.ID_FASCICOLO_SIGE = av.FAS_SIGE_ID_FASCICOLO_SIGE

SELECT id_avvocato_fascicolo_sige, AVV_ID_AVVOCATO, chiave_anno fs, chiave_progr fs, cod_stato_fascicolo fs FROM AVVOCATO_FASCICOLO_SIGE  av, FASCICOLO_SIGE fs WHERE
avv_id_avvocato IN (347471012016, 242473012013, 238034012012, 234262012012, 225328012010)
AND fs.ID_FASCICOLO_SIGE = av.FAS_SIGE_ID_FASCICOLO_SIGE


Per individuare i sottosistemi in cui gli avvocati aggiornati dalla bonifica hanno procedimenti pendenti si può utilizzare la seguente query

SELECT acp.COD_FISCALE, acp.ID_AVVOCATO, acp.FLAG_REGINDE, acp.NUM_PENDENZE, acp.AMBIENTE, acp.ID_AVV_CERT_REGINDE   FROM XBA_AVVOCATI_CON_PENDENZE acp
WHERE acp.FLAG_REGINDE = 'SI' OR ID_AVV_CERT_REGINDE IS NOT NULL
ORDER BY acp.COD_FISCALE , acp.DATA_INSERIMENTO DESC, acp.ID_AVVOCATO DESC;


di seguito un esempio di estrazione



| COD_FISCALE | ID_AVVOCATO | FLAG_REGINDE | NUM_PENDENZE | AMBIENTE | ID_AVV_CERT_REGINDE |
| --- | --- | --- | --- | --- | --- |
| BBTFBR50P30D810D | 347471012016 | SI | 1 | SIEP | 347471012016 |
| BBTFBR50P30D810D | 242473012013 | NO | 1 | SIUS | 347471012016 |
| BBTFBR50P30D810D | 238034012012 | NO | 1 | SIEP | 347471012016 |
| BBTFBR50P30D810D | 234262012012 | NO | 2 | SIEP | 347471012016 |
| BBTFBR50P30D810D | 225328012010 | NO | 1 | SIEP | 347471012016 |
| BCCDVD67S07L182U | 219160012009 | SI | 19 | SIEP | 219160012009 |
| BCCDVD67S07L182U | 343935012016 | NO | 1 | SIEP | 219160012009 |
| BCCDVD67S07L182U | 246360012014 | NO | 3 | SIGE | 219160012009 |
| BCCDVD67S07L182U | 175438012008 | NO | 1 | SIUS | 219160012009 |



Per verificare i records delle tabelle a valle dell’AVVOCATO che sono stati modificati, accedere alle tabelle

AVVISI_AVVOCATO_BONIF, AVVOCATO_FASCICOLO_SIEP_BONIF, AVVOCATO_FASCICOLO_SIUS_BONIF, AVVOCATO_FASCICOLO_SIGE_BONIF, NUOVA_ISTANZA_BONIF, PARTI_UDIENZA_DIFENSORE_BONIF, STORICO_AVVOCATO_BONIF

in cui per ciascun records è presente nella colonna AVV_ID_AVVOCATO_NEW il valore assunto dalla colonna AVV_ID_AVVOCATO  nello stesso record sulla corrispondente tabella di esercizio.

11) XBA_RESTORE_TABELLE_AVVOCATI.prc – La procedure contiene le istruzioni per il ripristino di tutte le tabelle interessate dalla bonifica (AVVOCATO, AVVOCATO_FASCICOLO_SIEP, AVVOCATO_FASCICOLO_SIUS, AVVOCATO_FASCICOLO_SIGE, PARTI_UDIENZA_DIFENSORE, STORICO_AVVOCATO, AVVISI_AVVOCATO,  NUOVA_ISTANZA), ma può essere utilizzata anche per un ripristino parziale, commentando le istruzione delle tabelle da non ripristinare. Da utilizzare solo per il ripristino delle tabelle aggiornate, in caso di errori rilevati, che comportino un ripristino di tutte o di alcune tabelle.

12) Restore_CGREFCODES_pre_Bonifica.sql – Lo script ripristina i domini ‘FORO_AVVOCATI’ e ‘NON_ATTIVITA’ della CG_REF_CODES allo stato preesistente all’esecuzione dei punti 4 e 5 della presente procedura. Da eseguire solo in caso di ripristino.

## 3.2 Esecuzione Procedura Bonifica Difensori SIES in un unico passaggio
E’ possibile eseguire l’intera procedura con il lancio di un unico script, in tal caso procedere  come di seguito:

Aprire una shell linux sul server SIES e loggarsi come utente “root”;
Eseguire il comando: “cd /etc/init.d”;
Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”;
Fermare il processo di gestione delle code tramite il comando: “./imq stop”;

Per le attività lato DB:

Collegarsi come utente oracle sul db server;
Impostare le variabili ORACLE_HOME e ORACLE_SID (se non già settate) eseguendo le seguenti istruzioni:
(il percorso varia in base all’installazione di oracle)
export ORACLE_HOME=/u01/app/oracle/product/12.1.0/dbhome_1
(sostituire xxxxx col nome dell’istanza oracle)
export ORACLE_SID=xxxxx
Aggiungere nella variabile PATH $ORACLE_HOME/bin
Esempio: PATH=$PATH:/u01/app/oracle/product/12.1.0/dbhome_1/bin

Prima di avviare la procedura, accertarsi che sia il listener che il database siano avviati.

Copiare il file bonifica_db.zip in una qualsiasi cartella e scompattarlo. il sistema crea la cartella bonifica_db;
Creare sul server DB una cartella MEV-2019_21 (se non già esistente) sotto la directory /home/oracle/;
Copiare il contenuto della cartella bonifica_db nella cartella /home/oracle/MEV-2019_21/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella bonifica_db tramite il comando:
chmod 777 bonifica_db

In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx

Nella cartella appena creata, lanciare il comando:
./bonifica.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/MEV-2019_21/bonifica_db/log/ in cui si può constatare l’esito dell’esecuzione.
Per il risultato delle procedure di Bonifica può essere consultata la tabella XBA_LOG_BONIFICA_AVVOCATI, ordinandola per data DATA_ESECUZIONE, in cui non dovrebbe essere riportato alcun messaggio di errore.

N.B. Le segnalazioni del tipo:
ORA-00001: violata restrizione di unicità
ORA-00955: name is already used by an existing object
Cartella log già presente
ORA-04043: object does not exist
sono da considerarsi warning e non errori.

Accedere ad oracle (con qualsiasi strumento tipo toad, developer…) come utente siesxx e compilare tutte le procedure e i package che non risultano compilate.
ATTENZIONE: la procedura SUPER_SOGGETTO_PREGR e il package CARICA_RES potrebbero restare non compilate: non è da considerarsi errore.

Di seguito l’elenco dei files contenuti nella cartella sottocartella ../BONIFICA_AVVOCATI/bonifica_db/bonifica


| bonifica_db.zip | Database | Scripts/procedure per aggiornamento base dati: 
Aggiorna_AVVOCATO_FORO.sql
Aggiorna_CG_REF_CODES_NON_ATTIVITA.sql
Inserisci_CG_REF_CODES_FORO_AVVOCATI.sql
CREA_TABELLA_XBA_LOG_BONIFICA_AVVOCATI.sql
XBA_SALVA_TABELLE_AVVOCATI.prc
XBA_MODIFICA_AVVOCATO.prc
XBA_CREA_AVV_CON_PENDENZE.prc
XBA_CARICA_AVV_CON_PENDENZE.prc
XBA_BONIFICA_AVV_CON_PENDENZE.prc
XBA_BONIFICA_AVVOCATO.prc
XBA_RESTORE_TABELLE_AVVOCATI.prc
Restore_CGREFCODES_pre_Bonifica.sql |
| --- | --- | --- |