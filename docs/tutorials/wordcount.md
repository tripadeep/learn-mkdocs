# Word Count (PySpark tutorial)

A minimal word count example using RDDs and DataFrames.

## RDD version

```python
rdd = spark.sparkContext.textFile("data/text.txt")
counts = rdd.flatMap(lambda line: line.split()) 
            .map(lambda w: (w,1)) 
            .reduceByKey(lambda a,b: a+b)
counts.collect()
```

## DataFrame version

```python
from pyspark.sql.functions import explode, split, col

text = spark.read.text("data/text.txt")
words = text.select(explode(split(col("value"), "\s+")).alias("word"))
counts = words.groupBy("word").count()
counts.show()
```
