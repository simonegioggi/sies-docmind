---
uniqueName: siut-sie-ar-21-20200407-descrizione-servizi-web
displayName: "SIUT SIE AR 2.1 20200407 Descrizione Servizi Web"
category: "GENERAL"
tags: []
---

﻿
| Ministero della GiustiziaDipartimento dell’Organizzazione Giudiziaria, del Personale e dei ServiziDirezione Generale per i Sistemi Informativi Automatizzati |
| --- |
|  |






Il presente documento è stato redatto con la collaborazione del RTI Engineering Ingegneria Informatica S.p.A. & Sirfin-PA S.r.l. nell’ambito del contratto CIG 73479643B7 per lo “Sviluppo del Sistema Informativo Unitario Telematico, la manutenzione degli attuali sistemi dell’area Penale del Ministero della Giustizia e servizi correlati. Lotto 1”.


Approvazioni

|  | Nominativo | Funzione |
| --- | --- | --- |
| Elaborato da | Simone Gioggi | Analista programmatore |
| Verificato da | Vito Bufi | Responsabile Manutenzione Sistemi attuali |
| Approvato da | Paolo Ceccanti | Responsabile Unico Fornitura |
| Data approvazione | 07/04/2020 |  |
| Livello di riservatezza | L3 |  |


Elenco versioni

| Versione | Data | Motivo | Modifica |
| --- | --- | --- | --- |
| 2.1 | 07/04/2020 | Integrazione Scheda N° 2019/020 | Integrazione delle modifiche per la realizzazione dell’intervento richiesto con la scheda Avvocatura Sede:2.1.3Definizione XSD:negli elementi DATI_PROCEDIMENTO_INPUT edUFFICIO_TYPE aggiunto il parametro di tipo “string” codUfficio.2.6.3Definizione XSD: nell’elemento DATI_SOGGETTO_INPUT aggiunto il parametro di tipo “string” codUfficioDistretto; nell’elemento DATI_PROCEDIMENTO_TYPE aggiunti i parametri di tipo “string” descrTipoUfficio, codUfficioDistretto e descrUfficioDistretto. |


Lista di distribuzione

| Nominativo | Organizzazione | Ufficio | Funzione |
| --- | --- | --- | --- |
| Ing. Giovanni Malesci | Amministrazione |  | Responsabile Unico Procedimento |
| Dr.ssa Annamaria Palmieri | Amministrazione |  | Direttore Esecutivo Contratto |
| Paolo Ceccanti | RTI |  | Responsabile Unico Fornitura |
| Pasquale Lamattina | RTI |  | Referente Tecnico |
| Vito Bufi | RTI |  | Responsabile Manutenzione Sistemi attuali |
| Fabio Mazzocchi | RTI |  | Responsabile Manutenzione Correttiva |
| Andrea Salvaggio | RTI |  | Responsabile Progetto Sistema Unitario |
| Antonio Iacobelli | RTI |  | Responsabile Supporto Specialistico |
| Antonella Damiani | RTI |  | Responsabile Centro di Competenza |
| Fabio Gattamorta | RTI |  | Responsabile PMO |
| Alessandro Falleni | RTI |  | Referente sicurezza |
| Edoardo Lamuraglia | RTI |  | Referente qualità |
| Francesco Rosati | RTI |  | Referente qualità |
| Andrea Castorino | RTI |  | Referente Applicativo Gestore Fascicolo Documentale |



INDICE DEI CONTENUTI
1.Introduzione6
1.1Scopo del documento6
1.2Riferimenti6
1.3Glossario6
1.3.1Definizioni6
1.3.2Acronimi e abbreviazioni6
2.DESCRIZIONE SERVIZI WEB8
2.1.Ricerca Procedimento Sius8
2.1.1.Definizione Namespace8
2.1.2.Definizione WSDL8
2.1.3.Definizione XSD10
2.1.4.Interfaccia Metodi Disponibili16
2.2.Dettaglio Ordinanza16
2.2.1.Definizione Namespace16
2.2.2.Definizione WSDL16
2.2.3.Definizione XSD18
2.2.4.Interfaccia Metodi Disponibili23
2.3.Dettaglio Decreto24
2.3.1.Definizione Namespace24
2.3.2.Definizione WSDL24
2.3.3.Definizione XSD25
2.4.Dettaglio Rinvio Udienza31
2.4.1.Definizione Namespace31
2.4.2.Definizione WSDL31
2.4.3.Definizione XSD32
2.4.4.Interfaccia Metodi Disponibili34
2.5.Ricerca Soggetti Con Procedimento34
2.5.1.Definizione Namespace34
2.5.2.Definizione WSDL34
2.5.3.Definizione XSD36
2.5.4.Interfaccia Metodi Disponibili36
2.6.Elenco Procedimenti Per Soggetto37
2.6.1.Definizione Namespace37
2.6.2.Definizione WSDL37
2.6.3.Definizione XSD38
2.6.4.Interfaccia Metodi Disponibili39
2.7.Ricerca Avvisi40
2.7.1.Definizione Namespace40
2.7.2.Definizione WSDL40
2.7.3.Definizione XSD41
2.7.4.Interfaccia Metodi Disponibili42
2.8.Richiesta Stampa Allegato43
2.8.1.Definizione Namespace43
2.8.2.Definizione WSDL43
2.8.3.Definizione XSD44
2.8.4.Interfaccia Metodi Disponibili45


Introduzione
## Scopo del documento

Lo scopo del presente documento è definire quali siano i servizi web messi a disposizione dal sistema SIES per permettere le seguenti consultazioni da parte del Sistema di Consultazione Procedimenti Avvisi SIUS:

Ricerca di un procedimento SIUS
Visualizzazione del dettaglio di un’ORDINANZA
Visualizzazione del dettaglio di un DECRETO
Visualizzazione del dettaglio di un RINVIO UDIENZA
Ricerca soggetti con procedimento SIUS
Visualizzazione elenco procedimenti per soggetto
Ricerca avvisi per avvocato
Richiesta di stampa dell’allegato SIUS
## Riferimenti


| Riferimento | Nome Documento | Descrizione Documento |
| --- | --- | --- |
|  | SIUT-SIE-SC-1.0-20191002_Scheda di intervento n.20_Avvocatura_SIES_Sede | Scheda intervento |
|  | SIUT-SIE-SI-1.3-20200317_Specifiche_Intervento_Avvocatura.pdf | Specifiche di intervento |

## Glossario

### Definizioni


| Definizione | Descrizione |
| --- | --- |
|  |  |
|  |  |

### Acronimi e abbreviazioni


| Sigla | Descrizione |
| --- | --- |
| AgID | Agenzia per l’Italia Digitale |
| API | Application Programming Interface |
| CPU | Central Processing Unit |
| CV | Curriculum Vitae |
| DB | Data Base |
| DEC | Direttore Esecutivo Contratto |
| DGSIA | Direzione Generale per i Sistemi Informativi Automatizzati |
| DR | Disaster Recovery |
| ETSI | EuropeanTelecommunications Standards Institute |
| FP | Function Point |
| GdL | Gruppo di Lavoro |
| GDPR | General Data ProtectionRegulation |
| HW | HardWare |
| ICT | Information & Communication Technology |
| ISO | International Organization for Standardization |
| ISP | Information Security Policy |
| IT | Information Technology |
| KPI | Key Performance Indicator |
| MAAC | MAndatory Access Control |
| MAC | MAnutenzione Correttiva |
| MEV | Manutenzione EVolutiva |
| OWASP | Open Web Application Security Project |
| PA | Pubblica Amministrazione |
| PEC | Posta Elettronica Certificata |
| PDCA | Plan, Do, Check, Act |
| PdQ | Piano della Qualità |
| PdP | Piano di Progetto |
| PdS | Piano della Sicurezza |
| PMO | Program Management Office |
| POO | Program Operating Office |
| QM | Quality Manager |
| RA | Risk Assessment |
| RID | Riservatezza, Integrità, Disponibilità |
| RM | Resource Manager |
| RPO | Recovery Point Objective |
| RTO | Recovery Time Objective |
| RTI | Raggruppamento Temporaneo di Impresa |
| RUF | Responsabile Unico Fornitore |
| RUP | Responsabile Unico Progetto |
| SAL | Stato Avanzamento Lavori |
| SGQ | Sistema di Gestione per la Qualità di Engineering Ingegneria Informatica S.p.A. |
| SGSI | Sistema di Gestione della Sicurezza Informatica |
| SIU | Sistema Informativo Unitario |
| SLA | Service Level Agreement |
| SM | Security Manager |
| SQL | Structured Query Language |
| SW | SoftWare |
| TT | Trouble Ticketing |
| UTA | Utente Generico Amministrazione |
| VPN | Virtual Private Network |
| SIUS | Sistema Informativo per l'Ufficio di Sorveglianza |
| XSD | XML Schema Definition |
| WSDL | Web Services Description Language |


DESCRIZIONE SERVIZI WEB
In riferimento all’intervento richiesto [RIF1.] ed all’integrazione di cui alla tabella “Elenco Versioni” del presente documento, si riporta brevemente la descrizione degli interventi apportati ai fini della gestione dell’informazione “Sede” del distretto.
L’aggiunta di questa informazione, la cui esigenza è nata per garantire l’univocità di un procedimento all’interno di un medesimo distretto, a parità di anno, numero e tipo ufficio, è intervenuta sulle seguenti strutture dati:

Alla struttura dati di input, DATI_PROCEDIMENTO_INPUT, elemento chiave per il servizio di dettaglio procedimento, ossia alla struttura in chiamata al servizio web di “Ricerca di un Procedimento SIUS”. In questa struttura è stato inserito il campo ‘codUfficio’ che mappa il codice della sede dell’ufficio di iscrizione del procedimento SIUS.
Alla struttura dati, UFFICIO_TYPE, elemento descrittivo per il servizio di dettaglio procedimento, ossia alla struttura in chiamata al servizio web di “Ricerca di un Procedimento SIUS”. In questa struttura è stato inserito il campo ‘codUfficio’ che mappa il codice della sede dell’ufficio di iscrizione del procedimento SIUS.
Alla struttura dati di input,DATI_SOGGETTO_INPUT, elemento contenitore dei dati di input per la ricerca dell'elenco dei procedimenti (ELENCO_PROCEDIMENTI), ossia alla struttura in chiamata al servizio web di “Elenco Procedimenti SIUS”. In questa struttura è stato inserito il campo ‘codUfficioDistretto’ che mappa il codice della sede dell’ufficio di iscrizione del procedimento SIUS ricercato.
Alla struttura dati di output, DATI_PROCEDIMENTO_TYPE, elemento contenitore dei dati di risposta alla ricerca dell’elenco dei procedimenti (ELENCO_PROCEDIMENTI_OUTPUT), utilizzata come struttura in risposta al servizio di “Elenco Procedimenti per Soggetto”. In questa struttura sono stati inseriti i campi ‘descrTipoUfficio’, ‘codUfficioDistretto’ e ‘descrUfficioDistretto’ che mappano la descrizione del tipo di ufficio, il codice e la descrizione della sede dell’ufficio di iscrizione del procedimento SIUS ricercato.
Ricerca Procedimento Sius
Il web service di ricerca procedimento, permette di effettuare la ricerca di un procedimento di sorveglianza sul sistema SIUS, dato in input gli estremi del procedimento (Anno, Numero, distretto, tipo ufficio e sede).
Definizione Namespace
targetNamespace= "http://it/eng/giustizia/avvocatura/ws/dettaglioProcedimento/"
Definizione WSDL
<wsdl:definitions
xmlns:apachesoap="http://xml.apache.org/xml-soap"
xmlns:intf="http://it/eng/giustizia/avvocatura/ws/dettaglioProcedimento/"
xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/"
xmlns:tns="http://it/eng/giustizia/avvocatura/ws/dettaglioProcedimento/"
xmlns:wsdl=http://schemas.xmlsoap.org/wsdl/
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
targetNamespace="http://it/eng/giustizia/avvocatura/ws/dettaglioProcedimento/">
<wsdl:types>
<schemaxmlns="http://www.w3.org/2001/XMLSchema"targetNamespace="http://it/eng/giustizia/avvocatura/ws/dettaglioProcedimento/">
<elementname="DettaglioProcedimento">
<complexType>
        <sequence>
