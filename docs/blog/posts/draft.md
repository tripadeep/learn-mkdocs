---
date:
  created: 2026-01-04
draft: true
categories:
  - Tips
tags:
  - pyspark
  - tips
authors:
  - team
---

# PySpark Tips: Efficient Filtering

Quick tip: prefer `filter` on DataFrames with column expressions rather than Python functions for better performance because Spark can optimize the filter operation.

```python
from pyspark.sql.functions import col

df_filtered = df.filter(col("value") > 100)
```

This is a draft post — polish and publish when ready.