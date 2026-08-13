---
uniqueName: riscontro-nota-specifiche-di-intervento-sies-20192
displayName: "Riscontro Nota Specifiche di intervento SIES 2019 21  entro 04 10 "
category: "GENERAL"
tags: []
---

# Riscontro Nota Specifiche di intervento SIES 2019_21 (entro 04_10)

> **File originale:** `MEV/SCHEDA_021/Docs/Riscontri DGSIA/Riscontro Nota Specifiche di intervento SIES 2019_21 (entro 04_10).pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi  
Direzione Generale per i Sistemi Informativi Automatizzati 
 
 
AP/mg/pam 
Livello di Riservatezza:  L3 
Ambito: 
RTI Engineering sirfin Pa 
Area penale  
 
 
 
 
 
 
Spett.le Engineering Ingegneria Informatica S.p.A.  
In proprio e n.q. mandataria RTI  
Engineering Ingegneria Informatica S.p.A & Sirfin PA S.r.l.  
 
Al  RUP  
Ing Giovanni Malesci 
 
Oggetto: Gara informale ex art. 162 d.lgs. 50/2016 per l’affidamento dello sviluppo del sistema 
informativo unitario telematico del processo penale e per la manutenzione e diffusione degli attuali 
sistemi dell’area penale del Ministero della Giustizia e servizi correlati ex art 162 d.lgs. 50/2016.  
SIA 106.1.B.EV.S.23/19P.   Lotto 1 - CIG: 73479643B7 – CUP: J51C1700050001 Riscontro scheda 
SIES 2019_21 
 
 
Con riferimento al documento  SIUT-SIE-SI-2.3-20210730-Specifiche-intervento-021-
SIES.pdf si trasmettono le osservazioni del gruppo di lavoro. 
Si attende un riscontro entro il 04.10.2021 
 
 
  
 
 
 
 
 
 
 
 
IL DEC 
 
 
 
 
 
 
 
Dr.ssa Annamaria Palmieri 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
PALMIERI ANNAMARIA
MINISTERO DELLA
GIUSTIZIA/CF:IT-80184430587
28.09.2021 20:25:07
GMT+00:00

In relazione al documento “SIUT-SIE-SI-2.3-20210730-Specifiche-intervento-021-SIES”, si 
inoltrano le seguenti osservazioni da inoltrare all’RTI. 
a) Paragrafo 6.2 pag. 40: bisogna che l’RTI preveda dei test specifici per simulare il malfunzionamento 
del Reginde per verificare come avviene la ricerca sulla base dati locale.  
b) Paragrafo 6.2.5 pag. 71: va indicato l’url corretto del Reginde.  
• 
Per il pre-esercizio è http://reginde.processotelematicotest.giustizia.it  
• 
Per l’esercizio è http://reginde.processotelematico.giustizia.it.  
c) Paragrafo 6.2.5.2 pag. 73 devono essere inseriti gli interventi necessari per l’eventuale 
funzionamento con il protocollo TLS 1.0  
d) Paragrafo 6.2.7 pag. 73 va integrato secondo quanto indicato al punto b), indicando anche cosa fare 
in previsione del passaggio ad https. 
e) Paragrafo 6.3.3 pag. 74 lo stile grafico delle interfacce non sembra essere identico a quello 
dell’attuale SIES. 
f) Paragrafo 6.6.2 pag. 89: si fa riferimento ad una consegna del gruppo Tabelle Fisse di DGSIA. E’ 
opportuno indicare la data della consegna.  
g) Paragrafo 6.6.2.2 pag. 91: la prima frase “dovranno essere adottati anche nella tabella REGIONE della 
DGSIA.” sembra introdurre un obbligo che non può essere mandatorio per il gruppo Tabelle Fisse di 
DGSIA. Che succede se il gruppo tabelle fisse non cambia il suo file? 
h) Paragrafo 6.6.2.2 paragrafo Pag. 91, frase “Considerando il numero limitato di records da modificare 
l’allineamento su SIES sarà effettuato manualmente.” - Specificare cosa significa manualmente 
(tramite strumenti tipo Toads o tramite script) 
i) 
Paragrafo 6.6.2.3 pagina 92: sulla frase “A seguito dell’aggiornamento del dominio NAZIONE della 
CG_REF_CODES bisognerà aggiornare anche la tabella CODICI_SIES_NSC, utilizzata nel modulo di 
interoperabilità SIES-NSC, per i records con CO_DOMAIN = ‘NAZIONE’, modificando il valore della 
colonne CO_SIES_DES per quelli per cui vi sarà una modifica della Denominazione e l’inserimento di 
nuovi record per quelle NAZIONI aggiunti nella tabella CG_REF_CODES, dopo verifica dell’esistenza 
degli stessi nella equivalente tabella di NSC (DC_TAB_STATO_ESTERO). Eventuali Nazioni aggiunte 
nella CG_REF_CODES ed assenti in NSC, saranno segnalate agli amministratori di quel Sistema per le 
opportune verifiche.”, si suppone che la verifica sia stata fatta dal fornitore, visti gli accordi verbali. 
Se non fatta, occorre chiarirlo bene, per coinvolgere il Casellario.  
j) 
Nel capitolo 6.6., viene detto più volte “In caso di aggiornamento della tabella fissa xxxxxxx, il Gruppo 
tabelle fisse della DGSIA dovrà trasmettere le modifiche anche a SIES.” Faccio presente che fa parte 
integrante di questo progetto la fornitura delle opportune procedure per il futuro aggiornamento.

Il documento di specifiche non è autoconsistente, in quanto, al suo interno, sono richiamati i 
documenti di seguito elencati che vanno rivisti nel loro complesso: 
1) SIUT-SIES-MG-1.0-20210730 - Istruzioni_Bonifica_Difensori_021_RegInde_SIES.pdf 
2) SIUT-SIES-MG-1.0-20210730 - Aggiornamento_SIES_da_Tabelle_DGSIA_021_RegInde_SIES.pdf 
 
Di seguito, alcune osservazioni non esaustive:  
a) Nel documento n°1, sembrerebbe che il ripristino, in caso di fallimento, sia previsto solo per le tabelle 
avvocato, in senso lato. Se qualcosa nelle bonifiche non dovesse andare a buon fine, per cui non 
fosse possibile installare tutta la MEV, il sistema nel suo complesso deve essere ripristinato nello 
stato precedente. Pertanto, dovrà essere previsto un ripristino di tutte le tabelle coinvolte nel 
processo di bonifica. E’ opportuno altresì indicare se sia necessario effettuare dei backup puntuali 
(oltre all’intero backup dell’intera base dati preliminarmente all’inizio delle attività) come ad 
esempio della tabella “CG_REF_CODES”. 
b) Sul documento n°1, indicare/valutare se durante le operazioni “bonifica avvocati” ci fossero delle 
fasi intermedie per controllare l’effetto di quanto appena eseguito. In caso di risposta affermativa la 
procedura di bonifica dovrà essere redatta in modo tale da permettere il controllo puntuale. 
c) Nell’attuale documento non è ben chiara la logica del punto 10 a pag. 12 Paragrafo “3.2 Procedura 
Bonifica Difensori SIES”, dove sarebbe utile mettere un punto di verifica. 
d) In entrambi i documenti occorre eliminare i riferimenti ai file di tipo “xlsx”: le tabelle da importare 
devono essere già pronte; deve essere indicata la fonte da cui si è partiti (file inviato da… il ….). 
e) In entrambi documenti è necessario, separare le istruzioni relative al “SIES distrettuale” da quelle 
per “SIUS Avvocati”. Sono sistemi diversi e pertanto devono esserci consegne separate, anche se gli 
aggiornamenti dovranno essere eseguiti in modo contestuale. 
Si chiede se ci sono controindicazioni per procedere per passi  
1) eseguire la bonifica delle Tabelle Fisse con un rilascio  
2) Effettuare la bonifica degli avvocati 
3) Realizzare l’aggancio al Reginde..