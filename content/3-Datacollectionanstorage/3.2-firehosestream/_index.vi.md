---
title : "Tạo Firehose Stream"
date :  "2025-06-11"
weight : 2
chapter : false
pre : " <b> 3.2 </b> "
---

### Tạo Firehose Stream

1. Chuẩn bị

    - Gắn thêm các quyền sau vào IAM User ```AmazonKinesisFullAccess```, ```AmazonKinesisFirehoseFullAccess```, ```IAMFullAccess```.

![Fire](/images/3.firehose/0001-fire.png)

2. Truy cập ```Kinesis```

![Fire](/images/3.firehose/0002-fire.png)

3. Vào AmaZone Data Firehose

![Fire](/images/3.firehose/0003-fire.png)

4. Trong Firehose streams chọn **Create Firehose stream**

![Fire](/images/3.firehose/0004-fire.png)

5. Trong **Create Firehose stream**

    - Trong **Sourse** chọn **Direct PUT**
    - Trong **Destination** chọn **Amazon S3**
    - Trong **Firehose stream name** điền ```PUT-S3-UserLogsToS3```

![Fire](/images/3.firehose/0006-fire.png)

6. Trong **Destination settings**

    - Chọn S3 bucket đã tạo trước đó 
    - S3 bucket prefix nhập ```data/raw/user-logs/```
    - S3 bucket error output prefix nhập ```data/error/user-logs/```

![Fire](/images/3.firehose/0008-fire.png)

7. Trong phần **Buffer hins, compression, file extention and encryption**

    - Buffer size nhập ```1```.
    - Buffer interval nhập ```60```.

![Fire](/images/3.firehose/0009-fire.png)

8. Trong bước **Advanced settings**

    - **Service access** chọn **Create or update IAM role**
    - Sau đó chọn **Create delivery stream**
![Fire](/images/3.firehose/0005-fire.png)


 {{%notice tip%}}
Nếu trong bước trên bị lỗi IAM role khi ấn **Create delivery stream** bạn chỉ cần ấn lại thêm một lần nữa là được :))
{{%/notice%}}

9. Tạo thành công Firehose streams

![Fire](/images/3.firehose/0010-fire.png)
