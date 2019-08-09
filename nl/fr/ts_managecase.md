---

copyright:

  years: 2015, 2019

lastupdated: "2019-07-25"

keywords: help managing cases, resolve issues managing cases, trouble working with cases

subcollection: get-support

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Traitement des incidents liés à la gestion des cas de support
{: #Supportcases}

Vous pouvez rencontrer des problèmes lors de la création et de la gestion des cas de support {{site.data.keyword.Bluemix}}. Dans de nombreux cas, ces problèmes peuvent être résolus en quelques opérations simples.
{:shortdesc}

## Pourquoi ne puis-je pas créer ou modifier des cas de support ? 
{: #ts_service_broker}

Vous ne pouvez pas créer ou éditer un cas de support {{site.data.keyword.Bluemix_notm}} et un message d'erreur indiquant que vous ne disposez pas de l'accès approprié s'affiche. 
{:shortdesc}

Lorsque vous tentez de créer un cas, le message d'erreur suivant s'affiche :   
{: tsSymptoms}

`Il semble que vous ne soyez pas autorisé à créer des cas pour ce compte.`

Des problèmes généraux liés à l'accès et à la gestion des cas de support peuvent être dus à l'absence de règle d'accès IAM (Identity and Access Management) pour le service de gestion de compte du Centre de support. Le rôle d'éditeur ou d'administrateur sur le service de gestion des comptes du centre de support doit vous être attribué pour que vous puissiez créer des cas. 
{: tsCauses}

Pour résoudre le problème, le propriétaire du compte, un administrateur du service de centre de support ou l'administrateur de tous les services de gestion de compte peut affecter une règle IAM au centre de support pour gérer les cas. 
{: tsResolve}

Si vous êtes le propriétaire du compte ou un administrateur du Centre de support, procédez comme suit pour créer une règle d'accès permettant de traiter des cas de support :

1. Accédez à **Gérer** &gt; **Accès (IAM)** puis sélectionnez **Utilisateurs**.
2. Sélectionnez un nom d'utilisateur et cliquez sur **Règles d'accès**. 
3. Cliquez sur **Affecter un accès**. 
4. Sélectionnez **Affecter l'accès aux services de gestion des comptes**. 
5. Dans le menu **Service**, sélectionnez **Centre de support**. 
6. Sélectionnez un rôle pour définir le niveau d'accès de l'utilisateur. 


## Pourquoi ne puis-je pas voir tous les cas du compte ?
{: #ts_viewcasedetails}

Vous ne pouvez pas afficher tous les cas du compte car vous n'avez pas accès à tous les utilisateurs du compte. 
{:shortdesc}

Lorsque vous tentez d'afficher les cas de support associés au compte, vous ne pouvez pas voir tous les cas ouverts. 
{: tsSymptoms}

Le propriétaire du compte a défini le [paramètre de visibilité de la liste d'utilisateurs](/docs/iam?topic=iam-userlistview#userlistview) sur restreint. Lorsque le paramètre est défini sur restreint et que vous ne disposez pas d'une règle d'accès supplémentaire pour afficher les utilisateurs du compte, vous ne disposez pas de l'accès requis pour afficher tous les cas du compte. Vous pouvez afficher uniquement les utilisateurs que vous avez invités au compte, avec lesquels vous pouvez partager une adhésion à l'organisation Cloud Foundry, ou les utilisateurs appartenant à votre hiérarchie d'utilisateurs d'infrastructure classique. 
{: tsCauses}

Vous devez disposer d'une règle IAM avec au moins le rôle Afficheur sur le service de gestion des comptes Gestion des utilisateurs, en plus de la règle d'accès au service de gestion des comptes de votre Centre de support. Pour consulter votre accès en cours, accédez à **Gérer** &gt; **Accès (IAM)**, et sélectionnez votre nom sur la page **Utilisateurs**. Cliquez sur l'onglet **Règles d'accès**, et examinez les règles qui vous sont affectées. 
{: tsResolve}

Pour résoudre le problème, contactez le propriétaire du compte pour demander l'accès approprié. 

## Pourquoi ne puis-je pas trouver un cas que j'ai créé précédemment ? 
{: #ts_viewarchivedcase}

Les cas créés avant l'amélioration de la plateforme {{site.data.keyword.Bluemix_notm}} ne sont pas accessibles. 
{:shortdesc}

Dans l'onglet **Gérer les cas** du centre de support, vous ne pouvez pas accéder aux cas créés avant le 2 décembre 2018.
{: tsSymptoms}

Les cas ouverts avant le 2 décembre 2018 sont visibles uniquement en sélectionnant **Afficher les cas archivés**. 
{: tsCauses}

Pour afficher vos cas, accédez à **Support**, sélectionnez **Gérer les cas** puis cliquez sur **Afficher les cas archivés**.
{: tsResolve} 






