---

copyright:

  years: 2018,2019

lastupdated: "2019-01-30"

keywords: status page, status query

subcollection: get-support

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}

# 進階狀態搜尋
{: #adv-search}

您可以在「狀態」頁面上的所有標籤中搜尋，但您是否知道可以從主控台之外使用查詢參數來建置 URL 搜尋值？
{:shortdesc}

下列清單包含 URL 搜尋選項的範例：

* 載入頁面並選取「狀態」標籤：`console.cloud.ibm.com/status?selected=status`
* 載入頁面並選取「計劃性維護」標籤：`console.cloud.ibm.com/status?selected=maintenance`
* 載入頁面並選取「安全公告」標籤：`console.cloud.ibm.com/status?selected=security`
* 載入頁面並選取「公告」標籤：`console.cloud.ibm.com/status?selected=announcement`
* 載入頁面並輸入搜尋查詢：`console.cloud.ibm.com/status?selected=<selected>&query=<query>`
* 登陸頁面並選取過濾器。例如，您可以使用下列 URL 搜尋將地理位置設定為北美洲：`console.cloud.ibm.com/status?selected=status&region=na`

* 使用唯一的通知 ID 作為搜尋參數，以直接移至通知的詳細資料。例如，`query=INC1000001` 會以具有 ID `INC1000001` 的項目為目標。在此範例中，`INC1000001` 是維護通知的案例號碼。

### URL 查詢過濾器：
{: #url-query}

|URL 查詢參數| 說明                                                  |值|
| ----- | ----- | ----- | ----- |
| `?type` |僅適用於「狀態」標籤的過濾器。請使用 `?type` 查詢，依突發事件或維護來過濾「狀態」標籤。| `=incident`、`=maintenance` |
| `?region` |依地理位置過濾頁面。| `=na`、`=eu`、`=sa`、`=ap` |
| `?component` |依 {{site.data.keyword.Bluemix_notm}} 元件過濾頁面。例如，您可能依您感興趣的服務來進行過濾。|適用於大部分全球型錄 ID；例如，`?component=iotf-service` 將會過濾頁面，且只會顯示影響 Internet of Things Platform 的事件|
{: caption="表 1. URL 查詢過濾器" caption-side="top"}

您隨時都可以使用**過濾依據**過濾器，然後將產生的 URL 查詢複製或設為書籤。過濾器會顯示在 URL 中，並且可協助您建置未來的查詢。
{: tip}
