---

copyright:

  years: 2015, 2018

lastupdated: "2018-05-14"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# 如何取得案例的快速回應？
{: #quicktickresp}

與支援中心聯絡並開啟支援案例時，您可以要求特定嚴重性層次（視問題的類型及緊急性而定）。嚴重性層次可能會影響解決問題的快慢。
{:shortdesc}

您可以根據商業需求及支援層次來定義問題嚴重性。如需支援方案層次的相關資訊，請參閱[支援方案](/docs/get-support/index.html)。會調查所有案例，以識別及解決問題的主要原因。需要問題診斷資料來判定問題的主要原因時，系統將要求您核准從應用程式存取日誌檔及其他問題判斷資料。如果沒有此資料，可能會延遲問題的解決。

## 收集診斷資訊
{: #collecting-diagnostic-information}

為了診斷及解決 {{site.data.keyword.Bluemix_notm}} 應用程式及服務的問題，「{{site.data.keyword.Bluemix_notm}} 支援中心」團隊可能會要求您收集診斷資訊。請使用下列指示，盡快收集及提供所要求的資訊。

在您收集診斷資訊之前，請先完成下列步驟：

1. 確定您已安裝最新的 Cloud Foundry 指令行介面。如需相關資訊，請參閱[安裝 Cloud Foundry 指令行介面](/docs/starters/install_cli.html)。
>**附註：**如果您沒有安裝最新的 Cloud Foundry 指令行介面，在 cf 指令行連接至 {{site.data.keyword.Bluemix_notm}} 之後，`cf logs` 指令可能不會傳回輸出。
2. 使用 `cf api` 指令，確定您已將 Cloud Foundry 指令行介面連接到執行 {{site.data.keyword.Bluemix_notm}} 的位置。

使用下列其中一個 Script 來收集診斷資訊：

  * 對於 Windows 作業系統，下載並執行 [bmdiag-general.bat ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} 檔案。
  * 對於 Linux 及 Mac 作業系統，下載並執行 [bmdiag-general.sh ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} 檔案。

Script 使用 Cloud Foundry 指令行介面來擷取應用程式環境的下列資訊：
  * 應用程式日誌
  * 應用程式 meta 資料
  * 配置的路徑
  * 事件
  * 佈建的服務

## 呈報支援案例
{: #escalation}

身為 {{site.data.keyword.Bluemix_notm}} 客戶，您可以透過將您的案例呈報給值班的 {{site.data.keyword.Bluemix_notm}} 支援經理，來要求進一步的協助。呈報處理程序可讓您浮現重要問題，也可以在您覺得未適當解決您的支援案例的情況下，表達您的疑慮。案例呈報之後，值班經理會檢閱支援案例中的資訊、安排 {{site.data.keyword.Bluemix_notm}} 支援技術團隊的適當成員參與，然後為您提供適當的更新。

若要呈報支援案例，您必須具有 {{site.data.keyword.Bluemix_notm}} 進階或超值支援，且必須已開啟該問題的支援案例。此外，也請確定技術問題已詳細記錄在您開啟的支援案例中。

 若要呈報案例，請完成下列步驟：

  1. 以電話或會談與 {{site.data.keyword.Bluemix_notm}} 支援中心團隊聯絡:
    * 電話號碼如下：866-403-7638。
    * 使用會談請從 {{site.data.keyword.Bluemix_notm}} [支援中心 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://console.bluemix.net/unifiedsupport/supportcenter){: new_window}，或是如果您有未鏈結的 SoftLayer 帳戶，請從[客戶入口網站 ![外部鏈結圖示](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window}。
  2. 提供您現有的案例號碼，並要求呈報案例。
  3. 提供調整的理由及您案例的業務衝擊。

{{site.data.keyword.Bluemix_notm}} 支援經理每天 24 小時、每週每天都值班並提供服務。值班經理會安排適當的資源以解決您的案例，然後通知您已採取的動作。
