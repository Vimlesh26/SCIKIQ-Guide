# Data Migration

### **Introduction**

Data migration is a critical process for businesses seeking to modernize their data infrastructure, move to more scalable and cost-effective platforms, or consolidate their data across different systems. SCIKIQ’s Data Migration module offers a comprehensive, wizard-based solution designed to simplify this often-complex task. Whether you're transferring structured data from traditional on-premise databases like Oracle or migrating datasets to cloud-native platforms such as Vertica, SCIKIQ provides an intuitive environment that streamlines the entire migration process.

The Data Migration module within SCIKIQ allows data architects, analysts, and administrators to seamlessly perform migrations, ensuring that data integrity and consistency are maintained. The module supports a range of migration tasks, from schema migration and delta synchronization to full data replication, all without the need for any custom coding.

### Key Features

1. **User-Friendly Interface**: A wizard-based interface guides users through each step, making it accessible even for those with limited technical expertise.
2. **Real-Time Validation**: Data integrity is ensured with built-in validation checks throughout the migration process.
3. **Metadata Intelligence**: Leverages the system’s metadata intelligence to optimize the mapping and transformation of data between different environments.
4. **No Code Migration**: Provides a no-code solution, allowing users to focus on their data without worrying about complex scripting.
5. **Delta Synchronization & Replication**: The module supports ongoing synchronization, so data can be kept up-to-date during and after migration.

### **Purpose of Data Migration in SCIKIQ**

The primary purpose of SCIKIQ’s Data Migration module is to make data migration more efficient, less error-prone, and more accessible. By abstracting away the complexity of the process, SCIKIQ allows businesses to focus on their data-driven goals without worrying about the intricacies of different database technologies or environments. Whether businesses are shifting to modern cloud-based platforms like Vertica, optimizing performance, or improving data accessibility, SCIKIQ enables smooth transitions while safeguarding data quality.

The migration process not only moves data but also ensures that the right data structure, integrity, and relationships are maintained. This is particularly important when transferring data between disparate systems, such as from legacy databases like Oracle to newer, high-performance systems like Vertica.

In essence, SCIKIQ's Data Migration module serves the following purposes:

* **Streamlining Data Transfer**: It automates and simplifies the otherwise tedious and error-prone process of data migration.
* **Ensuring Data Integrity**: By validating data in real-time and offering metadata intelligence, SCIKIQ ensures that no data is lost or corrupted during migration.
* **Supporting Delta Synchronization**: Businesses can keep their systems up-to-date during the migration process, ensuring minimal disruption to operations.
* **Optimizing Data Operations**: By enabling the use of modern data platforms, SCIKIQ enhances performance, scalability, and accessibility of migrated data.

This document provides a step-by-step guide for performing a typical migration from Oracle to Vertica, demonstrating the power of SCIKIQ’s Migration Hub in enabling seamless and efficient transitions.

### Accessing the Data Migration Module

In the SCIKIQ Connect navigation panel, go to the Scikiq Migration Hub section and select Data Migration. This section houses tools to create and manage migration pipelines.

Here, users can:

* Initiate a new migration workflow
* View previous migration requests
* Monitor schema transfers and transformation jobs
* Access migration logs



<figure><img src="../../../.gitbook/assets/image (596).png" alt=""><figcaption></figcaption></figure>

**Launching the Data Migration Wizard**

Upon selecting Data Migration, users are directed to the Data Migration Wizard, which provides a six-step guided process:

1. **Get Started** – A brief introduction to the migration journey.
2. **Source & Target** – Configure your source and target databases (e.g., Oracle to Vertica).
3. **Migration** – Select tables to be migrated.
4. **Analyze & Sync** – Profile, validate, and optionally enable sync jobs.
5. **POD Management** – Manage jobs and pipelines.
6. **Review & Submit** – Final review and execution of migration.

This interface visually communicates the flow: Source → Target → Schedule & Run, emphasizing ease of use even for non-technical users.

<figure><img src="../../../.gitbook/assets/image (597).png" alt=""><figcaption><p>this screen allows the user to specify the source database system from which data will be migrated</p></figcaption></figure>

### **Source & Target Configuration (Continued)**

Once users are welcomed into the migration wizard and understand its high-level functionality (source → target → schedule), the next crucial stage involves defining where the data comes from and where it needs to go. This is handled in the "Source & Target" section.

Selecting the Data Source Type

The **ScikIQ Migration Hub** is a centralized interface designed to manage the migration of data, configurations, and business processes across ScikIQ environments. It ensures a seamless and traceable transition of critical assets with a focus on security, integrity, and efficiency.                             &#x20;

1. Navigate to the Source & Target tab.
2. Under Source Information, click the dropdown next to “Select Data Source Type.”
3. A list of supported source systems appears, including:
   1. Oracle
   2. MySQL
   3. Postgres
   4. Redshift
   5. SAP HANA

### Use Case 1- Oracle Data Migration

1. **Select Oracle as the source type for this scenario.**
2. Once selected, the system prompts for a connection. Users must choose an existing Oracle connection or set one up via the connection manager.

**Note**: Supported source databases reflect SCIKIQ’s interoperability with major enterprise platforms.

<figure><img src="../../../.gitbook/assets/image (598).png" alt=""><figcaption><p>This screen finalizes the source and target systems for the migration job.</p></figcaption></figure>

#### **Source and Target Connection Details**

**Process Steps:**

1. **Source Information:**
   1. The user selects Oracle as the source.
   2. Connection details such as host IP, schema name, and connection alias appear.
   3. This verifies that the data to be extracted is from a known Oracle instance.
2. **Target Information:**
   1. The user now defines the destination by selecting the target type — in this case, SCIKIQ DNA Hub(Vertica).
   2. A predefined connection like VS\_SciKiQ is chosen.
   3. The system also displays the target host IP and schema name in read-only fields for validation.
3. Once source and target details are populated and verified, the user clicks Next to proceed to the Migration step.

Ensure both source and target schemas are accessible and validated by performing a quick test connection prior to proceeding.

<figure><img src="../../../.gitbook/assets/image (599).png" alt=""><figcaption></figcaption></figure>

#### Migration – Table Selection

Once the source and target connections are configured, the next step in the Data Migration Wizard is selecting the tables you want to migrate from the source database (Oracle) to the target (Vertica).

#### Source Table List View

This screen presents the complete list of available tables in the Oracle source database.

