---
uniqueName: cgrefcodesdizionario-2
displayName: "cg ref codes dizionario"
category: "GENERAL"
tags: []
---

# Dizionario dei Domini CG_REF_CODES — SIES

## Sommario

| Metadato | Valore |
|---|---|
| Totale domini | 206 |
| Nomi dominio distinti | 205 (la lista sorgente duplica `DETTAGLIO_MOTIVO`) |
| Totale valori stimati | ~9.404 |
| Schema Oracle | SIESTO |
| Tabella | CG_REF_CODES |
| Progetto Java | siesWeb (package `siap.*`) |
| Data analisi | 2026-07-02 |
| Domini senza match letterale nella batch search | 60 |

## Pattern di utilizzo nel codice Java

La tabella `SIESTO.CG_REF_CODES` è il dizionario centrale di lookup del sistema SIES. Dalla FASE 1 emergono tre pattern dominanti di accesso:

1. **Lookup generico via `DecodificheDAO` / `IDecodifiche`**: il DAO mappa `CG_REF_CODES` su `RV_LOW_VALUE`, `RV_MEANING`, `RV_DOMAIN`, `RV_ABBREVIATION`, `RV_HIGH_VALUE` e campi ausiliari `RV_ALT2_VALUE..RV_ALT5_VALUE`, costruendo la `WHERE` a partire dal dominio e da eventuali filtri. Esempio: `siap/sico/decodifiche/dao/DecodificheDAO.java`.
2. **Popolamento di combo e filtri nelle action/controller**: il codice imposta il dominio con `DecodificheModel#setContesto(...)` e recupera la collection con `ExRicercaDecodifiche(...)`. Questo è il pattern più frequente nelle maschere. Esempi: `DecodificheManagerBean`, `DecodificheManagerModel`, `ActLoadTrasferisciNuovaIstanza`.
3. **Join SQL dirette per decorare le entità di business**: molte `SqlDAO` fanno join su `CG_REF_CODES` per trasformare codici in descrizioni leggibili (`NAZIONE`, `PROVINCIA`, `TIPO_RICORSO`, `TENORE_DECISIONE_RICORSO`, `TIPO_UFFICIO`, ecc.). Esempi: `RegeSoggettoSqlDAO`, `ImpugnazioneSqlDAO`, `RegeResidenzaSqlDAO`.

La grep suggerita per `getCgRefCodes|getRefCodes|cgRefCode|CgRefCode` non restituisce un pattern applicativo significativo: il progetto non usa helper con quel naming, ma concentra l’accesso su `DecodificheModel`, `IDecodifiche` ed SQL esplicito.

> **Nota metodologica**: la batch search della FASE 2 conta solo le occorrenze letterali del dominio in **doppie virgolette** (`"DOMINIO"`). I join SQL scritti con **apici singoli** (`RV_DOMAIN = 'DOMINIO'`) sono quindi rilevati qualitativamente nella FASE 1, ma non sempre incrementano il conteggio numerico del catalogo alfabetico.

### Esempi rappresentativi

```java
// Pattern 1 - DAO generico su CG_REF_CODES
setTable("CG_REF_CODES");
setField("RV_LOW_VALUE", STRING);
setField("RV_MEANING", STRING);
setField("RV_DOMAIN", STRING);
lCondizione = " RV_DOMAIN = '" + aModel.getContesto() + "'";
```

```java
// Pattern 2 - popolamento collection per combo box e filtri
DecodificheModel lModel = new DecodificheModel();
lModel.setContesto("TIPO_UFFICIO");
Collection uffici = lDecodifiche.ExRicercaDecodifiche(lModel);
```

```java
// Pattern 3 - join SQL diretta per ottenere la descrizione
FROM IMPUGNAZIONE IMP
JOIN CG_REF_CODES TIPO_IMPUGNAZIONE
  ON (TIPO_IMPUGNAZIONE.RV_DOMAIN = 'TIPO_RICORSO' AND TIPO_IMPUGNAZIONE.RV_LOW_VALUE = IMP.COD_TIPO_IMPUGNAZIONE)
JOIN CG_REF_CODES TENORE_DECISIONE
  ON (TENORE_DECISIONE.RV_DOMAIN = 'TENORE_DECISIONE_RICORSO' AND TENORE_DECISIONE.RV_LOW_VALUE = IMP.COD_TENORE_DECISIONE)
```

---

## Catalogo per categoria

### Categoria: FLAG (FLAG_*) (10 voci)

| Dominio | N° valori | Occorrenze batch | File Java principali |
|---|---:|---:|---|
| `FLAG_CONCESSO` | 4 | 6 | `LibAnticipataCumuloDAO`, `LibAnticipataCumuloSqlDAO`, `PeriodoLibanticipataSqlDAO`, `LicenzaLibanticipataSqlDAO`, `PeriodoLibanticipataDAO` |
| `FLAG_ERGASTOLO` | 3 | 14 | `PenaResiduaDettaglioSqlDAO`, `PenaPrecedenteSqlDAO`, `PenaResiduaDAO`, `PenaResiduaSqlDAO`, `PenaResiduaPerStatoEsecuzioneSqlDAO` |
| `FLAG_ESITO_TENORE` | 4 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `FLAG_ISTANZA` | 3 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `FLAG_ISTANZA_PD` | 2 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `FLAG_PIU_MENO` | 3 | 18 | `EventoVerbaleSqlDAO`, `ComputiCumuloSqlDAO`, `ComputiCumuloDAO`, `IstanzaSqlDAO`, `ProvvedimentoSqlDAO` |
| `FLAG_SCARCERATO_SCARCERARE` | 3 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `FLAG_SI_NO` | 3 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `FLAG_STATO` | 4 | 50 | `ReatoCumuloDAO`, `LibAnticipataCumuloDAO`, `PeriodoLibAntCumuloDAO`, `BeneficioCumuloDAO`, `ComputiCumuloSqlDAO` |
| `SOSPENDE_E_TRASMETTE_GLI_ATTI_AL_TDS` | 1 | 0 | — (nessuna occorrenza letterale con la batch search) |

### Categoria: ESITI (ESITO_* / TENORE_*) (14 voci)

