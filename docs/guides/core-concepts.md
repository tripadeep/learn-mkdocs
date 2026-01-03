# Core Concepts

This page explains PySpark concepts: RDDs, DataFrames, SparkSession, transformations vs actions, and partitioning.

## RDD vs DataFrame
- RDD: low-level resilient distributed dataset.
- DataFrame: higher-level table-like API with optimizations via Catalyst.

## Transformations and Actions
- Transformations are lazy (e.g., map, filter, select).
- Actions trigger execution (e.g., show, collect, write).

## Partitioning
- Data is divided into partitions for parallelism.
- Repartition and coalesce can change partition counts.

## Lazy evaluation and optimization
- Spark builds a logical plan and optimizes it before execution.
