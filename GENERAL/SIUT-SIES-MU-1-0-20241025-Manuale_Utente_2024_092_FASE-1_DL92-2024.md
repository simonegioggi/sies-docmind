---
uniqueName: siut-sies-mu-1-0-20241025-manualeutente2024092fase
displayName: "SIUT SIES MU 1 0 20241025 Manuale Utente 2024 092 FASE 1 DL92 2024"
category: "GENERAL"
tags: []
---

# SIUT-SIES-MU-1.0-20241025-Manuale_Utente_2024_092_FASE-1_DL92-2024

> **File originale:** `MEV/SCHEDA_092/SIUT-SIES-MU-1.0-20241025-Manuale_Utente_2024_092_FASE-1_DL92-2024.docx`  
> **Tipo:** DOCX

---

| Ministero della Giustizia
Dipartimento per l’innovazione tecnologica della giustizia
Direzione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |
|  |
|  |
|  |





Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.

Approvazioni
|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Engineering | RTI |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 25/10/2024 |  |
| Livello di riservatezza | L3 |  |


Elenco versioni
| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 1.0 | 25/10/2024 | Prima emissione |  |



Lista di distribuzione
| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Salvatore Piazza | RTI |  | Technical Manager |
| Sergio Tamburrini | RTI |  | Organization Manager |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Francesco Rosati | RTI |  | Responsabile Manutenzione Correttiva
Referente Qualità e Sicurezza |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Referente PMO e Qualità |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |
| Luigi Buglione | RTI |  | Referente Metrico |


INDICE DEI CONTENUTI
1.	Introduzione	5
1.1.	Scopo del documento	5
1.2.	Glossario	5
1.2.1.	Definizioni	5
1.2.2.	Acronimi e abbreviazioni	5
2.	Interventi su SIEP	6
2.1	Calcolo Pena DL 92/2024  (Calcolatrice Pena Ipotetica)	6

# Introduzione
## Scopo del documento
Nel documento sono descritti gli interventi realizzati nel sistema SIES, sottosistemi SIEP e SIUS, con lo scopo di soddisfare i requisiti espressi dall’Amministrazione in relazione alla richiesta di adeguamento normativo del Sistema, nella sua interezza, al DL 92/2024.

Il documento espone gli interventi attinenti alle funzioni previsti nel sistema in base alle novità normative del decreto DL 92/202, descritte nel documento SIUT-SIES-SC-1.0-20240917-Scheda_Intervento_2024_092-FASE-1_DL92-2024.pdf.
## Glossario
## Definizioni
Si premette un glossario esplicativo delle abbreviazioni e dei termini tecnici e giuridici utilizzati nel documento (Tabella - Glossario dei termini e degli acronimi usati nel documento).

| Definizione | Descrizione |
| --- | --- |
| ReGIndE | Registro Generale degli Indirizzi Elettronici |
| Portal Liferay | Liferay è un entreprise portal free e open Source |
| PDF | Portable Document Format – Standard per scambio documenti elettronici |
| P7M | Estensione file firmato con modalità CAdES, ovvero il documento firmato ed il file con la firma digitale vengono inseriti insieme in una busta. |
| PDF Firmato | Firma digitale apposta con modalità PAdES in cui vengono sfruttate le caratteristiche dei documenti in formato pdf. Il file contenente la firma digitale viene inglobato insieme al documento stesso. |
| Web-based | Un programma in cui tutte le funzioni sono accessibili tramite un normale web-browser come Firefox, Chrome o Explorer. Questo significa che non è necessario effettuare l’installazione di alcun software sui computer dell’azienda che deve utilizzare il programma. |


## Acronimi e abbreviazioni
| Sigla | Descrizione |
| --- | --- |
| GSU | Gestione Servizi UNEP |
| PDOC | Sistema Piattaforma Documentale |
| PEC | Posta Elettronica Certificata |
| PST | Portale dei Servizi Telematici |
| REGE | Registro Generale delle Notizie di Reato |
| RG | Registro Generale |
| SNT | Sistema Notifiche Telematiche |
| UNEP | Ufficio Notificazioni Esecuzioni Protesti |
| XML | eXtensible Markup Language |



