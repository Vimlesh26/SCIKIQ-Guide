---
hidden: true
icon: code-branch
---

# Delta Pipeline

### Delta Pipeline Overview

#### What is a Delta Pipeline?

A **Delta Pipeline** is an optimized data integration process designed to capture and process only the changes (also known as "deltas") in a dataset, rather than performing a full data reload. This approach is ideal for scenarios where frequent data updates are required, but performing a complete data reload would be inefficient or unnecessary.

The delta pipeline identifies and extracts only **new, updated, or deleted records** since the last execution. This significantly reduces processing times, minimizes the load on source and target systems, and ensures that the data remains consistent and up to date without redundancy.

#### Core Purpose

The core purpose of a Delta Pipeline is to enable **incremental and periodic updates** in an efficient manner. This is especially useful when:

* **Full data reloads are impractical**: Loading the entire dataset is inefficient and time-consuming.
* **Change Data Capture (CDC)** is required: The system needs to track and synchronize only the changes, such as inserts, updates, and deletes.
* **Regular refresh schedules** are needed: Delta Pipelines can be scheduled to run at specific intervals (e.g., hourly, daily, or weekly) to update the data with minimal resources.

Delta Pipelines are often used in scenarios like:

* Synchronizing data between different systems (e.g., syncing data from a CRM to a Data Warehouse).
* Keeping analytics or reporting systems updated with the latest changes (e.g., pushing new inventory data to an analytics platform).
* Periodically refreshing the data in a data lake or other storage systems.

#### Key Features

Delta Pipelines come with several key features that enhance their flexibility, scalability, and ease of use:

* **Change Data Capture (CDC)**: Delta Pipelines support CDC to track changes in the source systems and only load the changed records (inserts, updates, deletes).
* **Parameterization**: They allow parameterized filtering, making it easy to track deltas using fields such as timestamps, row versions, or other unique identifiers.
* **Incremental Loading**: Only new or modified records are extracted, reducing the processing time and resource consumption compared to full data loads.
* **Scheduled Execution**: Delta Pipelines can be set up to run on a schedule (e.g., hourly, daily) to automatically capture and apply the changes.
* **Built-In Versioning**: Ensures that the pipeline schema and logic are reusable and easily adaptable to future changes.
* **Drag-and-Drop Interface**: Designed for simplicity, with a visual editor to configure pipelines without needing advanced coding skills.

#### How Does a Delta Pipeline Work?

1. **Input Nodes**: The pipeline begins by pulling data from source systems such as databases, flat files, or APIs. The key to delta processing is that the data is queried based on certain conditions (e.g., records created or updated after a certain date).
2. **Variable Nodes**: Delta tracking relies on **variable nodes**. These are used to store the timestamp, transaction ID, or other tracking information from the last pipeline run. When the pipeline executes again, it compares the source data with the values stored in these variables to identify changes.
3. **Transformation Nodes** (Optional): Once data is pulled, the pipeline can include transformation logic, such as data cleaning, filtering, and mapping, to ensure that only the necessary changes are processed.
4. **Output Nodes**: After transformation, the pipeline loads the changes into target systems (e.g., Data Warehouse, APIs, file sinks).
5. **Scheduler**: The pipeline can be scheduled to run at predefined times (e.g., daily at 2:00 AM) to keep the data in the target system updated regularly.
6. **Delta Logic**: The key to delta pipelines is the logic for determining what constitutes a "change." This logic usually compares data based on the tracking variables (e.g., `LAST_RUN_DATE` or `TransactionID`) to identify the new or modified records.

#### Common Use Cases for Delta Pipelines

Delta Pipelines are highly effective for use cases where data changes frequently but performing a full data reload is not feasible or efficient. Some common use cases include:

* **Customer Data Sync from CRM to Data Warehouse**: Sync only new or modified customer records from a CRM system to a Data Warehouse.
* **Inventory Transactions**: Track new inventory transactions that occur in a warehouse system and update the analytics platform.
* **ERP System Data Sync**: Pull incremental changes from an ERP system and push them to reporting layers in the Data Warehouse.

#### Key Components of a Delta Pipeline

A typical Delta Pipeline consists of the following components:

