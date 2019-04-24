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

# Utilisation de cas de support 
{: #open-case}

Si vous rencontrez des problèmes avec {{site.data.keyword.Bluemix}}, vous pouvez utiliser des cas de support pour obtenir de l'aide concernant des problèmes techniques, de compte et d'accès, de facturation et de factures ou des demandes d'informations commerciales. Vous pouvez créer et gérer un cas de support en utilisant le [Centre de support](https://dev.console.cloud.ibm.com/unifiedsupport/supportcenter){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe"). Une fois que vous avez soumis un cas de support, l'équipe de support travaille à l'étude et à la résolution du problème en fonction de votre type de plan de support.
{:shortdesc}

Par défaut, les utilisateurs d'un compte n'ont pas accès à la création, la mise à jour, la recherche ou la consultation de cas. En tant que propriétaire du compte, vous devez fournir aux utilisateurs un accès en attribuant une règle d'accès IAM (Identity and Access Management). Pour plus d'informations, voir [Attribution d'accès utilisateur pour l'utilisation de cas de support](/docs/get-support?topic=get-support-access#access).
{:tip}

## Création de cas de support
{: #opentechcase}

Tous les utilisateurs peuvent ouvrir n'importe quel type de cas de support.

Par défaut, les utilisateurs d'un compte n'ont pas accès à la création, la mise à jour, la recherche ou la consultation de cas. Vous devez fournir aux utilisateurs un accès en attribuant une règle d'accès IAM (Identity and Access Management). Pour plus d'informations, voir [Rôles de gestion de plateforme](/docs/iam?topic=iam-platformroles#platformroles).
{:tip}

Effectuez les étapes suivantes pour créer un cas de support à partir du Centre de support : 

  1. Cliquez sur **Support** dans la barre de menus de la console.
  2. Créez un cas en cliquant sur **Créer un cas** dans le menu **Besoin d'aide ?** ou en cliquant sur **Gérer les cas > Créer un cas**.
  3. Sélectionnez **Technique**, **Compte & Accès**, **Facturation & Factures** ou **Demande de vente** en fonction de votre problème.
  4. Ensuite, choisissez la gravité de votre cas dans le menu. La gravité détermine la manière dont votre cas est traité. Pour plus d'informations sur la gravité des cas, voir [Escalade de cas de support](/docs/get-support?topic=get-support-escalation#escalation).
  5. Sélectionnez la catégorie et l'offre de votre cas. Les informations requises dépendent du contexte de ressources que vous avez sélectionné, ainsi que du type de plan de support de votre compte.
  6. Complétez les informations requises pour l'objet et la description du cas. 
  
    Vous pouvez joindre des fichiers pouvant fournir plus de détails sur le problème rencontré.
    {: tip}
  7. Cliquez sur **Soumettre**. Lorsque vous recevez une notification par courrier électronique, suivez les instructions pour toute communication ultérieure sur le problème. 

### Types de fichiers pris en charge pour les cas 
{: #supported-file-types}

Lorsque vous créez un cas, vous avez la possibilité de joindre un fichier et seuls certains types de fichiers sont pris en charge. 

Les types de fichier suivants sont pris en charge : 

```
7z, ace, ams, arm, asp, bash, history, bkp, big, bmp, bz2, ca, ca-bundle, ca-crt, cabundle, cap, cer, cert, cfg, cnf, crt, csr, csv, dat, dbs, debug, dib, dmesg, dmp, doc, docx, dotx, dump, email, eml, emz, env, eps, error, log, evt, evtx, fragment, gif, gz, gz_aa, gz_ab, gz_ac, har, hosts, htaccess, html, iaf, ics, id, img, info, jpb, jpe, jpeg, jpg, key, lic, log, logsm lon02, lst, lzh, mai, md5, mib, mjpg, msg, mso, odp, ods, odt, oft, openssh, out, ovf, ovpn, p7b, p7s, pages, pcap, pcf, pcx, pdb, pem, pfx, pic, pix, png, ppk, ppt, pptx, psd, psp, pspimage, pub_key, rar, raw, rdp, req, rpt, rtf, sjc03-raid-2, sjc03-raid-log-1, snag, sql, ssh, stats, sth, svg, sxc, tar, targz, tbz2, tcpdump, text, tgz, tgz-aa, tgz-ab, tgz-ac, tgz-ad, tgz-ae, tgz-af, tgz-ag, tgz-ah, tgz-ai, tgz-aj, tgz-ak, tgz-ak, tgz-al, tgz-al, tgz-am, tif, tiff, tip, trace, tsv, txt, ufo, vcf, vdx, vsdx, webarchive, wml, wps, wpz, wrf, wri, xcf, xlog, xlr, xls, xis, xism, xisx, xit, xml, xpm, xps, xslic, xz, yaml, zip, zipaa, zipx, zone.
```
{: screen}

## Gestion des cas de support 
{: #check-case-status}

Tous les problèmes de support client sont documentés dans des cas de support. A chaque cas de support sont associés un numéro de référence unique et un niveau de gravité basé sur les détails contenus dans la description du cas. Vous pouvez utiliser le cas de support pour suivre sa progression et le mettre à jour. Les mises à jour de vos cas et les réponses vous sont adressées par e-mail et sont enregistrées dans les notes sur le cas. 

Pour examiner et gérer vos cas de support, procédez comme suit :

  1. Cliquez sur **Support** dans la barre de menus de la console.
  2. Pour afficher une liste des cas ouverts, sélectionnez **Gérer les cas**.
  3. Sélectionnez un cas dans la liste pour ajouter des commentaires ou mettre à jour un cas.
  4. Les cas fermés ou résolus sont disponibles en utilisant l'option de filtrage permettant d'extraire les cas, quel que soit leur statut. 

Si vous êtes un utilisateur d'infrastructure classique et que vous ne voyez pas de liste d'un cas précédent, sélectionnez **Afficher les cas archivés**. 
{: tip}

