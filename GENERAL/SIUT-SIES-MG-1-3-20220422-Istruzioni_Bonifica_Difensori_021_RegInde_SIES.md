---
uniqueName: siut-sies-mg-1-3-20220422-istruzionibonificadifens
displayName: "SIUT SIES MG 1 3 20220422 Istruzioni Bonifica Difensori 021 RegInde SIES"
category: "GENERAL"
tags: []
---

# SIUT-SIES-MG-1.3-20220422-Istruzioni_Bonifica_Difensori_021_RegInde_SIES

> **File originale:** `MEV/SCHEDA_021/Docs/consegna docx/20220422/SIUT-SIES-MG-1.3-20220422-Istruzioni_Bonifica_Difensori_021_RegInde_SIES.docx`  
> **Tipo:** DOCX

---


Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi Direzione Generale per i Sistemi Informativi Automatizzati


Istruzioni Bonifica Difensori
MEV 021_2019 RegInde










Versione 1.3 del 22/04/2022





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Engineering | RTI |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 22/04/2022 |  |
| Livello di riservatezza | L3 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 30/07/2021 | Prima emissione |  |
| 1.1 | 08/10/2021 | Seconda emissione | Rivista intera struttura documento |
| 1.2 | 24/01/2022 | Terza emissione | Rivista intera struttura documento |
| 1.3 | 22/04/2022 | Quarta emissione | Rivista intera struttura documento |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Francesco Rosati | RTI |  | Responsabile Manutenzione Correttiva
Referente Qualità e Sicurezza |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario
Referente Tecnico |
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
1.3.2 Acronimi e abbreviazioni	5
2 	Generalità	7
3 	Descrizione delle Attività	8
3.1 Istruzioni per lancio eseguibili file.sh	8
3.1.1 Attività di installazione ed esecuzione procedura batch Bonifica Difensori	8
3.2 Procedura Bonifica Difensori SIES	9
3.2.1 STEP 1	9
3.2.2 STEP 2	12
3.2.3 STEP 3	16
3.2.4 STEP 4	19
3.2.5 STEP 5	23
3.2.6 STEP 6	30
3.2.7 STEP 7	36
3.3	Procedura di Aggiornamento Tabella SIES da Tabella fissa DGSIA	38

# 1 	Introduzione
## 1.1 Scopo del documento
Il presente documento viene rilasciato con lo scopo di dettagliare le attività preliminari da eseguire prima della messa in esercizio della MEV 21 RegInde e sono relative alla bonifica dei difensori sulla base dell’estrazione degli avvocati presenti in ReGIndE, fornita dall’Amministrazione.
In particolare, nel seguente documento, si forniscono le istruzioni da seguire ed i relativi controlli da effettuare prima della messa in esercizio della MEV 21.
## 1.2 Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF1. | SIUT-SIE-PR-1.3-20220422-Piano_di_rilascio_021_RegInde_SIES | Piano di rilascio |

## 1.3 Glossario
1.3.1 Definizioni
| Definizione | Descrizione |
| --- | --- |
|  |  |

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
Le attività descritte indicano i passi necessari alla bonifica degli Avvocati e sono preliminari alle attività di installazione del software relativo alla MEV-2019_21 di SIES.

# 3 	Descrizione delle Attività
Le attività descritte nel paragrafo 3.1 si articolano su scripts .sql e procedures plsql, contenuti nel pacchetto bonifica_db.zip, che va estratto ottenendo la cartella ..\MEV-2019_21\bonifica_db\bonifica.
## 3.1 Istruzioni per lancio eseguibili file.sh
Aprire una shell linux sul server SIES e loggarsi come utente “root”;
Eseguire il comando: “cd /etc/init.d”;
Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”;
Fermare il processo di gestione delle code tramite il comando: “./imq stop”;
## 3.1.1 Attività di installazione ed esecuzione procedura batch Bonifica Difensori
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
Copiare la cartella bonifica_db nella cartella /home/oracle/MEV-2019_21/.
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella MEV-2019_21 tramite il comando:
chmod 777 MEV-2019_21

In fase di esecuzione degli script, di seguito riportati, saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx

Posizionarsi nel percorso /home/oracle/MEV-2019_21/bonifica_db/ e creare la cartella log tramite il comando mkdir log e, poi, dare i permessi tramite il comando chmod 777 log.
Posizionarsi nel percorso /home/oracle/MEV-2019_21/bonifica_db/bonifica/; lanciare il comando:
imp siesxx/siesxx@sies file=AVVOCATO_REGINDE_18112020.dmp log=/home/oracle/MEV-2019_21/bonifica_db/log/AVVOCATO_REGINDE.log FROMUSER=siespz TOUSER=siesxx
Nel file di log menzionato nel comando si potrà controllare l’esito dell’import (ovvero la creazione della tabella AVVOCATO_REGINDE_18112020 nel tablespace ‘siesxx’).
Posizionarsi nel percorso /home/oracle/MEV-2019_21/bonifica_db/; lanciare sequenzialmente i comandi, indicati nel par. 3.3.
## 3.2 Procedura Bonifica Difensori SIES
Di seguito le attività da eseguire per la bonifica degli AVVOCATI di SIES con i dati di REGINDE.
## 3.2.1 STEP 1
Verificare tramite il comando pwd di trovarsi nel percorso /home/oracle/MEV-2019_21/bonifica_db/ ed eseguire il comando

./bonifica_avv_1.sh

Dettaglio del file:
CREA_TABELLA_XBA_LOG_BONIFICA_AVVOCATI.sql = Crea tabella XBA_LOG_BONIFICA_AVVOCATI che conterrà il LOG delle successive attività.
PRE_XBA_CREA_AVV_CON_PENDENZE.prc = Crea Tabella PRE_XBA_ AVVOCATI_CON_PENDENZE che conterrà i dettagli di tutti gli avvocati aventi procedimenti SIEP, SIUS e SIGE pendenti.
PRE_XBA_CAR_AVV_CON_PENDENZE.prc = Compila ed Esegue la procedura PRE_XBA_CAR_AVV_CON_PENDENZE  per  estrarre dalla tabella AVVOCATO i records relativi ai difensori con procedimenti SIEP, SIUS e SIGE pendenti, relativi ad uffici giudiziari del Distretto, e li inserisce nella tabella PRE_XBA_ AVVOCATI_CON_PENDENZE. (La tabella può essere utilizzata per verificare la correttezza dei dati che saranno estratti dalla successiva procedure XBA_CARICA_AVV_CON_PENDENZE.prc).
Un procedimento SIEP si considera pendente se non archiviato (COD_STATO_FASCICOLO <> '01').
Un procedimento SIUS si considera pendente se non in stato di Definito o di Emesso Provvedimento o di unificato (COD_STATO_FASCICOLO NOT in ('01', '07', '05')).
Un procedimento SIGE si considera pendente se la data definizione non è valorizzata (DATA_DEFINIZIONE IS NULL).
Per ciascun Avvocato selezionato vengono valorizzate le colonne AMBIENTE (nome sottosistema) e NUM_PENDENZE (totale procedimenti pendenti nell’ambiente).

Per ogni punto precedente sono riportati di seguito gli eventuali controlli per verificare la corretta esecuzione dello step bonifica_avv_1.sh:

Verificare che nel file /home/oracle/MEV-2019_21/bonifica_db/log/LOG_Bonifica_AVV_1.log non siano riportati errori oracle;

Collegarsi al database con utenza SIESXX

Per verificare la creazione della tabella XBA_LOG_BONIFICA_AVVOCATI, effettuare la query

SELECT * FROM user_tables a WHERE a.TABLE_NAME='XBA_LOG_BONIFICA_AVVOCATI';

Prima di procedere all’esecuzione delle effettive attività di bonifica si procede ad una estrazione preventiva di tutti gli avvocati aventi procedimenti SIEP, SIUS e SIGE pendenti

L’esecuzione della procedura PRE_XBA_CREA_AVV_CON_PENDENZE.prc è tracciata nella tabella               XBA_LOG_BONIFICA_AVVOCATI: per verificare che l’elaborazione della procedura risulti completata verificare, con la seguente query, che nella tabella ci siano le righe di Inizio e Fine PRE_XBA_CREA_AVV_CON_PENDENZE.

SELECT * FROM XBA_LOG_BONIFICA_AVVOCATI ORDER BY DATA_ESECUZIONE;

Di seguito un esempio:

| Inizio PRE_XBA_CREA_AVV_CON_PENDENZE. La tabella PRE_XBA_AVVOCATI_CON_PENDENZE conterrà gli AVVOCATI con i procedimenti pendenti. |  | YYYY-MM-DD HH:MM:SS.m |
| --- | --- | --- |
| Fine PRE_XBA_CREA_AVV_CON_PENDENZE. |  | YYYY-MM-DD HH:MM:SS.m |


Accertarsi che sia presente la tabella PRE_XBA_ AVVOCATI_CON_PENDENZE con la seguente query:

SELECT * FROM USER_TABLES A WHERE A.TABLE_NAME= 'PRE_XBA_AVVOCATI_CON_PENDENZE';

La tabella strutturalmente è una immagine della tabella AVVOCATO, con l’aggiunta delle seguenti colonne:

| AMBIENTE | Nome del sottosistema di appartenenza del procedimento ( SIEP, SIUS, SIGE) |
| --- | --- |
| NUM_PENDENZE | Numero totale procedimenti pendenti a carico dell’avvocato nell’ambito del sottosistema |
| ID_AVV_CERT_REGINDE | non valorizzato |
| ID_FASCICOLO_SIEP | ID del procedimento SIEP |
| ID_FASCICOLO_SIUS | ID del procedimento SIUS |
| ID_FASCICOLO_SIGE | ID del procedimento SIGE |
| CHIAVE_ANNO | Anno del procedimento |
| CHIAVE_PROGR | Numero progressivo procedimento |
| CHIAVE_UFFICIO | Codice Ufficio di appartenenza procedimento |
| COD_STATO_FASCICOLO | Codice stato procedimento |
| COD_TIPO_UFF | Tipo ufficio appartenenza procedimento |
| DESCRCOMUNE | Descrizione ufficio appartenenza procedimento |


L’esecuzione della procedura PRE_XBA_CAR_AVV_CON_PENDENZE è tracciata nella tabella
XBA_LOG_BONIFICA_AVVOCATI: per verificare che l’elaborazione della procedura risulti completata 	verificare, con la seguente query, che nella tabella ci siano le righe di Inizio e Fine PRE_XBA_CARICA_AVV_CON_PENDENZE.

SELECT * FROM XBA_LOG_BONIFICA_AVVOCATI ORDER BY DATA_ESECUZIONE

Di seguito un esempio:
(la prima colonna non appartiene alla tabella ma serve dopo per le query di verifica)

|  | Elaborazione | Elaborati | Data_Esecuzione |
| --- | --- | --- | --- |
| (O) | Inizio PRE_XBA_CAR_AVV_CON_PENDENZE. Si estraggono gli avvocati SIES per i quali sussistono fascicoli pendenti del Distretto in almeno un sottosistema (SIEP, SIUS, SIGE). I dati estratti vengono inseriti nella tabella PRE_XBA_AVVOCATI_CON_PENDENZE.  
Il valore indica il CODICE DISTRETTO | 1 | YYYY-MM-DD HH:MM:SS.m |
|  | ============================================ |  | YYYY-MM-DD HH:MM:SS.m |
| (A) | = Totale Avvocati SIEP con pendenze : | 19925 | YYYY-MM-DD HH:MM:SS.m |
| (B) | = Totale Avvocati SIUS con pendenze : | 6136 | YYYY-MM-DD HH:MM:SS.m |
| (C) | = Totale Avvocati SIGE con pendenze : | 821 | YYYY-MM-DD HH:MM:SS.m |
| (D) | = Totale Fascicoli SIEP pendenti : | 56386 | YYYY-MM-DD HH:MM:SS.m |
| (E) | = Totale Fascicoli SIUS pendenti : | 9669 | YYYY-MM-DD HH:MM:SS.m |
| (F) | = Totale Fascicoli SIGE pendenti : | 1085 | YYYY-MM-DD HH:MM:SS.m |
|  | ============================================ |  | YYYY-MM-DD HH:MM:SS.m |
|  | Fine PRE_XBA_CAR_AVV_CON_PENDENZE. |  | YYYY-MM-DD HH:MM:SS.m |


