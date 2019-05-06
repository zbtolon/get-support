---

copyright:

  years: 2015, 2018

lastupdated: "2019-04-29"

keywords: upcoming maintenance, stay up-to-date, monitor status

subcollection: get-support

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 監視狀態的最佳作法
{: #best-practices}

請使用下列最佳作法來監視 {{site.data.keyword.Bluemix}} 的狀態，以隨時取得通知並據此進行規劃。
{: shortdesc}

## 檢查即將到來的維護時間範圍
{: #monbp-checmaintwin}

使用下列其中一個選項，檢查 {{site.data.keyword.Bluemix_notm}} 主控台「儀表板」頁面上所張貼即將到來的維護時間範圍（至少每 24 小時一次）：
* 檢查[儀表板 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com){: new_window} 上的「計劃性維護」小組件。按一下**所有事件**，以檢視所有計劃性維護。
* 直接導覽至[狀態 - 計劃性維護 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com/status?selected=maintenance){: new_window} 頁面。

## 檢查現行維護時間範圍或進行中的突發事件
{: #monbp-checcurmaninprog}

如果您懷疑 {{site.data.keyword.Bluemix_notm}} 未如預期般運作，請檢查「狀態」頁面中是否有現行維護時間範圍或進行中的突發事件。若要報告「狀態」頁面尚未列出的突發事件，請從功能表列按一下**支援**來開立支援案例。然後，在「取得支援」標籤上按一下**建立新的案例**。

## 充分運用多個 {{site.data.keyword.Bluemix_notm}} 位置
{: #monbp-multpreg}

{{site.data.keyword.Bluemix_notm}} 的所有使用者都自動能夠存取「達拉斯」、「倫敦」、「法蘭克福」、「雪梨」、「華盛頓特區」及「東京」位置。{{site.data.keyword.Bluemix_notm}} Global Operations 團隊會管理所有位置，以避免維護造成的影響，並讓發生同時影響所有位置之突發事件的風險降到最低。

若要切換位置，請移至儀表板，並展開**位置**功能表。

## 準備因應輕微岔斷
{: #monbp-prepmininter}

在大部分情況下，即使是在維護時間範圍的期間內，{{site.data.keyword.Bluemix_notm}} 仍可繼續正常使用。不過，無法完全避免服務的輕微岔斷。即使暫時岔斷 {{site.data.keyword.Bluemix_notm}} 的應用程式管理功能（例如啟動及停止應用程式），執行中的應用程式通常仍可持續使用。為了盡量提高執行中應用程式的可用性，針對每一個應用程式請至少執行三個實例。

## 訂閱電子郵件通知
{: #monbp-subscribing}

如果您是「精簡」帳戶擁有者，可以選取是否要收到有關 {{site.data.keyword.Bluemix_notm}} 平台非計劃性事件（例如運作中斷）及計劃性事件（例如維護）的電子郵件通知。此外，如果您有「隨收隨付制」或「訂閱」帳戶，可以選擇是否要收到有關非計劃性事件、維護及公告的 {{site.data.keyword.Bluemix_notm}} 基礎架構電子郵件通知。如需相關資訊，請參閱[設定電子郵件喜好設定](/docs/account?topic=account-email-prefs)。



