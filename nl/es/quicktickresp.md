---

copyright:

  years: 2015, 2018

lastupdated: "2018-03-15"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# ¿Cómo puedo obtener una rápida respuesta a mi incidencia?
{: #quicktickresp}

Cuando se pone en contacto con el soporte y abre una incidencia de soporte, puede solicitar un nivel de gravedad específico, según el tipo y la urgencia del problema. El nivel de gravedad puede estar relacionado con la celeridad con la que se soluciona el problema.
{:shortdesc}

Usted define la gravedad del problema en función de sus requisitos empresariales y de su nivel de soporte. Todas las incidencias se investigan para identificar y resolver la causa raíz del problema. Cuando se necesiten datos de diagnóstico del problema para determinar la causa raíz de un problema, se le solicitará aprobación para acceder a archivos de registro y a otros datos de determinación de problemas desde la aplicación. Sin estos datos es posible que se retrase la resolución del problema.

Si se le pide que proporcione información de diagnóstico, utilice las instrucciones siguientes para recopilar y proporcionar la información solicitada lo antes posible.

## Recopilación de información de diagnóstico
{: #collecting-diagnostic-information}

Para diagnosticar y resolver problemas con los servicios y apps de {{site.data.keyword.Bluemix_notm}}, es posible que el equipo de soporte de {{site.data.keyword.Bluemix_notm}} le solicite que recopile información de diagnóstico.

Antes de recopilar la información de diagnóstico, siga estos pasos:

1. Asegúrese de haber instalado la última interfaz de línea de mandatos cf. Para obtener más información, consulte [Instalación de la interfaz de línea de mandatos cf](/docs/starters/install_cli.html).
>**Nota:** Si no tiene instalada la última interfaz de línea de mandatos cf, después de conectar la línea de mandatos cf a {{site.data.keyword.Bluemix_notm}} el mandato `cf logs` no devuelve información.
2. Asegúrese de haber conectado la interfaz de línea de mandatos cf al lugar en el que se ejecuta {{site.data.keyword.Bluemix_notm}} mediante el mandato `cf api`.

Utilice uno de los scripts siguientes para recopilar información de diagnóstico:

  * Para sistemas operativos Windows, descargue el archivo [bmdiag-general.bat ![icono de enlace externo](../icons/launch-glyph.svg "icono de enlace externo")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} y ejecútelo.
  * Para sistemas operativos Linux, descargue el archivo [bmdiag-general.sh ![icono de enlace externo](../icons/launch-glyph.svg "icono de enlace externo")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} y ejecútelo.

Los scripts utilizan la interfaz de línea de mandatos cf para extraer la siguiente información del entorno de app:
  * Registro de aplicación
  * Metadatos de aplicación
  * Rutas configuradas
  * Sucesos
  * Servicio de suministro

## ¿Puedo escalar una incidencia de soporte?
{: #escalation}

Con el soporte premium o avanzado, si no ha recibido una respuesta a tiempo para una incidencia de soporte, o piensa que la incidencia no se está resolviendo adecuadamente, puede escalarla.  
{:shortdesc}

Consulte [Tipos de soporte](/docs/get-support/getstarttssup.html#typesofsupport) para obtener más información sobre el soporte premium y avanzado.

Gracias al proceso de escalada de incidencias de soporte, los gestores de IBM revisan sus preocupaciones y trabajan
conjuntamente con usted para mejorar su experiencia de soporte.

Para enviar una solicitud de escalado, realice los pasos siguientes:
  1. Abra una nueva incidencia de soporte con el resumen **Solicitud de escalado**.
  2. Para asegurarse de que su solicitud de escalada se puedan asociar a la incidencia de soporte original, incluya la información siguiente en el cuerpo de la incidencia:
      * El número de incidencia de su incidencia de soporte abierta que necesita ser escalada.
      * Un breve resumen de los motivos por las que hace falta escalar.

## Horas de operación
{: #support-hours-operation}

Los problemas de gravedad 1 se supervisan 24 horas al día, 7 días por semana. Los envíos de formularios para problemas con todos los demás niveles de gravedad se supervisan entre el domingo a las 21:30 UTC y el viernes a las 23:59 UTC (excluyendo los días festivos).

Para obtener ayuda para convertir este horario de soporte a su huso horario, consulte [Timeanddate.com ![icono de enlace externo](../icons/launch-glyph.svg "icono de enlace externo")](https://www.timeanddate.com). Para obtener más información sobre planificación de vacaciones, consulte [{{site.data.keyword.Bluemix_notm}} Support Holidays ![icono de enlace externo](../icons/launch-glyph.svg "icono de enlace externo")](http://ibm.biz/bluemixholidays).
