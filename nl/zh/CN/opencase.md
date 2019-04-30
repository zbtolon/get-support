---

copyright:

  years: 2015, 2019

lastupdated: "2019-04-18"

keywords: create case, manage case, open case, start case, ticket

subcollection: get-support

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 处理支持案例 
{: #open-case}

如果您遇到 {{site.data.keyword.Bluemix}} 问题，那么可以使用支持案例来获取技术、帐户和访问权、计费和发票或者销售查询问题的帮助。您可以使用[支持中心](https://dev.console.cloud.ibm.com/unifiedsupport/supportcenter){: new_window} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标") 来创建和管理支持案例。在提交支持案例之后，支持团队会根据您的支持套餐类型来进行调查并解决问题。
{:shortdesc}

缺省情况下，帐户中的用户无权创建、更新、搜索或查看案例。作为帐户所有者，您必须通过分配 Identity and Access Management (IAM) 访问策略来向用户提供访问权。有关更多信息，请参阅[分配用于处理支持案例的用户访问权](/docs/get-support?topic=get-support-access#access)
{:tip}

## 创建支持案例
{: #opentechcase}

所有用户都可以打开任何类型的支持案例。

缺省情况下，帐户中的用户无权创建、更新、搜索或查看案例。您必须通过分配 Identity and Access Management (IAM) 访问策略来向用户提供访问权。有关更多信息，请参阅[平台管理角色](/docs/iam?topic=iam-userroles#platformroles)。
{:tip}

要从支持中心创建支持案例，请完成下列步骤： 

  1. 在控制台菜单栏中，单击**支持**。
  2. 通过单击**需要更多帮助**菜单中的**创建案例**或者单击**管理案例 > 创建新案例**来创建案例。
  3. 根据您的问题，选择**技术**、**帐户和访问权**、**计费和发票**或**销售查询**。
  4. 接下来，从菜单中选择案例的严重性。严重性将决定案例的处理方式。有关案例严重性的更多信息，请参阅[上报支持案例](/docs/get-support?topic=get-support-escalation#escalation)。
  5. 选择案例的类别和产品。必需的信息取决于您所选的资源上下文，还取决于您帐户的支持套餐类型。
  6. 填写案例的主题和描述所需的信息。 
  
    您可以附加文件以提供有关您遇到的问题的更多详细信息。
    {: tip}
  7. 单击**提交**。在收到电子邮件通知时，请按照指示信息就该问题作进一步的沟通。 

### 支持的案例文件类型 
{: #supported-file-types}

在创建案例时，可以选择附加文件，仅支持某些文件类型。 

支持以下文件类型： 

```
7z、ace、ams、arm、asp、bash、history、bkp、big、bmp、bz2、ca、ca-bundle、ca-crt、cabundle、cap、cer、cert、cfg、cnf、crt、csr、csv、dat、dbs、debug、dib、dmesg、dmp、doc、docx、dotx、dump、email、eml、emz、env、eps、error、evt、evtx、fragment、gif、gz、gz_aa、gz_ab、gz_ac、har、hosts、htaccess、html、iaf、ics、id、img、info、jpb、jpe、jpeg、jpg、key、lic、log、logsm lon02、lst、lzh、mai、md5、mib、mjpg、msg、mso、odp、ods、odt、oft、openssh、out、ovf、ovpn、p7b、p7s、pages、pcap、pcf、pcx、pdb、pem、pfx、pic、pix、png、ppk、ppt、pptx、psd、psp、pspimage、pub_key、rar、raw、rdp、req、rpt、rtf、sjc03-raid-2、sjc03-raid-log-1、snag、sql、ssh、stats、sth、svg、sxc、tar、targz、tbz2、tcpdump、text、tgz、tgz-aa、tgz-ab、tgz-ac、tgz-ad、tgz-ae、tgz-af、tgz-ag、tgz-ah、tgz-ai、tgz-aj、tgz-ak、tgz-ak、tgz-al、tgz-al、tgz-am、tif、tiff、tip、trace、tsv、txt、ufo、vcf、vdx、vsdx、webarchive、wml、wps、wpz、wrf、wri、xcf、xlog、xlr、xls、xis、xism、xisx、xit、xml、xpm、xps、xslic、xz、yaml、zip、zipaa、zipx、zone
```
{: screen}

## 管理支持案例 
{: #check-case-status}

所有客户支持问题都记录在支持案例中。每个支持案例都会分配有唯一的案例号以方便查询，还会根据案例描述中的详细信息分配严重性级别。可以使用案例号来查看支持案例的进度以及更新支持案例。
案例更新和响应会通过电子邮件发送给您并记录在案例说明中。 

要查看并管理支持案例，请使用以下步骤：

  1. 在控制台菜单栏中，单击**支持**。
  2. 要查看已提交案例的列表，请选择**管理案例**。
  3. 从列表中选择案例以添加注释或更新案例。
  4. 通过使用过滤器选项来检索任何状态的案例，可以找到已关闭或已解决的案例。 

如果您是经典基础架构用户，并且看不到先前案例的列表，请转至**查看归档案例**。
{: tip}

