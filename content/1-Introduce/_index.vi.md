---
title : "Giới thiệu"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
**l AWS Identity and Access Management (IAM)** l AWS Identity and Access Management (IAM), bạn có thể chỉ định những cá nhân có quyền truy cập, loại dịch vụ và tài nguyên AWS họ có thể truy cập và điều kiện truy cập. IAM là một tính năng được cung cấp miễn phí của tài khoản AWS. 


🔹 Amazon S3 – Dịch vụ lưu trữ đối tượng linh hoạt
Amazon S3 (Simple Storage Service) là một dịch vụ lưu trữ đối tượng mạnh mẽ thuộc nền tảng AWS, cho phép bạn lưu trữ và truy xuất bất kỳ loại dữ liệu nào — từ hình ảnh, video, tệp văn bản đến các dữ liệu dung lượng lớn.
Dữ liệu được tổ chức trong các đơn vị gọi là "bucket", và có thể truy cập dễ dàng thông qua các liên kết URL hoặc thông qua API.

S3 cung cấp khả năng lưu trữ không giới hạn, với độ bền dữ liệu lên đến 99.999999999% (11 số 9), phù hợp cho cả lưu trữ dài hạn và các ứng dụng đòi hỏi độ tin cậy cao. Ngoài ra, S3 còn tích hợp tốt với các dịch vụ khác như AWS Lambda, CloudFront hay API Gateway, tạo nên một giải pháp toàn diện cho các hệ thống serverless hoặc hệ thống phân phối nội dung.

- Lợi ích nổi bật của S3:
Lưu trữ hàng triệu đến hàng tỷ đối tượng mà không lo giới hạn dung lượng.

Đảm bảo độ bền dữ liệu cực cao.

Mỗi tệp tin đều có thể được truy cập qua một đường dẫn duy nhất.

Hỗ trợ kiểm soát truy cập chi tiết bằng IAM, bucket policy hoặc ACL.

Dễ dàng tích hợp với các dịch vụ khác trong AWS như Lambda, Athena, API Gateway,…

🔹 Amazon API Gateway – Cầu nối giữa người dùng và backend
API Gateway là một dịch vụ quản lý API do AWS cung cấp, cho phép bạn xây dựng, triển khai và duy trì các API RESTful hoặc HTTP ở quy mô lớn.
Dịch vụ này hoạt động như một cổng trung gian giữa client (trình duyệt, ứng dụng mobile...) và backend (Lambda, EC2, hoặc các dịch vụ nội bộ khác).

API Gateway hỗ trợ quản lý version API, giới hạn tần suất truy cập (rate limiting), xác thực người dùng, ghi log chi tiết và bảo mật truy cập. Nhờ vậy, bạn có thể dễ dàng triển khai các API ổn định, bảo mật và có thể mở rộng theo nhu cầu thực tế.

🔹 AWS Lambda – Chạy code không cần máy chủ
AWS Lambda là dịch vụ điện toán serverless cho phép bạn chạy mã mà không cần triển khai hoặc quản lý máy chủ.
Lambda được kích hoạt bởi các sự kiện như: có yêu cầu từ API Gateway, một file được upload lên S3, hoặc một cron job định kỳ. Khi sự kiện xảy ra, Lambda sẽ tự động thực thi đoạn mã mà bạn đã định nghĩa sẵn.

Lambda hỗ trợ nhiều ngôn ngữ phổ biến như: Node.js, Python, Java, Go,... và rất phù hợp để xử lý các tác vụ ngắn gọn, tự động hoá, hoặc làm phần backend cho các ứng dụng web/mobile hiện đại.

 🔹Tổng kết
Việc kết hợp Amazon S3, API Gateway, và AWS Lambda tạo thành một kiến trúc serverless linh hoạt, giúp bạn:

Lưu trữ và phục vụ dữ liệu hiệu quả (S3).

Xây dựng các API truy cập hoặc xử lý dữ liệu (API Gateway).

Xử lý backend logic mà không cần quản lý hạ tầng (Lambda).

Đây là một giải pháp tối ưu cho các hệ thống hiện đại như: ứng dụng chia sẻ ảnh, nền tảng lưu trữ đám mây, hoặc backend cho mobile/web app. Nhờ khả năng mở rộng tự động và tích hợp sâu trong hệ sinh thái AWS, bạn có thể triển khai nhanh chóng, an toàn và tiết kiệm chi phí.