E’ possibile verificare i suddetti numeri eseguendo nell’ordine le seguenti queries:

| (O) | SELECT SUBSTR(FASCICOLO_SIUS.ID_FASCICOLO_SIUS,-6, 2)  w_codice_distretto 
FROM FASCICOLO_SIUS
		WHERE ROWNUM = 1
        		GROUP BY SUBSTR(FASCICOLO_SIUS.ID_FASCICOLO_SIUS,-6, 2)
        	ORDER BY count(SUBSTR(FASCICOLO_SIUS.ID_FASCICOLO_SIUS,-6, 2)) DESC; |
| --- | --- |
| (A) | SELECT count(DISTINCT ID_AVVOCATO) FROM PRE_XBA_AVVOCATI_CON_PENDENZE pacp 
WHERE ambiente = 'SIEP' |
| (B) | SELECT count(DISTINCT ID_AVVOCATO) FROM PRE_XBA_AVVOCATI_CON_PENDENZE pacp 
WHERE ambiente = 'SIUS' |
| (C) | SELECT count(DISTINCT ID_AVVOCATO) FROM PRE_XBA_AVVOCATI_CON_PENDENZE pacp 
WHERE ambiente = 'SIGE' |
| (D) | SELECT count(*) FROM PRE_XBA_AVVOCATI_CON_PENDENZE pxacp WHERE AMBIENTE = 'SIEP' |
| (E) | SELECT count(*) FROM PRE_XBA_AVVOCATI_CON_PENDENZE pxacp WHERE AMBIENTE = 'SIUS' |
| (F) | SELECT count(*) FROM PRE_XBA_AVVOCATI_CON_PENDENZE pxacp WHERE AMBIENTE = 'SIGE' |


Accedendo alla tabella PRE_XBA_AVVOCATI_CON_PENDENZE è possibile selezionare, a campione, procedimenti SIEP, SIUS e SIGE e il relativo avvocato assegnatario: collegandosi, quindi, da applicativo web, è possibile verificare che i procedimenti risultino effettivamente in stato di ISCRITTO e assegnati all’avvocato indicato in tabella.
## 3.2.2 STEP 2
Verificare tramite il comando pwd di trovarsi nel percorso /home/oracle/MEV-2019_21/bonifica_db/ ed eseguire il comando

./bonifica_avv_2.sh

Dettaglio del file:
XBA_SALVA_TABELLE_AVVOCATI.prc     = Effettua il backup con lo stesso nome delle tabelle coinvolte, con l'aggiunta del suffisso _SXBA (Salvataggio per bonifica Avvocati).
Le tabelle trattate sono: AVVOCATO, AVVOCATO_FASCICOLO_SIEP, AVVOCATO_FASCICOLO_SIUS, AVVOCATO_FASCICOLO_SIGE, PARTI_UDIENZA_DIFENSORE, STORICO_AVVOCATO, AVVISI_AVVOCATO, NUOVA_ISTANZA, CG_REF_CODES.
Le stesse tabelle, ad esclusione della  CG_REF_CODES, vengono duplicate anche con l’aggiunta del suffisso _BONIF, per loggare i records che verranno aggiornati dalla procedura
Aggiorna_AVVOCATO_FORO.sql = modifica le attuali descrizioni di alcuni fori ('REGGIO DI CALABRIA', 'REGGIO NELL''EMILIA', 'MASSA',  'CARRARA', 'FORLI''', 'CESENA') in quelle gestite in ReGIndE (‘REGGIO CALABRIA’, 'REGGIO EMILIA', 'MASSA CARRARA', 'FORLÌ-CESENA').
Aggiorna_CG_REF_CODES_NON_ATTIVITA.sql = aggiunge nuovi Stati del Difensore (A, C ,R , S) nel dominio NON_ATTIVITA della CG_REF_CODES.
Inserisci_CG_REF_CODES_FORO_AVVOCATI.sql = effettua l’aggiornamento del dominio FORO_AVVOCATI della CG_REF_CODES eliminando i preesistenti e inserendo i nuovi records, predisposti per gestire il comune sede di un Foro, svincolato dalla Descrizione e con nuove Descrizioni di alcuni fori.
XBA_MODIFICA_AVVOCATO.prc   	 = Aggiunge di 6 colonne (PEC, 	FLAG_REGINDE, DESCR_COMUNE_STUDIO, COD_STATO_NASCITA_AVV, DESC_LUOGO_NAS_REGINDE, ID_AVVOCATO_BONIFICATO) alla tabella AVVOCATO: queste colonne sono funzionali alla bonifica Avvocati e alla nuova gestione di AVVOCATO con certificazione REGINDE.
Aggiunge anche la colonna AVV_ID_AVVOCATO_NEW su tutte le tabelle di log (con estensione _BONIF) create al punto 1: questa colonna conterrà l’id dell’avvocato certificato ReGIndE, con cui sarà aggiornata la colonna AVV_ID_AVVOCATO nella tabella originaria.
Per la sola tabella NUOVA_ISTANZA_BONIF, poiché nella tabella originale (NUOVA_ISTANZA) sono presenti 2 colonne riferite all’avvocato (AVV_ID_AVVOCATO e AVV_ID_AVVOCATO_PRESENTANTE) sarà aggiunta l’ulteriore colonna AVV_ID_AVVPRES_NEW oltre la già citata AVV_ID_AVVOCATO_NEW.

Al termine dell’attività di Bonifica queste tabelle con estensione _BONIF conterranno solo i records aggiornati.

Per ogni punto precedente sono riportati di seguito gli eventuali controlli per verificare la corretta esecuzione dello step bonifica_avv_2.sh:

Verificare che nel file /home/oracle/MEV-2019_21/bonifica_db/log/LOG_Bonifica_AVV_2.log non siano riportati errori oracle;

Collegarsi al database con utenza siesxx:

L’esecuzione della procedura XBA_SALVA_TABELLE_AVVOCATI.prc  è tracciata nella tabella
XBA_LOG_BONIFICA_AVVOCATI: per verificare che l’elaborazione della procedura risulti completata verificare, con la seguente query, che nella tabella ci siano le righe di Inizio e Fine XBA_SALVA_TABELLE_AVVOCATI.

SELECT * FROM XBA_LOG_BONIFICA_AVVOCATI ORDER BY DATA_ESECUZIONE

Di seguito un esempio:
| Elaborazione | Elaborati | Data_Esecuzione |
| --- | --- | --- |
| ===> Inizio XBA_SALVA_TABELLE_AVVOCATI. Salvataggio delle tabelle AVVOCATO, AVVOCATO_FASCICOLO_SIEP, AVVOCATO_FASCICOLO_SIUS, AVVOCATO_FASCICOLO_SIGE, PARTI_UDIENZA_DIFENSORE, STORICO_AVVOCATO, AVVISI_AVVOCATO, NUOVA_ISTANZA  aggiungendo il suffisso _SXBA (Salvataggio per bonifica Avvocati). |  | YYYY-MM-DD HH:MM:SS.m |
| CREATA TABELLA AVVOCATO_SXBA |  | YYYY-MM-DD HH:MM:SS.m |
| CREATA TABELLA AVVOCATO_FASCICOLO_SIEP_SXBA |  | YYYY-MM-DD HH:MM:SS.m |
| CREATA TABELLA AVVOCATO_FASCICOLO_SIUS_SXBA |  | YYYY-MM-DD HH:MM:SS.m |
| CREATA TABELLA AVVOCATO_FASCICOLO_SIGE_SXBA |  | YYYY-MM-DD HH:MM:SS.m |
| CREATA TABELLA PARTI_UDIENZA_DIFENSORE_SXBA |  | YYYY-MM-DD HH:MM:SS.m |
| CREATA TABELLA STORICO_AVVOCATO_SXBA |  | YYYY-MM-DD HH:MM:SS.m |
| CREATA TABELLA AVVISI_AVVOCATO_SXBA |  | YYYY-MM-DD HH:MM:SS.m |
| CREATA TABELLA NUOVA_ISTANZA_SXBA |  | YYYY-MM-DD HH:MM:SS.m |
| CREATA TABELLA CG_REF_CODES_SXBA |  | YYYY-MM-DD HH:MM:SS.m |
| CREATA TABELLA AVVOCATO_BONIF |  | YYYY-MM-DD HH:MM:SS.m |
| CREATA TABELLA AVVOCATO_FASCICOLO_SIEP_BONIF |  | YYYY-MM-DD HH:MM:SS.m |
| CREATA  TABELLA AVVOCATO_FASCICOLO_SIUS_BONIF |  | YYYY-MM-DD HH:MM:SS.m |
| CREATA TABELLA AVVOCATO_FASCICOLO_SIGE_BONIF |  | YYYY-MM-DD HH:MM:SS.m |
| CREATA TABELLA PARTI_UDIENZA_DIFENSORE_BONIF |  | YYYY-MM-DD HH:MM:SS.m |
| CREATA TABELLA AVVOCATO_STORICO_AVVOCATO_BONIF |  | YYYY-MM-DD HH:MM:SS.m |
| CREATA TABELLA AVVISI_AVVOCATO_BONIF |  | YYYY-MM-DD HH:MM:SS.m |
| CREATA TABELLA NUOVA_ISTANZA_BONIF |  | YYYY-MM-DD HH:MM:SS.m |
| ===> Fine XBA_SALVA_TABELLE_AVVOCATI. |  | YYYY-MM-DD HH:MM:SS.m |


E’ possibile, inoltre, verificare la presenza delle suddette tabelle con la seguenti query:

SELECT * FROM USER_TABLES A WHERE A.TABLE_NAME LIKE '%_SXBA' ORDER BY TABLE_NAME

SELECT * FROM USER_TABLES A WHERE A.TABLE_NAME LIKE '%_BONIF' ORDER BY TABLE_NAME

Per verificare l’aggiornamento effettuato al secondo punto eseguire quanto di seguito:
SELECT COUNT(*) FROM AVVOCATO_SXBA WHERE FORO IN ('REGGIO DI CALABRIA', 'REGGIO    NELL''EMILIA', 'MASSA',  'CARRARA', 'FORLI''', 'CESENA')

il risultato deve essere <> 0

SELECT COUNT(*) FROM AVVOCATO WHERE FORO IN ('REGGIO DI CALABRIA', 'REGGIO NELL''EMILIA', 'MASSA',  'CARRARA', 'FORLI''', 'CESENA')

il risultato deve essere = 0

SELECT COUNT(*) FROM AVVOCATO WHERE FORO IN ('REGGIO CALABRIA', 'REGGIO EMILIA', 'MASSA    CARRARA', 'FORLÌ-CESENA')

il risultato deve essere <> 0

Per verificare l’aggiornamento effettuato al terzo punto eseguire quanto di seguito:

SELECT * FROM CG_REF_CODES WHERE RV_DOMAIN = 'NON_ATTIVITA'

verificare che siano presenti i nuovi records con RV_LOW_VALUE = (A, C ,R , S)

Per verificare l’aggiornamento effettuato al quarto punto eseguire quanto di seguito:

SELECT * FROM CG_REF_CODES WHERE RV_DOMAIN = 'FORO_AVVOCATI'

verificare che tutti i records risultino con la colonna RV_ALT2_VALUE valorizzato, che sia
presente il foro di NAPOLI NORD

