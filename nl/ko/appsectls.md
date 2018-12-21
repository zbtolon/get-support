---

copyright:

  years: 1994, 2018

lastupdated: "2018-11-10"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# TLS 1.0 및 1.1에 대한 지원 중단
{: #tlssupportwithdraw}

IBM은 2018년 3월 1일부터 여러 클라우드 제품 및 서비스에서 TLS 1.0 및 TLS 1.1에 대한 지원을 중단했습니다. TLS 1.2는 TLS 1.0 및 1.1에 대한 지원을 중단하는 모든 {{site.data.keyword.Bluemix}} 제품 또는 서비스에서 지원됩니다.
{:shortdesc}

## TLS 버전 지원이 변경되는 이유는 무엇입니까?
{: #why}

TLS 버전 지원 변경은 안전하며, 보안 및 데이터 개인정보 보호에 대한 업계 우수 사례를 따르는 클라우드 환경을 제공합니다.

## TLS는 무엇입니까?
{: #what}

[TLS 프로토콜 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://en.wikipedia.org/wiki/Transport_Layer_Security){: new_window}은 전송된 데이터가 개인용으로 유지되도록 네트워크에서 통신을 암호화하는 데 사용됩니다. TLS는 버전 1.0, 1.1 및 1.2가 릴리스되었습니다. 모든 HTTPS 연결은 TLS를 사용합니다. HTTPS는 {{site.data.keyword.Bluemix_notm}} 제품과 서비스에 대한 연결이 신뢰 가능하고 보안되도록 하는 뛰어난 방법입니다. 일부 {{site.data.keyword.Bluemix_notm}} 제품 및 서비스는 TLS도 사용하는 WSS(WebSocket Secure) 프로토콜을 사용한 보안 연결을 허용합니다. TLS 1.0 및 1.1에 대한 지원 중단에는 HTTPS 및 WSS 연결이 둘 다 포함됩니다.

## 영향을 받지 않도록 하려면 어떤 조치를 수행해야 합니까?
{: #impact}

{{site.data.keyword.Bluemix_notm}} 제품 또는 서비스에 대한 대부분의 연결은 이미 TLS 1.2를 사용하고 있습니다. 연결이 TLS 1.0 또는 1.1을 필요로 하지 않는 경우에는 영향을 받지 않습니다.

TLS 1.0 또는 1.1에 대한 지원을 중단하는 제품 또는 서비스를 사용하고 있는 경우에는 연결에 TLS 1.0 또는 1.1이 필요하지 않은지 확인해야 합니다.

### {{site.data.keyword.Bluemix_notm}}의 Cloud Foundry

Cloud Foundry 애플리케이션의 경우에는 {{site.data.keyword.Bluemix_notm}} 외부에서 사용자 애플리케이션으로의 연결이 영향을 받지 않는지 확인해야 합니다. 사용자의 애플리케이션에서 {{site.data.keyword.Bluemix_notm}}에 있는 다른 Cloud Foundry 애플리케이션으로의 연결 또한 영향을 받지 않는지 확인하십시오.

TLS를 사용하는 Cloud Foundry에 대한 모든 연결(웹 브라우저의 모든 연결 포함)은 잠재적으로 영향을 받습니다. {{site.data.keyword.Bluemix_notm}} [전제조건](/docs/overview/prereqs.html#browsers)인 브라우저를 포함한 모든 최신 브라우저는 TLS 1.2를 지원합니다.
{: tip}

#### Cloud Foundry 애플리케이션에 연결

`*.mybluemix.net` 도메인의 모든 Cloud Foundry 애플리케이션 엔드포인트는 TLS 1.2만을 지원하는 대체 엔드포인트를 통해 액세스할 수 있습니다.

대체 엔드포인트를 사용하려면 애플리케이션의 하위 도메인 뒤에 `alt.`을 추가하십시오. 예를 들어, 애플리케이션이 `https://myapplication.mybluemix.net`에서 호스팅되는 경우에는 `https://myapplication.alt.mybluemix.net`을 사용하십시오. 또는 `https://myapplication.eu-gb.mybluemix.net`의 경우에는 `https://myapplication.alt.eu-gb.mybluemix.net`을 사용하십시오.

대체 엔드포인트에 연결할 수 있는 경우에는 영향을 받지 않습니다.

연결할 수 없는 경우에는 TLS 1.2를 사용하도록 클라이언트, 클라이언트 라이브러리 또는 클라이언트 구성을 변경해야 합니다.

#### Cloud Foundry 애플리케이션 간 연결

다른 애플리케이션에 연결할 때 `*.mybluemix.net` 도메인에서 사용 가능한 대체 엔드포인트로 자동으로 경로 재지정하도록 Cloud Foundry 애플리케이션을 구성하려면 다음 명령을 사용하십시오.
```
cf set-env <application_name> BLUEMIX_TLS10_DISABLED true
```

`BLUEMIX_TLS10_DISABLED`를 `true`로 설정한 후 이 변경사항을 적용하려면 다음 명령을 사용하여 애플리케이션을 다시 스테이징해야 합니다.
```
cf restage <application_name>
```

이와 같이 변경하면 애플리케이션의 아웃바운드 요청이 대체 TLS 1.2 전용 엔드포인트로 경로 재지정됩니다.

대체 엔드포인트를 사용하려면 클라이언트가 SNI(Server Name Indication) TLS 확장을 지원해야 합니다. 그렇지 않은 경우에는 클라이언트가 리턴된 인증서를 올바르지 않은 것으로 간주할 수 있으며, 사용자가 자신이 TLS 1.0 및 1.1 제거에 영향을 받는 것으로 잘못 생각할 수 있습니다.
{: tip}

### Watson 제품 및 서비스

Watson 제품 및 서비스의 경우에는 연결에서 다음 항목을 대체하십시오.
  * `gateway.watsonplatform.net`을 `gateway-tls12.watsonplatform.net`으로 대체
  * `stream.wastonplatform.net`을 `stream-tls12.watsonplatform.net`으로 대체

이러한 대체 엔드포인트는 TLS 1.2만 지원합니다. 대체 엔드포인트에 연결할 수 있는 경우에는 영향을 받지 않습니다. 연결할 수 없는 경우에는 TLS 1.2를 사용하도록 클라이언트, 클라이언트 라이브러리 또는 클라이언트 구성을 변경해야 합니다.

댈러스 외 위치의 Watson 제품 및 서비스는 이미 TLS 1.2만 지원하므로 이에 대한 대체 엔드포인트는 제공되지 않습니다.

`gatway-tls12.watsonplatform.net` 및 `stream-tls12.watsonplatform.net`은 오로지 테스트용이며 TLS 1.0과 1.1이 제거된 후에는 사용할 수 없습니다.
{: tip}

### 기타 제품 또는 서비스

사용 가능한 대체 TLS 1.2 전용 엔드포인트가 없는 제품 또는 서비스의 경우 클라이언트에 사용 가능한 문서를 참조하십시오. 지원되는 TLS 버전 및 사용 중인 버전을 판별하는 방법에 대한 정보는 클라이언트 라이브러리를 참조하십시오. 

## TLS 1.0 및 1.1에 대한 지원을 중단하는 제품과 서비스는 무엇입니까?
{: #prodsandservs}

다음 제품 또는 서비스는 TLS 1.0 및 1.1에 대한 지원을 중단합니다.

{{site.data.keyword.Bluemix_notm}}의 Cloud Foundry와 {{site.data.keyword.Bluemix_notm}} 카탈로그의 서비스와 같은 일부 제품 또는 서비스는 여러 위치에 제공될 수 있습니다. 현재 지원되는 모든 위치에서 TLS 1.0 및 1.1이 제거됩니다.

**중요한 참고:** {{site.data.keyword.Bluemix_notm}} 프라이빗 또는 {{site.data.keyword.Bluemix_notm}} 로컬 시스템 배치나 이러한 배치에서 호스팅되는 모든 {{site.data.keyword.Bluemix_notm}} 서비스는 포함되지 않습니다. 배치가 여전히 TLS 1.0 또는 1.1을 지원하는 경우, 고객 또는 지원 담당자와 함께 제거 시기를 판별하십시오.

### {{site.data.keyword.Bluemix_notm}} 카탈로그에서 사용 가능한 제품 또는 서비스

#### 클라우드 플랫폼

* {{site.data.keyword.Bluemix_notm}}의 Cloud Foundry
* {{site.data.keyword.Bluemix_notm}} 인프라(`api.softlayer.com` 및 `api.service.softlayer.com`)

#### API

* API Connect

#### 애플리케이션 서비스

* Business Rules
* Message Hub
* Voice Agent with Watson\*
* Watson Content Knowledge Kits\*

#### 데이터 및 분석

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

#### 금융

* Historical Instrument Analytics\*
* Instrument Analytics\*
* Investment Portfolio\*
* Portfolio Optimization\*
* Predictive Market Scenarios\*
* Simulated Historical Instrument Analytics\*
* Simulated Instrument Analytics\*

#### Functions

* Functions

#### 통합

* App Connect
* Product Insights
* Secure Gateway
* API Harmony\*

#### Internet of Things

* IoT for Electronics

#### 모바일

* App ID†
* Mobile Analytics
* Mobile Foundation
* Push Notifications
* App Launch\*

#### 보안

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

\* {{site.data.keyword.Bluemix_notm}} 카탈로그의 시범 서비스에서 사용 가능합니다.  
† TLS 1.0은 이미 제거되었으며 TLS 1.1만 제거됩니다.  
‡ 더 이상 사용되지 않으며, 기존 고객만 사용할 수 있습니다.

### IBM Marketplace를 통해 사용 가능한 제품 또는 서비스

* Forms Experience Builder on Cloud
* IoT for Insurance
* Watson Customer Insight for Insurance
* Watson Marketing Insights
* Watson Knowledge Studio
* Watson Virtual Agent
* Weather Company Energy Trader

### 기타 제품 또는 서비스
{: #prodservices}

* Teacher Advisor with Watson

## 내 제품이나 서비스가 목록에 없으면 어떻게 됩니까?
{: #tlsprodnotlisted}

제품 또는 서비스가 이미 TLS 1.2만 지원하거나, 이번에 TLS 1.0 및 1.1이 제거되지 않는 경우일 수 있습니다. 다양한 클라이언트 및 온라인 도구를 사용하여 제품 또는 서비스 엔드포인트의 TLS 1.0 및 1.1 지원 여부를 확인할 수 있습니다.

## 지원이 중지된 후에도 TLS 1.0 또는 1.1을 계속 사용할 수 있는 방법이 있습니까?
{: #tlskeepusing}

일부 제품 및 서비스는 TLS 1.0 및 1.1이 기본 엔드포인트에서 제거된 후에도 계속 이들을 지원하는 대체 엔드포인트를 사용으로 설정합니다.

### {{site.data.keyword.Bluemix_notm}} 인프라

TLS 1.0 및 1.1에 대한 지원이 `api.softlayer.com` 및 `api.service.softlayer.com`에서 제거되면 대체 엔드포인트가 발표되며 30일 동안 사용 가능합니다.

### Watson 제품 및 서비스
{: #watsonprodservices}

지원이 중단된 후에도 Watson 제품 및 서비스에 연결하는 데 TLS 1.0 또는 1.1을 계속 사용하려는 경우에는 다음 대체 중 하나를 수행할 수 있습니다.
  * `gateway.watsonplatform.net`을 `gateway-tls10.wastonplatform.net`으로 대체
  * `stream.watsonplatform.net`을 `stream-tls10.watsonplatform.net`으로 대체

TLS 1.0, 1.1 및 1.2 버전이 `gateway.watsonplatform.net` 및 `stream.watsonplatform.net`에서 제거된 후에도 `gateway-tls10.watsonplatform.net` 및 `stream-tls10.watsonplatform.net`을 계속 사용하여 이러한 버전을 지원할 수 있습니다.

## 문의하기
{: #tlssupport}

질문, 관심사항 또는 문제점이 있는 경우 [지원 센터에 문의 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.ibm.com/cloud/support){: new_window}하십시오.
