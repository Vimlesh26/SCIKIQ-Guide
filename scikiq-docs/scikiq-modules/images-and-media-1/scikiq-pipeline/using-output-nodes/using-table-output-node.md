# Using Table Output Node

This page explains how to use the **Table Output** node with an input/transform node. You can use the **able Output** node to **write the final processed data into a target table** in a database or data platform. It acts as the **last step in a pipeline**, persisting data after it has been read, transformed, validated, or enriched.

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

Connecting the  **Table Output** node to an input node involves a sequence of steps. These steps include [Connect Table Output Node](using-table-output-node.md#connect-table-output-node), [Configure Input Node,](using-table-output-node.md#configure-input-node) [Configure Transform Node (Optional),](using-table-output-node.md#configure-transform-node-optional) [Configure Table Output Node,](using-table-output-node.md#configure-table-output-node) [Save ETL Job](using-table-output-node.md#save-etl-job) and [Preview Data.](using-table-output-node.md#preview-data)

***

## Procedure

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

## Related Topics

* [Configuring Input Nodes](/broken/pages/Qe52MzyFrHp43dWO41kf)
* [Configuring Transform Nodes](/broken/pages/hbzg9uHn194g3ivtwx4q)
