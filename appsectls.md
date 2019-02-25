---

copyright:

  years: 1994, 2019

lastupdated: "2019-02-14"

keywords: TLS, TLS support

subcollection: get-support

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}

# Withdrawal of support for TLS 1.0 and 1.1
{: #tlssupportwithdraw}

IBM withdrew support for TLS 1.0 and TLS 1.1 across many cloud products and services on 01 March 2018. TLS 1.2 is supported for any {{site.data.keyword.Bluemix}} product or service that is withdrawing support for TLS 1.0 and 1.1.
{:shortdesc}

## Why is TLS version support changing?
{: #why}

Changing TLS version support provides a cloud environment that is secure and in alignment with industry best practices for security and data privacy.

## What is TLS?
{: #what}

The [TLS protocol ![External link icon](../icons/launch-glyph.svg "External link icon")](https://en.wikipedia.org/wiki/Transport_Layer_Security){: new_window} is used to encrypt communications across a network to ensure that transmitted data stays private. TLS released the following versions: 1.0, 1.1, and 1.2. All HTTPS connections use TLS. HTTPS is the predominant method of ensuring that your connections to {{site.data.keyword.Bluemix_notm}} products and services are trusted and secure. Some {{site.data.keyword.Bluemix_notm}} products and services allow secure connections by using the WebSocket Secure (WSS) protocol, which also uses TLS. Withdrawal of support for TLS 1.0 and 1.1 covers both HTTPS and WSS connections.

## What actions do I need to take to make sure I'm not impacted?
{: #impact}

Most connections that are made to {{site.data.keyword.Bluemix_notm}} products or services already use TLS 1.2. If your connections don't require TLS 1.0 or 1.1, you aren't impacted.

If you're using any of the products of services that are withdrawing support for TLS 1.0 or 1.1, you must confirm that your connections don't require TLS 1.0 or 1.1.

### Cloud Foundry on {{site.data.keyword.Bluemix_notm}}
{: #cf}

For Cloud Foundry applications, you must confirm your connections to your application from outside of {{site.data.keyword.Bluemix_notm}} aren't impacted. Also, confirm that connections from your application to another Cloud Foundry application on {{site.data.keyword.Bluemix_notm}} aren't impacted.

All connections to Cloud Foundry that use TLS are potentially impacted, including any connections made from web browsers. All modern browsers support TLS 1.2, including browsers that are {{site.data.keyword.Bluemix_notm}} [Prerequisites](/docs/overview?topic=overview-browsers-platform#browsers).
{: tip}

#### Connecting to your Cloud Foundry application
{: #connect-cf}
All Cloud Foundry application endpoints on the `*.app.domain.cloud` domain can be accessed through an alternative endpoint that supports only TLS 1.2.

To use the alternative endpoint, add `alt.` after your application’s subdomain. For example, if your application is hosted at `https://myapplication.app.domain.cloud` use `https://myapplication.alt.app.domain.cloud`. Or, for `https://myapplication.eu-gb.app.domain.cloud` use `https://myapplication.alt.eu-gb.app.domain.cloud`.

If you can successfully connect to the alternative endpoint, you're not impacted.

If you can't successfully connect, you must change your client, client libraries, or client configuration to enable TLS 1.2.

#### Connecting between Cloud Foundry applications
{: #connect2}

Use the following command to configure your Cloud Foundry application to automatically redirect to the alternative endpoints that are available on the `*.app.domain.cloud` domain when you connect to other applications:
```
cf set-env <application_name> BLUEMIX_TLS10_DISABLED true
```

After you set `BLUEMIX_TLS10_DISABLED` to `true`, you must use the following command to restage your application for this change to take effect:
```
cf restage <application_name>
```

After you make these changes, any outbound request from your application redirects to the alternative TLS 1.2-only endpoints.

To use the alternative endpoints, your client must support the Server Name Indication (SNI) TLS extension. If it doesn't, the returned certificate might be considered invalid by your client and you might incorrectly assume that you're impacted by TLS 1.0 and 1.1 removal.
{: tip}

### Watson products and services
{: #watson-serv}

For Watson products and services make the following replacements to your connections:
  * Replace `gateway.watsonplatform.net` with `gateway-tls12.watsonplatform.net`
  * Replace  `stream.wastonplatform.net` with `stream-tls12.watsonplatform.net`

These alternative endpoints support TLS 1.2 only. If you can successfully connect to these alternative endpoints, you aren't impacted. If you can't successfully connect, you must change your client, client libraries, or client configuration to enable TLS 1.2.

Alternative endpoints for Watson products and services in locations other than Dallas aren't provided as these already support only TLS 1.2.

`gatway-tls12.watsonplatform.net` and `stream-tls12.watsonplatform.net` are for testing purposes only and won't be available after TLS 1.0 and 1.1 are removed.
{: tip}

### Other products or services
{: #other-serv}

For products or services that don't have alternative TLS 1.2-only endpoints available refer to any available documentation for your client. For information on how to determine which versions of TLS are supported and which version you're using refer to client libraries. 

## What products and services are withdrawing support for TLS 1.0 and 1.1?
{: #prodsandservs}

The following products or services are withdrawing support for TLS 1.0 and 1.1.

Some products or services, such as Cloud Foundry on {{site.data.keyword.Bluemix_notm}} and services in the {{site.data.keyword.Bluemix_notm}} catalog, might be offered in multiple locations. TLS 1.0 and 1.1 is removed across all locations where they're currently supported.

{{site.data.keyword.Bluemix_notm}} Private or {{site.data.keyword.Bluemix_notm}} Local System deployments or any {{site.data.keyword.Bluemix_notm}} services that are hosted in these deployments aren't included. If your deployment still supports TLS 1.0 or 1.1, work with your customer or support representative to determine when removal is right for you. 
{: note}

### Products or services available from the {{site.data.keyword.Bluemix_notm}} catalog
{: #available}

#### Cloud Platform

* Cloud Foundry on {{site.data.keyword.Bluemix_notm}}
* {{site.data.keyword.Bluemix_notm}} infrastructure (`api.softlayer.com` and `api.service.softlayer.com`)

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
* Managed MS-SQL Database Server\*

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

#### Finance
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

#### Integrate
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

#### Security
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

\* Available under experimental services in the {{site.data.keyword.Bluemix_notm}} catalog.  
† TLS 1.0 was previously removed; only TLS 1.1 is being removed.  
‡ Deprecated, only available to existing customers.

### Products or services available through IBM Marketplace
{: #marketplace}

* Forms Experience Builder on Cloud
* IoT for Insurance
* Watson Customer Insight for Insurance
* Watson Marketing Insights
* Watson Knowledge Studio
* Watson Virtual Agent
* Weather Company Energy Trader

### Other products or services
{: #prodservices}

* Teacher Advisor with Watson

## What if my product or service isn't listed?
{: #tlsprodnotlisted}

Your product or service might already support only TLS 1.2, or it might not be removing TLS 1.0 and 1.1 now. You can use various available client and online tools to check whether TLS 1.0 and 1.1 are supported by a product or service's endpoints.

## Is there a way I can continue to use TLS 1.0 or 1.1 after support is withdrawn?
{: #tlskeepusing}

Some products and services are enabling alternative endpoints that continue to support TLS 1.0 and 1.1 after they're removed from the primary endpoints.

### {{site.data.keyword.Bluemix_notm}} infrastructure
{: #infrastructure}

When support for TLS 1.0 and 1.1 is removed from `api.softlayer.com` and `api.service.softlayer.com`, alternative endpoints are announced and available for 30 days.

### Watson products and services
{: #watsonprodservices}

To continue to use TLS 1.0 or 1.1 to connect to Watson products and services after support is withdrawn, you can make one of the following replacements:
  * Replace `gateway.watsonplatform.net` with `gateway-tls10.wastonplatform.net`
  * Replace `stream.watsonplatform.net` with `stream-tls10.watsonplatform.net`

You can continue to use `gateway-tls10.watsonplatform.net` and `stream-tls10.watsonplatform.net` to support TLS 1.0 and 1.1 after these versions of TLS are removed from `gateway.watsonplatform.net` and `stream.watsonplatform.net`.

## Get in touch
{: #tlssupport}

If you have any questions, concerns, or problems, [Contact support ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/cloud/support){: new_window}
