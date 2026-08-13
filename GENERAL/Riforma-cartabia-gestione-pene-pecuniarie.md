---
uniqueName: riforma-cartabia-gestione-pene-pecuniarie
displayName: "Riforma cartabia gestione pene pecuniarie"
category: "GENERAL"
tags: []
---

# Riforma cartabia gestione pene pecuniarie

> **File originale:** `MEV/SCHEDA_013/Docs/Test/Riforma cartabia gestione pene pecuniarie.docx`  
> **Tipo:** DOCX

---


Ministero della Giustizia
Gruppo di lavoro esecuzione e sorveglianza


S.I.E.P.

SISTEMA INFORMATIVO  ESECUZIONE PENALE
riforma cartabia
gestione pene pecuniarie


|  |  |
| --- | --- |
|  |  |



SOMMARIO


1	Sanzioni sostitutive delle pene detentive brevi	3
2	Iscrizione procedimenti	4
2.1	Iscrizione in classe I	4
2.2	Iscrizione in classe II	4
2.3	Iscrizione in classe VI	4
3	Gestione Pene pecuniarie	5
3.1	Maschera Siep per iscrizione delle sanzioni	5
4	Aannotazione tipologie di pagamento	7
4.1	Pagamento in Unica Soluzione	7
4.2	Pagamento rateale	7
4.3	Iscrizione Civilmente obbligato	7
5	Gestione  riscossione delle pene pecuniarie	9
5.1	Creazione dello scadenziario per determinare i termini di pagamento	9
5.2	Unica rata:	9
5.3	pagamento in rate mensili	9
6	Gestione pene pecuniarie	10
6.1	Emissione Ordine di Ingiunzione al Pagamento	10
7	“Gestione Notifiche” Autorità delegate alla notifica per ogni attore coinvolto	11
7.1	Notifica condannato	11
7.2	Notifica Difensore	11
7.3	Persona civilmente obbligata (se presente)	11
7.4	Richiesta informazioni	11
7.5	Rinnovo Ricerche per Omesse Notifiche	12
8	Gestione scadenziario	13
8.1	Consultazione e verifica scadenze notifiche.	13
8.2	pagamento Unica soluzione	13
8.3	Pagamento in rate mensili	13
8.3.1	Mancato pagamento di una delle rate	13
9	Gestione del procedimento di avvenuto/mancato pagamen	15
9.1	Accertato pagamento della pena pecuniaria	15
9.2	mancato pagamento della pena pecuniaria	15
9.3	trasmissione  atti al magistrato di sorveglianza	15
10	Decisioni magistratura di Sorveglianza	16
10.1	Annotazione differimento della conversione	16
10.2	Comunicazione ordine di pagamento al civilmente obbligato	16
10.3	Conversione delle pene pecuniarie in sanzione Sostitutive detentive brevi	17


# Sanzioni sostitutive delle pene detentive brevi
criteri per l'applicazione delle sanzioni sostitutive
Fino a 1 anno > Pena pecuniaria della specie corrispondente
La pena pecuniaria sostitutiva può essere applicata dal giudice in caso di condanna alla reclusione o
all’arresto non superiori a un anno.
Fino a 3 anni
> Lavoro di pubblica utilità (se il condannato non si oppone) la durata corrispondente alla pena sostituita
Il lavoro di pubblica utilità sostitutivo può essere applicato dal giudice in caso di condanna alla
reclusione o all’arresto non superiori a tre anni.
Fino a 4  anni
> Detenzione domiciliare sostitutiva
> Semilibertà sostitutiva
La semilibertà sostitutiva e la detenzione domiciliare sostitutiva possono essere applicate dal
giudice in caso di condanna alla reclusione o all’arresto non superiori a quattro anni.
# Iscrizione procedimenti
Per gestire le pene pecuniarie ordinarie e sostitutive, dopo la riforma Cartabia, proporrei di iscrivere il procedimento nella classe di riferimento.
## Iscrizione in classe I
Nel caso in cui il medesimo titolo esecutivo riporti condanna a pena detentiva congiuntamente pecuniaria si iscriverà il procedimento in classe prima, comprese le sanzioni sostitutive brevi  congiunte a pena pecuniaria
## Iscrizione in classe II
Nel caso in cui il medesimo titolo esecutivo riporti condanna a sola pena pecuniaria si iscriverà il procedimento in classe seconda,  compresa La pena pecuniaria sostitutiva
anche sostitutiva del
## Iscrizione in classe VI
Tutte le sanzioni di competenza del giudice di pace, anche se emesse da altro giudice
Tutti gli atti di esecuzione si dovranno gestire nella classe di iscrizione e per gestire la fase di recupero della pena pecuniaria si creerà una gestione parallela, creando un’apposita sezione sul modello già esistente in classe VII, che permetta di gestire tutte le fasi del recupero della sanzione pecuniaria.
# Gestione Pene pecuniarie
Quantificazione e determinazione sanzioni detentive brevi
Per gestire nuove sanzioni va creata una nuova maschere per l’iscrizione della pena. Come modello di iscrizione va presa la nuova maschera creata nella gestione cumulo adattandola e integrandola per le nuove esigenze:
## Maschera Siep per iscrizione delle sanzioni
la maschera per il caricamento delle pene detentive rimane quella attuale.

Per poter quantificare correttamente la quantificazione delle sanzioni sostitutive va creata una maschera intermedia, sul modello del casellario, che permetta all’operatore di poter indicare quale il
quantitativo di pena che si sostituisce:
| Indicare la pena detentiva sostituta | Indicare la pena detentiva sostituta | Indicare la pena detentiva sostituta | Indicare la pena detentiva sostituta |
| --- | --- | --- | --- |
| Reclusione | []  Intera pena | Oppure | Anni:  ___  Mesi:  ___  Giorni :___ |
| Arresto | []  Intera pena | Oppure | Anni:  ___  Mesi:  ___  Giorni :___ |
| Multa | []  Intera pena | Oppure | Euro: ______ |
| Ammenda | []  Intera pena | Oppure | Euro:_______ |

Va creata una nuova sezione denominata “Pene Sostitutive Delle Pene Detentive Brevi” che contenga   seguenti valori:
Maschera quantificazione delle Sanzioni detentive brevi (creare tabella si quantificazione in automatico)
| Sanzioni sostitutive delle pene detentive brevi | Sanzioni sostitutive delle pene detentive brevi | Sanzioni sostitutive delle pene detentive brevi | Sanzioni sostitutive delle pene detentive brevi | Sanzioni sostitutive delle pene detentive brevi | Sanzioni sostitutive delle pene detentive brevi | Sanzioni sostitutive delle pene detentive brevi | Sanzioni sostitutive delle pene detentive brevi | Sanzioni sostitutive delle pene detentive brevi |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Semilibertà Sostitutiva | Semilibertà Sostitutiva | Semilibertà Sostitutiva | Anni:  ___  Mesi:  ___  Giorni :___ | Anni:  ___  Mesi:  ___  Giorni :___ | Anni:  ___  Mesi:  ___  Giorni :___ | Anni:  ___  Mesi:  ___  Giorni :___ | Anni:  ___  Mesi:  ___  Giorni :___ | Anni:  ___  Mesi:  ___  Giorni :___ |  |
| detenzione domiciliare Sostitutiva | detenzione domiciliare Sostitutiva | detenzione domiciliare Sostitutiva | Anni:  ___  Mesi:  ___  Giorni :___ | Anni:  ___  Mesi:  ___  Giorni :___ | Anni:  ___  Mesi:  ___  Giorni :___ | Anni:  ___  Mesi:  ___  Giorni :___ | Anni:  ___  Mesi:  ___  Giorni :___ | Anni:  ___  Mesi:  ___  Giorni :___ |  |
| Pena Pecuniaria Sostitutiva | Pena Pecuniaria Sostitutiva | Pena Pecuniaria Sostitutiva | Multa: | Euro: _____ | Euro: _____ | Ammenda | Ammenda | Euro: _____ |  |
| lavoro Pubblica Utilità Sostitutivo | lavoro Pubblica Utilità Sostitutivo | lavoro Pubblica Utilità Sostitutivo | Anni  Mesi  Giorni | Anni  Mesi  Giorni | Anni  Mesi  Giorni | Anni  Mesi  Giorni | Anni  Mesi  Giorni | Anni  Mesi  Giorni |  |
| Modalità di Esecuzione Lavoro Pubblica Utilità | Modalità di Esecuzione Lavoro Pubblica Utilità | Modalità di Esecuzione Lavoro Pubblica Utilità | Modalità di Esecuzione Lavoro Pubblica Utilità | Modalità di Esecuzione Lavoro Pubblica Utilità | Modalità di Esecuzione Lavoro Pubblica Utilità | Modalità di Esecuzione Lavoro Pubblica Utilità | Modalità di Esecuzione Lavoro Pubblica Utilità | Modalità di Esecuzione Lavoro Pubblica Utilità |
| Ore di lavoro Settimanali da Svolgere:_______ | Ore di lavoro Settimanali da Svolgere:_______ | Frequenza Settimanale: ore____ | Frequenza Settimanale: ore____ | Frequenza Settimanale: ore____ | Frequenza Settimanale: ore____ | Frequenza Settimanale: ore____ | Frequenza Settimanale: ore____ | Frequenza Settimanale: ore____ |
| Ore di lavoro Settimanali da Svolgere:_______ | Ore di lavoro Settimanali da Svolgere:_______ | [] Determinata ___ [] Non Determinata | [] Determinata ___ [] Non Determinata | [] Determinata ___ [] Non Determinata | [] Determinata ___ [] Non Determinata | [] Determinata ___ [] Non Determinata | [] Determinata ___ [] Non Determinata | [] Determinata ___ [] Non Determinata |
| Struttura designata per lo svolgimento del lavoro | Struttura designata per lo svolgimento del lavoro | Struttura designata per lo svolgimento del lavoro | Struttura designata per lo svolgimento del lavoro | Struttura designata per lo svolgimento del lavoro | Sede | Sede | Indirizzo | Indirizzo |
| Lavoro Pubblica Utilità (Codice Strada) | Lavoro Pubblica Utilità (Codice Strada) | Lavoro Pubblica Utilità (Codice Strada) | Lavoro Pubblica Utilità (Codice Strada) | Lavoro Pubblica Utilità (Codice Strada) | Lavoro Pubblica Utilità (Codice Strada) | Lavoro Pubblica Utilità (Codice Strada) | Lavoro Pubblica Utilità (Codice Strada) | Lavoro Pubblica Utilità (Codice Strada) |  |
| Lavoro Pubblica Utilità | Tipo: | Tipo: | Tipo: | Tipo: | Tipo: | Tipo: | Tipo: | Tipo: |  |
| Nella misura di: Anni: ___  Mesi:  ___  Giorni :___Pari ad ore ___  complessive ___ | Nella misura di: Anni: ___  Mesi:  ___  Giorni :___Pari ad ore ___  complessive ___ | Nella misura di: Anni: ___  Mesi:  ___  Giorni :___Pari ad ore ___  complessive ___ | Nella misura di: Anni: ___  Mesi:  ___  Giorni :___Pari ad ore ___  complessive ___ | Nella misura di: Anni: ___  Mesi:  ___  Giorni :___Pari ad ore ___  complessive ___ | Nella misura di: Anni: ___  Mesi:  ___  Giorni :___Pari ad ore ___  complessive ___ | Nella misura di: Anni: ___  Mesi:  ___  Giorni :___Pari ad ore ___  complessive ___ | Nella misura di: Anni: ___  Mesi:  ___  Giorni :___Pari ad ore ___  complessive ___ | Nella misura di: Anni: ___  Mesi:  ___  Giorni :___Pari ad ore ___  complessive ___ |  |
| Modalità di Esecuzione Lavoro Pubblica Utilità | Modalità di Esecuzione Lavoro Pubblica Utilità | Modalità di Esecuzione Lavoro Pubblica Utilità | Modalità di Esecuzione Lavoro Pubblica Utilità | Modalità di Esecuzione Lavoro Pubblica Utilità | Modalità di Esecuzione Lavoro Pubblica Utilità | Modalità di Esecuzione Lavoro Pubblica Utilità | Modalità di Esecuzione Lavoro Pubblica Utilità | Modalità di Esecuzione Lavoro Pubblica Utilità |  |
| Ore di lavoro Settimanali                   da Svolgere: _______ | Ore di lavoro Settimanali                   da Svolgere: _______ | Frequenza Settimanale: | Frequenza Settimanale: | Frequenza Settimanale: | Frequenza Settimanale: | Frequenza Settimanale: | Frequenza Settimanale: | Frequenza Settimanale: |  |
| Ore di lavoro Settimanali                   da Svolgere: _______ | Ore di lavoro Settimanali                   da Svolgere: _______ | [] Determinata ___ [] Non Determinata | [] Determinata ___ [] Non Determinata | [] Determinata ___ [] Non Determinata | [] Determinata ___ [] Non Determinata | [] Determinata ___ [] Non Determinata | [] Determinata ___ [] Non Determinata | [] Determinata ___ [] Non Determinata |  |
| Struttura designata per lo svolgimento del lavoro | Struttura designata per lo svolgimento del lavoro | Struttura designata per lo svolgimento del lavoro | Struttura designata per lo svolgimento del lavoro | Struttura designata per lo svolgimento del lavoro | Sede | Sede | Indirizzo | Indirizzo |  |

Tutta la gestione deve rispecchiare quella già prevista pel la gestione della pena detentiva











# Aannotazione tipologie di pagamento
Il sistema in presenza di una pena pecuniaria deve permettere di indicare le modalità di pagamento:
## Pagamento in Unica Soluzione
Dopo la quantificazione della sanzione il sistema deve permettere di annotale i termini di pagamento:
Pagamento rata entro gg 90 Pagamento e quantificare la scadenza.
## Pagamento rateale
Il sistema deve integrare al maschera per permettere l’annotazione del numero N °______ rate   mensili importo Rate  Euro:___/___ ed il termine di pagamento, entro GG____ dalla notifica dell’ingiunzione.
## Iscrizione Civilmente obbligato
deve permettere, nei casi dell’articolo 534 il caricamento dei dati del civilmente obbligato al pagamento della pena pecuniaria, può essere persona fisica o persona giuridica, il sistema SIGE è già presente la maschera di iscrizione, si riporta la tipologia di maschera:
Persona fisica:

Persona giuridica:



