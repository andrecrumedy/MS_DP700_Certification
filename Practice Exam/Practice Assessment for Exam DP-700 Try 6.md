It took you 37 minutes to complete this assessment.

Overall Results
To be better prepared for the exam, aim to achieve a score of 80% or higher in multiple attempts.

Score: 94%

Performance by assessment section
To further strengthen your skills in the following areas, refer to the Customized Learning Material section below.

Implement and manage an analytics solution - Passed with 100%

Ingest and transform data -  passed with 80%

Monitor and optimize an analytics solution - passed with 100%

Answer Summary
Below is a summary of your answers.

Question 1 of 50
Your company uses Microsoft Fabric for data engineering workflows.

You notice that Spark jobs are slow due to suboptimal resource allocation.

You need to enhance the Spark job efficiency by adjusting environment settings.

What should you do?

Your Answer
Enable dynamic allocation of executors.

This answer is correct.
Correct Answer
Enable dynamic allocation of executors.

This answer is correct.
Enabling dynamic allocation of executors in the Spark environment settings is beneficial because it allows the system to adjust resources based on the workload, thereby improving efficiency. Setting a fixed number of nodes or a fixed memory allocation for executors can lead to inefficient resource usage as they do not adapt to varying workloads. Increasing the number of partitions is a common misconception that it will improve job efficiency, but it can lead to overhead and not necessarily enhance resource allocation.

Prepare to use Apache Spark - Training | Microsoft Learn
Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn

Question 2 of 50
Your organization uses Microsoft Fabric for data engineering.

You notice delays with Apache Spark jobs due to high demand on shared resources.

You need to optimize the Spark job execution time by configuring a custom Spark pool.

What should you do?

Your Answer
Create a custom Spark pool with autoscaling enabled and set the maximum nodes based on peak load.

This answer is correct.
Correct Answer
Create a custom Spark pool with autoscaling enabled and set the maximum nodes based on peak load.

This answer is correct.
Creating a custom Spark pool with autoscaling enabled and setting the maximum number of nodes based on expected peak load is effective because it allows the system to dynamically adjust resources according to demand, ensuring efficient job execution. Enabling static allocation of executors or nodes would lead to inefficient resource usage, as it fails to adapt to varying workloads. Increasing the node size of the existing starter pool is not feasible since the node size is predefined and cannot be modified. Using a custom Spark pool with a fixed number of nodes does not address the core issue of resource contention and may result in inefficient resource usage.

Prepare to use Apache Spark - Training | Microsoft Learn
Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn

Question 3 of 50
You have a Fabric workspace named Workspace1 that contains an Apache Spark pool.

You plan to create a notebook named Notebook1 in Workspace1.

You need to ensure that Notebook1 uses high concurrency mode so that Spark sessions can be shared across multiple concurrent users or processes.

Which Workspace settings should you configure?

Your Answer
Data Engineering/Science Settings />

This answer is correct.
Correct Answer
Data Engineering/Science Settings />

This answer is correct.
High concurrency for Spark is controlled via Data Engineering/Science Settings; other settings are unrelated.

Prepare to use Apache Spark

Question 4 of 50
Your organization uses Microsoft Fabric deployment pipelines with stages: Development, Test, and Production.

You need to configure the Production stage to connect to the production database. The solution must minimize administrative effort.

What should you do?

Your Answer
Create a deployment rule for Production.

This answer is correct.
Correct Answer
Create a deployment rule for Production.

This answer is correct.
Creating a deployment rule for the Production stage is essential to ensure the production database connection remains intact during deployments. Using deployment pipelines to manage database connections is a common misconception, as they are not specifically designed for this purpose. Using a script to update the database connection can introduce complexity and potential errors if not managed properly. Full deployment updates all content but does not specifically address the need to maintain certain settings, such as database connections.

Get started with deployment pipelines - Training | Microsoft Learn

Question 5 of 50
Your organization uses Microsoft Fabric with deployment pipelines to deploy an analytics solution over multiple stages.

You need to ensure database connections are correct after deploying content in each stage.

What should you do?

Your Answer
Define deployment rules.

This answer is correct.
Correct Answer
Define deployment rules.

This answer is correct.
To ensure database connections remain correct after content deployment, defining deployment rules is crucial. This method allows specifying database connections for each stage, directly addressing the need for accuracy. Using deployment pipelines might seem like a way to manage connections but does not guarantee their correctness post-deployment. Checking database connection settings can help verify current configurations but does not actively maintain them post-deployment. Automatic binding might seem like it ensures correct connections but does not focus on updating database connections.

Get started with deployment pipelines - Training | Microsoft Learn

Question 6 of 50
You have a Fabric workspace named Workspace1 that contains a notebook named Notebook1.

You need to implement version control for Notebook1. The solution must ensure that you can revert Notebook1 to any previous state.

What should you do?

Your Answer
Connect Workspace1 to a Git repository.

This answer is correct.
Correct Answer
Connect Workspace1 to a Git repository.

This answer is correct.
Connecting the workspace to Git enables commits and versioning; deployment pipelines move content between stages, branching requires a Git repo first, and Data Factory pipelines do not provide source control.

Notebook source control and deployment

Question 7 of 50
You have a Fabric data warehouse named Warehouse1.

You need to create a database project for Warehouse1 in Microsoft Visual Studio Code. The solution must allow you to later modify the schema of Warehouse1 from within Visual Studio Code. The solution must NOT affect the existing schema of Warehouse1 when the project is created.

What should you do first?

Your Answer
Add a connection to Warehouse1, right-click the connection, and select Create Project From Database.

This answer is correct.
Correct Answer
Add a connection to Warehouse1, right-click the connection, and select Create Project From Database.

This answer is correct.
Creating a project from the connected database imports schema into a project without altering the database; other actions either don’t create a project or don’t import existing schema.

Use SQL Database Projects

