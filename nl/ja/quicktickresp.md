---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-23"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# チケットに対して迅速な対応を得るには
{: #quicktickresp}

サポートに連絡してサポート・チケットをオープンする際には、問題のタイプと緊急度に応じて、特定の重大度レベルを要求できます。 重大度レベルは、どれぐらい迅速に問題が対処されるかに影響を与えます。
{:shortdesc}

問題の重大度は、業務での必要性およびサポート・レベルに基づいて定義してください。 サポート・プランのレベルについて詳しくは、『[サポート・プラン](/docs/get-support/index.html)』を参照してください。 すべてのチケットが、問題の根本原因を特定して解決するために調査されます。 問題の根本原因を判別するためにサポート・チームが問題診断データを必要とする場合、アプリケーションからのログ・ファイルおよびその他の問題判別データへのアクセスを承認するように依頼されます。 このデータがないと、問題の解決が遅れることがあります。

## 診断情報の収集
{: #collecting-diagnostic-information}

{{site.data.keyword.Bluemix_notm}} アプリケーションおよびサービスに関する問題を診断し解決するために、{{site.data.keyword.Bluemix_notm}} サポート・チームから診断情報を求められることがあります。 以下の手順を使用して、要求された情報をできるだけ早く収集して提供してください。

診断情報を収集する前に、以下のステップを実行します。

1. 最新バージョンの Cloud Foundry コマンド・ライン・インターフェースがインストールされていることを確認します。 詳細については、[Cloud Foundry コマンド・ライン・インターフェースのインストール (Installing the Cloud Foundry command line interface) ](/docs/starters/install_cli.html)を参照してください。
>**注:** 最新バージョンがない場合、Cloud Foundry コマンド・ラインが {{site.data.keyword.Bluemix_notm}} に接続された後も、`cf logs` コマンドが出力を返さない可能性があります。
2. `cf api` コマンドを使用して、{{site.data.keyword.Bluemix_notm}} が実行中の場所に Cloud Foundry コマンド・ライン・インターフェースを接続済みであることを確認してください。

診断情報を収集するには、以下のいずれかのスクリプトを使用してください。

  * Windows オペレーティング・システムの場合、[bmdiag-general.bat ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} ファイルをダウンロードして実行します。
  * Linux および Mac オペレーティング・システムの場合、[bmdiag-general.sh ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} ファイルをダウンロードして実行します。

これらのスクリプトは Cloud Foundry コマンド・ライン・インターフェースを使用して、ご使用のアプリケーション環境から以下の情報を抽出します。
  * アプリケーション・ログ
  * アプリケーション・メタデータ
  * 構成済みの経路
  * イベント
  * プロビジョンされたサービス

## サポート・ケースのエスカレート
{: #escalation}

サポート・ケースが適切に対処されていないと感じる場合や、重大な問題を表面化させたい場合に、エスカレーション・プロセスを使用できます。 ケースがエスカレートされると、当番の管理者がそのサポート・ケース内の情報を検討し、{{site.data.keyword.Bluemix_notm}} サポート・テクニカル・チームの適切なメンバーを手配し、適切な更新をお客様に提供します。

任意の有料サブスクリプションを持つお客様としてケースを当番の {{site.data.keyword.Bluemix_notm}} サポート管理者にエスカレートすることで、さらに支援を要求できます。 

サポート・ケースをエスカレートするには、問題のサポート・ケースがオープンされている必要があります。 また、オープンしたサポート・ケースに、技術的な問題を詳しく記述したことも確認してください。

 問題事項をエスカレートするには、以下のステップを実行します。

  1. 電話またはチャットで {{site.data.keyword.Bluemix_notm}} サポート・チームに連絡を取ります。
    * 電話の場合は番号 866-403-7638 を使用します。
    * チャットの場合は {{site.data.keyword.Bluemix_notm}} [サポート・センター ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.bluemix.net/unifiedsupport/supportcenter){: new_window} から行うか、または、リンクされていない SoftLayer アカウントをお持ちの場合は[カスタマー・ポータル ![外部リンク・アイコン](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window} から行います。
  2. 既存のケース番号を知らせ、その問題をエスカレートするよう依頼します。
  3. エスカレーションの理由付けと、ビジネスへのその問題の影響を説明します。

{{site.data.keyword.Bluemix_notm}} サポート・マネージャーが任務に就いていて、1 日 24 時間、週 7 日対応しています。 当番のマネージャーが、問題に対処するための適切な人員を手配し、実行されたアクションについてお客様に知らせます。