<elementname="datiProcedimentoInput"type="xsd:string"/>
</sequence>
</complexType>
</element>
<elementname="DettaglioProcedimentoResponse">
<complexType>
<sequence>
<elementname="datiProcedimentoOutput"type="xsd:string"/>
</sequence>
      </complexType>
</element>
</schema>
</wsdl:types>
<wsdl:messagename="DettaglioProcedimentoRequest">
<wsdl:partelement="tns:DettaglioProcedimento"name="datiProcedimentoInput"/>
</wsdl:message>
<wsdl:messagename="DettaglioProcedimentoResponse">
<wsdl:partelement="tns:DettaglioProcedimentoResponse"name="datiProcedimentoOutput"/>
</wsdl:message>
<wsdl:portTypename="dettaglioProcedimento">
<wsdl:operationname="DettaglioProcedimento">
<wsdl:inputmessage="tns:DettaglioProcedimentoRequest"/>
<wsdl:outputmessage="tns:DettaglioProcedimentoResponse"/>
</wsdl:operation>
</wsdl:portType>
<wsdl:bindingname="dettaglioProcedimento"type="tns:dettaglioProcedimento">
<soap:bindingstyle="document" transport="http://schemas.xmlsoap.org/soap/http"/>
<wsdl:operationname="DettaglioProcedimento">
<soap:operationsoapAction="http://it/eng/giustizia/avvocatura/ws/dettaglioProcedimento/DettaglioProcedimento"/>
<wsdl:input>
<soap:bodyuse="literal"/>
</wsdl:input>
<wsdl:output>
<soap:bodyuse="literal"/>
</wsdl:output>
</wsdl:operation>
</wsdl:binding>
<wsdl:servicename="dettaglioProcedimento">
<wsdl:portbinding="tns:dettaglioProcedimento"name="dettaglioProcedimento">
<soap:addresslocation="http://localhost:8080/services/dettaglioProcedimento" />
</wsdl:port>
</wsdl:service>
</wsdl:definitions>
Definizione XSD

| Nome Elemento | Note | Tipo |
| --- | --- | --- |
| DATI_PROCEDIMENTO_INPUT |
| DATI_PROCEDIMENTO_INPUT | elemento root per il servizio di dettaglio procedimento | -- |
| annoProcedimento | anno del procedimento | integer |
| numeroProcedimento | numero del procedimento | integer |
| codiceFiscaleAvvocato | cf avvocato | string |
| codTipoUfficio | UDS: Ufficio di Sorveglianza TDS: Tribunale di Sorveglianza UDSM:Ufficio di Sorveglianza Minori TDSM:Tribunale di Sorveglianza Minori | string |
| codDistretto | distretto | string |
| codUfficio | codice ufficio | string |
| DATI_PROCEDIMENTO_OUTPUT |
| DATI_PROCEDIMENTO_OUTPUT | elemento contenitore dei dati complessivi del procedimento | -- |
| type:FASCICOLO_SIUS | elemento contenitore dei dati del fascicolo SIUS | -- |
| type:SOGGETTO | elemento contenitore dei dati del Soggetto | -- |
| type:ATTO | elemento contenitore dei dati dell'atto | -- |
| type:FASCICOLO_SIEP | elemento contenitore dei dati del fascicolo SIEP | -- |
| oggetto | è la sezione OGGETTO | type:TENORE_TYPE |
| oggettiStralciati | Fa riferimento alla lista dei tenori stralciati | type:TENORE_TYPE |
| elencoRiferimentiFascicoliSIEP | Elemento contenitore degli alti Titoli Esecutivi | type:RIFERIMENTO_FASC_SIEP_TYPE |
| listaAvvocati | elenco dei difensori | type:AVVOCATO_TYPE |
| elencoMovimentiUdienza | elenco dei movimenti udienza | type:MOVIMENTI_UDIENZA_TYPE |
| elencoProvvedimenti | Sezione Provvedimenti | type:EVENTO_TYPE |
| elencoAtti | Contiene la sezione Altri Atti | type:EVENTO_TYPE |
| elencoRichiesteIstruttorie | elenco delle richieste istruttorie | type:NOTIFICA_TYPE |
| ALLEGATO_RTF | allegato della stampa rtf di SIUS | base64Binary |
| type:ERRORE | elemento contenitore di errori | -- |
| UFFICIO |
| UFFICIO | -- | UFFICIO |
| FASCICOLO_SIEP |
| FASCICOLO_SIEP | Contiene dati per la stampa della sezione Titolo Esecutivo | -- |
| chiaveProgrSIEP | numero del fascicolo SIEP | integer |
| chiaveAnnoSIEP | anno del fascicolo SIEP | integer |
| flagCumulante | flag cumulante | string |
| descrTipoUfficio | Tipo Ufficio che ha iscritto il titolo esecutivo | -- |
| descrComuneUfficio | comune dell'ufficio | string |
| dataIscrizione | data di iscrizione del fascicolo SIEP | type:DATA_TYPE |
| type:SENTENZA | dati della sentenza | -- |
| descrPosizioneGiuridica | descrizione della posizione giuridica | string |
| PENA_RESIDUA | dati della pena residua | type:PENA_TYPE |
| PENA_COMPLESSIVA | dati della pena complessiva | type:PENA_TYPE |
| SOGGETTO |
| SOGGETTO | -- | SOGGETTO |
| SENTENZA |
| SENTENZA | -- | SENTENZA |
| UDIENZA |
| UDIENZA | -- | -- |
| dataUdienza | data dell'udienza | type:DATA_TYPE |
| dataCameraConsiglio | data camera di consiglio | type:DATA_TYPE |
| flagRinviata | flag udienza rinviata | string |
| descrPresidente | presidente udienza | string |
| TENORE |
| TENORE | L'elemento Tenore viene usato per gli OGGETTI STRALCIATI | TENORE |
| FASCICOLO_SIUS |
| FASCICOLO_SIUS | -- | FASCICOLO_SIUS |
| MAGISTRATO |
| MAGISTRATO | -- | -- |
| mCognome | cognome del magistrato | -- |
| mNome | nome del magistrato | -- |
| ERRORE |
| ERRORE | -- | -- |
| CODICE_ERRORE | codice dell'errore | string |
| DESCR_ERRORE | descrizione dell'errore | string |
| RICERCA_PROCEDIMENTO |
| RICERCA_PROCEDIMENTO | -- | -- |
| type:DATI_PROCEDIMENTO_INPUT | -- | -- |
| type:DATI_PROCEDIMENTO_OUTPUT | -- | -- |
| MOVIMENTI_UDIENZA |
| MOVIMENTI_UDIENZA | -- | MOVIMENTI_UDIENZA |
| ATTO |
| ATTO | -- | -- |
| dataRichiesta | data di richiesta dell'atto | type:DATA_TYPE |
| descrTipoAtto | descrizione del tipo di 'atto | string |
| dataArrivoCancelleria | data di arrivo in cancelleria | type:DATA_TYPE |
| descrTipoMittenteAtto | descrizione del tipo mittente | string |
| descrSedeMittente | descrizione sede mittente | string |
| descrMittente | descrizione del mittente | string |
| FASCICOLO_SIUS_TYPE |
| FASCICOLO_SIUS_TYPE | -- | -- |
| idFascicoloSius | identificativo del fascicolo SIUS | integer |
| chiaveAnno | è l'anno del procedimento | integer |
| chiaveProg | è il numero del procedimento | integer |
| dataIscrizione | data di iscrizione del fascicolo SIUS | type:DATA_TYPE |
| descrPosizioneMateriale | descrizione della posizione materiale | string |
| descrStatoFascicolo | descrizione dello stato del fascicolo | string |
| fascicoloUnificante | anno/numero del fascicolo unificante | string |
| dataDefinizione | data di definizione del fascicolo SIUS | type:DATA_TYPE |
| descrDefinizione | descrizione della definizione | string |
| tipoDefinizione | tipo di definizione | string |
| codTipoRegistro | codice del tipo registro | string |
| descrTipoRegistro | descrizione del tipo registro | string |
| annoS1 | anno del fascicolo unificato | string |
| progrS1 | numero del fascicolo unificato | string |
| elencoFascicoliUnificati | sarà una concatenazione di stringhe così formate: anno/numero;anno/numero | string |
| elencoFascicoliCollegati | sarà una concatenazione di stringhe così formate: anno/numero tipoUfficio e DescrizioneUfficio;anno/numero tipoUfficio e DescrizioneUfficio | string |
| fascicoloPadre | sarà una concatenazione di stringhe così formate: anno/numero tipoUfficio e DescrizioneUfficio;anno/numero tipoUfficio e DescrizioneUfficio | string |
| type:UDIENZA | dati dell'udienza | -- |
| contenuto | è la sezione contenuto | string |
| type:MAGISTRATO | dati del magistrato | -- |
| descrCancelleriaAssegnataria | cancelleria assegnataria | string |
| annotazioniProcedimento | annotazioni del procedimento | string |
| listaNote | elenco di note del fascicolo | type:NOTE_TYPE |
| ulterioriIstanze | descrizione di ulteriori istanze | boolean |
| TENORE_TYPE |
| TENORE_TYPE | -- | -- |
| descrOggettoTenore | descrizione oggetto | -- |
| note | note | string |
| RESIDENZA_TYPE |
| RESIDENZA_TYPE | -- | -- |
| codTipoResidenza | codiTipoResidenza=R (residenza) else domicilio | string |
| codStato | codice stato di residenza | string |
| descrStato | descrizione stato di residenza | string |
| codProvincia | codice della provincia di residenza | string |
| descrComune | descrizione del comune di residenza | string |
| indirizzo | indirizzo di residenza | string |
| descComuneEstero | comune estero di residenza | string |
| PENA_TYPE |
| PENA_TYPE | -- | -- |
| dataInizioPena | data inizio della pena | type:DATA_TYPE |
| dataFinePena | data fine della pena | type:DATA_TYPE |
| sanzSostResidua | sanzione sostitutiva residua | string |
| flagErgastolo | S=ERGASTOLO D=ISOLAMENTO DIURNO | string |
| numAnniIsolamentoDiurno | numero anni di isolamento diurno | integer |
| numMesiIsolamentoDiurno | numero mesi di isolamento diurno | integer |
| numGiorniIsolamentoDiurno | numero giorni di isolamento diurno | integer |
| numAnniReclusione | numero anni di reclusione | integer |
| numMesiReclusione | numero mesi di reclusione | integer |
| numGiorniReclusione | numero giorni di reclusione | integer |
| importoMulta | importo della multa | decimal |
| numAnniArresto | numero anni di arresto | integer |
| numMesiArresto | numero mesi di reclusione | integer |
| numGiorniArresto | numero giorni di reclusione | integer |
| importoAmmenda | importo dell'ammenda | decimal |
| codTipoPenaDetentiva | tipo di pena detentiva | string |
| descrTipoPenaDetentiva | descrizione del tipo di pena detentiva | string |
| SENTENZA_TYPE |
| SENTENZA_TYPE | -- | -- |
| idSentenza | identificativo della sentenza | integer |
| numeroSentenza | numero della sentenza | string |
| annoSentenza | anno della sentenza | integer |
| dataProvvedimento | data del provvedimento | type:DATA_TYPE |
| descrTipoAutoritaEmittente | autorita emittente | string |
| AVVOCATO_TYPE |
| AVVOCATO_TYPE | -- | -- |
| cognome | cognome dell'avvocato | string |
| nome | nome dell'avvocato | string |
| descrTipo | descrizione del tipo di avvocato | string |
| codiceFiscale | codice fiscale dell'avvocato | string |
| NOTE_TYPE |
| NOTE_TYPE | -- | -- |
| data | data | type:DATA_TYPE |
| descrizione | descrizione | string |
| IMPUGNAZIONE_TYPE |
| IMPUGNAZIONE_TYPE | -- | -- |
| descrTipoImpugnazione | descrizione del tipo di impugnazione | string |
| dataRicorso | data del ricorso | type:DATA_TYPE |
| flagTipo | I=impugnazione O=opposizione | string |
| EVENTO_TYPE |
| EVENTO_TYPE | -- | -- |
| idEvento | identificativo evento | integer |
| dataEmissione | data di emissione del provvedimento | type:DATA_TYPE |
| descrTipoProvvedimento | descrizione del tipo provvedimento | string |
| descrMotivo | descrizione del motivo del provvedimento | string |
| descrEsito | descrizione esito del provvedimento | string |
| dataDeposito | data di deposito del provvedimento | type:DATA_TYPE |
| altreInformazioni | altre informazioni inerenti al provvedimento | string |
| codTipoProvvedimento | codice del tipo provvedimento | string |
| eventoIdEventoRevoca | identificativo del evento di revoca | string |
| elencoImpugnazioniOpposizioni | elenco delle impugnazioni ed opposizioni | type:IMPUGNAZIONE_TYPE |
| flagDocumentoRegistrato | A=ANNULLATO S=VALIDATO | string |
| flagDepositoValidato | flag che individua se deposito provvedimento è validato | string |
| RIFERIMENTO_FASC_SIEP_TYPE |
| RIFERIMENTO_FASC_SIEP_TYPE | -- | -- |
| idRiferimentoFascicoloSiep | identificativo del riferimento al fascicolo siep | integer |
| flagMS | flag misure sicurezza | string |
| annoFascicoloSiep | anno del fascicolo SIEP | integer |
| progrFascicoloSiep | numero del fascicolo SIEP | string |
| descrUffFascicoloSiep | ufficio del fascicolo SIEP | string |
| dataProvvedimento | data del provvedimento | type:DATA_TYPE |
| descrTipoProvvedimento | descrizione del tipo provvedimento | string |
| descrTipoAutoritaEmittente | descrizione del tipo autorità emittente | string |
| descrLuogoEmittente | luogo emittente | string |
| dataIrrevocabilita | data di irrevocabilita | type:DATA_TYPE |
| annoProvvedimento | anno del provvedimento | integer |
| numeroProvvedimento | numero del provvedimento | string |
| NOTIFICA_TYPE |
| NOTIFICA_TYPE | Modella l'oggetto NotificaModel di SIES | -- |
| mDescrizione | descrizione della notifica | string |
| mDestinatario | Destinatario può essere: un oggetto UFFICIO AUTORITA_ESTERNA AVVOCATO_SIEP AVVOCATO_SIUS UEPE(vedi CSSAModel di SIUS) | -- |
| mDataInvio | data invio notifica | type:DATA_TYPE |
| mDataAvvenutaNotifica | data di avvenuta notifica | type:DATA_TYPE |
| UFFICIO_TYPE |
| UFFICIO_TYPE | -- | -- |
| codTipoUfficio | UDS: Ufficio di Sorveglianza TDS: Tribunale di Sorveglianza UDSM:Ufficio di Sorveglianza Minori TDSM:Tribunale di Sorveglianza Minori | string |
| descrTipoUfficio | descrizione del tipo ufficio | string |
| descrComune | descrizione del comune dell'ufficio | string |
| codDistretto | distretto di appartenenza dell'ufficio | string |
| codUfficio | codice dell'ufficio | string |
| AUTORITA_ESTERNA_TYPE |
| AUTORITA_ESTERNA_TYPE | -- | -- |
| mDescrTipoAutorita | descrizione del tipo autorità | string |
| mDescrSede | descrizione sede autorità | string |
| SOGGETTO_TYPE |
| SOGGETTO_TYPE | -- | -- |
| cognome | cognome soggetto | string |
| nome | nome soggetto | string |
| sesso | sesso del soggetto | string |
| dataNascita | data di nascita del soggetto | type:DATA_TYPE |
| descrComuneNascita | comune di nascita del soggetto | string |
| descrStatoNascita | stato di nascita del soggetto | string |
| codProvinciaNascita | provincia di nascita del soggetto | string |
| idSoggetto | identificativo del soggetto | integer |
| listaResidenze | elenco delle residenze del soggetto | type:RESIDENZA_TYPE |
| paternita | paternità del soggetto | string |
| codCs | è il codice CUI | string |
| cognomeMadre | cognome madre del soggetto | string |
| numeroFascicoli | numero di fascicoli del soggetto | integer |
| descrPosGiuridica | posizione giuridica del soggetto | string |
| dataFinePena | data fine pena | type:DATA_TYPE |
| luogoDetenzione | luogo di detenzione | string |
| codComuneNascita | codice del comune di nascita del soggetto | string |
| codStatoNascita | codice dello stato di nascita del soggetto | string |
| DATA_TYPE |
| DATA_TYPE | -- | -- |
| giorno | giorno della data | int |
| mese | mese della data | int |
| anno | anno della data | int |
| MOVIMENTI_UDIENZA_TYPE |
| MOVIMENTI_UDIENZA_TYPE | -- | -- |
| dataUdienza | data dell'udienza | type:DATA_TYPE |
| tipoOperazione | tipo di movimento udienza | string |
| dataInserimento | data inserimento del movimento udienza | type:DATA_TYPE |
| dataModifica | data modifica udienza | type:DATA_TYPE |

