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

# 高级状态搜索
{: #adv-search}

您可以在“状态”页面上的所有选项卡上进行搜索，但您是否知道可以通过从控制台外部使用查询参数来构建 URL 搜索值？
{:shortdesc}

以下列表包含 URL 搜索选项的示例：

* 装入已选中“状态”选项卡的页面：`console.cloud.ibm.com/status?selected=status`
* 装入已选中“计划维护”选项卡的页面：`console.cloud.ibm.com/status?selected=maintenance`
* 装入已选中“安全公告”选项卡的页面：`console.cloud.ibm.com/status?selected=security`
* 装入已选中“声明”选项卡的页面：`console.cloud.ibm.com/status?selected=announcement`
* 装入已输入搜索查询的页面：`console.cloud.ibm.com/status?selected=<selected>&query=<query>`
* 登录已选中过滤器的页面。例如，您可以使用以下 URL 搜索将地理位置设置为“北美”：`console.cloud.ibm.com/status?selected=status&region=na`

* 使用唯一的通知标识作为搜索参数以直接转至通知的详细信息。例如，`query=INC1000001` 以标识为 `INC1000001` 的项为目标。在此示例中，`INC1000001` 是维护通知的案例号。

### URL 查询过滤器：

|URL 查询参数|描述|值|
| ----- | ----- | ----- | ----- |
| `?type` |仅适用于“状态”选项卡的过滤器。使用 `?type` 查询可按事件或维护过滤“状态”选项卡。| `=incident`、`=maintenance` |
| `?region` |按地理位置过滤页面。| `=na`、`=eu`、`=sa`、`=ap` |
| `?component` |按 {{site.data.keyword.Bluemix_notm}} 组件过滤页面。例如，您可以按感兴趣的服务进行过滤。|适用于大多数全局目录标识；例如，`?component=iotf-service` 将过滤页面，仅显示影响物联网平台的事件|
{: caption="表 1. URL 查询过滤器" caption-side="top"}

您始终可以使用**过滤条件**过滤器，然后复制生成的 URL 查询或将其设为书签。这些过滤器将显示在 URL 中，并且可帮助您构建未来查询。
{: tip}
