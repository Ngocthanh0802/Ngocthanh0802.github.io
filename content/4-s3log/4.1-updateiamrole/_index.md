---
title: "Configure API Gateway to Connect with Lambda"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 4.1 </b> "
---

1. Configuration
   - Select **API** from the left-hand navigation panel  
   ![API](/images/20.png)

   - On the API configuration page that we created, go to **Resources**

   - Proceed to **Create Resource**

   - Resource name: `files`

   - Finally, click **Create Resource**
   ![API](/images/21.png)

- You will be redirected back to the Resources interface and receive a success message

- Select `/files` → **Actions** → **Create Method** → select **POST** → click the green check mark  
  ![API](/images/22.png)

  Configuration:

  - Integration type: **Lambda Function**
  - **Use Lambda Proxy integration:** ENABLED
  - **Lambda Region:** us-east-1
  - **Lambda Function:** select `uploadImageToS3`

  Click **Create Method**  
  ![API](/images/23.png)  
  ![API](/images/24.png)  
  ![API](/images/25.png)

#### Repeat the same steps for the download function

2. **Deploy API**  
From the **Actions** menu → select **Deploy API**  
Create a new Stage:  
- Stage name: `dev`  
- Click **Deploy**

![API](/images/27.png)

**After deployment, you will receive an endpoint URL**  
![API](/images/28.png)
