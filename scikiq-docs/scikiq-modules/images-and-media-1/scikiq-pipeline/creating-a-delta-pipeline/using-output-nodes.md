---
icon: circle-share-nodes
---

# Using Output Nodes

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The **Output nodes** act as the final destination in a pipeline and define where and how the processed data is delivered after all input and transformation steps are completed.

In a pipeline flow, input nodes bring data into the system, transform nodes process the data, and output nodes deliver the final result to the target destination.

Input Nodes → Transform Nodes → Output Nodes

> <mark style="color:red;">**Note:**</mark> It is not mandatory to include a transform node every time when connecting an output node to an input node. If no data transformation is required, the output node can be connected directly to the input node. A transform node should be added only when the data needs to be modified, enriched, or restructured before being written to the output.

***

### Using Output Nodes

SCIKIQ supports the below mentioned output nodes:

{% tabs %}
{% tab title="Table Output" %}
**Overview**

You can use the **Table Output** node to **write the final processed data into a target table** in a database or data platform. It acts as the **last step in a pipeline**, persisting data after it has been read, transformed, validated, or enriched.

**Key Concepts:**

<details>

<summary><strong>How Table Output node works with an input node</strong></summary>

The Table Output node works with an input node as mentioned below:

* The **input node** reads data from the configured source (such as a database, file, API, or event stream).
* The data is passed downstream in a structured format to the **Table Output node**.
* The **Table Output node** maps the incoming fields to the columns of the target database table.
* If the input data schema matches the target table schema, the data is written directly without any transformation.
* If schema alignment or data preparation is required, a **transform node** can be added between the input and Table Output nodes.
* The Table Output node then inserts the incoming records into the target table based on its configuration.

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The **Table Output node** can be used with most structured input nodes, provided the incoming data can be represented in a tabular (row–column) format. These include - **Database input nodes, File input nodes (CSV, JSON, Parquet, etc., after parsing), API input nodes returning structured data, and Kafka or streaming inputs (after schema is defined).**

</details>

<details>

<summary><strong>Applicable Transform nodes</strong></summary>

The Table Output node can be used with all transform nodes that produce a **tabular output**, such as **Filter, Select / Project, Join, Aggregate, Calculated / Derived columns, Data type conversion, and Bulk column** operations.

</details>

<details>

<summary><strong>Non-applicable nodes</strong></summary>

The **Table Output node** cannot be connected to nodes that do **not produce row-level, structured data** or are meant only for configuration and control. In general, any node that does **not output a structured dataset** cannot be connected to a Table Output node.&#x20;

</details>

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Connect Table Output Node</strong></summary>

**Purpose:**

The purpose of connecting a **Table Output node** to an **Input/Transform node** is to **write the processed pipeline data into a database table for storage, analysis, or further use**.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

* On the **Right Pane**, place the **Input node, Transform node,** and **Table Output node** and then connect them.

> <mark style="color:red;">**Note:**</mark> Make sure you have added at least one input or transformation node to the canvas before continuing.

<figure><img src="../../../../.gitbook/assets/S (419).png" alt="" width="513"><figcaption><p>Connecting Table Output Node</p></figcaption></figure>

</details>

<details>

<summary><strong>Configure Input Node</strong></summary>

**Overview:**

As part of configuring the **input node**, you need to first select the **datasource connection**, select the **required table**, and then the **table columns**.&#x20;

**Procedure:**

The below mentioned step-by-step instructions describe the process:

**Step-by-Step Instructions**

A. On the **Right Pane**, click the **Input Node**.

The Input node fields are displayed on the left pane.

B. On the **Left Pane**, in the **Data Type** section, from the **Datasource** drop-down box, select the **required datasource.**

C. In the **Schema Properties** section, select the **required** **Table,** and **Table Columns**.

{% hint style="info" %}
**Tip:** For more information on how to configure the Database Input Node, click [Configuring Database Node](/broken/pages/UZQ10sI7DoyEEhybN9of).
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (420).png" alt="" width="543"><figcaption><p>Selecting Database and Table Columns</p></figcaption></figure>

</details>

<details>

<summary><strong>Configure Transform Node (Optional)</strong></summary>

**Overview:**

As part of configuring the transform node (in this example, it is Select node), you need to  select the **required columns.**

**Procedure:**

The below mentioned step-by-step instructions describe the process:

**Step-by-Step Instructions**

A. On the **Right Pane**, click the **Transform Node**. Here it is Select.

The corresponding fields are displayed on the left pane.

B. On the **Left Pane**, select the **required columns**.

<figure><img src="../../../../.gitbook/assets/S (421).png" alt="" width="518"><figcaption><p>Selecting Columns</p></figcaption></figure>

</details>

<details>

<summary><strong>Configure Table Output Node</strong></summary>

**Overview:**

As part of configuring the **Table Output** node, you need to select the choosing from **Create Table, Truncate Table,** and **Drop Table If Exists** option&#x73;**.**&#x20;

**Procedure:**

The below mentioned step-by-step instructions describe the process:

**Step-by-Step Instructions**

A. On the **Right Pane**, click the **Table Output Node**.

The Table Output Node fields are displayed on the left pane.

B. On the Left Pane, select Table Output options choosing from **Create Table, Truncate Table,** and **Drop Table If Exists.** See below for the description of these options.

{% hint style="info" icon="info" %}
**Table Output Options**

