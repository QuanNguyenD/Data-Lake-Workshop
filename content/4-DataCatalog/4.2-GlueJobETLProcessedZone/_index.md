---
title : "Create Glue Job ETL → Processed Zone "
date :  "2025-06-11"
weight : 2
chapter : false
pre : " <b> 4. </b> "
---

### Steps

1. Access the [AWS Management Console](https://console.aws.amazon.com) interface

- Find and select **AWS Glue**
![Fire](/Data-Lake-Workshop/images/3.firehose/0022-fire.png)
2. Select Data Catalog -> Database

![Glue](/Data-Lake-Workshop/images/5.glue/0001-glue.png)
3. Select Add database

![Glue](/Data-Lake-Workshop/images/5.glue/0002-glue.png)

4. Enter the name Name: ```processed_db```

![Glue](/Data-Lake-Workshop/images/5.glue/0003-glue.png)

![Glue](/Data-Lake-Workshop/images/5.glue/0004-glue.png)

5. Create Glue Job (ETL Raw → Processed)

Preparation
- You need to have created:

- IAM Role with access to S3, Glue, Lake Formation (eg: AWSGlueServiceRole-DataLake)

- Glue Database raw_db (already from the previous step)

- Crawler running for Raw Zone → has JSON table

- Bucket S3 Processed Zone
### Create Glue Job (ETL Raw → Processed)

6. AWS Console → AWS Glue → ETL Jobs → “script editor”.

![Glue](/Data-Lake-Workshop/images/5.glue/0005-glue.png)

7. At **Engine** select **Spark**
8. Options select Upload script
9. Proceed to download the script file [here](https://raw.githubusercontent.com/QuanNguyenD/FcjWS/refs/heads/main/import_sys.py) then upload and click Create Script

![Glue](/Data-Lake-Workshop/images/5.glue/0006-glue.png)

10. In the next section select **Jobs details**
11. Name ```etl_raw_to_processed```
12. IAM role select Glue role with permissions to S3/Lake Formation.

![Glue](/Data-Lake-Workshop/images/5.glue/0007-glue.png)

13. Created successfully

![Glue](/Data-Lake-Workshop/images/5.glue/0008-glue.png)

14. Click Run, After running, go to S3 to check

![Glue](/Data-Lake-Workshop/images/5.glue/0009-glue.png)