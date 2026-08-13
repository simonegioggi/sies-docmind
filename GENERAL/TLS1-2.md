---
uniqueName: tls1-2
displayName: "TLS1 2"
category: "GENERAL"
tags: []
---

# TLS1.2

> **File originale:** `MEV/SCHEDA_021/Docs/consegna docx/20222401/my/TLS1.2.docx`  
> **Tipo:** DOCX

---

# TLS1.2
DOMANDA: Sul pst hanno montato tls 1.2. Ci chiedono se Avvocatura Sies funziona ancora o è necessario un Upgrade?
RISPOSTA:
Il protocollo va di pari passo con la versione Java: nel nostro caso non abbiamo problemi in quanto la jdk di default è la versione “1.8.0_45”.

Per quanto riguarda il file di configurazione del server JBOSS 6.4 eap in uso "standalone-full.xml" (presente nel path "/home/SIES/jboss-eap-6.4.Alpha/standalone-AVVOCATURA/configuration") bisogna modificarlo in due punti:

<system-properties>
...
<property name="jdk.tls.client.protocols" value="SSLv2Hello,SSLv3,TLSv1"/>
...
</system-properties>
IN
<system-properties>
...
<property name="jdk.tls.client.protocols" value="TLSv1.2"/>
...
</system-properties>


<subsystem xmlns="urn:jboss:domain:web:2.2" default-virtual-server="default-host" native="false">
...
<connector name="https" protocol="HTTP/1.1" scheme="https" socket-binding="https" enable-lookups="false" secure="true">
<ssl name="https" key-alias="…" password="…" certificate-key-file="…" protocol="SSLv2Hello,SSLv3,TLSv1"/>
</connector>
...
</subsystem>
IN
<subsystem xmlns="urn:jboss:domain:web:2.2" default-virtual-server="default-host" native="false">
...
<connector name="https" protocol="HTTP/1.1" scheme="https" socket-binding="https" enable-lookups="false" secure="true">
<ssl name="https" key-alias="…" password="…" certificate-key-file="…" protocol="TLSv1.2"/>
</connector>
...
</subsystem>

Togliere i valori "SSLv2Hello,SSLv3" poiché nel file "java.security" (presente nel path "/usr/java/jdk1.8.0_45/jre/lib/security")
vi è scritto espressamente:
jdk.tls.disabledAlgorithms=SSLv3

Quindi:
NON aggiornare la versione Java;
cambiare il parametro SSLProtocol in TLSv1.2 nel file “standalone-full.xml” (due occorrenze);
modificare, opzionalmente nel file “java.security”:
jdk.tls.disabledAlgorithms=SSLv2Hello,SSLv3,TLSv1,TLSv1.1



# TEST DI VALIDAZIONE
Eseguire i comandi sotto indicati (se risponde con un valore per il cipher allora il protocollo è abilitato, se ritorna 0000 per il cipher allora  il protocollo è disabilitato)

openssl s_client -connect <IP>:<port>
SSL-Session:
Protocol  : TLSv1.2
Cipher    : AES128-SHA
openssl s_client -connect <IP>:<port> -tls1_2
SSL-Session:
Protocol  : TLSv1.2
Cipher    : AES128-SHA
openssl s_client -connect <IP>:<port> -ssl3
SSL-Session:
Protocol  : SSLv3
Cipher    : 0000
openssl s_client -connect <IP>:<port> -tls1
SSL-Session:
Protocol  : TLSv1
Cipher    : 0000
openssl s_client -connect <IP>:<port> -tls1_1
SSL-Session:
Protocol  : TLSv1.1
Cipher    : 0000