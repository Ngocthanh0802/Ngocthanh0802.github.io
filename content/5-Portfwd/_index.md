---
title: "Deploy on Postman"
date: "`r Sys.Date()`"
weight: 5
chapter: false
pre: "<b> 5. </b>"
---

#### Test API on Postman

1. Upload an image via Postman

- Let’s proceed with Postman:
  + Method: **POST**
  + URL: The API you just created
  + Header: `"Content-Type: application/json"`
  + Body:

- The URL of the POST API:

![Link](/images/0000.png)

- Then click **Send** and the result will be displayed below:

![Link](/images/111.png)

2. Check the result on S3  
- After Postman indicates the upload was successful, go to the S3 console to check if the image was uploaded.
- As shown in the image, the upload was successful:
![Link](/images/2222.png)

#### Congratulations, you have successfully uploaded an image to S3.

3. Download an image using Postman

- Let’s proceed again in Postman:
  + Method: **GET**
  + URL: The API you just created
  + Header: `"Content-Type: text/plain"`
  + Body:

- The URL of the GET API:
![Link](/images/5555.png)

- Then click **Send** and the result will be displayed below:
![Link](/images/1128.png)

#### Congratulations, you have successfully downloaded an image from S3.