L’esecuzione della procedura XBA_MODIFICA_AVVOCATO.prc è tracciata nella tabella
XBA_LOG_BONIFICA_AVVOCATI: per verificare che l’elaborazione della procedura risulti
completata verificare, con la seguente query, che nella tabella ci siano le righe di Inizio e Fine
XBA_SALVA_TABELLE_AVVOCATI.

SELECT * FROM XBA_LOG_BONIFICA_AVVOCATI ORDER BY DATA_ESECUZIONE

Di seguito un esempio:

| Inizio XBA_MODIFICA_AVVOCATO. Aggiunta di 6 colonne (PEC, FLAG_REGINDE, DESCR_COMUNE_STUDIO, COD_STATO_NASCITA_AVV, DESC_LUOGO_NAS_REGINDE, ID_AVVOCATO_BONIFICATO), funzionali alla bonifica Avvocati e alla nuova gestione di AVVOCATO con certificazione REGINDE. |  | YYYY-MM-DD HH:MM:SS.m |
| --- | --- | --- |
| Fine XBA_MODIFICA_AVVOCATO. |  | YYYY-MM-DD HH:MM:SS.m |


Accedere alla tabella AVVOCATO e verificare che siano presenti le nuove colonne PEC, FLAG_REGINDE, DESCR_COMUNE_STUDIO, COD_STATO_NASCITA_AVV, DESC_LUOGO_NAS_REGINDE, ID_AVVOCATO_BONIFICATO

Accedere alle tabelle AVVOCATO_BONIF, AVVOCATO_FASCICOLO_SIEP_BONIF, AVVOCATO_FASCICOLO_SIUS_BONIF, AVVOCATO_FASCICOLO_SIGE_BONIF, PARTI_UDIENZA_DIFENSORE_BONIF, STORICO_AVVOCATO_BONIF, AVVISI_AVVOCATO_BONIF e verificare che sia presente la nuova colonna AVV_ID_AVVOCATO_NEW.  Accedere alla tabella NUOVA_ISTANZA_BONIF e verificare che siano presenti le nuove colonne AVV_ID_AVVOCATO_NEW e AVV_ID_AVVPRES_NEW.
## 3.2.3 STEP 3
Verificare tramite il comando pwd di trovarsi nel percorso /home/oracle/MEV-2019_21/bonifica_db/ ed eseguire il comando

./bonifica_avv_3.sh

Dettaglio del file:
XBA_CREA_AVV_CON_PENDENZE.prc = Crea la tabella XBA_AVVOCATI_CON_PENDENZE, che conterrà i dati di transito per poter eseguire la bonifica Avvocato SIES. La tabella è una immagine della tabella AVVOCATO con l’aggiunta di 3 nuove colonne AMBIENTE, NUM_PENDENZE, ID_AVV_CERT_REGINDE.
XBA_CARICA_AVV_CON_PENDENZE.prc = Compila ed Esegue la procedura XBA_CARICA_AVV_CON_PENDENZE . La procedura ricerca il codice del Distretto su cui viene eseguita, in base al raggruppamento per ordine decrescente dei records FASCICOLO_SIUS, sulla base del sestultimo e quintultimo carattere della colonna ID_FASCICOLO_SIUS.
La procedura estrae gli avvocati a cui sono collegati procedimenti SIEP, SIUS e SIGE ancora pendenti, appartenenti a uffici del Distretto.
Un procedimento SIEP si considera pendente se non archiviato (COD_STATO_FASCICOLO <> '01').
Un procedimento SIUS si considera pendente se non in stato di Definito o di Emesso Provvedimento o di unificato (COD_STATO_FASCICOLO NOT in ('01', '07', '05')).
Un procedimento SIGE si considera pendente se la data definizione non è valorizzata (DATA_DEFINIZIONE IS NULL).
Per ciascun Avvocato selezionato vengono valorizzate le colonne AMBIENTE (nome sottosistema) e NUM_PENDENZE (totale procedimenti pendenti nell’ambiente).
I records estratti vengono registrati nella tabella XBA_AVVOCATI_CON_PENDENZE.



Per ogni punto precedente sono riportati di seguito gli eventuali controlli per verificare la corretta esecuzione dello step bonifica_avv_3.sh:

Verificare che nel file /home/oracle/MEV-2019_21/bonifica_db/log/LOG_Bonifica_AVV_3.log non siano riportati errori oracle;

Collegarsi al database con utenza SIESXX

Prima di procedere all’esecuzione delle effettive attività di bonifica si procede ad una estrazione
preventiva di tutti gli avvocati aventi procedimenti SIEP, SIUS e SIGE pendenti

L’esecuzione della procedura XBA_CREA_AVV_CON_PENDENZE.prc è tracciata nella tabella               XBA_LOG_BONIFICA_AVVOCATI: per verificare che l’elaborazione della procedura risulti completata verificare, con la seguente query, che nella tabella ci siano le righe di Inizio e Fine PRE_XBA_CREA_AVV_CON_PENDENZE.

SELECT * FROM XBA_LOG_BONIFICA_AVVOCATI ORDER BY DATA_ESECUZIONE;

Di seguito un esempio:

| Inizio XBA_CREA_AVV_CON_PENDENZE. La tabella XBA_AVVOCATI_CON_PENDENZE conterrà i dati di transito per eseguire la bonifica AVVOCATO. |  | YYYY-MM-DD HH:MM:SS.m |
| --- | --- | --- |
| Fine XBA_CREA_AVV_CON_PENDENZE. |  | YYYY-MM-DD HH:MM:SS.m |


Accertarsi che sia presente la tabella XBA_ AVVOCATI_CON_PENDENZE con la seguente query:

SELECT * FROM USER_TABLES A WHERE A.TABLE_NAME='XBA_AVVOCATI_CON_PENDENZE'

La tabella strutturalmente è una immagine della tabella AVVOCATO, con l’aggiunta delle seguenti
colonne:

| AMBIENTE | Nome del sottosistema di appartenenza del procedimento ( SIEP, SIUS, SIGE) |
| --- | --- |
| NUM_PENDENZE | Numero totale proc. pendenti a carico dell’avvocato nell’ambito del sottosistema |
| ID_AVV_CERT_REGINDE | non valorizzato |


L’esecuzione della procedura XBA_CARICA_AVV_CON_PENDENZE è tracciata nella tabella
XBA_LOG_BONIFICA_AVVOCATI: per verificare che l’elaborazione della procedura risulti completata verificare, con la seguente query, che nella tabella ci siano le righe di Inizio e Fine XBA_CARICA_AVV_CON_PENDENZE.

SELECT * FROM XBA_LOG_BONIFICA_AVVOCATI ORDER BY DATA_ESECUZIONE

Di seguito un esempio:
(la prima colonna non appartiene alla tabella ma serve dopo per le query di verifica)

|  | Elaborazione | Elaborati | Data_Esecuzione |
| --- | --- | --- | --- |
| (O) | Inizio XBA_CARICA_AVV_CON_PENDENZE. Si estraggono gli avvocati SIES per i quali sussistono fascicoli pendenti del Distretto in almeno un sottosistema (SIEP, SIUS, SIGE). I dati estratti vengono inseriti nella tabella XBA_AVVOCATI_CON_PENDENZE.  
Il valore indica il CODICE DISTRETTO | 1 | YYYY-MM-DD HH:MM:SS.m |
|  | ============================================ |  | YYYY-MM-DD HH:MM:SS.m |
| (A) | = Totale Avvocati SIEP con pendenze : | 19925 | YYYY-MM-DD HH:MM:SS.m |
| (B) | = Totale Avvocati SIUS con pendenze : | 6136 | YYYY-MM-DD HH:MM:SS.m |
| (C) | = Totale Avvocati SIGE con pendenze : | 821 | YYYY-MM-DD HH:MM:SS.m |
| (D) | = Totale Fascicoli SIEP pendenti : | 56386 | YYYY-MM-DD HH:MM:SS.m |
| (E) | = Totale Fascicoli SIUS pendenti : | 9669 | YYYY-MM-DD HH:MM:SS.m |
| (F) | = Totale Fascicoli SIGE pendenti : | 1085 | YYYY-MM-DD HH:MM:SS.m |
|  | ============================================ |  | YYYY-MM-DD HH:MM:SS.m |
|  | Fine XBA_CARICA_AVV_CON_PENDENZE. |  | YYYY-MM-DD HH:MM:SS.m |


E’ possibile effettuare le seguenti verifiche sui suddetti numeri eseguendo nell’ordine le seguenti
queries:

| (O) | SELECT SUBSTR(FASCICOLO_SIUS.ID_FASCICOLO_SIUS,-6, 2)  w_codice_distretto 
FROM FASCICOLO_SIUS
		WHERE ROWNUM = 1
        		GROUP BY SUBSTR(FASCICOLO_SIUS.ID_FASCICOLO_SIUS,-6, 2)
        	ORDER BY count(SUBSTR(FASCICOLO_SIUS.ID_FASCICOLO_SIUS,-6, 2)) DESC; |
| --- | --- |
| (A) | SELECT count(*) FROM XBA_AVVOCATI_CON_PENDENZE xacp WHERE ambiente = 'SIEP' |
| (B) | SELECT count(*) FROM XBA_AVVOCATI_CON_PENDENZE xacp WHERE ambiente = 'SIUS' |
| (C) | SELECT count(*) FROM XBA_AVVOCATI_CON_PENDENZE xacp WHERE ambiente = 'SIGE' |
| (D) | SELECT SUM(NUM_PENDENZE) FROM XBA_AVVOCATI_CON_PENDENZE xacp WHERE ambiente = 'SIEP' |
| (E) | SELECT SUM(NUM_PENDENZE) FROM XBA_AVVOCATI_CON_PENDENZE xacp WHERE ambiente='SIUS' |
| (F) | SELECT SUM(NUM_PENDENZE) FROM XBA_AVVOCATI_CON_PENDENZE xacp WHERE ambiente = 'SIGE' |


E’ possibile inoltre verificare la corrispondenza dei numeri riportati nella tabella con quelli riportati nell’analoga tabella riportata allo STEP1 – punto3 delle verifiche (PRE_XBA_CAR_AVV_CON_PENDENZE.prc)

Accedendo alla tabella XBA_AVVOCATI_CON_PENDENZE, eseguendo la query

SELECT ID_AVVOCATO, COD_FISCALE, AMBIENTE, NUM_PENDENZE  FROM XBA_AVVOCATI_CON_PENDENZE ORDER BY COD_FISCALE, AMBIENTE

è possibile selezionare, a campione, un avvocato, anche con più occorrenze, annotarsi Codice Fiscale, il numero di pendenze (valore NUM_PENDENZE) per ciascun AMBIENTE e verificare che nella tabella PRE_XBA_AVVOCATI_CON_PENDENZE, eseguendo la seguente query (in cui va sostituito il parametro 'valore codice fiscale' con il codice fiscale annotato)

SELECT * FROM PRE_XBA_AVVOCATI_CON_PENDENZE WHERE COD_FISCALE = 'valore codice fiscale'  ORDER BY AMBIENTE

siano presenti un numero di records (Procedimenti pendenti) corrispondenti al numero riportato in NUM_PENDENZE della tabella XBA_AVVOCATI_CON_PENDENZE.
## 3.2.4 STEP 4
Verificare tramite il comando pwd di trovarsi nel percorso /home/oracle/MEV-2019_21/bonifica_db/ ed eseguire il comando

./bonifica_avv_4.sh

