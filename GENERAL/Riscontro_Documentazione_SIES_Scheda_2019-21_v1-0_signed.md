---
uniqueName: riscontrodocumentazionesiesscheda2019-21v1-0signed
displayName: "Riscontro Documentazione SIES Scheda 2019 21 v1 0 signed"
category: "GENERAL"
tags: []
---

# Riscontro_Documentazione_SIES_Scheda_2019-21_v1.0_signed

> **File originale:** `MEV/SCHEDA_021/Docs/Riscontri DGSIA/2022_docs_errori/Riscontro_Documentazione_SIES_Scheda_2019-21_v1.0_signed.pdf`  
> **Tipo:** PDF

---

Via Crescenzio 17/C Roma - prot.dgsia.dog@giustiziacert.it – protocollo.dgsia@giustizia.it 
 
Ministero della Giustizia 
Dipartimento dell’organizzazione giudiziaria, del personale e dei servizi 
  Direzione generale per i sistemi informativi automatizzati 
 
 
AP/mg/oo 
 
               Spett.le 
                 Engineering Ingegneria Informatica  
                      S.p.A Piazzale dell’Agricoltura 24  
00144 Roma    
 
       E p.c. 
 
Al RUP ing. Giovanni Malesci                   
 
 
 
   
        
Oggetto: Gara informale ex art. 162 d.lgs. 50/2016 per l’affidamento dello sviluppo del sistema  
informativo unitario telematico del processo penale e per la manutenzione e diffusione degli attuali  
sistemi dell’area penale del Ministero della Giustizia e servizi correlati ex art 162 d.lgs. 
50/2016.SIA 106.1.B.EV.S.23/19P. Lotto 1 - CIG: 73479643B7 – CUP: J51C1700050001 – Scheda 
2019 21 SIES REGINDE – Richiesta aggiornamento documentazione 
 
 
Atteso che l’Amministrazione deve poter diffondere in esercizio la MEV in oggetto, a seguito di 
verifiche interne svolte sulla fruibilità della documentazione tecnica, si chiede di apportare alcune modifiche 
a quest’ultima per consentire alle strutture addette di procedere senza difficoltà. 
 
A seguire si elencano i punti che richiedono intervento: 
 
Osservazioni su “SIUT-SIES-PR-1.3-20220422-Piano_di_Rilascio_021_RegInde_SIES” e su “SIUT-
SIES-MG-1.4-20220525-Istruzioni_Bonifica_Difensori_021_RegInde”: 
1) IN GENERALE: occorre che i documenti correlati tra loro siano coerenti, cioè se in un 
documento viene referenziato un altro documento occorre che sia citato il nome corretto. 
Esempio: a p. 10 del “SIUT-SIES-PR-1.3-20220422-Piano_di_Rilascio_021_RegInde_SIES”, si 
rimanda al documento “SIUTSIES- MG-1.3-20220422-
Istruzioni_Bonifica_Difensori_021_RegInde_SIES.docx,” che è obsoleto. L’attuale documento, 
infatti, è “SIUT-SIES-MG-1.4-20220525 Istruzioni_Bonifica_Difensori_021_RegInde”

Via Crescenzio 17/C Roma - prot.dgsia.dog@giustiziacert.it – protocollo.dgsia@giustizia.it 
2 
 
2) IN GENERALE: occorre che siano referenziati correttamente i paragrafi da prendere in 
considerazione. 
Esempio: a p. 10 del “SIUT-SIES-PR-1.3-20220422-Piano_di_Rilascio_021_RegInde_SIES”, si 
cita il paragrafo 3.3.7 di un altro documento, ma tale paragrafo non esiste. 
3) Occorre definire la versione di riferimento; “nel documento 
SIUT-SIES-PR-1.3-20220422-Piano_di_Rilascio_021_RegInde_SIES” è indicata la 12.4.18.0 
che ormai è obsoleta. 
 