Develop warehouse projects in Visual Studio Code

Question 8 of 50
You have a data warehouse named DB1.

You need to use a database project to deploy schema changes to DB1.

What should you do?

Your Answer
Create a new SDK-style project, and import the schema of DB1 into the project.

This answer is correct.
Correct Answer
Create a new SDK-style project, and import the schema of DB1 into the project.

This answer is correct.
Use an SDK-style SQL Database Project and import the existing database schema; the DAC approaches or non-SDK projects do not meet the requirement.

Use SQL Database Projects

Get started with SQL database projects

What are SQL database projects?

Question 9 of 50
You have a table named CustomerInfo table that contains the following columns: CustomerID, Name, Address, and CreditCardNumber.

You need to apply a mask to the CreditCardNumber column to comply with the data governance policy.

What should you do?

Your Answer
ALTER TABLE CustomerInfo ALTER COLUMN CreditCardNumber ADD MASKED WITH (FUNCTION = 'partial(0,"XXXX-XXXX-XXXX-",4)');

This answer is correct.
Correct Answer
ALTER TABLE CustomerInfo ALTER COLUMN CreditCardNumber ADD MASKED WITH (FUNCTION = 'partial(0,"XXXX-XXXX-XXXX-",4)');

This answer is correct.
The SQL statement to add a partial mask to the CreditCardNumber column effectively complies with the data governance policy by displaying only the last four digits, which is a standard practice for credit card masking. Adding a default mask would not provide the necessary partial masking. Creating a view with static masked values fails to provide dynamic masking based on user permissions, which is necessary for compliance. Creating a view without applying any masking does not protect the data.

How to implement dynamic data masking in Fabric Data Warehouse - Training | Microsoft Learn
Dynamic data masking in Fabric data warehousing - Training | Microsoft Learn

Question 10 of 50
Your company uses a Microsoft Fabric data warehouse to store employee salary information.

You need to configure permissions so that only specific users can view unmasked salary data while others see masked data.

Which permission should you grant to the authorized users?

Your Answer
Grant UNMASK permission.

This answer is correct.
Correct Answer
Grant UNMASK permission.

This answer is correct.
Granting the UNMASK permission is essential as it specifically allows authorized users to view unmasked data in columns where dynamic data masking is applied, meeting the requirement to differentiate access levels. The ALTER ANY MASK permission enables modification of masking rules but does not permit viewing unmasked data, making it unsuitable for this task. The VIEW DEFINITION permission allows users to view metadata about database objects but does not grant access to view unmasked data, thus failing to meet the objective. The SELECT permission facilitates data querying but does not override masking, failing to meet the objective of allowing access to unmasked data.

Explore dynamic data masking - Training | Microsoft Learn
Dynamic data masking in Fabric data warehousing - Training | Microsoft Learn

Question 11 of 50
Your company is using Microsoft Fabric to manage a data warehouse that contains a table with sensitive employee information.

The table contains columns such as EmployeeID, Name, Salary, and SocialSecurityNumber.

You need to restrict access to the Salary and SocialSecurityNumber columns to HR personnel only.

Which three actions should you perform? Each correct answer presents part of the solution.

Your Answer
Create an HR role and assign it to HR personnel.

This answer is correct.
Deny SELECT permission on the sensitive columns to other roles.

This answer is correct.
Grant SELECT permission on the sensitive columns to the HR role.

This answer is correct.
Correct Answer
Create an HR role and assign it to HR personnel.

This answer is correct.
Deny SELECT permission on the sensitive columns to other roles.

This answer is correct.
Grant SELECT permission on the sensitive columns to the HR role.

This answer is correct.
Creating an HR role and granting it SELECT permission on the sensitive columns ensures that only HR personnel can access the Salary and SocialSecurityNumber data. Denying SELECT permission to all other roles further secures the data by preventing unauthorized access. Creating a view is not appropriate for this scenario, as it does not provide the required column-level access control.

Security for data warehousing in Microsoft Fabric - Training | Microsoft Learn
SQL granular permissions in Microsoft Fabric - Training | Microsoft Learn

Question 12 of 50
Your company has a data warehouse in Microsoft Fabric to store sales data.

Different departments need access to the data, but each department should only see data relevant to their operations.

You need to configure the data warehouse so that each department can only view its own sales data.

Which two actions should you perform? Each correct answer presents part of the solution.

Your Answer
Create a security policy with a filter predicate for departments.

This answer is correct.
Implement row-level security using department identifiers.

This answer is correct.
Correct Answer
Create a security policy with a filter predicate for departments.

This answer is correct.
Implement row-level security using department identifiers.

This answer is correct.
Creating a security policy with a filter predicate and implementing row-level security using department identifiers ensures that each department can only access its own sales data. Column-level security controls access to specific columns within a table, not specific rows, and does not provide the granularity needed for department-specific access.

Row-level security in Fabric data warehousing - Training | Microsoft Learn

Question 13 of 50
Your organization uses Microsoft Fabric to manage a data warehouse that contains sensitive customer information.

You need to prevent nonprivileged users from viewing full email addresses and credit card numbers.

Which two actions should you perform? Each correct answer presents part of the solution.

Your Answer
Use dynamic data masking on CreditCardNumber with partial() function.

This answer is correct.
Use dynamic data masking on Email with email() function.

This answer is correct.
Correct Answer
Use dynamic data masking on CreditCardNumber with partial() function.

This answer is correct.
Use dynamic data masking on Email with email() function.

This answer is correct.
Implementing dynamic data masking on the Email and CreditCardNumber columns ensures that nonprivileged users can access the data without seeing sensitive information. Row-level security controls access to specific rows, which might seem like a way to protect sensitive data but does not mask it.

Dynamic data masking - Training | Microsoft Learn

