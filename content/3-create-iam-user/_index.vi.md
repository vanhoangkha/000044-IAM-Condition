+++
title = "Tạo IAM User"
weight = 3
chapter = false
pre = "<b>3. </b>"
+++

#### Tổng quan 

Ở phần này, bạn sẽ tạo ra bốn IAM User với các tên và mục đích như sau:
- **EC2-admin-user**: đây là user được gán quyền quản trị khi truy cập vào các dịch vụ thuộc EC2.
- **RDS-admin-user**: đây là user được gán quyền quản trị khi truy cập vào các dịch vụ thuộc RDS.
- **Group-user**: đây là user được gán quyền quản trị thông qua IAM User Group được tạo ở phần 2.
- **No-permission-user**: đây là user không có quyền gì cả. User sẽ này sẽ được dùng để tiếp nhận IAM role có quyền Admin ở phần 4.

#### Nội dung
- [Tạo các IAM User](3.1-createuser/)
- [Kiểm tra quyền User](3.2-verifyuseraccess/)
