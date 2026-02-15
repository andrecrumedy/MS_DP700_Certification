Question 1 of 50

Your organization uses Microsoft Fabric to manage real-time data ingestion from various IoT devices through Azure Event Hubs. The data is processed and stored in a Microsoft Delta Lake for further analysis.

You need to ensure that unnecessary columns, such as sensor IDs, are removed before storing the data in Microsoft Delta Lake format.

What should you do?

Select only one answer.

Store data in a temporary staging area and filter columns before final storage.


Use a batch processing system to clean data before transfer.


Use a Spark job to preprocess data before ingestion.


Use the event processor to remove unnecessary columns.

This answer is correct.
Using the event processor to remove unnecessary columns before sending data to the lakehouse is the most efficient solution, as it automates the filtering process and ensures only relevant data is stored. Using a Spark job for preprocessing can be unnecessarily complex and resource-intensive compared to built-in tools. Storing data in a temporary staging area before filtering can lead to inefficiencies in processing and storage. Using a batch processing system for cleaning data is not suitable for real-time processing as it introduces delays and is not efficient for continuous data streams.

Get started with lakehouses in Microsoft Fabric - Training | Microsoft Learn

Question 2 of 50

Your organization uses Microsoft Fabric to manage real-time data from IoT devices sent to Azure Event Hub.

You need to recommend a solution to process events for storage in a Fabric lakehouse.

Which two actions should you recommend? Each correct answer presents part of the solution.

Select all answers that apply.

Set up an eventstream with Azure Event Hub as a source.

This answer is correct.

Use Azure Data Factory for real-time data ingestion.


Use Azure Stream Analytics to process data from Azure Event Hub.


Use Data Factory pipelines to ingest data into the lakehouse.


Use the event processor to filter and transform data.

This answer is correct.
Setting up an eventstream with Azure Event Hub as a source is essential for ingesting real-time data into Microsoft Fabric, allowing for the initial data flow setup. Using the event processor to filter and transform data ensures that only necessary data is stored, optimizing storage and processing efficiency. Using Data Factory pipelines is not suitable for real-time event processing, as they are designed for batch processing. Using Azure Stream Analytics to process data from Azure Event Hub is not appropriate for the specific goal of storing processed data in a Fabric lakehouse. Using Azure Data Factory for real-time data ingestion is not appropriate, as it is more suited for batch processing.

Get started with lakehouses in Microsoft Fabric - Training | Microsoft Learn

Question 3 of 50

You are implementing a data warehouse using Microsoft Fabric.

You plan to integrate data from multiple sources, including Microsoft Azure Data Lake Storage Gen2 and Microsoft SQL Server databases.

You need to design a process to efficiently load data into tables while ensuring data quality and consistency.

Which two tasks should you recommend? Each correct answer presents part of the solution.

Select all answers that apply.

Use Azure Synapse Analytics for data integration.


Use Data Factory pipelines for ETL orchestration and T-SQL execution.

This answer is correct.

Use dataflows to ingest and transform data from Azure Data Lake Storage Gen2.

This answer is correct.

Use SSIS packages for data integration.

Using Microsoft Data Factory pipelines and dataflows are both effective methods for orchestrating ETL processes and transforming data from various sources into a dimensional model. Microsoft Data Factory pipelines allow for complex orchestration and execution of T-SQL scripts, ensuring efficient data transformation and loading. Dataflows offer a low-code solution for data ingestion and transformation using Power Query, making them suitable for integrating data from Microsoft Azure Data Lake Storage Gen2. Using SSIS packages for data integration is less efficient compared to modern tools like Data Factory and dataflows, especially in a Microsoft Fabric environment. While Azure Synapse Analytics is a powerful tool for data analytics and integration, it is not specifically designed for the ETL processes required to transform and load data into a dimensional model.

Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn
Prepare data for analysis and reporting - Training | Microsoft Learn

Question 4 of 50

Your company uses a Microsoft Fabric data warehouse to store frequently updated customer transaction data.

