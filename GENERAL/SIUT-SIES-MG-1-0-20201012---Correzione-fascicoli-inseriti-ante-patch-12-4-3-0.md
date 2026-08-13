---
uniqueName: siut-sies-mg-1-0-20201012-correzione-fascicoli-ins
displayName: "SIUT SIES MG 1 0 20201012   Correzione fascicoli inseriti ante patch 12 4 3 0"
category: "GENERAL"
tags: []
---

# SIUT-SIES-MG-1.0-20201012 - Correzione fascicoli inseriti ante patch 12.4.3.0

> **File originale:** `RILASCIO_12.4.3.0/SIUT-SIES-MG-1.0-20201012 - Correzione fascicoli inseriti ante patch 12.4.3.0.doc`  
> **Tipo:** DOC

---

Ministero della Giustizia 

Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 

Direzione Generale per i Sistemi Informativi Automatizzati 

 

 

Ministero della Giustizia 

Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 

Direzione Generale per i Sistemi Informativi Automatizzati 

 



 

Ministero della Giustizia 

Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi Direzione Generale per i Sistemi Informativi Automatizzati 

 

 

SIUT-SIES-MG-1.0-20201007

Correzione fascicoli inseriti ante patch 12.4.3.0

 

 

 

 

 

 

 

 

 

Versione 1.0 del 12/10/2020 

 

 	 

 

 

 

Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A - Sirfin-PA, nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del sistema informativo unitario telematico, la manutenzione degli attuali sistemi dell’area penale del Ministero della Giustizia e servizi correlati. Lotto 1”. 

 

 	 


Approvazioni

 

Nominativo 

Elaborato da 

Engineering 

Verificato da 

Vito Bufi 

Approvato da 

Paolo Ceccanti 

Data approvazione 

12/10/2020 

Livello di riservatezza 

L4 

 

Elenco versioni

Versione 

Data  

Motivo 

Modifica 

1.0 

12/10/2020 

Prima Emissione 

 

 

Lista di distribuzione

Nominativo

Organizzazione

Ufficio

Funzione

Ing. Giovanni Malesci

Amministrazione



Responsabile Unico Procedimento

Dr.ssa Anna Maria Palmieri

Amministrazione



Direttore Esecutivo Contratto

Paolo Ceccanti

RTI



Responsabile Unico Fornitura

Pasquale Lamattina

RTI



Referente Tecnico

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

Fabio Gattamorta

RTI



Responsabile PMO 

Alessandro Falleni

RTI



Referente sicurezza

Edoardo Lamuraglia

RTI



Referente qualità

Francesco Rosati

RTI



Referente qualità

Andrea Castorino

Alessandro Lanari

RTI



Referente Applicativo Gestore Fascicolo Documentale

Luigi Buglione

RTI



Referente Metrico

 




 

INDICE DEI CONTENUTI 

1 	Introduzione	5

	1.1 Scopo del documento	5

	1.2 Riferimenti	5

	1.3 Glossario	5

	1.3.1 Definizioni	5

	1.3.2 Acronimi e abbreviazioni	5

2 	Generalità	8

3 	Descrizione delle Attività	9

	2.1 Procedura di intervento	9

 	 


	1 	Introduzione 

		1.1 Scopo del documento 

Il presente documento viene rilasciato con lo scopo di dettagliare le attività relative alla correzione dei fascicoli impattati dall’errore segnalato nel Ticket 20200915015 e corretto nel rilascio della patch 12.4.3.0.  

Il problema segnalato nel suddetto ticket era causato da un errato inserimento dei dati in fase di creazione di un fascicolo di classe 7 a partire da un fascicolo di classe 1. 

Il sistema, nel duplicare sulla classe 7 lo Stato Procedimento della classe 1, lasciava valorizzato il campo EVE_ID_EVENTO nella tabella STATO_PROCEDIMENTO che continuava a fare riferimento all’evento del fascicolo di origine. Questo rendeva impossibile l'acquisizione del fascicolo di classe 7 su un altro distretto per violazione della Foreign_Key tra Stato Procedimento ed Evento. L'evento infatti non era oggetto di trasferimento in quanto apparteneva ad un altro fascicolo.

In particolare, nel seguente documento, si forniscono le istruzioni per l’esecuzione della procedura di correzione ed i relativi controlli PRE e POST correzione. 

		1.2 Riferimenti 

Riferimento 

Nome Documento 





Descrizione Documento 

