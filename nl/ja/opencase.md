---

copyright:

  years: 2015, 2018

lastupdated: "2018-11-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# サポート・ケースの処理 
{: #open-case}

{{site.data.keyword.Bluemix}} で問題が発生した場合、サポート・ケースを使用して、技術的、アカウントとアクセス権限、請求と請求書、または販売の問い合わせの各問題に関する支援を受けることができます。 [サポート・センター](https://dev.console.cloud.ibm.com/unifiedsupport/supportcenter){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン") を使用して、サポート・ケースの作成および管理を行えます。 サポート・ケースを送信すると、サポート・チームがサポート・プランのタイプに応じて問題の調査と解決を行います。
{:shortdesc}

デフォルトでは、アカウント内のユーザーは、ケースを作成、更新、検索、表示するためのアクセス権限はいずれも持っていません。 アカウント所有者は、Identity and Access Management (IAM) アクセス・ポリシーを割り当てることによって、ユーザーにアクセス権限を提供する必要があります。 詳しくは、[サポート・ケースを処理するためのユーザー・アクセスの割り当て](/docs/get-support/support_access.html#access)を参照してください。
{:tip}

## サポート・ケースの作成
{: #opentechcase}

すべてのユーザーが任意のタイプのサポート・ケースをオープンできます。

サポート・センターからサポート・ケースを作成するには、以下のステップを実行します。 

  1. コンソールのメニュー・バーから**「サポート」**をクリックします。
  2. **「お困りですか? (Need more help)」** メニューで **「ケースの作成 (Create case)」** をクリックするか、**「ケースの管理 (Manage cases)」 > 「新規ケースの作成 (Create a new case)」** をクリックしてケースを作成します。
  3. 問題に応じて、**「技術的」**、**「アカウントとアクセス権限 (Account & Access)」**、**「請求と請求書 (Billing & Invoice)」**、または**「販売の問い合わせ (Sales Inquiry)」**を選択します。
  4. 次に、メニューからケースの重大度を選択します。 重大度によってケースの処理方法が決まります。 ケース重大度について詳しくは、[サポート・ケースのエスカレート](/docs/get-support/quick-case-response.html#escalation)を参照してください。
  5. ケースのカテゴリーとオファリングを選択します。 必要な情報は、選択したリソース・コンテキストのほか、アカウントのサポート・プランのタイプによっても異なります。
  6. ケースの件名と説明に必要な情報を入力します。 
  
    発生している問題に関する詳細を示すことができるファイルを添付できます。
    {: tip}
  7. **「送信」**をクリックします。 E メール通知を受信したら、問題に関するさらなるやり取りについての指示に従います。 

デフォルトでは、アカウント内のユーザーは、ケースを作成、更新、検索、表示するためのアクセス権限はいずれも持っていません。 Identity and Access Management (IAM) アクセス・ポリシーを割り当てることによって、ユーザーにアクセス権限を提供する必要があります。 詳しくは、[プラットフォーム管理の役割](/docs/iam/users_roles.html#platformrolestable2)を参照してください。{:tip}

### ケースでサポートされるファイル・タイプ 
{: #supported-file-types}

ケースの作成時には、ファイルを添付するオプションがあり、特定のファイル・タイプのみがサポートされます。 

以下のファイル・タイプがサポートされます。7z、ace、ams、arm、asp、bash、history、bkp、big、bmp、bz2、ca、ca-bundle、ca-crt、cabundle、cap、cer、cert、cfg、cnf、crt、csr、csv、dat、dbs、debug、dib、dmesg、dmp、doc、docx、dotx、dump、email、eml、emz、env、eps、error、log、evt、evtx、fragment、gif、gz、gz_aa、gz_ab、gz_ac、har、hosts、htaccess、html、iaf、ics、id、img、info、jpb、jpe、jpeg、jpg、key、lic、log、logsm lon02、lst、lzh、mai、md5、mib、mjpg、msg、mso、odp、ods、odt、oft、openssh、out、ovf、ovpn、p7b、p7s、pages、pcap、pcf、pcx、pdb、pem、pfx、pic、pix、png、ppk、ppt、pptx、psd、psp、pspimage、pub_key、rar、raw、rdp、req、rpt、rtf、sjc03-raid-2、sjc03-raid-log-1、snag、sql、ssh、stats、sth、svg、sxc、tar、targz、tbz2、tcpdump、text、tgz、tgz-aa、tgz-ab、tgz-ac、tgz-ad、tgz-ae、tgz-af、tgz-ag、tgz-ah、tgz-ai、tgz-aj、tgz-ak、tgz-ak、tgz-al、tgz-al、tgz-am、tif、tiff、tip、trace、tsv、txt、ufo、vcf、vdx、vsdx、webarchive、wml、wps、wpz、wrf、wri、xcf、xlog、xlr、xls、xis、xism、xisx、xit、xml、xpm、xps、xslic、xz、yaml、zip、zipaa、zipx、zone。 

## サポート・ケースの管理 
{: #check-case-status}

お客様のサポートに関する問題はすべてサポート・ケースに文書化されます。 各サポート・ケースには、参照用の固有のケース番号と、ケース説明に記述された詳細に基づく重大度レベルが割り当てられます。 このケース番号を使用して、サポート・ケースの進行状況を確認したり、サポート・ケースを更新したりできます。 ケースの更新および返答は E メールで送信され、ケースのメモに記録されます。 

サポート・ケースを表示および管理するには、以下の手順を使用します。

  1. コンソールのメニュー・バーから**「サポート」**をクリックします。
  2. オープン・ケースのリストを表示するには、**「ケースの管理 (Manage cases)」**を選択します。
  3. リストからケースを選択して、コメントを追加したり、ケースを更新したりします。 
  4. 前のケースのリストを表示するには、**「アーカイブ済みケースの表示 (View archived cases)」**を選択します。 
