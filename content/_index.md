+++
title = "IAM Role & Condition"
date = 2021
weight = 1
chapter = false
+++

# IAM Role & Condition 

Ở bài [Bắt đầu với IAM](https://000002.awsstudygroup.com/) chúng ta đã tạo IAM User có quyền admin cho mọi dịch vụ. Trong thực tế chúng ta thường chỉ cấp quyền vừa đủ ( tối thiểu ) cho người quản trị.
Trong bài này chúng ta sẽ cùng ôn lại khái niệm về IAM, sau đó tiến hành tạo User/Group đóng vai trò admin từng dịch vụ EC2 , RDS. Bước tiếp theo chúng ta tạo Role và tăng cường tính bảo mật bằng cách đặt thêm điều kiện giới hạn theo địa chỉ IP và thời gian.

1. [Khái niệm IAM](1-iam-intro/)
2. [Tạo User quản trị EC2](2-create-ec2-admin/)
3. [Tạo User quản trị RDS](3-create-rds-admin/)
4. [Tạo Group quản trị](4-create-group-ec2-rds/)
5. [Cấu hình IAM Role & Condition](5-configure-iam-role-condition/)