+++
title = "Cấu hình Switch role"
weight = 2
chapter = false
pre = "<b>4.2 </b>"
+++

#### Tổng quan
Ở bước này, bạn sẽ cấu hình role **lab44-RoleFullAccess** để cho phép user **No-permission-user** sử dụng được role này.

**Nội dung:**
- [Cấu hình Switch role](#cấu-hình-switch-role)

#### Cấu hình Switch role

1. Truy cập trang IAM console ở link https://console.aws.amazon.com/iam/home#/home
2. Ở thanh điều hướng bên trái, chọn **Users**
3. Bấm vào user **No-permission-user**, sao chép thông tin **User ARN**

![4.2_UserARN](/images/4.2_UserARN.png?width=90pc)

4. Tại thanh điều hướng bên trái, bấm chọn **Roles**, rồi chọn IAM Role mới tạo **lab44-RoleFullAccess**.

5. Chọn tab **Trust relationships** và chọn **Edit trust relationship**

![4.2_EditTrust](/images/4.2_EditTrust.png?width=90pc)

6. Bổ sung **AWS** với thông tin là **User ARN** của user **No-permission-user** như hình bên dưới. Sau đó bấm **Update Trust Policy**

![4.2_UpdatePolicy](/images/4.2_UpdatePolicy.png?width=90pc)

7. Như vậy, user **No-permission-user** đã có thể sử dụng role **lab44-RoleFullAccess**. Để kiểm tra assume role, ta thao tác như sau:
    - Thực hiện log in user **No-permission-user**, sau đó bấm vào tên của user ở góc phải màn hình, chọn **Switch Role**
    - Tại màn hình **Switch Role**, nhập các thông tin theo yêu cầu.
    - Bấm **Switch role** để thực hiện assume role cho user **No-permission-user**.
    - Thực hiện truy cập các dịch vụ cơ bản như EC2 hoặc RDS để xác nhận cấu hình Switch role thành công. Với quyền truy cập **AdministratorAccess**, user **No-permission-user** giờ đây có thể sử dụng bất kỳ dịch vụ nào.
