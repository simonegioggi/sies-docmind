---
uniqueName: siut-sies-pr-1-0-20191206-piano-di-rilascio-sies
displayName: "SIUT SIES PR 1 0 20191206 Piano di rilascio SIES"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20191206-Piano di rilascio SIES

> **File originale:** `RILASCIO_11.2.3/SIUT-SIES-PR-1.0-20191206-Piano di rilascio SIES.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
Piano di rilascio 
 
 
 
 
 
 
 
 
 
Versione 1.0 del 06/12/2019

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20191206 Piano di rilascio SIES 
Ver. 1.0 del 06/12/2019 
Pag. 2/15 
 
 
 
Il presente documento è stato redatto con la collaborazione 
del RTI Engineering Ingegneria Informatica S.p.A - Sirfin-PA, 
nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del 
sistema informativo unitario telematico, la manutenzione 
degli attuali sistemi dell’area penale del Ministero della 
Giustizia e servizi correlati. Lotto 1”.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20191206 Piano di rilascio SIES 
Ver. 1.0 del 06/12/2019 
Pag. 3/15 
Elenco approvazioni 
 
Versione 
V. 1.0 del 06/12/2019 
Redatto da: 
Domenico Nania, Simone Gioggi 
Verificato da: 
Vito Nicola Bufi 
Approvato da: 
Vito Nicola Bufi 
Data approvazione: 
06/12/2019 
Livello di riservatezza: 
L4 
 
Lista di distribuzione 
Nominativo 
Organizzazione 
Ufficio 
Ruolo 
Ing. Giovanni Malesci 
Amministrazione 
 
Responsabile Unico Procedimento 
Dr.ssa Anna Maria Palmieri 
Amministrazione 
 
Direttore Esecutivo Contratto 
Paolo Ceccanti 
RTI 
 
Responsabile Unico Fornitura 
Pasquale Lamattina 
RTI 
 
Referente Tecnico 
Vito Bufi 
RTI 
 
Responsabile Manutenzione Sistemi attuali 
Fabio Mazzocchi 
RTI 
 
Responsabile Manutenzione Correttiva 
Antonella Damiani 
RTI 
 
Responsabile Centro di Competenza 
Alessandro Falleni 
RTI 
 
Referente sicurezza 
Fabio Gattamorta 
RTI 
 
PMO 
Edoardo Lamuraglia 
RTI 
 
Referente qualità 
Francesco Rosati 
RTI 
 
Referente qualità 
 
Elenco versioni 
Versione 
Data  
Motivo 
Modifica 
1.0 
06/12/2019 
Prima Emissione

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20191206 Piano di rilascio SIES 
Ver. 1.0 del 06/12/2019 
Pag. 4/15 
INDICE DEI CONTENUTI 
1 
INTRODUZIONE ...................................................................................................................................... 5 
1.1 
SCOPO DEL DOCUMENTO .................................................................................................................................. 5 
1.2 
ACRONIMI E DEFINIZIONI .................................................................................................................................. 5 
1.2.1 
Acronimi .............................................................................................................................................................. 5 
1.2.2 
Definizioni ............................................................................................................................................................ 6 
1.3 
RIFERIMENTI ................................................................................................................................................... 6 
2 
GENERALITÀ .......................................................................................................................................... 7 
3 
IDENTIFICAZIONE DEGLI ELEMENTI RILASCIATI ........................................................................................ 8 
4 
RIFERIMENTI DEGLI OGGETTI DEL RILASCIO ............................................................................................ 9 
5 
DETTAGLIO DEGLI ELEMENTI SW OGGETTO DEL RILASCIO ...................................................................... 11 
6 
INSTALLAZIONE ..................................................................................................................................... 12 
6.1 
ATTIVITÀ PRELIMINARI .................................................................................................................................... 12 
6.2 
INSTALLAZIONE LATO DB ORACLE ..................................................................................................................... 12 
6.2.1 Esecuzione Script ...................................................................................................................................................... 12 
6.3 
INSTALLAZIONE APPLICAZIONE .......................................................................................................................... 14 
6.3.1 Deploy Applicazione ................................................................................................................................................. 14

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20191206 Piano di rilascio SIES 
Ver. 1.0 del 06/12/2019 
Pag. 5/15 
1 Introduzione 
1.1 Scopo del documento 
Il documento descrive il piano di rilascio del sistema SIES. 
Gli interventi in oggetto sono rilasciati nell’ambito della release 11.2.3 SIES. 
1.2 Acronimi e Definizioni 
1.2.1 
Acronimi 
Sigla 
Descrizione 
AgID 
Agenzia per l’Italia Digitale 
API 
Application Programming Interface 
CPU 
Central Processing Unit 
CV 
Curriculum Vitae 
DB 
Data Base 
DEC 
Direttore Esecutivo Contratto 
DGSIA 
Direzione Generale per o Sistemi Informativi Automatizzati 
DR 
Disaster Recovery 
ETSI 
European Telecommunications Standards Institute 
FP 
Function Point 
GDPR 
General Data Protection Regulation 
HW 
HardWare 
ICT 
Information & Communication Technology 
ISO 
International Organization for Standardization 
ISP
Information Security Policy
IT 
Information Technology 
KPI
Key Performance Indicator
MAAC 
Mandatory Access Control 
MAC
MAnutenzione Correttiva
MEV 
Manutenzione EVolutiva 
OSWAP
Open Web Application Security Project
PA 
Pubblica Amministrazione 
PEC
Posta Elettronica Certificata
PDCA 
Plan, Do, Check, Act 
PdQ
Piano della Qualità
PdP 
Piano di Progetto 
PdS
Piano della Sicurezza
QM 
Quality Manager 
RA
Risk Assessment
RID 
Riservatezza, Integrità, Disponibilità 
RM
Resource Manager
RPO 
Recovery Point Objective 
RTO
Recovery Time Objective
RTI 
Raggruppamento Temporaneo di Impresa Engineering – Sirfin-PA 
RUF
Responsabile Unico Fornitore
RUP 
Responsabile unico Progetto 
SAL 
Stato Avanzamento Lavori 
SGQ 
Sistema di Gestione per la Qualità di Engineering Ingegneria Informatica S.p.A.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20191206 Piano di rilascio SIES 
Ver. 1.0 del 06/12/2019 
Pag. 6/15 
Sigla 
Descrizione 
SGSI 
Sistema di Gestione della Sicurezza Informatica 
SICP
Sistema Informativo Cognizione Penale
SIU 
Sistema Informativo Unitario 
SLA 
Service Level Agreement 
SM 
Security Manager 
SQL 
Structured Query Language 
SW 
SoftWare 
TT 
Trouble Ticketing 
VPN 
Virtual Private Network 
1.2.2 
Definizioni 
Glossa 
Sinonimo 
Definizione 
 
 
 
 
 
 
 
 
 
1.3 Riferimenti 
Riferimento 
Nome Documento 
Descrizione Documento 
RIF1
SIUT-SIES-PT-1.0-20191206-Piano-dei-
Test.pdf 
Il documento descrive il piano dei test per la 
verifica della risoluzione dei ticket indicati 
nel presente Piano di Rilascio 
RIF2 
SIUT-SIES-CT-1.0-20191206-Allegato-al-
piano-test.xls 
Il documento riporta l'elenco dei test 
eseguiti per la verifica della risoluzione delle 
anomalie

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20191206 Piano di rilascio SIES 
Ver. 1.0 del 06/12/2019 
Pag. 7/15 
2 Generalità 
Il presente documento riporta l’elenco delle funzionalità modificate con gli interventi eseguiti dal servizio di 
manutenzione rilasciati con il presente rilascio.  
Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20191206 Piano di rilascio SIES 
Ver. 1.0 del 06/12/2019 
Pag. 8/15 
3 Identificazione degli elementi rilasciati 
Supporto 
n° 
Oggetti: 
Rev. del 
Portale della Fornitura 
1 
Company Home > SIUT > 06 - Rilasci Software > SIES > 
Rilascio V11.2.3 2019-12-06 
1.0 
06/12/2019 
Note-osservazioni

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20191206 Piano di rilascio SIES 
Ver. 1.0 del 06/12/2019 
Pag. 9/15 
4 Riferimenti degli oggetti del rilascio 
Tipo di 
Intervento
Rif. Ticket 
OTRS 
Anomalia Segnalata 
Descrizione Soluzione 
MAC 
20191108014 
SIUS - Problema 
cancellazione note dopo 
scarico ordinanza di rinvio 
udienza 
Aggiunta valorizzazione attributo annotazione; 
modificate le classi 
"LoadInserisciOrdinanzaRinvioUdienza.jsp" e 
"ActLoadInserisciOrdinanzaRinvioUdienza.java". 
 
MAC 
20191115013 
SIGE - La pagina iniziale del 
fascicolo non visualizza le 
date di rinvio delle udienze
la data udienza deve essere visibile anche per tipo 
provvedimento 'Rinvio udienza da verbale' ('50') 
MAC 
20191112011 
SIEP – Emissione 
liberazione anticipata per 
detenuto agli arresti 
domiciliari  
adesso per la posizione giuridica 'Arresti Domiciliare ex 
art 89 dpr 309/90 - ex art. 656 comma 10 cpp' ('84') 
viene caricata la stessa pagina della posizione giuridica 
'Arresti domiciliari ex art.656/10' ('02') 
MAC
20191108016
Soggetto presentante
Realizzata una procedura oracle di bonifica dati
MAC 
201911140122
"Errore bloccante nella 
generazione della stampa 
del provvedimento 
relativo al ""Dettaglio 
Detenzione Domiciliare a 
Termine""" 
Modificato il template SIEP_MA_DETERM_DET.rtf 
MAC 
20191128014 
Non fornisce lo 
scadenziario per DS 
notificato con Decreto 
Irreperibilità 
Modificata la classe "OrdineEsecuzioneController.java"
 
MAC 
20191106018 
DECRETI IRREPERIBILITA' 
LEGGE SIMEONE 
Modificata la classe "OrdineEsecuzioneController.java"
MAC 
20191122012 
"Errore bloccante nella 
generazione della stampa 
del provvedimento 
relativo al ""Dettaglio 
Detenzione Domiciliare a 
Termine" 
Modificato il template SIEP_MA_DETERM_DET.rtf 
 
MAC 
201911260110 Errore su template post 
patch 
Modificato il template 
SIEP_CUMULO_OE_656_LIB_C10_TRAD.rtf 
MAC 
201911250110
Errore bloccante Tribunale 
di Sorveglianza dei 
Minorenni di Roma il 
sistema non riconosce 
l’Ufficio del Magistrato di 
Sorveglianza per i 
Minorenni di Roma 
quando viene formato un 
fascicolo E.M.A. sul fasc. 
portante 
Modificate le classi "LoadIscrProcedimentoUDS.jsp" e 
"ActInsFascicoloDaSiusUDS.java" 
 
MAC
20191122014
Sige - Tribunale Ricorsi in 
Realizzata una procedura oracle di bonifica dati

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20191206 Piano di rilascio SIES 
Ver. 1.0 del 06/12/2019 
Pag. 10/15 
Tipo di 
Intervento
Rif. Ticket 
OTRS 
Anomalia Segnalata 
Descrizione Soluzione 
Cassazione
MAC 
20191122013 
SIGE - Corte D'Appello -
Errata indicazione del 
depositante nel ricorso per 
cassazione 
Realizzata una procedura oracle di bonifica dati 
MAC 
20191114019 
SIES - mancata 
registrazione data inizio 
misura 
Modificate le classi 
"ActLoadInserisciVariazioneVerbaleSottoscrizione.java" 
e "ActLoadInserisciVerbaleSottoscrizione.java" 
MAC 
20191112019 
2019-11 Ancona Procura 
Minori non fa caricare 
inizio misura 
Modificate le classi 
"ActLoadInserisciVariazioneVerbaleSottoscrizione.java" 
e "ActLoadInserisciVerbaleSottoscrizione.java"

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20191206 Piano di rilascio SIES 
Ver. 1.0 del 06/12/2019 
Pag. 11/15 
5 Dettaglio degli elementi sw oggetto del rilascio 
 
 
Dimensione 
Motivazione-riferimento 
Nome File 
Path 
(MB) 
Aggiorna_db.zip 
Database 
 
Script per risoluzione delle anomalie 
template.zip
Template
Nuovi template per risoluzione anomalie 
segnalate: 
SIEP_CUMULO_OE_656_LIB_C10_TRAD.rtf
SIEP_MA_DETERM_DET.rtf 
sies.war 
Applicazione 
104 
 
Eseguibile dell’applicazione 
Sorgenti.zip
Sorgenti
100
Sorgenti software
documentazione.zip
Documentazione
SIUT-SIES-CT-1.0-20191206-Allegato-al-
piano-test.xls 
 
SIUT-SIES-PR-1.0-20191206-Piano di 
rilascio SIES.pdf 
 
SIUT-SIES-PT-1.0-20191206-Piano-dei-
Test.pdf 
Note-osservazioni

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20191206 Piano di rilascio SIES 
Ver. 1.0 del 06/12/2019 
Pag. 12/15 
6 Installazione 
6.1 
Attività Preliminari 
1 - Arrestare il servizio MessageQueue e stoppare il webserver jboss (dopo avere avvertito gli utenti degli uffici 
che lavorano sul SIES). 
2 - Verificare che il tnsnames.ora sia presente sul db server e configurato correttamente per l’accesso al DB da 
aggiornare. 
6.2 
Installazione lato DB Oracle 
6.2.1 Esecuzione Script 
(E’ consigliato che tale procedura venga eseguita da personale competente in ambiente Oracle) 
Il documento elenca i passi necessari per la corretta esecuzione.  
 
Accedere ad Oracle (con qualsiasi strumento tipo toad, developer …) come utente siesxx ed eseguire le seguenti 
attività: 
 
• 
lanciare la seguente query: 
 
SELECT s.soggetto_impugnante cod, r.rv_meaning tipo_soggetto, COUNT(*) conteggio 
FROM impugnazione_sige s, cg_ref_codes r 
WHERE to_date(to_char(s.DATA_AGGIORNAMENTO, 'dd/mm/yyyy'), 'dd/mm/yyyy') >= 
to_date('xx/xx/xxxx', 'dd/mm/yyyy') 
AND to_date(to_char(s.DATA_AGGIORNAMENTO, 'dd/mm/yyyy'), ' dd/mm/yyyy') <= 
SYSDATE 
AND r.rv_low_value = s.soggetto_impugnante 
AND r.rv_domain = 'SOGGETTO_IMPUGNANTE_SIGE' 
GROUP BY s.soggetto_impugnante, r.rv_meaning 
 
NB:  nel campo ‘xx/xx/xxxxx’  deve essere indicata la data in cui è stata installata la versione 
11.2.1 del SIES. 
 
• 
Il risultato restituito sarà simile a quello indicato nella seguente figura: 
 
 
 
• 
Salvare il risultato ottenuto dalla query in un foglio excel (es: datiPreBonifica.xls) 
• 
Effettuare il backup della tabella ‘impugnazione_sige’. 
• 
Effettuare il backup della tabella ‘cg_ref_codes’. 
 
Collegarsi come utente oracle sul db server. 
Impostare le variabili ORACLE_HOME e ORACLE_SID (se non già settate) eseguendo le seguenti istruzioni:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20191206 Piano di rilascio SIES 
Ver. 1.0 del 06/12/2019 
Pag. 13/15 
 
(il percorso varia in base all’installazione di oracle) 
export ORACLE_HOME=/u01/app/oracle/product/12.1.0/dbhome_1 
 
(sostituire xxxxx col nome dell’istanza oracle) 
export ORACLE_SID=xxxxx 
 
aggiungere nella variabile PATH $ORACLE_HOME/bin 
 
esempio  
 
PATH=$PATH:/u01/app/oracle/product/12.1.0/dbhome_1/bin 
 
Prima di avviare la procedura, accertarsi che sia il listener che il database siano avviati. 
 
Copiare il file aggiorna_db.zip  in una qualsiasi cartella e scompattarlo, il sistema crea la cartella aggiorna_db. 
Creare sul server DB una cartella V_11_2_3 sotto la directory /home/oracle/ 
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/ V_11_2_3/ 
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella V_11_2_3 tramite il comando: 
chmod 777 V_11_2_3 
 
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta: 
================================================== 
Riassunto dei dati immessi per questa installazione 
Nome ....................: sies 
================================================== 
SID Oracle ..............: sies 
Utente_SIES..............: siesxx 
Password_SIES............: siesxx 
 
Nella cartella appena creata (V_11_2_3), lanciare il comando ./aggiorna_db.sh 
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/ V_11_2_3/log/ in cui si può 
constatare l’esito dell’esecuzione. 
N.B. Le segnalazioni del tipo  
ORA-00001: violata restrizione di unicità 
ORA-00955: name is already used by an existing object 
Cartella log già presente 
ORA-04043: object does not exist 
 
sono da considerarsi warning e non errori. 
 
Accedere ad oracle (con qualsiasi strumento tipo toad, developer…) come utente siesxx e compilare tutte le 
procedure e i package che non risultano compilate. 
ATTENZIONE: la procedura SUPER_SOGGETTO_PREGR e il package CARICA_RES potrebbero restare non 
compilate: non è da considerarsi errore. 
 
Una volta terminata l’esecuzione eseguire le seguenti attività:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20191206 Piano di rilascio SIES 
Ver. 1.0 del 06/12/2019 
Pag. 14/15 
• 
Eseguire la procedura ‘bonifica_soggetto_presentante(data_versione IN VARCHAR2)’, andando a 
specificare nel campo ‘data_versione’ la data in cui è stata installata la versione 11.2.1 del SIES. 
 
Per l’esecuzione della procedura, lanciare il seguente comando: 
 
execute bonifica_soggetto_presentante('xx/xx/xxxx'); 
 
 
NB:  nel campo ‘xx/xx/xxxxx’  deve essere indicata la data in cui è stata installata la versione 
11.2.1 del SIES. 
 
 
• 
Eseguire nuovamente la query riportata al primo punto elenco. 
• 
Il risultato restituito sarà simile a quello indicato nella seguente figura: 
 
 
 
• 
Salvare il risultato ottenuto dalla query in un foglio excel (es: datiPostBonifica.xls). 
• 
Effettuare un confronto tra i due files excel salvati precedentemente e verificare che in corrispondenza 
del TIPO_SOGGETTO, il conteggio sia il medesimo. Ciò che deve differire tra i due file è solo il valore 
della colonna COD (codice), infatti la bonifica si limita a cambiare solo il codice associato al tipo soggetto 
presentante. 
 
Per dati uguali si può dire che la bonifica ha avuto esito positivo. 
 
Nella casistica in cui non ci sia corrispondenza tra i conteggi ottenuti nella query pre bonifica e post 
bonifica, si può dedurre che la bonifica non ha avuto esito positivo. In tal caso procedere con le seguenti 
attività: 
 
- 
Ripristinare la tabella cg_ref_codes con il backup eseguito precedentemente. 
- 
Ripristinare la tabella impugnazione_sige con il backup eseguito precedentemente. 
 
6.3 
Installazione applicazione 
6.3.1 Deploy Applicazione 
• 
Aprire una shell linux sul server SIES e loggarsi come utente “root”. 
• 
Eseguire il comando: “cd /etc/init.d” e fermare il processo di gestione delle code tramite il comando: 
“./imq stop” (già indicato nelle attività preliminari).

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIES-PR-1.0-20191206 Piano di rilascio SIES 
Ver. 1.0 del 06/12/2019 
Pag. 15/15 
• 
Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione 
dell’istruzione tramite il comando: “service jboss status” (già indicato nelle attività preliminari). 
• 
Scaricare i files “sies.war” sul server SIES ed eseguire le seguenti operazioni: 
• 
posizionarsi sotto la cartella: 
“/opt/jboss-eap-6.4/standalone/deployments”; 
• 
cancellare il vecchio eseguibile (se esistente) “sies.war” e la copia deployata “sies.war.deployed”; 
• 
copiare, nello stesso percorso, il nuovo eseguibile “sies.war”; 
• 
posizionarsi sotto la cartella: 
“/opt/jboss-eap-6.4/standalone”; 
• 
cancellare le cartelle “data”, “log” e “tmp” (se esistenti). 
• 
Copiare il file contenuto nella cartella template\siep\ma 
nella cartella “/var/SIES/template/siep/ma” sovrascrivendo quello precedente. 
• 
Copiare il file contenuto nella cartella template\siep\cumulo 
nella cartella “/var/SIES/template/siep/cumulo” sovrascrivendo quello precedente. 
 
Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le 
istruzioni ai punti 4.b e 4.e. All’avvio, infatti, tali cartelle verranno ricreate. 
 
• 
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione 
dell’istruzione tramite il comando: “service jboss status”. 
• 
Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.