# Using Write No SQL Output Node

This page explains how to use the **Write** **No SQL Output** node with an input node. A **Write NoSQL** node can be used with an **input node** when the pipeline needs to store incoming or processed data in a **NoSQL database** such as MongoDB. It is typically used when the data from the input node is in a structured or semi-structured format and needs to be persisted in a scalable, schema-flexible NoSQL data store.

**Key Concepts:**

<details>

<summary><strong>How Write</strong> <strong>No SQL Output node works with an input node</strong></summary>

* The **input node** retrieves data from the configured source (such as a database, file, API, or event stream).
* The data flows through the pipeline and may optionally pass through **transform nodes** if data preparation is required.
* The **Write to NoSQL node** maps the incoming fields to the corresponding NoSQL collection or document structure.
* The processed records are then written to the configured **NoSQL database or collection**.

In simple terms, the input node provides the data and the Write to NoSQL node stores that data in the NoSQL system.

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The **Write to NoSQL node** can be connected to input nodes that produce **structured or semi-structured datasets**.

Applicable input nodes include:

* Database Input
* File Input
* API Input
* Kafka Topic (Event Input)

</details>

<details>

<summary><strong>Applicable Transform nodes (Optional)</strong></summary>

Transform nodes can be used between the input node and Write to NoSQL node when the data needs modification or preparation.

Applicable transform nodes include:

* Mapping / Data Transform
* Filter
* Join
* Aggregation
* EDA Transform

</details>

<details>

<summary><strong>Non-applicable nodes</strong></summary>

The **Write to NoSQL node** cannot be connected directly to nodes that **do not produce row-level data** or are used only for configuration.

Non-applicable nodes include:

* API Schema Node
* Execution Settings
* Parameters
* Any control or utility nodes that do not output datasets.

</details>

Connecting the **Write** **No SQL** **output** node to an input node involves a sequence of steps. The table below provides a brief overview of each step in the process.

<table><thead><tr><th width="221">Step</th><th valign="top">Description</th></tr></thead><tbody><tr><td><a href="using-write-no-sql-output-node.md#add-input-node">Add Input Node</a></td><td valign="top">This is the first step in applying  <strong>Write</strong> <strong>No SQL output node</strong> to an input node. As part of this, you will drag the required input node from the <a data-footnote-ref href="#user-content-fn-1"><mark style="color:blue;">Input Node Palette</mark></a> and then place it on the <strong>Main Workspace.</strong></td></tr><tr><td><a href="using-write-no-sql-output-node.md#select-necessary-columns">Select Necessary Columns</a> </td><td valign="top">After placing the input node, you will select the <strong>necessary  columns</strong> pertaining to the source. This is to make them appear when input node is connected with the <strong>Write</strong> <strong>No SQL output</strong> node. </td></tr><tr><td><a href="using-write-no-sql-output-node.md#connect-write-no-sql-output-node-to-an-input-node">Connect Write No SQL Output Node to Input Node</a></td><td valign="top">As part of this step, you will drag the <strong>Write</strong> <strong>No SQL output</strong> node from the  <a data-footnote-ref href="#user-content-fn-2"><mark style="color:blue;"><strong>Output Node Palette</strong></mark></a> and then place it on the <strong>Main Workspace</strong>. Once done, you can connect both the <strong>Input</strong> and  <strong>Write</strong> <strong>No SQL output</strong> nodes.</td></tr><tr><td><a href="using-write-no-sql-output-node.md#configure-mongodb-connection">Configure MongoDB Connection</a></td><td valign="top">Subsequent to connecting the input node and <strong>Write</strong> <strong>No SQL output</strong> node, you will configure <strong>MongoDB Connection.</strong> Configuring a <strong>MongoDB connection</strong> enables the pipeline to communicate with the MongoDB database. It specifies the connection details required for the <strong>Write to NoSQL node</strong> to store pipeline data in the designated MongoDB collection.</td></tr><tr><td><a href="using-write-no-sql-output-node.md#save-etl-job">Save ETL Job</a></td><td valign="top">After selecting the columns, you will save the <strong>ETL job</strong> to confirm the pipeline setup. This ensures that the <strong>Write</strong> <strong>No SQL output</strong> node is configured correctly and can be used effectively during execution. Once saved, the pipeline is displayed on the <strong>Data Pipelines</strong> page.</td></tr><tr><td><a href="using-write-no-sql-output-node.md#run-pipeline">Run Pipeline</a></td><td valign="top"><strong>Running the pipeline</strong> triggers the data flow from the input node and writes the records to the configured NoSQL database. It also confirms that the node configuration is correct and that the data is successfully stored in the target collection.</td></tr><tr><td><a href="using-write-no-sql-output-node.md#validate-data-in-mongodb">Validate Data in MongoDB</a></td><td valign="top">Validating the data in MongoDB after executing the pipeline ensures that the records have been successfully inserted into the specified collection. It helps confirm that the pipeline has stored the data accurately in the database.</td></tr></tbody></table>

