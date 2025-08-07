---
title : "Cấu hình API Gateway để Kết nối với Lambda"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 4.1 </b> "
---

1. Cấu Hình
   - Chọn **API** ở thanh chức năng bên trái 
  ![API](/images/20.png)

  - Tại trang cấu hình cho API chúng ta tạo , truy cập vào Resources

  - Tiến hành **Create resources**

  - Resource name : files

  - Cuối là **Create reosources**
  ![API](/images/21.png)
  
- Sau đó sẽ trả về lại giao diện Resources và thông báo tạo thành công

- Chọn /files → **Actions** → **Create Method** → chọn **POST** → nhấn tick xanh
 ![API](/images/22.png)
  
  Cấu hình:

Integration type: **Lambda Function**

**Use Lambda Proxy integration:**  BẬT

**Lambda Region:** us-east-1

**Lambda Function:** chọn uploadImageToS3

Nhấn **Create Method**
 ![API](/images/23.png)
 ![API](/images/24.png)
 ![API](/images/25.png)

#### Làm tương tự với download function


2. **Deploy API**
Trên thanh menu **Actions** → chọn **Deploy API**
Tạo một Stage mới:
Stage name: dev
Nhấn Deploy

![API](/images/27.png)

**Sau khi deploy xong thì bạn sẽ nhận được 1 đường link**
![API](/images/28.png)