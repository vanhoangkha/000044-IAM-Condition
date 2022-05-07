+++
title = "Giới hạn theo thời gian"
weight = 2
chapter = false
pre = "<b>4.3.2 </b>"
+++

#### Giới hạn Thời gian được phép Switch role

1. Truy cập trang IAM console ở link https://console.aws.amazon.com/iam/home#/home với quyền user Admin
2. Tại thanh điều hướng bên trái, bấm chọn **Roles**, rồi chọn IAM Role mới tạo **lab44-RoleFullAccess** 
3. Ở tab **Trust relationships**, bấm **Edit trust relationship**, bổ sung **Condition** như bên dưới, sau đó bấm **Update Trust Policy**

![4.3_TimeCondition](/images/4.3_TimeCondition.png?width=90pc)

4. Sau khi cập nhật trust policy, phần **Condition** được bổ sung thông tin Date time được phép thực hiện switch role

![4.3_TimeTrust](/images/4.3_TimeTrust.png?width=90pc)

5. Trở lại phiên log in của user **No-permission-user**, thực hiện lại việc switch role ta sẽ nhận được thông báo lỗi như hình bên dưới do thời điểm mà ta thực hiện Switch đã ngoài khoảng thời gian cho phép.

![4.3_Error](/images/4.3_Error.png?width=90pc)