Integrazioni e opzioni
La maschera va integrata con gli indirizzi e-mail e Pec;
Va prevista l’annotazione del difensore;
Prevedere la notifica dell’ingiunzione di pagamento già al primo atto.
# Gestione  riscossione delle pene pecuniarie
## Creazione dello scadenziario per determinare i termini di pagamento
Per poter attivare lo scadenziario occorre prevedere la funzione (Notifica atti) per annotare le date di notifiche dell’atto, riportando tutti i soggetti coinvolti nelle notifiche.
## Unica rata:
Termini pagamento Unica soluzione (rata): giorni 90 giorni, dalla notifica dell’ingiunzione
Il sistema deve prevede lo scadenziario dei termini di pagamento.
Il termine va calcolato dalla data di notifica dell’ordine di ingiunzione.
Va poi prevista una scadenza intermedia per calcolare il termine per la presentazione ex art. 133 -  ter ovvero calcolare il termine di venti giorni, termine per il deposito dell’istanza di pagamento rateale della pena pecuniaria.

## pagamento in rate mensili
Dopo la notifica dell’ordine di ingiunzione al pagamento va calcolata  la scadenza della prima rata sul quantitativo di giorni indicato dal giudice (30) e la seconda rata, frequenza Mensile, deve tenere conto del fine  di ogni  mese  prendendo l'ultimo giorno utile (es giorno 28 29 30 il 31)
Nei casi dell’articolo 534, l’ordine di esecuzione è notificato altresì al civilmente obbligato per la pena pecuniaria. ( Può essere un soggetto o una persona giuridica)
# Gestione pene pecuniarie
Per poter gestire la nuova sanzione proporrei di creare una nuova voce “Gestione Pene Pecuniarie (legge 134/21Cartabia)” sul menu “Gestione Altre Sanzioni” o sul menu verticale
Menu esecuzione pene sostitutive brevi (d.lgs. n. 150/2022) Cartabia)
le voci per gestire la nuova procedura delle riscossioni delle pene pecuniarie, tenendo conto che molto probabilmente all’interno dell’uffici si creerà una sezione dedicata, vanno riportati nella specifica sessione:
## Emissione Ordine di Ingiunzione al Pagamento
La maschera di gestione va creata ed adeguata all’esecuzione della nuova sanzione riportando quanto determinato dal giudice nel provvedimento di condanna
Stato procedimento
Posizione giuridica
Proporrei di non adoperare le posizioni giuridiche di Siep ma di crearne delle nuove per semplificare la gestione:
Libero o in misura alternativa
Detenuto a qualsiasi titolo in istituto
Il sistema sceglie la modulistica in base alla tipologia di pagamento ed alla posizione giuridica del condannato.
Vanno bene definite i soggetti a cui va notificato l’atto:
Condannato e difensore
Civilmente obbligato e suo difensore (se presente)
Autorità delegate alla notifica:
Difensore Notifica SNT (creare oggetto sull’applicativo)
Condannato
Forze di polizia
Ufficiali giudiziari
Civilmente obbligato
Ufficiali giudiziari o pec
Difensore del (Notifica SNT)

Tutti soggetti coinvolti dovranno essere replicati nella sessione “Notifiche atti” e stabilire quali fanno scattare i termini di scadenza del pagamento delle rate.
# “Gestione Notifiche” Autorità delegate alla notifica per ogni attore coinvolto
Creare la gestione delle notifiche prevedendo, all’interno della funzione, un elenco delle attività svolte ( elenco ordini di ingiunzione emessi) con ampia visibilità delle scadenze delle notifiche e delle mancate notifiche.
Azionata la voce, il sistema visualizza tutti i soggetti a cui è stata inviata la notifica.
## Notifica condannato
Il sistema deve permettermi di annotare:
data di notifica
data di mancata notifica ed autorità
il sistema deve poter gestire la mancata notifica anche all’interno della funzione, richiamando la maschera di gestione attuale. Se la compilazione avviene dalla funzione “verbale Vane richieste” il sistema riporta in automatico il dato. Il sistema deve riportare l’autorità delegata alla notifica  all’atto dell’emissione del provvedimento. Con possibilità di indicarel’ “ Autorità che ha effettuato la notifica”
In base alla tipologia di pagamento il sistema deve attivare gli scadenziari:
## Notifica Difensore
Prevedere la data di annotazione
Modalità di notifica (replicata dalla maschera di emissione del provvedimento
Notifica ai sensi dell’art. 148 comma 2 c.p.p. 8
Opzioni
Posta elettronica certificata;
Sistema notifiche penali;
## Persona civilmente obbligata (se presente)
Nei casi dell’articolo 534, l’ordine di esecuzione è notificato altresì al civilmente obbligato, per la pena pecuniaria:
Prevedere la notifica con casella pec
Ufficiali giudiziari;
Posta elettronica certificata.
## Richiesta informazioni
Art. 5 art. 660
Quando e' provato o appare probabile che il condannato non abbia avuto effettiva conoscenza dell'ordine di esecuzione, il pubblico ministero puo' assumere, anche presso il difensore, le opportune informazioni, all'esito delle quali puo' disporre la rinnovazione della notifica.
La gestione è già presente nella gestione del decreto di sospensione si può replicare, mostrando         l’ elenco ordini di ingiunzione emessi a cui fa riferimento la richiesta.
Autorità:
Richiesta Informazioni al Difensore
Richiesta Informazioni ad altri
Rinnovo notifiche
Stessa gestione del decreto di sospensione
stessa autorità
altra autorità
## Rinnovo Ricerche per Omesse Notifiche
Manterrei la funzione in caso di contenuti che non soddisfano le ricerche effettuate.

# Gestione scadenziario
## Consultazione e verifica scadenze notifiche.
Dopo la notifica dell’ingiunzione al pagamento occorre creare diversi scadenziari, correlati tra loro.
Va creata un’efficace e chiara gestione delle scadenze per rendere fruibile il dato anche a livello di procedimento, vanno creati molteplici report in base alle scadenze (da concordare).
## pagamento Unica soluzione
Lo scadenziario si attiva dopo la conclusione dell’attività di notifica.
Dopo la notifica dell’ingiunzione va creato lo scadenzario che determini la data di scadenza del pagamento in un Unica soluzione
Va poi prevista una scadenza intermedia per calcolare il termine per la presentazione ex art. 133 -  ter ovvero calcolare il termine di venti giorni, termine per il deposito dell’istanza di pagamento rateale della pena pecuniaria.
Va creato un nuovo contenuto “Art. 133-ter. (Pagamento rateale della multa o dell'ammenda).
Istanza di pagamento rateale della pena pecuniaria (ex art. 133-ter c.p.)
Iscrizione istanza
La gestione dell’istanza va rivista, il sistema considera tutte le istanze riferite alle misure alternative, va normalizzata – va poi rivista la gestione della nomina del difensore, la maschera va richiamata con un tasto funzione e, una volta caricato l’avvocato lo deve caricare sul procedimento.
Il sistema, dopo l’annotazione dell’istanza, e la trasmissione degli atti al magistrato di sorveglianza competente, che procede ai sensi dell’articolo 667, comma 4, non va interrotto lo scadenziario????  Va lasciata  la nota di pagamento su pagoPA
Gestione
Provvedimenti del Pubblico Ministero
Va creata la funzione “trasmissione degli atti al Magistrato di sorveglianza”
Prevedere parere pm?

## Pagamento in rate mensili
Il sistema deve creare un prospetto riepilogativo dei pagamenti suddiviso in  rate:
n. rata - Data Scadenza – Importo - Stato Pagamento - Pagamento PagoPA
Dopo l’annotazione della data di pagamento della prima rata, calcolata dopo la notifica dell’ordine, il sistema elabora il prospetto scadenze delle successive rate, la quantificazione è già presente sull’applicativo, calcolare la seconda rata, con frequenza Mensile, nel conteggio delle scadenze successive si deve tenere conto del fine di ogni mese prendendo l'ultimo giorno utile (es giorno 28 29 30 il 31) va creato scadenziario scadenze rate. Trasmissione moduli pagamento??
Il sistema al pagamento delle rate deve calcolare il residuo della somma da pagare.
### Mancato pagamento di una delle rate
Il mancato pagamento, di una delle rate comporta la decadenza del beneficio del pagamento rateale, il sistema dopo l’annotazione del mancato pagamento deve calcolare la somma residua da pagare ed emette un nuovo provvedimento (ingiunzione) con l’obbligo di pagare la parte residua della somma in un’unica soluzione entro i 60 giorni successivi dalla notifica dell’ingiunzione. Scadenzario
Il pubblico ministero ricalcola la somma residua ho riemette un nuovo ordine con l’intera cifra
Gestione :
Emissione di un nuovo ordine di ingiunzione
Sostituzione  del pagamento su PagoPA con nuovo importo,?
Si ripete tutta la gestione

# Gestione del procedimento di avvenuto/mancato pagamento
La gestione è identica per i due modalità di pagamento
Alla scadenza del termine il pubblico ministero:
## Accertato pagamento della pena pecuniaria
Accertato l’avvenuto pagamento, il Pubblico Ministero
dichiara avvenuta l’esecuzione della pena
Redige il foglio complementare
Trasmette il foglio al casellario

## mancato pagamento della pena pecuniaria
Il mancato pagamento della pena pecuniaria, entro il termine indicato nell'ordine di esecuzione, il pubblico ministero trasmette gli atti al magistrato di sorveglianza
## trasmissione  atti al magistrato di sorveglianza
Trasmissione degli atti al Magistrato di sorveglianza.
Tutta questa fase va allineata ai provvedimenti emessi dalla magistratura di sorveglianza
Il procedimento per la conversione della pena pecuniaria, anche sostitutiva, è disciplinato dall’articolo 667, comma4. Per la conversione della pena pecuniaria, ai sensi degli articoli 71, 102 e 103 della legge 24 novembre 1981, n. 689, si applica, in quanto compatibile, l’articolo 545- bis, commi 2 e 3.
# Decisioni magistratura di Sorveglianza
Va gestito tutto il flusso compreso l’eventuale impugnazione delle decisione del Magistrato di sorveglianza.
## Annotazione differimento della conversione
10. Quando il mancato pagamento della pena pecuniaria è dovuto a insolvibilità, il condannato può chiedere al magistrato di sorveglianza il differimento della conversione per un tempo non superiore a sei mesi, rinnovabile per una sola volta se lo stato di insolvibilità perdura. Ai fini della estinzione della pena pecuniaria per decorso del tempo, non si tiene conto del periodo durante il quale la conversione è stata differita.
Prevedere scadenzari differimento conversione
Alla scadenza verificare se è stata presa decisione
Ed emettere provvedimenti appropriati.
## Comunicazione ordine di pagamento al civilmente obbligato
11. Se vi è stata condanna ai sensi dell’articolo 534, ed è accertata l’insolvibilità del condannato, il magistrato di sorveglianza ne dà comunicazione al pubblico ministero, il quale ordina al civilmente obbligato per la pena pecuniaria di provvedere al pagamento della multa o dell’ammenda entro il termine di cui al terzo comma, ovvero, in caso di pagamento rateale, entro il termine di cui al quarto comma. Qualora il civilmente obbligato per la pena pecuniaria non provveda al pagamento entro i termini stabiliti, il pubblico ministero ne dà comunicazione al magistrato di sorveglianza che provvede alla conversione della pena nei confronti del condannato.
Emissione ingiunzione di pagamento al civilmente obbligato
Creare opzione
Testo norma
Se vi è stata condanna ai sensi dell’articolo 534, ed è accertata l’insolvibilità del condannato, il magistrato di sorveglianza ne dà comunicazione al pubblico ministero, il quale ordina al civilmente obbligato per la pena pecuniaria di provvedere al pagamento della multa o dell’ammenda entro il termine di cui al terzo comma, ovvero, in caso di pagamento rateale, entro il termine di cui al quarto comma.
Annotazione Ordinanza
Il sistema deve prevedere la presa in carico dell’ordinanza/decreto ed emettere l’ordine di ingiunzione
I Termini e le scadenze dovrebbero essere quelle riportate in sentenza di condanna
Stralcio quarto comma art. 660
Emissione ordine di ingiunzione  - gestione notifiche
Con l’ordine di esecuzione il pubblico ministero ingiunge al condannato di pagare la prima rata entro trenta giorni dalla notifica del provvedimento, avvertendolo che in caso di mancato tempestivo pagamento della prima rata è prevista l’automatica decadenza dal beneficio e il pagamento della restante parte della pena in un’unica soluzione, da effettuarsi, a pena di conversione ai sensi del comma precedente, entro i sessanta giorni successivi.
Gestione pagamento rate
Attivare tutta la procedura prevista per l’esecuzione del pagamento delle rate, unica o rateale, riportato.
Esiti procedura di recupero
Pagamento avvenuto dichiarazione
Mancato pagamento.

## Conversione delle pene pecuniarie in sanzione Sostitutive detentive brevi
«Art. 103  (Mancato pagamento della pena pecuniaria per insolvibilità del condannato)
Quando le condizioni economiche e patrimoniali del condannato al momento dell’esecuzione rendono impossibile il pagamento della multa o dell’ammenda entro il termine di cui all’articolo 660 del codice di procedura penale, la pena pecuniaria è convertita nel lavoro di pubblica utilità sostitutivo ovvero, se il condannato si oppone, nella detenzione domiciliare sostitutiva.
Annotazione ordinanza da presa in carico
L’esecuzione delle pene determinate è di competenza, in caso di:
lavoro di pubblica utilità sostitutiva il giudice che ha emesso il provvedimento (Tribunale /Gip..)
detenzione domiciliare sostitutiva lo stesso magistrato di sorveglianza
Il sistema deve prevedere l’annotazione del provvedimento
Il ricorso contro l’ordinanza di conversione ne sospende l’esecuzione.
13. Il ricorso contro l’ordinanza di conversione ne sospende l’esecuzione.
Annotazione ordinanza da presa in carico
Annotazione esito
Dopo esito ricorso prevedere l’annotazione della decisione
Revoca pene sostitutive, conseguenti alla conversione della pena pecuniaria
15. Le pene sostitutive, conseguenti alla conversione della pena pecuniaria, sono immediatamente revocate dal magistrato di sorveglianza quando risulta che il condannato ha pagato la multa o l’ammenda, dedotta la somma corrispondente alla durata della pena da conversione espiata. Durante l’esecuzione, delle sanzioni sostitutive da conversione pene pecuniarie  il condannato può chiedere al magistrato di sorveglianza di essere ammesso al pagamento rateale, ai sensi dell’articolo 133- ter del codice penale. In tal caso, dopo il pagamento della prima rata l’esecuzione della pena da conversione è sospesa, e riprende in caso di mancato pagamento di una delle rate.
Occorre accertare se in questa specifica ipotesi la gestione rimane alla sorveglianza si





Esecuzione di pene sostitutive concorrenti (cumulo)
«Art. 70 (Esecuzione di pene sostitutive concorrenti). — Quando contro la stessa persona sono state pro- nunciate, per più reati, una o più sentenze o decreti penali di condanna a pena sostitutiva, si osservano, in quanto compatibili, le disposizioni degli articoli da 71 a 80 del codice penale.
Va creata tutta la gestione compresa il computo della custodia cautelare, il ragguaglio va fatto tenendo conto del criterio di conversione adoperato dal giudice in sentenza.
Se più reati importano pene sostitutive, anche di specie diversa, e il cumulo delle pene detentive sostituite non eccede complessivamente la durata di quattro anni, si applicano le singole pene sostitutive distintamente, anche oltre i limiti di cui all’articolo 53 per la pena pecuniaria e per il lavoro di pubblica utilità.
Se supera il limite
Se il cumulo delle pene detentive sostituite eccede complessivamente la durata di quattro anni, si applica per intero la pena sostituita, salvo che la pena residua da eseguire sia pari o inferiore ad anni quattro.
Le pene sostitutive sono sempre eseguite dopo le pene detentive e, nell’ordine, si eseguono la semilibertà, la detenzione domiciliare ed il lavoro di pubblica  utilità.
Per l’esecuzione delle pene sostitutive concorrenti si applica, in quanto compatibile, l’articolo 663 del codice di procedura penale. È tuttavia fatta salva, limitatamente all’esecuzione del lavoro di pubblica utilità, anche con- corrente con pene sostitutive di specie diversa, la competenza del giudice che ha applicato tale pena.»;
Creare Gestione Sanzioni Detentive Brevi
Va aggiornata, con particolare attenzione alle sanzioni pecuniarie, il sistema deve dare la possibilità di gestire la pena ed adeguare il provvedimento di cumulo creando le seguenti funzioni:
aggiornare tutte le maschere con le nuove sanzioni
adeguare tutti i conteggi della pena adeguandoli alla normativa, gestione separata.
nuova gestione delle pene pecuniarie ( dividendo la gestione vecchie e nuove)
Gestione della pene, Sezione “attività del PM”.









Computo della custodia cautelare e delle pene espia- te senza titolo
“Art. 657 (Computo della custodia cautelare e delle pene espia- te senza titolo). — 1. Il pubblico ministero, nel determinare la pena        detentiva da eseguire, computa il periodo di custodia cautelare subita per lo stesso o per altro reato, anche se la custodia è ancora in corso. Allo stesso modo procede in caso di applicazione provvisoria di una misura di sicurezza detentiva, se questa non è stata applicata definitivamente.
Il pubblico ministero computa altresì il periodo di pena detentiva espiata per un reato diverso, quando la relativa condanna è stata revocata, quando per il reato è stata concessa amnistia o quando è stato concesso indulto, nei limiti dello stesso.
Nei casi previsti dai commi 1 e 2, il condannato può chiedere al pubblico ministero o, in caso di condanna alla pena del lavoro di pubblica utilità sostitutivo, al giudice che i periodi di custodia caute- lare e di pena detentiva espiata, operato il ragguaglio, siano computati per la determinazione della pena pecuniaria o della pena sostitutiva da eseguire; nei casi previsti dal comma 2,
può altresì chiedere che le pene sostitutive espiate siano computate nelle pene sostitutive da eseguire per altro reato.
In ogni caso sono computate soltanto la custodia cautelare subita o le pene espiate dopo la commissione del reato per il quale deve essere determinata la pena da eseguire.
Il pubblico ministero provvede con decreto, che deve essere notificato al condannato e al suo difensore.”
Gestione istanza
Per la gestione dell’ipotesi occorre prevedere la gestione dell’istanza presentata al Pubblico Ministero o
Giudice dell’esecuzione. Va prevista la gestione  in entrambi i casi


«Art. 64 (Modifica delle modalità di esecuzione delle pene sostitutive). — Le prescrizioni imposte con l’ordinanza prevista dall’articolo 62, su istanza del con- dannato da inoltrare tramite l’ufficio di esecuzione penale esterna, possono essere modificate per comprovati motivi dal magistrato di sorveglianza, che procede nelle forme dell’articolo 678, comma 1-bis, del codice di procedura penale.
Le prescrizioni imposte con la sentenza che appli- ca il lavoro di pubblica utilità, su istanza del condannato da inoltrare tramite l’ufficio di esecuzione penale esterna, possono essere modificate per comprovati motivi dal giudice che ha applicato la pena sostitutiva, il quale prov- vede a norma dell’articolo 667, comma 4, del codice di procedura penale.
I provvedimenti di cui al primo e al secondo com- ma sono immediatamente trasmessi all’ufficio di esecu- zione penale esterna, all’organo di polizia o al direttore dell’istituto competenti per il controllo sull’adempimento delle prescrizioni.
Non possono essere modificate le prescrizioni di cui all’articolo 56-ter, primo comma, numeri 1, 2, 4 e 5.»;
o)	all’articolo 65:
1)	al primo comma, le parole: «la semidetenzione o la libertà controllata o» sono sostituite  dalle   seguenti:
«le pene sostitutive della semilibertà, della detenzione domiciliare o del lavoro di pubblica utilità ovvero»; la parola: «verifica» è sostituita dalle seguenti: «, e il nucleo di Polizia penitenziaria presso l’ufficio di esecuzione pe- nale esterna verificano» e la parola: «tiene» è sostituita dalla seguente: «tengono»;
2)	al secondo comma, le parole: «custoditi l’estrat- to della» sono sostituite dalle seguenti: «custodite la» e dopo la parola «condanna» il segno di interpunzione «,»  è sostituito dalle seguenti parole: «che applica il lavoro   di pubblica utilità  sostitutivo  ovvero» e dopo le   parole:
«modalità di esecuzione» sono inserite le seguenti: «della semilibertà sostitutiva o della detenzione domiciliare so- stitutiva»; nel secondo periodo, la parola: «semidetenzio- ne» è sostituita dalla seguente: «semilibertà» e le  parole:
«29 aprile 1976, n. 431» sono sostituite dalle seguenti:
«30 giugno 2000, n. 230»;
3)	nel terzo comma, le parole: «o della sezione ivi indicata» sono soppresse;
4)	nella rubrica, le parole: «imposte con la senten- za di condanna» sono soppresse;
p)	l’articolo 66 è sostituito dal seguente:
«Art. 66 (Revoca per inosservanza delle prescri zioni). — Salvo quanto previsto dall’articolo 71 per la pena pecuniaria, la mancata esecuzione della pena sosti- tutiva, ovvero la violazione grave o reiterata degli obbli- ghi e delle prescrizioni ad essa inerenti, ne determina la revoca e la parte residua si converte nella pena detentiva sostituita ovvero in altra pena sostitutiva più grave.
Gli ufficiali e gli agenti della polizia giudiziaria,  il direttore dell’istituto a cui il condannato è assegnato o il direttore dell’ufficio di esecuzione penale esterna infor- mano, senza indugio, il giudice che ha applicato il lavoro di pubblica utilità, ovvero il magistrato di sorveglianza che ha emesso l’ordinanza prevista dall’articolo 62, di ogni violazione degli adempimenti sui quali gli organi medesimi esercitano i rispettivi controlli.
Il magistrato di sorveglianza compie, ove occorra, sommari accertamenti e, qualora ritenga doversi disporre la revoca della semilibertà o della detenzione domicilia- re e la conversione previste dal primo comma, procede a norma dell’articolo 666 del codice di procedura penale. Allo stesso modo procede il giudice che ha applicato il lavoro di pubblica utilità.»;

