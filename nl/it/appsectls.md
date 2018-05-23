---

copyright:

  years: 1994, 2018

lastupdated: "2018-02-12"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Ritiro del supporto per TLS 1.0 e 1.1
{: #tlssupportwithdraw}

IBM ritirerà il supporto per TLS 1.0 e TLS 1.1 in molti prodotti e servizi cloud a partire dal 1# marzo 2018. TLS 1.2 continuerà a essere supportato per qualsiasi prodotto o servizio {{site.data.keyword.Bluemix_notm}} che stia ritirando il supporto per TLS 1.0 e 1.1.
{:shortdesc}

## Perché stiamo apportando questa modifica?
{: #why}

Questo fa parte dell'impegno di IBM nell'offrire un cloud totalmente sicuro e in linea con le procedure consigliate di settore per la sicurezza e la riservatezza dei dati.

## Cos'è TLS?
{: #what}

Il [protocollo TLS ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://en.wikipedia.org/wiki/Transport_Layer_Security){: new_window} viene utilizzato per crittografare le comunicazioni attraverso una rete per garantire che i dati trasmessi rimangano privati. Esistono tre versioni rilasciate di TLS: 1.0, 1.1 e 1.2. Tutte le connessioni HTTPS utilizzano TLS. HTTPS è il metodo predominante per garantire che le connessioni a prodotti e servizi {{site.data.keyword.Bluemix_notm}} siano attendibili e sicure. Alcuni prodotti e servizi {{site.data.keyword.Bluemix_notm}} consentono connessioni sicure tramite il protocollo WSS (WebSocket Secure) che utilizza anche TLS. Il ritiro del supporto per TLS 1.0 e 1.1 riguarda entrambe le connessioni HTTPS e WSS.

## Quali azioni devo intraprendere per assicurarmi che non subisca alcun impatto?
{: #impact}

La maggior parte delle connessioni effettuate ai prodotti o ai servizi {{site.data.keyword.Bluemix_notm}} utilizza già TLS 1.2. Se le tue connessioni non richiedono TLS 1.0 o 1.1, non subirai alcun impatto.

Se utilizzi uno dei prodotti o servizi che ritirano il supporto per TLS 1.0 o 1.1, devi confermare che le tue connessioni non richiedono TLS 1.0 o 1.1.

### Cloud Foundry su {{site.data.keyword.Bluemix_notm}}

Per le applicazioni Cloud Foundry devi confermare che non subirai alcun impatto durante la connessione alla tua applicazione dall'esterno di {{site.data.keyword.Bluemix_notm}} o durante la connessione dalla tua applicazione a un'altra applicazione Cloud Foundry su {{site.data.keyword.Bluemix_notm}}.

Tutte le connessioni a Cloud Foundry che utilizzano TLS sono potenzialmente interessate, incluse le connessioni effettuate dai browser web. Tutti i browser moderni supportano TLS 1.2, inclusi quelli che sono [Prerequisiti](https://console.bluemix.net/docs/overview/prereqs.html#browsers) di {{site.data.keyword.Bluemix_notm}}.
{: tip}

#### Connessione alla tua applicazione Cloud Foundry

Tutti gli endpoint dell'applicazione Cloud Foundry sul dominio `*.mybluemix.net` sono accessibili tramite un endpoint alternativo che supporta solo TLS 1.2.

Per utilizzare l'endpoint alternativo, aggiungi `alt.` dopo il dominio secondario della tua applicazione, ad esempio, se la tua applicazione è ospitata in `https://myapplication.mybluemix.net`, utilizza `https://myapplication.alt.mybluemix.net`. Oppure, per `https://myapplication.eu-gb.mybluemix.net`, utilizza `https://myapplication.alt.eu-gb.mybluemix.net`.

Se riesci a connetterti correttamente all'endpoint alternativo, non subirai alcun impatto.

Se non riesci a connetterti correttamente, subirai un impatto e dovrai modificare il tuo client, le tue librerie client o la configurazione del client per abilitare TLS 1.2.

#### Connessione tra le applicazioni Cloud Foundry

Puoi configurare la tua applicazione Cloud Foundry in modo che venga reindirizzata automaticamente agli endpoint alternativi disponibili sul dominio `*.mybluemix.net` durante la connessione ad altre applicazioni utilizzando il seguente comando:
```
cf set-env <application_name> BLUEMIX_TLS10_DISABLED true
```

Dopo aver impostato `BLUEMIX_TLS10_DISABLED` su `true`, la tua applicazione deve essere ripreparata utilizzando il seguente comando per rendere effettiva questa modifica:
```
cf restage <application_name>
```

Dopo aver apportato queste modifiche, qualsiasi richiesta in uscita dall'applicazione reindirizzerà ai soli endpoint alternativi di TLS 1.2.

Per utilizzare gli endpoint alternativi, il tuo client deve supportare l'estensione TLS SNI (Server Name Indication ). In caso contrario, il certificato restituito potrebbe essere considerato non valido dal tuo client. Se ciò si verifica, potresti erroneamente supporre di essere interessato dalla rimozione di TLS 1.0 e 1.1.
{: tip}

### Prodotti e servizi Watson

Per i prodotti e i servizi Watson a cui ti connetti utilizzando `gateway.watsonplatform.net` o `stream.wastonplatform.net`, sostituiscili con `gateway-tls12.watsonplatform.net` o `stream-tls12.watsonplatform.net`. Questi endpoint alternativi supportano solo TLS 1.2. Se riesci a connetterti correttamente a questi endpoint, non subirai alcun impatto. Se non riesci a connetterti correttamente, subirai un impatto e dovrai modificare il tuo client, le tue librerie client o la configurazione del client per abilitare TLS 1.2.

Gli endpoint alternativi per prodotti e servizi Watson in regioni diverse da Stati Uniti Sud non vengono forniti, in quanto supportano già solo TLS 1.2.

`gatway-tls12.watsonplatform.net` e `stream-tls12.watsonplatform.net` sono solo a scopo di test e non saranno disponibili dopo la rimozione di TLS 1.0 e 1.1.
{: tip}

### Altri prodotti e servizi

Per prodotti o servizi che non dispongono di endpoint alternativi per TLS 1.2, fai riferimento a qualsiasi documentazione disponibile per il tuo cliente o le tue librerie client per informazioni su come determinare quali versioni di TLS sono supportate e quale versione si sta utilizzando.

## Quali prodotti e servizi ritireranno il supporto per TLS 1.0 e 1.1?
{: #prodsandservs}

I seguenti prodotti e servizi ritireranno il supporto per TLS 1.0 e 1.1.

Alcuni prodotti o servizi, come Cloud Foundry su {{site.data.keyword.Bluemix_notm}} e servizi nel catalogo {{site.data.keyword.Bluemix_notm}}, potrebbero essere offerti in più regioni. TLS 1.0 e 1.1 verranno rimossi in tutte le regioni in cui sono attualmente supportati.

**Nota importante:** le distribuzioni di {{site.data.keyword.Bluemix_notm}} privato o del sistema {{site.data.keyword.Bluemix_notm}} locale o i servizi {{site.data.keyword.Bluemix_notm}} ospitati in queste distribuzioni non sono inclusi. Se la tua distribuzione supporta ancora TLS 1.0 o 1.1, collabora con il tuo cliente o rappresentante del supporto per determinare quando la rimozione è più giusta per te.

### Prodotti o servizi disponibili dal catalogo {{site.data.keyword.Bluemix_notm}}

#### Piattaforma cloud

* Cloud Foundry su {{site.data.keyword.Bluemix_notm}}
* Infrastruttura {{site.data.keyword.Bluemix_notm}} (`api.softlayer.com` e `api.service.softlayer.com`)

#### API

* API Connect

#### Servizi dell'applicazione

* Business Rules
* Message Hub
* Voice Agent with Watson\*
* Watson Content Knowledge Kits\*

#### Data & Analytics

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

* Historical Instrument Analytics\*
* Instrument Analytics\*
* Investment Portfolio\*
* Portfolio Optimization\*
* Predictive Market Scenarios\*
* Simulated Historical Instrument Analytics\*
* Simulated Instrument Analytics\*

#### Functions

* Functions

#### Integra

* App Connect
* Product Insights
* Secure Gateway
* API Harmony\*

#### Internet delle cose

* IoT for Electronics

#### Mobile

* App ID†
* Mobile Analytics
* Mobile Foundation
* Push Notifications
* App Launch\*

#### Sicurezza

* App ID†
* SSL Certificates†

#### Watson

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
† TLS 1.0 è già stato rimosso, verrà rimosso solo TLS 1.1.  
‡ Obsoleto, disponibile solo per i clienti esistenti.

### Prodotti o servizi disponibili in IBM Marketplace

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

Il tuo prodotto o servizio potrebbe già supportare TLS 1.2 o potrebbe non rimuovere TLS 1.0 e 1.1 in questo momento. Sono disponibili vari strumenti client e online che puoi utilizzare per verificare se TLS 1.0 e 1.1 sono supportati dagli endpoint di un prodotto o di un servizio.

## C'è un modo per continuare a utilizzare TLS 1.0 o 1.1 dopo che il supporto è stato ritirato?
{: #tlskeepusing}

Alcuni prodotti e servizi stanno rendendo disponibili endpoint alternativi che continueranno a supportare TLS 1.0 e 1.1 dopo che questi saranno stati rimossi dagli endpoint primari.

### Infrastruttura {{site.data.keyword.Bluemix_notm}}

Quando il supporto per TLS 1.0 e 1.1 viene rimosso da `api.softlayer.com` e `api.service.softlayer.com`, verranno annunciati degli endpoint alternativi che supportano TLS 1.0 e 1.1 e verranno resi disponibili per 30 giorni.

### Prodotti e servizi Watson
{: #watsonprodservices}

Se devi continuare a utilizzare TLS 1.0 o 1.1 durante la connessione a prodotti e servizi Watson dopo il ritiro del supporto, puoi sostituire `gateway.watsonplatform.net` con `gateway-tls10.wastonplatform.net` o `stream.watsonplatform.net` con `stream-tls10.watsonplatform.net`. `gateway-tls10.watsonplatform.net` e `stream-tls10.watsonplatform.net` supportano TLS 1.0, 1.1 e 1.2 e continueranno a essere disponibili per l'uso dopo che TLS 1.0 e 1.1 saranno stati rimossi da `gateway.watsonplatform.net` e `stream.watsonplatform.net`.

## Contattaci
{: #tlssupport}

Se hai domande, dubbi o problemi, [Contatta il supporto ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/cloud/support){: new_window}
