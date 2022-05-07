+++
title = "Create IAM User"
weight = 3
chapter = false
pre = "<b>3. </b>"
+++

#### Overview

In this section, you will create four IAM Users with the following names and purposes:
- **EC2-admin-user**: this is the user assigned administrative rights when accessing EC2 services.
- **RDS-admin-user**: this is the user assigned administrative rights when accessing RDS services.
- **Group-user**: this is the user assigned administrative rights through the IAM User Group created in part 2.
- **No-permission-user**: this is a user with no permissions at all. This user will be used to accept the IAM role with Admin rights in part 4.

#### Content
- [Create IAM Users](3.1-createuser/)
- [Check User Permissions](3.2-verifyuseraccess/)