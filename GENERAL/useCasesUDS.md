---
uniqueName: usecasesuds
displayName: "useCasesUDS"
category: "GENERAL"
tags: []
---

# Casi d'uso – SIUS – Ufficio / Magistrato di Sorveglianza (UDS / UDSM)

**Sottosistema:** SIUS (Sistema Informativo Unico per la Sorveglianza)  
**Attore:** Ufficio di Sorveglianza adulti (**UDS**) e Ufficio di Sorveglianza Minorenni (**UDSM**) / Magistrato di Sorveglianza  
**Tipo organo:** Monocratico (1 magistrato)  
**Tipo provvedimento principale:** Ordinanza

---

## UC-U01 – Iscrizione fascicolo SIUS da procedimento SIEP (UDS)

**Precondizione:** Esiste un procedimento SIEP (es. istanza di misura alternativa) trasmesso all'UDS.  
**Flusso:** L'utente UDS ricerca il fascicolo SIEP di origine → verifica i mittenti validi (TDS, TDSM, UDS, UDSM, PM, PGCAP per gli arresti domiciliari) → inserisce i dati del generale procedimento → registra i tenori → crea il fascicolo SIUS.  
**Postcondizione:** Fascicolo SIUS creato e assegnato all'ufficio UDS, stato "aperto".

---

## UC-U02 – Iscrizione fascicolo SIUS in modalità manuale (UDS)

**Precondizione:** Non esiste un fascicolo SIEP collegabile (es. procedimento originato localmente).  
**Flusso:** L'utente UDS compila manualmente tutti i campi del fascicolo e del generale procedimento.  
**Postcondizione:** Fascicolo SIUS manuale creato.

---

## UC-U03 – Presa in carico del procedimento

**Precondizione:** Fascicolo SIUS appena iscritto o trasmesso da altro ufficio.  
**Flusso:** L'utente conferma la presa in carico → il sistema registra data e ufficio di presa in carico.  
**Postcondizione:** Presa in carico formalizzata.

---

## UC-U04 – Assegnazione cancelleria assegnataria

**Precondizione:** Fascicolo SIUS aperto.  
**Flusso:** L'utente indica la cancelleria (sezione) assegnataria del fascicolo.  
**Postcondizione:** Cancelleria assegnataria registrata.

---

## UC-U05 – Cancellazione assegnazione fascicolo

**Precondizione:** Assegnazione errata della cancelleria.  
**Flusso:** L'utente annulla l'assegnazione precedente.  
**Postcondizione:** Assegnazione cancellata.

---

## UC-U06 – Fissazione udienza monocratica

**Precondizione:** Fascicolo SIUS aperto; il magistrato decide di fissare un'udienza.  
**Flusso:** L'utente UDS fissa l'udienza (data, ora, aula, procedimenti da trattare).  
**Postcondizione:** Udienza monocratica schedulata.

---

## UC-U07 – Modifica/cancellazione udienza monocratica

**Precondizione:** Udienza fissata, non ancora tenuta.  
**Flusso:** L'utente modifica data/ora/aula o cancella l'udienza.  
**Postcondizione:** Udienza aggiornata/cancellata.

---

## UC-U08 – Redazione verbale udienza monocratica

**Precondizione:** Udienza tenuta.  
**Flusso:** L'utente inserisce il verbale (presenze, dichiarazioni, decisioni del magistrato).  
**Postcondizione:** Verbale registrato.

---

## UC-U09 – Rinvio udienza con ordinanza di rinvio

**Precondizione:** Udienza monocratica in corso; necessità di rinvio.  
**Flusso:** L'utente emette ordinanza di rinvio → indica la nuova data.  
**Postcondizione:** Udienza rinviata.

---

## UC-U10 – Emissione ordinanza di concessione misura alternativa

