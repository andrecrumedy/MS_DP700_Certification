Post AI_Assisted Learning
I missed many of the mulitple selection answers. 

It took you 45 minutes to complete this assessment.

Overall Results
To be better prepared for the exam, aim to achieve a score of 80% or higher in multiple attempts.

Score: 86%

Performance by assessment section
To further strengthen your skills in the following areas, refer to the Customized Learning Material section below.

Implement and manage an analytics solution - Fully Passed score near 90%

Ingest and transform data - Barely pass with score at 80%

Monitor and optimize an analytics solution - Fully Pass score just below 90%

Answer Summary
Below is a summary of your answers.

Question 1 of 50
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

Question 2 of 50
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

Question 3 of 50
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

Question 4 of 50
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

Question 5 of 50
Your organization uses Microsoft Fabric for analytics solutions.

You plan to set up deployment pipelines for transitions between development, testing, and production environments.

You need to maintain distinct configurations for each stage and ensure only verified changes are promoted to production.

Which two actions should you perform? Each correct answer presents part of the solution.

Your Answer
Create unique deployment rules for each stage.

This answer is correct.
Use selective deployment for content control.

This answer is correct.
Correct Answer
Create unique deployment rules for each stage.

This answer is correct.
Use selective deployment for content control.

This answer is correct.
Assigning one workspace to all stages undermines the separation of environments, which is vital for effective deployment management. Creating unique deployment rules for each stage is essential for maintaining distinct configurations, allowing each environment to operate with its own settings. Deploying content across all stages simultaneously bypasses necessary testing and control measures, risking untested changes reaching production. Using selective deployment allows specific content movement, ensuring only tested changes reach production, providing control over the deployment process.

Deploy content using Deployment pipelines - Training | Microsoft Learn
Create deployment rules - Training | Microsoft Learn

Question 6 of 50
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

Question 7 of 50
You have a data warehouse named DB1.

You need to use a database project to deploy schema changes to DB1.

What should you do?

Your Answer
Create a new database project, and import the schema of DB1 into the project.

This answer is incorrect.
Correct Answer
Create a new SDK-style project, and import the schema of DB1 into the project.

This answer is correct.
Use an SDK-style SQL Database Project and import the existing database schema; the DAC approaches or non-SDK projects do not meet the requirement.

Use SQL Database Projects

Get started with SQL database projects

What are SQL database projects?

Question 8 of 50
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
Your organization uses Microsoft Fabric for data warehouse management. The security team is concerned about unauthorized access to sensitive customer information in a database.

You need to ensure sensitive data is protected and accessible only to authorized users.

Which three actions should you perform? Each correct answer presents part of the solution.

Your Answer
Define dynamic data masking for sensitive columns.

This answer is correct.
Revoke SELECT permission from non-privileged users.

This answer is incorrect.
Test masking with a non-privileged user.

This answer is correct.
Correct Answer
Define dynamic data masking for sensitive columns.

This answer is correct.
Grant UNMASK permission to authorized users.

This answer is correct.
Test masking with a non-privileged user.

This answer is correct.
Defining dynamic data masking for sensitive columns ensures that unauthorized users cannot view sensitive information, aligning with the security objective. Granting UNMASK permission to authorized users allows them to access unmasked data, maintaining controlled access. Testing masking with a non-privileged user confirms the effectiveness of the masking rules, ensuring they work as intended. Removing all masking rules would expose sensitive data, contradicting the goal of protecting it. Revoking SELECT permission from non-privileged users is impractical as it restricts access to all data, not just sensitive information.

Security for data warehousing in Microsoft Fabric - Training | Microsoft Learn
How to implement dynamic data masking in Fabric Data Warehouse - Training | Microsoft Learn

Question 12 of 50
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

Question 13 of 50
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

Question 14 of 50
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
Your organization uses Microsoft Fabric for managing data pipelines in a large-scale ETL process. The setup involves multiple pipelines that must handle different datasets dynamically, reducing hardcoding and improving maintainability.

