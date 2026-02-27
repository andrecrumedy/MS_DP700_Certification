Pre AI_Assisted Learning
Question 1 of 50

Your company has set up a Microsoft Fabric lakehouse to store and analyze data from multiple sources, including Azure Event Hubs and local files. The data is used for generating Power BI reports.

You need to implement a loading pattern that supports both full and incremental data loads.

Which approach do you use?

Select only one answer.

Develop a custom ETL tool for data loads.


Use Azure Synapse Analytics for data loads.


Use Data Factory for incremental data loads.


Use Dataflows Gen2 for full and incremental data loads.

This answer is correct.
Using Dataflows Gen2 to implement both full and incremental data loads is the best approach, as it provides the necessary flexibility and efficiency for report generation. Developing a custom ETL tool is unnecessary when existing tools like Dataflows Gen2 can efficiently handle the task. Using Data Factory for incremental data loads might seem viable but does not address the need for both full and incremental data loads. Using Azure Synapse Analytics might seem like a viable option due to its capabilities in handling large-scale data processing, but it does not specifically address the need for both full and incremental data loads in a Microsoft Fabric lakehouse environment.

Get started with lakehouses in Microsoft Fabric - Training | Microsoft Learn

Question 2 of 50

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

Question 3 of 50

Your company experiences performance issues with its current ETL process, which involves loading large volumes of sales data into a fact table in a Microsoft Fabric data warehouse. The process currently uses a full reload strategy, which is time-consuming and resource-intensive.

You need to enhance the ETL process to boost performance and decrease resource usage.

Which two actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Continue full reloads with increased compute resources.


Implement an incremental load strategy.

This answer is correct.

Manually partition the fact table.


Switch to Azure Data Factory for ETL.


Use Change Data Capture (CDC) for tracking changes.

This answer is correct.
Implementing an incremental load strategy is effective because it reduces the amount of data processed during each ETL run, improving performance and reducing resource usage. Using Change Data Capture (CDC) for tracking changes is also beneficial as it allows tracking of changes in the source system, enabling efficient incremental loading of only the modified data into the fact table. Continuing full reloads with increased compute resources may temporarily alleviate performance issues but does not address the inefficiencies of a full reload strategy. Manually partitioning the fact table can improve query performance but does not directly address the inefficiencies in the ETL process itself. Switching to Azure Data Factory for ETL without addressing the full reload strategy may not improve performance.

Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn
Prepare data for analysis and reporting - Training | Microsoft Learn

Question 4 of 50

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

This answer is incorrect.

a stored procedure


Auto Loader

Notebooks provide flexible, code-based incremental load patterns for Fabric lakehouses; Auto Loader is not available in Fabric, stored procedures aren’t a lakehouse querying solution, and pipelines are orchestration—not querying.

Options to get data into the Fabric Lakehouse

Question 6 of 50

A company uses a lakehouse architecture with Microsoft Fabric.

You plan to transform large datasets in Delta format for machine learning.

You need to perform data transformations efficiently using Microsoft Fabric tools.

What should you use?

Select only one answer.

Apache Spark notebooks.

This answer is correct.

Azure Data Factory.


Power BI Dataflows.


SQL Server Management Studio.

Apache Spark notebooks are ideal for processing large-scale data transformations and support the Delta format, making them suitable for this scenario. Power BI Dataflows are often confused with Dataflows Gen2, but they are not designed for large-scale data transformations in a lakehouse environment. Azure Data Factory is a powerful tool for data integration and orchestration but is not specifically designed for direct data transformations within a lakehouse environment using Delta format. SQL Server Management Studio is primarily used for managing SQL databases and is not optimized for large-scale data transformations in a lakehouse environment.

Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn

Question 7 of 50

Your organization uses Microsoft Fabric to manage data from various sources, including Azure SQL Database.

You must continuously replicate Azure SQL Database data into OneLake in an analytics-ready, queryable format. The replication must occur in near real time and must not require complex ETL pipelines.

What should you do?

Select only one answer.

Create a dataflow for continuous data import.


Create a dataflow for periodic data import.


Implement database mirroring.

This answer is correct.

Use Azure Data Factory for continuous data replication.

Implementing database mirroring in Microsoft Fabric is the most suitable solution as it ensures continuous data synchronization into OneLake without the need for complex ETL processes. Creating a dataflow for continuous data import might seem plausible but does not offer the seamless integration and automatic mirroring capabilities of Microsoft Fabric. Using Azure Data Factory for continuous data replication is inappropriate in this context as it is designed for batch processing and ETL tasks rather than real-time continuous replication.

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

You use Microsoft Fabric to manage data across warehouses and lakehouses.

You need to integrate data from a warehouse and a lakehouse into a single table for analysis. The solution must minimize development effort.