Question 14 of 50
Your company uses Dynamic Data Masking (DDM) in its Microsoft Fabric SQL database to protect sensitive customer information, including Email, PhoneNumber, and CreditCardNumber fields.

You need to configure DDM so nonprivileged users see masked versions of these fields.

Which masking function should you apply to the CreditCardNumber field?

Your Answer
partial(0,"XXXX-XXXX-XXXX-",4)

This answer is correct.
Correct Answer
partial(0,"XXXX-XXXX-XXXX-",4)

This answer is correct.
Applying the 'partial(0,"XXXX-XXXX-XXXX-",4)' function is the most appropriate choice for masking credit card numbers, as it allows specific parts of the data to be visible while masking the rest. The 'default()' function would hide all data, which is not desired here. The 'email()' function is inappropriate for credit card numbers, and the 'random()' function is not suitable as it replaces them with random values.

Explore dynamic data masking - Training | Microsoft Learn

Question 15 of 50
Your company implements a new data analytics solution using Microsoft Fabric.

You need to design an orchestration pattern that minimizes manual intervention and supports dynamic data loading into a lakehouse.

Which approach should you recommend?

Your Answer
Implement a Data Factory pipeline with parameters and dynamic expressions.

This answer is correct.
Correct Answer
Implement a Data Factory pipeline with parameters and dynamic expressions.

This answer is correct.
Implementing a Data Factory pipeline with parameters and dynamic expressions automates data loading, reduces manual intervention, and supports dynamic data handling. Using a static configuration lacks flexibility, while using a single notebook without parameters lacks flexibility. Creating individual pipelines for each data source increases complexity and maintenance.
https://learn.microsoft.com/en-us/fabric/data-factory/parameters

Question 16 of 50
Your organization uses Microsoft Fabric to manage data pipelines for various ETL processes.

You need to create a flexible and reusable pipeline that handles different datasets by using parameters and expressions.

What should you do?

Your Answer
Use parameters and string interpolation for dynamic content.

This answer is correct.
Correct Answer
Use parameters and string interpolation for dynamic content.

This answer is correct.
Using parameters and string interpolation in the pipeline provides the necessary flexibility and reusability for handling different datasets. Creating separate pipelines for each dataset increases maintenance overhead, while hardcoding dataset values and using static expressions make the pipeline inflexible. Relying solely on default values does not offer the required flexibility for dynamic dataset handling.

Parameters for Data Factory in Microsoft Fabric - Training | Microsoft Learn

Question 17 of 50
Your organization uses Microsoft Fabric for managing data pipelines in a large-scale ETL process. The current setup involves multiple pipelines triggered by specific events and schedules, facing challenges with hard-coded values.

You need to implement dynamic parameterization to enhance flexibility and reduce maintenance.

Which two settings should you configure? Each correct answer presents part of the solution.

Your Answer
Pass external values using pipeline parameters.

This answer is correct.
Use dynamic expressions for runtime evaluation.

This answer is correct.
Correct Answer
Pass external values using pipeline parameters.

This answer is correct.
Use dynamic expressions for runtime evaluation.

This answer is correct.
Hard-coding values in the configuration contradicts the goal of reducing maintenance overhead and increasing flexibility. Using dynamic expressions for runtime evaluation allows parameter values to be evaluated at runtime, providing the flexibility needed to adapt to different scenarios without changing the pipeline code. Using static values in expressions does not provide the flexibility needed for dynamic parameterization. Using static triggers for pipeline execution does not provide the flexibility required for dynamic parameterization. Passing external values using pipeline parameters allows you to pass external values into the pipelines, making them more flexible and reducing the need for hard-coded values.

Load data using T-SQL - Training | Microsoft Learn
Parameters for Data Factory in Microsoft Fabric - Training | Microsoft Learn

Question 18 of 50
You have a Fabric workspace named Workspace1 that contains a lakehouse.

You create a pipeline in Workspace1 and add a Copy Data activity to the pipeline.

What is the purpose of the Copy Data activity?

Your Answer
to copy data from a source to a destination

This answer is correct.
Correct Answer
to copy data from a source to a destination

This answer is correct.
Copy Data moves data from source to destination with basic mapping; transformations require Dataflow Gen2 or notebooks; running notebooks or SQL scripts uses different pipeline activities.

Use the Copy Data activity

Question 19 of 50
You have a Fabric workspace that contains a lakehouse named Lakehouse1.

You need to create a solution that loads data from a CSV file stored in Azure Data Lake Storage Gen2 into Lakehouse1. The solution must be interactive and support collaboration.

Which type of item should you create?

Your Answer
a notebook

This answer is correct.
Correct Answer
a notebook

This answer is correct.
Notebooks are interactive and collaborative; pipelines/dataflows are geared to repeatable orchestration/prep; Spark job definitions are non-interactive production workloads.

Describe Microsoft Fabric Real-Time Intelligence?

Explore notebooks

Question 20 of 50
You have a pipeline in a Fabric workspace.

You need to configure the pipeline to run automatically once per day.

Which type of trigger should you use?

Your Answer
schedule

This answer is correct.
Correct Answer
schedule

This answer is correct.
Schedule triggers run pipelines on a defined cadence (daily/hourly); custom events trigger on specific events, tumbling windows are interval-based but not simply “once per day”, and storage events react to storage changes.

Run, schedule, or use events to trigger a pipeline

Question 21 of 50
Your company is implementing real-time data processing using Spark Structured Streaming in Microsoft Fabric. Data from IoT devices needs to be stored in a Delta table.

You need to ensure efficient processing of streaming data while preventing errors due to data changes.

What should you do?

Your Answer
Use ignoreChanges.

This answer is correct.
Correct Answer
Use ignoreChanges.

This answer is correct.
The ignoreChanges option ensures efficient processing by allowing the stream to handle data modifications without causing errors. Enabling overwrite mode would replace existing data, which contradicts the needs of a streaming solution that requires continuous data appending. Setting checkpointLocation to null would hinder stream state tracking, potentially leading to data loss and inefficiencies. Using the Append method would continuously add new data without addressing changes, leading to potential data duplication.