You need to reuse pipeline components with varying inputs during execution.

Which two settings should you configure? Each correct answer presents part of the solution.

Your Answer
Pass external values as parameters.

This answer is correct.
Use string interpolation.

This answer is correct.
Correct Answer
Pass external values as parameters.

This answer is correct.
Use string interpolation.

This answer is correct.
Hardcoding dataset paths does not support dynamic execution and requires manual changes for each dataset, which is inefficient. Using string interpolation is effective as it allows the construction of dynamic expressions by incorporating parameter values, facilitating the handling of various datasets. Passing external values as parameters is crucial for dynamic execution, as it enables the pipeline to adapt to different datasets without hardcoding. Fixed dataset configurations are unsuitable because they lack the flexibility needed for runtime changes, failing to meet the dynamic requirements of the scenario.

Load data using T-SQL - Training | Microsoft Learn
Parameters for Data Factory in Microsoft Fabric - Training | Microsoft Learn
Expressions and functions for Data Factory in Microsoft Fabric - Training | Microsoft Learn

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
Your organization uses Microsoft Fabric to manage real-time data ingestion from various IoT devices through Azure Event Hubs. The data is processed and stored in a Microsoft Delta Lake for further analysis.

You need to ensure that unnecessary columns, such as sensor IDs, are removed before storing the data in Microsoft Delta Lake format.

What should you do?

Your Answer
Use the event processor to remove unnecessary columns.

This answer is correct.
Correct Answer
Use the event processor to remove unnecessary columns.

This answer is correct.
Using the event processor to remove unnecessary columns before sending data to the lakehouse is the most efficient solution, as it automates the filtering process and ensures only relevant data is stored. Using a Spark job for preprocessing can be unnecessarily complex and resource-intensive compared to built-in tools. Storing data in a temporary staging area before filtering can lead to inefficiencies in processing and storage. Using a batch processing system for cleaning data is not suitable for real-time processing as it introduces delays and is not efficient for continuous data streams.

Get started with lakehouses in Microsoft Fabric - Training | Microsoft Learn

Question 24 of 50
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

Question 25 of 50
You have a large dataset stored in a Microsoft Fabric Lakehouse, including sales transactions from multiple regions.

You need to implement a strategy to support incremental data loads while maintaining data integrity and consistency.

Which two actions should you perform? Each correct answer presents part of the solution.

Your Answer
Adopt a medallion architecture for data organization.

This answer is correct.
Use Dataflows Gen2 for data transformation and cleaning.

This answer is correct.
Correct Answer
Adopt a medallion architecture for data organization.

This answer is correct.
Use Dataflows Gen2 for data transformation and cleaning.

This answer is correct.
Adopting a medallion architecture for data organization and using Dataflows Gen2 for data transformation and cleaning are both effective strategies for ensuring high data quality and supporting incremental data loads. A medallion architecture organizes data into layers, allowing for efficient incremental loading and ensuring data quality at each stage of the transformation process. Microsoft Dataflows Gen2, based on Power Query, provide a visual and code-free way to transform and clean data, ensuring high data quality before loading into the dimensional model. Loading data directly into the dimensional model without transformation can lead to inconsistencies and poor data quality, which is not suitable for a dimensional model that requires cleansed and conformed data. Using Data Factory pipelines for data transformation is less efficient compared to the automated solutions provided by Dataflows Gen2 and medallion architecture.

Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn
Prepare data for analysis and reporting - Training | Microsoft Learn

Question 26 of 50
You are implementing a data warehouse using Microsoft Fabric.

You plan to integrate data from multiple sources, including Microsoft Azure Data Lake Storage Gen2 and Microsoft SQL Server databases.

You need to design a process to efficiently load data into tables while ensuring data quality and consistency.

Which two tasks should you recommend? Each correct answer presents part of the solution.

Your Answer
Use Azure Synapse Analytics for data integration.

This answer is incorrect.
Use dataflows to ingest and transform data from Azure Data Lake Storage Gen2.