| Dominio | N° valori | Occorrenze batch | File Java principali |
|---|---:|---:|---|
| `ESITO_ATTIVITA_SIEPE` | 2 | 1 | `DecodificheManagerModel` |
| `ESITO_ISTANZA` | 6 | 1 | `DecodificheManagerModel` |
| `ESITO_NOTIFICA` | 4 | 1 | `DecodificheManagerBean` |
| `ESITO_PERMESSO_LICENZA` | 3 | 1 | `DecodificheManagerModel` |
| `ESITO_PROVVEDIMENTO` | 374 | 4 | `ActLoadModificaIstanza`, `ActLoadModificaIstanzaAnnTrasmissione`, `DecodificheManagerBean`, `DecodificheManagerModel` |
| `ESITO_PROVVEDIMENTO_SIGE` | 81 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `ESITO_RICHIESTA` | 5 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `ESITO_SIEP` | 480 | 1 | `DecodificheManagerBean` |
| `ESITO_TENORE` | 1237 | 1 | `DecodificheManagerBean` |
| `ESITO_TENORE_SIGE` | 392 | 1 | `DecodificheManagerModel` |
| `PESO_ESITO_TENORE` | 331 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TENORE_DECISIONE_RICORSO` | 14 | 1 | `DecodificheManagerBean` |
| `TENORE_DECISIONE_RICORSO_SIGE` | 14 | 1 | `DecodificheManagerBean` |
| `TENORE_ORDINANZA_PA` | 6 | 6 | `ActLoadInserisciPenaAccessoria`, `ActLoadInserisciEsecuzionePA`, `ActLoadComunicazione`, `ActLoadInserisciPenaAccessoria`, `ActLoadInserisciComunicazione` |

### Categoria: STATI (STATO_*) (13 voci)

| Dominio | N° valori | Occorrenze batch | File Java principali |
|---|---:|---:|---|
| `STATO_AVVOCATO` | 5 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `STATO_FASCICOLO` | 23 | 2 | `FascicoloSiepSoggettoSqlDAO`, `DecodificheManagerBean` |
| `STATO_FLAG_RINVIATA` | 4 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `STATO_ISTANZA` | 5 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `STATO_ISTRUTTORIA_CUMULO` | 4 | 1 | `DecodificheManagerModel` |
| `STATO_LIBERTATIS` | 3 | 1 | `DecodificheManagerBean` |
| `STATO_MISURA_CUMULO` | 4 | 1 | `DecodificheManagerBean` |
| `STATO_NUOVA_ISTANZA` | 9 | 1 | `DecodificheManagerModel` |
| `STATO_PAGAMENTO` | 3 | 3 | `BollettinoPagopaDAO`, `BollettinoPagopaSqlDAO`, `ScadenzarioSoggettoSqlDAO` |
| `STATO_PERMESSO` | 5 | 1 | `DecodificheManagerBean` |
| `STATO_PROCEDIMENTO` | 473 | 6 | `StatoProcedimentoDAO`, `FascicoloSiepOnViewSqlDAO`, `EventoSimeoneSqlDAO`, `DecodificheManagerBean`, `ProcAggregatiProcuraMittenteSqlDAO` |
| `STATO_PROC_GENERICO` | 50 | 1 | `ActUploadProvvedimentoGenerico` |
| `STATO_RICEZIONE_SIEPE` | 5 | 1 | `DecodificheManagerModel` |

### Categoria: MOTIVI (MOTIVO_*) (15 voci)

| Dominio | N° valori | Occorrenze batch | File Java principali |
|---|---:|---:|---|
| `DETTAGLIO_MOTIVO` | 49 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `DETTAGLIO_MOTIVO (voce duplicata nella lista sorgente)` | 19 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `MOTIVAZIONE_NON_INVIO_FC` | 2 | 1 | `DecodificheManagerBean` |
| `MOTIVO_ARCHIVIAZIONE` | 15 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `MOTIVO_DESIGNAZIONE` | 8 | 1 | `DecodificheManagerBean` |
| `MOTIVO_DETENZIONE` | 2 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `MOTIVO_INAMMISSIBILITA` | 57 | 1 | `DecodificheController` |
| `MOTIVO_INAMMISSIBILITA_SIGE` | 9 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `MOTIVO_INTSOSP` | 18 | 1 | `DecodificheManagerBean` |
| `MOTIVO_NON_COMPUTABILE` | 7 | 1 | `DecodificheManagerBean` |
| `MOTIVO_PERIODO_EMS` | 3 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `MOTIVO_PERIODO_ESS` | 3 | 1 | `DecodificheManagerBean` |
| `MOTIVO_PROVVEDIMENTO` | 1659 | 35 | `ActLoadInserisciRevocaMisuraAlternativaCumulo`, `ActLoadInserisciEspulsioneCumulo`, `ActLoadInserisciSospMisuraAlternativaCumulo`, `ActLoadInserisciSospEsecuzionePenaCumulo`, `ActDettaglioRichiestaGERevocaBenefici` |
| `MOTIVO_SOSPENSIONE_CUMULO` | 1 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `REVOCA_DECSOSP` | 3 | 1 | `DecodificheManagerBean` |

### Categoria: TIPI - Uffici (TIPO_UFFICIO*) (17 voci)

| Dominio | N° valori | Occorrenze batch | File Java principali |
|---|---:|---:|---|
| `AUTORITA_COMPETENTE` | 9 | 7 | `PosizioneGiuridicaSqlDAO`, `PosizioneGiuridicaDAO`, `MisuraCautelareCumuloDAO`, `MisuraCautelareCumuloSqlDAO`, `MisuraCautelareDAO` |
| `AUTORITA_CUMULO` | 9 | 1 | `DecodificheManagerBean` |
| `AUTORITA_NOTIFICA` | 22 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `FIRMA_UFFICIO` | 5 | 1 | `DecodificheManagerBean` |
| `TIPO_AUTORITA` | 121 | 6 | `MisuraSicurezzaSqlDAO`, `DecodificheManagerBean`, `DecodificheManagerCore`, `ActLoadInserisciEsitoImpugnazioneSige`, `ActLoadInserisciRichiestaRemissioneDebito` |
| `TIPO_AUTORITA_VERBALE_ARRESTO` | 6 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_UFFICIO` | 59 | 24 | `IstruttoriaController`, `ActLoadTrasferisciNuovaIstanza`, `FascicoloSiepSqlDAO`, `ActLoadListaProvvedimentiTrasmessi`, `ActLoadTrasferisciProvvedimentoL78del2013` |
| `TIPO_UFFICIO_CUMULO` | 31 | 2 | `DecodificheManagerBean`, `ActLoadInserisciDataDepositoDecreto` |
| `TIPO_UFFICIO_DEFI` | 31 | 1 | `DecodificheManagerBean` |
| `TIPO_UFFICIO_EMITTENTE` | 27 | 8 | `DatiFinaliCumuloController`, `ActLoadDettaglioAnnotazioneRevoca`, `ActLoadDettaglioRichiestaRevoca`, `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadRevoche` |
| `TIPO_UFFICIO_GE` | 12 | 2 | `DecodificheManagerBean`, `DecodificheManagerCore` |
| `TIPO_UFFICIO_PM` | 9 | 1 | `DecodificheManagerBean` |
| `TIPO_UFFICIO_REGE` | 5 | 1 | `RegeDecodificheManager` |
| `TIPO_UFFICIO_RPA` | 31 | 1 | `DecodificheManagerBean` |
| `TIPO_UFFICIO_SCARCERAZIONE` | 5 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_UFFICIO_SOSP` | 27 | 3 | `ActLoadInserisciSospensioneEsecPenaDispPm`, `DecodificheManagerBean`, `DecodificheController` |
| `UFFICIO_LOGIN` | 23 | 1 | `DecodificheManagerBean` |

### Categoria: TIPI - Provvedimenti (TIPO_PROVVEDIMENTO*) (15 voci)

| Dominio | N° valori | Occorrenze batch | File Java principali |
|---|---:|---:|---|
| `CONTENUTO_DECRETO` | 7 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `DATI_PROVVEDIMENTO_SIGE` | 53 | 1 | `DatiProvvedimentoSigeDAO` |
| `NOME_PROVVEDIMENTO` | 170 | 1 | `NomeProvvedimentoDAO` |
| `TIPO_DECISIONE` | 1 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_DECISIONE_CASSAZIONE` | 9 | 3 | `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadSentenza`, `DecodificheManagerBean` |
| `TIPO_DECISIONE_SORVEGLIANZA` | 3 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_DECRETO` | 51 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_ORDINANZA` | 57 | 1 | `DecodificheManagerBean` |
| `TIPO_PROVVEDIMENTO` | 57 | 6 | `MisuraSicurezzaSqlDAO`, `ActNscToSiesLoadCircostanze`, `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadSentenza`, `DecodificheManagerBean` |
| `TIPO_PROVVEDIMENTO_ARC` | 3 | 1 | `DecodificheManagerBean` |
| `TIPO_PROVVEDIMENTO_RIF` | 3 | 1 | `DecodificheManagerBean` |
| `TIPO_PROVVEDIMENTO_RIF_P` | 5 | 1 | `DecodificheManagerBean` |
| `TIPO_PROVVEDIMENTO_RIF_PG` | 3 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_PROVVEDIMENTO_SIGE` | 25 | 1 | `DecodificheManagerModel` |
| `TIPO_SENTENZA` | 5 | 1 | `DecodificheManagerBean` |

### Categoria: TIPI - Sanzioni (TIPO_SANZIONE*) (11 voci)

| Dominio | N° valori | Occorrenze batch | File Java principali |
|---|---:|---:|---|
| `CAUSALE_COMPUTO` | 14 | 1 | `DecodificheManagerBean` |
| `NATURA_PENA` | 1 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_FUNGIBILITA` | 4 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_PENA_ACCESSORIA` | 106 | 3 | `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadPeneAccessorie`, `DecodificheManagerBean` |
| `TIPO_PENA_DETENTIVA` | 5 | 4 | `ActNscToSiesLoadReato`, `ActNscToSiesLoadPenaComplessiva`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean` |
| `TIPO_SANZIONE` | 3 | 3 | `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadSostituzionePene`, `DecodificheManagerBean` |
| `TIPO_SANZIONE_AMMINISTRATIVA` | 14 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_SANZIONE_CONVERTITA` | 7 | 1 | `DecodificheManagerBean` |
| `TIPO_SANZIONE_SOSTITUTIVA` | 9 | 1 | `DecodificheManagerBean` |
| `TIPO_SANZIONE_SOSTITUTIVA_LPU` | 3 | 1 | `DecodificheManagerBean` |
| `TIPO_ULTERIORE_SANZIONE` | 13 | 0 | — (nessuna occorrenza letterale con la batch search) |

### Categoria: TIPI - Registri e Atti (18 voci)

| Dominio | N° valori | Occorrenze batch | File Java principali |
|---|---:|---:|---|
| `ATTI_ARCHIVIO` | 2 | 1 | `DecodificheManagerModel` |
| `DESTINATARIO_DEPOSITO` | 10 | 1 | `DecodificheManagerBean` |
| `DESTINATARIO_DEPOSITO_MINORENNI` | 4 | 1 | `DecodificheManagerBean` |
| `DESTINATARIO_DEPOSITO_SIGE` | 2 | 1 | `DecodificheManagerModel` |
| `MITTENTE_ATTO` | 36 | 2 | `DecodificheManagerBean`, `ProcAggregatiProcuraMittenteSqlDAO` |
| `MITTENTE_ISTANZA` | 71 | 1 | `DecodificheManagerModel` |
| `TIPO_ATTO` | 14 | 6 | `DecodificheManagerBean`, `ActRicercaAttiVistiPerTipo`, `ActRicercaAttiPerTipoeDate`, `ActRicercaAttiPerSoggetto`, `ActRicercaAttiPerSIEPeSIUS` |
| `TIPO_ATTO_SIGE` | 5 | 1 | `DecodificheManagerModel` |
| `TIPO_CERTIFICATO` | 10 | 2 | `ActLoadInserisciCertificatiComune`, `ActInserisciCertificatiComune` |
| `TIPO_DOCUMENTO_ALLEGATO` | 5 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_EMITTENTE` | 6 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_MITTENTE` | 5 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_NOTIFICA` | 18 | 4 | `ActInserisciRichRiesamePericoloSociale`, `DecodificheManagerBean`, `NotificheSiesDAO`, `NotificheSiesSqlDAO` |
| `TIPO_REGISTRO` | 26 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_REGISTRO_ORDINANZA` | 4 | 1 | `DecodificheManagerBean` |
| `TIPO_REG_GEN` | 8 | 7 | `DecretoOrdinanzaSiepSqlDAO`, `DecretoOrdinanzaSiepDAO`, `ContinuazioneCumuloDAO`, `TitoloCumulatoDAO`, `ContinuazioneCumuloSqlDAO` |
| `TIPO_TRASMISSIONE` | 3 | 5 | `TrasmissioniSqlDAO`, `TrasmissioniDAO`, `DecodificheManagerBean`, `StatoPrenotazioniBdmcDAO`, `StatoPrenotazioniBdmcSqlDAO` |
| `TIPO_VERBALE` | 9 | 0 | — (nessuna occorrenza letterale con la batch search) |

### Categoria: TIPI - Procedure e Riti (24 voci)

| Dominio | N° valori | Occorrenze batch | File Java principali |
|---|---:|---:|---|
| `RICERCA_EMA` | 28 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_CONTINUAZIONE` | 5 | 3 | `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadContinuazione`, `DecodificheManagerBean` |
| `TIPO_CONTROLLO_ESECUZIONE` | 3 | 7 | `DepositoDecretoSqlDAO`, `DepositoDecretoDAO`, `EveFasGepSogSenSqlDAO`, `EveFasGepSogDecSqlDAO`, `EveFasGepSogOrdSqlDAO` |
| `TIPO_CUMULO` | 1 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_DEFINIZIONE` | 19 | 8 | `PosizioneMaterialeFascSqlDAO`, `DecodificheManagerModel`, `ActLoadDefinizioneProcedimento`, `FascicoloSiepeDAO`, `FascicoloSiepeSqlDAO` |
| `TIPO_DEFINIZIONE_SIEPE` | 3 | 1 | `DecodificheManagerModel` |
| `TIPO_DURATA` | 3 | 1 | `DecodificheManagerBean` |
| `TIPO_ELENCO_RICORSI` | 2 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_EVENTO` | 23 | 1 | `DecodificheManagerBean` |
| `TIPO_EVENTO_PERMESSO_LICENZA` | 8 | 1 | `DecodificheManagerModel` |
| `TIPO_GE` | 6 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_INTSOSP` | 7 | 1 | `DecodificheManagerBean` |
| `TIPO_PRESCRIZIONE` | 39 | 1 | `DecodificheManagerModel` |
| `TIPO_RICHIESTA_CUMULO` | 3 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_RICHIESTA_GE` | 9 | 4 | `ActPreLoadRichiestaGE`, `ActLoadInserisciRichiestaGE`, `ActLoadRichiestaGE`, `ActRichiestaGE` |
| `TIPO_RICHIESTA_SIEPE` | 11 | 1 | `DecodificheManagerModel` |
| `TIPO_RICORSO` | 4 | 1 | `DecodificheManagerBean` |
| `TIPO_RICORSO_SIGE` | 3 | 1 | `DecodificheManagerBean` |
| `TIPO_RITO` | 6 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_RITO_SENTENZA` | 3 | 1 | `DecodificheManagerBean` |
| `TIPO_SCADENZARIO` | 28 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_SOSPENSIONE` | 3 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_SOSP_SUBORDINATA` | 9 | 3 | `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadBenefici`, `DecodificheManagerBean` |
| `TIPO_VISUALIZZAZIONE` | 6 | 0 | — (nessuna occorrenza letterale con la batch search) |

### Categoria: TIPI - Soggetti e Ruoli (14 voci)

| Dominio | N° valori | Occorrenze batch | File Java principali |
|---|---:|---:|---|
| `ATTIVITA_AVVOCATO` | 5 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `FORO_AVVOCATI` | 167 | 1 | `DecodificheManagerModel` |
| `POSIZIONE_PROCESSUALE` | 4 | 1 | `DecodificheManagerBean` |
| `RICHIEDENTE` | 1 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `RUOLO_GIUDICE_POPOLARE` | 3 | 1 | `DecodificheManagerModel` |
| `RUOLO_MAGISTRATO` | 4 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `SOGGETTO_IMPUGNANTE` | 9 | 6 | `DecodificheManagerBean`, `FascicoloSigeSqlDAO`, `ImpugnazioneSigeDAO`, `ImpugnazioneSigeSqlDAO`, `ImpugnazioneDAO` |
| `SOGGETTO_IMPUGNANTE_SIGE` | 7 | 1 | `DecodificheManagerBean` |
| `TIPO_AVVOCATO` | 4 | 3 | `NuovaIstanzaSqlDAO`, `NuovaIstanzaDAO`, `DecodificheManagerBean` |
| `TIPO_CURATORE` | 3 | 1 | `DecodificheManagerModel` |
| `TIPO_FUNZIONE` | 15 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_RICHIEDENTE_SIEPE` | 5 | 1 | `DecodificheManagerModel` |
| `TIPO_RICHIEDENTE_SIGE` | 52 | 1 | `DecodificheManagerModel` |
| `TIPO_TUTORE` | 3 | 1 | `DecodificheManagerBean` |

### Categoria: TIPI - Misure e Benefici (15 voci)

| Dominio | N° valori | Occorrenze batch | File Java principali |
|---|---:|---:|---|
| `INSERIMENTO_MA` | 39 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `INSERIMENTO_SS` | 5 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `NATURA_BENEFICIO` | 3 | 1 | `DecodificheManagerBean` |
| `NATURA_MISURA_SICUREZZA` | 4 | 1 | `DecodificheManagerBean` |
| `POSIZIONE_GIURIDICA_BENEFICI` | 85 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `SOTTOTIPO_BENEFICIO` | 11 | 1 | `DecodificheManagerBean` |
| `TIPO_ATTIVITA_SIEPE` | 46 | 1 | `DecodificheManagerModel` |
| `TIPO_BENEFICIO` | 9 | 3 | `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadBenefici`, `DecodificheManagerBean` |
| `TIPO_INCARICO_SIEPE` | 75 | 1 | `DecodificheManagerModel` |
| `TIPO_LICENZA` | 14 | 1 | `DecodificheManagerBean` |
| `TIPO_MISURA_CAUTELARE` | 17 | 2 | `DecodificheManagerBean`, `DecodificheManagerCore` |
| `TIPO_MISURA_SICUREZZA` | 24 | 6 | `TitoloEsecutivoController`, `ModuloCumuloController`, `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadMisuraSicurezza`, `DecodificheManagerBean` |
| `TIPO_PERMESSO` | 3 | 1 | `DecodificheManagerBean` |
| `TIPO_POS_LIBERO` | 2 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `TIPO_RESIDENZA` | 3 | 0 | — (nessuna occorrenza letterale con la batch search) |

### Categoria: OGGETTI (OGGETTO_*) (6 voci)

| Dominio | N° valori | Occorrenze batch | File Java principali |
|---|---:|---:|---|
| `OGGETTO_DECRETO` | 6 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `OGGETTO_PROCEDIMENTO` | 278 | 10 | `DecodificheManagerBean`, `ProcedimentixUdienzaSqlDAO`, `DepositoSentenzaSqlDAO`, `DepositoSentenzaDAO`, `DepositoSentenzaController` |
| `OGGETTO_RICHIESTA` | 1 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `OGGETTO_SIEP` | 33 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `OGGETTO_SIGE` | 214 | 1 | `DecodificheManagerModel` |
| `OGGETTO_SOSPENSIONI` | 35 | 2 | `DecodificheManagerBean`, `DecodificheController` |

### Categoria: ANAGRAFICA E TERRITORIO (9 voci)

| Dominio | N° valori | Occorrenze batch | File Java principali |
|---|---:|---:|---|
| `NAZIONALITA` | 3 | 23 | `RegeSoggettoSqlDAO`, `RegeSoggettoDAO`, `RegeSoggettoSentenzaSqlDAO`, `FascicoloSiepSqlDAO`, `FascicoloSiepSoggettoSqlDAO` |
| `NAZIONE` | 269 | 19 | `ActModificaCivilmenteObbligato`, `ActInserisciCivilmenteObbligato`, `FascicoloReatoSqlDAO`, `ActDettaglioSoggettoCumulato`, `ActInserisciSoggettoCumulato` |
| `NUM_GIORNO` | 7 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `PROVINCIA` | 117 | 29 | `RegeSoggettoSqlDAO`, `RegeSoggettoSentenzaSqlDAO`, `StoricoAvvocatoDAO`, `StoricoAvvocatoSqlDAO`, `ActModificaCivilmenteObbligato` |
| `QUESTURE` | 103 | 1 | `DecodificheManagerBean` |
| `REGIONE` | 22 | 0 | — (nessuna occorrenza letterale con la batch search) |
| `SEDE_GAB_POL_SCI` | 14 | 1 | `DecodificheManagerModel` |
| `SESSO` | 2 | 24 | `RegeSoggettoSqlDAO`, `RegeSoggettoDAO`, `RegeSoggettoSentenzaSqlDAO`, `CivilmenteObbligatoSqlDAO`, `CivilmenteObbligatoDAO` |
| `TIPO_ISTITUTO` | 36 | 2 | `DecodificheManagerBean`, `ProcAggregatiIstitutoDetenzioneSqlDAO` |

### Categoria: SEGNALAZIONI (5 voci)