Use delta tables with streaming data - Training | Microsoft Learn

Question 22 of 50
Your company has set up a Microsoft Fabric lakehouse to store and analyze data from multiple sources, including Azure Event Hubs and local files. The data is used for generating Power BI reports.

You need to implement a loading pattern that supports both full and incremental data loads.

Which approach do you use?

Your Answer
Use Dataflows Gen2 for full and incremental data loads.

This answer is correct.
Correct Answer
Use Dataflows Gen2 for full and incremental data loads.

This answer is correct.
Using Dataflows Gen2 to implement both full and incremental data loads is the best approach, as it provides the necessary flexibility and efficiency for report generation. Developing a custom ETL tool is unnecessary when existing tools like Dataflows Gen2 can efficiently handle the task. Using Data Factory for incremental data loads might seem viable but does not address the need for both full and incremental data loads. Using Azure Synapse Analytics might seem like a viable option due to its capabilities in handling large-scale data processing, but it does not specifically address the need for both full and incremental data loads in a Microsoft Fabric lakehouse environment.

Get started with lakehouses in Microsoft Fabric - Training | Microsoft Learn

Question 23 of 50
Your company experiences performance issues with its current ETL process, which involves loading large volumes of sales data into a fact table in a Microsoft Fabric data warehouse. The process currently uses a full reload strategy, which is time-consuming and resource-intensive.

You need to enhance the ETL process to boost performance and decrease resource usage.

Which two actions should you perform? Each correct answer presents part of the solution.

Your Answer
Implement an incremental load strategy.

This answer is correct.
Use Change Data Capture (CDC) for tracking changes.

This answer is correct.
Correct Answer
Implement an incremental load strategy.

This answer is correct.
Use Change Data Capture (CDC) for tracking changes.

This answer is correct.
Implementing an incremental load strategy is effective because it reduces the amount of data processed during each ETL run, improving performance and reducing resource usage. Using Change Data Capture (CDC) for tracking changes is also beneficial as it allows tracking of changes in the source system, enabling efficient incremental loading of only the modified data into the fact table. Continuing full reloads with increased compute resources may temporarily alleviate performance issues but does not address the inefficiencies of a full reload strategy. Manually partitioning the fact table can improve query performance but does not directly address the inefficiencies in the ETL process itself. Switching to Azure Data Factory for ETL without addressing the full reload strategy may not improve performance.

Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn
Prepare data for analysis and reporting - Training | Microsoft Learn

Question 24 of 50
Your company uses a Microsoft Fabric data warehouse to store frequently updated customer transaction data.

You need to design an ETL process that minimizes load on source systems while ensuring only new or changed data is loaded.

What should you include in your design?

Your Answer
Use Change Data Capture (CDC) for tracking source data changes.

This answer is correct.
Correct Answer
Use Change Data Capture (CDC) for tracking source data changes.

This answer is correct.
Using Change Data Capture (CDC) is the most efficient method for tracking changes in the source data, allowing only new or changed data to be loaded into the warehouse, thus minimizing the load on the source systems. Performing a full data load every night is inefficient and places unnecessary load on the source systems, making it unsuitable for frequent updates. Using a timestamp column for incremental data loading may not capture all changes as effectively as CDC, particularly in complex scenarios. Implementing a trigger-based change detection can introduce complexity and may not efficiently handle large volumes of data changes, making it less effective for this scenario.

Dimensional modeling in Microsoft Fabric Warehouse: Load tables - Training | Microsoft Learn

Question 25 of 50
You are implementing a data warehouse solution using Microsoft Fabric.

The data warehouse integrates data from multiple sources, including Microsoft Azure Data Lake Storage Gen2 and Microsoft SQL Server databases.

You need to recommend an ETL process that efficiently transforms and loads the data into dimensional model tables for reporting purposes.

Which three actions should you recommend? Each correct answer presents part of the solution.

Your Answer
Stage data before loading.

This answer is correct.
Transform data to match the model.

This answer is correct.
Use Data Factory pipelines.

This answer is correct.
Correct Answer
Stage data before loading.

This answer is correct.
Transform data to match the model.

This answer is correct.
Use Data Factory pipelines.

This answer is correct.
Using Microsoft Data Factory pipelines to orchestrate the ETL process is essential for managing complex workflows and ensuring efficient data integration. Staging source data in staging tables helps minimize the impact on operational systems and supports data transformation, which is crucial for maintaining data quality. Transforming source data to align with the dimensional model's structure ensures that the data is cleansed and conforms to the required format, supporting accurate reporting. Loading data directly from source systems without staging can lead to data quality issues, making it an incorrect choice. Using a basic ETL tool without automation features is inefficient compared to advanced ETL tools. Proceeding without verifying data quality can result in low-quality data being loaded, leading to inaccurate reports.

Dimensional modeling in Microsoft Fabric Warehouse: Load tables - Training | Microsoft Learn

Question 26 of 50
You have a Fabric lakehouse named Lakehouse1 that contains a table named Sales. Sales contains the following columns:

OrderID (INT)
OrderDate (DATE)
ProductID (INT)
Quantity (INT)
You plan to implement incremental loads of new sales records from a CSV file located in the /files/sales/ folder of Lakehouse1.

You need to identify a querying solution for the incremental loads. The solution must minimize maintenance effort.

What should you use?

Your Answer
a pipeline

This answer is incorrect.
Correct Answer
a notebook

This answer is correct.
Notebooks provide flexible, code-based incremental load patterns for Fabric lakehouses; Auto Loader is not available in Fabric, stored procedures aren’t a lakehouse querying solution, and pipelines are orchestration—not querying.

Options to get data into the Fabric Lakehouse

