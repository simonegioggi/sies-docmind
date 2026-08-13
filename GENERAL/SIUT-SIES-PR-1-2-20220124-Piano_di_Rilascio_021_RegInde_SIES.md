---
uniqueName: siut-sies-pr-1-2-20220124-pianodirilascio021regind
displayName: "SIUT SIES PR 1 2 20220124 Piano di Rilascio 021 RegInde SIES"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.2-20220124-Piano_di_Rilascio_021_RegInde_SIES

> **File originale:** `MEV/SCHEDA_021/Docs/consegna docx/ORIGINALS/SIUT-SIES-PR-1.2-20220124-Piano_di_Rilascio_021_RegInde_SIES.docx`  
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
| Data approvazione | 24/01/2022 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 30/07/2021 | Prima Emissione |  |
| 1.1 | 08/10/2021 | Seconda Emissione |  |


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
6.3	Attività di installazione ed esecuzione procedura batch Bonifica Difensori	10
6.4	Attività di installazione ed aggiornamento di alcune Tabelle fisse e dell’Applicazione	16
6.4.1	Installazione lato DB	16
6.4.1.1	Esecuzione script	16
6.4.2	Installazione applicazione	19
6.4.2.1	Deploy Applicazione	19
6.5	Attività di configurazione	19
6.6	Attività di post-installazione	20


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio degli interventi realizzati nell’ambito del Sistema Integrato Esecuzione Sorveglianza per la realizzazione di quanto dettagliato nella scheda di intervento di riferimento.
Gli interventi in oggetto sono rilasciati nell’ambito della release MEV-2019_21 di SIES.
Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio.
## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF1. | SIUT-SIE-SI-2.5-20220119-Specifiche-intervento-021-SIES.pdf | Scheda Intervento |
| RIF2. | SIUT-SIES-MG-1.2-20220124-Istruzioni_Bonifica_Difensori_021_RegInde_SIES.pdf | Manuale Gestione |
| RIF3. | SIUT-SIES-MG-1.2-20220124-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_SIES.pdf | Manuale Gestione |

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
Il presente documento descrive il piano di rilascio del software relativo alla MEV-2019_21 di SIES, contenente l’integrazione della suddetta MEV con la versione SIES 12.4.15.0.

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
| - | SIUT-SIE-SI-2.5-20220119-Specifiche-intervento-021-SIES.pdf | - | Integrazione del SIES con ReGIndE |

# Dettaglio degli elementi oggetto del rilascio
| Nome File | Path | Motivazione-riferimento |
| --- | --- | --- |
| aggiorna_db.zip | Database | Script per aggiornamento base dati: 
Aggiornamento Tabella “RELAZIONE_FUNZIONE”
Aggiornamento Tabella “FUNZIONE_PROFILO”
Aggiornamento Tabella “FUNZIONE”
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
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.2-20220124-Piano_di_Rilascio_021_RegInde_SIES.pdf
SIUT-SIE-MU-1.1-20211008-Manuale_Utente_021_RegInde_SIES.pdf
SIUT-SIE-CT-1.1-20211008-Allegato_al_piano_test_021_RegInde_SIES.xlsx
SIUT-SIES-MG-1.2-20220124-Istruzioni_Bonifica_Difensori_021_RegInde_SIES.pdf
SIUT-SIES-MG-1.2-20220124-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_SIES.pdf
SIUT-SIE-PT-1.0-20210730-Piano_dei_Test_021_RegInde_SIES.pdf |
| Bonifica.zip | Bonifica | Contiene procedure e script per eseguire la bonifica |
| Aggiornamento Tabelle Fisse.zip | TabelleFisse | Contiene procedure e script per eseguire l’aggiornamento delle tabelle fisse |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.15.0.
L’installazione della release si articola sulle due seguenti attività:
esecuzione di una procedura batch per la bonifica dei Difensori sulla base dell’estrazione degli Avvocati presenti in ReGIndE;
aggiornamento della tabella COMUNE, dei domini PROVINCIA, REGIONE, NAZIONE della Tabella CG_REF_CODES e dei domini COMUNE e NAZIONE della Tabella CODICI_SIES_NSC sulla base delle tabelle Fisse, fornite dall’Amministrazione. Installazione dell’Applicazione aggiornata.
Le attività vanno eseguite nell’ordine sopra indicate, l’attività 2) può essere eseguita solo se l’attività 1) non ha fornito messaggi di errore nella tabella di log XBA_LOG_BONIFICA_AVVOCATI.
## Attività di preinstallazione
Aprire una shell linux sul server SIES e loggarsi come utente “root”;
Eseguire il comando: “cd /etc/init.d”;
Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”;
Fermare il processo di gestione delle code tramite il comando: “./imq stop”;
## Attività di installazione ed esecuzione procedura batch Bonifica Difensori
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
Di seguito l’elenco dei files contenuti nella cartella ../MEV-2019_21/bonifica_db/bonifica:

| bonifica_db.zip | Database | Scripts/procedure per aggiornamento base dati: 
Aggiorna_AVVOCATO_FORO.sql
Aggiorna_CG_REF_CODES_NON_ATTIVITA.sql
AVVOCATO_REGINDE_18112020.dmp
Crea_tabella_AVVOCATO_REGINDE_18112020.sql
CREA_TABELLA_XBA_LOG_BONIFICA_AVVOCATI.sql
Inserisci_CG_REF_CODES_FORO_AVVOCATI.sql
Restore_CGREFCODES_pre_Bonifica.sql
XBA_BONIFICA_AVV_CON_PENDENZE.prc
XBA_BONIFICA_AVVOCATO.prc
XBA_CARICA_AVV_CON_PENDENZE.prc
XBA_CREA_AVV_CON_PENDENZE.prc
XBA_MODIFICA_AVVOCATO.prc
XBA_RESTORE_TABELLE_AVVOCATI.prc
XBA_SALVA_TABELLE_AVVOCATI.prc
DROP_TABELLE_BONIFICA |
| --- | --- | --- |


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

Posizionarsi nel percorso /home/oracle/MEV-2019_21/bonifica_db/bonifica/; lanciare il comando:
imp siesxx/siesxx@sies file=AVVOCATO_REGINDE_18112020.dmp log=/home/oracle/MEV-2019_21/bonifica_db/log/AVVOCATO_REGINDE.log full=y
Nel file di log menzionato nel comando si potrà controllare l’esito dell’import (ovvero la creazione della tabella AVVOCATO_REGINDE_18112020 nel tablespace ‘siesxx’).
Posizionarsi nel percorso /home/oracle/MEV-2019_21/bonifica_db/; lanciare sequenzialmente i comandi:
./bonifica_avv_1.sh

immettere i parametri richiesti relativi al nome installazione, sid, utente e password e attendere il termine dell’elaborazione

( Il tempo di esecuzione verificato in fase di test è stato di circa 10 secondi per una base dati contenente 389000 records AVVOCATO, 272500 AVVOCATO_FASCICOLO_SIEP, 121227 AVVOCATO_FASCICOLO_SIUS e 6000 AVVOCATO_FASCICOLO_SIGE. Chiaramente il tempo varierà in base al n.ro di records delle suddette tabelle, variabili per ciascun Distretto, e dalla configurazione dei servers)

Al termine verificare:
che nel file /home/oracle/MEV-2019_21/bonifica_db/log/LOG_Bonifica_AVV_1.log non siano riportati errori oracle;
che nella base dati sia stata creata la tabella XBA_LOG_BONIFICA_AVVOCATI
accedere alla suddetta tabella, ordinandola per DATA_ESECUZIONE crescente,  e verificare che siano presenti i seguenti records

