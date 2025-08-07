---
title: "Configure Lambda"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

### 1. Access Lambda and Select the Function

- Open the **Lambda** service in the **AWS Console**  
- From the left-hand menu, select **Functions**  
- Search for the function you created, for example: **UploadFunction**  
- Click the function name to view its overview and configuration  
  ![Lambda](/images/12.png)

---

### 2. Configure **Lambda**

Here is where you can enter code using the **Python** language, as configured earlier:  
  ![Lambda](/images/14.png)

**Sample code for the Upload Function**:

```python
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
