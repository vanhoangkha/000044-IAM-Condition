+++
title = "Tạo IAM User"
date = 2020-05-14T00:38:32+07:00
weight = 3
chapter = false
pre = "<b>3. </b>"
+++

#### Tổng quan 
Ở phần này, bạn sẽ tạo ra bốn IAM User với các tên và mục đích như sau:
- **EC2-admin-user**: đây là user được gán quyền quản trị khi truy cập vào các dịch vụ thuộc EC2.
- **RDS-admin-user**: đây là user được gán quyền quản trị khi truy cập vào các dịch vụ thuộc RDS.
- **Group-user**: đây là user được gán quyền quản trị thông qua IAM User Group được tạo ở phần 2.
- **No-permission-user**: đây là user không có quyền gì cả. User sẽ này sẽ được dùng để tiếp nhận IAM role có quyền Admin ở phần 4.

**Nội dung:**
- [Tạo IAM User](#tạo-iam-user)
- [Kiểm tra hoạt động của User](#kiểm-tra-hoạt-động-của-user)

#### Tạo IAM User
Sau đây, bạn sẽ được hướng dẫn chi tiết cách khởi tạo IAM user, cụ thể là user **EC2-admin-user**. Với các user còn lại, bạn sẽ có hướng dẫn chung về thông số khởi tạo.

1. Đăng nhập vào **IAM console** theo link https://console.aws.amazon.com/iam/home#/home
2. Ở thanh điều hướng bên trái, chọn **User**, sau đó bấm **Add User**

![3_AddUser](/images/3_AddUser.png?width=90pc)

3. Tại trang **Set user details**, nhập những thông tin sau: 
    - User name: **EC2-admin-user**
    - Access type: tick vào **AWS Management Console cccess** để cho phép user truy cập vào AWS Management Console
    - Console password: chọn **Custom password** và nhập mật khẩu tùy thích cho user
    - Require password reset: bỏ chọn lựa chọn này để user không cần phải đổi mật khẩu khi đăng nhập lần đầu
    - Kiểm tra và chọn **Next: Permissions**

![3_SetDetails](/images/3_SetDetails.png?width=90pc)

4. Tại trang **Set permissions**, ta thao tác:
    - Chọn **Attach existing policies directly** để chọn phương pháp gán quyền trực tiếp cho user.
	- Trong vùng search box bên cạnh **Filter Policies**, tìm và chọn **AmazonEC2FullAccess**
    - Kiểm tra và chọn **Next: Tags**

![3_SetPermission](/images/3_SetPermission.png?width=90pc)

5. Tại trang **Add tags (optional)**, giữ nguyên mặc định và chọn **Next: Review**

6. Tại trang **Review**, kiểm tra thông tin và chọn **Create user**

7. Khi quá trình khởi tạo hoàn thành, nhấn **Close** để trở về IAM Console.

Như vậy, bạn đã hoàn thành bước khởi tạo user. Để tạo các user còn lại, bạn cần lặp lại quy trình trên với thông số khác biệt sau cho **bước 3 và 4**:
- **RDS-admin-user**: 
    - **Bước 3**: Tại trang **Set user details**, nhập những thông tin sau: 
        - User name: **RDS-admin-user**
    - **Bước 4**: trang **Set permissions**, thao tác:
        - Chọn **Attach existing policies directly** 
        - Chọn **AmazonRDSFullAccess** và **DatabaseAdministrator**
- **Group-user**: 
    - **Bước 3**: Tại trang **Set user details**, nhập những thông tin sau: 
        - User name: **Group-user**
    - **Bước 4**: trang **Set permissions**, thao tác:
        - Chọn **Add user to group**
        - Tick vào group **ec2-rds-admin-group**
- **No-permission-user**: 
    - **Bước 3**: Tại trang **Set user details**, nhập những thông tin sau: 
        - User name: **No-permission-user**
    - **Bước 4**: bỏ qua và chọn **Next: Tags**

#### Kiểm tra hoạt động của User
Sau đây, bạn sẽ được hướng dẫn chi tiết cách đăng nhập vào IAM User, cụ thể là user **EC2-admin-user**.

1. Đăng nhập vào **IAM console** theo link https://console.aws.amazon.com/iam/home#/home
2. Ở thanh điều hướng bên trái, chọn **User**
3. Chọn vào **EC2-admin-user**

![3_UserInfo](/images/3_UserInfo.png?width=90pc)

4. Chọn vào tab **Security credentials**, copy đường link để đăng nhập cho user ở bên cạnh **Summary**

![3_Link](/images/3_Link.png?width=90pc)

5. Mở một tab broswer ở chế độ ẩn danh hoặc mở một broswer khác với broswer bạn đang sử dụng. Sau đó, truy cập vào đường link vừa copy ở trên.

6. Sử dụng username và password cho user **EC2-admin-user** để đăng nhập.

7. Lặp lại bước 1-6 để lần lượt đăng nhập vào các user khác

8. Sau khi đăng nhập thành công, bạn sẽ làm các bài kiểm tra sau để chắc chắn các user đã được cấu hình chính xác:
    - **EC2-admin-user**: khởi chạy thành công một EC2 instance
    - **RDS-admin-user**: khởi chạy thành công một RDS instance
    - **Group-user**: khởi chạy thành công một EC2 instance và một RDS instance
    - **No-permission-user**: không sử dụng được bất kỳ dịch vụ nào
