---
title : "Tạo IAM Role"
date :  "2025-06-11"
weight : 2 
chapter : false
pre : " <b> 2.2 </b> "
---

### Tạo IAM Role

Trong bước này chúng ta sẽ tiến hành tạo IAM Role. Role này sẽ cho phép AWS Glue truy cập tới dữ liệu nằm trong S3 và tạo các đối tượng cần thiết trong Glue Catalog.

1. Truy cập giao diện [AWS Management Console](https://console.aws.amazon.com)
    - Tìm và chọn **IAM**

2. Trong giao diện **IAM** chọn **Role** sau đó chọn **Crete Role**

![IAM](/images/2.prerequisite/0006-createiamrole.png)

3. Trong bước **Select trusted entity**:

  - Chọn **Chọn AWS service**
  - Trong **Service or use case** chọn **Glue**
  - Sau đó chọn **Next**


![IAM](/images/2.prerequisite/0007-createiamrole.png)

4. Trong bước **Trong bước Add permissions** : 

  - Tìm và chọn **AmazonAthenaFullAccess**, **AmazonS3FullAccess**, **AWSGlueServiceRole**
  - Sau đó chọn **Next**
5. Trong bước **Name, review, and create**: 

  - Role name điền: **GlueDataLakeRole**
  - Sau đó chọn **Create role**

![IAM](/images/2.prerequisite/0008-createiamrole.png)

6. Vậy là chúng ta đã hoàn thành tạo **IAM Role**


 <!-- ```php 
php artisan make:controller FileUploadController
``` -->