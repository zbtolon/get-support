---

copyright:

  years: 2015, 2018

lastupdated: "2018-03-15"

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

Vous définissez la gravité du problème en fonction de vos besoins métier et de votre niveau d'assistance. Tous les tickets sont examinés afin d'identifier la cause première et de résoudre le problème. Lorsque des données de diagnostic de problème sont nécessaires pour déterminer la cause première du problème, le système vous demande d'approuver l'accès aux fichiers journaux et à d'autres données d'identification de problème à partir de votre application. Sans ces données, la résolution du problème peut être retardée.

Si vous devez fournir des informations de diagnostic, utilisez les instructions suivantes pour collecter les informations demandées aussi rapidement que possible.

## Collecte d'informations de diagnostic
{: #collecting-diagnostic-information}

Pour diagnostiquer et résoudre des problèmes avec les applications et les services {{site.data.keyword.Bluemix_notm}}, il se peut que l'équipe de support {{site.data.keyword.Bluemix_notm}} vous demande de collecter des informations de diagnostic.

Avant de collecter des informations de diagnostic, procédez comme suit :

1. Vérifiez que vous avez installé la version la plus récente de l'interface de ligne de commande cf. Pour plus d'informations, voir [Installation de l'interface de ligne de commande cf](/docs/starters/install_cli.html).
>**Remarque :** si vous n'avez pas installé la version la plus récente de l'interface de ligne de commande cf, lorsque cette interface est connectée à {{site.data.keyword.Bluemix_notm}}, la commande `cf logs` risque de ne pas renvoyer de sortie.
2. Assurez-vous d'avoir connecté l'interface de ligne de commande cf à l'emplacement où {{site.data.keyword.Bluemix_notm}} est en cours d'exécution par l'intermédiaire de la commande `cf api`.

Utilisez l'un des scripts suivants pour collecter les informations de diagnostic :

  * Pour les systèmes d'exploitation Windows, téléchargez le fichier [bmdiag-general.bat ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} et exécutez-le.
  * Pour les systèmes d'exploitation Linux et Mac, téléchargez le fichier [bmdiag-general.sh ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} et exécutez-le.

Les scripts utilisent l'interface de ligne de commande cf pour extraire les informations suivantes de votre environnement d'application :
  * Journaux d'application
  * Métadonnées d'application
  * Routes configurées
  * Evénements
  * Services mis à disposition

## Est-il possible de rendre prioritaire un ticket de demande de service ?
{: #escalation}

Avec le support premium ou avancé, si vous n'avez pas reçu de réponse à un ticket de demande de service dans un délai raisonnable, ou si vous pensez qu'un ticket de demande de service n'a pas été traité de manière appropriée, vous pouvez le transférer à un niveau supérieur.  
{:shortdesc}

Pour plus d'informations sur le support premium et avancé, voir [Types de support](/docs/get-support/getstarttssup.html#typesofsupport). 

Dans le cadre du processus d'escalade d'un ticket de demande de service, les responsables IBM prennent connaissance de vos préoccupations et collaborent avec vous afin d'améliorer votre expérience en matière d'assistance.

Pour soumettre une demande d'escalade, procédez comme suit :
  1. Ouvrez un nouveau ticket de demande de service avec comme récapitulatif **Demande d'escalade**.
  2. Pour que votre demande d'escalade puisse être mise en corrélation avec le ticket de demande de support d'origine, incluez les informations suivantes dans le corps du ticket :
      * Le numéro du ticket de demande de service ouvert nécessitant une escalade.
      * Un bref récapitulatif des raisons de l'escalade.

## Heures de service
{: #support-hours-operation}

Les problèmes de gravité 1 sont surveillés 24 heures sur 24, 7 jours sur 7. Les soumissions de formulaire relatifs aux problèmes avec des niveaux de gravité autres sont surveillés du dimanche 21:30 UTC au vendredi 23:59 UTC (à l'exclusion des jours fériés).

Pour obtenir de l'aide afin de savoir comment convertir ces heures de support dans votre fuseau horaire local, consultez [Timeanddate.com ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien ")](https://www.timeanddate.com). Pour plus d'informations sur le planning des jours fériés, voir [{{site.data.keyword.Bluemix_notm}} Support Holidays ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://ibm.biz/bluemixholidays).
