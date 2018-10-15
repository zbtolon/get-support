---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-04"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 查看系统状态和通知
{: #viewing-bluemix-status}

“状态”页面是查找通知和公告的一个中心位置，从中可了解影响 {{site.data.keyword.Bluemix_notm}} 平台和主要服务的关键事件。
{:shortdesc}

在“状态”页面上，可以找到以下信息：

  * 所有 {{site.data.keyword.Bluemix_notm}} Foundry 服务区域中服务和组件的当前状态。
  * 维护和事件相关公告的列表，按时间顺序排列。您可以过滤该列表或打开单个公告来查看更多详细信息。
  * 提供事先通知的计划维护时段，但在极端情况下除外。
  * 计划外的事件或中断，在 {{site.data.keyword.Bluemix_notm}} 团队获悉后立即发布。事件通知会定期更新，直到得到解决为止。
  * 对影响各种 {{site.data.keyword.Bluemix_notm}} 服务或平台的安全公报的引用。
  * 具有一般关注度的其他平台范围的公告。
  * [可以预订的 RSS 订阅源](#subscribing-rss-feed)。

可以通过选择以下两个选项之一来找到“状态”页面：

  * 登录到 {{site.data.keyword.Bluemix_notm}} 控制台。在菜单栏中，单击**支持**，然后选择**状态**。检查列出的资源中是否存在 ![某些问题](images/some_issues.svg) 图标。此图标可能指示有中断情况。
  * 直接通过 [{{site.data.keyword.Bluemix_notm}} - 状态 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://console.bluemix.net/status){: new_window} 进行访问。


## 监视状态的最佳做法
{: #best-practices}

使用针对监视 {{site.data.keyword.Bluemix_notm}} 状态的以下最佳实践可了解实时情况并相应进行规划。

### 检查即将开始的维护时段
{: #monbp-checmaintwin}

通过使用以下某个选项，检查“状态”页面上发布的即将开始的维护时段，至少每 24 小时检查一次：
* 直接导航至[状态 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://console.bluemix.net/status){: new_window} 页面
* 使用 RSS 订阅源或“RSS 到电子邮件”转发器

### 检查当前维护时段或进行中事件
{: #monbp-checcurmaninprog}

如果您怀疑 {{site.data.keyword.Bluemix_notm}} 未按预期运作，请检查“状态”页面上的当前维护时段或进行中的事件。要报告尚未在“状态”页面上列出的事件，请通过单击菜单栏上的**支持**并选择**添加凭单**或通过访问 [{{site.data.keyword.Bluemix_notm}} 支持 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://www.ibm.biz/bluemixsupport){: new_window} 帮助页面来开具支持凭单。

### 利用多个 {{site.data.keyword.Bluemix_notm}} Foundry 服务区域
{: #monbp-multpreg}

{{site.data.keyword.Bluemix_notm}} Public 的所有用户自动有权访问美国南部、英国、德国、悉尼、美国东部和亚太地区南部区域。{{site.data.keyword.Bluemix_notm}} 全球运营团队会管理所有区域，以避免维护影响，同时最大限度地降低影响所有区域的事件的风险。

要切换区域，请从 {{site.data.keyword.Bluemix_notm}} 菜单栏中，展开区域菜单，然后选择其他区域。

### 为小的中断做准备
{: #monbp-prepmininter}

在大多数情况下，即使在维护时段内，也可以正常继续使用 {{site.data.keyword.Bluemix_notm}}。但是，小的服务中断总是不可避免的。即使 {{site.data.keyword.Bluemix_notm}} 的应用程序管理功能（例如启动和停止应用程序）暂时中断，运行中应用程序通常也会一直可用。要最大限度地提高运行中应用程序的可用性，每个应用程序应至少运行三个实例。

## 预订 RSS 订阅源
{: #subscribing-rss-feed}

通过预订 {{site.data.keyword.Bluemix_notm}}“状态”页面的 RSS 订阅源来接收任何通知提醒。通过此方法，您可以获取更新，而不必定期查看“状态”页面。

要进行预订，请执行以下步骤：

1. 下载并安装 RSS 阅读器。
2. 通过以下某个方法，使用您的阅读器来预订订阅源：
    * 将 ![RSS](images/rss.svg) 图标拖入 RSS 阅读器。
    * 右键单击 RSS 图标，选择**复制链接地址**，然后将 URL 粘贴到 RSS 阅读器中。

有关更多信息，请参阅阅读器的**帮助**部分。 	   

通过 Web 浏览器插件可以使用其他阅读 RSS 订阅源的方法，例如以下插件：
  * [用于 Chrome 的 RSS 订阅源 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://feeder.co/){: new_window} 阅读器
  * [Firefox 的 Brief ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://addons.mozilla.org/en-US/firefox/addon/brief/){: new_window} 附加组件

新闻源（如以下站点）也会提供阅读 RSS 订阅源的方法：
  * [Feedly ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://www.feedly.com/){: new_window}
  * [G2reader ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://www.g2reader.com/en/){: new_window}

您还可以通过第三方服务自动发送电子邮件来通知每个 RSS 更新。以下列表提供了一些第三方服务示例：

  * www.feedmyinbox.com
  * www.rssforward.com
  * www.feedrabbit.com
  * www.mailchimp.com
  * www.feedmailer.com
  * www.iftt.com

{{site.data.keyword.Bluemix_notm}} 每月通常有 50 条左右的更新。


## 设置事件和维护通知
{: #setting-up-notifications}

在 {{site.data.keyword.Bluemix_notm}} Public 中，您可以通过注册来获取平台通知。平台通知是平台事件和维护事件的可选电子邮件警报。要设置通知，请单击**管理** > **帐户** > **通知**，然后选择**平台**选项卡。 