Interfaccia Metodi Disponibili

| OPERAZIONE | dettaglioProcedimento |
| --- | --- |
| Descrizione | Ricerca il dettaglio di un procedimento di sorveglianza |
| Parametri | DATI_PROCEDIMENTO_INPUT(per il dettaglio del type consultare la struttura xsd) |
| Risultato | DATI_PROCEDIMENTO_OUTPUT(per il dettaglio del type consultare la struttura xsd) |

Dettaglio Ordinanza
Il web service di dettaglio ordinanza, ricerca i dati di dettaglio di un ‘evento’ di tipo ordinanza, dato in input l’identificato dell’evento.
Definizione Namespace
targetNamespace= "http://it/eng/giustizia/avvocatura/ws/type/dettaglioOrdinanza"
Definizione WSDL
<?xmlversion="1.0"encoding="UTF-8"standalone="no"?>
<wsdl:definitionsxmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/"
xmlns:tns="http://it/eng/giustizia/avvocatura/ws/dettaglioOrdinanza/"
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/"xmlns:xsd="http://www.w3.org/2001/XMLSchema"
name="dettaglioOrdinanza"targetNamespace="http://it/eng/giustizia/avvocatura/ws/dettaglioOrdinanza/">
<wsdl:types>
<xsd:schema>
<xsd:import
namespace="http://it/eng/giustizia/avvocatura/ws/type/dettaglioOrdinanza"
schemaLocation="dettaglio_ordinanza.xsd"/>
</xsd:schema>
<xsd:schema
targetNamespace="http://it/eng/giustizia/avvocatura/ws/dettaglioOrdinanza/">
<xsd:elementname="DettaglioOrdinanza">
<xsd:complexType>
<xsd:sequence>
<xsd:elementname="datiOrdinanzaInput"type="xsd:string"/>
</xsd:sequence>
</xsd:complexType>
</xsd:element>
<xsd:elementname="DettaglioOrdinanzaResponse">
<xsd:complexType>
<xsd:sequence>
<xsd:elementname="datiOrdinanzaOutput"type="xsd:string"/>
</xsd:sequence>
</xsd:complexType>
</xsd:element>
</xsd:schema>
</wsdl:types>
<wsdl:messagename="DettaglioOrdinanzaResponse">
<wsdl:partelement="tns:DettaglioOrdinanzaResponse"name="parameters">
</wsdl:part>
</wsdl:message>
<wsdl:messagename="DettaglioOrdinanzaRequest">
<wsdl:partelement="tns:DettaglioOrdinanza"name="parameters">
</wsdl:part>
</wsdl:message>
<wsdl:portTypename="dettaglioOrdinanza">
<wsdl:operationname="DettaglioOrdinanza">
<wsdl:inputmessage="tns:DettaglioOrdinanzaRequest">
</wsdl:input>
<wsdl:outputmessage="tns:DettaglioOrdinanzaResponse">
</wsdl:output>
</wsdl:operation>
</wsdl:portType>
<wsdl:bindingname="dettaglioOrdinanza"type="tns:dettaglioOrdinanza">
<soap:bindingstyle="document"
transport="http://schemas.xmlsoap.org/soap/http"/>
<wsdl:operationname="DettaglioOrdinanza">
<soap:operationsoapAction="http://it/eng/giustizia/avvocatura/ws/dettaglioOrdinanza/DettaglioOrdinanza"/>
<wsdl:input>
<soap:bodyuse="literal"/>
</wsdl:input>
<wsdl:output>
<soap:bodyuse="literal"/>
</wsdl:output>
</wsdl:operation>
</wsdl:binding>
<wsdl:servicename="dettaglioOrdinanza">
<wsdl:portbinding="tns:dettaglioOrdinanza"name="dettaglioOrdinanza">
<soap:addresslocation="http://localhost:8080/services/dettaglioOrdinanza"/>
</wsdl:port>
</wsdl:service>
</wsdl:definitions>
Definizione XSD

