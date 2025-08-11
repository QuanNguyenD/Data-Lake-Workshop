---
title : "Prepare S3 "
date :  "2025-06-11"
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

### Prepare S3 bucket to store data:

Amazon S3 (Simple Storage Service) is a popular object storage service, often used as a storage platform for Data Lake. Creating an S3 bucket helps you store raw, semi-structured or unstructured data from many different sources, serving big data analysis.

In this article, we will divide data into 3 zones for effective management and processing:

1. Raw Zone:
- Stores original, unprocessed data from different sources (database, logs, IoT, ...).
- Data in raw form, not normalized or cleaned.
2. Processed Zone:
- Stores data that has been pre-processed such as cleaning, format conversion, error removal.
- The data here is ready for the next analysis steps.
3. Curated Zone
- Stores aggregated, standardized data, ready for in-depth analysis or reporting.
- Data in this zone is often of high quality and clearly structured.
### Implementation:

1. Access the [AWS Management Console](https://console.aws.amazon.com) interface

- Find and select **S3**
![S3](/Data-Lake-Workshop/images/4.s3/0001-creates3.png)
2. In the **S3** interface, select **Create bucket**
![S3](/Data-Lake-Workshop/images/4.s3/0002-creates3.png)
3. In the **Create bucket** interface

- **Bucket name** enter ``datalake-ecommerce-logs``
- Then select **Create bucket**
![S3](/Data-Lake-Workshop/images/4.s3/0003-creates3.png)
4. Successfully created bucket
![S3](/Data-Lake-Workshop/images/4.s3/0004-creates3.png)

5. After successfully creating a bucket, select the bucket you just created

- Select **Create folder**
- Enter the Folder name as ``data``
![S3](/Data-Lake-Workshop/images/4.s3/0006-creates3.png)

6. Folder created successfully
![S3](/Data-Lake-Workshop/images/4.s3/0007-creates3.png)

7. Select the **data** folder and select create folder

- Select Create folder
- In the Select Create folder interface, enter ``raw``
- Select create folder

![S3](/Data-Lake-Workshop/images/4.s3/0008-creates3.png)

8. Similar to creating ``processed`` and ``curated``
9. Successfully created 3 folders

![S3](/Data-Lake-Workshop/images/4.s3/0011-s3.png)

{{%notice tip%}}
These are the preparation steps, the following steps will be done on the created IAM User
{{%/notice%}}