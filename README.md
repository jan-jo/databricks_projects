# Transportation Data Pipeline — Databricks Lakeflow Project

> **Note:** I built this project while following a Databricks tutorial by Codebasics to learn **Lakeflow Spark Declarative Pipelines**. This is a hands-on learning project — not original work. 

---

## What Is This Project?

This is my first end-to-end **data pipeline project on Databricks**. It covers the full journey of data — from raw files all the way to clean, business-ready tables — using the **transportation domain** as a real-world use case.

I followed this tutorial to learn:
- How Databricks works in practice
- What the **Bronze → Silver → Gold** layered architecture looks like
- How to build pipelines using **Lakeflow Spark Declarative Pipelines**
- How to load data incrementally (so only new data gets processed each time)

---

## What I Learned

| Concept | What It Means  |
|---|---|
| **Declarative Pipelines** | You tell Databricks *what* you want, not *how* to do it — it figures out the steps |
| **Bronze Layer** | Raw data as-is, straight from the source — no changes |
| **Silver Layer** | Cleaned and transformed data — ready for analysis |
| **Gold Layer** | Final, BI-ready tables — what dashboards and reports use |
| **Incremental Load** | Only process new/changed data instead of reprocessing everything |
| **Access Management** | Controlling who can see or edit which data |

---

## Project Architecture

```
Raw Data (S3 Bucket)
        |
        v
  Bronze Layer      <- Raw ingestion (City, Trips tables)
        |
        v
  Silver Layer      <- Cleaned & transformed (City, Calendar, Trips)
        |
        v
  Gold Layer        <- BI-ready, aggregated data for reporting
```


---

## Tools & Technologies Used

- **Databricks Free Edition** — cloud platform for running the pipeline
- **Lakeflow Spark Declarative Pipelines** — the core pipeline framework
- **AWS S3** — storage for raw data files
- **Delta Lake** — table format used across all layers
- **SQL / PySpark** — for transformations

---


## How I Built It — Step by Step

1. **Set up Databricks Free Edition** and created a Catalog and Schemas
2. **Connected an AWS S3 bucket** as the data source
3. **Built the Bronze layer** — ingested raw City and Trips tables as-is
4. **Built the Silver layer** — cleaned data, added a Calendar table, fixed data types
5. **Built the Gold layer** — created final aggregated tables ready for BI tools
6. **Set up Incremental Loading** — so only new data runs through the pipeline
7. **Configured Access Management** — learned how to control data permissions

---

## My Takeaways

Before this project, I had never used Databricks. Here's what changed:

- I now understand **why the medallion architecture (Bronze/Silver/Gold)** exists — it keeps data clean and traceable
- Declarative pipelines feel very different from writing step-by-step code — less code, more clarity
- Setting up **S3 + Databricks** together was tricky at first but makes total sense now
- Incremental loading is something I'll definitely use in future real projects

---

## Certification

After completing this project, I earned the **Databricks Lakeflow Spark Declarative Pipelines** certification.

> Credential ID: `179086983` — issued by Databricks via Codebasics

---

*Made with curiosity and a lot of trial and error.*