| Nome Elemento | Note | Tipo |
| --- | --- | --- |
| DETTAGLIO_ORDINANZA |
| DETTAGLIO_ORDINANZA | Elemento root del servizio di dettaglio ordinanza | -- |
| type:DATI_INPUT_DETTAGLIO | Elemento contenitore dei dati di chiamata al servizio di dettaglio ordinanza | -- |
| type:OUTPUT_DETTAGLIO_ORDINANZA | Elemento contenitore dei dati di risposta al servizio di dettaglio ordinanza | -- |
| ERRORE |
| ERRORE | -- | -- |
| CODICE_ERRORE | codice errore | string |
| DESCR_ERRORE | descrizione errore | string |
| DATI_INPUT_DETTAGLIO |
| DATI_INPUT_DETTAGLIO | -- | -- |
| idEvento | identificativo dell'evento | string |
| codiTipoProvvedimento | tipo di provvedimento | string |
| tipoUfficio | tipo ufficio | string |
| type:DATI_AVVISO | elemento contenitore di identificazione di un avviso | -- |
| DATI_RIEPILOGO_PROCEDIMENTO |
| DATI_RIEPILOGO_PROCEDIMENTO | -- | -- |
| annoProcedimentoSIUS | anno del procedimento SIUS | integer |
| numeroProcedimentoSIUS | numero del procedimento SIUS | integer |
| oggettoProcedimentoSIUS | oggetto del procedimento SIUS | string |
| annoFascicoloSIEP | anno del fascicolo SIEP | integer |
| numeroFascicoloSIEP | numero del fascicolo SIEP | integer |
| ufficioFascicoloSIEP | ufficio del fascicolo SIEP | string |
| dataFascicoloSIEP | data del fascicolo SIEP | type:DATA_TYPE |
| nomeSoggetto | nome del soggetto | string |
| cognomeSoggetto | cognome del soggetto | string |
| dataNascita | data nascita del soggetto | type:DATA_TYPE |
| luogoNascita | luogo di nascita del soggetto | string |
| codiceProvincia | provincia di nascita del soggetto | string |
| dataUdienza | data udienza | type:DATA_TYPE |
| nomeMagistratoRelatore | nome del magistrato | string |
| cognomeMagistratoRelatore | cognome del magistrato | string |
| etaPresuntaAnni | età presunta del soggetto (numero anni) | integer |
| etaPresuntaMesi | età presunta del soggetto (numero mesi) | integer |
| sesso | sesso del soggetto | string |
| flagRinviata | flag rinviata | string |
| descrStatoFascicolo | descrizione dello stato del fascicolo | string |
| codiceStatoFascicolo | codice dello stato del fascicolo | string |
| DATI_ORDINANZA |
| DATI_ORDINANZA | -- | -- |
| tipoOrdinanza | tipo ordinanza | string |
| dataEmissione | data emissione | type:DATA_TYPE |
| annoOrdinanza | anno ordinanza | integer |
| numeroOrdinanza | numero ordinanza | integer |
| dataDepositoCancelleria | data deposito in cancelleria | type:DATA_TYPE |
| statoProvvedimento | stato del provvedimento | string |
| descrDecisione | decisione | string |
| totaleGiorniLibertaAnticipata | giorni liberta anticipata | integer |
| totaleGiorniRiduzionePena | giorni riduzione pena | integer |
| sommaRisarcimento | importo del risarcimento | decimal |
| ufficioSorveglianzaCompetente | ufficio sorveglianza competente | string |
| ufficioConcessioneRiduzione | ufficio concessione riduzione | string |
| dispositivo | è il valore di codiNaturaProvvedimento | string |
| ulterioreDescrDecisione | ulteriore decisione | string |
| flagNominaCommissarioActa | nomina commissario acta | string |
| descrCommissarioActa | commissario acta | string |
| dataCessazioneMisura | data fine misura | type:DATA_TYPE |
| dataInizioRinvio | data inizio periodo | type:DATA_TYPE |
| dataFineRinvio | data fine misura dell'ordinanza | type:DATA_TYPE |
| durataSospensione | durata sospensione | type:DURATA_TYPE |
| dataSospensioneOrdinanza | data sospensione | type:DATA_TYPE |
| durataResiduaAltraMisura | durata residua misura alternativa | type:DURATA_TYPE |
| descrUfficioMagistratoCompetente | ufficio magistrato competente | string |
| motivoRichiesta | è la descrizione del codNaturaProvvedimento | string |
| ulterioreDescrizioneOrdinanza | ulteriore descrizione ordinanza | string |
| motivazioni | motivazioni | string |
| dataDecorrenzaMisuraSicurezza | data decorrenza misura | type:DATA_TYPE |
| durataMisuraSicurezza | data misura di sicurezza | type:DURATA_TYPE |
| elencoEsiti | elenco esiti | type:ESITI_TYPE |
| totaleGiorniLibertaAnticipataSpeciale | totale giorni liberta anticipata speciale | integer |
| totaleGiorniLibertaAnticipataIntegrazione | totale giorni liberta anticipata integrazione | integer |
| totaleGiorniLibertaAnticipataNormale | totale giorni liberta anticipata normale | integer |
| oggettoProcedimento | -- | string |
| codTipoRegistro | -- | string |
| OUTPUT_DETTAGLIO_ORDINANZA |
| OUTPUT_DETTAGLIO_ORDINANZA | -- | -- |
| type:DATI_RIEPILOGO_PROCEDIMENTO | -- | -- |
| type:DATI_ORDINANZA | -- | -- |
| descrFormaMisuraMA | forma della misura alternativa | string |
| descrComunitaMA | comunità misura alternativa | string |
| descrFormaMisuraMS | forma misura sicurezza | string |
| descrComunitaMS | comunità misura sicurezza | string |
| elencoMisureSicurezza | elenco misure di sicurezza | type:MISURA_SICUREZZA_TYPE |
| datiEsecuzioneMisureSicurezzaAttuali | dati esecuzione misure di sicurezza precedenti | type:MISURA_SICUREZZA_TYPE |
| datiEsecuzioneMisureSicurezzaPrecedenti | dati esecuzione misure di sicurezza attuali | type:MISURA_SICUREZZA_TYPE |
| elencoMisureRideterminate | elenco misure rideterminate | type:MISURA_SICUREZZA_TYPE |
| elencoPrescrizioni | elenco prescrizioni | type:PRESCRIZIONE_TYPE |
| datiLibertaAnticipata | dati libertà anticipata | -- |
| datiLicenza | dati della licenza | -- |
| datiIndultino | dati indultino | -- |
| datiMisuraAlternativa | dati della misura alternativa | -- |
| datiRevocaMisuraAlternativa | dati della revoca della misura alternativa | -- |
| descrDiagnosiPsichiatrica | descrizione diagnosi | string |
| datiEstinzionePena | dati estinzione pena | -- |
| datiEstinzionePenaLibCondizionale | dati estinzione pena Libertà Condizionale | -- |
| datiConcessioneRinvio | dati di concessione di rinvio | -- |
| datiProrogaDetenDomicSpeciale | dati di proroga della detenzione domiciliare | -- |
| datiProrogaDetenDomic | dati di proroga di detenzione domiciliare | -- |
| datiOrdinanzaSospesa | dati ordinanza sospesa | -- |
| datiReclamoPermesso | dati reclamo permesso | -- |
| datiReclamiCEDU | dati per reclami CEDU | -- |
| datiScomputo | Quantum Pena da Computare | -- |
| datiOrdinanzaReclamata | dati ordinanza reclamata | -- |
| datiRevocaLibertaAnticipata | dati revoca libertà anticipata | -- |
| datiRevocaLiberazioneAnticipata | dati revoca liberazione anticipata | -- |
| datiSopravvenienzaNuovoTitolo | dati di sopravvenienza del nuovo titolo | -- |
| datiRicoveri | dati ricoveri | -- |
| datiRevoca | dati della revoca | -- |
| datiSanzioneSostitutiva | dati della sanzione sostitutiva | -- |
| datiRicoveriOssPsich | dati del ricovero in osservazione | -- |
| datiEstinzioneSanzSost | dati di estinzione della sanzione sostitutiva | -- |
| datiModificaPermanSanziSost | dati modifica permanenza sanzione sostitutiva | -- |
| datiSospEsecSanzSost | dati della sospensione dell'esecuzione della sanzione sostitutiva | -- |
| datiConversioneSanzSost | dati della conversione della sanzione sostitutiva | -- |
| datiRinvioSanzSost | dati di rinvio della sanzione sostitutiva | -- |
| elencoConversioniPecuniarie | elenco conversioni pecuniarie | type:CONVERSIONE_PENE_PECUNIARIE_TYPE |
| elencoDestinatariRimessionAtti | elenco dei destinatari | type:DESTINATARIO_TYPE |
| datiEsecuzDomicilio | contenitore di dati dell'esecuzione domicilio | -- |
| descTipoControlloEsecuzione | descrizione del tipo esecuzione | string |
| elencoDestinatari | elenco dei destinatari | type:DESTINATARIO_TYPE |
| type:ERRORE | Elemento contenitore dei codici di errori restituiti dal servizio | -- |
| datiFascicoloOrigine | contenitore dei dati del fascicolo origine SIUS | -- |
| DATI_AVVISO |
| DATI_AVVISO | -- | -- |
| idAvviso | identificativo avviso | integer |
| codiceFiscaleAvvocato | codice fiscale avvocato | string |
| DATA_TYPE |
| DATA_TYPE | -- | -- |
| giorno | giorno della data | int |
| mese | mese della data | int |
| anno | anno della data | int |
| ESITI_TYPE |
| ESITI_TYPE | -- | -- |
| descrOggettoTenore | descrizione oggetto tenore | string |
| descrEsitoTenore | esito tenore | string |
| codiceOggettoTenore | codice oggetto tenore | string |
| codiceEsitoTenore | codice esito tenore | string |
| oggettoProcedimento | oggetto procedimento | string |
| DURATA_TYPE |
| DURATA_TYPE | -- | -- |
| anni | anni della durata | integer |
| mesi | mesi della durata | integer |
| giorni | giorni della durata | integer |
| PERIODI_LIBERTA_ANTICIPATA_TYPE |
| PERIODI_LIBERTA_ANTICIPATA_TYPE | -- | -- |
| flagConcesso | flag concessione | string |
| flagScorta | flag scorta | string |
| descrStatoPermesso | descrizione dello stato del permesso | string |
| codiTipoLicenza | LS, LI, LA | string |
| numeroGiorniRiduzione | numero di giorni di Riduzione | string |
| sommaRisarcimentoDanni | somma del risarcimento del danno | decimal |
| elencoPeriodi | elenco di periodo di liberta anticipata | type:PERIODI_TYPE |
| MISURA_SICUREZZA_TYPE |
| MISURA_SICUREZZA_TYPE | -- | -- |
| codiceEsitoEvento | codice esito evento | string |
| descrNatura | descrizione natura | string |
| descrTipoMisura | descrizione misura | string |
| durataMisura | durata della misura | type:DURATA_TYPE |
| PRESCRIZIONE_TYPE |
| PRESCRIZIONE_TYPE | -- | -- |
| descrTipoPrescrizione | tipo prescrizione | string |
| descrAltraPrescrizione | altra prescrizione | string |
| DESTINATARIO_TYPE |
| DESTINATARIO_TYPE | -- | -- |
| descrTipoUfficio | descrizione del tipo ufficio | string |
| descrComuneUfficio | comune dell'ufficio | string |
| descrTipoAutoritaEsterna | tipo di autorità esterna | string |
| note | note | string |
| descrSedeAutoritaEsterna | sede dell'autorità esterna | string |
| descrTipoIstitutoDeten | tipo di istituto di detenzione | string |
| descrComuneIstitutoDeten | comune dell'istituto di detenzione | string |
| idSoggetto | identificativo del soggetto | string |
| avvocatoSIEP | cognome e nome dell'avvocato SIEP | string |
| avvocatoSIUS | cognome e nome dell'avvocato SIUS | string |
| tipoCuratore | tipo di curatore | string |
| curatore | cognome nome del curatore | string |
| indirizzoCSSA | indirizzo CSSA | string |
| comuneCSSA | comune CSSA | string |
| CONVERSIONE_PENE_PECUNIARIE_TYPE |
| CONVERSIONE_PENE_PECUNIARIE_TYPE | -- | -- |
| annoFascSIEP | anno del fascicolo SIEP | integer |
| numeroFascSIEP | numero del fascicolo SIEP | integer |
| codTipoSanzione | codice tipo sanzione | string |
| importoMulta | importo della multa | decimal |
| importoAmmenda | importo dell'ammenda | decimal |
| durataEsito | durata esito | type:DURATA_TYPE |
| codOggettoTenore | oggetto del tenore | string |
| descrOggettoTenore | descrizione oggetto tenore | string |
| valoreRata | valore della rata | decimal |
| valoreUltimaRata | valore dell'ultima rata | decimal |
| dataInizioPagamento | data inizio del pagamento | type:DATA_TYPE |
| numeroGiorniInizioPagamento | numero dei giorni | string |
| numeroRate | numero delle rate | int |
| PERIODI_TYPE |
| PERIODI_TYPE | -- | -- |
| dataInizio | data inizio periodo | type:DATA_TYPE |
| dataFine | data fine periodo | type:DATA_TYPE |
| flagConcesso | flag concessione | string |

Interfaccia Metodi Disponibili

| OPERAZIONE | dettaglioOrdinanzass |
| --- | --- |
| Descrizione | Ricerca il dettaglio di un’ordinanza |
| Parametri | DATI_INPUT_DETTAGLIO(per il dettaglio del type consultare la struttura xsd) |
| Risultato | OUTPUT_DETTAGLIO_ORDINANZA(per il dettaglio del type consultare la struttura xsd) |

