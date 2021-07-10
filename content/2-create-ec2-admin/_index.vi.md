+++
title = "Tạo User quản trị EC2"
date = 2021
weight = 2
chapter = true
pre = "<b>2. </b>"
+++

#  Tạo User quản trị dịch vụ EC2
---
#### Để vận hành bất cứ dịch vụ nào, User cần phải được cấp quyền thông qua policy. Policy được attach cho User có thể là trực tiếp hoặc gián tiếp. Đó là 
- Cấp quyền cho User thông qua Policy gán cho Group 
- Cấp quyền cho User bằng cách sao chép Policy từ một User khác
- Cấp quyền cho User bằng cách gán trực tiếp Policy

#### Các bước thực hiện cụ thể :
- Đăng nhập vào IAM console theo link https://console.aws.amazon.com/iam/home#/home
- Tại cột điều hướng bên trái, chọn **User**, sau đó bấm **Add User**
- Tại trang Details, ta thao tác: 
	- Thông tin **User name**, nhập **asg-user1**
	- Bấm chọn check box cho **AWS Management Console access**, chọn **Custom password**, sau đó nhập password vào text box. 
	- Tiếp theo, bỏ chọn **Require password reset** để không phải thay đổi mật khẩu ở lần Log in đầu tiên
	- Bấm **Next: Permission**
![1](/images/create-user1.PNG?width=90pc)
- Tại trang **Permissions**, ta thao tác :
    - Chọn **Attach existing policies directly** 
	- Trong vùng text box của **Filter Policies**, nhập **EC2** rồi chọn **AmazonEC2FullAccess**
![2](/images/create-user2.PNG?width=90pc)
	- Bấm **Next: Tags** để nhập thông tin Tag (nếu cần). Sau đó bấm **Next: Review**
![3](/images/create-user3.PNG?width=90pc)
	- Bấm **Create User**. Thực hiện lưu thông tin **Access Key ID** và **Secret Access Key** rồi bấm **Close** để kết thúc quá trình tạo User mới
![4](/images/create-user3-1.PNG?width=90pc)
- Để tra permissions, ta thực hiện log in vào user mới, chọn dịch vụ EC2 rồi thực hiện tạo một EC2 intance. 