This answer is correct.
Correct Answer
Use Data Factory pipelines for ETL orchestration and T-SQL execution.

This answer is correct.
Use dataflows to ingest and transform data from Azure Data Lake Storage Gen2.

This answer is correct.
Using Microsoft Data Factory pipelines and dataflows are both effective methods for orchestrating ETL processes and transforming data from various sources into a dimensional model. Microsoft Data Factory pipelines allow for complex orchestration and execution of T-SQL scripts, ensuring efficient data transformation and loading. Dataflows offer a low-code solution for data ingestion and transformation using Power Query, making them suitable for integrating data from Microsoft Azure Data Lake Storage Gen2. Using SSIS packages for data integration is less efficient compared to modern tools like Data Factory and dataflows, especially in a Microsoft Fabric environment. While Azure Synapse Analytics is a powerful tool for data analytics and integration, it is not specifically designed for the ETL processes required to transform and load data into a dimensional model.

Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn
Prepare data for analysis and reporting - Training | Microsoft Learn

Question 27 of 50
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

Question 28 of 50
You have a Fabric lakehouse named Lakehouse1 that contains a table named Sales. Sales contains the following columns:

OrderID (INT)
OrderDate (DATE)
ProductID (INT)
Quantity (INT)
You plan to implement incremental loads of new sales records from a CSV file located in the /files/sales/ folder of Lakehouse1.

You need to identify a querying solution for the incremental loads. The solution must minimize maintenance effort.

What should you use?

Your Answer
a notebook

This answer is correct.
Correct Answer
a notebook

This answer is correct.
Notebooks provide flexible, code-based incremental load patterns for Fabric lakehouses; Auto Loader is not available in Fabric, stored procedures aren’t a lakehouse querying solution, and pipelines are orchestration—not querying.

Options to get data into the Fabric Lakehouse

Question 29 of 50
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

Question 30 of 50
Your company has multiple data sources, including Azure Databricks and Azure Cosmos DB.

You plan to integrate the data sources into Microsoft Fabric for unified analytics.

You need to choose the appropriate type of mirroring for each data source to ensure efficient data integration.

Which types of mirroring should you use for Azure Databricks and Azure Cosmos DB?

Your Answer
Database mirroring for both

This answer is incorrect.
Correct Answer
Metadata mirroring for Databricks, database mirroring for Cosmos DB.

This answer is correct.
For efficient data integration into Microsoft Fabric, using metadata mirroring for Azure Databricks is ideal as it allows synchronization of metadata without transferring actual data, aligning with the needs of Databricks. On the other hand, database mirroring is necessary for Azure Cosmos DB to ensure complete data replication, which is crucial for maintaining data integrity across systems. Database mirroring for both would lead to unnecessary data movement for Databricks, while metadata mirroring for both would fail to replicate the necessary data for Cosmos DB.

What is Mirroring in Fabric? - Training | Microsoft Learn

Question 31 of 50
You are implementing a new data analytics solution using Microsoft Fabric.

The data to be ingested includes structured, semi-structured, and unstructured formats from various sources.

You need to select a data store that accommodates diverse data formats and supports both PySpark and SQL operations for data transformation and analysis.

Which two data stores should you select? Each correct answer presents a complete solution.

Your Answer
Azure Data Lake Storage Gen2

This answer is incorrect.
Microsoft Lakehouse

This answer is correct.
Correct Answer
Azure Synapse Analytics

This answer is correct.
Microsoft Lakehouse

This answer is correct.
Azure Synapse Analytics is suitable because it supports all data formats and allows operations using T-SQL and Spark, accommodating the team's diverse skill set and data needs. Microsoft Lakehouse is also appropriate as it supports structured, semi-structured, and unstructured data formats and allows operations using both PySpark and SQL, aligning with the team's skills and data requirements. In contrast, Microsoft Fabric Eventhouse is designed for real-time analytics and supports diverse data formats but is not optimized for batch processing or large-scale data transformation using PySpark and SQL, which are required in this scenario. Azure Data Lake Storage Gen2, while capable of storing diverse data formats, does not natively support PySpark and SQL operations, making it unsuitable for this scenario.