Dettaglio Decreto
Il web service di dettaglio decreto, ricerca i dati di dettaglio di un ‘evento’ di tipo decreto, dato in input l’identificato dell’evento.
Definizione Namespace
targetNamespace ="http://it/eng/giustizia/avvocatura/ws/type/dettaglioDecreto"
Definizione WSDL
<?xmlversion="1.0"encoding="UTF-8"standalone="no"?>
<wsdl:definitionsxmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/"
xmlns:tns="http://it/eng/giustizia/avvocatura/ws/dettaglioDecreto/"
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/"xmlns:xsd="http://www.w3.org/2001/XMLSchema"
name="dettaglioDecreto"targetNamespace="http://it/eng/giustizia/avvocatura/ws/dettaglioDecreto/">
<wsdl:types>
<xsd:schema>
<xsd:import
namespace="http://it/eng/giustizia/avvocatura/ws/type/dettaglioDecreto"
schemaLocation="dettaglio_decreto.xsd"/>
</xsd:schema>
<xsd:schematargetNamespace="http://it/eng/giustizia/avvocatura/ws/dettaglioDecreto/">
<xsd:elementname="DettaglioDecreto">
<xsd:complexType>
<xsd:sequence>
<xsd:elementname="datiDecretoInput"type="xsd:string"/>
</xsd:sequence>
</xsd:complexType>
</xsd:element>
<xsd:elementname="DettaglioDecretoResponse">
<xsd:complexType>
<xsd:sequence>
<xsd:elementname="datiDecretoOutput"type="xsd:string"/>
</xsd:sequence>
</xsd:complexType>
</xsd:element>
</xsd:schema>
</wsdl:types>
<wsdl:messagename="DettaglioDecretoResponse">
<wsdl:partelement="tns:DettaglioDecretoResponse"name="parameters">
</wsdl:part>
</wsdl:message>
<wsdl:messagename="DettaglioDecretoRequest">
<wsdl:partelement="tns:DettaglioDecreto"name="parameters">
</wsdl:part>
</wsdl:message>
<wsdl:portTypename="dettaglioDecreto">
<wsdl:operationname="DettaglioDecreto">
<wsdl:inputmessage="tns:DettaglioDecretoRequest">
</wsdl:input>
<wsdl:outputmessage="tns:DettaglioDecretoResponse">
</wsdl:output>
</wsdl:operation>
</wsdl:portType>
<wsdl:bindingname="dettaglioDecreto"type="tns:dettaglioDecreto">
<soap:bindingstyle="document"
transport="http://schemas.xmlsoap.org/soap/http"/>
<wsdl:operationname="DettaglioDecreto">
<soap:operationsoapAction="http://it/eng/giustizia/avvocatura/ws/dettaglioDecreto/DettaglioDecreto"/>
<wsdl:input>
<soap:bodyuse="literal"/>
</wsdl:input>
<wsdl:output>
<soap:bodyuse="literal"/>
</wsdl:output>
</wsdl:operation>
</wsdl:binding>
<wsdl:servicename="dettaglioDecreto">
<wsdl:portbinding="tns:dettaglioDecreto"name="dettaglioDecreto">
<soap:addresslocation="http://localhost:8080/services/dettaglioDecreto"/>
</wsdl:port>
</wsdl:service>
</wsdl:definitions>
Definizione XSD

| Nome Elemento | Note | Tipo |
| --- | --- | --- |
| DETTAGLIO_DECRETO |
| DETTAGLIO_DECRETO | Elemento root del servizio di dettaglio decreto | -- |
| type:DATI_INPUT_DETTAGLIO | Elemento contenente tutti i dati di input per la chiamata al servizio di dettaglio decreto | -- |
| type:OUTPUT_DETTAGLIO_DECRETO | Elemento contenente tutti i dati di ritorno alla chiamata del servizio di dettaglio decreto | -- |
| DATI_INPUT_DETTAGLIO |
| DATI_INPUT_DETTAGLIO | -- | -- |
| idEvento | Identificativo dell'evento SIUS che identifica il decreto per cui si sta richiedendo il dettaglio | string |
| codiTipoProvvedimento | Tipologia di Provvedimento | string |
| tipoUfficio | Tipologia dell'ufficio- ES: UDS, TDS | string |
| type:DATI_AVVISO | elemento da valorizzare per richiesta di dettaglio da elenco Avvisi. Serve per l'aggiornamento del flagVisualizzazione | -- |
| OUTPUT_DETTAGLIO_DECRETO |
| OUTPUT_DETTAGLIO_DECRETO | Elemento di output alla chiamata del servizio di dettaglio decreto | -- |
| type:DATI_RIEPILOGO_PROCEDIMENTO | Elemento contenitore di tutti i dati di riepilogo del procedimento SIUS | -- |
| type:DATI_DECRETO | Elemento contenitore dei dati che caratterizzano il DECRETO | -- |
| elencoEsiti | E' l'elenco dei tenori. | type:TENORE_TYPE |
| listaAvvocati | E' l'elenco dei Difensori | type:AVVOCATO_TYPE |
| elencoPrescrizioni | E' l'elenco delle Prescrizioni | type:PRESCRIZIONE_TYPE |
| elencoMotivazioniDecreto | presente in DettaglioDecretoInammissibilita.jsp | type:MOTIVAZIONI_TYPE |
| elencoDestinatari | E' l'elenco dei destinatari. Utilizzato anche per decreto di fissazioneUdienza | type:DESTINATARIO_TYPE |
| elencoPermessi | E' l'elenco dei permessi | type:PERMESSO_TYPE |
| datiRevocaLibertaAnticipata | Contenitore dei dati della revoca di Libertà Anticipata | -- |
| type:ERRORE | Elemento contenitore dei codici di errori restituiti dal servizio | -- |
| DATI_RIEPILOGO_PROCEDIMENTO |
| DATI_RIEPILOGO_PROCEDIMENTO | -- | -- |
| annoProcedimentoSIUS | anno del procedimento SIUS | integer |
| numeroProcedimentoSIUS | numero del procedimento SIUS | integer |
| oggettoProcedimentoSIUS | oggetto del procedimento SIUS | string |
| annoFascicoloSIEP | anno del fascicolo SIEP | integer |
| numeroFascicoloSIEP | numero del fascicolo SIEP | integer |
| ufficioFascicoloSIEP | ufficio del fascicolo SIEP | string |
| dataFascicoloSIEP | data del fascicolo SIEP | type:DATA_TYPE |
| nomeSoggetto | nome del soggetto | string |
| cognomeSoggetto | cognome del soggetto | string |
| dataNascita | data nascita del soggetto | type:DATA_TYPE |
| luogoNascita | luogo di nascita del soggetto | string |
| codiceProvincia | provincia di nascita del soggetto | string |
| dataUdienza | data udienza | type:DATA_TYPE |
| nomeMagistratoRelatore | nome del magistrato | string |
| cognomeMagistratoRelatore | cognome del magistrato | string |
| etaPresuntaAnni | età presunta del soggetto (numero anni) | integer |
| etaPresuntaMesi | età presunta del soggetto (numero mesi) | integer |
| sesso | sesso del soggetto | string |
| flagRinviata | flag rinviata | string |
| descrStatoFascicolo | descrizione dello stato del fascicolo | string |
| codiceStatoFascicolo | codice dello stato del fascicolo | string |
| DATI_DECRETO |
| DATI_DECRETO | -- | -- |
| descrTipoDecreto | descrizione del tipo decreto | string |
| annoDecreto | anno del decreto | integer |
| numeroDecreto | numero del decreto | integer |
| dataEmissione | data di emissione del decreto | type:DATA_TYPE |
| dataDepositoCancelleria | data del deposito in cancelleria del decreto | type:DATA_TYPE |
| statoProvvedimento | lo stato del provvedimento | string |
| eventualeMotivazione | note del decreto di deposito | string |
| tribSorvCompetente | tribunale di sorveglianza competente | string |
| ufficioSorvCompetente | ufficio di sorveglianza competente | string |
| descrTipoControlloEsecuzione | descrizione del tipo di esecuzione | string |
| descrCommActa | commissario ad acta | string |
| sentenzaRiferimento | sentenza riferimento | string |
| luogoSvolgimentoProva | luogo di svolgimento della prova | string |
| dataUdienza | data dell'udienza | type:DATA_TYPE |
| contenuto | descrizione Oggetto del Procedimento | string |
| note | note del decreto | string |
| type:DATI_DECRETO_UNIFICANTE | elemento contenitore di un decreto unificante | -- |
| descrProcuraEsecuzione | descrizione della procura di esecuzione | string |
| statusPersona | status della persona | string |
| annoProcRevocato | anno del procedimento revocato | integer |
| numeroProcRevocato | numero del procedimento revocato | integer |
| questuraCompEsecuzione | questura competente | string |
| descrProcuraRevocato | procura del procedimento revocato | string |
| totOreRaggiungimento | numero di ore | string |
| descrTipoIstitutoDeten | tipo istituto di detenzione | string |
| descrComuneIstitutoDeten | DettaglioDecretoInosservanzaObblighi.jsp | string |
| licenza | dati della licenza | type:LICENZA_TYPE |
| numeGiorniRevoca | DettaglioDecretoRevocaPermesso.jsp | integer |
| numeroOreRevoca | numero di ore di revoca | integer |
| DECRETO_REVOCATO | dati del decreto revocato | type:DATI_DECRETO_REVOCATO |
| elencoLicenzePeriodiLA | elenco delle licenze | type:LICENZA_TYPE |
| numeGiorniRiduzionePena | numero di giorni di riduzione pena | string |
| sommaRisarcimentoDanni | somma di risarcimento danni | decimal |
| dataSospensioneSanzSost | data di sospensione della sanzione sostitutiva | type:DATA_TYPE |
| durataSospensioneSanzSost | durata di sospensione della sanzione sostitutiva | type:DURATA_TYPE |
| dataScadenzaSospSanzSost | data di scadenza della sospensione della sanzione sostitutiva | type:DATA_TYPE |
| flagRecuperoSanzSost | recupero della sanzione sostitutiva | string |
| giorniRecuperoSanzSost | numero di giorni di recupero della sanzione sostitutiva | integer |
| durataSanzSostEspiata | durata della sanzione sostitutiva espiata | type:DURATA_TYPE |
| durataSanzSostResidua | durata della sanzione sostitutiva residua | type:DURATA_TYPE |
| codTipoRegistro | codice tipo registro | string |
| numeGiorniRevocaLA | numero di giorni di revoca di Liberta anticipata | integer |
| datiFascicoloOrigine | contenitore dati del fascicolo origine SIUS | -- |
| DATI_DECRETO_UNIFICANTE |
| DATI_DECRETO_UNIFICANTE | -- | -- |
| cognomeSoggetto | -- | string |
| nomeSoggetto | -- | string |
| dataNascita | -- | type:DATA_TYPE |
| luogoNascita | -- | string |
| numeroSIUS | stringa cosi composta: anno/numero | string |
| numeroSIEP | stringa cosi composta: anno/numero | string |
| dataUnificazione | -- | type:DATA_TYPE |
| fascicoloUnificato | stringa cosi composta: anno/numero | string |
| elencoOggetti | è l'elenco dei tenori. campo DescrOggettoTenore | string |
| ERRORE |
| ERRORE | -- | -- |
| CODICE_ERRORE | codice errore | string |
| DESCR_ERRORE | descrizione errore | string |
| DATI_AVVISO |
| DATI_AVVISO | -- | -- |
| idAvviso | Identificativo dell'avviso su SIUS | integer |
| codiceFiscaleAvvocato | Codice Fiscale dell'avvocato | string |
| AVVOCATO_TYPE |
| AVVOCATO_TYPE | -- | -- |
| cognome | cognome dell'avvocato | string |
| nome | nome dell'avvocato | string |
| descrTipo | descrizione del tipo di avvocato | string |
| codiceFiscale | codice fiscale dell'avvocato | string |
| DATA_TYPE |
| DATA_TYPE | -- | -- |
| giorno | giorno della data | int |
| mese | mese della data | int |
| anno | anno della data | int |
| TENORE_TYPE |
| TENORE_TYPE | -- | -- |
| descrOggettoTenore | descrizione oggetto | string |
| descrEsitoTenore | descrizione esito | string |
| codOggettoTenore | codice dell'oggetto | string |
| PRESCRIZIONE_TYPE |
| PRESCRIZIONE_TYPE | -- | -- |
| descrTipoPrescrizione | descrizione del tipo di prescrizione | string |
| descrAltraPrescrizione | altra prescrizione | string |
| MOTIVAZIONI_TYPE |
| MOTIVAZIONI_TYPE | -- | -- |
| descrMotivazioniDecreto | motivazioni del decreto | string |
| descrAltreMotivazioni | altre motivazioni | string |
| DESTINATARIO_TYPE |
| DESTINATARIO_TYPE | -- | -- |
| descrTipoUfficio | descrizione del tipo ufficio | string |
| descrComuneUfficio | descrizione del comune dell'ufficio | string |
| descrTipoAutoritaEsterna | descrizione del tipo di autorità esterna | string |
| note | note | string |
| descrSedeAutoritaEsterna | descrizione della sede dell'autorità esterna | string |
| descrTipoIstitutoDeten | tipo istituto di detenzione | string |
| descrComuneIstitutoDeten | comune dell'istituto di detenzione | string |
| avvocatoSIEP | stringa cognome nome dell'avvocato SIEP | string |
| avvocatoSIUS | stringa cognome nome dell'avvocato SIUS | string |
| tipoCuratore | tipo di curatore | string |
| curatore | stringa cognome nome del curatore | string |
| indirizzoCSSA | indirizzo del CSSA | string |
| comuneCSSA | comune del CSSA | string |
| DURATA_TYPE |
| DURATA_TYPE | -- | -- |
| anni | anni durata | integer |
| mesi | mesi durata | integer |
| giorni | giorni durata | integer |
| ore | anni durata | integer |
| PERMESSO_TYPE |
| PERMESSO_TYPE | -- | -- |
| descrTipoPermesso | descrizione del tipo permesso | string |
| descrStatoPermesso | stato del permesso | string |
| durataPermesso | durata del permesso | type:DURATA_TYPE |
| luogoSvolgimentoProva | luogo di svolgimento della prova | string |
| flagScorta | flag scorta | string |
| note | note | string |
| LICENZA_TYPE |
| LICENZA_TYPE | -- | -- |
| codiTipoLicenza | tipo di licenza | string |
| numeGiorni | numero di giorno della licenza | integer |
| numeMesi | numero di mesi della licenza | integer |
| numeOre | numero di ore della licenza | integer |
| dataInizio | data inizio della licenza | type:DATA_TYPE |
| dataFine | data fine della licenza | type:DATA_TYPE |
| oraInizio | ora inizio della licenza | string |
| oraFine | ora fine della licenza | string |
| luogoSvolgimentoProva | luogo di svolgimento della prova | string |
| sommaRisarcDanni | somma del risarcimento | decimal |
| descrStatoPermesso | descrizione dello stato del permesso | string |
| DATI_DECRETO_REVOCATO |
| DATI_DECRETO_REVOCATO | -- | -- |
| descrTipoDecreto | descrizione del tipo di decreto | string |
| annoDecreto | anno del decreto | integer |
| numeroDecreto | numero del decreto | integer |
| dataDepositoCancelleria | data di deposito in cancelleria | type:DATA_TYPE |
| statoProvvedimento | tato del provvedimento | string |
| elencoPermessi | elenco dei permessi | type:PERMESSO_TYPE |
| dataEmissione | data di emissione | type:DATA_TYPE |
| numeroGiorniRevocaLA | numero giorni di revoca di liberta anticipata | integer |
| annoProcRevocato | anno procedimento revocato | integer |
| numeroProcRevocato | numero del procedimento revocato | integer |
| descrOggettoProcedimento | descrizione dell'oggetto del procedimento | string |
| descrTipoUfficio | tipo di ufficio | string |
| descrComuneUfficio | comune ufficio | string |
| PERIODI_LIBERTA_ANTICIPATA_TYPE |
| PERIODI_LIBERTA_ANTICIPATA_TYPE | -- | -- |
| flagConcesso | flag concessione | string |
| flagScorta | flag scorta | string |
| descrStatoPermesso | descrizione dello stato del permesso | string |
| codiTipoLicenza | LS, LI, LA | string |
| numeroGiorniRiduzione | numero di giorni di Riduzione | string |
| sommaRisarcimentoDanni | somma del risarcimento del danno | decimal |
| elencoPeriodi | elenco di periodo di liberta anticipata | type:PERIODI_TYPE |
| PERIODI_TYPE |
| PERIODI_TYPE | -- | -- |
| dataInizio | data inizio | type:DATA_TYPE |
| dataFine | data fine | type:DATA_TYPE |
| flagConcesso | flag concessione | string |

