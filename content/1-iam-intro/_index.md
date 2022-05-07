+++
title = "Introduction about IAM"
weight = 1
chapter = false
pre = "<b>1. </b>"
+++

#### Definition of IAM
- A tool that controls how people or programs use AWS infrastructure
- Maintain the definition of traditional authentication such as User, Group, and access control policy to control AWS account, service

#### Application of IAM
- IAM does not have the ability to authenticate to the application. For example, in an on-prem system, an application-like software that uses AD as an authentication system, when moving to the AWS cloud, will need to be deployed AWS Directory Service (install & migrate).

- IAM cannot manage authentication for the operating system. After the servers in the on-prem system are migrated to EC2, access to EC2 can be via AD or LDAP that has been extended from the on-prem system or run standalone.

- Authentication technology:
    - Authentication to access Operating System >>>> AD or LDAP (Light weight Access protocol)
    - Authenticate Access to Application >>>> AD or Application User Repo or Amazon Cognito
    - AWS Resource Access Authentication >>>> IAM
Like most AWS services, IAM can be controlled through:
- AWS Management Console
- CLI - scripting tool
- AWS SDKs
- Some important operations are often done with IAM such as: Create User, Group, Role, and Access policy

#### Some basic concepts related to IAM
- **Resource**: resources under the management of IAM. For example User, Group, Role, or Identity provider object. On IAM, it is possible to add, delete and edit any resource element.
- **Identities**: a resource managed with IAM that is used for identification or grouping. Identities include User, Group, and Role. A Policy can be assigned to an Identity.
- **Principal** is an instance of IAM, which can interact directly with AWS resources. 3 types of principals: Root user, IAM user, and Role

{{< figure src="/images/serviceicon.png" title="IAM Role" width=75pc >}}

- **Policy** defines your permission to access the resources in your AWS account. IAM Policy can be assigned to IAM Group, IAM User, and IAM Role.

{{< figure src="/images/policy.png" title="IAM Policy" width=75pc >}}