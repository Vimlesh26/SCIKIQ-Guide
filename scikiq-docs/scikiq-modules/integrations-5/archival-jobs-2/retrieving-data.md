---
icon: page
---

# Retrieving Data

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The **View Data** module in SCIKIQ enables you to retrieve archived data. It also allows you to query the archived data using NLQ and SQL and provides the capability to delete the required archived data.

***

### Procedure

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Connect Data Source</strong></summary>

**Overview**

This section allows users to connect to a data source and navigate through catalogue, database, and tables to access archived data.

**Procedure**

The following step-by-step instructions guide you through the process.

**Step-by-Step Instructions**

1. Under **SCIKIQ Archival**, expand **Archival Jobs**, and then click **View Data**.

<figure><img src="../../../.gitbook/assets/image (1680).png" alt=""><figcaption></figcaption></figure>

The Data Retrieval page is displayed.

2. Click **Select data source** and choose the required source.
3. Click **Select catalogue** and select the relevant catalogue.
4. Click **Select database** and choose the database.

<figure><img src="../../../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>2.Tables</strong></summary>

**Overview**

This section displays all available tables and views within the selected database. Users can filter and select tables for querying.

**Procedure**

The following step-by-step instructions guide you through the process.

1. View the list of tables and views
2. Use **Filter tables and views** to search
3. Select required tables

> <mark style="color:red;">**Note:**</mark> Tables are displayed only after selecting a database

<figure><img src="../../../.gitbook/assets/image (124).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>3.Query Editor</strong></summary>

**Overview**

The **Editor** is the main workspace where users create, edit, and execute SQL queries. It provides a structured interface with action buttons such as **Run**, **Explain**, **Save**, **Clear**, and **Cancel**, enabling full control over query development and execution.

The editor also supports efficient query management by allowing users to save queries for reuse, analyze execution plans, and quickly reset or stop queries when needed.

**Procedure**

The following step-by-step instructions guide you through the process.

1. Navigate to the **Editor** tab in the Query Panel.

The query editor workspace is displayed.

<figure><img src="../../../.gitbook/assets/image (1693).png" alt=""><figcaption></figcaption></figure>

1. **Add New Query Editor**
   1. Click the **“+” (Add Query)** button.
   2. A new query tab is created.
   3. Use this tab to write a new query.

<figure><img src="../../../.gitbook/assets/image (1691).png" alt=""><figcaption></figcaption></figure>

d. Modify an existing query if needed (either **manually** or by loading from **saved** queries)

<figure><img src="../../../.gitbook/assets/image (1692).png" alt=""><figcaption></figcaption></figure>

2. **Manage Query Tabs:  Rename** option
   1. On the query tab, click the **three-dot (⋮) menu**.
   2. Select **Rename** from the menu.

<figure><img src="../../../.gitbook/assets/image (1697).png" alt=""><figcaption></figcaption></figure>

c. Enter a new name for the query tab.

d. Click **Rename button** to save the new name.

<figure><img src="../../../.gitbook/assets/image (1698).png" alt=""><figcaption></figcaption></figure>

3. **Manage Query Tabs: Duplicate** option
   1. On the query tab, click the **three-dot (⋮) menu**.
   2. Select **Duplicate** from the menu.
   3. A new tab is created with the same query content.

<figure><img src="../../../.gitbook/assets/image (1699).png" alt=""><figcaption></figcaption></figure>

4. **Manage Query Tabs: Close Tab** option
   1. On the query tab, click the **three-dot (⋮) menu**.
   2. Select **Close tab (×)** from the menu.
   3. The selected tab is closed.
   4. Ensure the query is saved before closing if needed.

<figure><img src="../../../.gitbook/assets/image (1700).png" alt=""><figcaption></figcaption></figure>

5. **Write or Modify Query**
   1. Enter the SQL query in the editor area.
   2. You can also paste an existing query or modify a loaded query.

<figure><img src="../../../.gitbook/assets/image (1694).png" alt=""><figcaption></figcaption></figure>

6. **Execute Query (Run)**
   1. Click the ![](<../../../.gitbook/assets/image (1707).png>) button.
   2. The system executes the query against the selected data source.
   3. Query results are displayed in the results section.

<figure><img src="../../../.gitbook/assets/image (1695).png" alt=""><figcaption></figcaption></figure>

7. **Analyze Query (Explain)**
   1. Click the ![](<../../../.gitbook/assets/image (1708).png>) button.
   2. The system displays the query execution plan.
   3. Use this to understand performance and optimize the query.

<figure><img src="../../../.gitbook/assets/image (1696).png" alt=""><figcaption></figcaption></figure>

8. **Save Query**
   1. Click ![](<../../../.gitbook/assets/image (1709).png>)to store the query for future use.

<figure><img src="../../../.gitbook/assets/image (93).png" alt=""><figcaption></figcaption></figure>

b. Enter a **Query Name** in the prompt.

c. Click **Save** to store the query.

<figure><img src="../../../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure>

d.  The query is saved under the **Saved Queries** tab for future use.

<figure><img src="../../../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>

9. **Clear Query**
   1. To clear the existing query, Click the ![](<../../../.gitbook/assets/image (1710).png>)button to remove all content from the query editor

