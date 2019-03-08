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

# Retirada de soporte para TLS 1.0 y 1.1
{: #tlssupportwithdraw}

IBM retira el soporte para TLS 1.0 y TLS 1.1 en muchos productos y servicios de nube el 1 de marzo de 2018. TLS 1.2 tiene soporte para cualquier producto o servicio de {{site.data.keyword.Bluemix}} en el que se retire el soporte para TLS 1.0 y 1.1.
{:shortdesc}

## ¿Por qué está cambiando el soporte de la versión de TLS?
{: #why}

El cambio del soporte de la versión de TLS proporciona un entorno de nube que es seguro y acorde con las mejores prácticas del sector para la seguridad y la privacidad de los datos.

## ¿Qué es TLS?
{: #what}

El [protocolo TLS ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://en.wikipedia.org/wiki/Transport_Layer_Security){: new_window} se utiliza para cifrar las comunicaciones en una red para garantizar que los datos transmitidos sean privados. TLS publicó las siguientes versiones: 1.0, 1.1 y 1.2. Todas las conexiones HTTPS utilizan TLS. HTTPS es el método predominante para garantizar que las conexiones a los productos y servicios de {{site.data.keyword.Bluemix_notm}} son fiables y seguras. Algunos productos y servicios de {{site.data.keyword.Bluemix_notm}} permiten conexiones seguras mediante el protocolo WebSocket Secure (WSS), que también utiliza TLS. La retirada de soporte para TLS 1.0 y 1.1 abarca las conexiones HTTPS y WSS.

## ¿Qué medidas debo tomar para asegurarme de que no me afecte?
{: #impact}

La mayoría de las conexiones realizadas a productos y servicios de {{site.data.keyword.Bluemix_notm}} ya utilizan TLS 1.2. Si sus conexiones no requieren TLS 1.0 o 1.1, no se verá afectado.

Si utiliza cualquiera de los productos o servicios en los que se va a retirar el soporte para TLS 1.0 o 1.1, debe confirmar que sus conexiones no requieren TLS 1.0 o 1.1.

### Cloud Foundry en {{site.data.keyword.Bluemix_notm}}
{: #cf}

Para las aplicaciones de Cloud Foundry, debe confirmar que sus conexiones a la aplicación desde fuera de {{site.data.keyword.Bluemix_notm}} no se verán afectadas. Confirme también que las conexiones desde la aplicación a otra aplicación de Cloud Foundry en {{site.data.keyword.Bluemix_notm}} no se verán afectadas.

Todas las conexiones a Cloud Foundry que utilicen TLS se pueden ver afectadas, incluidas las conexiones realizadas desde los navegadores web. Todos los navegadores modernos admiten TLS 1.2, incluidos los navegadores que son [Requisitos previos](/docs/overview?topic=overview-browsers-platform#browsers) de {{site.data.keyword.Bluemix_notm}}.
{: tip}

#### Conexión a la aplicación de Cloud Foundry
{: #connect-cf}
Se puede acceder a todos los puntos finales de aplicación de Cloud Foundry del dominio `*.app.domain.cloud` mediante un punto final alternativo que solo admite TLS 1.2.

Para utilizar el punto final alternativo, añada `alt.` después del subdominio de la aplicación. Por ejemplo, si la aplicación está alojada en `https://myapplication.app.domain.cloud`, utilice `https://myapplication.alt.app.domain.cloud`. O, para `https://myapplication.eu-gb.app.domain.cloud`, utilice `https://myapplication.alt.eu-gb.app.domain.cloud`.

Si puede conectar correctamente con el punto final alternativo, significa que no se ve afectado.

Si no se puede conectar correctamente, debe cambiar el cliente, las bibliotecas de cliente o la configuración de cliente para habilitar TLS 1.2.

#### Conexión entre aplicaciones de Cloud Foundry
{: #connect2}

Utilice el mandato siguiente para configurar la aplicación de Cloud Foundry para redirigir automáticamente a los puntos finales alternativos disponibles en el dominio `*.app.domain.cloud` al conectarse a otras aplicaciones:
```
cf set-env <application_name> BLUEMIX_TLS10_DISABLED true
```

Después de establecer `BLUEMIX_TLS10_DISABLED` en `true`, debe utilizar el mandato siguiente para volver a transferir su aplicación para que se aplique este cambio:
```
cf restage <application_name>
```

Tras realizar estos cambios, las solicitudes salientes de su aplicación se redirigirán solo a los puntos finales alternativos de TLS 1.2.

Para utilizar los puntos finales alternativos, el cliente debe ser compatible con la extensión de TLS Server Name Indication (SNI). Si no lo es, puede que el cliente considere no válido el certificado devuelto y puede que presuponga incorrectamente que le afecta la retirada de TLS 1.0 y 1.1.
{: tip}

### Productos y servicios de Watson
{: #watson-serv}

Para productos y servicios de Watson, realice las siguientes sustituciones a sus conexiones:
  * Sustituya `gateway.watsonplatform.net` por `gateway-tls12.watsonplatform.net`
  * Sustituya `stream.wastonplatform.net` por `stream-tls12.watsonplatform.net`

Estos puntos finales alternativos solo admiten TLS 1.2. Si puede conectar correctamente con estos puntos finales alternativos, no se ve afectado. Si no se puede conectar correctamente, debe cambiar el cliente, las bibliotecas de cliente o la configuración de cliente para habilitar TLS 1.2.

No se proporcionan puntos finales alternativos para productos y servicios de Watson en otras ubicaciones que no sean Dallas, ya que estas ya admiten solo TLS 1.2.

`gatway-tls12.watsonplatform.net` y `stream-tls12.watsonplatform.net` son solo para pruebas y no estarán disponibles tras la retirada de TLS 1.0 y 1.1.
{: tip}

### Otros productos o servicios
{: #other-serv}

Para productos o servicios que no tienen puntos finales alternativos de solo TLS 1.2 disponibles, consulte la documentación disponible para el cliente. Para obtener información sobre cómo determinar qué versiones de TLS están soportadas y qué versión está utilizando, consulte las bibliotecas de cliente. 

## ¿Qué productos y servicios van a retirar el soporte para TLS 1.0 y 1.1?
{: #prodsandservs}

Los siguientes productos o servicios van a retirar el soporte para TLS 1.0 y 1.1.

Algunos productos o servicios, como por ejemplo Cloud Foundry en {{site.data.keyword.Bluemix_notm}} y servicios del catálogo de {{site.data.keyword.Bluemix_notm}}, pueden ofrecerse en varias ubicaciones. TLS 1.0 y 1.1 se han eliminado en todas las ubicaciones en las que reciben soporte actualmente.

No se incluyen los despliegues de {{site.data.keyword.Bluemix_notm}} Private o {{site.data.keyword.Bluemix_notm}} Local System, ni ningún servicio de {{site.data.keyword.Bluemix_notm}} alojado en estos despliegues. Si su despliegue todavía admite TLS 1.0 o 1.1, valore con su representante de soporte o cliente el momento adecuado de la retirada. 
{: note}

### Productos o servicios disponibles en el catálogo de {{site.data.keyword.Bluemix_notm}}
{: #available}

#### Plataforma de nube

* Cloud Foundry en {{site.data.keyword.Bluemix_notm}}
* Infraestructura de {{site.data.keyword.Bluemix_notm}} (`api.softlayer.com` y `api.service.softlayer.com`)

#### API
{: #apis}

* API Connect

#### Servicios de aplicación
{: #app-serv}

* Business Rules
* Message Hub
* Voice Agent with Watson\*
* Watson Content Knowledge Kits\*

#### Datos y análisis

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

#### Finanzas
{: #finance}

* Historical Instrument Analytics\*
* Instrument Analytics\*
* Investment Portfolio\*
* Portfolio Optimization\*
* Predictive Market Scenarios\*
* Simulated Historical Instrument Analytics\*
* Simulated Instrument Analytics\*

#### Funciones
{: #function}

* Funciones

#### Integrar
{: #integrate}

* App Connect
* Product Insights
* Secure Gateway
* API Harmony\*

#### Internet de las cosas
{: #iot}

* IoT for Electronics

#### Móvil
{: #mobile}

* App ID†
* Mobile Analytics
* Mobile Foundation
* Push Notifications
* App Launch\*

#### Seguridad
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

\*Disponible en servicios experimentales en el catálogo de {{site.data.keyword.Bluemix_notm}}.  
† TLS 1.0 fue eliminado anteriormente; solo se va a eliminar TLS 1.1.  
‡ En desuso, solo disponible para clientes actuales.

### Productos o servicios disponibles a través de IBM Marketplace
{: #marketplace}

* Forms Experience Builder on Cloud
* IoT for Insurance
* Watson Customer Insight for Insurance
* Watson Marketing Insights
* Watson Knowledge Studio
* Watson Virtual Agent
* Weather Company Energy Trader

### Otros productos o servicios
{: #prodservices}

* Teacher Advisor with Watson

## ¿Qué pasa si mi producto o servicio no está en la lista?
{: #tlsprodnotlisted}

Puede que su producto o servicio ya admita solo TLS 1.2, o puede que no se vaya a eliminar TLS 1.0 ni 1.1 ahora. Puede utilizar varias herramientas de cliente y en línea disponibles para comprobar si TLS 1.0 y 1.1 están soportados por los puntos finales de un producto o servicio.

## ¿Hay alguna forma de poder seguir utilizando TLS 1.0 o 1.1 una vez retirado el soporte?
{: #tlskeepusing}

Algunos productos y servicios están habilitando puntos finales alternativos que siguen soportando TLS 1.0 y 1.1 después de que se eliminen de los puntos finales principales.

### Infraestructura de {{site.data.keyword.Bluemix_notm}}
{: #infrastructure}

Cuando se elimine el soporte para TLS 1.0 y 1.1 de `api.softlayer.com` y `api.service.softlayer.com`, se anunciarán puntos finales alternativos y estarán disponibles durante 30 días.

### Productos y servicios de Watson
{: #watsonprodservices}

Para seguir utilizando TLS 1.0 o 1.1 para conectarse a productos y servicios de Watson una vez que se haya retirado el soporte, puede realizar una de las sustituciones siguientes:
  * Sustituya `gateway.watsonplatform.net` por `gateway-tls10.wastonplatform.net`
  * Sustituya `stream.watsonplatform.net` por `stream-tls10.watsonplatform.net`

Puede seguir utilizando `gateway-tls10.watsonplatform.net` y `stream-tls10.watsonplatform.net` para dar soporte a TLS 1.0 y 1.1 una vez que estas versiones de TLS se eliminen de `gateway.watsonplatform.net` y `stream.watsonplatform.net`.

## Póngase en contacto
{: #tlssupport}

Si tiene alguna pregunta, duda o problema, [Póngase en contacto con el equipo de soporte de ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.ibm.com/cloud/support){: new_window}
