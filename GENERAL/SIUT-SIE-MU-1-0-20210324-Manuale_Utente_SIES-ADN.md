---
uniqueName: siut-sie-mu-1-0-20210324-manualeutentesies-adn
displayName: "SIUT SIE MU 1 0 20210324 Manuale Utente SIES ADN"
category: "GENERAL"
tags: []
---

# SIUT-SIE-MU-1.0-20210324-Manuale_Utente_SIES-ADN

> **File originale:** `MEV/Integrazione SIES-ADN/RILASCIO_MEV_SIES-ADN (PRE GO-LIVE)/20210324_1.0/SIUT-SIE-MU-1.0-20210324-Manuale_Utente_SIES-ADN.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
MEV Integrazione SIES-ADN 
 
 
Manuale Utente 
 
 
 
 
 
 
 
 
 
Versione 1.0 del 24/03/2021

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-MU-1.0-20210324-Manuale_Utente_SIES-ADN 
Ver. 1.0 del 24/03/2021 
Pag. 2/12 
 
 
 
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
Informativo Unitario Telematico, la manutenzione degli 
attuali sistemi dell’area Penale del Ministero della 
Giustizia e servizi correlati. Lotto 1”.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-MU-1.0-20210324-Manuale_Utente_SIES-ADN 
Ver. 1.0 del 24/03/2021 
Pag. 3/12 
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
24/03/2021 
 
Livello di riservatezza 
L3 
 
 
Elenco versioni 
Versione 
Data  
Motivo 
Modifica 
1.0 
24/03/2021 
Prima emissione 
 
 
 
Lista di distribuzione 
Nominativo 
Organizzazione 
Ufficio 
Funzione 
Ing. Giovanni Malesci 
Amministrazione 
 
Responsabile Unico Procedimento 
Dr.ssa Annamaria Palmieri 
Amministrazione 
 
Direttore Esecutivo Contratto 
Paolo Ceccanti 
RTI 
 
Responsabile Unico Fornitura 
Salvatore Piazza 
RTI 
 
Technical Manager 
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
 
Referente Applicativo Gestore Fascicolo Documentale
Luigi Buglione 
RTI 
 
Referente Metrico

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-MU-1.0-20210324-Manuale_Utente_SIES-ADN 
Ver. 1.0 del 24/03/2021 
Pag. 4/12 
INDICE DEI CONTENUTI 
1. 
INTRODUZIONE ......................................................................................................................... 5 
1.1. SCOPO DEL DOCUMENTO ........................................................................................................................ 5 
1.2. GLOSSARIO .......................................................................................................................................... 5 
1.2.1. 
DEFINIZIONI ...................................................................................................................................... 5 
1.2.2. 
ACRONIMI E ABBREVIAZIONI ................................................................................................................. 6 
2. 
LOGIN SIES ................................................................................................................................ 7 
2.1. SCOPO DELL’APPLICATIVO ....................................................................................................................... 7 
2.2. TIPOLOGIE DI UTENTI ............................................................................................................................. 7 
3. 
ACCESSO SISTEMA SIES .............................................................................................................. 8 
3.1. LOGIN ................................................................................................................................................. 8

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-MU-1.0-20210324-Manuale_Utente_SIES-ADN 
Ver. 1.0 del 24/03/2021 
Pag. 5/12 
1. Introduzione 
1.1. Scopo del documento 
Per garantire la continuità dei servizi di interconnessione ad oggi presenti tra il sistema SIES e SIC, si è 
reso necessario intervenire sugli attuali meccanismi di scambio ‘dati’ tra i due sistemi.  
L’intervento ha interessato l’allineamento dei vari ‘colloqui’ infrastrutturali relativamente a nuove 
dinamiche di autenticazione e profilazione.  
 
I processi di interconnessione presenti tra SIES e SIC sono:  
• Invio titoli esecutivi da SIES verso il SIC;  
• Invio dei fogli complementari da SIES verso il SIC;  
• Invio provvedimento di cumulo da SIES verso il SIC;  
• Recupero di provvedimenti principali dal SIC sul SIES;  
• Richiesta del certificato Penale;  
• Accesso al modulo WEB di interconnessione SIES-NSC. 
 
Nell’ottica di predisporre il sistema SIES all’integrazione con l’autenticazione basata sulle utenze di ADN 
di Giustizia, e di garantire continuità delle interconnessioni ad oggi in essere verso il SIC, si è intervenuti 
sulla pagina di accesso al SIES in modo da ‘iniziare’ ad alimentare ed arricchire la banca dati con le 
associazioni dell’utenza ADN rispetto all’ufficio o gli ‘n’ uffici con cui l’utente è profilato attualmente sul 
SIES rispetto anche ai sottosistemi SIEP, SIUS e SIGE. 
 
 
1.2. Glossario 
1.2.1. Definizioni 
Si premette un glossario esplicativo delle abbreviazioni e dei termini tecnici e giuridici utilizzati nel 
documento (Tabella - Glossario dei termini e degli acronimi usati nel documento). 
 
Definizione 
Descrizione 
Fascicolo penale 
Insieme degli atti cartacei relativi ad un procedimento penale 
Portal Liferay 
Liferay è un entreprise portal free e open Source 
PDF 
Portable Document Format – Standard per scambio documenti elettronici 
P7M 
Estensione file firmato con modalità CAdES, ovvero il documento firmato ed il file con la 
firma digitale vengono inseriti insieme in una busta. 
PDF Firmato 
Firma digitale apposta con modalità PAdES in cui vengono sfruttate le caratteristiche dei 
documenti in formato pdf. Il file contenente la firma digitale viene inglobato insieme al 
documento stesso. 
Web-based  
Un programma in cui tutte le funzioni sono accessibili tramite un normale web-browser come 
Firefox, Chrome o Explorer. Questo significa che non è necessario effettuare l’installazione di 
alcun software sui computer dell’azienda che deve utilizzare il programma.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-MU-1.0-20210324-Manuale_Utente_SIES-ADN 
Ver. 1.0 del 24/03/2021 
Pag. 6/12 
1.2.2. Acronimi e abbreviazioni 
Sigla 
Descrizione 
GSU 
Gestione Servizi UNEP 
PDOC 
Sistema Piattaforma Documentale 
PEC 
Posta Elettronica Certificata 
PST 
Portale dei Servizi Telematici 
REGE 
Registro Generale delle Notizie di Reato 
RG 
Registro Generale 
SNT 
Sistema Notifiche Telematiche 
UNEP 
Ufficio Notificazioni Esecuzioni Protesti 
XML 
eXtensible Markup Language

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-MU-1.0-20210324-Manuale_Utente_SIES-ADN 
Ver. 1.0 del 24/03/2021 
Pag. 7/12 
2. Login SIES 
2.1. Scopo dell’applicativo 
Con lo scopo di uniformare il comportamento delle applicazioni all’utilizzo dell’utenza ADN si è 
intervenuti sull’attuale gestione del login sul sistema SIES.  
In particolare, per l’applicazione del SIES, si è integrata la maschera di accesso con un’ulteriore sezione 
per permettere all’utente di inserire le credenziali ADN.  
A seguito dell’inserimento e verifica delle stesse, l’applicativo ‘registrerà’, in apposite tabelle associative 
la correlazione dell’utenza SIES con l’utenza ADN.  
2.2. Tipologie di utenti 
L’applicativo prevede due tipologie di utenti: Amministratore di sistema, utenti degli uffici giudiziari dei 
vari distretti. La prima è una tipologia di utente dedicata alla gestione e configurazione dell’applicativo, 
la seconda rappresenta il ruolo che fruisce delle funzionalità applicative del sistema.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-MU-1.0-20210324-Manuale_Utente_SIES-ADN 
Ver. 1.0 del 24/03/2021 
Pag. 8/12 
3. ACCESSO SISTEMA SIES 
3.1. Login 
La maschera di Login consente all’utente di autenticarsi per accedere alle funzionalità fornite 
dall’applicativo SIES.  
L’utente si trova sulla pagina di Login del SIES. Il sistema propone la pagina di accesso in cui l’utente sarà 
tenuto ad inserire le proprie credenziali ADN, in deroga a quanto attualmente previsto dal sistema SIES 
che chiede l’inserimento delle credenziali SIES.  
In realtà questo ‘nuovo’ modo di lavorare anticipa, in qualche modo, ciò che a tendere avverrà per 
l’accesso unico ai sistemi penali, dove appunto è prevista un’autenticazione basata sulle credenziali ADN 
Nazionale. 
 
 
 
 
Figura 1 - Login 
 
 
 
A seguito dell’azione di ‘submit’ delle credenziali, il sistema effettua un controllo sulla ‘autenticità’ delle 
informazioni inserite effettuando una chiamata LDAP sul server ADN di Giustizia. 
Per dati esatti, il sistema ridirige l’utente sulla stessa pagina, mostrando una funzione di gestione 
profilazione delle utenze SIES, così come riportato nell’immagine che segue, mentre per dati non 
corrispondenti, sarà visualizzato apposito messaggio di errore.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-MU-1.0-20210324-Manuale_Utente_SIES-ADN 
Ver. 1.0 del 24/03/2021 
Pag. 9/12 
Figura 2 - Pagina di selezione Account SIES 
 
 
 
Dalla form prospettata, con la selezione della procedura di ‘Seleziona/Configura un Account’, all’utente 
sarà mostrata la pagina per l’inserimento delle credenziali del SIES: 
 
 
 
Figura 3 - Pagina per inserimento credenziali SIES

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-MU-1.0-20210324-Manuale_Utente_SIES-ADN 
Ver. 1.0 del 24/03/2021 
Pag. 10/12 
A seguito dell’inserimento delle credenziali del SIES, il sistema effettuerà dei controlli per verificare 
l’autenticità delle stesse credenziali. Successivamente mostrerà un messaggio di avvenuta associazione 
utenza SIES: 
 
Figura 4 – Messaggio di avvenuta associazione utenza SIES 
 
A questo punto l’utente dopo aver cliccato sul pulsante OK presente nel messaggio vedrà la sua Utenza SIES con 
la descrizione dell’ufficio a cui appartiene ed il pulsante ‘Entra’: 
 
 
Figura 5 – Pagina con utenze SIES associate 
 
selezionando il tasto ‘Entra’ sarà ridiretto nella welcome page dell’applicazione del SIES:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-MU-1.0-20210324-Manuale_Utente_SIES-ADN 
Ver. 1.0 del 24/03/2021 
Pag. 11/12 
 
 
 
Figura 6 – Welcome page SIES 
 
 
 
Proseguendo invece con la funzione di ‘Seleziona/Configura un account’, il sistema mostrerà nuovamente la 
form di inserimento utenza e password SIES come in Figura 3. 
 
Configurando ogni account, l’utente completerebbe, sotto la propria responsabilità, la procedura di match tra la 
propria utenza ADN con le multiutenze del SIES.  
 
Al successivo accesso, se l’utente ha eseguito delle associazioni, si ritroverà, già configurate, le utenze che utilizza 
solitamente per l’accesso al SIES. 
 
Si riporta a seguire un esempio di pagina:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 SIUT-SIE-MU-1.0-20210324-Manuale_Utente_SIES-ADN 
Ver. 1.0 del 24/03/2021 
Pag. 12/12 
Figura 7 – Pagina di scelta utenza 
 
 
 
L’utente, pertanto, può selezionare l’utenza di interesse, cliccare sul pulsante ‘Entra’ ed iniziare la navigazione 
nel SIES, oppure configurare ed entrare con un account diverso.