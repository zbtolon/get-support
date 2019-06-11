---

copyright:

  years: 2018,2019

lastupdated: "2019-05-13"

keywords: status page, status query

subcollection: get-support

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}

# 拡張状況検索
{: #adv-search}

「状況」ページではすべてのタブにわたって検索できますが、コンソールの外部から照会パラメーターを使用して URL 検索値を作成できることをご存じでしたか?
{:shortdesc}

以下のリストに、 URL 検索オプションの例を示します。

* 「状況」タブを選択してページをロードします。`console.cloud.ibm.com/status?selected=status`
* 「計画保守」タブを選択してページをロードします。`console.cloud.ibm.com/status?selected=maintenance`
* 「セキュリティー情報 (Security bulletin)」タブを選択してページをロードします。`console.cloud.ibm.com/status?selected=security`
* 「発表」タブを選択してページをロードします。`console.cloud.ibm.com/status?selected=announcement`
* 検索照会を入力してページをロードします。`console.cloud.ibm.com/status?selected=<selected>&query=<query>`
* フィルターを選択してページをロードします。 例えば、次の URL 検索を使用すると、地理的位置を北アメリカに設定できます。`console.cloud.ibm.com/status?selected=status&region=na`

* 通知の詳細に直接移動するには、固有の通知 ID を検索パラメーターとして使用します。  例えば、`query=INC1000001` は、ID が `INC1000001` の項目をターゲットにします。 この例では、`INC1000001` は保守に関する通知の Case 番号です。

### URL 照会フィルター:
{: #url-query}

| URL 照会パラメーター | 説明 | 値 |
| ----- | ----- | ----- | ----- |
| `?type` | 「状況」タブにのみ適用されるフィルター。 インシデントまたは保守によって「状況」タブをフィルタリングするには、`? type` 照会を使用します。 | `=incident`、`=maintenance` |
| `?region` | 地理的位置でページをフィルタリングします。  | `=na`、`=eu`、`=sa`、`=ap` |
| `?component` | {{site.data.keyword.Bluemix_notm}} コンポーネントでページをフィルタリングします。 例えば、関心のあるサービスでフィルタリングできます。 | ほとんどのグローバル・カタログ ID に適用されます。例えば、`?component=iotf-service` は、ページをフィルタリングして、IoT プラットフォームに影響を与えるイベントを表示します。 |
{: caption="表 1. URL 照会フィルター" caption-side="top"}

**「フィルター基準 (Filter by)」**フィルターはいつでも使用でき、生成された URL 照会をコピーしたりブックマークしたりできます。 フィルターは URL に表示され、今後の照会の作成に役立ちます。
{: tip}
