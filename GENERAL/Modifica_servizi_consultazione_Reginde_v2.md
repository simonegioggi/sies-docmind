---
uniqueName: modificaserviziconsultazioneregindev2
displayName: "Modifica servizi consultazione Reginde v2"
category: "GENERAL"
tags: []
---

# Modifica_servizi_consultazione_Reginde_v2

> **File originale:** `MEV/SCHEDA_021/Modifiche_ReGIndE/Modifica_servizi_consultazione_Reginde_v2.pdf`  
> **Tipo:** PDF

---

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
Versione 2 del 28/03/2022 
 
1 
 
STORIA DELLE REVISIONI 
 
Versione 
Data 
Motivazione 
1 
18/03/2022 
Prima emissione  
2 
28/03/2022 
Corretto metodo ricercaEnteComplete 
 
Modifica dei servizi di consultazione del Reginde  
 
Servizio interrogazione Soggetto  
 
Vengono modificate le logiche dei servizi esposti a terzi tramite il wsdl ServiziInterrogazioneSoggetto.wsdl, 
namespace “http://www.giustizia.it/serviziTelematici/reginde/interrogazioniExt”.  
In particolare i servizi che vengono modificati sono:  
 
dettagliSoggettoPerCodice  
 
dettagliSoggettoPerIndirizzo  
 
elencoPaginatoSoggetti  
 
isMembroDi  
 
ricercaSoggetto  
 
ricercaSoggettoEx  
In ciascun servizio viene aggiunto un controllo sullo stato dei ruoli che possiede il soggetto affinché saranno 
visualizzati solo i soggetti che possiedono almeno un ruolo con stato "attivo" e le sole informazioni inerenti 
ai ruoli in tale stato. 
Si precisa che sono stati modificati gli oggetti in output integrando nuove informazioni. Per maggiori 
informazioni consultare il wsdl allegato. 
Servizio Interrogazione Ente  
 
Vengono modificate tutte le logiche dei servizi presenti in ServiziInterrogazioneEnte.wsdl in quanto non 
saranno più restituiti gli enti e le PA cancellate. In particolare vengono modificati i servizi:  
 
dettagliEnte  
 
ricercaEnte  
 
ricercaEnteEx  
 
ricercaEnteInt  
 
ricercaEntiReferente  
 
ricercaIndAbilitati  
 
ricercaReferente  
Si precisa che viene modificato il nome del metodo “ricercaReferenti” con “ricercaReferente”.

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
Versione 2 del 28/03/2022 
 
2 
 
Si precisa che sono stati modificati gli oggetti in output integrando nuove informazioni. Per maggiori 
informazioni consultare il wsdl allegato. 
Viene introdotto un nuovo metodo “ricercaEnteComplete” per permettere la ricerca di un ente in base ai 
parametri in input:  
 
tipoEnte  
 
idTipologia  
 
piva  
 
descrizione  
 
codiceFiscale  
 
indirizzoPec  
 
codiceEnte  
 
classe  
 
Infine, viene eliminato il servizio “ricercaSportelli” presente in “ServiziInterrogazioneEnte”.  
 
Alcuni esempi di chiamata 
Di seguito alcuni esempi di chiamata e risposta con i nuovi wsdl 
 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" 
xmlns:int="http://www.giustizia.it/serviziTelematici/reginde/interrogazioniExt"> 
   <soapenv:Header/> 
   <soapenv:Body> 
      <int:ricercaSoggettoEx> 
         <codiceFiscale>DPMDML80A01A944W</codiceFiscale> 
         <indirizzo></indirizzo> 
      </int:ricercaSoggettoEx> 
   </soapenv:Body> 
</soapenv:Envelope> 
 
 
<env:Envelope xmlns:env="http://schemas.xmlsoap.org/soap/envelope/"> 
   <env:Header/> 
   <env:Body> 
      <ns2:ricercaSoggettoExResponse 
xmlns:ns2="http://www.giustizia.it/serviziTelematici/reginde/interrogazioniExt"> 
         <return> 
            <ruoliente> 
               <codiceFiscale>00794470377</codiceFiscale> 
               <codice>ENTEIMOLA1</codice>

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
Versione 2 del 28/03/2022 
 
3 
 
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

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
Versione 2 del 28/03/2022 
 
4 
 
            </soggetto> 
         </return> 
      </ns2:ricercaSoggettoExResponse> 
   </env:Body> 
</env:Envelope> 
 
 
 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" 
xmlns:int="http://www.giustizia.it/serviziTelematici/reginde/interrogazioniExt"> 
   <soapenv:Header/> 
   <soapenv:Body> 
      <int:ricercaEnteEx> 
         <tipo>ENTE</tipo> 
         <descrizione>ODA ASTI</descrizione> 
         <codiceFiscale>80010790055</codiceFiscale> 
      </int:ricercaEnteEx> 
   </soapenv:Body> 
</soapenv:Envelope> 
 
<env:Envelope xmlns:env="http://schemas.xmlsoap.org/soap/envelope/"> 
   <env:Header/> 
   <env:Body> 
      <ns2:ricercaEnteExResponse 
xmlns:ns2="http://www.giustizia.it/serviziTelematici/reginde/interrogazioniExt"> 
         <return> 
            <codiceFiscale>80010790055</codiceFiscale> 
            <codice>COA005005</codice> 
            <descrizione>ODA ASTI</descrizione> 
            <id>4028b0c07f72d42d017f735337060096</id> 
            <indirizziAbilitati> 
               <id>4028b0c07f72d42d017f73536c2e0097</id> 
               <email>avvocato2.avvocato2@pec.esempio.it</email> 
               <codiceFiscale>VVCVCT56A01A944F</codiceFiscale> 
            </indirizziAbilitati> 
            <pubblicaAmministrazione>false</pubblicaAmministrazione> 
            <partitaIVA>80010790055</partitaIVA> 
            <tipologia> 
               <id>D99F6E8181AC7D17E050A8C02E306A78</id> 
               <descrizione>ODA (ORDINE DEGLI AVVOCATI)</descrizione> 
               <tipo>ENTE</tipo> 
            </tipologia> 
            <visibile>true</visibile> 
         </return>

Ministero della Giustizia 
Dipartimento dell’Organizzazione Giudiziaria, del Personale e dei Servizi 
Direzione Generale per i Sistemi Informativi Automatizzati 
 
Versione 2 del 28/03/2022 
 
5 
 
      </ns2:ricercaEnteExResponse> 
   </env:Body> 
</env:Envelope>