* **Create Table**: Creates a new table in the target database schema.
* **Truncate Table**: Deletes all records from an existing table before writing new data.
* **Drop Table If Exists**: Drops an existing table if found, then creates a new one.
{% endhint %}

C. In the **Test Name** field, enter a **name** for the table.

<figure><img src="../../../../.gitbook/assets/S (422).png" alt="" width="551"><figcaption><p>Configuring Table Options</p></figcaption></figure>

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Overview**

Saving the ETL job confirms the pipeline setup so the **Table Output** node can be configured correctly and used during execution.

**Procedure:**

The below mentioned step-by-step instructions describe the process:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (423).png" alt="" width="535"><figcaption><p>Saving ETL Job</p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Preview Data</strong></summary>

**Overview**

As part of previewing, you need to click the Preview icon on the top of Table Output node. Once done, the preview is displayed.

**Procedure:**

The below mentioned step-by-step instructions describe the process:

**Step-by-Step Instructions**

A. On the **Right Pane**, click the **Preview** icon on the top of **Table Output Node**.

<figure><img src="../../../../.gitbook/assets/S (424).png" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

The Pipeline Preview message is displayed.

B. Review the Pipeline Preview message, and then click the OK button.

<figure><img src="../../../../.gitbook/assets/S (425).png" alt="" width="521"><figcaption><p>Pipeline Preview Message Box</p></figcaption></figure>

The table output is displayed. See the below image.

<figure><img src="../../../../.gitbook/assets/S (426).png" alt=""><figcaption><p>Table Output Preview</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="File Output" %}
**Overview**

The File Output Node is used when the pipeline results need to be saved in a file format such as **CSV, Excel, JSON, or other supported formats**. It writes the output generated after data processing and transformations to a specified file location.

**Key Concepts:**

<details>

<summary><strong>How File Output node works with an input node</strong></summary>

The File Output node works with an input node as mentioned below:

* The **Input Node** connects to a data source such as a database, API, dataset, or file and fetches the required data
* The retrieved data may optionally pass through **transformation nodes** (such as Filter, Mapper, or Group) where it can be modified or processed.
* The **File Output Node** takes the incoming data from the previous node in the pipeline.
* The node exports the received data to a file in the configured format (for example, CSV, Excel, or JSON) and saves it to the specified location.

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The common compatible input nodes include: **Database input nodes, File input nodes, API input nodes (structured responses),** and **Kafka or streaming input nodes (after schema is defined).**

</details>

<details>

<summary><strong>Applicable Transform nodes</strong></summary>

The **File Output node** works with all transform nodes that produce structured or semi-structured output, such as: **Filter, Select / Rename, Join, Aggregate, Calculated or derived fields, Data type conversion, and Bulk column operations.**

</details>

<details>

<summary><strong>Non-applicable nodes</strong></summary>

The **File Output node** cannot be connected to nodes that **do not produce a dataset or tabular output that can be written to a file**. Since the File Output Node requires **structured data (rows and columns)** as input, nodes that generate other types of outputs cannot be connected directly to it.

</details>

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Connect File Output Node</strong></summary>



</details>

<details>

<summary><strong>Select File Storage Type, Connection, and Target Bucket</strong></summary>



</details>

<details>

<summary><strong>Set File Path and Format</strong></summary>



</details>

<details>

<summary><strong>Save ETL Job</strong></summary>



</details>

<details>

<summary><strong>Preview Data</strong></summary>



</details>
{% endtab %}

{% tab title="Table Update" %}
**Overview**

The **Table Update Output Node** can be connected with an **Input Node** when the data retrieved by the Input Node is used to **update existing records in a database table**.

**Key Concepts:**

<details>

<summary><strong>How Table Update node works with an input node</strong></summary>

The **Table Update** node works with an input node as mentioned below:

* The **Input Node** connects to a data source such as a database, dataset, or file and fetches the required data. This data usually contains the values that need to be updated.
* The retrieved data may pass through **transformation nodes** (such as Filter, Mapper, or SQL nodes) where it can be modified, filtered, or prepared for the update operation.
* The **Table Update Output Node** takes the processed data from the previous node in the pipeline.
* The node uses a **key column or condition** (such as ID, Customer ID, or Product ID) to match records in the target database table.
* The node updates the specified columns in the target table using the values provided in the pipeline data.

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The common compatible input nodes include: **Database input nodes, File input nodes, API input nodes (structured responses),** and **Kafka or streaming input nodes (after schema is defined).**

</details>

<details>

<summary><strong>Applicable Transform nodes</strong></summary>

The **Table Update node** can be connected to the transform nodes including **Mapping / Data Transform, Filter, Join, Aggregation,** and **EDA Transform.**

</details>

<details>

<summary><strong>Non-applicable nodes</strong></summary>

Input nodes that **do not produce updatable tabular data or do not support database update operations** are considered **non-applicable input nodes**.

</details>

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Connect Table Output Node</strong></summary>

* On the **Right Pane**, place the **Input node** and **Table Update node** and then connect them.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * In general, the input node is configured first to define the data source and how data is read. Once configured, it can be connected to an output node to specify where the data is written, without needing to reconfigure the input node.
> * In case, you want to know **how to configure the input nodes**, click [Configuring Input Nodes.](/broken/pages/Qe52MzyFrHp43dWO41kf)
> * Similarly, if you want to know **how to configure the transform nodes**, click [Applying Transform Nodes](/broken/pages/hbzg9uHn194g3ivtwx4q).