Dettaglio del file:
XBA_BONIFICA_AVV_CON_PENDENZE.prc    = Compila ed esegue la procedure XBA_BONIFICA_AVV_CON_PENDENZE. La procedure elabora i dati dei records della tabella XBA_AVVOCATI_CON_PENDENZE, incrociandoli con i dati di REGINDE presenti nella tabella AVVOCATO_REGINDE_18112020. La procedure effettua le seguenti operazioni:
- Scansione degli Avvocati con pendenze dalla tabella XBA_AVVOCATI_CON_PENDENZE, ordinati per COD_FISCALE, DATA_INSERIMENTO e ID_AVVOCATO decrescenti, al fine di individuare prima l'occorrenza di AVVOCATO "capostipite" verso cui far confluire le altre occorrenze afferenti allo stesso AVVOCATO.
- per l’avvocato deputato a essere certificato si ricerca nella tabella AVVOCATO_REGINDE_18112020 un record avente Cognome, Nome, Foro, Codice Fiscale, Luogo e Data Nascita uguali ai corrispondenti dati dell’avvocato deputato. In caso di condizioni verificate, sull’avvocato della tabella XBA_AVVOCATI_CON_PENDENZE si procede a valorizzare FLAG_REGINDE = ‘SI’, ID_AVV_CERT_REGINDE con l’id dell’avvocato corrente e le colonne DESCR_COMUNE_STUDIO, COD_STATO_NASCITA_AVV, DESC_LUOGO_NAS_REGINDE, PEC e INDIRIZZO con i valori delle corrispondenti colonne del record AVVOCATO_REGINDE_18112020;
- per i records della tabella XBA_AVVOCATI_CON_PENDENZE aventi Cognome, Nome, Foro, Codice Fiscale, Luogo e Data Nascita uguali a quelli dell’avvocato "capostipite", vengono valorizzate le colonne FLAG_REGINDE = ‘NO’,  ID_AVV_CERT_REGINDE=Id dell’avvocato capostipite;
- i records della tabella XBA_AVVOCATI_CON_PENDENZE non aventi Cognome, Nome, Foro, Codice Fiscale, Luogo e Data Nascita uguali a quelli dell’avvocato "capostipite" oppure non presenti in AVVOCATO_REGINDE_18112020 restano con le colonne FLAG_REGINDE = ‘NO’,  ID_AVV_CERT_REGINDE non valorizzato;
XBA_VERIF_AVV_CERTIFICABILI.sql    = Crea una Vista XBA_VERIF_AVV_CERTIFICABILI che permette di verificare la corretta individuazione degli avvocati certificati ReGIndE (FLAG_REGINDE = ‘SI’), di quelli non certificati ma associabili ad altro avvocato certificato (FLAG_REGINDE = ‘NO’, ma ID_AVVOCATO_CERT valorizzato) e quelli non certificabili perché assenti in ReGIndE (FLAG_REGINDE = ‘NO’, ID_AVVOCATO_CERT non valorizzato e COGNOME_RI non valorizzato) oppure con dati differenti di almeno 1 dei campi Cognome, Nome, Foro, Luogo e Data Nascita (FLAG_REGINDE = ‘NO’, ID_AVVOCATO_CERT non valorizzato). La vista per ogni Avvocato, presente nella tabella XBA_AVVOCATI_CON_PENDENZE, ricerca nella tabella AVVOCATI_REGINDE_18112020 avente Codice Fiscale uguale.
La vista è costituita dalle seguenti colonne:

| COGNOME_RI | Cognome Avvocato ReGIndE |
| --- | --- |
| NOME_RI | Nome Avvocato ReGIndE |
| COD_FISCALE_RI | Codice Fiscale ReGIndE |
| FORO_RI | Foro ReGIndE |
| COD_COMUNE_RI | Codice Comune Nascita ReGIndE |
| DATA_NASCITA_RI | Data Nascita ReGIndE |
| ID_AVVOCATO | Id_Avvocato SIES |
| COGNOME_SIES | Cognome Avvocato SIES |
| NOME_SIES | Nome Avvocato SIES |
| COD_FISCALE_SIES | Codice Fiscale SIES |
| FORO_SIES | Foro SIES |
| COD_COMUNE_SIES | Codice Comune Nascita SIES |
| DATA_NASCITA_SIES | Data Nascita SIES |
| FLAG_REGINDE | SI = certificato ReGIndE; ‘NO’ = non certificato |
| ID_AVVOCATO_CERT | Id_Avvocato dell’Avvocato certificato a cui risulta associato
Null se avvocato non associabile o inesistente in ReGIndE |



Per ogni punto precedente sono riportati di seguito gli eventuali controlli per verificare la corretta esecuzione dello step bonifica_avv_4.sh:

Verificare che nel file /home/oracle/MEV-2019_21/bonifica_db/log/LOG_Bonifica_AVV_4.log non siano riportati errori oracle;

Collegarsi al database con utenza SIESXX

L’esecuzione della procedura XBA_BONIFICA_AVV_CON_PENDENZE è tracciata nella tabella
XBA_LOG_BONIFICA_AVVOCATI: per verificare che l’elaborazione della procedura risulti completata 	verificare, con la seguente query, che nella tabella ci siano le righe di Inizio e Fine XBA_BONIFICA_AVV_CON_PENDENZE.

Select * from XBA_LOG_BONIFICA_AVVOCATI order by data_esecuzione

Di seguito un esempio:
(la prima colonna non appartiene alla tabella ma serve dopo per le query di verifica)

|  | Elaborazione | Elaborati | Data_Esecuzione |
| --- | --- | --- | --- |
|  | Inizio XBA_BONIFICA_AVV_CON_PENDENZE. Scansione degli Avvocati con pendenze ordinati per COD_FISCALE, DATA_INSERIMENTO e ID_AVVOCATO decrescenti; si individua così prima l AVVOCATO principale. |  | YYYY-MM-DD HH:MM:SS.m |
|  | ============================================ |  | YYYY-MM-DD HH:MM:SS.m |
| (A) | =  Totale Avvocati con pendenze          : | 26882 | YYYY-MM-DD HH:MM:SS.m |
| (B) | =  Avvocati presenti in REGINDE          : | 16580 | YYYY-MM-DD HH:MM:SS.m |
| (C) | =  Avvocati assenti in REGINDE           : | 10302 | YYYY-MM-DD HH:MM:SS.m |
| (D) | =  Avvocati certificati REGINDE          : | 7232 | YYYY-MM-DD HH:MM:SS.m |
| (E) | =  Avvocati collegati                    : | 9348 | YYYY-MM-DD HH:MM:SS.m |
| (F) | =  Avvocati con pendenze aggiornati      : | 16580 | YYYY-MM-DD HH:MM:SS.m |
|  | ============================================ |  | YYYY-MM-DD HH:MM:SS.m |
|  | Fine XBA_BONIFICA_AVV_CON_PENDENZE. |  | YYYY-MM-DD HH:MM:SS.m |


E’ possibile effettuare le seguenti verifiche sui suddetti numeri eseguendo nell’ordine le seguenti queries:

| (A) | SELECT count(*) FROM XBA_AVVOCATI_CON_PENDENZE |
| --- | --- |
| (B) | SELECT  count(*) FROM XBA_AVVOCATI_CON_PENDENZE WHERE ID_AVV_CERT_REGINDE IS NOT NULL |
| (C) | SELECT  count(*) FROM XBA_AVVOCATI_CON_PENDENZE WHERE ID_AVV_CERT_REGINDE IS NULL |
| (D) | SELECT  count(*) FROM XBA_AVVOCATI_CON_PENDENZE WHERE ID_AVV_CERT_REGINDE IS NOT NULL AND FLAG_REGINDE = 'SI' |
| (E) | SELECT  count(*) FROM XBA_AVVOCATI_CON_PENDENZE WHERE ID_AVV_CERT_REGINDE IS NOT NULL AND FLAG_REGINDE = 'NO' |
| (F) | SOMMA di (D) + (E) |


Per verificare la corretta individuazione degli avvocati certificati ReGIndE   e di quelli non certificati è possibile accedere alla vista, eseguendo le seguente query:
SELECT count(*) FROM XBA_VERIF_AVV_CERTIFICABILI     fornisce il numero degli avvocati presenti nella vista, deve essere uguale al numero (A) riportato nella tabella di cui al precedente punto

SELECT count(*) FROM XBA_VERIF_AVV_CERTIFICABILI WHERE FLAG_REGINDE = 'SI'   fornisce il numero degli avvocati certificati ReGIndE presenti nella vista,  deve essere uguale al numero (D) riportato nella tabella di cui al precedente punto

SELECT count(*) FROM XBA_VERIF_AVV_CERTIFICABILI WHERE FLAG_REGINDE = 'NO' AND ID_AVVOCATO_CERT IS NOT NULL	fornisce il numero degli avvocati non certificati ReGIndE, ma collegati ad altri con uguali dati anagrafici certificati, deve essere uguale al numero (E) riportato nella tabella di cui al precedente punto

SELECT count(*) FROM XBA_VERIF_AVV_CERTIFICABILI  WHERE COGNOME_RI IS NULL 	fornisce il numero degli avvocati non certificabili perché assenti in ReGIndE

SELECT count(*) FROM XBA_VERIF_AVV_CERTIFICABILI WHERE FLAG_REGINDE = 'NO' AND ID_AVVOCATO_CERT IS NULL AND COGNOME_RI IS NOT NULL		fornisce il numero degli avvocati non certificabili a causa di differenze dei dati anagrafici presenti in ReGIndE rispetto a quelli di SIES.  La somma dei numeri forniti da queste ultime 2 query deve essere uguale al numero (C) riportato nella tabella di cui al precedente punto

E’ possibile accedere ai dati della vista, eseguendo la query

Select * FROM XBA_VERIF_AVV_CERTIFICABILI 		individuare a campione un avvocato certificato ReGIndE (FLAG_REGINDE = ‘SI’), a cui risultano collegati altri avvocati non certificati (FLAG_REGINDE = ‘NO’, ID_AVVOCATO_CERT uguale a quello dell’avvocato certificato) e annotarsi il codice fiscale (es. BBTFBR50P30D810D)

eseguire la successiva query, sostituendo il codice fiscale con quello selezionato in precedenza

SELECT * FROM XBA_AVVOCATI_CON_PENDENZE WHERE COD_FISCALE = 'BBTFBR50P30D810D' ORDER BY FLAG_REGINDE DESC, DATA_INSERIMENTO DESC

verificare che l’avvocato certificato, individuato come riferimento di tutti gli altri, sia effettivamente l’ultimo inserito in ordine di tempo (valore DATA_INSERIMENTO) e a parità di data quello con ID_AVVOCATO più recente
## 3.2.5 STEP 5
Verificare tramite il comando pwd di trovarsi nel percorso /home/oracle/MEV-2019_21/bonifica_db/ ed eseguire il comando

./bonifica_avv_5.sh

Dettaglio del file:
XBA_BONIFICA_AVVOCATO.prc = Compila ed esegue la procedure XBA_BONIFICA_AVVOCATO. La procedure in base alla catalogazione degli Avvocati, effettuata con la precedente procedure, in avvocati certificati ReGIndE, avvocati non certificati ma associabili a quelli certificabili e avvocati non certificati e non associabili procede all’aggiornamento della tabella AVVOCATO e delle tabelle ad essa collegate.

La procedura estrae da XBA_AVVOCATI_CON_PENDENZE i records aventi ID_AVV_CERT_REGINDE valorizzato (not null), quindi già associati con un avvocato REGINDE,
-- ordinati per ID_AVV_CERT_REGINDE, FLAG_REGINDE e DATA_INSERIMENTO decrescenti.
-- Il cursore così individua prima le occorrenza di AVVOCATO che saranno certificati REGINDE
e subito dopo le occorrenze collegate allo stesso AVVOCATO ( aventi lo stesso ID_AVV_CERT_REGINDE ) per i quali si procederà a modificare l’AVV_ID_AVVOCATO nelle tabelle di relazione.

