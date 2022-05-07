+++
title = "Create Admin IAM Role "
weight = 1
chapter = false
pre = "<b>4.1 </b>"
+++
In this step, you will create an IAM Role with Admin rights.

#### Create Admin IAM Role 

1. Log in to the IAM console by following the link https://console.aws.amazon.com/iam/home#/home
2. In the left navigation bar, select **Roles**, then click **Create role**
3. Under **Select type of trusted entity**, select **AWS Service**. Under **Choose a use case**, select **EC2**. Then, select **Next: Permissions**.
{{% notice note %}}
Just to clarify, **trusted entity** is an entity that is allowed to assume a role. Although what we want for a trusted entity is IAM User **No-permission-user**, there is no direct option for this, so we choose **EC2**.
{{% /notice %}}

![4.1_RoleUseCase](/images/4.1_RoleUseCase.png?width=90pc)

4. In the **Attach permissions policies** section, find and select **AdministratorAccess**. Then, select **Next: Tags**.

![4.1_RolePermission](/images/4.1_RolePermission.png?width=90pc)

5. Skip the step of assigning tags and click **Next: Review**

6. On the **Review** page, enter the name of the Role as **lab44-RoleFullAccess**. Then, click **Create role** to finish the Role creation process