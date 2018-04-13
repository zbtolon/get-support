---

copyright:

  years: 2015, 2018

lastupdated: "2018-03-15"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# 如何取得問題單的快速回應？
{: #quicktickresp}

與支援中心聯絡並開立支援問題單時，您可以要求特定嚴重性層次（視問題的類型及緊急性而定）。嚴重性層次可能會影響解決問題的快慢。
{:shortdesc}

您可以根據商業需求及支援層次來定義問題嚴重性。調查所有問題單，以識別及解決問題的主要原因。需要問題診斷資料來判定問題的主要原因時，系統將要求您核准從應用程式存取日誌檔及其他問題判斷資料。如果沒有此資料，可能會延遲問題的解決。

如果要求您提供診斷資訊，請使用下列指示，盡快收集及提供所要求的資訊。

## 收集診斷資訊
{: #collecting-diagnostic-information}

為了診斷及解決 {{site.data.keyword.Bluemix_notm}} 應用程式及服務的問題，「{{site.data.keyword.Bluemix_notm}} 支援」團隊可能會要求您收集診斷資訊。

在您收集診斷資訊之前，請先完成下列步驟：

1. 確定您已安裝最新的 cf 指令行介面。如需相關資訊，請參閱[安裝 cf 指令行介面](/docs/starters/install_cli.html)。
>**附註：**如果您沒有安裝最新的 cf 指令行介面，在 cf 指令行連接至 {{site.data.keyword.Bluemix_notm}} 之後，`cf logs` 指令可能不會傳回輸出。
2. 使用 `cf api` 指令，確定您已將 cf 指令行介面連接到執行 {{site.data.keyword.Bluemix_notm}} 的目錄。

使用下列其中一個 Script 來收集診斷資訊：

  * 對於 Windows 作業系統，下載並執行 [bmdiag-general.bat ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} 檔案。
  * 對於 Linux 及 Mac 作業系統，下載並執行 [bmdiag-general.sh ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} 檔案。

Script 使用 cf 指令行介面來擷取應用程式環境的下列資訊：
  * 應用程式日誌
  * 應用程式 meta 資料
  * 配置的路徑
  * 事件
  * 佈建的服務

## 我可以呈報支援問題單嗎？
{: #escalation}

使用超值或進階支援時，如果您未收到支援問題單的及時回應，或覺得支援問題單未獲得適當地解決，則可以呈報支援問題單。  
{:shortdesc}

如需超值及進階支援的相關資訊，請參閱[支援類型](/docs/get-support/getstarttssup.html#typesofsupport)。

透過支援問題單呈報程序，IBM 管理會檢閱您的問題，並與您合作來改善支援體驗。

若要提交呈報要求，請完成下列步驟：
  1. 開立摘要為**呈報要求**的新支援問題單。
  2. 若要確定您的呈報要求與原始支援問題單相符，請在問題單的內文中包含下列資訊：
      * 需要呈報的已開立支援問題單的問題單號碼。
      * 需要呈報之原因的簡單摘要。

## 作業時間
{: #support-hours-operation}

我們將 24 小時全年無休地監視嚴重性 1 的問題。從星期日 21:30 UTC 到星期五 23:59 UTC（不包括假日）都會監視含所有其他嚴重性層次之問題的表單提交。

如需將這些支援時間轉換為當地時區的協助，請參閱 [Timeanddate.com ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://www.timeanddate.com)。如需假日排程的相關資訊，請參閱 [{{site.data.keyword.Bluemix_notm}} Support Holidays ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://ibm.biz/bluemixholidays)。
