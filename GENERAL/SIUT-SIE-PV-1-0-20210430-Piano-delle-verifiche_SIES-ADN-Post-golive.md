---
uniqueName: siut-sie-pv-1-0-20210430-piano-delle-verifichesies
displayName: "SIUT SIE PV 1 0 20210430 Piano delle verifiche SIES ADN Post golive"
category: "GENERAL"
tags: []
---

# SIUT-SIE-PV-1.0-20210430-Piano delle verifiche_SIES-ADN-Post-golive

> **File originale:** `MEV/Integrazione SIES-ADN/RILASCIO_MEV_SIES-ADN (POST GO-LIVE)/20210430_1.0/SIUT-SIE-PV-1.0-20210430-Piano delle verifiche_SIES-ADN-Post-golive.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati  
 
 
Piano delle verifiche 
Integrazione SIES-ADN-Post-golive 
 
 
 
 
 
 
 
 
 
Versione 1.0 del 30/04/2021

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PV-1.0-20210430 Piano delle verifiche_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 2/10 
 
 
 
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
 
 
SIUT-SIE-PV-1.0-20210430 Piano delle verifiche_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 3/10 
Approvazioni 
 
Nominativo 
Funzione 
Elaborato da 
Domenico Nania 
Analista Funzionale 
Verificato da 
Vito Bufi 
Responsabile Manutenzione Sistemi Attuali 
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
Prima Emissione 
 
 
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
 
 
SIUT-SIE-PV-1.0-20210430 Piano delle verifiche_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 4/10 
1 INDICE DEI CONTENUTI 
1 
INTRODUZIONE............................................................................................................................... 5 
1.1 
SCOPO DEL DOCUMENTO ............................................................................................................................. 5 
1.2 
RIFERIMENTI ............................................................................................................................................. 5 
1.3 
GLOSSARIO ............................................................................................................................................... 5 
1.3.1 
DEFINIZIONI .......................................................................................................................................... 5 
1.3.2 
ACRONIMI E ABBREVIAZIONI ...................................................................................................................... 5 
2 
CARATTERISTICHE E METRICHE DI VALUTAZIONE DELLA QUALITÀ DEL SOFTWARE ....................... 7 
2.1 
SCHEDE DI VERIFICA .................................................................................................................................... 7 
3 
CLASSIFICAZIONE DELLE DIFFORMITÀ ............................................................................................ 8 
3.1 
CLASSI DI RILEVANZA ................................................................................................................................... 8 
3.2 
CLASSI DI GRAVITÀ...................................................................................................................................... 9 
3.3 
SOGLIA DI ACCETTAZIONE ............................................................................................................................. 9 
3.4 
TEMPI DI RISOLUZIONE DELLE DIFFORMITÀ ..................................................................................................... 10 
3.5 
SOGLIA DI REITERAZIONI DIFFORMITÀ (RICICLO CORRETTIVO) ............................................................................. 10

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PV-1.0-20210430 Piano delle verifiche_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 5/10 
1 Introduzione 
1.1 Scopo del documento 
Nel presente documento sono riportate le caratteristiche di qualità che deve possedere il software 
realizzato nell’intervento di integrazione delle attività previste in scheda SIUT-SIC-SC-1.0-20200924-Scheda 
intervento Scheda_n.3_2019 Sostituzione IGI.pdf, nonché le metriche utilizzate ed applicate in sede di 
verifica di conformità. 
Le caratteristiche di qualità del prodotto software sono quelle indicate nell’Allegato 1 della “Procedura 
di gara informale ex art. 162 D.Lgs 50/2016” e sono formalizzate, ove possibile, secondo lo standard 
ISO/IEC 25000:2014. 
Le caratteristiche da sottoporre alla verifica di conformità sono strettamente correlate alle tecnologie 
adottate, all’ambiente software ed alla tipologia di rilascio dell’intervento oggetto di verifica. 
Il presente Piano di Verifica, redatto dal Fornitore, dovrà essere approvato dall’Amministrazione. 
1.2 Riferimenti 
Riferimento 
Nome Documento 
Descrizione Documento 
RIF1. 
 
Capitolato Tecnico – Allegato 1 
Caratteristiche Qualità 
RIF2. 
 
SIUT-SIE-PT-1.0-20210430-Piano_dei_Test_SIES-ADN-Post-
golive 
Piano dei Test 
RIF3. 
 
SIUT-SIE-CT-1.0-20210430-Allegato_al_piano_test_SIES-ADN-
Post-golive 
Elenco del piano dei test da 
eseguire per la verifica di 
conformità 
1.3 Glossario 
1.3.1 
Definizioni 
Definizione 
Descrizione 
 
 
 
 
1.3.2 
Acronimi e abbreviazioni 
Sigla 
Descrizione 
AgID 
Agenzia per l’Italia Digitale 
API 
Application Programming Interface 
CPU 
Central Processing Unit 
CV 
Curriculum Vitae 
DB 
Data Base 
DEC 
Direttore Esecutivo Contratto 
DGSIA 
Direzione Generale per i Sistemi Informativi Automatizzati 
DR 
Disaster Recovery 
ETSI 
European Telecommunications Standards Institute 
FP 
Function Point 
GdL 
Gruppo di Lavoro 
GDPR 
General Data Protection Regulation 
HW 
HardWare 
ICT 
Information & Communication Technology 
ISO 
International Organization for Standardization 
ISP 
Information Security Policy

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PV-1.0-20210430 Piano delle verifiche_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 6/10 
Sigla 
Descrizione 
IT 
Information Technology 
KPI 
Key Performance Indicator 
MAAC 
MAndatory Access Control 
MAC 
MAnutenzione Correttiva 
MEV 
Manutenzione Evolutiva 
OWASP 
Open Web Application Security Project 
PA 
Pubblica Amministrazione 
PEC 
Posta Elettronica Certificata 
PDCA 
Plan, Do, Check, Act 
PdQ 
Piano della Qualità 
PdP 
Piano di Progetto 
PdS 
Piano della Sicurezza 
PMO 
Program Management Office 
POO 
Program Operating Office 
QM 
Quality Manager 
RA 
Risk Assessment 
RID 
Riservatezza, Integrità, Disponibilità 
RM 
Resource Manager 
RPO 
Recovery Point Objective 
RTO 
Recovery Time Objective 
RTI 
Raggruppamento Temporaneo di Impresa 
RUF 
Responsabile Unico Fornitore 
RUP 
Responsabile Unico Progetto 
SAL 
Stato Avanzamento Lavori 
SGQ 
Sistema di Gestione per la Qualità di Engineering Ingegneria Informatica S.p.A. 
SGSI 
Sistema di Gestione della Sicurezza Informatica 
SIU 
Sistema Informativo Unitario 
SLA 
Service Level Agreement 
SM 
Security Manager 
SQL 
Structured Query Language 
SW 
SoftWare 
TT 
Trouble Ticketing 
UTA 
Utente Generico Amministrazione 
VPN 
Virtual Private Network

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PV-1.0-20210430 Piano delle verifiche_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 7/10 
2 CARATTERISTICHE E METRICHE DI VALUTAZIONE DELLA QUALITÀ DEL SOFTWARE  
In questa sezione viene riportato l’elenco le caratteristiche di qualità del software e relative metriche 
che dovranno essere rispettate in sede di verifica di conformità dell’intervento in oggetto. 
2.1 Schede di verifica 
Tipo Verifica 
Attributo  
Indicatore  
Scopo  
Adeguatezza 
delle 
funzionalità 
Completezza 
Funzionale 
Copertura 
dei 
requisiti 
Misura il grado di copertura funzionale offerta sulla base 
dell’analisi dei requisiti, delle funzionalità e degli obiettivi 
richiesti 
Adeguatezza 
delle 
funzionalità 
Correttezza 
Funzionale 
Aderenza 
ai 
Requisiti 
Misura il grado con cui le funzionalità implementate rispettano 
i requisiti richiesti 
Adeguatezza 
delle 
funzionalità 
Appropriatezza 
funzionale 
Conformità 
alle 
normative 
Misura l’aderenza delle funzionalità implementate rispetto alle 
normative pertinenti 
Affidabilità 
Robustezza 
Robustezza 
del 
software 
Misura la capacità del sistema di gestire condizioni non previste 
dalle specifiche 
Manutenibilità Analizzabilità 
Leggibilità 
del 
codice 
Misura la facilità di comprensione del codice, per esempio con 
riferimento ai nomi utilizzati per i moduli, le funzioni e le 
variabili, ai commenti e alla dimensione dei moduli e delle 
funzioni 
Manutenibilità Analizzabilità 
Copertura 
documentazione  
tecnica 
Misura il livello di completezza della documentazione tecnica di 
moduli e funzioni 
Manutenibilità Analizzabilità 
Adeguatezza 
documentazione  
tecnica 
Misura la qualità descrittiva della documentazione tecnica di 
moduli e funzioni 
Manutenibilità Verificabilità 
Completezza dei  
test 
Misura il grado di copertura del codice sviluppato da parte di 
test (di varia natura, come test unitari, test di integrazione, test 
end-to-end, test di accettazione, test di regressione, test di 
qualità) 
Tabella 1 - Esempio di Misure e Metriche da applicare

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PV-1.0-20210430 Piano delle verifiche_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 8/10 
3 CLASSIFICAZIONE DELLE DIFFORMITÀ  
Ai fini della verifica di conformità dei sistemi sottoposti a intervento, il Piano di Verifica identifica i limiti 
rispetto alle diverse tipologie di difformità che possono essere tollerate in sede di verifica.  
A tale proposito, le funzionalità del sistema e le difformità dovranno essere classificate secondo il 
seguente approccio:  
• 
Il Piano di Verifica identifica un certo numero di classi di rilevanza al fine di classificare le varie 
funzionalità del sistema (cfr. Tabella 2); 
• 
Il Piano di Verifica identifica un certo numero di classi di gravità al fine di classificare le difformità 
riscontrate (cfr. Tabella 3); 
• 
In fase di verifica, per ogni eventuale difformità rilevata viene identificata la relativa classe di 
gravità e la relativa classe di rilevanza, in riferimento alla funzionalità affetta dalla difformità. 
Complessivamente, nella redazione del Piano di Verifica l’Amministrazione ed il Fornitore, 
congiuntamente, danno indicazione delle seguenti informazioni:  
• 
Descrizione delle classi di rilevanza delle funzionalità; 
• 
Descrizione delle classi di gravità delle difformità; 
• 
Per ogni coppia classe di rilevanza/classe di gravità, il numero massimo di difformità (detto soglia 
di ammissibilità) che possono essere tollerate in sede di verifica affinché la verifica stessa possa 
proseguire; 
• 
Tempi di gestione delle difformità. 
3.1 Classi di rilevanza  
La classe di rilevanza descrive l’impatto che una specifica funzionalità ha sul soddisfacimento dei 
requisiti di sistema. In particolare, essa descrive il grado di importanza che la funzionalità ricopre 
all’interno del flusso lavorativo, impattando sull’operatività degli utenti. 
La Tabella 2 seguente descrive tre classi di rilevanza per le funzionalità, rispetto al loro obiettivo: 
Classe di rilevanza  
Descrizione  
Rilevanza-A  
La funzionalità è indispensabile all’operatività del flusso produttivo. Un suo mancato 
funzionamento determina l’impossibilità da parte dell’utente di espletare il proprio lavoro. 
Rilevanza-B  
La funzionalità non è centrale per l’operatività del flusso produttivo. Un suo mancato 
funzionamento determina l’impossibilità per gli utenti di espletare una parte delle proprie 
attività. 
Rilevanza-C  
La funzionalità è marginale rispetto all’operatività del flusso produttivo. Un suo mancato 
funzionamento non determina l’impossibilità degli utenti di espletare il proprio lavoro (tutto o 
in parte), tuttavia ne determina un netto e sostanziale impedimento o rallentamento. 
Tabella 2 - Classi di rilevanza delle funzionalità

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PV-1.0-20210430 Piano delle verifiche_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 9/10 
3.2 Classi di gravità  
La classe di gravità descrive l’impatto che la difformità ha sul soddisfacimento dei requisiti di qualità e 
tiene conto del danno economico o di immagine che ne potrebbe derivare all’Amministrazione o a terzi. 
La Tabella 3 riporta la classificazione delle difformità. 
 
Classe di gravità  
Descrizione  
Grado-1  
Il malfunzionamento determina la totale impossibilità di utilizzo della funzionalità affetta dallo 
stesso  
Grado-2  
Il malfunzionamento determina il parziale utilizzo della funzionalità  
Grado-3  
Il malfunzionamento non determina l’impossibilità – totale o parziale – di utilizzo della funzionalità 
ma ne impatta la struttura di presentazione grafica delle informazioni all’utente, degli oggetti di 
interazione o simili 
Grado-4 
Il malfunzionamento è di tipo marginale e non rientra nelle prime tre classi 
Tabella 3 – Classificazione delle gravità 
3.3 Soglia di accettazione   
In questo paragrafo sono specificate le soglie massime ammesse per le varie tipologie di difformità 
tollerabili in sede di verifica dell’intervento in oggetto. 
Specificatamente, le soglie di accettazione sono definite sulla base di due dimensioni: la classe di gravità 
della difformità e la classe di rilevanza della funzionalità che ne è affetta. 
La Tabella 4 riporta le soglie di accettazione. 
In fase di verifica, il numero di non conformità riscontrate per ogni classe di difformità viene 
globalmente conteggiato come somma di tutte le difformità con la medesima classe di gravità e classe 
di rilevanza sull’insieme di tutte le funzionalità soggette a verifica. 
Se tale somma eccede la soglia di accettazione per quella specifica classe di difformità, l’esito della 
verifica è negativo. 
Finché tutte le soglie di accettazione sono rispettate, il Fornitore avrà facoltà di risolvere le non 
conformità rilevate secondo le modalità definite più avanti. 
Classe di rilevanza  
Classe di gravità 
Grado-1  
Grado-2  
Grado-3  
Grado-4 
Rilevanza-A  
0 
0 
0 
0 
Rilevanza-B  
0 
2 
0 
0 
Rilevanza-C  
0 
0 
0 
0 
Tabella 4 - Soglie di accettazioni per ogni classe di difformità

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
SIUT-SIE-PV-1.0-20210430 Piano delle verifiche_SIES-ADN-Post-golive 
Ver. 1.0 del 30/04/2021 
Pag. 10/10 
3.4 Tempi di risoluzione delle difformità  
Il Piano di Verifica definisce, per ogni classe di gravità ed indipendentemente dalla classe di rilevanza 
della funzionalità affetta, il tempo massimo che ha il Fornitore per la risoluzione di una difformità 
rilevata. In particolare, tale valore descrive il tempo che intercorre tra la presa in carico della difformità 
da parte del Fornitore ed il momento in cui ritiene la stessa risolta, dando disponibilità di nuova verifica. 
Nella Tabella 5 si riporta lo schema che identifica i suddetti tempi. 
 
Classe di gravità  
Tempo massimo di risoluzione  
Grado-1 
16 ore 
Grado-2 
8 ore  
Grado-3 
6 ore  
Grado-4 
4 ore  
Tabella 5 - Tempi di risoluzione della difformità  
L’istante temporale a partire dal quale decorrono i tempi di cui sopra decorre dal termine della giornata 
lavorativa di verifica. 
Dai tempi massimi sono esclusi i tempi tecnici strettamente necessari al solo dispiegamento delle nuove 
versioni del software contenenti le correzioni interessate. 
In casi particolarmente critici, la commissione, in sede di verifica, può definire tempi diversi di gestione. 
3.5 Soglia di reiterazioni difformità (riciclo correttivo) 
Sono previste delle possibili reiterazioni degli interventi correttivi da parte del Fornitore, a fronte del 
rilevamento di una difformità il cui iniziale intervento correttivo non sia stato risolutivo. 
Sono previste per ogni coppia classe di gravità/classe di rilevanza un massimo di 10 ricicli 
compatibilmente con il numero ammissibile di difformità. 
Da sottolineare che ogni difformità ridurrà comunque di una unità la soglia di accettazione (cfr. Tabella 
4), sia nel caso di primo riscontro sia nel caso di una ripresentazione della stessa.