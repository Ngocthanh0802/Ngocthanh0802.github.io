---
title : "Cấp quyền cho Lambda(trong IAM Console)"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 3.2. </b> "
---
Cách 1: Cấp quyền toàn quyền **S3** (dễ, nhanh)
Trong giao diện **IAM** , tại thanh chức năng bên trái chọn Role

Bạn sẽ thấy Role có tên giống **function** mình vừa tạo

Tiến hành click vào **Role**

Kết quả như hình sau :
![Lambda](/images/17.png)

- Sau khi vào được giao diện của **Role** đó:

- Ở phần **Permissions policies:**

- Ta tiến hành chọn tác vụ **Add permission** sau đó chọn **Attach Policies**
- ![Lambda](/images/18.png)

Chúng ta sẽ thấy toàn bộ danh sách các **Permissions Policies**

- Trên thanh Seacrch, tiến hành tìm kiếm **AmazonS3FullAccess**
- Chọn policies đó và tiến hành **Add permission**