* On the left panel, the available source tables are listed along with their row count and column count, giving a quick view of the data volume.
* You can use the search box to quickly locate tables by name.
* The right-pointing arrow buttons allow you to move one or more selected tables from the source list to the target list for migration.
* Use the double arrow buttons to move all tables at once.
* A checkbox at the bottom labeled Bi-Directional Relationship indicates whether synchronization should occur in both directions (source ↔ target) post-migration. This is optional and can be disabled for one-way syncs.

Only move the necessary tables for the migration scope to keep the process optimize

<figure><img src="../../../.gitbook/assets/image (600).png" alt=""><figcaption></figcaption></figure>

#### Finalized Table Selection

After filtering and choosing your relevant source tables, the selected items appear in the right-hand panel.

* In this image, two tables — TRADES and TRADE\_OPTIONS — have been moved to the right pane, indicating that they are finalized for migration.
* This selection now defines the scope of your actual data migration process.
* You may continue adding more tables or remove ones by using the reverse arrow buttons.

Review row and column counts to validate whether a table’s size aligns with sync strategy or storage constraints at the destination.

<figure><img src="../../../.gitbook/assets/image (601).png" alt=""><figcaption></figcaption></figure>

#### Analyse & Sync

Once the source and target configurations are established and tables for migration are selected, the next critical phase is Analyze & Sync. This step ensures that the migrated data remains continuously synchronized between the source and the destination, offering support for scheduled sync jobs and fine-grained data control.

#### Analyze & Sync: Select Table and Configure Sync Settings

* **Enable Sync Job**:  At the top, the "Enable Sync Job" toggle is activated to allow continuous synchronization between Oracle and Vertica after migration.
* **Select Table for Syncing:**  From the dropdown under "Select Table", users can choose which tables (e.g., TRADES, TRADE\_OPTIONS) they want to monitor and sync post-migration.
* **Edit Columns / Metadata:**  There is an option to edit columns and metadata settings before synchronization. You can enable:
  * **Infer Schema:** To automatically detect and adapt schema changes.
  * **Enable Audit** Fields: To track data modifications during sync.
* **Score Card:** Displays a quick snapshot of the total number of columns and records being managed.
*   **Settings: Users can configure:**

    * **Batch Size** (e.g., 10,000 records) for sync operations to control data load and performance.
    * **Mark as Dimension:** Useful for analytical models where dimension tables must be separated.
    * **Create Daily Delta Job:** Automatically set up delta jobs to sync only the changes daily, ensuring efficiency without reloading complete datasets.



This image represents setting up the foundational configuration for a sync pipeline — enabling users to maintain data freshness between Oracle and Vertica automatically.

<figure><img src="../../../.gitbook/assets/image (602).png" alt=""><figcaption></figcaption></figure>

#### Analyze & Sync: Manage Sync Jobs with Kafka Integration

* **Drag and Drop Sync Management:** Users can drag and organize tables for different job types:
  * Truncate Jobs: Deletes and reloads tables completely on sync.
  * Batch Processing Jobs: Loads new data batches without full table truncation (configured under "Schedule 1").
  * Incremental CDC (Change Data Capture): Tracks and syncs only changed rows (optional).
  * Log-Based CDC: Advanced mechanism for near-real-time replication based on transaction logs (optional).
* **Kafka Integration:**\
  Kafka Server selection is available, indicating that you can stream real-time change data events to Kafka topics if needed for advanced integration and real-time analytics scenarios.

This image focuses on organizing how synchronization should happen operationally — either through complete reloads, incremental syncs, or log-based methods — while offering the ability to stream changes via Kafka for real-time use cases.

<figure><img src="../../../.gitbook/assets/image (603).png" alt=""><figcaption></figcaption></figure>

Column Profiling & Advanced Settings (Analyze & Sync)

Once tables are added to the sync pipeline, this stage provides tools to inspect and prepare the data schema before finalizing the migration and sync process.

#### Column-Level Profiling, Data Tags & Validation Tools

This screen offers in-depth column profiling, enabling users to assess data distribution, quality, and metadata attributes before migration.

#### Key Sections Highlighted:

* Table Profile: Displays column-wise stats such as data type (INT, FLOAT, DATE), record distributions, and sample values for easy analysis.
* Tagging Options (highlighted in yellow/blue/red box):
  * Unique Key: Marks the column as a unique identifier.
  * Filter: Applies filter conditions to the data.
  * Meta Data: Displays metadata information like data types and nullability.
  * EDA: Enables exploratory data analysis to visualize key patterns.
  * DQ Rules: Activates data quality rules to ensure valid and clean data.

This preview allows users to preemptively validate, clean, and prepare data—ensuring the migration not only succeeds but delivers trusted, high-quality information to the target.

<figure><img src="../../../.gitbook/assets/image (604).png" alt=""><figcaption></figcaption></figure>

#### Dimension Flags and Delta Job Creation

This screen helps finalize table-specific settings such as sync type and data destination configuration.

#### Key Features:

* Mark as Dimension: Identifies the table as a slowly changing dimension, useful in analytical environments.
* Create Daily Delta Job: Configures the sync job to capture and replicate only incremental changes daily, optimizing performance and storage.
* Copy To: Gives users the flexibility to write data into a New Table or an Existing Table on the target system (Vertica in this case).

These controls offer a fine-grained mechanism to support historical tracking (dimension handling) and ensure operational efficiency with delta-based syncing.

<figure><img src="../../../.gitbook/assets/image (605).png" alt=""><figcaption></figcaption></figure>

#### Analyze & Sync - Adding Data Filters

In this phase of the data migration process, SCIKIQ allows users to refine their data transformation pipeline by applying conditional filters on the source dataset before it is written to the target destination. This ensures that only qualified, relevant, and pre-validated data is moved, thereby optimizing storage, enhancing performance, and preserving downstream data quality.

#### Opening the Add Filter Panel

Upon navigating to the Analyze & Sync section of the Data Migration module, users can initiate the process of applying filters by clicking the Filter button located on the right side of the table profile view. This action triggers the "Add Filter" overlay panel.

In this interface, users can begin defining a custom filter condition by assigning a unique filter name (e.g., test1) and writing an expression using available fields and logical operators. The example illustrated shows the creation of a filter on the field COUNTER\_PARTY with a condition COUNTER\_PARTY > 23.

The right-hand pane of the dialog offers categorized assistance:

