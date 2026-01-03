# Deployment

Best practices for packaging and submitting PySpark jobs.

## Submit with spark-submit

```bash
spark-submit --master yarn --deploy-mode cluster \
  --conf spark.executor.memory=4g \
  --py-files dependencies.zip \
  app.py
```

## Packaging
- Use `spark-submit` with `--py-files` or build an egg/wheel.
- Ensure dependencies are available on the cluster or packaged with the job.
