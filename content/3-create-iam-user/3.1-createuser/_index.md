+++
title = "Create IAM Users"
weight = 1
chapter = false
pre = "<b>3.1 </b>"
+++

#### Create IAM Users
Here, you will be guided in detail on how to initialize an IAM user, specifically user **EC2-admin-user**. For the rest of the users, you will have a general guide to initialization parameters.

1. Log in to **IAM console** by following the link https://console.aws.amazon.com/iam/home#/home
2. In the left navigation bar, select **User**, then click **Add User**

![3_AddUser](/images/3_AddUser.png?width=90pc)

3. On the **Set user details** page, enter the following information:
    - User name: **EC2-admin-user**
    - Access type: tick **AWS Management Console access** to allow users to access AWS Management Console
    - Console password: select **Custom password** and enter the password you like for the user
    - Require password reset: uncheck this option so that the user does not need to change the password when logging in for the first time
    - Check and select **Next: Permissions**

![3_SetDetails](/images/3_SetDetails.png?width=90pc)

4. On the **Set permissions** page, we operate:
    - Select **Attach existing policies directly** to choose the method of assigning permissions directly to the user.
- In the search box next to **Filter Policies**, find and select **AmazonEC2FullAccess**
    - Check and select **Next: Tags**

![3_SetPermission](/images/3_SetPermission.png?width=90pc)

5. On the **Add tags (optional)** page, keep the defaults and select **Next: Review**

6. On the **Review** page, check the information and select **Create user**

7. When the initialization is complete, press **Close** to return to the IAM Console.

With that, you have completed the user initialization step. To create the remaining users, you need to repeat the above process with the following difference parameters for **steps 3 and 4**:
- **RDS-admin-user**:
    - **Step 3**: At the **Set user details** page, enter the following information:
        - User name: **RDS-admin-user**
    - **Step 4**: **Set permissions** page, manipulate:
        - Select **Attach existing policies directly**
        - Select **AmazonRDSFullAccess** and **DatabaseAdministrator**
- **Group-user**:
    - **Step 3**: At the **Set user details** page, enter the following information:
        - User name: **Group-user**
    - **Step 4**: **Set permissions** page, manipulate:
        - Select **Add user to group**
        - Tick the group **ec2-rds-admin-group**
- **No-permission-user**:
    - **Step 3**: At the **Set user details** page, enter the following information:
        - User name: **No-permission-user**
    - **Step 4**: skip and choose **Next: Tags**