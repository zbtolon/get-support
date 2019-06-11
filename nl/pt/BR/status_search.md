---

copyright:

  years: 2018,2019

lastupdated: "2019-06-05"

keywords: status page, status query

subcollection: get-support

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}

# Procura de status avançado
{: #adv-search}

É possível procurar em todas as guias na página Status, mas você sabia que é possível construir valores de procura de URL usando parâmetros de consulta de fora do console?
{:shortdesc}

A lista a seguir inclui exemplos de opções de procura de URL:

* Carregar a página com a guia Status selecionada: `console.cloud.ibm.com/status?selected=status`
* Carregar a página com a guia Manutenção planejada selecionada: `console.cloud.ibm.com/status?selected=maintenance`
* Carregar a página com a guia Boletim de segurança selecionada: `console.cloud.ibm.com/status?selected=security`
* Carregar a página com a guia Anúncios selecionada: `console.cloud.ibm.com/status?selected=announcement`
* Carregue a página com uma consulta de procura inserida: `console.cloud.ibm.com/status?selected=<selected>&query=<query>`
* Entrar na página com filtros selecionados. Por exemplo, é possível configurar a localização geográfica para América do Norte usando a procura de URL a seguir: `console.cloud.ibm.com/status?selected=status&region=na`

* Use identificadores de notificação exclusivos como parâmetro de procura para ir diretamente para os detalhes da notificação. Por exemplo, `query=INC1000001` visa itens com o ID: `INC1000001`. Neste exemplo, `INC1000001` é o número do caso para uma notificação de manutenção.

### Filtros de consulta de URL:
{: #url-query}

A tabela a seguir fornece informações sobre filtros de consulta de URL que podem ser usados para procuras em todas as guias da página de status. 

| Parâmetro de consulta de URL | Descrição | Valores |
| ----- | ----- | ----- | ----- |
| `?type` | Um filtro que se aplica somente à guia Status. Use a consulta `?type` para filtrar a guia Status por incidentes ou manutenção. | `=incident`, `=maintenance` |
| `?region` | Filtre a página por localização geográfica.  | `=na`, `=eu`, `=sa`, `=ap` |
| `?component` | Filtre a página por componentes do {{site.data.keyword.Bluemix_notm}}. Por exemplo, é possível filtrar por um serviço no qual você está interessado. | Aplica-se à maioria dos IDs do catálogo global; por exemplo, `?component=iotf-service` filtra a página e exibe eventos que afetam o Internet of Things Platform  |
{: caption="Tabela 1. Filtros de consulta de URL" caption-side="top"}

Sempre é possível usar os filtros **Filtrar por** e, em seguida, copiar ou marcar a consulta de URL gerada. Os filtros são exibidos em sua URL e podem ajudá-lo a construir consultas futuras.
{: tip}
