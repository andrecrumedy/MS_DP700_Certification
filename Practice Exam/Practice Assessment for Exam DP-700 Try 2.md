Question 1 of 50

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

Question 2 of 50

Your organization uses Microsoft Fabric for data engineering.

You notice delays with Apache Spark jobs due to high demand on shared resources.

You need to optimize the Spark job execution time by configuring a custom Spark pool.

What should you do?

Select only one answer.

Create a custom Spark pool with autoscaling enabled and set the maximum nodes based on peak load.

This answer is correct.

Create a custom Spark pool with static node allocation.


Enable static allocation of executors.


Use a custom Spark pool with a fixed number of nodes.

Creating a custom Spark pool with autoscaling enabled and setting the maximum number of nodes based on expected peak load is effective because it allows the system to dynamically adjust resources according to demand, ensuring efficient job execution. Enabling static allocation of executors or nodes would lead to inefficient resource usage, as it fails to adapt to varying workloads. Increasing the node size of the existing starter pool is not feasible since the node size is predefined and cannot be modified. Using a custom Spark pool with a fixed number of nodes does not address the core issue of resource contention and may result in inefficient resource usage.

Prepare to use Apache Spark - Training | Microsoft Learn
Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn

Question 3 of 50

Your organization is implementing a data mesh architecture using Microsoft Fabric.

The IT department plans to delegate governance controls to business units.

You need to configure settings for independent data management by business units.

Which three actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Assign domain-specific sensitivity labels.


Assign workspaces to domains.

This answer is correct.

Delegate tenant settings to domains.

This answer is correct.

Enable domain-level sensitivity labels.

This answer is incorrect.

Implement row-level security.


Specify domain administrators.

This answer is correct.
Assigning workspaces to specific domains ensures that all data within those workspaces is governed by the domain's rules and restrictions. Delegating tenant-level settings to the domain level allows each business unit to define its own rules and restrictions, enabling domain-specific governance. Specifying domain admins allows for effective management of domain settings and ensures that domain-specific governance is enforced. Implementing row-level security is a common data governance practice, but it does not directly enable domain-level governance in a data mesh architecture. Assigning domain-specific sensitivity labels is related to data protection but does not directly enable independent data management by business units.

Fabric domains | Microsoft Learn

Question 3 of 50

Your organization is implementing a data mesh architecture using Microsoft Fabric.

The IT department plans to delegate governance controls to business units.

You need to configure settings for independent data management by business units.

Which three actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Assign domain-specific sensitivity labels.


Assign workspaces to domains.

This answer is correct.

Delegate tenant settings to domains.

This answer is correct.

Enable domain-level sensitivity labels.

This answer is incorrect.

Implement row-level security.


Specify domain administrators.

This answer is correct.
Assigning workspaces to specific domains ensures that all data within those workspaces is governed by the domain's rules and restrictions. Delegating tenant-level settings to the domain level allows each business unit to define its own rules and restrictions, enabling domain-specific governance. Specifying domain admins allows for effective management of domain settings and ensures that domain-specific governance is enforced. Implementing row-level security is a common data governance practice, but it does not directly enable domain-level governance in a data mesh architecture. Assigning domain-specific sensitivity labels is related to data protection but does not directly enable independent data management by business units.

Fabric domains | Microsoft Learn

Question 4 of 50

Your organization uses Microsoft Fabric for data engineering.

You notice Microsoft Spark job failures due to incompatible library versions after updating a Spark runtime.

You need to resolve compatibility issues causing Microsoft Spark job failures.

Which two actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Adjust Spark executor memory settings.


Republish environment after removing incompatible libraries.

This answer is correct.

Revert to a previous Spark runtime version.


Update library versions to match new Spark runtime.

This answer is correct.

Use an outdated library version.