**Precondizione:** Istruttoria completata; il magistrato decide di concedere la misura.  
**Flusso:** L'utente seleziona il tipo ordinanza (es. "Concessione affidamento in prova", "Detenzione domiciliare", "Semi-libertà") → compila i dati → deposita l'ordinanza.  
**Postcondizione:** Ordinanza di concessione depositata, misura alternativa attiva.

---

## UC-U11 – Emissione ordinanza di conversione pena pecuniaria

**Precondizione:** Condannato inadempiente al pagamento della pena pecuniaria.  
**Flusso:** Tipo ordinanza "Conversione" → dati della pena pecuniaria → calcolo rateizzazione o conversione in libertà controllata/lavoro → deposito.  
**Postcondizione:** Ordinanza di conversione depositata.

---

## UC-U12 – Emissione ordinanza di revoca conversione pena pecuniaria sostitutiva

**Precondizione:** Conversione di pena pecuniaria sostitutiva in corso; sopravviene causa di revoca.  
**Flusso:** Tipo ordinanza "Revoca conversione PPS" → motivazione → deposito.  
**Postcondizione:** Revoca conversione PPS depositata.

---

## UC-U13 – Emissione ordinanza di liberazione anticipata

**Precondizione:** Soggetto che ha maturato i presupposti per la liberazione anticipata.  
**Flusso:** Tipo ordinanza "Liberazione Anticipata" → calcolo detrazione giorni → deposito.  
**Postcondizione:** Ordinanza di liberazione anticipata depositata, giorni detratti dal residuo pena.

---

## UC-U14 – Emissione ordinanza di revoca misura alternativa

**Precondizione:** Misura alternativa in corso; sopravviene causa di revoca (violazione prescrizioni).  
**Flusso:** Tipo ordinanza "Revoca misura alternativa" → motivazione → deposito.  
**Postcondizione:** Misura revocata, soggetto rientra in esecuzione ordinaria.

---

## UC-U15 – Emissione ordinanza di sospensione misura di sicurezza

**Precondizione:** Misura di sicurezza in corso di esecuzione.  
**Flusso:** L'utente registra la sospensione → indica motivazione (01=Inizio, 02=Ripresa, 03=Sospensione), durata sospensione (gg/mm/aa), tipo ufficio sospendente.  
**Postcondizione:** Periodo di sospensione registrato sull'esecuzione misura di sicurezza.

---

## UC-U16 – Emissione ordinanza di estensione misura alternativa

**Precondizione:** Misura alternativa in corso; necessità di estenderne il periodo.  
**Flusso:** Tipo ordinanza "Estensione" → nuovi termini → deposito.  
**Postcondizione:** Ordinanza di estensione depositata, periodo misura aggiornato.

---

## UC-U17 – Emissione ordinanza di remissione del debito

**Precondizione:** Condannato a pena pecuniaria con impossibilità di pagamento certificata.  
**Flusso:** L'utente compila la richiesta di remissione → il sistema verifica le condizioni → deposita il provvedimento di remissione debito.  
**Postcondizione:** Remissione debito registrata.

---

## UC-U18 – Annullamento di un'ordinanza

**Precondizione:** Ordinanza precedentemente emessa.  
**Flusso:** L'utente seleziona l'ordinanza → verifica l'esistenza di un Foglio Complementare trasmesso → inserisce la motivazione dell'annullamento → il sistema aggiorna l'evento (con nota o nota su FC).  
**Postcondizione:** Ordinanza annullata.

---

## UC-U19 – Validazione inizio esecuzione misura di sicurezza

**Precondizione:** Misura di sicurezza disposta; soggetto pronto all'esecuzione.  
**Flusso:** L'utente avvia la procedura di validazione inizio → verifica condizioni (pena residua, stato fascicolo) → conferma l'inizio dell'esecuzione.  
**Postcondizione:** Esecuzione misura di sicurezza avviata e validata.

---

## UC-U20 – Inserimento/modifica periodo esecuzione misura di sicurezza