What should you use?

Select only one answer.

Azure Data Factory


The CREATE TABLE AS SELECT (CTAS) statement.

This answer is correct.

Dataflow Gen2

This answer is incorrect.

The SELECT INTO statement.

The CREATE TABLE AS SELECT (CTAS) statement is the best choice for integrating data from a warehouse and a lakehouse into a single table, as it allows the creation of a new table based on combined data. Dataflow Gen2, while useful for data preparation and transformation, does not directly support creating new tables from combined data sources. The SELECT INTO statement can create a new table but is not suitable for integrating data from multiple sources. Azure Data Factory is a data integration service that might seem suitable for integrating data from multiple sources, but it does not directly support creating tables from combined data sources in a warehouse or lakehouse.

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

The COPY statement with Shared Access Signature efficiently ingests batch data from Azure Blob Storage into a warehouse due to its direct and secure data transfer capabilities. In contrast, a Data Factory pipeline requires manual configuration, making it less efficient. Dataflows Gen2 focus on data preparation and transformation, which does not align with the task of batch data ingestion. Azure Synapse Analytics is not designed for efficient batch data ingestion using Microsoft Fabric tools.

Load data using T-SQL - Training | Microsoft Learn

Question 11 of 50

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

Question 12 of 50

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

Question 13 of 50

You process streaming data from various sources using Microsoft Fabric, requiring transformation and storage in a lakehouse for analytics.

You need to select a method for effective transformation and storage of streaming data.

Which method should you choose?

Select only one answer.

Azure Data Factory for real-time data integration


Azure Stream Analytics for real-time processing.


Azure Synapse Analytics for transformation and storage.


Spark Structured Streaming with Delta tables.

This answer is correct.
Spark Structured Streaming with Delta tables is the most effective method for transforming and storing streaming data in real-time, utilizing Delta Lake's features for ACID transactions and scalability. Azure Stream Analytics is not suitable as it focuses on real-time processing rather than batch processing. Azure Data Factory lacks the necessary real-time processing capabilities, making it more appropriate for batch integrations. Azure Synapse Analytics, while powerful, is not specifically designed for real-time streaming data transformation and storage in a lakehouse, rendering it an inappropriate choice for this scenario.

Use delta tables with streaming data - Training | Microsoft Learn
Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn

Question 14 of 50

Your organization uses Microsoft Fabric to process streaming data from IoT devices.

You need to transform the streaming data in real-time for analysis.

What should you use?

Select only one answer.

Azure Data Factory for data orchestration.


Azure Event Hubs for real-time data ingestion.


Azure Stream Analytics for real-time processing.


Spark Structured Streaming with Delta tables.

This answer is correct.
Spark Structured Streaming with Delta tables is the most suitable solution for real-time data ingestion and transformation due to its ability to efficiently handle streaming data while maintaining data integrity through ACID transactions. Azure Stream Analytics, although capable of real-time processing, does not offer the same level of integration and transformation capabilities. Azure Data Factory is intended for data orchestration and lacks the necessary features for real-time data ingestion and transformation. Azure Event Hubs is designed for real-time data ingestion but does not provide the transformation capabilities needed for real-time analysis.

Use delta tables with streaming data - Training | Microsoft Learn
Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn

Question 14 of 50

Your organization uses Microsoft Fabric to process streaming data from IoT devices.

You need to transform the streaming data in real-time for analysis.

What should you use?

Select only one answer.

Azure Data Factory for data orchestration.


Azure Event Hubs for real-time data ingestion.


Azure Stream Analytics for real-time processing.


Spark Structured Streaming with Delta tables.

This answer is correct.
Spark Structured Streaming with Delta tables is the most suitable solution for real-time data ingestion and transformation due to its ability to efficiently handle streaming data while maintaining data integrity through ACID transactions. Azure Stream Analytics, although capable of real-time processing, does not offer the same level of integration and transformation capabilities. Azure Data Factory is intended for data orchestration and lacks the necessary features for real-time data ingestion and transformation. Azure Event Hubs is designed for real-time data ingestion but does not provide the transformation capabilities needed for real-time analysis.

Use delta tables with streaming data - Training | Microsoft Learn
Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn

Question 16 of 50

Your company is transitioning to a data mesh architecture using Microsoft Fabric.

You are responsible for organizing data into domains.

You need to configure settings for independent management of rules and restrictions by each business unit.

What should you do?

Select only one answer.

Assign workspaces to multiple domains.


Configure domain-specific sensitivity labels.


Create workspaces with shared governance settings.


Delegate tenant-level settings to domains.

