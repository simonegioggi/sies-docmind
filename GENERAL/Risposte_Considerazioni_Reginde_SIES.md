---
uniqueName: risposteconsiderazioniregindesies
displayName: "Risposte Considerazioni Reginde SIES"
category: "GENERAL"
tags: []
---

# Risposte_Considerazioni_Reginde_SIES

> **File originale:** `MEV/SCHEDA_021/Docs/Riscontri DGSIA/Risposte_Considerazioni_Reginde_SIES.docx`  
> **Tipo:** DOCX

---

Paragrafo 6.2 pag. 40: bisogna che l’RTI preveda dei test specifici per simulare il malfunzionamento del Reginde per verificare come avviene la ricerca sulla base dati locale.
Ci sono due modi per testare questo malfunzionamento:
Inserire nella maschera di ricerca del difensore su ReGIndE il cognome “Test”

e premere il tasto “Cerca su ReGIndE”:

Premere il tasto “OK” sulla popup risultante e si potrà effettuare la ricerca sulla base dati locale.

Oppure nel file “f3b.properties”, presente nel percorso “/var/SIES/CONFIG”, commentare col carattere “#” la seguente riga necessaria al collegamento col server nazionale del sistema ReGIndE:
#EndpointAddress=http://reginde.processotelematicotest.giustizia.it
e procedere col test come nel punto i); una volta premuto il tasto “Cerca su ReGIndE” si otterrà il messaggio come in figura sottostante:

Premere il tasto “OK” sulla popup risultante e si potrà effettuare la ricerca sulla base dati locale.

Paragrafo 6.2.5 pag. 71: va indicato l’url corretto del Reginde.
•	Per il pre-esercizio è http://reginde.processotelematicotest.giustizia.it
•	Per l’esercizio è http://reginde.processotelematico.giustizia.it
La frase in questione sarà modificata da:
L’endpoint di interesse è identificato dalla seguente url:
https://XX.XXX.XXXX.XXX/ServiziInterrogazioneRegindeExt/ServiziInterrogazioneInterni
e l’operazione, servizio applicativo a cui fare accesso, è ‘ricercaSoggettoComplete’.
a:
L’endpoint di interesse è identificato dalla seguente url:
http://reginde.processotelematicotest.giustizia.it	(ambiente di pre-esercizio)
http://reginde.processotelematico.giustizia.it	(ambiente di esercizio)
e l’operazione, servizio applicativo a cui fare accesso, è ‘ricercaSoggettoComplete’.

Paragrafo 6.2.5.2 pag. 73 devono essere inseriti gli interventi necessari per l’eventuale funzionamento con il protocollo TLS 1.0
Nel file “standalone-full.xml” presente nel percorso “/home/SIES/jboss-eap-6.4.Alpha/standalone/configuration” nel paragrafo dedicato alle proprietà di sistema, nella dicitura (già presente):
<property name="jdk.tls.client.protocols" value="SSLv2Hello,SSLv3,TLSv1"/>
Il parametro “TLSv1” abilita i protocolli TLSv1, TLSv1.1 e TLSv1.2, quindi non vi è alcun intervento da eseguire.
Lato java per TLSv1.2 potrebbe essere necessario:
System.setProperty("jdk.tls.client.protocols","SSLv2Hello,SSLv3,TLSv1");
System.setProperty("https.protocols", "TLSv1,TLSv1.1,TLSv1.2");

Paragrafo 6.2.7 pag. 73 va integrato secondo quanto indicato al punto b), indicando anche cosa fare in previsione del passaggio ad https.
La frase in questione sarà modificata da:
Per la connessione ai servizi in https sul sistema ReGIndE è da prevedere l’importazione della chiave pubblica (certificato ssl) che mappa il DNS del server su cui è esposto il servizio
ES:  https://reginde/ServiziInterrogazioneRegindeExt/ServiziInterrogazioneInterni
Il certificato deve essere importato nel file keystore del sies (trustore.jks) posizionato al /var/SIES/CONFIG/certs.
a:
Per la connessione ai servizi in https sul sistema ReGIndE è da prevedere l’importazione della chiave pubblica (certificato ssl) che mappa il DNS del server su cui è esposto il servizio
ES:
https://reginde.processotelematicotest.giustizia.it	(ambiente di pre-esercizio)
http://reginde.processotelematico.giustizia.it	(ambiente di esercizio)
Il certificato deve essere importato nel file keystore del sies (trustore.jks) posizionato al /var/SIES/CONFIG/certs.
HTTPS:
Per una connessione basata su protocollo https:
posizionarsi sotto la cartella: “/var/SIES/CONFIG/certs”;
aggiornare il file trustStore “sies.jks”, importando, con procedura nota all’Amministrazione, la catena di certificati ed il certificato necessari al colloquio con la macchina server che espone il servizio web.
NB: i certificati da importare devono essere resi disponibili dai referenti del sistema REGINDE e correlati all’ambiente predisposto per la verifica di conformità.

Paragrafo 6.3.3 pag. 74 lo stile grafico delle interfacce non sembra essere identico a quello dell’attuale SIES.
Occorre sostituire la popup nella schermata attuale incriminata con la seguente: