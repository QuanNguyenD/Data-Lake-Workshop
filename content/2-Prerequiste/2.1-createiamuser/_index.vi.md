---
title : "Chuẩn bị IAM User"
date :  "2025-06-11"
weight : 1 
chapter : false
pre : " <b> 2.1 </b> "
---

### Tạo IAM User 
1. Truy cập giao diện [AWS Management Console](https://console.aws.amazon.com)
    - Tìm và chọn **IAM**


![IAM](/images/2.prerequisite/0001-createiam.png)

2. Trong giao diện **IAM** chọn **User** 

![IAM](/images/2.prerequisite/0002-createiam.png)

3. Trong giao diện **IAM User** chọn **Create User**

![IAM](/images/2.prerequisite/0003-createiamuser.png)

4. Trong giao diện tạo IAM user chúng ta làm theo các bước sau:

    - **User name** điền **data-lake-admin**
    - Tick vào **Provide user access to the AWS Management Console - optional**
    - Trong phần User type chọn **I want to create an IAM user**
    - Tại phần **Console password** bạn có thể để chọn tạo mật khẩu ngẫu nhiên hoạc theo cách thủ công

![IAM](/images/2.prerequisite/0004-createiamuser.png)

5. Trong phần **Set permissions** chọn **Attach policies directly** và thêm các **Permissions policies** sau:
    - **AmazonS3FullAccess**
    - **AmazonAthenaFullAccess**
    - **AWSGlueConsoleFullAccess**
    - **AWSLakeFormationDataAdmin**
    - **CloudWatchLogsFullAccess**

    Sau đó chọn **Next** và chọn create user trong phần **Review and create**

![IAM](/images/2.prerequisite/0005-createiamuser.png)

6. Trong phần **Retrieve password** bạn có thể chọn Download .csv file về máy và lưu nó ở một nơi an toàn.



