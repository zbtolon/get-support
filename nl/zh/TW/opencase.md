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

# 使用支援案例 
{: #open-case}

如果您遇到 {{site.data.keyword.Bluemix}} 問題，可以使用支援案例來取得有關技術、帳戶及存取、計費及發票或銷售查詢問題的協助。您可以使用[支援中心 ](https://dev.console.cloud.ibm.com/unifiedsupport/supportcenter){: new_window}![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示") 來建立及管理支援案例。在提交支援案例之後，支援團隊會根據您的支援方案類型來調查及解決問題。
{:shortdesc}

依預設，帳戶中的使用者無權建立、更新、搜尋或檢視案例。身為帳戶擁有者，您必須指派 Identity and Access Management (IAM) 存取原則來提供使用者存取權。如需相關資訊，請參閱[指派使用者存取權以便使用支援案例](/docs/get-support?topic=get-support-access#access)。
{:tip}

## 建立支援案例
{: #opentechcase}

所有使用者都可以開立任何類型的支援案例。

依預設，帳戶中的使用者無權建立、更新、搜尋或檢視案例。您必須指派 Identity and Access Management (IAM) 存取原則來提供使用者存取權。如需相關資訊，請參閱[平台管理角色](/docs/iam?topic=iam-platformroles#platformroles)。
{:tip}

請完成下列步驟，從「支援中心」建立支援案例： 

  1. 從主控台功能表列按一下**支援**。
  2. 從**需要更多協助**功能表按一下**建立案例**，或按一下**管理案例 > 建立新的案例**，來建立案例。
  3. 根據您的問題，選取**技術**、**帳戶 & 存取**、**計費 & 發票**或**銷售查詢**。
  4. 接下來，從功能表選擇案例的嚴重性。嚴重性會決定案例的處理方式。如需案例嚴重性的相關資訊，請參閱[呈報支援案例](/docs/get-support?topic=get-support-escalation#escalation)。
  5. 選取案例的種類及供應項目。所需的資訊取決於您選取的資源環境定義，另外也取決於您帳戶的支援方案類型。
  6. 填妥案例主旨和說明的必要資訊。 
  
    您可以附加檔案，以提供所遭遇問題的更多詳細資料。
    {: tip}
  7. 按一下**提交**。當您收到電子郵件通知時，請遵循指示，針對該問題進行進一步的溝通。 

### 案例的支援檔案類型 
{: #supported-file-types}

當您建立案例時可以選擇附加檔案，且只有支援特定檔案類型。 

系統支援下列檔案類型： 

```
7z, ace, ams, arm, asp, bash, history, bkp, big, bmp, bz2, ca, ca-bundle, ca-crt, cabundle, cap, cer, cert, cfg, cnf, crt, csr, csv, dat, dbs, debug, dib, dmesg, dmp, doc, docx, dotx, dump, email, eml, emz, env, eps, error, evt, evtx, fragment, gif, gz, gz_aa, gz_ab, gz_ac, har, hosts, htaccess, html, iaf, ics, id, img, info, jpb, jpe, jpeg, jpg, key, lic, log, logsm lon02, lst, lzh, mai, md5, mib, mjpg, msg, mso, odp, ods, odt, oft, openssh, out, ovf, ovpn, p7b, p7s, pages, pcap, pcf, pcx, pdb, pem, pfx, pic, pix, png, ppk, ppt, pptx, psd, psp, pspimage, pub_key, rar, raw, rdp, req, rpt, rtf, sjc03-raid-2, sjc03-raid-log-1, snag, sql, ssh, stats, sth, svg, sxc, tar, targz, tbz2, tcpdump, text, tgz, tgz-aa, tgz-ab, tgz-ac, tgz-ad, tgz-ae, tgz-af, tgz-ag, tgz-ah, tgz-ai, tgz-aj, tgz-ak, tgz-ak, tgz-al, tgz-al, tgz-am, tif, tiff, tip, trace, tsv, txt, ufo, vcf, vdx, vsdx, webarchive, wml, wps, wpz, wrf, wri, xcf, xlog, xlr, xls, xis, xism, xisx, xit, xml, xpm, xps, xslic, xz, yaml, zip, zipaa, zipx, zone
```
{: screen}

## 管理支援案例 
{: #check-case-status}

支援案例中會記載所有用戶端支援問題。每個支援案例都會獲指派一個用於參照的唯一案例號碼，以及一個以案例說明中的詳細資料為基礎的嚴重性層次。您可以使用案例號碼來檢閱支援案例進度，以及更新支援案例。案例更新及回應會透過電子郵件傳送給您，並且記錄在案例注意事項中。 

若要檢視及管理支援案例，請使用下列步驟：

  1. 從主控台功能表列按一下**支援**。
  2. 若要檢視開立案例的清單，請選取**管理案例**。
  3. 從清單選取一個案例，以新增註解或更新案例。
  4. 使用過濾選項來擷取處於任何狀態的案例，即可找到已關閉或已解決的案例。 

如果您是標準基礎架構使用者，而且未看到先前案例的清單，請移至**檢視保存的案例**。
{: tip}