You need to design an ETL process that minimizes load on source systems while ensuring only new or changed data is loaded.

What should you include in your design?

Select only one answer.

Implement a trigger-based change detection.


Perform nightly full data loads.


Use a timestamp column for incremental data loading.


Use Change Data Capture (CDC) for tracking source data changes.

This answer is correct.
Using Change Data Capture (CDC) is the most efficient method for tracking changes in the source data, allowing only new or changed data to be loaded into the warehouse, thus minimizing the load on the source systems. Performing a full data load every night is inefficient and places unnecessary load on the source systems, making it unsuitable for frequent updates. Using a timestamp column for incremental data loading may not capture all changes as effectively as CDC, particularly in complex scenarios. Implementing a trigger-based change detection can introduce complexity and may not efficiently handle large volumes of data changes, making it less effective for this scenario.

Dimensional modeling in Microsoft Fabric Warehouse: Load tables - Training | Microsoft Learn

Question 5 of 50

You have a Fabric lakehouse named Lakehouse1 that contains a table named Sales. Sales contains the following columns:

OrderID (INT)
OrderDate (DATE)
ProductID (INT)
Quantity (INT)
You plan to implement incremental loads of new sales records from a CSV file located in the /files/sales/ folder of Lakehouse1.

You need to identify a querying solution for the incremental loads. The solution must minimize maintenance effort.

What should you use?

Select only one answer.

a notebook

This answer is correct.

a pipeline


a stored procedure

This answer is incorrect.

Auto Loader

Notebooks provide flexible, code-based incremental load patterns for Fabric lakehouses; Auto Loader is not available in Fabric, stored procedures aren’t a lakehouse querying solution, and pipelines are orchestration—not querying.

Options to get data into the Fabric Lakehouse

Question 6 of 50

You have a Fabric eventhouse that contains a KQL database named DB1.

You ingest data into DB1 from multiple sources.

You need to transform the data during ingestion. The solution must minimize development effort.

What should you use?

Select only one answer.

dataflows />


KQL

This answer is correct.

notebooks


T-SQL

KQL supports ingest-time transformations via update policies; T-SQL targets warehouses, notebooks require authoring/orchestration, and dataflows are for batch preparation into lakehouses/warehouses.

Choose an analytical data store in Microsoft Fabric

Store and query real-time data

Question 7 of 50

Your organization uses Microsoft Fabric for data analytics. The SQL database mirrors data to OneLake.

You need to ensure mirrored data is consistent and accessible during SQL database downtime.

What should you do?

Select only one answer.

Reconfigure mirroring settings after downtime.


Set up a data integration pipeline with Azure Data Factory.


Set up a secondary database for manual replication.


Use automatic mirroring in Microsoft Fabric.

This answer is correct.
Using automatic mirroring in Microsoft Fabric is the most effective solution because it ensures data replication resumes automatically after downtime, maintaining consistency and accessibility. Reconfiguring mirroring settings manually is unnecessary due to Microsoft Fabric's built-in capabilities. Setting up a secondary database for manual replication is redundant, and setting up a data integration pipeline with Azure Data Factory is not needed as Microsoft Fabric's mirroring already ensures data consistency and recovery.

What is Mirroring in Fabric? - Training | Microsoft Learn

Question 8 of 50

You are implementing a new data warehouse solution using Microsoft Fabric.

You need to implement a solution that captures changes in dimension tables over time while preserving historical data.

Which type of Slowly Changing Dimension (SCD) should you use?

Select only one answer.

Type 1 Slowly Changing Dimension (SCD)


Type 2 Slowly Changing Dimension (SCD)

This answer is correct.

Type 3 Slowly Changing Dimension (SCD)


Type 4 Slowly Changing Dimension (SCD)

