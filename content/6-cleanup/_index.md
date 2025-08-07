+++
title = "Cleaning Up Resources"
date = 2021
weight = 6
chapter = false
pre = "<b>6. </b>"
+++

1. **Access the S3 Management Console**
- Click on the S3 bucket you created for the practice.
- Click **Empty**.
- Type `permanently delete`, then click **Empty** to delete all objects in the bucket.
- Click **Exit**.

2. After deleting all objects, click **Delete** to remove the bucket.
   ![API](/images/30.png)  
   ![API](/images/31.png)  
   ![API](/images/32.png)

3. **Delete Lambda Function**
- In the **AWS Console**:
  - Go to **AWS Lambda**.
  - Select **Functions** → Choose the function you want to delete.
  - Click **Actions** → **Delete function**.
  - Confirm the deletion.
   ![API](/images/36.png)  
   ![API](/images/37.png)  
   ![API](/images/38.png)

4. **Delete IAM Role**
- In **IAM**:
  - Go to **IAM** → Select **Roles**
  - Find the role associated with your **Lambda function**
  - Make sure it’s not being used elsewhere.
  - Click **Delete**.
   ![API](/images/39.png)  
   ![API](/images/40.png)

5. **Delete API Gateway (REST API or HTTP API)**
- Step 1: Access **API Gateway**
  - In the **AWS Console**, find and select the **API Gateway** service.

- Step 2: Select the API type
  - Click on the **APIs** tab.
  - Select the API you want to delete (e.g., `upload-api`, `MyRestAPI`, etc.)

- Step 3: Delete the API
  - Click on the **API name** to open its details.
  - Click **Actions** → Select **Delete**.
  - Confirm the deletion → The API will be completely removed from the system.
   ![API](/images/33.png)  
   ![API](/images/34.png)  
   ![API](/images/35.png)
