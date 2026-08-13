---
uniqueName: siut-sies-pr-1-5-20221026-pianodirilascio021regind
displayName: "SIUT SIES PR 1 5 20221026 Piano di Rilascio 021 RegInde SIES"
category: "GENERAL"
tags: []
---

# SIUT-SIES-PR-1.5-20221026-Piano_di_Rilascio_021_RegInde_SIES

> **File originale:** `MEV/SCHEDA_021/Docs/SIUT-SIES-PR-1.5-20221026-Piano_di_Rilascio_021_RegInde_SIES.docx`  
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
| Data approvazione | 26/10/2022 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 30/07/2021 | Prima Emissione |  |
| 1.1 | 08/10/2021 | Seconda Emissione | Revisione Completa |
| 1.2 | 24/01/2022 | Terza Emissione | Revisione Completa |
| 1.3 | 22/04/2022 | Quarta Emissione | Revisione Completa |
| 1.4 | 15/09/2022 | Quinta Emissione | Modificati i riferimenti ai documenti di bonifica ed aggiornamento; corretta la versione di installazione del SIES |
| 1.4 | 26/10/2022 | Sesta Emissione | Modificati i riferimenti ai documenti di bonifica ed aggiornamento; corretta la versione di installazione del SIES |


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
6.2	Attività di installazione ed esecuzione procedura batch Bonifica Difensori	10
6.3	Attività di installazione ed aggiornamento di alcune Tabelle fisse e dell’Applicazione	10
6.4	Installazione applicazione	10
6.4.1	Deploy Applicazione	10
6.5	Attività di configurazione	11
6.6	Attività di post-installazione	11


# Introduzione
## Scopo del documento
Il presente documento descrive il piano di rilascio degli interventi realizzati nell’ambito del Sistema Integrato Esecuzione Sorveglianza per la realizzazione di quanto dettagliato nella scheda di intervento di riferimento.
Gli interventi in oggetto sono rilasciati nell’ambito della release 12.4.23.0-MEV_2019_021 di SIES.
Riporta inoltre le modalità di installazione degli aggiornamenti in ambiente di esercizio.
## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
| RIF1. | SIUT-SIE-SI-2.6-20220422-Specifiche-intervento-021-SIES.pdf | Scheda Intervento |
| RIF2. | SIUT-SIES-MG-1.6-20221026-Istruzioni_Bonifica_Difensori_021_RegInde_SIES.pdf | Manuale Gestione |
| RIF3. | SIUT-SIES-MG-1.6-20221026-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_SIES.pdf | Manuale Gestione |

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
Il presente documento descrive il piano di rilascio del software relativo alla MEV-2019_021 di SIES, contenente l’integrazione della suddetta MEV con la versione SIES 12.4.23.0.

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
| - | SIUT-SIE-SI-2.6-20220422-Specifiche-intervento-021-SIES.pdf | - | Integrazione del SIES con ReGIndE |

# Dettaglio degli elementi oggetto del rilascio
| Nome File | Path | Motivazione-riferimento |
| --- | --- | --- |
| aggiorna_db.zip | Database | Script per aggiornamento base dati: 
Aggiornamento, inserimento e cancellazione in varie tabelle
Procedura di salvataggio tabelle
Aggiornamento versione SIES in tabella “VERSIONE” |
| sorgenti.zip | Sorgenti | Sorgenti software |
| sies.war | Applicazione | Eseguibile dell’applicazione SIES |
| documentazione.zip | Documentazione | SIUT-SIES-PR-1.5-20221026-Piano_di_Rilascio_021_RegInde_SIES.pdf
SIUT-SIE-MU-1.1-20211008-Manuale_Utente_021_RegInde_SIES.pdf
SIUT-SIE-CT-1.1-20211008-Allegato_al_piano_test_021_RegInde_SIES.xlsx
SIUT-SIES-MG-1.6-20221026-Istruzioni_Bonifica_Difensori_021_RegInde_SIES.pdf
SIUT-SIES-MG-1.6-20221026-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_SIES.pdf
SIUT-SIE-PT-1.0-20210730-Piano_dei_Test_021_RegInde_SIES.pdf |
| Bonifica.zip | Bonifica Database | Contiene procedure e script per eseguire la bonifica |
| Aggiornamento Tabelle Fisse.zip | Aggiornamento TabelleFisse | Contiene procedure e script per eseguire l’aggiornamento delle tabelle fisse |
| Note-osservazioni |  |  |

# Installazione
## Prerequisiti
Per l’installazione della release SIES oggetto del presente rilascio è necessario aver installato la precedente release 12.4.23.0.
L’installazione della release si articola sulle quattro seguenti attività:
effettuare preliminarmente uno snapshot del DB di modo che in caso di esito negativo di una o più verifiche riportate nei successivi STEP si possa riportare il DB alla situazione iniziale;
esecuzione di una procedura batch per la bonifica dei Difensori sulla base dell’estrazione degli Avvocati presenti in ReGIndE;
aggiornamento della tabella COMUNE, dei domini PROVINCIA, REGIONE, NAZIONE della Tabella CG_REF_CODES e dei domini COMUNE e NAZIONE della Tabella CODICI_SIES_NSC sulla base delle tabelle Fisse, fornite dall’Amministrazione;
installazione dell’Applicazione aggiornata.
Le attività vanno eseguite nell’ordine sopra indicato solo se ognuna non ha fornito messaggi di errore nei file o nelle tabelle di log; per esempio, l’attività 2) può essere eseguita solo se l’attività 1) non ha fornito messaggi di errore nella tabella di log XBA_LOG_BONIFICA_AVVOCATI.
## Attività di installazione ed esecuzione procedura batch Bonifica Difensori
La descrizione dettagliata delle operazioni da eseguire per quest’attività sono riportate nel documento SIUT-SIES-MG-1.6-20221026-Istruzioni_Bonifica_Difensori_021_RegInde_SIES.pdf, da considerarsi parte integrante del presente documento.

Se  tutte le attività descritte nel suddetto documento, ad esclusione di quelle descritte al par. 3.2.7, non hanno presentato errori si potrà procedere con le attività descritte nel successivo paragrafo.

In caso di errori consultare i tecnici dell’assistenza Engineering ed attendere loro indicazioni.
## Attività di installazione ed aggiornamento di alcune Tabelle fisse e dell’Applicazione
La descrizione dettagliata delle operazioni da eseguire per quest’attività sono riportate nel documento SIUT-SIES-MG-1.6-20221026-Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_SIES.pdf, da considerarsi parte integrante del presente documento.

Se  tutte le attività descritte nel suddetto documento, ad esclusione di quelle descritte al par. 3.3.2, non hanno presentato errori, si potrà procedere con le attività descritte nel successivo paragrafo.

In caso di errori consultare i tecnici dell’assistenza Engineering ed attendere loro indicazioni.
## Installazione applicazione
## Deploy Applicazione
Aprire una shell linux sul server SIES e loggarsi come utente “root”;
Posizionarsi sotto la cartella:
“/var/SIES/CONFIG”;
Editare il file “f3b.properties” ed aggiungere alla fine del file le seguenti righe:
# MEV_021 RegInde parametri di configurazione collegamento SERVER nazionale
EndpointAddress=http://reginde.processotelematico.giustizia.it/ServiziInterrogazioneRegindeExt/ServiziInterrogazioneInterni
oppure in caso di connessione in https:
EndpointAddress=https://reginde.processotelematico.giustizia.it/ServiziInterrogazioneRegindeExt/ServiziInterrogazioneInterni

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