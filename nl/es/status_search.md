---

copyright:

  years: 2018

lastupdated: "2018-11-13"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}

# Búsqueda avanzada de estado
{: #adv-search}

Puede realizar búsquedas en todos los separadores de la página Estado, pero ¿sabía que puede crear valores de búsqueda de URL utilizando parámetros de consulta desde fuera de la consola?
{:shortdesc}

La lista siguiente incluye ejemplos de opciones de búsqueda de URL:

* Cargue la página con el separador Estado seleccionado: `console.cloud.ibm.com/status?selected=status `
* Cargue la página con el separador Mantenimiento planificado seleccionado: `console.cloud.ibm.com/status?selected=maintenance`
* Cargue la página con el separador Boletín de seguridad seleccionado: `console.cloud.ibm.com/status?selected=security`
* Cargue la página con el separador Anuncios seleccionado: `console.cloud.ibm.com/status?selected=announcement`
* Cargue la página con una consulta de búsqueda especificada: `console.cloud.ibm.com/status?selected=<selected>&query=<query>`
* Acceda a la página con filtros seleccionados. Por ejemplo, puede definir la ubicación geográfica correspondiente a América del Norte con la siguiente búsqueda de URL: `console.cloud.ibm.com/status?selected=status&region=na`

* Utilice identificadores de notificación exclusivos como parámetro de búsqueda para ir directamente a los detalles de la notificación.  Por ejemplo, `query=INC1000001` tiene como destino los elementos con el ID: `INC1000001`. En este ejemplo, `INC1000001` es el número de caso correspondiente a una notificación de mantenimiento.

### Filtros de consultas de URL:

| Parámetro consulta URL | Descripción | Valores |
| ----- | ----- | ----- | ----- |
| `?type` | Un filtro que solo se aplica al separador Estado. Utilice la consulta `?type` para filtrar el separador Estado por incidencias o mantenimiento. | `=incident`, `=maintenance` |
| `?region` | Filtrar la página por ubicación geográfica.  | `=na`, `=eu`, `=sa`, `=ap` |
| `?component` | Filtre la página por componentes de {{site.data.keyword.Bluemix_notm}}. Por ejemplo, puede filtrar por el servicio en el que está interesado. | Se aplica a la mayoría de los ID de catálogo globales; por ejemplo, `?component=iotf-service`
filtra la página y solo mostrará los sucesos que afecten a la plataforma Internet de las cosas  |
{: caption="Tabla 1. Filtros de consultas de URL" caption-side="top"}

Siempre puede utilizar los filtros **Filtrar por** y luego copiar o marcar la consulta de URL que se genera. Los filtros se muestran en el URL y pueden ayudarle a crear consultas futuras.
{: tip}
