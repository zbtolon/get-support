---

copyright:

  years: 2018,2019

lastupdated: "2019-05-13"

keywords: access to cases, get access for cases, assign cases

subcollection: get-support

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}

# Attribution d'accès utilisateur pour l'utilisation de cas de support
{: #access}

Par défaut, les utilisateurs de votre compte n'ont pas accès à la création, la mise à jour, la recherche ou la consultation de cas. En tant que propriétaire du compte, vous devez fournir aux utilisateurs un accès en attribuant une règle d'accès IAM (Identity and Access Management). Utilisez le service de gestion des comptes du Centre de support pour attribuer aux utilisateurs un accès permettant de gérer des cas de support. 
{:shortdesc}

Lorsque vous créez un cas, vous pouvez accorder à d'autres utilisateurs l'accès complet à ce dernier en ajoutant leur adresse électronique dans la zone **Ajouter une autre personne à ce cas**. Tout utilisateur ajouté peut afficher, éditer et mettre à jour uniquement ce cas dans le compte. Il reçoit également des notifications lors de la mise à jour du cas.
{: tip}

Pour les utilisateurs d'infrastructure classique, les droits d'affectation de l'accès au cas de support sont désormais disponibles dans les [groupes d'accès migrés des droits d'infrastructure classique](/docs/iam?topic=iam-infrapermission#predefined). Les groupes d'accès migrés des droits incluent la règle IAM sur le service Gestion des utilisateurs avec le rôle Afficheur attribué.

## Création d'un groupe d'accès pour l'utilisation de cas
{: #creating-access-group}

Pour rationaliser le processus d'affectation d'accès, vous pouvez tirer parti de l'affectation d'une règle aux utilisateurs via des groupes d'accès. Procédez comme suit pour créer un groupe d'accès avec l'accès au service de centre de support :

1. Dans la barre de menus, sélectionnez **Gérer** &gt; **Accès (IAM)** puis **Groupes d'accès** et cliquez sur **Créer**. 
2. Entrez une description et un nom de groupe d'accès puis cliquez sur **Créer**. 
3. Cliquez sur **Règles d'accès** > **Affecter un accès**.
4. Sélectionnez **Affecter l'accès aux services de gestion des comptes**.
5. Sélectionnez **Centre de support**.
6. Sélectionnez le rôle **Afficheur**, **Editeur** ou **Administrateur** en fonction du type d'accès que vous souhaitez accorder à ce groupe, puis cliquez sur **Affecter**.

Si vous souhaitez que vos utilisateurs puissent afficher tous les autres utilisateurs du compte, vous pouvez également ajouter le rôle d'afficheur de gestion d'utilisateur à votre groupe d'accès :

1. Cliquez sur **Règles d'accès** > **Affecter un accès**.
2. Sélectionnez **Affecter l'accès aux services de gestion des comptes**.
3. Sélectionnez **Gestion des utilisateurs**.
4. Sélectionnez **Afficheur** puis cliquez sur **Affecter**.

Le tableau suivant répertorie les droits inclus dans chaque rôle pour l'utilisation de cas.

| Rôle | Action | 
|--------|---------------|
|Afficheur  | Afficher et rechercher des cas |
|Editeur | Afficher, rechercher, créer et mettre à jour des cas|
|Administrateur | Afficher, rechercher, créer et mettre à jour des cas ; gérer des rôles de centre de support pour les autres utilisateurs|
{: caption="Tableau 1. Rôles et actions pour le service de Centre de support" caption-side="top"}

## Ajout d'utilisateurs à votre groupe d'accès de gestion des cas
{: #add-user-access-group} 

Maintenant que le groupe d'accès est créé, ajoutez des utilisateurs :

1. Dans l'onglet **Utilisateurs** de votre groupe d'accès, cliquez sur **Ajouter des utilisateurs**.
2. Sélectionnez l'utilisateur que vous souhaitez ajouter au groupe puis cliquez sur **Ajouter au groupe**.

## Octroi de l'accès aux cas pour les utilisateurs individuels 

L'utilisation de groupes d'accès pour l'affectation de services de gestion d'utilisateur et de centre de support constitue la méthode la plus efficace pour l'affectation d'accès. Cependant, vous pouvez également affecter les mêmes droits à des utilisateurs individuels. 

1. Cliquez sur **Gérer** &gt; **Accès (IAM)** puis sélectionnez **Utilisateurs**. 
2. Cliquez sur **Règles d'accès** > **Affecter un accès**.
3. Sélectionnez **Affecter l'accès aux services de gestion des comptes**.
4. Sélectionnez **Centre de support**.
5. Sélectionnez le rôle **Afficheur**, **Editeur** ou **Administrateur** en fonction du type d'accès que vous souhaitez accorder à ce groupe, puis cliquez sur **Affecter**.
6. Si vous souhaitez qu'un utilisateur puisse afficher tous les autres utilisateurs du compte, vous pouvez également lui affecter le rôle d'afficheur de gestion d'utilisateur. 
