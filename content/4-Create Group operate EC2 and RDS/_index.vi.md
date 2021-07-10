+++
title = "Tạo Group có quyền operate EC2 và RDS"
date = 2020-04-18T00:38:32+07:00
weight = 4
chapter = true
pre = "<b>4. </b>"
+++

#  Tạo Group có quyền operate EC2 & RDS 
---
- Truy cập trang IAM console ở link https://console.aws.amazon.com/iam/home#/home
- Tại cột điều hướng bên trái, chọn **Groups**, sau đó bấm **Create New Group**
- Thông tin **Group name**, nhập **asg-group1**
- Chuyển sang mục **Attach Policy**, nhập lần lượt filer "EC2" và "Data" để lấy các policy cấp quyền operate EC2 và RDS. Chọn **AmazonEC2FullAccess**, **AmazonRDSFullAccess** và **DatabaseAdministrator**, sau đó bấm **Next Step**
![1](/images/create-group1.PNG?width=90pc) ![2](/images/create-group2.PNG?width=90pc)
- Tại trang **Review**, kiểm tra thông tin lại lần cuối cùng, sau đó bấm **Create Group** để kết thúc quá trình tạo Group
![3](/images/create-group3.PNG?width=90pc)
- Để kiểm tra permissions đã cấp cho Group, thực hiện tạo User rồi truy cập các dịch vụ tương ứng
	- Tại cột điều hướng bên trái, chọn **User**, sau đó bấm **Add User**
	- Thông tin **User name**, nhập **asg-user3**
	- Bấm chọn check box cho **AWS Management Console access**, chọn **Custom password**, sau đó nhập password vào text box. 
	- Tiếp theo, bỏ chọn **Require password reset*** để không phải thay đổi mật khẩu ở lần Log in đầu tiên
	- Bấm **Next: Permission**, chọn **Add user to group** như mặc định. Bên dưới tích chọn tên Group mới tạo **asg-group1**. 
![4](/images/create-group4.PNG?width=90pc)
	- Bấm **Next: Tags** để nhập thông tin Tag (nếu cần). Sau đó bấm **Next: Review**
![5](/images/create-group5.PNG?width=90pc)
	- Bấm **Create User**. Thực hiện lưu thông tin **Access Key ID** và **Secret Access Key** rồi bấm **Close** để kết thúc quá trình tạo User mới
	- Thực hiện log in vào user mới tạo, chọn dịch vụ EC2 & RDS và thực hiện các thao tác kiểm thử. 
