---
uniqueName: usecasestds
displayName: "useCasesTDS"
category: "GENERAL"
tags: []
---

# Casi d'uso – SIUS – Tribunale di Sorveglianza (TDS / TDSM)

**Sottosistema:** SIUS (Sistema Informativo Unico per la Sorveglianza)  
**Attore:** Tribunale di Sorveglianza adulti (**TDS**) e Tribunale di Sorveglianza Minorenni (**TDSM**)  
**Tipo organo:** Collegiale (3 giudici)  
**Tipo provvedimento principale:** Decreto

---

## UC-T01 – Iscrizione fascicolo SIUS da procedimento SIEP

**Precondizione:** Esiste un procedimento SIEP da cui origina la competenza del TDS.  
**Flusso:** L'utente TDS ricerca il procedimento SIEP → seleziona il fascicolo di origine → inserisce i dati del generale del procedimento (oggetto, data richiesta, tipo atto, sede mittente, autorità delegata) → registra i tenori (soggetti giuridici) → il sistema crea il fascicolo SIUS in stato "aperto" (02).  
**Postcondizione:** Fascicolo SIUS creato, abbinato al fascicolo SIEP e al soggetto.

---

## UC-T02 – Assegnazione magistrato relatore

**Precondizione:** Fascicolo SIUS aperto.  
**Flusso:** L'utente assegna un magistrato relatore al fascicolo (o al singolo tenore) selezionandolo dall'elenco degli ufficiali giudiziari.  
**Postcondizione:** Magistrato relatore registrato sul fascicolo/tenore.

---

## UC-T03 – Fissazione udienza collegiale

**Precondizione:** Fascicolo SIUS aperto, magistrato relatore assegnato.  
**Flusso:** L'utente fissa l'udienza collegiale (data, ora, aula) → associa i procedimenti da trattare → il sistema registra la fissazione.  
**Postcondizione:** Udienza collegiale schedulata.

---

## UC-T04 – Modifica/cancellazione udienza collegiale

**Precondizione:** Udienza già fissata, non ancora tenuta.  
**Flusso:** L'utente modifica data/ora/aula o cancella l'udienza.  
**Postcondizione:** Udienza aggiornata o cancellata.

---

## UC-T05 – Redazione verbale udienza

**Precondizione:** Udienza tenuta.  
**Flusso:** L'utente inserisce il verbale dell'udienza (presenze, dichiarazioni, esito) → il sistema registra il verbale collegato all'udienza.  
**Postcondizione:** Verbale udienza registrato.

---

## UC-T06 – Rinvio udienza con decreto/sentenza di rinvio

**Precondizione:** Udienza in corso o conclusa senza decisione finale.  
**Flusso:** L'utente inserisce il decreto/sentenza di rinvio → specifica la nuova data → il sistema crea la nuova fissazione.  
**Postcondizione:** Udienza rinviata, nuovo appuntamento creato.

---

## UC-T07 – Emissione decreto di inammissibilità

**Precondizione:** Fascicolo SIUS aperto; il TDS valuta la richiesta inammissibile.  
**Flusso:** L'utente seleziona il tipo decreto "Inammissibilità" → compila motivazione e data deposito → il sistema registra il decreto sull'evento.  
**Postcondizione:** Decreto di inammissibilità depositato, fascicolo può essere archiviato.

---

## UC-T08 – Emissione decreto di incompetenza

**Precondizione:** Fascicolo SIUS aperto; il TDS dichiara la propria incompetenza territoriale/materiale.  
**Flusso:** Tipo decreto "Incompetenza" → compilazione dati → il sistema può avviare la trasmissione degli atti all'ufficio competente.  
**Postcondizione:** Decreto di incompetenza depositato.

---

## UC-T09 – Emissione decreto di irreperibilità

**Precondizione:** Il soggetto non è reperibile.  
**Flusso:** Tipo decreto "Irreperibilità" → registrazione dati → deposito.  
**Postcondizione:** Decreto depositato, iter sospeso.

---

## UC-T10 – Emissione decreto di revoca (misura alternativa / misura di sicurezza)

**Precondizione:** Misura alternativa o di sicurezza in corso di esecuzione; sopravviene causa di revoca.  
**Flusso:** Tipo decreto "Revoca" → selezione della misura da revocare → compilazione motivazione → deposito.  
**Postcondizione:** Misura revocata, esecuzione aggiornata.

---

## UC-T11 – Emissione decreto per violazione CEDU

**Precondizione:** Accertata violazione della Convenzione Europea dei Diritti dell'Uomo.  
**Flusso:** Tipo decreto "Violazione CEDU" → inserimento dati specifici CEDU → deposito.  
**Postcondizione:** Decreto CEDU registrato.

---

## UC-T12 – Emissione decreto di unificazione pene (cumulo)

**Precondizione:** Esistono più fascicoli/titoli esecutivi a carico del medesimo soggetto.  
**Flusso:** L'utente avvia l'unificazione → seleziona i fascicoli da unificare → calcola il cumulo → emette il decreto di unificazione.  
**Postcondizione:** Fascicoli unificati, unico fascicolo cumulato, decreto di unificazione depositato.

---

## UC-T13 – Annullamento di un decreto

**Precondizione:** Decreto precedentemente emesso; sopravviene causa di annullamento.  
**Flusso:** L'utente seleziona il decreto → inserisce la motivazione dell'annullamento → il sistema verifica l'esistenza di un Foglio Complementare trasmesso e aggiorna di conseguenza la nota sull'evento.  
**Postcondizione:** Decreto annullato, motivazione registrata.

---

