+++
title = "Giới hạn theo Thời gian "
date = 2021
weight = 5
chapter = false
pre = "<b>5.5 </b>"
+++


#### Giới hạn Thời gian được phép Switch role
---
- Truy cập trang IAM console ở link https://console.aws.amazon.com/iam/home#/home với quyền user Admin
- Tại cột điều hướng bên trái, bấm chọn **Roles**, rồi chọn IAM Role mới tạo **asg-RoleFullAccess**
- Ở tab **Trust relationships**, bấm **edit trust relationship**, bổ sung **Condition** như bên dưới, sau đó bấm **Update Trust Policy**
![14](/images/AssumeRole10-Condition2.PNG?width=90pc)
- Sau khi cập nhật trust policy, phần **Condition** được bổ sung thông tin Date time được phép thực hiện switch role
![15](/images/AssumeRole11-Condition2.PNG?width=90pc)
- Trở lại phiên log in của user **asg-user4**, thực hiện lại việc switch role ta sẽ nhận được thông báo lỗi như hình bên dưới do thời điểm mà ta thực hiện Switch đã ngoài khoảng thời gian cho phép.
![13](/images/AssumeRole9-Condition1.PNG?width=90pc)