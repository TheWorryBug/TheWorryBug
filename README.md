<h1 align="center">Eeshani</h1>

<p align="center">
  <b>Data Engineer focused on cloud data platforms, distributed pipelines, warehouse modeling, and data reliability.</b>
</p>

<p align="center">
  Building data systems that are reliable, traceable, maintainable, and designed for real analytical consumption.
</p>

---

## About

I work on data engineering systems across ingestion, transformation, orchestration, warehouse design, data quality, and analytics enablement.

My interests sit at the intersection of cloud data platforms, distributed processing, analytical modeling, and production reliability. I like building systems where data movement is observable, transformations are explainable, failures are recoverable, and downstream users can trust the outputs.

I care about:

- Clean pipeline design
- Strong source-to-target lineage
- Practical data modeling
- Controlled failure handling
- Reconciliation and validation
- Operational runbooks
- Reusable engineering patterns
- Clear ownership of assumptions, grain, and business logic
- Documentation that helps another engineer operate the system

I prefer simple, reliable systems over clever implementations that become difficult to debug later.

---

## Core Engineering Areas

### Cloud Data Platforms

- Data lake and warehouse architecture
- Raw, refined, and curated data layers
- Batch-oriented ingestion and transformation
- Environment-aware configuration
- Storage layout and partitioning considerations
- Separation of landing, archive, reject, and processed zones
- Pipeline behavior designed for reruns, backfills, and recovery

### Pipeline Engineering

- File-based and API-based ingestion patterns
- Metadata-driven source onboarding
- Idempotent load design
- Duplicate prevention
- Schema validation
- Audit logging
- Retry and failure classification
- Parameterized pipeline execution
- Explicit input and output contracts

### Distributed Transformation

- PySpark-based data processing
- Raw-to-refined standardization
- Deduplication, enrichment, and conformance logic
- Handling malformed, late-arriving, and incomplete records
- Reusable transformation utilities
- Testable business rules
- Transformation logic designed around dataset grain and downstream usage

### Warehouse and Analytics Modeling

- SQL-based transformation layers
- Staging, intermediate, and mart models
- Fact and dimension modeling
- Business keys and surrogate keys
- Incremental loading patterns
- Metric definition consistency
- BI-ready tables with clear grain and ownership
- Models designed for usability, not just storage

### Data Quality and Reliability

- Row count reconciliation
- Aggregate and hash-total checks
- Null, duplicate, and accepted-value validations
- Referential integrity checks
- Freshness checks
- Severity-based issue classification
- Data quality reporting
- Operational notes for failure investigation and reruns

### Orchestration and Operations

- DAG-based dependency design
- Task-level retries and timeouts
- Failure isolation
- Backfill-safe execution
- Alerting and support flows
- CI checks for Python, SQL, and configuration changes
- Runbooks for common operational scenarios

---

## Technical Stack

<p align="left">
  <img src="https://img.shields.io/badge/Python-Pipeline%20Engineering-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/SQL-Modeling%20%26%20Validation-336791?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/PySpark-Distributed%20Processing-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white" />
  <img src="https://img.shields.io/badge/AWS-Cloud%20Data%20Platforms-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white" />
  <img src="https://img.shields.io/badge/Snowflake-Warehouse%20Architecture-29B5E8?style=for-the-badge&logo=snowflake&logoColor=white" />
  <img src="https://img.shields.io/badge/Airflow-Orchestration-017CEE?style=for-the-badge&logo=apacheairflow&logoColor=white" />
  <img src="https://img.shields.io/badge/dbt-Analytics%20Engineering-FF694B?style=for-the-badge&logo=dbt&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub%20Actions-CI%20Checks-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" />
</p>

---

## Projects

### retail-data-platform-aws-snowflake

A retail analytics platform designed around a cloud data lake and warehouse architecture.

The project models an end-to-end data flow from raw operational data to curated analytical marts.

Key areas:

- Raw, silver, and gold data layers
- S3-style data lake organization
- PySpark transformation jobs
- Airflow-style orchestration
- Snowflake-style warehouse models
- dbt-style curated marts
- Data quality checks
- Source-to-target reconciliation
- Lineage documentation
- Operational runbooks

Focus areas:

- Cloud-native data platform design
- Medallion architecture
- Batch pipeline orchestration
- Warehouse modeling
- BI-ready data products
- Production support thinking

---

### metadata-driven-ingestion-framework

A reusable ingestion framework for onboarding multiple sources through configuration instead of hardcoded pipeline logic.

Key areas:

- Source-level configuration
- File ingestion contracts
- API ingestion contracts
- File-drop ingestion simulation
- Schema validation
- Audit logging
- Duplicate prevention
- Retry handling
- Failure tracking
- Load manifest generation

Focus areas:

- Framework-oriented engineering
- Scalable source onboarding
- Idempotent ingestion
- Operational auditability
- Config-driven pipeline behavior

---

### data-quality-reconciliation-platform

A validation and reconciliation layer for improving trust in analytical datasets.

Key areas:

- Row count reconciliation
- Hash-total comparison
- Null checks
- Duplicate checks
- Accepted-value checks
- Referential integrity checks
- Freshness validation
- Severity-based reporting
- Incident and remediation documentation

Focus areas:

- Data reliability
- Source-to-target validation
- Production monitoring
- Business trust in reporting
- Data quality ownership

---

## Engineering Principles

I like working on data systems where the important parts are explicit:

- What is the source?
- What is the grain?
- What changed during transformation?
- What assumptions were made?
- What checks prove the data is usable?
- What happens when something fails?
- Can the pipeline be rerun safely?
- Can another engineer understand and operate it?

For me, good data engineering means designing for correctness, observability, recovery, and long-term maintainability.

---

## How I Use AI in Engineering

I use AI-assisted development as part of a broader engineering workflow, mainly to improve speed, review depth, and iteration quality.

I use it for:

- Exploring implementation options
- Generating repetitive scaffolding
- Reviewing code structure
- Stress-testing design assumptions
- Drafting test cases
- Identifying edge cases
- Improving documentation clarity
- Comparing trade-offs across different approaches

Generated output is never treated as final by default.

My process is:

- Review the logic manually
- Validate against sample data
- Check grain, joins, filters, and aggregations
- Add or adjust tests
- Confirm failure paths and edge cases
- Refactor for readability and maintainability
- Keep final design decisions explainable

AI is useful for acceleration, but the engineering judgment, validation, and ownership stay with me.

---

## What I’m Exploring

I actively follow and experiment with patterns around:

- Lakehouse architecture
- Open table formats
- Modern orchestration patterns
- Data contracts
- Analytics engineering
- Data observability
- Warehouse performance design
- Metadata-driven pipelines
- LLM-assisted developer workflows
- Reliable data product design

I’m especially interested in how data teams can build systems that are faster to change without becoming harder to trust.

---

## Repository Standards

Across my data projects, I try to keep structure consistent and operationally understandable.

```text
project/
├── airflow_dags/
├── config/
├── data_quality/
├── dbt/
├── docs/
├── ingestion/
├── sample_data/
├── spark_jobs/
├── sql/
├── tests/
└── README.md