RIF1. 

SIUT-SIES-PR-1.0-20201012-Piano_di_Rilascio_SIES_v.12.4.3.0

Piano di rilascio 

		1.3 Glossario 

		1.3.1 Definizioni 

		

		

		

Definizione 

Descrizione 







 

 

 

		1.3.2 Acronimi e abbreviazioni 

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

IT

Information Technology

KPI

Key Performance Indicator

MAAC

MAndatory Access Control

MAC

MAnutenzione Correttiva

MEV

Manutenzione EVolutiva

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




	2 	Generalità 

In relazione alla correzione dati di cui in oggetto, si fa presente che da uno studio delle casistiche di errore, il problema si verifica solo nel caso in cui il fascicolo di classe 7 viene ricercato ed importato da altro distretto subito dopo la sua creazione.

Se invece tale fascicolo è soggetto ad attività che ne modificano lo stato procedimento, per esempio trasmissione su altro distretto, il problema si risolve da solo. Infatti, la modifica dello stato procedimento prevede la sua cancellazione e nuovo inserimento. In questo modo il record contenente l'errato puntamento viene cancellato e non si verifica più l'errore in fase di trasferimento. 

 


	3 	Descrizione delle Attività 

 

Le attività descritte di seguito presuppongono che siano stati effettuati i primi tre step del paragrafo 6.3.1.1 contenuti nel documento SIUT-SIES-PR-1.0-20201012-Piano_di_Rilascio_SIES_v.12.4.3.0.doc. 

 

La creazione della tabella di appoggio è solo a scopo cautelativo per storicizzare il dato prima della sua modifica.

 

		2.1 Procedura di intervento 

 

Su Oracle eseguire le seguenti attività: 



creazione di una tabella appoggio (STATO_PROCEDIMENTO_APPO) per la preventiva estrazione dei dati che risultano erroneamente inseriti e che saranno oggetto di correzione

CREATE TABLE STATO_PROCEDIMENTO_APPO (

  STA_PROGRESSIVO NUMBER,

  STA_FAS_SIE_ID_FASCICOLO_SIEP NUMBER,

  STA_COD_STATO_PROCEDIMENTO VARCHAR2(4),

  STA_DATA DATE,

  STA_COD_OPERATORE_INSERIMENTO VARCHAR2(100),

  STA_DATA_INSERIMENTO DATE,

  STA_COD_UFFICIO_INSERIMENTO VARCHAR2(11),

  STA_EVE_ID_EVENTO NUMBER(38,0),

  EVEN_ID_EVENTO NUMBER(38,0),

  EVEN_COD_TIPO_EVENTO VARCHAR2(2),

  EVEN_COD_TIPO_PROVVEDIMENTO VARCHAR2(2),

  EVEN_COD_MOTIVO VARCHAR2(4),

  EVEN_FAS_SIE_ID_FASCICOLO_SIEP NUMBER(38,0),

  FAS_STA_ID_FASCICOLO_SIEP NUMBER(38,0),

  FAS_STA_CHIAVE_ANNO NUMBER(4,0),

  FAS_STA_CHIAVE_PROGR NUMBER(38,0),

  FAS_STA_CHIAVE_UFFICIO VARCHAR2(11),

  FAS_EVE_ID_FASCICOLO_SIEP NUMBER(38,0),

  FAS_EVE_CHIAVE_ANNO NUMBER(4,0),

  FAS_EVE_CHIAVE_PROGR NUMBER(38,0),

  FAS_EVE_CHIAVE_UFFICIO VARCHAR2(11),

  DATA_ESTRAZIONE DATE

);

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."STA_PROGRESSIVO" IS 'Copia Campi STATO_PROCEDIMENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."STA_FAS_SIE_ID_FASCICOLO_SIEP" IS 'Copia Campi STATO_PROCEDIMENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."STA_COD_STATO_PROCEDIMENTO" IS 'Copia Campi STATO_PROCEDIMENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."STA_DATA" IS 'Copia Campi STATO_PROCEDIMENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."STA_COD_OPERATORE_INSERIMENTO" IS 'Copia Campi STATO_PROCEDIMENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."STA_DATA_INSERIMENTO" IS 'Copia Campi STATO_PROCEDIMENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."STA_COD_UFFICIO_INSERIMENTO" IS 'Copia Campi STATO_PROCEDIMENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."STA_EVE_ID_EVENTO" IS 'Copia Campi STATO_PROCEDIMENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."EVEN_ID_EVENTO" IS 'Copia Campi EVENTO puntato da STATO_PROCEDIMENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."EVEN_COD_TIPO_EVENTO" IS 'Copia Campi EVENTO puntato da STATO_PROCEDIMENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."EVEN_COD_TIPO_PROVVEDIMENTO" IS 'Copia Campi EVENTO puntato da STATO_PROCEDIMENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."EVEN_COD_MOTIVO" IS 'Copia Campi EVENTO puntato da STATO_PROCEDIMENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."EVEN_FAS_SIE_ID_FASCICOLO_SIEP" IS 'Copia Campi EVENTO puntato da STATO_PROCEDIMENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."FAS_STA_ID_FASCICOLO_SIEP" IS 'Copia Campi FASCICOLO puntato da STATO_PROCEDIMENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."FAS_STA_CHIAVE_ANNO" IS 'Copia Campi FASCICOLO puntato da STATO_PROCEDIMENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."FAS_STA_CHIAVE_PROGR" IS 'Copia Campi FASCICOLO puntato da STATO_PROCEDIMENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."FAS_STA_CHIAVE_UFFICIO" IS 'Copia Campi FASCICOLO puntato da STATO_PROCEDIMENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."FAS_EVE_ID_FASCICOLO_SIEP" IS 'Copia Campi FASCICOLO puntato da EVENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."FAS_EVE_CHIAVE_ANNO" IS 'Copia Campi FASCICOLO puntato da EVENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."FAS_EVE_CHIAVE_PROGR" IS 'Copia Campi FASCICOLO puntato da EVENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."FAS_EVE_CHIAVE_UFFICIO" IS 'Copia Campi FASCICOLO puntato da EVENTO';

   COMMENT ON COLUMN "STATO_PROCEDIMENTO_APPO"."DATA_ESTRAZIONE" IS 'Data estrazione dei dati dalla tabella STATO_PROCEDIMENTO';

   COMMENT ON TABLE "STATO_PROCEDIMENTO_APPO"  IS 'Tabella di appoggio per l''estrazione dei record della tabella STATO_PROCEDIMENTO che presentano EVE_ID_EVENTO erroneamente valorizzato. Ticket 20200915015.';



