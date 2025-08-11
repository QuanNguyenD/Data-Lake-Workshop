---
title : "Chuẩn bị IAM User"
date :  "2025-06-11"
weight : 1 
chapter : false
pre : " <b> 2.1 </b> "
---

### Create IAM User
1. Access the [AWS Management Console](https://console.aws.amazon.com) interface
- Find and select **IAM**

![IAM](/Data-Lake-Workshop/images/2.prerequisite/0001-createiam.png)

2. In the **IAM** interface, select **User**

![IAM](/Data-Lake-Workshop/images/2.prerequisite/0002-createiam.png)

3. In the **IAM User** interface, select **Create User**

![IAM](/Data-Lake-Workshop/images/2.prerequisite/0003-createiamuser.png)

4. In the IAM user creation interface, we follow these steps:

- **User name** enter **data-lake-admin**
- Tick **Provide user access to the AWS Management Console - optional**
- In the User type section, select **I want to create an IAM user**
- In the **Console password** section, you can choose to create a random password or manually

![IAM](/Data-Lake-Workshop/images/2.prerequisite/0004-createiamuser.png)

5. In the **Set permissions** section, select **Attach policies directly** and add the following **Permissions policies**:
    - **AmazonS3FullAccess**
    - **AmazonAthenaFullAccess**
    - **AWSGlueConsoleFullAccess**
    - **AWSLakeFormationDataAdmin**
    - **CloudWatchLogsFullAccess**
Then select **Next** and select create user in the **Review and create** section

![IAM](/Data-Lake-Workshop/images/2.prerequisite/0005-createiamuser.png)

6. In the **Retrieve password** section you can choose to Download the .csv file to your computer and save it in a safe place.