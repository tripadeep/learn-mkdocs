# ETL Pipeline (PySpark tutorial)

This tutorial demonstrates a simple ETL pipeline: read CSV, transform, and write Parquet.

```python
from pyspark.sql.functions import col, to_date

df = spark.read.csv("data/input.csv", header=True, inferSchema=True)
df2 = df.withColumn("date", to_date(col("date_str"), "yyyy-MM-dd"))
df2.filter(col("amount") > 0).write.mode("overwrite").parquet("data/output")
```