| Dominio | N° valori | Occorrenze batch | File Java principali |
|---|---:|---:|---|
| `SEGNALAZIONE_AZIONE` | 10 | 1 | `DecodificheManagerBean` |
| `SEGNALAZIONE_FUNZIONALITA` | 187 | 1 | `DecodificheManagerBean` |
| `SEGNALAZIONE_GRAVITA` | 5 | 1 | `DecodificheManagerBean` |
| `SEGNALAZIONE_TIPOLOGIA` | 6 | 1 | `DecodificheManagerBean` |
| `SEGNALAZIONE_TITOLO` | 4 | 1 | `DecodificheManagerBean` |

### Categoria: DOMINI SPECIFICI SOTTOSISTEMI (2 voci)

| Dominio | N° valori | Occorrenze batch | File Java principali |
|---|---:|---:|---|
| `CONTENUTO_SIEP` | 105 | 1 | `DecodificheManagerBean` |
| `TIPO_GIUDIZIO_SIGE` | 2 | 1 | `DecodificheManagerModel` |

### Categoria: ALTRI DOMINI (18 voci)

| Dominio | N° valori | Occorrenze batch | File Java principali |
|---|---:|---:|---|
| `BILANCIAMENTO_CIRCOSTANZE` | 9 | 3 | `ActNscToSiesLoadCircostanze`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean` |
| `CONTENUTO_ISTANZA` | 44 | 1 | `DecodificheManagerBean` |
| `DEFI_ALTRO` | 4 | 5 | `ActLoadAnnotazioneRevocaConversione`, `ActLoadAnnotazioneRevocaConversioneSanzSost`, `ActLoadInserisciProvvConvPenPec`, `ActLoadInserisciProvvAltraAutorita`, `DecodificheManagerBean` |
| `DPR` | 25 | 5 | `StampaCumuloController`, `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadRevoche`, `ActNscToSiesLoadBenefici`, `DecodificheManagerBean` |
| `FONTE` | 32 | 4 | `ActNscToSiesLoadCircostanze`, `ActNscToSiesLoadReato`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean` |
| `NATURA_DECISIONE` | 32 | 2 | `ScambioSanzioneSqlDAO`, `MisuraAlternativaSqlDAO` |
| `NON_ATTIVITA` | 9 | 1 | `DecodificheManagerBean` |
| `PERIODO_CONSUMAZIONE` | 24 | 3 | `ActNscToSiesLoadReato`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean` |
| `POSIZIONE_GIURIDICA` | 85 | 12 | `ActStampaOrdineIngiunzione`, `CalcoloPenaDL92DAO`, `CalcoloPenaDL92SqlDAO`, `PosizioneGiuridicaDAO`, `DecodificheManagerBean` |
| `SOTTONUMERAZIONE` | 29 | 4 | `ActNscToSiesLoadCircostanze`, `ActNscToSiesLoadReato`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean` |
| `STAMPE_CUMULO` | 5 | 1 | `DecodificheManagerBean` |
| `TIPO_ANNOTAZIONE` | 30 | 1 | `DecodificheManagerBean` |
| `TIPO_ASSOLUZIONE` | 5 | 1 | `DecodificheManagerBean` |
| `TIPO_COMUNICAZIONE_PA` | 7 | 4 | `ActPreLoadComunicazione`, `ActComunicazione`, `ActLoadComunicazione`, `ActLoadInserisciComunicazione` |
| `TIPO_CONSEGUENZA` | 8 | 1 | `DecodificheManagerModel` |
| `TIPO_RATEIZZAZIONE` | 2 | 6 | `RateizzazionePPSqlDAO`, `RicercaStatoPagamentiSqlDao`, `RateizzazionePPDAO`, `BollettinoPagopaDAO`, `BollettinoPagopaSqlDAO` |
| `TIPO_REATO` | 3 | 3 | `ActNscToSiesLoadReato`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean` |
| `TIPO_RINNOVO` | 10 | 0 | — (nessuna occorrenza letterale con la batch search) |

---

## Catalogo alfabetico completo

### ATTIVITA_AVVOCATO

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | TIPI - Soggetti e Ruoli |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di attività svolte dall'avvocato nell'ambito del procedimento (es. difensore, sostituto). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### ATTI_ARCHIVIO

| Attributo | Valore |
|-----------|--------|
| N° valori | 2 |
| Categoria | TIPI - Registri e Atti |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipologie di atti archiviati nel fascicolo. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### AUTORITA_COMPETENTE

| Attributo | Valore |
|-----------|--------|
| N° valori | 9 |
| Categoria | TIPI - Uffici (TIPO_UFFICIO*) |
| File Java principali | `PosizioneGiuridicaSqlDAO`, `PosizioneGiuridicaDAO`, `MisuraCautelareCumuloDAO`, `MisuraCautelareCumuloSqlDAO`, `MisuraCautelareDAO` |
| Occorrenze nel codice | 7 file |
| Sottosistema | Trasversale |

**Descrizione**: Autorità giudiziarie/amministrative competenti per specifici procedimenti. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 7 file Java; i principali sono `PosizioneGiuridicaSqlDAO`, `PosizioneGiuridicaDAO`, `MisuraCautelareCumuloDAO`, `MisuraCautelareCumuloSqlDAO`, `MisuraCautelareDAO`.

### AUTORITA_CUMULO

| Attributo | Valore |
|-----------|--------|
| N° valori | 9 |
| Categoria | TIPI - Uffici (TIPO_UFFICIO*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Autorità competenti nel procedimento di cumulo delle pene. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nel procedimento di cumulo pene, sia nelle schermate di istruttoria sia nelle stampe e nei calcoli collegati. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### AUTORITA_NOTIFICA

| Attributo | Valore |
|-----------|--------|
| N° valori | 22 |
| Categoria | TIPI - Uffici (TIPO_UFFICIO*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Destinatari/mittenti delle notifiche giudiziarie (es. Procura, Avvocatura, Forze dell'ordine). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### BILANCIAMENTO_CIRCOSTANZE

| Attributo | Valore |
|-----------|--------|
| N° valori | 9 |
| Categoria | ALTRI DOMINI |
| File Java principali | `ActNscToSiesLoadCircostanze`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean` |
| Occorrenze nel codice | 3 file |
| Sottosistema | Trasversale |

**Descrizione**: Modalità di bilanciamento tra circostanze aggravanti e attenuanti. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 3 file Java; i principali sono `ActNscToSiesLoadCircostanze`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean`.

### CAUSALE_COMPUTO

| Attributo | Valore |
|-----------|--------|
| N° valori | 14 |
| Categoria | TIPI - Sanzioni (TIPO_SANZIONE*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Causali per il calcolo/computo della pena (es. custodia cautelare, liberazione anticipata). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle funzioni di esecuzione pena, calcolo del presofferto, conversione, cumulo e trattamento delle sanzioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### CONTENUTO_DECRETO

| Attributo | Valore |
|-----------|--------|
| N° valori | 7 |
| Categoria | TIPI - Provvedimenti (TIPO_PROVVEDIMENTO*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Contenuti tipici dei decreti emessi (es. decreto penale di condanna). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### CONTENUTO_ISTANZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 44 |
| Categoria | ALTRI DOMINI |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipologie di contenuti nelle istanze presentate dalla difesa o dal PM. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle schermate di acquisizione e lavorazione di istanze e richieste istruttorie. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### CONTENUTO_SIEP

| Attributo | Valore |
|-----------|--------|
| N° valori | 105 |
| Categoria | DOMINI SPECIFICI SOTTOSISTEMI / SIEP |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIEP |

**Descrizione**: Contenuti classificati nel sottosistema SIEP. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIEP indica una variante usata dal nucleo storico di gestione dell’esecuzione penale e delle sue classificazioni di fascicolo.

**Utilizzo applicativo**: È usato nel nucleo SIEP, nelle viste di fascicolo esecutivo, negli eventi e nelle classificazioni procedimentali. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### DATI_PROVVEDIMENTO_SIGE

| Attributo | Valore |
|-----------|--------|
| N° valori | 53 |
| Categoria | TIPI - Provvedimenti (TIPO_PROVVEDIMENTO*) / SIGE |
| File Java principali | `DatiProvvedimentoSigeDAO` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIGE |

**Descrizione**: Dati classificatori dei provvedimenti nel sottosistema SIGE. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIGE evidenzia una specializzazione per la Gestione Esecuzione, con valori mirati alle lavorazioni del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIGE, soprattutto nelle funzioni di fascicolo, udienza, impugnazione e gestione dei provvedimenti esecutivi. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DatiProvvedimentoSigeDAO`.

### DEFI_ALTRO

| Attributo | Valore |
|-----------|--------|
| N° valori | 4 |
| Categoria | ALTRI DOMINI |
| File Java principali | `ActLoadAnnotazioneRevocaConversione`, `ActLoadAnnotazioneRevocaConversioneSanzSost`, `ActLoadInserisciProvvConvPenPec`, `ActLoadInserisciProvvAltraAutorita`, `DecodificheManagerBean` |
| Occorrenze nel codice | 5 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipologie di definizione "altra" dei procedimenti. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 5 file Java; i principali sono `ActLoadAnnotazioneRevocaConversione`, `ActLoadAnnotazioneRevocaConversioneSanzSost`, `ActLoadInserisciProvvConvPenPec`, `ActLoadInserisciProvvAltraAutorita`, `DecodificheManagerBean`.

### DESTINATARIO_DEPOSITO

| Attributo | Valore |
|-----------|--------|
| N° valori | 10 |
| Categoria | TIPI - Registri e Atti |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Destinatari del deposito degli atti (es. cancelleria, archivio). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### DESTINATARIO_DEPOSITO_MINORENNI

| Attributo | Valore |
|-----------|--------|
| N° valori | 4 |
| Categoria | TIPI - Registri e Atti |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Destinatari deposito per procedimenti minorili. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### DESTINATARIO_DEPOSITO_SIGE

| Attributo | Valore |
|-----------|--------|
| N° valori | 2 |
| Categoria | TIPI - Registri e Atti / SIGE |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIGE |

**Descrizione**: Destinatari deposito nel sottosistema SIGE. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIGE evidenzia una specializzazione per la Gestione Esecuzione, con valori mirati alle lavorazioni del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIGE, soprattutto nelle funzioni di fascicolo, udienza, impugnazione e gestione dei provvedimenti esecutivi. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### DETTAGLIO_MOTIVO