Per gli avvocati della tabella XBA_AVVOCATI_CON_PENDENZE, certificati REGINDE  (FLAG_REGINDE = ‘SI’) saranno valorizzate le colonne FLAG_CANCELLATO = ‘N’, COD_NON_ATTIVITA = 'A', FLAG_REGINDE = ‘SI’, COD_UFFICIO_APPARTENENZA = ‘00000’, FLAG_REGINDE = ‘SI’, COD_OPERATORE_AGGIORNAMENTO = 'Update Bonifica ReGIndE', DATA_AGGIORNAMENTO = CURRENT_DATE,  mentre le colonne PEC, DESCR_COMUNE_STUDIO , COD_STATO_NASCITA_AVV, DESC_LUOGO_NAS_REGINDE saranno valorizzate con il contenuto delle corrispondenti colonne di XBA_AVVOCATI_CON_PENDENZE.

Per gli avvocati della tabella XBA_AVVOCATI_CON_PENDENZE, non certificati REGINDE  (FLAG_REGINDE = ‘NO’) ma con  ID_AVV_CERT_REGINDE valorizzato, saranno valorizzate le colonne FLAG_CANCELLATO = ‘S’, FLAG_REGINDE = ‘NO’, ID_AVVOCATO_BONIFICATO = ID_AVV_CERT_REGINDE, COD_OPERATORE_AGGIORNAMENTO = 'Update Bonifica ReGIndE', DATA_AGGIORNAMENTO = CURRENT_DATE.  (ID_AVVOCATO_BONIFICATO contiene il valore dell’avvocato sotto cui migrano i procedimenti pendenti).
Per ogni AVVOCATO aggiornato si procede ad aggiornare sul corrispondente record della tabella AVVOCATO_BONIF la colonna AVV_ID_AVVOCATO_NEW con il valore ID_AVV_CERT_REGINDE.
Nessuna attività viene effettuata per i records della tabella XBA_AVVOCATI_CON_PENDENZE, aventi ID_AVV_CERT_REGINDE non valorizzato.

Per ogni AVVOCATO con ID_AVVOCATO_BONIFICATO valorizzato (not null)  si procede a modificare nelle tabelle AVVOCATO_FASCICOLO_SIEP,  AVVOCATO_FASCICOLO_SIUS, AVVOCATO_FASCICOLO_SIGE, i records aventi AVV_ID_AVVOCATO=ID_AVVOCATO e relativi a procedimenti pendenti impostando AVV_ID_AVVOCATO = ID_AVVOCATO_BONIFICATO, per cui i procedimenti precedentemente collegati all’avvocato non certificato saranno collegati all’avvocato certificato ReGIndE (FLAG_REGINDE=’SI’).
Per i corrispondenti records delle tabelle di log AVVOCATO_FASCICOLO_SIEP_BONIF,  AVVOCATO_FASCICOLO_SIUS_BONIF, AVVOCATO_FASCICOLO_SIGE_BONIF si procede ad  aggiornare la colonna AVV_ID_AVVOCATO_NEW con il valore ID_AVVOCATO_BONIFICATO.

Per ogni AVVOCATO con ID_AVVOCATO_BONIFICATO valorizzato (not null) si procede a modificare nelle tabelle PARTI_UDIENZA_DIFENSORE, STORICO_AVVOCATO, AVVISI_AVVOCATO il valore di AVV_ID_AVVOCATO impostandolo a ID_AVVOCATO_ BONIFICATO, per cui queste entità prima collegate a un avvocato non certificato saranno collegate a un avvocato certificato ReGIndE (FLAG_REGINDE=’SI’).

Per ogni AVVOCATO con ID_AVVOCATO_BONIFICATO valorizzato (not null) si procede a modificare nella tabella NUOVA_ISTANZA,  aventi AVV_ID_AVVOCATO = ID_AVVOCATO, il valore di AVV_ID_AVVOCATO impostandolo a ID_AVVOCATO_ BONIFICATO, analogamente si procederà per i records aventi AVV_ID_AVVOCATO_PRESENTANTE = ID_AVVOCATO, per cui queste entità prima collegate a un avvocato non certificato saranno collegate a un avvocato certificato ReGIndE (FLAG_REGINDE=’SI’).

Per i corrispondenti records delle tabelle di log PARTI_UDIENZA_DIFENSORE_BONIF, STORICO_AVVOCATO_BONIF, AVVISI_AVVOCATO_BONIF si procede ad  aggiornare la colonna AVV_ID_AVVOCATO_NEW con il valore ID_AVVOCATO_BONIFICATO.
Per i corrispondenti records della tabella di log NUOVA_ISTANZA_BONIF  si procede ad  aggiornare le colonne AVV_ID_AVVOCATO_NEW  e/o AVV_ID_AVVPRES_NEW con il valore ID_AVVOCATO_BONIFICATO.
POST_XBA_CREA_AVV_CON_PENDENZE.prc = Crea Tabella POST_XBA_ AVVOCATI_CON_PENDENZE
che conterrà i dettagli di tutti gli avvocati aventi procedimenti SIEP, SIUS e SIGE pendenti dopo la bonifica ed è finalizzata a permettere di verificarne la corretta esecuzione.
POST_XBA_CAR_AVV_CON_PENDENZE.prc = Compila ed esegue la procedure POST_XBA_CAR_AVV_CON_PENDENZE  per  estrarre dalla tabella AVVOCATO, bonificata, i records relativi ai difensori con procedimenti SIEP, SIUS e SIGE pendenti, relativi ad uffici giudiziari del Distretto, e li inserisce nella tabella POST_XBA_ AVVOCATI_CON_PENDENZE.
Per ogni punto precedente sono riportati di seguito gli eventuali controlli per verificare la corretta esecuzione dello step bonifica_avv_5.sh:

Verificare che nel file /home/oracle/MEV-2019_21/bonifica_db/log/LOG_Bonifica_AVV_5.log non siano riportati errori oracle;

Collegarsi al database con utenza SIESXX

L’esecuzione della procedura XBA_BONIFICA_AVVOCATO è tracciata nella tabella
XBA_LOG_BONIFICA_AVVOCATI: per verificare che l’elaborazione della procedura risulti completata 	verificare, con la seguente query, che nella tabella ci siano le righe di Inizio e Fine XBA_BONIFICA_AVVOCATO.

SELECT * FROM XBA_LOG_BONIFICA_AVVOCATI ORDER BY DATA_ESECUZIONE

Di seguito un esempio:
(la prima colonna non appartiene alla tabella ma serve dopo per le query di verifica)

|  | Elaborazione | Elaborati | Data_Esecuzione |
| --- | --- | --- | --- |
| (O) | Inizio XBA_BONIFICA_AVVOCATO. Aggiornamento degli avvocati SIES certificati REGINDE e di quelli ad essi associabili. Il valore indica il Codice Distretto | 1 | YYYY-MM-DD HH:MM:SS.m |
|  | ============================================ |  | YYYY-MM-DD HH:MM:SS.m |
| (A) | =  Avvocati con pendenze letti           : | 16580 | YYYY-MM-DD HH:MM:SS.m |
| (B) | =  AVVOCATI aggiornati                   : | 16580 | YYYY-MM-DD HH:MM:SS.m |
| (C) | =  Avvocati certificati REGINDE          : | 7232 | YYYY-MM-DD HH:MM:SS.m |
| (D) | =  Avvocati collegati ai referenti       : | 9348 | YYYY-MM-DD HH:MM:SS.m |
| (E) | =  AVVOCATO_FASCICOLO_SIEP aggiornati    : | 25787 | YYYY-MM-DD HH:MM:SS.m |
| (F) | =  AVVOCATO_FASCICOLO_SIUS aggiornati    : | 4896 | YYYY-MM-DD HH:MM:SS.m |
| (G) | =  AVVOCATO_FASCICOLO_SIGE aggiornati    : | 550 | YYYY-MM-DD HH:MM:SS.m |
| (H) | =  PARTI_UDIENZA_DIFENSORE aggiornati    : | 151 | YYYY-MM-DD HH:MM:SS.m |
| (J) | =  STORICO_AVVOCATO aggiornati           : | 90936 | YYYY-MM-DD HH:MM:SS.m |
| (K) | =  AVVISI_AVVOCATO aggiornati            : | 3 | YYYY-MM-DD HH:MM:SS.m |
| (L) | =  NUOVA_ISTANZA aggiornati              : | 19146 | YYYY-MM-DD HH:MM:SS.m |
|  | ============================================ |  |  |
|  | Fine XBA_BONIFICA_AVVOCATO |  |  |


E’ possibile effettuare le seguenti verifiche sui suddetti numeri eseguendo nell’ordine le seguenti queries:

| (O) | SELECT SUBSTR(FASCICOLO_SIUS.ID_FASCICOLO_SIUS,-6, 2)  w_codice_distretto 
FROM FASCICOLO_SIUS
		WHERE ROWNUM = 1
        		GROUP BY SUBSTR(FASCICOLO_SIUS.ID_FASCICOLO_SIUS,-6, 2)
        	ORDER BY count(SUBSTR(FASCICOLO_SIUS.ID_FASCICOLO_SIUS,-6, 2)) DESC; |
| --- | --- |
| (A) | SELECT  count(*) FROM XBA_AVVOCATI_CON_PENDENZE WHERE ID_AVV_CERT_REGINDE IS NOT NULL |
| (B) | SELECT  count(*) FROM AVVOCATO a WHERE FLAG_REGINDE = 'SI' OR ID_AVVOCATO_BONIFICATO IS NOT NULL |
| (C) | SELECT  count(*) FROM AVVOCATO a WHERE FLAG_REGINDE = 'SI' |
| (D) | SELECT  count(*) FROM XBA_AVVOCATI_CON_PENDENZE WHERE ID_AVV_CERT_REGINDE IS NOT NULL AND FLAG_REGINDE = 'SI' |
| (E) | SELECT  count(*) FROM AVVOCATO_FASCICOLO_SIEP_BONIF           oppure
SELECT sum(num_pendenze) FROM XBA_AVVOCATI_CON_PENDENZE xacp WHERE ambiente = 'SIEP' AND ID_AVV_CERT_REGINDE IS NOT NULL AND FLAG_REGINDE = 'NO' |
| (F) | SELECT  count(*) FROM AVVOCATO_FASCICOLO_SIUS_BONIF         oppure
SELECT sum(num_pendenze) FROM XBA_AVVOCATI_CON_PENDENZE xacp WHERE ambiente = 'SIUS' AND ID_AVV_CERT_REGINDE IS NOT NULL AND FLAG_REGINDE = 'NO' |
| (G) | SELECT  count(*) FROM AVVOCATO_FASCICOLO_SIGE_BONIF   oppure
SELECT sum(num_pendenze) FROM XBA_AVVOCATI_CON_PENDENZE xacp WHERE ambiente = 'SIGE' AND ID_AVV_CERT_REGINDE IS NOT NULL AND FLAG_REGINDE = 'NO' |
| (H) | SELECT  count(*) FROM PARTI_UDIENZA_DIFENSORE_BONIF |
| (J) | SELECT  count(*) FROM STORICO_AVVOCATO_BONIF   oppure
SELECT  count(*) FROM STORICO_AVVOCATO WHERE COD_OPERATORE_AGGIORNAMENTO LIKE 'Update Bon%' |
| (K) | SELECT  count(*) FROM AVVISI_AVVOCATO_BONIF |
| (L) | SELECT  count(*) FROM NUOVA_ISTANZA_BONIF |


verificare che nella tabella AVVOCATO bonificato non vi siano records con FLAG_REGINDE = 'SI' e Codici Fiscali uguali
SELECT count(*), COD_fiscale FROM AVVOCATO a WHERE FLAG_REGINDE = 'SI' GROUP BY COD_fiscale  HAVING count(*)>1 ORDER BY 1 DESC
il risultato dovrebbe essere = 0

