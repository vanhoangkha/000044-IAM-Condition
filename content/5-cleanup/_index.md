+++
title = "Clean up resources"
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

#### Clean up resources

You would clean up resources in the following order:

1. Delete role **lab44-RoleFullAccess**
     - Access to IAM Console
     - in the left sidebar, select **Roles**
     - Find and tick the role **lab44-RoleFullAccess**
     - Select Delete

2. Delete IAM users including **EC2-admin-user**, **RDS-admin-user**, **Group-user**, and **No-permission-user**.
     - Access to IAM Console
     - in the left sidebar, select **Users**
     - Tick the users related to the lab
     - Select Delete user

3. Delete User Group **ec2-rds-admin-group**
    - Access to IAM Console
     - in the left sidebar, select **User groups**
     - Tick the user group related to the lab
     - Select Delete