**Precondizione:** Misura di sicurezza in esecuzione.  
**Flusso:** L'utente inserisce o modifica un periodo di esecuzione (date, istituto di detenzione, motivazione).  
**Postcondizione:** Periodo esecuzione aggiornato.

---

## UC-U21 – Inserimento/modifica esecuzione misura alternativa

**Precondizione:** Misura alternativa concessa.  
**Flusso:** L'utente registra l'inizio/aggiornamento dell'esecuzione della misura alternativa (date, luogo, autorità esecutrice, motivazione).  
**Postcondizione:** Esecuzione misura alternativa registrata/aggiornata.

---

## UC-U22 – Inserimento/modifica esecuzione sanzione sostitutiva

**Precondizione:** Sanzione sostitutiva concessa.  
**Flusso:** L'utente registra i periodi di esecuzione della sanzione sostitutiva.  
**Postcondizione:** Esecuzione sanzione sostitutiva registrata.

---

## UC-U23 – Gestione permessi

**Precondizione:** Soggetto in esecuzione pena; richiesta di permesso.  
**Flusso:** L'utente registra il permesso (tipo, date, condizioni, esito).  
**Postcondizione:** Permesso registrato.

---

## UC-U24 – Gestione prescrizione

**Precondizione:** Titolo esecutivo con possibile prescrizione del reato/pena.  
**Flusso:** L'utente registra o aggiorna i dati di prescrizione (data scadenza, esito).  
**Postcondizione:** Prescrizione gestita.

---

## UC-U25 – Modifica titolo esecutivo / riferimento SIEP

**Precondizione:** Fascicolo SIUS con titolo esecutivo da aggiornare.  
**Flusso:** L'utente modifica il collegamento al procedimento SIEP o aggiorna i dati del soggetto.  
**Postcondizione:** Titolo esecutivo aggiornato.

---

## UC-U26 – Richiesta atti ad altro ufficio/istituto

**Precondizione:** Necessità di acquisire documentazione da uffici esterni.  
**Flusso:** L'utente registra la richiesta atti (destinatario, tipo atti, data richiesta) → il sistema traccia lo stato della richiesta.  
**Postcondizione:** Richiesta atti registrata e monitorata.

---

## UC-U27 – Richiesta atti per misure di sicurezza

**Precondizione:** Procedimento di misura di sicurezza; necessità di acquisire perizie/documentazione medica.  
**Flusso:** Variante specializzata di UC-U26 per le misure di sicurezza (tipo richiesta specifico, destinatari specializzati).  
**Postcondizione:** Richiesta atti specifica per misura di sicurezza registrata.

---

## UC-U28 – Gestione curatore per soggetti minorenni (UDSM)

**Precondizione:** Soggetto minorenne; necessità di nominare un curatore.  
**Flusso:** L'utente UDSM nomina/aggiorna il curatore del minore (dati anagrafici, ruolo).  
**Postcondizione:** Curatore registrato sul fascicolo minorenne.

---

## UC-U29 – Gestione avvocato difensore

**Precondizione:** Fascicolo SIUS aperto.  
**Flusso:** L'utente registra o aggiorna l'avvocato difensore del soggetto.  
**Postcondizione:** Avvocato registrato.

---

## UC-U30 – Gestione avvocatura (ufficio legale)

**Precondizione:** Fascicolo con rappresentanza dell'avvocatura dello Stato o ente.  
**Flusso:** L'utente registra l'avvocatura assegnata al fascicolo.  
**Postcondizione:** Avvocatura registrata.

---

## UC-U31 – Gestione esperti (criminologi, psicologi, ecc.)

**Precondizione:** Necessità di perizia o relazione specialistica.  
**Flusso:** L'utente nomina un esperto → registra i dati (tipo, periodo incarico, esito).  
**Postcondizione:** Esperto registrato.

---

## UC-U32 – Gestione collaboratori

