---
uniqueName: mltabellainesistente
displayName: "ML TABELLA INESISTENTE"
category: "GENERAL"
tags: []
---

# ML_TABELLA_INESISTENTE

> **File originale:** `MEV/SCHEDA_033/ML_TABELLA_INESISTENTE.docx`  
> **Tipo:** DOCX

---

# PROVVEDIMENTO_SIES_NSC
tabella di working contenente i dati relativi al provvedimento che viene trasferito a nsc. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| PROVV_DOMAIN | VARCHAR2 (100 CHAR) NOT NULL | Nome logico del dominio |
| PROVV_CODCENTR | VARCHAR2 (100 CHAR) NOT NULL | Codice centrale del provvedimento |
| PROVV_NSC_CAT | VARCHAR2 (100 CHAR) NOT NULL | Categoria del provvedimento NSC |
| PROVV_NSC_DES_CAT | VARCHAR2 (240 CHAR) | Descrizione della categoria del provvedimento NSC |
| PROVV_NSC_NAT | VARCHAR2 (100 CHAR) NOT NULL | Natura del provvedimento NSC |
| PROVV_NSC_DES_NAT | VARCHAR2 (240 CHAR) | Descrizione della natura del provvedimento NSC |
| PROVV_SIES_OGGETTO | VARCHAR2 (100 CHAR) NOT NULL | Oggetto del provvedimento SIES |
| PROVV_SIES_DES_OGGETTO | VARCHAR2 (240 CHAR) | Descrizione dell’oggetto del provvedimento SIES |
| PROVV_SIES_MOTIVO | VARCHAR2 (100 CHAR) NOT NULL | Motivo del provvedimento SIES |
| PROVV_SIES_DES_MOTIVO | VARCHAR2 (240 CHAR) | Descrizione del motivo del provvedimento SIES |
| PROVV_SIES_ESITO | VARCHAR2 (100 CHAR) NOT NULL | Esito del provvedimento SIES |
| PROVV_SIES_DES_ESITO | VARCHAR2 (240 CHAR) | Descrizione dell’esito del provvedimento SIES |
| PROVV_VAL1 | VARCHAR2 (100 CHAR) | Prima valore |
| PROVV_VAL2 | VARCHAR2 (100 CHAR) | Secondo valore |
| PROVV_VAL3 | VARCHAR2 (100 CHAR). | Terzo valore |


# ISP_TIPOLOGIA_ISTANZA
tabella utilizzata per le statistiche relative alle istanze di un provvedimento. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ISTANZA | NUMBER NOT NULL | Chiave naturale della tabella. Legata a Sequence IST_SEQ. |
| COD_MOTIVO | VARCHAR2 (4 CHAR) | Codifica del Motivo dell'Istanza; Associata al Dominio MOTIVO_PROVVEDIMENTO di CG_REF_CODES. |
| NOTE | VARCHAR2 (2000 CHAR) | Campo libero per inserire tutte le informazioni sull'istanza |
| COGNOME_SOGGETTO_PRESENTANTE | VARCHAR2 (100 CHAR) | E' un campo libero in cui è indicato chi presenta l'istanza. Si può ipotizzare di impostare per default 'CONDANNATO' ma può assumere valori quali AVVOCATO PARENTE ecc. |
| NOME_SOGGETTO_PRESENTANTE | VARCHAR2 (100 CHAR) | E' un campo libero in cui è indicato il nome di chi presenta l'istanza. |
| DATA_PRESENTAZIONE | DATE NOT NULL | Data di presentazione dell'istanza. Tale data può essere utile per eventuali scadenzari |
| COD_ESITO | VARCHAR2 (4 CHAR) | Tipologia di esito dell'istanza. Deriva da dominio ESITO_PROVVEDIMENTO. Può assumere i seguenti valori: ACCOLTA RESPINTA |
| ANNO_REGISTRO | NUMBER | Anno del registro delle istanze. Tale registro che attualmente esiste potrebbe essere abolito in futuro. Viene mantenuto in vita per i processi di migrazione dati da RES |
| PROGR_REGISTRO | NUMBER | Progressivo nell'ambito dell'anno del registro delle istanze. Tale registro cha attualmente esiste potrebbe essere abolito in futuro. Viene mantenuto in vita per i processi di migrazione dati da RES |
| COD_TIPO_UFFICIO_DESTINATARIO | VARCHAR2 (6 CHAR) | Codifica del Tipo Ufficio del destinatario. Associato al Dominio TIPO_UFFICIO di CG_REF_CODES. |
| COD_LUOGO_DESTINATARIO | VARCHAR2 (6 CHAR) | Codice comune del Luogo del destinatario. |
| COD_UFFICIO_DESTINATARIO | VARCHAR2 (11 CHAR) | Codice dell'Ufficio destinatario. |
| COGNOME_AVVOCATO | VARCHAR2 (100 CHAR) | Cognome dell'avvocato. |
| NOME_AVVOCATO | VARCHAR2 (100 CHAR) | Nome dell'avvocato. |
| FORO_COMPETENZA | VARCHAR2 (50 CHAR) | Campo libero contenente i dati del foro di competenza. |
| ANNO_SENTENZA | NUMBER | Anno della sentenza. |
| NUMERO_SENTENZA | VARCHAR2 (6 CHAR) | Progressivo della sentenza. |
| DATA_SENTENZA | DATE | Data della sentenza. |
| DATA_IRREVOCABILITA | DATE | Data Irrevocabilità. |
| COD_TIPO_AUTORITA_EMITTENTE | VARCHAR2 (6 CHAR) | Codifica del Tipo Ufficio emittente. Associato al dominio TIPO_UFFICIO_EMITTENTE di CG_REF_CODES. |
| COD_LUOGO_EMITTENTE | VARCHAR2 (6 CHAR) | Codice del comune luogo di emissione Istanza. |
| COD_STATO_ISTANZA | VARCHAR2 (1 CHAR) | Codice dello stato dell’istante |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| SOG_ID_SOGGETTO | NUMBER NOT NULL | Identificativo del soggetto |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| CAM_ID_CAMPO_NOTE | NUMBER | Identificativo delle note |