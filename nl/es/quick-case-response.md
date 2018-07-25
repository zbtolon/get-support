---

copyright:

  years: 2015, 2018

lastupdated: "2018-05-14"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# ¿Cómo puedo obtener una respuesta rápida a mi caso?
{: #quicktickresp}

Cuando se pone en contacto con el soporte y abre un caso de soporte, puede solicitar un nivel de gravedad específico, según el tipo y la urgencia del problema. El nivel de gravedad puede estar relacionado con la celeridad con la que se soluciona el problema.
{:shortdesc}

Usted define la gravedad del problema en función de sus requisitos empresariales y de su nivel de soporte. Consulte [planes de soporte](/docs/get-support/index.html) para obtener más información sobre los niveles de planes de apoyo. Todos los casos se investigan para identificar y resolver la causa raíz del problema. Cuando se necesiten datos de diagnóstico del problema para determinar la causa raíz de un problema, se le solicita aprobación para acceder a archivos de registro y a otros datos de determinación de problemas desde la aplicación. Sin estos datos es posible que se retrase la resolución del problema.

## Recopilación de información de diagnóstico
{: #collecting-diagnostic-information}

Para diagnosticar y resolver problemas con los servicios y aplicaciones de {{site.data.keyword.Bluemix_notm}}, es posible que el equipo de soporte de {{site.data.keyword.Bluemix_notm}} le solicite que recopile información de diagnóstico. Utilice las instrucciones siguientes para recopilar y proporcionar la información solicitada lo antes posible.

Antes de recopilar la información de diagnóstico, siga estos pasos:

1. Asegúrese de haber instalado la última interfaz de línea de mandatos Cloud Foundry. Para obtener más información, consulte [Instalación de la interfaz de línea de mandatos de Cloud Foundry](/docs/starters/install_cli.html).
>**Nota:** Si no tiene instalada la última interfaz de línea de mandatos Cloud Foundry, después de conectar la línea de mandatos cf a {{site.data.keyword.Bluemix_notm}} el mandato `cf logs` no devuelve información.
2. Asegúrese de haber conectado la interfaz de línea de mandatos de Cloud Foundry al lugar en el que se ejecuta {{site.data.keyword.Bluemix_notm}} mediante el mandato `cf api`.

Utilice uno de los scripts siguientes para recopilar información de diagnóstico:

  * Para sistemas operativos Windows, descargue el archivo [bmdiag-general.bat ![icono de enlace externo](../icons/launch-glyph.svg "icono de enlace externo")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} y ejecútelo.
  * Para sistemas operativos Linux, descargue el archivo [bmdiag-general.sh ![icono de enlace externo](../icons/launch-glyph.svg "icono de enlace externo")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} y ejecútelo.

Los scripts utilizan la interfaz de línea de mandatos de Cloud Foundry para extraer la siguiente información del entorno de aplicación:
  * Registro de aplicación
  * Metadatos de aplicación
  * Rutas configuradas
  * Sucesos
  * Servicio de suministro

## Escalamiento de casos de soporte
{: #escalation}

Como cliente de {{site.data.keyword.Bluemix_notm}}, puede solicitar asistencia adicional escalando su caso al gestor de soporte de {{site.data.keyword.Bluemix_notm}} en servicio. El proceso de escalamiento le permite emerger problemas críticos y expresar sus inquietudes cuando crea que su caso de soporte no se está resolviendo como es debido. Una vez que se haya escalado un caso, el gestor en servicio registra la información del caso de soporte, interactúa con los miembros adecuados del equipo técnico de soporte de {{site.data.keyword.Bluemix_notm}} y le proporciona las actualizaciones adecuadas.

Para escalar un caso de soporte, debe tener soporte avanzado o premium de {{site.data.keyword.Bluemix_notm}} y debe haber abierto un caso de soporte para el problema. Asimismo, asegúrese de que el problema técnico está bien documentado en el caso de soporte que haya abierto.

 Para escalar un caso, complete los pasos siguientes:

  1. Póngase en contacto con el equipo de soporte de {{site.data.keyword.Bluemix_notm}} por teléfono o a través del chat.:
    * Si lo hace por teléfono, marque el número siguiente: 866-403-7638.
    * Si lo hace mediante el chat, desde el {{site.data.keyword.Bluemix_notm}} [Centro de soporte ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://console.bluemix.net/unifiedsupport/supportcenter){: new_window} o, si dispone de una cuenta de SoftLayer que no esté enlazada, desde el [portal de clientes ![Icono de enlace externo](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window}.
  2. Proporcione el número de caso existente y solicite escalar el caso.
  3. Proporcione la justificación del escalamiento y el impacto empresarial de su caso.

Los gestores de soporte de {{site.data.keyword.Bluemix_notm}} están en servicio y disponibles las 24 horas del día, todos los días de la semana. Los gestores en servicio utilizan los recursos adecuados para enfocar su caso y le informan sobre las acciones que se han realizado.
