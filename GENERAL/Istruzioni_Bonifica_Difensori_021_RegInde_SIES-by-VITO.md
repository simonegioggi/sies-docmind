---
uniqueName: istruzionibonificadifensori021regindesies-by-vito
displayName: "Istruzioni Bonifica Difensori 021 RegInde SIES by VITO"
category: "GENERAL"
tags: []
---

# Istruzioni_Bonifica_Difensori_021_RegInde_SIES by VITO

> **File originale:** `MEV/SCHEDA_021/Docs/consegna docx/20220915/Istruzioni_Bonifica_Difensori_021_RegInde_SIES by VITO.docx`  
> **Tipo:** DOCX

---


Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi Direzione Generale per i Sistemi Informativi Automatizzati


Istruzioni Bonifica Difensori
MEV 021_2019 RegInde










Versione 1.4 del 25/05/2022





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Engineering | RTI |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 25/05/2022 |  |
| Livello di riservatezza | L3 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 30/07/2021 | Prima emissione |  |
| 1.1 | 08/10/2021 | Seconda emissione | Rivista intera struttura documento |
| 1.2 | 24/01/2022 | Terza emissione | Rivista intera struttura documento |
| 1.3 | 22/04/2022 | Quarta emissione | Rivista intera struttura documento |
| 1.4 | 25/05/2022 | Quinta emissione | Eliminato par. 3.3 |
| 1.5 |  | Sesta Emissione |  |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dott. Oris Orlando | Amministrazione |  | Direttore Esecutivo Contratto |
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



INDICE DEI CONTENUTI
1 	Introduzione	5
1.1 Scopo del documento	5
1.2 Riferimenti	5
1.3 Glossario	5
1.3.1 Definizioni	5
1.3.2 Acronimi e abbreviazioni	5
2 	Generalità	7
3 	Descrizione delle Attività	8
3.1 Istruzioni per lancio eseguibili file.sh	8
3.1.1 Attività di installazione ed esecuzione procedura batch Bonifica Difensori	8
3.2 Procedura Bonifica Difensori SIES	9
3.2.1 STEP 1	9
3.2.2 STEP 2	13
3.2.3 STEP 3	16
3.2.4 STEP 4	17
3.2.5 STEP 5	20
3.2.6 STEP 6	25
3.2.7 STEP 7	32

# 1 	Introduzione
## 1.1 Scopo del documento
Il presente documento viene rilasciato con lo scopo di dettagliare le attività preliminari da eseguire prima della messa in esercizio della MEV 21 RegInde e sono relative alla bonifica dei difensori sulla base dell’estrazione degli avvocati presenti in ReGIndE, fornita dall’Amministrazione.
In particolare, nel seguente documento, si forniscono le istruzioni da seguire ed i relativi controlli da effettuare prima della messa in esercizio della MEV 21.
## 1.2 Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF1. | SIUT-SIE-PR-1.3-20220422-Piano_di_rilascio_021_RegInde_SIES | Piano di rilascio |

## 1.3 Glossario
## 1.3.1 Definizioni
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
in cui siesxx deve essere sies<SIGLADISTRETTO> (es. siesto per Torino)
Nel file di log menzionato nel comando si potrà controllare l’esito dell’import (ovvero la creazione della tabella AVVOCATO_REGINDE_18112020 nel tablespace ‘siesxx’).
Posizionarsi nel percorso /home/oracle/MEV-2019_21/bonifica_db/; lanciare sequenzialmente i comandi, indicati nel par. 3.2 Procedura Bonifica Difensori SIES
## 3.2 Procedura Bonifica Difensori SIES
Di seguito le attività da eseguire per la bonifica degli AVVOCATI di SIES con i dati di REGINDE.
I diversi step sottoelencati saranno tracciati nella tabella di log XBA_LOG_BONIFICA_AVVOCATI.
N.B. Effettuare preliminarmente uno snapshot del DB di modo che in caso di esito negativo di una o più verifiche riportate nei successivi STEP si possa riportare il DB alla situazione iniziale.
## 3.2.1 STEP 1
Verificare tramite il comando pwd di trovarsi nel percorso /home/oracle/MEV-2019_21/bonifica_db/ ed eseguire il comando

