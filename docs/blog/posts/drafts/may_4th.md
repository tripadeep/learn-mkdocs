---
date:
  created: 2026-01-04
draft: true
categories:
  - Tutorials
tags:
  - pyspark
  - partitioning
authors:
  - team
---

# Draft: Partitioning Strategies in PySpark

Notes on partitioning for performance and shuffles. Topics to finish: examples for `repartition`, `coalesce`, and partitioning by column on write.

- When to repartition before a shuffle
- When to use `coalesce` to reduce partitions
- Partitioning writes by columns for faster reads

<!-- more -->

(Work in progress.)