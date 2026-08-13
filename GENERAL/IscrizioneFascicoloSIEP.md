---
uniqueName: iscrizionefascicolosiep
displayName: "IscrizioneFascicoloSIEP"
category: "GENERAL"
tags: []
---

# IscrizioneFascicoloSIEP

## Indice

|   Unnamed: 0 | Unnamed: 1                         |
|-------------:|:-----------------------------------|
|          nan | INDICE                             |
|          nan | nan                                |
|          nan | 1.   Titolo Esecutivo              |
|          nan | 2.   Soggetto                      |
|          nan | 3.   Procedimento                  |
|          nan | 4.   Pena Complessiva              |
|          nan | 5.   Magistrato Competente         |
|          nan | 6.   Reato                         |
|          nan | 7.   Difensore                     |
|          nan | 8.   Posizione Giuridica           |
|          nan | 9.   Pena Accessoria               |
|          nan | 10.   Misura di Sicurezza          |
|          nan | 11.   Circostanza                  |
|          nan | 12.   Notizia di Reato             |
|          nan | 13.   Beneficio                    |
|          nan | 14.   Revoca del Beneficio         |
|          nan | 15.   Misura cautelare             |
|          nan | 16.   Residenza                    |
|          nan | 17.   Domicilio                    |
|          nan | 18.   Pagamento Pena Pecuniaria    |
|          nan | 19.   Civilmente Obbligato         |
|          nan | 20.   Continuazione Altre Sentenze |


## TitoloEsecutivo

| Campo                                 | Obbligatorio   | Tipo       | Sezione                 | Note                                                                   | Unnamed: 5                                            |
|:--------------------------------------|:---------------|:-----------|:------------------------|:-----------------------------------------------------------------------|:------------------------------------------------------|
| Anno R.G.N.R.                         | *              | input text | Dati generali           | Parte di "Anno/Numero R.G.N.R."                                        | nan                                                   |
| Numero R.G.N.R.                       | *              | input text | Dati generali           | Parte di "Anno/Numero R.G.N.R."                                        | nan                                                   |
| Anno Reg.Gen.                         | nan            | input text | Dati generali           | Parte di "Anno/Numero Reg.Gen."                                        | nan                                                   |
| Numero Reg.Gen.                       | nan            | input text | Dati generali           | Parte di "Anno/Numero Reg.Gen."                                        | nan                                                   |
| Tipo Registro Generale                | *              | select     | Dati generali           | Obbligatorio da controllo JavaScript Verify()                          | nan                                                   |
| Sede PM                               | *              | input text | Dati generali           | Marcato con (*) in pagina                                              | talvolta readonly poiché già preinserito nella pagina |
| Giorno Data Sentenza                  | *              | input text | Sentenza da Eseguire    | Parte di "Data Sentenza"                                               | nan                                                   |
| Mese Data Sentenza                    | *              | input text | Sentenza da Eseguire    | Parte di "Data Sentenza"                                               | nan                                                   |
| Anno Data Sentenza                    | *              | input text | Sentenza da Eseguire    | Parte di "Data Sentenza"                                               | nan                                                   |
| Anno Sentenza                         | *              | input text | Sentenza da Eseguire    | Parte di "Anno/Numero Sentenza"                                        | nan                                                   |
| Numero Sentenza                       | *              | input text | Sentenza da Eseguire    | Parte di "Anno/Numero Sentenza"                                        | nan                                                   |
| Autorità Emittente                    | *              | select     | Sentenza da Eseguire    | nan                                                                    | nan                                                   |
| Tipo Rito                             | nan            | select     | Sentenza da Eseguire    | Visibile solo per alcune autorità emittenti                            | nan                                                   |
| Luogo Emittente                       | *              | input text | Sentenza da Eseguire    | nan                                                                    | nan                                                   |
| Sezione Autorità Emittente            | nan            | input text | Sentenza da Eseguire    | nan                                                                    | nan                                                   |
| Tipo Provvedimento                    | nan            | select     | Altro Grado di Giudizio | nan                                                                    | nan                                                   |
| Tipo Sentenza                         | nan            | select     | Altro Grado di Giudizio | Condizionalmente obbligatorio se si compila la sentenza di riferimento | nan                                                   |
| Giorno Data Sentenza di Riferimento   | nan            | input text | Altro Grado di Giudizio | Condizionalmente obbligatorio se si compila la sentenza di riferimento | nan                                                   |
| Mese Data Sentenza di Riferimento     | nan            | input text | Altro Grado di Giudizio | Condizionalmente obbligatorio se si compila la sentenza di riferimento | nan                                                   |
| Anno Data Sentenza di Riferimento     | nan            | input text | Altro Grado di Giudizio | Condizionalmente obbligatorio se si compila la sentenza di riferimento | nan                                                   |
| Anno Sentenza/Ordinanza Riferimento   | nan            | input text | Altro Grado di Giudizio | nan                                                                    | nan                                                   |
| Numero Sentenza/Ordinanza Riferimento | nan            | input text | Altro Grado di Giudizio | nan                                                                    | nan                                                   |
| Autorità Sentenza Riferimento         | nan            | select     | Altro Grado di Giudizio | Condizionalmente obbligatorio se si compila la sentenza di riferimento | nan                                                   |
| Tipo Rito Riferimento                 | nan            | select     | Altro Grado di Giudizio | Visibile solo per alcune autorità emittenti                            | nan                                                   |
| Luogo Sentenza Riferimento            | nan            | input text | Altro Grado di Giudizio | Condizionalmente obbligatorio se si compila la sentenza di riferimento | nan                                                   |
| Sezione Autorità Riferimento          | nan            | input text | Altro Grado di Giudizio | nan                                                                    | nan                                                   |
| Tipo Provvedimento Cassazione         | nan            | select     | Decisione Cassazione    | nan                                                                    | nan                                                   |
| Anno Re.Ge. Cassazione                | nan            | input text | Decisione Cassazione    | Campo name=ANNOREGECAS                                                 | nan                                                   |
| Numero Re.Ge. Cassazione              | nan            | input text | Decisione Cassazione    | Campo name=NUMREGECAS                                                  | nan                                                   |
| Anno Sentenza Cassazione              | nan            | input text | Decisione Cassazione    | nan                                                                    | nan                                                   |
| Numero Sentenza Cassazione            | nan            | input text | Decisione Cassazione    | nan                                                                    | nan                                                   |
| Anno Raccolta Generale                | nan            | input text | Decisione Cassazione    | nan                                                                    | nan                                                   |
| Numero Raccolta Generale              | nan            | input text | Decisione Cassazione    | nan                                                                    | nan                                                   |
| Dispositivo Cassazione                | nan            | select     | Decisione Cassazione    | nan                                                                    | nan                                                   |
| Note                                  | nan            | textarea   | Note Aggiuntive         | nan                                                                    | nan                                                   |
| nan                                   | nan            | nan        | nan                     | nan                                                                    | nan                                                   |
| Indice                                | nan            | nan        | nan                     | nan                                                                    | nan                                                   |


## Soggetto

| Etichetta                    | Nome tecnico                     | Tipo       | Obbligatorio   | Condizione                    | Note                                                 |
|:-----------------------------|:---------------------------------|:-----------|:---------------|:------------------------------|:-----------------------------------------------------|
| Cognome                      | CAMPO_COGNOME                    | input text | *              | Sempre                        | Max 35 caratteri                                     |
| Nome                         | CAMPO_NOME                       | input text | *              | Sempre                        | Max 35 caratteri                                     |
| Sesso                        | CAMPO_SESSO                      | select     | *              | Sempre                        | nan                                                  |
| Data di nascita - Giorno     | CAMPO_GIORNO_DATA_NASCITA        | input text | nan            | Condizionale                  | Parte della data di nascita                          |
| Data di nascita - Mese       | CAMPO_MESE_DATA_NASCITA          | input text | nan            | Condizionale                  | Parte della data di nascita                          |
| Data di nascita - Anno       | CAMPO_ANNO_DATA_NASCITA          | input text | nan            | Condizionale                  | Parte della data di nascita                          |
| Data Presunta                | CAMPO_DATA_NASCITA_PRESUNTA      | select     | nan            | Condizionale                  | Valori gestiti da select                             |
| Età Presunta - Anni          | CAMPO_ETA_PRESUNTA_ANNI          | input text | nan            | Condizionale                  | Richiesta se manca la data di nascita in alcuni casi |
| Età Presunta - Mesi          | CAMPO_ETA_PRESUNTA_MESI          | input text | nan            | Condizionale                  | Deve essere minore di 12                             |
| Data commesso reato - Giorno | CAMPO_GIORNO_DATA_COMMESSO_REATO | input text | nan            | Condizionale                  | Presente solo per alcuni profili/uffici              |
| Data commesso reato - Mese   | CAMPO_MESE_DATA_COMMESSO_REATO   | input text | nan            | Condizionale                  | Presente solo per alcuni profili/uffici              |
| Data commesso reato - Anno   | CAMPO_ANNO_DATA_COMMESSO_REATO   | input text | nan            | Condizionale                  | Presente solo per alcuni profili/uffici              |
| Comune Nascita               | CAMPO_COD_COMUNE_NASCITA         | input text | *              | Se Stato di Nascita = Italia  | Con lookup comuni                                    |
| Stato Cittadinanza           | CAMPO_NAZIONALITA                | select     | nan            | Facoltativo                   | nan                                                  |
| Stato di Nascita             | CAMPO_COD_STATO_NASCITA          | select     | nan            | Facoltativo                   | nan                                                  |
| Luogo di Nascita Estero      | CAMPO_DESC_COMUNE_NASCITA_ESTERO | input text | nan            | Se Stato di Nascita != Italia | Comune estero testuale                               |
| Paternità                    | CAMPO_PATERNITA                  | input text | nan            | Facoltativo                   | Max 35 caratteri                                     |
| Cognome Madre                | CAMPO_COGNOME_MADRE              | input text | nan            | Facoltativo                   | Max 35 caratteri                                     |
| Nome Madre                   | CAMPO_NOME_MADRE                 | input text | nan            | Facoltativo                   | Max 35 caratteri                                     |
| Codice Fiscale               | CAMPO_COD_FISCALE                | input text | nan            | Facoltativo                   | Max 16 caratteri                                     |
| Atto Nascita                 | CAMPO_ATTO_NASCITA               | input text | nan            | Facoltativo                   | Max 10 caratteri                                     |
| Codice CUI                   | CAMPO_COD_AFIS                   | input text | nan            | Facoltativo                   | Max 7 caratteri                                      |
| Note                         | CAMPO_NOTE                       | textarea   | nan            | Facoltativo                   | nan                                                  |
| nan                          | nan                              | nan        | nan            | nan                           | nan                                                  |
| Indice                       | nan                              | nan        | nan            | nan                           | nan                                                  |


## Procedimento

