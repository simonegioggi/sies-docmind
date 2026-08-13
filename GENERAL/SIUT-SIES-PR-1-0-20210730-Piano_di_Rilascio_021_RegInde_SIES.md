---
uniqueName: siut-sies-pr-1-0-20210730-pianodirilascio021regind
displayName: "SIUT SIES PR 1 0 20210730 Piano di Rilascio 021 RegInde SIES"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.0-20210730-Piano_di_Rilascio_021_RegInde_SIES

> **File originale:** `MEV/SCHEDA_021/Docs/consegna docx/ORIGINALS/SIUT-SIES-PR-1.0-20210730-Piano_di_Rilascio_021_RegInde_SIES.docx`  
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
| Data approvazione | 30/07/2021 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 30/07/2021 | Prima Emissione |  |


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
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario e Referente Tecnico |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Referente PMO e Qualità |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |
| Luigi Buglione | RTI |  | Referente Metrico |


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
6.2	Attività di preinstallazione	10
6.3	Attività di installazione	10
6.3.1	Installazione lato DB	10
6.3.1.1	Esecuzione script	10
6.3.2	Installazione applicazione	12
6.3.2.1	Deploy Applicazione	12
6.4	Attività di configurazione	13
6.5	Attività di post-installazione	13


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio degli interventi realizzati nell’ambito del Sistema Integrato Esecuzione Sorveglianza per la realizzazione di quanto dettagliato nella scheda di intervento di riferimento.
Gli interventi in oggetto sono rilasciati nell’ambito della release MEV-2019_21 di SIES.
Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio.
## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF1. | SIUT-SIE-SI-2.3-20210730-Specifiche-intervento-021-SIES.pdf | Scheda Intervento |
| RIF2. | SIUT-SIES-MG-1.0-20210730 - Istruzioni_Bonifica_Difensori_021_RegInde_SIES.pdf | Manuale Gestione |
| RIF3. | SIUT-SIES-MG-1.0-20210730 - Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_SIES.pdf | Manuale Gestione |

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
Il presente documento descrive il piano di rilascio del software relativo alla MEV-2019_21 di SIES, contenente l’integrazione della suddetta MEV con la versione SIES 12.4.12.0.

Vengono elencati i passi da effettuare per la corretta installazione di tutte le componenti in ambiente di esercizio.
# Identificazione degli elementi rilasciati
| Supporto | Oggetti: | Ver. | Del |
| --- | --- | --- | --- |
| Portale fornitura | SIUT > 07 - MEV > 2019_021_SIES_Reginde > 05_Verifica di Conformita' |  |  |
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
| - | SIUT-SIE-SI-2.3-20210730-Specifiche-intervento-021-SIES.pdf | - | Integrazione del SIES con ReGIndE |

