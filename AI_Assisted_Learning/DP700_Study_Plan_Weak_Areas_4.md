## DP-700 Targeted Study Plan – Round 4 (Based on Try 6 – 94%)

On Try 6 you scored **94%** again, with:

- **Implement and manage an analytics solution** – **100%**
- **Monitor and optimize an analytics solution** – **100%**
- **Ingest and transform data** – **80%** (only **one** missed question)

The **only remaining weak spot** in this run:

- Choosing the correct **incremental load/querying pattern into a lakehouse**: **notebook** vs **pipeline** (Q26).

This short guide tightens just that.

---

## Section 1 – Notebooks vs Pipelines for Lakehouse Incremental Loads

### 1.1 What You Need to Know

- **Pipelines (Data Factory in Fabric)**
  - **Orchestration** tool:
    - Run **Copy Data** activities, **notebooks**, **SQL scripts**, etc.
    - Schedule with **triggers** (schedule, tumbling window, event).
  - Good for:
    - End-to-end **ETL/ELT workflows**.
    - Coordinating multiple steps and dependencies.
  - Important: Pipelines themselves are **not** the “querying solution” for incremental logic; they **call** something (like a notebook or SQL) that implements the logic.

- **Notebooks (Spark)**
  - **Code-based data processing + querying** environment.
  - Ideal for:
    - **Incremental load logic** into a **lakehouse**:
      - Read from `/files/...` (e.g., CSVs).
      - Implement watermark or CDC-like patterns in **PySpark/SQL**.
      - Write to **Delta tables** in the `Tables` area.
  - When a question asks for a **“querying solution”** or **“incremental load logic”** for a lakehouse (especially from **files inside the same lakehouse**), the exam strongly favors **notebooks**.

- **Why “notebook” was the right answer in Q26**
  - Scenario: Incremental loads from `/files/sales/` into a **lakehouse table**.
  - Requirement: “identify a **querying solution**” that minimizes maintenance.
  - Pattern:
    - Use **a notebook** where you:
      - Read new CSVs from `/files/sales/`.
      - Determine what’s new (e.g., by Date/ID).
      - Upsert/append into `Sales` Delta table.
  - Pipelines would **orchestrate** when that notebook runs but are **not** the querying/incremental logic themselves.

### 1.2 Quick Quiz – Lakehouse Incremental Patterns

1. You have a Fabric lakehouse `Lakehouse1` with a Delta table `Sales`. New CSV files arrive in `/files/sales/`. You must implement **incremental loads** into `Sales`, and the question asks specifically for a **querying solution**.  
   Which item should you choose?

2. You want to **schedule** that incremental process to run daily at midnight, but you already have the logic implemented in a notebook.  
   Which Fabric component should you use to orchestrate the schedule?

3. A question describes: “You need a low-code pattern that supports full and incremental loads into a lakehouse or warehouse (from various sources) using Power Query.”  
   Which Fabric feature is being tested?

4. Match each scenario with the **best** Fabric component (choose each once):
   - **Scenario A**: Coordinate a series of steps—copy from source, run a notebook, then send a notification.  
   - **Scenario B**: Implement custom incremental logic from files in `/files/...` into a Delta table using PySpark/SQL.  
   - **Scenario C**: Build low-code incremental ingestion/transformation from ADLS Gen2 into a lakehouse.

#### 1.3 Answer Key – Section 1

1. **A notebook** (Spark notebook in the lakehouse workspace).  
2. Use a **Data Factory pipeline** (with a **schedule trigger**) to orchestrate the notebook runs.  
3. **Dataflows Gen2** (Power Query-based ingestion and transformation with full + incremental support).  
4.  
   - **Scenario A → Pipeline (Data Factory)** – orchestration with multiple steps.  
   - **Scenario B → Notebook** – code-based incremental logic against lakehouse files/tables.  
   - **Scenario C → Dataflows Gen2** – low-code ingestion and transformation.

---

At this point, your misses are down to nuance (wording and “best-fit” tool choice). One more 90%+ pass will give you three strong, recent practice runs and excellent DP-700 readiness. 

