---
title : "Chuẩn bị S3"
date :  "2025-06-11"
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

### Chuẩn bị S3 bucket để lưu trừ dữ liệu:

Amazon S3 (Simple Storage Service) là dịch vụ lưu trữ đối tượng phổ biến, thường được sử dụng làm nền tảng lưu trữ cho Data Lake. Việc tạo một bucket S3 giúp bạn lưu trữ dữ liệu thô, bán cấu trúc hoặc không cấu trúc từ nhiều nguồn khác nhau, phục vụ cho phân tích dữ liệu lớn.


Ở trong bài này chúng ta sẽ chia dữ liệu thường được phân chia thành 3 vùng (zone) để quản lý và xử lý hiệu quả:

1. Raw Zone:
    - Lưu trữ dữ liệu gốc, chưa qua xử lý từ các nguồn khác nhau (database, logs, IoT,...).
    - Dữ liệu ở dạng thô, chưa chuẩn hóa hoặc làm sạch.
2. Processed Zone:
    - Lưu trữ dữ liệu đã được xử lý sơ bộ như làm sạch, chuyển đổi định dạng, loại bỏ lỗi.
    - Dữ liệu ở đây đã sẵn sàng cho các bước phân tích tiếp theo.
3. Curated Zone
    - Lưu trữ dữ liệu đã được tổng hợp, chuẩn hóa, sẵn sàng cho phân tích chuyên sâu hoặc phục vụ báo cáo.
    - Dữ liệu ở zone này thường có chất lượng cao, cấu trúc rõ ràng.
### Triển khai thực hiện:

1. Truy cập giao diện [AWS Management Console](https://console.aws.amazon.com)

    - Tìm và chọn **S3**

![S3](/Data-Lake-Workshop/images/4.s3/0001-creates3.png)

2. Trong giao diện **S3** chọn **Create bucket**

![S3](/Data-Lake-Workshop/images/4.s3/0002-creates3.png)

3. Trong giao diện **Create bucket**

    - **Bucket name** điền ``datalake-ecommerce-logs ``
    - Sau đó chọn **Create buckert**

![S3](/Data-Lake-Workshop/images/4.s3/0003-creates3.png)


4. Tạo thành công bucket

![S3](/Data-Lake-Workshop/images/4.s3/0004-creates3.png)

5. Sau khi đã tạo thành công bucket chọn bucket vừa tạo

    - Chọn **Create folder**
    - Nhập Folder name là ``data ``

![S3](/Data-Lake-Workshop/images/4.s3/0006-creates3.png)

6. Tạo folder thành công

![S3](/Data-Lake-Workshop/images/4.s3/0007-creates3.png)

7. Chọn folder **data** và cọn create folder

    - Chọn Create folder
    - Trong giao diện Chọn Create folder, nhập ``raw``
    - Chọn create folder 

![S3](/Data-Lake-Workshop/images/4.s3/0008-creates3.png)

8. Tương tự với việc tạo ``processed`` và ``curated``
9. Tạo thành công 3 folder 

![S3](/Data-Lake-Workshop/images/4.s3/0011-s3.png)

 {{%notice tip%}}
Đó là các bước chuẩn bị , các bước về sau sẽ làm trên IAM User đã tạo 
{{%/notice%}}


  
