---
uniqueName: posizionigiuridichemappainterfacciadb
displayName: "Posizioni Giuridiche mappa interfaccia db"
category: "GENERAL"
tags: []
---

# Posizioni_Giuridiche_mappa_interfaccia_db

> **File originale:** `MEV/Mev10/Posizioni_Giuridiche_mappa_interfaccia_db.xls`  
> **Tipo:** XLS

---

## Pososizione Giuridica

|  |  |  | Mask iniziale | Mask L | Mask L1 | Mask L2 | Mask L3 | Mask EI | Mask EA |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| POSIZIONE_GIURIDICA |  |  |  |  |  |  |  |  |  |
|  | ID_POSIZIONE_GIURIDICA |  | key | key | key | key | key | key | key |
|  | COD_POSIZIONE_GIURIDICA |  | 1. Posizione Giuridica | 1. Posizione Giuridica | 1. Posizione Giuridica | 1. Posizione Giuridica | 1. Posizione Giuridica | 1. Posizione Giuridica | 1. Posizione Giuridica |
|  | DATA_INIZIO |  | 2. Data di Decorrenza |  |  |  |  | 2. Data di Decorrenza Pena | 2. Data di Decorrenza Pena |
|  | DATA_FINE |  |  |  |  |  |  |  |  |
|  | COD_POSIZIONE_PROCESSUALE |  | '-' | '-' | '-' | '-' | '-' | '-' | '-' |
|  | NOTE |  |  |  |  |  |  |  |  |
|  | LUOGO_PROVA_AFFIDAMENTO |  | 5. Luogo Prova Affidamento | 3. Note | 10. Note | 16. Note | 19. Note | 4. Note | 7. Note |
|  | LUOGO_LAVORO_SEMILIBERTA |  | 6. Luogo Lavoro Semilibertà | 3. Note | 10. Note | 16. Note | 19. Note | 4. Note | 7. Note |
|  | FAS_SIE_ID_FASCICOLO_SIEP |  | idFascicoloSiep | idFascicoloSiep | idFascicoloSiep | idFascicoloSiep | idFascicoloSiep | idFascicoloSiep | idFascicoloSiep |
|  | ID_EVENTO_RIFERIMENTO |  |  |  |  |  |  |  |  |
|  | ALT_CAU_ID_ALTRA_CAUSA |  | for-key |  | for-key | for-key | for-key |  |  |
|  | LUOGO_ESPIAZIONE |  |  |  |  |  |  |  | 3. Luogo di Espiazione |
|  | AUTORITA_COMPETENTE |  |  |  |  |  |  |  | 4. Autorità Competente per territorio |
|  | AUTORITA_COMPETENTE_SEDE |  |  |  |  |  |  |  | 5. Sede |
|  | AUTORITA_COMPETENTE_INDIRIZZO |  |  |  |  |  |  |  | 6. Indirizzo |
|  | COD_MASCHERA |  |  | 'L' | 'L1' | 'L2' | 'L3' | 'EI' | 'EA' |
| FASCICOLO_SIEP |  |  |  |  |  |  |  |  |  |
|  | … |  |  |  |  |  |  |  |  |
|  | FLAG_ALTRA_CAUSA |  | 7. Detenuto per altra causa | 2.Detenuto altra causa ('N') | 2.Detenuto altra causa ('S') | 2.Detenuto altra causa ('S') | 2.Detenuto altra causa ('S') | (null) | (null) |
|  | COD_TIPO_POS_LIBERO |  | '-' | '-' | '-' | '-' | '-' | '-' | '-' |
|  | … |  |  |  |  |  |  |  |  |
| ALTRA_CAUSA |  |  |  |  |  |  |  |  |  |
|  | ID_ALTRA_CAUSA |  | key |  | key | key | key |  |  |
|  | ANNO |  | 13. Anno/Numero Tit. Esec. |  | 5. Anno SIEP |  |  |  |  |
|  | NUMERO |  | 13. Anno/Numero Tit. Esec. |  | 6. Numero SIEP |  |  |  |  |
|  | DATA |  | 14. Data |  |  |  |  |  |  |
|  | COD_LUOGO |  | 16. Luogo |  | 8. Luogo Emittente |  |  |  |  |
|  | COD_AUTORITA |  | 15. Autorità |  | 7. Autorità Emittente |  |  |  |  |
|  | DATA_DECORRENZA |  | 9. Data di Decorrenza |  |  |  |  |  |  |
|  | DATA_SCADENZA |  | 10. Data di Scadenza |  | 9.Data Scadenza Altra Pena |  |  |  |  |
|  | COD_TIPO_POS_GIURIDICA |  | 8. Tipo Misura |  | 3. Tipo Misura |  |  |  |  |
|  | ALTRO_LUOGO |  | 12. Altro Luogo Detenzione |  |  |  |  |  |  |
|  | NOTE |  |  |  |  |  |  |  |  |
|  | FAS_SIE_ID_FASCICOLO_SIEP |  | idFascicoloSiep |  | idFascicoloSiep | idFascicoloSiep | idFascicoloSiep |  |  |
|  | IST_DET_ID_ISTITUTO_DETENZIONE |  | 11. Istituto |  | 4. Istituto di Detenzione | 15. Istituto di Detenzione |  |  |  |
| MISURA_CAUTELARE |  |  |  |  |  |  |  |  |  |
|  | ID_MISURA_CAUTELARE |  |  |  |  | key | key |  |  |
|  | COD_TIPO_MISURA |  |  |  |  | 14.Tipo misura | 14.Tipo misura |  |  |
|  | DATA_INIZIO |  |  |  |  |  |  |  |  |
|  | DATA_FINE |  |  |  |  |  |  |  |  |
|  | NUM_ANNI |  |  |  |  |  |  |  |  |
|  | NUM_MESI |  |  |  |  |  |  |  |  |
|  | NUM_GIORNI |  |  |  |  |  |  |  |  |
|  | FLAG_COMPUTABILE |  |  |  |  |  |  |  |  |
|  | COD_MOTIVO_NON_COMPUTABILE |  |  |  |  |  |  |  |  |
|  | ALTRO_LUOGO_DETENZIONE |  |  |  |  |  | 15. Luogo di Espiazione |  |  |
|  | COD_TIPO_UFFICIO_RIFER |  |  |  |  |  |  |  |  |
|  | COD_LUOGO_UFFICIO_RIFER |  |  |  |  |  |  |  |  |
|  | DATA_FUNGIBILITA |  |  |  |  |  |  |  |  |
|  | NUM_RIFER |  |  |  |  |  |  |  |  |
|  | NOTE |  |  |  |  |  |  |  |  |
|  | FAS_SIE_ID_FASCICOLO_SIEP |  |  |  |  |  |  |  |  |
|  | EVE_ID_EVENTO |  |  |  |  |  |  |  |  |
|  | IST_DET_ID_ISTITUTO_DETENZIONE |  |  |  |  |  |  |  |  |
|  | ANNO_FASC_BDMC |  |  |  |  | 3.Anno BDMC | 3. Anno B.D.M.C. |  |  |
|  | NUME_FASC_BDMC |  |  |  |  | 4.Numero BDMC | 4. Numero B.D.M.C. |  |  |
|  | ANNO_RGNR |  |  |  |  | 7.Anno RGNR | 7. Anno R.G.N.R. |  |  |
|  | NUMERO_RGNR |  |  |  |  | 8.Numero RGNR | 8. Numero R.G.N.R. |  |  |
|  | ANNO_REG_GEN |  |  |  |  | 9.Anno Reg. Gen. | 9. Anno Reg. Gen. |  |  |
|  | NUMERO_REG_GEN |  |  |  |  | 10.Numero Reg. Gen. | 10. Numero Reg. Gen. |  |  |
|  | TIPO_UFFICIO_REG_GEN |  |  |  |  | 11.Tipo Reg. Gen. | 11. Tipo ufficio Reg. Gen. |  |  |
|  | AUTORITA_EMITTENTE |  |  |  |  | 12.Autorità emittente | 12. Autorità Emittente |  |  |
|  | AUTORITA_EMITTENTE_LUOGO |  |  |  |  | 13.Luogo Emittente | 13. Luogo Emittente |  |  |
|  | AUTORITA_COMPETENTE |  |  |  |  |  | 16. Autorità Competente per territorio |  |  |
|  | AUTORITA_COMPETENTE_SEDE |  |  |  |  |  | 17. Autorità Competente per territorio - Sede |  |  |
|  | AUTORITA_COMPETENTE_INDIRIZZO |  |  |  |  |  | 18. Autorità Competente per territorio - Indirizzo |  |  |
|  | ANNO_RIFER |  |  |  |  |  |  |  |  |
|  | CODICE_UFFICIO_PM_SEDE |  |  |  |  | 5.Tipo ufficio PM
6.Sede PM | 5.Tipo ufficio PM
6.Sede PM |  |  |
|  | POS_GIU_ID_POSIZIONE_GIURIDICA |  |  |  |  | for-key | for-key |  |  |
| LUOGO_DETENZIONE |  |  |  |  |  |  |  |  |  |
|  | ID_LUOGO_DETENZIONE |  | key | key | key | key | key | key | key |
|  | NOTE |  |  |  |  |  |  |  |  |
|  | DATA_INIZIO_DETENZIONE |  | sysdate |  |  |  |  |  |  |
|  | DATA_FINE_DETENZIONE |  |  |  |  |  |  |  |  |
|  | FAS_SIE_ID_FASCICOLO_SIEP |  | idFascicoloSiep | idFascicoloSiep | idFascicoloSiep | idFascicoloSiep | idFascicoloSiep | idFascicoloSiep | idFascicoloSiep |
|  | FAS_SIU_ID_FASCICOLO_SIUS |  | idFascicoloSius | idFascicoloSius | idFascicoloSius | idFascicoloSius | idFascicoloSius | idFascicoloSius | idFascicoloSius |
|  | POS_GIU_ID_POSIZIONE_GIURIDICA |  | for-key | for-key | for-key | for-key | for-key | for-key | for-key |
|  | ALTRO_LUOGO |  | 4. Altro Luogo Detenzione |  |  |  |  |  |  |
|  | IST_DET_ID_ISTITUTO_DETENZIONE |  | 3. Istituto |  |  |  |  | 3. Istituto |  |

## legenda

| Tipo Maschera | Cod Maschera |
| --- | --- |
| Posizione Libero | L |
| Libero - Definitiva in istituto di detenzione | L1 |
| Libero - Misura cautelare in istituto detenzione | L2 |
| Libero - Misura cautelare in altro luogo | L3 |
| Espiazione Pena in istituto di detenzione | EI |
| Espiazione Pena in altro luogo | EA |