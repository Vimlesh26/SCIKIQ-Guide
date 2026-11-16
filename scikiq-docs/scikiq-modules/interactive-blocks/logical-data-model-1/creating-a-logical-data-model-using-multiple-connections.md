---
icon: page
---

# Creating a Logical Data Model Using Multiple Connections

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to create a logical data model using multiple connections. **Creating a Logical Data Model** **using a using multiple connections** allows you to include tables from different databases in a single logical model, establish relationships between them, and create a unified view of business data across different systems.

**Key Points and Troubleshooting Information:**

<details>

<summary><strong>How to identify a table's source?</strong></summary>

Each table in the Logical Data Model (LDM) retains its source connection details. This helps users identify where each table originates, even when tables have similar names.

The source information is displayed as follows:

1\. **Source Information:** The connection name appears below each table name. For files, the file path is also displayed.

2\. **Hover Information:** Hovering over a table name displays its full name, source connection, and file path (if applicable).

3\. **Relationship Window:** The source connection appears in brackets next to each table name.

4\. **Reopening the Model:** If a connection has been deleted, the available tables are loaded, and the tables that cannot be loaded are identified.

</details>

<details>

<summary><strong>How are relationships defined between tables from different sources?</strong></summary>

Relationships between tables from different sources are defined using the same **Define Relationship** window, with the same relationship types and **Cross-filter Direction** options.

Key points to remember:

1\. **Automatic Key Matching:** The system automatically matches compatible data types, such as different number formats, text and category, or date and timestamp.

2\. **Incompatible Data Types:** If the key columns have incompatible types, such as text and numbers, an error message identifies the columns.

3\. **Many-to-One Relationship:** Unmatched records are retained and displayed under a blank value, ensuring that totals remain complete (Use Cases 4.1 and 4.3).

4\. **One-to-One Relationship:** Unmatched records are excluded. For example, in Use Case 4.2, regions without an assigned manager do not appear in tables displaying the `manager_name` field.

</details>

<details>

<summary><strong>What are the limitations of using multiple connections?</strong></summary>

The following limitations apply when creating Logical Data Models using multiple connections:

1\. **Supported File Storage:** Only Amazon S3 and SharePoint are supported. OneDrive, Azure Blob, GCP, OCI, and FTP are not currently supported.

2\. **Supported File Formats:** CSV, Excel (first sheet only), and Parquet are supported. Other formats, such as TXT, TSV, JSON, Avro, and ORC, are not supported.

3\. **Fixed File Path:** Each table is linked to a single file path. Files uploaded with a new name, such as daily files, are not automatically detected.

4\. **New Columns:** Newly added file columns appear only after the table is added to the model again.

5\. **File Updates:** Changes to uploaded files are reflected only after the files are uploaded again through **Data Source**.

6\. **Earlier File Stores:** Files uploaded under a previous file store may not be available in the current file store.

7\. **Archived Files:** Files in archive storage, such as Amazon S3 Glacier, may be listed but cannot be read.

8\. **Unsupported Operations:** Whole-model operations, such as Preview Data, Data Profiling, Data API, and Publish, are not supported for these models.

9\. **Saving Models in Data Prep Studio:** Models combining multiple connections are saved as a single physical table in the connection specified under **Admin > Save Dataset To**. The connection is displayed as locked in the save window.

</details>

<details>

<summary><strong>Which operations are not supported, and why?</strong></summary>

Screens that process the entire Logical Data Model (LDM) as a single database query cannot access tables stored across different connections. Therefore, these operations display an appropriate error message instead of processing the model.

**Unsupported Model Configurations and Error Messages**

<table><thead><tr><th valign="top">Model Configuration</th><th valign="top">Error Message</th></tr></thead><tbody><tr><td valign="top">Tables from multiple connections</td><td valign="top"><strong>SCIK-0516:</strong> Not supported for multi connection used in LDM/dataset</td></tr><tr><td valign="top">Tables from a single connection containing files (uploaded files, Amazon S3, or SharePoint)</td><td valign="top"><strong>SCIK-0517:</strong> Not supported for file tables used in LDM/dataset</td></tr></tbody></table>

