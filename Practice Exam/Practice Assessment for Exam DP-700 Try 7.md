It took you 26 minutes to complete this assessment.

Overall Results
To be better prepared for the exam, aim to achieve a score of 80% or higher in multiple attempts.

Score: 96%

Performance by assessment section
To further strengthen your skills in the following areas, refer to the Customized Learning Material section below.

Implement and manage an analytics solution - passed with 98%

Ingest and transform data - passed with 98%

Monitor and optimize an analytics solution - passed with 100%

Answer Summary
Below is a summary of your answers.

Question 1 of 50
Your company is transitioning to a data mesh architecture using Microsoft Fabric.

You are responsible for organizing data into domains.

You need to configure settings for independent management of rules and restrictions by each business unit.

What should you do?

Your Answer
Delegate tenant-level settings to domains.

This answer is correct.
Correct Answer
Delegate tenant-level settings to domains.

This answer is correct.
Delegating tenant-level settings to the domain level allows each business unit to manage its own governance settings, which is essential for implementing a data mesh architecture. Assigning workspaces to multiple domains complicates governance and does not support independent management. Creating workspaces with shared governance settings centralizes control and does not facilitate domain-specific governance. Configuring domain-specific sensitivity labels is related to governance but does not address the need for independent management of rules and restrictions by each business unit.

Prepare to use Apache Spark - Training | Microsoft Learn
Implement row-level security - Training | Microsoft Learn

Question 2 of 50
Your company uses Microsoft Fabric to manage data engineering workloads.

You notice performance issues with Spark jobs due to inefficient resource allocation.

You need to optimize the Spark pool configuration to improve performance and reduce costs.

Which three actions should you perform? Each correct answer presents part of the solution.

Your Answer
Configure dynamic allocation for executors.

This answer is correct.
Enable autoscale for node provisioning.

This answer is correct.
Use compute-optimized nodes.

This answer is incorrect.
Correct Answer
Configure dynamic allocation for executors.

This answer is correct.
Enable autoscale for node provisioning.

This answer is correct.
Select memory-optimized nodes.

This answer is correct.
Configuring dynamic allocation for executors optimizes resource usage by adjusting executor processes according to data volume, enhancing performance and efficiency. Enabling autoscale for node provisioning allows the Spark pool to dynamically adjust the number of nodes based on workload demands, optimizing resource usage and cost. Selecting memory-optimized nodes provides better performance for data-intensive operations, which is critical for improving Spark job efficiency. Enabling fixed resource allocation does not address performance issues related to dynamic resource needs and could lead to inefficient resource usage. Using static node allocation lacks flexibility in resource allocation, necessary for handling varying workloads efficiently. Using compute-optimized nodes may seem beneficial for performance but are not ideal for data-intensive Spark jobs compared to memory-optimized nodes.

Prepare to use Apache Spark | Microsoft Learn

Question 3 of 50
Your organization uses Microsoft Fabric to manage data engineering tasks. The current setup includes a starter pool for Apache Spark jobs.

You notice that some jobs require more compute resources than the starter pool can provide.

You need to optimize the workspace configuration to efficiently handle larger Spark jobs without significantly increasing session start times.

Which two actions should you perform? Each correct answer presents part of the solution.

Your Answer
Create a custom Spark pool with autoscaling.

This answer is correct.
Enable dynamic allocation of executors.

This answer is correct.
Correct Answer
Create a custom Spark pool with autoscaling.

This answer is correct.
Enable dynamic allocation of executors.

This answer is correct.
Creating a custom Spark pool with autoscaling allows for specifying node sizes and enabling dynamic resource allocation, which is essential for handling larger Spark jobs. Enabling dynamic allocation of executors further optimizes resource usage by adjusting the number of executors based on workload demands. Disabling the starter pool without a custom pool reduces available resources, while increasing executor memory in the starter pool lacks the dynamic aspect needed for efficient resource management. Increasing the number of partitions does not address the core issue of managing larger Spark jobs.

Prepare to use Apache Spark | Microsoft Learn