Dettaglio Rinvio Udienza
Il web service di dettaglio rinvio udienza, ricerca i dati di dettaglio di un ‘evento’ di tipo rinvio udienza, dato in input l’identificato dell’evento.
Definizione Namespace
targetNamespace="http://it/eng/giustizia/avvocatura/ws/type/dettaglioRinvioUdienza"
Definizione WSDL
<?xmlversion="1.0"encoding="UTF-8"standalone="no"?>
<wsdl:definitionsxmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/"
xmlns:tns="http://it/eng/giustizia/avvocatura/ws/dettaglioRinvioUdienza/"
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/"xmlns:xsd="http://www.w3.org/2001/XMLSchema"
name="dettaglioRinvioUdienza"targetNamespace="http://it/eng/giustizia/avvocatura/ws/dettaglioRinvioUdienza/">
<wsdl:types>
<xsd:schema>
<xsd:import
namespace="http://it/eng/giustizia/avvocatura/ws/type/dettaglioRinvioUdienza"
schemaLocation="dettaglio_rinvio_udienza.xsd"/>
</xsd:schema>
<xsd:schema
targetNamespace="http://it/eng/giustizia/avvocatura/ws/dettaglioRinvioUdienza/">
<xsd:elementname="DettaglioRinvioUdienza">
<xsd:complexType>
<xsd:sequence>
<xsd:elementname="datiRinvioUdienzaInput"type="xsd:string"/>
</xsd:sequence>
</xsd:complexType>
</xsd:element>
<xsd:elementname="DettaglioRinvioUdienzaResponse">
<xsd:complexType>
<xsd:sequence>
<xsd:elementname="datiRinvioUdienzaOutput"type="xsd:string"/>
</xsd:sequence>
</xsd:complexType>
</xsd:element>
</xsd:schema>
</wsdl:types>
<wsdl:messagename="DettaglioRinvioUdienzaResponse">
<wsdl:partelement="tns:DettaglioRinvioUdienzaResponse"
name="datiRinvioUdienzaOutput">
</wsdl:part>
</wsdl:message>
<wsdl:messagename="DettaglioRinvioUdienzaRequest">
<wsdl:partelement="tns:DettaglioRinvioUdienza"name="datiRinvioUdienzaInput">
</wsdl:part>
</wsdl:message>
<wsdl:portTypename="dettaglioRinvioUdienza">
<wsdl:operationname="DettaglioRinvioUdienza">
<wsdl:inputmessage="tns:DettaglioRinvioUdienzaRequest">
</wsdl:input>
<wsdl:outputmessage="tns:DettaglioRinvioUdienzaResponse">
</wsdl:output>
</wsdl:operation>
</wsdl:portType>
<wsdl:bindingname="dettaglioRinvioUdienza"type="tns:dettaglioRinvioUdienza">
<soap:bindingstyle="document"
transport="http://schemas.xmlsoap.org/soap/http"/>
<wsdl:operationname="DettaglioRinvioUdienza">
<soap:operationsoapAction="http://it/eng/giustizia/avvocatura/ws/dettaglioRinvioUdienza/DettaglioRinvioUdienza"/>
<wsdl:input>
<soap:bodyuse="literal"/>
</wsdl:input>
<wsdl:output>
<soap:bodyuse="literal"/>
</wsdl:output>
</wsdl:operation>
</wsdl:binding>
<wsdl:servicename="dettaglioRinvioUdienza">
<wsdl:portbinding="tns:dettaglioRinvioUdienza"name="dettaglioRinvioUdienza">
<soap:addresslocation="http://localhost:8080/services/dettaglioRinvioUdienza"/>
</wsdl:port>
</wsdl:service>
</wsdl:definitions>
Definizione XSD

| Nome Elemento | Note | Tipo |
| --- | --- | --- |
| DETTAGLIO_RINVIO_UDIENZA |
| DETTAGLIO_RINVIO_UDIENZA | elemento root per il dettaglio di un rinvio udienza | -- |
| type:DATI_INPUT_DETTAGLIO | contenitore dei dati di input per la chiamata al servizio | -- |
| type:OUTPUT_RINVIO_UDIENZA | contenitore dei dati di output per la chiamata al servizio | -- |
| DATI_RIEPILOGO_PROCEDIMENTO |
| DATI_RIEPILOGO_PROCEDIMENTO | elemento contenitore dei dati di riepilogo del procedimento | -- |
| annoProcedimentoSIUS | anno del procedimento SIUS | integer |
| numeroProcedimentoSIUS | numero del procedimento SIUS | integer |
| oggettoProcedimentoSIUS | oggetto del procedimento SIUS | string |
| annoFascicoloSIEP | anno del fascicolo SIEP | integer |
| numeroFascicoloSIEP | numero del fascicolo SIEP | integer |
| ufficioFascicoloSIEP | ufficio del fascicolo SIEP | string |
| dataFascicoloSIEP | data del fascicolo SIEP | type:DATA_TYPE |
| nomeSoggetto | nome del soggetto | string |
| cognomeSoggetto | cognome del soggetto | string |
| dataNascita | data nascita del soggetto | type:DATA_TYPE |
| luogoNascita | luogo di nascita del soggetto | string |
| codiceProvincia | provincia di nascita del soggetto | string |
| dataUdienza | data udienza | type:DATA_TYPE |
| nomeMagistratoRelatore | nome del magistrato | string |
| cognomeMagistratoRelatore | cognome del magistrato | string |
| etaPresuntaAnni | età presunta del soggetto (numero anni) | integer |
| etaPresuntaMesi | età presunta del soggetto (numero mesi) | integer |
| sesso | sesso del soggetto | string |
| flagRinviata | flag rinviata | string |
| descrStatoFascicolo | descrizione dello stato del fascicolo | string |
| codiceStatoFascicolo | codice dello stato del fascicolo | string |
| DATI_INPUT_DETTAGLIO |
| DATI_INPUT_DETTAGLIO | contenitore dei dati di input per la chiamata al servizio | -- |
| idEvento | -- | string |
| codiTipoProvvedimento | tipo provvedimento | string |
| tipoUfficio | tipo ufficio | string |
| type:DATI_AVVISO | elemento da valorizzare per richiesta di dettaglio da elenco Avvisi. Serve per l'aggiornamento del flagVisualizzazione | -- |
| DATI_AVVISO |
| DATI_AVVISO | dati dell'avviso | -- |
| idAvviso | identificativo avviso | integer |
| codiceFiscaleAvvocato | cf avvocato | string |
| OUTPUT_RINVIO_UDIENZA |
| OUTPUT_RINVIO_UDIENZA | contenitore dei dati di output per la chiamata al servizio | -- |
| type:DATI_RIEPILOGO_PROCEDIMENTO | -- | -- |
| type:DATI_RINVIO_UDIENZA | -- | -- |
| type:ERRORE | -- | -- |
| DATI_RINVIO_UDIENZA |
| DATI_RINVIO_UDIENZA | dati del rinvio udienza | -- |
| elencoOggetti | è l'elenco dei tenori | type:TENORE_TYPE |
| dataEmissione | data emissione | type:DATA_TYPE |
| luogoSvolgimentoUdienza | luogo svolgimento udienza | string |
| dataUdienza | data udienza | type:DATA_TYPE |
| dateUdienzePrecedenti | contiene una lista di date di udienze | string |
| ERRORE |
| ERRORE | elemento contenitore di errori | -- |
| CODICE_ERRORE | -- | string |
| DESCR_ERRORE | -- | string |
| DATA_TYPE |
| DATA_TYPE | -- | -- |
| giorno | giorno della data | int |
| mese | mese della data | int |
| anno | anno della data | int |
| TENORE_TYPE |
| TENORE_TYPE | -- | -- |
| descrOggettoTenore | oggetto tenore | string |
| note | note | string |

Interfaccia Metodi Disponibili

| OPERAZIONE | dettaglioRinvioUdienza |
| --- | --- |
| Descrizione | Ricerca il dettaglio di un decreto |
| Parametri | DATI_INPUT_DETTAGLIO(per il dettaglio del type consultare la struttura xsd) |
| Risultato | OUTPUT_DETTAGLIO_DECRETO(per il dettaglio del type consultare la struttura xsd) |

