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

When you create a case, you can give users full access by entering their email. By adding a user to a case that you create, they have access to view, edit, and update only that case in the account. They also receive notifications when the case is updated.
{: tip}

For classic infrastructure users who previously used classic infrastructure permissions to assign support case access, those permissions are now available in [migrated classic infrastructure permission access groups](/docs/iam/infrastructureaccess.html#predefined). The migrated permission access groups do include the IAM policy on the user management service with the viewer role assigned.

## Creating an access group for working with cases

To assign users access to work with support cases in your account, complete the following steps to create an access group with the necessary support center and user management service access:

1. From the menu bar, click **Manage** &gt; **Access (IAM)**, and then select **Access groups**.
2. Click **Create**. 
3. Enter an access group name and description, and click **Create**. 
5. Select **Access policies**, and then click **Assign access**.
7. Select **Assign access to account management services**.
8. Select the **Support Center** service.
9. Select **Viewer** or **Administrator** role depending on the type of access that you want this group to have.
10. Click **Assign**.

The following table lists the permissions that are included in each role for working with cases.

| Role | Action | 
|--------|---------------|
|Viewer  | View and search cases |
|Administrator | View, search, create, and update cases|
{: caption="Table 1. Roles and actions for the Support Center service" caption-side="top"}

## Adding users to your support case management access group
{: #add-user-access-group} 

Now that you have the access group created, add users:

1. From the **Users** tab for your access group, click **Add users**.
2. Select the user that you want to add to the group.
3. Click **Add to group**.

## Adding a policy for the user management service 
{: #policy-for-user-mgmt-service}

The Support Center access policies don't provide access for users to view other users in the account. So, if an account owner has set the [user list visibility setting](/docs/iam/userlist.html#userlistview) to **Restricted view**, users might not be able to access the cases assigned to other users or the account owner. To ensure that users can view all cases, you must provide additional access by assigning an IAM access policy for the user management service with the viewer role assigned. 

1. Click **Assign access** from the **Access policies** tab for the access group.
2. Select **Assign access to account management services**.
3. Select the **User Management** service.
4. Select the **Viewer** role.
5. Click **Assign**.