* Operator: Logical symbols such as >, <, =, etc.
* Date & Time: Functions to manipulate or evaluate timestamps
* Column: All available source fields that can be inserted into the filter

This interactive composition environment ensures that filters are both syntactically and semantically accurate.

&#x20;

<figure><img src="../../../.gitbook/assets/image (606).png" alt=""><figcaption></figcaption></figure>

#### Reviewing and Applying the Filter

After writing the condition, clicking Add Filter validates and records the filter in a structured table beneath the editor. This table includes:

* Filter Name
* Filter Condition
* Row Count (preview of how many records will pass the condition)

In this scenario, the filter COUNTER\_PARTY > 23 successfully selects 60 records from the source table.

The user then confirms the inclusion of the filter by clicking OK, which finalizes the filter logic for execution during the sync process. This ensures that subsequent migration operations will apply only to the filtered dataset.

#### Purpose and Best Practices:

The addition of filters serves multiple strategic purposes:

* Scoping Large Datasets: Limit records to those within a defined business logic
* Compliance and Auditing: Exclude sensitive or invalidated records from being moved
* Efficiency in Delta Jobs: Focus compute resources only on relevant data slices

For optimal design, filters should be defined with clarity, testable logic, and naming conventions that support auditing and reproducibility.

This step in the migration pipeline reflects SCIKIQ's commitment to providing both technical rigor and operational flexibility in enterprise data transformations.

&#x20;

<figure><img src="../../../.gitbook/assets/image (607).png" alt=""><figcaption></figcaption></figure>

#### Column Mapping and Table Configuration

**Objective**: Define how source table columns map to the target schema and configure table creation behavior before initiating data migration.

#### Column Mapping Interface

This screen enables users to map source columns from the selected Oracle table to the destination Vertica table.

* Mapping Tab Highlighted:\
  The active tab "Mapping" allows the user to align source and target columns.
* Column Name vs Target Column:\
  Each row shows a source column (e.g., TRADE\_ID, COUNTER\_PARTY, QUANTITY) on the left and a corresponding target field which can be edited or renamed.
* Data Types Auto-Filled:\
  Based on the source, the system automatically assigns compatible data types such as NUMBER and DATE.
* Add Column Option:\
  The + Add Column button allows users to manually introduce additional fields into the target schema if needed.

This interface is particularly useful when source and target schemas differ slightly or when enriching the target with derived or additional fields.

<figure><img src="../../../.gitbook/assets/image (608).png" alt=""><figcaption></figcaption></figure>

#### Copy to New Table and Custom Naming

This screen extends the column mapping by introducing destination-specific configurations:

* Copy To – New Table Selected:\
  A critical setting where users decide whether to write into a new table or an existing one in Vertica. Selecting “New Table” ensures no existing data is overwritten.
* Custom Table Name:\
  The default destination table name (e.g., TRADES) can be customized (as seen here with TRADES\_28thApril) to reflect versioning, testing, or environment-specific use.
* Final Schema Readiness Check:\
  The mapped fields are verified for consistency, and the destination schema is locked before proceeding to execution.

This configuration ensures auditability and avoids conflicts with existing data structures while giving flexibility in naming and structure replication.

<figure><img src="../../../.gitbook/assets/image (609).png" alt=""><figcaption></figcaption></figure>

#### POD Management

Purpose: The POD (Process-Oriented Design) Management step allows users to organize and segment data for migration into logical groupings known as PODs. These groupings help manage and execute table migrations in modular units, increasing clarity and control during large-scale migrations.

Image Reference: The displayed interface showcases the migration configuration screen where two separate PODs are managed: TRADES - test1 and TRADE\_OPTIONS.

#### Functionality Overview:

* Default POD: This is where tables are initially listed by default. In this example, the table TRADES - test1 is shown with metadata indicators for row count, column count, and audit fields.
* Add POD: Users can create additional PODs to logically segment migration tasks. Each POD can be labeled, and tables can be dragged into or removed from these groups.
* Drag-and-Drop Assignment: Tables such as TRADE\_OPTIONS have been moved into a newly created POD 2, as seen in the right-hand panel.
* Delete Option: Each POD comes with an option to remove it via a trash icon, allowing full control over organization.

Benefits:

* Enhances clarity for multi-table migrations.
* Enables stepwise or prioritized execution of migration tasks.
* Supports modular testing and execution.

<figure><img src="../../../.gitbook/assets/image (610).png" alt=""><figcaption></figcaption></figure>

#### Review & Submit

Purpose: This final step summarizes the migration configuration, allowing users to verify all settings before execution. It ensures accuracy, confirms table mappings, and initiates the migration pipeline.

Image Reference: The screenshot presents the review screen titled "Review & Submit," with clearly defined task details and selected table mappings.

Functionality Overview:

* Task Name and Description: Users can assign a custom task name (e.g., Trade Table Migration) and description for traceability.
* Source and Destination Overview: A summary box highlights the connection mapping from source (e.g., Oracle Connection) to destination (Vs\_Scikiq).
* Table Mapping Summary:
*
  * Source Tables: TRADE\_OPTIONS, TRADES
  * Corresponding Target Tables: TRADE\_OPTIONS, TRADES\_28thApril
  * Flags indicating whether these are new or existing tables.
  * Truncate flags confirm whether the target tables will be emptied before migration (set to "No" here).
* Final Action: Clicking the Finish button triggers the full migration process as per the reviewed configuration.

#### Best Practices:

* Double-check all target table names to avoid overwrite or data mismatch.
* Ensure POD assignments reflect business logic or batch strategy.
  *   Validate audit fields and delta job settings if applicable.

      The POD Management and Review & Submit steps conclude the setup of a well-structured data migration process. By enforcing verification and logical grouping, SCIKIQ ensures enterprise-grade reliability and traceability for every migration task.

<figure><img src="../../../.gitbook/assets/image (611).png" alt=""><figcaption></figcaption></figure>

#### Confirmation of Data Migration Job Creation

After configuring all required parameters and submitting the migration job from the _Review & Submit_ section, the system displays a confirmation dialog indicating the successful creation of the data migration job.

