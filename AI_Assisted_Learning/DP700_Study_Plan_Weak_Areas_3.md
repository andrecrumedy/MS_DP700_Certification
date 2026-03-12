## DP-700 Targeted Study Plan – Round 3 (Based on 94% Attempt)

You scored **94%**. Only **3 questions** missed this time, which means we should focus on **precision** (exam wording + best-fit patterns), not broad coverage.

Remaining weak areas from Try 5:

- **Incremental updates in a Fabric lakehouse: watermark strategy vs CDC** (Q23)
- **T-SQL TRY/CATCH + transactions: why COMMIT/ROLLBACK fails without BEGIN TRAN** (Q46)
- **Eventstream monitoring: Data insights vs Runtime logs vs “change transformation logic”** (Q47)

This guide focuses **only** on those weak areas. For each section:

- **Review**: short, high-signal reminders.
- **Quiz**: exam-style questions, heavy on **“which two/three”** multi-select. Answers are right below.

---

## Section 1 – Incremental Updates in a Fabric Lakehouse (Watermark vs CDC)

### 1.1 What You Need to Know

- **Watermark strategy (incremental loads)**
  - A **watermark** is a “high-water mark” value (typically a **timestamp** like `LastModifiedDate` or a **monotonic ID**) that tracks the **last successfully processed** point.
  - Each run loads only rows where the change key is **greater than** the stored watermark.
  - Key exam cues that point to watermark:
    - “**updated incrementally**”
    - “**reflect changes** from source systems”
    - “**regular updates**”
    - “**efficient incremental method**” (especially when no CDC feature is stated as available)
  - Why it’s favored: **simple**, **low overhead**, works broadly with many sources.

- **CDC (Change Data Capture)**
  - CDC is a feature/pattern where the source system emits a **change feed** (inserts/updates/deletes).
  - CDC is great **when explicitly supported and required**, but exam wording often expects watermark when:
    - The question doesn’t say CDC is enabled/available, or
    - It’s specifically about “incremental updates” in lakehouse without calling for “capture deletes” or “track all changes.”

- **Quick discriminator**
  - **Watermark** = “only pull what changed since last time” using a **last-updated** marker.
  - **CDC** = “pull from an explicit change log/feed” (often includes deletes/updates as events).

### 1.2 Quick Quiz – Watermark vs CDC

1. You have a Fabric lakehouse that is refreshed regularly from operational systems. You must update incrementally to reflect changes with minimal complexity.  
   What is the best method?

2. You need to implement incremental loads into a lakehouse. Which **two** items are essential for a watermark-based approach?

3. A requirement says: “capture inserts, updates, and deletes from the source system in near real time.”  
   Which approach is the best fit?

4. You have a table with `LastModifiedDate`. Which **two** statements best describe how a watermark works in practice?

#### 1.3 Answer Key – Section 1

1. **Implement a watermark strategy.**
2.  
   - A **change-tracking column** (e.g., `LastModifiedDate` or increasing ID).  
   - A stored **watermark state** (persist “last processed value” after successful runs).  
3. **Use CDC** (or an explicit change feed), because deletes/updates/inserts tracking is the core requirement.  
4.  
   - Each run loads rows where `LastModifiedDate` is **greater than** the stored watermark.  
   - After a successful run, the watermark is updated to the **latest processed** `LastModifiedDate`.

---

## Section 2 – T-SQL TRY/CATCH with Transactions (BEGIN TRAN is required)

### 2.1 What You Need to Know

- **Core rule**
  - You cannot **COMMIT** or **ROLLBACK** a transaction that was never started.
  - If code contains `COMMIT TRANSACTION;` but there is no preceding **`BEGIN TRANSACTION;`**, you will get failures (or “no corresponding BEGIN TRANSACTION” behaviors).

- **Correct pattern (exam-friendly)**
  - Put **`BEGIN TRANSACTION`** inside the **TRY** block before the work.
  - `COMMIT` in **TRY** after the work.
  - `ROLLBACK` in **CATCH** (often guarded by `IF @@TRANCOUNT > 0` in real-world SQL, but exams often focus on the missing BEGIN TRAN).

- **Common trap answers**
  - “Remove ROLLBACK” is almost always wrong: it breaks exception safety.
  - “Move COMMIT into CATCH” is wrong: CATCH is for cleanup, not success.

### 2.2 Quick Quiz – Transactions + TRY/CATCH

1. You see code that does `COMMIT TRANSACTION;` inside TRY but there is no `BEGIN TRANSACTION;`.  
   What single change fixes the root cause while keeping exception handling?

2. Which **two** statements are true about proper TRY/CATCH transaction handling?

3. A developer suggests removing `ROLLBACK TRANSACTION` from the CATCH block to stop errors.  
   Why is this a bad idea?

#### 2.3 Answer Key – Section 2

1. Add **`BEGIN TRANSACTION;`** at the start of the TRY block (before the INSERT/UPDATE/DELETE).  
2.  
   - **COMMIT** should happen only when the TRY block completes successfully.  
   - **ROLLBACK** should happen in CATCH to undo partial work when an error occurs.  
3. It leaves failed operations **unrolled back**, can leave the session in a bad transaction state, and breaks the “all-or-nothing” guarantee the transaction is supposed to provide.

---

## Section 3 – Eventstream Monitoring (Data insights vs Runtime logs)

### 3.1 What You Need to Know

- **Eventstream monitoring toolkit**
  - **Data insights**:
    - High-level **metrics/telemetry** about throughput, latency, event health.
    - Use it to identify **patterns** and performance bottlenecks quickly.
  - **Runtime logs**:
    - Detailed error information for diagnosing **what failed** and **why**.
    - Use filters such as **severity** to prioritize urgent issues.

- **Exam trap: “modify transformation logic”**
  - When the requirement is “identify and resolve runtime errors” **via monitoring**, the best answers are typically:
    - **Check Data insights**
    - **Review Runtime logs**
    - **Filter logs by severity**
  - “Modify transformation logic” is an **action you might take later**, but it’s not a monitoring step and is often not selected when the question asks what to do to **identify/diagnose** errors.

### 3.2 Quick Quiz – Eventstream Monitoring

1. Frequent runtime errors are affecting event processing. You need to identify and resolve runtime errors efficiently.  
   Which **three** actions should you take?

2. You want to quickly spot throughput drops or latency spikes in an eventstream.  
   Which monitoring view is most appropriate?

3. You need exact error details (stack/exception messages) for event processing failures.  
   Which monitoring artifact should you review?

4. A question asks for **monitoring steps**, but one option is “Modify data transformation logic.”  
   Why is that often **not** selected as part of the correct set?

#### 3.3 Answer Key – Section 3

1.  
   - **Check Data insights for event metrics.**  
   - **Review Runtime logs for error details.**  
   - **Filter logs by error severity.**  
2. **Data insights** (metrics view).  
3. **Runtime logs**.  
4. Because it’s a **remediation/change step**, not a monitoring/diagnostic step; the question is usually testing whether you know where to **observe** metrics and **inspect** errors first.

---

If you retake again, your target is to keep **Monitor and optimize** at **90%+** (it was 88% this run). With these three topics patched, you should be positioned to hit **3 consecutive 90%+** attempts.

