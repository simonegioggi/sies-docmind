---
uniqueName: regindeclient
displayName: "RegindeClient"
category: "GENERAL"
tags: []
---

# RegindeClient

> **File originale:** `MEV/SCHEDA_021/RegindeClient.docx`  
> **Tipo:** DOCX

---

# ReGIndE_CLIENT
PROBLEMA:
si segnala che nell'ambiente di test è stata modificata la struttura del XML; nel tipo "ruoloente" è stato aggiunto l'attributo "tipologia". La url che chiamiamo è: https://89.119.251.203/ServiziInterrogazioneRegindeExt/ServiziInterrogazioneInterni
Se si modifica il client aggiungendo l'attributo, la chiamata a ReGIndE torna a funzionare, il problema è quale versione utilizzare, con o senza l'attributo "tipologia"?
SOLUZIONE:
http://161.27.213.72:8080/reginde/jsp/index.jsp
Inserire nel campo Nome, per esempio, “RES%” ed avviare la ricerca (ricercare eventuali errori nel file “server.log” reperibile seguendo il percorso “/home/SIES/jboss-eap-6.4.Alpha/standalone/log”.
Nel percorso “/home/SIES/jboss-eap-6.4.Alpha/standalone/configuration” si trova il file di configurazione “standalone-full.xml_ReGIndE” che serve per far funzionare il client che invoca il servizio di interrogazione utilizzando, come truststore, il file “trustore.jks” presente nel percorso “/var/SIES/CONFIG/certs/”:
<property name="javax.net.ssl.trustStore" value="/var/SIES/CONFIG/certs/trustore.jks"/>
<property name="javax.net.ssl.trustStorePassword" value="password"/>
Il nuovo wsdl è:
<definitions name='WsServiziInterrogazioneInterni' targetNamespace='http://www.giustizia.it/serviziTelematici/reginde/interrogazioniInt' xmlns='http://schemas.xmlsoap.org/wsdl/' xmlns:ns1='http://www.giustizia.it/serviziTelematici/reginde/interrogazioniExt' xmlns:soap='http://schemas.xmlsoap.org/wsdl/soap/' xmlns:tns='http://www.giustizia.it/serviziTelematici/reginde/interrogazioniInt' xmlns:xsd='http://www.w3.org/2001/XMLSchema'>
<types>
<xs:schema targetNamespace='http://www.giustizia.it/serviziTelematici/reginde/interrogazioniExt' version='1.0' xmlns:tns='http://www.giustizia.it/serviziTelematici/reginde/interrogazioniExt' xmlns:xs='http://www.w3.org/2001/XMLSchema'>
<xs:complexType name='ruoloente'>
<xs:sequence>
<xs:element minOccurs='0' name='codiceFiscale' type='xs:string'/>
<xs:element minOccurs='0' name='codice' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element name='pubblicaAmministrazione' type='xs:boolean'/>
<xs:element minOccurs='0' name='pec' type='xs:string'/>
<xs:element minOccurs='0' name='partitaIVA' type='xs:string'/>
<xs:element minOccurs='0' name='ruolo' type='xs:string'/>
<xs:element minOccurs='0' name='stato' type='xs:string'/>
<xs:element minOccurs='0' name='tipologia' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='soggetto'>
<xs:sequence>
<xs:element maxOccurs='unbounded' minOccurs='0' name='ruoliente' type='tns:ruoloente'/>
<xs:element maxOccurs='unbounded' minOccurs='0' name='indirizzi' type='tns:indirizzo'/>
<xs:element minOccurs='0' name='soggetto' type='tns:soggetti'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='indirizzo'>
<xs:sequence>
<xs:element minOccurs='0' name='cap' type='xs:string'/>
<xs:element minOccurs='0' name='comune' type='xs:string'/>
<xs:element minOccurs='0' name='email' type='xs:string'/>
<xs:element minOccurs='0' name='fax' type='xs:string'/>
<xs:element minOccurs='0' name='indirizzo' type='xs:string'/>
<xs:element minOccurs='0' name='prov' type='xs:string'/>
<xs:element minOccurs='0' name='telefono' type='xs:string'/>
<xs:element minOccurs='0' name='tp_indirizzo' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='soggetti'>
<xs:sequence>
<xs:element minOccurs='0' name='codFisc' type='xs:string'/>
<xs:element minOccurs='0' name='cognome' type='xs:string'/>
<xs:element minOccurs='0' name='dataNascita' type='xs:dateTime'/>
<xs:element minOccurs='0' name='luogoNascita' type='xs:string'/>
<xs:element minOccurs='0' name='nome' type='xs:string'/>
<xs:element minOccurs='0' name='pec' type='xs:string'/>
<xs:element minOccurs='0' name='provNascita' type='xs:string'/>
</xs:sequence>
</xs:complexType>
</xs:schema>
<xs:schema targetNamespace='http://www.giustizia.it/serviziTelematici/reginde/interrogazioniInt' version='1.0' xmlns:ns1='http://www.giustizia.it/serviziTelematici/reginde/interrogazioniExt' xmlns:tns='http://www.giustizia.it/serviziTelematici/reginde/interrogazioniInt' xmlns:xs='http://www.w3.org/2001/XMLSchema'>
<xs:import namespace='http://www.giustizia.it/serviziTelematici/reginde/interrogazioniExt'/>
<xs:element name='SearchLimitException' type='tns:SearchLimitException'/>
<xs:element name='ricercaEnteComplete' type='tns:ricercaEnteComplete'/>
<xs:element name='ricercaEnteCompleteResponse' type='tns:ricercaEnteCompleteResponse'/>
<xs:element name='ricercaSoggettoComplete' type='tns:ricercaSoggettoComplete'/>
<xs:element name='ricercaSoggettoCompleteResponse' type='tns:ricercaSoggettoCompleteResponse'/>
<xs:complexType name='ricercaEnteComplete'>
<xs:sequence>
<xs:element minOccurs='0' name='tipo' type='xs:string'/>
<xs:element minOccurs='0' name='descrizione' type='xs:string'/>
<xs:element minOccurs='0' name='codiceEnte' type='xs:string'/>
<xs:element minOccurs='0' name='codiceFiscale' type='xs:string'/>
<xs:element minOccurs='0' name='indirizzoPec' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='ricercaEnteCompleteResponse'>
<xs:sequence>
<xs:element maxOccurs='unbounded' minOccurs='0' name='return' type='ns1:ruoloente'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='SearchLimitException'>
<xs:sequence>
<xs:element minOccurs='0' name='message' type='xs:string'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='ricercaSoggettoComplete'>
<xs:sequence>
<xs:element minOccurs='0' name='cognome' type='xs:string'/>
<xs:element minOccurs='0' name='nome' type='xs:string'/>
<xs:element minOccurs='0' name='codiceFiscale' type='xs:string'/>
<xs:element minOccurs='0' name='indirizzo' type='xs:string'/>
<xs:element minOccurs='0' name='codiceEnte' type='xs:string'/>
<xs:element minOccurs='0' name='orderBy' type='xs:string'/>
<xs:element minOccurs='0' name='asc' type='xs:boolean'/>
</xs:sequence>
</xs:complexType>
<xs:complexType name='ricercaSoggettoCompleteResponse'>
<xs:sequence>
<xs:element maxOccurs='unbounded' minOccurs='0' name='return' type='ns1:soggetto'/>
</xs:sequence>
</xs:complexType>
</xs:schema>
</types>
<message name='SearchLimitException'>
<part element='tns:SearchLimitException' name='SearchLimitException'></part>
</message>
<message name='WsServiziInterrogazioneInterni_ricercaEnteComplete'>
<part element='tns:ricercaEnteComplete' name='ricercaEnteComplete'></part>
</message>
<message name='WsServiziInterrogazioneInterni_ricercaSoggettoCompleteResponse'>
<part element='tns:ricercaSoggettoCompleteResponse' name='ricercaSoggettoCompleteResponse'></part>
</message>
<message name='WsServiziInterrogazioneInterni_ricercaSoggettoComplete'>
<part element='tns:ricercaSoggettoComplete' name='ricercaSoggettoComplete'></part>
</message>
<message name='WsServiziInterrogazioneInterni_ricercaEnteCompleteResponse'>
<part element='tns:ricercaEnteCompleteResponse' name='ricercaEnteCompleteResponse'></part>
</message>
<portType name='WsServiziInterrogazioneInterni'>
<operation name='ricercaEnteComplete' parameterOrder='ricercaEnteComplete'>
<input message='tns:WsServiziInterrogazioneInterni_ricercaEnteComplete'></input>
<output message='tns:WsServiziInterrogazioneInterni_ricercaEnteCompleteResponse'></output>
<fault message='tns:SearchLimitException' name='SearchLimitException'></fault>
</operation>
<operation name='ricercaSoggettoComplete' parameterOrder='ricercaSoggettoComplete'>
<input message='tns:WsServiziInterrogazioneInterni_ricercaSoggettoComplete'></input>
<output message='tns:WsServiziInterrogazioneInterni_ricercaSoggettoCompleteResponse'></output>
<fault message='tns:SearchLimitException' name='SearchLimitException'></fault>
</operation>
</portType>
<binding name='WsServiziInterrogazioneInterniBinding' type='tns:WsServiziInterrogazioneInterni'>
<soap:binding style='document' transport='http://schemas.xmlsoap.org/soap/http'/>
<operation name='ricercaEnteComplete'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
<fault name='SearchLimitException'>
<soap:fault name='SearchLimitException' use='literal'/>
</fault>
</operation>
<operation name='ricercaSoggettoComplete'>
<soap:operation soapAction=''/>
<input>
<soap:body use='literal'/>
</input>
<output>
<soap:body use='literal'/>
</output>
<fault name='SearchLimitException'>
<soap:fault name='SearchLimitException' use='literal'/>
</fault>
</operation>
</binding>
<service name='WsServiziInterrogazioneInterni'>
<port binding='tns:WsServiziInterrogazioneInterniBinding' name='ServiziInterrogazioneInterniBeanPort'>
<soap:address location='https://89.119.251.203/ServiziInterrogazioneRegindeExt/ServiziInterrogazioneInterni'/>
</port>
</service>
</definitions>
L’applicazione “RegInde.war” è deployata nel percorso “/home/SIES/jboss-eap-6.4.Alpha/standalone/deployments”.

Il comando per estrarre il wsdl dal web è:
“wget https://89.119.251.203/ServiziInterrogazioneRegindeExt/ServiziInterrogazioneInterni?wsdl --no-check-certificate”.

Se si modifica il client aggiungendo l'attributo, la chiamata a ReGIndE torna a funzionare?
SI dopo la modifica funziona!

Il problema è quale versione utilizzare, con o senza l'attributo "tipologia"?
Io utilizzerei la versione aggiornata!