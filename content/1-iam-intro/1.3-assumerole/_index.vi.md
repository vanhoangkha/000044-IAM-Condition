+++
title = "Quá trình assume role"
weight = 3
chapter = false
pre = "<b>1.3 </b>"
+++

#### Quá trình assume role

- Trong phần này chúng ta sẽ cùng tìm hiểu quá trình một IAM User thực hiện assume role và lấy thông tin chứng thực tạm thời như thế nào nhé.

{{< figure src="/images/IAM.png" title="Assume Role Process" width=70% >}}

1. IAM user sẽ có thông tin chứng thực dài hạn ( password / acccesskey & secretaccesskey ) và sẽ dùng thông tin chứng thực dài hạn đó để request tới AWS Security Token Service ( AWS STS ) và thực hiện action sts:AssumeRole.
2. STS sẽ thực hiện kiểm tra xem IAM user có quyền để thực hiện action này hay không thông qua kiểm tra Trust Relationship ( gán vào Role ) và Identity Policy ( gán vào IAM User )
3. Nếu quá trình STS kiểm tra thành công, STS sẽ trả về thông tin chứng thực tạm thời.
4. IAM user sẽ sử dụng thông tin chứng thực tạm thời để thực hiện các request ( API call ) tới các dịch vụ của AWS.( IAM User ở thời điểm này sẽ có các quyền hạn được gán vào IAM role mà IAM User đã assume)