Question 27 of 50
You have a Fabric eventhouse that contains a KQL database named DB1.

You ingest data into DB1 from multiple sources.

You need to transform the data during ingestion. The solution must minimize development effort.

What should you use?

Your Answer
KQL

This answer is correct.
Correct Answer
KQL

This answer is correct.
KQL supports ingest-time transformations via update policies; T-SQL targets warehouses, notebooks require authoring/orchestration, and dataflows are for batch preparation into lakehouses/warehouses.

Choose an analytical data store in Microsoft Fabric

Store and query real-time data

Question 28 of 50
Your organization uses Microsoft Fabric for data analytics. The SQL database mirrors data to OneLake.

You need to ensure mirrored data is consistent and accessible during SQL database downtime.

What should you do?

Your Answer
Use automatic mirroring in Microsoft Fabric.

This answer is correct.
Correct Answer
Use automatic mirroring in Microsoft Fabric.

This answer is correct.
Using automatic mirroring in Microsoft Fabric is the most effective solution because it ensures data replication resumes automatically after downtime, maintaining consistency and accessibility. Reconfiguring mirroring settings manually is unnecessary due to Microsoft Fabric's built-in capabilities. Setting up a secondary database for manual replication is redundant, and setting up a data integration pipeline with Azure Data Factory is not needed as Microsoft Fabric's mirroring already ensures data consistency and recovery.

What is Mirroring in Fabric? - Training | Microsoft Learn

Question 29 of 50
Your company has multiple data sources, including Azure Databricks and Azure Cosmos DB.

You plan to integrate the data sources into Microsoft Fabric for unified analytics.

You need to choose the appropriate type of mirroring for each data source to ensure efficient data integration.

Which types of mirroring should you use for Azure Databricks and Azure Cosmos DB?

Your Answer
Metadata mirroring for Databricks, database mirroring for Cosmos DB.

This answer is correct.
Correct Answer
Metadata mirroring for Databricks, database mirroring for Cosmos DB.

This answer is correct.
For efficient data integration into Microsoft Fabric, using metadata mirroring for Azure Databricks is ideal as it allows synchronization of metadata without transferring actual data, aligning with the needs of Databricks. On the other hand, database mirroring is necessary for Azure Cosmos DB to ensure complete data replication, which is crucial for maintaining data integrity across systems. Database mirroring for both would lead to unnecessary data movement for Databricks, while metadata mirroring for both would fail to replicate the necessary data for Cosmos DB.

What is Mirroring in Fabric? - Training | Microsoft Learn

Question 30 of 50
You are using Microsoft Fabric to manage data ingestion and transformation.

You need to set up a data pipeline to ingest batch data from multiple CSV files stored in Azure Blob Storage. The solution must ensure the process is efficient and handles errors effectively.

Which three actions should you perform? Each correct answer presents part of the solution.

Your Answer
Transform data with Azure Data Lake Storage Gen2 before ingestion.

This answer is incorrect.
Use the COPY statement to load data.

This answer is correct.
Use wildcards in the path to load multiple files.

This answer is correct.
Correct Answer
Specify a location for rejected rows.

This answer is correct.
Use the COPY statement to load data.

This answer is correct.
Use wildcards in the path to load multiple files.

This answer is correct.
To achieve efficient data ingestion and effective error handling, it is crucial to use the COPY statement, specify a REJECTED_ROW_LOCATION, and use wildcards. The COPY statement is optimal for loading data from Microsoft Azure Blob Storage, ensuring efficiency. Specifying a REJECTED_ROW_LOCATION enhances error management by isolating problematic rows for further analysis. Using wildcards allows for the bulk loading of multiple files, streamlining the process. Transforming data with Power BI or Azure Data Lake Storage Gen2 before ingestion adds unnecessary complexity when the focus is on efficient ingestion using the COPY statement.

Load data using T-SQL - Training | Microsoft Learn

Question 31 of 50
You use Microsoft Fabric to manage data across warehouses and lakehouses.

You need to integrate data from a warehouse and a lakehouse into a single table for analysis. The solution must minimize development effort.

What should you use?

Your Answer
The CREATE TABLE AS SELECT (CTAS) statement.

This answer is correct.
Correct Answer
The CREATE TABLE AS SELECT (CTAS) statement.

This answer is correct.
The CREATE TABLE AS SELECT (CTAS) statement is the best choice for integrating data from a warehouse and a lakehouse into a single table, as it allows the creation of a new table based on combined data. Dataflow Gen2, while useful for data preparation and transformation, does not directly support creating new tables from combined data sources. The SELECT INTO statement can create a new table but is not suitable for integrating data from multiple sources. Azure Data Factory is a data integration service that might seem suitable for integrating data from multiple sources, but it does not directly support creating tables from combined data sources in a warehouse or lakehouse.

Load data using T-SQL - Training | Microsoft Learn

Question 32 of 50
You use Microsoft Fabric to manage data across cloud platforms.

You plan to ingest batch data from Azure Blob Storage into a warehouse.

You need to determine the most efficient method to import this data using Microsoft Fabric tools.

What should you use?

Your Answer
COPY statement with Shared Access Signature.

This answer is correct.
Correct Answer
COPY statement with Shared Access Signature.

This answer is correct.
The COPY statement with Shared Access Signature efficiently ingests batch data from Azure Blob Storage into a warehouse due to its direct and secure data transfer capabilities. In contrast, a Data Factory pipeline requires manual configuration, making it less efficient. Dataflows Gen2 focus on data preparation and transformation, which does not align with the task of batch data ingestion. Azure Synapse Analytics is not designed for efficient batch data ingestion using Microsoft Fabric tools.

Load data using T-SQL - Training | Microsoft Learn

Question 33 of 50
Your organization uses Microsoft Fabric to process real-time data from IoT devices.

You need to implement a solution for ingesting and transforming streaming data without writing code.

