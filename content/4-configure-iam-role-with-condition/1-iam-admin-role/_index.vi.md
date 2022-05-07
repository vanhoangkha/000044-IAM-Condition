+++
title = "Tạo Admin IAM Role "
weight = 1
chapter = false
pre = "<b>4.1 </b>"
+++
Ở bước này, bạn sẽ tạo một IAM Role có quyền Admin.

#### Tạo Admin IAM Role 

1. Đăng nhập vào IAM console theo link https://console.aws.amazon.com/iam/home#/home
2. Tại thanh điều hướng bên trái, chọn **Roles**, sau đó bấm **Create role**
3. Ở mục  **Select type of trusted entity**, chọn **AWS Service**. Ở mục **Choose a use case**, chọn **EC2**. Sau đó, chọn **Next: Permissions**.
{{% notice note %}}
Cần làm rõ một chút, **trusted entity** là thực thể được phép assume role. Mặc dù điều ta muốn là trusted entity là IAM User **No-permission-user**, tuy nhiên không có lựa chọn trực tiếp cho mong muốn này, do vậy ta chọn **EC2**.
{{% /notice %}}

![4.1_RoleUseCase](/images/4.1_RoleUseCase.png?width=90pc)

4. Tại mục **Attach permissions policies**, tìm và chọn **AdministratorAccess**. Sau đó, chọn **Next: Tags**. 

![4.1_RolePermission](/images/4.1_RolePermission.png?width=90pc)

5. Bỏ qua bước gán tag và bấm **Next: Review**

6. Tại trang **Review**, nhập tên của Role là **lab44-RoleFullAccess**. Sau đó, bấm **Create role** để kết thúc quá trình tạo Role