Question 4 of 50
Your organization uses Microsoft Fabric for data engineering.

You notice Microsoft Spark job failures due to incompatible library versions after updating a Spark runtime.

You need to resolve compatibility issues causing Microsoft Spark job failures.

Which two actions should you perform? Each correct answer presents part of the solution.

Your Answer
Republish environment after removing incompatible libraries.

This answer is correct.
Update library versions to match new Spark runtime.

This answer is correct.
Correct Answer
Republish environment after removing incompatible libraries.

This answer is correct.
Update library versions to match new Spark runtime.

This answer is correct.
To resolve compatibility issues causing Microsoft Spark job failures, it is essential to republish the environment after removing incompatible libraries. This ensures only compatible configurations are applied, preventing job failures. Additionally, updating library versions to match new Microsoft Spark runtime requirements is crucial as it aligns libraries with the updated runtime, ensuring all dependencies are met. Using an outdated library version does not resolve compatibility issues, and adjusting Spark executor memory settings does not solve incompatible libraries causing job failures. Reverting to a previous Spark runtime version might seem like a solution, but it does not address the root cause of library compatibility issues after an update.

Create, configure, and use an environment in Fabric | Microsoft Learn

Question 5 of 50
Your organization uses Microsoft Fabric for data engineering and runs Spark jobs requiring efficient resource utilization.

You need to optimize resource management in the Microsoft Spark environment based on workload demands.

What should you do?

Your Answer
Enable autoscaling

This answer is correct.
Correct Answer
Enable autoscaling

This answer is correct.
To optimize resource management in the Microsoft Spark environment, enabling autoscaling is the most effective solution. It allows the system to dynamically adjust the number of nodes based on workload demands, ensuring efficient resource utilization. Enabling fixed resource allocation would prevent necessary adjustments, contradicting the optimization goal. Setting a fixed number of nodes leads to inefficiencies as it lacks dynamic adjustment capabilities. Using a single node cluster restricts scalability and flexibility, failing to accommodate varying workloads effectively.

What is Apache Spark compute in Microsoft Fabric? - Training | Microsoft Learn
Data Engineering workspace administration settings in Microsoft Fabric - Training | Microsoft Learn

Question 6 of 50
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

Question 7 of 50
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

Question 8 of 50
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

Question 9 of 50
Your organization uses Microsoft Fabric deployment pipelines to manage analytics solutions across Development, Test, and Production stages.

You need to restrict editing of pipeline settings to authorized users only.

What should you do?

Your Answer
Assign pipeline admin roles.

This answer is correct.
Correct Answer
Assign pipeline admin roles.

This answer is correct.
To ensure that only authorized users can edit pipeline settings, assigning pipeline admin roles is essential. This approach maintains security and control over the deployment process. Configuring workspace permissions involves setting access levels for users within a workspace, but it does not specifically restrict editing of pipeline settings. Enabling stage-level security might seem like it restricts access, but it fails to limit editing permissions. Implementing role-based access control manages user permissions but does not specifically influence who can edit pipeline settings.

The deployment pipelines process - Training | Microsoft Learn
Get started with deployment pipelines - Training | Microsoft Learn

Question 10 of 50
You have a Fabric workspace named Workspace1 that contains two datasets named datasetA and datasetB.

You plan to use a deployment pipeline in Workspace1.

You create a pipeline named pipeline1 and add a development stage and a test stage. You assign Workspace1 to the Development stage of pipeline1. You create another workspace Workspace2.

What will occur when you assign Workspace2 to the test stage of pipeline1?

Your Answer
datasetA and datasetB will be copied to Workspace2.

This answer is correct.
Correct Answer
datasetA and datasetB will be copied to Workspace2.

This answer is correct.
Assigning a workspace to a downstream stage deploys items from the development workspace into it; the other options contradict pipeline behavior.

The deployment pipelines process
Implement deployment pipelines

Question 11 of 50
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

Question 12 of 50
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

Question 13 of 50
Your organization is using Microsoft Fabric to manage a data warehouse containing sensitive financial data, including columns such as AccountNumber, Balance, and TransactionHistory.

