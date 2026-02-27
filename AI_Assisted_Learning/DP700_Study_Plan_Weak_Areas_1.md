## DP-700 Targeted Study Plan (Based on Your Practice Results)

You scored **78%** on the recent full practice assessments. Both attempts highlight three weaker areas:

- **Implement and manage an analytics solution**
- **Ingest and transform data**
- **Monitor and optimize an analytics solution**

This guide is structured **section by section**. For each section:

- **Review**: short, focused concepts you must know.
- **Quiz**: precise scenario-style questions to check mastery. Answers are at the end of each section.

---

## Section 1 – Implement and Manage an Analytics Solution

### 1.1 What You Need to Know

- **Workspaces, domains, and data mesh**
  - **Domains**: logical business areas in Fabric; they own workspaces and governance.
  - **Subdomains**: hierarchical structure inside domains for finer ownership.
  - **Workspaces**:
    - Assigned to **one domain** only.
    - Can also be assigned to a **subdomain** (from *workspace settings*).
  - **Data mesh governance**:
    - Use **domains** to delegate governance to business units.
    - **Delegate tenant-level settings to domains** so each domain can manage its own rules.
    - **Assign workspaces to domains** and **specify domain admins** for independent management.

- **Roles, permissions, and least privilege**
  - **Workspace roles**:
    - **Admin**: full control over workspace, including permissions.
    - **Member**: edit and publish most content.
    - **Contributor**: create and edit content but less administrative control.
    - **Viewer**: read-only for all items in the workspace.
  - **Item permissions**:
    - Use **item-level permissions** (e.g., on a lakehouse or warehouse) when you want access to **one specific item** without broad workspace access.
    - For least privilege, prefer **item permissions** over giving workspace roles if the user only needs one item.

- **Security options in warehouses**
  - **Dynamic Data Masking (DDM)**:
    - Use DDM to **obscure sensitive data in query results** for non-privileged users.
    - Common function for cards: `partial(0,'XXXX-XXXX-XXXX-',4)` to show last 4 digits.
    - Grant **UNMASK** permission to roles/users who must see real values.
  - **Column-level security**:
    - Restrict access to specific columns (e.g., `Salary`, `TransactionHistory`) to a role (such as HR).
    - Pattern:
      - Create an **HR role**.
      - **Grant SELECT** on sensitive columns to HR role.
      - **Deny SELECT** on sensitive columns to other roles.
  - **Row-level security (RLS)**:
    - Use security policies/filter predicates to restrict **which rows** a user can see (e.g., department-based views of sales data).

- **Deployment pipelines and CI/CD**
  - **Stages**: Development → Test → Production.
  - **Assigning workspaces**:
    - Dev stage: source workspace.
    - Test/Prod stages: when you assign a new workspace to a downstream stage, **content from Dev is deployed there**.
  - **Selective deployment**:
    - Use **selective deployment** to move only specific artifacts (e.g., only a dataset or report).
  - **Deployment rules**:
    - Use **deployment rules** to change environment-specific settings (e.g., connection strings for Test vs Prod).
    - Define rules per stage to avoid manual edits after deployment.
  - **Pipeline security**:
    - Only users with **pipeline admin roles** should be able to change pipeline settings.

- **CI/CD concepts**
  - CI/CD in Fabric usually combines:
    - **Deployment pipelines** for promotion across stages.
    - **Git integration** for version control of semantic models, reports, and some data items.
  - Goal: **automated, repeatable deployments** with minimal manual steps and clear separation of environments.

- **Spark pools and environments**
  - **Starter pool**: shared, limited; good for small ad-hoc work, not for heavy/latency-sensitive jobs.
  - **Custom Spark pools**:
    - Use **autoscaling** and **dynamic allocation of executors** to adjust resources to workload.
    - Use **session tags** to **reuse** Spark sessions and reduce start-up overhead.
    - Use **native execution engine** (when available) for complex transformations on Delta tables.
  - **High concurrency mode**:
    - Configure in **Data Engineering/Science workspace settings** for concurrent users sharing sessions.

