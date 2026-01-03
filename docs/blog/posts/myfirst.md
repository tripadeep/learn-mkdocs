---
date:
  created: 2026-01-04
readtime: 5
categories:
  - Introduction
tags:
  - pyspark
  - getting-started
authors:
  - team
slug: intro-pyspark
---

# Introduction to PySpark

PySpark is the Python API for Apache Spark — a unified analytics engine for large-scale data processing. This post explains what PySpark is, when to use it, and how to start a local Spark session.

<!-- more -->

## Quick example

```python
from pyspark.sql import SparkSession

spark = SparkSession.builder 
    .appName("pyspark-intro") 
    .master("local[*]") 
    .getOrCreate()

print(spark.version)

spark.stop()
```

For hands-on examples, see the Tutorials section of this site.