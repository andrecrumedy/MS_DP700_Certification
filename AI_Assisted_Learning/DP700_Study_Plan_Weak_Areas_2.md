## DP-700 Targeted Study Plan – Round 2 (Based on 86% Attempt)

You raised your score to **86%** – great progress. The latest attempt shows remaining gaps in a few **specific subtopics**:

- **Data warehouse projects and schema lifecycle (SQL Database Projects in VS Code)**
- **Dynamic Data Masking vs general permissions**
- **Modern ETL patterns for Fabric warehouses (Data Factory vs Synapse/SSIS)**
- **Mirroring types and data store selection**
- **Real-Time hub alerts for semantic model refreshes**
- **Eventhouse Always-On behavior**

This guide focuses **only** on those weak areas. For each section:

- **Review**: concise reminders of what to know.
- **Quiz**: short, exam-style questions (many **“which two/three”**). Answers follow each section.

---

## Section 1 – SQL Database Projects for Fabric Warehouses

### 1.1 What You Need to Know

- **SQL Database Projects in VS Code**
  - Use the **SQL Database Projects extension** to manage Fabric **warehouse schemas as code**.
  - To start from an existing warehouse (`Warehouse1`):
    - Connect in VS Code.
    - **Right-click the connection → Create Project From Database** (imports current schema, does **not** change the live DB).
  - For ongoing deploys:
    - Use an **SDK-style SQL Database Project** (modern .NET-style project) – this is what Fabric Learn content expects.
    - You then **build and deploy** schema changes from the project back to the warehouse.

- **Key distinctions**
  - **Create Project From Database**: imports schema into a project **without** altering the source database.
  - **SDK-style project** vs. “classic” projects:
    - SDK-style is the **recommended** project type going forward (CI/CD friendly, modern tooling).

### 1.2 Quick Quiz – SQL Database Projects

1. You have an existing warehouse `DB1` in Fabric. You want to:
   - Manage schema changes in VS Code as code.
   - Avoid any change to `DB1` when you create the project.
   What **two** steps describe the correct initial setup?
2. You later want to deploy schema changes from VS Code to `DB1` using a project that fits modern tooling and CI/CD.  
   What type of project should you use?
3. Which statement best describes what happens when you choose **Create Project From Database** on a Fabric warehouse connection?

#### 1.3 Answer Key – Section 1

1.  
   - **Add a connection** to `DB1` in VS Code.  
   - **Right-click the connection and select “Create Project From Database”** to import the schema into a new project.  
2. Use an **SDK-style SQL Database Project** and import the schema of `DB1` into it.  
3. It **creates a local project that contains the current schema** of the warehouse **without modifying** the existing database.

---

## Section 2 – Dynamic Data Masking vs Permissions

### 2.1 What You Need to Know

- **Dynamic Data Masking (DDM)**
  - DDM **masks query results** for non-privileged users while keeping underlying data unchanged.
  - Typical masking functions:
    - **`partial(0,'XXXX-XXXX-XXXX-',4)`** – standard for **credit cards** (show last 4).
    - **`email()`** – masks email addresses.
  - DDM is about **obscuring sensitive data**, not blocking all access.

- **UNMASK vs SELECT**
  - **SELECT** permission **does not bypass** DDM; users with only SELECT still see **masked** values.
  - **UNMASK** permission:
    - Grants the ability to see **unmasked** values on columns with DDM.
    - Assign **UNMASK** to roles/users who legitimately need full visibility (e.g., HR, finance).
  - You generally **do not revoke all SELECT** from non-privileged users – they often still need non-sensitive data; DDM controls what they see.

- **Good pattern for protecting sensitive data**
  - Apply **DDM** to sensitive columns (Email, CreditCardNumber, etc.).
  - Grant **UNMASK** only to authorized roles.
  - **Test masking** with a non-privileged user to validate behavior.

### 2.2 Quick Quiz – DDM and Permissions

1. You have a table with `Email` and `CreditCardNumber` columns. Non-privileged users should never see full values; finance staff can.  
   Which **three** actions form the best solution?
2. A security team suggests revoking **SELECT** on all sensitive columns from non-privileged users to “be safe,” while also enabling DDM.  
   Why is this usually **not** the best approach, and what should you do instead?
3. You’ve implemented DDM on several columns. How do you verify that masking works as expected before going live?

#### 2.3 Answer Key – Section 2

