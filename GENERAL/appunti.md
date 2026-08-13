---
uniqueName: appunti
displayName: "appunti"
category: "GENERAL"
tags: []
---

# appunti

> **File originale:** `MEV/SCHEDA_013/Docs/Test/appunti.docx`  
> **Tipo:** DOCX

---

<xs:complexType name='richiestaPagamentoTelematico'>
    <xs:sequence>
     <xs:element minOccurs='0' name='codiceDistretto' type='xs:string'/>
     <xs:element minOccurs='0' name='codiceUfficio' type='xs:string'/>
     <xs:element name='autenticazioneSoggetto' type='xs:string'/>OTH
     <xs:element name='soggettoPagatore' type='tns:anagraficaSoggetto'/>
     <xs:element minOccurs='0' name='soggettoVersante' type='tns:anagraficaSoggetto'/>
     <xs:element name='datiVersamento' type='tns:datiVersamento'/>
     <xs:element minOccurs='0' name='dataScadenza' type='xs:dateTime'/>in pago pa è obbligatoria. se non la specifichiamo in automatico viene considerata di 30 gg
    </xs:sequence>
   </xs:complexType>
   <xs:complexType name='anagraficaSoggetto'>
    <xs:sequence>
     <xs:element minOccurs='0' name='naturaGiuridica' type='xs:string'/>F/G
     <xs:element name='codiceIdentificativoUnivoco' type='xs:string'/>Codice Fiscale o PI
     <xs:element name='nominativo' type='xs:string'/>max 70 caratteri
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
     <xs:element minOccurs='0' name='causale' type='xs:string'/>massimo 100 caratteri e con il seguente formato “/<importo>/TXT/<descr causale>”. Es: “/139.0/TXT/Pagamenti in favore Amministrazione”
     <xs:element name='datiSpecificiRiscossione' type='xs:string'/>PENPE fisso
     <xs:element minOccurs='0' name='datiMarcaBolloDigitale' type='tns:datiMarcaBolloDigitale'/>
    </xs:sequence>

<tr><td>&nbsp;</td></tr>
<tr>
<td colspan="4" class="Titolo">########## INIZIO TEST x Genera Avviso PagoPA ##########</td>
</tr>
<tr>
<%-- MEV_2023-13: aggiunta etichetta --%>
<td class="l" colspan="4" style="text-align: center;">
<a href="<%=IWebConstants.PG_MAIN%>?<%=IWebConstants.ACTION_FIELD%>=siap.siep.pagoPA.action.ActLoadGeneraAvvisoPagoPA">WS Genera Avviso PagoPA</a>
</td>
</tr>
<tr>
<td colspan="4" class="Titolo">########## FINE TEST x Genera Avviso PagoPA ##########</td>
</tr>
<tr><td>&nbsp;</td></tr>
<tr>
<td colspan="4" class="Titolo">########## INIZIO TEST x Elenco Pagamenti PagoPA ##########</td>
</tr>
<tr>
<%-- MEV_2023-13: aggiunta etichetta --%>
<td class="l" colspan="4" style="text-align: center;">
<a href="<%=IWebConstants.PG_MAIN%>?<%=IWebConstants.ACTION_FIELD%>=siap.siep.pagoPA.action.ActInvocaWSGeneraAvvisoPagoPA">WS Elenco Pagamenti PagoPA</a>
</td>
</tr>
<tr>
<td colspan="4" class="Titolo">########## FINE TEST x Elenco Pagamenti PagoPA ##########</td>
</tr>