q)	l’articolo 67 è sostituito dal seguente:
«Art. 67 (Inapplicabilità delle misure alternative alla detenzione). —  Salvo  quanto  previsto  dall’artico- lo 47, comma 3-ter, della legge 26 luglio 1975, n. 354,    le misure alternative alla detenzione di cui al capo VI del titolo I della medesima legge n. 354 del 1975, non si ap- plicano al condannato in espiazione di pena sostitutiva.
Salvo che si tratti di minori di età al momento della condanna, le misure di cui al primo comma non si applicano altresì, prima dell’avvenuta espiazione di metà della pena residua, al condannato in espiazione di pena detentiva per conversione effettuata ai sensi dell’artico-  lo 66 o del quarto comma dell’articolo 72.»;
r)	l’articolo 68 è sostituito dal seguente:
«Art. 68 (Sospensione dell’esecuzione delle pene sostitutive). — L’esecuzione della semilibertà sostitutiva, della detenzione domiciliare sostitutiva o del lavoro di pubblica utilità sostitutivo è sospesa in caso di notifica    di un ordine di carcerazione o di consegna; l’esecuzione  è altresì sospesa in caso di arresto o di fermo del condan- nato o di applicazione, anche provvisoria, di una misura  di sicurezza detentiva.
L’ordine di esecuzione della semilibertà sostituti- va, della detenzione domiciliare sostitutiva o del lavoro di pubblica utilità sostitutivo emesso nei confronti dell’im- putato detenuto o  internato  non  sospende  l’esecuzione di pene detentive o l’esecuzione, anche provvisoria, di misure di sicurezza detentive, né il corso della custodia cautelare.
Nei casi previsti dal primo comma, il giudice ov- vero il magistrato di sorveglianza determinano la durata residua della pena sostitutiva e trasmettono il provvedi- mento al direttore dell’istituto in cui si trova il condan- nato; questi informa anticipatamente l’organo  di  poli- zia della data in cui riprenderà l’esecuzione della pena sostitutiva.
La pena sostitutiva riprende a decorrere dal giorno successivo a quello della cessazione della esecuzione del- la pena detentiva ovvero dal secondo giorno successivo, in relazione alle necessità di viaggio e alle condizioni dei trasporti.»;

