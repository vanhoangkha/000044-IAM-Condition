+++
title = "Giới thiệu về IAM"
weight = 1
chapter = false
pre = "<b>1. </b>"
+++

#### Định nghĩa về IAM
- Là công cụ kiểm soát cách con người hoặc chương trình sử dụng hạ tầng của AWS
- Vẫn giữ nguyên định nghĩa về xác thực truyền thống như User, Group và chính sách kiểm soát truy cập để kiểm soát AWS account, service 

#### Ứng dụng của IAM
- IAM không có khả năng xác thực đối với ứng dụng. Ví dụ ở hệ thống on-prem, 1 ứng dụng như phần mềm sử dụng AD làm hệ thống xác thực, thì khi chuyển lên AWS cloud sẽ cần triển khai 
AWS Directory Service (cài đặt & migrate). 

- IAM không có khả năng quản lý xác thực đối với hệ điều hành. Sau khi các máy chủ ở hệ thống on-prem được migrate lên EC2, việc truy cập vào EC2 có thể thông qua AD hoặc LDAP đã được extend từ hệ thống on-prem hoặc chạy standalone.

- Công nghệ xác thực: 
    - Xác thực truy cập Hệ Điều Hành >>>> AD hoặc LDAP (Light weight Access protocol)
    - Xác thực truy cập Ứng dụng >>>> AD hoặc Application User Repo hoặc Amazon Cognito
    - Xác thực truy cập AWS Resource >>>> IAM
- Giống như hầu hết các service của AWS, IAM có thể được điểu khiển thông qua: 
	- AWS Management Console
	- CLI - công cụ scripting
	- AWS SDKs
- Một số thao tác quan trọng thường làm với IAM như: Tạo User, Group, Role, Access policy

#### Một số khái niệm cơ bản liên quan đến IAM
- **Resource**: tài nguyên thuộc quản lý của IAM. Ví dụ như User, Group, Role hoặc một Identity provider object. Trên IAM có thể thêm xóa sửa bất cứ thành phần tài nguyên nào.
- **Identities**: một tài nguyên được quản lý với IAM mà được sử dụng cho việc định danh hoặc phân nhóm. Identities bao gồm User, Group và Role. Một Policy có thể được gán cho một Identities.
- **Principal** là một thực thể của IAM, là đối tượng có khả năng tương tác trực tiếp với các AWS resource. 3 loại principal: Root user, IAM user và Role

{{< figure src="/images/serviceicon.png" title="IAM Role" width=75pc >}}

- **Policy** cấp quyền cho phép bạn truy cập các tài nguyên trong AWS account của bạn. IAM Policy có thể gán cho IAM Group, IAM User và IAM Role.

{{< figure src="/images/policy.png" title="IAM Policy" width=75pc >}}