You need to ensure that only authorized finance team members can view the TransactionHistory column.

What should you use?

Your Answer
Column-Level Security

This answer is correct.
Correct Answer
Column-Level Security

This answer is correct.
Column-Level Security is essential for controlling access to specific columns, such as TransactionHistory, ensuring that only authorized users can view sensitive financial data. Data Encryption, while useful for securing data, does not offer the column-specific access control required in this scenario. Dynamic Data Masking obscures sensitive data but does not provide access control to specific columns. Row-Level Security manages permissions at a row level, lacking the necessary granularity for protecting individual columns.

Security for data warehousing in Microsoft Fabric - Training | Microsoft Learn

Question 14 of 50
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

Question 15 of 50
You have a Fabric workspace named Workspace1 that contains a lakehouse named Lakehouse1 and a user named User1.

User1 is assigned the Contributor workspace role for Workspace1.

You discover that User1 is consuming more resources than expected. You remove User1 from Workspace1. User1 now requires read-only access to the data in Lakehouse1.

You need to ensure that User1 can read the data in Lakehouse1. The solution must follow the principle of least privilege.

What should you do?

Your Answer
Configure item permissions for Lakehouse1.

This answer is correct.
Correct Answer
Configure item permissions for Lakehouse1.

This answer is correct.
Item-level permissions on Lakehouse1 grant access only to that item, adhering to least privilege; workspace roles (Viewer, Member, Contributor) grant broader access to all workspace items.

Configure workspace and item permissions

Question 16 of 50
Your company uses a lakehouse architecture with Microsoft Fabric for analytics. Data is ingested and transformed using Microsoft Data Factory pipelines and stored in Delta tables.

You need to enhance data transformation efficiency and reduce loading time.

What should you do?

Your Answer
Use session tags to reuse Spark sessions.

This answer is correct.
Correct Answer
Use session tags to reuse Spark sessions.

This answer is correct.
Using session tags to reuse existing Microsoft Spark sessions minimizes startup time and enhances the efficiency of data transformation processes. Configuring the Microsoft Spark pool to use more worker nodes might seem beneficial for handling more tasks but does not directly improve transformation efficiency. Switching to a different Spark runtime version does not inherently minimize transformation time compared to optimized Spark execution. Enabling Delta Lake optimization is more about data storage and management rather than transformation efficiency.

Transform data by running a notebook - Training | Microsoft Learn

Question 17 of 50
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

Question 18 of 50
Your organization uses Microsoft Azure Synapse Analytics to manage data pipelines. A new requirement has emerged to trigger a pipeline whenever a new file is uploaded to a specific folder in a Microsoft Azure Blob Storage account.

You need to implement a solution that triggers the pipeline upon file upload.

What should you do?

Your Answer
Create a storage event trigger for Blob created events in the folder.

This answer is correct.
Correct Answer
Create a storage event trigger for Blob created events in the folder.

This answer is correct.
Creating a storage event trigger for Blob created events in Microsoft Azure Synapse Analytics is the optimal solution because it leverages native integration with Microsoft Azure Event Grid to automatically trigger the pipeline upon file upload. Using an Azure Function introduces unnecessary complexity, while scheduling a daily pipeline run or using a Logic App fails to provide real-time triggering, making them inefficient solutions.

Create a trigger that runs a pipeline in response to a storage event - Training | Microsoft Learn

Question 19 of 50
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

Question 20 of 50
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

Question 21 of 50
Your company has implemented a Microsoft Fabric lakehouse to store and analyze data from multiple sources. The data is used for generating Microsoft Power BI reports and requires regular updates.

You need to ensure that the data in the Microsoft Fabric lakehouse is updated incrementally to reflect changes from the source systems.

Which method should you use?

Your Answer
Use Change Data Capture (CDC).

This answer is incorrect.
Correct Answer
Implement a watermark strategy.