Type 2 SCD is the most suitable choice for capturing changes in dimension tables over time while preserving historical data. It adds new records for changes, maintaining a full history for a given natural key. Type 4 SCD involves creating a new dimension for changes, which is not suitable for tracking historical changes within the same dimension table. Type 1 SCD overwrites existing data and does not keep history, failing to meet the requirement. Type 3 SCD adds history as a new column, but its scope is limited and not suitable for comprehensive historical tracking.

Dimensional modeling in Microsoft Fabric Warehouse: Dimension tables - Training | Microsoft Learn

Question 9 of 50

You are using Microsoft Fabric to manage data ingestion and transformation.

You need to set up a data pipeline to ingest batch data from multiple CSV files stored in Azure Blob Storage. The solution must ensure the process is efficient and handles errors effectively.

Which three actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Specify a location for rejected rows.

This answer is correct.

Transform data with Azure Data Lake Storage Gen2 before ingestion.


Transform data with Power BI before ingestion.


Use the COPY statement to load data.

This answer is correct.

Use wildcards in the path to load multiple files.

This answer is correct.
To achieve efficient data ingestion and effective error handling, it is crucial to use the COPY statement, specify a REJECTED_ROW_LOCATION, and use wildcards. The COPY statement is optimal for loading data from Microsoft Azure Blob Storage, ensuring efficiency. Specifying a REJECTED_ROW_LOCATION enhances error management by isolating problematic rows for further analysis. Using wildcards allows for the bulk loading of multiple files, streamlining the process. Transforming data with Power BI or Azure Data Lake Storage Gen2 before ingestion adds unnecessary complexity when the focus is on efficient ingestion using the COPY statement.

Load data using T-SQL - Training | Microsoft Learn

Question 10 of 50

You use Microsoft Fabric to manage data across cloud platforms.

You plan to ingest batch data from Azure Blob Storage into a warehouse.

You need to determine the most efficient method to import this data using Microsoft Fabric tools.

What should you use?

Select only one answer.

Azure Synapse Analytics.


COPY statement with Shared Access Signature.

This answer is correct.

Data Factory pipeline.


Dataflows Gen2.

This answer is incorrect.
The COPY statement with Shared Access Signature efficiently ingests batch data from Azure Blob Storage into a warehouse due to its direct and secure data transfer capabilities. In contrast, a Data Factory pipeline requires manual configuration, making it less efficient. Dataflows Gen2 focus on data preparation and transformation, which does not align with the task of batch data ingestion. Azure Synapse Analytics is not designed for efficient batch data ingestion using Microsoft Fabric tools.

Load data using T-SQL - Training | Microsoft Learn

Question 11 of 50

You are implementing a new data analytics solution using Microsoft Fabric.

The data to be ingested includes structured, semi-structured, and unstructured formats from various sources.

You need to select a data store that accommodates diverse data formats and supports both PySpark and SQL operations for data transformation and analysis.

Which two data stores should you select? Each correct answer presents a complete solution.

Select all answers that apply.

Azure Data Lake Storage Gen2

This answer is incorrect.

Azure Synapse Analytics

This answer is correct.

Microsoft Fabric Eventhouse


Microsoft Lakehouse

This answer is correct.
Azure Synapse Analytics is suitable because it supports all data formats and allows operations using T-SQL and Spark, accommodating the team's diverse skill set and data needs. Microsoft Lakehouse is also appropriate as it supports structured, semi-structured, and unstructured data formats and allows operations using both PySpark and SQL, aligning with the team's skills and data requirements. In contrast, Microsoft Fabric Eventhouse is designed for real-time analytics and supports diverse data formats but is not optimized for batch processing or large-scale data transformation using PySpark and SQL, which are required in this scenario. Azure Data Lake Storage Gen2, while capable of storing diverse data formats, does not natively support PySpark and SQL operations, making it unsuitable for this scenario.

Microsoft Fabric decision guide: choose a data store - Training | Microsoft Learn

Question 12 of 50

Your organization uses Microsoft Fabric to process real-time data from IoT devices.

You need to implement a solution for ingesting and transforming streaming data without writing code.

