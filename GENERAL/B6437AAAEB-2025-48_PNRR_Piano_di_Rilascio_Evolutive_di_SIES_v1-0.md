---
uniqueName: b6437aaaeb-2025-48pnrrpianodirilascioevolutivedisi
displayName: "B6437AAAEB 2025 48 PNRR Piano di Rilascio Evolutive di SIES v1 0"
category: "GENERAL"
tags: []
---

# B6437AAAEB-2025-48_PNRR_Piano_di_Rilascio_Evolutive_di_SIES_v1.0

> **File originale:** `MEV/SCHEDA_48/B6437AAAEB-2025-48_PNRR_Piano_di_Rilascio_Evolutive_di_SIES_v1.0.docx`  
> **Tipo:** DOCX

---

Ministero della Giustizia
Dipartimento per l’innovazione tecnologica della giustizia

SCHEDA INTERVENTO
INTERVENTI EVOLUTIVI SULL’APPLICAZIONE SIES

| Prospetto Informativo Sintetico | Prospetto Informativo Sintetico |
| --- | --- |
| INTERVENTO | Interventi evolutivi sull’applicazione SIES |
| CONTRATTO DI RIFERIMENTO | Accordo Quadro per l’affidamento di servizi applicativi in ottica cloud e l’affidamento di servizi di demand e PMO per le pubbliche amministrazioni centrali ID 2483 – Seconda Edizione - Lotto 1 – Digitalizzazione Area Penale – CIG B6437AAAEB |
| Milestone PNRR | M1C1-38 bis 
Interventi già programmati per il 2024 su sistemi complementari ad APP per la digitalizzazione del processo penale di primo grado (B2) |
| CICLO DI VITA | Ridotto |
| DOCUMENTO | Piano di Rilascio: B6437AAAEB_2025_48 |
| FILE | B6437AAAEB-2025-48_PNRR_Piano_di_Rilascio_Evolutive_di_SIES_v1.0 |
| DATA DOCUMENTO | 22/12/2025 |
| FORNITORE | RTI - Accenture |

l
| Elenco versioni | Elenco versioni |
| --- | --- |
| v1 | Prima emissione |


| Referenti | Referenti |
| --- | --- |
| Nominativo | Organizzazione |
| Oris Orlando | DEC - DGSAP |
| Marta Nicoletti Altimari | RUP – DGSAP |
| Michele D’Alessandro | RUAC - RTI Accenture |



INDICE

1.	Premessa	3
2.	Generalità	4
3.	Identificazione degli elementi rilasciati	5
4.	Dettaglio degli elementi oggetto del rilascio	6
5.	Installazione	8
5.1	Prerequisiti	8
5.2	Attività di preinstallazione	8
5.3	Attività di installazione	8
5.3.1	Installazione lato DB	8
5.3.1.1	Esecuzione script	8
5.3.2	Installazione applicazione	9
5.3.2.1	Deploy Applicazione	9
5.4	Attività di configurazione	9
5.5	Attività di post-installazione	9


# Premessa
Il presente documento descrive il piano di rilascio degli interventi realizzati nell’ambito del Sistema Integrato Esecuzione Sorveglianza per la realizzazione di quanto dettagliato nella scheda di intervento di riferimento.
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.8.4.0-MEV_2025_48 di SIES.
Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio.
# Generalità
Il presente documento descrive il piano di rilascio del software relativo alla MEV 2025-48 - PNRR Scheda Intervento Evolutive di SIES v1.0 di SIES, contenente l’integrazione della suddetta MEV con la versione SIES 12.8.4.0.

Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.
# Identificazione degli elementi rilasciati
| Supporto | Oggetti: | Ver. | Del |
| --- | --- | --- | --- |
| Portale fornitura | SIUT > 07 - MEV > SCHEDA 2025-48 - PNRR Scheda Esigenze Evolutive SIES v1.0 > 05_Verifica di Conformita' | 1.0 | 22/12/2025 |
| Note-osservazioni |  |  |  |