| Campo                                     | Obbligatorio   | Tipo       | Sezione              | Note                                                                    |
|:------------------------------------------|:---------------|:-----------|:---------------------|:------------------------------------------------------------------------|
| Giorno Data Iscrizione Procedimento       | *              | input text | Dati procedimento    | Obbligatorio in assegnazione manuale, hidden in assegnazione automatica |
| Mese Data Iscrizione Procedimento         | *              | input text | Dati procedimento    | Obbligatorio in assegnazione manuale, hidden in assegnazione automatica |
| Anno Data Iscrizione Procedimento         | *              | input text | Dati procedimento    | Obbligatorio in assegnazione manuale, hidden in assegnazione automatica |
| Giorno Data Arrivo Atto                   | nan            | input text | Dati procedimento    | Data validata da JavaScript                                             |
| Mese Data Arrivo Atto                     | nan            | input text | Dati procedimento    | Data validata da JavaScript                                             |
| Anno Data Arrivo Atto                     | nan            | input text | Dati procedimento    | Data validata da JavaScript                                             |
| Giorno Data Irrevocabilità / Esecutivo il | nan            | input text | Dati procedimento    | Data validata da JavaScript                                             |
| Mese Data Irrevocabilità / Esecutivo il   | nan            | input text | Dati procedimento    | Data validata da JavaScript                                             |
| Anno Data Irrevocabilità / Esecutivo il   | nan            | input text | Dati procedimento    | Data validata da JavaScript                                             |
| Anno Procedimento                         | *              | input text | Assegnazione manuale | Obbligatorio solo se assegnazione_manuale = S                           |
| Numero Procedimento                       | *              | input text | Assegnazione manuale | Obbligatorio solo se assegnazione_manuale = S                           |
| Assegna numerazione speciale              | nan            | checkbox   | Assegnazione manuale | Mostra azioni R.E.S. / P.T. e disabilita anno/numero procedimento       |
| Classe I                                  | nan            | radio      | Classe procedimento  | Opzione radio gruppo tipo                                               |
| Classe II                                 | nan            | radio      | Classe procedimento  | Opzione radio gruppo tipo                                               |
| Classe III                                | nan            | radio      | Classe procedimento  | Opzione radio gruppo tipo                                               |
| Classe IV                                 | nan            | radio      | Classe procedimento  | Opzione radio gruppo tipo                                               |
| Classe V                                  | nan            | radio      | Classe procedimento  | Opzione radio gruppo tipo                                               |
| Classe VI                                 | nan            | radio      | Classe procedimento  | Opzione radio gruppo tipo                                               |
| Classe VII                                | nan            | radio      | Classe procedimento  | Opzione radio gruppo tipo                                               |
| Note Procedimento                         | nan            | textarea   | Note                 | nan                                                                     |


## PenaComplessiva

| Campo                                            |   Obbligatorio | Tipo         | Sezione                               | Note                                                                    |
|:-------------------------------------------------|---------------:|:-------------|:--------------------------------------|:------------------------------------------------------------------------|
| Anni Reclusione                                  |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Mesi Reclusione                                  |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Giorni Reclusione                                |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Intero Multa                                     |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Decimale Multa                                   |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Valuta Multa                                     |            nan | select       | Pena                                  | nan                                                                     |
| Anni Arresto                                     |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Mesi Arresto                                     |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Giorni Arresto                                   |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Intero Ammenda                                   |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Decimale Ammenda                                 |            nan | input text   | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Valuta Ammenda                                   |            nan | select       | Pena                                  | nan                                                                     |
| Ergastolo / Tipo Pena Detentiva                  |            nan | select       | Pena                                  | Almeno un campo della sezione Pena deve essere valorizzato              |
| Anni Isolamento Diurno                           |            nan | input text   | Pena                                  | nan                                                                     |
| Mesi Isolamento Diurno                           |            nan | input text   | Pena                                  | nan                                                                     |
| Giorni Isolamento Diurno                         |            nan | input text   | Pena                                  | nan                                                                     |
| Giorno Data Prescrizione                         |            nan | input text   | Pena                                  | Data opzionale ma validata                                              |
| Mese Data Prescrizione                           |            nan | input text   | Pena                                  | Data opzionale ma validata                                              |
| Anno Data Prescrizione                           |            nan | input text   | Pena                                  | Data opzionale ma validata                                              |
| Sanzione Sostitutiva                             |            nan | checkbox     | Sanzione Sostitutiva                  | Se selezionata attiva obblighi condizionali                             |
| Tipo Sanzione Sostitutiva                        |            nan | select       | Sanzione Sostitutiva                  | Obbligatorio se checkbox Sanzione Sostitutiva selezionato               |
| Anni Sanzione Sostitutiva                        |            nan | input text   | Sanzione Sostitutiva                  | Obbligatorio in alternativa alla pena pecuniaria secondo il tipo scelto |
| Mesi Sanzione Sostitutiva                        |            nan | input text   | Sanzione Sostitutiva                  | Obbligatorio in alternativa alla pena pecuniaria secondo il tipo scelto |
| Giorni Sanzione Sostitutiva                      |            nan | input text   | Sanzione Sostitutiva                  | Obbligatorio in alternativa alla pena pecuniaria secondo il tipo scelto |
| Intero Pena Pecuniaria Sostitutiva Multa         |            nan | input text   | Sanzione Sostitutiva                  | Obbligatorio per tipo pecuniario se selezionata                         |
| Decimale Pena Pecuniaria Sostitutiva Multa       |            nan | input text   | Sanzione Sostitutiva                  | Obbligatorio per tipo pecuniario se selezionata                         |
| Valuta Pena Pecuniaria Sostitutiva Multa/Ammenda |            nan | select       | Sanzione Sostitutiva                  | nan                                                                     |
| Intero Pena Pecuniaria Sostitutiva Ammenda       |            nan | input text   | Sanzione Sostitutiva                  | Obbligatorio per tipo pecuniario se selezionata                         |
| Decimale Pena Pecuniaria Sostitutiva Ammenda     |            nan | input text   | Sanzione Sostitutiva                  | Obbligatorio per tipo pecuniario se selezionata                         |
| Pena Sostitutiva                                 |            nan | checkbox     | Pene sostitutive Pene Detentive Brevi | Se selezionata attiva obblighi condizionali                             |
| Tipo Pena Sostitutiva                            |            nan | select       | Pene sostitutive Pene Detentive Brevi | Obbligatorio se checkbox Pena Sostitutiva selezionato                   |
| Anni Pena Sostitutiva                            |            nan | input text   | Pene sostitutive Pene Detentive Brevi | Obbligatorio in alternativa alla pena pecuniaria secondo il tipo scelto |
| Mesi Pena Sostitutiva                            |            nan | input text   | Pene sostitutive Pene Detentive Brevi | Obbligatorio in alternativa alla pena pecuniaria secondo il tipo scelto |
| Giorni Pena Sostitutiva                          |            nan | input text   | Pene sostitutive Pene Detentive Brevi | Obbligatorio in alternativa alla pena pecuniaria secondo il tipo scelto |
| Intero Pena Pecuniaria Sostitutiva               |            nan | input text   | Pene sostitutive Pene Detentive Brevi | Obbligatorio per tipo pecuniario se selezionata                         |
| Decimale Pena Pecuniaria Sostitutiva             |            nan | input text   | Pene sostitutive Pene Detentive Brevi | Obbligatorio per tipo pecuniario se selezionata                         |
| Confisca per equivalente                         |            nan | checkbox     | Importo da Pagare Include             | nan                                                                     |
| Continuazione con altre sentenze                 |            nan | checkbox     | Continuazione                         | Se selezionata attiva 2 blocchi continuazione                           |
| Tipo Continuazione riga 1                        |            nan | input/select | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Anno Sentenza riga 1                             |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Numero Sentenza riga 1                           |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Giorno Data Sentenza riga 1                      |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Mese Data Sentenza riga 1                        |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Anno Data Sentenza riga 1                        |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Autorità Sentenza riga 1                         |            nan | select       | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Luogo Sentenza riga 1                            |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Anno R.G.N.R. riga 1                             |            nan | input text   | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Numero R.G.N.R. riga 1                           |            nan | input text   | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Anno Reg. Gen. riga 1                            |            nan | input text   | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Numero Reg. Gen. riga 1                          |            nan | input text   | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Tipo Reg. Gen. riga 1                            |            nan | select       | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Tipo Continuazione riga 2                        |            nan | input/select | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Anno Sentenza riga 2                             |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Numero Sentenza riga 2                           |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Giorno Data Sentenza riga 2                      |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Mese Data Sentenza riga 2                        |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Anno Data Sentenza riga 2                        |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Autorità Sentenza riga 2                         |            nan | select       | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Luogo Sentenza riga 2                            |            nan | input text   | Continuazione                         | Condizionale se flag continuazione selezionato                          |
| Anno R.G.N.R. riga 2                             |            nan | input text   | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Numero R.G.N.R. riga 2                           |            nan | input text   | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Anno Reg. Gen. riga 2                            |            nan | input text   | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Numero Reg. Gen. riga 2                          |            nan | input text   | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| Tipo Reg. Gen. riga 2                            |            nan | select       | Continuazione                         | Condizionale se valorizzati dati R.G.                                   |
| nan                                              |            nan | nan          | nan                                   | nan                                                                     |
| Indice                                           |            nan | nan          | nan                                   | nan                                                                     |


## MagistratoCompetente

| Campo                         | Obbligatorio   | Tipo       | Sezione                 | Note                                                               |
|:------------------------------|:---------------|:-----------|:------------------------|:-------------------------------------------------------------------|
| Cognome                       | *              | input text | Magistrato Assegnatario | Readonly in pagina, valorizzato tramite popup selezione magistrato |
| Nome                          | *              | input text | Magistrato Assegnatario | Readonly in pagina, valorizzato tramite popup selezione magistrato |
| Giorno Data Inizio Competenza | *              | input text | Magistrato Assegnatario | Parte della data di inizio competenza                              |
| Mese Data Inizio Competenza   | *              | input text | Magistrato Assegnatario | Parte della data di inizio competenza                              |
| Anno Data Inizio Competenza   | nan            | input text | Magistrato Assegnatario | Validato come numerico con range 1900-3000                         |
| nan                           | nan            | nan        | nan                     | nan                                                                |
| Indice                        | nan            | nan        | nan                     | nan                                                                |


## Reato

| Sezione                         | Etichetta campo      | Nome campo (name)              | Tipo     | Obbligatorio   | Note obbligatorietà                                                |
|:--------------------------------|:---------------------|:-------------------------------|:---------|:---------------|:-------------------------------------------------------------------|
| Reato                           | Numero Reato         | CAMPO_PROGR_NUMERO_MANUALE     | text     | nan            | nan                                                                |
| Riferimenti normativi (5 righe) | Fonte                | CAMPO_COD_FONTE                | select   | *              | Almeno una coppia Fonte+Articolo deve essere valorizzata           |
| Riferimenti normativi (5 righe) | Anno                 | CAMPO_ANNO_FONTE               | text     | nan            | nan                                                                |
| Riferimenti normativi (5 righe) | Numero               | CAMPO_NUMERO_FONTE             | text     | nan            | nan                                                                |
| Riferimenti normativi (5 righe) | Articolo             | CAMPO_ARTICOLO                 | text     | *              | Almeno una coppia Fonte+Articolo deve essere valorizzata           |
| Riferimenti normativi (5 righe) | Art. qualificante    | CAMPO_COD_SOTTONUMERAZIONE     | select   | nan            | nan                                                                |
| Riferimenti normativi (5 righe) | Comma                | CAMPO_COMMA                    | text     | *              | Obbligatorio se valorizzato Comma qualificante                     |
| Riferimenti normativi (5 righe) | Comma qualificante   | CAMPO_COMMA_QUALIFICANTE       | select   | nan            | nan                                                                |
| Riferimenti normativi (5 righe) | Lettera              | CAMPO_LETTERA                  | text     | nan            | nan                                                                |
| Riferimenti normativi (5 righe) | Numero               | CAMPO_NUMERO                   | text     | nan            | nan                                                                |
| Checkbox cablati2               | 110 CP               | cablati2                       | checkbox | nan            | nan                                                                |
| Checkbox cablati2               | 56 CP                | cablati2                       | checkbox | nan            | nan                                                                |
| Checkbox cablati2               | 81 CP C1             | cablati2                       | checkbox | nan            | nan                                                                |
| Checkbox cablati2               | 81 CP C2             | cablati2                       | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N1             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N2             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N3             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N4             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N5             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N6             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N7             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N8             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N9             | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N10            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 61 CP N11            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 112 CP C1            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 112 CP C2            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 112 CP C3            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 112 CP C4            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 113 CP               | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 114 CP               | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 116 CP               | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 117 CP               | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N1            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N2            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N3            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N4            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N5            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N6            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N7            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N8            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N9            | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N10           | cablati                        | checkbox | nan            | nan                                                                |
| Checkbox cablati                | 625 CP N11           | cablati                        | checkbox | nan            | nan                                                                |
| Dettaglio reato                 | Tipo Reato           | CAMPO_COD_TIPO_REATO           | select   | nan            | nan                                                                |
| Dettaglio reato                 | Luogo Reato          | CAMPO_DESC_LUOGO               | text     | nan            | Se valorizzato, è obbligatorio indicare anche Periodo Consumazione |
| Dettaglio reato                 | Periodo Consumazione | CAMPO_COD_PERIODO_CONSUMAZIONE | select   | *              | Obbligatorio se è valorizzato Luogo Reato o una delle date         |
| Date                            | Data1 - Giorno       | CAMPO_GIORNO_DATA_INIZIO       | text     | *              | Obbligatorio in base al valore di Periodo Consumazione             |
| Date                            | Data1 - Mese         | CAMPO_MESE_DATA_INIZIO         | text     | nan            | nan                                                                |
| Date                            | Data1 - Anno         | CAMPO_ANNO_DATA_INIZIO         | text     | *              | Obbligatorio in base al valore di Periodo Consumazione             |
| Date                            | Data2 - Giorno       | CAMPO_GIORNO_DATA_FINE         | text     | nan            | nan                                                                |
| Date                            | Data2 - Mese         | CAMPO_MESE_DATA_FINE           | text     | nan            | nan                                                                |
| Date                            | Data2 - Anno         | CAMPO_ANNO_DATA_FINE           | text     | *              | Obbligatorio in base al valore di Periodo Consumazione             |
| Dettaglio reato                 | Note                 | CAMPO_NOTE                     | textarea | nan            | nan                                                                |
| nan                             | nan                  | nan                            | nan      | nan            | nan                                                                |
| Indice                          | nan                  | nan                            | nan      | nan            | nan                                                                |