What should you do?

Select only one answer.

Use Azure Event Hubs to ingest and transform the data.


Use Azure Stream Analytics to process the data.


Use Microsoft Spark Structured Streaming with PySpark scripts.


Use the eventstreams feature in Microsoft Fabric with enhanced capabilities.

This answer is correct.
Using the eventstreams feature in Microsoft Fabric with enhanced capabilities enabled is the correct choice because it provides a no-code solution for ingesting and transforming streaming data, meeting the requirements of the scenario. Using Azure Stream Analytics requires setting up queries, which does not satisfy the no-code requirement. Using Azure Event Hubs requires coding for data transformation, making it unsuitable for the no-code requirement. Using Microsoft Spark Structured Streaming with PySpark scripts also involves coding, making it unsuitable for the no-code requirement.

Fabric Eventstream - overview - Training | Microsoft Learn

Question 13 of 50

Your organization uses Microsoft Fabric to process real-time IoT data monitoring environmental conditions. The data includes temperature and humidity readings streamed into a Microsoft KQL database.

You need to ensure efficient data ingestion and near real-time querying for reporting.

What should you do?

Select only one answer.

Implement Spark Structured Streaming to write data to Delta table.

This answer is correct.

Store data in Azure Blob Storage and load periodically into KQL database.


Use Azure Data Explorer for data storage and direct querying.


Use Azure Stream Analytics for real-time data processing and querying.

Implementing Spark Structured Streaming to write data to a Delta table is effective because it supports efficient ingestion and near real-time querying of streaming data, aligning with the scenario's requirements. Using Azure Stream Analytics for real-time data processing and querying is not suitable as it does not integrate with Microsoft Fabric's KQL database. Storing data in Azure Blob Storage and loading it periodically fails to meet the real-time processing needs. Using Azure Data Explorer for data storage and direct querying is unsuitable as it is not directly integrated with Microsoft Fabric's KQL database.

Work with Delta Lake tables in Microsoft Fabric - Training | Microsoft Learn

Question 14 of 50

Your organization implements a real-time analytics solution using Microsoft Fabric to process streaming data from IoT devices.

You need to ensure efficient processing of streaming data for prompt querying.

Which two actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Implement Spark Structured Streaming.

This answer is correct.

Set up a SQL analytics endpoint.

This answer is correct.

Store streaming data in a JSON file.


Use Azure Stream Analytics for data processing.

This answer is incorrect.

Use batch processing to load data every hour.

Setting up a SQL analytics endpoint allows querying of data stored in Delta tables within a Microsoft lakehouse, providing near real-time insights. Implementing Spark Structured Streaming allows for efficient processing and writing of streaming data to Delta tables, supporting ACID transactions and enabling querying in near real-time. Storing data in a JSON file does not support real-time querying or ACID transactions, which are necessary for this scenario. Batch processing does not meet the requirement for near real-time data ingestion and analysis. Azure Stream Analytics is not typically used for processing streaming data in Microsoft Fabric; Microsoft Spark Structured Streaming is more appropriate.

Get streaming data into lakehouse and access with SQL analytics endpoint - Training | Microsoft Learn

Question 15 of 50

Your organization is implementing a real-time analytics solution using Microsoft Fabric to process streaming data from IoT devices.

You need to ensure that the streaming data is efficiently processed and accessible for analysis.

Which two actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Configure a SQL analytics endpoint.

This answer is correct.

Set up a Power BI dataflow.


Use Azure Stream Analytics


Use Spark Structured Streaming.

This answer is correct.
Configuring a SQL analytics endpoint allows querying of the Delta table, providing real-time insights into the streaming data stored in the Microsoft lakehouse. Using Spark Structured Streaming allows for real-time data processing and writing to Delta tables, which are optimized for both batch and streaming data. Setting up a Power BI dataflow might seem like a viable option for data processing, but it is not suitable for real-time streaming data ingestion. Using Azure Stream Analytics might seem like a viable option for real-time data processing, but it is not directly integrated with Microsoft Fabric for this specific use case.

