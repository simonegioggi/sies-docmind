---
uniqueName: siut-sies-pr-1-6-20221125-pianodirilascio021regind
displayName: "SIUT SIES PR 1 6 20221125 Piano di Rilascio 021 RegInde SIES"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.6-20221125-Piano_di_Rilascio_021_RegInde_SIES

> **File originale:** `MEV/SCHEDA_021/Docs/SIUT-SIES-PR-1.6-20221125-Piano_di_Rilascio_021_RegInde_SIES.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati
 
 
 
Piano di Rilascio 
MEV-2019_021 
 
 
 
 
 
 
 
 
 
Versione 1.6 del 25/11/2022

Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
SIUT-SIES-PR-1.6-20221125-Piano_di_Rilascio_021_RegInde_SIES 
Ver. 1.6 del 25/11/2022 
Pag. 2/14 
 
 
Il 
presente 
documento 
è 
stato 
redatto 
con 
la 
collaborazione 
del 
RTI 
Engineering 
Ingegneria 
Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del 
contratto CIG 73479643B7 per lo “Sviluppo del Sistema 
Informativo Unitario Telematico, la manutenzione 
degli attuali sistemi dell’area Penale del Ministero 
della Giustizia e servizi correlati. Lotto 1”.

Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
SIUT-SIES-PR-1.6-20221125-Piano_di_Rilascio_021_RegInde_SIES 
Ver. 1.6 del 25/11/2022 
Pag. 3/14 
Approvazioni 
 
 
Nominativo 
Funzione 
Elaborato da 
Engineering 
RTI 
Verificato da 
Vito Bufi 
Responsabile Manutenzione Sistemi attuali
Approvato da 
Paolo Ceccanti 
Responsabile Unico Fornitura 
Data approvazione 
25/11/2022 
 
Livello di riservatezza 
L4 
 
 
Elenco versioni 
Versione 
Data  
Motivo 
Modifica 
1.0 
30/07/2021 
Prima Emissione 
 
1.1 
08/10/2021 
Seconda Emissione 
Revisione Completa 
1.2 
24/01/2022 
Terza Emissione 
Revisione Completa 
1.3 
22/04/2022 
Quarta Emissione 
Revisione Completa 
1.4 
15/09/2022 
Quinta Emissione 
Modificati i riferimenti ai documenti di bonifica ed 
aggiornamento; corretta la versione di installazione 
del SIES 
1.5 
11/11/2022 
Sesta Emissione 
Modificati i riferimenti al documento di bonifica 
difensori ed inglobato il documento di aggiornamento
SIES da tabelle DGSIA; corretta la versione di 
installazione del SIES 
1.6 
25/11/2022 
Settima Emissione 
Modificati i riferimenti a pag. 10; corretto elenco pag. 
12 
 
Lista di distribuzione 
Nominativo 
Organizzazione 
Ufficio 
Funzione 
Ing. Giovanni Malesci 
Amministrazione 
 
Responsabile Unico Procedimento 
Dott. Oris Orlando 
Amministrazione 
 
Direttore Esecutivo Contratto 
Paolo Ceccanti 
RTI 
 
Responsabile Unico Fornitura 
Sergio Tamburrini 
RTI 
 
Organization Manager 
Vito Bufi 
RTI 
 
Responsabile Manutenzione Sistemi attuali 
Francesco Rosati 
RTI 
 
Responsabile Manutenzione Correttiva 
Referente Qualità e Sicurezza 
Andrea Salvaggio 
RTI 
 
Responsabile Progetto Sistema Unitario 
Referente Tecnico 
Antonio Iacobelli 
RTI 
 
Responsabile Supporto Specialistico 
Antonella Damiani 
RTI 
 
Responsabile Centro di Competenza 
Fabio Gattamorta 
RTI 
 
Referente PMO e Qualità 
Alessandro Falleni 
RTI 
 
Referente sicurezza 
Andrea Castorino 
RTI 
 
Referente Applicativo Gestore Fascicolo 
Documentale

Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
SIUT-SIES-PR-1.6-20221125-Piano_di_Rilascio_021_RegInde_SIES 
Ver. 1.6 del 25/11/2022 
Pag. 4/14 
INDICE DEI CONTENUTI 
1. 
INTRODUZIONE ..................................................................................................................... 5 
1.1 
SCOPO DEL DOCUMENTO ................................................................................................................... 5 
1.2 
RIFERIMENTI.................................................................................................................................... 5 
1.3 
GLOSSARIO ..................................................................................................................................... 5 
1.3.1 
DEFINIZIONI ................................................................................................................................. 5 
1.3.2 
ACRONIMI E ABBREVIAZIONI ............................................................................................................ 5 
2. 
GENERALITÀ .......................................................................................................................... 6 
3. 
IDENTIFICAZIONE DEGLI ELEMENTI RILASCIATI ...................................................................... 7 
4. 
RIFERIMENTI DEGLI OGGETTI DEL RILASCIO ........................................................................... 8 
4.1 
RIFERIMENTI ANOMALIA (MAC/GAR) ................................................................................................ 8 
4.2 
RIFERIMENTI CHANGEREQUEST (ADE/MEV) ........................................................................................ 8 
5. 
DETTAGLIO DEGLI ELEMENTI OGGETTO DEL RILASCIO ............................................................ 9 
6. 
INSTALLAZIONE ................................................................................................................... 10 
6.1 
PREREQUISITI ................................................................................................................................ 10 
6.2 
ATTIVITÀ DI INSTALLAZIONE ED ESECUZIONE PROCEDURA BATCH BONIFICA DIFENSORI .................................. 10 
6.3 
PROCEDURA DI AGGIORNAMENTO TABELLA SIES DA TABELLA FISSA DGSIA .............................................. 10 
6.3.1 
ATTIVITÀ DI INSTALLAZIONE ED ESECUZIONE PROCEDURA BATCH AGGIORNAMENTO TABELLA SIES DA TABELLA 
FISSA DGSIA ........................................................................................................................................... 10 
6.3.2 
PROCEDURA AGGIORNAMENTO TABELLE SIES - STEP 1 ..................................................................... 11 
6.3.3 
PROCEDURA AGGIORNAMENTO TABELLE SIES - STEP 2 ..................................................................... 12 
6.4 
INSTALLAZIONE APPLICAZIONE ........................................................................................................... 13 
6.4.1 
DEPLOY APPLICAZIONE ................................................................................................................. 13 
6.5 
ATTIVITÀ DI CONFIGURAZIONE ........................................................................................................... 14 
6.6 
ATTIVITÀ DI POST-INSTALLAZIONE ...................................................................................................... 14

Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
SIUT-SIES-PR-1.6-20221125-Piano_di_Rilascio_021_RegInde_SIES 
Ver. 1.6 del 25/11/2022 
Pag. 5/14 
1. Introduzione 
1.1 Scopo del documento 
Il presente documento descrive il piano di rilascio degli interventi realizzati nell’ambito del Sistema Integrato 
Esecuzione Sorveglianza per la realizzazione di quanto dettagliato nella scheda di intervento di riferimento. 
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.7.1.0-MEV_2019_021 di SIES. 
Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio. 
1.2 Riferimenti 
Riferimento 
Nome Documento 
Descrizione Documento 
RIF1. 
SIUT-SIE-SI-2.6-20220422-Specifiche-intervento-021-SIES.pdf 
Scheda Intervento 
RIF2. 
SIUT-SIES-MG-1.7-20221125-
Istruzioni_Bonifica_Difensori_021_RegInde_SIES.pdf 
Manuale Gestione 
1.3 Glossario 
1.3.1 Definizioni 
Definizione 
Descrizione 
 
 
1.3.2 Acronimi e abbreviazioni 
Sigla 
Descrizione 
DB 
Data Base 
DEC 
Direttore Esecutivo Contratto 
DGSIA 
Direzione Generale per i Sistemi Informativi Automatizzati 
FP 
Function Point 
GdL 
Gruppo di Lavoro 
HW 
HardWare 
MAC 
MAnutenzione Correttiva 
MEV 
Manutenzione EVolutiva 
PA 
Pubblica Amministrazione 
PEC 
Posta Elettronica Certificata 
RTI 
Raggruppamento Temporaneo di Impresa 
RUF 
Responsabile Unico Fornitore 
RUP 
Responsabile Unico Progetto 
SW 
SoftWare

Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
SIUT-SIES-PR-1.6-20221125-Piano_di_Rilascio_021_RegInde_SIES 
Ver. 1.6 del 25/11/2022 
Pag. 6/14 
2. Generalità 
Il presente documento descrive il piano di rilascio del software relativo alla MEV-2019_021 di SIES, contenente 
l’integrazione della suddetta MEV con la versione SIES 12.7.1.0. 
 
Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di 
esercizio.

Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
SIUT-SIES-PR-1.6-20221125-Piano_di_Rilascio_021_RegInde_SIES 
Ver. 1.6 del 25/11/2022 
Pag. 7/14 
3. Identificazione degli elementi rilasciati 
Supporto 
Oggetti: 
Ver. 
Del 
Portale fornitura 
SIUT > 07 - MEV > 2019_021_SIES_Reginde > 
05_Verifica di Conformita' 
1.6 
25/11/2022 
Note-osservazioni

Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
SIUT-SIES-PR-1.6-20221125-Piano_di_Rilascio_021_RegInde_SIES 
Ver. 1.6 del 25/11/2022 
Pag. 8/14 
4. Riferimenti degli oggetti del rilascio 
4.1 Riferimenti Anomalia (MAC/GAR) 
Rif. Ticket 
OTRS 
Sede 
Ufficio 
Descrizione 
segnalazione 
Descrizione 
intervento 
Descrizione 
Tecnica 
Manuali 
corretti 
 
 
 
 
 
 
4.2 Riferimenti ChangeRequest (ADE/MEV) 
Prot. Richiesta o 
Rif. Ticket OTRS 
Scheda Intervento 
Specifica Intervento 
Descrizione Breve 
- 
SIUT-SIE-SI-2.6-20220422-Specifiche-
intervento-021-SIES.pdf 
- 
Integrazione del SIES 
con ReGIndE

Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
SIUT-SIES-PR-1.6-20221125-Piano_di_Rilascio_021_RegInde_SIES 
Ver. 1.6 del 25/11/2022 
Pag. 9/14 
5. Dettaglio degli elementi oggetto del rilascio 
Nome File 
Path 
Motivazione-riferimento 
aggiorna_db.zip 
Database 
Script per aggiornamento base dati:  
 Aggiornamento, inserimento e cancellazione in varie tabelle 
 Procedura di salvataggio tabelle 
 Aggiornamento versione SIES in tabella “VERSIONE” 
sorgenti.zip 
Sorgenti 
 Sorgenti software 
sies.war 
Applicazione 
 Eseguibile dell’applicazione SIES 
documentazione.zip
Documentazione 
 SIUT-SIES-PR-1.6-20221125-Piano_di_Rilascio_021_RegInde_SIES.pdf 
 SIUT-SIE-MU-1.1-20211008-Manuale_Utente_021_RegInde_SIES.pdf 
 SIUT-SIE-CT-1.2-20221111-
Allegato_al_piano_test_021_RegInde_SIES.xlsx 
 SIUT-SIES-MG-1.7-20221125-
Istruzioni_Bonifica_Difensori_021_RegInde_SIES.pdf 
 SIUT-SIE-PT-1.0-20210730-Piano_dei_Test_021_RegInde_SIES.pdf 
 SIUT-SIES-MG-1.0-20220525-
Analisi_Procedure_Allineamento_021_RegInde_SIES.pdf 
Bonifica.zip 
Bonifica Database Contiene procedure e script per eseguire la bonifica 
Aggiornamento 
Tabelle Fisse.zip 
Aggiornamento 
TabelleFisse 
Contiene procedure e script per eseguire l’aggiornamento delle tabelle 
fisse  
Note-osservazioni

Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
SIUT-SIES-PR-1.6-20221125-Piano_di_Rilascio_021_RegInde_SIES 
Ver. 1.6 del 25/11/2022 
Pag. 10/14 
6. Installazione 
6.1 Prerequisiti 
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente 
release 12.7.1.0. 
L’installazione della release si articola sulle quattro seguenti attività: 
1) effettuare preliminarmente uno snapshot del DB di modo che in caso di esito negativo di una o più 
verifiche riportate nei successivi STEP si possa riportare il DB alla situazione iniziale; 
2) esecuzione di una procedura batch per la bonifica dei Difensori sulla base dell’estrazione degli 
Avvocati presenti in ReGIndE; 
3) aggiornamento della tabella COMUNE, dei domini PROVINCIA, REGIONE, NAZIONE della Tabella 
CG_REF_CODES e dei domini COMUNE e NAZIONE della Tabella CODICI_SIES_NSC sulla base delle 
tabelle Fisse, fornite dall’Amministrazione; 
4) installazione dell’Applicazione aggiornata. 
Le attività vanno eseguite nell’ordine sopra indicato solo se ognuna non ha fornito messaggi di errore nei file o 
nelle tabelle di log; per esempio, l’attività 3) può essere eseguita solo se l’attività 2) non ha fornito messaggi 
di errore nella tabella di log XBA_LOG_BONIFICA_AVVOCATI. 
6.2 
Attività di installazione ed esecuzione procedura batch Bonifica Difensori 
La descrizione dettagliata delle operazioni da eseguire per quest’attività sono riportate nel documento SIUT-
SIES-MG-1.7-20221125-Istruzioni_Bonifica_Difensori_021_RegInde_SIES.pdf, da considerarsi parte integrante 
del presente documento. 
 
Se  tutte le attività descritte nel suddetto documento, ad esclusione di quelle descritte al par. 3.2.7, non 
hanno presentato errori si potrà procedere con le attività descritte nel successivo paragrafo. 
 
In caso di errori consultare i tecnici dell’assistenza Engineering ed attendere loro indicazioni. 
6.3 
Procedura di Aggiornamento Tabella SIES da Tabella fissa DGSIA 
Le attività descritte in questo paragrafo indicano i passi necessari all’allineamento delle tabelle SIES COMUNE, 
CG_REF_CODES, relativamente ai domini PROVINCIA, REGIONE e NAZIONE, e CODICI_SIES_NSC, 
relativamente ai domini COMUNE e NAZIONE e sono preliminari alle attività di installazione del software 
relativo alla MEV-2019_021 di SIES. 
Le attività descritte nel paragrafo 6.3.1 si articolano su scripts .sql e procedures plsql, contenuti nel pacchetto 
aggiorna_db.zip, che va estratto ottenendo la cartella ..\aggiorna_db. 
Di seguito l’attività da eseguire per l’aggiornamento delle tabelle SIES da quelle fornite da DGSIA, ricevute 
tramite e-mail di Anna.Maffucci@giustizia.it a Vito.Bufi@eng.it del 06/11/2020 09:06. 
6.3.1 
Attività di installazione ed esecuzione procedura batch Aggiornamento Tabella SIES da 
Tabella fissa DGSIA 
1) Copiare il file aggiorna_db.zip in una qualsiasi cartella e scompattarlo. Il sistema creerà la cartella 
aggiorna_db; 
2) Copiare la cartella aggiorna_db nella cartella /home/oracle/MEV-2019_21/.

Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
SIUT-SIES-PR-1.6-20221125-Piano_di_Rilascio_021_RegInde_SIES 
Ver. 1.6 del 25/11/2022 
Pag. 11/14 
In fase di esecuzione degli script, di seguito riportati, saranno chiesti alcuni parametri; di seguito un 
esempio di tale richiesta (dove xx è la sigla del distretto di appartenenza, per esempio siesrm per Roma): 
================================================== 
Riassunto dei dati immessi per questa installazione 
Nome ....................: sies 
================================================== 
SID Oracle ..............: sies 
Utente_SIES..............: siesxx 
Password_SIES............: siesxx 
3) Posizionarsi nel percorso /home/oracle/MEV-2019_21/aggiorna_db/; lanciare sequenzialmente i comandi, 
indicati nel par. 6.3.2. 
6.3.2 
Procedura Aggiornamento Tabelle SIES - STEP 1 
Verificare tramite il comando pwd di trovarsi nel percorso /home/oracle/MEV-2019_21/aggiorna_db/ ed 
eseguire il comando: 
./aggiorna_db.sh 
Dettaglio del file: 
1. XAT_SALVA_TABELLE_PRE_ALLINEA.prc 
= 
Crea 
e 
compila 
la 
procedure 
XAT_SALVA_TABELLE_PRE_ALLINEA, che esegue una copia di backup delle tabelle COMUNE, 
CG_REF_CODES e CODICI_SIES_NSC nelle tabelle COMUNE_SXALLTF, CG_REF_CODES_SXALLTF e 
CODICI_SIES_NSC_SXALLTF. 
2. Alter_Comune.sql = Lo script .sql aggiunge all’attuale struttura della tabella COMUNE le nuove 
colonne 
COD_CATASTALE_COMUNE, 
DATA_AGGIORNAMENTO_COMUNE, 
DATA_FINE_VALIDITA_COMUNE. 
3. Aggiornamento_TABELLA_COMUNE_esercizio.sql = Lo script effettua l’aggiornamento della tabella 
COMUNE, cancellando i preesistenti 8112 records e ne inserisce 13327. 
4. Aggiornamento_CG_REF_CODES_PROVINCIA_esercizio.sql = Lo script che cancella dalla tabella 
CG_REF_CODES i records aventi RV_DOMAIN = ‘PROVINCIA’ e carica i nuovi records. Il dominio 
conterrà 117 records a fronte dei 105 precedenti. 
5. Insert_REGIONE.sql = Lo script inserisce un nuovo record (LUOGO_SCONOSCIUTO) nella tabella 
CG_REF_CODES per RV_DOMAIN = ‘REGIONE’. 
6. Aggiornamento_CG_REF_CODES_NAZIONE_esercizio.sql 
= 
Lo 
script 
cancella 
dalla 
tabella 
CG_REF_CODES i records aventi RV_DOMAIN = ‘NAZIONE’ e carica i nuovi records. Il dominio conterrà 
269 records a fronte dei 200 precedenti. 
7. Alter_CODICI_SIES_NSC.sql = Lo script modifica la constraint attuale, che è costituita dalle colonne 
(CO_DOMAIN, CO_CODCENTR), alla nuova costituita da (CO_DOMAIN, CO_CODCENTR, CO_SIES) per 
permettere la gestione di comuni omonimi, che pur avendo lo stesso valore di CO_CODCENTR hanno 
diverso valore del CO_SIES. 
8. Aggiornamento_CODICI_SIES_NSC_COMUNE_esercizio.sql = Lo script cancella dalla tabella 
CODICI_SIES_NSC i records aventi CO_DOMAIN = ‘COMUNE’ e carica i nuovi records. Il dominio 
conterrà 8607 records a fronte degli 8145 precedenti. 
9. Aggiornamento_CODICI_SIES_NSC_NAZIONE_esercizio.sql = Lo script cancella dalla tabella 
CODICI_SIES_NSC i records aventi CO_DOMAIN = ‘NAZIONE’ e carica i nuovi records. Il dominio 
conterrà 204 records a fronte dei 201 precedenti. 
10. Disabilita_Funzioni_Inserimento_Modifica_Difensore.sql = Lo script disabilita le funzioni Inserimento 
e Modifica Difensore in Funzioni Amministrative/Gestione Difensori.

Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
SIUT-SIES-PR-1.6-20221125-Piano_di_Rilascio_021_RegInde_SIES 
Ver. 1.6 del 25/11/2022 
Pag. 12/14 
11. Insert_FUNZIONE-FUNZIONE_PROFILO.sql = Lo script inserisce nelle tabelle FUNZIONE e 
FUNZIONE_PROFILO i records necessari ad abilitare le nuove funzionalità necessarie alla ricerca ed alla 
gestione dell’Avvocato su ReGIndE ed alla ricerca e gestione del comune e provincia di nascita (nuova 
struttura delle tabella COMUNE e CODICI_SIES_NSC). 
12. Inserimento_CODICI_SIES_NSC_NAZIONE_NO_Cod_Univoco.sql = Lo script inserisce nella tabella 
CODICI_SIES_NSC i 32 records aventi CO_DOMAIN = ‘NAZIONE’ e che hanno una corrispondenza in 
entrambe 
le 
tabelle 
degli 
stati 
[CG_REF_CODES 
(RV_DOMAIN 
= 
‘NAZIONE’ 
di 
SIES, 
DC_TAB_STATO_ESTERO di NSC] ma non hanno nella tabella di NSC valorizzato il codice univoco. 
13. aggiorna_versione.sql = Lo script inserisce il record con la descrizione della nuova release nella tabella 
VERSIONE. 
 
Per ogni punto precedente sono riportati di seguito gli eventuali controlli per verificare la corretta esecuzione 
di aggiorna_db.sh: 
 
 
verificare che nel file /home/oracle/MEV-2019_21/aggiorna_db/log/Log_Aggiorna_DB.log non siano 
riportati errori oracle; 
 
Collegarsi al database con utenza siesxx (dove xx è la sigla del distretto di appartenenza, per esempio siesrm 
per Roma): 
1. Per verificare l’aggiornamento effettuato al terzo punto eseguire quanto di seguito  
SELECT COUNT(*) FROM COMUNE  
il risultato deve essere 13327. 
2. Per verificare l’aggiornamento effettuato al quarto punto eseguire quanto di seguito  
SELECT COUNT(*) FROM CG_REF_CODES WHERE RV_DOMAIN = 'PROVINCIA'  
il risultato deve essere 117. 
3. Per verificare l’aggiornamento effettuato al quinto punto eseguire quanto di seguito 
SELECT * FROM CG_REF_CODES WHERE RV_DOMAIN = 'REGIONE' 
verificare che nell’elenco sia presente il record con RV_LOW_VALUE = 21 
4. Per verificare l’aggiornamento effettuato al sesto punto eseguire quanto di seguito 
SELECT COUNT (*) FROM CG_REF_CODES WHERE RV_DOMAIN = 'NAZIONE' 
il risultato deve essere 269. 
5. Per verificare l’aggiornamento effettuato all’ottavo punto eseguire quanto di seguito 
SELECT COUNT(*) FROM CODICI_SIES_NSC WHERE CO_DOMAIN = 'COMUNE' 
il risultato deve essere 8607. 
6. Per verificare l’aggiornamento effettuato al dodicesimo punto eseguire quanto di seguito 
SELECT COUNT(*) FROM CODICI_SIES_NSC WHERE CO_DOMAIN = 'NAZIONE' 
il risultato deve essere 236. 
 
In caso di esito positivo delle su riportate attività LE TABELLE DI BACKUP COMUNE_SXALLTF, 
CG_REF_CODES_SXALLTF e CODICI_SIES_NSC_SXALLTF NON DEVONO ESSERE CANCELLATE MA VANNO 
MANTENUTE PER ALMENO 6 MESI, PER PERMETTERE EVENTUALI ATTIVITÀ DI VERIFICA. 
 
6.3.3 
Procedura Aggiornamento Tabelle SIES - STEP 2 
In caso di errori verificatisi nell’esecuzione di uno degli step precedenti, a seguito indicazioni dell’help desk 
del fornitore, è necessario ripristinare lo snapshot effettuato all’inizio delle attività di aggiornamento della 
Base Dati.

Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
SIUT-SIES-PR-1.6-20221125-Piano_di_Rilascio_021_RegInde_SIES 
Ver. 1.6 del 25/11/2022 
Pag. 13/14 
6.4 
Installazione applicazione 
6.4.1 
Deploy Applicazione 
4) Aprire una shell linux sul server SIES e loggarsi come utente “root”; 
5) Posizionarsi sotto la cartella: 
“/var/SIES/CONFIG”; 
6) Editare il file “f3b.properties” ed aggiungere alla fine del file le seguenti righe: 
# MEV_021 RegInde parametri di configurazione collegamento SERVER nazionale 
EndpointAddress=http://reginde.processotelematico.giustizia.it/ServiziInterrogazioneRegindeExt/Serviz
iInterrogazioneInterni   
 oppure in caso di connessione in https: 
 
EndpointAddress=https://reginde.processotelematico.giustizia.it/ServiziInterrogazioneRegindeE
xt/ServiziInterrogazioneInterni 
 
NB: Tali valori devono essere parametrizzati in base all’ambiente di installazione del servizio reso 
disponibile dal sistema REGINDE per la verifica di conformità. 
Per una connessione basata su protocollo https, proseguire con i passi di cui al punto 7 e 8; In caso di 
connessione di tipo http passare direttamente al punto 9. 
7) Posizionarsi sotto la cartella: 
“/var/SIES/CONFIG/certs”; 
8) Proseguire con l’aggiornamento del file trustStore “sies.jks”, importando, con procedura nota 
all’Amministrazione, la catena di certificati ed il certificato necessari al colloquio con la macchina server 
che espone il servizio web. 
NB: i certificati da importare devono essere resi disponibili dai referenti del sistema REGINDE e correlati 
all’ambiente predisposto per la verifica di conformità. 
9) Scaricare i files “sies.war” sul server SIES ed eseguire le seguenti operazioni: 
a) posizionarsi sotto la cartella: 
“/opt/jboss-eap-6.4/standalone/deployments”; 
b) cancellare il vecchio eseguibile (se esistente) “sies.war” e la copia deployata “sies.war.deployed”; 
c) copiare, nello stesso percorso, il nuovo eseguibile “sies.war”; 
d) posizionarsi sotto la cartella: 
“/opt/jboss-eap-6.4/standalone”; 
e) cancellare le cartelle “data”, “log” e “tmp” (se esistenti); 
 
Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le 
istruzioni ai punti 6.b e 6.e. All’avvio, infatti, tali cartelle verranno ricreate. 
 
10) Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”. 
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso 
“/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 
'imqbroker@nomemacchina:7676' pronto”;

Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
SIUT-SIES-PR-1.6-20221125-Piano_di_Rilascio_021_RegInde_SIES 
Ver. 1.6 del 25/11/2022 
Pag. 14/14 
11) Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione 
dell’istruzione tramite il comando: “service jboss status”. 
6.5 Attività di configurazione 
N.A. 
6.6 Attività di post-installazione 
N.A.