s)	l’articolo 69 è sostituito dal seguente:
«Art. 69 (Licenze ai condannati alla semilibertà e alla detenzione domiciliare. Sospensione e rinvio delle pene sostitutive). — Per giustificati motivi, attinenti alla salute, al lavoro, allo studio, alla formazione, alla fami- glia o alle relazioni affettive, al condannato alla pena so- stitutiva della semilibertà o della detenzione domiciliare possono essere concesse licenze per la durata necessaria e comunque non superiore nel complesso a quarantacinque giorni all’anno. Si applica il terzo comma dell’articolo 52 della legge 26 luglio 1975, n. 354. Al condannato che, allo scadere della licenza o dopo la revoca di essa, non rientra in istituto o nel luogo indicato nell’articolo 56, primo comma, è applicabile l’articolo 66, primo  comma.
Per gli stessi giustificati motivi di cui al primo comma ovvero per cause riconducibili all’attività dei soggetti di cui all’articolo 56-bis, la pena sostitutiva del lavoro di pubblica utilità può essere sospesa per un perio- do non superiore nel complesso a quarantacinque    giorni all’anno. Al condannato che, allo scadere della sospen- sione, non si presenta al lavoro è applicabile l’articolo 66 secondo comma.
Per il rinvio dell’esecuzione della pena sostitutiva della semilibertà o della detenzione domiciliare nei casi  di cui agli articoli 146 e 147 del codice penale si applica l’articolo 684 del codice di procedura penale. Al condan- nato alla semilibertà può essere applicata la pena sostitu- tiva della detenzione domiciliare, ove compatibile. In tal caso, l’esecuzione della pena prosegue durante la deten- zione domiciliare.
Quando le condizioni di cui agli articoli 146 e 147 del codice penale non sono compatibili con la prosecuzio- ne della prestazione lavorativa, il giudice che ha applicato il lavoro di pubblica utilità, nelle forme previste di cui all’articolo 666 del codice di procedura penale, dispone il rinvio dell’esecuzione della pena.
Nelle medesime forme di cui al terzo e al quarto comma si provvede quando occorre disporre la proroga del termine del rinvio dell’esecuzione.»;
t)	l’articolo 70 è sostituito dal seguente:
«Art. 70 (Esecuzione di pene sostitutive concor- renti). — Quando contro la stessa persona sono state pro- nunciate, per più reati, una o più sentenze o decreti penali di condanna a pena sostitutiva, si osservano, in quanto compatibili, le disposizioni degli articoli da 71 a 80 del codice penale.
Se più reati importano pene sostitutive, anche di specie diversa, e il cumulo delle pene detentive sostituite non eccede complessivamente la durata di quattro anni, si applicano le singole pene sostitutive distintamente, anche oltre i limiti di cui all’articolo 53 per la pena pecuniaria e per il lavoro di pubblica utilità.
Se il cumulo delle pene detentive sostituite ecce- de complessivamente la durata di quattro anni, si applica per intero la pena sostituita, salvo che la pena residua da eseguire sia pari o inferiore ad anni quattro.
Le pene sostitutive sono sempre eseguite dopo le pene detentive e, nell’ordine, si eseguono la semilibertà, la detenzione domiciliare ed il lavoro di pubblica  utilità.
Per l’esecuzione delle pene sostitutive concorrenti si applica, in quanto compatibile, l’articolo 663 del codice di procedura penale. È tuttavia fatta salva, limitatamente all’esecuzione del lavoro di pubblica utilità, anche con- corrente con pene sostitutive di specie diversa, la compe- tenza del giudice che ha applicato tale pena.»;
u)	l’articolo 71 è sostituito dal seguente:
«Art. 71 (Esecuzione della pena pecuniaria so- stitutiva. Revoca e conversione per mancato pagamento).
—	Alla pena pecuniaria sostitutiva della pena detentiva si applicano le disposizioni dell’articolo 660 del codice di procedura penale.
Il mancato pagamento della pena pecuniaria sosti- tutiva, entro il termine di cui all’articolo 660 del codice  di procedura penale indicato nell’ordine di esecuzione,   ne comporta la revoca e la conversione nella semiliber-   tà sostitutiva  o nella detenzione domiciliare sostitutiva.  Si applica l’articolo 58. Se è stato disposto il   pagamento rateale, il mancato pagamento di una rata, alla scadenza stabilita, comporta la revoca della pena pecuniaria sosti- tutiva e la conversione ha luogo per la parte  residua.
Quando le condizioni economiche e patrimoniali del condannato al momento dell’esecuzione rendono im- possibile il pagamento entro il termine indicato nell’ordi- ne di esecuzione, la pena pecuniaria sostitutiva è revocata e convertita nel lavoro di pubblica utilità sostitutivo o,   se il condannato si oppone, nella detenzione domiciliare sostitutiva. Si applicano le disposizioni del terzo periodo del secondo comma.»;
v)	l’articolo 72 è sostituito dal seguente:
«Art. 72 (Ipotesi di responsabilità penale e revo- ca). — Il condannato alla pena sostitutiva della semiliber- tà o della detenzione domiciliare che per più di dodici ore, senza giustificato motivo, rimane assente dall’istituto di pena ovvero si allontana da uno dei luoghi indicati nell’ar- ticolo 56 è punito ai sensi del primo comma dell’artico-  lo 385 del codice penale. Si applica la disposizione del quarto comma dell’articolo 385 del codice  penale.
Il condannato alla pena sostitutiva del lavoro di pubblica utilità che, senza giustificato motivo, non si reca nel luogo in cui deve svolgere il lavoro ovvero lo abban- dona è punito ai sensi dell’articolo 56 del decreto legisla- tivo 28 agosto 2000, n. 274.
La condanna a uno dei delitti di cui ai commi pri- mo e secondo importa la revoca della pena sostitutiva, salvo che il fatto sia di lieve entità.
La condanna a pena detentiva per un delitto non colposo commesso durante l’esecuzione di una pena so- stitutiva, diversa dalla pena pecuniaria, ne determina la revoca e la conversione per la parte residua nella pena detentiva sostituita, quando la condotta tenuta appare in- compatibile con la prosecuzione della pena sostitutiva, tenuto conto dei criteri di cui all’articolo 58.
La cancelleria del giudice che ha pronunciato la sentenza di cui al quarto comma informa senza indugio    il magistrato di sorveglianza competente per la detenzio- ne domiciliare sostitutiva o per la semilibertà sostitutiva, ovvero il giudice che ha applicato il lavoro di pubblica utilità sostitutivo.»;
z) l’articolo 75 è sostituito dal seguente:
«Art. 75 (Disposizioni relative ai minorenni). — Le disposizioni del presente Capo si applicano anche, in quanto compatibili, agli imputati minorenni. Si applica l’articolo 30 del decreto del Presidente della Repubblica 22 settembre 1988, n. 448.»;
aa) dopo l’articolo 75 è inserito il seguente:
«Art. 75-bis (Disposizioni relative ai reati milita- ri). — Le disposizioni del presente Capo si applicano, in quanto compatibili, ai reati militari quando le prescrizioni risultano in concreto compatibili con la posizione sogget- tiva del condannato.»;
bb) l’articolo 76 è sostituito dal seguente:
«Art. 76 (Norme applicabili). — Alle pene sosti- tutive previste dal presente Capo si applicano, in quan-   to compatibili, gli articoli 47, comma 12-bis, 51-bis, 51-quater e 53-bis della legge 26 luglio 1975, n.  354.»;
cc) alla rubrica del Capo III, le parole: «Sanzioni so- stitutive delle pene detentive brevi» sono sostituite dalle seguenti: «Pene sostitutive delle pene detentive brevi»;
dd) l’articolo 102 è sostituito dal seguente:
«Art. 102 (Conversione delle pene pecuniarie principali per mancato pagamento). — Il mancato paga- mento della multa o dell’ammenda entro il termine di cui all’articolo 660 del codice di procedura penale indicato nell’ordine di esecuzione ne comporta la conversione nel- la semilibertà sostitutiva.
Il ragguaglio si esegue a norma dell’articolo 135 del codice penale. In ogni caso la semilibertà sostitutiva non può avere durata superiore a quattro anni, se la pena convertita è quella della multa, e durata superiore a due anni, se la pena convertita è quella  dell’ammenda.
Se è stato disposto il pagamento rateale, ai sensi dell’articolo 133-ter del codice penale, la conversione ha luogo per la parte residua della pena  pecuniaria.
Il condannato può sempre far cessare l’esecuzione della semilibertà pagando la multa o l’ammenda, dedotta la somma corrispondente alla durata della pena da con- versione espiata; a tal fine, può essere ammesso al pa- gamento rateale, ai sensi dell’articolo 133-ter del codice penale.»;
ee) l’articolo 103 è sostituito dal seguente:
«Art. 103 (Mancato pagamento della pena pecu- niaria per insolvibilità del condannato). — Quando le con- dizioni economiche e patrimoniali del condannato al mo- mento dell’esecuzione rendono impossibile il pagamento della multa o dell’ammenda entro il termine di cui all’arti- colo 660 del codice di procedura penale indicato nell’ordi- ne di esecuzione, la pena pecuniaria è convertita nel lavoro di pubblica utilità sostitutivo ovvero, se il condannato si oppone, nella detenzione domiciliare sostitutiva.
Il ragguaglio si esegue in ogni caso a norma dell’articolo 135 del codice penale e un giorno di lavoro di pubblica utilità sostitutivo  consiste nella prestazione  di due ore di lavoro. In ogni caso il lavoro di pubblica utilità sostitutivo e la detenzione domiciliare sostitutiva non possono avere durata superiore a due anni, se la pena convertita è la multa, e durata superiore a un anno, se la pena convertita è l’ammenda.
Se è stato disposto il pagamento rateale, ai sensi dell’articolo 133-ter del codice penale, la conversione ha luogo per la parte residua della pena  pecuniaria.
Il condannato può in ogni caso far cessare l’ese- cuzione del lavoro di pubblica utilità sostitutiva o della detenzione domiciliare sostitutiva pagando la multa o l’ammenda, dedotta la somma corrispondente alla durata della pena da conversione espiata. A tal fine può essere ammesso al pagamento rateale, ai sensi dell’articolo 133- ter del codice penale.»;
ff) dopo l’articolo 103 sono inseriti i seguenti:
«Art. 103-bis (Inapplicabilità delle misure al- ternative alla detenzione). — Le misure alternative alla detenzione, di cui al  Capo VI  del Titolo  I  della  legge 26 luglio 1975 n. 354, non si applicano al condannato alla semilibertà sostitutiva o alla detenzione domiciliare so- stitutiva derivanti da conversione della pena pecuniaria ai sensi del presente Capo.
Art. 72.
Modifiche al decreto legislativo 28 agosto 2000, n.  274
1.	Al decreto legislativo 28 agosto 2000, n. 274, sono apportate le seguenti modificazioni:
a)	all’articolo 29, al comma 4, le parole: «di media- zione di centri e strutture pubbliche o private presenti sul territorio» sono sostituite dalle seguenti: «dei Centri per la giustizia riparativa presenti sul territorio»;
b)	dopo l’articolo 42, abrogato dall’articolo 299 del decreto del Presidente della Repubblica 30 maggio  2002,
n.	115, è inserito il seguente:
«Art. 42-bis (Esecuzione delle pene    pecuniarie).
—	Le condanne a pena pecuniaria si eseguono a norma dell’articolo 660 del codice di procedura  penale.»;
c)	l’articolo 55 è sostituito dal seguente:
«Art. 55 (Conversione delle pene pecuniarie).  —
1.	Per i reati di competenza del giudice di pace, la pena pecuniaria non eseguita per insolvibilità del condanna-    to entro il termine di cui all’articolo 660 del codice di procedura penale indicato nell’ordine di esecuzione si converte, a richiesta del condannato, in lavoro di pubbli- ca utilità da svolgere per un periodo non inferiore ad un mese e non superiore a sei mesi con le modalità indicate nell’articolo 54.
2.	Ai fini della conversione un giorno di lavoro di pub- blica utilità equivale a 250 euro di pena  pecuniaria.
3.	Quando è violato l’obbligo del lavoro di pubblica utilità conseguente alla conversione della pena pecunia- ria, la parte di lavoro non ancora eseguito si converte nell’obbligo di permanenza domiciliare secondo i criteri di ragguaglio indicati nel comma 5.
4.	Se il condannato non richiede di svolgere il lavoro di pubblica utilità, ovvero se il mancato pagamento di cui al primo comma non è dovuto a insolvibilità, le pene pecu- niarie non eseguite si convertono nell’obbligo di perma- nenza domiciliare con le forme e nei modi previsti dall’ar- ticolo 53, comma 1, e in questo caso non è applicabile al condannato il divieto di cui all’articolo 53, comma 3.
5.	Ai fini della conversione un giorno di permanenza domiciliare equivale a 250 euro di pena pecuniaria e la durata della permanenza non può essere superiore a qua- rantacinque giorni.
6.	Il condannato può sempre far cessare la pena del la- voro di pubblica utilità o della permanenza domiciliare pagando la pena pecuniaria, dedotta la somma corrispon- dente alla durata della pena da conversione  espiata.».
Art. 73.
Modifiche al decreto del Presidente della Repubblica 22 settembre 1988, n. 448
1.	L’articolo 30 del decreto del Presidente della Repub- blica 22 settembre 1988, n. 448, è sostituito dal seguente:
«Art. 30 (Pene sostitutive). — 1. Con la sentenza di condanna il giudice, quando ritiene di dover applicare una pena detentiva non superiore a quattro anni, può sostitu- irla con la semilibertà o con la detenzione domiciliare, previste dalla legge 24 novembre 1981, n. 689; quando

ritiene di dover applicare una pena detentiva non supe- riore a tre anni, può sostituirla, se vi è il consenso del minore non più soggetto ad obbligo di istruzione, con il lavoro di pubblica utilità previsto dalla legge 24 novem- bre 1981, n. 689; quando ritiene di doverla determinare entro il limite di un anno, può sostituirla, altresì, con la pena pecuniaria della specie corrispondente, determinata ai sensi dell’articolo 56-quater della legge 24 novembre 1981, n. 689. In ogni caso, nel sostituire la pena detentiva e nello scegliere la pena sostitutiva, il giudice tiene conto della personalità e delle esigenze di lavoro o di studio del minorenne nonché delle sue condizioni familiari, sociali  e ambientali.
2.	Il pubblico ministero competente per l’esecuzione trasmette l’estratto della sentenza al magistrato di sorve- glianza per i minorenni del luogo di abituale dimora del condannato. Il magistrato di sorveglianza convoca, entro tre giorni dalla comunicazione, il minorenne, l’esercen-  te la responsabilità genitoriale, l’eventuale affidatario e     i servizi minorili dell’amministrazione della giustizia e provvede in ordine alla esecuzione della pena sostitutiva  a norma delle leggi vigenti, tenuto conto anche delle esi- genze educative del minorenne.
3.	Si applicano, in quanto compatibili, le disposi- zioni di cui al Capo III della legge 24 novembre 1981,
n.	689, ad eccezione dell’articolo 59, e le funzioni attribu- ite all’ufficio di esecuzione penale esterna sono esercitate dai servizi minorili dell’amministrazione della  giustizia.
4.	Al compimento del venticinquesimo anno di età, se è in corso l’esecuzione di una pena sostitutiva, il magi- strato di sorveglianza per i minorenni trasmette gli atti al magistrato di sorveglianza ordinario per la prosecuzione della pena, ove ne ricorrano le condizioni, con le modalità previste dalla legge 24 novembre 1981, n.  689.».
Art. 74.
Modifiche al decreto legislativo 28 luglio 1989, n.  272
1.	Al decreto legislativo 28 luglio 1989, n. 272, sono apportate le seguenti modificazioni:
a)	all’articolo 11, al comma 1 e nella rubrica le paro- le «e semidetenzione» sono soppresse;
b)	all’articolo 24, comma 1, la parola «sanzioni» è sostituita dalla seguente: «pene».
Art. 75.
Modifiche alla legge 28 aprile 2014, n. 67
1.	All’articolo 7 della legge 28 aprile 2014, n. 67, sono apportate le seguenti modificazioni:
a)	al comma 1, dopo le parole «del presente capo» sono inserite le seguenti: «e del decreto legislativo attua- tivo della legge 27 settembre 2021, n. 134» e le parole:
«Dipartimento dell’amministrazione penitenziaria» sono sostituite dalle seguenti: «Dipartimento per la giustizia minorile e di comunità»;
b)	al comma 2, dopo le parole «alla prova» sono ag- giunte le seguenti: «e di pene sostitutive delle pene deten- tive, nonché sullo stato generale dell’esecuzione penale esterna»;

c)	nella rubrica, le parole: «Dipartimento dell’ammi- nistrazione penitenziaria» sono sostituite dalle   seguenti:
«Dipartimento per la giustizia minorile e di  comunità».
Art. 76.
Modifiche al codice penale militare di pace, approvato con regio decreto 20 febbraio 1941, n. 303)
1.	Al codice penale militare di pace, approvato con re- gio decreto 20 febbraio 1941, n. 303, sono apportate le seguenti modifiche:
a)	all’articolo 174, dopo il terzo comma, è aggiunto il seguente: «Non si applica l’articolo 131-bis del codice penale.»;
b)	all’articolo 215, dopo il primo comma, è aggiunto il seguente: «Non si applica l’articolo 131-bis del   codice

Art. 78.
Modifiche alla legge 26 luglio 1975, n. 354
1.	Alla legge 26 luglio 1975, n. 354, sono apportate le seguenti modificazioni:
a)	all’articolo 13, dopo il terzo comma è inserito il seguente: «Nei confronti dei condannati e degli internati  è favorito il ricorso a programmi di giustizia  riparativa.»;
b)	dopo l’articolo 15 è inserito il seguente:
«Art. 15-bis (Giustizia riparativa). — 1. In qual- siasi fase dell’esecuzione, l’autorità giudiziaria può di- sporre l’invio dei condannati e degli internati, previa ade- guata informazione e su base volontaria, ai programmi di giustizia riparativa.
2.	La partecipazione al programma di giustizia ri- parativa e l’eventuale esito riparativo sono valutati ai  fini