Use delta tables with streaming data - Training | Microsoft Learn
Get streaming data into lakehouse and access with SQL analytics endpoint - Training | Microsoft Learn

Question 16 of 50

Your company is transitioning to a data mesh architecture using Microsoft Fabric.

You are responsible for organizing data into domains.

You need to configure settings for independent management of rules and restrictions by each business unit.

What should you do?

Select only one answer.

Assign workspaces to multiple domains.

This answer is incorrect.

Configure domain-specific sensitivity labels.


Create workspaces with shared governance settings.


Delegate tenant-level settings to domains.

This answer is correct.
Delegating tenant-level settings to the domain level allows each business unit to manage its own governance settings, which is essential for implementing a data mesh architecture. Assigning workspaces to multiple domains complicates governance and does not support independent management. Creating workspaces with shared governance settings centralizes control and does not facilitate domain-specific governance. Configuring domain-specific sensitivity labels is related to governance but does not address the need for independent management of rules and restrictions by each business unit.

Prepare to use Apache Spark - Training | Microsoft Learn
Implement row-level security - Training | Microsoft Learn

Question 17 of 50

Your company uses Microsoft Fabric to manage data engineering workloads.

You notice performance issues with Spark jobs due to inefficient resource allocation.

You need to optimize the Spark pool configuration to improve performance and reduce costs.

Which three actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Configure dynamic allocation for executors.

This answer is correct.

Enable autoscale for node provisioning.

This answer is correct.

Enable fixed resource allocation.


Select memory-optimized nodes.

This answer is correct.

Use compute-optimized nodes.

This answer is incorrect.

Use static node allocation.

Configuring dynamic allocation for executors optimizes resource usage by adjusting executor processes according to data volume, enhancing performance and efficiency. Enabling autoscale for node provisioning allows the Spark pool to dynamically adjust the number of nodes based on workload demands, optimizing resource usage and cost. Selecting memory-optimized nodes provides better performance for data-intensive operations, which is critical for improving Spark job efficiency. Enabling fixed resource allocation does not address performance issues related to dynamic resource needs and could lead to inefficient resource usage. Using static node allocation lacks flexibility in resource allocation, necessary for handling varying workloads efficiently. Using compute-optimized nodes may seem beneficial for performance but are not ideal for data-intensive Spark jobs compared to memory-optimized nodes.

Prepare to use Apache Spark | Microsoft Learn

Question 18 of 50

Your organization is implementing a data mesh architecture using Microsoft Fabric.

The IT department plans to delegate governance controls to business units.

You need to configure settings for independent data management by business units.

Which three actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Assign domain-specific sensitivity labels.

This answer is incorrect.

Assign workspaces to domains.

This answer is correct.

Delegate tenant settings to domains.

This answer is correct.

Enable domain-level sensitivity labels.


Implement row-level security.


Specify domain administrators.

This answer is correct.
Assigning workspaces to specific domains ensures that all data within those workspaces is governed by the domain's rules and restrictions. Delegating tenant-level settings to the domain level allows each business unit to define its own rules and restrictions, enabling domain-specific governance. Specifying domain admins allows for effective management of domain settings and ensures that domain-specific governance is enforced. Implementing row-level security is a common data governance practice, but it does not directly enable domain-level governance in a data mesh architecture. Assigning domain-specific sensitivity labels is related to data protection but does not directly enable independent data management by business units.

Fabric domains | Microsoft Learn

Question 19 of 50

Your organization uses Microsoft Fabric for data engineering and runs Spark jobs requiring efficient resource utilization.

You need to optimize resource management in the Microsoft Spark environment based on workload demands.

What should you do?

Select only one answer.

Enable autoscaling

This answer is correct.

Enable fixed resource allocation


Set a fixed number of executors


Change nodesize to Large

