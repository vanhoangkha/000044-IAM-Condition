+++
title = "Chứng thực các request "
weight = 2
chapter = false
pre = "<b>1.2 </b>"
+++

#### Chứng thực các request tới AWS service

- **Authentication**: Một principal phải có khả năng xác thực truy cập để có thể gửi request tới AWS. 
	- Với **Root user**: khi login cần thông tin **địa chỉ email và password**. ( thông tin chứng thực dài hạn) 
	- với **IAM user**: cần thông tin account ID hoặc alias, và **user + password** tương ứng. ( thông tin chứng thực dài hạn)
	- Để xác thực IAM user qua AWS API hay CLI, chúng ta có thể sử dụng **Access key** và **Secret access key** ( thông tin chứng thực dài hạn) hoặc sử dụng **IAM Role** và thông tin chứng thực tạm thời được cấp khi chúng ta thực hiện thao tác **assume role** thông qua dịch vụ **AWS Security Token Service** (**AWS STS**)


{{< figure src="/images/sts.png" title="AWS STS" width=75pc >}}