| Elaborazione | Elaborati | Data_Esecuzione |
| --- | --- | --- |
| ===> Inizio XBA_SALVA_TABELLE_AVVOCATI. Salvataggio delle tabelle AVVOCATO, AVVOCATO_FASCICOLO_SIEP, AVVOCATO_FASCICOLO_SIUS, AVVOCATO_FASCICOLO_SIGE, PARTI_UDIENZA_DIFENSORE, STORICO_AVVOCATO, AVVISI_AVVOCATO, NUOVA_ISTANZA  aggiungendo il suffisso _SXBA (Salvataggio per bonifica Avvocati). |  | YYYY-MM-DD HH:MM:SS.0 |
| CREATA TABELLA AVVOCATO_SXBA |  | YYYY-MM-DD HH:MM:SS.0 |
| CREATA TABELLA AVVOCATO_FASCICOLO_SIEP_SXBA |  | YYYY-MM-DD HH:MM:SS.0 |
| CREATA TABELLA AVVOCATO_FASCICOLO_SIUS_SXBA |  | YYYY-MM-DD HH:MM:SS.0 |
| CREATA TABELLA AVVOCATO_FASCICOLO_SIGE_SXBA |  | YYYY-MM-DD HH:MM:SS.0 |
| CREATA TABELLA PARTI_UDIENZA_DIFENSORE_SXBA |  | YYYY-MM-DD HH:MM:SS.0 |
| CREATA TABELLA STORICO_AVVOCATO_SXBA |  | YYYY-MM-DD HH:MM:SS.0 |
| CREATA TABELLA AVVISI_AVVOCATO_SXBA |  | YYYY-MM-DD HH:MM:SS.0 |
| CREATA TABELLA NUOVA_ISTANZA_SXBA |  | YYYY-MM-DD HH:MM:SS.0 |
| CREATA TABELLA CG_REF_CODES_SXBA |  | YYYY-MM-DD HH:MM:SS.0 |
| CREATA TABELLA AVVOCATO_BONIF |  | YYYY-MM-DD HH:MM:SS.0 |
| CREATA TABELLA AVVOCATO_FASCICOLO_SIEP_BONIF |  | YYYY-MM-DD HH:MM:SS.0 |
| CREATA TABELLA AVVOCATO_FASCICOLO_SIUS_BONIF |  | YYYY-MM-DD HH:MM:SS.0 |
| CREATA TABELLA AVVOCATO_FASCICOLO_SIGE_BONIF |  | YYYY-MM-DD HH:MM:SS.0 |
| CREATA TABELLA PARTI_UDIENZA_DIFENSORE_BONIF |  | YYYY-MM-DD HH:MM:SS.0 |
| CREATA TABELLA AVVOCATO_STORICO_AVVOCATO_BONIF |  | YYYY-MM-DD HH:MM:SS.0 |
| CREATA TABELLA AVVISI_AVVOCATO_BONIF |  | YYYY-MM-DD HH:MM:SS.0 |
| CREATA TABELLA NUOVA_ISTANZA_BONIF |  | YYYY-MM-DD HH:MM:SS.0 |
| ===> Fine XBA_SALVA_TABELLE_AVVOCATI. |  | YYYY-MM-DD HH:MM:SS.0 |


In caso di errori o di assenza di alcuna delle tabelle sopra riportate, consultare i tecnici dell’assistenza Eng ed, eventualmente,  su loro indicazione eseguire la procedura bonifica_restore, descritta in fondo a questo paragrafo.

./bonifica_avv_2.sh

immettere i parametri richiesti relativi al nome installazione, sid, utente e password e attendere il termine dell’elaborazione

( Il tempo di esecuzione verificato in fase di test è stato di circa 10 secondi)

Al termine verificare:
che nel file /home/oracle/MEV-2019_21/bonifica_db/log/LOG_Bonifica_AVV_2.log non siano riportati errori oracle;
che nella base dati sia stata creata la tabella XBA_AVVOCATI_CON_PENDENZE;
accedere alla tabella XBA_LOG_BONIFICA_AVVOCATI, ordinandola per DATA_ESECUZIONE crescente,  e verificare che siano presenti i seguenti records (i numeri riportati nella colonna Elaborati sono esempi, essi varieranno per ogni Distretto)