Query di conteggio preventivo dei record della tabella STATO_PROCEDIMENTO impattati.

SELECT count(*)

FROM STATO_PROCEDIMENTO, EVENTO, FASCICOLO_SIEP FAS_STA, FASCICOLO_SIEP FAS_EVE

WHERE 1=1

AND STATO_PROCEDIMENTO.EVE_ID_EVENTO = EVENTO.ID_EVENTO

AND STATO_PROCEDIMENTO.EVE_ID_EVENTO IS NOT null

AND STATO_PROCEDIMENTO.FAS_SIE_ID_FASCICOLO_SIEP <> EVENTO.FAS_SIE_ID_FASCICOLO_SIEP

AND STATO_PROCEDIMENTO.FAS_SIE_ID_FASCICOLO_SIEP = FAS_STA.ID_FASCICOLO_SIEP

AND EVENTO.FAS_SIE_ID_FASCICOLO_SIEP = FAS_EVE.ID_FASCICOLO_SIEP

AND (FAS_STA.CHIAVE_PROGR > 70000 AND FAS_STA.CHIAVE_PROGR<=79999)



script di popolamento della tabella di appoggio. Tale script effettuerà una copia integrale dei dati dei record della tabella STATO_PROCEDIMENTO che saranno identificati come "da correggere". Per facilità di lettura sulla tabella verranno riportati anche i dati identificativi del fascicolo puntato dallo stato procedimento, dell'evento puntato erroneamente e del fascicolo a cui tale evento appartiene.

