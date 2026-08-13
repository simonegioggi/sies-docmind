---
uniqueName: mev10step3intervento21150202
displayName: "mev10 step 3 intervento 21 150202"
category: "GENERAL"
tags: []
---

# mev10_step_3_intervento_21_150202

> **File originale:** `MEV/Mev10/mev10_step_3_intervento_21_150202.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 65 di 84
Versione n° 0.1 del 04/11/2014
 
21 Invio segnalazione tramite email 
21.1 Intervento richiesto dall’Amministrazione  
Modulo invio segnalazione tramite posta elettronica ordinaria. 
21.2 Situazione attuale 
21.3 Descrizione dell’intervento 
All’interno del menu principale l’operatore seleziona la voce “invia Segnalazione ” (Figura 24), il sistema 
visualizza la finestra contente il modulo della segnalazione (Figura 25). 
 
 
Figura 24 -  Menu principale

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 66 di 84
Versione n° 0.1 del 04/11/2014
 
A
A
B
B
C
C
D
D
E
E
F
F
G
G
H
H
Figura 25 -  Modulo segnalazione 
La maggior parte della informazioni del modulo sono presenti nella sessione dell’operatore e vengono 
utilizzati per prevalorizzare le relative caselle di testo. 
Le informazioni prevalorizzate sono: 
a) Tipologia ufficio 
b) Sede ufficio 
c) Email ufficio 
d) Telefono ufficio

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 67 di 84
Versione n° 0.1 del 04/11/2014
 
e) Cognome  
f) Nome 
g) Email richiedente 
h) Sottosistema 
i) 
Versione.  
Il sistema valorizza suddette caselle di testo e l’operatore non può modificarle. 
Per le rimanenti informazioni del modulo, l’operatore seleziona dagli elenchi predisposti dal sistema: 
j) 
la funzionalità  
k) l’azione  
l) 
la tipologia della segnalazione 
m) la gravità della segnalazione. 
Il sistema valorizza l’elenco delle funzionalità in relazione al sottosistema dell’operatore. 
Inoltre, vengono aggiunte le voci comuni a tutti i sottosistemi (CG_REF_CODES.RV_HIGH _VALUE= “TUTTI”). 
L’elenco così popolato viene presentato all’operatore in ordine alfabetico.  
Pertanto, l’operatore che accede al sistema SIEP può selezionare la funzionalità desiderata dall’elenco 
formato da  tutte le voci del suo sottosistema (CG_REF_CODES.RV_HIGH_VALUE = “SIEP”) e da quelle 
comuni a tutti i sottosistemi CG_REF_CODES.RV_HIGH_VALUE = “TUTTI”). 
L’operatore valorizza il numero e l’anno del procedimento. 
Infine, inserisce una breve descrizione della segnalazione nella casella “Oggetto segnalazione” e descrive 
con maggiori dettagli la sua segnalazione nella casella “Descrizione segnalazione”. 
L’operatore se vuole ricevere nella sua casella di posta elettronica ordinaria del Ministero una copia della 
segnalazione seleziona la casella di spunta “Inviare copia email nella casella di posta”. 
L’operatore può collegare dei file all’email. 
Il numero massimo di file allegati è uguale a cinque.  
Ogni file può avere dimensione massima pari ad un megabyte. 
Il nome del file allegato è subito visibile nella griglia presente nella parte inferiore del modulo. 
L’operatore può annullare il collegamento con il file allegato premendo l’icona a destra del nome del file 
allegato. 
L’operatore può svuotare il contenuto delle caselle modificabili premendo il pulsante  “Svuota modulo”. 
L’operatore può annullare l’inserimento delle informazioni ed uscire dal modulo premendo il pulsante 
“Chiudi”. 
L’operatore conferma l’inserimento delle informazioni premendo il pulsante “Invia email”. 
Il sistema invia un’email alla casella di posta predisposta a ricevere tutte le segnalazioni inviate dagli utenti. 
Se l’operatore ha valorizzato la casella di testo con l’email del referente, il sistema invia un’email alla casella 
di posta del referente. 
Qualora l’operatore avesse selezionato la casella di spunta “Inviare copia email nella casella di posta”, il 
sistema invierà un’email alla casella di posta dell’operatore che ha inserito la segnalazione. 
L’operatore accedendo alla casella di posta destinataria delle segnalazioni visualizza le informazioni della 
segnalazione. 
Il mittente della email è la casella di posta: “segnalazioni_sies@giustizia.it”. 
Se l’operatore è del sottosistema SIEP la casella destinataria dell’email è siep@giustizia.it. 
Se l’operatore è del sottosistema SIGE la casella destinataria dell’email è sige@giustizia.it. 
Se l’operatore è del sottosistema SIUS la casella destinataria dell’email è sius@giustizia.it. 
Attualmente la presente funzionalità non è prevista per il sottosistema SIEPE.  
L’oggetto della email è: “Segnalazione_SIES_“ + sottosistema + “_“ + cod_tipo_ufficio + “_“ + sede ufficio + 
+ “_“ + data sistema +  “_“  + ora sistema. 
Quindi una segnalazione inviata dall’operatore dell’ufficio della Procura presso il Tribunale ordinario di 
Torino in data 22/12/2014 alle ore 16.00 e riguardante il sottosistema SIEP ha nel campo oggetto il 
seguente testo: “Segnalazione_SIES_SIEP_PM_TORINO_221214_1600”.  
Il corpo del testo dell’email ha la stessa formattazione nello standard html del modulo utilizzato per inserire la 
segnalazione (

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 68 di 84
Versione n° 0.1 del 04/11/2014
 
 
Figura 26).  
Attualmente non è prevista la persistenza delle informazioni della segnalazione e, pertanto, il sistema non 
registra le informazioni inserite dall’operatore nel modulo della segnalazione.  
L’intervento prevede anche l’intervento di un record nella tabella <> che censisce l’elenco delle principali 
funzionalità del sistema.

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 69 di 84
Versione n° 0.1 del 04/11/2014
 
 
Figura 26 -  Email visualizzata  
 
21.4 Riferimenti 
21.5 Sottosistema 
La modifica interessa solo il sottosistema SIEP, SIGE e SIUS.  
21.6 Uffici 
L’intervento in parola riguarda tutti gli utenti che accedono al sistema. 
21.7 Modifica funzionalità 
21.8 Modifica interfacce utente 
L’intervento prevede la realizzazione di una nuova interfaccia utente come descritta in precedenza. 
La nuova interfaccia è composta dalle seguenti sezioni: 
 
 
Figura 27 - Sezione A – Nome funzione

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 70 di 84
Versione n° 0.1 del 04/11/2014
 
Figura 28 - Sezione B - Ufficio 
 
 
Figura 29 - Sezione C - Referente 
 
 
Figura 30 - Sezione D - Richiedente 
 
 
Figura 31 - Sezione E - Segnalazione 
 
 
Figura 32 - Sezione F – Copia email 
 
Figura 33 - Sezione G - Allegati

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 71 di 84
Versione n° 0.1 del 04/11/2014
 
 
Figura 34 - Sezione H - Pulsanti 
21.9 Modifica interfacce software/algoritmi 
Il sistema nella valorizzazione dei campi deve seguire le seguenti regole: 
N.
Campo
O
D
Nota
Campo lettura
1. Nome funzione 
 
 
Aggiungere record alla tabella funzione funzione. 
 
Tabella 40 – Sezione A – Nome funzione 
 
N.
Campo
O
D
Nota
Campo lettura
2. Tipologia ufficio 
 
 
Prevalorizzato e non modificabile. 
La decodifica del campo <cod_tipo_uff> è presente nella tabella 
<CG_REF_CODES> con <RV_DOMAIN> = “TIPO_UFFICIO”. 
Ufficio.cod_tipo_uff
3. Sede ufficio 
 
 
Prevalorizzato e non modificabile. 
La decodifica del campo <cod_comune> è presente nella tabella 
<COMUNE>. 
Ufficio.cod_comune
4. Email ufficio 
 
 
Prevalorizzato e non modificabile. 
Ufficio.e_mail 
5. Telefono ufficio 
 
 
Prevalorizzato e non modificabile. 
 
Ufficio.telefono 
Tabella 41 – Sezione B - Ufficio  
 
N.
Campo
O
D
Nota
Campo lettura
6.
Titolo Referente 
 
 
Elenco contenente le seguenti voci: 
{“Signora”, “Signor”,”Dott.ssa”,”Dott.”}. 
Prevalorizzato a ‘-‘. 
Tabella 
<CG_REF_CODES> 
campo 
<RV_DOMAIN> = 
“SEGNALAZIONE_TI
TOLO”. 
7. Cognome Referente 
 
 
Testo libero max 40 caratteri alfanumerici 
 
8. Nome Referente 
 
 
Testo libero max 40 caratteri alfanumerici 
 
9. Email Referente 
 
 
Testo libero max 100 caratteri alfanumerici 
 
10 Telefono Referente 
 
 
Testo libero max 15 caratteri alfanumerici 
 
Tabella 42 – Sezione C - Referente 
 
N.
Campo
O
D
Nota
Campo lettura
11
Titolo  
 
 
Elenco contenente le seguenti voci: 
{“Signora”, “Signor”,”Dott.ssa”,”Dott.”}. 
Prevalorizzato a ‘-‘. 
Tabella 
<CG_REF_CODES> 
campo 
<RV_DOMAIN> = 
“SEGNALAZIONE_TI
TOLO”. 
12 Cognome 
 
 
Prevalorizzato e non modificabile. 
 
Utente.cognome

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 72 di 84
Versione n° 0.1 del 04/11/2014
 
N.
Campo
O
D
Nota
Campo lettura
13 Nome  
 
 
Prevalorizzato e non modificabile. 
 
Utente.nome 
14 Telefono 
 
 
Prevalorizzato e non modificabile. 
 
Utente.telefono 
15 Email  
 
 
Prevalorizzato e non modificabile. 
 
Utente.e_mail 
Tabella 43 – Sezione D- Richiedente 
 
N.
Campo
O
D
Nota
Campo lettura
16 Sottosistema 
 
 
Prevalorizzato e non modificabile. 
L’informazione è recuperata dai dati di sessione dell’operatore. 
 
 
17 Versione 
 
 
Prevalorizzato e non modificabile. 
L’informazione è recuperata dai dati di sessione dell’operatore. 
 
Versione.cod_versi
one 
Tabella 44 –Sezione E – Segnalazione - Dati sistema 
 
N.
Campo
O
D
Nota
Campo lettura
18
Funzionalità 
 
 
Il sistema valorizza l’elenco delle funzionalità in relazione al 
sottosistema dell’operatore. 
Inoltre, il sistema aggiunge le voci comuni a tutti i sottosistemi 
(CG_REF_CODES.RV_HIGH_VALUE= “TUTTI”). 
L’elenco così popolato viene presentato all’operatore in ordine 
alfabetico.  
Prevalorizzato a ‘-‘. 
Tabella 
<CG_REF_CODES> 
campo 
<RV_DOMAIN> = 
“SEGNALAZIONE_F
UNZIONALITA”. 
19
Azione 
 
 
Elenco contenente le seguenti voci: 
{“Cancella”, “Dettaglio”, “Elenco”, “Excel”,  “Inserimento”, 
“Modifica”, “Ricerca”, “Stampa”, “Trasferimento”, “Variazione”} 
Prevalorizzato a ‘-‘. 
Tabella 
<CG_REF_CODES> 
campo 
<RV_DOMAIN> = 
“SEGNALAZIONE_A
ZIONE”. 
20
Tipologia  
segnalazione 
 
 
Elenco contenente le seguenti voci: 
{“Adeguamento normativo” 
 “Errore bloccante”, 
“Errore non bloccante”, 
“Miglioramento funzionale”, 
“Miglioramento grafico”, 
“Nuova funzionalità”}. 
Prevalorizzato a ‘-‘. 
Tabella 
<CG_REF_CODES> 
campo 
<RV_DOMAIN> = 
“SEGNALAZIONE_TI
POLOGIA”. 
21
Gravità segnalazione. 
 
 
Elenco contenente le seguenti voci: 
{ “Molto alta”, 
“Alta”, 
“Media”, 
“Bassa”, 
“Molto bassa”}. 
Prevalorizzato a ‘-‘. 
Tabella 
<CG_REF_CODES> 
campo 
<RV_DOMAIN> = 
“SEGNALAZIONE_G
RAVITA”. 
22 Oggetto segnalazione 
 
 
Testo libero max 70 caratteri alfanumerici 
 
23 Descrizione 
 
 
Testo libero max 200 caratteri alfanumerici 
 
24 Anno procedimento 
 
 
Testo libero max 4 caratteri numerici [0..9] 
 
25 Numero 
procedimento 
 
 
Testo libero max 6 caratteri numerici [0..9] 
 
Tabella 45 – Sezione E - Segnalazione

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 73 di 84
Versione n° 0.1 del 04/11/2014
 
 
N. 
Campo 
O 
D 
Nota 
 
26 Inviare 
copia 
email 
nella propria casella di 
posta 
 
 
Casella di spunta. 
Prevalorizzato non selezionato 
 
Tabella 46 – Sezione F – Copia email  
 
N. 
Campo 
O 
D 
Nota 
 
27 Nome allegato 
 
 
Il sistema mostra l’elenco dei nomi dei file allegati. 
 
28 Cancella 
 
 
L’operatore può annullare il collegamento dell’allegato all’email.   
 
Tabella 47 – Sezione G– Allegati 
N. 
Campo 
O 
D 
Nota 
 
29 Pulsante “Allegati” 
 
 
L’operatore può allegare fino a 5 file. Ogni file può avere dimensione 
massima pari ad un megabyte.  
 
30 Pulsante “Chiudi” 
 
 
L’operatore preme il pulsante ed il sistema chiude la finestra 
 
31 Pulsante “Svuota” 
 
 
L’operatore preme il pulsante ed il sistema svuota le caselle 
valorizzabili dall’operatore. 
 
32 Pulsante “Invia” 
 
 
L’operatore preme il pulsante ed il sistema invia l’email ai destinatari 
 
Tabella 48 – Sezione I- Pulsanti 
21.10 Modifica database 
L’intervento prevede l’inserimento nella tabella <CG_REF_CODES> dei seguenti record: 
N
. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
1.
SEGNALAZIONE_TIT
OLO 
01 
NULL 
NULL 
Signora 
NULL 
NULL 
NULL 
NULL 
2.
SEGNALAZIONE_TIT
OLO 
02 
NULL 
NULL 
Signor 
NULL 
NULL 
NULL 
NULL 
3.
SEGNALAZIONE_TIT
OLO 
03 
NULL 
NULL 
Dott.ssa 
NULL 
NULL 
NULL 
NULL 
4.
SEGNALAZIONE_TIT
OLO 
04 
NULL 
NULL 
Dott. 
NULL 
NULL 
NULL 
NULL 
Tabella 49 – Titolo 
N. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
5.
SEGNALAZIONE_FUN
ZIONALITA 
0001 
TUTTI 
NULL 
Alias 
NULL 
NULL 
NULL 
NULL 
6.
SEGNALAZIONE_FUN
ZIONALITA 
0002 
TUTTI 
NULL 
Altre Richieste 
NULL 
NULL 
NULL 
NULL 
7.
SEGNALAZIONE_FUN
ZIONALITA 
0003 
TUTTI 
NULL 
Altri Atti 
NULL 
NULL 
NULL 
NULL 
8.
SEGNALAZIONE_FUN
ZIONALITA 
0004 
TUTTI 
NULL 
Annotazione Manuale 
NULL 
NULL 
NULL 
NULL 
9.
SEGNALAZIONE_FUN
ZIONALITA 
0005 
TUTTI 
NULL 
Annotazioni Manuali Benefici 
NULL 
NULL 
NULL 
NULL 
10. SEGNALAZIONE_FUN
ZIONALITA 
0006 
TUTTI 
NULL 
Assegnazioni 
NULL 
NULL 
NULL 
NULL

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 74 di 84
Versione n° 0.1 del 04/11/2014
 
N. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
11. SEGNALAZIONE_FUN
ZIONALITA 
0007 
TUTTI 
NULL 
Assistente Sociale 
NULL 
NULL 
NULL 
NULL 
12. SEGNALAZIONE_FUN
ZIONALITA 
0008 
TUTTI 
NULL 
Assistenti Giudiziari 
NULL 
NULL 
NULL 
NULL 
13. SEGNALAZIONE_FUN
ZIONALITA 
0009 
TUTTI 
NULL 
Associazione Fascicoli SIES - BDMC 
NULL 
NULL 
NULL 
NULL 
14. SEGNALAZIONE_FUN
ZIONALITA 
0010 
TUTTI 
NULL 
Associazione/Cambio Magistrato 
NULL 
NULL 
NULL 
NULL 
15. SEGNALAZIONE_FUN
ZIONALITA 
0011 
TUTTI 
NULL 
Atti Ricevuti Per Competenza 
NULL 
NULL 
NULL 
NULL 
16. SEGNALAZIONE_FUN
ZIONALITA 
0012 
TUTTI 
NULL 
Attività 
NULL 
NULL 
NULL 
NULL 
17. SEGNALAZIONE_FUN
ZIONALITA 
0013 
TUTTI 
NULL 
Attività 
NULL 
NULL 
NULL 
NULL 
18. SEGNALAZIONE_FUN
ZIONALITA 
0014 
TUTTI 
NULL 
Aumenti E Riduzioni Pena 
NULL 
NULL 
NULL 
NULL 
19. SEGNALAZIONE_FUN
ZIONALITA 
0015 
TUTTI 
NULL 
Avvocato 
NULL 
NULL 
NULL 
NULL 
20. SEGNALAZIONE_FUN
ZIONALITA 
0016 
TUTTI 
NULL 
BDMC 
NULL 
NULL 
NULL 
NULL 
21. SEGNALAZIONE_FUN
ZIONALITA 
0017 
TUTTI 
NULL 
Cancelleria Assegnataria 
NULL 
NULL 
NULL 
NULL 
22. SEGNALAZIONE_FUN
ZIONALITA 
0018 
TUTTI 
NULL 
Capi D'Imputazione 
NULL 
NULL 
NULL 
NULL 
23. SEGNALAZIONE_FUN
ZIONALITA 
0019 
TUTTI 
NULL 
Chiusura Esecuzione 
NULL 
NULL 
NULL 
NULL 
24. SEGNALAZIONE_FUN
ZIONALITA 
0020 
TUTTI 
NULL 
Copertina 
NULL 
NULL 
NULL 
NULL 
25. SEGNALAZIONE_FUN
ZIONALITA 
0021 
TUTTI 
NULL 
UEPE 
NULL 
NULL 
NULL 
NULL 
26. SEGNALAZIONE_FUN
ZIONALITA 
0022 
TUTTI 
NULL 
Cumulo 
NULL 
NULL 
NULL 
NULL 
27. SEGNALAZIONE_FUN
ZIONALITA 
0023 
TUTTI 
NULL 
Curatore 
NULL 
NULL 
NULL 
NULL 
28. SEGNALAZIONE_FUN
ZIONALITA 
0024 
TUTTI 
NULL 
Curatori/Tutori – SIUS 
NULL 
NULL 
NULL 
NULL 
29. SEGNALAZIONE_FUN
ZIONALITA 
0025 
TUTTI 
NULL 
Data Iscrizione E Oggetto 
NULL 
NULL 
NULL 
NULL 
30. SEGNALAZIONE_FUN
ZIONALITA 
0026 
TUTTI 
NULL 
Decodifiche 
NULL 
NULL 
NULL 
NULL 
31. SEGNALAZIONE_FUN
ZIONALITA 
0027 
TUTTI 
NULL 
Decreti 
NULL 
NULL 
NULL 
NULL 
32. SEGNALAZIONE_FUN
ZIONALITA 
0028 
TUTTI 
NULL 
Decreti Incompetenza, Inammissibilità, 
Ndp/Nlp 
NULL 
NULL 
NULL 
NULL 
33. SEGNALAZIONE_FUN
ZIONALITA 
0029 
TUTTI 
NULL 
Detenzione Domiciliare Speciale 
NULL 
NULL 
NULL 
NULL 
34. SEGNALAZIONE_FUN
ZIONALITA 
0030 
TUTTI 
NULL 
Dettaglio Trasmissione Atti 
NULL 
NULL 
NULL 
NULL 
35. SEGNALAZIONE_FUN
ZIONALITA 
0031 
TUTTI 
NULL 
Difensori 
NULL 
NULL 
NULL 
NULL 
36. SEGNALAZIONE_FUN
ZIONALITA 
0032 
TUTTI 
NULL 
Differimento 
NULL 
NULL 
NULL 
NULL 
37. SEGNALAZIONE_FUN
ZIONALITA 
0033 
TUTTI 
NULL 
Esecuzione In Carcere 
NULL 
NULL 
NULL 
NULL 
38. SEGNALAZIONE_FUN
ZIONALITA 
0034 
TUTTI 
NULL 
Esecuzione Misure 
NULL 
NULL 
NULL 
NULL 
39. SEGNALAZIONE_FUN
ZIONALITA 
0035 
TUTTI 
NULL 
Esecuzione Misure Sicurezza 
NULL 
NULL 
NULL 
NULL 
40. SEGNALAZIONE_FUN
ZIONALITA 
0036 
TUTTI 
NULL 
Esecuzione Presso Domicilio Delle 
Pene Detentive Br 
NULL 
NULL 
NULL 
NULL 
41. SEGNALAZIONE_FUN
ZIONALITA 
0037 
TUTTI 
NULL 
Esecuzione Sanzioni Sostitutive 
NULL 
NULL 
NULL 
NULL 
42. SEGNALAZIONE_FUN
ZIONALITA 
0038 
TUTTI 
NULL 
Esito Decreto Sospensione 
NULL 
NULL 
NULL 
NULL

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 75 di 84
Versione n° 0.1 del 04/11/2014
 
N. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
43. SEGNALAZIONE_FUN
ZIONALITA 
0039 
TUTTI 
NULL 
Esito Istanza 
NULL 
NULL 
NULL 
NULL 
44. SEGNALAZIONE_FUN
ZIONALITA 
0040 
TUTTI 
NULL 
Esperto 
NULL 
NULL 
NULL 
NULL 
45. SEGNALAZIONE_FUN
ZIONALITA 
0041 
TUTTI 
NULL 
Estensione 
NULL 
NULL 
NULL 
NULL 
46. SEGNALAZIONE_FUN
ZIONALITA 
0042 
TUTTI 
NULL 
Estensione Definitiva 
NULL 
NULL 
NULL 
NULL 
47. SEGNALAZIONE_FUN
ZIONALITA 
0043 
TUTTI 
NULL 
Estensione Provvisoria 
NULL 
NULL 
NULL 
NULL 
48. SEGNALAZIONE_FUN
ZIONALITA 
0044 
TUTTI 
NULL 
Estinzione Della Pena 
NULL 
NULL 
NULL 
NULL 
49. SEGNALAZIONE_FUN
ZIONALITA 
0045 
TUTTI 
NULL 
Estremi Procedimento 
NULL 
NULL 
NULL 
NULL 
50. SEGNALAZIONE_FUN
ZIONALITA 
0046 
TUTTI 
NULL 
Estremi Sentenza 
NULL 
NULL 
NULL 
NULL 
51. SEGNALAZIONE_FUN
ZIONALITA 
0047 
TUTTI 
NULL 
Estremi Titolo 
NULL 
NULL 
NULL 
NULL 
52. SEGNALAZIONE_FUN
ZIONALITA 
0048 
TUTTI 
NULL 
Evento 
NULL 
NULL 
NULL 
NULL 
53. SEGNALAZIONE_FUN
ZIONALITA 
0049 
TUTTI 
NULL 
Fascicolo 
NULL 
NULL 
NULL 
NULL 
54. SEGNALAZIONE_FUN
ZIONALITA 
0050 
TUTTI 
NULL 
Fase Istruttoria 
NULL 
NULL 
NULL 
NULL 
55. SEGNALAZIONE_FUN
ZIONALITA 
0051 
TUTTI 
NULL 
Fine Pena Convertita 
NULL 
NULL 
NULL 
NULL 
56. SEGNALAZIONE_FUN
ZIONALITA 
0052 
TUTTI 
NULL 
Funzioni Amministrative 
NULL 
NULL 
NULL 
NULL 
57. SEGNALAZIONE_FUN
ZIONALITA 
0053 
TUTTI 
NULL 
Giudice Popolare 
NULL 
NULL 
NULL 
NULL 
58. SEGNALAZIONE_FUN
ZIONALITA 
0054 
TUTTI 
NULL 
Help 
NULL 
NULL 
NULL 
NULL 
59. SEGNALAZIONE_FUN
ZIONALITA 
0055 
TUTTI 
NULL 
Incarichi E Attività 
NULL 
NULL 
NULL 
NULL 
60. SEGNALAZIONE_FUN
ZIONALITA 
0056 
TUTTI 
NULL 
Incompetenza, Ndp/Nlp, Conflitto Di 
Competenza 
NULL 
NULL 
NULL 
NULL 
61. SEGNALAZIONE_FUN
ZIONALITA 
0057 
TUTTI 
NULL 
Ingiunzione Demolizione 
NULL 
NULL 
NULL 
NULL 
62. SEGNALAZIONE_FUN
ZIONALITA 
0058 
TUTTI 
NULL 
Sospensione Arresti Domiciliari 
NULL 
NULL 
NULL 
NULL 
63. SEGNALAZIONE_FUN
ZIONALITA 
0059 
TUTTI 
NULL 
Interruzione Sospensione 
NULL 
NULL 
NULL 
NULL 
64. SEGNALAZIONE_FUN
ZIONALITA 
0060 
TUTTI 
NULL 
Irrevocabilità Ordinanza Giudice 
esecuzione 
NULL 
NULL 
NULL 
NULL 
65. SEGNALAZIONE_FUN
ZIONALITA 
0061 
TUTTI 
NULL 
Iscrizione 
NULL 
NULL 
NULL 
NULL 
66. SEGNALAZIONE_FUN
ZIONALITA 
0062 
TUTTI 
NULL 
Iscrizione - Sorveglianza 
NULL 
NULL 
NULL 
NULL 
67. SEGNALAZIONE_FUN
ZIONALITA 
0063 
TUTTI 
NULL 
Iscrizione Altro Atto 
NULL 
NULL 
NULL 
NULL 
68. SEGNALAZIONE_FUN
ZIONALITA 
0064 
TUTTI 
NULL 
Iscrizione Completa Sentenza/Decreto 
NULL 
NULL 
NULL 
NULL 
69. SEGNALAZIONE_FUN
ZIONALITA 
0065 
TUTTI 
NULL 
Iscrizione E Fase Istruttoria 
NULL 
NULL 
NULL 
NULL 
70. SEGNALAZIONE_FUN
ZIONALITA 
0066 
TUTTI 
NULL 
Iscrizione Guidata 
NULL 
NULL 
NULL 
NULL 
71. SEGNALAZIONE_FUN
ZIONALITA 
0067 
TUTTI 
NULL 
Iscrizione Manuale 
NULL 
NULL 
NULL 
NULL 
72. SEGNALAZIONE_FUN
ZIONALITA 
0068 
TUTTI 
NULL 
Istanze 
NULL 
NULL 
NULL 
NULL 
73. SEGNALAZIONE_FUN
ZIONALITA 
0069 
TUTTI 
NULL 
Istruttoria - Sorveglianza 
NULL 
NULL 
NULL 
NULL 
74. SEGNALAZIONE_FUN
ZIONALITA 
0070 
TUTTI 
NULL 
Legge 78/2013 
NULL 
NULL 
NULL 
NULL

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 76 di 84
Versione n° 0.1 del 04/11/2014
 
N. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
75. SEGNALAZIONE_FUN
ZIONALITA 
0071 
TUTTI 
NULL 
Legge Simeone 
NULL 
NULL 
NULL 
NULL 
76. SEGNALAZIONE_FUN
ZIONALITA 
0072 
TUTTI 
NULL 
Liberazione Condizionale 
NULL 
NULL 
NULL 
NULL 
77. SEGNALAZIONE_FUN
ZIONALITA 
0073 
TUTTI 
NULL 
Liberta Anticipata 
NULL 
NULL 
NULL 
NULL 
78. SEGNALAZIONE_FUN
ZIONALITA 
0074 
TUTTI 
NULL 
Log 
NULL 
NULL 
NULL 
NULL 
79. SEGNALAZIONE_FUN
ZIONALITA 
0075 
TUTTI 
NULL 
Magistrato 
NULL 
NULL 
NULL 
NULL 
80. SEGNALAZIONE_FUN
ZIONALITA 
0076 
TUTTI 
NULL 
Magistrato Competente 
NULL 
NULL 
NULL 
NULL 
81. SEGNALAZIONE_FUN
ZIONALITA 
0077 
TUTTI 
NULL 
Misura Alternativa 
NULL 
NULL 
NULL 
NULL 
82. SEGNALAZIONE_FUN
ZIONALITA 
0078 
TUTTI 
NULL 
Misura Cautelare 
NULL 
NULL 
NULL 
NULL 
83. SEGNALAZIONE_FUN
ZIONALITA 
0079 
TUTTI 
NULL 
Misura Sicurezza 
NULL 
NULL 
NULL 
NULL 
84. SEGNALAZIONE_FUN
ZIONALITA 
0080 
TUTTI 
NULL 
Misure Cautelari 
NULL 
NULL 
NULL 
NULL 
85. SEGNALAZIONE_FUN
ZIONALITA 
0081 
TUTTI 
NULL 
Mod. 36 Aggiuntiva 
NULL 
NULL 
NULL 
NULL 
86. SEGNALAZIONE_FUN
ZIONALITA 
0082 
TUTTI 
NULL 
Mod. 36 Primaria 
NULL 
NULL 
NULL 
NULL 
87. SEGNALAZIONE_FUN
ZIONALITA 
0083 
TUTTI 
NULL 
Notifiche 
NULL 
NULL 
NULL 
NULL 
88. SEGNALAZIONE_FUN
ZIONALITA 
0084 
TUTTI 
NULL 
Oe Simeone 
NULL 
NULL 
NULL 
NULL 
89. SEGNALAZIONE_FUN
ZIONALITA 
0085 
TUTTI 
NULL 
Opposizioni/Ricorsi 
NULL 
NULL 
NULL 
NULL 
90. SEGNALAZIONE_FUN
ZIONALITA 
0086 
TUTTI 
NULL 
Ordinanze 
NULL 
NULL 
NULL 
NULL 
91. SEGNALAZIONE_FUN
ZIONALITA 
0087 
TUTTI 
NULL 
Ordine Esecuzione Detenuto Arresti 
Domiciliari 
NULL 
NULL 
NULL 
NULL 
92. SEGNALAZIONE_FUN
ZIONALITA 
0088 
TUTTI 
NULL 
Ordine Esecuzione Detenuto 
Condannato Per Altra Causa 
NULL 
NULL 
NULL 
NULL 
93. SEGNALAZIONE_FUN
ZIONALITA 
0089 
TUTTI 
NULL 
Ordini Di Esecuzione 
NULL 
NULL 
NULL 
NULL 
94. SEGNALAZIONE_FUN
ZIONALITA 
0090 
TUTTI 
NULL 
Pareri 
NULL 
NULL 
NULL 
NULL 
95. SEGNALAZIONE_FUN
ZIONALITA 
0091 
TUTTI 
NULL 
Pena Complessiva 
NULL 
NULL 
NULL 
NULL 
96. SEGNALAZIONE_FUN
ZIONALITA 
0092 
TUTTI 
NULL 
Pena Pecuniaria 
NULL 
NULL 
NULL 
NULL 
97. SEGNALAZIONE_FUN
ZIONALITA 
0093 
TUTTI 
NULL 
Pene Accessorie 
NULL 
NULL 
NULL 
NULL 
98. SEGNALAZIONE_FUN
ZIONALITA 
0094 
TUTTI 
NULL 
Pene Sospese 
NULL 
NULL 
NULL 
NULL 
99. SEGNALAZIONE_FUN
ZIONALITA 
0095 
TUTTI 
NULL 
Periodo Feriale 
NULL 
NULL 
NULL 
NULL 
100 SEGNALAZIONE_FUN
ZIONALITA 
0096 
TUTTI 
NULL 
Posizione Fascicolo 
NULL 
NULL 
NULL 
NULL 
101 SEGNALAZIONE_FUN
ZIONALITA 
0097 
TUTTI 
NULL 
Posizione Giuridica 
NULL 
NULL 
NULL 
NULL 
102 SEGNALAZIONE_FUN
ZIONALITA 
0098 
TUTTI 
NULL 
Posizione Giuridica In Sentenza 
NULL 
NULL 
NULL 
NULL 
103 SEGNALAZIONE_FUN
ZIONALITA 
0099 
TUTTI 
NULL 
Posizione Materiale 
NULL 
NULL 
NULL 
NULL 
104 SEGNALAZIONE_FUN
ZIONALITA 
0100 
TUTTI 
NULL 
Posizione Materiale Fascicolo 
NULL 
NULL 
NULL 
NULL 
105 SEGNALAZIONE_FUN
ZIONALITA 
0101 
TUTTI 
NULL 
Presa In Carico - Sorveglianza 
NULL 
NULL 
NULL 
NULL 
106 SEGNALAZIONE_FUN
ZIONALITA 
0102 
TUTTI 
NULL 
Presa In Carico Provvedimenti 
NULL 
NULL 
NULL 
NULL

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 77 di 84
Versione n° 0.1 del 04/11/2014
 
N. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
107 SEGNALAZIONE_FUN
ZIONALITA 
0103 
TUTTI 
NULL 
Prima Iscrizione Sentenza/Decreto 
NULL 
NULL 
NULL 
NULL 
108 SEGNALAZIONE_FUN
ZIONALITA 
0104 
TUTTI 
NULL 
Procedimenti Di Esecuzione 
NULL 
NULL 
NULL 
NULL 
109 SEGNALAZIONE_FUN
ZIONALITA 
0105 
TUTTI 
NULL 
Procedimento 
NULL 
NULL 
NULL 
NULL 
110 SEGNALAZIONE_FUN
ZIONALITA 
0106 
TUTTI 
NULL 
Procedimenti BDMC 
NULL 
NULL 
NULL 
NULL 
111 SEGNALAZIONE_FUN
ZIONALITA 
0107 
TUTTI 
NULL 
Produzione Atti - Sorveglianza 
NULL 
NULL 
NULL 
NULL 
112 SEGNALAZIONE_FUN
ZIONALITA 
0108 
TUTTI 
NULL 
Profili 
NULL 
NULL 
NULL 
NULL 
113 SEGNALAZIONE_FUN
ZIONALITA 
0109 
TUTTI 
NULL 
Prosecuzione 
NULL 
NULL 
NULL 
NULL 
114 SEGNALAZIONE_FUN
ZIONALITA 
0110 
TUTTI 
NULL 
Prosecuzione Provvisoria 
NULL 
NULL 
NULL 
NULL 
115 SEGNALAZIONE_FUN
ZIONALITA 
0111 
TUTTI 
NULL 
Prospetto Per Grazia 
NULL 
NULL 
NULL 
NULL 
116 SEGNALAZIONE_FUN
ZIONALITA 
0112 
TUTTI 
NULL 
Provvedimenti 
NULL 
NULL 
NULL 
NULL 
117 SEGNALAZIONE_FUN
ZIONALITA 
0113 
TUTTI 
NULL 
Provvedimenti - Sorveglianza 
NULL 
NULL 
NULL 
NULL 
118 SEGNALAZIONE_FUN
ZIONALITA 
0114 
TUTTI 
NULL 
Provvedimenti Del Pm 
NULL 
NULL 
NULL 
NULL 
119 SEGNALAZIONE_FUN
ZIONALITA 
0115 
TUTTI 
NULL 
Provvedimenti Interlocutori 
NULL 
NULL 
NULL 
NULL 
120 SEGNALAZIONE_FUN
ZIONALITA 
0116 
TUTTI 
NULL 
Provvedimenti Magistrato Sorveglianza
NULL 
NULL 
NULL 
NULL 
121 SEGNALAZIONE_FUN
ZIONALITA 
0117 
TUTTI 
NULL 
Provvedimenti Pubblico Ministero 
NULL 
NULL 
NULL 
NULL 
122 SEGNALAZIONE_FUN
ZIONALITA 
0118 
TUTTI 
NULL 
Provvedimento 
NULL 
NULL 
NULL 
NULL 
123 SEGNALAZIONE_FUN
ZIONALITA 
0119 
TUTTI 
NULL 
Provvedimento Pm 
NULL 
NULL 
NULL 
NULL 
124 SEGNALAZIONE_FUN
ZIONALITA 
0120 
TUTTI 
NULL 
Provvedimento Pm 
NULL 
NULL 
NULL 
NULL 
125 SEGNALAZIONE_FUN
ZIONALITA 
0121 
TUTTI 
NULL 
Rateizzazioni 
NULL 
NULL 
NULL 
NULL 
126 SEGNALAZIONE_FUN
ZIONALITA 
0122 
TUTTI 
NULL 
Reati 
NULL 
NULL 
NULL 
NULL 
127 SEGNALAZIONE_FUN
ZIONALITA 
0123 
TUTTI 
NULL 
Rege Circostanza 
NULL 
NULL 
NULL 
NULL 
128 SEGNALAZIONE_FUN
ZIONALITA 
0124 
TUTTI 
NULL 
Rege Notizia Reato 
NULL 
NULL 
NULL 
NULL 
129 SEGNALAZIONE_FUN
ZIONALITA 
0125 
TUTTI 
NULL 
Rege Reato 
NULL 
NULL 
NULL 
NULL 
130 SEGNALAZIONE_FUN
ZIONALITA 
0126 
TUTTI 
NULL 
Rege Residenza 
NULL 
NULL 
NULL 
NULL 
131 SEGNALAZIONE_FUN
ZIONALITA 
0127 
TUTTI 
NULL 
Rege Scarti 
NULL 
NULL 
NULL 
NULL 
132 SEGNALAZIONE_FUN
ZIONALITA 
0128 
TUTTI 
NULL 
Rege Sentenza 
NULL 
NULL 
NULL 
NULL 
133 SEGNALAZIONE_FUN
ZIONALITA 
0129 
TUTTI 
NULL 
Rege Soggetto 
NULL 
NULL 
NULL 
NULL 
134 SEGNALAZIONE_FUN
ZIONALITA 
0130 
TUTTI 
NULL 
Residenza 
NULL 
NULL 
NULL 
NULL 
135 SEGNALAZIONE_FUN
ZIONALITA 
0131 
TUTTI 
NULL 
RGNR 
NULL 
NULL 
NULL 
NULL 
136 SEGNALAZIONE_FUN
ZIONALITA 
0132 
TUTTI 
NULL 
Ricerca per estremi 
NULL 
NULL 
NULL 
NULL 
137 SEGNALAZIONE_FUN
ZIONALITA 
0133 
TUTTI 
NULL 
Ricerca per numero SIEP 
NULL 
NULL 
NULL 
NULL 
138 SEGNALAZIONE_FUN
ZIONALITA 
0134 
TUTTI 
NULL 
Ricerche 
NULL 
NULL 
NULL 
NULL 
139 SEGNALAZIONE_FUN
ZIONALITA 
0135 
TUTTI 
NULL 
Ricerche - Sorveglianza 
NULL 
NULL 
NULL 
NULL

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 78 di 84
Versione n° 0.1 del 04/11/2014
 
N. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
140 SEGNALAZIONE_FUN
ZIONALITA 
0136 
TUTTI 
NULL 
Ricerche Altre BDI 
NULL 
NULL 
NULL 
NULL 
141 SEGNALAZIONE_FUN
ZIONALITA 
0137 
TUTTI 
NULL 
Ricerche E Visualizzazioni 
NULL 
NULL 
NULL 
NULL 
142 SEGNALAZIONE_FUN
ZIONALITA 
0138 
TUTTI 
NULL 
Ricerche Generali 
NULL 
NULL 
NULL 
NULL 
143 SEGNALAZIONE_FUN
ZIONALITA 
0139 
TUTTI 
NULL 
Ricerche Generalizzate 
NULL 
NULL 
NULL 
NULL 
144 SEGNALAZIONE_FUN
ZIONALITA 
0140 
TUTTI 
NULL 
Ricezione Atti 
NULL 
NULL 
NULL 
NULL 
145 SEGNALAZIONE_FUN
ZIONALITA 
0141 
TUTTI 
NULL 
Richiesta 
NULL 
NULL 
NULL 
NULL 
146 SEGNALAZIONE_FUN
ZIONALITA 
0142 
TUTTI 
NULL 
Richiesta Generalità Esatte 
NULL 
NULL 
NULL 
NULL 
147 SEGNALAZIONE_FUN
ZIONALITA 
0143 
TUTTI 
NULL 
Richiesta Restituzione Ordine Di 
Esecuzione Per Concessione 
NULL 
NULL 
NULL 
NULL 
148 SEGNALAZIONE_FUN
ZIONALITA 
0144 
TUTTI 
NULL 
Richiesta Revoca Benefici Amnistia 
NULL 
NULL 
NULL 
NULL 
149 SEGNALAZIONE_FUN
ZIONALITA 
0145 
TUTTI 
NULL 
Richiesta Revoca Benefici Indulto 
NULL 
NULL 
NULL 
NULL 
150 SEGNALAZIONE_FUN
ZIONALITA 
0146 
TUTTI 
NULL 
Richieste - Sorveglianza 
NULL 
NULL 
NULL 
NULL 
151 SEGNALAZIONE_FUN
ZIONALITA 
0147 
TUTTI 
NULL 
Richieste Al Giudice esecuzione 
NULL 
NULL 
NULL 
NULL 
152 SEGNALAZIONE_FUN
ZIONALITA 
0148 
TUTTI 
NULL 
Richieste Al Magistrato Di Sorveglianza 
NULL 
NULL 
NULL 
NULL 
153 SEGNALAZIONE_FUN
ZIONALITA 
0149 
TUTTI 
NULL 
Richieste Al Tribunale Di Sorveglianza 
NULL 
NULL 
NULL 
NULL 
154 SEGNALAZIONE_FUN
ZIONALITA 
0150 
TUTTI 
NULL 
Rinvio Udienza 
NULL 
NULL 
NULL 
NULL 
155 SEGNALAZIONE_FUN
ZIONALITA 
0151 
TUTTI 
NULL 
Ruolo 
NULL 
NULL 
NULL 
NULL 
156 SEGNALAZIONE_FUN
ZIONALITA 
0152 
TUTTI 
NULL 
Sanzione Amministrativa 
NULL 
NULL 
NULL 
NULL 
157 SEGNALAZIONE_FUN
ZIONALITA 
0153 
TUTTI 
NULL 
Sanzione Sostitutiva 
NULL 
NULL 
NULL 
NULL 
158 SEGNALAZIONE_FUN
ZIONALITA 
0154 
TUTTI 
NULL 
Scadenza sollecito per Tribunale 
Ordinanza Est. pena 
NULL 
NULL 
NULL 
NULL 
159 SEGNALAZIONE_FUN
ZIONALITA 
0155 
TUTTI 
NULL 
Scadenzari 
NULL 
NULL 
NULL 
NULL 
160 SEGNALAZIONE_FUN
ZIONALITA 
0156 
TUTTI 
NULL 
Scadenzari – Sorveglianza 
NULL 
NULL 
NULL 
NULL 
161 SEGNALAZIONE_FUN
ZIONALITA 
0157 
TUTTI 
NULL 
Scadenzario 
NULL 
NULL 
NULL 
NULL 
162 SEGNALAZIONE_FUN
ZIONALITA 
0158 
TUTTI 
NULL 
Security 
NULL 
NULL 
NULL 
NULL 
163 SEGNALAZIONE_FUN
ZIONALITA 
0159 
TUTTI 
NULL 
Sentenza 
NULL 
NULL 
NULL 
NULL 
164 SEGNALAZIONE_FUN
ZIONALITA 
0160 
TUTTI 
NULL 
Sentenza 
NULL 
NULL 
NULL 
NULL 
165 SEGNALAZIONE_FUN
ZIONALITA 
0161 
TUTTI 
NULL 
Sezione 
NULL 
NULL 
NULL 
NULL 
166 SEGNALAZIONE_FUN
ZIONALITA 
0162 
TUTTI 
NULL 
Simeone 
NULL 
NULL 
NULL 
NULL 
167 SEGNALAZIONE_FUN
ZIONALITA 
0163 
TUTTI 
NULL 
Soggetto 
NULL 
NULL 
NULL 
NULL 
168 SEGNALAZIONE_FUN
ZIONALITA 
0164 
TUTTI 
NULL 
Soggetto con procedimento 
.Sorveglianza 
NULL 
NULL 
NULL 
NULL 
169 SEGNALAZIONE_FUN
ZIONALITA 
0165 
TUTTI 
NULL 
Sospensione Esecuzione Dpr309 
NULL 
NULL 
NULL 
NULL 
170 SEGNALAZIONE_FUN
ZIONALITA 
0166 
TUTTI 
NULL 
Sospensione Simeone 
NULL 
NULL 
NULL 
NULL 
171 SEGNALAZIONE_FUN
ZIONALITA 
0167 
TUTTI 
NULL 
Stampe Richieste Al Giudice 
NULL 
NULL 
NULL 
NULL

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 79 di 84
Versione n° 0.1 del 04/11/2014
 
N. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
esecuzione
172 SEGNALAZIONE_FUN
ZIONALITA 
0168 
TUTTI 
NULL 
Statistiche/ Monitoraggio 
NULL 
NULL 
NULL 
NULL 
173 SEGNALAZIONE_FUN
ZIONALITA 
0169 
TUTTI 
NULL 
Stato Esecuzione 
NULL 
NULL 
NULL 
NULL 
174 SEGNALAZIONE_FUN
ZIONALITA 
0170 
TUTTI 
NULL 
Stato Richieste 
NULL 
NULL 
NULL 
NULL 
175 SEGNALAZIONE_FUN
ZIONALITA 
0171 
TUTTI 
NULL 
Storico Soggetto 
NULL 
NULL 
NULL 
NULL 
176 SEGNALAZIONE_FUN
ZIONALITA 
0172 
TUTTI 
NULL 
Test 
NULL 
NULL 
NULL 
NULL 
177 SEGNALAZIONE_FUN
ZIONALITA 
0173 
TUTTI 
NULL 
Titolo Esecutivo Per Soggetto 
NULL 
NULL 
NULL 
NULL 
178 SEGNALAZIONE_FUN
ZIONALITA 
0174 
TUTTI 
NULL 
Trasmissione Per Competenza 
NULL 
NULL 
NULL 
NULL 
179 SEGNALAZIONE_FUN
ZIONALITA 
0175 
TUTTI 
NULL 
Udienza 
NULL 
NULL 
NULL 
NULL 
180 SEGNALAZIONE_FUN
ZIONALITA 
0176 
TUTTI 
NULL 
Udienza - Sorveglianza 
NULL 
NULL 
NULL 
NULL 
181 SEGNALAZIONE_FUN
ZIONALITA 
0177 
TUTTI 
NULL 
Udienza Collegiale 
NULL 
NULL 
NULL 
NULL 
182 SEGNALAZIONE_FUN
ZIONALITA 
0178 
TUTTI 
NULL 
Udienza Monocratica 
NULL 
NULL 
NULL 
NULL 
183 SEGNALAZIONE_FUN
ZIONALITA 
0179 
TUTTI 
NULL 
Udienze 
NULL 
NULL 
NULL 
NULL 
184 SEGNALAZIONE_FUN
ZIONALITA 
0180 
TUTTI 
NULL 
Ufficio 
NULL 
NULL 
NULL 
NULL 
185 SEGNALAZIONE_FUN
ZIONALITA 
0181 
TUTTI 
NULL 
Ulteriore Periodo 
NULL 
NULL 
NULL 
NULL 
186 SEGNALAZIONE_FUN
ZIONALITA 
0182 
TUTTI 
NULL 
Unificazione Procedimenti 
NULL 
NULL 
NULL 
NULL 
187 SEGNALAZIONE_FUN
ZIONALITA 
0183 
TUTTI 
NULL 
Unificazioni 
NULL 
NULL 
NULL 
NULL 
188 SEGNALAZIONE_FUN
ZIONALITA 
0184 
TUTTI 
NULL 
Utenti 
NULL 
NULL 
NULL 
NULL 
189 SEGNALAZIONE_FUN
ZIONALITA 
0185 
TUTTI 
NULL 
Validazione Fascicolo 
NULL 
NULL 
NULL 
NULL 
190 SEGNALAZIONE_FUN
ZIONALITA 
0186 
TUTTI 
NULL 
Verbali 
NULL 
NULL 
NULL 
NULL 
191 SEGNALAZIONE_FUN
ZIONALITA 
0187 
TUTTI 
NULL 
Verbali Arresto/Vane Ricerche 
NULL 
NULL 
NULL 
NULL 
Tabella 50 – Funzionalità Sies 
 
N
. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
192 SEGNALAZIONE_FUN
ZIONALITA 
0001 
SIEP 
NULL 
Altri Gradi Giudizio 
NULL 
NULL 
NULL 
NULL 
193 SEGNALAZIONE_FUN
ZIONALITA 
0002 
SIEP 
NULL 
Archiviazione 
NULL 
NULL 
NULL 
NULL 
194 SEGNALAZIONE_FUN
ZIONALITA 
0003 
SIEP 
NULL 
Beneficio 
NULL 
NULL 
NULL 
NULL 
195 SEGNALAZIONE_FUN
ZIONALITA 
0004 
SIEP 
NULL 
Calcolo Pena 
NULL 
NULL 
NULL 
NULL 
196 SEGNALAZIONE_FUN
ZIONALITA 
0005 
SIEP 
NULL 
Certificato Stato Esecuzione 
NULL 
NULL 
NULL 
NULL 
197 SEGNALAZIONE_FUN
ZIONALITA 
0006 
SIEP 
NULL 
Circostanza 
NULL 
NULL 
NULL 
NULL 
198 SEGNALAZIONE_FUN
ZIONALITA 
0007 
SIEP 
NULL 
Continuazione 
NULL 
NULL 
NULL 
NULL 
199 SEGNALAZIONE_FUN
ZIONALITA 
0008 
SIEP 
NULL 
Documenti 
NULL 
NULL 
NULL 
NULL

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 80 di 84
Versione n° 0.1 del 04/11/2014
 
N
. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
200 SEGNALAZIONE_FUN
ZIONALITA 
0009 
SIEP 
NULL 
Iscrizione Guidata 
NULL 
NULL 
NULL 
NULL 
201 SEGNALAZIONE_FUN
ZIONALITA 
0010 
SIEP 
NULL 
Istituto Detenzione 
NULL 
NULL 
NULL 
NULL 
202 SEGNALAZIONE_FUN
ZIONALITA 
0011 
SIEP 
NULL 
Istruttoria 
NULL 
NULL 
NULL 
NULL 
203 SEGNALAZIONE_FUN
ZIONALITA 
0012 
SIEP 
NULL 
Istruttoria Cumulo 
NULL 
NULL 
NULL 
NULL 
204 SEGNALAZIONE_FUN
ZIONALITA 
0013 
SIEP 
NULL 
Ma Rigetto 
NULL 
NULL 
NULL 
NULL 
205 SEGNALAZIONE_FUN
ZIONALITA 
0014 
SIEP 
NULL 
Modulo Cumulo 
NULL 
NULL 
NULL 
NULL 
206 SEGNALAZIONE_FUN
ZIONALITA 
0015 
SIEP 
NULL 
Note Fascicolo 
NULL 
NULL 
NULL 
NULL 
207 SEGNALAZIONE_FUN
ZIONALITA 
0016 
SIEP 
NULL 
Notizia Reato 
NULL 
NULL 
NULL 
NULL 
208 SEGNALAZIONE_FUN
ZIONALITA 
0017 
SIEP 
NULL 
Nuova Istanza 
NULL 
NULL 
NULL 
NULL 
209 SEGNALAZIONE_FUN
ZIONALITA 
0018 
SIEP 
NULL 
Ordine Scarcerazione 
NULL 
NULL 
NULL 
NULL 
210 SEGNALAZIONE_FUN
ZIONALITA 
0019 
SIEP 
NULL 
Parametro 
NULL 
NULL 
NULL 
NULL 
211 SEGNALAZIONE_FUN
ZIONALITA 
0020 
SIEP 
NULL 
Pena Residua 
NULL 
NULL 
NULL 
NULL 
212 SEGNALAZIONE_FUN
ZIONALITA 
0021 
SIEP 
NULL 
Posizione 
NULL 
NULL 
NULL 
NULL 
213 SEGNALAZIONE_FUN
ZIONALITA 
0022 
SIEP 
NULL 
Provvedimento Generico 
NULL 
NULL 
NULL 
NULL 
214 SEGNALAZIONE_FUN
ZIONALITA 
0023 
SIEP 
NULL 
Reato Predisposto 
NULL 
NULL 
NULL 
NULL 
215 SEGNALAZIONE_FUN
ZIONALITA 
0024 
SIEP 
NULL 
Revoca 
NULL 
NULL 
NULL 
NULL 
216 SEGNALAZIONE_FUN
ZIONALITA 
0025 
SIEP 
NULL 
Rinnovo 
NULL 
NULL 
NULL 
NULL 
217 SEGNALAZIONE_FUN
ZIONALITA 
0026 
SIEP 
NULL 
Ripristino 
NULL 
NULL 
NULL 
NULL 
218 SEGNALAZIONE_FUN
ZIONALITA 
0027 
SIEP 
NULL 
Risultato Ricerca 
NULL 
NULL 
NULL 
NULL 
219 SEGNALAZIONE_FUN
ZIONALITA 
0028 
SIEP 
NULL 
Scambio Sanzione 
NULL 
NULL 
NULL 
NULL 
220 SEGNALAZIONE_FUN
ZIONALITA 
0029 
SIEP 
NULL 
Scarti 
NULL 
NULL 
NULL 
NULL 
221 SEGNALAZIONE_FUN
ZIONALITA 
0030 
SIEP 
NULL 
Sentenza Riunita 
NULL 
NULL 
NULL 
NULL 
222 SEGNALAZIONE_FUN
ZIONALITA 
0031 
SIEP 
NULL 
Sospensione 
NULL 
NULL 
NULL 
NULL 
223 SEGNALAZIONE_FUN
ZIONALITA 
0032 
SIEP 
NULL 
Stato Procedimento 
NULL 
NULL 
NULL 
NULL 
Tabella 51 – Funzionalità Siep 
 
N
. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
224 SEGNALAZIONE_FUN
ZIONALITA 
0001 
SIEPE 
NULL 
Assistente Sociale Attività 
NULL 
NULL 
NULL 
NULL 
225 SEGNALAZIONE_FUN
ZIONALITA 
0002 
SIEPE 
NULL 
Esperto Attività 
NULL 
NULL 
NULL 
NULL 
226 SEGNALAZIONE_FUN
ZIONALITA 
0003 
SIEPE 
NULL 
Relazione 
NULL 
NULL 
NULL 
NULL 
Tabella 52 – Funzionalità Siepe

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 81 di 84
Versione n° 0.1 del 04/11/2014
 
N
. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
227 SEGNALAZIONE_FUN
ZIONALITA 
0001 
SIGE 
NULL 
Collegio 
NULL 
NULL 
NULL 
NULL 
228 SEGNALAZIONE_FUN
ZIONALITA 
0002 
SIGE 
NULL 
Decreto Unificazione 
NULL 
NULL 
NULL 
NULL 
229 SEGNALAZIONE_FUN
ZIONALITA 
0003 
SIGE 
NULL 
Detenzione 
NULL 
NULL 
NULL 
NULL 
230 SEGNALAZIONE_FUN
ZIONALITA 
0004 
SIGE 
NULL 
Impugnazione 
NULL 
NULL 
NULL 
NULL 
231 SEGNALAZIONE_FUN
ZIONALITA 
0005 
SIGE 
NULL 
Magistrato Assegnatario 
NULL 
NULL 
NULL 
NULL 
232 SEGNALAZIONE_FUN
ZIONALITA 
0006 
SIGE 
NULL 
Produzione atti 
NULL 
NULL 
NULL 
NULL 
233 SEGNALAZIONE_FUN
ZIONALITA 
0007 
SIGE 
NULL 
Richiesta Atti 
NULL 
NULL 
NULL 
NULL 
234 SEGNALAZIONE_FUN
ZIONALITA 
0008 
SIGE 
NULL 
Tenore 
NULL 
NULL 
NULL 
NULL 
235 SEGNALAZIONE_FUN
ZIONALITA 
0009 
SIGE 
NULL 
Unificazione 
NULL 
NULL 
NULL 
NULL 
Tabella 53 – Funzionalità Sige 
 
 
N
. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
236 SEGNALAZIONE_FUN
ZIONALITA 
0001 
SIUS 
NULL 
Collaboratore 
NULL 
NULL 
NULL 
NULL 
237 SEGNALAZIONE_FUN
ZIONALITA 
0002 
SIUS 
NULL 
Deposito Decreto 
NULL 
NULL 
NULL 
NULL 
238 SEGNALAZIONE_FUN
ZIONALITA 
0003 
SIUS 
NULL 
Deposito Ordinanza Pc 
NULL 
NULL 
NULL 
NULL 
239 SEGNALAZIONE_FUN
ZIONALITA 
0004 
SIUS 
NULL 
Documento allegato 
NULL 
NULL 
NULL 
NULL 
240 SEGNALAZIONE_FUN
ZIONALITA 
0005 
SIUS 
NULL 
Esecuzione Misura Alternativa 
NULL 
NULL 
NULL 
NULL 
241 SEGNALAZIONE_FUN
ZIONALITA 
0006 
SIUS 
NULL 
Esecuzione Misura Sicurezza 
NULL 
NULL 
NULL 
NULL 
242 SEGNALAZIONE_FUN
ZIONALITA 
0007 
SIUS 
NULL 
Esecuzione Sanzione Sostitutiva 
NULL 
NULL 
NULL 
NULL 
243 SEGNALAZIONE_FUN
ZIONALITA 
0008 
SIUS 
NULL 
Generale Procedimento 
NULL 
NULL 
NULL 
NULL 
244 SEGNALAZIONE_FUN
ZIONALITA 
0009 
SIUS 
NULL 
Luogo Detenzione 
NULL 
NULL 
NULL 
NULL 
245 SEGNALAZIONE_FUN
ZIONALITA 
0010 
SIUS 
NULL 
Magistrato Relatore 
NULL 
NULL 
NULL 
NULL 
246 SEGNALAZIONE_FUN
ZIONALITA 
0011 
SIUS 
NULL 
Misure Sicurezza Richiesta Atti 
NULL 
NULL 
NULL 
NULL 
247 SEGNALAZIONE_FUN
ZIONALITA 
0012 
SIUS 
NULL 
Motivazione Decreto 
NULL 
NULL 
NULL 
NULL 
248 SEGNALAZIONE_FUN
ZIONALITA 
0013 
SIUS 
NULL 
Permesso 
NULL 
NULL 
NULL 
NULL 
249 SEGNALAZIONE_FUN
ZIONALITA 
0014 
SIUS 
NULL 
Presa In Carico 
NULL 
NULL 
NULL 
NULL 
250 SEGNALAZIONE_FUN
ZIONALITA 
0015 
SIUS 
NULL 
Prescrizione 
NULL 
NULL 
NULL 
NULL 
251 SEGNALAZIONE_FUN
ZIONALITA 
0016 
SIUS 
NULL 
Remissione Debito 
NULL 
NULL 
NULL 
NULL 
252 SEGNALAZIONE_FUN
ZIONALITA 
0017 
SIUS 
NULL 
Stralcio 
NULL 
NULL 
NULL 
NULL 
253 SEGNALAZIONE_FUN
ZIONALITA 
0018 
SIUS 
NULL 
Titolo Esecutivo 
NULL 
NULL 
NULL 
NULL 
254 SEGNALAZIONE_FUN
ZIONALITA 
0019 
SIUS 
NULL 
Trasmissione Atti 
NULL 
NULL 
NULL 
NULL

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 82 di 84
Versione n° 0.1 del 04/11/2014
 
N
. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
255 SEGNALAZIONE_FUN
ZIONALITA 
0020 
SIUS 
NULL 
Ulteriore Istanza 
NULL 
NULL 
NULL 
NULL 
Tabella 54 – Funzionalità Sius 
 
N
. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
256SEGNALAZIONE_AZI
ONE 
01 
NULL 
NULL 
Cancella 
NULL 
NULL 
NULL 
NULL 
257SEGNALAZIONE_AZI
ONE 
02 
NULL 
NULL 
Dettaglio 
NULL 
NULL 
NULL 
NULL 
258SEGNALAZIONE_AZI
ONE 
03 
NULL 
NULL 
Elenco 
NULL 
NULL 
NULL 
NULL 
259SEGNALAZIONE_AZI
ONE 
04 
NULL 
NULL 
Excel 
NULL 
NULL 
NULL 
NULL 
260SEGNALAZIONE_AZI
ONE 
05 
NULL 
NULL 
Inserimento 
NULL 
NULL 
NULL 
NULL 
261SEGNALAZIONE_AZI
ONE 
06 
NULL 
NULL 
Modifica 
NULL 
NULL 
NULL 
NULL 
262SEGNALAZIONE_AZI
ONE 
07 
NULL 
NULL 
Ricerca 
NULL 
NULL 
NULL 
NULL 
263SEGNALAZIONE_AZI
ONE 
08 
NULL 
NULL 
Stampa 
NULL 
NULL 
NULL 
NULL 
264SEGNALAZIONE_AZI
ONE 
09 
NULL 
NULL 
Trasferimento 
NULL 
NULL 
NULL 
NULL 
265SEGNALAZIONE_AZI
ONE 
10 
NULL 
NULL 
Variazione 
NULL 
NULL 
NULL 
NULL 
Tabella 55 – Azioni 
 
N
. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
266SEGNALAZIONE_TIP
OLOGIA 
01 
NULL 
NULL 
Adeguamento normativo 
NULL 
NULL 
NULL 
NULL 
267SEGNALAZIONE_TIP
OLOGIA 
02 
NULL 
NULL 
Errore bloccante 
NULL 
NULL 
NULL 
NULL 
268SEGNALAZIONE_TIP
OLOGIA 
03 
NULL 
NULL 
Errore non bloccante 
NULL 
NULL 
NULL 
NULL 
269SEGNALAZIONE_TIP
OLOGIA 
04 
NULL 
NULL 
Miglioramento funzionale 
NULL 
NULL 
NULL 
NULL 
270SEGNALAZIONE_TIP
OLOGIA 
05 
NULL 
NULL 
Miglioramento Grafico 
NULL 
NULL 
NULL 
NULL 
271SEGNALAZIONE_TIP
OLOGIA 
06 
NULL 
NULL 
Nuova funzionalità 
NULL 
NULL 
NULL 
NULL 
Tabella 56 – Tipologia 
 
N
. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
272SEGNALAZIONE_GRA
VITA 
01 
NULL 
NULL 
Molto Alta 
NULL 
NULL 
NULL 
NULL 
273SEGNALAZIONE_GRA
VITA 
02 
NULL 
NULL 
Alta 
NULL 
NULL 
NULL 
NULL 
274SEGNALAZIONE_GRA
VITA 
03 
NULL 
NULL 
Media 
NULL 
NULL 
NULL 
NULL 
275SEGNALAZIONE_GRA
VITA 
04 
NULL 
NULL 
Bassa 
NULL 
NULL 
NULL 
NULL

Ministero della Giustizia 
 Analisi funzionale Mev SIEP 
Codice Documento: SIEP_PNL_AF
Pag. 83 di 84
Versione n° 0.1 del 04/11/2014
 
N
. 
RV_DOMAIN 
RV_LO
W_VAL
UE 
RV_HIG
H_VALU
E 
RV_ABB
REVIATI
ON 
RV_MEANING 
RV_ALT
2_VALU
E 
RV_ALT
3_VALU
E 
RV_ALT4
_VALUE 
RV_ALT5_V
ALUE 
276SEGNALAZIONE_GRA
VITA 
05 
NULL 
NULL 
Molto Bassa 
NULL 
NULL 
NULL 
NULL 
Tabella 57 – Gravità 
L’intervento prevede l’inserimento nella tabella <FUNZIONE> dei seguenti record: 
N. 
ID_FUNZIONE 
DESCRIZIONE 
COD_
TIPO_
FUNZI
ONE 
AZIONE_CONTESTO_JAVA 
277. XX.YYY.ZZZ 
Invia segnalazione 
Z 
 
Tabella 58 – Gravità 
 
21.11 Modifica template 
Nessuna modifica prevista.