This answer is correct.
Implementing a watermark strategy is the most efficient method for achieving incremental updates, as it tracks changes and ensures only new or modified data is loaded. Using batch processing for updates is not suitable for incremental updates as it processes data in large chunks rather than focusing on recent changes. Using a full data reload approach is inefficient for incremental updates as it involves reloading all data rather than just the changes. Using Change Data Capture (CDC) is not the most efficient approach for incremental updates in a Microsoft Fabric lakehouse environment.

Incrementally load data from Data Warehouse to Lakehouse - Training | Microsoft Lear

Question 22 of 50
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

Question 23 of 50
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

Question 24 of 50
A company uses a lakehouse architecture with Microsoft Fabric.

You plan to transform large datasets in Delta format for machine learning.

You need to perform data transformations efficiently using Microsoft Fabric tools.

What should you use?

Your Answer
Apache Spark notebooks.

This answer is correct.
Correct Answer
Apache Spark notebooks.

This answer is correct.
Apache Spark notebooks are ideal for processing large-scale data transformations and support the Delta format, making them suitable for this scenario. Power BI Dataflows are often confused with Dataflows Gen2, but they are not designed for large-scale data transformations in a lakehouse environment. Azure Data Factory is a powerful tool for data integration and orchestration but is not specifically designed for direct data transformations within a lakehouse environment using Delta format. SQL Server Management Studio is primarily used for managing SQL databases and is not optimized for large-scale data transformations in a lakehouse environment.

Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn

Question 25 of 50
Your organization uses Microsoft Fabric to manage data across cloud platforms.

You plan to integrate data from a cloud storage service into a lakehouse in Microsoft OneLake.

You need to ensure data from the cloud storage service is accessible within the lakehouse without duplication.

What should you do?

Your Answer
Create a shortcut pointing to the cloud storage service.

This answer is correct.
Correct Answer
Create a shortcut pointing to the cloud storage service.

This answer is correct.
Creating a shortcut in the lakehouse pointing to the cloud storage service allows direct access to the data without creating redundant copies, leveraging Microsoft OneLake's capability to unify data across different storage systems. Using a Data Factory pipeline to transform and load data would result in redundant copies and increased storage costs, which is unnecessary when using Microsoft OneLake shortcuts.

OneLake shortcuts - Training | Microsoft Learn

Question 26 of 50
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

Question 27 of 50
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

Question 28 of 50
You are implementing a new data warehouse solution using Microsoft Fabric.

You need to implement a solution that captures changes in dimension tables over time while preserving historical data.

Which type of Slowly Changing Dimension (SCD) should you use?

Your Answer
Type 2 Slowly Changing Dimension (SCD)

This answer is correct.
Correct Answer
Type 2 Slowly Changing Dimension (SCD)

This answer is correct.
Type 2 SCD is the most suitable choice for capturing changes in dimension tables over time while preserving historical data. It adds new records for changes, maintaining a full history for a given natural key. Type 4 SCD involves creating a new dimension for changes, which is not suitable for tracking historical changes within the same dimension table. Type 1 SCD overwrites existing data and does not keep history, failing to meet the requirement. Type 3 SCD adds history as a new column, but its scope is limited and not suitable for comprehensive historical tracking.

Dimensional modeling in Microsoft Fabric Warehouse: Dimension tables - Training | Microsoft Learn

Question 29 of 50
You are using Microsoft Fabric to manage data ingestion and transformation.

You need to set up a data pipeline to ingest batch data from multiple CSV files stored in Azure Blob Storage. The solution must ensure the process is efficient and handles errors effectively.

Which three actions should you perform? Each correct answer presents part of the solution.

Your Answer
Specify a location for rejected rows.

This answer is correct.
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

Question 30 of 50
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

Question 31 of 50
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

Question 32 of 50
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

Question 33 of 50
Your organization uses Microsoft Fabric to process streaming data from IoT devices.

You need to transform the streaming data in real-time for analysis.

What should you use?

Your Answer
Spark Structured Streaming with Delta tables.

This answer is correct.
Correct Answer
Spark Structured Streaming with Delta tables.

