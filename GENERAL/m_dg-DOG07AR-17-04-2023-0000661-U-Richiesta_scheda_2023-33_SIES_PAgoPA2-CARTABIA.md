---
uniqueName: mdg-dog07ar-17-04-2023-0000661-u-richiestascheda20
displayName: "m dg DOG07AR 17 04 2023 0000661 U Richiesta scheda 2023 33 SIES PAgoPA2 CARTABIA"
category: "GENERAL"
tags: []
---

# m_dg.DOG07AR.17-04-2023.0000661.U.Richiesta_scheda_2023-33_SIES_PAgoPA2-CARTABIA_signed (3)

> **File originale:** `MEV/SCHEDA_033/NOTE RILASCIO DGSIA/m_dg.DOG07AR.17-04-2023.0000661.U.Richiesta_scheda_2023-33_SIES_PAgoPA2-CARTABIA_signed (3).pdf`  
> **Tipo:** PDF

---

Richiesta scheda 2023-33 - SIES - interventi Cartabia e pagoPA fase 2 
 
Ministero della Giustizia 
Dipartimento per la transizione digitale della giustizia,  
l’analisi statistica e le politiche di coesione 
  Direzione generale per i sistemi informativi automatizzati 
 
 
AP/ga/oo 
Livello di Riservatezza:  L3 
Ambito: 
RTI Engineering sirfin Pa 
Area penale 
Allegati 
 
               Spett.le 
         Engineering Ingegneria Informatica S.p.A.  
Piazzale dell’Agricoltura24  
00144 Roma    
 
       e p.c. 
Al RUP ing. Aurora Garofalo 
   
 
Oggetto: Gara informale ex art. 162 d.lgs. 50/2016 per l’affidamento dello sviluppo del sistema  
informativo unitario telematico del processo penale e per la manutenzione e diffusione degli 
attuali sistemi dell’area penale del Ministero della Giustizia e servizi correlati ex art 162 d.lgs. 
50/2016.SIA 106.1.B.EV.S.23/19P. Lotto 1 - CIG 73479643B7 – CUP J51C1700050001 – Richiesta 
scheda 2023-33 - SIES - interventi Cartabia e pagoPA fase 2   
 
Con riferimento al contratto in oggetto, si richiede la seguente scheda di intervento 
entro il 12.06.2023: 
 
 
Scheda di Intervento  
2023-33 
Oggetto  
SIES: interventi Cartabia e pagoPA fase 2   
Complessità  
Alta 
Servizio  
MEV  
 
 
Premessa: 
Preso atto della realizzazione eseguita con la scheda 2023/13 SIES-PagoPA, si chiede la 
realizzazione di quanto lasciato in sospeso al fine di concludere il flusso di lavoro.

Richiesta scheda 2023-33 - SIES - interventi Cartabia e pagoPA fase 2 
Applicativi:  
SIES – sottosistemi SIEP-SIUS-SIGE 
 
 
Uffici interessati dalla modifica:  
Uffici utilizzatori del SIEP-SIUS-SIGE  
 
 
Requisiti funzionali: 
 
Lato SIEP:  
Completamento della versione   Riscossione Pene Pecuniarie 
Il sistema consegnato con la scheda 2023-13 va integrato con le seguenti modifiche:   
➢ Template 
− Rivedere tabella posizioni giuridiche che deve comprendere solamente due valori: 
o Libero  
o Detenuto in istituto per qualsiasi titolo 
− Completamento template ingiunzione: 
Quelli attualmente prodotti dall’applicativo vanno integrati nella parte dispositiva con la 
disposizione del giudice sulla tipologia di pagamento, unica soluzione rate mensili.  
− Modifica di alcuni template in uso con integrazione del testo in modo specifico sulla 
legge Cartabia. 
➢ Gestione ordine di ingiunzione 
Attualmente si riesce ad annotare solamente la notifica ai soli difensore e condannato. 
Vanno realizzate le seguenti funzioni:  
o Notifiche (già realizzata) 
o Rinnovo ricerche per Omessa notifica 
o Richieste informazione 
o Rinnovazione notifiche 
o Irreperibilità? 
o Solleciti 
➢ Gestione civilmente obbligato 
o Gestione difensore  
o Annotazione notifiche 
o Generazione template 
o Emissione ordine ingiunzione di pagamento (prima notifica)