./bonifica_avv_1.sh

Dettaglio del file:
CREA_TABELLA_XBA_LOG_BONIFICA_AVVOCATI.sql = Crea tabella XBA_LOG_BONIFICA_AVVOCATI che conterrà il LOG delle successive attività.
PRE_XBA_CREA_AVV_CON_PENDENZE.prc = Crea Tabella PRE_XBA_AVVOCATI_CON_PENDENZE che conterrà i dettagli di tutti gli avvocati aventi procedimenti SIEP, SIUS e SIGE pendenti.
PRE_XBA_CAR_AVV_CON_PENDENZE.prc = Compila ed Esegue la procedura PRE_XBA_CAR_AVV_CON_PENDENZE  per  estrarre dalla tabella AVVOCATO i records relativi ai difensori con procedimenti SIEP, SIUS e SIGE pendenti, relativi ad uffici giudiziari del Distretto, creando un record per ciascun procedimento,  e li inserisce nella tabella PRE_XBA_ AVVOCATI_CON_PENDENZE. (La tabella può essere utilizzata per verificare la correttezza dei dati che saranno estratti dalla successiva procedure XBA_CARICA_AVV_CON_PENDENZE.prc).
Un procedimento SIEP si considera pendente se non archiviato (COD_STATO_FASCICOLO <> '01').
Un procedimento SIUS si considera pendente se non in stato di Definito o di Emesso Provvedimento o di unificato (COD_STATO_FASCICOLO NOT in ('01', '07', '05')).
Un procedimento SIGE si considera pendente se la data definizione non è valorizzata (DATA_DEFINIZIONE IS NULL).
Per ciascun Avvocato selezionato vengono valorizzate le colonne AMBIENTE (nome sottosistema) e NUM_PENDENZE (totale procedimenti pendenti nell’ambiente).
Per ogni punto precedente sono riportati di seguito gli eventuali controlli per verificare la corretta esecuzione dello step bonifica_avv_1.sh:

Verificare che nel file /home/oracle/MEV-2019_21/bonifica_db/log/LOG_Bonifica_AVV_1.log non siano riportati errori oracle;

Collegarsi al database con utenza SIESXX

Per verificare la creazione della tabella XBA_LOG_BONIFICA_AVVOCATI, effettuare la query

SELECT * FROM user_tables a WHERE a.TABLE_NAME='XBA_LOG_BONIFICA_AVVOCATI';


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


Per verificare che la procedura PRE_XBA_CAR_AVV_CON_PENDENZE sia stata eseguita, effettuare la seguente query:

SELECT count(*) FROM PRE_XBA_AVVOCATI_CON_PENDENZE pacp

La query deve ritornare un valore maggiore di zero.

Per verificare la correttezza dei numeri riportati nella PRE_XBA_AVVOCATI_CON_PENDENZE eseguire le seguenti queries, in cui bisogna sostituire il parametro ‘XX’ con il codice del Distretto:


SELECT count(DISTINCT ID_AVVOCATO) FROM PRE_XBA_AVVOCATI_CON_PENDENZE pacp
WHERE ambiente = 'SIEP'

Deve essere uguale a:

SELECT count(*) "Avvocati con pendenze SIEP"  FROM (SELECT DISTINCT a.* FROM AVVOCATO a
JOIN AVVOCATO_FASCICOLO_SIEP afs ON (afs.AVV_ID_AVVOCATO = a.ID_AVVOCATO and SUBSTR(afs.FAS_SIE_ID_FASCICOLO_SIEP,-6, 2) = 'XX')
JOIN FASCICOLO_SIEP fs ON (fs.ID_FASCICOLO_SIEP = afs.FAS_SIE_ID_FASCICOLO_SIEP
and  fs.COD_STATO_FASCICOLO <> '01'))


