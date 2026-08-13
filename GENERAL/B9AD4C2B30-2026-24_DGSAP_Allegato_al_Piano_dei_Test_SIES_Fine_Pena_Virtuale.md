---
uniqueName: b9ad4c2b30-2026-24dgsapallegatoalpianodeitestsiesf
displayName: "B9AD4C2B30 2026 24 DGSAP Allegato al Piano dei Test SIES Fine Pena Virtuale"
category: "GENERAL"
tags: []
---

# B9AD4C2B30-2026-24_DGSAP_Allegato_al_Piano_dei_Test_SIES_Fine_Pena_Virtuale

> **File originale:** `MEV/SCHEDA_2026-24/B9AD4C2B30-2026-24_DGSAP_Allegato_al_Piano_dei_Test_SIES_Fine_Pena_Virtuale.xlsx`  
> **Tipo:** XLSX

---

## Copertina

## TabellaTest

| Intervento |  | B9AD4C2B30-2026-24_DGSAP_Scheda_Intervento_SIES_Fine_Pena_Virtuale |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  | B9AD4C2B30-2026-24_DGSAP_Allegato_al_Piano_dei_Test_SIES_Fine_Pena_Virtuale.xlsx |  |  |  |  |  |  |  |  |
| Codice Appl. | ID Requisito Padre | Lista Requisiti | ID Caso d'Uso | Caso d'Uso | ID | Scenario di test | Classe di Gravità (1-4) | Classe di Rilevanza (A, B, C) | Esito |  |
| SIES/SIEP | PAR. 2.1-048-01 | PAR. 2.1-048-01 | UC01 | Visualizzazione Data Fine Pena Virtuale su Dettaglio Procedimento | TF001.UC01 | Verifica: Verificare nel sottosistema SIEP la funzione Storico Calcoli Validati su Calcolo Pena DL 92/2024 in caso di assenza storico | 3 | C |  |  |
| SIES/SIEP | PAR. 2.1-048-01 | PAR. 2.1-048-01 | UC02 | Visualizzazione Data Fine Pena Virtuale su Dettaglio Procedimento | TF001.UC02 | Verifica: Verificare nel sottosistema SIEP la funzione Valida su Calcolo Pena DL 92/2024 | 3 | C |  |  |
| SIES/SIEP | PAR. 2.1-048-01 | PAR. 2.1-048-01 | UC03 | Visualizzazione Data Fine Pena Virtuale su Dettaglio Procedimento | TF001.UC03 | Verifica: Verificare nel sottosistema SIEP la funzione Storico Calcoli Validati su Calcolo Pena DL 92/2024 | 3 | C |  |  |
| SIES/SIEP | PAR. 2.1-048-01 | PAR. 2.1-048-01 | UC04 | Visualizzazione Data Fine Pena Virtuale su Dettaglio Procedimento | TF001.UC04 | Verifica: Verificare nel sottosistema SIEP la funzione Dettaglio Procedimento | 3 | C |  |  |
| SIES/SIEP | PAR. 2.2-048-02 | PAR. 2.2-048-02 | UC01 | Visualizzazione Scadenzario Fine Pena | TF002.UC01 | Verifica: Verificare nel sottosistema SIEP la funzione Scadenzario Fine Pena | 3 | C |  |  |
| SIES/SIUS | PAR. 3.1-048-03 | PAR. 3.1-048-03 | UC01 | Ricerca Fine Pena Procedimenti Pendenti | TF003.UC01 | Verifica: Verificare nel sottosistema SIUS la funzione Ricerca Fine Pena Procedimenti Pendenti per data fine pena reale | 3 | C |  |  |
| SIES/SIUS | PAR. 3.1-048-03 | PAR. 3.1-048-03 | UC02 | Ricerca Fine Pena Procedimenti Pendenti | TF003.UC02 | Verifica: Verificare nel sottosistema SIUS la funzione Ricerca Fine Pena Procedimenti Pendenti per fine pena virtuale | 3 | C |  |  |
| SIES/SIUS | PAR.3.2-048-04 | PAR.3.2-048-04 | UC01 | Condivisione Calcolatrice DL 92/2024 di SIEP lato SIUS | TF004.UC01 | Condivisione Calcolatrice DL 92/2024 di SIEP lato SIUS | 3 | C |  |  |