What should you do?

Your Answer
Use the eventstreams feature in Microsoft Fabric with enhanced capabilities.

This answer is correct.
Correct Answer
Use the eventstreams feature in Microsoft Fabric with enhanced capabilities.

This answer is correct.
Using the eventstreams feature in Microsoft Fabric with enhanced capabilities enabled is the correct choice because it provides a no-code solution for ingesting and transforming streaming data, meeting the requirements of the scenario. Using Azure Stream Analytics requires setting up queries, which does not satisfy the no-code requirement. Using Azure Event Hubs requires coding for data transformation, making it unsuitable for the no-code requirement. Using Microsoft Spark Structured Streaming with PySpark scripts also involves coding, making it unsuitable for the no-code requirement.

Fabric Eventstream - overview - Training | Microsoft Learn

Question 34 of 50
You process streaming data from various sources using Microsoft Fabric, requiring transformation and storage in a lakehouse for analytics.

You need to select a method for effective transformation and storage of streaming data.

Which method should you choose?

Your Answer
Spark Structured Streaming with Delta tables.

This answer is correct.
Correct Answer
Spark Structured Streaming with Delta tables.

This answer is correct.
Spark Structured Streaming with Delta tables is the most effective method for transforming and storing streaming data in real-time, utilizing Delta Lake's features for ACID transactions and scalability. Azure Stream Analytics is not suitable as it focuses on real-time processing rather than batch processing. Azure Data Factory lacks the necessary real-time processing capabilities, making it more appropriate for batch integrations. Azure Synapse Analytics, while powerful, is not specifically designed for real-time streaming data transformation and storage in a lakehouse, rendering it an inappropriate choice for this scenario.

Use delta tables with streaming data - Training | Microsoft Learn
Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn

Question 35 of 50
Your company is using Microsoft Fabric to manage and analyze large volumes of streaming data from various sources.

You need to implement a solution that filters out invalid data and adds calculated fields before storing it in a lakehouse.

Which three actions should you perform? Each correct answer presents part of the solution.

Your Answer
Add calculated columns using Spark SQL expressions.

This answer is correct.
Use Spark Structured Streaming to read the data stream.

This answer is correct.
Correct Answer
Add calculated columns using Spark SQL expressions.

This answer is correct.
Filter out rows with NULL values in critical columns.

This answer is correct.
Use Spark Structured Streaming to read the data stream.

This answer is correct.
Using Microsoft Spark Structured Streaming to read the data stream into a DataFrame is the first step in processing and transforming the data. Filtering out rows with NULL values ensures that only valid data is processed and stored, improving data quality. Adding calculated columns enriches the data stream with additional information, which can be useful for downstream analytics. Using a CSV file for batch processing does not meet the requirement for real-time processing and transformation. Batch processing frameworks are not suitable for real-time data transformations as they do not support continuous data flow.

Use delta tables with streaming data - Training | Microsoft Learn
Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn

Question 36 of 50
Your organization uses Microsoft Fabric for data analytics workflows.

There are delays in processing due to inefficient monitoring of data ingestion and transformation.

You need to implement a solution for effective monitoring of data workflows.

What should you do?

Your Answer
Configure alerts in the Microsoft Real-Time hub.

This answer is correct.
Correct Answer
Configure alerts in the Microsoft Real-Time hub.

This answer is correct.
Configuring alerts in the Microsoft Real-Time hub is the most effective solution because it provides real-time monitoring and alerting capabilities for data ingestion and transformation processes, directly addressing the organization's needs. Creating a Power BI dashboard, while useful for visualization, lacks the necessary real-time alerting functionality. Storing data events in a data lake is insufficient as it does not offer immediate notifications required for timely responses. Using Azure Monitor is not ideal as it does not specifically target Microsoft Fabric workspace events, making it less effective for this scenario.

Set alerts on Fabric workspace item events in Real-Time hub - Training | Microsoft Learn
Set alerts based on Fabric events in Real-Time hub - Training | Microsoft Learn

Question 37 of 50
Your organization uses Microsoft Fabric to manage and analyze large datasets.

Recently, issues with data ingestion processes fail intermittently, causing delays in data availability for analysis.

You need to implement a strategy to detect patterns or recurring issues in data ingestion activities.

Which two actions should you perform? Each correct answer presents part of the solution.

Your Answer
Configure alerts for future ingestion failures.

This answer is correct.
Filter activities by status to identify failures.

This answer is correct.
Correct Answer
Configure alerts for future ingestion failures.

This answer is correct.
Filter activities by status to identify failures.

This answer is correct.
Configuring alerts for future ingestion failures ensures immediate notification and timely intervention, making it a proactive monitoring approach. Filtering activities by status in the Monitor hub allows for quick identification of failed ingestion processes, directly addressing the need to monitor and resolve issues. Analyzing error logs might seem useful for identifying patterns, but it does not address the immediate need to monitor and resolve failures effectively. Removing all filters could lead to information overload, making it difficult to focus on specific failed activities.

Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn
Prepare data for analysis and reporting - Training | Microsoft Learn

Question 38 of 50
Your organization uses Microsoft Fabric to manage and monitor various data activities, including data pipelines, dataflows, and semantic models.

Recently, there have been issues with delayed data ingestion and transformation processes.

You need to identify and resolve the causes of these delays to improve data processing efficiency.

Which two actions should you perform? Each correct answer presents part of the solution.

Your Answer
Filter activities by status and start time.

This answer is correct.
Set up alerts for data process delays.

This answer is correct.
Correct Answer
Filter activities by status and start time.

This answer is correct.
Set up alerts for data process delays.

