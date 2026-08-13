---
uniqueName: tutorialwspagopa
displayName: "Tutorial WS PagoPA"
category: "GENERAL"
tags: []
---

# Tutorial_WS_PagoPA

> **File originale:** `MEV/SCHEDA_013/Docs/Test/Tutorial_WS_PagoPA.docx`  
> **Tipo:** DOCX

---

# Web Service PagoPA
Dalla URL dove è esposto il web service:
https://servizibe.processotelematicocoll.giustizia.it/servizi/ServiziInvioPagamentiTelematici?wsdl
abbiamo (con Firefox per esempio) estratto il file “processotelematico-giustizia-it.pem”.
Poi abbiamo inserito tale certificato all’interno del sies.jks (TRUSTSTORE); posizionandosi  nel percorso della JDK del server:
/usr/java/jdk1.8.0_45/jre/bin dove andremo a copiare il file *.pem di cui sopra ed il sies.jks;
e lanciare la seguente istruzione:
keytool -import -alias pagopa -keystore sies.jks -file processotelematico-giustizia-it.pem
poi cancellare il file *.pem e spostare il file sies.jks nel percorso predefinito:
/var/SIES/CONFIG2/certs, sostituendo il precedente.
Dal sies.jks abbiamo poi estratto il certificato pagopa.cer.
Come seconda operazione abbiamo inserito il pagopa.cer nel file cacerts della JDK tramite il comando unix:
keytool -import -alias pagopa -keystore "/usr/java/jdk1.8.0_45/jre/lib/security/cacerts" -file pagopa.cer
La password da inserire è changeit e la risposta alla domanda sulla sicurezza del certificato è SI/YES.
Dal file serversies.jks (KEYSTORE) abbiamo estratto il file 1.cer che abbiamo inviato al servizio PST.
Quindi, abbiamo inviato a PST la nostra chiave pubblica (KEYSTORE) e contemporaneamente abbiamo dovuto dire al nostro TRUSTSTORE che chi ci rispondeva era una fonte attendibile.

