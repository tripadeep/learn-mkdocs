# DataFrame API

This page covers common DataFrame operations: read, select, filter, groupBy, joins, and write.

## Reading data

```python
# CSV
df = spark.read.csv("data.csv", header=True, inferSchema=True)

# Parquet
df = spark.read.parquet("path/to/parquet")
```

## Selecting and filtering

```python
from pyspark.sql.functions import col

df2 = df.select("id", "name").filter(col("id") > 10)
df2.show()
```

## Grouping

```python
df.groupBy("category").count().show()
```

## Joins

```python
joined = df.alias("a").join(other.alias("b"), on=["id"], how="inner")
```

## Writing data

```python
df.write.mode("overwrite").parquet("output/path")
```