Richiesta scheda 2023-33 - SIES - interventi Cartabia e pagoPA fase 2 
o Emissione ingiunzione dopo ordinanza Magistrato sorveglianza  
o Emissione bollettini Pagamento 
➢ Scadenzari gestione delle pene sostitutiva pecuniaria 
o Gestione scadenza pagamento prima rata suddiviso: 
▪ Rata unica (evidenziando la scadenza intermedia 20 gg) 
▪ Pagamento rateale 
▪  
➢ Generazioni Avvisi PagoPA 
o Adattamento dei modelli in base alla tipologia di pagamento; 
o Pagamento rateale: Possibilità di stampa di tutti i modelli in un'unica azione, 
lasciando la stampa singola; 
o Generazione di un modulo istruzioni e modalità di pagamento per il 
condannato; 
o Modalità di sostituzione modelli a seguito di emissione ordine di ingiunzione, 
errore materiale, emissione provvedimento di cumulo; 
o Emissione bollettini Pagamento per civilmente obbligato (dopo decisione mds) 
o Emissione nuovo bollettino dopo mancato pagamento Rata., 
➢ Scadenzari gestione delle pene sostitutiva pecuniaria 
Scadenzario dopo notifica Ingiunzione; lo scadenziario si deve attivare ad ogni emissione 
di ordine di ingiunzione, che, come vedremo di seguito sono diversi. 
 