**Precondizione:** Fascicolo con figure accessorie (assistenti sociali, ecc.).  
**Flusso:** L'utente registra i collaboratori coinvolti nel fascicolo.  
**Postcondizione:** Collaboratori registrati.

---

## UC-U33 – Inserimento motivazione provvedimento

**Precondizione:** Provvedimento emesso senza motivazione contestuale.  
**Flusso:** L'utente aggiunge o integra la motivazione del provvedimento.  
**Postcondizione:** Motivazione registrata.

---

## UC-U34 – Gestione notifiche su provvedimento

**Precondizione:** Provvedimento emesso; necessità di notifica alle parti.  
**Flusso:** L'utente registra le notifiche effettuate (destinatario, data, modalità).  
**Postcondizione:** Notifiche registrate sull'evento.

---

## UC-U35 – Inserimento/gestione Foglio Complementare

**Precondizione:** Provvedimento già trasmesso che richiede integrazioni.  
**Flusso:** L'utente inserisce il Foglio Complementare al provvedimento → il sistema lo collega all'evento originale.  
**Postcondizione:** Foglio Complementare registrato e trasmesso.

---

## UC-U36 – Annullamento Foglio Complementare

**Precondizione:** Foglio Complementare già inserito.  
**Flusso:** L'utente annulla il Foglio Complementare → il sistema aggiorna lo stato dell'evento.  
**Postcondizione:** Foglio Complementare annullato.

---

## UC-U37 – Trasmissione ordinanza ad altro ufficio

**Precondizione:** Ordinanza emessa dall'UDS.  
**Flusso:** L'utente avvia la trasmissione → indica l'ufficio destinatario → conferma.  
**Postcondizione:** Ordinanza trasmessa.

---

## UC-U38 – Registrazione impugnazione contro ordinanza

**Precondizione:** Ordinanza emessa; la parte propone impugnazione.  
**Flusso:** L'utente registra il tipo e la data dell'impugnazione.  
**Postcondizione:** Impugnazione registrata.

---

## UC-U39 – Registrazione luogo di detenzione

**Precondizione:** Soggetto detenuto con cambio istituto.  
**Flusso:** L'utente aggiorna il luogo di detenzione del soggetto (istituto, data ingresso).  
**Postcondizione:** Luogo di detenzione aggiornato.

---

## UC-U40 – Gestione scadenzario (UDS)

**Precondizione:** Fascicolo con scadenze da monitorare (fine pena, termine misura).  
**Flusso:** L'utente visualizza e aggiorna le scadenze associate al fascicolo.  
**Postcondizione:** Scadenzario aggiornato.

---

## UC-U41 – Stralcio del procedimento (UDS)

**Precondizione:** Fascicolo con procedimento da concludere parzialmente.  
**Flusso:** L'utente registra lo stralcio (es. estrazione di un soggetto o titolo esecutivo).  
**Postcondizione:** Stralcio registrato.

---

## UC-U42 – Ricerca e consultazione fascicoli (UDS)

**Precondizione:** Utente UDS/UDSM autenticato.  
**Flusso:** L'utente filtra per criteri (soggetto, anno, numero, stato) → visualizza l'elenco → accede al dettaglio fascicolo.  
**Postcondizione:** Fascicolo visualizzato.

---

## UC-U43 – Stampa ordinanza / provvedimento

**Precondizione:** Ordinanza/provvedimento depositato.  
**Flusso:** L'utente seleziona il tipo di stampa (per tipo ordinanza) → il sistema genera il documento.  
**Postcondizione:** Documento stampato/esportato.

---

## UC-U44 – Generazione statistiche (UDS)

**Precondizione:** Utente UDS/UDSM con privilegi statistici.  
**Flusso:** L'utente imposta i parametri (periodo, tipo misura, esiti) → il sistema genera il report.  
**Postcondizione:** Report statistico prodotto.

---

