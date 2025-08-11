---
title : "Glue Crawler for Processed Zone "
date :  "2025-06-11"
weight : 3
chapter : false
pre : " <b> 4.3 </b> "
---

### Create Glue Crawler for Processed Zone

1. Access the [AWS Management Console](https://console.aws.amazon.com) interface

- Find and select **AWS Glue**
![Fire](/Data-Lake-Workshop/images/3.firehose/0022-fire.png)

2. Select Crawlers → Add Crawler
![Glue](/Data-Lake-Workshop/images/5.glue/0010-glue.png)
3. In the Name section, enter: ```processed-user-log-crawler```, select Next
4. In the Data sources section, select **Add a data sources**
5. In the S3 path section, select the S3 path and Add an S3 data source.
![Glue](/Data-Lake-Workshop/images/5.glue/0011-glue.png)
6. Select **Next**

![Glue](/Data-Lake-Workshop/images/5.glue/0012-glue.png)
7. Select the IAM role that already has access to S3 and Glue Or click "Create new IAM role" if needed
![Glue](/Data-Lake-Workshop/images/5.glue/0013-glue.png)
8. Select next
9. For Target database, select **processed_db**
![Glue](/Data-Lake-Workshop/images/5.glue/0014-glue.png)
10. Check the configuration again and select Create crawler
![Glue](/Data-Lake-Workshop/images/5.glue/0015-glue.png)
11. Successfully created

![Glue](/Data-Lake-Workshop/images/5.glue/0016-glue.png)
12. Select Run crawler → create table in catalog
![Glue](/Data-Lake-Workshop/images/5.glue/0017-glue.png)

13. Run crawler successfully

![Glue](/Data-Lake-Workshop/images/5.glue/0018-glue.png)

14. Check Glue Table result
- Go to Glue → Tables → select database processed_db
- You will see 1 more Column name is log_date

![Glue](/Data-Lake-Workshop/images/5.glue/0019-glue.png)