Ricerca Soggetti Con Procedimento
Il web service di ricerca soggetti, effettua una ricerca dei soggetti con procedimenti di sorveglianza, dato in input specifici dati anagrafici del soggetto.
Definizione Namespace
targetNamespace ="http://it/eng/giustizia/avvocatura/ws/type/ricercaSoggettiConProcedimenti"
Definizione WSDL
<?xmlversion="1.0"encoding="UTF-8"standalone="no"?>
<wsdl:definitionsxmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/"
xmlns:tns="http://it/eng/giustizia/avvocatura/ws/ricercaSoggettiConProcedimenti/"
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/"xmlns:xsd="http://www.w3.org/2001/XMLSchema"
name="ricercaSoggettiConProcedimenti"
targetNamespace="http://it/eng/giustizia/avvocatura/ws/ricercaSoggettiConProcedimenti/">
<wsdl:types>
<xsd:schema>
<xsd:import
namespace="http://it/eng/giustizia/avvocatura/ws/type/ricercaSoggettiConProcedimenti"
schemaLocation="ricerca_soggetto.xsd"/>
</xsd:schema>
<xsd:schema
targetNamespace="http://it/eng/giustizia/avvocatura/ws/ricercaSoggettiConProcedimenti/">
<xsd:elementname="RicercaSoggettiConProcedimenti">
<xsd:complexType>
<xsd:sequence>
<xsd:elementname="datiSoggettoInput"type="xsd:string"/>
</xsd:sequence>
</xsd:complexType>
</xsd:element>
<xsd:elementname="RicercaSoggettiConProcedimentiResponse">
<xsd:complexType>
<xsd:sequence>
<xsd:elementname="datiSoggettoOutput"type="xsd:string"/>
</xsd:sequence>
</xsd:complexType>
</xsd:element>
</xsd:schema>
</wsdl:types>
<wsdl:messagename="RicercaSoggettiConProcedimentiResponse">
<wsdl:partelement="tns:RicercaSoggettiConProcedimentiResponse"
name="datiSoggettoOutput">
</wsdl:part>
</wsdl:message>
<wsdl:messagename="RicercaSoggettiConProcedimentiRequest">
<wsdl:partelement="tns:RicercaSoggettiConProcedimenti"
name="datiSoggettoInput">
</wsdl:part>
</wsdl:message>
<wsdl:portTypename="ricercaSoggettiConProcedimenti">
<wsdl:operationname="RicercaSoggettiConProcedimenti">
<wsdl:inputmessage="tns:RicercaSoggettiConProcedimentiRequest">
</wsdl:input>
<wsdl:outputmessage="tns:RicercaSoggettiConProcedimentiResponse">
</wsdl:output>
</wsdl:operation>
</wsdl:portType>
<wsdl:bindingname="ricercaSoggettiConProcedimenti"type="tns:ricercaSoggettiConProcedimenti">
<soap:bindingstyle="document"
transport="http://schemas.xmlsoap.org/soap/http"/>
<wsdl:operationname="RicercaSoggettiConProcedimenti">
<soap:operationsoapAction="http://it/eng/giustizia/avvocatura/ws/ricercaSoggettiConProcedimenti/RicercaSoggettiConProcedimenti"/>
<wsdl:input>
<soap:bodyuse="literal"/>
</wsdl:input>
<wsdl:output>
<soap:bodyuse="literal"/>
</wsdl:output>
</wsdl:operation>
</wsdl:binding>
<wsdl:servicename="ricercaSoggettiConProcedimenti">
<wsdl:portbinding="tns:ricercaSoggettiConProcedimenti"
name="ricercaSoggettiConProcedimenti">
<soap:address
location="http://localhost:8080/services/ricercaSoggettiConProcedimenti"/>
</wsdl:port>
</wsdl:service>
</wsdl:definitions>
Definizione XSD

| Nome Elemento | Note | Tipo |
| --- | --- | --- |
| RICERCA_SOGGETTO |
| RICERCA_SOGGETTO | Elemento root per la ricerca del soggetto | -- |
| type:DATI_SOGGETTO_INPUT | elemento contenitore dei dati di input alla ricerca soggetto | -- |
| type:DATI_SOGGETTO_OUTPUT | elemento contenitore dei dati di output alla ricerca soggetto | -- |
| DATI_SOGGETTO_INPUT |
| DATI_SOGGETTO_INPUT | Contenitore dati input per chiamata alla ricerca soggetto | -- |
| codiceFiscaleAvvocato | codice fiscale avvocato | string |
| codTipoUfficio | UDS: Ufficio di Sorveglianza TDS: Tribunale di Sorveglianza UDSM:Ufficio di Sorveglianza Minori TDSM:Tribunale di Sorveglianza Minori | string |
| codDistretto | distretto | string |
| type:SOGGETTO | dati del soggetto | -- |
| DATI_SOGGETTO_OUTPUT |
| DATI_SOGGETTO_OUTPUT | Contenitore dati output alla chiamata di ricerca soggetto | -- |
| elencoSoggetti | elenco dei soggetti | type:SOGGETTO_TYPE |
| type:ERRORE | contenitore di errori | -- |

Interfaccia Metodi Disponibili

| OPERAZIONE | ricercaSoggettiConProcedimenti |
| --- | --- |
| Descrizione | Ricerca un elenco di soggetti che soddisfano i criteri passati in input |
| Parametri | DATI_SOGGETTO_INPUT (per il dettaglio del type consultare la struttura xsd del servizio dettaglioProcedimento) |
| Risultato | DATI_SOGGETTO_OUTPUT(per il dettaglio del type consultare la struttura xsd del servizio dettaglioProcedimento) |

Elenco Procedimenti Per Soggetto
Il web service di elenco procedimenti del soggetto, effettua una ricerca dei procedimenti di sorveglianza di uno specifico soggetto, dato in input l’identificativo del soggetto.
Definizione Namespace
targetNamespace ="http://it/eng/giustizia/avvocatura/ws/type/elencoProcedimenti"
Definizione WSDL
<?xmlversion="1.0"encoding="UTF-8"standalone="no"?>
<wsdl:definitionsxmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/"
xmlns:tns="http://it/eng/giustizia/avvocatura/ws/elencoProcedimentiDelSoggetto/"
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/"xmlns:xsd="http://www.w3.org/2001/XMLSchema"
name="elencoProcedimentiDelSoggetto"
targetNamespace="http://it/eng/giustizia/avvocatura/ws/elencoProcedimentiDelSoggetto/">
<wsdl:types>
<xsd:schema>
<xsd:import
namespace="http://it/eng/giustizia/avvocatura/ws/type/elencoProcedimenti"
schemaLocation="elenco_procedimenti.xsd" />
</xsd:schema>
<xsd:schema
targetNamespace="http://it/eng/giustizia/avvocatura/ws/elencoProcedimentiDelSoggetto/">
<xsd:elementname="ElencoProcedimentiDelSoggetto">
<xsd:complexType>
<xsd:sequence>
<xsd:elementname="datiSoggettoInput"type="xsd:string"/>
</xsd:sequence>
</xsd:complexType>
</xsd:element>
<xsd:elementname="ElencoProcedimentiDelSoggettoResponse">
<xsd:complexType>
<xsd:sequence>
<xsd:elementname="elencoProcedimentiOutput"type="xsd:string"/>
</xsd:sequence>
</xsd:complexType>
</xsd:element>
</xsd:schema>
</wsdl:types>
<wsdl:messagename="ElencoProcedimentiDelSoggettoResponse">
<wsdl:partelement="tns:ElencoProcedimentiDelSoggettoResponse"
name="elencoProcedimentiOutput">
</wsdl:part>
</wsdl:message>
<wsdl:messagename="ElencoProcedimentiDelSoggettoRequest">
<wsdl:partelement="tns:ElencoProcedimentiDelSoggetto"name="elencoProcedimentiInput">
</wsdl:part>
</wsdl:message>
<wsdl:portTypename="elencoProcedimentiDelSoggetto">
<wsdl:operationname="ElencoProcedimentiDelSoggetto">
<wsdl:inputmessage="tns:ElencoProcedimentiDelSoggettoRequest">
</wsdl:input>
<wsdl:outputmessage="tns:ElencoProcedimentiDelSoggettoResponse">
</wsdl:output>
</wsdl:operation>
</wsdl:portType>
<wsdl:bindingname="elencoProcedimentiDelSoggetto"type="tns:elencoProcedimentiDelSoggetto">
<soap:bindingstyle="document"
transport="http://schemas.xmlsoap.org/soap/http"/>
<wsdl:operationname="ElencoProcedimentiDelSoggetto">
<soap:operationsoapAction="http://it/eng/giustizia/avvocatura/ws/elencoProcedimentiDelSoggetto/ElencoProcedimentiDelSoggetto"/>
<wsdl:input>
<soap:bodyuse="literal"/>
</wsdl:input>
<wsdl:output>
<soap:bodyuse="literal"/>
</wsdl:output>
</wsdl:operation>
</wsdl:binding>
<wsdl:servicename="elencoProcedimentiDelSoggetto">
<wsdl:portbinding="tns:elencoProcedimentiDelSoggetto"name="elencoProcedimentiDelSoggetto">
<soap:address
location="http://localhost:8080/services/elencoProcedimentiDelSoggetto"/>
</wsdl:port>
</wsdl:service>
</wsdl:definitions>
Definizione XSD

| Nome Elemento | Note | Tipo |
| --- | --- | --- |
| ELENCO_PROCEDIMENTI |
| ELENCO_PROCEDIMENTI | WS CHE EFFETTUA LA RICERCA PROCEDIMENTI PER SOGGETTO | -- |
| type:DATI_SOGGETTO_INPUT | elemento contenitore dei dati di input per la ricerca dell'elenco dei procedimenti | -- |
| type:ELENCO_PROCEDIMENTI_OUTPUT | elemento contenitore dei dati di output della ricerca dell'elenco dei procedimenti | -- |
| DATI_SOGGETTO_INPUT |
| DATI_SOGGETTO_INPUT | -- | -- |
| codiceFiscaleAvvocato | Codice fiscale avvocato | string |
| codTipoUfficio | UDS: Ufficio di Sorveglianza TDS: Tribunale di Sorveglianza UDSM:Ufficio di Sorveglianza Minori TDSM:Tribunale di Sorveglianza Minori | string |
| codDistretto | distretto | string |
| codUfficioDistretto | codice ufficio distretto | string |
| idSoggetto | identificativo soggetto | integer |
| ELENCO_PROCEDIMENTI_OUTPUT |
| ELENCO_PROCEDIMENTI_OUTPUT | -- | -- |
| elencoProcedimenti | elenco dei procedimenti | type:DATI_PROCEDIMENTO_TYPE |
| type:ERRORE | contenitore di errori | -- |
| ERRORE |
| ERRORE | -- | -- |
| CODICE_ERRORE | codice errore | string |
| DESCR_ERRORE | descrizione errore | string |
| DATI_PROCEDIMENTO_TYPE |
| DATI_PROCEDIMENTO_TYPE | -- | -- |
| idFascicoloSius | identificativo fascicolo sius | integer |
| chiaveAnno | anno del procedimento | integer |
| chiaveProgr | numero del procedimento | integer |
| codPosGiuridica | codice posizione giuridica | string |
| descrPosGiuridica | descrizione posizione giuridica | string |
| dataCameraConsiglio | data camera di consiglio | type:DATA_TYPE |
| codStatoFascicolo | codice stato fascicolo | string |
| descrStatoFascicolo | descrizione stato fascicolo | string |
| codOggettoProcedimento | oggetto del procedimento | string |
| descrOggettoProcedimento | descrizione oggetto procedimento | string |
| dataRichiesta | data richiesta | type:DATA_TYPE |
| dataAggiornamento | data aggiornamento | type:DATA_TYPE |
| descrDefinizione | definizione | string |
| codTipoAtto | codice tipo atto | string |
| descrTipoAtto | descrizione tipo atto | string |
| codTipoUfficio | UDS: Ufficio di Sorveglianza TDS: Tribunale di Sorveglianza UDSM:Ufficio di Sorveglianza Minori TDSM:Tribunale di Sorveglianza Minori | string |
| descrTipoUfficio | descrizione tipo ufficio | string |
| codUfficioDistretto | codice ufficio | string |
| descrUfficioDistretto | descrizione ufficio | string |
| DATA_TYPE |
| DATA_TYPE | -- | -- |
| giorno | giorno della data | int |
| mese | mese della data | int |
| anno | anno della data | int |

