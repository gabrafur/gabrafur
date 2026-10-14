<p align="center">
  <img src="./assets/profile-banner.svg" width="100%" alt="Gabriel B. Furlan — Senior Data and Platform Engineer" />
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/gabrielbfurlan/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="Connect on LinkedIn" /></a>
  <a href="mailto:gabrafur@gmail.com"><img src="https://img.shields.io/badge/Email-Contact-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Send an email" /></a>
  <a href="https://github.com/gabrafur?tab=repositories"><img src="https://img.shields.io/badge/Repositories-Explore-111827?style=flat-square&logo=github&logoColor=white" alt="Explore repositories" /></a>
</p>

<p align="center">
  <strong>Vitória, Brazil · Italian / EU citizen</strong><br />
  Eligible to work in the European Union · Open to remote and international opportunities
</p>

I build and operate data platforms that turn business data into reliable analytics and operational decisions. My work spans banking, fraud prevention, commercial analytics, and global data products, with responsibility for architecture, delivery, performance, and production recovery.

**Core stack:** Databricks · PySpark · Python · SQL · Delta Lake · Azure · Airflow

At AB InBev / BEES, I was the technical owner of a global platform delivering real-time datasets for BI, curated tables for Data Science, and model-generated tasks and planned visits through APIs for field representatives.

## Selected impact

- **AB InBev / BEES:** Platform supporting **22+ countries**, processing **50M+ records/day**, and enabling data products and decisioning models that impacted **100K+ users**. Configuration-driven orchestration and platform optimizations reduced runtime by **~35%**, infrastructure cost by **~20%**, and manual operations by **~60%**.
- **Ambev:** Distributed workflows supporting **200K+ monthly promotion campaigns**. Architecture and performance optimization, in partnership with Databricks, reduced Databricks processing costs by **~70%**.

## Featured engineering projects

These independent projects make my engineering decisions reviewable through code, architecture notes, tests, and operational documentation. They use synthetic or sanitized data and contain no proprietary employer code, production data, credentials, or internal business logic.

### [Customer Engagement Data Platform](https://github.com/gabrafur/customer-engagement-data-platform)

Turns synthetic customer activity into ranked recommendations, with explicit controls for data quality, reruns, historical rebuilding, and simulated delivery.

- **Processing:** Five-task Databricks serverless pipeline using PySpark and Unity Catalog managed Delta tables, with quality checks that stop invalid data before publication.
- **Reliability:** An identical rerun inserted **zero new recommendations**; historical replay stayed isolated from normal output and delivery tables.
- **Evidence:** The documented v0.3.0 run passed **17 independent acceptance checks** against persisted state, tied to the deployed source commit and package.

The public demonstration uses 100 synthetic customers and 380 transactions. It validates processing behavior; production-scale experience is described separately above.

`Python` · `PySpark` · `Spark SQL` · `Databricks` · `Unity Catalog` · `Delta Lake`