<definitions name='ServiziInvioPagamentiTelematiciBeanService' targetNamespace='http://www.giustizia.it/serviziTelematici/serviziGenerici' xmlns='http://schemas.xmlsoap.org/wsdl/' xmlns:ns1='http://www.giustizia.it/serviziTelematici/pstbe/gestione' xmlns:soap='http://schemas.xmlsoap.org/wsdl/soap/' xmlns:tns='http://www.giustizia.it/serviziTelematici/serviziGenerici' xmlns:xsd='http://www.w3.org/2001/XMLSchema'>
<types>
<xs:schema targetNamespace='http://www.giustizia.it/serviziTelematici/pstbe/gestione' version='1.0' xmlns:ns1='http://www.giustizia.it/serviziTelematici/serviziGenerici' xmlns:tns='http://www.giustizia.it/serviziTelematici/pstbe/gestione' xmlns:xs='http://www.w3.org/2001/XMLSchema'>
<xs:import namespace='http://www.giustizia.it/serviziTelematici/serviziGenerici'/>
<xs:complexType name='datiRiscossione'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='codCausale' type='xs:string'/>
<xs:element minOccurs='0' name='descCausale' type='xs:string'/>
<xs:element minOccurs='0' name='codiceUtilizzatore' type='xs:string'/>
<xs:element minOccurs='0' name='codiceGeneratore' type='xs:string'/>
<xs:element minOccurs='0' name='codiceVersamento' type='xs:string'/>
<xs:element minOccurs='0' name='tassonomia' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType abstract='true' name='anagrafica'>
<xs:sequence/>
</xs:complexType>
<xs:complexType name='cdo'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='codice' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element minOccurs='0' name='numeroAlbo' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='parteCausa'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element name='abilitato' type='xs:boolean'/>
<xs:element minOccurs='0' name='codiceFiscale' type='xs:string'/>
<xs:element minOccurs='0' name='cognome' type='xs:string'/>
<xs:element minOccurs='0' name='dataCreazione' type='xs:dateTime'/>
<xs:element minOccurs='0' name='nome' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='definizioneServizio'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='codice' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element minOccurs='0' name='note' type='xs:string'/>
<xs:element minOccurs='0' name='visibile' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='definizioneTemplate'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='pspCode' type='xs:string'/>
<xs:element minOccurs='0' name='templateContent' type='xs:string'/>
<xs:element minOccurs='0' name='templateName' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='pda'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='certificatoHash' type='xs:string'/>
<xs:element minOccurs='0' name='certificatoSSL' type='xs:base64Binary'/>
<xs:element minOccurs='0' name='codPagTel' type='xs:string'/>
<xs:element minOccurs='0' name='codiceAlbo' type='xs:string'/>
<xs:element minOccurs='0' name='dataAutorizzazione' type='xs:dateTime'/>
<xs:element minOccurs='0' name='dataCessazione' type='xs:dateTime'/>
<xs:element minOccurs='0' name='descEstesa' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element minOccurs='0' name='flagPdaPagTel' type='xs:string'/>
<xs:element minOccurs='0' name='fornitori' type='tns:fornitori'/>
<xs:element minOccurs='0' name='legaleRappresentante' type='xs:string'/>
<xs:element minOccurs='0' name='linkManOp' type='xs:string'/>
<xs:element minOccurs='0' name='nomeCertificatoSSL' type='xs:string'/>
<xs:element minOccurs='0' name='note' type='xs:base64Binary'/>
<xs:element minOccurs='0' name='sedeLegale' type='xs:string'/>
<xs:element minOccurs='0' name='tipologia' type='tns:tipologiaPda'/>
<xs:element minOccurs='0' name='url' type='xs:string'/>
<xs:element minOccurs='0' name='urlWebService' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='fornitori'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='tipologiaPda'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='uffici'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='certificatoCifra' type='xs:base64Binary'/>
<xs:element minOccurs='0' name='certificatoMimetype' type='xs:string'/>
<xs:element minOccurs='0' name='codiceGL' type='xs:string'/>
<xs:element name='codiceRegione' type='xs:int'/>
<xs:element minOccurs='0' name='codiceUfficioMaster' type='xs:string'/>
<xs:element minOccurs='0' name='comune' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element minOccurs='0' name='indirizzoPec' type='xs:string'/>
<xs:element minOccurs='0' name='nomeCertificatoCifra' type='xs:string'/>
<xs:element minOccurs='0' name='provincia' type='xs:string'/>
<xs:element minOccurs='0' name='tipoUfficio' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='servizi'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='dataAttivazione' type='xs:dateTime'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element minOccurs='0' name='note' type='xs:string'/>
<xs:element maxOccurs='unbounded' minOccurs='0' name='registri' type='ns1:registro'/>
<xs:element maxOccurs='unbounded' minOccurs='0' name='serviziAtti' nillable='true' type='tns:serviziAtti'/>
<xs:element minOccurs='0' name='tipoServizio' type='tns:definizioneServizio'/>
<xs:element minOccurs='0' name='url' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='serviziAtti'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='dataDecreto' type='xs:dateTime'/>
<xs:element minOccurs='0' name='decreto' type='xs:base64Binary'/>
<xs:element minOccurs='0' name='fase' type='xs:string'/>
<xs:element minOccurs='0' name='grado' type='xs:string'/>
<xs:element minOccurs='0' name='mimetype' type='xs:string'/>
<xs:element minOccurs='0' name='nomeDecreto' type='xs:string'/>
<xs:element minOccurs='0' name='note' type='xs:string'/>
<xs:element minOccurs='0' name='rito' type='xs:string'/>
<xs:element minOccurs='0' name='servizio' type='xs:string'/>
<xs:element minOccurs='0' name='qName' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='ufficiGiudiziari'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='certificatoCifra' type='xs:base64Binary'/>
<xs:element minOccurs='0' name='certificatoMimetype' type='xs:string'/>
<xs:element minOccurs='0' name='codiceUfficioMaster' type='xs:string'/>
<xs:element minOccurs='0' name='comune' type='xs:string'/>
<xs:element minOccurs='0' name='descMaster' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element minOccurs='0' name='gestoreLocale' type='tns:gestoreLocale'/>
<xs:element minOccurs='0' name='indirizzoPec' type='xs:string'/>
<xs:element minOccurs='0' name='nomeCertificatoCifra' type='xs:string'/>
<xs:element minOccurs='0' name='provincia' type='xs:string'/>
<xs:element minOccurs='0' name='regione' type='tns:regioni'/>
<xs:element maxOccurs='unbounded' minOccurs='0' name='servizi' nillable='true' type='tns:servizi'/>
<xs:element minOccurs='0' name='tipoUfficio' type='tns:tipiUfficio'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='gestoreLocale'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='certificatoSSL' type='xs:base64Binary'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element minOccurs='0' name='distretto' type='tns:distretti'/>
<xs:element minOccurs='0' name='url' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='distretti'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='codiceGestoreLocale' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='regioni'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='tipiUfficio'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element minOccurs='0' name='gruppo' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='ufficiPenale'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element maxOccurs='unbounded' minOccurs='0' name='attiDepositabiliUfficio' nillable='true' type='tns:attiDepositabiliUfficio'/>
<xs:element minOccurs='0' name='certificatoCifra' type='xs:base64Binary'/>
<xs:element minOccurs='0' name='citta' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element minOccurs='0' name='gestoreLocale' type='tns:gestoreLocale'/>
<xs:element minOccurs='0' name='indirizzoPec' type='xs:string'/>
<xs:element minOccurs='0' name='nomeCertificatoCifra' type='xs:string'/>
<xs:element minOccurs='0' name='provincia' type='xs:string'/>
<xs:element minOccurs='0' name='regione' type='tns:regioni'/>
<xs:element minOccurs='0' name='tipiAttoDepositabile' type='tns:tipiAttoDepositabile'/>
<xs:element minOccurs='0' name='tipoUfficio' type='tns:tipiUfficio'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='attiDepositabiliUfficio'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='codiceUfficio' type='xs:string'/>
<xs:element minOccurs='0' name='dtAttivazione' type='xs:dateTime'/>
<xs:element minOccurs='0' name='nomeFile' type='xs:string'/>
<xs:element minOccurs='0' name='normativa' type='xs:base64Binary'/>
<xs:element minOccurs='0' name='note' type='xs:string'/>
<xs:element minOccurs='0' name='tipoAttoDep' type='tns:tipiAttoDepositabile'/>
<xs:element minOccurs='0' name='ufficioInterno' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='tipiAttoDepositabile'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='enti'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='codice' type='xs:string'/>
<xs:element minOccurs='0' name='codiceFiscale' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element maxOccurs='unbounded' minOccurs='0' name='indirizzi' nillable='true' type='tns:indirizziAbilitati'/>
<xs:element minOccurs='0' name='partitaIva' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='indirizziAbilitati'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='codiceFiscaleFirma' type='xs:string'/>
<xs:element minOccurs='0' name='pec' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='download'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='dataAvviso' type='xs:dateTime'/>
<xs:element minOccurs='0' name='dataDownload' type='xs:dateTime'/>
<xs:element minOccurs='0' name='destinazione' type='xs:string'/>
<xs:element minOccurs='0' name='sito' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='rito'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element minOccurs='0' name='registro' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='lookupUfficio'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='codiceFiscale' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element minOccurs='0' name='gestoreLocale' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='contenutoRichiestaRtag'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element name='annullamento' type='xs:int'/>
<xs:element minOccurs='0' name='dataRegistrazione' type='xs:dateTime'/>
<xs:element minOccurs='0' name='dataRegistrazioneConstraint' type='ns1:dateConstraint'/>
<xs:element minOccurs='0' name='destinazione' type='xs:string'/>
<xs:element minOccurs='0' name='erroreServer' type='xs:string'/>
<xs:element minOccurs='0' name='hostInvio' type='xs:string'/>
<xs:element minOccurs='0' name='hostRicezione' type='xs:string'/>
<xs:element minOccurs='0' name='idMessaggio' type='xs:string'/>
<xs:element name='progressivo' type='xs:int'/>
<xs:element minOccurs='0' name='richiesta' type='tns:richiestaRtag'/>
<xs:element minOccurs='0' name='sorgente' type='xs:string'/>
<xs:element minOccurs='0' name='tipologia' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='richiestaRtag'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='idRepertorio' type='xs:string'/>
<xs:element minOccurs='0' name='idUnivoco' type='xs:string'/>
<xs:element minOccurs='0' name='ufficio' type='tns:lookupUfficio'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='lookupRepertorio'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='altriSoggetti'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='codice' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element minOccurs='0' name='pecAddr' type='xs:string'/>
<xs:element minOccurs='0' name='tipologia' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='causalePagamentoConf'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='canalePagamento' type='xs:string'/>
<xs:element minOccurs='0' name='cfBeneficiario' type='xs:string'/>
<xs:element minOccurs='0' name='codiceCausale' type='xs:string'/>
<xs:element minOccurs='0' name='descBeneficiario' type='xs:string'/>
<xs:element minOccurs='0' name='descCCP' type='xs:string'/>
<xs:element minOccurs='0' name='ibanAccredito' type='xs:string'/>
<xs:element minOccurs='0' name='ibanAppoggio' type='xs:string'/>
<xs:element minOccurs='0' name='metodoPagamento' type='xs:string'/>
<xs:element minOccurs='0' name='numeroCCP' type='xs:string'/>
<xs:element minOccurs='0' name='tipoBeneficiario' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='causalePagamentoNEPConf'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='canalePagamento' type='xs:string'/>
<xs:element minOccurs='0' name='cfBeneficiario' type='xs:string'/>
<xs:element minOccurs='0' name='codiceCausale' type='xs:string'/>
<xs:element minOccurs='0' name='descBeneficiario' type='xs:string'/>
<xs:element minOccurs='0' name='descCCP' type='xs:string'/>
<xs:element minOccurs='0' name='ibanAccredito' type='xs:string'/>
<xs:element minOccurs='0' name='ibanAppoggio' type='xs:string'/>
<xs:element minOccurs='0' name='importo' type='xs:float'/>
<xs:element minOccurs='0' name='metodoPagamento' type='xs:string'/>
<xs:element minOccurs='0' name='numeroCCP' type='xs:string'/>
<xs:element minOccurs='0' name='tipoBeneficiario' type='xs:string'/>
<xs:element minOccurs='0' name='tipologia' type='xs:string'/>
<xs:element minOccurs='0' name='ufficioNEP' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='applicazioni'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='certificatoHash' type='xs:string'/>
<xs:element minOccurs='0' name='certificatoSSL' type='xs:base64Binary'/>
<xs:element minOccurs='0' name='codPagTel' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element minOccurs='0' name='url' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
<xs:complexType name='ufficioInterno'>
<xs:complexContent>
<xs:extension base='tns:anagrafica'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element minOccurs='0' name='tipoUfficio' type='xs:string'/>
</xs:sequence>
</xs:extension>
</xs:complexContent>
</xs:complexType>
</xs:schema>
<xs:schema targetNamespace='http://www.giustizia.it/serviziTelematici/serviziGenerici' version='1.0' xmlns:ns1='http://www.giustizia.it/serviziTelematici/pstbe/gestione' xmlns:tns='http://www.giustizia.it/serviziTelematici/serviziGenerici' xmlns:xs='http://www.w3.org/2001/XMLSchema'>
<xs:import namespace='http://www.giustizia.it/serviziTelematici/pstbe/gestione'/>
<xs:element name='ServiziPagamentiException' type='tns:ServiziPagamentiException'/>
<xs:element name='downloadAvviso' type='tns:downloadAvviso'/>
<xs:element name='downloadAvvisoResponse' type='tns:downloadAvvisoResponse'/>
<xs:element name='eliminaRichiesta' type='tns:eliminaRichiesta'/>
<xs:element name='eliminaRichiestaResponse' type='tns:eliminaRichiestaResponse'/>
<xs:element name='generaAvviso' type='tns:generaAvviso'/>
<xs:element name='generaAvvisoResponse' type='tns:generaAvvisoResponse'/>
<xs:element name='generaRPT' type='tns:generaRPT'/>
<xs:element name='generaRPTResponse' type='tns:generaRPTResponse'/>
<xs:element name='inviaCarrelloRPT' type='tns:inviaCarrelloRPT'/>
<xs:element name='inviaCarrelloRPTResponse' type='tns:inviaCarrelloRPTResponse'/>
<xs:element name='inviaER' type='tns:inviaER'/>
<xs:element name='inviaERResponse' type='tns:inviaERResponse'/>
<xs:element name='listaConfNEP' type='tns:listaConfNEP'/>
<xs:element name='listaConfNEPResponse' type='tns:listaConfNEPResponse'/>
<xs:element name='listaDatiRiscossione' type='tns:listaDatiRiscossione'/>
<xs:element name='listaDatiRiscossioneResponse' type='tns:listaDatiRiscossioneResponse'/>
<xs:element name='registraRispostaWisp' type='tns:registraRispostaWisp'/>
<xs:element name='registraRispostaWispResponse' type='tns:registraRispostaWispResponse'/>
<xs:element name='richiediCopiaRT' type='tns:richiediCopiaRT'/>
<xs:element name='richiediCopiaRTResponse' type='tns:richiediCopiaRTResponse'/>
<xs:element name='verificaRichiesta' type='tns:verificaRichiesta'/>
<xs:element name='verificaRichiestaResponse' type='tns:verificaRichiestaResponse'/>
<xs:complexType name='listaDatiRiscossione'>
<xs:sequence>
<xs:element minOccurs='0' name='idtipologia' type='xs:string'/>
<xs:element minOccurs='0' name='codice' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='listaDatiRiscossioneResponse'>
<xs:sequence>
<xs:element maxOccurs='unbounded' minOccurs='0' name='datiRiscossione' type='ns1:datiRiscossione'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='registro'>
<xs:sequence>
<xs:element minOccurs='0' name='codice' type='xs:string'/>
<xs:element minOccurs='0' name='codiceApplicazione' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='dateConstraint'>
<xs:sequence>
<xs:element minOccurs='0' name='lower' type='xs:dateTime'/>
<xs:element minOccurs='0' name='upper' type='xs:dateTime'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='verificaRichiesta'>
<xs:sequence>
<xs:element minOccurs='0' name='codiceCRS' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='verificaRichiestaResponse'>
<xs:sequence>
<xs:element maxOccurs='unbounded' minOccurs='0' name='return' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='ServiziPagamentiException'>
<xs:sequence>
<xs:element minOccurs='0' name='CRS' type='xs:string'/>
<xs:element minOccurs='0' name='message' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='eliminaRichiesta'>
<xs:sequence>
<xs:element minOccurs='0' name='codiceCRS' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='eliminaRichiestaResponse'>
<xs:sequence/>
</xs:complexType>
<xs:complexType name='generaRPT'>
<xs:sequence>
<xs:element minOccurs='0' name='richiestaPagamentoTelematico' type='tns:richiestaPagamentoTelematico'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='richiestaPagamentoTelematico'>
<xs:sequence>
<xs:element minOccurs='0' name='codiceDistretto' type='xs:string'/>
<xs:element minOccurs='0' name='codiceUfficio' type='xs:string'/>
<xs:element name='autenticazioneSoggetto' type='xs:string'/>
<xs:element name='soggettoPagatore' type='tns:anagraficaSoggetto'/>
<xs:element minOccurs='0' name='soggettoVersante' type='tns:anagraficaSoggetto'/>
<xs:element name='datiVersamento' type='tns:datiVersamento'/>
<xs:element minOccurs='0' name='dataScadenza' type='xs:dateTime'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='anagraficaSoggetto'>
<xs:sequence>
<xs:element minOccurs='0' name='naturaGiuridica' type='xs:string'/>
<xs:element name='codiceIdentificativoUnivoco' type='xs:string'/>
<xs:element name='nominativo' type='xs:string'/>
<xs:element minOccurs='0' name='indirizzo' type='xs:string'/>
<xs:element minOccurs='0' name='civico' type='xs:string'/>
<xs:element minOccurs='0' name='cap' type='xs:string'/>
<xs:element minOccurs='0' name='localita' type='xs:string'/>
<xs:element minOccurs='0' name='provincia' type='xs:string'/>
<xs:element minOccurs='0' name='regione' type='xs:string'/>
<xs:element minOccurs='0' name='nazione' type='xs:string'/>
<xs:element minOccurs='0' name='email' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='datiVersamento'>
<xs:sequence>
<xs:element name='importoTotale' type='xs:decimal'/>
<xs:element minOccurs='0' name='ibanAddebito' type='xs:string'/>
<xs:element minOccurs='0' name='bicAddebito' type='xs:string'/>
<xs:element maxOccurs='unbounded' name='datiSingoloVersamento' type='tns:datiSingoloVersamento'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='datiSingoloVersamento'>
<xs:sequence>
<xs:element name='importo' type='xs:decimal'/>
<xs:element minOccurs='0' name='causale' type='xs:string'/>
<xs:element name='datiSpecificiRiscossione' type='xs:string'/>
<xs:element minOccurs='0' name='datiMarcaBolloDigitale' type='tns:datiMarcaBolloDigitale'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='datiMarcaBolloDigitale'>
<xs:sequence>
<xs:element name='tipoBollo' type='xs:string'/>
<xs:element name='hashDocumento' type='xs:string'/>
<xs:element name='provinciaResidenza' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='generaRPTResponse'>
<xs:sequence>
<xs:element minOccurs='0' name='xmlRPT' type='xs:base64Binary'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='inviaCarrelloRPT'>
<xs:sequence>
<xs:element minOccurs='0' name='codiceFiscale' type='xs:string'/>
<xs:element maxOccurs='unbounded' minOccurs='0' name='crs' type='xs:string'/>
<xs:element name='areaPubblica' type='xs:boolean'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='inviaCarrelloRPTResponse'>
<xs:sequence>
<xs:element minOccurs='0' name='urlWISP' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='registraRispostaWisp'>
<xs:sequence>
<xs:element minOccurs='0' name='idSession' type='xs:string'/>
<xs:element minOccurs='0' name='esito' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='registraRispostaWispResponse'>
<xs:sequence>
<xs:element minOccurs='0' name='esitoRispostaWisp' type='tns:esitoRispostaWisp'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='esitoRispostaWisp'>
<xs:sequence>
<xs:element minOccurs='0' name='areaPubblica' type='xs:boolean'/>
<xs:element name='pagamentoBollo' type='xs:boolean'/>
<xs:element minOccurs='0' name='urlRedirect' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='listaConfNEP'>
<xs:sequence>
<xs:element minOccurs='0' name='codiceUfficioNEP' type='xs:string'/>
<xs:element minOccurs='0' name='tipologia' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='listaConfNEPResponse'>
<xs:sequence>
<xs:element maxOccurs='unbounded' minOccurs='0' name='causalePagamentoNEPConf' type='ns1:causalePagamentoNEPConf'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='richiediCopiaRT'>
<xs:sequence>
<xs:element minOccurs='0' name='codiceCRS' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='richiediCopiaRTResponse'>
<xs:sequence>
<xs:element maxOccurs='unbounded' minOccurs='0' name='return' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='inviaER'>
<xs:sequence>
<xs:element minOccurs='0' name='idRevoca' type='xs:string'/>
<xs:element minOccurs='0' name='dataRevoca' type='xs:dateTime'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='inviaERResponse'>
<xs:sequence>
<xs:element minOccurs='0' name='return' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='generaAvviso'>
<xs:sequence>
<xs:element minOccurs='0' name='richiestaPagamentoTelematico' type='tns:richiestaPagamentoTelematico'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='generaAvvisoResponse'>
<xs:sequence>
<xs:element minOccurs='0' name='return' type='tns:esitoGeneraAvviso'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='esitoGeneraAvviso'>
<xs:sequence>
<xs:element minOccurs='0' name='bollettino' type='xs:base64Binary'/>
<xs:element minOccurs='0' name='numeroAvviso' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='downloadAvviso'>
<xs:sequence>
<xs:element minOccurs='0' name='numeroAvviso' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='downloadAvvisoResponse'>
<xs:sequence>
<xs:element minOccurs='0' name='return' type='xs:base64Binary'/>
</xs:sequence>
</xs:complexType>
</xs:schema>
</types>
<message name='ServiziInvioPagamentiTelematici_downloadAvviso'>
<part element='tns:downloadAvviso' name='downloadAvviso'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_eliminaRichiesta'>
<part element='tns:eliminaRichiesta' name='eliminaRichiesta'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_registraRispostaWispResponse'>
<part element='tns:registraRispostaWispResponse' name='registraRispostaWispResponse'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_downloadAvvisoResponse'>
<part element='tns:downloadAvvisoResponse' name='downloadAvvisoResponse'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_generaAvviso'>
<part element='tns:generaAvviso' name='generaAvviso'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_verificaRichiesta'>
<part element='tns:verificaRichiesta' name='verificaRichiesta'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_richiediCopiaRT'>
<part element='tns:richiediCopiaRT' name='richiediCopiaRT'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_listaConfNEP'>
<part element='tns:listaConfNEP' name='listaConfNEP'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_generaRPT'>
<part element='tns:generaRPT' name='generaRPT'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_inviaCarrelloRPT'>
<part element='tns:inviaCarrelloRPT' name='inviaCarrelloRPT'></part>
</message>
<message name='ServiziPagamentiException'>
<part element='tns:ServiziPagamentiException' name='ServiziPagamentiException'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_richiediCopiaRTResponse'>
<part element='tns:richiediCopiaRTResponse' name='richiediCopiaRTResponse'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_registraRispostaWisp'>
<part element='tns:registraRispostaWisp' name='registraRispostaWisp'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_listaDatiRiscossione'>
<part element='tns:listaDatiRiscossione' name='listaDatiRiscossione'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_generaAvvisoResponse'>
<part element='tns:generaAvvisoResponse' name='generaAvvisoResponse'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_inviaER'>
<part element='tns:inviaER' name='inviaER'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_listaConfNEPResponse'>
<part element='tns:listaConfNEPResponse' name='listaConfNEPResponse'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_eliminaRichiestaResponse'>
<part element='tns:eliminaRichiestaResponse' name='eliminaRichiestaResponse'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_listaDatiRiscossioneResponse'>
<part element='tns:listaDatiRiscossioneResponse' name='listaDatiRiscossioneResponse'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_inviaCarrelloRPTResponse'>
<part element='tns:inviaCarrelloRPTResponse' name='inviaCarrelloRPTResponse'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_inviaERResponse'>
<part element='tns:inviaERResponse' name='inviaERResponse'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_verificaRichiestaResponse'>
<part element='tns:verificaRichiestaResponse' name='verificaRichiestaResponse'></part>
</message>
<message name='ServiziInvioPagamentiTelematici_generaRPTResponse'>
<part element='tns:generaRPTResponse' name='generaRPTResponse'></part>
</message>
<portType name='ServiziInvioPagamentiTelematici'>
<operation name='downloadAvviso' parameterOrder='downloadAvviso'>
<input message='tns:ServiziInvioPagamentiTelematici_downloadAvviso'></input>
<output message='tns:ServiziInvioPagamentiTelematici_downloadAvvisoResponse'></output>
<fault message='tns:ServiziPagamentiException' name='ServiziPagamentiException'></fault>
</operation>
<operation name='eliminaRichiesta' parameterOrder='eliminaRichiesta'>
<input message='tns:ServiziInvioPagamentiTelematici_eliminaRichiesta'></input>
<output message='tns:ServiziInvioPagamentiTelematici_eliminaRichiestaResponse'></output>
<fault message='tns:ServiziPagamentiException' name='ServiziPagamentiException'></fault>
</operation>
<operation name='generaAvviso' parameterOrder='generaAvviso'>
<input message='tns:ServiziInvioPagamentiTelematici_generaAvviso'></input>
<output message='tns:ServiziInvioPagamentiTelematici_generaAvvisoResponse'></output>
<fault message='tns:ServiziPagamentiException' name='ServiziPagamentiException'></fault>
</operation>
<operation name='generaRPT' parameterOrder='generaRPT'>
<input message='tns:ServiziInvioPagamentiTelematici_generaRPT'></input>
<output message='tns:ServiziInvioPagamentiTelematici_generaRPTResponse'></output>
<fault message='tns:ServiziPagamentiException' name='ServiziPagamentiException'></fault>
</operation>
<operation name='inviaCarrelloRPT' parameterOrder='inviaCarrelloRPT'>
<input message='tns:ServiziInvioPagamentiTelematici_inviaCarrelloRPT'></input>
<output message='tns:ServiziInvioPagamentiTelematici_inviaCarrelloRPTResponse'></output>
<fault message='tns:ServiziPagamentiException' name='ServiziPagamentiException'></fault>
</operation>
<operation name='inviaER' parameterOrder='inviaER'>
<input message='tns:ServiziInvioPagamentiTelematici_inviaER'></input>
<output message='tns:ServiziInvioPagamentiTelematici_inviaERResponse'></output>
<fault message='tns:ServiziPagamentiException' name='ServiziPagamentiException'></fault>
</operation>
<operation name='listaConfNEP' parameterOrder='listaConfNEP'>
<input message='tns:ServiziInvioPagamentiTelematici_listaConfNEP'></input>
<output message='tns:ServiziInvioPagamentiTelematici_listaConfNEPResponse'></output>
</operation>
<operation name='listaDatiRiscossione' parameterOrder='listaDatiRiscossione'>
<input message='tns:ServiziInvioPagamentiTelematici_listaDatiRiscossione'></input>
<output message='tns:ServiziInvioPagamentiTelematici_listaDatiRiscossioneResponse'></output>
</operation>
<operation name='registraRispostaWisp' parameterOrder='registraRispostaWisp'>
<input message='tns:ServiziInvioPagamentiTelematici_registraRispostaWisp'></input>
<output message='tns:ServiziInvioPagamentiTelematici_registraRispostaWispResponse'></output>
<fault message='tns:ServiziPagamentiException' name='ServiziPagamentiException'></fault>
</operation>
<operation name='richiediCopiaRT' parameterOrder='richiediCopiaRT'>
<input message='tns:ServiziInvioPagamentiTelematici_richiediCopiaRT'></input>
<output message='tns:ServiziInvioPagamentiTelematici_richiediCopiaRTResponse'></output>
<fault message='tns:ServiziPagamentiException' name='ServiziPagamentiException'></fault>
</operation>
<operation name='verificaRichiesta' parameterOrder='verificaRichiesta'>
<input message='tns:ServiziInvioPagamentiTelematici_verificaRichiesta'></input>
<output message='tns:ServiziInvioPagamentiTelematici_verificaRichiestaResponse'></output>
<fault message='tns:ServiziPagamentiException' name='ServiziPagamentiException'></fault>
</operation>
</portType>
<binding name='ServiziInvioPagamentiTelematiciBinding' type='tns:ServiziInvioPagamentiTelematici'>
<soap:binding style='document' transport='http://schemas.xmlsoap.org/soap/http'/>
<operation name='downloadAvviso'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
<fault name='ServiziPagamentiException'>
<soap:fault name='ServiziPagamentiException' use='literal'/>
</fault>
</operation>
<operation name='eliminaRichiesta'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
<fault name='ServiziPagamentiException'>
<soap:fault name='ServiziPagamentiException' use='literal'/>
</fault>
</operation>
<operation name='generaAvviso'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
<fault name='ServiziPagamentiException'>
<soap:fault name='ServiziPagamentiException' use='literal'/>
</fault>
</operation>
<operation name='generaRPT'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
<fault name='ServiziPagamentiException'>
<soap:fault name='ServiziPagamentiException' use='literal'/>
</fault>
</operation>
<operation name='inviaCarrelloRPT'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
<fault name='ServiziPagamentiException'>
<soap:fault name='ServiziPagamentiException' use='literal'/>
</fault>
</operation>
<operation name='inviaER'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
<fault name='ServiziPagamentiException'>
<soap:fault name='ServiziPagamentiException' use='literal'/>
</fault>
</operation>
<operation name='listaConfNEP'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
</operation>
<operation name='listaDatiRiscossione'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
</operation>
<operation name='registraRispostaWisp'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
<fault name='ServiziPagamentiException'>
<soap:fault name='ServiziPagamentiException' use='literal'/>
</fault>
</operation>
<operation name='richiediCopiaRT'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
<fault name='ServiziPagamentiException'>
<soap:fault name='ServiziPagamentiException' use='literal'/>
</fault>
</operation>
<operation name='verificaRichiesta'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
<fault name='ServiziPagamentiException'>
<soap:fault name='ServiziPagamentiException' use='literal'/>
</fault>
</operation>
</binding>
<service name='ServiziInvioPagamentiTelematiciBeanService'>
<port binding='tns:ServiziInvioPagamentiTelematiciBinding' name='ServiziInvioPagamentiTelematiciSOAPPort'>
<soap:address location='http://test-pst/servizi/ServiziInvioPagamentiTelematici'/>
</port>
</service>
</definitions>