## Difensore

| Campo                                           | Obbligatorio   | Tipo                             | Sezione                            | Note                                                                |
|:------------------------------------------------|:---------------|:---------------------------------|:-----------------------------------|:--------------------------------------------------------------------|
| Cognome                                         | *              | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Nome                                            | *              | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Comune di Nascita                               | *              | input text + popup comuni        | Dati difensore                     | Obbligatorio se Stato di Nascita = Italia (in inserimento manuale)  |
| Stato di Nascita                                | nan            | select                           | Dati difensore                     | Disabled di default, editabile in inserimento manuale (non reginde) |
| Luogo di Nascita Estero                         | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Giorno Data di nascita                          | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Mese Data di nascita                            | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Anno Data di nascita                            | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Foro                                            | *              | select                           | Dati difensore                     | Disabled di default, editabile in inserimento manuale (non reginde) |
| Indirizzo                                       | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Con Studio in                                   | nan            | input text + popup comuni        | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Telefono                                        | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Fax                                             | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| e-mail                                          | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| pec                                             | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Codice Fiscale                                  | nan            | input text                       | Dati difensore                     | Readonly di default, editabile in inserimento manuale (non reginde) |
| Stato Difensore                                 | nan            | select                           | Dati difensore                     | Disabled di default, editabile in inserimento manuale (non reginde) |
| Tipo Difensore                                  | *              | select                           | Dati difensore                     | Obbligatorio                                                        |
| Giorno Data di Nomina                           | nan            | input text                       | Nomina (Tipo Difensore = 02)       | Visibile per difensore di fiducia                                   |
| Mese Data di Nomina                             | nan            | input text                       | Nomina (Tipo Difensore = 02)       | Visibile per difensore di fiducia                                   |
| Anno Data di Nomina                             | nan            | input text                       | Nomina (Tipo Difensore = 02)       | Visibile per difensore di fiducia                                   |
| Giorno Data di Designazione                     | nan            | input text                       | Designazione (Tipo Difensore = 01) | Visibile per difensore d'ufficio                                    |
| Mese Data di Designazione                       | nan            | input text                       | Designazione (Tipo Difensore = 01) | Visibile per difensore d'ufficio                                    |
| Anno Data di Designazione                       | nan            | input text                       | Designazione (Tipo Difensore = 01) | Visibile per difensore d'ufficio                                    |
| Motivo della Designazione                       | *              | select                           | Designazione (Tipo Difensore = 01) | Obbligatorio se Tipo Difensore = 01                                 |
| Note                                            | nan            | textarea                         | Designazione (Tipo Difensore = 01) | Visibile solo se Motivo della Designazione = 0008                   |
| Autorità (notifica al Condannato)               | nan            | select                           | Autorità notifica al Condannato    | nan                                                                 |
| Sede (notifica al Condannato)                   | nan            | input text + popup comuni        | Autorità notifica al Condannato    | nan                                                                 |
| Indirizzo (notifica al Condannato)              | nan            | textarea                         | Autorità notifica al Condannato    | nan                                                                 |
| Istituto di Detenzione (notifica al Condannato) | nan            | popup lista istituti + hidden id | Autorità notifica al Condannato    | Valorizzato tramite popup                                           |
| Autorità (notifica al Difensore)                | nan            | select                           | Autorità notifica al Difensore     | nan                                                                 |
| Sede (notifica al Difensore)                    | nan            | input text + popup comuni        | Autorità notifica al Difensore     | nan                                                                 |
| nan                                             | nan            | nan                              | nan                                | nan                                                                 |
| Indice                                          | nan            | nan                              | nan                                | nan                                                                 |


## PosizioneGiuridica

