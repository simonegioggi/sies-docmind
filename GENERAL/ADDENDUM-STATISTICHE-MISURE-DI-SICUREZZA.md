---
uniqueName: addendum-statistiche-misure-di-sicurezza
displayName: "ADDENDUM STATISTICHE MISURE DI SICUREZZA"
category: "GENERAL"
tags: []
---

# ADDENDUM STATISTICHE MISURE DI SICUREZZA

> **File originale:** `MEV/VERSIONE_SIES_11.3_NEW/MEV_39/ADDENDUM STATISTICHE MISURE DI SICUREZZA.docx`  
> **Tipo:** DOCX

---

ADDENDUM STATISTICHE MISURE DI SICUREZZA

Statistica Riepilogo Iscrizioni e Tipologia Misura

Il primo foglio della statistica deve riportare il riepilogo delle iscrizioni di procedimenti di  Misure di Sicurezza suddivise tra:
Applicate in sentenza di condanna
Applicate in sentenza di assoluzione
Applicate dal Magistrato di Sorveglianza
Applicate dal Magistrato di Sorveglianza (su richiesta Pubblico Ministero)
Applicate dal Giudice di Cognizione (provvisoria)
Applicate dal Tribunale di sorveglianza (impugnazione ex art 680 c.p.p.)
Determinate in Cumulo
Pervenute per competenza territoriale ex artt. 658- 679 comma 1 c.p.p.
Pervenute per competenza all’esecuzione artt. 658 - 659 comma 2 c.p.p.
Procedimenti iscritti per errore

Le voci delle varie tipologie su riportate NON SONO VISUALIZZATE se non vengono trovate corrispondenze per il periodo indicato.

Il fascicolo con la misura di sicurezza rientra nella categoria di ‘Applicate in sentenza di condanna’ quando per il fascicolo di classe I o classe IV esiste una pena complessiva.  (Vista oracle interessata VW_MS_APPL_SENT_COND).

Il fascicolo con la misura di sicurezza rientra nella categoria di ‘Applicate in sentenza di assoluzione’ quando per il fascicolo di classe I o classe IV NON esiste una pena complessiva. (Vista oracle interessata VW_MS_APPL_SENT_ASS).

Il fascicolo con la misura di sicurezza rientra nella categoria di ‘Applicate dal Magistrato di Sorveglianza’ quando la misura risulta applicata con ordinanza dalla Sorveglianza senza una richiesta di dichiarazione di abituabilità/professionalità nel reato da parte della Procura. (Vista oracle interessata VW_MS_APPL_MAG_SORV).

Il fascicolo con la misura di sicurezza rientra nella categoria di ‘Applicate dal Magistrato di Sorveglianza (su richiesta Pubblico Ministero)’ quando la misura risulta applicata con ordinanza dalla Sorveglianza a seguito di una richiesta di dichiarazione di abituabilità/professionalità nel reato da parte della Procura con uno de seguenti esiti:
Accerta  pericolosita' sociale e ordina esecuzione misura sicurezza
Dichiara delinquenza professionale e applica la misura sicurezza
Dichiara delinquenza abituale e applica la misura sicurezza
Dichiara delinquenza per tendenza e applica la misura sicurezza
Accerta Pericolosita' Sociale, unifica le m.s. e ne ordina l'esecuzione
Dichiara abitualita' nelle contravvenzioni e applica la m.s.
(Vista oracle interessata VW_MS_APPL_MAG_SORV_RICH_SIEP).

Il fascicolo di classe IV rientra nella categoria di ‘Applicate dal Giudice di Cognizione (provvisoria)’ quando la misura nasce da un’iscrizione provvisoria. (Vista oracle interessata VW_MS_APPL_GIU_COGNIZIONE).

Il fascicolo con la misura di sicurezza rientra nella categoria di ‘Applicate dal Tribunale di sorveglianza (impugnazione ex art 680 c.p.p.)’  quando per il fascicolo di classe I o classe IV esiste un provvedimento emesso dal Tribunale Sorveglianza relativo ad uno dei seguenti oggetti:
Impugnazione Contro Provvedimento Mds
Appello Contro Sentenza Giudice di Merito
Declaratoria sospensione Sentenza/Ordinanza impugnata (680/3)
con esito:
Accoglie appello e modifica provvedimento MdS
Accoglie sospensione
Accoglie Appello e Revoca Provvedimento
Accoglie Appello e Applica la Misura
(Vista oracle interessata VW_MS_APPL_TRIB_SORV_IMPUGN).

Il fascicolo di classe IV rientra nella categoria di Misure di Sicurezza ‘Determinate in Cumulo’ quando il fascicolo collegato al procedimento di classe IV è un cumulo. Quindi si va a verificare  che nell’elenco dei titoli coinvolti nel cumulo ci sia un procedimento proveniente da un ufficio diverso che abbia misure di sicurezza e che abbia come stato del fascicolo ‘Trasmessi Atti per competenza per emissione provvedimento di cumulo’.   (Vista oracle interessata VW_MS_CUMULO).

