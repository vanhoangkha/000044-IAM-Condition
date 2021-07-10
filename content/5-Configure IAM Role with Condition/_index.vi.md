+++
title = "Cấu hình IAM Role theo Điều kiện"
date = 2020-04-18T00:38:32+07:00
weight = 5
chapter = true
pre = "<b>5. </b>"
+++

#### Các bước thực hiện:

- [#### Bước 1: Tạo IAM Role có quyền Quản trị](#h4-idbước-1-tạo-iam-role-có-quyền-quản-trị-2bước-1-tạo-iam-role-có-quyền-quản-trịh4)
- [#### Bước 2: Tạo IAM User](#h4-idbước-2-tạo-iam-user-2bước-2-tạo-iam-userh4)
- [#### Bước 3: Cấu hình Switch role cho IAM User](#h4-idbước-3-cấu-hình-switch-role-cho-iam-user-2bước-3-cấu-hình-switch-role-cho-iam-userh4)
- [#### Bước 4: Cấu hình Condition 1 - Giới hạn IP được phép Switch role](#h4-idbước-4-cấu-hình-condition-1---giới-hạn-ip-được-phép-switch-role-2bước-4-cấu-hình-condition-1---giới-hạn-ip-được-phép-switch-roleh4)
- [#### Bước 5: Cấu hình Condition 2 - Giới hạn Thời gian được phép Switch role](#h4-idbước-5-cấu-hình-condition-2---giới-hạn-thời-gian-được-phép-switch-role-2bước-5-cấu-hình-condition-2---giới-hạn-thời-gian-được-phép-switch-roleh4)

---
#### Bước 1: Tạo IAM Role có quyền Quản trị
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

---
#### Bước 2: Tạo IAM User
---
- Truy cập trang IAM console ở link https://console.aws.amazon.com/iam/home#/home
- Thông tin **User name**, nhập **asg-user4**
- Bấm chọn check box cho **AWS Management Console access**, chọn **Custom password**, sau đó nhập password vào text box. 
- Tiếp theo, bỏ chọn **Require password reset*** để không phải thay đổi mật khẩu ở lần Log in đầu tiên
- Bấm **Next: Permission**, tuy nhiên ta bỏ qua bước cấu hình này để thực hiện assume role sau này.
- Bấm **Next: Tags** để nhập thông tin Tag (nếu cần). Sau đó bấm **Next: Review**
![4](/images/create-role4.PNG?width=90pc)
- Bấm **Create User**. Thực hiện lưu thông tin **Access Key ID** và **Secret Access Key** rồi bấm **Close** để kết thúc quá trình tạo User mới
Sau bước khởi tạo này, IAM User mới vẫn chưa có bất cứ quyền truy cập tới dịch vụ nào.
![5](/images/AssumeRole1.PNG?width=90pc)

---
#### Bước 3: Cấu hình Switch role cho IAM User
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

---
#### Bước 4: Cấu hình Condition 1 - Giới hạn IP được phép Switch role
---
- Truy cập trang IAM console ở link https://console.aws.amazon.com/iam/home#/home với quyền user Admin
- Tại cột điều hướng bên trái, bấm chọn **Roles**, rồi chọn IAM Role mới tạo **asg-RoleFullAccess**
- Ở tab **Trust relationships**, bấm **edit trust relationship**, bổ sung **Condition** như bên dưới, sau đó bấm **Update Trust Policy**
![11](/images/AssumeRole7-Condition1.PNG?width=90pc)
- Sau khi cập nhật trust policy, phần **Condition** được bổ sung thông tin IP được phép thực hiện switch role
![12](/images/AssumeRole8-Condition1.PNG?width=90pc)
- Trở lại phiên log in của user **asg-user4**, thực hiện lại việc switch role ta sẽ nhận được thông báo lỗi như hình bên dưới do ta đang truy cập dịch vụ từ thiết bị không có IP như trong điều kiện.
![13](/images/AssumeRole9-Condition1.PNG?width=90pc)

---
#### Bước 5: Cấu hình Condition 2 - Giới hạn Thời gian được phép Switch role
---
- Truy cập trang IAM console ở link https://console.aws.amazon.com/iam/home#/home với quyền user Admin
- Tại cột điều hướng bên trái, bấm chọn **Roles**, rồi chọn IAM Role mới tạo **asg-RoleFullAccess**
- Ở tab **Trust relationships**, bấm **edit trust relationship**, bổ sung **Condition** như bên dưới, sau đó bấm **Update Trust Policy**
![14](/images/AssumeRole10-Condition2.PNG?width=90pc)
- Sau khi cập nhật trust policy, phần **Condition** được bổ sung thông tin Date time được phép thực hiện switch role
![15](/images/AssumeRole11-Condition2.PNG?width=90pc)
- Trở lại phiên log in của user **asg-user4**, thực hiện lại việc switch role ta sẽ nhận được thông báo lỗi như hình bên dưới do thời điểm mà ta thực hiện Switch đã ngoài khoảng thời gian cho phép.
![13](/images/AssumeRole9-Condition1.PNG?width=90pc)