- **Data stores & integration**
  - **Lakehouse vs Warehouse vs Eventhouse vs KQL DB**:
    - **Lakehouse**: structured + semi/unstructured, supports PySpark + SQL; great for analytics and ML.
    - **Warehouse**: relational, T-SQL focused, star-schema analytics, SQL-based ingestion (e.g., `COPY`).
    - **Eventhouse / KQL DB**: optimized for real-time and log/event analytics using **KQL**.
  - **Mirroring**:
    - Use **database mirroring in Fabric** to continuously replicate data (e.g., from Azure SQL DB to OneLake) in near real time without complex ETL.
  - **Shortcuts**:
    - Use **OneLake shortcuts** to point to external storage (e.g., ADLS, S3) without duplicating data.

### 1.2 Quick Quiz – Implement and Manage an Analytics Solution

Answer these before checking the key.

1. You are implementing a data mesh in Fabric. Business units must manage their own governance rules.  
   Which **two** actions best support this requirement?
2. You have a workspace in `Domain1` and a subdomain `Subdomain1`. You want the workspace to belong to `Subdomain1` while staying in `Domain1`.  
   Where do you change this configuration?
3. A contractor needs **read-only access to a single lakehouse** in a workspace, and nothing else.  
   What is the most appropriate way to grant this access?
4. In a data warehouse table, you must show only the last four digits of `CreditCardNumber` to non-privileged users while letting finance staff see the full value.  
   - a) Which masking function do you use?  
   - b) Which permission do finance staff need?
5. You must ensure only HR staff can see `Salary` and `SocialSecurityNumber` columns.  
   Which **three** steps should you take?
6. In a deployment pipeline, you must ensure the **Production** stage always points to the production database connection string without manual edits after each release.  
   What should you configure?
7. You want to **deploy only one dataset and one report** from Test to Production, leaving everything else unchanged.  
   What deployment feature do you use?
8. Spark jobs in your custom pool run long and often sit idle between notebook executions. You want to improve efficiency without hardcoding resource sizes.  
   Which **two** environment features should you enable?

#### 1.3 Answer Key – Section 1

1. **Delegate tenant settings to domains** and **assign workspaces to the appropriate domains** (and specify domain admins).  
2. From the **workspace settings**, assign the workspace to the subdomain (`Subdomain1`); you do **not** move the domain.  
3. Use **item-level permissions** on the lakehouse, granting the contractor read access only to that item (principle of least privilege) instead of giving a workspace Viewer role.  
4.  
   - a) Use `partial(0,'XXXX-XXXX-XXXX-',4)` dynamic data masking function.  
   - b) Grant the **UNMASK** permission to the finance role/users.  
5.  
   - Create an **HR role** and assign HR users to it.  
   - **Grant SELECT** on `Salary` and `SocialSecurityNumber` to the HR role.  
   - **Deny SELECT** on those columns to other roles.  
6. Create a **deployment rule** for the Production stage that sets the correct production database connection.  
7. Use **selective deployment** in the deployment pipeline.  
8. Enable a **custom Spark pool with autoscaling** and **dynamic allocation of executors** (optionally combined with **session tags** to reuse sessions).

---

## Section 2 – Ingest and Transform Data

### 2.1 What You Need to Know

- **Choosing the right ingestion tool**
  - **COPY statement**:
    - Best for **batch loading** from blob/ADLS into a Fabric **warehouse** using T-SQL.
    - Use with **SAS tokens** for secure access.
  - **Dataflows Gen2**:
    - Low-code **Power Query**-based ingestion & transformation.
    - Supports **full and incremental loads** into lakehouse/warehouse.
  - **Pipelines (Data Factory in Fabric)**:
    - Orchestrate **end-to-end ETL**: copy activities, notebook runs, SQL script activities.
    - Use **triggers** (schedule, event, tumbling window) to automate runs.
  - **Notebooks (Spark)**:
    - Code-heavy, highly flexible pattern (PySpark, Scala, SQL).
    - Good for custom incremental logic, complex transformations, ML.
  - **Eventstream / Event processor**:
    - For **streaming**/real-time data from Event Hubs, Kafka, etc.
    - Use **event processor** to filter and transform data before writing to lakehouse/eventhouse.

- **Full vs Incremental loads**
  - **Full load**:
    - Replace or truncate-and-load entire dataset.
    - Simple but slow and resource-heavy for large tables.
  - **Incremental load**:
    - Load only new or changed data (typically based on a high-watermark like `LastModifiedDate` or identity key).
    - Use **Change Data Capture (CDC)** when available to track changes.
  - Best practices:
    - For large fact tables: **CDC + incremental loads** instead of frequent full reload.
    - Divide large loads into **batches** and **group INSERTs** to improve performance.