| Elaborazione | Elaborati | Data_Esecuzione |
| --- | --- | --- |
| Inizio XBA_MODIFICA_AVVOCATO. Aggiunta di 6 colonne (PEC, FLAG_REGINDE, DESCR_COMUNE_STUDIO, COD_STATO_NASCITA_AVV, DESC_LUOGO_NAS_REGINDE, ID_AVVOCATO_BONIFICATO), funzionali alla bonifica Avvocati e alla nuova gestione di AVVOCATO con certificazione REGINDE. |  | YYYY-MM-DD HH:MM:SS.0 |
| Fine XBA_MODIFICA_AVVOCATO. |  | YYYY-MM-DD HH:MM:SS.0 |
| Inizio XBA_CREA_AVV_CON_PENDENZE. La tabella XBA_AVVOCATI_CON_PENDENZE conterrà i dati di transito per eseguire la bonifica AVVOCATO. |  | YYYY-MM-DD HH:MM:SS.0 |
| Fine XBA_CREA_AVV_CON_PENDENZE. |  | YYYY-MM-DD HH:MM:SS.0 |
| Inizio XBA_CARICA_AVV_CON_PENDENZE. Si estraggono gli avvocati SIES per i quali sussistono fascicoli pendenti del Distretto in almeno un sottosistema (SIEP, SIUS, SIGE). I dati estratti vengono inseriti nella tabella XBA_AVVOCATI_CON_PENDENZE. | 1 | YYYY-MM-DD HH:MM:SS.0 |
| ============================================ |  | YYYY-MM-DD HH:MM:SS.0 |
| = Totale Avvocati SIEP con pendenze : | 19923 | YYYY-MM-DD HH:MM:SS.0 |
| = Totale Avvocati SIUS con pendenze : | 6136 | YYYY-MM-DD HH:MM:SS.0 |
| = Totale Avvocati SIGE con pendenze : | 821 | YYYY-MM-DD HH:MM:SS.0 |
| = Totale Fascicoli SIEP pendenti : | 56387 | YYYY-MM-DD HH:MM:SS.0 |
| = Totale Fascicoli SIUS pendenti : | 9671 | YYYY-MM-DD HH:MM:SS.0 |
| = Totale Fascicoli SIGE pendenti : | 1086 | YYYY-MM-DD HH:MM:SS.0 |
| ============================================ |  | YYYY-MM-DD HH:MM:SS.0 |
| Fine XBA_CARICA_AVV_CON_PENDENZENEW. |  | YYYY-MM-DD HH:MM:SS.0 |


In caso di errori o di assenza di alcuna delle righe sopra riportate, consultare i tecnici dell’assistenza Eng ed, eventualmente,  su loro indicazione eseguire la procedura bonifica_restore, descritta in fondo a questo paragrafo.

./bonifica_avv_3.sh

immettere i parametri richiesti relativi al nome installazione, sid, utente e password e attendere il termine dell’elaborazione

( Il tempo di esecuzione verificato in fase di test è stato di circa 10 minuti)

Al termine verificare:
che nel file /home/oracle/MEV-2019_21/bonifica_db/log/LOG_Bonifica_AVV_3.log non siano riportati errori oracle;
accedere alla tabella XBA_LOG_BONIFICA_AVVOCATI, ordinandola per DATA_ESECUZIONE crescente,  e verificare che siano presenti i seguenti records (i numeri riportati nella colonna Elaborati sono esempi, essi varieranno per ogni Distretto)

| Elaborazione | Elaborati | Data_Esecuzione |
| --- | --- | --- |
| Inizio XBA_BONIFICA_AVV_CON_PENDENZE. Scansione degli Avvocati con pendenze ordinati per COD_FISCALE, DATA_INSERIMENTO e ID_AVVOCATO decrescenti; si individua così prima l AVVOCATO principale. |  | YYYY-MM-DD HH:MM:SS.0 |
| ============================================ |  | YYYY-MM-DD HH:MM:SS.0 |
| =  Totale Avvocati con pendenze          : | 26880 | YYYY-MM-DD HH:MM:SS.0 |
| =  Avvocati presenti in REGINDE          : | 16579 | YYYY-MM-DD HH:MM:SS.0 |
| =  Avvocati assenti in REGINDE           : | 10301 | YYYY-MM-DD HH:MM:SS.0 |
| =  Avvocati certificati REGINDE          : | 7229 | YYYY-MM-DD HH:MM:SS.0 |
| =  Avvocati collegati                    : | 9350 | YYYY-MM-DD HH:MM:SS.0 |
| =  Avvocati con pendenze aggiornati      : | 16579 | YYYY-MM-DD HH:MM:SS.0 |
| ============================================ |  | YYYY-MM-DD HH:MM:SS.0 |
| Fine XBA_BONIFICA_AVV_CON_PENDENZE. |  | YYYY-MM-DD HH:MM:SS.0 |


