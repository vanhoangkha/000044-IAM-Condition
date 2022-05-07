+++
title = "Limit switch role by IP "
weight = 1
chapter = false
pre = "<b>4.3.1 </b>"
+++

#### Limit Switch role by IP 

1. Access the IAM console page at the link https://console.aws.amazon.com/iam/home#/home with Admin user rights
2. In the left navigation bar, click **Roles**, then select the newly created IAM Role **lab44-RoleFullAccess**
3. In the **Trust relationships** tab, click **Edit trust relationship**, add **Condition** as shown below, then click **Update Trust Policy**

![4.3_IPCondition](/images/4.3_IPCondition.png?width=90pc)

4. After updating the trust policy, **Condition** section is added with IP information that is allowed to perform switch role

![4.3_IPTrust](/images/4.3_IPTrust.png?width=90pc)

5. Go back to the log in session of the user **No-permission-user**, perform the switch role again, we will receive the error message as shown below because we are accessing the service from a device that does not have an IP like within the conditions of.

![4.3_Error](/images/4.3_Error.png?width=90pc)