- **Lakehouse patterns and Delta tables**
  - **Delta format**:
    - Transactional, supports ACID, time travel, streaming + batch.
  - Performance maintenance:
    - **OPTIMIZE**: consolidate many small files into fewer larger ones.
    - **V-Order**: optimize ordering, encoding, compression for fast queries.
    - **VACUUM**: remove obsolete files to free space and reduce file scan overhead.
  - Streaming:
    - Use **Spark Structured Streaming with Delta tables** for streaming ingestion and near real-time analytics.

- **Pipelines: parameters, expressions, and triggers**
  - **Parameters**:
    - Use pipeline parameters to pass values like file paths, table names, dates.
  - **Dynamic expressions & string interpolation**:
    - Build dynamic dataset paths, queries, and outputs at runtime instead of hardcoding.
  - **Triggers**:
    - **Schedule trigger**: run once per day/hour/etc.
    - **Event triggers** (e.g., storage events): run on file arrival.
    - **Tumbling window**: fixed-size, non-overlapping time windows for periodic, grouped processing.

- **Choosing data stores for ingestion**
  - **Lakehouse**:
    - Use when you need **flexible schema**, support for files + tables, and both SQL + Spark.
  - **Warehouse**:
    - Use for **relational analytics**, star schemas, serving BI with T-SQL.
  - **KQL DB / Eventhouse**:
    - Use for **log/event** and near-real-time analytics with KQL.

### 2.2 Quick Quiz – Ingest and Transform Data

1. You have sales data landing as CSV files in ADLS. You need **high-throughput batch loads into a Fabric warehouse** with minimal orchestration and best performance.  
   Which ingestion method should you use?
2. You created a lakehouse for analytics and want a **low-code solution** that supports both full and incremental loads into that lakehouse.  
   Which Fabric feature do you choose?
3. A fact table in your data warehouse is currently reloaded in full every hour, causing performance bottlenecks.  
   Which **two** tactics best address this?
4. You notice that queries against a Delta table in the lakehouse are slowing down because there are thousands of small Parquet files.  
   Which **two** maintenance operations should you use?
5. You are processing streaming IoT data from Event Hubs into a lakehouse. You want to **remove unnecessary columns (such as sensor IDs) before storage**, and you prefer a no-/low-code approach in Fabric.  
   What component should you configure?
6. You are designing a pipeline that must load multiple different datasets using the same logic but different paths and table names.  
   Which **two** pipeline features should you use to avoid hardcoding values?
7. You need a pipeline that runs automatically **once per day** at midnight.  
   Which trigger type should you configure?
8. Your team wants a single store that can handle structured, semi-structured, and unstructured data, accessible via **both PySpark and SQL** in Fabric.  
   Which data store type best fits this need?

#### 2.3 Answer Key – Section 2

1. Use the **`COPY` statement with a SAS token** to batch-load data into the warehouse.  
2. Use **Dataflows Gen2**, which supports both full and incremental loads into lakehouse/warehouse.  
3.  
   - Implement an **incremental load strategy** instead of full reloads.  
   - Use **Change Data Capture (CDC)** or similar change-tracking to feed incremental loads.  
4. Use **OPTIMIZE** to consolidate small files and **V-Order** (and/or **VACUUM**) to optimize layout and remove obsolete files.  
5. Use the **event processor** within **Eventstream** to filter and transform events before writing to the lakehouse.  
6. Use **pipeline parameters** and **dynamic expressions/string interpolation** in activities/datasets.  
7. Configure a **schedule trigger** for the pipeline.  
8. Use a **Fabric lakehouse** (supports structured/semi/unstructured data with both PySpark and SQL).

---

## Section 3 – Monitor and Optimize an Analytics Solution

### 3.1 What You Need to Know

- **Monitoring in Fabric**
  - **Monitor hub**:
    - Central place to track **pipelines, dataflows, semantic models, and other activities**.
    - Filter by **status**, **time**, and **item** to find failures or performance issues.
  - **Alerts and notifications (Real-Time hub / events)**:
    - Configure **alerts** for workspace events (e.g., pipeline failures, refresh failures, transformation events).
    - Use **Real-Time hub + Activator** for event-driven automation (e.g., send Teams/email, run a pipeline).

