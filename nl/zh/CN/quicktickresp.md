---

copyright:

  years: 2015, 2018

lastupdated: "2018-01-10"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# 如何获得对凭单的快速响应？
{: #quicktickresp}

联系支持人员并开具支持凭单时，可根据问题的类型和紧急程度来请求特定严重性级别。严重性级别可能会影响解决问题的速度。
{:shortdesc}

您可根据业务需要和支持级别来定义问题的严重性。将对所有凭单进行调查，以确定并解决问题的根本原因。需要问题诊断数据来确定问题的根本原因时，将要求您批准从您的应用程序访问日志文件和其他问题确定数据。没有这些数据，您的问题解决起来可能更慢。

如果要求您提供诊断信息，请使用以下指示信息尽快收集并提供所请求的信息。

## 收集诊断信息
{: #collecting-diagnostic-information}

要诊断并解决 {{site.data.keyword.Bluemix_notm}} 应用程序和服务的问题，{{site.data.keyword.Bluemix_notm}} 支持团队可能会要求您收集诊断信息。

在收集诊断信息之前，请完成以下步骤：

1. 确保已安装最新的 cf 命令行界面。有关更多信息，请参阅[安装 cf 命令行界面](/docs/starters/install_cli.html)。
>**注：**如果未安装最新 cf 命令行界面，那么在 cf 命令行连接到 {{site.data.keyword.Bluemix_notm}} 后，`cf logs` 命令可能不会返回输出。
2. 确保使用 `cf api` 命令将 cf 命令行界面连接到 {{site.data.keyword.Bluemix_notm}} 正在运行的位置。

使用以下其中一个脚本来收集诊断信息：

  * 对于 Windows 操作系统，下载并运行 [bmdiag-general.bat ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} 文件。
  * 对于 Linux 和 Mac 操作系统，下载并运行 [bmdiag-general.sh ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} 文件。

脚本使用 cf 命令行界面来从应用程序环境抽取以下信息：
  * 应用程序日志
  * 应用程序元数据
  * 配置的路径
  * 事件
  * 提供的服务

## 可以上报支持凭单吗？
{: #escalation}

对于高端或标准支持，如果您未收到对支持凭单的及时响应，或者如果您认为支持凭单未得到恰当处理，那么可以上报支持凭单。  
{:shortdesc}

有关高端和标准支持的更多信息，请参阅[支持类型](/docs/get-support/getstarttssup.html#typesofsupport)。

通过支持凭单上报过程，IBM 管理人员将复查您的问题，并与您合作来改进支持体验。

要提交上报请求，请完成以下步骤：
  1. 使用摘要**上报请求**来开具新的支持凭单。
  2. 要确保上报请求能与原始支持凭单匹配，请在凭单正文中包含以下信息：
      * 需要上报的已开具支持凭单的凭单编号。
      * 对需要上报的原因的简要概述。

## 工作时间
{: #support-hours-operation}

将全天候监视严重性为 1 的问题。将在周日 21:30 UTC 到周五 23:59 UTC（不包括节假日）监视具有其他所有严重性级别的问题的表单提交。

有关将这些支持工作时间转换为本地时区的帮助，请参阅 [Timeanddate.com ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://www.timeanddate.com)。有关节假日安排的更多信息，请参阅 [{{site.data.keyword.Bluemix_notm}} Support Holidays ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://ibm.biz/bluemixholidays)。
