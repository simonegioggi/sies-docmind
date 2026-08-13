---
uniqueName: siut-sie-ar-1-3-20210129-architetturasies
displayName: "SIUT SIE AR 1 3 20210129 Architettura SIES"
category: "GENERAL"
tags: []
---

# SIUT-SIE-AR-1.3-20210129-Architettura_SIES

> **File originale:** `Docs_CMDBuild_SIES+SIUS_Avvocati/SIUT-SIE-AR-1.3-20210129-Architettura_SIES.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
SIES 
Architettura del sistema 
 
 
 
 
 
 
 
 
 
 
Versione 1.3 del 29/01/2021

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 2/24 
 
 
 
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
Informatica S.p.A&Sirfin-PA 
S.r.l. 
nell’ambito 
del 
contratto CIG 73479643B7 per lo “Sviluppo del sistema 
informativo unitario telematico, la manutenzione degli 
attuali sistemi dell’area penale del Ministero della 
Giustizia e servizi correlati. Lotto 1”.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 3/24 
Approvazioni 
 
Nominativo 
Funzione 
Elaborato da 
Domenico Nania 
Analista Funzionale Senior 
Verificato da 
Fabio Gattamorta 
Referente PMO e Qualità 
Approvato da 
Paolo Ceccanti 
Responsabile Unico Fornitura 
Data approvazione 
29/01/2021 
 
Livello di riservatezza 
L3 
 
Elenco versioni 
Versione 
Data  
Motivo 
Modifica 
1.0 
13/12/2016 
Prima Emissione 
 
1.1 
06/03/2017 
Revisione 
Descrizione WEB-Service 
1.2 
12/04/2017 
Revisione 
Aggiornamento descrizione WEB-service 
1.3 
29/01/2021 
Revisione 
Adeguamento al formato standard SIUT 
 
 
Lista di distribuzione 
Nominativo 
Organizzazione 
Ufficio 
Ruolo 
Ing. Giovanni Malesci 
Amministrazione 
 
Responsabile Unico Procedimento 
Dr.ssa Annamaria Palmieri 
Amministrazione 
 
Direttore Esecutivo Contratto 
Paolo Ceccanti 
RTI 
 
Responsabile Unico Fornitura 
Vito Bufi 
RTI 
 
Responsabile Manutenzione Sistemi attuali 
Fabio Mazzocchi 
RTI 
 
Responsabile Manutenzione Correttiva 
Andrea Salvaggio 
RTI 
 
Responsabile Progetto Sistema Unitario 
Antonio Iacobelli 
RTI 
 
Responsabile Supporto Specialistico 
Antonella Damiani 
RTI 
 
Responsabile Centro di Competenza 
Salvatore Piazza 
RTI 
 
Technical Manager 
Sergio Tamburrini 
RTI 
 
Organization Manager 
Alessandro Falleni 
RTI 
 
Referente Sicurezza 
Fabio Gattamorta 
RTI 
 
Referente PMO e Qualità 
Francesco Rosati 
RTI 
 
Referente Qualità e Sicurezza 
Andrea Castorino 
RTI 
 
Referente Applicativo Gestore Fascicolo Documentale 
Luigi Buglione 
RTI 
 
Referente Metrico

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 4/24 
INDICE DEI CONTENUTI 
1 
INTRODUZIONE ........................................................................................................................... 5 
1.1 
SCOPO DEL DOCUMENTO ......................................................................................................................5 
1.2 
RIFERIMENTI .......................................................................................................................................5 
1.3 
GLOSSARIO ........................................................................................................................................5 
1.3.1 
DEFINIZIONI ....................................................................................................................................5 
1.3.2 
ACRONIMI E ABBREVIAZIONI ...............................................................................................................5 
2 
INTRODUZIONE ........................................................................................................................... 6 
3 
DISEGNO GENERALE DEL SISTEMA .............................................................................................. 7 
3.1 
INTERCONNESSIONE TRA NODI SIES ...................................................................................................... 8 
3.2 
SIES-NSC ........................................................................................................................................ 8 
3.3 
PST VS SIUS AVVOCATURA ............................................................................................................. 9 
3.4 
SIUS AVVOCATURA VS SISTEMI SIES .............................................................................................. 10 
4 
ARCHITETTURA DEL SISTEMA SIES ............................................................................................ 12 
5 
ARCHITETTURA SIUS AVVOCATURA ........................................................................................... 14 
6 
GENERAZIONE DEI REPORT CON WINDWARD .............................................................................15 
7 
SOFTWARE DI BASE (STACK) ...................................................................................................... 20 
8 
LIBRERIE UTILIZZATE ................................................................................................................. 21 
9 
WEB SERVICE ..............................................................................................................................23 
10 
START-STOP APPLICATION SERVER ........................................................................................ 24

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 5/24 
1 Introduzione 
1.1 Scopo del documento 
 
Questo documento descrive l'architettura di sistema adottata per il progetto SIES. 
 
 
1.2 Riferimenti 
Riferimento 
Nome Documento 
Descrizione Documento 
RIF1. 
 
 
 
 
1.3 Glossario 
1.3.1 Definizioni 
Definizione 
Descrizione 
 
 
 
 
1.3.2 Acronimi e abbreviazioni 
Sigla 
Descrizione 
DB 
Data Base 
BDI 
Base Dati Integrata 
DAO 
Data Access Object 
HTTP 
HyperText Transfer Protocol 
HTTPS 
HyperText Transfer Protocol over Secure Socket Layer 
JMS 
Java Message Service 
MVC 
Model View Controller 
NSC 
Nuovo Sistema Casellario 
RUG 
Rete Unitaria del Ministero della Giustizia 
SIC 
Sistema Informativo Casellario giudiziale 
SIEP 
Sottosistema Informativo delle Esecuzioni Penali 
SIES 
Sistema Informativo dell'Esecuzione Penale e Sorveglianza 
SIUS 
Sottosistema Informativo Uffici Sorveglianza 
WS 
Web Service

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 6/24 
2 Introduzione 
Questo documento descrive l'architettura di sistema adottata per il progetto SIES. 
Di seguito saranno descritte: 
• 
Il disegno generale del sistema, in cui si evidenziano tutte le componenti di SIES e i sistemi con cui 
sussistono scambi informativi.  
• 
L’architettura di sistema con la descrizione della struttura delle parti che compongono l’installazione 
software completa includendo le responsabilità dei vari componenti e le interconnessioni e tecnologie 
utilizzate.  
• 
Il software di base utilizzato.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 7/24 
3 Disegno generale del sistema 
Si riporta di seguito il disegno delle principali componenti del sistema SIES ed i sistemi con cui SIES si interfaccia. 
 
NSC
TITOLI ESECUTIVI
RUG
Interconnessioni tra nodi 
SIES per scambio Titoli 
Esecutivi e per le ricerche. 
L’interconnessione avviene 
attraverso la RUG 
mediante lo scambio di 
messaggi JMS su protocollo 
HTTP
Interconnessioni dei nodi 
SIES con NSC per 
acquisizione Titoli Esecutivi
Interconnessione dei nodi 
SIES con la componente 
AVVOCATI
SIES (nodo 2)
BDI
SIGE
SIUS
SIEP
SIEPE
SIES (nodo 29)
BDI
SIGE
SIUS
SIEP
SIEPE
SIES (nodo 1)
BDI
SIGE
SIUS
SIEP
SIEPE
SIUS 
Avvocatura
PST
Servizi riservati
Procedimenti 
Penali-SIUS
Procedimenti 
Penali SIUS
Richieste HTTPS da porxy 
PST a SIUS Avvocatura
 
 
Figura 1 Schema generale del sistema SIES 
 
 
 
La figura riporta: 
• 
Nodi SIES distribuiti sul territorio; 
• 
NSC, il sistema centralizzato del Casellario; 
• 
PST, il sistema centralizzato del Portale dei Servizi Telematici (PST); 
• 
SIUS Avvocatura, il sistema centralizzato per la fruizione dei servizi destinati alla consultazione dei

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 8/24 
Procedimenti penali SIUS. 
 
Di seguito sono descritte le modalità di interconnessione tra i diversi componenti e i flussi informativi scambiati. 
 
3.1 Interconnessione tra nodi SIES 
I diversi nodi SIES sono interconnessi tra di loro mediante un sistema di messaging basato sullo standard Java 
Message Service (JMS). JMS è un insieme di API (Application Program Interface) capaci di fornire servizi di 
messaggistica; più precisamente si tratta di una serie d’interfacce che permettono di accedere e di utilizzare i 
servizi di un sistema di middleware orientato ai messaggi, utilizzando Java come linguaggio. 
In sostanza JMS fornisce un metodo standard tramite il quale le applicazioni possono creare, inviare e ricevere i 
messaggi in modalità asincrona. 
Ogni nodo ha il suo server JMS, non esistendo un unico server JMS centralizzato su cui pubblicare ed 
eventualmente sottoscriversi. La modalità di invio messaggi è point-to-point.  
Ogni server JMS è configurato per comunicare con gli altri server via protocollo HTTP. Al suo interno sono state 
configurate due code, una per i messaggi in partenza ed una per i messaggi in arrivo. Il server JMS assicura 
all’applicativo SIES ildelivery dei messaggi consegnati, per fare questo persiste i messaggi su una base dati 
dedicata. 
I dati scambiati tra i distretti sono memorizzati sulla tabella Messaggio il cui contenuto è descritto nel 
documento SIGI_PNL_ML_2017 03 06_1.1_Modello dei Dati_SIES.doc 
La figura seguente illustra quanto esposto. 
Scambio di messaggi JMS 
point-to-point su protocollo 
HTTP mediante la rete RUG
SIES (nodo n)
BDI
SIGE
SIUS
SIEP
SIEPE
DB 
JMS
Server JMS
SIGE
SIGE
Coda ingresso
Coda uscita
SIES (nodo m)
BDI
SIGE
SIUS
SIEP
SIEPE
DB 
JMS
Server JMS
SIGE
SIGE
Coda ingresso
Coda uscita
 
Figura 2 Interconnessione tramite JMS 
 
 
3.2 
SIES-NSC 
I flussi informativi che coinvolgono il sistema SIES e il sistema del Casellario sono diversi: 
1. Invio Titolo Esecutivo da SIEP verso NSC; 
2. Invio Fogli Complementari da SIEP/SIUS verso NSC; 
3. Invio Titolo Esecutivo da NSC verso SIEP;

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 9/24 
4. Richiesta Certificato del Casellario da SIEP-SIUS; 
5. Interconnessione WEB tra SIES ed NSC: ovvero da SIES si può aprire il modulo di interoperabilità per 
effettuare ricerche direttamente su NSC. L’utente SIES non necessita di autenticarsi nuovamente sul 
sistema NSC perché le sue credenziali viaggiano attraverso il protocollo SAML. 
 
I primi 4 flussi sono contenuti in un “pacchetto applicativo” proprio di SIES; il flusso 5 pur partendo da SIES apre 
un’interfaccia di NSC. 
Gli scambi avvengono mediante protocollo HTTPS su rete RUG. 
 
 
Invocazione di web 
services su HTTPS
NSC
Fogli Complement.
Rich. Certificato
Titolo Esecutivo
Ricerche
Web Services
Interoperabilità
Con SIES
SIES (nodo i)
BDI
SIGE
SIUS
SIEP
SIEPE
Interoperabilità 
Web 
Con SIES
 
 
Figura 3 Interconnessione/interoperabilità con NSC 
 
 
3.3 
PST vs SIUS AVVOCATURA 
Il Portale dei Servizi Telematici PST si occupa dell’autenticazione e dell’autorizzazione degli avvocati alla 
fruizione delle funzionalità del sistema SIUS Avvocatura. 
L’accesso alle funzionalità avviene mediante un meccanismo di reverse-proxy in modo tale che il sistema SIUS 
Avvocatura non sia mai esposto direttamente all’esterno della rete RUG. L’interconnessione del browser 
dell’utente finale avviene solo con il proxy di PST che si occupa di attivare la funzionalità di SIUS Avvocatura. La 
risposta di SIUS Avvocatura arriva al proxy che si occupa di ritornarla al browser dell’utente. Tutti gli scambi 
avvengono con protocollo HTTPS.  
Per il dettaglio della configurazione si rimanda al documento SIGI_PNL_PA_2016 11 30_2.0_SIES Release 
11_Piano Adeguamento Ambienti-Istruzioni.docx

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 10/24 
Connessione HTTPS 
sulla rete RUG
SIUS 
Avvocatura
Procedimenti 
Penali SIUS
PST – Portale Servizi Telematici
Servizi riservati
Link a
Procedimenti 
Penali-SIUS
Reverse 
Proxy di 
PST
 
Figura 4 Interconnessione PST con SIUS Avvocatura 
 
3.4 
SIUS AVVOCATURA vs SISTEMI SIES 
Il modulo SIUS Avvocatura eroga i servizi di ricerca agli utenti mediante la chiamata di web-service esposti dai 
nodi SIES. Le chiamate ai web-services sono sincrone e avvengono mediante protocollo HTTPS sulla rete RUG. Di 
seguito la schematica rappresentazione dell’interconnessione di SIUS Avvocatura con uno dei nodi SIES. 
Per il dettaglio della configurazione si rimanda al documento SIGI_PNL_PA_2016 11 30_2.0_Avvocatura-Piano 
Adeguamento Ambienti-Istruzioni.doc 
Per il dettaglio dei WebServices si rimanda al documento SIGI_PNL_WS_2016 11 30_2.0_Descrizione Servizi 
Web AVVOCATURA-SIUS.doc

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 11/24 
SIES (nodo i)
BDI
SIGE
SIUS
SIEP
SIEPE
SIUS 
Avvocatura
Procedimenti 
Penali SIUS
Web Services 
per 
Avvocatura
Invocazione da parte di 
SIES Avvocatura dei web 
service di un nodo SIES
Protocollo HTTPS su RUG
 
Figura 5 Interconnessione SIUS Avvocatura SIES

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 12/24 
4 Architettura del SISTEMA SIES 
 
Di seguito sono descritte le componenti tecniche che compongono il sistema SIES. 
 
Application Server SIES
Web Service
per interoperabilità 
e per Avvocatura
Moduli Funzionalità
Sistema 
SIES
Postazione utente
Web Browser
HTTP/HTTPS
Server JMS
Code messaggi
per interoberabilità
nodi 
SIES
JDBC
JMS
Base Dati SIES
RDBMS
JDBC
 
Figura 6 Componenti SIES 
Come si evince dal diagramma, il nodo SIES è realizzato con architettura web three tier i cui principali elementi 
funzionali sono costituiti: 
1. per la componente di interfaccia utente (presentation), da un web browser; 
2. per la componente server di comunicazione e logica applicativa (application logic) da un web server con 
funzioni integrate di application server; 
3. per la componente accesso a dati (data access) da un database relazionale. 
 
 
In questo contesto si verifica quanto segue: 
1. Un client attraverso un browser invia una richiesta HTTP al Web Server, in questo caso integrato con 
l’application server;

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 13/24 
2. La richiesta HTTP è elaborata dal modulo funzionale opportunamente richiamato dall’application server; 
3. Il modulo funzionale elabora la richiesta, eventualmente accedendo al database, e produce il codice 
HTML risultato dell’elaborazione; 
4. L’application server mediante il modulo Web Server integrato restituisce il codice HTML al browser web; 
5. Il browser web reindirizza il risultato. 
 
Opzionalmente il processo può accodare messaggi sul server JMS che saranno elaborati in modo asincrono. Il 
server JMS persiste le informazioni relative ai messaggi sullo stesso database utilizzato dall’applicativo. 
 
L’applicativo è realizzato con tecnologia Java Enterprise Edition; si tratta di una web application che non fa uso 
della tecnologia Enterprise Java Bean ed è fornita nel formato Web Archive (WAR). 
 
I principali design pattern seguiti sono Model View Controller (MVC) e Data Access Object (DAO). 
 
L'utilizzo del design pattern MVC rappresenta un aiuto per lo sviluppo delle applicazioni che sono divise in tre 
aree funzionali:  
• 
Modello: Il modello rappresenta la logica di business che, nella maggior parte dei casi, richiede l'accesso 
ad archivi dati quali i database relazionali.  
• 
Visualizzazione: La visualizzazione è il codice che presenta immagini e dati sulle pagine Web.  
• 
Controller: Il controller è il codice che determina il flusso globale di eventi.  
 
Il pattern di programmazione DAO permette di disaccoppiare la logica di business dalla logica di persistenza dei 
dati: pertanto utilizzeremo il (Data Access Object). Attraverso l’uso del DAO Pattern la logica di business è 
indipendente dal sistema di memorizzazione adottato. 
 
Per l’implemetazione del pattern MVC viene utilizzato il framework F3B : Framework Bull Building Blocks. 
 
Per l’accesso ai dati sono utilizzate le API JDBC standard del linguaggio Java.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 14/24 
5 Architettura SIUS AVVOCATURA 
 
Il modulo SIES Avvocatura ha una architettura analoga a quella dei nodi SIES con l’unica peculiarità che l’accesso 
non avviene direttamente dal browser web, ma mediate l’interposizione del proxy PST.  
 
Proxy PST
Configurazione
Per
SIUS
Avvocatura
Postazione utente
Web Browser
HTTPS
Application Server 
SIUS Avvocatura
Moduli 
Funzionalità
HTTPS
Base Dati SIES
RDBMS
JDBC
Client dei Web 
Services esposti dai 
nodi SIES
Web Server SIUS 
Avvocatura
Configurazione
Per
SIUS
Avvocatura
HTTPS/AJP
 
Figura 7 Componenti SIUS Avvocatura 
 
 
L’applicativo SIUS utilizza una architettura web three tier. 
 
L’applicativo è realizzato con tecnologia Java Enterprise Edition; si tratta di una web application che non fa uso 
della tecnologia Enterprise Java Bean ed è fornita nel formato Web Archive (WAR). 
 
I principali design pattern seguiti sono Model View Controller (MVC), Inversion Of Control (IOC), Façade e Data 
Access Object (DAO). 
 
Come framework di sviluppo è stato utilizzato SpringFramework (http://projects.spring.io/spring-framework/) 
ed in particolare le componenti Core e MVC.  
Per l’accesso ai dati è stato utilizzato iBatis ( https://ibatis.apache.org ).

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 15/24 
6 Generazione dei report con WindWard 
La soluzione utilizzata prevede l’uso di librerie che lavorano come mostrato sinteticamente nella figura 
seguente: 
 
 
 
Infatti, partendo da un template RTF contenente dei tag XSLPath ed un XML viene generato il documento finale 
pronto per la stampa. 
Alleghiamo di seguito un esempio basato su un caso reale, riportando nell' ordine il template RTF, il file XML con 
i dati estratti, con query inclusa nel codice Java, ed il documento completo. 
 
 
 
 
 
<=:/X/TipoUfficioT1> 
<=:/X/TipoUfficioT2> 
di <=:/X/Ufficio> 
__________________________________________________ 
 
<=:/X/Ufficio>,<=:/X/Evento/DataEmissione>  
N. SIEP <=:/X/FascicoloSiep/ChiaveProgr>/<=:/X/FascicoloSiep/ChiaveAnno> 
 
 
PROCURA DELLA REPUBBLICA
Il Signor <=:/Doc/Soggetto/Nome>
<=:/Doc/Soggetto/Cognome>
<if:/sex=‘M’>Nato<else>Nata<end:>
a <=:/Doc/Soggetto/Luogo>
il <=:/Doc/Soggetto/Data>
Ha commesso i seguenti reati
<while:/Doc/Soggetto/Reato>
<=:./Desc>
<end:>
<Doc>
<Soggetto>
<Nome>Arturo</Nome>
<Cognome>Rossi</ Cognome >
<Sesso>M</Sesso>
<Luogo>TARANTO</Luogo>
<Data>01/01/1950 </Data> 
<Reato>
<Desc>Furto</Desc>
</Reato>
<Reato>
<Desc>Rapina </Desc>
</Reato>
<Reato>
<Desc>Scippo </Desc>
</Reato>
</Soggetto>
</Doc>
XML
Il signor Arturo Rossi
Nato a TARANTO il 01/01/1950
Ha commesso i seguenti reati:
Furto
Rapina
Scippo
WindWard 
Process
PROCURA DELLA REPUBBLICA
Documento
Finale

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 16/24 
Oggetto: Esecuzione penale contro 
 
<=:/X/Soggetto/Cognome>/<=:/X/Soggetto/Nome> 
 
<if:/X/Soggetto[Sesso='M']> nato <else:> nata <end:>a <=:/X/Soggetto/DescrComuneNascita > (Prov. 
<=:/X/Soggetto/CodProvinciaNascita >) il <if:/X/Soggetto/DataNascita> 
<=:/X/Soggetto/DataNascita><else:><=:/X/Soggetto/AnnoNascita><end:> 
<while:/X/Soggetto/Alias>alias <=:./Cognome>/<=:./Nome> 
<if:./.[Sesso='M']> nato <else:> nata <end:>a <=:./DescrComuneNascita > (Prov. <=:. /DescrProvinciaNascita >) il 
<if:./DataNascita> <=:./DataNascita><else:><=:./AnnoNascita><end:><end:> 
<if:/X/Soggetto[Sesso='M']>Condannato <else:> Condannata <end:>con 
<=:/X/Sentenza/DescrTipoProvvedimento> N. 
<=:/X/Sentenza/NumeroSentenza>/<=:/X/Sentenza/AnnoSentenza> Reg. Gen. -
<if:/X/Sentenza/NumeroRegePm> N. <=:/X/Sentenza/NumeroRegePm>/<=:/X/Sentenza/AnnoRegePm> Reg. 
Gen. Not.Reato,<end:> del <=:/X/Sentenza/DataProvvedimento> di 
<=:/X/Sentenza/DescrTipoAutoritaEmittente> 
<=:/X/Sentenza/DescrLuogoEmittente><if:/X/Sentenza/NumSezioneAutoritaEmittente> sez. 
<=:/X/Sentenza/NumSezioneAutoritaEmittente><end:>, 
<if:/X/Sentenza/DataProvvRif><=:/X/Sentenza/DescrTipoProvvRif> in data 
<=:/X/Sentenza/DataProvvRif><if:/X/Sentenza/CodTipoAutoritaProvvRif> da 
<=:/X/Sentenza/DescrTipoAutoritaProvvRif><if:/X/Sentenza/CodLuogoProvvRif> 
<=:/X/Sentenza/DescrLuogoProvvRif>,<end:><end:><if:/X/Sentenza[CodTipoProvvedimento = '01']> definitiva 
<end:><if:/X/Sentenza[CodTipoProvvedimento = '02']> definitivo <end:><end:>in data 
<=:/X/Sentenza/DataIrrevocabilita>  
 
 
Alla Cancelleria della 
<=:/X/Sentenza/DescrTipoAutoritaEmittente> 
<=:/X/Sentenza/DescrLuogoEmittente><if:/X/Sentenza/NumSezioneAutoritaEmittente>  sezione 
<=:/X/Sentenza/NumSezioneAutoritaEmittente> <end:> 
 
 
 
 
Si comunica che in data <=:/X/FascicoloSiep/DataIscrizione> questo Ufficio ha iscritto il provvedimento in 
oggetto al N. <=:/X/FascicoloSiep/ChiaveProgr>/<=:/X/FascicoloSiep/ChiaveAnno> del Registro Esecuzioni 
Sentenze. 
 
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 17/24 
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 18/24 
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 19/24 
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
 
 Condannata con SENTENZA N. 764/2013 Reg. Gen. - N. 998/2003 Reg. Gen. Not.Reato, del 02-02-2012 di 
PROCURA DELLA REPUBBLICA PRESSO IL TRIBUNALE ORDINARIO TORINO, in data 11-03-2012  
 
 
 
Alla Cancelleria della 
PROCURA DELLA REPUBBLICA PRESSO IL TRIBUNALE ORDINARIO TORINO 
 
 
 
 
Si comunica che in data 15-01-2014 questo Ufficio ha iscritto il provvedimento in oggetto al N. 1/2014 del 
Registro Esecuzioni Sentenze.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 20/24 
7 Software di base (Stack) 
Lo stack software su cui è realizzato il sistema SIES è il seguente: 
 
• 
Sistema Operativo: Red Hat Enterprise Linux 6.4 a 64bit 
• 
Java Virtual Machine: Oracle JVM 1.8 
• 
Application server: Red Hat Enterprise Application Platform 6.4 
• 
Server JMS (solo per Sies): Open MQ 5.1 
• 
Web Server (solo per Sies Avvocatura): Apache 2 
• 
Oracle 12.1.0.2

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 21/24 
8 Librerie utilizzate 
Di seguito l’elenco delle librerie utilizzate e la rispettiva versione. 
Per “siesEsecuzione”:   
• librerie native del server Jboss Enterprise Application Platform 6.1+ Runtime; 
• librerie native del sistema JRE (jdk1.8.0_45); 
• Maven Dependancies: 
o json-20090211.jar; 
o commons-lang-2.6.jar; 
o mybatis-3.0.5.jar 
o servlet-api-2.5.jar; 
o jsp-api-2.1.jar; 
o standard-1.1.2.jar; 
o jstl-1.2.jar; 
o junit-3.8.1.jar; 
o commons-fileupload-1.2.2.jar; 
o log4j-1.2.16.jar. 
Per “SiesWeb”: 
• ojdbc6.jar; 
• librerie native del server Jboss Enterprise Application Platform 6.1+ Runtime; 
• librerie native del sistema JRE (jdk1.8.0_45); 
• axis.jar 
• bcmail-jdk16-140.jar 
• bcprov-jdk16-142.jar 
• commons-beanutils.jar 
• commons-codec.jar 
• commons-discovery-0.2.jar 
• commons-fileupload-1.1.1.jar 
• commons-httpclient-2.0.2.jar 
• commons-io-1.3.2.jar 
• commons-logging.jar 
• commons-logging-api-1.0.3.jar 
• dom4j.jar 
• freemarker-2.3.13.jar 
• imq.jar 
• imqjmx.jar 
• iText.jar 
• iTextAsian.jar 
• iTextXML.jar.jar 
• jasper.jar 
• jasper-el.jar

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 22/24 
• jasper-jdt.jar 
• jaxen.jar 
• jaxp-api-1.4.2.jar 
• jaxp-ri-1.4.jar 
• jaxrpc.jar 
• jaxws-api-2.2.1.jar 
• jaxws-rt-2.1.4.jar 
• jcl-over-slf4j-1.7.21.jar 
• jcommon.jar 
• jfreechart.jar 
• jms.jar 
• joda-time-1.5.2.jar 
• json.jar 
• json_simple-1.1.jar 
• json-20090211.jar 
• jsr173_1.0_api_XMLBEANS.jar 
• log4j-over-slf4j-1.7.21.jar 
• logback-classic-1.1.7.jar 
• logback-core-1.1.7.jar 
• mail.jar 
• ognl-2.6.11.jar 
• opensaml-2.2.3 
• resolver_XMLBEANS.jar 
• saaj.jar 
• sies_ese.jar 
• sies_v2.jar 
• sippi.jar 
• slf4j-api-1.7.21.jar 
• tika-app-0.6.jar 
• tools-1.6.0.jar 
• WindwardReports.jar 
• wsdl4j.jar 
• xalan-2.4.1.jar 
• xbean_XMLBEANS.jar 
• xbean_xpath_XMLBEANS.jar 
• xercesImpl.jar 
• xml-apis-1.0.b2.jar 
• xmlbeans-qname_XMLBEANS.jar 
• xmlpublic_XMLBEANS.jar 
• xmlsec-1.4.2.jar 
• xmltooling-1.2.0.jar 
• xwork-2.1.2.jar

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 23/24 
9 WEB Service 
Per quanto riguarda i web services abbiamo la seguente situazione. 
Il sistema “Sies” espone il seguente web services realizzato con architettura “Apache Axis 1.4” e viene 
richiamato da NSC attraverso il modulo di interoperabilità: 
• “WSNscToSies” è il web service per l’iscrizione in Sies di un titolo esecutivo proveniente da NSC. 
Il sistema “SiusAvvocatura” espone i seguenti web services tutti realizzati con architettura Apache Axis 
1.4: 
 
• “dettaglio Procedimento” è il web service per la richiesta del dettaglio di un procedimento; 
• “dettaglioDeceto” è il web service per la richiesta del dettaglio di un decreto; 
• “dettaglio Sentenza” è il web service per la richiesta del dettaglio di una sentenza; 
• “dettaglioOrdinanza” è il web service per la richiesta del dettaglio di una ordinanza; 
• “dettaglioRinvioUdienza” è il web service per la richiesta del dettaglio di un rinvio udienza; 
• “elencoProcedimentiDelSoggetto” è il web service per la ricerca di tutti i procedimenti a carico 
di un soggetto; 
• “ricercaSoggettiConProcedimenti” è il web service per la ricerca di tutti i soggetti con 
procedimenti a carico; 
• “richistaStampa” è il web service per la stampa dei dati di un procedimento; 
• “ricercaAvvisi” è il web service per la ricerca degli avvisi per avvocato. 
 
Il sistema “NSC” espone i seguenti web services tutti realizzati con architettura “JAX-WS RI 2.0” e sono 
richiamati da funzionalità presenti su SIES. 
 
• “iscriviProvvedimentoEsecuzione” è il web service che consente il trasferimento di un foglio 
complementare dal sottosistema “Sius” ad NSC; 
• “iscriviProvvedimentoProvvisorio” è il web service che consente l’iscrizione di un soggetto e di 
un provvedimento provvisorio da “Sius/Siep” ad NSC; 
• “RichiestaCertificatoService” è il web service che soddisfa la richiesta “Sius/Siep” di un 
certificato per un dato soggetto; 
• “trasferisciFoglioComplementare” è il web service che consente il trasferimento di un foglio 
complementare dal sottosistema “Siep” ad NSC.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-AR-20210129-1.3 Architettura SIES 
Ver. 1.3 del 29/01/2021 
Pag. 24/24 
10 Start-Stop Application Server 
Stop 
 
1. Aprire una shell linux sul server SIES e loggarsi come utente root 
2. Eseguire il comando: “cd /etc/init.d” e fermare il processo di gestione delle code tramite il 
comando: “./imq stop” . Per le verifiche si può far riferimento al file di log 
/var/mq/instances/imqbroker/log/log.txt. 
3. Fermare il server jboss tramite il comando: “service jboss stop” e controllare l’avvenuta esecuzione 
dell’istruzione tramite il comando: “service jboss status”. Per le verifiche si può far riferimento al file 
di log /opt/jboss-eap-6.4/standalone/logconsole/console.log 
 
Start 
 
1. Aprire una shell linux sul server SIES e loggarsi come utente root 
2. Avviare il server jboss tramite il comando “service jboss start” e controllare l’avvenuta esecuzione 
dell’istruzione tramite il comando: “service jboss status”. Per le verifiche si può far riferimento al file 
di log /opt/jboss-eap-6.4/standalone/logconsole/console.log 
3. Eseguire il comando: “cd /etc/init.d” e avviare il processo di gestione delle code tramite il comando: 
“./imq 
start”. 
Per 
le 
verifiche 
si 
può 
far 
riferimento 
al 
file 
di 
log 
/var/mq/instances/imqbroker/log/log.txt.