# Dettaglio degli elementi oggetto del rilascio
| Nome File | Path | Motivazione-riferimento |
| --- | --- | --- |
| aggiorna_db.zip | Database | Script per aggiornamento base dati: 
Aggiornamento Tabella “RELAZIONE_FUNZIONE”
Aggiornamento Tabella “FUNZIONE_PROFILO”
Aggiornamento Tabella “AVVOCATO”
Aggiornamento Tabella “FUNZIONE”
Aggiornamento Tabella “COMUNI” e “STATI”
Aggiornamento Tabella “CG_REF_CODES” dominio “NAZIONE”
Aggiornamento Tabella “CG_REF_CODES” dominio “PROVINCIA”
Aggiornamento Tabella “CG_REF_CODES” dominio “REGIONE”
Aggiornamento Tabella “CODICI_SIES_NSC”
Aggiornamento Tabella “CODICI_SIES_NSC” dominio “COMUNE”
Aggiornamento Tabella “CODICI_SIES_NSC” dominio “NAZIONE”
Aggiornamento Tabella “COMUNE”
Procedura di salvataggio delle tabelle COMUNE, CG_REF_CODES E CODICI_SIES_NSC
Aggiornamento versione SIES in tabella “VERSIONE” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.0-20210730-Piano_di_Rilascio_021_RegInde_SIES.docx
SIUT-SIE-PV-1.0-20210730-Piano_delle_verifiche_021_RegInde_SIES.pdf
SIUT-SIE-MU-1.0-20210730-Manuale_Utente_021_RegInde_SIES.pdf
SIUT-SIE-PT-1.0-20210730-Piano_dei_Test_021_RegInde_SIES.pdf
SIUT-SIE-CT-1.0-20210730-Allegato_al_piano_test_021_RegInde_SIES.xlsx
SIUT-SIE-SI-2.3-20210730-Specifiche-intervento-021-SIES.pdf
SIGI_PNL_ML_20210730_1.8_Modello dei Dati_SIES.pdf
SIUT-SIES-MG-1.0-20210730 - Istruzioni_Bonifica_Difensori_021_RegInde_SIES.pdf
SIUT-SIES-MG-1.0-20210730 - Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_SIES.pdf |
| Bonifica.zip | Bonifica | Contiene documentazione, procedure e script per eseguire la bonifica |
| Aggiornamento Tabelle Fisse.zip | TabelleFisse | Contiene documentazione, procedure e script per eseguire l’aggiornamento delle tabelle fisse |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.12.0.
A monte delle attività indicate in questo documento (aggiornamento DB ed Application Server), si
ricorda di effettuare, in maniera sequenziale, quelle indicate nel documento “SIUT-SIES-MG-1.0-20210730 - Istruzioni_Bonifica_Difensori_021_RegInde_SIES.pdf” inerenti ai controlli ed all’esecuzione della bonifica della tabella “AVVOCATO”.
Poiché in questa release è previsto anche il rilascio in esercizio degli script o procedure che contengono già la versione aggiornata delle tabelle SIES COMUNE, CG_REF_CODES (relativamente ai domini PROVINCIA, REGIONE, NAZIONE), CODICI_SIES_NSC (relativamente ai domini COMUNE, NAZIONE) e delle tabelle SIES-AVVOCATURA COMUNI e STATI, viene rilasciato anche il documento “SIUT-SIES-MG-1.0-20210730 - Aggiornamento_SIES_da_Tabelle_DGSIA_021_ RegInde_SIES.pdf”, in cui sono indicate le attività eseguite per l’aggiornamento delle stesse alle equivalenti tabelle fisse della DGSIA. Queste attività possono essere rieseguite dall’Amministrazione per verificare la correttezza dei passaggi eseguiti per pervenire alla versione aggiornata delle suddette tabelle di SIES e SIES-Avvocatura. Gli scripts e le procedure che contengono già la versione definitiva delle stesse e sono contenuti nel file aggiorna.zip (vedi par. 6.3.3.1 punto 4). Per la descrizione dettagliata del contenuto dei diversi files vedi par. 3.1.8 del documento sopra indicato.
## Attività di preinstallazione
Prima di procedere con le attività descritte di seguito deve essere già stata eseguita con esito positivo la procedura di Bonifica Difensori  (Rif2).

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

Nella cartella appena creata (MEV-2019_21), lanciare il comando:
./aggiorna_db.sh
Durante l’esecuzione verrà creato un file di log nella cartella /home/oracle/MEV-2019_21/log/ in cui si può constatare l’esito dell’esecuzione.

N.B. Le segnalazioni del tipo:
ORA-00001: violata restrizione di unicità
ORA-00955: name is already used by an existing object
Cartella log già presente
ORA-04043: object does not exist
sono da considerarsi warning e non errori.

Accedere ad oracle (con qualsiasi strumento tipo toad, developer…) come utente siesxx e compilare tutte le procedure e i package che non risultano compilate.
ATTENZIONE: la procedura SUPER_SOGGETTO_PREGR e il package CARICA_RES potrebbero restare non compilate: non è da considerarsi errore.

