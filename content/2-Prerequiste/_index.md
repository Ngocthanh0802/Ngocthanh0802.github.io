---
title: "Preparation Steps"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

{{% notice info %}}
You need to create **one Linux instance in the public subnet** and **one Windows instance in the private subnet** to perform this lab.
{{% /notice %}}

To learn how to create EC2 instances and a VPC with public/private subnets, you can refer to the following labs:
- [Introduction to Amazon EC2](https://000004.awsstudygroup.com/vi/)
- [Working with Amazon VPC](https://000003.awsstudygroup.com/vi/)

To use **AWS Systems Manager** to manage the Windows instance specifically, and instances in general on AWS, you need to grant the necessary permissions for the instances to work with Systems Manager.

In this preparation section, we will also **create an IAM Role** to allow our instances to interact with Systems Manager.

### Content
- [Prepare VPC and EC2 Instances](2.1-createec2/)
- [Create IAM Role](2.2-createiamrole/)