<definitions name='ServiziConsultazionePagamentiTelematiciBeanService' targetNamespace='http://www.giustizia.it/serviziTelematici/serviziGenerici' xmlns='http://schemas.xmlsoap.org/wsdl/' xmlns:ns1='http://www.giustizia.it/serviziTelematici/Pagamenti' xmlns:soap='http://schemas.xmlsoap.org/wsdl/soap/' xmlns:tns='http://www.giustizia.it/serviziTelematici/serviziGenerici' xmlns:xsd='http://www.w3.org/2001/XMLSchema'>
<types>
<xs:schema targetNamespace='http://www.giustizia.it/serviziTelematici/Pagamenti' version='1.0' xmlns:ns1='http://www.giustizia.it/serviziTelematici/serviziGenerici' xmlns:xs='http://www.w3.org/2001/XMLSchema'>
<xs:import namespace='http://www.giustizia.it/serviziTelematici/serviziGenerici'/>
<xs:complexType name='dettaglioCRS'>
<xs:sequence>
<xs:element minOccurs='0' name='CRS' type='xs:string'/>
<xs:element minOccurs='0' name='dataCreazione' type='xs:dateTime'/>
<xs:element minOccurs='0' name='pagatore' type='xs:string'/>
<xs:element minOccurs='0' name='denominazionePagatore' type='xs:string'/>
<xs:element minOccurs='0' name='versante' type='xs:string'/>
<xs:element minOccurs='0' name='denominazioneVersante' type='xs:string'/>
<xs:element minOccurs='0' name='causale' type='xs:string'/>
<xs:element name='importo' type='xs:float'/>
<xs:element name='esitoPagamento' type='xs:int'/>
<xs:element minOccurs='0' name='tipoAllegato' type='xs:string'/>
<xs:element minOccurs='0' name='contenutoAllegato' type='xs:base64Binary'/>
<xs:element minOccurs='0' name='codiceSistemaRT' type='xs:string'/>
<xs:element minOccurs='0' name='contesto' type='ns1:datiContesto'/>
<xs:element minOccurs='0' name='idApa' type='xs:string'/>
</xs:sequence>
</xs:complexType>
</xs:schema>
<xs:schema targetNamespace='http://www.giustizia.it/serviziTelematici/serviziGenerici' version='1.0' xmlns:tns='http://www.giustizia.it/serviziTelematici/serviziGenerici' xmlns:xs='http://www.w3.org/2001/XMLSchema'>
<xs:element name='downloadRicevuta' type='tns:downloadRicevuta'/>
<xs:element name='downloadRicevutaResponse' type='tns:downloadRicevutaResponse'/>
<xs:element name='downloadRichiesta' type='tns:downloadRichiesta'/>
<xs:element name='downloadRichiestaResponse' type='tns:downloadRichiestaResponse'/>
<xs:element name='elencoPagamenti' type='tns:elencoPagamenti'/>
<xs:element name='elencoPagamentiResponse' type='tns:elencoPagamentiResponse'/>
<xs:element name='elencoPagamentiRevocati' type='tns:elencoPagamentiRevocati'/>
<xs:element name='elencoPagamentiRevocatiResponse' type='tns:elencoPagamentiRevocatiResponse'/>
<xs:element name='getAPAinKO' type='tns:getAPAinKO'/>
<xs:element name='getAPAinKOResponse' type='tns:getAPAinKOResponse'/>
<xs:element name='getPagamentiRevocati' type='tns:getPagamentiRevocati'/>
<xs:element name='getPagamentiRevocatiResponse' type='tns:getPagamentiRevocatiResponse'/>
<xs:element name='getPagamentoByCRS' type='tns:getPagamentoByCRS'/>
<xs:element name='getPagamentoByCRSResponse' type='tns:getPagamentoByCRSResponse'/>
<xs:element name='getPagamentoByDate' type='tns:getPagamentoByDate'/>
<xs:element name='getPagamentoByDateResponse' type='tns:getPagamentoByDateResponse'/>
<xs:element name='ricercaFlussiRendicontazioneScaricati' type='tns:ricercaFlussiRendicontazioneScaricati'/>
<xs:element name='ricercaFlussiRendicontazioneScaricatiResponse' type='tns:ricercaFlussiRendicontazioneScaricatiResponse'/>
<xs:element name='ricercaPagamentiNonVerificati' type='tns:ricercaPagamentiNonVerificati'/>
<xs:element name='ricercaPagamentiNonVerificatiResponse' type='tns:ricercaPagamentiNonVerificatiResponse'/>
<xs:complexType name='downloadRicevuta'>
<xs:sequence>
<xs:element minOccurs='0' name='codiceCRS' type='xs:string'/>
<xs:element name='originale' type='xs:boolean'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='downloadRicevutaResponse'>
<xs:sequence>
<xs:element minOccurs='0' name='content' type='xs:base64Binary'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='downloadRichiesta'>
<xs:sequence>
<xs:element minOccurs='0' name='codiceCRS' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='downloadRichiestaResponse'>
<xs:sequence>
<xs:element minOccurs='0' name='content' type='xs:base64Binary'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='elencoPagamenti'>
<xs:sequence>
<xs:element minOccurs='0' name='codiceCRS' type='xs:string'/>
<xs:element minOccurs='0' name='tipologia' type='xs:string'/>
<xs:element minOccurs='0' name='codiceFiscale' type='xs:string'/>
<xs:element minOccurs='0' name='codiceDistretto' type='xs:string'/>
<xs:element minOccurs='0' name='causale' type='xs:string'/>
<xs:element minOccurs='0' name='stato' type='xs:string'/>
<xs:element minOccurs='0' name='dataRichiestaDa' type='xs:dateTime'/>
<xs:element minOccurs='0' name='dataRichiestaA' type='xs:dateTime'/>
<xs:element name='dimensionePagina' type='xs:int'/>
<xs:element name='numeroPagina' type='xs:int'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='elencoPagamentiResponse'>
<xs:sequence>
<xs:element minOccurs='0' name='return' type='tns:risultatoRicerca'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='risultatoRicerca'>
<xs:sequence>
<xs:element name='count' type='xs:int'/>
<xs:element name='dimensionePagina' type='xs:int'/>
<xs:element maxOccurs='unbounded' minOccurs='0' name='items' type='xs:anyType'/>
<xs:element name='numeroPagina' type='xs:int'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='statoRichiestaPagamento'>
<xs:sequence>
<xs:element minOccurs='0' name='id' type='xs:string'/>
<xs:element minOccurs='0' name='codiceCRS' type='xs:string'/>
<xs:element minOccurs='0' name='codiceDistretto' type='xs:string'/>
<xs:element minOccurs='0' name='descrizioneDistretto' type='xs:string'/>
<xs:element minOccurs='0' name='pagatore' type='xs:string'/>
<xs:element minOccurs='0' name='denominazionePagatore' type='xs:string'/>
<xs:element minOccurs='0' name='versante' type='xs:string'/>
<xs:element minOccurs='0' name='denominazioneVersante' type='xs:string'/>
<xs:element minOccurs='0' name='dataRichiesta' type='xs:dateTime'/>
<xs:element minOccurs='0' name='dataRicevuta' type='xs:dateTime'/>
<xs:element minOccurs='0' name='stato' type='xs:string'/>
<xs:element name='importo' type='xs:float'/>
<xs:element minOccurs='0' name='causale' type='xs:string'/>
<xs:element minOccurs='0' name='statoNodoPA' type='xs:string'/>
<xs:element minOccurs='0' name='tipologia' type='xs:string'/>
<xs:element minOccurs='0' name='errore' type='xs:string'/>
<xs:element minOccurs='0' name='ruolo' type='xs:string'/>
<xs:element minOccurs='0' name='destinazione' type='xs:string'/>
<xs:element minOccurs='0' name='descrizioneTipologia' type='xs:string'/>
<xs:element minOccurs='0' name='numeroAvviso' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='datiContesto'>
<xs:sequence>
<xs:element name='codiceServizio' type='xs:string'/>
<xs:element name='datiServizio' type='xs:string'/>
<xs:element name='dominio' type='xs:string'/>
<xs:element name='gruppo' type='xs:string'/>
<xs:element minOccurs='0' name='stato' type='xs:string'/>
<xs:element minOccurs='0' name='dataModifica' type='xs:dateTime'/>
<xs:element minOccurs='0' name='dataInvalidazione' type='xs:dateTime'/>
<xs:element minOccurs='0' name='utilizzatore' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='revocaPagamento'>
<xs:sequence>
<xs:element minOccurs='0' name='codiceCRS' type='xs:string'/>
<xs:element minOccurs='0' name='dataRevoca' type='xs:dateTime'/>
<xs:element name='importoRTRevocata' type='xs:float'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='getPagamentoByCRS'>
<xs:sequence>
<xs:element minOccurs='0' name='codiceCRS' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='getPagamentoByCRSResponse'>
<xs:sequence>
<xs:element minOccurs='0' name='return' type='tns:statoRichiestaPagamento'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='getPagamentoByDate'>
<xs:sequence>
<xs:element minOccurs='0' name='dataRichiestaDa' type='xs:dateTime'/>
<xs:element minOccurs='0' name='dataRichiestaA' type='xs:dateTime'/>
<xs:element name='senzaRicevuta' type='xs:boolean'/>
<xs:element name='dimensionePagina' type='xs:int'/>
<xs:element name='numeroPagina' type='xs:int'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='getPagamentoByDateResponse'>
<xs:sequence>
<xs:element minOccurs='0' name='return' type='tns:risultatoRicercaPagamenti'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='risultatoRicercaPagamenti'>
<xs:sequence>
<xs:element name='count' type='xs:int'/>
<xs:element name='dimensionePagina' type='xs:int'/>
<xs:element maxOccurs='unbounded' minOccurs='0' name='items' type='tns:statoRichiestaPagamento'/>
<xs:element name='numeroPagina' type='xs:int'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='elencoPagamentiRevocati'>
<xs:sequence>
<xs:element minOccurs='0' name='dataRicevutaRevocataDa' type='xs:dateTime'/>
<xs:element minOccurs='0' name='dataRicevutaRevocataA' type='xs:dateTime'/>
<xs:element name='dimensionePagina' type='xs:int'/>
<xs:element name='numeroPagina' type='xs:int'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='elencoPagamentiRevocatiResponse'>
<xs:sequence>
<xs:element minOccurs='0' name='return' type='tns:risultatoRicerca'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='getPagamentiRevocati'>
<xs:sequence>
<xs:element minOccurs='0' name='dataRicevutaRevocataDa' type='xs:dateTime'/>
<xs:element minOccurs='0' name='dataRicevutaRevocataA' type='xs:dateTime'/>
<xs:element minOccurs='0' name='dataRevocataDa' type='xs:dateTime'/>
<xs:element minOccurs='0' name='dataRevocataA' type='xs:dateTime'/>
<xs:element name='dimensionePagina' type='xs:int'/>
<xs:element name='numeroPagina' type='xs:int'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='getPagamentiRevocatiResponse'>
<xs:sequence>
<xs:element minOccurs='0' name='return' type='tns:risultatoRicercaRevocati'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='risultatoRicercaRevocati'>
<xs:sequence>
<xs:element name='count' type='xs:int'/>
<xs:element name='dimensionePagina' type='xs:int'/>
<xs:element maxOccurs='unbounded' minOccurs='0' name='items' type='tns:pagamentoRevocato'/>
<xs:element name='numeroPagina' type='xs:int'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='pagamentoRevocato'>
<xs:sequence>
<xs:element minOccurs='0' name='data_er' type='xs:dateTime'/>
<xs:element minOccurs='0' name='data_revoca' type='xs:dateTime'/>
<xs:element minOccurs='0' name='esito_er' type='xs:string'/>
<xs:element minOccurs='0' name='esito_rr' type='xs:string'/>
<xs:element minOccurs='0' name='id_crs' type='xs:string'/>
<xs:element minOccurs='0' name='id_er' type='xs:string'/>
<xs:element minOccurs='0' name='id_revoca' type='xs:string'/>
<xs:element minOccurs='0' name='rt_revocata_data' type='xs:dateTime'/>
<xs:element name='rt_revocata_importo' type='xs:float'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='ricercaFlussiRendicontazioneScaricati'>
<xs:sequence>
<xs:element minOccurs='0' name='dataScaricoDa' type='xs:dateTime'/>
<xs:element minOccurs='0' name='dataScaricoA' type='xs:dateTime'/>
<xs:element name='crsErrore' type='xs:boolean'/>
<xs:element name='dimensionePagina' type='xs:int'/>
<xs:element name='numeroPagina' type='xs:int'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='ricercaFlussiRendicontazioneScaricatiResponse'>
<xs:sequence>
<xs:element minOccurs='0' name='return' type='tns:risultatoRicercaRendicontazione'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='risultatoRicercaRendicontazione'>
<xs:sequence>
<xs:element name='count' type='xs:int'/>
<xs:element name='dimensionePagina' type='xs:int'/>
<xs:element maxOccurs='unbounded' minOccurs='0' name='items' type='tns:flussoRendicontazione'/>
<xs:element name='numeroPagina' type='xs:int'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='flussoRendicontazione'>
<xs:sequence>
<xs:element minOccurs='0' name='idRendicontazione' type='xs:string'/>
<xs:element minOccurs='0' name='identificativoPsp' type='xs:string'/>
<xs:element minOccurs='0' name='idFlusso' type='xs:string'/>
<xs:element minOccurs='0' name='dataOraFlusso' type='xs:dateTime'/>
<xs:element name='avvenutoScarico' type='xs:boolean'/>
<xs:element minOccurs='0' name='dataScarico' type='xs:dateTime'/>
<xs:element name='avvenutoControllo' type='xs:boolean'/>
<xs:element minOccurs='0' name='dataControllo' type='xs:dateTime'/>
<xs:element minOccurs='0' name='rendicontazione' type='xs:base64Binary'/>
<xs:element minOccurs='0' name='iuRegolamento' type='xs:string'/>
<xs:element minOccurs='0' name='numTotalePagamenti' type='xs:string'/>
<xs:element name='importoTotale' type='xs:float'/>
<xs:element minOccurs='0' name='crsErrore' type='xs:base64Binary'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='ricercaPagamentiNonVerificati'>
<xs:sequence>
<xs:element minOccurs='0' name='dataControlloDa' type='xs:dateTime'/>
<xs:element minOccurs='0' name='dataControlloA' type='xs:dateTime'/>
<xs:element minOccurs='0' name='idFlusso' type='xs:string'/>
<xs:element minOccurs='0' name='dataRicevutaDa' type='xs:dateTime'/>
<xs:element minOccurs='0' name='dataRicevutaA' type='xs:dateTime'/>
<xs:element name='dimensionePagina' type='xs:int'/>
<xs:element name='numeroPagina' type='xs:int'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='ricercaPagamentiNonVerificatiResponse'>
<xs:sequence>
<xs:element minOccurs='0' name='return' type='tns:risultatoRicercaPagaNoVerify'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='risultatoRicercaPagaNoVerify'>
<xs:sequence>
<xs:element name='count' type='xs:int'/>
<xs:element name='dimensionePagina' type='xs:int'/>
<xs:element maxOccurs='unbounded' minOccurs='0' name='items' type='tns:pagamentoNonVerificato'/>
<xs:element name='numeroPagina' type='xs:int'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='pagamentoNonVerificato'>
<xs:sequence>
<xs:element minOccurs='0' name='crs' type='xs:string'/>
<xs:element minOccurs='0' name='identificativoUnivocoRiscossione' type='xs:string'/>
<xs:element name='importo' type='xs:float'/>
<xs:element minOccurs='0' name='indiceDatSingoloPagamento' type='xs:string'/>
<xs:element minOccurs='0' name='numeroAvviso' type='xs:string'/>
<xs:element minOccurs='0' name='tipologiaPagamento' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='getAPAinKO'>
<xs:sequence>
<xs:element minOccurs='0' name='dataRichiestaDa' type='xs:dateTime'/>
<xs:element minOccurs='0' name='dataRichiestaA' type='xs:dateTime'/>
<xs:element minOccurs='0' name='codiceDistretto' type='xs:string'/>
<xs:element minOccurs='0' name='codiceUfficio' type='xs:string'/>
<xs:element name='dimensionePagina' type='xs:int'/>
<xs:element name='numeroPagina' type='xs:int'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='getAPAinKOResponse'>
<xs:sequence>
<xs:element minOccurs='0' name='return' type='tns:risultatoRicercaPagamenti'/>
</xs:sequence>
</xs:complexType>
</xs:schema>
</types>
<message name='ServiziConsultazionePagamentiTelematici_downloadRicevuta'>
<part element='tns:downloadRicevuta' name='downloadRicevuta'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_getPagamentoByDateResponse'>
<part element='tns:getPagamentoByDateResponse' name='getPagamentoByDateResponse'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_getPagamentoByCRS'>
<part element='tns:getPagamentoByCRS' name='getPagamentoByCRS'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_downloadRicevutaResponse'>
<part element='tns:downloadRicevutaResponse' name='downloadRicevutaResponse'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_getAPAinKO'>
<part element='tns:getAPAinKO' name='getAPAinKO'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_elencoPagamentiResponse'>
<part element='tns:elencoPagamentiResponse' name='elencoPagamentiResponse'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_getPagamentoByCRSResponse'>
<part element='tns:getPagamentoByCRSResponse' name='getPagamentoByCRSResponse'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_getPagamentiRevocatiResponse'>
<part element='tns:getPagamentiRevocatiResponse' name='getPagamentiRevocatiResponse'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_getAPAinKOResponse'>
<part element='tns:getAPAinKOResponse' name='getAPAinKOResponse'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_getPagamentiRevocati'>
<part element='tns:getPagamentiRevocati' name='getPagamentiRevocati'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_ricercaPagamentiNonVerificatiResponse'>
<part element='tns:ricercaPagamentiNonVerificatiResponse' name='ricercaPagamentiNonVerificatiResponse'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_ricercaFlussiRendicontazioneScaricatiResponse'>
<part element='tns:ricercaFlussiRendicontazioneScaricatiResponse' name='ricercaFlussiRendicontazioneScaricatiResponse'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_ricercaFlussiRendicontazioneScaricati'>
<part element='tns:ricercaFlussiRendicontazioneScaricati' name='ricercaFlussiRendicontazioneScaricati'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_downloadRichiesta'>
<part element='tns:downloadRichiesta' name='downloadRichiesta'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_downloadRichiestaResponse'>
<part element='tns:downloadRichiestaResponse' name='downloadRichiestaResponse'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_getPagamentoByDate'>
<part element='tns:getPagamentoByDate' name='getPagamentoByDate'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_ricercaPagamentiNonVerificati'>
<part element='tns:ricercaPagamentiNonVerificati' name='ricercaPagamentiNonVerificati'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_elencoPagamenti'>
<part element='tns:elencoPagamenti' name='elencoPagamenti'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_elencoPagamentiRevocati'>
<part element='tns:elencoPagamentiRevocati' name='elencoPagamentiRevocati'></part>
</message>
<message name='ServiziConsultazionePagamentiTelematici_elencoPagamentiRevocatiResponse'>
<part element='tns:elencoPagamentiRevocatiResponse' name='elencoPagamentiRevocatiResponse'></part>
</message>
<portType name='ServiziConsultazionePagamentiTelematici'>
<operation name='downloadRicevuta' parameterOrder='downloadRicevuta'>
<input message='tns:ServiziConsultazionePagamentiTelematici_downloadRicevuta'></input>
<output message='tns:ServiziConsultazionePagamentiTelematici_downloadRicevutaResponse'></output>
</operation>
<operation name='downloadRichiesta' parameterOrder='downloadRichiesta'>
<input message='tns:ServiziConsultazionePagamentiTelematici_downloadRichiesta'></input>
<output message='tns:ServiziConsultazionePagamentiTelematici_downloadRichiestaResponse'></output>
</operation>
<operation name='elencoPagamenti' parameterOrder='elencoPagamenti'>
<input message='tns:ServiziConsultazionePagamentiTelematici_elencoPagamenti'></input>
<output message='tns:ServiziConsultazionePagamentiTelematici_elencoPagamentiResponse'></output>
</operation>
<operation name='elencoPagamentiRevocati' parameterOrder='elencoPagamentiRevocati'>
<input message='tns:ServiziConsultazionePagamentiTelematici_elencoPagamentiRevocati'></input>
<output message='tns:ServiziConsultazionePagamentiTelematici_elencoPagamentiRevocatiResponse'></output>
</operation>
<operation name='getAPAinKO' parameterOrder='getAPAinKO'>
<input message='tns:ServiziConsultazionePagamentiTelematici_getAPAinKO'></input>
<output message='tns:ServiziConsultazionePagamentiTelematici_getAPAinKOResponse'></output>
</operation>
<operation name='getPagamentiRevocati' parameterOrder='getPagamentiRevocati'>
<input message='tns:ServiziConsultazionePagamentiTelematici_getPagamentiRevocati'></input>
<output message='tns:ServiziConsultazionePagamentiTelematici_getPagamentiRevocatiResponse'></output>
</operation>
<operation name='getPagamentoByCRS' parameterOrder='getPagamentoByCRS'>
<input message='tns:ServiziConsultazionePagamentiTelematici_getPagamentoByCRS'></input>
<output message='tns:ServiziConsultazionePagamentiTelematici_getPagamentoByCRSResponse'></output>
</operation>
<operation name='getPagamentoByDate' parameterOrder='getPagamentoByDate'>
<input message='tns:ServiziConsultazionePagamentiTelematici_getPagamentoByDate'></input>
<output message='tns:ServiziConsultazionePagamentiTelematici_getPagamentoByDateResponse'></output>
</operation>
<operation name='ricercaFlussiRendicontazioneScaricati' parameterOrder='ricercaFlussiRendicontazioneScaricati'>
<input message='tns:ServiziConsultazionePagamentiTelematici_ricercaFlussiRendicontazioneScaricati'></input>
<output message='tns:ServiziConsultazionePagamentiTelematici_ricercaFlussiRendicontazioneScaricatiResponse'></output>
</operation>
<operation name='ricercaPagamentiNonVerificati' parameterOrder='ricercaPagamentiNonVerificati'>
<input message='tns:ServiziConsultazionePagamentiTelematici_ricercaPagamentiNonVerificati'></input>
<output message='tns:ServiziConsultazionePagamentiTelematici_ricercaPagamentiNonVerificatiResponse'></output>
</operation>
</portType>
<binding name='ServiziConsultazionePagamentiTelematiciBinding' type='tns:ServiziConsultazionePagamentiTelematici'>
<soap:binding style='document' transport='http://schemas.xmlsoap.org/soap/http'/>
<operation name='downloadRicevuta'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
</operation>
<operation name='downloadRichiesta'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
</operation>
<operation name='elencoPagamenti'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
</operation>
<operation name='elencoPagamentiRevocati'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
</operation>
<operation name='getAPAinKO'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
</operation>
<operation name='getPagamentiRevocati'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
</operation>
<operation name='getPagamentoByCRS'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
</operation>
<operation name='getPagamentoByDate'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
</operation>
<operation name='ricercaFlussiRendicontazioneScaricati'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
</operation>
<operation name='ricercaPagamentiNonVerificati'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
</operation>
</binding>
<service name='ServiziConsultazionePagamentiTelematiciBeanService'>
<port binding='tns:ServiziConsultazionePagamentiTelematiciBinding' name='ServiziConsultazionePagamentiTelematiciSOAPPort'>
<soap:address location='http://test-pst/servizi/ServiziConsultazionePagamentiTelematici'/>
</port>
</service>
</definitions>