| Campo                                        | Obbligatorio   | Tipo       | Sezione                                                | Note                                                                                        |
|:---------------------------------------------|:---------------|:-----------|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| Libero                                       | nan            | radio      | Scelta sezione                                         | Radio iniziale della pagina                                                                 |
| Espiazione Pena in Istituto di Detenzione    | nan            | radio      | Scelta sezione                                         | Radio iniziale della pagina                                                                 |
| Espiazione Pena in Altro Luogo               | nan            | radio      | Scelta sezione                                         | Radio iniziale della pagina                                                                 |
| Posizione Giuridica                          | *              | select     | Libero                                                 | Obbligatoria nella sezione Libero                                                           |
| Detenuto per altra causa                     | nan            | checkbox   | Libero                                                 | Mostra la sottosezione altra causa                                                          |
| Definitivo - in Istituto di Detenzione       | nan            | radio      | Libero / Altra causa                                   | Opzione radio visibile se è selezionato Detenuto per altra causa                            |
| Misure Cautelari - in Istituto di Detenzione | nan            | radio      | Libero / Altra causa                                   | Opzione radio visibile se è selezionato Detenuto per altra causa                            |
| Misure Cautelari - in Altro Luogo            | nan            | radio      | Libero / Altra causa                                   | Opzione radio visibile se è selezionato Detenuto per altra causa                            |
| Tipo Misura                                  | *              | select     | Libero / Altra causa / Definitivo in istituto          | Obbligatorio se è selezionato Detenuto per altra causa con radio DD                         |
| Istituto                                     | nan            | input text | Libero / Altra causa / Definitivo in istituto          | Readonly, valorizzato tramite popup                                                         |
| Anno SIEP                                    | nan            | input text | Libero / Altra causa / Definitivo in istituto          | nan                                                                                         |
| Numero SIEP                                  | nan            | input text | Libero / Altra causa / Definitivo in istituto          | nan                                                                                         |
| Autorità                                     | nan            | select     | Libero / Altra causa / Definitivo in istituto          | nan                                                                                         |
| Luogo                                        | nan            | input text | Libero / Altra causa / Definitivo in istituto          | Selezionabile tramite popup                                                                 |
| Giorno Data Scadenza Altra Pena              | nan            | input text | Libero / Altra causa / Definitivo in istituto          | Data opzionale ma validata                                                                  |
| Mese Data Scadenza Altra Pena                | nan            | input text | Libero / Altra causa / Definitivo in istituto          | Data opzionale ma validata                                                                  |
| Anno Data Scadenza Altra Pena                | nan            | input text | Libero / Altra causa / Definitivo in istituto          | Data opzionale ma validata                                                                  |
| Anno RG.N.R.                                 | nan            | input text | Libero / Altra causa / Misure cautelari in istituto    | nan                                                                                         |
| Numero RG.N.R.                               | nan            | input text | Libero / Altra causa / Misure cautelari in istituto    | nan                                                                                         |
| Tipo Ufficio PM                              | *              | select     | Libero / Altra causa / Misure cautelari in istituto    | Obbligatorio con radio MCD                                                                  |
| Sede                                         | *              | input text | Libero / Altra causa / Misure cautelari in istituto    | Obbligatoria con radio MCD, valorizzabile tramite popup                                     |
| Anno B.D.M.C.                                | nan            | input text | Libero / Altra causa / Misure cautelari in istituto    | nan                                                                                         |
| Numero B.D.M.C.                              | nan            | input text | Libero / Altra causa / Misure cautelari in istituto    | nan                                                                                         |
| Anno Reg. Gen.                               | nan            | input text | Libero / Altra causa / Misure cautelari in istituto    | nan                                                                                         |
| Numero Reg. Gen.                             | nan            | input text | Libero / Altra causa / Misure cautelari in istituto    | nan                                                                                         |
| Tipo Ufficio Reg. Gen.                       | nan            | select     | Libero / Altra causa / Misure cautelari in istituto    | nan                                                                                         |
| Autorità Emittente                           | *              | select     | Libero / Altra causa / Misure cautelari in istituto    | Obbligatoria con radio MCD                                                                  |
| Luogo Emittente                              | nan            | input text | Libero / Altra causa / Misure cautelari in istituto    | Selezionabile tramite popup                                                                 |
| Giorno Data emissione Ordinanza              | nan            | input text | Libero / Altra causa / Misure cautelari in istituto    | Data opzionale ma validata                                                                  |
| Mese Data emissione Ordinanza                | nan            | input text | Libero / Altra causa / Misure cautelari in istituto    | Data opzionale ma validata                                                                  |
| Anno Data emissione Ordinanza                | nan            | input text | Libero / Altra causa / Misure cautelari in istituto    | Data opzionale ma validata                                                                  |
| Tipo Misura                                  | *              | select     | Libero / Altra causa / Misure cautelari in istituto    | Obbligatorio con radio MCD                                                                  |
| Istituto                                     | nan            | input text | Libero / Altra causa / Misure cautelari in istituto    | Readonly, valorizzato tramite popup                                                         |
| Anno RG.N.R.                                 | nan            | input text | Libero / Altra causa / Misure cautelari in altro luogo | nan                                                                                         |
| Numero RG.N.R.                               | nan            | input text | Libero / Altra causa / Misure cautelari in altro luogo | nan                                                                                         |
| Tipo Ufficio PM                              | *              | select     | Libero / Altra causa / Misure cautelari in altro luogo | Obbligatorio con radio MCA                                                                  |
| Sede                                         | *              | input text | Libero / Altra causa / Misure cautelari in altro luogo | Obbligatoria con radio MCA, valorizzabile tramite popup                                     |
| Anno B.D.M.C.                                | nan            | input text | Libero / Altra causa / Misure cautelari in altro luogo | nan                                                                                         |
| Numero B.D.M.C.                              | nan            | input text | Libero / Altra causa / Misure cautelari in altro luogo | nan                                                                                         |
| Anno Reg. Gen.                               | nan            | input text | Libero / Altra causa / Misure cautelari in altro luogo | nan                                                                                         |
| Numero Reg. Gen.                             | nan            | input text | Libero / Altra causa / Misure cautelari in altro luogo | nan                                                                                         |
| Tipo Ufficio Reg. Gen.                       | nan            | select     | Libero / Altra causa / Misure cautelari in altro luogo | nan                                                                                         |
| Autorità Emittente                           | *              | select     | Libero / Altra causa / Misure cautelari in altro luogo | Obbligatoria con radio MCA                                                                  |
| Luogo Emittente                              | nan            | input text | Libero / Altra causa / Misure cautelari in altro luogo | Selezionabile tramite popup                                                                 |
| Giorno Data emissione Ordinanza              | nan            | input text | Libero / Altra causa / Misure cautelari in altro luogo | Data opzionale ma validata                                                                  |
| Mese Data emissione Ordinanza                | nan            | input text | Libero / Altra causa / Misure cautelari in altro luogo | Data opzionale ma validata                                                                  |
| Anno Data emissione Ordinanza                | nan            | input text | Libero / Altra causa / Misure cautelari in altro luogo | Data opzionale ma validata                                                                  |
| Tipo Misura                                  | *              | select     | Libero / Altra causa / Misure cautelari in altro luogo | Obbligatorio con radio MCA                                                                  |
| Luogo di Espiazione                          | nan            | input text | Libero / Altra causa / Misure cautelari in altro luogo | nan                                                                                         |
| Autorità Competente per territorio           | nan            | select     | Libero / Altra causa / Misure cautelari in altro luogo | nan                                                                                         |
| Sede                                         | nan            | input text | Libero / Altra causa / Misure cautelari in altro luogo | Selezionabile tramite popup                                                                 |
| Indirizzo                                    | nan            | textarea   | Libero / Altra causa / Misure cautelari in altro luogo | nan                                                                                         |
| Posizione Giuridica                          | *              | select     | Espiazione Pena in Istituto di Detenzione              | Obbligatoria nella sezione EI                                                               |
| Giorno Data di Decorrenza Pena               | *              | input text | Espiazione Pena in Istituto di Detenzione              | Obbligatoria e validata                                                                     |
| Mese Data di Decorrenza Pena                 | *              | input text | Espiazione Pena in Istituto di Detenzione              | Obbligatoria e validata                                                                     |
| Anno Data di Decorrenza Pena                 | *              | input text | Espiazione Pena in Istituto di Detenzione              | Obbligatoria e validata                                                                     |
| Istituto                                     | nan            | input text | Espiazione Pena in Istituto di Detenzione              | Readonly, valorizzato tramite popup                                                         |
| Posizione Giuridica                          | *              | select     | Espiazione Pena in Altro Luogo                         | Obbligatoria nella sezione EA                                                               |
| Giorno Data di Decorrenza Pena               | *              | input text | Espiazione Pena in Altro Luogo                         | Obbligatoria e validata                                                                     |
| Mese Data di Decorrenza Pena                 | *              | input text | Espiazione Pena in Altro Luogo                         | Obbligatoria e validata                                                                     |
| Anno Data di Decorrenza Pena                 | *              | input text | Espiazione Pena in Altro Luogo                         | Obbligatoria e validata                                                                     |
| Luogo di Espiazione                          | nan            | input text | Espiazione Pena in Altro Luogo                         | nan                                                                                         |
| Autorità Competente per territorio           | nan            | select     | Espiazione Pena in Altro Luogo                         | nan                                                                                         |
| Sede                                         | nan            | input text | Espiazione Pena in Altro Luogo                         | Selezionabile tramite popup                                                                 |
| Indirizzo                                    | nan            | textarea   | Espiazione Pena in Altro Luogo                         | nan                                                                                         |
| Posizione Giuridica                          | *              | select     | Legacy / Form old                                      | Obbligatoria se non è selezionato Detenuto per altra causa                                  |
| Giorno Data di Decorrenza                    | nan            | input text | Legacy / Form old                                      | Obbligatoria solo per alcune posizioni giuridiche (01/02), altrimenti opzionale ma validata |
| Mese Data di Decorrenza                      | nan            | input text | Legacy / Form old                                      | Obbligatoria solo per alcune posizioni giuridiche (01/02), altrimenti opzionale ma validata |
| Anno Data di Decorrenza                      | nan            | input text | Legacy / Form old                                      | Obbligatoria solo per alcune posizioni giuridiche (01/02), altrimenti opzionale ma validata |
| Istituto                                     | nan            | input text | Legacy / Form old                                      | Readonly, valorizzato tramite popup                                                         |
| Altro Luogo Detenzione                       | nan            | input text | Legacy / Form old                                      | nan                                                                                         |
| Luogo Prova Affidamento                      | nan            | input text | Legacy / Form old                                      | nan                                                                                         |
| Luogo Lavoro Semilibertà                     | nan            | input text | Legacy / Form old                                      | nan                                                                                         |
| Detenuto per altra causa                     | nan            | checkbox   | Legacy / Form old                                      | nan                                                                                         |
| Tipo Misura                                  | *              | select     | Legacy / Form old / Detenuto per altra causa           | Obbligatorio se è selezionato Detenuto per altra causa                                      |
| Giorno Data di Decorrenza                    | nan            | input text | Legacy / Form old / Detenuto per altra causa           | Data opzionale ma validata                                                                  |
| Mese Data di Decorrenza                      | nan            | input text | Legacy / Form old / Detenuto per altra causa           | Data opzionale ma validata                                                                  |
| Anno Data di Decorrenza                      | nan            | input text | Legacy / Form old / Detenuto per altra causa           | Data opzionale ma validata                                                                  |
| Giorno Data di Scadenza                      | nan            | input text | Legacy / Form old / Detenuto per altra causa           | Data opzionale ma validata                                                                  |
| Mese Data di Scadenza                        | nan            | input text | Legacy / Form old / Detenuto per altra causa           | Data opzionale ma validata                                                                  |
| Anno Data di Scadenza                        | nan            | input text | Legacy / Form old / Detenuto per altra causa           | Data opzionale ma validata                                                                  |
| Istituto                                     | nan            | input text | Legacy / Form old / Detenuto per altra causa           | Readonly, valorizzato tramite popup                                                         |
| Altro Luogo Detenzione                       | nan            | input text | Legacy / Form old / Detenuto per altra causa           | nan                                                                                         |
| Anno Tit. Esec.                              | nan            | input text | Legacy / Form old / Detenuto per altra causa           | nan                                                                                         |
| Numero Tit. Esec.                            | nan            | input text | Legacy / Form old / Detenuto per altra causa           | nan                                                                                         |
| Giorno Data Tit. Esec.                       | nan            | input text | Legacy / Form old / Detenuto per altra causa           | Data opzionale ma validata                                                                  |
| Mese Data Tit. Esec.                         | nan            | input text | Legacy / Form old / Detenuto per altra causa           | Data opzionale ma validata                                                                  |
| Anno Data Tit. Esec.                         | nan            | input text | Legacy / Form old / Detenuto per altra causa           | Data opzionale ma validata                                                                  |
| Autorità                                     | nan            | select     | Legacy / Form old / Detenuto per altra causa           | nan                                                                                         |
| Luogo                                        | nan            | input text | Legacy / Form old / Detenuto per altra causa           | Selezionabile tramite popup                                                                 |
| nan                                          | nan            | nan        | nan                                                    | nan                                                                                         |
| Indice                                       | nan            | nan        | nan                                                    | nan                                                                                         |


## PenaAccessoria

| Campo                                     | Obbligatorio   | Tipo       | Sezione                                                        | Note                                                                     |
|:------------------------------------------|:---------------|:-----------|:---------------------------------------------------------------|:-------------------------------------------------------------------------|
| Tipo di Pena Accessoria                   | *              | select     | Generale                                                       | Obbligatorio sempre (validazione req)                                    |
| Descrizione Altre P.A.                    | nan            | input text | Generale                                                       | Visibile/editabile quando Tipo di Pena Accessoria = "Altre" (codice 999) |
| Tipo Durata                               | nan            | select     | Generale                                                       | nan                                                                      |
| Anni Durata                               | nan            | input text | Durata                                                         | nan                                                                      |
| Mesi Durata                               | nan            | input text | Durata                                                         | nan                                                                      |
| Giorni Durata                             | nan            | input text | Durata                                                         | nan                                                                      |
| Giorno Data Fine Validità                 | nan            | input text | Data Fine Validità                                             | nan                                                                      |
| Mese Data Fine Validità                   | nan            | input text | Data Fine Validità                                             | nan                                                                      |
| Anno Data Fine Validità                   | nan            | input text | Data Fine Validità                                             | nan                                                                      |
| Giorno Data Ordinanza GE                  | nan            | input text | Estremi Ordinanza Applicazione del GE                          | nan                                                                      |
| Mese Data Ordinanza GE                    | nan            | input text | Estremi Ordinanza Applicazione del GE                          | nan                                                                      |
| Anno Data Ordinanza GE                    | nan            | input text | Estremi Ordinanza Applicazione del GE                          | nan                                                                      |
| Anno Ordinanza GE                         | nan            | input text | Estremi Ordinanza Applicazione del GE                          | nan                                                                      |
| Numero Ordinanza GE                       | nan            | input text | Estremi Ordinanza Applicazione del GE                          | nan                                                                      |
| Autorità Ordinanza GE                     | nan            | select     | Estremi Ordinanza Applicazione del GE                          | nan                                                                      |
| Luogo Ordinanza GE                        | nan            | input text | Estremi Ordinanza Applicazione del GE                          | Valorizzabile anche da lookup comuni                                     |
| Tenore                                    | nan            | select     | Estremi Ordinanza Condono/Revoca/Sostituzione/Depenalizzazione | nan                                                                      |
| Giorno Data Ordinanza PA                  | nan            | input text | Estremi Ordinanza Condono/Revoca/Sostituzione/Depenalizzazione | nan                                                                      |
| Mese Data Ordinanza PA                    | nan            | input text | Estremi Ordinanza Condono/Revoca/Sostituzione/Depenalizzazione | nan                                                                      |
| Anno Data Ordinanza PA                    | nan            | input text | Estremi Ordinanza Condono/Revoca/Sostituzione/Depenalizzazione | nan                                                                      |
| Anno Ordinanza PA                         | nan            | input text | Estremi Ordinanza Condono/Revoca/Sostituzione/Depenalizzazione | nan                                                                      |
| Numero Ordinanza PA                       | nan            | input text | Estremi Ordinanza Condono/Revoca/Sostituzione/Depenalizzazione | nan                                                                      |
| Autorità Emittente PA                     | nan            | select     | Estremi Ordinanza Condono/Revoca/Sostituzione/Depenalizzazione | nan                                                                      |
| Luogo Ordinanza PA                        | nan            | input text | Estremi Ordinanza Condono/Revoca/Sostituzione/Depenalizzazione | Valorizzabile anche da lookup comuni                                     |
| Fonte                                     | nan            | select     | Estremi Condono/Depenalizzazione/Amnistia                      | nan                                                                      |
| Anno Fonte                                | nan            | input text | Estremi Condono/Depenalizzazione/Amnistia                      | nan                                                                      |
| Numero Fonte                              | nan            | input text | Estremi Condono/Depenalizzazione/Amnistia                      | nan                                                                      |
| Articolo Fonte                            | nan            | input text | Estremi Condono/Depenalizzazione/Amnistia                      | nan                                                                      |
| Art.qualificante                          | nan            | select     | Estremi Condono/Depenalizzazione/Amnistia                      | nan                                                                      |
| Comma                                     | nan            | input text | Estremi Condono/Depenalizzazione/Amnistia                      | nan                                                                      |
| Lettera                                   | nan            | input text | Estremi Condono/Depenalizzazione/Amnistia                      | nan                                                                      |
| Numero (articolo)                         | nan            | input text | Estremi Condono/Depenalizzazione/Amnistia                      | nan                                                                      |
| Tipo di Pena Accessoria (in sostituzione) | *              | select     | Estremi Pena Accessoria in Sostituzione                        | Obbligatorio se Tenore = "S" o "T"                                       |
| Revoca Condono                            | nan            | checkbox   | Revoca Condono                                                 | nan                                                                      |
| Giorno Data Sentenza Revoca               | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Mese Data Sentenza Revoca                 | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Anno Data Sentenza Revoca                 | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Anno Sentenza Revoca                      | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Numero Sentenza Revoca                    | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Autorità Sentenza Revoca                  | nan            | select     | Revoca Condono                                                 | nan                                                                      |
| Luogo Sentenza Revoca                     | nan            | input text | Revoca Condono                                                 | Valorizzabile anche da lookup comuni                                     |
| Anno Re.Ge. PM Revoca                     | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Numero Re.Ge. PM Revoca                   | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Anno Re.Ge. GIP Revoca                    | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Numero Re.Ge. GIP Revoca                  | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Anno Re.Ge. DIB Revoca                    | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Numero Re.Ge. DIB Revoca                  | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Anno Re.Ge. CAS Revoca                    | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Numero Re.Ge. CAS Revoca                  | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Anno Re.Ge. CAP Revoca                    | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Numero Re.Ge. CAP Revoca                  | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Anno Re.Ge. CASAP Revoca                  | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Numero Re.Ge. CASAP Revoca                | nan            | input text | Revoca Condono                                                 | nan                                                                      |
| Falsità di documenti                      | nan            | checkbox   | Revoca Condono                                                 | nan                                                                      |
| Note                                      | nan            | textarea   | Revoca Condono                                                 | nan                                                                      |
| nan                                       | nan            | nan        | nan                                                            | nan                                                                      |
| Indice                                    | nan            | nan        | nan                                                            | nan                                                                      |


