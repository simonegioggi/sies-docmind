---
uniqueName: siut-sies-pr-1-3-20221026-pianodirilascio021regind
displayName: "SIUT SIES PR 1 3 20221026 Piano di Rilascio 021 RegInde AVVOCATURA"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.3-20221026-Piano_di_Rilascio_021_RegInde_AVVOCATURA

> **File originale:** `MEV/SCHEDA_021/Docs/SIUT-SIES-PR-1.3-20221026-Piano_di_Rilascio_021_RegInde_AVVOCATURA.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |




Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni

|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Engineering | RTI |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 25/10/2022 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 30/07/2021 | Prima Emissione |  |
| 1.1 | 08/10/2021 | Seconda Emissione | Rivista intera struttura del documento |
| 1.2 | 24/01/2022 | Terza Emissione | Modificati i riferimenti ai documenti di bonifica ed aggiornamento |
| 1.3 | 25/10/2022 | Quarta Emissione | Rivista intera struttura del documento |


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
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario e Referente Tecnico |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Referente PMO e Qualità |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |


INDICE DEI CONTENUTI
1.	Introduzione	5
1.1	Scopo del documento	5
1.2	Riferimenti	5
1.3	Glossario	5
1.3.1	Definizioni	5
1.3.2	Acronimi e abbreviazioni	5
2.	Generalità	6
3.	Identificazione degli elementi rilasciati	7
4.	Riferimenti degli oggetti del rilascio	8
4.1	Riferimenti Anomalia (MAC/GAR)	8
4.2	Riferimenti ChangeRequest (ADE/MEV)	8
5.	Dettaglio degli elementi oggetto del rilascio	9
6.	Installazione	10
6.1	Prerequisiti	10
6.2	Procedura di Aggiornamento Tabella SIUS-Avvocati da Tabella fissa DGSIA	10
6.2.1	Attività di installazione ed esecuzione procedura batch Aggiornamento Tabella SIUS-Avvocati (utente “avvsies”) da Tabella fissa DGSIA	10
6.3	Procedura Aggiornamento tabelle COMUNI e STATI di SIES-AVVOCATURA	11
6.3.1	STEP 1	11
6.3.2	STEP 2	12
6.4	Installazione applicazione	12
6.4.1	Deploy Applicazione	12
6.5	Attività di configurazione	12
6.6	Attività di post-installazione	12


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio degli interventi realizzati nell’ambito del Sistema Integrato Esecuzione Sorveglianza per la realizzazione di quanto dettagliato nella scheda di intervento di riferimento.
Gli interventi in oggetto sono rilasciati nell’ambito della release MEV-2019_21_AVVOCATURA di SIUS - AVVOCATURA.
Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio.
## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF1. | SIUT-SIE-SI-2.6-20220422-Specifiche-intervento-021-SIES.pdf | Scheda Intervento |
| RIF2. | SIUT-SIE-PV-1.0-20210730-Piano_delle_verifiche_021_RegInde_SIES.pdf | Piano delle Verifiche |

## Glossario
## Definizioni
| Definizione | Descrizione |
| --- | --- |
|  |  |

## Acronimi e abbreviazioni
| Sigla | Descrizione |
| --- | --- |
| DB | Data Base |
| DEC | Direttore Esecutivo Contratto |
| DGSIA | Direzione Generale per i Sistemi Informativi Automatizzati |
| FP | Function Point |
| GdL | Gruppo di Lavoro |
| HW | HardWare |
| MAC | MAnutenzione Correttiva |
| MEV | Manutenzione EVolutiva |
| PA | Pubblica Amministrazione |
| PEC | Posta Elettronica Certificata |
| RTI | Raggruppamento Temporaneo di Impresa |
| RUF | Responsabile Unico Fornitore |
| RUP | Responsabile Unico Progetto |
| SW | SoftWare |


# Generalità
Il presente documento descrive il piano di rilascio del software relativo alla MEV-2019_21_AVVOCATURA di SIUS - AVVOCATURA.

Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.
# Identificazione degli elementi rilasciati
| Supporto | Oggetti: | Ver. | Del |
| --- | --- | --- | --- |
| Portale fornitura | SIUT > 07 - MEV > 2019_021_SIES_Reginde > 05_Verifica di Conformita' | 1.3 | 25/10/2022 |
| Note-osservazioni |  |  |  |


# Riferimenti degli oggetti del rilascio
## Riferimenti Anomalia (MAC/GAR)
| Rif. Ticket OTRS | Sede
Ufficio | Descrizione segnalazione | Descrizione
intervento | Descrizione Tecnica | Manuali corretti |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |

## Riferimenti ChangeRequest (ADE/MEV)
| Prot. Richiesta o
Rif. Ticket OTRS | Scheda Intervento | Specifica Intervento | Descrizione Breve |
| --- | --- | --- | --- |
| - | SIUT-SIE-SI-2.6-20220422-Specifiche-intervento-021-SIES.pdf | - | Integrazione del SIES con ReGIndE |

# Dettaglio degli elementi oggetto del rilascio
| Nome File | Path | Motivazione-riferimento |
| --- | --- | --- |
| aggiorna_db_AVVOCATURA.zip | Database | Script per aggiornamento base dati: 
Modifica Strutturale delle Tabelle “avvsies.COMUNI” e “avvsies.STATI”
Aggiornamento Tabella “avvsies.COMUNI” e “avvsies.STATI”
Procedura di salvataggio delle tabelle “avvsies.COMUNI”, “avvsies.STATI” |
| documentazione_AVVOCATURA.zip | Documentazione | SIUT-SIES-PR-1.3-20221026-Piano_di_Rilascio_021_RegInde_AVVOCATURA.pdf
SIUT-SIE-PV-1.0-20210730-Piano_delle_verifiche_021_RegInde_SIES.pdf |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
L’installazione della release si articola sulle seguenti attività:
effettuare preliminarmente uno snapshot del DB di modo che in caso di esito negativo di una o più verifiche riportate nei successivi STEP si possa riportare il DB alla situazione iniziale;
aggiornamento delle tabelle COMUNI e STATI sulla base delle tabelle Fisse, fornite dall’Amministrazione.
## Procedura di Aggiornamento Tabella SIUS-Avvocati da Tabella fissa DGSIA
Le attività descritte indicano i passi necessari all’allineamento delle tabelle SIES-AVVOCATURA avvsies.COMUNI ed avvsies.STATI, e sono preliminari alle attività di installazione del software relativo alla MEV 021_2019 RegInde di SIES.
Le attività descritte nel paragrafo 6.3 si articolano su scripts .sql e procedures plsql, contenuti nel pacchetto aggiorna_db_AVVOCATURA.zip, che va estratto ottenendo la cartella ..\aggiorna_db_AVVOCATURA.
Di seguito l’attività da eseguire per l’aggiornamento delle tabelle SIES (utente “avvsies”) da quelle fornite da DGSIA, ricevute tramite e-mail di Anna.Maffucci@giustizia.it a Vito.Bufi@eng.it del 6/11/2020 09:06.
## Attività di installazione ed esecuzione procedura batch Aggiornamento Tabella SIUS-Avvocati (utente “avvsies”) da Tabella fissa DGSIA
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
Copiare il file aggiorna_db_AVVOCATURA.zip in una qualsiasi cartella e scompattarlo. il sistema crea la cartella aggiorna_db_AVVOCATURA;
Creare sul server DB una cartella MEV-2019_21_AVVOCATURA sotto la directory /home/oracle/;
Copiare la cartella aggiorna_db_AVVOCATURA nella cartella /home/oracle/MEV-2019_21_AVVOCATURA/.
Dare i permessi di lettura, scrittura ed esecuzione a tutti i file della cartella MEV-2019_21_AVVOCATURA tramite il comando:
chmod 777 MEV-2019_21_AVVOCATURA

In fase di esecuzione degli script, di seguito riportati, saranno chiesti alcuni parametri; di seguito un esempio di tale richiesta (dove xx è la sigla del distretto di appartenenza, per esempio siesrm per Roma):
==================================================
Riassunto dei dati immessi per questa installazione
Nome ....................: sies
==================================================
SID Oracle ..............: sies
Utente_SIES..............: siesxx
Password_SIES............: siesxx

Posizionarsi nel percorso /home/oracle/MEV-2019_21_AVVOCATURA/ e lanciare sequenzialmente i comandi, indicati nel par. 6.3.
## Procedura Aggiornamento tabelle COMUNI e STATI di SIES-AVVOCATURA
Di seguito le attività da eseguire per l’aggiornamento delle tabelle avvsies.COMUNI e avvsies.STATI alle tabelle fisse COMUNE e STATO-NAZIONE fornite dalla DGSIA.
## STEP 1
Verificare tramite il comando pwd di trovarsi nel percorso /home/oracle/MEV-2019_21_AVVOCATURA/ ed eseguire il comando

./aggiorna_db_AVVOCATURA.sh

Dettaglio del file:
XAT_SALVA_TABELLE_AVVOCATURA.prc = Crea e compila la procedure XAT_SALVA_TABELLE_ AVVOCATURA, che esegue una copia di backup delle tabelle avvsies.COMUNI e avvsies.STATI nelle tabelle avvsies.COMUNI_SXALLTF e avvsies.STATI_SXALLTF.
ALTER_COMUNI_STATI_AVVOCATURA.sql = lo script .sql aggiunge all’attuale struttura della tabella avvsies.COMUNI le nuove colonne COD_CATASTALE_COMUNE, DATA_AGGIORNAMENTO_COMUNE e DATA_FINE_VALIDITA_COMUNE; aggiunge all’attuale struttura della tabella avvsies.STATI le nuove colonne COD_STATO_ISO, COD_ISTAT_STATO, COD_CATASTALE e DATA_FINE_VALIDITA.
AGGIORNA_COMUNI_AVVOCATURA.prc = La procedure effettua l’aggiornamento della tabella avvsies.COMUNI, cancellando  i preesistenti 8112 records e ne inserisce 13327.
AGGIORNA_STATI_AVVOCATURA.sql = Lo script cancella dalla tabella avvsies.STATI e la ricrea caricando i nuovi records. Il dominio conterrà 269 records a fronte dei 200 precedenti.

Per ogni punto precedente sono riportati di seguito gli eventuali controlli per verificare la corretta esecuzione di aggiorna_db_AVVOCATURA.sh:

Verificare che nel file /home/oracle/MEV-2019_21_AVVOCATURA/log/Log_Aggiorna_DB.log non siano riportati errori oracle.

Collegarsi al database con utenza siesxx (dove xx è la sigla del distretto di appartenenza, per esempio siesrm per Roma):

Per verificare l’aggiornamento effettuato al terzo punto eseguire quanto di seguito

SELECT COUNT(*) FROM avvsies.COMUNI           	il risultato deve essere 13327.

Per verificare l’aggiornamento effettuato al quarto punto eseguire quanto di seguito

SELECT COUNT (*) FROM avvsies.STATI		il risultato deve essere  269.

In caso di esito positivo delle su riportate attività LE TABELLE DI BACKUP, create nello STEP 1 (tramite la procedure “XAT_SALVA_TABELLE_AVVOCATURA.prc”), NON DEVONO ESSERE CANCELLATE MA VANNO MANTENUTE PER ALMENO 6 MESI, PER PERMETTERE EVENTUALI ATTIVITÀ DI VERIFICA.
## STEP 2
In caso di errori verificatisi nell’esecuzione di uno degli step precedenti, a seguito indicazioni dell’help desk del fornitore, è necessario ripristinare lo snapshot effettuato all’inizio delle attività di aggiornamento della Base Dati.
## Installazione applicazione
## Deploy Applicazione
Attenzione!! La variabile $JBOSS_HOME rappresenta il path di installazione dell’Enterprise Application Server 6.4.0 GA. (es: /opt/jboss-eap-6.4/)

Aprire una shell linux sul server Avvocatura_SIES e loggarsi come utente “root”.
Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”;
Eseguire le seguenti operazioni:
posizionarsi sotto la cartella:
“$JBOSS_HOME/standalone/deployments”;
cancellare la copia deployata “avvocatura.war.deployed”;
posizionarsi sotto la cartella:
“$JBOSS_HOME/standalone”;
cancellare le cartelle “data”, “log” e “tmp” (se esistenti).

Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 3.b e 3.d. All’avvio, infatti, tali cartelle verranno ricreate.

Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.