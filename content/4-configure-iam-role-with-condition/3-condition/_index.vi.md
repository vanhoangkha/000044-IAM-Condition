+++
title = "Giới hạn truy cập role"
date = 2021
weight = 3
chapter = false
pre = "<b>4.3 </b>"
+++

#### Tổng quan

Ở bước này, bạn cấu hình lại role **lab44-RoleFullAccess** để siết chặt khả năng sử dụng role này theo địa chỉ IP và thờ gian.

**Nội dung:**

- [Giới hạn IP được phép Switch role](#giới-hạn-ip-được-phép-switch-role)
- [Giới hạn Thời gian được phép Switch role](#giới-hạn-thời-gian-được-phép-switch-role)

#### Giới hạn IP được phép Switch role

1. Truy cập trang IAM console ở link https://console.aws.amazon.com/iam/home#/home với quyền user Admin
2. Tại thanh điều hướng bên trái, bấm chọn **Roles**, rồi chọn IAM Role mới tạo **lab44-RoleFullAccess** 
3. Ở tab **Trust relationships**, bấm **Edit trust relationship**, bổ sung **Condition** như bên dưới, sau đó bấm **Update Trust Policy**

![4.3_IPCondition](/images/4.3_IPCondition.png?width=90pc)

4. Sau khi cập nhật trust policy, phần **Condition** được bổ sung thông tin IP được phép thực hiện switch role

![4.3_IPTrust](/images/4.3_IPTrust.png?width=90pc)

5. Trở lại phiên log in của user **No-permission-user**, thực hiện lại việc switch role ta sẽ nhận được thông báo lỗi như hình bên dưới do ta đang truy cập dịch vụ từ thiết bị không có IP như trong điều kiện.

![4.3_Error](/images/4.3_Error.png?width=90pc)

#### Giới hạn Thời gian được phép Switch role
1. Truy cập trang IAM console ở link https://console.aws.amazon.com/iam/home#/home với quyền user Admin
2. Tại thanh điều hướng bên trái, bấm chọn **Roles**, rồi chọn IAM Role mới tạo **lab44-RoleFullAccess** 
3. Ở tab **Trust relationships**, bấm **Edit trust relationship**, bổ sung **Condition** như bên dưới, sau đó bấm **Update Trust Policy**

![4.3_TimeCondition](/images/4.3_TimeCondition.png?width=90pc)

4. Sau khi cập nhật trust policy, phần **Condition** được bổ sung thông tin Date time được phép thực hiện switch role

![4.3_TimeTrust](/images/4.3_TimeTrust.png?width=90pc)

5. Trở lại phiên log in của user **No-permission-user**, thực hiện lại việc switch role ta sẽ nhận được thông báo lỗi như hình bên dưới do thời điểm mà ta thực hiện Switch đã ngoài khoảng thời gian cho phép.

![4.3_Error](/images/4.3_Error.png?width=90pc)

