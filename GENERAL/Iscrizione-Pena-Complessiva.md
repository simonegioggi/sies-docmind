---
uniqueName: iscrizione-pena-complessiva
displayName: "Iscrizione Pena Complessiva"
category: "GENERAL"
tags: []
---

# Iscrizione Pena Complessiva

> **File originale:** `MEV/SCHEDA_013/Docs/Test/Iscrizione Pena Complessiva.docx`  
> **Tipo:** DOCX

---

Iscrizione Pena Complessiva
La form di Iscrizione Pene Complessiva sarà aggiunta una nuova sezione per l’acquisizione dei dati relativi alle Pene Sostitutive delle Pene Detentive Brevi


in cui sarà possibile gestire le seguenti tipologie di pena


Per il caricamento delle due combo utilizziamo sempre il dominio “TIPO_SANZIONE_SOSTITUTIVA”, in cui oltre ad aggiungere le nuove pene sostitutive, sarà valorizzata la colonna RV_ABBREVIATION con le seguenti descrizioni ‘Sanzione Sostitutiva’ o 'Pena Sostitutiva'. Nel caricamento della combo Tipo della Sanzione Sostitutiva bisognerà rivedere l’attuale filtro aggiungendo la condizione ‘AND  ( RV_ABBREVIATION =  'Sanzione Sostitutiva' OR RV_ABBREVIATION IS NULL), mentre nel caricamento della combo Tipo bisognerà filtrare per RV_DOMAIN = 'TIPO_SANZIONE_SOSTITUTIVA' AND  ( RV_ABBREVIATION =  'Pena Sostitutiva' OR RV_ABBREVIATION IS NULL).

Di seguito loscript per il caricamento del Dominio:
DELETE CG_REF_CODES where RV_DOMAIN = 'TIPO_SANZIONE_SOSTITUTIVA';
INSERT INTO CG_REF_CODES (RV_DOMAIN, RV_LOW_VALUE, RV_HIGH_VALUE, RV_ABBREVIATION, RV_MEANING, RV_ALT2_VALUE, RV_ALT3_VALUE, RV_ALT4_VALUE, RV_ALT5_VALUE)
VALUES('TIPO_SANZIONE_SOSTITUTIVA', '-', 'A', NULL, '-', NULL, NULL, NULL, NULL);
INSERT INTO CG_REF_CODES (RV_DOMAIN, RV_LOW_VALUE, RV_HIGH_VALUE, RV_ABBREVIATION, RV_MEANING, RV_ALT2_VALUE, RV_ALT3_VALUE, RV_ALT4_VALUE, RV_ALT5_VALUE)
VALUES('TIPO_SANZIONE_SOSTITUTIVA', 'E', 'E', 'Sanzione Sostitutiva', 'Espulsione', NULL, NULL, NULL, NULL);
INSERT INTO CG_REF_CODES (RV_DOMAIN, RV_LOW_VALUE, RV_HIGH_VALUE, RV_ABBREVIATION, RV_MEANING, RV_ALT2_VALUE, RV_ALT3_VALUE, RV_ALT4_VALUE, RV_ALT5_VALUE)
VALUES('TIPO_SANZIONE_SOSTITUTIVA', 'L', 'C', 'Sanzione Sostitutiva', 'Liberta'' Controllata', NULL, NULL, NULL, NULL);
INSERT INTO CG_REF_CODES (RV_DOMAIN, RV_LOW_VALUE, RV_HIGH_VALUE, RV_ABBREVIATION, RV_MEANING, RV_ALT2_VALUE, RV_ALT3_VALUE, RV_ALT4_VALUE, RV_ALT5_VALUE)
VALUES('TIPO_SANZIONE_SOSTITUTIVA', 'P', 'D', 'Sanzione Sostitutiva', 'Pena Pecuniaria', NULL, NULL, NULL, NULL);
INSERT INTO CG_REF_CODES (RV_DOMAIN, RV_LOW_VALUE, RV_HIGH_VALUE, RV_ABBREVIATION, RV_MEANING, RV_ALT2_VALUE, RV_ALT3_VALUE, RV_ALT4_VALUE, RV_ALT5_VALUE)
VALUES('TIPO_SANZIONE_SOSTITUTIVA', 'S', 'B', 'Sanzione Sostitutiva', 'Semidetenzione', NULL, NULL, NULL, NULL);
INSERT INTO CG_REF_CODES (RV_DOMAIN, RV_LOW_VALUE, RV_HIGH_VALUE, RV_ABBREVIATION, RV_MEANING, RV_ALT2_VALUE, RV_ALT3_VALUE, RV_ALT4_VALUE, RV_ALT5_VALUE)
VALUES('TIPO_SANZIONE_SOSTITUTIVA', 'U', 'F', 'Pena Sostitutiva', 'Lavoro pubblica utilita'' sostitutivo', NULL, NULL, NULL, NULL);
INSERT INTO CG_REF_CODES (RV_DOMAIN, RV_LOW_VALUE, RV_HIGH_VALUE, RV_ABBREVIATION, RV_MEANING, RV_ALT2_VALUE, RV_ALT3_VALUE, RV_ALT4_VALUE, RV_ALT5_VALUE)
VALUES('TIPO_SANZIONE_SOSTITUTIVA', 'T', 'G', 'Pena Sostitutiva', 'Semiliberta'' sostitutiva', NULL, NULL, NULL, NULL);
INSERT INTO CG_REF_CODES (RV_DOMAIN, RV_LOW_VALUE, RV_HIGH_VALUE, RV_ABBREVIATION, RV_MEANING, RV_ALT2_VALUE, RV_ALT3_VALUE, RV_ALT4_VALUE, RV_ALT5_VALUE)
VALUES('TIPO_SANZIONE_SOSTITUTIVA', 'V', 'H', 'Pena Sostitutiva', 'Detenzione Domiciliare sostitutiva', NULL, NULL, NULL, NULL);
INSERT INTO CG_REF_CODES (RV_DOMAIN, RV_LOW_VALUE, RV_HIGH_VALUE, RV_ABBREVIATION, RV_MEANING, RV_ALT2_VALUE, RV_ALT3_VALUE, RV_ALT4_VALUE, RV_ALT5_VALUE)
VALUES('TIPO_SANZIONE_SOSTITUTIVA', 'Z', 'I', 'Pena Sostitutiva', 'Pena Pecuniaria sostitutiva', NULL, NULL, NULL, NULL);
COMMIT;

La sezione Sanzione Sostituiva è alternativa alla sezione Pene Sostitutive delle Pene Detentive Brevi. La nuova sezione sarà riportata anche nelle form di Dettaglio, quando valorizzata, e Modifica.

La tabella in cui inserire i dati della Sanzione Sostitutive o delle Pene Sostitutive è sempre SANZIONE_SOSTITUTIVA.
Nella form di Dettaglio Pena Complessiva, nella combo box delle azioni saranno aggiunte due nuove voci “Modalità Pagamento Pena Pecuniaria”, “Civilmente Obbligato Pena Pecuniaria”