To resolve compatibility issues causing Microsoft Spark job failures, it is essential to republish the environment after removing incompatible libraries. This ensures only compatible configurations are applied, preventing job failures. Additionally, updating library versions to match new Microsoft Spark runtime requirements is crucial as it aligns libraries with the updated runtime, ensuring all dependencies are met. Using an outdated library version does not resolve compatibility issues, and adjusting Spark executor memory settings does not solve incompatible libraries causing job failures. Reverting to a previous Spark runtime version might seem like a solution, but it does not address the root cause of library compatibility issues after an update.

Create, configure, and use an environment in Fabric | Microsoft Learn

Question 5 of 50

You have a Fabric domain named Domain1 that contains a subdomain named Subdomain1.

You have a workspace named Workspace1 that is assigned to Domain1.

You plan to assign Workspace1 to Subdomain1.

You need to ensure that Workspace1 is assigned to the subdomain without changing its domain assignment.

What should you do from the Fabric admin portal?

Select only one answer.

Edit the Domain settings.


Edit the Subdomain settings.


Edit the Workspace settings.

This answer is correct.

Move the workspace to a new domain and reassign the subdomain.

Assigning a workspace to a subdomain is done from the workspace settings; editing subdomain or domain settings won’t assign a specific workspace.

Best practices for planning and creating domains in Microsoft Fabric

Power BI implementation planning: Workspaces at the tenant level

Question 6 of 50

You have a Fabric workspace named Workspace1 that contains an Apache Spark pool.

You plan to create a notebook named Notebook1 in Workspace1.

You need to ensure that Notebook1 uses high concurrency mode so that Spark sessions can be shared across multiple concurrent users or processes.

Which Workspace settings should you configure?

Select only one answer.

Data Engineering/Science Settings />

This answer is correct.

Data Factory


Data Warehouse


Delegated Settings

High concurrency for Spark is controlled via Data Engineering/Science Settings; other settings are unrelated.

Prepare to use Apache Spark

Question 7 of 50

You are implementing an analytics solution using Microsoft Fabric with a deployment pipeline: Development, Test, and Production.

You need to configure the deployment pipeline to deploy only specific content from Test to Production.

What should you do?

Select only one answer.

Deploy all content


Modify deployment rules for the Test stage.

This answer is incorrect.

Modify the existing pipeline by removing unnecessary content.


Use selective deployment.

This answer is correct.
Using selective deployment is the correct approach to choose specific content for deployment from the Test stage to the Production stage. Modifying deployment rules affects how content is deployed but does not allow for selective deployment of specific content. Modifying the existing pipeline by removing unnecessary content does not utilize the selective deployment feature, which allows for specific content deployment without altering the pipeline structure. Deploying all content updates everything in the target stage, which does not meet the requirement of deploying only specific content.

Get started with deployment pipelines - Training | Microsoft Learn

Question 8 of 50

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

Question 9 of 50

Your organization uses Microsoft Fabric deployment pipelines to manage analytics solutions across Development, Test, and Production stages.

You need to restrict editing of pipeline settings to authorized users only.

What should you do?

Select only one answer.

Assign pipeline admin roles.

This answer is correct.

Configure workspace permissions.


Enable stage-level security.


Implement role-based access control.

To ensure that only authorized users can edit pipeline settings, assigning pipeline admin roles is essential. This approach maintains security and control over the deployment process. Configuring workspace permissions involves setting access levels for users within a workspace, but it does not specifically restrict editing of pipeline settings. Enabling stage-level security might seem like it restricts access, but it fails to limit editing permissions. Implementing role-based access control manages user permissions but does not specifically influence who can edit pipeline settings.

The deployment pipelines process - Training | Microsoft Learn
Get started with deployment pipelines - Training | Microsoft Learn

Question 10 of 50

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

Question 11 of 50

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

Question 12 of 50

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

Question 13 of 50

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


This answer is correct.
Creating a security policy with a filter predicate and implementing row-level security using department identifiers ensures that each department can only access its own sales data. Column-level security controls access to specific columns within a table, not specific rows, and does not provide the granularity needed for department-specific access.

Row-level security in Fabric data warehousing - Training | Microsoft Learn

