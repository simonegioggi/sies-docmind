---
uniqueName: mev35-iscrizioneprocedimentoesecuzionepenesostitut
displayName: "MEV 35   IscrizioneProcedimentoEsecuzionePeneSostitutive"
category: "GENERAL"
tags: []
---

# MEV_35 - IscrizioneProcedimentoEsecuzionePeneSostitutive

> **File originale:** `MEV/SCHEDA_035/MEV_35 - IscrizioneProcedimentoEsecuzionePeneSostitutive.docx`  
> **Tipo:** DOCX

---

Iscrizione procedimento Esecuzione Pene Sostitutive
Per l’iscrizione di questo tipo di procedimento dobbiamo duplicare le funzioni di iscrizione procedimento di esecuzione sanzione sostitutiva (OGGETTO_PROCEDIMENTO= ‘U019’ e RV_HIGH_VALUE = ‘S12’, che rappresenta il valore da inserire nella colonna COD_TIPO_REGISTRO di “Generale_Procedimento”).
Riporto un esempio di iscrizione:

Selezionando “Iscrizione Procedimento”:

Selezionando nella combo box “Esecuzione Sanzione Sostitutiva” la form visualizza il campo Anno/Numero Ordinanza obbligatorio

A seguito della compilazione dei campi obbligatori e della Conferma, il sistema inserisce un procedimento, caratterizzato da avere un numero di ESS corrisponde al numro di Procedimento
Vi sono quattro tipologie di Inserimento: quella su riportata “Iscrizione da fascicolo SIEP”, “Iscrizione da Soggetto”, “Iscrizione da presa in carico” e “Iscrizione procedimento collegato”.
Si ricorda che quando si va a iscrivere un procedimento il cui contenuto è marcato come figlio di quello di ESS (records CG_REF_CODES con RV_DOMAIN = ‘OGGETTO_PROCEDIMENTO’ e RV_LOW_VALUE = ‘S12’), la form di Iscrizione richiede obbligatoriamente di indicare Anno e Numero del procedimento di ESS

I procedimenti di Esecuzione Pene Sostitutive (OGGETTO_PROCEDIMENTO= ‘U126’ e RV_HIGH_VALUE = ‘S30’, che rappresenta il valore da inserire nella colonna COD_TIPO_REGISTRO di Generale_Procedimento) devono comportarsi alla stessa maniera di quelli di ESS, utilizzando le stesse tabelle. Sarà il valore di COD_OGGETTO_PROCEDIMENTO ‘U126’ o ‘U019’ a far capire se si tratta di Esecuzione Pene Sostitutive o di ESS.
Estratto dalla SI-MEV35
Dopo che il Magistrato di Sorveglianza ha determinato le modalità di esecuzione della pena sostitutiva invia l’ordinanza all’Ufficio di Sorveglianza competente per l’esecuzione della pena sostitutiva. L’Ufficio iscrive un fascicolo che farà da collettore per tutti i procedimenti che si apriranno durante l’esecuzione ad essa attinenti. Questa tipologia di procedimento, come già fatto per l’esecuzione delle misure alternative, delle misure di sicurezza e delle sanzioni sostitutive, sarà identificato comunemente come “Fascicolo padre”, mentre tutti i procedimenti relativi ad atti relativi alla fase di esecuzione, che saranno caratterizzati da una doppia numerazione il numero identificativo del procedimento e il numero del fascicolo di Esecuzione Pene Sostitutive, saranno identificati comunemente come “Fascicoli Figli”.
Nell’ambito dell’Ufficio di Sorveglianza (UDS/UDSM), il contenuto da integrare è il seguente:
Esecuzione Pene Sostitutive  (U126 – S30)
Al nuovo contenuto vanno associati i seguenti oggetti:
Semilibertà sostitutiva (art. 55 - 62 L. 689/1981)    2900
Detenzione domiciliare sostitutiva (art. 56 - 62 L. 689/1981)     2911
Lavoro di pubblica utilità sostitutivo (art. 56 bis L. 689/1981 – 55 DL 274/20)   2912
Permanenza Domiciliare     2913
Per questo tipo di procedimento non sono previsti esiti.
Per questo procedimento, come negli altri casi di procedimenti di Esecuzione, il sistema presenterà la seguente form:

che in caso di iscrizione da presa in carico dell’ordinanza di applicazione presenterà già precompilati i campi Tipo Atto, Data atto, Mittente, Sede Mittente, Anno e Numero Ordinanza.
La form simile, ma priva di dati precompilati, si presenterà anche in caso di iscrizione da Procedimento SIEP, iscrizione da Soggetto e Iscrizione Procedimento Collegato.
A seguito della Conferma il sistema inserirà un fascicolo “padre” di esecuzione pene sostitutive e presenterà la seguente form di dettaglio dalla quale sarà possibile attivare le azioni di Modifica e Stampa:

Da questa form cliccando su Anno e Numero Esecuzione Pena Sostitutiva si riceverà la seguente form:

da cui sarà possibile proseguire con l’inserimento di un nuovo procedimento figlio o con la modifica dei dati relativi alla durata ed al luogo di esecuzione della pena sostitutiva. Il completamento di tali dati avviene successivamente all’iscrizione del procedimento, quando l’ufficio riceve le ulteriori informazioni.