---
title : "Phân tích với Athena "
date :  "2025-06-11"
weight : 5
chapter : false
pre : " <b> 5. </b> "
---

### Phân tích với Athena

1. Truy cập giao diện [AWS Management Console](https://console.aws.amazon.com)
2. Truy cập **Athena**
3. Trong giao diện Athena:
    - Tại mục Data Source, chọn AwsDataCatalog
    - Tại mục Database, chọn curated_db
    - Thực hiện câu truy vấn sau 

``` SELECT * FROM "curated_db"."user_logs" limit 10; ```

![Glue](/images/5.glue/0036-glue.png)

- Nhấn Run Query

- Chờ đến khi trạng thái chuyển thành Complete

- Xem kết quả của câu truy vấn

![Glue](/images/5.glue/0037-glue.png)

4. Thực hiện câu truy vấn khác 
```
SELECT customer,count(amount_value) 
FROM "curated_db"."user_logs" 
GROUP BY customer 
ORDER BY customer 
limit 10;
```

![Glue](/images/5.glue/0038-glue.png)



