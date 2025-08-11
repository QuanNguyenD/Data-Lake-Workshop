---
title : "Glue Crawler for Curated Zone "
date :  "2025-06-11"
weight : 5
chapter : false
pre : " <b> 4.5 </b> "
---

### Create Glue Crawler for Curated Zone

1. Access the [AWS Management Console](https://console.aws.amazon.com) interface

- Find and select **AWS Glue**
![Fire](/Data-Lake-Workshop/images/3.firehose/0022-fire.png)

2. Select Crawlers → Add Crawler

![Glue](/Data-Lake-Workshop/images/5.glue/0028-glue.png)

3. In the S3 section, select: ```s3://your-curated-bucket/curated/user_logs/```, then select Add an S3 data source

![Glue](/Data-Lake-Workshop/images/5.glue/0029-glue.png)

4. Select **Next**

5. Select the IAM role that has access access S3 and Glue Or click "Create new IAM role" if needed then select **Next**

![Glue](/Data-Lake-Workshop/images/5.glue/0030-glue.png)

6. In Target database section select **curated_db** then select **Next**

![Glue](/Data-Lake-Workshop/images/5.glue/0031-glue.png)

7. Check configuration again and select Create crawler

![Glue](/Data-Lake-Workshop/images/5.glue/0032-glue.png)

8. Created successfully

![Glue](/Data-Lake-Workshop/images/5.glue/0033-glue.png)

12. Select Run crawler

![Glue](/Data-Lake-Workshop/images/5.glue/0034-glue.png)

13. After successful run check Glue Table result

![Glue](/Data-Lake-Workshop/images/5.glue/0035-glue.png)