To optimize resource management in the Microsoft Spark environment, enabling autoscaling is the most effective solution. It allows the system to dynamically adjust the number of nodes based on workload demands, ensuring efficient resource utilization. Enabling fixed resource allocation would prevent necessary adjustments, contradicting the optimization goal. Setting a fixed number of nodes leads to inefficiencies as it lacks dynamic adjustment capabilities. Using a single node cluster restricts scalability and flexibility, failing to accommodate varying workloads effectively.

What is Apache Spark compute in Microsoft Fabric? - Training | Microsoft Learn
Data Engineering workspace administration settings in Microsoft Fabric - Training | Microsoft Learn

Question 20 of 50

Your organization uses Microsoft Fabric deployment pipelines with stages: Development, Test, and Production.

You need to configure the Production stage to connect to the production database. The solution must minimize administrative effort.

What should you do?

Select only one answer.

Create a deployment rule for Production.

This answer is correct.

Use a script to update the database connection after each deployment.


Use deployment pipelines to manage database connections.

This answer is incorrect.

Use full deployment to update all settings.

Creating a deployment rule for the Production stage is essential to ensure the production database connection remains intact during deployments. Using deployment pipelines to manage database connections is a common misconception, as they are not specifically designed for this purpose. Using a script to update the database connection can introduce complexity and potential errors if not managed properly. Full deployment updates all content but does not specifically address the need to maintain certain settings, such as database connections.

Get started with deployment pipelines - Training | Microsoft Learn

Question 21 of 50

Your organization uses Microsoft Fabric with deployment pipelines to deploy an analytics solution over multiple stages.

You need to ensure database connections are correct after deploying content in each stage.

What should you do?

Select only one answer.

Check database connection settings.


Define deployment rules.

This answer is correct.

Use automatic binding.


Use deployment pipelines to manage database connections.

To ensure database connections remain correct after content deployment, defining deployment rules is crucial. This method allows specifying database connections for each stage, directly addressing the need for accuracy. Using deployment pipelines might seem like a way to manage connections but does not guarantee their correctness post-deployment. Checking database connection settings can help verify current configurations but does not actively maintain them post-deployment. Automatic binding might seem like it ensures correct connections but does not focus on updating database connections.

Get started with deployment pipelines - Training | Microsoft Learn

Question 22 of 50

Your organization uses Microsoft Fabric deployment pipelines to manage analytics solutions across Development, Test, and Production stages.

You need to restrict editing of pipeline settings to authorized users only.

What should you do?

Select only one answer.

Assign pipeline admin roles.

This answer is correct.

Configure workspace permissions.


Enable stage-level security.


Implement role-based access control.

This answer is incorrect.
To ensure that only authorized users can edit pipeline settings, assigning pipeline admin roles is essential. This approach maintains security and control over the deployment process. Configuring workspace permissions involves setting access levels for users within a workspace, but it does not specifically restrict editing of pipeline settings. Enabling stage-level security might seem like it restricts access, but it fails to limit editing permissions. Implementing role-based access control manages user permissions but does not specifically influence who can edit pipeline settings.

The deployment pipelines process - Training | Microsoft Learn
Get started with deployment pipelines - Training | Microsoft Learn

Question 23 of 50

Your organization uses Microsoft Fabric for analytics solutions.

You plan to set up deployment pipelines for transitions between development, testing, and production environments.

You need to maintain distinct configurations for each stage and ensure only verified changes are promoted to production.

Which two actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Assign one workspace to all stages.


Create unique deployment rules for each stage.

This answer is correct.

Deploy content across all stages simultaneously.


Use selective deployment for content control.

This answer is correct.
Assigning one workspace to all stages undermines the separation of environments, which is vital for effective deployment management. Creating unique deployment rules for each stage is essential for maintaining distinct configurations, allowing each environment to operate with its own settings. Deploying content across all stages simultaneously bypasses necessary testing and control measures, risking untested changes reaching production. Using selective deployment allows specific content movement, ensuring only tested changes reach production, providing control over the deployment process.