This answer is correct.
Setting up alerts for data process delays is crucial as it provides immediate notifications, allowing for proactive management and timely resolution of issues. Filtering activities by status and start time in the Monitor hub enables identification of specific delayed processes, facilitating targeted troubleshooting. Optimizing data transformation processes can improve efficiency but may not address the core issue if the delays are caused by other factors. Increasing data storage capacity without understanding the root cause of delays may not solve the problem and could lead to unnecessary costs.

Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn
Prepare data for analysis and reporting - Training | Microsoft Learn

Question 39 of 50
You have a Fabric workspace named Workspace1.

In Workspace1, you create a lakehouse named Lakehouse1.

You plan to ingest data into Lakehouse1.

You need to monitor the data ingestion process.

What should you use?

Your Answer
Monitor hub/>

This answer is correct.
Correct Answer
Monitor hub/>

This answer is correct.
Monitor hub tracks ingestion and transformation activities; query insights target data warehouse queries, and capacity metrics focus on capacity usage rather than ingestion details.

Introduction

Question 40 of 50
Your organization uses Microsoft Fabric for data workflows.

You notice that some data transformations are not completing, causing delays.

You need to ensure that you receive immediate alerts for data processing issues.

What should you do?

Your Answer
Set up notifications for transformation events in Microsoft Fabric.

This answer is correct.
Correct Answer
Set up notifications for transformation events in Microsoft Fabric.

This answer is correct.
Setting up notifications for transformation events in Microsoft Fabric is the most effective solution as it provides immediate alerts, allowing quick response to issues. Increasing data refresh frequency does not address underlying transformation issues and leads to additional resource consumption. Setting up a weekly report for transformation logs lacks the real-time aspect needed for prompt action, and setting up a dashboard in Power BI provides insights but does not offer real-time alerts for immediate action.

Set alerts on Fabric workspace item events in Real-Time hub - Training | Microsoft Learn

Question 41 of 50
You have a Dataflow Gen2 dataflow in Fabric that uses an on-premises data gateway.

You discover that a refresh fails after running for approximately one hour.

You need to troubleshoot the cause of the failure.

What should you do first?

Your Answer
Verify the version of the on-premises data gateway.

This answer is correct.
Correct Answer
Verify the version of the on-premises data gateway.

This answer is correct.
Gateway version issues commonly cause long-running refresh failures; pipeline timeouts, queued runs, and parameter limits relate to pipelines, not Dataflows Gen2 refresh via gateway.

Data Factory limitations overview

Question 42 of 50
Your company has implemented a SQL database in Microsoft Fabric to handle large-scale data analytics.

Users report slow query performance during peak hours.

You need to implement a solution that optimizes query performance automatically without manual intervention.

What should you do?

Your Answer
Enable automatic tuning.

This answer is correct.
Correct Answer
Enable automatic tuning.

This answer is correct.
Enabling automatic tuning allows the system to adapt to workload changes and optimize query performance without manual intervention. Enabling query caching might seem beneficial but does not directly optimize query execution automatically. Enabling manual index management requires ongoing oversight and does not align with the goal of optimization without manual intervention. Enabling resource governance policies can help manage resources and improve performance indirectly but does not directly optimize query performance automatically without manual intervention.

Configure SQL granular permissions using T-SQL - Training | Microsoft Learn

Question 43 of 50
Your organization uses Microsoft Fabric to manage data pipelines for processing sales data.

Recently, a pipeline failed during execution, and the error logs indicate a missing data source in one of the Lookup activities.

You need to configure the pipeline to fail gracefully with a clear error message when such issues occur in the future.

What should you do?

Your Answer
Add a Fail activity with a custom error message and code.

This answer is correct.
Correct Answer
Add a Fail activity with a custom error message and code.

This answer is correct.
Adding a Fail activity with a custom error message and error code ensures the pipeline fails gracefully, meeting the requirement. Adding a conditional check to handle missing data sources does not ensure the pipeline fails with a clear error message when the data source is missing. Automatically retrying the pipeline does not address the requirement to fail the pipeline with a clear error message. Logging errors without failing the pipeline does not meet the requirement to stop execution with a clear error message.

Use the Fail activity to cause pipeline execution to fail with a customized error message and error code - Training | Microsoft Learn

Question 44 of 50
You have a Fabric eventhouse named Eventhouse1.

You discover that after 10 minutes of inactivity, Eventhouse1 automatically suspends and must be reactivated before you can query data.

You need to prevent Eventhouse1 from suspending due to inactivity. The solution must minimize administrative effort and prevent the eventhouse from having to be reactivated manually.

What should you do?

Your Answer
Enable Always-On for Eventhouse1.
This answer is correct.
Correct Answer
Enable Always-On for Eventhouse1.
This answer is correct.
An Eventhouse in Microsoft Fabric will automatically suspend after 10 minutes of inactivity unless Always-On is enabled. To prevent suspension and avoid manually reactivating the compute, you must configure the Always-On setting for the eventhouse. In the Fabric UI, this is done from the Eventhouse ribbon by selecting Always-On, and then choosing the appropriate consumption mode. Selecting Minimum consumption ensures the eventhouse stays active while consuming the lowest amount of resources, minimizing administrative effort and controlling cost. Therefore, enabling Always-On and explicitly selecting Minimum consumption is the correct solution because it prevents automatic suspension while maintaining low-cost continuous availability.

Eventhouse overview
Manage and monitor an eventhouse

Question 45 of 50
You have a table named dbo.Customers.

You run the following code.

BEGIN TRY

  INSERT INTO dbo.Customers (FirstName, LastName)

  VALUES (N'Jeff', N'Price');

  COMMIT TRANSACTION;

END TRY

BEGIN CATCH

  SELECT ERROR_NUMBER() AS ErrorNumber, ERROR_MESSAGE() AS ErrorMessage;

  ROLLBACK TRANSACTION;

END CATCH;

Users report that the code fails to insert data into the Customers table.

You need to ensure that the code runs successfully and in a transaction. The solution must continue to handle exceptions.

What should you do?