[![View repository](https://img.shields.io/badge/View-Repository-111827?style=flat-square&logo=github&logoColor=white)](https://github.com/gabrafur/customer-engagement-data-platform)
[![E2E evidence](https://img.shields.io/badge/Databricks-E2E%20Evidence-FF3621?style=flat-square&logo=databricks&logoColor=white)](https://github.com/gabrafur/customer-engagement-data-platform/blob/main/docs/databricks-e2e.md)
[![CI](https://github.com/gabrafur/customer-engagement-data-platform/actions/workflows/test.yml/badge.svg)](https://github.com/gabrafur/customer-engagement-data-platform/actions/workflows/test.yml)
[Architecture and trade-offs](https://github.com/gabrafur/customer-engagement-data-platform/blob/main/docs/interview-walkthrough.md)

---

### [Local AI RTX](https://github.com/gabrafur/local-ai-rtx)

Connects engineering tools to local Ollama-compatible models through MCP and a CLI, with controlled task routing and validation before a result is used.

- **Integration:** Python MCP server and CLI using the standard library, deterministic routing, and log extraction anchored to source content.
- **Operation:** Versioned, checksummed releases with atomic activation and recoverable rollback.
- **Boundaries:** Metadata-only telemetry, experimental inference routes disabled by default, and fallback to the primary model when a route is unavailable or rejected.

`Python` · `Node.js` · `MCP` · `Ollama` · `NVIDIA RTX` · `WSL2` · `GitHub Actions`

[![View repository](https://img.shields.io/badge/View-Repository-111827?style=flat-square&logo=github&logoColor=white)](https://github.com/gabrafur/local-ai-rtx)
[![Release](https://img.shields.io/github/v/release/gabrafur/local-ai-rtx?style=flat-square&label=Release)](https://github.com/gabrafur/local-ai-rtx/releases/latest)
[![CI](https://github.com/gabrafur/local-ai-rtx/actions/workflows/ci.yml/badge.svg)](https://github.com/gabrafur/local-ai-rtx/actions/workflows/ci.yml)

---

### [My Smart Home](https://github.com/gabrafur/my_smart_home)

A continuously operated home-automation platform used to practice event-driven integration, state recovery, and infrastructure maintenance.

- **Resilience:** Node-RED flows handle duplicate events, stale state, retries, and restart recovery.
- **Operations:** Versioned infrastructure, observability, and backup/restore procedures with verification and rollback.
- **Reproducibility:** Public configuration and synthetic tests are separated from private household state; the demo runs without controlling physical devices.

`Python` · `JavaScript` · `Node-RED` · `MQTT` · `Docker Compose` · `Home Assistant` · `Zigbee2MQTT` · `Matter` · `YAML/Jinja`

[![View repository](https://img.shields.io/badge/View-Repository-111827?style=flat-square&logo=github&logoColor=white)](https://github.com/gabrafur/my_smart_home)
[![Validation](https://github.com/gabrafur/my_smart_home/actions/workflows/public-validation.yml/badge.svg)](https://github.com/gabrafur/my_smart_home/actions/workflows/public-validation.yml)
[Technical portfolio tour](https://github.com/gabrafur/my_smart_home/blob/main/docs/ENGINEERING_TOUR.md)

## Engineering approach

- **Design for recovery:** Define processing boundaries, stable identities, retry behavior, and reconciliation so reruns and incident recovery have predictable outcomes.
- **Make decisions reusable:** Turn recurring production problems into shared patterns, configuration-driven workflows, and reviewable architecture decisions.
- **Connect engineering to users:** Work with Product, Data Science, BI, and business stakeholders to clarify what data must reach each consumer and when.
- **Develop the team:** Mentor engineers, review code and designs, and align architecture, delivery, and operational responsibilities.

## Professional background

**AB InBev / BEES · Senior Data Engineer / Data Platform Technical Lead · Feb 2025–Sep 2026**

Owned architecture, orchestration, deployment, observability, and incident response for a global data platform. Built partition-scoped Delta `MERGE` and retry strategies, workflow controls that kept snapshots consistent, and idempotent delivery and reconciliation patterns for concurrent country workloads. Integrated Cosmos DB, files, ODBC sources, and Delta tables into batch and streaming pipelines serving BI, Data Science, and operational APIs.

**Ambev · Data Engineer Specialist / Databricks Lakehouse Engineer · Jun 2022–Feb 2025**

Built Azure Databricks solutions for Revenue Management, marketplace prioritization, and promotion optimization. Integrated intraday weather data for **5,000+ Brazilian cities** and external market research into analytical workflows. Worked with Airflow, Azure Data Factory, Unity Catalog, Azure DevOps, RabbitMQ, and Azure Service Bus.

**Santander Brazil · Senior Data Analyst / Data Engineer, Fraud Analytics · Dec 2019–May 2022**

Built ETL and streaming pipelines, fraud-monitoring data structures, and reusable Python tooling. Worked extensively with **Apache Hive and Impala**. Developed systems connecting anomaly detection to operational workflows and supported fraud-prevention initiatives associated with **~80% lower losses within the covered scope**, approximately **US$200M**.

**Itaú Unibanco · Operations Analytics and Workforce Planning · Dec 2016–Dec 2019**

Progressed from intern to planning and performance analyst. Used SQL, SAS, and operational data to improve forecasting, staffing, routing, and service-center availability. Contributed to approximately **US$5M in annual savings** through resource reallocation and a further **US$10M** through improved service-center availability.

## Technologies and tools

**Data platforms and orchestration**

![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat-square&logo=databricks&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Apache%20Spark-E25A1C?style=flat-square&logo=apachespark&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-3776AB?style=flat-square&logo=python&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-003366?style=flat-square)
![Unity Catalog](https://img.shields.io/badge/Unity%20Catalog-FF3621?style=flat-square&logo=databricks&logoColor=white)
![Azure Data Factory](https://img.shields.io/badge/Azure%20Data%20Factory-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Apache Airflow](https://img.shields.io/badge/Apache%20Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat-square&logo=snowflake&logoColor=white)
![Apache Hive](https://img.shields.io/badge/Apache%20Hive-FDEE21?style=flat-square&logo=apachehive&logoColor=111827)
![Apache Impala](https://img.shields.io/badge/Apache%20Impala-4A5A6A?style=flat-square)

**Languages and development**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=111827)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter%20Notebook-F37626?style=flat-square&logo=jupyter&logoColor=white)

**Cloud, infrastructure, and delivery**

![Microsoft Azure](https://img.shields.io/badge/Microsoft%20Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Docker Compose](https://img.shields.io/badge/Docker%20Compose-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

**Integration, quality, and observability**

![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white)
![Azure Service Bus](https://img.shields.io/badge/Azure%20Service%20Bus-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![REST APIs](https://img.shields.io/badge/REST%20APIs-0F766E?style=flat-square)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
![Datadog](https://img.shields.io/badge/Datadog-632CA6?style=flat-square&logo=datadog&logoColor=white)
![New Relic](https://img.shields.io/badge/New%20Relic-1CE783?style=flat-square&logo=newrelic&logoColor=0B1220)

**AI tools and local inference**

![Codex](https://img.shields.io/badge/Codex-111827?style=flat-square&logo=openai&logoColor=white)
![Claude](https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=anthropic&logoColor=white)
![GitHub Copilot](https://img.shields.io/badge/GitHub%20Copilot-111827?style=flat-square&logo=githubcopilot&logoColor=white)
![Cursor (Composer)](https://img.shields.io/badge/Cursor%20(Composer)-111827?style=flat-square&logo=cursor&logoColor=white)
![Databricks Genie](https://img.shields.io/badge/Databricks%20Genie-FF3621?style=flat-square&logo=databricks&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-111827?style=flat-square&logo=ollama&logoColor=white)
![Model Context Protocol](https://img.shields.io/badge/Model%20Context%20Protocol-4F46E5?style=flat-square)

**Automation and IoT**

![Home Assistant](https://img.shields.io/badge/Home%20Assistant-18BCF2?style=flat-square&logo=homeassistant&logoColor=white)
![Node-RED](https://img.shields.io/badge/Node--RED-8F0000?style=flat-square&logo=nodered&logoColor=white)
![MQTT](https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white)
![Zigbee](https://img.shields.io/badge/Zigbee-EB0443?style=flat-square&logo=zigbee&logoColor=white)
![Matter](https://img.shields.io/badge/Matter-111827?style=flat-square)

## Education and development

- **Postgraduate Specialization in Data Engineering** · Escola Politécnica da USP
- **Bachelor's in Aerospace Engineering** · Universidade Federal do ABC
- **Technical Degree in Electrotechnics** · IFES
- Preparing for the **Databricks Certified Data Engineer Professional** examination.
- Continuing development in **Generative AI, agent engineering, MLOps, and data platform architecture**.
- **Languages:** Portuguese (native) · English (B2 professional) · Spanish (basic)

## Connect

Interested in Senior and Staff opportunities in **Data Engineering and Data Platform Engineering**, with a focus on technical leadership, reliable distributed processing, and global data products.

<p align="center">
  <a href="mailto:gabrafur@gmail.com"><img src="https://img.shields.io/badge/Discuss%20an%20opportunity-gabrafur%40gmail.com-0F766E?style=for-the-badge&logo=gmail&logoColor=white" alt="Contact Gabriel Furlan" /></a>
</p>