* Message Displayed: "Data migration job is created successfully!"
* Status: The job is tagged with a system-generated status – CREATED, signifying that the request has been successfully registered in SCIKIQ’s orchestration system.
* Request Number: A unique request identifier (e.g., DTAMCLINT0043000064) is generated and assigned for downstream tracking and audit purposes.
* Submitted By: The identity of the initiating user (e.g., "Vimlesh Singh") is logged and displayed.
* User Action: Clicking OK will close this confirmation and redirect the user to the migration job listing interface for further monitoring or execution.

This acts as a critical checkpoint ensuring task integrity, auditability, and traceability before executing potentially large-scale data transformations.

&#x20;

<figure><img src="../../../.gitbook/assets/image (612).png" alt=""><figcaption></figcaption></figure>

### Use Case 2: SAP Data Migration

SAP systems are at the heart of many enterprises, housing critical data across ERP, finance, supply chain, and more. Migrating this data to modern cloud platforms is essential to unlock analytics, AI, and digital transformation initiatives. However, traditional SAP data migration can be complex, invasive, and resource-intensive.

ScikIQ’s SAP Data Migration solution simplifies this journey with a non-invasive, automated, and highly configurable platform that supports seamless extraction, transformation, and loading (ETL) of SAP data—without disrupting source systems.

Key Features:

* Rich Library of SAP-Specific Functions: ScikIQ provides a robust set of reusable transformations tailored for SAP data types and structures.
* Minimal to Zero Source System Impact: Leverages non-intrusive techniques like database triggers, change data capture (CDC), and native RFCs to avoid performance degradation.
* Automated Data Reconciliation: Ensures data consistency and integrity across the entire migration process through built-in validation checks.

&#x20;

<figure><img src="../../../.gitbook/assets/image (1253).png" alt=""><figcaption></figcaption></figure>

SAP Data Migration Approaches Supported by ScikIQ

With ScikIQ, you can extract data from a full range of SAP including SAP HANA, ECC or SAP BW with just a few clicks. Through it NO Code Data Integration and Data Transformation Platform it let our client teams to effortlessly centralize all the data & build single version-of-truth thereby enabling them to make faster, smarter & confident decisions using data.

ScikIQ supports SAP Data Extraction from SAP using following methodologies

1. Database Level: Extraction Framework at Database Level extracts raw data as it is being written to SAP database, transform the data to consumable formats with the required mappings and writes on a target database i.e., Snowflake or Vertica,MSSQL.
2. Application Level: ScikIQ uses Remote Function Call libraries to natively connect and extract data from remote function modules, views, tables, and queries.
3. OData: SAP OData connectors allow you to browse different OData services exposed in the SAP server through its Catalog service. You can select any service of your choice, retrieve the meta-data of various entities exposed in the selected service and then design a job within ScikIQ to extract data for the given entity set.

<figure><img src="../../../.gitbook/assets/image (1255).png" alt=""><figcaption></figcaption></figure>

Data Integration Capabilities for SAP Ecosystem

ScikIQ supports robust and flexible data integration from a wide range of SAP environments, including SAP S/4HANA, SAP ECC on HANA, SAP BW on HANA/BW/4HANA, and SAP HANA RDBMS. This comprehensive support empowers enterprises to unify operational and analytical data across both legacy and modern SAP deployments, enabling real-time insights and scalable analytics.

&#x20;

1\.      SAP S/4 HANA

•       SAP ERP is an enterprise resource planning software.

•       SAP ERP consists of several modules, including Financial Accounting (FI), Controlling (CO), Asset Accounting (AA), Sales & Distribution (SD),SAP Customer Relationship Management (SAP CRM), Material Management (MM), Production Planning (PP), Quality Management (QM), Project System (PS), Plant Maintenance (PM), Human Resources (HR), Warehouse Management (WM).

<figure><img src="../../../.gitbook/assets/image (1256).png" alt=""><figcaption></figcaption></figure>

1\.      BW on HANA/BW4HANA

•       SAP Business Warehouse or SAP BW as it is better known is SAP’s enterprise data warehouse.

•       SAP Business Warehouse has a lot of functions, including data modelling, administration, and provision for staging.

•        It integrates multi-source data, aggregates, and transforms data, carries out data cleansing and stores data. SAP BW stores data from SAP and non-SAP sources and users can access this through built-in reporting, BI and analytics tools and even third-party software

<figure><img src="../../../.gitbook/assets/image (1257).png" alt=""><figcaption></figcaption></figure>

1\.      ECC ON HANA

SAP ECC running on HANA provides high-speed access to traditional ERP functionality. ScikIQ supports:

* Data extraction from transparent tables and function modules
* Custom Z-table integration
* Data replication from key transactional modules with change tracking

This integration is ideal for enterprises that are still operating ECC environments but want to modernize reporting and analytics.

<figure><img src="../../../.gitbook/assets/image (1258).png" alt=""><figcaption></figcaption></figure>

Providing Source and Target Connection Details

This step establishes the source and target systems for the data migration job in ScikIQ. While this example covers SAP ECC to MSSQL, the same procedure applies for migrating data from SAP S4 APP SERVER or SAP BW  to any supported RDBMS like Vertica, Snowflake, or PostgreSQL.

Process Steps:

1. Source Information:
2.
   * Select SAP ECC as the source system.
   * ScikIQ displays the host IP, connection type, and other metadata.
   * This confirms that data will be extracted from a registered and validated SAP ECC instance.
3. Target Information:
4.
   * Choose the destination system — here, it is SQL Server (MSSQL).
   * Select an existing connection (e.g., Master MSSQL Connection).
   * Target details like host IP and schema name are shown as read-only for review and validation.
5. Validation & Next Step:
6.
   * Ensure both source and target systems are reachable by performing a Test Connection.
   * After validation, click Next to proceed to the Migration step.

<figure><img src="../../../.gitbook/assets/image (1259).png" alt=""><figcaption></figcaption></figure>

Migration – Table Selection

The Data Migration Wizard facilitates the transfer of data from SAP ECC (Source Database) to MSSQL (Target Database). Once the source and target database connections are successfully configured, the next step involves selecting the tables to be migrated. This document outlines the process for selecting the relevant tables from the SAP ECC system.

&#x20;

Source Table List View

In SAP ECC, there are numerous tables available for migration. To facilitate the selection of tables, the Search Table functionality is provided within the Data Migration Wizard.

&#x20;

Steps to Search and Select Tables:

1\.      Click the Search Table Button:

Once you're in the Data Migration Wizard, you will find a Search Table button. Clicking this button opens a modal window, which allows you to search and select tables based on specific criteria.



