---
title : "Create IAM Role"
date :  "2025-06-11"
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

### Create IAM Role

In this step we will create an IAM Role. This role will allow AWS Glue to access data in S3 and create the necessary objects in the Glue Catalog.

1. Access the [AWS Management Console](https://console.aws.amazon.com) interface
- Find and select **IAM**

2. In the **IAM** interface, select **Role** then select **Crete Role**

![IAM](/Data-Lake-Workshop/images/2.prerequisite/0006-createiamrole.png)

3. In the **Select trusted entity** step:

- Select **Select AWS service**
- In **Service or use case** select **Glue**
- Then select **Next**

![IAM](/Data-Lake-Workshop/images/2.prerequisite/0007-createiamrole.png)

4. In the **Add permissions** step:

- Find and select **AmazonAthenaFullAccess**, **AmazonS3FullAccess**, **AWSGlueServiceRole**

Then select **Next**
5. In the **Name, review, and create** step:

- Role name fill in: **GlueDataLakeRole**

Then select **Create role**

![IAM](/Data-Lake-Workshop/images/2.prerequisite/0008-createiamrole.png)

6. So we have completed creating **IAM Role**