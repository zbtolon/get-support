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

# Mit Supportfällen arbeiten 
{: #open-case}

Wenn Probleme mit {{site.data.keyword.Bluemix}} auftreten, können Sie Supportfälle verwenden, um Hilfe bei technischen Fragen sowie bei Problemen mit dem Konto und dem Zugriff, mit Abrechnung und Rechnungen oder mit Verkaufsanfragen zu erhalten. Sie können Supportfälle mithilfe des [Support Centers](https://dev.console.cloud.ibm.com/unifiedsupport/supportcenter){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") erstellen und verwalten. Nachdem Sie einen Supportfall eingereicht haben, arbeitet das Support-Team je nach Ihrem Supportplantyp an der Untersuchung und Lösung des Problems.
{:shortdesc}

Standardmäßig haben Benutzer in einem Konto keinen Zugriff zum Erstellen, Aktualisieren, Suchen oder Anzeigen von Fällen. Als Kontoeigner müssen Sie Benutzern erst Zugriff gewähren, indem Sie eine IAM-Zugriffsrichtlinie (IAM, Identitäts- und Zugriffsmanagement) zuweisen. Weitere Informationen zu diesem Thema finden Sie in [Benutzerzugriff für die Arbeit mit Supportfällen zuweisen](/docs/get-support?topic=get-support-access#access).
{:tip}

## Supportfälle erstellen
{: #opentechcase}

Alle Benutzer können einen beliebigen Supportfalltyp öffnen.

Standardmäßig haben Benutzer in einem Konto keinen Zugriff zum Erstellen, Aktualisieren, Suchen oder Anzeigen von Fällen. Sie müssen Benutzern erst Zugriff gewähren, indem Sie eine IAM-Zugriffsrichtlinie (IAM, Identitäts- und Zugriffsmanagement) zuweisen. Weitere Informationen finden Sie unter [Plattformmanagementrollen](/docs/iam?topic=iam-userroles#platformroles)
{:tip}

Führen Sie die folgenden Schritte aus, um einen Supportfall im Support Center zu erstellen: 

  1. Klicken Sie in der Menüleiste der Konsole auf **Support**.
  2. Erstellen Sie einen Fall, indem Sie im Menü **Sie benötigen weitere Hilfe?** auf **Fall erstellen** klicken oder indem Sie auf **Fälle verwalten > Neuen Fall erstellen** klicken.
  3. Wählen Sie abhängig von Ihrem Problem **Technisch**, **Konto & Zugriff**, **Abrechnung & Rechnung** oder **Verkaufsanfragen** aus.
  4. Wählen Sie als nächstes die Priorität Ihres Falls im Menü aus. Die Priorität bestimmt, wie Ihr Fall verarbeitet wird. Weitere Informationen zur Priorität von Fällen finden Sie in [Supportfälle eskalieren](/docs/get-support?topic=get-support-escalation#escalation).
  5. Wählen Sie die Kategorie und das Angebot Ihres Falls aus. Welche Informationen benötigt werden, richtet sich nach dem von Ihnen ausgewählten Ressourcenkontext sowie nach dem Typ des Supportplans für Ihr Konto.
  6. Füllen Sie die erforderlichen Informationen für das Thema und die Beschreibung des Falls aus. 
  
    Sie können Dateien anhängen, die mehr Details zu dem Thema, das Sie gerade beschäftigt, bereitstellen können.
    {: tip}
  7. Klicken Sie auf **Abschicken**. Wenn Sie eine E-Mail-Benachrichtigung erhalten, befolgen Sie die Anweisungen für die weitere Kommunikation zu diesem Thema. 

### Unterstützte Dateitypen für Fälle 
{: #supported-file-types}

Wenn Sie einen Fall erstellen, haben Sie die Möglichkeit, eine Datei anzuhängen, wobei nur bestimmte Dateitypen unterstützt werden. 

Die folgenden Dateitypen werden unterstützt: 

```
7z, ace, ams, arm, asp, bash, history, bkp, big, bmp, bz2, ca, ca-bundle, ca-crt, cabundle, cap, cer, cert, cfg, cnf, crt, csr, csv, dat, dbs, debug, dib, dmesg, dmp, doc, docx, dotx, dump, email, eml, emz, env, eps, error, evt, evtx, fragment, gif, gz, gz_aa, gz_ab, gz_ac, har, hosts, htaccess, html, iaf, ics, id, img, info, jpb, jpe, jpeg, jpg, key, lic, log, logsm lon02, lst, lzh, mai, md5, mib, mjpg, msg, mso, odp, ods, odt, oft, openssh, out, ovf, ovpn, p7b, p7s, pages, pcap, pcf, pcx, pdb, pem, pfx, pic, pix, png, ppk, ppt, pptx, psd, psp, pspimage, pub_key, rar, raw, rdp, req, rpt, rtf, sjc03-raid-2, sjc03-raid-log-1, snag, sql, ssh, stats, sth, svg, sxc, tar, targz, tbz2, tcpdump, text, tgz, tgz-aa, tgz-ab, tgz-ac, tgz-ad, tgz-ae, tgz-af, tgz-ag, tgz-ah, tgz-ai, tgz-aj, tgz-ak, tgz-ak, tgz-al, tgz-al, tgz-am, tif, tiff, tip, trace, tsv, txt, ufo, vcf, vdx, vsdx, webarchive, wml, wps, wpz, wrf, wri, xcf, xlog, xlr, xls, xis, xism, xisx, xit, xml, xpm, xps, xslic, xz, yaml, zip, zipaa, zipx, zone
```
{: screen}

## Supportfälle verwalten 
{: #check-case-status}

Alle Supportprobleme von Kunden werden in Supportfällen dokumentiert. Jedem Supportfall wird zu Referenzzwecken eine eindeutige Fallnummer sowie eine Prioritätsstufe auf der Basis der in der Fallbeschreibung enthaltenen Details zugewiesen. Sie können die Fallnummer verwenden, um den Fortschritt Ihres Supportfalls zu überprüfen und den Supportfall zu aktualisieren. Aktualisierungen an Ihren Fällen und Antworten werden per E-Mail an Sie gesendet und in den Fallnotizen aufgezeichnet. 

Führen Sie die folgenden Schritte aus, um Ihre Supportfälle anzuzeigen und zu verwalten:

  1. Klicken Sie in der Menüleiste der Konsole auf **Support**.
  2. Um eine Auflistung offener Fälle anzuzeigen, wählen Sie **Fälle verwalten** aus.
  3. Wählen Sie einen Fall aus der Liste aus, um Kommentare hinzuzufügen oder einen Fall zu aktualisieren.
  4. Abgeschlossene oder gelöste Fälle können gesucht werden, indem Sie Fälle mit beliebigem Status unter Verwendung der Filteroption abrufen. 

Wenn Sie ein Benutzer der klassischen Infrastruktur sind und ein vorheriger Fall nicht in der Auflistung aufgeführt wird, verwenden Sie die Option **Archivierte Fälle anzeigen**. 
{: tip}

