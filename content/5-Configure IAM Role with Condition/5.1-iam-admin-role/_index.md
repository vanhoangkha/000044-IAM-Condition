+++
title = "Tạo IAM Role có quyền Admin"
date = 2021
weight = 1
chapter = false
pre = "<b>5.1 </b>"
+++


#### Tạo IAM Role có quyền Admin
---
- Đăng nhập vào IAM console theo link https://console.aws.amazon.com/iam/home#/home
- Tại cột điều hướng bên trái, chọn **Roles**, sau đó bấm **Create role**
- Ở phần trusted entity, chọn **EC2**. 
  Cần làm rõ một chút, trusted entity là thực thể được phép assume role. Mặc dù điều ta muốn là trusted entity là IAM User, tuy nhiên không có lựa chọn trực tiếp cho mong muốn này, do vậy ta chọn **EC2**.
![1](/images/create-role1.PNG?width=90pc)
- Bấm **Next: Permission**. Tại mục **Attach permissions policies**, chọn **AdminstratorAccess** 
![2](/images/create-role2.PNG?width=90pc)
- Bấm **Next: Tags** để nhập thông tin Tag (nếu cần). Sau đó bấm **Next: Review**
- Tại trang **Review**, nhập tên của Role, **asg-RoleFullAccess**, sau đó bấm **Create role** để kết thúc quá trình tạo Role
![3](/images/create-role3.PNG?width=90pc)
