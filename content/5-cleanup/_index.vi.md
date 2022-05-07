+++
title = "Dọn dẹp tài nguyên"
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

#### Dọn dẹp tài nguyên

Bạn sẽ dọn dẹp tài nguyên theo thứ tự sau đây:

1. Xóa role **lab44-RoleFullAccess**
    - Truy cập vào IAM Console
    - ở thanh bên trái, chọn **Roles**
    - Tìm và tick vào role **lab44-RoleFullAccess**
    - Chọn Delete

2. Xóa IAM user bao gồm **EC2-admin-user**, **RDS-admin-user**, **Group-user**, và **No-permission-user**.
    - Truy cập vào IAM Console
    - ở thanh bên trái, chọn **Users**
    - Tick vào các user liên quan tới bài lab
    - Chọn Delete user

3. Xóa User Group **ec2-rds-admin-group**
   - Truy cập vào IAM Console
    - ở thanh bên trái, chọn **User groups**
    - Tick vào user group liên quan tới bài lab
    - Chọn Delete