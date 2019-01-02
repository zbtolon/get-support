---

copyright:

  years: 2018

lastupdated: "2018-11-28"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}

# Attribution d'accès utilisateur pour l'utilisation de cas de support 
{: #access}

Par défaut, les utilisateurs de votre compte n'ont pas accès à la création, la mise à jour, la recherche ou la consultation de cas. En tant que propriétaire du compte, vous devez fournir aux utilisateurs un accès en attribuant une règle d'accès IAM (Identity and Access Management). Utilisez le service de gestion des comptes du Centre de support pour attribuer aux utilisateurs un accès permettant de gérer des cas de support. {:shortdesc}

Les règles d'accès du Centre de support permettent aux utilisateurs de gérer des cas de support. Cependant, ces règles d'accès ne permettent pas aux utilisateurs d'afficher les autres utilisateurs du compte. Ainsi, si un propriétaire de compte définit le [**paramètre Visibilité de la liste d'utilisateurs**](/docs/iam/userlist.html#userlistview) sur **Affichage restreint**, les utilisateurs ayant accès à la gestion des cas peuvent ne pas être en mesure d'accéder aux cas attribués à d'autres utilisateurs ou au propriétaire du compte. Pour vous assurer que les utilisateurs peuvent afficher tous les cas, vous devez fournir un accès supplémentaire en attribuant également une règle d'accès IAM pour le service de gestion des comptes Gestion des utilisateurs avec le rôle Afficheur attribué.  

Pour accorder aux utilisateurs spécifiques un accès complet à certains cas du compte au lieu d'un accès à tous les cas à l'aide d'une règle d'accès IAM, ajoutez ces utilisateurs au cas en saisissant leur adresse électronique lors de la création du cas. En ajoutant un utilisateur à un cas que vous créez, vous lui accordez le droit d'afficher, de modifier et de mettre à jour uniquement ce cas dans le compte. Ils reçoivent également des notifications lorsque le cas est mis à jour. 

Pour les utilisateurs d'infrastructure classiques qui utilisaient auparavant des droits d'infrastructure classiques pour attribuer un accès aux cas de support, ces droits sont désormais disponibles dans [les groupes d'accès migrés des droits d'infrastructure classique.](/docs/iam/infrastructureaccess.html#predefined). Les groupes d'accès migrés des droits incluent la règle IAM sur le service Gestion des utilisateurs avec le rôle Afficheur attribué. 

Pour affecter à un utilisateur une règle d'accès IAM sur un service de gestion de compte, tel que le service de Centre de support ou le service Gestion des utilisateurs, procédez comme suit : 

1. Dans la barre de menus, cliquez sur **Gérer** &gt; **Accès (IAM)** puis sélectionnez **Utilisateurs**.
2. Sélectionnez un utilisateur dans la liste.
3. Cliquez sur **Règles d'accès**.
4. Cliquez sur **Affecter un accès**.
5. Sélectionnez **Affecter l'accès aux services de gestion des comptes**.
6. Sélectionnez un service dans la liste.  
5. Sélectionnez un rôle pour lui attribuer l'accès prévu. 

Consultez le tableau suivant pour comprendre exactement quels droits sont inclus dans chaque rôle. 

| Rôle | Action | 
|--------|---------------|
|Afficheur  | Afficher et rechercher des cas |
|Administrateur | Afficher, rechercher, créer et mettre à jour des cas|
{: caption="Tableau 1. Rôles et actions pour le service de Centre de support" caption-side="top"}