This answer is correct.
Delegating tenant-level settings to the domain level allows each business unit to manage its own governance settings, which is essential for implementing a data mesh architecture. Assigning workspaces to multiple domains complicates governance and does not support independent management. Creating workspaces with shared governance settings centralizes control and does not facilitate domain-specific governance. Configuring domain-specific sensitivity labels is related to governance but does not address the need for independent management of rules and restrictions by each business unit.

Prepare to use Apache Spark - Training | Microsoft Learn
Implement row-level security - Training | Microsoft Learn

Question 17 of 50

Your company uses Microsoft Fabric for data engineering workflows.

You notice that Spark jobs are slow due to suboptimal resource allocation.

You need to enhance the Spark job efficiency by adjusting environment settings.

What should you do?

Select only one answer.

Enable dynamic allocation of executors.

This answer is correct.

Increase the number of partitions.


Set a fixed memory allocation for executors.


Set a fixed number of nodes.

Enabling dynamic allocation of executors in the Spark environment settings is beneficial because it allows the system to adjust resources based on the workload, thereby improving efficiency. Setting a fixed number of nodes or a fixed memory allocation for executors can lead to inefficient resource usage as they do not adapt to varying workloads. Increasing the number of partitions is a common misconception that it will improve job efficiency, but it can lead to overhead and not necessarily enhance resource allocation.

Prepare to use Apache Spark - Training | Microsoft Learn
Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn

Question 18 of 50

Your organization uses Microsoft Fabric to manage data engineering tasks. The current setup includes a starter pool for Apache Spark jobs.

You notice that some jobs require more compute resources than the starter pool can provide.

You need to optimize the workspace configuration to efficiently handle larger Spark jobs without significantly increasing session start times.

Which two actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Create a custom Spark pool with autoscaling.

This answer is correct.

Disable the starter pool.

This answer is incorrect.

Enable dynamic allocation of executors.

This answer is correct.

Increase executor memory in the starter pool.


Increase the number of partitions in the Spark job.

Creating a custom Spark pool with autoscaling allows for specifying node sizes and enabling dynamic resource allocation, which is essential for handling larger Spark jobs. Enabling dynamic allocation of executors further optimizes resource usage by adjusting the number of executors based on workload demands. Disabling the starter pool without a custom pool reduces available resources, while increasing executor memory in the starter pool lacks the dynamic aspect needed for efficient resource management. Increasing the number of partitions does not address the core issue of managing larger Spark jobs.

Prepare to use Apache Spark | Microsoft Learn

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


Use full deployment to update all settings.

Creating a deployment rule for the Production stage is essential to ensure the production database connection remains intact during deployments. Using deployment pipelines to manage database connections is a common misconception, as they are not specifically designed for this purpose. Using a script to update the database connection can introduce complexity and potential errors if not managed properly. Full deployment updates all content but does not specifically address the need to maintain certain settings, such as database connections.

Get started with deployment pipelines - Training | Microsoft Learn

Question 21 of 50

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

Question 22 of 50

You have a table named CustomerInfo table that contains the following columns: CustomerID, Name, Address, and CreditCardNumber.

You need to apply a mask to the CreditCardNumber column to comply with the data governance policy.

What should you do?

Select only one answer.

ALTER TABLE CustomerInfo ALTER COLUMN CreditCardNumber ADD MASKED WITH (FUNCTION = 'default()');


ALTER TABLE CustomerInfo ALTER COLUMN CreditCardNumber ADD MASKED WITH (FUNCTION = 'partial(0,"XXXX-XXXX-XXXX-",4)');

This answer is correct.

CREATE VIEW MaskedCustomerInfo AS SELECT CustomerID, Name, Address, 'XXXX-XXXX-XXXX-XXXX' AS CreditCardNumber FROM CustomerInfo;


CREATE VIEW PublicCustomerInfo AS SELECT CustomerID, Name, Address, CreditCardNumber FROM CustomerInfo;

The SQL statement to add a partial mask to the CreditCardNumber column effectively complies with the data governance policy by displaying only the last four digits, which is a standard practice for credit card masking. Adding a default mask would not provide the necessary partial masking. Creating a view with static masked values fails to provide dynamic masking based on user permissions, which is necessary for compliance. Creating a view without applying any masking does not protect the data.

How to implement dynamic data masking in Fabric Data Warehouse - Training | Microsoft Learn
Dynamic data masking in Fabric data warehousing - Training | Microsoft Learn

Question 23 of 50

Your company uses a Microsoft Fabric data warehouse to store employee salary information.

You need to configure permissions so that only specific users can view unmasked salary data while others see masked data.

Which permission should you grant to the authorized users?

Select only one answer.

Grant ALTER ANY MASK permission.


Grant SELECT permission.


Grant UNMASK permission.

This answer is correct.

Grant VIEW DEFINITION permission.