verificare l’aggregazione dei records AVVOCATO aggiornati
SELECT acp.COD_FISCALE, acp.ID_AVVOCATO, acp.FLAG_REGINDE, acp.ID_AVVocato_BONIFICATO   FROM AVVOCATO acp  WHERE acp.FLAG_REGINDE = 'SI' OR ID_AVVOCATO_BONIFICATO IS NOT null ORDER BY acp.COD_FISCALE , acp.DATA_INSERIMENTO DESC, acp.ID_AVVOCATO DESC;

di seguito un esempio di un sott’insieme dell’ estrazione della query

| COD_FISCALE | ID_AVVOCATO |  | ID_AVVOCATO_BONIFICATO |
| --- | --- | --- | --- |
| BBTFBR50P30D810D | 347471012016 | SI |  |
| BBTFBR50P30D810D | 242473012013 | NO | 347471012016 |
| BBTFBR50P30D810D | 238034012012 | NO | 347471012016 |
| BBTFBR50P30D810D | 234262012012 | NO | 347471012016 |
| BBTFBR50P30D810D | 225328012010 | NO | 347471012016 |


L’esecuzione della procedura POST_XBA_CREA_AVV_CON_PENDENZE.prc è tracciata nella tabella               XBA_LOG_BONIFICA_AVVOCATI: per verificare che l’elaborazione della procedura risulti completata verificare, con la seguente query, che nella tabella ci siano le righe di Inizio e Fine POST_XBA_CREA_AVV_CON_PENDENZE.

SELECT * FROM XBA_LOG_BONIFICA_AVVOCATI order by data_esecuzione;

Di seguito un esempio:

| Inizio POST_XBA_CREA_AVV_CON_PENDENZE. La tabella POST_XBA_AVVOCATI_CON_PENDENZE conterrà i dati Degli Avvocati con procedimenti pendenti bonificati e non. |  | YYYY-MM-DD HH:MM:SS.m |
| --- | --- | --- |
| Fine POST_XBA_CREA_AVV_CON_PENDENZE. |  | YYYY-MM-DD HH:MM:SS.m |


Accertarsi che sia presente la tabella POST_XBA_ AVVOCATI_CON_PENDENZE con la seguente query:

SELECT * FROM user_tables a WHERE a.TABLE_NAME= 'POST_XBA_AVVOCATI_CON_PENDENZE';
La tabella strutturalmente è una immagine della tabella PRE_XBA_AVVOCATI_CON_PENDENZE, con l’aggiunta della colonna FLAG_REGINDE.

L’esecuzione della procedura POST_XBA_CAR_AVV_CON_PENDENZE è tracciata nella tabella
XBA_LOG_BONIFICA_AVVOCATI: per verificare che l’elaborazione della procedura risulti completata 	verificare, con la seguente query, che nella tabella ci siano le righe di Inizio e Fine POST_XBA_CAR_AVV_CON_PENDENZE.

Select * from XBA_LOG_BONIFICA_AVVOCATI order by data_esecuzione

Di seguito un esempio:
(la prima colonna non appartiene alla tabella ma serve dopo per le query di verifica)

|  | Elaborazione | Elaborati | Data_Esecuzione |
| --- | --- | --- | --- |
| (O) | Inizio POST_XBA_CAR_AVV_CON_PENDENZE. Si estraggono gli avvocati SIES per i quali sussistono fascicoli pendenti del Distretto in almeno un sottosistema (SIEP, SIUS, SIGE). I dati estratti vengono inseriti nella tabella PRE_XBA_AVVOCATI_CON_PENDENZE.  
Il valore indica il CODICE DISTRETTO | 1 | YYYY-MM-DD HH:MM:SS.m |
|  | ============================================ |  | YYYY-MM-DD HH:MM:SS.m |
| (A) | = Totale Avvocati SIEP con pendenze : | 15022 | YYYY-MM-DD HH:MM:SS.m |
| (B) | = Totale Avvocati SIUS con pendenze : | 4253 | YYYY-MM-DD HH:MM:SS.m |
| (C) | = Totale Avvocati SIGE con pendenze : | 755 | YYYY-MM-DD HH:MM:SS.m |
| (D) | = Totale Fascicoli SIEP pendenti : | 56386 | YYYY-MM-DD HH:MM:SS.m |
| (E) | = Totale Fascicoli SIUS pendenti : | 9669 | YYYY-MM-DD HH:MM:SS.m |
| (F) | = Totale Fascicoli SIGE pendenti : | 1085 | YYYY-MM-DD HH:MM:SS.m |
|  | ============================================ |  | YYYY-MM-DD HH:MM:SS.m |
|  | Fine POST_XBA_CAR_AVV_CON_PENDENZE. |  | YYYY-MM-DD HH:MM:SS.m |


E’ possibile verificare i suddetti numeri eseguendo nell’ordine le seguenti queries:

| (O) | SELECT SUBSTR(FASCICOLO_SIUS.ID_FASCICOLO_SIUS,-6, 2)  w_codice_distretto 
FROM FASCICOLO_SIUS
		WHERE ROWNUM = 1
        		GROUP BY SUBSTR(FASCICOLO_SIUS.ID_FASCICOLO_SIUS,-6, 2)
        	ORDER BY count(SUBSTR(FASCICOLO_SIUS.ID_FASCICOLO_SIUS,-6, 2)) DESC; |
| --- | --- |
| (A) | SELECT count(DISTINCT ID_AVVOCATO) FROM POST_XBA_AVVOCATI_CON_PENDENZE WHERE ambiente = 'SIEP' |
| (B) | SELECT count(DISTINCT ID_AVVOCATO) FROM POST_XBA_AVVOCATI_CON_PENDENZE WHERE ambiente = 'SIUS' |
| (C) | SELECT count(DISTINCT ID_AVVOCATO) FROM POST_XBA_AVVOCATI_CON_PENDENZE WHERE ambiente = 'SIGE' |
| (D) | SELECT count(*) FROM POST_XBA_AVVOCATI_CON_PENDENZE  WHERE AMBIENTE = 'SIEP' |
| (E) | SELECT count(*) FROM POST_XBA_AVVOCATI_CON_PENDENZE  WHERE AMBIENTE = 'SIUS' |
| (F) | SELECT count(*) FROM POST_XBA_AVVOCATI_CON_PENDENZE  WHERE AMBIENTE = 'SIGE' |



Raffrontando i numeri relativi agli avvocati (righe (A),(B),(C)) con i corrispondenti, risultanti al termine dell’esecuzione delle procedure PRE_XBA_CAR_AVV_CON_PENDENZE (vedi STEP 1) si nota che il numero degli avvocati è diminuito, a seguito dell’accorpamento di parte degli avvocati a quelli certificati, mentre sono rimasti immutati i numeri relativi ai procedimenti pendenti nei diversi ambienti.

Per raffrontare i dati post e pre bonifica, accedere alla tabella POST_XBA_AVVOCATI_CON_PENDENZE

SELECT * FROM POST_XBA_AVVOCATI_CON_PENDENZE ORDER BY ID_AVVOCATO, AMBIENTE

selezionare fra i dati estratti il codice_fiscale di un Avvocato che ricorra più volte
con stesso id_avvocato, annotando il totale dei records estratti per quell’avvocato,
es. 'SFRCLD53M10H501M'

SELECT *  FROM PRE_XBA_AVVOCATI_CON_PENDENZE WHERE COD_FISCALE = 'SFRCLD53M10H501M' ORDER BY ID_AVVOCATO, AMBIENTE

verificare che il numero di records estratti sia corrispondente a quello dei records estratti sulla tabella POST, con la differenza che in quest’ultima i procedimenti puntano tutti all’id_avvocato certificato ReGIndE.


## 3.2.6 STEP 6
Per facilitare le verifiche sulle tabelle AVVOCATO_FASCICOLO_SIEP_BONIF, AVVOCATO_FASCICOLO_SIUS_BONIF, AVVOCATO_FASCICOLO_SIGE_BONIF, PARTI_UDIENZA_DIFENSORE_BONIF, STORICO_AVVOCATO_BONIF, AVVISI_AVVOCATO_BONIF,  NUOVA_ISTANZA_BONIF  sono state realizzate le  Viste riportate di seguito.

Verificare tramite il comando pwd di trovarsi nel percorso /home/oracle/MEV-2019_21/bonifica_db/ ed eseguire il comando

./bonifica_avv_6.sh

Dettaglio del file:
XBA_VERIF_AVV_FAS_SIEP.sql    = Crea la Vista XBA_VERIF_AVV_FAS_SIEP che permette di verificare per ciascun record della tabella AVVOCATO_FASCICOLO_SIEP_BONIF la corretta individuazione dell’ avvocato certificato ReGIndE (FLAG_REGINDE = ‘SI’), gli estremi dei procedimenti SIEP interessati alla modifica dell’avvocato di riferimento.
La vista è costituita dalle seguenti colonne

| ID_AVVOCATO_FASCICOLO_SIEP | Id del record AVVOCATO_FASCICOLO_SIEP |
| --- | --- |
| FAS_SIE_ID_FASCICOLO_SIEP | Id del record FASCICOLO_SIEP a cui è collegato |
| CHIAVE_ANNO | Anno del procedimento |
| CHIAVE_PROGR | Numero progressivo del procedimento |
| CHIAVE_UFFICIO | Codice ufficio appartenenza |
| COD_TIPO_UFFICIO | Codice Tipo Ufficio |
| DESCRIZIONE | Descrizione del Comune sede ufficio |
| AVV_ID_AVVOCATO | ID dell’Avvocato prima della bonifica |
| COD_FISCALE_PREC | Codice Fiscale prima della bonifica |
| COGNOME_PREC | Cognome dell’Avvocato prima della bonifica |
| NOME_PREC | Nome dell’Avvocato prima della bonifica |
| FORO_PREC | Foro di appartenenza dell’avvocato prima della bonifica |
| AVV_ID_AVVOCATO_NEW | ID dell’Avvocato dopo la bonifica |
| COD_FISCALE | Codice Fiscale dopo la bonifica |
| COGNOME | Cognome dell’Avvocato dopo la bonifica |
| NOME | Cognome dell’Avvocato dopo la bonifica |
| FORO | Foro di appartenenza dell’avvocato dopo la bonifica |
| FLAG_REGINDE | FLAG_REGINDE dopo la bonifica |


XBA_VERIF_AVV_FAS_SIGE.sql    = Crea la Vista XBA_VERIF_AVV_FAS_SIGE che permette di verificare per ciascun record della tabella AVVOCATO_FASCICOLO_SIGE_BONIF la corretta individuazione dell’ avvocato certificato i avvocati certificati ReGIndE (FLAG_REGINDE = ‘SI’), gli estremi dei procedimenti SIGE interessati alla modifica dell’avvocato di riferimento.
La vista è costituita dalle seguenti colonne

| ID_AVVOCATO_FASCICOLO_SIGE | Id del record AVVOCATO_FASCICOLO_SIGE |
| --- | --- |
| FAS_SIGE_ID_FASCICOLO_SIGE | Id del record FASCICOLO_SIGE a cui è collegato |
| CHIAVE_ANNO | Anno del procedimento |
| CHIAVE_PROGR | Numero progressivo del procedimento |
| CHIAVE_UFFICIO | Codice ufficio appartenenza |
| COD_TIPO_UFFICIO | Codice Tipo Ufficio |
| DESCRIZIONE | Descrizione del Comune sede ufficio |
| AVV_ID_AVVOCATO | ID dell’Avvocato prima della bonifica |
| COD_FISCALE_PREC | Codice Fiscale prima della bonifica |
| COGNOME_PREC | Cognome dell’Avvocato prima della bonifica |
| NOME_PREC | Nome dell’Avvocato prima della bonifica |
| FORO_PREC | Foro di appartenenza dell’avvocato prima della bonifica |
| AVV_ID_AVVOCATO_NEW | ID dell’Avvocato dopo la bonifica |
| COD_FISCALE | Codice Fiscale dopo la bonifica |
| COGNOME | Cognome dell’Avvocato dopo la bonifica |
| NOME | Cognome dell’Avvocato dopo la bonifica |
| FORO | Foro di appartenenza dell’avvocato dopo la bonifica |
| FLAG_REGINDE | FLAG_REGINDE dopo la bonifica |