***

## Procedure

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Add Input Node</strong></summary>

**Overview:**

As part of adding the **Input Node**, you need to drag it from the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-3)[^3] and then place it on the in the **Main Workspace**. Once placed, the input fields corresponding to the selected node are displayed on the left pane.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

,The  [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-3)[^3] is displayed.&#x20;

3. From the  [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-3)[^3], select the **Input Node** (For example, Database Input), and drag it onto the **Main Workspace.**&#x20;

<figure><img src="../../../../.gitbook/assets/S (431).png" alt=""><figcaption><p>Adding Input Node</p></figcaption></figure>

The Select File Type and Scheme Properties are displayed in the left pane Left Pane.

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

<figure><img src="../../../../.gitbook/assets/S (432).png" alt=""><figcaption><p>Selecting database Type and Connection</p></figcaption></figure>

{% hint style="info" %}
**Tip:**&#x20;

* If required, you can create a new data source connection by clicking the **Create New Connection** ![](<../../../../.gitbook/assets/image (158).png>) button. To learn **how to create a new data source connection**, click [**Creating a New Data Source Connection**](/broken/pages/Ga8WoiowoXOkY4RtBNpS).
{% endhint %}

C. If you want **Asset,** then select the required **asset** from the **Asset** drop-down box.

{% hint style="info" %}
Tip: &#x20;

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

<figure><img src="../../../../.gitbook/assets/S (433).png" alt="" width="563"><figcaption><p>Selecting Columns</p></figcaption></figure>

The **Column Details Saved** message is displayed.

</details>

<details>

<summary><strong>Connect Write</strong> <strong>No SQL</strong> <strong>Output Node to an Input Node</strong></summary>

**Purpose:**

The purpose of connecting a **Write to NoSQL node** to an **input node** is to store the incoming or processed data from the pipeline into a NoSQL database. The input node provides the data, and the Write to NoSQL node writes that data into the specified NoSQL collection or data store.

**Procedure:**