Per tutti i distretti: Accedere al paragrafo 3.1 del manuale di gestione [Rif. 2] e procedere secondo gli step indicati nel suddetto paragrafo.

Solo DGSIA: accedere al paragrafo 3.1 del manuale di gestione [Rif. 3] e procedere secondo gli step indicati nel suddetto paragrafo solo per la verifica della correttezza delle attività eseguite per ottenere gli script/procedure che saranno rilasciate in tutti i Distretti in fase di messa in esercizio.


Di seguito l’elenco dei files contenuti nella cartella sottocartella ../MEV-2019_21/aggiorna_db/MEV-2019_21

| aggiorna_db.zip | Database | Scripts/procedure per aggiornamento base dati: 
Insert_FUNZIONE-FUNZIONE_PROFILO.sql
XAT_SALVA_TABELLE_PRE_ALLINEA.sql
Alter_Comune.sql
Alter_CODICI_SIES_NSC.sql
Alter_COMUNI_STATI.sql      
Aggiornamento_TABELLA_COMUNE_esercizio.sql
Aggiornamento_CG_REF_CODES_PROVINCIA_esercizio.sql
Insert_REGIONE.sql
Aggiornamento_CG_REF_CODES_NAZIONE_esercizio.sql
Aggiornamento_CODICI_SIES_NSC_COMUNE_esercizio.sql
Aggiornamento_CODICI_SIES_NSC_NAZIONE_esercizio.sql
AGGIORNA_COMUNI_AVVOCATURA.prc        
Aggiorna_TABELLA_STATI_SIES_AVVOCATURA.sql
Disabilita_Funzioni_Inserimento_Modifica_Difensore |
| --- | --- | --- |


## Installazione applicazione
## Deploy Applicazione
Aprire una shell linux sul server SIES e loggarsi come utente “root”;
Posizionarsi sotto la cartella:
“/var/SIES/CONFIG”;
Editare il file “f3b.properties” ed aggiungere alla fine del file le seguenti righe:
# MEV_21 RegInde parametri di configurazione collegamento SERVER nazionale
EndpointAddress={PROT_REGINDE}://{IP_REGINDE}/ServiziInterrogazioneRegindeExt/ServiziInterrogazioneInterni
PROT_REGINDE è il protocollo di comunicazione per il servizio (http o https);
IP_REGINDE è l’IP address della macchina dove è esposto il web service di ricerca Avvocato di ReGIndE.
NB: Tali valori devono essere parametrizzati in base all’ambiente di installazione del servizio reso disponibile dal sistema REGINDE per la verifica di conformità.
Per una connessione basata su protocollo https, proseguire con i passi di cui al punto 4 e 5; In caso di connessione di tipo http passare direttamente al punto 6.
Posizionarsi sotto la cartella:
“/var/SIES/CONFIG/certs”;
Proseguire con l’aggiornamento del file trustStore “sies.jks”, importando, con procedura nota all’Amministrazione, la catena di certificati ed il certificato necessari al colloquio con la macchina server che espone il servizio web.
NB: i certificati da importare devono essere resi disponibili dai referenti del sistema REGINDE e correlati all’ambiente predisposto per la verifica di conformità.
Scaricare i files “sies.war” sul server SIES ed eseguire le seguenti operazioni:
posizionarsi sotto la cartella:
“/opt/jboss-eap-6.4/standalone/deployments”;
cancellare il vecchio eseguibile (se esistente) “sies.war” e la copia deployata “sies.war.deployed”;
copiare, nello stesso percorso, il nuovo eseguibile “sies.war”;
posizionarsi sotto la cartella:
“/opt/jboss-eap-6.4/standalone”;
cancellare le cartelle “data”, “log” e “tmp” (se esistenti);

Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 6.b e 6.e. All’avvio, infatti, tali cartelle verranno ricreate.

Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.