This answer is correct.
Spark Structured Streaming with Delta tables is the most suitable solution for real-time data ingestion and transformation due to its ability to efficiently handle streaming data while maintaining data integrity through ACID transactions. Azure Stream Analytics, although capable of real-time processing, does not offer the same level of integration and transformation capabilities. Azure Data Factory is intended for data orchestration and lacks the necessary features for real-time data ingestion and transformation. Azure Event Hubs is designed for real-time data ingestion but does not provide the transformation capabilities needed for real-time analysis.

Use delta tables with streaming data - Training | Microsoft Learn
Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn

Question 34 of 50
Your organization is implementing a real-time analytics solution using Microsoft Fabric to process streaming data from IoT devices.

You need to configure a job to ingest streaming data into a table for near real-time querying.

Which three actions should you perform? Each correct answer presents part of the solution.

Your Answer
Create a Spark Job Definition with a Python script for Structured Streaming.

This answer is correct.
Set the checkpoint location in the streaming job.

This answer is correct.
Use Delta table as a sink for streaming data.

This answer is correct.
Correct Answer
Create a Spark Job Definition with a Python script for Structured Streaming.

This answer is correct.
Set the checkpoint location in the streaming job.

This answer is correct.
Use Delta table as a sink for streaming data.

This answer is correct.
Creating a Microsoft Spark Job Definition with a Python script using Microsoft Spark Structured Streaming is essential for processing streaming data and writing it to a Microsoft Delta table. Using the Microsoft Delta table as a sink allows the streaming data to be stored in a structured format, enabling efficient querying and analysis. Setting the checkpoint location is crucial for maintaining the state of the stream processing and ensuring fault tolerance. Batch processing is not suitable for real-time data ingestion as it does not support continuous data flow. Storing data in a JSON file does not support real-time querying and lacks the transactional capabilities of a Microsoft Delta table.

Use delta tables with streaming data - Training | Microsoft Learn
Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn

Question 35 of 50
Your organization implements a real-time analytics solution using Microsoft Fabric to process streaming data from IoT devices.

You need to ensure efficient processing of streaming data for prompt querying.

Which two actions should you perform? Each correct answer presents part of the solution.

Your Answer
Implement Spark Structured Streaming.

This answer is correct.
Set up a SQL analytics endpoint.

This answer is correct.
Correct Answer
Implement Spark Structured Streaming.

This answer is correct.
Set up a SQL analytics endpoint.

This answer is correct.
Setting up a SQL analytics endpoint allows querying of data stored in Delta tables within a Microsoft lakehouse, providing near real-time insights. Implementing Spark Structured Streaming allows for efficient processing and writing of streaming data to Delta tables, supporting ACID transactions and enabling querying in near real-time. Storing data in a JSON file does not support real-time querying or ACID transactions, which are necessary for this scenario. Batch processing does not meet the requirement for near real-time data ingestion and analysis. Azure Stream Analytics is not typically used for processing streaming data in Microsoft Fabric; Microsoft Spark Structured Streaming is more appropriate.

Get streaming data into lakehouse and access with SQL analytics endpoint - Training | Microsoft Learn

Question 36 of 50
Your organization uses Microsoft Fabric to manage and monitor various data activities, including data pipelines, dataflows, and semantic models.

Recently, issues with data ingestion processes failing intermittently have caused delays in data availability for reporting.

You need to determine the cause of these failures and ensure effective monitoring of data ingestion processes to prevent future disruptions.

What should you do?

Your Answer
Use the Monitor hub to filter activities by status and start time.

This answer is correct.
Correct Answer
Use the Monitor hub to filter activities by status and start time.

This answer is correct.
Using the Monitor hub to filter activities by status and start time is effective because it helps identify patterns in failures, aiding in diagnosing the root cause. Enabling alerts only for non-critical issues can result in missing critical alerts, making it harder to monitor and address them. Increasing the frequency of data ingestion does not address the root cause and leads to more frequent disruptions. Using a basic logging tool might seem like a viable option, but it lacks the advanced features needed for effective monitoring in complex environments like Microsoft Fabric.

Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn
Prepare data for analysis and reporting - Training | Microsoft Learn