SELECT count(DISTINCT ID_AVVOCATO) FROM PRE_XBA_AVVOCATI_CON_PENDENZE pacp
WHERE ambiente = 'SIUS'

Deve essere uguale a:

SELECT count(*) "Avvocati con pendenze SIUS"  FROM (SELECT DISTINCT a.* FROM AVVOCATO a
JOIN AVVOCATO_FASCICOLO_SIUS afs ON (afs.AVV_ID_AVVOCATO = a.ID_AVVOCATO and SUBSTR(afs.FAS_SIU_ID_FASCICOLO_SIUS,-6, 2) = 'XX')
JOIN FASCICOLO_SIUS fs ON (fs.ID_FASCICOLO_SIUS = afs.FAS_SIU_ID_FASCICOLO_SIUS
and  fs.COD_STATO_FASCICOLO  NOT IN ('01','05','07')))



SELECT count(DISTINCT ID_AVVOCATO) FROM PRE_XBA_AVVOCATI_CON_PENDENZE pacp
WHERE ambiente = 'SIGE'

Deve essere uguale a

SELECT count(*) "Avvocati con pendenze SIGE"  FROM (SELECT DISTINCT a.* FROM AVVOCATO a
JOIN AVVOCATO_FASCICOLO_SIGE afs ON (afs.AVV_ID_AVVOCATO = a.ID_AVVOCATO and SUBSTR(afs.FAS_SIGE_ID_FASCICOLO_SIGE,-6, 2) = 'XX')
JOIN FASCICOLO_SIGE fs ON (fs.ID_FASCICOLO_SIGE = afs.FAS_SIGE_ID_FASCICOLO_SIGE
and  fs.DATA_DEFINIZIONE IS NULL))


SELECT count(*) FROM PRE_XBA_AVVOCATI_CON_PENDENZE pxacp WHERE AMBIENTE = 'SIEP'

Deve essere uguale a

select count(*) "Fascicoli SIEP pendenti" from AVVOCATO a JOIN AVVOCATO_FASCICOLO_SIEP afs   ON(afs.AVV_ID_AVVOCATO = a.ID_AVVOCATO AND SUBSTR(afs.FAS_SIE_ID_FASCICOLO_SIEP,-6, 2) = 'XX') JOIN FASCICOLO_SIEP fs ON (fs.ID_FASCICOLO_SIEP = afs.FAS_SIE_ID_FASCICOLO_SIEP and  fs.COD_STATO_FASCICOLO <> '01' )



SELECT count(*) FROM PRE_XBA_AVVOCATI_CON_PENDENZE pxacp WHERE AMBIENTE = 'SIUS'

Deve essere uguale a

select count(*) "Fascicoli SIUS pendenti " from avvocato a JOIN AVVOCATO_FASCICOLO_SIUS afs ON (afs.AVV_ID_AVVOCATO = a.ID_AVVOCATO AND SUBSTR(afs.FAS_SIU_ID_FASCICOLO_SIUS,-6, 2) = 'XX')
JOIN FASCICOLO_SIUS fs ON (fs.ID_FASCICOLO_SIUS = afs.FAS_SIU_ID_FASCICOLO_SIUS
and  fs.COD_STATO_FASCICOLO  NOT IN ('01','05','07') )



SELECT count(*) FROM PRE_XBA_AVVOCATI_CON_PENDENZE pxacp WHERE AMBIENTE = 'SIGE'

Deve essere uguale a

select count(*) " Fascicoli SIGE pendenti " from avvocato_sxba a
JOIN AVVOCATO_FASCICOLO_SIGE_sxba afs ON (afs.AVV_ID_AVVOCATO = a.ID_AVVOCATO AND SUBSTR(afs.FAS_SIGE_ID_FASCICOLO_SIGE,-6, 2) = 'XX')
JOIN FASCICOLO_SIGE fs ON (fs.ID_FASCICOLO_SIGE = afs.FAS_SIGE_ID_FASCICOLO_SIGE
and  fs.DATA_DEFINIZIONE IS NULL )


