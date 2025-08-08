---
title : "Tạo Glue Craler "
date :  "2025-06-11"
weight : 1
chapter : false
pre : " <b> 4. </b> "
---

### Các bước thực hiện 

1. Truy cập giao diện [AWS Management Console](https://console.aws.amazon.com)

    - Tìm và chọn **AWS Glue**
![Fire](/images/3.firehose/0022-fire.png)
2. Chọn Data Catalog -> Database 

![Fire](/images/3.firehose/0023-fire.png)

3. Bấm **Add database**

4. Nhập: 
    - Database name: raw_db
    - (Optional) Description: Glue database for raw logs from user behavior
5. Nhấn **Create**

6. Vào tab **Crawlers** → Bấm **Create crawler**

![Fire](/images/3.firehose/0024-fire.png)

7. Nhập: **Name**: ```raw-user-log-crawler``` rồi ấn **Next**

![Fire](/images/3.firehose/0025-fire.png)

8. Choose data source: Data stores
9. Location:
    - Chọn S3
    - Nhập: s3://data-lake-raw-user-log/ (hoặc bucket bạn đã tạo)
    - Chọn Crawl new sub-folders only

![Fire](/images/3.firehose/0026-fire.png)

10. Bấm Next
![Fire](/images/3.firehose/0027-fire.png)

**IAM Role cho crawler**

11. Chọn IAM role đã có quyền truy cập S3 và Glue  Hoặc bấm "Create new IAM role" nếu cần

![Fire](/images/3.firehose/0028-fire.png)

12. Bấm **Next**


![Fire](/images/3.firehose/0029-fire.png)

**Output (Đầu ra)**

13. Chọn database: ecommerce_raw_db
14. Bấm Next → Finish

![Fire](/images/3.firehose/0030-fire.png)

15. Kiểm tra lại cấu hình và chọn Create crawler.

![Fire](/images/3.firehose/0031-fire.png)

16. Tạo Crawler thành công. Sau đó, bạn chọn Run crawler.
![Fire](/images/3.firehose/0032-fire.png)

17. Run crawler thành công 

![Fire](/images/3.firehose/0033-fire.png)
![Fire](/images/3.firehose/0034-fire.png)


18. Kiểm tra kết quả Glue Table
    - Vào Glue → Tables → chọn database ecommerce_raw_db
    - Xem bảng đã được tạo
    - Kiểm tra: column names, types
    - ormat: JSON
    - Bạn có thể sửa tên table nếu cần

![Fire](/images/3.firehose/0035-fire.png)