Deploy content using Deployment pipelines - Training | Microsoft Learn
Create deployment rules - Training | Microsoft Learn

Question 24 of 50

You have a Fabric workspace named Workspace1 that contains a notebook named Notebook1.

You need to implement version control for Notebook1. The solution must ensure that you can revert Notebook1 to any previous state.

What should you do?

Select only one answer.

Add Notebook1 to an Azure Data Factory pipeline. />


Connect Workspace1 to a Git repository.

This answer is correct.

Create a deployment pipeline.


Create a branch in Workspace1.

Connecting the workspace to Git enables commits and versioning; deployment pipelines move content between stages, branching requires a Git repo first, and Data Factory pipelines do not provide source control.

Notebook source control and deployment

Question 25 of 50

You have a Fabric data warehouse named Warehouse1.

You need to create a database project for Warehouse1 in Microsoft Visual Studio Code. The solution must allow you to later modify the schema of Warehouse1 from within Visual Studio Code. The solution must NOT affect the existing schema of Warehouse1 when the project is created.

What should you do first?

Select only one answer.

Add a connection to DB1, right-click the connection, and select Manage Packages.


Add a connection to Warehouse1, right-click the connection, and select Create Project From Database.

This answer is correct.

Add a connection to warehouse1, right-click the connection, and select New Query.


From the Command Palette, run Create Database Project From Scratch.

Creating a project from the connected database imports schema into a project without altering the database; other actions either don’t create a project or don’t import existing schema.

Use SQL Database Projects

Develop warehouse projects in Visual Studio Code

Question 26 of 50

You have a Fabric workspace named Workspace1 that contains two datasets named datasetA and datasetB.

You plan to use a deployment pipeline in Workspace1.

You create a pipeline named pipeline1 and add a development stage and a test stage. You assign Workspace1 to the Development stage of pipeline1. You create another workspace Workspace2.

What will occur when you assign Workspace2 to the test stage of pipeline1?

Select only one answer.

datasetA and datasetB will be copied to Workspace2.

This answer is correct.

No changes will occur.


The development stage will be renamed as test.


Workspace2 will be empty.

Assigning a workspace to a downstream stage deploys items from the development workspace into it; the other options contradict pipeline behavior.

The deployment pipelines process
Implement deployment pipelines

Question 27 of 50

Your company uses a Microsoft Fabric data warehouse to store employee salary information.

You need to configure permissions so that only specific users can view unmasked salary data while others see masked data.

Which permission should you grant to the authorized users?

Select only one answer.

Grant ALTER ANY MASK permission.

This answer is incorrect.

Grant SELECT permission.


Grant UNMASK permission.

This answer is correct.

Grant VIEW DEFINITION permission.

Granting the UNMASK permission is essential as it specifically allows authorized users to view unmasked data in columns where dynamic data masking is applied, meeting the requirement to differentiate access levels. The ALTER ANY MASK permission enables modification of masking rules but does not permit viewing unmasked data, making it unsuitable for this task. The VIEW DEFINITION permission allows users to view metadata about database objects but does not grant access to view unmasked data, thus failing to meet the objective. The SELECT permission facilitates data querying but does not override masking, failing to meet the objective of allowing access to unmasked data.

Explore dynamic data masking - Training | Microsoft Learn
Dynamic data masking in Fabric data warehousing - Training | Microsoft Learn

 
Question 28 of 50

Your organization is using Microsoft Fabric to manage a data warehouse containing sensitive financial data, including columns such as AccountNumber, Balance, and TransactionHistory.

You need to ensure that only authorized finance team members can view the TransactionHistory column.

What should you use?

Select only one answer.

Column-Level Security

This answer is correct.

Data Encryption


Dynamic Data Masking


Row-Level Security

