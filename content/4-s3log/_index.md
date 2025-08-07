---
title : "API Gateway Configuration"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

### 🔹 What is API Gateway?

**Amazon API Gateway** is a service that helps you create, manage, and secure APIs that connect clients (frontend) with backends like Lambda, EC2, or other AWS services.

---

### 🔹 Purpose

- Acts as a **gateway** between users and backend systems.
- **Handles HTTP/RESTful requests** efficiently.
- Supports features such as:
  - **Authentication**
  - **Rate limiting**
  - **Logging**
  - **Monitoring**

---

### 🔹 Example Scenario

- Create an API endpoint: `POST /upload-image`
- API Gateway receives the request from the frontend (client).
- Forwards the request to a Lambda function.
- Lambda processes the image upload to S3.
- The result is returned to the client via API Gateway.

---

### 🔹 Commonly Used Related Services

| AWS Service     | Main Purpose                      |
|------------------|------------------------------------|
| **Lambda**        | Handles backend logic              |
| **Amazon S3**     | Stores files (images, data, etc.)  |
| **IAM**           | Manages API access permissions     |
| **CloudWatch**    | Logs and monitors API activities   |
| **Cognito**       | Handles user authentication        |

---

### ✅ Summary

> **API Gateway enables fast, manageable, and easily integrated API development with AWS services — a key component in a serverless architecture.**