o Gestione scadenza pagamento prima rata suddiviso: 
▪ Rata unica (evidenziando la scadenza intermedia (20 gg) 
▪ Pagamento rateale 
o Scadenziario scadenze rate (dopo notifica Ingiunzione)  
▪ Dopo notifiche ingiunzione (il sistema deve calcolare la data di scadenza 
delle rate per le due tipologie di pagamento. 
o Scadenziario verifica stato pagamenti per date  
▪ Verifica avvenuto pagamento (estinzione del debito)   
▪ Verifica mancato pagamento (scadenza rate) 
 
➢ Gestione provvedimenti successivi 
• Mancato pagamento di una delle rate 
Il mancato pagamento, di una delle rate comporta la decadenza del beneficio del 
pagamento rateale, comporta l’emissione di un nuovo ordine di ingiunzione  per la 
residua  somma non pagata.

Richiesta scheda 2023-33 - SIES - interventi Cartabia e pagoPA fase 2 
o Emissione di un nuovo ordine di ingiunzione - Si ripete tutta la gestione con i nuovi 
termini; 
 
➢ Gestione del procedimento avvenuto/ mancato pagamento 
gestione del flusso di avvenuto pagamento della sanzione pecuniaria con trasmissione 
all’ufficio competente (sorveglianza) nei casi di avvenuto/mancato pagamento 
• Accertamento avvenuto pagamento 
Creazione maschera per l’emissione del provvedimento di estinzione pena 
o Emissione provvedimento di estinzione pena 
o Redazione foglio complementare casellario 
o Trasmissione foglio al casellario 
o Definizione procedimento  
 
• Mancato pagamento della pena pecuniaria 
Il mancato pagamento della pena pecuniaria, entro il termine indicato nell'ordine di 
esecuzione, il pubblico ministero trasmette gli atti al magistrato di sorveglianza. 
Vanno create le seguenti funzioni 
o trasmissione atti al magistrato di sorveglianza competente 
o Verifica esito trasmissioni atti per Competenza” 
o Riscontro trasmissione - annotazione della presa in carico   
 
➢ Creazione di un cruscotto di monitoraggi scadenze 
 
 
➢ DECISIONI MAGISTRATURA DI SORVEGLIANZA 
 
Importante  
Va creata una nuova funzione per lo scambio dati in elettronico automatizzato. 
È necessario, dopo l’emissione del provvedimento, che il sistema autonomamente 
trasmetta in elettronico il provvedimento alla Procura competente per l’esecuzione. 
In alternativa dare la possibilità alla procura di importare il dato.  
Ad oggi, benché esista la funzione, da fuori distretto arriva solamente un 5% di 
provvedimenti. 
 
➢ Gestione provvedimenti magistratura di sorveglianza e gestione del PM.  
Tutte le decisioni vanno concordati con la sorveglianza.  
➢ Annotazione differimento della conversione 
▪ PM -Prevedere scadenzari differimento conversione 
▪ PM - funzione accertamento scadenza 
➢ Comunicazione ordine di pagamento civilmente obbligato 
▪ PM – emissione ordine ingiunzione civilmente obbligato  
▪ PM – emette bollettino di pagamento 
➢ Ammissione al Pagamento rateale 
▪ PM – emissione ordine ingiunzione pagamento 
▪ PM – emette bollettino di pagamento 
➢ Conversione della pena pecuniaria in pena sostitutiva breve

Richiesta scheda 2023-33 - SIES - interventi Cartabia e pagoPA fase 2 
o PM –Annotare la decisione: 
- 
Semilibertà sostitutiva 
- 
Detenzione domiciliare sostitutiva 
- 
Lavoro pubblica utilità sostitutivo (Trasmissione atti al 
giudice) 
▪ PM –annota ordinanza  
 
➢ Revoca delle pene sostitutive per inosservanza delle prescrizioni  
le pene conseguenti alla conversione della pena pecuniaria, anche sostitutiva di una pena 
detentiva comporta la revoca e la parte residua si converte in uguale periodo di reclusione 
o di arresto. 
➢ Revoca per inosservanza della prescrizione  
o Revoca pena sostitutiva e ripristino pene detentiva 
o PM – annotazione conversione 
o PM – emette ordine di esecuzione 
 
➢ Sospensione dell'esecuzione delle pene sostitutive). 
Prevedere la sospensione dell’esecuzione delle pene sostitutive in caso di esecuzione di 
pene detentive o l'esecuzione, anche provvisoria, di misure di sicurezza detentive e corso 
della custodia cautelare, la sospensiva va fatta anche in caso di cumulo con pene detentive 
 
o Emissione provvedimento di sospensione Apposito 
 
➢ SANZIONI DEL GIUDICE DI PACE 
Iscrizione procedimento 
Il pubblico ministero e l’autorità predisposta all’esecuzione delle pene del giudice di pace. 
L’iscrizione del titolo esecutivo è già prevista in classe ed occorre trascrivere le sanzioni 
applicate: 
➢ pena principale  
o pena pecuniaria 
o Permanenza domiciliare 
o Lavoro di pubblica utilità 
o Espulsione dallo stato 
➢ Pena sostitutiva 
Pena pecuniaria sostitutiva 
La procedura per la riscossione della pena pecuniaria è identica alla procedura sopra 
descritta ad eccezione della procedura di conversione che prevede che la pena pecuniaria non 
eseguita per insolvibilità del condannato entro il termine di cui all'articolo 660 del codice di 
procedura penale indicato nell'ordine di ingiunzione.  
Il sistema deve prevedere l’iscrizione delle sanzioni del giudice di pace 
o Emissione di ordine di ingiunzione per sanzione gdp 
o Generazione bollettino di pagamento 
La procedura è identica a quella appena descritta in precedenza.

Richiesta scheda 2023-33 - SIES - interventi Cartabia e pagoPA fase 2 
➢ Trasmissione atti al magistrato di sorveglianza per conversione 
 
➢ Mancato pagamento trasmissione atti alla sorveglianza per conversione 
➢ Conversione della pena pecuniaria in pena sanzioni del giudice di pace 
o PM –Annotare la decisione: 
▪ Lavoro pubblica utilità 
▪ Permanenza domiciliare 
o PM –emettere provvedimenti per l‘esecuzione 
Il sistema deve prevedere l’emissione dei provvedimenti per l’esecuzione delle sanzioni 
 
➢ Violazione obblighi lavoro pubblica utilità. 
▪ PM trasmetta atti magistrato sorveglianza 
o Conversione in permanenza domiciliare 
▪ PM –Annotare la decisione: 
▪ PM –emettere provvedimenti per l‘esecuzione 
 
- 
Pagamento spontaneo della pena pecuniaria 
Il condannato può sempre far cessare la pena del lavoro di pubblica utilità o della permanenza 
domiciliare pagando la pena pecuniaria, dedotta la somma corrispondente alla durata della 
pena da conversione espiata.». 
 
 
➢ Provvedimento di computo della pena espiata  
È necessario creare la procedura per computare i periodi di pena individuando il valore 
giornaliero applicato dal giudice nel determinare la pena sostitutiva pecuniaria 
tutta le tipologie e quantitativi di pena e quantitativi di applicazione 
▪ Pm Computo della residua pena da espiare (secondo la tipologia di pena) 
▪ Pm emissione di nuovo ordine di pagamento. 
 
➢ PENE SOSTITUTIVE DELLE PENE DETENTIVE BREVI 
- 
 
La riforma delle pene sostitutive delle pene detentive brevi applicate dal giudice di 
cognizione in sentenza di condanna sono le seguenti:  
 
- 
La Semilibertà Sostitutiva;  
- 
La Detenzione Domiciliare Sostitutiva;  
- 
Il Lavoro Di Pubblica Utilità Sostitutivo;  
- 
La Pena Pecuniaria Sostitutiva.  
La maschera per l’iscrizione è già stata realizza  
Occorre creare la maschera per l’iscrizione delle sanzioni del giudice di pace che 
sono: 
- 
Pena pecuniaria 
- 
Permanenza in casa 
- 
Lavoro di pubblica utilità 
- 
Espulsione 
 
 
➢ Gestione delle pene sostitutive brevi 
o Esecuzione della semilibertà

Richiesta scheda 2023-33 - SIES - interventi Cartabia e pagoPA fase 2 
o detenzione domiciliare sostitutive 
PM – emette provvedimento( in base alla posizione giuridica) 
▪ PM - Trasmette copia della sentenza al magistrato di 
sorveglianza 
 
➢ Emissione ordinanza di conferma delle prescrizioni 
• Pm annota ordinanza ed emette  
 
➢ Esecuzione di pene sostitutive concorrenti 
o Creazione delle maschere per inserire le pene sostitutive 
o Gestione delle pene 
o Prevedere un provvedimento di cumulo separato 
▪ Pene pecuniarie pre cartabia 
▪ Pene pecuniarie sostitutive.  
 
➢ Registro istanze Creazione di nuovi contenuti e Gestione 
o Art. 133-ter. (Pagamento rateale della multa o dell'ammenda 
o Art. 55 (Conversione delle pene pecuniarie). Gdp 
o Istanza di conversione pena  pecuniaria il lavoro di pubblica utilità (GdP) 
 
➢ Template 
➢ Estrazione dati 
 
Lato SIGE 
 
➢ Template – fissazione udienza 
È necessario modificare la dicitura presente nell’attuale documento per adeguarlo alla 
nuova normativa. 
o Vecchia frase 
AVVERTE 
il condannato detenuto: 
➢ in luogo posto nella circoscrizione del Giudice che può chiedere la traduzione 
all’udienza; 
➢ in luogo posto fuori della circoscrizione del Giudice, che, se ne farà richiesta, sarà 
sentito, prima del giorno dell’udienza dal Magistrato di Sorveglianza del luogo di 
detenzione, salvo che il Giudice dell’esecuzione, non ne disponga d’ufficio la 
traduzione.  
o Nuova frase prevista dall’art art. 666, comma 4 c.p.p. 
 
AVVERTE 
il condannato detenuto: 
_in luogo posto nella circoscrizione del Giudice che può chiedere la traduzione all’udienza_; 
L'interessato che ne fa richiesta è sentito personalmente.  A tal fine si procede   mediante 
collegamento a distanza, quando una particolare disposizione di legge lo prevede o quando 
l’interessato vi consente.  Tuttavia, se è detenuto o internato in luogo posto fuori della

Richiesta scheda 2023-33 - SIES - interventi Cartabia e pagoPA fase 2 
circoscrizione del giudice e non consente all’audizione mediante   collegamento   a distanza, 
l'interessato è sentito prima del giorno dell’udienza dal magistrato di  sorveglianza  del  luogo,  
salvo  che  il  giudice ritenga di disporre la traduzione 
.  
➢ Integrazione tabelle oggetti  
− art. 95 disposizioni transitorie in materia di pene sostitutive delle pene detentive 
brevi 
o contenuto:  
o applicazione pene sostitutive delle pene detentive brevi art. 95. D.lgs. 150/22 
oggetto 
- 
Applicazione della pena in semilibertà sostitutiva;   
- 
Applicazione della pena in detenzione domiciliare sostitutiva; 
- 
Applicazione della pena il lavoro di pubblica utilità sostitutivo; 
- 
Applicazione della pena la pena pecuniaria sostitutiva. 
 
Decisioni/Esito 
a) applicazione della Pena sostitutiva breve 
b) rigetta l’istanza; 
c) dichiara il non luogo a provvedere; 
d) dichiara il non doversi procedere; 
e) dichiara l’inammissibilità; 
f) dichiara la propria la propria incompetenza. 
 