Accedendo, inoltre, alla tabella PRE_XBA_AVVOCATI_CON_PENDENZE è possibile selezionare, a campione, procedimenti SIEP, SIUS e SIGE e il relativo avvocato assegnatario: collegandosi, quindi, da applicativo web, è possibile verificare che i procedimenti risultino effettivamente in stato di ISCRITTO e assegnati all’avvocato indicato in tabella.


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

Per verificare che l’elaborazione della procedura risulti completata verificare, con la seguente query, che siano presenti le tabelle: AVVOCATO, AVVOCATO_FASCICOLO_SIEP, AVVOCATO_FASCICOLO_SIUS, AVVOCATO_FASCICOLO_SIGE, PARTI_UDIENZA_DIFENSORE, STORICO_AVVOCATO, AVVISI_AVVOCATO, NUOVA_ISTANZA , CG_REF_CODES con suffisso _SXBA e _BONIF.

SELECT * FROM USER_TABLES A WHERE A.TABLE_NAME LIKE '%_SXBA' ORDER BY TABLE_NAME;
SELECT * FROM USER_TABLES A WHERE A.TABLE_NAME LIKE '%_BONIF' ORDER BY TABLE_NAME;

Per verificare l’aggiornamento effettuato al secondo punto eseguire le seguenti query:

Query per verificare gli avvocati prima dell’aggiornamento:

SELECT foro, COUNT(*) FROM AVVOCATO_SXBA WHERE FORO IN ('REGGIO DI CALABRIA', 'REGGIO CALABRIA','REGGIO NELL''EMILIA', 'REGGIO EMILIA', 'MASSA',  'CARRARA',
'MASSA CARRARA', 'FORLI'' CESENA', 'FORLI''', 'CESENA', 'FORLÌ-CESENA')  GROUP BY foro

es. risultato (n.b. i numeri variano per ogni Distretto)

| FORO | COUNT(*) |
| --- | --- |
| CARRARA | 2 |
| CESENA | 4 |
| FORLI' | 1059 |
| MASSA | 69 |
| MASSA CARRARA | 860 |
| REGGIO CALABRIA | 2318 |
| REGGIO DI CALABRIA | 603 |
| REGGIO EMILIA | 1014 |
| REGGIO NELL'EMILIA | 279 |



Query sulla tabella AVVOCATO, oggetto delle modifiche:

SELECT foro, COUNT(*) FROM AVVOCATO WHERE FORO IN ('REGGIO DI CALABRIA', 'REGGIO CALABRIA','REGGIO NELL''EMILIA', 'REGGIO EMILIA', 'MASSA',  'CARRARA',
'MASSA CARRARA', 'FORLI'' CESENA', 'FORLI''', 'CESENA', 'FORLÌ-CESENA')  GROUP BY
foro

verificare che siano presenti solo i fori sottoelencati e che il totale del numero di records sia uguale o maggiore di quelli della precedente query.

esempio  (n.b. i numeri variano per ogni Distretto)

| FORO | COUNT(*) |
| --- | --- |
| FORLÌ-CESENA | 1061 |
| MASSA CARRARA | 931 |
| REGGIO CALABRIA | 2921 |
| REGGIO EMILIA | 1293 |




Per verificare l’aggiornamento effettuato al terzo punto eseguire quanto di seguito:

SELECT * FROM CG_REF_CODES WHERE RV_DOMAIN = 'NON_ATTIVITA'

verificare che siano presenti i 4 nuovi records con RV_LOW_VALUE = (A, C ,R , S)

Per verificare l’aggiornamento effettuato al quarto punto eseguire quanto di seguito:

La query:
SELECT * FROM CG_REF_CODES WHERE RV_DOMAIN = 'FORO_AVVOCATI' and RV_ALT2_VALUE Is Null
non deve fornire alcun risultato.

La query:
SELECT * FROM CG_REF_CODES WHERE RV_DOMAIN = 'FORO_AVVOCATI' and RV_MEANING = ‘NAPOLI NORD’
deve fornire un record.

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