Microsoft Fabric decision guide: choose a data store - Training | Microsoft Learn

Question 32 of 50
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

Question 33 of 50
Your organization uses Microsoft Fabric to process real-time IoT data monitoring environmental conditions. The data includes temperature and humidity readings streamed into a Microsoft KQL database.

You need to ensure efficient data ingestion and near real-time querying for reporting.

What should you do?

Your Answer
Implement Spark Structured Streaming to write data to Delta table.

This answer is correct.
Correct Answer
Implement Spark Structured Streaming to write data to Delta table.

This answer is correct.
Implementing Spark Structured Streaming to write data to a Delta table is effective because it supports efficient ingestion and near real-time querying of streaming data, aligning with the scenario's requirements. Using Azure Stream Analytics for real-time data processing and querying is not suitable as it does not integrate with Microsoft Fabric's KQL database. Storing data in Azure Blob Storage and loading it periodically fails to meet the real-time processing needs. Using Azure Data Explorer for data storage and direct querying is unsuitable as it is not directly integrated with Microsoft Fabric's KQL database.

Work with Delta Lake tables in Microsoft Fabric - Training | Microsoft Learn

Question 34 of 50
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

Question 35 of 50
Your organization is implementing a real-time analytics solution using Microsoft Fabric to process streaming data from IoT devices.

You need to ensure that the streaming data is efficiently processed and accessible for analysis.

Which two actions should you perform? Each correct answer presents part of the solution.

Your Answer
Configure a SQL analytics endpoint.

This answer is correct.
Use Spark Structured Streaming.

This answer is correct.
Correct Answer
Configure a SQL analytics endpoint.

This answer is correct.
Use Spark Structured Streaming.

This answer is correct.
Configuring a SQL analytics endpoint allows querying of the Delta table, providing real-time insights into the streaming data stored in the Microsoft lakehouse. Using Spark Structured Streaming allows for real-time data processing and writing to Delta tables, which are optimized for both batch and streaming data. Setting up a Power BI dataflow might seem like a viable option for data processing, but it is not suitable for real-time streaming data ingestion. Using Azure Stream Analytics might seem like a viable option for real-time data processing, but it is not directly integrated with Microsoft Fabric for this specific use case.

Use delta tables with streaming data - Training | Microsoft Learn
Get streaming data into lakehouse and access with SQL analytics endpoint - Training | Microsoft Learn

Question 36 of 50
Your organization uses Microsoft Fabric for data engineering tasks.

Recently, there have been issues with data pipeline runs failing intermittently, causing delays in data processing.

You need to monitor data pipeline runs to identify the root cause of failures.

What should you do?

Your Answer
Use the Monitoring hub to analyze pipeline run details.

This answer is correct.
Correct Answer
Use the Monitoring hub to analyze pipeline run details.

This answer is correct.
Accessing the Monitoring hub to view and analyze data pipeline run details is the correct approach as it provides insights into the failures, allowing for effective troubleshooting. Using a third-party tool might not provide the same level of integration and detail as the built-in Monitoring hub. Extending timeout settings might lead to inefficiencies without addressing the root cause of the failures. Retrying failed runs without investigation does not solve the underlying issues and can result in repeated failures.

Get started with lakehouses in Microsoft Fabric - Training | Microsoft Learn

Question 37 of 50
Your company has implemented a lakehouse architecture using Microsoft Fabric to support large-scale data analytics.

Data transformation processes must be optimized for performance and reliability.

You need to oversee the data transformation processes to detect any bottlenecks or failures and enhance them accordingly.

What should you do?

Your Answer
Configure alerts for transformation failures.

This answer is correct.
Correct Answer
Configure alerts for transformation failures.