<figure><img src="../../../.gitbook/assets/image (92).png" alt=""><figcaption></figcaption></figure>

10. **Cancel Query Execution**
    1. Click the **Cancel** button while a query is running.
    2. The system stops the execution immediately.

</details>

<details>

<summary>4.<strong>Recent Queries</strong></summary>

**Overview**

The **Recent Queries** tab displays a list of queries that were recently executed in the Query Editor. It helps users quickly revisit, review, and reuse previously run queries without rewriting them, improving efficiency and productivity.

**Procedure**

The following step-by-step instructions guide you through the process.

1. **Navigate to Recent Queries**
   1. Click on the **Recent Queries** tab in the Query Panel.
   2. The system displays a list of recently executed queries.
2. **View Recent Queries**
   1. Check the list of queries along with basic details.
   2. Each entry represents a query executed earlier.

<figure><img src="../../../.gitbook/assets/image (1701).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>5.Saved Queries</strong></summary>

**Overview**

The **Saved Queries** tab allows users to store and manage frequently used SQL queries for future use. It helps avoid rewriting queries by providing quick access to previously saved queries along with their associated configurations.

Saved queries retain not only the query text but also related context such as database, connection, catalog, and selected tables, making reuse efficient and consistent.

**Procedure**

The following step-by-step instructions guide you through the process.

1. **Access Saved Queries**
   1. Click on the **Saved Queries** tab in the Query Panel.
   2. The system displays a list of all saved queries.

<figure><img src="../../../.gitbook/assets/image (1687).png" alt=""><figcaption></figcaption></figure>

2. **View Saved Queries**
   1. Check the list of saved queries.
   2. Each entry represents a stored query available for reuse.

<figure><img src="../../../.gitbook/assets/image (1711).png" alt=""><figcaption></figcaption></figure>

c. Use the **Search** option (if available) to find a specific query.

<figure><img src="../../../.gitbook/assets/image (1703).png" alt=""><figcaption></figcaption></figure>

3. **Load Saved Query**
   1. Select the required query from the **Saved Queries**.
   2. Click **Load Query** to open a previously saved query in the editor it in the Query Editor.

<figure><img src="../../../.gitbook/assets/image (1702).png" alt=""><figcaption></figcaption></figure>

**c. Upon loading, the system automatically:**

* Loads the query into the Query Editor
* Selects the associated **Database**
* Selects the **Connection**
* Selects the **Catalog**
* Selects the relevant **Tables**

<figure><img src="../../../.gitbook/assets/image (1704).png" alt=""><figcaption></figcaption></figure>

4. **Delete Saved Query**
   1. From the **Saved Queries** section, select query you want to remove and click **Delete Button** to remove unwanted queries Select the

<figure><img src="../../../.gitbook/assets/image (1705).png" alt=""><figcaption></figcaption></figure>

b. A confirmation message is displayed: _“Delete saved query ‘\<query name>’?”_

c. Click **OK to** delete the query permanently.

<figure><img src="../../../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>6.Query Settings</strong></summary>

**Overview**

The **Query Settings** tab allows users to configure how queries are executed and how results are returned. It provides control over execution resources, result limits, and editor behavior to ensure efficient query performance.

**Procedure**

The following step-by-step instructions guide you through the process.

1. **Open Query Settings**
   1. Click on the **Query Settings** tab in the Query Panel.
   2. The Query Settings options are displayed.

<figure><img src="../../../.gitbook/assets/image (1712).png" alt=""><figcaption></figcaption></figure>

2. Configure the **Workgroup** (default: `primary`) to control query execution and resource usage.
3. set the **Result Limit** (default: 200 rows, range: 1–1000) to define the maximum number of rows returned.&#x20;
4. Enable or disable **Typeahead Code Suggestions** to receive automatic query suggestions while typing.

<figure><img src="../../../.gitbook/assets/image (1713).png" alt=""><figcaption></figcaption></figure>

5. **Save or Cancel Settings**
   1. Click **Save Settings** to apply the changes.
   2. Click **Cancel** to discard any changes made.

<figure><img src="../../../.gitbook/assets/image (1714).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>7<strong>.Query Archived Data Using NLQ</strong></summary>

**Overview**

Natural Language Query (NLQ) enables users to retrieve data using simple business questions instead of writing SQL.

**Procedure**

The following step-by-step instructions guide you through the process.

1. On the **Data Retrieval** page, in the Right **Pane**, click the **Query NLQ** icon corresponding to the table.&#x20;
2. Next, in the **center Pane**, enter the required **query**, and then click the **Run Query** button.

<figure><img src="../../../.gitbook/assets/image (125).png" alt=""><figcaption></figcaption></figure>

3. Submit the query.
4. The required archived data is retrieved.

<figure><img src="../../../.gitbook/assets/image (127).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>8<strong>.Query Archived Data Using SQL</strong></summary>

**Overview**

This section enables users to perform advanced data retrieval using SQL queries.

**Procedure**&#x20;

The following step-by-step instructions guide you through the process.

1. On the **Data Retrieval** page, click the **SQL** button in the **Query Data** pane.
2. Next, on the **Switch Query Mode** message box.

