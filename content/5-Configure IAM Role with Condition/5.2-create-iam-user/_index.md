+++
title = "Tạo IAM User"
date = 2021
weight = 2
chapter = false
pre = "<b>5.2 </b>"
+++

#### Tạo IAM User
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