<figure><img src="../../../.gitbook/assets/image (1260).png" alt=""><figcaption></figcaption></figure>

1\.      Modal Window for Table Search:

The modal window provides various search options for selecting data types within SAP ECC. You can search for and choose tables based on the following criteria:

&#x20;

a)      Table

* Description: These are standard database tables within the SAP ECC system. Tables contain data that can be used for various operations like reporting, transactions, or integrations.
* Example:
*
  * T001: Company Codes Table. This table contains details about the company codes in SAP.
  * MARA: Material Master Table. It stores data related to materials, such as material number, description, and type.
  * VBRK: Billing Document: Header Data. This table contains header-level information about billing documents.

<figure><img src="../../../.gitbook/assets/image (1261).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1262).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1263).png" alt=""><figcaption></figcaption></figure>

&#x20;

a)      CDS View (Core Data Services View)

* Description: CDS views provide a semantic layer over SAP HANA database tables. They allow users to define complex queries, creating a unified data structure that can be accessed and consumed by SAP applications. CDS views help in simplifying access to data and are often used in S/4HANA environments.
* Example:
*
  * I\_SalesOrder: A CDS view representing sales order data, combining information from multiple tables like sales orders, customers, and items.
  * I\_FinancialStatement: A CDS view that aggregates financial data from different modules (FI, CO) to generate comprehensive financial reports.

<figure><img src="../../../.gitbook/assets/image (1264).png" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="../../../.gitbook/assets/image (1266).png" alt=""><figcaption></figcaption></figure>

&#x20;

a)      BAPI Function (Business Application Programming Interface)

* Description: BAPIs are standardized programming interfaces provided by SAP for integrating external systems with SAP or for automating business processes within SAP. BAPI functions can be used to retrieve data, create, update, or delete records.
* Example:
*
  * BAPI\_SALESORDER\_CREATEFROMDAT2: A BAPI function used for creating sales orders in SAP.
  * BAPI\_MATERIAL\_SAVEDATA: A BAPI used for saving material master data into SAP.
  * BAPI\_GOODSMVT\_CREATE: A BAPI for posting goods movement (e.g., for inventory management).

<figure><img src="../../../.gitbook/assets/image (1267).png" alt=""><figcaption></figcaption></figure>



<figure><img src="../../../.gitbook/assets/image (1268).png" alt=""><figcaption></figcaption></figure>

a)      Tcode Search (Transaction Code Search)

* Description: Transaction codes (Tcodes) in SAP represent specific tasks or operations in the system, such as creating a sales order, posting an invoice, or managing inventory. The Tcode search allows you to find tables associated with specific transactions or operations within SAP.
* Example:
*
  * Tcode: VA01 (Create Sales Order): This transaction code allows users to create sales orders. Tables related to VA01 would include VBAK (Sales Order Header) and VBAP (Sales Order Item).
  * Tcode: ME21N (Create Purchase Order): This transaction code is used to create a purchase order. Relevant tables might include EKKO (Purchase Order Header) and EKPO (Purchase Order Item).

<figure><img src="../../../.gitbook/assets/image (1270).png" alt=""><figcaption></figcaption></figure>

a)      Process Migration Search

* Description: This search type helps identify tables related to specific process migration scenarios in SAP ECC, often used during the migration from older versions of SAP or when transitioning from SAP ECC to S/4HANA. It helps track the necessary data related to business processes being migrated.
* Example:
*
  * Finance Migration: Tables related to the migration of financial data might include BKPF (Accounting Document Header) and BSEG (Accounting Document Segment).

&#x20;

*
  * Material Master Migration: If migrating data related to materials, tables such as MARA (General Material Data) and MAKT (Material Descriptions) may be relevant.
  *

&#x20;

<figure><img src="../../../.gitbook/assets/image (1271).png" alt=""><figcaption></figcaption></figure>

We are moving forward with the SAP ECC table migration, starting with table T001.

When preparing for migration, you can easily locate the tables, CDS views, or related objects using the Table Search feature. For this example, we’ve selected T001. As you can see, once the table is searched, all related tables appear in the list on the left-hand side.

Key actions during this step:

* Use the search box to quickly find tables by name.
* Use the single right-pointing arrow button to move selected tables from the source list to the target list for migration.
* Use the double right-pointing arrow button to move all listed tables at once.
* An optional “Bi-Directional Relationship” checkbox at the bottom determines whether synchronization should be two-way (source ↔ target) after migration. Disable this if only one-way sync is required.

<figure><img src="../../../.gitbook/assets/image (1272).png" alt=""><figcaption></figcaption></figure>

Finalized Table Selection

After filtering and choosing your relevant source tables, the selected items appear in the right-hand panel.

* In this image, two tables — T001 and T001B — have been moved to the right pane, indicating that they are finalized for migration.
* This selection now defines the scope of your actual data migration process.
* You may continue adding more tables or remove ones by using the reverse arrow buttons.

Review row and column counts to validate whether a table’s size aligns with sync strategy or storage constraints at the destination.

<figure><img src="../../../.gitbook/assets/image (1273).png" alt=""><figcaption></figcaption></figure>

Analyze & Sync

Once the source and target configurations are established and tables for migration are selected, the next critical phase is Analyze & Sync. This step ensures that the migrated data remains continuously synchronized between the source and the destination, offering support for scheduled sync jobs and fine-grained data control.

&#x20;

Analyze & Sync: Select Table and Configure Sync Settings

* Enable Sync Job:\
  At the top, the "Enable Sync Job" toggle is activated to allow continuous synchronization between Oracle and Vertica after migration.
* Select Table for Syncing:\
  From the dropdown under "Select Table", users can choose which tables (e.g., T001, T001B) they want to monitor and sync post-migration.
* Edit Columns / Metadata:\
  There is an option to edit columns and metadata settings before synchronization. You can enable:
*
  * Infer Schema: To automatically detect and adapt schema changes.
  * Enable Audit Fields: To track data modifications during sync.
* Score Card:\
  Displays a quick snapshot of the total number of columns and records being managed.
* Settings:\
  Users can configure:
*
  * Batch Size (e.g., 10,000 records) for sync operations to control data load and performance.
  * Mark as Dimension: Useful for analytical models where dimension tables must be separated.
  * Create Daily Delta Job: Automatically set up delta jobs to sync only the changes daily, ensuring efficiency without reloading complete datasets.