Osservazioni su “SIUT-SIES-MG-1.4-20220525-Istruzioni_Bonifica_Difensori_021_RegInde”: 
1) Controllare l’indice: il numero di pagine indicato nell’indice arriva fino a 61 mentre il documento è 
composta da 39 pagine. IN GENERALE: l’osservazione vale per ogni documento. 
2) Controllare il numero di pagine nel pié di pagina. IN GENERALE: l’osservazione vale per ogni 
documento. 
3) Punto 9 pagina 9: esplicitare cosa significhi XX in SIESXX 
4) Nella procedura bonifica_avv_1.sh, citata nel paragrafo “3.2.1 step 1” c’è un'istruzione MKDIR che 
va in errore perché la cartella LOG è stata creata a mano precedentemente. Togliere questa istruzione 
oppure fare un controllo del tipo "se esiste la cartella" allora si procede, sennò la si crea. IN 
GENERALE: le procedure vanno provate prima della consegna per evitare la presenza di errori 
sintattici evitabili. 
5) Punto 2 pagina 10: l’inizio del punto 2, non sembra una verifica ma una spiegazione della procedura. 
Non ha pertanto motivo di stare nel punto indicato, occorre valutare se non sia meglio inserirla prima, 
nella fase di spiegazione delle operazioni che fa lo script, per esempio al punto 2 di pag. 9. IN 
GENERALE: occorre che le fasi di spiegazione degli script e di verifica dei risultati/dati siano bene 
separate. Occorre provvedere anche nel resto del documento e negli altri documenti consegnati. 
6) Punto 3 pagina 11: vedi osservazione punto 5) precedente 
7) Le query a pagina 12 non permettono una verifica dei numeri indicati nella tabella indicata, essendo 
dei conteggi fatti su una tabella costruita appositamente. Servono invece le query che stanno dentro 
la procedura eseguita e che vanno a contare dentro le tabelle di origine.  
8) Punto 1 pagina 13: il primo periodo non è chiaro. Si propone di sostituirlo con: “verificare che nella 
tabella XBA_LOG.... sia presente la riga "inizio XBA_SALVA....." e "fine XBA_SALVA....". 
9) La query riportata al punto 1 pagina 13 non tira fuori tutte le operazioni fatte e poi bisogna andare a 
cercare quella che interessa. 
10) Punto 2 pagina 15: la prima e la terza query non sembrano dare un'idea della coerenza del prima e 
del dopo. In pratica non si capisce se, dopo la modifica fatto dallo script, i record con il foro corretto 
siano gli stessi di quelli di partenza. Anzi la terza query da un numero inferiore alla prima mentre ci 
aspetteremmo un numero uguale o maggiore. 
11) Punto 4 pagina 15: non è chiaro il motivo per cui invece di dire  “verificare che tutti i records risultino 
con la colonna RV_ALT2_VALUE valorizzato, che sia presente il foro di NAPOLI NORD” non si

Via Crescenzio 17/C Roma - prot.dgsia.dog@giustiziacert.it – protocollo.dgsia@giustizia.it 
3 
 
metta la query di verifica, ad esempio: SELECT * FROM CG_REF_CODES WHERE RV_DOMAIN 
= 'FORO_AVVOCATI' and RV_ALT2_VALUE Is Null o similare. 
12) Le verifiche a pagina 16, prima del paragrafo 3”.2.3 STEP 3” sembrano inutili: se non ho alcun 
errore nel log dello script di creazione, perché queste colonne NON ci dovrebbero essere? Sembrano 
delle verifiche ridondanti e poco utili ai fini della procedura di bonifica vera e propria IN 
GENERALE: le verifiche pre e post bonifica vanno fatte sui dati elaborati. I dati pre e post devono 
essere estratti con le stesse query. Devono essere esplicitati i controlli sui dati. Le verifiche sulle 
strutture create ed utilizzate sembrano ridondanti. 
13) A pagina 13, prima del paragrafo 3”.2.3 STEP 3”, MANCANO LE ISTRUZIONI DI ROLL-BACK 
NEL CASO IN CUI qualche controllo sui dati non sia andato a buon fine. cioè, oltre ad aprire il 
ticket il SIES va riportato allo stato originale.  
 
In linea generale, per rendere più fruibile la documentazione tecnica, si chiede di: 
- 
snellire la lettura del documento evitando rimandi avanti ed indietro all’interno dello stesso 
documento quando non necessario; 
- 
snellire le frasi;  
- 
separare le  spiegazioni dalle verifiche vere e proprie;  
- 
prevedere i controlli sui log per la corretta esecuzione formale degli script;  
- 
prevedere i controlli opportuni sui dati pre e post elaborazione per verificare la bontà della logica di 
bonifica. In particolare le verifiche pre e post bonifica vanno fatte sui dati pre e post elaborazione. I 
dati pre e post devono essere estratti con le stesse query. Devono essere esplicitati i controlli sui dati.  
- 
i documenti correlati tra loro devono essere coerenti, cioè se in un documento viene referenziato un 
altro documento occorre che sia citato il nome corretto. 
- 
controllare gli indici e le numerazioni. 
 
    
 
 Il DEC 
                                                                Dott. Oris Orlando 
 
 
ORLANDO ORIS
MINISTERO
DELLA GIUSTIZIA
06.09.2022
08:47:23
GMT+02:00