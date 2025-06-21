# Iceberg Hidden Partitioning (Scala + Spark)

This project demonstrates how **Apache Iceberg hidden partitioning** works using **Apache Spark 3.4.x** and **Scala**.

---

## What Is Hidden Partitioning?

In Iceberg, you can partition data using **transformed values** (like `days(event_time)`), but the partition column is **not exposed** in the table schema.

You benefit from:
- Partition pruning
- Cleaner schemas
- Efficient query performance

---

## Requirements

- Java 8+
- Apache Spark 3.4.x
- Scala 2.12.x
- Iceberg runtime JAR (Spark 3.4 version):

## How to Run

### Use spark shell (Quick Demo)

Step 1: Launch Spark Shell with Iceberg

```bash
spark-shell \
  --packages org.apache.iceberg:iceberg-spark-runtime-3.4_2.12:1.4.2 \
  --conf spark.sql.catalog.local=org.apache.iceberg.spark.SparkCatalog \
  --conf spark.sql.catalog.local.type=hadoop \
  --conf spark.sql.catalog.local.warehouse=warehouse \
  --conf spark.sql.extensions=org.apache.iceberg.spark.extensions.IcebergSparkSessionExtensions

Step 2: Paste the hidden_partition.txt file code into the shell

