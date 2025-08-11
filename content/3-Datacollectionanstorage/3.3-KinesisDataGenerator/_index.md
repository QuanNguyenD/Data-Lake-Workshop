---
title : "Configuring Amazon Cognito for Kinesis Data Generator"
date :  "2025-06-11"
weight : 3
chapter : false
pre : " <b> 3.3 </b> "
---

### Steps

**First add IAM role for Iam users**

![Fire](/Data-Lake-Workshop/images/3.firehose/0011-fire.png)

1. Go to AWS Management Console.
- Search for CloudFormation.
- Select CloudFormation

![Fire](/Data-Lake-Workshop/images/3.firehose/0012-fire.png)

2. In the CloudFormation interface, select **Create stack**

![Fire](/Data-Lake-Workshop/images/3.firehose/0013-fire.png)

3. Proceed to download the file [setup](https://raw.githubusercontent.com/QuanNguyenD/FcjWS/refs/heads/main/cognito-setup.json)

4. In the **Create stack** interface:

- **Choose an existing template**
- In the **Specify template** section, select **Upload a template file**
- In the **Choose file** section, select the previously downloaded file

Click **Next**
5. In the **Specify stack details** interface
- Enter stack name ```Kinesis-Data-Generator-Cognito-User```
- User name enter ```admin```
- Password enter your password

Select **Next**
![Fire](/Data-Lake-Workshop/images/3.firehose/0014-fire.png)

6. Continue to select **Next** and **Submit**

![Fire](/Data-Lake-Workshop/images/3.firehose/0016-fire.png)
![Fire](/Data-Lake-Workshop/images/3.firehose/0015-fire.png)

7. Created successfully

![Fire](/Data-Lake-Workshop/images/3.firehose/0017-fire.png)

8. In the **Stack** interface, select **Output** and select **KinesisDataGeneratorUrl**

![Fire](/Data-Lake-Workshop/images/3.firehose/0019-fire.png)

9. Enter your password and username

10. In the **Amazon Kinesis Data Generator** interface

- **Record per second** enter 2000

- **Record template** select **template 1**

- Enter the following code

```
{
"order_id": "{{random.uuid}}",
"customer": {{random.arrayElement([
"\"Alice\"", "\"Bob\"", "\"Charlie\"", "\"Diana\"", "\"Eve\"",
"\"Frank\"", "\"Grace\"", "\"Hannah\"", "\"Ivan\"", "\"Jack\"",
"\"Karen\"", "\"Leo\"", "\"Mia\"", "\"Nina\"", "\"Oscar\""
])}},
"amount": {{random.number({ "min": 50, "max": 1000, "precision": 0.01 })}},
"timestamp": "{{date.now("iso")}}"
}
```
11. Then select send data, and stop after sending 100000

![Fire](/Data-Lake-Workshop/images/3.firehose/0020-fire.png)

12. Check in S3 to see if there is data yet

![Fire](/Data-Lake-Workshop/images/3.firehose/0021-fire.png)

**So the data has gone into S3**