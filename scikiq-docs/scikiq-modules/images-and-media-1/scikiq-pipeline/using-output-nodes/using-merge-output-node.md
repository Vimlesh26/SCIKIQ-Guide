# Using Merge Output Node

This page explains how to use the **Merge node** node with an input node. You can use the **Merge** node when there is a need to merge one table with another table and synchronize the target table with incoming records.. You can merge the tables by choosing **Row Wise, Temp Table,** or same **Database.**

**Key Concepts:**

<details>

<summary><strong>How Merge node works with an input node</strong></summary>

* The **input node** reads data from the source system (database, file, API, or event stream).
* The **Merge node** compares incoming records with the target table using configured **match (key) columns**.&#x20;
* Based on the comparison:
  * Matching records are **updated**
  * Non-matching records are **inserted**
  * (Optional) Records not present in the source can be **deleted or marked inactive**, depending on configuration
* The Merge node applies these changes atomically to keep the target table synchronized.

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The Merge node can be connected to any input node that produces **structured, row-level data** including **Database Input, File Input, API Input, and Kafka Topic (Event Input).**

</details>

<details>

<summary><strong>Applicable Transform nodes</strong></summary>

Transform nodes can be placed between the **input node** and the **Merge** node when data preparation is required: **Mapping / Data Transform, Filter, Join,Aggregation,** and **EDA Transform.**

</details>

<details>

<summary><strong>Non-applicable nodes</strong></summary>

The Merge node **cannot be connected directly** to nodes that do not emit structured datasets or serve only configuration purposes: **API Schema Node, Execution Settings, Parameters**, and Control or utility nodes that do not output row-level data.&#x20;

</details>

Connecting the Merge output node to an input node involves a sequence of steps. The table below provides a brief overview of each step in the process.

<table><thead><tr><th width="221">Step</th><th valign="top">Description</th></tr></thead><tbody><tr><td><a href="using-merge-output-node.md#add-input-node">Add Input Node</a></td><td valign="top">This is the first step in applying  <strong>Merge output</strong> node to an input node. As part of this, you will drag the required input node from the <a data-footnote-ref href="#user-content-fn-1"><mark style="color:blue;">Input Node Palette</mark></a> and then place it on the <strong>Main Workspace.</strong></td></tr><tr><td><a href="using-merge-output-node.md#select-necessary-columns">Select Necessary Columns</a> </td><td valign="top">After placing the input node, you will select the <strong>necessary  columns</strong> pertaining to the source. This is to make them appear when input node is connected with the <strong>Merge output</strong> node. </td></tr><tr><td><a href="using-merge-output-node.md#connect-merge-output-node-to-input-node">Connect Merge Output Node to Input Node</a></td><td valign="top">As part of this step, you will drag the <strong>Merge output</strong> node from the  <a data-footnote-ref href="#user-content-fn-2"><mark style="color:blue;"><strong>Output Node Palette</strong></mark></a> and then place it on the <strong>Main Workspace</strong>. Once done, you can connect both the <strong>Input</strong> and  <strong>Merge output</strong> nodes.</td></tr><tr><td><a href="using-merge-output-node.md#configure-target-type-and-merge-type">Configure Target Type and Merge Type</a></td><td valign="top">Subsequent to connecting the input node and <strong>Merge output</strong> node, you will configure <strong>Target Type</strong> and <strong>Merge Type</strong>. <strong>Target Type</strong> defines where the merge is applied, and <strong>Merge Type</strong> defines how the merge is executed.</td></tr><tr><td><a href="using-merge-output-node.md#configure-join-operator">Configure Join Operator</a></td><td valign="top">As part of this step, you will configure the Join operator,  which defines how source data is matched with target table records using key columns.</td></tr><tr><td><a href="using-merge-output-node.md#save-etl-job">Save ETL Job</a></td><td valign="top">After selecting the columns, you will save the <strong>ETL job</strong> to confirm the pipeline setup. This ensures that the <strong>Merge output</strong> node is configured correctly and can be used effectively during execution. Once saved, the pipeline is displayed on the <strong>Data Pipelines</strong> page.</td></tr><tr><td><a href="using-merge-output-node.md#run-pipeline">Run Pipeline</a></td><td valign="top">After connecting the <strong>Merge node</strong> with the input node, running it executes the merge operation by comparing incoming source data with the target table. This applies the configured join, match, and unmatch rules to insert new records and update existing ones, ensuring the target table is synchronized with the source data.</td></tr></tbody></table>

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

<summary><strong>Connect Merge Output Node to Input Node</strong></summary>

**Purpose:**

The **purpose** of connecting a **Merge output node** with an **input node** is to **synchronize incoming source data with an existing target table**. The input node provides the source records, and the Merge node compares them with the target table to insert new records, update existing ones, or apply other configured merge actions, ensuring the target table stays up to date.

**Procedure:**