In caso di errori o di assenza di alcuna delle righe sopra riportate, consultare i tecnici dell’assistenza Eng ed, eventualmente,  su loro indicazione eseguire la procedura bonifica_restore, descritta in fondo a questo paragrafo.

./bonifica_avv_4.sh

immettere i parametri richiesti relativi al nome installazione, sid, utente e password e attendere il termine dell’elaborazione

( Il tempo di esecuzione verificato in fase di test è stato di circa 30 minuti)

Al termine verificare:
che nel file /home/oracle/MEV-2019_21/bonifica_db/log/LOG_Bonifica_AVV_4.log non siano riportati errori oracle;
accedere alla tabella XBA_LOG_BONIFICA_AVVOCATI, ordinandola per DATA_ESECUZIONE crescente, e verificare che siano presenti i seguenti records (i numeri riportati nella colonna Elaborati sono esempi, essi varieranno per ogni Distretto)

| ELABORAZIONE | ELABORATI | DATA_ESECUZIONE |
| --- | --- | --- |
| Inizio XBA_BONIFICA_AVVOCATO. Individuazione degli avvocati SIES deputati a divenire certificati REGINDE. | 1 | YYYY-MM-DD HH:MM:SS.0 |
| ============================================ |  | YYYY-MM-DD HH:MM:SS.0 |
| =  Avvocati con pendenze letti           : | 16579 | YYYY-MM-DD HH:MM:SS.0 |
| =  AVVOCATI aggiornati                   : | 16579 | YYYY-MM-DD HH:MM:SS.0 |
| =  Avvocati certificati REGINDE          : | 7229 | YYYY-MM-DD HH:MM:SS.0 |
| =  Avvocati collegati ai referenti       : | 9350 | YYYY-MM-DD HH:MM:SS.0 |
| =  AVVOCATO_FASCICOLO_SIEP aggiornati    : | 25791 | YYYY-MM-DD HH:MM:SS.0 |
| =  AVVOCATO_FASCICOLO_SIUS aggiornati    : | 4896 | YYYY-MM-DD HH:MM:SS.0 |
| =  AVVOCATO_FASCICOLO_SIGE aggiornati    : | 550 | YYYY-MM-DD HH:MM:SS.0 |
| =  PARTI_UDIENZA_DIFENSORE aggiornati    : | 0 |  |
| =  STORICO_AVVOCATO aggiornati           : | 90936 |  |
| =  AVVISI_AVVOCATO aggiornati            : | 3 |  |
| =  NUOVA_ISTANZA aggiornati              : | 1556 |  |
| ============================================ |  |  |
| Fine XBA_BONIFICA_AVVOCATO |  | YYYY-MM-DD HH:MM:SS.0 |


In caso di errori o di assenza di alcuna delle righe sopra riportate, consultare i tecnici dell’assistenza Eng ed, eventualmente,  su loro indicazione eseguire la procedura bonifica_restore, descritta in fondo a questo paragrafo.

N.B. Le segnalazioni del tipo:
ORA-00001: violata restrizione di unicità
ORA-00955: name is already used by an existing object
Cartella log già presente
ORA-04043: object does not exist
sono da considerarsi warning e non errori.

Per accedere ad oracle utilizzare qualsiasi strumento tipo toad, developer, ecc. Le tabelle di appoggio create per l’esecuzione della procedura di Bonifica Avvocati devono essere conservate per almeno 6 mesi, per permettere eventuali attività di verifica.

