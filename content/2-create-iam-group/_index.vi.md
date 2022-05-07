+++
title = "Tạo IAM Group"
weight = 2
chapter = false
pre = "<b>2. </b>"
+++

#### Tạo IAM Group
Ở phần này, bạn sẽ tạo IAM Group có quyền truy cập admin tới cả hai dịch vụ EC2 và RDS. 

1. Truy cập trang IAM console ở link https://console.aws.amazon.com/iam/home#/home
2. Tại thanh điều hướng bên trái, chọn **User groups**, sau đó bấm **Create group**

![2_CreateGroup](/images/2_CreateGroup.png?width=90pc)

3. Tại trang **Create user group**, nhập các thông tin sau:
    - User group name: **ec2-rds-admin-group**
    - Cuốn xuống mục **Attach permissions policies - Optional**, tìm và chọn các policy **AmazonEC2FullAccess**, **AmazonRDSFullAccess** và **DatabaseAdministrator**
    - Kiểm tra và bấm **Create group**

![2_GroupPolicy](/images/2_GroupPolicy.png?width=90pc)

Như vậy, bạn đã tạo thành công IAM Group.