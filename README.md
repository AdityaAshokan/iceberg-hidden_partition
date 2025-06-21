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