Attività di restore delle tabelle (da eseguire solo in caso di errori e su indicazione dell’assistenza ENG)

./bonifica_restore.sh

immettere i parametri richiesti relativi al nome installazione, sid, utente e password e attendere il termine dell’elaborazione

( Il tempo di esecuzione verificato in fase di test è stato di circa 2 minuti)

Al termine verificare:
che nel file /home/oracle/MEV-2019_21/bonifica_db/log/ /log/LOG_Bonifica_AVV_Restore.log non siano riportati errori oracle;
accedere alla tabella XBA_LOG_BONIFICA_AVVOCATI, ordinandola per DATA_ESECUZIONE crescente, e verificare che siano presenti i seguenti records

| ELABORAZIONE | ELABORATI | DATA_ESECUZIONE |
| --- | --- | --- |
| ===> Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore di tutte le tabelle interessate dalla procedura di bonifica. |  | YYYY-MM-DD HH:MM:SS.0 |
| ============================================ |  | YYYY-MM-DD HH:MM:SS.0 |
| Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore tabella AVVOCATO effettuata. |  | YYYY-MM-DD HH:MM:SS.0 |
| Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore tabella AVVOCATO_FASCICOLO_SIEP effettuata. |  | YYYY-MM-DD HH:MM:SS.0 |
| Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore tabella AVVOCATO_FASCICOLO_SIUS effettuata. |  | YYYY-MM-DD HH:MM:SS.0 |
| Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore tabella AVVOCATO_FASCICOLO_SIGE effettuata. |  | YYYY-MM-DD HH:MM:SS.0 |
| Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore tabella PARTI_UDIENZA_DIFENSORE effettuata. |  | YYYY-MM-DD HH:MM:SS.0 |
| Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore tabella STORICO_AVVOCATO effettuata. |  | YYYY-MM-DD HH:MM:SS.0 |
| Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore tabella AVVISI_AVVOCATO effettuata. |  | YYYY-MM-DD HH:MM:SS.0 |
| Inizio XBA_RESTORE_TABELLE_AVVOCATI. Restore tabella NUOVA_ISTANZA effettuata. |  |  |
| ===> Fine XBA_RESTORE_TABELLE_AVVOCATI. Restore di tutte le tabelle interessate dalla procedura di bonifica. |  | YYYY-MM-DD HH:MM:SS.0 |


In caso di errori o di assenza di alcuna delle righe sopra riportate, consultare i tecnici dell’assistenza Eng ed attendere loro indicazioni.
## Attività di installazione ed aggiornamento di alcune Tabelle fisse e dell’Applicazione
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
Copiare il contenuto della cartella aggiorna_db nella cartella /home/oracle/MEV-2019_21/, che conterrà i seguenti files:
| aggiorna_db.zip | Database | Scripts/procedure per aggiornamento base dati: 
XAT_SALVA_TABELLE_PRE_ALLINEA.prc
Aggiornamento_CG_REF_CODES_NAZIONE_esercizio.sql
Aggiornamento_CG_REF_CODES_PROVINCIA_esercizio.sql
Aggiornamento_CODICI_SIES_NSC_COMUNE_esercizio.sql
Aggiornamento_CODICI_SIES_NSC_NAZIONE_esercizio.sql
Aggiornamento_TABELLA_COMUNE_esercizio.sql
Alter_CODICI_SIES_NSC.sql
Alter_Comune.sql
Disabilita_Funzioni_Inserimento_Modifica_Difensore
Insert_FUNZIONE-FUNZIONE_PROFILO.sql
Insert_REGIONE.sql
Restore_CGREFCODES_NAZIONE.sql
Restore_CGREFCODES_PROVINCIA.sql
Restore_CGREFCODES_REGIONE.sql
Restore_CODICISIESNSC_COMUNE.sql
Restore_CODICISIESNSC_NAZIONE.sql
Restore_COMUNE_pre_allineamento.sql
Restore_Funzione_FunzioneProfilo.sql |
| --- | --- | --- |


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