## SpecificaTest

| Intervento |  |  | B9AD4C2B30-2026-24_DGSAP_Scheda_Intervento_SIES_Fine_Pena_Virtuale |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | B9AD4C2B30-2026-24_DGSAP_Allegato_al_Piano_dei_Test_SIES_Fine_Pena_Virtuale.xlsx |  |  |  |
| ID caso di test | Requisito |  | Caso d'uso |  | Scenario di test |  |
| TF001.UC01 | PAR. 2.1-048-01 |  | Visualizzazione Data Fine Pena Virtuale su Dettaglio Procedimento |  | Verifica: Verificare nel sottosistema SIEP la funzione Storico Calcoli Validati su Calcolo Pena DL 92/2024 in caso di assenza storico |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura c/o Tribunale | Axxxxx (Procura c/o Tribunale) |  |  |
|  | P | Stato Base | L'utente ricerca un procedimento di classe 1 con Soggetto detenuto e con almeno 4 anni di pena |  | Visualizzazione pagina di Dettaglio  procedimento |  |
|  | 1 | Navigazione | selezionare la funzione Calcolo Pena DL 92/2024 |  | Visualizzazione pagina   Calcolo pena ipotetica con detrazioni DL. 92/2024 |  |
|  | V | Verifica | Verificare che sia presente il tasto Storico Calcolo Validati |  |  |  |
|  | 2 | Azione | Cliccare sul tasto Storico Calcolo Validati |  | Visualizzazione pagina  Storico Calcolo pena ipotetica con detrazioni DL. 92/2024 |  |
|  | V | Verifica | Verificare che sia presente alcun dato storicizzato e sia riportata la dicitura Nessun calcolo e' stato validato per il fascicolo corrente |  |  |  |
| TF001.UC02 | PAR. 2.1-048-01 |  | Visualizzazione Data Fine Pena Virtuale su Dettaglio Procedimento |  | Verifica: Verificare nel sottosistema SIEP la funzione Valida su Calcolo Pena DL 92/2024 |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura c/o Tribunale | Axxxxx (Procura c/o Tribunale) |  |  |
|  | P | Stato Base | L'utente è posizionato sulla form di Dettaglio del procedimento SIEP del test precedente |  | Visualizzazione pagina di Dettaglio  procedimento |  |
|  | 1 | Navigazione | selezionare la funzione Calcolo Pena DL 92/2024 |  | Visualizzazione pagina   Calcolo pena ipotetica con detrazioni DL. 92/2024 |  |
|  | 2 | Azione | Cliccare sul tasto Conferma |  | Visualizzazione pagina  Calcolo pena ipotetica con detrazioni DL. 92/2024 con il Dettaglio di tutti i dati coinvolti nel calcolo e i risulati dello stesso |  |
|  | 3 | Azione | Cliccare su tasto Valida |  | Visualizzazione messaggio di Conferma a procedere alla storicizzazione dei dati presenti nella pagina |  |
|  | 4 | Azione | Cliccare su OK |  | Visualizzazione messaggio di Avvenuta storicizzazione del Calcolo Pena |  |
|  | V | Verifica | Visualizzazione pagina  Calcolo pena ipotetica con detrazioni DL. 92/2024 con il Dettaglio di tutti i dati coinvolti nel calcolo e i risulati dello stesso |  |  |  |
| TF001.UC03 | TF001.UC03 |  | Visualizzazione Data Fine Pena Virtuale su Dettaglio Procedimento |  | Verifica: Verificare nel sottosistema SIEP la funzione Storico Calcoli Validati su Calcolo Pena DL 92/2024 |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Stato Base | L'utente è posizionato sulla pagina  Calcolo pena ipotetica con detrazioni DL. 92/2024 con il Dettaglio di tutti i dati coinvolti nel calcolo del precedente test |  |  |  |
|  | 1 | Azione | Cliccare sul tasto Storico Calcolo Validati |  | Visualizzazione pagina  Storico Calcolo pena ipotetica con detrazioni DL. 92/2024 |  |
|  | V | Verifica | Verificare che nell'Elenco dei dati storicizzati, sia riportato quello validato nel precedente test |  |  |  |
|  | 3 | Azione | Cliccare sull'icona di Dettaglio per il record di interesse |  | Visualizzazione pagina  Storico Calcolo pena ipotetica con detrazioni DL. 92/2024 |  |
|  | V | Verifica | Verificare che siano riportati tutti i dati di input e i dati generati dal calcolo |  |  |  |
|  | 4 | Azione | Cliccare su icona di Ritorna su |  | Visualizzazione pagina  Storico Calcolo pena ipotetica con detrazioni DL. 92/2024 |  |
| TF001.UC04 | TF001.UC04 |  | Visualizzazione Data Fine Pena Virtuale su Dettaglio Procedimento |  | Verifica: Verificare nel sottosistema SIEP la funzione Dettaglio Procedimento |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura c/o Tribunale | Axxxxx (Procura c/o Tribunale) |  |  |
|  | P | Stato Base | L'utente è posizionato sulla pagina Calcolo pena ipotetica con detrazioni DL. 92/2024  del procedimento SIEP del test precedente |  | Visualizzazione pagina   Calcolo pena ipotetica con detrazioni DL. 92/2024 |  |
|  | 1 | Azione | Cliccare su Anno e Numero procedimento |  | Visualizzazione pagina di Dettaglio  procedimento |  |
|  | V | Verifica | Verificare che accanto alle date inizio e fine pena sia presente la data Fine Pena Virtuale |  |  |  |
|  | 2 | Azione | Cliccare sul link Fine Pena Virtuale |  | Visualizzazione pagina  Storico Calcolo pena ipotetica con detrazioni DL. 92/2024 |  |
|  | V | Verifica | Verificare che siano riportati tutti i dati di input e i dati generati dal calcolo collegato alla data fine pena virtuale |  |  |  |
|  | 3 | Azione | Cliccare su icona di Ritorna su |  | Visualizzazione pagina di Dettaglio  procedimento |  |
| TF002.UC01 | TF002.UC01 |  | Visualizzazione Scadenzario Fine Pena |  | Verifica: Verificare nel sottosistema SIEP la funzione Scadenzario Fine Pena |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura c/o Tribunale | Axxxxx (Procura c/o Tribunale) |  |  |
|  | P | Stato Base | L'utente è posizionato sulla Home Page |  |  |  |
|  | 1 | Navigazione | selezionare la funzione Scadenzari>>Fine Pena |  | Visualizzazione pagina   Consultazione Scadenzario Fine Pena |  |
|  | 2 | Azione | Impostare radio button In scadenza,  Anni 5 e cliccare Ricerca |  | Visualizzazione pagina di   Consultazione Scadenzario Fine Pena - In Scadenza |  |
|  | V | Verifica | Verificare che nell'Elenco sia presente la nuova colonna Fine Pena Virtuale |  |  |  |
|  | P | Attività Preliminari e/o Precondizioni | Per alcuni dei procedimenti presenti nell'Elenco, procedere a utilizzare la funzione Calcolo Pena DL 92/2024 e la relativa funzione Valida |  |  |  |
|  | R1 | Riciclo Test | Ripetere passo 1 e 2 del test |  |  |  |
|  | V | Verifica | Verificare che nell'Elenco sia presente la nuova colonna Fine Pena Virtuale e che la stessa risulti valorizzata per i procedimenti su cui è stata utilizzata la funzione di Calcolo |  |  |  |
| TF003.UC01 | TF003.UC01 |  | Ricerca Fine Pena Procedimenti Pendenti |  | Verifica: Verificare nel sottosistema SIUS la funzione Ricerca Fine Pena Procedimenti Pendenti per data fine pena reale |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente è collegato al sistema SIUS come Ufficio di Sorveglianza | Exxxxx (Ufficio di Sorveglianza) |  |  |
|  | P | Stato Base | L'utente è posizionato nella Home Page SIUS |  |  |  |
|  | 1 | Navigazione | Scadenzari >> Ricerca Fine Pena Procedimenti Pendenti |  | Visualizzazione pagina Ricerca Fine Pena Procedimenti Pendenti |  |
|  | V | Verifica | Verificare che siano presenti i seguenti filtri di ricerca: Intervallo Estremi Procedimenti ; Intervallo Date Iscrizione (uno dei due intervalli è obbligatorio); Criteri di ricerca (Tutti, In scadenza entro periodo, in scadenza oggi, scaduti) obbligatorio; Data Fine Pena Reale, Data Fine Pena Virtuale |  |  |  |
|  | 2 | Azione | Valorizzare Intervallo Estremi Procedimenti, In scadenza entro 5 anni, Data Fine Pena Reale e cliccare su Ricerca |  | Visualizzazione pagina Elenco Procedimenti Pendenti con data inizio e Fine Pena |  |
|  | V | Verifica | Verificare che la form sia impaginata e presenti 20 risultati per pagina ordinata per data fine decrescente, per ciascuna riga siano riportati: Anno e Numero procedimento SIUS, Cognome e Nome soggetto, Luogo e Data nascita, Posizione Giuridica, Contenuto, Data inizio pena, Data Fine Pena, giorni residui alla scadenza dalla data odierna, Fine pena virtuale, giorni residui alla scadenza, Anno e Numero procedimento SIEP |  |  |  |
| TF003.UC02 | TF003.UC02 |  | Ricerca Fine Pena Procedimenti Pendenti |  | Verifica: Verificare nel sottosistema SIUS la funzione Ricerca Fine Pena Procedimenti Pendenti per fine pena virtuale |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente è collegato al sistema SIUS come Ufficio di Sorveglianza | Exxxxx (Ufficio di Sorveglianza) | Per alcuni dei procedimenti SIEP estratti nel precedente Test, lato SIEP bisogna calcolare la data fine pena virtuale |  |
|  | P | Stato Base | L'utente è posizionato nella Home Page SIUS |  |  |  |
|  | 1 | Navigazione | Scadenzari >> Ricerca Fine Pena Procedimenti Pendenti |  | Visualizzazione pagina Ricerca Fine Pena Procedimenti Pendenti |  |
|  | V | Verifica | Verificare che siano presenti i seguenti filtri di ricerca: Intervallo Estremi Procedimenti ; Intervallo Date Iscrizione (uno dei due intervalli è obbligatorio); Criteri di ricerca (Tutti, In scadenza entro periodo, in scadenza oggi, scaduti) obbligatorio; Data Fine Pena Reale, Data Fine Pena Virtuale |  |  |  |
|  | 2 | Azione | Valorizzare Intervallo Estremi Procedimenti, In scadenza entro 5 anni, Data Fine Pena Virtuale e cliccare su Ricerca |  | Visualizzazione pagina Elenco Procedimenti Pendenti con data inizio e Fine Pena |  |
|  | V | Verifica | Verificare che la form sia impaginata e presenti 20 risultati per pagina ordinata per data fine vrtuale decrescente, per ciascuna riga siano riportati: Anno e Numero procedimento SIUS, Cognome e Nome soggetto, Luogo e Data nascita, Posizione Giuridica, Contenuto, Data inizio pena, Data Fine Pena, giorni residui alla scadenza dalla data odierna, Fine pena virtuale, giorni residui alla scadenza, Anno e Numero procedimento SIEP |  |  |  |
| TF004.UC01 | PAR.3.2-048-04 |  | Condivisione Calcolatrice DL 92/2024 di SIEP lato SIUS |  | Condivisione Calcolatrice DL 92/2024 di SIEP lato SIUS |  |
|  | Step | Tipo | Istruzioni
(test) | Dati di input
(Associated Data) | Risultati attesi
(Expected Result) | Esito |
|  | P | Attività Preliminari e/o Precondizioni | L'utente effettua l'accesso al sistema SIEP come Procura c/o Tribunale | Exxxxx (Ufficio di Sorveglianza) |  |  |
|  | P | Stato Base | L'utente ricerca un procedimento SIEP validato |  | Visualizzazione pagina di Dettaglio  procedimento SIEP |  |
|  | 1 | Navigazione | selezionare la funzione Calcolo Pena DL 92/2024 nel menu verticale |  | Visualizzazione pagina   Calcolo pena ipotetica con detrazioni DL. 92/2024 |  |
|  | 2 | Azione | Cliccare sul tasto Conferma |  | Visualizzazione pagina  Calcolo pena ipotetica con detrazioni DL. 92/2024 con il Dettaglio di tutti i dati coinvolti nel calcolo e i risultati dello stesso |  |
|  | V | Verifica | che nella form sia presente solo il tasto Ricalcolo, quindi non sia presente il tasto Valida |  |  |  |