Question 15 of 50

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

Question 16 of 50

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

Question 17 of 50

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

Question 18 of 50

You have a Fabric workspace named Workspace1 that contains a lakehouse.

You create a pipeline in Workspace1 and add a Copy Data activity to the pipeline.

What is the purpose of the Copy Data activity?

Select only one answer.

to apply data transformations to ingested data


to copy data from a source to a destination

This answer is correct.

to run an Apache Spark notebook


to run SQL code

Copy Data moves data from source to destination with basic mapping; transformations require Dataflow Gen2 or notebooks; running notebooks or SQL scripts uses different pipeline activities.

Use the Copy Data activity

Question 19 of 50

You have a Fabric workspace that contains a lakehouse named Lakehouse1.

You need to create a solution that loads data from a CSV file stored in Azure Data Lake Storage Gen2 into Lakehouse1. The solution must be interactive and support collaboration.

Which type of item should you create?

Select only one answer.

a data pipeline


a dataflow


a notebook

This answer is correct.

an Apache Spark job definition

Notebooks are interactive and collaborative; pipelines/dataflows are geared to repeatable orchestration/prep; Spark job definitions are non-interactive production workloads.

Describe Microsoft Fabric Real-Time Intelligence?

Explore notebooks

Question 20 of 50

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

Question 21 of 50

Your organization uses Microsoft Fabric for data analytics workflows.

There are delays in processing due to inefficient monitoring of data ingestion and transformation.

You need to implement a solution for effective monitoring of data workflows.

What should you do?

Select only one answer.

Configure alerts in the Microsoft Real-Time hub.

This answer is correct.

Create a Power BI dashboard.


Store data events in a data lake.


Use Azure Monitor.

This answer is incorrect.
Configuring alerts in the Microsoft Real-Time hub is the most effective solution because it provides real-time monitoring and alerting capabilities for data ingestion and transformation processes, directly addressing the organization's needs. Creating a Power BI dashboard, while useful for visualization, lacks the necessary real-time alerting functionality. Storing data events in a data lake is insufficient as it does not offer immediate notifications required for timely responses. Using Azure Monitor is not ideal as it does not specifically target Microsoft Fabric workspace events, making it less effective for this scenario.

Set alerts on Fabric workspace item events in Real-Time hub - Training | Microsoft Learn
Set alerts based on Fabric events in Real-Time hub - Training | Microsoft Learn

Question 21 of 50

Your organization uses Microsoft Fabric for data analytics workflows.

There are delays in processing due to inefficient monitoring of data ingestion and transformation.

You need to implement a solution for effective monitoring of data workflows.

What should you do?

Select only one answer.

Configure alerts in the Microsoft Real-Time hub.

This answer is correct.

Create a Power BI dashboard.


Store data events in a data lake.


Use Azure Monitor.

This answer is incorrect.
Configuring alerts in the Microsoft Real-Time hub is the most effective solution because it provides real-time monitoring and alerting capabilities for data ingestion and transformation processes, directly addressing the organization's needs. Creating a Power BI dashboard, while useful for visualization, lacks the necessary real-time alerting functionality. Storing data events in a data lake is insufficient as it does not offer immediate notifications required for timely responses. Using Azure Monitor is not ideal as it does not specifically target Microsoft Fabric workspace events, making it less effective for this scenario.

Set alerts on Fabric workspace item events in Real-Time hub - Training | Microsoft Learn
Set alerts based on Fabric events in Real-Time hub - Training | Microsoft Learn

Question 23 of 50

Your organization uses Microsoft Fabric to manage and analyze large datasets.

Recently, issues with data ingestion processes fail intermittently, causing delays in data availability for analysis.

You need to implement a strategy to detect patterns or recurring issues in data ingestion activities.

Which two actions should you perform? Each correct answer presents part of the solution.

Select all answers that apply.

Analyze error logs for past ingestion activities.


Configure alerts for future ingestion failures.

This answer is correct.

Filter activities by status to identify failures.