immettere i parametri richiesti relativi al nome installazione, sid, utente e password e attendere il termine dell’elaborazione

( Il tempo di esecuzione verificato in fase di test è stato di circa 5 minuti)

Al termine verificare:
che nel file /home/oracle/MEV-2019_21 /log/ AllineaTabelle_&nomeinstallazione..log non siano riportati errori oracle;
accedere alla Base Dati e verificare che siano state create le tabelle COMUNE_SXALLTF, CG_REF_CODES_SXALLTF e CODICI_SIES_NSC_SXALLTF
sempre collegati alla Base Dati eseguire le seguenti queries .sql e verificarne il risultato

SELECT count(*) FROM COMUNE c         				risultato  13327

SELECT count(*) FROM CG_REF_CODES WHERE RV_DOMAIN = 'PROVINCIA'  	ris. 117

SELECT count(*) FROM CG_REF_CODES WHERE RV_DOMAIN = 'REGIONE'	 	ris. 22

SELECT count(*) FROM CG_REF_CODES WHERE RV_DOMAIN = 'NAZIONE'	 	ris. 269

SELECT count(*) FROM CODICI_SIES_NSC WHERE CO_DOMAIN = 'COMUNE' 	ris. 8607

SELECT count(*) FROM CODICI_SIES_NSC WHERE CO_DOMAIN = 'NAZIONE'	ris. 204

In caso di messaggi di errore o di non corrispondenza dei suddetti risultati, consultare i tecnici dell’assistenza Eng ed, eventualmente,  su loro indicazione eseguire gli script di restore presenti nella cartella /home/oracle/MEV-2019_21 /.


N.B. Le segnalazioni del tipo:
ORA-00001: violata restrizione di unicità
ORA-00955: name is already used by an existing object
Cartella log già presente
ORA-04043: object does not exist
sono da considerarsi warning e non errori.

Accedere ad oracle (con qualsiasi strumento tipo toad, developer…) come utente siesxx e compilare tutte le procedure e i package che non risultano compilate.
ATTENZIONE: la procedura SUPER_SOGGETTO_PREGR e il package CARICA_RES potrebbero restare non compilate: non è da considerarsi errore.
## Installazione applicazione
## Deploy Applicazione
Aprire una shell linux sul server SIES e loggarsi come utente “root”;
Posizionarsi sotto la cartella:
“/var/SIES/CONFIG”;
Editare il file “f3b.properties” ed aggiungere alla fine del file le seguenti righe:
# MEV_21 RegInde parametri di configurazione collegamento SERVER nazionale
EndpointAddress= http://reginde.processotelematico.giustizia.it.

NB: Tali valori devono essere parametrizzati in base all’ambiente di installazione del servizio reso disponibile dal sistema REGINDE per la verifica di conformità.
Scaricare i files “sies.war” sul server SIES ed eseguire le seguenti operazioni:
posizionarsi sotto la cartella:
“/opt/jboss-eap-6.4/standalone/deployments”;
cancellare il vecchio eseguibile (se esistente) “sies.war” e la copia deployata “sies.war.deployed”;
copiare, nello stesso percorso, il nuovo eseguibile “sies.war”;
posizionarsi sotto la cartella:
“/opt/jboss-eap-6.4/standalone”;
cancellare le cartelle “data”, “log” e “tmp” (se esistenti);

Attenzione!! Prima di avviare il server jboss assicurarsi di aver cancellato gli elementi già esistenti seguendo le istruzioni ai punti 4.b e 4.e. All’avvio, infatti, tali cartelle verranno ricreate.

Avviare il processo di gestione delle code tramite il comando: “/etc/init.d/imq start”.
Per verificare la partenza delle code si può analizzare il file di log “log.txt”, presente nel percorso “/var/mq/instances/imqbroker/log”, controllando al suo interno la presenza della dicitura “Broker 'imqbroker@nomemacchina:7676' pronto”;
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”.
## Attività di configurazione
N.A.
## Attività di post-installazione
N.A.