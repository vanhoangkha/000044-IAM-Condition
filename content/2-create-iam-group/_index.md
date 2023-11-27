+++
title = "Create IAM Group"
weight = 2
chapter = false
pre = "<b>2. </b>"
+++

#### Create an IAM Group

In this section, you will create an IAM Group with administrative access to both EC2 and RDS services.

1. Navigate to the IAM console at the following link: [IAM Console](https://console.aws.amazon.com/iam/home#/home).
2. In the left-hand navigation pane, select **User groups**, and then click **Create group**.

![2_CreateGroup](/images/2_CreateGroup.png?width=90pc)

3. On the **Create user group** page, enter the following information:
    - User group name: **ec2-rds-admin-group**
    - Scroll down to the **Attach permissions policies - Optional** section, search for and select the policies **AmazonEC2FullAccess**, **AmazonRDSFullAccess**, and **DatabaseAdministrator**.
    - Review and click **Create group**.

![2_GroupPolicy](/images/2_GroupPolicy.png?width=90pc)

Congratulations, you have successfully created an IAM Group.