## MisuraSicurezza

| Campo                       | Obbligatorio   | Tipo       | Sezione             | Note                                                                            |
|:----------------------------|:---------------|:-----------|:--------------------|:--------------------------------------------------------------------------------|
| Natura Misura               | nan            | select     | Misura di Sicurezza | Combo filtro; al cambio aggiorna la combo Tipo Misura                           |
| Tipo Misura                 | *              | select     | Misura di Sicurezza | Obbligatorio; caricato dinamicamente in base a Natura Misura                    |
| Durata Misura - Anni        | nan            | input text | Misura di Sicurezza | Numerico, max 2 cifre                                                           |
| Durata Misura - Mesi        | nan            | input text | Misura di Sicurezza | Numerico, max 2 cifre                                                           |
| Durata Misura - Giorni      | nan            | input text | Misura di Sicurezza | Numerico, max 2 cifre                                                           |
| Data Fine Validità - Giorno | nan            | input text | Misura di Sicurezza | Formato gg; se valorizzato richiede validazione data completa e conferma utente |
| Data Fine Validità - Mese   | nan            | input text | Misura di Sicurezza | Formato mm; parte della data fine validità                                      |
| Data Fine Validità - Anno   | nan            | input text | Misura di Sicurezza | Formato aaaa; parte della data fine validità                                    |
| nan                         | nan            | nan        | nan                 | nan                                                                             |
| Indice                      | nan            | nan        | nan                 | nan                                                                             |


## Circostanza

| Campo                                 | Obbligatorio   | Tipo       | Sezione              | Note (Circostanze = Aggravanti soggettive / Attenuanti)                            |
|:--------------------------------------|:---------------|:-----------|:---------------------|:-----------------------------------------------------------------------------------|
| Fonte (riga 1-5)                      | *              | select     | Definizione articolo | Obbligatorio con Articolo: se uno dei due è valorizzato deve esserci anche l'altro |
| Anno Fonte (riga 1-5)                 | nan            | input text | Definizione articolo | Numerico (4 cifre), compilabile solo se presente la coppia Fonte/Articolo          |
| Numero Fonte (riga 1-5)               | nan            | input text | Definizione articolo | Alfanumerico, compilabile solo se presente la coppia Fonte/Articolo                |
| Articolo (riga 1-5)                   | *              | input text | Definizione articolo | Obbligatorio con Fonte: se uno dei due è valorizzato deve esserci anche l'altro    |
| Articolo qualificante (riga 1-5)      | nan            | select     | Definizione articolo | Compilabile solo se presente la coppia Fonte/Articolo                              |
| Comma (riga 1-5)                      | *              | input text | Definizione articolo | Obbligatorio se Comma qualificante è valorizzato                                   |
| Comma qualificante (riga 1-5)         | nan            | select     | Definizione articolo | Se valorizzato richiede Comma                                                      |
| Lettera (riga 1-5)                    | nan            | input text | Definizione articolo | Compilabile solo se presente la coppia Fonte/Articolo                              |
| Numero (riga 1-5)                     | nan            | input text | Definizione articolo | Compilabile solo se presente la coppia Fonte/Articolo                              |
| 99 CP C1                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 99 CP C2 N1                           | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 99 CP C2 N2                           | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 99 CP C2 N3                           | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 99 CP C3                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 99 CP C4                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 102 CP                                | nan            | checkbox   | Circostanze cablate  | Checkbox                                                                           |
| 103 CP                                | nan            | checkbox   | Circostanze cablate  | Checkbox                                                                           |
| 104 CP                                | nan            | checkbox   | Circostanze cablate  | Checkbox                                                                           |
| 105 CP                                | nan            | checkbox   | Circostanze cablate  | Checkbox                                                                           |
| 108 CP                                | nan            | checkbox   | Circostanze cablate  | Checkbox                                                                           |
| 62 CP N1                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 62 CP N2                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 62 CP N3                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 62 CP N4                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 62 CP N5                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 62 CP N6                              | nan            | checkbox   | Circostanze cablate  | Checkbox multipla                                                                  |
| 62 BIS CP                             | nan            | checkbox   | Circostanze cablate  | Checkbox                                                                           |
| Sentenza di applicazione pena         | nan            | checkbox   | Campi comuni         | In modifica può risultare non editabile (renderizzato come hidden)                 |
| Bilanciamento circostanze             | nan            | select     | Campi comuni         | In modifica può risultare non editabile (renderizzato come hidden)                 |
| Annotazioni Bilanciamento circostanze | nan            | textarea   | Campi comuni         | nan                                                                                |
| Giudizio abbreviato                   | nan            | checkbox   | Campi comuni         | In modifica può risultare non editabile (renderizzato come hidden)                 |
| nan                                   | nan            | nan        | nan                  | nan                                                                                |
| Indice                                | nan            | nan        | nan                  | nan                                                                                |


## NotiziaReato

| Campo                        | Obbligatorio   | Tipo       | Sezione            | Note                                                       |
|:-----------------------------|:---------------|:-----------|:-------------------|:-----------------------------------------------------------|
| Giorno Data Pervenimento     | nan            | input text | Dati Notizia Reato | Campo data (dd)                                            |
| Mese Data Pervenimento       | nan            | input text | Dati Notizia Reato | Campo data (MM)                                            |
| Anno Data Pervenimento       | nan            | input text | Dati Notizia Reato | Campo data (yyyy)                                          |
| Giorno Data Acquisizione     | nan            | input text | Dati Notizia Reato | Campo data (dd)                                            |
| Mese Data Acquisizione       | nan            | input text | Dati Notizia Reato | Campo data (MM)                                            |
| Anno Data Acquisizione       | nan            | input text | Dati Notizia Reato | Campo data (yyyy)                                          |
| Acquisizione Diretta         | nan            | select     | Dati Notizia Reato | Selezione da combo                                         |
| Giorno Data Fatto            | *              | input text | Dati Notizia Reato | Obbligatorio (campo mostrato con asterisco in pagina)      |
| Mese Data Fatto              | *              | input text | Dati Notizia Reato | Parte della Data Fatto obbligatoria                        |
| Anno Data Fatto              | *              | input text | Dati Notizia Reato | Parte della Data Fatto obbligatoria                        |
| Descrizione Fonte            | nan            | input text | Dati Notizia Reato | nan                                                        |
| Comune Fonte                 | *              | input text | Dati Notizia Reato | Obbligatorio                                               |
| Numero Registro Autorità     | nan            | input text | Dati Notizia Reato | nan                                                        |
| Luogo Provenienza            | nan            | input text | Dati Notizia Reato | nan                                                        |
| Numero Ricevuta              | nan            | input text | Dati Notizia Reato | nan                                                        |
| Giorno Data Arresto          | nan            | input text | Dati Notizia Reato | Campo data (dd)                                            |
| Mese Data Arresto            | nan            | input text | Dati Notizia Reato | Campo data (MM)                                            |
| Anno Data Arresto            | nan            | input text | Dati Notizia Reato | Campo data (yyyy)                                          |
| Giorno Data Fermo            | nan            | input text | Dati Notizia Reato | Campo data (dd)                                            |
| Mese Data Fermo              | nan            | input text | Dati Notizia Reato | Campo data (MM)                                            |
| Anno Data Fermo              | nan            | input text | Dati Notizia Reato | Campo data (yyyy)                                          |
| Fotosegnalato                | nan            | select     | Fotosegnalazione   | Se S rende obbligatori i campi del blocco Fotosegnalazione |
| Giorno Data Fotosegnalazione | *              | input text | Fotosegnalazione   | Obbligatorio se Fotosegnalato=S                            |
| Mese Data Fotosegnalazione   | *              | input text | Fotosegnalazione   | Obbligatorio se Fotosegnalato=S                            |
| Anno Data Fotosegnalazione   | *              | input text | Fotosegnalazione   | Obbligatorio se Fotosegnalato=S                            |
| Autorità Fotosegnalazione    | *              | select     | Fotosegnalazione   | Obbligatorio se Fotosegnalato=S                            |
| Comune Fotosegnalazione      | *              | input text | Fotosegnalazione   | Obbligatorio se Fotosegnalato=S                            |
| nan                          | nan            | nan        | nan                | nan                                                        |
| Indice                       | nan            | nan        | nan                | nan                                                        |


## Beneficio