Interfaccia Metodi Disponibili

| OPERAZIONE | elencoProcedimentiDelSoggetto |
| --- | --- |
| Descrizione | Ricerca un elenco di procedimenti per soggetto |
| Parametri | DATI_SOGGETTO_INPUT (per il dettaglio del type consultare la struttura xsd) |
| Risultato | ELENCO_PROCEDIMENTI_OUTPUT (per il dettaglio del type consultare la struttura xsd) |

Ricerca Avvisi
Il web service di ricerca avvisi, restituisce un elenco di provvedimenti (ordinanze, decreti o rinvii udienze) per i quali è stato emesso un avviso.
Definizione Namespace
targetNamespace ="http://it/eng/giustizia/avvocatura/ws/type/ricercaAvvisi"
Definizione WSDL
<?xmlversion="1.0"encoding="UTF-8"standalone="no"?>
<wsdl:definitionsxmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/"
xmlns:tns="http://it/eng/giustizia/avvocatura/ws/ricercaAvvisi/"
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/"xmlns:xsd="http://www.w3.org/2001/XMLSchema"
name="ricercaAvvisi"targetNamespace="http://it/eng/giustizia/avvocatura/ws/ricercaAvvisi/">
<wsdl:types>
<xsd:schema>
<xsd:import
namespace="http://it/eng/giustizia/avvocatura/ws/type/ricercaAvvisi"
schemaLocation="ricerca_avviso.xsd"/>
</xsd:schema>
<xsd:schematargetNamespace="http://it/eng/giustizia/avvocatura/ws/ricercaAvvisi/">
<xsd:elementname="RicercaAvvisi">
<xsd:complexType>
<xsd:sequence>
<xsd:elementname="datiAvvisoInput"type="xsd:string"/>
</xsd:sequence>
</xsd:complexType>
</xsd:element>
<xsd:elementname="RicercaAvvisiResponse">
<xsd:complexType>
<xsd:sequence>
<xsd:elementname="datiAvvisoOutput"type="xsd:string"/>
</xsd:sequence>
</xsd:complexType>
</xsd:element>
</xsd:schema>
</wsdl:types>
<wsdl:messagename="RicercaAvvisiResponse">
<wsdl:partelement="tns:RicercaAvvisiResponse"name="datiAvvisoOutput">
</wsdl:part>
</wsdl:message>
<wsdl:messagename="RicercaAvvisiRequest">
<wsdl:partelement="tns:RicercaAvvisi"name="datiAvvisoInput">
</wsdl:part>
</wsdl:message>
<wsdl:portTypename="ricercaAvvisi">
<wsdl:operationname="RicercaAvvisi">
<wsdl:inputmessage="tns:RicercaAvvisiRequest">
</wsdl:input>
<wsdl:outputmessage="tns:RicercaAvvisiResponse">
</wsdl:output>
</wsdl:operation>
</wsdl:portType>
<wsdl:bindingname="ricercaAvvisi"type="tns:ricercaAvvisi">
<soap:bindingstyle="document"
transport="http://schemas.xmlsoap.org/soap/http"/>
<wsdl:operationname="RicercaAvvisi">
<soap:operation
soapAction="http://it/eng/giustizia/avvocatura/ws/ricercaAvvisi/RicercaAvvisi"/>
<wsdl:input>
<soap:bodyuse="literal"/>
</wsdl:input>
<wsdl:output>
<soap:bodyuse="literal"/>
</wsdl:output>
</wsdl:operation>
</wsdl:binding>
<wsdl:servicename="ricercaAvvisi">
<wsdl:portbinding="tns:ricercaAvvisi"name="ricercaAvvisi">
<soap:addresslocation="http://localhost:8080/services/ricercaAvvisi"/>
</wsdl:port>
</wsdl:service>
</wsdl:definitions>
Definizione XSD

| Nome Elemento | Note | Tipo |
| --- | --- | --- |
| RICERCA_AVVISO |
| RICERCA_AVVISO | elemento root per la ricerca degli avvisi | -- |
| type:DATI_AVVISO_INPUT | elemento contenitore dei dati di input per la ricerca dell'avviso | -- |
| type:DATI_AVVISO_OUTPUT | elemento contenitore dei dati di output per la ricerca dell'avviso | -- |
| AVVISO |
| AVVISO | -- | -- |
| idAvviso | identificativo avviso | integer |
| codiceFiscaleAvvocato | codice fiscale avvocato | string |
| descrTipoProvvedimento | tipo provvedimento | string |
| contenuto | contenuto | string |
| ufficioEmittente | ufficio emittente | string |
| dataInserimento | data inserimento | type:DATA_TYPE |
| annoProcedimentoSIUS | anno procedimento SIUS | integer |
| numeroProcedimentoSIUS | numero procedimento SIUS | integer |
| nomeSoggetto | nome soggetto | string |
| cognomeSoggetto | cognome soggetto | string |
| dataUdienza | data udienza | type:DATA_TYPE |
| codStatoAvviso | stato dell'avviso | string |
| idEvento | identificativo evento | string |
| codTipoProvvedimento | tipo provvedimento | string |
| codiceEsito | codice esito | string |
| ERRORE |
| ERRORE | -- | -- |
| CODICE_ERRORE | codice errore | string |
| DESCR_ERRORE | descrizione errore | string |
| DATI_AVVISO_INPUT |
| DATI_AVVISO_INPUT | -- | -- |
| dataEmissioneInizio | data inizio emissione | type:DATA_TYPE |
| dataEmissioneFine | data fine emissione | type:DATA_TYPE |
| codStatoAvviso | S=avviso visualizzato N=avviso non visualizzato T=Tutti | string |
| codDistretto | distretto | string |
| codiceFiscaleAvvocato | cf avvocato | string |
| codTipoUfficio | UDS: Ufficio di Sorveglianza TDS: Tribunale di Sorveglianza UDSM:Ufficio di Sorveglianza Minori TDSM:Tribunale di Sorveglianza Minori | string |
| DATI_AVVISO_OUTPUT |
| DATI_AVVISO_OUTPUT | -- | -- |
| type:AVVISO | elemento contenitore dei dati avviso | -- |
| type:ERRORE | elemento contenitore per gli errori | -- |
| DATA_TYPE |
| DATA_TYPE | -- | -- |
| giorno | giorno della data | int |
| mese | mese della data | int |
| anno | anno della data | int |

Interfaccia Metodi Disponibili

| OPERAZIONE | ricercaAvvisi |
| --- | --- |
| Descrizione | Ricerca un elenco di provvedimenti per cui è stato emesso avviso |
| Parametri | DATI_AVVISO_INPUT (per il dettaglio del type consultare la struttura xsd) |
| Risultato | DATI_AVVISO_OUTPUT (per il dettaglio del type consultare la struttura xsd) |

Richiesta Stampa Allegato
Il web service di stampa allegato permette di recuperate l’allegato rtf generato dal sistema SIUS per un fascicolo.
Definizione Namespace
targetNamespace="http://it/eng/giustizia/avvocatura/ws/type/richiestaStampa"
Definizione WSDL
<?xmlversion="1.0"encoding="UTF-8"standalone="no"?>
<wsdl:definitionsxmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/"
xmlns:tns="http://it/eng/giustizia/avvocatura/ws/richiestaStampa/"
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/"xmlns:xsd="http://www.w3.org/2001/XMLSchema"
name="richiestaStampa"targetNamespace="http://it/eng/giustizia/avvocatura/ws/richiestaStampa/">
<wsdl:types>
<xsd:schema>
<xsd:import
namespace="http://it/eng/giustizia/avvocatura/ws/type/richiestaStampa"
schemaLocation="richiesta_stampa.xsd"/>
</xsd:schema>
<xsd:schematargetNamespace="http://it/eng/giustizia/avvocatura/ws/richiestaStampa/">
<xsd:elementname="RichiestaStampa">
<xsd:complexType>
<xsd:sequence>
<xsd:elementname="datiStampaInput"type="xsd:string"/>
</xsd:sequence>
</xsd:complexType>
</xsd:element>
<xsd:elementname="RichiestaStampaResponse">
<xsd:complexType>
<xsd:sequence>
<xsd:elementname="datiStampaOutput"type="xsd:string"/>
</xsd:sequence>
</xsd:complexType>
</xsd:element>
</xsd:schema>
</wsdl:types>
<wsdl:messagename="RichiestaStampaRequest">
<wsdl:partelement="tns:RichiestaStampa"name="datiStampaInput"/>
</wsdl:message>
<wsdl:messagename="RichiestaStampaResponse">
<wsdl:partelement="tns:RichiestaStampaResponse"name="datiStampaOutput"/>
</wsdl:message>
<wsdl:portTypename="richiestaStampa">
<wsdl:operationname="RichiestaStampa">
<wsdl:inputmessage="tns:RichiestaStampaRequest"/>
<wsdl:outputmessage="tns:RichiestaStampaResponse"/>
</wsdl:operation>
</wsdl:portType>
<wsdl:bindingname="richiestaStampa"type="tns:richiestaStampa">
<soap:bindingstyle="document"
transport="http://schemas.xmlsoap.org/soap/http"/>
<wsdl:operationname="RichiestaStampa">
<soap:operationsoapAction="http://it/eng/giustizia/avvocatura/ws/richiestaStampa/RichiestaStampa"/>
<wsdl:input>
<soap:bodyuse="literal"/>
</wsdl:input>
<wsdl:output>
<soap:bodyuse="literal"/>
</wsdl:output>
</wsdl:operation>
</wsdl:binding>
<wsdl:servicename="richiestaStampa">
<wsdl:portbinding="tns:richiestaStampa"name="richiestaStampa">
<soap:address
location="http://localhost:8080/services/richiestaStampa"/>
</wsdl:port>
</wsdl:service></wsdl:definitions>
Definizione XSD

| Nome Elemento | Note | Tipo |
| --- | --- | --- |
| RICHIESTA_STAMPA |
| RICHIESTA_STAMPA | richiesta di download della stampa rtf | -- |
| type:DATI_STAMPA_INPUT | elemento contenitore dei dati di input per la richiesta stampa | -- |
| type:DATI_STAMPA_OUTPUT | elemento contenitore dei dati di output per la richiesta stampa | -- |
| DATI_STAMPA_INPUT |
| DATI_STAMPA_INPUT | elemento contenitore dei dati di input per la richiesta stampa | -- |
| codiceFiscaleAvvocato | codice fiscale avvocato | string |
| codTipoUfficio | UDS: Ufficio di Sorveglianza TDS: Tribunale di Sorveglianza UDSM:Ufficio di Sorveglianza Minori TDSM:Tribunale di Sorveglianza Minori | string |
| codDistretto | codice del distretto | string |
| idFascicoloSius | identificativo del fascicolo SIUS | integer |
| DATI_STAMPA_OUTPUT |
| DATI_STAMPA_OUTPUT | elemento contenitore dei dati di output per la richiesta stampa | -- |
| idFascicoloSius | identificativo del fascicolo SIUS | integer |
| ALLEGATO_RTF | allegato | base64Binary |
| type:ERRORE | contenitore dei dati di errore | -- |
| ERRORE |
| ERRORE | contenitore dei dati di errore | -- |
| CODICE_ERRORE | codice errore | string |
| DESCR_ERRORE | descrizione errore | string |

Interfaccia Metodi Disponibili

| OPERAZIONE | richiestaStampa |
| --- | --- |
| Descrizione | Recupera l’allegato rtf generato dal sistema SIUS per un fascicolo. |
| Parametri | DATI_STAMPA_INPUT (per il dettaglio del type consultare la struttura xsd) |
| Risultato | DATI_STAMPA_OUTPUT(per il dettaglio del type consultare la struttura xsd) |