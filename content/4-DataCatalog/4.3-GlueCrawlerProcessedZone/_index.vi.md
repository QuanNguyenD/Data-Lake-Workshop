---
title : "Glue Crawler cho Processed Zone "
date :  "2025-06-11"
weight : 3
chapter : false
pre : " <b> 4.3 </b> "
---

### Tạo Glue Crawler cho Processed Zone

1. Truy cập giao diện [AWS Management Console](https://console.aws.amazon.com)

    - Tìm và chọn **AWS Glue**
![Fire](/images/3.firehose/0022-fire.png)

2. Chọn Crawlers → Add Crawler
![Glue](/images/5.glue/0010-glue.png)
3. Phần Name nhập : ```processed-user-log-crawler```, chọn Next
4. Trong Data sources chọn **Add a data sources**
5. Trong phần S3 path chọn đường dẫn S3 và Add an S3 data source.
![Glue](/images/5.glue/0011-glue.png)
6. Chọn **Next**

![Glue](/images/5.glue/0012-glue.png)
7. Chọn IAM role đã có quyền truy cập S3 và Glue  Hoặc bấm "Create new IAM role" nếu cần
![Glue](/images/5.glue/0013-glue.png)
8. Chọn next
9. Phần Target database chọn **processed_db**
![Glue](/images/5.glue/0014-glue.png)
10. Kiểm tra lại cấu hình và chọn Create crawler
![Glue](/images/5.glue/0015-glue.png)
11. Đã tạo thành công 

![Glue](/images/5.glue/0016-glue.png)
12. Chọn Run crawler → tạo table trong catalog
![Glue](/images/5.glue/0017-glue.png)

13. Run crawler thành công

![Glue](/images/5.glue/0018-glue.png)

14. Kiểm tra kết quả Glue Table
- Vào Glue → Tables → chọn database processed_db
- Bạn sẽ thấy thêm 1 Column name là log_date

![Glue](/images/5.glue/0019-glue.png)
