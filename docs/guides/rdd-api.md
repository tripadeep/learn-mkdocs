# RDD API

Use RDDs for fine-grained control and when you need custom partitioning or lower-level APIs.

```python
rdd = spark.sparkContext.parallelize([1,2,3,4])
mapped = rdd.map(lambda x: x * 2)
print(mapped.collect())
```