Granting the UNMASK permission is essential as it specifically allows authorized users to view unmasked data in columns where dynamic data masking is applied, meeting the requirement to differentiate access levels. The ALTER ANY MASK permission enables modification of masking rules but does not permit viewing unmasked data, making it unsuitable for this task. The VIEW DEFINITION permission allows users to view metadata about database objects but does not grant access to view unmasked data, thus failing to meet the objective. The SELECT permission facilitates data querying but does not override masking, failing to meet the objective of allowing access to unmasked data.

Explore dynamic data masking - Training | Microsoft Learn
Dynamic data masking in Fabric data warehousing - Training | Microsoft Learn

Question 24 of 50

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

Question 25 of 50

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

Question 26 of 50

Your organization uses Microsoft Fabric for data warehouse management. The security team is concerned about unauthorized access to sensitive customer information in a database.

You need to ensure sensitive data is protected and accessible only to authorized users.

Which three actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Define dynamic data masking for sensitive columns.

This answer is correct.

Grant UNMASK permission to authorized users.

This answer is correct.

Remove all masking rules from a database.


Revoke SELECT permission from non-privileged users.

This answer is incorrect.

Test masking with a non-privileged user.

This answer is correct.
Defining dynamic data masking for sensitive columns ensures that unauthorized users cannot view sensitive information, aligning with the security objective. Granting UNMASK permission to authorized users allows them to access unmasked data, maintaining controlled access. Testing masking with a non-privileged user confirms the effectiveness of the masking rules, ensuring they work as intended. Removing all masking rules would expose sensitive data, contradicting the goal of protecting it. Revoking SELECT permission from non-privileged users is impractical as it restricts access to all data, not just sensitive information.

Security for data warehousing in Microsoft Fabric - Training | Microsoft Learn
How to implement dynamic data masking in Fabric Data Warehouse - Training | Microsoft Learn

 
Question 27 of 50

Your organization uses Microsoft Fabric for data warehousing.

The data contains sensitive customer information such as email addresses and credit card numbers.

You need to implement a security solution to mask sensitive data in real-time without altering the data structure.

What should you do?

Select only one answer.

Apply column-level security to restrict access to specific columns.


Create a separate database for sensitive information.


Implement Dynamic Data Masking on sensitive columns.

This answer is correct.

Implement Transparent Data Encryption (TDE).


Use encryption to mask sensitive data in real-time.

To protect sensitive data without altering the database structure, implementing Dynamic Data Masking and applying column-level security are both necessary. Dynamic Data Masking provides real-time masking, which is essential for safeguarding email and credit card information. Column-level security ensures that only authorized users can access specific columns, adding an extra layer of protection. Creating a separate database does not fulfill the requirement for real-time masking within the existing structure. Implementing Transparent Data Encryption (TDE), while protective, does not offer the real-time masking or selective access control required. Encryption is not applicable as it secures data at rest and in transit, not during query results.

Secure a Microsoft Fabric data warehouse - Training | Microsoft Learn

Question 28 of 50

Your company uses Dynamic Data Masking (DDM) in its Microsoft Fabric SQL database to protect sensitive customer information, including Email, PhoneNumber, and CreditCardNumber fields.

You need to configure DDM so nonprivileged users see masked versions of these fields.

Which masking function should you apply to the CreditCardNumber field?

Select only one answer.

default()


email()


partial(0,"XXXX-XXXX-XXXX-",4)

This answer is correct.

random(1000,9999)

Applying the 'partial(0,"XXXX-XXXX-XXXX-",4)' function is the most appropriate choice for masking credit card numbers, as it allows specific parts of the data to be visible while masking the rest. The 'default()' function would hide all data, which is not desired here. The 'email()' function is inappropriate for credit card numbers, and the 'random()' function is not suitable as it replaces them with random values.

Explore dynamic data masking - Training | Microsoft Learn

Question 29 of 50

You have a Fabric workspace named Workspace1 that contains a lakehouse named Lakehouse1 and a user named User1.

User1 is assigned the Contributor workspace role for Workspace1.

You discover that User1 is consuming more resources than expected. You remove User1 from Workspace1. User1 now requires read-only access to the data in Lakehouse1.

You need to ensure that User1 can read the data in Lakehouse1. The solution must follow the principle of least privilege.

What should you do?

Select only one answer.

Assign User1 the Contributor workspace role for Workspace1.


Assign User1 the Member workspace role for Workspace1.


Assign User1 the Viewer workspace role for Workspace1.


Configure item permissions for Lakehouse1.

This answer is correct.
Item-level permissions on Lakehouse1 grant access only to that item, adhering to least privilege; workspace roles (Viewer, Member, Contributor) grant broader access to all workspace items.

Configure workspace and item permissions

Question 30 of 50

Your company uses a lakehouse architecture with Microsoft Fabric for analytics. Data is ingested and transformed using Microsoft Data Factory pipelines and stored in Delta tables.

