---

copyright:

  years: 2015, 2018

lastupdated: "2019-02-18"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 监视状态的最佳做法
{: #best-practices}

要随时获得最新信息并相应进行规划，请使用以下最佳做法来监视 {{site.data.keyword.Bluemix}} 的状态。
{: shortdesc}

## 检查即将开始的维护时段
{: #monbp-checmaintwin}

通过使用以下某个选项，检查 {{site.data.keyword.Bluemix_notm}} 控制台“仪表板”页面上发布的即将开始的维护时段，至少每 24 小时检查一次：
* 检查[“仪表板”![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://cloud.ibm.com){: new_window} 上的“计划维护”窗口小部件。单击**所有事件**以查看所有计划维护。
* 直接导航至[状态 - 计划维护 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://cloud.ibm.com/status?selected=maintenance){: new_window} 页面

## 检查当前维护时段或进行中事件
{: #monbp-checcurmaninprog}

如果您怀疑{{site.data.keyword.Bluemix_notm}}未按预期运行，请检查“状态”页面以获取当前维护时段或正在进行的事件。要报告尚未在“状态”页面上列出的事件，请通过单击菜单栏中的**支持**来打开支持案例。然后，在“获取支持”选项卡上单击**创建新案例**。

## 利用多个 {{site.data.keyword.Bluemix_notm}} 位置
{: #monbp-multpreg}

所有 {{site.data.keyword.Bluemix_notm}} 用户都自动有权访问达拉斯、伦敦、法兰克福、悉尼、华盛顿和东京的位置。{{site.data.keyword.Bluemix_notm}} 全球运营团队会管理所有位置，以避免维护影响，并最大限度降低同时影响所有区域的事件的风险。

要切换位置，请转至仪表板并展开**位置**菜单。

## 为小的中断做准备
{: #monbp-prepmininter}

在大多数情况下，即使在维护时段内，也可以正常继续使用 {{site.data.keyword.Bluemix_notm}}。但是，小的服务中断总是不可避免的。即使 {{site.data.keyword.Bluemix_notm}} 的应用程序管理功能（例如启动和停止应用程序）暂时中断，运行中应用程序通常也会一直可用。要最大限度地提高运行中应用程序的可用性，每个应用程序应至少运行三个实例。

## 预订电子邮件通知
{: #monbp-subscribing}

如果您是轻量帐户所有者，那么可以选择是否接收有关 {{site.data.keyword.Bluemix_notm}} 平台计划外事件（如中断）和计划事件（如维护）的电子邮件通知。此外，如果您有现收现付或预订帐户，那么可以选择是否接收有关计划外事件、维护和公告的 {{site.data.keyword.Bluemix_notm}} 基础架构电子邮件通知。有关更多信息，请参阅[设置电子邮件首选项](/docs/account?topic=account-account_setup#account_setup)。



