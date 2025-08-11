---
title : "Create Glue Job: ETL from Processed →Curated "
date : "2025-06-11"
weight : 4
chapter : false
pre : " <b> 4.4 </b> "
---

### Steps

1. Access the [AWS Management Console](https://console.aws.amazon.com) interface

- Find and select **AWS Glue**
![Fire](/Data-Lake-Workshop/images/3.firehose/0022-fire.png)

2. Select Data Catalog -> Database
![Glue](/Data-Lake-Workshop/images/5.glue/0020-glue.png)
3. Select Add database
- Enter **name**: ```curated_db```
- Click Create database
![Glue](/Data-Lake-Workshop/images/5.glue/0021-glue.png)

4. Created successfully
![Glue](/Data-Lake-Workshop/images/5.glue/0022-glue.png)

### Create Glue Job: ETL from Processed → Curated

6. AWS Console → AWS Glue → ETL Jobs → “script editor”.

7. Options select Upload script

8. Proceed to download the script file [here](https://raw.githubusercontent.com/QuanNguyenD/FcjWS/refs/heads/main/import_sys_cru.py) then upload and click Create Script

![Glue](/Data-Lake-Workshop/images/5.glue/0023-glue.png)
10. In the next section, select **Jobs details**
- Job name: etl_processed_to_curated
- IAM Role: AWSGlueServiceRole-submit-crawler
- Type: Spark
![Glue](/Data-Lake-Workshop/images/5.glue/0024-glue.png)
11. Created successfully

![Glue](/Data-Lake-Workshop/images/5.glue/0025-glue.png)

12. Click Run

![Glue](/Data-Lake-Workshop/images/5.glue/0026-glue.png)
13. After running successfully, go to S3 to check

![Glue](/Data-Lake-Workshop/images/5.glue/0027-glue.png)