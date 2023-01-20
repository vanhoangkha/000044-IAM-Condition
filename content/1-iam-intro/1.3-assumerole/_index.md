+++
title = "Assume Role Process "
weight = 3
chapter = false
pre = "<b>1.3 </b>"
+++

#### The process of assume role

- In this section, we will learn how an IAM User performs the assume role and obtains temporary authentication information.

{{< figure src="/images/IAM.png" title="Assume Role Process" width=70% >}}

1. IAM user will have long-term credentials ( password / acccesskey & secretaccesskey ) and will use that long-term credentials to request to AWS Security Token Service ( AWS STS ) and perform sts:AssumeRole action.
2. STS will check whether the IAM user has permission to perform this action or not through Trust Relationship (assigned to Role) and Identity Policy (assigned to IAM User) check.
3. If the STS check is successful, the STS will return the temporary credentials.
4. The IAM user will use the temporary credentials to make requests (API calls) to AWS services. (The IAM User at this point will have the permissions assigned to the IAM role that the IAM User has assigned. assume)