---
title: "Create S3 Bucket"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 2.1.1 </b> "
---

#### Initialize an S3 Bucket for storing images and results

Access the AWS Console and search for the **Amazon S3** service:

- Visit the [AWS Management Console](https://aws.amazon.com/console/)
- Log in with your AWS account
- After a successful login, you will be redirected to the AWS Management Console homepage:
  ![S3](/images/3.png)

- Search for **S3** in the search bar and select the **S3** service  
  ![S3](/images/1.png)

- Click **Create bucket** and follow the setup instructions

**S3 Configuration:**

In the **General configuration** section:

- **AWS Region**: Select your preferred region  
- **Bucket type**: Choose **General purpose**  
- **Bucket name**: `my-file-sharing-bucket-amc0802`

In the **Object Ownership** section:

- Choose **ACLs disabled (recommended)**  
  ![S3](/images/4.png)

In the **Block Public Access settings for this bucket** section:

- Uncheck **Block all public access**
- Check **I acknowledge that the current settings might result in this bucket and the objects within becoming public.**  
  ![S3](/images/5.png)
