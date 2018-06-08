---

copyright:

  years: 1994, 2018

lastupdated: "2018-05-22"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Retirada de suporte para o TLS 1.0 e 1.1
{: #tlssupportwithdraw}

A IBM retirou o suporte para o TLS 1.0 e TLS 1.1 em muitos produtos e serviços de nuvem em 01 de março de 2018. O TLS 1.2 é suportado para qualquer produto ou serviço {{site.data.keyword.Bluemix_notm}} que esteja retirando o suporte para o TLS 1.0 e 1.1.
{:shortdesc}

## Por que está mudando o suporte de versão do TLS.
{: #why}

A mudança do suporte de versão do TLS fornece um ambiente de nuvem seguro e em alinhamento com as melhores práticas do segmento de mercado para segurança e privacidade de dados.

## O que é TLS?
{: #what}

O [protocolo TLS ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://en.wikipedia.org/wiki/Transport_Layer_Security){: new_window} é usado para criptografar comunicações em uma rede para assegurar que os dados transmitidos permaneçam privados. O TLS liberou as versões a seguir: 1.0, 1.1 e 1.2. Todas as conexões HTTPS usam o TLS. HTTPS é o método predominante de assegurar que suas conexões com produtos e serviços do {{site.data.keyword.Bluemix_notm}} sejam confiáveis e seguras. Alguns produtos e serviços do {{site.data.keyword.Bluemix_notm}} permitem conexões seguras usando o protocolo WebSocket Secure (WSS), que também usa TLS. A retirada de suporte para o TLS 1.0 e o 1.1 abrange as conexões HTTPS e WSS.

## Quais ações preciso executar para certificar-me de não ser afetado?
{: #impact}

A maioria das conexões feitas para produtos ou serviços {{site.data.keyword.Bluemix_notm}} já usa o TLS 1.2. Se as suas conexões não requererem o TLS 1.0 ou 1.1, você não será afetado.

Se você está usando qualquer um dos produtos de serviços que estão retirando o suporte para o TLS 1.0 ou 1.1, deve-se confirmar se as suas conexões não requerem o TLS 1.0 ou 1.1.

### Cloud Foundry no {{site.data.keyword.Bluemix_notm}}

Para aplicativos Cloud Foundry, é necessário confirmar se as conexões com seu aplicativo de fora do {{site.data.keyword.Bluemix_notm}} não foram afetadas. Confirme também se as conexões de seu aplicativo com outro aplicativo Cloud Foundry no {{site.data.keyword.Bluemix_notm}} não foram afetadas.

Todas as conexões com o Cloud Foundry que usam o TLS são potencialmente afetadas, incluindo quaisquer conexões feitas de navegadores da web. Todos os navegadores modernos suportam o TLS 1.2, incluindo aqueles que são [Pré-requisitos](https://console.bluemix.net/docs/overview/prereqs.html#browsers) do {{site.data.keyword.Bluemix_notm}}.
{: tip}

#### Conectando-se ao seu aplicativo Cloud Foundry

Todos os terminais de aplicativo do Cloud Foundry no domínio `*.mybluemix.net` podem ser acessados por meio de um terminal alternativo que suporta apenas o TLS 1.2.

Para usar o terminal alternativo, inclua `alt.` Após o subdomínio do seu aplicativo. Por exemplo, se o seu aplicativo estiver hospedado em `https://myapplication.mybluemix.net`, use `https://myapplication.alt.mybluemix.net`. Ou, para `https://myapplication.eu-gb.mybluemix.net` use `https://myapplication.alt.eu-gb.mybluemix.net`.

Se você puder se conectar com êxito ao terminal alternativo, é porque não foi afetado.

Se você não puder se conectar com êxito, deverá mudar o seu cliente, as bibliotecas do cliente ou a configuração do cliente para ativar o TLS 1.2.

#### Conectando entre aplicativos Cloud Foundry

Use o comando a seguir para configurar seu aplicativo Cloud Foundry para redirecionamento automaticamente para os terminais alternativos que estão disponíveis no domínio `*.mybluemix.net` ao se conectar a outros aplicativos:
```
cf set-env <application_name> BLUEMIX_TLS10_DISABLED true
```

Depois de configurar `BLUEMIX_TLS10_DISABLED` como `true`, deve-se usar o comando a seguir para remontar seu aplicativo para que essa mudança entre em vigor:
```
cf restage <application_name>
```

Depois de fazer essas mudanças, qualquer solicitação de saída de seu aplicativo será redirecionada somente para os terminais alternativos TLS 1.2.

Para usar os terminais alternativos, o cliente deve suportar a extensão do TLS Server Name Indication (SNI). Caso contrário, o certificado retornado poderá ser considerado inválido por seu cliente e você poderá supor incorretamente que foi afetado pela remoção do TLS 1.0 e 1.1.
{: tip}

### Produtos e serviços Watson

Para produtos e serviços do Watson, faça as substituições a seguir para suas conexões:
  * Substitua ``gateway.watsonplatform.net` com `gateway-tls12.watsonplatform.net`
  * Substitua ``stream.wastonplatform.net` com `stream-tls12.watsonplatform.net`

Esses terminais alternativos suportam apenas o TLS 1.2. Se você puder se conectar com êxito a esses terminais alternativos, é porque não foi afetado. Se você não puder se conectar com êxito, deverá mudar o seu cliente, as bibliotecas do cliente ou a configuração do cliente para ativar o TLS 1.2.

Terminais alternativos para produtos e serviços do Watson em regiões diferentes do sul dos EUA não são fornecidos, pois já suportam apenas o TLS 1.2.

`gatway-tls12.watsonplatform.net` e `stream-tls12.watsonplatform.net` são somente para propósitos de teste e não estarão disponíveis após o TLS 1.0 e o 1.1 serem removidos.
{: tip}

### Outros produtos ou serviços

Para produtos ou serviços que não possuem somente terminais alternativos TLS 1.2 disponíveis, consulte qualquer documentação disponível de seu cliente ou bibliotecas do cliente para obter informações sobre como determinar quais versões do TLS são suportadas e qual versão você está usando.

## Quais produtos e serviços estão retirando o suporte para o TLS 1.0 e 1.1?
{: #prodsandservs}

Os produtos ou serviços a seguir estão retirando o suporte para o TLS 1.0 e 1.1.

Alguns produtos ou serviços, como o Cloud Foundry no {{site.data.keyword.Bluemix_notm}} e os serviços no catálogo do {{site.data.keyword.Bluemix_notm}}, podem ser oferecidos em múltiplas regiões. O TLS 1.0 e o 1.1 serão removidos de todas as regiões em que eles são suportados atualmente.

**Nota importante:** as implementações do {{site.data.keyword.Bluemix_notm}} Private ou {{site.data.keyword.Bluemix_notm}} Local System ou quaisquer serviços do {{site.data.keyword.Bluemix_notm}} hospedados nessas implementações não são incluídos. Se a sua implementação ainda suporta o TLS 1.0 ou 1.1, trabalhe com seu cliente ou representante de suporte para determinar quando a remoção é correta para você.

### Produtos ou serviços disponíveis no catálogo do {{site.data.keyword.Bluemix_notm}}

#### Plataforma de nuvem

* Cloud Foundry no {{site.data.keyword.Bluemix_notm}}
* Infraestrutura do {{site.data.keyword.Bluemix_notm}} (`api.softlayer.com` e `api.service.softlayer.com`)

#### APIs

* API Connect

#### Serviços de Aplicativos

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

* Auto-Scaling
* Alert Notification
* Availability Monitoring
* Entrega contínua
* Continuous Release
* DevOps Insights
* Gerenciamento de eventos
* Globalization Pipeline
* Automated Accessibility Tester\*
* Digital Content Checker\*
* Runbook Automation\*

#### Finança

* Historical Instrument Analytics\*
* Instrument Analytics\*
* Investment Portfolio\*
* Portfolio Optimization\*
* Predictive Market Scenarios\*
* Simulated Historical Instrument Analytics\*
* Simulated Instrument Analytics\*

#### Functions

* Functions

#### Integrar

* App Connect
* Product Insights
* Secure Gateway
* API Harmony\*

#### Internet of Things

* IoT para Eletroeletrônico

#### Dispositivo móvel

* ID do app†
* Mobile Analytics
* Mobile Foundation
* Push Notifications
* App Launch\*

#### Segurança

* ID do app†
* SSL Certificates†

#### Watson

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

Alguns produtos e serviços estão permitindo terminais alternativos que continuam suportando o TLS 1.0 e 1.1 após sua remoção dos terminais primários.

### Infraestrutura do {{site.data.keyword.Bluemix_notm}}

Quando o suporte para o TLS 1.0 e 1.1 for removido de `api.softlayer.com` e `api.service.softlayer.com`, terminais alternativos serão anunciados e disponibilizados por 30 dias.

### Produtos e serviços Watson
{: #watsonprodservices}

Para continuar usando o TLS 1.0 ou 1.1 para se conectar a produtos e serviços do Watson após a retirada do suporte, será possível fazer uma das substituições a seguir:
  * Substitua ``gateway.watsonplatform.net` com `gateway-tls10.wastonplatform.net`
  * Substitua `stream.watsonplatform.net` com `stream-tls10.watsonplatform.net`

Será possível continuar usando `gateway-tls10.watsonplatform.net` e `stream-tls10.watsonplatform.net` para suportar o TLS 1.0, 1.1 e 1.2 depois que essas versões do TLS forem removidas de `gateway.watsonplatform.net` e `stream.watsonplatform.net`.

## Entre em contato
{: #tlssupport}

Se você tiver quaisquer perguntas, preocupações ou problemas, [Entre em contato com o suporte ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/cloud/support){: new_window}
