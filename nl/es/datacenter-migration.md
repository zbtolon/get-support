---

copyright:

  years: 1994, 2019

lastupdated: "2019-01-30"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Retirada de soporte para algunos centros de datos de EE.UU.
{: #dc-migrate}

IBM está retirando el soporte para los siguientes centros de datos de los Estados Unidos: 

* dal01 pods 2 y 3
* wdc01 pods 1 y 2
{:shortdesc}

##  ¿Por qué tengo que trasladarme a otro centro de datos?
{: #required-data}

Para seguir ofreciendo el mejor servicio, hardware y conectividad, evaluamos continuamente todos nuestros sitios para asegurarnos de que cumplen con los estándares de red, eléctricos y otros estándares de infraestructura. A pesar de que estos sitios son adecuados, ya no cumplen con nuestros estándares actuales.

## ¿Tengo que haber finalizado la migración por completo en la fecha que aparece en la lista?
{: #data-list}

Sí. Para garantizar que no sufra ninguna interrupción en el servicio, estamos intentando dejar el máximo tiempo posible para facilitarle la transición lo máximo posible. Comunicamos este traslado de sitio en mayo de 2018.

## ¿Tendré que volver a trasladarme a otro centro de datos en el futuro?
{: #move-data}

Evaluamos constantemente la calidad de nuestros sitios para ofrecerle el servicio mejor y más fiable. Es posible que tengamos otros movimientos a medida que evaluamos algunos de los sitios más antiguos.

## ¿Puedo elegir cualquier centro de datos de {{site.data.keyword.Bluemix_notm}} EE.UU.?
{: #us-data}

Sí, puede elegir el sitio de IBM de EE.UU. que mejor se ajuste sus requisitos de ubicación.

## ¿Cómo puedo elegir el centro de datos en el que realizar el despliegue?
{: #deploy-data}

IBM tiene más de 60 centros de datos en ubicaciones de todo el mundo. Consulte el mapa de centros de datos en nuestra página de centros de datos globales para los centros de datos en los que puede realizar el despliegue. 

Tenga en cuenta los siguientes factores cuando seleccione el centro de datos:
* Proximidad a los usuarios de los sistemas
* Proximidad a cualquier otro sistema con el que se tenga que comunicar este servidor
* Políticas o regulaciones de datos que requieran que los datos se almacenen en una ubicación específica

## ¿También estoy obligado a utilizar sitios de EE.UU. para el periodo de transición?
{: #transition}

Puede utilizar cualquier sitio de {{site.data.keyword.cloud_notm}} del mundo durante el periodo de transición, que dura un máximo de 60 días.

## ¿Los dos meses gratuitos de recursos en periodo de transición se suman a mi tiempo de servidor existente?
{: #free}

Sí. Póngase en contacto con nosotros y un representante de soporte le puede ayudar en el proceso de adquirir sus servidores en periodo de transición.

## ¿Cómo puedo determinar mi configuración de hardware actual?
{: #current-hardware}

Inicie una sesión en el portal de clientes. En la **Lista de dispositivos**, seleccione el servidor en el que está interesado y busque los detalles de configuración del sistema. Desde allí, puede ver el tipo de procesador, por ejemplo, Single Intel Xeon E3-1270 (4 núcleos, 3,50 GHz). También puede ver la cantidad de memoria (RAM), el almacenamiento y otros datos.

## ¿Cómo puedo determinar la utilización de mi hardware actual?
{: #utilization} 

La mayoría de los sistemas operativos proporcionan herramientas que puede utilizar para comprender la utilización de su sistema, por ejemplo vmstat e iostat en Linux o Windows System Performance Monitor. Es posible que también disponga de otras herramientas de supervisión del rendimiento. La supervisión y el ajuste del rendimiento es algo en lo que puede invertir un tiempo y esfuerzo considerables. En general, tiene que comprender si hay recursos específicos dentro del sistema (procesador, memoria, disco, red) que estén sobreutilizados o que no se utilicen como se debería. Esta información le puede ayudar a calcular mejor el tamaño de su nuevo sistema. Por ejemplo, un sistema en el que se suele agotar la capacidad de memoria probablemente se beneficiará de un tamaño de memoria mayor en el sistema de destino al que migre.

## ¿Cómo se compara el procesador antiguo con el nuevo?
{: #old-new}

Para comparar las especificaciones de los procesadores Intel antiguos y nuevos, vaya a [https://ark.intel.com/#@Processors](https://ark.intel.com/#@Processors){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo"). Si conoce el tipo de procesador, puede navegar por los menús. Si no, puede utilizar la opción de búsqueda para localizar las especificaciones de los dos procesadores. Los procesadores nuevos tienden a tener más núcleos de procesador y suelen ejecutarse a velocidades de reloj más lentas que las variantes antiguas. Si tiene una carga de trabajo limitada por el procesador (su rendimiento está limitado por la velocidad del procesador), le aconsejamos que elija un procesador con menos núcleos y una velocidad de reloj más alta.  Si ejecuta muchas cargas de trabajo que no están especialmente restringidas por la velocidad del procesador, la elección de un procesador con más núcleos y una velocidad de reloj similar o más lenta podría resultar la mejor opción.

## ¿Cómo elijo mi nuevo sistema operativo?
{: #operating-system}

Si el servidor se ha utilizado durante muchos años y no se mantiene actualizado, es probable que esté ejecutando una versión más antigua del sistema operativo. Esto puede presentar desafíos con la migración. Es posible que no tenga el soporte de instalación para el sistema operativo antiguo desde el que se va a instalar.  También es posible que se encuentre con que el hardware de servidor nuevo al que va a migrar no reciba soporte de la versión del sistema operativo antiguo. Es posible que tenga que elegir otro sistema operativo al que migrar.

La selección del sistema operativo puede venir impuesta por las aplicaciones que ejecute. Como parte de la migración, es posible que tenga que ejecutar la aplicación en una versión posterior del sistema operativo. Asegúrese de que esto funciona en la versión nueva.

Los conocimientos de los que dispone sobre un determinado sistema operativo también pueden afectar a su selección. Si tiene el código fuente de la aplicación, asegúrese de disponer en la nueva plataforma de las herramientas de desarrollo y de las funciones de sistema operativo o de middleware necesarias.  En general, los sistemas de tipo Linux suelen dar mejor soporte a aplicaciones antiguas en versiones nuevas del sistema operativo que Windows, pero no hay ninguna garantía.

## ¿Qué ancho de banda recibiré con mi nueva configuración y es la tasa la misma que la que tengo ahora?
{: #bandwidth}

Recibirá un paquete de ancho de banda estrechamente relacionado con el paquete que tiene ahora. La tasa correspondiente al paquete será la que incluya su paquete o tasa actual.

## ¿Cómo puedo copiar datos de mi servidor antiguo en el nuevo?
{: #old-server}

Después de establecer la conectividad entre el servidor antiguo y el nuevo, debe pensar cómo moverá los datos entre los mismos.  Suponiendo que tiene almacenamiento suficiente en el nuevo servidor para acomodar el volumen de datos, una copia directa de servidor a servidor es la forma más sencilla de conseguirlo.  Existen varias herramientas que puede utilizar.  

* scp es una buena opción para copiar de forma segura un archivo del origen en el destino.  Realiza una copia lineal sin formato. 
* Si tiene que copiar un gran número de archivos, rsync sobre ssh es mucho más rápido que scp. rsync también copia las estructuras de directorios y conserva los permisos de los archivos.

En general, solo debe copiar aplicaciones y datos de aplicaciones entre los sistemas. El hecho de copiar versiones antiguas de archivos del sistema operativo en una versión más nueva puede ocasionar problemas.

Cierre las bases de datos antes de copiarlas entre los sistemas para asegurarse de que los datos son coherentes. Cuando migre datos de bases de datos, asegúrese de que los datos se migren de modo que no limiten sus opciones para importarlos en el nuevo sistema. En lugar de copiar datos de bases de datos de un sistema en otro, tenga en cuenta la posibilidad de exportarlos a un formato que le permita importarlos en una base de datos más nueva. Los archivos de texto sin formato, los archivos CSV, etc. proporcionan más opciones que el uso de formatos de archivo propietario o cerrado cuando se trata de mover datos entre sistemas. Pruebe siempre los métodos de migración de datos en un pequeño conjunto de datos de prueba antes de realizar la copia oficial.

## ¿Tengo que volver a configurar mi red en el nuevo sitio?
{: #networking}

Lo más probable es que su red tenga que cambiar para trabajar con los nuevos servidores y el nuevo sitio.  Si necesita ayuda con este proceso, póngase en contacto con el equipo de soporte técnico por teléfono o chat.

## ¿Qué debo hacer si no tengo los conocimientos necesarios para realizar la migración?
{: #migrate-skills}

La migración de aplicaciones puede resultar una tarea compleja. Uno de los requisitos es disponer de los conocimientos necesarios para hacerlo. Si es necesario realizar cambios de código en la aplicación, asegúrese de tener los conocimientos de programación necesarios. Este es particularmente importante en el caso de sistemas más antiguos en que los conocimientos pueden quedarse cortos o cuando no hay suficiente documentación o conocimientos sobre el propio sistema. Si esto supone un esfuerzo significativo y el sistema resulta esencial para el negocio, baraje la posibilidad de invertir en servicios de pago o en otros servicios de migración que le puedan ayudar.

## ¿Cómo puedo obtener ayuda general con la migración?
{: #gen-migration}

Dependiendo del nivel de ayuda que necesite, puede ponerse en contacto con el equipo de soporte técnico por teléfono o chat. También puede ponerse en contacto con nuestro equipo de servicios gestionados para obtener ayuda.

## ¿Con quién puedo contactar si no tengo un gestor de cuentas?
{: #account-contact}

Puede ponerse en contacto con el servicio de soporte técnico por teléfono o chat para plantear cualquier pregunta que tenga sobre la migración.