penale.»;
c)	dopo l’articolo 261-quater è inserito il seguente:
«Art. 261-quinquies (Malfunzionamento dei si- stemi informatici degli uffici giudiziari militari). — Il malfunzionamento dei sistemi informatici in uso presso gli uffici giudiziari militari è certificato dal responsabi-   le della transizione al digitale del Ministero della difesa, attestato sul portale della Giustizia militare e comunicato dal dirigente dell’ufficio giudiziario, con modalità tali da assicurarne la tempestiva conoscibilità ai soggetti interes- sati. Il ripristino del corretto funzionamento è certificato, attestato e comunicato con le medesime  modalità.
Le certificazioni, attestazioni e comunicazioni di cui al primo comma contengono l’indicazione della data e, ove risulti, dell’orario dell’inizio e della fine del mal- funzionamento, registrati, in relazione a ciascun settore interessato, dal responsabile della transizione al digitale del Ministero della difesa.
Nei casi di cui al primo e al secondo comma, a de- correre dall’inizio e sino alla fine del malfunzionamento dei sistemi informatici, atti e documenti sono redatti in forma di documento analogico e depositati con modalità non telematiche, fermo quanto disposto dagli articoli 110, comma 4, e 111-ter, comma 3, del codice di procedura penale.
La disposizione di cui al terzo comma si appli-  ca, altresì, nel caso di malfunzionamento del sistema non certificato ai sensi del primo comma, accertato ed atte- stato dal dirigente dell’ufficio giudiziario, e comunicato con modalità tali da assicurare la tempestiva conoscibilità ai soggetti interessati della data di inizio e della fine del malfunzionamento.
Se la scadenza di un termine previsto a pena di decadenza si verifica nel periodo di malfunzionamento certificato ai sensi del primo e del secondo comma o ac- certato ai sensi del quarto comma 4, si applicano le dispo- sizioni dell’articolo 175 del codice di procedura  penale».
Art. 77.
Modifiche alla legge 9 dicembre 1941, n. 1383
1. Alla legge 9 dicembre 1941, n. 1383, all’articolo 3, dopo il terzo comma, è aggiunto il seguente: «Non si ap- plica l’articolo 131-bis del codice penale.».
za o insolvibilità del condannato, alla estinzione per esito positivo dell’affidamento in prova al servizio sociale, ai sensi dell’articolo 47, comma 12, della legge 26 luglio 1975, n. 354, e alla prescrizione ai sensi degli articoli 172 e 173 del codice penale, sono pubblicati periodicamente sul sito del Ministero della giustizia e sono trasmessi an- nualmente al Parlamento, unitamente alla relazione di cui al comma 1.

Capo IV
MODIFICHE IN MATERIA DI SPESE DI  GIUSTIZIA

Art. 80.
Modifiche al decreto del Presidente della Repubblica 30 maggio 2002, n. 115
1.	Al decreto del Presidente della Repubblica 30 mag- gio 2002, n. 115, sono apportate le seguenti modificazioni:
a)	all’articolo 1, comma 1, le parole: «delle pene pe- cuniarie,» sono soppresse;
b)	all’articolo 200, comma 1, le parole: «le pene pe- cuniarie,» sono soppresse;
c)	all’articolo 211, comma 1, le parole: «per le pene pecuniarie,» sono soppresse;
d)	all’articolo 235:
1)	al comma 1, le parole: «e alle pene pecuniarie,» sono soppresse;
2)	al comma 2, le parole: «e delle pene pecunia- rie» sono soppresse.

Art. 81.
Modifiche alla legge 24 dicembre 2007, n. 244
1. All’articolo 1, comma 367, della legge 24 dicembre 2007, n. 244, le parole: «e alle pene pecuniarie» sono soppresse.

Capo V
MODIFICHE IN MATERIA DI ISCRIZIONE NEL CASELLARIO GIUDIZIARIO

Art. 82.
Modifiche al decreto del Presidente della Repubblica 14 novembre 2002, n. 313
1. All’articolo 3, comma 1, del decreto del Presidente della Repubblica 14 novembre 2002, n. 313, la lettera g)  è sostituita dalla seguente: «g) i provvedimenti giudiziari definitivi di condanna alle pene sostitutive e i provvedi- menti di conversione di cui agli articoli 66, terzo com- ma, e 72, quarto comma, della legge 24 novembre   1981,
n.	689;» e dopo la lettera g) è inserita la seguente: «g- bis) i provvedimenti di conversione di cui agli articoli 71, 102, 103 e 108 della legge 24 novembre 1981, n. 689, e di cui all’articolo 55 del decreto legislativo 28 agosto 2000, n. 274;».

Capo VI
MODIFICHE IN MATERIA DI GIUSTIZIA RIPARATIVA IN AMBITO MINORILE

Art. 83.
Modifiche al decreto del Presidente della Repubblica 22 settembre 1988, n. 448
1.	All’articolo 28, comma 2, del decreto del Presidente della Repubblica 22 settembre 1988, n. 448, dopo le paro- le «persona offesa dal reato» sono aggiunte le seguenti: «, nonché formulare l’invito a partecipare a un programma di giustizia riparativa, ove ne ricorrano le  condizioni».
Art. 84.
Modifiche al decreto legislativo 2 ottobre 2018, n. 121
1.	Al decreto legislativo 2 ottobre 2018, n. 121, sono apportate le seguenti modificazioni:
a)	all’articolo 1, comma 2, le parole «percorsi di giu- stizia riparativa e di mediazione con le vittime di reato» sono sostituite dalle seguenti: «i programmi di giustizia riparativa di cui al decreto legislativo attuativo della leg- ge 27 settembre 2021, n. 134»;
b)	dopo l’articolo 1 è inserito il seguente:
«Art. 1-bis (Giustizia riparativa). — 1. In qualsiasi fase dell’esecuzione, l’autorità giudiziaria può disporre l’in- vio dei minorenni condannati, previa adeguata informazio- ne e su base volontaria, ai programmi di giustizia riparativa.
2.	Il giudice, ai fini dell’adozione delle misure penali di comunità, delle altre misure alternative e della liberazione condizionale, valuta la partecipazione al pro- gramma di giustizia riparativa e l’eventuale esito ripara- tivo. In ogni caso, non tiene conto della mancata effettua- zione del programma, dell’interruzione dello stesso o del mancato raggiungimento di un esito  riparativo.».





TITOLO VI
DISPOSIZIONI TRANSITORIE, FINALI E ABROGAZIONI

Art. 85.
Disposizioni transitorie in materia di modifica del regime di procedibilità
1.	Per i reati perseguibili a querela della persona of- fesa in base alle disposizioni del presente decreto, com- messi prima della data di entrata in vigore dello stesso, il termine per la presentazione della querela decorre dalla predetta data, se la persona offesa ha avuto in precedenza notizia del fatto costituente reato.
2.	Quando, per i reati di cui al comma 1, alla data di entrata in vigore del presente decreto è stata già esercitata l’azione penale, il giudice informa la persona offesa dal re- ato della facoltà di esercitare il diritto di querela e il termine decorre dal giorno in cui la persona offesa è stata informa- ta. Ai fini di cui al primo periodo, il giudice effettua ogni utile ricerca anagrafica, ove necessaria. Prima dell’eserci- zio dell’azione penale, provvede il pubblico  ministero.
Art. 86.
Disposizioni transitorie in materia di notificazioni al querelante
1.	Per le querele presentate prima dell’entrata in vigore del presente decreto, le notificazioni al querelante sono eseguite ai sensi dell’articolo 33 delle norme di attuazio- ne, di coordinamento e transitorie del codice di procedura penale, di cui al decreto legislativo 28 luglio 1989, n. 271.
2.	Quando il querelante non ha nominato un difensore, le notificazioni si eseguono presso il domicilio dichiara- to o eletto dal querelante. In mancanza di dichiarazione    o elezione di domicilio, le notificazioni sono eseguite a norma dell’articolo 157, commi 1, 2, 3, 4 e 8, del codice di procedura penale.
Art. 87.
Disposizioni transitorie in materia di processo penale telematico
1.	Con decreto del Ministro della giustizia, da adottarsi entro il 31 dicembre 2023 ai sensi dell’articolo 17, com- ma 3, della legge 23 agosto 1988, n. 400, sentito il Ga- rante per la protezione dei dati personali, sono definite le regole tecniche riguardanti il deposito, la comunicazione e la notificazione con modalità telematiche degli atti del procedimento penale, anche modificando, ove necessario, il regolamento di cui al decreto del Ministro della giusti- zia 21 febbraio 2011, n. 44, e, in ogni caso, assicurando  la conformità al principio di idoneità del mezzo e a quello della certezza del compimento dell’atto.
2.	Nel rispetto delle disposizioni del presente decre-  to e del regolamento di cui al comma 1, ulteriori regole tecniche possono essere adottate con atto dirigenziale del Direttore generale dei sistemi informativi e automatizzati del Ministero della giustizia.
3.	Con decreto del Ministro della giustizia, da adottarsi entro il 31 dicembre 2023 ai sensi dell’articolo 17, com- ma 3, della legge 23 agosto 1988, n. 400, sentiti il Consi- glio superiore della magistratura e il Consiglio nazionale forense, sono individuati gli uffici giudiziari e le tipologie di atti per cui possano essere adottate anche modalità non telematiche di deposito, comunicazione o notificazione, nonché i termini di transizione al nuovo regime di depo- sito, comunicazione e notificazione.
4.	Sino al quindicesimo giorno successivo alla pubbli- cazione dei regolamenti di cui ai commi 1 e 3, ovvero sino al diverso termine di transizione previsto dal regola- mento di cui al comma 3 per gli uffici giudiziari e per le tipologie di atti in esso indicati, continuano ad applicarsi, nel testo vigente al momento dell’entrata in vigore del presente decreto, le disposizioni di cui agli articoli 110, 111, comma 1, 116, comma 3-bis, 125, comma 5, 134, comma 2, 135, comma 2, 162, comma 1, 311, comma 3, 391-octies, comma 3, 419, comma 5, primo periodo, 447, comma 1, primo periodo, 461, comma 1, 462, comma 1, 582, comma 1, 585, comma 4, del codice di procedura penale, nonché le disposizioni di cui l’articolo 154, com- mi 2, 3 e 4 delle norme di attuazione, di coordinamento e transitorie del codice di procedura penale, di cui al decre- to legislativo 28 luglio 1989, n. 271.

5.	Le disposizioni di cui agli articoli 111, commi 2-  bis, 2-ter e 2-quater, 111-bis, 111-ter, 122, comma 2-bis, 172, commi 6-bis e 6-ter, 175-bis, 386, comma 1-ter,  483, comma 1-bis, 582, comma 1-bis, del codice di pro- cedura penale, così come introdotte dal presente decreto, si applicano a partire dal quindicesimo giorno successivo alla pubblicazione dei regolamenti di cui ai commi 1 e    3, ovvero a partire dal diverso termine previsto dal re- golamento di cui al comma 3 per gli uffici giudiziari  e  per le tipologie di atti in esso indicati. Sino alle stesse date, la dichiarazione e l’elezione di domicilio prevista dal comma 2 dell’articolo 153-bis del codice di procedura penale, come introdotto dall’articolo 10, comma 1, lettera e), del presente decreto, nonché le comunicazioni previste dal comma 3 dello stesso articolo 153-bis sono effettuate con le forme ivi previste in alternativa al deposito in via telematica.
6.	Sino al quindicesimo giorno successivo alla pubbli- cazione dei regolamenti di cui ai commi 1 e 3, ovvero sino al diverso termine previsto dal regolamento di cui    al comma 3 per gli uffici giudiziari e le tipologie di atti   in esso indicati, continuano ad applicarsi le disposizioni dell’articolo 164 delle norme di attuazione, di coordina- mento e transitorie del codice di procedura penale, di cui al decreto legislativo 28 luglio 1989, n. 271, e dell’ar- ticolo 24, commi da 1 a 3, del decreto-legge 28 ottobre 2020, n. 137, convertito, con modificazioni, dalla legge  18 dicembre 2020, n. 176.
7.	Le disposizioni del presente articolo si applicano anche in relazione agli atti del procedimento penale mi- litare, ma i regolamenti di cui ai commi 1 e 3 sono adot- tati, entro il 31 dicembre 2023, con decreto del Ministro della difesa, ai sensi dell’articolo 17, comma 3, della leg- ge 23 agosto 1988, n. 400, sentiti il Consiglio della ma- gistratura militare e il Garante per la protezione dei dati personali. Le ulteriori regole tecniche di cui al comma 2 possono essere adottate, d’intesa con il Consiglio della magistratura militare, con atto dirigenziale del responsa- bile della transizione al digitale del Ministero della difesa.
Art. 88.
Disposizioni transitorie in materia di restituzione nel termine
1. Nei procedimenti che hanno ad oggetto reati com- messi prima del 1° gennaio 2020, nei quali sia disposta la restituzione nel termine prevista dall’articolo 175, com- ma 2.1, del codice di procedura penale non si tiene conto, ai fini della prescrizione del reato, del tempo intercorso  tra la scadenza dei termini per impugnare di cui all’arti- colo 585 del codice di procedura penale e la notificazione alla parte dell’avviso di deposito dell’ordinanza che con- cede la restituzione.
Art. 89.
Disposizioni transitorie in materia di assenza
1.	Salvo quanto previsto dai commi 2 e 3, quando, nei processi pendenti alla data di entrata in vigore del pre- sente decreto,  è stata  già pronunciata,  in qualsiasi  stato e grado del procedimento, ordinanza con la quale si è  di-
sposto procedersi in assenza dell’imputato, continuano ad applicarsi le disposizioni del codice di procedura penale e delle norme di attuazione, di coordinamento e transitorie del codice di procedura penale in materia di assenza ante- riormente vigenti, comprese quelle relative alle questioni di nullità in appello e alla rescissione del  giudicato.
2.	Quando, prima dell’entrata in vigore del presente decreto, nell’udienza preliminare o nel giudizio di primo grado è stata disposta la sospensione del processo ai sensi dell’articolo 420-quater, comma 2, del codice di procedu- ra penale nel testo vigente prima dell’entrata in vigore del presente decreto e l’imputato non è stato ancora rintrac- ciato, in luogo di disporre nuove ricerche ai sensi dell’ar- ticolo 420-quinquies del codice di procedura penale nel testo vigente prima dell’entrata in vigore del presente de- creto, il giudice provvede ai sensi dell’articolo 420-qua- ter del codice di procedura penale come modificato dal presente decreto. In questo caso si applicano gli articoli 420-quinquies e 420-sexies del codice di procedura pena- le, come modificati dal presente decreto.
3.	Le disposizioni degli articoli 157-ter, comma 3, 581, commi 1-ter e 1-quater, e 585, comma 1-bis, del codice  di procedura penale si applicano per le sole impugnazioni proposte avverso sentenze pronunciate in data successiva a quella di entrata in vigore del presente decreto. Negli stessi casi si applicano anche le disposizioni dell’artico-  lo 175 del codice di procedura penale, come modificato dal presente decreto.
4.	Nei procedimenti indicati al comma 1, continua ad applicarsi la disposizione dell’articolo 159, primo com- ma, numero 3-bis), del codice penale nel testo vigente prima della data di entrata in vigore del presente decreto legislativo.
5.	Nei procedimenti di cui ai commi 1 e 2 che hanno  ad oggetto reati commessi dopo il 18 ottobre 2021, nel caso di sospensione del corso della prescrizione ai sensi dell’articolo 159, primo comma, numero 3-bis, del codi- ce penale, si applica la disposizione dell’ultimo comma   di detto articolo, come modificata dal presente decreto legislativo.