| Campo                                             | Obbligatorio   | Tipo       | Sezione                    | Note                                                                              |   Unnamed: 5 | Pena Sospesa - Non Menzione (Ex Artt 163 165 c.p.)   |
|:--------------------------------------------------|:---------------|:-----------|:---------------------------|:----------------------------------------------------------------------------------|-------------:|:-----------------------------------------------------|
| Tipo Sospensione                                  | *              | select     | Dati beneficio             | Obbligatorio in alternativa a "Non Menzione" (almeno uno dei due valorizzato)     |          nan | nan                                                  |
| Non Menzione                                      | *              | checkbox   | Dati beneficio             | Obbligatorio in alternativa a "Tipo Sospensione" (almeno uno dei due valorizzato) |          nan | nan                                                  |
| Anni Durata Sospensione                           | nan            | input text | Durata sospensione         | nan                                                                               |          nan | nan                                                  |
| Obblighi del condannato ex art 165 c.p.           | nan            | select     | Obblighi subordinati       | Visibile/editabile se Tipo Sospensione = valore 03                                |          nan | nan                                                  |
| Tipologia Obbligo                                 | nan            | textarea   | Obblighi subordinati       | Visibile/editabile se Tipo Sospensione = valore 03                                |          nan | nan                                                  |
| Anni Termine Adempimento Obbligo                  | nan            | input text | Obblighi subordinati       | Visibile/editabile se Tipo Sospensione = valore 03                                |          nan | nan                                                  |
| Mesi Termine Adempimento Obbligo                  | nan            | input text | Obblighi subordinati       | Visibile/editabile se Tipo Sospensione = valore 03                                |          nan | nan                                                  |
| Giorni Termine Adempimento Obbligo                | nan            | input text | Obblighi subordinati       | Visibile/editabile se Tipo Sospensione = valore 03                                |          nan | nan                                                  |
| Mesi Durata Prestazione Attività Non Retribuita   | nan            | input text | Prestazione non retribuita | Visibile/editabile se Obblighi subordinati = valore 08                            |          nan | nan                                                  |
| Giorni Durata Prestazione Attività Non Retribuita | nan            | input text | Prestazione non retribuita | Visibile/editabile se Obblighi subordinati = valore 08                            |          nan | nan                                                  |
| Ore Settimanali                                   | nan            | input text | Prestazione non retribuita | Visibile/editabile se Obblighi subordinati = valore 08                            |          nan | nan                                                  |
| Frequenza Settimanale - Non Determinata           | nan            | radio      | Prestazione non retribuita | Visibile/editabile se Obblighi subordinati = valore 08                            |          nan | nan                                                  |
| Frequenza Settimanale - Determinata               | nan            | radio      | Prestazione non retribuita | Visibile/editabile se Obblighi subordinati = valore 08                            |          nan | nan                                                  |
| Lunedì                                            | nan            | checkbox   | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Dalle ore Lunedì                                  | nan            | input text | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Alle ore Lunedì                                   | nan            | input text | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Martedì                                           | nan            | checkbox   | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Dalle ore Martedì                                 | nan            | input text | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Alle ore Martedì                                  | nan            | input text | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Mercoledì                                         | nan            | checkbox   | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Dalle ore Mercoledì                               | nan            | input text | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Alle ore Mercoledì                                | nan            | input text | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Giovedì                                           | nan            | checkbox   | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Dalle ore Giovedì                                 | nan            | input text | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Alle ore Giovedì                                  | nan            | input text | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Venerdì                                           | nan            | checkbox   | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Dalle ore Venerdì                                 | nan            | input text | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Alle ore Venerdì                                  | nan            | input text | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Sabato                                            | nan            | checkbox   | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Dalle ore Sabato                                  | nan            | input text | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Alle ore Sabato                                   | nan            | input text | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Domenica                                          | nan            | checkbox   | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Dalle ore Domenica                                | nan            | input text | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Alle ore Domenica                                 | nan            | input text | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| Ente Incaricato dei controlli                     | nan            | textarea   | Tipologia orario           | Visibile/editabile se Frequenza Settimanale = Determinata                         |          nan | nan                                                  |
| nan                                               | nan            | nan        | nan                        | nan                                                                               |          nan | nan                                                  |
| Campo                                             | Obbligatorio   | Tipo       | Sezione                    | Note                                                                              |          nan | Indulto                                              |
| Tipo Beneficio                                    | nan            | select     | Dati beneficio             | Combo valorizzata da tipoBeneficio                                                |          nan | nan                                                  |
| Provvedimento di Concessione                      | nan            | select     | Dati beneficio             | Combo valorizzata da listaDPR                                                     |          nan | nan                                                  |
| Applicazione del beneficio                        | nan            | select     | Dati beneficio             | Combo sottotipo con onchange CaricaPena()                                         |          nan | nan                                                  |
| Anni Reclusione                                   | nan            | input text | Reclusione                 | Campo ARec con validazione numerica                                               |          nan | nan                                                  |
| Mesi Reclusione                                   | nan            | input text | Reclusione                 | Campo MRec con validazione numerica                                               |          nan | nan                                                  |
| Giorni Reclusione                                 | nan            | input text | Reclusione                 | Campo GRec con validazione numerica                                               |          nan | nan                                                  |
| Multa (parte intera)                              | nan            | input text | Reclusione                 | Campo Multa con validazione numerica                                              |          nan | nan                                                  |
| Multa (parte decimale)                            | nan            | input text | Reclusione                 | Campo Mul_dec con validazione numerica                                            |          nan | nan                                                  |
| Anni Arresto                                      | nan            | input text | Arresto                    | Campo AArr con validazione numerica                                               |          nan | nan                                                  |
| Mesi Arresto                                      | nan            | input text | Arresto                    | Campo MArr con validazione numerica                                               |          nan | nan                                                  |
| Giorni Arresto                                    | nan            | input text | Arresto                    | Campo GArr con validazione numerica                                               |          nan | nan                                                  |
| Ammenda (parte intera)                            | nan            | input text | Arresto                    | Campo Ammenda con validazione numerica                                            |          nan | nan                                                  |
| Ammenda (parte decimale)                          | nan            | input text | Arresto                    | Campo Amm_dec con validazione numerica                                            |          nan | nan                                                  |
| Note                                              | nan            | textarea   | Note                       | Campo CAMPO_NOTE                                                                  |          nan | nan                                                  |
| Tipo Pena Accessoria                              | nan            | checkbox   | Pene accessorie            | Checkbox multiple CAMPO_ID_PENA_ACCESSORIA visibili in base al sottotipo          |          nan | nan                                                  |
| nan                                               | nan            | nan        | nan                        | nan                                                                               |          nan | nan                                                  |
| Indice                                            | nan            | nan        | nan                        | nan                                                                               |          nan | nan                                                  |


## RevocaBeneficio

| Campo                        | Obbligatorio   | Tipo       | Sezione                               | Note                                                                               |   Unnamed: 5 | Revoca della Sospensione Condizionale della Pena/Non Menzione concessa in altro Provvedimento   |
|:-----------------------------|:---------------|:-----------|:--------------------------------------|:-----------------------------------------------------------------------------------|-------------:|:------------------------------------------------------------------------------------------------|
| Sospensione Condizionale     | nan            | checkbox   | Tipo Beneficio Revocato               | Almeno uno tra Sospensione Condizionale e Non Menzione deve essere selezionato (*) |          nan | nan                                                                                             |
| Non Menzione                 | nan            | checkbox   | Tipo Beneficio Revocato               | Almeno uno tra Sospensione Condizionale e Non Menzione deve essere selezionato (*) |          nan | nan                                                                                             |
| Tipo Provvedimento *         | Sì             | select     | Estremi del provvedimento             | nan                                                                                |          nan | nan                                                                                             |
| Data Provvedimento (GG) *    | Sì             | input text | Estremi del provvedimento             | Formato GG-MM-AAAA; data validata                                                  |          nan | nan                                                                                             |
| Data Provvedimento (MM) *    | Sì             | input text | Estremi del provvedimento             | nan                                                                                |          nan | nan                                                                                             |
| Data Provvedimento (AAAA) *  | Sì             | input text | Estremi del provvedimento             | nan                                                                                |          nan | nan                                                                                             |
| Definitivo in Data (GG) *    | Sì             | input text | Estremi del provvedimento             | Formato GG-MM-AAAA; data validata                                                  |          nan | nan                                                                                             |
| Definitivo in Data (MM) *    | Sì             | input text | Estremi del provvedimento             | nan                                                                                |          nan | nan                                                                                             |
| Definitivo in Data (AAAA) *  | Sì             | input text | Estremi del provvedimento             | nan                                                                                |          nan | nan                                                                                             |
| Pronunciata da *             | Sì             | select     | Estremi del provvedimento             | nan                                                                                |          nan | nan                                                                                             |
| Luogo *                      | Sì             | input text | Estremi del provvedimento             | Selezionabile tramite ricerca comuni                                               |          nan | nan                                                                                             |
| Sezione                      | nan            | input text | Estremi del provvedimento             | nan                                                                                |          nan | nan                                                                                             |
| nan                          | nan            | nan        | nan                                   | nan                                                                                |          nan | nan                                                                                             |
| Campo                        | Obbligatorio   | Tipo       | Sezione                               | Note                                                                               |          nan | Revoca Indulto Concesso in altro Provvedimento                                                  |
| Provvedimento di Concessione | *              | select     | Tipo Beneficio Revocato               | Campo CAMPO_COD_DPR                                                                |          nan | nan                                                                                             |
| Tipo Provvedimento           | *              | select     | Estremi del Provvedimento da Revocare | Campo CAMPO_COD_TIPO_PROVVEDIMENTO                                                 |          nan | nan                                                                                             |
| Giorno Data Provvedimento    | *              | input text | Estremi del Provvedimento da Revocare | Parte della data provvedimento                                                     |          nan | nan                                                                                             |
| Mese Data Provvedimento      | *              | input text | Estremi del Provvedimento da Revocare | Parte della data provvedimento                                                     |          nan | nan                                                                                             |
| Anno Data Provvedimento      | *              | input text | Estremi del Provvedimento da Revocare | Parte della data provvedimento                                                     |          nan | nan                                                                                             |
| Giorno Definitivo in Data    | nan            | input text | Estremi del Provvedimento da Revocare | Obbligatorio se Tipo Provvedimento != 03                                           |          nan | nan                                                                                             |
| Mese Definitivo in Data      | nan            | input text | Estremi del Provvedimento da Revocare | Obbligatorio se Tipo Provvedimento != 03                                           |          nan | nan                                                                                             |
| Anno Definitivo in Data      | nan            | input text | Estremi del Provvedimento da Revocare | Obbligatorio se Tipo Provvedimento != 03                                           |          nan | nan                                                                                             |
| Emessa da                    | *              | select     | Estremi del Provvedimento da Revocare | Campo CAMPO_COD_TIPO_AUTORITA_EMITTENTE                                            |          nan | nan                                                                                             |
| Luogo                        | *              | input text | Estremi del Provvedimento da Revocare | Campo CAMPO_COD_LUOGO_EMITTENTE                                                    |          nan | nan                                                                                             |
| Sezione                      | nan            | input text | Estremi del Provvedimento da Revocare | Campo CAMPO_NUM_SEZIONE_AUTORITA_EMITTENTE                                         |          nan | nan                                                                                             |
| Anni Reclusione              | nan            | input text | Eventuale Quantum                     | Campo CAMPO_NUM_ANNI_RECLUSIONE                                                    |          nan | nan                                                                                             |
| Mesi Reclusione              | nan            | input text | Eventuale Quantum                     | Campo CAMPO_NUM_MESI_RECLUSIONE                                                    |          nan | nan                                                                                             |
| Giorni Reclusione            | nan            | input text | Eventuale Quantum                     | Campo CAMPO_NUM_GIORNI_RECLUSIONE                                                  |          nan | nan                                                                                             |
| Multa Intero                 | nan            | input text | Eventuale Quantum                     | Può essere valorizzato da solo o con parte decimale                                |          nan | nan                                                                                             |
| Multa Decimale               | nan            | input text | Eventuale Quantum                     | Opzionale, ma se valorizzato richiede la parte intera                              |          nan | nan                                                                                             |
| Anni Arresto                 | nan            | input text | Eventuale Quantum                     | Campo CAMPO_NUM_ANNI_ARRESTO                                                       |          nan | nan                                                                                             |
| Mesi Arresto                 | nan            | input text | Eventuale Quantum                     | Campo CAMPO_NUM_MESI_ARRESTO                                                       |          nan | nan                                                                                             |
| Giorni Arresto               | nan            | input text | Eventuale Quantum                     | Campo CAMPO_NUM_GIORNI_ARRESTO                                                     |          nan | nan                                                                                             |
| Ammenda Intero               | nan            | input text | Eventuale Quantum                     | Può essere valorizzato da solo o con parte decimale                                |          nan | nan                                                                                             |
| Ammenda Decimale             | nan            | input text | Eventuale Quantum                     | Opzionale, ma se valorizzato richiede la parte intera                              |          nan | nan                                                                                             |
| Note                         | nan            | textarea   | Eventuale Quantum                     | Campo CAMPO_NOTE                                                                   |          nan | nan                                                                                             |
| nan                          | nan            | nan        | nan                                   | nan                                                                                |          nan | nan                                                                                             |
| Indice                       | nan            | nan        | nan                                   | nan                                                                                |          nan | nan                                                                                             |


## MisuraCautelare