Interventi su SIEP
L’esigenza principale richiesta dagli uffici nella fase di gestione dei nuovi procedimenti è di poter calcolare i semestri e i relativi n.ro di giorni di liberazione anticipata usufruibili dal condannato e quindi arrivare al calcolo della pena ipotetica da espiare, se il soggetto aderisce alle opere di rieducazione stabilite dalla Sorveglianza.
2.1	Calcolo Pena DL 92/2024  (Calcolatrice Pena Ipotetica)
La funzione permette di calcolare per un procedimento SIEP, in base ai dati presenti nella base dati, il numero di giorni di liberazione anticipata concedibili sui quantum di pena di presofferto e sui quantum di pena da espiare, pervenendo alla cosiddetta pena ipotetica ad esito delle detrazioni dei soli giorni di liberazione anticipata detraibili.
La funzione può essere utilizzata anche senza avere corrente nel sistema alcun procedimento corrente, impostando manualmente  i dati relativi al presofferto e alla pena da espiare.

La funzione può essere attivata, selezionando una nuova icona, che è stata aggiunta nel menu delle azioni veloci



Selezionandola si riceverà una delle seguenti form:
nel caso che non sia stato selezionato alcun procedimento SIEP





in caso di fascicolo presente in sessione


In cui sono riportati i dati di sintesi del procedimento, la pena da espiare ed il presofferto secondo i dati presenti nella base dati.
Questi dati possono essere verificati anche utilizzando la funzione, preesistente, Dettaglio Pena



I campi presenti nella form di Calcolo Pena DL 92/2024 sono in entrambi i casi modificabili dall’utente.
Dopo aver verificato i dati estratti dalla base dati o digitati dall’utente, a seguito della Conferma, il sistema effettua i seguenti calcoli:
- per il presofferto, il numero di giorni di L.A. usufruibili, il numero di semestri utili, il numero di giorni di custodia cautelare eccedenti il numero di semestri utili da poter conteggiare sulla pena da espiare;
- per la pena da espiare, il numero di semestri utili di pena ipotetica per l’erogazione della liberazione anticipata, giorni di liberazione anticipata maturata e usufruibili;
- Dati da indicare  nel provvedimento di esecuzione, pena ipotetica ottenuta applicando le detrazioni (Anni, Mesi e Giorni), numero di semestri scontati, giorni di l.a. concedibili, giorni di l.a. usufruibili
- Calcoli con data di esecuzione (solo se risulta valorizzata la data di Decorrenza nella prima parte della form (in caso di soggetto detenuto)), data decorrenza pena, data scarcerazione senza l.a., data scarcerazione con l.a. applicata (data fine pena con fungibilità), data scarcerazione con l.a. concessi (data fine pena senza fungibilità), data scarcerazione senza applicare l’ultima semestre (in caso di credito l.a.).
E presenta una delle seguenti form:
Soggetto Libero


Soggetto Detenuto
La form differisce dalla precedente nella parte evidenziata con il riquadro in rosso

Al termine della fase di elaborazione sarà possibile, selezionando l’icona  ,  richiedere la generazione del file Excel, contenente i dati riportati a video, per eventuali verifiche da parte dell’ufficio.
Il file contiene tre fogli:
Riepilogo


Libero

Detenuto (es. di soggetto detenuto con indicazione della data decorrenza)

Sempre al termine della fase di elaborazione sarà possibile, selezionando l’icona  ,  richiedere la stampa di un template, che in base alla posizione giuridica impostata nella prima form, sarà libero o detenuto, il cui contenuto sarà specificato dall’Amministrazione e che dovrebbe essere utilizzato per integrare gli attuali provvedimenti, prodotti da SIEP, in cui è necessario specificare la pena ipotetica ad esito delle detrazioni usufruibili.



Al momento sono previsti i seguenti template:

Per soggetto libero (SIEP_DL92-24_LIB.rtf)













Per soggetto detenuto (SIEP_DL92-24_DET.rtf)