Accertarsi che sia presente la tabella XBA_ AVVOCATI_CON_PENDENZE con la seguente query:

SELECT * FROM USER_TABLES A WHERE A.TABLE_NAME='XBA_AVVOCATI_CON_PENDENZE'

La tabella strutturalmente è una immagine della tabella AVVOCATO, con l’aggiunta delle seguenti
colonne:

| AMBIENTE | Nome del sottosistema di appartenenza del procedimento ( SIEP, SIUS, SIGE) |
| --- | --- |
| NUM_PENDENZE | Numero totale proc. pendenti a carico dell’avvocato nell’ambito del sottosistema |
| ID_AVV_CERT_REGINDE | non valorizzato |




E’ possibile verificare la corrispondenza dei record nella tabella XBA_AVVOCATI_CON_PENDENZE con quelli riportati nell’analoga tabella riportata allo STEP1 – punto 3 delle verifiche (PRE_XBA_CAR_AVV_CON_PENDENZE.prc) a pag.11

Accedendo alla tabella XBA_AVVOCATI_CON_PENDENZE, eseguendo la query

SELECT ID_AVVOCATO, COD_FISCALE, AMBIENTE, NUM_PENDENZE  FROM XBA_AVVOCATI_CON_PENDENZE ORDER BY COD_FISCALE, AMBIENTE

è possibile selezionare, a campione, un avvocato, anche con più occorrenze, annotarsi Codice Fiscale, il numero di pendenze (valore NUM_PENDENZE) per ciascun AMBIENTE e verificare che nella tabella PRE_XBA_AVVOCATI_CON_PENDENZE, eseguendo la seguente query (in cui va sostituito il parametro 'XXXXXXXXXXXXXXXX' con il codice fiscale annotato)

SELECT * FROM PRE_XBA_AVVOCATI_CON_PENDENZE WHERE COD_FISCALE = 'XXXXXXXXXXXXXXXX' ORDER BY AMBIENTE

siano presenti un numero di records (Procedimenti pendenti) corrispondenti al numero riportato in NUM_PENDENZE della tabella XBA_AVVOCATI_CON_PENDENZE per AMBIENTE.
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


1 e 2)
Per verificare l’esito della procedura, è possibile accedere ai dati della vista XBA_VERIF_AVV_CERTIFICABILI, eseguendo la query:

SELECT DISTINCT A.COD_FISCALE_RI   FROM XBA_VERIF_AVV_CERTIFICABILI A, XBA_VERIF_AVV_CERTIFICABILI B
WHERE A.FLAG_REGINDE = 'SI'   AND A.ID_AVVOCATO = B.ID_AVVOCATO_CERT   AND B.FLAG_REGINDE = 'NO'

Successivamente, eseguire la query di seguito riportata, sostituendo il codice fiscale XXXXXXXXXXXXXXXX con uno di quelli selezionati in precedenza

SELECT * FROM XBA_AVVOCATI_CON_PENDENZE WHERE COD_FISCALE = 'XXXXXXXXXXXXXXXX' ORDER BY FLAG_REGINDE DESC, DATA_INSERIMENTO DESC

verificare che l’avvocato certificato, individuato come riferimento di tutti gli altri, sia effettivamente l’ultimo inserito in ordine di tempo (valore DATA_INSERIMENTO) e a parità di data quello con ID_AVVOCATO più recente
Verificare se aggiungere la condizione AVERE FLAG_REGINDE=SI?????
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

Verificare che nella tabella AVVOCATO bonificato non vi siano records con FLAG_REGINDE = 'SI' e Codici Fiscali uguali
SELECT count(*), COD_fiscale FROM AVVOCATO a WHERE FLAG_REGINDE = 'SI' GROUP BY COD_fiscale  HAVING count(*)>1 ORDER BY 1 DESC

il risultato deve essere = 0

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



Accertarsi che sia presente la tabella POST_XBA_ AVVOCATI_CON_PENDENZE con la seguente query:

