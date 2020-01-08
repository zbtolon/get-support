---

copyright:

  years: 2015, 2020

lastupdated: "2020-01-08"

keywords: create case, manage case, open case, start case, ticket, customer success, supported file types, file types, manage case, archived case 

subcollection: get-support

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Working with support cases 
{: #open-case}

If you experience problems with {{site.data.keyword.Bluemix}}, you can use support cases to get help with technical, access (IAM), billing & usage, and invoice or sales inquiry issues. You can create and manage a support case by using the [Support Center](https://cloud.ibm.com/unifiedsupport/supportcenter){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon"). After you submit a support case, the support team works to investigate and resolve the issue depending on your type of support plan.
{:shortdesc}

By default, users in an account don't have access to create, update, search, or view cases. As the account owner, you must provide users access by assigning an Identity and Access Management (IAM) access policy. For more information, see [Assigning user access for working with support cases](/docs/get-support?topic=get-support-access#access)
{:tip}

## Creating support cases
{: #opentechcase}

All users can open a support case, but lite accounts can't open technical support cases. Technical support for lite accounts is provided by the IBM Cloud docs and the online community. 

By default, users in an account don't have access to create, update, search, or view cases. You must provide users access by assigning an Identity and Access Management (IAM) access policy. For more information, see [Platform management roles](/docs/iam?topic=iam-userroles#platformroles)
{:tip}

Complete the following steps to create a support case from the Support Center: 

  1. Click **Support** from the console menu bar.
  2. Create a case by going to the **Still need help** section, and clicking **Create case**. You can also create a case by clicking **View all open cases**. After you are directed to the **Manage cases** page, click **Create new case**. 
  3. Select the type of issue that you need help with. All users have the choice of choosing **Access (IAM)**, **Account**, **Billing & Usage**, or **Customer success**. Other options are available based on what you have provisioned in the catalog or the level of support on the account.  
  4. Next, choose the business impact by selecting the severity of your case. The severity determines how your case is handled. For more information on case severity, see [Escalating support cases](/docs/get-support?topic=get-support-escalation#escalation).
  5. Complete the required information for the subject and description of the case. 
  
    You can attach files that can provide more details about the issue you're experiencing.
    {: tip}
  6. You can add another user to the case if the user is in the account. For more information, see [Adding users to your case management access group](/docs/get-support?topic=get-support-access#add-user-access-group).
  7. Select **Email me updates about this case** to receive notifications about the case. 
  6. Click **Create**. When you receive an email notification, follow the instructions for further communication on the issue. 

### Supported file types for cases 
{: #supported-file-types}

When you create a case, you have the option of attaching a file and only certain file types are supported. The following file types are supported: 

```
7z, ace, ams, arm, asp, bash, history, bkp, big, bmp, bz2, ca, ca-bundle, ca-crt, cabundle, cap, cer, cert, cfg, cnf, crt, csr, csv, dat, dbs, debug, dib, dmesg, dmp, doc, docx, dotx, dump, email, eml, emz, env, eps, error, evt, evtx, fragment, gif, gz, gz_aa, gz_ab, gz_ac, har, hosts, htaccess, html, iaf, ics, id, img, info, jpb, jpe, jpeg, jpg, key, lic, log, logsm lon02, lst, lzh, mai, md5, mib, mjpg, msg, mso, odp, ods, odt, oft, openssh, out, ovf, ovpn, p7b, p7s, pages, pcap, pcf, pcx, pdb, pem, pfx, pic, pix, png, ppk, ppt, pptx, psd, psp, pspimage, pub_key, rar, raw, rdp, req, rpt, rtf, sjc03-raid-2, sjc03-raid-log-1, snag, sql, ssh, stats, sth, svg, sxc, tar, targz, tbz2, tcpdump, text, tgz, tgz-aa, tgz-ab, tgz-ac, tgz-ad, tgz-ae, tgz-af, tgz-ag, tgz-ah, tgz-ai, tgz-aj, tgz-ak, tgz-ak, tgz-al, tgz-al, tgz-am, tif, tiff, tip, trace, tsv, txt, ufo, vcf, vdx, vsdx, webarchive, wml, wps, wpz, wrf, wri, xcf, xlog, xlr, xls, xis, xism, xisx, xit, xml, xpm, xps, xslic, xz, yaml, zip, zipaa, zipx, zone
```
{: screen}

## Managing your support cases 
{: #check-case-status}

All client support issues are documented in support cases. Each support case is assigned a unique case number for reference and a severity level based on the details in the case description. You can use the case number to review your support case progress and update the support case. Updates to your cases and responses are sent to you by email and recorded in the case notes. 

To view and manage your support cases, use the following steps:

  1. Click **Support** from the console menu bar.
  2. To view a listing of open cases, select **Manage cases**.
  3. Select a case from the list to add comments or update a case. You can also add users that are in the account to a watchlist so they can receive alerts about a case.
  4. You can find closed or resolved cases by using the filter option to retrieve cases in any status. 

If you're a classic infrastructure user, and you don't see a listing of a previous case, go to **View archived cases**. 
{: tip}
