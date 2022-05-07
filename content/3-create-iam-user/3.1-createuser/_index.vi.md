+++
title = "Tạo các IAM User"
weight = 1
chapter = false
pre = "<b>3.1 </b>"
+++

#### Tạo các IAM User
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