Il fascicolo di classe IV o classe I con la misura di sicurezza rientra nella categoria di ‘Pervenute per competenza territoriale ex artt. 658- 679 comma 1 c.p.p.’ quando il fascicolo collegato ha come stato del fascicolo ‘Trasmessi Atti per competenza ex artt. 658 e 679 comma 1 c.p.p.’
(Vista oracle interessata VW_MS_COMPET_TERRIT_C1).

Il fascicolo di classe IV o classe I con la misura di sicurezza rientra nella categoria di ‘Pervenute per competenza territoriale ex artt. 658- 679 comma 2 c.p.p.’ quando il fascicolo collegato ha come stato del fascicolo ‘Trasmessi Atti per competenza ex artt. 658 e 679 comma 2 c.p.p.’
(Vista oracle interessata VW_MS_COMPET_TERRIT_C2).

Il fascicolo di classe IV con la misura di sicurezza rientra nella categoria di ‘Iscritti per Errore’ quando il fascicolo risulta Archiviato/Definito e l’oggetto definizione è uguale a ‘Iscritti per Errore’.
(Vista oracle interessata VW_MS_PROC_ISCR_PER_ERRORE).

Il secondo foglio della statistica riporta il riepilogo generale delle misure suddivise per Tipologia Misura di Sicurezza.
Il terzo foglio, dettaglio procedimenti di misura di sicurezza per tipologia di iscrizione, fornisce il riepilogo delle iscrizioni di misure, per anno e tipologia.


Statistica per Procedimenti Pendenti nel Periodo

Con la statistica in oggetto si chiede di elaborare un calcolo dei procedimenti in materia di misure di sicurezza (classe IV), in modo da riportare, in base al periodo prescelto, le seguenti informazioni:

Procedimenti pendenti inizio periodo
Procedimenti sopravvenuti nel periodo
Procedimenti esauriti nel periodo
Procedimenti riaperti
Procedimenti pendenti fine periodo

Procedimenti pendenti inizio periodo
Rappresentano tutti i procedimenti non definiti/non archiviati per i quali la data di iscrizione è minore della data inizio elaborazione della statistica.
(Vista oracle interessata VW_MS_PROC_INIZIO_FINE_PERIODO).

Procedimenti sopravvenuti nel periodo
Rappresentano tutti i procedimenti per i quali la data di iscrizione, a prescindere dallo stato del procedimento, è compresa tra la data inizio e la data fine elaborazione della statistica.
(Vista oracle interessata VW_MS_PROCEDIMENTI).

Procedimenti esauriti nel periodo
Rappresentano tutti i procedimenti che hanno assunto lo stato di Archiviato\Definito nel periodo della statistica e per i quali la data di iscrizione è compresa tra la data inizio e la data fine elaborazione della statistica.
(Vista oracle interessata VW_MS_PROC_ESAURITI).
Procedimenti riaperti
Rappresentano tutti i procedimenti per i quali la data di iscrizione è compresa tra la data inizio e la data fine elaborazione della statistica con provvedimento e per i quali è stato chiesto l’annullamento dello stato Archiviato\Definito.
(Vista oracle interessata VW_MS_PROC_RIAPERTI).

Procedimenti pendenti fine periodo
Rappresentano i tutti i procedimenti che hanno lo stato “non definiti” per i quali la data di iscrizione è minore della data fine elaborazione della statistica.
(Vista oracle interessata VW_MS_PROC_INIZIO_FINE_PERIODO).

Movimento Procedimenti (Riepilogo Procedimenti Pendenti)

Il package oracle che si occupa della statistica in oggetto è ISPETTORATO_MS ed in particolare la procedura stat_provvedimenti.
L’algoritmo di estrazione dei dati, va ad estrapolare i soli procedimenti la cui data_iscrizione è compresa nell’intervallo specificato e lo stato attuale del procedimento è quello di interesse dell’utente. Non è possibile risalire allo stato in cui si trovava un determinato procedimento per una data specificata in quanto il sistema SIES non gestisce lo storico dello stato del procedimento.
La procedura pertanto lavora sulla stato che assume il procedimento al momento dell’elaborazione della statistica.

Statistica Attività Magistrati
Le statistiche inerenti al Lavoro Magistrati possono essere di due tipologie:
Per Procedimenti Pendenti

Per la statistica in oggetto vengono interrogate le seguenti viste oracle:

VW_MS_PROC_PERIODO_MAG
VW_MS_PROCEDIMENTI_MAG
VW_MS_PROC_ESAURITI_MAG
VW_MS_PROC_RIAPERTI_MAG
VW_MS_PROC_PERIODO_MAG


I vari fogli previsti in statistica, NON SONO VISUALIZZATI se non vengono trovate corrispondenze per il periodo indicato.

Per Attività Magistrati

Il package oracle che si occupa della statistica in oggetto è ISPETTORATO_MS ed in particolare la procedura attivita_magistrati.