<figure><img src="../../../.gitbook/assets/image (128).png" alt=""><figcaption></figcaption></figure>

3. SQL syntax is displayed in the Query Data pane.&#x20;
4. Select the **table**, then click on the Query Edit blank screen.
   1. The SQL query for the selected tables will be generated **automatically**.

<figure><img src="../../../.gitbook/assets/image (130).png" alt=""><figcaption></figcaption></figure>

5. Click the **Run SQL Query** button.
6. The required archived data is retrieved

</details>

<details>

<summary><strong>9.Query Results</strong></summary>

**Overview**

The Query Results section displays the output generated after executing a query. It also provides execution status to confirm whether the query ran successfully or encountered errors.

**UI Components & Field Description**

* **Query Results Grid**
  * Displays retrieved data in rows and columns
  * Allows users to review output records
* **Query Status**
  * Indicates whether the query execution was successful or failed
  * Displays error messages if applicable

**Procedure**

The following step-by-step instructions guide you through the process.

1. View the output data in the **Query Results** section

<figure><img src="../../../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure>

2. Review the displayed records for accuracy and completeness
3. Check **Query Status** to confirm whether the execution was successful or if any errors occurred

<figure><img src="../../../.gitbook/assets/image (87).png" alt=""><figcaption></figcaption></figure>

4. If errors are present, update the query and re-run

</details>

<details>

<summary><strong>10.Query Execution Details</strong></summary>

**Overview**

This section provides detailed insights into query performance and execution metrics. It helps users analyze efficiency and troubleshoot issues.

**UI Components & Field Description**

* **Run Time**
  * Displays total time taken for query execution
* **Scanned**
  * Indicates the volume of data scanned during execution
* **Rows**
  * Shows the number of rows returned in the result
* **Workgroup**
  * Displays the execution group used
  * Default value: **primary**

**Procedure**

The following step-by-step instructions guide you through the process.

1. Review **Run Time** to understand how long the query took to execute
2. Check **Scanned** data volume to evaluate how much data was processed
3. View **Rows** returned to confirm the output size
4. Check the **Workgroup** used for execution (default: _primary_)

<figure><img src="../../../.gitbook/assets/image (88).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>11.BLOB Data Tasks</strong></summary>

**Overview**

**BLOB (Binary Large Object)** is a database data type used to store large amounts of binary data.&#x20;

Some of the  examples of data that can be stored as a BLOB are:

* Images (JPEG, PNG, GIF)
* Audio files
* Video files
* PDF documents
* Word documents
* Other binary files

**Example**

In databases such as MySQL, Oracle Database, and Microsoft SQL Server, a BLOB column can store a user's profile picture directly in the database.

**Procedure**

The following sections explain how to perform the following tasks: **Set the BLOB Query Limit, View BLOB Data, Download BLOB Data,** and **Export Complete Query Results.**

**1.Set Blob Query Limit**

A. On the **Editor** tab, type the **limit**. See below image.

B. Click the **Run** button

<figure><img src="../../../.gitbook/assets/image (2047).png" alt=""><figcaption></figcaption></figure>

The results are displayed as per the limit specified.

***

**2.View Blob Data**

* On the **Editor** tab, under **Query Results**, click the **View** button corresponding to the required file.

<figure><img src="../../../.gitbook/assets/image (2040).png" alt=""><figcaption></figcaption></figure>

In the selected file, the binary data stored as an image is displayed. See the below image.

<figure><img src="../../../.gitbook/assets/image (2041).png" alt=""><figcaption></figcaption></figure>

***

**3.Download Blob Data**

* On the **Row Data Viewer**, click the **Download** button.

<figure><img src="../../../.gitbook/assets/image (2043).png" alt=""><figcaption></figcaption></figure>

The Blob Data is downloaded.

***

**4.Export Full Query Result**

A. On the **Query Editor**, in the **Query Results** section, click the **Export Full Query Result** button.

<figure><img src="../../../.gitbook/assets/image (2044).png" alt=""><figcaption></figcaption></figure>

The **Export Full Query Result** dialogue box is displayed.

B. On the **Export Full Query Result** dialogue box:

* Select the **File storage connection, specify Export Path, File Type,** and **Rows per file**.
* Click the **Submit export** button.

<figure><img src="../../../.gitbook/assets/image (2045).png" alt=""><figcaption></figcaption></figure>

The full query results are displayed in the selected file format.

</details>

***

### Related Topics

* [**Creating a Table Archival Job**](creating-a-table-archival-job.md)
* [**Creating a File Archival Job**](creating-a-file-archival-job.md)
* [**Validating Data**](validating-data.md)
* [**Managing Existing Jobs**](managing-existing-jobs.md)
* [**Managing Deployment Configs**](managing-deployment-configs.md)
* [**Deleting Archived Data**](deleting-archived-data.md)
* [**Managing Retention Schedules**](managing-retention-schedules.md)
* [**Using Archival Dashboard**](using-archival-dashboard.md)
* [**Using Cube Manager**](using-cube-manager.md)
* [**Using Cube Viewer**](using-cube-viewer.md)