You need to enhance data transformation efficiency and reduce loading time.

What should you do?

Select only one answer.

Configure Spark pool with more worker nodes.


Enable Delta Lake optimization.

This answer is incorrect.

Switch to a different Spark runtime version.


Use session tags to reuse Spark sessions.

This answer is correct.
Using session tags to reuse existing Microsoft Spark sessions minimizes startup time and enhances the efficiency of data transformation processes. Configuring the Microsoft Spark pool to use more worker nodes might seem beneficial for handling more tasks but does not directly improve transformation efficiency. Switching to a different Spark runtime version does not inherently minimize transformation time compared to optimized Spark execution. Enabling Delta Lake optimization is more about data storage and management rather than transformation efficiency.

Transform data by running a notebook - Training | Microsoft Learn

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

Question 32 of 50

Your organization uses Microsoft Fabric to manage data pipelines for various ETL processes.

You need to create a flexible and reusable pipeline that handles different datasets by using parameters and expressions.

What should you do?

Select only one answer.

Create separate pipelines for each dataset.


Hardcode dataset values and use static expressions.


Use only default values for dataset changes.


Use parameters and string interpolation for dynamic content.

This answer is correct.
Using parameters and string interpolation in the pipeline provides the necessary flexibility and reusability for handling different datasets. Creating separate pipelines for each dataset increases maintenance overhead, while hardcoding dataset values and using static expressions make the pipeline inflexible. Relying solely on default values does not offer the required flexibility for dynamic dataset handling.

Parameters for Data Factory in Microsoft Fabric - Training | Microsoft Learn

Question 33 of 50

Your organization uses Microsoft Fabric for managing data pipelines in a large-scale ETL process. The current setup involves multiple pipelines triggered by specific events and schedules, facing challenges with hard-coded values.

You need to implement dynamic parameterization to enhance flexibility and reduce maintenance.

Which two settings should you configure? Each correct answer presents part of the solution.

Select all answers that apply.

Hard-code values in the configuration.


Pass external values using pipeline parameters.

This answer is correct.

Use dynamic expressions for runtime evaluation.

This answer is correct.

Use static triggers for pipeline execution.


Use static values in expressions.

Hard-coding values in the configuration contradicts the goal of reducing maintenance overhead and increasing flexibility. Using dynamic expressions for runtime evaluation allows parameter values to be evaluated at runtime, providing the flexibility needed to adapt to different scenarios without changing the pipeline code. Using static values in expressions does not provide the flexibility needed for dynamic parameterization. Using static triggers for pipeline execution does not provide the flexibility required for dynamic parameterization. Passing external values using pipeline parameters allows you to pass external values into the pipelines, making them more flexible and reducing the need for hard-coded values.

Load data using T-SQL - Training | Microsoft Learn
Parameters for Data Factory in Microsoft Fabric - Training | Microsoft Learn

Question 34 of 50

Your organization uses Microsoft Fabric for managing data pipelines in a large-scale ETL process. The setup involves multiple pipelines that must handle different datasets dynamically, reducing hardcoding and improving maintainability.

You need to reuse pipeline components with varying inputs during execution.

Which two settings should you configure? Each correct answer presents part of the solution.

Select all answers that apply.

Hardcode dataset paths.


Pass external values as parameters.

This answer is correct.

Use fixed dataset configurations.


Use string interpolation.

This answer is correct.
Hardcoding dataset paths does not support dynamic execution and requires manual changes for each dataset, which is inefficient. Using string interpolation is effective as it allows the construction of dynamic expressions by incorporating parameter values, facilitating the handling of various datasets. Passing external values as parameters is crucial for dynamic execution, as it enables the pipeline to adapt to different datasets without hardcoding. Fixed dataset configurations are unsuitable because they lack the flexibility needed for runtime changes, failing to meet the dynamic requirements of the scenario.

Load data using T-SQL - Training | Microsoft Learn
Parameters for Data Factory in Microsoft Fabric - Training | Microsoft Learn
Expressions and functions for Data Factory in Microsoft Fabric - Training | Microsoft Learn

Question 35 of 50

You have a pipeline in a Fabric workspace.

You need to configure the pipeline to run automatically once per day.

Which type of trigger should you use?

Select only one answer.

custom events />


schedule

This answer is correct.

storage events


tumbling window

Schedule triggers run pipelines on a defined cadence (daily/hourly); custom events trigger on specific events, tumbling windows are interval-based but not simply “once per day”, and storage events react to storage changes.

Run, schedule, or use events to trigger a pipeline

Question 36 of 50

Your company has implemented a lakehouse architecture using Microsoft Fabric to support large-scale data analytics.

