---

copyright:

  years: 2018

lastupdated: "2018-12-03"

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

To quickly assign users access to work with support cases in your account, complete the following steps to create an access group with the necessary support center and user management service access, and then add the users to the access group that need the access:

1. From the menu bar, click **Manage** &gt; **Access (IAM)**, and then select **Access groups**.
2. Click **Create**. 
3. Enter an access group name and description. 
4. Click **Create**. 
5. Click **Access policies**.
6. Click **Assign access**.
7. Select **Assign access to account management services**.
8. Select the **Support Center** service.
9. Select **Viewer** or **Administrator** role depending on the type of access that you want this group to have.
10. Click **Assign**.

Check out the following table to understand exactly what permissions are included in each role for the Support Center.

| Role | Action | 
|--------|---------------|
|Viewer  | View and search cases |
|Administrator | View, search, create, and update cases|
{: caption="Table 1. Roles and actions for the Support Center service" caption-side="top"}

Then, if the User list visibility setting it set to restricted in the account, you might want to add an additional policy for the User management service with the Viewer role to ensure that users can access all cases in the account. For the access group that you already created and assigned the Support Center access, complete the following steps to add the additional policy:

1. Click **Assign access** from the **Access policies** tab for the access group.
2. Select **Assign access to account management services**.
3. Select the **User Management** service.
4. Select the **Viewer** role.
5. Click **Assign**.

Now, you have an access group that you can add any users to in your account to streamline the process of assigning access to work with support cases. To add users to your access group, complete the following steps:

1. From the **Users** tab for your access group, click **Add users**.
2. Select the user that you want added to the group.
3. Click **Add to group**.



