---
uniqueName: siepinterventoparte2xxxversione0102015011616-00
displayName: "Siep intervento parte 2 xxx versione 0 1 0 2015 01 16 16 00"
category: "GENERAL"
tags: []
---

# Siep_intervento_parte_2_xxx_versione_0_1_0_2015_01_16_16.00

> **File originale:** `MEV/Mev10/Siep_intervento_parte_2_xxx_versione_0_1_0_2015_01_16_16.00.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia |
| --- |


Analisi funzionale Mev SIEP
Siep per gli uffici giudiziari dei minorenni
Parte


Codice documento:SIEP_PNL_AF
|  | Versione 0.1 Data |
| --- | --- |
|  |  |



| Titolo | Analisi funzionale Mev SIEP |
| --- | --- |
| Codice doc | SIEP_PNL_AF |
| Versione | 0.1 |



|  | Nome | Data |
| --- | --- | --- |
| Autore/i | Salvatore Sapienza |  |
| Verificato |  |  |
| Responsabile |  |  |
| Cliente e/o utenti |  |  |
| Direzione |  |  |


Revisioni
| Data | Versione | Autore/i | Descrizione |
| --- | --- | --- | --- |
| 26/11/2014 | 0.1 |  | Versione iniziale |
|  |  |  |  |
|  |  |  |  |


Riferimenti
| Rif. | Documento | Nota |
| --- | --- | --- |
|  | documento analisi 16_07_14.doc |  |
|  | Elenco uffici minorili.xls |  |
|  | Prototipo SIES- Server: Torino–Versione: 8.0 |  |



Allegati:
| Rif. | Documento | Nota |
| --- | --- | --- |
|  | SIEP_MA_ARDOM_SOSP_PROC.RTF |  |
|  | SIEP_MA_ ARDOM_SOSP_MDS.RTF |  |
|  | SIEP_MA_ ARDOM_RIPR_MDS.RTF |  |
|  | SIEP_MA_ ARDOM_RIPR_MDS_PROC.RTF |  |
|  | SIEP_MA_ ARDOM_RIPR_ TDS.RTF |  |
|  | SIEP_MA_ ARDOM_RIPR_TDS_PROC.RTF |  |
|  | SIEP_MA_ARDOM_REVO_DIRETTA.RTF |  |
|  | SIEP_MA_ARDOM_REVO_SOSPENSIONE.RTF |  |
|  | 16_Posizione_giuridica_iniziale.rar |  |
|  | 17_arresti domiciliari art. 626 comma 10 |  |








# Sommario
Sommario	4
Indice figure	5
Indice tabelle	8
Introduzione	11
Elenco degli interventi	12
Legenda colori	13
Convenzioni tipografiche	13
Questioni aperte	13
15	Tabella posizioni giuridiche iniziali	14
15.1	Intervento richiesto dall’Amministrazione	14
15.2	Situazione attuale	14
15.3	Descrizione dell’intervento	14
15.4	Riferimenti	14
15.5	Sottosistema	14
15.6	Uffici	14
15.7	Modifica funzionalità	15
15.8	Modifica interfacce utente	15
15.9	Modifica interfacce software/algoritmi	15
15.10	Modifica database	15
15.11	Modifica template	15
16	Gestione posizione giuridica iniziale	15
16.1	Intervento richiesto dall’Amministrazione	15
16.2	Situazione attuale	15
16.3	Descrizione dell’intervento	15
16.4	Riferimenti	22
16.5	Sottosistema	22
16.6	Uffici	22
16.7	Modifica funzionalità	22
16.8	Modifica interfacce utente	22
16.9	Modifica interfacce software/algoritmi	24
16.10	Modifica database	29
16.11	Modifica template	30
17	Decisione sorveglianza – Arresti domiciliari ex 656 comma 10°	31
17.1	Intervento richiesto dall’Amministrazione	31
17.2	Situazione attuale	33
17.3	Descrizione dell’intervento	33
17.4	Riferimenti	44
17.5	Sottosistema	44
17.6	Uffici	45
17.7	Modifiche  previste	45
17.8	Modifica funzionalità	45
17.9	Modifica interfacce utente	45
17.10	Modifica interfacce software/algoritmi	50
17.11	Modifica database	62
17.12	Modifica template	69
18	Gestione Provvedimenti emessi dalla Magistratura di Sorveglianza	69
18.1	Intervento richiesto dall’Amministrazione	69
18.2	Situazione attuale	69
18.3	Descrizione dell’intervento	70
18.4	Riferimenti	83
18.5	Sottosistema	83
18.6	Uffici	84
18.7	Modifica interfacce utente	84
18.8	Modifica funzionalità	84
18.9	Modifica interfacce software/algoritmi	84
18.10	Modifica database	95
18.11	Modifica template	104
# Indice figure
Figura 1 - Punto accesso Iscrizione posizione giuridica	17
Figura 2 - Punto di accesso Elenco Posizioni Giuridiche	18
Figura 3 - Elenco Posizioni Giuridiche	18
Figura 4 - Maschera posizione libero	19
Figura 5 - Maschera Espiazione pena in istituto di detenzione	19
Figura 6 - Maschera Espiazione pena in altro luogo	20
Figura 7 - Maschera libero – Definitiva in istituto di detenzione	20
Figura 8 - Maschera libero – misura cautelare in istituto detenzione	21
Figura 9 - Maschera libero – misura cautelare in altro luogo	21
Figura 10 - Diagramma navigazione	22
Figura 11 - Sezione A	22
Figura 12 - Sezione B	22
Figura 13 - Sezione C	23
Figura 14 - Sezione D	23
Figura 15 - Sezione E - Libero – Detenuto Altra Causa – Definitivo in Istituto	23
Figura 16 - Sezione F - Libero – Detenuto Altra Causa – Misura cautelare in Istituto	23
Figura 17 - Sezione G – Libero – Detenuto Altra Causa – Misura cautelare in Altro Luogo	23
Figura 18 - Sezione H - Espiazione Pena in Istituto di Detenzione	24
Figura 19 - Sezione I - Espiazione Pena in Altro Luogo	24
Figura 20 - Sezione L	24
Figura 21 - Decisioni Sorveglianza	34
Figura 22 - Decisioni Sorveglianza	34
Figura 23 - Inserimento arresti domiciliari	35
Figura 24 - Sospensione provvisoria Arresti Domiciliari – Eseguita Procura	35
Figura 25 - Sospensione provvisoria Arresti Domiciliari – Eseguita Magistrato di Sorveglianza	36
Figura 26 - Revoca Arresti Domiciliari  e Rigetta applicazione misura alternativa - Revoca diretta	37
Figura 27 - Revoca Arresti Domiciliari  e Rigetta applicazione misura alternativa - Revoca dopo sospensione	38
Figura 28 - Ripristino Degli Arresti Domiciliari – Eseguita Procura	39
Figura 29 - Ripristino Degli Arresti Domiciliari – Eseguita Sorveglianza	40
Figura 30 - Dettaglio procedimento - Elenco provvedimenti Sorveglianza	44
Figura 31 - Elenco provvedimenti	44
Figura 32 – Sezione A - Funzione sospensione provvisoria	46
Figura 33 – Sezione B - Funzione revoca	46
Figura 34 – Sezione C - Funzione ripristino	46
Figura 35 – Sezione D - Dati salienti procedimento	46
Figura 36 – Sezione E - Dati posizione giuridica	46
Figura 37 – Sezione F - Dati pena complessiva	47
Figura 38 - Sezione G - Dati inzio e fine pena	47
Figura 39 – Sezione H - Ordinanza revoca	47
Figura 40 – Sezione I – Decreto Sospensione	47
Figura 41 – Sezione L – Ordinanza/Decreto ripristino	48
Figura 42 – Sezione M - Magistrato firmatario	48
Figura 43 – Sezione N - Destinatari ordinanza revoca diretta	48
Figura 44 – Sezione O - Destinatari ordinanza revoca dopo sospensione	48
Figura 45 – Sezione P - Destinatari decreto Sospensione – Eseguita Procura	49
Figura 46 – Sezione Q - Destinatari decreto – Eseguita Magistrato di Sorveglianza	49
Figura 47 – Sezione R - Destinatari ordinanza ripristino – Eseguita Procura	49
Figura 48 – Sezione S - Destinatari ordinanza ripristino – Eseguita Sorveglianza	49
Figura 49 – Sezione T - Destinatari per la notifica	50
Figura 50 – Sezione U - Conferma	50
Figura 51 – Diagramma inserimento decreto sospensione	59
Figura 52 – Diagramma inserimento ordinanza revoca	60
Figura 53 – Diagramma inserimento ordinanza ripristino	60
Figura 54 - Dettaglio maschera decisione della sorveglianza	69
Figura 55 -  Selezione Decisioni Sorveglianza	70
Figura 56 - Decisioni Sorveglianza	71
Figura 57 – Attuale ufficio emittente prevalorizzato	72
Figura 58 - Autorità Emittente	72
Figura 59 – Attuale ufficio emittente modificabile	72
Figura 60 - Autorità Emittente	72
Figura 61 – Ufficio emittente modificabile	73
Figura 62 – Autorità emittente modificabile	73
Figura 63 - Attuale UEPE	73
Figura 64 - USSM per i minorenni	73
Figura 65 – attuale etichetta UEPE	73
Figura 66 - Ricerca UEPE	74
Figura 67 - Attuale Ufficio di Sorveglianza	74
Figura 68 - Attuale Ufficio di Sorveglianza	75
Figura 69 - Magistrato di Sorveglianza per i minorenni	75
Figura 70 -  Funzione selezione ufficio di sorveglianza	75
Figura 71 - Attuale Tribunale di sorveglianza	76
Figura 72 -  Tribunale per i  Minorenni in funzione di Tribunale di Sorveglianza	76
Figura 73 -  Funzione selezione Tribunale di sorveglianza	76
Figura 74 - Autorità competente per territorio	77
Figura 75 - Autorità destinazione	77
Figura 76 - Destinatario per esecuzione	77
Figura 77 - Destinatario per esecuzione	78
Figura 78 - Autorità per la Restituzione	78
Figura 79 -  Magistrato firmatario	78
Figura 80 - Dettaglio	83

# Indice tabelle
Tabella 1 - Giudici della cognizione	11
Tabella 2 - Giudici dell'esecuzione	11
Tabella 3 - Magistratura di Sorveglianza	12
Tabella 4 - Tabella <CG_REF_CODES>	15
Tabella 5 - Elenco posizioni giuridiche iniziali	16
Tabella 6 - Elenco misure	17
Tabella 7 – Interfaccia - Sezione C – Libero	24
Tabella 8 – Interfaccia - Sezione E – Libero – Altra causa – Definitivo in Istituto	25
Tabella 9 – Interfaccia - Sezione F - Libero – Altra causa – Misura cautelare in Istituto	26
Tabella 10 – Interfaccia - Sezione G - Libero – Altra causa – Misura cautelare in Altro luogo	28
Tabella 11 – Interfaccia – Sezione H	28
Tabella 12 – Interfaccia – Sezione I	28
Tabella 13 – Interfaccia – Sezione L	28
Tabella 14 - Schema riepilogativo	29
Tabella 15 - Tabella MISURA_CAUTELARE nuova colonna	29
Tabella 16 – Tabella <POSIZIONE_GIURIDICA> nuove colonne	30
Tabella 17 – Tabella <CG_REF_CODES> Tipo misura cautelare	30
Tabella 18 – Nuovi template	41
Tabella 19 – Posizione giuridica finale	42
Tabella 20 - Stato Procedimento	43
Tabella 21 – Sezione A – Funzione sospensione provvisoria	50
Tabella 22 – Sezione B – Funzione revoca	50
Tabella 23 – Sezione C – Funzione ripristino	50
Tabella 24 – Sezione D – Dati salienti procedimento	50
Tabella 25 – Sezione E – Posizione giuridica iniziale	51
Tabella 26 – Sezione F – Dati pena complessiva	51
Tabella 27 – Sezione G – Dati inizio e fine pena	51
Tabella 28 – Sezione H - Ordinanza revoca	52
Tabella 29 – Sezione I – Decreto Sospensione	53
Tabella 30 –  Sezione L – Ordinanza/Decreto ripristino	54
Tabella 31 –  Sezione M - Magistrato firmatario	54
Tabella 32 –  Sezione N - Destinatari ordinanza Revoca diretta	54
Tabella 33 –  Sezione N - Destinatari ordinanza Revoca diretta	55
Tabella 34 –  Sezione O - Destinatari ordinanza Revoca dopo Sospensione	55
Tabella 35 –  Sezione P - Destinatari decreto Sospensione – Eseguita Procura	56
Tabella 36 –  Sezione Q - Destinatari decreto Sospensione – Eseguita Magistrato di Sorveglianza	56
Tabella 37 –  Sezione R- Destinatari ordinanza di ripristino – Eseguita Procura	57
Tabella 38 –  Sezione S- Destinatari ordinanza di ripristino – Eseguita Sorveglianza	58
Tabella 39 –  Sezione T - Destinatari per notifica	58
Tabella 40 - Valorizzazione tabella <Notifica>	61
Tabella 41 - Valorizzazione <COD_TIPO_NOTIFICA>	62
Tabella 42 - Tabella <CG_REF_CODES>-Decreto sospensione	62
Tabella 43 - Tabella <CG_REF_CODES>- Ordinanza revoca	62
Tabella 44 - Tabella <CG_REF_CODES>- Ordinanza/decreto  ripristino	63
Tabella 45 - Tabella <CG_REF_CODES> Posizione giuridica	64
Tabella 46 - Tabella <CG_REF_CODES> Stato procedimento	65
Tabella 47 - Tabella <CG_REF_CODES> Nome provvedimento	66
Tabella 48 - Tabella <TEMPLATE> Nuovi modelli	68
Tabella 49 - Tabella <CG_REF_CODES> TIPO_UFFICIO	68
Tabella 50- Maschere decisione sorveglianza	82
Tabella 51 - Ufficio Emittente	84
Tabella 52 – UEPE / USSM	84
Tabella 53 – Ufficio di Sorveglianza / Magistrato di Sorveglianza per i Minorenni	84
Tabella 54 – Tribunale di Sorveglianza / Tribunale per i  Minorenni in funzione di Tribunale di Sorveglianza	85
Tabella 55- Elenco Istituti detentivi minorili	86
Tabella 56 - Nuovo elenco Istituti detentivi minorili	87
Tabella 57 - Elenco Procure presso Tribunale per i minorenni	88
Tabella 58 - Nuovo elenco Procure presso Tribunale per i minorenni	89
Tabella 59 - Elenco Tribunali per i minorenni	91
Tabella 60 – Nuovo elenco Tribunali per i minorenni	92
Tabella 61 - Elenco Uffici Servizi Sociali Minorenni	93
Tabella 62 - Elenco Uffici Servizi Sociali Minorenni sedi distaccate	94
Tabella 63 - Nuovo record istituto minorile	95
Tabella 64 – Tabella <UFFICIO> - riferimenti aggiornati UEPE  Vibo Valentia	96
Tabella 65 - Tabella <CSSA> - riferimenti aggiornati UEPE  Vibo Valentia	96
Tabella 66 – Tabella <UFFICIO> - USSM	98
Tabella 67 – USSM – Sedi distaccate	99
Tabella 68 – Tabella <CSSA> - USSM	102
Tabella 69 – Tabella <CSSA> - USSMSS	104
Tabella 70 - Tabella <CG_REG_CODES>	104



# Introduzione
Le immagini contenute nel presente documento sono estratte dal sistema tramite un’utenza della Procura della Repubblica presso il Tribunale ordinario, ma gli interventi previsti riguardano gli uffici giudiziari minorili e qualche volta gli uffici giudiziari dei maggiorenni del sistema SIEP.
Per ciascuno intervento vengono riportate
le richieste del Referente nel paragrafo “Intervento richiesto” dei vari capitoli,
la descrizione dell’intervento con la soluzione proposta,
le modifiche alle interfacce utente, agli algoritmi e alla struttura del database.
Il presente documento riporta suddivisi in capitoli gli interventi richiesti dall’Amministrazione nel documento “documento analisi 16_07_14.doc”.
L’intervento richiesto è descritto di volta in volta nei vari paragrafi “Intervento richiesto”.
Gli interventi richiesti dall’Amministrazione sono stati suddivisi in due parti.
Il presente documento contiene la prima parte degli interventi.
Le immagini sono presenti a titolo esemplificativo e suggeriscono al lettore come potrebbero apparire le interfacce utente dopo l’intervento manutentivo.
Nella realizzazione e nella modifica delle interfacce si deve tener conto degli standard grafici e delle convenzioni adottate in precedenza e presenti nel progetto.
Per le attività di analisi il sistema di riferimento è stato quello installato come prototipo SIES – Server: Torino- Versione: 8.0.

| Giudice di cognizione | Giudice di cognizione | Giudice di cognizione |
| --- | --- | --- |
| Gradi di Giudizio | Giudice | Pubblico Ministero |
| I | Tribunale Minorenni | Procura Repubblica  per i Minorenni |
| Appello | Sezione Corte Appello Minorenni | Procura Generale presso la Corte di Appello |
| Ricorso | Corte  Suprema di Cassazione | Procura Generale presso la Corte di Cassazione |

Tabella 1 - Giudici della cognizione
| Giudice dell’esecuzione | Giudice dell’esecuzione | Giudice dell’esecuzione |
| --- | --- | --- |
| Gradi di Giudizio | Giudice | Pubblico Ministero |
| I – senza Appello | Tribunale per i Minorenni
Gip - Tribunale per i Minorenni
Gup - Tribunale per i Minorenni | Procura Repubblica per i Minorenni |
| Appello senza Riforma | Tribunale per i Minorenni
Gip - Tribunale per i Minorenni
Gup - Tribunale per i Minorenni | Procura Repubblica per i Minorenni |
| Appello con Riforma | Sezione Corte Appello Minorenni | Procura Generale presso la Corte di Appello |

Tabella 2 - Giudici dell'esecuzione



| Magistratura di Sorveglianza |
| --- |
| Tribunale per i Minorenni in funzione di Tribunale di Sorveglianza |
| Magistrato di Sorveglianza per i Minorenni |

Tabella 3 - Magistratura di Sorveglianza

# Elenco degli interventi
| Codice | Titolo | Ambito
Maggiorenni | Ambito
Minorenni |
| --- | --- | --- | --- |
| SIEP_M_015 | Tabella posizioni giuridiche iniziali |  |  |
| SIEP_M_016 | Gestione posizione giuridica iniziale |  |  |
| SIEP_M_017 | Decisione sorveglianza – Arresti domiciliari ex 656 comma 10° |  |  |
| SIEP_M_018 | Gestione Provvedimenti emessi dalla Magistratura di Sorveglianza |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |




# Legenda colori

| N. | Colore | Descrizione | Nota |
| --- | --- | --- | --- |
| 1 |  | Da rivedere meglio |  |
| 2 |  | Intervento sospeso |  |
| 3 |  |  |  |
| 4 |  |  |  |
| 5 |  |  |  |


# Convenzioni tipografiche

| N. |  | Nota |
| --- | --- | --- |
| 1 | Tra parentesi angolari <> | Nome tabella, oppure, nome campo |
| 2 | Tra virgolette alte “” | Testo etichetta |
| 3 | Tra parentesi quadre [] | Valori facoltativi |
| 4 | Tra parentesi graffe {} | Elenchi di valori |
| 5 | (*) | Dato obbligatorio |
| 6 | Sottolineatura | Probabile presenza di un collegamento. |


# Questioni aperte

| N. | Descrizione | Nota |
| --- | --- | --- |
| 1 |  |  |
| 2 |  |  |
| 3 |  |  |
| 4 |  |  |



# Tabella posizioni giuridiche iniziali
## Intervento richiesto dall’Amministrazione
Di conseguenza va aggiornata la tabella delle posizioni giuridiche iniziali da gestire.
La tabella deve contenere le seguenti voci:
Libero
Custodia Cautelare in regime di detenzione
Custodia Cautelare  in regime di Arresti Domiciliari
Custodia  Cautelare in Regime di Arresti  Domiciliare ex art 89  dpr 309/90
Custodia Cautelare in Regime di Permanenza in Casa
Custodia Cautelare in Collocamento in Comunità
Custodia Cautelare in Misura di Sicurezza Applicata in via Provvisoria
## Situazione attuale
## Descrizione dell’intervento
L’intervento prevede l’aggiunta alla tabella <CG_REF_CODES> delle seguenti voci:
Libero
Custodia Cautelare in regime di detenzione
Custodia Cautelare  in regime di Arresti Domiciliari
Custodia  Cautelare in Regime di Arresti  Domiciliare ex art 89  dpr 309/90
Custodia Cautelare in Regime di Permanenza in Casa
Custodia Cautelare in Collocamento in Comunità
Custodia Cautelare in Misura di Sicurezza Applicata in via Provvisoria.

Attualmente l’elenco delle posizioni giuridiche iniziali si ottiene dalla tabella <CG_REF_CODES>  selezionando tutte le tuple aventi la colonna <RV_DOMAIN>  valorizzata = a “TIPO_POSIZIONE_GIURIDICA” e la colonna <RV_ABBREVIATION> valorizzata uguale a “PRIMA”.
Pertanto, sono al momento presenti  solo le seguenti occorrenze:

| Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| N. | RV_DOMAIN | RV_LOW_VALUE | RV_HIGH_VALUE | RV_ABBREVIATION | RV_MEANING | RV_ALT2_VALUE | RV_ALT3_VALUE | RV_ALT4_VALUE | RV_ALT5_VALUE |
|  | POSIZIONE_GIURIDICA | 01 | C | PRIMA | Custodia Cautelare per Questa Causa in Regime di Detenzione | NULL | NULL | NULL | NULL |
|  | POSIZIONE_GIURIDICA | 02 | B | PRIMA | Custodia Cautelare per Questa Causa in Regime di Arresti Domiciliari | NULL | NULL | NULL | NULL |
|  | POSIZIONE_GIURIDICA | 05 | D | PRIMA | Latitante | NULL | NULL | NULL | NULL |
|  | POSIZIONE_GIURIDICA | 06 | E | PRIMA | Internato | NULL | NULL | NULL | NULL |
|  | POSIZIONE_GIURIDICA | 07 | A | PRIMA | Libero | NULL | NULL | NULL | NULL |


## Riferimenti
Confronta “documento analisi 16_07_14.doc”.
## Sottosistema
La modifica interessa solo il sottosistema Siep.
## Uffici
L’intervento in parola riguarda tutti gli uffici.
## Modifica funzionalità
Nessuna modifica prevista.
## Modifica interfacce utente
Nessuna modifica prevista.
## Modifica interfacce software/algoritmi
Nessuna modifica prevista.
## Modifica database
L’intervento prevede l’inserimento nella tabella <CG_REF_CODES> delle seguenti voci:
| N. | RV_DOMAIN | RV_LOW_VALUE | RV_HIGH_VALUE | RV_ABBREVIATION | RV_MEANING | RV_ALT2_VALUE | RV_ALT3_VALUE | RV_ALT4_VALUE | RV_ALT5_VALUE |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | POSIZIONE_GIURIDICA | 70 | B | PRIMA | Custodia  Cautelare in Regime di Arresti  Domiciliare ex art 89  dpr 309/90 | NULL | NULL | NULL | NULL |
|  | POSIZIONE_GIURIDICA | 71 | B | PRIMA | Custodia Cautelare in Regime di Permanenza in Casa | NULL | NULL | NULL | NULL |
|  | POSIZIONE_GIURIDICA | 72 | B | PRIMA | Custodia Cautelare in Collocamento in Comunità | NULL | NULL | NULL | NULL |
|  | POSIZIONE_GIURIDICA | 73 | C | PRIMA | Custodia Cautelare in Misura di Sicurezza Applicata in via Provvisoria | NULL | NULL | NULL | NULL |

Tabella 4 - Tabella <CG_REF_CODES>
## Modifica template
Nessuna modifica prevista.

# Gestione posizione giuridica iniziale
## Intervento richiesto dall’Amministrazione
Le maschere per l’annotazione per l’annotazione della posizione giuridica iniziale.
La maschera di caricamento per la gestione della posizione  giuridica iniziale va adattata alla posizione giuridica la maschera deve contenere la data di decorrenza pena.
Riportare i campi per lo scambio dati misura cautelare
## Situazione attuale
## Descrizione dell’intervento
L’utente all’interno del procedimento tramite la funzionalità del “Dettaglio procedimento” seleziona la voce “Iscrizione posizione giuridica” e prosegue facendo click sulla icona  “Vai” (Figura 1).
Il sistema mostra l’interfaccia utente della funzione “INSERIMENTO/MODIFICA POSIZIONE GIURIDICA” ed i dati salienti del procedimento (Figura 11).
L’utente seleziona dal gruppo di caselle di opzioni (radiobottom) una tra le seguenti voci:
Libero (voce valorizzata per default)
Espiazione Pena in Istituto di Detenzione
Espiazione Pena in Altro Luogo (Figura 12).
Se l’operatore seleziona l’opzione “Espiazione Pena in Istituto di Detenzione” il sistema visualizza la sezione “I” (Figura 18).
Se l’operatore seleziona l’opzione “Espiazione Pena in Altro Luogo” il sistema visualizza la sezione “L”(Figura 19).
Inizialmente per default viene mostrata la sezione “C” (Figura 13) e la sezione “L” (Figura 20).
L’elenco delle “Posizione Giuridiche” (Tabella 5) deve essere filtrato e mostrare solo posizioni giuridiche compatibili con la scelta effettuata nel gruppo di opzioni.
L’elenco delle “Misure” (Tabella 6) deve essere filtrato e mostrare solo misure compatibili con la scelta effettuata.
Se l’operatore spunta la casella di spunta (checkbox) “Detenuto per altra causa” il sistema mostra la sezione “D” (Figura 14).
Se l’operatore preme il pulsante “Conferma” il sistema valorizza la <DATA_DECORRENZA> con la data di sistema e salva le informazioni negli archivi.
La sezione “D” contiene un gruppo di caselle di opzioni:
“Definitivo - in Istituto di Detenzione” prevalorizzato per default
“Misure Cautelari- in Istituto di Detenzione”
“Misure Cautelari- in Altro Luogo”.
Per default sono selezionate le voci del punto a) ed il sistema visualizza la sezione “E” (Figura 15).
Se l’operatore seleziona la voce del punto b) ed il sistema visualizza la sezione “F”(Figura 16)
Se l’operatore seleziona la voce del punto c) ed il sistema visualizza la sezione “H”(Figura 17)
L’operatore preme il pulsante “Conferma” ed il sistema memorizza tutte le informazioni in archivio e visualizza le informazioni appena inserite in modo strutturato simile a quello di inserimento.
L’operatore può visualizzare le informazioni relative alla posizione giuridica richiamando dalla barra del dettaglio del procedimento la funzione “Elenco Posizioni giuridiche” e premendo sull’icona “Vai” (Figura 2).
Il sistema visualizza l’elenco delle posizioni giuridiche del soggetto e permette all’utente di vedere il dettaglio premendo sull’icona  oppure di cancellare la posizione premendo sull’icona (Figura 3).

Per quanto riguarda l’obbligatorietà delle informazioni si concorda di tener conto di quanto stabilito per l’intervento “Inserimento Misura – Detentiva/Non Detentiva  - Computabile/Non Computabile” perché spesso al momento dell’inserimento dei dati alcune informazioni possono non essere disponibili all’operatore.
Il presente intervento ha solo per oggetto la della funzione “INSERIMENTO/MODIFICA POSIZIONE GIURIDICA”  tramite il punto di accesso della funzionalità del “Dettaglio procedimento” come sopra descritto.

| N. | Descrizione | Nota |
| --- | --- | --- |
|  | Libero |  |
|  | Custodia Cautelare in regime di detenzione |  |
|  | Custodia Cautelare  in regime di Arresti Domiciliari |  |
|  | Custodia  Cautelare in Regime di Arresti  Domiciliare ex art 89  dpr 309/90 |  |
|  | Custodia Cautelare in Regime di Permanenza in Casa |  |
|  | Custodia Cautelare in Collocamento in Comunità |  |
|  | Custodia Cautelare in Misura di Sicurezza Applicata in via Provvisoria |  |

Tabella 5 - Elenco posizioni giuridiche iniziali

| N. | Descrizione | Nota |
| --- | --- | --- |
|  | Espiazione pena per Altra Causa in Regime di Detenzione |  |
|  | Espiazione pena per Altra Causa  in Misura Sicurezza  Detentiva ( Internato) |  |
|  | Custodia Cautelare per Altra Causa in Regime di Detenzione |  |
|  | Espiazione pena per Altra Causa in Misura di Sicurezza Applicata in Via Provvisoria |  |
|  | Custodia Cautelare per Altra Causa -  Regime di Arresti Domiciliari |  |
|  | Custodia Cautelare per Altra Causa -  Regime Permanenza in Casa |  |
|  | Custodia Cautelare per Altra Causa - Collocamento in Comunità |  |
|  | Custodia Cautelare per Altra Causa -  Regime di Arresti Domiciliari ex art 89 dpr 309/90 |  |

Tabella 6 - Elenco misure


Figura 1 - Punto accesso Iscrizione posizione giuridica


Figura 2 - Punto di accesso Elenco Posizioni Giuridiche


Figura 3 - Elenco Posizioni Giuridiche

Riassumendo in fase di inserimento l’operatore accede alla funzionalità di “iscrizione posizione giuridica iniziale” ed il sistema visualizza la maschera come mostrata in Figura 4 - Maschera posizione libero.
|  |  |
| --- | --- |
|  |  |
|  |  |
|  |  |

Figura 4 - Maschera posizione libero

Se l’operatore seleziona la casella di opzione (radiobutton) “Espiazione Pena in Istituto di Detenzione” il sistema visualizza la maschera in Figura 5 - Maschera Espiazione pena in istituto di detenzione.
|  |  |
| --- | --- |
|  |  |
|  |  |
|  |  |

Figura 5 - Maschera Espiazione pena in istituto di detenzione

Se l’operatore seleziona la casella di opzione (radiobutton) “Espiazione Pena in Altro Luogo” il sistema visualizza la maschera in Figura 6 - Maschera Espiazione pena in altro luogo.
|  |  |
| --- | --- |
|  |  |
|  |  |
|  |  |

Figura 6 - Maschera Espiazione pena in altro luogo

Se l’operatore nella maschera (Figura 4 - Maschera posizione libero) pone la spunta sulla casella (checkbutton) “Detenuto per altra causa” ed il sistema visualizza la maschera in Figura 7 - Maschera libero – Definitiva in istituto di detenzione.
|  |  |
| --- | --- |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |

Figura 7 - Maschera libero – Definitiva in istituto di detenzione
Se l’operatore nella maschera spunta (Figura 7 - Maschera libero – Definitiva in istituto di detenzione)
seleziona la casella di opzione “Misura Cautelare – in Istituto di Detenzione”  ed il sistema visualizza la maschera in (Figura 8 - Maschera libero – misura cautelare in istituto detenzione).

|  |  |
| --- | --- |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |

Figura 8 - Maschera libero – misura cautelare in istituto detenzione
Se l’operatore  nella maschera  (Figura 7 - Maschera libero – Definitiva in istituto di detenzione)
seleziona la casella di opzione “Misura Cautelare – in  Altro Luogo”  ed il sistema visualizza la maschera in
Figura 9 - Maschera libero – misura cautelare in altro luogo).
|  |  |
| --- | --- |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |

Figura 9 - Maschera libero – misura cautelare in altro luogo
Le interfacce utente sopra allegate sono navigabili secondo il seguente diagramma di navigazione:


Figura 10 - Diagramma navigazione
## Riferimenti
Confronta “documento analisi 16_07_14.doc”.
## Sottosistema
La modifica interessa solo il sottosistema Siep.
## Uffici
L’intervento in parola riguarda tutti gli uffici.
## Modifica funzionalità
## Modifica interfacce utente
Le interfacce devono essere realizzate componendo le sezioni con i criteri descritti nel paragrafo precedente (Descrizione dell’intervento).

Figura 11 - Sezione A


Figura 12 - Sezione B


Figura 13 - Sezione C


Figura 14 - Sezione D


Figura 15 - Sezione E - Libero – Detenuto Altra Causa – Definitivo in Istituto


Figura 16 - Sezione F - Libero – Detenuto Altra Causa – Misura cautelare in Istituto


Figura 17 - Sezione G – Libero – Detenuto Altra Causa – Misura cautelare in Altro Luogo


Figura 18 - Sezione H - Espiazione Pena in Istituto di Detenzione


Figura 19 - Sezione I - Espiazione Pena in Altro Luogo

Figura 20 - Sezione L
Dalla vecchia interfaccia utente vengono rimosse le informazioni:
“Luogo lavoro semilibertà”
“Luogo prova affidamento”.
Le informazioni contenute in archivio vengono visualizzate nelle nuove interfacce nel campo “Note” a sola lettura e non modificabile dall’operatore.
Si è concordato che le caselle di opzione devono precedere le relative etichette come mostrato nelle figure precedenti.

## Modifica interfacce software/algoritmi
Il sistema nella valorizzazione dei campi deve seguire le seguenti regole:
| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Posizione Giuridica | * |  | Valorizzato tramite elenco tipo posizione giuridica prelevato da tabella < CG_REF_CODES > filtrata selezionando le tuple aventi colonna <RV_DOMAIN> = “POSIZIONE_GIURIDICA”
Per l’opzione “Libero” viene valorizzata solo la posizione “Libero”
Per l’opzione “Espiazione Pena in Istituto di Detenzione” :
{“Custodia Cautelare in regime di detenzione”,
“Custodia Cautelare in Misura di Sicurezza Applicata in via Provvisoria”}
Per l’opzione “Espiazione Pena in Altro Luogo” : 
{“Custodia Cautelare  in regime di Arresti Domiciliari”,
“Custodia  Cautelare in Regime di Arresti  Domiciliare ex art 89  dpr 309/90”,
“Custodia Cautelare in Regime di Permanenza in Casa”,
“Custodia Cautelare in Collocamento in Comunità”
“Custodia Cautelare in Misura di Sicurezza Applicata in via Provvisoria”} |
|  | Detenuto Altra Causa |  |  | Casella di spunta 
Prevalorizzata non spuntata |

Tabella 7 – Interfaccia - Sezione C – Libero
| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Tipo Misura |  |  | Valorizzato tramite elenco:
{“Espiazione pena per Altra Causa in Regime di Detenzione”,
“Espiazione pena per Altra Causa  in Misura Sicurezza  Detentiva ( Internato)”} |
|  | Istituto di Detenzione |  |  | Valorizzato tramite funzione “Ricerca istituto detenzione”.
L’operatore può svuotare il campo tramite la funzione “Cancella”. |
|  | Anno SIEP |  |  | Testo valorizzato dall’utente. 4 cifre [0..9] |
|  | Numero SIEP |  |  | Testo valorizzato dall’utente. 6 cifre [0..9] |
|  | Autorità Emittente | * |  | Valorizzato tramite elenco uffici prelevato da tabella <CG_REF_CODES>  con campo <RV_DOMAIN> = ‘TIPO_UFFICIO’.
Nell’elenco devono essere vivibili e selezionabili le seguenti voci:
{“Procura Generale della Repubblica presso la Corte di Appello” (RV_DOMAIN=”PGCAP”)
“Procura della Repubblica presso il Tribunale Ordinario”               (RV_DOMAIN=”PM”),        
“Procura presso il Tribunale per i minorenni                                     (RV_DOMAIN=”PMM”} |
|  | Luogo Emittente |  |  | Valorizzato dall’operatore tramite elenco in relazione alla scelta della Autorità Emittente. |
|  | Data Scadenza Pena |  |  | Data (2 gg 2 mm 4 anno) – controllare correttezza formale data |

Tabella 8 – Interfaccia - Sezione E – Libero – Altra causa – Definitivo in Istituto

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Anno B.D.M.C. |  | 4 | Testo valorizzato dall’utente. 4 cifre [0..9] |
|  | Numero B.D.M.C. |  | 6 | Testo valorizzato dall’utente. 6 cifre [0..9] |
|  | Tipo Ufficio PM | * |  | Valorizzato tramite elenco uffici prelevato da tabella <CG_REF_CODES>  con campo <RV_DOMAIN> = ‘TIPO_UFFICIO’.
Se l’operatore è un operatore della Procura della Repubblica prevalorizzato per default a “Procura della Repubblica” 
Se l’operatore è un operatore della Procura per i minorenni prevalorizzato per default a “Procura presso il Tribunale per i minorenni” 
Se l’operatore è un operatore della Procura Generale prevalorizzato per default a per default a “Procura della Repubblica” |
|  | Sede Ufficio PM |  |  | Valorizzato tramite elenco in relazione alla scelta del “Tipo Ufficio PM”
Se l’operatore seleziona “Tipo Ufficio PM” = “Procura della Repubblica”
L’elenco contiene solo le sedi delle Procure della Repubblica
Se l’operatore seleziona “Tipo Ufficio PM” = “Procura Generale”
L’elenco contiene solo le sedi delle Procure Generali
Se l’operatore seleziona “Tipo Ufficio PM” = “Procura presso Tribunale per i minorenni”
L’elenco contiene solo le sedi delle Procure presso Tribunale per i minorenni. |
|  | Anno R.G.N.R. |  | 4 | Testo valorizzato dall’utente. 4 cifre [0..9] |
|  | Numero R.G.N.R. |  | 6 | Testo valorizzato dall’utente. 6 cifre [0..9] |
|  | Anno Reg. Gen. |  | 4 | Testo valorizzato dall’utente. 4 cifre [0..9] |
|  | Numero Reg. Gen. |  | 6 | Testo valorizzato dall’utente. 6 cifre [0..9] |
|  | Tipo ufficio Reg. Gen. |  |  | Valorizzato tramite elenco :=  {“GIP”,”DIB”,”CAS”,”CAP”,”CASAP”}.
Prevalorizzato inizialmente con il valore “-“ |
|  | Autorità emittente | * |  | Valorizzato tramite elenco uffici prelevato da tabella <CG_REF_CODES>  con campo <RV_DOMAIN> = ‘TIPO_UFFICIO’.
Nell’elenco devono essere vivibili e selezionabili le seguenti voci:
{Corte D'Appello
Corte di Assise
Corte di Assise di Appello
Sezione Distaccata
Corte Suprema di Cassazione
Gip Presso il Tribunale per i Minorenni
Gip Presso il Tribunale Ordinario
Gup Presso il Tribunale per i Minorenni
Gup Presso Tribunale Ordinario
Sezione Distaccata di Tribunale
Sezione Minorenni per la Corte di Appello
Tribunale Ordinario
Tribunale per i Minorenni}
In fase di inserimento prevalorizzato inizialmente con il valore “Gip Presso il Tribunale Ordinario“ se l’operatore è della Procura presso il Tribunale Ordinario oppure se l’operatore è della Procura Generale presso la Corte di Appello.
In fase di inserimento prevalorizzato inizialmente con il valore “Gip Presso il Tribunale per i Minorenni“ se l’operatore è della Procura presso il Tribunale per i minorenni. |
|  | Luogo Emittente |  |  | In fase di inserimento 
1) prevalorizzato per default con la sede dell’operatore, oppure
2) valorizzato con lo stesso valore della “Sede del PM”
3) Valorizzato dall’operatore tramite in relazione alla scelta della Autorità Emittente. |
|  | Tipo misura | * |  | Valorizzato tramite elenco tipo misure cautelari prelevato da tabella < CG_REF_CODES > filtrata selezionando le tuple aventi colonna <RV_DOMAIN> = “TIPO_MISURA_CAUTELARE”
Per l’opzione ““Misure Cautelari- in Istituto di Detenzione”” contiene:

Valorizzato tramite elenco:
{“Custodia Cautelare per Altra Causa in Regime di Detenzione”, 
“Espiazione pena per Altra Causa in Misura di Sicurezza Applicata in Via Provvisoria”} |
|  | Istituto di Detenzione |  |  | Valorizzato tramite funzione “Ricerca istituto detenzione”.
L’operatore può svuotare il campo tramite la funzione “Cancella”. |

Tabella 9 – Interfaccia - Sezione F - Libero – Altra causa – Misura cautelare in Istituto

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Anno B.D.M.C. |  | 4 | Testo valorizzato dall’utente. 4 cifre [0..9] |
|  | Numero B.D.M.C. |  | 6 | Testo valorizzato dall’utente. 6 cifre [0..9] |
|  | Tipo Ufficio PM | * |  | Valorizzato tramite elenco uffici prelevato da tabella <CG_REF_CODES>  con campo <RV_DOMAIN> = ‘TIPO_UFFICIO’.
Se l’operatore è un operatore della Procura della Repubblica prevalorizzato per default a “Procura della Repubblica” 
Se l’operatore è un operatore della Procura per i minorenni prevalorizzato per default a “Procura presso il Tribunale per i minorenni” 
Se l’operatore è un operatore della Procura Generale prevalorizzato per default a per default a “Procura della Repubblica” |
|  | Sede Ufficio PM |  |  | Valorizzato tramite elenco in relazione alla scelta del “Tipo Ufficio PM”
Se l’operatore seleziona “Tipo Ufficio PM” = “Procura della Repubblica”
L’elenco contiene solo le sedi delle Procure della Repubblica
Se l’operatore seleziona “Tipo Ufficio PM” = “Procura Generale”
L’elenco contiene solo le sedi delle Procure Generali
Se l’operatore seleziona “Tipo Ufficio PM” = “Procura presso Tribunale per i minorenni”
L’elenco contiene solo le sedi delle Procure presso Tribunale per i minorenni. |
|  | Anno R.G.N.R. |  | 4 | Testo valorizzato dall’utente. 4 cifre [0..9] |
|  | Numero R.G.N.R. |  | 6 | Testo valorizzato dall’utente. 6 cifre [0..9] |
|  | Anno Reg. Gen. |  | 4 | Testo valorizzato dall’utente. 4 cifre [0..9] |
|  | Numero Reg. Gen. |  | 6 | Testo valorizzato dall’utente. 6 cifre [0..9] |
|  | Tipo ufficio Reg. Gen. |  |  | Valorizzato tramite elenco :=  {“GIP”,”DIB”,”CAS”,”CAP”,”CASAP”}.
Prevalorizzato inizialmente con il valore “-“ |
|  | Autorità Emittente | * |  | Valorizzato tramite elenco uffici prelevato da tabella <CG_REF_CODES>  con campo <RV_DOMAIN> = ‘TIPO_UFFICIO’.
Nell’elenco devono essere vivibili e selezionabili le seguenti voci:
{Corte D'Appello
Corte di Assise
Corte di Assise di Appello
Sezione Distaccata
Corte Suprema di Cassazione
Gip Presso il Tribunale per i Minorenni
Gip Presso il Tribunale Ordinario
Gup Presso il Tribunale per i Minorenni
Gup Presso Tribunale Ordinario
Sezione Distaccata di Tribunale
Sezione Minorenni per la Corte di Appello
Tribunale Ordinario
Tribunale per i Minorenni}
In fase di inserimento prevalorizzato inizialmente con il valore “Gip Presso il Tribunale Ordinario“ se l’operatore è della Procura presso il Tribunale Ordinario oppure se l’operatore è della Procura Generale presso la Corte di Appello.
In fase di inserimento prevalorizzato inizialmente con il valore “Gip Presso il Tribunale per i Minorenni“ se l’operatore è della Procura presso il Tribunale per i minorenni. |
|  | Luogo Emittente |  |  | In fase di inserimento 
1)prevalorizzato per default con la sede dell’operatore, oppure
2) valorizzato con lo stesso valore della “Sede del PM”
3) Valorizzato dall’operatore tramite elenco in relazione alla scelta della Autorità Emittente |
|  | Tipo misura | * |  | Valorizzato tramite elenco tipo misure cautelari prelevato da tabella <CG_REF_CODES> filtrata selezionando le tuple aventi colonna <RV_DOMAIN> = “TIPO_MISURA_CAUTELARE”
Per l’opzione ““Misure Cautelari- in Altro Luogo” contiene:

Valorizzato tramite elenco:
{“Custodia Cautelare per Altra Causa -  Regime di Arresti Domiciliari”,   
“Custodia Cautelare per Altra Causa -  Regime Permanenza in Casa”,
“Custodia Cautelare per Altra Causa - Collocamento in Comunità”,
“Custodia Cautelare per Altra Causa -  Regime di Arresti Domiciliari ex art 89 dpr 309/90”} |
|  | Luogo di Espiazione |  |  | Testo libero |
|  | Autorità Competente per territorio | * |  | Valorizzato tramite elenco autorità prelevato da tabella <CF_REF_CODES> con campo <RV_DOMAIN> = ‘TIPO_AUTORITA’ e filtrata secondo indicazioni fornite nell’intervento  “Tabella forze di Polizia”. |
|  | Autorità Competente per territorio - Sede |  |  | Valorizzato tramite funzione “Ricerca comune” in relazione alla selezione della Autorità. |
|  | Autorità Competente per territorio - Indirizzo |  |  | Testo libero massimo 1000 caratteri alfanumerici |

Tabella 10 – Interfaccia - Sezione G - Libero – Altra causa – Misura cautelare in Altro luogo

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Data di Decorrenza Pena |  |  | Data (2 gg 2 mm 4 anno) – controllare correttezza formale data |
|  | Istituto di Detenzione |  |  | Valorizzato tramite funzione “Ricerca istituto detenzione”.
L’operatore può svuotare il campo tramite la funzione “Cancella”. |

Tabella 11 – Interfaccia – Sezione H

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Data di Decorrenza Pena |  |  | Data (2 gg 2 mm 4 anno) – controllare correttezza formale data |
|  | Luogo di Espiazione |  |  | Testo libero massimo 1000 caratteri alfanumerici |
|  | Autorità Competente per territorio | * |  | Valorizzato tramite elenco autorità prelevato da tabella <CF_REF_CODES> con campo <RV_DOMAIN> = ‘TIPO_AUTORITA’. |
|  | Autorità Competente per territorio - Sede |  |  | Valorizzato tramite funzione “Ricerca comune” in relazione alla selezione della Autorità. |
|  | Autorità Competente per territorio - Indirizzo |  |  | Testo libero massimo 1000 caratteri alfanumerici |

Tabella 12 – Interfaccia – Sezione I

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Note |  |  | Campo sola lettura non modificabile dall’operatore.
Contiene le informazioni presenti nei campi  rimossi:
“Luogo lavoro semilibertà”
“Luogo prova affidamento”. |
|  | Conferma |  |  | L’operatore conferma le informazioni inserite premendo il pulsante “CONFERMA” |

Tabella 13 – Interfaccia – Sezione L

Prima dell’intervento in oggetto le informazioni inserite dall’operatore vengono distribuite nelle seguenti tabelle:
<POSIZIONE_GIURIDICA>
<ALTRA_CAUSA>
<LUOGO_DETENZIONE>
Dopo l’intervento alcune informazioni devono essere memorizzate anche nella tabella
<MISURA_CAUTELARE>.
Attualmente ogni volta che il sistema inserisce un record nella tabella <POSIZIONE_GIURIDICA> inserisce sempre un record nella tabella <LUOGO_DETENZIONE>.
Il collegamento tra le tabelle <POSIZIONE_GIURIDICA> e <LUOGO_DETENZIONE>è garantita dalla relazione tra tabella <POSIZIONE_GIURIDICA> campo <ID_POSIZIONE_GIURIDICA> e tabella <LUOGO_DETENZIONE> campo <POS_GIU_ID_POSIZIONE_GIURIDICA >.
In modo analogo per permettere il collegamento modo univoco e certo tra le tabelle <POSIZIONE_GIURIDICA> e <MISURA_CAUTELARE> deve essere inserito nella tabella <MISURA_CAUTELARE> il campo <POS_GIU_ID_POSIZIONE_GIURIDICA>.
Nella memorizzazione delle informazioni è necessario tener conto delle seguenti regole (Tabella 14) durante l’inserimento nel rispetto di quanto avviene prima dell’intervento in oggetto:
il sistema inserisce sempre un record nella tabella <POSIZIONE_GIURIDICA>
se l’operatore seleziona l’opzione “Libero” e pone la spunta sulla casella di spunta “Detenuto Altra causa” il sistema inserisce un record anche nella tabella <ALTRA_CAUSA>
il sistema inserisce un record anche nella tabella <LUOGO_DETENZIONE>
se l’operatore valorizza una misura cautelare il sistema inserisce un record anche nella tabella <MISURA_CAUTELARE>.
Attualmente, è presente nel codice un controllo che nel caso di “Espiazione Pena in Istituto di Detenzione“ oppure nel caso di “Espiazione Pena in Altro Luogo” inserisce nella tabella <MISURA_CAUTELARE> un record. Il suddetto controllo viene mantenuto anche dopo il presente intervento.

| Opzioni | Opzioni | Opzioni | Opzioni | Opzioni | Tabelle | Tabelle | Tabelle | Tabelle |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Opzioni | Opzioni | Opzioni | Opzioni | Opzioni | POSIZIONE_GIURIDICA | ALTRA_CAUSA | LUOGO_DETENZIONE | MISURA_CAUTELARE |
|  | Libero | Libero | Libero | Libero |  |  |  |  |
|  | Espiazione Pena in Istituto di Detenzione | Espiazione Pena in Istituto di Detenzione | Espiazione Pena in Istituto di Detenzione | Espiazione Pena in Istituto di Detenzione |  |  |  |  |
|  | Espiazione Pena in Altro Luogo | Espiazione Pena in Altro Luogo | Espiazione Pena in Altro Luogo | Espiazione Pena in Altro Luogo |  |  |  |  |
|  | Libero | Detenuto Altra causa | Definitivo | Istituto |  |  |  |  |
|  | Libero | Detenuto Altra causa | Misura Cautelare | Istituto |  |  |  |  |
|  | Libero | Detenuto Altra causa | Misura Cautelare | Altro Luogo |  |  |  |  |

Tabella 14 - Schema riepilogativo

## Modifica database
L’intervento prevede, per permettere il collegamento modo univoco e certo tra le tabelle <POSIZIONE_GIURIDICA> e <MISURA_CAUTELARE>, l’inserimento nella tabella <MISURA_CAUTELARE> di una nuova colonna <POS_GIU_ID_POSIZIONE_GIURIDICA>.

| N. | Nome colonna | Tipo | Null | Tipo Dato | Dim | Note |
| --- | --- | --- | --- | --- | --- | --- |
|  | POS_GIU_ID_POSIZIONE_GIURIDICA |  | Y | Numerico | 38 |  |

Tabella 15 - Tabella MISURA_CAUTELARE nuova colonna

Inoltre, l’intervento prevede l’inserimento nella tabella <POSIZIONE_GIURIDICA> i seguenti campi:
| N. | Nome colonna | Tipo | Null | Tipo Dato | Dim | Note |
| --- | --- | --- | --- | --- | --- | --- |
|  | LUOGO_ESPIAZIONE |  | Y | Varchar2 | 1000 |  |
|  | AUTORITA_COMPETENTE |  | N | Varchar2 | 2 | Codice tipo autorità |
|  | AUTORITA_ COMPETENTE_SEDE |  | Y | Varchar2 | 6 | Codice Istat del comune |
|  | AUTORITA_ COMPETENTE_INDIRIZZO |  | Y | Varchar2 | 1000 |  |
|  | COD_MASCHERA |  | Y | Varchar2 | 2 | Per memorizzare il codice della maschera |

Tabella 16 – Tabella <POSIZIONE_GIURIDICA> nuove colonne

L’intervento prevede l’inserimento nella tabella <CG_REF_CODES> dei seguenti record:
| N. | RV_DOMAIN | RV_LOW_VALUE | RV_HIGH_VALUE | RV_ABBREVIATION | RV_MEANING | RV_ALT2_VALUE | RV_ALT3_VALUE | RV_ALT4_VALUE | RV_ALT5_VALUE |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | TIPO_MISURA_CAUTELARE | EA | NULL | NULL | Espiazione pena per Altra Causa in Regime di Detenzione | NULL | NULL | NULL | NULL |
|  | TIPO_MISURA_CAUTELARE | EB | NULL | NULL | Espiazione pena per Altra Causa  in Misura Sicurezza  Detentiva ( Internato) | NULL | NULL | NULL | NULL |
|  | TIPO_MISURA_CAUTELARE | CF | NULL | NULL | Custodia Cautelare per Altra Causa in Regime di Detenzione | NULL | NULL | NULL | NULL |
|  | TIPO_MISURA_CAUTELARE | CG | NULL | NULL | Espiazione pena per Altra Causa in Misura di Sicurezza Applicata in Via Provvisoria | NULL | NULL | NULL | NULL |
|  | TIPO_MISURA_CAUTELARE | CH | NULL | NULL | Custodia Cautelare per Altra Causa -  Regime di Arresti Domiciliari | NULL | NULL | NULL | NULL |
|  | TIPO_MISURA_CAUTELARE | CI | NULL | NULL | Custodia Cautelare per Altra Causa -  Regime Permanenza in Casa | NULL | NULL | NULL | NULL |
|  | TIPO_MISURA_CAUTELARE | CJ | NULL | NULL | Custodia Cautelare per Altra Causa - Collocamento in Comunità | NULL | NULL | NULL | NULL |
|  | TIPO_MISURA_CAUTELARE | CK | NULL | NULL | Custodia Cautelare per Altra Causa -  Regime di Arresti Domiciliari ex art 89 dpr 309/90 | NULL | NULL | NULL | NULL |

Tabella 17 – Tabella <CG_REF_CODES> Tipo misura cautelare

## Modifica template
Nessuna modifica prevista.


# Decisione sorveglianza – Arresti domiciliari ex 656 comma 10°
## Intervento richiesto dall’Amministrazione
Sulla scheda Decisione della Sorveglianza va creata una nuova voce:

Gestione arresti domiciliari di conseguenza va prevista la gestione dei provvedimenti emessi dal magistrato di sorveglianza.

La scheda “Sospensione Arresti Domiciliari“ è identica alla sospensione ex art. 51 ter, già presenti nell’applicativo.
Il campo “data  ingresso in carcere va resa  visibile unicamente  se l’operatore seleziona la funzione “Eseguita da Magistrato di Sorveglianza” .
Il campo oggetto decreto deve contenere i seguenti valori:
sospensione provvisoria  Arresti Domiciliari ex art.656 comma 10
sospensione provvisoria Domiciliari ex art 89 dpr 309/90
sospensione provvisoria Permanenza in Casa
sospensione provvisoria Collocamento in Comunità.
Va creata una nuova Posizione giuridica:
Sospensione provvisoria 51 ter   Arresti Domiciliari ex art.656 comma 10
Sospensione provvisoria 51 ter   Domiciliari ex art 89 dpr 309/90
Sospensione provvisoria 51 ter   Permanenza in Casa
Sospensione provvisoria 51 ter   Collocamento in Comunità.


Revoca  Arresti Domiciliari  Rigetta applicazione misura alternativa


Il tasto di richiamo della funzione deve essere rinominato in Revoca Rigetto – verificare flusso Tribunale Sorveglianza.
Va gestita la posizione da espiazione misura che da detenuto per sospensiva del Magistrato ex art.51 ter
la gestione è equiparata alla revoca detenzione domiciliare compresa la modulistica che va adeguata alle nuove misure.
Valori da gestire:
Arresti Domiciliari ex art.656 comma 10
Domiciliari ex art 89 dpr 309/90
Permanenza in Casa
Collocamento in Comunità.

Concessione delle  misure alternativa
Vanno verificate, partendo dalle nuove misure: prosecuzione in Permanenza in casa e collocamento in comunità che vanno equiparate agli arresti domiciliari 656 comma 10.
Arresti Domiciliari ex art.656 comma 10
Domiciliari ex art 89 dpr 309/90
Permanenza in Casa
Collocamento in Comunità.



Ripristino Degli Arresti Domiciliari

La scheda è identica a quella prevista per la detenzione domiciliare vanno replicate tutte le funzioni.
Arresti Domiciliari 656 comma 10 cpp
Arresti Domiciliari ex art 89 dpr 309/90
Permanenza in Casa (656 comma 10 cpp)
Collocamento in Comunità (656 comma 10 cpp).

## Situazione attuale
Il sistema attualmente non prevede la gestione della decisione in oggetto.
## Descrizione dell’intervento
L’intervento prevede la gestione all’interno delle decisione della Sorveglianza degli “Arresti domiciliari ex 656 comma 10°”.
L’operatore all’interno del procedimento dopo aver selezionato nel menu a sinistra la voce “Decisioni Sorveglianza” (Figura 21) può selezionare nella parte centrale della finestra la nuova tipologia di decisione (Figura 22).
L’operatore dopo aver selezionato “Arresti domiciliari art. 656 comma 10” il sistema mostra la maschera (Figura 23) per permettere la selezione di 1 dei seguenti successivi 4 passaggi:
Sospensione provvisoria Arresti Domiciliari 				(nuova maschera)
Ripristino Degli Arresti Domiciliari					(nuova maschera)
Revoca Arresti Domiciliari  e Rigetta applicazione misura alternativa 	(nuova maschera).


Figura 21 - Decisioni Sorveglianza


Figura 22 - Decisioni Sorveglianza

Figura 23 - Inserimento arresti domiciliari
Se l’operatore seleziona “Sospensione provvisoria Arresti Domiciliari” il sistema mostra la seguente interfaccia:

|  |  |
| --- | --- |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |

Figura 24 - Sospensione provvisoria Arresti Domiciliari – Eseguita Procura





Se l’operatore seleziona la casella di opzione “Eseguita da Magistrato di Sorveglianza” ” il sistema mostra la seguente interfaccia:

|  |  |
| --- | --- |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |

Figura 25 - Sospensione provvisoria Arresti Domiciliari – Eseguita Magistrato di Sorveglianza


La revoca degli arresti domiciliari può avvenire dopo la sospensione provvisoria, oppure, direttamente.
Nel caso (revoca dopo sospensione) la posizione giuridica iniziale del soggetto è uguale (Tabella 45 - Tabella <CG_REF_CODES> Posizione giuridica) a:
Sospensione provvisoria prosecuzione arresti domiciliari ex art. 656 comma 10
Sospensione provvisoria prosecuzione Arresti Domiciliari ex art 89 dpr 309/90
Sospensione provvisoria prosecuzione permanenza in casa ex art. 656 comma 10
Sospensione provvisoria prosecuzione collocamento in comunità ex art. 656 comma 10.

Se l’operatore nella interfaccia (Figura 23) seleziona “Revoca Arresti Domiciliari  e Rigetta applicazione misura alternativa” nel caso di revoca diretta senza precedente sospensione provvisoria il sistema mostra la seguente interfaccia:

|  |  |
| --- | --- |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |

Figura 26 - Revoca Arresti Domiciliari  e Rigetta applicazione misura alternativa - Revoca diretta
Se l’operatore nella interfaccia (Figura 23) seleziona “Revoca Arresti Domiciliari  e Rigetta applicazione misura alternativa” nel caso di revoca dopo precedente sospensione provvisoria il sistema mostra la seguente interfaccia:

|  |  |
| --- | --- |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |

Figura 27 - Revoca Arresti Domiciliari  e Rigetta applicazione misura alternativa - Revoca dopo sospensione


Se l’operatore nella interfaccia (Figura 23) seleziona “Ripristino Degli Arresti Domiciliari” il sistema mostra la seguente interfaccia:

|  |  |
| --- | --- |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |

Figura 28 - Ripristino Degli Arresti Domiciliari – Eseguita Procura



Se l’operatore seleziona la casella di opzione “Eseguita dalla Sorveglianza” il sistema mostra la seguente interfaccia:

|  |  |
| --- | --- |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |

Figura 29 - Ripristino Degli Arresti Domiciliari – Eseguita Sorveglianza

Se l’operatore preme il pulsante “Conferma” il sistema provvede a memorizzare le informazioni inserite/valorizzate dall’operatore.
L’operatore può stampare il documento utilizzando uno dei nuovi template (Tabella 48) ed infine validarlo.



|  | Condizioni | Template |
| --- | --- | --- |
| Sospensione provvisoria Arresti Domiciliari | Eseguita da PM | SIEP_MA_ARDOM_SOSP_PROC |
| Sospensione provvisoria Arresti Domiciliari | Eseguita da Magistrato Sorveglianza | SIEP_MA_ ARDOM_SOSP_MDS |
| Ripristino Arresti Domiciliari | Tipo provvedimento (decreto/ordinanza) del Magistrato 
Eseguito dal Magistrato di Sorveglianza | SIEP_MA_ ARDOM_RIPR_MDS |
| Ripristino Arresti Domiciliari | Tipo provvedimento (decreto/ordinanza)  del Magistrato 
Eseguito dalla Procura | SIEP_MA_ ARDOM_RIPR_MDS_PROC |
| Ripristino Arresti Domiciliari | Tipo provvedimento (decreto/ordinanza)  del Tribunale
Eseguito dal Tribunale di Sorveglianza | SIEP_MA_ ARDOM_RIPR_ TDS |
| Ripristino Arresti Domiciliari | Tipo provvedimento (decreto/ordinanza)  del Tribunale
Eseguito dalla Procura | SIEP_MA_ ARDOM_RIPR_TDS_PROC |
| Revoca Arresti Domiciliari | Revoca diretta senza prima sospensione provvisoria | SIEP_MA_ARDOM_REVO_DIRETTA |
| Revoca Arresti Domiciliari | Revoca a seguito di  sospensione provvisoria | SIEP_MA_ARDOM_REVO_SOSPENSIONE |

Tabella 18 – Nuovi template
Inoltre, l’operatore può visualizzare il  provvedimento selezionando dalla barra del dettaglio del procedimento la voce “Elenco provvedimenti Sorveglianza e GE” (Figura 30).

L’intervento prevede l’inserimento di 8 nomi provvedimento (Tabella 47).
I nuovi “Nome provvedimento” mappano uno a uno i nuovi template (Tabella 18)

Dopo l’inserimento delle informazioni e dopo la validazione del provvedimento il sistema aggiorna la posizione giuridica.
Nel caso della “Sospensione provvisoria Arresti Domiciliari”, il sistema aggiorna:
la posizione giuridica           [utilizzando le nuove posizioni giuridiche     (Tabella 45)].
lo stato del procedimento  [utilizzando i nuovi stati del procedimento  (Tabella 46)].
Nel caso del “Ripristino Degli Arresti Domiciliari”, il sistema aggiorna:
la posizione giuridica           [utilizzando le nuove posizioni giuridiche    (Tabella 45)].
lo stato del procedimento  [utilizzando i nuovi stati del procedimento (Tabella 46)].

Nel caso della “Revoca Arresti Domiciliari  e Rigetta applicazione misura alternativa”, il sistema aggiorna:
la posizione giuridica           [utilizzando le nuove posizioni giuridiche    (Tabella 45)].
lo stato del procedimento  [utilizzando i nuovi stati del procedimento (Tabella 46)].

|  |  |  | Oggetto Decisione | Posizione giuridica Finale |
| --- | --- | --- | --- | --- |
| Sospensione provvisoria Arresti Domiciliari | Sospensione provvisoria Arresti Domiciliari | Sospensione provvisoria Arresti Domiciliari | Sospensione provvisoria Arresti Domiciliari | Sospensione provvisoria Arresti Domiciliari |
|  |  |  | Sospensione provvisoria  prosecuzione arresti domiciliari ex art. 656 comma 10 | Sospensione provvisoria  prosecuzione arresti domiciliari ex art. 656 comma 10 |
|  |  |  | Sospensione provvisoria  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90 | Sospensione provvisoria  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90 |
|  |  |  | Sospensione provvisoria  prosecuzione permanenza in casa  ex art. 656 comma 10 | Sospensione provvisoria  prosecuzione permanenza in casa  ex art. 656 comma 10 |
|  |  |  | Sospensione provvisoria  prosecuzione collocamento in comunità  ex art.  656 comma 10 | Sospensione provvisoria  prosecuzione collocamento in comunità  ex art.  656 comma 10 |
| Ripristino Arresti Domiciliari | Ripristino Arresti Domiciliari | Ripristino Arresti Domiciliari | Ripristino Arresti Domiciliari | Ripristino Arresti Domiciliari |
|  |  |  | Rigetto revoca  prosecuzione arresti domiciliari ex art. 656 comma 10 | Arresti domiciliari ex art. 656 comma 10 |
|  |  |  | Rigetto revoca  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90 | Arresti Domiciliari ex art 89 dpr 309/90 |
|  |  |  | Rigetto revoca  prosecuzione permanenza in casa  ex art. 656 comma 10 | Permanenza in casa  ex art. 656 comma 10 |
|  |  |  | Rigetto revoca  prosecuzione collocamento in comunità  ex art.  656 comma 10 | Collocamento in comunità  ex art.  656 comma 10 |
|  |  |  | Perdita efficacia Sospensione provvisoria  prosecuzione arresti domiciliari ex art. 656 comma 10 | Arresti domiciliari ex art. 656 comma 10 |
|  |  |  | Perdita efficacia Sospensione provvisoria  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90 | Arresti Domiciliari ex art 89 dpr 309/90 |
|  |  |  | Perdita efficacia Sospensione provvisoria  prosecuzione permanenza in casa  ex art. 656 comma 10 | Permanenza in casa  ex art. 656 comma 10 |
|  |  |  | Perdita efficacia Sospensione provvisoria  prosecuzione collocamento in comunità  ex art.  656 comma 10 | Collocamento in comunità  ex art.  656 comma 10 |
| Revoca Arresti Domiciliari | Revoca Arresti Domiciliari | Revoca Arresti Domiciliari | Revoca Arresti Domiciliari | Revoca Arresti Domiciliari |
|  |  |  | Revoca  Arresti domiciliari ex art. 656 comma 10 | Espiazione pena in regime carcerario |
|  |  |  | Revoca   Arresti Domiciliari ex art 89 dpr 309/90 | Espiazione pena in regime carcerario |
|  |  |  | Revoca   Permanenza in casa  ex art. 656 comma 10 | Espiazione pena in regime carcerario |
|  |  |  | Revoca  Collocamento in comunità  ex art.  656 comma 10 | Espiazione pena in regime carcerario |

Tabella 19 – Posizione giuridica finale

| Oggetto Decisione | Oggetto Decisione | Stato procedimento finale | Stato procedimento finale |
| --- | --- | --- | --- |
|  |  | Eseguita PM | Eseguita da Sorveglianza |
| Sospensione provvisoria Arresti Domiciliari | Sospensione provvisoria Arresti Domiciliari |  |  |
|  | Sospensione provvisoria  prosecuzione arresti domiciliari ex art. 656 comma 10 | Sospensione provvisoria  prosecuzione arresti domiciliari ex art. 656 comma 10 - Emesso Ordine di Esecuzione  in data [data provvedimento] | Sospensione provvisoria  prosecuzione arresti domiciliari ex art. 656 comma 10 - Emessa Comunicazione Scadenza Pena: [data provvedimento] |
|  | Sospensione provvisoria  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90 | Sospensione provvisoria  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90 -  Emesso Ordine di Esecuzione  in data [data provvedimento] | Sospensione provvisoria  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90 -  Emessa Comunicazione Scadenza Pena: [data provvedimento] |
|  | Sospensione provvisoria  prosecuzione permanenza in casa  ex art. 656 comma 10 | Sospensione provvisoria  prosecuzione permanenza in casa  ex art. 656 comma 10 - Emesso Ordine di Esecuzione  in data [data provvedimento] | Sospensione provvisoria  prosecuzione permanenza in casa  ex art. 656 comma 10 - Emessa Comunicazione Scadenza Pena: [data provvedimento] |
|  | Sospensione provvisoria  prosecuzione collocamento in comunità  ex art.  656 comma 10 | Sospensione provvisoria  prosecuzione collocamento in comunità  ex art.  656 comma 10 - Emesso Ordine di Esecuzione  in data [data provvedimento] | Sospensione provvisoria  prosecuzione collocamento in comunità  ex art.  656 comma 10 - Emessa Comunicazione Scadenza Pena: [data provvedimento] |
| Ripristino Arresti Domiciliari | Ripristino Arresti Domiciliari | Ripristino Arresti Domiciliari | Ripristino Arresti Domiciliari |
|  | Rigetto revoca  prosecuzione arresti domiciliari ex art. 656 comma 10 | Ripristino arresti domiciliari ex art. 656 comma 10 | Ripristino arresti domiciliari ex art. 656 comma 10 |
|  | Rigetto revoca  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90 | Ripristino arresti domiciliari ex art 89 dpr 309/90 | Ripristino arresti domiciliari ex art 89 dpr 309/90 |
|  | Rigetto revoca  prosecuzione permanenza in casa  ex art. 656 comma 10 | Ripristino permanenza in casa  ex art. 656 comma 10 | Ripristino permanenza in casa  ex art. 656 comma 10 |
|  | Rigetto revoca  prosecuzione collocamento in comunità  ex art.  656 comma 10 | Ripristino collocamento in comunità  ex art.  656 comma 10 | Ripristino collocamento in comunità  ex art.  656 comma 10 |
|  | Perdita efficacia Sospensione provvisoria  prosecuzione arresti domiciliari ex art. 656 comma 10 | Ripristino arresti domiciliari ex art. 656 comma 10 - Emessa Comunicazione Scadenza Misura: [data provvedimento] | Ripristino arresti domiciliari ex art. 656 comma 10 - Emessa Comunicazione Scadenza Misura: [data provvedimento] |
|  | Perdita efficacia Sospensione provvisoria  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90 | Ripristino arresti domiciliari ex art 89 dpr 309/90- Emessa Comunicazione Scadenza Misura: [data provvedimento] | Ripristino arresti domiciliari ex art 89 dpr 309/90- Emessa Comunicazione Scadenza Misura: [data provvedimento] |
|  | Perdita efficacia Sospensione provvisoria  prosecuzione permanenza in casa  ex art. 656 comma 10 | Ripristino permanenza in casa  ex art. 656 comma 10 - Emessa Comunicazione Scadenza Misura: [data provvedimento] | Ripristino permanenza in casa  ex art. 656 comma 10 - Emessa Comunicazione Scadenza Misura: [data provvedimento] |
|  | Perdita efficacia Sospensione provvisoria  prosecuzione collocamento in comunità  ex art.  656 comma 10 | Ripristino collocamento in comunità  ex art.  656 comma 10 - Emessa Comunicazione Scadenza Misura: [data provvedimento] | Ripristino collocamento in comunità  ex art.  656 comma 10 - Emessa Comunicazione Scadenza Misura: [data provvedimento] |
| Revoca Arresti Domiciliari | Revoca Arresti Domiciliari | Revoca Arresti Domiciliari | Revoca Arresti Domiciliari |
|  | Revoca  Arresti domiciliari ex art. 656 comma 10 | Revoca  Arresti domiciliari ex art. 656 comma 10 - Emesso Ordine Esecuzione : [data provvedimento] | Revoca  Arresti domiciliari ex art. 656 comma 10 - Emesso Ordine Esecuzione : [data provvedimento] |
|  | Revoca   Arresti Domiciliari ex art 89 dpr 309/90 | Revoca   Permanenza in casa  ex art. 656 comma 10 - Emesso Ordine Esecuzione : [data provvedimento] | Revoca   Permanenza in casa  ex art. 656 comma 10 - Emesso Ordine Esecuzione : [data provvedimento] |
|  | Revoca   Permanenza in casa  ex art. 656 comma 10 | Revoca   Arresti Domiciliari ex art 89 dpr 309/90 - Emesso Ordine Esecuzione : [data provvedimento] | Revoca   Arresti Domiciliari ex art 89 dpr 309/90 - Emesso Ordine Esecuzione : [data provvedimento] |
|  | Revoca  Collocamento in comunità  ex art.  656 comma 10 | Revoca  Collocamento in comunità  ex art.  656 comma 10 - Emesso Ordine Esecuzione : [data provvedimento] | Revoca  Collocamento in comunità  ex art.  656 comma 10 - Emesso Ordine Esecuzione : [data provvedimento] |

Tabella 20 - Stato Procedimento



Figura 30 - Dettaglio procedimento - Elenco provvedimenti Sorveglianza

Il sistema dopo la selezione mostra l’elenco dei provvedimenti (Figura 31):


Figura 31 - Elenco provvedimenti
Per facilitare l’analisi del presente intervento e la discussione del medesimo è stato realizzato un prototipo.
Inoltra, l’implementazione dell’intervento deve essere coordinato con quella dell’intervento 18.Gestione Provvedimenti emessi dalla Magistratura di Sorveglianza.
## Riferimenti
Confronta “documento analisi 16_07_14.doc”.
## Sottosistema
La modifica interessa solo il sottosistema Siep.
## Uffici
L’intervento in parola riguarda tutti gli uffici.
## Modifiche  previste
## Modifica funzionalità
## Modifica interfacce utente
La maschera “Sospensione provvisoria Arresti Domiciliari” è composta dalle 4 seguenti sezioni:
Sezione “Funzione sospensione provvisoria”	(Figura 32)
Sezione “Dati salienti procedimento” 		(Figura 35)
Sezione “Dati posizione giuridica”		(Figura 36)
Sezione “Dati pena complessiva”         		(Figura 37)
Sezione “Dati inizio e fine pena”		(Figura 38)
Sezione “Decreto”				(Figura 40)
Sezione “Magistrato firmatario”          		(Figura 42)
Sezione “Destinatari decreto” 			(Figura 45) / (Figura 46)
Sezione “Conferma” 				(Figura 50).

Il campo “Data  ingresso in carcere” deve essere visibile unicamente  se l’operatore ha selezionato  il radiobutton  “Eseguita da Magistrato di Sorveglianza”.
Il campo “Oggetto Decreto” deve contenere i seguenti valori (Tabella 42):
Sospensione provvisoria  Arresti Domiciliari ex art. 656 comma 10
Sospensione provvisoria Domiciliari ex art. 89 dpr 309/90
Sospensione provvisoria Permanenza in Casa
Sospensione provvisoria Collocamento in Comunità.

La maschera di riferimento è quella della sospensione ex art. 51 ter della detenzione domiciliare.

A seguito del nuovo intervento devono essere create le  seguenti  nuove “Posizione giuridica” (Tabella 45):
Sospensione provvisoria 51 ter   Arresti Domiciliari ex art. 656 comma 10
Sospensione provvisoria 51 ter   Domiciliari ex art 89 dpr 309/90
Sospensione provvisoria 51 ter   Permanenza in Casa
Sospensione provvisoria 51 ter   Collocamento in Comunità.
La maschera “Revoca Arresti Domiciliari  e Rigetta applicazione misura alternativa” è composta dalle 4 seguenti sezioni:
Sezione “Funzione revoca”			(Figura 33)
Sezione “Dati salienti procedimento” 		(Figura 35)
Sezione “Dati posizione giuridica”		(Figura 36)
Sezione “Dati pena complessiva”       	  	(Figura 37)
Sezione “Dati inizio e fine pena”		(Figura 38)
Sezione “Ordinanza  revoca”        		(Figura 39)
Sezione “Magistrato firmatario”      	    	(Figura 42)
Sezione “Destinatari ordinanza”		(Figura 43) / (Figura 44)
Sezione “Destinatari per notifica” 		(Figura 49)
Sezione “Conferma” 				(Figura 50).

Il campo “Oggetto Ordinanza” deve contenere i seguenti valori (Tabella 43):
Revoca Arresti Domiciliari ex art. 656 comma 10
Revoca Domiciliari ex art. 89 dpr 309/90
Revoca Permanenza in Casa
Revoca Collocamento in Comunità.

La maschera di riferimento è quella della revoca della detenzione domiciliare.
La maschera “Ripristino Degli Arresti Domiciliari ” è composta dalle 4 seguenti sezioni:
Sezione “Funzione ripristino”			(Figura 34)
Sezione “Dati salienti procedimento” 		(Figura 35)
Sezione “Dati posizione giuridica”		(Figura 36)
Sezione “Dati pena complessiva”         		(Figura 37)
Sezione “Dati inizio e fine pena”		(Figura 47)
Sezione “Magistrato firmatario”       	   	(Figura 42)
Sezione “Destinatari ordinanza”		(Figura 47) / (Figura 48)
Sezione “Conferma” 		      		(Figura 50).

Il campo “Oggetto Decisione” deve contenere i seguenti valori (Tabella 44):
Rigetto revoca prosecuzione arresti domiciliari ex art. 656 comma 10
Rigetto revoca prosecuzione Arresti Domiciliari ex art 89 dpr 309/90
Rigetto revoca prosecuzione permanenza in casa  ex art. 656 comma 10
Rigetto revoca prosecuzione collocamento in comunità  ex art.  656 comma 10
Perdita di efficacia -  Sospensione provvisoria  prosecuzione arresti domiciliari ex art. 656 comma 10
Perdita di efficacia - Sospensione provvisoria  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90
Perdita di efficacia - Sospensione provvisoria  prosecuzione permanenza in casa  ex art. 656 comma 10
Perdita di efficacia - Sospensione provvisoria  prosecuzione collocamento in comunità  ex art.  656 comma 10.

La maschera di riferimento è quella della ripristino della detenzione domiciliare.


Figura 32 – Sezione A - Funzione sospensione provvisoria


Figura 33 – Sezione B - Funzione revoca


Figura 34 – Sezione C - Funzione ripristino


Figura 35 – Sezione D - Dati salienti procedimento


Figura 36 – Sezione E - Dati posizione giuridica


Figura 37 – Sezione F - Dati pena complessiva


Figura 38 - Sezione G - Dati inzio e fine pena


Figura 39 – Sezione H - Ordinanza revoca


Figura 40 – Sezione I – Decreto Sospensione


Figura 41 – Sezione L – Ordinanza/Decreto ripristino


Figura 42 – Sezione M - Magistrato firmatario


Figura 43 – Sezione N - Destinatari ordinanza revoca diretta


Figura 44 – Sezione O - Destinatari ordinanza revoca dopo sospensione


Figura 45 – Sezione P - Destinatari decreto Sospensione – Eseguita Procura


Figura 46 – Sezione Q - Destinatari decreto – Eseguita Magistrato di Sorveglianza


Figura 47 – Sezione R - Destinatari ordinanza ripristino – Eseguita Procura


Figura 48 – Sezione S - Destinatari ordinanza ripristino – Eseguita Sorveglianza




Figura 49 – Sezione T - Destinatari per la notifica


Figura 50 – Sezione U - Conferma
## Modifica interfacce software/algoritmi
Il sistema nella valorizzazione dei campi deve seguire le seguenti regole:
| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Funzione |  |  | Nome della funzione |

Tabella 21 – Sezione A – Funzione sospensione provvisoria

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Funzione |  |  | Nome della funzione |

Tabella 22 – Sezione B – Funzione revoca

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Funzione |  |  | Nome della funzione |

Tabella 23 – Sezione C – Funzione ripristino

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Procedimento N. |  |  | Anno/Numero procedimento |
|  | Soggetto |  |  | Cognome e Nome del soggetto |
|  | Nato il |  |  | Data di nascita del soggetto |
|  | In |  |  | Luogo di nascita del soggetto |
|  | Sentenza N. |  |  | Numero sentenza |
|  | Data Sentenza |  |  | Data della sentenza |
|  | Emessa da |  |  | Ufficio che ha emesso la sentenza |

Tabella 24 – Sezione D – Dati salienti procedimento

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Posizione giuridica |  |  | Posizione giuridica iniziale (del momento di accesso alla funzione) del soggetto |

Tabella 25 – Sezione E – Posizione giuridica iniziale

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Reclusione |  |  | Reclusione: Anni, Mesi e Giorni |
|  | Multa |  |  |  |

Tabella 26 – Sezione F – Dati pena complessiva

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Data decorrenza pena |  |  | Data di decorrenza della pena |
|  | Data fine pena |  |  | Data di fine della pena |

Tabella 27 – Sezione G – Dati inizio e fine pena

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Data Emissione |  |  | Data (2 gg 2 mm 4 anno) – controllare correttezza formale data  
Data iscrizione procedimento <= data <= data di sistema |
|  | Data Trasmissione |  |  | Data (2 gg 2 mm 4 anno) – controllare correttezza formale data  
Data iscrizione procedimento <= data <= data di sistema |
|  | Seleziona provvedimento di Sorveglianza dalla lista |  |  | L’operatore può valorizzare le informazioni della sezione selezionando un provvedimento tramite la funzione già presente della “Selezione provvedimento di Sorveglianza dalla lista”.
In alternativa, le informazioni possono essere valorizzate dall’operatore. |
|  | Anno SIUS |  | 4 | Testo valorizzato dall’utente. 4 cifre [0..9] |
|  | Numero SIUS |  | 6 | Testo valorizzato dall’utente. 6 cifre [0..9] |
|  | Anno Ordinanza |  | 4 | Testo valorizzato dall’utente. 4 cifre [0..9] |
|  | Numero Ordinanza |  | 6 | Testo valorizzato dall’utente. 6 cifre [0..9] |
|  | Ufficio Emittente | * |  | Valorizzato dall’operatore tramite la selezione di un valore presente nel seguente elenco:
{ “Tribunale di Sorveglianza” 
“Ufficio di Sorveglianza” 
“Magistrato di Sorveglianza per i Minorenni”
“Tribunale per Minorenni in funzione di Tribunale di Sorveglianza”}.
L’elenco è popolato selezionando le voci dalla tabella <CG_REF_CODES>  aventi <RV_DOMAIN> = “TIPO_UFFICIO” e <RV_LOW_VALUE> = ad uno dei seguenti valori “TDS”,”UDS”,”TDSM” e  ”UDSM”.
Prevalorizzato uguale a “-”. |
|  | Sede Ufficio Emittente | * |  | Valorizzato tramite funzione “Ricerca comune”, valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali. |
|  | Oggetto Ordinanza |  |  | Valorizzato dall’operatore tramite la selezione di un valore presente nel seguente elenco:
 {“Revoca Arresti domiciliari ex art. 656 comma 10”
“Revoca Arresti Domiciliari ex art 89 dpr 309/90”
“Revoca Permanenza in casa  ex art. 656 comma 10”
“Revoca Collocamento in comunità  ex art.  656 comma 10”}.
L’elenco è popolato selezionando dalla tabella <CG_REF_CODES> le tuple aventi il campo <RV_DOMAIN> = “MOTIVO_PROVVEDIMENTO” e <RV_LOW_VALUE> = ad uno valori indicati nella Tabella 43 - Tabella <CG_REF_CODES>- Ordinanza revoca.
Prevalorizzato uguale a “-“ |
|  | Data Emissione Ordinanza |  |  | Data (2 gg 2 mm 4 anno) – controllare correttezza formale data  
Data iscrizione procedimento <= data <= data di sistema
Prevalorizzata con la data di sistema |
|  | Note |  |  | Testo libero max 1000 caratteri alfanumerici |

Tabella 28 – Sezione H - Ordinanza revoca

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Data Emissione |  |  | Data (2 gg 2 mm 4 anno) – controllare correttezza formale data  
Data iscrizione procedimento <= data <= data di sistema |
|  | Data Trasmissione |  |  | Data (2 gg 2 mm 4 anno) – controllare correttezza formale data  
Data iscrizione procedimento <= data <= data di sistema |
|  | Seleziona provvedimento di Sorveglianza dalla lista |  |  | L’operatore può valorizzare le informazioni della sezione selezionando un provvedimento tramite la funzione già presente della “Selezione provvedimento di Sorveglianza dalla lista”.
In alternativa, le informazioni possono essere valorizzate dall’operatore. |
|  | Anno SIUS |  | 4 | Testo valorizzato dall’utente. 4 cifre [0..9] |
|  | Numero SIUS |  | 6 | Testo valorizzato dall’utente. 6 cifre [0..9] |
|  | Anno Decreto |  | 4 | Testo valorizzato dall’utente. 4 cifre [0..9] |
|  | Numero Decreto |  | 6 | Testo valorizzato dall’utente. 6 cifre [0..9] |
|  | Ufficio Emittente | * |  | Valorizzato tramite elenco uffici prelevato da tabella <CG_REF_CODES>  con campo <RV_DOMAIN> = ‘TIPO_UFFICIO’.
Valorizzato dall’operatore tramite la selezione di un valore presente nel seguente elenco:
{“Tribunale di Sorveglianza”
“Ufficio di Sorveglianza”
“Magistrato di Sorveglianza per i Minorenni”
“Tribunale per Minorenni in funzione di Tribunale di Sorveglianza”}.
L’elenco è popolato selezionando le voci dalla tabella <CG_REF_CODES>  aventi <RV_DOMAIN> = “TIPO_UFFICIO” e <RV_LOW_VALUE> = ad uno dei seguenti valori “TDS”,”UDS”,”TDSM” e  ”UDSM”.
Prevalorizzato uguale a “-”. |
|  | Sede Ufficio Emittente | * |  | Valorizzato tramite funzione “Ricerca comune”  in relazione alla selezione della Autorità, valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali. |
|  | Oggetto Decreto |  |  | Valorizzato dall’operatore tramite la selezione di un valore presente nel seguente elenco:
{“Sospensione provvisoria  Arresti Domiciliari ex art. 656 comma 10”, 
“Sospensione provvisoria Domiciliari ex art. 89 dpr 309/90”, 
“Sospensione provvisoria Permanenza in Casa”,
”Sospensione provvisoria Collocamento in Comunità”}.
L’elenco è popolato selezionando dalla tabella <CG_REF_CODES> le tuple aventi il campo <RV_DOMAIN> = “MOTIVO_PROVVEDIMENTO” e <RV_LOW_VALUE> = ad uno valori indicati nella Tabella 42 - Tabella <CG_REF_CODES>-Decreto sospensione.
Prevalorizzato uguale a “-”. |
|  | Data Emissione decreto |  |  | Data (2 gg 2 mm 4 anno) – controllare correttezza formale data  
Data iscrizione procedimento <= data <= data di sistema
Prevalorizzata con la data di sistema |
|  | Note |  |  | Testo libero max 1000 caratteri alfanumerici |
|  | Eseguita Procura |  |  | Prevalorizzato come selezionato, modificabile dall’operatore |
|  | Eseguita Magistrato Sorveglianza |  |  |  |
|  | Data Ingresso in Carcere |  |  | Visibile solo se misura eseguita da Magistrato di Sorveglianza
Data (2 gg 2 mm 4 anno) – controllare correttezza formale data  
Data iscrizione procedimento <= data <= data di sistema |

Tabella 29 – Sezione I – Decreto Sospensione


| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Data Emissione |  |  | Data (2 gg 2 mm 4 anno) – controllare correttezza formale data  
Data iscrizione procedimento <= data <= data di sistema |
|  | Data Trasmissione |  |  | Data (2 gg 2 mm 4 anno) – controllare correttezza formale data  
Data iscrizione procedimento <= data <= data di sistema |
|  | Seleziona provvedimento di Sorveglianza dalla lista |  |  | L’operatore può valorizzare le informazioni della sezione selezionando un provvedimento tramite la funzione già presente della “Selezione provvedimento di Sorveglianza dalla lista”.
In alternativa, le informazioni possono essere valorizzate dall’operatore. |
|  | Anno SIUS |  | 4 | Testo valorizzato dall’utente. 4 cifre [0..9] |
|  | Numero SIUS |  | 6 | Testo valorizzato dall’utente. 6 cifre [0..9] |
|  | Anno Decisione |  | 4 | Testo valorizzato dall’utente. 4 cifre [0..9] |
|  | Numero Decisione |  | 6 | Testo valorizzato dall’utente. 6 cifre [0..9] |
|  | Ufficio Emittente | * |  | Popolato tramite elenco uffici prelevato da tabella <CG_REF_CODES>  con campo <RV_DOMAIN> = ‘TIPO_UFFICIO’.
Valorizzato dall’operatore tramite la selezione di un valore presente nel seguente elenco:
{ “Tribunale di Sorveglianza”
“Ufficio di Sorveglianza”
“Magistrato di Sorveglianza per i Minorenni”
“Tribunale per Minorenni in funzione di Tribunale di Sorveglianza”}.
L’elenco è popolato selezionando le voci dalla tabella <CG_REF_CODES>  aventi <RV_DOMAIN> = “TIPO_UFFICIO” e <RV_LOW_VALUE> = ad uno dei seguenti valori “TDS”,”UDS”,”TDSM” e  ”UDSM”.
Prevalorizzato uguale a “-”. |
|  | Sede Ufficio Emittente | * |  | Valorizzato tramite funzione “Ricerca comune” in relazione alla selezione della Autorità, valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali. |
|  | Tipo Provvedimento | * |  | Valorizzato dall’operatore tramite la selezione di un valore presente nel seguente elenco:
{“Decreto”, “Ordinanza”}. Prevalorizzato uguale a “Ordinanza”. |
|  | Oggetto Decisione | * |  | Se l’operatore seleziona “Ufficio Emittente” = a  “Tribunale di Sorveglianza” oppure = a “Tribunale per Minorenni in funzione di Tribunale di Sorveglianza”,  valorizzato dall’operatore tramite la selezione di un valore presente nel seguente elenco:
{“Rigetto revoca  prosecuzione arresti domiciliari ex art. 656 comma 10”
“Rigetto revoca  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90”
“Rigetto revoca  prosecuzione permanenza in casa  ex art. 656 comma 10”
“Rigetto revoca  prosecuzione collocamento in comunità  ex art.  656 comma 10”}.

Se l’operatore seleziona “Ufficio Emittente” = a  “Magistrato di Sorveglianza” oppure = a “Magistrato di Sorveglianza per Minorenni”,  valorizzato dall’operatore tramite la selezione di un valore presente nel seguente elenco:
{“Perdita di efficacia -  Sospensione provvisoria  prosecuzione arresti domiciliari ex art. 656 comma 10”
“Perdita di efficacia - Sospensione provvisoria  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90”
“Perdita di efficacia - Sospensione provvisoria  prosecuzione permanenza in casa  ex art. 656 comma 10”
“Perdita di efficacia - Sospensione provvisoria  prosecuzione collocamento in comunità  ex art.  656 comma 10”.
L’elenco è popolato selezionando dalla tabella <CG_REF_CODES> le tuple aventi il campo <RV_DOMAIN> = “MOTIVO_PROVVEDIMENTO” e <RV_LOW_VALUE> = ad uno valori indicati nella Tabella 44 - Tabella <CG_REF_CODES>- Ordinanza/decreto  ripristino.
Prevalorizzato uguale a “-”. |
|  | Data Emissione Decisione |  |  | Data (2 gg 2 mm 4 anno) – controllare correttezza formale data  
Data iscrizione procedimento <= data <= data di sistema
Prevalorizzata con la data di sistema |
|  | Luogo della Detenzione |  |  | Testo libero max 1000 caratteri alfanumerici |
|  | Note |  |  | Testo libero max 1000 caratteri alfanumerici |
|  | Eseguita Procura |  |  |  |
|  | Eseguita dalla Sorveglianza |  |  |  |
|  | Data Scarcerazione |  |  | Data (2 gg 2 mm 4 anno) – controllare correttezza formale data  
Data iscrizione procedimento <= data <= data di sistema |

Tabella 30 –  Sezione L – Ordinanza/Decreto ripristino

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Cognome Magistrato |  |  | Valorizzato il  magistrato tramite la funzione di “Ricerca Magistrato Ufficio”.
Prevalorizzato con il magistrato assegnato al procedimento, modificabile dall’operatore |
|  | Nome Magistrato |  |  |  |

Tabella 31 –  Sezione M - Magistrato firmatario

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Autorità Competente per Territorio | * |  | Valorizzato tramite elenco autorità prelevato da tabella <CF_REF_CODES> con campo <RV_DOMAIN> = ‘TIPO_AUTORITA’. |
|  | Sede |  |  | Valorizza la sede tramite la funzione di “Ricerca comune”, valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali. |
|  | Indirizzo |  |  | Testo libero max 1000 caratteri alfanumerici |
|  | Ufficio di Sorveglianza | * |  | Valorizza l’ufficio tramite la funzione di “Ricerca Ufficio  di Sorveglianza”, valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali.
Vedere per minorenni |
|  | Tribunale di Sorveglianza | * |  | Valorizza tribunale tramite la funzione di “Ricerca Tribunale  di Sorveglianza”, valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali.
Vedere per minorenni |

Tabella 32 –  Sezione N - Destinatari ordinanza Revoca diretta

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Autorità Competente per Territorio | * |  | Valorizzato tramite elenco autorità prelevato da tabella <CF_REF_CODES> con campo <RV_DOMAIN> = ‘TIPO_AUTORITA’. |
|  | Sede |  |  | Valorizza la sede tramite la funzione di “Ricerca comune”, valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali. |
|  | Indirizzo |  |  | Testo libero max 1000 caratteri alfanumerici |
|  | Ufficio di Sorveglianza | * |  | Valorizza l’ufficio tramite la funzione di “Ricerca Ufficio  di Sorveglianza”, valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali.
Vedere per minorenni |
|  | Tribunale di Sorveglianza | * |  | Valorizza tribunale tramite la funzione di “Ricerca Tribunale  di Sorveglianza”, valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali.
Vedere per minorenni |

Tabella 33 –  Sezione N - Destinatari ordinanza Revoca diretta
| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Istituto di Detenzione | * |  | Valorizzabile tramite la funzione di “Ricerca Istituto di Detenzione”.
Per l’ambito dei minorenni la funzione deve permettere all’operatore di selezionare tra l’elenco degli istituti di Detenzione minorili (Vedere  intervento successivo). |
|  | Ufficio di Sorveglianza | * |  | Valorizza l’ufficio tramite la funzione di “Ricerca Ufficio  di Sorveglianza”, valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali.
Vedere per minorenni |
|  | Tribunale di Sorveglianza | * |  | Valorizza tribunale tramite la funzione di “Ricerca Tribunale  di Sorveglianza”, valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali.
Vedere per minorenni |

Tabella 34 –  Sezione O - Destinatari ordinanza Revoca dopo Sospensione

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Autorità di Competente per Territorio | * |  | Valorizzato tramite elenco autorità prelevato da tabella <CG_REF_CODES> con campo <RV_DOMAIN> = ‘TIPO_AUTORITA’.
L’elenco deve contenere:
{Carabinieri
Carabinieri - Comando Compagnia
Carabinieri - Comando Provinciale
Carabinieri - Comando Regionale
Carabinieri - Comando Stazione
Carabinieri - Nucleo Operativo
Commissariato di P.S.
Polizia di Stato
Questura
Questura - Ufficio Stranieri
Questura Divisione Anticrimine
Servizio Centrale Protezione c/o Ministero dell'Interno
Guardia di Finanza}.
Prevalorizzato uguale a “-“ |
|  | Sede |  |  | Valorizza la sede tramite la funzione di “Ricerca comune”, valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali. |
|  | Indirizzo |  |  | Testo libero max 1000 caratteri alfanumerici |
|  | Ufficio di Sorveglianza | * |  | Valorizza l’ufficio tramite la funzione di “Ricerca Ufficio  di Sorveglianza”, valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali.
Per l’ambito dei minorenni la funzione deve permettere all’operatore di selezionare tra l’elenco dei Magistrato di Sorveglianza per i minorenni (Vedere  intervento successivo). |
|  | Tribunale di Sorveglianza | * |  | Valorizza tribunale tramite la funzione di “Ricerca Tribunale  di Sorveglianza” , valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali.
Per l’ambito dei minorenni la funzione deve permettere all’operatore di selezionare tra l’elenco dei Tribunali per i minorenni in funzione di Tribunale di sorveglianza (Vedere  intervento successivo). |

Tabella 35 –  Sezione P - Destinatari decreto Sospensione – Eseguita Procura

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Istituto di Detenzione | * |  | Valorizzabile tramite la funzione di “Ricerca Istituto di Detenzione”.
Per l’ambito dei minorenni la funzione deve permettere all’operatore di selezionare tra l’elenco degli istituti di Detenzione minorili (Vedere  intervento successivo). |
|  | Ufficio di Sorveglianza | * |  | Valorizza l’ufficio tramite la funzione di “Ricerca Ufficio  di Sorveglianza”, valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali.
Per l’ambito dei minorenni la funzione deve permettere all’operatore di selezionare tra l’elenco dei Magistrato di Sorveglianza per i minorenni (Vedere  intervento successivo). |
|  | Tribunale di Sorveglianza | * |  | Valorizza tribunale tramite la funzione di “Ricerca Tribunale  di Sorveglianza” , valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali.
Per l’ambito dei minorenni la funzione deve permettere all’operatore di selezionare tra l’elenco dei Tribunali per i minorenni in funzione di Tribunale di sorveglianza (Vedere  intervento successivo). |

Tabella 36 –  Sezione Q - Destinatari decreto Sospensione – Eseguita Magistrato di Sorveglianza

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Autorità Competente per Terrritorio | * |  | Valorizzato tramite elenco autorità prelevato da tabella <CG_REF_CODES> con campo <RV_DOMAIN> = ‘TIPO_AUTORITA’.
L’elenco deve contenere:
{Carabinieri
Carabinieri - Comando Compagnia
Carabinieri - Comando Provinciale
Carabinieri - Comando Regionale
Carabinieri - Comando Stazione
Carabinieri - Nucleo Operativo
Commissariato di P.S.
Polizia di Stato
Questura
Questura - Ufficio Stranieri
Questura Divisione Anticrimine
Servizio Centrale Protezione c/o Ministero dell'Interno
Guardia di Finanza}.
Prevalorizzato uguale a “-“ |
|  | Sede |  |  | Valorizza la sede tramite la funzione di “Ricerca comune” , valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali. |
|  | Indirizzo |  |  | Testo libero max 1000 caratteri alfanumerici |
|  | Istituto di Detenzione | * |  | Valorizzabile tramite la funzione di “Ricerca Istituto di Detenzione”.
Per l’ambito dei minorenni la funzione deve permettere all’operatore di selezionare tra l’elenco degli istituti di Detenzione minorili (Vedere  intervento successivo). |
|  | UEPE | * |  | Valorizzabile tramite la funzione di “UEPE”.
Per l’ambito dei minorenni la funzione deve permettere all’operatore di selezionare tra l’elenco degli USSM e USSMSS (Vedere  intervento successivo). |
|  | Ufficio di Sorveglianza | * |  | Valorizza l’ufficio tramite la funzione di “Ricerca Ufficio  di Sorveglianza”, , valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali.
Per l’ambito dei minorenni la funzione deve permettere all’operatore di selezionare tra l’elenco dei Magistrato di Sorveglianza per i minorenni (Vedere  intervento successivo). |
|  | Tribunale di Sorveglianza | * |  | Valorizza tribunale tramite la funzione di “Ricerca Tribunale  di Sorveglianza” , valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali.
Per l’ambito dei minorenni la funzione deve permettere all’operatore di selezionare tra l’elenco dei Tribunali per i minorenni in funzione di Tribunale di sorveglianza (Vedere  intervento successivo). |

Tabella 37 –  Sezione R- Destinatari ordinanza di ripristino – Eseguita Procura

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Autorità Competente per Terrritorio | * |  | Valorizzato tramite elenco autorità prelevato da tabella <CG_REF_CODES> con campo <RV_DOMAIN> = ‘TIPO_AUTORITA’.
L’elenco deve contenere:
{Carabinieri
Carabinieri - Comando Compagnia
Carabinieri - Comando Provinciale
Carabinieri - Comando Regionale
Carabinieri - Comando Stazione
Carabinieri - Nucleo Operativo
Commissariato di P.S.
Polizia di Stato
Questura
Questura - Ufficio Stranieri
Questura Divisione Anticrimine
Servizio Centrale Protezione c/o Ministero dell'Interno
Guardia di Finanza}.
Prevalorizzato uguale a “-“ |
|  | Sede |  |  | Valorizza la sede tramite la funzione di “Ricerca comune” , valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali. |
|  | Indirizzo |  |  | Testo libero max 1000 caratteri alfanumerici |
|  | UEPE | * |  | Valorizzabile tramite la funzione di “UEPE”.
Per l’ambito dei minorenni la funzione deve permettere all’operatore di selezionare tra l’elenco degli USSM e USSMSS (Vedere  intervento successivo). |
|  | Ufficio di Sorveglianza | * |  | Valorizza l’ufficio tramite la funzione di “Ricerca Ufficio  di Sorveglianza”, , valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali.
Per l’ambito dei minorenni la funzione deve permettere all’operatore di selezionare tra l’elenco dei Magistrato di Sorveglianza per i minorenni (Vedere  intervento successivo). |
|  | Tribunale di Sorveglianza | * |  | Valorizza tribunale tramite la funzione di “Ricerca Tribunale  di Sorveglianza” , valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali.
Per l’ambito dei minorenni la funzione deve permettere all’operatore di selezionare tra l’elenco dei Tribunali per i minorenni in funzione di Tribunale di sorveglianza (Vedere  intervento successivo). |

Tabella 38 –  Sezione S- Destinatari ordinanza di ripristino – Eseguita Sorveglianza

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Avvocato |  |  | Cognome e nome del difensore - non modificabile dall’operatore |
|  | Foro di |  |  | Foro del difensore – non modificabile dall’operatore |
|  | Rapporto |  |  | Rapporto tra soggetto e difensore – non modificabile dall’operatore |
|  | Ufficio di Destinazione | * |  | Valorizzato tramite elenco autorità prelevato da tabella <CF_REF_CODES> con campo <RV_DOMAIN> = ‘TIPO_AUTORITA’.
Prevalorizzato uguale a “UNEP” |
|  | Sede |  |  | Valorizza la sede tramite la funzione di “Ricerca comune”, valorizzabile manualmente dall’operatore.
Il sistema verifica che l’ufficio esista, se l’ufficio non esiste il sistema con apposito messaggio avvisa l’operatore. Il sistema ripresenta all’operatore la finestra con i valori iniziali.
Prevalorizzato con la località sede dell’operatore. |
|  | Note |  |  | Testo libero max 1000 caratteri alfanumerici |

Tabella 39 –  Sezione T - Destinatari per notifica

Dopo l’inserimento di una misura alternativa – decreto di sospensione -   il sistema popola alla fine dell’intero percorso le seguenti tabelle:
| <DEPOSITO_DECRETO> |
| --- |
| <EVENTO> |
| <MISURA_ALTERNATIVA> |
| <NOME_PROVVEDIMENTO> |
| <NOTIFICA> |
| <PENA_RESIDUA> |
| <POSIZIONE_GIURIDICA> |
| <SCADENZARIO_SIEP>
<TENORE>. |


Secondo il seguente diagramma:


Figura 51 – Diagramma inserimento decreto sospensione

Il sistema inserisce generalmente 1 record ma il numero tra parentesi quadre indica il numero di record inseriti.
La descrizione “Evento [2]” indica che la associazione avviene con il secondo record della tabella <EVENTO>.

Dopo l’inserimento di una misura alternativa – ordinanza di revoca -   il sistema popola alla fine dell’intero percorso le seguenti tabelle:
| <DEPOSITO_ORDINANZA_PC> |
| --- |
| <EVENTO> |
| <MISURA_ALTERNATIVA> |
| <NOME_PROVVEDIMENTO> |
| <NOTIFICA> |
| <PENA_RESIDUA> |
| <POSIZIONE_GIURIDICA> |
| <TENORE>. |



Secondo il seguente diagramma:


Figura 52 – Diagramma inserimento ordinanza revoca
Dopo l’inserimento di una misura alternativa – ordinanza di ripristino -   il sistema popola alla fine dell’intero percorso le seguenti tabelle:
| <DEPOSITO_ORDINANZA_PC> |
| --- |
| <EVENTO> |
| <MISURA_ALTERNATIVA> |
| <NOME_PROVVEDIMENTO> |
| <NOTIFICA> |
| <PENA_RESIDUA> |
| <POSIZIONE_GIURIDICA > |
| <SCADENZARIO_SIEP> |
| <TENORE>. |

Secondo il seguente diagramma:


Figura 53 – Diagramma inserimento ordinanza ripristino
Il sistema inserisce nella tabella 1 record per ogni destinatario di notifica.
Il numero dei record inseriti varia in relazione alla decisione della sorveglianza (sospensione, revoca e rispristino.
I destinatari delle notifiche possono essere:
l’autorità esterna
l’avvocato
l’Uepe (CSSA)		        [per i minorenni l’ufficio è denominato USSM]
l’istituto di detenzione
il Tribunale di Sorveglianza   [(TDS) per i maggiorenni  / (TDSM) per i minorenni]
il Magistrato di Sorveglianza [(UDS) per i maggiorenni  / (UDSM) per i minorenni].

Il sistema popola la tabella <NOTIFICA> secondo il seguente riepilogo:

| N. | Campo | Provvedimento | Provvedimento | Provvedimento | Provvedimento | Provvedimento | Nota | Nota |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| N. | Campo | Decreto sospensione | Decreto sospensione | Ordinanza revoca | Ordinanza ripristino | Ordinanza ripristino | Nota | Nota |
|  |  | Esegue
Procura | Esegue
Sorveglianza |  |  |  |  |  |
|  | COD_TIPO_NOTIFICA | E | E | E | E |  |  |  |
|  |  | C | C | C | C |  |  |  |
|  |  | C | C | N | C |  |  |  |
|  |  |  |  | C | C |  |  |  |
|  |  |  |  |  | C |  |  |  |
| A | AUT_EST_ID_AUTORITA_ESTERNA | X |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |  |
|  |  |  |  | X |  |  |  |  |
|  |  |  |  |  |  |  |  |  |
|  |  |  |  |  | X |  |  |  |
| B | AVV_ID_AVVOCATO_FASCICOLO_SIEP |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |  |
|  |  |  |  | X |  |  |  |  |
|  |  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |  |
| C | CSS_ID_CSSA |  |  |  |  |  |  |  |
|  |  |  |  |  | X |  |  |  |
|  |  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |  |
| D | IST_DET_ID_ISTITUTO_DETENZIONE |  | X | X | X |  |  |  |
|  |  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |  |
| E | UFF_COD_UFFICIO 
TDS/TDSM |  |  |  |  | (tipo ufficio TDS/TDSM) | (tipo ufficio TDS/TDSM) | (tipo ufficio TDS/TDSM) |
|  |  |  |  | X |  |  |  |  |
|  |  | X | X |  |  |  |  |  |
|  |  |  |  |  | X |  |  |  |
|  |  |  |  |  |  |  |  |  |
| F | UFF_COD_UFFICIO |  |  |  |  | (tipo ufficio UDS/UDSM) | (tipo ufficio UDS/UDSM) | (tipo ufficio UDS/UDSM) |
|  |  | X | X |  |  |  |  |  |
|  |  |  |  |  | X |  |  |  |
|  |  |  |  | X |  |  |  |  |
|  |  |  |  |  |  |  |  |  |

Tabella 40 - Valorizzazione tabella <Notifica>

Il sistema valorizza il campo <COD_TIPO_NOTIFICA>  con i seguenti 3 valori prelevati dalla tabella <CG_REF_CODES> ed avente campo <RV_DOMAIN> = “TIPO_NOTIFICA”:

| N. | <RV_LOW_VALUE> | <RV_LOW_VALUE> | <RV_MEANING> |
| --- | --- | --- | --- |
|  |  | “C” | “Comunicazione” |
|  |  | “E” | “Esecuzione” |
|  |  | “N” | “Notifica” |

Tabella 41 - Valorizzazione <COD_TIPO_NOTIFICA>

Inoltre, il sistema traccia le attività eseguite nella tabella <LOG_ATTIVITA>.

## Modifica database
Per l’oggetto del decreto di sospensione, l’intervento prevede l’inserimento nella tabella <CG_REF_CODES> delle seguenti voci:
| N. | RV_DOMAIN | RV_LOW_VALUE | RV_HIGH_VALUE | RV_ABBREVIATION | RV_MEANING | RV_ALT2_VALUE | RV_ALT3_VALUE | RV_ALT4_VALUE | RV_ALT5_VALUE |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | MOTIVO_PROVVEDIMENTO | 2756 | C046 | Sospensione provvisoria  Arresti Domiciliari ex art. 656 comma 10 | Sospensione provvisoria  Arresti Domiciliari ex art. 656 comma 10 | NULL | NULL | NULL | NULL |
|  | MOTIVO_PROVVEDIMENTO | 2741 | C046 | Sospensione provvisoria Domiciliari ex art. 89 dpr 309/90 | Sospensione provvisoria Domiciliari ex art. 89 dpr 309/90 | NULL | NULL | NULL | NULL |
|  | MOTIVO_PROVVEDIMENTO | 2742 | C046 | Sospensione provvisoria Permanenza in Casa | Sospensione provvisoria Permanenza in Casa | NULL | NULL | NULL | NULL |
|  | MOTIVO_PROVVEDIMENTO | 2743 | C046 | Sospensione provvisoria Collocamento in Comunità. | Sospensione provvisoria Collocamento in Comunità. | NULL | NULL | NULL | NULL |

Tabella 42 - Tabella <CG_REF_CODES>-Decreto sospensione
Per l’oggetto dell’ordinanza di revoca, l’intervento prevede l’inserimento nella tabella <CG_REF_CODES> delle seguenti voci:
| N. | RV_DOMAIN | RV_LOW_VALUE | RV_HIGH_VALUE | RV_ABBREVIATION | RV_MEANING | RV_ALT2_VALUE | RV_ALT3_VALUE | RV_ALT4_VALUE | RV_ALT5_VALUE |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | MOTIVO_PROVVEDIMENTO | 2744 | C046 | Revoca Arresti Domiciliari ex art. 656 comma 10 | Revoca Arresti Domiciliari ex art. 656 comma 10 | NULL | NULL | NULL | NULL |
|  | MOTIVO_PROVVEDIMENTO | 2757 | C046 | Revoca Domiciliari ex art. 89 dpr 309/90 | Revoca Domiciliari ex art. 89 dpr 309/90 | NULL | NULL | NULL | NULL |
|  | MOTIVO_PROVVEDIMENTO | 2746 | C046 | Revoca Permanenza in Casa | Revoca Permanenza in Casa | NULL | NULL | NULL | NULL |
|  | MOTIVO_PROVVEDIMENTO | 2747 | C046 | Revoca Collocamento in Comunità. | Revoca Collocamento in Comunità. | NULL | NULL | NULL | NULL |

Tabella 43 - Tabella <CG_REF_CODES>- Ordinanza revoca
Per l’oggetto dell’ordinanza/decreto di ripristino, l’intervento prevede l’inserimento nella tabella <CG_REF_CODES> delle seguenti voci:
| N. | RV_DOMAIN | RV_LOW_VALUE | RV_HIGH_VALUE | RV_ABBREVIATION | RV_MEANING | RV_ALT2_VALUE | RV_ALT3_VALUE | RV_ALT4_VALUE | RV_ALT5_VALUE |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | MOTIVO_PROVVEDIMENTO | 2748 | C046 | Rigetto revoca  prosecuzione arresti domiciliari ex art. 656 comma 10 | Rigetto revoca  prosecuzione arresti domiciliari ex art. 656 comma 10 | NULL | NULL | NULL | NULL |
|  | MOTIVO_PROVVEDIMENTO | 2749 | C046 | Rigetto revoca  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90 | Rigetto revoca  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90 | NULL | NULL | NULL | NULL |
|  | MOTIVO_PROVVEDIMENTO | 2758 | C046 | Rigetto revoca  prosecuzione permanenza in casa  ex art. 656 comma 10 | Rigetto revoca  prosecuzione permanenza in casa  ex art. 656 comma 10 | NULL | NULL | NULL | NULL |
|  | MOTIVO_PROVVEDIMENTO | 2759 | C046 | Rigetto revoca  prosecuzione collocamento in comunità  ex art.  656 comma 10 | Rigetto revoca  prosecuzione collocamento in comunità  ex art.  656 comma 10 | NULL | NULL | NULL | NULL |
|  | MOTIVO_PROVVEDIMENTO | 2752 | C046 | Perdita di efficacia -  Sospensione provvisoria  prosecuzione arresti domiciliari ex art. 656 comma 10 | Perdita di efficacia -  Sospensione provvisoria  prosecuzione arresti domiciliari ex art. 656 comma 10 | NULL | NULL | NULL | NULL |
|  | MOTIVO_PROVVEDIMENTO | 2753 | C046 | Perdita di efficacia - Sospensione provvisoria  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90 | Perdita di efficacia - Sospensione provvisoria  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90 | NULL | NULL | NULL | NULL |
|  | MOTIVO_PROVVEDIMENTO | 2754 | C046 | Perdita di efficacia - Sospensione provvisoria  prosecuzione permanenza in casa  ex art. 656 comma 10 | Perdita di efficacia - Sospensione provvisoria  prosecuzione permanenza in casa  ex art. 656 comma 10 | NULL | NULL | NULL | NULL |
|  | MOTIVO_PROVVEDIMENTO | 2755 | C046 | Perdita di efficacia - Sospensione provvisoria  prosecuzione collocamento in comunità  ex art.  656 comma 10 | Perdita di efficacia - Sospensione provvisoria  prosecuzione collocamento in comunità  ex art.  656 comma 10 | NULL | NULL | NULL | NULL |

Tabella 44 - Tabella <CG_REF_CODES>- Ordinanza/decreto  ripristino

Le prime 4 voci sono da utilizzare per il Tribunale di Sorveglianza/Tribunale per i Minorenni in funzione di Tribunale di Sorveglianza.
Le rimanenti 4 voci sono da utilizzare per il Magistrato di Sorveglianza/ Magistrato di Sorveglianza per i Minorenni.
L’intervento prevede l’inserimento nella tabella <CG_REF_CODES> delle seguenti posizioni giuridiche:
| N. | RV_DOMAIN | RV_LOW_VALUE | RV_HIGH_VALUE | RV_ABBREVIATION | RV_MEANING | RV_ALT2_VALUE | RV_ALT3_VALUE | RV_ALT4_VALUE | RV_ALT5_VALUE |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | POSIZIONE_GIURIDICA | 62 | NULL | NULL | Sospensione provvisoria 51 ter   Arresti Domiciliari ex art. 656 comma 10 | NULL | NULL | NULL | NULL |
|  | POSIZIONE_GIURIDICA | 63 | NULL | NULL | Sospensione provvisoria 51 ter   Domiciliari ex art 89 dpr 309/90 | NULL | NULL | NULL | NULL |
|  | POSIZIONE_GIURIDICA | 64 | NULL | NULL | Sospensione provvisoria 51 ter   Permanenza in Casa | NULL | NULL | NULL | NULL |
|  | POSIZIONE_GIURIDICA | 65 | NULL | NULL | Sospensione provvisoria 51 ter   Collocamento in Comunità | NULL | NULL | NULL | NULL |
|  | POSIZIONE_GIURIDICA | 67 | NULL | NULL | Arresti Domiciliari ex art 89 dpr 309/90 | NULL | NULL | NULL | NULL |
|  | POSIZIONE_GIURIDICA | 68 | NULL | NULL | Permanenza in casa  ex art. 656 comma 10 | NULL | NULL | NULL | NULL |
|  | POSIZIONE_GIURIDICA | 69 | NULL | NULL | Collocamento in comunità  ex art.  656 comma 10 | NULL | NULL | NULL | NULL |

Tabella 45 - Tabella <CG_REF_CODES> Posizione giuridica

L’intervento prevede l’inserimento nella tabella <CG_REF_CODES> dei seguenti stati del procedimento:
| N. | RV_DOMAIN | RV_LOW_VALUE | RV_HIGH_VALUE | RV_ABBREVIATION | RV_MEANING | RV_ALT2_VALUE | RV_ALT3_VALUE | RV_ALT4_VALUE | RV_ALT5_VALUE |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | STATO_PROCEDIMENTO | 0529 | NULL | In esecuzione | Sospensione provvisoria  prosecuzione arresti domiciliari ex art. 656 comma 10 - Emesso Ordine di Esecuzione  in data | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0530 | NULL | In esecuzione | Sospensione provvisoria  prosecuzione arresti domiciliari ex art. 656 comma 10 - Emessa Comunicazione Scadenza Pena | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0531 | NULL | In esecuzione | Sospensione provvisoria  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90 -  Emesso Ordine di Esecuzione  in data | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0532 | NULL | In esecuzione | Sospensione provvisoria  prosecuzione Arresti Domiciliari ex art 89 dpr 309/90 -  Emessa Comunicazione Scadenza Pena | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0533 | NULL | In esecuzione | Sospensione provvisoria  prosecuzione permanenza in casa  ex art. 656 comma 10 - Emesso Ordine di Esecuzione  in data | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0534 | NULL | In esecuzione | Sospensione provvisoria  prosecuzione permanenza in casa  ex art. 656 comma 10 - Emessa Comunicazione Scadenza Pena | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0535 | NULL | In esecuzione | Sospensione provvisoria  prosecuzione collocamento in comunità  ex art.  656 comma 10 - Emesso Ordine di Esecuzione  in data | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0536 | NULL | In esecuzione | Sospensione provvisoria  prosecuzione collocamento in comunità  ex art.  656 comma 10 - Emessa Comunicazione Scadenza Pena | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0537 | NULL | In esecuzione | Ripristino arresti domiciliari ex art. 656 comma 10 | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0538 | NULL | In esecuzione | Ripristino arresti domiciliari ex art 89 dpr 309/90 | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0539 | NULL | In esecuzione | Ripristino permanenza in casa  ex art. 656 comma 10 | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0540 | NULL | In esecuzione | Ripristino collocamento in comunità  ex art.  656 comma 10 | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0541 | NULL | In esecuzione | Ripristino arresti domiciliari ex art. 656 comma 10 - Emessa Comunicazione Scadenza Misura | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0542 | NULL | In esecuzione | Ripristino arresti domiciliari ex art 89 dpr 309/90- Emessa Comunicazione Scadenza Misura | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0543 | NULL | In esecuzione | Ripristino permanenza in casa  ex art. 656 comma 10 - Emessa Comunicazione Scadenza Misura | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0544 | NULL | In esecuzione | Ripristino collocamento in comunità  ex art.  656 comma 10 - Emessa Comunicazione Scadenza Misura | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0545 | NULL | In esecuzione | Revoca  Arresti domiciliari ex art. 656 comma 10 - Emesso Ordine Esecuzione | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0546 | NULL | In esecuzione | Revoca   Permanenza in casa  ex art. 656 comma 10 - Emesso Ordine Esecuzione | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0547 | NULL | In esecuzione | Revoca   Arresti Domiciliari ex art 89 dpr 309/90 - Emesso Ordine Esecuzione | NULL | NULL | NULL | NULL |
|  | STATO_PROCEDIMENTO | 0548 | NULL | In esecuzione | Revoca  Collocamento in comunità  ex art.  656 comma 10 - Emesso Ordine Esecuzione | NULL | NULL | NULL | NULL |

Tabella 46 - Tabella <CG_REF_CODES> Stato procedimento

L’intervento prevede l’inserimento nella tabella <CG_REF_CODES> dei seguenti nomi di provvedimento:
| N. | RV_DOMAIN | RV_LOW_VALUE | RV_HIGH_VALUE | RV_ABBREVIATION | RV_MEANING | RV_ALT2_VALUE | RV_ALT3_VALUE | RV_ALT4_VALUE | RV_ALT5_VALUE |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | NOME_PROVVEDIMENTO | NP301 | NULL | NULL | Sospensione provvisoria Arresti Domiciliari - Eseguita da PM | NULL | NULL | NULL | NULL |
|  | NOME_PROVVEDIMENTO | NP302 | NULL | NULL | Sospensione provvisoria Arresti Domiciliari - Eseguita da Magistrato Sorveglianza | NULL | NULL | NULL | NULL |
|  | NOME_PROVVEDIMENTO | NP303 | NULL | NULL | Ripristino Arresti Domiciliari – Decreto - Eseguito dal Magistrato di Sorveglianza | NULL | NULL | NULL | NULL |
|  | NOME_PROVVEDIMENTO | NP304 | NULL | NULL | Ripristino Arresti Domiciliari – Decreto - Eseguito dalla Procura | NULL | NULL | NULL | NULL |
|  | NOME_PROVVEDIMENTO | NP305 | NULL | NULL | Ripristino Arresti Domiciliari – Ordinanza – Eseguita da Tribunale di Sorveglianza | NULL | NULL | NULL | NULL |
|  | NOME_PROVVEDIMENTO | NP306 | NULL | NULL | Ripristino Arresti Domiciliari - Ordinanza - Eseguita dalla Procura | NULL | NULL | NULL | NULL |
|  | NOME_PROVVEDIMENTO | NP307 | NULL | NULL | Revoca Arresti Domiciliari - Diretta | NULL | NULL | NULL | NULL |
|  | NOME_PROVVEDIMENTO | NP308 | NULL | NULL | Revoca Arresti Domiciliari – A seguito sospensione | NULL | NULL | NULL | NULL |

Tabella 47 - Tabella <CG_REF_CODES> Nome provvedimento

L’intervento prevede l’inserimento nella tabella <TEMPLATE> dei seguenti modelli:
| N. | ID_TEMPLATE | NOME_TEMPLATE | DESCR | PATH_RICERCA | COD_TIPO_EVENTO | COD_TIPO_PROVVEDIMENTO | COD_MOTIVO | FLAG_TEMPLATE | COD_ESITO | COD_OGGETTO_PROCEDIMENTO | MAG_COD_MAGISTRATO | COD_TIPO_PROVVEDIMENTO_SIGE |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | SIEP_MA_558 | SIEP_MA_ARDOM_SOSP_PROC | Sospensione provvisoria_arresti_domiciliari_esegue_procura | c:\template\siep\ma\ | 01 | 02 | 2756 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_559 | SIEP_MA_ARDOM_SOSP_PROC | Sospensione provvisoria_arresti_domiciliari_esegue_procura | c:\template\siep\ma\ | 01 | 02 | 2741 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_560 | SIEP_MA_ARDOM_SOSP_PROC | Sospensione provvisoria_arresti_domiciliari_esegue_procura | c:\template\siep\ma\ | 01 | 02 | 2742 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_561 | SIEP_MA_ARDOM_SOSP_PROC | Sospensione provvisoria_arresti_domiciliari_esegue_procura | c:\template\siep\ma\ | 01 | 02 | 2743 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_562 | SIEP_MA_ ARDOM_SOSP_MDS | Sospensione provvisoria_arresti_domiciliari_esegue_sorveglianza | c:\template\siep\ma\ | 01 | 02 | 2756 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_563 | SIEP_MA_ ARDOM_SOSP_MDS | Sospensione provvisoria_arresti_domiciliari_esegue_sorveglianza | c:\template\siep\ma\ | 01 | 02 | 2741 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_564 | SIEP_MA_ ARDOM_SOSP_MDS | Sospensione provvisoria_arresti_domiciliari_esegue_sorveglianza | c:\template\siep\ma\ | 01 | 02 | 2742 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_565 | SIEP_MA_ ARDOM_SOSP_MDS | Sospensione provvisoria_arresti_domiciliari_esegue_sorveglianza | c:\template\siep\ma\ | 01 | 02 | 2743 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_566 | SIEP_MA_ ARDOM_RIPR_MDS | Ripristino_arresti_domiciliari_sorveglianza | c:\template\siep\ma\ | 1 | 2 | 2752 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_567 | SIEP_MA_ ARDOM_RIPR_MDS | Ripristino_arresti_domiciliari_sorveglianza | c:\template\siep\ma\ | 1 | 2 | 2753 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_568 | SIEP_MA_ ARDOM_RIPR_MDS | Ripristino_arresti_domiciliari_sorveglianza | c:\template\siep\ma\ | 1 | 2 | 2754 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_569 | SIEP_MA_ ARDOM_RIPR_MDS | Ripristino_arresti_domiciliari_sorveglianza | c:\template\siep\ma\ | 1 | 2 | 2755 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_570 | SIEP_MA_ ARDOM_RIPR_MDS | Ripristino_arresti_domiciliari_sorveglianza | c:\template\siep\ma\ | 1 | 3 | 2752 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_571 | SIEP_MA_ ARDOM_RIPR_MDS | Ripristino_arresti_domiciliari_sorveglianza | c:\template\siep\ma\ | 1 | 3 | 2753 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_572 | SIEP_MA_ ARDOM_RIPR_MDS | Ripristino_arresti_domiciliari_sorveglianza | c:\template\siep\ma\ | 1 | 3 | 2754 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_573 | SIEP_MA_ ARDOM_RIPR_MDS | Ripristino_arresti_domiciliari_sorveglianza | c:\template\siep\ma\ | 1 | 3 | 2755 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_574 | SIEP_MA_ ARDOM_RIPR_MDS_PROC | Ripristino_arresti_domiciliari_sorveglianza_esegue_procura | c:\template\siep\ma\ | 1 | 2 | 2752 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_575 | SIEP_MA_ ARDOM_RIPR_MDS_PROC | Ripristino_arresti_domiciliari_sorveglianza_esegue_procura | c:\template\siep\ma\ | 1 | 2 | 2753 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_576 | SIEP_MA_ ARDOM_RIPR_MDS_PROC | Ripristino_arresti_domiciliari_sorveglianza_esegue_procura | c:\template\siep\ma\ | 1 | 2 | 2754 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_577 | SIEP_MA_ ARDOM_RIPR_MDS_PROC | Ripristino_arresti_domiciliari_sorveglianza_esegue_procura | c:\template\siep\ma\ | 1 | 2 | 2755 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_578 | SIEP_MA_ ARDOM_RIPR_MDS_PROC | Ripristino_arresti_domiciliari_sorveglianza_esegue_procura | c:\template\siep\ma\ | 1 | 3 | 2752 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_579 | SIEP_MA_ ARDOM_RIPR_MDS_PROC | Ripristino_arresti_domiciliari_sorveglianza_esegue_procura | c:\template\siep\ma\ | 1 | 3 | 2753 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_580 | SIEP_MA_ ARDOM_RIPR_MDS_PROC | Ripristino_arresti_domiciliari_sorveglianza_esegue_procura | c:\template\siep\ma\ | 1 | 3 | 2754 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_581 | SIEP_MA_ ARDOM_RIPR_MDS_PROC | Ripristino_arresti_domiciliari_sorveglianza_esegue_procura | c:\template\siep\ma\ | 1 | 3 | 2755 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_582 | SIEP_MA_ ARDOM_RIPR_TDS | Ripristino_arresti_domiciliari_tribunale_sorveglianza | c:\template\siep\ma\ | 1 | 3 | 2748 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_583 | SIEP_MA_ ARDOM_RIPR_TDS | Ripristino_arresti_domiciliari_tribunale_sorveglianza | c:\template\siep\ma\ | 1 | 3 | 2749 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_584 | SIEP_MA_ ARDOM_RIPR_TDS | Ripristino_arresti_domiciliari_tribunale_sorveglianza | c:\template\siep\ma\ | 1 | 3 | 2758 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_585 | SIEP_MA_ ARDOM_RIPR_TDS | Ripristino_arresti_domiciliari_tribunale_sorveglianza | c:\template\siep\ma\ | 1 | 3 | 2759 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_586 | SIEP_MA_ ARDOM_RIPR_TDS | Ripristino_arresti_domiciliari_tribunale_sorveglianza | c:\template\siep\ma\ | 1 | 2 | 2748 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_587 | SIEP_MA_ ARDOM_RIPR_TDS | Ripristino_arresti_domiciliari_tribunale_sorveglianza | c:\template\siep\ma\ | 1 | 2 | 2749 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_588 | SIEP_MA_ ARDOM_RIPR_TDS | Ripristino_arresti_domiciliari_tribunale_sorveglianza | c:\template\siep\ma\ | 1 | 2 | 2758 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_589 | SIEP_MA_ ARDOM_RIPR_TDS | Ripristino_arresti_domiciliari_tribunale_sorveglianza | c:\template\siep\ma\ | 1 | 2 | 2759 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_590 | SIEP_MA_ ARDOM_RIPR_TDS_PROC | Ripristino_arresti_domiciliari_tribunale_sorveglianza_esegue_procura | c:\template\siep\ma\ | 1 | 3 | 2748 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_591 | SIEP_MA_ ARDOM_RIPR_TDS_PROC | Ripristino_arresti_domiciliari_tribunale_sorveglianza_esegue_procura | c:\template\siep\ma\ | 1 | 3 | 2749 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_592 | SIEP_MA_ ARDOM_RIPR_TDS_PROC | Ripristino_arresti_domiciliari_tribunale_sorveglianza_esegue_procura | c:\template\siep\ma\ | 1 | 3 | 2758 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_593 | SIEP_MA_ ARDOM_RIPR_TDS_PROC | Ripristino_arresti_domiciliari_tribunale_sorveglianza_esegue_procura | c:\template\siep\ma\ | 1 | 3 | 2759 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_594 | SIEP_MA_ ARDOM_RIPR_TDS_PROC | Ripristino_arresti_domiciliari_tribunale_sorveglianza_esegue_procura | c:\template\siep\ma\ | 1 | 2 | 2748 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_595 | SIEP_MA_ ARDOM_RIPR_TDS_PROC | Ripristino_arresti_domiciliari_tribunale_sorveglianza_esegue_procura | c:\template\siep\ma\ | 1 | 2 | 2749 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_596 | SIEP_MA_ ARDOM_RIPR_TDS_PROC | Ripristino_arresti_domiciliari_tribunale_sorveglianza_esegue_procura | c:\template\siep\ma\ | 1 | 2 | 2758 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_597 | SIEP_MA_ ARDOM_RIPR_TDS_PROC | Ripristino_arresti_domiciliari_tribunale_sorveglianza_esegue_procura | c:\template\siep\ma\ | 1 | 2 | 2759 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_550 | SIEP_MA_ARDOM_REVO_DIRETTA | Revoca_arresti_domiciliari_diretta | c:\template\siep\ma\ | 01 | 03 | 2744 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_551 | SIEP_MA_ARDOM_REVO_DIRETTA | Revoca_arresti_domiciliari_diretta | c:\template\siep\ma\ | 01 | 03 | 2757 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_552 | SIEP_MA_ARDOM_REVO_DIRETTA | Revoca_arresti_domiciliari_diretta | c:\template\siep\ma\ | 01 | 03 | 2746 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_553 | SIEP_MA_ARDOM_REVO_DIRETTA | Revoca_arresti_domiciliari_diretta | c:\template\siep\ma\ | 01 | 03 | 2747 | 0 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_554 | SIEP_MA_ARDOM_REVO_SOSPENSIONE | Revoca_arresti_domiciliari_dopo_sospensione | c:\template\siep\ma\ | 01 | 03 | 2744 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_555 | SIEP_MA_ARDOM_REVO_SOSPENSIONE | Revoca_arresti_domiciliari_dopo_sospensione | c:\template\siep\ma\ | 01 | 03 | 2757 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_556 | SIEP_MA_ARDOM_REVO_SOSPENSIONE | Revoca_arresti_domiciliari_dopo_sospensione | c:\template\siep\ma\ | 01 | 03 | 2746 | 1 | NULL | NULL | NULL | NULL |
|  | SIEP_MA_557 | SIEP_MA_ARDOM_REVO_SOSPENSIONE | Revoca_arresti_domiciliari_dopo_sospensione | c:\template\siep\ma\ | 01 | 03 | 2747 | 1 | NULL | NULL | NULL | NULL |

Tabella 48 - Tabella <TEMPLATE> Nuovi modelli

Gli attuali template utilizzati per le misure alternative hanno tutti <COD_TIPO_EVENTO> = ‘01’.
L’intervento prevede la aggiornamento nella tabella <CG_REF_CODES> del seguente record:
| N. | RV_DOMAIN | RV_LOW_VALUE | RV_HIGH_VALUE | RV_ABBREVIATION | RV_MEANING | RV_ALT2_VALUE | RV_ALT3_VALUE | RV_ALT4_VALUE | RV_ALT5_VALUE |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | TIPO_UFFICIO | UDSM | T | NULL | Magistrato di Sorveglianza per i Minorenni | NULL | NULL | NULL | NULL |

Tabella 49 - Tabella <CG_REF_CODES> TIPO_UFFICIO

## Modifica template
L’intervento prevede i seguenti nuovi template (allegati al presente documento):
SIEP_MA_ARDOM_SOSP_PROC
SIEP_MA_ ARDOM_SOSP_MDS
SIEP_MA_ ARDOM_RIPR_MDS
SIEP_MA_ ARDOM_RIPR_MDS_PROC
SIEP_MA_ ARDOM_RIPR_ TDS
SIEP_MA_ ARDOM_RIPR_TDS_PROC
SIEP_MA_ARDOM_REVO_DIRETTA
SIEP_MA_ARDOM_REVO_SOSPENSIONE.
# Gestione Provvedimenti emessi dalla Magistratura di Sorveglianza
## Intervento richiesto dall’Amministrazione
Le regole sulla visibilità dei soggetti minorenni è la stessa adottata per gli uffici di procura.
Per la gestione dei provvedimenti della Magistratura di Sorveglianza occorre:
integrare tutte le Schede previste per la gestione dei provvedimenti della magistratura di sorveglianza
verificare i flussi dello scambio dati in elettronico.


Figura 54 - Dettaglio maschera decisione della sorveglianza
Tutta la procedura di scambio dati va realizzata ed integrata in contemporanea con le modifiche apportate al sistema SIUS Minorenni.
Valori di Tabella da inserire:
Tribunale per i  Minorenni in Funzione di Tribunale di Sorveglianza
Magistrato Di Sorveglianza per i Minorenni
Ussm  (Ufficio Servizio Sociale Per Minorenni)
Istituti Di Detenzione minorili.
Tutte le schede vanno aggiornate inserendo una tabella che comprenda le autorità minorili.
## Situazione attuale
Attualmente il sistema non permette in modo completo la gestione delle decisione emesse dalla magistratura di sorveglianza per i minorenni.
## Descrizione dell’intervento
L’intervento prevede l’adeguamento di tutte le maschere delle decisioni della magistratura di sorveglianza con le caratteristiche peculiari dell’ambito minorile.
L’operatore all’interno del procedimento seleziona dal menu laterale di sinistra la voce “Decisione Sorveglianza) (Figura 55).


Figura 55 -  Selezione Decisioni Sorveglianza


Il sistema mostra l’interfaccia con le decisioni della sorveglianza (Figura 56).

Figura 56 - Decisioni Sorveglianza

Le modifiche sono previste per i procedimenti iscritti dalla Procura presso il Tribunale per i minorenni (cod_tipo_ufficio = “PMM”) e dalla Procura generale (cod_tipo_ufficio = “PGCAP”) presso la Corte di Appello sezione per i minorenni (cod_tipo_ufficio = “CAPSM”) e devono tener conto del fatto che uffici che svolgono funzioni giurisdizionali simili hanno diverso nome in relazione all’ambito di appartenenza.
Ad esempio, il Tribunale di Sorveglianza per l’ambito degli uffici giudiziari dei minorenni assume il nome “Tribunale per i  Minorenni in Funzione di Tribunale di Sorveglianza”.
Inoltre, sullo stesso procedimento posso essere presenti uffici di entrambi gli ambiti (maggiorenni/minorenni).
Pertanto, è stato richiesto che nella stessa maschera sia possibile avere, in alcuni casi, al posto di una sola etichetta un elenco contenente 2 diverse etichette.


Modifica – Ufficio emittente/Autorità emittente

Attualmente, l’ufficio emittente, talvolta, è prevalorizzato e non modificabile dall’operatore:


Figura 57 – Attuale ufficio emittente prevalorizzato
In qualche caso, l’etichetta è “Autorità Emittente”.

Figura 58 - Autorità Emittente
In altri casi, è prevalorizzato, ma il sistema permette la selezione da un elenco dell’ufficio emittente:


Figura 59 – Attuale ufficio emittente modificabile
Anche in questo caso, l’etichetta può essere “Autorità Emittente”.

Figura 60 - Autorità Emittente
L’intervento prevede nel primo caso della immagine (Figura 57 – Attuale ufficio emittente prevalorizzato) e nel secondo caso della immagine (Figura 59 – Attuale ufficio emittente modificabile) l’inserimento di una casella di selezione (combobox) (Figura 61) contenente il seguente elenco:
Tribunale di Sorveglianza
Magistrato di Sorveglianza
Tribunale per i  Minorenni in Funzione di Tribunale di Sorveglianza
Magistrato di sorveglianza per i Minorenni.
La relativa funzione di ricerca della sede deve tener conto della selezione effettuata dall’operatore.
Nel caso:
il sistema mostra l’elenco dei Tribunali di Sorveglianza (cod_tipo_ufficio=”TDS”),
il sistema mostra l’elenco dei Magistrati di Sorveglianza (cod_tipo_ufficio=”UDS”),
il sistema mostra l’elenco dei Tribunali per i  Minorenni in Funzione di Tribunale di Sorveglianza (cod_tipo_ufficio=”TDSM”),
il sistema mostra l’elenco dei Magistrati di sorveglianza per i Minorenni (cod_tipo_ufficio=”UDSM”).


I 4 casi descritti nelle immagini (Figura 57, Figura 58, Figura 59 e Figura 60) dopo l’intervento sono ridotti a soli 2 (Figura 61 e Figura 62).

Figura 61 – Ufficio emittente modificabile


Figura 62 – Autorità emittente modificabile
L’intervento in parola riguarda tutti i procedimenti.

Modifica – UEPE

L’etichetta “UEPE” deve essere modificata in una casella di selezione contenente i seguenti 2 valori:
UEPE (valore di default)
USSM.
La relativa funzione di ricerca deve tener conto della selezione effettuata dall’operatore.
Nel caso:
il sistema mostra l’elenco degli UEPE (tipo=”UEPE” oppure ”UEPESS”),
il sistema mostra l’elenco degli USSM  (tipo=”USSM” oppure ”USSMSS”) prelevando dalla tabella <CSSA>.


Figura 63 - Attuale UEPE


Figura 64 - USSM per i minorenni
Quando l’etichetta “UEPE” è seguita dall’indicazione dell’ufficio in sola lettura presente in archivio (Figura 65), l’etichetta deve essere visualizzata a seconda del  codice tipo ufficio (vedi maschera “Variazione Data Inizio Misura”).

Figura 65 – attuale etichetta UEPE

Figura 66 - Ricerca UEPE

Modifica – Magistrato di sorveglianza / Ufficio di sorveglianza

L’etichetta “Ufficio di Sorveglianza” deve essere modificata in una casella di selezione contenente i seguenti 2 valori:
Ufficio di Sorveglianza (valore di default)
Magistrato di Sorveglianza per i Minorenni.
La relativa funzione di ricerca deve tener conto della selezione effettuata dall’operatore.
Nel caso:
il sistema mostra l’elenco degli uffici di sorveglianza (cod_tipo_ufficio=”UDS”),
il sistema mostra l’elenco dei magistrati di sorveglianza per i minorenni (cod_tipo_ufficio=”UDSM”).
Nella finestra (Figura 70) nel primo caso l’etichetta è “Lista Uffici Di Sorveglianza”, nel secondo caso “Lista Magistrati Di Sorveglianza per i Minorenni”.


Figura 67 - Attuale Ufficio di Sorveglianza
In alcuni casi l’etichetta è “Magistrato di Sorveglianza”.
In questi casi, l’etichetta “Magistrato di Sorveglianza” deve essere modificata in una casella di selezione contenente i seguenti 2 valori:
Magistrato di Sorveglianza (valore di default)
Magistrato di Sorveglianza per i Minorenni.
La relativa funzione di ricerca deve tener conto della selezione effettuata dall’operatore.
Nel caso:
il sistema mostra l’elenco degli uffici di sorveglianza (cod_tipo_ufficio=”UDS”),
il sistema mostra l’elenco dei magistrati di sorveglianza per i minorenni (cod_tipo_ufficio=”UDSM”).
Nella finestra (Figura 70) nel primo caso l’etichetta è “Lista Uffici Di Sorveglianza”, nel secondo caso “Lista Magistrati Di Sorveglianza per i Minorenni”.


Figura 68 - Attuale Ufficio di Sorveglianza


Figura 69 - Magistrato di Sorveglianza per i minorenni


Figura 70 -  Funzione selezione ufficio di sorveglianza

Modifica – Tribunale di sorveglianza

L’etichetta “Tribunale di Sorveglianza” deve essere modificata in una casella di selezione contenente i seguenti 2 valori:
Tribunale di Sorveglianza (valore di default)
Tribunale per i  Minorenni in funzione di Tribunale di Sorveglianza.
La relativa funzione di ricerca deve tener conto della selezione effettuata dall’operatore.
Nel caso:
il sistema mostra l’elenco dei Tribunali di sorveglianza (cod_tipo_ufficio=”TDS”),
il sistema mostra l’elenco Tribunale per i  Minorenni in funzione di Tribunale di Sorveglianza (cod_tipo_ufficio=”TDSM”).
Nella finestra (Figura 73) nel primo caso l’etichetta è “Elenco Tribunali Di Sorveglianza”, nel secondo caso “Elenco Tribunali per i Minorenni in funzione di Tribunale Di Sorveglianza”.



Figura 71 - Attuale Tribunale di sorveglianza


Figura 72 -  Tribunale per i  Minorenni in funzione di Tribunale di Sorveglianza


Figura 73 -  Funzione selezione Tribunale di sorveglianza

Autorità competente per territorio

Negli elenchi delle autorità di destinazione devono essere presenti anche la tipologia dell’Ufficio Servizi Sociali Minorenni (cod_tipo_ufficio = “USSM”) e la voce “SNT”.


Figura 74 - Autorità competente per territorio
Autorità Destinazione

Negli elenchi delle autorità di destinazione devono essere presenti anche la tipologia dell’Ufficio Servizi Sociali Minorenni (cod_tipo_ufficio = “USSM”) e la voce “SNT”.


Figura 75 - Autorità destinazione

Negli elenchi del destinatario per l’esecuzione devono essere presenti anche la tipologia dell’Ufficio Servizi Sociali Minorenni (cod_tipo_ufficio = “USSM”) e la voce “SNT”.

Destinatario per esecuzione


Figura 76 - Destinatario per esecuzione


Figura 77 - Destinatario per esecuzione

Autorità per esecuzione

Negli elenchi della Autorità per la restituzione devono essere presenti anche la tipologia dell’Ufficio Servizi Sociali Minorenni (cod_tipo_ufficio = “USSM”) e la voce “SNT”.


Figura 78 - Autorità per la Restituzione

La selezione per magistrato deve tener correttamente conto dell’ufficio di appartenenza.
Pertanto, l’operatore della Procura presso il Tribunale per i minorenni può selezionare un magistrato associato all’ufficio della Procura presso il Tribunale per i minorenni.


Figura 79 -  Magistrato firmatario

Il risultato del censimento delle maschere è contenuto nella successiva Tabella 50- Maschere decisione sorveglianza.
Per ciascuna maschera è stata indicata con una lettera dalla “A” alla “I” la modifica da apportare.
Le maschere di inserimento delle decisione della sorveglianza da modificare sono:

| N. |  |  |  | A | B | C | D | E | F | G | I |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | Misure alternative |  |  |  |  |  |  |  |  |  |  |
|  |  | Affidamento in Prova al Servizio Sociale |  |  |  |  |  |  |  |  |  |
|  |  |  | Concessione | A | B | C | D | E |  |  |  |
|  |  |  | Sospensione Provvisoria 51 Ter | A |  | C | D |  | F |  |  |
|  |  |  | Cessazione Sospensione Provvisoria |  | B | C | D | E |  |  |  |
|  |  |  | Ripristino | A | B | C | D | E |  |  |  |
|  |  |  | Revoca | A |  |  |  |  |  |  |  |
|  |  |  | Sospensione Provvisoria 51 Bis | A |  | C | D |  | F |  |  |
|  |  |  | Estensione Definitiva (senza cumulo) | A | B | C | D | E |  |  |  |
|  |  |  | Estensione Definitiva (con cumulo) | A | B | C | D | E |  |  |  |
|  |  | Funzione in fase di implementazione | Dichiarazione di Inefficacia |  |  |  |  |  |  |  |  |
|  |  |  | Ammissione Provvisoria | A | B | C | D | E |  |  | I |
|  |  |  | Cessazione | A |  |  |  |  |  |  |  |
|  |  |  | Prosecuzione Della Misura In Corso | A |  |  |  |  |  |  |  |
|  |  |  | Cessazione 51bis | A |  |  |  |  |  |  |  |
|  |  | Detenzione Domiciliare |  |  |  |  |  |  |  |  |  |
|  |  |  | Concessione | A |  |  |  |  | F | G |  |
|  |  |  | Sospensione Provvisoria 51 Ter | A |  | C | D |  | F |  |  |
|  |  |  | Cessazione Sospensione Provvisoria |  | B | C | D | E |  |  |  |
|  |  |  | Ripristino | A | B | C | D | E |  |  |  |
|  |  |  | Revoca | A |  |  | D | E | F |  |  |
|  |  |  | Sospensione Provvisoria 51 Bis | A |  | C | D |  | F |  |  |
|  |  |  | Estensione Definitiva (senza cumulo) | A | B | C | D | E |  |  |  |
|  |  |  | Estensione Definitiva (con cumulo) | A | B | C | D | E |  |  |  |
|  |  |  | Ammissione Provvisoria  a Detenzione domiciliare | A | B | C | D | E | F |  |  |
|  |  | Funzione in fase di implementazione | Sospensione provvisoria arresti domiciliari |  |  |  |  |  |  |  |  |
|  |  |  | Cessazione | A |  |  | D | E |  | F |  |
|  |  |  | Prosecuzione Della Misura In Corso | A |  |  |  |  |  |  |  |
|  |  |  | Cessazione 51bis | A |  |  |  |  |  |  |  |
|  |  | Semilibertà |  |  |  |  |  |  |  |  |  |
|  |  |  | Concessione | A |  |  |  |  | F | G |  |
|  |  |  | Sospensione Provvisoria 51 Ter | A |  | C | D |  | F |  |  |
|  |  |  | Cessazione Sospensione Provvisoria |  | B | C | D | E |  |  |  |
|  |  |  | Ripristino | A | B | C | D | E |  |  |  |
|  |  |  | Revoca | A |  |  | D | E | F |  |  |
|  |  |  | Sospensione Provvisoria 51 Bis | A |  | C | D |  | F |  |  |
|  |  |  | Estensione Definitiva (senza cumulo) | A | B | C | D | E |  |  |  |
|  |  |  | Estensione Definitiva (con cumulo) | A | B | C | D | E |  |  |  |
|  |  |  | Cessazione | A |  |  | D | E | F |  |  |
|  |  |  | Prosecuzione Della Misura In Corso | A |  |  |  |  |  |  |  |
|  |  |  | Cessazione 51bis | A |  |  |  |  |  |  |  |
|  |  | Detenzione Domiciliare Speciale | Funzione in fase di implementazione |  |  |  |  |  |  |  |  |
|  |  | L. 207/2003 |  |  |  |  |  |  |  |  |  |
|  |  |  | Concessione | A |  |  |  |  | F | G |  |
|  |  |  | Sospensione Provvisoria 51 Ter | A |  | C | D |  | F |  |  |
|  |  |  | Sospensione Provvisoria 51 Bis | A |  | C | D |  | F |  |  |
|  |  |  | Cessazione Sospensione Provvisoria |  | B | C | D | E |  |  |  |
|  |  |  | Ripristino | A | B | C | D | E |  |  |  |
|  |  |  | Revoca | A |  |  |  |  |  |  |  |
|  |  |  | Cessazione | A |  |  |  |  |  |  |  |
|  |  |  | Cessazione 51bis | A |  |  |  |  |  |  |  |
|  |  | Liberazione Condizionale | Funzione in fase di implementazione |  |  |  |  |  |  |  |  |
|  |  | Registrazione Data Inizio Misura | Non prevista |  |  |  |  |  |  |  |  |
|  |  | Rigetto Misure Alternative |  | A |  |  |  |  | F | G |  |
|  |  | Detenzione Domiciliare a termine |  |  |  |  |  |  |  |  |  |
|  |  |  | Concessione | A |  |  |  |  | F | G |  |
|  |  |  | Proroga | A |  |  |  |  | F | G |  |
|  |  |  | Proroga Provvisoria | A | B | C | D | E |  |  |  |
|  |  |  | Cessazione Sospensione Provvisoria |  | B | C | D | E |  |  |  |
|  |  |  | Revoca | A |  |  | D | E | F |  |  |
|  |  |  | Sospensione Provvisoria 51 ter | A |  | C | D |  | F |  |  |
|  |  | Non prevista | Ripristino Detenzione in Carcere |  |  |  |  |  |  |  |  |
|  |  |  | Ordine Esecuzione |  |  |  |  |  | F |  |  |
|  |  |  | Cessazione | A |  |  | D | E | F |  |  |
|  |  |  | Prosecuzione Della Misura In Corso | A |  |  |  |  |  |  |  |
|  |  |  | Cessazione 51bis | A |  |  |  |  |  |  |  |
|  |  | Variazione Data Inizio Misura |  |  | B | C | D |  | F |  |  |
|  |  | Esecuzione Pena Presso Domicilio |  |  |  |  |  |  |  |  |  |
|  |  |  | Concessione | A |  |  |  |  | F | G |  |
|  |  |  | Sospensione Provvisoria 51 Ter | A |  | C | D |  | F |  |  |
|  |  |  | Sospensione Provvisoria 51 Bis | A |  | C | D |  | F |  |  |
|  |  |  | Cessazione Sospensione Provvisoria | A | B | C | D | E |  |  |  |
|  |  |  | Ripristino | A | B | C | D | E |  |  |  |
|  |  |  | Revoca | A |  |  |  |  |  |  |  |
|  |  |  | Cessazione | A |  |  |  |  |  |  |  |
|  |  |  | Prosecuzione Della Misura In Corso | A |  |  |  |  |  |  |  |
|  |  |  | Cessazione 51bis | A |  |  |  |  |  |  |  |
|  |  | Arresti domiciliari ex 656 comma 10° |  |  |  |  |  |  |  |  |  |
|  |  | Nuovo | Sospensione provvisoria Arresti Domiciliari | A |  | C | D | E | F |  |  |
|  |  | Nuovo | Revoca Arresti Domiciliari  e Rigetta applicazione misura alternativa | A |  | C | D | E |  |  |  |
|  |  | Nuovo | Ripristino Degli Arresti Domiciliari | A | B | C | D | E |  |  |  |
|  | Sospensioni |  |  |  |  |  |  |  |  |  |  |
|  |  | Sospensione Esecuzione Pena |  | A |  |  |  |  |  |  |  |
|  |  | Differimento |  |  |  |  |  |  |  |  |  |
|  |  |  | Differimento Provvisorio | A |  |  |  |  |  |  |  |
|  |  |  | Differimento Definitivo | A |  |  |  |  |  |  |  |
|  |  |  | Rigetto Differimento | A |  |  |  |  |  |  |  |
|  |  |  | Revoca Differimento | A |  |  |  |  |  |  |  |
|  |  | Espulsione |  |  |  |  |  |  |  |  |  |
|  |  |  | Concessione | A | B |  |  |  | F |  |  |
|  |  |  | Rinuncia Opposizione |  | B |  |  |  | F |  |  |
|  |  |  | Accoglimento Opposizione | A | B |  |  |  | F |  |  |
|  |  |  | Rigetto Opposizione | A | B |  |  |  | F |  |  |
|  |  | Non prevista | Avvenuta Espulsione |  |  |  |  |  |  |  |  |
|  |  |  | Richiesta Esito Espulsione |  |  |  |  |  | F |  |  |
|  | Liberazione anticipata |  |  |  |  |  |  |  |  |  |  |
|  |  | Liberazione anticipata |  | A |  |  |  |  |  |  |  |
|  |  | Scomputo Permesso |  | A |  |  |  |  |  |  |  |
|  | Altre Decisioni |  |  |  |  |  |  |  |  |  |  |
|  |  | Altre Ordinanze/Decreti |  | A |  |  |  |  |  |  |  |

Tabella 50- Maschere decisione sorveglianza

Inoltre, sono da modificare le etichette delle maschere di dettaglio richiamate dopo la conferma delle informazioni inserite nelle maschere di inserimento.
La funzionalità “Decisione Sorveglianza” è volta a produrre un provvedimento con relativo documento.
Il documento prodotto deve essere infine validato dall’operatore.
Dopi l’inserimento delle informazioni, ad esempio, della revoca della detenzione domiciliare, il sistema mostra la seguente interfaccia (Figura 80 - Dettaglio).

Figura 80 - Dettaglio
L’operatore all’interno dell’interfaccia può generare la creazione del documento.
Il sistema non prevede la modifica delle informazioni già inserite ma solo la cancellazione delle informazioni già inserite.
Pertanto, l’intervento in parola non prevede la gestione della modifica delle informazioni inserite e quindi le modifiche da apportare alle interfaccia nel presente intervento riguardano solo la fase di inserimento delle informazioni.
Inoltra, l’implementazione dell’intervento deve essere coordinato con quella dell’intervento 17.Decisione sorveglianza – Arresti domiciliari ex 656 comma 10°.
## Riferimenti
Confronta “documento analisi 16_07_14.doc”.
Confronta “Elenco uffici minorili.xls”.
## Sottosistema
La modifica interessa solo il sottosistema Siep.
## Uffici
L’intervento in parola riguarda tutti gli uffici.
## Modifica interfacce utente
Le interfacce devono essere realizzate componendo le sezioni con i criteri descritti nel paragrafo precedente (18.3-Descrizione dell’intervento).
## Modifica funzionalità
Nessuna modifica prevista
## Modifica interfacce software/algoritmi
Il sistema nella valorizzazione dei campi deve seguire le seguenti regole:
| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Ufficio Emittente |  |  | Valorizzato tramite elenco contenente i valori:
Tribunale di Sorveglianza
Ufficio di Sorveglianza
Tribunale per i  Minorenni in Funzione di Tribunale di Sorveglianza
Magistrato di sorveglianza per i Minorenni. |
|  | Sede Ufficio Emittente | * |  | Valorizzabile tramite funzione di ricerca ufficio emittente.
Se l’operatore seleziona come “Ufficio Emittente” = “Tribunale di Sorveglianza”, il sistema mostra l’elenco dei Tribunali di Sorveglianza (cod_tipo_ufficio=”TDS”).
Se l’operatore seleziona come “Ufficio Emittente” = “Magistrato di Sorveglianza”, il sistema mostra l’elenco dei Magistrati di Sorveglianza (cod_tipo_ufficio=”UDS”).
Se l’operatore seleziona come “Ufficio Emittente” = “Tribunale per i  Minorenni in Funzione di Tribunale di Sorveglianza” il sistema mostra l’elenco dei Tribunali per i  Minorenni in Funzione di Tribunale di Sorveglianza (cod_tipo_ufficio=”TDSM”).
Se l’operatore seleziona come “Ufficio Emittente” = “Magistrato di sorveglianza per i Minorenni”, il sistema mostra l’elenco dei Magistrati di sorveglianza per i Minorenni (cod_tipo_ufficio=”UDSM”). |

Tabella 51 - Ufficio Emittente

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Combobox: UEPE / USSM |  |  | Elenco contenente i valori:
UEPE (valore di default)
USSM. |
|  | Ufficio UEPE / USSM | * |  | Valorizzabile tramite funzione di ricerca dell’ufficio in relazione alla selezione effettuata dall’operatore.
Se l’operatore nell’elenco seleziona “UEPE” il sistema mostra l’elenco degli UEPE (tipo=”UEPE” oppure ”UEPESS”) presenti nella tabella <CSSA>.
Se l’operatore nell’elenco seleziona “USSM” il sistema mostra l’elenco degli USSM (tipo=”USSM” oppure ”USSMSS”) presenti nella tabella <CSSA>. |

Tabella 52 – UEPE / USSM

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Combobox |  |  | Elenco contenente i valori:
Ufficio di Sorveglianza
Magistrato di Sorveglianza per i Minorenni. |
|  | Ufficio di Sorveglianza / Magistrato di Sorveglianza per i Minorenni | * |  | Valorizzabile tramite funzione di ricerca dell’ufficio in relazione alla selezione effettuata dall’operatore.
Se l’operatore nell’elenco seleziona “Ufficio di Sorveglianza”, il sistema mostra l’elenco degli uffici di sorveglianza (cod_tipo_ufficio=”UDS”).
Se l’operatore nell’elenco seleziona “Magistrato di Sorveglianza per i Minorenni”, il il sistema mostra l’elenco dei magistrati di sorveglianza per i minorenni (cod_tipo_ufficio=”UDSM”). |

Tabella 53 – Ufficio di Sorveglianza / Magistrato di Sorveglianza per i Minorenni

| N. | Campo | O | D | Nota |
| --- | --- | --- | --- | --- |
|  | Combobox |  |  | Elenco contenente i valori:
“Tribunale di Sorveglianza”
“Tribunale per i  Minorenni in funzione di Tribunale di Sorveglianza”. |
|  | Tribunale di Sorveglianza / Tribunale per i  Minorenni in funzione di Tribunale di Sorveglianza | * |  | Valorizzabile tramite funzione di ricerca dell’ufficio in relazione alla selezione effettuata dall’operatore.
Se l’operatore nell’elenco seleziona “Tribunale di Sorveglianza”, il sistema mostra l’elenco dei Tribunali di sorveglianza (cod_tipo_ufficio=”TDS”).
Se l’operatore nell’elenco seleziona “Tribunale per i  Minorenni in funzione di Tribunale di Sorveglianza”, il  sistema mostra l’elenco dei Tribunale per i  Minorenni in funzione di Tribunale di Sorveglianza (cod_tipo_ufficio=”TDSM”). |

Tabella 54 – Tribunale di Sorveglianza / Tribunale per i  Minorenni in funzione di Tribunale di Sorveglianza
Il sistema per i procedimenti iscritti dagli uffici giudiziari per i minorenni deve permettere la selezione dei soli uffici per i minorenni.
L’intervento prevede l’aggiornamento dove necessario delle informazioni riguardanti:
gli istitutivi penali minorili
le Procure presso il Tribunale per i minorenni
i Tribunali per i minorenni
gli Uffici Servizi Sociali Minorenni.
Pertanto , le funzioni di seleziona dagli elenchi devono tener conto correttamente del filtro per gli uffici per i minorenni.
Attualmente le informazioni degli istituti penali minorili sono contenute nella tabella <ISTITUTI_DETENZIONE>.
Nella tabella <ISTITUTI_DETENZIONE> per i minorenni il campo <COD_TIPO_ISTITUTO> può assumere i seguenti valori:

| N. | <COD_TIPO_ISTITUTO> | Descrizione | Note |
| --- | --- | --- | --- |
|  | 48 | Istituto Penale per Minorenni |  |
|  | 50 | Istituto per Minor.Sez. Femm |  |
|  | 51 | Istituto per Minor.Sez.Cust.Caut. Femm. |  |



Pertanto, selezionando dalla tabella <ISTITUTI_DETENZIONE>  per campo <COD_TIPO_ISTITUTO> uguali a “48” oppure “50” oppure “51” si ottengono i seguenti risultati.
| N. | ID_
ISTITUTO__
DETENZIONE | COMUNE | PR | INDIRIZZO | DESCRIZIONE |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  | Istituto Penale per Minorenni (cod_tipo_istituto = 48) | Istituto Penale per Minorenni (cod_tipo_istituto = 48) |
|  | ZZ01 | ACIREALE | CT | VIA GUIDO GOZZANO N.6 | ACIREALE |
|  | YY04 | AIROLA | BN | CORSO MONTELLA N.16 | AIROLA |
|  | WW01 | BARI | BA | VIA GIULIO PETRONI N.90 | BARI - NICOLA FORNELLI |
|  | RR02 | BOLOGNA | BO | VIA DEL PRATELLO N.34 | BOLOGNA |
|  | ZZ02 | CALTANISSETTA | CL | VIAF. TURATI  16 | CALTANISSETTA |
|  | PP04 | CASTIGLIONE DELLE STIVIERE | MN | NULL | CASTIGLIONE DELLE STIVIERE |
|  | ZZ04 | CATANIA | CT | TANGENZIALE OVEST KM 8 | CATANIA |
|  | WW03 | CATANZARO | CZ | VIA PAGLIA  43 | CATANZARO |
|  | RR03 | FIRENZE | FI | VIA ORTI ORICELLARI N.18 | FIRENZE - GIAN PAOLO MEUCCI |
|  | PP06 | GENOVA | GE | NULL | GENOVA - PONTEDECIMO |
|  | TT02 | L'AQUILA | AQ | VIA ACQUASANTA N.1 | L'AQUILA - L. FERRARI |
|  | WW02 | LECCE | LE | VIA MONTERONI  43 | LECCE |
|  | PP03 | MILANO | MI | VIA CALCHI TAEGGI N.20 | MILANO - CESARE BECCARIA |
|  | YY02 | NAPOLI | NA | SALITA LA FARINA | NAPOLI - NISIDA |
|  | ZZ03 | PALERMO | PA | VIA PRINCIPE DI PALAGONIA N.135 | PALERMO |
|  | YY12 | POTENZA | PZ | VIA APPIA N.176/B | POTENZA |
|  | TT05 | QUARTUCCIU | CA | LOCALITA' PEZZUMANNU | QUARTUCCIU |
|  | WW04 | REGGIO DI CALABRIA | RC | NULL | REGGIO DI CALABRIA |
|  | TT01 | ROMA | RM | VIA BARELLAI N.140 | ROMA - CASAL DEL MARMO |
|  | YY03 | SANTA MARIA CAPUA VETERE | CE | PIAZZA ANDREA ANGIULLI N.1 | SANTA MARIA CAPUA VETERE |
|  | PP02 | TORINO | TO | CORSO UNIONE SOVIETICA N.327 | TORINO |
|  | SS01 | TREVISO | TV | VIA SANTA BONA NUOVA N.5/C | TREVISO |
|  |  |  |  | Istituto per Minor.Sez. Femm (cod_tipo_istituto = 50) | Istituto per Minor.Sez. Femm (cod_tipo_istituto = 50) |
|  | TT08 | ROMA | RM | VIA G. BARELLAIN.140 | ROMA - CASAL DEL MARMO |
|  |  |  |  | Istituto per Minor.Sez.Cust.Caut. Femm. (cod_tipo_istituto = 51) | Istituto per Minor.Sez.Cust.Caut. Femm. (cod_tipo_istituto = 51) |
|  | YY11 | NAPOLI | NA | NULL | NAPOLI - NISIDA |

Tabella 55- Elenco Istituti detentivi minorili


L’elenco aggiornato consegnato dalla Amministrazione contiene i seguenti istituti:
| N. | ID_
ISTITUTO__
DETENZIONE | COMUNE | PR | INDIRIZZO |  |
| --- | --- | --- | --- | --- | --- |
|  | ZZ01 | ACIREALE |  | VIA G. GOZZANO, 8 |  |
|  | YY04 | AIROLA |  | CORSO MONTELLA, 16 |  |
|  | WW01 | BARI |  | VIA GIULIO PETRONI, 90 |  |
|  | RR02 | BOLOGNA |  | VIA DEI MARCHI, 5/2 |  |
|  | TT05 | CAGLIARI |  | LOC. SUPEZZU MANNU |  |
|  | ZZ02 | CALTANISSETTA |  | Via Filippo Turati, 46 |  |
|  | ZZ04 | CATANIA |  | LOC. BICOCCA |  |
|  | WW03 | CATANZARO |  | VIA PAGLIA, 43 |  |
|  | RR03 | FIRENZE |  | VIA DEGLI ORTI ORICELLARI, 18 |  |
|  | TT02 | L'AQUILA |  | VIA ACQUASANTA, 1 |  |
|  | WW02 | LECCE |  | VIA MONTERONI, 43 |  |
|  | PP03 | MILANO |  | VIA CALCHI E TAEGGI, 20 |  |
|  | YY02 | NISIDA-NA |  | VIA NISIDA,59 |  |
|  | ZZ03 | PALERMO |  | VIA FRANCESCO CILEA,28 |  |
|  |  | PONTREMOLI - MS |  | Via IV Novembre, 15 | Deve essere aggiunto in tabella
Con < ID_ISTITUTO__DETENZIONE> = “RR04”
E < COD_TIPO_ISTITUTO> = “48”. |
|  | YY12 | POTENZA |  | VIA APPIA, 175/BIS |  |
|  | TT01 | ROMA |  | VIA G. BARELLAI, 140 |  |
|  | PP02 | TORINO |  | Via Berruti e Ferreri, 3 |  |
|  | SS01 | TREVISO |  | VIA S. BONA NUOVA, 5/C |  |

Tabella 56 - Nuovo elenco Istituti detentivi minorili
Le informazioni evidenziate in verde devono essere aggiornate nella tabella <ISTITUTO_DETENZIONE>.
Attualmente le informazioni delle Procure presso il Tribunale per i minorenni sono contenute nella tabella <UFFICI> con campo <COD_TIPO_UFFICIO > = “PMM”:
| N. | COD_UFFICIO | DESCRIZIONE | INDIRIZZO | CAP | TELEFONO | E_MAIL |
| --- | --- | --- | --- | --- | --- | --- |
|  | 04200201208 | ANCONA | C.SO MAZZINI, 32 | 60121 | 071 - 200173 (CENTRALINO) | PROCMIN.ANCONA@GIUSTIZIA.IT |
|  | 07200601202 | BARI | VIA TOMMASO FIORE, 49/D | 70123 | 080-5741717 /  5741716 | PROCMIN.BARI@GIUSTIZIA.IT |
|  | 03700601209 | BOLOGNA | VIA DEL PRATELLO, 36 | 40122 | 051 - 2964811 | PROCMIN.BOLOGNA@GIUSTIZIA.IT |
|  | 02100801205 | BOLZANO | CORSO LIBERTA', 25 | 39100 | 0471 - 226433 / 226432 | PROCMIN.BOLZANO@GIUSTIZIA.IT |
|  | 01702901203 | BRESCIA | VIA MALTA, 12 | 25125 | 030 - 2421832 | PROCMIN.BRESCIA@GIUSTIZIA.IT |
|  | 09200901202 | CAGLIARI | VIA DANTE, 6 | 09127 | 070-34921 (CENTRALINO) | PROCMIN.CAGLIARI@GIUSTIZIA.IT |
|  | 08500401203 | CALTANISSETTA | VIA DON MINZONI | 93100 | 0934-597340 / 597337 | PROCMIN.CALTANISSETTA@GIUSTIZIA.IT |
|  | 07000601200 | CAMPOBASSO | VIA PRINCIPE DI PIEMONTE, 45 | 86100 | 0874 - 90147 | PROCMIN.CAMPOBASSO@GIUSTIZIA.IT |
|  | 08701501208 | CATANIA | VIA RAIMONDO FRANCHETTI, 62 | 95123 | 095-7240113 | PROCMIN.CATANIA@GIUSTIZIA.IT |
|  | 07902301205 | CATANZARO | VIA PAGLIA, 47 | 88100 | 0961-517211 (CENTRALINO) | PROCMIN.CATANZARO@GIUSTIZIA.IT |
|  | 04801701205 | FIRENZE | VIA DELLA SCALA, 79 | 50123 | 055 - 267296 | PROCMIN.FIRENZE@GIUSTIZIA.IT |
|  | 01002501208 | GENOVA | V.LE 4 NOVEMBRE, 4 | 16121 | 010 - 586440 / 587506 / 594117 | PROCMIN.GENOVA@GIUSTIZIA.IT |
|  | 06604901204 | L'AQUILA | VIA ACQUASANTA, 1 | 67100 | 0862 - 25372 | PROCMIN.LAQUILA@GIUSTIZIA.IT |
|  | 07503501206 | LECCE | VIA GRAMSCI, 1-2 | 73100 | 0832-462111 | PROCMIN.LECCE@GIUSTIZIA.IT |
|  | 08304801203 | MESSINA | V.LE EUROPA, 137 | 98124 | 090-2928088 | PROCMIN.MESSINA@GIUSTIZIA.IT |
|  | 01514601209 | MILANO | VIA LEOPARDI, 18 | 20123 | 02 - 467581 | PROCMIN.MILANO@GIUSTIZIA.IT |
|  | 06304901201 | NAPOLI | V.LE COLLI AMINEI, 44 | 80131 | 081-7447111 | PROCMIN.NAPOLI@GIUSTIZIA.IT |
|  | 08205301203 | PALERMO | VIA PRINCIPE DI PALAGONIA, 135 | 90145 | 091-6824738 / 6824641 / 6813142 | PROCMIN.PALERMO@GIUSTIZIA.IT |
|  | 05403901209 | PERUGIA | VIA MARTIRI DEI LAGER, 65 | 06128 | 075 - 506311 | PROCMIN.PERUGIA@GIUSTIZIA.IT |
|  | 07606301206 | POTENZA | VIA APPIA, 175 BIS | 85100 | 0971-55544 | PROCMIN.POTENZA@GIUSTIZIA.IT |
|  | 08006301202 | REGGIO DI CALABRIA | VIA MARSALA, 13 | 89133 | 0965-23825 | PROCMIN.REGGIOCALABRIA@GIUSTIZIA.IT |
|  | 05809101203 | ROMA | VIA DEI BRESCIANI, 32 | 00186 | 06-6889601 | PROCMIN.ROMA@GIUSTIZIA.IT |
|  | 06511601206 | SALERNO | LARGO S. TOMMASO D'AQUINO | 84100 | 089-231297 | PROCMIN.SALERNO@GIUSTIZIA.IT |
|  | 09006401206 | SASSARI | VIA PREDDA NIEDDA, 6/C | 07100 | NULL | PROCMIN.SASSARI@GIUSTIZIA.IT |
|  | 07302701207 | TARANTO | P.ZZA DUOMO - PALAZZO SANTACHIARA | 74100 | 099-7343111 (CENTRALINO UFFICI GIUDIZIARI) / 7343569 | PROCMIN.TARANTO@GIUSTIZIA.IT |
|  | 00127201200 | TORINO | C.SO UNIONE SOVIETICA, 325 | 10135 | 011-6195801 | PROCMIN.TORINO@GIUSTIZIA.IT |
|  | 02220501204 | TRENTO | VIA ROSMINI, 71 | 38100 | 0461 - 220111 | PROCMIN.TRENTO@GIUSTIZIA.IT |
|  | 03200601204 | TRIESTE | VIA CORONEO, 20 | 34100 | 040 - 7792111 | PROCMIN.TRIESTE@GIUSTIZIA.IT |
|  | 02704201203 | VENEZIA | VIA FORTE MARGHERA VENEZIA - MESTRE | 30173 | 041 - 5066311 | PROCMIN.VENEZIA@GIUSTIZIA.IT |

Tabella 57 - Elenco Procure presso Tribunale per i minorenni

L’elenco aggiornato consegnato dalla Amministrazione contiene le seguenti Procure presso il Tribunale per i minorenni:
| N. | COD_UFFICIO | DESCRIZIONE | INDIRIZZO | CAP | TELEFONO | E_MAIL |
| --- | --- | --- | --- | --- | --- | --- |
|  | 04200201208 | ANCONA | VIA CAVORCHIE, 1/D | 60123 | 071.200173 | procmin.ancona@giustizia.it |
|  | 07200601202 | BARI | VIA TOMMASO FIORE, 49/D | 70123 | 080.5741717 080.5741716 | procmin.bari@giustizia.it |
|  | 03700601209 | BOLOGNA | VIA DEL PRATELLO, 36 | 40122 | 051.264895 | procmin.bologna@giustizia.it |
|  | 02100801205 | BOLZANO | CORSO LIBERTA', 23 | 39100 | 0471.226111 0471.226433 0471.226432 | procmin.bolzano@giustizia.it |
|  | 01702901203 | BRESCIA | VIA MALTA, 12 | 25125 | 030.2421832 | procmin.brescia@giustizia.it |
|  | 09200901202 | CAGLIARI | VIA DANTE, 6 | 09127 | 070.34921 | procmin.cagliari@giustizia.it |
|  | 08500401203 | CALTANISSETTA | VIA F. TURATI, 46 | 93100 | 0934.597337 0934.597340 | procmin.caltanissetta@giustizia.it |
|  | 07000601200 | CAMPOBASSO | VIA PRINCIPE DI PIEMONTE, 45 | 86100 | 0874.43181 | procmin.campobasso@giustizia.it |
|  | 08701501208 | CATANIA | VIA R. FRANCHETTI, 62 | 95131 | 095.7240113 095.7240111 | procmin.catania@giustizia.it |
|  | 07902301205 | CATANZARO | VIA PAGLIA, 47 | 88100 | 0961.517211 | procmin.catanzaro@giustizia.it |
|  | 04801701205 | FIRENZE | VIA DELLA SCALA, 79 | 50123 | 055.267296 | procmin.firenze@giustizia.it |
|  | 01002501208 | GENOVA | VIALE IV NOVEMBRE, 4 | 16129 | 010.587506- 010.586440 | procmin.genova@giustizia.it |
|  | 06604901204 | L'AQUILA | VIA ACQUASANTA, 1 | 67100 | 0862.25372 | procmin.laquila@giustizia.it |
|  | 07503501206 | LECCE | VIA DALMAZIO BIRAGO, S.N. | 73100 | 0832.2111 | procmin.lecce@giustizia.it |
|  | 08304801203 | MESSINA | VIALE EUROPA, 137 | 98124 | 090.2928088 | procmin.messina@giustizia.it |
|  | 01514601209 | MILANO | VIA G. LEOPARDI, 18 | 20123 | 02.467581 | procmin.milano@giustizia.it |
|  | 06304901201 | NAPOLI | VIALE COLLI AMINEI, 44 | 80131 | 081.7447111 | procmin.napoli@giustizia.it |
|  | 05403901209 | PALERMO | VIA PRINCIPE DI PALAGONIA, 135 | 90145 | 091.6824738 091.6824641 091.6813142 | procmin.palermo@giustizia.it |
|  | 07606301206 | PERUGIA | VIA MARTIRI DEI LAGER, 65 | 06128 | 075.506311 | procmin.perugia@giustizia.it |
|  | 08006301202 | POTENZA | VIA APPIA, 175/BIS | 85100 | 0971.55544 | procmin.potenza@giustizia.it |
|  | 05809101203 | REGGIO CALABRIA | VIA MARSALA, 13 | 89133 | 0965.23825 | procmin.reggiocalabria@giustizia.it |
|  | 06511601206 | ROMA | VIA DEI BRESCIANI, 32 | 00186 | 06.6889601 | procmin.roma@giustizia.it |
|  | 05403901209 | SALERNO | LARGO S. TOMMASO D'AQUINO | 84100 | 089.2570111 | procmin.salerno@giustizia.it |
|  | 09006401206 | SASSARI | Strada prov.le Sassari/Ittiri Km 0.500 Loc. Piandanna | 07100 | 079.2637245 | procmin.sassari@giustizia.it |
|  | 07302701207 | TARANTO | VIA DUOMO - PALAZZO S. CHIARA | 74100 | 099.7343111 | procmin.taranto@giustizia.it |
|  | 00127201200 | TORINO | CORSO UNIONE SOVIETICA, 325 | 10135 | 011.6195801 | procmin.torino@giustizia.it |
|  | 02220501204 | TRENTO | VIA ROSMINI, 71 | 38100 | 0461.220111 0461.2202229 | procmin.trento@giustizia.it |
|  | 03200601204 | TRIESTE | Foro Ulpiano, 1 c/o Tribunale Ordinario | 34100 | 040.7792111 | procmin.trieste@giustizia.it |
|  | 02704201203 | VENEZIA | VIA BISSA - MESTRE | 30173 | 041.5066311 | procmin.venezia@giustizia.it |

Tabella 58 - Nuovo elenco Procure presso Tribunale per i minorenni

Le informazioni evidenziate in verde devono essere aggiornate nella tabella <UFFICI>.
Attualmente le informazioni dei  Tribunale per i minorenni sono contenute nella tabella <UFFICI> con campo <COD_TIPO_UFFICIO> = “DIBM”:

| N. | COD_UFFICIO | DESCRIZIONE | INDIRIZZO | CAP | TELEFONO | E_MAIL |
| --- | --- | --- | --- | --- | --- | --- |
|  | 04200201107 | ANCONA | VIA CAVORCHIE, 1/D | 60121 | 071 - 204546 | TRIBMIN.ANCONA@GIUSTIZIA.IT |
|  | 07200601101 | BARI | VIA TOMMASO FIORE, 49/D | 70123 | 080-5744133 /  5741658 | TRIBMIN.BARI@GIUSTIZIA.IT |
|  | 03700601108 | BOLOGNA | VIA DEL PRATELLO, 36 | 40122 | 051 - 2964880 | TRIBMIN.BOLOGNA@GIUSTIZIA.IT ADOZIONI.CIVILE.TRIBMIN.BOLOGNA@GIUSTIZIA.IT   GIPGUP.TIBMIN.BOLOGNA@GIUSTIZIA.IT |
|  | 02100801104 | BOLZANO | C.SO LIBERTA', 25 | 39100 | 0471 - 226111 (CENTRALINO) | TRIBMIN.BOLZANO@GIUSTIZIA.IT |
|  | 01702901102 | BRESCIA | VIA MALTA, 12 | 25125 | 030 - 2420151 | TRIBMIN.BRESCIA@GIUSTIZIA.IT |
|  | 09200901101 | CAGLIARI | VIA DANTE, 1 | 09127 | 070-34921 | TRIBMIN.CAGLIARI@GIUSTIZIA.IT |
|  | 08500401102 | CALTANISSETTA | VIA DON MINZONI | 93100 | 0934-597339 | TRIBMIN.CALTANISSETTA@GIUSTIZIA.IT |
|  | 07000601109 | CAMPOBASSO | VIA PRINCIPE DI PIEMONTE, 45 | 86100 | 0874 - 90143 / 90145 | TRIBMIN.CAMPOBASSO@GIUSTIZIA.IT |
|  | 08701501107 | CATANIA | VIA RAIMONDO FRANCHETTI, 62 | 95131 | 095-7240112 | TRIBMIN.CATANIA@GIUSTIZIA.IT |
|  | 07902301104 | CATANZARO | VIA PAGLIA | 88100 | 0961-517111 | TRIBMIN.CATANZARO@GIUSTIZIA.IT |
|  | 04801701104 | FIRENZE | VIA DELLA SCALA, 79 | 50123 | 055 - 267295 | TRIBMIN.FIRENZE@GIUSTIZIA.IT |
|  | 01002501107 | GENOVA | V.LE IV NOVEMBRE, 4 | 16121 | 010 - 596191 | TRIBMIN.GENOVA@GIUSTIZIA.IT |
|  | 06604901103 | L'AQUILA | VIA ACQUASANTA, 1 | 67100 | 0862 - 420083 / 420341 / 420342 | TRIBMIN.LAQUILA@GIUSTIZIA.IT |
|  | 07503501105 | LECCE | VIA GRAMSCI, 1-3 | 73100 | 0832-461111 | TRIBMIN.LECCE@GIUSTIZIA.IT |
|  | 08304801102 | MESSINA | V.LE EUROPA, 137 | 98124 | 090-2937370 / 2937391 | TRIBMIN.MESSINA@GIUSTIZIA.IT |
|  | 01514601108 | MILANO | VIA LEOPARDI, 18 | 20123 | 02 - 4672230 / 4672231 | TRIBMIN.MILANO@GIUSTIZIA.IT |
|  | 06304901100 | NAPOLI | V.LE COLLI AMINEI, 42 | 80131 | 081-7449111 | TRIBMIN.NAPOLI@GIUSTIZIA.IT |
|  | 08205301102 | PALERMO | VIA PRINCIPE DI PALAGONIA, 135 | 90145 | 091-6813067 / 6817360 / 6823863 | TRIBMIN.PALERMO@GIUSTIZIA.IT |
|  | 05403901108 | PERUGIA | VIA MARTIRI DEI LAGER, 65 (SCALA B) | 06128 | 075 - 506311 | TRIBMIN.PERUGIA@GIUSTIZIA.IT |
|  | 07606301105 | POTENZA | VIA APPIA, 175/BIS | 85100 | 0971-52071 / 55258 | TRIBMIN.POTENZA@GIUSTIZIA.IT |
|  | 08006301101 | REGGIO DI CALABRIA | VIA MARSALA, 13 | 89133 | 0965-812987 | TRIBMIN.REGGIOCALABRIA@GIUSTIZIA.IT |
|  | 05809101102 | ROMA | VIA DEI BRESCIANI, 32 | 00186 | 06-688931 | TRIBMIN.ROMA@GIUSTIZIA.IT |
|  | 06511601105 | SALERNO | LARGO S. TOMMASO D'AQUINO | 84100 | 089-254251 / 231184 | TRIBMIN.SALERNO@GIUSTIZIA.IT |
|  | 09006401105 | SASSARI | VIA PREDDA NIEDDA, 6/C | 07100 | 079-2637200 | TRIBMIN.SASSARI@GIUSTIZIA.IT |
|  | 07302701106 | TARANTO | P.ZZA DUOMO - PALAZZO SANTACHIARA | 74100 | 099-7343111 (CENTRALINO UFFICI GIUDIZIARI) / 7343558 | TRIBMIN.TARANTO@GIUSTIZIA.IT |
|  | 00127201109 | TORINO | C.SO UNIONE SOVIETICA, 325 | 10135 | 011-6195701 / 6195711 | NULL |
|  | 02220501103 | TRENTO | VIA ROSMINI, 71 | 38100 | 0461 - 234736 / 237221 | TRIBMIN.TRENTO@GIUSTIZIA.IT |
|  | 03200601103 | TRIESTE | VIA CORONEO, 20 | 34100 | 040 - 7792111 | TRIBMIN.TRIESTE@GIUSTIZIA.IT |
|  | 02704201102 | VENEZIA | VIA BISSA S.N. - MESTRE (VE) | 30172 | 041 - 5066212 / 041- 5066111 (CENTRALINO - NON ANCORA ATTIVO) | TRIBMIN.VENEZIA@GIUSTIZIA.IT |

Tabella 59 - Elenco Tribunali per i minorenni
L’elenco del  Magistrato di Sorveglianza per i minorenni e L’elenco del  Tribunale per i  Minorenni in funzione di Tribunale di Sorveglianza  devono essere popolato con i seguenti valori:

| N. | COD_UFFICIO | DESCRIZIONE | INDIRIZZO | CAP | TELEFONO | E_MAIL |
| --- | --- | --- | --- | --- | --- | --- |
|  | 04200201107 | ANCONA | VIA CAVORCHIE, 1/C | 60121 | 071.20898603 | tribmin.ancona@giustizia.it |
|  | 07200601101 | BARI | VIA TOMMASO FIORE, 49/D | 70123 | 080.5744133 - 080.5744357 | tribmin.bari@giustizia.it |
|  | 03700601108 | BOLOGNA | VIA DEL PRATELLO, 36 | 40122 | 051.2964880 | tribmin.bologna@giustizia.it |
|  | 02100801104 | BOLZANO | CORSO LIBERTA', 25 | 39100 | 0471.226111 | tribmin.bolzano@giustizia.it |
|  | 01702901102 | BRESCIA | VIA MALTA, 12 | 25125 | 030.2420151 | tribmin.brescia@giustizia.it |
|  | 09200901101 | CAGLIARI | VIA DANTE, 1 | 09127 | 070.34921 | tribmin.cagliari@giustizia.it |
|  | 08500401102 | CALTANISSETTA | VIA DON MINZONI | 93100 | 0934.597339 | tribmin.caltanissetta@giustizia.it |
|  | 07000601109 | CAMPOBASSO | VIA PRINCIPE DI PIEMONTE, 45 | 86100 | 0874.43181 | tribmin.campobasso@giustizia.it |
|  | 08701501107 | CATANIA | VIA R. FRANCHETTI, 62 | 95123 | 095.7240112 | tribmin.catania@giustizia.it |
|  | 07902301104 | CATANZARO | VIA PAGLIA, 47 | 88100 | 0961.517111 - 0961.517163 | tribmin.catanzaro@giustizia.it |
|  | 04801701104 | FIRENZE | VIA DELLA SCALA, 79 | 50123 | 055.267295 | tribmin.firenze@giustizia.it |
|  | 01002501107 | GENOVA | VIALE IV NOVEMBRE, 4 | 16121 | 010.596191 | tribmin.genova@giustizia.it |
|  | 06604901103 | L'AQUILA | VIA ACQUASANTA, 1 | 67100 | 0862.4841200 | tribmin.laquila@giustizia.it |
|  | 07503501105 | LECCE | VIA DALMAZIO BIRAGO, S.N. | 73100 | 0832.2131 337/827743 (ore ufficio) | tribmin.lecce@giustizia.it |
|  | 08304801102 | MESSINA | VIALE EUROPA, 137 | 98124 | 090.2937370 - 090.2937391 | tribmin.messina@giustizia.it |
|  | 01514601108 | MILANO | VIA G. LEOPARDI, 18 | 20123 | 02.46721 | tribmin.milano@giustizia.it |
|  | 06304901100 | NAPOLI | VIALE COLLI AMINEI, 42 | 80131 | 081.7449111-7447312 | tribmin.napoli@giustizia.it |
|  | 08205301102 | PALERMO | VIA PRINCIPE DI PALAGONIA, 135 | 90145 | 091.6813067 - 6817360 - 6823863 | tribmin.palermo@giustizia.it |
|  | 05403901108 | PERUGIA | VIA MARTIRI DEI LAGER, 65 | 06128 | 075.506311 | tribmin.perugia@giustizia.it |
|  | 07606301105 | POTENZA | VIA APPIA, 175/BIS | 85100 | 0971.52071 - 0971.55258 | tribmin.potenza@giustizia.it |
|  | 08006301101 | REGGIO CALABRIA | VIA MARSALA, 13 | 89133 | 0965.812987 | tribmin.reggiocalabria@giustizia.it |
|  | 05809101102 | ROMA | VIA DEI BRESCIANI, 32 | 00186 | 06.688931 | tribmin.roma@giustizia.it |
|  | 06511601105 | SALERNO | LARGO S. TOMMASO D'AQUINO | 84100 | 089.254251 - 089.231184 | tribmin.salerno@giustizia.it |
|  | 09006401105 | SASSARI | Strada prov.le Sassari/Ittiri Km 0.500 Loc. Piandanna | 07100 | 079.2637200 | tribmin.sassari@giustizia.it |
|  | 07302701106 | TARANTO | VIA DUOMO - PALAZZO S. CHIARA | 74100 | 099.7343111/7343558 | tribmin.taranto@giustizia.it |
|  | 00127201109 | TORINO | CORSO UNIONE SOVIETICA, 325 | 10135 | 011-6195701 - 011.6195711 | tribmin.torino@giustizia.it |
|  | 02220501103 | TRENTO | VIA ROSMINI, 71 | 38100 | 0461.234736 - 0461.237221 | tribmin.trento@giustizia.it |
|  | 03200601103 | TRIESTE | Foro Ulpiano, 1 c/o Tribunale Ordinario | 34121 | 040.7792111 | tribmin.trieste@giustizia.it |
|  | 02704201102 | VENEZIA | VIA BISSA - MESTRE | 37173 | 041.5066212 / 101 | tribmin.venezia@giustizia.it |

Tabella 60 – Nuovo elenco Tribunali per i minorenni
Gli  Uffici  servizi  sociali minorenni (USSM) svolgono attività/funzionalità molto simili agli Uffici per l'esecuzione penale esterna (UEPE) dell’ambito degli uffici per i maggiorenni.
Attualmente le informazioni degli UEPE sono contenute nella tabella <Ufficio> aventi <COD_TIPO_UFFICIO> uguale a “UEPE” ed a ”UEPESS” per le sedi distaccate.
In modo analogo gli USSM devono essere inseriti nella tabella <Ufficio> con <COD_TIPO_UFFICIO> uguale a “USSM”.
Per le sedi distaccate il <COD_TIPO_UFFICIO> deve essere uguale a “USSMSS”.
I codici ufficio corretti degli USSM e degli USSMSS sono stati forniti dall’Ammistrazione.
L’elenco degli  USSM deve essere popolato con i seguenti valori:

| N. | COD_UFFICIO | DESCRIZIONE | INDIRIZZO | CAP | TELEFONO | E_MAIL |
| --- | --- | --- | --- | --- | --- | --- |
|  |  | BARI | VIA AMENDOLA, 172/C | 70126 | 080.5481555 | ussm.bari.dgm@giustizia.it |
|  |  | BOLOGNA | VIA DEL PRATELLO, 34 | 40122 | 051.266419 - 238478 | ussm.bologna.dgm@giustizia.it |
|  |  | BOLZANO | PIAZZA VITTORIA, 47 | 39100 | 0471.262854 | ussm.bolzano.dgm@giustizia.it |
|  |  | BRESCIA | VIA MALTA, 12 | 25124 | 030.2424071-221445 | ussm.brescia.dgm@giustizia.it |
|  |  | CAGLIARI | VIA SONNINO,184 | 09128 | 070.401981 - 070.401982 | ussm.cagliari.dgm@giustizia.it |
|  |  | CALTANISSETTA | VIA DON MINZONI | 93100 | 0934.551372 | ussm.caltanissetta.dgm@giustizia.it |
|  |  | CAMPOBASSO | VIA PRINCIPE DI PIEMONTE, 61 | 86100 | 0874.47761 | ussm.campobasso.dgm@giustizia.it |
|  |  | CATANIA | PIAZZA DELLA REPUBBLICA, 31 | 95129 | 095.535566 - 095.532379 | ussm.catania.dgm@giustizia.it |
|  |  | CATANZARO | VIA PAGLIA, 47 | 88100 | 0961.517511 | ussm.catanzaro.dgm@giustizia.it |
|  |  | FIRENZE | VIA BOLOGNESE, 86 | 50139 | 055.471826 | ussm.firenze.dgm@giustizia.it |
|  |  | GENOVA | VIA PASSO FRUGONI, 4/3 | 16121 | 010.541771 - 5451575 - 543675 | ussm.genova.dgm@giustizia.it |
|  |  | L'AQUILA | VIA ACQUASANTA, 1 | 67100 | 0862.483745 | ussm.laquila.dgm@giustizia.it |
|  |  | LECCE | VIA DALMAZIO BIRAGO, S.N. | 73100 | 0832.246919 - 241880 | ussm.lecce.dgm@giustizia.it |
|  |  | MESSINA | VIALE EUROPA, 137 | 98124 | 090.2921270 | ussm.messina.dgm@giustizia.it |
|  |  | MILANO | VIA G.SPAGLIARDI | 20152 | 02.414901 - 41490302-304-306 | ussm.milano.dgm@giustizia.it |
|  |  | NAPOLI | VIALE COLLI AMINEI, 44 | 80131 | 081.7448271 | ussm.napoli.dgm@giustizia.it |
|  |  | PALERMO | VIA CILEA (COMPL. MALASPINA) | 90144 | 091.6828732 | ussm.palermo.dgm@giustizia.it |
|  |  | PERUGIA | VIA MARTIRI DEI LAGER, 65 | 06128 | 075.5063138 | ussm.perugia.dgm@giustizia.it |
|  |  | POTENZA | VIA APPIA, 175/BIS | 85100 | 0971.54467 | ussm.potenza.dgm@giustizia.it |
|  |  | REGGIO CALABRIA | CORSO GARIBALDI, 404 | 89127 | 0965.24500 | ussm.reggiocalabria.dgm@giustizia.it |
|  |  | ROMA | VIA AGNELLI, 15 | 00151 | 06.96668011 | ussm.roma.dgm@giustizia.it |
|  |  | SALERNO | VIA G. NEGRI, 5 | 84100 | 089.229478 | ussm.salerno.dgm@giustizia.it |
|  |  | SASSARI | VIA PREDDA NIEDDA, 6C | 07100 | 079.2633024 | ussm.sassari.dgm@giustizia.it |
|  |  | TARANTO | VICO S. AGOSTINO, 1 | 74100 | 099.4706054 | ussm.taranto.dgm@giustizia.it |
|  |  | TORINO | VIA BERRUTI E FERRERO, 1/A | 10135 | 011.6194260 | ussm.torino.dgm@giustizia.it |
|  |  | TRENTO | VIA MADRUZZO, 13 | 38100 | 0461.984261- 982056 | ussm.trento.dgm@giustizia.it |
|  |  | TRIESTE | VIA CARDUCCI, 20 | 34122 | 040-635254 040-635003 | ussm.trieste.dgm@giustizia.it |
|  |  | VENEZIA | VIA BISSA - MESTRE | 30173 | 041.5060836 - 5060889 | ussm.venezia.dgm@giustizia.it |

Tabella 61 - Elenco Uffici Servizi Sociali Minorenni

L’elenco  USSMSS deve essere popolato con i seguenti valori:


| N. | COD_UFFICIO | DESCRIZIONE | INDIRIZZO | CAP | TELEFONO | E_MAIL |
| --- | --- | --- | --- | --- | --- | --- |
|  |  | ANCONA | VIA CAVORCHIE, 1/E | 60100 | 071.201004 | ussm.ancona.dgm@giustizia.it |
|  |  | BRINDISI | VIA INDIPENDENZA, 8 | 72100 | 0831.521481 |  |
|  |  | CITTANOVA - R.C. | VIALE MERANO | 89022 | 0966.662406 |  |
|  |  | COSENZA | VIA GIOVANNI AMELLINO c/o II Circoscrizione | 87100 | 0984.34861 |  |
|  |  | ERICE | Via Giuseppe Clemente,100 ERICE località Casa Santa (TP) | 91016 | 0923 553208 |  |
|  |  | FOGGIA | PIAZZA CAVOUR 1 | 71100 | 0881.776031 |  |
|  |  | FROSINONE | PIAZZA S. TOMMASO D'AQUINO 25 | 03100 | 0775.211866 |  |
|  |  | GELA | CORSO VITTORIO EMANUELE, 168 | 93012 | 0933.823628 |  |
|  |  | LA SPEZIA | VIA DON MINZONI 43 | 19100 | 0187.22238 |  |
|  |  | LATINA | VIA DON MOROSINI, 2 | 04100 | 0773.662946 |  |
|  |  | LIVORNO | Via Caduti del Lavoro,26 | 57100 | 0586 264126 |  |
|  |  | LUCCA | VIA DELLE SETTE ARTI 3 | 55100 | 0583.464459 |  |
|  |  | MATERA | VIA CAPPELLUTI, 60/62 | 75100 | 0835.336055 |  |
|  |  | NUORO | VIALE SARDEGNA 33 B | 08100 | 0784.33580 |  |
|  |  | PADOVA | PIAZZA DEI FRUTTI, 38 | 35100 | 049.8758155 |  |
|  |  | PATTI-ME | VIA MOLINO CROCE | 98066 | 0941.245289 |  |
|  |  | PESCARA | VIA RIGOPIANO, 30/1 | 65100 | 085.2058848 - 085.2058971 |  |
|  |  | RAGUSA | VIA NATANELLI, 58 | 97100 | 0932.245520 |  |
|  |  | RIMINI | Via Alberto Dalla Chiesa, 11 | 47900 | 0541-763554 |  |
|  |  | SIENA | VIA TOMMASO PENDOLA, 37 | 53100 | 0577.283623 |  |
|  |  | SIRACUSA | VIA SANTA PANAGIA, 109 | 96100 | 0931.752685 - 0931.752686 |  |
|  |  | TERAMO | VIA G. BOVIO 6 | 64100 | 0861/243063 |  |
|  |  | TREVISO | VIA D'ANNUNZIO, 28 | 31100 | 0422.410507 |  |
|  |  | UDINE | VIA LARGA, 35 | 33100 | 0432.505744-512883 |  |
|  |  | VERONA | VIA VALERIO CATULLO, 12 | 37121 | 045.8030177 |  |
|  |  | VICENZA | VIA PESCHERIE VECCHIE 26 | 36100 | 0444.323265 |  |

Tabella 62 - Elenco Uffici Servizi Sociali Minorenni sedi distaccate
Solo l’ufficio USSM - sede distaccata contiene nel campo <COD_UFFICIO_COMPETENTE> il legame con l’ufficio centrale.
L’intervento in oggetto non prevede la memorizzazione di informazioni in maniera difforme dall’attuale.
Pertanto, le informazioni inserite dall’operatore dopo l’intervento in parola continuano ad essere memorizzate nelle tabelle e nei campi appositi con le modalità e nel rispetto delle regole uguali a quelle esistenti e valide prima dell’intervento medesimo.
I rimanenti algoritmi, se non indicato diversamente in modo esplicito, rimangono immutati.

## Modifica database
Pertanto, l’intervento in oggetto prevede:
l’inserimento nella tabella <ISTITUTO_DETENZIONE> di un nuovo record
l’aggiornamento della tabella <ISTITUTO_DETENZIONE>
l’aggiornamento della tabella <UFFICIO> delle occorrenze per il <COD_TIPO_UFFICIO> uguale a  “PMM”
l’aggiornamento della tabella <UFFICIO> delle occorrenze per il <COD_TIPO_UFFICIO> uguale a  “DIBM”
l’aggiornamento della tabella <UFFICIO> delle occorrenze per il <COD_TIPO_UFFICIO> uguale a  “UEPE” ed uguale a  “UEPESS” per la sede di Vibo Valentia.
l’aggiornamento della tabella <CSSA> delle occorrenze per il <TIPO> uguale a  “UEPE” ed uguale a  “UEPESS” per la sede di Vibo Valentia.
l’inserimento nella tabella <UFFICIO> delle occorrenze per il <COD_TIPO_UFFICIO> uguale a  USSM ed uguale a  “USSMSS”.
l’inserimento nella tabella <CSSA> delle occorrenze per il <TIPO> uguale a  “USSM” ed uguale a  “USSMSS”
l’inserimento nella tabella <CG_REF_CODES> di 2 nuove occorrenze.

Inserimento nella tabella <ISTITUTO_DETENZIONE> del record:

| N. | ID_
ISTITUTO__
DETENZIONE | COD_
TIPO_
ISTITUTO | COD_COMUNE | CODICE_
PROVINCIA | INDIRIZZO | DESCRIZIONE | NOTE | COD_DISTRETTO |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | RR04 | 48 | 045014 | MS | Via IV Novembre, 15 | NULL | NULL | 01002500600 |

Tabella 63 - Nuovo record istituto minorile

Aggiornamento della tabella <ISTITUTO_DETENZIONE>: vedere Tabella 56 - Nuovo elenco Istituti detentivi minorili.

Aggiornamento della tabella <UFFICIO> delle occorrenze per il <COD_TIPO_UFFICIO> uguale a  “PMM”: vedere Tabella 58 - Nuovo elenco Procure presso Tribunale per i minorenni.

Aggiornamento della tabella <UFFICIO> delle occorrenze per il <COD_TIPO_UFFICIO> uguale a  “DIBM”: vedere Tabella 60 – Nuovo elenco Tribunali per i minorenni.

Aggiornamento della tabella <UFFICIO> della occorrenza per UEPE di Vibo Valentia:

| N | COD_
UFFICIO | COD_
PROVINCIA | COD_
COMUNE | COD_
DISTRETTO | COD_
UFFICIO_
COMPETENTE | INDIRIZZO | CAP | TELEFONO | FAX | E_MAIL |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | 10204702109 | VV | 102047 | 07902300607 | 07902300809 | Contrada Castelluccio -Località Cocari | 89900 | 0963 472383 | 0963 471006 |  |

Tabella 64 – Tabella <UFFICIO> - riferimenti aggiornati UEPE  Vibo Valentia
I seguenti campi sono uguali per tutte le occorrenze della tabella precedente.

| CAMPO | VALORE | NOTA |
| --- | --- | --- |
| COD_TIPO_UFFICIO | UEPESS |  |
| DATA_CARICAMENTO_REGE | 10/04/2003  12.06.13 |  |
| COD_OPERATORE_AGG | null |  |
| DATA_AGG | null |  |
| COD_UFFICIO_AGG | null |  |
| FLAG_ACCORP. | N |  |


Aggiornamento della tabella <CSSA> della occorrenza per UEPE di Vibo Valentia:

| N | ID_CSSA | TIPO | COMUNE | INDIRIZZO | EMAIL | FAX | TEL | INCARICO | TITOLO | NOME | COGNOME | DATA_CARICAMENTO |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | 64 | UEPESS | VIBO VALENTIA | Contrada Castelluccio-Località Cocari |  | 0963 471006 | 0963 472383 | NULL | NULL | NULL | NULL | 31/08/2006  0.00.00 |

Tabella 65 - Tabella <CSSA> - riferimenti aggiornati UEPE  Vibo Valentia

L’inserimento nella tabella <UFFICIO> delle occorrenze per il <COD_TIPO_UFFICIO> uguale a  USSM ed uguale a  “USSMSS”:

| N | COD_
UFFICIO | COD_
PROVINCIA | COD_
COMUNE | COD_
DISTRETTO | COD_
UFFICIO_
COMPETENTE | INDIRIZZO | CAP | TELEFONO | FAX | E_MAIL |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | 07200600818 | BA | 072006 | 07200600604 | NULL | VIA AMENDOLA, 172/C | 70126 | 080.5481555 | NULL | ussm.bari.dgm@giustizia.it |
|  | 03700600815 | BO | 037006 | 03700600601 | NULL | VIA DEL PRATELLO, 34 | 40122 | 051.266419 - 238478 | NULL | ussm.bologna.dgm@giustizia.it |
|  | 02100800811 | BZ | 021008 | 02100800607 | NULL | PIAZZA VITTORIA, 47 | 39100 | 0471.262854 | NULL | ussm.bolzano.dgm@giustizia.it |
|  | 01702900819 | BS | 017029 | 01702900605 | NULL | VIA MALTA, 12 | 25124 | 030.2424071-221445 | NULL | ussm.brescia.dgm@giustizia.it |
|  | 09200900818 | CA | 092009 | 09200900604 | NULL | VIA SONNINO,184 | 09128 | 070.401981 - 070.401982 | NULL | ussm.cagliari.dgm@giustizia.it |
|  | 08500400819 | CL | 085004 | 08500400605 | NULL | VIA DON MINZONI | 93100 | 0934.551372 | NULL | ussm.caltanissetta.dgm@giustizia.it |
|  | 07000600816 | CB | 070006 | 07000600602 | NULL | VIA PRINCIPE DI PIEMONTE, 61 | 86100 | 0874.47761 | NULL | ussm.campobasso.dgm@giustizia.it |
|  | 08701500814 | CT | 087015 | 08701500600 | NULL | PIAZZA DELLA REPUBBLICA, 31 | 95129 | 095.535566 - 095.532379 | NULL | ussm.catania.dgm@giustizia.it |
|  | 07902300811 | CZ | 079023 | 07902300607 | NULL | VIA PAGLIA, 47 | 88100 | 0961.517511 | NULL | ussm.catanzaro.dgm@giustizia.it |
|  | 04801700811 | FI | 048017 | 04801700607 | NULL | VIA BOLOGNESE, 86 | 50139 | 055.471826 | NULL | ussm.firenze.dgm@giustizia.it |
|  | 01002500814 | GE | 010025 | 01002500600 | NULL | VIA PASSO FRUGONI, 4/3 | 16121 | 010.541771 - 5451575 - 543675 | NULL | ussm.genova.dgm@giustizia.it |
|  | 06604900810 | AQ | 066049 | 06604900606 | NULL | VIA ACQUASANTA, 1 | 67100 | 0862.483745 | NULL | ussm.laquila.dgm@giustizia.it |
|  | 07503500812 | LE | 075035 | 07503500608 | NULL | VIA DALMAZIO BIRAGO, S.N. | 73100 | 0832.246919 - 241880 | NULL | ussm.lecce.dgm@giustizia.it |
|  | 08304800819 | ME | 083048 | 08304800605 | NULL | VIALE EUROPA, 137 | 98124 | 090.2921270 | NULL | ussm.messina.dgm@giustizia.it |
|  | 01514600815 | MI | 015146 | 01514600601 | NULL | VIA G.SPAGLIARDI | 20152 | 02.414901 - 41490302-304-306 | NULL | ussm.milano.dgm@giustizia.it |
|  | 06304900817 | NA | 063049 | 06304900603 | NULL | VIALE COLLI AMINEI, 44 | 80131 | 081.7448271 | NULL | ussm.napoli.dgm@giustizia.it |
|  | 08205300819 | PA | 082053 | 08205300605 | NULL | VIA CILEA (COMPL. MALASPINA) | 90144 | 091.6828732 | NULL | ussm.palermo.dgm@giustizia.it |
|  | 05403900815 | PG | 054039 | 05403900601 | NULL | VIA MARTIRI DEI LAGER, 65 | 06128 | 075.5063138 | NULL | ussm.perugia.dgm@giustizia.it |
|  | 07606300812 | PZ | 076063 | 07606300608 | NULL | VIA APPIA, 175/BIS | 85100 | 0971.54467 | NULL | ussm.potenza.dgm@giustizia.it |
|  | 08006300818 | RC | 080063 | 08006300604 | NULL | CORSO GARIBALDI, 404 | 89127 | 0965.24500 | NULL | ussm.reggiocalabria.dgm@giustizia.it |
|  | 05809100819 | RM | 058091 | 05809100605 | NULL | VIA AGNELLI, 15 | 00151 | 06.96668011 | NULL | ussm.roma.dgm@giustizia.it |
|  | 06511600812 | SA | 065116 | 06511600608 | NULL | VIA G. NEGRI, 5 | 84100 | 089.229478 | NULL | ussm.salerno.dgm@giustizia.it |
|  | 09006400812 | SS | 090064 | 09006400608 | NULL | VIA PREDDA NIEDDA, 6C | 07100 | 079.2633024 | NULL | ussm.sassari.dgm@giustizia.it |
|  | 07302700813 | TA | 073027 | 07302700609 | NULL | VICO S. AGOSTINO, 1 | 74100 | 099.4706054 | NULL | ussm.taranto.dgm@giustizia.it |
|  | 00127200816 | TO | 001272 | 00127200602 | NULL | VIA BERRUTI E FERRERO, 1/A | 10135 | 011.6194260 | NULL | ussm.torino.dgm@giustizia.it |
|  | 02220500810 | TN | 022205 | 02220500606 | NULL | VIA MADRUZZO, 13 | 38100 | 0461.984261- 982056 | NULL | ussm.trento.dgm@giustizia.it |
|  | 03200600810 | TS | 032006 | 03200600606 | NULL | VIA CARDUCCI, 20 | 34122 | 040-635254 040-635003 | NULL | ussm.trieste.dgm@giustizia.it |
|  | 02704200819 | VE | 027042 | 02704200605 | NULL | VIA BISSA - MESTRE | 30173 | 041.5060836 - 5060889 | NULL | ussm.venezia.dgm@giustizia.it |

Tabella 66 – Tabella <UFFICIO> - USSM
I seguenti campi sono uguali per tutte le occorrenze della tabella precedente.

| CAMPO | VALORE | NOTA |
| --- | --- | --- |
| COD_TIPO_UFFICIO | USSM |  |
| DATA_CARICAMENTO_REGE | null |  |
| COD_OPERATORE_AGG | null |  |
| DATA_AGG | null |  |
| COD_UFFICIO_AGG | null |  |
| FLAG_ACCORP. | N |  |



| N. | COD_
UFFICIO | COD_
PROVINCIA | COD_
COMUNE | COD_
DISTRETTO | COD_
UFFICIO_
COMPETENTE | INDIRIZZO | CAP | TELEFONO | FAX | E_MAIL |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | 04200200826 | AN | 042002 | 04200200600 | 06604900810 | VIA CAVORCHIE, 1/E | 60100 | 071.201004 | NULL | ussm.ancona.dgm@giustizia.it |
|  | 07400100822 | BR | 074001 | 07503500608 | 07503500812 | VIA INDIPENDENZA, 8 | 72100 | 0831.521481 | NULL | NULL |
|  | 08002800826 | RC | 080028 | 08006300604 | 08006300818 | VIALE MERANO | 89022 | 0966.662406 | NULL | NULL |
|  | 07804500828 | CS | 078045 | 07902300607 | 07902300811 | VIA GIOVANNI AMELLINO c/o II Circoscrizione | 87100 | 0984.34861 | NULL | NULL |
|  | 08100800825 | TP | 081008 | 08205300605 | 08205300819 | Via Giuseppe Clemente,100 ERICE località Casa Santa (TP) | 91016 | 0923 553208 | NULL | NULL |
|  | 07102400827 | FG | 071024 | 07200600604 | 07200600818 | PIAZZA CAVOUR 1 | 71100 | 0881.776031 | NULL | NULL |
|  | 06003800823 | FR | 060038 | 05809100605 | 05809100819 | PIAZZA S. TOMMASO D'AQUINO 25 | 03100 | 0775.211866 | NULL | NULL |
|  | 08500700827 | CL | 085007 | 08500400605 | 08500400819 | CORSO VITTORIO EMANUELE, 168 | 93012 | 0933.823628 | NULL | NULL |
|  | 01101500826 | SP | 011015 | 01002500600 | 01002500814 | VIA DON MINZONI 43 | 19100 | 0187.22238 | NULL | NULL |
|  | 05901100824 | LT | 059011 | 05809100605 | 05809100819 | VIA DON MOROSINI, 2 | 04100 | 0773.662946 | NULL | NULL |
|  | 04900900827 | LI | 049009 | 04801700607 | 04801700811 | Via Caduti del Lavoro,26 | 57100 | 0586 264126 | NULL | NULL |
|  | 04601700821 | LU | 046017 | 04801700607 | 04801700811 | VIA DELLE SETTE ARTI 3 | 55100 | 0583.464459 | NULL | NULL |
|  | 07701400822 | MT | 077014 | 07606300608 | 07606300812 | VIA CAPPELLUTI, 60/62 | 75100 | 0835.336055 | NULL | NULL |
|  | 09105100828 | NU | 091051 | 09006400608 | 09006400812 | VIALE SARDEGNA 33 B | 08100 | 0784.33580 | NULL | NULL |
|  | 02806000820 | PD | 028060 | 02704200605 | 02704200819 | PIAZZA DEI FRUTTI, 38 | 35100 | 049.8758155 | NULL | NULL |
|  | 08306600829 | ME | 083066 | 08304800605 | 08304800819 | VIA MOLINO CROCE | 98066 | 0941.245289 | NULL | NULL |
|  | 06802800820 | PE | 068028 | 06604900606 | 06604900810 | VIA RIGOPIANO, 30/1 | 65100 | 085.2058848 - 085.2058971 | NULL | NULL |
|  | 08800900824 | RG | 088009 | 08701500600 | 08701500814 | VIA NATANELLI, 58 | 97100 | 0932.245520 | NULL | NULL |
|  | 09901400828 | RN | 099014 | 03700600601 | 03700600815 | Via Alberto Dalla Chiesa, 11 | 47900 | 0541-763554 | NULL | NULL |
|  | 05203200821 | SI | 052032 | 04801700607 | 04801700811 | VIA TOMMASO PENDOLA, 37 | 53100 | 0577.283623 | NULL | NULL |
|  | 08901700822 | SR | 089017 | 08701500600 | 08701500814 | VIA SANTA PANAGIA, 109 | 96100 | 0931.752685 - 0931.752686 | NULL | NULL |
|  | 06704100827 | TE | 067041 | 06604900606 | 06604900810 | VIA G. BOVIO 6 | 64100 | 0861/243063 | NULL | NULL |
|  | 02608600822 | TV | 026086 | 02704200605 | 02704200819 | VIA D'ANNUNZIO, 28 | 31100 | 0422.410507 | NULL | NULL |
|  | 03012900820 | UD | 030129 | 03200600606 | 03200600810 | VIA LARGA, 35 | 33100 | 0432.505744-512883 | NULL | NULL |
|  | 02309100820 | VR | 023091 | 02704200605 | 02704200819 | VIA VALERIO CATULLO, 12 | 37121 | 045.8030177 | NULL | NULL |
|  | 02411600825 | VI | 024116 | 02704200605 | 02704200819 | PESCHERIE VECCHIE 26 | 36100 | 0444.323265 | NULL | NULL |

Tabella 67 – USSM – Sedi distaccate

I seguenti campi sono uguali per tutte le occorrenze della tabella precedente.

| CAMPO | VALORE | NOTA |
| --- | --- | --- |
| COD_TIPO_UFFICIO | USSMSS |  |
| DATA_CARICAMENTO_REGE | Null |  |
| COD_OPERATORE_AGG | null |  |
| DATA_AGG | null |  |
| COD_UFFICIO_AGG | null |  |
| FLAG_ACCORP. | N |  |


Inserimento nella tabella <CSSA> delle occorrenze per il <TIPO> uguale a  “USSM” ed uguale a  “USSMSS”:

| N | ID_CSSA | TIPO | COMUNE | INDIRIZZO | EMAIL | FAX | TEL | INCARICO | TITOLO | NOME | COGNOME | DATA_CARICAMENTO |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | 85 | USSM | BARI | VIA AMENDOLA, 172/C | ussm.bari.dgm@giustizia.it | NULL | 805.481.555 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 86 | USSM | BOLOGNA | VIA DEL PRATELLO, 34 | ussm.bologna.dgm@giustizia.it | NULL | 051.266419 - 238478 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 87 | USSM | BOLZANO | PIAZZA VITTORIA, 47 | ussm.bolzano.dgm@giustizia.it | NULL | 471.262.854 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 88 | USSM | BRESCIA | VIA MALTA, 12 | ussm.brescia.dgm@giustizia.it | NULL | 030.2424071-221445 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 89 | USSM | CAGLIARI | VIA SONNINO,184 | ussm.cagliari.dgm@giustizia.it | NULL | 070.401981 - 070.401982 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 90 | USSM | CALTANISSETTA | VIA DON MINZONI | ussm.caltanissetta.dgm@giustizia.it | NULL | 934.551.372 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 91 | USSM | CAMPOBASSO | VIA PRINCIPE DI PIEMONTE, 61 | ussm.campobasso.dgm@giustizia.it | NULL | 87.447.761 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 92 | USSM | CATANIA | PIAZZA DELLA REPUBBLICA, 31 | ussm.catania.dgm@giustizia.it | NULL | 095.535566 - 095.532379 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 93 | USSM | CATANZARO | VIA PAGLIA, 47 | ussm.catanzaro.dgm@giustizia.it | NULL | 961.517.511 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 94 | USSM | FIRENZE | VIA BOLOGNESE, 86 | ussm.firenze.dgm@giustizia.it | NULL | 55.471.826 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 95 | USSM | GENOVA | VIA PASSO FRUGONI, 4/3 | ussm.genova.dgm@giustizia.it | NULL | 010.541771 - 5451575 - 543675 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 96 | USSM | L'AQUILA | VIA ACQUASANTA, 1 | ussm.laquila.dgm@giustizia.it | NULL | 862.483.745 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 97 | USSM | LECCE | VIA DALMAZIO BIRAGO, S.N. | ussm.lecce.dgm@giustizia.it | NULL | 0832.246919 - 241880 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 98 | USSM | MESSINA | VIALE EUROPA, 137 | ussm.messina.dgm@giustizia.it | NULL | 902.921.270 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 99 | USSM | MILANO | VIA G.SPAGLIARDI | ussm.milano.dgm@giustizia.it | NULL | 02.414901 - 41490302-304-306 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 100 | USSM | NAPOLI | VIALE COLLI AMINEI, 44 | ussm.napoli.dgm@giustizia.it | NULL | 817.448.271 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 101 | USSM | PALERMO | VIA CILEA (COMPL. MALASPINA) | ussm.palermo.dgm@giustizia.it | NULL | 916.828.732 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 102 | USSM | PERUGIA | VIA MARTIRI DEI LAGER, 65 | ussm.perugia.dgm@giustizia.it | NULL | 755.063.138 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 103 | USSM | POTENZA | VIA APPIA, 175/BIS | ussm.potenza.dgm@giustizia.it | NULL | 97.154.467 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 104 | USSM | REGGIO CALABRIA | CORSO GARIBALDI, 404 | ussm.reggiocalabria.dgm@giustizia.it | NULL | 96.524.500 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 105 | USSM | ROMA | VIA AGNELLI, 15 | ussm.roma.dgm@giustizia.it | NULL | 696.668.011 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 106 | USSM | SALERNO | VIA G. NEGRI, 5 | ussm.salerno.dgm@giustizia.it | NULL | 89.229.478 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 107 | USSM | SASSARI | VIA PREDDA NIEDDA, 6C | ussm.sassari.dgm@giustizia.it | NULL | 792.633.024 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 108 | USSM | TARANTO | VICO S. AGOSTINO, 1 | ussm.taranto.dgm@giustizia.it | NULL | 994.706.054 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 109 | USSM | TORINO | VIA BERRUTI E FERRERO, 1/A | ussm.torino.dgm@giustizia.it | NULL | 116.194.260 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 110 | USSM | TRENTO | VIA MADRUZZO, 13 | ussm.trento.dgm@giustizia.it | NULL | 0461.984261- 982056 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 111 | USSM | TRIESTE | VIA CARDUCCI, 20 | ussm.trieste.dgm@giustizia.it | NULL | 040-635254 040-635003 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 112 | USSM | VENEZIA | VIA BISSA - MESTRE | ussm.venezia.dgm@giustizia.it | NULL | 041.5060836 - 5060889 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |

Tabella 68 – Tabella <CSSA> - USSM

| N | ID_CSSA | TIPO | COMUNE | INDIRIZZO | EMAIL | FAX | TEL | INCARICO | TITOLO | NOME | COGNOME | DATA_CARICAMENTO |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | 113 | USSMSS | ANCONA | VIA CAVORCHIE, 1/E | ussm.ancona.dgm@giustizia.it | NULL | 71.201.004 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 114 | USSMSS | BRINDISI | VIA INDIPENDENZA, 8 | NULL | NULL | 831.521.481 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 115 | USSMSS | CITTANOVA | VIALE MERANO | NULL | NULL | 966.662.406 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 116 | USSMSS | COSENZA | VIA GIOVANNI AMELLINO c/o II Circoscrizione | NULL | NULL | 98.434.861 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 117 | USSMSS | ERICE | Via Giuseppe Clemente,100 ERICE località Casa Santa (TP) | NULL | NULL | 0923 553208 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 118 | USSMSS | FOGGIA | PIAZZA CAVOUR 1 | NULL | NULL | 881.776.031 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 119 | USSMSS | FROSINONE | PIAZZA S. TOMMASO D'AQUINO 25 | NULL | NULL | 775.211.866 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 120 | USSMSS | GELA | CORSO VITTORIO EMANUELE, 168 | NULL | NULL | 933.823.628 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 121 | USSMSS | LA SPEZIA | VIA DON MINZONI 43 | NULL | NULL | 18.722.238 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 122 | USSMSS | LATINA | VIA DON MOROSINI, 2 | NULL | NULL | 773.662.946 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 123 | USSMSS | LIVORNO | Via Caduti del Lavoro,26 | NULL | NULL | 0586 264126 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 124 | USSMSS | LUCCA | VIA DELLE SETTE ARTI 3 | NULL | NULL | 583.464.459 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 125 | USSMSS | MATERA | VIA CAPPELLUTI, 60/62 | NULL | NULL | 835.336.055 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 126 | USSMSS | NUORO | VIALE SARDEGNA 33 B | NULL | NULL | 78.433.580 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 127 | USSMSS | PADOVA | PIAZZA DEI FRUTTI, 38 | NULL | NULL | 498.758.155 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 128 | USSMSS | PATTI | VIA MOLINO CROCE | NULL | NULL | 941.245.289 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 129 | USSMSS | PESCARA | VIA RIGOPIANO, 30/1 | NULL | NULL | 085.2058848 - 085.2058971 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 130 | USSMSS | RAGUSA | VIA NATANELLI, 58 | NULL | NULL | 932.245.520 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 131 | USSMSS | RIMINI | Via Alberto Dalla Chiesa, 11 | NULL | NULL | 0541-763554 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 132 | USSMSS | SIENA | VIA TOMMASO PENDOLA, 37 | NULL | NULL | 577.283.623 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 133 | USSMSS | SIRACUSA | VIA SANTA PANAGIA, 109 | NULL | NULL | 0931.752685 - 0931.752686 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 134 | USSMSS | TERAMO | VIA G. BOVIO 6 | NULL | NULL | 0861/243063 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 135 | USSMSS | TREVISO | VIA D'ANNUNZIO, 28 | NULL | NULL | 422.410.507 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 136 | USSMSS | UDINE | VIA LARGA, 35 | NULL | NULL | 0432.505744-512883 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 137 | USSMSS | VERONA | VIA VALERIO CATULLO, 12 | NULL | NULL | 458.030.177 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |
|  | 138 | USSMSS | VICENZA | PESCHERIE VECCHIE 26 | NULL | NULL | 444.323.265 | NULL | NULL | NULL | NULL | 01/11/2014 0.00.00 |

Tabella 69 – Tabella <CSSA> - USSMSS

L’intervento in oggetto prevede l’inserimento nella tabella <CG_REF_CODES>:

| Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> | Tabella <CG_REF_CODES> |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| N. | RV_DOMAIN | RV_LOW_VALUE | RV_HIGH_VALUE | RV_ABBREVIATION | RV_MEANING | RV_ALT2_VALUE | RV_ALT3_VALUE | RV_ALT4_VALUE | RV_ALT5_VALUE |
|  | TIPO_AUTORITA | 4A | USSM | NULL | Ufficio Servizi Sociali per i Minorenni | NULL | NULL | NULL | NULL |
|  | TIPO_AUTORITA | 4B | SNT | NULL | Sistema Notifiche Telematiche | NULL | NULL | NULL | NULL |
|  | TIPO_UFFICIO | USSM | NULL | NULL | Ufficio Servizi Sociali per i Minorenni | NULL | NULL | NULL | NULL |
|  | TIPO_UFFICIO | USSMSS | NULL | NULL | Ufficio Servizi Sociali per i Minorenni – Sezione di Servizio | NULL | NULL | NULL | NULL |

Tabella 70 - Tabella <CG_REG_CODES>
## Modifica template
Nessuna modifica prevista.