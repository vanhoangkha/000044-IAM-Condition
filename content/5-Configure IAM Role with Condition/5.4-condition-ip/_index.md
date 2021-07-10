+++
title = "Giới hạn theo IP"
date = 2021
weight = 4
chapter = false
pre = "<b>5.4 </b>"
+++

#### Giới hạn IP được phép Switch role
---
- Truy cập trang IAM console ở link https://console.aws.amazon.com/iam/home#/home với quyền user Admin
- Tại cột điều hướng bên trái, bấm chọn **Roles**, rồi chọn IAM Role mới tạo **asg-RoleFullAccess**
- Ở tab **Trust relationships**, bấm **edit trust relationship**, bổ sung **Condition** như bên dưới, sau đó bấm **Update Trust Policy**
![11](/images/AssumeRole7-Condition1.PNG?width=90pc)
- Sau khi cập nhật trust policy, phần **Condition** được bổ sung thông tin IP được phép thực hiện switch role
![12](/images/AssumeRole8-Condition1.PNG?width=90pc)
- Trở lại phiên log in của user **asg-user4**, thực hiện lại việc switch role ta sẽ nhận được thông báo lỗi như hình bên dưới do ta đang truy cập dịch vụ từ thiết bị không có IP như trong điều kiện.
![13](/images/AssumeRole9-Condition1.PNG?width=90pc)
