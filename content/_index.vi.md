+++
title = "IAM Role & Condition"
weight = 1
chapter = false
+++

# IAM Role & Condition 

#### Tổng quan
Ở bài [Bắt đầu với IAM](https://000002.awsstudygroup.com/) chúng ta đã tạo IAM User có quyền admin cho mọi dịch vụ. Trong thực tế chúng ta thường chỉ cấp quyền vừa đủ (quyền tối thiểu - *least privilege*) cho người quản trị.

Trong bài này chúng ta sẽ cùng ôn lại khái niệm về IAM, sau đó tiến hành tạo User/Group đóng vai trò admin từng dịch vụ EC2 , RDS. Bước tiếp theo chúng ta tạo Role và tăng cường tính bảo mật bằng cách đặt thêm điều kiện giới hạn theo địa chỉ IP và thời gian.

{{< figure src="../images/serviceicon2.png" title="AWS IAM" width=150pc >}}


{{< figure src="/images/IAM.png" title="Assume Role Process" width=70% >}}
#### Nội dung
1. [Giới thiệu về IAM](1-iam-intro/)
2. [Tạo IAM Group](2-create-iam-group/)
3. [Tạo IAM User](3-create-iam-user/)
4. [Cấu hình IAM Role & Condition](4-configure-iam-role-with-condition/)
5. [Dọn dẹp tài nguyên](5-cleanup)