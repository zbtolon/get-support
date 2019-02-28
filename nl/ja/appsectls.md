---

copyright:

  years: 1994, 2018

lastupdated: "2018-01-05"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}

# TLS 1.0 および 1.1 のサポート終了
{: #tlssupportwithdraw}

IBM は、2018 年 3 月 1 日付けでクラウド製品ならびにサービスの多くで TLS 1.0 および TLS 1.1 のサポートを終了します。 TLS 1.0 および 1.1 のサポートを終了するすべての {{site.data.keyword.Bluemix}} 製品およびサービスで、TLS 1.2 がサポートされます。
{:shortdesc}

## TLS バージョンのサポートが変更されるのはなぜですか?
{: #why}

TLS バージョンのサポートを変更することによって、セキュリティーおよびデータ・プライバシーに関する業界のベスト・プラクティスに合致するセキュアなクラウド環境が提供されます。

## TLS とは?
{: #what}

[TLS プロトコル![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://en.wikipedia.org/wiki/Transport_Layer_Security){: new_window}は、送信データの秘密が守られるようにネットワークでの通信を暗号化するために使用されます。 リリースされている TLS のバージョンには、1.0、1.1、および 1.2 があります。 HTTPS 接続はすべて TLS を使用します。 HTTPS は、{{site.data.keyword.Bluemix_notm}} 製品およびサービスへの接続がセキュアで信頼できることを保証するための主要な方式です。 一部の {{site.data.keyword.Bluemix_notm}} 製品およびサービスは、WebSocket Secure (WSS) プロトコルを使用したセキュア接続を許可していますが、このプロトコルも TLS を使用します。 TLS 1.0 および 1.1 のサポート終了は、HTTPS 接続と WSS 接続の両方に該当します。

## 影響を受けないようにするには、どのような処置が必要ですか?
{: #impact}

{{site.data.keyword.Bluemix_notm}} 製品またはサービスに対して行われるほとんどの接続は既に TLS 1.2 を使用しています。 ご使用の接続が TLS 1.0 または 1.1 を必要としない場合、影響は受けません。

TLS 1.0 または 1.1 のサポートが終了されるいずれかの製品またはサービスを使用している場合、接続が TLS 1.0 または 1.1 を必要としないことを確認する必要があります。

### {{site.data.keyword.Bluemix_notm}} 上の Cloud Foundry

Cloud Foundry アプリケーションに関しては、{{site.data.keyword.Bluemix_notm}} 外部からアプリケーションへの接続は影響を受けないことを確認しておく必要があります。 また、アプリケーションから {{site.data.keyword.Bluemix_notm}} 上の別の Cloud Foundry アプリケーションへの接続が影響を受けないことも確認してください。

Web ブラウザーから行われる接続を含め、Cloud Foundry への TLS を使用するすべての接続は影響を受ける可能性があります。 {{site.data.keyword.Bluemix_notm}} [前提条件](/docs/overview/prereqs.html#browsers)のブラウザーを含め、最新のブラウザーはすべて TLS 1.2 をサポートしています。
{: tip}

#### Cloud Foundry アプリケーションへの接続

`*.mybluemix.net` ドメインのすべての Cloud Foundry アプリケーション・エンドポイントに、TLS 1.2 のみをサポートする代替エンドポイントからアクセスできます。

代替エンドポイントを使用するには、アプリケーションのサブドメインの後に `alt.` を追加します。 例えば、アプリケーションが `https://myapplication.mybluemix.net` でホストされている場合、`https://myapplication.alt.mybluemix.net` を使用します。 また、`https://myapplication.eu-gb.mybluemix.net` であれば、`https://myapplication.alt.eu-gb.mybluemix.net` を使用します。

代替エンドポイントに正常に接続できる場合は、影響を受けません。

正常に接続できない場合は、クライアント、クライアント・ライブラリー、またはクライアント構成を変更して、TLS 1.2 に対応できるようにする必要があります。

#### Cloud Foundry アプリケーション間の接続

以下のコマンドを使用して、他のアプリケーションに接続するときに `*.mybluemix.net` ドメイン上の使用可能な代替エンドポイントに自動的にリダイレクトするように Cloud Foundry アプリケーションを構成できます。
```
cf set-env <application_name> BLUEMIX_TLS10_DISABLED true
```

`BLUEMIX_TLS10_DISABLED` を `true` に設定した後、以下のコマンドを使用して、この変更を有効にするためにアプリケーションを再ステージングする必要があります。
```
cf restage <application_name>
```

これらの変更を加えると、アプリケーションからのアウトバウンド要求は代替の TLS 1.2 専用エンドポイントにリダイレクトされます。

代替エンドポイントを使用するには、クライアントがサーバー名表示 (SNI) TLS 拡張機能をサポートしていなければなりません。 サポートしていない場合、返される証明書はクライアントによって無効と見なされる可能性があり、TLS 1.0 および 1.1 の廃止による影響であると誤った思い込みをしてしまう可能性があります。
{: tip}

### Watson 製品およびサービス

Watson 製品およびサービス用に、接続を以下のように置き換えてください。
  * `gateway.watsonplatform.net` を `gateway-tls12.watsonplatform.net` に置き換えます
  * `stream.wastonplatform.net` を `stream-tls12.watsonplatform.net` に置き換えます

これらの代替エンドポイントは、TLS 1.2 のみをサポートします。 これらの代替エンドポイントに正常に接続できる場合、影響を受けることはありません。 正常に接続できない場合は、クライアント、クライアント・ライブラリー、またはクライアント構成を変更して、TLS 1.2 に対応できるようにする必要があります。

ダラス以外のロケーションにある Watson 製品およびサービスの代替エンドポイントは提供されません。それらのエンドポイントでは既に TLS 1.2 しかサポートしていません。

`gatway-tls12.watsonplatform.net` および `stream-tls12.watsonplatform.net` はテスト専用であり、TLS 1.0 および 1.1 が廃止された後は使用できません。
{: tip}

### その他の製品またはサービス

使用可能な代替の TLS 1.2 専用エンドポイントを持たない製品またはサービスの場合、提供されているクライアントの資料を参照してください。 サポートされる TLS のバージョンおよび使用中のバージョンを判別する方法については、クライアント・ライブラリーを参照してください。 

## TLS 1.0 および 1.1 のサポートを終了する製品およびサービス
{: #prodsandservs}

以下の製品またはサービスで、TLS 1.0 および 1.1 のサポートが終了します。

{{site.data.keyword.Bluemix_notm}} 上の Cloud Foundry や {{site.data.keyword.Bluemix_notm}} カタログ内のサービスなど、一部の製品またはサービスは、複数のロケーションで提供されていることがあります。 TLS 1.0 および 1.1 は、現在サポートされているすべてのロケーションで削除されます。

{{site.data.keyword.Bluemix_notm}} Private または {{site.data.keyword.Bluemix_notm}} Local System デプロイメント、またはそのようなデプロイメントでホストされる {{site.data.keyword.Bluemix_notm}} サービスは含まれません。 ご使用のデプロイメントがまだ TLS 1.0 または 1.1 をサポートしている場合は、顧客またはサポート担当者と相談して廃止する適当な時機を決定してください。 
{: note}

### {{site.data.keyword.Bluemix_notm}} カタログから使用可能な製品またはサービス

#### クラウド・プラットフォーム

* {{site.data.keyword.Bluemix_notm}} 上の Cloud Foundry
* {{site.data.keyword.Bluemix_notm}} インフラストラクチャー (`api.softlayer.com` および `api.service.softlayer.com`)

#### API

* API Connect

#### アプリケーション・サービス

* Business Rules
* Message Hub
* Voice Agent with Watson\*
* Watson Content Knowledge Kits\*

#### データ & 分析

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
* Continuous Delivery
* Continuous Release
* DevOps Insights
* Event Management
* Globalization Pipeline
* Automated Accessibility Tester\*
* Digital Content Checker\*
* Runbook Automation\*

#### 金融

* Historical Instrument Analytics\*
* Instrument Analytics\*
* Investment Portfolio\*
* Portfolio Optimization\*
* Predictive Market Scenarios\*
* Simulated Historical Instrument Analytics\*
* Simulated Instrument Analytics\*

#### 機能

* 機能

#### インテグレーション

* App Connect
* Product Insights
* Secure Gateway
* API Harmony\*

#### IoT

* 電機向け IoT

#### モバイル

* App ID†
* Mobile Analytics
* Mobile Foundation
* Push Notifications
* App Launch\*

#### セキュリティー

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

\* {{site.data.keyword.Bluemix_notm}} カタログ内の試験サービスとして使用可能です。  
† TLS 1.0 は前に廃止されており、TLS 1.1 のみが廃止されます。  
‡ 非推奨。既存のお客様のみが使用できます。

### IBM Marketplace から使用可能な製品またはサービス

* Forms Experience Builder on Cloud
* IoT for Insurance
* Watson Customer Insight for Insurance
* Watson Marketing Insights
* Watson Knowledge Studio
* Watson Virtual Agent
* Weather Company Energy Trader

### その他の製品またはサービス
{: #prodservices}

* Teacher Advisor with Watson

## 使用している製品またはサービスがリストにない場合、どうしたらいいですか?
{: #tlsprodnotlisted}

ご使用の製品またはサービスは、既に TLS 1.2 しかサポートしていないか、今は TLS 1.0 および 1.1 を廃止しない可能性があります。 各種クライアント・ツールやオンライン・ツールを使用して、製品またはサービスのエンドポイントで TLS 1.0 および 1.1 がサポートされているかどうかを確認できます。

## サポート終了後も TLS 1.0 または 1.1 をそのまま使用できる方法はありますか?
{: #tlskeepusing}

一部の製品とサービスは、1 次エンドポイントで TLS 1.0 および 1.1 が廃止された後もそれらを引き続きサポートする代替エンドポイントを使用可能にします。

### {{site.data.keyword.Bluemix_notm}} インフラストラクチャー

TLS 1.0 および 1.1 のサポートが `api.softlayer.com` および `api.service.softlayer.com` から削除されるときには、代替エンドポイントが告知され、30 日間使用可能になります。

### Watson 製品およびサービス
{: #watsonprodservices}

サポート終了後も Watson 製品およびサービスへの接続に引き続き TLS 1.0 または 1.1 を使用するために、以下のいずれかの置き換えを実行できます。
  * `gateway.watsonplatform.net` を `gateway-tls10.wastonplatform.net` に置き換えます
  * `stream.watsonplatform.net` を `stream-tls10.watsonplatform.net` に置き換えます

TLS 1.0 および 1.1 が `gateway.watsonplatform.net` および `stream.watsonplatform.net` から削除された後、これらのバージョンの TLS をサポートするために `gateway-tls10.watsonplatform.net` および `stream-tls10.watsonplatform.net` を引き続き使用できます。

## 連絡
{: #tlssupport}

質問、懸念事項、または問題がある場合、[サポートにお問い合わせください ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://www.ibm.com/cloud/support){: new_window}。