SELECT * FROM user_tables a WHERE a.TABLE_NAME= 'POST_XBA_AVVOCATI_CON_PENDENZE';

La tabella strutturalmente è una immagine della tabella PRE_XBA_AVVOCATI_CON_PENDENZE, con l’aggiunta della colonna FLAG_REGINDE.

Verificare che la query:

SELECT count(DISTINCT ID_AVVOCATO) FROM POST_XBA_AVVOCATI_CON_PENDENZE WHERE ambiente = 'SIEP'

restituisca un numero <= a quello restituito dalla query:

SELECT count(DISTINCT ID_AVVOCATO) FROM PRE_XBA_AVVOCATI_CON_PENDENZE pacp
WHERE ambiente = 'SIEP'

==============================================================================

SELECT count(DISTINCT ID_AVVOCATO) FROM POST_XBA_AVVOCATI_CON_PENDENZE WHERE ambiente = 'SIUS'

restituisca un numero <= a quello restituito dalla query:

SELECT count(DISTINCT ID_AVVOCATO) FROM PRE_XBA_AVVOCATI_CON_PENDENZE pacp WHERE ambiente = 'SIUS'
==============================================================================

SELECT count(DISTINCT ID_AVVOCATO) FROM POST_XBA_AVVOCATI_CON_PENDENZE WHERE ambiente = 'SIGE'

restituisca un numero <= a quello restituito dalla query:

SELECT count(DISTINCT ID_AVVOCATO) FROM PRE_XBA_AVVOCATI_CON_PENDENZE pacp WHERE ambiente = 'SIGE'

ovvero, il numero degli avvocati è diminuito, a seguito dell’accorpamento di parte degli avvocati a quelli certificati.

Sono rimasti, invece, immutati i numeri relativi ai procedimenti pendenti nei diversi ambienti:

per raffrontare i dati post e pre bonifica, accedere alla tabella POST_XBA_AVVOCATI_CON_PENDENZE ed eseguire la query cambiando XXXXXXXXXXXXXXXX con il codice fiscale di un avvocato

SELECT count(*) FROM POST_XBA_AVVOCATI_CON_PENDENZE WHERE COD_FISCALE = ‘XXXXXXXXXXXXXXXX‘

Eseguire questa query con lo stesso codice fiscale

SELECT count(*)  FROM PRE_XBA_AVVOCATI_CON_PENDENZE WHERE COD_FISCALE = ‘XXXXXXXXXXXXXXXX’ORDER BY ID_AVVOCATO, AMBIENTE

verificare che il numero di records estratti sia corrispondente a quello dei records estratti sulla tabella POST. E’ possibile anche verificare una congruità dei dati estratti confrontando i dati degli id_fascicolo_siep, id_fascicolo_sius e id_fascicolo_sige e verificando che siano uguali tra le due tabelle:

SELECT SUM(fas_siep),SUM(fas_sius), SUM(fas_sige) FROM (
SELECT COUNT(DISTINCT a.id_fascicolo_siep) fas_siep, 0 fas_sius, 0 fas_sige FROM POST_XBA_AVVOCATI_CON_PENDENZE a, PRE_XBA_AVVOCATI_CON_PENDENZE b WHERE a.cod_fiscale='XXXXXXXXXXXXXXXX'
AND a.cod_fiscale=b.cod_fiscale
AND a.ambiente=b.ambiente
AND a.id_fascicolo_siep=b.id_fascicolo_siep
AND a.id_fascicolo_siep IS NOT NULL
UNION
SELECT 0 fas_siep, COUNT(DISTINCT a.id_fascicolo_sius) fas_sius, 0 fas_sige FROM POST_XBA_AVVOCATI_CON_PENDENZE a, PRE_XBA_AVVOCATI_CON_PENDENZE b WHERE a.cod_fiscale='XXXXXXXXXXXXXXXX'
AND a.cod_fiscale=b.cod_fiscale
AND a.ambiente=b.ambiente
AND a.id_fascicolo_sius=b.id_fascicolo_sius
AND a.id_fascicolo_sius IS NOT NULL
UNION
SELECT 0 fas_siep, 0 fas_sius, COUNT(DISTINCT a.id_fascicolo_sige) fas_sige FROM POST_XBA_AVVOCATI_CON_PENDENZE a, PRE_XBA_AVVOCATI_CON_PENDENZE b WHERE a.cod_fiscale='XXXXXXXXXXXXXXXX'
AND a.cod_fiscale=b.cod_fiscale
AND a.ambiente=b.ambiente
AND a.id_fascicolo_sige=b.id_fascicolo_sige
AND a.id_fascicolo_sige IS NOT NULL)

