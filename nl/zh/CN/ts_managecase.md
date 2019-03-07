---

copyright:

  years: 2015, 2019

lastupdated: "2019-02-19"

keywords: help managing cases, resolve issues managing cases, trouble working with cases

subcollection: get-support

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# 有关管理支持案例的故障诊断
{: #Supportcases}

您可能会遇到有关创建和管理 {{site.data.keyword.Bluemix}} 支持案例的问题。在许多情况下，只需执行几个简单的步骤即可解决这些问题。
{:shortdesc}

## 为什么无法创建或编辑支持案例？ 
{: #ts_service_broker}

您无法创建或编辑 {{site.data.keyword.Bluemix_notm}} 支持案例，并且会显示一条错误消息，说明您没有相应的访问权。
{:shortdesc}

尝试创建案例时，将显示以下错误消息：   
{: tsSymptoms}

`您似乎无权为此帐户创建案例。`

访问和管理支持案例时出现的一般问题的原因可能是没有支持中心帐户管理服务的 Identity and Access Management (IAM) 访问策略。必须在支持中心帐户管理服务上为您分配编辑者或管理员角色，您才能创建案例。
{: tsCauses}

要解决此问题，帐户所有者、支持中心服务的管理员或所有帐户管理服务的管理员都可以在支持中心上分配 IAM 策略来管理案例。
{: tsResolve}

如果您是支持中心的帐户所有者或管理员，请完成以下步骤来创建用于处理支持案例的访问策略：

1. 转至**管理** &gt; **访问权 (IAM)**，然后选择**用户**。
2. 选择用户名，然后单击**访问策略**。 
3. 单击**分配访问权**。 
4. 选择**分配对帐户管理服务的访问权**。 
5. 在**服务**菜单中，选择**支持中心**。 
6. 选择角色以定义用户的访问级别。 


## 为什么无法查看帐户中的所有案例？
{: #ts_viewcasedetails}

您无法查看帐户中的所有案例，因为您无权查看帐户中的所有用户。
{:shortdesc}

尝试查看与帐户关联的支持案例时，看不到所有打开的案例。
{: tsSymptoms}

帐户所有者将[用户列表可视性设置](/docs/iam?topic=iam-userlistview#userlistview)设为受限。如果该设置设为受限，并且您没有额外的访问策略来查看帐户中的用户，那么您没有查看帐户中所有案例的必需访问权。您只能查看您邀请到帐户中的用户、与之共享 Cloud Foundry 组织成员资格的用户，或者位于您的经典基础架构用户层次结构中的用户。
{: tsCauses}

除了支持中心帐户管理服务访问策略之外，必须为您分配对用户管理帐户管理服务的至少具有“查看者”角色的 IAM 策略。要查看当前访问权，请转至**管理** &gt; **访问权 (IAM)**，然后从**用户**页面中选择您的名称。单击**访问策略**选项卡，然后复审分配的策略。
{: tsResolve}

要解决此问题，请与帐户所有者联系以请求相应的访问权。 

## 为什么我找不到先前创建的案例？ 
{: #ts_viewarchivedcase}

您无法查找在增强 {{site.data.keyword.Bluemix_notm}} 平台体验之前创建的案例。
{:shortdesc}

在转至支持中心的**管理案例**选项卡后，即无法查找在 2018 年 12 月 2 日之前创建的任何案例。
{: tsSymptoms}

2018 年 12 月 2 日之前打开的案例仅在**查看归档案例**中显示。
{: tsCauses}

要查看您的案例，请转至**支持**，选择**管理案例**，然后单击**查看归档案例**。
{: tsResolve} 






