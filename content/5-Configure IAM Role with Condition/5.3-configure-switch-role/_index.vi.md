+++
title = "Cấu hình Switch role"
date = 2021
weight = 3
chapter = false
pre = "<b>5.3 </b>"
+++

#### Cấu hình Switch role cho IAM User
---
- Truy cập trang IAM console ở link https://console.aws.amazon.com/iam/home#/home, ở cột điều hướng bên trái, chọn **User**
- Bấm vào user mới tạo **asg-user4**, sao chép thông tin **User ARN**
- Tại cột điều hướng bên trái, bấm chọn **Roles**, rồi chọn IAM Role mới tạo **asg-RoleFullAccess**, sao chép thông tin **Role ARN** và **Instance Profile ARNs**
- Ở tab **Trust relationships**, bấm **edit trust relationship**
![6](/images/AssumeRole2.PNG?width=90pc)
- Bổ sung **AWS** với thông tin **User ARN** như hình bên dưới. Sau đó bấm **Update Trust Policy**
![7](/images/AssumeRole3.PNG?width=90pc)
Để kiểm tra assume role, ta thao tác như sau
- Thực hiện log in user **asg-user4**, sau đó bấm vào tên của user ở góc phải màn hình, chọn **Switch Role**
![8](/images/AssumeRole4.PNG?width=90pc)
- Tại màn hình **Switch Role**, nhập các thông tin theo yêu cầu bao gồm, **Account** là Account number, **Role** là tên của Role, **Display name** là tên hiển thị cho User sau khi switch role.
![9](/images/AssumeRole5.PNG?width=90pc)
- Bấm **Switch role** để thực hiện assume role cho user **asg-user4**. Thực hiện truy cập các dịch vụ cơ bản như S3 để xác nhận cấu hình Switch role thành công. Hình bên dưới thể hiện **asg-user4** sau khi switch role đã có khả năng tạo bucket.
![10](/images/AssumeRole6-success.PNG?width=90pc)
