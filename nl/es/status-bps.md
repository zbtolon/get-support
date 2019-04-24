---

copyright:

  years: 2015, 2018

lastupdated: "2019-02-18"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Prácticas recomendadas para supervisar el estado
{: #best-practices}

Para mantenerse informado y planificar en consecuencia, utilice las siguientes prácticas recomendadas para la supervisión del estado de {{site.data.keyword.Bluemix}}.
{: shortdesc}

## Comprobar los próximos períodos de mantenimiento
{: #monbp-checmaintwin}

Compruebe los próximos períodos de mantenimiento publicados en la página del panel de control de la consola de {{site.data.keyword.Bluemix_notm}} al menos una vez cada 24 horas, mediante una de las opciones siguientes:
* Consulte el widget de mantenimiento planificado en el [Panel de control ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com){: new_window}. Pulse **Todos los sucesos** para ver todos los mantenimientos planificados.
* Vaya directamente a la página [Estado - Mantenimiento planificado ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/status?selected=maintenance){: new_window}

## Comprobar los períodos de mantenimiento actuales o una incidencia en curso
{: #monbp-checcurmaninprog}

Si cree que {{site.data.keyword.Bluemix_notm}} no funciona según lo previsto, compruebe la página de estado de los períodos actuales de mantenimiento y las incidencias en curso. Para notificar un incidente que no aparezca en la lista de la página Estado, abra un caso de soporte pulsando **Soporte** en la barra de menús. Luego pulse **Crear caso nuevo** en el separador Obtener soporte.

## Aprovechar las diversas ubicaciones de {{site.data.keyword.Bluemix_notm}}
{: #monbp-multpreg}

Todos los usuarios de {{site.data.keyword.Bluemix_notm}} tienen automáticamente acceso a las ubicaciones Dallas, Londres, Frankfurt, Sídney, Washington DC y Tokio. El equipo {{site.data.keyword.Bluemix_notm}} Global Operations gestiona todas las ubicaciones para evitar que les afecte el mantenimiento y minimizar el riesgo de incidencias que afecten a todas las ubicaciones al mismo tiempo.

Para cambiar de ubicación, vaya al panel de control y expanda el menú **UBICACIÓN**.

## Preparar para interrupciones menores
{: #monbp-prepmininter}

En la mayoría de los casos, se puede seguir utilizando {{site.data.keyword.Bluemix_notm}} con normalidad, incluso durante los períodos de mantenimiento. Sin embargo, no siempre se pueden evitar las interrupciones menores del servicio. La ejecución de aplicaciones suele seguir disponible aunque se interrumpan temporalmente las funciones de gestión de aplicaciones de {{site.data.keyword.Bluemix_notm}}, como iniciar y detener apps. Para maximizar la disponibilidad de las aplicaciones en ejecución, ejecute al menos tres instancias de cada aplicación.

## Suscripción a notificaciones por correo electrónico
{: #monbp-subscribing}

Si es el propietario de una cuenta Lite, puede seleccionar si desea recibir notificaciones de correo electrónico sobre sucesos no planificados de la plataforma {{site.data.keyword.Bluemix_notm}}, como paradas, y sobre sucesos planificados, como los de mantenimiento. Además, si tiene una cuenta de Pago según uso o de Suscripción, puede elegir si desea recibir notificaciones por correo electrónico relacionados con la infraestructura de {{site.data.keyword.Bluemix_notm}} sobre sucesos no planificados, mantenimiento y anuncios. Para obtener más información, consulte [Establecimiento de preferencias de correo electrónico](/docs/account?topic=account-account_setup#account_setup).



