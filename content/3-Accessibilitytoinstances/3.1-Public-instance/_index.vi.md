---
title : "Cấu hình cho Lambda"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 3.1. </b> "
---
1. Truy cập vào Lambda và chọn function
- Mở dịch vụ Lambda trong **AWS Console.**

- Ở menu bên trái, chọn **Functions.**

- Tìm **function** bạn đã tạo, ví dụ: **UploadFunction**

- Nhấn vào tên **function** để xem thông tin tổng quan và cấu hình.
 ![Lambda](/images/12.png)
2. Cấu hình **Lambda**
Tại đây chính là phần mà bạn có thể thao tác các dòng lệnh code để lập trình bằng ngôn ngữ **Python** như đã cấu hình ở phần trước đó:
 ![Lambda](/images/14.png)
 **Dưới đây là đoạn code tham khảo của Upload Function**
 
 
///
import json

import boto3

import base64

s3 = boto3.client('s3')

BUCKET_NAME = 'ngocthanh0802'

def lambda_handler(event, context):
    try:
        if 'queryStringParameters' not in event or 'fileName' not in event['queryStringParameters']:
            return {
                'statusCode': 400,
                'body': json.dumps({'error': 'Missing fileName in query parameters'})
            }

        file_name = event['queryStringParameters']['fileName']

        if 'body' not in event:
            return {
                'statusCode': 400,
                'body': json.dumps({'error': 'Missing file content in body'})
            }

        if event.get('isBase64Encoded', False):
            file_content = base64.b64decode(event['body'])
        else:
            file_content = event['body'] if isinstance(event['body'], bytes) else event['body'].encode('utf-8')

        content_type = 'application/octet-stream'
        if file_name.lower().endswith(('.jpg', '.jpeg')):
            content_type = 'image/jpeg'
        elif file_name.lower().endswith('.png'):
            content_type = 'image/png'
        elif file_name.lower().endswith('.gif'):
            content_type = 'image/gif'
        elif file_name.lower().endswith('.txt'):
            content_type = 'text/plain'

        s3.put_object(
            Bucket=BUCKET_NAME,
            Key=file_name,
            Body=file_content,
            ContentType=content_type
        )

        return {
            'statusCode': 200,
            'body': json.dumps({'message': f'File {file_name} uploaded successfully!'}),
            'headers': {
                'Content-Type': 'application/json'
            }
        }

    except Exception as e:
        return {
            'statusCode': 500,
            'body': json.dumps({'error': f'Error uploading file: {str(e)}'}),
            'headers': {
                'Content-Type': 'application/json'
            }
        }
///
- Sau khi nhập vào trong phần Code Source theo cấu trúc trên bạn có thể tiến hành lưu lại cách thay đổi bằng cách:
- Bấm button Deploy hoặc tổ hợp phím (Ctrl + Shift + U)
- Đợi một vài giây, hệ thống sẽ lưu lại tất cả các thay đổi của bạn và trả về thông báo lưu thành công
 ![Lambda](/images/14.png)


**3.Tiếp tục cấu hình thêm Lambda Download Function**
Tại đây chính là phần mà bạn có thể thao tác các dòng lệnh code để lập trình bằng ngôn ngữ **Python** như đã cấu hình ở phần trước đó:
 ![Lambda](/images/15.png)
 **Dưới đây là đoạn code tham khảo của Download Function**
 
 \\\ 

import json

import boto3

import base64

s3 = boto3.client('s3')
BUCKET_NAME = 'ngocthanh0802'

def lambda_handler(event, context):
    
    try:
        
        # Kiểm tra fileName trong query parameters
        if 'queryStringParameters' not in event or 'fileName' not in event['queryStringParameters']:
            return {
                'statusCode': 400,
                'body': json.dumps({'error': 'Missing fileName in query parameters'}),
                'headers': {'Content-Type': 'application/json'}
            }

        file_name = event['queryStringParameters']['fileName']
        
        # Lấy file từ S3
        file_obj = s3.get_object(Bucket=BUCKET_NAME, Key=file_name)
        file_content = file_obj['Body'].read()
        
        # Xác định Content-Type dựa trên phần mở rộng file
        content_type = 'application/octet-stream'
        if file_name.lower().endswith(('.jpg', '.jpeg')):
            content_type = 'image/jpeg'
        elif file_name.lower().endswith('.png'):
            content_type = 'image/png'
        elif file_name.lower().endswith('.gif'):
            content_type = 'image/gif'
        
        return {
            'statusCode': 200,
            'body': base64.b64encode(file_content).decode('utf-8'),
            'isBase64Encoded': True,
            'headers': {
                'Content-Type': content_type,
                # Bỏ Content-Disposition để trình duyệt hiển thị trực tiếp
                'Cache-Control': 'max-age=3600'  # Cache hình ảnh trong 1 giờ
            }
        }
    except s3.exceptions.NoSuchKey:
        return {
            'statusCode': 404,
            'body': json.dumps({'error': 'File not found'}),
            'headers': {'Content-Type': 'application/json'}
        }
    except Exception as e:
        return {
            'statusCode': 500,
            'body': json.dumps({'error': f'Error retrieving file: {str(e)}'}),
            'headers': {'Content-Type': 'application/json'}
        }

\\\
 **Bạn đã hoàn thành bước cấu hình cho Lambda**