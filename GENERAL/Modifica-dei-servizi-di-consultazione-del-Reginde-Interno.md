---
uniqueName: modifica-dei-servizi-di-consultazione-del-reginde-
displayName: "Modifica dei servizi di consultazione del Reginde Interno"
category: "GENERAL"
tags: []
---

# Modifica dei servizi di consultazione del Reginde Interno

> **File originale:** `MEV/SCHEDA_021/Modifiche_ReGIndE/Modifica dei servizi di consultazione del Reginde Interno.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
Versione 1 del 18/03/2022 
 
STORIA DELLE REVISIONI 
 
Versione 
Data 
Motivazione 
1 
18/03/2022 
Prima emissione  
 
Modifica dei servizi Interni di consultazione del 
Reginde 
Servizi Interrogazione Interni  
Vengono modificate le logiche dei servizi esposti ai sistemi interni tramite il wsdl 
ServiziInterrogazioneInterni.wsdl, namespace 
“http://www.giustizia.it/serviziTelematici/reginde/interrogazioniInt”.  
In particolare i servizi che vengono modificati sono:  
 
ricercaEnteComplete  
 
ricercaSoggettoComplete  
In ciascun servizio viene aggiunto un controllo sullo stato dei ruoli che possiede il soggetto in modo da 
visualizzare solo i soggetti che possiedono almeno un ruolo con stato "attivo" e le sole informazioni inerenti 
ai ruoli in tale stato. Non saranno più restituiti gli stati “cancellato”, “radiato” e “sospeso. 
Inoltre vengono modificati per non restituire gli enti e le PA cancellate. 
Si precisa che vengono modificati gli output di tali servizi per l’integrazione delle nuove informazioni 
inserite nel sistema. 
Per maggiori informazioni consultare il wsdl allegato. 
Di seguito un esempio di chiamata e risposta con il nuovo wsdl: 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" 
xmlns:int="http://www.giustizia.it/serviziTelematici/reginde/interrogazioniInt"> 
   <soapenv:Header/> 
   <soapenv:Body> 
      <int:ricercaSoggettoComplete> 
         <cognome></cognome> 
         <nome></nome> 
         <codiceFiscale>DPMDML80A01A944W</codiceFiscale> 
         <indirizzo></indirizzo> 
         <codiceEnte></codiceEnte> 
         <orderBy></orderBy> 
         <asc></asc> 
      </int:ricercaSoggettoComplete> 
   </soapenv:Body>

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
Versione 1 del 18/03/2022 
 
</soapenv:Envelope> 
 
 
 
<env:Envelope xmlns:env="http://schemas.xmlsoap.org/soap/envelope/"> 
   <env:Header/> 
   <env:Body> 
      <ns2:ricercaSoggettoCompleteResponse 
xmlns:ns2="http://www.giustizia.it/serviziTelematici/reginde/interrogazioniInt"> 
         <return> 
            <ruoliente> 
               <codiceFiscale>00794470377</codiceFiscale> 
               <codice>ENTEIMOLA1</codice> 
               <descrizione>Comune di Imola</descrizione> 
               <id>4028b0c57f6daac5017f6e0dbd73002d</id> 
               <indirizziAbilitati> 
                  <id>4028b0c07f72d42d017f736da94300b6</id> 
                  <email>avvocato2.avvocato2@pec.esempio.it</email> 
                  <codiceFiscale>VVCVCT56A01A944F</codiceFiscale> 
               </indirizziAbilitati> 
               <pubblicaAmministrazione>false</pubblicaAmministrazione> 
               <ruolo>avvocato</ruolo> 
               <stato>attivo</stato> 
               <tipologia> 
                  <id>D99F6E8181C67D17E050A8C02E306A78</id> 
                  <descrizione>Altri Enti</descrizione> 
                  <tipo>ENTE</tipo> 
               </tipologia> 
               <visibile>true</visibile> 
            </ruoliente> 
            <ruoliente> 
               <classe>ART</classe> 
               <codiceFiscale>23232312323</codiceFiscale> 
               <codice>K9</codice> 
               <descrizione>L'ENTE</descrizione> 
               <id>4028adc16427c833016446cad8dd061c</id> 
               <indirizziAbilitati> 
                  <id>6FB56CF46339EB79E050A8C02E2D730A</id> 
                  <email>avvocato2.avvocato2@pec.esempio.it</email> 
                  <codiceFiscale>VVCVCT56A01A944F</codiceFiscale> 
               </indirizziAbilitati> 
               <pubblicaAmministrazione>false</pubblicaAmministrazione> 
               <ruolo>altroprofessionista</ruolo> 
               <stato>attivo</stato>

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
Versione 1 del 18/03/2022 
 
               <tipologia> 
                  <id>D99F6E8181AE7D17E050A8C02E306A78</id> 
                  <descrizione>Agronomi</descrizione> 
                  <tipo>ENTE</tipo> 
               </tipologia> 
               <visibile>true</visibile> 
            </ruoliente> 
            <soggetto> 
               <codFisc>DPMDML80A01A944W</codFisc> 
               <cognome>DIPIMOLA</cognome> 
               <idSoggetto>4028b0c57f6daac5017f6e17902b0038</idSoggetto> 
               <nome>DIPIMOLA</nome> 
               <pec>dipimola2@pec.esempio.it</pec> 
            </soggetto> 
         </return> 
      </ns2:ricercaSoggettoCompleteResponse> 
   </env:Body> 
</env:Envelope>