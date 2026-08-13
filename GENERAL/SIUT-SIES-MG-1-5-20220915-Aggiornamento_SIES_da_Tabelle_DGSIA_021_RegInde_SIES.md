---
uniqueName: siut-sies-mg-1-5-20220915-aggiornamentosiesdatabel
displayName: "SIUT SIES MG 1 5 20220915 Aggiornamento SIES da Tabelle DGSIA 021 RegInde SIES"
category: "GENERAL"
tags: []
---

# SIUT-SIES-MG-1.5-20220915-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_SIES

> **File originale:** `MEV/SCHEDA_021/Docs/SIUT-SIES-MG-1.5-20220915-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_SIES.docx`  
> **Tipo:** DOCX

---


Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi Direzione Generale per i Sistemi Informativi Automatizzati


Aggiornamento SIES da Tabelle DGSIA
MEV 021_2019 RegInde










Versione 1.5 del 15/09/2022





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Engineering | RTI |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 15/09/2022 |  |
| Livello di riservatezza | L3 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 30/07/2021 | Prima emissione |  |
| 1.1 | 08/10/2021 | Seconda emissione | Rivista intera struttura documento |
| 1.2 | 24/01/2022 | Terza emissione | Rivista intera struttura documento |
| 1.3 | 22/04/2022 | Quarta emissione | Rivista intera struttura documento |
| 1.4 | 25/05/2022 | Quinta emissione | Eliminato cap. 4 |
| 1.5 | 15/09/2022 | Sesta Emissione | Rivista intera struttura documento |


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
3 	Descrizione delle Attività per messa in esercizio	8
3.1 Procedura di Aggiornamento Tabella SIES da Tabella fissa DGSIA	8
3.2 Istruzioni per lancio eseguibili file.sh	8
3.2.1 Attività di installazione ed esecuzione procedura batch Bonifica Difensori	8
3.3	Procedura Aggiornamento Tabelle SIES	9
3.3.1 STEP 1	9
3.3.2 STEP 2	11

# 1 	Introduzione
## 1.1 Scopo del documento
Il presente documento viene rilasciato con lo scopo di dettagliare le attività preliminari prima della messa in esercizio della MEV 021_2019 RegInde e sono relative all’aggiornamento Tabelle SIES da Tabelle fisse DGSIA.
## 1.2 Riferimenti
| Riferimento | Nome Documento | Nome Documento | Nome Documento | Nome Documento | Descrizione Documento |
| --- | --- | --- | --- | --- | --- |
| RIF1. | SIUT-SIES-PR-1.4-20220915-Piano_di_Rilascio_021_RegInde_SIES | SIUT-SIES-PR-1.4-20220915-Piano_di_Rilascio_021_RegInde_SIES | SIUT-SIES-PR-1.4-20220915-Piano_di_Rilascio_021_RegInde_SIES | SIUT-SIES-PR-1.4-20220915-Piano_di_Rilascio_021_RegInde_SIES | Piano di rilascio |
| 1.3 Glossario
1.3.1 Definizioni | 1.3 Glossario
1.3.1 Definizioni | 1.3 Glossario
1.3.1 Definizioni |  |  |  |
| Definizione | Definizione | Descrizione | Descrizione | Descrizione | Descrizione |
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
Le attività descritte indicano i passi necessari all’allineamento delle tabelle SIES COMUNE, CG_REF_CODES, relativamente ai Domini PROVINCIA, REGIONE e NAZIONE, e CODICI_SIES_NSC, relativamente ai Domini COMUNE e NAZIONE e sono preliminari alle attività di installazione del software relativo alla MEV 021_2019 RegInde di SIES.

# 3 	Descrizione delle Attività per messa in esercizio
Le attività descritte nel paragrafo 3.1 si articolano su scripts .sql e procedures plsql, contenuti nel pacchetto  aggiorna_db.zip, che va estratto ottenendo la cartella ..\aggiorna_db.
## 3.1 Procedura di Aggiornamento Tabella SIES da Tabella fissa DGSIA
Di seguito l’attività da eseguire per l’aggiornamento delle tabelle SIES da quelle fornite da DGSIA, ricevute tramite e-mail di Anna.Maffucci@giustizia.it a Vito.Bufi@eng.it del 6/11/2020 09:06.
## 3.2 Istruzioni per lancio eseguibili file.sh
Aprire una shell linux sul server SIES e loggarsi come utente “root”;
Eseguire il comando: “cd /etc/init.d”;
Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”;
Fermare il processo di gestione delle code tramite il comando: “./imq stop”;
## 3.2.1 Attività di installazione ed esecuzione procedura batch Bonifica Difensori
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
Copiare il file aggiorna_db.zip in una qualsiasi cartella e scompattarlo. il sistema crea la cartella aggiorna_db;
Creare sul server DB una cartella MEV-2019_21 sotto la directory /home/oracle/;
Copiare la cartella aggiorna_db nella cartella /home/oracle/MEV-2019_21/.
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella MEV-2019_21 tramite il comando:
chmod 777 MEV-2019_21

In fase di esecuzione degli script, di seguito riportati, saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta (dove xx è la sigla del distretto di appartenenza, per esempio siesrm per Roma):
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx

Posizionarsi nel percorso /home/oracle/MEV-2019_21/; lanciare sequenzialmente i comandi, indicati nel par. 3.3.
## Procedura Aggiornamento Tabelle SIES
Di seguito le attività da eseguire per l’aggiornamento della tabella COMUNE, dei Domini PROVINCIA, REGIONE e NAZIONE della tabella CG_REF_CODES, dei Domini COMUNE e NAZIONE della tabella CODICI_SIES_NSC alle tabelle fisse COMUNE, PROVINCIA, REGIONE e STATO-NAZIONE fornite dalla DGSIA.
N.B. In caso di esito negativo di una o più verifiche riportate nei successivi STEP, affinché si possa ripristinare il database alla situazione iniziale, utilizzare lo snapshot del DB creato nel paragrafo 3.2 del documento “SIUT-SIES-MG-1.5-20220915-Istruzioni_Bonifica_Difensori_021_RegInde_SIES.docx”.
## 3.3.1 STEP 1
Verificare tramite il comando pwd di trovarsi nel percorso /home/oracle/MEV-2019_21/ ed eseguire il comando

./aggiorna_db.sh

Dettaglio del file:
XAT_SALVA_TABELLE_PRE_ALLINEA.prc = Crea e compila la procedure XAT_SALVA_TABELLE_PRE_ALLINEA, che esegue una copia di backup delle tabelle COMUNE, CG_REF_CODES e CODICI_SIES_NSC nelle tabelle COMUNE_SXALLTF, CG_REF_CODES_SXALLTF e CODICI_SIES_NSC_SXALLTF.
Alter_Comune.sql = lo script .sql aggiunge all’attuale struttura della tabella COMUNE le nuove colonne COD_CATASTALE_COMUNE, DATA_AGGIORNAMENTO_COMUNE, DATA_FINE_VALIDITA_COMUNE.
Aggiornamento_TABELLA_COMUNE_esercizio.sql = Lo script effettua l’aggiornamento della tabella COMUNE, cancellando  i preesistenti 8112 records e ne inserisce 13327.
Aggiornamento_CG_REF_CODES_PROVINCIA_esercizio.sql = Lo script che cancella dalla tabella CG_REF_CODES i records aventi RV_DOMAIN = ‘PROVINCIA’ e carica i nuovi records. Il dominio conterrà 117 records a fronte dei 105 precedenti.
Insert_REGIONE.sql = Lo script inserisce un nuovo record (LUOGO_SCONOSCIUTO) nella tabella CG_REF_CODES per RV_DOMAIN = ‘REGIONE’.
Aggiornamento_CG_REF_CODES_NAZIONE_esercizio.sql = Lo script cancella dalla tabella CG_REF_CODES i records aventi RV_DOMAIN = ‘NAZIONE’ e carica i nuovi records. Il dominio conterrà 269 records a fronte dei 200 precedenti.
Alter_CODICI_SIES_NSC.sql = Lo script modifica la constraint attuale, che è costituita dalle colonne (CO_DOMAIN, CO_CODCENTR), alla nuova costituita da (CO_DOMAIN, CO_CODCENTR, CO_SIES) per permettere la gestione di comuni omonimi, che pur avendo lo stesso valore di CO_CODCENTR hanno diverso valore del CO_SIES.
Aggiornamento_CODICI_SIES_NSC_COMUNE_esercizio.sql = Lo script cancella dalla tabella CODICI_SIES_NSC i records aventi CO_DOMAIN = ‘COMUNE’ e carica i nuovi records. Il dominio conterrà 8607 records a fronte degli 8145 precedenti.
Aggiornamento_CODICI_SIES_NSC_NAZIONE_esercizio.sql = Lo script cancella dalla tabella CODICI_SIES_NSC i records aventi CO_DOMAIN = ‘NAZIONE’ e carica i nuovi records. Il dominio conterrà 204 records a fronte dei 201 precedenti.
Disabilita_Funzioni_Inserimento_Modifica_Difensore.sql = Lo script disabilita le funzioni Inserimento e Modifica Difensore in Funzioni Amministrative/Gestione Difensori.
Insert_FUNZIONE-FUNZIONE_PROFILO.sql = Lo script inserisce nelle tabelle FUNZIONE e FUNZIONE_PROFILO i records necessari ad abilitare le nuove funzionalità necessarie alla Ricerca e alla gestione dell’Avvocato su ReGIndE e alla gestione della nuova struttura delle tabella COMUNE e CODICI_SIES_NSC.
aggiorna_versione.sql = Lo script inserisce il record con la descrizione della nuova release nella tabella VERSIONE.