This answer is correct.

Increase the frequency of data ingestion checks.


Remove all filters to view all activities.

Configuring alerts for future ingestion failures ensures immediate notification and timely intervention, making it a proactive monitoring approach. Filtering activities by status in the Monitor hub allows for quick identification of failed ingestion processes, directly addressing the need to monitor and resolve issues. Analyzing error logs might seem useful for identifying patterns, but it does not address the immediate need to monitor and resolve failures effectively. Removing all filters could lead to information overload, making it difficult to focus on specific failed activities.

Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn
Prepare data for analysis and reporting - Training | Microsoft Learn

ue if the delays are caused by other factors. Increasing data storage capacity without understanding the root cause of delays may not solve the problem and could lead to unnecessary costs.

Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn
Prepare data for analysis and reporting - Training | Microsoft Learn

Question 25 of 50

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

Question 26 of 50

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

Question 27 of 50

You have a Fabric workspace named Workspace1 that contains a data pipeline named Pipeline1.

Pipeline1 runs every morning and loads data into a lakehouse named Lakehouse1.

You discover that Pipeline1 loads data successfully, but the load takes longer than expected.

You need to monitor the data transformation process to identify possible performance issues.

What should you use?

Select only one answer.

a dataflow


a pipeline


an activator


Monitoring hub

This answer is correct.
Monitoring hub surfaces transformation metrics and performance insights; activators automate responses to events, dataflows perform transformations, and pipelines orchestrate tasks but do not provide the dedicated monitoring views.

Introduction

Understand monitoring

Question 28 of 50

You have a Dataflow Gen2 dataflow in Fabric that uses an on-premises data gateway.

You discover that a refresh fails after running for approximately one hour.

You need to troubleshoot the cause of the failure.

What should you do first?

Select only one answer.

Verify the maximum parameters per pipeline. />


Verify the maximum queued runs per pipeline.


Verify the maximum timeout for pipeline activity runs.

This answer is incorrect.

Verify the version of the on-premises data gateway.

This answer is correct.
Gateway version issues commonly cause long-running refresh failures; pipeline timeouts, queued runs, and parameter limits relate to pipelines, not Dataflows Gen2 refresh via gateway.

Data Factory limitations overview

Question 29 of 50

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

Question 30 of 50

Your organization uses Microsoft Fabric to manage data pipelines for processing sales data.

Recently, a pipeline failed during execution, and the error logs indicate a missing data source in one of the Lookup activities.

You need to configure the pipeline to fail gracefully with a clear error message when such issues occur in the future.

What should you do?

Select only one answer.

Add a conditional check to handle missing data sources.


Add a Fail activity with a custom error message and code.

This answer is correct.

Log errors and continue pipeline execution.


Retry the pipeline execution automatically upon encountering missing data sources.

Adding a Fail activity with a custom error message and error code ensures the pipeline fails gracefully, meeting the requirement. Adding a conditional check to handle missing data sources does not ensure the pipeline fails with a clear error message when the data source is missing. Automatically retrying the pipeline does not address the requirement to fail the pipeline with a clear error message. Logging errors without failing the pipeline does not meet the requirement to stop execution with a clear error message.

Use the Fail activity to cause pipeline execution to fail with a customized error message and error code - Training | Microsoft Learn

Question 31 of 50

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

Question 32 of 50

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

Question 33 of 50

Your organization uses Microsoft Fabric Lakehouse to manage large datasets for analytics.

You notice that  query performance has degraded due to the increasing number of small Parquet files generated during data ingestion.

You need to reduce the number of small files to improve query performance in the Microsoft Fabric Lakehouse tables.

What should you do?

Select only one answer.

Apply V-Order for sorting and compression.


Increase file size using Delta Lake compaction.


Use Lakehouse API for file management.


Use Optimize to consolidate small files.

