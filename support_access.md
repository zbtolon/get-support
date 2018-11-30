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

# Assigning user access for working with support cases
{: #access}

By default, users in your account don't have access to create, update, search, or view cases. As the account owner, you must provide users access by assigning an Identity and Access Management (IAM) access policy. Use the Support Center account management service to assign users access to work with support cases. 
{:shortdesc}

The Support Center access policies provide users access to work with support cases. However, those access policies don't provide access for users to view other users in the account. So, if an account owner set the [**User list visibility setting**](/docs/iam/userlist.html#userlistview) to **Restricted view**, users who have access to manage cases might not be able to access the cases assigned to other users or the account owner. To ensure that users can view all cases, you must provide additional access by also assigning an IAM access policy for the User management account management service with the Viewer role assigned. 

To give specific users full access to certain cases in the account instead of access to all cases by using an IAM access policy, add them to the case by entering their email when you create the case. By adding a user to a case that you create, they have access to view, edit, and update only that case in the account. They also receive notifications when there are updates to the case.

For classic infrastructure users who previously used classic infrastructure permissions to assign support case access, those permissions are now available in [migrated classic infrastructure permission access groups](/docs/iam/infrastructureaccess.html#predefined). The migrated permission access groups do include the IAM policy on the User management service with the Viewer role assigned.

To assign a user an IAM access policy on an account management service, such as the Support Center service or User management service, complete the following steps:

1. From the menu bar, click **Manage** &gt; **Access (IAM)**, and then select **Users**.
2. Select a user from the list.
3. Click **Access policies**.
4. Click **Assign access**.
5. Select **Assign access to account management services**.
6. Select a service from the list. 
5. Select a role to assign the intended access.

Check out the following table to understand exactly what permissions are included in each role.

| Role | Action | 
|--------|---------------|
|Viewer  | View and search cases |
|Administrator | View, search, create, and update cases|
{: caption="Table 1. Roles and actions for the Support Center service" caption-side="top"}

