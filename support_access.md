---

copyright:

  years: 2018,2019

lastupdated: "2019-06-25"

keywords: access to cases, get access for cases, assign cases, watchlist

subcollection: get-support

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Assigning user access for working with support cases
{: #access}

By default, users in your account don't have access to create, update, search, or view cases. As the account owner, you must provide users access by assigning an Identity and Access Management (IAM) access policy. Use the Support Center account management service to assign users access to work with support cases. 
{:shortdesc}

When you create a case, you can give other users full access to that case by adding their email on the **Add another person to this case** field. Any added users have access to view, edit, and update only that case in the account. They also receive notifications when the case is updated.
{: tip}

While giving a user access by assigning a role on the Support Center service enables users to view, edit, or create support cases, they might not be able to view all cases in an account. If the account owner sets the user list visbility setting to restricted, then users only see the cases that they create themselves. To ensure a user can always view or edit all cases in the account, you must assign a second access policy with the viewer role on the user management service. 

For classic infrastructure users, the permissions to assign support case access is now available in [migrated classic infrastructure permission access groups](/docs/iam?topic=iam-infrapermission#predefined). The migrated permission access groups do include the IAM policy on the user management service with the viewer role assigned.
{: note}

## Creating an access group for working with cases
{: #creating-access-group}

To streamline the access assignment process, you can take advantage of assigning a policy to users through access groups. Complete the following steps to create an access group with support center service access:

1. From the menu bar, go to **Manage** &gt; **Access (IAM)**, select **Access groups**, and click **Create**. 
2. Enter an access group name and description, and click **Create**. 
3. Click **Access policies** > **Assign access**.
4. Select **Assign access to account management services**.
5. Select **Support Center**.
6. Select the Viewer, Editor, or Administrator role depending on the type of access that you want this group to have, and click **Assign**. The following table lists the actions that are included in each role for working with cases.

| Role | Action | 
|--------|---------------|
|Viewer  | View and search cases |
|Editor | View, search, create, and update cases|
|Administrator | View, search, create, and update cases; manage support center roles for other users|
{: caption="Table 1. Roles and actions for the Support Center service" caption-side="top"}

By default, users with a Support Center service role can access only support cases that they are assigned to unless one of the following conditions is met:

* User list visibility is set to Unrestricted view by the account owner.
* The user is assigned a user management account management service role.


If you want to ensure that your users can view all support cases in the account, you can also add a policy with the viewer role for the User Management service to your access group:

1. Click **Access policies** > **Assign access**.
2. Select **Assign access to account management services**.
3. Select **User Management**.
4. Select **Viewer** and click **Assign**.


## Adding users to your case management access group
{: #add-user-access-group} 

After you create the access group, complete the following steps to add users:

1. From the **Users** tab for your access group, click **Add users**.
2. Select the user that you want to add and click **Add to group**.

## Granting individual users access to cases 

Using access groups to assign the support center and user management services is the most efficient way for you to assign access, but you can also assign the same permissions to individual users. 

1. Click **Manage** &gt; **Access (IAM)**, and then select **Users**. 
2. Click **Access policies** > **Assign access**.
3. Select **Assign access to account management services**.
4. Select **Support Center**.
5. Select the **Viewer**, **Editor**, or **Administrator** role depending on the type of access that you want this group to have, and click **Assign**.
6. If you want a user to be able to view all other users in the account, you can also assign them the user management viewer role. 
