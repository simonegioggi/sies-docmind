---
uniqueName: richiestascheda2023-13app-siespagopav1-0signed
displayName: "Richiesta scheda 2023 13 APP SIES PAGOPA v 1 0 signed"
category: "GENERAL"
tags: []
---

# Richiesta_scheda_2023-13_APP-SIES_PAGOPA_v_1.0_signed

> **File originale:** `MEV/SCHEDA_013/Docs/Richiesta_scheda_2023-13_APP-SIES_PAGOPA_v_1.0_signed.pdf`  
> **Tipo:** PDF

---

Richiesta scheda 2023-13 – APP/SICP/SIES – pagamenti PagoPA per pene pecuniarie 
 
Ministero della Giustizia 
Dipartimento per la transizione digitale della giustizia,  
l’analisi statistica e le politiche di coesione 
  Direzione generale per i sistemi informativi automatizzati 
 
 
AP/dlv/oo 
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
Al RUP ing. Vincenzo De Lisi 
   
 
Oggetto: Gara informale ex art. 162 d.lgs. 50/2016 per l’affidamento dello sviluppo del sistema  
informativo unitario telematico del processo penale e per la manutenzione e diffusione degli 
attuali sistemi dell’area penale del Ministero della Giustizia e servizi correlati ex art 162 d.lgs. 
50/2016.SIA 106.1.B.EV.S.23/19P. Lotto 1 - CIG: 73479643B7 – CUP: J51C1700050001 – Richiesta 
scheda 2023-13 – APP/SICP/SIES – pagamenti PagoPA per pene pecuniarie 
 
Con riferimento al contratto in oggetto, si richiede la seguente scheda di intervento. 
Nonostante i tempi contrattuali, in base alla complessità della scheda, prevederebbero un 
rilascio della stessa entro il 21.03.2023, si chiede di anticipare i tempi in quanto la 
funzionalità deve entrare in esercizio alla fine di marzo 2023. 
 
 
Scheda di Intervento  
2023-13 
Oggetto  
APP/SICP/SIES – pagamenti PagoPA per 
pene pecuniarie 
Complessità  
media 
Servizio  
MEV

Richiesta scheda 2023-13 – APP/SICP/SIES – pagamenti PagoPA per pene pecuniarie 
Premessa: 
Si trasmettono i requisiti relativi per rendere operative le previsioni degli artt. 460 e 660 c.p.p. 
rispettivamente per cognizione ed esecuzione. Allo stesso modo si chiede di implementare le medesime 
funzionalità in relazione ai casi di pagamento dell’oblazione (ex art. 162 c.p.). 
 
Applicativi:  
Work Flow Manager (WFM) - da rinominarsi in Applicativo Area Penale (APP) - RegeWeb/SICP – 
SIES. 
 
Uffici interessati dalla modifica:  
tutti gli uffici requirenti e giudicanti di primo grado 
  
Requisiti funzionali: 
 
Servizi PST da interfacciare: 
A. 
Invocare un servizio per la generazione del Bollettino (quando viene creato un  
bollettino viene in automatico generato uno stato ad esso associato, identificativo 
IUV); 
B. 
Invocare un servizio per avere aggiornamenti sullo stato del bollettino. 
 
Flusso: 
1) 
Generazione bollettino (Sistema Penale → PST): Quando viene generato un atto 
esecutivo o provvedimento del giudice con obbligo di pagamento, o altri eventi (ad 
esempio proroga di un pagamento scaduto) sarà possibile effettuare l’azione 
“Genera Bollettino”, richiamando il servizio del PST che genera il bollettino di 
pagamento e eventualmente anche quello rateizzato. Il servizio del PST restituisce il 
bollettino e lo IUV che lo identifica univocamente; 
2) 
Il sistema penale mostrerà all’utente cancelliere un record con le informazioni 
opportune (IUV, scadenza, stato, link al pdf); 
3) 
Tasto STAMPA: l’utente dovrà poter stampare il bollettino, contenente altresì le 
informazioni relative al procedimento e al titolo di pagamento, che verrà notificato 
al destinatario finale che dovrà procedere al pagamento (online o presso qualsiasi 
sportello); 
4) 
Aggiornamento STATO (Sistema Penale → PST): il sistema penale invocherà il 
servizio del PST (una volta al giorno) per aggiornare lo stato del pagamento. Infatti, 
quando verrà effettuato il pagamento il PST (collegandosi a PagoPA) si aggiorna di 
conseguenza; 
5) 
I sistemi penali verranno aggiornati in base allo stato del pagamento, ed alla 
scadenza andrà scatenata un’azione (alert o simili) di notifica sul sistema.

Richiesta scheda 2023-13 – APP/SICP/SIES – pagamenti PagoPA per pene pecuniarie 
 
 
Note: 
• 
Se il pagamento scade non è più possibile pagarlo, ed in caso di proroga da parte del 
giudice sarà necessario generare un nuovo bollettino, in questo caso riabilitando il 
tasto “Genera Bollettino”. Questo dovrà accadere anche in caso di rate non pagate 
totalmente. Va considerato il caso di pagamento parziale con relative tracciamento. 
• 
Successivamente all’invio della presente richiesta di scheda l’Amministrazione 
provvederà ad inviare al RTI la lista degli atti coinvolti.  
 
Il Direttore dell’Esecuzione 
                                                                       Dott. Oris Orlando 
 
 
ORLANDO ORIS
MINISTERO
DELLA GIUSTIZIA
14.02.2023
13:35:31
GMT+01:00