Question 37 of 50
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

Question 38 of 50
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

Question 39 of 50
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

Question 40 of 50
You have a Fabric workspace named Workspace1 that contains a data pipeline named Pipeline1.

Pipeline1 runs every morning and loads data into a lakehouse named Lakehouse1.

You discover that Pipeline1 loads data successfully, but the load takes longer than expected.

You need to monitor the data transformation process to identify possible performance issues.

What should you use?

Your Answer
Monitoring hub

This answer is correct.
Correct Answer
Monitoring hub

This answer is correct.
Monitoring hub surfaces transformation metrics and performance insights; activators automate responses to events, dataflows perform transformations, and pipelines orchestrate tasks but do not provide the dedicated monitoring views.

Introduction

Understand monitoring

Question 41 of 50
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

Question 42 of 50
Your company uses a lakehouse architecture with Microsoft Fabric for large-scale data analytics.

There are reports about delays in data availability for real-time analytics.

You need to optimize the data ingestion process for timely data availability.

What should you recommend?

Your Answer
Use Spark Structured Streaming for real-time processing.

This answer is correct.
Correct Answer
Use Spark Structured Streaming for real-time processing.

This answer is correct.
Using Spark Structured Streaming to process data in real-time as it arrives is the correct recommendation because it directly addresses the need for real-time data availability. Implementing data partitioning improves access speed but does not solve ingestion delays. Increasing the number of data nodes does not directly optimize the data ingestion process. Switching to micro-batch processing would still introduce delays, not eliminate them.

Use delta tables with streaming data - Training | Microsoft Learn

Question 43 of 50
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

Question 44 of 50
Your organization uses Microsoft Fabric Lakehouse to manage large datasets for analytics.

You notice that  query performance has degraded due to the increasing number of small Parquet files generated during data ingestion.

You need to reduce the number of small files to improve query performance in the Microsoft Fabric Lakehouse tables.

What should you do?

Your Answer
Use Optimize to consolidate small files.

This answer is correct.
Correct Answer
Use Optimize to consolidate small files.

This answer is correct.
Using the Optimize command in Microsoft Fabric Lakehouse consolidates multiple small Parquet files into larger files, which improves query performance by reducing the number of files that need to be scanned during read operations. Applying V-Order optimizes sorting and compression but does not specifically address the issue of consolidating small files into larger ones. Increasing file size using Delta Lake compaction might seem like a solution but does not directly address the issue of consolidating small files. Using the Lakehouse API for file management might seem like a solution to optimize file sizes, but it does not directly address the issue of consolidating small files for better query performance.

Use table maintenance feature to manage delta tables in Fabric - Training | Microsoft Learn

Question 45 of 50
Your company uses Microsoft Fabric's lakehouse architecture to store and process large volumes of data.

You notice that some queries are not performing as expected, particularly those involving user-defined functions (UDFs).

You need to ensure optimal query performance while maintaining use of UDFs.

What should you do?

Your Answer
Use traditional Spark engine.

This answer is correct.
Correct Answer
Use traditional Spark engine.

This answer is correct.
Using traditional Spark engine for queries involving UDFs ensures compatibility and maintains performance due to the native execution engine's lack of support for UDFs. Enabling high concurrency mode might improve overall throughput but does not address the specific performance issues with UDFs. Enabling query caching does not address the compatibility issue with UDFs in the native execution engine. Switching to a different execution engine might seem like a solution, but it does not resolve the compatibility issues with UDFs.

Load data using T-SQL - Training | Microsoft Learn

Question 46 of 50
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

Question 47 of 50
Your company uses Microsoft Fabric for its data warehouse, loading large datasets from Azure Blob Storage.

You need to ensure efficient data ingestion with minimal errors.

What should you do?

Your Answer
Use COPY statement with wildcards.

This answer is correct.
Correct Answer
Use COPY statement with wildcards.