- **Monitoring ingestion and transformations**
  - Use **Monitor hub** to specifically:
    - Track **pipeline runs** (success, failure, duration).
    - Track **dataflow refresh** status and diagnose failures.
    - Track **lakehouse ingestion** activities.
  - For streaming:
    - For **Eventstream**: use **Data insights** + **Runtime logs**, filter by severity to identify bottlenecks/errors.

- **Troubleshooting common issues**
  - **Dataflow Gen2 refresh via gateway fails after ~1 hour**:
    - First check the **gateway version** (often a mismatch/outdated gateway).
  - **Pipelines timing out or failing**:
    - Check **Monitor hub** and use **Fail activity with custom error message/code** to fail gracefully and surface clear diagnostics.
  - **Refresh or pipeline limits**:
    - Know Data Factory limits (e.g., max activity run timeout, queued runs, etc.) for deeper troubleshooting.

- **Performance optimization – warehouses**
  - **Automatic tuning**:
    - Enable **automatic tuning** so the system auto-manages indexes and query plans.
  - **Loading performance**:
    - Prefer **batch INSERTs** and **divide large inserts into smaller parts**.
    - Use **COPY** for bulk ingestion.
  - **Table maintenance** (for Delta in lakehouse, but impacts warehouse queries if they read from lakehouse):
    - Use **OPTIMIZE**, **V-Order**, **VACUUM** as in Section 2.

- **Performance optimization – Spark**
  - **Autoscaling & dynamic allocation**:
    - Enable **autoscaling** in Spark pools to scale nodes based on workload.
    - Enable **dynamic allocation of executors**.
  - **Native execution engine**:
    - Turn on **native execution engine** for complex transformations and aggregations on Delta tables.
  - **Session management**:
    - Use **session tags** to reuse sessions and reduce startup costs.
  - **High concurrency**:
    - Use **high concurrency mode** when many users share the same workspace and need concurrent interactive sessions.

- **Capacity and Always-On**
  - **Eventhouse**:
    - By default, suspends after inactivity (~10 minutes).
    - Enable **Always-On** to keep it running and avoid manual resume; choose **Minimum consumption** for lower cost.  
  - **Notebooks**:
    - Increase **workspace session timeout** to reduce “session timed out after inactivity” problems.

### 3.2 Quick Quiz – Monitor and Optimize

1. You need a **single place** in Fabric to see the history of all pipeline runs, dataflow refreshes, and related activity to identify failures and long-running jobs.  
   Which feature should you use?
2. An intermittent Dataflow Gen2 refresh that uses an on-prem gateway fails after about one hour.  
   What is the **first** thing you should check?
3. A pipeline sometimes fails due to a missing source in a Lookup activity. You want the pipeline to **fail with a clear, custom error message and code** when this happens.  
   Which activity do you add, and what do you configure on it?
4. Your warehouse queries have become slow during peak periods. You want **automatic** query tuning without ongoing manual index management.  
   What feature do you enable?
5. An eventhouse suspends after 10 minutes of inactivity and must be manually resumed before queries work. You want it to stay available with minimal administrative effort.  
   What should you configure?
6. You manage an Eventstream that frequently experiences runtime errors. You want to quickly identify patterns and prioritize critical issues.  
   Which **two** tools/actions in Eventstream monitoring should you use?
7. Complex Spark jobs on Delta tables are running slowly. You are **not allowed to modify the job code**, only environment settings.  
   Which environment feature should you enable to optimize these jobs?
8. You run notebooks in a workspace and often see “Your session timed out after inactivity,” requiring manual session start before each run.  
   What configuration change in the workspace should you make?

#### 3.3 Answer Key – Section 3

1. Use the **Monitor hub** in Fabric.  
2. Verify the **version of the on-premises data gateway** (and update if necessary).  
3. Add a **Fail activity** and configure its **custom error message and error code** so the pipeline fails clearly when the Lookup error occurs.  
4. Enable **automatic tuning** on the Fabric SQL warehouse.  
5. Enable **Always-On** for the eventhouse (ideally with **Minimum consumption** mode for lower cost).  
6. Use **Data insights** to see event metrics and **Runtime logs filtered by severity** to prioritize critical errors.  
7. Enable the **native execution engine** in the Spark environment settings.  
8. **Increase the workspace session timeout** so sessions do not expire so quickly.

---

You can now work through these sections one at a time. Once you feel solid on all three, we can move to **exam-style mixed drills** that interleave all topics until you are consistently scoring **90%+**.

