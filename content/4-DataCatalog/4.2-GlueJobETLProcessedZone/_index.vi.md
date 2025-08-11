---
title : "Tạo Glue Job ETL → Processed Zone "
date :  "2025-06-11"
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---

### Các bước thực hiện 

1. Truy cập giao diện [AWS Management Console](https://console.aws.amazon.com)

    - Tìm và chọn **AWS Glue**
![Fire](/Data-Lake-Workshop/images/3.firehose/0022-fire.png)
2. Chọn Data Catalog -> Database 

![Glue](/Data-Lake-Workshop/images/5.glue/0001-glue.png)
3. Chọn Add database

![Glue](/Data-Lake-Workshop/images/5.glue/0002-glue.png)

4. Nhập tên Tên: ```processed_db```

![Glue](/Data-Lake-Workshop/images/5.glue/0003-glue.png)

![Glue](/Data-Lake-Workshop/images/5.glue/0004-glue.png)

5. Tạo Glue Job (ETL Raw → Processed)
    Chuẩn bị
   - 	Bạn cần đã tạo:
   - 	IAM Role có quyền truy cập S3, Glue, Lake Formation (ví dụ: AWSGlueServiceRole-DataLake)
   - 	Glue Database raw_db (đã có từ bước trước)
   - 	Crawler đã chạy cho Raw Zone → có table JSON
   - 	Bucket S3 Processed Zone
### Tạo Glue Job (ETL Raw → Processed)

6. AWS Console → AWS Glue →  ETL Jobs → “script editor”.

![Glue](/Data-Lake-Workshop/images/5.glue/0005-glue.png)

7. Tại **Engine** chọn **Spark**
8. Options chọn Upload script 
9. Tiến hành tải file script [tại đây](https://raw.githubusercontent.com/QuanNguyenD/FcjWS/refs/heads/main/import_sys.py) sau đó upload và nhấn Create Script

![Glue](/Data-Lake-Workshop/images/5.glue/0006-glue.png)

10. Tại phần tiếp theo chọn **Jobs details**
11. Name ```etl_raw_to_processed```
12. IAM role chọn role Glue có quyền với S3/Lake Formation.

![Glue](/Data-Lake-Workshop/images/5.glue/0007-glue.png)

13. Tạo tành công 

![Glue](/Data-Lake-Workshop/images/5.glue/0008-glue.png)

14. Bấm Run, Sau khi chạy xong vào S3 để kiểm tra 

![Glue](/Data-Lake-Workshop/images/5.glue/0009-glue.png)


