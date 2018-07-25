---

copyright:

  years: 2015, 2018

lastupdated: "2018-05-22"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Visualización de estados y notificaciones de {{site.data.keyword.Bluemix_notm}}
{: #viewing-bluemix-status}

La página Estado es el recurso central para buscar notificaciones y anuncios sobre sucesos clave que afectan a la plataforma {{site.data.keyword.Bluemix_notm}} y a los servicios principales.
{:shortdesc}

En la página Estado hay disponible la información siguiente:

  * El estado actual de los servicios y componentes en todas las regiones de {{site.data.keyword.Bluemix_notm}} Foundry Service.
  * Una lista de anuncios, en orden cronológico, sobre mantenimiento e incidencias. Puede filtrar la lista o abrir un anuncio concreto para obtener más información.
  * Ventana de mantenimiento planificado para las que se proporciona notificación previa, excepto en circunstancias extremas.
  * Incidencias o paradas no planificadas, que se publican en cuanto las conoce el equipo de {{site.data.keyword.Bluemix_notm}}. Las notificaciones de incidencias se actualizan con regularidad hasta que quedan resueltas.
  * Referencias a boletines de seguridad que afectan a diversos servicios de {{site.data.keyword.Bluemix_notm}} o la plataforma.
  * Otros anuncios sobre la plataforma en general que puedan ser de su interés.
  * [Un canal de información RSS al que se puede suscribir.](#subscribing-rss-feed).

Para ver la página Estado, seleccione una de las dos opciones siguientes:

  * Inicie sesión en la consola de {{site.data.keyword.Bluemix_notm}}. En la barra de menús, pulse **Soporte** y seleccione **Estado**. Compruebe la lista de recursos en busca del icono ![algunos problemas](images/some_issues.svg). Este icono podría indicar una parada.
  * Acceda directamente en [{{site.data.keyword.Bluemix_notm}} - Estado ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://console.bluemix.net/status){: new_window}.


## Prácticas recomendadas para supervisar el estado
{: #best-practices}

Utilice las siguientes prácticas recomendadas para la supervisión del estado de {{site.data.keyword.Bluemix_notm}} para permanecer informado y planear en consecuencia.

### Comprobar los próximos períodos de mantenimiento
{: #monbp-checmaintwin}

Compruebe los próximos períodos de mantenimiento publicados en la página de estado al menos una vez cada 24 horas, mediante una de las opciones siguientes:
* Navegando directamente a la página [Estado ![icono de enlace externo](../icons/launch-glyph.svg "icono de enlace externo")](https://console.bluemix.net/status){: new_window}
* Usando el hilo de RSS o un reenviador de RSS a correo electrónico

### Comprobar los períodos de mantenimiento actuales o una incidencia en curso
{: #monbp-checcurmaninprog}

Si cree que {{site.data.keyword.Bluemix_notm}} no funciona según lo previsto, compruebe la página de estado de los períodos actuales de mantenimiento y las incidencias en curso. Para informar de una incidencia que no aparece en la página de estado, abra una incidencia de soporte a través del elemento de menú **Soporte** y seleccione **Añadir incidencia** en la barra de menús o acceda la página de ayuda del [Soporte de {{site.data.keyword.Bluemix_notm}}![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://www.ibm.biz/bluemixsupport){: new_window}.

### Aprovechar varias regiones de {{site.data.keyword.Bluemix_notm}} Foundry Service
{: #monbp-multpreg}

Todos los usuarios de {{site.data.keyword.Bluemix_notm}} Public tienen acceso automáticamente a las regiones US-SOUTH, US-EAST, EU-GB, EU-DE y AU-SYD. El equipo {{site.data.keyword.Bluemix_notm}} Global Operations gestiona todas las regiones para evitar que les afecte el mantenimiento y minimizar el riesgo de incidencias que afecten a todas las regiones al mismo tiempo.

Para cambiar entre regiones, desde la barra de menús de {{site.data.keyword.Bluemix_notm}}, amplíe el menú de región y, a continuación, seleccione otra región.

### Preparar para interrupciones menores
{: #monbp-prepmininter}

En la mayoría de los casos, se puede seguir utilizando {{site.data.keyword.Bluemix_notm}} con normalidad, incluso durante los períodos de mantenimiento. Sin embargo, no siempre se pueden evitar las interrupciones menores del servicio. La ejecución de aplicaciones suele seguir disponible aunque se interrumpan temporalmente las funciones de gestión de aplicaciones de {{site.data.keyword.Bluemix_notm}}, como iniciar y detener apps. Para maximizar la disponibilidad de las aplicaciones en ejecución, ejecute al menos tres instancias de cada aplicación.

## Suscripción a un hilo RSS
{: #subscribing-rss-feed}

Recibirá alertas de notificaciones suscribiéndose al hilo RSS de la página Estado de {{site.data.keyword.Bluemix_notm}}. Este enfoque proporciona una forma de recibir las actualizaciones sin tener que consultar la página de estado.

Para suscribirse, siga estos pasos:

1. Descargue e instale un lector de RSS.
2. Utilice el lector para suscribirse al hilo de una de las formas siguientes:
    * Arrastre el icono ![RSS](images/rss.svg) al lector de RSS.
    * Pulse con el botón derecho en el icono de RSS, seleccione **Copiar dirección del enlace** y pegue el URL
en el lector de RSS.

Para obtener más información, consulte la sección **Ayuda** del lector. 	   

Hay otros métodos de lectura de canales de información RSS disponibles a través de plug-ins del navegador web como los siguientes:
  * [Lector de canales de información RSS ![icono de enlace externo](../icons/launch-glyph.svg "icono de enlace externo")](http://feeder.co/){: new_window} para Chrome
  * [Complemento Brief ![icono de enlace externo](../icons/launch-glyph.svg "icono de enlace externo")](https://addons.mozilla.org/en-US/firefox/addon/brief/){: new_window} para Firefox

Fuentes de noticias como los siguientes también proporcionan métodos para leer canales de información RSS:
  * [Feedly ![icono de enlace externo](../icons/launch-glyph.svg "icono de enlace externo")](http://www.feedly.com/){: new_window}
  * [G2reader ![icono de enlace externo](../icons/launch-glyph.svg "icono de enlace externo")](http://www.g2reader.com/en/){: new_window}

También puede utilizar un servicio de terceros para enviar cada actualización de RSS por correo electrónico automáticamente. En la lista
siguiente se proporcionan algunos ejemplos de servicios de terceros:

  * www.feedmyinbox.com
  * www.rssforward.com
  * www.feedrabbit.com
  * www.mailchimp.com
  * www.feedmailer.com
  * www.iftt.com

{{site.data.keyword.Bluemix_notm}} suele tener unas 50 actualizaciones por mes.


## Configuración de notificaciones de correo electrónico de incidencias y mantenimiento
{: #setting-up-notifications}

Para {{site.data.keyword.Bluemix_notm}} público, puede registrarse para las notificaciones de plataforma. Las notificaciones de plataforma son alertas por correo electrónico para sucesos de mantenimiento e incidencias para la plataforma
{{site.data.keyword.Bluemix_notm}}. Puede elegir entre recibir estas notificaciones a través de correo electrónico pulsando **Gestionar** > **Cuenta** > **Notificaciones** y seleccionando el separador **Plataforma**. Para obtener más información sobre el establecimiento de notificaciones de cuenta, consulte [Configuración de notificaciones](/docs/account/notifications.html#setting-notifications).