Art. 90.
Disposizioni transitorie in materia di sospensione del procedimento con messa alla prova dell’imputato
1.	La disposizione dell’articolo 32, comma 1, lettera a), del presente decreto, che comporta l’estensione della disciplina della sospensione del procedimento con messa alla prova a ulteriori reati, si applica anche ai procedi- menti pendenti nel giudizio di primo grado e in grado di appello alla data di entrata in vigore del presente decreto legislativo.
2.	Se sono già decorsi i termini di cui all’articolo 464- bis, comma 2, del codice di procedura penale, l’imputa- to, personalmente o a mezzo di procuratore speciale,  può

formulare la richiesta di sospensione del procedimento con messa alla prova, a pena di decadenza, entro la prima udienza successiva alla data di entrata in vigore del pre- sente decreto. Quando nei quarantacinque giorni succes- sivi alla data di entrata in vigore del presente decreto non è fissata udienza, la richiesta è depositata in cancelleria, a pena di decadenza, entro il predetto termine.
3.	Nel caso in cui sia stata disposta la sospensione del procedimento con messa alla prova in forza dei commi precedenti, non si applica l’articolo 75, comma 3, del co- dice di procedura penale.

Art. 91.
Disposizioni transitorie in materia di rimedi per l’esecuzione delle decisioni della Corte europea dei diritti dell’uomo

1.	Quando, in data anteriore all’entrata in vigore del presente decreto, è divenuta definitiva la decisione  con cui la Corte europea ha accertato una violazione dei diritti riconosciuti dalla Convenzione per la salvaguardia dei di- ritti dell’uomo e delle libertà fondamentali o dai Protocol- li addizionali alla Convenzione, ovvero la Corte europea ha disposto, ai sensi dell’articolo 37 della Convenzione,  la cancellazione dal ruolo del ricorso a seguito del ricono- scimento unilaterale della violazione da parte dello Stato, il termine indicato nell’articolo 628-bis, comma 2, del codice di procedura penale decorre dal giorno successivo alla data di entrata in vigore del presente  decreto.
2.	Per i reati commessi in data anteriore al 1° gennaio 2020, la prescrizione riprende il suo corso in ogni caso in cui la Corte di cassazione dispone la riapertura del pro- cesso ai sensi dell’articolo 628-bis, comma 5, del codice di procedura penale.

Art. 92.
Disposizioni transitorie in materia di giustizia riparativa. Servizi esistenti

1.	La Conferenza locale per la giustizia riparativa, en- tro il termine di sei mesi dalla data di entrata in vigore del presente decreto, provvede alla ricognizione dei servizi   di giustizia riparativa in materia penale erogati alla stessa data da soggetti pubblici o privati specializzati, conven- zionati con il Ministero della giustizia ovvero che opera- no in virtù di protocolli di intesa con gli uffici giudiziari o altri soggetti pubblici.
2.	La Conferenza valuta i soggetti di cui al comma 1 con riferimento all’esperienza maturata almeno nell’ulti- mo quinquennio e il curricolo degli operatori in servizio alla data di entrata in vigore del presente decreto, verifi- cando altresì la coerenza delle prestazioni erogate e dei requisiti  posseduti  dagli  operatori  con  quanto  disposto
dagli articoli 42, 64 e 93, e redige al termine un elenco   da cui attingono gli enti locali per la prima apertura dei centri di cui all’articolo 63.

Art. 93.
Disposizioni transitorie in materia di giustizia riparativa. Inserimento nell’elenco dei mediatori
1.	Sono inseriti nell’elenco di cui all’articolo 60 coloro che, alla data di entrata in vigore del presente decreto, sono in possesso di almeno uno dei seguenti requisiti:
a)	avere completato una formazione alla giustizia ri- parativa ed essere in possesso di una esperienza almeno quinquennale, anche a titolo volontario e gratuito, acqui- sita nel decennio precedente presso soggetti specializzati che erogano servizi di giustizia riparativa, pubblici o pri- vati, convenzionati con il Ministero della giustizia ovvero che operano in virtù di protocolli di intesa con gli uffici giudiziari o altri enti pubblici;
b)	avere completato una formazione teorica e prati- ca, seguita da tirocinio, nell’ambito della giustizia ripa- rativa in materia penale, equivalente o superiore a quella prevista dal presente decreto;
c)	prestare servizio presso i servizi minorili della giustizia o gli uffici di esecuzione penale esterna, ave-    re completato una adeguata formazione alla giustizia riparativa ed essere in possesso di adeguata esperienza almeno quinquennale acquisita in materia nel decennio precedente.
2.	L’inserimento nell’elenco, ai sensi del comma 1, è disposto a seguito della presentazione, a cura dell’inte- ressato, di idonea documentazione comprovante il pos- sesso dei requisiti e, nel caso di cui alla lettera b), previo superamento di una prova pratica valutativa, il cui onere finanziario è a carico dei partecipanti, come da succes- siva regolamentazione a mezzo di decreto del Ministro della giustizia, di concerto con il Ministro dell’università e della ricerca.
3.	Con il medesimo decreto di cui al comma 2 sono stabilite altresì le modalità di svolgimento e valutazio-   ne della prova di cui al comma 2, nonché di inserimento nell’elenco di cui ai commi 1 e 2.

Art. 94.
Disposizioni transitorie in materia di videoregistrazioni e di giudizi di impugnazione
1.	Le disposizioni di cui all’articolo 30, comma 1, let- tera i), si applicano decorso un anno dalla data di entrata in vigore del presente decreto.
2.	Le disposizioni degli articoli 34, comma 1, lettere c), e), f), g), numeri 2), 3), 4), e h), 35, comma 1, lettera a),   e 41, comma 1, lettera ee), si applicano a decorrere   dalla

scadenza del termine fissato dall’articolo 16, comma 1, del decreto-legge 30 dicembre 2021, n. 228,    convertito,
con modificazioni, dalla legge 25 febbraio 2022, n.  15.

Art. 95.
Disposizioni transitorie in materia di pene sostitutive delle pene detentive brevi
1.	Le norme previste dal Capo III della legge 24 no- vembre 1981, n. 689, se più favorevoli, si applicano an- che ai procedimenti penali pendenti in primo grado o in grado di appello al momento dell’entrata in vigore del presente decreto. Il condannato a pena detentiva non su- periore a quattro anni, all’esito di un procedimento pen- dente innanzi la Corte di cassazione all’entrata in vigore del presente decreto, può presentare istanza di applicazio- ne di una delle pene sostitutive di cui al Capo III della leg- ge 24 novembre 1981, n. 689, al giudice dell’esecuzione, ai sensi dell’articolo 666 del codice di procedura penale, entro trenta giorni dalla irrevocabilità della sentenza. Nel giudizio di esecuzione si applicano, in quanto compatibi- li, le norme del Capo III della legge 24 novembre 1981,
n. 689, e del codice di procedura penale relative alle pene sostitutive. In caso di annullamento con rinvio provvede  il giudice del rinvio.
2.	Le sanzioni sostitutive della semidetenzione e della libertà controllata, già applicate o in corso di esecuzione al momento dell’entrata in vigore del presente decreto, continuano ad essere disciplinate dalle disposizioni previ- genti. Tuttavia, i condannati alla semidetenzione possono chiedere al magistrato di sorveglianza la conversione nel- la semilibertà sostitutiva.
3.	Sino all’entrata in vigore del decreto ministeriale di cui all’articolo 56-bis, quarto comma, della legge 24 no- vembre 1981, n. 689, si applicano, in quanto compatibi- li, i decreti del Ministro della giustizia 26 marzo 2001, pubblicato nella Gazzetta ufficiale 5 aprile 2001, n. 80, e 8 giugno 2015, n. 88, pubblicato nella Gazzetta ufficiale  2 luglio 2015, n. 151.

Art. 96.
Disposizioni transitorie in materia di estinzione delle contravvenzioni in materia di alimenti
1.	Le disposizioni dell’articolo 70 non si applicano ai procedimenti in corso alla data di entrata in vigore del presente decreto nei quali sia già stata esercitata l’azione penale.
2.	Nelle more dell’adozione del decreto di cui all’arti- colo 12-quinquies, comma 4, della legge 30 aprile   1962,
n. 283, si applicano, in quanto compatibili, i decreti del Ministro della giustizia 26 marzo 2001, pubblicato nella Gazzetta ufficiale 5 aprile 2001, n. 80, e 8 giugno    2015,
n.	88, pubblicato nella Gazzetta ufficiale 2 luglio 2015,  n. 151.
Art. 97.
Disposizioni transitorie in materia di esecuzione e conversione delle pene pecuniarie
1.	Salvo che risultino più favorevoli al condannato, le disposizioni in materia di conversione delle pene pecu- niarie, previste dall’articolo 71 e dal Capo V della legge 24 novembre 1981, n. 689, come modificate dal presente decreto, si applicano ai reati commessi dopo la sua entrata in vigore.
2.	Fermo quanto previsto dal comma 1, ai reati com- messi prima della data di entrata in vigore del presente decreto continuano ad applicarsi le disposizioni in ma- teria di conversione ed esecuzione delle pene pecunia-  rie previste dal Capo V della legge 24 novembre 1981,
n. 689, dall’articolo 660 del codice di procedura penale    e da ogni altra disposizione di legge, vigenti prima della data di entrata in vigore del presente decreto.
3.	Le disposizioni del decreto del Presidente della Re- pubblica 30 maggio 2002, n. 115, abrogate o modificate dal presente decreto, nonché le disposizioni di cui all’arti- colo 1, comma 367, della legge 24 dicembre 2007, n. 244, continuano ad applicarsi in relazione alle pene pecunia- rie irrogate per reati commessi prima della sua entrata in vigore.

Art. 98.
Abrogazioni
1.	Dalla data di entrata in vigore del presente decreto legislativo sono abrogate le seguenti disposizioni:
a)	gli articoli 134, comma 4, 150, 151, 157, com-  ma 8-bis, 158, 161, comma 2, 369, comma 2, 405, com- ma 1, 406, commi 2-bis e 2-ter, 407, comma 3-bis, 415, comma 2-bis, 416, comma 2-bis, 420-ter, comma 3, 429, commi 2-bis e 4, 442, comma 3, 552, comma 1-bis, 555, commi 2 e 3, 582, comma 2, 583, 599-bis, comma 2, 602, comma 1-bis, del codice di procedura penale;
b)	gli articoli 45-bis, comma 2, 125, 133, comma 1, 134,146-bis, commi 2, 3, 4, 5 e 6, 147-bis, comma 4, 154, comma 3, 164 delle norme di attuazione, di coordinamen- to e transitorie del codice di procedura penale, di cui al decreto legislativo 28 luglio 1989, n. 271;
c)	gli articoli 105 e 106 della legge 24 novembre 1981, n. 689;
d)	gli articoli 236, 237, 238 e 238-bis del decreto del Presidente della Repubblica 30 maggio 2002, n. 115.

Art. 99.
Disposizioni finanziarie
1.	Salvo quanto previsto all’articolo 67, le amministra- zioni interessate nell’ambito delle rispettive competenze, danno attuazione alle disposizioni del presente decreto, con le risorse umane, strumentali e finanziarie disponibili a legislazione vigente e senza nuovi o maggiori oneri a carico della finanza pubblica.

Il presente decreto, munito del sigillo dello Stato, sarà inserito nella Raccolta ufficiale degli atti normativi della Repubblica italiana. E’ fatto obbligo a chiunque spetti di osservarlo e di farlo osservare.
Dato a Roma, addì 10 ottobre 2022

MATTARELLA
DRAGHI, Presidente del Con- siglio dei ministri
CARTABIA, Ministro della giustizia
FRANCO, Ministro dell’eco- nomia e delle finanze
COLAO, Ministro per l’inno- vazione tecnologica e la transizione digitale
BRUNETTA, Ministro per la pubblica amministra zio- ne
BIANCHI, Ministro dell’istru- zione
MESSA, Ministro dell’univer- sità e della ricerca
GELMINI, Ministro per gli affari regionali e le auto- nomie
ORLANDO, Ministro del lavo- ro e delle politiche sociali
LAMORGESE,	Ministro dell’interno
GUERINI, Ministro della di- fesa
Visto, il Guardasigilli: CARTABIA



–  Giudice di Pace decreto legislativo 28 agosto 2000, n.  274

«Art. 42-bis (Esecuzione delle pene    pecuniarie).
—	Le condanne a pena pecuniaria si eseguono a norma dell’articolo 660 del codice di procedura  penale.»;
c)	l’articolo 55 è sostituito dal seguente:
«Art. 55 (Conversione delle pene pecuniarie).  —
1.	Per i reati di competenza del giudice di pace, la pena pecuniaria non eseguita per insolvibilità del condannato entro il termine di cui all’articolo 660 del codice di procedura penale indicato nell’ordine di esecuzione si converte, a richiesta del condannato, in lavoro di pubblica utilità da svolgere per un periodo non inferiore ad un mese e non superiore a sei mesi con le modalità indicate nell’articolo 54.
2.	Ai fini della conversione un giorno di lavoro di pubblica utilità equivale a 250 euro di pena  pecuniaria.
3.	Quando è violato l’obbligo del lavoro di pubblica utilità conseguente alla conversione della pena pecuniaria, la parte di lavoro non ancora eseguito si converte nell’obbligo di permanenza domiciliare secondo i criteri di ragguaglio indicati nel comma 5.
4.	Se il condannato non richiede di svolgere il lavoro di pubblica utilità, ovvero se il mancato pagamento di cui al primo comma non è dovuto a insolvibilità, le pene pecuniarie non eseguite si convertono nell’obbligo di permanenza domiciliare con le forme e nei modi previsti dall’articolo 53, comma 1, e in questo caso non è applicabile al condannato il divieto di cui all’articolo 53, comma 3.
5.	Ai fini della conversione un giorno di permanenza domiciliare equivale a 250 euro di pena pecuniaria e la durata della permanenza non può essere superiore a quarantacinque giorni.
6.	Il condannato può sempre far cessare la pena del la- voro di pubblica utilità o della permanenza domiciliare pagando la pena pecuniaria, dedotta la somma corrispondente alla durata della pena da conversione  espiata.».