1.  
   - Apply **DDM** to `Email` (e.g., `email()` function).  
   - Apply **DDM** to `CreditCardNumber` (e.g., `partial(0,'XXXX-XXXX-XXXX-',4)`).  
   - Grant **UNMASK** permission only to authorized roles/users (e.g., finance).  
2. Revoking SELECT removes all access, even to **non-sensitive** data, which is overly restrictive and impractical.  
   Instead, **keep SELECT** for needed users, apply **DDM** on sensitive columns, and grant **UNMASK** only to those who must see full values.  
3. Log in or test as a **non-privileged user** and run SELECT queries to confirm that sensitive columns appear **masked**, while privileged users (with **UNMASK**) see real values.

---

## Section 3 – Modern ETL for Fabric Warehouses

### 3.1 What You Need to Know

- **Recommended tooling in a Fabric-centric solution**
  - **Data Factory pipelines in Fabric**:
    - Orchestrate **ETL/ELT** from multiple sources (SQL, ADLS, etc.).
    - Run **T-SQL scripts** against warehouses.
    - Handle scheduling, parameters, error handling.
  - **Dataflows Gen2**:
    - **Power Query-based**, low-code transforms.
    - Great for ingesting & shaping data from **ADLS Gen2** and other sources.

- **What is *not* preferred for Fabric ETL**
  - **Azure Synapse Analytics**:
    - Powerful platform, but Fabric exam scenarios usually prefer **Fabric Data Factory + Dataflows** for ETL into Fabric warehouses.
  - **SSIS**:
    - Legacy tool; not the recommended primary ETL stack for new Fabric architectures.

- **End-to-end pattern (for a dimensional model)**
  - **Stage data** in staging tables / lakehouse layers.
  - **Transform data** (cleanse, conform) to match the dimensional model.
  - Use **Data Factory pipelines** + **Dataflows Gen2** to orchestrate and transform.

### 3.2 Quick Quiz – ETL Choices in Fabric

1. You are designing a new ETL process that loads multiple sources (SQL Server, ADLS Gen2) into a Fabric **warehouse** for reporting.  
   Which **two** tools are recommended for orchestration and transformation in a modern Fabric solution?
2. In an exam scenario, you selected **Azure Synapse Analytics** as the primary ETL engine to move and transform data into a Fabric warehouse.  
   Why is this **not** the best answer for DP-700, and what stack should you prefer?
3. You need to ingest and transform raw files from **Azure Data Lake Storage Gen2** before loading them into a dimensional model.  
   Which tool provides a **low-code**, Power Query-based way to do this in Fabric?

#### 3.3 Answer Key – Section 3

1.  
   - **Data Factory pipelines** in Fabric for ETL orchestration and T-SQL execution.  
   - **Dataflows Gen2** for low-code ingestion and transformation, especially from ADLS Gen2.  
2. DP-700 focuses on **Fabric-native** patterns, so Synapse is not the primary ETL choice into Fabric warehouses.  
   Prefer **Data Factory pipelines + Dataflows Gen2** as the recommended combination.  
3. Use **Dataflows Gen2** to ingest and transform data from **ADLS Gen2**.

---

## Section 4 – Mirroring and Data Store Selection

### 4.1 What You Need to Know

- **Mirroring types in Fabric**
  - **Database mirroring**:
    - Copies **data + schema** into Fabric (OneLake).
    - Typical for **Azure SQL DB**, **Azure Cosmos DB**, etc.
  - **Metadata mirroring**:
    - Syncs **metadata only** (tables, schemas, etc.), while data remains in the external engine.
    - Good for compute engines like **Azure Databricks** where Fabric should “see” tables without fully copying data.

- **Exam pattern for mirroring**
  - **Azure Databricks** → **metadata mirroring** (share catalog/metadata, avoid full database copy).  
  - **Azure Cosmos DB** → **database mirroring** (replicate data into Fabric for analytics).

- **Choosing data stores for diverse formats + compute**
  - You need support for **structured, semi-structured, and unstructured** data with both **PySpark and SQL**:
    - **Microsoft Lakehouse** in Fabric:  
      - Native exam-favorite answer for this requirement.
    - **Azure Synapse Analytics**:  
      - Also supports Spark + SQL + multiple formats; often appears as a valid second choice in exam questions.
  - **Azure Data Lake Storage Gen2**:
    - Is **storage only**; it does not natively expose **PySpark + SQL compute** by itself.

