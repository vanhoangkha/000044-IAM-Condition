+++
title = "Kiểm tra quyền"
weight = 2
chapter = false
pre = "<b>3.2 </b>"
+++

#### Kiểm tra quyền của User
Sau đây, bạn sẽ được hướng dẫn chi tiết cách đăng nhập vào IAM User, cụ thể là user **EC2-admin-user**.

1. Đăng nhập vào **IAM console** theo link https://console.aws.amazon.com/iam/home#/home
2. Ở thanh điều hướng bên trái, chọn **User**
3. Chọn vào **EC2-admin-user**

![3_UserInfo](/images/3_UserInfo.png?featherlight=false&featherlight=false&width=90pc)

4. Chọn vào tab **Security credentials**, copy đường link để đăng nhập cho user ở bên cạnh **Summary**

![3_Link](/images/3_Link.png?featherlight=false&featherlight=false&width=90pc)

5. Mở một tab broswer ở chế độ ẩn danh hoặc mở một broswer khác với broswer bạn đang sử dụng. Sau đó, truy cập vào đường link vừa copy ở trên.

6. Sử dụng username và password cho user **EC2-admin-user** để đăng nhập.

7. Lặp lại bước 1-6 để lần lượt đăng nhập vào các user khác

8. Sau khi đăng nhập thành công, bạn sẽ làm các bài kiểm tra sau để chắc chắn các user đã được cấu hình chính xác:
    - **EC2-admin-user**: khởi chạy thành công một EC2 instance
    - **RDS-admin-user**: khởi chạy thành công một RDS instance
    - **Group-user**: khởi chạy thành công một EC2 instance và một RDS instance
    - **No-permission-user**: không sử dụng được bất kỳ dịch vụ nào
