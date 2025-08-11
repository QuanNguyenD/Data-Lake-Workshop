---
title : "Glue Crawler for Raw Zone "
date : "2025-06-11"
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---

### Steps

1. Access the [AWS Management Console](https://console.aws.amazon.com) interface

- Find and select **AWS Glue**
![Fire](/Data-Lake-Workshop/images/3.firehose/0022-fire.png)

2. Select Data Catalog -> Database

![Fire](/Data-Lake-Workshop/images/3.firehose/0023-fire.png)

3. Click **Add database**

4. Enter:

- Database name: raw_db
- (Optional) Description: Glue database for raw logs from user behavior
5. Click **Create**

6. Go to the **Crawlers** tab → Click **Create crawler**

![Fire](/Data-Lake-Workshop/images/3.firehose/0024-fire.png)

7. Enter: **Name**: ```raw-user-log-crawler``` then press **Next**

![Fire](/Data-Lake-Workshop/images/3.firehose/0025-fire.png)

8. Choose data source: Data stores
9. Location:
- Select S3
- Enter: s3://data-lake-raw-user-log/ (or the bucket you created)
- Select Crawl new sub-folders only

![Fire](/Data-Lake-Workshop/images/3.firehose/0026-fire.png)

10. Click Next
![Fire](/Data-Lake-Workshop/images/3.firehose/0027-fire.png)

**IAM Role for crawler**

11. Select IAM role that already has access to S3 and Glue Or press "Create new IAM role" if need

![Fire](/Data-Lake-Workshop/images/3.firehose/0028-fire.png)

12. Click **Next**

![Fire](/Data-Lake-Workshop/images/3.firehose/0029-fire.png)

**Output**

13. Select database: ecommerce_raw_db
14. Click Next → Finish

![Fire](/Data-Lake-Workshop/images/3.firehose/0030-fire.png)

15. Check the configuration again and select Create crawler.

![Fire](/Data-Lake-Workshop/images/3.firehose/0031-fire.png)

16. Crawler created successfully. Then, you select Run crawler.
![Fire](/Data-Lake-Workshop/images/3.firehose/0032-fire.png)

17. Run crawler successfully

![Fire](/Data-Lake-Workshop/images/3.firehose/0033-fire.png)
![Fire](/Data-Lake-Workshop/images/3.firehose/0034-fire.png)

18. Check Glue Table results
- Go to Glue → Tables → select database ecommerce_raw_db
- View the created table
- Check: column names, types
- ormat: JSON
- You can edit the table name if needed

![Fire](/Data-Lake-Workshop/images/3.firehose/0035-fire.png)