<mark style="color:red;">**Note:**</mark> Only the dashboard service supports joining tables across multiple data sources.

</details>

<details>

<summary><strong>Messages and Troubleshooting</strong></summary>

The following table lists common error messages and issues, their possible causes, and recommended solutions.

| You see                                                                                                                                   | Where                                           | Why                                                                                                                                   | What to do                                                                                       |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| **SCIK-0516: Not supported for multi-connection used in LDM/dataset**                                                                     | Preview Data, Data Profiling, Publish, Data API | The model contains tables from more than one connection.                                                                              | Create a dashboard on the model and check individual tables using their Preview icon.            |
| **SCIK-0517: Not supported for file tables used in LDM/dataset**                                                                          | Same places                                     | The model contains file-based tables.                                                                                                 | Create a dashboard on the model and check individual tables using their Preview icon.            |
| **The file '...' is not in the file store. Upload the file again in Data Source.**                                                        | Model page, File Upload category                | The file was uploaded under an earlier file store.                                                                                    | Upload the file again through Data Source, then add it to the model.                             |
| **The data connection '...' used by this dataset could not be used, so its tables (...) could not be loaded.**                            | Dashboard                                       | One of the model's data sources cannot be reached.                                                                                    | Test or fix the connection, then reload the dashboard.                                           |
| **The relationship between ... and ... cannot be used: the two columns hold different kinds of values. Relate columns of the same kind.** | Dashboard chart                                 | A relationship connects columns with incompatible data types, such as text and numbers.                                               | Relate columns that have compatible data types.                                                  |
| **... and ... are linked only through ... Add a ... column to this chart, or relate the two tables directly in the LDM.**                 | Dashboard chart                                 | The chart's tables are connected through a third table that the chart does not use.                                                   | Add the named column or create a direct relationship between the tables.                         |
| **You need edit access to this dataset to save a calculated field.**                                                                      | Calculated field window                         | Your role does not allow you to edit the model.                                                                                       | Ask the model owner to provide edit access.                                                      |
| **You are not connected. Join them, or remove the step you do not need, then save again.**                                                | Data Prep Studio save                           | Some input steps are not connected to the remaining steps.                                                                            | Join the unconnected steps or remove the unnecessary steps, then save again.                     |
| **Charts stay empty on the first open**                                                                                                   | Dashboard                                       | The model's tables are still loading in the background.                                                                               | Reload the dashboard after a short wait.                                                         |
| **Rows under a blank value**                                                                                                              | Dashboard chart                                 | The key has no matching record in the related table. For example, _Telangana_ and _Telengana_ do not match, as shown in Use Case 4.3. | Correct the key in the source. The rows will appear under the correct value after the next load. |

</details>

***

### Procedure

The following three example use cases demonstrate how to create Logical Data Models (LDMs) using multiple data connections and different data sources.

These use cases are:

* [**Using Two Database Connections in a Single Model**](creating-a-logical-data-model-using-multiple-connections.md#using-two-database-connections-in-a-single-model)
* [**Adding an Uploaded File from S3**](creating-a-logical-data-model-using-multiple-connections.md#adding-an-uploaded-file-from-s3)
* [**Joining a SharePoint File with a Database Table**](creating-a-logical-data-model-using-multiple-connections.md#joining-a-sharepoint-file-with-a-database-table)

Each use case covers a specific scenario and provides step-by-step instructions for adding the required data sources, defining relationships, and creating the Logical Data Model.

Click the tabs below to view the individual use cases and their corresponding step-by-step instructions.

{% tabs %}
{% tab title=" Using Two Database Connections in a Single Model" %}
**Overview**

The following example demonstrates how to use two database connections within a single Logical Data Model (LDM). It illustrates how data from different databases can be brought together to support reporting and analysis.

In this example, one database contains project-related information, including actual amounts, project details, and regions, while another database contains region-related information.&#x20;

By including tables from both connections and defining relationships between them, users can create a unified data model to analyse actual amounts by project and region.

**Procedure**

The process of creating a multi-connection dashboard involves navigating to the Logical Data Model page and selecting the required Source Type and Source Category.&#x20;

The first connection is then selected, and the required tables are added to the canvas by dragging them onto it. Relationships are defined between the relevant tables.&#x20;

The same process is repeated for the second connection by selecting it, adding the required tables, and defining their relationships.

Once all the required tables and relationships are configured, the Logical Data Model (LDM) is saved. The dashboard can then be opened to view and analyse data from the selected connections.

The below step-by-step instructions describe the process:

_**To use two database connections in a logical model**_

{% stepper %}
{% step %}
**Navigate to Logical Data Model Page**&#x20;

* On the **SCIKIQ left menu**, go to **SCIKIQ CURATE**, and then click **Logical Data Model**.

<figure><img src="../../../.gitbook/assets/image (2704).png" alt=""><figcaption></figcaption></figure>

The **Logical Data Model** page is displayed.
{% endstep %}

{% step %}
&#x20;**Select Source Type**&#x20;

* On the **Logical Data Model** page, from the **Select Source Type** drop-down box, select either **Datasource** or **Assets**. For example, Datasource.
{% endstep %}

{% step %}
**Select Source Category**

* From the **Source Category** drop-down box, select the required **source category**. For example, RDBMS.

{% hint style="info" %}
**Tip:** The following table describes the available source categories, their corresponding connections, and the items to be dragged onto the canvas.

<table><thead><tr><th>Source Category</th><th valign="top">Available Connections</th><th valign="top">Items to be Dragged</th></tr></thead><tbody><tr><td>RDBMS</td><td valign="top">Database connections, such as Vertica, SQL Server,<br>PostgreSQL, MySQL, Snowflake</td><td valign="top">A table from the searchable list</td></tr><tr><td>BigQuery</td><td valign="top">BigQuery connections</td><td valign="top">A table</td></tr><tr><td>File Storage</td><td valign="top">S3 and SharePoint connections</td><td valign="top">A CSV, Excel or Parquet file, found by browsing<br>folders (and the bucket, for S3)</td></tr><tr><td>Glue</td><td valign="top">Glue catalog connections</td><td valign="top">A catalog table</td></tr><tr><td>File Upload<br>(CSV/Excel)</td><td valign="top">Files uploaded under Data Source, one connection<br>per file</td><td valign="top">The uploaded file</td></tr></tbody></table>
{% endhint %}
{% endstep %}

{% step %}
**Select Connection 1, Drag Tables onto the Canvas, and Define Relationship**

1. From the **Select Connection** drop-down box, select the required connection. For example, VS\_Test\_Data\_Sample.

The **Table List** is displayed.

2. From the **Table List,** drag the required **tables** onto to the **right pane (Canvas)**. For example, ebit\_combine\_fact\_table and dim\_project.

<figure><img src="../../../.gitbook/assets/image (3250).png" alt=""><figcaption></figcaption></figure>

3. On the **Top Menu**, click the **Relationship** <img src="../../../.gitbook/assets/image (3243).png" alt="" data-size="line"> button.

The **Define Relationship LDM** drop-down box is displayed.

4. On the **Define Relationship LDM** drop-down box, in the **Source** section, select the **Source Table** and **Columns**. For example, ebit\_combine\_fact\_table and project\_key.
5. In the **Target** section, select the **Target Table** and **Columns**. For example, dim\_project and Project\_key.
6. From the **Relationship** drop-down box, select **Many To One.**&#x20;
7. Click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (3251).png" alt=""><figcaption></figcaption></figure>

The relationship is defined. See the below image.

<figure><img src="../../../.gitbook/assets/image (3252).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Select a Different Connection, Drag Tables onto the Canvas, and Define Relationship**

1.  From the **Select Connection** drop-down box, select the a different connection. For example, No Schema Vertica.

    The **Table List** is displayed.
2. From the **Table List,** drag the required **table** onto to the **right pane (Canvas)**. For example, dim\_region.
3. On the **Top Menu**, click the **Relationship** <img src="../../../.gitbook/assets/image (3243).png" alt="" data-size="line"> button.

The **Relations Properties** screen is displayed.

4. On the **Relationship Properties** screen, click the **Add Relationship** button.

The **Define Relationship LDM** drop-down box is displayed.

5. On the **Define Relationship LDM** drop-down box, in the **Source** section, select the **Source Table** and **Columns**. For example, ebit\_combine\_fact\_table and project\_key.
6. In the **Target** section, select the **Target Table** and **Columns**. For example, dim\_region and region\_key.
7. From the **Relationship** drop-down box, select **Many To One.**&#x20;
8. Click the **Save** button.

The relationships are defined. See the below image.

<figure><img src="../../../.gitbook/assets/image (3244).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Save LDM**

1. On the **Top Menu** right corner, click the **Save** button.

The **Save LDM** dialogue box displayed.

2. On the **Save LDM** dialogue box, in the **Add Metadata** tab, specify all the required details.

> <mark style="color:red;">**Note:**</mark> If required, you can modify the **Business Name** as required.

3. Click the **Next** button.

The **Add Governance** tab is opened.

4. On the **Add Governance** tab, specify the **Business Owner, Technical Owner**, and then click the **Next** button.

The **Review & Submit** tab is opened.

5. On the **Review & Submit** tab, enter name and description for the LDM, and then click the Finish **button**.

The logical data model is created and reflected on the Business Models page. It is available in the Dashboard Designer page to create dashboard.
{% endstep %}

{% step %}
**Create Dashboard**

1. On the **SCIKIQ left menu**, go to **SCIKIQ CONSUME**, and then click **Dashboard Designer**.

The **Dashboard Designer** page is displayed.

2. On the **Dashboard Designer** page, select the required template.

The **Source Data** drop-down is activated on the left pane.&#x20;

3. On the **left pane**, **Source Data** drop-down, select **Dataset**.

The **Dataset** drop-down box is displayed.

4. From the **Dataset** drop-down box, select the **logical model** which you have already created.

<figure><img src="../../../.gitbook/assets/image (3245).png" alt=""><figcaption></figcaption></figure>

5. Create the Dashboard using **logic**al model.

> Note: To know how to create a dashboard, click [**Dashboard Designer**](../../openapi/dashboard-designer/).

The dashboard is created and displayed in the **Dashboard List** page.

6. Now, go to **SCIKIQ CONSUME**, and click **Dashboard List**.

The **Dashboard List** page is displayed.

7. On the **Dashboard List** page, **search** for the **logical data model**, and then click the **View** icon corresponding to it.

<figure><img src="../../../.gitbook/assets/image (3247).png" alt=""><figcaption></figcaption></figure>

The Dashboard is displayed. Here it is OP14010 Multi-Connection.

<figure><img src="../../../.gitbook/assets/image (3253).png" alt=""><figcaption></figcaption></figure>

**Dashboard description:**

* A table showing actual amounts by project and region (50 rows).
* A bar chart comparing actual and budget amounts by region.
* Records with region keys that do not have a matching entry in the Region table (10 rows, totalling 35,000) are displayed under a **Blank** region instead of being excluded from the report.
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Adding an Uploaded File from S3" %}
**Overview**

The following example demonstrates how to include regional targets (a CSV file uploaded under **Data Source**) and regional managers (an Excel file stored in an **S3 bucket**) alongside database tables in a single Logical Data Model.

**Procedure**

The procedure involves navigating to the **Logical Data Model** page and selecting the required **Source Type** and **Source Category**. The two database tables are added to the canvas, and a relationship is defined between them. Next, **FileUpload** is selected, and the required SharePoint file is added to the canvas. A relationship is then defined between the file and the relevant database table.

Similarly, the required file is selected from **Amazon S3** and added to the canvas, followed by defining the required relationship. Once all tables and relationships are configured, the **Logical Data Model (LDM)** is saved. The dashboard can then be opened to view and analyse data from the selected sources.

Follow the step-by-step instructions below to complete the process.

{% stepper %}
{% step %}
**Drag Database Tables onto the Canvas**&#x20;

1. Navigate to **Logical Data Model** page.
2. On the **Logical Data Model** page, from the **Select Source Type** drop-down box, select either **Datasource** or **Assets**. For example, Datasource.
3. From the **Source Category** drop-down box, select **RDBMS**.
4. From the **Select Connection** drop-down box, select the required connection. For example, No Schema Vertica.

The **Table List** is displayed.

5. From the **Table List,** drag the required **tables** onto to the **right pane (Canvas)**. For example, ebit\_combine\_fact\_table and dim\_project.
{% endstep %}

{% step %}
**Define Relationship between Database Tables**

1. On the **Top Menu of Logical Data Model,** click the **Relationship** <img src="../../../.gitbook/assets/image (3243).png" alt="" data-size="line"> button.

The **Define Relationship LDM** drop-down box is displayed.

2. On the **Define Relationship LDM** drop-down box, in the **Source** section, select the **Source Table** and **Columns**. For example, ebit\_combine\_fact\_table.project\_key.
3. In the **Target** section, select the **Target Table** and **Columns**. For example, dim\_project.Project\_key.
4. From the **Relationship** drop-down box, select Many To On&#x65;**.**&#x20;
5. Click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (3249).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Select FileUpload and Drag the Selected File onto the Canvas**

1. From the **Select Source Category** drop-down box, select **Data Source**.
2. From the **Select Connection** drop-down box, select **File Upload (CSV/Excel)**.
3. From the **Select Connection** drop-down box, select **OP14010 Region targets**.

The **Table List** is displayed.

4. From the **Table List,** drag the **required file** onto the canvas. Here it is OP14010 Region targets.&#x20;
{% endstep %}

{% step %}
**Define Relationship between Database Tables and Selected File**

1. On the **Top Menu**, click the **Relationship** <img src="../../../.gitbook/assets/image (3243).png" alt="" data-size="line"> button.

The **Relationship Properties** screen is displayed.

2. On the **Relationship Properties** screen, in the **Source** section, select the **Source Table** and **Columns**. For example, ebit\_combine\_fact\_table and project\_key.
3. In the **Target** section, select the **Target Table** and **Columns**. For example, dim\_project and project\_key.
4. From the **Relationship** drop-down box, select **Many To One.**&#x20;
5. Click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (3224).png" alt=""><figcaption></figcaption></figure>

The relationship is defined. See the image below.

<figure><img src="../../../.gitbook/assets/image (3225).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Select a File from Amazon S3 and Drag it onto Canvas**

1. From the **Select Source Category** drop-down box, select **Data Source**.
2. From the **Select Storage** drop-down box, select **File Storage**.
3. From the **Select Connection** drop-down box, select the required **connection**. For example, VS Bucket S3 Store.
4. From the **Select Bucket** drop-down box, select the required **bucket**. For example, Connection Bucket.
5. From the **File Type** drop-down box, select the required **file format** choosing from **All Table Files, CSV, Excel,** or **Parquet.** For example, All Table Files.
6. Click the **Connect** button.

The list of available folders are displayed.

7. In the **Drag to Canvas** field, enter the required folder. For example, Scikiq71.

The required folder is displayed below.

8. Open the displayed folder, and then drag the desired file onto the canvas. Here it is op14010\_region\_managers.xlsx.

<figure><img src="../../../.gitbook/assets/image (3228).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> If you want to view the file path, click the **Gear** icon. See the below image.

<figure><img src="../../../.gitbook/assets/image (3229).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Define Relationship**&#x20;

1. On the **Top Menu**, click the **Relationship** <img src="../../../.gitbook/assets/image (3243).png" alt="" data-size="line"> button.

The **Relationship Properties** screen is displayed.

2. On the **Relationship Properties** screen, in the **Source** section, select the **Source Table** and **Columns**. For example, op14010\_region\_managers.xlsx and region\_key.
3. In the **Target** section, select the **Target Table** and **Columns**. For example, dim\_region (No Schema Vertica) and region\_key.
4. From the **Relationship** drop-down box, select One To On&#x65;**.**&#x20;
5. Click the **Save** button.

The relationship is defined.

<figure><img src="../../../.gitbook/assets/image (3254).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> If you want to view the data of a table, click the **Preview Data** icon on that table. See the below image.
>
> ![](<../../../.gitbook/assets/image (3232).png>)
{% endstep %}

{% step %}
**Save LDM**

* Finally, click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (3233).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Create Dashboard**

1. On the **SCIKIQ left menu**, go to **SCIKIQ CONSUME**, and then click **Dashboard Designer**.

The **Dashboard Designer** page is displayed.

2. On the **Dashboard Designer** page, select the required template.

The **Source Data** drop-down is activated on the left pane.&#x20;

3. On the **left pane**, **Source Data** drop-down, select **Dataset**.

The **Dataset** drop-down box is displayed.

4. From the **Dataset** drop-down box, select the **logic**al model that has been created using the tables mentioned above.

<figure><img src="../../../.gitbook/assets/image (3245).png" alt=""><figcaption></figcaption></figure>

5. Create the Dashboard using **logic**al model.

> Note: To know how to create a dashboard, click [**Dashboard Designer**](../../openapi/dashboard-designer/).

The dashboard is created and displayed in the **Dashboard List** page.

6. Under **SCIKIQ CONSUME**, click **Dashboard List**.

The **Dashboard List** page is displayed.

7. On the **Dashboard List** page, in the **Search** field, enter the data model name. Here it is OP14010 Mixed sources.

The dashboard is displayed.

8. Now, click the **View** icon corresponding the dashboard.

The OP14010 Mixed sources dashboard is displayed.

<figure><img src="../../../.gitbook/assets/image (3235).png" alt=""><figcaption></figcaption></figure>

**Dashboard Description**

1. **Actual Amount by Region:** The table displays actual amounts for the eight regions that have assigned managers. For example, Delhi (Manager A) has an actual amount of 81,709,711.
2. **Unknown Region:** A blank row displays an actual amount of 35,000 for records with region keys that do not have matching entries in the Region table.
3. **Regional Targets:** The bar chart displays targets for all 14 regions included in the uploaded file. Delhi has the highest target at 80,000,000.50.
4. **Calculated Field:** The text calculated field op14010\_manager\_region combines the manager name and region name.
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Joining a SharePoint File with a Database Table" %}
**Overview**

The following example demonstrates how to establish a relationship between a SharePoint file and a database table within a single Logical Data Model (LDM).

In this example, the SharePoint file (CSV) contains records of 5,000 bank customers, while the database table is stored in Vertica. By adding both data sources to the LDM and defining a relationship between them, customer information from the SharePoint file can be associated with the corresponding records in the Vertica table.&#x20;

This enables to analyse data from both sources through a unified model.

**Procedure**

The process of adding a SharePoint file to a database table involves navigating to the **Logical Data Model** page and selecting the required **Source Type** and **Source Category**.

The required database table is first added to the canvas, followed by the SharePoint file. A relationship is then defined between the database table and the SharePoint file.

Once the **Logical Data Model (LDM)** is saved, the dashboard can be opened to view and analyse data from both sources.

Follow the below step-by-step instructions:

{% stepper %}
{% step %}
**Drag a Database Table onto the Canvas**

1. Navigate to **Logical Data Model** page.
2. On the **Logical Data Model** page, from the **Select Source Type** drop-down box, select either **Datasource** or **Assets**. For example, Datasource.
3. From the **Source Category** drop-down box, select **RDBMS**.
4. From the **Select Connection** drop-down box, select the required connection. For example, No Schema Vertica.

The **Table List** is displayed.

5. From the **Table List,** drag the required **table** onto to the **right pane (Canvas)**. For example, dim\_region.

<figure><img src="../../../.gitbook/assets/image (3236).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Drag a SharePoint File onto the Canvas**

1. On the **Logical Data Model** page, from the **Source Category** drop-down box, select **File Storage**.
2. From the **Select Connection** drop-down box, select the **SharePoint** connection. For example, SHAREPOINT\_vlt.

The **SharePoint** file folder is displayed.

3. Open the SharePoint folder, drag the required file onto to the **right pane (Canvas)**. For example, bank\_customer.csv.

<figure><img src="../../../.gitbook/assets/image (3237).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Define Relationship between Database Table and SharePoint File**

1. On the **Top Menu of Logical Data Model,** click the **Relationship** <img src="../../../.gitbook/assets/image (3243).png" alt="" data-size="line"> button.

The **Define Relationship LDM** drop-down box is displayed.

2. On the **Define Relationship LDM** drop-down box, in the **Source** section, select the **Source Table** and **Columns**. For example,bank\_customers.csv and State.
3. In the **Target** section, select the **Target Table** and **Columns**. For example, dim\_region and region\_name.
4. From the **Relationship** drop-down box, select **Many To One.**&#x20;
5. Click the **Save** button.

The relationship is defined. See the image below.

<figure><img src="../../../.gitbook/assets/image (3238).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Save LDM**

* Finally, click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (3255).png" alt=""><figcaption></figcaption></figure>

The logical data model is created.
{% endstep %}

{% step %}
**Create Dashboard**

1. On the **SCIKIQ left menu**, go to **SCIKIQ CONSUME**, and then click **Dashboard Designer**.

The **Dashboard Designer** page is displayed.

2. On the **Dashboard Designer** page, select the required template.

The **Source Data** drop-down is activated on the left pane.&#x20;

3. On the **left pane**, **Source Data** drop-down, select **Dataset**.

The **Dataset** drop-down box is displayed.

4. From the **Dataset** drop-down box, select the **logic**al model that has been created using the tables mentioned above.
5. Create the Dashboard using **logic**al model.

<figure><img src="../../../.gitbook/assets/image (3256).png" alt=""><figcaption></figcaption></figure>

> Note: To know how to create a dashboard, click [**Dashboard Designer**](../../openapi/dashboard-designer/).

The dashboard is created and displayed in the **Dashboard List** page.

6. Go back to **SCIKIQ CONSUME**, click **Dashboard List**.

The **Dashboard List** page is displayed.

7. On the **Dashboard List** page, in the **Search** field, enter the data model name. Here it is OP13224 Database and SharePoint dashboard.

The dashboard is displayed.

8. Now, click the **View** icon corresponding the dashboard

The OP13224 Database and SharePoint dashboard is displayed.

<figure><img src="../../../.gitbook/assets/image (3257).png" alt=""><figcaption></figcaption></figure>

**Dashboard Description**

**1. Regional Summary:** Displays the account balance, number of cards, and loan amount for 11 regions.

**2. Unmatched Records:** A total of 249 customers appear under a blank region because the SharePoint file contains the state name as Telangana, while the `dim_region` table contains it as Telengana.

**3. Impact of the Mismatch:** These unmatched records have a total account balance of 612,178,682.34 and 580 cards.

**4. Resolution:** Correcting the spelling in either data source ensures that these customers are mapped to the correct region during the next data load.
{% endstep %}
{% endstepper %}
{% endtab %}
{% endtabs %}



***

### Related Topics

* [**Managing Logical Data Models**](managing-logical-data-models.md)
