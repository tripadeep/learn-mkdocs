# SQL & SparkSession

SparkSession is the entry point for DataFrame and SQL functionality.

```python
spark.sql("SELECT 1").show()
```

## Registering temporary views

```python
df.createOrReplaceTempView("my_view")
res = spark.sql("SELECT * FROM my_view WHERE id > 10")
res.show()
```
