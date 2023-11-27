+++
title = "Create IAM User"
weight = 3
chapter = false
pre = "<b>3. </b>"
+++

#### Overview

In this section, you will create four IAM Users with the following names and purposes:
- **EC2-admin-user**: This user is assigned administrative privileges for accessing services within EC2.
- **RDS-admin-user**: This user is assigned administrative privileges for accessing services within RDS.
- **Group-user**: This user is granted administrative privileges through an IAM User Group created in section 2.
- **No-permission-user**: This user has no permissions at all. It will be used to assume an IAM role with Admin privileges in section 4.

#### Contents
- [Create IAM Users](3.1-createuser/)
- [Verify User Access Rights](3.2-verifyuseraccess/)
