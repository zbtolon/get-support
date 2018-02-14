---

copyright:

  years: 2015, 2018

lastupdated: "2018-01-16"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 檢視 {{site.data.keyword.Bluemix_notm}} 狀態及通知
{: #viewing-bluemix-status}

「狀態」頁面是尋找通知和公告的一個中心位置，從中可瞭解影響 {{site.data.keyword.Bluemix_notm}} 平台及主要服務的重要事件。
{:shortdesc}

在「狀態」頁面上，您可以找到下列資訊：

  * 所有 {{site.data.keyword.Bluemix_notm}} Foundry Service 地區中服務及元件的現行狀態。
  * 維護及突發事件的公告清單（依時間順序）。您可以過濾清單，或開啟個別公告以取得其他詳細資料。
  * 計劃性的維護時間，除非是極端情況，否則至少會提前 24 小時張貼。
  * 非計劃性的突發事件或運作中斷，{{site.data.keyword.Bluemix_notm}} 團隊一發現就會立即張貼。突發事件通知會定期更新，直到解決為止。
  * 影響各種 {{site.data.keyword.Bluemix_notm}} 服務或該平台的安全性公告的參照。
  * 符合您一般利益的其他平台層面公告。
  * [您可以訂閱的 RSS 資訊來源](#subscribing-rss-feed)。

您可以選擇下列其中一個選項來尋找「狀態」頁面：

  * 登入 {{site.data.keyword.Bluemix_notm}} 主控台。從功能表列中，按一下**支援**，然後選取**狀態**。請檢查針對 ![部分問題](images/some_issues.svg) 圖示列出的資源。此圖示可能指出運作中斷。
  * 直接在 [{{site.data.keyword.Bluemix_notm}} - 狀態 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://console.bluemix.net/status){: new_window} 進行存取。


## 監視狀態的最佳作法
{: #best-practices}

請使用下列最佳作法來監視 {{site.data.keyword.Bluemix_notm}} 的狀態，以隨時取得通知並據此進行規劃。

### 檢查即將到來的維護時間範圍
{: #monbp-checmaintwin}

使用下列其中一個選項，檢查「狀態」頁面上張貼的即將到來的維護時間範圍（至少每 24 小時一次）：
* 直接導覽至[狀態 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://console.bluemix.net/status){: new_window} 頁面
* 使用 RSS 資訊來源或 RSS 對電子郵件的轉遞程式

### 檢查現行維護時間範圍或進行中的突發事件
{: #monbp-checcurmaninprog}

如果您懷疑 {{site.data.keyword.Bluemix_notm}} 未如預期般運作，請檢查「狀態」頁面中的現行維護時間範圍或進行中的突發事件。若要提報「狀態」頁面上尚未列出的突發事件，請按一下功能表列上的**支援**並選取**新增問題單**，或是存取 [{{site.data.keyword.Bluemix_notm}} 支援中心 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://www.ibm.biz/bluemixsupport){: new_window} 說明頁面，來開立支援問題單。

### 充分運用多個 {{site.data.keyword.Bluemix_notm}} Foundry Service 地區
{: #monbp-multpreg}

「{{site.data.keyword.Bluemix_notm}} 公用」的所有使用者都自動可存取 US-SOUTH、US-EAST、EU-GB、EU-DE 及 AU-SYD 地區。{{site.data.keyword.Bluemix_notm}} Global Operations 團隊會管理所有地區，以避免維護造成的影響，並讓發生同時影響所有地區之突發事件的風險降到最低。

若要切換地區，請從 {{site.data.keyword.Bluemix_notm}} 功能表列中，展開地區功能表，然後選取另一個地區。

### 準備進行輕微岔斷
{: #monbp-prepmininter}

在大部分情況下，即使是在維護時間範圍的期間內，{{site.data.keyword.Bluemix_notm}} 仍可繼續正常使用。不過，無法完全避免服務的輕微岔斷。即使暫時岔斷 {{site.data.keyword.Bluemix_notm}} 的應用程式管理功能（例如啟動及停止應用程式），執行中應用程式通常仍可持續使用。為了盡量提高執行中應用程式的可用性，針對每一個應用程式請至少執行三個實例。

## 訂閱 RSS 資訊來源
{: #subscribing-rss-feed}

您會透過訂閱 {{site.data.keyword.Bluemix_notm}}「狀態」頁面的 RSS 資訊來源，來收到任何通知的警示。這種方式讓您不需要定期查閱「狀態」頁面即可取得更新。

若要訂閱，請遵循下列步驟：

1. 下載並安裝 RSS 閱讀器。
2. 以下列其中一種方法，使用您的閱讀器訂閱資訊來源：
    * 將 RSS ![RSS](images/rss.svg) 圖示拖曳到您的 RSS 閱讀器。
    * 在 RSS 圖示上按一下滑鼠右鍵、選取**複製鏈結位址**，然後將 URL 貼入您的 RSS 閱讀器。

如需相關資訊，請參閱閱讀器的**說明**區段。
 	   

透過 Web 瀏覽器外掛程式，可以取得其他讀取 RSS 資訊來源的方法，例如：
  * 適用於 Chrome 的 [RSS 資訊來源 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://feeder.co/){: new_window} 讀取器
  * 適用於 Firefox 的 [Brief ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://addons.mozilla.org/en-US/firefox/addon/brief/){: new_window} 附加程式

News 來源（例如下列網站）也提供方法來讀取 RSS 資訊來源：
  * [Feedly ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://www.feedly.com/){: new_window}
  * [G2reader ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://www.g2reader.com/en/){: new_window}

您也可以使用協力廠商服務，自動為每一個 RSS 更新傳送電子郵件。下列清單提供部分協力廠商服務範例：

  * www.feedmyinbox.com
  * www.rssforward.com
  * www.feedrabbit.com
  * www.mailchimp.com
  * www.feedmailer.com
  * www.iftt.com

{{site.data.keyword.Bluemix_notm}} 每個月通常約有 50 次更新。


## 設定突發事件及維護電子郵件通知
{: #setting-up-notifications}

若為「{{site.data.keyword.Bluemix_notm}} 公用」，您可以註冊平台通知。平台通知是 {{site.data.keyword.Bluemix_notm}} 平台的突發事件及維護事件的選用性電子郵件警示。您可以選擇接收這些電子郵件通知，方法是按一下**管理** > **帳戶** > **通知**，然後選取**平台**標籤。如需設定帳戶通知的相關資訊，請參閱[設定通知](/docs/account/notifications.html#setting-notifications)。
