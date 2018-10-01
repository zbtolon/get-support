---

copyright:

  years: 2015, 2018

lastupdated: "2018-09-14"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Affichage des notifications et du statut du système
{: #viewing-bluemix-status}

La page Statut est l'emplacement central pour rechercher des notifications et des annonces sur les événements clés affectant la plateforme {{site.data.keyword.Bluemix_notm}} et les principaux services.
{:shortdesc}

Les informations suivantes sont disponibles sur la page Statut :

  * Statut en cours des services et des composants pour toutes les régions de service {{site.data.keyword.Bluemix_notm}} Foundry.
  * Liste des annonces, par ordre chronologique, pour la maintenance et les incidents. Vous pouvez appliquer un filtre à la liste ou ouvrir une annonce individuelle pour plus de détails.
  * Créneaux de maintenance planifiés dont vous êtes avisé à l'avance, excepté en cas de circonstances extrêmes.
  * Incidents ou pannes imprévus, publiés dès que l'équipe {{site.data.keyword.Bluemix_notm}} en est informée. Les notifications d'incident sont régulièrement mises à jour jusqu'à leur résolution.
  * Références aux bulletins de sécurité qui ont un impact sur les divers services {{site.data.keyword.Bluemix_notm}} ou la plateforme.
  * Autres annonces relatives aux plateformes d'intérêt général.
  * [Flux RSS auquel vous pouvez vous abonner](#subscribing-rss-feed).

Vous pouvez afficher la page Statut en choisissant l'une des options suivantes :

  * Connectez vous à la console {{site.data.keyword.Bluemix_notm}}. Dans la barre de menus, cliquez sur **Support** et sélectionnez **Statut**. Recherchez dans les ressources répertoriées l'icône signalant ![des problèmes](images/some_issues.svg). Celle-ci peut indiquer une indisponibilité.
  * Vous pouvez y accéder directement à l'adresse [{{site.data.keyword.Bluemix_notm}} - Statut ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.bluemix.net/status){: new_window}.


## Meilleures pratiques pour la surveillance du statut
{: #best-practices}

Appliquez les meilleures pratiques suivantes surveiller le statut de {{site.data.keyword.Bluemix_notm}} afin de rester informé et de planifier en conséquence.

### Vérification des fenêtres de maintenance prévues
{: #monbp-checmaintwin}

Vérifiez les fenêtres de maintenance prévues publiées sur la page Statut au moins une fois par jour en utilisant l'une des options suivantes :
* En accédant directement à la page [Statut ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.bluemix.net/status){: new_window}
* En utilisant le flux RSS ou un réexpéditeur RSS vers e-mail

### Vérification des fenêtres de maintenance ou d'un incident en cours
{: #monbp-checcurmaninprog}

Si vous trouvez que {{site.data.keyword.Bluemix_notm}} ne fonctionne pas comme prévu, recherchez des fenêtres de maintenance ou un incident en cours sur la page Statut. Pour signaler un incident qui n'est pas déjà répertorié sur cette page, ouvrez un ticket de demande de service en cliquant sur **Support** et en sélectionnant **Ajouter un ticket** dans la barre de menus, ou en accédant à la page d'aide [{{site.data.keyword.Bluemix_notm}} Support ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://www.ibm.biz/bluemixsupport){: new_window}.

### Avantages des régions multiples de services {{site.data.keyword.Bluemix_notm}} Foundry
{: #monbp-multpreg}

Tous les utilisateurs de l'environnement {{site.data.keyword.Bluemix_notm}} Public ont automatiquement accès aux régions Sud des Etats-Unis, Est des Etats-Unis, Europe-Royaume-Uni, Europe-Allemagne et Australie-Sydney. L'équipe de {{site.data.keyword.Bluemix_notm}} Global Operations gère toutes les régions afin d'éviter les impacts de la maintenance et de minimiser le risque d'incidents affectant simultanément toutes les régions.

Pour basculer vers une autre région, depuis la barre de menus {{site.data.keyword.Bluemix_notm}}, développez le menu Région, puis sélectionnez une autre région.

### Préparation pour des interruptions mineures
{: #monbp-prepmininter}

Dans la plupart des cas, {{site.data.keyword.Bluemix_notm}} peut continuer à être utilisé normalement, même pendant une fenêtre de maintenance. Des interruptions mineures de service ne peuvent cependant pas toujours être évitées. L'exécution des applications reste généralement disponible, même si les fonctions de gestion d'application de {{site.data.keyword.Bluemix_notm}}, telles que le démarrage et l'arrêt d'applications, sont temporairement interrompues. Pour une plus grande disponibilité de vos applications en cours d'exécution, exécutez au moins trois instances de chaque application.

## Abonnement à un flux RSS
{: #subscribing-rss-feed}

Vous pouvez recevoir des alertes sur toutes les notifications en vous abonnant au flux RSS pour la page Statut {{site.data.keyword.Bluemix_notm}}. Cette approche permet d'obtenir des mises à jour sans avoir à consulter régulièrement la page Statut.

Pour vous abonner, procédez comme suit :

1. Téléchargez et installez le lecteur RSS.
2. Utilisez votre lecteur pour vous abonner au flux à l'aide de l'une des méthodes suivantes :
    * Faites glisser l'icône RSS ![RSS](images/rss.svg) dans votre lecteur RSS.
    * Cliquez avec le bouton droit de la souris sur l'icône RSS, sélectionnez **Copy link address**, et collez l'adresse URL dans votre lecteur RSS.

Pour plus d'informations, reportez-vous à la section **Aide** de votre lecteur. 	   

D'autres méthodes de lecture de flux RSS sont disponibles via des plug-in de navigateur Web, tels que les suivants :
  * [Lecteur de flux RSS ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://feeder.co/){: new_window} pour Chrome
  * [Module complémentaire Brief ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://addons.mozilla.org/en-US/firefox/addon/brief/){: new_window} pour Firefox

Des sources Nouveautés, telles que les sites suivants, fournissent également des méthodes de lecture de flux RSS :
  * [Feedly ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://www.feedly.com/){: new_window}
  * [G2reader ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://www.g2reader.com/en/){: new_window}

Vous pouvez également utiliser un service de tiers pour envoyer un courrier électronique automatiquement à chaque mise à jour RSS. La liste suivante répertorie des exemples de service de tiers :

  * www.feedmyinbox.com
  * www.rssforward.com
  * www.feedrabbit.com
  * www.mailchimp.com
  * www.feedmailer.com
  * www.iftt.com

Généralement, {{site.data.keyword.Bluemix_notm}} présente environ 50 mises à jour par mois.


## Configuration des notifications d'incident et de maintenance
{: #setting-up-notifications}

Pour {{site.data.keyword.Bluemix_notm}} Public, vous pouvez vous inscrire afin de recevoir des notifications de plateforme, qui sont des alertes par courrier électronique facultatives relatives à des événements d'incident et de maintenance pour la plateforme. Pour configurer les notifications, cliquez sur **Gérer** > **Compte** > **Notifications** et sélectionnez l'onglet **Plateforme**. 
