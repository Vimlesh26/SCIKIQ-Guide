---
hidden: true
icon: circle-share-nodes
---

# Copy of Configuring Input Nodes

**Contents**

* [**Instructions for Using this Page**](copy-of-configuring-input-nodes.md#instructions-for-using-this-page)
* [**Overview**](copy-of-configuring-input-nodes.md#overview)
* [**SCIKIQ Input Nodes**](copy-of-configuring-input-nodes.md#scikiq-input-nodes)
  * [**Database Input Node**](copy-of-configuring-input-nodes.md#configuring-database-node)
  * [**File Input Node**](copy-of-configuring-input-nodes.md#configuring-file-input-node)
  * [**Query Input Node (SQL)**](copy-of-configuring-input-nodes.md#configuring-query-input-node)
  * [**API Input Node**](copy-of-configuring-input-nodes.md#configuring-api-input-node)
  * [**SAP App Input Node**](copy-of-configuring-input-nodes.md#configuring-sap-app-node)
  * [**NoSQL Input Node**](copy-of-configuring-input-nodes.md#configuring-no-sql-node)
  * [**UCM File Loader Input Node**](copy-of-configuring-input-nodes.md#configuring-ucm-file-loader)
  * [**GraphQL Input Node**](copy-of-configuring-input-nodes.md#configuring-ucm-file-loader)
* [**Related Topics**](copy-of-configuring-input-nodes.md#related-topics)

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]

***

### Overview

The purpose of configuring an input node while creating a delta pipeline connection is to define what data the system should read from the source and how it should be accessed. It helps the pipeline understand:

* **Where the data is coming from** (for example, a specific database, file, table, or API)
* **What data to read** (such as selected tables, files, or columns)
* **How to read the data** (like authentication details, formats, filters, or query conditions)

***

### SCIKIQ Input Nodes

SCIKIQ supports the below mentioned input nodes:

<table><thead><tr><th width="246" valign="top">Input Nodes</th><th width="409" valign="top">Description</th></tr></thead><tbody><tr><td valign="top"><img src="../../../../.gitbook/assets/image (157).png" alt=""></td><td valign="top"><p></p><p>The <strong>Input Nodes</strong> collect data from different systems and feed it into the data pipeline for processing. </p><p></p><p><strong>Purpose of Each Input Node:</strong></p><p></p><ul><li><a href="/broken/pages/UZQ10sI7DoyEEhybN9of"><strong>Database Input</strong></a> – Extracts structured data from relational databases</li><li><a href="/broken/pages/0GPrLZaKMVvtp5vGwiPV"><strong>File Input</strong></a> – Reads data from files like CSV, Excel, JSON, or XML</li><li><a href="/broken/pages/beOOie3BmRTrVDJoMdXc"><strong>Query Input</strong></a> – Fetches data by running custom SQL queries</li><li><a href="/broken/pages/t5gJrVQdFC7fkFlj6ha3"><strong>API Input</strong></a> – Pulls data from external applications using REST APIs</li><li><a href="/broken/pages/5OlbyxVoA1MWuZnM7nBk"><strong>GraphQL Input</strong></a> – Retrieves data using flexible GraphQL queries</li><li><a href="/broken/pages/qPMY0gYgxwkI8LvCgCiE"><strong>SAP APP SInput</strong></a> – Connects to SAP systems to extract business data</li><li><a href="/broken/pages/e53opWC4pvYSV8kNVx7F"><strong>NoSQL Input</strong></a> – Reads data from NoSQL databases such as MongoDB</li><li><a href="/broken/pages/PRV9f5CQlUfOJgGeYBSm"><strong>UCM File Loader</strong></a> – Loads files stored in UCM repositories into the pipeline</li></ul></td></tr></tbody></table>

### Configuring Database Node

#### Overview

The **Database Node** is configured when the source data resides in a database. It functions as a core component for data interaction within the pipeline, providing structured connectivity, data refinement, validation capabilities, and controlled data flow management. Accurate configuration of the Database Node is required to ensure reliable, efficient, and consistent pipeline execution.

This page explains how to configure a Database Node to create a delta pipeline. The configuration can be completed by following a sequence of guided steps.&#x20;

The below table provides a brief overview of each step involved in the process.

<table><thead><tr><th width="258">Step</th><th>Description</th></tr></thead><tbody><tr><td><a href="copy-of-configuring-input-nodes.md#select-database-input-node">Select Database Input</a></td><td>This is the first step in the process. As part of this, you will drag the Database Input Node from the <a data-footnote-ref href="#user-content-fn-2"><mark style="color:blue;"><strong>Node Palette</strong></mark></a> and then place it on the in the Main Workspace.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#select-database-type">Select Database Type</a></td><td>As part of this step, you will select either <a data-footnote-ref href="#user-content-fn-3"><mark style="color:blue;"><strong>Datasource</strong></mark></a> or <a data-footnote-ref href="#user-content-fn-4"><mark style="color:blue;"><strong>Asset</strong></mark></a> to define how the database will be used within the pipeline. </td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#select-columns">Select Columns</a></td><td>As part of this step, you will select the required columns to define which fields are extracted from the selected database type. </td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#apply-filters">Apply Filters</a></td><td>Applying <strong>Filters</strong> allow you retrieve only <strong>relevant data</strong> based on defined criteria and exclude <strong>unnecessary or unwanted records.</strong></td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#apply-limit-operator">Apply Limit Operator</a></td><td>Applying the <strong>Limit</strong> operator enable you to define an <strong>upper limit</strong> on the number of records retrieved. </td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#apply-order-operator">Apply Order Operator</a></td><td>Applying the <strong>Order</strong> operator enables to define the <strong>sort order</strong> of records based on one or more selected columns, in either <strong>ascending</strong> or <strong>descending order</strong>.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#apply-group-operator">Apply Group Operator</a></td><td>Applying the <strong>Group</strong> operator enables to aggregate data based on selected columns, facilitating the summarization of large datasets for enhanced analytical insights.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#preview-data">Preview Data</a></td><td><strong>Preview</strong> allows you to verify that the <strong>Database Input Node</strong> is correctly configured and is extracting the expected data from the selected table before the pipeline is executed.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#save-pipeline">Save Pipeline</a></td><td><strong>Saving</strong> ensures that all input node settings are retained and correctly applied during pipeline runs.</td></tr></tbody></table>

***

#### Procedure

The expandable panels below provide guided assistance for each step in the configuration process. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Select Database Input Node</strong></summary>

**Purpose:**

The purpose of selecting the **Database Node** while creating a delta pipeline is to define the database as the data source for the pipeline.

**Procedure:**

As part of selecting the **Database Node**, you need to drag it from the **Node Palette** and then place it on the in the Main Workspace. Once added, the **Database Type** and **Schema Properties fields** are displayed in the left pane.&#x20;

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

<figure><img src="../../../../.gitbook/assets/S.png" alt=""><figcaption><p>Create Delta Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

<figure><img src="../../../../.gitbook/assets/S (1).png" alt=""><figcaption><p>Input Menu Item</p></figcaption></figure>

The [<mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-5)[^5] is displayed. See the image below.

<figure><img src="../../../../.gitbook/assets/S (2).png" alt=""><figcaption><p>Node Palette</p></figcaption></figure>

3. From the **Node Palette**, select the **Database Input,** and drag it onto the **Main Workspace**.

<figure><img src="../../../../.gitbook/assets/S (3).png" alt=""><figcaption><p>Selecting Database Input</p></figcaption></figure>

The Input fields are displayed on the Left Pane.

</details>

<details>

<summary><strong>Select Database Type and Connection</strong></summary>

**Purpose:**

The purpose of configuring a **Database Type** (such as **Data Source** or **Asset**) is to define **how the database will be used within the pipeline**.

**Procedure:**

As part of the procedure, you need to select either **Data Source** or **Asset** based on your requirement.  Selecting the **Datasource** option connects to an external database whereas the **Assets** option use pre-configured datasets stored within SCIKIQ. Once the database type is selected, the tables pertaining to the selected data source or asset are available in the Schema Properties section on the Left Pane.

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

A. On the **Left Pane**, from the **Data Type** drop-down box, select either **Datasource** or **Assets.**

&#x20;B. If you wish to choose **Datasource,** then from the **Datasource** drop-down box, select the required **datasource connection.**

<figure><img src="../../../../.gitbook/assets/S (4).png" alt=""><figcaption><p>Selecting Datasource Connection</p></figcaption></figure>

{% hint style="info" %}
**Tip:**&#x20;

* If required, you can create a new data source connection by clicking the **Create New Connection** ![](<../../../../.gitbook/assets/image (158).png>) button. To learn **how to create a new data source connection**, click [**Creating a New Data Source Connection**](/broken/pages/Ga8WoiowoXOkY4RtBNpS).
{% endhint %}

C. If you want **Asset,** then select the required **asset** from the **Asset** drop-down box.

{% hint style="info" %}
**Tip:** &#x20;

* If required, you can create new asset by clicking the **Create New Asset** ![](<../../../../.gitbook/assets/image (159).png>)button. To learn **how to create a new asset**, click [**Creating an Asset**](/broken/pages/m9HgqxqwHFgvtRGcp0ij)**.**
{% endhint %}

The tables pertaining to the selected data source or asset are populated in the Schema Properties section on the Left Pane.

</details>

<details>

<summary><strong>Select Columns</strong></summary>

**Purpose:**&#x20;

During the configuration of the **Database Input Node**, **column selection** is used to **specify the fields to be extracted**.

**Procedure:**

As part of the procedure, the relevant collection or table is selected first, after which the available fields are displayed. From this list, the required fields can be selected. Duplicate records can be removed using the **Distinct** option, and **Data Quality (DQ)** rules can be applied as required.

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1.In the **Schema Properties** section, from the **Table** drop-down box, select the **required table**. See the below image.

The list of columns pertaining to the selected table are displayed.&#x20;

2.From the **list of columns**, select the **required columns**.

{% hint style="info" %}
**Tip:** You can select a **single column, multiple columns,** or **all columns** based on your requirement. Selecting the **Select All** checkbox allows you to select all tables at once. See the **ticked checkbox** in the image below.

![](<../../../../.gitbook/assets/image (160).png>)
{% endhint %}

3.If you want to **add a new column**, click the **New Column** ![](<../../../../.gitbook/assets/image (161).png>)button.

The column is added.&#x20;

{% hint style="info" %}
**Tip:** You can add multiple columns based on your requirement.
{% endhint %}

4.Click the **Distinct** ![](<../../../../.gitbook/assets/image (162).png>)button to remove the duplicates.

5.If you want apply **DQ Rules**, click the **DQ Rules** ![](<../../../../.gitbook/assets/image (163).png>)button.&#x20;

{% hint style="info" %}
**Tip:** Click **here** to know how to apply DQ Rules.
{% endhint %}

6.Click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (5).png" alt=""><figcaption><p>Selecting Columns</p></figcaption></figure>

</details>

<details>

<summary><strong>Apply Filters Operator</strong></summary>

**Purpose:**

The purpose of **Filters** is to control which records are included in data processing by applying specific conditions to the dataset. In practical terms, filters allow retrieve only **relevant data** based on defined criteria and exclude **unnecessary or unwanted records.**

**Procedure:**

As part of the using the filters, you need to define the **logical relationship between multiple conditions** by selecting either **AND** or **OR** and then define the **precise data filtering criteria.** Based on the requirement, you can use parameters and variables as well.&#x20;

The below step-by-step instructions describe the procedure of using the filters:&#x20;

**Step-by-Step instructions:**

1. In the **Schema Properties** section, Click the **Filters** icon, and then click the **Add/Edit Filter** button.

<figure><img src="../../../../.gitbook/assets/S (6).png" alt="" width="446"><figcaption><p>Scheme Properties - Filters Icon</p></figcaption></figure>

{% hint style="info" %}
**Tip:** To view the **Schema Properties** section in an expanded view, click the **Toggle Full Screen** icon. See the highlighted part in red the below image.

<img src="../../../../.gitbook/assets/S (7).png" alt="" data-size="original">
{% endhint %}

The **Add/Edit Filter** dialogue box is displayed.

2\. On the **Add/Edit Filter** dialogue box (See the image below):

<figure><img src="../../../../.gitbook/assets/S (8).png" alt="" width="563"><figcaption><p>Configuring Filters</p></figcaption></figure>

A. **Select** **Add or Edit**&#x20;

{% hint style="info" %}
**Tip:** The purpose of using AND or OR is to define the logical relationship between multiple conditions.
{% endhint %}

* Select **AND** if you want all conditions to be true for a record to be selected.&#x20;
* Select **OR** if you want any one of the conditions can be true for a record to be selected.

B. **Define Filter Condition**&#x20;

{% hint style="info" %}
**Tip:** Filtering condition allows to define **precise data filtering criteria** (For example, Date less than 2024-01-01.
{% endhint %}

* From the **Columns** drop-down box, select the **Column** to which the filter should be applied.
* From the **Operator** drop-down box, select the **required operator**.&#x20;
* In the **Value** field, enter the required **value**

C. **To add a new condition line** (For example, Revenue ID less than 10101)&#x20;

* Click the **Add Filter** ![](<../../../../.gitbook/assets/image (164).png>) button.&#x20;

D. **To add a nested filter logic** (For example, Revenue ID less than 10101 and Value less than 10000)

* Click the **Add Filter Group** ![](<../../../../.gitbook/assets/image (165).png>)  button.&#x20;

E. **To use dynamic parameters in filters**

* Prefix the parameter with `@@` in the ETL design.

{% hint style="info" %}
**Tip:** The purpose of using Parameters is to enable **dynamic filtering** at runtime and allows values to be passed externally.
{% endhint %}

F. **To use ETL variables in filters**

* Prefix the variable with `##`

{% hint style="info" %}
**Tip:** Using variables supports reusable and internally computed values that are **generated within the system and can be used multiple times across the pipeline** without being hard-coded.
{% endhint %}

4. Finally, click the **Save** button.

</details>

<details>

<summary><strong>Apply Limit Operator</strong></summary>

**Purpose:**

You can use the **Limit** operator to define an **upper limit** on the number of records retrieved from a dataset. This functionality is commonly used to optimize performance, support testing activities, and manage data processing volume before transformations are applied.

**Procedure:**

As part of the procedure, you need to select either the system-defined upper limit or the custom option. Once selected, the upper limit for record retrieval is established.

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. In the **Schema Properties** section, select the **Limit** icon, and then define the limit choosing from **Limit By 10, Limit By 500, Limit By 1000, Limit By 2000,** or **Custom**.&#x20;

<figure><img src="../../../../.gitbook/assets/S (9).png" alt=""><figcaption><p>Defining Record Retrieval Limit</p></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> If you wish to define a **custom** limit, then select the **Custom** option, and specify the custom limit. A **custom limit** is a **user-defined restriction on the number of records retrieved from a dataset**, rather than using a system-defined default limit.

2. Click the **Preview** tab to check the defined number of records.

</details>

<details>

<summary><strong>Apply Order</strong> <strong>Operator</strong></summary>

**Purpose:**

The **Order** operator enables to define the **sort order** of records based on one or more selected columns, in either **ascending** or **descending order**. This functionality supports structured data preparation prior to transformation, ensuring that datasets follow a consistent and meaningful sequence for downstream analysis and processing.

**Procedure:**

As part of the procedure, you need to select the **Order** icon and specify the record order by choosing either **ASC option** or **DESC option**. Once done, the records are sorted according to the specified order.

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. In the **Schema Properties** section, select the **Order** icon, and then from the **Column Name** drop-down box, select the **required value**. For example, Amount.
2. From the **Order By** drop-down box, select [<mark style="color:blue;">**ASC**</mark>](#user-content-fn-6)[^6] or [<mark style="color:blue;">**DESC**</mark>](#user-content-fn-7)[^7] based on your requiremen&#x74;**.**

{% hint style="info" %}
**Tip:** ASC refers to ascending order, while DESC refers to descending order.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (10).png" alt=""><figcaption><p>Specifying the Order</p></figcaption></figure>

4. Click the **Preview** tab to view the data.

</details>

<details>

<summary><strong>Apply Group</strong> <strong>Operator</strong></summary>

**Purpose:**

The **Group** operator in the pipeline enables to aggregate data based on selected columns, facilitating the summarization of large datasets for enhanced analytical insights.&#x20;

It supports standard aggregation operations such as SUM, COUNT, AVG, MAX, and MIN on grouped records.&#x20;

This functionality ensures logical data structuring, reduces redundancy, and improves the efficiency of reporting and downstream data processing.&#x20;

**Procedure:**

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. In the **Schema Properties** section, select the **Group** icon, and then select the **required columns**.&#x20;

<figure><img src="../../../../.gitbook/assets/S (11).png" alt=""><figcaption><p>Specifying Group By Option</p></figcaption></figure>

2. Click the **Preview** tab to view the data.

</details>

<details>

<summary><strong>Preview Data</strong></summary>

**Purpose:**

Previewing allows you to verify that the **Database Input Node** is correctly configured and is extracting the expected data from the selected table before the pipeline is executed.

**Procedure:**

The below step-by-step instructions describe the procedure:

* On the **Right Pane**, click the **Preview** icon on the top of **Database Input Node.**

<figure><img src="../../../../.gitbook/assets/S (12).png" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

The data is displayed on the Preview tab.

</details>

<details>

<summary><strong>Save Pipeline</strong></summary>

**Purpose**

After selecting the input node, you need to save the pipeline to persist its configuration and make it available for execution. Saving ensures that all input node settings are retained and correctly applied during pipeline runs.

**Procedure**

As part of the procedure, you need to provide a **name** for the pipeline along with specifying the **summary** of the delta pipeline and the **metadata** including **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (14).png" alt="" width="563"><figcaption></figcaption></figure>

The Pipeline is saved.

</details>

### Configuring File Input Node

#### Overview

The **File Input Node** is used when the source data for a pipeline resides in files rather than in databases. It enables the pipeline to **read, interpret, and ingest data from file-based sources** such as **CSV, Excel, JSON, XML**, or other supported formats.

The below table provides a brief overview of each step involved in the process.

<table><thead><tr><th width="237" valign="top">Step</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top"><a href="copy-of-configuring-input-nodes.md#select-file-input-node">Select File Input Node</a></td><td valign="top">This is the first step in the <strong>File Input Node</strong> configuration process. As part of this step, you will drag <strong>File Input</strong> from the <a data-footnote-ref href="#user-content-fn-8"><mark style="color:blue;">Node Palette</mark></a><mark style="color:blue;">,</mark> and then place it on the in the <strong>Main Workspace</strong>.</td></tr><tr><td valign="top"><a href="copy-of-configuring-input-nodes.md#configure-file-upload-and-preview-data">Configure File Upload and Preview Data</a></td><td valign="top">The <strong>File Upload</strong> type enables you to upload the files such as <strong>CSV, XLS</strong>, etc. directly from your local system. As part of this step, you will select the <strong>File Upload</strong> <strong>Type</strong>, define <strong>Schema Properties</strong>, and <strong>Preview</strong> data.</td></tr><tr><td valign="top"><a href="copy-of-configuring-input-nodes.md#configure-file-storage-and-preview-data">Configure File Storage and Preview Data</a></td><td valign="top">The <strong>File Storage</strong> type allows you to connect to external storage locations such as <strong>Hadoop (HDFS), SFTP</strong>, and <strong>Cloud-based Storage services</strong>. In this step, you will select <strong>File Type,</strong> establish <strong>Connection,</strong> choose <strong>File,</strong> configure <strong>Parameters,</strong> define <strong>Schema Properties,</strong> and <strong>Preview Data</strong>.</td></tr><tr><td valign="top"><a href="copy-of-configuring-input-nodes.md#save-pipeline">Save Pipeline</a></td><td valign="top"><strong>Saving</strong> ensures that all input node settings are retained and correctly applied during pipeline runs.</td></tr></tbody></table>

#### Procedure

The expandable panels below provide guided assistance for each step in the configuration process. Expand the panels to view detailed, step-by-step instructions.

> <mark style="color:red;">**Note:**</mark> You can configure either File Upload or File Storage, but not both simultaneously. Select the appropriate option based on your requirements.

<details>

<summary><strong>Select File Input Node</strong></summary>

**Purpose:**

The purpose of selecting the **File Input Node** while creating a delta pipeline is to define the file as the source of data for the pipeline.

**Procedure:**

As part of adding the **File Put Node**, you need to drag it from the **Node Palette** and then place it on the in the Main Workspace. Once added, the **FileType** and **Schema Properties fields** are displayed in the left pane.&#x20;

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

<figure><img src="../../../../.gitbook/assets/S.png" alt=""><figcaption><p>Create Delta Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

<figure><img src="../../../../.gitbook/assets/S (1).png" alt=""><figcaption><p>Input Menu Item</p></figcaption></figure>

The [<mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-5)[^5] is displayed. See the image below.

<figure><img src="../../../../.gitbook/assets/S (2).png" alt=""><figcaption><p>Node Palette</p></figcaption></figure>

3. From the **Node Palette**, select the **File Input,** and drag it onto the **Main Workspace.**

<figure><img src="../../../../.gitbook/assets/S (15).png" alt="" width="465"><figcaption><p>Adding File Input Node</p></figcaption></figure>

The Input fields are displayed on the Left Pane.

</details>

<details>

<summary><strong>Configure File Upload and Preview Data</strong></summary>

**Purpose:**

The **File Upload** type enables you to upload the files such as **CSV, XLS**, etc. directly from your local system.&#x20;

**Procedure:**

The procedure to configure the File Upload type includes - **Select File Upload, Define Schema Properties,** and **Preview.**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

**1.Select File Upload**

A. On the **Left Pane**, from the **Select File Type** drop-down box, select **File Upload.**

The available files are displayed in the drop-down box below.

B. From the **list of available files**, select the **required file**.

<figure><img src="../../../../.gitbook/assets/S (16).png" alt=""><figcaption><p>Selecting File Upload </p></figcaption></figure>

The table data is displayed with a list of columns in the Schema Properties section.&#x20;

**2.Define Schema Properties**

A. In the **Schema Properties** section, from the **list of columns**, select the **required columns**.&#x20;

B. Enable the **Distinct** option to remove the duplicates.

<figure><img src="../../../../.gitbook/assets/S (17).png" alt=""><figcaption><p>Selecting Columns</p></figcaption></figure>

{% hint style="info" %}
**Tip:** You can select a **single column, multiple columns,** or **all columns** based on your requirement. Selecting the **Select All** checkbox allows you to select all columns at once. See the **ticked checkbox** in the image below.

![](<../../../../.gitbook/assets/image (166).png>)
{% endhint %}

**3.Preview Data**

* On the **Right Pane**, click **Preview** on the **Input Node**.

<figure><img src="../../../../.gitbook/assets/S (18).png" alt=""><figcaption><p>Input Node - Preview Option</p></figcaption></figure>

The data is displayed on the Preview tab below. See the below image.

<figure><img src="../../../../.gitbook/assets/S (19).png" alt=""><figcaption><p>Preview Tab - Display of Data</p></figcaption></figure>

</details>

<details>

<summary><strong>Configure File Storage and Preview Data</strong></summary>

**Purpose:**

The **File Storage** type enables connection to external storage locations such as Hadoop (HDFS), SFTP, and cloud-based storage services.&#x20;

**Procedure:**

The procedure to configure File Storage includes - **Select File Type, Establish Connection, Select File, Configure Parameters, Define Schema Properties,** and **Preview Data.**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

**A. Select File Type**

{% hint style="info" %}
**Tip:** To view the **Select File Type** section in full screen, click the **Toggle Full Screen** icon.

<img src="../../../../.gitbook/assets/S (20).png" alt="" data-size="original">
{% endhint %}

1. On the **Left Pane**, from the **Select File Type** drop-down box, select **File Storage.**
2. From the **Select Storage** drop-down box, select the **required storage**. For example, DataScikiq File Storage (S3).

<figure><img src="../../../../.gitbook/assets/S (21).png" alt=""><figcaption><p>Selecting File Storage Type</p></figcaption></figure>

The available files are displayed in the **Select** drop-down box below.

**B. Establish Connection**

1. From the **list of available files**, select the **required file.**&#x20;
2. From the **File Extension** drop-down box, select the **required file extension**. For example, CSV.
3. Next, select **Structured** or **Unstructured.**

{% hint style="info" %}
**Tip:**&#x20;

* **Structured files** store data in a **fixed, well-defined format**, usually in rows and columns.
* **Unstructured files** do **not follow a fixed schema** or tabular format. The data is free-form and varies from file to file.
{% endhint %}

4. Click the **Connect** button to establish the connection.

<figure><img src="../../../../.gitbook/assets/S (22).png" alt=""><figcaption><p> Establishing Connection</p></figcaption></figure>

The available folders and files are displayed in the ROOT section.

**C. Select File**

1. On the **Select File Type** screen, in the **ROOT** section, from the **available folders**, select the **folder** where the **file** is available.&#x20;

<figure><img src="../../../../.gitbook/assets/S (23).png" alt="" width="563"><figcaption><p>Selecting Folder </p></figcaption></figure>

The file is displayed.

2. Next, click the displayed **file.**

<figure><img src="../../../../.gitbook/assets/S (24).png" alt=""><figcaption><p>Selecting File </p></figcaption></figure>

The file path and file name are displayed.

**D. Configure File Parameters**

<figure><img src="../../../../.gitbook/assets/S (25).png" alt=""><figcaption><p>Preview</p></figcaption></figure>

1. On the **Select File Type Screen**, from the **Encoding** drop-down box, select the **appropriate Encoding Format** (For example, ASCII, UTF-8).&#x20;

{% hint style="info" %}
**Tip:** Selecting a format such as **ASCII** or **UTF-8** defines the file’s **character encoding**, ensuring that text and special characters are interpreted and displayed correctly during processing.
{% endhint %}

2. Enable the **First Row is Column Header, Skip the rows,** and **Limit By** options based on the requirement. Refer to the below tip for the description of these:

{% hint style="info" %}
**Tip:** Description for **First Row is Column Header**, **Skip the rows**, and **Limit By:**

* **First Row is Column Header:** Specifies that the first row of the file contains column names, enabling accurate schema mapping during data ingestion.
* **Skip the Rows:** Allows you to exclude a specified number of initial rows from processing, ensuring that only valid data records are ingested.
* **Limit By:** Restricts the number of records read from the file to support testing, sampling, and performance optimization.
{% endhint %}

3. Select the **required file format** choosing format. For example, CSV.
4. Select the **Delimited Text File** option choosing from **Comma, Tab, Semicolon, Space, or Other.**

{% hint style="info" %}
**Tip:** The purpose of selecting the **Delimited Text File** option is to specify that the file’s data fields are **separated by a delimiter** (such as a comma, tab, or pipe), allowing the system to correctly parse and structure the data into columns.
{% endhint %}

5. Select the **Password Protected** option based on the requirement.
6. Click the **Preview** button.

The required dataset is accessible and ready for transformation. Also, the table schema along with the columns is displayed in the Scheme Properties section.

**E. Define Schema Properties**

1. In the **Scheme Properties** section, select the **required columns**.
2. Enable the **Distinct** option to remove the duplicates.

<figure><img src="../../../../.gitbook/assets/S (26).png" alt=""><figcaption><p>Selecting Columns</p></figcaption></figure>

**F. Preview Data**

* On the **Right Pane**, click **Preview** on the **Input Node**.&#x20;

<figure><img src="../../../../.gitbook/assets/S (27).png" alt=""><figcaption><p>Preview </p></figcaption></figure>

The data is displayed on the Preview tab below. See the below image.

<figure><img src="../../../../.gitbook/assets/S (28).png" alt=""><figcaption><p>Data Display on Preview Tab</p></figcaption></figure>

</details>

<details>

<summary><strong>Save Pipeline</strong></summary>

**Purpose**

After selecting the input node, you need to save the pipeline to persist its configuration and make it available for execution. Saving ensures that all input node settings are retained and correctly applied during pipeline runs.

**Procedure**

As part of the procedure, you need to provide a **name** for the pipeline along with specifying the **summary** of the delta pipeline and the **metadata** including **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (14).png" alt="" width="563"><figcaption></figcaption></figure>

The Pipeline is saved.

</details>

### Configuring Query Input Node

#### Overview

The **SQL Query Input Node** is used when data must be extracted using a **custom SQL statement** rather than selecting entire tables or standard inputs. It allows you to define precise data retrieval logic directly at the source database level.

The SQL Query Input Node provides **greater flexibility, control, and efficiency** in data extraction. It is essential when pipeline requirements demand **custom logic, optimized performance, or complex source-level transformations**.

The below table provides a brief overview of each step involved in the process.

<table><thead><tr><th width="276">Step</th><th>Description</th></tr></thead><tbody><tr><td><a href="copy-of-configuring-input-nodes.md#select-query-input-node">Select Query Input Node </a></td><td>This is the first step in the <strong>Query Input Node</strong> configuration process. As part of this step, you will drag <strong>Query Input</strong> from the <a data-footnote-ref href="#user-content-fn-8"><mark style="color:blue;">Node Palette</mark></a><mark style="color:blue;">,</mark> and then place it on the in the <strong>Main Workspace.</strong></td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#select-database-type">Select Database Type</a></td><td>As part of this step, you will select the <strong>Database Type</strong> choosing between <strong>Data Source</strong> and <strong>Asset</strong> options. Selecting the <strong>Datasource</strong> option connects to an external database whereas the <strong>Assets</strong> option use pre-configured datasets stored within SCIKIQ.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#get-sql-and-preview-data">Get SQL and Preview Data</a></td><td>This step generates the <strong>SQL statement</strong> and allows you to preview the data using <strong>Get Columns</strong>.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#save-pipeline">Save Pipeline</a></td><td><strong>Saving</strong> ensures that all input node settings are retained and correctly applied during pipeline runs.</td></tr></tbody></table>

***

#### Procedure

The expandable panels below provide guided assistance for each step in the configuration process. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Select Query Input Node</strong> </summary>

**Overview:**

The purpose of selecting the **Query Input Node** while creating a delta pipeline is to define the it as the source of data for the pipeline.

**Procedure:**

You can select the **Query Input Node** by dragging it from the **Node Palette** and then and dropping it on the in the **Main Workspace**. Once done, the **Database Type** and **Query Editor** sections are displayed in the Left Pane.&#x20;

The below step-by-step instructions describe how to select Query Input Node:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

<figure><img src="../../../../.gitbook/assets/S (1).png" alt=""><figcaption><p>Input Menu Item</p></figcaption></figure>

The [<mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-9)[^9] is displayed.&#x20;

3. From the **Node Palette**, select the **Query Input,** and drag it onto the **Main Workspace.**

<figure><img src="../../../../.gitbook/assets/S (29).png" alt="" width="457"><figcaption><p>Adding Query Input Node </p></figcaption></figure>

The Database Type and Query Editor sections are displayed in the Left Pane.&#x20;

</details>

<details>

<summary><strong>Select Database Type</strong></summary>

**Purpose:**

The purpose of configuring a **Database Type** (such as **Data Source** or **Asset**) is to define **how the database will be used within the pipeline**.&#x20;

**Procedure:**

As part of configuring, selecting the **Datasource** option connects to an external database whereas the **Assets** option use pre-configured datasets stored within SCIKIQ. Once the database type is selected, the tables pertaining to the selected data source or asset are available in the Schema Properties section on the Left Pane.

The below step-by-step instructions describe how to select database type:

**Step-by-Step Instructions**

A. On the **Left Pane**, from the **Data Type** drop-down box, select either **Datasource** or **Assets.**

&#x20;B. If you wish to choose **Datasource,** then from the **Datasource** drop-down box, select the required **datasource.**

<figure><img src="../../../../.gitbook/assets/S (4).png" alt=""><figcaption><p>Selecting Database Type</p></figcaption></figure>

{% hint style="info" %}
**Tip:**&#x20;

* If required, you can create a new data source connection by clicking the **Create New Connection** ![](<../../../../.gitbook/assets/image (158).png>) button. To learn **how to create a new data source connection**, click [**Creating a New Data Source Connection**](/broken/pages/Ga8WoiowoXOkY4RtBNpS).
{% endhint %}

C. If you want **Asset,** then select the required **asset** from the **Asset** drop-down box..

{% hint style="info" %}
Tip: &#x20;

* If required, you can create new asset by clicking the **Create New Asset** ![](<../../../../.gitbook/assets/image (159).png>)button. To learn **how to create a new asset**, click [**Creating an Asset**](/broken/pages/m9HgqxqwHFgvtRGcp0ij)**.**
{% endhint %}

The tables pertaining to the selected data source or asset are available in the Schema Properties section on the Left Pane.

</details>

<details>

<summary><strong>Get SQL and Preview Data</strong></summary>



**Purpose:**

The Get SQL functionality generates and displays the SQL query derived from the current configuration. This allows you to review and validate the query before execution. It also supports troubleshooting by making the underlying query logic visible.

{% hint style="info" %}
**Tip:** The **Get SQL** functionality generates an SQL query containing all selected columns (fields). Within the generated query, existing fields can be removed but new fields cannot be added. If required, you can write a new query or modify the existing query in the Query Editor.
{% endhint %}

**Procedure:**

The below step-by-step instructions describe how to use the Get SQL functionality:

1. On the **Left Pane**, in the **Query Editor** section, from the **Select** drop-down box, select the required **table**. For example, Aurora\_Order. See the example image below.
2. Next, click the **Get SQL** button.

{% hint style="info" %}
**Tip:** Alternatively, you can write code instead of using the Get SQL functionality in the Query Editor.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (30).png" alt=""><figcaption><p>Using Get SQL </p></figcaption></figure>

The SQL statement is displayed. See the below image.

<figure><img src="../../../../.gitbook/assets/S (31).png" alt=""><figcaption><p> Display of SQL</p></figcaption></figure>

3. Now, scroll down to the bottom of **Query Editor.**
4. In the **Limit** field, specify the **record limit**. For example, 10.
5. Finally, click the **Get Columns** button.

{% hint style="info" %}
**Tip:** In case, you wish to remove the existing query from the Query Editor, then click the **Clear** ![](<../../../../.gitbook/assets/image (167).png>) button.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (32).png" alt=""><figcaption><p>Specifying Record Limit </p></figcaption></figure>

The data is displayed on the Preview tab. See the image below.

<figure><img src="../../../../.gitbook/assets/S (33).png" alt=""><figcaption><p>Data Preview</p></figcaption></figure>

</details>

<details>

<summary><strong>Save Pipeline</strong></summary>

**Purpose:**

After selecting the input node, you need to save the pipeline to persist its configuration and make it available for execution. Saving ensures that all input node settings are retained and correctly applied during pipeline runs.

**Procedure:**

The below step-by-step instructions describe how to save a pipeline:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption><p>Save Button</p></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (14).png" alt="" width="563"><figcaption><p>Saving Pipeline</p></figcaption></figure>

The Pipeline is saved.

</details>

### Configuring API Input Node

#### Overview

The **API Node** is used during pipeline creation when the source or target data is exposed through an API (Application Programming Interface) rather than a file or database. It is typically used when the data needs to be retrieved from external applications or services.

This page describes the procedure for configuring the API Input Node to create a delta pipeline in SCIKIQ. The below table provides a brief overview of each step involved in the process.

> <mark style="color:red;">**Note:**</mark> To configure an API Input Node, an existing API connection must be available in your account.

<table><thead><tr><th width="297">Step</th><th>Description</th></tr></thead><tbody><tr><td><a href="copy-of-configuring-input-nodes.md#select-api-input-node">Select API Input Node </a></td><td>This is the first step in the <strong>API Input Node</strong> configuration process. As part of this step, you will drag <strong>API</strong> from the <a data-footnote-ref href="#user-content-fn-8"><mark style="color:blue;">Node Palette</mark></a><mark style="color:blue;">,</mark> and then place it on the in the <strong>Main Workspace</strong>.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#select-an-existing-api-connection">Select an Existing API Connection </a></td><td>Selecting an <strong>API connection</strong> defines the external service used by the pipeline. The selected connection automatically populates the <strong>Base URL, Endpoint URL,</strong> and <strong>authentication details</strong> on the <strong>Select API screen</strong>.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#preview-data">Preview Data</a></td><td>You can preview the data in both <strong>JSON</strong> and <strong>tabular</strong> formats.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#save-pipeline">Save Pipeline</a></td><td><strong>Saving</strong> ensures that all input node settings are retained and correctly applied during pipeline runs.</td></tr></tbody></table>

#### Procedure

The expandable panels below provide guided assistance for each step in the configuration process. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Select API Input Node</strong> </summary>

**Overview:**

The purpose of selecting the **API Input Node** before creating a delta pipeline is to define it as the data source and establish how incremental data will be retrieved.

**Procedure:**

As part of selecting the **API Input Node**, you need to drag it from the **Node Palette** and then place it on the in the **Main Workspace**. Once placed, the **Select API** and **Select Data Frame** sections are displayed in the left pane.&#x20;

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

<figure><img src="../../../../.gitbook/assets/S (1).png" alt=""><figcaption><p>Input Menu Item</p></figcaption></figure>

The [<mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-5)[^5] is displayed.&#x20;

3. From the **Node Palette**, select the **API Input,** and drag it onto the **Main Workspace.**

<figure><img src="../../../../.gitbook/assets/S (34).png" alt="" width="507"><figcaption><p>Placing API Node on Right Pane</p></figcaption></figure>

The Select API and Select Data Frame sections are displayed in the left pane Left Pane.&#x20;

</details>

<details>

<summary><strong>Select an Existing API Connection</strong> </summary>

**Purpose:**

**Selecting an API** defines the external service or endpoint from which the pipeline retrieves or sends data. In the SCIKIQ application, selecting an API connection automatically populates the [<mark style="color:blue;">**Base URL**</mark>](#user-content-fn-10)[^10], [<mark style="color:blue;">**Endpoint URL**</mark>](#user-content-fn-11)[^11], [<mark style="color:blue;">**Authentication Key**</mark>](#user-content-fn-12)[^12], and [<mark style="color:blue;">**Token**</mark>](#user-content-fn-13)[^13] on the **Select API** screen. The application also provides data preview capabilities in both JSON and tabular formats.

**Procedure:**

The below step-by-step instructions describe the procedure:

* On the **Left Pane**, from the **Select API** drop-down box, select the required **API**. For example, test\_ytd\_Idm. See the example image below.

<figure><img src="../../../../.gitbook/assets/S (35).png" alt="" width="506"><figcaption><p>Selecting API Connection</p></figcaption></figure>

The BASE URL, END POINT, Authentication Key and Value are displayed in the Select API section. See the image below.

<figure><img src="../../../../.gitbook/assets/S (36).png" alt="" width="563"><figcaption><p>BASE URL, END POINT, Authentication Key and Value</p></figcaption></figure>

</details>

<details>

<summary><strong>Preview Data</strong></summary>

**Overview:**

You can preview the data in both **JSON** and **tabular** formats. Enabling the [<mark style="color:blue;">DF</mark>](#user-content-fn-14)[^14] option treats the incoming data as rows and columns and displays it in a tabular view.&#x20;

**Procedure:**

The below step-by-step instructions describe the procedure:

**1.Preview Data in JSON Format**

A. In the **Select Data Frame** section, don't enable the **DF Enable** option.

<figure><img src="../../../../.gitbook/assets/S (37).png" alt=""><figcaption><p>DF Enable Option</p></figcaption></figure>

B. On the **Right Pane**, click the **Preview** icon on the top of **Input API Node.**

<figure><img src="../../../../.gitbook/assets/S (38).png" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

The data is displayed on the JSON Preview tab. See the example image below:

<figure><img src="../../../../.gitbook/assets/S (39).png" alt=""><figcaption><p>JSON Preview</p></figcaption></figure>

**2.Preview Data in Tabular Format**

A. On the **Left Pane**, in the **Select Data Frame** section, select the **DF Enable** option.&#x20;

B. From the **Select Data Frame** drop-down box, select the **DF\_API** option.

<figure><img src="../../../../.gitbook/assets/S (40).png" alt="" width="466"><figcaption><p>Selecting DF Enable Option</p></figcaption></figure>

C. On the **Right Pane**, click the **Preview** icon on the top of **Input API Node**,&#x20;

<figure><img src="../../../../.gitbook/assets/S (41).png" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

&#x20;The data is displayed in tabular format. See the image below.

<figure><img src="../../../../.gitbook/assets/S (42).png" alt="" width="563"><figcaption><p>Preview in Tabular Format</p></figcaption></figure>

</details>

<details>

<summary><strong>Save Pipeline</strong></summary>

**Purpose**

After selecting the input node, you need to save the pipeline to persist its configuration and make it available for execution. Saving ensures that all input node settings are retained and correctly applied during pipeline runs.

**Procedure**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (14).png" alt="" width="563"><figcaption></figcaption></figure>

The Pipeline is saved.

</details>

### Configuring SAP APP Node

#### Overview

You configure the **SAP App Node** while creating a delta pipeline **when the source is an SAP application** and data needs to be extracted from SAP. It is typically used when data must be retrieved from **SAP systems such as SAP ECC, SAP S/4HANA, or SAP BW4.**

This page describes the procedure for configuring a SAP APP Node to create a delta pipeline in SCIKIQ. The below table provides a brief overview of each step involved in the process.

<table><thead><tr><th width="265">Step</th><th>Description</th></tr></thead><tbody><tr><td><a href="copy-of-configuring-input-nodes.md#select-sap-app-input-node">Select SAP APP Input Node</a> </td><td>This is the first step in the <strong>GRAPHQL Input Node</strong> configuration process. As part of this step, you will drag <strong>SAP App Node</strong> from the <a data-footnote-ref href="#user-content-fn-8"><mark style="color:blue;">Node Palette</mark></a><mark style="color:blue;">,</mark> and then place it on the in the <strong>Main Workspace</strong>.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#select-an-api-connection-and-source-type">Select an API Connection and Source Type</a> </td><td>As part of this step, you will select an existing <strong>API connection</strong>.  Once selected, the tables  associated with that connection are are displayed.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#select-columns">Select Columns</a></td><td>During this step, you will select <strong>only the required columns.</strong> This reduces data volume, improves performance, and ensures that only relevant business data is processed in downstream transformations.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#apply-filters">Apply Filters</a></td><td>Applying <strong>Filters</strong> allow you retrieve only <strong>relevant data</strong> based on defined criteria and exclude <strong>unnecessary or unwanted records.</strong></td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#apply-limit">Apply Limit</a></td><td>Applying the <strong>Limit</strong> operator enable you to define an <strong>upper limit</strong> on the number of records retrieved. </td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#preview-data">Preview Data</a></td><td><strong>Preview</strong> allows you to verify that the <strong>SAP APP Input Node</strong> is correctly configured and is extracting the expected data from the selected table before the pipeline is executed.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#save-pipeline">Save Pipeline</a></td><td><strong>Saving</strong> ensures that all input node settings are retained and correctly applied during pipeline runs.</td></tr></tbody></table>

#### Procedure

The expandable panels below provide guided assistance for each step in the configuration process. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Select SAP APP Input Node</strong> </summary>

P**urpose:**

The purpose of selecting the **SAP APP  Node** while creating a delta pipeline is to define it as the data source for the pipeline.

**Procedure:**

As part of configuring the **SAP Input Node**, you need to first drag it from the **Node Palette** and then place it on the in the Main Workspace. Once placed, the **Select Connection** and **SAP App Server** sections are displayed in the left pane.&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

<figure><img src="../../../../.gitbook/assets/S.png" alt="" width="467"><figcaption><p>Create Delta Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

<figure><img src="../../../../.gitbook/assets/S (1).png" alt="" width="460"><figcaption><p>Input Menu Item</p></figcaption></figure>

The [<mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-5)[^5] is displayed. See the image below.

<figure><img src="../../../../.gitbook/assets/S (2).png" alt="" width="464"><figcaption><p>Node Palette</p></figcaption></figure>

3. From the **Node Palette**, select the **SAP APP Input,** and drag it onto the **Main Workspace**.

<figure><img src="../../../../.gitbook/assets/S (43).png" alt="" width="511"><figcaption><p>Selecting SAP APP Input Node</p></figcaption></figure>

The Select Connection and SAP APP Server sections are displayed on the left pane.

</details>

<details>

<summary><strong>Select an API Connection and Source Type</strong></summary>

**Purpose:**

Selecting an **SAP APP connection** defines **which SAP system the SAP node will connect to** during pipeline execution.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

A. On the **Left Pane**, from the **Select Connection** drop-down box, select the required connection choosing from **BW4 Hana Connection, S4 Hana, SAP ECC App Server,** or **SAP ECC Connection.** For example, S4 Hana.&#x20;

> <mark style="color:red;">**Note:**</mark> The source types are different for each of these SAP Connections. See the below table.&#x20;

<table><thead><tr><th width="124.54534912109375" valign="top">Coonection</th><th width="161.3636474609375" valign="top">Source</th><th width="387.1817626953125" valign="top">Description</th></tr></thead><tbody><tr><td valign="top">S4 Hana</td><td valign="top">Table</td><td valign="top"><p>A <strong>Table</strong> in SAP is a physical database object that stores transactional or master data in rows and columns. You can use Tables when you need detailed transactional or master data</p><p><strong>Search field examples:</strong> </p><p>MARA (Material master),MAKT (Material descriptions)</p></td></tr><tr><td valign="top"></td><td valign="top"><a data-footnote-ref href="#user-content-fn-15"><mark style="color:blue;"><strong>CDS</strong></mark></a></td><td valign="top"><p>A <strong>CDS View i</strong>s a logical, semantically rich data model built on top of one or more SAP tables. You can use CDS Views when you need pre-joined, business-contextual, and analytics-ready data.</p><p><strong>Search field examples:</strong></p><p>I_Material (Material master interface view), I_Customer (Customer master interface view)</p></td></tr><tr><td valign="top">SAP ECC App Server</td><td valign="top">The source types (Table and CDS) are same  that of  S4 Hana </td><td valign="top"></td></tr><tr><td valign="top">SAP ECC Connection</td><td valign="top">The source types (Table and CDS) are same  that of  S4 Hana </td><td valign="top"></td></tr><tr><td valign="top">BW4 Hana Connection</td><td valign="top">Table</td><td valign="top">Refer to the above <strong>Table</strong> description.</td></tr><tr><td valign="top"></td><td valign="top">CDS</td><td valign="top">Refer to the above <strong>CDS</strong> description.</td></tr><tr><td valign="top"></td><td valign="top">InfoObjects</td><td valign="top"><p>An <strong>InfoObject</strong> is the fundamental data element in BW/4HANA used to describe business characteristics or key figures.</p><p><strong>Search field examples:</strong></p><p>0CUSTOMER - Customer</p><p>0MATERIAL - Material</p></td></tr><tr><td valign="top"></td><td valign="top">InfoCubes</td><td valign="top"><p>An <strong>InfoCube</strong> is a multidimensional data model designed primarily for analytical reporting. It organizes data into fact data (key figures) and dimensions (characteristics).</p><p><strong>Search field examples:</strong></p><p>ZSD_SALES_IC <strong>-</strong> Sales InfoCube</p><p>ZFI_GL_IC - Finance General Ledger Cube</p></td></tr><tr><td valign="top"></td><td valign="top">DSO</td><td valign="top"><p>A <strong>DSO</strong> (DataStore Object) is a table-based data object used to store detailed, granular transactional data. It supports overwrite and delta updates, making it suitable for operational reporting and staging.</p><p><strong>Search field examples:</strong></p><p>ZSD_SALES_DSO - Sales transactional DSO</p><p>ZFI_AP_DSO - Accounts Payable DSO</p></td></tr><tr><td valign="top"></td><td valign="top">ADSO</td><td valign="top"><p>An <strong>ADSO</strong> (Advanced DataStore Object) is the <strong>central and most flexible data object in BW/4HANA</strong>, replacing classic InfoCubes and DSOs. It supports <strong>staging, harmonization, and reporting</strong> in a single object.</p><p><strong>Search field examples:</strong></p><p>ZSD_SALES_ADSO <strong>-</strong> ZSD_SALES_ADSO</p><p>Sales ADSO - Finance General Ledger ADSO</p></td></tr></tbody></table>

2. From the **Source Type** drop-down box, select the required **source type.** For example, Table.
3. In the **Search** field, enter the **search input**. For example, TCURR.
4. Click the **Search** button.

<figure><img src="../../../../.gitbook/assets/S (44).png" alt="" width="510"><figcaption><p>Selecting SAP APP Connection</p></figcaption></figure>

The available tables are displayed in Select Table drop-down box of SAP APP Server section.

</details>

<details>

<summary><strong>Select Columns</strong></summary>

**Purpose:**

The purpose of selecting table columns while configuring an SAP App Input Node is to **control which fields are extracted from the SAP source**. By selecting only the required columns, the pipeline reduces data volume, improves performance, and ensures that only relevant business data is processed in downstream transformations.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

1. In the **SAP APP Server** section, from the **Table** drop-down box, select the **required table**. For example, TCURR.

The list of columns pertaining to the selected table are displayed.&#x20;

2. From the **list of columns**, select the **required columns**.

<figure><img src="../../../../.gitbook/assets/S (45).png" alt="" width="503"><figcaption><p>Selecting Columns</p></figcaption></figure>

{% hint style="info" %}
**Tip:** You can select a **single column, multiple columns,** or **all columns** based on your requirement. Selecting the **Select All** checkbox allows you to select all tables at once. See the **ticked checkbox** in the image below.

![](<../../../../.gitbook/assets/image (168).png>)
{% endhint %}

</details>

<details>

<summary><strong>Apply Filters</strong></summary>

**Overview:**

The purpose of **filters** is to control which records are included in data processing by applying specific conditions to the dataset. In practical terms, filters allow retrieve only **relevant data** based on defined criteria and exclude **unnecessary or unwanted records.**

**Procedure:**

As part of the using the filters, you need to define the **logical relationship between multiple conditions** by selecting either **AND** or **OR** and then define the **precise data filtering criteria.** Based on the requirement, you can use parameters and variables as well.&#x20;

The below step-by-step instructions describe the procedure of using the filters:&#x20;

**Step-by-Step instructions:**

1. In the **SAP App Server** section, Click the **Filters** icon, and then click the **Add/Edit Filter** button.

{% hint style="info" %}
**Tip:** To view the **SAP App Server** section in an expanded view, click the **Toggle Full Screen** icon. See the highlighted part in red the below image.

![](<../../../../.gitbook/assets/image (169).png>)
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (46).png" alt="" width="509"><figcaption><p>Applying Filters</p></figcaption></figure>

The **Add/Edit Filter** dialogue box is displayed.

2\. On the **Add/Edit Filter** dialogue box (See the image below):

<figure><img src="../../../../.gitbook/assets/S (47).png" alt="" width="563"><figcaption><p>Applying Filters</p></figcaption></figure>

A. **Select** **Add or Edit**&#x20;

{% hint style="info" %}
**Tip:** The purpose of using AND or OR is to define the logical relationship between multiple conditions.
{% endhint %}

* Select **AND** if you want all conditions to be true for a record to be selected.&#x20;
* Select **OR** if you want any one of the conditions can be true for a record to be selected.

B. **Define Filter Condition**&#x20;

{% hint style="info" %}
**Tip:** Filtering condition allows to define **precise data filtering criteria** (For example, Date less than 2024-01-01.
{% endhint %}

* From the **Columns** drop-down box, select the **Column** to which the filter should be applied.
* From the **Operator** drop-down box, select the **required operator**.&#x20;
* In the **Value** field, enter the required **value.**

C. **To add a new condition line** (For example, Revenue ID less than 10101)&#x20;

* Click the **Add Filter** ![](<../../../../.gitbook/assets/image (164).png>) button.&#x20;

D. **To add a nested filter logic** (For example, Revenue ID less than 10101 and Value less than 10000)

* Click the **Add Filter Group** ![](<../../../../.gitbook/assets/image (165).png>)  button.&#x20;

E. **To use dynamic parameters in filters**

* Prefix the parameter with `@@` in the ETL design.

{% hint style="info" %}
**Tip:** The purpose of using Parameters is to enable **dynamic filtering** at runtime and allows values to be passed externally.
{% endhint %}

F. **To use ETL variables in filters**

* Prefix the variable with `##`

{% hint style="info" %}
**Tip:** Using variables supports reusable and internally computed values that are **generated within the system and can be used multiple times across the pipeline** without being hard-coded.
{% endhint %}

4. Finally, click the **Save** button.

</details>

<details>

<summary><strong>Apply Limit</strong> </summary>

**Overview:**

You can use the **Limit** feature to define an **upper limit** on the number of records retrieved. This functionality is commonly used to optimize performance, support testing activities, and manage data processing volume before transformations are applied.

**Procedure:**

As part of the procedure, you need to select either the system-defined upper limit or the custom option. Once selected, the upper limit for record retrieval is established.

The information below outlines the step-by-step instructions for completing this task:&#x20;

**Step-by-Step instructions:**

1. In the **Schema Properties** section, select the **Limit By** icon, and then define the limit choosing from **Limit By 10, Limit By 500, Limit By 1000, Limit By 2000,** or **Custom**.&#x20;

<figure><img src="../../../../.gitbook/assets/S (48).png" alt="" width="504"><figcaption><p>Applying Limit By</p></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> If you wish to define a **custom** limit, then select the **Custom** option, and specify the custom limit. A **custom limit** is a **user-defined restriction on the number of records retrieved from a dataset**, rather than using a system-defined default limit.

2. Click the **Preview** tab to check the defined number of records.

</details>

<details>

<summary><strong>Preview Data</strong></summary>

**Overview:**

Previewing allows you to verify that the SAP APP Input Node is correctly configured and is extracting the expected data from the selected table before the pipeline is executed.

**Procedure:**

The below step-by-step instructions describe the procedure:

* On the **Right Pane**, click the **Preview** icon on the top of **SAP APP Input Node.**

<figure><img src="../../../../.gitbook/assets/S (49).png" alt="" width="509"><figcaption><p>Previewing Data</p></figcaption></figure>

The data is displayed on the Preview tab. See the image below:

<figure><img src="../../../../.gitbook/assets/S (50).png" alt=""><figcaption><p>Data Preview</p></figcaption></figure>

</details>

<details>

<summary><strong>Save Pipeline</strong></summary>

**Overview**

After selecting the input node, you need to save the pipeline to persist its configuration and make it available for execution. Saving ensures that all input node settings are retained and correctly applied during pipeline runs.

**Procedure**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (14).png" alt="" width="563"><figcaption></figcaption></figure>

The Pipeline is saved.

</details>

### Configuring No SQL Node

#### Overview

You can configure a **NoSQL Input Node** while creating a **delta pipeline** **when the source system is a NoSQL database and the pipeline needs to capture incremental (changed) data.**

The configuration can be completed by following a sequence of guided steps. Once the configuration is complete, the connection is listed on the **Delta Pipelines** page.&#x20;

The below table provides a brief overview of each step involved in the process.

<table><thead><tr><th width="224">Step</th><th>Description</th></tr></thead><tbody><tr><td><a href="copy-of-configuring-input-nodes.md#select-nosql-input-node">Select NoSQL Input Node</a></td><td>This is the first step in the NOSQL Input Node configuration process. As part of this, you will drag the NOSQL Input Node from the <a data-footnote-ref href="#user-content-fn-2"><mark style="color:blue;"><strong>Node Palette</strong></mark></a> and then place it on the in the Main Workspace.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#select-database-type-and-connection">Select Database Type and Connection</a></td><td>As part of this step, you will select either <a data-footnote-ref href="#user-content-fn-3"><mark style="color:blue;"><strong>Datasource</strong></mark></a> or <a data-footnote-ref href="#user-content-fn-4"><mark style="color:blue;"><strong>Asset</strong></mark></a> to define how the database will be used within the pipeline. </td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#select-table-and-columns">Select Table and Columns</a></td><td>As part of this step, you will select the required columns to define which fields are extracted from the selected database type. </td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#apply-filters">Apply Filters</a></td><td>Applying <strong>Filters</strong> allow you retrieve only <strong>relevant data</strong> based on defined criteria and exclude <strong>unnecessary or unwanted records.</strong></td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#apply-limit-operation">Apply Limit Operation</a></td><td>Applying the <strong>Limit</strong> operation enable you to define an <strong>upper limit</strong> on the number of records retrieved. </td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#apply-order-operation">Apply Order Operation</a></td><td>Applying the <strong>Order</strong> operation enables to define the <strong>sort order</strong> of records based on one or more selected columns, in either <strong>ascending</strong> or <strong>descending order</strong>.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#apply-group-operation">Apply Group Operation</a></td><td>Applying the <strong>Group</strong> operation enables to aggregate data based on selected columns, facilitating the summarization of large datasets for enhanced analytical insights.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#preview-data">Preview Data</a></td><td><strong>Preview</strong> allows you to verify that the NoSQL Input Node is correctly configured and is extracting the expected data from the selected table before the pipeline is executed.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#save-pipeline">Save Pipeline</a></td><td>Saving ensures that all input node settings are retained and correctly applied during pipeline runs.</td></tr></tbody></table>

***

#### Procedure

The expandable panels below provide guided assistance for each step in the configuration process. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Select NoSQL input Node</strong></summary>

**Purpose:**

Selecting a NoSQL Input Node defines the NoSQL database as the source and enables incremental data extraction for the delta pipeline.&#x20;

**Procedure:**

As part of the procedure to configure the **No SQL Input Node**, you need to first drag it from the **Node Palette** and then place it on the in the **Main Workspace**. Once placed, the **Database Type** and **NoSQL Properties** sections are displayed on the Left Pane.&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

<figure><img src="../../../../.gitbook/assets/S.png" alt="" width="467"><figcaption><p>Create Delta Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

<figure><img src="../../../../.gitbook/assets/S (1).png" alt="" width="460"><figcaption><p>Input Menu </p></figcaption></figure>

The [<mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-5)[^5] is displayed. See the image below.

<figure><img src="../../../../.gitbook/assets/S (2).png" alt="" width="464"><figcaption><p>Node Palette</p></figcaption></figure>

3. From the **Node Palette**, select **No SQL,** and then drag it onto the **Main Workspace**.

<figure><img src="../../../../.gitbook/assets/S (51).png" alt="" width="511"><figcaption><p>Selecting No SQL Node</p></figcaption></figure>

The **Database Type** and **NoSQL Properties** sections are displayed on the Left Pane.

</details>

<details>

<summary><strong>Select Database Type and Connection</strong></summary>

**Purpose:**

The purpose of configuring a **Database Type** (**Data Source** or **Asset**) is to define **how the database will be used within the pipeline**.&#x20;

**Procedure:**

As part of the procedure, you need to select either **Data Source** or **Asset** based on your requirement.  Selecting the **Datasource** option connects to an external database whereas the **Assets** option use pre-configured datasets stored within SCIKIQ. Once the database type is selected, the tables pertaining to the selected data source or asset are available in the Schema Properties section on the Left Pane.

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

A. On the **Left Pane**, from the **Data Type** drop-down box, select either **Datasource** or **Assets.**

B. If you wish to choose **Datasource,** then from the **Datasource** drop-down box, select the required **datasource connection.**

<figure><img src="../../../../.gitbook/assets/S (52).png" alt="" width="509"><figcaption><p>Selecting Datasource Connection</p></figcaption></figure>

{% hint style="info" %}
**Tip:**&#x20;

* If required, you can create a new data source connection by clicking the **Create New Connection** ![](<../../../../.gitbook/assets/image (158).png>) button. To learn **how to create a new data source connection**, click [**Creating a New Data Source Connection**](/broken/pages/Ga8WoiowoXOkY4RtBNpS).
{% endhint %}

C. If you want **Asset,** then select the required **asset** from the **Asset** drop-down box.

{% hint style="info" %}
**Tip:** &#x20;

* If required, you can create new asset by clicking the **Create New Asset** ![](<../../../../.gitbook/assets/image (159).png>)button. To learn **how to create a new asset**, click [**Creating an Asset**](/broken/pages/m9HgqxqwHFgvtRGcp0ij)**.**
{% endhint %}

The tables pertaining to the selected data source or assets are populated in the **NoSQL Properties** section on the Left Pane.

</details>

<details>

<summary><strong>Select Table and Columns</strong></summary>

**Purpose:**

During the configuration of a NoSQL Input Node, **column selection** is used to **specify the fields to be extracted**.&#x20;

**Procedure:**

As part of the procedure, the table is selected first, after which the available columns are displayed. From this list, the required columns can be selected. Duplicate records can be removed using the **Distinct** option, and **Data Quality (DQ)** rules can be applied as required.

The information below outlines the step-by-step instructions for completing this task:

{% hint style="info" %}
**Tip:** For a larger view of the **NoSQL Properties** section, click the **Toggle Fullscreen** ![](<../../../../.gitbook/assets/image (170).png>) icon. &#x20;
{% endhint %}

1.In the **NoSQL Properties** section (Refer to the **Selecting Columns** image below), from the **Table** drop-down box, select the **required table**.&#x20;

The list of columns pertaining to the selected table are displayed.&#x20;

2.From the **list of columns**, select the **required columns**.

{% hint style="info" %}
**Tip:** You can select a **single column, multiple columns,** or **all columns** based on your requirement. Selecting the **Select All** checkbox allows you to select all tables at once. See the **ticked checkbox** in the image below.

![](<../../../../.gitbook/assets/image (171).png>)


{% endhint %}

3.If you want to **add a new column**, click the **New Column** ![](<../../../../.gitbook/assets/image (161).png>)button.

The column is added.&#x20;

{% hint style="info" %}
**Tip:** You can add multiple columns based on your requirement.
{% endhint %}

4.Click the **Distinct** ![](<../../../../.gitbook/assets/image (162).png>)button to remove the duplicates.

5.If you want apply **DQ Rules**, click the **DQ Rules** ![](<../../../../.gitbook/assets/image (163).png>)button.&#x20;

{% hint style="info" %}
**Tip:** Click **here** to know how to apply DQ Rules.
{% endhint %}

6.Click the **Save** button.&#x20;

<figure><img src="../../../../.gitbook/assets/S (53).png" alt=""><figcaption><p>Selecting Columns</p></figcaption></figure>

</details>

<details>

<summary><strong>Apply Filters</strong></summary>

**Purpose:**

The purpose of **Filters** is to control which records are included in data processing by applying specific conditions to the dataset. In practical terms, filters allow retrieve only **relevant data** based on defined criteria and exclude **unnecessary or unwanted records.**

**Procedure:**

As part of the using the filters, you need to define the **logical relationship between multiple conditions** by selecting either **AND** or **OR** and then define the **precise data filtering criteria.** Based on the requirement, you can use parameters and variables as well.&#x20;

The below step-by-step instructions describe the procedure of using the filters:&#x20;

**Step-by-Step instructions:**

1. In the **NoSQL Properties** section, click the **Filters** icon, and then click the **Add/Edit Filter** button.

<figure><img src="../../../../.gitbook/assets/S (54).png" alt=""><figcaption><p>Filter Icon</p></figcaption></figure>

The **Add/Edit Filter** dialogue box is displayed.

2\. On the **Add/Edit Filter** dialogue box (See the image below):

<figure><img src="../../../../.gitbook/assets/S (47).png" alt="" width="563"><figcaption><p>Applying Filters</p></figcaption></figure>

A. **Select** **Add or Edit**&#x20;

{% hint style="info" %}
**Tip:** The purpose of using AND or OR is to define the logical relationship between multiple conditions.
{% endhint %}

* Select **AND** if you want all conditions to be true for a record to be selected.&#x20;
* Select **OR** if you want any one of the conditions can be true for a record to be selected.

B. **Define Filter Condition**&#x20;

{% hint style="info" %}
**Tip:** Filtering condition allows to define **precise data filtering criteria** (For example, Date less than 2024-01-01.
{% endhint %}

* From the **Columns** drop-down box, select the **Column** to which the filter should be applied.
* From the **Operator** drop-down box, select the **required operator**.&#x20;
* In the **Value** field, enter the required **value.**

C. **To add a new condition line** (For example, Revenue ID less than 10101)&#x20;

* Click the **Add Filter** ![](<../../../../.gitbook/assets/image (164).png>) button.&#x20;

D. **To add a nested filter logic** (For example, Revenue ID less than 10101 and Value less than 10000)

* Click the **Add Filter Group** ![](<../../../../.gitbook/assets/image (165).png>)  button.&#x20;

E. **To use dynamic parameters in filters**

* Prefix the parameter with `@@` in the ETL design.

{% hint style="info" %}
**Tip:** The purpose of using Parameters is to enable **dynamic filtering** at runtime and allows values to be passed externally.
{% endhint %}

F. **To use ETL variables in filters**

* Prefix the variable with `##`

{% hint style="info" %}
**Tip:** Using variables supports reusable and internally computed values that are **generated within the system and can be used multiple times across the pipeline** without being hard-coded.
{% endhint %}

4. Finally, click the **Save** button.

</details>

<details>

<summary><strong>Apply Limit Operator</strong></summary>

**Purpose:**

You can use the **Limit** feature to define an **upper limit** on the number of records retrieved. This functionality is commonly used to optimize performance, support testing activities, and manage data processing volume before transformations are applied.

**Procedure:**

As part of the procedure, you need to **select either the system-defined upper limit or the custom optio**n. Once selected, the upper limit for record retrieval is established.

The information below outlines the step-by-step instructions for completing this task:&#x20;

**Step-by-Step instructions:**

1. In the **Schema Properties** section, click the **Limit** icon, and then define the limit choosing from **Limit By 10, Limit By 500, Limit By 1000, Limit By 2000,** or **Custom**.&#x20;

<figure><img src="../../../../.gitbook/assets/S (55).png" alt=""><figcaption><p>Applying Limit Operation</p></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> If you wish to define a **custom** limit, then select the **Custom** option, and specify the limit. A **custom limit** is a **user-defined restriction on the number of records retrieved from a dataset**, rather than using a system-defined default limit.

2. Click the **Preview** tab to check the defined number of records.

</details>

<details>

<summary><strong>Apply Order Operator</strong></summary>

**Purpose:**

The **Order** operation enables to define the **sort order** of records based on one or more selected columns, in either **ascending** or **descending order**. This functionality supports structured data preparation prior to transformation, ensuring that datasets follow a consistent and meaningful sequence for downstream analysis and processing.

**Procedure:**

As part of the procedure, you need to select the **Order** icon and specify the record order by choosing either [<mark style="color:blue;">**ASC**</mark>](#user-content-fn-6)[^6] option or [<mark style="color:blue;">**DESC**</mark>](#user-content-fn-7)[^7] **option.** Once done, the records are sorted according to the specified order.

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. In the **NOSQL Properties** section, click the **Order** icon, and then from the **Column Name** drop-down box, select the **required value**. For example, SRC.
2. From the **Order By** drop-down box, select [<mark style="color:blue;">**ASC**</mark>](#user-content-fn-6)[^6] or [<mark style="color:blue;">**DESC**</mark>](#user-content-fn-7)[^7] based on your requiremen&#x74;**.**

{% hint style="info" %}
**Tip:** ASC refers to ascending order, while DESC refers to descending order.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (56).png" alt="" width="563"><figcaption><p>Applying Order By Operation</p></figcaption></figure>

3. Click the **Preview** tab to view the data.

</details>

<details>

<summary><strong>Apply Group Operator</strong></summary>

**Purpose:**

The **Group** operation enables to aggregate data based on selected columns, facilitating the summarization of large datasets for enhanced analytical insights. It supports standard aggregation operations such as SUM, COUNT, AVG, MAX, and MIN on grouped records.&#x20;

This functionality ensures logical data structuring, reduces redundancy, and improves the efficiency of reporting and downstream data processing.&#x20;

**Procedure:**

As part of the procedure, you need to select the **Group** and then select the required columns. The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. In the **NoSQL Properties** section, click the **Group** icon, and then select the **required columns**.&#x20;

<figure><img src="../../../../.gitbook/assets/S (57).png" alt=""><figcaption><p>Applying Group Operation</p></figcaption></figure>

2. Click the **Preview** tab to view the data.

</details>

<details>

<summary><strong>Preview Data</strong></summary>

**Purpose:**

Previewing allows you to verify that the NoSQL Input Node is correctly configured and is extracting the expected data from the selected table before the pipeline is executed.

**Procedure:**

The below step-by-step instructions describe the procedure:

* On the **Right Pane**, click the **Preview** icon on the top of **NoSQL Input Node.**

<figure><img src="../../../../.gitbook/assets/S (58).png" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

The data is displayed on the Preview tab.&#x20;

</details>

<details>

<summary><strong>Save Pipeline</strong></summary>

**Purpose**

After selecting the input node, you need to save the pipeline to persist its configuration and make it available for execution. Saving ensures that all input node settings are retained and correctly applied during pipeline runs.

**Procedure**

As part of the procedure, you need to provide a **name** for the pipeline along with specifying the **summary** of the delta pipeline and the **metadata** including **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (14).png" alt="" width="563"><figcaption></figcaption></figure>

The Pipeline is saved.

</details>

### Configuring UCM File Loader

#### Overview

You can configure a **UCM File Loader Input Node** while creating a **delta pipeline** when **source data is stored as files in UCM repository** such as CSV, JSON, XML, or other structured or semi-structured file formats. The configuration can be completed by following a sequence of guided steps. Once the configuration is complete, the connection is listed on the **Delta Pipelines** page.&#x20;

The below table provides a brief overview of each step involved in the process.

<table><thead><tr><th width="224">Step</th><th>Description</th></tr></thead><tbody><tr><td><a href="copy-of-configuring-input-nodes.md#select-ucm-file-loader-input-node">Select UCM File Loader input Node</a></td><td>This is the first step in the <strong>UCM File Loader Input Node</strong> configuration process. As part of this, you will drag the UCB File Loader Input Node from the <a data-footnote-ref href="#user-content-fn-8"><mark style="color:blue;">Node Palette</mark></a> and then place it on the in the Main Workspace.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#define-ucm-file-loader-settings">Define UCM File Loader Settings</a></td><td>As part of this step, you will define <a data-footnote-ref href="#user-content-fn-16"><mark style="color:blue;">UCM File Loader Connection</mark></a>, <a data-footnote-ref href="#user-content-fn-17"><mark style="color:blue;">File Storage Connection</mark></a>, <a data-footnote-ref href="#user-content-fn-18"><mark style="color:blue;">File Storage Folder/Bucket</mark></a>, and <a data-footnote-ref href="#user-content-fn-19"><mark style="color:blue;">UCM Process</mark></a> to define how the database will be used within the pipeline. </td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#select-process-tables">Select Process Tables</a> </td><td>As part of this step, you will select the required <a data-footnote-ref href="#user-content-fn-20"><mark style="color:blue;">Process Table</mark></a> to define which fields are extracted from the selected file format. </td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#preview-configuration">Preview Configuration</a></td><td><strong>Preview</strong> confirms that the UCM connection, storage location, and other settings are correctly configured and the correct files from the specified folder or bucket are being picked up.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#save-pipeline">Save Pipeline</a></td><td><strong>Saving</strong> ensures that all input node settings are retained and correctly applied during pipeline runs.</td></tr></tbody></table>

***

#### Procedure

The expandable panels below provide guided assistance for each step in the configuration process. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Select UCM File Loader input Node</strong></summary>

**Purpose:**

Selecting a **UCM File Loader Input Node** defines the UCM repository as the source and enables incremental ingestion of file-based data for the delta pipeline.

**Procedure:**

As part of the procedure to configure the **UCM File Loader Input Node**, you need to first drag it from the **Node Palette** and then place it on the in the **Main Workspace**. Once placed, the **Oracle UCM File Loader** and **Select Process Table** sections are displayed on the Left Pane.&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

<figure><img src="../../../../.gitbook/assets/S.png" alt="" width="467"><figcaption><p>Create Delta Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

<figure><img src="../../../../.gitbook/assets/S (1).png" alt="" width="460"><figcaption><p>Input Menu </p></figcaption></figure>

The [<mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-5)[^5] is displayed. See the image below.

3. From the **Node Palette**, select **UCM File Loader,** and then drag it onto the **Main Workspace**.

<figure><img src="../../../../.gitbook/assets/S (59).png" alt="" width="511"><figcaption><p>Selecting UCM File Loader Node</p></figcaption></figure>

The **Oracle UCM File Loader** and **Select Process Table** sections are displayed on the Left Pane.

</details>

<details>

<summary><strong>Define UCM File Loader Settings</strong></summary>

**Purpose:**

The purpose of defining **UCM File Loader Settings** is to **define where the files come from, how they are accessed, and how they are processed**.&#x20;

**Procedure:**

As part of defining the **UCM File Loader Settings**, you need to define:

* **UCM File Loader Connection**, which identifies the UCM environment and establishes a secure connection to access UCM-managed content.
* **File Storage Connection**, which specifies the underlying storage service where the UCM files physically reside.
* **File Storage Folder/Bucket**, which defines the exact directory or bucket from which files should be read, limiting ingestion to the relevant file location.
* **UCM Process**, which determines the processing logic applied to the files, such as parsing rules, metadata handling, and ingestion behavior.

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

A. On the **Left Pane**, from the **Select Connection** drop-down box, select the **UCM** **file loader connection.** For example, Oracle OCM.

B. From the **Select File Storage Connection** drop-down box, select the **file storage connection**. For example, File Store S3 (S3)

The files related to the selected storage connection are populated in the Select File Storage Folder/Bucket drop-down box.

C. From the **Select File Storage Folder/Bucket** drop-down box, select the required **storage folder/bucket**.

D. From the **UCM Process** drop-down box, select the required **UCM process**.

<figure><img src="../../../../.gitbook/assets/S (60).png" alt=""><figcaption><p>Defining UCM File Loader Settings</p></figcaption></figure>

The related tables are displayed in the **Select Process Tables** section.

</details>

<details>

<summary><strong>Select Process Tables</strong></summary>

**Purpose:**

The purpose of **selecting Process Tables while configuring a UCM File Loader Input Node** is to **define how the ingested UCM files are structured and interpreted as tabular data** for pipeline processing.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

* &#x20;From the **Select Process Tables** section, select the **required tables**.

<figure><img src="../../../../.gitbook/assets/S (61).png" alt="" width="466"><figcaption><p>Selecting Process Table</p></figcaption></figure>

{% hint style="info" %}
**Tip:** You can select a **single column, multiple columns,** or **all columns** based on your requirement. Selecting the **Select All** checkbox allows you to select all tables at once. See the **ticked checkbox** in the image below.

![](<../../../../.gitbook/assets/image (172).png>)
{% endhint %}

</details>

<details>

<summary><strong>Preview Configuration</strong></summary>

**Purpose:**

The purpose of **Preview** during the configuration of a **UCM File Loader Input Node** while creating a **delta pipeline** is to **validate the file ingestion setup**.

**Procedure:**

The below step-by-step instructions describe the procedure:

* On the **Right Pane**, click the **Preview** icon on the top of **UCM File Loader Input Node.**

<figure><img src="../../../../.gitbook/assets/S (62).png" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

The **Files uploaded on the file storage** message is displayed. See the image below.

<figure><img src="../../../../.gitbook/assets/S (63).png" alt=""><figcaption><p>Files uploaded Message</p></figcaption></figure>

</details>

<details>

<summary><strong>Save Pipeline</strong></summary>

**Purpose**

After selecting the input node, you need to save the pipeline to persist its configuration and make it available for execution. Saving ensures that all input node settings are retained and correctly applied during pipeline runs.

**Procedure**

As part of the procedure, you need to provide a **name** for the pipeline along with specifying the **summary** of the delta pipeline and the **metadata** including **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (14).png" alt="" width="563"><figcaption></figcaption></figure>

The Pipeline is saved.

</details>

### Configuring GRAPHQL Input Node

#### Overview

You can configure the **GRAPHQL Input Node** while creating a **delta pipeline** **when the source system exposes data through a** [<mark style="color:blue;">**GraphQL API**</mark>](#user-content-fn-21)[^21] **and the data needs to be extracted efficiently**. The configuration can be completed by following a sequence of guided steps. The below table provides a brief overview of each step involved in the process.

> <mark style="color:red;">**Note:**</mark> To configure the GRAPHQL Input Node, an existing GRAPHQL API connection must be available in your account.

<table><thead><tr><th width="254">Step</th><th>Description</th></tr></thead><tbody><tr><td><a href="copy-of-configuring-input-nodes.md#select-graphql-input-node">Select GRAPHQL Input Node</a> </td><td>This is the first step in the <strong>GRAPHQL Input Node</strong> configuration process. As part of this step, you will drag <strong>GRAPHQL</strong> from the <a data-footnote-ref href="#user-content-fn-8"><mark style="color:blue;">Node Palette</mark></a><mark style="color:blue;">,</mark> and then place it on the in the <strong>Main Workspace</strong>.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#select-an-existing-api-connection">Select an Existing API Connection </a></td><td>As part of this step, you will select an existing API connection.  Once selected, the system <strong>automatically populates the API endpoint URL</strong> associated with that connection. </td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#configure-graphql-api-inputs">Configure GRAPHQL API Inputs</a></td><td>As part of configuring <strong>GRAPHQL API Inputs</strong>, you will define <a data-footnote-ref href="#user-content-fn-22"><mark style="color:blue;">GraphQL Parameter</mark></a>, <a data-footnote-ref href="#user-content-fn-23"><mark style="color:blue;">Header</mark></a>, and <a data-footnote-ref href="#user-content-fn-24"><mark style="color:blue;">GraphQL Query</mark></a>.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#preview-data">Preview Data</a></td><td>You can preview the data both in JSON and tabular formats. Previewing allows  to validate and test the configuration in real time before running the complete pipeline or workflow.</td></tr><tr><td><a href="copy-of-configuring-input-nodes.md#save-pipeline">Save Pipeline</a></td><td><strong>Saving</strong> ensures that all input node settings are retained and correctly applied during pipeline runs.</td></tr></tbody></table>

#### Procedure

The expandable panels below provide guided assistance for each step in the configuration process. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Select GRAPHQL Input Node</strong> </summary>

**Purpose:**

The purpose of selecting the **GraphQL Input Node** before creating a delta pipeline is to define the **GraphQL API** as the data source and establish how incremental data will be retrieved.

**Procedure:**

As part of selecting the **GRAPHQL Input Node**, you need to drag it from the **Node Palette** and then place it on the in the **Main Workspace**. Once placed, the **Select GRAPHQL API** and **Select Data Frame** sections are displayed in the left pane.&#x20;

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

<figure><img src="../../../../.gitbook/assets/S (1).png" alt=""><figcaption><p>Input Menu Item</p></figcaption></figure>

The [<mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-5)[^5] is displayed.&#x20;

3. From the **Node Palette**, select **GRAPHQL,** and drag it onto the **Main Workspace.**

<figure><img src="../../../../.gitbook/assets/S (64).png" alt="" width="462"><figcaption><p>Selecting GRAPHQL Input Node</p></figcaption></figure>

The **Select GRAPHQL API** and **Select Data Frame** sections are displayed in the left pane. &#x20;

</details>

<details>

<summary><strong>Select an Existing API Connection</strong> </summary>

**Purpose:**

**Selecting an existing API** defines the endpoint from which the pipeline retrieves or sends data. In the SCIKIQ application, selecting an API connection automatically populates the **API endpoint URL** associated with that connection. This endpoint is used to execute the configured GraphQL query.&#x20;

**Procedure:**

The below step-by-step instructions describe the procedure:

1. On the **Left Pane**, from the **Select Connection** drop-down box, select the required **API connection** in the the **Select GRAPHQL API** section.&#x20;

<figure><img src="../../../../.gitbook/assets/S (65).png" alt=""><figcaption><p>Selecting GRAPHQL API Connection</p></figcaption></figure>

The **API endpoint URL** associated with that connection is automatically displayed.

{% hint style="info" %}
**Tip:** To view the **Select GRAPHQL API** section larger, click the **Toggle Full Screen** icon.

<img src="../../../../.gitbook/assets/S (66).png" alt="" data-size="original">
{% endhint %}

2. Click the **Show details** ![](<../../../../.gitbook/assets/image (173).png>) icon on the **Select GRAPHQL API** screen if the URL is not visible.

</details>

<details>

<summary><strong>Configure GRAPHQL API Inputs</strong></summary>

**Purpose:**

Configuring the **GRAPHQL API Inputs** define **how the node communicates with the GraphQL API and what data it retrieves or modifies**. The below table provides description of API inputs:

<table><thead><tr><th width="199" valign="top">Input</th><th width="312" valign="top">Description</th><th valign="top">Example</th></tr></thead><tbody><tr><td valign="top">GraphQL Parameters</td><td valign="top">GraphQL Parameters allow you to pass <strong>dynamic values</strong> to the GraphQL query at runtime.</td><td valign="top"><p>userId</p><p>fromDate</p><p>limit</p></td></tr><tr><td valign="top">Header</td><td valign="top">Headers are used to <strong>authenticate and authorize</strong> the API request and to pass additional request metadata.</td><td valign="top">api-key: &#x3C;key></td></tr><tr><td valign="top">GraphQL Query</td><td valign="top">GraphQL Query defines <strong>what operation to perform and what data to fetch or modify.</strong></td><td valign="top"></td></tr></tbody></table>

**Procedure:**

The below step-by-step instructions describe the procedure:

1. On the **Select GRAPHQL API** section, the **Toggle Full Screen** icon section to view it larger.&#x20;

<figure><img src="../../../../.gitbook/assets/image (174).png" alt=""><figcaption><p>Toggle Full Screen icon</p></figcaption></figure>

2. Specify the **GraphQL Parameters, Header**, and **GraphQL Query** input&#x73;**.** See the above table for the description of these inputs.

<figure><img src="../../../../.gitbook/assets/S (67).png" alt="" width="563"><figcaption><p>GraphQL Parameters, Header, and Query</p></figcaption></figure>

</details>

<details>

<summary><strong>Preview Data</strong></summary>

**Purpose:**

Previewing data allows to **validate and test GraphQL configuration in real time** before running the complete pipeline or workflow.

**Procedure:**

You can preview the data in both **JSON** and **tabular** formats. Enabling the [<mark style="color:blue;">DF</mark>](#user-content-fn-14)[^14] option treats the incoming data as rows and columns and displays it in a tabular view.&#x20;

**Procedure:**

The below step-by-step instructions describe the procedure:

**1.Preview Data in JSON Format**

A. In the **Select Data Frame** section, leave the **DF Enable** option in the disabled state.

<figure><img src="../../../../.gitbook/assets/S (68).png" alt=""><figcaption><p>DF Enable in Disabled State</p></figcaption></figure>

B. On the **Right Pane**, click the **Preview** icon on the top of **GRAPHQL Node.**

<figure><img src="../../../../.gitbook/assets/S (69).png" alt=""><figcaption><p>Prewing Data</p></figcaption></figure>

The data is displayed on the JSON Preview tab. See the example image below:

<figure><img src="../../../../.gitbook/assets/S (70).png" alt=""><figcaption><p>Data Preview in JSON Format</p></figcaption></figure>

**2.Preview Data in Tabular Format**

A. On the **Left Pane**, in the **Select Data Frame** section, enable the **DF Enable** option.&#x20;

B. From the **Select Data Frame** drop-down box, select the required **Data Frame,** and then click the **Preview** icon on the top of **GRAPHQL Node**.

<figure><img src="../../../../.gitbook/assets/S (71).png" alt=""><figcaption><p>Selecting Data Frame and Previewing Data</p></figcaption></figure>

&#x20;The data is displayed in tabular format. See the image below.

<figure><img src="../../../../.gitbook/assets/S (72).png" alt=""><figcaption><p>Data Preview in Tabular Format</p></figcaption></figure>

</details>

<details>

<summary><strong>Save Pipeline</strong></summary>

**Overview**

After selecting the input node, you need to save the pipeline to persist its configuration and make it available for execution. Saving ensures that all input node settings are retained and correctly applied during pipeline runs.

**Procedure**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (14).png" alt="" width="563"><figcaption></figcaption></figure>

The Pipeline is saved.

</details>

## Related Topics

* [Applying Transform Nodes](/broken/pages/wbuWbzMSOZjkjpmFRBzV)
* [Using Output Nodes](../using-output-nodes/)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.

[^2]: The **Node Palette** contains a set of input nodes, including Database Input, File Input, Query Input, API, GraphQL, SAP APP, NoSQL, and UCM File Loader.

[^3]: Selecting the **Datasource** option connects to an external database.

[^4]: Selecting the **Assets** option use pre-configured datasets stored within SCIKIQ.

[^5]: 

    **Input Nodes' Description**



    * **Database Input** – Extracts structured data from relational databases
    * **File Input** – Reads data from files like CSV, Excel, JSON, or XML
    * **Query Input** – Fetches data by running custom SQL queries
    * **API Input** – Pulls data from external applications using REST APIs
    * **GraphQL Input** – Retrieves data using flexible GraphQL queries
    * **SAP APP Server Input** – Connects to SAP systems to extract business data
    * **NoSQL Input** – Reads data from NoSQL databases such as MongoDB
    * **UCM File Loader** – Loads files stored in UCM repositories into the pipeline

[^6]: **ASC** refers to Ascending Order.

[^7]: **DESC** refers to Descending Order.

[^8]: The Node Palette contains a set of input nodes, including Database Input, File Input, Query Input, API, GraphQL, SAP APP, NoSQL, and UCM File Loader.

[^9]: 

    **Node Palette Components**



    * **Database Input** – Extracts structured data from relational databases
    * **File Input** – Reads data from files like CSV, Excel, JSON, or XML
    * **Query Input** – Fetches data by running custom SQL queries
    * **API Input** – Pulls data from external applications using REST APIs
    * **GraphQL Input** – Retrieves data using flexible GraphQL queries
    * **SAP APP Server Input** – Connects to SAP systems to extract business data
    * **NoSQL Input** – Reads data from NoSQL databases such as MongoDB
    * **UCM File Loader** – Loads files stored in UCM repositories into the pipeline

[^10]: The **Base URL** specifies the main address of the API service.

[^11]: The **Endpoint URL** identifies the specific resource or operation being accessed.

[^12]: The **authentication key** defines the credentials required for access.

[^13]: The **token** provides a secure, time-bound authorization for API communication.

[^14]: Data Frame

[^15]: **Core Data Services**&#x20;

[^16]: Identifies the UCM environment and establishes a secure connection to access UCM-managed content

[^17]: Specifies the underlying storage service where the UCM files physically reside

[^18]: Defines the exact directory or bucket from which files should be read, limiting ingestion to the relevant file location

[^19]: Determines the processing logic applied to the files, such as parsing rules, metadata handling, and ingestion behavior

[^20]: Define how the ingested UCM files are structured and interpreted as tabular data for pipeline processing.

[^21]: A **GraphQL API** lets applications request exactly the data they need from a single endpoint, using a structured query format.

[^22]: Allows you to pass **dynamic values** to the GraphQL query at runtime

[^23]: Used to **authenticate and authorize** the API request and to pass additional request metadata

[^24]: Defines **what operation to perform and what data to fetch or modify**
