+++
title = "Request tới AWS service"
weight = 1
chapter = false
pre = "<b>1.1 </b>"
+++

#### Request tới AWS service

- **Request**: Khi một principal cố gắng thực hiện một thao tác sử dụng AWS Console, AWS API hoặc AWS CLI, principal đó sẽ phải gửi đi một request. Thông tin Request bao gồm
	- **Action** or **Operation**: hành động mà principal muốn thực hiện. 
	- **Resource**: thông tin tài nguyên sẽ bị tác động
	- **Principal**: thông tin về người hoặc ứng dụng gửi đi yêu cầu, bao gồm cả thông tin policy đã được attach với principal đó
	- **Environment data**: thông tin về địa chỉ IP, user agent, trạng thái enable SSL và thời điểm gửi request
	- **Resource data**: thông tin liên quan đến tài nguyên mà có thể đc request. Ví dụ tên của bảng dữ liệu DynamoDB, hay tên tag của máy ảo EC2
