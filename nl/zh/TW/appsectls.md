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

# 撤銷 TLS 1.0 及 1.1 支援
{: #tlssupportwithdraw}

IBM 在 2018 年 3 月 1 日撤銷許多雲端產品及服務的 TLS 1.0 和 TLS 1.1 支援。針對撤銷 TLS 1.0 及 1.1 支援的任何 {{site.data.keyword.Bluemix}} 產品或服務，會支援 TLS 1.2。
{:shortdesc}

## TLS 版本支援為何變更？
{: #why}

變更 TLS 版本支援，可提供安全且符合安全及資料隱私方面之業界最佳作法的雲端環境。

## 何謂 TLS？
{: #what}

我們使用 [TLS 通訊協定 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://en.wikipedia.org/wiki/Transport_Layer_Security){: new_window} 來加密透過網路進行的通訊，以確保傳輸的資料能保持專用。TLS 已發行下列版本：1.0、1.1 及 1.2。所有 HTTPS 連線都會使用 TLS。HTTPS 是確定您與 {{site.data.keyword.Bluemix_notm}} 產品及服務的連線受信任且安全時，主要的方法。某些 {{site.data.keyword.Bluemix_notm}} 產品及服務容許使用 WebSocket Secure (WSS) 通訊協定來進行安全連線，而該通訊協定也使用 TLS。撤銷 TLS 1.0 及 1.1 支援同時涵蓋 HTTPS 和 WSS 連線。

## 我需要採取哪些動作，才能確保我不會受到影響？
{: #impact}

對 {{site.data.keyword.Bluemix_notm}} 產品或服務建立的大部分連線已使用 TLS 1.2。如果您的連線不需要 TLS 1.0 或 1.1，則您不會受到影響。

如果您使用任何即將撤銷 TLS 1.0 或 1.1 支援的產品或服務，則必須確認您的連線不需要 TLS 1.0 或 1.1。

### {{site.data.keyword.Bluemix_notm}} 上的 Cloud Foundry
{: #cf}

對於 Cloud Foundry 應用程式，您必須確認從 {{site.data.keyword.Bluemix_notm}} 外連接至您應用程式的連線不受影響。同時，也請確認從您應用程式連接至 {{site.data.keyword.Bluemix_notm}} 上另一個 Cloud Foundry 應用程式的連線不受影響。

所有使用 TLS 的 Cloud Foundry 連線都可能受到影響，包括任何從 Web 瀏覽器建立的連線。所有現代瀏覽器都支援 TLS 1.2，包括作為 {{site.data.keyword.Bluemix_notm}} [必要條件](/docs/overview?topic=overview-browsers-platform#browsers)的瀏覽器。
{: tip}

#### 連接至 Cloud Foundry 應用程式
{: #connect-cf}
`*.app.domain.cloud` 網域上的所有 Cloud Foundry 應用程式端點，都可以透過只支援 TLS 1.2 的替代端點進行存取。

若要使用替代端點，請在應用程式的子網域之後新增 `alt.`。比方說，如果您的應用程式是在 `https://myapplication.app.domain.cloud` 進行管理，則請使用 `https://myapplication.alt.app.domain.cloud`。或者，如果是 `https://myapplication.eu-gb.app.domain.cloud`，請使用 `https://myapplication.alt.eu-gb.app.domain.cloud`。

如果您可以順利連接至替代端點，則不受影響。

如果您無法順利連接，則必須變更用戶端、用戶端程式庫或用戶端配置，以啟用 TLS 1.2。

#### Cloud Foundry 應用程式之間的連線
{: #connect2}

使用下列指令，將 Cloud Foundry 應用程式配置為在連接至其他應用程式時，自動重新導向至 `*.app.domain.cloud` 網域上可用的替代端點：
```
cf set-env <application_name> BLUEMIX_TLS10_DISABLED true
```

將 `BLUEMIX_TLS10_DISABLED` 設為 `true` 之後，您必須使用下列指令來重新編譯打包您的應用程式，這項變更才會生效：
```
cf restage <application_name>
```

在您進行這些變更之後，來自應用程式的任何出埠要求都會重新導向至僅限 TLS 1.2 的替代端點。

若要使用替代端點，您的用戶端必須支援「伺服器名稱指示 (SNI)」TLS 延伸規格。否則，您的用戶端可能會將傳回的憑證視為無效，且您可能會不正確地假設您受到 TLS 1.0 及 1.1 移除作業的影響。
{: tip}

### Watson 產品及服務
{: #watson-serv}

若為 Watson 產品和服務，請對您的連線進行下列取代：
  * 將 `gateway.watsonplatform.net` 取代為 `gateway-tls12.watsonplatform.net`
  * 將 `stream.wastonplatform.net` 取代為 `stream-tls12.watsonplatform.net`

這些替代端點僅支援 TLS 1.2。如果您可以順利連接至這些替代端點，則不受影響。如果您無法順利連接，則必須變更用戶端、用戶端程式庫或用戶端配置，以啟用 TLS 1.2。

在達拉斯以外的位置中，未提供 Watson 產品及服務的替代端點，因為這些產品及服務已經僅支援 TLS 1.2。

`gatway-tls12.watsonplatform.net` 及 `stream-tls12.watsonplatform.net` 僅供測試使用，而且在移除 TLS 1.0 及 1.1 之後將無法使用。
{: tip}

### 其他產品或服務
{: #other-serv}

針對沒有僅限 TLS 1.2 替代端點可用的產品或服務，請參閱用戶端的任何可用文件。如需如何判定所支援 TLS 版本以及您所使用版本的相關資訊，請參閱用戶端程式庫。 

## 哪些產品及服務將撤銷對 TLS 1.0 及 1.1 的支援？
{: #prodsandservs}

下列產品或服務將撤銷對 TLS 1.0 及 1.1 的支援。

部分產品或服務（例如 {{site.data.keyword.Bluemix_notm}} 上的 Cloud Foundry 及 {{site.data.keyword.Bluemix_notm}} 型錄中的服務）可能會在多個位置提供。TLS 1.0 及 1.1 已在目前支援它們的所有位置中移除。

{{site.data.keyword.Bluemix_notm}} Private 或 {{site.data.keyword.Bluemix_notm}} Local System 部署，或者這些部署中所管理的任何 {{site.data.keyword.Bluemix_notm}} 服務皆不在此列。如果您的部署仍然支援 TLS 1.0 或 1.1，請與客戶或支援代表合作，決定適合移除的時機。
{: note}

### 可從 {{site.data.keyword.Bluemix_notm}} 型錄取得的產品或服務
{: #available}

#### 雲端平台

* {{site.data.keyword.Bluemix_notm}} 上的 Cloud Foundry
* {{site.data.keyword.Bluemix_notm}} 基礎架構（`api.softlayer.com` 及 `api.service.softlayer.com`）

#### API
{: #apis}

* API Connect

#### 應用程式服務
{: #app-serv}

* Business Rules
* Message Hub
* Voice Agent with Watson\*
* Watson Content Knowledge Kits\*

#### 資料及分析

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

#### 金融
{: #finance}

* Historical Instrument Analytics\*
* Instrument Analytics\*
* Investment Portfolio\*
* Portfolio Optimization\*
* Predictive Market Scenarios\*
* Simulated Historical Instrument Analytics\*
* Simulated Instrument Analytics\*

#### 函數
{: #function}

* 函數

#### 整合
{: #integrate}

* App Connect
* Product Insights
* Secure Gateway
* API Harmony\*

#### 物聯網
{: #iot}

* IoT for Electronics

#### 行動
{: #mobile}

* App ID†
* Mobile Analytics
* Mobile Foundation
* Push Notifications
* App Launch\*

#### 安全
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

\* 在 {{site.data.keyword.Bluemix_notm}} 型錄的實驗性服務下提供。  
† 先前已移除 TLS 1.0，將僅移除 TLS 1.1。  
‡ 已淘汰，只有現有客戶才能使用。

### 可透過 IBM Marketplace 取得的產品或服務
{: #marketplace}

* Forms Experience Builder on Cloud
* IoT for Insurance
* Watson Customer Insight for Insurance
* Watson Marketing Insights
* Watson Knowledge Studio
* Watson Virtual Agent
* Weather Company Energy Trader

### 其他產品或服務
{: #prodservices}

* Teacher Advisor with Watson

## 未列出我的產品或服務時，該怎麼辦？
{: #tlsprodnotlisted}

您的產品或服務可能已經僅支援 TLS 1.2，或是目前可能不會移除 TLS 1.0 及 1.1。您可以使用各種可用的用戶端及線上工具，來檢查產品或服務的端點是否支援 TLS 1.0 及 1.1。

## 在撤銷支援之後，是否有方法可以繼續使用 TLS 1.0 或 1.1？
{: #tlskeepusing}

部分產品及服務會啟用替代端點，以在從主要端點移除 TLS 1.0 及 1.1 之後繼續支援 TLS 1.0 及 1.1。

### {{site.data.keyword.Bluemix_notm}} 基礎架構
{: #infrastructure}

從 `api.softlayer.com` 及 `api.service.softlayer.com` 移除 TLS 1.0 及 1.1 支援後，將會公告替代端點並提供使用 30 天。

### Watson 產品及服務
{: #watsonprodservices}

若要在支援撤銷後，繼續使用 TLS 1.0 或 1.1 連接至 Watson 產品和服務，您可以進行下列其中一項取代作業：
  * 將 `gateway.watsonplatform.net` 取代為 `gateway-tls10.wastonplatform.net`
  * 將 `stream.watsonplatform.net` 取代為 `stream-tls10.watsonplatform.net`

您可以在從 `gateway.watsonplatform.net` 和 `stream.watsonplatform.net` 移除 TLS 1.0 及 1.1 之後，繼續使用 `gateway-tls10.watsonplatform.net` 和 `stream-tls10.watsonplatform.net` 以支援這些版本的 TLS。

## 聯繫
{: #tlssupport}

如果您有任何疑問、疑慮或問題，請[與支援中心聯絡 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/cloud/support){: new_window}。