Column-Level Security is essential for controlling access to specific columns, such as TransactionHistory, ensuring that only authorized users can view sensitive financial data. Data Encryption, while useful for securing data, does not offer the column-specific access control required in this scenario. Dynamic Data Masking obscures sensitive data but does not provide access control to specific columns. Row-Level Security manages permissions at a row level, lacking the necessary granularity for protecting individual columns.

Security for data warehousing in Microsoft Fabric - Training | Microsoft Learn

Question 29 of 50

Your company is using Microsoft Fabric to manage a data warehouse that contains a table with sensitive employee information.

The table contains columns such as EmployeeID, Name, Salary, and SocialSecurityNumber.

You need to restrict access to the Salary and SocialSecurityNumber columns to HR personnel only.

Which three actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Create a view to restrict access to the Salary and SocialSecurityNumber columns.


Create an HR role and assign it to HR personnel.

This answer is correct.

Deny SELECT permission on the sensitive columns to other roles.

This answer is correct.

Grant SELECT permission on the sensitive columns to the HR role.

This answer is correct.

Use dynamic data masking on the sensitive columns.

This answer is incorrect.
Creating an HR role and granting it SELECT permission on the sensitive columns ensures that only HR personnel can access the Salary and SocialSecurityNumber data. Denying SELECT permission to all other roles further secures the data by preventing unauthorized access. Creating a view is not appropriate for this scenario, as it does not provide the required column-level access control.

Security for data warehousing in Microsoft Fabric - Training | Microsoft Learn
SQL granular permissions in Microsoft Fabric - Training | Microsoft Learn

Question 30 of 50

Your company has a data warehouse in Microsoft Fabric to store sales data.

Different departments need access to the data, but each department should only see data relevant to their operations.

You need to configure the data warehouse so that each department can only view its own sales data.

Which two actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Create a security policy with a filter predicate for departments.

This answer is correct.

Implement column-level security for Sales table access.


Implement column-level security for sensitive sales data.


Implement row-level security using department identifiers.

This answer is correct.
Creating a security policy with a filter predicate and implementing row-level security using department identifiers ensures that each department can only access its own sales data. Column-level security controls access to specific columns within a table, not specific rows, and does not provide the granularity needed for department-specific access.

Row-level security in Fabric data warehousing - Training | Microsoft Learn

Question 31 of 50

You have a Fabric workspace named Workspace1 that contains a lakehouse named Lakehouse1 and a user named User1.

User1 is assigned the Contributor workspace role for Workspace1.

You discover that User1 is consuming more resources than expected. You remove User1 from Workspace1. User1 now requires read-only access to the data in Lakehouse1.

You need to ensure that User1 can read the data in Lakehouse1. The solution must follow the principle of least privilege.

What should you do?

Select only one answer.

Assign User1 the Contributor workspace role for Workspace1.


Assign User1 the Member workspace role for Workspace1.


Assign User1 the Viewer workspace role for Workspace1.

This answer is incorrect.

Configure item permissions for Lakehouse1.

This answer is correct.
Item-level permissions on Lakehouse1 grant access only to that item, adhering to least privilege; workspace roles (Viewer, Member, Contributor) grant broader access to all workspace items.

Configure workspace and item permissions

Question 32 of 50

Your company implements a new data analytics solution using Microsoft Fabric.

You need to design an orchestration pattern that minimizes manual intervention and supports dynamic data loading into a lakehouse.

Which approach should you recommend?

Select only one answer.

Create individual pipelines for each data source.


Implement a Data Factory pipeline with parameters and dynamic expressions.

This answer is correct.

Use a single notebook for all ETL activities without parameters.

This answer is incorrect.

Use a static configuration for data loading.

Implementing a Data Factory pipeline with parameters and dynamic expressions automates data loading, reduces manual intervention, and supports dynamic data handling. Using a static configuration lacks flexibility, while using a single notebook without parameters lacks flexibility. Creating individual pipelines for each data source increases complexity and maintenance.
https://learn.microsoft.com/en-us/fabric/data-factory/parameters


My Notes:
Browser reset couldn't finish test. Will restart teston next attempt. 
