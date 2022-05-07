+++
title = "Authenticate requests"
weight = 2
chapter = false
pre = "<b>1.2 </b>"
+++

#### Authenticate requests to AWS service

- **Authentication**: A principal must be able to authenticate access to send requests to AWS.
  - With **Root user**: when logging in, you need information **email address and password**. (long-term certification information)
  - With **IAM user**: need account ID or alias information and **user + password** respectively. (long-term certification information)
  - To authenticate IAM user via AWS API or CLI, we can use **Access key** and **Secret access key** (long-term credentials) or use **IAM Role** and Temporary credentials are issued when we perform **assume role** operation through **AWS Security Token Service** (**AWS STS**)


{{< figure src="/images/sts.png" title="AWS STS" width=75pc >}}