Data transformation processes must be optimized for performance and reliability.

You need to oversee the data transformation processes to detect any bottlenecks or failures and enhance them accordingly.

What should you do?

Select only one answer.

Configure alerts for transformation failures.

This answer is correct.

Enable detailed logging for performance analysis.


Implement automated scaling for transformation processes.


Use basic monitoring tools without advanced configurations.

Configuring alerts in the Monitor hub is effective because it ensures the team is notified of any data transformation failures, allowing for quick resolution. Enabling detailed logging might help analyze performance but does not directly address monitoring or identifying specific issues. Implementing automated scaling might handle performance fluctuations but does not address monitoring or identifying specific issues. Using basic monitoring tools without advanced configurations is inadequate for effectively overseeing large-scale data transformation processes.

Prepare data for analysis and reporting - Training | Microsoft Learn
Use the Monitor hub - Training | Microsoft Learn

Question 37 of 50

Your organization uses Microsoft Fabric to manage and monitor various data activities, including data pipelines, dataflows, and semantic models.

Recently, issues with data ingestion processes failing intermittently have caused delays in data availability for reporting.

You need to determine the cause of these failures and ensure effective monitoring of data ingestion processes to prevent future disruptions.

What should you do?

Select only one answer.

Enable alerts only for non-critical issues.


Increase data ingestion frequency.


Use a basic logging tool for monitoring.


Use the Monitor hub to filter activities by status and start time.

This answer is correct.
Using the Monitor hub to filter activities by status and start time is effective because it helps identify patterns in failures, aiding in diagnosing the root cause. Enabling alerts only for non-critical issues can result in missing critical alerts, making it harder to monitor and address them. Increasing the frequency of data ingestion does not address the root cause and leads to more frequent disruptions. Using a basic logging tool might seem like a viable option, but it lacks the advanced features needed for effective monitoring in complex environments like Microsoft Fabric.

Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn
Prepare data for analysis and reporting - Training | Microsoft Learn

Question 38 of 50

Your organization uses Microsoft Fabric to manage and analyze large datasets.

Recently, issues with data ingestion processes fail intermittently, causing delays in data availability for analysis.

You need to implement a strategy to detect patterns or recurring issues in data ingestion activities.

Which two actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Analyze error logs for past ingestion activities.

This answer is incorrect.

Configure alerts for future ingestion failures.

This answer is correct.

Filter activities by status to identify failures.

This answer is correct.

Increase the frequency of data ingestion checks.


Remove all filters to view all activities.

Configuring alerts for future ingestion failures ensures immediate notification and timely intervention, making it a proactive monitoring approach. Filtering activities by status in the Monitor hub allows for quick identification of failed ingestion processes, directly addressing the need to monitor and resolve issues. Analyzing error logs might seem useful for identifying patterns, but it does not address the immediate need to monitor and resolve failures effectively. Removing all filters could lead to information overload, making it difficult to focus on specific failed activities.

Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn
Prepare data for analysis and reporting - Training | Microsoft Learn

Question 39 of 50

You have a Fabric workspace named Workspace1.

In Workspace1, you create a lakehouse named Lakehouse1.

You plan to ingest data into Lakehouse1.

You need to monitor the data ingestion process.

What should you use?

Select only one answer.

Monitor hub/>

This answer is correct.

the Fabric Capacity Metrics Power BI app


the query insights view for Lakehouse1


the query insights view for Workspace1

Monitor hub tracks ingestion and transformation activities; query insights target data warehouse queries, and capacity metrics focus on capacity usage rather than ingestion details.

Introduction

Question 40 of 50

Your organization uses Microsoft Fabric for data workflows.

You notice that some data transformations are not completing, causing delays.

You need to ensure that you receive immediate alerts for data processing issues.

What should you do?

Select only one answer.

Increase data refresh frequency.


Set up a dashboard in Power BI.


Set up a weekly report for transformation logs.


Set up notifications for transformation events in Microsoft Fabric.

This answer is correct.
Setting up notifications for transformation events in Microsoft Fabric is the most effective solution as it provides immediate alerts, allowing quick response to issues. Increasing data refresh frequency does not address underlying transformation issues and leads to additional resource consumption. Setting up a weekly report for transformation logs lacks the real-time aspect needed for prompt action, and setting up a dashboard in Power BI provides insights but does not offer real-time alerts for immediate action.

Set alerts on Fabric workspace item events in Real-Time hub - Training | Microsoft Learn

Question 41 of 50

You have a Dataflow Gen2 dataflow in Fabric that uses an on-premises data gateway.

You discover that a refresh fails after running for approximately one hour.

You need to troubleshoot the cause of the failure.

What should you do first?

Select only one answer.

Verify the maximum parameters per pipeline. />


Verify the maximum queued runs per pipeline.