## UC-T14 – Stampa / esportazione decreto

**Precondizione:** Decreto depositato.  
**Flusso:** L'utente seleziona il decreto → avvia la stampa → il sistema genera il documento.  
**Postcondizione:** Documento cartaceo/PDF del decreto prodotto.

---

## UC-T15 – Trasmissione decreto ad altro ufficio

**Precondizione:** Decreto emesso; necessità di trasmetterlo a TDS/UDS competente.  
**Flusso:** L'utente seleziona il decreto → indica l'ufficio destinatario → conferma la trasmissione.  
**Postcondizione:** Decreto trasmesso, stato trasmissione registrato.

---

## UC-T16 – Registrazione impugnazione contro decreto

**Precondizione:** Decreto emesso; la parte interessata propone impugnazione.  
**Flusso:** L'utente registra l'impugnazione (tipo, data, parte impugnante) → il sistema collega l'impugnazione al decreto/evento.  
**Postcondizione:** Impugnazione registrata.

---

## UC-T17 – Ricerca e consultazione fascicoli

**Precondizione:** Utente TDS/TDSM autenticato.  
**Flusso:** L'utente inserisce criteri di ricerca (soggetto, anno, numero, stato) → il sistema restituisce l'elenco dei fascicoli → l'utente accede al dettaglio.  
**Postcondizione:** Fascicolo visualizzato.

---

## UC-T18 – Inserimento e gestione allegati documentali

**Precondizione:** Fascicolo SIUS aperto.  
**Flusso:** L'utente allega documenti digitali al fascicolo o a un evento specifico.  
**Postcondizione:** Documento allegato registrato.

---

## UC-T19 – Aggiornamento posizione materiale fascicolo

**Precondizione:** Fascicolo fisico cartaceo localizzato in archivio.  
**Flusso:** L'utente aggiorna la posizione fisica (scaffale, busta, archivio) del fascicolo.  
**Postcondizione:** Posizione materiale aggiornata.

---

## UC-T20 – Gestione scadenzario

**Precondizione:** Fascicolo aperto con scadenze giuridiche da monitorare.  
**Flusso:** L'utente visualizza o aggiorna le scadenze associate al fascicolo (fine pena, termine misura, ecc.).  
**Postcondizione:** Scadenze aggiornate/monitorate.

---

## UC-T21 – Produzione e trasmissione atti

**Precondizione:** Necessità di produrre o trasmettere atti processuali.  
**Flusso:** L'utente registra la produzione di atti → eventualmente avvia la trasmissione all'ufficio destinatario.  
**Postcondizione:** Produzione/trasmissione atti registrata.

---

## UC-T22 – Stralcio del procedimento

**Precondizione:** Fascicolo con procedimento da concludere parzialmente.  
**Flusso:** L'utente registra lo stralcio parziale del procedimento (es. estrazione di un soggetto o di un titolo).  
**Postcondizione:** Stralcio registrato, fascicolo parzialmente concluso.

---

## UC-T23 – Generazione statistiche

**Precondizione:** Utente TDS/TDSM con privilegi statistici.  
**Flusso:** L'utente seleziona i parametri statistici (periodo, tipo procedimento, tipo decisione) → il sistema genera il report.  
**Postcondizione:** Report statistico prodotto.

---

## UC-T24 – Gestione riferimenti a procedimenti SIEP (RIFASIEP)

**Precondizione:** Fascicolo SIUS esistente.  
**Flusso:** L'utente aggiunge, modifica o elimina i riferimenti ai procedimenti SIEP collegati al fascicolo SIUS.  
**Postcondizione:** Riferimenti SIEP aggiornati.

---

## UC-T25 – Gestione riferimenti interni SIUS (RIFASIUS)

**Precondizione:** Fascicolo SIUS esistente.  
**Flusso:** L'utente gestisce i riferimenti ad altri fascicoli SIUS collegati (procedimenti correlati).  
**Postcondizione:** Riferimenti SIUS aggiornati.

---

## Riepilogo

| Codice | Titolo |
|--------|--------|
| UC-T01 | Iscrizione fascicolo SIUS da procedimento SIEP |
| UC-T02 | Assegnazione magistrato relatore |
| UC-T03 | Fissazione udienza collegiale |
| UC-T04 | Modifica/cancellazione udienza collegiale |
| UC-T05 | Redazione verbale udienza |
| UC-T06 | Rinvio udienza con decreto/sentenza di rinvio |
| UC-T07 | Emissione decreto di inammissibilità |
| UC-T08 | Emissione decreto di incompetenza |
| UC-T09 | Emissione decreto di irreperibilità |
| UC-T10 | Emissione decreto di revoca |
| UC-T11 | Emissione decreto per violazione CEDU |
| UC-T12 | Emissione decreto di unificazione pene |
| UC-T13 | Annullamento di un decreto |
| UC-T14 | Stampa / esportazione decreto |
| UC-T15 | Trasmissione decreto ad altro ufficio |
| UC-T16 | Registrazione impugnazione contro decreto |
| UC-T17 | Ricerca e consultazione fascicoli |
| UC-T18 | Inserimento e gestione allegati documentali |
| UC-T19 | Aggiornamento posizione materiale fascicolo |
| UC-T20 | Gestione scadenzario |
| UC-T21 | Produzione e trasmissione atti |
| UC-T22 | Stralcio del procedimento |
| UC-T23 | Generazione statistiche |
| UC-T24 | Gestione riferimenti SIEP (RIFASIEP) |
| UC-T25 | Gestione riferimenti interni SIUS (RIFASIUS) |

**Totale: 25 casi d'uso**