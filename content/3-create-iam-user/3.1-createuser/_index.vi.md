+++
title = "Tạo các IAM User"
weight = 1
chapter = false
pre = "<b>3.1 </b>"
+++

#### Creating IAM Users

Here, you will be guided on how to create IAM users, specifically the user **EC2-admin-user**. For other users, you will have general instructions for the setup.

1. Log in to the **IAM console** using the link: https://console.aws.amazon.com/iam/home#/home
2. In the left navigation pane, select **Users**, and then click **Add User**.

![3_AddUser](/images/3_AddUser.png?width=90pc)

3. On the **Set user details** page, enter the following information:
    - User name: **EC2-admin-user**
    - Access type: Check **AWS Management Console access** to allow user access to the AWS Management Console.
    - Console password: Choose **Custom password** and set a password of your choice for the user.
    - Require password reset: Uncheck this option to avoid the user changing their password on the first login.
    - Review and click **Next: Permissions**.

![3_SetDetails](/images/3_SetDetails.png?width=90pc)

4. On the **Set permissions** page, perform the following steps:
    - Select **Attach existing policies directly** to assign permissions directly to the user.
    - In the search box next to **Filter Policies**, search for and select **AmazonEC2FullAccess**.
    - Review and click **Next: Tags**.

![3_SetPermission](/images/3_SetPermission.png?width=90pc)

5. On the **Add tags (optional)** page, leave the defaults and click **Next: Review**.

6. On the **Review** page, review the information and click **Create user**.

7. Once the user creation process is complete, click **Close** to return to the IAM Console.

You have successfully created the user. To create other users, follow the same procedure with different settings for **Step 3 and 4**:
- **RDS-admin-user**:
    - **Step 3**: On the **Set user details** page, enter the following information:
        - User name: **RDS-admin-user**
    - **Step 4**: On the **Set permissions** page, do the following:
        - Select **Attach existing policies directly**.
        - Choose **AmazonRDSFullAccess** and **DatabaseAdministrator**.
- **Group-user**:
    - **Step 3**: On the **Set user details** page, enter the following information:
        - User name: **Group-user**
    - **Step 4**: On the **Set permissions** page, do the following:
        - Select **Add user to group**.
        - Check the group **ec2-rds-admin-group**.
- **No-permission-user**:
    - **Step 3**: On the **Set user details** page, enter the following information:
        - User name: **No-permission-user**
    - **Step 4**: Skip the permissions and click **Next: Tags**.