\
This image represents setting up the foundational configuration for a sync pipeline — enabling users to maintain data freshness between Oracle and Vertica automatically.



<figure><img src="../../../.gitbook/assets/image (1274).png" alt=""><figcaption></figcaption></figure>

Analyze & Sync: Manage Sync Jobs with Kafka Integration

* Drag and Drop Sync Management:\
  Users can drag and organize tables for different job types:
*
  * Truncate Jobs: Deletes and reloads tables completely on sync.
  * Batch Processing Jobs: Loads new data batches without full table truncation (configured under "Schedule 1").
  * Incremental CDC (Change Data Capture): Tracks and syncs only changed rows (optional).
  * Log-Based CDC: Advanced mechanism for near-real-time replication based on transaction logs (optional).
* Kafka Integration:\
  Kafka Server selection is available, indicating that you can stream real-time change data events to Kafka topics if needed for advanced integration and real-time analytics scenarios.

\
This image focuses on organizing how synchronization should happen operationally — either through complete reloads, incremental syncs, or log-based methods — while offering the ability to stream changes via Kafka for real-time use cases.

<figure><img src="../../../.gitbook/assets/image (1275).png" alt=""><figcaption></figcaption></figure>

Column Profiling & Advanced Settings (Analyze & Sync)

Once tables are added to the sync pipeline, this stage provides tools to inspect and prepare the data schema before finalizing the migration and sync process.

&#x20;

Column-Level Profiling, Data Tags & Validation Tools

This screen offers in-depth column profiling, enabling users to assess data distribution, quality, and metadata attributes before migration.

Key Sections Highlighted:

* Table Profile: Displays column-wise stats such as data type (INT, FLOAT, DATE), record distributions, and sample values for easy analysis.
* Tagging Options (highlighted in yellow/blue/red box):
*
  * Unique Key: Marks the column as a unique identifier.
  * Filter: Applies filter conditions to the data.
  * Meta Data: Displays metadata information like data types and nullability.
  * EDA: Enables exploratory data analysis to visualize key patterns.
  * DQ Rules: Activates data quality rules to ensure valid and clean data.

This preview allows users to preemptively validate, clean, and prepare data—ensuring the migration not only succeeds but delivers trusted, high-quality information to the target.

<figure><img src="../../../.gitbook/assets/image (1276).png" alt=""><figcaption></figcaption></figure>

Dimension Flags and Delta Job Creation

This screen helps finalize table-specific settings such as sync type and data destination configuration.

Key Features:

* Mark as Dimension: Identifies the table as a slowly changing dimension, useful in analytical environments.
* Create Daily Delta Job: Configures the sync job to capture and replicate only incremental changes daily, optimizing performance and storage.
* Copy To: Gives users the flexibility to write data into a New Table or an Existing Table on the target system (Vertica in this case).

These controls offer a fine-grained mechanism to support historical tracking (dimension handling) and ensure operational efficiency with delta-based syncing.

<figure><img src="../../../.gitbook/assets/image (1277).png" alt=""><figcaption></figcaption></figure>

&#x20;

Analyze & Sync - Adding Data Filters

In this phase of the data migration process, SCIKIQ allows users to refine their data transformation pipeline by applying conditional filters on the source dataset before it is written to the target destination. This ensures that only qualified, relevant, and pre-validated data is moved, thereby optimizing storage, enhancing performance, and preserving downstream data quality.

Opening the Add Filter Panel

Upon navigating to the Analyze & Sync section of the Data Migration module, users can initiate the process of applying filters by clicking the Filter button located on the right side of the table profile view. This action triggers the "Add Filter" overlay panel.

In this interface, users can begin defining a custom filter condition by assigning a unique filter name (e.g., filter1, filter2) and writing an expression using available fields and logical operators. The example illustrated shows the creation of a filter1 on the field WAERS with a condition WAERS ='ARS', and filter2 on the field WAERS with a condition WAERS ='EUR'.

The right-hand pane of the dialog offers categorized assistance:

* Operator: Logical symbols such as >, <, =, etc.
* Date & Time: Functions to manipulate or evaluate timestamps
* Column: All available source fields that can be inserted into the filter

This interactive composition environment ensures that filters are both syntactically and semantically accurate.

&#x20;

Reviewing and Applying the Filter

After writing the condition, clicking Add Filter validates and records the filter in a structured table beneath the editor. This table includes:

* Filter Name
* Filter Condition
* Row Count (preview of how many records will pass the condition)

In this scenario, the filter WAERS ='ARS' successfully selects 2 records and WAERS =' EUR' successfully selects 24 records from the source table.

The user then confirms the inclusion of the filter by clicking OK, which finalizes the filter logic for execution during the sync process. This ensures that subsequent migration operations will apply only to the filtered dataset.

Purpose and Best Practices:

The addition of filters serves multiple strategic purposes:

* Scoping Large Datasets: Limit records to those within a defined business logic
* Compliance and Auditing: Exclude sensitive or invalidated records from being moved
* Efficiency in Delta Jobs: Focus compute resources only on relevant data slices

For optimal design, filters should be defined with clarity, testable logic, and naming conventions that support auditing and reproducibility.

This step in the migration pipeline reflects SCIKIQ's commitment to providing both technical rigor and operational flexibility in enterprise data transformations.

<figure><img src="../../../.gitbook/assets/image (1278).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1279).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1280).png" alt=""><figcaption></figcaption></figure>

Column Mapping and Table Configuration

Objective:\
Define how source table columns map to the target schema and configure table creation behaviour before initiating data migration.

Column Mapping Interface

This screen enables users to map source columns from the selected Oracle table to the destination Vertica table.

* Mapping Tab Highlighted:\
  The active tab "Mapping" allows the user to align source and target columns.
* Column Name vs Target Column:\
  Each row shows a source column (e.g., MANDT, BUKRS) on the left and a corresponding target field which can be edited or renamed.
* Data Types Auto-Filled:\
  Based on the source, the system automatically assigns compatible data types such as NUMBER and DATE.
* Add Column Option:\
  The + Add Column button allows users to manually introduce additional fields into the target schema if needed.

This interface is particularly useful when source and target schemas differ slightly or when enriching the target with derived or additional fields.

<figure><img src="../../../.gitbook/assets/image (1281).png" alt=""><figcaption></figcaption></figure>

&#x20;

Copy to New Table and Custom Naming

This screen extends the column mapping by introducing destination-specific configurations:

* Copy To – New Table Selected:\
  A critical setting where users decide whether to write into a new table or an existing one in MSSQL. Selecting “New Table” ensures no existing data is overwritten.
* Custom Table Name:\
  The default destination table name (e.g., T001) can be customized (as seen here with T001\_28thApril) to reflect versioning, testing, or environment-specific use.
* Final Schema Readiness Check:\
  The mapped fields are verified for consistency, and the destination schema is locked before proceeding to execution.

This configuration ensures auditability and avoids conflicts with existing data structures while giving flexibility in naming and structure replication.

<figure><img src="../../../.gitbook/assets/image (1282).png" alt=""><figcaption></figcaption></figure>

Meta data shown

<figure><img src="../../../.gitbook/assets/image (1283).png" alt=""><figcaption></figcaption></figure>

POD Management

Purpose: The POD (Process-Oriented Design) Management step allows users to organize and segment data for migration into logical groupings known as PODs. These groupings help manage and execute table migrations in modular units, increasing clarity and control during large-scale migrations.

Image Reference: The displayed interface showcases the migration configuration screen where two separate PODs are managed: T001B, T001-filter and T001-filer2.

Functionality Overview:

* Default POD: This is where tables are initially listed by default. In this example, the table T001B is shown with metadata indicators for row count, column count, and audit fields.
* Add POD: Users can create additional PODs to logically segment migration tasks. Each POD can be labeled, and tables can be dragged into or removed from these groups.
* Drag-and-Drop Assignment: Tables such as T001-filter and T001-filer2 have been moved into a newly created POD 2, as seen in the right-hand panel.
* Delete Option: Each POD comes with an option to remove it via a trash icon, allowing full control over organization.

Benefits:

* Enhances clarity for multi-table migrations.
* Enables stepwise or prioritized execution of migration tasks.
* Supports modular testing and execution.

<figure><img src="../../../.gitbook/assets/image (1284).png" alt=""><figcaption></figcaption></figure>

Review & Submit

Purpose: This final step summarizes the migration configuration, allowing users to verify all settings before execution. It ensures accuracy, confirms table mappings, and initiates the migration pipeline.

Image Reference: The screenshot presents the review screen titled "Review & Submit," with clearly defined task details and selected table mappings.

Functionality Overview:

* Task Name and Description: Users can assign a custom task name (e.g., T001 Table Migration) and description for traceability.
* Source and Destination Overview: A summary box highlights the connection mapping from source (e.g., SAP ECC) to destination (MSSQL).
* Table Mapping Summary:
*
  * Source Tables: T001, T001B
  * Corresponding Target Tables: T001, T001B
  * Flags indicating whether these are new or existing tables.
  * Truncate flags confirm whether the target tables will be emptied before migration (set to "No" here).
* Final Action: Clicking the Finish button triggers the full migration process as per the reviewed configuration.

Best Practices:

* Double-check all target table names to avoid overwrite or data mismatch.
* Ensure POD assignments reflect business logic or batch strategy.
* Validate audit fields and delta job settings if applicable.

The POD Management and Review & Submit steps conclude the setup of a well-structured data migration process. By enforcing verification and logical grouping, SCIKIQ ensures enterprise-grade reliability and traceability for every migration task.

<figure><img src="../../../.gitbook/assets/image (1285).png" alt=""><figcaption></figcaption></figure>

Confirmation of Data Migration Job Creation

After configuring all required parameters and submitting the migration job from the _Review & Submit_ section, the system displays a confirmation dialog indicating the successful creation of the data migration job.

* Message Displayed: "Data migration job is created successfully!"
* Status: The job is tagged with a system-generated status – CREATED, signifying that the request has been successfully registered in SCIKIQ’s orchestration system.
* Request Number: A unique request identifier (e.g., DTAMCLNT0104000317) is generated and assigned for downstream tracking and audit purposes.
* Submitted By: The identity of the initiating user (e.g., "Sonali Sharma") is logged and displayed.
* User Action: Clicking OK will close this confirmation and redirect the user to the migration job listing interface for further monitoring or execution.

This acts as a critical checkpoint ensuring task integrity, auditability, and traceability before executing potentially large-scale data transformations.

&#x20;

Navigating to Migration Request Dashboard

Once the job is created, users are redirected to the Data Migration Request dashboard which provides a comprehensive view of all submitted migration jobs.

* Job Listing Panel: Lists multiple migration jobs including historical records. Each job is represented by a card showing:
*
  * Source and target systems (e.g., SAP ECC → MSSQL).
  * Status of the job (CREATED, FINISHED, ERROR, etc.).
  * Action buttons (RUN, RE-RUN, CREATE PHYSICAL MODEL) for control and rerun.
* Quick Filters: Users can filter by job status, data source, or page size for effective tracking.
* Action Highlight: The topmost job (DTAMCLNT0104000317) is in CREATED state and ready to be executed using the RUN button.

This dashboard offers real-time visibility into all data migration workflows, supporting governance, operational tracking, and error resolution at scale.

<figure><img src="../../../.gitbook/assets/image (1286).png" alt=""><figcaption></figcaption></figure>

Viewing Migration Request Summary

Clicking on a job card expands the Request Detail View that presents a job-specific breakdown:

* Meta Information: Includes:
*
  * Task name and description.
  * Request ID.
  * Submission time and initiator’s identity.
* Current Status: Still listed as CREATED, indicating readiness for execution.
* Pod Assignment Panels:
*
  * Tables like T001B and T001 are organized into Pods (POD1, POD2).
  * Status indicators for tasks like Pod Assignment, Source Stats Capture, Data Copy, and Discovery.
* Filter Used: Custom filters (e.g., filter,  filter2) are shown against each table when applied during preprocessing.
* Execution Timeline: Start times are recorded and displayed; end time updates upon completion.

This screen serves as the command center for migration execution monitoring, revealing the lifecycle stage of each table and transformation involved in the job.

<figure><img src="../../../.gitbook/assets/image (1287).png" alt=""><figcaption></figcaption></figure>

&#x20;

Confirmation of Migration Job Execution Start

Upon clicking the RUN button, a toast notification appears at the bottom right of the screen:

* Message: “Data Migration Started”
* Visual Cue: Green success indicator confirms that the system has transitioned from configuration state to execution.

This final interface feedback validates the system’s responsiveness and helps the user transition focus from job setup to performance tracking and post-migration analysis.

