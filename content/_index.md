+++
title = "IAM Role & Condition"
weight = 1
chapter = false
+++

# IAM Role & Condition

#### Overview
In lesson [Getting started with IAM](https://000002.awsstudygroup.com/) we have created IAM User with admin rights for all services. In practice, we usually only grant sufficient rights (minimum privileges - *least privilege*) to the administrator.

In this article, we will review the concept of IAM, then proceed to create a User/Group that plays the role of admin for each EC2 and RDS service. The next step is to create a Role and increase security by setting additional restrictions by IP address and time.

{{< figure src="../images/serviceicon2.png" title="AWS IAM" width=150pc >}}
{{< figure src="/images/IAM.png" title="Assume Role Process" width=70% >}}
#### Content
1. [Introduction to IAM](1-iam-intro/)
2. [Create IAM Group](2-create-iam-group/)
3. [Create IAM User](3-create-iam-user/)
4. [Configure IAM Role & Condition](4-configure-iam-role-with-condition/)
5. [Resource Cleanup](5-cleanup)