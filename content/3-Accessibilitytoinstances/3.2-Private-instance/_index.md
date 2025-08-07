---
title : "Granting Permissions to Lambda (in IAM Console)"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.2. </b> "
---

### Method 1: Grant Full S3 Access (Quick & Easy)

In the **IAM** interface, on the left sidebar, select **Roles**.

You will see a **Role** with the same name as the **Lambda function** you just created.

Click on that **Role**.

The result will look like this:

![Lambda](/images/17.png)

---

Once you’ve entered the Role's detail page:

- In the **Permissions policies** section:
- Click **Add permissions**, then choose **Attach policies**.
- ![Lambda](/images/18.png)

You will see the full list of **Permission Policies**.

- In the search bar, type **AmazonS3FullAccess**
- Select that policy and then click **Add permission**