| Attributo | Valore |
|-----------|--------|
| N° valori | 49 |
| Categoria | MOTIVI (MOTIVO_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Dettagli specifici del motivo di una decisione o provvedimento. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### DETTAGLIO_MOTIVO (voce duplicata nella lista sorgente)

| Attributo | Valore |
|-----------|--------|
| N° valori | 19 |
| Categoria | MOTIVI (MOTIVO_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Dettagli specifici del motivo di una decisione o provvedimento. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. La lista sorgente fornita per questa analisi riporta una seconda voce omonima con cardinalità diversa; la distinzione va confermata sul database Oracle.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli. In assenza di riferimenti distinti nel codice, questa seconda voce è trattata come anomalia della lista sorgente e non come dominio Java separato.

### DPR

| Attributo | Valore |
|-----------|--------|
| N° valori | 25 |
| Categoria | ALTRI DOMINI |
| File Java principali | `StampaCumuloController`, `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadRevoche`, `ActNscToSiesLoadBenefici`, `DecodificheManagerBean` |
| Occorrenze nel codice | 5 file |
| Sottosistema | Trasversale |

**Descrizione**: Classificazione DPR (Decreti del Presidente della Repubblica) rilevanti. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 5 file Java; i principali sono `StampaCumuloController`, `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadRevoche`, `ActNscToSiesLoadBenefici`, `DecodificheManagerBean`.

### ESITO_ATTIVITA_SIEPE

| Attributo | Valore |
|-----------|--------|
| N° valori | 2 |
| Categoria | ESITI (ESITO_* / TENORE_*) / SIEPE |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIEPE |

**Descrizione**: Esiti delle attività nel sottosistema SIEPE (permessi/licenze). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIEPE segnala un uso dedicato alle funzioni su permessi, licenze e attività istruttorie del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIEPE, in particolare per permessi, licenze, richieste e attività istruttorie. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### ESITO_ISTANZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 6 |
| Categoria | ESITI (ESITO_* / TENORE_*) |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Esiti delle istanze (es. accolta, rigettata, inammissibile). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle schermate di acquisizione e lavorazione di istanze e richieste istruttorie. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### ESITO_NOTIFICA

| Attributo | Valore |
|-----------|--------|
| N° valori | 4 |
| Categoria | ESITI (ESITO_* / TENORE_*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Esiti delle notifiche giudiziarie (es. notificata, irreperibile). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### ESITO_PERMESSO_LICENZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | ESITI (ESITO_* / TENORE_*) |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Esiti di permessi e licenze (es. concesso, revocato, scaduto). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella gestione di benefici penitenziari, misure cautelari o di sicurezza, permessi, licenze e sospensioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### ESITO_PROVVEDIMENTO

| Attributo | Valore |
|-----------|--------|
| N° valori | 374 |
| Categoria | ESITI (ESITO_* / TENORE_*) |
| File Java principali | `ActLoadModificaIstanza`, `ActLoadModificaIstanzaAnnTrasmissione`, `DecodificheManagerBean`, `DecodificheManagerModel` |
| Occorrenze nel codice | 4 file |
| Sottosistema | Trasversale |

**Descrizione**: Esiti dei provvedimenti giudiziari (lista molto ampia, 374 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search basata su letterali in doppie virgolette ha rilevato 4 file Java; i principali sono `ActLoadModificaIstanza`, `ActLoadModificaIstanzaAnnTrasmissione`, `DecodificheManagerBean`, `DecodificheManagerModel`.

### ESITO_PROVVEDIMENTO_SIGE

| Attributo | Valore |
|-----------|--------|
| N° valori | 81 |
| Categoria | ESITI (ESITO_* / TENORE_*) / SIGE |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | SIGE |

**Descrizione**: Esiti provvedimenti nel sottosistema SIGE. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIGE evidenzia una specializzazione per la Gestione Esecuzione, con valori mirati alle lavorazioni del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIGE, soprattutto nelle funzioni di fascicolo, udienza, impugnazione e gestione dei provvedimenti esecutivi. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### ESITO_RICHIESTA

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | ESITI (ESITO_* / TENORE_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Esiti delle richieste istruttorie. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle schermate di acquisizione e lavorazione di istanze e richieste istruttorie. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### ESITO_SIEP

| Attributo | Valore |
|-----------|--------|
| N° valori | 480 |
| Categoria | ESITI (ESITO_* / TENORE_*) / SIEP |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIEP |

**Descrizione**: Esiti nel sottosistema SIEP (480 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIEP indica una variante usata dal nucleo storico di gestione dell’esecuzione penale e delle sue classificazioni di fascicolo.

**Utilizzo applicativo**: È usato nel nucleo SIEP, nelle viste di fascicolo esecutivo, negli eventi e nelle classificazioni procedimentali. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### ESITO_TENORE

| Attributo | Valore |
|-----------|--------|
| N° valori | 1237 |
| Categoria | ESITI (ESITO_* / TENORE_*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tenore degli esiti dei procedimenti (1237 valori - tabella principale decodifica). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle viste di fascicolo e procedimento, per esporre in modo coerente stati, oggetti, posizioni ed esiti. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### ESITO_TENORE_SIGE

| Attributo | Valore |
|-----------|--------|
| N° valori | 392 |
| Categoria | ESITI (ESITO_* / TENORE_*) / SIGE |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIGE |

**Descrizione**: Tenore esiti nel sottosistema SIGE. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIGE evidenzia una specializzazione per la Gestione Esecuzione, con valori mirati alle lavorazioni del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIGE, soprattutto nelle funzioni di fascicolo, udienza, impugnazione e gestione dei provvedimenti esecutivi. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### FIRMA_UFFICIO

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | TIPI - Uffici (TIPO_UFFICIO*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Uffici/magistrati abilitati alla firma degli atti. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### FLAG_CONCESSO

| Attributo | Valore |
|-----------|--------|
| N° valori | 4 |
| Categoria | FLAG (FLAG_*) |
| File Java principali | `LibAnticipataCumuloDAO`, `LibAnticipataCumuloSqlDAO`, `PeriodoLibanticipataSqlDAO`, `LicenzaLibanticipataSqlDAO`, `PeriodoLibanticipataDAO` |
| Occorrenze nel codice | 6 file |
| Sottosistema | Trasversale |

**Descrizione**: Indicatore booleano/ternario se un beneficio/misura è stato concesso. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 6 file Java; i principali sono `LibAnticipataCumuloDAO`, `LibAnticipataCumuloSqlDAO`, `PeriodoLibanticipataSqlDAO`, `LicenzaLibanticipataSqlDAO`, `PeriodoLibanticipataDAO`.

### FLAG_ERGASTOLO

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | FLAG (FLAG_*) |
| File Java principali | `PenaResiduaDettaglioSqlDAO`, `PenaPrecedenteSqlDAO`, `PenaResiduaDAO`, `PenaResiduaSqlDAO`, `PenaResiduaPerStatoEsecuzioneSqlDAO` |
| Occorrenze nel codice | 14 file |
| Sottosistema | Trasversale |

**Descrizione**: Indicatore presenza pena ergastolo nel fascicolo. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle funzioni di esecuzione pena, calcolo del presofferto, conversione, cumulo e trattamento delle sanzioni. La batch search basata su letterali in doppie virgolette ha rilevato 14 file Java; i principali sono `PenaResiduaDettaglioSqlDAO`, `PenaPrecedenteSqlDAO`, `PenaResiduaDAO`, `PenaResiduaSqlDAO`, `PenaResiduaPerStatoEsecuzioneSqlDAO`.

### FLAG_ESITO_TENORE

| Attributo | Valore |
|-----------|--------|
| N° valori | 4 |
| Categoria | FLAG (FLAG_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Flag classificatorio associato all'esito/tenore. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle viste di fascicolo e procedimento, per esporre in modo coerente stati, oggetti, posizioni ed esiti. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### FLAG_ISTANZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | FLAG (FLAG_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Flag di stato/tipo dell'istanza. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle schermate di acquisizione e lavorazione di istanze e richieste istruttorie. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### FLAG_ISTANZA_PD

| Attributo | Valore |
|-----------|--------|
| N° valori | 2 |
| Categoria | FLAG (FLAG_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Flag istanza per procedimenti direttissima. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle schermate di acquisizione e lavorazione di istanze e richieste istruttorie. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### FLAG_PIU_MENO

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | FLAG (FLAG_*) |
| File Java principali | `EventoVerbaleSqlDAO`, `ComputiCumuloSqlDAO`, `ComputiCumuloDAO`, `IstanzaSqlDAO`, `ProvvedimentoSqlDAO` |
| Occorrenze nel codice | 18 file |
| Sottosistema | Trasversale |

**Descrizione**: Indicatore segno algebrico (aggiunta/sottrazione) nel calcolo pena. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 18 file Java; i principali sono `EventoVerbaleSqlDAO`, `ComputiCumuloSqlDAO`, `ComputiCumuloDAO`, `IstanzaSqlDAO`, `ProvvedimentoSqlDAO`.

### FLAG_SCARCERATO_SCARCERARE

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | FLAG (FLAG_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Stato scarcerazione del detenuto. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### FLAG_SI_NO

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | FLAG (FLAG_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Flag booleano generico sì/no. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### FLAG_STATO

| Attributo | Valore |
|-----------|--------|
| N° valori | 4 |
| Categoria | FLAG (FLAG_*) |
| File Java principali | `ReatoCumuloDAO`, `LibAnticipataCumuloDAO`, `PeriodoLibAntCumuloDAO`, `BeneficioCumuloDAO`, `ComputiCumuloSqlDAO` |
| Occorrenze nel codice | 50 file |
| Sottosistema | Trasversale |

**Descrizione**: Flag di stato generico. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle viste di fascicolo e procedimento, per esporre in modo coerente stati, oggetti, posizioni ed esiti. La batch search basata su letterali in doppie virgolette ha rilevato 50 file Java; i principali sono `ReatoCumuloDAO`, `LibAnticipataCumuloDAO`, `PeriodoLibAntCumuloDAO`, `BeneficioCumuloDAO`, `ComputiCumuloSqlDAO`.

### FONTE

| Attributo | Valore |
|-----------|--------|
| N° valori | 32 |
| Categoria | ALTRI DOMINI |
| File Java principali | `ActNscToSiesLoadCircostanze`, `ActNscToSiesLoadReato`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean` |
| Occorrenze nel codice | 4 file |
| Sottosistema | Trasversale |

**Descrizione**: Fonte/provenienza dell'atto o dell'informazione (es. MIN, TRI, PRO). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 4 file Java; i principali sono `ActNscToSiesLoadCircostanze`, `ActNscToSiesLoadReato`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean`.

### FORO_AVVOCATI

| Attributo | Valore |
|-----------|--------|
| N° valori | 167 |
| Categoria | TIPI - Soggetti e Ruoli |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Fori/ordini professionali di appartenenza degli avvocati. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle anagrafiche di soggetti, difensori, residenze e sedi territoriali. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### INSERIMENTO_MA

| Attributo | Valore |
|-----------|--------|
| N° valori | 39 |
| Categoria | TIPI - Misure e Benefici |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipologie di inserimento per misure alternative. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### INSERIMENTO_SS

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | TIPI - Misure e Benefici |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipologie di inserimento per semilibertà. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### MITTENTE_ATTO

| Attributo | Valore |
|-----------|--------|
| N° valori | 36 |
| Categoria | TIPI - Registri e Atti |
| File Java principali | `DecodificheManagerBean`, `ProcAggregatiProcuraMittenteSqlDAO` |
| Occorrenze nel codice | 2 file |
| Sottosistema | Trasversale |

**Descrizione**: Mittenti degli atti giudiziari. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 2 file Java; i principali sono `DecodificheManagerBean`, `ProcAggregatiProcuraMittenteSqlDAO`.

### MITTENTE_ISTANZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 71 |
| Categoria | TIPI - Registri e Atti |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Mittenti delle istanze (es. difensore, imputato, PM). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### MOTIVAZIONE_NON_INVIO_FC

| Attributo | Valore |
|-----------|--------|
| N° valori | 2 |
| Categoria | MOTIVI (MOTIVO_*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Motivazioni per il mancato invio al fascicolo centrale. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### MOTIVO_ARCHIVIAZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 15 |
| Categoria | MOTIVI (MOTIVO_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Motivi di archiviazione del procedimento. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### MOTIVO_DESIGNAZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 8 |
| Categoria | MOTIVI (MOTIVO_*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Motivi di designazione del magistrato/ufficio. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle anagrafiche di soggetti, difensori, residenze e sedi territoriali. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### MOTIVO_DETENZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 2 |
| Categoria | MOTIVI (MOTIVO_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Motivi giuridici della detenzione (es. custodia cautelare, esecuzione pena). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### MOTIVO_INAMMISSIBILITA

| Attributo | Valore |
|-----------|--------|
| N° valori | 57 |
| Categoria | MOTIVI (MOTIVO_*) |
| File Java principali | `DecodificheController` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Motivi di inammissibilità di un'istanza o ricorso. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheController`.

### MOTIVO_INAMMISSIBILITA_SIGE

| Attributo | Valore |
|-----------|--------|
| N° valori | 9 |
| Categoria | MOTIVI (MOTIVO_*) / SIGE |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | SIGE |

**Descrizione**: Motivi inammissibilità nel sottosistema SIGE. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIGE evidenzia una specializzazione per la Gestione Esecuzione, con valori mirati alle lavorazioni del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIGE, soprattutto nelle funzioni di fascicolo, udienza, impugnazione e gestione dei provvedimenti esecutivi. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### MOTIVO_INTSOSP

| Attributo | Valore |
|-----------|--------|
| N° valori | 18 |
| Categoria | MOTIVI (MOTIVO_*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Motivi di interruzione/sospensione della pena. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella gestione di benefici penitenziari, misure cautelari o di sicurezza, permessi, licenze e sospensioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### MOTIVO_NON_COMPUTABILE

| Attributo | Valore |
|-----------|--------|
| N° valori | 7 |
| Categoria | MOTIVI (MOTIVO_*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Motivi per cui un periodo non è computabile nella pena. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### MOTIVO_PERIODO_EMS

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | MOTIVI (MOTIVO_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Motivi dei periodi di esecuzione in misura sostitutiva. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### MOTIVO_PERIODO_ESS

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | MOTIVI (MOTIVO_*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Motivi dei periodi di esecuzione in semilibertà. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### MOTIVO_PROVVEDIMENTO

| Attributo | Valore |
|-----------|--------|
| N° valori | 1659 |
| Categoria | MOTIVI (MOTIVO_*) |
| File Java principali | `ActLoadInserisciRevocaMisuraAlternativaCumulo`, `ActLoadInserisciEspulsioneCumulo`, `ActLoadInserisciSospMisuraAlternativaCumulo`, `ActLoadInserisciSospEsecuzionePenaCumulo`, `ActDettaglioRichiestaGERevocaBenefici` |
| Occorrenze nel codice | 35 file |
| Sottosistema | Trasversale |

**Descrizione**: Motivi alla base dei provvedimenti (1659 valori - tabella più grande). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search basata su letterali in doppie virgolette ha rilevato 35 file Java; i principali sono `ActLoadInserisciRevocaMisuraAlternativaCumulo`, `ActLoadInserisciEspulsioneCumulo`, `ActLoadInserisciSospMisuraAlternativaCumulo`, `ActLoadInserisciSospEsecuzionePenaCumulo`, `ActDettaglioRichiestaGERevocaBenefici`.

### MOTIVO_SOSPENSIONE_CUMULO

| Attributo | Valore |
|-----------|--------|
| N° valori | 1 |
| Categoria | MOTIVI (MOTIVO_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Motivi di sospensione del cumulo pene. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nel procedimento di cumulo pene, sia nelle schermate di istruttoria sia nelle stampe e nei calcoli collegati. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### NATURA_BENEFICIO

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Misure e Benefici |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Natura/tipo del beneficio penitenziario. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella gestione di benefici penitenziari, misure cautelari o di sicurezza, permessi, licenze e sospensioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### NATURA_DECISIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 32 |
| Categoria | ALTRI DOMINI |
| File Java principali | `ScambioSanzioneSqlDAO`, `MisuraAlternativaSqlDAO` |
| Occorrenze nel codice | 2 file |
| Sottosistema | Trasversale |

**Descrizione**: Natura della decisione giudiziaria. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search basata su letterali in doppie virgolette ha rilevato 2 file Java; i principali sono `ScambioSanzioneSqlDAO`, `MisuraAlternativaSqlDAO`.

### NATURA_MISURA_SICUREZZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 4 |
| Categoria | TIPI - Misure e Benefici |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Natura della misura di sicurezza applicata. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella gestione di benefici penitenziari, misure cautelari o di sicurezza, permessi, licenze e sospensioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### NATURA_PENA

| Attributo | Valore |
|-----------|--------|
| N° valori | 1 |
| Categoria | TIPI - Sanzioni (TIPO_SANZIONE*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Natura della pena (es. detentiva, pecuniaria). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle funzioni di esecuzione pena, calcolo del presofferto, conversione, cumulo e trattamento delle sanzioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### NAZIONALITA

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | ANAGRAFICA E TERRITORIO |
| File Java principali | `RegeSoggettoSqlDAO`, `RegeSoggettoDAO`, `RegeSoggettoSentenzaSqlDAO`, `FascicoloSiepSqlDAO`, `FascicoloSiepSoggettoSqlDAO` |
| Occorrenze nel codice | 23 file |
| Sottosistema | Trasversale |

**Descrizione**: Nazionalità dei soggetti (stranieri/italiani/apolidi). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle anagrafiche di soggetti, difensori, residenze e sedi territoriali. La batch search basata su letterali in doppie virgolette ha rilevato 23 file Java; i principali sono `RegeSoggettoSqlDAO`, `RegeSoggettoDAO`, `RegeSoggettoSentenzaSqlDAO`, `FascicoloSiepSqlDAO`, `FascicoloSiepSoggettoSqlDAO`.

### NAZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 269 |
| Categoria | ANAGRAFICA E TERRITORIO |
| File Java principali | `ActModificaCivilmenteObbligato`, `ActInserisciCivilmenteObbligato`, `FascicoloReatoSqlDAO`, `ActDettaglioSoggettoCumulato`, `ActInserisciSoggettoCumulato` |
| Occorrenze nel codice | 19 file |
| Sottosistema | Trasversale |

**Descrizione**: Codici nazione (269 valori - lista paesi). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle anagrafiche di soggetti, difensori, residenze e sedi territoriali. La batch search basata su letterali in doppie virgolette ha rilevato 19 file Java; i principali sono `ActModificaCivilmenteObbligato`, `ActInserisciCivilmenteObbligato`, `FascicoloReatoSqlDAO`, `ActDettaglioSoggettoCumulato`, `ActInserisciSoggettoCumulato`.

### NOME_PROVVEDIMENTO

| Attributo | Valore |
|-----------|--------|
| N° valori | 170 |
| Categoria | TIPI - Provvedimenti (TIPO_PROVVEDIMENTO*) |
| File Java principali | `NomeProvvedimentoDAO` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Denominazioni dei tipi di provvedimento. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `NomeProvvedimentoDAO`.

### NON_ATTIVITA

| Attributo | Valore |
|-----------|--------|
| N° valori | 9 |
| Categoria | ALTRI DOMINI |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Classificazione attività non eseguite/sospese. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### NUM_GIORNO

| Attributo | Valore |
|-----------|--------|
| N° valori | 7 |
| Categoria | ANAGRAFICA E TERRITORIO |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Giorni della settimana o numerazione giorni. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### OGGETTO_DECRETO

| Attributo | Valore |
|-----------|--------|
| N° valori | 6 |
| Categoria | OGGETTI (OGGETTO_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Oggetto/materia dei decreti. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### OGGETTO_PROCEDIMENTO

| Attributo | Valore |
|-----------|--------|
| N° valori | 278 |
| Categoria | OGGETTI (OGGETTO_*) |
| File Java principali | `DecodificheManagerBean`, `ProcedimentixUdienzaSqlDAO`, `DepositoSentenzaSqlDAO`, `DepositoSentenzaDAO`, `DepositoSentenzaController` |
| Occorrenze nel codice | 10 file |
| Sottosistema | Trasversale |

**Descrizione**: Oggetto/materia del procedimento penale (278 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle viste di fascicolo e procedimento, per esporre in modo coerente stati, oggetti, posizioni ed esiti. La batch search basata su letterali in doppie virgolette ha rilevato 10 file Java; i principali sono `DecodificheManagerBean`, `ProcedimentixUdienzaSqlDAO`, `DepositoSentenzaSqlDAO`, `DepositoSentenzaDAO`, `DepositoSentenzaController`.

### OGGETTO_RICHIESTA

| Attributo | Valore |
|-----------|--------|
| N° valori | 1 |
| Categoria | OGGETTI (OGGETTO_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Oggetto delle richieste istruttorie. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle schermate di acquisizione e lavorazione di istanze e richieste istruttorie. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### OGGETTO_SIEP

| Attributo | Valore |
|-----------|--------|
| N° valori | 33 |
| Categoria | OGGETTI (OGGETTO_*) / SIEP |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | SIEP |

**Descrizione**: Oggetto nel sottosistema SIEP. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIEP indica una variante usata dal nucleo storico di gestione dell’esecuzione penale e delle sue classificazioni di fascicolo.

**Utilizzo applicativo**: È usato nel nucleo SIEP, nelle viste di fascicolo esecutivo, negli eventi e nelle classificazioni procedimentali. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### OGGETTO_SIGE

| Attributo | Valore |
|-----------|--------|
| N° valori | 214 |
| Categoria | OGGETTI (OGGETTO_*) / SIGE |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIGE |

**Descrizione**: Oggetto nel sottosistema SIGE (214 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIGE evidenzia una specializzazione per la Gestione Esecuzione, con valori mirati alle lavorazioni del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIGE, soprattutto nelle funzioni di fascicolo, udienza, impugnazione e gestione dei provvedimenti esecutivi. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### OGGETTO_SOSPENSIONI

| Attributo | Valore |
|-----------|--------|
| N° valori | 35 |
| Categoria | OGGETTI (OGGETTO_*) |
| File Java principali | `DecodificheManagerBean`, `DecodificheController` |
| Occorrenze nel codice | 2 file |
| Sottosistema | Trasversale |

**Descrizione**: Oggetto delle sospensioni dell'esecuzione. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle viste di fascicolo e procedimento, per esporre in modo coerente stati, oggetti, posizioni ed esiti. La batch search basata su letterali in doppie virgolette ha rilevato 2 file Java; i principali sono `DecodificheManagerBean`, `DecodificheController`.

### PERIODO_CONSUMAZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 24 |
| Categoria | ALTRI DOMINI |
| File Java principali | `ActNscToSiesLoadReato`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean` |
| Occorrenze nel codice | 3 file |
| Sottosistema | Trasversale |

**Descrizione**: Periodi rilevanti per la consumazione del reato. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 3 file Java; i principali sono `ActNscToSiesLoadReato`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean`.

### PESO_ESITO_TENORE

| Attributo | Valore |
|-----------|--------|
| N° valori | 331 |
| Categoria | ESITI (ESITO_* / TENORE_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Peso/priorità associato all'esito tenore per ordinamento. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle viste di fascicolo e procedimento, per esporre in modo coerente stati, oggetti, posizioni ed esiti. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### POSIZIONE_GIURIDICA

| Attributo | Valore |
|-----------|--------|
| N° valori | 85 |
| Categoria | ALTRI DOMINI |
| File Java principali | `ActStampaOrdineIngiunzione`, `CalcoloPenaDL92DAO`, `CalcoloPenaDL92SqlDAO`, `PosizioneGiuridicaDAO`, `DecodificheManagerBean` |
| Occorrenze nel codice | 12 file |
| Sottosistema | Trasversale |

**Descrizione**: Posizione giuridica del detenuto (85 valori - es. definitivo, in attesa giudizio). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle viste di fascicolo e procedimento, per esporre in modo coerente stati, oggetti, posizioni ed esiti. La batch search basata su letterali in doppie virgolette ha rilevato 12 file Java; i principali sono `ActStampaOrdineIngiunzione`, `CalcoloPenaDL92DAO`, `CalcoloPenaDL92SqlDAO`, `PosizioneGiuridicaDAO`, `DecodificheManagerBean`.

### POSIZIONE_GIURIDICA_BENEFICI

| Attributo | Valore |
|-----------|--------|
| N° valori | 85 |
| Categoria | TIPI - Misure e Benefici |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Posizione giuridica rilevante per la concessione di benefici. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle viste di fascicolo e procedimento, per esporre in modo coerente stati, oggetti, posizioni ed esiti. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### POSIZIONE_PROCESSUALE

| Attributo | Valore |
|-----------|--------|
| N° valori | 4 |
| Categoria | TIPI - Soggetti e Ruoli |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Posizione del soggetto nel processo (es. imputato, condannato, prosciolto). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle viste di fascicolo e procedimento, per esporre in modo coerente stati, oggetti, posizioni ed esiti. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### PROVINCIA

| Attributo | Valore |
|-----------|--------|
| N° valori | 117 |
| Categoria | ANAGRAFICA E TERRITORIO |
| File Java principali | `RegeSoggettoSqlDAO`, `RegeSoggettoSentenzaSqlDAO`, `StoricoAvvocatoDAO`, `StoricoAvvocatoSqlDAO`, `ActModificaCivilmenteObbligato` |
| Occorrenze nel codice | 29 file |
| Sottosistema | Trasversale |

**Descrizione**: Province italiane (117 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle anagrafiche di soggetti, difensori, residenze e sedi territoriali. La batch search basata su letterali in doppie virgolette ha rilevato 29 file Java; i principali sono `RegeSoggettoSqlDAO`, `RegeSoggettoSentenzaSqlDAO`, `StoricoAvvocatoDAO`, `StoricoAvvocatoSqlDAO`, `ActModificaCivilmenteObbligato`.

### QUESTURE

| Attributo | Valore |
|-----------|--------|
| N° valori | 103 |
| Categoria | ANAGRAFICA E TERRITORIO |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Questure italiane (103 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle anagrafiche di soggetti, difensori, residenze e sedi territoriali. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### REGIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 22 |
| Categoria | ANAGRAFICA E TERRITORIO |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Regioni italiane (22 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle anagrafiche di soggetti, difensori, residenze e sedi territoriali. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### REVOCA_DECSOSP

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | MOTIVI (MOTIVO_*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipologie di revoca di decreti di sospensione. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### RICERCA_EMA

| Attributo | Valore |
|-----------|--------|
| N° valori | 28 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Parametri di ricerca nel modulo EMA (Esecuzione Misure Alternative). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### RICHIEDENTE

| Attributo | Valore |
|-----------|--------|
| N° valori | 1 |
| Categoria | TIPI - Soggetti e Ruoli |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Soggetto richiedente nel procedimento. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### RUOLO_GIUDICE_POPOLARE

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Soggetti e Ruoli |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Ruoli dei giudici popolari in Corte d'Assise. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### RUOLO_MAGISTRATO

| Attributo | Valore |
|-----------|--------|
| N° valori | 4 |
| Categoria | TIPI - Soggetti e Ruoli |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Ruoli dei magistrati nell'ufficio (es. Presidente, Sostituto). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### SEDE_GAB_POL_SCI

| Attributo | Valore |
|-----------|--------|
| N° valori | 14 |
| Categoria | ANAGRAFICA E TERRITORIO |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Sedi dei Gabinetti di Polizia Scientifica. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### SEGNALAZIONE_AZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 10 |
| Categoria | SEGNALAZIONI |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Azioni previste per le segnalazioni nel sistema. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nel modulo di segnalazione anomalie, classificazione bug e raccolta richieste di miglioramento. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### SEGNALAZIONE_FUNZIONALITA

| Attributo | Valore |
|-----------|--------|
| N° valori | 187 |
| Categoria | SEGNALAZIONI |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Funzionalità del sistema a cui si riferisce la segnalazione (187 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nel modulo di segnalazione anomalie, classificazione bug e raccolta richieste di miglioramento. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### SEGNALAZIONE_GRAVITA

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | SEGNALAZIONI |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Livelli di gravità delle segnalazioni (bug/anomalie). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nel modulo di segnalazione anomalie, classificazione bug e raccolta richieste di miglioramento. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### SEGNALAZIONE_TIPOLOGIA

| Attributo | Valore |
|-----------|--------|
| N° valori | 6 |
| Categoria | SEGNALAZIONI |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipologie di segnalazione (es. bug, richiesta miglioramento). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nel modulo di segnalazione anomalie, classificazione bug e raccolta richieste di miglioramento. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### SEGNALAZIONE_TITOLO

| Attributo | Valore |
|-----------|--------|
| N° valori | 4 |
| Categoria | SEGNALAZIONI |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Titoli predefiniti per le segnalazioni. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nel modulo di segnalazione anomalie, classificazione bug e raccolta richieste di miglioramento. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### SESSO

| Attributo | Valore |
|-----------|--------|
| N° valori | 2 |
| Categoria | ANAGRAFICA E TERRITORIO |
| File Java principali | `RegeSoggettoSqlDAO`, `RegeSoggettoDAO`, `RegeSoggettoSentenzaSqlDAO`, `CivilmenteObbligatoSqlDAO`, `CivilmenteObbligatoDAO` |
| Occorrenze nel codice | 24 file |
| Sottosistema | Trasversale |

**Descrizione**: Sesso del soggetto (M/F). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle anagrafiche di soggetti, difensori, residenze e sedi territoriali. La batch search basata su letterali in doppie virgolette ha rilevato 24 file Java; i principali sono `RegeSoggettoSqlDAO`, `RegeSoggettoDAO`, `RegeSoggettoSentenzaSqlDAO`, `CivilmenteObbligatoSqlDAO`, `CivilmenteObbligatoDAO`.

### SOGGETTO_IMPUGNANTE

| Attributo | Valore |
|-----------|--------|
| N° valori | 9 |
| Categoria | TIPI - Soggetti e Ruoli |
| File Java principali | `DecodificheManagerBean`, `FascicoloSigeSqlDAO`, `ImpugnazioneSigeDAO`, `ImpugnazioneSigeSqlDAO`, `ImpugnazioneDAO` |
| Occorrenze nel codice | 6 file |
| Sottosistema | Trasversale |

**Descrizione**: Soggetti che presentano impugnazione. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle viste di fascicolo e procedimento, per esporre in modo coerente stati, oggetti, posizioni ed esiti. La batch search basata su letterali in doppie virgolette ha rilevato 6 file Java; i principali sono `DecodificheManagerBean`, `FascicoloSigeSqlDAO`, `ImpugnazioneSigeDAO`, `ImpugnazioneSigeSqlDAO`, `ImpugnazioneDAO`.

### SOGGETTO_IMPUGNANTE_SIGE

| Attributo | Valore |
|-----------|--------|
| N° valori | 7 |
| Categoria | TIPI - Soggetti e Ruoli / SIGE |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIGE |

**Descrizione**: Soggetti impugnanti nel sottosistema SIGE. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIGE evidenzia una specializzazione per la Gestione Esecuzione, con valori mirati alle lavorazioni del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIGE, soprattutto nelle funzioni di fascicolo, udienza, impugnazione e gestione dei provvedimenti esecutivi. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### SOSPENDE_E_TRASMETTE_GLI_ATTI_AL_TDS

| Attributo | Valore |
|-----------|--------|
| N° valori | 1 |
| Categoria | FLAG (FLAG_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Flag per sospensione e trasmissione atti al Tribunale di Sorveglianza. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### SOTTONUMERAZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 29 |
| Categoria | ALTRI DOMINI |
| File Java principali | `ActNscToSiesLoadCircostanze`, `ActNscToSiesLoadReato`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean` |
| Occorrenze nel codice | 4 file |
| Sottosistema | Trasversale |

**Descrizione**: Modalità di sottonumerazione dei fascicoli. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 4 file Java; i principali sono `ActNscToSiesLoadCircostanze`, `ActNscToSiesLoadReato`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean`.

### SOTTOTIPO_BENEFICIO

| Attributo | Valore |
|-----------|--------|
| N° valori | 11 |
| Categoria | TIPI - Misure e Benefici |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Sottotipi specifici dei benefici penitenziari. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella gestione di benefici penitenziari, misure cautelari o di sicurezza, permessi, licenze e sospensioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### STAMPE_CUMULO

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | ALTRI DOMINI |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipologie di stampe nel procedimento di cumulo. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nel procedimento di cumulo pene, sia nelle schermate di istruttoria sia nelle stampe e nei calcoli collegati. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### STATO_AVVOCATO

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | STATI (STATO_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Stato professionale dell'avvocato (es. abilitato, sospeso). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle viste di fascicolo e procedimento, per esporre in modo coerente stati, oggetti, posizioni ed esiti. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### STATO_FASCICOLO

| Attributo | Valore |
|-----------|--------|
| N° valori | 23 |
| Categoria | STATI (STATO_*) |
| File Java principali | `FascicoloSiepSoggettoSqlDAO`, `DecodificheManagerBean` |
| Occorrenze nel codice | 2 file |
| Sottosistema | Trasversale |

**Descrizione**: Stato del fascicolo processuale (23 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle viste di fascicolo e procedimento, per esporre in modo coerente stati, oggetti, posizioni ed esiti. La batch search basata su letterali in doppie virgolette ha rilevato 2 file Java; i principali sono `FascicoloSiepSoggettoSqlDAO`, `DecodificheManagerBean`.

### STATO_FLAG_RINVIATA

| Attributo | Valore |
|-----------|--------|
| N° valori | 4 |
| Categoria | STATI (STATO_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Flag di stato per udienze rinviate. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle viste di fascicolo e procedimento, per esporre in modo coerente stati, oggetti, posizioni ed esiti. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### STATO_ISTANZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | STATI (STATO_*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Stato dell'istanza presentata. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle schermate di acquisizione e lavorazione di istanze e richieste istruttorie. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### STATO_ISTRUTTORIA_CUMULO

| Attributo | Valore |
|-----------|--------|
| N° valori | 4 |
| Categoria | STATI (STATO_*) |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Stato dell'istruttoria nel procedimento di cumulo. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nel procedimento di cumulo pene, sia nelle schermate di istruttoria sia nelle stampe e nei calcoli collegati. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### STATO_LIBERTATIS

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | STATI (STATO_*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Stato di libertà del soggetto (es. detenuto, libero, latitante). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle viste di fascicolo e procedimento, per esporre in modo coerente stati, oggetti, posizioni ed esiti. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### STATO_MISURA_CUMULO

| Attributo | Valore |
|-----------|--------|
| N° valori | 4 |
| Categoria | STATI (STATO_*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Stato della misura nel cumulo pene. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nel procedimento di cumulo pene, sia nelle schermate di istruttoria sia nelle stampe e nei calcoli collegati. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### STATO_NUOVA_ISTANZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 9 |
| Categoria | STATI (STATO_*) |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Stato di una nuova istanza inserita. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle schermate di acquisizione e lavorazione di istanze e richieste istruttorie. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### STATO_PAGAMENTO

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | STATI (STATO_*) |
| File Java principali | `BollettinoPagopaDAO`, `BollettinoPagopaSqlDAO`, `ScadenzarioSoggettoSqlDAO` |
| Occorrenze nel codice | 3 file |
| Sottosistema | Trasversale |

**Descrizione**: Stato del pagamento di pene pecuniarie. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle viste di fascicolo e procedimento, per esporre in modo coerente stati, oggetti, posizioni ed esiti. La batch search basata su letterali in doppie virgolette ha rilevato 3 file Java; i principali sono `BollettinoPagopaDAO`, `BollettinoPagopaSqlDAO`, `ScadenzarioSoggettoSqlDAO`.

### STATO_PERMESSO

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | STATI (STATO_*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Stato del permesso (es. in corso, scaduto, revocato). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella gestione di benefici penitenziari, misure cautelari o di sicurezza, permessi, licenze e sospensioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### STATO_PROCEDIMENTO

| Attributo | Valore |
|-----------|--------|
| N° valori | 473 |
| Categoria | STATI (STATO_*) |
| File Java principali | `StatoProcedimentoDAO`, `FascicoloSiepOnViewSqlDAO`, `EventoSimeoneSqlDAO`, `DecodificheManagerBean`, `ProcAggregatiProcuraMittenteSqlDAO` |
| Occorrenze nel codice | 6 file |
| Sottosistema | Trasversale |

**Descrizione**: Stato del procedimento penale (473 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle viste di fascicolo e procedimento, per esporre in modo coerente stati, oggetti, posizioni ed esiti. La batch search basata su letterali in doppie virgolette ha rilevato 6 file Java; i principali sono `StatoProcedimentoDAO`, `FascicoloSiepOnViewSqlDAO`, `EventoSimeoneSqlDAO`, `DecodificheManagerBean`, `ProcAggregatiProcuraMittenteSqlDAO`.

### STATO_PROC_GENERICO

| Attributo | Valore |
|-----------|--------|
| N° valori | 50 |
| Categoria | STATI (STATO_*) |
| File Java principali | `ActUploadProvvedimentoGenerico` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Stato generico del procedimento. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle viste di fascicolo e procedimento, per esporre in modo coerente stati, oggetti, posizioni ed esiti. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `ActUploadProvvedimentoGenerico`.

### STATO_RICEZIONE_SIEPE

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | STATI (STATO_*) / SIEPE |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIEPE |

**Descrizione**: Stato di ricezione nel sottosistema SIEPE. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIEPE segnala un uso dedicato alle funzioni su permessi, licenze e attività istruttorie del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIEPE, in particolare per permessi, licenze, richieste e attività istruttorie. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### TENORE_DECISIONE_RICORSO

| Attributo | Valore |
|-----------|--------|
| N° valori | 14 |
| Categoria | ESITI (ESITO_* / TENORE_*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tenore/dispositivo della decisione sul ricorso. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TENORE_DECISIONE_RICORSO_SIGE

| Attributo | Valore |
|-----------|--------|
| N° valori | 14 |
| Categoria | ESITI (ESITO_* / TENORE_*) / SIGE |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIGE |

**Descrizione**: Tenore decisione ricorso nel sottosistema SIGE. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIGE evidenzia una specializzazione per la Gestione Esecuzione, con valori mirati alle lavorazioni del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIGE, soprattutto nelle funzioni di fascicolo, udienza, impugnazione e gestione dei provvedimenti esecutivi. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TENORE_ORDINANZA_PA

| Attributo | Valore |
|-----------|--------|
| N° valori | 6 |
| Categoria | ESITI (ESITO_* / TENORE_*) |
| File Java principali | `ActLoadInserisciPenaAccessoria`, `ActLoadInserisciEsecuzionePA`, `ActLoadComunicazione`, `ActLoadInserisciPenaAccessoria`, `ActLoadInserisciComunicazione` |
| Occorrenze nel codice | 6 file |
| Sottosistema | Trasversale |

**Descrizione**: Tenore dell'ordinanza della Procura/Presidenza dell'Assemblea. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search basata su letterali in doppie virgolette ha rilevato 6 file Java; i principali sono `ActLoadInserisciPenaAccessoria`, `ActLoadInserisciEsecuzionePA`, `ActLoadComunicazione`, `ActLoadInserisciPenaAccessoria`, `ActLoadInserisciComunicazione`.

### TIPO_ANNOTAZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 30 |
| Categoria | ALTRI DOMINI |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di annotazione inseribili nel fascicolo. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_ASSOLUZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | ALTRI DOMINI |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di assoluzione (es. per non aver commesso il fatto, perché il fatto non sussiste). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_ATTIVITA_SIEPE

| Attributo | Valore |
|-----------|--------|
| N° valori | 46 |
| Categoria | TIPI - Misure e Benefici / SIEPE |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIEPE |

**Descrizione**: Tipi di attività nel sottosistema SIEPE (permessi/licenze). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIEPE segnala un uso dedicato alle funzioni su permessi, licenze e attività istruttorie del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIEPE, in particolare per permessi, licenze, richieste e attività istruttorie. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### TIPO_ATTO

| Attributo | Valore |
|-----------|--------|
| N° valori | 14 |
| Categoria | TIPI - Registri e Atti |
| File Java principali | `DecodificheManagerBean`, `ActRicercaAttiVistiPerTipo`, `ActRicercaAttiPerTipoeDate`, `ActRicercaAttiPerSoggetto`, `ActRicercaAttiPerSIEPeSIUS` |
| Occorrenze nel codice | 6 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di atto giudiziario. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search basata su letterali in doppie virgolette ha rilevato 6 file Java; i principali sono `DecodificheManagerBean`, `ActRicercaAttiVistiPerTipo`, `ActRicercaAttiPerTipoeDate`, `ActRicercaAttiPerSoggetto`, `ActRicercaAttiPerSIEPeSIUS`.

### TIPO_ATTO_SIGE

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | TIPI - Registri e Atti / SIGE |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIGE |

**Descrizione**: Tipi di atto nel sottosistema SIGE. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIGE evidenzia una specializzazione per la Gestione Esecuzione, con valori mirati alle lavorazioni del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIGE, soprattutto nelle funzioni di fascicolo, udienza, impugnazione e gestione dei provvedimenti esecutivi. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### TIPO_AUTORITA

| Attributo | Valore |
|-----------|--------|
| N° valori | 121 |
| Categoria | TIPI - Uffici (TIPO_UFFICIO*) |
| File Java principali | `MisuraSicurezzaSqlDAO`, `DecodificheManagerBean`, `DecodificheManagerCore`, `ActLoadInserisciEsitoImpugnazioneSige`, `ActLoadInserisciRichiestaRemissioneDebito` |
| Occorrenze nel codice | 6 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di autorità giudiziarie/amministrative (121 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 6 file Java; i principali sono `MisuraSicurezzaSqlDAO`, `DecodificheManagerBean`, `DecodificheManagerCore`, `ActLoadInserisciEsitoImpugnazioneSige`, `ActLoadInserisciRichiestaRemissioneDebito`.

### TIPO_AUTORITA_VERBALE_ARRESTO

| Attributo | Valore |
|-----------|--------|
| N° valori | 6 |
| Categoria | TIPI - Uffici (TIPO_UFFICIO*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipo di autorità che redige il verbale di arresto. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_AVVOCATO

| Attributo | Valore |
|-----------|--------|
| N° valori | 4 |
| Categoria | TIPI - Soggetti e Ruoli |
| File Java principali | `NuovaIstanzaSqlDAO`, `NuovaIstanzaDAO`, `DecodificheManagerBean` |
| Occorrenze nel codice | 3 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipologia di avvocato (es. d'ufficio, di fiducia). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 3 file Java; i principali sono `NuovaIstanzaSqlDAO`, `NuovaIstanzaDAO`, `DecodificheManagerBean`.

### TIPO_BENEFICIO

| Attributo | Valore |
|-----------|--------|
| N° valori | 9 |
| Categoria | TIPI - Misure e Benefici |
| File Java principali | `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadBenefici`, `DecodificheManagerBean` |
| Occorrenze nel codice | 3 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di beneficio penitenziario (es. permesso premio, semilibertà, affidamento). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella gestione di benefici penitenziari, misure cautelari o di sicurezza, permessi, licenze e sospensioni. La batch search basata su letterali in doppie virgolette ha rilevato 3 file Java; i principali sono `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadBenefici`, `DecodificheManagerBean`.

### TIPO_CERTIFICATO

| Attributo | Valore |
|-----------|--------|
| N° valori | 10 |
| Categoria | TIPI - Registri e Atti |
| File Java principali | `ActLoadInserisciCertificatiComune`, `ActInserisciCertificatiComune` |
| Occorrenze nel codice | 2 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di certificato emettibile. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 2 file Java; i principali sono `ActLoadInserisciCertificatiComune`, `ActInserisciCertificatiComune`.

### TIPO_COMUNICAZIONE_PA

| Attributo | Valore |
|-----------|--------|
| N° valori | 7 |
| Categoria | ALTRI DOMINI |
| File Java principali | `ActPreLoadComunicazione`, `ActComunicazione`, `ActLoadComunicazione`, `ActLoadInserisciComunicazione` |
| Occorrenze nel codice | 4 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di comunicazione alle Pubbliche Autorità. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 4 file Java; i principali sono `ActPreLoadComunicazione`, `ActComunicazione`, `ActLoadComunicazione`, `ActLoadInserisciComunicazione`.

### TIPO_CONSEGUENZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 8 |
| Categoria | ALTRI DOMINI |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di conseguenza giuridica di un atto/decisione. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### TIPO_CONTINUAZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadContinuazione`, `DecodificheManagerBean` |
| Occorrenze nel codice | 3 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di continuazione nel reato continuato. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle funzioni di esecuzione pena, calcolo del presofferto, conversione, cumulo e trattamento delle sanzioni. La batch search basata su letterali in doppie virgolette ha rilevato 3 file Java; i principali sono `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadContinuazione`, `DecodificheManagerBean`.

### TIPO_CONTROLLO_ESECUZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | `DepositoDecretoSqlDAO`, `DepositoDecretoDAO`, `EveFasGepSogSenSqlDAO`, `EveFasGepSogDecSqlDAO`, `EveFasGepSogOrdSqlDAO` |
| Occorrenze nel codice | 7 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di controllo nell'esecuzione della pena. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 7 file Java; i principali sono `DepositoDecretoSqlDAO`, `DepositoDecretoDAO`, `EveFasGepSogSenSqlDAO`, `EveFasGepSogDecSqlDAO`, `EveFasGepSogOrdSqlDAO`.

### TIPO_CUMULO

| Attributo | Valore |
|-----------|--------|
| N° valori | 1 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di procedimento di cumulo pene. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nel procedimento di cumulo pene, sia nelle schermate di istruttoria sia nelle stampe e nei calcoli collegati. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_CURATORE

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Soggetti e Ruoli |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di curatore (per incapaci, minori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### TIPO_DECISIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 1 |
| Categoria | TIPI - Provvedimenti (TIPO_PROVVEDIMENTO*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di decisione giudiziaria. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_DECISIONE_CASSAZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 9 |
| Categoria | TIPI - Provvedimenti (TIPO_PROVVEDIMENTO*) |
| File Java principali | `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadSentenza`, `DecodificheManagerBean` |
| Occorrenze nel codice | 3 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di decisione della Corte di Cassazione. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search basata su letterali in doppie virgolette ha rilevato 3 file Java; i principali sono `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadSentenza`, `DecodificheManagerBean`.

### TIPO_DECISIONE_SORVEGLIANZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Provvedimenti (TIPO_PROVVEDIMENTO*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di decisione del Tribunale di Sorveglianza. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_DECRETO

| Attributo | Valore |
|-----------|--------|
| N° valori | 51 |
| Categoria | TIPI - Provvedimenti (TIPO_PROVVEDIMENTO*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di decreto (51 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_DEFINIZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 19 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | `PosizioneMaterialeFascSqlDAO`, `DecodificheManagerModel`, `ActLoadDefinizioneProcedimento`, `FascicoloSiepeDAO`, `FascicoloSiepeSqlDAO` |
| Occorrenze nel codice | 8 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di definizione del procedimento. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 8 file Java; i principali sono `PosizioneMaterialeFascSqlDAO`, `DecodificheManagerModel`, `ActLoadDefinizioneProcedimento`, `FascicoloSiepeDAO`, `FascicoloSiepeSqlDAO`.

### TIPO_DEFINIZIONE_SIEPE

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Procedure e Riti / SIEPE |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIEPE |

**Descrizione**: Tipi di definizione nel sottosistema SIEPE. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIEPE segnala un uso dedicato alle funzioni su permessi, licenze e attività istruttorie del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIEPE, in particolare per permessi, licenze, richieste e attività istruttorie. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### TIPO_DOCUMENTO_ALLEGATO

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | TIPI - Registri e Atti |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di documento allegabile al fascicolo. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_DURATA

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di durata (es. determinata, indeterminata). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_ELENCO_RICORSI

| Attributo | Valore |
|-----------|--------|
| N° valori | 2 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di elenco ricorsi. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_EMITTENTE

| Attributo | Valore |
|-----------|--------|
| N° valori | 6 |
| Categoria | TIPI - Registri e Atti |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di emittente dell'atto. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_EVENTO

| Attributo | Valore |
|-----------|--------|
| N° valori | 23 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di evento registrabile nel fascicolo. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_EVENTO_PERMESSO_LICENZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 8 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di evento relativo a permessi e licenze. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella gestione di benefici penitenziari, misure cautelari o di sicurezza, permessi, licenze e sospensioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### TIPO_FUNGIBILITA

| Attributo | Valore |
|-----------|--------|
| N° valori | 4 |
| Categoria | TIPI - Sanzioni (TIPO_SANZIONE*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di fungibilità delle pene. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_FUNZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 15 |
| Categoria | TIPI - Soggetti e Ruoli |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di funzione/ruolo nel sistema. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_GE

| Attributo | Valore |
|-----------|--------|
| N° valori | 6 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi nel modulo Gestione Esecuzione. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_GIUDIZIO_SIGE

| Attributo | Valore |
|-----------|--------|
| N° valori | 2 |
| Categoria | DOMINI SPECIFICI SOTTOSISTEMI / SIGE |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIGE |

**Descrizione**: Tipi di giudizio nel sottosistema SIGE. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIGE evidenzia una specializzazione per la Gestione Esecuzione, con valori mirati alle lavorazioni del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIGE, soprattutto nelle funzioni di fascicolo, udienza, impugnazione e gestione dei provvedimenti esecutivi. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### TIPO_INCARICO_SIEPE

| Attributo | Valore |
|-----------|--------|
| N° valori | 75 |
| Categoria | TIPI - Misure e Benefici / SIEPE |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIEPE |

**Descrizione**: Tipi di incarico nel sottosistema SIEPE (75 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIEPE segnala un uso dedicato alle funzioni su permessi, licenze e attività istruttorie del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIEPE, in particolare per permessi, licenze, richieste e attività istruttorie. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### TIPO_INTSOSP

| Attributo | Valore |
|-----------|--------|
| N° valori | 7 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di interruzione/sospensione pena. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella gestione di benefici penitenziari, misure cautelari o di sicurezza, permessi, licenze e sospensioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_ISTITUTO

| Attributo | Valore |
|-----------|--------|
| N° valori | 36 |
| Categoria | ANAGRAFICA E TERRITORIO |
| File Java principali | `DecodificheManagerBean`, `ProcAggregatiIstitutoDetenzioneSqlDAO` |
| Occorrenze nel codice | 2 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di istituto penitenziario o giudiziario. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 2 file Java; i principali sono `DecodificheManagerBean`, `ProcAggregatiIstitutoDetenzioneSqlDAO`.

### TIPO_LICENZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 14 |
| Categoria | TIPI - Misure e Benefici |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di licenza (es. licenza finale, licenza ordinaria, per i semiliberi). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella gestione di benefici penitenziari, misure cautelari o di sicurezza, permessi, licenze e sospensioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_MISURA_CAUTELARE

| Attributo | Valore |
|-----------|--------|
| N° valori | 17 |
| Categoria | TIPI - Misure e Benefici |
| File Java principali | `DecodificheManagerBean`, `DecodificheManagerCore` |
| Occorrenze nel codice | 2 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di misura cautelare (17 valori - es. custodia in carcere, arresti domiciliari, obblighi). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella gestione di benefici penitenziari, misure cautelari o di sicurezza, permessi, licenze e sospensioni. La batch search basata su letterali in doppie virgolette ha rilevato 2 file Java; i principali sono `DecodificheManagerBean`, `DecodificheManagerCore`.

### TIPO_MISURA_SICUREZZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 24 |
| Categoria | TIPI - Misure e Benefici |
| File Java principali | `TitoloEsecutivoController`, `ModuloCumuloController`, `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadMisuraSicurezza`, `DecodificheManagerBean` |
| Occorrenze nel codice | 6 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di misura di sicurezza (24 valori - es. OPG, casa di cura, libertà vigilata). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella gestione di benefici penitenziari, misure cautelari o di sicurezza, permessi, licenze e sospensioni. La batch search basata su letterali in doppie virgolette ha rilevato 6 file Java; i principali sono `TitoloEsecutivoController`, `ModuloCumuloController`, `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadMisuraSicurezza`, `DecodificheManagerBean`.

### TIPO_MITTENTE

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | TIPI - Registri e Atti |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di mittente degli atti. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_NOTIFICA

| Attributo | Valore |
|-----------|--------|
| N° valori | 18 |
| Categoria | TIPI - Registri e Atti |
| File Java principali | `ActInserisciRichRiesamePericoloSociale`, `DecodificheManagerBean`, `NotificheSiesDAO`, `NotificheSiesSqlDAO` |
| Occorrenze nel codice | 4 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di notifica giudiziaria. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 4 file Java; i principali sono `ActInserisciRichRiesamePericoloSociale`, `DecodificheManagerBean`, `NotificheSiesDAO`, `NotificheSiesSqlDAO`.

### TIPO_ORDINANZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 57 |
| Categoria | TIPI - Provvedimenti (TIPO_PROVVEDIMENTO*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di ordinanza (57 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_PENA_ACCESSORIA

| Attributo | Valore |
|-----------|--------|
| N° valori | 106 |
| Categoria | TIPI - Sanzioni (TIPO_SANZIONE*) |
| File Java principali | `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadPeneAccessorie`, `DecodificheManagerBean` |
| Occorrenze nel codice | 3 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di pena accessoria (106 valori - es. interdizione, decadenza dalla potestà). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle funzioni di esecuzione pena, calcolo del presofferto, conversione, cumulo e trattamento delle sanzioni. La batch search basata su letterali in doppie virgolette ha rilevato 3 file Java; i principali sono `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadPeneAccessorie`, `DecodificheManagerBean`.

### TIPO_PENA_DETENTIVA

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | TIPI - Sanzioni (TIPO_SANZIONE*) |
| File Java principali | `ActNscToSiesLoadReato`, `ActNscToSiesLoadPenaComplessiva`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean` |
| Occorrenze nel codice | 4 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di pena detentiva (es. reclusione, arresto). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle funzioni di esecuzione pena, calcolo del presofferto, conversione, cumulo e trattamento delle sanzioni. La batch search basata su letterali in doppie virgolette ha rilevato 4 file Java; i principali sono `ActNscToSiesLoadReato`, `ActNscToSiesLoadPenaComplessiva`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean`.

### TIPO_PERMESSO

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Misure e Benefici |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di permesso (es. permesso premio, permesso umanitario, permesso di necessità). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella gestione di benefici penitenziari, misure cautelari o di sicurezza, permessi, licenze e sospensioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_POS_LIBERO

| Attributo | Valore |
|-----------|--------|
| N° valori | 2 |
| Categoria | TIPI - Misure e Benefici |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di posizione libero (es. in libertà, misura alternativa). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_PRESCRIZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 39 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di prescrizione (39 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### TIPO_PROVVEDIMENTO

| Attributo | Valore |
|-----------|--------|
| N° valori | 57 |
| Categoria | TIPI - Provvedimenti (TIPO_PROVVEDIMENTO*) |
| File Java principali | `MisuraSicurezzaSqlDAO`, `ActNscToSiesLoadCircostanze`, `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadSentenza`, `DecodificheManagerBean` |
| Occorrenze nel codice | 6 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di provvedimento giudiziario (57 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search basata su letterali in doppie virgolette ha rilevato 6 file Java; i principali sono `MisuraSicurezzaSqlDAO`, `ActNscToSiesLoadCircostanze`, `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadSentenza`, `DecodificheManagerBean`.

### TIPO_PROVVEDIMENTO_ARC

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Provvedimenti (TIPO_PROVVEDIMENTO*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di provvedimento per archiviazione. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_PROVVEDIMENTO_RIF

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Provvedimenti (TIPO_PROVVEDIMENTO*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di provvedimento di riferimento. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_PROVVEDIMENTO_RIF_P

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | TIPI - Provvedimenti (TIPO_PROVVEDIMENTO*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di provvedimento di riferimento per PM. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_PROVVEDIMENTO_RIF_PG

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Provvedimenti (TIPO_PROVVEDIMENTO*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di provvedimento di riferimento per PG. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_PROVVEDIMENTO_SIGE

| Attributo | Valore |
|-----------|--------|
| N° valori | 25 |
| Categoria | TIPI - Provvedimenti (TIPO_PROVVEDIMENTO*) / SIGE |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIGE |

**Descrizione**: Tipi di provvedimento nel sottosistema SIGE. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIGE evidenzia una specializzazione per la Gestione Esecuzione, con valori mirati alle lavorazioni del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIGE, soprattutto nelle funzioni di fascicolo, udienza, impugnazione e gestione dei provvedimenti esecutivi. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### TIPO_RATEIZZAZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 2 |
| Categoria | ALTRI DOMINI |
| File Java principali | `RateizzazionePPSqlDAO`, `RicercaStatoPagamentiSqlDao`, `RateizzazionePPDAO`, `BollettinoPagopaDAO`, `BollettinoPagopaSqlDAO` |
| Occorrenze nel codice | 6 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di rateizzazione delle pene pecuniarie. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 6 file Java; i principali sono `RateizzazionePPSqlDAO`, `RicercaStatoPagamentiSqlDao`, `RateizzazionePPDAO`, `BollettinoPagopaDAO`, `BollettinoPagopaSqlDAO`.

### TIPO_REATO

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | ALTRI DOMINI |
| File Java principali | `ActNscToSiesLoadReato`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean` |
| Occorrenze nel codice | 3 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di reato (es. delitto, contravvenzione). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle funzioni di esecuzione pena, calcolo del presofferto, conversione, cumulo e trattamento delle sanzioni. La batch search basata su letterali in doppie virgolette ha rilevato 3 file Java; i principali sono `ActNscToSiesLoadReato`, `ActPrelevaDatiFascicolo`, `DecodificheManagerBean`.

### TIPO_REGISTRO

| Attributo | Valore |
|-----------|--------|
| N° valori | 26 |
| Categoria | TIPI - Registri e Atti |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di registro giudiziario. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_REGISTRO_ORDINANZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 4 |
| Categoria | TIPI - Registri e Atti |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di registro per le ordinanze. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_REG_GEN

| Attributo | Valore |
|-----------|--------|
| N° valori | 8 |
| Categoria | TIPI - Registri e Atti |
| File Java principali | `DecretoOrdinanzaSiepSqlDAO`, `DecretoOrdinanzaSiepDAO`, `ContinuazioneCumuloDAO`, `TitoloCumulatoDAO`, `ContinuazioneCumuloSqlDAO` |
| Occorrenze nel codice | 7 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di registro generale. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 7 file Java; i principali sono `DecretoOrdinanzaSiepSqlDAO`, `DecretoOrdinanzaSiepDAO`, `ContinuazioneCumuloDAO`, `TitoloCumulatoDAO`, `ContinuazioneCumuloSqlDAO`.

### TIPO_RESIDENZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Misure e Benefici |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di residenza del soggetto. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle anagrafiche di soggetti, difensori, residenze e sedi territoriali. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_RICHIEDENTE_SIEPE

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | TIPI - Soggetti e Ruoli / SIEPE |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIEPE |

**Descrizione**: Tipi di richiedente nel sottosistema SIEPE. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIEPE segnala un uso dedicato alle funzioni su permessi, licenze e attività istruttorie del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIEPE, in particolare per permessi, licenze, richieste e attività istruttorie. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### TIPO_RICHIEDENTE_SIGE

| Attributo | Valore |
|-----------|--------|
| N° valori | 52 |
| Categoria | TIPI - Soggetti e Ruoli / SIGE |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIGE |

**Descrizione**: Tipi di richiedente nel sottosistema SIGE (52 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIGE evidenzia una specializzazione per la Gestione Esecuzione, con valori mirati alle lavorazioni del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIGE, soprattutto nelle funzioni di fascicolo, udienza, impugnazione e gestione dei provvedimenti esecutivi. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### TIPO_RICHIESTA_CUMULO

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di richiesta nel procedimento di cumulo. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nel procedimento di cumulo pene, sia nelle schermate di istruttoria sia nelle stampe e nei calcoli collegati. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_RICHIESTA_GE

| Attributo | Valore |
|-----------|--------|
| N° valori | 9 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | `ActPreLoadRichiestaGE`, `ActLoadInserisciRichiestaGE`, `ActLoadRichiestaGE`, `ActRichiestaGE` |
| Occorrenze nel codice | 4 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di richiesta nella Gestione Esecuzione. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle schermate di acquisizione e lavorazione di istanze e richieste istruttorie. La batch search basata su letterali in doppie virgolette ha rilevato 4 file Java; i principali sono `ActPreLoadRichiestaGE`, `ActLoadInserisciRichiestaGE`, `ActLoadRichiestaGE`, `ActRichiestaGE`.

### TIPO_RICHIESTA_SIEPE

| Attributo | Valore |
|-----------|--------|
| N° valori | 11 |
| Categoria | TIPI - Procedure e Riti / SIEPE |
| File Java principali | `DecodificheManagerModel` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIEPE |

**Descrizione**: Tipi di richiesta nel sottosistema SIEPE. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIEPE segnala un uso dedicato alle funzioni su permessi, licenze e attività istruttorie del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIEPE, in particolare per permessi, licenze, richieste e attività istruttorie. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerModel`.

### TIPO_RICORSO

| Attributo | Valore |
|-----------|--------|
| N° valori | 4 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di ricorso (es. appello, cassazione, riesame). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_RICORSO_SIGE

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Procedure e Riti / SIGE |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | SIGE |

**Descrizione**: Tipi di ricorso nel sottosistema SIGE. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto. Il suffisso SIGE evidenzia una specializzazione per la Gestione Esecuzione, con valori mirati alle lavorazioni del relativo sottosistema.

**Utilizzo applicativo**: È usato nel sottosistema SIGE, soprattutto nelle funzioni di fascicolo, udienza, impugnazione e gestione dei provvedimenti esecutivi. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_RINNOVO

| Attributo | Valore |
|-----------|--------|
| N° valori | 10 |
| Categoria | ALTRI DOMINI |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di rinnovo (es. di permesso, di misura alternativa). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_RITO

| Attributo | Valore |
|-----------|--------|
| N° valori | 6 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di rito processuale (es. ordinario, abbreviato, patteggiamento). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_RITO_SENTENZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipo di rito risultante dalla sentenza. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_SANZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Sanzioni (TIPO_SANZIONE*) |
| File Java principali | `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadSostituzionePene`, `DecodificheManagerBean` |
| Occorrenze nel codice | 3 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di sanzione penale. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle funzioni di esecuzione pena, calcolo del presofferto, conversione, cumulo e trattamento delle sanzioni. La batch search basata su letterali in doppie virgolette ha rilevato 3 file Java; i principali sono `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadSostituzionePene`, `DecodificheManagerBean`.

### TIPO_SANZIONE_AMMINISTRATIVA

| Attributo | Valore |
|-----------|--------|
| N° valori | 14 |
| Categoria | TIPI - Sanzioni (TIPO_SANZIONE*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di sanzione amministrativa. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle funzioni di esecuzione pena, calcolo del presofferto, conversione, cumulo e trattamento delle sanzioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_SANZIONE_CONVERTITA

| Attributo | Valore |
|-----------|--------|
| N° valori | 7 |
| Categoria | TIPI - Sanzioni (TIPO_SANZIONE*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di sanzione convertita. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle funzioni di esecuzione pena, calcolo del presofferto, conversione, cumulo e trattamento delle sanzioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_SANZIONE_SOSTITUTIVA

| Attributo | Valore |
|-----------|--------|
| N° valori | 9 |
| Categoria | TIPI - Sanzioni (TIPO_SANZIONE*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di sanzione sostitutiva. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle funzioni di esecuzione pena, calcolo del presofferto, conversione, cumulo e trattamento delle sanzioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_SANZIONE_SOSTITUTIVA_LPU

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Sanzioni (TIPO_SANZIONE*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di sanzione sostitutiva con lavoro di pubblica utilità. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle funzioni di esecuzione pena, calcolo del presofferto, conversione, cumulo e trattamento delle sanzioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_SCADENZARIO

| Attributo | Valore |
|-----------|--------|
| N° valori | 28 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di scadenzario/agenda nel sistema. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_SENTENZA

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | TIPI - Provvedimenti (TIPO_PROVVEDIMENTO*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di sentenza (es. condanna, assoluzione, patteggiamento). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_SOSPENSIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di sospensione dell'esecuzione. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_SOSP_SUBORDINATA

| Attributo | Valore |
|-----------|--------|
| N° valori | 9 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadBenefici`, `DecodificheManagerBean` |
| Occorrenze nel codice | 3 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di sospensione subordinata. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 3 file Java; i principali sono `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadBenefici`, `DecodificheManagerBean`.

### TIPO_TRASMISSIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Registri e Atti |
| File Java principali | `TrasmissioniSqlDAO`, `TrasmissioniDAO`, `DecodificheManagerBean`, `StatoPrenotazioniBdmcDAO`, `StatoPrenotazioniBdmcSqlDAO` |
| Occorrenze nel codice | 5 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di trasmissione degli atti. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 5 file Java; i principali sono `TrasmissioniSqlDAO`, `TrasmissioniDAO`, `DecodificheManagerBean`, `StatoPrenotazioniBdmcDAO`, `StatoPrenotazioniBdmcSqlDAO`.

### TIPO_TUTORE

| Attributo | Valore |
|-----------|--------|
| N° valori | 3 |
| Categoria | TIPI - Soggetti e Ruoli |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di tutore legale. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_UFFICIO

| Attributo | Valore |
|-----------|--------|
| N° valori | 59 |
| Categoria | TIPI - Uffici (TIPO_UFFICIO*) |
| File Java principali | `IstruttoriaController`, `ActLoadTrasferisciNuovaIstanza`, `FascicoloSiepSqlDAO`, `ActLoadListaProvvedimentiTrasmessi`, `ActLoadTrasferisciProvvedimentoL78del2013` |
| Occorrenze nel codice | 24 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di ufficio giudiziario (59 valori - es. Tribunale, Procura, Corte d'Appello). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 24 file Java; i principali sono `IstruttoriaController`, `ActLoadTrasferisciNuovaIstanza`, `FascicoloSiepSqlDAO`, `ActLoadListaProvvedimentiTrasmessi`, `ActLoadTrasferisciProvvedimentoL78del2013`.

### TIPO_UFFICIO_CUMULO

| Attributo | Valore |
|-----------|--------|
| N° valori | 31 |
| Categoria | TIPI - Uffici (TIPO_UFFICIO*) |
| File Java principali | `DecodificheManagerBean`, `ActLoadInserisciDataDepositoDecreto` |
| Occorrenze nel codice | 2 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di ufficio nel procedimento di cumulo. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nel procedimento di cumulo pene, sia nelle schermate di istruttoria sia nelle stampe e nei calcoli collegati. La batch search basata su letterali in doppie virgolette ha rilevato 2 file Java; i principali sono `DecodificheManagerBean`, `ActLoadInserisciDataDepositoDecreto`.

### TIPO_UFFICIO_DEFI

| Attributo | Valore |
|-----------|--------|
| N° valori | 31 |
| Categoria | TIPI - Uffici (TIPO_UFFICIO*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di ufficio per la definizione del procedimento. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_UFFICIO_EMITTENTE

| Attributo | Valore |
|-----------|--------|
| N° valori | 27 |
| Categoria | TIPI - Uffici (TIPO_UFFICIO*) |
| File Java principali | `DatiFinaliCumuloController`, `ActLoadDettaglioAnnotazioneRevoca`, `ActLoadDettaglioRichiestaRevoca`, `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadRevoche` |
| Occorrenze nel codice | 8 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di ufficio emittente dell'atto. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 8 file Java; i principali sono `DatiFinaliCumuloController`, `ActLoadDettaglioAnnotazioneRevoca`, `ActLoadDettaglioRichiestaRevoca`, `ActPrelevaDatiFascicolo`, `ActNscToSiesLoadRevoche`.

### TIPO_UFFICIO_GE

| Attributo | Valore |
|-----------|--------|
| N° valori | 12 |
| Categoria | TIPI - Uffici (TIPO_UFFICIO*) |
| File Java principali | `DecodificheManagerBean`, `DecodificheManagerCore` |
| Occorrenze nel codice | 2 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di ufficio nella Gestione Esecuzione. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 2 file Java; i principali sono `DecodificheManagerBean`, `DecodificheManagerCore`.

### TIPO_UFFICIO_PM

| Attributo | Valore |
|-----------|--------|
| N° valori | 9 |
| Categoria | TIPI - Uffici (TIPO_UFFICIO*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di ufficio del Pubblico Ministero. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_UFFICIO_REGE

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | TIPI - Uffici (TIPO_UFFICIO*) |
| File Java principali | `RegeDecodificheManager` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di ufficio nel modulo REGE. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `RegeDecodificheManager`.

### TIPO_UFFICIO_RPA

| Attributo | Valore |
|-----------|--------|
| N° valori | 31 |
| Categoria | TIPI - Uffici (TIPO_UFFICIO*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di ufficio per la ricezione/produzione atti. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.

### TIPO_UFFICIO_SCARCERAZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 5 |
| Categoria | TIPI - Uffici (TIPO_UFFICIO*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di ufficio per la scarcerazione. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_UFFICIO_SOSP

| Attributo | Valore |
|-----------|--------|
| N° valori | 27 |
| Categoria | TIPI - Uffici (TIPO_UFFICIO*) |
| File Java principali | `ActLoadInserisciSospensioneEsecPenaDispPm`, `DecodificheManagerBean`, `DecodificheController` |
| Occorrenze nel codice | 3 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di ufficio per la sospensione. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 3 file Java; i principali sono `ActLoadInserisciSospensioneEsecPenaDispPm`, `DecodificheManagerBean`, `DecodificheController`.

### TIPO_ULTERIORE_SANZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 13 |
| Categoria | TIPI - Sanzioni (TIPO_SANZIONE*) |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di ulteriore sanzione applicata. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nelle funzioni di esecuzione pena, calcolo del presofferto, conversione, cumulo e trattamento delle sanzioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_VERBALE

| Attributo | Valore |
|-----------|--------|
| N° valori | 9 |
| Categoria | TIPI - Registri e Atti |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di verbale (es. verbale di arresto, di interrogatorio). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella formazione, ricerca e classificazione di atti, provvedimenti, ricorsi e registri del fascicolo. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### TIPO_VISUALIZZAZIONE

| Attributo | Valore |
|-----------|--------|
| N° valori | 6 |
| Categoria | TIPI - Procedure e Riti |
| File Java principali | — (nessuna occorrenza letterale con la batch search) |
| Occorrenze nel codice | 0 file |
| Sottosistema | Trasversale |

**Descrizione**: Tipi di visualizzazione/modalità di presentazione dati. Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato trasversalmente nei moduli SIES che richiedono codifiche controllate per combo, filtri, report e integrazioni. La batch search non ha trovato riferimenti letterali in doppie virgolette, ma il dominio è coerente con un consumo indiretto tramite `IDecodifiche`/`DecodificheDAO` oppure con join SQL su `CG_REF_CODES` espressi con apici singoli.

### UFFICIO_LOGIN

| Attributo | Valore |
|-----------|--------|
| N° valori | 23 |
| Categoria | TIPI - Uffici (TIPO_UFFICIO*) |
| File Java principali | `DecodificheManagerBean` |
| Occorrenze nel codice | 1 file |
| Sottosistema | Trasversale |

**Descrizione**: Uffici abilitati al login nel sistema (23 valori). Il dominio raccoglie coppie codice/descrizione riusate tra DAO, action/controller, ricerche, stampe e flussi di integrazione, così da evitare enumerazioni hard-coded sparse nel progetto.

**Utilizzo applicativo**: È usato nella classificazione di uffici, autorità, mittenti/destinatari e flussi di notifica o trasmissione degli atti. La batch search basata su letterali in doppie virgolette ha rilevato 1 file Java; i principali sono `DecodificheManagerBean`.