As part of connecting the **Merge output node** with the input node, you need to first drag the **Merge output node** from the [<mark style="color:blue;">**Output Node Palette**</mark>](#user-content-fn-2)[^2] on to the **Mainwork space**, and then connect it with the input node.

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Top Toolbar**, click the **Output Nodes** menu item.

The [<mark style="color:blue;">**Output Node Palette**</mark>](#user-content-fn-2)[^2] is dispalette is displayed.

2. From the [<mark style="color:blue;">**Output Node Palette**</mark>](#user-content-fn-2)[^2]<mark style="color:blue;">**,**</mark> drag the **Merge output node** on to the **Main Workspace**, and then connect them.&#x20;

<figure><img src="../../../../.gitbook/assets/S (434).png" alt=""><figcaption><p>Connecting Nodes</p></figcaption></figure>

Once the Merge is connected with the input node, the input fields corresponding to the Merge node are displayed on the left pane.

</details>

<details>

<summary><strong>Configure Target Type and Merge Type</strong></summary>

**Purpose:**

The **target table** specifies the destination table where the merge operation is applied and where records are inserted or updated. The **merge type** defines how the merge is performed, such as merging row by row, using a temporary table, or merging within the same database. Together, they control where the data is written and the strategy used to keep the target table in sync with the source data.

**Procedure:**

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. On the **Left Pane**, in the **Database Type** section, select the **Database Type** and **Connection.**
2. From the **Target** table drop-down box, select the **target table**.

{% hint style="info" %}
**Tip:** The **target table** is the **destination table** where the final operation is applied.
{% endhint %}

3. From the **Merge Type** drop-down box, select the required **merge type** select the required merge type choosing from **Row Wise, Temp Table,** or same **Database.**

{% hint style="info" %}
**Tip: Description of Merge Options**

* **Row Wise** – Merges records one by one by matching key columns and inserting or updating rows accordingly.
* **Temp Table** – Loads source data into a temporary table first and then merges it with the target table for better performance on large datasets.
* **Same Database** – Performs the merge directly within the same database when both source and target tables are located there, ensuring faster execution.
{% endhint %}

4\. Select the **Join** tab, if it is already not selected by default, and then click the **Add** ![](<../../../../.gitbook/assets/image (2533).png>)icon corresponding to it.

The Source and Target drop-down boxes are displayed.

T

</details>

<details>

<summary><strong>Configure Join Operator</strong></summary>

**Purpose:**

The **Join** configuration defines how source records are matched with existing records in the target table by specifying key columns used for comparison. Based on this matching logic, the **Match** functionality updates existing target records when a match is found, while the **Unmatch** functionality inserts new records into the target table when no match exists.

**Procedure:**

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. On the **Left Pane**, under the **Join** tab, click the **Add** ![](<../../../../.gitbook/assets/image (2533).png>)icon corresponding to it.

The Source and Target drop-down boxes are displayed.

2. From the **Source** drop-down box, select the **source**. For example, order\_id.
3. From the **Target** drop-down box, select the **target**. For example, order\_id.

> <mark style="color:red;">**Note:**</mark> You can add multiple source–target row mappings by clicking the **Add** ![](<../../../../.gitbook/assets/image (2533).png>)icon. To remove a row, click the **Delete** ![](<../../../../.gitbook/assets/image (2534).png>)icon.

{% hint style="info" %}
**Tip:** The purpose of selecting **source** and **target** as part of the **Join** operation is to define **how incoming data is matched with existing records** in the target table. By mapping source fields to corresponding target fields, the Merge node can identify matching and non-matching records and apply the appropriate insert or update actions during the merge process.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (435).png" alt=""><figcaption><p>Configuring Join Operator</p></figcaption></figure>

The Pipeline Review message box is displayed.

4. On the **Pipeline Review message box**, click the **OK** button.

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the  **Merge** node can be configured correctly and used during execution.

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

<figure><img src="../../../../.gitbook/assets/S (436).png" alt="" width="563"><figcaption><p>Saving ETL Job </p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Run Pipeline</strong></summary>

**Purpose:**

After connecting the **Merge node** with the input node, running it executes the merge operation by comparing incoming source data with the target table. This applies the configured join, match, and unmatch rules to insert new records and update existing ones, ensuring the target table is synchronized with the source data.

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step instructions:**

1. On the **Delta Pipelines** page, click the **Edit** icon corresponding to the saved pipeline.&#x20;

<figure><img src="../../../../.gitbook/assets/S (437).png" alt=""><figcaption><p>Pipeline Run Button</p></figcaption></figure>

The Pipeline Parameters screen is displayed.

2. On the Pipeline Parameters **screen**, make the required changes, and then click the **OK button.**

<figure><img src="../../../../.gitbook/assets/S (438).png" alt=""><figcaption><p>Running Pipeline</p></figcaption></figure>

The Logs Viewer screen is displayed with **Running** status. See the image below.

<figure><img src="../../../../.gitbook/assets/S (439).png" alt=""><figcaption><p>Pipeline Running Status</p></figcaption></figure>

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