* **Input Nodes**: Sources of data, such as databases, files, or APIs.
  * Examples: Database Input, File Input, SAP App Server, NoSQL Input
* **Transformation Nodes** (Optional): Logic applied to the data to clean, filter, or manipulate it.
  * Examples: Filter, Join, Expression
* **Output Nodes**: Where the data is loaded after processing.
  * Examples: Database Output, File Output, API Output
* **Variable Nodes**: Variables that store tracking information (e.g., last modified timestamp or transaction ID).
  * Examples: `LAST_RUN_DATE`, `LAST_TRANSACTION_ID`
* **Scheduler**: Automates the execution of the pipeline on a set schedule (e.g., hourly, daily).

***

#### Benefits of Using Delta Pipelines

1. **Improved Performance**: By processing only the changed data, delta pipelines reduce the overall processing time and resource consumption compared to full data loads.
2. **Reduced Data Redundancy**: Only new or modified records are processed, which minimizes redundancy in the target system.
3. **Better Resource Efficiency**: Delta pipelines are more resource-efficient, using less CPU, memory, and network bandwidth during each execution.
4. **Faster Data Processing**: They allow for faster updates, ensuring that the data remains fresh and up-to-date in real-time or at regular intervals.
5. **Simplified Maintenance**: Delta Pipelines can be scheduled to run automatically, reducing the need for manual intervention and ensuring regular data refreshes.

### Use Cases for Delta Pipelines

#### **Use Cases for Delta Pipelines**

Once the user understands the concept of Delta Pipelines, you can present practical examples of how Delta Pipelines can be applied. These use cases will help users visualize real-world scenarios and how to configure and utilize Delta Pipelines for their specific needs.

***

#### **1. CRM Customer Data Sync (Daily)**

**Use Case Description:**

This use case focuses on synchronizing customer data from a **CRM system** to a **Data Warehouse**. The goal is to track only new and updated customer records, ensuring that the data warehouse remains up-to-date with the latest customer information.

**Steps:**

1. **Create a New Delta Pipeline**:
   * Name the pipeline **CRM Customer Sync**.
   * Select **Delta Pipeline** type.
2. **Input Node**:
   * Configure the input node to fetch customer records from the CRM system using a **SQL query** with a filter condition for `ModifiedDate > '{{LAST_RUN_DATE}}'` (last run timestamp).
   *   Example query:

       ```sql
       sqlCopyEditSELECT * FROM Customers WHERE ModifiedDate > '{{LAST_RUN_DATE}}';
       ```
3. **Variable Node**:
   * Use a variable node, `LAST_RUN_DATE`, to store the timestamp of the last successful pipeline execution.
   * Initially set it to `'2024-01-01'` (this will change after each execution).
4. **Transformation Nodes**:
   * Apply any necessary transformations (e.g., deduplication, data validation, or business logic).
5. **Output Node**:
   * Set the output node to load the new or updated customer records into the **Customer Table** in the **Data Warehouse**.
6. **Scheduler**:
   * Schedule the pipeline to run **daily** at **2:00 AM** to keep the data up-to-date.
7. **Post-Execution**:
   * After the pipeline completes, update the **LAST\_RUN\_DATE** variable to the current timestamp for the next run.

***

#### **2. Hourly Inventory Transactions Sync**

**Use Case Description:**

This use case involves syncing **inventory transaction data** from an **inventory management system** to a **data warehouse** on an hourly basis. It ensures that only newly added or modified transaction records are loaded into the warehouse.

**Steps:**

1. **Create a New Delta Pipeline**:
   * Name the pipeline **Inventory Transactions Sync**.
   * Select **Delta Pipeline** type.
2. **Input Node**:
   * Configure the input node to query the **Inventory\_Transactions** table.
   * Use the `TransactionID > {{LAST_TRANSACTION_ID}}` filter to fetch only the new or updated transaction records.
   *   Example query:

       ```sql
       sqlCopyEditSELECT * FROM Inventory_Transactions WHERE TransactionID > {{LAST_TRANSACTION_ID}};
       ```
3. **Variable Node**:
   * Use a variable node, `LAST_TRANSACTION_ID`, to store the last processed transaction ID.
   * This variable will be updated after every execution to ensure that only the new transactions are processed in the next run.
