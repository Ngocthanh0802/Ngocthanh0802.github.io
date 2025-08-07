---
title : "Tạo S3 Bucket "
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 2.1.1 </b> "
---


#### Khởi tạo S3 Bucket dùng để lưu trữ hình ảnh và kết quả
Truy cập vào Console và tìm dịch vụ Amazon S3

- Truy cập vào trang [AWS Management Console](https://aws.amazon.com/vi/console/)
- Tiến hành đăng nhập tài khoản của bạn
- Sau khi đăng nhập thành công thì sẽ chuyển người dùng đến trang chính của AWS Manage Console như hình dưới :
![S3](/images/3.png)
- Tìm kiếm S3 trên thanh Search và chọn dịch vụ S3
![S3](/images/1.png)
- Chọn Create bucket và làm theo hướng dẫn
Cấu hình cho S3

Tại phần **General configuration:**

- AWS Region: tùy theo Region của bạn muốn sử dụng
- Bucket type: chọn General purpose
- Bucket name: my-file-sharing-bucket-amc0802
Tại phần **Object Ownership:**

- Chọn **ACLs disable (recommended)**
  ![S3](/images/4.png)
Tại phần **Block Public Access setting for this bucket:**

- Bỏ chọn **Block all public access**
- Tích chọn **I acknowledge that the current settings might result in this bucket and the objects within becoming public.**
 ![S3](/images/5.png)