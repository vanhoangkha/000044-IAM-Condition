+++
title = "Limit switch role by Time "
weight = 2
chapter = false
pre = "<b>4.3.2 </b>"
+++

#### Limit switch role by Time 

1. Access the IAM console page at the link https://console.aws.amazon.com/iam/home#/home with Admin user rights
2. In the left navigation bar, click **Roles**, then select the newly created IAM Role **lab44-RoleFullAccess**
3. In the **Trust relationships** tab, click **Edit trust relationship**, add **Condition** as shown below, then click **Update Trust Policy**

![4.3_TimeCondition](/images/4.3_TimeCondition.png?width=90pc)

4. After updating the trust policy, the **Condition** section is added with Date time information that is allowed to perform the switch role

![4.3_TimeTrust](/images/4.3_TimeTrust.png?width=90pc)

5. Go back to the log in session of the user **No-permission-user**, perform the switch role again, we will receive the error message as shown below because the time when we perform the Switch has been out of time for permission.

![4.3_Error](/images/4.3_Error.png?width=90pc)