# Homelab Data Platform — Engineering Portfolio

**A production-informed, independently implemented Data Engineering platform on a single HP homelab server.**

This repository is the **central architecture overview and GitHub Pages website** for the projects below. It contains documentation and a public showcase, **not** a copy of any employer's production environment.

## Components and source repositories

| Area | Repository | Purpose |
| --- | --- | --- |
| Infrastructure & identity | [outline_wiki](https://github.com/glazole/outline_wiki) | Nginx, Keycloak, RustFS S3, Outline and shared services |
| Orchestration | [homelab-airflow](https://github.com/glazole/homelab-airflow) | Apache Airflow, schedules, DAGs and local task execution |
| Lakehouse & compute | [homelab-sparkice](https://github.com/glazole/homelab-sparkice) | Spark, Iceberg, JupyterHub and object storage |
| Analytics | [homelab-analytics-stack](https://github.com/glazole/homelab-analytics-stack) | PostgreSQL, ClickHouse, pgAdmin and Metabase |

**Planned extension:** Kafka and NiFi for event ingestion and integration.

## Website

The static portfolio is in [docs/index.html](docs/index.html). After enabling GitHub Pages with **Settings → Pages → Deploy from a branch → main → /docs**, it will be available at:

**https://glazole.github.io/homelab-data-platform/**

The site does not require a backend, database, or credentials. Internal homelab services are intentionally not exposed as public demos.

## Engineering background

The homelab reflects architectural patterns learned while designing, implementing and operating Data Engineering solutions over roughly three years in real production work. The public code, configurations and descriptions are independently prepared for demonstration. No production data, source code, access credentials or non-public system details belong in this portfolio.

This is a **single-host laboratory**, not a highly available production cluster. Hardware budgets and operational assumptions differ from enterprise deployments.

## Architecture principles

- **Separation of concerns:** Airflow orchestrates tasks; Spark processes data; Iceberg structures tables; S3-compatible storage holds objects.
- **Shared platform services:** reverse proxy, authentication and persistence are reused across projects rather than duplicated in every Compose file.
- **Reproducibility:** independent Git repositories, documented prerequisites, smoke tests and explicit limits.
- **Operational realism:** integrations, retries, observability and failure handling should be demonstrated with safe synthetic workloads.

## Owner

[Oleg Glazkov — GitHub](https://github.com/glazole) · Data Engineering · Data Platforms · Applied AI & Research