XBA_VERIF_AVV_FAS_SIUS.sql    = Crea la Vista XBA_VERIF_AVV_FAS_SIUS che permette di verificare per ciascun record della tabella AVVOCATO_FASCICOLO_SIUS_BONIF la corretta individuazione dell’ avvocato certificato ReGIndE (FLAG_REGINDE = ‘SI’), gli estremi dei procedimenti SIGE interessati alla modifica dell’avvocato di riferimento.
La vista è costituita dalle seguenti colonne

| ID_AVVOCATO_FASCICOLO_SIUS | Id del record AVVOCATO_FASCICOLO_SIUS |
| --- | --- |
| FAS_SIU_ID_FASCICOLO_SIUS | Id del record FASCICOLO_SIUS a cui è collegato |
| CHIAVE_ANNO | Anno del procedimento |
| CHIAVE_PROGR | Numero progressivo del procedimento |
| CHIAVE_UFFICIO | Codice ufficio appartenenza |
| COD_TIPO_UFFICIO | Codice Tipo Ufficio |
| DESCRIZIONE | Descrizione del Comune sede ufficio |
| AVV_ID_AVVOCATO | ID dell’Avvocato prima della bonifica |
| COD_FISCALE_PREC | Codice Fiscale prima della bonifica |
| COGNOME_PREC | Cognome dell’Avvocato prima della bonifica |
| NOME_PREC | Nome dell’Avvocato prima della bonifica |
| FORO_PREC | Foro di appartenenza dell’avvocato prima della bonifica |
| AVV_ID_AVVOCATO_NEW | ID dell’Avvocato dopo la bonifica |
| COD_FISCALE | Codice Fiscale dopo la bonifica |
| COGNOME | Cognome dell’Avvocato dopo la bonifica |
| NOME | Cognome dell’Avvocato dopo la bonifica |
| FORO | Foro di appartenenza dell’avvocato dopo la bonifica |
| FLAG_REGINDE | FLAG_REGINDE dopo la bonifica |


XBA_VERIF_AVVISI_AVVOCATO.sql    = Crea la Vista XBA_VERIF_AVVISI_AVVOCATO che permette di verificare per ciascun record della tabella AVVISI_AVVOCATO_BONIF la corretta dell’ avvocato certificato ReGIndE (FLAG_REGINDE = ‘SI’), gli estremi dei procedimenti SIUS e del relativo EVENTO interessati alla modifica dell’avvocato di riferimento.
La vista è costituita dalle seguenti colonne

| ID_AVVOCATO_PARTE_UDIENZA | Id del record AVVISO_AVVOCATO |
| --- | --- |
| ID_FASCICOLO_SIGE | Id del record FASCICOLO_SIUS a cui è collegato |
| CHIAVE_ANNO | Anno del procedimento |
| CHIAVE_PROGR | Numero progressivo del procedimento |
| CHIAVE_UFFICIO | Codice ufficio appartenenza |
| COD_TIPO_UFFICIO | Codice Tipo Ufficio |
| DESCRIZIONE | Descrizione del Comune sede ufficio |
| ID_EVENTO | Id del record EVENTO a cui è collegato |
| RV_MEANIG | Descrizione del tipo provvedimento |
| MOTIVO_PROVV | Motivo del provvedimento |
| DATA_EMISSIONE | Data emissione provvedimento |
| AVV_ID_AVVOCATO | ID dell’Avvocato prima della bonifica |
| COD_FISCALE_PREC | Codice Fiscale prima della bonifica |
| COGNOME_PREC | Cognome dell’Avvocato prima della bonifica |
| NOME_PREC | Nome dell’Avvocato prima della bonifica |
| FORO_PREC | Foro di appartenenza dell’avvocato prima della bonifica |
| AVV_ID_AVVOCATO_NEW | ID dell’Avvocato dopo la bonifica |
| COD_FISCALE | Codice Fiscale dopo la bonifica |
| COGNOME | Cognome dell’Avvocato dopo la bonifica |
| NOME | Cognome dell’Avvocato dopo la bonifica |
| FORO | Foro di appartenenza dell’avvocato dopo la bonifica |
| FLAG_REGINDE | FLAG_REGINDE dopo la bonifica |


XBA_VERIF_PARTI_UDIENZA_DIF.sql    = Crea la Vista XBA_VERIF_PARTI_UDIENZA_DIF che permette di verificare per ciascun record della tabella PARTI_UDIENZA_DIFENSORE_BONIF la corretta individuazione dell’ avvocato certificato ReGIndE (FLAG_REGINDE = ‘SI’), gli estremi dei procedimenti SIUS e del relativo EVENTO interessati alla modifica dell’avvocato di riferimento.
La vista è costituita dalle seguenti colonne

| ID_AVVOCATO_PARTE_UDIENZA | Id del record PARTE_UDIENZA_DIFENSORE |
| --- | --- |
| ID_FASCICOLO_SIGE | Id del record FASCICOLO_SIGE a cui è collegato |
| CHIAVE_ANNO | Anno del procedimento |
| CHIAVE_PROGR | Numero progressivo del procedimento |
| CHIAVE_UFFICIO | Codice ufficio appartenenza |
| COD_TIPO_UFFICIO | Codice Tipo Ufficio |
| DESCRIZIONE | Descrizione del Comune sede ufficio |
| ID_EVENTO | Id del record EVENTO a cui è collegato |
| RV_MEANIG | Descrizione del tipo provvedimento |
| MOTIVO_PROVV | Motivo del provvedimento |
| DATA_EMISSIONE | Data emissione provvedimento |
| ID_SOGGETTO | Id del record ANAGRAFICA_PARTI_UDIENZA |
| COGNOME_PARTE | Cognome della parte |
| NOME_PARTE | Nome della parte |
| AVV_ID_AVVOCATO | ID dell’Avvocato prima della bonifica |
| COD_FISCALE_PREC | Codice Fiscale prima della bonifica |
| COGNOME_PREC | Cognome dell’Avvocato prima della bonifica |
| NOME_PREC | Nome dell’Avvocato prima della bonifica |
| FORO_PREC | Foro di appartenenza dell’avvocato prima della bonifica |
| AVV_ID_AVVOCATO_NEW | ID dell’Avvocato dopo la bonifica |
| COD_FISCALE | Codice Fiscale dopo la bonifica |
| COGNOME | Cognome dell’Avvocato dopo la bonifica |
| NOME | Cognome dell’Avvocato dopo la bonifica |
| FORO | Foro di appartenenza dell’avvocato dopo la bonifica |
| FLAG_REGINDE | FLAG_REGINDE dopo la bonifica |


XBA_VERIF_STORICO_AVVOCATO.sql    = Crea la Vista XBA_VERIF_STORICO_AVVOCATO che permette di verificare per ciascun record della tabella STORICO_AVVOCATO_BONIF la corretta individuazione dell’ avvocato certificato ReGIndE (FLAG_REGINDE = ‘SI’), riportando gli estremi dell’avvocato prima e dopo la bonifica.
La vista è costituita dalle seguenti colonne

| ID_STORICO_AVVOCATO | Id del record STORICO_AVVOCATO |
| --- | --- |
| COGNOME | Id del record FASCICOLO_SIGE a cui è collegato |
| NOME | Anno del procedimento |
| COD_FISCALE | Numero progressivo del procedimento |
| AVV_ID_AVVOCATO | ID dell’Avvocato prima della bonifica |
| COD_FISCALE_PREC | Codice Fiscale prima della bonifica |
| COGNOME_PREC | Cognome dell’Avvocato prima della bonifica |
| NOME_PREC | Nome dell’Avvocato prima della bonifica |
| FORO_PREC | Foro di appartenenza dell’avvocato prima della bonifica |
| AVV_ID_AVVOCATO_NEW | ID dell’Avvocato dopo la bonifica |
| COD_FISCALE_NEW | Codice Fiscale dopo la bonifica |
| COGNOME_NEW | Cognome dell’Avvocato dopo la bonifica |
| NOME_NEW | Cognome dell’Avvocato dopo la bonifica |
| FORO | Foro di appartenenza dell’avvocato dopo la bonifica |
| FLAG_REGINDE | FLAG_REGINDE dopo la bonifica |


XBA_VERIF_NUOVA_ISTANZA.sql    = Crea la Vista XBA_VERIF_NUOVA_ISTANZA che permette di verificare per ciascun record della tabella NUOVA_ISTANZA_BONIF la corretta individuazione dell’ avvocato certificato ReGIndE (FLAG_REGINDE = ‘SI’), sia per l’avvocato assegnatario sia per l’avvocato presentante, gli estremi dei procedimenti SIEP alla modifica degli avvocati di riferimento.
La vista è costituita dalle seguenti colonne

| ID_NUOVA_ISTANZA | Id del record NUOVA_ISTANZA |
| --- | --- |
| FAS_SIE_ID_FASCICOLO_SIEP | Id del record FASCICOLO_SIEP a cui è collegato |
| CHIAVE_ANNO | Anno del procedimento |
| CHIAVE_PROGR | Numero progressivo del procedimento |
| CHIAVE_UFFICIO | Codice ufficio appartenenza |
| COD_TIPO_UFFICIO | Codice Tipo Ufficio |
| DESCRIZIONE | Descrizione del Comune sede ufficio |
| AVV_ID_AVVOCATO | ID dell’Avvocato prima della bonifica |
| COD_FISCALE_PREC | Codice Fiscale prima della bonifica |
| COGNOME_PREC | Cognome dell’Avvocato prima della bonifica |
| NOME_PREC | Nome dell’Avvocato prima della bonifica |
| FORO_PREC | Foro di appartenenza dell’avvocato prima della bonifica |
| AVV_ID_AVVOCATO_NEW | ID dell’Avvocato dopo la bonifica |
| COD_FISCALE | Codice Fiscale dopo la bonifica |
| COGNOME | Cognome dell’Avvocato dopo la bonifica |
| NOME | Cognome dell’Avvocato dopo la bonifica |
| FORO | Foro di appartenenza dell’avvocato dopo la bonifica |
| FLAG_REGINDE | FLAG_REGINDE Avvocato dopo la bonifica |
| AVV_ID_AVVOCATO_PRESENTANTE | ID dell’Avvocato Presentante prima della bonifica |
| COD_FISCALE_PRES | Codice Fiscale Avvocato Presentante prima della bonifica |
| COGNOME_PRES | Cognome dell’Avvocato Presentante prima della bonifica |
| NOME_PRES | Nome dell’Avvocato Presentante prima della bonifica |
| FORO_PRES | Foro di appartenenza dell’avv. Presentante prima della bonifica |
| AVV_ID_AVVPRES_NEW | ID dell’Avvocato Presentante dopo la bonifica |
| COD_FISCALE_PRESN | Codice Fiscale Avvocato Presentante dopo la bonifica |
| COGNOME_PRESN | Cognome dell’Avvocato Presentante dopo la bonifica |
| NOME_PRESN | Cognome dell’Avvocato Presentante dopo la bonifica |
| FORO_PRESN | Foro di appartenenza dell’avv. Presentante dopo la bonifica |
| FLAG_REGINDEN | FLAG_REGINDE Avvocato Presentante dopo la bonifica |


Per ogni punto precedente sono riportati di seguito gli eventuali controlli per verificare la corretta esecuzione dello step bonifica_avv_6.sh:

Verificare che nel file /home/oracle/MEV-2019_21/bonifica_db/log/LOG_Bonifica_AVV_6.log non siano riportati errori oracle;

Collegarsi al database con utenza siesxx:

