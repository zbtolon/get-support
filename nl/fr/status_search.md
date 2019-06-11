---

copyright:

  years: 2018,2019

lastupdated: "2019-05-16"

keywords: status page, status query

subcollection: get-support

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}

# Recherche de statut avancée
{: #adv-search}

Vous pouvez effectuer une recherche dans tous les onglets de la page Statut, mais saviez-vous que vous pouvez créer des valeurs de recherche d'URL en utilisant des paramètres de requête extérieurs à la console ?
{:shortdesc}

La liste suivante comprend des exemples d'options de recherche d'URL :

* Chargez la page avec l'onglet Statut sélectionné : `console.cloud.ibm.com/status?selected=status`
* Chargez la page avec l'onglet Maintenance planifiée sélectionné : `console.cloud.ibm.com/status?selected=maintenance`
* Chargez la page avec l'onglet Bulletin de sécurité sélectionné : `console.cloud.ibm.com/status?selected=security`
* Chargez la page avec l'onglet Annonces sélectionné : `console.cloud.ibm.com/status?selected=announcement`
* Chargez la page avec une requête de recherche entrée : `console.cloud.ibm.com/status?selected=<selected>&query=<query>`
* Ouvrez la page avec les filtres sélectionnés. Par exemple, vous pouvez définir l'emplacement géographique sur Amérique du Nord à l'aide de la recherche d'URL suivante : `console.cloud.ibm.com/status?selected=status&region=na`

* Utilisez des identificateurs de notification uniques comme paramètre de recherche pour accéder directement aux détails de la notification. Par exemple, `query=INC1000001` cible les éléments avec l'ID : `INC1000001`. Dans cet exemple, `INC1000001` est le numéro de cas d'une notification de maintenance.

### Filtres de requête d'URL :
{: #url-query}

| Paramètre de requête d'URL | Description | Valeurs |
| ----- | ----- | ----- | ----- |
| `?type` | Filtre qui s'applique uniquement à l'onglet Statut. Utilisez la requête `?type` pour filtrer l'onglet Statut par incident ou par maintenance. | `=incident`, `=maintenance` |
| `?region` | Filtrer la page par emplacement géographique.  | `=na`, `=eu`, `=sa`, `=ap` |
| `?component` | Filtrer la page par composants {{site.data.keyword.Bluemix_notm}}. Par exemple, vous pouvez filtrer selon le service qui vous intéresse. | S'applique à la plupart des ID de catalogue globaux ; par exemple, `?component=iotf-service` filtre la page et affiche les événements qui affectent Internet of Things Platform  |
{: caption="Tableau 1. Filtres de requête d'URL" caption-side="top"}

Vous pouvez toujours utiliser les filtres **Filtrer par**, puis copier ou marquer la requête URL générée. Les filtres sont affichés dans votre URL et peuvent vous aider à créer des requêtes ultérieures.
{: tip}