## VerificheConformità

| Intervento |  |  | B9AD4C2B30-2026-24_DGSAP_Scheda_Intervento_SIES_Fine_Pena_Virtuale |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  |  | B9AD4C2B30-2026-24_DGSAP_Allegato_al_Piano_dei_Test_SIES_Fine_Pena_Virtuale.xlsx |  |  |  |  |
| ID | Tipo Verifica | Attributo | Indicatore | Descrizione tipo Verifica | Esito Verifica Fornitore | Esito Verifica Amministrazione |  |
| 001 | Adeguatezza delle funzionalità | Completezza funzionale | Copertura dei requisiti | Verifica del grado di copertura funzionale offerta sulla base dell’analisi dei requisiti, delle funzionalità e degli obiettivi richiesti | OK |  |  |
| 002 | Adeguatezza delle funzionalità | Correttezza funzionale | Aderenza ai requisiti | Verifica del grado con cui le funzionalità implementate rispettano i requisiti richiesti | OK |  |  |
| 003 | Adeguatezza delle funzionalità | Appropriatezza funzionale | Conformità alle normative | Verifica l’aderenza delle funzionalità implementate rispetto alle normative pertinenti | OK |  |  |
| 004 | Affidabilità | Robustezza | Robustezza del software | Verifica della capacità del sistema di gestire condizioni non previste dalle specifiche | OK |  |  |
| 005 | Manutenibilità | Analizzabilità | Leggibilità del codice | Verifica della facilità di comprensione del codice, per esempio con riferimento ai nomi utilizzati per i moduli, le funzioni e le variabili, ai commenti e alla dimensione dei moduli e delle funzioni | OK |  |  |
| 006 | Manutenibilità | Analizzabilità | Copertura documentazione tecnica | Verifica del livello di completezza della documentazione tecnica di moduli e funzioni | OK |  |  |
| 007 | Manutenibilità | Analizzabilità | Adeguatezza documentazione tecnica | Verifica della qualità descrittiva della documentazione tecnica di moduli e funzioni | OK |  |  |
| 008 | Manutenibilità | Verificabilità | Completezza dei test | Verifica del grado di copertura del codice sviluppato da parte di test (di varia natura, come test unitari, test di integrazione, test end-to-end, test di accettazione, test di regressione, test di qualità) | OK |  |  |

## SogliaAccettazione

| Intervento |  | B9AD4C2B30-2026-24_DGSAP_Scheda_Intervento_SIES_Fine_Pena_Virtuale |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Codifica Piano di test |  | B9AD4C2B30-2026-24_DGSAP_Allegato_al_Piano_dei_Test_SIES_Fine_Pena_Virtuale.xlsx |  |  |  |  |  |  |
| Verifica Soglia di Accettazione |  |  |  |  |  | In Rosso le difformità che hanno superato il numero massimo ammissibile |  |  |
| Classe di rilevanza | Classe di gravità |  |  |  |  |  |  |  |
|  | 1 | 2 | 3 | 4 |  |  |  |  |
| A |  |  |  |  |  |  |  |  |
| B |  |  |  |  |  |  |  |  |
| C |  |  |  |  |  |  |  |  |
| Numero massimo di difformità ammesse |  |  |  |  |  |  |  |  |
| Classe di rilevanza | Classe di gravità |  |  |  |  |  |  |  |
|  | 1 | 2 | 3 | 4 |  |  |  |  |
| A |  |  |  |  |  |  |  |  |
| B |  |  |  |  |  |  |  |  |
| C |  |  | 6 |  |  |  |  |  |