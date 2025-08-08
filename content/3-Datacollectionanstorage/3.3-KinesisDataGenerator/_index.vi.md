---
title : "Cấu hình Amazon Cognito cho Kinesis Data Generator"
date :  "2025-06-11"
weight : 3
chapter : false
pre : " <b> 3.3 </b> "
---

### Các bước thực hiện

**Trước tiên hãy thêm IAM role cho Iam users** 

![Fire](/images/3.firehose/0011-fire.png)

1. Truy cập AWS Management Console.
    - Tìm CloudFormation.
    - Chọn CloudFormation

![Fire](/images/3.firehose/0012-fire.png)

2. Trong giao diện CloudFormation chọn **Create stack**

![Fire](/images/3.firehose/0013-fire.png)

3. Tiến hành tải file [setup](https://raw.githubusercontent.com/QuanNguyenD/FcjWS/refs/heads/main/cognito-setup.json)

4. Trong giao diện **Create stack**:
    - **Choose an existing template**
    - Trong phần **Specify template** chọn **Upload a template file**
    - Trong phần **Choose file** chọn file đa tải về trước đó 
    - Ấn **Next**
5. Trong giao diện **Specify stack details**
    - Stack name nhập ```Kinesis-Data-Generator-Cognito-User```
    - User name nhập ```admin```
    - Password nhâp mật khẩu của bạn
    - Chọn **Next**
![Fire](/images/3.firehose/0014-fire.png)

6. Tiếp tuc chọn **Next** và **Submit**

![Fire](/images/3.firehose/0016-fire.png)
![Fire](/images/3.firehose/0015-fire.png)

7. Tạo thành công

![Fire](/images/3.firehose/0017-fire.png)

8. Trong giao diện **Stack** chọn **Output** và chọn **KinesisDataGeneratorUrl**

![Fire](/images/3.firehose/0019-fire.png)

9. Tiến hành nhập mật khẩu và tên đăng nhập

10. Trong giao diện **Amazon Kinesis Data Generator**

    - **Record per second** nhập 2000

    - **Record template** chọn **template 1**
    - Nhập đoạn mã sau 
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
11. Sau đó chon send data, và sau khi send dc 100000 thì dừng

![Fire](/images/3.firehose/0020-fire.png)

12. Kiểm tra lại trong S3 xem đã có dữ liệu chưa 

![Fire](/images/3.firehose/0021-fire.png)

**Như vây dữ liệu đa đi vào S3**