Per verificare il corretto aggiornamento dell’avv_id_avvocato dei procedimenti SIEP pendenti, eseguire la seguente query
SELECT * FROM XBA_VERIF_AVV_FAS_SIEP   	dalla lista selezionare a campione dei procedimenti e verificare da applicativo, che al procedimento risultino collegati avvocati certificati

Per verificare il corretto aggiornamento dell’avv_id_avvocato dei procedimenti SIGE pendenti, eseguire la seguente query
SELECT * FROM XBA_VERIF_AVV_FAS_SIGE	dalla lista selezionare a campione dei procedimenti e verificare da applicativo, che al procedimento risultino collegati avvocati certificati

Per verificare il corretto aggiornamento dell’avv_id_avvocato dei procedimenti SIUS pendenti, eseguire la seguente query
SELECT * FROM XBA_VERIF_AVV_FAS_SIUS	dalla lista selezionare a campione dei procedimenti e verificare da applicativo, che al procedimento risultino collegati avvocati certificati

Per verificare il corretto aggiornamento dell’avv_id_avvocato dei records AVVISI_AVVOCATO, eseguire la seguente query
SELECT * FROM XBA_VERIF_AVVISI_AVVOCATO	dalla lista selezionare a campione dei procedimenti SIUS e verificare da applicativo, che al procedimento risulti collegato l’avvocato certificato

Per verificare il corretto aggiornamento dell’avv_id_avvocato dei records PARTI_UDIENZA_DIFENSORE, eseguire la seguente query
SELECT * FROM XBA_VERIF_PARTI_UDIENZA_DIF	dalla lista selezionare a campione dei procedimenti Sige e verificare da applicativo, che al procedimento risulti collegato l’avvocato certificato

Per verificare il corretto aggiornamento dell’avv_id_avvocato dei records STORICO_AVVOCATO, eseguire la seguente query
SELECT * FROM XBA_VERIF_STORICO_AVVOCATO

Per verificare il corretto aggiornamento dell’avv_id_avvocato e dell’avv_id_avvocato_presentante dei records NUOVA_ISTANZA, eseguire la seguente query
SELECT * FROM XBA_VERIF_NUOVA_ISTANZA	    	dalla lista selezionare a campione dei procedimenti SIEP e verificare da applicativo, che al procedimento risultino collegati avvocati certificati

In caso di esito positivo dell’intera procedura di Bonifica, TUTTE LE TABELLE DI BACKUP, DI LOG E DI APPOGGIO RIPORTATE NEGLI STEP DA 1 A 6 NON DEVONO ESSERE CANCELLATE E DEVONO ESSERE MANTENUTE PER ALMENO 6 MESI, PER PERMETTERE EVENTUALI ATTIVITÀ DI VERIFICA.
## 3.2.7 STEP 7
QUESTO STEP VA ESEGUITO SOLO IN CASO DI ERRORI VERIFICATISI NELL’ESECUZIONE DI UNO DEGLI STEP PRECEDENTI E SOLO SU INDICAZIONE DEI TECNICI DEL FORNITORE, COINVOLTI A SEGUITO APERTURA TICKET SU OTRS.

Verificare tramite il comando pwd di trovarsi nel percorso /home/oracle/MEV-2019_21/bonifica_db/ ed eseguire il comando

./bonifica_restore.sh

Dettaglio del file:
XBA_RESTORE_TABELLE_AVVOCATI.prc = Effettua il ripristino di tutte le tabelle interessate dalla bonifica (AVVOCATO, AVVOCATO_FASCICOLO_SIEP, AVVOCATO_FASCICOLO_SIUS, AVVOCATO_FASCICOLO_SIGE, PARTI_UDIENZA_DIFENSORE, STORICO_AVVOCATO, AVVISI_AVVOCATO,  NUOVA_ISTANZA), utilizzando le tabelle di backup AVVOCATO_SXBA, AVVOCATO_FASCICOLO_SIEP_SXBA, AVVOCATO_FASCICOLO_SIUS_SXBA, AVVOCATO_FASCICOLO_SIGE_SXBA, PARTI_UDIENZA_DIFENSORE_SXBA, STORICO_AVVOCATO_SXBA, AVVISI_AVVOCATO_SXBA,  NUOVA_ISTANZA_SXBA (vedi STEP2 punto 1).
Restore_CGREFCODES_pre_Bonifica.sql – Lo script ripristina i domini ‘FORO_AVVOCATI’ e ‘NON_ATTIVITA’ della CG_REF_CODES allo stato preesistente all’esecuzione dei punti 3 e 4 dello STEP 2.
DROP_TABELLE_BONIFICA.sql = Lo script cancella tutte le tabelle di backup, di log e di appoggio, create negli STEP da 1 a 6, predisponendo la base dati per una nuova esecuzione della procedura.

Per ogni punto precedente sono riportati di seguito gli eventuali controlli per verificare la corretta esecuzione dello step bonifica_avv_2.sh:

Verificare che nel file /home/oracle/MEV-2019_21/bonifica_db/log/LOG_Bonifica_AVV_Restore.log non siano riportati errori oracle;

Collegarsi al database con utenza siesxx:
1.	L’esecuzione della procedura XBA_RESTORE_TABELLE_AVVOCATI.prc  è tracciata nella tabella
XBA_LOG_BONIFICA_AVVOCATI: per verificare che l’elaborazione della procedura risulti completata verificare, con la seguente query, che nella tabella ci siano le righe di Inizio e Fine XBA_RESTORE_TABELLE_AVVOCATI.

SELECT * FROM XBA_LOG_BONIFICA_AVVOCATI ORDER BY DATA_ESECUZIONE

Di seguito un esempio:


| Elaborazione | Elaborati | Data_Esecuzione |
| --- | --- | --- |
| ===> Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore di tutte le tabelle interessate dalla procedura di bonifica. |  | YYYY-MM-DD HH:MM:SS.m |
| Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore tabella AVVOCATO effettuata. |  | YYYY-MM-DD HH:MM:SS.m |
| Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore tabella AVVOCATO_FASCICOLO_SIEP effettuata. |  | YYYY-MM-DD HH:MM:SS.m |
| Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore tabella AVVOCATO_FASCICOLO_SIUS effettuata. |  | YYYY-MM-DD HH:MM:SS.m |
| Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore tabella AVVOCATO_FASCICOLO_SIGE effettuata. |  | YYYY-MM-DD HH:MM:SS.m |
| Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore tabella PARTI_UDIENZA_DIFENSORE effettuata. |  | YYYY-MM-DD HH:MM:SS.m |
| Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore tabella STORICO_AVVOCATO effettuata. |  | YYYY-MM-DD HH:MM:SS.m |
| Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore tabella AVVISI_AVVOCATO effettuata. |  | YYYY-MM-DD HH:MM:SS.m |
| Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore tabella NUOVA_ISTANZA effettuata. |  | YYYY-MM-DD HH:MM:SS.m |
| ===> Fine XBA_RESTORE_TABELLE_AVVOCATI. Restore di tutte le tabelle interessate dalla procedura di bonifica. |  | YYYY-MM-DD HH:MM:SS.m |


E’ possibile eseguire anche la seguente query

SELECT COUNT(*) FROM AVVOCATO WHERE FORO IN ('REGGIO DI CALABRIA', 'REGGIO NELL''EMILIA', 'MASSA',  'CARRARA', 'FORLI''', 'CESENA')

il risultato deve essere <> 0

Per verificare l’esecuzione dello script Restore_CGREFCODES_pre_Bonifica.sql prc
eseguire quanto di seguito:

SELECT * FROM CG_REF_CODES WHERE RV_DOMAIN = ‘NON_ATTIVITA’

verificare che non siano presenti i nuovi records con RV_LOW_VALUE = (A, C ,R , S)

SELECT COUNT(*) FROM CG_REF_CODES WHERE RV_DOMAIN = ‘FORO_AVVOCATO’ AND RV_ALT2_VALUE IS NOT NULL

il risultato deve essere = 0

E’ possibile, inoltre, verificare l’assenza delle suddette tabelle di backup  e di log con la seguenti query:
SELECT * FROM USER_TABLES A WHERE A.TABLE_NAME LIKE '%_SXBA' ORDER BY TABLE_NAME

SELECT * FROM USER_TABLES A WHERE A.TABLE_NAME LIKE '%_BONIF' ORDER BY TABLE_NAME

che non devono estrarre alcuna occorrenza.

TUTTE LE TABELLE DI BACKUP, DI LOG E DI APPOGGIO RIPORTATE NEGLI STEP DA 1 A 6 NON DEVONO ESSERE CANCELLATE AL TERMINE DELLA PROCEDURA DI BONIFICA E MANTENUTE PER ALMENO 6 MESI, PER PERMETTERE EVENTUALI ATTIVITÀ DI VERIFICA.
## 3.3	Procedura di Aggiornamento Tabella SIES da Tabella fissa DGSIA
Le attività descritte in questo paragrafo non devono essere eseguite nella fase di messa in esercizio della MEV nei Distretti, che si limiteranno ad importare la tabella  AVVOCATO_REGINDE_18112020.dmp, già precaricata.

Le attività sono riportate per permettere (qualora si abbia un elenco di Avvocati più aggiornato) di rieseguire tutte le operazioni effettuate per giungere all’ottenimento della suddetta tabella, partendo dal file .xls fornito dall’Amministrazione, contenente gli avvocati estratti da ReGIndE.

La prima attività da eseguire è l’importazione in SIES  della tabella Avvocati Reginde, fornita dall’Amministrazione, tabellefisse18novembre2020.xls, contenente 388221 records (disponibilità del file comunicato via e-mail da annamaria.palmieri@giustizia.ii a vito.bufi@eng.it il 23/11/2020 13:05). Poiché nella tabella vi sono avvocati riferite ad Enti non di interesse di SIES, righe duplicate per lo stesso Difensore, si procede prima al trattamento dei dati effettuando le seguenti operazioni:
Applicare filtro su tutte le colonne
sulla colonna ODA, aprire il filtro e selezionare solo quelli non riferiti a ODA (es. Avvocatura, Consigli nazionali, Enti, vuote). Eliminare tutte le righe.
sulla colonna ODA, aprire il filtro e selezionare tutti gli  ODA
ordinare la tabella per codice fiscale cresc, tipo_indirizzo cresc, comune residenza cresc, indirizzo cresc
Scegliere Dati > Rimuovi duplicati e in Colonne selezionare la colonna Codice Fiscale. Fare clic su OK.
Salvare il file con nuovo nome  (es. tabellefisse18novembre2020-senza duplicati.xls, contenente 242948 records).
I due files .xls sono contenuti all’interno della cartella bonifica.

Bisogna quindi creare in SIES la tabella AVVOCATO_REGINDE_18112020 in cui importare i dati, eseguendo lo script

Crea_tabella_AVVOCATO_REGINDE_18112020.sql

La tabella, oltre a creare tutte le colonne presenti nel file di input, aggiunge anche le colonne COD_CATASTO, COD_COMUNE e COD_NAZIONE, che saranno valorizzate successivamente con procedure plsql previste all’interno della procedura di aggiornamento della tabelle COMUNE, CG_REF_CODES e CODICI_SIES_NSC (vedi SIUT-SIES-MG-1.1-20211008 - Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_SIES). La valorizzazione delle suddette 3 colonne è un prerequisito all’avvio della procedura di Bonifica Avvocati.

Poi importare i dati utilizzando uno dei tools a disposizione (Toad, plsql developer, sql developer, DbEaver, …). Questa attività deve essere eseguita a livello centrale, in modo da permettere la distribuzione nei Distretti della tabella AVVOCATO_REGINDE_18112020 già precaricata.

Nella cartella di distribuzione della procedura di bonifica è presente il file AVVOCATO_REGINDE_18112020.dmp, che va semplicemente importato in SIES.