As part of connecting the **Write to NoSQL node** with the input node, you need to first drag it from the [<mark style="color:blue;">**Output Node Palette**</mark>](#user-content-fn-2)[^2] on to the **Mainwork space**, and then connect it with the input node.

> <mark style="color:red;">**Note:**</mark> If required, you can add the required transform node in between **input node** and **Write to NoSQL node**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Top Toolbar**, click the **Output Nodes** menu item.

The [<mark style="color:blue;">**Output Node Palette**</mark>](#user-content-fn-2)[^2] is dispalette is displayed.

2. From the [<mark style="color:blue;">**Output Node Palette**</mark>](#user-content-fn-2)[^2]<mark style="color:blue;">**,**</mark> drag the **Write to NoSQL node** on to the **Main Workspace**, and then connect them.&#x20;

<figure><img src="../../../../.gitbook/assets/S (444).png" alt=""><figcaption><p>Connecting Nodes</p></figcaption></figure>

Once the **Write to NoSQL node** is connected with the input node, the input fields corresponding to it are displayed on the left pane.

</details>

<details>

<summary><strong>Configure MongoDB Connection</strong></summary>

**Purpose:**

The purpose of configuring a **MongoDB connection** is to establish a connection between the pipeline and the MongoDB database. It provides the required connection details so the **Write to NoSQL node** can write the processed data from the input node into the specified MongoDB collection.

**Procedure:**

The below step-by-step instructions describe the procedure:&#x20;

1. On the **Left Pane,** from the **Data Source** drop-down box, select the **required MongoDB connection.**

{% hint style="info" %}
**Tip:** If no connection exists, then create a new MongoDB connection by clicking the **Create New Connection** ![](<../../../../.gitbook/assets/image (2538).png>)   button.
{% endhint %}

2. In the **Schema Properties** section, from the **Table** drop-down box, select the **required table.**

<figure><img src="../../../../.gitbook/assets/S (445).png" alt=""><figcaption><p>Configuring MongoDB Connection</p></figcaption></figure>

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the **Write** **No SQL** **Output Node** can be configured correctly and used during execution.

**Procedure**

As part of saving the ETL job, you need to input a **name** and **description** for the pipeline along with specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption><p>Save Button</p></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (446).png" alt="" width="563"><figcaption><p>Saving Pipeline</p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Run Pipeline</strong></summary>

**Purpose:**

The purpose of running the pipeline after connecting the **Write to NoSQL** output node to an input node is to execute the data flow and store the incoming records in the specified NoSQL database. It also helps verify that the configuration is correct and that the data is successfully written to the target collection.

**Procedure:**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step instructions:**

1. On the **Data Pipelines,** click the **Run** button corresponding to the **Write No SQL Pipeline**.

<figure><img src="../../../../.gitbook/assets/S (447).png" alt=""><figcaption><p>Pipeline Run Button</p></figcaption></figure>

The **Delta Pipeline Parameters** screen is displayed.

2. On the **Delta Pipeline Parameters** screen, make the changes required, and then click the **Run** button.

<figure><img src="../../../../.gitbook/assets/S (448).png" alt="" width="563"><figcaption><p>Running Pipeline</p></figcaption></figure>

The pipeline is executed and **Logs Viewer** screen is displayed.

</details>

<details>

<summary><strong>Validate Data in MongoDB</strong></summary>

**Purpose:**

The purpose of **validating data in MongoDB** after running the Write to NoSQL pipeline is to confirm that the records have been successfully written to the target MongoDB collection. It helps ensure that the data has been stored correctly and that the pipeline execution produced the expected results.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

* Open the **MongoDB database** using MongoDB Compass or another supported client.
* Navigate to the **target database and collection**.
* Verify that the data has been inserted correctly.

</details>

## Related Topics

* [Configuring Input Nodes](/broken/pages/Qe52MzyFrHp43dWO41kf)
* [Configuring Transform Nodes](/broken/pages/hbzg9uHn194g3ivtwx4q)

[^1]: The Input Node Palette contains a set of input nodes, including Database Input, File Input, Query Input, API, GraphQL, SAP APP, NoSQL, and UCM File Loader.

[^2]: **Output Nodes:**



    * **Table Output** – Writes processed data into a database table.
    * **File Output** – Saves processed data to files in a specified file format and location.
    * **GraphQL Write** – Sends processed data to a GraphQL endpoint for consumption by applications.
    * **Table Update** – Updates existing records in a database table using incoming data.
    * **Merge** – Synchronizes source data with a target table by inserting new records and updating existing ones.
    * **Put API** – Pushes processed data to an external or internal system through an API call.
    * **Kafka Producer** – Publishes processed data as events to a Kafka topic.
    * **Files to Tables** – Loads data from files directly into database tables.
    * **Write NoSQL** – Writes processed data into a NoSQL database.

[^3]: The **Input Node Palette** contains a set of input nodes, including Database Input, File Input, Query Input, API, GraphQL, SAP APP, NoSQL, and UCM File Loader.
