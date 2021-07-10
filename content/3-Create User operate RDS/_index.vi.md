+++
title = "Tạo User có quyền operate RDS"
date = 2020-05-14T00:38:32+07:00
weight = 3
chapter = true
pre = "<b>3. </b>"
+++

#  Tạo User có quyền operate RDS
---
- Tương tự cách tạo User có quyền operate EC2, ở cột điều hướng bên trái, chọn **User**, sau đó bấm **Add User**
- Tại trang Details, ta thao tác: 
	- Thông tin **User name**, nhập **asg-user2**
	- Bấm chọn check box cho **AWS Management Console access**, chọn **Custom password**, sau đó nhập password vào text box. 
	- Tiếp theo, bỏ chọn **Require password reset** để không phải thay đổi mật khẩu ở lần Log in đầu tiên
	- Bấm **Next: Permission**
- Tại trang **Permissions**, ta thao tác :
    - Chọn **Attach existing policies directly** 
	- Trong vùng text box của **Filter Policies**, nhập **RDS** rồi chọn **AmazonRDSFullAccess** và **DatabaseAdministrator**
![1](/images/create-user4.PNG?width=90pc) ![2](/images/create-user5.PNG?width=90pc)
	- Bấm **Next: Tags** để nhập thông tin Tag (nếu cần). Sau đó bấm **Next: Review**
![3](/images/create-user6.PNG?width=90pc)
	- Bấm **Create User**. Thực hiện lưu thông tin **Access Key ID** và **Secret Access Key** rồi bấm **Close** để kết thúc quá trình tạo User mới
- Để tra permissions, ta thực hiện log in vào user mới, chọn dịch vụ RDS rồi thực hiện tạo một RDS intance mới. 