&#x20;

<figure><img src="../../../.gitbook/assets/image (1288).png" alt=""><figcaption></figcaption></figure>

Monitor Real-Time Job Execution – Status: In Progress

Once the user triggers the migration process, the job status transitions from CREATED to IN PROGRESS, indicating the pipeline is actively processing the data from the source (SAP ECC) to the target (MSSQL).

Key observations:

* Progress Bars show the sequential execution of subtasks:
*
  * POD Assignment
  * Source Stats Capture
  * Data Copy
  * Discovery
* Highlight: A green progress bar shows the completed step Source Stats Capture, while Data Copy and Discovery are still running.
* Filter Application: The custom filter (filter,filter1) remains associated with the T001 table migration.
* Time Tracking: Each step logs start and end timestamps, aiding in performance audits and operational benchmarking.

This stage provides transparency in execution and is critical for identifying runtime bottlenecks or latency issues.

&#x20;&#x20;

<figure><img src="../../../.gitbook/assets/image (1289).png" alt=""><figcaption></figcaption></figure>

Job Status – Data Copied

Once the data extraction, transformation (if applied), and load (ETL) are complete, the job status is updated to DATA COPIED.

Highlights:

* Orange Label (DATA COPIED) is shown both at the job level and table level.
* Pod Details: Information for POD2 has also appeared, indicating parallel execution for different tables.
* Execution Trail: Each subtask's execution % and status (e.g., 100% Done, 0% Done, In Progress) are visible.
* Control Panel: Discovery and Data Quality checks remain optional at this point.

This serves as a checkpoint before entering validation stages such as reconciliation, metadata verification, and downstream audit readiness

<figure><img src="../../../.gitbook/assets/image (1290).png" alt=""><figcaption></figcaption></figure>



Row-Level Reconciliation – Green Signal

The job details pane now shows the reconciliation indicator as green, signifying that row-level reconciliation has passed successfully.

Breakdown:

* Source Table: T001B
* Destination Table: T001B
* Source/Target Row Count: Both equal to 32
* Start/End Time: Clearly recorded with millisecond precision
* Status: DATA COPIED
* Reconciliation Status: Green tick confirms that row count matches and no data integrity violation has occurred.

This screen is pivotal for regulatory compliance in industries like finance and healthcare where reconciliation logs are mandatory for audits.

<figure><img src="../../../.gitbook/assets/image (1291).png" alt=""><figcaption></figcaption></figure>

Column-Level Profile Validation

Clicking on the reconciliation tile brings up a column-level table profile, offering detailed insights into each column’s transformation and integrity post-migration.

Attributes Tracked:

* Source vs Destination Column Name and Type
* Source/Target Count (Total, Null, Unique)
* Data Type Mapping

Additionally:

* A CSV Export button allows users to download the reconciliation results for offline reporting or audit archival.

This in-depth validation ensures semantic consistency and confirms that no corruption or loss occurred during migration essential for mission-critical datasets.

<figure><img src="../../../.gitbook/assets/image (1292).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1293).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1294).png" alt=""><figcaption></figcaption></figure>

Final Migration Status, Physical Model Creation, and Job Tracking

Final Migration Summary Panel

This image provides a comprehensive summary of a data migration task post-execution. It showcases the metadata associated with the migration job, including:

* Request Number: DTAMCLNT0104000317
* Submitted By: sonali sharma
* Submission Date: 05-05-2025 6:53:33 PM
* Current Status: Data Copied (green label)
* Total Cost: Not Available (indicative of either cost not yet calculated or cost tracking disabled)

Below the metadata block, the panel captures the pod assignment and task lifecycle events:

* POD1 Assignment and Timeline: 100% completed; all components like Source Stats Capture, Data Copy, and Discovery are tracked with visual progress indicators.
* Execution Logs: Confirmed start and end times of the task steps (Source Capture, Copy, and Discovery)
* Row Statistics: Source Table T001B was migrated into T001B with 32 source rows, 32 target rows, and status marked as Data Copied.

This panel is critical for auditability and governance teams to review the data pipeline completion status and monitor for data integrity.

<figure><img src="../../../.gitbook/assets/image (1295).png" alt=""><figcaption></figcaption></figure>

Migration Completion and Transition to Physical Model Creation

Upon successful data migration and reconciliation, the job status is marked as FINISHED, as indicated in the top header.

A key feature becomes available here: "Create Physical Model". This option is highlighted in green and serves as the logical next step post-migration. It allows users to:

* Visualize the structure of newly ingested tables
* Build relational mappings between tables (primary/foreign key relationships)
* Prepare the data for downstream consumption in analytics and reporting workflows

This interface links data migration with semantic and data modeling tasks, ensuring continuity in the data lifecycle.

<figure><img src="../../../.gitbook/assets/image (1296).png" alt=""><figcaption></figcaption></figure>

Physical Model Canvas Interface

This image showcases the Physical Model Designer Studio, where the user has successfully pulled the migrated tables into the design canvas.

Key highlights:

* Tables Available on Left Panel: A full list of entities accessible within the current data source
* Canvas Area: Allows drag-and-drop functionality for selected tables
* System Columns Auto-Appended: Columns such as ska\_created\_at, ska\_updated\_at, etc., are automatically injected for operational metadata tracking
* No active joins defined yet: This is an opportunity for users to establish relationships between entities for lineage and business semantics

This step is fundamental for constructing enterprise-ready datasets suitable for semantic querying, BI visualization, or publishing to other systems

<figure><img src="../../../.gitbook/assets/image (1297).png" alt=""><figcaption></figcaption></figure>

Advanced Search and Filtering of Migration Jobs

The final image illustrates the Data Migration Dashboard’s Advanced Search Panel, a feature built to help users track and manage large volumes of migration tasks.

Functional elements:

* Filter by Migration Status: Dropdown options include All, Created, In Progress, Submitted, Data Copied, Partial, Finished, and Error
* Pagination Controls: Page size selectors (e.g., 20 results per page)
* Search Filters: Source Type, Target Type, Connection Names, and Table Identifiers can all be used to narrow down results

This tool is essential for administrators and project managers who oversee numerous migrations across different systems. It ensures traceability, performance auditing, and quick access to problematic or completed jobs.&#x20;



<figure><img src="../../../.gitbook/assets/image (1298).png" alt=""><figcaption></figcaption></figure>