FAS_SIEP deve essere uguale al risultato delle query:

SELECT COUNT(DISTINCT A.ID_FASCICOLO_SIEP) FAS_SIEP
FROM PRE_XBA_AVVOCATI_CON_PENDENZE A
WHERE A.COD_FISCALE = 'XXXXXXXXXXXXXXXX'
AND A.ID_FASCICOLO_SIEP IS NOT NULL;

SELECT COUNT(DISTINCT A.ID_FASCICOLO_SIEP) FAS_SIEP
FROM POST_XBA_AVVOCATI_CON_PENDENZE A
WHERE A.COD_FISCALE = 'XXXXXXXXXXXXXXXX'
AND A.ID_FASCICOLO_SIEP IS NOT NULL;

FAS_SIUS deve essere uguale al risultato delle query:

SELECT COUNT(DISTINCT A.ID_FASCICOLO_SIUS) FAS_SIUS
FROM PRE_XBA_AVVOCATI_CON_PENDENZE A
WHERE A.COD_FISCALE = 'XXXXXXXXXXXXXXXX'
AND A.ID_FASCICOLO_SIUS IS NOT NULL;

SELECT COUNT(DISTINCT A.ID_FASCICOLO_SIUS) FAS_SIUS
FROM POST_XBA_AVVOCATI_CON_PENDENZE A
WHERE A.COD_FISCALE = 'XXXXXXXXXXXXXXXX'
AND A.ID_FASCICOLO_SIUS IS NOT NULL;

FAS_SIGE deve essere uguale al risultato delle query:

SELECT COUNT(DISTINCT A.ID_FASCICOLO_SIUS) FAS_SIGE
FROM PRE_XBA_AVVOCATI_CON_PENDENZE A
WHERE A.COD_FISCALE = 'XXXXXXXXXXXXXXXX'
AND A.ID_FASCICOLO_SIGE IS NOT NULL;

SELECT COUNT(DISTINCT A.ID_FASCICOLO_SIUS) FAS_SIGE
FROM POST_XBA_AVVOCATI_CON_PENDENZE A
WHERE A.COD_FISCALE = 'XXXXXXXXXXXXXXXX'
AND A.ID_FASCICOLO_SIGE IS NOT NULL;

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
SELECT * FROM XBA_VERIF_AVV_FAS_SIEP dalla lista selezionare a campione dei procedimenti e verificare da applicativo, che al procedimento risultino collegati avvocati certificati

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
Alla fine di queste attività di aggiornamento, passare al punto 2 del paragrafo 6.1 del documento “SIUT-SIES-PR-1.3-20220422-Piano_di_Rilascio_021_RegInde_SIES.docx”.
## 3.2.7 STEP 7
In caso di errori verificatisi nell’esecuzione di uno degli step precedenti è necessario ripristinare lo snapshot effettuato all’inizio della procedura.

TUTTE LE TABELLE DI BACKUP, DI LOG E DI APPOGGIO RIPORTATE NEGLI STEP DA 1 A 6 NON DEVONO ESSERE CANCELLATE AL TERMINE DELLA PROCEDURA DI BONIFICA E MANTENUTE PER ALMENO 6 MESI, PER PERMETTERE EVENTUALI ATTIVITÀ DI VERIFICA.