− riduzione pena art. 442, comma 2-bis - D.lgs. 150/22 
contenuto 
o riduzione della pena articolo 442, comma 2-bis. 
Decisione/esito 
a) 
applica riduzione pena; 
b) 
rigetta l’istanza; 
c) 
dichiara il non luogo a provvedere; 
d) 
dichiara il non doversi procedere; 
e) 
dichiara l’inammissibilità; 
f) 
dichiara la propria la propria incompetenza. 
 
➢ Risoluzione problematica ricorso per cassazione 
La mancata classificazione dell’attività comporta un’errata estrazione dati 
 
➢ Estrazione dati 
o Ampliare estrazione dati  
▪ Esempio di tipologia elaborazioni    
− Da ricezione a iscrizione  
− Da iscrizione a provvedimento

Richiesta scheda 2023-33 - SIES - interventi Cartabia e pagoPA fase 2 
− Da ultima udienza a provvedimento 
− Da provvedimento a deposito ricorso\opposizione  
− Da data richiesta atti istruttori a prevedimento atto 
− Da data presentazione ricorso a trasmissione  atti 
 
 
Requisiti generali 
- Creazione di un cruscotto di gestione degli errori di collegamento con PST-PagoPA.  
Il cruscotto dovrà essere accessibile tramite opportuna profilazione, e dovrà prevedere anche 
l’attivazione on demand del collegamento con PST-PagoPA. 
- Controllo delle attribuzioni ai profili preimpostati del SIES per le funzioni realizzate con la 
scheda 2023/13 SIES-PagoPA. Inoltre, nella realizzazione delle funzioni richieste, si dovrà 
tenere conto della corretta attribuzione ai profili. 
- Nella realizzazione delle funzioni richieste si deve prevedere l’allineamento dei sottosistemi 
ai fini della reciproca interoperabilità. 
- Nella realizzazione delle funzioni richieste si deve considerare anche l’eventuale impatto con 
il sistema SIUS-Avvocati 
- Nella realizzazione delle funzioni richieste si considerare anche l’eventuale impatto con il 
sistema del Casellario. 
  
Il Direttore dell’Esecuzione 
                                                                       Dott. Oris Orlando 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
ORLANDO ORIS
MINISTERO
DELLA GIUSTIZIA
17.04.2023
11:36:33
GMT+02:00