INSERT INTO STATO_PROCEDIMENTO_APPO (

  STA_PROGRESSIVO ,

  STA_FAS_SIE_ID_FASCICOLO_SIEP ,

  STA_COD_STATO_PROCEDIMENTO ,

  STA_DATA ,

  STA_COD_OPERATORE_INSERIMENTO ,

  STA_DATA_INSERIMENTO ,

  STA_COD_UFFICIO_INSERIMENTO ,

  STA_EVE_ID_EVENTO ,

  EVEN_ID_EVENTO  ,

  EVEN_COD_TIPO_EVENTO ,

  EVEN_COD_TIPO_PROVVEDIMENTO ,

  EVEN_COD_MOTIVO ,

  EVEN_FAS_SIE_ID_FASCICOLO_SIEP  ,

  FAS_STA_ID_FASCICOLO_SIEP  ,

  FAS_STA_CHIAVE_ANNO,

  FAS_STA_CHIAVE_PROGR  ,

  FAS_STA_CHIAVE_UFFICIO ,

  FAS_EVE_ID_FASCICOLO_SIEP  ,

  FAS_EVE_CHIAVE_ANNO ,

  FAS_EVE_CHIAVE_PROGR  ,

  FAS_EVE_CHIAVE_UFFICIO,

  DATA_ESTRAZIONE)

SELECT STATO_PROCEDIMENTO.PROGRESSIVO, STATO_PROCEDIMENTO.FAS_SIE_ID_FASCICOLO_SIEP

, STATO_PROCEDIMENTO.COD_STATO_PROCEDIMENTO, STATO_PROCEDIMENTO."DATA"

, STATO_PROCEDIMENTO.COD_OPERATORE_INSERIMENTO, STATO_PROCEDIMENTO.DATA_INSERIMENTO

, STATO_PROCEDIMENTO.COD_UFFICIO_INSERIMENTO

, STATO_PROCEDIMENTO.EVE_ID_EVENTO

, EVENTO.ID_EVENTO, EVENTO.COD_TIPO_EVENTO, EVENTO.COD_TIPO_PROVVEDIMENTO, EVENTO.COD_MOTIVO

, EVENTO.FAS_SIE_ID_FASCICOLO_SIEP

, FAS_STA.ID_FASCICOLO_SIEP, FAS_STA.CHIAVE_ANNO, FAS_STA.CHIAVE_PROGR, FAS_STA.CHIAVE_UFFICIO

, FAS_EVE.ID_FASCICOLO_SIEP, FAS_EVE.CHIAVE_ANNO, FAS_EVE.CHIAVE_PROGR, FAS_EVE.CHIAVE_UFFICIO

, sysdate

FROM STATO_PROCEDIMENTO, EVENTO, FASCICOLO_SIEP FAS_STA, FASCICOLO_SIEP FAS_EVE

WHERE 1=1

AND STATO_PROCEDIMENTO.EVE_ID_EVENTO = EVENTO.ID_EVENTO

AND STATO_PROCEDIMENTO.EVE_ID_EVENTO IS NOT null

AND STATO_PROCEDIMENTO.FAS_SIE_ID_FASCICOLO_SIEP <> EVENTO.FAS_SIE_ID_FASCICOLO_SIEP

AND STATO_PROCEDIMENTO.FAS_SIE_ID_FASCICOLO_SIEP = FAS_STA.ID_FASCICOLO_SIEP

AND EVENTO.FAS_SIE_ID_FASCICOLO_SIEP = FAS_EVE.ID_FASCICOLO_SIEP

AND (FAS_STA.CHIAVE_PROGR > 70000 AND FAS_STA.CHIAVE_PROGR<=79999);

COMMIT;

 

verifica della corretta estrazione dei record. La count deve coincidere con il risultato della query del punto 2

SELECT count(*)

FROM STATO_PROCEDIMENTO_APPO



script di correzione dei record della tabella STATO_PROCEDIMENTO. Lo script preleverà dalla tabella appoggio gli identificativi (chiavi) dei record da correggere ed imposterà a null il valore del campo EVE_ID_EVENTO erroneamente valorizzato.

UPDATE STATO_PROCEDIMENTO SET EVE_ID_EVENTO = NULL

where (STATO_PROCEDIMENTO.PROGRESSIVO

     , STATO_PROCEDIMENTO.FAS_SIE_ID_FASCICOLO_SIEP

     , STATO_PROCEDIMENTO.COD_STATO_PROCEDIMENTO

     , STATO_PROCEDIMENTO.EVE_ID_EVENTO

     , STATO_PROCEDIMENTO.DATA_INSERIMENTO

)

in (select STA_PROGRESSIVO,

           STA_FAS_SIE_ID_FASCICOLO_SIEP ,

           STA_COD_STATO_PROCEDIMENTO ,

           STA_EVE_ID_EVENTO,

           STA_DATA_INSERIMENTO

      from STATO_PROCEDIMENTO_APPO

   ) ;

COMMIT;



