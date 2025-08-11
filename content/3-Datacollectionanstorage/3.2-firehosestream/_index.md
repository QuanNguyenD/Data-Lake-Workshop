---
title : "Create Firehose Stream"
date :  "2025-06-11"
weight : 2
chapter : false
pre : " <b> 3.2 </b> "
---

1. Preparation

- Add the following permissions to IAM User ```AmazonKinesisFullAccess```, ```AmazonKinesisFirehoseFullAccess```, ```IAMFullAccess```.

![Fire](/Data-Lake-Workshop/images/3.firehose/0001-fire.png)

2. Go to ```Kinesis```

![Fire](/Data-Lake-Workshop/images/3.firehose/0002-fire.png)

3. Go to AmaZone Data Firehose

![Fire](/Data-Lake-Workshop/images/3.firehose/0003-fire.png)

4. In Firehose streams select **Create Firehose stream**

![Fire](/Data-Lake-Workshop/images/3.firehose/0004-fire.png)

5. In **Create Firehose stream** 

- In **Sourse** select **Direct PUT** 
- In **Destination** select **Amazon S3** 
- In **Firehose stream name** fill in ```PUT-S3-UserLogsToS3```

![Fire](/Data-Lake-Workshop/images/3.firehose/0006-fire.png)

6. In **Destination settings** 

- Select the S3 bucket created earlier 
- S3 bucket prefix enter ```data/raw/user-logs/``` 
- S3 bucket error output prefix enter ```data/error/user-logs/```

![Fire](/Data-Lake-Workshop/images/3.firehose/0008-fire.png)

7. In the **Buffer hins, compression, file extention and encryption** section 

- Buffer size enter ```1```. 
- Buffer interval enter ```60```.

![Fire](/Data-Lake-Workshop/images/3.firehose/0009-fire.png)

8. In the **Advanced settings** step

- **Service access** select **Create or update IAM role**
- Then select **Create delivery stream**
![Fire](/Data-Lake-Workshop/images/3.firehose/0005-fire.png)

{{%notice tip%}}
If in the above step there is an IAM role error when pressing **Create delivery stream**, you just need to press it again :))
{{%/notice%}}

9. Successfully created Firehose streams

![Fire](/Data-Lake-Workshop/images/3.firehose/0010-fire.png)