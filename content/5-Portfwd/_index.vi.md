---
title : "Triển khai trên Postman"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---

#### Test API trên PostMan

1.Tải ảnh lên postman




- Tiếp theo cùng tiến hành trên PostMan
    + Method : POST
    + URL : API vừa tạo
    + Header : "" Content-Type: application/json ""
    + Body :


- Đường link của Post API

![Link](/images/0000.png)

- Sau đó nhấn Send và kết quả sẽ được hiển thị bên dưới :

![Link](/images/111.png)

1. Kiểm tra kết quả trên S3
- Sai khi Post man thông báo upload thành công thì chúng ta qua S3 kiểm tra kết quả ảnh đã lên chưa
- Như trong hình ảnh là đã thành công
![Link](/images/2222.png)




#### Vậy là bạn đã thực hiện upload ảnh lên S3 thành công

3.Tải ảnh về postman

 


- Tiếp theo cùng tiến hành trên PostMan
    + Method : GET
    + URL : API vừa tạo
    + Header : "" Content-Type: text/plain ""
    + Body :


- Đường link của GET API
![Link](/images/5555.png)
- Sau đó nhấn Send và kết quả sẽ được hiển thị bên dưới :
![Link](/images/1128.png)
#### Vậy là bạn đã thực hiện download ảnh lên S3 thành công