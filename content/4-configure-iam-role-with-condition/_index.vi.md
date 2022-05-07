+++
title = "Cấu hình Role Condition"
weight = 4
chapter = false
pre = "<b>4. </b>"
+++

#### Tổng quan

Việc sử dụng Role là một phương pháp thực hành tốt trong hệ thống AWS. Ở bước này chúng ta không chỉ cấu hình cho phép người dùng sử dụng (*assume*) 1 role cụ thể bất cứ lúc nào mà còn thêm vào các Condition (*điều kiện*). Chỉ khi thỏa điều kiện về địa chỉ IP hoặc thời gian, người dùng mới có thể thực hiện switch role.
Để hiểu cách switch role, bạn có thể xem lại bài [Bắt đầu với IAM](https://000002.awsstudygroup.com/vi/).

**Nội dung:**

- [4.1 Tạo IAM Role có quyền Quản trị](1-iam-admin-role/)
- [4.2 Cấu hình Switch role cho IAM User](2-configure-switch-role/)
- [4.3 Giới hạn truy cập role](3-condition/)
