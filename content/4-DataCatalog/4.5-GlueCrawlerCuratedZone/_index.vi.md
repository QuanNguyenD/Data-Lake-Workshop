---
title : "Glue Crawler cho Curated Zone "
date :  "2025-06-11"
weight : 5
chapter : false
pre : " <b> 4.5 </b> "
---


### Tạo Glue Crawler cho Curated Zone

1. Truy cập giao diện [AWS Management Console](https://console.aws.amazon.com)

    - Tìm và chọn **AWS Glue**
![Fire](/Data-Lake-Workshop/images/3.firehose/0022-fire.png)

2. Chọn Crawlers → Add Crawler

![Glue](/Data-Lake-Workshop/images/5.glue/0028-glue.png)

3. Phần S3 chọn : ```s3://your-curated-bucket/curated/user_logs/```, sau đó chọn Add an S3 data source

![Glue](/Data-Lake-Workshop/images/5.glue/0029-glue.png)

4. Chọn **Next**

5. Chọn IAM role đã có quyền truy cập S3 và Glue  Hoặc bấm "Create new IAM role" nếu cần sau dó chọn **Next**

![Glue](/Data-Lake-Workshop/images/5.glue/0030-glue.png)

6. Phần Target database chọn **curated_db** sau đó chon **Next**

![Glue](/Data-Lake-Workshop/images/5.glue/0031-glue.png)

7. Kiểm tra lại cấu hình và chọn Create crawler

![Glue](/Data-Lake-Workshop/images/5.glue/0032-glue.png)

8. Tạo thành công 

![Glue](/Data-Lake-Workshop/images/5.glue/0033-glue.png)

12. Chọn Run crawler

![Glue](/Data-Lake-Workshop/images/5.glue/0034-glue.png)

13. Sau khi chạy thành công kiểm tra kết quả Glue Table

![Glue](/Data-Lake-Workshop/images/5.glue/0035-glue.png)