4. **Transformation Nodes**:
   * Apply transformations such as filtering out irrelevant records or performing calculations (e.g., updating stock levels).
5. **Output Node**:
   * Configure the output node to load the filtered and transformed records into the **Inventory Transactions** table in the **Data Warehouse**.
6. **Scheduler**:
   * Schedule the pipeline to run **every hour** to capture real-time transaction updates.
7. **Post-Execution**:
   * After the pipeline completes, update the **LAST\_TRANSACTION\_ID** variable to the highest `TransactionID` processed during this run.

***

#### **3. Weekly Sales File Delta Processing**

**Use Case Description:**

This use case focuses on processing weekly sales data files stored in an **S3 bucket**. The pipeline should only process new files that have been added to the bucket since the last run, ensuring that only the latest data is used for analysis.

**Steps:**

1. **Create a New Delta Pipeline**:
   * Name the pipeline **Weekly Sales File Processing**.
   * Select **Delta Pipeline** type.
2. **Input Node**:
   * Use a **File Input Node** to read the files from the **S3 bucket**.
   * Filter the files by the `FileDate` using a variable node.
   * Example path: `s3://sales_data/week/{{CURRENT_WEEK}}/*.csv`
3. **Variable Node**:
   * Use a variable node `CURRENT_WEEK` to store the current week’s date (or the date of the last processed file).
   * This will help track which files have been processed and ensure that only new files are loaded.
4. **Transformation Nodes**:
   * Transform the data as necessary (e.g., cleaning, aggregating sales data, or formatting).
5. **Output Node**:
   * Set the output node to load the processed sales data into the **Sales Data Warehouse Table**.
6. **Scheduler**:
   * Schedule the pipeline to run **weekly** at **5:00 AM** every Monday.
7. **Post-Execution**:
   * After the pipeline completes, update the **CURRENT\_WEEK** variable with the date of the last file processed to ensure that only new files are selected in the next run.

***

#### **4. API-based Product Catalog Sync (Daily)**

**Use Case Description:**

This use case syncs product catalog data from an **API** to an internal **product database**. The pipeline checks for newly added or updated products and syncs them to ensure the product catalog is up-to-date.

**Steps:**

1. **Create a New Delta Pipeline**:
   * Name the pipeline **API Product Catalog Sync**.
   * Select **Delta Pipeline** type.
2. **Input Node**:
   * Use an **API Input Node** to fetch product data from an external API endpoint (e.g., `GET /products/modified_since={{LAST_SYNC_DATE}}`).
3. **Variable Node**:
   * Use the `LAST_SYNC_DATE` variable to store the last synchronization timestamp (initially set to `'2024-01-01'`).
4. **Transformation Nodes**:
   * Apply any necessary transformation, such as filtering or mapping product attributes.
5. **Output Node**:
   * Configure the output node to load the data into the **Product Catalog Database**.
6. **Scheduler**:
   * Schedule the pipeline to run **daily** at **1:00 AM**.
7. **Post-Execution**:
   * After the pipeline completes, update the **LAST\_SYNC\_DATE** variable to the current timestamp to ensure the next run fetches only the changes.

***

#### **5. Delta Merge from Data Lake**

**Use Case Description:**

This use case is about merging new data into an existing **Data Lake**. It performs a **Delete-Insert** merge operation to ensure that the latest changes (e.g., updated or deleted records) are reflected in the data lake.

**Steps:**

1. **Create a New Delta Pipeline**:
   * Name the pipeline **Data Lake Delta Merge**.
   * Select **Delta Pipeline** type.
2. **Input Node**:
   * Use a **Database Input Node** or **File Input Node** to fetch data from the source system (e.g., a staging area or data lake).
3. **Transformation Nodes**:
   * Apply a **Delta Merge** transformation to compare the existing records with the new data and perform a **Delete-Insert** merge operation.
   * Handle updates by deleting outdated records and inserting the new or updated records.
4. **Output Node**:
   * Load the merged data into the **Data Lake**.
5. **Scheduler**:
   * Schedule the pipeline to run **daily** or **weekly**, depending on the update frequency.
6. **Post-Execution**:
   * Update tracking variables to ensure that the next pipeline run processes the correct data.