This answer is correct.
Using the Optimize command in Microsoft Fabric Lakehouse consolidates multiple small Parquet files into larger files, which improves query performance by reducing the number of files that need to be scanned during read operations. Applying V-Order optimizes sorting and compression but does not specifically address the issue of consolidating small files into larger ones. Increasing file size using Delta Lake compaction might seem like a solution but does not directly address the issue of consolidating small files. Using the Lakehouse API for file management might seem like a solution to optimize file sizes, but it does not directly address the issue of consolidating small files for better query performance.

Use table maintenance feature to manage delta tables in Fabric - Training | Microsoft Learn

Question 34 of 50

Your company uses Microsoft Fabric to manage large-scale data processing tasks.

You notice performance issues with Spark jobs involving complex transformations and aggregations on Delta format data.

You need to enhance performance of these Spark jobs without modifying the existing codebase.

What should you do?

Select only one answer.

Enable adaptive query execution.


Enable dynamic allocation.


Enable high concurrency mode.

This answer is incorrect.

Enable native execution engine.

This answer is correct.
Enabling native execution engine in environment settings optimizes performance for complex Spark jobs without code modifications. Enabling dynamic allocation can lead to resource inefficiencies and does not directly enhance performance for complex transformations and aggregations. Enabling high concurrency mode allows multiple users to share Spark sessions, but it does not directly enhance performance for complex transformations and aggregations. Enabling adaptive query execution is a common consideration for optimizing Spark job performance, but it does not directly address the specific performance issues related to complex transformations and aggregations on Delta format data.

Load data using T-SQL - Training | Microsoft Learn

Question 35 of 50

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

Question 36 of 50

Your company has set up a Microsoft Fabric lakehouse to store and analyze data from multiple sources, including Azure Event Hubs and local files. The data is used for generating Power BI reports.

You need to implement a loading pattern that supports both full and incremental data loads.

Which approach do you use?

Select only one answer.

Develop a custom ETL tool for data loads.

This answer is incorrect.

Use Azure Synapse Analytics for data loads.


Use Data Factory for incremental data loads.


Use Dataflows Gen2 for full and incremental data loads.

This answer is correct.
Using Dataflows Gen2 to implement both full and incremental data loads is the best approach, as it provides the necessary flexibility and efficiency for report generation. Developing a custom ETL tool is unnecessary when existing tools like Dataflows Gen2 can efficiently handle the task. Using Data Factory for incremental data loads might seem viable but does not address the need for both full and incremental data loads. Using Azure Synapse Analytics might seem like a viable option due to its capabilities in handling large-scale data processing, but it does not specifically address the need for both full and incremental data loads in a Microsoft Fabric lakehouse environment.

Get started with lakehouses in Microsoft Fabric - Training | Microsoft Learn

Question 37 of 50

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

Question 38 of 50

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

Question 39 of 50

You are implementing a data warehouse using Microsoft Fabric.

You plan to integrate data from multiple sources, including Microsoft Azure Data Lake Storage Gen2 and Microsoft SQL Server databases.

You need to design a process to efficiently load data into tables while ensuring data quality and consistency.

Which two tasks should you recommend? Each correct answer presents part of the solution.

Select all answers that apply.

Use Azure Synapse Analytics for data integration.

This answer is incorrect.

Use Data Factory pipelines for ETL orchestration and T-SQL execution.

This answer is correct.

Use dataflows to ingest and transform data from Azure Data Lake Storage Gen2.

This answer is correct.

Use SSIS packages for data integration.

Using Microsoft Data Factory pipelines and dataflows are both effective methods for orchestrating ETL processes and transforming data from various sources into a dimensional model. Microsoft Data Factory pipelines allow for complex orchestration and execution of T-SQL scripts, ensuring efficient data transformation and loading. Dataflows offer a low-code solution for data ingestion and transformation using Power Query, making them suitable for integrating data from Microsoft Azure Data Lake Storage Gen2. Using SSIS packages for data integration is less efficient compared to modern tools like Data Factory and dataflows, especially in a Microsoft Fabric environment. While Azure Synapse Analytics is a powerful tool for data analytics and integration, it is not specifically designed for the ETL processes required to transform and load data into a dimensional model.

