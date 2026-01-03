---
date:
  created: 2026-01-04
draft: true
categories:
  - Tips
tags:
  - pyspark
  - nulls
authors:
  - team
---

# Draft: Handling Nulls and Defaults

Draft notes on handling nulls in DataFrames, using `na.fill`, `na.drop`, and safe SQL expressions.

Examples to add:

```python
df.na.fill({"col1": 0, "col2": "unknown"})
```

(Work in progress.)