## UC-U45 – Gestione ulteriore istanza

**Precondizione:** Procedimento giunto all'ultima fase; presentazione di ulteriore istanza.  
**Flusso:** L'utente registra l'ulteriore istanza → collega i soggetti coinvolti (tenori dell'ulteriore istanza).  
**Postcondizione:** Ulteriore istanza registrata con i relativi tenori.

---

## UC-U46 – Produzione e trasmissione atti (UDS)

**Precondizione:** Necessità di produrre/trasmettere atti processuali.  
**Flusso:** L'utente registra la produzione → avvia la trasmissione verso ufficio destinatario.  
**Postcondizione:** Produzione/trasmissione registrata.

---

## Riepilogo

| Codice | Titolo |
|--------|--------|
| UC-U01 | Iscrizione fascicolo SIUS da procedimento SIEP (UDS) |
| UC-U02 | Iscrizione fascicolo SIUS in modalità manuale (UDS) |
| UC-U03 | Presa in carico del procedimento |
| UC-U04 | Assegnazione cancelleria assegnataria |
| UC-U05 | Cancellazione assegnazione fascicolo |
| UC-U06 | Fissazione udienza monocratica |
| UC-U07 | Modifica/cancellazione udienza monocratica |
| UC-U08 | Redazione verbale udienza monocratica |
| UC-U09 | Rinvio udienza con ordinanza di rinvio |
| UC-U10 | Emissione ordinanza di concessione misura alternativa |
| UC-U11 | Emissione ordinanza di conversione pena pecuniaria |
| UC-U12 | Emissione ordinanza di revoca conversione PPS |
| UC-U13 | Emissione ordinanza di liberazione anticipata |
| UC-U14 | Emissione ordinanza di revoca misura alternativa |
| UC-U15 | Emissione ordinanza di sospensione misura di sicurezza |
| UC-U16 | Emissione ordinanza di estensione misura alternativa |
| UC-U17 | Emissione ordinanza di remissione del debito |
| UC-U18 | Annullamento di un'ordinanza |
| UC-U19 | Validazione inizio esecuzione misura di sicurezza |
| UC-U20 | Inserimento/modifica periodo esecuzione misura di sicurezza |
| UC-U21 | Inserimento/modifica esecuzione misura alternativa |
| UC-U22 | Inserimento/modifica esecuzione sanzione sostitutiva |
| UC-U23 | Gestione permessi |
| UC-U24 | Gestione prescrizione |
| UC-U25 | Modifica titolo esecutivo / riferimento SIEP |
| UC-U26 | Richiesta atti ad altro ufficio/istituto |
| UC-U27 | Richiesta atti per misure di sicurezza |
| UC-U28 | Gestione curatore per soggetti minorenni (UDSM) |
| UC-U29 | Gestione avvocato difensore |
| UC-U30 | Gestione avvocatura (ufficio legale) |
| UC-U31 | Gestione esperti |
| UC-U32 | Gestione collaboratori |
| UC-U33 | Inserimento motivazione provvedimento |
| UC-U34 | Gestione notifiche su provvedimento |
| UC-U35 | Inserimento/gestione Foglio Complementare |
| UC-U36 | Annullamento Foglio Complementare |
| UC-U37 | Trasmissione ordinanza ad altro ufficio |
| UC-U38 | Registrazione impugnazione contro ordinanza |
| UC-U39 | Registrazione luogo di detenzione |
| UC-U40 | Gestione scadenzario (UDS) |
| UC-U41 | Stralcio del procedimento (UDS) |
| UC-U42 | Ricerca e consultazione fascicoli (UDS) |
| UC-U43 | Stampa ordinanza / provvedimento |
| UC-U44 | Generazione statistiche (UDS) |
| UC-U45 | Gestione ulteriore istanza |
| UC-U46 | Produzione e trasmissione atti (UDS) |

**Totale: 46 casi d'uso**