Explore the Microsoft Fabric lakehouse - Training | Microsoft Learn
Prepare data for analysis and reporting - Training | Microsoft Learn

Question 40 of 50

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

Question 41 of 50

Your organization uses Microsoft Fabric to manage data across cloud platforms.

You plan to integrate data from a cloud storage service into a lakehouse in Microsoft OneLake.

You need to ensure data from the cloud storage service is accessible within the lakehouse without duplication.

What should you do?

Select only one answer.

Create a shortcut pointing to the cloud storage service.

This answer is correct.

Use a Data Factory pipeline to copy data into the lakehouse.


Use a Data Factory pipeline to export data to Azure Blob Storage and then import it into the lakehouse.


Use a Data Factory pipeline to transform data before loading it into the lakehouse.

Creating a shortcut in the lakehouse pointing to the cloud storage service allows direct access to the data without creating redundant copies, leveraging Microsoft OneLake's capability to unify data across different storage systems. Using a Data Factory pipeline to transform and load data would result in redundant copies and increased storage costs, which is unnecessary when using Microsoft OneLake shortcuts.

OneLake shortcuts - Training | Microsoft Learn

Question 42 of 50

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

Question 43 of 50

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

Question 44 of 50

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

Question 45 of 50

You are implementing a new data analytics solution using Microsoft Fabric.

The data to be ingested includes structured, semi-structured, and unstructured formats from various sources.

You need to select a data store that accommodates diverse data formats and supports both PySpark and SQL operations for data transformation and analysis.

Which two data stores should you select? Each correct answer presents a complete solution.

Select all answers that apply.

Azure Data Lake Storage Gen2


Azure Synapse Analytics

This answer is correct.

Microsoft Fabric Eventhouse

This answer is incorrect.

Microsoft Lakehouse

This answer is correct.
Azure Synapse Analytics is suitable because it supports all data formats and allows operations using T-SQL and Spark, accommodating the team's diverse skill set and data needs. Microsoft Lakehouse is also appropriate as it supports structured, semi-structured, and unstructured data formats and allows operations using both PySpark and SQL, aligning with the team's skills and data requirements. In contrast, Microsoft Fabric Eventhouse is designed for real-time analytics and supports diverse data formats but is not optimized for batch processing or large-scale data transformation using PySpark and SQL, which are required in this scenario. Azure Data Lake Storage Gen2, while capable of storing diverse data formats, does not natively support PySpark and SQL operations, making it unsuitable for this scenario.

Microsoft Fabric decision guide: choose a data store - Training | Microsoft Learn

Question 46 of 50

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

Question 47 of 50

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

Question 48 of 50

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

Question 49 of 50

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


Use batch processing to load data every hour.

Setting up a SQL analytics endpoint allows querying of data stored in Delta tables within a Microsoft lakehouse, providing near real-time insights. Implementing Spark Structured Streaming allows for efficient processing and writing of streaming data to Delta tables, supporting ACID transactions and enabling querying in near real-time. Storing data in a JSON file does not support real-time querying or ACID transactions, which are necessary for this scenario. Batch processing does not meet the requirement for near real-time data ingestion and analysis. Azure Stream Analytics is not typically used for processing streaming data in Microsoft Fabric; Microsoft Spark Structured Streaming is more appropriate.

Get streaming data into lakehouse and access with SQL analytics endpoint - Training | Microsoft Learn

Question 50 of 50

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

Practice Assessment Results: February 15, 2026

Practice Assessment for Exam DP-700: Implementing Data Engineering Solutions Using Microsoft Fabric

It took you 10 minutes to complete this assessment.

Overall Results
To be better prepared for the exam, aim to achieve a score of 80% or higher in multiple attempts.

Score: 78%

Performance by assessment section
To further strengthen your skills in the following areas, refer to the Customized Learning Material section below.

Implement and manage an analytics solution

Ingest and transform data

Monitor and optimize an analytics solution