<figure><img src="../../../../.gitbook/assets/S (427).png" alt=""><figcaption><p>Connecting Nodes</p></figcaption></figure>

</details>

<details>

<summary><strong>Configure Table Update Node Settings</strong> </summary>

**Overview:**

As part of configuring the **Table Update node** settings, you need to select the columns, configure condition, and then map the **source** and **destination**.&#x20;

**Procedure:**

The below mentioned step-by-step instructions describe the process:

**Step-by-Step Instructions**

**A. Select Columns**

a. On the  **Right Pane**, select the **Table Update** node.

The input fields corresponding to the Table Update node are displayed on the left pane.

b. Go to the T**able Update** section on the **Left Pane**.

c. From the **Table** drop-down box, select the required **table**.&#x20;

The Columns are displayed.

d. Select the required **option** against the required **Column.** For example, order\_id.

<figure><img src="../../../../.gitbook/assets/S (428).png" alt="" width="512"><figcaption><p>Selecting Columns</p></figcaption></figure>

**B. Configure Conditions**

a. In the **Table Update** section, select the **Conditions** tab, and then click the **Add** ![](<../../../../.gitbook/assets/image (2532).png>) icon.

The Table, Column, Operator, and Value fields are displayed.

b. From the **Table** drop-down box,  select **Source** or **Target.** &#x20;

c. From **Column** drop-down box,, select the **required column.**

d. From the **Operator** drop-down box, select the required **operator.** For example, >.

e. In the Value field, enter the required value.

<figure><img src="../../../../.gitbook/assets/S (429).png" alt="" width="509"><figcaption><p>Configuring Conditions</p></figcaption></figure>



**C. Map Source** and **Destination**

a. In the **Table Update** section, select the **Map** tab, and then click the **Add** ![](<../../../../.gitbook/assets/image (2532).png>) icon.

The Source and Destination fields are displayed.

b. Select the required **Source** and **Destination.**

<figure><img src="../../../../.gitbook/assets/S (430).png" alt="" width="505"><figcaption><p>Mapping Source and Destination</p></figcaption></figure>

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Overview**

Saving the ETL job confirms the pipeline setup so the **Table Update** node can be configured correctly and used during execution.

**Procedure:**

The below mentioned step-by-step instructions describe the process:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Preview Data</strong></summary>

* On the **Right Pane**, click the **Preview** icon on the top of **Table Update** node.

The file output is displayed.&#x20;

</details>
{% endtab %}

{% tab title="Merge Output" %}
**Overview**

You can use the **Merge** node when there is a need to merge one table with another table and synchronize the target table with incoming records.. You can merge the tables by choosing **Row Wise, Temp Table,** or same **Database.**

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

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Add Input Node</strong></summary>

**Overview:**

As part of adding the **Input Node**, you need to drag it from the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] and then place it on the in the **Main Workspace**. Once placed, the input fields corresponding to the selected node are displayed on the left pane.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

,The  [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] is displayed.&#x20;

3. From the  [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1], select the **Input Node** (For example, Database Input), and drag it onto the **Main Workspace.**&#x20;

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
{% endtab %}

{% tab title="Kafka Producer Output" %}
**Overview**

A **Kafka Producer** can be used with an **input node** when the pipeline needs to **publish incoming or processed data as events to a Kafka topic**. This is useful for real-time integrations, event-driven architectures, and streaming use cases where downstream systems consume data through Kafka.

**Key Concepts:**

<details>

<summary><strong>How Kafka Producer node works with an input node</strong></summary>

* The **input node** reads data from the configured source (such as a database, file, API, or event stream).
* The data flows downstream, optionally through transform nodes if processing is required.
* The **Kafka Producer** serializes the incoming data based on the configured message format.
*   The serialized data is then published as messages to the specified Kafka topic.

    In simple terms, the input node supplies the data, and the Kafka Producer sends it to Kafka as events.

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The **Kafka Producer** node can be connected to input nodes that produce **structured, event-ready data**: **Database Input, File Input, API Input,** and **Kafka Topic** (for republishing or streaming transformations).

</details>

<details>

<summary><strong>Applicable Transform nodes</strong></summary>

Transform nodes can be placed between the input node and Kafka Producer when data preparation is required: Mapping / Data Transform, Filter, Join, Aggregation, and EDA Transform.

</details>

<details>

<summary><strong>Non-applicable nodes</strong></summary>

The **Kafka Producer** **cannot be connected directly** to nodes that do not output data records or are configuration-only components:: **API Schema Node, Execution Settings, Parameters**, and Control or utility nodes that do not output row-level data.&#x20;

</details>

**Procedure**

> <mark style="color:red;">**Note:**</mark> **Prerequisites for Using the Kafka Producer Node**
>
> * A Kafka connection must be configured in the system, or it can be created during node configuration.
> * The input data must be in a JSON-compatible structure before being sent to Kafka.
> * If the Avro message format is used, the corresponding Avro schema must be defined.

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Add Input Node</strong></summary>

**Overview:**

As part of adding the **Input Node**, you need to drag it from the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] and then place it on the in the **Main Workspace**. Once placed, the input fields corresponding to the selected node are displayed on the left pane.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

,The  [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] is displayed.&#x20;

3. From the  [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1], select the **Input Node** (For example, Database Input), and drag it onto the **Main Workspace.**&#x20;

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

