+++
title = "Dọn dẹp tài nguyên  "
date = 2021
weight = 6
chapter = false
pre = "<b>6. </b>"
+++

1. Truy cập giao diện quản trị dịch vụ **S3**
- Click chọn S3 bucket chúng ta đã tạo cho bài thực hành. 
- Click Empty.
- Điền permanently delete, sau đó click Empty để tiến hành xóa object trong bucket.
- Click Exit.
2. Sau khi xóa hết object trong bucket, click Delete
   ![API](/images/30.png)
   ![API](/images/31.png)
   ![API](/images/32.png)
3. **Xoá Lambda**
- Trên **AWS Console:**

- Vào **AWS Lambda.**

- Chọn **Functions** → Chọn function bạn muốn xóa.

- Nhấn **Actions** → **Delete function.**

- Xác nhận xóa.
  ![API](/images/36.png)
  ![API](/images/37.png)
  ![API](/images/38.png)
4. Xóa **IAM Role**
- Trên **IAM:**

- Vào **IAM** → Chọn **Roles**

- Tìm role đã gán cho **Lambda.**

- Đảm bảo không dùng ở nơi khác.

- Nhấn **Delete.**
  ![API](/images/39.png)
  ![API](/images/40.png)
5. Xóa API Gateway (REST API hoặc HTTP API)
- Bước 1: Truy cập API Gateway
 Vào **AWS Console**

 Tìm và chọn dịch vụ **API Gateway**

- Bước 2: Chọn loại **API**
 Chọn tab **APIs**

 Chọn API bạn muốn xóa (ví dụ: upload-api, MyRestAPI, v.v.)

- Bước 3: Xóa **API**
 Nhấn vào tên **API** để vào trang chi tiết

 Nhấn **Actions** → chọn **Delete**

 Xác nhận xóa → **API** sẽ bị gỡ hoàn toàn khỏi hệ thống
  ![API](/images/33.png)
  ![API](/images/34.png)
  ![API](/images/35.png)
