---
uniqueName: siut-sies-mg-1-0-20210730-istruzionibonificadifens
displayName: "SIUT SIES MG 1 0 20210730   Istruzioni Bonifica Difensori 021 RegInde SIES"
category: "GENERAL"
tags: []
---

# SIUT-SIES-MG-1.0-20210730 - Istruzioni_Bonifica_Difensori_021_RegInde_SIES

> **File originale:** `MEV/SCHEDA_021/Docs/consegna docx/ORIGINALS/SIUT-SIES-MG-1.0-20210730 - Istruzioni_Bonifica_Difensori_021_RegInde_SIES.docx`  
> **Tipo:** DOCX

---


Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi Direzione Generale per i Sistemi Informativi Automatizzati


Istruzioni Bonifica Difensori










Versione 1.0 del 30/07/2021





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Engineering | RTI |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 30/07/2021 |  |
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
3.2 Procedura Bonifica Difensori SIES	10
3.3 Esecuzione Procedura Bonifica Difensori SIES in un unico passaggio	13

# 1 	Introduzione
## 1.1 Scopo del documento
Il presente documento viene rilasciato con lo scopo di dettagliare le attività preliminari da eseguire prima della messa in esercizio della MEV 21 RegInde e sono relative alla bonifica dei difensori sulla base dell’estrazione degli avvocati presenti in ReGIndE, fornita dall’Amministrazione.
In particolare, nel seguente documento, si forniscono le istruzioni da seguire ed i relativi controlli da effettuare prima della messa in esercizio della MEV 21.
## 1.2 Riferimenti
| Riferimento | Nome Documento | Nome Documento |  |  | Descrizione Documento |
| --- | --- | --- | --- | --- | --- |
| RIF1. | SIUT-SIE-PR-1.0-20210730-Piano_di_rilascio_021_RegInde_SIES | SIUT-SIE-PR-1.0-20210730-Piano_di_rilascio_021_RegInde_SIES | SIUT-SIE-PR-1.0-20210730-Piano_di_rilascio_021_RegInde_SIES | SIUT-SIE-PR-1.0-20210730-Piano_di_rilascio_021_RegInde_SIES | Piano di rilascio |
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
Le attività descritte sono preliminari alle attività di installazione del software relativo alla MEV-2019_21 di SIES descritte nel documento SIUT-SIES-PR-1.0-20210730-Piano_di_Rilascio_021_RegInde_SIES.docx.
# 3 	Descrizione delle Attività
Le attività descritte nel paragrafo 3.1 si articolano su scripts.sql e procedures plsql, contenuti nel pacchetto bonifica_db.zip, che va estratto ottenendo la cartella ..\bonifica_db\bonifica.
## 3.1 Importazione tabella Avvocati ReGIndE in SIES
La prima attività da eseguire è l’importazione in SIES  della tabella Avvocati Reginde, fornita dall’Amministrazione,
tabellefisse18novembre2020.xls, contenente 388221 records. Poiché nella tabella vi sono avvocati riferite ad Enti non di interesse di SIES, righe duplicate per lo stesso Difensore, si procede prima a trattamento dei dati effettuando le seguenti operazioni:

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

che oltre a creare tutte le colonne presenti nel file di input, aggiunge anche le colonne COD_CATASTO, COD_COMUNE e COD_NAZIONE, che saranno valorizzate successivamente con procedure plsql previste all’interno della procedura di aggiornamento della tabelle COMUNE, CG_REF_CODES e CODICI_SIES_NSC (vedi SIUT-SIES-MG-1.0-20210730 - Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_SIES). La valorizzazione delle suddette 3 colonne è un prerequisito all’avvio della procedura di Bonifica Avvocati.

Poi importare i dati utilizzando uno dei tools a disposizione (Toad, pls/developer, DbEaver,…). Questa attività deve essere eseguita a livello centrale, in modo da permettere la distribuzione nei Distretti della tabella AVVOCATO_REGINDE_18112020 già precaricata.