<summary><strong>Connect Kafka Producer Output Node to an Input Node</strong></summary>

**Purpose:**

The **purpose** of connecting a **Kafka Producer output node** with an **input node** is to **synchronize incoming source data with an existing target table**. The input node provides the source records, and the **Kafka Producer** node compares them with the target table to insert new records, update existing ones, or apply other configured merge actions, ensuring the target table stays up to date.

**Procedure:**

As part of connecting the **Kafka Producer output node** with the input node, you need to first drag the **Kafka Producer output node** from the [<mark style="color:blue;">**Output Node Palette**</mark>](#user-content-fn-2)[^2] on to the **Mainwork space**, and then connect it with the input node.

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Top Toolbar**, click the **Output Nodes** menu item.

The [<mark style="color:blue;">**Output Node Palette**</mark>](#user-content-fn-2)[^2] is dispalette is displayed.

2. From the [<mark style="color:blue;">**Output Node Palette**</mark>](#user-content-fn-2)[^2]<mark style="color:blue;">**,**</mark> drag the **Kafka Producer output node** on to the **Main Workspace**, and then connect them.&#x20;

<figure><img src="../../../../.gitbook/assets/S (440).png" alt=""><figcaption><p>Connecting Nodes</p></figcaption></figure>

Once the **Kafka Producer** is connected with the input node, the input fields corresponding to the **Kafka Producer** node are displayed on the left pane.

</details>

<details>

<summary><strong>Configure Kafka Connection</strong></summary>

**Purpose:**

The purpose of configuring a **Kafka connection** is to establish a secure connection between the pipeline and the Kafka cluster. It provides the necessary broker details and authentication settings required to publish or consume messages from Kafka topics.

**Procedure:**

The below step-by-step instructions describe the procedure:&#x20;

* Select an existing **Kafka connection**, if available.
* If no connection exists, create a new Kafka connection by specifying the **Kafka Server URL** (for example, `kafka://localhost:9092`).

</details>

<details>

<summary><strong>Configure Kafka Topic</strong></summary>

**Purpose:**

The purpose of configuring a **Kafka topic** is to specify the destination topic where the pipeline will publish messages. It ensures that the processed data is sent to the correct event stream for consumption by downstream systems or applications.

**Procedure:**

You can configure a Kafka topic using one of two methods: **Create New Topic** or **Use Existing Topic**.&#x20;

**1.Create New Topic**

**Overview:**

This method creates a new Kafka topic during configuration. It is used when the required topic does not already exist in the Kafka cluster.

**Procedure:**

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

A. On the **Left Pane**, in the **Kafka Producer** section, click the **Add Kafka Producer link.**

The **Kafka Producer link 1** drop-down box is displayed.

B. On the **Kafka Producer link 1** drop-down box, click the **Down Arrow** to expand it.

The **Kafka Producer link 1** fields are displayed.

C. From the **Kafka Server** drop-down box, select the **Kafka Connection**.

{% hint style="info" %}
**Tip:** Selecting the **Kafka Connection** defines which Kafka cluster the data will be published to.
{% endhint %}

D. Enable **Create New Topic** ![](<../../../../.gitbook/assets/image (2535).png>)feature to create a **new Kafka topic** directly from the configuration screen if the required topic does not already exist.

Once the **Create New Topic** feature is enabled, the Kafka Topic Name field is displayed. &#x20;

E. In the **Kafka Topic Name** field, enter a name for the **Kafka Topic.**&#x20;

F. From the **Format Type** drop-down box, select the **required format type** choosing from **Avro, JSON,** or **PROTOBUF.** For example, AVRO.

{% hint style="info" %}
**Tip:** **Format Type** specifies how the data is serialized before being sent to Kafka (for example, Avro), ensuring the message format is compatible with Kafka consumers.

**Description for Avro, JSON, and PROTOBUF:**

* **Avro:** Avro is efficient and commonly used in Kafka and big data pipelines. It is a compact binary serialization format commonly used with Kafka and big data systems. It uses a defined schema to structure the data.
* **JSON:** JSON is easy to read and flexible, but larger in size. It is a text-based data format that represents data using key–value pairs. It is widely used for APIs and data exchange.
* **PROTOBUF:** PROTOBUF is very fast and compact, often used in high-performance systems and microservices. It is a binary serialization format developed by Google that uses predefined message schemas.
{% endhint %}

G. From the **Proto Message Type** drop-down box, select the **message type**.

{% hint style="info" %}
**Tip: Proto Message Type** defines the schema or message structure used to organize fields in the Kafka message, ensuring consistency and correct interpretation by downstream systems.
{% endhint %}

H. From the **Source Data** drop-down box, select the **source data.** For example, Aurora\_Order.

{% hint style="info" %}
**Tip: Source Data** selects the pipeline dataset from the input or transform node that will be published as messages to the Kafka topic
{% endhint %}

I. For **Avro or Protobuf**, click **Set Schema** and define the schema either manually or through a schema registry.

<figure><img src="../../../../.gitbook/assets/S (441).png" alt=""><figcaption><p>Creating New Kafka Topic</p></figcaption></figure>

**2.Use Existing Topic**

**Procedure:**

The below step-by-step instructions help you understand how to use a new Kafka topic:

**Step-by-Step instructions:**

A. On the **Left Pane**, in the **Kafka Producer** section, click the **Add Kafka Producer link.**

The **Kafka Producer link 1** drop-down box is displayed.

B. On the **Kafka Producer link 1** drop-down box, click the **Down Arrow** to expand it.

The **Kafka Producer link 1** fields are displayed.

C. From the **Kafka Server** drop-down box, select the **Kafka Connection**.

{% hint style="info" %}
**Tip:** Selecting the **Kafka Connection** defines which Kafka cluster the data will be published to.
{% endhint %}

D. Disable **Create New Topic** ![](<../../../../.gitbook/assets/image (2536).png>).

E. From the **Kafka Topic** drop-down box, select an **existing Kafka topic.**

<figure><img src="../../../../.gitbook/assets/S (442).png" alt=""><figcaption><p>Selecting an Existing Topic</p></figcaption></figure>

</details>

<details>

<summary><strong>Set Output Format</strong></summary>

**Purpose:**

The purpose of **setting the Output Format** when connecting a Kafka output node with an input node is to define **how the data will be serialized and structured before being sent to the Kafka topic**. This ensures that the published messages follow a consistent format that can be correctly interpreted by downstream Kafka consumers.

**Procedure:**

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. Choose the **Output Format** (e.g., Avro).
2. Ensure the data you are sending matches the schema format.
3. Define Avro Schema.
4. Provide an Avro schema to structure the data.

{"type":"record","name":"DFtoJSON","fields":\[{"name":"Category","type":"string"},{"name":"Product\_ID","type":"double"},{"name":"Unit\_Price","type":"double"},{"name":"Updated\_Price","type":"double"}]}

<figure><img src="../../../../.gitbook/assets/image (2537).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the  **Kaaka Output** node can be configured correctly and used during execution.

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

<figure><img src="../../../../.gitbook/assets/S (443).png" alt="" width="536"><figcaption><p>Saving ETL Job </p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Run &#x26; Preview</strong></summary>

**Purpose:**

The purpose of **Run & Preview** is to execute the pipeline and verify that the data from the input node is correctly processed and published to the Kafka topic. It helps validate the configuration and ensures that the output messages are generated as expected before finalizing the setup.

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step instructions:**

1. On the **Top Toolbar,** click **Preview** **Step** button to see how the data correctly processed and published to the Kafka topic.

The Preview is displayed.

2. On the **Top Toolbar,** click the **Run** button to execute the pipeline.

The Kafka Producer published the messages to the selected topic or create a new topic.

</details>

<details>

<summary><strong>Post Execution</strong></summary>

Once the pipeline runs successfully, check the **Kafka server** or **topic logs** to verify that the messages have been published.

</details>
{% endtab %}

{% tab title="Write NoSQL" %}
**Overview**

A **Write NoSQL** node can be used with an **input node** when the pipeline needs to store incoming or processed data in a **NoSQL database** such as MongoDB. It is typically used when the data from the input node is in a structured or semi-structured format and needs to be persisted in a scalable, schema-flexible NoSQL data store.

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

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Add Input Node</strong></summary>

**Overview:**

As part of adding the **Input Node**, you need to drag it from the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] and then place it on the in the **Main Workspace**. Once placed, the input fields corresponding to the selected node are displayed on the left pane.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

,The  [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] is displayed.&#x20;

3. From the  [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1], select the **Input Node** (For example, Database Input), and drag it onto the **Main Workspace.**&#x20;

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
{% endtab %}

{% tab title="Put API" %}
**Overview**

The **Put API Output node** can be connected to an **input node** when the pipeline needs to **send incoming or processed data to an external or internal system through a REST API using the PUT method**. It is typically used when the pipeline must update resources or push data to another application or service.

This node supports sending **JSON data through HTTP PUT requests**, with capabilities for **dynamic field mapping, authentication, and support for multiple payload formats**.

**Key Concepts:**

<details>

<summary><strong>How Put API Output node works with an input node</strong></summary>

* The **input node** retrieves data from the configured source (such as a database, file, API, or event stream).
* The data flows through the pipeline and may optionally pass through **transform nodes** if any modifications or formatting are required.
* The **Put API Output Node** formats the incoming data according to the API request structure.
* The node then sends the data as a **PUT request** to the configured API endpoint.

In simple terms, the input node supplies the data and the Put API node sends that data to another system through an API call.

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The Put API Output Node can be connected to input nodes that produce **structured datasets**.

**Applicable input nodes include:**

* **Database Input**
* **File Input**
* **API Input**
* **Kafka Topic (Event Input)**

</details>

<details>

<summary><strong>Applicable Transform nodes (Optional)</strong></summary>

Transform nodes can be used between the input node and the Put API node when the data must be prepared before sending it to the API.

Applicable transform nodes include:

* Mapping / Data Transform
* Filter
* Join
* Aggregation
* EDA Transform

</details>

<details>

<summary><strong>Non-applicable nodes</strong></summary>

The **Put API Output Node** cannot be connected directly to nodes that **do not produce data records**.

**Non-applicable nodes include:**

* **API Schema Node**
* **Execution Settings**
* **Parameters**
* Any **utility or control nodes** that do not output datasets

</details>

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Connect Put API Output Node to Input Node/Transform Node</strong></summary>

**Purpose:**

The purpose of connecting a **Put API Output Node** to an **Input Node** is to send the data retrieved by the input node to an external or internal system through an HTTP PUT API request. This enables the pipeline to update or transmit data to another application or service via an API endpoint.

**Procedure:**

As part of connecting the **Put API Output Node** with the input node, you need to first drag it from the [<mark style="color:blue;">**Output Node Palette**</mark>](#user-content-fn-2)[^2] on to the **Mainwork space**, and then connect it with the input node.

> <mark style="color:red;">**Note:**</mark> Based on requirement, you can add the necessary transform node in between **input node** and **Write to NoSQL node.**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Top Toolbar**, click the **Output Nodes** menu item.

The [<mark style="color:blue;">**Output Node Palette**</mark>](#user-content-fn-2)[^2] is dispalette is displayed.

2. From the [<mark style="color:blue;">**Output Node Palette**</mark>](#user-content-fn-2)[^2]<mark style="color:blue;">**,**</mark> drag the **Put API Output Node** on to the **Main Workspace**, and then connect it to the input node.&#x20;

<figure><img src="../../../../.gitbook/assets/S (449).png" alt=""><figcaption><p>Connetinging Put API Node to Input Node</p></figcaption></figure>

Once the **Put API Output Node** is connected with the input node, the Put API section is displayed on the left pane.

</details>

<details>

<summary><strong>Select Output Type and API Connection</strong></summary>

**Purpose:**

* **Output Type** – Selecting the output type defines the **format or structure of the data** that will be sent in the API request. It ensures that the data from the input node is properly formatted before being transmitted to the API endpoint.
* **API Connection** – Selecting the API connection specifies the **API endpoint and authentication details** required to send the request. It establishes the connection between the pipeline and the target system where the data will be delivered.

**Procedure:**

As part of selecting the output type, you can choose from either Webhook or API Write. Once selected, the Select drop-down box is displayed. From this Select drop-down box, you can select the API connection.

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Left Pane**, in the **Put API** section, click **Add**.

<figure><img src="../../../../.gitbook/assets/S (450).png" alt="" width="505"><figcaption><p>Add Link</p></figcaption></figure>

The Put API Collapsible Panel is displayed.

2. Expand the **Put API Collapsible Panel**, and then select the **Output Type** choosing from **Webhook** or **API Write**. For example, API Write.

{% hint style="info" %}
**Tip:** You can choose the **API Type** as **Webhook** for simple POST or PUT API requests, or **API Write** for advanced API requests that require headers, tokens, or additional configurations.
{% endhint %}

The Select drop-down box is displayed.

3. From the **Select** drop-down box, select an **API Connection**.

<figure><img src="../../../../.gitbook/assets/S (451).png" alt=""><figcaption><p>Selecting Output Type and API Connection</p></figcaption></figure>

</details>

<details>

<summary><strong>Configure Conditions</strong> </summary>

**Purpose:**

Configuring a **condition** allows the pipeline to send data through the API only when it meets defined criteria. This ensures that only relevant records are transmitted, avoiding unnecessary requests and improving efficiency.

**Procedure:**

The below step-by-step instructions describe the procedure:&#x20;

1. On the **Left Pane,** in the **Put API** section, click the **Add/Edit Condition** button.

The Add/Edit Filter dialogue box is displayed.

2. On the **Add/Edit Filter** dialogue box, **configure the condition** as shown in the below example image, and then click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (452).png" alt=""><figcaption><p>Configuring Condition</p></figcaption></figure>

</details>

<details>

<summary><strong>Map Fields</strong></summary>

**Purpose**

The purpose of **mapping** is to define how data fields from the pipeline are assigned to the API request payload. It allows you to control which columns from the input dataset are sent to the API and how they are structured in the request.

**Procedure**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Left Pane**, in the **Put API** section, click the **Mapper** tab.
2. Enter the **inputs** as described in the table below:

<table><thead><tr><th width="170">Field</th><th>Description</th></tr></thead><tbody><tr><td>Interval</td><td>Enter the time interval (in seconds) between consecutive API requests. This setting helps control the request rate and prevents API throttling or overload.</td></tr><tr><td>Append All Row in One Request</td><td>Enable this option to include all rows in a single API request payload. Disable it to send each row as a separate API request.</td></tr><tr><td>Search Column</td><td>Use this field to quickly locate a specific column when the dataset contains many fields</td></tr><tr><td>Mapper Column</td><td>From this, specify the API payload field name or request parameter to which the data should be mapped.</td></tr><tr><td>Column</td><td>From this, select the source column from the pipeline dataset that provides the value for the mapped API field.</td></tr></tbody></table>

<figure><img src="../../../../.gitbook/assets/S (453).png" alt="" width="512"><figcaption><p>Mapping Fields</p></figcaption></figure>

</details>

<details>

<summary><strong>Advanced Configurations</strong></summary>

**Overview**

The advanced configuration allows you to review and update the API endpoint based on the API being used, add any required headers according to the API specifications, and configure the response settings. The response configuration can be set by selecting options such as **Request Payload**, **Request Header**, **Previous Data**, or **Multiple Response**.

**Procedure**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. **Base URL:** It is displayed by default since it is defined in the API connection.
2. **End Point:** In the **End Point** field, **update or confirm** the endpoint value based on the API you are calling.

{% hint style="info" %}
**Tip:** The endpoint specifies the **API resource path** where the PUT request will be sent. The base URL is defined in the API connection.
{% endhint %}

3. **API Header:** You may need to add additional headers **depending on the API requirements.**

{% hint style="info" %}
Tip: Only add headers if the **API documentation requires them**.
{% endhint %}

4. **API Params:** The API Params are used to send **query parameters** along with the API request.&#x20;

{% hint style="info" %}
**Tip: API Params are optional** and are used only when the API requires **query parameters** to filter, identify, or modify the request. If the API endpoint works without query parameters, you can leave the **API Params** section empty.
{% endhint %}

5. **Response Config:** Select the **Response Configuration** choosing from **Request Payload, Request Header, Previous Data,** or **Multiple Response.**

{% hint style="info" %}
**Tip:** **Description of Response Config. Options**&#x20;

* **Request Payload** – Displays the data sent in the API request body. It helps verify that the correct data from the pipeline is being transmitted to the API.
* **Request Header** – Shows the HTTP headers included in the API request, such as authentication tokens, content type, or other metadata required by the API.
* **Previous Data** – Provides access to the data generated in earlier stages of the pipeline, allowing it to be referenced or used when handling the API response.
* **Multiple Response** – Handles scenarios where the API returns multiple responses or records, enabling the pipeline to process each response item appropriately.
{% endhint %}

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

<figure><img src="../../../../.gitbook/assets/S (454).png" alt="" width="531"><figcaption><p>Saving Pipeline</p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Preview Response</strong></summary>

**Purpose:**

Previewing the response allows you to check whether the API request was processed correctly and whether the returned response matches the expected output. It helps validate the API configuration and request structure before executing the pipeline fully. &#x20;

**Procedure:**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step instructions:**

1. On the **Right Pane**, click the **Preview** icon on the top of **Put API Output** Node.

<figure><img src="../../../../.gitbook/assets/S (455).png" alt=""><figcaption><p>Previewing</p></figcaption></figure>

After successful execution, the response is displayed as shown below:

<figure><img src="../../../../.gitbook/assets/S (456).png" alt=""><figcaption><p>Response Preview</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="Files to Tables" %}
**Overview**

The **Files to Tables Output node** can be used to **store pipeline data into one or more database tables by writing the output into files and then loading those files into tables**. It is typically used when large volumes of data need to be efficiently written to database tables.

**Key Concepts:**

<details>

<summary><strong>How Files to Tables Output node works with an input node</strong></summary>

* The **Input node extracts data** from the source system.
* The data is passed directly to the **Files to Tables Output node**.
* The node **creates intermediate files and loads the data into the specified database tables**.

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The **Files to Tables** Output node can be connected to **Input nodes that produce structured datasets**.

Examples include:

* **Database Input Node**
* **File Input Node (CSV, JSON, XML)**
* **API Input Node**
* **Streaming Input Node**

These nodes generate **records or tabular datasets**, which can be written to database tables.

</details>

<details>

<summary><strong>Applicable Transform nodes (Optional)</strong></summary>

It cannot be connected to input nodes that **do not produce structured data records**.

Examples include:

* Trigger or scheduling nodes
* Configuration nodes
* Control nodes used only to manage pipeline execution

Since these nodes **do not output data records**, the Files to Tables Output node cannot process them.

</details>

<details>

<summary><strong>Non-applicable Input and Transform nodes</strong></summary>

**Non-applicable** **Input Nodes:**

It cannot be connected to input nodes that **do not produce structured data records**.

Examples include:

* Trigger or scheduling nodes
* Configuration nodes
* Control nodes used only to manage pipeline execution

Since these nodes **do not output data records**, the Files to Tables Output node cannot process them.

**Non-applicable Transform Nodes:**

Transform nodes that **do not produce tabular output** cannot be connected.

Examples include:

* Control or validation-only transforms
* Transforms that produce only metadata or execution status

These do not generate **data records suitable for table loading**.

</details>

**Procedure**

> <mark style="color:red;">**Note:**</mark> In this procedure, **UCM File Loader** input node is used as an example to demonstrate how the **Files to Tables** output node works. However, the same process applies when using the **Files to Tables Output Node** with other input types, Database Input Node, File Input Node (CSV, JSON, XML), and API Input Node.

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Add input Node</strong></summary>

**Overview:**

As part of the adding the input node (Oracle UCM File Loader), you need to first drag it from the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] and then place it on the in the **Main Workspace**. Once placed, the **Oracle UCM File Loader** and **Select Process Table** sections are displayed on the left pane.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

<figure><img src="../../../../.gitbook/assets/S.png" alt="" width="467"><figcaption><p>Create Delta Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

<figure><img src="../../../../.gitbook/assets/S (1).png" alt="" width="460"><figcaption><p>Input Menu </p></figcaption></figure>

The [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] is displayed. See the image below.

3. From the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1], select **UCM File Loader,** and then drag it onto the **Main Workspace**.

<figure><img src="../../../../.gitbook/assets/S (59).png" alt="" width="511"><figcaption><p>Selecting UCM File Loader Node</p></figcaption></figure>

The **Oracle UCM File Loader** and **Select Process Table** sections are displayed on the Left Pane.

</details>

<details>

<summary><strong>Configure input Node Settings</strong></summary>

**Purpose:**

Configuring the **UCM File Loader** identifies the source files, storage location, and associated tables, while the **Files to Tables Output node** uses that information to load the file data into the appropriate database tables.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

* On the **Left Menu**, in the **UCM** **File Loader** section, select the **Connection, File Storage Connection, File Storage Folder/Bucket, UCM Process,** and **Process Table.**&#x20;

Refer to the below table for the description of these settings:

<table><thead><tr><th width="230" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Connection</td><td valign="top">Selecting the <strong>Connection</strong> tells the pipeline <strong>which Oracle UCM environment to connect to</strong>.</td></tr><tr><td valign="top">File Storage Connection</td><td valign="top">Selecting the <strong>File Storage Connection</strong> tells the pipeline <strong>which storage system to access for retrieving the files</strong>.</td></tr><tr><td valign="top">File Storage Folder/Bucket</td><td valign="top">Selecting the <strong>File Storage Folder/Bucket</strong> narrows down the storage location to a <strong>specific directory or bucket containing the required files</strong>.</td></tr><tr><td valign="top">UCM Process</td><td valign="top">Selecting the <strong>UCM Process</strong> tells the pipeline <strong>which process definition should be used to interpret and load the file data</strong>.</td></tr><tr><td valign="top">Process Table</td><td valign="top">Selecting the <strong>Process Tables</strong> makes the pipeline to use only the <strong>selected tables.</strong></td></tr></tbody></table>

<figure><img src="../../../../.gitbook/assets/S (457).png" alt="" width="512"><figcaption><p>Configuring Input Node Settings</p></figcaption></figure>

</details>

<details>

<summary><strong>Connect Files to Tables Output Node to input Node</strong></summary>

**Purpose:**&#x20;

The purpose of connecting the **Files to Tables Output node** to an **input node** (In this example, it is  UCM File Loader) is to **load data from files stored in UCM into database tables in a structured manner**.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1.  On the **Top Toolbar**, click the **Output** menu item.

    The [<mark style="color:blue;">**Output Node Palette**</mark>](#user-content-fn-2)[^2] is dispalette is displayed.
2. From the [<mark style="color:blue;">**Output Node Palette**</mark>](#user-content-fn-2)[^2]<mark style="color:blue;">**,**</mark> drag the **Files to Tables** output node on to the **Main Workspace,** and then connect it to the **input or transform node**.

<figure><img src="../../../../.gitbook/assets/S (458).png" alt=""><figcaption><p>Connecting Nodes</p></figcaption></figure>

Once connected, the **Files to Tables** section is displayed on the left pane.

</details>

<details>

<summary><strong>Configure  Files to Tables Output Node Settings</strong></summary>

**Purpose:**

Configuring the **Files to Tables Output node** settings defines how the data received from the input node is written into database tables through files. These settings specify the **file storage location, file format, database connection**, and the **mapping between files and tables**, ensuring that the pipeline loads the data correctly.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Left Menu**, in the **Files to Tables** section, select the **File Storage Connection, File Storage Connection, File Extension,** and **Database Connection.**&#x20;

Refer to the below table for the description of these fields:

<table><thead><tr><th width="230" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Storage Connection</td><td valign="top">Selecting the <strong>Connection</strong> tells the pipeline <strong>where to read or create the files used for loading data into tables.</strong></td></tr><tr><td valign="top">File Storage Folder/Bucket</td><td valign="top">Selecting the <strong>File Storage Folder/Bucket</strong> defines the specific folder or bucket in the storage system where the files are stored or staged.</td></tr><tr><td valign="top">File Extension</td><td valign="top">The selected <strong>File Extension</strong> is displayed by default.</td></tr><tr><td valign="top">Database Connection</td><td valign="top">Selecting the <strong>Database Connection</strong> defines the target database where the data will be loaded.</td></tr></tbody></table>

2. In the **File Name Pattern to Table Mapping s**ection, click the Add  ![](<../../../../.gitbook/assets/image (2539).png>)icon.

The **File Name Pattern** and **Table fields** are displayed.

3. In the **File Name Pattern** and **Table fields**, enter the **File Name Pattern** and **Table.**

{% hint style="info" %}
**Tip:**&#x20;

* **File Name Pattern s**pecifies the **pattern used to identify files**.
* **Table** specifies the **database table where the file data should be loaded**.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (459).png" alt="" width="518"><figcaption><p>Configuring Files Tables Settings</p></figcaption></figure>

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the **Files to Tables Output node** can be configured correctly and used during execution.

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

<figure><img src="../../../../.gitbook/assets/S (460).png" alt="" width="563"><figcaption><p>Saving Pipeline</p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Run Pipeline</strong></summary>

**Purpose:**

The purpose of running the pipeline after connecting the **Files to Tables output node** is to execute the complete data loading process so that the files identified by the input node are read and their data is loaded into the corresponding database tables.

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step instructions:**

1. On the **Delta Pipelines** page, click the **Edit** icon corresponding to the saved pipeline.&#x20;

<figure><img src="../../../../.gitbook/assets/S (461).png" alt=""><figcaption><p>Run Button</p></figcaption></figure>

The Pipeline Parameters screen is displayed.

2. On the Pipeline Parameters **screen**, make the required changes, and then click the **OK button.**

<figure><img src="../../../../.gitbook/assets/S (438).png" alt=""><figcaption><p>Running Pipeline</p></figcaption></figure>

The Logs Viewer screen is displayed with **Running** status.&#x20;

</details>
{% endtab %}
{% endtabs %}

### Related Topics

* [**Configuring Input Nodes**](configuring-input-nodes.md)
* [**Applying Transform Nodes**](applying-transform-nodes.md)

[^1]: The **Input Node Palette** contains a set of input nodes, including Database Input, File Input, Query Input, API, GraphQL, SAP APP, NoSQL, and UCM File Loader.

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
