---
title : "Analyze with Athena "
date : "2025-06-11"
weight : 5
chapter : false
pre : " <b> 5. </b> "
---

### Analyze with Athena

1. Access the [AWS Management Console](https://console.aws.amazon.com) interface
2. Access **Athena**
3. In the Athena interface:

- In the Data Source section, select AwsDataCatalog

- In the Database section, select curated_db

- Execute the following query

``` SELECT * FROM "curated_db"."user_logs" limit 10; ```

![Glue](/Data-Lake-Workshop/images/5.glue/0036-glue.png)

- Click Run Query

- Wait until the status changes to Complete

- View the results of the query

![Glue](/Data-Lake-Workshop/images/5.glue/0037-glue.png)

4. Execute another query
```
SELECT customer,count(amount_value)
FROM "curated_db"."user_logs"
GROUP BY customer
ORDER BY customer
limit 10;
```

![Glue](/Data-Lake-Workshop/images/5.glue/0038-glue.png)