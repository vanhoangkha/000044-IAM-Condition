+++
title = "Configure Switch role"
weight = 2
chapter = false
pre = "<b>4.2 </b>"
+++

#### Overview
In this step, you will configure the **lab44-RoleFullAccess** role to allow **No-permission-user** user to use this role.

**Content:**
- [Configure Switch role](#configure-switch-role)

#### Switch role configuration

1. Access the IAM console page at the link https://console.aws.amazon.com/iam/home#/home
2. In the left navigation bar, select **Users**
3. Click on user **No-permission-user**, copy information **User ARN**

![4.2_UserARN](/images/4.2_UserARN.png?width=90pc)

4. In the left navigation bar, click **Roles**, then select the newly created IAM Role **lab44-RoleFullAccess**.

5. Select the **Trust relationships** tab and select **Edit trust relationship**

![4.2_EditTrust](/images/4.2_EditTrust.png?width=90pc)

6. Add **AWS** with information as **User ARN** of user **No-permission-user** as shown below. Then click **Update Trust Policy**

![4.2_UpdatePolicy](/images/4.2_UpdatePolicy.png?width=90pc)

7. Thus, the **No-permission-user** user can already use the **lab44-RoleFullAccess** role. To check assume role, do the following:
    - Log in user **No-permission-user**, then click on the user's name in the right corner of the screen, select **Switch Role**
    - At the **Switch Role** screen, enter the required information.
    - Click **Switch role** to assume role for user **No-permission-user**.
    - Perform access to basic services such as EC2 or RDS to confirm successful Switch role configuration. With **AdministratorAccess** access, **No-permission-user** user can now use any service.