# Dettaglio degli elementi oggetto del rilascio
| Nome File | Path | Motivazione-riferimento |
| --- | --- | --- |
| aggiorna_db.zip | Database | Script per aggiornamento base dati: 
Aggiornamento, inserimento e alterazione in varie tabelle
Aggiornamento versione SIES in tabella “VERSIONE” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| documentazione.zip | Documentazione | B6437AAAEB-2025-48_PNRR_Piano_di_Rilascio_Evolutive_di_SIES_v1.0.pdf
B6437AAAEB-2025-48_PNRR_Scheda_Intervento_Evolutive_di_SIES_v1.0.pdf
B6437AAAEB-2025-48_PNRR_Allegato_al_Piano_dei_Test_Evolutive_di_SIES_v1.0.xlsx
B6437AAAEB-2025-48_PNRR_Piano_dei_Test_Evolutive_di_SIES_v1.0.pdf
B6437AAAEB-2025-48_PNRR_Manuale_Utente_Evolutive_di_SIES_v1.0.pdf
B6437AAAEB-2025-48_PNRR_Modello_Logico_dei_Dati_Evolutive_di_SIES_v1.0.pdf |
| template.zip | Template | import\EsecuzioneMisuraSicurezzaCumulo.rtf
import\PenaComplessivaSoloPecuniaria.rtf
import\RichiestePmCumInviateGEAltre.rtf
import\RichiestePmCumInviateGEAltre-sr.rtf
import\RichiestePmCumInviateGEApplicaBenefici.rtf
import\RichiestePmCumInviateGEApplicaBenefici-sr.rtf
import\RichiestePmCumInviateGEPenaPrinc.rtf
import\RichiestePmCumInviateGEPenaPrinc-sr.rtf
import\RichiestePmCumInviateGERevocaBenefici.rtf
import\RichiestePmCumInviateGERevocaBenefici-sr.rtf
import\RichiestePmCumInviateGERevocaLA.rtf
import\RichiestePmCumInviateGERevocaLA-sr.rtf
import\RichiestePmCumInviateGERevocaSS.rtf
import\RichiestePmCumInviateGERevocaSS-sr.rtf
import\RichiestePmCumInviatePeneAcc.rtf
import\RichiestePmCumInviatePeneAcc-sr.rtf
import\RichiestePmCumInviateRevocaMA.rtf
import\RichiestePmCumInviateRevocaMA-sr.rtf
import\RichiestePmCumInviateUnificaMS.rtf
import\RichiestePmCumInviateUnificaMS-sr.rtf
import\RichiestePmInCumuloAltre.rtf
import\RichiestePmInCumuloApplicazBenefici.rtf
import\RichiestePmInCumuloPeneAccessorie.rtf
import\RichiestePmInCumuloRevocaBenefici.rtf
import\RichiestePmInCumuloRevocaLA.rtf
import\RichiestePmInCumuloRevocaMA.rtf
import\RichiestePmInCumuloRevocaPenaPrinc.rtf
import\RichiestePmInCumuloRevocaSS.rtf
import\RichiestePmInCumuloUnificaMS.rtf
import\Variabili.rtf
siep\cumulo\SIEP_CUMULO_656_4BIS_COMU.rtf
siep\cumulo\SIEP_CUMULO_656_4BIS_TRASM.rtf
siep\cumulo\SIEP_CUMULO_DETENUTO.rtf
siep\cumulo\SIEP_CUMULO_DISPOSITIVO.rtf
siep\cumulo\SIEP_CUMULO_GENERICO_NEW.rtf
siep\cumulo\SIEP_CUMULO_MA_CESS_51BIS.rtf
siep\cumulo\SIEP_CUMULO_MA_PROSEC_51BIS.rtf
siep\cumulo\SIEP_CUMULO_MA_PROSEC_51BIS_DIFFDETDOM.rtf
siep\cumulo\SIEP_CUMULO_OE_656_4TER_TRASM.rtf
siep\cumulo\SIEP_CUMULO_OE_656_C5_IRR.rtf
siep\cumulo\SIEP_CUMULO_OE_656_C5_REV.rtf
siep\cumulo\SIEP_CUMULO_OE_656_C5_SOSP.rtf
siep\cumulo\SIEP_CUMULO_OE_656_C10.rtf
siep\cumulo\SIEP_CUMULO_OE_656_C10_PROSEC.rtf
siep\cumulo\SIEP_CUMULO_OE_656_DET.rtf
siep\cumulo\SIEP_CUMULO_OE_656_LIB.rtf
siep\cumulo\SIEP_CUMULO_OE_656_LIB_C10_TRAD.rtf
siep\cumulo\SIEP_CUMULO_OE_656_LIB_TRAD.rtf
siep\cumulo\SIEP_CUMULO_OE_SOSP_199_ESPPREDOM_AD.rtf
siep\cumulo\SIEP_CUMULO_OE_SOSP_199_ESPPREDOM_DET.rtf
siep\cumulo\SIEP_CUMULO_OE_SOSP_199_ESPPREDOM_LIB.rtf
siep\cumulo\SIEP_CUMULO_PROSEC_DIFF.rtf
siep\cumulo\SIEP_CUMULO_PROSPETTO_PROPOSTA.rtf
siep\cumulo\SIEP_CUMULO_RICHIESTEPM_GE_SORV.rtf
siep\cumulo\SIEP_RICH_INVIATE_CUM.rtf
sius\or\SIUS_OR_GENERICAPENASOST.rtf
sius\or\SIUS_OR_MODGENERICOPS.rtf |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.8.4.0.
## Attività di preinstallazione
Aprire una shell linux sul server SIES e loggarsi come utente “root”;
Eseguire il comando: “cd /etc/init.d”;
Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”;
Fermare il processo di gestione delle code tramite il comando: “./imq stop”;
## Attività di installazione
## Installazione lato DB
## Esecuzione script
(E’ consigliato che tale procedura venga eseguita da personale competente in ambiente Oracle)
Il documento elenca i passi necessari per la corretta esecuzione.
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
Creare sul server DB una cartella MEV_2025_48 sotto la directory /home/oracle/;
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/MEV_2025_48/;
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella MEV_2025_48 tramite il comando:
chmod 777 MEV_2025_48
In fase di esecuzione dello script saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta:
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES...........: siesxx	(dove xx è la sigla del distretto di appartenenza, per esempio: rm per Roma)
Password_SIES.......: siesxx
Nella cartella appena creata (MEV_2025_48), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/MEV_2025_48/log/ in cui si può constatare l’esito dell’esecuzione.
N.B. Le segnalazioni del tipo:
ORA-00001: violata restrizione di unicità
ORA-00955: name is already used by an existing object
ORA-01430: column being added already exists in table
ORA-04043: object does not exist
Cartella log già presente
sono da considerarsi warning e non errori.
Accedere ad oracle (con qualsiasi strumento tipo toad, developer…) come utente siesxx e compilare tutte le procedure e i package che non risultano compilate.
ATTENZIONE: la procedura SUPER_SOGGETTO_PREGR ed il package CARICA_RES potrebbero restare non compilate: non è da considerarsi errore.
## Installazione applicazione
## Deploy Applicazione
Aprire una shell linux sul server SIES e loggarsi come utente “root”;
Scaricare il file “sies.war” sul server SIES ed eseguire le seguenti operazioni:
posizionarsi sotto la cartella:
“/opt/jboss-eap-6.4/standalone/deployments”;
cancellare il vecchio eseguibile (se esistente) “sies.war” e la copia deployata “sies.war.deployed”;
copiare, nello stesso percorso, il nuovo eseguibile “sies.war”;
posizionarsi sotto la cartella:
“/opt/jboss-eap-6.4/standalone”;
cancellare le cartelle “data”, “log” e “tmp” (se esistenti);
Copiare i files contenuti nella cartella template\import
nella cartella “/var/SIES/template/import” sovrascrivendo quelli precedenti;
Copiare i files contenuti nella cartella template\siep\cumulo
nella cartella “/var/SIES/template/siep/cumulo” sovrascrivendo quelli precedenti;
Copiare i files contenuti nella cartella template\sius\or
nella cartella “/var/SIES/template/sius/or” sovrascrivendo quelli precedenti;
Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 2.b e 2.e. All’avvio, infatti, tali cartelle verranno ricreate.
Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.