| Campo                                                  | Obbligatorio   | Tipo                            | Sezione                   | Note                                                  |   Unnamed: 5 | Cessata al momento del passaggio in giudicato computabili     |
|:-------------------------------------------------------|:---------------|:--------------------------------|:--------------------------|:------------------------------------------------------|-------------:|:--------------------------------------------------------------|
| Anno/Numero RG.N.R. - Anno                             | nan            | input text                      | Dati procedimento         | nan                                                   |          nan | nan                                                           |
| Anno/Numero RG.N.R. - Numero                           | nan            | input text                      | Dati procedimento         | nan                                                   |          nan | nan                                                           |
| Tipo Ufficio PM                                        | *              | select                          | Dati procedimento         | Controllo obbligatorietà in VerifyAltreBDI()          |          nan | nan                                                           |
| Sede PM                                                | *              | input text                      | Dati procedimento         | Compilabile con popup ListaUfficiComuni               |          nan | nan                                                           |
| Anno/Numero B.D.M.C. - Anno                            | nan            | input text                      | Dati procedimento         | nan                                                   |          nan | nan                                                           |
| Anno/Numero B.D.M.C. - Numero                          | nan            | input text                      | Dati procedimento         | nan                                                   |          nan | nan                                                           |
| Anno/Numero Reg. Gen. - Anno                           | nan            | input text                      | Dati procedimento         | nan                                                   |          nan | nan                                                           |
| Anno/Numero Reg. Gen. - Numero                         | nan            | input text                      | Dati procedimento         | nan                                                   |          nan | nan                                                           |
| Tipo Ufficio Reg. Gen.                                 | nan            | select                          | Dati procedimento         | nan                                                   |          nan | nan                                                           |
| Autorità Emittente                                     | *              | select                          | Provvedimento             | Controllo obbligatorietà in VerifyAltreBDI()          |          nan | nan                                                           |
| Luogo Autorità Emittente                               | nan            | input text                      | Provvedimento             | Compilabile con popup ListaUfficiPerTipo              |          nan | nan                                                           |
| Data emissione ordinanza - Giorno                      | nan            | input text                      | Provvedimento             | nan                                                   |          nan | nan                                                           |
| Data emissione ordinanza - Mese                        | nan            | input text                      | Provvedimento             | nan                                                   |          nan | nan                                                           |
| Data emissione ordinanza - Anno                        | nan            | input text                      | Provvedimento             | nan                                                   |          nan | nan                                                           |
| Espiazione pena (istituto di detenzione / altro luogo) | nan            | radio                           | Tipologia espiazione      | Selezione modalità                                    |          nan | nan                                                           |
| Misura cautelare non detentiva                         | *              | select                          | Tipologia espiazione      | Obbligatoria in alternativa alla misura detentiva     |          nan | nan                                                           |
| Misura cautelare detentiva                             | *              | select                          | Tipologia espiazione      | Obbligatoria in alternativa alla misura non detentiva |          nan | nan                                                           |
| Data misura "Da" - Giorno                              | *              | input text                      | Periodo misura            | Controllo obbligatorietà in VerifyAltreBDI()          |          nan | nan                                                           |
| Data misura "Da" - Mese                                | *              | input text                      | Periodo misura            | Controllo obbligatorietà in VerifyAltreBDI()          |          nan | nan                                                           |
| Data misura "Da" - Anno                                | *              | input text                      | Periodo misura            | Controllo obbligatorietà in VerifyAltreBDI()          |          nan | nan                                                           |
| Data misura "A" - Giorno                               | *              | input text                      | Periodo misura            | Controllo obbligatorietà in VerifyAltreBDI()          |          nan | nan                                                           |
| Data misura "A" - Mese                                 | *              | input text                      | Periodo misura            | Controllo obbligatorietà in VerifyAltreBDI()          |          nan | nan                                                           |
| Data misura "A" - Anno                                 | *              | input text                      | Periodo misura            | Controllo obbligatorietà in VerifyAltreBDI()          |          nan | nan                                                           |
| Istituto di Detenzione                                 | nan            | input text (readonly+popup)     | Espiazione in istituto    | Valorizzabile tramite popup ListaIstitutoDetenzione   |          nan | nan                                                           |
| Luogo di espiazione                                    | nan            | textarea                        | Espiazione in altro luogo | nan                                                   |          nan | nan                                                           |
| Autorità competente per territorio                     | nan            | select                          | Espiazione in altro luogo | nan                                                   |          nan | nan                                                           |
| Sede autorità competente                               | nan            | input text                      | Espiazione in altro luogo | Compilabile con popup ListaComuni                     |          nan | nan                                                           |
| Indirizzo autorità competente                          | nan            | textarea                        | Espiazione in altro luogo | nan                                                   |          nan | nan                                                           |
| nan                                                    | nan            | nan                             | nan                       | nan                                                   |          nan | nan                                                           |
| Campo                                                  | Obbligatorio   | Tipo                            | Sezione                   | Note                                                  |          nan | Cessata al momento del passaggio in giudicato non computabili |
| Anno RG.N.R.                                           | nan            | input text                      | Procedimento              | nan                                                   |          nan | nan                                                           |
| Numero RG.N.R.                                         | nan            | input text                      | Procedimento              | nan                                                   |          nan | nan                                                           |
| Tipo Ufficio PM                                        | *              | select                          | Procedimento              | nan                                                   |          nan | nan                                                           |
| Sede Ufficio PM                                        | *              | input text                      | Procedimento              | nan                                                   |          nan | nan                                                           |
| Anno B.D.M.C.                                          | nan            | input text                      | Procedimento              | nan                                                   |          nan | nan                                                           |
| Numero B.D.M.C.                                        | nan            | input text                      | Procedimento              | nan                                                   |          nan | nan                                                           |
| Anno Reg. Gen.                                         | nan            | input text                      | Procedimento              | nan                                                   |          nan | nan                                                           |
| Numero Reg. Gen.                                       | nan            | input text                      | Procedimento              | nan                                                   |          nan | nan                                                           |
| Tipo ufficio Reg. Gen.                                 | nan            | select                          | Procedimento              | nan                                                   |          nan | nan                                                           |
| Autorità Emittente                                     | *              | select                          | Autorità emittente        | nan                                                   |          nan | nan                                                           |
| Luogo Autorità Emittente                               | nan            | input text                      | Autorità emittente        | nan                                                   |          nan | nan                                                           |
| Giorno Data emissione Ordinanza                        | nan            | input text                      | Autorità emittente        | nan                                                   |          nan | nan                                                           |
| Mese Data emissione Ordinanza                          | nan            | input text                      | Autorità emittente        | nan                                                   |          nan | nan                                                           |
| Anno Data emissione Ordinanza                          | nan            | input text                      | Autorità emittente        | nan                                                   |          nan | nan                                                           |
| Espiazione pena (istituto detenzione / altro luogo)    | nan            | radio                           | Misura cautelare          | nan                                                   |          nan | nan                                                           |
| Misura non detentiva                                   | *              | select                          | Misura cautelare          | Obbligatorio in alternativa alla misura detentiva     |          nan | nan                                                           |
| Misura detentiva                                       | *              | select                          | Misura cautelare          | Obbligatorio in alternativa alla misura non detentiva |          nan | nan                                                           |
| Giorno Data inizio misura                              | *              | input text                      | Misura cautelare          | nan                                                   |          nan | nan                                                           |
| Mese Data inizio misura                                | *              | input text                      | Misura cautelare          | nan                                                   |          nan | nan                                                           |
| Anno Data inizio misura                                | *              | input text                      | Misura cautelare          | nan                                                   |          nan | nan                                                           |
| Giorno Data fine misura                                | *              | input text                      | Misura cautelare          | nan                                                   |          nan | nan                                                           |
| Mese Data fine misura                                  | *              | input text                      | Misura cautelare          | nan                                                   |          nan | nan                                                           |
| Anno Data fine misura                                  | *              | input text                      | Misura cautelare          | nan                                                   |          nan | nan                                                           |
| Istituto di Detenzione                                 | nan            | input text (readonly con popup) | Espiazione in istituto    | Campo compilato tramite popup di selezione istituto   |          nan | nan                                                           |
| Luogo di espiazione                                    | nan            | input text                      | Espiazione in altro luogo | nan                                                   |          nan | nan                                                           |
| Autorità competente per territorio                     | nan            | select                          | Espiazione in altro luogo | nan                                                   |          nan | nan                                                           |
| Sede autorità competente                               | nan            | input text                      | Espiazione in altro luogo | nan                                                   |          nan | nan                                                           |
| Indirizzo autorità competente                          | nan            | textarea                        | Espiazione in altro luogo | nan                                                   |          nan | nan                                                           |
| Motivo Non Computabilità                               | nan            | select                          | Non computabilità         | nan                                                   |          nan | nan                                                           |
| Giorno Data provvedimento di Fungibilità               | nan            | input text                      | Non computabilità         | nan                                                   |          nan | nan                                                           |
| Mese Data provvedimento di Fungibilità                 | nan            | input text                      | Non computabilità         | nan                                                   |          nan | nan                                                           |
| Anno Data provvedimento di Fungibilità                 | nan            | input text                      | Non computabilità         | nan                                                   |          nan | nan                                                           |
| Anno SIEP                                              | nan            | input text                      | Riferimento SIEP          | nan                                                   |          nan | nan                                                           |
| Numero SIEP                                            | nan            | input text                      | Riferimento SIEP          | nan                                                   |          nan | nan                                                           |
| Ufficio riferimento                                    | nan            | select                          | Riferimento SIEP          | nan                                                   |          nan | nan                                                           |
| Sede riferimento                                       | nan            | input text                      | Riferimento SIEP          | nan                                                   |          nan | nan                                                           |
| Note                                                   | nan            | textarea                        | Note                      | nan                                                   |          nan | nan                                                           |
| nan                                                    | nan            | nan                             | nan                       | nan                                                   |          nan | nan                                                           |
| Indice                                                 | nan            | nan                             | nan                       | nan                                                   |          nan | nan                                                           |


## Residenza

| Campo         | Obbligatorio   | Tipo       | Sezione        | Note                                                                                   |
|:--------------|:---------------|:-----------|:---------------|:---------------------------------------------------------------------------------------|
| Indirizzo     | nan            | input text | Dati Residenza | Stringa max 100 caratteri                                                              |
| Cap           | nan            | input text | Dati Residenza | Numerico, lunghezza esatta 5 cifre (validazione JS)                                    |
| Luogo         | *              | input text | Dati Residenza | Obbligatorio quando Stato = Italia (039); valorizzabile tramite popup selezione comune |
| Comune Estero | *              | input text | Dati Residenza | Obbligatorio quando Stato estero (diverso da 039); non compilare se Stato = Italia     |
| Stato         | *              | select     | Dati Residenza | Sempre obbligatorio; selezione nazione da lista                                        |
| nan           | nan            | nan        | nan            | nan                                                                                    |
| Indice        | nan            | nan        | nan            | nan                                                                                    |


## Domicilio

| Campo         | Obbligatorio   | Tipo       | Sezione   | Note                                                         |
|:--------------|:---------------|:-----------|:----------|:-------------------------------------------------------------|
| Indirizzo     | nan            | input text | Domicilio | Se valorizzato, attiva controlli su Luogo/Comune Estero      |
| Cap           | nan            | input text | Domicilio | Validazione JavaScript: numerico, lunghezza minima 5         |
| Luogo         | *              | input text | Domicilio | Obbligatorio quando Stato = Italia (codice 039)              |
| Comune Estero | *              | input text | Domicilio | Obbligatorio per Stato estero quando è presente un indirizzo |
| Stato         | *              | select     | Domicilio | Obbligatorio (non può essere '-')                            |
| nan           | nan            | nan        | nan       | nan                                                          |
| Indice        | nan            | nan        | nan       | nan                                                          |


## PagamentoPP

