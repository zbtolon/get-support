---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-02"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# 如何让我的凭单快速得到受理？
{: #quicktickresp}

联系支持人员并开具支持凭单时，可根据问题的类型和紧急程度来请求特定严重性级别。严重性级别可能会影响解决问题的速度。
{:shortdesc}

您可根据业务需要和支持级别来定义问题的严重性。有关支持套餐级别的更多信息，请参阅[支持套餐](/docs/get-support/index.html)。将对所有凭单进行调查，以确定并解决问题的根本原因。支持团队需要问题诊断数据来确定问题的根本原因时，会询问您是否允许访问您应用程序中的日志文件，以及其他用于确定问题的数据。没有这些数据，您的问题解决起来可能更慢。

## 收集诊断信息
{: #collecting-diagnostic-information}

要诊断并解决 {{site.data.keyword.Bluemix_notm}} 应用程序和服务的问题，{{site.data.keyword.Bluemix_notm}} 支持团队可能要求提供诊断信息。请根据以下指示信息，尽快收集并提供所要求的信息。

在收集诊断信息之前，请完成以下步骤：

1. 确保已安装最新版本的 Cloud Foundry 命令行界面。有关更多信息，请参阅[安装 Cloud Foundry 命令行界面](/docs/starters/install_cli.html)。
>**注：**如果未安装最新版本，那么在 Cloud Foundry 命令行连接到 {{site.data.keyword.Bluemix_notm}} 后，`cf logs` 命令可能不会返回输出。
2. 确保使用 `cf api` 命令将 Cloud Foundry 命令行界面连接到 {{site.data.keyword.Bluemix_notm}} 正在运行的位置。

使用以下其中一个脚本来收集诊断信息：

  * 对于 Windows 操作系统，下载并运行 [bmdiag-general.bat ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} 文件。
  * 对于 Linux 和 Mac 操作系统，下载并运行 [bmdiag-general.sh ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} 文件。

脚本使用 Cloud Foundry 命令行界面来从应用程序环境中抽取以下信息：
  * 应用程序日志
  * 应用程序元数据
  * 配置的路径
  * 事件
  * 提供的服务

## 上报支持案例
{: #escalation}

使用上报过程可报告严重问题，或者如果您认为自己的支持案例未得到妥善处理，也可以使用上报过程。上报案例后，当值经理会复查支持案例中的信息，与 {{site.data.keyword.Bluemix_notm}} 技术支持团队的相应成员进行沟通，然后通知您最新的进展。

作为任何付费预订的客户，您可以将您的案例上报给当值的 {site.data.keyword.Bluemix_notm}} 支持经理来请求进一步的帮助。 

要上报支持案例，您必须已针对问题开具支持案例。此外，请确保在所开具的支持案例中已对技术问题进行详细的描述。

 要上报案例，请完成以下步骤：

  1. 通过电话或交谈与 {{site.data.keyword.Bluemix_notm}} 支持团队进行联系：
    * 电话号码：866-403-7638。
    * 交谈选项：{{site.data.keyword.Bluemix_notm}} [支持中心 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://console.bluemix.net/unifiedsupport/supportcenter){: new_window}，或[客户门户网站 ![外部链接图标](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window}（如果您有未链接的 SoftLayer 帐户）。
  2. 提供现有案例号并请求上报案例。
  3. 提供上报理由以及该案例所带来的业务影响。

{{site.data.keyword.Bluemix_notm}} 支持经理全天候当值。当值经理会与相应的资源进行联系来处理您的案例，然后会通知您要采取哪些措施。