script di verifica del corretto esito della procedura di correzione: rieseguire il passo 2 ed il risultato atteso deve essere 0. In tal caso la procedura di correzione ha avuto esito positivo, tralasciare il punto 7 e proseguire come indicato nel punto 8. 

In caso di esito negativo del controllo, ovvero count diversa da 0, continuare con il punto 7 con lo script di rollback, tralasciare il resto delle istruzioni e passare direttamente al punto 3 del paragrafo 6.3.2.1 descritto nel documento SIUT-SIES-PR-1.0-20201012-Piano_di_Rilascio_SIES_v.12.4.3.0 per il riavvio del server.



script di rollback. Lo script consentirà di ripristinare il valore EVE_ID_EVENTO sui record della tabella STATO_PROCEDIMENTO aggiornati dalla procedura se ve ne fosse necessità. Questo step è omesso se i primi 6 step sono avvenuti correttamente.

UPDATE STATO_PROCEDIMENTO SET EVE_ID_EVENTO =

(

SELECT STATO_PROCEDIMENTO_APPO.STA_EVE_ID_EVENTO

  FROM STATO_PROCEDIMENTO_APPO

 WHERE STATO_PROCEDIMENTO.PROGRESSIVO = STATO_PROCEDIMENTO_APPO.STA_PROGRESSIVO

   AND STATO_PROCEDIMENTO.FAS_SIE_ID_FASCICOLO_SIEP = STATO_PROCEDIMENTO_APPO.STA_FAS_SIE_ID_FASCICOLO_SIEP

   AND STATO_PROCEDIMENTO.COD_STATO_PROCEDIMENTO = STATO_PROCEDIMENTO_APPO. STA_COD_STATO_PROCEDIMENTO

   AND STATO_PROCEDIMENTO.DATA_INSERIMENTO = STATO_PROCEDIMENTO_APPO.STA_DATA_INSERIMENTO

   AND STATO_PROCEDIMENTO.COD_OPERATORE_INSERIMENTO = STATO_PROCEDIMENTO_APPO.STA_COD_OPERATORE_INSERIMENTO

   AND STATO_PROCEDIMENTO.COD_UFFICIO_INSERIMENTO = STATO_PROCEDIMENTO_APPO.STA_COD_UFFICIO_INSERIMENTO

)

WHERE EXISTS (SELECT 1 

               FROM STATO_PROCEDIMENTO_APPO 

              WHERE STATO_PROCEDIMENTO.PROGRESSIVO = STATO_PROCEDIMENTO_APPO.STA_PROGRESSIVO

                AND STATO_PROCEDIMENTO.FAS_SIE_ID_FASCICOLO_SIEP = STATO_PROCEDIMENTO_APPO.STA_FAS_SIE_ID_FASCICOLO_SIEP

                AND STATO_PROCEDIMENTO.COD_STATO_PROCEDIMENTO = STATO_PROCEDIMENTO_APPO. STA_COD_STATO_PROCEDIMENTO

                AND STATO_PROCEDIMENTO.DATA_INSERIMENTO = STATO_PROCEDIMENTO_APPO.STA_DATA_INSERIMENTO

                AND STATO_PROCEDIMENTO.COD_OPERATORE_INSERIMENTO = STATO_PROCEDIMENTO_APPO.STA_COD_OPERATORE_INSERIMENTO

                AND STATO_PROCEDIMENTO.COD_UFFICIO_INSERIMENTO = STATO_PROCEDIMENTO_APPO.STA_COD_UFFICIO_INSERIMENTO

            );

COMMIT;

			

NB: i record della tabella STATO_PROCEDIMENTO sono per loro natura soggetti a cancellazione ed inserimento da parte dell'applicativo SIEP quando lo stato del fascicolo evolve. Pertanto, il lancio dello script di rollback ha senso solo per ripristinare i dati prima del riavvio del server.



Se la correzione dei fascicoli, descritta in questo documento, è terminata positivamente procedere dallo step 5 del par. 6.3.1.1 del documento SIUT-SIES-PR-1.0-20201012-Piano_di_Rilascio_SIES_v.12.4.3.0.doc.





SIUT-SIES-MG-1.0-20200228 - Bonifica Soggetti Impugnanti 

		SIGE 	Ver. 1.0 del 28/02/2020 	Pag. 2/12 

 

SIUT-SIES-MG-1.0-20201012 - Correzione fascicoli inseriti ante patch 12.4.3.0	Ver. 1.0 del 12/10/2020

        Pag. 14/14