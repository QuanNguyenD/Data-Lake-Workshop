---
title : "Đưa dữ liệu vào S3 bucket "
date :  "2025-06-11"
weight : 1
chapter : false
pre : " <b> 3.1 </b> "
---

**Trong bước này chúng ta sẽ**

1. Truy cập giao diện [AWS Management Console](https://console.aws.amazon.com)

    - Tìm và chọn **S3**
2. Truy cập vào S3 bucket đã tạo trước đó sau đó mở folder raw
3. Tạo 1 thư mục mới là ``user-logs`` trong ``raw``

![S3](/Data-Lake-Workshop/images/4.s3/0012-s3.png)

4. Chúng ta sẽ tải file [order.json](https://raw.githubusercontent.com/QuanNguyenD/FcjWS/refs/heads/main/orders.json)

5. Chúng ta tiến hành Upload dữ liệu:

    - Chọn upload

![S3](/Data-Lake-Workshop/images/4.s3/0013-s3.png)

6. Trong giao diện upload 

    - Chọn Add file 
    - Chọn order.json
    - Chọn upload

![S3](/Data-Lake-Workshop/images/4.s3/0015-s3.png)

7. Sau khi đã upload thành công

![S3](/Data-Lake-Workshop/images/4.s3/0014-s3.png)