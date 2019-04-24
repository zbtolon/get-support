---

copyright:

  years: 2015, 2019

lastupdated: "2019-01-29"

keywords: create case, manage case, open case, start case, ticket

subcollection: get-support

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# サポート Case の処理 
{: #open-case}

{{site.data.keyword.Bluemix}} で問題が発生した場合、サポート Case を使用して、技術的、アカウントとアクセス権限、請求と請求書、または販売の問い合わせの各問題に関する支援を受けることができます。 [サポート・センター](https://dev.console.cloud.ibm.com/unifiedsupport/supportcenter){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン") を使用して、サポート Case の作成および管理を行えます。 サポート Case を送信すると、サポート・チームがサポート・プランのタイプに応じて問題の調査と解決を行います。
{:shortdesc}

デフォルトでは、アカウント内のユーザーは、Case を作成、更新、検索、表示するためのアクセス権限はいずれも持っていません。 アカウント所有者は、Identity and Access Management (IAM) アクセス・ポリシーを割り当てることによって、ユーザーにアクセス権限を提供する必要があります。 詳しくは、[サポート Case を処理するためのユーザー・アクセスの割り当て](/docs/get-support?topic=get-support-access#access)を参照してください。
{:tip}

## サポート Case の作成
{: #opentechcase}

すべてのユーザーが任意のタイプのサポート Case をオープンできます。

デフォルトでは、アカウント内のユーザーは、Case を作成、更新、検索、表示するためのアクセス権限はいずれも持っていません。 Identity and Access Management (IAM) アクセス・ポリシーを割り当てることによって、ユーザーにアクセス権限を提供する必要があります。 詳しくは、[プラットフォーム管理の役割](/docs/iam?topic=iam-platformroles#platformroles)を参照してください。
{:tip}

サポート・センターからサポート Case を作成するには、以下のステップを実行します。 

  1. コンソールのメニュー・バーから**「サポート」**をクリックします。
  2. **「お困りですか? (Need more help)」** メニューで **「Case の作成 (Create case)」** をクリックするか、**「Case の管理 (Manage cases)」 > 「新規 Case の作成 (Create a new case)」** をクリックして Case を作成します。
  3. 問題に応じて、**「技術的」**、**「アカウントとアクセス権限 (Account & Access)」**、**「請求と請求書 (Billing & Invoice)」**、または**「販売の問い合わせ (Sales Inquiry)」**を選択します。
  4. 次に、メニューから Case の重大度を選択します。 重大度によって Case の処理方法が決まります。 Case 重大度について詳しくは、[サポート Case のエスカレート](/docs/get-support?topic=get-support-escalation#escalation)を参照してください。
  5. Case のカテゴリーとオファリングを選択します。 必要な情報は、選択したリソース・コンテキストのほか、アカウントのサポート・プランのタイプによっても異なります。
  6. Case の件名と説明に必要な情報を入力します。 
  
    発生している問題に関する詳細を示すことができるファイルを添付できます。
    {: tip}
  7. **「送信」**をクリックします。 E メール通知を受信したら、問題に関するさらなるやり取りについての指示に従います。 

### Case でサポートされるファイル・タイプ 
{: #supported-file-types}

Case の作成時には、ファイルを添付するオプションがあり、特定のファイル・タイプのみがサポートされます。 

以下のファイル・タイプがサポートされます。 

```
7z, ace, ams, arm, asp, bash, history, bkp, big, bmp, bz2, ca, ca-bundle, ca-crt, cabundle, cap, cer, cert, cfg, cnf, crt, csr, csv, dat, dbs, debug, dib, dmesg, dmp, doc, docx, dotx, dump, email, eml, emz, env, eps, error, evt, evtx, fragment, gif, gz, gz_aa, gz_ab, gz_ac, har, hosts, htaccess, html, iaf, ics, id, img, info, jpb, jpe, jpeg, jpg, key, lic, log, logsm lon02, lst, lzh, mai, md5, mib, mjpg, msg, mso, odp, ods, odt, oft, openssh, out, ovf, ovpn, p7b, p7s, pages, pcap, pcf, pcx, pdb, pem, pfx, pic, pix, png, ppk, ppt, pptx, psd, psp, pspimage, pub_key, rar, raw, rdp, req, rpt, rtf, sjc03-raid-2, sjc03-raid-log-1, snag, sql, ssh, stats, sth, svg, sxc, tar, targz, tbz2, tcpdump, text, tgz, tgz-aa, tgz-ab, tgz-ac, tgz-ad, tgz-ae, tgz-af, tgz-ag, tgz-ah, tgz-ai, tgz-aj, tgz-ak, tgz-ak, tgz-al, tgz-al, tgz-am, tif, tiff, tip, trace, tsv, txt, ufo, vcf, vdx, vsdx, webarchive, wml, wps, wpz, wrf, wri, xcf, xlog, xlr, xls, xis, xism, xisx, xit, xml, xpm, xps, xslic, xz, yaml, zip, zipaa, zipx, zone
```
{: screen}

## サポート Case の管理 
{: #check-case-status}

お客様のサポートに関する問題はすべてサポート Case に文書化されます。 各サポート Case には、参照用の固有の Case 番号と、 Case 説明に記述された詳細に基づく重大度レベルが割り当てられます。 この Case 番号を使用して、サポート Case の進行状況を確認したり、サポート Case を更新したりできます。 Case の更新および返答は E メールで送信され、Case のメモに記録されます。 

サポート Case を表示および管理するには、以下の手順を使用します。

  1. コンソールのメニュー・バーから**「サポート」**をクリックします。
  2. オープンされた Case のリストを表示するには、**「Case の管理 (Manage cases)」**を選択します。
  3. リストから Case を選択して、コメントを追加したり、Case を更新したりします。
  4. クローズ済みや解決済みの Case は、あらゆる状況の Case を取り出すフィルター・オプションを使用して検出できます。 

クラシック・インフラストラクチャー・ユーザーで、以前の Case のリストが表示されない場合は、**「アーカイブされた Case の表示」**にアクセスしてください。 
{: tip}

