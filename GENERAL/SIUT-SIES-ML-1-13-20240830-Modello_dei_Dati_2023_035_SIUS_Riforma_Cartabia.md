---
uniqueName: siut-sies-ml-1-13-20240830-modellodeidati2023035si
displayName: "SIUT SIES ML 1 13 20240830 Modello dei Dati 2023 035 SIUS Riforma Cartabia"
category: "GENERAL"
tags: []
---

# SIUT-SIES-ML-1.13-20240830-Modello_dei_Dati_2023_035_SIUS_Riforma_Cartabia

> **File originale:** `MEV/SCHEDA_035/ORIGINALI/SIUT-SIES-ML-1.13-20240830-Modello_dei_Dati_2023_035_SIUS_Riforma_Cartabia.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |




Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni

|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Engineering | RTI |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 30/08/2024 |  |
| Livello di riservatezza | L4 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 13/11/2016 | Prima emissione |  |
| 1.1 | 06/03/2017 | Seconda emissione | Introdotte le informazioni sullo schema COLL |
| 1.2 |  | Terza emissione | Modificate/Introdotte le seguenti tabelle:
ISTRUTTORIA_CUMULO	
CIRCOSTANZA_CUMULO	
PROCEDIMENTO_CUMULATO	
STATO_ESEC_TITOLO_CUMULATO	
NOTIFICA_CUMULO	
LIB_ANTICIPATA_CUMULO	
PERIODO_LIB_ANT_CUMULO	
CONTINUAZIONE_CUMULO	
RICHIESTE_INVIATE_CUMULO	
RICHIESTE_PM_IN_CUMULO	
BENEFICIO_CUMULO	
PROVVEDIMENTO_GE_SORV_CUM	
ESITO_ARCHIVIAZIONI_CUMULO	
RICHPM_BENEFICIO _CUM	
RICHPM_MISSICUR_CUM	
RICHPM_PENACC_CUM	
RICHPM_PENACC_CUM	
RICHPM_REATO_CUM	
RICHPM_SANZIONE_SOST_CUM	
RICHPM_STATO_ESEC_CUM	
RICHPM_TITOLO_CUM	
COMPUTI_CUMULO	
POSIZIONE_GIURIDICA_CUMULO	
EVENTO	
COMPETENZA
IMPUGNAZIONE_SIGE
AULA_UDIENZA
FASCICOLO_SIGE
SENTENZA
IMPUGNAZIONE |
| 1.3 |  | Quarta emissione | Modificate/Introdotte le seguenti tabelle:
RICHPM_TITOLO_CUM
COMPUTI_CUMULO
MAGISTRATO_ASSEGNATARIO	
COLLEGIO |
| 1.4 |  | Quinta emissione | Modificate/Introdotte le seguenti tabelle:
ERRORI_TRIGGER
ISP_ATTIVITA_MAGISTRATI_MS
ISP_MOTIVO_ATTIVITA_MS
ISP_PROVVEDIMENTI_MS
ISP_SCARTI_MS
ISP_TEMPI_ISCRIZIONE_MS
ISP_TEMPI_RICEZIONE_MS
ISP_TIPOLOGIA_ATTIVITA_MS
SCADENZARIO_SIEP
SENTENZA
STATO_FASCICOLO_RES_MS |
| 1.5 | 12/03/2021 | Sesta emissione | Introdotte le seguenti tabelle:
ASSOC_UTENTE_SIES_ADN
UTENZA_ADN |
| 1.6 | 24/03/2021 | Settima emissione | Aggiornate le descrizioni COD_TIPO_FUNZIONE della tabella FUNZIONE e COD_TIPO_VISUALIZZAZIONE della tabella RELAZIONE_FUNZIONE |
| 1.7 | 21/05/2021 | Ottava emissione | Aggiornate le descrizioni COGNOME_SOGGETTO e NOME_SOGGETTO della tabella AVVISI_AVVOCATO |
| 1.8 | 24/03/2023 | Nona emissione | Aggiornate le tabelle NOTIFICA e RESIDENZA; aggiunte le tabelle BATCH_PAGOPA, BOLLETTINO_PAGOPA, CIVIL_OBBL_DIFENSORE, CIVILMENTE_OBBLIGATO, RATEIZZAZIONE_PP e UFFICI_PRODUZIONE |
| 1.9 | 10/05/2023 | Decima emissione | Aggiornata la tabella BOLLETTINO_PAGOPA |
| 1.10 | 30/01/2024 | Undicesima emissione | Create le seguenti tabelle:
BOLLETTINO_BATCH_PAGOPA
ERRORI_SIES_PAGOPA
INVOCAZIONE_PAGOPA
Alterate le seguenti tabelle:
BATCH_PAGOPA
RINNOVO |
| 1.11 | 19/04/2024 | Dodicesima emissione | Aggiornata la tabella MISURA_ALTERNATIVA |
| 1.12 | 02/08/2024 | Tredicesima emissione | Creata la tabella:
PRESA_IN_CARICO |
| 1.13 | 31/08/2024 | Quattordicesima emissione | Alterate le tabelle:
DEPOSITO_ORDINANZA_PC
RATEIZZAZIONE_PP |


Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Aurora Garofalo | Amministrazione |  | Responsabile Unico Procedimento |
| Dott. Oris Orlando | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Francesco Rosati | RTI |  | Responsabile Manutenzione Correttiva
Referente Qualità e Sicurezza |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario
Referente Tecnico |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Referente PMO e Qualità |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |


INDICE DEI CONTENUTI
1.	Introduzione	15
1.1	Scopo del documento	15
1.2	Riferimenti	15
1.3	Glossario	15
1.3.1	Definizioni	15
1.3.2	Acronimi e abbreviazioni	15
2.	Disegno DB	16
3.	AGDG_FASCICOLO_SIEP	17
4.	ALIAS	18
5.	ALTRA_CAUSA	20
6.	ALTRI_GRADI_GIUDIZIO	22
7.	ANAGRAFICA_PARTI_UDIENZA	24
8.	ANNMAN_PENACOMPL	25
9.	ANNMAN_REATO	26
10.	ANNOTAZIONE_ESITO_TRASMISSIONE	27
11.	ANNOTAZIONE_MANUALE	28
12.	ARCHIVIAZIONE	32
13.	ASSISTENTE_GIUDIZIARIO	34
14.	ASSISTENTE_SOCIALE	35
15.	ASSISTENTE_SOCIALE_ATTIVITA	36
16.	ASSOC_UTENTE_SIES_ADN	37
17.	ATTIVITA	38
18.	AULA_UDIENZA	39
19.	AUTORITA_ESTERNA	40
20.	AVVISI_AVVOCATO	41
21.	AVVOCATO	42
22.	AVVOCATO_FASCICOLO_SIEP	44
23.	AVVOCATO_FASCICOLO_SIGE	46
24.	AVVOCATO_FASCICOLO_SIUS	48
25.	BATCH_PAGOPA	50
26.	BENEFICIO	51
27.	BENEFICIO_CUMULO	54
28.	BENEFICIO_SENTENZA_SIGE	56
29.	bollettino_batch_pagopa	57
30.	BOLLETTINO_PAGOPA	58
31.	CAMPO_NOTA	60
32.	CANC_ASS_FASC_SIUS	61
33.	CANCELLERIA_ASSEGNATARIA	62
34.	CERTIFICATO_OMONIMI_NSC	63
35.	CERTIFICATO_STATO_ESEC	64
36.	CG_REF_CODES	65
37.	CIRCOSTANZA	67
38.	CIRCOSTANZA_CUMULO	69
39.	CIRCOSTANZA_SENTENZA_SIGE	71
40.	CIVILMENTE_OBBLIGATO	72
41.	CIVIL_OBBL_DIFENSORE	74
42.	CODICI_SIES_NSC	76
43.	CODICI_UNIVOCI_MAPPATI	77
44.	COLLEGIO	78
45.	COLLEGIO_ESPERTO	79
46.	COLLEGIO_GIUDICE_POPOLARE	80
47.	COLLEGIO_MAGISTRATO	81
48.	COMPETENZA	82
49.	COMPUTI_CUMULO	84
50.	COMUNE	87
51.	CONTINUAZIONE	88
52.	CONTINUAZIONE_CUMULO	90
53.	CSSA	91
54.	CUMULO	92
55.	CURATORE	94
56.	CURATORE_SIUS	95
57.	DATI_FINALI_CUMULO	96
58.	DATI_FINALI_ULTERIORI_SANZIONI	97
59.	DATI_PROVVEDIMENTO_SIGE	98
60.	DECRETO_ORDINANZA_SIEP	99
61.	DEPOSITO_DECRETO	101
62.	DEPOSITO_ORDINANZA_PC	103
63.	DEPOSITO_SENTENZA	106
64.	DETTAGLIO_PROVVEDIMENTO	108
65.	DOCUMENTO_ALLEGATO	109
66.	errori_sies_pagopa	111
67.	ERRORI_TRIGGER	112
68.	ESECUZIONE_MISURA_ALTERNATIVA	113
69.	ESECUZIONE_MISURA_SICUREZZA	115
70.	ESECUZIONE_SANZIONE_SOST	116
71.	ESITO_ARCHIVIAZIONI_CUMULO	118
72.	ESPERTO	119
73.	ESPERTO_ATTIVITA	120
74.	EVENTO	121
75.	EVENTO_PERMESSO_LICENZA	125
76.	FASCICOLO_SIEP	126
77.	FASCICOLO_SIEP_BDMC	130
78.	FASCICOLO_SIEPE	131
79.	FASCICOLO_SIGE	133
80.	FASCICOLO_SIUS	135
81.	FASC_MS_TO_FASC_SIEP	137
82.	FAS_SIGE_DETENZIONE	138
83.	FAS_SIGE_SENTENZA	139
84.	FUNGIBILITA	140
85.	FUNZIONE	141
86.	FUNZIONE_PROFILO	142
87.	FUNZIONI_TESTATE	143
88.	GENERALE_PROCEDIMENTO	144
89.	GIUDICE_POPOLARE	146
90.	HELPONLINE	147
91.	IMPUGNAZIONE	148
92.	IMPUGNAZIONE_SIGE	150
93.	INCARICO_ATTIVITA	151
94.	invocazione_pagopa	152
95.	ISP_ESITO_PROVVEDIMENTO	153
96.	isp_motivo_attivita	154
97.	ISP_MOTIVO_ATTIVITA_MS	155
98.	ISP_OGGETTO_PROCEDIMENTO	156
99.	ISP_POSIZIONE_GIURIDICA	157
100.	ISP_STAT_RIS_SIES	158
101.	ISP_TEMPI_RICEZIONE_MS	159
102.	ISP_TIPOLOGIA_ATTIVITA	160
103.	ISP_TIPOLOGIA_ATTIVITA_MS	161
104.	ISTANZA	162
105.	ISTITUTO_DETENZIONE	164
106.	ISTRUTTORIA_CUMULO	165
107.	JMS_CODE	166
108.	LIB_ANTICIPATA_CUMULO	167
109.	LICENZA_LIBANTICIPATA	168
110.	LOG_ATTIVITA	170
111.	LOG_TRASFERIMENTO_ESECUZIONE	171
112.	LUOGO_DETENZIONE	172
113.	MAGISTRATO	173
114.	MAGISTRATO_ASSEGNATARIO	174
115.	MAGISTRATO_COMPETENTE	175
116.	MAGISTRATO_RELATORE	176
117.	MAGISTRATO_SEZIONE	177
118.	MAX_STATO_PROCEDIMENTO	178
119.	MESSAGGIO	179
120.	MISURA_ALTERNATIVA	181
121.	MISURA_CAUTELARE	184
122.	MISURA_CAUTELARE_BDMC	186
123.	MISURA_CAUTELARE_CUMULO	189
124.	MISURA_SICUREZZA	190
125.	MISURA_SICUREZZA_CUMULO	192
126.	MISURA_SICUREZZA_SENTENZA_SIGE	194
127.	MOTIVAZIONE_DECRETO	195
128.	MOTIVAZIONE_PROVVED_SIGE	196
129.	MOTIVO_EVENTO	197
130.	MOVIMENTO_REG_ESECUZIONE	198
131.	NOME_PROVVEDIMENTO	200
132.	NOTE	201
133.	NOTE_FASCICOLO	202
134.	NOTIFICA	203
135.	NOTIFICA_CUMULO	205
136.	NOTIFICHE_SIES	206
137.	NOTIZIA_REATO	207
138.	NUOVA_ISTANZA	208
139.	PARAMETRO	209
140.	PARTI_UDIENZA_DIFENSORE	210
141.	PENA_ACCESSORIA	212
142.	PENA_ACCESSORIA_CUMULO	215
143.	PENA_ACCESSORIA_SENTENZA_SIGE	216
144.	PENA_COMPLESSIVA	217
145.	PENA_COMPLESSIVA_CUMULO	219
146.	PENA_COMPLESSIVA_SENTENZA_SIGE	220
147.	PENA_CUMULO	221
148.	PENA_PECUNIARIA	223
149.	PENA_PRESUNTA	224
150.	PENA_RESIDUA	225
151.	PENA_RIDETERMINATA_CUMULO	227
152.	PERIODO_ALTRA_MISURA	228
153.	PERIODO_ALTRA_SANZIONE	230
154.	PERIODO_LIB_ANT_CUMULO	232
155.	PERIODO_LIBANTICIPATA	233
156.	POSIZIONE_GIURIDICA	234
157.	POSIZIONE_GIURIDICA_CUMULO	236
158.	POSIZIONE_MATERIALE	237
159.	POSIZIONE_MATERIALE_FASC	238
160.	POSIZIONE_MATERIALE_FASC_SIGE	239
161.	POSIZIONE_MATERIALE_FASC_SIUS	240
162.	PRESA_IN_CARICO	241
163.	PRESCRIZIONE	242
164.	PROCEDIMENTO_CUMULATO	244
165.	PROFILO	245
166.	PROFILO_TIPOUFFICIO	246
167.	PROVVEDIMENTO_GE_SORV_CUM	247
168.	PROVVEDIMENTO_SIGE	249
169.	RATEIZZAZIONE_PP	251
170.	REATO	252
171.	REATO_CUMULATO	255
172.	REATO_PREDISPOSTO	257
173.	REATO_SENTENZA_SIGE	258
174.	REFERTO_SCARCERAZIONE	259
175.	RELAZIONE	260
176.	RELAZIONE_FUNZIONE	261
177.	REMOTE_LOGIN	262
178.	RESIDENZA	263
179.	RESIDENZA_FASCICOLO_SIEP	265
180.	RESIDENZA_FASCICOLO_SIGE	266
181.	RESIDENZA_FASCICOLO_SIUS	267
182.	RIAPERTURA_FASCICOLO_SIEP	268
183.	RICHIESTA	269
184.	RICHIESTA_CONVERSIONE	270
185.	RICHIESTA_REMISSIONE	272
186.	RICHIESTA_SIGE	273
187.	RICHIESTE_INVIATE_CUM	274
188.	RICHIESTE_PM_IN_CUMULO	275
189.	RICHPM_BENEFICIO_CUM	277
190.	RICHPM_MISSICUR_CUM	278
191.	RICHPM_PENACC_CUM	279
192.	RICHPM_REATO_CUM	280
193.	RICHPM_SANZIONE_SOST_CUM	281
194.	RICHPM_STATO_ESEC_CUM	282
195.	RICHPM_TITOLO_CUM	283
196.	RIEPILOGO_PROVVEDIMENTO	284
197.	RIFERIMENTO_FASCICOLO_SIEP	286
198.	RIFERIMENTO_FASCICOLO_SIUS	287
199.	RINNOVO	288
200.	RINVIO_PROVVEDIMENTO	289
201.	RISULTATO_RICERCA	290
202.	SANZIONE_AMMINISTRATIVA	291
203.	SANZIONE_SOST_CUM	292
204.	SANZIONE_SOSTITUTIVA	293
205.	SANZIONE_SOST_RESIDUA	294
206.	SCADENZARIO_SIEP	295
207.	SCADENZARIO_SIGE	297
208.	SCADENZARIO_SIUS	298
209.	SCAMBIO_SANZIONE	299
210.	SEDE_GIUDIZIARIA	301
211.	SENTENZA	302
212.	SENTENZA_RIUNITA	305
213.	SENTENZARIUNITA_FASC_SIEP	307
214.	SEZIONE	308
215.	SOGGETTO	309
216.	SOGGETTO_CERTIFICATO	312
217.	SOGGETTO_CUMULATO	313
218.	SOGGETTO_DATTILO	314
219.	SOLLECITO_ESITO_TRASMISSIONE	315
220.	SOSPENSIONE	316
221.	STAMPA_DOCUMENTI	318
222.	STATO_ESEC_TITOLO_CUMULATO	319
223.	STATO_ESECUZIONE_PROCEDIMENTO	321
224.	STATO_FASCICOLO_RES	322
225.	STATO_FASCICOLO_RES_MS	323
226.	STATO_PRENOTAZIONI_BDMC	324
227.	STATO_PROCEDIMENTO	325
228.	STORICO_AVVOCATO	326
229.	STORICO_SOGGETTO	328
230.	TEMPLATE	330
231.	TENORE	331
232.	TENORE_SENTENZA_REATO	333
233.	TENORE_SIGE	334
234.	TIPO_EVENTI_BDMC	336
235.	TIPOLOGIA_ORARIO	337
236.	TITOLO_CUMULATO	338
237.	TRASMISSIONI	340
238.	UDIENZA	341
239.	UDIENZA_PARTI	343
240.	UDIENZA_PROCEDIMENTO	344
241.	UDIENZA_PROCEDIMENTO_SIGE	345
242.	UDIENZA_SIGE	346
243.	UFFICIO	347
244.	UFFICIO_ACCORPATO	349
245.	UFFICIO_DESCR	350
246.	UFFICI_PRODUZIONE	351
247.	ULTERIORE_ISTANZA	352
248.	ULTERIORE_ISTANZA_TENORE	353
249.	ULTERIORE_SANZIONE_CUMULO	354
250.	UTENTE	355
251.	UTENTE_PROFILO	356
252.	UTENTE_UFFICIO	357
253.	UTENZA_ADN	358
254.	VERBALE	359
255.	VERSIONE	361
256.	COLLA.COLLABORATORE	362
257.	STATIS.ISP_ATTIVITA_MAGISTRATI_MS	363
258.	STATIS.ISP_PROVVEDIMENTI_MS	364
259.	STATIS.ISP_SCARTI_MS	365
260.	STATIS.ISP_TEMPI_ISCRIZIONE_MS	366
261.	Viste utilizzate dallo schema SIESXX	367

# Introduzione
## Scopo del documento
Il presente documento descrive la banca dati del sistema SIES relativamente allo schema SIESXX. Si sottolinea che la tabella “COLLABORATORE” dello schema “COLLA” è presente solo nel distretto di ROMA.
Si fa presente che le tutte tabelle “tipologiche” sono aggiornabili solo tramite script eseguibili direttamente sulla banca dati.
## Riferimenti
| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
|  |  |  |

## Glossario
## Definizioni
| Definizione | Descrizione |
| --- | --- |
|  |  |

## Acronimi e abbreviazioni
| Sigla | Descrizione |
| --- | --- |
| DB | Data Base |
| DEC | Direttore Esecutivo Contratto |
| DGSIA | Direzione Generale per i Sistemi Informativi Automatizzati |
| FP | Function Point |
| GdL | Gruppo di Lavoro |
| HW | HardWare |
| MAC | MAnutenzione Correttiva |
| MEV | Manutenzione EVolutiva |
| PA | Pubblica Amministrazione |
| PEC | Posta Elettronica Certificata |
| RTI | Raggruppamento Temporaneo di Impresa |
| RUF | Responsabile Unico Fornitore |
| RUP | Responsabile Unico Progetto |
| SW | SoftWare |


# Disegno DB
Si riporta di seguito il disegno delle principali tabelle dello schema SIESXX:








# AGDG_FASCICOLO_SIEP
La tabella è un’associativa tra la tabella altri_gradi_giudizio e fascicolo_siep. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_AGDG_FASCICOLO_SIEP | NUMBER NOT NULL | Chiave della Tabella di Relazione |
| AGDG_ID_ALTRIGRADIGIUDIZIO | NUMBER NOT NULL | ID AGDG_FASCICOLO_SIEP |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL. | ID Fascicolo SIEP |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| AGDG_FAS_SIE_AGDG_FK | AGDG_ID_ALTRIGRADIGIUDIZIO | (ALTRI_GRADI_GIUDIZIO.ID_ALTRIGRADIGIUDIZIO) |
| AGDG_FAS_SIE_FAS_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |

# ALIAS
La tabella identifica gli alias di un soggetto. La tabella è utilizzata dai sottosistemi SIEP-SIUP-SIGE

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ALIAS | NUMBER NOT NULL | Progressivo nell'ambito del singolo soggetto. Insieme al codice_soggetto (entità soggetto) identifica tutti gli alias del soggetto. |
| COGNOME | VARCHAR2 (100 CHAR) | Cognome Alias. Potrebbe non coincidere con il Cognome del Soggetto. |
| NOME | VARCHAR2 (100 CHAR) | Nome Alias. Potrebbe non coincidere con il Nome del Soggetto. |
| PATERNITA | VARCHAR2 (35 CHAR) | Descrizione del nome del padre se presente. |
| COD_FISCALE | VARCHAR2 (16 CHAR) | Eventuale Codice fiscale. |
| COD_CS | VARCHAR2 (18 CHAR) | Codice relativo all’acquisizione delle impronte digitali. Codice univoco identificativo (codice attribuito dal casellario centrale di Identità del Ministero degli Interni mediante l'acquisizione delle impronte digitali) o Il dato deve essere reso obbligatorio per gli stranieri o E' previsto in RE.GE: standard non ancora codificato. |
| COD_AFIS | VARCHAR2 (18 CHAR) | Codice relativo all’acquisizione delle impronte digitali. Codice univoco identificativo (codice attribuito dal casellario centrale di Identità del Ministero degli Interni. |
| ATTO_NASCITA | VARCHAR2 (240 CHAR) | Estratto dell'atto di nascita. |
| SESSO | VARCHAR2 (1 CHAR) | Indicazione del sesso del soggetto. Deriva da dominio e vale: M = Maschio
F = Femmina |
| COD_COMUNE_NASCITA | VARCHAR2 (6 CHAR) | Fa riferimento alla tabella di dominio COMUNE. |
| COD_PROVINCIA_NASCITA | VARCHAR2 (2 CHAR) | Codice di due lettere indicante la provincia. |
| COD_STATO_NASCITA | VARCHAR2 (3 CHAR) | Codice dello stato di nascita. |
| DATA_NASCITA | DATE | Data di nascita del soggetto. |
| NOTE | VARCHAR2 (2000) | Eventuali note aggiuntive. |
| DESC_COMUNE_NASCITA_ESTERO | VARCHAR2 (200 CHAR) | Attributo relativo alle informazioni del comune di nascita di un soggetto nato all'estero. E' un campo a testo libero. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| SOG_ID_SOGGETTO | NUMBER NOT NULL | ID Soggetto collegato. |
| PROG_ANAG_ALIAS_RES | NUMBER | Progressivo dell’anagrafica RES |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| ALI_SOG_FK | SOG_ID_SOGGETTO | (SOGGETTO.ID_SOGGETTO) |

# ALTRA_CAUSA
La tabella indica i dati riferiti alla sentenza per altra_causa. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ALTRA_CAUSA | NUMBER NOT NULL | Chiave numerica naturale dell'entità. |
| ANNO | NUMBER | Anno sentenza altra causa. |
| NUMERO | VARCHAR2 (6 CHAR) | Numero sentenza altra causa. |
| DATA | DATE | Data sentenza altra causa. |
| COD_LUOGO | VARCHAR2 (6 CHAR) | Codice del luogo dove è stata emessa sentenza. Il campo serve per determinare correttamente l'ufficio emittente della sentenza. |
| COD_AUTORITA | VARCHAR2 (6 CHAR) | Codice dell'autorità che ha emesso la sentenza. Il campo serve per determinare correttamente l'ufficio emittente della sentenza. |
| DATA_DECORRENZA | DATE | Data di decorrenza della sentenza. |
| DATA_SCADENZA | DATE | Data scadenza della pena o misura relativa alla causa. |
| COD_TIPO_POS_GIURIDICA | VARCHAR2 (2 CHAR) | Codice della posizione giuridica. |
| ALTRO_LUOGO | VARCHAR2 (2000 CHAR) | Eventuale altro luogo di trascorrimento del periodo di pena. Ad esempio nel caso di arresti domiciliari potrebbe indicare l'indirizzo del soggetto presso il quale sta trascorrendo il periodo di arresti domiciliari indicato dalla misura alternativa. |
| NOTE | VARCHAR2 (2000 CHAR) | Eventuali note aggiuntive. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL | ID Fascicolo SIEP collegato. |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2 (4 CHAR) | ID Istituto detenzione collegato. |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| ALT_CAU_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |

Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| FAS_SIGE_DETENZIONE | FAS_SIGE_DETEN_ALTRA_FK | AC_ID_ALTRA_CAUSA |
| POSIZIONE_GIURIDICA | POS_GIU_ALT_CAU_FK | ALT_CAU_ID_ALTRA_CAUSA |


# ALTRI_GRADI_GIUDIZIO
La tabella indica i dati riferiti agli altri gradi di giudizio di una sentenza. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ALTRIGRADIGIUDIZIO | NUMBER NOT NULL | Chiave numerica naturale dell'entità. |
| DATA_SENTENZA_I_GRADO | DATE | Data della sentenza di primo grado |
| ANNO_SENTENZA_I_GRADO | NUMBER | Anno della sentenza di primo grado |
| NUMERO_SENTENZA_I_GRADO | VARCHAR2 (8 CHAR) | Numero della sentenza di primo grado |
| COD_AUT_EMITT_SENT_I_GRADO | VARCHAR2 (6 CHAR) | Autorità che ha emesso la sentenza di primo grado |
| COD_LUO_EMITT_SENT_I_GRADO | VARCHAR2 (6 CHAR) | Luogo di emissione della sentenza di primo grado |
| NUM_SEZ_EMITT_SENT_I_GRADO | VARCHAR2 (100 CHAR) | Numero della sezione della sentenza di primo grado |
| COD_TIPO_SENTENZA_II_GRADO | VARCHAR2 (2 CHAR) | Tipo della sentenza di secondo grado |
| DATA_SENTENZA_II_GRADO | DATE | Data della sentenza di secondo grado |
| ANNO_SENTENZA_II_GRADO | NUMBER | Anno della sentenza di secondo grado |
| NUMERO_SENTENZA_II_GRADO | VARCHAR2 (8 CHAR) | Numero della sentenza di secondo grado |
| COD_AUT_EMITT_SENT_II_GRADO | VARCHAR2 (6 CHAR) | Autorità che ha emesso la sentenza di secondo grado |
| COD_LUO_EMITT_SENT_II_GRADO | VARCHAR2 (6 CHAR) | Luogo di emissione della sentenza di secondo grado |
| NUM_SEZ_EMITT_SENT_II_GRADO | VARCHAR2 (100 CHAR) | Numero della sezione della sentenza di secondo grado |
| ANNO_REG_GEN_CASSAZ | NUMBER | Anno del registro generale della Cassazione |
| NUMERO_REG_GEN_CASSAZ | VARCHAR2 (10 CHAR) | Numero del registro generale della Cassazione |
| ANNO_SENTENZA_CASSAZ | NUMBER | Anno sentenza cassazione |
| NUMERO_SENTENZA_CASSAZ | VARCHAR2 (8 CHAR) | Numero sentenza cassazione |
| ANNO_RACC_GENEALE_II_GRADO | NUMBER | Anno raccordo di secondo grado |
| NUMERO_RACC_GENEALE_II_GRADO | VARCHAR2 (8 CHAR) | Numero raccordo di secondo grado |
| COD_TIPO_DECISIONE_CASSAZIO NE | VARCHAR2 (2 CHAR) | Tipo delle decisione di secondo grado |
| SEN_ID_SENTENZA | NUMBER NOT NULL | Identificativo della sentenza |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| COD_TIPO_RITO | VARCHAR2 (1 CHAR) | Tipo del rito |

Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| AGDG_SEN_FK | SEN_ID_SENTENZA | (SENTENZA.ID_SENTENZA) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| AGDG_FASCICOLO_SIEP | AGDG_FAS_SIE_AGDG_FK | AGDG_ID_ALTRIGRADIGIUDIZIO |

# ANAGRAFICA_PARTI_UDIENZA
La tabella indica i dati riferiti ai dati anagrafici delle parti in una udienza. utilizzata dal sistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SOGGETTO | NUMBER(38) not null | PK Soggetto |
| COD_TIPO_PART | VARCHAR2(1) not null | Civile o fisica |
| COD_PARTE | VARCHAR2(1) not null | Codice della parte |
| COD_FISCALE | VARCHAR2(16) | Codice fiscale della parte |
| COGNOME | VARCHAR2(100) | Cognome della parte |
| NOME | VARCHAR2(100) | Nome della parte |
| DENOMINAZIONE | VARCHAR2(200) | Denominazione della parte |
| DATA_NASCITA | DATE | Data di nascita della parte |
| COD_COMUNE_NASCITA | VARCHAR2(6) | Comune di nascita della parte |
| COD_PROVINCIA_NASCITA | VARCHAR2(2) | Provincia di nascita della parte |
| COD_STATO_NASCITA | VARCHAR2(3) | Stato di nascita della parte |
| DESC_COMUNE_NASCITA_ESTERO | VARCHAR2(200) | Comune estero di nascita della parte |
| SESSO | VARCHAR2(1) | Sesso della parte |
| RAG_SOCIALE | VARCHAR2(5) | Ragione sociale della parte |
| COD_PROVINCIA | VARCHAR2(2) | Provincia di nascita della parte |
| IND_SEDE_LEGALE | VARCHAR2(200) | Indirizzo della sede legale della parte |
| IND_SEDE_OPERATIVA | VARCHAR2(200) | Indirizzo della sede operativa della parte |
| FLG_CONV_UDIENZA | VARCHAR2(1) | Flag udienza |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Utenza dell’operatore che ha effettuato l’inserimento |
| DATA_INSERIMENTO | DATE | Data inserimento |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11) | ufficio dell’operatore che ha effettuato l’inserimento |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100) | Utenza dell’operatore che ha effettuato l’aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data dell’aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(11) | Ufficio dell’operatore che ha effettuato l’aggiornamento |
| COD_FISCALE_RAP | VARCHAR2(16) | Codice fiscale del rappresentante |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| PARTI_UDIENZA_DIFENSORE | ID_PARTE_UDEINZA_FK | SOGG_ID_SOGGETTO |
| UDIENZA_PARTI | ID_SOGGETTO_FK | ID_SOGGETTO |

# ANNMAN_PENACOMPL
La tabella è una associativa tra la tabella Annotazione Manuale e la Pena Complessiva. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ANNMAN_PENACOMPL | NUMBER NOT NULL | Chiave numerica della tabella di relazione. |
| ANNOTAZIONEMANUALE_ID | NUMBER | ID Annotazione Manuale Collegata. |
| PENACOMPLESSIVA_ID | NUMBER | ID Pena Complessiva. |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| ANMA_ANNMAN_FK | ANNOTAZIONEMANUALE_ID | (ANNOTAZIONE_MANUALE.ID_ANNOTAZIONE_MANUALE) |
| ANMA_PENACOMPL_FK | PENACOMPLESSIVA_ID | (PENA_COMPLESSIVA.ID_PENA_COMPLESSIVA) |



# ANNMAN_REATO
La tabella è una associativa tra la tabella Annotazione Manuale e il Reato. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ANNMAN_REATO | NUMBER NOT NULL | Chiave primaria numerica. |
| ANNOTAZIONEMANUALE_ID | NUMBER | ID Annotazione Manuale Collegata. |
| REATO_ID | NUMBER | ID Reato collegato. |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| ANMA_ANNMAN_R_FK | ANNOTAZIONEMANUALE_ID | (ANNOTAZIONE_MANUALE.ID_ANNOTAZIONE_MANUALE) |
| ANMA_REATO_FK | REATO_ID | (REATO.ID_REATO) |




# ANNOTAZIONE_ESITO_TRASMISSIONE
La tabella contiene gli esiti delle trasmissioni avvenute tra i distretti. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ESITO_TRASMISSIONE | NUMBER not null | Chiave primaria della tabelle |
| DATA_TRASMISSIONE | DATE | Data della trasmissione |
| OGGETTO_TRASMISSIONE | VARCHAR2(5 CHAR) | Oggetto della trasmissione |
| COD_UFFICIO_DESTINATARIO | VARCHAR2(11 CHAR) | Ufficio destinatario della trasmissione |
| COD_UFFICIO_INOLTRANTE | VARCHAR2(11 CHAR) | Ufficio mittente |
| COD_UFFICIO_INOLTRO | VARCHAR2(11 CHAR) | Ufficio a cui si inoltra la trasmissione |
| COD_UFFICIO_ESITO | VARCHAR2(11 CHAR) not null | Ufficio dell’esito |
| DATA_ESITO | DATE not null | Data Esito |
| COD_ESITO | VARCHAR2(35 CHAR) not null | Codice dell’esito |
| NOTE_ESITO | VARCHAR2(2000 CHAR) | Note |
| CHIAVE_ANNO | NUMBER(4) | Anno del procedimento inviato |
| CHIAVE_PROGR | NUMBER(38) | Numero del procedimento inviato |
| CHIAVE_UFFICIO | VARCHAR2(11 CHAR) | Ufficio del procedimento inviato |
| EVE_ID_EVENTO | NUMBER(38) not null | Evento trasmesso |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER(38) not null | Identificativo del fascicolo SIEP |
| MES_ID_MESSAGGIO_RICHIESTA | NUMBER(38) | Identificativo del messaggio della richiesta |
| MES_ID_MESSAGGIO_ESITO | NUMBER(38) | Identificativo del messaggio dell’esito |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100 CHAR) | Identificativo dell’operatore che ha effettuato la trasmissione |
| DATA_INSERIMENTO | DATE | Data della trasmissione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11 CHAR) | Ufficio che ha effettato la trasmissione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_AGGIORNAMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(11 CHAR) | Ufficio dell’operatore che ha inserito il record |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| ANN_ESITO_TRASMISS_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| ANN_ESITO_TRASMISS_FASSIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


# ANNOTAZIONE_MANUALE
La tabella contiene i dati relativi alle annotazioni manuali effettuati su un provvedimento. Utilizzata dai sottosistemi SIEP e SIGE.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ANNOTAZIONE_MANUALE | NUMBER NOT NULL | Chiave primaria numerica. |
| COD_TIPO_ANNOTAZIONE | VARCHAR2 (3 CHAR) | Definisce il tipo di annotazione che si sta trattando. Associato al Dominio TIPO_ANNOTAZIONE della Tabella CG_REF_CODES. |
| FLAG_PIU_MENO | VARCHAR2 (1 CHAR) | Indica se i valori riportati devono essere sommati o detratti dal calcolo della pena. |
| NUM_ANNI_RECLUSIONE | NUMBER | Quantità di anni per la reclusione. |
| NUM_MESI_RECLUSIONE | NUMBER | Quantità di mesi per la reclusione. |
| NUM_GIORNI_RECLUSIONE | NUMBER | Quantità di giorni per la reclusione. |
| DATA_RECLUSIONE_DA | DATE | Data dalla quale parte la reclusione. |
| DATA_RECLUSIONE_A | DATE | Data alla quale finisce la reclusione. |
| IMPORTO_MULTA | NUMBER (2.11) | Importo della eventuale multa presente. Espresso in Euro. |
| NUM_ANNI_ARRESTO | NUMBER | Quantità di anni per l'arresto. |
| NUM_MESI_ARRESTO | NUMBER | Quantità di mesi per l'arresto. |
| NUM_GIORNI_ARRESTO | NUMBER | Quantità di mesi per l'arresto. |
| DATA_ARRESTO_DA | DATE | Data dalla quale parte l'arresto. |
| DATA_ARRESTO_A | DATE | Data alla quale arriva l'arresto. |
| IMPORTO_AMMENDA | NUMBER (2.11) | Importo della eventuale ammenda presente. Espresso in Euro. |
| DATA_RICEZIONE_DOC | DATE | Data di ricezione del verbale di arresto. |
| MOTIVAZIONI | VARCHAR2 (2000 CHAR) | Eventuali note aggiuntive per la descrizione dell'arresto. |
| NOTE_RECLUSIONE | VARCHAR2 (2000 CHAR) | Eventuali note aggiuntive per la descrizione della reclusione. |
| ANNO_GE | NUMBER | Parte della chiave dell'ordinanza del Giudice di esecuzione. |
| NUMERO_GE | VARCHAR2 (6 CHAR) | Parte della chiave dell'ordinanza del Giudice di esecuzione. |
| ANNO_REGE | NUMBER | Parte della chiave della sentenza scritta su RE.GE. |
| NUMERO_REGE | VARCHAR2 (6 CHAR) | Parte della chiave della sentenza scritta su RE.GE. |
| ANNO_MC | NUMBER | Parte della chiave dell'ordinanza relativa alle Misure Cautelari. |
| NUMERO_MC | VARCHAR2 (6 CHAR) | Parte della chiave dell'ordinanza relativa alle Misure Cautelari. |
| ANNO_CDA | NUMBER | Parte della chiave della sentenza della Corte di Appello. |
| NUMERO_CDA | VARCHAR2 (6 CHAR) | Parte della chiave della sentenza della Corte di Appello. |
| ANNO_CC | NUMBER | Parte della chiave della sentenza della Corte di Cassazione. |
| NUMERO_CC | VARCHAR2 (6 CHAR) | Parte della chiave della sentenza della Corte di Cassazione. |
| ANNO_SIEP | NUMBER | Parte della chiave componente il codice del fascicolo SIEP di riferimento. |
| NUMERO_SIEP | VARCHAR2 (9 CHAR) | Parte della chiave componente il codice del fascicolo SIEP di riferimento. |
| COD_TIPO_UFFICIO_SIEP | VARCHAR2 (6 CHAR) | Identificativo della tipologia di ufficio relativo all'ufficio componente la chiave del fascicolo SIEP Associato al Domino TIPO_UFFICIO della Tabella CG_REF_CODES. |
| COD_LUOGO_UFFICIO_SIEP | VARCHAR2 (6 CHAR) | Identificativo del comune dell'ufficio relativo all'ufficio componente la chiave del fascicolo SIEP. |
| DATA_ISCRIZIONE_SIEP | DATE | Data di iscrizione del fascicolo la cui chiave è indicata nei campi precedenti. |
| COD_FONTE | VARCHAR2 (5 CHAR) | FONTE GIURIDICA è il tipo di fonte giuridica relativo agli articoli di reato; es.: codice penale legge. Associato al Dominio FONTE della Tabella CG_REF_CODES. |
| ANNO_FONTE | NUMBER | Anno della norma. |
| NUMERO_FONTE | VARCHAR2 (6 CHAR) | Numero della norma |
| COD_SOTTONUMERAZIONE | VARCHAR2 (2 CHAR) | Sottonumerazione articolo (bis ter ecc.) Associato al Dominio SOTTONUMERAZIONE della Tabella CG_REF_CODES. |
| COMMA | VARCHAR2 (10 CHAR) | Comma dell'articolo trattato. |
| LETTERA | VARCHAR2 (2 CHAR) | Lettera dell'articolo trattato. |
| NUMERO | VARCHAR2 (2 CHAR) | Eventuale numero dell'articolo trattato. |
| ARTICOLO | VARCHAR2 (50 CHAR) | Determina il tipo di fatto di cui si fa carico al condannato in base alla classificazione di legge (articolo comma ed altro eventuale). |
| COD_CAUSALE_COMPUTO | VARCHAR2 (3 CHAR) | CAUSALE per il COMPUTO della pena. Associato al Dominio CAUSALE_COMPUTO della Tabella CG_REF_CODES. |
| COD_DPR | VARCHAR2 (2 CHAR) | Numero del Decreto del Presidente della Repubblica riferito allo specifico beneficio concesso e descritto nell'annotazione manuale. |
| FLAG_VALIDATO | VARCHAR2 (1 CHAR) | Validazione occorrenza trattata. Associato al Dominio FLAG_SI_NO di CG_REF_CODES. |
| FLAG_CONFORME | VARCHAR2 (1 CHAR) | A fronte di una applicazione provvisoria posso avere una ordinanza del GE che rifacendo i conti applica in modo difforme (se non concorda con i dati del PM di esecuzione) l'annotazione manuale. Associato al Dominio FLAG_SI_NO di CG_REF_CODES. |
| FLAG_APP_PROVVISORIA | VARCHAR2 (1 CHAR) | Indica l'eventuale applicazione provvisoria della annotazione manuale detta "anticipazione degli effetti". Associato al Dominio FLAG_SI_NO di CG_REF_CODES. |
| PEN_RES_ID_PENA_RESIDUA | NUMBER | Link alla pena residua |
| FUN_ID_FUNGIBILITA | NUMBER | Link alla pena fungibile |
| DATA_RICHIESTA | DATE | Data di richiesta applicazione beneficio al Giudice dell'Esecuzione. |
| DATA_GE | DATE | Data dell'Ordinanza del Giudice dell'Esecuzione. |
| DATA_CC | DATE | Data Sentenza CC per la richiesta al Giudice dell'Esecuzione. |
| ANNO_SENTENZA_SIAP | NUMBER | Anno sentenza Siep di riferimento. |
| NUMERO_SENTENZA_SIAP | VARCHAR2 (6 CHAR) | Numero sentenza Siep di riferimento. |
| DATA_SENTENZA_SIAP | DATE | Data sentenza Siep di riferimento. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| REA_ID_REATO | NUMBER | Identificativo del reato |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| ANNO_ID_ANNOTAZIONE_MANUALE | NUMBER | Anno dell’annotazione manuale |
| FLAG_COMPUTABILE | VARCHAR2 (1 CHAR). | Flag computabilità |
| SEN_ID_SENTENZA | NUMBER(38) | Identificativo titolo esecutivo collegato |
| TEN_ID_TENORE_SIGE | NUMBER(38) | Identificativo tenore sige collegato |
| FLAG_SEL_QUANTUM | VARCHAR2(1) | Flag relativo alla selezione quantum nella decisione |
| ANNO_SIGE | NUMBER(4) | Anno SIGE |
| NUMERO_SIGE | NUMBER(38) | Numero SIGE |
| FLG_BENEFICIO_DETRATTO | VARCHAR2(1) | Se impostato a S indica che non bisogna eseguire il calcolo della pena |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| ANN_MAN_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |
| ANN_MAN_REA_FK | REA_ID_REATO | (REATO.ID_REATO) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| ANNMAN_PENACOMPL | ANMA_ANNMAN_FK | ANNOTAZIONEMANUALE_ID |
| ANNMAN_REATO | ANMA_ANNMAN_R_FK | ANNOTAZIONEMANUALE_ID |
| EVENTO | EVE_ANN_MAN_FK | ANN_ID_ANNOTAZIONE_MANUALE |


# ARCHIVIAZIONE
La tabella contiene i dati relativi all’archiviazione di una sentenza. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ARCHIVIAZIONE | NUMBER NOT NULL | Chiave primaria numerica. |
| COD_TIPO_PROVVEDIMENTO | VARCHAR2 (2 CHAR) DEFAULT '-' | Codifica Tipo provvedimento. Collegato al dominio TIPO_PROVVEDIMENTO di CG_REF_CODES. |
| DATA_EMISSIONE | DATE | Data Emissione |
| DATA_RICEZIONE | DATE | Data Ricezione |
| ANNO_NOTA | NUMBER | Anno della nota |
| NUM_NOTA | VARCHAR2 (35 CHAR) | Numero della nota |
| COD_PROVVEDIMENTO | VARCHAR2 (4 CHAR)DEFAULT '-' | Codice del provvedimento |
| ANNO_PROVVEDIMENTO | NUMBER | Anno del provvedimento |
| NUM_PROVVEDIMENTO | VARCHAR2 (9 CHAR) | Numero del provvedimento |
| COD_TIPO_PROVVEDIMENTO_ARC | VARCHAR2 (2 CHAR) DEFAULT '-' | Tipo del provvedimento archiviato |
| DATA_DEFINIZIONE | DATE | Data di definizione |
| COD_OGGETTO_DEFINIZIONE | VARCHAR2 (4 CHAR) DEFAULT '-' | Oggetto della definizione |
| COD_TIPO_EMITTENTE | VARCHAR2 (2 CHAR)
DEFAULT '-' | Tipo emittente |
| COD_TIPO_AUTORITA_EMITTENTE | VARCHAR2 (6 CHAR) DEFAULT '-' | Autorità emittente |
| COD_LUOGO_EMITTENTE | VARCHAR2 (6 CHAR) DEFAULT '-' | Luogo dell’autorità emittente |
| INDIRIZZO_EMITTENTE | VARCHAR2 (100 CHAR) | Indirizzo emittente |
| ALTRA_AUTORITA | VARCHAR2 (200 CHAR) | Altra autorità emittente |
| NOTE | VARCHAR2 (2000 CHAR) | Note |
| FLAG_ANNULLAMENTO | VARCHAR2 (1 CHAR) DEFAULT 'N' | S/N |
| DATA_ANNULLAMENTO | DATE | Data di annullamento |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2 (4 CHAR) | Identificativo dell’istituto di destinazione |
| CSS_ID_CSSA. | NUMBER | Identificativo del CSSA |
| CHIAVE_ANNO | NUMBER(4) | Anno del procedimento archiviato |
| CHIAVE_PROGR | NUMBER(38) | Numero del procedimento archiviato |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100) | Operatore che ha effettuato l’aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(11) | Ufficio che ha effettuato l’aggiornamento |

Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| ARC_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| ARC_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |



# ASSISTENTE_GIUDIZIARIO
La tabella contiene i dati anagrafici degli assistenti giudiziari. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ASSISTENTE_GIUDIZIARIO | NUMBER NOT NULL | Chiave primaria numerica. |
| COGNOME | VARCHAR2 (50 CHAR) NOT NULL | Cognome dell' Assistente. |
| NOME | VARCHAR2 (50 CHAR) | Nome dell' Assistente. |
| COD_UFFICIO_APPARTENENZA | VARCHAR2 (11 CHAR) | Ufficio di appartenenza dell' Assistente Giudiziario. |
| FLAG_STATO | VARCHAR2 (1 CHAR) | Campo che indica lo stato dell'assistente: Assente Trasferito Presente... Associato al dominio FLAG_STATO di CG_REF_CODES. |
| DATA_INIZIO_VALIDITA | DATE | Data di inizio incarico dell'Assistente Giudiziario. |
| DATA_FINE_VALIDITA | DATE | Data di fine incarico dell'Assistente Giudiziario. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMEN TO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| UDIENZA | UDIENZA_ASSISTENTE_FK2 | COD_ID_ASSISTENTE |




# ASSISTENTE_SOCIALE
La tabella contiene i dati anagrafici degli assistenti sociali. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ASSISTENTE_SOCIALE | NUMBER NOT NULL | Chiave primaria numerica. |
| COGNOME | VARCHAR2 (50 CHAR) NOT NULL | Cognome dell' Assistente Sociale. |
| NOME | VARCHAR2 (50 CHAR) | Nome dell' Assistente Sociale. |
| COD_UFFICIO_APPARTENENZA | VARCHAR2 (11 CHAR) | Ufficio di appartenenza dell' Assistente Sociale. |
| FLAG_STATO | VARCHAR2 (1 CHAR) | Campo che indica lo stato dell'assistente sociale: Assente Trasferito Presente... Associato al dominio FLAG_STATO di CG_REF_CODES. |
| DATA_INIZIO_VALIDITA | DATE | Data di inizio incarico dell'Assistente Sociale. |
| DATA_FINE_VALIDITA | DATE | Data di fine incarico dell'Assistente Sociale. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| INDIRIZZO | VARCHAR2 (200 CHAR) | Indirizzo dell’assistente sociale |
| TELEFONO | VARCHAR2 (12 CHAR) | Telefono dell’assistente sociale |
| CODICE_FISCALE | VARCHAR2 (16 CHAR) | Codice fiscale dell’assistente sociale |
| CELLULARE | VARCHAR2 (12 CHAR) | Numero del Cellullare dell’assistente sociale |
| FAX | VARCHAR2 (12 CHAR) | Fax dell’assistente sociale |
| EMAIL | VARCHAR2 (100 CHAR) | Email dell’assistente sociale |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| ASSISTENTE_SOCIALE_ATTIVITA | ASS_SOC_ATT_ESP_FK | ASS_SOC_ID_ASS_SOCIALE |
| ATTIVITA | ATT_ASS_SOC_FK | ASS_SOC_ID_ASS_SOCIALE |


# ASSISTENTE_SOCIALE_ATTIVITA
La tabella è una associativa tra la tabella Attività e Assistente Sociale. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| DATA_INIZIO | DATE NOT NULL | Data di Inizio Attività dell’Assistente Sociale. |
| DATA_FINE | DATE | Data di Fine Attività dell’Assistente Sociale. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| ASS_SOC_ID_ASS_SOCIALE | NUMBER NOT NULL | ID dell’Assistente Sociale interessato. |
| ATT_ID_ATTIVITA | NUMBER NOT NULL. | ID dell’Attività espletata. |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| ASS_SOC_ATT_ATT_FK | ATT_ID_ATTIVITA | (ATTIVITA.ID_ATTIVITA) |
| ASS_SOC_ATT_ESP_FK | ASS_SOC_ID_ASS_SOCIALE | (ASSISTENTE_SOCIALE.ID_ASSISTENTE_SOCIALE) |

# ASSOC_UTENTE_SIES_ADN
La tabella è una associativa tra la tabella Utente e Utenza_ADN. utilizzata da tutti i sottosistemi di sies.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID | NUMBER(38) | Identificativo record |
| UTE_COD_UTENTE | VARCHAR2 (100 CHAR) | Codice univoco che identifica l'utente a livello distrettuale. Tale codice è usato in tutte le tabelle nelle quali è registrata l'informazione di chi ha fatto cosa. |
| ID_UTENTE_ADN | NUMBER(38) | Identificativo ADN dell’utente |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| ASSOC_UTENTE_SIES_ADN_PK | ID |  |
| ASSOC_UTENTE_SIES_ADN_UK | ID_UTENTE_ADN, UTE_COD_UTENTE |  |
| ASSOC_UTENTE_UTENTE_ADN_FK | ID_UTENTE_ADN | ID |
| ASSOC_UTENTE_UTENTE_FK | UTE_COD_UTENTE | COD_UTENTE |



# ATTIVITA
La tabella contiene i dati relativi al Tipo Attività in SIEPE

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ATTIVITA | NUMBER NOT NULL | Chiave primaria numerica. |
| DATA_INIZIO | DATE | Data di Inizio Attività. |
| DATA_CHIUSURA | DATE | Data di Fine Attività. |
| COD_TIPO_ATTIVITA | VARCHAR2 (4 CHAR) | Codifica del Tipo Attività eseguita. Associata al dominio TIPO_ATTIVITA_SIEPE. |
| NOTE | VARCHAR2 (1000 CHAR) | Note |
| DOC_BLOB | BLOB | Descrizione attività |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FAS_SIEPE | NUMBER NOT NULL |  |
| ASS_SOC_ID_ASS_SOCIALE | NUMBER | ID Assistente Sociale attualmente operativo sull’Attività. |
| FLAG_DOCUMENTO_REGISTRATO | VARCHAR2 (1 CHAR) | Indica se il documento è stato registrato S/N |
| COD_ESITO_ATTIVITA | VARCHAR2 (4 CHAR) | Codice dell’esito dell’attività |
| NOTA_CHIUSURA | VARCHAR2 (1000 CHAR) | Nota di chiusura |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| ATT_ASS_SOC_FK | ASS_SOC_ID_ASS_SOCIALE | (ASSISTENTE_SOCIALE.ID_ASSISTENTE_SOCIALE) |
| ATT_FAS_SIEPE_FK | FAS_SIE_ID_FAS_SIEPE | (FASCICOLO_SIEPE.ID_FASCICOLO_SIEPE) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| ASSISTENTE_SOCIALE_ATTIVITA | ASS_SOC_ATT_ATT_FK | ATT_ID_ATTIVITA |
| ESPERTO_ATTIVITA | ESP_ATT_ATT_FK | ATT_ID_ATTIVITA |
| RELAZIONE | REL_ATT_FK | ATT_ID_ATTIVITA |

# AULA_UDIENZA
La tabella contiene i dati relativi all’aula di un udienza. utilizzata dal sottosistema siep-sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_AULA | NUMBER(38) not null | PK Aula |
| ID_SEZIONE | NUMBER(38) not null | Identificativo della sezione |
| DESCRIZIONE_AULA | VARCHAR2(100) | Descrizione aula |
| DESCRIZIONE_STANZA | VARCHAR2(100) | Descrizione stanza |
| DESCRIZIONE_INGRESSO | VARCHAR2(100) | Descrizione ingresso |
| NUMERO_PIANO | VARCHAR2(30) | Numero del piano |
| FLAG_PREDEFINITA | VARCHAR2(1) | Indica se l’aula è predefinita |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(11) | Utenza dell’operatore che ha effettuato l’inserimento |
| DATA_INSERIMENTO | DATE | Data inserimento |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(100) | ufficio dell’operatore che ha effettuato l’inserimento |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(11) | Utenza dell’operatore che ha effettuato l’aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data dell’aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(100) | Ufficio dell’operatore che ha effettuato l’aggiornamento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| SEZIONE_ID_SEZIONE | ID_SEZIONE | (SEZIONE.ID_SEZIONE) |



# AUTORITA_ESTERNA
La tabella contiene i dati relativi all’autorità esterna a cui inviare la notifica. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_AUTORITA_ESTERNA | NUMBER NOT NULL | Chiave naturale dell'entità. Legata a sequence AUT_EST_SEQ. |
| COD_TIPO_AUTORITA | VARCHAR2 (2 CHAR) NOT NULL | Codice dell'autorità. Identifica l'autorità alla quale inviare la notifica. Deriva da dominio e assume ad esempio i seguenti valori: CASA CIRCONDARIALE CASA MANDAMENTALE OSPEDALE PSICHIATRICO GIUDIZIARIO COMMISSARIATO DI P.S.
QUESTURA Associata al dominio TIPO_AUTORITA di CG_REF_CODES. |
| DESCRIZIONE | VARCHAR2 (200 CHAR) | Descrizione estesa dell'autorità. Questo campo generalmente compare in stampa o a video. Può essere utilizzato per dettagliare maggiormente una autorità. |
| COD_SEDE | VARCHAR2 (6 CHAR) | Descrizione del luogo a cui appartiene l'autorità esterna di riferimento. Fa riferimento alla tabella di dominio COMUNE. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| NOTIFICA | NOT_1_AUT_EST_FK | AUT_EST_ID_AUTORITA_ESTERNA |
| NOTIFICA | NOT_AUT_EST_DELEG_FK | AUT_EST_ID_AUTORITA_EST_DELEG |


# AVVISI_AVVOCATO
La tabella contiene i dati relativi agli avvisi di pertinenza di un avvocato. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_AVVISO | NUMBER not null | Identificativo dell''Avviso |
| ID_AVVOCATO | NUMBER(38) not null | Identificativo dell''Avvocato |
| COGNOME_SOGGETTO | VARCHAR2(100) | Cognome del Soggetto del provvedimento a cui fa riferimento l'avviso |
| NOME_SOGGETTO | VARCHAR2(100) | Nome del Soggetto del provvedimento a cui fa riferimento l'avviso |
| ID_EVENTO | NUMBER(38) not null | Identificativo evento |
| DESC_PROVVEDIMENTO | VARCHAR2(100) | Tipo provvedimento a cui fa riferimento l'avviso |
| UFFICIO_EMITTENTE | VARCHAR2(100) | Ufficio che emette l''avviso |
| TESTO_AVVISO | VARCHAR2(2000) not null | Contenuto dell''avviso |
| FLAG_VISUALIZZAZIONE | VARCHAR2(1) not null | Avviso visualizzato=S Avviso Non Visualizzato=N' |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice dell’operatore che ha effettuato l’inserimento |
| DATA_INSERIMENTO | DATE | Data dell’inserimento |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11) | Codice dell’ufficio dell’operatore che ha effettuato l’inserimento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| ID_AVVOCATO_AVVISI_FK | ID_AVVOCATO | (AVVOCATO.ID_AVVOCATO) |


# AVVOCATO
La tabella contiene i dati relativi all’anagrafica dell’avvocato. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_AVVOCATO | NUMBER NOT NULL | Chiave naturale dell'entità. Legata a sequence AVV_SEQ. |
| COGNOME | VARCHAR2 (100 CHAR) | Cognome dell'Avvocato. |
| NOME | VARCHAR2 (100 CHAR) | Nome dell'Avvocato. |
| FORO | VARCHAR2 (100 CHAR) NOT NULL | Campo descrittivo libero che contiene la sede del foro di appartenenza dell'avvocato. |
| INDIRIZZO | VARCHAR2 (300 CHAR) | Campo libero che contiene l'indirizzo dell'Avvocato. |
| TELEFONO | VARCHAR2 (20 CHAR) | Campo libero che contiene eventuali recapiti telefonici. |
| FAX | VARCHAR2 (20 CHAR) | Campo libero che contiene eventuali recapiti FAX. |
| E_MAIL | VARCHAR2 (200 CHAR) | Campo libero che contiene eventuali recapiti e-mail. |
| COD_COMUNE_RESIDENZA | VARCHAR2 (6 CHAR) | Identificativo del comune di residenza dell'Avvocato. |
| COD_LUOGO_NASCITA | VARCHAR2 (6 CHAR) | Identificativo del comune di nascita dell'Avvocato. |
| DATA_NASCITA | DATE | Data di nascita dell'Avvocato. |
| DATA_SOSPESO_FINO_AL | DATE | Il campo contiene l'eventuale data di fine sospensione dell'Avvocato. |
| DATA_RADIATO_DAL | DATE | Il campo contiene l'eventuale data di radiazione dell'Avvocato. |
| COD_NON_ATTIVITA | VARCHAR2  (4 CHAR) | Il campo codifica la motivazione di inattività dell'Avvocato: Cessazione Attività Trasferito... Associato al dominio NON_ATTIVITA di CG_REF_CODES. |
| NOTE | VARCHAR2 (2000 CHAR) | Eventuali note registrate per l'Avvocato. |
| FLAG_CANCELLATO | VARCHAR2 (1 CHAR) DEFAULT 'N' | La cancellazione di Avvocato avviene logicamente con l'utilizzo di FLAG_CANCELLATO. Associato al Dominio FLAG_SI_NO di CG_REF_CODES. |
| COD_UFFICIO_APPARTENENZA | VARCHAR2 (11 CHAR) | Ufficio di appartenenza dell' Avvocato. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| COD_FISCALE | VARCHAR2 (16 CHAR) | Codice fiscale dell’avvocato |
| PROVINCIA | VARCHAR2 (4 CHAR) | Provincia del foro dove esercita l’avvocato |
| CAP | VARCHAR2 (6 CHAR) | CAP della provincia del foro dove esercita l’avvocato |
| ID_AVVOCATO_STANDARD | NUMBER | Puntamento al record dell’avvocato di default |
| FLAG_VISUALIZZA | NUMBER | Indica se l’avvocato sarà o meno visualizzato |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| ATT_ASS_SOC_FK | ASS_SOC_ID_ASS_SOCIALE | (ASSISTENTE_SOCIALE.ID_ASSISTENTE_SOCIALE) |
| ATT_FAS_SIEPE_FK | FAS_SIE_ID_FAS_SIEPE | (FASCICOLO_SIEPE.ID_FASCICOLO_SIEPE) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| AVVOCATO_FASCICOLO_SIEP | AVV_FAS_AVV_FK | AVV_ID_AVVOCATO |
| AVVISI_AVVOCATO | ID_AVVOCATO_AVVISI_FK | ID_AVVOCATO |
| AVVISI_AVVOCATO_OLD | ID_AVVOCATO_AVVISI_OLD_FK | ID_AVVOCATO |
| PARTI_UDIENZA_DIFENSORE | ID_AVVOCATO_FK | AVV_ID_AVVOCATO |
| STORICO_AVVOCATO | STO_AVV_FK | AVV_ID_AVVOCATO |


# AVVOCATO_FASCICOLO_SIEP
La tabella contiene i dati relativi ad un avvocato per fascicolo siep. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_AVVOCATO_FASCICOLO_SIEP | NUMBER NOT NULL | Chiave naturale della tabella. Legata alla sequence: AVV_FAS_SIE_SEQ. |
| COD_TIPO_AVVOCATO | VARCHAR2 (2 CHAR) NOT NULL | Indica il tipo di avvocato che si sta relazionando ossia specifica il rapporto tra il soggetto e il suo avvocato. Deriva da domino e assume i seguenti valori: D'UFFICIO DI FIDUCIA DELLA FASE DI GIUDIZIO. Associato al dominio TIPO_AVVOCATO. |
| DATA_INIZIO_VALIDITA | DATE NOT NULL | Data di inizio validità del rapporto dell'avvocato per un soggetto nell'ambito di un fascicolo SIEP. |
| DATA_FINE_VALIDITA | DATE | Data di fine validità del rapporto dell'avvocato per un soggetto nell'ambito di un fascicolo SIEP. |
| COD_MOTIVO_DESIGNAZIONE | VARCHAR2 (4 CHAR) | Codifica del motivo di designazione; può essere: Sostituzione Difensore di Ufficio; Mancanza Difensore di Fiducia o del Giudizio; Revoca del Difensore... Associato al dominio MOTIVO_DESIGNAZIONE. |
| NOTE | VARCHAR2 (2000 CHAR) | Eventuali note aggiuntive. |
| COD_TIPO_AUTORITA | VARCHAR2 (2 CHAR) | Tipo di autorità |
| SEDE_TIPO_AUTORITA | VARCHAR2 (6 CHAR) | Sede dell’ autorità |
| INDIRIZZO_TIPO_AUTORITA | VARCHAR2 (300 CHAR) | Indirizzo autorità |
| COD_TIPO_AUTORITA_DIF | VARCHAR2 (2 CHAR) | Tipo del difensore |
| SEDE_TIPO_AUTORITA_DIF | VARCHAR2 (6 CHAR) | Sede del difensore |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| AVV_ID_AVVOCATO | NUMBER NOT NULL | Chiave esterna dell’Identificativo dell’avvocato |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL | Identificativo del fascicolo SIEP |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2 (4 CHAR) | Identificativo dell’istituto di detenzione |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| MOTIVO | VARCHAR2 (20 CHAR) | Motivo |
| AVV_ID_AVVOCATO_FASCICOLO_SOST | NUMBER | Identificativo dell’avvocato sostituito al fascicolo |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| AVV_FAS_AVV_FK | AVV_ID_AVVOCATO | (AVVOCATO.ID_AVVOCATO) |
| AVV_FAS_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| NOTIFICA | NOT_1_AVV_FAS_FK | AVV_ID_AVVOCATO_FASCICOLO_SIEP |



# AVVOCATO_FASCICOLO_SIGE
La tabella contiene i dati relativi ad un avvocato per fascicolo sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_AVVOCATO_FASCICOLO_SIGE | NUMBER NOT NULL | Chiave naturale della tabella. Legata alla sequence: AVV_FAS_SIGE_SEQ. |
| COD_TIPO_AVVOCATO | VARCHAR2 (2 CHAR) NOT NULL | Indica il tipo di avvocato che si sta relazionando ossia specifica il rapporto tra il soggetto e il suo avvocato. Deriva da domino e assume i seguenti valori: D'UFFICIO DI FIDUCIA DELLA FASE DI GIUDIZIO. Associato al dominio TIPO_AVVOCATO. |
| DATA_INIZIO_VALIDITA | DATE NOT NULL | Data di inizio validità del rapporto dell'avvocato per un soggetto nell'ambito di un fascicolo SIGE. |
| DATA_FINE_VALIDITA | DATE | Data di fine validità del rapporto dell'avvocato per un soggetto nell'ambito di un fascicolo SIGE. |
| COD_MOTIVO_DESIGNAZIONE | VARCHAR2 (4 CHAR) | Codifica del motivo di designazione; può essere: Sostituzione Difensore di Ufficio; Mancanza Difensore di Fiducia o del Giudizio; Revoca del Difensore... Associato al dominio MOTIVO_DESIGNAZIONE. |
| NOTE | VARCHAR2 (2000 CHAR) | Eventuali note aggiuntive. |
| COD_TIPO_AUTORITA | VARCHAR2 (2 CHAR) | Tipo del difensore |
| SEDE_TIPO_AUTORITA | VARCHAR2 (6 CHAR) | Sede del difensore |
| INDIRIZZO_TIPO_AUTORITA | VARCHAR2 (300 CHAR) | Indirizzo autorità |
| COD_TIPO_AUTORITA_DIF | VARCHAR2 (2 CHAR) | Tipo del difensore |
| SEDE_TIPO_AUTORITA_DIF | VARCHAR2 (6 CHAR) | Sede del difensore |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIGE_ID_FASCICOLO_SIGE | NUMBER NOT NULL | Identificativo del fascicolo SIGE |
| AVV_ID_AVVOCATO | NUMBER NOT NULL | Identificativo dell’avvocato |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2 (4 CHAR). | Identificativo dell’istituto del detenzione |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| AVV_FAS_SIGE_FASCICOLO_SIGE_FK | FAS_SIGE_ID_FASCICOLO_SIGE | (FASCICOLO_SIGE.ID_FASCICOLO_SIGE) |

# AVVOCATO_FASCICOLO_SIUS
La tabella contiene i dati relativi ad un avvocato per fascicolo sius. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_AVVOCATO_FASCICOLO_SIUS | NUMBER NOT NULL | Chiave naturale della tabella. Legata alla sequence: AVV_FAS_SIU_SEQ |
| COD_TIPO_AVVOCATO | VARCHAR2 (2 CHAR) NOT NULL | Indica il tipo di avvocato che si sta relazionando ossia specifica il rapporto tra il soggetto e il suo avvocato. Deriva da domino e assume i seguenti valori: D'UFFICIO DI FIDUCIA DELLA FASE DI GIUDIZIO. Associato al dominio TIPO_AVVOCATO. |
| DATA_INIZIO_VALIDITA | DATE
NOT NULL | Data di inizio validità del rapporto dell'avvocato per un soggetto nell'ambito di un fascicolo SIEP. |
| DATA_FINE_VALIDITA | DATE | Data di fine validità del rapporto dell'avvocato per un soggetto nell'ambito di un fascicolo SIEP. |
| COD_MOTIVO_DESIGNAZIONE | VARCHAR2 (4 CHAR) | Codifica del motivo di designazione; può essere: Sostituzione Difensore di Ufficio; Mancanza Difensore di Fiducia o del Giudizio; Revoca del Difensore... Associato al dominio MOTIVO_DESIGNAZIONE. |
| NOTE | VARCHAR2 (2000 CHAR) | Eventuali note aggiuntive. |
| COD_TIPO_AUTORITA | VARCHAR2 (2 CHAR) | Tipo del difensore |
| SEDE_TIPO_AUTORITA | VARCHAR2 (6 CHAR) | Sede del difensore |
| INDIRIZZO_TIPO_AUTORITA | VARCHAR2 (300 CHAR) | Indirizzo autorità |
| COD_TIPO_AUTORITA_DIF | VARCHAR2 (2 CHAR) | Tipo del difensore |
| SEDE_TIPO_AUTORITA_DIF | VARCHAR2 (6 CHAR) | Sede del difensore |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER NOT NULL | Identificativo del fascicolo SIUS |
| AVV_ID_AVVOCATO | NUMBER NOT NULL | Identificativo dell’avvocato |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2 (4 CHAR) | Identificativo dell’istituto del detenzione |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| NOTIFICA | NOT_2_AVV_FAS_FK | AVV_ID_AVVOCATO_FASCICOLO_SIUS |

# BATCH_PAGOPA
La tabella contiene i dati relativi al batch per il colloquio col sistema PST_PagoPA. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_BATCH_PAGOPA | NUMBER(38) NOT NULL | Primary Key della tabella, legata alla sequence batch_pagopa_seq |
| DATA_INIZIO_ESECUZIONE | DATE | Data di inizio esecuzione del Batch |
| DATA_FINE_ESECUZIONE | DATE | Data di fine esecuzione del Batch |
| NUM_POS_DEBITORIE_VERIFICATE | NUMBER(4) | Indica il numero delle posizioni debitorie verificate durante l’esecuzione del Batch |
| NUM_BOLLETTINI_AGGIORNATI | NUMBER(4) | Indica il numero di bollettini aggiornati durante l’esecuzione del Batch |
| ESITO_ESECUZIONE | VARCHAR2(2000) | Indica l’esito dell’esecuzione del Batch |
| ERRORE_ESECUZIONE | VARCHAR2(2000) | Indica l’errore verificatosi durante l’esecuzione del Batch |
| num_iuv_verificati | NUMBER(4) | Indica il numero dei Bollettini verificati |
| num_errori_invocazione | NUMBER(4) | Indica il numero degli errori per invocazione |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| bollettino_batch_pagopa | bollbatch_batch_fk | fk_id_batch_pagopa |


# BENEFICIO
La tabella contiene i dati relativi al dettaglio dei benefici concessi o revocati. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_BENEFICIO | NUMBER NOT NULL | Chiave naturale interna legata a Sequence BEN_SEQ. |
| COD_NATURA_BENEFICIO | VARCHAR2 (1 CHAR) NOT NULL | Esprime la natura del beneficio intesa nella sua concessione o revoca. Deriva da dominio Può assumere i seguenti valori: REVOCATO CONCESSO. |
| COD_TIPO_BENEFICIO | VARCHAR2 (2 CHAR) NOT NULL | E' il dettaglio del beneficio concesso cioè è specificato il tipo di beneficio evidenziando e distinguendo quelli che derivano dalla sola sentenza. Deriva da dominio e assume i seguenti valori: SOSPENSIONE CONDIZIONALE NON MENZIONE INDULTO
AMNISTIA INDULTO GRAZIA. Associato al dominio TIPO_BENEFICIO della tabella CG_REF_CODES. |
| COD_TIPO_SOSP_SUBORDINATA | VARCHAR2 (2 CHAR) DEFAULT '-' | Codice dell'eventuale sospensione subordinata. Deriva da dominio e può assumere i seguenti valori: ALL'ADEMPIMENTO DELL'OBBLIGO DELLA RESTITUZIONE; AL PAGAMENTO DELLA SOMMA LIQUIDATA A TITOLO DI RISARC.DANNO O PROVV.ASSEGNATA SULL'AMMONTARE; ALLA PUBBLICAZIONE DELLA SENTENZA A TITOLO DI RIPARAZIONE DEL DANNO; ALL'ELIMINAZIONE DELLE CONSEGUENZE DANNOSE O PERICOLOSE DEL REATO.
Associato al dominio TIPO_SOSP_SUBORDINATA della tabella CG_REF_CODES |
| NUM_ANNI_RECLUSIONE | NUMBER | Numero di anni di reclusione riferiti al tipo di beneficio concesso o revocato. |
| NUM_MESI_RECLUSIONE | NUMBER | Numero di mesi di reclusione riferiti al tipo di beneficio concesso o revocato. |
| NUM_GIORNI_RECLUSIONE | NUMBER | Numero di giorni di reclusione riferiti al tipo di beneficio concesso o revocato. |
| IMPORTO_MULTA | NUMBER (211) | Importo della sanzione inflitta riferita al tipo di beneficio concesso o revocato. |
| NUM_ANNI_ARRESTO | NUMBER | Numero di anni di arresto riferiti al tipo di beneficio concesso o revocato. |
| NUM_MESI_ARRESTO | NUMBER | Numero di mesi di arresto riferiti al tipo di beneficio concesso o revocato. |
| NUM_GIORNI_ARRESTO | NUMBER | Numero di giorni di arresto riferiti al tipo di beneficio concesso o revocato. |
| IMPORTO_AMMENDA | NUMBER (211) | Importo della sanzione inflitta riferita al tipo di beneficio concesso o revocato. |
| COD_DPR | VARCHAR2 (2 CHAR) DEFAULT 'NULL' | Numero del Decreto del presidente della repubblica riferito allo specifico beneficio. Associato al dominio COD_DPR della tabella CG_REF_CODES. |
| NOTE | VARCHAR2 (2000 CHAR) | Campo a testo libero per aggiungere informazioni ulteriori. |
| INAPPLICABILITA_MIS_SICUREZZA | VARCHAR2 (1 CHAR) | Flag indicante la possibilità di non applicare la misura di sicurezza indicata. Associato al dominio FLAG_SI_NO della tabella CG_REF_SODES. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo fascicolo SIEP |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| COD_SOTTOTIPO_BENEFICIO | VARCHAR2 (2 CHAR) DEFAULT '-' | Sotto tipologia del beneficio |
| NUM_ANNI_SOSPENSIONE | NUMBER | Numero anni di sospensione |
| NUM_MESI_PRESTAZIONE | NUMBER | Numero mesi di prestazione |
| NUM_GIORNI_PRESTAZIONE | NUMBER | Numero giorni di prestazione |
| NUM_ORE_SETTIMANALI | NUMBER | Numero di ore settimanali |
| FLAG_FREQUENZA_SETTIMANALE | VARCHAR2 (1 CHAR) | S/N Frequenza settimanale |
| RIF_ID_PROVVEDIMENTO | NUMBER | Identificativo del provvedimento |
| RIF_COD_TIPO_PROVVEDIMENTO | VARCHAR2 (2 CHAR) DEFAULT '-' | Tipo del provvedimento |
| RIF_DATA_PROVVEDIMENTO | DATE | Data del provvedimento |
| RIF_COD_TIPO_AUTO_EMITTENTE | VARCHAR2 (6 CHAR) DEFAULT '-' | Tipologia di autorità emittente |
| RIF_COD_LUOGO_EMITTENTE | VARCHAR2 (6 CHAR) | Luogo dell’autorità emittente |
| RIF_NUM_SEZIONE_AUTO_EMITTENTE | VARCHAR2 (100 CHAR) | Sezione dell’autorità emittente |
| RIF_ANNO_PROVVEDIMENTO | NUMBER | Anno del provvedimento |
| RIF_NUMERO_PROVVEDIMENTO | VARCHAR2 (6 CHAR) | Numero  del provvedimento |
| NUM_ANNI_ADEMPIMENTO | NUMBER | Numero di anni di adempimento |
| NUM_MESI_ADEMPIMENTO | NUMBER | Mesi di adempimento |
| NUM_GIORNI_ADEMPIMENTO | NUMBER | Giorni di adempimento |
| BEN_ID_BENEFICIO | NUMBER | Identificativo del beneficio |
| RIF_DATA_IRREVOCABILITA. | DATE | Dada di irrevocabilità di riferimento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| BEN_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| BEN_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| BENEFICIO_SENTENZA_SIGE | BEN_SEN_SIGE_FK | BEN_ID_BENEFICIO |
| TIPOLOGIA_ORARIO | TIP_ORA_ID_BEN_FK | BEN_ID_BENEFICIO |


# BENEFICIO_CUMULO
La tabella contiene i dati relativi al dettaglio dei benefici concessi o revocati con il cumulo. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_BENEFICIO_CUMULO | NUMBER(38) NOT NULL | Chiave naturale interna. |
| COD_NATURA_BENEFICIO | VARCHAR2(1 CHAR) NOT NULL | CG_REF_CODES.RV_DOMAIN= ’NATURA_BENEFICIO’ |
| COD_TIPO_BENEFICIO | VARCHAR2(2 CHAR) NOT NULL | CG_REF_CODES.RV_DOMAIN= ’TIPO_BENEFICIO’ |
| COD_TIPO_SOSP_SUBORDINATA | VARCHAR2(2 CHAR) | CG_REF_CODES.RV_DOMAIN= ‘TIPO_SOSP_SUBORDINATA’ |
| COD_SOTTOTIPO_BENEFICIO | VARCHAR2(2 CHAR) | CG_REF_CODES.RV_DOMAIN= ‘SOTTOTIPO_BENEFICIO’ |
| NUM_MESI_RECLUSIONE | NUMBER(3) | Numero mesi reclusione concessi/revocati indulto |
| NUM_ANNI_RECLUSIONE | NUMBER(3) | Numero anni reclusione concessi/revocati indulto |
| NUM_GIORNI_RECLUSIONE | NUMBER(4) | Numero giorni reclusione concessi/revocati indulto |
| IMPORTO_MULTA | NUMBER(112) | Importo multa concessa/revocata indulto |
| NUM_ANNI_ARRESTO | NUMBER(3) | Numero anni arresto concessi/revocati indulto |
| NUM_MESI_ARRESTO | NUMBER(3) | Numero mesi arresto concessi/revocati indulto |
| NUM_GIORNI_ARRESTO | NUMBER(4) | Numero giorni arresto concessi/revocati indulto |
| IMPORTO_AMMENDA | NUMBER(112) | Importo ammenda concessa/revocata indulto |
| COD_DPR | VARCHAR2(2 CHAR) | CG_REF_CODES.RV_DOMAIN= ‘DPR’ |
| NOTE | VARCHAR2(2000 CHAR) | Campo per eventuali note |
| NUM_ANNI_SOSPENSIONE | NUMBER(3) | Anni sospensione concessi |
| NUM_MESI_PRESTAZIONE | NUMBER(3) | Mesi Sospensione - Con Obbligo di Prestazione |
| NUM_GIORNI_PRESTAZIONE | NUMBER(3) | Giorni Sospensione - Con Obbligo di Prestazione |
| NUM_ORE_SETTIMANALI | NUMBER(3) | Ore settimanali Sospensione - Con Adempimenti |
| NUM_ANNI_ADEMPIMENTO | NUMBER(3) | Anni Sospensione - Con Adempimenti |
| NUM_MESI_ADEMPIMENTO | NUMBER(3) | Mesi Sospensione - Con Adempimenti |
| NUM_GIORNI_ADEMPIMENTO | NUMBER(4) | Giorni Sospensione - Con Adempimenti |
| FLAG_FREQUENZA_SETTIMANALE | VARCHAR2(1 CHAR) | Concessione Sospensione - D=Determinata N=Non Determinata |
| ENTE_INCARICATO | VARCHAR2(2000 CHAR) | Descrizione Ente Incaricato |
| RIF_ID_PROVVEDIMENTO | NUMBER(38) | Solo REVOCA - Id Sentenza di concessione |
| RIF_COD_TIPO_PROVVEDIMENTO | VARCHAR2(2 CHAR) DEFAULT '-' | Solo REVOCA – Codice Tipo Provvedimento |
| RIF_DATA_PROVVEDIMENTO | DATE | Solo REVOCA – Data Provvedimento |
| RIF_DATA_IRREVOCABILITA | DATE | Solo REVOCA – Data Irrevocabilità |
| RIF_COD_TIPO_AUTO_EMITTENTE | VARCHAR2(6 CHAR) DEFAULT '-' | Solo REVOCA – Codice Tipo Autorità |
| RIF_COD_LUOGO_EMITTENTE | VARCHAR2(6 CHAR) | Solo REVOCA – Codice Luogo Autorità |
| RIF_NUM_SEZIONE_AUTO_EMITTENTE | VARCHAR2(100 CHAR) | Solo REVOCA – Sezione Autorità |
| RIF_ANNO_PROVVEDIMENTO | NUMBER(4) | Solo REVOCA – Anno Provvedimento |
| RIF_NUMERO_PROVVEDIMENTO | VARCHAR2(8 CHAR) | Solo REVOCA – Numero  Provvedimento |
| TIT_ID_TITOLO_CUMULATO | NUMBER(38) NOT NULL | FK alla tabella TITOLO_CUMULATO |
| FLAG_STATO | VARCHAR2(1 CHAR) NOT NULL | E=estratto M=modificato C=Cancellato I=Iscritto |
| MOTIVO_MODIFICA | VARCHAR2(2000 CHAR) | Note inserite dall''operatore in fase di Modifica Cancellazione Iscrizione |
| ID_BENEFICIO_ORIGINE | NUMBER(38) | Eventuale ID del record BENEFICIO da cui è stato derivato questo record |
| BEN_ID_BENEFICIO_ORIG | NUMBER(38) | Solo Non Menzione - Punta il record Sospensione se collegati - Origine |
| BEN_ID_BENEFICIO_CUMULO | NUMBER(38) | Solo Non Menzione - Punta il record Sospensione se collegati |
| TIT_ID_TITOLO_CUMULO_COLLEGATO | NUMBER(38) | Se REVOCA: Id del Titolo_Cumulato della Concessione;  Se CONCESSO: Id del Titolo_Cumulato relativo alla eventuale Revoca |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100 CHAR) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11 CHAR) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100 CHAR) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(11 CHAR) | Codice Ufficio Utente ultimo aggiornamento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| BEN_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| BEN_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| BENEFICIO_SENTENZA_SIGE | BEN_SEN_SIGE_FK | BEN_ID_BENEFICIO |
| TIPOLOGIA_ORARIO | TIP_ORA_ID_BEN_FK | BEN_ID_BENEFICIO |


# BENEFICIO_SENTENZA_SIGE
La tabella è un’associativa tra il beneficio e la sentenza di sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| BEN_ID_BENEFICIO | NUMBER NOT NULL | ID Beneficio relazionato. |
| FAS_SIGE_SEN_ID | NUMBER NOT NULL. | ID FAS_SIGE_SENTENZA relazionata. |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| BEN_FAS_SIGE_SEN_FK | FAS_SIGE_SEN_ID | (FAS_SIGE_SENTENZA.ID_FAS_SIGE_SENTENZA) |
| BEN_SEN_SIGE_FK | BEN_ID_BENEFICIO | (BENEFICIO.ID_BENEFICIO) |

# bollettino_batch_pagopa
La tabella contiene i dati relativi al batch per la verifica dello stato del bollettino tramite colloquio col sistema PST_PagoPA. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| fk_id_invocazione_pagopa | NUMBER(38) NOT NULL | Foreign Key della tabella, legata alla primary key ID_INVOCAZIONE_PAGOPA |
| fk_id_bollettino_pagopa | NUMBER(38) NOT NULL | Foreign Key della tabella, legata alla primary key ID_BOLLETTINO_PAGOPA |
| fk_id_batch_pagopa | NUMBER(38) NOT NULL | Foreign Key della tabella, legata alla primary key ID_BATCH_PAGOPA |
| stato_pagopa | VARCHAR2(2000) | Indica lo stato del pagamento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| BOLLBATCH_BATCH_FK | FK_ID_BATCH_PAGOPA | (BATCH_PAGOPA.ID_BATCH_PAGOPA) |
| BOLLBATCH_BOLLETTINO_FK | FK_ID_BOLLETTINO_PAGOPA | (BOLLETTINO_PAGOPA.ID_BOLLETTINO_PAGOPA) |
| BOLLBATCH_INVOCAZIONE_FK | FK_ID_INVOCAZIONE_PAGOPA | (INVOCAZIONE_PAGOPA.ID_INVOCAZIONE_PAGOPA) |


# BOLLETTINO_PAGOPA
La tabella contiene i dati relativi al bollettino per il colloquio col sistema PST_PagoPA. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_BOLLETTINO_PAGOPA | NUMBER(38) NOT NULL | Primary Key della tabella, legata alla sequence boll_pag_seq |
| PROG_RATA | NUMBER(4) | Indica il numero progressivo della rata |
| NUMERO_RATE | NUMBER(4) | Indica il numero totale di rate |
| TIPO_RATEIZZAZIONE | VARCHAR2(1) | Indica il tipo di rateizzazione (R per Pagamento Rateizzato, U per Rata Unica) |
| IUV | VARCHAR2(35) | Indica l’Identificativo Univoco Versamento del bollettino |
| IMPORTO_RATA | NUMBER(16,2) | Indica l’importo della rata |
| IMPORTO_PAGATO | NUMBER(16,2) | Indica l’importo pagato della rata |
| DATA_AVV_PAGAMENTO | DATE | Indica la data di avvenuto pagamento |
| DATA_SCADENZA | DATE | Indica la data di scadenza del bollettino |
| DATA_SCADENZA_RICH | DATE | Indica la data di scadenza della richiesta |
| STATO_PAGAMENTO | VARCHAR2(2) | Indica lo stato del pagamento (PN per Non Pagato, PA per Pagato, PP per Pagato Parzialmente) |
| DOC_BOLL_BLOB | BLOB | Contiene il bollettino in formato .pdf |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Indica il Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Indica la Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11) | Indica il Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100) | Indica il Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Indica la Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(11) | Indica il Codice Ufficio Utente ultimo aggiornamento |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER(38) | Foreign Key verso la tabella FASCICOLO_SIEP.ID_FASCICOLO_SIEP |
| RAT_ID_RATEIZZAZIONE_PP | NUMBER(38) | Foreign Key verso la tabella RATEIZZAZIONE_PP.ID_ RATEIZZAZIONE_PP |
| DATA_ULTIMO_CONTROLLO | DATE | Indica la data dell’ultimo controllo dopo l’esecuzione del Batch |
| CODICE_FISCALE | VARCHAR2(16) | Indica il codice fiscale del soggetto dopo l’esecuzione del Batch |
| STATO_PAGOPA | VARCHAR2(2000) | Indica lo stato del pagamento dopo l’esecuzione del Batch |
| ERRORE_PAGOPA | VARCHAR2(2000) | Indica la descrizione dell’errore dopo l’esecuzione del Batch |
| CODICE_DISTRETTO | VARCHAR2(10) | Indica il codice del distretto dopo l’esecuzione del Batch |
| DATA_GENERAZIONE_BOLLETTINO | DATE | Indica la data di generazione del bollettino |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| BOLLETT_PAGOPA_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |
| BOLLETT_PAGOPA_RATEIZZA_FK | RAT_ID_RATEIZZAZIONE_PP | (RATEIZZAZIONE_PP. ID_RATEIZZAZIONE_PP) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| bollettino_batch_pagopa | bollbatch_bollettino_fk | fk_id_bollettino_pagopa |


# CAMPO_NOTA
La tabella contiene i dati relativi alle note di un provvedimento. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_CAMPO_NOTA | NUMBER NOT NULL | Chiave interna legata a sequence CAM_NOT_SEQ. |
| PROGRESSIVO | NUMBER NOT NULL | Progressivo della nota nell'ambito del singolo provvedimento. Non è gestito da sequence e il suo incremento viene gestito dall'applicazione. |
| DESCR | VARCHAR2 (2000 CHAR) NOT NULL | Campo in cui inserire la nota (max. 2000 caratteri). |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| OGGETTO_NOTA_RES | VARCHAR2 (45 CHAR) | Descrizione nota all’oggetto RES |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| CAM_NOT_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| CAM_NOT_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| ISTANZA | CAM_ID_CAMPO_NOTE_FK | CAM_ID_CAMPO_NOTE |


# CANC_ASS_FASC_SIUS
La tabella è un’associativa tra il fascicolo sius e la cancelleria assegnataria. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_CANCELLERIA_ASSEGNATARIA | VARCHAR2 (3 CHAR) NOT NULL | Identificativo della cancelleria assegnataria |
| COD_UFFICIO | VARCHAR2 (11 CHAR) NOT NULL | Codice dell’Ufficio |
| FAS_SIUS_ID_FASCICOLO_SIUS | NUMBER NOT NULL | Identificativo del fascicolo SIUS |
| COD_STATO_PROCEDIMENTO | VARCHAR2 (4 CHAR) | Stato del procedimento |
| DATA_INIZIO | DATE NOT NULL | Data inizio |
| DATA_FINE | DATE | Data fine |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| DESCR_STATO_PROCEDIMENTO | VARCHAR2 (2000 CHAR) DEFAULT 'NULL'. | Descrizione dello stato del procedimento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| CAN_ASS_FAS_SIUS_CAN_ASS | COD_UFFICIO | (CANCELLERIA_ASSEGNATARIA.COD_UFFICIO) |
| CAN_ASS_FAS_SIUS_CAN_ASS | COD_CANCELLERIA_ASSEGNATARIA | (CANCELLERIA_ASSEGNATARIA.COD_CANCELLERIA_ASSEGNATARIA) |
| FAS_SIUS_ID_CAN_ASS_FASC_SIUS | FAS_SIUS_ID_FASCICOLO_SIUS | (FASCICOLO_SIUS.ID_FASCICOLO_SIUS) |

# CANCELLERIA_ASSEGNATARIA
La tabella contiene i dati relativi alla cancelleria assegnataria. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_CANCELLERIA_ASSEGNATARIA | VARCHAR2 (3 CHAR) NOT NULL | Identificativo della tabella |
| COD_UFFICIO | VARCHAR2 (11 CHAR) NOT NULL | Codice dell’ufficio |
| DESC_CANCELLERIA_ASSEGNATARIA | VARCHAR2 (100 CHAR) | Descrizione della cancelleria assegnataria |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR). | Ufficio dell’operatore che ha aggiornato il record |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| CANC_ASS_FASC_SIUS | CAN_ASS_FAS_SIUS_CAN_ASS | COD_CANCELLERIA_ASSEGNATARIA |
| CANC_ASS_FASC_SIUS | CAN_ASS_FAS_SIUS_CAN_ASS | COD_UFFICIO |



# CERTIFICATO_OMONIMI_NSC
La tabella contiene i dati relativi ai certificati del casellario giudiziale per gli omonimi risultanti nelle ricerche del soggetto. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_CERTIFICATO_OMONIMI | NUMBER NOT NULL | Chiave primaria  della tabella |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| CERTIFICATO | BLOB | Certificato dei soggetti omonimi |



# CERTIFICATO_STATO_ESEC
La tabella contiene i dati relativi al certificato dello stato di esecuzione. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_CERTIFICATO_STATO_ESEC | NUMBER NOT NULL | Chiave primaria della tabella |
| ANNOTAZIONI | VARCHAR2 (2000 CHAR) | Annotazioni |
| FLAG_UPLOAD | VARCHAR2 (1 CHAR) NOT NULL | Flag upload S/N |
| DOC_BLOB | BLOB | Contiene il pdf del certificato |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP. | NUMBER | Identificativo del fascicolo SIEP |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| CERT_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |




# CG_REF_CODES
La tabella contiene i dati utilizzati per codificare le tabelle tipologiche. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| RV_DOMAIN | VARCHAR2 (100 CHAR) NOT NULL | Nome del dominio per la sua identificazione in tabella |
| RV_LOW_VALUE | VARCHAR2 (240 CHAR) NOT NULL | Codice che normalmente è inserito nel campo che deve essere decodificato. |
| RV_HIGH_VALUE | VARCHAR2 (240 CHAR) | Campo di servizio usato per maggiori dettagli: a volte è usato per raggruppare i valori del campo RV_HIGH_VALUE |
| RV_ABBREVIATION | VARCHAR2 (240 CHAR) | Campo di servizio usato per maggiori dettagli |
| RV_MEANING | VARCHAR2 (500 CHAR) | Descrizione del codice indicato nel campo RV_LOW_VALUE. |
| RV_ALT2_VALUE | VARCHAR2 (24 CHAR) |  |
| RV_ALT3_VALUE | VARCHAR2 (24 CHAR) |  |
| RV_ALT4_VALUE | VARCHAR2 (24 CHAR) |  |
| RV_ALT5_VALUE | VARCHAR2 (24 CHAR). |  |


Di seguito si inserisce un esempio per chiarire il contenuto della tabella:

| RV_DOMAIN | RV_LOW_VALUE | RV_HIGH_VALUE | RV_ABBREVIATION | RV_MEANING | RV_ALT2_VALUE | RV_ALT3_VALUE | RV_ALT4_VALUE | RV_ALT5_VALUE |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ESITO_TENORE | 1260 | U029 | 0076 | Sospende Cautelativamente la Misura Alternativa  e Trasmette Atti al TdS |  |  |  |  |
| ESITO_TENORE | 1280 | U031 | 0042 | Approva |  |  |  |  |
| ESITO_TENORE | 1273 | U030 | 0003 | Dichiara Inammissibilità |  |  |  |  |
| ESITO_TENORE | 1272 | U030 | 0005 | Dichiara la Propria Incompetenza |  |  |  |  |
| ESITO_TENORE | 1284 | U031 | 0005 | Dichiara la Propria Incompetenza |  |  |  |  |
| ESITO_TENORE | 1283 | U031 | 0004 | Dichiara N.D.P./N.L.P. |  |  |  |  |
| ESITO_TENORE | 1282 | U031 | 0044 | Non Approva e Restituisce con Osservazioni |  |  |  |  |
| ESITO_TENORE | 1271 | U030 | 0004 | Dichiara N.D.P./N.L.P. |  |  |  |  |
| ESITO_TENORE | 1263 | U029 | 0004 | Dichiara N.D.P./ N.L.P. |  |  |  |  |
| ESITO_TENORE | 1262 | U029 | 0078 | Non Sospende |  |  |  |  |
| ESITO_TENORE | 1261 | U029 | 0077 | Non Sospende la Misura  Alternativa e Trasmette gli Atti al TdS con Proposta di Revoca |  |  |  |  |
| ESITO_TENORE | 1270 | U030 | 0064 | Dichiara Perdita di Efficacia, Ordina la Scarcerazione |  |  |  |  |
| ESITO_TENORE | 1265 | U029 | 0003 | Dichiara Inammissibilità |  |  |  |  |
| ESITO_TENORE | 1264 | U029 | 0005 | Dichiara la Propria Incompetenza |  |  |  |  |
| ESITO_TENORE | 0057 | C014 | 0004 | Dichiara N.D.P./ N.L.P. |  |  |  |  |
| ESITO_TENORE | 0058 | C014 | 0005 | Dichiara la Propria Incompetenza |  |  |  |  |
| ESITO_TENORE | 0053 | C014 | 0035 | Concede per un Periodo |  |  |  |  |
| ESITO_TENORE | 0056 | C014 | 0002 | Rigetta |  |  |  |  |
| ESITO_TENORE | 0059 | C014 | 0003 | Dichiara L’Inammissibilità |  |  |  |  |
| ESITO_TENORE | 0062 | C015 | 0004 | Dichiara N.D.P./ N.L.P. |  |  |  |  |
| ESITO_TENORE | 0063 | C015 | 0005 | Dichiara la Propria Incompetenza |  |  |  |  |


# CIRCOSTANZA
La tabella contiene i dati relativi alle circostanze del reato. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_CIRCOSTANZA | NUMBER NOT NULL | Chiave numerica naturale per la gestione dei record in tabella. Legata a Sequence CIR_SEQ. |
| COD_TIPO_CIRCOSTANZA | VARCHAR2 (1 CHAR) | Determina il tipo di circostanza. Deriva da dominio e può assumere i seguenti valori: C = Circostanza N = Norma. Associato al dominio TIPO_CIRCOSTANZA della tabella CG_REF_CODES. |
| COD_FONTE | VARCHAR2 (5 CHAR) | FONTE GIURIDICA è il tipo di fonte giuridica relativo agli articoli di reato; es.: codice penale legge. Associato al Dominio FONTE della Tabella CG_REF_CODES. |
| ANNO_FONTE | NUMBER | Anno della norma. |
| NUMERO_FONTE | VARCHAR2 (6 CHAR) | Numero della norma. |
| COD_SOTTONUMERAZIONE | VARCHAR2 (2 CHAR) | Sottonumerazione articolo (bis ter ecc.) Associato al Dominio SOTTONUMERAZIONE della Tabella CG_REF_CODES. |
| COMMA | VARCHAR2 (10 CHAR) | Comma dell'articolo trattato. |
| LETTERA | VARCHAR2 (2 CHAR) | Lettera dell'articolo trattato. |
| NUMERO | VARCHAR2 (2 CHAR) | Eventuale numero dell'articolo trattato. |
| ARTICOLO | VARCHAR2 (50 CHAR) | Determina il tipo di fatto di cui si fa carico al condannato in base alla classificazione di legge (articolo comma ed altro eventuale). |
| NOTE | VARCHAR2 (2000 CHAR) | Eventuali note aggiuntive. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| FLAG_SENTENZA_APPLICAZ_PENA | VARCHAR2 (1 CHAR) | S/N flag applicazione pena |
| FLAG_GIUDIZIO_ABBREVIATO | VARCHAR2 (1 CHAR) | S/N giudizio abbreviato |
| COD_BILANCIAMENTO_CIRCOSTANZE | VARCHAR2 (1 CHAR) | S/N bilanciamento circostanze |
| NOTE_BILANCIAMENTO | VARCHAR2 (2000 CHAR) | Note |
| COMMA_QUALIFICANTE | VARCHAR2 (2 CHAR). | Comma qualificante |



Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| CIR_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


# CIRCOSTANZA_CUMULO
La tabella contiene i dati relativi alle informazioni della Circostanza del Procedimento Cumulato.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_CIRCOSTANZA_CUMULO | NUMBER(38) | Sequence |
| COD_TIPO_CIRCOSTANZA | VARCHAR2(1) | Determina il tipo di circostanza. Deriva da dominio e può assumere i seguenti valori: C = Circostanza N = Norma. Associato al dominio TIPO_CIRCOSTANZA della tabella CG_REF_CODES |
| COD_FONTE | VARCHAR2(5) | FONTE GIURIDICA è il tipo di fonte giuridica relativo agli articoli di reato; es.: codice penale, legge. Associato al Dominio FONTE della Tabella CG_REF_CODES |
| ANNO_FONTE | NUMBER (4) | Anno della norma |
| NUMERO_FONTE | VARCHAR2(6) | Numero della norma |
| ARTICOLO | VARCHAR2(50) | Articolo della norma |
| COD_SOTTONUMERAZIONE | VARCHAR2(2) | Sottonumerazione articolo (bis, ter, ecc.) Associato al Dominio SOTTONUMERAZIONE della Tabella CG_REF_CODES |
| COMMA | VARCHAR2(10) | Comma dell'articolo trattato |
| COMMA_QUALIFICANTE | VARCHAR2(2) | Comma qualificante dell'articolo trattato |
| LETTERA | VARCHAR2(2) | Lettera dell'articolo trattato |
| NUMERO | VARCHAR2(2) | Eventuale numero dell'articolo trattato |
| NOTE | VARCHAR2(2000) | Eventuali note aggiuntive. |
| FLAG_SENTENZA_APPLICAZ_PENA | VARCHAR2(1) | Impostato a ‘S’, se trattasi di sentenza applicazione pena |
| FLAG_GIUDIZIO_ABBREVIATO | VARCHAR2(1) | Impostato a ‘S’, se trattasi di sentenza giudizio abbreviato |
| COD_BILANCIAMENTO_CIRCOSTANZE | VARCHAR2(1) | Valorizzato in caso di bilanciamento circostanza con RV_LOW_VALUE del dominio  BILANCIAMENTO_CIRCOSTANZE della Tabella CG_REF_CODES. |
| NOTE_BILANCIAMENTO | CHAR(2000) | Eventuali note |
| ID_CIRCOSTANZA_ORIGINE | NUMBER(38) | ID del record Circostanza di origine |
| FLAG_STATO | VARCHAR2(1) | E=estratto, M=modificato, C=Cancellato, I=Iscritto |
| MOTIVO_MODIFICA | VARCHAR2(2000) | Eventuale descrizione motivo modifica |
| TIT_ID_TITOLO_CUMULATO | NUMBER(38) | FK alla tabella TITOLO_CUMULATO |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |


# CIRCOSTANZA_SENTENZA_SIGE
La tabella contiene i dati relativi alle circostanze di una sentenza sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| CIR_ID_CIRCOSTANZA | NUMBER NOT NULL | Chiave primaria della tabella |
| FAS_SIGE_SEN_ID | NUMBER NOT NULL. | Chiave della sentenza |

# CIVILMENTE_OBBLIGATO
La tabella contiene i dati relativi al civilmente obbligato, utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_CIVILMENTE_OBBLIGATO | NUMBER(38) NOT NULL | Primary Key della tabella, legata alla sequence seq_civilmente_obbligato |
| COD_TUTORE | VARCHAR2(1) | Indica il codice del Tutore (E per Esercente Responsabilità Genitoriale, T per Tutore, -) |
| COD_PERSONA | VARCHAR2(1) NOT NULL | Indica il codice della persona (F per Fisica, G per Giuridica) |
| COD_FISCALE | VARCHAR2(16) | Indica il codice fiscale |
| COGNOME | VARCHAR2(100) | Indica il cognome |
| NOME | VARCHAR2(100) | Indica il nome |
| DENOMINAZIONE | VARCHAR2(200) | Indica la denominazione della persona giuridica |
| DATA_NASCITA | DATE | Indica la data di nascita |
| COD_COMUNE_NASCITA | VARCHAR2(6) | Indica il codice del comune di nascita |
| COD_PROVINCIA_NASCITA | VARCHAR2(2) | Indica il codice della provincia di nascita |
| COD_STATO_NASCITA | VARCHAR2(3) | Indica il codice dello stato di nascita |
| DESC_COMUNE_NASCITA_ESTERO | VARCHAR2(200) | Indica la descrizione del comune di nascita |
| SESSO | VARCHAR2(1) | Indica il sesso (M/F) |
| RAG_SOCIALE | VARCHAR2(5) | Indica la ragione sociale (Ente) della persona giuridica |
| COD_PROVINCIA | VARCHAR2(2) | Indica il codice della provincia della persona giuridica |
| IND_SEDE_LEGALE | VARCHAR2(200) | Indica l’indirizzo della sede legale della persona giuridica |
| IND_SEDE_OPERATIVA | VARCHAR2(200) | Indica l’indirizzo della sede operativa della persona giuridica |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Indica il Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Indica la Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11) | Indica il Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100) | Indica il Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Indica la Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(11) | Indica il Codice Ufficio Utente ultimo aggiornamento |
| COD_FISCALE_RAP | VARCHAR2(16) | Indica il codice fiscale o la partita IVA della persona giuridica |
| PEC | VARCHAR2(200) | Indica l’indirizzo di Posta Elettronica Certificata |
| E_MAIL | VARCHAR2(200) | Indica l’indirizzo di Posta Elettronica |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL | Foreign Key verso la tabella FASCICOLO_SIEP.ID_FASCICOLO_SIEP |



Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| CIVIL_OBBL_DIFENSORE | ID_CIVIL_OBBL_DIFENSORE_FK | ID_CIVIL_OBBL_DIFENSORE |

# CIVIL_OBBL_DIFENSORE
La tabella contiene i dati relativi al difensore del civilmente obbligato, utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_CIVIL_OBBL_DIFENSORE | NUMBER(38) NOT NULL | Primary Key della tabella |
| COD_TIPO_AVVOCATO | VARCHAR2(2) NOT NULL | Indica il Codice del Tipo di Avvocato (-, 01 per D'Ufficio, 02 per Di Fiducia, 03 per Della Fase di Giudizio) |
| DATA_INIZIO_VALIDITA | DATE NOT NULL | Indica la data di inizio validità |
| DATA_FINE_VALIDITA | DATE | Indica la data di fine validità |
| COD_MOTIVO_DESIGNAZIONE | VARCHAR2(4) | Indica il Codice del Motivo della Designazione (dominio “MOTIVO_DESIGNAZIONE” della tabella “CG_REF_CODES”) |
| COD_TIPO_AUTORITA | VARCHAR2(2) | Indica il Codice del Tipo della Autorità (dominio “TIPO_AUTORITA” della tabella “CG_REF_CODES”) |
| SEDE_TIPO_AUTORITA | VARCHAR2(6) | Indica il Codice della Sede del Tipo della Autorità |
| INDIRIZZO_TIPO_AUTORITA | VARCHAR2(300) | Indica l’Indirizzo della Sede del Tipo della Autorità |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Indica il Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Indica la Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11) | Indica il Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100) | Indica il Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Indica la Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(11) | Indica il Codice Ufficio Utente ultimo aggiornamento |
| AVV_ID_AVVOCATO | NUMBER(38) NOT NULL | Foreign Key verso la tabella AVVOCATO.ID_AVVOCATO |
| CIV_ID_CIVILMENTE_OBBLIGATO | NUMBER(38) NOT NULL | Foreign Key verso la tabella CIVILMENTE_OBBLIGATO. ID_CIVILMENTE_OBBLIGATO |
| NOTE | VARCHAR2(2000) | Indica il campo delle eventuali Note |
| COD_TIPO_AUTORITA_DIF | VARCHAR2(2) | Indica il Codice del Tipo della Autorità del Difensore (dominio “TIPO_AUTORITA” della tabella “CG_REF_CODES”) |
| SEDE_TIPO_AUTORITA_DIF | VARCHAR2(6) | Indica il Codice della Sede del Tipo della Autorità del Difensore |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2(4) | Indica il valore del campo ID_ISTITUTO_DETENZIONE della tabella ISTITUTO_DETENZIONE |



Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| CIV_ID_AVVOCATO_FK | AVV_ID_AVVOCATO | AVVOCATO.ID_AVVOCATO |
| ID_CIVIL_OBBL_DIFENSORE_FK | CIV_ID_CIVILMENTE_OBBLIGATO | CIVILMENTE_OBBLIGATO.ID_CIVILMENTE_OBBLIGATO |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |


# CODICI_SIES_NSC
La tabella contiene i dati relativi ai codici utilizzati per lo scambio dati tra sies e nsc. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| CO_DOMAIN | VARCHAR2 (100 CHAR) NOT NULL | Dominio della tabella |
| CO_CODCENTR | VARCHAR2 (100 CHAR) NOT NULL | Codice univoco |
| CO_NSC | VARCHAR2 (100 CHAR) NOT NULL | Codice di NSC |
| CO_NSC_DES | VARCHAR2 (240 CHAR) | Descrizione del codice NSC |
| CO_SIES | VARCHAR2  (100 CHAR) NOT NULL | Codice di SIE |
| CO_SIES_DES | VARCHAR2 (240 CHAR) | Descrizione del codice SIES |
| CO_VAL1 | VARCHAR2 (100 CHAR) |  |
| CO_VAL2 | VARCHAR2 (100 CHAR) |  |
| CO_VAL3 | VARCHAR2 (100 CHAR). |  |

# CODICI_UNIVOCI_MAPPATI
La tabella contiene i dati relativi ai codici contenuto/oggetto/esito che sono utilizzati dai fogli complementari per l’invio a nsc. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_CONTENUTO | VARCHAR2(10) | Contenuto del fascicolo SIUS |
| ID_OGGETTO | VARCHAR2(4 CHAR) | Oggetto del fascicolo SIUS |
| ID_ESITO | VARCHAR2(4 CHAR) | Esito del fascicolo SIUS |


# COLLEGIO
La tabella contiene i dati relativi al collegio. utilizzata dal sottosistema siep-sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_COLLEGIO | NUMBER NOT NULL | Chiave naturale della tabella. Legata alla sequence: COL_SEQ. |
| COD_COLLEGIO | VARCHAR2 (4 CHAR) NOT NULL | Codice del Collegio. |
| SEZ_ID_SEZIONE | NUMBER | ID della Sezione. |
| COD_UFFICIO_APPARTENENZA | VARCHAR2 (11 CHAR) NOT NULL | Codice dell’Ufficio di appartenenza. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| DATA_INIZIO_VALIDITA | DATE NOT NULL | Data inizio validità |
| DATA_FINE_VALIDITA. | DATE | Data fine validità |
| MAG_COD_MAGISTRATO | VARCHAR2 (6 CHAR) | Codice del Magistrato Presidente del collegio o se non scelto nella creazione del collegio, coincide con il magistrato assegnatario |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| COLLEGIO_ESPERTO | COL_ESP_COLLEGIO_FK | COL_ID_COLLEGIO |
| COLLEGIO_GIUDICE_POPOLARE | COL_GIU_POP_COLLEGIO_FK | COL_ID_COLLEGIO |
| COLLEGIO_MAGISTRATO | COL_MAG_COLLEGIO_FK | COL_ID_COLLEGIO |
| PROVVEDIMENTO_SIGE | PROV_COLLEGIO_FK | COL_ID_COLLEGIO |




# COLLEGIO_ESPERTO
La tabella è un’associativa tra la tabella Collegio ed Esperto. utilizzata dal sottosistema siep-sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COL_ID_COLLEGIO | NUMBER NOT NULL | ID del Collegio in relazione. |
| ESP_ID_ESPERTO | NUMBER NOT NULL | ID dell’Esperto in relazione |
| DATA_INSERIMENTO | DATE NOT NULL | Data di inserimento |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) NOT NULL | Codice dell’operatore che ha inserito il record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) NOT NULL. | Ufficio dell’operatore che ha inserito il record |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| COL_ESP_COLLEGIO_FK | COL_ID_COLLEGIO | (COLLEGIO.ID_COLLEGIO) |
| COL_ESP_ESPERTO_FK | ESP_ID_ESPERTO | (ESPERTO.ID_ESPERTO) |




# COLLEGIO_GIUDICE_POPOLARE
La tabella è un’associativa tra la tabella Collegio e Giudice Popolare. utilizzata dal sottosistema siep-sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COL_ID_COLLEGIO | NUMBER NOT NULL | Id Collegio Referenziale |
| GIU_POP_ID_GIUDICE_POPOLARE | NUMBER NOT NULL | Id Giudice Popolare Referenziale |
| DATA_INSERIMENTO | DATE NOT NULL | Data Inserimento |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) NOT NULL | Codice Operatore Inserimento |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) NOT NULL | Codice Ufficio Inserimento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| COL_GIU_POP_COLLEGIO_FK | COL_ID_COLLEGIO | (COLLEGIO.ID_COLLEGIO) |
| COL_GIU_POP_GIU_POP_FK | GIU_POP_ID_GIUDICE_POPOLARE | (GIUDICE_POPOLARE.ID_GIUDICE_POPOLARE) |




# COLLEGIO_MAGISTRATO
La tabella è un’associativa tra la tabella Collegio e Magistrato. utilizzata dal sottosistema siep-sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COL_ID_COLLEGIO | NUMBER NOT NULL | ID Collegio Referenziale |
| MAG_COD_MAGISTRATO | VARCHAR2 (6 CHAR) NOT NULL | Codice Magistrato Referenziale |
| DATA_INSERIMENTO | DATE NOT NULL | Data Inserimento |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) NOT NULL | Codice Operatore Inserimento |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) NOT NULL | Codice Ufficio Inserimento |
| COD_UFFICIO_APPARTENENZA | VARCHAR2 (11 CHAR). | Codice Ufficio Appartenenza |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| COL_MAG_COLLEGIO_FK | COL_ID_COLLEGIO | (COLLEGIO.ID_COLLEGIO) |
| COL_MAG_MAGISTRATO_FK | MAG_COD_MAGISTRATO | (MAGISTRATO.COD_MAGISTRATO) |
| COL_MAG_MAGISTRATO_FK | COD_UFFICIO_INSERIMENTO | (MAGISTRATO.COD_UFFICIO_APPARTENENZA) |



# COMPETENZA
La tabella contiene i dati relativi all’autorità competente relativa ad una sentenza. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_COMPETENZA | NUMBER NOT NULL | ID del Collegio in relazione. |
| COD_TIPO_PROVVEDIMENTO | VARCHAR2 (2 CHAR) NOT NULL | Tipo provvedimento |
| DATA_PROVVEDIMENTO | DATE NOT NULL | Data del provvedimento |
| COD_TIPO_AUTORITA_EMITTENTE | VARCHAR2 (6 CHAR) NOT NULL | Tipo di autorità emittente |
| COD_LUOGO_EMITTENTE | VARCHAR2 (6 CHAR) NOT NULL | Lugo dell’autorità emittente |
| NUM_SEZIONE_AUTORITA_EMITTENTE | VARCHAR2 (100 CHAR) | Numero della sezione dell’autorità emittente |
| ANNO_SENTENZA | NUMBER | Anno della sentenza |
| NUMERO_SENTENZA | VARCHAR2 (6 CHAR) | Numero della sentenza |
| DATA_IRREVOCABILITA | DATE NOT NULL | Data di irrevocabilità |
| SEN_ID_SENTENZA | NUMBER | Identificativo della sentenza |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| EVE_ID_EVENTO | NUMBER NOT NULL | Identificativo dell’evento |
| CHIAVE_ANNO | NUMBER | Anno del fascicolo |
| CHIAVE_UFFICIO | VARCHAR2 (11 CHAR) NOT NULL | Identificativo dell’ufficio |
| CHIAVE_PROGR | NUMBER | Progressivo del fascicolo |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| COD_TIPO_AUTORITA_COMP | VARCHAR2 (11 CHAR) NOT NULL | Tipo di autorità competente |
| COD_LUOGO_AUTORITA_COMP | VARCHAR2 (6 CHAR) NOT NULL | Sede dell’autorità competente |
| COD_UFFICIO_AUTORITA_COMP | VARCHAR2 (11 CHAR). | Ufficio dell’autorità competente |
| COD_TIPO_PROVVEDIMENTO_RICH | VARCHAR2(2) | Codice Tipo Provvedimento del Titolo Richiesto (Messaggio di Rigetto Trasferimento Atti per Competenza) |
| DATA_PROVVEDIMENTO_RICH | DATE | Data del Provvedimento del Titolo Richiesto (Messaggio di Rigetto Trasferimento Atti per Competenza) |
| COD_TIPO_AUTOR_EMITTENTE_RICH | VARCHAR2(6) | Codice Tipo Autorità Emittente del Titolo Richiesto (Messaggio di Rigetto Trasferimento Atti per Competenza) |
| COD_LUOGO_EMITTENTE_RICH | VARCHAR2(6) | Codice Comune Emittente del Titolo Richiesto (Messaggio di Rigetto Trasferimento Atti per Competenza) |
| NUM_SEZIONE_AUTOR_EMITT_RICH | VARCHAR2(100) | Numero sezione Autorità emittente del Titolo Richiesto (Messaggio di Rigetto Trasferimento Atti per Competenza) |
| ANNO_SENTENZA_RICH | NUMBER(4) | Anno Sentenza del Titolo Richiesto (Messaggio di Rigetto Trasferimento Atti per Competenza) |
| NUMERO_SENTENZA_RICH | VARCHAR2(6) | Numero Sentenza del Titolo Richiesto (Messaggio di Rigetto Trasferimento Atti per Competenza) |
| DATA_IRREVOCABILITA_RICH | DATE | Data Irrevocabilità del Titolo Richiesto (Messaggio di Rigetto Trasferimento Atti per Competenza) |
| COGNOME_SOGGETTO_RICH | VARCHAR2(35) | Cognome soggetto legato al Titolo Richiesto (Messaggio di Rigetto Trasferimento Atti per Competenza) |
| NOME_SOGGETTO_RICH | VARCHAR2(35) | Nome soggetto legato al Titolo Richiesto (Messaggio di Rigetto Trasferimento Atti per Competenza) |
| DATA_NASCITA_SOGGETTO_RICH | DATE | Data nascita del soggetto legato al Titolo Richiesto (Messaggio di Rigetto Trasferimento Atti per Competenza) |
| COD_STATO_NASC_SOGGETTO_RICH | VARCHAR2(3) | Codice stato nascita del soggetto legato al Titolo Richiesto (Messaggio di Rigetto Trasferimento Atti per Competenza) |
| COD_COMUNE_NASC_SOGGETTO_RICH | VARCHAR2(6) | Codice comune nascita del soggetto legato al Titolo Richiesto (Messaggio di Rigetto Trasferimento Atti per Competenza) |
| CODICECUI_SOGGETTO_RICH | VARCHAR2(7) | Codice AFIS del soggetto legato al Titolo Richiesto (Messaggio di Rigetto Trasferimento Atti per Competenza) |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| COMPETENZA_ID_EVENTO_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| COMPETENZA_ID_FASC_SIEP_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |



# COMPUTI_CUMULO
Per poter gestire correttamente le nuove funzionalità del cumulo, si è reso necessario aggiungere molte informazioni alla tabella. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| STAT_ID_STATO_ESEC_TIT_CUM | NUMBER(38) | FK alla tabella STAT_ESEC_TITOLO_CUMULATO |
| NUM_GIORNI_MAP | NUMBER(6) | Numero giorni Messa alla Prova di Presofferto |
| COD_TIPO_MISURA | VARCHAR2(2) | CG_REF_CODES.RV_DOMAIN= ‘TIPO_MISURA_CAUTELARE’ |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2(4) | ID dell’ISTITUTO_DETENZIONE |
| ALTRO_LUOGO_DETENZIONE | VARCHAR2(1000) | Descrizione altro luogo |
| DATA_RICEZIONE _PROVV | DATE | Data ricezione provvedimento Altra Autorità per annotazione pagamento pena pecuniaria |
| DATA_EMISSIONE_PROVV | DATE | Data emissione provvedimento Altra Autorità per annotazione pagamento pena pecuniaria |
| ANNO_PROVV | NUMBER(4) | Anno provvedimento Altra Autorità per annotazione pagamento pena pecuniaria |
| PROGR_PROVV | NUMBER(38) | Numero provvedimento Altra Autorità per annotazione pagamento pena pecuniaria |
| COD_UFFICIO_EMITTENTE_PROVV | VARCHAR2(11) | Codice Ufficio che ha emesso provvedimento pagamento pena pecuniaria |
| COD_LUOGO_UFFICIO_PROVV | VARCHAR2(6) | Codice Comune sede Ufficio che ha emesso provvedimento pagamento pena pecuniaria |
| SEZIONE_PROVV | VARCHAR2(50) | Sezione Ufficio che ha emesso provvedimento pagamento pena pecuniaria |
| ANNO_PROC | NUMBER(4) | Anno procedimento pagamento pena pecuniaria |
| PROGR_PROC | NUMBER(38) | Numero procedimento pagamento pena pecuniaria |
| ANNO_REGE_PM | NUMBER(4) | Anno Registro Notizie Reato |
| NUMERO_REGE_PM | VARCHAR2(6) | Numero Registro Notizie Reato |
| COD_TIPO_UFFICIO_PM | VARCHAR2(240) | Codice Tipo Ufficio del Registro Notizie Reato |
| COD_SEDE_UFFICIO_PM | VARCHAR2(6) | Codice Comune sede Ufficio del Registro Notizie Reato |
| ANNO_BDMC | NUMBER(4) | Anno procedimento Banca Dati Misure Cautelari |
| NUMERO_BDMC | VARCHAR2(6) | Numero procedimento Banca Dati Misure Cautelari |
| ANNO_REGE | NUMBER(4) | Note inserite dall''operatore in fase di Modifica, Cancellazione, Iscrizione |
| NUMERO_REGE | VARCHAR2(8) | Numero Registro Generale |
| TIPO_REGE | VARCHAR2(240) | Codice Tipo Registro Generale |
| TIPO_AUT_REGE | VARCHAR2(6) | Codice Tipo Autorità Registro Generale |
| COD_SEDE_REGE | VARCHAR2(6) | Codice Comune sede Autorità Registro Generale |
| DATA_REGE | DATE | Data iscrizione Registro Generale |
| CHIAVE_ANNO_SIEP | NUMBER(4) | Anno Procedimento SIEP |
| CHIAVE_NUMERO_SIEP | NUMBER(38) | Numero Procedimento SIEP |
| CHIAVE_UFFICIO_SIEP | VARCHAR2(11) | Codice Ufficio Procedimento SIEP |
| ANNO_SENTENZA | NUMBER(4) | Anno sentenza riferimento Altro Titolo |
| NUMERO_SENTENZA | VARCHAR2(8) | Numero sentenza riferimento Altro Titolo |
| DATA_SENTENZA | DATE | Data sentenza riferimento Altro Titolo |
| COD_TIPO_AUT_EMITT_SENTENZA | VARCHAR2(6) | Codice Tipo Ufficio sentenza riferimento Altro Titolo |
| COD_LUOGO_EMITTENTE_SENTENZA | VARCHAR2(6) | Codice Comune sede Ufficio sentenza riferimento Altro Titolo |
| REA_ID_REATO_CUM | NUMBER(38) | FK alla tabella REATO_CUMULO |
| COD_FONTE | VARCHAR2(5) | Codice Fonte estremi legislativi Depenalizzazione |
| ANNO_FONTE | NUMBER(4) | Anno Fonte estremi legislativi Depenalizzazione |
| NUMERO_FONTE | VARCHAR2(6) | Numero Fonte estremi legislativi Depenalizzazione |
| COD_SOTTONUMERAZIONE | VARCHAR2(2) | Codice sottonumerazione Fonte estremi legislativi Depenalizzazione |
| COMMA | VARCHAR2(10) | Comma Fonte estremi legislativi Depenalizzazione |
| LETTERA | VARCHAR2(2) | Lettera Fonte estremi legislativi Depenalizzazione |
| NUMERO | VARCHAR2(2) | Numero Fonte estremi legislativi Depenalizzazione |
| ARTICOLO | VARCHAR2(50) | Articolo Fonte estremi legislativi Depenalizzazione |
| COD_TIPO_REGISTRO_ORDINANZA | VARCHAR2(4) | CG_REF_CODES.RV_DOMAIN= ‘OGGETTO_SOSPENSIONI’ |
| DATA_SOSPENSIONE_INTERRUZIONE | DATE | Data provvedimento sospensione |
| COD_OGGETTO_DECISIONE | VARCHAR2(4) | CG_REF_CODES.RV_DOMAIN= ‘CONTENUTO_SIEP’ |
| PROTOCOLLO | VARCHAR2(100) | Protocollo provvedimento interruzione del GE |
| ALTRA_AUTORITA | VARCHAR2(300) | Descrizione Autorità del provvedimento interruzione del GE |
| ALTRO_LUOGO | VARCHAR2(2000) | Descrizione sede Autorità del provvedimento interruzione del GE |
| LUOGO_ESEC_MISURA | VARCHAR2(400) | Luogo esecuzione misura alternativa |
| DATA_INIZIO_MISURA | DATE | Data inizio esecuzione misura alternativa |
| DATA_FINE_MISURA | DATE | Data fine esecuzione misura alternativa |
| NUM_ANNI_MISURA | NUMBER(2) | Numero anni  misura alternativa |
| NUM_MESI_MISURA | NUMBER(2) | Numero mesi  misura alternativa |
| NUM_GIORNI_MISURA | NUMBER(4) | Numero giorni  misura alternativa |
| DATA_INIZIO_REVOCA | DATE | Data inizio revoca misura alternativa |
| NUM_ANNI_REVOCA_RECLUSIONE | NUMBER(2) | Numero anni reclusione misura alternativa revocata |
| NUM_MESI_REVOCA_RECLUSIONE | NUMBER(2) | Numero mesi  reclusione misura alternativa revocata |
| NUM_GIORNI_REVOCA_RECLUSIONE | NUMBER(4) | Numero giorni  reclusione misura alternativa revocata |
| NUM_ANNI_REVOCA_ARRESTO | NUMBER(2) | Numero anni  arresto misura alternativa revocata |
| NUM_MESI_REVOCA_ARRESTO | NUMBER(2) | Numero mesi arresto  misura alternativa revocata |
| NUM_GIORNI_REVOCA_ARRESTO | NUMBER(4) | Numero giorni arresto  misura alternativa revocata |
| DATA_INGRESSO_ISTITUTO | DATE | Data ingresso istituto in caso di sospensione misura alternativa |
| DATA_SCARCERAZIONE | DATE | Data scarcerazione in caso di sospensione misura alternativa |
| FLAG_DECISIONE_TRIBUNALE | VARCHAR2(1) | ‘S’ in caso di decisione del TDS su differimento pena |
| COD_TDS_COMPETENTE | VARCHAR2(11) | Codice Ufficio TDS che ha emesso decisione su differimento pena |
| COD_TIPO_PROVV | VARCHAR2(2) | Codice Tipo Provvedimento (Ordinanza/Decreto) in caso di annotazione Ridet. pena per Provvedimento altro ufficio |



# COMUNE
La tabella contiene i dati relativi ai comuni italiani. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_COMUNE | VARCHAR2 (6 CHAR) NOT NULL | Codice di 6 cifre indicante il comune |
| COD_PROVINCIA | VARCHAR2 (2 CHAR) NOT NULL | Provincia di appartenenza del comune |
| DESCRIZIONE | VARCHAR2 (250 CHAR) NOT NULL | Nome del comune |
| CAP | VARCHAR2 (5 CHAR) | CAP principale del comune. |
| DATA_CARICAMENTO_REGE | DATE | Data di caricamento da Re.Ge |
| COD_SEDE_GIUDIZIARIA | VARCHAR2 (3 CHAR). | Codice del casellario competente. |




# CONTINUAZIONE
La tabella contiene i dati relativi alla continuazione tra sentenze. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_CONTINUAZIONE | NUMBER NOT NULL | Chiave numerica naturale per la gestione dei record in tabella. Legata a Sequence CIR_SEQ. |
| PROGR_CONTINUAZIONE | NUMBER NOT NULL | Numero progressivo relativo alla continuazione. |
| COD_TIPO_CONTINUAZIONE | VARCHAR2 (1 CHAR) | Tipo continuazione. Deriva da dominio e può assumere i seguenti valori: PENA COMPLESSIVA RITENUTA LA CONTINUAZIONE; PENA IN AUMENTO RITENUTA LA CONTINUAZIONE.
Associato al dominio |
| COD_TIPO_AUTORITA | VARCHAR2 (6 CHAR) | Indica il tipo di autorità che ha emesso la sentenza relativa alla pena. Collegato al dominio AUTORITA_CUMULO della tabella CG_REF_CODES. |
| COD_LUOGO_AUTORITA | VARCHAR2 (6 CHAR) | Indica il luogo riferito al tipo di autorità che ha emesso la sentenza relativa alla pena. |
| DATA_SENTENZA | DATE | Data emissione della sentenza |
| ANNO_SENTENZA | NUMBER | Anno della sentenza fa parte della chiave identificante una sentenza |
| NUM_SENTENZA | VARCHAR2 (6 CHAR) | Numero della sentenza fa parte della chiave identificante una sentenza |
| ANNO_REGE_PM | NUMBER | Compone la chiave del numero di registro generale del fascicolo RE.GE presso il PM |
| NUM_REGE_PM | VARCHAR2 (6 CHAR) | Compone la chiave del numero di registro generale del fascicolo RE.GE presso il PM |
| ANNO_REGE_GIP | NUMBER | Compone la chiave del numero di registro generale del fascicolo RE.GE presso il GIP |
| NUM_REGE_GIP | VARCHAR2 (6 CHAR) | Compone la chiave del numero di registro generale del fascicolo RE.GE presso il GIP |
| ANNO_REGE_DIB | NUMBER | Compone la chiave del numero di registro generale del fascicolo RE.GE presso il Tribunale |
| NUM_REGE_DIB | VARCHAR2 (6 CHAR) | Compone la chiave del numero di registro generale del fascicolo RE.GE presso il Tribunale |
| ANNO_REGE_CAS | NUMBER | Compone la chiave del numero di registro generale del fascicolo RE.GE presso la Corte d'Assise |
| NUM_REGE_CAS | VARCHAR2 (6 CHAR) | Compone la chiave del numero di registro generale del fascicolo RE.GE presso la Corte d'Assise |
| ANNO_REGE_CAP | NUMBER | Compone la chiave del numero di registro generale del fascicolo RE.GE presso la Corte d'Appello |
| NUM_REGE_CAP | VARCHAR2 (6 CHAR) | Compone la chiave del numero di registro generale del fascicolo RE.GE presso la Corte d'Appello |
| ANNO_REGE_CASAP | NUMBER | Compone la chiave del numero di registro generale del fascicolo RE.GE presso la Corte d'Assise d'Appello |
| NUM_REGE_CASAP | VARCHAR2 (6 CHAR) | Compone la chiave del numero di registro generale del fascicolo RE.GE presso la Corte d'Assise d'Appello |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| PEN_COM_ID_PENA_COMPLESSIVA | NUMBER NOT NULL | Identificativo delle pena complessiva |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- | --- |
| CON_PEN_COM_FK | PEN_COM_ID_PENA_COMPLESSIVA | (PENA_COMPLESSIVA.ID_PENA_COMPLESSIVA) | (PENA_COMPLESSIVA.ID_PENA_COMPLESSIVA) |







# CONTINUAZIONE_CUMULO
La tabella contiene i dati relativi alla continuazione tra provvedimenti di cumulo. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_CONTINUAZIONE_CUM | NUMBER(38) | Chiave primaria della tabella |
| PROGR_CONTINUAZIONE | NUMBER(38) | Progressivo della continuazione |
| COD_TIPO_CONTINUAZIONE | VARCHAR2(1) | CG_REF_CODES.RV_DOMAIN= ’TIPO_CONTINUAZIONE’ |
| COD_TIPO_AUTORITA | VARCHAR2(6) | CG_REF_CODES.RV_DOMAIN= ’TIPO_UFFICIO’ |
| COD_LUOGO_AUTORITA | VARCHAR2(6) | Codice Luogo Autorità (COD_COMUNE) |
| DATA_SENTENZA | DATE | Data Sentenza |
| ANNO_SENTENZA | NUMBER(4) | Anno Sentenza |
| NUM_SENTENZA | VARCHAR2(8) | Numero Sentenza |
| ANNO_REGE_PM | NUMBER(4) | Anno Registro N.R. |
| NUM_REGE_PM | VARCHAR2(6) | Numero Registro N.R. |
| ANNO_REG_GEN | NUMBER(4) | Anno Registro Gen. |
| NUMERO_REG_GEN | VARCHAR2(8) | Numero Registro Gen. |
| TIPO_REG_GEN | VARCHAR2(240) | Tipo Registro Gen. |
| PC_ID_PENA_COMPLESSIVA_CUM | NUMBER(38) | FK alla tabella PENA_COMPLESSIVA_CUM |
| TIT_ID_TITOLO_CUMULATO_CONT | NUMBER(38) | Riferimento Al Titolo_Cumulato in Continuazione |
| FLAG_STATO | VARCHAR2(1) | E=estratto M=modificato C=Cancellato I=Iscritto |
| MOTIVO_MODIFICA | VARCHAR2(2000) | Note inserite dall''operatore in fase di Modifica Cancellazione Iscrizione |
| TIT_ID_TITOLO_CUMULATO | NUMBER(38) | FK alla tabella TITOLO_CUMULATO |
| ID_CONTINUAZIONE_ORIGINE | NUMBER(38) | Eventuale ID del record CONTINUAZIONE da cui è stato derivato questo record |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |

# CSSA
tabella contenente i dati dei Centri di Servizio Sociale per Adulti. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_CSSA | NUMBER NOT NULL | Chiave primaria del CSSA per la sua identificazione. |
| TIPO | VARCHAR2 (10 CHAR) | Indica il tipo di CSSA nel caso in cui ce ne siano di diversi |
| COMUNE | VARCHAR2 (35 CHAR) | Comune di appartenenza. |
| INDIRIZZO | VARCHAR2 (300 CHAR) | Indirizzo del CSSA |
| E_MAIL | VARCHAR2 (200 CHAR) | Eventuale indirizzo e-mail |
| FAX | VARCHAR2 (20 CHAR) | Numero di fax |
| TEL | VARCHAR2 (20 CHAR) | Numero di telefono |
| INCARICO | VARCHAR2 (30 CHAR) | Incarico riferito al contenuto del campo cognome e nome. Es. "Direttore" |
| TITOLO | VARCHAR2 (30 CHAR) | Titolo riferito al contenuto del campo cognome e nome |
| NOME | VARCHAR2 (35 CHAR) | Nome di un referente |
| COGNOME | VARCHAR2 (50 CHAR) | Cognome di un referente |
| DATA_CARICAMENTO | DATE | Data di caricamento dei dati forniti da DGSIA |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| CSSA | NOTIFICA | NOT_1_CSS_FK |



# CUMULO
tabella contenente i dati del cumulo. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_CUMULO | NUMBER NOT NULL | Chiave naturale numerica per la gestione dei record in tabella. |
| ID_FASCICOLO_SIEP_CUMULATO | NUMBER | Chiave del fascicolo cumulato. L'id del fascicolo è ricavato utilizzando le informazioni dei campi successivi che compongono la vera chiave del fascicolo. Il fatto di riportare tutti i campi identificativi del  fascicolo cumulato è dovuto alla necessità di avere diversi modi di accesso a tale fascicolo. Infatti un utente che chiede ad un ufficio  l'invio di un fascicolo scriverà ANNO/PROGRESSIVO e selezionerà l'ufficio tramite TIPO E LUOGO mentre il sistema nel fare le sue ricerche sfrutterà l'ID del fascicolo (utile anche per tutte le relazioni). |
| CHIAVE_ANNO_FAS_CUMULATO | NUMBER | Chiave parziale del fascicolo cumulato |
| CHIAVE_PROGR_FAS_CUMULATO | NUMBER | Chiave parziale del fascicolo cumulato |
| COD_TIPO_UFFICIO_FAS_CUMULATO | VARCHAR2 (6 CHAR) | Codice del tipo dell'ufficio che possiede il fascicolo da cumulare. |
| COD_LUOGO_UFFICIO_FAS_CUMULATO | VARCHAR2 (6 CHAR) | Codice del comune dell'ufficio che possiede il fascicolo da cumulare. |
| COD_UFFICIO_FAS_CUMULATO | VARCHAR2 (11 CHAR) | Codice dell'ufficio a cui appartiene il fascicolo cumulato. Insieme all'anno ed al progressivo compone la chiave del fascicolo cumulato. |
| COD_TIPO_CUMULO | VARCHAR2 (2 CHAR) | Codice indicante le varie tipologie di cumulo. Deriva da dominio. Al momento si trova ancora in fase di analisi e quindi non è possibile riportare un esempio. |
| DATA_RICHIESTA_FASCICOLO | DATE | Data della richiesta da parte del cumulante del fascicolo da cumulare. La richiesta non implica necessariamente che si dia seguito ad un cumulo ma semplicemente che siano inviate o estratte tutte le informazioni che dovranno essere vagliate dal richiedente dei fascicoli in generale un PM di esecuzione. |
| DATA_PERVENIMENTO_FASCICOLO | DATE | Data di arrivo di un fascicolo cumulato richiesto. |
| DATA_CUMULO | DATE | Data di effettivo inizio cumulo. |
| COD_MOTIVO_SOSPENSIONE_CUM ULO | VARCHAR2 (2 CHAR) | Codice indicante le varie motivazioni della sospensione di un cumulo. |
| DATA_SOSPENSIONE_CUMULO | DATE | Data della sospensione di un cumulo. |
| NOTE | VARCHAR2 (2000 CHAR) | Note aggiuntive alle informazioni già inserite. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL | Identificativo del fascicolo SIEP |
| FLAG_TIPO_STAMPA | VARCHAR2 (1 CHAR) DEFAULT '-' | tipologia di stampa richiesta (previste per il momento solo Libero/Detenuto/Misura Alternativa). |
| SEN_ID_SENTENZA | NUMBER NOT NULL | Identificativo della sentenza |
| FLAG_VALIDATO | VARCHAR2 (1 CHAR) DEFAULT 'N' | Indica se il cumulo è validato o meno |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| PRIMO_CUMULO | VARCHAR2 (1 CHAR) | Indica se trattasi di primo cumulo |
| ISTR_ID_ISTRUTTORIA_CUMULO | NUMBER | Identificativo dell’istruttoria a cui il cumulo appartiene |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| CUM_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| CUM_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| PENA_CUMULO | PEN_CUM_CUM_FK | CUM_ID_CUMULO |
| ULTERIORE_SANZIONE_CUMULO | ULT_SAN_CUM_ID_CUM | CUM_ID_CUMULO |



# CURATORE
tabella contenente i dati anagrafici dei curatori fallimentari. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_CURATORE | NUMBER NOT NULL | ID Curatore |
| COGNOME | VARCHAR2 (50 CHAR) NOT NULL | Cognome |
| NOME | VARCHAR2 (50 CHAR) | Nome |
| INDIRIZZO | VARCHAR2 (200 CHAR) | Indirizzo |
| TELEFONO | VARCHAR2 (12 CHAR) | Telefono |
| COD_UFFICIO_APPARTENENZA | VARCHAR2 (11 CHAR) NOT NULL | Codice Ufficio di Appartenenza |
| EMAIL | VARCHAR2 (100 CHAR) | Email |
| FAX | VARCHAR2 (12 CHAR) | Fax |
| CELLULARE | VARCHAR2 (12 CHAR) | Cellulare |
| DATA_INIZIO_VALIDITA | DATE NOT NULL | Data Inizio Validità |
| DATA_FINE_VALIDITA | DATE | Data Fine Validità |
| FLAG_STATO | VARCHAR2 (1 CHAR) | Flag di Stato |
| CODICE_FISCALE | VARCHAR2 (16 CHAR) | Codice Fiscale |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| CURATORE_SIUS | CURATORE_CUR_SIUS_FK | CUR_ID_CURATORE |



# CURATORE_SIUS
tabella associativa tra la tabella Curatore e Fascicolo_SIUS. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| DATA_INIZIO | DATE NOT NULL | Chiave naturale numerica per la gestione dei record in tabella. |
| DATA_FINE | DATE |  |
| FLAG_TIPO | VARCHAR2 (1 CHAR) NOT NULL | C=Curatore T=Tutore |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| CUR_ID_CURATORE | NUMBER NOT NULL | ID del record CURATORE |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER NOT NULL. | ID del record FASCICOLO_SIUS |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| CURATORE_CUR_SIUS_FK | CUR_ID_CURATORE | (CURATORE.ID_CURATORE) |
| CUR_SIUS_FK | FAS_SIU_ID_FASCICOLO_SIUS | (FASCICOLO_SIUS.ID_FASCICOLO_SIUS) |


# DATI_FINALI_CUMULO
tabella contenente i dati finali del cumulo. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_DATI_FINALI_CUMULO | NUMBER(38) | Chiave naturale numerica per la gestione dei record in tabella. |
| TIPO_UFFICIO_EMISSIONE | VARCHAR2(2) | ‘03’=Emesso con Ordinanza; ‘04’=Emesso da Ufficio |
| DATA_PROVVEDIMENTO | DATE | Data Provvedimento |
| COD_TIPO_PROVVEDIMENTO | VARCHAR2(2) | Codice Tipo Provvedimento |
| ANNO_PROVVEDIMENTO | NUMBER(4) | Anno Provvedimento |
| NUMERO_PROVVEDIMENTO | NUMBER(9) | Numero Provvedimento |
| COD_TIPO_UFFICIO_EMITTENTE | VARCHAR2(10) | Codice Tipo Ufficio Emittente |
| COD_LUOGO_UFFICIO_EMITTENTE | VARCHAR2(6) | Codice Comune Ufficio Emittente |
| SEZIONE_UFFICIO_EMITTENTE | VARCHAR2(200) | Sezione Ufficio Emittente |
| FLAG_CREA_FASCICOLO_MS | VARCHAR2(1) | Impostato a ‘S’ se è stato creato fascicolo di Misure Sicurezza |
| FLAG_PRIMO_CUMULO | VARCHAR2(1) | FK alla tabella TITOLO_CUMULATO |
| FAS_SIE_ID_FASCICOLO_SIEP_MS | NUMBER(38) | Eventuale ID del record MISURA_SICUREZZA da cui è stato derivato questo record |
| EVE_ID_EVENTO | NUMBER(38) | ‘A’ se misura annullata |
| ISTR_ID_ISTRUTTORIA_CUMULO | NUMBER(38) | Data Fine Validità |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |




# DATI_FINALI_ULTERIORI_SANZIONI
tabella contenente i dati finali relativi alle ulteriori sanzioni date per il lavoro di pubblica utilità. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_DATI_FINALI_ULTERIORI_SANZ | NUMBER(38) | Chiave naturale numerica per la gestione dei record in tabella. |
| COD_TIPO_ULTERIORE_SANZIONE | VARCHAR2(2) | CG_REF_CODES.RV_DOMAIN= ‘TIPO_ULTERIORE_SANZIONE’ |
| NUM_ANNI | NUMBER(4) | Numero Anni |
| NUM_MESI | NUMBER(4) | Numero Mesi |
| NUM_GIORNI | NUMBER(4) | Numero Giorni |
| MULTA | NUMBER(162) | Importo Multa |
| AMMENDA | NUMBER(162) | Importo Ammenda |
| FLAG_ESPUL_PERP | VARCHAR2(4) | P=Perpetua T=Temporanea |
| COD_TIPO_LPU | VARCHAR2(10) | CG_REF_CODES.RV_DOMAIN= ‘TIPO_SANZIONE_SOSTITUTIVA_LPU’ |
| NUM_ORE_TOT | NUMBER(4) | numero ore complessive LPU |
| NUM_ORE_SETT | NUMBER(4) | ore settimanali LPU |
| COD_FREQ_SETT | NUMBER(1) | LPU: 0=frequenza NON determinata 1 = frequenza determinata |
| DAT_ID_DATI_FINALI_CUMULO | NUMBER(38) | FK alla tabella DATI_FINALI_CUMULO |
| ISTR_ID_ISTRUTTORIA_CUMULO | NUMBER(38) | FK alla tabella ISTRUTTORIA_CUMULO |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |





# DATI_PROVVEDIMENTO_SIGE
tabella contenente alcuni dati relativi al provvedimento sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_DATI_PROVVEDIMENTO_SIGE | NUMBER NOT NULL | Chiave primaria. |
| COD_TIPO_DATI_PROV | VARCHAR2 (4 CHAR) NOT NULL | Codice tipo dati dal DOMINIO = DATI_PROVVEDIMENTO_SIGE nella CG_REF_CODES |
| NOTE | VARCHAR2 (2000 CHAR) | Ulteriore descrizione. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) NOT NULL | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE NOT NULL | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) NOT NULL | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| TEN_ID_TENORE_SIGE | NUMBER NOT NULL | Chiave esterna a TENORE_SIGE. |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| TEN_ID_TEN_SIGE_FK | TEN_ID_TENORE_SIGE | (TENORE_SIGE.ID_TENORE_SIGE) |





# DECRETO_ORDINANZA_SIEP
tabella contenente i dati relativi all’ordinanza di siep. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_DECRETO_ORDINANZA_SIEP | NUMBER NOT NULL | Chiave naturale interna legata a Sequence DEC_ORD_SEQ |
| DATA_RICEZIONE_PROVVEDIMENTO | DATE | Data di ricezione del Provvedimento. |
| DATA_EMISSIONE_PROVVEDIMENTO | DATE | Data di emissione del Provvedimento. |
| COD_TIPO_REGISTRO_ORDINANZA | VARCHAR2 (4 CHAR) | Identifica se l'ordinanza è stata emessa dalla Sorveglianza oppure dal Giudice di Esecuzione. |
| ANNO_REGISTRO | NUMBER | Anno di Registro. |
| NUM_REGISTRO | NUMBER | Progressivo di registro. |
| ANNO_PROVVEDIMENTO | NUMBER | Anno del provvedimento (Decreto/Ordinanza). |
| NUM_PROVVEDIMENTO | NUMBER | Numero del provvedimento (Decreto/Ordinanza). |
| COD_TIPO_PROVVEDIMENTO | VARCHAR2 (2 CHAR) | Codifica del Tipo Provvedimento. Associato al dominio TIPO_PROVVEDIMENTO. |
| COD_TIPO_AUTORITA_EMITTENTE | VARCHAR2 (6 CHAR) | Codifica Tipo Autorità Emittente. |
| COD_LUOGO_EMITTENTE | VARCHAR2 (6 CHAR) | Codice Comune del luogo emittente. |
| DATA_SOSPENSIONE_ESECUZIONE | DATE | Data di sospensione dell'esecuzione. |
| DATA_DIFFERIMENTO | DATE | Data del differimento della pena. |
| DATA_RINVIO | DATE | Data di rinvio provvedimento. |
| DATA_FINE_INTERRUZIONE | DATE | Data di fine interruzione. |
| DATA_DEPOSITO_ISTANZA | DATE | Data di deposito dell'istanza. |
| DATA_INTERRUZIONE_PENA | DATE | Data di interruzione della pena. |
| COD_OGGETTO_DECISIONE | VARCHAR2 (4 CHAR) | Codifica dell'oggetto Procedimento sottoposto a decisione. Associato al dominio OGGETTO_PROCEDIMENTO di CG_REF_CODES. |
| MOTIVAZIONI | VARCHAR2 (2000 CHAR) | Campo di testo libero. Contiene le Motivazioni del provvedimento. |
| NOTE | VARCHAR2 (2000 CHAR) | Eventuali note aggiuntive. |
| FLAG_SCARCERARE_SCARCERATO | VARCHAR2 (2 CHAR) | Codifica del Stato di Carcerazione. Associato al dominio FLAG_SCARCERATO_SCARCERARE. |
| FLAG_PRESENTANTE_ISTANZA | VARCHAR2 (1 CHAR) | Codifica del tipo di soggetto che presenta l'Istanza (Difensore interessato...) Associato al FLAG_ISTANZA. |
| COD_CONTENUTO_DECRETO | VARCHAR2 (2 CHAR) | Codifica del contenuto del Decreto (Art. 667 Cpp. Grazia...). Associato al dominio CONTENUTO_DECRETO. |
| COD_OGGETTO_PROCEDIMENTO | VARCHAR2 (4 CHAR) | Codifica della motivazione del provvedimento . Associato al dominio MOTIVO_PROVVEDIMENTO di CG_REF_CODES. |
| FLAG_DATA_INTERRUZIONE_INV ALID | VARCHAR2 (1 CHAR) | Identifica se la data di interruzione della pena è valida oppure no. |
| PROTOCOLLO | VARCHAR2 (100 CHAR) | Identifica un protocollo(di un documento) proveniente da altre autorità (es. vigili urbani che hanno riscontrato il motivo dell'interruzione della pena). |
| ALTRA_AUTORITA | VARCHAR2 (300 CHAR) | Campo descrittivo che identifica una tipologia di autorità diversa da quelle della cg_ref_codes (es. vigili del fuoco). |
| ALTRO_LUOGO | VARCHAR2 (2000 CHAR) | Campo descrittivo che identifica un luogo diverso dalla lista comuni (es. frazione di comune). |
| ID_EVENTO_GENERATO | NUMBER | Codice Identificativo dell'Evento generato. |
| FLAG_ELABORATO | VARCHAR2 (1 CHAR) | Indica se il provvedimento è stato o meno elaborato. Associato al Dominio FLAG_SI_NO. |
| DATA_ESPULSIONE | DATE | Data di espulsione del soggetto. |
| FLAG_DECISIONE_TRIBUNALE | VARCHAR2 (1 CHAR) | Identifica se c'è stata o no la decisione del TdS. |
| COD_ESITO | VARCHAR2 (4 CHAR) | Uguale  a esito_provvedimento. |
| NUM_ANNI_RINVIO | NUMBER | Anni di rinvio della pena da espiare. |
| NUM_MESI_RINVIO | NUMBER | Mesi di rinvio della pena da espiare. |
| NUM_GIORNI_RINVIO | NUMBER | Giorni di rinvio della pena da espiare. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Data di inserimento del record |
| DATA_INSERIMENTO | DATE | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Data di aggiornamento del record |
| DATA_AGGIORNAMENTO | DATE | Ufficio dell’operatore che ha aggiornato il record |
| DATA_REVOCA_SOSPENSIONE | DATE | Data revoca delle sospensione |
| FAS_SIE_ID_FASCICOLO_SIEP. | NUMBER | Identificativo del fascicolo SIEP |
| ANNO_REG_GEN | NUMBER(4) | Anno di registro generale |
| NUMERO_REG_GEN | NUMBER(6) | Numero del registro generale |
| TIPO_REG_GEN | VARCHAR2(5) | Tipo registro generale |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| DEC_SIE_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


# DEPOSITO_DECRETO
tabella contenente i dati relativi al deposito del decreto. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_DEPOSITO_DECRETO | NUMBER NOT NULL | Chiave naturale interna legata a Sequence DEP_DEC_SEQ |
| ANNO_S72 | NUMBER | Anno del Registro S72. |
| NUM_S72 | NUMBER | Numero del Registro S72. |
| COD_TIPO_DECRETO | VARCHAR2 (2 CHAR) | Codifica del Tipo Decreto. Associato al Dominio TIPO_DECRETO |
| DATA_EMISSIONE | DATE | Data Emissione del Decreto. |
| DATA_DEPOSITO | DATE | Data Deposito del Decreto. |
| COD_MAGISTRATO | VARCHAR2 (6 CHAR) | Codice del Magistrato che ha emesso il Decreto. |
| ALTRI_DESTINATARI | VARCHAR2 (200 CHAR) | Indica altri destinatari |
| DATA_PARERE_PG | DATE | Data del parere della Procura Generale |
| COD_TIPO_PARERE_PG | VARCHAR2 (2 CHAR) | Tipologia di parere della Procura Generale |
| DATA_RICORSO_IMPUGNAZIONE | DATE | Data del ricorso dell’impugnazione |
| DATA_INVIO_ATTI_IMPUGNAZIONE | DATE | Data invio atti dell’impugnazione |
| DATA_SENTENZA_IMPUGNAZIONE | DATE | Data della sentenza dell’impugnazione |
| TENORE_SENTENZA_IMPUGNAZIONE | VARCHAR2 (2 CHAR) | Codice del tenore della sentenza dell’impugnazione |
| NOTE | VARCHAR2 (2000 CHAR) | Note |
| SENTENZE_RIFERIMENTO | VARCHAR2 (200 CHAR) | Descrizione contenente le sentenze di riferimento |
| COD_PROCURA_ESECUZIONE | VARCHAR2 (11 CHAR) | Codice della Procura dell’esecuzione |
| COD_UFFICIO_COMP | VARCHAR2 (11 CHAR) | Identificativo dell’ufficio di competenza |
| COD_TDS_COMP | VARCHAR2 (11 CHAR) | Tribunale di Sorveglianza di competenza |
| STATUS_PERSONA | VARCHAR2 (2 CHAR) | Status della persona |
| TOT_ORE_RAGGIUNGIMENTO | VARCHAR2 (3 CHAR) | Numero totale di ore del raggiungimento |
| ANNO_PROC_REVOCATO | NUMBER | Anno del procedimento revocato |
| UFFICIO_PROC_REVOCATO | VARCHAR2 (11 CHAR) | Codice dell’ufficio che ha revocato il procedimento |
| PROGR_PROC_REVOCATO | NUMBER | Identificativo del procedimento revocato |
| LUOGO_SVOLGIMENTO_PROVA | VARCHAR2 (2000 CHAR) | Descrizione del luogo in cui si svolge la prova |
| ID_EVENTO_GENERATO | NUMBER | Identificativo dell’evento |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| IST_DET_ID_ISTITUTO_DETENZION E | VARCHAR2 (4 CHAR) | Identificativo dell’istituto di detenzione |
| GEN_PRID_GENERALE_PROCEDIMENTO | NUMBER | Identificativo della tabella generale procedimento |
| DATA_COMP_FOGLIO_COMPLEMENTARE | DATE | Data di compilazione del foglio complementare |
| DATA_SOSPENSIONE_SS | DATE | Data di sospensione sanzioni sostitutive |
| GIORNI_RECUPERO_SS | NUMBER | Giorni di recupero sanzioni sostitutive |
| FLAG_RECUPERO_SS | VARCHAR2 (1 CHAR) | S/N recupero sanzioni sostitutive |
| DATA_SCADENZA_SOSPENSIONE_ SS | DATE | Data di scadenza sanzioni sostitutive |
| SOSPENSIONE_GG | NUMBER | Giorni di sospensione |
| SOSPENSIONE_MM | NUMBER | Mesi di sospensione |
| SOSPENSIONE_AA . | NUMBER | Anni di sospensione |
| TIPO_CONTROLLO_ESECUZIONE | VARCHAR2(1 CHAR) | Tipo di controllo dell’esecuzione |
| FLAG_NOMINA_COMM_ACTA | VARCHAR2(1 CHAR) | Flag nomina acta |
| DESCR_COMM_ACTA | VARCHAR2(500 CHAR) | Descrizione acta |
| NUM_GIORNI_REVOCA_LA | NUMBER(4) | Numero di giorni di revoca della liberazione anticipata |
| NUM_GIORNI_RIDUZIONE_PENA | NUMBER(4) | Numero di giorni di riduzione pena |
| SOMMA_RISARC_DANNI | NUMBER(38) | Somma per il risarcimento dati |
| FLAG_ELABORATO | VARCHAR2(1 CHAR) | Flag elaborato S/N |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| DEP_DEC_EVE_FK | ID_EVENTO_GENERATO | (EVENTO.ID_EVENTO) |
| DEP_DEC_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO | (GENERALE_PROCEDIMENTO.ID_GENERALE_PROCEDIMENTO) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| IMPUGNAZIONE | IMP_DEP_DEC_FK | DEP_DEC_ID_DEPOSITO_DECRETO |
| MOTIVAZIONE_DECRETO | MOT_DEC_DEP_DEC_FK | DEP_DEC_ID_DEPOSITO_DECRETO |
| TENORE | TEN_DEP_DEC_FK | DEP_DEC_ID_DEPOSITO_DECRETO |



# DEPOSITO_ORDINANZA_PC
tabella contenente i dati relativi al deposito dell’ordinanza. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_DEPOSITO_ORDINANZA_PC | NUMBER NOT NULL | Chiave naturale interna legata a Sequence DEP_ORD_SEQ |
| ANNO_S3 | NUMBER | Anno del Registro S3. |
| NUM_S3 | NUMBER | Numero del Registro S3. |
| OGGETTO_PROCEDIMENTO | VARCHAR2 (240 CHAR) | Codifica del Tipo Decreto. Associato al Dominio TIPO_ORDINANZA |
| DATA_UDIENZA | DATE | Data dell’Udienza. |
| DATA_CAMERA_CONSIGLIO | DATE | Data Emissione dell’Ordinanza. |
| DATA_DEPOSITO | DATE | Data Deposito dell’Ordinanza. |
| COD_NATURA_PROVVEDIMENTO | VARCHAR2 (2000 CHAR) | Natura del provvedimento |
| ID_CSSA_COMP | NUMBER | Identificativo del CSSA |
| COD_UFFICIO_MAGISTRATO_COMP | VARCHAR2 (11 CHAR) | Ufficio del magistrato competente |
| LUOGO_SVOLGIMENTO_PROVA | VARCHAR2 (2000 CHAR) | Luogo di svolgimento della prova |
| SERVIZIO_TERAPEUTICO_COMP | VARCHAR2 (100 CHAR) | Descrizione del servizio terapeutico |
| NUM_GIORNI_DETENZIONE_DOM | NUMBER | Numero di giorni di detenzione domiciliari |
| NUM_MESI_DETENZIONE_DOM | NUMBER | Numero di mesi di detenzione domiciliari |
| NUM_ANNI_DETENZIONE_DOM | NUMBER | Numero di anni di detenzione domiciliari |
| NUM_GIORNI_PERMESSO_ACCORDATI | NUMBER | Numero di giorni di permesso accordato |
| NUM_GIORNI_RIDUZIONE_PENA | NUMBER | Numero di giorni di riduzione pena |
| NUM_GIORNI_RIDUZIONE_USUFRUITI | NUMBER | Numero di giorni di riduzione usufruiti |
| COD_UFF_TDS_CONCESSO_RIDUZIONE | VARCHAR2 (11 CHAR) DEFAULT '-' | Ufficio del Tribunale di Sorveglianza che ha concesso la riduzione |
| COD_MAGISTRATO | VARCHAR2 (6 CHAR) | Codice del magistrato |
| ID_EVENTO_GENERATO | NUMBER | Identificato dell’evento generato |
| NUM_GIORNI_LIBANTICIPATA | NUMBER | Numero di giorni di liberazione anticipata |
| FLAG_ELABORATO | VARCHAR2 (1 CHAR) | S/N elaborato o no |
| COD_TIPO_ORDINANZA | VARCHAR2 (2 CHAR) | Tipo dell’ordinanza |
| DATA_FINE_MISURA | DATE | Data fine misura |
| DATA_DECORRENZA | DATE | Data di decorrenza |
| DATA_INIZIO_PERIODO | DATE | Data inizio periodo |
| FLAG_ESISTENZA_REATOOSTATIVO | VARCHAR2 (1 CHAR) | Flag che indica l’esistenza del reato ostativo |
| FLAG_ESPIAZIONE_REATOOSTATIVO | VARCHAR2 (1 CHAR) | Flag che indica l’esistenza del reato ostativo |
| AUTORITA_VIGILANTE | VARCHAR2 (500 CHAR) | Descrizione dell’Autorità vigilante |
| DATA_TRASMISSIONE | DATE | Data della trasmissione |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMEN TO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha  aggiornato del record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| GEN_PRID_GENERALE_PROCEDIMENTO | NUMBER | Identificativo del Generale Procedimento |
| DATA_COMP_FOGLIO_COMPLEMENTARE | DATE | Data di compilazione del Foglio Complementare |
| NUM_GIORNI_ARRESTO_REV | NUMBER | Numero di giorni di arresto di revoca |
| NUM_MESI_ARRESTO_REV | NUMBER | Numero di mesi di arresto di revoca |
| NUM_ANNI_ARRESTO_REV | NUMBER | Numero di anni di arresto di revoca |
| ULTERIORE_DESCRIZIONE | VARCHAR2 (2000 CHAR) | Ulteriore descrizione |
| DATA_SOSPENSIONE_SS | DATE | Data di sospensione della sanzione sostitutiva |
| GIORNI_RECUPERO_SS | NUMBER | Numero di giorni della sanzione sostitutiva |
| FLAG_RECUPERO_SS | VARCHAR2 (1 CHAR) | S/N Recupero della sanzione sostitutiva |
| DATA_SCADENZA_SOSPENSIONE_ SS | DATE | Data di scadenza della sospensione della sanzione sostitutiva |
| SOSPENSIONE_GG | NUMBER | Numero di giorni della sospensione |
| SOSPENSIONE_MM | NUMBER | Numero di mesi della sospensione |
| SOSPENSIONE_AA | NUMBER | Numero di anni della sospensione |
| TIPO_CONTROLLO_ESECUZIONE | VARCHAR2(1 CHAR) | Tipologia di controllo dell’esecuzione |
| FLAG_NOMINA_COMM_ACTA | VARCHAR2(1 CHAR) | Flag nomina commissione acta |
| DESCR_COMM_ACTA | VARCHAR2(500 CHAR) | Descrizione commissione acta |
| SOMMA_RISARC_DANNI | NUMBER(92) | Importo della somma di risarcimento danni |
| COD_USSM | NUMBER(38) | Ufficio Servizio Sociale per i Minorenni |
| DATA_ESECUTIVITA | DATE | Data esecutivita' dell'Ordinanza di Applicazione Provvisoria M.A. |
| NOTE_DATA_ESECUTIVITA | VARCHAR2(2000 CHAR) | Note alla Data esecutivita' dell'Ordinanza di Applicazione Provvisoria M.A. |
| COD_TIPO_SANZIONE | VARCHAR2(2 CHAR) | 01=Semiliberta; 02=Detenzione Domiciliare; 03=Lavoro Pubblica Utilita; 04=Permanenza Domiciliare |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| DEP_OPC_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO | (GENERALE_PROCEDIMENTO.ID_GENERALE_PROCEDIMENTO) |
| DEP_ORD_PC_EVE_FK | ID_EVENTO_GENERATO | (EVENTO.ID_EVENTO) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| IMPUGNAZIONE | IMP_DEP_OPC_FK | DEP_OPID_DEPOSITO_ORDINANZA_PC |
| TENORE | TEN_DEP_OPC_FK | DEP_OPID_DEPOSITO_ORDINANZA_PC |


# DEPOSITO_SENTENZA
tabella contenente i dati relativi al deposito della sentenza. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_DEPOSITO_SENTENZA | NUMBER(22) | Identificativo deposito sentenza |
| ANNO_SENTENZA | NUMBER(22) | Anno sentenza |
| NUM_SENTENZA | NUMBER(22) | Numero sentenza |
| COD_TIPO_SENTENZA | VARCHAR2(2) | Tipo sentenza |
| DATA_EMISSIONE | DATE(7) | Data emissione |
| DATA_DEPOSITO | DATE(7) | Data deposito |
| COD_MAGISTRATO | VARCHAR2(6) | Codice del magistrato |
| ALTRI_DESTINATARI | VARCHAR2(200) | Descrizione altri destinatari |
| DATA_PARERE_PG | DATE(7) | Data del parere del PG |
| COD_TIPO_PARERE_PG | VARCHAR2(2) | Tipo parere PG |
| DATA_RICORSO_IMPUGNAZIONE | DATE(7) | Data del ricorso dell’impugnazione |
| DATA_INVIO_ATTI_IMPUGNAZIONE | DATE(7) | Data dell’invio degli atti dell’impugnazione |
| DATA_SENTENZA_IMPUGNAZIONE | DATE(7) | Data delle sentenza di impugnazione |
| TENORE_SENTENZA_IMPUGNAZIONE | VARCHAR2(2) | Identificativo del tenore dell’impugnazione |
| NOTE | VARCHAR2(2000) | Note |
| SENTENZE_RIFERIMENTO | VARCHAR2(200) | Descrizione delle sentenze di riferimento |
| COD_PROCURA_ESECUZIONE | VARCHAR2(11) | Identificativo procura di riferimenti |
| COD_UFFICIO_COMP | VARCHAR2(11) | Codice dell’Ufficio competente |
| ID_EVENTO_GENERATO | NUMBER(22) | Identificati dell’eventi |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Utente che ha effettuato l’inserimento |
| DATA_INSERIMENTO | DATE(7) | Data dell’inserimento |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11) | Ufficio che ha effettuato l’inserimento |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100) | Utente che ha effettuato l’aggiornamenti |
| DATA_AGGIORNAMENTO | DATE(7) | Data di aggiornamento del  record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(11) | Ufficio che ha effettuato l’aggiornamento |
| GEN_PRID_GENERALE_PROCEDIMENTO | NUMBER(22) | Identificato della tabella generale procedimento |
| ULTERIORE_DESCRIZIONE | VARCHAR2(2000) | Ulteriore descrizione |
| COD_NATURA_PROVVEDIMENTO | VARCHAR2(2000) | Identificativo della natura del provvedimento |
| OGGETTO_PROCEDIMENTO | VARCHAR2(240) | Oggetto del procedimento |
| DATA_UDIENZA | DATE(7) | Data dell’udienza |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| DEP_SENT_EVE_FK | ID_EVENTO_GENERATO | (EVENTO.ID_EVENTO) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| IMPUGNAZIONE | IMP_DEP_SEN_FK | DEP_ID_DEPOSITO_SENTENZA |
| TENORE | TEN_DEP_SENT_FK | DEP_ID_DEPOSITO_SENTENZA |


# DETTAGLIO_PROVVEDIMENTO
tabella contenente i dati relativi alle action java rispetto al tipo di provvedimento e codice motivo.  utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_TIPO_EVENTO | VARCHAR2 (2 CHAR) NOT NULL | Chiave naturale interna legata a Sequence DEP_ORD_SEQ |
| COD_TIPO_PROVVEDIMENTO | VARCHAR2 (2 CHAR) NOT NULL | Tipologia del provvedimento |
| COD_MOTIVO | VARCHAR2 (4 CHAR) NOT NULL | Codice motivo |
| ACTION_DETTAGLIO | VARCHAR2 (100 CHAR) NOT NULL | Dettaglio della action |
| NOTE | VARCHAR2 (2000 CHAR) | Note |
| ACTION_UPLOAD | VARCHAR2 (100 CHAR). | Action dell’upload |


# DOCUMENTO_ALLEGATO
tabella contenente i dati relativi al documento allegato ad un foglio complementare. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_DOCUMENTO_ALLEGATO | NUMBER NOT NULL | Chiave naturale interna legata a Sequence DOC_ALL_SEQ |
| DATA_EMISSIONE | DATE | Data di emissione del documento. |
| COD_TIPO_DOCUMENTO | VARCHAR2 (2 CHAR) | Codifica del Tipo di Documento. Associato al dominio TIPO_DOCUMENTO_ALLEGATO di CG_REF_CODES. |
| NUMERO_PROGRESSIVO | NUMBER | Numero progressivo del documento |
| FLAG_DOCUMENTO_REGISTRATO | VARCHAR2 (1 CHAR) | Indica l'avvenuta registrazione del documento. Associato al dominio FLAG_SI_NO di CG_REF_CODES. |
| DOC_BLOB | BLOB | Dato di tipo BLOB Contenente il documento prodotto. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| EVE_ID_EVENTO | NUMBER | Identificativo dell'evento collegato. |
| TEM_ID_TEMPLATE | VARCHAR2 (25 CHAR) | Identificativo del Template collegato. |
| ANNO_FOGLIO_COMPLEMENTARE | NUMBER | Anno del foglio complementare |
| PROGR_FOGLIO_COMPLEMENTAR E | NUMBER | Progressivo del foglio complementare |
| DATA_TRASMISSIONE | DATE | Data della trasmissione |
| DATA_ANNULLAMENTO | DATE | Data dell’annullamento |
| MOTIVO_ANNULLAMENTO | VARCHAR2 (2000 CHAR) | Descrizione del motivo dell’annullamento |
| COMUNE_SEDE_GIUDIZIARIA | VARCHAR2 (200 CHAR) DEFAULT 'NULL' | Comune del Casellario Giudiziario (per i Fogli Complementari ) |
| CODI_MOTIVAZIONE_NON_INVIO | VARCHAR2(3 CHAR) | Indica la motivazione del non invio ad NSC |
| DESCRIZIONE_NON_INVIO | VARCHAR2(250 CHAR) | Indica la motivazione del non invio ad NSC |
| DATA_ULT_INVIO | DATE | Indica la data invio ultimo aggiornamento |
| DATA_INS_MAN | DATE | Indica la data inserimento manuale su NSC |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| DOC_ALL_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| DOC_ALL_TEM_FK | TEM_ID_TEMPLATE | (TEMPLATE.ID_TEMPLATE) |


# errori_sies_pagopa
tabella utilizzata per la gestione degli errori provenienti dalla interazione tra siep e PagoPA.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| id_errori_sies_pagopa | NUMBER(38) NOT NULL | Primary key della tabella, indica l’identificativo dell’errore |
| id_fascicolo_siep | NUMBER(38) | Indica l’identificativo del fascicolo SIEP collegato |
| id_evento | NUMBER(38) | Indica l’identificativo dell’evento SIEP collegato |
| azione_contesto_java | VARCHAR2(100) | Indica la classe Java di riferimento |
| descrizione_funzione | VARCHAR2(100) | Indica la descrizione della funzione utilizzata |
| cod_utente | VARCHAR2(100) | Indica il codice utente collegato |
| cod_ufficio | VARCHAR2(11) | Indica il codice dell’ufficio dell’utente collegato |
| errore_esecuzione | VARCHAR2(2000) | Indica la descrizione dell’errore rilevato |
| data_inserimento | DATE | Indica la data di inserimento del record |
| data_visualizzazione | DATE | Indica la data di visualizzazione dell’errore |
| cod_utente_visualizzazione | VARCHAR2(100) | Indica il codice dell’utente che ha visualizzato l’errore |


# ERRORI_TRIGGER
tabella utilizzata per la gestione degli errori provenienti dall’esecuzione del trigger siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| PROVENIENZA | VARCHAR2(50) | Provenienza del trigger andato in errore. |
| DATA_ERRORE | DATE | Data dell’errore. |
| NUME_ERRORE | NUMBER | Numero dell’errore. |
| DESC_ERRORE | VARCHAR2(4000 CHAR) | Descrizione dell’errore. |


# ESECUZIONE_MISURA_ALTERNATIVA
tabella contenente i dati relativi all’esecuzione di una misura alternativa. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ESECUZIONE_MISURA_ALTERNATIVA | NUMBER NOT NULL | Chiave naturale interna legata a Sequence ESE_MIS_ALT_SEQ |
| ANNO_S07 | NUMBER NOT NULL | Anno del Registro S07. |
| PROGR_S07 | NUMBER NOT NULL | Progressivo del Registro S07. |
| DATA_ORDINANZA | DATE | Data dell'Ordinanza. |
| COD_AUTORITA_EMITT_ORD | VARCHAR2 (11 CHAR) | Codice Ufficio dell'Autorità che ha emesso l'ordinanza. |
| COD_TIPO_AUTORITA_EMITT_ORD | VARCHAR2 (2 CHAR) | Codifica del Tipo autorità che ha emesso l'Ordinanza. Associato al dominio TIPO_AUTORITA di CG_REF_CODES. |
| COD_LUOGO_AUTORITA_EMITT_O RD | VARCHAR2 (6 CHAR) | Codice Comune dell'Autorità che ha emesso l'Ordinanza |
| COD_TIPO_MISURA | VARCHAR2 (4 CHAR) | Codifica dell' Oggetto Tenore del Provvedimento. Associato al dominio MOTIVO_PROVVEDIMENTO |
| DATA_INIZIO_MISURA | DATE | Data di inizio della misura |
| DATA_TERMINE_INIZIALE | DATE | Data di termine iniziale della misura |
| DATA_TERMINE_ATTUALE | DATE | Data di termine attuale della misura |
| DATA_DECLARATORIA_EP | DATE | Data declaratoria di Estinzione pena |
| DATA_TX_ATTI_EST_PENA | DATE | Data Trasmissione atti Estinzione Pena |
| DEP_DEC_ID_DEPOSITO_DECRETO | NUMBER | Identificativo del Deposito_Decreto collegato. |
| DEP_OPID_DEPOSITO_ORDINANZA_PC | NUMBER | Identificativo del Deposito_OrdinanzaPC collegato. |
| NOTE | VARCHAR2 (2000 CHAR) | Eventuali note aggiuntive |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| GEN_PRID_GENERALE_PROCEDIMENTO | NUMBER NOT NULL | Identificativo del GENERALE_PROCEDIMENTO collegato. |
| LUOGO_ESECUZIONE_MISURA | VARCHAR2 (100 CHAR) | Luogo di Esecuzione della Misura Alternativa. |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| EXE_MIS_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO | (GENERALE_PROCEDIMENTO.ID_GENERALE_PROCEDIMENTO) |


# ESECUZIONE_MISURA_SICUREZZA
tabella contenente i dati relativi all’esecuzione di una misura di sicurezza. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ESECUZIONE_MISURA_SICUREZZA | NUMBER NOT NULL | Chiave naturale interna legata a Sequence ESE_MIS_ALT_SEQ |
| ANNO_S07 | NUMBER NOT NULL | Anno del Registro S07. |
| PROGR_S07 | NUMBER NOT NULL | Progressivo del Registro S07. |
| DATA_ORDINANZA | DATE | Data dell’ordinanza |
| COD_AUTORITA_EMITT_ORD | VARCHAR2 (11 CHAR) | Codice dell’autorità emittente dell’ordinanza |
| COD_TIPO_AUTORITA_EMITT_ORD | VARCHAR2 (2 CHAR) | Tipo dell’autorità emittente dell’ordinanza |
| COD_LUOGO_AUTORITA_EMITT_O RD | VARCHAR2 (6 CHAR) | Sede dell’autorità emittente dell’ordinanza |
| COD_TIPO_MISURA | VARCHAR2 (4 CHAR) | Tipologia della Misura |
| DATA_INIZIO_MISURA | DATE | Data inizio della misura |
| DATA_TERMINE_INIZIALE | DATE | Data termine iniziale |
| DATA_TERMINE_ATTUALE | DATE | Data termine attuale |
| DATA_DECLARATORIA_EMS | DATE | Data declaratoria dell’esecuzione della misura di sicurezza |
| DEP_DEC_ID_DEPOSITO_DECRETO | NUMBER | Identificati del deposito del decreto |
| DEP_OPID_DEPOSITO_ORDINANZA_PC | NUMBER | Identificativo del deposito dell’ordinanza |
| NOTE | VARCHAR2 (2000 CHAR) | Note |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| GEN_PRID_GENERALE_PROCEDIMENTO | NUMBER NOT NULL | Identificativo del generale del procedimento |
| LUOGO_ESECUZIONE_MISURA | VARCHAR2 (100 CHAR) | Luogo di esecuzione della MS |
| NUM_GIORNI_MISURA | NUMBER | Numero di giorni della misura |
| NUM_MESI_MISURA | NUMBER | Numero di mesi della misura |
| NUM_ANNI_MISURA | NUMBER | Numero di anni della misura |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| EMS_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO | (GENERALE_PROCEDIMENTO.ID_GENERALE_PROCEDIMENTO) |

# ESECUZIONE_SANZIONE_SOST
tabella contenente i dati relativi all’esecuzione di una sanzione sostitutiva. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ESECUZIONE_SANZIONE_SOST | NUMBER NOT NULL | Chiave numerica naturale dell'entità |
| ANNO_S07 | NUMBER NOT NULL | Anno del Registro S07. |
| PROGR_S07 | NUMBER NOT NULL | Progressivo del Registro S07. |
| DATA_ORDINANZA | DATE | Data di Emissione dell’Ordinanza. |
| COD_AUTORITA_EMITT_ORD | VARCHAR2 (11 CHAR) | Codice dell’Autorità Emittente l’Ordinanza. |
| COD_TIPO_AUTORITA_EMITT_ORD | VARCHAR2 (2 CHAR) | Codice del Tipo Autorità Emittente l’Ordinanza. |
| COD_LUOGO_AUTORITA_EMITT_ORD | VARCHAR2 (6 CHAR) | Codice del Comune sede dell’Autorità Emittente l’Ordinanza. |
| COD_TIPO_SANZIONE | VARCHAR2 (4 CHAR) | Tipologia della sanzione |
| DATA_INIZIO_SANZIONE | DATE | Data inizio sanzione |
| DATA_TERMINE_INIZIALE | DATE | Data temine iniziale |
| DATA_TERMINE_ATTUALE | DATE | Data termine attuale |
| DATA_DECLARATORIA_ESS | DATE | Data declaratoria dell’esecuzione della sanzione sostitutiva |
| DEP_DEC_ID_DEPOSITO_DECRETO | NUMBER | Identificativo del deposito del decreto |
| DEP_OPID_DEPOSITO_ORDINANZA_PC | NUMBER | Identificativo del deposito dell’ordinanza |
| NOTE | VARCHAR2 (2000 CHAR) | Note |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMEN TO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| GEN_PRID_GENERALE_PROCEDIMENTO | NUMBER NOT NULL | Identificativo del generale del procedimento |
| LUOGO_ESECUZIONE_SANZIONE | VARCHAR2 (100 CHAR) | Luogo di esecuzione della Sanzione Sostitutiva |
| NUM_GIORNI_SANZIONE | NUMBER | Numero di giorni della Sanzione Sostitutiva |
| NUM_MESI_SANZIONE | NUMBER | Numero di mesi della Sanzione Sostitutiva |
| NUM_ANNI_SANZIONE | NUMBER | Numero di anni della Sanzione Sostitutiva |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| EXE_SAN_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO | (GENERALE_PROCEDIMENTO.ID_GENERALE_PROCEDIMENTO) |


# ESITO_ARCHIVIAZIONI_CUMULO
tabella contenente i dati relativi dati di sintesi dell’esito dell’archiviazione di una Istruttoria Cumulo.  utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ESITO_ARCHIVIAZIONI_CUMULO | NUMBER(38) | Sequence |
| FLAG_ARCHIVIATO | VARCHAR2(1) | ‘N’ non archiviato, ‘S’ archiviato |
| DESCRIZIONE_ESITO | VARCHAR2(2000) | Descrizione motivo archiviazione |
| CHIAVE_UFFICIO | VARCHAR2(11) | Codice Ufficio del Procedimento SIEP |
| CHIAVE_ANNO_FASC_SIEP | NUMBER(4) | Anno Procedimento SIEP |
| CHIAVE_PROGR_FASC_SIEP | NUMBER(9) | Numero Procedimento SIEP |
| FAS_ID_FASCICOLO_SIEP | NUMBER(38) | Eventuale FK della tabella FASCICOLO_SIEP |
| ISTR_ID_ISTRUTTORIA_CUMULO | NUMBER(38) | FK alla tabella ISTRUTTORIA_CUMULO |
| EVE_ID_EVENTO | NUMBER(38) | FK alla tabella EVENTO |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Inserimento |
| DATA_INSERIMENTO | DATE | Data Inserimento |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Inserimento |

# ESPERTO
tabella contenente i dati anagrafici di un esperto. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ESPERTO | NUMBER NOT NULL | Chiave numerica naturale dell'entità |
| COGNOME | VARCHAR2 (50 CHAR) NOT NULL | Cognome esperto |
| NOME | VARCHAR2 (50 CHAR) | Nome esperto |
| INDIRIZZO | VARCHAR2 (200 CHAR) | Indirizzo di riferimento dell'esperto |
| TELEFONO | VARCHAR2 (12 CHAR) | Telefono di riferimento dell'esperto |
| COD_UFFICIO_APPARTENENZA | VARCHAR2 (11 CHAR) | Codice di appartenenza dell'esperto. Univoco perché un esperto è in genere legato ad un solo ufficio |
| EMAIL | VARCHAR2 (100 CHAR) | Indirizzo di posta elettronica di riferimento dell'esperto |
| FAX | VARCHAR2 (12 CHAR) | fax di riferimento dell'esperto |
| CELLULARE | VARCHAR2 (12 CHAR) | Numero di cellulare di riferimento dell'esperto |
| DATA_INIZIO_VALIDITA | DATE | Data di inizio del rapporto esperto-ufficio |
| DATA_FINE_VALIDITA | DATE | Data di fine del rapporto esperto-ufficio |
| FLAG_STATO | VARCHAR2 (1 CHAR) | Campo indicante lo stato del rapporto esperto-ufficio.
Deriva da dominio FLAG_STATO e può assumere i seguenti valori:
A-ASSENTE 
P-RESENTE
T-TRASFERITO |
| CODICE_FISCALE | VARCHAR2 (16 CHAR) | Codice fiscale dell'Esperto utile in caso di omonimia. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR). | Ufficio dell’operatore che ha aggiornato il record |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| COLLEGIO_ESPERTO | COL_ESP_ESPERTO_FK | ESP_ID_ESPERTO |
| ESPERTO_ATTIVITA | ESP_ATT_ESP_FK | ESP_ID_ESPERTO |
| MAGISTRATO_RELATORE | MAG_REL_ESP_FK | ESP_ID_ESPERTO |
| UDIENZA | UDIENZA_ESPERTO_FK1 | COD_ID_ESPERTO_1 |
| UDIENZA | UDIENZA_ESPERTO_FK2 | COD_ID_ESPERTO_2 |


# ESPERTO_ATTIVITA
tabella associativa tra l’Esperto e l’Attività. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| DATA_INIZIO | DATE NOT NULL | Data inizio attività |
| DATA_FINE | DATE | Data fine attività |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMEN TO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| ESP_ID_ESPERTO | NUMBER NOT NULL | Identificativo esperto |
| ATT_ID_ATTIVITA | NUMBER NOT NULL | Identificativo attività |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| ESP_ATT_ATT_FK | ATT_ID_ATTIVITA | (ATTIVITA.ID_ATTIVITA) |
| ESP_ATT_ESP_FK | ESP_ID_ESPERTO | (ESPERTO.ID_ESPERTO) |




# EVENTO
tabella contenente i dati relativi agli eventi di un fascicolo. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_EVENTO | NOT NULL | Chiave numerica naturale per la gestione dei record della tabella Evento. |
| COD_TIPO_EVENTO | VARCHAR2 (2 CHAR) NOT NULL | Codice che identifica il tipo di evento che si sta trattando. Deriva da dominio e può assumere diversi valori tra i quali spiccano: PROVVEDIMENTO RICHIESTA ISTANZA INFORMATIVA RICHIESTA ISTRUTTORIA |
| COD_TIPO_PROVVEDIMENTO | VARCHAR2 (2 CHAR) | Attributo relativo al solo tipo evento "PROVVEDIMENTO" Referenziato dal dominio di valori: S= sentenza O= ordinanza D= decreto |
| COD_MOTIVO | VARCHAR2 (4 CHAR) | E' il motivo per cui viene emesso un provvedimento. Deriva da dominio "MOTIVO_PROVVEDIMENTO" Es. - Ordine di esecuzione
- Ordine di scarcerazione - Art.146 C.P. (RINVIO OBBLIGATORIO
ESECUZIONE) |
| COD_UFFICIO_EMITTENTE | VARCHAR2 (11 CHAR) | Indica l'ufficio di chi emette il provvedimento. Non coincide necessariamente con l'ufficio presso il quale è depositato e trattato il fascicolo. Deriva da dominio "UFFICIO" |
| COD_LUOGO_EMITTENTE | VARCHAR2 (6 CHAR) | Indica il luogo (comune) presso cui risiede l'ufficio dell'autorità emittente. Deriva da dominio "COMUNE" e serve per completare l'informazione Autorità emittente. Es. RUOLO del UFFICIO di COMUNE - PM del TRIBUNALE di NAPOLI |
| DATA_EMISSIONE | DATE | Data di emissione del Provvedimento |
| COD_ESITO | VARCHAR2 (4 CHAR) | Deriva dal dominio "ESITO" vale: Accolto Rigettato |
| FLAG_PIU_MENO | VARCHAR2 (1 CHAR) | Deriva da dominio vale: P quando devono essere sommati dei valori alla pena attuale per la sua rideterminazione D quando devono essere sottratti dei valori alla pena attuale per la sua rideterminazione |
| DATA_TRASMISSIONE_ATTI | DATE | Equivalente alla "Data Notifica" per tutti i casi in cui non ho solo la notifica verso Autorità Esterne. Ad esempio la notifica al SOGGETTO o al/agli AVVOCATO/I i quali non sono autorità esterne. |
| DATA_RICEZIONE_ATTI | DATE | Registrazione della data di presa in carico di un atto legato ad un evento |
| COD_UFFICIO_DESTINATARIO | VARCHAR2 (11 CHAR) | Si intende l'ufficio a cui è destinato l'evento trattato. Es. TdS o altro ufficio esecuzione Il valore dentro questo attributo è generato dall'accoppiata TIPO/LUOGO Destinatario |
| ANNO_PROTOCOLLO | NUMBER | Necessario se anche per il protocollo (così come avviene per le ISTANZE) è necessario mantenere una sorta di registro progressivo. Fa parte della chiave di tale registro. |
| PROGR_PROTOCOLLO | NUMBER | Necessario se anche per il protocollo (così come avviene per le ISTANZE) è necessario mantenere una sorta di registro progressivo. Fa parte della chiave di tale registro. |
| DOC_BLOB | BLOB | Documento in formato binario prodotto per l'evento. Può essere generato modificato e aggiornato fintanto che il campo FLAG_DOCUMENTO_REGISTRATO |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMEN TO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER | Identificativo del fascicolo SIUS |
| COD_LUOGO_DESTINATARIO | VARCHAR2 (6 CHAR) | Indica il luogo (comune) presso cui risiede il destinatario. Deriva da dominio "COMUNE" e serve per completare l'informazione Autorità emittente. Es. RUOLO del UFFICIO di COMUNE - PM del TRIBUNALE di NAPOLI |
| TEN_ID_TENORE | NUMBER | Identificativo del tenore |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| FLAG_DOCUMENTO_REGISTRATO | VARCHAR2 (1 CHAR) | Flag per marcare un documento affinché non possa più essere modificato. |
| COD_MAGISTRATO | VARCHAR2 (6 CHAR) | Indica il codice Magistrato. |
| COD_TIPO_UFFICIO_DESTINATARIO | VARCHAR2 (6 CHAR) | Contiene la codifica del Tipo Ufficio. Associato al dominio TIPO_UFFICIO. |
| COGNOME_SOGGETTO_PRESENTANTE | VARCHAR2 (100 CHAR) | Cognome del Soggetto che ha presentato la richiesta. |
| NOME_SOGGETTO_PRESENTANTE | VARCHAR2 (100 CHAR) | Nome del Soggetto che ha presentato la richiesta. |
| FAS_SIU_ID_FASCICOLO_SIUS_DEST | NUMBER | Chiave (ID) del fascicolo SIUS destinatario dell'evento. |
| TEM_ID_TEMPLATE | VARCHAR2 (25 CHAR) | Chiave (ID) dell'eventuale template utilizzato in un particolare evento. |
| FLAG_STAMPA_SIEP | VARCHAR2 (1 CHAR) | Flag per indicare se tale evento può essere stampato nell'ordine di esecuzione del soggetto |
| FLAG_STAMPA_SIUS | VARCHAR2 (1 CHAR) | Flag per indicare se tale evento può essere stampato nell'ordine di esecuzione del soggetto in ambito SIUS |
| FLAG_VIDEO_SIEP | VARCHAR2 (1 CHAR) | Flag per indicare se tale evento può essere mostrato a video |
| FLAG_VIDEO_SIUS | VARCHAR2 (1 CHAR) | Flag per indicare se tale evento può essere mostrato a video in ambito SIUS |
| DEC_ID_DECRETO_ORDINANZA_SIEP | NUMBER | Identificativo del decreto dell’ordinanza |
| PEN_ACC_ID_PENA_ACCESSORIA | NUMBER | Identificativo pena accessoria |
| EVE_ID_EVENTO_REVOCA | NUMBER | Identificativo evento di revoca |
| ANN_ID_ANNOTAZIONE_MANUALE | NUMBER | Identificativo annotazione manuale |
| PEN_ID_PENA_RESIDUA | NUMBER | Identificativo pena residua |
| PROTOCOLLO_RES | NUMBER | Protocollo RES |
| DATA_ESPULSIONE_SANZ_SOST | DATE | Data di espulsione della sanzione sostitutiva |
| DATA_RICHIESTA | DATE | Data arrivo richiesta variazione Decorrenza Scadenza |
| KEY_ESEC_NSC | NUMBER | Chiave del provvedimento di NSC |
| DATA_INVIO_ATTI | DATE | Data invio atti in archivio |
| TIPOLOGIA_INVIO_ATTI | VARCHAR2(240) | Tipologia invio atti |
| DESCRIZIONE_INVIO_ATTI | VARCHAR2(240) | Descrizione invio atti |
| ISTR_ID_ISTRUTTORIA_CUMULO | NUMBER(38) | Identificativo istruttoria cumulo |
| ESTREMI_SOGG_RICH_ISTR | VARCHAR2(2000) | Estremi soggetto x Richieste Istruttorie in cumulo |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| EVE_ANN_MAN_FK | ANN_ID_ANNOTAZIONE_MANUALE | (ANNOTAZIONE_MANUALE.ID_ANNOTAZIONE_MANUALE) |
| EVE_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| EVE_EVE_REVOCA_FK | EVE_ID_EVENTO_REVOCA | (EVENTO.ID_EVENTO) |
| EVE_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |
| EVE_FAS_SIU_FK | FAS_SIU_ID_FASCICOLO_SIUS | (FASCICOLO_SIUS.ID_FASCICOLO_SIUS) |
| EVE_PEN_RES_FK | PEN_ID_PENA_RESIDUA | (PENA_RESIDUA.ID_PENA_RESIDUA) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| ANNOTAZIONE_ESITO_TRASMISSIONE | ANN_ESITO_TRASMISS_EVE_FK | EVE_ID_EVENTO |
| ARCHIVIAZIONE | ARC_EVE_FK | EVE_ID_EVENTO |
| BENEFICIO | BEN_EVE_FK | EVE_ID_EVENTO |
| CAMPO_NOTA | CAM_NOT_EVE_FK | EVE_ID_EVENTO |
| COMPETENZA | COMPETENZA_ID_EVENTO_FK | EVE_ID_EVENTO |
| CUMULO | CUM_EVE_FK | EVE_ID_EVENTO |
| DEPOSITO_DECRETO | DEP_DEC_EVE_FK | ID_EVENTO_GENERATO |
| DEPOSITO_ORDINANZA_PC | DEP_ORD_PC_EVE_FK | ID_EVENTO_GENERATO |
| DEPOSITO_SENTENZA | DEP_SENT_EVE_FK | ID_EVENTO_GENERATO |
| DOCUMENTO_ALLEGATO | DOC_ALL_EVE_FK | EVE_ID_EVENTO |
| EVENTO | EVE_EVE_FK | EVE_ID_EVENTO |
| EVENTO | EVE_EVE_REVOCA_FK | EVE_ID_EVENTO_REVOCA |
| MOTIVO_EVENTO | EVE_ID_EVENTO_FK | EVE_ID_EVENTO |
| SCAMBIO_SANZIONE | EVE_ID_EVENTO_SCAM_SANZ_FK | EVE_ID_EVENTO |
| STATO_PROCEDIMENTO | EVE_STATO_PROC_FK | EVE_ID_EVENTO |
| FASCICOLO_SIEPE | FAS_SIEPE_EVE_FK | EVE_ID_EVENTO |
| FUNGIBILITA | FNG_EVE_FK | EVE_ID_EVENTO |
| ISTANZA | IST_EVE_FK | EVE_ID_EVENTO |
| LICENZA_LIBANTICIPATA | LIC_LIB_EVE_FK | EVE_ID_EVENTO |
| MISURA_ALTERNATIVA | MIS_ALT_EVE_FK | EVE_ID_EVENTO |
| MISURA_CAUTELARE | MIS_CAU_EVE_FK | EVE_ID_EVENTO |
| MISURA_SICUREZZA | MIS_SIC_EVE_FK | EVE_ID_EVENTO |
| MOTIVAZIONE_DECRETO | MOT_DEC_EVE_FK | EVE_ID_EVENTO |
| MOTIVAZIONE_PROVVED_SIGE | MOT_PRO_SIG_EVE_FK | EVE_ID_EVENTO |
| NOME_PROVVEDIMENTO | NOM_PRO_EVE_FK | EVE_ID_EVENTO |
| NOTIFICA | NOT_1_EVE_FK | EVE_ID_EVENTO |
| PENA_PECUNIARIA | PEN_PEC_EVE_FK | EVE_ID_EVENTO |
| PENA_RESIDUA | PEN_RES_EVE_FK | EVE_ID_EVENTO |
| PERIODO_ALTRA_MISURA | PER_MISU_ID_EVENTO_FK | EVE_ID_EVENTO |
| PERIODO_ALTRA_SANZIONE | PER_SANZ_ID_EVENTO_FK | EVE_ID_EVENTO |
| POSIZIONE_GIURIDICA | POS_GIU_EVE_FK | ID_EVENTO_RIFERIMENTO |
| PRESCRIZIONE | PRE_1_EVE_FK | EVE_ID_EVENTO |
| PROVVEDIMENTO_SIGE | PROV_EVE_FK | ID_EVENTO_GENERATO |
| REFERTO_SCARCERAZIONE | REF_SCA_EVE_FK | EVE_ID_EVENTO |
| RICHIESTA_CONVERSIONE | RIC_CON_ID_EVENTO_FK | EVE_ID_EVENTO |
| RICHIESTA_REMISSIONE | RIC_REM_ID_EVENTO_FK | EVE_ID_EVENTO |
| SANZIONE_AMMINISTRATIVA | SAN_AMM_EVE_FK | EVE_ID_EVENTO |
| SCADENZARIO_SIEP | SCA_SIE_EVE_FK | EVE_ID_EVENTO |
| SCADENZARIO_SIGE | SCA_SIGE_EVE_FK | EVE_ID_EVENTO |
| SCADENZARIO_SIUS | SCA_SIU_EVE_FK | EVE_ID_EVENTO |
| SOLLECITO_ESITO_TRASMISSIONE | SOLL_ESITO_TRASMISS_EVE_FK | EVE_ID_EVENTO |
| UDIENZA_PROCEDIMENTO | UDI_PRO_EVE_FK | EVE_ID_EVENTO |
| UDIENZA_PROCEDIMENTO_SIGE | UDI_PRO_SIG_EVE_FK | EVE_ID_EVENTO |
| VERBALE | VER_EVE_FK | EVE_ID_EVENTO |


# EVENTO_PERMESSO_LICENZA
tabella contenente i dati relativi al permesso di licenza relativo ad un evento. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_EVENTO_PERMESSO_LICENZA | NUMBER NOT NULL | ID Evento Permesso Licenza |
| COD_TIPO_EVENTO | VARCHAR2 (2 CHAR) | Codice tipo evento |
| DATA_SEGNALAZIONE | DATE | Data della segnalazione evento |
| MITTENTE_SEGNALAZIONE | VARCHAR2 (200 CHAR) | Mittente della segnalazione |
| COD_TIPO_CONSEGUENZA | VARCHAR2 (4 CHAR) | Codice tipo conseguenza |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice operatore inserimento record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Codice ufficio inserimento record |
| DATA_INSERIMENTO | DATE | Data inserimento record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice operatore aggiornamento record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Codice Ufficio Aggiornamento record |
| DATA_AGGIORNAMENTO | DATE | Data aggiornamento record |
| LIC_ID_LICENZA_LIBANTICIPATA | NUMBER | ID Licenza Lib anticipata |
| DESCR_EVENTO | VARCHAR2 (200 CHAR) | Descrizione evento |
| DESCR_CONSEGUENZE . | VARCHAR2 (100 CHAR) | Descrizione conseguenze |


# FASCICOLO_SIEP
tabella contenente i dati relativi al fascicolo siep. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_EVENTO_PERMESSO_LICENZA | NUMBER NOT NULL | Identificativo del permesso di licenza |
| ID_FASCICOLO_SIEP | NUMBER NOT NULL | Chiave naturale della tabella "Fascicolo_siep" legata a sequence "FAS_SIE_SEQ" Necessaria per le relazioni con le altre tabelle nelle quali sarà identificata come foreign key. Generata da ogni accoppiata Soggetto/Sentenza i quali sono entrambi necessari e obbligatori. |
| CHIAVE_ANNO | NUMBER NOT NULL | Porzione del Codice SIEP reale. Vale sempre l'anno corrente di generazione del fascicolo. Deve essere impostato automaticamente e non è modificabile |
| CHIAVE_UFFICIO | VARCHAR2 (11 CHAR) NOT NULL | Porzione del Codice SIEP reale. Fa riferimento all'ufficio che sta trattando l'esecuzione penale nell'ambito dell'accoppiata Sentenza/Soggetto |
| CHIAVE_PROGR | NUMBER NOT NULL | Porzione del Codice SIEP reale. Valore progressivo per distinguere i fascicoli nell'ambito di uno stesso ufficio. E' azzerato ad ogni inizio anno. |
| COD_STATO_FASCICOLO | VARCHAR2 (2 CHAR) NOT NULL | Deriva da dominio "STATO_FASCICOLO" Identifica gli stati di un Fascicolo. APERTO ARCHIVIATO VALIDATO ARCHIVIATO PER CUMULO ecc. |
| DATA_ISCRIZIONE | DATE | Data di iscrizione del fascicolo nel sistema informativo. Per default vale la data inserimento |
| DATA_ARCHIVIAZIONE | DATE | Data dalla quale un fascicolo risulta archiviato. Tale data una volta inserita non è modificabile |
| COD_MOTIVO_ARCHIVIAZIONE | VARCHAR2 (2 CHAR) | Deriva da dominio "MOTIVO_ARCHIVIAZIONE". E' la motivazione per cui un fascicolo ASSORBIMENTO IN CUMULO AVVENUTA ESPIAZIONE ESTINZIONE PENA PER MORTE DEL REO ecc. |
| LETTERA_FASCICOLO | VARCHAR2 (240 CHAR) | Lettera del fascicolo |
| NOTE | VARCHAR2 (2000 CHAR) | Campo per inserire eventuali informazioni supplementari. |
| COD_TIPO_POS_LIBERO | VARCHAR2 (1 CHAR) | Campo presente in RES. Mantenuto per coerenza con la precedente applicazione non è più necessario nella presente. |
| FLAG_VALIDATO | VARCHAR2 (1 CHAR) | Flag per determinare se un fascicolo è stato validato o meno. La validazione implica che i dati del soggetto e della sentenza più tutti i dati dei capi di imputazione siano stati controllati e confermati dal PM di esecuzione. La validazione impedisce di cancellare uno qualunque dei dati legati al fascicolo. Da questo momento in poi sarà possibile modificare i dati del fascicolo solo storicizzando la precedente situazione. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| SOG_ID_SOGGETTO | NUMBER NOT NULL | Identificativo del soggetto |
| SEN_ID_SENTENZA | NUMBER NOT NULL | Identificativo della sentenza |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo siep |
| FLAG_ALTRA_CAUSA | VARCHAR2 (1 CHAR) | Flag altra causa |
| DATA_IRREVOCABILITA | DATE | Data di irrevocabilità |
| FLAG_CUMULANTE | VARCHAR2 (1 CHAR) DEFAULT 'N' | Indica se il fascicola cumula |
| FLAG_CUMULATO | VARCHAR2 (1 CHAR) DEFAULT 'N' | Indica se il fascicolo è cumulato |
| COD_UFFICIO_UNIONE | VARCHAR2 (11 CHAR) DEFAULT '-' | Ufficio unificazione |
| ANNO_FASCICOLO_UNIONE | VARCHAR2 (4 CHAR) | Anno del fascicolo unificazione |
| NUM_FASCICOLO_UNIONE | VARCHAR2 (6 CHAR) | Numero del fascicolo unificazione |
| DATA_UNIONE | DATE | Data unificazione |
| KEY_PROVV_NSC | NUMBER | Chiave del provvedimento NSC |
| DATA_ARRIVO_ATTO. | DATE | Data di arrivo dell’atto |
| CHIAVE_PROGR_ORIG | NUMBER(38) | Identificativo del procedimento originario |
| CERTIFICATO_PENALE | BLOB | Contenuto del certificato del casellario centrale |
| VISIBILITA_EX_MINORENNE | VARCHAR2(1) | Flag che indica se è un ex minorenne |
| DATA_ULTIMA_RIAPERTURA | DATE | Data dell''ultima Riapertura del procedimento |
| COD_MOTIVO_RIAPERTURA | VARCHAR2(4) | Codice del Motivo_Provvedimento dell''ultima Riapertura |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| FAS_SIE_SEN_FK | SEN_ID_SENTENZA | (SENTENZA.ID_SENTENZA) |
| FAS_SIE_SOG_FK | SOG_ID_SOGGETTO | (SOGGETTO.ID_SOGGETTO) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| AGDG_FASCICOLO_SIEP | AGDG_FAS_SIE_FAS_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| ALTRA_CAUSA | ALT_CAU_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| ANNOTAZIONE_ESITO_TRASMISSIONE | ANN_ESITO_TRASMISS_FASSIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| ANNOTAZIONE_MANUALE | ANN_MAN_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| ARCHIVIAZIONE | ARC_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| AVVOCATO_FASCICOLO_SIEP | AVV_FAS_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| BENEFICIO | BEN_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| CAMPO_NOTA | CAM_NOT_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| CERTIFICATO_STATO_ESEC | CERT_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| CIRCOSTANZA | CIR_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| COMPETENZA | COMPETENZA_ID_FASC_SIEP_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| CUMULO | CUM_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| DECRETO_ORDINANZA_SIEP | DEC_SIE_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| EVENTO | EVE_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| FASCICOLO_SIEPE | FAS_SIEPE_FAS_SIEP_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| RIFERIMENTO_FASCICOLO_SIEP | FAS_SIE_ID_FASCICOLO_SIEP_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| POSIZIONE_MATERIALE_FASC | FAS_SIE_ID_POS_MAT_FASC | FAS_SIE_ID_FASCICOLO_SIEP |
| FASCICOLO_SIUS | FAS_SIU_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| FUNGIBILITA | FNG_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| LICENZA_LIBANTICIPATA | LIC_LIB_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| MAGISTRATO_COMPETENTE | MAG_COM_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| MAX_STATO_PROCEDIMENTO | MAX_STA_PRO_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| MISURA_CAUTELARE | MIS_CAU_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| MISURA_SICUREZZA | MIS_SIC_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| NOTE | NOTE_FAS_SIE_SIEP_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| NOTIZIA_REATO | NOT_REA_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| PENA_ACCESSORIA | PEN_ACC_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| PENA_COMPLESSIVA | PEN_COM_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| PENA_PECUNIARIA | PEN_PEC_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| PENA_PRESUNTA | PEN_PRE_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| PENA_RESIDUA | PEN_RES_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| PERIODO_ALTRA_MISURA | PER_MISU_FASCICOLO_SIEP_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| PERIODO_ALTRA_SANZIONE | PER_SANZ_FASCICOLO_SIEP_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| POSIZIONE_GIURIDICA | POS_GIU_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| REATO | REA_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| RIAPERTURA_FASCICOLO_SIEP | RIAPER_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| RICHIESTA_CONVERSIONE | RIC_CON_ID_FASC_SIEP_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| RICHIESTA_REMISSIONE | RIC_REM_ID_FASC_SIEP_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| RICHIESTA_SIGE | RIC_SIG_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| RIFERIMENTO_FASCICOLO_SIUS | RIF_SIU_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| SANZIONE_AMMINISTRATIVA | SAN_AMM_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| SCADENZARIO_SIEP | SCA_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| SOLLECITO_ESITO_TRASMISSIONE | SOLL_ESITO_TRASMISS_FASSIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| SOSPENSIONE | SOS_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| STATO_PROCEDIMENTO | STA_PRO_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| STORICO_SOGGETTO | STO_SOG_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |
| ULTERIORE_SANZIONE_CUMULO | ULT_SAN_CUM_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP |

# FASCICOLO_SIEP_BDMC
tabella contenente i dati relativi al fascicolo di bdmc. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_FASCICOLO_BDMC | NUMBER NOT NULL | Identificativo del fascicolo BDMC |
| CHIAVE_ANNO_BDMC | NUMBER NOT NULL | Anno del fascicolo BDMC |
| CHIAVE_UFFICIO_BDMC | VARCHAR2 (11 CHAR) NOT NULL | Ufficio del fascicolo BDMC |
| CHIAVE_PROGR_BDMC | NUMBER NOT NULL | Progressivo del fascicolo BDMC |
| CHIAVE_ANNO_SIEP | NUMBER NOT NULL | Anno del fascicolo SIEP |
| CHIAVE_UFFICIO_SIEP | VARCHAR2 (11 CHAR) NOT NULL | Ufficio del fascicolo SIEP |
| CHIAVE_PROGR_SIEP | NUMBER NOT NULL | Numero del fascicolo SIEP |
| FLAG_TRASMISSIONE | VARCHAR2 (1 CHAR) | S/N Flag trasmissione |
| DATA_TRASMISSIONE | DATE | Data di trasmissione |
| DATA_DISATTIVAZIONE | DATE | Data disattivazione |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMEN TO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| TIPO_MISURA | VARCHAR2 (2 CHAR) | Tipo di misura |
| ID_EVENTO | NUMBER | Identificativo dell’evento |
| FLAG_ORDINE_ESECUZIONE | CHAR (1 CHAR) | S/N Flag ordine esecuzione |
| ISTITUTO_DETENZIONE | VARCHAR2 (4 CHAR) | Codice dell’istituto di detenzione |
| ALTRO_LUOGO | VARCHAR2 (100 CHAR) | Descrizione altro luogo |
| COD_COMUNE | VARCHAR2 (6 CHAR). | Codice del comune |


# FASCICOLO_SIEPE
tabella contenente i dati relativi al fascicolo siepe. utilizzata dal sottosistema siepe.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_FASCICOLO_SIEPE | NUMBER NOT NULL | Chiave primaria della tabella |
| CHIAVE_ANNO | NUMBER NOT NULL | Anno del fascicolo SIEPE |
| CHIAVE_PROGR | NUMBER NOT NULL | Progressivo del fascicolo SIEPE |
| CHIAVE_UFFICIO | VARCHAR2 (11 CHAR) NOT NULL | Ufficio del fascicolo SIEPE |
| NUM_UEPE | NUMBER | Numero UEPE |
| ANNO_UEPE | NUMBER | Anno UEPE |
| PROGR_UEPE | NUMBER | Progressivo UEPE |
| COD_STATO_FASCICOLO | VARCHAR2 (2 CHAR) | Stato del fascicolo |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_ISCRIZIONE | DATE | Data di iscrizione del fascicolo |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMEN TO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| SOG_ID_SOGGETTO | NUMBER NOT NULL | Identificativo del soggetto |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER | Identificativo del fascicolo SIUS |
| COD_INCARICO | VARCHAR2 (4 CHAR) | Codice dell’incarico |
| NOTE | VARCHAR2 (1000 CHAR) | Note |
| COD_UFFICIO_MITTENTE | VARCHAR2 (11 CHAR) | Ufficio mittente |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| TIPO_DEFINIZIONE | VARCHAR2 (2 CHAR) | Tipologia di definizione |
| DATA_DEFINIZIONE | DATE | Data definizione |
| DESCR_DEFINIZIONE | VARCHAR2 (2000 CHAR). | Descrizione della definizione |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| FAS_SIEPE_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| FAS_SIEPE_FAS_SIEP_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |
| FAS_SIEPE_FAS_SIUS_FK | FAS_SIU_ID_FASCICOLO_SIUS | (FASCICOLO_SIUS.ID_FASCICOLO_SIUS) |
| FAS_SIEPE_SOG_FK | SOG_ID_SOGGETTO | (SOGGETTO.ID_SOGGETTO) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| ATTIVITA | ATT_FAS_SIEPE_FK | FAS_SIE_ID_FAS_SIEPE |
| RICHIESTA | RIC_FAS_SIEPE_FK | FAS_SIE_ID_FAS_SIEPE |


# FASCICOLO_SIGE
tabella contenente i dati relativi al fascicolo sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_FASCICOLO_SIGE | NUMBER NOT NULL | Chiave primaria. |
| SOG_ID_SOGGETTO | NUMBER NOT NULL | ID del soggetto cui si riferisce il fascicolo. |
| CHIAVE_ANNO | NUMBER NOT NULL | Parte di chiave secondaria.
ANNO/PROGR individuano univocamente il Fascicolo nell'Ufficio |
| CHIAVE_UFFICIO | VARCHAR2 (11 CHAR)  NOT NULL | Ufficio di competenza. |
| CHIAVE_PROGR | NUMBER NOT NULL | Parte di chiave secondaria.
ANNO/PROGR individuano univocamente il Fascicolo nell'Ufficio |
| COD_STATO_FASCICOLO | VARCHAR2 (2 CHAR) NOT NULL | Stato del Fascicolo. |
| COD_TIPO_GIUDIZIO | VARCHAR2 (2 CHAR) | Tipo di giudizio: Monocratico/Collegiale. |
| DATA_ISCRIZIONE | DATE NOT NULL | Data di iscrizione del Fascicolo. |
| DATA_DEFINIZIONE | DATE
DEFAULT null | Data nella quale il Fascicolo viene DEFINITO. |
| RIC_ID_RICHIESTA_SIGE | NUMBER NOT NULL | ID della Richiesta generante il Fascicolo. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) NOT NULL | Codice dell’operatore che ha inserito il record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) NOT NULL | Data di inserimento del record |
| DATA_INSERIMENTO | DATE NOT NULL | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR)
DEFAULT NULL | Codice dell’operatore che ha aggiornato il record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR)
DEFAULT NULL | Data di aggiornamento del record |
| DATA_AGGIORNAMENTO | DATE
DEFAULT NULL | Ufficio dell’operatore che ha aggiornato il record |
| NOTE | VARCHAR2 (2000 CHAR) | Note a testo libero. |
| COD_POSIZIONE_GIURIDICA | VARCHAR2 (2 CHAR) | Codice della Posizione Giuridica. |
| DATA_FINE_PENA | DATE
DEFAULT NULL | Data di Fine Pena. |
| SEZ_ID_SEZIONE | NUMBER
DEFAULT NULL | ID della Sezione di competenza. |
| COD_TIPO_DEFINIZIONE | VARCHAR2 (2 CHAR)
DEFAULT NULL | Codice del tipo di definizione del Procedimento. |
| DESCR_DEFINIZIONE | VARCHAR2 (2000 CHAR)
DEFAULT NULL | Ulteriore descrizione della Definizione del Procedimento. Usato per definizione manuale. |
| FAS_SIG_ID_FASCICOLO_SIGE | NUMBER | Identificativo del fascicolo SIGE |
| NUMERO_FASCICOLI_UNIFICATI | NUMBER | Numero dei fascicoli unificati |
| CHIAVE_PROGR_ORIG | NUMBER | Chiave del progressivo origine |
| SEN_ID_SENTENZA_CUMULO | NUMBER | Identificativo della sentenza di cumulo |
| ID_FASCICOLO_SIGE_ORIGINE | NUMBER | Identificativo del SIGE origine |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| FAS_SIG_RIC_SIG_FK | RIC_ID_RICHIESTA_SIGE | (RICHIESTA_SIGE.ID_RICHIESTA_SIGE) |
| FAS_SIG_SEZ | SEZ_ID_SEZIONE | (SEZIONE.ID_SEZIONE) |
| FAS_SIG_SOG_FK | SOG_ID_SOGGETTO | (SOGGETTO.ID_SOGGETTO) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| AVVOCATO_FASCICOLO_SIGE | AVV_FAS_SIGE_FASCICOLO_SIGE_FK | FAS_SIGE_ID_FASCICOLO_SIGE |
| TENORE_SIGE | FAS_ID_FASCICOLO_SIGE_FK | FAS_ID_FASCICOLO_SIGE |
| FAS_SIGE_DETENZIONE | FAS_SIGE_DET_FK | FAS_ID_FAS_SIGE |
| FAS_SIGE_SENTENZA | FAS_SIGE_ID_FAS_FK | FAS_ID_FASCICOLO_SIGE |
| POSIZIONE_MATERIALE_FASC_SIGE | FAS_SIGE_ID_POS_MAT_FAS | FAS_SIGE_ID_FASCICOLO_SIGE |
| MAGISTRATO_ASSEGNATARIO | MAG_ASS_FAS_SIE_FK | FAS_SIGE_ID_FASCICOLO_SIGE |
| PROVVEDIMENTO_SIGE | PROV_FAS_SIGE_FK | FAS_ID_FASCICOLO_SIGE |
| RESIDENZA_FASCICOLO_SIGE | RES_FAS_SIGE_FAS_SIGE_FK | FAS_SIGE_ID_FASCICOLO_SIGE |
| SCADENZARIO_SIGE | SCA_FAS_SIGE_FK | FAS_ID_FASCICOLO_SIGE |
| UDIENZA_PROCEDIMENTO_SIGE | UDI_PRO_FAS_SIG_FK | FAS_ID_FASCICOLO_SIGE |



# FASCICOLO_SIUS
tabella contenente i dati relativi al fascicolo sius. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_FASCICOLO_SIUS | NUMBER NOT NULL | Chiave naturale della tabella "Fascicolo_sius" legata a sequence "FAS_SIU_SEQ". Necessaria per le relazioni con le altre tabelle nelle quali sarà identificata come foreign key. |
| CHIAVE_ANNO | NUMBER NOT NULL | Anno di registrazione del Fascicolo. |
| CHIAVE_UFFICIO | VARCHAR2 (11 CHAR) NOT NULL | Codice dell'Ufficio titolare del Fascicolo SIUS. |
| CHIAVE_PROGR | NUMBER NOT NULL | Progressivo di registrazione del Fascicolo. |
| COD_STATO_FASCICOLO | VARCHAR2 (2 CHAR) | Codifica dello stato fascicolo. Può assumere valori quali: 01=Archiviato/Definito
02=Iscritto 03=Validato
....
Associato al dominio STATO_FASCICOLO. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMEN TO) | VARCHAR2 (100 CHAR | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| SOG_ID_SOGGETTO | NUMBER NOT NULL | Identificativo del soggetto |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| DATA_ISCRIZIONE | DATE | Data di Iscrizione del Fascicolo. |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER | Identificativo del fascicolo SIUS |
| DATA_DEFINIZIONE | DATE | Data di variazione dello stato del Fascicolo. |
| ID_FASCICOLO_SIUS_ORIGINE | NUMBER | Identificativo del Fascicolo SIUS che ha dato origine al Fascicolo in questione. Valorizzato solo in circostanze come la "Presa in carico" di Decreti/Ordinanze da altre BDI o quando si decide di iscrivere un "procedimento collegato". |
| NUMERO_FASCICOLI_UNIFICATI. | NUMBER | Numero totale di fascicoli unificati a quello in oggetto. Viene inizializzato a "0". |
| CERTIFICATO_PENALE | BLOB | Contenuto del certificato del casellario centrale |
| VISIBILITA_EX_MINORENNE | VARCHAR2(1) | Flag che indica se è un ex minorenne |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| FAS_SIU_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |
| FAS_SIU_SOG_FK | SOG_ID_SOGGETTO | (SOGGETTO.ID_SOGGETTO) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| CURATORE_SIUS | CUR_SIUS_FK | FAS_SIU_ID_FASCICOLO_SIUS |
| EVENTO | EVE_FAS_SIU_FK | FAS_SIU_ID_FASCICOLO_SIUS |
| FASCICOLO_SIEPE | FAS_SIEPE_FAS_SIUS_FK | FAS_SIU_ID_FASCICOLO_SIUS |
| CANC_ASS_FASC_SIUS | FAS_SIUS_ID_CAN_ASS_FASC_SIUS | FAS_SIUS_ID_FASCICOLO_SIUS |
| POSIZIONE_MATERIALE_FASC_SIUS | FAS_SIUS_ID_POS_MAT_FASC_SIUS | FAS_SIUS_ID_FASCICOLO_SIUS |
| RIFERIMENTO_FASCICOLO_SIEP | FAS_SIU_ID_FASCICOLO_SIUS_FK | FAS_SIU_ID_FASCICOLO_SIUS |
| GENERALE_PROCEDIMENTO | GEN_PRO_FAS_SIU_FK | FAS_SIU_ID_FASCICOLO_SIUS |
| LICENZA_LIBANTICIPATA | LIC_LIB_FAS_SIU_FK | FAS_SIU_ID_FASCICOLO_SIUS |
| MAGISTRATO_RELATORE | MAG_REL_FAS_SIU_FK | FAS_SIU_ID_FASCICOLO_SIUS |
| NOTE | NOTE_FAS_SIU_SIUS_FK | FAS_SIU_ID_FASCICOLO_SIUS |
| PERIODO_ALTRA_MISURA | PER_MISU_FASCICOLO_SIUS_FK | FAS_SIU_ID_FASCICOLO_SIUS |
| PERIODO_ALTRA_SANZIONE | PER_SANZ_FASCICOLO_SIUS_FK | FAS_SIU_ID_FASCICOLO_SIUS |
| SCADENZARIO_SIUS | SCA_FAS_SIU_FK | FAS_SIU_ID_FASCICOLO_SIUS |
| STORICO_SOGGETTO | STO_SOG_FAS_SIUS_FK | FAS_SIE_ID_FASCICOLO_SIUS |


# FASC_MS_TO_FASC_SIEP
tabella contenente i dati relativi al fascicolo di misure di sicurezza preso in carico e iscritto dal sistema siep. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_FASC_MS_TO_FASC_SIEP | NUMBER (38) | Chiave della tabella |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER (38) | FK al fascicolo SIEP |
| CHIAVE_ANNO_SIEP | NUMBER (4) | Identificativo del fascicolo  SIEP |
| CHIAVE_PROGR_SIEP | NUMBER (38) | Progressivo del fascicolo SIEP |
| CHIAVE_UFFICIO_SIEP | VARCHAR2 (11) | Ufficio del fascicolo SIEP |
| COD_TIPO_RELAZIONE_MS | VARCHAR2 (240) | Tipo di Collegamento tra il fascicolo corrente e quello collegato: IN_ESECUZIONE_DI/ISCRITTO_AL
IN_ESECUZIONE_DI: indica che il fascicolo corrente è IN esecuzione del fascicolo collegato ovvero è in fascicolo di classe IV iscritto a seguito della presa in carico di un fascicolo di classe I o classe IV trasmesso per l’esecuzione.
ISCRITTO_AL: indica che il fascicolo corrente è stato trasmesso per competenza ed il fascicolo collegato è stato iscritto a partire da quello corrente. |
| FAS_SIE_ID_FASCICOLO_COLLEGATO | NUMBER (38) | FK al fascicolo di classe IV se presente sulla base dati |
| CHIAVE_ANNO_SIEP_COLLEGATO | NUMBER (4) | Identificativo del fascicolo collegato: anno numero e ufficio |
| CHIAVE_PROGR_SIEP_COLLEGATO | NUMBER (38) | Progressivo del fascicolo SIEP collegato |
| CHIAVE_UFFICIO_SIEP_COLLEGATO | VARCHAR2 (11) | Ufficio del fascicolo SIEP collegato |
| MES_ID_MESSAGGIO | NUMBER (38) | Eventuale id del messaggio di richiesta di presa in carico a seguito del quale è stata effettuata l'iscrizione. |
| EVE_ID_EVENTO | NUMBER (38) | FK all'eventuale evento di annotazione iscrizione in classe IV |
| DATA_CUMULO | DATE | Eventuale data ultimo cumulo del fascicolo collegato di iscrizione delle MS |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Ufficio dell’operatore che ha aggiornato il record |



# FAS_SIGE_DETENZIONE
tabella associativa tra Luogo_detenzione e Fascicolo_sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_FAS_SIGE_DETENZIONE | NUMBER NOT NULL | Chiave primaria. |
| FAS_ID_FAS_SIGE | NUMBER NOT NULL | ID univoco del FASCICOLO_SIGE. |
| LD_ID_LUOGO_DETENZIONE | NUMBER DEFAULT null | ID univoco del LUOGO_DETENZIONE. |
| DATA_INSERIMENTO | DATE NOT NULL | Data di inserimento del record |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (11 CHAR) NOT NULL | Codice dell’operatore che ha inserito il record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) NOT NULL | Ufficio dell’operatore che ha inserito il record |
| DATA_AGGIORNAMENTO | DATE
DEFAULT null | Codice dell’operatore che ha aggiornato il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| AC_ID_ALTRA_CAUSA | NUMBER
DEFAULT null | Identificativo altra causa |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| FAS_SIGE_DETEN_ALTRA_FK | AC_ID_ALTRA_CAUSA | (ALTRA_CAUSA.ID_ALTRA_CAUSA) |
| FAS_SIGE_DET_FK | FAS_ID_FAS_SIGE | (FASCICOLO_SIGE.ID_FASCICOLO_SIGE) |
| FAS_SIGE_DET_LUOGO_FK | LD_ID_LUOGO_DETENZIONE | (LUOGO_DETENZIONE.ID_LUOGO_DETENZIONE) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| BENEFICIO_SENTENZA_SIGE | BEN_FAS_SIGE_SEN_FK | FAS_SIGE_SEN_ID |
| REATO_SENTENZA_SIGE | FAS_SIGE_SENTENZA_FK | FAS_SIGE_SEN_ID |
| PENA_ACCESSORIA_SENTENZA_SIGE | PNA_FAS_SIGE_SEN_FK | FAS_SIGE_SEN_ID |
| PENA_COMPLESSIVA_SENTENZA_SIGE | PNC_FAS_SIGE_SEN_FK | FAS_SIGE_SEN_ID |



# FAS_SIGE_SENTENZA
tabella associativa tra Sentenza e Fascicolo_sige. utilizzata dal sottosistema siep-sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_FAS_SIGE_SENTENZA | NUMBER NOT NULL | Chiave primaria. |
| FAS_ID_FASCICOLO_SIGE | NUMBER NOT NULL | ID del Fascicolo SIGE. |
| SEN_ID_SENTENZA | NUMBER NOT NULL | ID della Sentenza. |
| DATA_INSERIMENTO | DATE NOT NULL | Data di inserimento del record |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (11 CHAR) NOT NULL | Codice dell’operatore che ha inserito il record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) NOT NULL | Ufficio dell’operatore che ha inserito il record |
| DATA_IRREVOCABILITA | DATE | Data di irrevocabilità della sentenza per quel procedimento. |
| FLAG_COMPETENZA | VARCHAR2 (1 CHAR)
DEFAULT NULL | Definisce il Titolo che conferisce la competenza al procedimento. |
| DATA_AGGIORNAMENTO | DATE | Codice dell’operatore che ha aggiornato il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER
DEFAULT NULL | ID Fascicolo SIEP afferente |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| FAS_SIGE_ID_FAS_FK | FAS_ID_FASCICOLO_SIGE | (FASCICOLO_SIGE.ID_FASCICOLO_SIGE) |
| FAS_SIGE_SEN_FK | SEN_ID_SENTENZA | (SENTENZA.ID_SENTENZA) |



# FUNGIBILITA
tabella contenente i dati relativi alla fungibilità. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_FUNGIBILITA | NUMBER NOT NULL | Chiave numerica naturale della tabella. |
| COD_TIPO_FUNGIBILITA | VARCHAR2 (2 CHAR) | Indica la tipologia di fungibilità da utilizzare. Deriva da dominio e può assumere i seguenti valori:
FUNGIBILITA
PENA ESPIATA IN ECCESSO PENA SENZA TITOLO |
| NUM_ANNI | NUMBER | Quantità di anni a disposizione per la fungibilità |
| NUM_MESI | NUMBER | Quantità di mesi a disposizione per la fungibilità |
| NUM_GIORNI | NUMBER | Quantità di giorni a disposizione per la fungibilità |
| DATA_DA | DATE | Identifica l'inizio del periodo di fungibilità. |
| DATA_A | DATE | Identifica la fine del periodo di fungibilità. |
| DATA_INIZIO_VALIDITA | DATE | Data dalla quale considerare la fruibilità della fungibilità. |
| DATA_FINE_VALIDITA | DATE | Data finale di fruibilità della fungibilità. |
| COD_UFFICIO_FRUITORE | VARCHAR2 (11 CHAR) | Codice dell' ufficio che eventualmente ha disposto del periodo di fungibilità. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMEN TO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| FLAG_VALIDATO | VARCHAR2 (1 CHAR). | Flag che indica se la Fungibilità risulta o meno validata. |
| NUM_GIORNI_FRUITI | NUMBER | Numero di giorni fruiti |
| NUM_GIORNI_NON_FRUITI | NUMBER | Numero di giorni non fruiti |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| FNG_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| FNG_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |



# FUNZIONE
tabella contenente il censimento delle funzionalità del sistema SIES. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_FUNZIONE | NUMBER NOT NULL | Chiave primaria dell'entità |
| DESCRIZIONE | VARCHAR2 (60 CHAR) | Testo con scopo puramente descrittivo della funzione |
| COD_TIPO_FUNZIONE | VARCHAR2 (1 CHAR) NOT NULL | Codice che identifica l'appartenenza al menù gerarchico o al contesto. Deriva dal dominio TIPO_FUNZIONE |
| AZIONE_CONTESTO_JAVA | VARCHAR2 (100 CHAR). | Identifica l'azione java che deve essere eseguita al click del pulsante di menù |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| FUNZIONE_PROFILO | FUN_PRO_FUN_FK | FUN_ID_FUNZIONE |
| RELAZIONE_FUNZIONE | REL_FUN_FUN_FIGLIA_FK | FUN_ID_FUNZIONE_FIGLIA |
| RELAZIONE_FUNZIONE | REL_FUN_FUN_FK | FUN_ID_FUNZIONE |


# FUNZIONE_PROFILO
tabella associativa tra Funzione e Profilo. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| DATA_INIZIO_VALIDITA | DATE NOT NULL | Data di Inizio Validità dell' accesso alla funzione da parte di un profilo. Questa data viene compilata con la data di sistema ogni volta che l'utente stabilisce l'accesso ad una funzione da parte di un profilo. |
| DATA_FINE_VALIDITA | DATE | Data di Fine Validità dell' accesso alla funzione da parte di un profilo. Questa data viene compilata con la data di sistema solo quando l'utente richiede di disabilitare l'accesso ad una funzione da parte di un profilo. L' accesso è abilitato solo se questa data è = NULL altrimenti l'accesso è stato disabilitato ma si vuole mantenere questa informazione per la storicizzazione dei dati. |
| FUN_ID_FUNZIONE | NUMBER NOT NULL | Identificativo della funzione |
| PRF_COD_PROFILO | NUMBER NOT NULL | Identificativo del profilo |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Ufficio dell’operatore che ha inserito il record |
| DATA_AGGIORNAMENTO | DATE | Data  aggiornamento del record |
| FLAG_ATTIVO | VARCHAR2 (1 CHAR) DEFAULT 'S' NOT NULL. | S/N flag attivo |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| FUN_PRO_FUN_FK | FUN_ID_FUNZIONE | (FUNZIONE.ID_FUNZIONE) |
| FUN_PRO_PRF_FK | PRF_COD_PROFILO | (PROFILO.COD_PROFILO) |







# FUNZIONI_TESTATE
tabella di lavoro utilizzata per test. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| FUN_ID_FUNZIONE | NUMBER |  |
| FLAG_TESTATO | CHAR (1 CHAR) |  |



# GENERALE_PROCEDIMENTO
tabella relativa ai dati generali del procedimento sius. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_GENERALE_PROCEDIMENTO | NUMBER NOT NULL | Chiave primaria dell'entità. Collegata al Fascicolo SIUS. |
| ANNO_S1 | NUMBER NOT NULL | Anno del Registro S1 (Registro Generale dei Procedimenti). |
| PROGR_S1 | NUMBER NOT NULL | Progressivo del Registro S1. |
| COD_TIPO_REGISTRO | VARCHAR2 (3 CHAR) DEFAULT NULL | Codifica del Tipo Registro. Associato al dominio COD_TIPO_REGISTRO |
| COD_OGGETTO_PROCEDIMENTO | VARCHAR2 (4 CHAR) | Codifica dell’Oggetto Procedimento. Associato al dominio OGGETTO_PROCEDIMENTO |
| DATA_RICHIESTA | DATE | Data di immissione dati del Fascicolo |
| DATA_ARRIVO_CANCELLERIA | DATE | Data di arrivo in Cancelleria |
| DATA_CAMERA_CONSIGLIO | DATE | Data di Udienza |
| DESCR_RICHIESTA_DELEGAZIONE | VARCHAR2 (2000 CHAR) | Descrizione della richiesta della delegazione |
| COD_AUTORITA_DELEGATA | VARCHAR2 (9 CHAR) | Codice dell’autorità delegata |
| DATA_RESTITUZ_DELEGAZIONE | DATE | Data restituzione delegazione |
| DATA_RICORSO_IMPUGN | DATE | Data di ricorso dell’impugnazione |
| DATA_INVIO_ATTI_IMPUGN | DATE | Data invio atti dell’impugnazione |
| DATA_INVIO_ESECUZ_PROVVISORIA | DATE | Data invio esecuzione provvisoria |
| DATA_INVIO_ESECUZ_ORDINARIA | DATE | Data invio esecuzione ordinaria |
| DATA_COMPILAZ_COMPLEMENTARE | DATE | Data compilazione foglio complementare |
| COD_TIPO_FOGLIO_COMPLEMENT ARE | VARCHAR2 (2 CHAR) | Tipologia di foglio complementare |
| DATA_ANNOTAZIONE | DATE | Data di annotazione |
| ANNOTAZIONE | VARCHAR2 (2000 CHAR) | Annotazione |
| TIPO_DEFINIZIONE | VARCHAR2 (2 CHAR) | Tipo di definizione |
| DATA_DEFINIZIONE | DATE | Data di definizione |
| DESCR_DEFINIZIONE | VARCHAR2 (2000 CHAR) | Descrizione della definizione |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMEN TO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| COD_TIPO_ATTO | VARCHAR2 (2 CHAR) | Tipologia dell’atto |
| COD_SEDE_MITTENTE | VARCHAR2 (6 CHAR) | Sede del mittente |
| COD_TIPO_MITTENTE_ATTO | VARCHAR2 (2 CHAR) | Tipologia dell’atto del mittente |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER NOT NULL | Identificativo del fascicolo SIUS |
| SEZIONE | VARCHAR2 (3 CHAR) | Sezione |
| DATA_FINE_PENA | DATE | Data dine pena |
| COD_POSIZIONE_GIURIDICA | VARCHAR2 (2 CHAR) | Codice della posizione giuridica |
| UDI_ID_UDIENZA | NUMBER | Identificativo dell’udienza |
| DESCR_MITTENTE | VARCHAR2 (200 CHAR) | Descrizione del mittente |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| GEN_PRO_FAS_SIU_FK | FAS_SIU_ID_FASCICOLO_SIUS | (FASCICOLO_SIUS.ID_FASCICOLO_SIUS) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| DEPOSITO_DECRETO | DEP_DEC_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO |
| DEPOSITO_ORDINANZA_PC | DEP_OPC_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO |
| ESECUZIONE_MISURA_SICUREZZA | EMS_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO |
| ESECUZIONE_MISURA_ALTERNATIVA | EXE_MIS_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO |
| ESECUZIONE_SANZIONE_SOST | EXE_SAN_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO |
| MOVIMENTO_REG_ESECUZIONE | MOV_REG_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO |
| RINVIO_PROVVEDIMENTO | RIN_PRO_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO |
| TENORE | TEN_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO |
| UDIENZA_PROCEDIMENTO | UDI_PRO_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO |


# GIUDICE_POPOLARE
tabella contenente l’anagrafica dei giudici popolari. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_GIUDICE_POPOLARE | NUMBER NOT NULL | ID Giudice Popolare |
| COGNOME | VARCHAR2 (50 CHAR) NOT NULL | Cognome |
| NOME | VARCHAR2 (50 CHAR) | Nome |
| INDIRIZZO | VARCHAR2 (200 CHAR) | Indirizzo |
| COD_UFFICIO_APPARTENENZA | VARCHAR2 (11 CHAR) | Codice Ufficio di Appartenenza |
| DATA_INIZIO_VALIDITA | DATE NOT NULL | Data Inizio Validità |
| DATA_FINE_VALIDITA | DATE | Data Fine Validità |
| COD_RUOLO | VARCHAR2 (1 CHAR) NOT NULL | Codice Ruolo |
| CODICE_FISCALE | VARCHAR2 (16 CHAR) | Codice Fiscale |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice Operatore Inserimento |
| DATA_INSERIMENTO | DATE | Data Inserimento |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Codice Ufficio Inserimento |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice Operatore Aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data Aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Codice Ufficio Aggiornamento |
| DATA_NASCITA | DATE NOT NULL | Data di Nascita |
| COD_COMUNE_NASCITA | VARCHAR2 (6 CHAR) | Codice Comune di nascita |
| COMUNE_ESTERO_NASCITA | VARCHAR2 (100 CHAR) | Comune Estero di Nascita |
| COD_SESSO | VARCHAR2 1 CHAR) NOT NULL | Sesso |
| SEZ_ID_SEZIONE | NUMBER | Id della sezione di riferimento. |
| COD_STATO_NASCITA | VARCHAR2 (3 CHAR). | Codice dello stato di nascita |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| COLLEGIO_GIUDICE_POPOLARE | COL_GIU_POP_GIU_POP_FK | GIU_POP_ID_GIUDICE_POPOLARE |



# HELPONLINE
tabella utilizzata per l’help online di sius. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| FUN_ID_FUNZIONE | NUMBER NOT NULL | Identificativo della funzione |
| NOME_PAGINA | VARCHAR2 (100 CHAR). | Nome della pagina |



# IMPUGNAZIONE
tabella contenente i dati relativi all’impugnazione. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_IMPUGNAZIONE | NUMBER NOT NULL | Chiave naturale della tabella. Legata a Sequence IMP_SEQ. |
| ANNO_S7 | NUMBER NOT NULL | Anno del Registro S07. |
| PROGR_S7 | NUMBER NOT NULL | Progressivo del Registro S07. |
| COD_TIPO_IMPUGNAZIONE | VARCHAR2 (2 CHAR) | Codifica del Tipo Impugnazione/Ricorso (Ricorso Appello Reclamo). Associato al Dominio TIPO_RICORSO di CG_REF_CODES. |
| SOGGETTO_IMPUGNANTE | VARCHAR2 (240 CHAR) | Denominazione del soggetto impugnante |
| DATA_RICORSO | DATE NOT NULL | Data del ricorso |
| DATA_ANNOTAZIONE | DATE | Data dell’annotazione |
| ANNOTAZIONE | VARCHAR2 (200 CHAR) | Descrizione dell’annotazione |
| DATA_ARRIVO_CANCELLERIA | DATE | Data arrivo cancelleria |
| DATA_TRASMISSIONE_ATTI | DATE | Data di trasmissione degli atti |
| COD_AUTORITA_DESTINATARIA | VARCHAR2 (11 CHAR) | Codice dell’autorità destinataria |
| DATA_DECISIONE | DATE | Data della decisione |
| COD_TENORE_DECISIONE | VARCHAR2 (2 CHAR) | Codice del tenore della decisione |
| DATA_RESTITUZIONE_ATTI | DATE | Data restituzione atti |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| DEP_OPID_DEPOSITO_ORDINANZA_PC | NUMBER | Identificativo del deposito dell’ordinanza |
| DEP_DEC_ID_DEPOSITO_DECRETO | NUMBER | Identificativo del deposito del decreto |
| FLAG_ANNULLAMENTO | VARCHAR2 (1 CHAR) | Flag annullamento |
| DATA_ANNULLAMENTO | DATE | Data dell’annullamento |
| MOTIVO_ANNULLAMENTO | VARCHAR2 (2000 CHAR) | Motivo dell’annullamento |
| FLAG_SOSP_ESEC | VARCHAR2 (1 CHAR). | Flag sospensione dell’esecuzione |
| DEP_ID_DEPOSITO_SENTENZA | NUMBER | Identificativo del deposito della sentenza |
| DESCRIZIONE_ALTRO | VARCHAR2 (100) | Altra descrizione |


Chiavi Esterne

| CONSTRAINT_NAME | CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN | REFERENCES_COLUMN |  |
| --- | --- | --- | --- | --- | --- |
| IMP_DEP_DEC_FK | DEP_DEC_ID_DEPOSITO_DECRETO | DEP_DEC_ID_DEPOSITO_DECRETO | DEP_DEC_ID_DEPOSITO_DECRETO | (DEPOSITO_DECRETO.ID_DEPOSITO_DECRETO) | (DEPOSITO_DECRETO.ID_DEPOSITO_DECRETO) |
| IMP_DEP_OPC_FK | DEP_OPID_DEPOSITO_ORDINANZA_PC | DEP_OPID_DEPOSITO_ORDINANZA_PC | DEP_OPID_DEPOSITO_ORDINANZA_PC | (DEPOSITO_ORDINANZA_PC.ID_DEPOSITO_ORDINANZA_PC) | (DEPOSITO_ORDINANZA_PC.ID_DEPOSITO_ORDINANZA_PC) |
| IMP_DEP_SEN_FK | DEP_ID_DEPOSITO_SENTENZA | DEP_ID_DEPOSITO_SENTENZA | DEP_ID_DEPOSITO_SENTENZA | (DEPOSITO_SENTENZA.ID_DEPOSITO_SENTENZA) | (DEPOSITO_SENTENZA.ID_DEPOSITO_SENTENZA) |

# IMPUGNAZIONE_SIGE
tabella contenente i dati relativi all’impugnazione relativamente ad un fascicolo sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_IMPUGNAZIONE_SIGE | NUMBER NOT NULL | Chiave naturale della tabella. Legata a Sequence IMP_SIGE_SEQ. |
| ANNO_S7 | NUMBER NOT NULL | Anno del Registro S07. |
| PROGR_S7 | NUMBER NOT NULL | Progressivo del Registro S07. |
| COD_TIPO_IMPUGNAZIONE | VARCHAR2 (2 CHAR) | Codifica del Tipo Impugnazione/Ricorso (Ricorso Appello Reclamo). Associato al Dominio TIPO_RICORSO_SIGE di CG_REF_CODES. |
| SOGGETTO_IMPUGNANTE | VARCHAR2 (240 CHAR) | Generalità Soggetto Impugnante. |
| DATA_RICORSO | DATE NOT NULL | Data del ricorso |
| DATA_ANNOTAZIONE | DATE | Data annotazione |
| ANNOTAZIONE | VARCHAR2 (200 CHAR) | Descrizione dell’annotazione |
| DATA_ARRIVO_CANCELLERIA | DATE | Data arrivo cancelleria |
| DATA_TRASMISSIONE_ATTI | DATE | Data di trasmissione degli atti |
| COD_AUTORITA_DESTINATARIA | VARCHAR2 (11 CHAR) | Codice dell’autorità destinataria |
| DATA_DECISIONE | DATE | Data della decisione |
| COD_TENORE_DECISIONE | VARCHAR2 (2 CHAR) | Codice del tenore della decisione |
| DATA_RESTITUZIONE_ATTI | DATE | Data restituzione atti |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMEN TO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| PROVV_ID_PROVVEDIMENTO_SIGE | NUMBER | Identificativo del provvedimento SIGE |
| FLAG_ANNULLAMENTO | VARCHAR2 (1 CHAR) | Flag annullamento |
| DATA_ANNULLAMENTO | DATE | Data dell’annullamento |
| MOTIVO_ANNULLAMENTO | VARCHAR2 (2000 CHAR) | Motivo dell’annullamento |
| FLAG_SOSP_ESEC | VARCHAR2 (1 CHAR). | Flag sospensione dell’esecuzione |
| PROVV_ID_PROVV_GENERATO | NUMBER | Identificativo del provvedimento generato |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| IMP_PROVV_SIGE_FK | PROVV_ID_PROVVEDIMENTO_SIGE | (PROVVEDIMENTO_SIGE.ID_PROVVEDIMENTO_SIGE) |

# INCARICO_ATTIVITA
tabella associativi tra Incarico e Attività. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| RV_INCARICO | VARCHAR2 (240 CHAR) NOT NULL | RV_LOW_VALUE di INCARICO in CG_REF_CODES |
| RV_ATTIVITA | VARCHAR2 (240 CHAR) NOT NULL. | RV_LOW_VALUE di ATTIVITA in CG_REF_CODES |


# invocazione_pagopa
La tabella contiene i dati relativi all’invocazione della richiesta (batch) di controllo bollettini per il colloquio col sistema PST_PagoPA. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| id_invocazione_pagopa | NUMBER(38) NOT NULL | Primary Key della tabella, indica l’identificativo univoco della invocazione |
| data_invocazione | DATE NOT NULL | Indica la data dell’invocazione |
| codice_fiscale | VARCHAR2(16) | Indica il codice fiscale del soggetto |
| iuv | VARCHAR2(35) | Indica l’Identificativo Univoco di Versamento |
| xml_richiesta | VARCHAR2(2000) | Indica l’xml per l’invocazione del web service |
| xml_risposta | VARCHAR2(2000) | Indica l’xml per la risposta del web service |
| errore | VARCHAR2(2000) | Indica l’errore verificatosi |
| fk_id_batch | NUMBER(38) | Indica l’identificativo del batch invocato |
| cod_operatore_inserimento | VARCHAR2(100 CHAR) | Indica il codice dell’operatore che ha lanciato l’invocazione del batch |
| data_inserimento | DATE | Indica la data di invocazione del batch |
| cod_ufficio_inserimento | VARCHAR2(11 CHAR) | Indica il codice dell’ufficio dell’operatore che ha lanciato l’invocazione del batch |
| cod_operatore_aggiornamento | VARCHAR2(100 CHAR) | Indica il codice dell’operatore che ha rilanciato l’invocazione del batch |
| data_aggiornamento | DATE | Indica la data di re-invocazione del batch |
| cod_ufficio_aggiornamento | VARCHAR2(11 CHAR) | Indica il codice dell’ufficio dell’operatore che ha rilanciato l’invocazione del batch |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| bollettino_batch_pagopa | bollbatch_invocazione_fk | fk_id_invocazione_pagopa |


# ISP_ESITO_PROVVEDIMENTO
tabella utilizzata per le statistiche relative agli esiti di un provvedimento. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_ESITO_PROVVEDIMENTO | VARCHAR2 (4 CHAR) NOT NULL | Chiave naturale della tabella. Legata a Sequence IMP_SIGE_SEQ. |
| ISP_COD_ESITO_PROVVEDIMENTO | VARCHAR2 (1 CHAR) | Codice dell’esito del provvedimento |
| DESCRIZIONE_ESITO_PROVV | VARCHAR2 (200 CHAR) | Descrizione esito del provvedimento |
| ISP_DESCRIZIONE_ESITO_PROVV | VARCHAR2 (200 CHAR). | Descrizione per l’ispezione dell’esito del provvedimento |


# isp_motivo_attivita
tabella utilizzata per le statistiche relative al motivo delle attività di un provvedimento. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_MOTIVO | VARCHAR2 (4 CHAR) | Codice del motivo dell’attività. |
| DESCRIZIONE_ MOTIVO | VARCHAR2 (500 CHAR) | Descrizione del motivo dell’attività. |
| COD_ATTIVITA | VARCHAR2 (2 CHAR) | Codice dell’attività. |
| PROGR | VARCHAR2 (3 CHAR). | Progressivo della statistica. |


# ISP_MOTIVO_ATTIVITA_MS
tabella utilizzata per le statistiche relative al motivo delle attività di un provvedimento di misure di sicurezza. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_MOTIVO | VARCHAR2 (4 CHAR) | Codice del motivo dell’attività. |
| DESCRIZIONE_ MOTIVO | VARCHAR2 (500 CHAR) | Descrizione del motivo dell’attività. |
| COD_ATTIVITA | VARCHAR2 (2 CHAR) | Codice dell’attività. |
| TIPO_MS | VARCHAR2 (3 CHAR). | Tipologia della misura di sicurezza. Associato al Dominio TIPO_MISURA_SICUREZZA di CG_REF_CODES. |
| PROGR | VARCHAR2 (3 CHAR). | Progressivo della statistica. |


# ISP_OGGETTO_PROCEDIMENTO
tabella utilizzata per le statistiche relative agli oggetti di un provvedimento. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_OGGETTO_PROCEDIMENTO | VARCHAR2 (4 CHAR) NOT NULL | Codice dell’oggetto del procedimento |
| ISP_COD_OGGETTO_PROCEDIMENTO | VARCHAR2 (20 CHAR) | Codice dell’oggetto del procedimento per l’ispezione |
| DESCRIZIONE_OGGETTO_PROC | VARCHAR2 (200 CHAR) | Descrizione dell’oggetto del procedimento |
| ISP_DESCRIZIONE_OGGETTO_PROC | VARCHAR2 (200 CHAR) | Descrizione dell’oggetto del procedimento per l’ispezione |



# ISP_POSIZIONE_GIURIDICA
tabella utilizzata per le statistiche relative alle posizioni giuridiche di un provvedimento. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_POSIZIONE_GIURIDICA | VARCHAR2 (2 CHAR) NOT NULL | Codice della posizione giuridica |
| ISP_DESCR_POSIZIONE_GIURIDICA | VARCHAR2 (100 CHAR). | Descrizione della posizione giuridica per l’ispezione |


# ISP_STAT_RIS_SIES
tabella utilizzata per le statistiche relative ad un fascicolo siep. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| CHIAVE_ANNO | NUMBER NOT NULL | Anno del fascicolo |
| CHIAVE_PROGR | NUMBER NOT NULL | Numero del fascicolo |
| COD_UFFICIO | VARCHAR2 (11 CHAR) NOT NULL | Ufficio che ha iscritto il fascicolo |
| DATA_ESTRAZIONE | DATE NOT NULL | Data dell’estrazione |
| COD_POSIZIONE_GIURIDICA | VARCHAR2 (2 CHAR) | Codice della posizione giuridica |
| COD_STATO_PROCEDIMENTO | VARCHAR2 (4 CHAR) | Codice dello stato del procedimento |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Data di inserimento del record |
| DATA_INSERIMENTO. | DATE | Ufficio dell’operatore che ha inserito il record |

# ISP_TEMPI_RICEZIONE_MS
tabella utilizzata per le statistiche relative ai tempi di ricezione dei provvedimenti di misure di sicurezza. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP di riferimento. |
| CHIAVE_ANNO | NUMBER(4) | Anno del fascicolo SIEP di riferimento. |
| CHIAVE_PROGR | NUMBER | Progressivo del fascicolo SIEP di riferimento. |
| COD_UFFICIO | VARCHAR2(11 CHAR) | Ufficio interessato dalla statistica. |
| DATA_ARRIVO_ATTO | DATE | Data dell’arrivo dell’atto. |
| DATA_IRREVOCABILITA | DATE | Data di irrevocabilità del fascicolo. |
| TEMPO_GIUDICATO_RICEZIONE | NUMBER | Tempo di passaggio in giudicato di ricezione del fascicolo. |
| DESC_TIPO_AUTORITA_EMITTENTE | VARCHAR2(200 CHAR) | Descrizione dell’autorità emittente del fascicolo. Associato al Dominio TIPO_AUTORITA di CG_REF_CODES. |
| DESC_LUOGO_EMITTENTE | VARCHAR2(200 CHAR) | Descrizione del luogo di appartenenza dell’autorità emittente del fascicolo. |
| DESC_SEZIONE_AUTORITA | VARCHAR2(50 CHAR) | Descrizione della sezione dell’autorità emittente del fascicolo. |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record. |
| CHIAVE_PROGR_ORIG | NUMBER(38) | Progressivo del fascicolo SIEP originario. |
| DESC_UFFICIO_INSERIMENTO | VARCHAR2(200 CHAR) | Descrizione dell’ufficio dell’operatore che ha inserito il record. |



# ISP_TIPOLOGIA_ATTIVITA
tabella utilizzata per le statistiche relative alle attività di un provvedimento. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_ATTIVITA | VARCHAR2 (2 CHAR) NOT NULL | Codice dell’attività |
| DESCRIZIONE_ATTIVITA | VARCHAR2 (200 CHAR) | Descrizione dell’attività |
| TIPOLOGIA | VARCHAR2 (10 CHAR). | Tipologia dell’attività |




# ISP_TIPOLOGIA_ATTIVITA_MS
tabella utilizzata per le statistiche relative alla tipologia di attività di un provvedimento di misure di sicurezza. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_ATTIVITA | VARCHAR2 (2 CHAR) NOT NULL | Codice dell’attività. |
| DESCRIZIONE_ATTIVITA | VARCHAR2 (200 CHAR) | Descrizione dell’attività. |
| TIPOLOGIA | VARCHAR2 (10 CHAR). | Tipologia dell’attività. |


# ISTANZA
tabella contenente i dati relativi all’istanza. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ISTANZA | NUMBER(38) NOT NULL | Chiave univoca di identificazione degli istituti |
| COD_MOTIVO | VARCHAR2(4 CHAR) | Codice del motivo |
| NOTE | VARCHAR2(2000 CHAR) | Note |
| COGNOME_SOGGETTO_PRESENTANTE | VARCHAR2(100 CHAR) | Cognome del soggetto rappresentante |
| NOME_SOGGETTO_PRESENTANTE | VARCHAR2(100 CHAR) | Nome del soggetto rappresentante |
| DATA_PRESENTAZIONE | DATE NOT NULL | Data di presentazione |
| COD_ESITO | VARCHAR2(4 CHAR) | Codice dell’esito |
| ANNO_REGISTRO | NUMBER(4) | Anno del registro |
| PROGR_REGISTRO | NUMBER(9) | Progressivo del registro |
| COD_TIPO_UFFICIO_DESTINATARIO | VARCHAR2(6 CHAR) | Tipologia dell’ufficio destinatario |
| COD_LUOGO_DESTINATARIO | VARCHAR2(6 CHAR) | Luogo dell’ufficio destinatario |
| COD_UFFICIO_DESTINATARIO | VARCHAR2(11 CHAR) | Codice dell’ufficio destinatario |
| COGNOME_AVVOCATO | VARCHAR2(100 CHAR) | Cognome avvocato |
| NOME_AVVOCATO | VARCHAR2(100 CHAR) | Nome avvocato |
| FORO_COMPETENZA | VARCHAR2(50 CHAR) | Foro di competenza |
| ANNO_SENTENZA | NUMBER(4) | Anno della sentenza |
| NUMERO_SENTENZA | VARCHAR2(6 CHAR) | Numero della sentenza |
| DATA_SENTENZA | DATE | Data della sentenza |
| DATA_IRREVOCABILITA | DATE | Data di irrevocabilità |
| COD_TIPO_AUTORITA_EMITTENTE | VARCHAR2(6 CHAR) | Tipo autorità emittente |
| COD_LUOGO_EMITTENTE | VARCHAR2(6 CHAR) | Luogo dell’autorità emittente |
| COD_STATO_ISTANZA | VARCHAR2(1 CHAR) | Stato dell’istanza |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| SOG_ID_SOGGETTO | NUMBER(38) NOT NULL | Identificativo del soggetto |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| CAM_ID_CAMPO_NOTE | NUMBER(38) | Campo note |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| CAM_ID_CAMPO_NOTE_FK | CAM_ID_CAMPO_NOTE | (CAMPO_NOTA.ID_CAMPO_NOTA) |
| IST_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| IST_SOG_FK | SOG_ID_SOGGETTO | (SOGGETTO.ID_SOGGETTO) |


# ISTITUTO_DETENZIONE
tabella contenente i dati relativi agli istituti di detenzione. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ISTITUTO_DETENZIONE | VARCHAR2 (4 CHAR) NOT NULL | Chiave univoca di identificazione degli istituti |
| COD_TIPO_ISTITUTO | VARCHAR2 (2 CHAR) | Identifica in dettaglio il tipo di istituto. Deriva da dominio e può assumere diversi valori tra i quali riportiamo ad esempio:  CASA CIRCONDARIALE
CASA DI LAVORO
CASA MANDAMENTALE CASA PENALE |
| COD_COMUNE | VARCHAR2 (6 CHAR) | Codice del comune di appartenenza dell'istituto |
| COD_PROVINCIA | VARCHAR2 (2 CHAR) | Codice della provincia di appartenenza dell'istituto |
| INDIRIZZO | VARCHAR2 (300 CHAR) | Indirizzo dettagliato dell'istituto. Questo campo a parità di tipologia di istituto e di comune di appartenenza è l'unico che permette di distinguerli tra di loro. |
| DESCRIZIONE | VARCHAR2 (300 CHAR) | Campo che dovrebbe contenere il dettaglio descrittivo dell'istituto ma che non è stato fornito da Ministero della Giustizia.
Ad esempio per Roma tale campo dovrebbe contenere:
REGINA COELI REBIBBIA |
| NOTE | VARCHAR2 (2000 CHAR) | Campo per eventuali note aggiuntive |
| COD_DISTRETTO | VARCHAR2 (11 CHAR) | Codice del distretto. |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| PERIODO_ALTRA_MISURA | PER_MISU_ISTITUTO_DET_FK | IST_DET_ID_ISTITUTO_DETENZIONE |
| PERIODO_ALTRA_SANZIONE | PER_SANZ_ISTITUTO_DET_FK | IST_DET_ID_ISTITUTO_DETENZIONE |


# ISTRUTTORIA_CUMULO
tabella contenente i dati relativi all’istruttoria di un cumulo. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ISTRUTTORIA_CUMULO | NUMBER(38) NOT NULL | Chiave primaria della tabella |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER(38) NOT NULL | Identificativo del fascicolo SIEP |
| ANNO_PROTOCOLLO | NUMBER(4) NOT NULL | Protocollo Istruttoria: Anno |
| NUM_PROTOCOLLO | NUMBER(9) NOT NULL | Protocollo Istruttoria: Numero |
| CHIAVE_UFFICIO | VARCHAR2(11 CHAR) | Protocollo Istruttoria: Codice Ufficio |
| DATA_APERTURA | DATE | Data apertura Istruttoria |
| DATA_CHIUSURA | DATE | Data chiusura Istruttoria |
| FLAG_STATO | VARCHAR2(1 CHAR) NOT NULL | A = Aperta C = Chiusa N = annullata |
| NOTE | VARCHAR2(2000 CHAR) | Motivo chiusura forzata (annullamento) |
| EVE_ID_EVENTO_ISTR | NUMBER(38) | Id Evento istruttoria (se previsto) |
| EVE_ID_EVENTO_PROV | NUMBER(38) | Id Del Provvedimento di cumulo che chiude l''istruttoria |
| ORDINAMENTO_TITOLI | VARCHAR2(13 CHAR) | Ordinamento titoli coinvolti: x data irrevocabilità o data provvedimento ASC/DESC |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |



# JMS_CODE
tabella contenente i dati relativi alle code jms. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| DOMINIO | VARCHAR2 (24 CHAR) NOT NULL | Dominio logico della tabella |
| CODICE | VARCHAR2 (24 CHAR) NOT NULL | Codice identificativo all’interno del dominio |
| DESCRIZIONE | VARCHAR2 (240 CHAR) NOT NULL | Descrizione relativa la codice |



# LIB_ANTICIPATA_CUMULO
tabella contenente di dati relativi Liberazione Anticipata del Procedimento Cumulato. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_LIBANTICIPATA_CUMULO | NUMBER(38) | Sequence |
| COD_TIPO_LICENZA | VARCHAR2(1) | CG_REF_CODES.RV_DOMAIN= ‘TIPO_LICENZA’ |
| NUMERO_GIORNI | NUMBER(4) | Numero giorni di L.A. |
| SOMMA_RISARC_DANNI | NUMBER(9,2) | Somma di risarcimento danni concessa |
| FLAG_CONCESSO | VARCHAR2(1) | C=Concessi, S=Scomputati |
| TIPO_LA | VARCHAR2(3) | LA (ordinaria), LI (integrazione), LS (speciale), LAU, LIU, LSU. Indica il tipo di LA |
| FLAG_ELABORATO | VARCHAR2(1) | ‘S’ se elaborato |
| FLAG_STATO | VARCHAR2(1) | E=estratto, M=modificato, C=Cancellato, I=Iscritto |
| MOTIVO_MODIFICA | VARCHAR2(2000) | Note inserite dall''operatore in fase di Modifica, Cancellazione, Iscrizione |
| STAT_ID_STATO_ESEC_TIT_CUM | NUMBER(38) | FK alla tabella STATO_ESEC_TITOLO_CUMULATO |
| TIT_ID_TITOLO_CUMULATO | NUMBER(38) | FK alla tabella TITOLO_CUMULATO |
| ID_LIBANTICIPATA_ORIGINE | NUMBER(38) | Eventuale ID del record LIBERAZIONE_ANTICIPATA da cui è stato derivato questo record |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |

# LICENZA_LIBANTICIPATA
tabella contenente di dati relativi alle licenze per liberazione anticipata. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_LICENZA_LIBANTICIPATA | NUMBER NOT NULL | Chiave naturale della tabella. Legata a Sequence LIC_LIB_SEQ. |
| COD_TIPO_LICENZA | VARCHAR2 (2 CHAR) | Codifica del Tipo Licenza (Liberazione Anticipata Permesso Premio
...). Associato al dominio TIPO_LICENZA di CG_REF_CODES. |
| NUMERO_GIORNI | NUMBER | Numero gg. di licenza. |
| DATA_INIZIO | DATE | Data inizio licenza. |
| ORA_INIZIO | VARCHAR2 (5 CHAR) | Ora inizio licenza. |
| DATA_FINE | DATE | Data fine licenza. |
| ORA_FINE | VARCHAR2 (5 CHAR) | Ora di fine Licenza. |
| LUOGO_SVOLGIMENTO_PROVA | VARCHAR2 (2000 CHAR) | Luogo di svolgimento della prova. |
| DATA_DETENZ_RIF_DA | DATE | Data di inizio detenzione. |
| DATA_DETENZ_RIF_A | DATE | Data di fine detenzione. |
| FLAG_INFRAZIONE_OBBLIGHI | VARCHAR2 (1 CHAR) | Codifica di avvenuta infrazione obblighi. Associata al Dominio FLAG_SI_NO. |
| DATA_INFRAZIONE_OBBLIGHI | DATE | Eventuale data di Infrazione obblighi. |
| DESCR_INFRAZIONE_OBBLIGHI | VARCHAR2 (2000 CHAR) | Campo descrittivo per l'infrazione obblighi. |
| FLAG_SCOMPUTO | VARCHAR2 (1 CHAR) | Flag che indica se il periodo va o meno scomputato dalla pena. Associato al Dominio FLAG_SI_NO di CG_REF_CODES. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER | Identificativo del fascicolo SIUS |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo  del fascicolo SIEP |
| FLAG_CONCESSO | VARCHAR2 (1 CHAR) | Campo che Indica se è stata o meno concessa la licenza. Associata al Dominio FLAG_CONCESSO. |
| FLAG_ELABORATO | VARCHAR2 (1 CHAR) | Campo che Indica se è stata o meno elaborata la licenza. Associata al Dominio FLAG_SI_NO. |
| FLAG_SCORTA | VARCHAR2 (1 CHAR) | Campo che Indica se è stata o meno concessa la scorta. Associata al Dominio FLAG_SI_NO. |
| COD_STATO_PERMESSO | VARCHAR2 (2 CHAR) | Codifica dello stato del permesso (Affidato Ad un Familiare Libero
...). Associato al dominio STATO_PERMESSO di CG_REF_CODES. |
| DESCR_STATO_PERMESSO | VARCHAR2 (50 CHAR) | Descrizione supplementare dello stato permesso. |
| NUMERO_ORE | NUMBER | Numero Ore del permesso. |
| ANNO_SIUS | NUMBER | Anno SIUS. |
| NUMERO_SIUS | VARCHAR2 (6 CHAR) | Numero SIUS. |
| ANNO_ORDINANZA | NUMBER | Anno dell'Ordinanza. |
| NUMERO_ORDINANZA | NUMBER | Numero dell'Ordinanza. |
| COD_UFFICIO_EMITTENTE | VARCHAR2 (11 CHAR) | Codice dell’ufficio che ha emesso la liberazione anticipata |
| COD_LUOGO_EMITTENTE | VARCHAR2 (6 CHAR) | Sede dell’ufficio che ha emesso la liberazione anticipata |
| DATA_EMISSIONE_ORDINANZA | DATE | Data di emissione ordinanza |
| GIORNI_SCOMPUTATI | VARCHAR2 (3 CHAR) | Numero di giorni scomputati |
| COD_ESITO | VARCHAR2 (2 CHAR) | Codice dell’esito |
| DATA_ANNOTAZIONE_ESITO | DATE | Data annotazione esito |
| ANNOTAZIONE | VARCHAR2 (2000 CHAR) | Annotazione |
| NUMERO_GIORNI_NO_FRUITI | NUMBER | Numero di giorni non fruiti |
| NUMERO_ORE_NO_FRUITE. | NUMBER | Numero di ore non fruite |
| NUMERO_MESI | NUMBER(3) | Numero di mesi non fruiti |
| SOMMA_RISARC_DANNI | NUMBER | Somma relativa al risarcimento danni |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| LIC_LIB_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| LIC_LIB_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |
| LIC_LIB_FAS_SIU_FK | FAS_SIU_ID_FASCICOLO_SIUS | (FASCICOLO_SIUS.ID_FASCICOLO_SIUS) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| PERIODO_LIBANTICIPATA | PER_LIBAN_ID_LIC_LIBAN_FK | LIC_ID_LICENZA_LIBANTICIPATA |


# LOG_ATTIVITA
tabella contenente di dati relativi alle attività di un utente utilizzatore di sies. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| RECORD | VARCHAR2 (4000 CHAR) | Dati della tabella prima della modifica o della cancellazione. Dati della tabella nuovi in caso di inserimento |
| COD_OPERATORE | VARCHAR2 (100 CHAR) | Utente che ha effettuato l’operazione |
| DATA | DATE | Data/ora dell'operazione |
| IP_UTENTE | VARCHAR2 (15 CHAR) | Indirizzo ip del computer dell’ utente che ha effettuato l’operazione |
| AZIONE_CONTESTO_JAVA | VARCHAR2 (100 CHAR). | Action del modulo java |


# LOG_TRASFERIMENTO_ESECUZIONE
tabella contenente i log  relativi ai fogli complementari trasferiti da sies verso nsc. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ESITO | VARCHAR2(300 CHAR) | Esito del trasferimento dell’invio del foglio complementare dal sistema SIES verso NSC |
| CHIAVE_SIES | NUMBER(38) | Identificativo del foglio complementare SIES inviato |
| CHIAVE_NSC | NUMBER(38) | Identificativo del foglio complementare NSC iscritto |
| ESTRATTO | BLOB | Estratto del provvedimento iscritto |
| ID | NUMBER(38) NOT NULL | Identificativo della tabella |
| DATA_OPERAZIONE | DATE | Data in cui è effettuato l’invio |
| OPERAZIONE | VARCHAR2(40 CHAR) | Descrizione dell’operazione effettuata INSERT, UPDATE,DELETE |
| COMPLETATO | VARCHAR2(1 CHAR) | S/N |


# LUOGO_DETENZIONE
tabella contenente di dati relativi al luogo di detenzione. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_LUOGO_DETENZIONE | NUMBER NOT NULL | Chiave numerica univoca dell'entità |
| NOTE | VARCHAR2 (2000 CHAR) | Eventuali note aggiuntive |
| DATA_INIZIO_DETENZIONE | DATE | Data da cui decorre la Detenzione |
| DATA_FINE_DETENZIONE | DATE | Data di fine detenzione. Il valore in questo campo non coincide necessariamente con la data di scadenza della pena ma indica fino a quale data il soggetto è stato presso un determinato istituto di detenzione. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER | Identificativo del fascicolo SIUS |
| POS_GIU_ID_POSIZIONE_GIURIDICA | NUMBER | Identificativo della posizione giuridica |
| ALTRO_LUOGO | VARCHAR2 (2000 CHAR) | Campo descrittivo indicante un altro luogo di detenzione diverso dall'istituto contenuto nella tabella "ISTITUTO_DETENZIONE". Spesso ad esempio è usato per indicare il luogo della detenzione domiciliare. |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2 (4 CHAR). | Identificativo dell’istituto  di detenzione |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| FAS_SIGE_DETENZIONE | FAS_SIGE_DET_LUOGO_FK | LD_ID_LUOGO_DETENZIONE |



# MAGISTRATO
tabella contenente di dati relativi ai magistrati. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_MAGISTRATO | VARCHAR2 (6 CHAR) NOT NULL | Codice del Magistrato. |
| COGNOME | VARCHAR2 (50 CHAR) NOT NULL | Cognome del Magistrato. |
| NOME | VARCHAR2 (50 CHAR) NOT NULL | Nome del Magistrato. |
| FLAG_STATO | VARCHAR2 (1 CHAR) | Codifica dello stato operativo del Magistrato (Presente Trasferito ...). Associato al dominio FLAG_STATO di CG_REF_CODES. |
| COD_UFFICIO_APPARTENENZA | VARCHAR2 (11 CHAR) NOT NULL | Codice dell' Ufficio a cui appartiene il magistrato. |
| DATA_INIZIO_VALIDITA | DATE NOT NULL | Data di inizio validità di stato del Magistrato. |
| DATA_FINE_VALIDITA | DATE | Data di fine validità di stato del Magistrato. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| E_MAIL_UFFICIO | VARCHAR2 (300 CHAR) | e-mail dell'ufficio. |
| E_MAIL_PRIVATA | VARCHAR2 (300 CHAR) | e-mail Privata. |
| NUM_CELLULARE | VARCHAR2 (15 CHAR). | Numero Cellulare. |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| COLLEGIO_MAGISTRATO | COL_MAG_MAGISTRATO_FK | COD_UFFICIO_INSERIMENTO |
| COLLEGIO_MAGISTRATO | COL_MAG_MAGISTRATO_FK | MAG_COD_MAGISTRATO |


# MAGISTRATO_ASSEGNATARIO
tabella contenente di dati relativi ai magistrati assegnati ad un fascicolo sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| DATA_INIZIO | DATE NOT NULL | data di inizio del periodo di assegnazione del magistrato |
| DATA_FINE | DATE | data di fine assegnazione del magistrato |
| COD_RUOLO_MAGISTRATO | VARCHAR2 (2 CHAR) | ruolo del magistrato codificato in CG_REF_CODES |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | codice nazionale univoco identificatore del magistrato |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| MAG_COD_MAGISTRATO | VARCHAR2 (6 CHAR) NOT NULL | Identificativo del magistrato assegnato al fascicolo SIGE |
| FAS_SIGE_ID_FASCICOLO_SIGE | NUMBER NOT NULL. | ID Fascicolo SIGE assegnato al magistrato nel periodo |
| COD_PROCURATORE | VARCHAR2 (6 CHAR) | Codice del Procuratore |
| COD_ID_ASSISTENTE | NUMBER | Codice Assistente |
| FLAG_MODIF_IN_BLOCCO | VARCHAR2(1) | Flag che identifica se il magistrato è stato interessato dalla modifica in blocco per il RUOLO |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| MAG_ASS_FAS_SIE_FK | FAS_SIGE_ID_FASCICOLO_SIGE | (FASCICOLO_SIGE.ID_FASCICOLO_SIGE) |
| MAG_ASS_MAG_FK | MAG_COD_MAGISTRATO | (W_MAGISTRATO.COD_MAGISTRATO) |





# MAGISTRATO_COMPETENTE
tabella contenente di dati relativi al magistrato competente per fascicolo siep. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| DATA_INIZIO | DATE NOT NULL | Data di inizio competenza sul fascicolo. |
| DATA_FINE | DATE | Data fine competenza sul fascicolo. |
| COD_RUOLO_MAGISTRATO | VARCHAR2 (2 CHAR) | Codifica Ruolo del Magistrato (P.M. di Esecuzione Magistrato di Sorveglianza ...). Associato al dominio RUOLO_MAGISTRATO di CG_REF_CODES. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| MAG_COD_MAGISTRATO | VARCHAR2 (6 CHAR) NOT NULL | Identificativo del magistrato assegnato al fascicolo SIEP |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL. | ID Fascicolo SIEP assegnato al magistrato nel periodo |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| MAG_COM_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |
| MAG_COM_MAG_FK | MAG_COD_MAGISTRATO | (W_MAGISTRATO.COD_MAGISTRATO) |




# MAGISTRATO_RELATORE
tabella contenente di dati relativi al magistrato relatore per un fascicolo sius. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| DATA_INIZIO | DATE NOT NULL | Data di inizio competenza sul fascicolo. |
| DATA_FINE | DATE | Data fine competenza sul fascicolo. |
| COD_RUOLO_MAGISTRATO | VARCHAR2 (2 CHAR) | Codifica Ruolo del Magistrato (P.M. di Esecuzione Magistrato di Sorveglianza ...). Associato al dominio RUOLO_MAGISTRATO di CG_REF_CODES. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| MAG_COD_MAGISTRATO | VARCHAR2 (6 CHAR) | Identificativo del magistrato assegnato al fascicolo SIUS |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER NOT NULL | ID Fascicolo SIUS assegnato al magistrato nel periodo |
| ESP_ID_ESPERTO | NUMBER | Identificativo dell’esperto |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| MAG_REL_ESP_FK | ESP_ID_ESPERTO | (ESPERTO.ID_ESPERTO) |
| MAG_REL_FAS_SIU_FK | FAS_SIU_ID_FASCICOLO_SIUS | (FASCICOLO_SIUS.ID_FASCICOLO_SIUS) |
| MAG_REL_MAG_FK | MAG_COD_MAGISTRATO | (W_MAGISTRATO.COD_MAGISTRATO) |




# MAGISTRATO_SEZIONE
tabella contenente di dati relativi alle sezioni associate ad un magistrato. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| MAG_COD_MAGISTRATO | VARCHAR2 (6 CHAR) NOT NULL | Codice Magistrato Referenza |
| COD_UFFICIO_APPARTENENZA | VARCHAR2 (11 CHAR) | Codice Ufficio di Appartenenza |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice Operatore Inserimento |
| DATA_INSERIMENTO | DATE | Data Inserimento |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Codice Ufficio Inserimento |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice Operatore Aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data Aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Codice Ufficio Aggiornamento |
| SEZ_ID_SEZIONE | NUMBER | Id Sezione Referenza |
| DATA_INIZIO_ASS | DATE | Indica la data di inizio assegnazione sezione |
| DATA_FINE_ASS | DATE | Indica la data di fine assegnazione sezione |
| FLG_VALIDO_SN | VARCHA2 (1 CHAR) | Se impostato a S indica ULTIMA SEZIONE INSERITA ALTRIMENTI N |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| MAG_SEZ_MAG_FK | MAG_COD_MAGISTRATO | (W_MAGISTRATO.COD_MAGISTRATO) |
| MAG_SEZ_SEZ_FK | SEZ_ID_SEZIONE | (SEZIONE.ID_SEZIONE) |


# MAX_STATO_PROCEDIMENTO
tabella contenente di dati relativi allo stato del fascicolo siep. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| STA_PRO_PROGRESSIVO | NUMBER NOT NULL | Codifica dello Stato Fascicolo (Iscritto Trasmesso per Competenza...). Associato al Dominio STATO_FASCICOLO di CG_REF_CODES |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL | Identificativo del fascicolo SIEP a cui afferisce lo stato in questione. |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| MAX_STA_PRO_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


# MESSAGGIO
tabella contenente di dati relativi all’invio di una richiesta nel colloquio tra banche dati interdistrettuali. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_MESSAGGIO | NUMBER NOT NULL | Chiave primaria della tabella |
| COD_UFFICIO_MITTENTE | VARCHAR2 (11 CHAR) DEFAULT '-' | Codice dell’ufficio mittente |
| COD_BDI_MITTENTE | VARCHAR2 (11 CHAR) DEFAULT '-' | Codice della banca dati del distretto mittente |
| COD_UFFICIO_DESTINATARIO | VARCHAR2 (11 CHAR) DEFAULT '-' | Codice dell’ufficio destinatario |
| COD_BDI_DESTINATARIA | VARCHAR2 (11 CHAR) DEFAULT '-' | Codice della banca dati del distretto destinatario |
| DATA_INVIO | DATE | Data di invio del messaggio |
| DATA_ESITO | DATE | Data dell’esito dell’invio |
| CODICE_UTENTE_MITTENTE | VARCHAR2 (11 CHAR) | Codice dell’utente mittente |
| COD_ESITO | VARCHAR2 (35 CHAR) | Codice dell’esito dell’invio |
| BLOB_ESITO | BLOB | Campo contenente l’esito |
| JMS_ID_MESSAGE | VARCHAR2 (128 CHAR) | Identificativo del messaggio della coda jms |
| JMS_CORRELATION_ID_MESSAGE | VARCHAR2 (128 CHAR) | Identificativo del messaggio di correlazione |
| FLAG_VISTO | VARCHAR2 (1 CHAR) | Flag visionato S/N |
| COD_TIPO_MESSAGGIO | VARCHAR2 (2 CHAR) | Codice del tipo di messaggio |
| COD_TIPO_OPERAZIONE | VARCHAR2 (5 CHAR) | Codice del tipo di operazione |
| CHIAVE_ANNO_SIEP | NUMBER | Anno del fascicolo SIEP inviato |
| CHIAVE_PROGR_SIEP | NUMBER | Progressivo del fascicolo SIEP inviato |
| CHIAVE_ANNO_SIUS | NUMBER | Anno del fascicolo SIUS inviato |
| CHIAVE_PROGR_SIUS | NUMBER | Progressivo del fascicolo SIUS inviato |
| CHIAVE_ANNO_SIEPE | NUMBER | Anno del fascicolo SIEPE inviato |
| CHIAVE_PROGR_SIEPE | NUMBER | Progressivo del fascicolo SIEPE inviato |
| COGNOME_SOGGETTO | VARCHAR2 (35 CHAR) | Cognome del soggetto inviato |
| NOME_SOGGETTO | VARCHAR2 (35 CHAR) | Nome del soggetto inviato |
| DATA_NASCITA | DATE | Data di nascita del soggetto inviato |
| COD_STATO_NASCITA | VARCHAR2 (3 CHAR) | Codice dello stato di nascita del soggetto inviato |
| COD_COMUNE_NASCITA | VARCHAR2 (6 CHAR) | Codice del comune di nascita del soggetto inviato |
| CHIAVE_PROGR_FAS_CUMULANTE | NUMBER | Progressivo del fascicolo cumulante |
| CHIAVE_ANNO_FAS_CUMULANTE | NUMBER | Anno del fascicolo cumulante |
| NOTE | VARCHAR2 (2000 CHAR). | Note |
| CHIAVE_UFFICIO_SIEP | VARCHAR2(11 CHAR) | UFFICIO SIEP titolare degli atti inoltrati |
| DELIVERY_MODE | VARCHAR2(5 CHAR) | Codice BDI a cui inviare la risposta nel caso di Inoltro ricevuto |
| COD_UFFICIO_INOLTRO | VARCHAR2(11 CHAR) | Codice UFFICIO a cui e stato inoltrato il messaggio |
| COD_BDI_INOLTRO | VARCHAR2(11 CHAR) | Codice BDI a cui e stato inoltrato il messaggio |
| COD_UFFICIO_REPLY_TO | VARCHAR2(11 CHAR) | Codice Ufficio a cui inviare la risposta nel caso di Inoltro ricevuto |
| COD_BDI_REPLY_TO | VARCHAR2(11 CHAR) | Codice BDI a cui inviare la risposta nel caso di Inoltro ricevuto |
| JMS_CORRELATION_REPLY_TO | VARCHAR2(128 CHAR) | ID del messaggio di INOLTRO inviato sulla BDI di invio |
| ID_MESSAGGIO_SOLLECITATO | VARCHAR2(128 CHAR) | ID del messaggio di Richiesta Sollecitato |
| CHIAVE_UFFICIO_FAS_CUMULANTE | VARCHAR2(11 CHAR) | Chiave Ufficio del fascicolo cumulante |
| ID_RICHIESTA | NUMBER(38) | ID del messaggio di Richiesta Atti per emissione trasferimento competenza |



# MISURA_ALTERNATIVA
tabella contenente i dati relativi alla misura alternativa. utilizzata dal sottosistema sius.

| Field | Datatype | Datatype | Descrizione |
| --- | --- | --- | --- |
| ID_MISURA_ALTERNATIVA | NUMBER NOT NULL | Valore di chiave primaria numerica legata alla sequence MIS_ALT_SEQ | Valore di chiave primaria numerica legata alla sequence MIS_ALT_SEQ |
| COD_TIPO_DECISIONE | VARCHAR2 (2 CHAR) | Deriva da dominio TIPO_DECISIONE_SORVEGLIANZA e assume i seguenti valori: D Decreto O Ordinanza | Deriva da dominio TIPO_DECISIONE_SORVEGLIANZA e assume i seguenti valori: D Decreto O Ordinanza |
| COD_NATURA_DECISIONE | VARCHAR2 (2 CHAR) | In funzione del COD_TIPO_MISURA assume i seguenti valori: CO concessione RE revoca SO sospensione provvisoria RI ripristino IN interruzione ecc. Tali valori sono prelevati dal campo RV_HIGH_VALUE della CG_REF_CODES con RV_DOMAIN=ESITO_PROVVEDIMEN TO e RV_LOW_VALUE
= RV_ABBREVIATION della CG_REF_CODES del RV_DOMAIN=ESITO_TENORE. Sembra un ragionamento contorto
ma permette di ottenere univocamente la Misura Alternativa trattata. | In funzione del COD_TIPO_MISURA assume i seguenti valori: CO concessione RE revoca SO sospensione provvisoria RI ripristino IN interruzione ecc. Tali valori sono prelevati dal campo RV_HIGH_VALUE della CG_REF_CODES con RV_DOMAIN=ESITO_PROVVEDIMEN TO e RV_LOW_VALUE
= RV_ABBREVIATION della CG_REF_CODES del RV_DOMAIN=ESITO_TENORE. Sembra un ragionamento contorto
ma permette di ottenere univocamente la Misura Alternativa trattata. |
| COD_TIPO_MISURA | VARCHAR2 (4 CHAR) | Valore derivabile da dominio e coincide con il MOTIVO_PROVEDIMENTO che generalmente è trattato da SIUS potendo così utilizzare tutti i valori possibili di una misura alternativa. | Valore derivabile da dominio e coincide con il MOTIVO_PROVEDIMENTO che generalmente è trattato da SIUS potendo così utilizzare tutti i valori possibili di una misura alternativa. |
| DATA_DECISIONE | DATE | Data dell'ordinanza o del decreto riferito alla misura alternativa | Data dell'ordinanza o del decreto riferito alla misura alternativa |
| COD_MAGISTRATO | VARCHAR2 (6 CHAR) | Codice magistrato dell'evento | Codice magistrato dell'evento |
| COD_UFFICIO_SORVEGLIANZA | VARCHAR2 (11 CHAR) DEFAULT '-' | Codice ufficio che ha emesso il decreto o l'ordinanza | Codice ufficio che ha emesso il decreto o l'ordinanza |
| CSS_ID_CSSA | NUMBER | Codice ID del CSSA Competente | Codice ID del CSSA Competente |
| DESCR_LUOGO_PROVA | VARCHAR2 (2000 CHAR) | Campo a testo libero del luogo in cui si svolgerà la misura alternativa concessa | Campo a testo libero del luogo in cui si svolgerà la misura alternativa concessa |
| NUM_ANNI_MISURA | NUMBER | Numero di anni riferiti alla misura alternativa. Sono necessari per ilo calcolo della pena residua | Numero di anni riferiti alla misura alternativa. Sono necessari per ilo calcolo della pena residua |
| NUM_MESI_MISURA | NUMBER | Numero di mesi riferiti alla misura alternativa. Sono necessari per ilo calcolo della pena residua | Numero di mesi riferiti alla misura alternativa. Sono necessari per ilo calcolo della pena residua |
| NUM_GIORNI_MISURA | NUMBER | Numero di giorni riferiti alla misura alternativa. Sono necessari per ilo calcolo della pena residua | Numero di giorni riferiti alla misura alternativa. Sono necessari per ilo calcolo della pena residua |
| DATA_INIZIO_MISURA | DATE | Data di inizio della misura alternativa. E' necessario per il calcolo della pena | Data di inizio della misura alternativa. E' necessario per il calcolo della pena |
| DATA_FINE_MISURA | DATE |  |  |
| CHIAVE_ANNO_FASCICOLO_SIUS | NUMBER | Campo di composizione del codice fascicolo SIUS. Si è preferito usare il codice composito del fascicolo SIUS (anno ufficio progressivo) al posto dell'ID perché nelle stampe è possibile fare così riferimento al fascicolo SIUS competente. | Campo di composizione del codice fascicolo SIUS. Si è preferito usare il codice composito del fascicolo SIUS (anno ufficio progressivo) al posto dell'ID perché nelle stampe è possibile fare così riferimento al fascicolo SIUS competente. |
| CHIAVE_UFFICIO_FASCICOLO_SIUS | VARCHAR2 (11 CHAR) | Campo di composizione del codice fascicolo SIUS. | Campo di composizione del codice fascicolo SIUS. |
| CHIAVE_PROGR_FASCICOLO_SIUS | NUMBER | Campo di composizione del codice fascicolo SIUS. | Campo di composizione del codice fascicolo SIUS. |
| ANNO_REGISTRO | NUMBER | Anno del registro | Anno del registro |
| NUMERO_REGISTRO | NUMBER | Numero del registro | Numero del registro |
| NOTE | VARCHAR2 (2000 CHAR) | Note | Note |
| DATA_SCARCERAZIONE | DATE | Data della scarcerazione | Data della scarcerazione |
| DATA_INGRESSO_ISTITUTO | DATE | Data di ingresso nell’istituto | Data di ingresso nell’istituto |
| COD_TIPO_UFFICIO_SCARCERAZIONE | VARCHAR2 (4 CHAR) | Tipo di ufficio che effettua la scarcerazione | Tipo di ufficio che effettua la scarcerazione |
| FLAG_UFFICIO_INSERIMENTO | VARCHAR2 (1 CHAR) | Flag utilizzato per discriminare se l'ordinanza emessa e la conseguente
M.A. sono state inserite da SIUS o inserite a mano da SIEP. Solo in questo caso vale 'P'. La differenza non visibile in maschera permette
di avere i campi relativi ai radio button abilitati o meno. | Flag utilizzato per discriminare se l'ordinanza emessa e la conseguente
M.A. sono state inserite da SIUS o inserite a mano da SIEP. Solo in questo caso vale 'P'. La differenza non visibile in maschera permette
di avere i campi relativi ai radio button abilitati o meno. |
| DATA_INIZIO_REVOCA | DATE | Data inizio revoca | Data inizio revoca |
| NUM_ANNI_REVOCA_RECLUSIONE | NUMBER | Anni revoca della reclusione | Anni revoca della reclusione |
| NUM_MESI_REVOCA_RECLUSIONE | NUMBER | Mesi revoca della reclusione | Mesi revoca della reclusione |
| NUM_GIORNI_REVOCA_RECLUSIONE | NUMBER | Giorni revoca della reclusione | Giorni revoca della reclusione |
| NUM_ANNI_REVOCA_ARRESTO | NUMBER | Anni revoca della arresto | Anni revoca della arresto |
| NUM_MESI_REVOCA_ARRESTO | NUMBER | Mesi revoca della arresto | Mesi revoca della arresto |
| NUM_GIORNI_REVOCA_ARRESTO | NUMBER | Giorni revoca della arresto | Giorni revoca della arresto |
| ANNO_ALTRO_TITOLO | NUMBER | Anno altro titolo esecutivo | Anno altro titolo esecutivo |
| NUM_ALTRO_TITOLO | VARCHAR2 (6 CHAR) | Numero di altro titolo esecutivo | Numero di altro titolo esecutivo |
| DATA_ALTRO_TITOLO | DATE | Data altro titolo esecutivo | Data altro titolo esecutivo |
| COD_LUOGO_ALTRO_TITOLO | VARCHAR2 (6 CHAR) DEFAULT '-' | Codice del luogo di altro titolo esecutivo | Codice del luogo di altro titolo esecutivo |
| COD_AUTORITA_ALTRO_TITOLO | VARCHAR2 (6 CHAR) DEFAULT '-' | Codice autorità di altro titolo esecutivo | Codice autorità di altro titolo esecutivo |
| FLAG_PERIODO_ESPIATO | VARCHAR2 (2 CHAR) | Periodo Espiato S/N | Periodo Espiato S/N |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP | Identificativo del fascicolo SIEP |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento | Identificativo dell’evento |
| DATA_SCADENZA_PROROGA | DATE | Data di scadenza della proroga | Data di scadenza della proroga |
| FLAG_DECISIONE_TRIBUNALE | VARCHAR2 (1 CHAR) | S/N flag decisione del tribunale | S/N flag decisione del tribunale |
| COD_TDS_COMPETENTE | VARCHAR2 (11 CHAR) DEFAULT '-' | Codice del TdS competente | Codice del TdS competente |
| FLAG_SITUAZIONE | VARCHAR2 (1 CHAR). | S/N Flag situazione | S/N Flag situazione |
| COD_TIPO_DECISIONE_MA_AT | VARCHAR2(2 CHAR) | Tipo della decisione di Misura Alternativa | Tipo della decisione di Misura Alternativa |
| COD_TIPO_MISURA_MA_AT | VARCHAR2(4 CHAR) | Tipo della misura di Misura Alternativa | Tipo della misura di Misura Alternativa |
| DATA_DECISIONE_MA_AT | DATE | Data della decisione di Misura Alternativa | Data della decisione di Misura Alternativa |
| CHIAVE_ANNO_FAS_SIUS_MA_AT | NUMBER(4) | Anno del fascicolo Misura Alternativa | Anno del fascicolo Misura Alternativa |
| CHIAVE_PROGR_FAS_SIUS_MA_AT | NUMBER | Numero del fascicolo Misura Alternativa | Numero del fascicolo Misura Alternativa |
| CHIAVE_UFF_FAS_SIUS_MA_AT | VARCHAR2(11 CHAR) | Ufficio che ha inserito Misura Alternativa | Ufficio che ha inserito Misura Alternativa |
| ANNO_REGISTRO_MA_AT | NUMBER(4) | Anno del registro di Misura Alternativa | Anno del registro di Misura Alternativa |
| NUMERO_REGISTRO_MA_AT | NUMBER(9) | Numero del registro di Misura Alternativa | Numero del registro di Misura Alternativa |
| FL_FORMA_MISURA | NUMBER(1) | Flag forma della misura | Flag forma della misura |
| DESCRIZIONE_COMUNITA | VARCHAR2(2000) | Descrizione della comunità | Descrizione della comunità |
| DATA_ESECUTIVITA | DATE | Data esecutivita' dell'Ordinanza di Applicazione Provvisoria M.A. | Data esecutivita' dell'Ordinanza di Applicazione Provvisoria M.A. |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| MIS_ALT_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |




# MISURA_CAUTELARE
tabella contenente di dati relativi alle misure cautelari. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_MISURA_CAUTELARE | NUMBER NOT NULL | Campo chiave fornito dal progressivo nell'ambito del fascicolo. |
| COD_TIPO_MISURA | VARCHAR2 (2 CHAR) | Definito da dominio. Assume i seguenti valori: CA Carcere AD Arresti Domiciliari |
| DATA_INIZIO | DATE | Data inizio validità della Misura Cautelare |
| DATA_FINE | DATE | Eventuale data di termine validità della Misura Cautelare |
| NUM_ANNI | NUMBER | Numero di anni della misura cautelare |
| NUM_MESI | NUMBER | Numero di mesi della misura cautelare |
| NUM_GIORNI | NUMBER | Numero di giorni della misura cautelare |
| FLAG_COMPUTABILE | VARCHAR2 (1 CHAR) | Indica se la misura cautelare è computabile o meno per il calcolo della pena. Non computabile è il periodo di fungibilità subita cioè già goduta su altri fascicoli |
| COD_MOTIVO_NON_COMPUTABILE | VARCHAR2 (2 CHAR) | Deriva da dominio e indica il motivo della non computabilità |
| ALTRO_LUOGO_DETENZIONE | VARCHAR2 (1000 CHAR) | Campo utilizzato nel caso in cui il luogo di detenzione non sia codificato |
| COD_TIPO_UFFICIO_RIFER | VARCHAR2 (6 CHAR) | Indica la tipologia dell'ufficio che ha emesso la fungibilità |
| COD_LUOGO_UFFICIO_RIFER | VARCHAR2 (6 CHAR) | Indica il comune dell'ufficio che ha emesso la fungibilità. Insieme al tipo ufficio identifica univocamente un codice ufficio giudiziario |
| DATA_FUNGIBILITA | DATE | Data del provvedimento di fungibilità |
| NUM_RIFER | VARCHAR2 (24 CHAR) | Il codice del fascicolo o del numero RES della fungibilità subita dal proprio fascicolo |
| NOTE | VARCHAR2 (2000 CHAR) | Note |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2 (4 CHAR). | Identificativo dell’istituto di detenzione |
| ANNO_FASC_BDMC | NUMBER(4) | Indica anno del fascicolo bdmc |
| NUME_FASC_BDMC | NUMBER(6) | Indica numero del fascicolo bdmc |
| CODICE_UFFICIO_PM_SEDE | VARCHAR2(11) | Indica ufficio del PM del fascicolo bdmc |
| ANNO_RGNR | NUMBER(4) | Indica anno del registro generale della notizia di reato |
| NUMERO_RGNR | NUMBER(6) | Indica numero del registro generale della notizia di reato |
| ANNO_REG_GEN | NUMBER(4) | Indica anno del registro generale |
| NUMERO_REG_GEN | NUMBER(6) | Indica numero del registro generale |
| TIPO_UFFICIO_REG_GEN | VARCHAR2(6) | Indica Codice tipo ufficio |
| AUTORITA_EMITTENTE | VARCHAR2(11) | Indica codice autorità emittente |
| AUTORITA_EMITTENTE_LUOGO | VARCHAR2(6) | Indica codice del comune autorità emittente |
| AUTORITA_COMPETENTE | VARCHAR2(2) | Indica codice tipo autorità competente |
| AUTORITA_COMPETENTE_SEDE | VARCHAR2(6) | Indica sede dell’autorità competente |
| AUTORITA_COMPETENTE_INDIRIZZO | VARCHAR2(1000) | Indica l’indirizzo dell’autorità competente |
| ANNO_RIFER | NUMBER(4) | Indica anno di riferimento |
| POS_GIU_ID_POSIZIONE_GIURIDICA | NUMBER(38) | Indica il codice della posizione giuridica' |
| GIORNI | NUMBER(6) | Indica giorni di misura cautelare |
| FLAG_MODIFICA_MANUALE | VARCHAR2(12) | Indica modifica manuale s/n |
| DATA_EMISSIONE_ORDINANZA | DATE | Indica la data di Emissione ordinanza' |
| KEY_ESEC_NSC | NUMBER(38) | Chiave di nsc |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| MIS_CAU_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| MIS_CAU_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |




# MISURA_CAUTELARE_BDMC
tabella contenente di dati relativi alle misure cautelari bdmc. utilizzata dal sottosistema siep.

| Field | Datatype | Datatype | Descrizione |
| --- | --- | --- | --- |
| ID_MISURA_CAUTELARE_BDMC | ID_MISURA_CAUTELARE_BDMC | NUMBER NOT NULL | Campo chiave fornito dal progressivo nell'ambito del fascicolo |
| FAS_SIE_ID_FASCICOLO_SIEP | FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL | Identificativo del fascicolo SIEP |
| SOG_ID_SOGGETTO | SOG_ID_SOGGETTO | NUMBER NOT NULL | Identificativo del soggetto |
| EVE_ID_EVENTO | EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| PEN_RES_ID_PENA_RESIDUA | PEN_RES_ID_PENA_RESIDUA | NUMBER | Identificativo della pena residua |
| ID_PREN | ID_PREN | NUMBER | Identificativo della Pren |
| PROG_PERI_PRES | PROG_PERI_PRES | NUMBER | Identificativo della presenza |
| FLAG_CARICAMENTO | FLAG_CARICAMENTO | VARCHAR2 (4 CHAR) NOT NULL | S/N flag caricamento |
| FLAG_STATO | FLAG_STATO | VARCHAR2 (1 CHAR) NOT NULL | Flag dello stato |
| COD_TIPO_MISURA | COD_TIPO_MISURA | VARCHAR2 (2 CHAR) | Codice tipo misura |
| DATA_INIZIO | DATA_INIZIO | DATE | Data inizio misura |
| DATA_FINE | DATA_FINE | DATE | Data fine misura |
| NUM_ANNI | NUM_ANNI | NUMBER | Numero di anni della misura |
| NUM_MESI | NUM_MESI | NUMBER | Numero di mesi della misura |
| NUM_GIORNI | NUM_GIORNI | NUMBER | Numero di giorni della misura |
| IST_DET_ID_ISTITUTO_DETENZIONE | IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2 (4 CHAR) | Identificativo dell’istituto di detenzione |
| ALTRO_LUOGO_DETENZIONE | ALTRO_LUOGO_DETENZIONE | VARCHAR2 (1000 CHAR) | Descrizione altro luogo di detenzione |
| FLAG_COMPUTABILE | FLAG_COMPUTABILE | VARCHAR2 (1 CHAR) | S/N flag computabile |
| COD_MOTIVO_NON_COMPUTABILE | COD_MOTIVO_NON_COMPUTABILE | VARCHAR2 (2 CHAR) | Codice del motivo di non computabilità |
| COD_TIPO_UFFICIO_RIFER | COD_TIPO_UFFICIO_RIFER | VARCHAR2 (6 CHAR) | Tipo ufficio di riferimento |
| COD_LUOGO_UFFICIO_RIFER | COD_LUOGO_UFFICIO_RIFER | VARCHAR2 (6 CHAR) | Luogo dell’ufficio di riferimento |
| DATA_COMPUTO | DATA_COMPUTO | DATE | Data di computo |
| ANNO_FASC_SIEP | ANNO_FASC_SIEP | NUMBER | Anno del fascicolo SIEP |
| NUME_FASC_SIEP | NUME_FASC_SIEP | NUMBER | Numero del fascicolo SIEP |
| NOTE | NOTE | VARCHAR2 (2000 CHAR) | Note |
| ANNO_FASC_BDMC | ANNO_FASC_BDMC | NUMBER | Anno del fascicolo bdmc |
| NUME_FASC_BDMC | NUME_FASC_BDMC | NUMBER | Numero del fascicolo bdmc |
| COD_UFFICIO_BDMC | COD_UFFICIO_BDMC | VARCHAR2 (11 CHAR) | Codice dell’ufficio bdmc |
| ANNO_RGNR | ANNO_RGNR | NUMBER | Indica anno del registro generale della notizia di reato |
| NUME_RGNR | NUME_RGNR | NUMBER | Indica numero del registro generale della notizia di reato |
| COD_UFFICIO_RGNR | COD_UFFICIO_RGNR | VARCHAR2 (11 CHAR) | Indica codice dell’ufficio del registro generale della notizia di reato |
| ANNO_REGE_GIP | ANNO_REGE_GIP | NUMBER | Anno del registro gip |
| NUMERO_REGE_GIP | NUMERO_REGE_GIP | NUMBER | Numero del registro gip |
| COD_UFFICIO_GIP | COD_UFFICIO_GIP | VARCHAR2 (11 CHAR) | Codice ufficio del registro gip |
| ANNO_REGE_DIB | ANNO_REGE_DIB | NUMBER | Anno del registro dib |
| NUMERO_REGE_DIB | NUMERO_REGE_DIB | NUMBER | Numero del registro dib |
| COD_UFFICIO_DIB | COD_UFFICIO_DIB | VARCHAR2 (11 CHAR) | Codice ufficio del registro dib |
| ANNO_REGE_CAS | ANNO_REGE_CAS | NUMBER | Anno del registro cas |
| NUMERO_REGE_CAS | NUMERO_REGE_CAS | NUMBER | Numero del registro cas |
| COD_UFFICIO_CAS | COD_UFFICIO_CAS | VARCHAR2 (11 CHAR) | Codice ufficio del registro cas |
| ANNO_REGE_CAP | ANNO_REGE_CAP | NUMBER | Anno del registro cap |
| NUMERO_REGE_CAP | NUMERO_REGE_CAP | NUMBER | Numero del registro cap |
| COD_UFFICIO_CAP | COD_UFFICIO_CAP | VARCHAR2 (11 CHAR) | Codice ufficio del registro cap |
| ANNO_REGE_CASAP | ANNO_REGE_CASAP | NUMBER | Anno del registro casap |
| NUMERO_REGE_CASAP | NUMERO_REGE_CASAP | NUMBER | Numero del registro casap |
| COD_UFFICIO_CASAP | COD_UFFICIO_CASAP | VARCHAR2 (11 CHAR) | Codice ufficio del registro casap |
| COD_OPERATORE_INSERIMENTO | COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMEN TO | COD_OPERATORE_AGGIORNAMEN TO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| ID_MISURA_CAUTELARE | ID_MISURA_CAUTELARE | NUMBER | Identificativo della misura cautelare |
| ID_ANNOTAZIONE_MANUALE | ID_ANNOTAZIONE_MANUALE | NUMBER | Identificativo dell’annotazione manuale |
| STATO_TRASMISSIONE_ISC | STATO_TRASMISSIONE_ISC | VARCHAR2 (1 CHAR) | Stato della trasmissione per quanto riguarda l’iscrizione |
| STATO_TRASMISSIONE_VAL | STATO_TRASMISSIONE_VAL | VARCHAR2 (1 CHAR) | Stato della trasmissione per quanto riguarda la validazione |
| DATA_INIZIO_USATA | DATA_INIZIO_USATA | DATE | Data inizio mc |
| DATA_FINE_USATA | DATA_FINE_USATA | DATE | Data fine mc |
| ID_PROVV_BDMC | ID_PROVV_BDMC | NUMBER | Identificativo del provvedimento di bdmc |



# MISURA_CAUTELARE_CUMULO
tabella contenente di dati relativi alle misure cautelari di un cumulo. utilizzata dal sottosistema siep.
| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_MISURA_CAUTELARE_CUMULO | NUMBER(38) | Identificativo della tabella |
| COD_TIPO_MISURA | VARCHAR2(2) | CG_REF_CODES.RV_DOMAIN= ’NATURA_MISURA_SICUREZZA’ |
| DATA_INIZIO | DATE | CG_REF_CODES.RV_DOMAIN= ’TIPO_MISURA_SICUREZZA’ |
| DATA_FINE | DATE | Durata: Numero Anni |
| NUM_ANNI | NUMBER(4) | Durata: Numero Mesi |
| NUM_MESI | NUMBER(4) | Durata: Numero Giorno |
| NUM_GIORNI | NUMBER(4) | Anno Reg. Mod. 38 |
| GIORNI | NUMBER(6) | Anno Reg. Mod. 38 |
| FLAG_MODIFICA_MANUALE | VARCHAR2(12) | E=estratto M=modificato C=Cancellato I=Iscritto |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2(4) | Note inserite dall''operatore in fase di Modifica Cancellazione Iscrizione |
| ALTRO_LUOGO_DETENZIONE | VARCHAR2(1000) | FK alla tabella TITOLO_CUMULATO |
| AUTORITA_COMPETENTE | VARCHAR2(2) | Eventuale ID del record MISURA_SICUREZZA da cui è stato derivato questo record |
| AUTORITA_COMPETENTE_SEDE | VARCHAR2(6) | ‘A’ se misura annullata |
| AUTORITA_COMPETENTE_INDIRIZZO | VARCHAR2(1000) | Data Fine Validità |
| TIT_ID_TITOLO_CUMULATO | NUMBER(38) | FK alla tabella TITOLO_CUMULATO |
| FLAG_STATO | VARCHAR2(1) | E=estratto M=modificato C=Cancellato I=Iscritto |
| MOTIVO_MODIFICA | VARCHAR2(2000) | Note inserite dall''operatore in fase di Modifica Cancellazione Iscrizione |
| ID_MISURA_CAUTELARE_ORIGINE | NUMBER(38) | Eventuale ID del record MISURA_CAUTELARE da cui è stato derivato questo record |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |



# MISURA_SICUREZZA
tabella contenente di dati relativi alle misure cautelari. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_MISURA_SICUREZZA | NUMBER NOT NULL | Valore di chiave primaria numerica legata alla sequence MIS_SIC_SEQ |
| COD_NATURA | VARCHAR2 (4 CHAR) NOT NULL | Codifica della Natura Misura Sicurezza (detentiva non detentiva ...). Associata al Dominio NATURA_MISURA_SICUREZZA di CG_REF_CODES. |
| COD_TIPO | VARCHAR2 (2 CHAR) | Tipo di misura (casa lavoro ecc.). Associata al Dominio TIPO_MISURA_SICUREZZA di CG_TEF_CODES. |
| NUM_ANNI | NUMBER | Numero di anni della misura di sicurezza |
| NUM_MESI | NUMBER | Numero di mesi della misura di sicurezza |
| NUM_GIORNI | NUMBER | Numero di giorni della misura di sicurezza |
| ANNO_REG_38 | NUMBER | Anno del registro |
| NUM_REG_38 | NUMBER | Numero del registro |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| COD_TIPO_ASSOLUZIONE | VARCHAR2 (2 CHAR) | Codifica Tipo Assoluzione. Associato al Dominio TIPO_ASSOLUZIONE di CG_REF_CODES. |
| NOTE | VARCHAR2 (2000 CHAR) | Note |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER | Indica il Fascicolo SIEP a cui si riferisce una MS definita in SIUS' |
| FAS_SIE_ID_FASCICOLO_SIEP_RIF | NUMBER(38) | Indica il Fascicolo SIEP (Principale) a cui si riferisce una MS definita in SIUS' |
| SEN_ID_SENTENZA | NUMBER(38) | Identificativo della sentenza |
| DATA_DECORRENZA | DATE | Data di decorrenza |
| DATA_FINE_VALIDITA | DATE | Data fine validità |
| FLAG_ANNULLA_MISURA | VARCHAR2(1 CHAR) | S/N annulla misura |
| MIS_ID_MISURA_SICUREZZA | NUMBER(38) | Identificativo della misura di sicurezza |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2(4 CHAR) | Identificativo dell’istituto di detenzione |
| LUOGO_ESECUZIONE_MISURA | VARCHAR2(2000 CHAR) | Descrizione del luogo di esecuzione della misura |
| FL_FORMA_MISURA | NUMBER(1) | Se impostato a 1 indica che  presente la permanenza in casa se impostato a 2 indica che è presente il collocamento in comunità |
| DESCRIZIONE_COMUNITA | VARCHAR2(2000) | Descrizione della comunità |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| MIS_SIC_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| MIS_SIC_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |





# MISURA_SICUREZZA_CUMULO
tabella contenente di dati relativi alle misure di sicurezza di un cumulo. utilizzata dal sottosistema siep.
| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_MISURA_SICUREZZA_CUMULO | NUMBER(38) NOT NULL | Identificativo della misura di sicurezza |
| COD_NATURA | VARCHAR2(4 CHAR) NOT NULL | CG_REF_CODES.RV_DOMAIN= ’NATURA_MISURA_SICUREZZA’ |
| COD_TIPO | VARCHAR2(2 CHAR) | CG_REF_CODES.RV_DOMAIN= ’TIPO_MISURA_SICUREZZA’ |
| NUM_ANNI | NUMBER(2) | Durata: Numero Anni |
| NUM_MESI | NUMBER(2) | Durata: Numero Mesi |
| NUM_GIORNI | NUMBER(3) | Durata: Numero Giorno |
| ANNO_REG_38 | NUMBER(4) | Anno Reg. Mod. 38 |
| NUM_REG_38 | NUMBER(6) | Anno Reg. Mod. 38 |
| FLAG_STATO | VARCHAR2(1 CHAR) NOT NULL | E=estratto M=modificato C=Cancellato I=Iscritto |
| MOTIVO_MODIFICA | VARCHAR2(2000 CHAR) | Note inserite dall''operatore in fase di Modifica Cancellazione Iscrizione |
| TIT_ID_TITOLO_CUMULATO | NUMBER(38) NOT NULL | FK alla tabella TITOLO_CUMULATO |
| ID_MISURA_SICUREZZA_ORIGINE | NUMBER(38) | Eventuale ID del record MISURA_SICUREZZA da cui è stato derivato questo record |
| FLAG_ANNULLA_MISURA | VARCHAR2(1 CHAR) | ‘A’ se misura annullata |
| DATA_FINE_VALIDITA | DATE | Data Fine Validità |
| MIS_ID_MISURA_SICUREZZA_CUMULO | NUMBER(38) | FK alla tabella MISURA_SICUREZZA_CUMULO |
| MIS_ID_MISURA_SICUREZZA_ORIG | NUMBER(38) | FK alla tabella MISURA_SICUREZZA origine |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2(4 CHAR) | Id della tabella ISTITUTO_DETENZIONE |
| LUOGO_ESECUZIONE_MISURA | VARCHAR2(2000 CHAR) | Luogo Esecuzione Misura |
| FLAG_DATI_FINALI | VARCHAR2(1 CHAR) | S/N indica se la misura è stata selezionata per i dati Finali Cumulo |
| ANNO_FASCICOLO_CLASSE_IV | NUMBER(4) | Anno Procedimento Classe IV |
| NUMERO_FASCICOLO_CLASSE_IV | NUMBER(38) | Numero Procedimento Classe IV |
| COD_AUTORITA_EMITT_CLASSE_IV | VARCHAR2(11 CHAR) | Codice Ufficio Procedimento Classe IV |
| LUOGO_AUTORITA_EMITT_CLASSE_IV | VARCHAR2(11 CHAR) | Luogo Ufficio Procedimento Classe IV |
| FLAG_STATO_MISURA | VARCHAR2(6 CHAR) | CG_REF_CODES.RV_DOMAIN= ’STATO_MISURA_CUMULO’ |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(1 CHAR) NOT NULL | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | VARCHAR2(100 CHAR) | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | DATE | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(11 CHAR) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | VARCHAR2(100 CHAR) | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | DATE | Codice Ufficio Utente ultimo aggiornamento |



# MISURA_SICUREZZA_SENTENZA_SIGE
tabella contenente ii dati relativi alle misure di sicurezza di sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| MIS_ID_MISURA_SICUREZZA | NUMBER NOT NULL | Identificativo misure di sicurezza |
| FAS_SIGE_SEN_ID | NUMBER NOT NULL | Identificativo della sentenza di sige |



# MOTIVAZIONE_DECRETO
tabella contenente di dati relativi alla motivazione di un decreto . utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_MOTIVAZIONE_DECRETO | NUMBER NOT NULL | Valore di chiave primaria numerica legata alla sequence MOT_DEC_SEQ. |
| COD_TIPO_MOTIVAZIONE | VARCHAR2 (2 CHAR) | Codifica del Tipo Motivazione. |
| DESCR_MOTIVAZIONE | VARCHAR2 (200 CHAR) | Descrizione della motivazione |
| ALTRA_MOTIVAZIONE | VARCHAR2 (2000 CHAR) | Altra motivazione |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| DEP_DEC_ID_DEPOSITO_DECRETO | NUMBER | Identificativo del deposito decreto |
| PROGR_MOTIVAZIONE | NUMBER | Progressivo della motivazione |
| EVE_ID_EVENTO. | NUMBER | Identificativo dell’evento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| MOT_DEC_DEP_DEC_FK | DEP_DEC_ID_DEPOSITO_DECRETO | (DEPOSITO_DECRETO.ID_DEPOSITO_DECRETO) |
| MOT_DEC_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |



# MOTIVAZIONE_PROVVED_SIGE
tabella contenente di dati relativi alla motivazione di un provvedimento sige . utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_MOTIVAZIONE_PROVVED_SIGE | NUMBER NOT NULL | Valore di chiave primaria numerica legata alla sequence MOT_PRO_SIG_SEQ. |
| COD_TIPO_MOTIVAZIONE | VARCHAR2 (2 CHAR) | Codifica del Tipo Motivazione. Legata al Dominio MOTIVO_INAMMISSIBILITA_SIGE. |
| DESCR_MOTIVAZIONE | VARCHAR2 (200 CHAR) | Descrizione della motivazione |
| ALTRA_MOTIVAZIONE | VARCHAR2 (2000 CHAR) | Altra motivazione |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| PRO_SIG_ID_PROVVED_SIGE | NUMBER | Identificativo del provvedimento SIGE |
| PROGR_MOTIVAZIONE | NUMBER | Progressivo della motivazione |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| MOT_PRO_SIG_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |


# MOTIVO_EVENTO
tabella contenente di dati relativi alla motivazione di una revoca di un evento. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_MOTIVO_EVENTO | NUMBER NOT NULL | Identificativo del motivo dell’evento |
| COD_MOTIVO_REVOCA | VARCHAR2 (4 CHAR) | Codice del motivo della revoca |
| COD_MOTIVO_REVOCA_PM | VARCHAR2 (4 CHAR) | Codice del motivo della revoca del PM |
| MOTIVAZIONI | VARCHAR2 (2000 CHAR) | Descrizione della motivazione |
| EVE_ID_EVENTO | NUMBER NOT NULL. | Identificativo dell’evento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| EVE_ID_EVENTO_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |


# MOVIMENTO_REG_ESECUZIONE
tabella contenente di dati relativi ai movimenti del registro dell’esecuzione. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_MOVIMENTO_REG_ESECUZIONE | NUMBER NOT NULL | Valore di chiave primaria numerica legata alla sequence MOV_REG_SEQ . |
| COD_MOVIMENTO | VARCHAR2 (240 CHAR) | Codice del movimento |
| COD_TIPO_MOVIMENTO | VARCHAR2 (240 CHAR) | Codice del tipo di movimento |
| DATA_MOVIMENTO | DATE | Data del movimento |
| COD_RICHIEDENTE | VARCHAR2 (2 CHAR) | Codice del richiedente |
| COD_OGGETTO_RICHIESTO | VARCHAR2 (2 CHAR) | Codice dell’oggetto richiesto |
| DATA_RICHIESTA | DATE | Data della richiesta |
| DESCR_RICHIESTA | VARCHAR2 (2000 CHAR) | Descrizione della richiesta |
| COD_TIPO_DECISIONE | VARCHAR2 (2 CHAR) | Codice del tipo di decisione |
| COD_TENORE_DECISIONE | VARCHAR2 (2 CHAR) | Codice del tenore della decisione |
| COD_MAGISTRATO | VARCHAR2 (6 CHAR) | Codice del magistrato |
| DATA_DECRETO_SOSPENSIONE | DATE | Data del decreto di sospensione |
| DATA_TX_TDS | DATE | Data della transazione del tribunale di sorveglianza |
| DATA_DECISIONE_TDS | DATE | Data della decisione del tribunale di sorveglianza |
| COD_TENORE_DECISIONE_TDS | VARCHAR2 (2 CHAR) | Codice del tenore della decisione del tribunale di sorveglianza |
| DATA_TX_COMPETENZA | DATE | Data di transazione di competenza |
| COD_UFFICIO_DESTINATARIO | VARCHAR2 (11 CHAR) | Codice ufficio destinatario |
| DATA_RECLAMO | DATE | Data reclamo |
| DATA_TERMINE_MISURA | DATE | Data temine misura |
| NOTE | VARCHAR2 (2000 CHAR) | Note |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| GEN_PRID_GENERALE_PROCEDIMENTO | NUMBER NOT NULL. | Identificativo del generale procedimento |

Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| MOV_REG_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO | (GENERALE_PROCEDIMENTO.ID_GENERALE_PROCEDIMENTO) |



# NOME_PROVVEDIMENTO
tabella contenente di dati relativi al nome del provvedimento per un evento. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione | Descrizione |
| --- | --- | --- | --- |
| COD_NOME_PROVVEDIMENTO | VARCHAR2 (5 CHAR) NOT NULL | VARCHAR2 (5 CHAR) NOT NULL | Codifica del Nome Provvedimento. Associato al Dominio NOME_PROVVEDIMENTO di CG_REF_CODES. |
| EVE_ID_EVENTO | NUMBER NOT NULL. | NUMBER NOT NULL. | Identificativo dell’evento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| NOM_PRO_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |




# NOTE
tabella contenente di dati relativi alle note di un fascicolo. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_NOTE | NUMBER NOT NULL | Identificativo della tabella note |
| DATA | DATE | Data della nota |
| DESCRIZIONE | VARCHAR2 (2000 CHAR) | Descrizione della nota |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER NOT NULL | Identificativo del fascicolo SIUS |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| FAS_SIGE_ID_FASCICOLO_SIGE | NUMBER | Identificativo del fascicolo SIGE |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| NOTE_FAS_SIE_SIEP_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |
| NOTE_FAS_SIU_SIUS_FK | FAS_SIU_ID_FASCICOLO_SIUS | (FASCICOLO_SIUS.ID_FASCICOLO_SIUS) |





# NOTE_FASCICOLO
tabella contenente di dati relativi alle note degli avvocati per un fascicolo siep. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| NOTA_DISPOSITIVO | VARCHAR2 (200 CHAR) | Nota del dispositivo |
| NOTA_AVVOCATI | VARCHAR2 (500 CHAR) | Nota degli avvocati |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL. | Identificativo del fascicolo SIEP |




# NOTIFICA
tabella contenente di dati relativi alle notifiche. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_NOTIFICA | NUMBER NOT NULL | Chiave naturale dell'entità. Legata alla sequence NOT_SEQ |
| COD_TIPO_NOTIFICA | VARCHAR2 (2 CHAR) NOT NULL | Distingue il tipo di notifica determinando le eventuali differenze sui documenti stampati. Legato a dominio assume i seguenti valori: N = notifica E = esecuzione. |
| DATA_AVVENUTA_NOTIFICA | DATE | Data di arrivo della notifica da inserire se la notifica necessita di ritorno. |
| DATA_INVIO | DATE NOT NULL | Data invio della notifica. |
| COD_ESITO | VARCHAR2 (2 CHAR) | Eventuale esito di consegna o meno della notifica. Legato a dominio ESITO assume i seguenti valori: ESEGUITA NON ESEGUITA. |
| NOTE | VARCHAR2 (2000 CHAR) | Eventuali note di accompagno della notifica. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| CODICE_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| EVE_ID_EVENTO | NUMBER NOT NULL | Identificativo dell’evento |
| AUT_EST_ID_AUTORITA_ESTERNA | NUMBER | Identificativo dell’autorità esterna |
| SOG_ID_SOGGETTO | NUMBER | Identificativo del soggetto |
| AVV_ID_AVVOCATO_FASCICOLO_ SIEP | NUMBER | Identificativo dell’avvocato SIEP |
| UFF_COD_UFFICIO | VARCHAR2 (11 CHAR) | Codice dell’ufficio |
| SOLLECITO | NUMBER | Numero del sollecito |
| AVV_ID_AVVOCATO_FASCICOLO_ SIUS | NUMBER | Identificativo dell’avvocato SIUS |
| CSS_ID_CSSA | NUMBER | Codice del CSSA |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2 (4 CHAR) | Identificativo dell’istituto di detenzione |
| AUT_EST_ID_AUTORITA_EST_DELEG | NUMBER | Identificativo dell’autorità esterna del delegato |
| AVV_ID_AVVOCATO_FASCICOLO_ SIGE | NUMBER | Identificativo dell’avvocato SIGE |
| CUR_ID_CURATORE. | NUMBER | Identificativo del curatore |
| COD_UFF_UEPE_USSM_SS | VARCHAR2(11) | Indica Codice Ufficio Destinatario Servizio Sociale |
| COD_UFF_UDS_UDSM | VARCHAR2(11) | Indica Codice Ufficio Destinatario Magistrato Sorveglianza |
| COD_UFF_TDS_TDSM | VARCHAR2(11) | Indica Codice Ufficio Destinatario Ente Sorveglianza |
| FLAG_NOTIFICA_VIA_FAX | NUMBER(1) | Flag che indica se la notifica all’avvocato deve essere inviata via Fax o meno |
| ID_PARTE_UDIENZA | NUMBER(38) | Indica la chiave delle parti civili e offese inserite in udienza |
| ID_CIVILMENTE_OBBLIGATO | NUMBER(38) |  |


Chiavi Esterne

| CONSTRAINT_NAME | CONSTRAINT_NAME | COLUMN_NAME | COLUMN_NAME | REFERENCES_COLUMN | REFERENCES_COLUMN |
| --- | --- | --- | --- | --- | --- |
| NOT_AUT_EST_DELEG_FK | AUT_EST_ID_AUTORITA_EST_DELEG | AUT_EST_ID_AUTORITA_EST_DELEG | (AUTORITA_ESTERNA.ID_AUTORITA_ESTERNA) | (AUTORITA_ESTERNA.ID_AUTORITA_ESTERNA) |  |
| NOT_1_AUT_EST_FK | AUT_EST_ID_AUTORITA_ESTERNA | AUT_EST_ID_AUTORITA_ESTERNA | (AUTORITA_ESTERNA.ID_AUTORITA_ESTERNA) | (AUTORITA_ESTERNA.ID_AUTORITA_ESTERNA) |  |
| NOT_1_AVV_FAS_FK | AVV_ID_AVVOCATO_FASCICOLO_SIEP | AVV_ID_AVVOCATO_FASCICOLO_SIEP | (AVVOCATO_FASCICOLO_SIEP.ID_AVVOCATO_FASCICOLO_SIEP) | (AVVOCATO_FASCICOLO_SIEP.ID_AVVOCATO_FASCICOLO_SIEP) |  |
| NOT_1_CSS_FK | CSS_ID_CSSA | CSS_ID_CSSA | (CSSA.ID_CSSA) | (CSSA.ID_CSSA) |  |
| NOT_1_EVE_FK | EVE_ID_EVENTO | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) | (EVENTO.ID_EVENTO) |  |
| NOT_1_SOG_FK | SOG_ID_SOGGETTO | SOG_ID_SOGGETTO | (SOGGETTO.ID_SOGGETTO) | (SOGGETTO.ID_SOGGETTO) |  |
| NOT_2_AVV_FAS_FK | AVV_ID_AVVOCATO_FASCICOLO_SIUS | AVV_ID_AVVOCATO_FASCICOLO_SIUS | (AVVOCATO_FASCICOLO_SIUS.ID_AVVOCATO_FASCICOLO_SIUS) | (AVVOCATO_FASCICOLO_SIUS.ID_AVVOCATO_FASCICOLO_SIUS) |  |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| RINNOVO | RIN_NOT_FK | NOT_ID_NOTIFICA |
| SCADENZARIO_SIEP | SCA_SIE_NOT_FK | NOT_ID_NOTIFICA |
| VERBALE | VER_NOT_FK | NOT_ID_NOTIFICA |


# NOTIFICA_CUMULO
tabella contenente di dati relativi alle Notifiche di provvedimenti del Procedimento Cumulato. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_NOTIFICA_CUMULO | NUMBER(38) | Sequence |
| COD_TIPO_NOTIFICA | VARCHAR2(2) | CG_REF_CODES.RV_DOMAIN= ‘TIPO_NOTIFICA’ |
| DATA_AVVENUTA_NOTIFICA | DATE | Data avvenuta notifica |
| DATA_INVIO | DATE | Data invio |
| COD_ESITO | VARCHAR2(2) | CG_REF_CODES.RV_DOMAIN= ‘ESITO_NOTIFICA’ |
| NOTE | VARCHAR2(2000) | Eventuali note/indirizzo |
| STAT_ID_STATO_ESEC_TIT_CUM | NUMBER(38) | FK alla tabella STATO_ESEC_TITOLO_CUMULATO di riferimento |
| AUT_EST_ID_AUTORITA_ESTERNA | NUMBER(38) | Eventuale FK alla tabella AUTORITA_ESTERNA di riferimento |
| SOG_ID_SOGGETTO | NUMBER(38) | Eventuale FK alla tabella SOGGETTO di riferimento |
| AVV_ID_AVVOCATO_FASCICOLO_SIEP | NUMBER(38) | Eventuale FK alla tabella AVVOCATO_FASCICOLO_SIEP di riferimento |
| UFF_COD_UFFICIO | VARCHAR2(11) | Codice dell’Ufficio destinatario |
| CSS_ID_CSSA | NUMBER(38) | Eventuale FK alla tabella CSSA di riferimento |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2(4) | Eventuale FK alla tabella ISTITUTO_DETENZIONE di riferimento |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |

# NOTIFICHE_SIES
tabella contenente di dati relativi alle notifiche sies. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_NOTIFICHE_SIES | NUMBER NOT NULL | Identificativo della tabella |
| ANNO_SIEP | NUMBER | Anno del fascicolo SIEP |
| PROG_SIEP | NUMBER | Progressivo del fascicolo SIEP |
| UFFICIO_SIEP | VARCHAR2 (11 CHAR) | Codice dell’ufficio del fascicolo SIEP |
| ANNO_FASC_BDMC | NUMBER | Anno del fascicolo bdmc |
| UFFICIO_FASC_BDMC | VARCHAR2 (15 CHAR) | Codice dell’ufficio del fascicolo bdmc |
| NUMERO_FASC_BDMC | NUMBER | Numero del fascicolo bdmc |
| TIPO_NOTIFICA | CHAR (1 CHAR) | Tipo di notifica |
| DATA_NOTIFICA | DATE | Data della notifica |
| STATO_TRASMISSIONE | CHAR (1 CHAR) | Stato della trasmissione |
| DATA_TRASMISSIONE | DATE | Data della trasmissione |
| ID_PREN | NUMBER | Identificativo |
| PROG_PERI_PRES | NUMBER | Progressivo |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| ID_EVENTO | NUMBER | Identificativo dell’evento |
| ID_FASCICOLO_BDMC | NUMBER | Identificativo del fascicolo bdmc |



# NOTIZIA_REATO
tabella contenente di dati relativi alle notizie di reato. utilizzata dal sottosistema siep-sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_NOTIZIA_REATO | NUMBER NOT NULL | Identificativo della tabella |
| PROGR_NOTIZIA | VARCHAR2 (4 CHAR) | Progressivo della notizia di reato |
| DATA_PERVENIMENTO | DATE | Data del pervenimento |
| ACQUISIZIONE_DIRETTA | VARCHAR2 (1 CHAR) | Flag acquisizione diretta |
| DATA_FATTO | DATE | Data del fatto |
| COD_FONTE | VARCHAR2 (10 CHAR) | Codice della fonte |
| TIPO_FONTE | VARCHAR2 (3 CHAR) | Tipo della fonte |
| COD_COMUNE_FONTE | VARCHAR2 (6 CHAR) | Codice comune della fonte |
| NUM_REG_AUTORITA | VARCHAR2 (25 CHAR) | Numero di registro dell’autorità |
| LUOGO_PROVENIENZA | VARCHAR2 (78 CHAR) | Luogo di provenienza |
| DATA_ACQUISIZIONE | DATE | Data di acquisizione |
| NUMERO_RICEVUTA | VARCHAR2 (9 CHAR) | Numero della ricevuta |
| DESCRIZIONE_FONTE | VARCHAR2 (30 CHAR) | Descrizione della fonte |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMEN TO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| DATA_ARRESTO | DATE | Data dell’arresto |
| DATA_FERMO | DATE | Data del fermo |
| FLAG_FOTOSEGNALATO | VARCHAR2 (1 CHAR) | S/N flag foto segnaletica |
| FLAG_ARRESTATO | VARCHAR2 (1 CHAR) | S/N flag arrestato |
| DATA_FOTO | DATE | Data della foto |
| COD_COMUNE_FOTO | VARCHAR2 (6 CHAR) | Codice del comune della foto |
| COD_AUTORITA_FOTO | VARCHAR2 (11 CHAR) | Codice autorità della foto |
| FAS_ID_FASCICOLO_SIGE | NUMBER | Identificativo del fascicolo SIGE |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| NOT_REA_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |




# NUOVA_ISTANZA
tabella contenente di dati relativi alle istanze. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_NUOVA_ISTANZA | NUMBER NOT NULL | Identificativo della tabella |
| COD_CONTENUTO | VARCHAR2 (4 CHAR) | Codice del contenuto |
| DATA_ISTANZA | DATE NOT NULL | Data dell’istanza |
| NOTE | VARCHAR2 (2000 CHAR) | Note |
| FLAG_PRESDEP | VARCHAR2 (1 CHAR) | S/N Flag presentante |
| SOGG_PRESENTANTE | VARCHAR2 (100 CHAR) | Soggetto presentante |
| SOGG_PRESENTANTE_IDENTIFICATO | VARCHAR2 (100 CHAR) | Identificativo del soggetto presentante |
| AVV_ID_AVVOCATO_PRESENTANTE | NUMBER | Identificativo dell’avvocato presentante |
| COD_AUTORITA_MITTENTE | VARCHAR2 (6 CHAR) | Codice dell’autorità mittente |
| COD_SEDE_MITTENTE | VARCHAR2 (6 CHAR) | Sede dell’autorità mittente |
| AVV_ID_AVVOCATO | NUMBER | Identificativo dell’avvocato |
| COD_ESITO | VARCHAR2 (4 CHAR) | Codice dell’esito |
| ANNO_REGISTRO | NUMBER | Anno del registro |
| PROGR_REGISTRO | NUMBER | Progressivo del registro |
| COD_TIPO_UFFICIO_DESTINATARIO | VARCHAR2 (6 CHAR) | Tipo ufficio destinatario |
| COD_LUOGO_DESTINATARIO | VARCHAR2 (6 CHAR) | Luogo del destinatario |
| COD_UFFICIO_DESTINATARIO | VARCHAR2 (11 CHAR) | Ufficio destinatario |
| COD_STATO_ISTANZA | VARCHAR2 (2 CHAR) | Codice dello stato dell’istanza |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL | Identificativo del fascicolo SIEP |
| EVE_ID_EVENTO | NUMBER NOT NULL | Identificativo dell’evento |
| DATA_INOLTRO_PM | DATE | Data di inoltro al pubblico ministero |
| DATA_NOTIFICA_AVVOCATO | DATE | Data di notifica all’avvocato |
| TIPO_AVVOCATO | VARCHAR2 (2 CHAR) | Tipologia dell’avvocato |
| DESCR_MITTENTE | VARCHAR2 (200 CHAR). | Descrizione del mittente |



# PARAMETRO
tabella contenente i dati relativi ai parametri impostati dall’utente, come ad esempio il periodo feriale, il temine sottoscrizione verbale. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PARAMETRO | NUMBER NOT NULL | Identificato della tabella |
| NOME_PARAMETRO | VARCHAR2 (50 CHAR) NOT NULL | Nome del parametro |
| VALORE | VARCHAR2 (500 CHAR) | Valore |
| ANNI | NUMBER | Numero di anni |
| MESI | NUMBER | Numero di mesi |
| GIORNI | NUMBER | Numero di giorni |
| IMPORTO | NUMBER (38) | Importo |
| DATA_INIZIO_VALIDITA | DATE | Data inizio validità |
| DATA_FINE_VALIDITA | DATE | Data fine validità |
| COD_UFFICIO_VALIDITA | VARCHAR2 (11 CHAR) | Codice ufficio che ha validato il parametro |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |


# PARTI_UDIENZA_DIFENSORE
tabella contenente i dati relativi ai difensori parti udienza. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_AVVOCATO_PARTE_UDIENZA | NUMBER(38) | Identificativo Della Tabella |
| COD_TIPO_AVVOCATO | VARCHAR2(2) | Tipo Avvocato |
| DATA_INIZIO_VALIDITA | VARCHAR2(2) | Data Inizio Validità |
| DATA_FINE_VALIDITA | DATE | Data Fine Validità |
| COD_MOTIVO_DESIGNAZIONE | DATE | Motivo Della Designazione |
| COD_TIPO_AUTORITA | VARCHAR2(4) | Tipo Autorità |
| SEDE_TIPO_AUTORITA | VARCHAR2(2) | Sede Autorità |
| INDIRIZZO_TIPO_AUTORITA | VARCHAR2(6) | Indirizzo Autorità |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Utenza Dell’operatore Che Ha Effettuato L’inserimento |
| DATA_INSERIMENTO | DATE | Data Inserimento |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11) | Ufficio Dell’operatore Che Ha Effettuato L’inserimento |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100) | Utenza Dell’operatore Che Ha Effettuato L’aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data Dell’aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(11) | Ufficio Dell’operatore Che Ha Effettuato L’aggiornamento |
| AVV_ID_AVVOCATO | NUMBER(38) | Identificativo Dell’avvocato |
| SOGG_ID_SOGGETTO | NUMBER(38) | Identificativo Del Soggetto |
| NOTE | VARCHAR2(2000) | Note |
| COD_TIPO_AUTORITA_DIF | VARCHAR2(2) | Tipo Autorità Difensore |
| SEDE_TIPO_AUTORITA_DIF | VARCHAR2(6) | Sede Autorità Difensore |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2(4) | Identificativo Istituto Detenzione |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| ID_AVVOCATO_FK | AVV_ID_AVVOCATO | (AVVOCATO.ID_AVVOCATO) |
| ID_PARTE_UDEINZA_FK | SOGG_ID_SOGGETTO | (ANAGRAFICA_PARTI_UDIENZA.ID_SOGGETTO) |


# PENA_ACCESSORIA
tabella contenente i dati relativi alle pene accessorie. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PENA_ACCESSORIA | NUMBER NOT NULL | Chiave naturale numerica della tabella. |
| COD_TIPO_PENA_ACCESSORIA | VARCHAR2 (3 CHAR) DEFAULT '-' NOT NULL | Indica la tipologia della pena accessoria inflitta. Deriva da dominio e ad esempio può assumere i seguenti valori (estratto del totale): PERDITA DELLA PATRIA POTESTA' PUBBLICAZIONE DI SENTENZA PENALE DI CONDANNA REVOCA DELLA LICENZA DI CACCIA REVOCA DELLA PATENTE DI GUIDA RIMOZIONE DAL GRADO RIPRISTINO DELLO STATO DEI LUOGHI RITIRO DELLA PATENTE DI GUIDA SOSPENSIONE DA OGNI INCARICO DI PUBBLICO SERVIZIO SOSPENSIONE DA OGNI PUBBLICO UFFICIO ecc. |
| DURATA | VARCHAR2 (1 CHAR) | Campo indicante la tipologia di durata della pena accessoria inflitta. Deriva da domino e vale: DURANTE LA PENA PERPETUA. |
| NUM_ANNI | NUMBER | Numero anni di durata della pena accessoria. |
| NUM_MESI | NUMBER | Numero mesi di durata della pena accessoria. |
| NUM_GIORNI | NUMBER | Numero giorni di durata della pena accessoria. |
| FLAG_CONDONATA | VARCHAR2 (1 CHAR) | Flag indicante l'eventuale condono della pena. |
| DATA_DPR | DATE | Data di emissione del DPR con il quale si condona la pena accessoria. |
| NUM_DPR | VARCHAR2 (8 CHAR) | Numero del DPR con il quale si condona la pena accessoria. |
| FLAG_DICHIARAZIONE_FALSITA | VARCHAR2 (1 CHAR) | Campo per la gestione della dichiarazione di falsità da parte del soggetto. |
| FLAG_REVOCA_CONDONO | VARCHAR2 (1 CHAR) | Campo indicante se il condono della pena accessoria è stato revocato. La revoca avviene attraverso una sentenza o una ordinanza. |
| DATA_SENTENZA_REVOCA | DATE | Data Sentenza di revoca condono. |
| ANNO_SENTENZA_REVOCA | NUMBER | Anno Sentenza di revoca condono. |
| NUMERO_SENTENZA_REVOCA | VARCHAR2 (6 CHAR) | Numero Sentenza di revoca condono. |
| COD_TIPO_UFFICIO_SENTENZA_REVO | VARCHAR2 (6 CHAR) DEFAULT '-' | Tipo Ufficio emittente Sentenza di revoca condono. |
| COD_LUOGO_SENTENZA_REVOCA | VARCHAR2 (6 CHAR) DEFAULT '-' | Comune di appartenenza dell'ufficio emittente la sentenza di revoca condono. |
| ANNO_REGE_PM_REVOCA | NUMBER | Parte della chiave del fascicolo Re.Ge. emesso a livello di PM. |
| NUMERO_REGE_PM_REVOCA | VARCHAR2 (6 CHAR) | Parte della chiave del fascicolo Re.Ge. emesso a livello di PM. |
| ANNO_REGE_GIP_REVOCA | NUMBER | Parte della chiave del fascicolo Re.Ge. emesso a livello di PM. |
| NUMERO_REGE_GIP_REVOCA | VARCHAR2 (6 CHAR) | Parte della chiave del fascicolo Re.Ge. emesso a livello di PM. |
| ANNO_REGE_DIB_REVOCA | NUMBER | Parte della chiave del fascicolo Re.Ge. emesso a livello Dibattimentale. |
| NUMERO_REGE_DIB_REVOCA | VARCHAR2 (6 CHAR) | Parte della chiave del fascicolo Re.Ge. emesso a livello Dibattimentale. |
| ANNO_REGE_CAS_REVOCA | NUMBER | Parte della chiave del fascicolo Re.Ge. emesso a livello di Corte d'Assise. |
| NUMERO_REGE_CAS_REVOCA | VARCHAR2 (6 CHAR) | Parte della chiave del fascicolo Re.Ge. emesso a livello di Corte d'Assise. |
| ANNO_REGE_CAP_REVOCA | NUMBER | Parte della chiave del fascicolo Re.Ge. emesso a livello di Corte d'Appello. |
| NUMERO_REGE_CAP_REVOCA | VARCHAR2 (6 CHAR) | Parte della chiave del fascicolo Re.Ge. emesso a livello di Corte d'Appello. |
| ANNO_REGE_CASAP_REVOCA | NUMBER | Parte della chiave del fascicolo Re.Ge. emesso a livello di Corte d’Assise d'Appello. |
| NUMERO_REGE_CASAP_REVOCA | VARCHAR2 (6 CHAR) | Parte della chiave del fascicolo Re.Ge. emesso a livello di Corte d’Assise d'Appello. |
| NOTE | VARCHAR2 (2000 CHAR) | Eventuali note aggiuntive sulla pena accessoria o sul suo trattamento. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| DATA_INIZIO_VALIDITA | DATE | Data inizio validità |
| DATA_FINE_VALIDITA | DATE | Data fine validità |
| ANNO_ORDINANZA_GE | NUMBER | Anno dell’ordinanza del GE |
| NUMERO_ORDINANZA_GE | NUMBER | Numero di ordinanza del GE |
| DATA_ORDINANZA_GE | DATE | Data di ordinanza del GE |
| ESTREMI_CONDONO | VARCHAR2 (100 CHAR) | Estremi del condono |
| ID_PENA_ACCESSORIA_ORIGINE | NUMBER | Identificativo della pena accessoria originaria |
| COD_NUOVO_TIPO_PENA_ACCESSORIA | VARCHAR2 (3 CHAR) | Tipologia della pena accessoria |
| COD_TIPO_UFFICIO_ORDINANZA_ GE | VARCHAR2 (6 CHAR) | Tipologia dell’ufficio che ha emesso l’ordinanza del GE |
| COD_LUOGO_UFFICIO_ORDINANZA_GE | VARCHAR2 (6 CHAR) | Sede dell’ufficio che ha emesso l’ordinanza del GE |
| DATA_ORDINANZA_PA | DATE | Data dell’ordinanza della pena accessoria |
| ANNO_ORDINANZA_PA | NUMBER | Anno dell’ordinanza della pena accessoria |
| NUMERO_ORDINANZA_PA | NUMBER | Numero dell’ordinanza della pena accessoria |
| COD_TIPO_UFFICIO_ORDINANZA_ PA | VARCHAR2 (6 CHAR) | Tipo di ufficio dell’ordinanza della pena accessoria |
| COD_LUOGO_UFFICIO_ORDINANZA_PA | VARCHAR2 (6 CHAR) | Sede dell’ufficio dell’ordinanza della pena accessoria |
| DESCR_ALTRE_PA | VARCHAR2 (100 CHAR) | Descrizione di altre pene accessorie |
| COD_FONTE_GE | VARCHAR2 (5 CHAR) | Codice fonte giudice dell’esecuzione |
| ANNO_FONTE_GE | VARCHAR2 (4 CHAR) | Anno fonte giudice dell’esecuzione |
| NUMERO_FONTE_GE | VARCHAR2 (6 CHAR) | Numero fonte giudice dell’esecuzione |
| COD_SOTTONUMERAZIONE_GE | VARCHAR2 (2 CHAR) | Sottonumerazione fonte giudice dell’esecuzione |
| COMMA_GE | VARCHAR2 (10 CHAR) | Comma del giudice dell’esecuzione |
| LETTERA_GE | VARCHAR2 (2 CHAR) | Lettera giudice dell’esecuzione |
| NUMERO_GE | VARCHAR2 (2 CHAR) | Numero giudice dell’esecuzione |
| ARTICOLO_GE | VARCHAR2 (50 CHAR) | Articolo giudice dell’esecuzione |
| BEN_ID_BENEFICIO. | NUMBER | Identificativo del beneficio |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| PEN_ACC_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| PENA_ACCESSORIA_SENTENZA_SIGE | PNA_SEN_SIGE_FK | PNA_ID_PENA_ACCESSORIA |



# PENA_ACCESSORIA_CUMULO
tabella contenente i dati relativi alle pene accessorie nel cumulo. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PENA_ACCESSORIA_CUMULO | NUMBER(38) | Identificativo della tabella |
| COD_TIPO_PENA_ACCESSORIA | VARCHAR2(3) | CG_REF_CODES.RV_DOMAIN= ’TIPO_ PENA_ACCESSORIA’ |
| COD_TIPO_DURATA | VARCHAR2(1) | CG_REF_CODES.RV_DOMAIN= ’TIPO_DURATA’ |
| NUM_ANNI | NUMBER(4) | Durata: numero anni |
| NUM_MESI | NUMBER(4) | Durata: numero mesi |
| NUM_GIORNI | NUMBER(4) | Durata: numero giorni |
| NOTE | VARCHAR2(2000) | Campo per eventuali note |
| TIT_ID_TITOLO_CUMULATO | NUMBER(38) | FK alla tabella TITOLO_CUMULATO |
| FLAG_STATO | VARCHAR2(1) | E=estratto M=modificato C=Cancellato I=Iscritto |
| MOTIVO_MODIFICA | VARCHAR2(2000) | Note inserite dall''operatore in fase di Modifica Cancellazione Iscrizione |
| ID_PENA_ACCESSORIA_ORIGINE | NUMBER(38) | Eventuale ID del record PENA_ACCESSORIA da cui è stato derivato questo record |
| DESCR_ALTRE_PA | VARCHAR2(100) | Descrizione per Altre Pene Accessorie |
| BEN_ID_BENEFICIO_ORIG | NUMBER(38) | Id dell’eventuale record BENEFICIO (indulto/amnistia) che ha Annullato la PA (n.b. stesso titolo) |
| BEN_ID_BENEFICIO_CUMULO | NUMBER(38) | Id dell’eventuale record BENEFICIO_CUMULO (indulto/amnistia) che ha Annullato la PA (n.b. stesso titolo) |
| FLAG_DATI_FINALI | VARCHAR2(1) | S/N indica se la misura è stata selezionata per i dati Finali Cumulo |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |


# PENA_ACCESSORIA_SENTENZA_SIGE
tabella associativa tra pena accessoria e sentenza sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| PNA_ID_PENA_ACCESSORIA | NUMBER NOT NULL | ID del record PENA_ACCESSORIA. |
| FAS_SIGE_SEN_ID | NUMBER NOT NULL. | ID del record FAS_SIGE_SENTENZA. |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| PNA_FAS_SIGE_SEN_FK | FAS_SIGE_SEN_ID | (FAS_SIGE_SENTENZA.ID_FAS_SIGE_SENTENZA) |
| PNA_SEN_SIGE_FK | PNA_ID_PENA_ACCESSORIA | (PENA_ACCESSORIA.ID_PENA_ACCESSORIA) |



# PENA_COMPLESSIVA
tabella contenente i dati relativi alla pena complessiva. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PENA_COMPLESSIVA | NUMBER NOT NULL | Chiave naturale dell'entità. E' un progressivo gestito da sequence. |
| COD_TIPO_PENA_DETENTIVA | VARCHAR2 (2 CHAR) | In particolare indica il tipo di ergastolo se presente. Infatti assume i seguenti valori: ERGASTOLO CON ISOLAMENTO
DIURNO. Nel caso non sia valorizzata significa che siamo in presenze o di Reclusione o di Arresto. |
| NUM_ANNI_RECLUSIONE | NUMBER | Quantità degli anni assegnati in caso di reclusione. |
| NUM_MESI_RECLUSIONE | NUMBER | Quantità dei mesi assegnati in caso di reclusione. |
| NUM_GIORNI_RECLUSIONE | NUMBER | Quantità dei giorni assegnati in caso di reclusione. |
| IMPORTO_MULTA | NUMBER (2-16) | Quantità di importo pecuniario in caso di reclusione. |
| NUM_ANNI_ARRESTO | NUMBER | Quantità degli anni assegnati in caso di arresto. |
| NUM_MESI_ARRESTO | NUMBER | Quantità dei mesi assegnati in caso di arresto. |
| NUM_GIORNI_ARRESTO | NUMBER | Quantità dei giorni assegnati in caso di arresto. |
| IMPORTO_AMMENDA | NUMBER (2-16) | Quantità di importo pecuniario in caso di arresto. |
| DATA_INIZIO | DATE | Data da cui considerare valido l'inizio della pena complessiva. |
| DATA_FINE | DATE | Data di termine della pena complessiva. Resta da definire che data inserire se siamo in presenza di ergastolo. |
| COD_TIPO_RITO | VARCHAR2 (1 CHAR) | Valore derivante da dominio. Assume i seguenti valori: Abbreviato Patteggiamento. |
| DATA_INIZIO_ISOLAMENTO_DIURNO | DATE |  |
| DATA_FINE_ISOLAMENTO_DIURNO | DATE |  |
| NUM_ANNI_ISOLAMENTO_DIURNO | NUMBER |  |
| NUM_MESI_ISOLAMENTO_DIURNO | NUMBER |  |
| NUM_GIORNI_ISOLAMENTO_DIURNO | NUMBER |  |
| FLAG_PENA_IN_CONTINUAZIONE | VARCHAR2 (1 CHAR) | Questo flag indica se la pena trattata è una continuazione di pene inflitte precedentemente. |
| NUM_ANNI_CONDONATI | NUMBER |  |
| NUM_MESI_CONDONATI | NUMBER |  |
| NUM_GIORNI_CONDONATI | NUMBER |  |
| IMPORTO_CONDONATO | NUMBER (2-16) |  |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| DATA_PRESCRIZIONE | DATE | Data della prescrizione |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| PEN_COM_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| ANNMAN_PENACOMPL | ANMA_PENACOMPL_FK | PENACOMPLESSIVA_ID |
| CONTINUAZIONE | CON_PEN_COM_FK | PEN_COM_ID_PENA_COMPLESSIVA |
| PENA_COMPLESSIVA_SENTENZA_SIGE | PNC_SEN_SIGE_FK | PNC_ID_PENA_COMPLESSIVA |
| SANZIONE_SOSTITUTIVA | SAN_SOS_PEN_COM_FK | PEN_COM_ID_PENA_COMPLESSIVA |


# PENA_COMPLESSIVA_CUMULO
tabella contenente i dati relativi alla pena complessiva in un cumulo. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PENA_COMPLESSIVA_CUM | NUMBER(38) NOT NULL | Identificativo della tabella |
| COD_TIPO_PENA_DETENTIVA | VARCHAR2(2 CHAR) | -01=Reclusione 02=Arresto03=Ergastolo04=Ergastolo Isolamento Diurno |
| NUM_ANNI_RECLUSIONE | NUMBER(4) | Numero Anni reclusione |
| NUM_MESI_RECLUSIONE | NUMBER(4) | Numero Mesi reclusione |
| NUM_GIORNI_RECLUSIONE | NUMBER(4) | Numero Giorni reclusione |
| IMPORTO_MULTA | NUMBER(162) | Importo della Multa |
| NUM_ANNI_ARRESTO | NUMBER(4) | Numero Anni arresto |
| NUM_MESI_ARRESTO | NUMBER(4) | Numero Mesi arresto |
| NUM_GIORNI_ARRESTO | NUMBER(4) | Numero Giorni arresto |
| IMPORTO_AMMENDA | NUMBER(162) | Importo Ammenda |
| NUM_ANNI_ISOLAMENTO_DIURNO | NUMBER(3) | Numero Anni Isolamento Diurno |
| NUM_MESI_ISOLAMENTO_DIURNO | NUMBER(4) | Numero Mesi Isolamento Diurno |
| NUM_GIORNI_ISOLAMENTO_DIURNO | NUMBER(4) | Numero Giorni Isolamento Diurno |
| DATA_PRESCRIZIONE | DATE | Data Prescrizione |
| FLAG_PENA_IN_CONTINUAZIONE | VARCHAR2(1 CHAR) | Tipo Continuazione (-ADNR) |
| FLAG_STATO | VARCHAR2(1 CHAR) NOT NULL | E=estratto M=modificato C=Cancellato I=Iscritto |
| MOTIVO_MODIFICA | VARCHAR2(2000 CHAR) | Note inserite dall''operatore in fase di Modifica Cancellazione Iscrizione |
| TIT_ID_TITOLO_CUMULATO | NUMBER(38) NOT NULL | FK alla tabella TITOLO_CUMULATO |
| ID_PENA_COMPLESSIVA_ORIGINE | NUMBER(38) | Eventuale ID del record PENA_COMPLESSIVA da cui è stato derivato questo record |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100 CHAR) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11 CHAR) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100 CHAR) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(11 CHAR) | Codice Ufficio Utente ultimo aggiornamento |



# PENA_COMPLESSIVA_SENTENZA_SIGE
tabella associativa tra Pena_complessiva e Sentenza_sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| PNC_ID_PENA_COMPLESSIVA | NUMBER NOT NULL | ID del record PENA_COMPLESSIVA. |
| FAS_SIGE_SEN_ID | NUMBER NOT NULL. | ID del record FAS_SIGE_SENTENZA. |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| PNC_FAS_SIGE_SEN_FK | FAS_SIGE_SEN_ID | (FAS_SIGE_SENTENZA.ID_FAS_SIGE_SENTENZA) |
| PNC_SEN_SIGE_FK | PNC_ID_PENA_COMPLESSIVA | (PENA_COMPLESSIVA.ID_PENA_COMPLESSIVA) |





# PENA_CUMULO
tabella contenente i dati relativi alla pena di un cumulo. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PENA_CUMULO | NUMBER NOT NULL | Chiave naturale dell'entità. E' un progressivo gestito da sequence. |
| COD_TIPO_PENA_DETENTIVA | VARCHAR2 (2 CHAR) | Eventuale Ergastolo o Ergastolo con Isolamento Diurno. |
| NUM_ANNI_RECLUSIONE | NUMBER | Anni di pena residua. |
| NUM_MESI_RECLUSIONE | NUMBER | Mesi di pena residua. |
| NUM_GIORNI_RECLUSIONE | NUMBER | Giorni di pena residua. |
| IMPORTO_MULTA | NUMBER (2-16) | Eventuale importo multa di pena residua. |
| NUM_ANNI_ARRESTO | NUMBER | Pena residua. |
| NUM_MESI_ARRESTO | NUMBER | Pena residua. |
| NUM_GIORNI_ARRESTO | NUMBER | Pena residua. |
| IMPORTO_AMMENDA | NUMBER (2-16) | Eventuale importo ammenda di pena residua. |
| DATA_DECORRENZA_PENA | DATE | Pari alla Data Inizio di pena residua. |
| MOTIVAZIONI | VARCHAR2 (2000 CHAR) | Motivazioni del periodo di sospensione. |
| NUM_ANNI_RECLUSIONE_SOSP | NUMBER | Anni di reclusione sospesi. |
| NUM_MESI_RECLUSIONE_SOSP | NUMBER | Mesi di reclusione sospesi. |
| NUM_GIORNI_RECLUSIONE_SOSP | NUMBER | Giorni di reclusione sospesi. |
| NUM_ANNI_ARRESTO_SOSP | NUMBER | Anni di arresto sospesi. |
| NUM_MESI_ARRESTO_SOSP | NUMBER | Mesi di arresto sospesi. |
| NUM_GIORNI_ARRESTO_SOSP | NUMBER | Giorni di arresto sospesi. |
| ESTREMI_ORDINANZA | VARCHAR2 (2000 CHAR) | Estremi dell'ordinanza che ha stabilito il periodo di sospensione. |
| FLAG_ERGASTOLO | VARCHAR2 (1 CHAR) | Si / No |
| NOTE | VARCHAR2 (2000 CHAR) | Eventuali note a corredo. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| CUM_ID_CUMULO | NUMBER |  |
| NUM_ANNI_ISOLAMENTO_DIURNO | NUMBER | Relativi all'ergastolo. |
| NUM_MESI_ISOLAMENTO_DIURNO | NUMBER | Relativi all'ergastolo. |
| NUM_GIORNI_ISOLAMENTO_DIURNO | NUMBER | Relativi all'ergastolo. |
| MISURA_SICUREZZA | VARCHAR2 (2000 CHAR) | Misura di sicurezza |
| PENA_ACCESSORIA | VARCHAR2 (2000 CHAR) | Pene accessorie |
| NUM_GIORNI_LIB_ANTICIPATA | NUMBER | Numero di giorni della liberazione anticipata |
| NUM_GIORNI_LIB_ANTICIPATA_LA | NUMBER | Numero di giorni della liberazione anticipata |
| NUM_GIORNI_LIB_ANTICIPATA_SPE | NUMBER | Numero di giorni della liberazione anticipata speciale |
| NUM_GIORNI_LIB_ANTICIPATA_INT | NUMBER | Numero di giorni della liberazione anticipata speciale integrativa |
| NUM_GIORNI_RIDUZIONE_PENA | NUMBER | Numero di giorni di riduzione pena |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| PEN_CUM_CUM_FK | CUM_ID_CUMULO | (CUMULO.ID_CUMULO) |





# PENA_PECUNIARIA
tabella contenente i dati relativi alla pena pecuniaria. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PENA_PECUNIARIA | NUMBER NOT NULL | Identificativo della pena pecuniaria |
| SANZIONE_PECUNIARIA | NUMBER (2-16) NOT NULL | Importo della sanzione pecuniaria |
| ANNO_REG_36 | NUMBER | Anno Reg. Mod. 36 |
| NUM_REG_36 | NUMBER | Numero Reg. Mod. 36 |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER |  |
| EVE_ID_EVENTO. | NUMBER |  |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| PEN_PEC_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| PEN_PEC_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |
|  |  |  |




# PENA_PRESUNTA
tabella contenente i dati relativi alla pena presunta. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PENA_PRESUNTA | NUMBER NOT NULL | Identificativo della pena presunta |
| DATA_INIZIO | DATE | Data inizio della pena |
| DATA_FINE | DATE | Data fine della pena |
| NUM_ANNI_RECLUSIONE | NUMBER | Numero di anni della reclusione |
| NUM_MESI_RECLUSIONE | NUMBER | Numero di mesi della reclusione |
| NUM_GIORNI_RECLUSIONE | NUMBER | Numero di giorni della reclusione |
| IMPORTO_MULTA | NUMBER (2-16) | Importo della multa |
| NUM_ANNI_ARRESTO | NUMBER | Numero di anni dell’arresto |
| NUM_MESI_ARRESTO | NUMBER | Numero di mesi dell’arresto |
| NUM_GIORNI_ARRESTO | NUMBER | Numero di giorni dell’arresto |
| IMPORTO_AMMENDA | NUMBER (2-16) | Importo dell’ammenda |
| DIES_A_QUO | VARCHAR2 (1 CHAR) | Se valorizzato con S indica che nel calcolo deve essere preso in considerazione anche il primo giorno (quello di notifica) |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| DATA_INIZIO_ARRESTO | DATE | Data di inizio arresto |
| DATA_FINE_RECLUSIONE | DATE | Data di fine reclusione |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| PEN_PRE_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


# PENA_RESIDUA
tabella contenente i dati relativi alla pena residua. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PENA_RESIDUA | NUMBER NOT NULL | Chiave naturale dell'entità. Legato alla sequence PEN_RES_SEQ. |
| DATA_INIZIO | DATE | Data di inizio di validità della pena. |
| DATA_FINE | DATE | Data di fine pena. |
| NUM_ANNI_RECLUSIONE | NUMBER | Quantità degli anni da scontare in caso di reclusione. |
| NUM_MESI_RECLUSIONE | NUMBER | Quantità dei mesi da scontare in caso di reclusione. |
| NUM_GIORNI_RECLUSIONE | NUMBER | Quantità dei giorni da scontare in caso di reclusione. |
| IMPORTO_MULTA | NUMBER (2-16) | Importo della multa comminata. |
| NUM_ANNI_ARRESTO | NUMBER | Quantità di anni da scontare in caso di arresto. |
| NUM_MESI_ARRESTO | NUMBER | Quantità di mesi da scontare in caso di arresto. |
| NUM_GIORNI_ARRESTO | NUMBER | Quantità di giorni da scontare in caso di arresto. |
| IMPORTO_AMMENDA | NUMBER (2-16) | Importo della sanzione pecuniaria in caso di arresto. |
| DIES_A_QUO | VARCHAR2 (1 CHAR) | Se valorizzato con S indica che nel calcolo deve essere preso in considerazione anche il primo giorno (quello di notifica). |
| FLAG_VALIDATO | VARCHAR2 (1 CHAR) | Indica se è stato fatto il calcolo in modalità provvisoria o definitiva e quindi è stato convalidato il calcolo. |
| DATA_FINE_PRESUNTA | DATE | Data calcolata in modalità provvisoria per la successiva convalida. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| DATA_FINE_RECLUSIONE | DATE | Data di fine reclusione |
| DATA_INIZIO_ARRESTO | DATE | Data di inizio dell’arresto |
| FLAG_ERGASTOLO | VARCHAR2 (1 CHAR) | Flag indicante la presenza dell'ergastolo o meno. |
| DATA_INIZIO_ISOLAMENTO_DIURNO | DATE | Data da cui inizia l'isolamento diurno di un ergastolano. |
| DATA_FINE_ISOLAMENTO_DIURNO | DATE | Data di termine dell'isolamento diurno di un ergastolano. |
| NUM_ANNI_ISOLAMENTO_DIURNO | NUMBER | Numero di anni di isolamento diurno |
| NUM_MESI_ISOLAMENTO_DIURNO | NUMBER | Numero di mesi di isolamento diurno |
| NUM_GIORNI_ISOLAMENTO_DIURNO | NUMBER | Numero di giorni di isolamento diurno |
| MIS_ALT_ID_MISURA_ALTERNATIVA | NUMBER | Identificativo della misura alternativa |
| FLAG_PENA_SOSPESA | VARCHAR2 (1 CHAR). | S/N Flag della pena sospesa |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| PEN_RES_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| PEN_RES_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| EVENTO | EVE_PEN_RES_FK | PEN_ID_PENA_RESIDUA |
| SOSPENSIONE | SOS_PEN_RES_FK | PEN_RES_ID_PENA_RESIDUA |



# PENA_RIDETERMINATA_CUMULO
tabella contenente i dati relativi alla pena rideterminata in un cumulo. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PENA_RIDETERMINATA_CUMULO | NUMBER(38) | Identificativo della tabella |
| COD_TIPO_PENA_DETENTIVA | VARCHAR2(2) | Utilizzato solo in caso di ergastolo (0304) |
| NUM_ANNI_RECLUSIONE | NUMBER(4) | Anni reclusione |
| NUM_MESI_RECLUSIONE | NUMBER(4) | Mesi reclusione |
| NUM_GIORNI_RECLUSIONE | NUMBER(4) | Giorni reclusione |
| IMPORTO_MULTA | NUMBER(162) | Importo multa |
| NUM_ANNI_ARRESTO | NUMBER(4) | Anni arresto |
| NUM_MESI_ARRESTO | NUMBER(4) | Mesi arresto |
| NUM_GIORNI_ARRESTO | NUMBER(4) | Giorni arresto |
| IMPORTO_AMMENDA | NUMBER(162) | Importo ammenda |
| NUM_ANNI_ISOLAMENTO_DIURNO | NUMBER(3) | Anni isolamento diurno |
| NUM_MESI_ISOLAMENTO_DIURNO | NUMBER(4) | Mesi isolamento diurno |
| NUM_GIORNI_ISOLAMENTO_DIURNO | NUMBER(4) | Giorni isolamento diurno |
| NUMERO_GIORNI_LA | NUMBER(4) | Numero giorni liberazione anticipata |
| NUMERO_GIORNI_LS | NUMBER(4) | Numero giorni liberazione Anticipata speciale |
| NUMERO_GIORNI_LI | NUMBER(4) | Numero giorni liberazione Anticipata integrazione |
| NUMERO_GIORNI_RIDUZIONE | NUMBER(4) | Giorni Rimedi Risarcitori DL92 |
| FLAG_PENA_RESIDUA_CUMULO | VARCHAR2(1) | ‘S’ se trattasi di pena è stata ricalcolata
‘N’ se trattasi di pena non ricalcolata |
| IS_PENA_DA_RICALCOLARE | VARCHAR2(1) | S/N indica se la pena è da ricalcolare |
| DATA_INIZIO | DATE | Data decorrenza pena |
| DATA_FINE_RECLUSIONE | DATE | Data fine reclusione |
| DATA_INIZIO_ARRESTO | DATE | Data inizio arresto |
| DATA_FINE_PRESUNTA | DATE | Data fine pena presunta |
| DATA_FINE | DATE | Data scadenza pena |
| DAT_ID_DATI_FINALI_CUMULO | NUMBER(38) | FK alla tabella DATI_FINALI_CUMULO |
| ISTR_ID_ISTRUTTORIA_CUMULO | NUMBER(38) | FK alla tabella ISTRUTTORIA_CUMULO |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |

# PERIODO_ALTRA_MISURA
tabella contenente i dati relativi ai periodi temporali definiti per altre misure. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PERIODO_ALTRA_MISURA | NUMBER NOT NULL | Identificativo altra misura |
| DATA_INIZIO_ESECUZIONE | DATE | Data di inizio dell’esecuzione |
| DATA_SCADENZA | DATE | Data di scadenza |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2 (4 CHAR) | Identificativo dell’istituto di detenzione |
| MOTIVAZIONE | VARCHAR2 (1000 CHAR) | Descrizione della motivazione |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER | Identificativo del fascicolo SIUS |
| FLAG_VALIDA | VARCHAR2 (1 CHAR) | S/N flag validità |
| COD_TIPO_AUTORITA | VARCHAR2 (2 CHAR) | Tipo di autorità |
| COD_LUOGO_AUTORITA | VARCHAR2 (6 CHAR) | Sede dell’autorità |
| SOSPENSIONE_GG | NUMBER | Numero giorni di sospensione |
| SOSPENSIONE_MM | NUMBER | Numero mesi di sospensione |
| SOSPENSIONE_AA | NUMBER | Numero anni di sospensione |
| DA_RECUPERARE | VARCHAR2 (1 CHAR) | S/N misura da recuperare |
| FLAG_MOTIVO | VARCHAR2 (2 CHAR) | Flag della motivazione |
| COD_TIPO_UFFICIO_SOSP | VARCHAR2 (3 CHAR) | Tipo ufficio della sospensione |
| ESPIATA_GG | NUMBER | Numero di giorni di pena espiata |
| ESPIATA_MM | NUMBER | Numero di mesi di pena espiata |
| ESPIATA_AA | NUMBER | Numero di anni di pena espiata |
| RESIDUA_GG | NUMBER | Numero di giorni di pena residua |
| RESIDUA_MM | NUMBER | Numero di mesi di pena residua |
| RESIDUA_AA | NUMBER | Numero di anni di pena residua |
| DA_RECUPERARE_GG | NUMBER | Numero di giorni di pena da recuperare |
| DA_RECUPERARE_MM | NUMBER | Numero di mesi di pena da recuperare |
| DA_RECUPERARE_AA | NUMBER | Numero di anni di pena da recuperare |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| PER_MISU_FASCICOLO_SIEP_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |
| PER_MISU_FASCICOLO_SIUS_FK | FAS_SIU_ID_FASCICOLO_SIUS | (FASCICOLO_SIUS.ID_FASCICOLO_SIUS) |
| PER_MISU_ID_EVENTO_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| PER_MISU_ISTITUTO_DET_FK | IST_DET_ID_ISTITUTO_DETENZIONE | (ISTITUTO_DETENZIONE.ID_ISTITUTO_DETENZIONE) |




# PERIODO_ALTRA_SANZIONE
tabella contenente i dati relativi ai periodi temporali definiti per altre sanzioni. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PERIODO_ALTRA_SANZIONE | NUMBER NOT NULL | Identificativo della tabella |
| DATA_INIZIO_ESECUZIONE | DATE | Data di inizio dell’esecuzione della pena |
| DATA_SCADENZA | DATE | Data della scadenza |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2 (4 CHAR) | Identificativo dell’istituto di detenzione |
| MOTIVAZIONE | VARCHAR2 (1000 CHAR) | Descrizione della motivazione |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER | Identificativo del fascicolo SIUS |
| FLAG_VALIDA | VARCHAR2 (1 CHAR) | S/N validità della sanzione |
| COD_TIPO_AUTORITA | VARCHAR2 (2 CHAR) | Tipo dell’autorità |
| COD_LUOGO_AUTORITA | VARCHAR2 (6 CHAR) | Sede dell’autorità |
| SOSPENSIONE_GG | NUMBER | Numero giorni di sospensione |
| SOSPENSIONE_MM | NUMBER | Numero mesi di sospensione |
| SOSPENSIONE_AA | NUMBER | Numero anni di sospensione |
| DA_RECUPERARE | VARCHAR2 (1 CHAR) | Sanzione sa recuperare |
| FLAG_MOTIVO | VARCHAR2 (2 CHAR) | Flag della motivazione |
| COD_TIPO_UFFICIO_SOSP | VARCHAR2 (3 CHAR) | Tipo ufficio della sospensione |
| ESPIATA_GG | NUMBER | Numero di giorni di pena espiata |
| ESPIATA_MM | NUMBER | Numero di mesi di pena espiata |
| ESPIATA_AA | NUMBER | Numero di anni di pena espiata |
| RESIDUA_GG | NUMBER | Numero di giorni di pena residua |
| RESIDUA_MM | NUMBER | Numero di mesi di pena residua |
| RESIDUA_AA | NUMBER | Numero di anni di pena residua |
| DA_RECUPERARE_GG | NUMBER | Numero di giorni di pena da recuperare |
| DA_RECUPERARE_MM | NUMBER | Numero di mesi di pena da recuperare |
| DA_RECUPERARE_AA | NUMBER | Numero di anni di pena da recuperare |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN | REFERENCES_COLUMN |  |
| --- | --- | --- | --- | --- |
| PER_SANZ_FASCICOLO_SIEP_FK | FAS_SIE_ID_FASCICOLO_SIEP | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |
| PER_SANZ_FASCICOLO_SIUS_FK | FAS_SIU_ID_FASCICOLO_SIUS | FAS_SIU_ID_FASCICOLO_SIUS | (FASCICOLO_SIUS.ID_FASCICOLO_SIUS) | (FASCICOLO_SIUS.ID_FASCICOLO_SIUS) |
| PER_SANZ_ID_EVENTO_FK | EVE_ID_EVENTO | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) | (EVENTO.ID_EVENTO) |
| PER_SANZ_ISTITUTO_DET_FK | IST_DET_ID_ISTITUTO_DETENZIONE | IST_DET_ID_ISTITUTO_DETENZIONE | (ISTITUTO_DETENZIONE.ID_ISTITUTO_DETENZIONE) | (ISTITUTO_DETENZIONE.ID_ISTITUTO_DETENZIONE) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| POSIZIONE_MATERIALE_FASC | POS_MAT_FAS_POS_MAT | COD_POSIZIONE_MATERIALE |
| POSIZIONE_MATERIALE_FASC | POS_MAT_FAS_POS_MAT | COD_UFFICIO |
| POSIZIONE_MATERIALE_FASC_SIUS | POS_MAT_FAS_SIUS_POS_MAT | COD_POSIZIONE_MATERIALE |
| POSIZIONE_MATERIALE_FASC_SIUS | POS_MAT_FAS_SIUS_POS_MAT | COD_UFFICIO |


# PERIODO_LIB_ANT_CUMULO
tabella contenente i dati relativi ai periodi di liberazione anticipata del procedimento cumulato. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PERIODO_LIBANTICIPATA | NUMBER(38) | Sequence |
| DATA_INIZIO | DATE | Data inizio periodo L.A. |
| DATA_FINE | DATE | Data fine periodo L.A. |
| LIB_ID_LIB_ANTICIPATA_CUMULO | NUMBER(38) | FK alla tabella LIB_ANTICIPATA_CUMULO |
| FLAG_STATO | VARCHAR2(1) | E=estratto, M=modificato, C=Cancellato, I=Iscritto |
| MOTIVO_MODIFICA | VARCHAR2(2000) | Note inserite dall''operatore in fase di Modifica, Cancellazione, Iscrizione |
| ID_PERIODO_LIBANT_ORIGINE | NUMBER(38) | Eventuale ID del record LICENZA_LIBANTICIPATA origine |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |

# PERIODO_LIBANTICIPATA
tabella contenente i dati relativi ai periodi di liberazione anticipata. utilizzata dal sottosistema siep-sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PERIODO_LIBANTICIPATA | NUMBER NOT NULL | Chiave naturale numerica gestita da Sequence PER_LIB_SEQ. |
| DATA_INIZIO | DATE | Data di inizio della liberazione anticipata |
| DATA_FINE | DATE | Data di fine della liberazione anticipata |
| FLAG_CONCESSO | VARCHAR2 (2 CHAR) | S/N concessione della liberazione anticipata |
| DATA_INSERIMENTO | DATE | Data inserimento record |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| LIC_ID_LICENZA_LIBANTICIPATA | NUMBER | Identificativo della licenza |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| PER_LIBAN_ID_LIC_LIBAN_FK | LIC_ID_LICENZA_LIBANTICIPATA | (LICENZA_LIBANTICIPATA.ID_LICENZA_LIBANTICIPATA) |


# POSIZIONE_GIURIDICA
tabella contenente i dati relativi alla posizione giuridica. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_POSIZIONE_GIURIDICA | NUMBER NOT NULL | Chiave naturale numerica gestita da Sequence POS_GIU_SEQ. |
| COD_POSIZIONE_GIURIDICA | VARCHAR2 (2 CHAR) | Codice della posizione giuridica. Valore legato a Dominio. I valori possibili sono: IN ESPIAZIONE PENA IN REGIME CARCERARIO; ARRESTI DOMICILIARI EX ART. 656/10; LATITANTE; INTERNATO; LIBERO; IN ESPIAZIONE PENA IN REGIME DI LIBERAZIONE CONDIZIONALE; IN ESPIAZIONE PENA IN REGIME DI DETENZIONE DOMICILIARE; IN ESPIAZIONE PENA IN REGIME DI AFFIDAMENTO IN PROVA; IN ESPIAZIONE PENA IN REGIME DI SEMILIBERTA'; IN
ESPIAZIONE PENA SOSTITUTIVA (libertà controllata); LIBERO IN DIFFERIMENTO PENA; LIBERO IN DIFFERIMENTO PENA (PROVVISORIA); IN ESPIAZIONE PENA SOSTITUTIVA
(LAVORO SOSTITUTIVO); IN ESPIAZIONE PENA SOSTITUVA (SEMIDETENZIONE); EVASO; IN MISURA DI SICUREZZA; LIBERTA' VIGILATA.
N.B. i primi 4 valgono solo per la posizione giuridica al momento del
passaggio in giudicato della sentenza. |
| DATA_INIZIO | DATE | Data di decorrenza della posizione giuridica nell'ambito del fascicolo. |
| DATA_FINE | DATE | Data di termine della posizione giuridica nell'ambito del fascicolo. Vale null fintanto che non è inserito un nuovo record relativo alla posizione giuridica |
| COD_POSIZIONE_PROCESSUALE | VARCHAR2 (1 CHAR) | Codice della Posizione processuale. Deriva da dominio e vale C: contumace A: assente P: presente. |
| NOTE | VARCHAR2 (2000 CHAR) | Note |
| LUOGO_PROVA_AFFIDAMENTO | VARCHAR2 (2000 CHAR) | Descrizione del luogo della prova dell’affidamento |
| LUOGO_LAVORO_SEMILIBERTA | VARCHAR2 (2000 CHAR) | Descrizione del luogo del lavoro della semilibertà |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL | Identificativo del fascicolo SIEP |
| ID_EVENTO_RIFERIMENTO | NUMBER | Identificativo dell’evento |
| ALT_CAU_ID_ALTRA_CAUSA | NUMBER | Identificativo dell’altra causa |
| COD_MASCHERA | VARCHAR2(2) | Indica il codice della maschera |
| LUOGO_ESPIAZIONE | VARCHAR2(1000) | Indica il luogo della espiazione della pena |
| AUTORITA_COMPETENTE | VARCHAR2(2) | Indica il codice autorità competente |
| AUTORITA_COMPETENTE_SEDE | VARCHAR2(6) | Indica il codice Istat del comune della autorità competente |
| AUTORITA_COMPETENTE_INDIRIZZO | VARCHAR2(1000) | Indica indirizzo della autorità competente |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| POS_GIU_ALT_CAU_FK | ALT_CAU_ID_ALTRA_CAUSA | (ALTRA_CAUSA.ID_ALTRA_CAUSA) |
| POS_GIU_EVE_FK | ID_EVENTO_RIFERIMENTO | (EVENTO.ID_EVENTO) |
| POS_GIU_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


# POSIZIONE_GIURIDICA_CUMULO
tabella contenente i dati relativi alla posizione giuridica di un cumulo. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_POSIZIONE_GIURIDICA_CUM | NUMBER(38) | Identificativo della tabella |
| COD_POSIZIONE_GIURIDICA | VARCHAR2(3) | CG_REF_CODES.RV_DOMAIN= ‘POSIZIONE_GIURIDICA’ |
| DATA_INIZIO | DATE | Data inizio validità |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2(4) | ID dell’ISTITUTO_DETENZIONE |
| ALTRO_LUOGO | VARCHAR2(2000) | Descrizione altro luogo |
| CHIAVE_ANNO_FAS_SIUS | NUMBER(4) | Anno Procedimento SIUS di concessione MA |
| CHIAVE_PROGR_FAS_SIUS | NUMBER(38) | Progressivo Procedimento SIUS di concessione MA |
| CHIAVE_UFF_FAS_SIUS | VARCHAR2(11) | Ufficio Procedimento SIUS di concessione MA |
| ANNO_REGISTRO | NUMBER(4) | Anno Provvedimento Sorveglianza |
| NUMERO_REGISTRO | NUMBER(9) | Progressivo Provvedimento Sorveglianza |
| COD_TIPO_PROVVEDIMENTO | VARCHAR2(2) | Codice Tipo Provvedimento Sorveglianza (0203) |
| DATA_EMISSIONE_PROVV | DATE | Data emissione provvedimento Sorveglianza |
| NUM_ANNI_MISURA | NUMBER(2) | Anni Misura Alternativa concessa |
| NUM_MESI_MISURA | NUMBER(2) | Mesi Misura Alternativa concessa |
| NUM_GIORNI_MISURA | NUMBER(4) | Giorni Misura Alternativa concessa |
| DATA_FINE_MISURA | DATE | Data Fine Misura |
| FLAG_DECISIONE_TRIBUNALE | VARCHAR2(1) | ‘S’ se differimento fino a decisione TDS |
| DAT_ID_DATI_FINALI_CUMULO | NUMBER(38) | FK alla tabella DATI_FINALI_CUMULO |
| ISTR_ID_ISTRUTTORIA_CUMULO | NUMBER(38) | FK alla tabella ISTRUTTORIA_CUMULO |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |
| TIT_ID_TITOLO_CUMULATO | NUMBER(38) | FK alla tabella TITOLO_CUMULATO |
| FLAG_DIFF_DET_DOM | VARCHAR2(1) | ‘S’ per indicare Differimento Pena nella forma della Detenzione Domiciliare |
| DATA_INIZIO_MISURA | DATE | Data inizio misura alternativa |



# POSIZIONE_MATERIALE
tabella contenente i dati relativi alle posizioni materiali. utilizzata dal sottosistema siep-sius-sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_POSIZIONE_MATERIALE | VARCHAR2 (3 CHAR) NOT NULL | Codice della posizione materiale |
| COD_UFFICIO | VARCHAR2 (11 CHAR) NOT NULL | Codice dell’ufficio |
| DESC_POSIZIONE_MATERIALE | VARCHAR2 (100 CHAR) | Descrizione della posizione materiale |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| DATA_FINE_VALIDITA | DATE | Data di fine validità |



# POSIZIONE_MATERIALE_FASC
tabella associativa tra la Posizione_materiale e ilFascicolo_siep. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_POSIZIONE_MATERIALE | VARCHAR2 (3 CHAR) NOT NULL | Codice della posizione materiale |
| COD_UFFICIO | VARCHAR2 (11 CHAR) NOT NULL | Codice dell’ufficio |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL | Identificativo del fascicolo SIEP |
| COD_STATO_PROCEDIMENTO | VARCHAR2 (4 CHAR) | Codice dello stato del procedimento |
| DATA_INIZIO | DATE NOT NULL | Data di inizio |
| DATA_FINE | DATE | Data della fine |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| DESCR_STATO_PROCEDIMENTO | VARCHAR2 (2000 CHAR) DEFAULT NULL | Descrizione dello stato del procedimento |


# POSIZIONE_MATERIALE_FASC_SIGE
tabella contenente i dati relativi alla posizione materiale di un fascicolo sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_POSIZIONE_MATERIALE | VARCHA2(3) | Codice della posizione materiale |
| COD_UFFICIO | VARCHAR2(11) | Codice ufficio |
| FAS_SIGE_ID_FASCICOLO_SIGE | NUMBER(38) | Identificativo del fascicolo sige |
| COD_STATO_PROCEDIMENTO | VARCHAR2(4) | Codice della stato del procedimento |
| DATA_INIZIO | DATE | Data inizio |
| DATA_FINE | DATE | Data fine |
| DESCR_STATO_PROCEDIMENTO | VARCHAR2(1000) | Descrizione dello stato del procedimento |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Utenza dell’operatore che ha effettuato l’inserimento |
| DATA_INSERIMENTO | DATE | Data inserimento |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11) | Ufficio dell’operatore che ha effettuato l’inserimento |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100) | Utenza dell’operatore che ha effettuato l’aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data dell’aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(11) | Ufficio dell’operatore che ha effettuato l’aggiornamento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| FAS_SIGE_ID_POS_MAT_FAS | FAS_SIGE_ID_FASCICOLO_SIGE | (FASCICOLO_SIGE.ID_FASCICOLO_SIGE) |




# POSIZIONE_MATERIALE_FASC_SIUS
tabella contenente i dati relativi alla posizione materiale di un fascicolo sius. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_POSIZIONE_MATERIALE | VARCHAR2 (3 CHAR) NOT NULL | Codice della posizione materiale |
| COD_UFFICIO | VARCHAR2 (11 CHAR) NOT NULL | Codice dell’ufficio |
| FAS_SIUS_ID_FASCICOLO_SIUS | NUMBER NOT NULL | Identificativo del fascicolo SIUS |
| COD_STATO_PROCEDIMENTO | VARCHAR2 (4 CHAR) | Codice dello stato del procedimento |
| DATA_INIZIO | DATE NOT NULL | Data inizio |
| DATA_FINE | DATE | Data fine |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| DESCR_STATO_PROCEDIMENTO | VARCHAR2 (2000 CHAR) DEFAULT 'NULL'. | Descrizione dello stato del procedimento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| FAS_SIUS_ID_POS_MAT_FASC_SIUS | FAS_SIUS_ID_FASCICOLO_SIUS | (FASCICOLO_SIUS.ID_FASCICOLO_SIUS) |
| POS_MAT_FAS_SIUS_POS_MAT | COD_POSIZIONE_MATERIALE | (POSIZIONE_MATERIALE.COD_POSIZIONE_MATERIALE) |
| POS_MAT_FAS_SIUS_POS_MAT | COD_UFFICIO | (POSIZIONE_MATERIALE.COD_UFFICIO) |


# PRESA_IN_CARICO
tabella contenente i dati relativi alla presa in carico di un fascicolo siep. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PRESA_IN_CARICO | NUMBER NOT NULL | Identificativo della presa in carico |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL | Identificativo del fascicolo SIEP |
| DATA_PRESA_IN_CARICO | DATE NOT NULL | Data della presa in carico |
| COD_OPERATORE_PRESA_IN_CARICO | VARCHAR2 (100 CHAR) NOT NULL | Codice dell’operatore che ha effettuato la presa in carico |
| COD_UFFICIO_PRESA_IN_CARICO | VARCHAR2 (11 CHAR) NOT NULL | Codice dell’Ufficio dell’operatore che ha effettuato la presa in carico |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| PRE_IN_CAR_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


# PRESCRIZIONE
tabella contenente i dati relativi alla prescrizione. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PRESCRIZIONE | NUMBER NOT NULL | Chiave naturale numerica gestita da Sequence. |
| COD_TIPO_PRESCRIZIONE | VARCHAR2 (2 CHAR) NOT NULL | Codifica del Tipo di Prescrizione : Es.(Mantenere Costanti Rapporti con il CSSA Non Uscire Dall'Abitazione Non Frequentare Persone Pregiudicate  ... ). Associato al dominio TIPO_PRESCRIZIONE di CG_REF_CODES. |
| COD_LUOGO_AFFIDAMENTO | VARCHAR2 (6 CHAR) | Codice del comune Luogo di svolgimento della misura. |
| COD_UFF_MAGISTRATO_COMPETENTE | VARCHAR2 (11 CHAR) | Codice Ufficio del Magistrato competente. |
| COD_LUOGO_AUTORIZZATO | VARCHAR2 (6 CHAR) | Codice comune del luogo autorizzato. |
| ID_CSSA_COMPETENTE | NUMBER | Chiave numerica del CSSA competente. |
| DESCR_MANSIONE_LAVORATIVA | VARCHAR2 (2000 CHAR) | Campo libero che descrive la mansione sostenuta. |
| DESCR_LUOGO_LAVORO | VARCHAR2 (2000 CHAR) | Descrizione del luogo di lavoro. |
| COD_PROVINCIA_AUTORIZZATA | VARCHAR2 (2 CHAR) | Codice della provincia entro cui opera l'affidato. |
| ORA_USCITA_ABITAZIONE | VARCHAR2 (5 CHAR) | Orario di uscita dall'abitazione. |
| ORA_RIENTRO_ABITAZIONE | VARCHAR2 (5 CHAR) | Ora di rientro in abitazione. |
| AUTORITA_COMPETENTE_CONTROLLO | VARCHAR2 (100 CHAR) | Descrizione dell'autorità preposta al controllo della prescrizione. |
| NUM_VOLTE_CONTROLLO | NUMBER | Numero di controlli effettuati per la prescrizione. |
| DESCR_ALTRA_PRESCRIZIONE | VARCHAR2 (2000 CHAR) | Descrizione di eventuale prescrizione non codificata. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| DESCR_COMUNITA_TERAPEUTICA | VARCHAR2 (2000 CHAR) | Descrizione della comunità terapeutica |
| PROGR_PRESCRIZIONE | NUMBER | Progressivi prescrizione. |
| DESCR_PRESCRIZIONE_1 | VARCHAR2 (2000 CHAR) | Descrizione 1 Prescrizione |
| DESCR_PRESCRIZIONE_2 | VARCHAR2 (100 CHAR) | Descrizione 2 Prescrizione |
| DESCR_PRESCRIZIONE_3 | VARCHAR2 (100 CHAR) | Descrizione 3 Prescrizione |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| PRE_1_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |


# PROCEDIMENTO_CUMULATO
tabella contenente i dati relativi procedimento cumulato. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PROCEDIMENTO_CUMULATO | NUMBER(38) | Identificativo del procedimento cumulato |
| CHIAVE_ANNO_FAS_CUMULATO | NUMBER (4) | Anno Procedimento |
| CHIAVE_PROGR_FAS_CUMULATO | NUMBER(38) | Numero procedimento |
| COD_TIPO_UFFICIO_FAS_CUMULATO | VARCHAR2(6) | Codice tipo ufficio |
| COD_LUOGO_UFFICIO_FAS_CUMULATO | VARCHAR2(6) | Luogo ufficio |
| COD_UFFICIO_FAS_CUMULATO | VARCHAR2(11) | Codice ufficio |
| FLAG_ACCORPATO | VARCHAR2(1) | S/N – indica se ufficio accorpato |
| CHIAVE_UFFICIO_ORIGINE | VARCHAR2(11) | Codice Ufficio origine |
| CHIAVE_PROGR_ORIGINE | NUMBER(38) | Id del Procedimento Origine |
| DATA_RICHIESTA_FASCICOLO | DATE | Data richiesta |
| DATA_PERVENIMENTO_FASCICOLO | DATE | Data Pervenimento |
| NOTE | VARCHAR2(2000) | Campo per eventuali note |
| KEY_PROVV_NSC | NUMBER(38) | Chiave associativa con NSC |
| TIT_ID_TITOLO_CUMULATO | NUMBER(38) | FK alla tabella TITOLO_CUMULATO |
| FLAG_STATO | VARCHAR2(1) | E=estratto M=modificato C=Cancellato I=Iscritto |
| MOTIVO_MODIFICA | VARCHAR2(2000) | Note inserite dall''operatore in fase di Modifica Cancellazione Iscrizione |
| ID_FASCICOLO_SIEP_ORIGINE | NUMBER(38) | Eventuale ID del record FASCICOLO_SIEP da cui è stato derivato questo record |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |
| EVE_ID_EVENTO | NUMBER(38) | FK alla tabella EVENTO  
Se Iscritto in Istruttoria nel Proprio Ufficio, indica Id_Evento dell''iscrizione in Istruttoria. Se si cancella il Titolo dall''Istruttoria, va eliminato l''Evento corrispondente' |



# PROFILO
tabella contenente i dati relativi ai possibili profili definibili per un utente di sies. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_PROFILO | NUMBER NOT NULL | Identificativo univoco del profilo. |
| DESCRIZIONE | VARCHAR2 (60 CHAR) | Descrizione generica del profilo associato al codice. |
| DATA_FINE_VALIDITA | DATE | Data di fine validità di un profilo. Questa data viene compilata con la data di sistema quando viene richiesta la disabilitazione di un profilo. Un profilo è attivo quando la data di fine validità = NULL altrimenti è disabilitato  ma si mantiene questa informazione per la storicizzazione dei dati. |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| FUNZIONE_PROFILO | FUN_PRO_PRF_FK | PRF_COD_PROFILO |
| UTENTE_PROFILO | UTE_PRO_PRF_FK | PRF_COD_PROFILO |



# PROFILO_TIPOUFFICIO
tabella associativa tra il Profilo e il Tipo_ufficio. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| PRF_COD_PROFILO | NUMBER NOT NULL |  |
| UFF_COD_TIPO_UFFICIO | VARCHAR2 (10 CHAR) NOT NULL. |  |


# PROVVEDIMENTO_GE_SORV_CUM
tabella di working contenente i dati relativi al Provvedimento del GE/della Sorveglianza in merito alla richiesta del PM relativamente ad una Istruttoria Cumulo. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PROVVEDIMENTO_GE_SORV_CUM | NUMBER(38) | Sequence |
| COD_UFFICIO_EMITTENTE | VARCHAR2(11) | Codice dell’Ufficio che ha emesso il provvedimento |
| COD_LUOGO_EMITTENTE | VARCHAR2(6) | Cod_Comune del luogo sede dell’Ufficio emittente |
| DATA_D | DATE, | Data della decisione |
| ANNO_PROVV | NUMBER(4) | Anno provvedimento |
| NUMERO_PROVV | VARCHAR2(6) | Numero del provvedimento |
| FLAG_CONFORME | VARCHAR2(1) | C=conforme, D=difforme, R=rigetta, I=Inammissibile |
| FLAG_PIU_MENO_D | VARCHAR2(1) NO | + / - |
| NUM_ANNI_RECLUSIONE_D | NUMBER(3) | Numero anni reclusione decisi |
| NUM_MESI_RECLUSIONE_D | NUMBER(3) | Numero mesi reclusione decisi |
| NUM_GIORNI_RECLUSIONE_D | NUMBER(4) | Numero giorni reclusione decisi |
| IMPORTO_MULTA_D | NUMBER(11,2) | Importo multa decisa |
| NUM_ANNI_ARRESTO_D | NUMBER(3) | Numero anni arresto decisi |
| NUM_MESI_ARRESTO_D | NUMBER(3) | Numero mesi arresto decisi |
| NUM_GIORNI_ARRESTO_D | NUMBER(4) | Numero giorni arresto decisi |
| IMPORTO_AMMENDA_D | NUMBER(11,2) | Importo ammenda decisa |
| NUM_GIORNI_LA_REV_D | NUMBER(4) | Numero giorni L.A. revocati decisi |
| NUM_GIORNI_LS_REV_D | NUMBER(4) | Numero giorni L.A. speciale revocati decisi |
| NUM_GIORNI_LI_REV_D | NUMBER(4) | Numero giorni integrazione L.A. revocati decisi |
| MOTIVAZIONI_D | VARCHAR2(2000) | Eventuali motivazioni |
| COD_TIPO_PROVVEDIMENTO | VARCHAR2(2) | CG_REF_CODES.RV_DOMAIN= ’TIPO_PROVVEDIMENTO’ |
| ANNO_SIUS | NUMBER(4) | Anno procedimento SIUS |
| NUMERO_SIUS | VARCHAR2(6) | Numero procedimento SIUS |
| COD_TIPO_MS_D | VARCHAR2(2) | CG_REF_CODES.RV_DOMAIN= ’TIPO_MISURA_SICUREZZA’ |
| NUM_ANNI_MS_D | NUMBER(2) | Numero anni durata MS |
| NUM_MESI_MS_D | NUMBER(2) | Numero mesi durata MS |
| NUM_GIORNI_MS_D | NUMBER(4) | Numero giorni durata MS |
| RIC_ID_RICHIESTE_PM_IN_CUMULO | NUMBER(38) | FK alla tabella RICHIESTE_PM_IN_CUMULO |
| BEN_SOSP_COND | VARCHAR2(1) | ‘S’, se concessa Sospensione Condizionale della pena |
| BEN_NON_MENZIONE | VARCHAR2(1) | ‘S’, se concessa Non Menzione |
| BEN_INDULTO | VARCHAR2(1) | ‘I’, se concesso Indulto |
| COD_TIPO_PENA_ACCESSORIA_D | VARCHAR2(3) | CG_REF_CODES.RV_DOMAIN= ’TIPO_ PENA_ACCESSORIA’ |
| COD_TIPO_DURATA_D | VARCHAR2(1) | CG_REF_CODES.RV_DOMAIN= ’TIPO_ DURATA’ |
| NUM_ANNI_PA_D | NUMBER(4) | Numero anni pena accessoria |
| NUM_MESI_PA_D | NUMBER(4) | Numero mesi pena accessoria |
| NUM_GIORNI_PA_D | NUMBER(4) | Numero giorni pena accessoria |
| DATA_REVOCA | DATE | Data Revoca |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |


# PROVVEDIMENTO_SIGE
tabella contenente i dati relativi al provvedimento sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_PROVVEDIMENTO_SIGE | NUMBER NOT NULL | Chiave primaria |
| FAS_ID_FASCICOLO_SIGE | NUMBER NOT NULL | Riferimento al FASCICOLO_SIGE. |
| ID_EVENTO_GENERATO | NUMBER NOT NULL | Riferimento all'Evento associato al Provvedimento. |
| CHIAVE_ANNO | NUMBER | Chiave ANNO per Ufficio. |
| CHIAVE_PROGR | NUMBER | Chiave Progressivo per Ufficio. |
| DATA_EMISSIONE | DATE NOT NULL | Data di Emissione del Provvedimento. |
| DATA_DEPOSITO | DATE DEFAULT 'NULL' | Data di Deposito del Provvedimento. |
| COD_TIPO_PROVVEDIMENTO | VARCHAR2 (2 CHAR) | Codice identificativo del tipo di Provvedimento. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) NOT NULL | Codice dell’operatore che ha inserito il record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) NOT NULL | Ufficio dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE NOT NULL | Data di inserimento del record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| DEFINITORIO | VARCHAR2 (1 CHAR) | Flag a S indica che il provvedimento è Definitorio |
| CHIAVE_UFFICIO | VARCHAR2 (11 CHAR) | Chiave Ufficio del Provvedimento SIGE |
| FLAG_ORDINE_TRADUZIONE | VARCHAR2 (1 CHAR) | Flag a S indica "Con Ordine di Traduzione in Carcere"; N "Senza Ordine di Traduzione in Carcere" |
| LUOGO_SVOLGIMENTO | VARCHAR2 (200 CHAR) | Per la Fissazione Udienza contiene il Luogo Svolgimento registrato nel momento della fissazione. |
| COL_ID_COLLEGIO | NUMBER DEFAULT NULL | ID di eventuale Collegio giudicante da definire se non c'è udienza e se tipo giudizio è collegiale. |
| COD_TIPO_PROVVEDIMENTO_SIGE | VARCHAR2 (2 CHAR) | Specifica il tipo di provvedimento nell''ambito dei decreti ordinanze verbali |
| COD_UFFICIO_DESTINATARIO | VARCHAR2 (11 CHAR) | Codice dell’ufficio del destinatario |
| NOTE | VARCHAR2 (2000 CHAR) | Note |
| PROVV_ID_PROVVEDIMENTO_SIGE | NUMBER | Indica l’id dell’udienza relativa ordinanza conflitto di competenza |
| UDI_ID_UDIENZA_SIGE | NUMBER(38) | Identificativo dell’udienza SIGE |
| COD_UFFICIO_DEST_CASS | VARCHAR2(11) | Indica la Corte Suprema di Cassazione |



Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| PROV_COLLEGIO_FK | COL_ID_COLLEGIO | (COLLEGIO.ID_COLLEGIO) |
| PROV_EVE_FK | ID_EVENTO_GENERATO | (EVENTO.ID_EVENTO) |
| PROV_FAS_SIGE_FK | FAS_ID_FASCICOLO_SIGE | (FASCICOLO_SIGE.ID_FASCICOLO_SIGE) |
| PROV_ID_SIGE_FK | PROVV_ID_PROVVEDIMENTO_SIGE | (PROVVEDIMENTO_SIGE.ID_PROVVEDIMENTO_SIGE) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| IMPUGNAZIONE_SIGE | IMP_PROVV_SIGE_FK | PROVV_ID_PROVVEDIMENTO_SIGE |
| TENORE_SIGE | PROV_ID_PROVVEDIMENTO_SIGE_FK | PROV_ID_PROVVEDIMENTO_SIGE |
| PROVVEDIMENTO_SIGE | PROV_ID_SIGE_FK | PROVV_ID_PROVVEDIMENTO_SIGE |



# RATEIZZAZIONE_PP
La tabella contiene i dati relativi alla rateizzazione della pena pecuniaria, utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_RATEIZZAZIONE_PP | NUMBER(38) | Primary Key della tabella, legata alla sequence RAT_PEN_SEQ |
| IMPORTO_RATA | NUMBER(16,2) | Indica l’importo della rata |
| NUMERO_RATE | NUMBER(4) | Indica il numero delle rate |
| TIPO_RATEIZZAZIONE | VARCHAR2(11) | Indica il Tipo di Rateizzazione (R per Pagamento Rateizzato, U per Rata Unica) |
| SCADENZA_GIORNI | NUMBER(4) | Indica la Scadenza in giorni della rata |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Indica il Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Indica la Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11) | Indica il Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100) | Indica il Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Indica la Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(11) | Indica il Codice Ufficio Utente ultimo aggiornamento |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER(38) | Foreign Key verso la tabella FASCICOLO_SIEP.ID_FASCICOLO_SIEP |
| IMPORTO_DA_PAGARE | NUMBER(16,2) | Indica l’importo da pagare |
| EVE_ID_EVENTO | NUMBER(38) | Foreign Key verso la tabella EVENTO.ID_EVENTO |
| PROGRESSIVO_RATA | NUMBER | Indica il numero Progressivo della rata |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER(38) | Foreign Key verso la tabella FASCICOLO_SIUS.ID_FASCICOLO_SIUS |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| RATEIZZAZIONE_PP_EVENTO_FK | EVE_ID_EVENTO | EVENTO.ID_EVENTO |
| RAT_PEN_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | FASCICOLO_SIEP. ID_FASCICOLO_SIEP |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| BOLLETTINO_PAGOPA | BOLLETT_PAGOPA_RATEIZZA_FK | RAT_ID_RATEIZZAZIONE_PP |

# REATO
tabella contenente i dati relativi al reato. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_REATO | NUMBER NOT NULL | Chiave naturale numerica per l'accesso alla tabella Reato. Legato alla SEQUENCE REA_SEQ. |
| COD_TIPO_REATO | VARCHAR2 (2 CHAR) | Codice del tipo di reato. Legato a Dominio In REGE è il campo TARGTREA.COD_TIPO_REATO. |
| DATA_REATO | DATE | Data del commesso reato |
| PROGR_NUMERO_MANUALE | VARCHAR2 (10 CHAR) | Progressivo editabile dall'utente per inserire valori particolari quali ad esempio "1A 2  2A 2B". |
| PROGR_REATO | NUMBER | Progressivo nell'ambito del fascicolo. Si incrementa ad ogni nuovo reato inserito e serve da riferimento per tutte le circostanze iscritte per quel reato. |
| PROGR_CIRCOSTANZA | NUMBER | Progressivo della circostanza nell'ambito di un reato. |
| DATA_INIZIO | DATE | Data completa di inizio commesso reato In REGE è il campo TARGQGF.DATA_INIZIO. In alcuni casi la data non è specificata ma sono utilizzati i soli campi anno mese o giorno. |
| ANNO_INIZIO | NUMBER | Anno della data di inizio commesso reato. |
| MESE_INIZIO | NUMBER | Mese della data di inizio commesso reato. |
| GIORNO_INIZIO | NUMBER | Giorno della data di inizio commesso reato. |
| DATA_FINE | DATE | Data completa di fine commesso reato In REGE è il campo TARGQGF.DATA_FINE In alcuni casi la data non è specificata ma sono utilizzati i soli campi anno mese o giorno. |
| ANNO_FINE | NUMBER | Anno della data di fine commesso reato. |
| MESE_FINE | NUMBER | Mese della data di fine commesso reato. |
| GIORNO_FINE | NUMBER | Giorno della data di fine commesso reato. |
| COD_PERIODO_CONSUMAZIONE | VARCHAR2 (2 CHAR) | Indica un periodo generico al quale è possibile associare una delle   date sopra citate. Deriva da dominio e può assumere i seguenti valori: COMMESSO IN DATA [data1] ACCERTATO IN DATA [data1] ACCERTATO IN DATA [data1] E TUTTORA PERMANENTE ACCERTATO IN DATA [data1] E PERMANENTE SINO AL [data2] IN EPOCA ANTERIORE E PROSSIMA AL [data1] IN EPOCA SUCCESSIVA E PROSSIMA AL [data1] ACCERTATO IN DATA [data1] ED IN DATA [data2] COMMESSO IN DATA [data1] E TUTTORA PERMANENTE COMMESSO IN DATA [data1] E PERMANENTE SINO AL [data2] COMMESSO IN DATA [data1] E IN DATA [data2]. |
| DESC_LUOGO | VARCHAR2 (300 CHAR) | Descrizione del luogo dove è stato commesso reato. In REGE è il campo TARGQGF.DESC_LUOGO oppure deriva da TARGTLSC.DESC_LUOGO_SCONOSC IUTO nel caso in cui sia il luogo non sia conosciuto. |
| COD_FONTE | VARCHAR2 (5 CHAR) | FONTE GIURIDICA è il tipo di fonte giuridica relativo agli articoli di reato; es.: codice penale legge. In REGE è il campo TARGFGIU.DESC_FONTE_GIU. |
| ANNO_FONTE | NUMBER | Anno della norma In REGE è il campo TARGARTI.ANNO_NORMA. |
| NUMERO_FONTE | VARCHAR2 (6 CHAR) | Numero della norma In REGE è il campo TARGARTI.ANNO_NORMA. |
| COD_SOTTONUMERAZIONE | VARCHAR2 (2 CHAR) | Sottonumerazione articolo (bis ter ecc.) Deriva da dominio. In REGE è il campo TARGSNUM.DESC_SOTTONUM. |
| COMMA | VARCHAR2 (10 CHAR) | Comma dell'articolo trattato. |
| LETTERA | VARCHAR2 (2 CHAR) | Lettera dell'articolo trattato. |
| NUMERO | VARCHAR2 (2 CHAR) | Eventuale Numero dell'articolo trattato. |
| ARTICOLO | VARCHAR2 (50 CHAR) | Determina il tipo di fatto di cui si fa carico al condannato in base alla classificazione di legge (articolo comma ed altro eventuale). In REGE è il campo TARGARTI.COD_ARTICOLO. |
| NOTE | VARCHAR2 (2000 CHAR) | Note aggiuntive per completare le informazioni sul reato.
Questo campo è utilizzato anche per inserire i dati provenienti dalla migrazione RES poiché in tale applicazione il reato è un campo descrittivo non condizionato da regole sintattiche o semantiche. |
| COD_TIPO_PENA_DETENTIVA | VARCHAR2 (2 CHAR) | Codifica dell'eventuale tipologia della pena detentiva. Deriva da dominio e può assumere i seguenti valori: ARRESTO ERGASTOLO CON ISOLAMENTO DIURNO RECLUSIONE. |
| NUM_ANNI | NUMBER | Numero anni assegnati per il singolo reato. |
| NUM_MESI | NUMBER | Numero mesi assegnati per il singolo reato. |
| NUM_GIORNI | NUMBER | Numero giorni assegnati per il singolo reato. |
| SANZIONE_PECUNIARIA | NUMBER (2-16) | Importo eventualmente assegnato per il singolo reato. |
| FLAG_ERGASTOLO | VARCHAR2 (1 CHAR) | Flag di presenza ergastolo. Deriva da dominio e può assumere solo valori S/N. |
| DATA_INIZIO_ISOLAMENTO_DIURNO | DATE | Data dalla quale decorre in caso di ergastolo con isolamento diurno l'isolamento in questione. |
| DATA_FINE_ISOLAMENTO_DIURNO | DATE | Data temine in caso di ergastolo con isolamento diurno dell' isolamento in questione. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| COD_TIPO_SANZIONE | VARCHAR2 (2 CHAR) | Campo utilizzato per dettagliare la tipologia di sanzione trattata nel reato. Deriva da dominio e vale: AMMENDA MULTA |
| GIORNI_ISOLAMENTO_DIURNO | NUMBER | Numero di giorni dell’isolamento diurno |
| MESI_ISOLAMENTO_DIURNO | NUMBER | Numero di mesi dell’isolamento diurno |
| ANNI_ISOLAMENTO_DIURNO | NUMBER | Numero di anni dell’isolamento diurno |
| ID_CONTINUAZIONE_REATO | NUMBER | Identificativo della continuazione del reato |
| TIPO_CONTINUAZIONE_REATO | VARCHAR2 (2 CHAR) | Tipo di continuazione tra i reati |
| KEY_REATO_NSC | NUMBER | Identificativo del reato di NSC |
| COMMA_QUALIFICANTE | VARCHAR2 (2 CHAR) | Qualificante del comma |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| REA_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| ANNMAN_REATO | ANMA_REATO_FK | REATO_ID |
| ANNOTAZIONE_MANUALE | ANN_MAN_REA_FK | REA_ID_REATO |
| TENORE_SENTENZA_REATO | REATO_FK | REA_ID_REATO |
| REATO_SENTENZA_SIGE | REA_ID_REATO_FK | REA_ID_REATO |


# REATO_CUMULATO
tabella contenente i dati relativi al reato in un provvedimento di cumulo. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_REATO_CUM | NUMBER(38)   NOT NULL | Identificativo della tabella |
| COD_TIPO_REATO | VARCHAR2(2) | -, 01=Delitto, 02=Contravvenzione |
| DATA_REATO | DATE | Data commesso Reato |
| PROGR_NUMERO_MANUALE | VARCHAR2(10) | Progressivo Reato Manuale |
| PROGR_REATO | NUMBER(3) | Progressivo Reato di Sistema |
| PROGR_CIRCOSTANZA | NUMBER(3) | Progressivo Circostanza |
| DATA_INIZIO | DATE | Data inizio |
| ANNO_INIZIO | NUMBER(4) | Anno inizio |
| MESE_INIZIO | NUMBER(2) | Mese inizio |
| GIORNO_INIZIO | NUMBER(2) | Giorno inizio |
| DATA_FINE | DATE | Data Fine |
| ANNO_FINE | NUMBER(4) | Anno Fine |
| MESE_FINE | NUMBER(2) | Mese Fine |
| GIORNO_FINE | NUMBER(2) | Giorno Fine |
| COD_PERIODO_CONSUMAZIONE | VARCHAR2(2) | Codice Periodo consumazione (da ‘–‘ a ‘25’) |
| DESC_LUOGO | VARCHAR2(300) | Descrizione Luogo Consumazione |
| COD_FONTE | VARCHAR2(5) | CG_REF_CODES.RV_DOMAIN= ’FONTE’ |
| ANNO_FONTE | NUMBER(4) | Anno Fonte |
| NUMERO_FONTE | VARCHAR2(6) | Numero Fonte |
| COD_SOTTONUMERAZIONE | VARCHAR2(2) | Codice Sottonumerazione |
| COMMA | VARCHAR2(10) | Comma |
| COMMA_QUALIFICANTE | VARCHAR2(2) | Comma qualificante |
| LETTERA | VARCHAR2(2) | Lettera |
| NUMERO | VARCHAR2(2) | Numero |
| ARTICOLO | VARCHAR2(50) | Articolo |
| COD_TIPO_PENA_DETENTIVA | VARCHAR2(2 ) | CG_REF_CODES.RV_DOMAIN= ’TIPO_PENA_DETENTIVA’ |
| NUM_ANNI | NUMBER(3) | Anni pena reato |
| NUM_MESI | NUMBER(3) | Mesi pena reato |
| NUM_GIORNI | NUMBER(4) | Giorni pena reato |
| COD_TIPO_SANZIONE | VARCHAR2(2) | CG_REF_CODES.RV_DOMAIN= ’TIPO_SANZIONE’ |
| SANZIONE_PECUNIARIA | NUMBER(16,2) | Importo pena pecuniaria reato |
| FLAG_ERGASTOLO | VARCHAR2(1) | CG_REF_CODES.RV_DOMAIN= ’FLAG_ERGASTOLO’ |
| GIORNI_ISOLAMENTO_DIURNO | NUMBER(4) | Giorni Isolamento Diurno |
| MESI_ISOLAMENTO_DIURNO | NUMBER(3) | Mesi Isolamento Diurno |
| ANNI_ISOLAMENTO_DIURNO | NUMBER(3) | Anni Isolamento Diurno |
| NOTE | VARCHAR2(2000) | Campo per eventuali note |
| ID_CONTINUAZIONE_REATO_CUM | NUMBER(38) | Note inserite dall''operatore in fase di Modifica, Cancellazione, Iscrizione |
| TIPO_CONTINUAZIONE_REATO | VARCHAR2(2) | Eventuale ID del record SENTENZA da cui è stato derivato questo record |
| KEY_REATO_NSC | NUMBER(38) | S/N indica se il titolo risulta momentaneamente escluso |
| FLAG_STATO | VARCHAR2(1) | E=estratto, M=modificato, C=Cancellato, I=Iscritto |
| MOTIVO_MODIFICA | VARCHAR2(2000) | Note inserite dall'operatore in fase di Modifica, Cancellazione, Iscrizione |
| TIT_ID_TITOLO_CUMULATO | NUMBER(38) | FK alla tabella TITOLO_CUMULATO |
| ID_REATO_ORIGINE | NUMBER(38) | Eventuale Id del record Reato da cui è stato derivato questo record |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |



# REATO_PREDISPOSTO
tabella contenente i dati relativi al reato predisposto. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_REATO_PREDISPOSTO | NUMBER NOT NULL | Identificativo del reato predisposto |
| PROGR_NORMA | NUMBER NOT NULL | Progressivo della norma |
| NOME_ELEMENTO | VARCHAR2 (100 CHAR) NOT NULL | Nome dell’elemento |
| COD_FONTE | VARCHAR2 (5 CHAR) | Codice della fonte informativa |
| ANNO_FONTE | NUMBER | Anno della fonte informativa |
| NUMERO_FONTE | VARCHAR2 (6 CHAR) | Numero della fonte informativa |
| COD_SOTTONUMERAZIONE | VARCHAR2 (2 CHAR) | Codice della sottonumerazione |
| COMMA | VARCHAR2 (10 CHAR) | Comma del reato |
| LETTERA | VARCHAR2 (2 CHAR) | Lettera del reato |
| NUMERO | VARCHAR2 (2 CHAR) | Numero del reato |
| ARTICOLO | VARCHAR2 (50 CHAR) | Articolo del reato |
| NOTE_ELEMENTO | VARCHAR2 (2000 CHAR) | Note dell’elemento |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR). | Ufficio dell’operatore che ha aggiornato il record |



# REATO_SENTENZA_SIGE
tabella associativa tra il reato e la sentenza coinvolta in un procedimento sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| REA_ID_REATO | NUMBER NOT NULL | ID del record REATO |
| FAS_SIGE_SEN_ID | NUMBER NOT NULL | ID del record FAS_SIGE_SENTENZA |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| FAS_SIGE_SENTENZA_FK | FAS_SIGE_SEN_ID | (FAS_SIGE_SENTENZA.ID_FAS_SIGE_SENTENZA) |
| REA_ID_REATO_FK | REA_ID_REATO | (REATO.ID_REATO) |




# REFERTO_SCARCERAZIONE
tabella contenente i dati relativi al referto per la scarcerazione. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_REFERTO_SCARCERAZIONE | NUMBER NOT NULL | Chiave numerica legata a sequence "REF_SCA_SEQ" |
| ANNO_NOTA | NUMBER | Anno del referto |
| NUM_NOTA | VARCHAR2 (6 CHAR) | Numero del referto |
| DATA_NOTA | DATE | Data del referto |
| DATA_SCARCERAZIONE | DATE | Data di scarcerazione |
| NOTE | VARCHAR2 (2000 CHAR) | Eventuali note aggiuntive |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2 (4 CHAR) | Identificativo dell’istituto di detenzione |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| REF_SCA_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |





# RELAZIONE
tabella contenente i dati relativi alla relazione. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_RELAZIONE | NUMBER NOT NULL | Identificativo della tabella |
| ATT_ID_ATTIVITA | NUMBER | Identificativo dell’attività |
| NOTE | VARCHAR2 (1000 CHAR) | Note |
| DOC_BLOB | BLOB | Documento che contiene la relazione |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FLAG_DOCUMENTO_REGISTRATO | VARCHAR2 (1 CHAR) | S/N flag documento registrato |
| RIC_ID_RICHIESTA | NUMBER | Identificativo della richiesta |
| COD_UFFICIO_DESTINATARIO | VARCHAR2 (11 CHAR) | Codice dell’ufficio destinatario |
| DATA_EMISSIONE | DATE | Data di emissione |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| REL_ATT_FK | ATT_ID_ATTIVITA | (ATTIVITA.ID_ATTIVITA) |
| REL_RIC_FK | RIC_ID_RICHIESTA | (RICHIESTA.ID_RICHIESTA) |






# RELAZIONE_FUNZIONE
tabella contenente le relazioni gerarchiche delle funzionalità di sies. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| FUN_ID_FUNZIONE | NUMBER NOT NULL | Identificativo della tabella |
| FUN_ID_FUNZIONE_FIGLIA | NUMBER NOT NULL | Identificativo della funzione foglia |
| COD_TIPO_VISUALIZZAZIONE | VARCHAR2 (2 CHAR) NOT NULL | Rappresenta il tipo di elemento mostrato a video. In particolare, indica se la funzione figlio deve essere visualizzato come un pulsante o un elemento di combo o una list-box. Deriva dal dominio TIPO_VISUALIZZAZIONE |
| LABEL_FUNZIONE | VARCHAR2 (100 CHAR) | Nel caso di cod_tipo_visualizzazione = menù o combo indica cosa viene mostrato a video. |
| ORDINE_VISUALIZZAZIONE | NUMBER NOT NULL | Indica l'ordine di visualizzazione dei figli procedendo dal primo in poi. |
| IMMAGINE | VARCHAR2 (100 CHAR). | Percorso della funzione |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| REL_FUN_FUN_FIGLIA_FK | FUN_ID_FUNZIONE_FIGLIA | (FUNZIONE.ID_FUNZIONE) |
| REL_FUN_FUN_FK | FUN_ID_FUNZIONE | (FUNZIONE.ID_FUNZIONE) |





# REMOTE_LOGIN
tabella contenente i dati relativi all’utente che si collega in remoto. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ORIGINAL_USERID | VARCHAR2 (6 CHAR) NOT NULL | Userid dell’operatore originale |
| NOME | VARCHAR2 (100 CHAR) NOT NULL | Nome di chi si sta collegando |
| COGNOME | VARCHAR2 (100 CHAR) NOT NULL | Cognome di chi si sta collegando |
| EMAIL | VARCHAR2 (100 CHAR) | Indirizzo dell’email di chi si sta collegando |
| TELEFONO | VARCHAR2 (100 CHAR) | Telefono di chi si sta collegando |
| FAX | VARCHAR2 (100 CHAR) | Fax di chi si sta collegando |
| LOCAL_PRF_COD_PROFILE | NUMBER NOT NULL | Codice del profilo dell’operatore locale |
| DATA_ACCESSO | DATE NOT NULL | Data di accesso |
| LOCAL_USERID | VARCHAR2 (6 CHAR) NOT NULL | Userid dell’utente locale |
| ORIGINAL_UFF_COD_UFFICIO | VARCHAR2 (11 CHAR) NOT NULL | Codice dell’ufficio originale |
| LOCAL_UFF_COD_UFFICIO | VARCHAR2 (11 CHAR). | Sede dell’ufficio originale |



# RESIDENZA
tabella contenente i dati relativi alla residenza. utilizzata dal sottosistema siep-sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_RESIDENZA | NUMBER NOT NULL | Chiave numerica legata a sequence "RES_SEQ" |
| COD_STATO | VARCHAR2 (3 CHAR) | Deriva da dominio "NAZIONE" Codice dello stato di residenza. |
| COD_PROVINCIA | VARCHAR2 (2 CHAR) | Codice della provincia di Domicilio/Residenza. Deriva da dominio. |
| COD_COMUNE | VARCHAR2 (6 CHAR) | Fa riferimento alla tabella di dominio COMUNE. |
| CAP | VARCHAR2 (5 CHAR) | Codice di avviamento postale di Domicilio/Residenza. |
| INDIRIZZO | VARCHAR2 (200 CHAR) | Campo descrittivo dell'indirizzo di Domicilio/Residenza. Non sono effettuati controlli di validità delle particelle toponomastiche. |
| COD_TIPO_RESIDENZA | VARCHAR2 (1 CHAR) | Identifica se i dati inseriti nel record fanno riferimento al Domicilio o alla Residenza. Deriva da dominio e vale: D - domicilio; R – residenza |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| SOG_ID_SOGGETTO | NUMBER | Identificativo del soggetto |
| DESC_COMUNE_ESTERO | VARCHAR2 (200 CHAR). | Descrizione dell'eventuale Comune estero di Residenza. |
| FLG_DOM_AVV | VARCHAR2(1) | Indica se il soggetto viene domiciliato presso avvocato |
| ID_PARTE_UDIENZA | NUMBER(38) | Indica la parte udienza a cui è collegata la residenza |
| FLG_DOMICILIO_DIFENSORE | VARCHAR2(1) | Se impostato a S indica che il soggetto ha il domicilio presso il difensore |
| ID_CIVILMENTE_OBBLIGATO | NUMBER(38) |  |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| RES_SOG_FK | SOG_ID_SOGGETTO | (SOGGETTO.ID_SOGGETTO) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| RESIDENZA_FASCICOLO_SIGE | RES_FAS_SIGE_RESIDENZA | RES_ID_RESIDENZA |


# RESIDENZA_FASCICOLO_SIEP
tabella associativa tra la tabella residenza e fascicolo siep. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| DATA_INIZIO_VALIDITA | DATE | Data di inizio validità |
| DATA_FINE_VALIDITA | DATE | Data di fine validità |
| RES_ID_RESIDENZA | NUMBER NOT NULL | Identificativo della residenza |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL. | Identificativo del fascicolo SIEP |





# RESIDENZA_FASCICOLO_SIGE
tabella associativa tra la residenza e il fascicolo sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| DATA_INIZIO_VALIDITA | DATE | Data di inizio validità |
| DATA_FINE_VALIDITA | DATE | Data di fine validità |
| RES_ID_RESIDENZA | NUMBER NOT NULL | Identificativo della residenza |
| FAS_SIE_ID_FASCICOLO_SIGE | NUMBER NOT NULL | Identificativo del fascicolo SIGE |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| RES_FAS_SIGE_FAS_SIGE_FK | FAS_SIGE_ID_FASCICOLO_SIGE | (FASCICOLO_SIGE.ID_FASCICOLO_SIGE) |
| RES_FAS_SIGE_RESIDENZA | RES_ID_RESIDENZA | (RESIDENZA.ID_RESIDENZA) |







# RESIDENZA_FASCICOLO_SIUS
tabella associativa tra la residenza e il fascicolo sius. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| DATA_INIZIO_VALIDITA | DATE | Data di inizio validità |
| DATA_FINE_VALIDITA | DATE | Data di fine validità |
| RES_ID_RESIDENZA | NUMBER NOT NULL | Identificativo della residenza |
| FAS_SIE_ID_FASCICOLO_SIUS | NUMBER NOT NULL | Identificativo del fascicolo SIUS |


# RIAPERTURA_FASCICOLO_SIEP
tabella contenente i dati relativi alla riapertura del fascicolo siep. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_RIAPERTURA_FASCICOLO_SIEP | NUMBER NOT NULL | Identificativo della riapertura del fascicolo SIEP |
| COD_MOTIVO | VARCHAR2(4) | Codice del motivo |
| DATA_RIAPERTURA | DATE | Data di riapertura |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(11) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| RIAPER_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |



# RICHIESTA
tabella contenente i dati relativi alla richiesta. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_RICHIESTA | NUMBER NOT NULL | ID della richiesta |
| DATA_RICHIESTA | DATE | Data della richiesta |
| COD_TIPO_RICHIESTA | VARCHAR2 (4 CHAR) | Codice del tipo della richiesta ( domain : TIPO_RICHIESTA ) |
| COD_TIPO_RICHIEDENTE | VARCHAR2 (4 CHAR) | Codice del tipo richiedente ( domain : TIPO_RICHIEDENTE ) |
| NOTE | VARCHAR2 (1000 CHAR) | Note |
| DOC_BLOB | BLOB | BLOB per stampa documento |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell''operatore che ha inserito il rec. |
| DATA_INSERIMENTO | DATE | Data dell''inserimento della richiesta |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Codice dell''ufficio che ha inserito il rec. |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell''operatore che ha aggiornato il rec. |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del rec. |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Codice dell''ufficio che ha aggiornato il rec. |
| FAS_SIE_ID_FAS_SIEPE | NUMBER NOT NULL | ID di relazione con il fascicolo SIEPE |
| FLAG_DOCUMENTO_REGISTRATO | VARCHAR2 (1 CHAR) | Flag di validazione del documento |
| COD_UFFICIO_DESTINATARIO | VARCHAR2 (11 CHAR) | Codice dell''ufficio destinatario |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| RIC_FAS_SIEPE_FK | FAS_SIE_ID_FAS_SIEPE | (FASCICOLO_SIEPE.ID_FASCICOLO_SIEPE) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| RELAZIONE | REL_RIC_FK | RIC_ID_RICHIESTA |


# RICHIESTA_CONVERSIONE
tabella contenente i dati relativi alla richiesta di conversione. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_RICHIESTA_CONVERSIONE | NUMBER NOT NULL | Identificativo della tabella |
| ANNO_PARTITA | NUMBER | Anno partita |
| NUM_PARTITA | NUMBER | Numero partita |
| NUM_EX_CAMPIONE | VARCHAR2 (20 CHAR) | Numero ex campione |
| PROT_CIRCOSRIZIONE_DOGANALE | VARCHAR2 (20 CHAR) | Protocollo della circoscrizione doganale |
| COD_TIPO_AUTORITA_EMITTENTE | VARCHAR2 (6 CHAR) | Tipo dell’autorità emittente |
| COD_LUOGO_EMITTENTE | VARCHAR2 (6 CHAR) | Luogo dell’autorità emittente |
| DATA_RICEZIONE_ATTO | DATE | Data di ricezione dell’atto |
| DATA_ISCRIZIONE_ATTO | DATE | Data di iscrizione dell’atto |
| DATA_ESAZIONE | DATE | Data di esazione |
| IMPORTO_MULTA | NUMBER (2-16) | Importo della multa |
| DATA_PRESCRIZIONE_MULTA | DATE | Data di prescrizione della multa |
| FLAG_IMPRESCRITTIBILE_MULTA | VARCHAR2 (1 CHAR) | S/N multa imprescrittibile |
| IMPORTO_AMMENDA | NUMBER (2-16) | Importo dell’ammenda |
| DATA_PRESCRIZIONE_AMMENDA | DATE | Data di prescrizione dell’ammenda |
| FLAG_IMPRESCRITTIBILE_AMMENDA | VARCHAR2 (1 CHAR) | S/N ammenda imprescrittibile |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER | Identificativo del fascicolo SIUS |
| DURATA_ESITO_ANNI | NUMBER | Anni della durata dell’esito |
| DURATA_ESITO_MESI | NUMBER | Mesi della durata dell’esito |
| DURATA_ESITO_GIORNI | NUMBER | Giorni della durata dell’esito |
| NUMERO_RATE | NUMBER | Numero delle rate |
| VALORE_RATA | NUMBER (2-16) | Valore della rata |
| VALORE_ULTIMA_RATA | NUMBER (2-16) | Valore dell’ultima rata |
| DATA_ANNULLAMENTO | DATE | Data di annullamento |
| COD_TIPO_SANZIONE | VARCHAR2 (2 CHAR) | 01=Liberta controllata; 02=Lavoro Sostitutivo |
| NOTE | VARCHAR2 (2000 CHAR) | Note |
| DATA_DEPOSITO | DATE | Data di deposito |
| DATA_INIZIO_PAGAMENTO | DATE | Data di inizio pagamento |
| NUMERO_GIORNI_INIZIO_PAGAMENTO | NUMBER. | Numero di giorni dall’inizio del pagamento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| RIC_CON_ID_EVENTO_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| RIC_CON_ID_FASC_SIEP_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |





# RICHIESTA_REMISSIONE
tabella contenente i dati relativi alla richiesta di emissione. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_RICHIESTA_REMISSIONE | NUMBER NOT NULL | Identificativo della tabella |
| ANNO_PARTITA | NUMBER | Anno partita |
| NUM_PARTITA | NUMBER | Numero partita |
| NUM_EX_CAMPIONE | VARCHAR2 (20 CHAR) | Numero ex campione |
| PROT_CIRCOSRIZIONE_DOGANALE | VARCHAR2 (20 CHAR) | Protocollo della circoscrizione doganale |
| COD_TIPO_AUTORITA_EMITTENTE | VARCHAR2 (6 CHAR) | Tipo dell’autorità emittente |
| COD_LUOGO_EMITTENTE | VARCHAR2 (6 CHAR) | Luogo dell’autorità emittente |
| COD_TIPO_PROVVEDIMENTO | VARCHAR2 (6 CHAR) | Tipo del provvedimento |
| DATA_EMISSIONE | DATE | Data di emissione |
| COD_AUTORITA_EMITTENTE_PROVV | VARCHAR2 (6 CHAR) | Codice dell’autorità emittente il provvedimento |
| COD_LUOGO_EMITTENTE_PROVV | VARCHAR2 (6 CHAR) | Sede dell’autorità emittente il provvedimento |
| FLAG_SPESE_CARCERE | VARCHAR2 (1 CHAR) | S/N indica se ci sono spese carcerarie |
| IMPORTO_SPESE_CARCERE | NUMBER (2-
16) | Importo delle spese carcerarie |
| FLAG_SPESE_PROCEDIMENTO | VARCHAR2 (1 CHAR) | S/N indica se ci sono spese del procedimento |
| IMPORTO_SPESE_PROCEDIMENTO | NUMBER (2-
16) | Importo delle spese del procedimento |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER | Identificativo del fascicolo SIUS |
| NOTE | VARCHAR2 (2000 CHAR) | Note |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| RIC_REM_ID_EVENTO_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| RIC_REM_ID_FASC_SIEP_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| COLLEGIO_ESPERTO | COL_ESP_COLLEGIO_FK | COL_ID_COLLEGIO |


# RICHIESTA_SIGE
tabella contenente i dati relativi alla richiesta sige. utilizzata dal sottosistema siep-sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_RICHIESTA_SIGE | NUMBER NOT NULL | Chiave primaria |
| COD_TIPO_ATTO | VARCHAR2 (4 CHAR) | Classificazione del tipo di richiesta |
| COD_TIPO_RICHIEDENTE | VARCHAR2 (4 CHAR)
DEFAULT null | Classificazione del richiedente. Associata al Dominio TIPO_RICHIEDENTE_SIGE di CG_REF_CODES |
| DATA_EMISSIONE | DATE | Data di emissione della richiesta |
| DATA_DEPOSITO | DATE
DEFAULT null | Data di deposito della richiesta |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) NOT NULL | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE NOT NULL | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) NOT NULL | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMEN TO | VARCHAR2 (100 CHAR)
DEFAULT null | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE
DEFAULT null | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR)
DEFAULT null | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER
DEFAULT null | ID del Fascicolo SIEP di competenza |
| COD_SEDE_RICHIEDENTE | VARCHAR2 (6 CHAR)
DEFAULT null | Codice COMUNE del Richiedente |
| DESC_RICHIEDENTE | VARCHAR2 (200 CHAR)
DEFAULT null | Indirizzo o altra informazione su Richiedente |
| COD_UFFICIO_RICHIEDENTE | VARCHAR2 (11 CHAR)
DEFAULT null | Ufficio del Richiedente valorizzato quando richiesta automatizzata |
| DATA_ARRIVO_CANCELLERIA | DATE
DEFAULT null | Data di arrivo in cancelleria della Richiesta |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| RIC_SIG_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| FASCICOLO_SIGE | FAS_SIG_RIC_SIG_FK | RIC_ID_RICHIESTA_SIGE |
| TENORE_SIGE | TEN_SIG_RIC_SIG_FK | RIC_SIG_ID_RICHIESTA_SIGE |


# RICHIESTE_INVIATE_CUM
tabella contenente i dati relativi alla richiesta inviata al cumulo. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_RICHIESTE_INVIATE_CUM | NUMBER(38) | Sequence |
| DATA_EMISSIONE | DATE | Data emissione |
| DATA_TRASMISSIONE | DATE | Data Trasmissione |
| COD_MAGISTRATO | VARCHAR2(6) | Codice del Magistrato firmatario Richiesta |
| CONTENUTO | VARCHAR2(2000) | Contenuto della Richiesta Inviata |
| COD_UFFICIO_DEST | VARCHAR2(11) | Codice dell’Ufficio GE/Sorv Destinatario |
| COD_LUOGO_DEST | VARCHAR2(6) | Codice Comune dell’Ufficio GE/Sorv Destinatario |
| ISTR_ID_ISTRUTTORIA_CUMULO | NUMBER(38) | FK alla tabella ISTRUTTORIA_CUMULO |
| DOC_BLOB | BLOB | Documento di invio prodotto |
| FLAG_VALIDATO | VARCHAR2(1) | ‘S’ se richiesta validata |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |


# RICHIESTE_PM_IN_CUMULO
tabella contenente i dati relativi alla Richieste del PM al GE/ alla Sorveglianza relative ad una Istruttoria Cumulo. utilizzata dal sottosistema siep-sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_RICHIESTE_PM_IN_CUMULO | NUMBER(38) | Sequence |
| COD_TIPO_RICHIESTA | VARCHAR2(3) | CG_REF_CODES.RV_DOMAIN= TIPO_RICHIESTA_CUMULO: 01=al GE, 02=alla SORV' |
| COD_TIPO_ANNOTAZIONE | VARCHAR2(3) | CG_REF_CODES.RV_DOMAIN= ’TIPO_ANNOTAZIONE’ |
| DATA_EMISSIONE | DATE | Data emissione |
| FLAG_PIU_MENO_R | VARCHAR2(1) | +/- |
| NUM_ANNI_RECLUSIONE_R | NUMBER(3) | Numero anni reclusione richiesti |
| NUM_MESI_RECLUSIONE_R | NUMBER(3) | Numero mesi reclusione richiesti |
| NUM_GIORNI_RECLUSIONE_R | NUMBER(4) | Numero giorni reclusione richiesti |
| IMPORTO_MULTA_R | NUMBER(11,2) | Importo multa richiesta |
| NUM_ANNI_ARRESTO_R | NUMBER(3) | Numero anni arresto richiesti |
| NUM_MESI_ARRESTO_R | NUMBER(3) | Numero mesi arresto richiesti |
| NUM_GIORNI_ARRESTO_R | NUMBER(4) | Numero giorni arresto richiesti |
| IMPORTO_AMMENDA_R | NUMBER(11,2) | Importo ammenda richiesta |
| FLAG_APP_PROVVISORIA | VARCHAR2(1) | A=Anticipazione, R=Richiesta senza Anticipazione' |
| COD_TIPO_PENA_ACCESSORIA | VARCHAR2(3) | CG_REF_CODES.RV_DOMAIN= ’TIPO_ PENA_ACCESSORIA’ |
| COD_TIPO_DURATA_PA | VARCHAR2(1) | CG_REF_CODES.RV_DOMAIN= ’TIPO_ DURATA’ |
| NUM_ANNI_PA | NUMBER(4) | Numero anni pena accessoria richiesti |
| NUM_MESI_PA | NUMBER(4) | Numero mesi pena accessoria richiesti |
| NUM_GIORNI_PA | NUMBER(4) | Numero giorni pena accessoria richiesti |
| COD_FONTE | VARCHAR2(5) | CG_REF_CODES.RV_DOMAIN= ’FONTE’ |
| ANNO_FONTE | NUMBER, | Anno della norma |
| NUMERO_FONTE | VARCHAR2(6) | Numero della norma |
| ARTICOLO | VARCHAR2(50) | Articolo della norma |
| COD_SOTTONUMERAZIONE | VARCHAR2(2) | Sottonumerazione articolo (bis, ter, ecc.) Associato al Dominio SOTTONUMERAZIONE della Tabella CG_REF_CODES |
| COMMA | VARCHAR2(10) | Comma dell'articolo trattato |
| LETTERA | VARCHAR2(2) | Lettera dell'articolo trattato |
| NUMERO | VARCHAR2(2) | Numero dell'articolo trattato |
| ANNO_CC | NUMBER, | Anno provvedimento Corte Costituzionale |
| NUMERO_CC | VARCHAR2(6) | Numero provvedimento Corte Costituzionale |
| DATA_CC | DATE, | Data provvedimento Corte Costituzionale |
| COD_DPR | VARCHAR2(2) | CG_REF_CODES.RV_DOMAIN= ’DPR’ |
| MOTIVAZIONI | VARCHAR2(2000) | Eventuali motivazioni |
| NOTE_RECLUSIONE | VARCHAR2(2000) | CG_REF_CODES.RV_DOMAIN= ’TIPO_DURATA’ |
| NUM_GIORNI_LA_REV | NUMBER(4) | Numero giorni L.A. revocati |
| NUM_GIORNI_LS_REV | NUMBER(4) | Numero giorni L.A. speciale revocati |
| NUM_GIORNI_LI_REV | NUMBER(4) | Numero giorni integrazione L.A. revocati |
| COD_MOTIVO | VARCHAR2(4) | CG_REF_CODES.RV_DOMAIN= ’MOTIVO_PROVVEDIMENTO’ |
| TIPO_ANNOTAZIONE_BENEFICIO | VARCHAR2(3) | CG_REF_CODES.RV_DOMAIN= ’TIPO_BENEFICIO’ |
| ISTR_ID_ISTRUTTORIA_CUMULO | NUMBER(38) | FK alla tabella ISTRUTTORIA_CUMULO |
| TIT_ID_TITOLO_CUMULATO | NUMBER(38) | Eventuale FK alla tabella TITOLO_CUMULATO |
| TIT_ID_TITOLO_CUMULATO_REF | NUMBER(38) | Eventuale REF al titolo collegato a quello per il quale si effettua la richiesta es: revoca beneficio |
| RIC_ID_RICHIESTE_INVIATE_CUM | NUMBER(38) | Eventuale FK alla tabella RICHIESTE_INVIATE_CUMULO |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |

# RICHPM_BENEFICIO_CUM
tabella contenente i dati relativi relazione fra le tabelle RICHIESTE_PM_IN_CUMULO e  BENEFICIO_CUMULO. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| RIC_ID_RICHIESTE_PM_IN_CUMULO | NUMBER(38) | FK alla tabella RICHIESTE_PM_IN_CUMULO |
| BEN_ID_BENEFICIO_CUM | NUMBER(38) | FK alla tabella BENEFICIO_CUMULO |


# RICHPM_MISSICUR_CUM
tabella contenente i dati relativi relazione fra le tabelle RICHIESTE_PM_IN_CUMULO e  MISURA_SICUREZZA_CUMULO. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| RIC_ID_RICHIESTE_PM_IN_CUMULO | NUMBER(38) | FK alla tabella RICHIESTE_PM_IN_CUMULO |
| MIS_ID_MISSICUR_CUMULO | NUMBER(38) | FK alla tabella MISURA_SICUREZZA_CUMULO |
| FLAG_CONDONO | VARCHAR (1) | S, se misura condonata |


# RICHPM_PENACC_CUM
tabella contenente i dati relativi relazione fra le tabelle RICHIESTE_PM_IN_CUMULO e  PENA_ACCESSORIA_CUMULO. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| RIC_ID_RICHIESTE_PM_IN_CUMULO | NUMBER(38) | FK alla tabella RICHIESTE_PM_IN_CUMULO |
| PEN_ID_PENACC_CUMULO | NUMBER(38) | FK alla tabella PENA_ACCESSORIA_CUMULO |
| FLAG_CONDONO | VARCHAR (1) | S, se misura condonata |


# RICHPM_REATO_CUM
tabella contenente i dati relativi relazione fra le tabelle RICHIESTE_PM_IN_CUMULO e  REATO_CUMULO. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| RIC_ID_RICHIESTE_PM_IN_CUMULO | NUMBER(38) | FK alla tabella RICHIESTE_PM_IN_CUMULO |
| REA_ID_REATO_CUMULO | NUMBER(38) | FK alla tabella REATO_CUMULO |


# RICHPM_SANZIONE_SOST_CUM
tabella contenente i dati relativi relazione fra le tabelle RICHIESTE_PM_IN_CUMULO e  SANZIONE_SOST_CUM. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| RIC_ID_RICHIESTE_PM_IN_CUMULO | NUMBER(38) | FK alla tabella RICHIESTE_PM_IN_CUMULO |
| SS_ID_SANZIONE_SOST_CUM | NUMBER(38) | FK alla tabella SANZIONE_SOST_CUM |

# RICHPM_STATO_ESEC_CUM
tabella contenente i dati relativi relazione fra le tabelle RICHIESTE_PM_IN_CUMULO e  STATO_ESEC_TITOLO_CUMULATO. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| RIC_ID_RICHIESTE_PM_IN_CUMULO | NUMBER(38) | FK alla tabella RICHIESTE_PM_IN_CUMULO |
| SS_ID_SANZIONE_SOST_CUM | NUMBER(38) | FK alla tabella STATO_ESEC_TITOLO_CUMULATO |


# RICHPM_TITOLO_CUM
tabella contenente i dati relativi relazione fra le tabelle RICHIESTE_PM_IN_CUMULO e  TITOLO_CUMULATO. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| RIC_ID_RICHIESTE_PM_IN_CUMULO | NUMBER(38) | FK alla tabella RICHIESTE_PM_IN_CUMULO |
| TIT_ID_TITOLO_CUMULATO | NUMBER(38) | FK alla tabella TITOLO_CUMULATO |
| FLAG_INTERO_CUMULO | CHAR(1) | Flag che indica se la richiesta l’intero ticket |

# RIEPILOGO_PROVVEDIMENTO
tabella contenente i dati relativi al riepilogo del provvedimento. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_RIEPILOGO_PROVVEDIMENTO | NUMBER NOT NULL | Chiave numerica legata a sequence "RIE_PRO_SEQ". |
| NUM_RES | NUMBER | Numero RES |
| NUM_PROGRESSIVO_RES | NUMBER | Numero progressivo RES |
| NUM_PROTOCOLLO_RES | NUMBER | Numero protocollo RES |
| FLAG_ERGASTOLO | VARCHAR2 (1 CHAR) | Codifica delle condizioni di reclusione x Ergastolo: (Ergastolo con Isolamento Diurno ...). Associato al dominio FLAG_ERGASTOLO di CG_REF_CODES |
| NUM_ANNI_RECLUSIONE | NUMBER | Numero anni di reclusione |
| NUM_MESI_RECLUSIONE | NUMBER | Numero mesi di reclusione |
| NUM_GIORNI_RECLUSIONE | NUMBER | Numero giorni di reclusione |
| IMPORTO_MULTA | NUMBER (2-16) | Totale importo multa |
| NUM_ANNI_ARRESTO | NUMBER | Numero anni di arresto |
| NUM_MESI_ARRESTO | NUMBER | Numero mesi di arresto |
| NUM_GIORNI_ARRESTO | NUMBER | Numero giorni di arresto |
| IMPORTO_AMMENDA | NUMBER (2-16) | Totale importo ammenda |
| NUM_ANNI_PRESOFFERTO | NUMBER | Numero anni di Presofferto |
| NUM_MESI_PRESOFFERTO | NUMBER | Numero mesi di Presofferto |
| NUM_GIORNI_PRESOFFERTO | NUMBER | Numero giorni di Presofferto |
| NUM_ANNI_INTERRUZIONE | NUMBER | Numero anni di interruzione |
| NUM_MESI_INTERRUZIONE | NUMBER | Numero mesi di interruzione |
| NUM_GIORNI_INTERRUZIONE | NUMBER | Numero giorni di interruzione |
| NUM_GIORNI_LIB_ANTICIPATA | NUMBER | Numero giorni liberazione anticipata |
| NUM_ANNI_RECLUSIONE_BENEFICI | NUMBER | Benefici: numero anni di reclusione |
| NUM_MESI_RECLUSIONE_BENEFICI | NUMBER | Benefici: numero mesi di reclusione |
| NUM_GIORNI_RECLUSIONE_BENEFICI | NUMBER | Benefici: numero giorni di reclusione |
| IMPORTO_MULTA_BENEFICI | NUMBER (2-16) | Totale importo multa benefici |
| NUM_ANNI_ARRESTO_BENEFICI | NUMBER | Benefici: numero anni di arresto |
| NUM_MESI_ARRESTO_BENEFICI | NUMBER | Benefici: numero mesi di arresto |
| NUM_GIORNI_ARRESTO_BENEFICI | NUMBER | Benefici: numero giorni di arresto |
| IMPORTO_AMMENDA_BENEFICI | NUMBER (2-16) | Totale importo ammenda benefici |
| NUM_ANNI_AUMENTI_PENA_RECLUS | NUMBER | Numero anni aumenti pena reclusione |
| NUM_MESI_AUMENTI_PENA_RECLUS | NUMBER | Numero mesi aumenti pena reclusione |
| NUM_GIORNI_AUMENTI_PENA_RECLUS | NUMBER | Numero giorni aumenti pena reclusione |
| IMPORTO_MULTA_AUMENTI_PENA | NUMBER (2-16) | Totale importo multa aumenti pena |
| NUM_ANNI_AUMENTI_PENA_ARRES | NUMBER | Numero anni aumenti pena arresto |
| NUM_MESI_AUMENTI_PENA_ARRES | NUMBER | Numero mesi aumenti pena arresto |
| NUM_GIORNI_AUMENTI_PENA_ARRES | NUMBER | Numero giorni aumenti pena arresto |
| IMPORTO_AMMENDA_AUMENTI_PENA | NUMBER (2-16) | Totale importo ammenda aumenti pena |
| DIES_A_QUO | VARCHAR2 (1 CHAR) | Giorno dell'arresto da considerare o no nel calcolo della pena |
| DATA_INIZIO_PENA | DATE | Data inizio pena |
| DATA_FINE_PENA | DATE | Data fine pena |
| DATA_FINE_RECLUSIONE | DATE | Data fine reclusione |
| DATA_FINE_PRECEDENTE | DATE | Data fine precedente |
| DATA_FINE_DET_DOMICILIARE | DATE | Data fine detenzione domiciliare |
| NUM_ANNI_PENA_RESIDUA_RECLUS | NUMBER | Numero anni pena residua reclusione |
| NUM_MESI_PENA_RESIDUA_RECLUS | NUMBER | Numero mesi pena residua reclusione |
| NUM_GIORNI_PENA_RESIDUA_RECLUS | NUMBER | Numero giorni pena residua reclusione |
| IMPORTO_MULTA_RESIDUA | NUMBER (2-16) | Totale importo multa pena residua |
| NUM_ANNI_PENA_RESIDUA_ARRES | NUMBER | Numero anni pena residua arresto |
| NUM_MESI_PENA_RESIDUA_ARRES | NUMBER | Numero mesi pena residua arresto |
| NUM_GIORNI_PENA_RESIDUA_ARRES | NUMBER | Numero giorni pena residua arresto |
| IMPORTO_AMMENDA_RESIDUA | NUMBER (2-16) | Totale importo ammenda pena residua |
| NUM_ANNI_FUNGIBILITA | NUMBER | Numero anni di fungibilità |
| NUM_MESI_FUNGIBILITA | NUMBER | Numero mesi di fungibilità |
| NUM_GIORNI_FUNGIBILITA | NUMBER | Numero giorni di fungibilità |
| COD_TIPO_PROVVEDIMENTO | NUMBER | Codice Tipo provvedimento |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |




# RIFERIMENTO_FASCICOLO_SIEP
tabella contenente i dati relativi al riferimento di un fascicolo siep. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_RIFERIMENTO_FASCICOLO_SIEP | NUMBER NOT NULL | Chiave numerica legata a sequence "RIF_SIE_SEQ" |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del Fascicolo SIEP associato. |
| ANNO_FASCICOLO_SIEP | NUMBER | Chiave Anno Fascicolo SIEP. |
| PROGR_FASCICOLO_SIEP | NUMBER | Chiave Progr Fascicolo SIEP. |
| COD_UFF_FASCICOLO_SIEP | VARCHAR2 (11 CHAR) | Chiave Ufficio Fascicolo SIEP. |
| COD_TIPO_PROVVEDIMENTO | VARCHAR2 (2 CHAR) | Codifica del Tipo Provvedimento. Associato al Dominio TIPO_PROVVEDIMENTO di CG_REF_CODES. |
| DATA_PROVVEDIMENTO | DATE | Data Provvedimento. |
| ANNO_PROVVEDIMENTO | NUMBER | Anno Provvedimento. |
| NUMERO_PROVVEDIMENTO | VARCHAR2 (6 CHAR) | Numero Provvedimento. |
| COD_TIPO_AUTORITA_EMITTENTE | VARCHAR2 (6 CHAR) | Codifica del Tipo Autorità Emittente. Associato al Dominio TIPO_AUTORITA di CG_REF_CODES. |
| COD_LUOGO_EMITTENTE | VARCHAR2 (6 CHAR) | Codice comune del Luogo Emittente. |
| DATA_IRREVOCABILITA | DATE | Data Irrevocabilità. |
| DATA_FINE_VALIDITA | DATE | DATA_FINE_VALIDITA |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER NOT NULL | Identificativo del fascicolo SIUS |
| NOTE | VARCHAR2 (2000 CHAR). | Eventuali note aggiuntive |
| FLAG_MS_SN | VARCHAR2 (1 CHAR) | Indica se il Titolo Esecutivo è presente su SIAP oppure no |
| FLAG_FAS_SIUS_UNIF_SN | VARCHAR2 (1 CHAR) | Indica se il Titolo Esecutivo è stato aggiunto in fase di unificazione oppure no |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| FAS_SIE_ID_FASCICOLO_SIEP_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |
| FAS_SIU_ID_FASCICOLO_SIUS_FK | FAS_SIU_ID_FASCICOLO_SIUS | (FASCICOLO_SIUS.ID_FASCICOLO_SIUS) |


# RIFERIMENTO_FASCICOLO_SIUS
tabella contenente i dati relativi al riferimento di un fascicolo sius. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_RIFERIMENTO_FASCICOLO_SIUS | NUMBER NOT NULL | Chiave numerica legata a sequence "RIF_SIU_SEQ" |
| ANNO_FASCICOLO_SIUS | UMBER | Anno Fascicolo SIUS riferito. |
| PROGR_FASCICOLO_SIUS | NUMBER | Progressivo Fascicolo SIUS riferito. |
| COD_UFF_FASCICOLO_SIUS | VARCHAR2 (11 CHAR) | Codice ufficio Fascicolo SIUS riferito. |
| DATA_RICEZIONE | DATE | Data di ricezione. |
| COD_OGGETTO_PROCEDIMENTO | VARCHAR2 (4 CHAR) | Codice Oggetto Procedimento. Associato al dominio OGGETTO_PROCEDIMENTO di CG_REF_CODES. |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL | Identificativo del fascicolo SIEP |
| NOTE | VARCHAR2 (2000 CHAR). | Note |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| RIF_SIU_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |





# RINNOVO
tabella contenente i dati relativi al rinnovo. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_RINNOVO | NUMBER NOT NULL | Chiave numerica legata a sequence "RIN_SEQ" |
| COD_TIPO_RINNOVO | VARCHAR2(2) | Tipo o motivo rinnovo |
| DATA_RINNOVO | DATE | Data rinnovo |
| COD_TIPO_AUTORITA_RINNOVO | VARCHAR2 (2 CHAR) | Autorità che provvede al rinnovo |
| COD_LUOGO_RINNOVO | VARCHAR2 (6 CHAR) | Codice del luogo autorità che opera il rinnovo |
| NOTE | VARCHAR2 (2000 CHAR) | Eventuali note a corredo |
| DOC_BLOB | BLOB | Documento long binary |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| NOT_ID_NOTIFICA | NUMBER | Identificativo della notifica |
| VER_ID_VERBALE | NUMBER | Identificativo del verbale |
| FLAG_DOCUMENTO_REGISTRATO | VARCHAR2 (1 CHAR) | S/N documento registrato |
| TEM_ID_TEMPLATE | VARCHAR2 (12 CHAR) | Identificativo del template |
| NUOVO_LUOGO_NOTIFICA | VARCHAR2 (2000) CHAR | Nuovo luogo della notifica |
| esito | VARCHAR2(1) | Indica se Esito positivo (P) o Esito Negativo (N) |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| RIN_NOT_FK | NOT_ID_NOTIFICA | (NOTIFICA.ID_NOTIFICA) |
| RIN_VER_FK | VER_ID_VERBALE | (VERBALE.ID_VERBALE) |


# RINVIO_PROVVEDIMENTO
tabella contenente i dati relativi al rinvio di un provvedimento. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_RINVIO_PROVVEDIMENTO | NUMBER NOT NULL | Chiave numerica legata a sequence "RIN_PRO_SEQ" |
| ANNO_S19 | NUMBER NOT NULL | Anno del registro mod. 39 |
| PROGR_S19 | NUMBER NOT NULL | Progressivo del registro mod. 39 |
| COD_NATURA_PENA | VARCHAR2 (2 CHAR) | Codice della natura della pena |
| DATA_TX_PENA_PROVV | DATE | Data della pena del provvedimento |
| DATA_ESECUZIONE_PROVV | DATE | Data di esecuzione del provvedimento |
| DATA_TX_PENA_ORD | DATE | Data della pena dell’ordinanza |
| DATA_ESECUZIONE_ORD | DATE | Data di esecuzione dell’ordinanza |
| NOTE | VARCHAR2 (2000 CHAR) | Note |
| DEP_DEC_ID_DEPOSITO_DECRETO | NUMBER | Identificativo del deposito del decreto |
| DEP_OPID_DEPOSITO_ORDINANZA_PC | NUMBER | Identificativo del deposito dell’ordinanza |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| GEN_PRID_GENERALE_PROCEDIMENTO | NUMBER NOT NULL. | Identificativo del generale procedimento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| RIN_PRO_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO | (GENERALE_PROCEDIMENTO.ID_GENERALE_PROCEDIMENTO) |






# RISULTATO_RICERCA
tabella contenente i dati relativi al risultato di una ricerca. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_RICERCA | NUMBER NOT NULL | Identificativo della ricerca |
| COD_UFFICIO | VARCHAR2 (11 CHAR) | Codice dell’ufficio |
| ID_FASCICOLO_SIEP | NUMBER NOT NULL | Identificativo del fascicolo SIEP |
| CHIAVE_ANNO | NUMBER | Anno del fascicolo SIEP |
| CHIAVE_PROGR | NUMBER | Numero del fascicolo SIEP |
| COGNOME | VARCHAR2 (100 CHAR) | Cognome del soggetto ricercato |
| NOME | VARCHAR2 (100 CHAR) | Nome del soggetto ricercato |
| LUOGO_NASCITA | VARCHAR2 (250 CHAR) | Luogo di nascita del soggetto ricercato |
| DATA_NASCITA | DATE | Data di nascita del soggetto ricercato |
| DATA_REATO | DATE | Data del commesso reato |
| DATA_FINE_PENA | DATE | Data di fine pena |
| NUM_ANNI_PENA_RES | NUMBER | Numero anni di pena residua |
| NUM_MESI_PENA_RES | NUMBER | Numero mesi di pena residua |
| NUM_GIORNI_PENA_RES | NUMBER | Numero giorni di pena residua |
| COD_POSIZIONE_GIURIDICA | VARCHAR2 (2 CHAR) | Codice della posizione giuridica |
| DESCR_POSIZIONE_GIURIDICA | VARCHAR2 (500 CHAR) | Descrizione della posizione giuridica |
| COD_UTENTE | VARCHAR2 (100 CHAR). | Codice dell’utente |
| NAZIONALITA | VARCHAR2(300) | Descrizione della nazionalità |




# SANZIONE_AMMINISTRATIVA
tabella contenente i dati relativi alla sanzione amministrativa. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SANZIONE_AMMINISTRATIVA | NUMBER NOT NULL | Identificativo della tabella |
| ANNO_REG | NUMBER NOT NULL | Anno del registro |
| NUM_REG | NUMBER NOT NULL | Numero del registro |
| COD_TIPO_SANZIONE | VARCHAR2 (2 CHAR) | Tipo della sanzione |
| COD_TIPO_MANUFATTO | VARCHAR2 (1 CHAR) | Tipo del manufatto |
| MODALITA_DEMOLIZIONE | VARCHAR2 (50 CHAR) | Modalità della demolizione |
| INDIRIZZO_MANUFATTO | VARCHAR2 (50 CHAR) | Indirizzo del manufatto |
| DATA_DEMOLIZIONE | DATE | Data della demolizione |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| EVE_ID_EVENTO. | NUMBER | Identificativo dell’evento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| SAN_AMM_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| SAN_AMM_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |


# SANZIONE_SOST_CUM
tabella contenente i dati relativi alle sanzioni sostitutive relative al cumulo. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SANZIONE_SOST_CUM | NUMBER(38) | Identificativo della tabella |
| COD_TIPO_SANZIONE | VARCHAR2(1) | Tipo (-, L, P, S, E) |
| NUM_ANNI | NUMBER(2) | Numero Anni |
| NUM_MESI | NUMBER(2) | Numero Mesi |
| NUM_GIORNI | NUMBER(3) | Numero Giorni |
| SANZIONE_PECUNIARIA_MULTA | NUMBER(16,2) | Importo della Multa |
| SANZIONE_PECUNIARIA_AMMENDA | NUMBER(16,2) | Importo Ammenda |
| PC_ID_PENA_COMPLESSIVA_CUM | NUMBER(38) | FK alla tabella PENA_COMPLESSIVA_CUM |
| FLAG_STATO | VARCHAR2(1) | E=estratto, M=modificato, C=Cancellato, I=Iscritto |
| MOTIVO_MODIFICA | VARCHAR2(2000) | Note inserite dall''operatore in fase di Modifica, Cancellazione, Iscrizione |
| TIT_ID_TITOLO_CUMULATO | NUMBER(38) | FK alla tabella TITOLO_CUMULATO |
| ID_SANZIONE_SOST_ORIGINE | NUMBER(38) | Eventuale ID del record SANZIONE SOSTITUTIVA da cui è stato derivato questo record |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |


# SANZIONE_SOSTITUTIVA
tabella contenente i dati relativi alla sanzione sostitutiva. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SANZIONE_SOSTITUTIVA | NUMBER NOT NULL | Identificativo della tabella |
| COD_TIPO_SANZIONE | VARCHAR2 (1 CHAR) NOT NULL | Tipo di sanzione |
| NUM_ANNI | NUMBER | Numero di anni della sanzione |
| NUM_MESI | NUMBER | Numero di mesi della sanzione |
| NUM_GIORNI | NUMBER | Numero di giorni della sanzione |
| SANZIONE_PECUNIARIA_MULTA | NUMBER (2-16) | Importo della multa della sanzione |
| ANNO_REGISTRO | NUMBER | Anno del registro |
| NUM_REGISTRO | NUMBER | Numero del registro |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| PEN_COM_ID_PENA_COMPLESSIVA | NUMBER NOT NULL | Identificativo della pena complessiva |
| SANZIONE_PECUNIARIA_AMMENDA | NUMBER (2-16) | Importo dell’ammenda della sanzione amministrativa |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| SAN_SOS_PEN_COM_FK | PEN_COM_ID_PENA_COMPLESSIVA | (PENA_COMPLESSIVA.ID_PENA_COMPLESSIVA) |


# SANZIONE_SOST_RESIDUA
tabella contenente i dati relativi alla sanzione sostitutiva residua. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SANZIONE_SOST_RESIDUA | NUMBER NOT NULL | Identificativo della tabella |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL | Identificativo del fascicolo SIEP |
| EVE_ID_EVENTO | NUMBER | Evento che ha rideterminato la SS da eseguire. Può essere null se la SS viene determinata sul primo calcolo |
| PEN_RES_ID_PENA_RESIDUA | NUMBER NOT NULL | Pena residua che ha rideterminato il calcolo |
| COD_TIPO_SANZIONE | VARCHAR2 (1 CHAR) NOT NULL | Dominio TIPO_SANZIONE_SOSTITUTIVA |
| DATA_INIZIO | DATE | Data inizio sostituzione residua |
| DATA_FINE_PRESUNTA | DATE | Data fine presunta sostituzione residua |
| DATA_FINE | DATE | Data fine sostituzione residua |
| NUM_ANNI | NUMBER | Numero anni sostituzione residua |
| NUM_MESI | NUMBER | Numero mesi sostituzione residua |
| NUM_GIORNI | NUMBER | Numero giorni sostituzione residua |
| SANZIONE_PECUNIARIA_MULTA | NUMBER (2-16) | Importo multa della sostituzione residua |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| SANZIONE_PECUNIARIA_AMMENDA | NUMBER (2-16) | Importo dell’ammenda sostituzione residua |



# SCADENZARIO_SIEP
tabella contenente i dati relativi allo scadenzario dei fascicoli siep. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SCADENZARIO_SIEP | NUMBER NOT NULL | Chiave naturale numerica della tabella |
| COD_TIPO_SCADENZARIO | VARCHAR2 (2 CHAR) NOT NULL | Determina il tipo di scadenza alla quale fare riferimento. Deriva da dominio e può assumere i seguenti valori: DETENZIONE DOMICILIARE SPECIALE DIFFERIMENTO PENA
FINE PENA
FINE PENA CONVERTITA INGIUNZIONE DEMOLIZIONE IRREVOCABILITA' ORDINANZA IRREVOCABILITA' ORDINANZA GE
LEGGE SIMEONE MISURE SICUREZZA RATEIZZAZIONI SOLLECITO ORDINANZA
ESTINZIONE PENA
SOSPENSIONE ESECUZIONE DPR 309/90 VANE RICERCHE |
| DATA_INIZIO_SCADENZA | DATE NOT NULL | Data dalla quale far partire il conto alla rovescia |
| DATA_FINE_SCADENZA | DATE | Data termine per la quale emettere una segnalazione. |
| FLAG_VISTO | VARCHAR2 (1 CHAR) DEFAULT 'N | Poiché spesso le scadenze non riguardano solo l'ufficio emittente dell'evento questo flag indica se la segnalazione di scadenza è stata considerata o meno. |
| DATA_VISTO | DATE | Data di presa in carico di una segnalazione di scadenza |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMEN TO | VARCHAR2 (100 CHAR | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL | Identificativo del fascicolo SIEP |
| NOT_ID_NOTIFICA | NUMBER | Identificativo della notifica |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| COD_STATO_NOTIFICA | VARCHAR2 (2 CHAR) DEFAULT 'N'. | Stato della notifica |
| RIF_FASC_SIEP_ORIG | NUMBER | Identificativo del fascicolo SIEP di riferimento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| SCA_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |
| SCA_SIE_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| SCA_SIE_NOT_FK | NOT_ID_NOTIFICA | (NOTIFICA.ID_NOTIFICA) |

# SCADENZARIO_SIGE
tabella contenente i dati relativi allo scadenzario sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SCADENZARIO_SIGE | NUMBER NOT NULL | Chiave numerica della tabella. |
| COD_TIPO_SCADENZARIO | VARCHAR2 (2 CHAR) NOT NULL | Determina il tipo di scadenza alla quale fare riferimento. Deriva da dominio e può assumere i seguenti valori: IRREVOCABILITA' PROVVEDIMENTO SIGE |
| DATA_INIZIO_SCADENZA | DATE NOT NULL | Data dalla quale far partire il conto alla rovescia |
| DATA_FINE_SCADENZA | DATE | Data termine per la quale emettere una segnalazione. |
| FLAG_VISTO | VARCHAR2 (1 CHAR) | Poiché spesso le scadenze non riguardano solo l'ufficio emittente dell'evento questo flag indica se la segnalazione di scadenza è stata considerata o meno. |
| DATA_VISTO | DATE | Data di presa in carico di una segnalazione di scadenza. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_ID_FASCICOLO_SIGE | NUMBER NOT NULL | Identificativo del fascicolo SIGE |
| EVE_ID_EVENTO. | NUMBER | Identificativo dell’evento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| SCA_FAS_SIGE_FK | FAS_ID_FASCICOLO_SIGE | (FASCICOLO_SIGE.ID_FASCICOLO_SIGE) |
| SCA_SIGE_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |





# SCADENZARIO_SIUS
tabella contenente i dati relativi allo scadenzario dei fascicolo sius. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SCADENZARIO_SIUS | NUMBER NOT NULL | Chiave primaria numerica naturale della tabella. |
| COD_TIPO_SCADENZARIO | VARCHAR2 (2 CHAR)  NOT NULL | Indica la tipologia di scadenzario. Deriva da dominio e vale: DETENZIONE DOMICILIARE SPECIALE
DIFFERIMENTO PENA FINE PENA
FINE PENA CONVERTITA INGIUNZIONE DEMOLIZIONE IRREVOCABILITA' ORDINANZA
IRREVOCABILITA' ORDINANZA GE LEGGE SIMEONE
MISURE SICUREZZA RATEIZZAZIONI
SOLLECITO ORDINANZA ESTINZIONE PENA
SOSPENSIONE ESECUZIONE DPR 309/90 VANE RICERCHE |
| DATA_INIZIO_SCADENZA | DATE NOT NULL | Data di riferimento per l'inizio di una scadenza |
| DATA_FINE_SCADENZA | DATE | Data di riferimento per il termine di una scadenza |
| FLAG_VISTO | VARCHAR2 (1 CHAR) | Flag che indica se una scadenza è stata rispettata o è ancora in attesa di essere rispettata |
| DATA_VISTO | DATE | Data in cui una scadenza è stata rispettata |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER NOT NULL | Identificativo del fascicolo SIUS |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| SCA_FAS_SIUS_FK | FAS_ID_FASCICOLO_SIUS | (FASCICOLO_SIGE.ID_FASCICOLO_SIUS) |
| SCA_SIUS_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |


# SCAMBIO_SANZIONE
tabella contenente i dati relativi allo scambio della sanzione. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SCAMBIO_SANZIONE | NUMBER NOT NULL | Identificativo della sanzione |
| COD_TIPO_DECISIONE | VARCHAR2 (4 CHAR) | Tipo della decisione |
| COD_NATURA_SANZIONE | VARCHAR2 (4 CHAR) | Natura della sanzione |
| COD_TIPO_SANZIONE | VARCHAR2 (4 CHAR) | Tipo della sanzione |
| DATA_INIZIO | DATE | Data inizio sanzione |
| DATA_FINE | DATE | Data fine sanzione |
| NOTE | VARCHAR2 (2000 CHAR) | Note |
| ANNO_REGISTRO | NUMBER | Anno del registro |
| NUMERO_REGISTRO | NUMBER | Numero del registro |
| CHIAVE_ANNO_FASCICOLO_SIUS | NUMBER | Anno del fascicolo SIUS |
| CHIAVE_PROGR_FASCICOLO_SIUS | NUMBER | Numero del fascicolo SIUS |
| COD_UFFICIO_SORVEGLIANZA | VARCHAR2 (11 CHAR) | Codice dell’ufficio di sorveglianza |
| COD_UFFICIO_EMITTENTE | VARCHAR2 (11 CHAR) | Codice dell’ufficio emittente |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| DATA_EMISSIONE | DATE | Data di emissione |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| NUM_GIORNI_RECLUSIONE | NUMBER | Numero di giorni di reclusione |
| NUM_MESI_RECLUSIONE | NUMBER | Numero di mesi di reclusione |
| NUM_ANNI_RECLUSIONE | NUMBER | Numero di anni di reclusione |
| NUM_GIORNI_ARRESTO | NUMBER | Numero di giorni di arresto |
| NUM_MESI_ARRESTO | NUMBER | Numero di mesi di arresto |
| NUM_ANNI_ARRESTO | NUMBER | Numero di anni di arresto |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| EVE_ID_EVENTO_SCAM_SANZ_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |

# SEDE_GIUDIZIARIA
tabella contenente i dati relativi alla sede giudiziaria. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_SEDE_GIUDIZIARIA | VARCHAR2 (3 CHAR) | Codice fornita da file esterno (re.ge) delle sedi giudiziarie |
| DESCRIZIONE | VARCHAR2 (200 CHAR) | Descrizione della sede giudiziaria corrispondente alle descrizioni dei comuni |
| DATA_CARICAMENTO_REGE | DATE | Data di caricamento del file da Re.Ge |
| COD_COMUNE | VARCHAR2 (6 CHAR) | Codice corrispondente alla descrizione della sede giudiziaria |



# SENTENZA
tabella contenente i dati relativi alla sentenza. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SENTENZA | NUMBER NOT NULL | Chiave numerica gestita da Sequence: SEN_SEQ |
| COD_TIPO_PROVVEDIMENTO | VARCHAR2 (2 CHAR) NOT NULL | Identifica la tipologia di provvedimento che verrà iscritta nel fascicolo. Deriva da dominio. Assume i seguenti valori: Sentenza Decreto Penale |
| ANNO_REGE_PM | NUMBER | Compone la chiave del numero di registro generale delle notizie di reato (procura) |
| NUMERO_REGE_PM | VARCHAR2 (8 CHAR) | Compone la chiave del numero di registro generale delle notizie di reato (procura) |
| DATA_ARRIVO_ATTO | DATE | Data di arrivo c/o (Uff. Esecuzione) |
| DATA_PROVVEDIMENTO | DATE NOT NULL | Equivale alla data iscrizione sentenza |
| COD_TIPO_AUTORITA_EMITTENTE | VARCHAR2 (6 CHAR) NOT NULL | L'ufficio che ha emesso la sentenza (tribunale corte d'appello ecc.). Deriva da dominio. Selezionare per "TIPO_UFFICIO" |
| COD_LUOGO_EMITTENTE | VARCHAR2 (6 CHAR) NOT NULL | La sede dell'autorità che ha emesso la sentenza. Fa riferimento alla tabella di dominio COMUNE |
| NUM_SEZIONE_AUTORITA_EMITTENTE | VARCHAR2 (100 CHAR) | Valore significativo per quelle autorità di cognizione per cui sono previste più sezioni nell'ambito dello stesso ufficio |
| ANNO_SENTENZA | NUMBER | Compone la chiave del numero di sentenza |
| NUMERO_SENTENZA | VARCHAR2 (8 CHAR) | Compone la chiave del numero univoco che identifica una sentenza. |
| DATA_IRREVOCABILITA | DATE | Data del passaggio in giudicato della sentenza |
| FLAG_SENTENZA_APPLICAZ_PENA | VARCHAR2 (1 CHAR) | S/N Applicazione della pena |
| COD_TIPO_PROVV_RIF | VARCHAR2 (2 CHAR) | Deriva da dominio vale: C conferma R riforma
Ha significato solo per le sentenze in cui l'autorità di cognizione è la corte d'appello che ha confermato o riformato la sentenza di 1° grado. |
| DATA_PROVV_RIF | DATE | Data in cui è emesso il provvedimento di appello |
| COD_TIPO_AUTORITA_PROVV_RIF | VARCHAR2 (6 CHAR) | Tipo di autorità del provvedimenti di riferimento |
| ANNO_PROVV_RIF | NUMBER | Anno del provvedimento di riferimento |
| NUMERO_PROVV_RIF | VARCHAR2 (8 CHAR) | Numero del provvedimento di riferimento |
| COD_LUOGO_PROVV_RIF | VARCHAR2 (6 CHAR) | Fa riferimento alla tabella di dominio COMUNE |
| NUM_SEZIONE_AUTORITA_PROVV_RIF | VARCHAR2 (200 CHAR) | Numero della sezione dell’autorità del provvedimento di  
 riferimento |
| COD_TIPO_DECISIONE_CASSAZIO NE | VARCHAR2 (2 CHAR) | Definito in dominio. Acquisito da RE.GE
Es. Inammissibilità Rigetta Annulla Parzialmente ecc. |
| NOTE1_DECISIONE_CASSAZIONE | VARCHAR2 (500 CHAR) | Note della decisione della cassazione |
| NOTE2_DECISIONE_CASSAZIONE | VARCHAR2 (500 CHAR) | Note della decisione della cassazione |
| ANNO_SENTENZA_CASSAZIONE | NUMBER | Anno di sentenza della cassazione |
| NUMERO_SENTENZA_CASSAZIONE | VARCHAR2 (8 CHAR) | Numero di sentenza della cassazione |
| ANNO_RACCOLTA_GENERALE | NUMBER | Anno della raccolta generale |
| NUMERO_RACCOLTA_GENERALE | VARCHAR2 (8 CHAR) | Numero della raccolta generale. |
| FLAG_ALTRE_SENTENZE | VARCHAR2 (1 CHAR) | Indica o meno se la sentenza fa riferimento ad altre sentenze.
Campo presente in RES e per ora utilizzato al solo scopo di mantenere coerenza con i dati migrati. |
| DESCR_ALTRE_SENTENZE | VARCHAR2 (200 CHAR) | Riporta in forma libera le eventuali altre sentenze presenti. Campo presente in RES e per ora utilizzato al solo scopo di mantenere coerenza con i dati migrati. |
| ANNO_REGISTRO_35 | NUMBER | Parte della chiave dell'attuale registro 35. |
| NUM_REGISTRO_35 | VARCHAR2 (10 CHAR) | Parte della chiave dell'attuale registro 35. |
| NOTE | VARCHAR2 (2000 CHAR) | Note. |
| DESCR_NUM_CAMPIONE_PENALE | VARCHAR2 (2000 CHAR) | Descrizione del numero di campione penale. |
| ANNO_REGE_GIP | NUMBER | Compone la chiave del numero di registro del fascicolo presso il GIP. |
| NUMERO_REGE_GIP | VARCHAR2 (8 CHAR) | Compone la chiave del numero di registro del fascicolo presso il GIP. |
| ANNO_REGE_DIB | NUMBER | Compone la chiave del numero di registro del fascicolo presso il Tribunale di 1° Grado. |
| NUMERO_REGE_DIB | VARCHAR2 (8 CHAR) | Compone la chiave del numero di registro del fascicolo presso il Tribunale di 1° Grado. |
| ANNO_REGE_CAS | NUMBER | Compone la chiave del numero di registro del fascicolo presso la Corte d'Assise. |
| NUMERO_REGE_CAS | VARCHAR2 (8 CHAR) | Compone la chiave del numero di registro del fascicolo presso la Corte d'Assise. |
| ANNO_REGE_CAP | NUMBER | Compone la chiave del numero di registro del fascicolo presso la Corte d'Appello. |
| NUMERO_REGE_CAP | VARCHAR2 (8 CHAR) | Compone la chiave del numero di registro del fascicolo presso la Corte d'Appello. |
| ANNO_REGE_CASAP | NUMBER | Compone la chiave del numero di registro del fascicolo presso la Corte di Assise d'Appello. |
| NUMERO_REGE_CASAP | VARCHAR2 (8 CHAR) | Compone la chiave del numero di registro del fascicolo presso la Corte di Assise d'Appello. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record. |
| DATA_INSERIMENTO | DATE | Data di inserimento del record. |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record. |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record. |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record. |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record. |
| FLAG_GIUDIZIO_ABBREVIATO | VARCHAR2 (1 CHAR) | Flag indicante la presenza o meno di rito abbreviato. |
| COD_BILANCIAMENTO_CIRCOSTANZE | VARCHAR2 (1 CHAR) | Campo indicante la presenza e la tipologia di circostanze di più o meno pari peso penale. Deriva da dominio e può assumere i seguenti valori:
EQUIVALENTI PREVALENTI MINUSVALENTI. |
| FLAG_MIGRATO | VARCHAR2 (1 CHAR) DEFAULT 'N' | Flag che indica l'eventuale provenienza da migrazione. Associato al dominio FLAG_SI_NO di CG_REF_CODES. |
| COD_TIPO_RITO | CHAR(1 CHAR) | Tipo del rito. |
| DATA_ISCRIZIONE | DATE | Data di iscrizione della sentenza. |
| COD_TIPO_PROVVEDIMENTO_RIF | VARCHAR2 (2 CHAR) | Tipo di provvedimento di riferimento. |
| COD_TIPO_PROVVEDIMENTO_ALTRO | VARCHAR2 (2 CHAR) | Tipo di altro provvedimento. |
| COD_SEDE_NOTIZIA_REATO | VARCHAR2 (11 CHAR). | Sede della notizia  di reato. |
| FLAG_VISIBILITA | VARCHAR2 (1 CHAR) | Indica i Titoli Esecutivi appartenenti ad un Fascicolo di Cumulo e non collegati a Procedimenti SIEP. |
| NUMERO_PROVVEDIMENTO | VARCHAR2 (8 CHAR) | Indica il numero del provvedimento. |
| ANNO_PROVVEDIMENTO | NUMBER(4) | Indica l’anno del provvedimento. |
| ANNO_REGE_GUP | NUMBER(4) | Indica anno rege GUP. |
| NUMERO_REGE_GUP | VARCHAR2 (8 CHAR) | Indica il numero rege GUP. |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| ALTRI_GRADI_GIUDIZIO | AGDG_SEN_FK | SEN_ID_SENTENZA |
| FASCICOLO_SIEP | FAS_SIE_SEN_FK | SEN_ID_SENTENZA |
| FAS_SIGE_SENTENZA | FAS_SIGE_SEN_FK | SEN_ID_SENTENZA |
| TENORE_SENTENZA_REATO | SENTENZA_FK | SEN_ID_SENTENZA |
| SENTENZA_RIUNITA | SEN_RIU_SEN_FK | SEN_ID_SENTENZA |


# SENTENZA_RIUNITA
tabella contenente i dati relativi alla sentenza riunita. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SENTENZA_RIUNITA | NUMBER NOT NULL | Chiave numerica gestita da Sequence: SEN_RIU_SEQ |
| DATA_SENTENZA | DATE | Data sentenza di primo grado |
| ANNO_SENTENZA | NUMBER | anno della sentenza di primo grado |
| NUMERO_SENTENZA | VARCHAR2 (6 CHAR) | numero sentenza di primo grado |
| COD_TIPO_AUTORITA_EMITTENTE | VARCHAR2 (6 CHAR) | Tipo autorità che ha emesso la sentenza di primo grado |
| COD_AUTORITA_EMITTENTE | VARCHAR2 (11 CHAR) | Autorità che ha emesso la sentenza di primo grado |
| COD_LUOGO_EMITTENTE | VARCHAR2 (6 CHAR) | Codice comune del luogo autorità emittente |
| SEZIONE_AUTORITA_EMITTENTE | VARCHAR2 (100 CHAR) | Sezione autorità emittente |
| ANNO_REGE_PM | NUMBER | Anno registro PM |
| NUMERO_REGE_PM | VARCHAR2 (6 CHAR) | Numero registro PM |
| ANNO_REGE_GIP | NUMBER | Anno registro GIP |
| NUMERO_REGE_GIP | VARCHAR2 (6 CHAR) | Numero registro GIP |
| ANNO_REGE_DIB | NUMBER | Anno registro dibattimento |
| NUMERO_REGE_DIB | VARCHAR2 (6 CHAR) | Numero registro dibattimento |
| ANNO_REGE_CAS | NUMBER | Anno registro Corte Assise |
| NUMERO_REGE_CAS | VARCHAR2 (6 CHAR) | Numero registro Corte Assise |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| SEN_ID_SENTENZA | NUMBER NOT NULL | Identificativo della sentenza |
| COD_SEDE_NOTIZIA_REATO | VARCHAR2 (11 CHAR) | Sede della notizia di reato |



Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| SEN_RIU_SEN_FK | SEN_ID_SENTENZA | (SENTENZA.ID_SENTENZA) |


# SENTENZARIUNITA_FASC_SIEP
tabella associativa relativa alla tabella sentenza_riunita e fascicolo_siep. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SENTENZARIUNITA_FASC_SIEP | NUMBER NOT NULL |  |
| SEN_RIU_ID_SENTENZA_RIUNITA | NUMBER NOT NULL |  |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL |  |


# SEZIONE
tabella contenente i dati relativi alla sezione. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SEZIONE | NUMBER NOT NULL | ID sezione |
| CODICE | VARCHAR2 (4 CHAR) NOT NULL | Codice della Sezione |
| DESCRIZIONE | VARCHAR2 (200 CHAR) NOT NULL | Descrizione della sezione |
| COD_UFFICIO_APPARTENENZA | VARCHAR2 (11 CHAR) NOT NULL | Ufficio di appartenenza |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| FASCICOLO_SIGE | FAS_SIG_SEZ | SEZ_ID_SEZIONE |
| MAGISTRATO_SEZIONE | MAG_SEZ_SEZ_FK | SEZ_ID_SEZIONE |
| AULA_UDIENZA | SEZIONE_ID_SEZIONE | ID_SEZIONE |




# SOGGETTO
tabella contenente i dati relativi ai dati anagrafici del soggetto. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SOGGETTO | NUMBER NOT NULL | Chiave numerica interna legata alla sequence "SOG_SEQ" che identifica univocamente un soggetto nell'ambito di una BDI distrettuale. |
| COD_FISCALE | VARCHAR2 (16 CHAR) | Codice fiscale (se presente) |
| COD_CS | VARCHAR2 (7 CHAR) | Codice relativo all’acquisizione delle impronte digitali. Codice univoco identificativo (codice attribuito dal casellario centrale di Identità del Ministero degli Interni mediante l'acquisizione delle impronte digitali)
o Il dato deve essere reso obbligatorio per gli stranieri o E' previsto in RE.GE: standard non ancora codificato
Codice di rilevazione impronte digitali Corrisponde al Codice AFIS |
| COD_AFIS | VARCHAR2 (7 CHAR) | Codice relativo all’acquisizione delle impronte digitali. Codice univoco identificativo (codice attribuito dal casellario centrale di Identità del Ministero degli Interni mediante l'acquisizione delle impronte digitali). Viene creato ogni volta che un soggetto viene fermato...
o Il dato deve essere reso obbligatorio per gli stranieri o E' previsto in RE.GE: standard non ancora codificato |
| COGNOME | VARCHAR2 (100 CHAR) NOT NULL | Cognome del Soggetto |
| NOME | VARCHAR2 (100 CHAR) NOT NULL | Nome del Soggetto |
| ANNO_NASCITA | NUMBER | Anno di nascita del soggetto. Questo dato è in alternativa con la data di nascita ed è usato quando un soggetto non fornisce una data di nascita completa ma solo l'anno |
| DATA_NASCITA | DATE | Data completa di nascita del soggetto |
| DATA_NASCITA_PRESUNTA | VARCHAR2 (1 CHAR) | E' un flag che indica se la data di nascita o l'anno di nascita inseriti sono stati confermati o meno. |
| COD_COMUNE_NASCITA | VARCHAR2 (6 CHAR) | Comune di nascita del soggetto. Per l'estero vale: "Estero" Fa riferimento alla tabella di dominio COMUNE |
| COD_PROVINCIA_NASCITA | VARCHAR2 (2 CHAR) | Codice Provincia di nascita. Per l'estero vale "ES" |
| COD_STATO_NASCITA | VARCHAR2 (3 CHAR) | Codice dello Stato di nascita del soggetto secondo la codifica Istat (comprende anche gli stati esteri) |
| DESC_COMUNE_NASCITA_ESTERO | VARCHAR2 (200 CHAR) | Attributo relativo alle informazioni del comune di nascita di un soggetto nato all'estero. E' un campo a testo libero. |
| NAZIONALITA | VARCHAR2 (3 CHAR) | Assume solo i valori: Italiana Estera (o Straniera) |
| PATERNITA | VARCHAR2 (35 CHAR) | Nome del padre. Il campo serve solo a dettagliare maggiormente un soggetto |
| COGNOME_MADRE | VARCHAR2 (35 CHAR) | Cognome da nubile della madre. Il campo serve solo a dettagliare maggiormente un soggetto |
| NOME_MADRE | VARCHAR2 (35 CHAR) | Nome della madre. Il campo serve solo a dettagliare maggiormente un Soggetto |
| SESSO | VARCHAR2 (1 CHAR) | Deiva da dominio. Sesso soggetto: M maschio
F Femmina |
| ATTO_NASCITA | VARCHAR2 (12 CHAR) | Indica il documento ufficiale registrato presso il comune di nascita di un soggetto. E' sicuramente un campo utile alla identificazione univoca di un soggetto per cui all'iscrizione di un nuovo soggetto ne dovrà essere controllata l'esistenza in BDI. |
| NOTE | VARCHAR2 (2000 CHAR) | Campo di pura descrizione aggiuntiva alle informazioni già inserite per un soggetto. |
| COD_COMUNE_CASELLARIO | VARCHAR2 (3 CHAR) | Fa riferimento alla tabella di dominio SEDE_GIUDIZIARIA ed indica il comune di riferimento del casellario in cui sono inserite le informazione del soggetto |
| FLAG_PRESENZA_FASCICOLO | VARCHAR2 (1 CHAR) | Questo flag indica se sul soggetto è stato aperto o meno un fascicolo. Serve per gestire le seguenti situazioni:
identificare tutti quei soggetti che non hanno ancora una sentenza collegata
identificare tutti quei soggetti per cui l'istanza è iscritta nella tabella ISTANZA e non trattata nella tabella EVENTO. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| MESE_NASCITA | NUMBER | Mese di nascita del soggetto |
| PROG_ANAG_RES | NUMBER | Progressivo dell’anagrafica RES |
| KEY_SOGG_NSC | NUMBER | Identificativo del soggetto NSC |
| ETA_PRESUNTA_ANNI | NUMBER(2) | Età presunta soggetto minorenne - anni |
| ETA_PRESUNTA_MESI | NUMBER(2) | Età presunta soggetto minorenne - mesi |
| DATA_NASCITA_PRESUNTA_CALC | DATE | Data nascita presunta calcolata soggetto minorenne |
| DATA_REATO_SIUS | DATE | Data commesso reato in iscrizione soggetto sius |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| ALIAS | ALI_SOG_FK | SOG_ID_SOGGETTO |
| FASCICOLO_SIEPE | FAS_SIEPE_SOG_FK | SOG_ID_SOGGETTO |
| FASCICOLO_SIEP | FAS_SIE_SOG_FK | SOG_ID_SOGGETTO |
| FASCICOLO_SIGE | FAS_SIG_SOG_FK | SOG_ID_SOGGETTO |
| FASCICOLO_SIUS | FAS_SIU_SOG_FK | SOG_ID_SOGGETTO |
| SOGGETTO_DATTILO | FK_COD_SOGGETTO | COD_SOGGETTO |
| ISTANZA | IST_SOG_FK | SOG_ID_SOGGETTO |
| NOTIFICA | NOT_1_SOG_FK | SOG_ID_SOGGETTO |
| RESIDENZA | RES_SOG_FK | SOG_ID_SOGGETTO |



# SOGGETTO_CERTIFICATO
tabella contenente i dati relativi al certificato di un soggetto. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SOGGETTO_CERTIFICATO | NUMBER NOT NULL | Identificativo della tabella |
| SOG_ID_SOGGETTO | NUMBER NOT NULL | Identificativo del soggetto |
| CERTIFICATO | BLOB | Campo che contiene il pdf del certificato del casellario |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| DATA_AGGIORNAMENTO | DATE | Codice dell’operatore che ha aggiornato il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR). | Ufficio dell’operatore che ha aggiornato il record |


# SOGGETTO_CUMULATO
tabella contenente i dati relativi ad un soggetto oggetto di un provvedimento di cumulo. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SOGGETTO_CUMULATO | NUMBER(38) | Identificativo della tabella |
| COGNOME | VARCHAR2(100) | Cognome |
| NOME | VARCHAR2(100) | Nome |
| SESSO | VARCHAR2(1) | M=maschio F=femmina |
| DATA_NASCITA | DATE | Data Nascita |
| DATA_NASCITA_PRESUNTA | VARCHAR2(1) | Valori= S o N |
| ANNO_NASCITA | NUMBER(4) | Anno di nascita |
| MESE_NASCITA | NUMBER(2) | Mese di Nascita |
| COD_COMUNE_NASCITA | VARCHAR2(6) | COMUNE.COD_COMUNE |
| COD_PROVINCIA_NASCITA | VARCHAR2(2) | Valorizzato in fase di inserimento ricavato dal comune di nascita. |
| COD_STATO_NASCITA | VARCHAR2(3) | Codice Stato Nascita |
| DESC_COMUNE_NASCITA_ESTERO | VARCHAR2(200) | Descrizione Comune Nascita Estero |
| PATERNITA | VARCHAR2(35) | Nome padre |
| COGNOME_MADRE | VARCHAR2(35) | Cognome madre |
| NOME_MADRE | VARCHAR2(35) | Nome madre |
| COD_FISCALE | VARCHAR2(16) | Codice Fiscale |
| ATTO_NASCITA | VARCHAR2(12) | Atto di Nascita |
| COD_AFIS | VARCHAR2(7) | Codice CUI |
| COD_COMUNE_CASELLARIO | VARCHAR2(3) | COMUNE.COD_SEDE_GIUDIZIARIA per i nati in Italia. Mentre per gli stranieri si utilizza casellario centrale di Roma (342) |
| NOTE | VARCHAR2(2000) | Campo Note |
| KEY_SOGG_NSC | NUMBER(38) | Chiave associativa con NSC presente sul record SOGGETTO di derivazione |
| TIT_ID_TITOLO_CUMULATO | NUMBER(38) | FK alla tabella TITOLO_CUMULATO |
| FLAG_STATO | VARCHAR2(1) | E=estratto M=modificato C=Cancellato I=Iscritto |
| MOTIVO_MODIFICA | VARCHAR2(2000) | Note inserite dall''operatore in fase di Modifica Cancellazione Iscrizione |
| ID_SOGGETTO_ORIGINE | NUMBER(38) | Eventuale ID del record SOGGETTO da cui è stato derivato questo record |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |


# SOGGETTO_DATTILO
tabella contenente i dati dattiloscopici di un soggetto. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_DATTILO | NUMBER (38) | Identificativo soggetto |
| COD_SOGGETTO | NUMBER(38) | Codice soggetto |
| DOC_TIPO | VARCHAR2(1) | Tipologia del soggetto |
| DOC_NOME | VARCHAR2(50) | Nome del documento |
| DATA_INSERIMENTO | DATE | Data inserimento |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Utente che ha effettuato l’inserimento |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11) | Ufficio che ha effettuato l’inserimento |
| DOC_BLOB | BLOB | Contiene il documento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| FK_COD_SOGGETTO | COD_SOGGETTO | (SOGGETTO.ID_SOGGETTO) |



# SOLLECITO_ESITO_TRASMISSIONE
tabella contenente i dati relativi all’esito del sollecito effettuato ad un ufficio. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SOLLECITO | NUMBER(38) NOT NULL | Identificativo del sollecito |
| COD_UFF_SOLLECITATO | VARCHAR2(11 CHAR) NOT NULL | Codice dell’ufficio sollecitato |
| OGGETTO_MS_SOLLECITO | VARCHAR2(5 CHAR) NOT NULL | Oggetto della MS oggetto del sollecito |
| OGGETTO_MS_SOLLECITATO | VARCHAR2(5 CHAR) | Oggetto della MS sollecitata |
| DATA_INVIO_MS_SOLLECITATO | DATE | Data invio della MS sollecitata |
| MES_ID_MESSAGGIO_SOLLECITATO | NUMBER(38) | Identificativo del messaggio sollecitato |
| COD_UFF_INOLTRANTE | VARCHAR2(11 CHAR) | Codice dell’ufficio che ha inoltrato il sollecito |
| DATA_INOLTRO | DATE | Data di inoltro |
| MES_ID_MESSAGGIO_INOLTRO | NUMBER(38) | Identificato del messaggio inoltrato |
| EVE_ID_EVENTO | NUMBER(38) NOT NULL | Identificativo dell’evento |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER(38) NOT NULL | Identificativo del fascicolo SIEP |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100 CHAR) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11 CHAR) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100 CHAR) | Codice Utente ultimo aggiornamento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| SOLL_ESITO_TRASMISS_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| SOLL_ESITO_TRASMISS_FASSIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |



# SOSPENSIONE
tabella contenente i dati relativi alla sospensione. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SOSPENSIONE | NUMBER NOT NULL | Chiave numerica naturale per la gestione dei dati nella tabella |
| DATA_INIZIO | DATE | Data dalla quale inizia l'interruzione della pena |
| DATA_FINE | DATE | Data alla quale termina l'interruzione della pena |
| NUM_ANNI_RINVIO | NUMBER | Eventuale periodo espresso in anni dell'interruzione della pena |
| NUM_MESI_RINVIO | NUMBER | Eventuale periodo espresso in mesi dell'interruzione della pena |
| NUM_GIORNI_RINVIO | NUMBER | Eventuale periodo espresso in giorni dell'interruzione della pena |
| PEN_RES_ID_PENA_RESIDUA | NUMBER | Identificativo della pena residua |
| NUM_ANNI_PENA_ESPIATA | NUMBER | Numero di anni della pena espiata |
| NUM_MESI_PENA_ESPIATA | NUMBER | Numero di mesi della pena espiata |
| NUM_GIORNI_PENA_ESPIATA | NUMBER | Numero di giorni della pena espiata |
| NUM_ANNI_PENA_RESIDUA_RECLUS | NUMBER | Numero di anni della pena residua della reclusione |
| NUM_MESI_PENA_RESIDUA_RECLUS | NUMBER | Numero di mesi della pena residua della reclusione |
| NUM_GIORNI_PENA_RESIDUA_RECLUS | NUMBER | Numero di giorni della pena residua della reclusione |
| NUM_ANNI_PENA_RESIDUA_ARRES | NUMBER | Numero di anni della pena residua dell’arresto |
| NUM_MESI_PENA_RESIDUA_ARRES | NUMBER | Numero di mesi della pena residua dell’arresto |
| NUM_GIORNI_PENA_RESIDUA_ARRES | NUMBER | Numero di giorni della pena residua dell’arresto |
| NUM_ANNI_INTERRUZIONE | NUMBER | Numero di anni di interruzione |
| NUM_MESI_INTERRUZIONE | NUMBER | Numero di mesi di interruzione |
| NUM_GIORNI_INTERRUZIONE | NUMBER | Numero di giorni di interruzione |
| MULTA_ESPIATA | NUMBER (2-16) | Importo della multa espiata |
| AMMENDA_ESPIATA | NUMBER (2-16) | Importo dell’ammenda espiata |
| MULTA_RESIDUA | NUMBER (2-16) | Importo della multa residua |
| AMMENDA_RESIDUA | NUMBER (2-16) | Importo dell’ammenda residua |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| FLAG_INTERRUZIONE | VARCHAR2 (1 CHAR) | S/N interruzione della sospensione |
| NUM_GIORNI_LIBANTICIPATA | NUMBER | Numero di giorni della liberazione anticipata |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| SOS_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |
| SOS_PEN_RES_FK | PEN_RES_ID_PENA_RESIDUA | (PENA_RESIDUA.ID_PENA_RESIDUA) |


# STAMPA_DOCUMENTI
tabella contenente i dati relativi all’utente che ha effettuato una stampa. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_STAMPA | NUMBER NOT NULL | Identificativo della tabella |
| ID_UTENTE | VARCHAR2 (60 CHAR) NOT NULL | Codice dell’utente che ha stampato il documento |
| DATA | DATE NOT NULL | Data di stampa del documento |
| STATO | VARCHAR2 (2 CHAR) | Stato della stampa |
| NUM_STAMPE_RICHIESTE | NUMBER | Numero delle stampe richieste |
| NUM_STAMPE_EFFETTUATE | NUMBER | Numero delle stampe effettuate |
| DOC_BLOB | BLOB | Campo che contiene il documento stampato |
| DESCRIZIONE | VARCHAR2 (1000 CHAR). | Descrizione del documento stampato |


# STATO_ESEC_TITOLO_CUMULATO
tabella contenente i dati relativi allo Stato Esecuzione del Titolo Cumulato.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_STATO_ESEC_TITOLO_CUMULATO | NUMBER(38) | Sequence |
| COD_TIPO_EVENTO | VARCHAR2(2) | CG_REF_CODES.RV_DOMAIN= ’TIPO_EVENTO’ |
| COD_TIPO_PROVVEDIMENTO | VARCHAR2(2) | CG_REF_CODES.RV_DOMAIN= ’TIPO_PROVVEDIMENTO’ |
| COD_MOTIVO | VARCHAR2(4) | CG_REF_CODES.RV_DOMAIN= ’MOTIVO_PROVVEDIMENTO’ |
| COD_MOTIVO_REVOCA | VARCHAR2(4) | CG_REF_CODES.RV_DOMAIN= ’REVOCA_DECSOSP’ |
| COD_MOTIVO_REVOCA_PM | VARCHAR2(4) | CG_REF_CODES.RV_DOMAIN= ’REVOCA_DECSOSP’ |
| COD_UFFICIO_EMITTENTE | VARCHAR2(11) | Codice Ufficio emittente provvedimento |
| COD_AUTORITA_EMITTENTE | VARCHAR2(2) | CG_REF_CODES.RV_DOMAIN= ’TIPO_AUTORITA’ |
| COD_LUOGO_EMITTENTE | VARCHAR2(6) | COD_COMUNE del luogo autorità emittente |
| DATA_EMISSIONE | DATE | Data emissione provvedimento |
| COD_ESITO | VARCHAR2(4) | CG_REF_CODES.RV_DOMAIN= ‘ESITO_PROVVEDIMENTO’ |
| COD_ESITO_TENORE | VARCHAR2(4) | CG_REF_CODES.RV_DOMAIN= ‘ESITO_PROVVEDIMENTO’ |
| ANNO_PROCEDIMENTO | NUMBER(4) | Anno del procedimento dell’Ufficio emittente |
| PROGR_PROCEDIMENTO | NUMBER(38) | Numero del procedimento dell’Ufficio emittente |
| ANNO_PROVVEDIMENTO | NUMBER(4) | Anno del provvedimento |
| PROGR_PROVVEDIMENTO | NUMBER(38) | Numero del provvedimento |
| NOTE | VARCHAR2(2000) | Eventuale campo note |
| COD_CONTENUTO_ISTANZA | VARCHAR2(4) | CG_REF_CODES.RV_DOMAIN= ‘CONTENUTO_ISTANZA’ |
| DATA_ISTANZA | DATE | Data dell’istanza |
| FLAG_ISTANZA_PRESDEP | VARCHAR2(1) | CG_REF_CODES.RV_DOMAIN= ‘FLAG_ISTANZA_PD’ |
| COD_STATO_ISTANZA | NUMBER(2) | CG_REF_CODES.RV_DOMAIN= ‘STATO_ISTANZA’ |
| FLAG_TIPO_SOSP | VARCHAR2(3) | CG_REF_CODES.RV_DOMAIN= ‘TIPO_SOSPENSIONE’ |
| COD_TIPO_UFFICIO_DESTINATARIO | VARCHAR2(10) | CG_REF_CODES.RV_DOMAIN= ‘TIPO_UFFICIO’ |
| COD_LUOGO_DESTINATARIO | VARCHAR2(6) | COD_COMUNE del luogo ufficio destinatario |
| COD_UFFICIO_DESTINATARIO | VARCHAR2(11) | COD_UFFICIO dell’Ufficio destinatario |
| DATA_TRASMISSIONE | DATE | Data Trasmissione |
| COD_TIPO_ISTANTE | VARCHAR2(1) | Tipo istante |
| COD_TIPO_UFFICIO_ALTRO | VARCHAR2(7) | CG_REF_CODES.RV_DOMAIN= ‘TIPO_UFFICIO’ |
| COD_TIPO_AUTORITA_ALTRO | VARCHAR2(2) | CG_REF_CODES.RV_DOMAIN= ’TIPO_AUTORITA’ |
| COD_LUOGO_ALTRO | VARCHAR2(6) | COD_COMUNE del luogo ufficio destinatario |
| COD_UFFICIO_ALTRO | VARCHAR2(11) | COD_UFFICIO dell’Ufficio destinatario |
| SEZIONE_ALTRO | VARCHAR2(100) | Descrizione Sezione |
| DATA_EMISSIONE_ALTRO | DATE | Data emissione |
| TIT_ID_TITOLO_CUMULATO | NUMBER(38) | FK alla tabella TITOLO_CUMULATO |
| ISTR_ID_ISTRUTTORIA_CUMULO | NUMBER(38) | FK alla tabella ISTRUTTORIA_CUMULO |
| FLAG_STATO | VARCHAR2(1) | E=estratto, M=modificato, C=Cancellato, I=Iscritto |
| MOTIVO_MODIFICA | VARCHAR2(2000) | Eventuale descrizione motivo modifica |
| ID_EVENTO_ORIGINE | NUMBER(38) | ID dell’EVENTO da cui è originato |
| EVE_ID_EVENTO_ORIGINE | NUMBER(38) | EVE_ID_EVENTO dell’EVENTO da cui è originato |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100) | Codice Utente di Iscrizione |
| DATA_INSERIMENTO | DATE | Data di Iscrizione |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11) | Codice Ufficio Utente di Iscrizione |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100) | Codice Utente ultimo aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data ultimo aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice Ufficio Utente ultimo aggiornamento |


# STATO_ESECUZIONE_PROCEDIMENTO
tabella contenente i dati relativi allo stato di esecuzione del procedimento. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_TIPO_PROVVEDIMENTO | VARCHAR2 (2 CHAR) | Tipo del provvedimento |
| COD_MOTIVO | VARCHAR2 (4 CHAR) | Codice del motivo |
| COD_STATO_PROCEDIMENTO | VARCHAR2 (4 CHAR) | Codice dello stato del procedimento |
| COD_STATO_FASCICOLO_RES | VARCHAR2 (3 CHAR) | Stato del fascicolo RES |
| COD_POSIZIONE_GIURIDICA | VARCHAR2 (3 CHAR). | Codice della posizione giuridica |




# STATO_FASCICOLO_RES
tabella contenente i dati relativi allo stato del fascicolo res. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_STATO_FASCICOLO | NUMBER NOT NULL | Stato del fascicolo |
| DESCRIZIONE | VARCHAR2(300 CHAR) | Descrizione dello stato del fascicolo |
| ORDINAMENTO | INTEGER | Ordinamento |
| TIPO_CAMPO | VARCHAR2(2 CHAR) | Tipo di campo |
| T1 | NUMBER | - |
| T2 | NUMBER | - |
| VIS_CPP | VARCHAR2(3 CHAR) | - |


# STATO_FASCICOLO_RES_MS
tabella contenente i dati relativi allo stato del fascicolo res per le misure di sicurezza. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_STATO_FASCICOLO | NUMBER NOT NULL | Codice dello Stato del fascicolo. |
| DESCRIZIONE | VARCHAR2(300 CHAR) | Descrizione dello stato del fascicolo. |
| ORDINAMENTO | INTEGER | Ordinamento. |
| TIPO_CAMPO | VARCHAR2(2 CHAR) | Tipo di campo. |
| T1 | NUMBER | Primo Intervallo temporale. |
| T2 | NUMBER | Secondo Intervallo temporale. |



# STATO_PRENOTAZIONI_BDMC
tabella contenente i dati relativi allo stato della prenotazione della bdmc. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| STATO_PRENOTAZIONI_BDMC | NUMBER NOT NULL | Stato della prenotazione |
| ID_MISURA_CAUTELARE_BDMC | NUMBER NOT NULL | Identificativo della misura cautelare |
| DATA_TRASMISSIONE | DATE | Data di trasmissione |
| ESITO_ID | NUMBER | Identificativo dell’esito |
| ESITO_MSG | VARCHAR2 (1000 CHAR) | Descrizione dell’esito del messaggio |
| ID_PRENOTAZIONE | NUMBER | Identificativo della prenotazione |
| PROG_PERI_PRES | NUMBER | Progressivo |
| TIPO_TRASMISSIONE | VARCHAR2 (1 CHAR). | Tipo di trasmissione |




# STATO_PROCEDIMENTO
tabella contenente i dati relativi allo stato di un procedimento siep relativamente ad un evento. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| PROGRESSIVO | NUMBER NOT NULL | Progressivo riga per la gestione dello stato del procedimento. |
| COD_STATO_PROCEDIMENTO | VARCHAR2 (4 CHAR) DEFAULT '-' | Codifica dello stato procedimento. |
| DATA | DATE | Data stato procedimento. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER NOT NULL | Identificativo del fascicolo SIEP |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| EVE_STATO_PROC_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| STA_PRO_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |





# STORICO_AVVOCATO
tabella contenente i dati relativi allo storico degli avvocati. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_STORICO_AVVOCATO | NUMBER NOT NULL | Identificativo della tabella |
| COGNOME | VARCHAR2 (100 CHAR) | Cognome dell’avvocato |
| NOME | VARCHAR2 (100 CHAR) | Nome dell’avvocato |
| FORO | VARCHAR2 (100 CHAR) | Foro di appartenenza dell’avvocato |
| INDIRIZZO | VARCHAR2 (300 CHAR) | Indirizzo dell’avvocato |
| TELEFONO | VARCHAR2 (20 CHAR) | Numero di telefono dell’avvocato |
| FAX | VARCHAR2 (20 CHAR) | Numero di fax dell’avvocato |
| E_MAIL | VARCHAR2 (200 CHAR) | Indirizzo email dell’avvocato |
| COD_COMUNE_RESIDENZA | VARCHAR2 (6 CHAR) | Codice del comune di residenza dell’avvocato |
| COD_LUOGO_NASCITA | VARCHAR2 (6 CHAR) | Luogo di nascita dell’avvocato |
| DATA_NASCITA | DATE | Data di nascita dell’avvocato |
| DATA_SOSPESO_FINO_AL | DATE | Data di sospensione dell’avvocato |
| DATA_RADIATO_DAL | DATE | Data di radiazione dell’avvocato |
| COD_NON_ATTIVITA | VARCHAR2 (4 CHAR) | Codice di inattività |
| NOTE | VARCHAR2 (2000 CHAR) | Note |
| COD_UFFICIO_APPARTENENZA | VARCHAR2 (11 CHAR) | Ufficio di appartenenza dell’avvocato |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| AVV_ID_AVVOCATO | NUMBER | Identificativo della tabella avvocato |
| FLAG_CANCELLATO | VARCHAR2 (1 CHAR) DEFAULT 'N' | S/N indica se l’avvocato è cancellato logicamente |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| COD_FISCALE | VARCHAR2 (16 CHAR) | Codice fiscale dell’ avvocato |
| PROVINCIA | VARCHAR2 (4 CHAR) | Codice della provincia |
| CAP | VARCHAR2 (6 CHAR) | CAP del comune di residenza dell’avvocato |
| ID_AVVOCATO_STANDARD | NUMBER | Identificativo dell’avvocato di default |
| FLAG_VISUALIZZA. | NUMBER | S/N Indica se l’avvocato deve essere visualizzato |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| STO_AVV_FK | AVV_ID_AVVOCATO | (AVVOCATO.ID_AVVOCATO) |


# STORICO_SOGGETTO
tabella contenente i dati relativi allo storico del soggetto. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| PROGRESSIVO_STORICO | NUMBER NOT NULL | Progressivo di variazione anagrafica nell'ambito del soggetto. |
| DATA_VARIAZIONE | DATE NOT NULL | Data di effettiva variazione dell’anagrafica del soggetto |
| ID_SOGGETTO_VARIATO | NUMBER NOT NULL | Identificativo del soggetto modificato |
| COD_FISCALE | VARCHAR2 (16 CHAR) | Codice fiscale del soggetto modificato |
| COD_CS | VARCHAR2 (7 CHAR) | Codice relativo all’acquisizione delle impronte digitali. Codice univoco identificativo (codice attribuito dal casellario centrale di Identità del Ministero degli Interni mediante l'acquisizione delle impronte digitali)
o Il dato deve essere reso obbligatorio per gli stranieri o E' previsto in RE.GE: standard non ancora codificato |
| COD_AFIS | VARCHAR2 (7 CHAR) | Codice AFIS del soggetto |
| COGNOME | VARCHAR2 (100 CHAR) | Cognome del soggetto modificato |
| NOME | VARCHAR2 (100 CHAR) | Nome del soggetto modificato |
| ANNO_NASCITA | NUMBER | Anno di nascita del soggetto modificato |
| DATA_NASCITA | DATE | Data di nascita del soggetto modificato |
| DATA_NASCITA_PRESUNTA | VARCHAR2 (1 CHAR) | Data di nascita presunta del soggetto modificato |
| COD_COMUNE_NASCITA | VARCHAR2 (6 CHAR) | Fa riferimento alla tabella di dominio COMUNE |
| COD_PROVINCIA_NASCITA | VARCHAR2 (2 CHAR) | Provincia di nascita del soggetto modificato |
| COD_STATO_NASCITA | VARCHAR2 (3 CHAR) | Stato di nascita del soggetto modificato |
| DESC_COMUNE_NASCITA_ESTERO | VARCHAR2 (200 CHAR) | Descrizione del comune estero del soggetto modificato |
| NAZIONALITA | VARCHAR2 (3 CHAR) | Nazionalità del soggetto modificato |
| PATERNITA | VARCHAR2 (35 CHAR) | Paternità del soggetto modificato |
| COGNOME_MADRE | VARCHAR2 (35 CHAR) | Cognome della madre del soggetto modificato |
| NOME_MADRE | VARCHAR2 (35 CHAR) | Nome della madre del soggetto modificato |
| SESSO | VARCHAR2 (1 CHAR) | Sesso del soggetto modificato |
| ATTO_NASCITA | VARCHAR2 (12 CHAR) | Atto di nascita del soggetto modificato |
| NOTE | VARCHAR2 (2000 CHAR) | Note |
| COD_COMUNE_CASELLARIO | VARCHAR2 (3 CHAR) | Codice del comune del Casellario |
| FLAG_PRESENZA_FASCICOLO | VARCHAR2 (1 CHAR) | S/N indica se il fascicolo è presente |
| MESE_NASCITA | NUMBER | Mese di nascita del soggetto modificato |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| ID_SOGGETTO_NUOVO | NUMBER | Identificativo del soggetto modificato |
| FAS_SIE_ID_FASCICOLO_SIUS | NUMBER | Identificativo del fascicolo SIUS |
| ETA_PRESUNTA_ANNI | NUMBER(2) | Anni dell’età presunta |
| ETA_PRESUNTA_MESI | NUMBER(2) | Mesi dell’età presunta |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| STO_SOG_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |
| STO_SOG_FAS_SIUS_FK | FAS_SIE_ID_FASCICOLO_SIUS | (FASCICOLO_SIUS.ID_FASCICOLO_SIUS) |





# TEMPLATE
tabella contenente i dati relativi ai template utilizzati per le stampe. utilizzata dal sottosistema siep-sius-sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_TEMPLATE | VARCHAR2 (25 CHAR) NOT NULL | Chiave univoca per l'identificazione di un template |
| NOME_TEMPLATE | VARCHAR2 (50 CHAR) | Nome del template |
| DESCR | VARCHAR2 (300 CHAR) | Descrizione del tipo di stampa legata al template; es. (Ordine di scarcerazione Richiesta certificato al casellario Richiesta certificato stato esecuzione ...) |
| PATH_RICERCA | VARCHAR2 (200 CHAR) | Individua il "path" fisico del file-system in cui è presente il documento riferito da NOME_TEMPLATE |
| COD_TIPO_EVENTO | VARCHAR2 (2 CHAR) | Codifica del tipo Evento relativo al documento in stampa |
| COD_TIPO_PROVVEDIMENTO | VARCHAR2 (2 CHAR) | Codifica del tipo provvedimento |
| COD_MOTIVO | VARCHAR2 (4 CHAR) | Codifica del motivo provvedimento |
| FLAG_TEMPLATE | VARCHAR2 (1 CHAR) | Serve ad identificare univocamente un template in tutti quei casi in cui a parità di chiave Evento e posizione giuridica si distingue un   template da altre informazioni |
| COD_ESITO | VARCHAR2 (4 CHAR) | Codice dell’esito |
| COD_OGGETTO_PROCEDIMENTO | VARCHAR2 (4 CHAR) | Codifica dell'Oggetto procedimento. Associato al dominio OGGETTO_PROCEDIMENTO di CG_REF_CODES |
| MAG_COD_MAGISTRATO | VARCHAR2 (6 CHAR) DEFAULT
null' | Codice Magistrato a cui è attribuito il Template |
| COD_TIPO_PROVVEDIMENTO_SIGE | VARCHAR2 (2 CHAR) | Codifica del tipo provvedimento SIGE. |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| TEM_MAG_FK | MAG_COD_MAGISTRATO | (W_MAGISTRATO.COD_MAGISTRATO) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| DOCUMENTO_ALLEGATO | DOC_ALL_TEM_FK | TEM_ID_TEMPLATE |



# TENORE
tabella contenente i dati relativi al tenore di un’ordinanza. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_TENORE | NUMBER NOT NULL | Chiave numerica interna legata alla sequence "TEN_SEQ". |
| COD_ESITO_TENORE | VARCHAR2 (4 CHAR) | Codifica dell'Esito del Tenore. |
| DATA | DATE | Data del tenore |
| COD_MAGISTRATO | VARCHAR2 (6 CHAR) | Identificativo del magistrato |
| NOTE | VARCHAR2 (2000 CHAR) | Eventuali note a corredo. |
| COD_OGGETTO_TENORE | VARCHAR2 (4 CHAR) | Fa riferimento alla tabella di dominio CG_REF_CODES con chiave "MOTIVO_PROVVEDIMENTO" |
| PROGR_TENORE | NUMBER | Progressivo del tenore. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| GEN_PRID_GENERALE_PROCEDIMENTO | NUMBER | Identificativo della tabella Generale Procedimento |
| DEP_OPID_DEPOSITO_ORDINANZA_PC | NUMBER | Identificativo della tabella ordinanza |
| IMP_ID_IMPUGNAZIONE | NUMBER | Identificativo della tabella impugnazione |
| DEP_DEC_ID_DEPOSITO_DECRETO | NUMBER | Identificativo della tabella deposito decreto |
| COD_DETTAGLIO_OGGETTO | VARCHAR2 (4 CHAR) | Codifica Del Dettaglio Motivo Provvedimento. Associato Al Dominio Dettaglio_Motivo Di Cg_Ref_Codes. |
| DATA_FINE | DATE | Data Di Fine Validità Del Tenore. |
| DEC_ID_DECRETO_ORDINANZA_SIEP | NUMBER | Identificativo della tabella decreto ordinanza |
| DEP_ID_DEPOSITO_SENTENZA | NUMBER | Identificativo della tabella deposito sentenza |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| TEN_DEP_DEC_FK | DEP_DEC_ID_DEPOSITO_DECRETO | (DEPOSITO_DECRETO.ID_DEPOSITO_DECRETO) |
| TEN_DEP_OPC_FK | DEP_OPID_DEPOSITO_ORDINANZA_PC | (DEPOSITO_ORDINANZA_PC.ID_DEPOSITO_ORDINANZA_PC) |
| TEN_DEP_SENT_FK | DEP_ID_DEPOSITO_SENTENZA | (DEPOSITO_SENTENZA.ID_DEPOSITO_SENTENZA) |
| TEN_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO | (GENERALE_PROCEDIMENTO.ID_GENERALE_PROCEDIMENTO) |


# TENORE_SENTENZA_REATO
tabella associativa tra le tabelle tenore, sentenza e reato. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| DATA_INSERIMENTO | DATE NOT NULL | Data di inserimento del record in tabella |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) NOT NULL | Codice dell’operatore che ha effettuato l’inserimento |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) NOT NULL | Codice dell’ufficio dell’operatore che ha effettuato l’inserimento |
| ID_TEN_SEN_REA | NUMBER NOT NULL | Chiave primaria della tabella |
| TEN_ID_TENORE_SIGE | NUMBER NOT NULL | Identificativo del TENORE_SIGE |
| SEN_ID_SENTENZA | NUMBER NOT NULL | Identificativo della SENTENZA |
| REA_ID_REATO | NUMBER | Identificativo del REATO |
| COD_ESITO | VARCHAR2 (4 CHAR)
DEFAULT null | Codice Esito Sige definito per lo specifico Sentenza-Reato |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha effettuato l’aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11) | Codice dell’ufficio dell’operatore che ha effettuato l’aggiornamento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| REATO_FK | REA_ID_REATO | (REATO.ID_REATO) |
| SENTENZA_FK | SEN_ID_SENTENZA | (SENTENZA.ID_SENTENZA) |
| TENORE_SIGE_FK | TEN_ID_TENORE_SIGE | (TENORE_SIGE.ID_TENORE_SIGE) |




# TENORE_SIGE
tabella contenente i dati relativi al tenore di un fascicolo sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_TENORE_SIGE | NUMBER NOT NULL | Chiave numerica interna legata alla sequence "TEN_SIGE_SEQ" |
| COD_OGGETTO_SIGE | VARCHAR2 (4 CHAR) NOT NULL | Classificazione dell'oggetto in base al dominio OGGETTO_SIGE di CG_REF_CODES |
| COD_ESITO_SIGE | VARCHAR2 (4 CHAR) DEFAULT 'NULL' | Codice dell'esito espresso sull'oggetto dell'oggetto in base al dominio ESITO_TENORE_SIGE di CG_REF_CODES |
| DATA | DATE | Data di definizione dell'oggetto |
| DATA_FINE | DATE DEFAULT 'NULL' | Data di fine validità ( storicizzazione) dell'oggetto |
| RIC_SIG_ID_RICHIESTA_SIGE | NUMBER DEFAULT NULL | ID della richiesta cui fa riferimento l'oggetto |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) NOT NULL | Codice dell’operatore che ha inserito il record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) NOT NULL | Data di inserimento del record |
| DATA_INSERIMENTO | DATE NOT NULL | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Data di aggiornamento del record |
| DATA_AGGIORNAMENTO | DATE | Ufficio dell’operatore che ha aggiornato il record |
| PROV_ID_PROVVEDIMENTO_SIGE | NUMBER DEFAULT NULL | ID di Riferimento al PROVVEDIMENTO_SIGE |
| FAS_ID_FASCICOLO_SIGE | NUMBER DEFAULT 'NULL' | ID del Fascicolo SIGE |
| NOTE | VARCHAR2 (2000 CHAR). | Ulteriore descrizione della decisione |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| FAS_ID_FASCICOLO_SIGE_FK | FAS_ID_FASCICOLO_SIGE | (FASCICOLO_SIGE.ID_FASCICOLO_SIGE) |
| PROV_ID_PROVVEDIMENTO_SIGE_FK | PROV_ID_PROVVEDIMENTO_SIGE | (PROVVEDIMENTO_SIGE.ID_PROVVEDIMENTO_SIGE) |
| TEN_SIG_RIC_SIG_FK | RIC_SIG_ID_RICHIESTA_SIGE | (RICHIESTA_SIGE.ID_RICHIESTA_SIGE) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| TENORE_SENTENZA_REATO | TENORE_SIGE_FK | TEN_ID_TENORE_SIGE |
| DATI_PROVVEDIMENTO_SIGE | TEN_ID_TEN_SIGE_FK | TEN_ID_TENORE_SIGE |

# TIPO_EVENTI_BDMC
tabella contenente i dati relativi alle tipologie di eventi per bdmc. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_TIPO_EVENTI_BDMC | NUMBER NOT NULL | Identificativo della tabella |
| COD_TIPO_EVENTO | VARCHAR2 (2 CHAR) NOT NULL | Codice del tipo di evento |
| COD_PROVVEDIMENTO | VARCHAR2 (2 CHAR) NOT NULL | Codice del provvedimento |
| COD_MOTIVO | VARCHAR2 (4 CHAR) NOT NULL. | Codice motivo |


# TIPOLOGIA_ORARIO
tabella contenente i dati relativi alla tipologia di orario per l’espletamento di una sanzione. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_TIPOLOGIA_ORARIO | NUMBER NOT NULL | Identificativo della tabella |
| COD_NUM_GIORNO | VARCHAR2 (2 CHAR) NOT NULL | Codice del numero del giorno |
| DALLE_ORE | VARCHAR2 (5 CHAR) | Inizio orario |
| ALLE_ORE | VARCHAR2 (5 CHAR) | Fine orario |
| ENTE_INCARICATO | VARCHAR2 (2000 CHAR) | Descrizione dell’ente |
| BEN_ID_BENEFICIO | NUMBER NOT NULL | Identificativo del beneficio |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR). | Ufficio dell’operatore che ha aggiornato il record |
| DAT_FIN_CUM_ULT_SANZIONI | NUMBER | Identificativo DATI_FINALI_ULTERIORI_SANZIONI |
| BEN_ID_BENEFICIO_CUMULO | NUMBER | Link al record BENEFICIO_CUMULO |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| TIP_ORA_ID_BEN_FK | BEN_ID_BENEFICIO | (BENEFICIO.ID_BENEFICIO) |




# TITOLO_CUMULATO
tabella contenente i dati relativi ad un titolo che è stato cumulato. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione | Descrizione |
| --- | --- | --- | --- |
| ID_TITOLO_CUMULATO | NUMBER(38) NOT NULL | NUMBER(38) NOT NULL | Identificativo del titolo cumulato |
| COD_TIPO_PROVVEDIMENTO | VARCHAR2(2 CHAR) NOT NULL | VARCHAR2(2 CHAR) NOT NULL | Sentenza/Decreto Penale |
| DATA_IRREVOCABILITA | DATE | DATE | Vedi FASCIOLO_SIEP.DATA_IRREVOCABILITA |
| ANNO_REGE_PM | NUMBER(4) | NUMBER(4) | Anno R.G.N.R. |
| NUMERO_REGE_PM | VARCHAR2(8 CHAR) | VARCHAR2(8 CHAR) | Numero R.G.N.R. |
| COD_SEDE_NOTIZIA_REATO | VARCHAR2(11 CHAR) | VARCHAR2(11 CHAR) | Sede R.G.N.R. |
| ANNO_REG_GEN | NUMBER(4) | NUMBER(4) | Anno Registro Generale |
| NUMERO_REG_GEN | VARCHAR2(8 CHAR) | VARCHAR2(8 CHAR) | Numero Registro Generale |
| TIPO_REG_GEN | VARCHAR2(240 CHAR) | VARCHAR2(240 CHAR) | Tipo Registro Generale (GIP DIB CAS CAP CASAP) |
| DATA_PROVVEDIMENTO | DATE NOT NULL | DATE NOT NULL | Sentenza da Eseguire - Data |
| ANNO_SENTENZA | NUMBER(4) | NUMBER(4) | Sentenza da Eseguire - Anno |
| NUMERO_SENTENZA | VARCHAR2(8 CHAR) | VARCHAR2(8 CHAR) | Sentenza da Eseguire - Numero |
| COD_TIPO_AUTORITA_EMITTENTE | VARCHAR2(6 CHAR) NOT NULL | VARCHAR2(6 CHAR) NOT NULL | Sentenza da Eseguire - Autorità Emittente |
| COD_LUOGO_EMITTENTE | VARCHAR2(6 CHAR) NOT NULL | VARCHAR2(6 CHAR) NOT NULL | Sentenza da Eseguire - Luogo |
| NUM_SEZIONE_AUTORITA_EMITTENTE | VARCHAR2(100 CHAR) | VARCHAR2(100 CHAR) | Sentenza da Eseguire - Eventuale sezione |
| COD_TIPO_RITO | CHAR(1 CHAR) | CHAR(1 CHAR) | Sentenza da Eseguire - Tipo Rito (Monocratico/Collegiale) solo per DIB e TRIBSD |
| COD_TIPO_PROVVEDIMENTO_RIF | VARCHAR2(2 CHAR) | VARCHAR2(2 CHAR) | Altro Grado di Giudizio - Sentenza/Ordinanza inammissibilità |
| COD_TIPO_PROVV_RIF | VARCHAR2(2 CHAR) | VARCHAR2(2 CHAR) | Altro Grado di Giudizio - Conferma/Riforma |
| DATA_PROVV_RIF | DATE | DATE | Altro Grado di Giudizio - Data |
| ANNO_PROVV_RIF | NUMBER(4) | NUMBER(4) | Altro Grado di Giudizio - Anno |
| NUMERO_PROVV_RIF | VARCHAR2(8 CHAR) | VARCHAR2(8 CHAR) | Altro Grado di Giudizio - Numero |
| COD_TIPO_AUTORITA_PROVV_RIF | VARCHAR2(6 CHAR) | VARCHAR2(6 CHAR) | Altro Grado di Giudizio - Tipo Autorità |
| COD_LUOGO_PROVV_RIF | VARCHAR2(6 CHAR) | VARCHAR2(6 CHAR) | Altro Grado di Giudizio - Sede Autorità |
| NUM_SEZIONE_AUTORITA_PROVV_RIF | VARCHAR2(200 CHAR) | VARCHAR2(200 CHAR) | Altro Grado di Giudizio - Eventuale sezione |
| COD_TIPO_RITO_RIF | CHAR(1 CHAR) | CHAR(1 CHAR) | Altro Grado di Giudizio - Tipo Rito (Monocratico/Collegiale) solo per DIB e TRIBSD |
| COD_TIPO_PROVVEDIMENTO_ALTRO | VARCHAR2(2 CHAR) | VARCHAR2(2 CHAR) | Decisione Cassazione - Sentenza/Ordinanza inammissibilità |
| NOTE1_DECISIONE_CASSAZIONE | VARCHAR2(500 CHAR) | VARCHAR2(500 CHAR) | Decisione Cassazione - Anno Reg. Gen. |
| NOTE2_DECISIONE_CASSAZIONE | VARCHAR2(500 CHAR) | VARCHAR2(500 CHAR) | Decisione Cassazione - Numero Reg. Gen. |
| ANNO_SENTENZA_CASSAZIONE | NUMBER(4) | NUMBER(4) | Decisione Cassazione - Anno Sentenza o anno Ordinanza |
| NUMERO_SENTENZA_CASSAZIONE | VARCHAR2(8 CHAR) | VARCHAR2(8 CHAR) | Decisione Cassazione - Numero Sentenza o Numero Ordinanza |
| ANNO_RACCOLTA_GENERALE | NUMBER(4) | NUMBER(4) | Decisione Cassazione - Anno Raccolta Generale |
| NUMERO_RACCOLTA_GENERALE | VARCHAR2(8 CHAR) | VARCHAR2(8 CHAR) | Decisione Cassazione - Numero Raccolta Generale |
| COD_TIPO_DECISIONE_CASSAZIONE | VARCHAR2(2 CHAR) | VARCHAR2(2 CHAR) | Decisione Cassazione - Dispositivo' 'E=estratto M=modificato C=Cancellato I=Iscritto' |
| NOTE | VARCHAR2(2000 CHAR) | VARCHAR2(2000 CHAR) | Note inserite dall''operatore in fase di Modifica Cancellazione Iscrizione |
| ISTR_ID_ISTRUTTORIA_CUMULO | NUMBER(38) NOT NULL | NUMBER(38) NOT NULL | Eventuale ID del record SENTENZA da cui è stato derivato questo record |
| FLAG_STATO | VARCHAR2(1 CHAR) NOT NULL | VARCHAR2(1 CHAR) NOT NULL | S/N indica se il titolo risulta momentaneamente escluso |
| MOTIVO_MODIFICA | VARCHAR2(2000 CHAR) | VARCHAR2(2000 CHAR) | Descrizione del motivo della modifica |
| ID_SENTENZA_ORIGINE | NUMBER(38) | NUMBER(38) | Identificativo della sentenza origine |
| FLAG_ESCLUSO | VARCHAR2(1 CHAR) | VARCHAR2(1 CHAR) | S/N flag esclusione |
| MESS_ID_MESSAGGIO | NUMBER(38) | NUMBER(38) | Identificativo del messaggio |
| TIPO_ISCRIZIONE | VARCHAR2(2 CHAR) | VARCHAR2(2 CHAR) | Tipologia di iscrizione |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100 CHAR) | VARCHAR2(100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11 CHAR) | VARCHAR2(11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100 CHAR) | VARCHAR2(100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(11 CHAR) | VARCHAR2(11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |


# TRASMISSIONI
tabella contenente i dati relativi alle trasmissioni dati tra nsc e sies. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_TRASMISSIONE | NUMBER NOT NULL | Identificativo della tabella |
| TIPO_TRASMISSIONE | VARCHAR2 (2 CHAR) NOT NULL | Tipologia di trasmissione |
| DATA_TRASMISSIONE | DATE NOT NULL | Data della trasmissione |
| ESITO_TRASMISSIONE | VARCHAR2 (3 CHAR) NOT NULL | Codice dell’esito della trasmissione |
| COD_ERRORE | VARCHAR2 (5 CHAR) | Codice dell’errore |
| TIPO_OPERAZIONE | VARCHAR2 (30 CHAR) NOT NULL | Tipo di operazione |
| DESTINAZIONE | VARCHAR2 (4 CHAR) NOT NULL | Destinazione della trasmissione |
| CHIAVE_SIES_SOGG | NUMBER | Identificativo del soggetto SIES |
| CHIAVE_SIES_FASC | NUMBER | Identificativo del fascicolo SIES |
| CHIAVE_NSC_SOGG | NUMBER | Identificativo del soggetto NSC |
| CHIAVE_NSC_PROV | NUMBER | Identificativo del provvedimento SIES |
| DATA_INSERIMENTO | DATE | Data di inserimento del record in tabella |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Codice dell’ufficio dell’operatore che ha effettuato l’inserimento |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha effettuato l’inserimento |
| CHIAVE_ANNO | NUMBER | Anno del fascicolo trasmesso |
| CHIAVE_PROGR | NUMBER | Numero del fascicolo trasmesso |



# UDIENZA
tabella contenente i dati relativi ad un’udienza. utilizzata dal sottosistema siep-sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_UDIENZA | NUMBER NOT NULL | Chiave numerica naturale dell'entità legata alla sequence UDI_SEQ. |
| DATA_UDIENZA | DATE NOT NULL | Data di svolgimento dell'udienza. |
| COD_PRESIDENTE | VARCHAR2 (6 CHAR) | Codice del magistrato che ha funzione di presidente. |
| COD_GIUDICE_1 | VARCHAR2 (6 CHAR) | Codice del magistrato avente funzione di primo giudice relatore. |
| COD_GIUDICE_2 | VARCHAR2 (6 CHAR) | Codice del magistrato avente funzione di secondo giudice relatore. |
| COD_PG | VARCHAR2 (6 CHAR) | Codice del Procuratore Generale della Repubblica che partecipa all'udienza. |
| COD_ID_ESPERTO_1 | NUMBER | Id del primo esperto nominato preposto alla causa. |
| COD_ID_ESPERTO_2 | NUMBER | Id dell'eventuale secondo esperto nominato preposto alla causa. |
| COD_ID_ASSISTENTE | NUMBER | Codice Identificativo dell'eventuale assistente. |
| NUMERO_MAX_FASCICOLI | NUMBER | Numero massimo di fascicoli trattati in udienza. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMEN TO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| LUOGO_UDIENZA | VARCHAR2 (100 CHAR) | Luogo svolgimento Udienza. |
| COD_UFFICIO_APPARTENENZA | VARCHAR2 (11 CHAR) NOT NULL | Codice dell'ufficio di appartenenza dell'Udienza. |
| NUM_COLLEGIO | NUMBER | Numero del collegio. |
| ORA_INIZIO | VARCHAR2 (2 CHAR) | Ora d’inizio dell’udienza |
| MIN_INIZIO | VARCHAR2 (2 CHAR) | Minuto d’inizio dell’udienza |
| ORA_FINE | VARCHAR2 (2 CHAR) | Ora fine dell’udienza |
| MIN_FINE | VARCHAR2 (2 CHAR) | Minuto fine dell’udienza |
| ORA_FINE_CC | VARCHAR2 (2 CHAR) | Ora fine camera di consiglio |
| MIN_FINE_CC | VARCHAR2 (2 CHAR) | Ora inizio camera di consiglio |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| UDIENZA_ASSISTENTE_FK2 | COD_ID_ASSISTENTE | (ASSISTENTE_GIUDIZIARIO.ID_ASSISTENTE_GIUDIZIARIO) |
| UDIENZA_ESPERTO_FK1 | COD_ID_ESPERTO_1 | (ESPERTO.ID_ESPERTO) |
| UDIENZA_ESPERTO_FK2 | COD_ID_ESPERTO_2 | (ESPERTO.ID_ESPERTO) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| UDIENZA_PROCEDIMENTO | UDI_PRO_UDI_FK | UDI_ID_UDIENZA |


# UDIENZA_PARTI
tabella contenente i dati relativi alle parti di un’udienza. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_SOGGETTO | NUMBER(38) | identificativo soggetto |
| ID_UDIENZA_PROCEDIMENTO_SIGE | NUMBER(38) | Identificativo procedimento sige |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Utenza dell’operatore che ha effettuato l’inserimento |
| DATA_INSERIMENTO | DATE | Data inserimento |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Utenza dell’operatore che ha effettuato l’inserimento |
| DATA_INSERIMENTO | DATE | Data inserimento |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11) | Ufficio dell’operatore che ha effettuato l’inserimento |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100) | Utenza dell’operatore che ha effettuato l’aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data dell’aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Ufficio dell’operatore che ha effettuato l’aggiornamento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| ID_SOGGETTO_FK | ID_SOGGETTO | (ANAGRAFICA_PARTI_UDIENZA.ID_SOGGETTO) |
| ID_UDIENZA_PROCEDIMENTO_FK | ID_UDIENZA_PROCEDIMENTO_SIGE | (UDIENZA_PROCEDIMENTO_SIGE.ID_UDIENZA_PROCEDIMENTO_SIGE) |


# UDIENZA_PROCEDIMENTO
tabella contenente i dati relativi all’udienza di un procedimento. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_UDIENZA_PROCEDIMENTO | NUMBER NOT NULL | Chiave numerica della tabella. |
| FLAG_RINVIATA | VARCHAR2 (1 BUTE) | Flag che indica l'eventuale rinvio dell'Udienza. Associato al Dominio FLAG_SI_NO di CG_REF_CODES. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| GEN_PRID_GENERALE_PROCEDIMENTO | NUMBER NOT NULL | Identificativo della tabella generale procedimento |
| UDI_ID_UDIENZA | NUMBER NOT NULL | Identificativo dell’udienza |
| UDI_ID_UDIENZA_RINVIO | NUMBER | Identificativo del rinvio udienza |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| UDI_PRO_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| UDI_PRO_GEN_PRO_FK | GEN_PRID_GENERALE_PROCEDIMENTO | (GENERALE_PROCEDIMENTO.ID_GENERALE_PROCEDIMENTO) |
| UDI_PRO_UDI_FK | UDI_ID_UDIENZA | (UDIENZA.ID_UDIENZA) |




# UDIENZA_PROCEDIMENTO_SIGE
tabella associativa tra la tabella udienza sige e procedimento sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_UDIENZA_PROCEDIMENTO_SIGE | NUMBER NOT NULL | Chiave numerica della tabella. |
| FLAG_RINVIATA | VARCHAR2 (1 CHAR) | Flag che indica l'eventuale rinvio dell'Udienza. Associato al Dominio FLAG_SI_NO di CG_REF_CODES. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_ID_FASCICOLO_SIGE | NUMBER NOT NULL | Identificativo del fascicolo SIGE |
| UDI_ID_UDIENZA_SIGE | NUMBER NOT NULL | Identificativo dell’udienza |
| UDI_ID_UDIENZA_RINVIO | NUMBER | Identificativo dell’udienza di rinvio |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| UDI_PRO_FAS_SIG_FK | FAS_ID_FASCICOLO_SIGE | (FASCICOLO_SIGE.ID_FASCICOLO_SIGE) |
| UDI_PRO_SIG_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| UDI_PRO_UDI_SIG_FK | UDI_ID_UDIENZA_SIGE | (UDIENZA_SIGE.ID_UDIENZA_SIGE) |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| UDIENZA_PARTI | ID_UDIENZA_PROCEDIMENTO_FK | ID_UDIENZA_PROCEDIMENTO_SIGE |


# UDIENZA_SIGE
tabella contenente i dati relativi ad un’udienza sige. utilizzata dal sottosistema sige.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_UDIENZA_SIGE | NUMBER NOT NULL | Chiave numerica naturale dell'entità legata alla sequence UDI_SIGE_SEQ. |
| DATA_UDIENZA | DATE NOT NULL | Data di svolgimento dell'udienza. |
| COD_PROCURATORE | VARCHAR2 (6 CHAR) | Codice del Procuratore. |
| COD_ID_ASSISTENTE | NUMBER | Codice Assistente. |
| NUMERO_MAX_FASCICOLI | NUMBER | Numero massimo di fascicoli per l’Udienza. |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| LUOGO_UDIENZA | VARCHAR2 (100 CHAR) | Luogo di svolgimento dell’Udienza. |
| COD_UFFICIO_APPARTENENZA | VARCHAR2 (11 CHAR) NOT NULL | Codice Ufficio Appartenenza. |
| ORA_INIZIO | VARCHAR2 (2 CHAR) | Ora Inizio |
| MIN_INIZIO | VARCHAR2 (2 CHAR) | Minuti Inizio |
| ORA_FINE | VARCHAR2 (2 CHAR) | Ora Fine |
| MIN_FINE | VARCHAR2 (2 CHAR) | Minuti Fine |
| COD_GIUDICE | VARCHAR2 (8 CHAR) | Codice del Giudice ( utilizzato solo per udienza monocratica ) |
| COL_ID_COLLEGIO. | NUMBER | Identificativo del collegio ( utilizzato solo per udienza collegiale ) |
| SEZIONE_UDIENZA | NUMBER | Indica la sezione dove viene svolta l’udienza |
| AULA_UDIENZA | NUMBER | Indica l’aula dove viene svolta l’udienza |


Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| UDIENZA_PROCEDIMENTO_SIGE | UDI_PRO_UDI_SIG_FK | UDI_ID_UDIENZA_SIGE |


# UFFICIO
tabella contenente i dati relativi all’ufficio. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_UFFICIO | VARCHAR2 (11 CHAR) NOT NULL | Codice ufficio derivante da Rege. La struttura di tale codice è così composto:
Codice Provincia (3 cifre) fornito dall’ISTAT
Codice Comune (3 cifre) fornito dall’ISTAT
Codice Frazione (1 cifra) vale 1 se la località appartiene ad un Comune
Codice Tipo Ufficio (2 cifre) fornito dal Ministero della Giustizia
Codice Dipendenza (1 cifre) fornito dal Ministero della Giustizia
Autocontrollo (1 cifre) generato in automatico attraverso la formula(autocontrollo=mod10 (S dispari + 2 S pari))
Quindi ad esempio "ROMA TRIBUNALE ORDINARIO - GIUDICE UNICO" avrà:
Codice Provincia: 058
Codice Comune: 091
Codice Frazione: 0
Codice Tipo Ufficio: 22
Codice Dipendenza: 0
Autocontrollo: 5
Pertanto il codice finale definitivo sarà: 05809102205 |
| COD_TIPO_UFFICIO | VARCHAR2 (10 CHAR) | Descrizione derivante da Re.Ge. |
| COD_PROVINCIA | VARCHAR2 (2 CHAR) | Codice letterale della provincia di appartenenza dell'ufficio. Es. LE=Lecce; RM=Roma; etc. |
| COD_COMUNE | VARCHAR2 (6 CHAR) | Codice del comune dell’ufficio |
| COD_DISTRETTO | VARCHAR2 (11 CHAR) | Codice del distretto di appartenenza dell'ufficio; Sarà fornito dall'amministrazione e sarà utilizzato per la le combo box per filtrare la scelta di un ufficio. |
| DATA_CARICAMENTO_REGE | DATE | Data di caricamento dei dati da Re.Ge. |
| COD_UFFICIO_COMPETENTE | VARCHAR2 (11 CHAR) | Codice dell’ufficio competente |
| INDIRIZZO | VARCHAR2 (200 CHAR) | Indirizzo dell’ufficio |
| CAP | VARCHAR2 (5 CHAR) | CAP dell’ufficio |
| TELEFONO | VARCHAR2 (255 CHAR) | Numero di telefono dell’ufficio |
| FAX | VARCHAR2 (255 CHAR) | Numero di fax dell’ufficio |
| E_MAIL | VARCHAR2 (255 CHAR) | Indirizzo email dell’ufficio |
| COD_OPERATORE_AGG | VARCHAR2 (100 CHAR) | Codice dell’operato che ha effettuato l’aggiornamento |
| DATA_AGG | DATE | Data di aggiornamento |
| COD_UFFICIO_AGG | VARCHAR2 (11 CHAR). | Codice dell’ufficio dell’operatore che ha effettuato l’aggiornamento |
| FLAG_ACCORP | VARCHAR2(1 CHAR) | S/N indica se l’ufficio è stato accorpato |



# UFFICIO_ACCORPATO
tabella contenente i dati relativi all’ufficio accorpato. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_UFFICIO | VARCHAR2(11 CHAR) not null | contiene il codice dell’ufficio soppresso |
| COD_TIPO_UFFICIO | VARCHAR2(10 CHAR) | contiene il tipo_ufficio dell’ufficio soppresso |
| DESCRIZIONE | VARCHAR2(50 CHAR) | contiene la descrizione dell’ufficio soppresso |
| COD_COMUNE | VARCHAR2(6 CHAR) | contiene il codice comune dell’ufficio soppresso |
| COD_DISTRETTO_OLD | VARCHAR2(11 CHAR) | contiene il codice del distretto di appartenenza dell’ufficio prima della soppressione |
| DESCRIZIONE_NEW_UFFICIO | VARCHAR2(50 CHAR) | contiene la descrizione dell’ufficio che ne assume la competenza |
| COD_UFFICIO_COMPETENTE | VARCHAR2(11 CHAR) | contiene il codice dell’ufficio del circondario che ne era competente |
| COD_DISTRETTO_NEW | VARCHAR2(11 CHAR) | contiene il codice del Distretto a cui appartiene l’ufficio che ne assume la competenza |
| COD_PROVINCIA | VARCHAR2(2 CHAR) | contiene la sigla della Provincia dell’ufficio soppresso |
| COD_UFFICIO_NEW | VARCHAR2(11 CHAR) | contiene il codice dell’ufficio che ne assume la competenza |
| INCR_PROGRESSIVO | VARCHAR2(14 CHAR) | contiene il valore di cui bisogna incrementare il valore presente nel campo CHIAVE_PROGR di FASCICOLO_SIEP o FASCICOLO_SIGE |
| DATA_INIZIO | DATE | contiene la data di inizio dell’accorpamento dell’ufficio |


# UFFICIO_DESCR
tabella contenente i dati relativi alle tipologie di ufficio. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione | Descrizione |
| --- | --- | --- | --- |
| COD_UFFICIO | VARCHAR2 (11 CHAR) NOT NULL | VARCHAR2 (11 CHAR) NOT NULL | Chiave numerica naturale dell'entità legata alla sequence UDI_SIGE_SEQ. |
| DESCR_TIPO_UFFICIO | VARCHAR2 (124 CHAR) NOT NULL | VARCHAR2 (124 CHAR) NOT NULL | Descrizione delle tipologia di ufficio |
| DESCR_COMUNE | VARCHAR2 (64 CHAR) NOT NULL | VARCHAR2 (64 CHAR) NOT NULL | Descrizione del comune |
| COD_PROVINCIA | VARCHAR2 (2 CHAR). | VARCHAR2 (2 CHAR). | Codice della provincia |

# UFFICI_PRODUZIONE
La tabella contiene i dati relativi agli uffici produzione per la decodifica del codice distretto e del codice comune, utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| CODICE_UFFICIO | VARCHAR2(11) | Indica il Codice dell’Ufficio da inviare per la richiesta del Bollettino |
| DESCRIZIONE_UFFICIO | VARCHAR2(255) | Indica la descrizione dell’Ufficio |
| CITTA | VARCHAR2(100) | Indica la descrizione della Città |
| TIPO_UFFICIO | VARCHAR2(2) | Indica il Codice del Tipo dell’Ufficio |
| CODICE_GL | VARCHAR2(4) | Indica il Codice del Distretto dell’Ufficio da inviare per la richiesta del Bollettino |
| COD_UFFICIO_SIES | VARCHAR2(11) | Indica il corrispondente Codice dell’Ufficio del SIES |
| TIPO_UFFICIO_SIES | VARCHAR2(8) | Indica il corrispondente Codice del Tipo Ufficio del SIES |
| COMUNE_SIES | VARCHAR2(100) | Indica la corrispondente descrizione del Comune del SIES |
| CODICE_DISTRETTO_SIES | VARCHAR2(11) | Indica il corrispondente Codice del Distretto del SIES |
| COD_COMUNE_SIES | VARCHAR2(6) | Indica il corrispondente Codice del Comune del SIES |


# ULTERIORE_ISTANZA
tabella contenente i dati relativi alle ulteriori istanze. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ULTERIORE_ISTANZA | NUMBER NOT NULL | Identificativo della tabella |
| COD_OGGETTO_PROCEDIMENTO | VARCHAR2 (4 CHAR) | Codice Oggetto Procedimento |
| DATA_RICHIESTA | DATE | Data Richiesta |
| DATA_ARRIVO_CANCELLERIA | DATE | Data Arrivo in cancelleria |
| COD_TIPO_ATTO | VARCHAR2 (2 CHAR) | Codice Tipo Atto |
| COD_TIPO_MITTENTE_ATTO | VARCHAR2 (2 CHAR) | Codice Tipo Mittente Atto |
| SEDE_MITTENTE | VARCHAR2 (6 CHAR) | Sede Mittente |
| DESCR_MITTENTE | VARCHAR2 (100 CHAR) | Descrizione Mittente |
| NOTE | VARCHAR2 (2000 CHAR) | Note |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice Operatore Inserimento |
| DATA_INSERIMENTO | DATE | Data Inserimento |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Codice Ufficio Inserimento |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice Operatore Aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data Aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Codice Ufficio Aggiornamento |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER | Id di relazione con il fascicolo SIUS |





# ULTERIORE_ISTANZA_TENORE
tabella contenente i dati relativi al tenore per le ulteriori istanze. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ULTERIORE_ISTANZA_TENORE | NUMBER NOT NULL | Identificativo della tabella |
| COD_OGGETTO_TENORE | VARCHAR2 (4 CHAR) | Codice Oggetto Tenore |
| DATA | DATE | Data |
| COD_DETTAGLIO_OGGETTO | VARCHAR2 (4 CHAR) | Codice Dettaglio Oggetto |
| COD_MAGISTRATO | VARCHAR2 (6 CHAR) | Codice Magistrato |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice Operatore Inserimento |
| DATA_INSERIMENTO | DATE | Data Inserimento |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Codice Ufficio Inserimento |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice Operatore Aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data Aggiornamento |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Codice Ufficio Aggiornamento |
| ULT_IST_ID_ULTERIORE_ISTANZA. | NUMBER | ID reference con "ULTERIORE_ISTANZA" |



# ULTERIORE_SANZIONE_CUMULO
tabella contenente i dati relativi alle ulteriori sanzioni per il cumulo. utilizzata dal sottosistema siep.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_ULTERIORE_SANZIONE_CUMU LO | NUMBER NOT NULL | Chiave numerica della tabella. |
| COD_TIPO_ULTERIORE_SANZIONE | VARCHAR2 (2 CHAR) | Codifica del tipo di ulteriore sanzione (Semidetenzione / Libertà controllata/ lavoro sostitutivo ecc.). Associata al dominio TIPO_ULTERIORE_SANZIONE di CG_REF_CODES. |
| NUM_ANNI | NUMBER | Numero anni di ulteriore sanzione. |
| NUM_MESI | NUMBER | Numero mesi di ulteriore sanzione. |
| NUM_GIORNI | NUMBER | Numero gg. di ulteriore sanzione. |
| SANZIONE | NUMBER (2-16) | Importo relativo alla sanzione pecuniaria. |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| FAS_SIE_ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP |
| CUM_ID_CUMULO | NUMBER | Identificativo del Cumulo |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| ULT_SAN_CUM_FAS_SIE_FK | FAS_SIE_ID_FASCICOLO_SIEP | (FASCICOLO_SIEP.ID_FASCICOLO_SIEP) |
| ULT_SAN_CUM_ID_CUM | CUM_ID_CUMULO | (CUMULO.ID_CUMULO) |





# UTENTE
tabella contenente i dati relativi agli utenti che utilizzano il sies. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_UTENTE | VARCHAR2 (100 CHAR) NOT NULL | Codice univoco che identifica l'utente a livello distrettuale. Tale codice è usato in tutte le tabelle nelle quali è registrata l'informazione di chi   ha fatto cosa. |
| COGNOME | VARCHAR2 (50 CHAR) NOT NULL | Cognome reale dell'utente |
| NOME | VARCHAR2 (50 CHAR) NOT NULL | Nome reale dell'utente |
| PWD | VARCHAR2 (30 CHAR) | Password riferita all'utente |
| DATA_FINE_VALIDITA | DATE | Data dalla quale un utente non si considera più valido. |
| DATA_ORA_CONNESSIONE | DATE | Data e ora dell'ultima connessione dell'utente al sistema |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Generalmente il codice dell'utente amministratore del sistema/utenti |
| DATA_INSERIMENTO | DATE | Data inserimento del record in tabella |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Generalmente il codice dell'utente amministratore del sistema/utenti |
| DATA_AGGIORNAMENTO | DATE | Data di ultima modifica del record in tabella |
| DATA_ULTIMA_MODIFICA_PWD | DATE | Data di ultima modifica della password. |
| IP | VARCHAR2 (15 CHAR) | Indirizzo IP del computer dell’utente |
| TELEFONO | VARCHAR2 (255 CHAR) | Numero di telefono dell’utente |
| FAX | VARCHAR2 (255 CHAR) | Numero di fax dell’utente |
| E_MAIL | VARCHAR2 (255 CHAR) | Indirizzo email dell’utente |
| USERID_NSC | VARCHAR2 (100 CHAR) | Indica la userid di accesso a NSC |
| PWD_NSC | VARCHAR2 (30 CHAR) | Indica la password di accesso a NSC |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| UTENTE_PROFILO | UTE_PRO_UTE_FK | UTE_COD_UTENTE |
| UTENTE_UFFICIO | UTE_UFF_UTE_FK | UTE_COD_UTENTE |




# UTENTE_PROFILO
tabella contenente i dati relativi ai profili degli utenti che utilizzano sies. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| DATA_INIZIO_VALIDITA | DATE NOT NULL | Data di inizio validità di una associazione utente/profilo |
| DATA_FINE_VALIDITA | DATE | Data dalla quale un utente non ha più l'associazione utente/profilo. Questo attributo che generalmente vale null deve essere popolato automaticamente dal sistema nel momento in cui all'utente si associa un nuovo profilo. |
| UTE_COD_UTENTE | VARCHAR2 (100 CHAR) NOT NULL | Codice dell’utente |
| PRF_COD_PROFILO | NUMBER NOT NULL | Codice del profilo |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha effettuato l’aggiornamento |
| DATA_AGGIORNAMENTO | DATE | Data in cui viene effettuato l’aggiornamento |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| UTE_PRO_PRF_FK | PRF_COD_PROFILO | (PROFILO.COD_PROFILO) |
| UTE_PRO_UTE_FK | UTE_COD_UTENTE | (UTENTE.COD_UTENTE) |





# UTENTE_UFFICIO
tabella contenente i dati relativi agli uffici di appartenenza degli utenti che utilizzano sies. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| DATA_INIZIO_VALIDITA | DATE NOT NULL | Data di inizio validità del rapporto utente-ufficio |
| DATA_FINE_VALIDITA | DATE | Data di fine validità del rapporto utente-ufficio |
| UTE_COD_UTENTE | VARCHAR2 (100 CHAR) NOT NULL | Codice dell’utente |
| UFF_COD_UFFICIO | VARCHAR2 (11 CHAR) NOT NULL | Codice dell’ufficio |
| COD_UTENTE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UTENTE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| UTE_UFF_UTE_FK | UTE_COD_UTENTE | (UTENTE.COD_UTENTE) |




# UTENZA_ADN
tabella contenente i dati relativi agli utenti che accedono al portale mygiustizia con utenza adn.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID | NUMBER(38) | Codice univoco che identifica il record |
| SAMACCOUNTNAME | VARCHAR2(60 CHAR) | Nome Accesso Univoco |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Generalmente il codice dell'utente amministratore del sistema/utenti che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data inserimento del record in tabella |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Indica il codice dell’utente che ha effettuato l’aggiornamento del dato in tabella |
| DATA_AGGIORNAMENTO | DATE | Data di ultima modifica del record in tabella |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| UTENZA_ADN_PK | ID | UTE_COD_UTENTE |
| UTENZA_ADN_UK | SAMACCOUNTNAME | UTE_COD_UTENTE |




# VERBALE
tabella contenente i dati relativi al verbale. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_VERBALE | NUMBER NOT NULL | Chiave numerica naturale della tabella. |
| COD_TIPO_VERBALE | VARCHAR2 (2 CHAR) NOT NULL | Indica la tipologia di verbale che si sta trattando. Deriva da dominio e può assumere i seguenti valori:
ARRESTO
SOTTOSCRIZIONE OBBLIGHI VANE RICERCHE |
| DATA_EMISSIONE | DATE | Data di emissione del Verbale |
| DATA_PERVENIMENTO | DATE | Data in cui il verbale è pervenuto al destinatario. |
| COD_TIPO_UFFICIO_FIRMATARIO | VARCHAR2 (2 CHAR) | Tipologia dell'ufficio che ha emesso/firmato il verbale |
| COD_LUOGO_UFFICIO_FIRMATARIO | VARCHAR2 (6 CHAR) | Comune dell'ufficio che ha emesso/firmato il verbale |
| NOTE | VARCHAR2 (2000 CHAR) | Eventuali note aggiuntive al verbale |
| COD_OPERATORE_INSERIMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha inserito il record |
| DATA_INSERIMENTO | DATE | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2 (100 CHAR) | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha aggiornato il record |
| EVE_ID_EVENTO | NUMBER | Identificativo dell’evento |
| CSS_ID_CSSA | NUMBER | Identificativo del CSSA |
| IST_DET_ID_ISTITUTO_DETENZIONE | VARCHAR2 (4 CHAR) | Identificativo dell’istituto di detenzione |
| FAS_SIU_ID_FASCICOLO_SIUS | NUMBER | Identificativo del fascicolo SIUS |
| NOT_ID_NOTIFICA | NUMBER | Identificativo della notifica |
| NUMERO_PROTOCOLLO | VARCHAR2 (2000 CHAR) | Numero di protocollo |
| NUM_ANNI_ESPULSIONE | NUMBER | Numero di anni di espulsione |
| NUM_MESI_ESPULSIONE | NUMBER | Numero di mesi di espulsione |
| NUM_GIORNI_ESPULSIONE | NUMBER | Numero di giorni di espulsione |


Chiavi Esterne

| CONSTRAINT_NAME | COLUMN_NAME | REFERENCES_COLUMN |
| --- | --- | --- |
| VER_EVE_FK | EVE_ID_EVENTO | (EVENTO.ID_EVENTO) |
| VER_NOT_FK | NOT_ID_NOTIFICA | (NOTIFICA.ID_NOTIFICA) |

Riferimenti Esterni

| TABLE_NAME | CONSTRAINT_NAME | COLUMN_NAME |
| --- | --- | --- |
| RINNOVO | RIN_VER_FK | VER_ID_VERBALE |



# VERSIONE
tabella contenente i dati relativi alla versione utilizzata di sies. utilizzata dal sottosistema siep-sige-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| COD_VERSIONE | VARCHAR2 (50 CHAR) NOT NULL | Codice della versione di SIES |
| DATA | DATE NOT NULL | Data di rilascio della versione |
| DESCRIZIONE | VARCHAR2 (2000 CHAR) | Descrizione del contenuto della versione |


# COLLA.COLLABORATORE
tabella contenente i dati relativi ai collaboratori di giustizia per la sorveglianza di Roma. utilizzata dal sottosistema sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_COLLABORATORE | NUMBER(38)  NOT NULL | Chiave individua univocamente un record |
| ID_FASCICOLO_SIUS | RAW(40) NOT NULL | Riferimento al Procedimento SIUS; il dato viene criptato. |
| UFFICIO | VARCHAR2(11 BYTE)   NOT NULL | Codice ufficio di competenza |
| DATA_INIZIO | DATE  NOT NULL | Data di inizio dell’attività di CG |
| DATA_FINE | DATE   DEFAULT NULL | Data di fine dell’attività di CG |
| COD_OPERATORE_INSERIMENTO | VARCHAR2(100 BYTE)  DEFAULT NULL | Valorizzato per definirne quando necessario, la revoca |
| DATA_INSERIMENTO | DATE   DEFAULT NULL | Data di inserimento del record |
| COD_UFFICIO_INSERIMENTO | VARCHAR2(11 BYTE)   DEFAULT NULL | Ufficio dell’operatore che ha inserito il record |
| COD_OPERATORE_AGGIORNAMENTO | VARCHAR2(100 BYTE)  DEFAULT NULL | Codice dell’operatore che ha aggiornato il record |
| DATA_AGGIORNAMENTO | DATE   DEFAULT NULL | Data di aggiornamento del record |
| COD_UFFICIO_AGGIORNAMENTO | VARCHAR2(11 BYTE)   DEFAULT NULL | Ufficio dell’operatore che ha aggiornato il record |

# STATIS.ISP_ATTIVITA_MAGISTRATI_MS
tabella utilizzata per le statistiche relative alle attività dei magistrati dei provvedimenti di misure di sicurezza. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP di riferimento. |
| CHIAVE_ANNO | NUMBER(4) | Anno del fascicolo SIEP di riferimento. |
| CHIAVE_PROGR | NUMBER | Progressivo del fascicolo SIEP di riferimento. |
| COD_UFFICIO | VARCHAR2(11 CHAR) | Ufficio interessato dalla statistica. |
| COD_MAGISTRATO | VARCHAR2 (7 CHAR) | Codice del magistrato interessato dall’attività. |
| DATA_EMISSIONE | DATE | Data di emissione del fascicolo. |
| COD_MOTIVO | VARCHAR2 (4 CHAR) | Codice Motivo del fascicolo. Associato al Dominio MOTIVO_PROVVEDIMENTO di CG_REF_CODES. |
| TIPOLOGIA | VARCHAR2(100 CHAR) | Tipologia dell’attività. |
| ID_EVENTO | NUMBER | Identificativo dell’evento associato al fascicolo. |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record. |
| CHIAVE_PROGR_ORIG | NUMBER(38) | Progressivo del fascicolo SIEP originario. |
| DESC_UFFICIO_INSERIMENTO | VARCHAR2(200 CHAR) | Descrizione dell’ufficio dell’operatore che ha inserito il record. |
| TIPO_MS | VARCHAR2(3 CHAR) | Tipologia della misura di sicurezza. Associato al Dominio TIPO_MISURA_SICUREZZA di CG_REF_CODES. |


# STATIS.ISP_PROVVEDIMENTI_MS
tabella utilizzata per le statistiche relative ai provvedimenti di misure di sicurezza. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_FASCICOLO_SIEP | NUMBER(38) | Identificativo del fascicolo SIEP di riferimento. |
| NRES | NUMBER(38) | Numero del Fascicolo Res. |
| CHIAVE_ANNO | NUMBER(4) | Anno del fascicolo SIEP di riferimento. |
| CHIAVE_PROGR | NUMBER(38) | Progressivo del fascicolo SIEP di riferimento. |
| ULT_TIPO_PROVVEDIMENTO | VARCHAR2(2 CHAR) | Ultima Tipologia di Provvedimento. Associato al Dominio TIPO_PROVVEDIMENTO di CG_REF_CODES. |
| ULT_COD_MOTIVO | VARCHAR2(4 CHAR) | Ultimo Codice Motivo. Associato al Dominio MOTIVO_PROVVEDIMENTO di CG_REF_CODES. |
| PEN_TIPO_PROVVEDIMENTO | VARCHAR2(2 CHAR) | Tipologia di Provvedimento della pena. Associato al Dominio TIPO_PROVVEDIMENTO di CG_REF_CODES. |
| PEN_COD_MOTIVO | VARCHAR2(4 CHAR) | Codice Motivo della pena. Associato al Dominio MOTIVO_PROVVEDIMENTO di CG_REF_CODES. |
| CONTA | NUMBER | Contatore per le statistiche. |
| COD_UFFICIO | VARCHAR2(11 CHAR) | Ufficio interessato dalla statistica. |
| COD_STATO_PROCEDIMENTO | VARCHAR2(4 CHAR) | Codice stato procedimento. Associato al Dominio STATO_PROCEDIMENTO di CG_REF_CODES. |
| COD_STATO_FASCICOLO_RES | NUMBER | Codice stato fascicolo res. Associato al Dominio STATO_FASCICOLO di CG_REF_CODES. |
| COD_POSIZIONE_GIURIDICA | VARCHAR2(2 CHAR) | Codice della posizione giuridica. Associato al Dominio POSIZIONE_GIURIDICA di CG_REF_CODES. |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record. |
| CHIAVE_PROGR_ORIG | NUMBER(38) | Progressivo del fascicolo SIEP originario. |
| DESC_UFFICIO_INSERIMENTO | VARCHAR2(200 CHAR) | Descrizione dell’ufficio dell’operatore che ha inserito il record. |


# STATIS.ISP_SCARTI_MS
tabella utilizzata per le statistiche relative agli scarti dei provvedimenti di misure di sicurezza. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_FASCICOLO_SIEP | NUMBER(38) | Identificativo del fascicolo SIEP di riferimento. |
| NRES | NUMBER(38) | Numero del Fascicolo Res. |
| CHIAVE_ANNO | NUMBER(4) | Anno del fascicolo SIEP di riferimento. |
| CHIAVE_PROGR | NUMBER(38) | Progressivo del fascicolo SIEP di riferimento. |
| ULT_TIPO_PROVVEDIMENTO | VARCHAR2(2 CHAR) | Ultima Tipologia di Provvedimento. Associato al Dominio TIPO_PROVVEDIMENTO di CG_REF_CODES. |
| ULT_COD_MOTIVO | VARCHAR2(4 CHAR) | Ultimo Codice Motivo. Associato al Dominio MOTIVO_PROVVEDIMENTO di CG_REF_CODES. |
| PEN_TIPO_PROVVEDIMENTO | VARCHAR2(2 CHAR) | Tipologia di Provvedimento della pena. Associato al Dominio TIPO_PROVVEDIMENTO di CG_REF_CODES. |
| PEN_COD_MOTIVO | VARCHAR2(4 CHAR) | Codice Motivo della pena. Associato al Dominio MOTIVO_PROVVEDIMENTO di CG_REF_CODES. |
| COD_UFFICIO | VARCHAR2(11 CHAR) | Ufficio interessato dalla statistica. |
| COD_STATO_PROCEDIMENTO | VARCHAR2(4 CHAR) | Codice stato procedimento. Associato al Dominio STATO_PROCEDIMENTO di CG_REF_CODES. |
| COD_STATO_FASCICOLO_RES | NUMBER | Codice stato fascicolo res. Associato al Dominio STATO_FASCICOLO di CG_REF_CODES. |
| COD_POSIZIONE_GIURIDICA | VARCHAR2(2 CHAR) | Codice della posizione giuridica. Associato al Dominio POSIZIONE_GIURIDICA di CG_REF_CODES. |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record. |
| CHIAVE_PROGR_ORIG | NUMBER(38) | Progressivo del fascicolo SIEP originario. |
| DESC_UFFICIO_INSERIMENTO | VARCHAR2(200 CHAR) | Descrizione dell’ufficio dell’operatore che ha inserito il record. |

# STATIS.ISP_TEMPI_ISCRIZIONE_MS
tabella utilizzata per le statistiche relative ai tempi di iscrizione dei provvedimenti di misure di sicurezza. utilizzata dal sottosistema siep-sius.

| Field | Datatype | Descrizione |
| --- | --- | --- |
| ID_FASCICOLO_SIEP | NUMBER | Identificativo del fascicolo SIEP di riferimento. |
| CHIAVE_ANNO | NUMBER(4) | Anno del fascicolo SIEP di riferimento. |
| CHIAVE_PROGR | NUMBER | Progressivo del fascicolo SIEP di riferimento. |
| COD_UFFICIO | VARCHAR2(11 CHAR) | Ufficio interessato dalla statistica. |
| DATA_ISCRIZIONE | DATE | Data di iscrizione del fascicolo. |
| DATA_ARRIVO_ATTO | DATE | Data dell’arrivo dell’atto. |
| DATA_IRREVOCABILITA | DATE | Data di irrevocabilità del fascicolo. |
| TEMPO_RICEZIONE_ISCRIZIONE | NUMBER | Tempo di ricezione dell’iscrizione del fascicolo. |
| TEMPO_GIUDICATO_ISCRIZIONE | NUMBER | Tempo di passaggio in giudicato dell’iscrizione del fascicolo. |
| DESC_TIPO_AUTORITA_EMITTENTE | VARCHAR2(200 CHAR) | Descrizione dell’autorità emittente del fascicolo. Associato al Dominio TIPO_AUTORITA di CG_REF_CODES. |
| DESC_LUOGO_EMITTENTE | VARCHAR2(200 CHAR) | Descrizione del luogo di appartenenza dell’autorità emittente del fascicolo. |
| DESC_SEZIONE_AUTORITA | VARCHAR2(50 CHAR) | Descrizione della sezione dell’autorità emittente del fascicolo. |
| COD_UFFICIO_INSERIMENTO | VARCHAR2 (11 CHAR) | Ufficio dell’operatore che ha inserito il record. |
| CHIAVE_PROGR_ORIG | NUMBER(38) | Progressivo del fascicolo SIEP originario. |
| DESC_UFFICIO_INSERIMENTO | VARCHAR2(200 CHAR) | Descrizione dell’ufficio dell’operatore che ha inserito il record. |

# Viste utilizzate dallo schema SIESXX
V_FASCICOLO_SIEP

CREATE OR REPLACE FORCE VIEW SIESTO.V_FASCICOLO_SIEP
(id_fascicolo_siep, chiave_anno, chiave_progr, chiave_ufficio, data_provvedimento, descr_tipo_provvedimento, descr_tipo_autorita_emittente, descr_luogo_emittente, data_irrevocabilita, cognome, nome, id_soggetto, id_sentenza, flag_validato, data_iscrizione, stato_procedimento, cod_distretto, data_aggiornamento, cod_stato_fascicolo, data_arrivo_atto, cod_ufficio_inserimento)
AS
SELECT fascicolo_siep.id_fascicolo_siep, fascicolo_siep.chiave_anno,
fascicolo_siep.chiave_progr, fascicolo_siep.chiave_ufficio,
sentenza.data_provvedimento,
tipo_provvedimento.rv_meaning descr_tipo_provvedimento,
tipo_autorita_emittente.rv_meaning descr_tipo_autorita_emittente,
luogo_emittente.descrizione descr_luogo_emittente,
fascicolo_siep.data_irrevocabilita, soggetto.cognome, soggetto.nome,
soggetto.id_soggetto, sentenza.id_sentenza, flag_validato,
fascicolo_siep.data_iscrizione,
(c.rv_meaning || ' ' || TO_CHAR (a.DATA, 'dd-mm-yyyy')
) descr_stato_procedimento,
cod_distretto, fascicolo_siep.data_aggiornamento, cod_stato_fascicolo,
fascicolo_siep.data_arrivo_atto,fascicolo_siep.cod_ufficio_inserimento
FROM fascicolo_siep,
soggetto,
sentenza,
cg_ref_codes tipo_provvedimento,
cg_ref_codes tipo_autorita_emittente,
comune luogo_emittente,
ufficio,
stato_procedimento a,
cg_ref_codes c,
max_stato_procedimento b
WHERE fascicolo_siep.sog_id_soggetto = soggetto.id_soggetto
AND ufficio.cod_ufficio = fascicolo_siep.chiave_ufficio
--==========================================================================
-- Condizioni sulla sentenza
AND fascicolo_siep.sen_id_sentenza = sentenza.id_sentenza
AND (    tipo_provvedimento.rv_domain = 'TIPO_PROVVEDIMENTO'
AND tipo_provvedimento.rv_low_value = sentenza.cod_tipo_provvedimento
)
AND (    tipo_autorita_emittente.rv_domain = 'TIPO_UFFICIO'
AND tipo_autorita_emittente.rv_low_value =
sentenza.cod_tipo_autorita_emittente
)
AND luogo_emittente.cod_comune = sentenza.cod_luogo_emittente
--==========================================================================
-- JOIN per lo Stato Procedimento.
-- n.b. può essere presente più di un record per un fascicolo. In questo caso
--      verrebbero estratti n record fascicolo. Per cui vado in join con
--      max_stato_procedimento per recuperare il progressivo corretto
-- Aggiunta gestione caso di mancanza stato procedimento (migrati). Venivano
-- scartati in quanto falliva la join con stato procedimento e max. stato
-- procedimento.
AND fascicolo_siep.id_fascicolo_siep = a.fas_sie_id_fascicolo_siep(+)
AND c.rv_domain = 'STATO_PROCEDIMENTO'
AND NVL (a.cod_stato_procedimento, '-') = c.rv_low_value
AND (    a.fas_sie_id_fascicolo_siep = b.fas_sie_id_fascicolo_siep(+)
AND (a.progressivo = b.sta_pro_progressivo OR a.progressivo IS NULL)
);

V_PROVVEDIMENTI

CREATE OR REPLACE FORCE VIEW SIESTO.V_PROVVEDIMENTI
(id_fascicolo_siep, chiave_anno, chiave_progr, chiave_ufficio, data_provvedimento, descr_tipo_provvedimento, descr_tipo_autorita_emittente, descr_luogo_emittente, data_irrevocabilita, cognome, nome, data_nascita, luogo_nascita, id_soggetto, id_sentenza, flag_validato, data_iscrizione, stato_procedimento, cod_distretto, data_aggiornamento, cod_stato_fascicolo, id_evento, descr_cod_motivo, cod_motivo, cod_tipo_evento, cod_tipo_provvedimento, flag_documento_registrato)
AS
SELECT
FASCICOLO_SIEP.ID_FASCICOLO_SIEP, FASCICOLO_SIEP.CHIAVE_ANNO,
FASCICOLO_SIEP.CHIAVE_PROGR,FASCICOLO_SIEP.CHIAVE_UFFICIO,
SENTENZA.DATA_PROVVEDIMENTO,
TIPO_PROVVEDIMENTO.RV_MEANING DESCR_TIPO_PROVVEDIMENTO,
TIPO_AUTORITA_EMITTENTE.RV_MEANING DESCR_TIPO_AUTORITA_EMITTENTE,
LUOGO_EMITTENTE.DESCRIZIONE DESCR_LUOGO_EMITTENTE,
FASCICOLO_SIEP.DATA_IRREVOCABILITA,
SOGGETTO.COGNOME, SOGGETTO.NOME,SOGGETTO.DATA_NASCITA,LUOGO_NASCITA.DESCRIZIONE DESCR_LUOGO_NASCITA,
SOGGETTO.ID_SOGGETTO, SENTENZA.ID_SENTENZA ,
FLAG_VALIDATO,FASCICOLO_SIEP.DATA_ISCRIZIONE,(c.RV_MEANING||' '||TO_CHAR(a.data,'dd-mm-yyyy')) descr_STATO_PROCEDIMENTO,
COD_DISTRETTO,FASCICOLO_SIEP.DATA_AGGIORNAMENTO,COD_STATO_FASCICOLO,EVENTO.ID_EVENTO,MOTIVO_PROVVEDIMENTO.RV_MEANING DESCR_MOTIVO_PROVVEDIMENTO,
EVENTO.cod_motivo,EVENTO.cod_tipo_evento,EVENTO.cod_tipo_provvedimento,EVENTO.flag_documento_registrato
FROM
FASCICOLO_SIEP,
SOGGETTO,
SENTENZA,
CG_REF_CODES TIPO_PROVVEDIMENTO,
CG_REF_CODES TIPO_AUTORITA_EMITTENTE,
CG_REF_CODES MOTIVO_PROVVEDIMENTO,
COMUNE LUOGO_EMITTENTE,
COMUNE LUOGO_NASCITA,
UFFICIO,
STATO_PROCEDIMENTO a,CG_REF_CODES c,
MAX_STATO_PROCEDIMENTO b,
EVENTO
WHERE a.FAS_SIE_ID_FASCICOLO_SIEP =b.FAS_SIE_ID_FASCICOLO_SIEP
AND a.PROGRESSIVO = b.STA_PRO_PROGRESSIVO
AND c.RV_DOMAIN = 'STATO_PROCEDIMENTO' AND
c.RV_LOW_VALUE = a.COD_STATO_PROCEDIMENTO
AND
FASCICOLO_SIEP.SOG_ID_SOGGETTO = SOGGETTO.ID_SOGGETTO AND
FASCICOLO_SIEP.SEN_ID_SENTENZA = SENTENZA.ID_SENTENZA AND
FASCICOLO_SIEP.ID_FASCICOLO_SIEP =a.FAS_SIE_ID_FASCICOLO_SIEP(+) AND
FASCICOLO_SIEP.ID_FASCICOLO_SIEP =EVENTO.fas_sie_id_fascicolo_siep AND
(TIPO_PROVVEDIMENTO.RV_DOMAIN = 'TIPO_PROVVEDIMENTO' AND
TIPO_PROVVEDIMENTO.RV_LOW_VALUE = SENTENZA.COD_TIPO_PROVVEDIMENTO) AND
(TIPO_AUTORITA_EMITTENTE.RV_DOMAIN = 'TIPO_UFFICIO' AND
TIPO_AUTORITA_EMITTENTE.RV_LOW_VALUE = SENTENZA.COD_TIPO_AUTORITA_EMITTENTE) AND
(MOTIVO_PROVVEDIMENTO.RV_DOMAIN = 'MOTIVO_PROVVEDIMENTO' AND
MOTIVO_PROVVEDIMENTO.RV_LOW_VALUE = EVENTO.cod_motivo) AND
LUOGO_EMITTENTE.COD_COMUNE = SENTENZA.COD_LUOGO_EMITTENTE AND
LUOGO_NASCITA.COD_COMUNE = SOGGETTO.COD_COMUNE_NASCITA
AND UFFICIO.COD_UFFICIO = FASCICOLO_SIEP.CHIAVE_UFFICIO;

V_REATI_FASCICOLO

CREATE OR REPLACE FORCE VIEW SIESTO.V_REATI_FASCICOLO AS
select fas_sie_id_fascicolo_siep,
count(*) num_reati,
min(data_inizio_composta) primo_reato,
max.(data_inizio_composta) ultimo_reato
from (select t.fas_sie_id_fascicolo_siep,
t.id_reato,
(case
when t.data_inizio is not null then
t.data_inizio
when t.mese_inizio is not null and t.anno_inizio is not null then
to_date('01/' || t.mese_inizio || '/' || t.anno_inizio, 'dd/mm/yyyy')
when t.anno_inizio is not null then
to_date('01/01/' || t.anno_inizio, 'dd/mm/yyyy')
else
null
end) as data_inizio_composta
from REATO t)
group by fas_sie_id_fascicolo_siep;

V_SOGGETTO_ETA

CREATE OR REPLACE FORCE VIEW SIESTO.V_SOGGETTO_ETA  AS
select tb."ID_FASCICOLO_SIEP" "FAS_SIE_ID_FASCICOLO_SIEP"
,tb."ID_SOGGETTO" COD_SOGGETTO
,(case
when ETA_SOGGETTO_ORA is not null then
ETA_SOGGETTO_ORA
when ETA_PRESUNTA_ORA is not null then
ETA_PRESUNTA_ORA
else  trunc(((nvl(eta_presunta_anni,0) * 12) + nvl(eta_presunta_mesi,0)) /12)
end) as eta_ora
from (select fs."ID_FASCICOLO_SIEP",
rf."NUM_REATI",
rf."PRIMO_REATO",
rf."ULTIMO_REATO",
sm."ID_SOGGETTO",
sm."DATA_MAGGIORENNE",
sm."ETA_SOGGETTO_ORA",
sm."DATA_NASCITA_PRESUNTA",
sm."ETA_PRESUNTA_ANNI",
sm."ETA_PRESUNTA_MESI",
trunc(MONTHS_BETWEEN(sysdate, ADD_MONTHS(ADD_MONTHS(rf.primo_reato, - nvl(sm.eta_presunta_anni,0) * 12), -nvl(sm.eta_presunta_mesi,0) ) ) / 12) ETA_PRESUNTA_ORA
from FASCICOLO_SIEP         fs,
V_REATI_FASCICOLO      rf,
V_SOGGETTO_MAGGIORENNE sm
where fs.id_fascicolo_siep = rf.fas_sie_id_fascicolo_siep (+)
and fs.sog_id_soggetto = sm.id_soggetto) tb;

V_SOGGETTO_MAGGIORENNE

CREATE OR REPLACE FORCE VIEW SIESTO.V_SOGGETTO_MAGGIORENNE AS
select id_soggetto,
ADD_MONTHS(data_nascita_composta, 18 * 12) data_maggiorenne,
trunc(MONTHS_BETWEEN(sysdate, data_nascita_composta)/12) eta_soggetto_ora,
eta_presunta_anni,
eta_presunta_mesi,
data_nascita_presunta,
data_reato_sius
from (select t.id_soggetto, t.eta_presunta_anni, t.eta_presunta_mesi, t.data_nascita_presunta,t.data_reato_sius,
(case
when t.data_nascita is not null then
t.data_nascita
when t.mese_nascita is not null and t.anno_nascita is not null then
to_date('01/' || t.mese_nascita || '/' || t.anno_nascita, 'dd/mm/yyyy')
when t.anno_nascita is not null then
to_date('01/01/' || t.anno_nascita, 'dd/mm/yyyy')
when t.data_nascita_presunta_calc is not null then
t.data_nascita_presunta_calc
else
null
end) as data_nascita_composta
from SOGGETTO t);

V_SOGGETTO_MAGGIORENNE_NEW

create or replace view v_soggetto_maggiorenne_new as
select distinct
TB_SOGGETTI.ID_SOGGETTO id_soggetto,
null data_maggiorenne,
(case
when TB_SOGGETTI.ETA_SOGGETTO_ORA is not null then
TB_SOGGETTI.ETA_SOGGETTO_ORA
when TB_SOGGETTI.ETA_PRESUNTA_ORA is not null then
TB_SOGGETTI.ETA_PRESUNTA_ORA
when TB_SOGGETTI_SIES.ETA_PRESUNTA_ORA is not null then
TB_SOGGETTI_SIES.ETA_PRESUNTA_ORA
when TB_SOGGETTI_SIGE.ETA_SOGGETTO_ORA_SIEP is not null then
TB_SOGGETTI_SIGE.ETA_SOGGETTO_ORA_SIEP
when TB_SOGGETTI_SIGE.ETA_PRESUNTA_ORA is not null then
TB_SOGGETTI_SIGE.ETA_PRESUNTA_ORA
else  trunc(((nvl(TB_SOGGETTI.eta_presunta_anni,0) * 12) + nvl(TB_SOGGETTI.eta_presunta_mesi,0)) /12)
end) as eta_soggetto_ora,
null eta_presunta_anni,
null eta_presunta_mesi,
TB_SOGGETTI.data_nascita_presunta,
TB_SOGGETTI.data_reato_sius
FROM (select null "ID_FASCICOLO_SIEP",
null "NUM_REATI",
null "PRIMO_REATO",
null "ULTIMO_REATO",
sm.id_soggetto ID_SOGGETTO,
sm."DATA_MAGGIORENNE",
sm."ETA_SOGGETTO_ORA",
sm."DATA_NASCITA_PRESUNTA",
sm."ETA_PRESUNTA_ANNI",
sm."ETA_PRESUNTA_MESI",
trunc(MONTHS_BETWEEN(sysdate, ADD_MONTHS(ADD_MONTHS(sm.data_reato_sius, - nvl(sm.eta_presunta_anni,0) * 12), -nvl(sm.eta_presunta_mesi,0) ) ) / 12)
ETA_PRESUNTA_ORA,
sm.data_reato_sius
from V_SOGGETTO_MAGGIORENNE sm
) TB_SOGGETTI
, (select fs."ID_FASCICOLO_SIEP",
rf."NUM_REATI",
rf."PRIMO_REATO",
rf."ULTIMO_REATO",
fs.sog_id_soggetto ID_SOGGETTO,
sm."DATA_MAGGIORENNE",
sm."ETA_SOGGETTO_ORA",
sm."DATA_NASCITA_PRESUNTA",
sm."ETA_PRESUNTA_ANNI",
sm."ETA_PRESUNTA_MESI",
nvl(trunc(MONTHS_BETWEEN(sysdate, ADD_MONTHS(ADD_MONTHS(sm.data_reato_sius, - nvl(sm.eta_presunta_anni,0) * 12), -nvl(sm.eta_presunta_mesi,0) ) ) / 12),
trunc(MONTHS_BETWEEN(sysdate, ADD_MONTHS(ADD_MONTHS(rf.primo_reato, - nvl(sm.eta_presunta_anni,0) * 12), -nvl(sm.eta_presunta_mesi,0) ) ) / 12))
ETA_PRESUNTA_ORA,
sm.data_reato_sius
from FASCICOLO_SIEP         fs,
V_REATI_FASCICOLO      rf,
V_SOGGETTO_MAGGIORENNE sm
where fs.id_fascicolo_siep = rf.fas_sie_id_fascicolo_siep
and fs.sog_id_soggetto = sm.id_soggetto
) TB_SOGGETTI_SIES
, ( select fs."ID_FASCICOLO_SIEP",
rf."NUM_REATI",
rf."PRIMO_REATO",
rf."ULTIMO_REATO",
a.sog_id_soggetto ID_SOGGETTO,
sm."DATA_MAGGIORENNE",
sm."ETA_SOGGETTO_ORA" ETA_SOGGETTO_ORA_SIGE,
smSIEP."ETA_SOGGETTO_ORA" ETA_SOGGETTO_ORA_SIEP,
sm."DATA_NASCITA_PRESUNTA",
sm."ETA_PRESUNTA_ANNI",
sm."ETA_PRESUNTA_MESI",
fs.ID_FASCICOLO_SIEP,
nvl(trunc(MONTHS_BETWEEN(sysdate, ADD_MONTHS(ADD_MONTHS(sm.data_reato_sius, - nvl(sm.eta_presunta_anni,0) * 12), -nvl(sm.eta_presunta_mesi,0) ) ) / 12),
trunc(MONTHS_BETWEEN(sysdate, ADD_MONTHS(ADD_MONTHS(rf.primo_reato, - nvl(sm.eta_presunta_anni,0) * 12), -nvl(sm.eta_presunta_mesi,0) ) ) / 12))
ETA_PRESUNTA_ORA,
sm.data_reato_sius
from FASCICOLO_SIEP         fs,
V_REATI_FASCICOLO      rf,
V_SOGGETTO_MAGGIORENNE sm,
V_SOGGETTO_MAGGIORENNE smSIEP,
fascicolo_sige a,
fas_sige_sentenza b
where fs.id_fascicolo_siep = rf.fas_sie_id_fascicolo_siep
and a.sog_id_soggetto = sm.id_soggetto
and fs.sog_id_soggetto = smSIEP.id_soggetto
and b.fas_id_fascicolo_sige = a.id_fascicolo_sige
and fs.id_fascicolo_siep = b.fas_sie_id_fascicolo_siep
) TB_SOGGETTI_SIGE
WHERE 1=1
AND TB_SOGGETTI.ID_SOGGETTO = TB_SOGGETTI_SIES.ID_SOGGETTO(+)
AND TB_SOGGETTI.ID_SOGGETTO = TB_SOGGETTI_SIGE.ID_SOGGETTO(+);

v_soggetto_maggiorenne_sige

create or replace view v_soggetto_maggiorenne_sige as
select distinct
tb."ID_SOGGETTO" id_soggetto,
null data_maggiorenne,
(case
when ETA_SOGGETTO_ORA is not null then
ETA_SOGGETTO_ORA
when ETA_PRESUNTA_ORA is not null then
ETA_PRESUNTA_ORA
else  trunc(((nvl(eta_presunta_anni,0) * 12) + nvl(eta_presunta_mesi,0)) /12)
end) as eta_soggetto_ora,
null eta_presunta_anni,
null eta_presunta_mesi,
data_nascita_presunta,
data_reato_sius
from (select null "ID_FASCICOLO_SIEP",
null "NUM_REATI",
null "PRIMO_REATO",
null "ULTIMO_REATO",
a.sog_id_soggetto ID_SOGGETTO,
sm."DATA_MAGGIORENNE",
sm."ETA_SOGGETTO_ORA",
sm."DATA_NASCITA_PRESUNTA",
sm."ETA_PRESUNTA_ANNI",
sm."ETA_PRESUNTA_MESI",
trunc(MONTHS_BETWEEN(sysdate, ADD_MONTHS(ADD_MONTHS(sm.data_reato_sius, - nvl(sm.eta_presunta_anni,0) * 12), -nvl(sm.eta_presunta_mesi,0) ) ) / 12)
ETA_PRESUNTA_ORA,
sm.data_reato_sius
from V_SOGGETTO_MAGGIORENNE sm,
fascicolo_sige a,
fas_sige_sentenza b
where a.sog_id_soggetto = sm.id_soggetto
and b.fas_id_fascicolo_sige(+)= a.id_fascicolo_sige
) tb;

v_sogsige_eta

create or replace view v_sogsige_eta as
select fs.ID_FASCICOLO_SIGE,
fs.sog_id_soggetto   COD_SOGGETTO,
SM.ETA_SOGGETTO_ORA  eta_soggetto_ora
from FASCICOLO_SIGE fs, V_SOGGETTO_MAGGIORENNE_NEW sm
where fs.sog_id_soggetto = sm.id_soggetto;

v_sogsige_eta_sige

create or replace view v_sogsige_eta_sige as
select fs.ID_FASCICOLO_SIGE,
fs.sog_id_soggetto   COD_SOGGETTO,
SM.ETA_SOGGETTO_ORA  eta_soggetto_ora
from FASCICOLO_SIGE fs, V_SOGGETTO_MAGGIORENNE_SIGE sm
where fs.sog_id_soggetto = sm.id_soggetto;

V_SOGSIUS_ETA

CREATE OR REPLACE FORCE VIEW SIESTO.V_SOGSIUS_ETA  AS
select tb."ID_FASCICOLO_SIUS" as id_fascicolo_sius,
tb."ID_SOGGETTO" COD_SOGGETTO,
(case
when ETA_SOGGETTO_ORA is not null then
ETA_SOGGETTO_ORA
else
ETA_PRESUNTA_ORA
end) as eta_ora
from (select fs.id_fascicolo_sius,
sm."ID_SOGGETTO",
sm."DATA_MAGGIORENNE",
sm."ETA_SOGGETTO_ORA",
sm."DATA_NASCITA_PRESUNTA",
sm."ETA_PRESUNTA_ANNI",
sm."ETA_PRESUNTA_MESI",
trunc(MONTHS_BETWEEN(sysdate, ADD_MONTHS(ADD_MONTHS(sm.data_reato_sius, - nvl(sm.eta_presunta_anni,0) * 12), -nvl(sm.eta_presunta_mesi,0) ) ) / 12) ETA_PRESUNTA_ORA
from FASCICOLO_SIUS         fs,
V_SOGGETTO_MAGGIORENNE sm
where fs.sog_id_soggetto = sm.id_soggetto) tb;

V_STAT_RIS

CREATE OR REPLACE FORCE VIEW SIESTO.V_STAT_RIS
(num_res, data_stat, res_status)
AS
SELECT a.num_res,b.max_data,res_status
FROM W_STAT_RIS a,(SELECT num_res,MAX(data_stat) max_data
FROM W_STAT_RIS
GROUP BY num_res
ORDER BY num_res) b
WHERE a.num_res=b.num_res
AND a.data_stat=b.max_data;

V_UTENTI_COMPLETA

CREATE OR REPLACE FORCE VIEW SIESTO.V_UTENTI_COMPLETA
(cod_ufficio, cod_tipo_ufficio, cod_distretto, cod_provincia, cod_comune, data_caricamento_rege, cod_ufficio_competente, indirizzo, cap_ufficio, telefono, fax, e_mail, descr_comune, descr_provincia, descr_tipo_ufficio, cod_utente, cognome, nome, pwd, data_fine_validita, data_ora_connessione, cod_operatore_inserimento, data_inserimento, cod_operatore_aggiornamento, data_aggiornamento, data_ultima_modifica_pwd, ip, cod_profilo, descrizione, dt_fin_ute_pro, utente_tel, utente_fax, utente_e_mail)
AS
SELECT   uff.cod_ufficio, uff.cod_tipo_ufficio, uff.cod_distretto,
uff.cod_provincia, uff.cod_comune, uff.data_caricamento_rege,
uff.cod_ufficio_competente, uff.indirizzo, uff.cap cap_ufficio,
uff.telefono, uff.fax, uff.e_mail, com.descrizione descr_comune,
descr_provincia.rv_meaning descr_provincia,
descr_tipo_ufficio.rv_meaning descr_tipo_ufficio, ute.cod_utente,
ute.cognome, ute.nome, ute.pwd, ute.data_fine_validita,
ute.data_ora_connessione, ute.cod_operatore_inserimento,
ute.data_inserimento, ute.cod_operatore_aggiornamento,
ute.data_aggiornamento, ute.data_ultima_modifica_pwd, ute.ip,
pro.cod_profilo, pro.descrizione,
ute_pro.data_fine_validita dt_fin_ute_pro,ute.telefono,ute.fax,ute.e_mail
FROM UFFICIO uff,
UTENTE_UFFICIO ute_uff,
COMUNE com,
CG_REF_CODES descr_provincia,
CG_REF_CODES descr_tipo_ufficio,
UTENTE ute,
PROFILO pro,
UTENTE_PROFILO ute_pro
WHERE (ute_uff.uff_cod_ufficio = uff.cod_ufficio)
AND (ute_uff.ute_cod_utente = ute.cod_utente)
AND (    (ute_uff.data_inizio_validita <= SYSDATE)
AND (   ute_uff.data_fine_validita IS NULL
OR ute_uff.data_fine_validita >= SYSDATE
)
)
AND (com.cod_comune = uff.cod_comune)
AND (descr_tipo_ufficio.rv_domain = 'TIPO_UFFICIO')
AND (descr_tipo_ufficio.rv_low_value = uff.cod_tipo_ufficio)
AND (descr_provincia.rv_domain = 'PROVINCIA')
AND (descr_provincia.rv_low_value = uff.cod_provincia)
AND (pro.cod_profilo = ute_pro.prf_cod_profilo)
AND (ute_pro.ute_cod_utente = ute.cod_utente)
ORDER BY ute.cognome,ute.nome;

AVVOCATO_MAT

CREATE MATERIALIZED VIEW SIESTO.AVVOCATO_MAT
REFRESH FORCE ON DEMAND
AS
SELECT "Q"."ID_AVVOCATO" "ID_AVVOCATO","Q"."COGNOME" "COGNOME","Q"."NOME" "NOME","Q"."FORO" "FORO","Q"."INDIRIZZO" "INDIRIZZO","Q"."TELEFONO" "TELEFONO","Q"."FAX" "FAX","Q"."E_MAIL" "E_MAIL","Q"."COD_COMUNE_RESIDENZA" "COD_COMUNE_RESIDENZA","Q"."COD_LUOGO_NASCITA" "COD_LUOGO_NASCITA","Q"."DATA_NASCITA" "DATA_NASCITA","Q"."DATA_SOSPESO_FINO_AL" "DATA_SOSPESO_FINO_AL","Q"."DATA_RADIATO_DAL" "DATA_RADIATO_DAL","Q"."COD_NON_ATTIVITA" "COD_NON_ATTIVITA","Q"."NOTE" "NOTE","Q"."FLAG_CANCELLATO" "FLAG_CANCELLATO","Q"."COD_UFFICIO_APPARTENENZA" "COD_UFFICIO_APPARTENENZA","Q"."COD_OPERATORE_INSERIMENTO" "COD_OPERATORE_INSERIMENTO","Q"."DATA_INSERIMENTO" "DATA_INSERIMENTO","Q"."COD_UFFICIO_INSERIMENTO" "COD_UFFICIO_INSERIMENTO","Q"."COD_OPERATORE_AGGIORNAMENTO" "COD_OPERATORE_AGGIORNAMENTO","Q"."DATA_AGGIORNAMENTO" "DATA_AGGIORNAMENTO","Q"."COD_UFFICIO_AGGIORNAMENTO" "COD_UFFICIO_AGGIORNAMENTO","Q"."COD_FISCALE" "COD_FISCALE","Q"."PROVINCIA" "PROVINCIA","Q"."CAP" "CAP","Q"."ID_AVVOCATO_STANDARD" "ID_AVVOCATO_STANDARD","Q"."FLAG_VISUALIZZA" "FLAG_VISUALIZZA" FROM "AVVOCATO" "Q" WHERE ("Q"."FORO"='ACQUI TERME' OR "Q"."FORO"='ALBA' OR "Q"."FORO"='ARIANO IRPINO' OR "Q"."FORO"='BASSANO DEL GRAPPA' OR "Q"."FORO"='CAMERINO' OR "Q"."FORO"='CASALE MONFERRATO' OR "Q"."FORO"='CHIAVARI' OR "Q"."FORO"='CREMA' OR "Q"."FORO"='LUCERA' OR "Q"."FORO"='MELFI' OR "Q"."FORO"='MISTRETTA' OR "Q"."FORO"='MODICA' OR "Q"."FORO"='MONDOVI''' OR "Q"."FORO"='MONTEPULCIANO' OR "Q"."FORO"='NICOSIA' OR "Q"."FORO"='ORVIETO' OR "Q"."FORO"='PINEROLO' OR "Q"."FORO"='ROSSANO' OR "Q"."FORO"='SALA CONSILINA' OR "Q"."FORO"='SALUZZO' OR "Q"."FORO"='SANREMO' OR "Q"."FORO"='SANT''ANGELO DEI LOMBARDI' OR "Q"."FORO"='TOLMEZZO' OR "Q"."FORO"='TORTONA' OR "Q"."FORO"='VIGEVANO' OR "Q"."FORO"='VOGHERA') AND "Q"."COD_UFFICIO_APPARTENENZA"<>'00000';