Verify the maximum timeout for pipeline activity runs.


Verify the version of the on-premises data gateway.

This answer is correct.
Gateway version issues commonly cause long-running refresh failures; pipeline timeouts, queued runs, and parameter limits relate to pipelines, not Dataflows Gen2 refresh via gateway.

Data Factory limitations overview

Question 42 of 50

Your company has implemented a SQL database in Microsoft Fabric to handle large-scale data analytics.

Users report slow query performance during peak hours.

You need to implement a solution that optimizes query performance automatically without manual intervention.

What should you do?

Select only one answer.

Enable automatic tuning.

This answer is correct.

Enable manual index management.


Enable query caching.


Enable resource governance policies.

Enabling automatic tuning allows the system to adapt to workload changes and optimize query performance without manual intervention. Enabling query caching might seem beneficial but does not directly optimize query execution automatically. Enabling manual index management requires ongoing oversight and does not align with the goal of optimization without manual intervention. Enabling resource governance policies can help manage resources and improve performance indirectly but does not directly optimize query performance automatically without manual intervention.

Configure SQL granular permissions using T-SQL - Training | Microsoft Learn

Question 43 of 50

You have a Fabric workspace named Workspace1 that contains a notebook named Notebook1.

Each time you attempt to run Notebook1, you receive the following error message: “Your session timed out after inactivity.”

You discover that you can successfully run Notebook1 after manually starting a session on the notebook.

You need to ensure that you can run Notebook1 without manually starting a session. The solution must minimize administrative effort.

What should you do?

Select only one answer.

Ask a Fabric administrator to resume capacity. />


Extend the workspace session timeout.

This answer is correct.

From the Edit menu, turn on AutoSave.


From the Session ready indicator, update the session timeout duration.

This answer is incorrect.
Increasing the workspace session timeout prevents frequent timeouts; the session indicator cannot change timeout; AutoSave doesn’t affect runtime; capacity is already active and unrelated to per-session timeouts.

Fabric notebooks troubleshooting guide

Question 44 of 50

You have a Fabric eventhouse named Eventhouse1.

You discover that after 10 minutes of inactivity, Eventhouse1 automatically suspends and must be reactivated before you can query data.

You need to prevent Eventhouse1 from suspending due to inactivity. The solution must minimize administrative effort and prevent the eventhouse from having to be reactivated manually.

What should you do?

Select only one answer.

Configure an eventstream to continuously send data to Eventhouse1./>


From the ribbon of Eventhouse1, select Always-On, and then from the Always-On pane, select Minimum consumption.

This answer is incorrect.

From the ribbon of Eventhouse1, select Always-On.

This answer is correct.

From the ribbon of Eventhouse1, select Minimum consumption.

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

Select only one answer.

Add a BEGIN TRANSACTION statement to the TRY block.

This answer is correct.

Move the COMMIT TRANSACTION statement to the CATCH block.


Remove the COMMIT TRANSACTION statement.


Remove the ROLLBACK TRANSACTION statement.

This answer is incorrect.
Adding a BEGIN TRANSACTION at the start of the TRY block ensures that the INSERT executes inside an explicit transaction and allows COMMIT TRANSACTION to succeed when no errors occur. The code currently attempts to commit a transaction that was never started, so the insert silently fails. Moving the COMMIT statement to the CATCH block is incorrect because COMMIT should only occur when no exception is thrown, and the CATCH block should handle rollbacks rather than commits. Removing the COMMIT statement would leave an open transaction and violate proper transaction handling, while removing the ROLLBACK would break error handling by preventing cleanup when an exception occurs.

Implement structured exception handling

RAISERROR (Transact-SQL)

Handle errors in transactions

Question 46 of 50

Your company has an eventstream using Microsoft Fabric to process real-time data from various sources.

You notice that frequent runtime errors affect data processing.

You need to ensure smooth data processing by identifying and resolving runtime errors.

Which three actions should be perform? Each correct answer presents part of the solution.

Select all answers that apply.

Check Data insights for event metrics.

This answer is correct.

Disable eventstream data transformation.


Filter logs by error severity.

This answer is correct.

Modify data transformation logic.


Review Runtime logs for error details.

This answer is correct.
Reviewing Runtime logs provides detailed error information, essential for diagnosing issues. Checking Data insights helps identify performance bottlenecks or issues. Filtering logs by severity allows prioritization of critical errors, ensuring they are addressed promptly. Modifying data transformation logic might seem like a way to address errors, but it does not resolve the actual problem. Increasing the eventstream node count does not directly address the root cause of runtime errors.

Monitoring status and performance of an eventstream - Training | Microsoft Learn

Question 47 of 50

Your company is using Microsoft Fabric to manage data pipelines for a lakehouse solution.