Per ogni punto precedente sono riportati di seguito gli eventuali controlli per verificare la corretta esecuzione di aggiorna_db.sh:

Verificare che nel file /home/oracle/MEV-2019_21/log/ Log_Aggiorna_DB.log non siano riportati errori oracle;

Collegarsi al database con utenza siesxx (dove xx è la sigla del distretto di appartenenza, per esempio siesrm per Roma):

E’ possibile verificare la corretta esecuzione della procedura XAT_SALVA_TABELLE_PRE_ALLINEA.prc eseguendo la query

SELECT * FROM USER_TABLES A WHERE A.TABLE_NAME LIKE '%_SXALLTF' ORDER BY TABLE_NAME
che deve dare come esito le seguenti tabelle CG_REF_CODES_SXALLTF, CODICI_SIES_NSC_SXALLTF e
COMUNE_SXALLTF.

Per verificare l’aggiornamento effettuato al secondo punto eseguire quanto di seguito
SELECT * FROM COMUNE
verificare presenza delle colonne COD_CATASTALE_COMUNE, DATA_AGGIORNAMENTO_COMUNE, DATA_FINE_VALIDITA_COMUNE.

Per verificare l’aggiornamento effettuato al terzo punto eseguire quanto di seguito
SELECT COUNT(*) FROM COMUNE           il risultato deve essere 13327.
SELECT COUNT(*) FROM COMUNE_SXALLTF        il risultato deve essere 8112.

Per verificare l’aggiornamento effettuato al quarto punto eseguire quanto di seguito
SELECT COUNT(*) FROM CG_REF_CODES WHERE RV_DOMAIN = 'PROVINCIA'      il risultato deve essere 117.

Per verificare l’aggiornamento effettuato al quinto punto eseguire quanto di seguito
SELECT * FROM CG_REF_CODES WHERE RV_DOMAIN = 'REGIONE'
verificare che nell’elenco sia presente il record con RV_LOW_VALUE = 21

Per verificare l’aggiornamento effettuato al sesto punto eseguire quanto di seguito
SELECT COUNT (*) FROM CG_REF_CODES WHERE RV_DOMAIN = 'NAZIONE'
il risultato deve essere  269.

Per verificare l’aggiornamento effettuato al settimo punto eseguire accedere alla tabella CODICI_SIES_NSC e verificare che la constraint CODICI_SIES_NSC_PK sia formata dalle colonne CO_DOMAIN, CO_CODCENTR e CO_SIES.

Per verificare l’aggiornamento effettuato all’ottavo punto eseguire quanto di seguito
SELECT COUNT(*) FROM CODICI_SIES_NSC WHERE CO_DOMAIN = 'COMUNE'
il risultato deve essere 8607.

Per verificare l’aggiornamento effettuato al nono punto eseguire quanto di seguito
SELECT COUNT(*) FROM CODICI_SIES_NSC WHERE CO_DOMAIN = 'NAZIONE'
il risultato deve essere 204.

Per verificare l’aggiornamento effettuato al decimo punto eseguire quanto di seguito
SELECT * FROM RELAZIONE_FUNZIONE WHERE FUN_ID_FUNZIONE IN ('41','11040012') AND FUN_ID_FUNZIONE_FIGLIA = '11040010'
che non deve estrarre alcun record.

In caso di esito positivo delle su riportate attività LE TABELLE DI BACKUP CREATE AL PUNTO 1 NON DEVONO ESSERE CANCELLATE MA VANNO MANTENUTE PER ALMENO 6 MESI, PER PERMETTERE EVENTUALI ATTIVITÀ DI VERIFICA.

Alla fine di queste attività di aggiornamento, passare al punto 3 del paragrafo 6.1 del documento “SIUT-SIES-PR-1.4-20220915-Piano_di_Rilascio_021_RegInde_SIES.docx”.
## 3.3.2 STEP 2
In caso di errori verificatisi nell’esecuzione di uno degli step precedenti è necessario ripristinare lo snapshot citato all’inizio della procedura.