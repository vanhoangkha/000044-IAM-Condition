+++
title = "Check permissions"
weight = 2
chapter = false
pre = "<b>3.2 </b>"
+++

#### Check User Permissions
Here, you will be guided in detail on how to log in to IAM User, specifically user **EC2-admin-user**.

1. Log in to **IAM console** by following the link https://console.aws.amazon.com/iam/home#/home
2. In the left navigation bar, select **User**
3. Select **EC2-admin-user**

![3_UserInfo](/images/3_UserInfo.png?featherlight=false&width=90pc)

4. Select the **Security credentials** tab, copy the link to login for the user next to **Summary**

![3_Link](/images/3_Link.png?featherlight=false&width=90pc)

5. Open a browser tab in incognito mode or open a different browser than the browser you are using. Then, access the link just copied above.

6. Use username and password for user **EC2-admin-user** to log in.

7. Repeat steps 1-6 to log in to other users in turn

8. After successful login, you will do the following tests to make sure the users are configured correctly:
    - **EC2-admin-user**: successfully launched an EC2 instance
    - **RDS-admin-user**: successfully launched an RDS instance
    - **Group-user**: successfully launched an EC2 instance and an RDS instance
    - **No-permission-user**: can't use any service