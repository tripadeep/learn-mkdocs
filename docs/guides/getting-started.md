# Getting Started with PySpark

This guide shows how to install PySpark, create a SparkSession, and run simple examples locally.

## Prerequisites
- Python 3.8+ (recommended)
- Java JDK 8/11 installed
- pip

## Install PySpark

```bash
python -m pip install pyspark
```

## Create a SparkSession

```python
from pyspark.sql import SparkSession

spark = SparkSession.builder 
    .appName("local-example") 
    .master("local[*]") 
    .getOrCreate()

# show version
print(spark.version)
```

## Create a DataFrame

```python
data = [(1, "Alice"), (2, "Bob")]
columns = ["id", "name"]
df = spark.createDataFrame(data, columns)
df.show()
```

## Stop the session

```python
spark.stop()
```