Creare la maschera di caricamento delle sanzioni del giudice di pace Già presente nel provvedimento di cumulo integrandola con le prescrizioni e termini per l’esecuzione.
| Sanzioni del giudice di pace | Sanzioni del giudice di pace |
| --- | --- |
| Permanenza Domiciliare | Anni  Mesi  Giorni |
| Lavoro pubblica utilità | Anni  Mesi  Giorni |
| Lavoro sostitutivo | Anni  Mesi  Giorni |
| Espulsione dallo Stato | Perpetua oppure Temporanea per Anni  Mesi  Giorni |

La parte relativa alla riscossione delle pena pecuniaria occorre fare riferimento alla parte iniziale-
Per le gestioni successiva va prevista tutta al gestione
Proporre la gestione anche della pena, anche in modalità ridotta

Esecuzione minorenni decreto del Presidente della Repubblica 22 settembre 1988, n. 448
La gestione rispecchia Siep maggiorenni

Art. 73.
Modifiche al decreto del Presidente della Repubblica 22 settembre 1988, n. 448
1.	L’articolo 30 del decreto del Presidente della Repub-blica 22 settembre 1988, n. 448, è sostituito dal seguente:
«Art. 30 (Pene sostitutive). — 1. Con la sentenza di condanna il giudice, quando ritiene di dover applicare una pena detentiva non superiore a quattro anni, può sostituirla con la semilibertà o con la detenzione domiciliare, previste dalla legge 24 novembre 1981, n. 689; quando
ne di dover applicare una pena detentiva non superiore a tre anni, può sostituirla, se vi è il consenso del minore non più soggetto ad obbligo di istruzione, con il lavoro di pubblica utilità previsto dalla legge 24 novem- bre 1981, n. 689; quando ritiene di doverla determinare entro il limite di un anno, può sostituirla, altresì, con la pena pecuniaria della specie corrispondente, determinata ai sensi dell’articolo 56-quater della legge 24 novembre 1981, n. 689. In ogni caso, nel sostituire la pena detentiva e nello scegliere la pena sostitutiva, il giudice tiene conto della personalità e delle esigenze di lavoro o di studio del minorenne nonché delle sue condizioni familiari, sociali  e ambientali.
2.	Il pubblico ministero competente per l’esecuzione trasmette l’estratto della sentenza al magistrato di sorveglianza per i minorenni del luogo di abituale dimora del condannato. Il magistrato di sorveglianza convoca, entro tre giorni dalla comunicazione, il minorenne, l’esercente la responsabilità genitoriale, l’eventuale affidatario e i servizi minorili dell’amministrazione della giustizia e provvede in ordine alla esecuzione della pena sostitutiva  a norma delle leggi vigenti, tenuto conto anche delle esigenze educative del minorenne.
3.	Si applicano, in quanto compatibili, le disposi- zioni di cui al Capo III della legge 24 novembre 1981,
n.	689, ad eccezione dell’articolo 59, e le funzioni attribuite all’ufficio di esecuzione penale esterna sono esercitate dai servizi minorili dell’amministrazione della  giustizia.
4.	Al compimento del venticinquesimo anno di età, se è in corso l’esecuzione di una pena sostitutiva, il magistrato di sorveglianza per i minorenni trasmette gli atti al magistrato di sorveglianza ordinario per la prosecuzione della pena, ove ne ricorrano le condizioni, con le modalità previste dalla legge 24 novembre 1981, n.  689.».
Art. 74.

Modifiche al decreto legislativo 28 luglio 1989, n.  272
1.	Al decreto legislativo 28 luglio 1989, n. 272, sono apportate le seguenti modificazioni:
a)	all’articolo 11, al comma 1 e nella rubrica le parole «e semidetenzione» sono soppresse;
b)	all’articolo 24, comma 1, la parola «sanzioni» è sostituita dalla seguente: «pene».
Art. 75.
Modifiche alla legge 28 aprile 2014, n. 67
1.	All’articolo 7 della legge 28 aprile 2014, n. 67, sono apportate le seguenti modificazioni:
a)	al comma 1, dopo le parole «del presente capo» sono inserite le seguenti: «e del decreto legislativo attuativo della legge 27 settembre 2021, n. 134» e le parole:
«Dipartimento dell’amministrazione penitenziaria» sono sostituite dalle seguenti: «Dipartimento per la giustizia minorile e di comunità»;
b)	al comma 2, dopo le parole «alla prova» sono ag- giunte le seguenti: «e di pene sostitutive delle pene deten- tive, nonché sullo stato generale dell’esecuzione penale esterna»;
c)	nella rubrica, le parole: «Dipartimento dell’amministrazione penitenziaria» sono sostituite dalle   seguenti:
«Dipartimento per la giustizia minorile e di  comunità».






«Art. 72
(Ipotesi di responsabilità penale e revoca)

Il condannato alla pena sostitutiva della semilibertà o della detenzione domiciliare che per più di dodici ore, senza giustificato motivo, rimane assente dall’istituto di pena ovvero si allontana da uno dei luoghi indicati nell’articolo 56 è punito ai sensi del primo comma dell’articolo 385 del codice penale. Si applica la disposizione del quarto comma dell’articolo 385 del codice penale.
Il condannato alla pena sostitutiva del lavoro di pubblica utilità che, senza giustificato motivo, non si reca nel luogo in cui deve svolgere il lavoro ovvero lo abbandona è punito ai sensi dell’articolo 56 del decreto legislativo 28 agosto 2000, n. 274.
La condanna a uno dei delitti di cui ai commi primo e secondo importa la revoca della pena sostitutiva, salvo che il fatto sia di lieve entità.
La condanna a pena detentiva per un delitto non colposo commesso durante l’esecuzione di una pena sostitutiva, diversa dalla pena pecuniaria, ne determina la revoca e la conversione per la parte residua nella pena detentiva sostituita, quando la condotta tenuta appare incompatibile con la prosecuzione della pena sostitutiva, tenuto conto dei criteri di cui all’articolo 58.
La cancelleria del giudice che ha pronunciato la sentenza di cui al quarto comma informa senza indugio il magistrato di sorveglianza competente per la detenzione domiciliare sostitutiva o per la semilibertà sostitutiva, ovvero il giudice che ha applicato il lavoro di pubblica utilità sostitutivo.»;
z)   l’articolo 75 è sostituito dal seguente:
«Art. 75
(Disposizioni relative ai minorenni)

Le disposizioni del presente Capo si applicano anche, in quanto compatibili, agli imputati minorenni. Si applica l’articolo 30 del decreto del Presidente della Repubblica 22 settembre 1988, n. 448.»;
aa) dopo l’articolo 75 è inserito il seguente:
«Art. 75-bis (Disposizioni relative ai reati militari)

Le disposizioni del presente Capo si applicano in quanto compatibili ai reati militari quando le prescrizioni risultano in concreto compatibili con la posizione soggettiva del condannato.»;
bb) l’articolo 76 è sostituito dal seguente:

«Art. 76
(Norme applicabili)

Alle pene sostitutive previste da questo Capo si applicano, in quanto compatibili, gli articoli 47, commi 12-bis, 51-bis, 51-quater e 53-bis, della legge 26 luglio 1975, n. 354.»;
cc) alla rubrica del Capo III, le parole: «Sanzioni sostitutive delle pene detentive brevi» sono sostituite dalle seguenti: «Pene sostitutive delle pene detentive brevi»;

dd) l’articolo 102 è sostituito dal seguente:
«Art. 102
(Conversione delle pene pecuniarie principali per mancato pagamento)

Il mancato pagamento della multa o dell’ammenda entro il termine di cui all’articolo 660 del codice di procedura penale ne comporta la conversione nella semilibertà sostitutiva.
Il ragguaglio si esegue a norma dell’articolo 135 del codice penale. In ogni caso la semilibertà sostitutiva non può avere durata superiore a quattro anni, se la pena convertita è quella della multa, e durata superiore a due anni, se la pena convertita è quella dell’ammenda.
Se è stato disposto il pagamento rateale, ai sensi dell’articolo 133-ter del codice penale, la conversione ha luogo per la parte residua della pena pecuniaria.
Il condannato può sempre far cessare l’esecuzione della semilibertà pagando la multa o l’ammenda, dedotta la somma corrispondente alla durata della pena da conversione espiata. A tal fine può essere ammesso al pagamento rateale, ai sensi dell’articolo 133-ter del codice penale.
ee) l’articolo 103 è sostituito dal seguente:
«Art. 103
(Mancato pagamento della pena pecuniaria per insolvibilità del condannato) Quando	le	condizioni	economiche	e	patrimoniali	del	condannato	al	momento dell’esecuzione rendono impossibile il pagamento della multa o dell’ammenda entro il termine di cui all’articolo 660 del codice di procedura penale, la pena pecuniaria è convertita nel lavoro di pubblica utilità sostitutivo ovvero, se il condannato si oppone, nella detenzione domiciliare sostitutiva.
Il ragguaglio si esegue in ogni caso a norma dell’articolo 135 del codice penale e un giorno di lavoro di pubblica utilità sostitutivo consiste nella prestazione di due ore di lavoro. In  ogni caso il lavoro di pubblica utilità sostitutivo e la detenzione domiciliare sostitutiva non possono avere durata superiore a due anni, se la pena convertita è la multa, e  durata superiore a un anno, se la pena convertita è l’ammenda.
Si applicano le disposizioni del terzo e del quarto comma dell’articolo 102.»; ff)  dopo l’articolo 103 sono inseriti i seguenti:
«Art. 103-bis
(Inapplicabilità delle misure alternative alla detenzione)

Le misure alternative alla detenzione, di cui al Capo VI del Titolo I della legge 26 luglio 1975 n. 354, non si applicano al condannato alla semilibertà sostitutiva o alla detenzione domiciliare sostitutiva, applicate a seguito della conversione della pena pecuniaria ai sensi del presente Capo.
Art. 103-ter (Disposizioni applicabili)

Alla semilibertà sostitutiva, alla detenzione domiciliare sostitutiva e al lavoro di pubblica utilità sostitutivo, quali pene da conversione della multa e dell’ammenda ai sensi del  presente Capo, si applicano, in quanto compatibili e non espressamente derogate, le disposizioni del Capo III della presente legge e le ulteriori disposizioni di legge, ovunque previste, che si riferiscono alle corrispondenti pene sostitutive.

Art. 103-quater (Disposizioni relative ai minorenni)

La pena pecuniaria, anche sostitutiva, applicata per un reato commesso da persona minore di età, in caso di mancato pagamento si converte nel lavoro di pubblica utilità sostitutivo, se vi è il consenso del minore non più soggetto ad obbligo di istruzione. Diversamente si converte nella detenzione domiciliare sostitutiva.
La durata della pena da conversione non può superare un anno, se la pena convertita è la multa, ovvero sei mesi, se la pena convertita è l’arresto. Tuttavia, in caso di insolvibilità del condannato la durata massima della pena da conversione non può superare sei mesi, se la pena convertita è la multa, ovvero tre mesi, se la pena convertita è l’arresto.
Si applicano, in quanto compatibili, gli articoli 71, 102 e 103, nonché l’articolo 103-ter. Si applica altresì, in quanto compatibile, l’articolo 660 del codice di procedura penale. Non si applica l’articolo 103-bis e il minore, nel corso dell’esecuzione della detenzione domiciliare sostitutiva, può essere affidato in prova al servizio sociale ai sensi del decreto legislativo 2 ottobre 2018, n. 121.»;
gg) l’articolo 107 è sostituito dal seguente:
«Art. 107
(Esecuzione delle pene conseguenti alla conversione della multa o dell’ammenda)

Per l’esecuzione della semilibertà sostitutiva, della detenzione domiciliare sostitutiva e del lavoro di pubblica utilità sostitutivo, quali pene conseguenti alla conversione della multa o dell’ammenda, si applicano gli articoli 62, 63, 64, 65, 68 e 69. Competente è il magistrato di sorveglianza, che provvede ai sensi dell’articolo 678, comma 1-bis, del codice di procedura penale.»;
hh) l’articolo 108 è sostituito dal seguente:






«Art. 108
(Inosservanza delle prescrizioni inerenti alle pene conseguenti alla conversione della multa o della ammenda)
La mancata esecuzione delle pene conseguenti alla conversione della pena pecuniaria, anche sostitutiva di una pena detentiva, ovvero la violazione grave o reiterata degli obblighi e delle prescrizioni ad esse inerenti, ne comporta la revoca e la parte residua si converte in uguale periodo di reclusione o di arresto, a seconda della specie della pena pecuniaria originariamente inflitta. La detenzione domiciliare e il lavoro di pubblica utilità, tuttavia, possono essere convertiti in altra pena sostitutiva più grave. Competente alla conversione è magistrato di sorveglianza, che provvede ai sensi dell’articolo 678, comma 1-bis, del codice di procedura penale. Si applicano, in quanto compatibili, il secondo e il terzo comma dell’articolo 66.
Si applicano le disposizioni di cui al primo e al secondo comma dell’articolo 72.»;

ART. 72
(Modifiche al decreto legislativo 28 agosto 2000, n. 274)
Al decreto legislativo 28 agosto 2000, n. 274, sono apportate le seguenti modificazioni:

all'articolo 29, al comma 4, le parole: «di mediazione di centri e strutture pubbliche o private presenti sul territorio» sono sostituite dalle seguenti: «dei Centri per la giustizia riparativa presenti sul territorio»;
dopo l’articolo 42 è inserito il seguente:
«Art. 42-bis (Esecuzione delle pene pecuniarie)

Le condanne a pena pecuniaria si eseguono a norma dell'articolo 660 del codice di procedura penale.»;
l’articolo 55 è sostituito dal seguente:
«Art. 55
(Conversione delle pene pecuniarie)

Per i reati di competenza del giudice di pace, la pena pecuniaria non eseguita per insolvibilità del condannato entro il termine di cui all’articolo 660 del codice di procedura penale si converte, a richiesta del condannato, in lavoro di pubblica utilità da svolgere per un periodo non inferiore ad un mese e non superiore a sei mesi con le modalità indicate nell'articolo 54.
Ai fini della conversione un giorno di lavoro di pubblica utilità equivale a 250 euro di pena pecuniaria.
Quando è violato l'obbligo del lavoro di pubblica utilità conseguente alla conversione della pena pecuniaria, la parte di lavoro non ancora eseguito si converte nell'obbligo di permanenza domiciliare secondo i criteri di ragguaglio indicati nel comma 5.
Se il condannato non richiede di svolgere il lavoro di pubblica utilità, ovvero se il mancato pagamento di cui al primo comma non è dovuto a insolvibilità, le pene pecuniarie non eseguite si convertono nell'obbligo di permanenza domiciliare con le forme e nei modi previsti dall'articolo 53, comma 1, e in questo caso non è applicabile al condannato il divieto di cui all'articolo 53, comma 3.