You notice that a pipeline failed due to a script activity error.

You need to ensure that the pipeline execution fails with a customized error message and code.

Which two actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Add a Fail activity.

This answer is correct.

Configure custom error settings in the Fail activity.

This answer is correct.

Enable logging for pipeline activities.


Use a Try-Catch activity.

To ensure that a pipeline reports a custom error message and code when a script activity fails, adding a Fail activity to the pipeline and configuring its settings with the desired error message and code are essential steps. The Fail activity is specifically designed for this purpose, making these actions correct. Using a Try-Catch activity is a common misconception as it is not applicable in this context, and enabling logging does not address the error reporting requirement, making them incorrect choices.

Use the Fail activity to cause pipeline execution to fail with a customized error message and error code - Training | Microsoft Learn

Question 48 of 50

Your company uses Microsoft Fabric to manage large-scale data processing tasks.

You notice performance issues with Spark jobs involving complex transformations and aggregations on Delta format data.

You need to enhance performance of these Spark jobs without modifying the existing codebase.

What should you do?

Select only one answer.

Enable adaptive query execution.


Enable dynamic allocation.


Enable high concurrency mode.


Enable native execution engine.

This answer is correct.
Enabling native execution engine in environment settings optimizes performance for complex Spark jobs without code modifications. Enabling dynamic allocation can lead to resource inefficiencies and does not directly enhance performance for complex transformations and aggregations. Enabling high concurrency mode allows multiple users to share Spark sessions, but it does not directly enhance performance for complex transformations and aggregations. Enabling adaptive query execution is a common consideration for optimizing Spark job performance, but it does not directly address the specific performance issues related to complex transformations and aggregations on Delta format data.

Load data using T-SQL - Training | Microsoft Learn

Question 49 of 50

Your company uses Microsoft Fabric to manage a large-scale data lakehouse containing numerous Delta tables. The tables are frequently updated and queried by various analytics teams.

You notice that query performance has degraded over time, leading to increased processing times and higher costs.

You need to recommend maintenance strategies to enhance the efficiency of Delta tables in a lakehouse.

Which three actions should you recommend? Each correct answer presents part of the solution.

Select all answers that apply.

Apply V-Order.

This answer is correct.

Enable Delta caching.


Use the OPTIMIZE command

This answer is correct.

Reduce the retention period.


Use the VACUUM command.

This answer is correct.
Applying V-Order optimizes sorting, encoding, and compression of Delta Parquet files, enhancing read operations and maintaining efficient query performance. Performing bin-compaction consolidates small Parquet files into larger ones, improving read efficiency and reducing the number of files scanned during queries. Using the VACUUM command removes old files, optimizing storage costs and potentially improving query performance by reducing clutter. Reducing the retention period might seem beneficial for performance but can lead to data loss and compromise Delta's time travel capabilities. Enabling Delta caching might seem beneficial for performance but can lead to increased memory usage and potential performance degradation if not managed properly.

Use table maintenance feature to manage delta tables in Fabric - Training | Microsoft Learn

Question 50 of 50

Your company has implemented a Microsoft Fabric data warehouse to handle large-scale data ingestion and processing.

The current setup involves frequent data loads throughout the day, which sometimes lead to performance bottlenecks.

You need to optimize the data ingestion process to handle large volumes efficiently without causing performance issues.

Which two actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Divide large INSERT operations into smaller parts.

This answer is correct.

Group INSERT statements into batches.

This answer is correct.

Use larger data types for columns.


Use smaller data types for columns.

Grouping INSERT statements into batches reduces transaction overhead, thereby improving performance during data ingestion. Dividing large INSERT operations into smaller parts minimizes rollback time and enhances system responsiveness, making it an effective strategy for handling large data volumes. Using smaller data types for columns can lead to data truncation or loss if not carefully considered, which is counterproductive to the goal of optimizing data ingestion.

Performance guidelines in Fabric Data Warehouse - Training | Microsoft Learn

Practice Assessment Results: February 25, 2026

Practice Assessment for Exam DP-700: Implementing Data Engineering Solutions Using Microsoft Fabric

It took you 24 minutes to complete this assessment.

Overall Results
To be better prepared for the exam, aim to achieve a score of 80% or higher in multiple attempts.

Score: 78%

Performance by assessment section
To further strengthen your skills in the following areas, refer to the Customized Learning Material section below.

Implement and manage an analytics solution

Ingest and transform data

Monitor and optimize an analytics solution

Customized learning material to improve your skills
Because you scored lower in "Implement and manage an analytics solution":

Implement continuous integration and continuous delivery (CI/CD) in Microsoft Fabric
46 mins
Because you scored lower in "Monitor and optimize an analytics solution":

Monitor activities in Microsoft Fabric
50 mins
