---
title : "Cấu hình API Gateway"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 4. </b> "
---


**API Gateway là gì?**
Amazon API Gateway là dịch vụ giúp bạn tạo, quản lý và bảo mật các API để kết nối giữa client (frontend) và backend như Lambda, EC2, hoặc các dịch vụ AWS khác.

**Tác dụng:**
- Là cổng giao tiếp giữa người dùng và backend

- Xử lý các request HTTP/RESTful

- Hỗ trợ xác thực, giới hạn tốc độ (rate limiting), logging...

**Ví dụ:**
- Bạn tạo một API POST /upload-image
- API Gateway nhận yêu cầu từ client
- Gửi tiếp tới Lambda để xử lý
- Lambda upload ảnh lên S3
- Trả kết quả lại cho client

**Các dịch vụ thường dùng chung:**

- AWS Lambda – Xử lý logic backend

- Amazon S3 – Lưu trữ file

- IAM – Cấp quyền truy cập API

- CloudWatch – Ghi log và giám sát API

- Cognito – Xác thực người dùng nếu cần

**Tóm lại:**
**API Gateway giúp xây dựng API nhanh chóng, dễ quản lý và dễ tích hợp với các dịch vụ AWS — là thành phần quan trọng trong mô hình serverless.**