Ai fini della conversione un giorno di permanenza domiciliare equivale a 250 euro di pena pecuniaria e la durata della permanenza non può essere superiore a quarantacinque giorni.
Il condannato può sempre far cessare la pena del lavoro di pubblica utilità o della permanenza domiciliare pagando la pena pecuniaria, dedotta la somma corrispondente alla durata del lavoro prestato.».

ART. 73
(Modifiche al decreto del Presidente della Repubblica 22 settembre 1988, n. 448)
L’articolo 30 del decreto del Presidente della Repubblica 22 settembre 1988, n. 448, è sostituito dal seguente:
«Art. 30
(Pene sostitutive)

Con la sentenza di condanna il giudice, quando ritiene di dover applicare una pena detentiva non superiore a quattro anni, può sostituirla con la semilibertà o con la detenzione domiciliare, previste dalla legge 24 novembre 1981, n. 689; quando ritiene di dover applicare una pena detentiva non superiore a tre anni, può sostituirla, se vi è il consenso del minore non più soggetto ad obbligo di istruzione, con il lavoro di pubblica utilità previsto dalla legge 24 novembre 1981, n. 689; quando ritiene di doverla determinare entro il limite di un anno, può sostituirla, altresì, con la pena pecuniaria della specie corrispondente, determinata ai sensi dell’articolo 56-quater della legge 24 novembre 1981, n. 689. In ogni caso, nel sostituire la pena detentiva e nello scegliere la pena sostitutiva, il giudice tiene conto della personalità e delle esigenze di lavoro o di studio del minorenne nonché delle sue condizioni familiari, sociali e ambientali.
Il pubblico ministero competente per l'esecuzione trasmette l'estratto della sentenza al magistrato di sorveglianza per i minorenni del luogo di abituale dimora del condannato. Il magistrato di sorveglianza convoca, entro tre giorni dalla comunicazione, il minorenne, l'esercente la responsabilità genitoriale, l'eventuale affidatario e i servizi minorili dell’amministrazione della giustizia e provvede in ordine alla esecuzione della pena sostitutiva a norma delle leggi vigenti, tenuto conto anche delle esigenze.
Si applicano, in quanto compatibili, le disposizioni di cui al Capo III della legge 24 novembre 1981, n. 689, ad eccezione dell’articolo 59, e le funzioni attribuite all’ufficio di esecuzione penale esterna sono esercitate dai servizi minorili dell’amministrazione della giustizia.
Al compimento del venticinquesimo anno di età, se è in corso l’esecuzione di una pena sostitutiva, il magistrato di sorveglianza per i minorenni trasmette gli atti al magistrato di sorveglianza ordinario per la prosecuzione della pena, ove ne ricorrano le condizioni, con le modalità previste dalla legge 24 novembre 1981, n. 689.».

ART. 74
(Modifiche al decreto legislativo 28 luglio 1989, n. 272)

1.   Al decreto legislativo 28 luglio 1989, n. 272, sono apportate le seguenti modificazioni:

all’articolo 11, al comma 1 e nella rubrica le parole «e semidetenzione» sono soppresse;
all’articolo 24, comma 1, la parola «sanzioni» è sostituita dalla parola «pene».

ART. 75
(Modifiche alla legge 28 aprile 2014, n. 67)

1.   All’articolo 7 della legge 28 aprile 2014, n. 67, sono apportate le seguenti modificazioni:
al comma 1, dopo le parole «del presente capo» sono inserite le seguenti: «e del decreto legislativo attuativo della legge 27 settembre 2021, n. 134» e le parole: «Dipartimento dell’amministrazione penitenziaria» sono sostituite dalle seguenti: «Dipartimento per la giustizia minorile e di comunità»;
al comma 2, dopo le parole «alla prova» sono aggiunte le seguenti: «e di pene sostitutive delle pene detentive, nonché sullo stato generale dell’esecuzione penale esterna.»;
nella rubrica, le parole: «Dipartimento dell’amministrazione penitenziaria» sono sostituite dalle seguenti: «Dipartimento per la giustizia minorile e di comunità».

ART. 76
(Modifiche al codice penale militare di pace, approvato con regio decreto 20 febbraio 1941, n.
303)
Al codice penale militare di pace, approvato con regio decreto 20 febbraio 1941, n. 303, sono apportate le seguenti modifiche:
all'articolo 174, dopo il terzo comma, è aggiunto il seguente: «Non si applica l'articolo 131-bis del codice penale.»;
all'articolo 215, dopo il primo comma, è aggiunto il seguente: «Non si applica l'articolo 131-bis del codice penale.»;
dopo l’articolo 261-quater è inserito il seguente:
«Art. 261-quinquies
(Malfunzionamento dei sistemi informatici degli uffici giudiziari militari)
Il malfunzionamento dei sistemi informatici in uso presso gli uffici giudiziari militari è certificato dal responsabile della transizione al digitale del Ministero della difesa, attestato sul portale della Giustizia militare e comunicato dal dirigente dell’ufficio giudiziario, con modalità tali da assicurarne la tempestiva conoscibilità ai soggetti interessati. Il ripristino del corretto funzionamento è certificato, attestato e comunicato con le medesime modalità.
Le certificazioni, attestazioni e comunicazioni di cui al comma 1 contengono l’indicazione della data dell’inizio e della fine del malfunzionamento, registrate, in relazione a ciascun settore interessato, dal responsabile della transizione al digitale del Ministero della difesa.
Nei casi di cui ai commi 1 e 2, a decorrere dall’inizio e sino alla fine del malfunzionamento dei sistemi informatici, atti e documenti sono redatti in forma di documento analogico e depositati con modalità non telematiche, fermo quanto disposto dagli articoli 110, comma 4, e 111-ter, comma 4, del codice di procedura penale.

La disposizione di cui al comma 3 si applica, altresì, nel caso di malfunzionamento del sistema non certificato ai sensi del comma 1, accertato ed attestato dal dirigente dell’ufficio giudiziario, e comunicato con modalità tali da assicurare la tempestiva conoscibilità ai soggetti interessati della data di inizio e della fine del malfunzionamento.
Se la scadenza di un termine previsto a pena di decadenza si verifica nel periodo di malfunzionamento certificato ai sensi dei commi 1 e 2 o accertato ai sensi del comma 4, si applicano le disposizioni dell’articolo 175 del codice di procedura penale».


ART. 77
(Modifiche alla Legge 9 dicembre 1941, n. 1383)
1. Alla legge 9 dicembre 1941, n. 1383 all'articolo 3, dopo il terzo comma, è aggiunto il seguente: «Non si applica l'articolo 131-bis del codice penale.».


ART. 78
(Modifiche alla legge 26 luglio 1975, n. 354)
1.   Alla legge 26 luglio 1975, n. 354, sono apportate le seguenti modificazioni:
all’articolo 13, dopo il terzo comma è inserito il seguente: «Nei confronti dei condannati e degli internati è favorito il ricorso a programmi di giustizia riparativa.»;
dopo l’articolo 15 è inserito il seguente:
«Art. 15-bis (Giustizia riparativa)
In qualsiasi fase dell’esecuzione, l’autorità giudiziaria può disporre l’invio dei condannati e degli internati, previa adeguata informazione e su base volontaria, ai programmi di giustizia riparativa.
La partecipazione al programma di giustizia riparativa e l’eventuale esito riparativo sono valutati ai fini dell’assegnazione al lavoro all’esterno, della concessione dei permessi premio e delle misure alternative alla detenzione previste dal capo VI, nonché della liberazione condizionale. Non si tiene conto in ogni caso della mancata effettuazione del programma, dell’interruzione dello stesso o del mancato raggiungimento di un esito riparativo»;
all’articolo 47:
dopo il comma 3-bis, è inserito il seguente: «3-ter. L’affidamento in prova può altresì essere concesso al condannato alle pene sostitutive della semilibertà sostitutiva o della detenzione domiciliare sostitutiva previste dalla legge 24 novembre 1981 n. 689 quando, dopo l’espiazione di almeno metà della pena, abbia serbato un comportamento tale per cui l’affidamento in prova appaia più idoneo alla rieducazione del condannato e assicuri comunque la prevenzione del pericolo che egli commetta altri reati. Si applica l’ultimo comma dell’articolo 54. Il tribunale di sorveglianza procede ai sensi dell’articolo 678, comma 1-ter, del codice di procedura penale, in quanto compatibile.»;
al comma 12, dopo le parole «pene accessorie perpetue.» è inserito il seguente periodo: «A tali fini è valutato anche lo svolgimento di un programma di giustizia riparativa e l’eventuale esito riparativo.»; dopo le parole «in disagiate condizioni economiche» sono inserite le

seguenti:  «e  patrimoniali»  e  dopo  le  parole  «già  riscossa»  sono  aggiunte  le   seguenti:
«ovvero la pena sostitutiva nella quale sia stata convertita la pena pecuniaria non eseguita».

ART. 79
(Relazione annuale al Parlamento sullo stato dell’esecuzione delle pene pecuniarie)

Entro il 31 maggio di ciascun anno, il Ministro della giustizia riferisce alle competenti Commissioni parlamentari in merito all’attuazione del presente decreto in materia di esecuzione e conversione delle pene pecuniarie. Al fine di un compiuto monitoraggio, in funzione del raggiungimento degli obiettivi di effettività ed efficienza perseguiti dal presente decreto, i dati statistici relativi alle sentenze e ai decreti di condanna a pena pecuniaria,  anche sostitutiva, alla riscossione, alla rateizzazione, alla sospensione condizionale e alla conversione, per insolvenza o insolvibilità del condannato, alla estinzione per esito positivo dell’affidamento in prova al servizio sociale, ai sensi dell’articolo 47, comma 12, della legge 26 luglio 1975, n. 354, e alla prescrizione ai sensi degli articoli 172 e 173 del codice penale, sono pubblicati periodicamente sul sito del Ministero della giustizia e sono trasmessi annualmente al Parlamento, unitamente alla relazione di cui al precedente comma.


CAPO IV
Modifiche in materia di spese di giustizia

ART. 80
(Modifiche al decreto del Presidente della Repubblica 30 maggio 2002, n. 115)

Al decreto del Presidente della Repubblica 30 maggio 2002, n. 115, sono apportate le seguenti modificazioni:

all’articolo 1, comma 1, le parole «delle pene pecuniarie,» sono soppresse;
all’articolo 200, comma 1, le parole «delle pene pecuniarie,» sono soppresse;
all’articolo 211, comma 1, le parole «per le pene pecuniarie,» sono soppresse;
all’articolo 235:
al comma 1, le parole «e alle pene pecuniarie,» sono soppresse;
al comma 2, le parole «e delle pene pecuniarie» sono soppresse.

ART. 81
(Modifiche alla legge 24 dicembre 2007, n. 244)
1. All’articolo 1, comma 367, della legge 24 dicembre 2007, n. 244, le parole «e alle pene pecuniarie» sono soppresse.

CAPO V
Modifiche in materia di iscrizione nel casellario giudiziario

ART. 82
(Modifiche al decreto del Presidente della Repubblica 14 novembre 2002, n. 313)
All’articolo 3, comma 1, del decreto del Presidente della Repubblica 14 novembre 2002, n. 313, la lettera g) è sostituita dalla seguente: «g) i provvedimenti giudiziari definitivi di condanna alle sanzioni sostitutive e i provvedimenti di conversione di cui agli articoli 66, terzo comma, e 72, quarto comma, della legge 24 novembre 1981, n. 689;» e dopo la  lettera
g) è inserita la seguente: «g-bis) i provvedimenti di conversione di cui agli articoli 71, 102, 103 e 108 della legge 24 novembre 1981, n. 689, e di cui all’articolo 55 del decreto legislativo 28 agosto 2000, n. 274;».

Ai fini della conversione un giorno di permanenza domiciliare equivale a 250 euro di pena pecuniaria e la durata della permanenza non può essere superiore a quarantacinque giorni.
Il condannato può sempre far cessare la pena del lavoro di pubblica utilità o della permanenza domiciliare pagando la pena pecuniaria, dedotta la somma corrispondente alla durata del lavoro prestato.».

ART. 73
(Modifiche al decreto del Presidente della Repubblica 22 settembre 1988, n. 448)
L’articolo 30 del decreto del Presidente della Repubblica 22 settembre 1988, n. 448, è sostituito dal seguente:
«Art. 30
(Pene sostitutive)

Con la sentenza di condanna il giudice, quando ritiene di dover applicare una pena detentiva non superiore a quattro anni, può sostituirla con la semilibertà o con la detenzione domiciliare, previste dalla legge 24 novembre 1981, n. 689; quando ritiene di dover applicare una pena detentiva non superiore a tre anni, può sostituirla, se vi è il consenso del minore non più soggetto ad obbligo di istruzione, con il lavoro di pubblica utilità previsto dalla legge 24 novembre 1981, n. 689; quando ritiene di doverla determinare entro il limite di un anno, può sostituirla, altresì, con la pena pecuniaria della specie corrispondente, determinata ai sensi dell’articolo 56-quater della legge 24 novembre 1981, n. 689. In ogni caso, nel sostituire la pena detentiva e nello scegliere la pena sostitutiva, il giudice tiene conto della personalità e delle esigenze di lavoro o di studio del minorenne nonché delle sue condizioni familiari, sociali e ambientali.
Il pubblico ministero competente per l'esecuzione trasmette l'estratto della sentenza al magistrato di sorveglianza per i minorenni del luogo di abituale dimora del condannato. Il magistrato di sorveglianza convoca, entro tre giorni dalla comunicazione, il minorenne, l'esercente la responsabilità genitoriale, l'eventuale affidatario e i servizi minorili dell’amministrazione della giustizia e provvede in ordine alla esecuzione della pena sostitutiva a norma delle leggi vigenti, tenuto conto anche delle esigenze.
Si applicano, in quanto compatibili, le disposizioni di cui al Capo III della legge 24 novembre 1981, n. 689, ad eccezione dell’articolo 59, e le funzioni attribuite all’ufficio di esecuzione penale esterna sono esercitate dai servizi minorili dell’amministrazione della giustizia.
Al compimento del venticinquesimo anno di età, se è in corso l’esecuzione di una pena sostitutiva, il magistrato di sorveglianza per i minorenni trasmette gli atti al magistrato di sorveglianza ordinario per la prosecuzione della pena, ove ne ricorrano le condizioni, con le modalità previste dalla legge 24 novembre 1981, n. 689.».

ART. 74
(Modifiche al decreto legislativo 28 luglio 1989, n. 272)