Nella cartella di distribuzione della procedura di bonifica è presente il file AVVOCATO_REGINDE_18112020.dmp, che va semplicemente importato in SIES:
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
Creare sul server DB una cartella MEV-2019_21 sotto la directory /home/oracle/;
Copiare il contenuto della cartella bonifica_db nella cartella /home/oracle/MEV-2019_21/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella MEV-2019_21 e ricorsivamente alle sue sottocartelle tramite il comando:
chmod -R 777 MEV-2019_21
Nella cartella appena copiata (MEV-2019_21/bonifica_db/bonifica), lanciare il comando:
imp siesxx/siesxx@sies file=AVVOCATO_REGINDE_18112020.dmp log=imp.log full=y
Durante l’esecuzione verrà creato un file di log (imp.log) nella cartella /home/oracle/MEV-2019_21/bonifica_db/bonifica/ in cui si può constatare l’esito dell’esecuzione.
## 3.2 Procedura Bonifica Difensori SIES
Di seguito le attività da eseguire per la bonifica degli AVVOCATI di SIES con i dati di REGINDE.
Eseguire lo script Aggiorna_AVVOCATO_FORO.sql, modifica le attuali descrizioni di alcuni fori ('REGGIO DI CALABRIA', 'REGGIO NELL''EMILIA', 'MASSA',  'CARRARA', 'FORLI''', 'CESENA') in quelle gestite in ReGIndE(‘REGGIO CALABRIA’, 'REGGIO EMILIA', 'MASSA CARRARA', 'FORLÌ-CESENA').

Eseguire lo script Aggiorna_CG_REF_CODES_NON_ATTIVITA.sql, aggiunge nuovi Stati del Difensore (A, C ,R , S) nel dominio NON_ATTIVITA della CG_REF_CODES.

Eseguire lo script Inserisci_CG_REF_CODES_FORO_AVVOCATI.sql, effettua l’aggiornamento del dominio FORO_AVVOCATI della CG_REF_CODES eliminando i preesistenti e inserendo i nuovi records, predisposti per gestire il comune sede di un Foro svincolato dalla Descrizione e con le nuove Descrizioni di alcuni fori.

Eseguire lo script CREA_TABELLA_XBA_LOG_BONIFICA_AVVOCATI.sql Preparazione della tabella XBA_LOG_BONIFICA_AVVOCATI che conterrà i dettagli delle attività di bonifica.

5) 	Eseguire XBA_SALVA_TABELLE_AVVOCATI.prc      - Effettua il backup con lo stesso nome delle tabelle coinvolte, con l'aggiunta del suffisso _SXBA (Salvataggio per bonifica Avvocati).
Le tabelle trattate sono: AVVOCATO, AVVOCATO_FASCICOLO_SIEP, AVVOCATO_FASCICOLO_SIUS, AVVOCATO_FASCICOLO_SIGE, PARTI_UDIENZA_DIFENSORE, STORICO_AVVOCATO, AVVISI_AVVOCATO,  NUOVA_ISTANZA.
Le stesse tabelle vengono duplicate anche con l’aggiunta del suffisso _BONIF, per loggare i records che vengono aggiornati dalla procedura. Al termine dell’attività di Bonifica queste tabelle conterranno solo i records aggiornati.
6)	Eseguire XBA_MODIFICA_AVVOCATO.prc
Aggiunge di 6 colonne (PEC, 	FLAG_REGINDE, DESCR_COMUNE_STUDIO, COD_STATO_NASCITA_AVV, DESC_LUOGO_NAS_REGINDE, ID_AVVOCATO_BONIFICATO), funzionali alla bonifica Avvocati e alla nuova gestione di AVVOCATO con certificazione REGINDE. Aggiunge anche la colonna AVV_ID_AVVOCATO_NEW su tutte le tabelle di log (con estensione _BONIF).

7)	Eseguire XBA_CREA_AVV_CON_PENDENZE.prc
Preparazione della tabella XBA_AVVOCATI_CON_PENDENZE, che conterrà i dati di transito per poter eseguire la bonifica Avvocato SIES. La tabella è una immagine della tabella AVVOCATO con l’aggiunta di 3 nuove colonne AMBIENTE, NUM_PENDENZE, ID_AVV_CERT_REGINDE.

