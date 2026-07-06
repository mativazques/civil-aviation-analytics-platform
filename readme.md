# Civil Aviation & Car Rental Analytics Platform

End-to-end data engineering capstone: two batch pipelines that ingest raw operational
data, process it with Spark, land it in a Hive data warehouse, and answer business
questions — one of them surfaced through a Power BI dashboard — plus a GCP cloud
architecture design.

## Stack
Apache Airflow · PySpark · Apache Hive · HDFS · Bash ingestion · Power BI · GCP (BigQuery, Dataprep, Dataflow/Beam)

## 1. Argentine civil aviation — landings & takeoffs
Argentina's National Civil Aviation Administration needs reporting on national air
traffic (most-flown aircraft, passenger volumes, origin/destination routes by date
range) to brief the Ministry of Transport.

Pipeline: bash ingestion → PySpark transformations → Hive DW, orchestrated with a
parent/child Airflow DAG, with business queries on top.

![Airflow DAG](docs/ejercicio-1/img/3_dag.png)

- Pipeline & solution: [docs/ejercicio-1/aviacion.md](docs/ejercicio-1/aviacion.md)
- Business queries: [docs/ejercicio-1/queries/queries-1.md](docs/ejercicio-1/queries/queries-1.md)

## 2. Car rental analytics + dashboard
A leading car-rental company needs data-driven reporting: total rentals and
segmentation by fuel type, location, brand/model, and rating.

Pipeline: ingest → Spark processing → Hive, orchestrated with Airflow, results
delivered in a Power BI dashboard.

![Power BI dashboard](docs/ejercicio-2/img/pbi.png)

- Pipeline & solution: [docs/ejercicio-2/car_rental_data.md](docs/ejercicio-2/car_rental_data.md)
- Dashboard file: [docs/ejercicio-2/Alquiler_de_automoviles.pbix](docs/ejercicio-2/Alquiler_de_automoviles.pbix)

## 3. GCP cloud architecture
A data architecture on GCP: ingest from S3/Parquet + Cloud SQL → processing → BigQuery
data warehouse → BI + a linear-regression ML model, documented as a design deliverable.

- Design: [docs/ejercicio-4/arquitectura.md](docs/ejercicio-4/arquitectura.md)

---
*Originated as the capstone of a Data Engineering program; built on public/sample datasets.*
