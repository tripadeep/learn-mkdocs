# Configuration

Common Spark configuration options and how to set them with SparkConf or SparkSession builder.

```python
from pyspark import SparkConf
from pyspark.sql import SparkSession

conf = SparkConf().set("spark.app.name", "app").set("spark.executor.memory", "2g")
spark = SparkSession.builder.config(conf=conf).getOrCreate()
```

## Common configs
- `spark.executor.memory` — memory per executor
- `spark.executor.cores` — cores per executor
- `spark.sql.shuffle.partitions` — default shuffle partitions
