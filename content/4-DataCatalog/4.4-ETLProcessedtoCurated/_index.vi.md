---
title : "Tạo Glue Job: ETL từ Processed →Curated "
date :  "2025-06-11"
weight : 4
chapter : false
pre : " <b> 4.4 </b> "
---
### Các bước thực hiện 

1. Truy cập giao diện [AWS Management Console](https://console.aws.amazon.com)

    - Tìm và chọn **AWS Glue**
![Fire](/images/3.firehose/0022-fire.png)
2. Chọn Data Catalog -> Database 
![Glue](/images/5.glue/0020-glue.png)
3. Chọn Add database
- Nhập **name**: ```curated_db```
- Nhấn Create database
![Glue](/images/5.glue/0021-glue.png)

4. Tạo thành công
![Glue](/images/5.glue/0022-glue.png)

### Tạo Glue Job: ETL từ Processed → Curated

6. AWS Console → AWS Glue →  ETL Jobs → “script editor”.
7. Options chọn Upload script 
8. Tiến hành tải file script [tại đây](https://raw.githubusercontent.com/QuanNguyenD/FcjWS/refs/heads/main/import_sys_cru.py) sau đó upload và nhấn Create Script

![Glue](/images/5.glue/0023-glue.png)
10. Tại phần tiếp theo chọn **Jobs details**
- Job name:	etl_processed_to_curated
- IAM Role    : AWSGlueServiceRole-submit-crawler
- Type:	Spark
![Glue](/images/5.glue/0024-glue.png)
11. Tạo thành công 

![Glue](/images/5.glue/0025-glue.png)

12. Bấm Run

![Glue](/images/5.glue/0026-glue.png)
13. Sau khi chạy thành công vào S3 kiểm tra 

![Glue](/images/5.glue/0027-glue.png)