This answer is correct.
Configuring alerts in the Monitor hub is effective because it ensures the team is notified of any data transformation failures, allowing for quick resolution. Enabling detailed logging might help analyze performance but does not directly address monitoring or identifying specific issues. Implementing automated scaling might handle performance fluctuations but does not address monitoring or identifying specific issues. Using basic monitoring tools without advanced configurations is inadequate for effectively overseeing large-scale data transformation processes.

Prepare data for analysis and reporting - Training | Microsoft Learn
Use the Monitor hub - Training | Microsoft Learn

Question 38 of 50
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

Question 39 of 50
Your organization has implemented Microsoft Fabric for data transformation processes.

There have been instances where semantic model refreshes fail without notification, impacting business intelligence reports.

You need to set up alerts to monitor semantic model refresh events and receive notifications upon failures.

Which three actions should you perform? Each correct answer presents part of the solution.

Your Answer
Configure a filter

This answer is correct.
Notify via Teams for all refresh events.

This answer is incorrect.
Use a KQL Queryset to monitor refresh statuses.

This answer is incorrect.
Correct Answer
Configure a filter

This answer is correct.
Select Fabric workspace item events in Real-Time hub.

This answer is correct.
Send an email for alert actions.

This answer is correct.
To monitor semantic model refresh events effectively, selecting Fabric workspace item events in the Real-Time hub allows access to relevant events for monitoring. Sending an email for alert actions ensures immediate notifications upon refresh failures, facilitating quick responses. Filtering based on refresh status isolates failed events, enabling targeted alerts. Using a KQL Queryset to monitor refresh statuses provides data analysis capabilities but lacks real-time alerts. Notifying via Teams for all refresh events does not address the need for failure-specific alerts. Setting alerts for all refresh events without filtering can lead to unnecessary notifications and does not specifically target failure events.

Set alerts on Fabric workspace item events in Real-Time hub - Training | Microsoft Learn

Question 40 of 50
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
You have a Fabric workspace named Workspace1 that contains a notebook named Notebook1.

Each time you attempt to run Notebook1, you receive the following error message: “Your session timed out after inactivity.”

You discover that you can successfully run Notebook1 after manually starting a session on the notebook.

You need to ensure that you can run Notebook1 without manually starting a session. The solution must minimize administrative effort.

What should you do?

Your Answer
Extend the workspace session timeout.

This answer is correct.
Correct Answer
Extend the workspace session timeout.

This answer is correct.
Increasing the workspace session timeout prevents frequent timeouts; the session indicator cannot change timeout; AutoSave doesn’t affect runtime; capacity is already active and unrelated to per-session timeouts.

Fabric notebooks troubleshooting guide

Question 44 of 50
You have a Fabric eventhouse named Eventhouse1.

You discover that after 10 minutes of inactivity, Eventhouse1 automatically suspends and must be reactivated before you can query data.

You need to prevent Eventhouse1 from suspending due to inactivity. The solution must minimize administrative effort and prevent the eventhouse from having to be reactivated manually.

What should you do?

Your Answer
From the ribbon of Eventhouse1, select Always-On, and then from the Always-On pane, select Minimum consumption.

This answer is incorrect.
Correct Answer
From the ribbon of Eventhouse1, select Always-On.

This answer is correct.
An Eventhouse in Microsoft Fabric will automatically suspend after 10 minutes of inactivity unless Always-On is enabled. To prevent suspension and avoid manually reactivating the compute, you must configure the Always-On setting for the eventhouse. In the Fabric UI, this is done from the Eventhouse ribbon by selecting Always-On, and then choosing the appropriate consumption mode. Selecting Minimum consumption ensures the eventhouse stays active while consuming the lowest amount of resources, minimizing administrative effort and controlling cost. Therefore, enabling Always-On and explicitly selecting Minimum consumption is the correct solution because it prevents automatic suspension while maintaining low-cost continuous availability.

Eventhouse overview
Manage and monitor an eventhouse

Question 45 of 50
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

Question 46 of 50
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

Question 47 of 50
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

Question 48 of 50
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

