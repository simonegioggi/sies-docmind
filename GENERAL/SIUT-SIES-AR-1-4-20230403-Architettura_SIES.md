---
uniqueName: siut-sies-ar-1-4-20230403-architetturasies
displayName: "SIUT SIES AR 1 4 20230403 Architettura SIES"
category: "GENERAL"
tags: []
---

# SIUT-SIES-AR-1.4-20230403-Architettura_SIES

> **File originale:** `MEV/SCHEDA_013/SIUT-SIES-AR-1.4-20230403-Architettura_SIES.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A&Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del sistema informativo unitario telematico, la manutenzione degli attuali sistemi dell’area penale del Ministero della Giustizia e servizi correlati. Lotto 1”.

Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Vito Bufi |  |
| Verificato da | Fabio Gattamorta | Referente PMO e Qualità |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 03/04/2023 |  |
| Livello di riservatezza | L3 |  |

Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 13/12/2016 | Prima Emissione |  |
| 1.1 | 06/03/2017 | Revisione | Descrizione WEB-Service |
| 1.2 | 12/04/2017 | Revisione | Aggiornamento descrizione WEB-service |
| 1.3 | 29/01/2021 | Revisione | Adeguamento al formato standard SIUT |
| 1.4 | 03/04/2023 | Revisione | Inserito paragrafo 3.5 |



Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Ruolo |
| --- | --- | --- | --- |
| Aurora Garofalo | Amministrazione |  | Responsabile Unico Procedimento |
| Oris Orlando | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Fabio Mazzocchi | RTI |  | Responsabile Manutenzione Correttiva |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Alessandro Falleni | RTI |  | Referente Sicurezza |
| Fabio Gattamorta | RTI |  | Referente PMO e Qualità |
| Francesco Rosati | RTI |  | Referente Qualità e Sicurezza |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |


INDICE DEI CONTENUTI
1	Introduzione	5
1.1	Scopo del documento	5
1.2	Riferimenti	5
1.3	Glossario	5
2	Introduzione	6
3	Disegno generale del sistema	7
3.1	Interconnessione tra nodi SIES	8
3.2	SIES-NSC	8
3.3	PST vs SIUS AVVOCATURA	9
3.4	SIUS AVVOCATURA vs SISTEMI SIES	10
3.5	PagoPA/PST - SIES	11
4	Architettura del SISTEMA SIES	15
5	Architettura SIUS AVVOCATURA	17
6	Generazione dei report con WindWard	18
7	Software di base (Stack)	23
8	Librerie utilizzate	24
9	WEB Service	26
10	Start-Stop Application Server	27


# Introduzione
## Scopo del documento

Questo documento descrive l'architettura di sistema adottata per il progetto SIES.


## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
|  |  |  |


## Glossario
### Definizioni
| Definizione | Descrizione |
| --- | --- |
|  |  |



### Acronimi e abbreviazioni
| Sigla | Descrizione |
| --- | --- |
| DB | Data Base |
| BDI | Base Dati Integrata |
| DAO | Data Access Object |
| HTTP | HyperText Transfer Protocol |
| HTTPS | HyperText Transfer Protocol over Secure Socket Layer |
| JMS | Java Message Service |
| MVC | Model View Controller |
| NSC | Nuovo Sistema Casellario |
| RUG | Rete Unitaria del Ministero della Giustizia |
| SIC | Sistema Informativo Casellario giudiziale |
| SIEP | Sottosistema Informativo delle Esecuzioni Penali |
| SIES | Sistema Informativo dell'Esecuzione Penale e Sorveglianza |
| SIUS | Sottosistema Informativo Uffici Sorveglianza |
| WS | Web Service |



# Introduzione
Questo documento descrive l'architettura di sistema adottata per il progetto SIES.
Di seguito saranno descritte:
Il disegno generale del sistema, in cui si evidenziano tutte le componenti di SIES e i sistemi con cui sussistono scambi informativi.
L’architettura di sistema con la descrizione della struttura delle parti che compongono l’installazione software completa includendo le responsabilità dei vari componenti e le interconnessioni e tecnologie utilizzate.
Il software di base utilizzato.
# Disegno generale del sistema
Si riporta di seguito il disegno delle principali componenti del sistema SIES ed i sistemi con cui SIES si interfaccia.



Figura 1 Schema generale del sistema SIES



La figura riporta:
Nodi SIES distribuiti sul territorio;
NSC, il sistema centralizzato del Casellario;
PST, il sistema centralizzato del Portale dei Servizi Telematici (PST);
SIUS Avvocatura, il sistema centralizzato per la fruizione dei servizi destinati alla consultazione dei Procedimenti penali SIUS.

Di seguito sono descritte le modalità di interconnessione tra i diversi componenti e i flussi informativi scambiati.

## Interconnessione tra nodi SIES
I diversi nodi SIES sono interconnessi tra di loro mediante un sistema di messaging basato sullo standard Java Message Service (JMS). JMS è un insieme di API (Application Program Interface) capaci di fornire servizi di messaggistica; più precisamente si tratta di una serie d’interfacce che permettono di accedere e di utilizzare i servizi di un sistema di middleware orientato ai messaggi, utilizzando Java come linguaggio.
In sostanza JMS fornisce un metodo standard tramite il quale le applicazioni possono creare, inviare e ricevere i messaggi in modalità asincrona.
Ogni nodo ha il suo server JMS, non esistendo un unico server JMS centralizzato su cui pubblicare ed eventualmente sottoscriversi. La modalità di invio messaggi è point-to-point.
Ogni server JMS è configurato per comunicare con gli altri server via protocollo HTTP. Al suo interno sono state configurate due code, una per i messaggi in partenza ed una per i messaggi in arrivo. Il server JMS assicura all’applicativo SIES ildelivery dei messaggi consegnati, per fare questo persiste i messaggi su una base dati dedicata.
I dati scambiati tra i distretti sono memorizzati sulla tabella Messaggio il cui contenuto è descritto nel documento SIGI_PNL_ML_2017 03 06_1.1_Modello dei Dati_SIES.doc
La figura seguente illustra quanto esposto.

Figura 2 Interconnessione tramite JMS


## SIES-NSC
I flussi informativi che coinvolgono il sistema SIES e il sistema del Casellario sono diversi:
Invio Titolo Esecutivo da SIEP verso NSC​;
​Invio Fogli Complementari da SIEP/SIUS verso NSC;
Invio Titolo Esecutivo da NSC verso SIEP;
Richiesta Certificato del Casellario da SIEP-SIUS;
Interconnessione WEB tra SIES ed NSC: ovvero da SIES si può aprire il modulo di interoperabilità per effettuare ricerche direttamente su NSC. L’utente SIES non necessita di autenticarsi nuovamente sul sistema NSC perché le sue credenziali viaggiano attraverso il protocollo SAML.

I primi 4 flussi sono contenuti in un “pacchetto applicativo” proprio di SIES; il flusso 5 pur partendo da SIES apre un’interfaccia di NSC.
Gli scambi avvengono mediante protocollo HTTPS su rete RUG.




Figura 3 Interconnessione/interoperabilità con NSC


## PST vs SIUS AVVOCATURA
Il Portale dei Servizi Telematici PST si occupa dell’autenticazione e dell’autorizzazione degli avvocati alla fruizione delle funzionalità del sistema SIUS Avvocatura.
L’accesso alle funzionalità avviene mediante un meccanismo di reverse-proxy in modo tale che il sistema SIUS Avvocatura non sia mai esposto direttamente all’esterno della rete RUG. L’interconnessione del browser dell’utente finale avviene solo con il proxy di PST che si occupa di attivare la funzionalità di SIUS Avvocatura. La risposta di SIUS Avvocatura arriva al proxy che si occupa di ritornarla al browser dell’utente. Tutti gli scambi avvengono con protocollo HTTPS.
Per il dettaglio della configurazione si rimanda al documento 
SIUT-GEN-MG-2.3-20220131-Manuale_Configurazione_Ambienti_AVVOCATURA.pdf


Figura 4 Interconnessione PST con SIUS Avvocatura

## SIUS AVVOCATURA vs SISTEMI SIES
Il modulo SIUS Avvocatura eroga i servizi di ricerca agli utenti mediante la chiamata di web-service esposti dai nodi SIES. Le chiamate ai web-services sono sincrone e avvengono mediante protocollo HTTPS sulla rete RUG. Di seguito la schematica rappresentazione dell’interconnessione di SIUS Avvocatura con uno dei nodi SIES.
Per il dettaglio della configurazione si rimanda al documento SIUT-GEN-MG-2.3-20220131-Manuale_Configurazione_Ambienti_AVVOCATURA.pdf
Per il dettaglio dei WebServices si rimanda al documento SIGI_PNL_WS_2016 11 30_2.0_Descrizione Servizi Web AVVOCATURA-SIUS.doc




Figura  Interconnessione SIUS Avvocatura SIES




## PagoPA/PST - SIES
Di seguito si rappresenta brevemente l’architettura di cooperazione del servizio PagoPA/PST con il sistema SIES





In figura troviamo:
Nodi SIES distribuiti sul territorio;
PST, il sistema centralizzato del Portale dei Servizi Telematici (PST) che espone i servizi necessari per generare i bollettini e verifica pagamento.



### Configurazione del certificato di comunicazione
Propedeutico alla prosecuzione dei seguenti passi è che il PST fornisca al SIES la chiave pubblica (file in formato “.pem”) associata ai servizi che espongono e che devono essere richiamati; per rendere più chiari i passi descritti di seguito presupporremo che il file si chiami, come in ambiente di collaudo, “processotelematico-giustizia-it.pem”.
Una volta ottenuta la chiave pubblica si dovrà procedere come segue:

Registrazione della chiave pubblica di PagoPA/PST all’interno del Truststore di SIES (sies.jks):
Importare il file processotelematico-giustizia-it.cer in sies.jks
Distribuire il Sies.jks ai vari distretti
Spostare il file sies.jks all’interno del percorso predefinito /var/SIES/CONFIG/certs, sostituendo il precedente file.

Inviare al PST la chiave pubblica contenuta nel Keystore di SIES (serversies.jks): la chiave pubblica è unica per tutti i distretti


### Batch di verifica stato del Pagamento
Il batch sviluppato si occupa, con cadenza giornaliera, di interrogare il servizio esitoPagamenti per conoscere lo stato di un certo pagamento (IUV).
Il batch interroga PagoPA per verificare lo stato dei pagamenti dei bollettini presenti sulla tabella BOLLETTINO_PAGOPA per i quali non risulta ancora pagato il bollettino (DATA_AVV_PAGAMENTO null e STATO_PAGAMENTO=NP) e per i quali le date DATA_SCADENZA e DATA_ULTIMO_CONTROLLO soddisfino le condizioni sotto descritte
Saranno presenti due parametri configurabili all’interno del file “f3b.properties”:
inScadenzaTraGiorni = indica il numero di giorni che determinerà l’intervallo di tempo da considerare per selezionare i bollettini da verificare. La condizione è la seguente:
data_scadenza between sysdate - inScadenzaTraGiorni and sysdate + inScadenzaTraGiorni
Se, quindi, il valore di inScadenzaTraGiorni è uguale a 3, si prenderanno in considerazione tutti i bollettini che sono scaduti da tre giorni o che scadranno tra tre giorni.
Il valore iniziale sarà settato per default a 3.
controllateDaGiorni = ogni volta che il batch è eseguito, aggiorna per ogni bollettino elaborato, la DATA_ULTIMO_CONTROLLO nella tabella BOLLETTINO_PAGOPA. Se il valore di controllateDaGiorni è diverso da zero, il batch prende in considerazione tutti i bollettini che hanno DATA_ULTIMO_CONTROLLO < SYSDATE-controllateDaGiorni di modo da elaborare solo i bollettini che sono NON stati controllati negli ultimi n giorni, di modo da non appesantire le richieste verso pagoPA.
Il valore iniziale sarà settato per default a 0 (ovvero questa condizione non viene presa in considerazione dal batch).
Se un bollettino risulta pagato il batch aggiorna lo stato del pagamento e la data avvenuto pagamento. Inoltre se il pagamento che sta registrando risulterà essere il primo di un pagamento rateizzato, aggiornerà anche la colonna DATA_SCADENZA delle altre rate collegate allo stesso ordine di ingiunzione al pagamento. La data scadenza della rate successive è l'ultimo giorno di ogni mese a partire dal mese successivo il pagamento della prima rata.
Questo servizio è stato sviluppato all’interno dello stesso sistema SIES, ed è schedulato per l’esecuzione attraverso le librerie quartz incluse nel progetto stesso.
Si sono aggiunti altri 2 parametri all’interno del file “f3b.properties”, il primo per abilitare/disabilitare il batch ed il secondo per configurarne la schedulazione attraverso la sintassi crontab, che sono:
PagoPaSchedulerEnabled -> True per abilitare il batch/False per disabilitare il batch
PagoPaCronExpression -> Valore espresso attraverso la sintassi crontab. Di default è stata inserita la stringa “0 0 4 * * ?” che rappresenta una schedulazione giornaliera alle 04:00 di ogni giorno.
Di seguito alcuni esempi:



# Architettura del SISTEMA SIES

Di seguito sono descritte le componenti tecniche che compongono il sistema SIES.


Figura 6 Componenti SIES
Come si evince dal diagramma, il nodo SIES è realizzato con architettura web three tier i cui principali elementi funzionali sono costituiti:
per la componente di interfaccia utente (presentation), da un web browser;
per la componente server di comunicazione e logica applicativa (application logic) da un web server con funzioni integrate di application server;
per la componente accesso a dati (data access) da un database relazionale.


In questo contesto si verifica quanto segue:
Un client attraverso un browser invia una richiesta HTTP al Web Server, in questo caso integrato con l’application server;
La richiesta HTTP è elaborata dal modulo funzionale opportunamente richiamato dall’application server;
Il modulo funzionale elabora la richiesta, eventualmente accedendo al database, e produce il codice HTML risultato dell’elaborazione;
L’application server mediante il modulo Web Server integrato restituisce il codice HTML al browser web;
Il browser web reindirizza il risultato.

Opzionalmente il processo può accodare messaggi sul server JMS che saranno elaborati in modo asincrono. Il server JMS persiste le informazioni relative ai messaggi sullo stesso database utilizzato dall’applicativo.

L’applicativo è realizzato con tecnologia Java Enterprise Edition; si tratta di una web application che non fa uso della tecnologia Enterprise Java Bean ed è fornita nel formato Web Archive (WAR).

I principali design pattern seguiti sono Model View Controller (MVC) e Data Access Object (DAO).

L'utilizzo del design pattern MVC rappresenta un aiuto per lo sviluppo delle applicazioni che sono divise in tre aree funzionali:
Modello: Il modello rappresenta la logica di business che, nella maggior parte dei casi, richiede l'accesso ad archivi dati quali i database relazionali.
Visualizzazione: La visualizzazione è il codice che presenta immagini e dati sulle pagine Web.
Controller: Il controller è il codice che determina il flusso globale di eventi.

Il pattern di programmazione DAO permette di disaccoppiare la logica di business dalla logica di persistenza dei dati: pertanto utilizzeremo il (Data Access Object). Attraverso l’uso del DAO Pattern la logica di business è indipendente dal sistema di memorizzazione adottato.

Per l’implemetazione del pattern MVC viene utilizzato il framework F3B : Framework Bull Building Blocks.

Per l’accesso ai dati sono utilizzate le API JDBC standard del linguaggio Java.






# Architettura SIUS AVVOCATURA

Il modulo SIES Avvocatura ha una architettura analoga a quella dei nodi SIES con l’unica peculiarità che l’accesso non avviene direttamente dal browser web, ma mediate l’interposizione del proxy PST.


Figura 7 Componenti SIUS Avvocatura


L’applicativo SIUS utilizza una architettura web three tier.

L’applicativo è realizzato con tecnologia Java Enterprise Edition; si tratta di una web application che non fa uso della tecnologia Enterprise Java Bean ed è fornita nel formato Web Archive (WAR).

I principali design pattern seguiti sono Model View Controller (MVC), Inversion Of Control (IOC), Façade e Data Access Object (DAO).

Come framework di sviluppo è stato utilizzato SpringFramework (http://projects.spring.io/spring-framework/) ed in particolare le componenti Core e MVC.
Per l’accesso ai dati è stato utilizzato iBatis ( https://ibatis.apache.org ).




# Generazione dei report con WindWard
La soluzione utilizzata prevede l’uso di librerie che lavorano come mostrato sinteticamente nella figura seguente:



Infatti, partendo da un template RTF contenente dei tag XSLPath ed un XML viene generato il documento finale pronto per la stampa.
Alleghiamo di seguito un esempio basato su un caso reale, riportando nell' ordine il template RTF, il file XML con i dati estratti, con query inclusa nel codice Java, ed il documento completo.





<=:/X/TipoUfficioT1>
<=:/X/TipoUfficioT2>
di <=:/X/Ufficio>
__________________________________________________

<=:/X/Ufficio>,<=:/X/Evento/DataEmissione>
N. SIEP <=:/X/FascicoloSiep/ChiaveProgr>/<=:/X/FascicoloSiep/ChiaveAnno>


Oggetto: Esecuzione penale contro

<=:/X/Soggetto/Cognome>/<=:/X/Soggetto/Nome>

<if:/X/Soggetto[Sesso='M']> nato <else:> nata <end:>a <=:/X/Soggetto/DescrComuneNascita > (Prov. <=:/X/Soggetto/CodProvinciaNascita >) il <if:/X/Soggetto/DataNascita> <=:/X/Soggetto/DataNascita><else:><=:/X/Soggetto/AnnoNascita><end:>
<while:/X/Soggetto/Alias>alias <=:./Cognome>/<=:./Nome>
<if:./.[Sesso='M']> nato <else:> nata <end:>a <=:./DescrComuneNascita > (Prov. <=:. /DescrProvinciaNascita >) il <if:./DataNascita> <=:./DataNascita><else:><=:./AnnoNascita><end:><end:>
<if:/X/Soggetto[Sesso='M']>Condannato <else:> Condannata <end:>con <=:/X/Sentenza/DescrTipoProvvedimento> N. <=:/X/Sentenza/NumeroSentenza>/<=:/X/Sentenza/AnnoSentenza> Reg. Gen. -<if:/X/Sentenza/NumeroRegePm> N. <=:/X/Sentenza/NumeroRegePm>/<=:/X/Sentenza/AnnoRegePm> Reg. Gen. Not.Reato,<end:> del <=:/X/Sentenza/DataProvvedimento> di <=:/X/Sentenza/DescrTipoAutoritaEmittente> <=:/X/Sentenza/DescrLuogoEmittente><if:/X/Sentenza/NumSezioneAutoritaEmittente> sez. <=:/X/Sentenza/NumSezioneAutoritaEmittente><end:>, <if:/X/Sentenza/DataProvvRif><=:/X/Sentenza/DescrTipoProvvRif> in data <=:/X/Sentenza/DataProvvRif><if:/X/Sentenza/CodTipoAutoritaProvvRif> da <=:/X/Sentenza/DescrTipoAutoritaProvvRif><if:/X/Sentenza/CodLuogoProvvRif> <=:/X/Sentenza/DescrLuogoProvvRif>,<end:><end:><if:/X/Sentenza[CodTipoProvvedimento = '01']> definitiva <end:><if:/X/Sentenza[CodTipoProvvedimento = '02']> definitivo <end:><end:>in data <=:/X/Sentenza/DataIrrevocabilita>


Alla Cancelleria della
<=:/X/Sentenza/DescrTipoAutoritaEmittente> <=:/X/Sentenza/DescrLuogoEmittente><if:/X/Sentenza/NumSezioneAutoritaEmittente>  sezione <=:/X/Sentenza/NumSezioneAutoritaEmittente> <end:>




Si comunica che in data <=:/X/FascicoloSiep/DataIscrizione> questo Ufficio ha iscritto il provvedimento in oggetto al N. <=:/X/FascicoloSiep/ChiaveProgr>/<=:/X/FascicoloSiep/ChiaveAnno> del Registro Esecuzioni Sentenze.

<?xml version="1.0" encoding="ISO-8859-1"?>
<X>
<TipoUfficio>PROCURA DELLA REPUBBLICA PRESSO IL TRIBUNALE ORDINARIO</TipoUfficio>
<Ufficio>VENEZIA</Ufficio>
<TipoUfficioT1>PROCURA DELLA REPUBBLICA </TipoUfficioT1>
<TipoUfficioT2>PRESSO IL TRIBUNALE ORDINARIO</TipoUfficioT2>
<Evento>
<CodTipoEvento>05</CodTipoEvento>
<DescrTipoEvento>RICHIESTA ISTRUTTORIA</DescrTipoEvento>
<CodTipoProvvedimento>-</CodTipoProvvedimento>
<DescrTipoProvvedimento>-</DescrTipoProvvedimento>
<CodMotivo>0047</CodMotivo>
<DescrMotivo>COMUNICAZIONE INIZIO ESECUZIONE</DescrMotivo>
<CodEsito>-</CodEsito>
<DescrEsito>-</DescrEsito>
<CodOperatoreInserimento>PMVE</CodOperatoreInserimento>
<DataInserimento>10-02-2004</DataInserimento>
<CodUfficioInserimento>02704202104</CodUfficioInserimento>
<FasSieIdFascicoloSiep>2004021</FasSieIdFascicoloSiep>
<IdEvento>20040228</IdEvento>
<CodUfficioEmittente>02704202104</CodUfficioEmittente>
<CodLuogoEmittente>027042</CodLuogoEmittente>
<DataEmissione>10-02-2004</DataEmissione>
<CodLuogoDestinatario>-</CodLuogoDestinatario>
<AnnoProtocollo>2004</AnnoProtocollo>
<ProgrProtocollo>2</ProgrProtocollo>
<FlagDocumentoRegistrato>N</FlagDocumentoRegistrato>
<CodTipoUfficioDestinatario>-</CodTipoUfficioDestinatario>
<DescrLuogoEmittente>VENEZIA</DescrLuogoEmittente>
<DescrUfficioEmittente>PROCURA DELLA REPUBBLICA PRESSO IL TRIBUNALE ORDINARIO</DescrUfficioEmittente>
<DescrLuogoDestinatario>-</DescrLuogoDestinatario>
<DescrTipoUfficioDestinatario>-</DescrTipoUfficioDestinatario>
<ExistBlob>false</ExistBlob>
<NumAllegati>0</NumAllegati>
<Notifica>
<CodEsito>-</CodEsito>
<DescrEsito>-</DescrEsito>
<CodOperatoreInserimento>PMVE</CodOperatoreInserimento>
<DataInserimento>10-02-2004</DataInserimento>
<CodUfficioInserimento>02704202104</CodUfficioInserimento>
<EveIdEvento>20040228</EveIdEvento>
<DescrUfficioInserimento/>
<DescrUfficioAggiornamento/>
<CodTipoNotifica>N</CodTipoNotifica>
<IdNotifica>20040260</IdNotifica>
<DataInvio>10-02-2004</DataInvio>
<DescrUfficioDestinatario/>
<DescrTipoNotifica>NOTIFICA</DescrTipoNotifica>
<Decrizione/>
<Ufficio>
<CodComune>027042</CodComune>
<CodUfficio>02704202104</CodUfficio>
<CodDistretto>02704200605</CodDistretto>
<CodProvincia>VE</CodProvincia>
<Cap>30125</Cap>
<CodTipoUfficio>PM</CodTipoUfficio>
<DateCarimentoRege>10-04-2003</DateCarimentoRege>
<CodUfficioCompetente/>
<Indirizzo>SAN POLO, 185</Indirizzo>
<Telefono>041 - 2402280</Telefono>
<Fax>041 - 2402281</Fax>
<EMail>PROCURA.VENEZIA@GIUSTIZIA.IT</EMail>
<DescrTipoUfficio>PROCURA DELLA REPUBBLICA PRESSO IL TRIBUNALE ORDINARIO</DescrTipoUfficio>
<DescProvincia>VENEZIA</DescProvincia>
<DescrComune>VENEZIA</DescrComune>
</Ufficio>
</Notifica>
</Evento>
<FascicoloSiep>
<Note>Primo procedimento DGSIA</Note>
<CodOperatoreInserimento>PMVE</CodOperatoreInserimento>
<DataInserimento>15-01-2004</DataInserimento>
<DescrTipoUfficio>PROCURA DELLA REPUBBLICA PRESSO IL TRIBUNALE ORDINARIO</DescrTipoUfficio>
<IdFascicoloSiep>2004021</IdFascicoloSiep>
<ChiaveAnno>2004</ChiaveAnno>
<ChiaveUfficio>02704202104</ChiaveUfficio>
<DescrComuneUfficio>VENEZIA</DescrComuneUfficio>
<ChiaveProgr>1</ChiaveProgr>
<CodStatoFascicolo>03</CodStatoFascicolo>
<DescrStatoFascicolo>VALIDATO</DescrStatoFascicolo>
<DataIscrizione>15-01-2004</DataIscrizione>
<CodMotivoArchiviazione>-</CodMotivoArchiviazione>
<DescrMotivoArchiviazione>-</DescrMotivoArchiviazione>
<CodTipoPosLibero>-</CodTipoPosLibero>
<DescrTipoPosLibero>-</DescrTipoPosLibero>
<FlagValidato>S</FlagValidato>
<CodUfficioInserimento>02704202104</CodUfficioInserimento>
<SogIdSoggetto>2004021</SogIdSoggetto>
<SenIdSentenza>2004021</SenIdSentenza>
<FlagAltraCausa>N</FlagAltraCausa>
</FascicoloSiep>
<Soggetto>
<Note>Primo utente Venezia in DGSIA</Note>
<Sesso>F</Sesso>
<Nazionalita>I</Nazionalita>
<Cognome>BARLOTTI</Cognome>
<Nome>FRANCESCO</Nome>
<CodOperatoreInserimento>PMVE</CodOperatoreInserimento>
<DataInserimento>15-01-2004</DataInserimento>
<CodUfficioInserimento>02704202104</CodUfficioInserimento>
<IdSoggetto>2004021</IdSoggetto>
<CodComuneNascita>093033</CodComuneNascita>
<Paternita>MARIO</Paternita>
<NomeMadre>MOIRA</NomeMadre>
<CognomeMadre>BELLEZZA</CognomeMadre>
<CodStatoNascita>039</CodStatoNascita>
<DataNascita>01-02-1980</DataNascita>
<AttoNascita>9988899988</AttoNascita>
<CodFiscale/>
<AnnoNascita>1980</AnnoNascita>
<DataNascitaPresunta>N</DataNascitaPresunta>
<CodProvinciaNascita>PN</CodProvinciaNascita>
<DescComuneNascitaEstero/>
<CodComuneCasellario>315</CodComuneCasellario>
<FlagPresenzaFascicolo>S</FlagPresenzaFascicolo>
<MeseNascita>2</MeseNascita>
<DescrComuneNascita>PORDENONE</DescrComuneNascita>
<DescrProvinciaNascita>PORDENONE</DescrProvinciaNascita>
<DescrStatoNascita>ITALIA</DescrStatoNascita>
<DescrNazionalita>ITALIANA</DescrNazionalita>
<DescrComuneCasellario>PORDENONE</DescrComuneCasellario>
<DescrUfficioInserimento/>
<DescrUfficioAggiornamento/>
</Soggetto>
<Sentenza>
<CodTipoProvvedimento>01</CodTipoProvvedimento>
<DescrTipoProvvedimento>SENTENZA</DescrTipoProvvedimento>
<CodOperatoreInserimento>PMVE</CodOperatoreInserimento>
<DataInserimento>15-01-2004</DataInserimento>
<CodUfficioInserimento>02704202104</CodUfficioInserimento>
<CodLuogoEmittente>001272</CodLuogoEmittente>
<IdSentenza>2004021</IdSentenza>
<AnnoRegePm>2003</AnnoRegePm>
<NumeroRegePm>998</NumeroRegePm>
<DataArrivoAtto>01-07-2002</DataArrivoAtto>
<DataProvvedimento>02-02-2002</DataProvvedimento>
<CodTipoAutoritaEmittente>PM</CodTipoAutoritaEmittente>
<DescrTipoAutoritaEmittente>PROCURA DELLA REPUBBLICA PRESSO IL TRIBUNALE ORDINARIO</DescrTipoAutoritaEmittente>
<DescrLuogoEmittente>TORINO</DescrLuogoEmittente>
<AnnoSentenza>2003</AnnoSentenza>
<NumeroSentenza>764</NumeroSentenza>
<DataIrrevocabilita>11-03-2002</DataIrrevocabilita>
<FlagSentenzaApplicazPena>N</FlagSentenzaApplicazPena>
<CodTipoProvvRif>-</CodTipoProvvRif>
<DescrTipoProvvRif>-</DescrTipoProvvRif>
<CodTipoAutoritaProvvRif>-</CodTipoAutoritaProvvRif>
<DescrTipoAutoritaProvvRif>-</DescrTipoAutoritaProvvRif>
<CodLuogoProvvRif>-</CodLuogoProvvRif>
<DescrLuogoProvvRif>-</DescrLuogoProvvRif>
<CodTipoDecisioneCassazione>-</CodTipoDecisioneCassazione>
<DescrTipoDecisioneCassazione>-</DescrTipoDecisioneCassazione>
<CodBilanciamentoCircostanze>-</CodBilanciamentoCircostanze>
<DescrBilanciamentoCircostanze>-</DescrBilanciamentoCircostanze>
<FlagGiudizioAbbreviato>N</FlagGiudizioAbbreviato>
</Sentenza>
</X>

PROCURA DELLA REPUBBLICA
PRESSO IL TRIBUNALE ORDINARIO
di VENEZIA
__________________________________________________

VENEZIA,10-02-2014
N. SIEP 1/2014


Oggetto: Esecuzione penale contro

Cognome/Nome
nata a Comune (Prov. PN) il  01-01-1900

Condannata con SENTENZA N. 764/2013 Reg. Gen. - N. 998/2003 Reg. Gen. Not.Reato, del 02-02-2012 di PROCURA DELLA REPUBBLICA PRESSO IL TRIBUNALE ORDINARIO TORINO, in data 11-03-2012



Alla Cancelleria della
PROCURA DELLA REPUBBLICA PRESSO IL TRIBUNALE ORDINARIO TORINO




Si comunica che in data 15-01-2014 questo Ufficio ha iscritto il provvedimento in oggetto al N. 1/2014 del Registro Esecuzioni Sentenze.

# Software di base (Stack)
Lo stack software su cui è realizzato il sistema SIES è il seguente:

Sistema Operativo: Red Hat Enterprise Linux 6.4 a 64bit
Java Virtual Machine: Oracle JVM 1.8
Application server: Red Hat Enterprise Application Platform 6.4
Server JMS (solo per Sies): Open MQ 5.1
Web Server (solo per Sies Avvocatura): Apache 2
Oracle 12.1.0.2


# Librerie utilizzate
Di seguito l’elenco delle librerie utilizzate e la rispettiva versione.
Per “siesEsecuzione”:
librerie native del server Jboss Enterprise Application Platform 6.1+ Runtime;
librerie native del sistema JRE (jdk1.8.0_45);
Maven Dependancies:
json-20090211.jar;
commons-lang-2.6.jar;
mybatis-3.0.5.jar
servlet-api-2.5.jar;
jsp-api-2.1.jar;
standard-1.1.2.jar;
jstl-1.2.jar;
junit-3.8.1.jar;
commons-fileupload-1.2.2.jar;
log4j-1.2.16.jar.
Per “SiesWeb”:
ojdbc6.jar;
librerie native del server Jboss Enterprise Application Platform 6.1+ Runtime;
librerie native del sistema JRE (jdk1.8.0_45);
axis.jar
bcmail-jdk16-140.jar
bcprov-jdk16-142.jar
commons-beanutils.jar
commons-codec.jar
commons-discovery-0.2.jar
commons-fileupload-1.1.1.jar
commons-httpclient-2.0.2.jar
commons-io-1.3.2.jar
commons-logging.jar
commons-logging-api-1.0.3.jar
dom4j.jar
freemarker-2.3.13.jar
imq.jar
imqjmx.jar
iText.jar
iTextAsian.jar
iTextXML.jar.jar
jasper.jar
jasper-el.jar
jasper-jdt.jar
jaxen.jar
jaxp-api-1.4.2.jar
jaxp-ri-1.4.jar
jaxrpc.jar
jaxws-api-2.2.1.jar
jaxws-rt-2.1.4.jar
jcl-over-slf4j-1.7.21.jar
jcommon.jar
jfreechart.jar
jms.jar
joda-time-1.5.2.jar
json.jar
json_simple-1.1.jar
json-20090211.jar
jsr173_1.0_api_XMLBEANS.jar
log4j-over-slf4j-1.7.21.jar
logback-classic-1.1.7.jar
logback-core-1.1.7.jar
mail.jar
ognl-2.6.11.jar
opensaml-2.2.3
resolver_XMLBEANS.jar
saaj.jar
sies_ese.jar
sies_v2.jar
sippi.jar
slf4j-api-1.7.21.jar
tika-app-0.6.jar
tools-1.6.0.jar
WindwardReports.jar
wsdl4j.jar
xalan-2.4.1.jar
xbean_XMLBEANS.jar
xbean_xpath_XMLBEANS.jar
xercesImpl.jar
xml-apis-1.0.b2.jar
xmlbeans-qname_XMLBEANS.jar
xmlpublic_XMLBEANS.jar
xmlsec-1.4.2.jar
xmltooling-1.2.0.jar
xwork-2.1.2.jar
# WEB Service
Per quanto riguarda i web services abbiamo la seguente situazione.
Il sistema “Sies” espone il seguente web services realizzato con architettura “Apache Axis 1.4” e viene richiamato da NSC attraverso il modulo di interoperabilità:
“WSNscToSies” è il web service per l’iscrizione in Sies di un titolo esecutivo proveniente da NSC.
Il sistema “SiusAvvocatura” espone i seguenti web services tutti realizzati con architettura Apache Axis 1.4:

“dettaglio Procedimento” è il web service per la richiesta del dettaglio di un procedimento;
“dettaglioDeceto” è il web service per la richiesta del dettaglio di un decreto;
“dettaglio Sentenza” è il web service per la richiesta del dettaglio di una sentenza;
“dettaglioOrdinanza” è il web service per la richiesta del dettaglio di una ordinanza;
“dettaglioRinvioUdienza” è il web service per la richiesta del dettaglio di un rinvio udienza;
“elencoProcedimentiDelSoggetto” è il web service per la ricerca di tutti i procedimenti a carico di un soggetto;
“ricercaSoggettiConProcedimenti” è il web service per la ricerca di tutti i soggetti con procedimenti a carico;
“richistaStampa” è il web service per la stampa dei dati di un procedimento;
“ricercaAvvisi” è il web service per la ricerca degli avvisi per avvocato.

Il sistema “NSC” espone i seguenti web services tutti realizzati con architettura “JAX-WS RI 2.0” e sono richiamati da funzionalità presenti su SIES.

“iscriviProvvedimentoEsecuzione” è il web service che consente il trasferimento di un foglio complementare dal sottosistema “Sius” ad NSC;
“iscriviProvvedimentoProvvisorio” è il web service che consente l’iscrizione di un soggetto e di un provvedimento provvisorio da “Sius/Siep” ad NSC;
“RichiestaCertificatoService” è il web service che soddisfa la richiesta “Sius/Siep” di un certificato per un dato soggetto;
“trasferisciFoglioComplementare” è il web service che consente il trasferimento di un foglio complementare dal sottosistema “Siep” ad NSC.


# Start-Stop Application Server
Stop

Aprire una shell linux sul server SIES e loggarsi come utente root
Eseguire il comando: “cd /etc/init.d” e fermare il processo di gestione delle code tramite il comando: “./imq stop” . Per le verifiche si può far riferimento al file di log /var/mq/instances/imqbroker/log/log.txt.
Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”. Per le verifiche si può far riferimento al file di log /opt/jboss-eap-6.4/standalone/logconsole/console.log

Start

Aprire una shell linux sul server SIES e loggarsi come utente root
Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione dell’istruzione tramite il comando: “service jboss status”. Per le verifiche si può far riferimento al file di log /opt/jboss-eap-6.4/standalone/logconsole/console.log
Eseguire il comando: “cd /etc/init.d” e avviare il processo di gestione delle code tramite il comando: “./imq start”. Per le verifiche si può far riferimento al file di log /var/mq/instances/imqbroker/log/log.txt.