| Campo                                            | Obbligatorio   | Tipo       | Sezione                   | Note                                                                             |
|:-------------------------------------------------|:---------------|:-----------|:--------------------------|:---------------------------------------------------------------------------------|
| Importo da pagare - Intero                       | *              | input text | Importo da pagare         | Obbligatorio come valore complessivo (> 0) insieme alla parte decimale           |
| Importo da pagare - Decimale                     | *              | input text | Importo da pagare         | Obbligatorio come valore complessivo (> 0) insieme alla parte intera             |
| Tipo rateizzazione - Unica Soluzione             | nan            | radio      | Tipo Rateizzazione        | Alternativa a Pagamento Rateizzato                                               |
| Tipo rateizzazione - Pagamento Rateizzato        | nan            | radio      | Tipo Rateizzazione        | Alternativa a Unica Soluzione                                                    |
| Importo rata unica - Intero                      | *              | input text | Pagamento Unica Soluzione | Obbligatorio se tipo rateizzazione = Unica Soluzione                             |
| Importo rata unica - Decimale                    | *              | input text | Pagamento Unica Soluzione | Obbligatorio se tipo rateizzazione = Unica Soluzione                             |
| Numero rate (riga attiva i)                      | *              | input text | Pagamento Rateizzato      | Obbligatorio per ogni riga visibile se tipo rateizzazione = Pagamento Rateizzato |
| Importo ciascuna rata - Intero (riga attiva i)   | *              | input text | Pagamento Rateizzato      | Obbligatorio per ogni riga visibile se tipo rateizzazione = Pagamento Rateizzato |
| Importo ciascuna rata - Decimale (riga attiva i) | *              | input text | Pagamento Rateizzato      | Obbligatorio per ogni riga visibile se tipo rateizzazione = Pagamento Rateizzato |
| nan                                              | nan            | nan        | nan                       | nan                                                                              |
| Indice                                           | nan            | nan        | nan                       | nan                                                                              |


## CivilmenteObbligato

| Campo                                             | Obbligatorio   | Tipo       | Sezione                                 | Note                                                                              |
|:--------------------------------------------------|:---------------|:-----------|:----------------------------------------|:----------------------------------------------------------------------------------|
| Tipologia Persona (Fisica/Giuridica)              | *              | radio      | Selezione iniziale                      | Visibile solo in modalità inserimento (modalita = I)                              |
| Qualifica                                         | nan            | select     | Persona Fisica                          | Se valorizzata mostra la sezione "Eventuale Seconda Persona Civilmente Obbligata" |
| Cognome                                           | *              | input text | Persona Fisica                          | Obbligatorio                                                                      |
| Nome                                              | *              | input text | Persona Fisica                          | Obbligatorio                                                                      |
| Sesso                                             | *              | select     | Persona Fisica                          | Obbligatorio                                                                      |
| Giorno Data di Nascita                            | *              | input text | Persona Fisica                          | Obbligatorio                                                                      |
| Mese Data di Nascita                              | *              | input text | Persona Fisica                          | Obbligatorio                                                                      |
| Anno Data di Nascita                              | *              | input text | Persona Fisica                          | Obbligatorio                                                                      |
| Comune di Nascita                                 | *              | input text | Persona Fisica                          | Obbligatorio se Stato di Nascita = Italia (039)                                   |
| Stato di Nascita                                  | nan            | select     | Persona Fisica                          | nan                                                                               |
| Comune di Nascita Estero                          | nan            | input text | Persona Fisica                          | Usato quando Stato di Nascita diverso da Italia                                   |
| Codice Fiscale                                    | nan            | input text | Persona Fisica                          | Validazione alfanumerica                                                          |
| Pec                                               | nan            | input text | Persona Fisica                          | nan                                                                               |
| Email                                             | nan            | input text | Persona Fisica                          | nan                                                                               |
| Indirizzo                                         | nan            | input text | Residenza/Domicilio Persona Fisica      | nan                                                                               |
| Comune di Residenza (Luogo)                       | *              | input text | Residenza/Domicilio Persona Fisica      | Obbligatorio se Stato di Residenza = Italia (039)                                 |
| CAP                                               | nan            | input text | Residenza/Domicilio Persona Fisica      | Validazione numerica                                                              |
| Comune Estero                                     | nan            | input text | Residenza/Domicilio Persona Fisica      | Usato quando Stato di Residenza diverso da Italia                                 |
| Stato di Residenza                                | nan            | select     | Residenza/Domicilio Persona Fisica      | nan                                                                               |
| Cognome Seconda Persona Civilmente Obbligata      | *              | input text | Seconda Persona Civilmente Obbligata    | Sezione condizionale (quando Qualifica diversa da '-')                            |
| Nome Seconda Persona Civilmente Obbligata         | *              | input text | Seconda Persona Civilmente Obbligata    | Sezione condizionale (quando Qualifica diversa da '-')                            |
| Sesso Seconda Persona Civilmente Obbligata        | *              | select     | Seconda Persona Civilmente Obbligata    | Sezione condizionale (quando Qualifica diversa da '-')                            |
| Giorno Data di Nascita Seconda Persona            | *              | input text | Seconda Persona Civilmente Obbligata    | Se compilati Cognome/Nome seconda persona                                         |
| Mese Data di Nascita Seconda Persona              | *              | input text | Seconda Persona Civilmente Obbligata    | Se compilati Cognome/Nome seconda persona                                         |
| Anno Data di Nascita Seconda Persona              | *              | input text | Seconda Persona Civilmente Obbligata    | Se compilati Cognome/Nome seconda persona                                         |
| Comune di Nascita Seconda Persona                 | *              | input text | Seconda Persona Civilmente Obbligata    | Obbligatorio se Stato di Nascita seconda persona = Italia (039)                   |
| Stato di Nascita Seconda Persona                  | nan            | select     | Seconda Persona Civilmente Obbligata    | nan                                                                               |
| Comune di Nascita Estero Seconda Persona          | nan            | input text | Seconda Persona Civilmente Obbligata    | nan                                                                               |
| Codice Fiscale Seconda Persona                    | nan            | input text | Seconda Persona Civilmente Obbligata    | Validazione alfanumerica non esplicita lato client per _ST                        |
| Pec Seconda Persona                               | nan            | input text | Seconda Persona Civilmente Obbligata    | nan                                                                               |
| Email Seconda Persona                             | nan            | input text | Seconda Persona Civilmente Obbligata    | nan                                                                               |
| Indirizzo Seconda Persona                         | nan            | input text | Residenza/Domicilio Seconda Persona     | nan                                                                               |
| Comune di Residenza Seconda Persona (Luogo)       | *              | input text | Residenza/Domicilio Seconda Persona     | Obbligatorio se Stato di Residenza seconda persona = Italia (039)                 |
| CAP Seconda Persona                               | nan            | input text | Residenza/Domicilio Seconda Persona     | nan                                                                               |
| Comune Estero Seconda Persona                     | nan            | input text | Residenza/Domicilio Seconda Persona     | nan                                                                               |
| Stato di Residenza Seconda Persona                | nan            | select     | Residenza/Domicilio Seconda Persona     | nan                                                                               |
| Qualifica                                         | nan            | select     | Persona Giuridica                       | nan                                                                               |
| Società                                           | *              | input text | Persona Giuridica                       | Obbligatorio                                                                      |
| Ragione Sociale                                   | nan            | select     | Persona Giuridica                       | nan                                                                               |
| Provincia                                         | nan            | select     | Persona Giuridica                       | nan                                                                               |
| Partita IVA/Codice Fiscale                        | nan            | input text | Persona Giuridica                       | Validazione alfanumerica                                                          |
| Sede Legale                                       | nan            | input text | Persona Giuridica                       | nan                                                                               |
| Sede Operativa/Indirizzo Attivita                 | nan            | input text | Persona Giuridica                       | nan                                                                               |
| Cognome Legale Rappresentante                     | *              | input text | Legale Rappresentante Persona Giuridica | Obbligatorio                                                                      |
| Nome Legale Rappresentante                        | *              | input text | Legale Rappresentante Persona Giuridica | Obbligatorio                                                                      |
| Sesso Legale Rappresentante                       | *              | select     | Legale Rappresentante Persona Giuridica | Obbligatorio                                                                      |
| Giorno Data di Nascita Legale Rappresentante      | *              | input text | Legale Rappresentante Persona Giuridica | Obbligatorio                                                                      |
| Mese Data di Nascita Legale Rappresentante        | *              | input text | Legale Rappresentante Persona Giuridica | Obbligatorio                                                                      |
| Anno Data di Nascita Legale Rappresentante        | *              | input text | Legale Rappresentante Persona Giuridica | Obbligatorio                                                                      |
| Comune di Nascita Legale Rappresentante           | *              | input text | Legale Rappresentante Persona Giuridica | Obbligatorio se Stato di Nascita = Italia (039)                                   |
| Stato di Nascita Legale Rappresentante            | nan            | select     | Legale Rappresentante Persona Giuridica | nan                                                                               |
| Comune di Nascita Estero Legale Rappresentante    | nan            | input text | Legale Rappresentante Persona Giuridica | nan                                                                               |
| Codice Fiscale Legale Rappresentante              | nan            | input text | Legale Rappresentante Persona Giuridica | nan                                                                               |
| Pec Legale Rappresentante                         | nan            | input text | Legale Rappresentante Persona Giuridica | nan                                                                               |
| Email Legale Rappresentante                       | nan            | input text | Legale Rappresentante Persona Giuridica | nan                                                                               |
| Indirizzo Legale Rappresentante                   | nan            | input text | Residenza/Domicilio Persona Giuridica   | nan                                                                               |
| Comune di Residenza Legale Rappresentante (Luogo) | *              | input text | Residenza/Domicilio Persona Giuridica   | Obbligatorio se Stato di Residenza = Italia (039)                                 |
| CAP Residenza Legale Rappresentante               | nan            | input text | Residenza/Domicilio Persona Giuridica   | Validazione numerica                                                              |
| Comune Estero Residenza Legale Rappresentante     | nan            | input text | Residenza/Domicilio Persona Giuridica   | nan                                                                               |
| Stato di Residenza Legale Rappresentante          | nan            | select     | Residenza/Domicilio Persona Giuridica   | nan                                                                               |
| nan                                               | nan            | nan        | nan                                     | nan                                                                               |
| Indice                                            | nan            | nan        | nan                                     | nan                                                                               |


## ContinuazioneSentenze

| Campo                    | Obbligatorio   | Tipo       | Sezione                          | Note                                                                                                        |
|:-------------------------|:---------------|:-----------|:---------------------------------|:------------------------------------------------------------------------------------------------------------|
| Tipo Continuazione (*)   | *              | select     | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio quando la riga è compilata o se sono valorizzati campi R.G.N.R./Reg.Gen. |
| Anno Sentenza (*)        | *              | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio quando la riga è compilata                                               |
| Numero Sentenza (*)      | *              | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio quando la riga è compilata                                               |
| Giorno Data Sentenza (*) | *              | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio quando la riga è compilata con data valida                               |
| Mese Data Sentenza (*)   | *              | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio quando la riga è compilata con data valida                               |
| Anno Data Sentenza (*)   | *              | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio quando la riga è compilata con data valida                               |
| Autorità Sentenza (*)    | *              | select     | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio quando la riga è compilata                                               |
| Luogo Sentenza (*)       | *              | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio quando la riga è compilata                                               |
| Anno R.G.N.R.            | nan            | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - opzionale ma obbligatorio se valorizzato Numero R.G.N.R.                              |
| Numero R.G.N.R.          | nan            | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - opzionale ma obbligatorio se valorizzato Anno R.G.N.R.                                |
| Anno Reg.Gen.            | nan            | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio insieme a Numero Reg.Gen. se Tipo Reg.Gen. è valorizzato                 |
| Numero Reg.Gen.          | nan            | input text | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio insieme a Anno Reg.Gen. se Tipo Reg.Gen. è valorizzato                   |
| Tipo Reg.Gen.            | nan            | select     | Continuazione con altre sentenze | Ripetuto su 3 righe - obbligatorio se sono valorizzati Anno e Numero Reg.Gen.                               |
| nan                      | nan            | nan        | nan                              | nan                                                                                                         |
| Indice                   | nan            | nan        | nan                              | nan                                                                                                         |