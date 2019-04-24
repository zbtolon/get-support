---

copyright:

  years: 1994, 2019

lastupdated: "2019-02-14"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}

# Ritiro del supporto per TLS 1.0 e 1.1
{: #tlssupportwithdraw}

Il 1° marzo 2018 IBM ha ritirato il supporto per TLS 1.0 e TLS 1.1 in molti prodotti e servizi cloud. TLS 1.2 è supportato per qualsiasi prodotto o servizio {{site.data.keyword.Bluemix}} che stia ritirando il supporto per TLS 1.0 e 1.1.
{:shortdesc}

## Perché viene modificato il supporto della versione TLS?
{: #why}

La modifica del supporto della versione TLS fornisce un ambiente cloud sicuro e in linea con le procedure consigliate del settore per la sicurezza e la riservatezza dei dati.

## Cos'è TLS?
{: #what}

Il [protocollo TLS ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://en.wikipedia.org/wiki/Transport_Layer_Security){: new_window} viene utilizzato per crittografare le comunicazioni attraverso una rete per garantire che i dati trasmessi rimangano privati. TLS ha rilasciato le seguenti versioni: 1.0, 1.1 e 1.2. Tutte le connessioni HTTPS utilizzano TLS. HTTPS è il metodo predominante per garantire che le connessioni a prodotti e servizi {{site.data.keyword.Bluemix_notm}} siano attendibili e sicure. Alcuni prodotti e servizi {{site.data.keyword.Bluemix_notm}} consentono connessioni sicure utilizzando il protocollo WSS (WebSocket Secure), che utilizza anche TLS. Il ritiro del supporto per TLS 1.0 e 1.1 riguarda entrambe le connessioni HTTPS e WSS.

## Quali azioni devo svolgere per assicurarmi di non subire alcun impatto?
{: #impact}

La maggior parte delle connessioni effettuate ai prodotti o ai servizi {{site.data.keyword.Bluemix_notm}} utilizza già TLS 1.2. Se le tue connessioni non richiedono TLS 1.0 o 1.1, non subisci alcun impatto.

Se utilizzi uno dei prodotti o servizi che ritirano il supporto per TLS 1.0 o 1.1, devi confermare che le tue connessioni non richiedono TLS 1.0 o 1.1.

### Cloud Foundry su {{site.data.keyword.Bluemix_notm}}
{: #cf}

Per le applicazioni Cloud Foundry, devi confermare che le connessioni alla tua applicazione dall'esterno di {{site.data.keyword.Bluemix_notm}} non siano interessate. Conferma inoltre che le connessioni dalla tua applicazione a un'altra applicazione Cloud Foundry su {{site.data.keyword.Bluemix_notm}} non siano interessate.

Tutte le connessioni a Cloud Foundry che utilizzano TLS sono potenzialmente interessate, incluse le connessioni effettuate dai browser web. Tutti i browser moderni supportano TLS 1.2, inclusi i browser che sono [Prerequisiti](/docs/overview?topic=overview-browsers-platform#browsers) di {{site.data.keyword.Bluemix_notm}}.
{: tip}

#### Connessione alla tua applicazione Cloud Foundry
{: #connect-cf}
Tutti gli endpoint dell'applicazione Cloud Foundry sul dominio `*.app.domain.cloud` sono accessibili tramite un endpoint alternativo che supporta solo TLS 1.2.

Per utilizzare l'endpoint alternativo, aggiungi `alt.` dopo il dominio secondario della tua applicazione. Ad esempio, se la tua applicazione è ospitata su `https://myapplication.app.domain.cloud`, utilizza `https://myapplication.alt.app.domain.cloud`. Oppure, per `https://myapplication.eu-gb.app.domain.cloud`, utilizza `https://myapplication.alt.eu-gb.app.domain.cloud`.

Se puoi connetterti correttamente all'endpoint alternativo, non subisci alcun impatto.

Se non puoi connetterti correttamente, devi modificare il tuo client, le librerie client o la configurazione del client per abilitare TLS 1.2.

#### Connessione tra le applicazioni Cloud Foundry
{: #connect2}

Utilizza il seguente comando per configurare la tua applicazione Cloud Foundry per il reindirizzamento automatico agli endpoint alternativi disponibili sul dominio `*.app.domain.cloud` quando ti connetti ad altre applicazioni:
```
cf set-env <application_name> BLUEMIX_TLS10_DISABLED true
```

Dopo aver impostato `BLUEMIX_TLS10_DISABLED` su `true`, devi utilizzare il seguente comando per ripreparare la tua applicazione affinché questa modifica abbia effetto:
```
cf restage <application_name>
```

Dopo aver apportato queste modifiche, qualsiasi richiesta in uscita dalla tua applicazione reindirizza ai soli endpoint alternativi di TLS 1.2.

Per utilizzare gli endpoint alternativi, il tuo client deve supportare l'estensione TLS SNI (Server Name Indication). In caso contrario, il certificato restituito potrebbe essere considerato non valido dal tuo client e potresti erroneamente supporre di essere influenzato dalla rimozione di TLS 1.0 e 1.1.
{: tip}

### Prodotti e servizi Watson
{: #watson-serv}

Per i prodotti e i servizi Watson, effettua le seguenti sostituzioni alle tue connessioni:
  * Sostituisci `gateway.watsonplatform.net` con `gateway-tls12.watsonplatform.net`
  * Sostituisci `stream.wastonplatform.net` con `stream-tls12.watsonplatform.net`

Questi endpoint alternativi supportano solo TLS 1.2. Se puoi connetterti correttamente a questi endpoint alternativi, non subisci alcun impatto. Se non puoi connetterti correttamente, devi modificare il tuo client, le librerie client o la configurazione del client per abilitare TLS 1.2.

Gli endpoint alternativi per prodotti e servizi Watson in ubicazioni diverse da Dallas non vengono forniti, in quanto supportano già solo TLS 1.2.

`gatway-tls12.watsonplatform.net` e `stream-tls12.watsonplatform.net` sono solo a scopo di test e non saranno disponibili dopo la rimozione di TLS 1.0 e 1.1.
{: tip}

### Altri prodotti e servizi
{: #other-serv}

Per prodotti o servizi che non dispongono di endpoint alternativi solo per TLS 1.2, fai riferimento a qualsiasi documentazione disponibile per il tuo client. Per informazioni su come determinare quali versioni di TLS sono supportate e quale versione stai utilizzando, fai riferimento alle librerie client. 

## Quali prodotti e servizi ritireranno il supporto per TLS 1.0 e 1.1?
{: #prodsandservs}

I seguenti prodotti e servizi ritireranno il supporto per TLS 1.0 e 1.1.

Alcuni prodotti o servizi, come Cloud Foundry su {{site.data.keyword.Bluemix_notm}} e i servizi nel catalogo {{site.data.keyword.Bluemix_notm}}, potrebbero essere offerti in più ubicazioni. TLS 1.0 e 1.1 viene rimosso in tutte le ubicazioni in cui sono al momento supportati.

Le distribuzioni di {{site.data.keyword.Bluemix_notm}} Private o del sistema {{site.data.keyword.Bluemix_notm}} locale o qualsiasi servizio {{site.data.keyword.Bluemix_notm}} ospitato in queste distribuzioni non sono inclusi. Se la tua distribuzione supporta ancora TLS 1.0 o 1.1, collabora con il tuo cliente o rappresentante del supporto per determinare quando la rimozione è più giusta per te. 
{: note}

### Prodotti o servizi disponibili dal catalogo {{site.data.keyword.Bluemix_notm}}
{: #available}

#### Piattaforma cloud

* Cloud Foundry su {{site.data.keyword.Bluemix_notm}}
* Infrastruttura {{site.data.keyword.Bluemix_notm}} (`api.softlayer.com` e `api.service.softlayer.com`)

#### API
{: #apis}

* API Connect

#### Servizi dell'applicazione
{: #app-serv}

* Business Rules
* Message Hub
* Voice Agent with Watson\*
* Watson Content Knowledge Kits\*

#### Dati e analisi

* Compose Enterprise
* Compose for Elasticsearch
* Compose for etcd
* Compose for JanusGraph
* Compose for MongoDB
* Compose for MySQL
* Compose for PostgreSQL
* Compose for RabbitMQ
* Compose for Redis
* Compose for RethinkDB
* Compose for ScyllaDB
* Data Catalog
* Data Connect
* Data Refinery
* Decision Optimization
* Graph
* Informix
* Lift
* Weather Company Data
* Managed MS-SQL Database Server\*

#### DevOps
{: #devop}

* Auto-Scaling
* Alert Notification
* Availability Monitoring
* Fornitura continua
* Continuous Release
* DevOps Insights
* Event Management
* Globalization Pipeline
* Automated Accessibility Tester\*
* Digital Content Checker\*
* Runbook Automation\*

#### Elemento finanziario
{: #finance}

* Historical Instrument Analytics\*
* Instrument Analytics\*
* Investment Portfolio\*
* Portfolio Optimization\*
* Predictive Market Scenarios\*
* Simulated Historical Instrument Analytics\*
* Simulated Instrument Analytics\*

#### Functions
{: #function}

* Functions

#### Integra
{: #integrate}

* App Connect
* Product Insights
* Secure Gateway
* API Harmony\*

#### Internet delle cose
{: #iot}

* IoT for Electronics

#### Mobile
{: #mobile}

* App ID†
* Mobile Analytics
* Mobile Foundation
* Push Notifications
* App Launch\*

#### Sicurezza
{: #security-app}

* App ID†
* SSL Certificates†

#### Watson
{: #watson}

* Conversation
* Discovery
* Language Translator
* Natural Language Classifier
* Natural Language Understanding
* Personality Insights
* Speech to Text
* Text to Speech
* Tone Analyzer
* Visual Recognition
* Knowledge Studio\*
* Document Conversion‡
* Retrieve & Rank‡
* Tradeoff Analytics‡

\* Disponibile sotto servizi sperimentali nel catalogo {{site.data.keyword.Bluemix_notm}}.  
† TLS 1.0 è stato già rimosso; viene rimosso solo TLS 1.1.  
‡ Obsoleto, disponibile solo per i clienti esistenti.

### Prodotti o servizi disponibili in IBM Marketplace
{: #marketplace}

* Forms Experience Builder on Cloud
* IoT for Insurance
* Watson Customer Insight for Insurance
* Watson Marketing Insights
* Watson Knowledge Studio
* Watson Virtual Agent
* Weather Company Energy Trader

### Altri prodotti e servizi
{: #prodservices}

* Teacher Advisor with Watson

## Cosa succede se il mio prodotto o servizio non è elencato?
{: #tlsprodnotlisted}

Il tuo prodotto o servizio potrebbe già supportare solo TLS 1.2 o potrebbe non rimuovere TLS 1.0 e 1.1 in questo momento. Puoi utilizzare i vari strumenti client e online disponibili per verificare se TLS 1.0 e 1.1 sono supportati dagli endpoint di un prodotto o di un servizio.

## C'è un modo per continuare a utilizzare TLS 1.0 o 1.1 dopo che il supporto è stato ritirato?
{: #tlskeepusing}

Alcuni prodotti e servizi stanno abilitando endpoint alternativi che continuano a supportare TLS 1.0 e 1.1 dopo che sono stati rimossi dagli endpoint primari.

### Infrastruttura {{site.data.keyword.Bluemix_notm}}
{: #infrastructure}

Quando il supporto per TLS 1.0 e 1.1 viene rimosso da `api.softlayer.com` e `api.service.softlayer.com`, vengono annunciati gli endpoint alternativi che saranno disponibili per 30 giorni.

### Prodotti e servizi Watson
{: #watsonprodservices}

Per continuare a utilizzare TLS 1.0 o 1.1 per la connessione ai prodotti e servizi Watson dopo il ritiro del supporto, puoi effettuare una delle seguenti sostituzioni:
  * Sostituisci `gateway.watsonplatform.net` con `gateway-tls10.wastonplatform.net`
  * Sostituisci `stream.watsonplatform.net` con `stream-tls10.watsonplatform.net`

Puoi continuare a utilizzare `gateway-tls10.watsonplatform.net` e `stream-tls10.watsonplatform.net` per supportare TLS 1.0 e 1.1 dopo che queste versioni di TLS sono state rimosse da `gateway.watsonplatform.net` e `stream.watsonplatform.net`.

## Contattaci
{: #tlssupport}

Se hai domande, dubbi o problemi, [Contatta il supporto ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/cloud/support){: new_window}
