---
uniqueName: problematicherilascioschedaintervento2023-33-v-2-0
displayName: "Problematiche rilascio Scheda Intervento 2023 33   v 2 0 signed"
category: "GENERAL"
tags: []
---

# Problematiche_rilascio_Scheda_Intervento_2023-33 - v.2.0_signed

> **File originale:** `MEV/SCHEDA_033/NOTE RILASCIO DGSIA/Problematiche_rilascio_Scheda_Intervento_2023-33 - v.2.0_signed.pdf`  
> **Tipo:** PDF

---

Problematiche rilascio scheda 2023 33 SIES PagoPA step 1 (prot. DGSIA n.206.E del 01.02.2024 e prot. 
RTI n. 20240130-001) 
 
 
 
Ministero della Giustizia 
Dipartimento per la transizione digitale della giustizia, l’analisi statistica         e le 
politiche di coesione 
  Direzione generale per i sistemi informativi automatizzati 
 
 
 
AP/ga/oo 
Allegati 
1. Allegato_m_dg.DOG07AR.01-02-2024.0000206.E_20240130-001-SIES-Scheda_2023-33-Cartabi.pdf; 
2. SIUT-SIES-PR-1.0-20240130-Piano_di_Rilascio_2023_33_PST_PagoPA_Step-1.docx. 
3. SIUT-SIES-CT-1.0-20240130-Allegato_al_piano_Test_2023_33_PST_PagoPA_Step-1.xlsx; 
4. SIUT-SIES-MU-1.0-20240130-Manuale_Utente_2023_33_PST_PagoPA_Step-1.docx. 
 
 
               Spett.le 
                 Engineering Ingegneria Informatica  
                      S.p.A Piazzale dell’Agricoltura 24  
00144 Roma    
 
       E p.c. 
 
Al RUP ing. Aurora Garofalo 
 
 
 
 
Oggetto: Gara informale ex art. 162 d.lgs. 50/2016 per l’affidamento dello sviluppo del sistema  
informativo unitario telematico del processo penale e per la manutenzione e diffusione degli 
attuali sistemi dell’area penale del Ministero della Giustizia e servizi correlati ex art 162 d.lgs. 
50/2016.SIA 106.1.B.EV.S.23/19P. Lotto 1 - CIG 73479643B7 – CUP J51C1700050001 – 
Problematiche rilascio scheda 2023 33 SIES PagoPA step 1 (prot. DGSIA n.206.E del 01.02.2024 e 
prot. RTI n. 20240130-001). 
 
Con riferimento alla scheda in oggetto, si rileva che il rilascio comunicato con pronti al 
collaudo (prot. DGSIA n.206.E del 01.02.2024 e prot. RTI n. 20240130-001) presenta le seguenti 
problematiche derivanti da una prima analisi da parte del gruppo di lavoro e pertanto non posso 
essere considerate esaustive:

Problematiche rilascio scheda 2023 33 SIES PagoPA step 1 (prot. DGSIA n.206.E del 01.02.2024 e prot. 
RTI n. 20240130-001) 
- 
I controlli eseguiti sul documento (allegato 2) fino a pagina 11 hanno rilevato alcune 
frasi non corrette, che sono state evidenziate in rosso e che riguardano la versione di 
partenza (12.5.6.0); 
 
- 
la numerazione di questo rilascio avrebbe dovuto essere 12.5.6.0+MEV_2023_33 (o 
similare); occorre correggere il file “aggiorna_versione.sql”; 
 
- 
Per quanto attiene il piano di test (allegato 3), si osserva che, essendo stato modificato il 
batch (vedi documento dei requisiti), occorre inserire un test per verificarne di nuovo il 
funzionamento (come fatto per la MEV 2023-13); 
 
- 
Per quanto riguarda il manuale utente (allegato 4)  non è chiaro il motivo per cui sia 
stata consegnata la versione 1.0 del manuale utente riferita a questa MEV, in quanto la 
scheda 2023-33 infatti non nasce da sola ma parte dal contesto della MEV 2023-13 
modificando/integrando/aggiungendo funzioni.  La MEV 2023-33, cioè, è la naturale 
prosecuzione della MEV 2023-13, pertanto il manuale utente deve seguire la stessa 
strada di modifica, integrazione e revisione, indicando, come usuale, le modifiche 
apportate. Si deve partire dal manuale utente esistente ed aggiornarlo di conseguenza. 
Inoltre, sempre per quanto riguarda il l’allegato 4, occorre eliminare la parte riferita 
all’utente amministratore ed occorre consegnare versione aggiornata del manuale di 
amministratore. 
 
- 
La procedura “aggiorna_db.sh” produce il seguente errore:

Problematiche rilascio scheda 2023 33 SIES PagoPA step 1 (prot. DGSIA n.206.E del 01.02.2024 e prot. 
RTI n. 20240130-001) 
Si chiede, pertanto, di aggiornare correttamente la documentazione, come da indicazioni, e 
fornire una versione funzionante della procedura “aggiorna_db.sh” e file collegati. 
 
Ulteriori osservazioni potranno essere inviate all’esito della verifica della nuova consegna.  
Il Direttore dell’Csecuzione 
                                                                 
   Dott. Oris Orlando 
 
 
 
 
ORLANDO ORIS
MINISTERO
DELLA GIUSTIZIA
08.02.2024
13:13:37
GMT+01:00