### 4.2 Quick Quiz – Mirroring & Stores

1. You must integrate **Azure Databricks** into Fabric so that Fabric can see Databricks tables without duplicating all data.  
   Which mirroring type should you use?
2. You must integrate **Azure Cosmos DB** into Fabric and need the actual data to be queryable within OneLake.  
   Which mirroring type should you use?
3. A question asks for **two** data stores that support structured, semi-structured, and unstructured data and allow both **PySpark and SQL** operations.  
   Which **two** should you pick?
4. In that same question, why is **Azure Data Lake Storage Gen2** not one of the correct answers?

#### 4.3 Answer Key – Section 4

1. Use **metadata mirroring** for **Azure Databricks**.  
2. Use **database mirroring** for **Azure Cosmos DB**.  
3. Choose **Microsoft Lakehouse** and **Azure Synapse Analytics**.  
4. ADLS Gen2 is a **storage layer only**; it doesn’t itself provide the **PySpark and SQL compute** required by the question.

---

## Section 5 – Real-Time Hub Alerts for Semantic Model Refresh

### 5.1 What You Need to Know

- **Goal**: get notified when semantic model refreshes **fail**, without noise from all events.

- **Real-Time hub pattern**
  - In **Real-Time hub**:
    - **Select Fabric workspace item events** as the source.
    - Configure a **filter** (e.g., by item type = semantic model, status = failed).
    - Define **alert actions**, typically:
      - **Send email** for failures (exam-friendly answer).
      - Teams/other targets can be used, but exam questions often highlight **email** as the official step.

- **What is not the core exam answer**
  - A **KQL Queryset** helps analyze logs but does **not** itself send alerts.
  - “Notify via Teams for all refresh events” is usually wrong if the requirement focuses on **failures**, not all events.

### 5.2 Quick Quiz – Semantic Model Alerts

1. You must receive notifications **only when a semantic model refresh fails**.  
   Which **three** actions form the recommended solution in Real-Time hub?
2. Why is “Notify via Teams for all refresh events” usually **not** the best answer for this requirement?
3. What role does a **KQL Queryset** play compared to the Real-Time hub alerts?

#### 5.3 Answer Key – Section 5

1.  
   - **Select Fabric workspace item events** as the event source.  
   - **Configure a filter** (e.g., refresh status = failed).  
   - Configure an **email action** to notify on failures.  
2. It sends messages for **every refresh**, including successful ones, creating noise and not focusing on failures; the requirement is to alert on **failed** refreshes only.  
3. A **KQL Queryset** is for **querying and analyzing** event data, not for emitting real-time alerts; Real-Time hub alerts perform the notification.

---

## Section 6 – Eventhouse Always-On Behavior

### 6.1 What You Need to Know

- **Default behavior**
  - An **eventhouse** suspends automatically after ~10 minutes of inactivity.
  - Suspended eventhouses must be **resumed** before queries can run.

- **Preventing suspension**
  - Use the **Always-On** setting on the eventhouse:
    - In the UI, from the **eventhouse ribbon**, choose **Always-On**.
    - Within that configuration, you can choose a **consumption mode** (such as minimum consumption), but the key exam concept is:
      - You must **enable Always-On** to keep the eventhouse from suspending.

- **Exam nuance**
  - If options include:
    - “From the ribbon, select **Always-On**”  
    - “From the ribbon, select **Always-On, and then Minimum consumption**”  
  - DP-700 answers tend to prefer the **general “Always-On”** option when that is the single correct choice.

### 6.2 Quick Quiz – Eventhouse

1. Your eventhouse keeps suspending after 10 minutes of inactivity, causing delays every time analysts try to query data.  
   What setting must you enable to keep it running?
2. In a multi-choice exam question, one option reads “From the ribbon of Eventhouse1, select **Always-On**,” and another adds “and then choose **Minimum consumption**.”  
   If you can select **only one** answer and the question is about **preventing suspension**, which one should you choose, and why?

#### 6.3 Answer Key – Section 6

1. Enable **Always-On** for the eventhouse.  
2. Choose **“From the ribbon of Eventhouse1, select Always-On”**, because the key requirement is to **prevent suspension**; Always-On is the configuration that does this, and exam answers usually focus on that single setting when only one option can be correct.

---

When you’ve worked through this Round 2 guide, retake the practice exam again. Once you share the next attempt, we’ll tighten any remaining gaps until you’re consistently at **90%+**. 

