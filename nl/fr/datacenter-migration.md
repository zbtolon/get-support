---

copyright:

  years: 1994, 2018

lastupdated: "2018-10-22"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Retrait de la prise en charge de certains centres de support aux Etats-Unis
{: #dc-migrate}

IBM retire le support des centres de données suivants aux Etats-Unis : 

* dal01 : pods 2 et 3
* wdc01 : pods 1 et 2
{:shortdesc}

##  Pourquoi dois-je migrer vers un autre centre de données ?

Pour continuer à vous faire bénéficier des meilleurs services, matériels et connectivité; nous évaluons continuellement tous nos sites pour nous assurer qu'ils répondent aux réseaux, aux équipements électriques et aux autres normes d'infrastructure. Même si ces sites sont adéquats, ils ne répondent plus à nos normes actuelles.

## Dois-je avoir terminé la migration à la date indiquée ?

Oui. Pour éviter toute interruption de service, nous essayons d'accorder un délai de mise en oeuvre le plus long possible afin de rendre la transition quasiment transparente pour vous. Nous avons commencé à évoquer le déplacement de ce site en mai 2018.

## Devrais-je à nouveau migrer un jour vers un autre centre de données ?

Nous évaluons constamment la qualité de nos sites pour vous offrir le service le meilleur et le plus fiable. Il se peut que d'autres migrations soient à l'ordre du jour suite à l'évaluation de certains de nos sites plus anciens.

## Puis-je choisir n'importe quel centre de données {{site.data.keyword.Bluemix_notm}} aux Etats-Unis ?

Oui, vous pouvez choisir n'importe quel centre de données aux Etats-Unis qui correspond à vos besoins d'emplacement.

## Comment sélectionner le centre de données sur lequel procéder au déploiement ?

IBM dispose de plus de 60 centres de données répartis à des emplacements divers à travers le monde. Examinez la carte de ces centres sur la page globale des centres de données pour déterminer les centres de données où vous pouvez effectuer le déploiement. 

Les facteurs suivants peuvent avoir un impact sur le centre de données que vous sélectionnez :
* Proximité avec les utilisateurs des systèmes
* Proximité avec les autres systèmes avec lesquels ce serveur a besoin de communiquer
* Stratégies de données ou réglementation imposant de stocker les données à un emplacement spécifique

## Suis-je obligé d'utiliser aussi des sites aux Etats-Unis pour la période de transition ?

Vous pouvez utiliser n'importe que site {{site.data.keyword.cloud_notm}} mondial au cours de votre période de transition, laquelle pourra aller jusqu'à 60 jours.

## Les deux mois gratuits des ressources de transition s'ajoutent-ils à mon temps serveur existant ?

Oui. Vous pouvez nous contacter et un représentant du support technique vous aidera pour la procédure d'acquisition de serveurs pour votre période de transition.

## Comment déterminer quelle est ma configuration matérielle actuelle ?

Connectez-vous au portail client. Dans **Liste des unités**, sélectionnez le serveur qui vous intéresse et recherchez les informations de configuration du système. Dans ces informations, vous pouvez examiner le type de processeur, par exemple : Single Intel Xeon E3-1270 (4 coeurs, 3,50 GHz). Vous pouvez également examiner la quantité de mémoire (RAM), le stockage et d'autres données.

## Comment puis-je déterminer l'utilisation de mon matériel actuel ?

La plupart des systèmes d'exploitation fournissent des outils que vous pouvez utiliser pour comprendre l'utilisation de votre système, par exemple, la commande vmstat et iostat sur Linux ou Windows System Performance Monitor. Beaucoup d'autres outils de surveillance des performances peuvent aussi vous être disponibles. La surveillance et le réglage des performances peuvent demander un investissement conséquent en temps et en efforts. En général, vous devez comprendre si des ressources spécifiques dans le système (processeur, mémoire, disque, réseau) sont lourdement utilisées ou ne sont pas utilisées comme elles le devraient. Ces informations peuvent vous aider à mieux dimensionner votre nouveau système. Par exemple, un système où la capacité de mémoire est fréquemment sursollicitée est susceptible de bénéficier d'une mémoire plus volumineuse dans le système cible où vous migrez.

## Comment comparer anciens et nouveaux processeurs ?

Pour comparer les spécifications des anciens et nouveaux processeurs Intel, accédez à [https://ark.intel.com/#@Processors](https://ark.intel.com/#@Processors). Si vous connaissez le type de processeur, vous pouvez naviguer dans les menus. Sinon, vous pouvez utiliser l'option de recherche pour identifier les spécifications des deux processeurs. Les processeurs les plus récents ont tendance à comporter plus de coeurs et à opérer à une cadence d'horloge plus faible que les variantes plus anciennes. Si votre charge de travail est tributaire du processeur (ses performances sont limitées par la vitesse du processeur), nous vous recommandons de choisir un processeur avec moins de coeurs et une vitesse supérieure. Si vous exécutez plusieurs charges de travail qui ne sont pas particulièrement limitées par la vitesse du processeur, la sélection d'un processeur avec plus de coeurs et une cadence d'horloge identique, ou plus faible, peut constituer une meilleure solution.

## Comment sélectionner mon nouveau système d'exploitation ?

Si vous utilisez le serveur depuis plusieurs années sans l'avoir mis jour, il est probable que vous exécutez une version plus ancienne du système d'exploitation. Ceci peut poser des défis pour la migration. Il se peut que vous ne disposiez pas du support d'installation de l'ancien système d'exploitation pour le réinstaller.  Vous pourriez aussi découvrir que le nouveau matériel serveur vers lequel vous migrez n'est pas pris en charge par l'ancienne version du système d'exploitation. Par conséquent, vous devez peut-être choisir un système d'exploitation différent vers lequel migrer.

Votre choix de système d'exploitation peut être dicté par les applications que vous exécutez. Dans le cadre de la migration, vous pouvez être amené à exécuter l'application sur une version ultérieure du système d'exploitation. Vérifiez qu'elle fonctionnera sur la version plus récente.

Les compétences disponibles avec un système d'exploitation spécifique peuvent aussi influencer votre choix. Si vous disposez du code source de l'application, vérifiez que les outils de développement et les fonctions de système et de middleware sont disponibles sur la nouvelle plateforme. En général, les systèmes Linux sont plus à même que Windows de prendre en charge les anciennes applications sur de nouvelles versions du système d'exploitation, mais ceci n'est pas garanti.

## Quelle bande passante est-elle obtenue avec ma nouvelle configuration et est-elle la même que ma bande passante actuelle ?

Vous recevez un package de bande passante actuel étroitement associé à celui dont vous disposiez. Le débit pour ce package est le même que votre débit actuel ou celui couvert par votre package.

## Comment copier des données de mon ancien serveur vers le nouveau ?

Une fois établie la connectivité entre l'ancien et le nouveau serveur, vous devez prendre en compte la manière dont vous transférez des données entre eux. En supposant que vous disposez d'un stockage suffisant sur le nouveau serveur pour gérer le volume de données, une copie directe serveur à serveur est la méthode la plus simple pour ce faire.  Il existe de nombreux outils disponibles que vous pouvez utiliser.  

* scp est un choix idoine pour copier en sécurité un fichier de la source à la destination. Il effectue une copie linéaire ordinaire. 
* Si vous avez besoin de copier un grand nombre de fichiers, la resynchronisation sous ssh est bien plus rapide que sous scp. rsync copie également les structures de répertoires et préserve les autorisations d'accès aux fichiers.

En général, vous de devriez copier que des applications et des données d'application entre les systèmes. La copie d'anciennes versions des fichiers de systèmes d'exploitation vers une nouvelle version peut provoquer des problèmes.

Arrêtez les bases de données avant de les copier entre les systèmes afin de garantir que les données sont cohérentes. Lors de la migration des données de base de données, vérifiez que les données sont migrées d'une façon qui ne limitent pas vos options d'importation dans le nouveau système. Au lieu de copier des données de base de données de système à système, envisagez de les exporter sous un format vous permettant de les importer dans une base de données plus récente. Les fichiers texte à plat, les fichiers CSV, etc., fournissent plus d'options que l'utilisation de formats de fichier propriétaire ou fermé lorsqu'il s'agit de transférer des données entre les systèmes. Testez systématiquement vos approches de migration de données sur un petit jeu de données de test avant d'effectuer la copie officielle.

## Dois-je configurer mon réseau à nouveau sur le nouveau site ?

Votre réseau devra probablement être modifié pour opérer avec les nouveaux serveurs et le nouveau site. Si vous avez besoin d'aide pour ce processus, contactez l'équipe de support par téléphone ou via une discussion.

## Que dois-je faire si je n'ai pas les compétences nécessaires pour migrer ?

La migration d'application peut être une tâche complexe. Ajoutez à ceci les compétences requises pour l'opération. Si des modifications du code de l'application sont requises, vérifiez que vous disposez des compétences de programmation nécessaires. C'est notamment le cas pour les systèmes plus anciens où les compétences se font rares ou qui peuvent être caractérisés par une absence de la documentation ou de connaissance du système lui-même. Si des efforts conséquents sont requis et que le système est particulièrement crucial pour l'activité, envisagez d'investir dans des services payants ou dans d'autres services de migration pour vous épauler.

## Comment obtenir une aide générale pour la migration ?

En fonction du niveau d'aide dont vous avez besoin, vous pouvez contacter le support technique par téléphone ou via une discussion en ligne. Ou vous pouvez contacter notre équipe des services gérés pour obtenir de l'aide.

## Qui contacter si un chargé de clientèle ne m'est pas rattaché ?

Vous pouvez contacter le support technique par téléphone ou via une discussion en ligne pour toute question de migration.
