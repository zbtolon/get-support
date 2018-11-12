---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-23"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Comment obtenir une réponse rapide à mon ticket ?
{: #quicktickresp}

Lorsque vous contactez le support et ouvrez un ticket de demande de service, vous pouvez demander un niveau de gravité particulier, en fonction du type et de l'urgence du problème. Le niveau de gravité peut avoir un impact sur la rapidité à laquelle votre problème est traité.
{:shortdesc}

Vous définissez la gravité du problème en fonction de vos besoins métier et de votre niveau d'assistance. Pour plus d'informations sur les niveaux des plans de support, voir [Plans de support](/docs/get-support/index.html). Tous les tickets sont examinés afin d'identifier la cause première et de résoudre le problème. Lorsque des données de diagnostic de problème sont nécessaires pour déterminer sa cause première, le système vous demande d'approuver l'accès aux fichiers journaux et à d'autres données d'identification de problème à partir de votre application. Sans ces données, la résolution du problème peut être retardée.

## Collecte d'informations de diagnostic
{: #collecting-diagnostic-information}

Pour diagnostiquer et résoudre des problèmes concernant des applications et services {{site.data.keyword.Bluemix_notm}}, il se peut que l'équipe de support {{site.data.keyword.Bluemix_notm}} vous réclame des informations de diagnostic. Utilisez les instructions ci-après pour collecter et fournir les informations demandées le plus rapidement possible.

Avant de collecter des informations de diagnostic, procédez comme suit :

1. Vérifiez que vous avez bien installé la version la plus récente de l'interface de ligne de commande Cloud Foundry. Pour plus d'informations, voir [Installation de l'interface de ligne de commande Cloud Foundry](/docs/starters/install_cli.html).
>**Remarque :** si vous n'avez pas installé sa version la plus récente, une fois l'interface de ligne de commande Cloud Foundry connectée à {{site.data.keyword.Bluemix_notm}}, il se peut que la commande `cf logs` ne renvoie pas de sortie.
2. Vérifiez à l'aide de la commande `cf api` que vous avez connecté l'interface de ligne de commande Cloud Foundry à l'emplacement où {{site.data.keyword.Bluemix_notm}} s'exécute.

Utilisez l'un des scripts suivants pour collecter les informations de diagnostic :

  * Pour les systèmes d'exploitation Windows, téléchargez le fichier [bmdiag-general.bat ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} et exécutez-le.
  * Pour les systèmes d'exploitation Linux et Mac, téléchargez le fichier [bmdiag-general.sh ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} et exécutez-le.

Les scripts utilisent l'interface de ligne de commande Cloud Foundry pour extraire les informations suivantes de votre environnement d'application :
  * Journaux d'application
  * Métadonnées d'application
  * Routes configurées
  * Evénements
  * Services mis à disposition

## Escalade de cas de support
{: #escalation}

Le processus d'escalade vous permet non seulement de signaler des problèmes critiques, mais également d'exprimer vos inquiétudes si vous avez le sentiment que votre cas de support n'est pas traité de manière appropriée. Lorsqu'un cas de support est remonté, le responsable qui est de service prend connaissance des informations contenues dans le cas de support, affecte le traitement de cette tâche aux personnes appropriées de l'équipe de support technique {{site.data.keyword.Bluemix_notm}} et vous tient informé.

Vous pouvez demander une assistance supplémentaire en faisant remonter votre cas au responsable de support {{site.data.keyword.Bluemix_notm}} qui est de service en tant que client avec un abonnement payant. 

Pour faire remonter un cas de support, vous devez avoir un case de support ouvert pour le problème. Prenez soin également de bien documenter le problème technique dans le cas de support que vous avez ouvert.

 Pour faire remonter un cas, procédez comme suit :

  1. Contactez l'équipe de support {{site.data.keyword.Bluemix_notm}} par téléphone ou via une discussion en ligne :
    * Par téléphone, composez le numéro suivant : 866-403-7638.
    * Si vous optez pour la discussion en ligne, accédez au [centre de support ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.bluemix.net/unifiedsupport/supportcenter){: new_window}{{site.data.keyword.Bluemix_notm}} ou, si vous disposez d'un compte SoftLayer qui n'est pas lié, accédez au [portail client ![Icône de lien externe](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window}.
  2. Indiquez le numéro de cas de support dont vous disposez et demandez à faire remonter le cas.
  3. Indiquez la justification de l'escalade et l'impact de votre cas.

Les responsables de support {{site.data.keyword.Bluemix_notm}} sont de service et disponibles 24 heures sur 24, 7 jours sur 7. Les responsables qui sont de service affectent les ressources appropriées au traitement de vos cas et vous informent sur les actions menées.