This answer is correct.
Using the COPY statement with wildcards enables efficient bulk data loading from multiple files, minimizing complexity and reducing the potential for errors. Enabling data partitioning before loading focuses on optimizing query performance, which does not directly enhance data ingestion efficiency. Using a single INSERT statement for each row is inefficient and increases the likelihood of errors, especially with large datasets. Using a single INSERT statement per file is not suitable for large datasets due to increased transaction times and potential errors.

Load data using T-SQL - Training | Microsoft Learn
COPY INTO (Transact-SQL) - Training | Microsoft Learn

Question 48 of 50
Your company uses Microsoft Fabric to manage a large-scale data lakehouse containing numerous Delta tables. The tables are frequently updated and queried by various analytics teams.

You notice that query performance has degraded over time, leading to increased processing times and higher costs.

You need to recommend maintenance strategies to enhance the efficiency of Delta tables in a lakehouse.

Which three actions should you recommend? Each correct answer presents part of the solution.

Your Answer
Apply V-Order.

This answer is correct.
Use the OPTIMIZE command

This answer is correct.
Use the VACUUM command.

This answer is correct.
Correct Answer
Apply V-Order.

This answer is correct.
Use the OPTIMIZE command

This answer is correct.
Use the VACUUM command.

This answer is correct.
Applying V-Order optimizes sorting, encoding, and compression of Delta Parquet files, enhancing read operations and maintaining efficient query performance. Performing bin-compaction consolidates small Parquet files into larger ones, improving read efficiency and reducing the number of files scanned during queries. Using the VACUUM command removes old files, optimizing storage costs and potentially improving query performance by reducing clutter. Reducing the retention period might seem beneficial for performance but can lead to data loss and compromise Delta's time travel capabilities. Enabling Delta caching might seem beneficial for performance but can lead to increased memory usage and potential performance degradation if not managed properly.

Use table maintenance feature to manage delta tables in Fabric - Training | Microsoft Learn

Question 49 of 50
Your company uses Microsoft Fabric Lakehouse to manage large datasets for analytics.

Recently, query performance on a Delta table has degraded due to an increase in small Parquet files.

You need to optimize the Delta table to improve query efficiency.

Which two actions should you perform? Each correct answer presents part of the solution.

Your Answer
Apply V-Order for better data sorting and compression.

This answer is correct.
Use the OPTIMIZE command to consolidate files.

This answer is correct.
Correct Answer
Apply V-Order for better data sorting and compression.

This answer is correct.
Use the OPTIMIZE command to consolidate files.

This answer is correct.
Applying V-Order optimizes sorting, encoding, and compression, enhancing read operations and overall query performance. The Optimize command consolidates multiple small Parquet files into larger ones, improving query performance by reducing the number of files that need to be scanned. Converting to a Hive table format is not supported for Delta tables in Lakehouse and would not improve performance. Increasing the number of partitions might seem beneficial but can lead to increased overhead and slower query times if not managed properly.

Use table maintenance feature to manage delta tables in Fabric - Training | Microsoft Learn

Question 50 of 50
Your company has implemented a Microsoft Fabric data warehouse to handle large-scale data ingestion and processing.

The current setup involves frequent data loads throughout the day, which sometimes lead to performance bottlenecks.

You need to optimize the data ingestion process to handle large volumes efficiently without causing performance issues.

Which two actions should you perform? Each correct answer presents part of the solution.

Your Answer
Divide large INSERT operations into smaller parts.

This answer is correct.
Group INSERT statements into batches.

This answer is correct.
Correct Answer
Divide large INSERT operations into smaller parts.

This answer is correct.
Group INSERT statements into batches.

This answer is correct.
Grouping INSERT statements into batches reduces transaction overhead, thereby improving performance during data ingestion. Dividing large INSERT operations into smaller parts minimizes rollback time and enhances system responsiveness, making it an effective strategy for handling large data volumes. Using smaller data types for columns can lead to data truncation or loss if not carefully considered, which is counterproductive to the goal of optimizing data ingestion.

Performance guidelines in Fabric Data Warehouse - Training | Microsoft Learn