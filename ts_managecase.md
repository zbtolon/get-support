---

copyright:

  years: 2015, 2019

lastupdated: "2019-05-16"

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


# Troubleshooting for managing support cases
{: #Supportcases}

You might encounter problems with creating and managing {{site.data.keyword.Bluemix}} support cases. In many cases, you can recover from these problems by following a few easy steps.
{:shortdesc}

## Why can't I create or edit support cases? 
{: #ts_service_broker}

You can't create or edit an {{site.data.keyword.Bluemix_notm}} support case, and you receive an error message that you don't have the appropriate access. 
{:shortdesc}

When you try to create a case the following error message is displayed:   
{: tsSymptoms}

`Looks like you don't have access to create cases for this account.`

General problems with accessing and managing support cases might be caused by 
not having the Identity and Access Management (IAM) access policy for the Support Center account management service. You must be assigned the editor or administrator role on the support center account management service to create cases. 
{: tsCauses}

To resolve the issue, the account owner, an administrator on the support center service, or the administrator on all account management services can assign an IAM policy on support center to manage cases. 
{: tsResolve}

If you're the account owner or an administrator of the Support Center, complete the following steps to create an access policy for working with support cases:

1. Go to **Manage** &gt; **Access (IAM)** and select **Users**.
2. Select a user name, and click **Access policies**. 
3. Click **Assign Access**. 
4. Select **Assign access to account management services**. 
5. From the **Service** menu, select **Support Center**. 
6. Select a role to define the level of access for the user. 


## Why can't I view all cases in the account?
{: #ts_viewcasedetails}

You can't view all of the cases in the account because you don't have access to view all users in the account. 
{:shortdesc}

When you try to view the support cases that are associated with the account, you can't see all open cases. 
{: tsSymptoms}

The account owner set the [user list visibility setting](/docs/iam?topic=iam-userlistview#userlistview) to restricted. When the setting is set as restricted, and you don't have an additional access policy for viewing users in the account, you don't have the required access to view all cases in the account. You can view only the users that you invited to the account, share a Cloud Foundry org membership with, or users who are in your classic infrastructure user hierarchy. 
{: tsCauses}

You must be assigned an IAM policy with at least the Viewer role on the User management account management service in addition to your Support Center account management service access policy. To view your current access, go to **Manage** &gt; **Access (IAM)**, and select your name from the **Users** page. Click the **Access policies** tab, and review your assigned policies. 
{: tsResolve}

To resolve the issue, contact the account owner to request the appropriate access. 

## Why can't I find a case that I previously created? 
{: #ts_viewarchivedcase}

You can't find your cases that you created before the enhanced {{site.data.keyword.Bluemix_notm}} platform experience. 
{:shortdesc}

After going to the **Manage cases** tab in the Support Center, you can't find any cases that you created before 2018 December 2. 
{: tsSymptoms}

Cases that were opened before 2018 December 2 are visible only from the **View archived cases**. 
{: tsCauses}

To view your cases, go to **Support**, select **Manage cases**, and click **View archived cases**.
{: tsResolve} 





