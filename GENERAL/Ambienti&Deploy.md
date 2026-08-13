---
uniqueName: ambientideploy
displayName: "Ambienti&Deploy"
category: "GENERAL"
tags: []
---

﻿Ambienti & Deploy
- CAPITOLO 1. NUOVA INFRASTRUTTURA (SIES@10.5.207.202)
Ambiente per la NUOVA INFRASTRUTTURA: 10.5.207.202
Gestione delle code:
- MESSINA http://10.5.207.202:8080
- TORINO http://10.5.207.202:8081
Per eseguire i test di colloquio tra nuova e vecchia infrastruttura, abbiamo spento le code su TORINO e abbiamo sostituito l’indirizzo con:
- TORINO http://10.5.207.139:13080
Ovviamente abbiamo attivato le code sulla 139.
Sulla macchina 202 abbiamo inoltre modificato il file “siapjms.properties” con il nuovo puntamento.
Una volta conclusi i test si può ristabilire la situazione iniziale.
SIES sulla nuova infrastruttura è raggiungibile all’indirizzo: http://10.5.207.202:8080/
- CAPITOLO 2. PRE-COLLAUDO (weblogic@10.5.207.119)
In ambiente di pre-collaudo utilizziamo due server per due deploy differenti:
L’applicativo NSC comprendente la MEV_ENG_31_BIS è deployato sul server “servizi-casellario-as1” e raggiungibile all’indirizzo: http://10.5.207.119:8001/nsc/index.do?dEbUg=true
L’applicativo NSC prima del merge del la MEV_ENG_31_BIS è deployato sul server “servizi-internet-as1” (che era spento e su cui era deployato “pecacc_svil”) e raggiungibile all’indirizzo: http://10.5.207.119:10001/nsc/index.do?dEbUg=true
- CAPITOLO 3. 139 (10.5.207.139)
Sulla macchina 139 ci sono 5 applicativi per SIES, più NSC:
- COLLAUDO http://10.5.207.139:8080/
- PREESERCIZIO http://10.5.207.139:9080/
- MAC http://10.5.207.139:10080/
- FORMAZIONE http://10.5.207.139:11080/
- TRUNK http://10.5.207.139:13080/
In ambiente di “COLLAUDO” è presente la MEV 16 per quanto riguarda SIES. La parte NSC è raggiungibile all’indirizzo: http://10.5.207.139:7001/nsc/index.do?dEbUg=true
In questo caso NSC espone il WS di trasferimento dei fogli complementari (ruolo SERVER) mentre SIES è il client che invoca il servizio ed attende la risposta.