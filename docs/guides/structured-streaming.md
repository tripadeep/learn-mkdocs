# Structured Streaming

Structured Streaming is Spark's high-level streaming API. It provides a table-like interface over streaming data.

```python
from pyspark.sql.functions import expr

stream = spark.readStream.format("socket").option("host","localhost").option("port",9999).load()
counts = stream.groupBy("value").count()
query = counts.writeStream.outputMode("complete").format("console").start()
query.awaitTermination()
```
