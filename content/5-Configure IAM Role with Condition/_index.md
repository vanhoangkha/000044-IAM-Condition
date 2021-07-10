+++
title = "Cấu hình IAM Role Condition"
date = 2021
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

#### Cấu hình IAM Role Condition 

Việc sử dụng Role là một phương pháp thực hành tốt trong hệ thống AWS. Ở bước này chúng ta không chỉ cấu hình cho phép người dùng sử dụng ( assume ) 1 role cụ thể bất cứ lúc nào mà còn thêm vào các Condition ( điều kiện ). Chỉ khi thỏa điều kiện về địa chỉ IP hoặc thời gian, người dùng mới có thể thực hiện switch role.
Để hiểu cách switch role, bạn có thể xem lại bài [Bắt đầu với IAM](https://000002.awsstudygroup.com/)

- [Tạo IAM Role có quyền Quản trị](5.1-iam-admin-role/)
- [Tạo IAM User](5.2-create-iam-user/)
- [Cấu hình Switch role cho IAM User](5.3-configure-switch-role/)
- [Giới hạn IP được phép Switch role](5.4-condition-ip/)
- [Giới hạn Thời gian được phép Switch role](5.5-condition-time/)
