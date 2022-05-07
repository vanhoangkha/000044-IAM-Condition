+++
title = "Create IAM Group"
weight = 2
chapter = false
pre = "<b>2. </b>"
+++

#### Create IAM Group
In this section, you will create an IAM Group with admin access to both EC2 and RDS services.

1. Access the IAM console page at the link https://console.aws.amazon.com/iam/home#/home
2. In the left navigation bar, select **User groups**, then click **Create group**

![2_CreateGroup](/images/2_CreateGroup.png?width=90pc)

3. At the **Create user group** page, enter the following information:
     - User group name: **ec2-rds-admin-group**
     - Scroll down to **Attach permissions policies - Optional**, find and select **AmazonEC2FullAccess**, **AmazonRDSFullAccess** and **DatabaseAdministrator** policies
     - Check and click **Create group**

![2_GroupPolicy](/images/2_GroupPolicy.png?width=90pc)

Thus, you have successfully created the IAM Group.