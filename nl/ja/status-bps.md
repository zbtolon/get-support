---

copyright:

  years: 2015, 2018

lastupdated: "2018-11-14"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 状況をモニターするためのベスト・プラクティス
{: #best-practices}

情報を受け取り、それに合わせて計画を立てるには、{{site.data.keyword.Bluemix}} の状況をモニターするための以下のベスト・プラクティスを使用します。
{: shortdesc}

## 近く予定されているメンテナンス時間帯を確認する
{: #monbp-checmaintwin}

{{site.data.keyword.Bluemix_notm}} コンソールの「ダッシュボード」ページに掲示された近く予定されているメンテナンス時間帯を、24 時間ごとに少なくとも一度は確認します。これには、以下のいずれかのオプションを使用します。
* [ダッシュボード ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://cloud.ibm.com){: new_window} で計画保守ウィジェットを確認します。**「すべてのイベント」**をクリックして、すべての計画保守を表示します。
* [「状況 - 計画保守」![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://cloud.ibm.com/status?selected=maintenance){: new_window} ページに直接ナビゲートします。

## 現在のメンテナンス時間帯や進行中の問題を確認する
{: #monbp-checcurmaninprog}

{{site.data.keyword.Bluemix_notm}} が期待どおりに動作していないと疑われる場合、「状況」ページで現在のメンテナンス時間帯や進行中の問題を確認します。 「状況」ページにまだリストされていないインシデントを報告するには、メニュー・バーで**「サポート」**をクリックして、サポート Case をオープンします。次に、「サポートの利用」タブで**「新規 Case の作成 (Create new case)」**をクリックします。 

## 複数の {{site.data.keyword.Bluemix_notm}} ロケーションを利用する
{: #monbp-multpreg}

{{site.data.keyword.Bluemix_notm}} のすべてのユーザーは、自動的にダラス、ロンドン、フランクフルト、シドニー、ワシントン DC、および東京の各ロケーションへのアクセス権限を持ちます。 {{site.data.keyword.Bluemix_notm}} グローバル運用チームは、すべてのロケーションを管理して、保守の影響を回避し、同時にすべてのロケーションに影響を与えるインシデントのリスクを最小限に抑えるようにしています。

ロケーションを切り替えるには、ダッシュボードに移動し、**「ロケーション」** メニューを展開します。

## 小規模の中断に備える
{: #monbp-prepmininter}

ほとんどの場合、メンテナンス時間帯の間でも {{site.data.keyword.Bluemix_notm}} の通常使用を継続できます。 しかし、サービスの小規模の中断を回避できない場合もあります。 {{site.data.keyword.Bluemix_notm}} のアプリケーション管理機能
(アプリの開始や停止など) が一時的に中断されても、稼働中のアプリケーションは通常、利用可能な状態を維持します。 稼働中のアプリケーションの可用性を最大にするために、アプリケーションごとに少なくとも 3 つのインスタンスを実行してください。

## E メール通知のサブスクライブ

ライト・アカウント所有者の場合、{{site.data.keyword.Bluemix_notm}} プラットフォームの計画外イベント (停止など) および計画されたイベント (保守など) に関する E メール通知を受信するかどうかを選択できます。 さらに、従量課金 (PAYG) アカウントまたはサブスクリプション・アカウントを使用している場合は、計画外イベント、保守、発表に関する {{site.data.keyword.Bluemix_notm}} インフラストラクチャーの E メール通知を受信するかどうかを選択できます。 詳しくは、[E メール・プリファレンスの設定](/docs/account/email.html)を参照してください。



