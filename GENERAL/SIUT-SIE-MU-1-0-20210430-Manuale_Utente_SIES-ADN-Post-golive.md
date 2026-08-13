---
uniqueName: siut-sie-mu-1-0-20210430-manualeutentesies-adn-pos
displayName: "SIUT SIE MU 1 0 20210430 Manuale Utente SIES ADN Post golive"
category: "GENERAL"
tags: []
---

# SIUT-SIE-MU-1.0-20210430-Manuale_Utente_SIES-ADN-Post-golive

> **File originale:** `MEV/Integrazione SIES-ADN/RILASCIO_MEV_SIES-ADN (POST GO-LIVE)/20210430_1.0/SIUT-SIE-MU-1.0-20210430-Manuale_Utente_SIES-ADN-Post-golive.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
Integrazione SIES-ADN-Post-golive 
 
 
Manuale Utente 
 
 
 
 
 
 
 
 
 
Versione 1.0 del 30/04/2021

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-MU-1.0-20210430-Manuale_Utente_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
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
Informativo Unitario Telematico, la manutenzione degli 
attuali sistemi dell’area Penale del Ministero della 
Giustizia e servizi correlati. Lotto 1”.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-MU-1.0-20210430-Manuale_Utente_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
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
30/04/2021 
 
Livello di riservatezza 
L3 
 
 
Elenco versioni 
Versione 
Data  
Motivo 
Modifica 
1.0 
30/04/2021 
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
 
Responsabile Progetto Sistema Unitario e 
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
 
Referente Sicurezza 
Francesco Rosati 
RTI 
 
Referente Qualità e Sicurezza 
Andrea Castorino 
RTI 
 
Referente Applicativo Gestore Fascicolo 
Documentale 
Luigi Buglione 
RTI 
 
Referente Metrico

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-MU-1.0-20210430-Manuale_Utente_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 4/14 
INDICE DEI CONTENUTI 
1. 
INTRODUZIONE.............................................................................................................................. 5 
1.1. SCOPO DEL DOCUMENTO ................................................................................................................... 5 
1.2. GLOSSARIO ..................................................................................................................................... 5 
1.2.1. 
DEFINIZIONI ................................................................................................................................ 5 
1.2.2. 
ACRONIMI E ABBREVIAZIONI ............................................................................................................ 6 
2. 
RICHIESTA DEL CERTIFICATO PENALE ............................................................................................ 7 
2.1. SCOPO DELL’APPLICATIVO .................................................................................................................. 7 
2.2. TIPOLOGIE DI UTENTI ........................................................................................................................ 7 
2.3. RICHIESTA DEL CERTIFICATO PENALE DA SIEP ......................................................................................... 7 
2.4. RICHIESTA DEL CERTIFICATO PENALE DA SIUS ....................................................................................... 10

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-MU-1.0-20210430-Manuale_Utente_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 5/14 
1. Introduzione 
1.1. Scopo del documento 
Per garantire la continuità dei servizi di interconnessione ad oggi presenti tra il sistema SIES e SIC, si è reso 
necessario intervenire sugli attuali meccanismi di scambio ‘dati’ tra i due sistemi.  
L’intervento ha interessato l’allineamento dei vari ‘colloqui’ infrastrutturali relativamente a nuove 
dinamiche di autenticazione e profilazione.  
 
La fase post go-live si inserisce in uno scenario in cui l’applicazione SIC risulta integrata, a livello tre, con il 
progetto My Giustizia: 
• gli utenti, tramite browser, accedono e si autenticano su my.giustizia.it; 
• il portale verifica le credenziali ADN fornite; 
• l’utente seleziona l’applicazione e viene reindirizzato dal portale; 
• l’utente viene autenticato per accedere all’applicazione selezionata. 
 
L’attività definita come ‘mappatura utenti SIC – ADN’ fa riferimento all’introduzione, sul sistema SIC, di 
una nuova funzionalità di associazione/mappatura di un utente ADN con uno specifico utente/ufficio del 
SIC.  
 
In questo documento verrà descritta la funzionalità di Richiesta del certificato Penale oggetto di modifica 
nella parte di interconnessione con il sistema SIC. 
 
1.2. Glossario 
1.2.1. Definizioni 
Si premette un glossario esplicativo delle abbreviazioni e dei termini tecnici e giuridici utilizzati nel 
documento (Tabella - Glossario dei termini e degli acronimi usati nel documento). 
 
Definizione  
Descrizione  
Casellario giudiziale 
Il casellario giudiziale (detto anche casellario giudiziario), nell'ordinamento giuridico 
italiano, è uno schedario istituito presso la Procura della Repubblica di ogni tribunale 
ordinario della Repubblica italiana, con lo scopo di raccogliere e conservare gli estratti 
dei provvedimenti dell'autorità giudiziaria o amministrativa, in modo tale che sia sempre 
possibile conoscere l'elenco dei precedenti penali e civili di ogni cittadino. 
Certificato Penale 
Contiene i provvedimenti in materia penale, civile e amministrativa. Per il cittadino 
italiano, attesta anche la sussistenza o meno di iscrizioni nel casellario giudiziale 
europeo. 
Username  
Numero o parola utilizzati da un utente per farsi identificare da un sistema operativo, da 
un elaboratore o da un servizio online. 
Fascicolo penale  
Insieme degli atti cartacei relativi ad un procedimento penale  
Password 
Una password (in italiano anche detta parola d'accesso, parola d'ordine o chiave 
d'accesso) è, in ambito informatico e crittografico, una sequenza di caratteri 
alfanumerici utilizzata per accedere in modo esclusivo a una risorsa informatica

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-MU-1.0-20210430-Manuale_Utente_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 6/14 
Definizione  
Descrizione  
Welcome Page 
La welcome page (letteralmente pagina di benvenuto), anche chiamata home page, 
inizio, pagina d'inizio, pagina iniziale o pagina principale è solitamente la prima pagina di 
un sito web o un'applicazione web. 
 
1.2.2. Acronimi e abbreviazioni 
Sigla  
Descrizione  
ADN 
Advanced Digital Network 
DEC  
Direttore Esecutivo Contratto  
DGSIA  
Direzione Generale per i Sistemi Informativi Automatizzati  
PA  
Pubblica Amministrazione  
PST  
Portale dei Servizi Telematici  
RUF  
Responsabile Unico Fornitore  
RUP  
Responsabile Unico Progetto  
SIC 
Sistema Informativo del Casellario 
SIEP  
Sistema Informativo Esecuzione Penale 
SIES 
Sistema Informativo Esecuzione e Sorveglianza 
SIGE 
Sistema Informativo Giudice dell’Esecuzione 
SIUS  
Sistema Informativo Uffici Sorveglianza  
UTA  
Utente Generico Amministrazione

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-MU-1.0-20210430-Manuale_Utente_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 7/14 
2. Richiesta del Certificato Penale 
2.1. Scopo dell’applicativo 
A fronte degli interventi previsti in SIC, nel sistema SIES è stata adeguata la funzione relativa 
all’invocazione del servizio di Richiesta del Certificato. In particolare, in fase di chiamata del servizio, non 
saranno più passate le credenziali di accesso, username e password del SIC, ma il sistema SIES invierà lo 
user-Name ADN Giustizia. 
 
2.2. Tipologie di utenti 
Gli utenti a cui ci si rivolge sono gli utenti degli uffici giudiziari dei vari distretti che utilizzano i sottosistemi 
SIEP e SIUS. 
 
2.3. Richiesta del Certificato Penale da SIEP 
L’utente, dopo aver inserito le proprie credenziali ADN, selezionando il tasto ‘Entra’ in corrispondenza del 
proprio ufficio di procura sarà ridiretto nella welcome page dell’applicazione SIEP [Figura 1]: 
 
 
Figura 1 – Welcome page SIEP 
 
 
L’utente seleziona dal menu verticale la voce Istruttorie/Richieste e nella pagina che viene visualizzata clicca sulla 
voce Richiesta Certificato Penale [Figura 2]:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-MU-1.0-20210430-Manuale_Utente_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 8/14 
 
 
Figura 2 – Istruttorie/Richieste 
 
 
Il sistema visualizza la funzione di Ricerca Procedimento. L’utente dopo aver inserito gli estremi del procedimento 
clicca sul pulsante Conferma [Figura 3]: 
 
 
Figura 3 – Ricerca Procedimento

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-MU-1.0-20210430-Manuale_Utente_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 9/14 
Il sistema visualizza la pagina di Richiesta Certificato Penale. L’utente, dopo aver verificato le informazioni presenti 
nella schermata, clicca sul pulsante Richiesta Certificato [Figura 4]: 
 
Figura 4 – Richiesta Certificato 
 
Il sistema invia le credenziali ADN dell’utente al SIC con i dati necessari per la richiesta del certificato penale [Figura 
5]: 
 
 
Figura 5 – Inoltro Richiesta Certificato Penale

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-MU-1.0-20210430-Manuale_Utente_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 10/14 
 
2.4. Richiesta del Certificato Penale da SIUS 
L’utente, dopo aver inserito le proprie credenziali ADN, selezionando il tasto ‘Entra’ in corrispondenza del 
proprio ufficio di sorveglianza sarà ridiretto nella welcome page dell’applicazione SIUS [Figura 6]: 
 
 
Figura 6 – Welcome page SIUS 
 
 
L’utente seleziona dal menu verticale la voce Ricerche e Visualizzazioni e nella pagina che viene visualizzata clicca 
sulla voce Procedimento per N° SIUS [Figura 7]:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-MU-1.0-20210430-Manuale_Utente_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 11/14 
Figura 7 – Ricerche e Visualizzazioni 
 
 
Il sistema visualizza la funzione di Ricerca Procedimento. L’utente, dopo aver inserito gli estremi del procedimento 
SIUS, clicca sul pulsante Ricerca [Figura 8]: 
 
Figura 8 – Ricerca Procedimento

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-MU-1.0-20210430-Manuale_Utente_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 12/14 
Il sistema visualizza la pagina di Dettaglio Procedimento SIUS [Figura 9]: 
 
Figura 9 – Dettaglio Procedimento SIUS 
 
L’utente apre la lista delle funzionalità disponibili per il procedimento cercato e seleziona la voce Richiesta 
Certificato Penale [Figura 10]:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-MU-1.0-20210430-Manuale_Utente_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 13/14 
 
Figura 10 – Lista Funzioni Procedimento SIUS 
 
 
Viene visualizzata la pagina di Ricerca certificato Penale. L’utente, dopo aver verificato le informazioni presenti 
nella pagina, clicca sul pulsante Richiesta Certificato [Figura 11]:

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
 
SIUT-SIE-MU-1.0-20210430-Manuale_Utente_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 14/14 
Figura 11 – Richiesta Certificato Penale 
 
 
Il sistema invia le credenziali ADN dell’utente al SIC con i dati necessari per la richiesta del certificato penale [Figura 
12]: 
 
 
Figura 12 – Inoltro Richiesta Certificato Penale