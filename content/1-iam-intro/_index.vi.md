+++
title = "Giới thiệu về IAM"
date = 2020-05-14T00:38:32+07:00
weight = 1
chapter = true
pre = "<b>1. </b>"
+++
  
#  Giới thiệu về IAM
---
- Là công cụ kiểm soát cách con người hoặc chương trình sử dụng hạ tầng của AWS
- Vẫn giữ nguyên định nghĩa về xác thực truyền thống như User, Group và chính sách kiểm soát truy cập để kiểm soát AWS account, service 
- Không có khả năng xác thực đối với ứng dụng. Ví dụ ở hệ thống on-prem, 1 ứng dụng như phần mềm sử dụng AD làm hệ thống xác thực, thì khi chuyển lên AWS cloud sẽ cần triển khai 
AWS Directory Service (cài đặt & migrate). Với hệ thống on-prem có ứng dụng di động, khi chuyển lên cloud sẽ dựng Amazon Coginito để kiểm soát việc xác thực đối với ứng dụng này. 
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
- Một số khái niệm cơ bản liên quan đến IAM
	- **Resource**: tài nguyên thuộc quản lý của IAM. Ví dụ như User, Group, Role hoặc một Identity provider object. Trên IAM có thể thêm xóa sửa bất cứ thành phần tài nguyên nào.
	- **Identities**: một tài nguyên được quản lý với IAM mà được sử dụng cho việc định danh hoặc phân nhóm. Identities bao gồm User, Group và Role. Một Policy có thể được gán cho một Identities.
	- **Entities**: cũng là một tài nguyên đc quản lý bởi IAM sử dụng cho việc xác thực. Entities bao gồm IAM User, Federated User và IAM role
	- **Principal** là một thực thể của IAM, là đối tượng có khả năng tương tác trực tiếp với các AWS resource. 3 loại principal: Root user, IAM user và Role
- Một số khái niệm khác
	- **Request**: Khi một principal cố gắng thực hiện một thao tác sử dụng AWS Console, AWS API hoặc AWS CLI, principal đó sẽ phải gửi đi một request. Thông tin Request bao gồm
		- **Action** or **Operation**: hành động mà principal muốn thực hiện. 
		- **Resource**: thông tin tài nguyên sẽ bị tác động
		- **Principal**: thông tin về người hoặc ứng dụng gửi đi yêu cầu, bao gồm cả thông tin policy đã được attach với principal đó
		- **Environment data**: thông tin về địa chỉ IP, user agent, trạng thái enable SSL và thời điểm gửi request
		- **Resource data**: thông tin liên quan đến tài nguyên mà có thể đc request. Ví dụ tên của bảng dữ liệu DynamoDB, hay tên tag của máy ảo EC2
	- **Authentication**: Một principal phải có khả năng xác thực truy cập để có thể gửi request tới AWS. 
		- Với **Root user**: khi login cần thông tin địa chỉ email và password
		- với **IAM user**: cần thông tin account ID hoặc alias, và user + password tương ứng
		- Để xác thực IAM user qua AWS API hay CLI, phải sử dụng **Access key** và **Secret key**. 