Your Answer
Add a BEGIN TRANSACTION statement to the TRY block.

This answer is correct.
Correct Answer
Add a BEGIN TRANSACTION statement to the TRY block.

This answer is correct.
Adding a BEGIN TRANSACTION at the start of the TRY block ensures that the INSERT executes inside an explicit transaction and allows COMMIT TRANSACTION to succeed when no errors occur. The code currently attempts to commit a transaction that was never started, so the insert silently fails. Moving the COMMIT statement to the CATCH block is incorrect because COMMIT should only occur when no exception is thrown, and the CATCH block should handle rollbacks rather than commits. Removing the COMMIT statement would leave an open transaction and violate proper transaction handling, while removing the ROLLBACK would break error handling by preventing cleanup when an exception occurs.

Implement structured exception handling

RAISERROR (Transact-SQL)

Handle errors in transactions

Question 46 of 50
Your company has an eventstream using Microsoft Fabric to process real-time data from various sources.

You notice that frequent runtime errors affect data processing.

You need to ensure smooth data processing by identifying and resolving runtime errors.

Which three actions should be perform? Each correct answer presents part of the solution.

Your Answer
Check Data insights for event metrics.

This answer is correct.
Filter logs by error severity.

This answer is correct.
Review Runtime logs for error details.

This answer is correct.
Correct Answer
Check Data insights for event metrics.

This answer is correct.
Filter logs by error severity.

This answer is correct.
Review Runtime logs for error details.

This answer is correct.
Reviewing Runtime logs provides detailed error information, essential for diagnosing issues. Checking Data insights helps identify performance bottlenecks or issues. Filtering logs by severity allows prioritization of critical errors, ensuring they are addressed promptly. Modifying data transformation logic might seem like a way to address errors, but it does not resolve the actual problem. Increasing the eventstream node count does not directly address the root cause of runtime errors.

Monitoring status and performance of an eventstream - Training | Microsoft Learn

Question 47 of 50
Your company uses Microsoft Fabric to manage data pipelines for a large-scale analytics solution.

You notice that several pipeline executions failed due to errors in the Lookup activity, which returned no matching data.

You need to configure the pipeline to terminate with specific error details when the Lookup activity returns no matching data.

Which two actions should you perform? Each correct answer presents part of the solution.

Your Answer
Add a Fail activity after the Lookup activity.

This answer is correct.
Configure the Fail activity with specific error details.

This answer is correct.
Correct Answer
Add a Fail activity after the Lookup activity.

This answer is correct.
Configure the Fail activity with specific error details.

This answer is correct.
Adding a Fail activity after the Lookup activity is essential because it allows the pipeline to terminate with a specific error message and code, directly addressing the requirement. Configuring this Fail activity with detailed error information ensures that the pipeline provides clear feedback when it fails. Adding a Wait activity does not address the need for customized error termination. Using a Retry activity might seem like a way to handle errors but does not fulfill the requirement to fail the pipeline with specific error details.

Use the Fail activity to cause pipeline execution to fail with a customized error message and error code - Training | Microsoft Learn

Question 48 of 50
Your company is using Microsoft Fabric to manage data pipelines for a lakehouse solution.

You notice that a pipeline failed due to a script activity error.

You need to ensure that the pipeline execution fails with a customized error message and code.

Which two actions should you perform? Each correct answer presents part of the solution.

Your Answer
Add a Fail activity.

This answer is correct.
Configure custom error settings in the Fail activity.

This answer is correct.
Correct Answer
Add a Fail activity.

This answer is correct.
Configure custom error settings in the Fail activity.

This answer is correct.
To ensure that a pipeline reports a custom error message and code when a script activity fails, adding a Fail activity to the pipeline and configuring its settings with the desired error message and code are essential steps. The Fail activity is specifically designed for this purpose, making these actions correct. Using a Try-Catch activity is a common misconception as it is not applicable in this context, and enabling logging does not address the error reporting requirement, making them incorrect choices.

Use the Fail activity to cause pipeline execution to fail with a customized error message and error code - Training | Microsoft Learn

Question 49 of 50
Your company uses Microsoft Fabric to manage large-scale data processing tasks.

You notice performance issues with Spark jobs involving complex transformations and aggregations on Delta format data.

You need to enhance performance of these Spark jobs without modifying the existing codebase.

What should you do?

Your Answer
Enable native execution engine.

This answer is correct.
Correct Answer
Enable native execution engine.

This answer is correct.
Enabling native execution engine in environment settings optimizes performance for complex Spark jobs without code modifications. Enabling dynamic allocation can lead to resource inefficiencies and does not directly enhance performance for complex transformations and aggregations. Enabling high concurrency mode allows multiple users to share Spark sessions, but it does not directly enhance performance for complex transformations and aggregations. Enabling adaptive query execution is a common consideration for optimizing Spark job performance, but it does not directly address the specific performance issues related to complex transformations and aggregations on Delta format data.

Load data using T-SQL - Training | Microsoft Learn

Question 50 of 50
Your company uses Microsoft Fabric Lakehouse to store and analyze large datasets.

You notice increased storage costs due to old files that are no longer needed for current operations.

You need to reduce storage costs by removing unnecessary files while maintaining data integrity.

What should you do?

Your Answer
Use VACUUM command.

This answer is correct.
Correct Answer
Use VACUUM command.

This answer is correct.
The VACUUM command effectively removes unreferenced files older than the retention threshold, reducing storage costs while maintaining data integrity. Enabling V-Order compression optimizes file compression and read performance but does not remove unnecessary files. Reducing the file retention period might seem like a cost-saving measure but can compromise data integrity and affect Delta's time travel capabilities. Using the OPTIMIZE command consolidates files for performance but does not remove unnecessary files, which is needed to reduce storage costs.

Use table maintenance feature to manage delta tables in Fabric - Training | Microsoft Learn

