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

# Retirada de suporte para o TLS 1.0 e 1.1
{: #tlssupportwithdraw}

A IBM retirou o suporte para o TLS 1.0 e TLS 1.1 em muitos produtos e serviços de nuvem em 01 de março de 2018. O TLS 1.2 é suportado para qualquer produto ou serviço {{site.data.keyword.Bluemix}} que esteja retirando o suporte para o TLS 1.0 e 1.1.
{:shortdesc}

## Por que está mudando o suporte de versão do TLS.
{: #why}

A mudança do suporte de versão do TLS fornece um ambiente de nuvem seguro e em alinhamento com as melhores práticas do segmento de mercado para segurança e privacidade de dados.

## O que é TLS?
{: #what}

O [protocolo TLS ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://en.wikipedia.org/wiki/Transport_Layer_Security){: new_window} é usado para criptografar as comunicações em uma rede para assegurar que os dados transmitidos permaneçam privados. O TLS liberou as versões a seguir: 1.0, 1.1 e 1.2. Todas as conexões HTTPS usam o TLS. HTTPS é o método predominante de assegurar que suas conexões com produtos e serviços do {{site.data.keyword.Bluemix_notm}} sejam confiáveis e seguras. Alguns produtos e serviços do {{site.data.keyword.Bluemix_notm}} permitem conexões seguras usando o protocolo WebSocket Secure (WSS), que também usa TLS. A retirada de suporte para o TLS 1.0 e o 1.1 abrange as conexões HTTPS e WSS.

## Quais ações eu preciso tomar para ter certeza de que não serei afetado?
{: #impact}

A maioria das conexões feitas para produtos ou serviços {{site.data.keyword.Bluemix_notm}} já usa o TLS 1.2. Se as suas conexões não requererem o TLS 1.0 ou 1.1, você não será afetado.

Se você estiver usando qualquer um dos produtos de serviços que estão retirando o suporte para o TLS 1.0 ou 1.1,
confirme se as suas conexões não requerem o TLS 1.0 ou 1.1.

### Cloud Foundry no {{site.data.keyword.Bluemix_notm}}
{: #cf}

Para os aplicativos Cloud Foundry, deve-se confirmar que as conexões com o aplicativo de fora do
{{site.data.keyword.Bluemix_notm}} não são afetadas. Além disso, confirme se as conexões do aplicativo com
outro aplicativo Cloud Foundry no {{site.data.keyword.Bluemix_notm}} não são afetadas.

Todas as conexões com o Cloud Foundry que usam o TLS são potencialmente afetadas, incluindo quaisquer conexões feitas de navegadores da web. Todos os navegadores modernos suportam o TLS 1.2, incluindo aqueles que são [Pré-requisitos](/docs/overview?topic=overview-browsers-platform#browsers) do {{site.data.keyword.Bluemix_notm}}.
{: tip}

#### Conectando-se ao seu aplicativo Cloud Foundry
{: #connect-cf}
Todos os terminais de aplicativo do Cloud Foundry no domínio `*.app.domain.cloud` podem ser acessados por meio de um terminal alternativo que suporta apenas o TLS 1.2.

Para usar o terminal alternativo, inclua `alt.` Após o subdomínio do seu aplicativo. Por exemplo, se o seu aplicativo estiver hospedado em `https://myapplication.app.domain.cloud`, use `https://myapplication.alt.app.domain.cloud`. Ou para `https://myapplication.eu-gb.app.domain.cloud`, use `https://myapplication.alt.eu-gb.app.domain.cloud`.

Se você puder se conectar com êxito ao terminal alternativo, não será afetado.

Se você não puder se conectar com êxito, mude o cliente, as bibliotecas do cliente ou a configuração do
cliente para ativar o TLS 1.2.

#### Conectando entre aplicativos Cloud Foundry
{: #connect2}

Use o comando a seguir para configurar o aplicativo Cloud Foundry para redirecionar automaticamente para os terminais alternativos disponíveis no domínio `*.app.domain.cloud` quando você se conectar a outros aplicativos:
```
cf set-env <application_name> BLUEMIX_TLS10_DISABLED true
```

Depois de configurar `BLUEMIX_TLS10_DISABLED` como `true`, deve-se usar o comando a seguir para remontar seu aplicativo para que essa mudança entre em vigor:
```
cf restage <application_name>
```

Depois de fazer essas mudanças, qualquer solicitação de saída de seu aplicativo será redirecionada somente para os terminais alternativos TLS 1.2.

Para usar os terminais alternativos, o cliente deve suportar a extensão do TLS Server Name Indication (SNI). Se
não, o certificado retornado poderá ser considerado inválido pelo cliente e você poderá supor incorretamente que
foi afetado pela remoção do TLS 1.0 e 1.1.
{: tip}

### Produtos e serviços Watson
{: #watson-serv}

Para produtos e serviços do Watson, faça as substituições a seguir para suas conexões:
  * Substitua ``gateway.watsonplatform.net` com `gateway-tls12.watsonplatform.net`
  * Substitua ``stream.wastonplatform.net` com `stream-tls12.watsonplatform.net`

Esses terminais alternativos suportam apenas o TLS 1.2. Se puder se conectar com êxito a esses terminais alternativos, você não será afetado. Se você não puder se conectar com êxito, mude o cliente, as bibliotecas do cliente ou a configuração do
cliente para ativar o TLS 1.2.

Terminais alternativos para produtos e serviços do Watson em locais diferentes de Dallas não são fornecidos, pois eles já suportam apenas o TLS 1.2.

`gatway-tls12.watsonplatform.net` e `stream-tls12.watsonplatform.net`
destinam-se somente a propósitos de teste e não estarão disponíveis após a remoção do TLS 1.0 e 1.1.
{: tip}

### Outros produtos ou serviços
{: #other-serv}

Para produtos ou serviços que não têm terminais alternativos somente do TLS 1.2 disponíveis, consulte qualquer documentação disponível de seu cliente. Para obter informações sobre como determinar quais versões do TLS são suportadas e qual versão você está usando, consulte as bibliotecas do cliente. 

## Quais produtos e serviços estão retirando o suporte para o TLS 1.0 e 1.1?
{: #prodsandservs}

Os produtos ou serviços a seguir estão retirando o suporte para o TLS 1.0 e 1.1.

Alguns produtos ou serviços, como o Cloud Foundry no {{site.data.keyword.Bluemix_notm}} e os serviços no
catálogo do {{site.data.keyword.Bluemix_notm}}, podem ser oferecidos em múltiplas localizações. O TLS 1.0 e 1.1
foi removido em todas as localizações nas quais são suportados atualmente.

As implementações do {{site.data.keyword.Bluemix_notm}} Private ou do {{site.data.keyword.Bluemix_notm}} Local System ou quaisquer serviços do {{site.data.keyword.Bluemix_notm}} hospedados nessas implementações não estão incluídos. Se a sua implementação ainda suporta o TLS 1.0 ou 1.1, trabalhe com seu cliente ou representante de suporte para determinar quando a remoção é correta para você. 
{: note}

### Produtos ou serviços disponíveis no catálogo do {{site.data.keyword.Bluemix_notm}}
{: #available}

#### Plataforma de nuvem

* Cloud Foundry no {{site.data.keyword.Bluemix_notm}}
* Infraestrutura do {{site.data.keyword.Bluemix_notm}} (`api.softlayer.com` e `api.service.softlayer.com`)

#### APIs
{: #apis}

* API Connect

#### Serviços de Aplicativos
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
* Conexão de dados
* Data Refinary
* Otimização de Decisão
* Gráfico
* Informix
* Lift
* Dados da empresa de clima
* Managed MS-SQL Database Server\*

#### DevOps
{: #devop}

* Auto-Scaling
* Alert Notification
* Availability Monitoring
* Continuous Delivery
* Liberação contínua
* DevOps Insights
* Gerenciamento de eventos
* Globalization Pipeline
* Automated Accessibility Tester\*
* Digital Content Checker\*
* Runbook Automation\*

#### Finança
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

#### Integrar
{: #integrate}

* App Connect
* Product Insights
* Secure Gateway
* API Harmony\*

#### Internet of Things
{: #iot}

* IoT para Eletroeletrônico

#### Dispositivo móvel
{: #mobile}

* ID do app†
* Mobile Analytics
* Mobile Foundation
* Push Notifications
* App Launch\*

#### Segurança
{: #security-app}

* ID do app†
* SSL Certificates†

#### Watson
{: #watson}

* Conversa
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

\* Disponível sob serviços experimentais no catálogo do {{site.data.keyword.Bluemix_notm}}.  
† O TLS 1.0 foi removido anteriormente; somente o TLS 1.1 está sendo removido.  
‡ Descontinuado, disponível somente para clientes existentes.

### Produtos ou serviços disponíveis por meio do mercado de profissionais IBM
{: #marketplace}

* Forms Experience Builder on Cloud
* IoT for Insurance
* Watson Customer Insight for Insurance
* Watson Marketing Insights
* Watson Knowledge Studio
* Watson Virtual Agent
* Weather Company Energy Trader

### Outros produtos ou serviços
{: #prodservices}

* Teacher Advisor with Watson

## E se meu produto ou serviço não está listado?
{: #tlsprodnotlisted}

Seu produto ou serviço já pode suportar somente o TLS 1.2 ou pode não estar removendo o TLS 1.0 e 1.1 agora. É possível usar várias ferramentas do cliente e on-line disponíveis para verificar se o TLS 1.0 e 1.1 são suportados pelos terminais de um produto ou serviço.

## Existe uma maneira de continuar usando o TLS 1.0 ou 1.1 após a retirada do suporte?
{: #tlskeepusing}

Alguns produtos e serviços estão ativando terminais alternativos que continuam a suportar o TLS 1.0 e 1.1 depois
que são removidos dos terminais primários.

### Infraestrutura do {{site.data.keyword.Bluemix_notm}}
{: #infrastructure}

Quando o suporte para o TLS 1.0 e 1.1 for removido do `api.softlayer.com` e do `api.service.softlayer.com`, os terminais alternativos serão anunciados e estarão disponíveis por 30 dias.

### Produtos e serviços Watson
{: #watsonprodservices}

Para continuar usando o TLS 1.0 ou 1.1 para se conectar a produtos e serviços do Watson após a retirada do suporte, será possível fazer uma das substituições a seguir:
  * Substitua ``gateway.watsonplatform.net` com `gateway-tls10.wastonplatform.net`
  * Substitua `stream.watsonplatform.net` com `stream-tls10.watsonplatform.net`

É possível continuar usando `gateway-tls10.watsonplatform.net` e `stream-tls10.watsonplatform.net` para suportar o TLS 1.0 e 1.1 depois que essas versões do TLS são removidas de `gateway.watsonplatform.net` e `stream.watsonplatform.net`.

## Entre em contato
{: #tlssupport}

Se você tiver quaisquer perguntas, preocupações ou problemas, [Entre em contato com o suporte ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/cloud/support){: new_window}
