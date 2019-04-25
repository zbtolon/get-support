---

copyright:

  years: 1994, 2019

lastupdated: "2019-04-18"

keywords: TLS, TLS support

subcollection: get-support

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}

# Unterstützung für TLS 1.0 und 1.1 wird eingestellt
{: #tlssupportwithdraw}

IBM hat die Unterstützung für TLS 1.0 und TLS 1.1 bei vielen Cloud-Produkten und -Services am 1. März 2018 eingestellt. TLS 1.2 wird für alle {{site.data.keyword.Bluemix}}-Produkte und -Services unterstützt, bei denen die Unterstützung für TLS 1.0 und 1.1 eingestellt wird.
{:shortdesc}

## Warum gibt es Änderungen bei der TLS-Versionsunterstützung?
{: #why}

Die Änderung der TLS-Versionsunterstützung geht einher mit der Bereitstellung einer Cloud-Umgebung, die sicher ist und im Einklang mit den bewährten Verfahren (Best Practices) der Branche für Sicherheit und Datenschutz steht.

## Was ist TLS?
{: #what}

Das [TLS-Protokoll![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://en.wikipedia.org/wiki/Transport_Layer_Security){: new_window} wird zur Verschlüsselung der Kommunikation über ein gesamtes Netzwerk verwendet, um die Vertraulichkeit der übertragenen Daten sicherzustellen. TLS hat die folgenden Versionen freigegeben: 1.0, 1.1 und 1.2. Bei allen HTTPS-Verbindungen wird TLS verwendet. Im Allgemeinen wird mithilfe von HTTPS sichergestellt, dass Ihre Verbindungen zu {{site.data.keyword.Bluemix_notm}}-Produkten und -Services zuverlässig und sicher sind. Einige {{site.data.keyword.Bluemix_notm}}-Produkte und -Service ermöglichen sichere Verbindungen über das WSS-Protokoll (WSS = WebSocket Secure), bei dem ebenfalls TLS verwendet wird. Das Einstellen der Unterstützung für TLS 1.0 und 1.1 bezieht sich sowohl auf HTTPS- als auch auf WSS-Verbindungen.

## Welche Vorkehrungen muss ich treffen, um Beeinträchtigungen zu vermeiden?
{: #impact}

Bei den meisten Verbindungen zu {{site.data.keyword.Bluemix_notm}}-Produkten und -Services wird bereits TLS 1.2 verwendet. Wenn Ihre Verbindungen nicht TLS 1.0 oder 1.1 erfordern, sind Sie nicht betroffen.

Wenn Sie Produkte oder Services verwenden, bei denen die Unterstützung für TLS 1.0 oder 1.1 eingestellt wird, müssen Sie sich vergewissern, dass Ihre Verbindungen TLS 1.0 oder 1.1 nicht benötigen.

### Cloud Foundry in {{site.data.keyword.Bluemix_notm}}
{: #cf}

Bei Cloud Foundry-Anwendungen müssen Sie sich vergewissern, dass die Verbindungen, die Sie außerhalb von {{site.data.keyword.Bluemix_notm}} zu Ihrer Anwendung herstellen, nicht betroffen sind. Versichern Sie sich außerdem auch, dass Verbindungen von Ihrer Anwendung zu einer anderen Cloud Foundry-Anwendung auf {{site.data.keyword.Bluemix_notm}} nicht betroffen sind.

Alle Verbindungen zu Cloud Foundry, bei denen TLS verwendet wird, sind möglicherweise betroffen. Dies schließt über Web-Browser hergestellte Verbindungen ein. Alle aktuellen Browser einschließlich der Browser, die [Voraussetzung](/docs/overview?topic=overview-prereqs-platform#prereqs-platform) für {{site.data.keyword.Bluemix_notm}} sind, unterstützen TLS 1.2.
{: tip}

#### Verbindung zu Ihrer Cloud Foundry-Anwendung herstellen
{: #connect-cf}
Auf alle Cloud Foundry-Anwendungsendpunkte in der Domäne `*.app.domain.cloud` kann über einen alternativen Endpunkt zugegriffen werden, der ausschließlich TLS 1.2 unterstützt.

Wenn der alternative Endpunkt verwendet werden soll, stellen Sie der Unterdomäne Ihrer Anwendung die Zeichenfolge `alt.` nach. Wenn Ihre Anwendung beispielsweise unter `https://myapplication.app.domain.cloud` gehostet wird, verwenden Sie `https://myapplication.alt.app.domain.cloud`. Oder verwenden Sie `https://myapplication.alt.eu-gb.app.domain.cloud` für `https://myapplication.eu-gb.app.domain.cloud`.

Wenn Sie die Verbindung zu dem alternativen Endpunkt erfolgreich herstellen können, ergeben sich durch die Einstellung der Unterstützung keine Beeinträchtigungen für Sie.

Falls Sie nicht in der Lage sind, eine solche Verbindung herzustellen, müssen Sie Ihren Client, die Clientbibliotheken oder die Clientkonfiguration ändern, damit die Verwendung von TLS 1.2 möglich ist.

#### Verbindungen zwischen Cloud Foundry-Anwendungen
{: #connect2}

Mit dem folgenden Befehl können Sie Ihre Cloud Foundry-Anwendung so konfigurieren, dass beim Herstellen von Verbindungen zu anderen Anwendungen automatisch eine Weiterleitung an die in der Domäne `*.app.domain.cloud` verfügbaren alternativen Endpunkte erfolgt:
```
cf set-env <Anwendungsname> BLUEMIX_TLS10_DISABLED true
```

Nachdem Sie für `BLUEMIX_TLS10_DISABLED` den Wert `true` festgelegt haben, müssen Sie mit dem folgenden Befehl ein erneutes Staging für die Anwendung durchführen, damit diese Änderung in Kraft tritt:
```
cf restage <Anwendungsname>
```

Nach Durchführen dieser Änderungen werden alle von Ihrer Anwendung abgehenden Anforderungen an die alternativen Endpunkte weitergeleitet, bei denen ausschließlich TLS 1.2 verwendet wird.

Damit eine Verwendung der alternativen Endpunkte überhaupt möglich ist, muss Ihr Client die TLS-Erweiterung SNI (Server Name Indication) unterstützen. Wenn das nicht der Fall ist, stuft Ihr Client das zurückgegebene Zertifikat möglicherweise als ungültig ein und Sie könnten fälschlicherweise annehmen, dass die Einstellung der Unterstützung für TLS 1.0 und 1.1 mit Beeinträchtigungen für Sie einhergeht.
{: tip}

### Watson-Produkte und -Services
{: #watson-serv}

Nehmen Sie für Watson-Produkte und -Service die folgenden Änderungen durch Ersetzen an Ihren Verbindungen vor:
  * Ersetzen Sie `gateway.watsonplatform.net` durch `gateway-tls12.watsonplatform.net`
  * Ersetzen Sie `stream.wastonplatform.net` durch `stream-tls12.watsonplatform.net`

Diese alternativen Endpunkte unterstützen ausschließlich TLS 1.2. Wenn Sie die Verbindung zu diesen alternativen Endpunkten erfolgreich herstellen können, ergeben sich durch die Einstellung der Unterstützung keine Beeinträchtigungen für Sie. Falls Sie nicht in der Lage sind, eine solche Verbindung herzustellen, müssen Sie Ihren Client, die Clientbibliotheken oder die Clientkonfiguration ändern, damit die Verwendung von TLS 1.2 möglich ist.

An anderen Standorten als dem Standort 'Dallas' werden keine alternativen Endpunkte für Watson-Produkte und -Services bereitgestellt, da an diesen Standorten bereits ausschließlich TLS 1.2 unterstützt wird.

`gateway-tls12.watsonplatform.net` und `stream-tls12.watsonplatform.net` sind nur für Testzwecke vorgesehen und nach dem Einstellen der Unterstützung von TLS 1.0 und 1.1 nicht mehr verfügbar.
{: tip}

### Sonstige Produkte und Services
{: #other-serv}

Für Produkte oder Services, die nicht über alternative, reine TLS 1.2-Endpunkte verfügen, finden Sie Informationen in der verfügbaren Dokumentation zu Ihrem Client. Informationen darüber, wie Sie feststellen, welche Versionen von TLS unterstützt werden und welche Versionen Sie verwenden, finden Sie in den Clientbibliotheken. 

## Bei welchen Produkten und Services wird die Unterstützung für TLS 1.0 und 1.1 eingestellt?
{: #prodsandservs}

Bei den im Folgenden aufgeführten Produkten und Services wird die Unterstützung für TLS 1.0 und 1.1 eingestellt.

Einige Produkte und Services, z. B. Cloud Foundry in {{site.data.keyword.Bluemix_notm}} und Services im {{site.data.keyword.Bluemix_notm}}-Katalog, werden möglicherweise an mehreren Standorten angeboten. TLS 1.0 und 1.1 wird an allen Standorten entfernt, an denen sie derzeit unterstützt werden.

{{site.data.keyword.Bluemix_notm}} Private- und {{site.data.keyword.Bluemix_notm}} Local System-Bereitstellungen sowie in diesen Bereitstellungen gehostete {{site.data.keyword.Bluemix_notm}}-Services sind nicht eingeschlossen. Wenn Ihre Bereitstellung weiterhin TLS 1.0 oder 1.1 unterstützt, wenden Sie sich an Ihren Ansprechpartner beim Kundendienst und klären Sie mit ihm, wann diese Unterstützung beendet werden sollte. 
{: note}

### Über den {{site.data.keyword.Bluemix_notm}}-Katalog verfügbare Produkte und Services
{: #available}

#### Cloudplattform

* Cloud Foundry in {{site.data.keyword.Bluemix_notm}}
* {{site.data.keyword.Bluemix_notm}}-Infrastruktur (`api.softlayer.com` und `api.service.softlayer.com`)

#### APIs
{: #apis}

* API Connect

#### Application Services
{: #app-serv}

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
* Verwalteter MS SQL-Datenbankserver\*

#### DevOps
{: #devop}

* Auto-Scaling
* Alert Notification
* Availability Monitoring
* Continuous Delivery
* Continuous Release
* DevOps Insights
* Event Management
* Globalization Pipeline
* Automated Accessibility Tester\*
* Digital Content Checker\*
* Runbook Automation\*

#### Finanzen
{: #finance}

* Historical Instrument Analytics\*
* Instrument Analytics\*
* Investment Portfolio\*
* Portfolio Optimization\*
* Predictive Market Scenarios\*
* Simulated Historical Instrument Analytics\*
* Simulated Instrument Analytics\*

#### Funktionen
{: #function}

* Funktionen

#### Integration
{: #integrate}

* App Connect
* Product Insights
* Secure Gateway
* API Harmony\*

#### Internet of Things
{: #iot}

* IoT for Electronics

#### Mobile
{: #mobile}

* App ID†
* Mobile Analytics
* Mobile Foundation
* Push Notifications
* App Launch\*

#### Sicherheit
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

\* Bei experimentellen Services im {{site.data.keyword.Bluemix_notm}}-Katalog verfügbar.  
† TLS 1.0 wurde bereits entfernt; es wird nur TLS 1.1 entfernt.  
‡ Wird nicht weiter unterstützt. Nur noch verfügbar für Bestandskunden.

### Über IBM Marketplace verfügbare Produkte und Services
{: #marketplace}

* Forms Experience Builder on Cloud
* IoT for Insurance
* Watson Customer Insight for Insurance
* Watson Marketing Insights
* Watson Knowledge Studio
* Watson Virtual Agent
* Weather Company Energy Trader

### Sonstige Produkte und Services
{: #prodservices}

* Teacher Advisor with Watson

## Was ist, wenn mein Produkt bzw. Service nicht in der Liste enthalten ist?
{: #tlsprodnotlisted}

Möglicherweise unterstützt Ihr Produkt bzw. Service bereits ausschließlich TLS 1.2 oder die Unterstützung für TLS 1.0 und 1.1 wird zum aktuellen Zeitpunkt noch nicht eingestellt. Sie können anhand verschiedener verfügbarer Client- und Online-Tools überprüfen, ob die Endpunkte eines Produkts oder Service TLS 1.0 und 1.1 unterstützen.

## Gibt es auch nach dem Einstellen der Unterstützung eine Möglichkeit, TLS 1.0 oder 1.1 weiterhin zu benutzen?
{: #tlskeepusing}

Für manche Produkte und Services werden alternative Endpunkte zur Verfügung gestellt, an denen TLS 1.0 und 1.1 auch nach ihrem Entfernen aus den primären Endpunkten weiterhin unterstützt werden.

### {{site.data.keyword.Bluemix_notm}}-Infrastruktur
{: #infrastructure}

Wenn die Unterstützung für TLS 1.0 und 1.1 bei `api.softlayer.com` und `api.service.softlayer.com` entfernt wird, werden alternative Endpunkte angekündigt und 30 Tage zur Verfügung gestellt.

### Watson-Produkte und -Services
{: #watsonprodservices}

Wenn Sie TLS 1.0 oder 1.1 auch nach dem Einstellen der Unterstützung weiterhin bei Verbindungen zu Watson-Produkten und -Services verwenden möchten, können Sie eine der folgenden Änderungen durch Ersetzen vornehmen:
  * Ersetzen Sie `gateway.watsonplatform.net` durch `gateway-tls10.wastonplatform.net`
  * Ersetzen Sie `stream.watsonplatform.net` durch `stream-tls10.watsonplatform.net`

Sie können `gateway-tls10.watsonplatform.net` und `stream-tls10.watsonplatform.net` auch dann noch zur Unterstützung von TLS 1.0 und 1.1 verwenden, nachdem diese Versionen von TLS aus `gateway.watsonplatform.net` und `stream.watsonplatform.net` entfernt worden sind.

## Kontaktaufnahme
{: #tlssupport}

Wenden Sie sich bei Fragen, Bedenken oder Problemen an den [Support ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/cloud/support){: new_window}.