8)  Eseguire XBA_CARICA_AVV_CON_PENDENZE.prc
Caricamento dei dati degli avvocati con pendenze, incrociando le informazioni di AVVOCATO, FASCICOLO_SIEP, FASCICOLO_SIUS, FASCICOLO_SIGE, AVVOCATO_FASCICOLO_SIEP, AVVOCATO_FASCICOLO_SIUS e AVVOCATO_FASCICOLO_SIGE.
La procedura estrae gli avvocati a cui sono collegati procedimenti SIEP, SIUS e SIGE ancora pendenti.
Un procedimento SIEP si considera pendente se non archiviato (COD_STATO_FASCICOLO <> '01').
Un procedimento SIUS si considera pendente se non in stato di Definito o di Emesso Provvedimento o di unificato (COD_STATO_FASCICOLO NOT in ('01', '07', '05')).
Un procedimento SIGE si considera pendente se la data definizione non è valorizzata (DATA_DEFINIZIONE IS NULL).
Per ciascun Avvocato selezionato vengono valorizzate le colonne AMBIENTE (nome sottosistema) e NUM_PENDENZE (totale procedimenti pendenti nell’ambiente).
I records estratti vengono registrati nella tabella XBA_AVVOCATI_CON_PENDENZE.

I risultati della procedure o eventuali errori sono riportati nella tabella XBA_LOG_BONIFICA_AVVOCATI creata in precedenza, di seguito un esempio:

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

9) Eseguire XBA_BONIFICA_AVV_CON_PENDENZE.prc

Elaborazione dei dati di avvocati SIES con pendenze, incrociando e assumendo in SIES i dati di REGINDE corrispondenti agli avvocati di SIES. La procedure effettua le seguenti operazioni:
- Scansione degli Avvocati con pendenze dalla tabella XBA_AVVOCATI_CON_PENDENZE, ordinati per COD_FISCALE, DATA_INSERIMENTO e ID_AVVOCATO decrescenti, al fine di individuare prima l'occorrenza di AVVOCATO "capostipite" verso cui far confluire le altre occorrenze afferenti allo stesso AVVOCATO.
- per l’avvocato deputato a essere certificato si ricerca nella tabella AVVOCATO_REGINDE_18112020 un record avente Cognome, Nome, Foro, Codice Fiscale, Luogo e Data Nascita uguali ai corrispondenti dati dell’avvocato deputato. In caso di condizioni verificate sull’avvocato della tabella XBA_AVVOCATI_CON_PENDENZE si procede a valorizzare FLAG_REGINDE = ‘SI’, ID_AVV_CERT_REGINDE con l’id dell’avvocato corrente e le colonne DESCR_COMUNE_STUDIO, COD_STATO_NASCITA_AVV, DESC_LUOGO_NAS_REGINDE, PEC e INDIRIZZO con i valori delle corrispondenti colonne del record AVVOCATO_REGINDE_18112020-
Per i records della tabella XBA_AVVOCATI_CON_PENDENZE aventi Cognome, Nome, Foro, Codice Fiscale, Luogo e Data Nascita uguali a quelli dell’avvocato "capostipite", vengono valorizzate le colonne FLAG_REGINDE = ‘NO’,  ID_AVV_CERT_REGINDE=Id dell’avvocato capostipite.

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

Le tabelle di logs (estensione _BONIF)  prima descritte conterranno un numero di records pari a quello riportato nel riepilogo dei risultati.

11) XBA_RESTORE_TABELLE_AVVOCATI.prc - Da utilizzare solo per il ripristino delle tabelle aggiornate, in caso di errori rilevati, che comportino un ripristino di tutte o di alcune tabelle.
## 3.3 Esecuzione Procedura Bonifica Difensori SIES in un unico passaggio
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

Creare sul server DB una cartella MEV-2019_21 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/MEV-2019_21/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella MEV-2019_21 tramite il comando:
chmod 777 MEV-2019_21

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
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/MEV-2019_21/log/ in cui si può constatare l’esito dell’esecuzione.
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
XBA_BONIFICA_AVVOCATO.prc |
| --- | --- | --- |