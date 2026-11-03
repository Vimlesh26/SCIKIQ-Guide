---
hidden: true
icon: chart-network
---

# Common Other Nodes

**Contents**

* [**Instructions for Using this Page**](./#instructions-for-using-this-page)
* [**Overview**](./#overview)
* [**SCIKIQ Input Nodes**](./#scikiq-input-nodes)
* [**Related Topics**](./#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]

***

## Overview

This page explains how to use the other common nodes while creating a pipeline. These other common nodes include **Join, Variable, SQL Statement, Notify, ML Model, Group,** and **Unstructured**.

***

## Other Nodes

The expandable panels below offer detailed, step-by-step instructions for configuring and using each output node.

<details>

<summary><strong>Join</strong></summary>

**Purpose:**&#x20;

The **Join Node** is used to combine datasets from two or more sources into a single unified view based on specified join conditions. It enables you to enrich and correlate data by joining tables using common fields or defined conditions.

**Types of Join Nodes:**

<table><thead><tr><th width="179">Type</th><th>Purpose</th></tr></thead><tbody><tr><td>Inner Join</td><td>Returns records that have matching values in both tables.</td></tr><tr><td>Left Join</td><td>Returns all records from the left table and matching records from the right table. If there's no match, NULLs are returned from the right.</td></tr><tr><td>Right Join</td><td>Returns all records from the right table and matching records from the left. If there's no match, NULLs are returned from the left.</td></tr><tr><td>Outer Join</td><td>Returns all records when there is a match in either left or right table.</td></tr></tbody></table>

**Procedure to use Join Node:**

The below step-by-step instructions describe the procedure:

1. **Connect Join Node to Input Nodes**

A. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click either **Create API Pipeline** or **Create Delta Pipeline**. For example, Create Delta Pipeline.

<figure><img src="../../../../.gitbook/assets/S.png" alt=""><figcaption><p>Create Delta Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

B. On the **Right Bane**, add **two input nodes**. For example, Database input nodes.

C. Now, from the **Top Toolbar** drag the **Join node** on to the **Main Workspace,** and connect it to the input nodes.

<figure><img src="/broken/files/Ec7Z2pyPRARcsTCPbgZw" alt=""><figcaption><p>Connecting Join Node</p></figcaption></figure>

The Join section is displayed on the left pane.

2. **Configure Condition**

A. On the **Left Pane**, click the **Add** **Join** button.

<figure><img src="/broken/files/hutPd189ElL3mU6helHa" alt=""><figcaption><p>Add Join Button</p></figcaption></figure>

The Join dialogue-box is displayed.

5. On the **Join** dialogue-box, from the **Join Type** dialogue-box, select the required **join type** choosing from **Inner, Left, Right,** or **Outer.**
6. From the drop-down box under **And/Or**, select the required **column**. To choose more columns, click the **Add Rule** button.
7. Click the **Save** button.

<figure><img src="/broken/files/cxp8nQzW9Iutr5macyNx" alt=""><figcaption><p>Configuring Condition</p></figcaption></figure>

3. **Select Columns**

A. On the **Left Pane**, in the **Join** section, click the **Columns** tab.

The list of columns is displayed.

B. From the **list of columns**, select the **required columns**.

<figure><img src="/broken/files/bJu0jV8r04MHZ2tPxFVW" alt=""><figcaption></figcaption></figure>













</details>

<details>

<summary><strong>Variable</strong></summary>

**Purpose:**

The **File Output node** is used to **write the final processed data from a pipeline into one or more files**. It enables you to export data in specific file formats so it can be stored, shared, archived, or consumed by external systems and users.&#x20;

The typical output formats include: **CSV, JSON, Parquet, and Avro (where supported)**.

**Applicable Input Nodes:**

The common compatible input nodes include: **Database input nodes, File input nodes, API input nodes (structured responses),** and **Kafka or streaming input nodes (after schema is defined).**

**Applicable Transform Nodes:**

The **File Output node** works with all transform nodes that produce structured or semi-structured output, such as: **Filter, Select / Rename, Join, Aggregate, Calculated or derived fields, Data type conversion, and Bulk column operations.**

**Procedure to Apply File Output Node**

**1.Add Source Nodes and Transform Node**

* On the **Right Pane**, add the **source nodes**.

> <mark style="color:red;">**Note:**</mark> Ensure that the data to be exported has already been processed using the required transformation nodes.

2.**Connect File Output Node**

A. Navigate to **Create Delta Pipeline page**.&#x20;

(SCIKIQ Connect>>SCIKIQ Delta Hub>>Create Delta Pipeline)

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * In case of **API Pipeline,** you need to navigate to **Create API Pipeline page.** (SCIKIQ Connect>>SCIKIQ Delta Hub>>Create API Pipeline)&#x20;
> * Similarly, in case of **Event Pipelines,** navigate to **Create Event Pipeline page**
>
> &#x20;     (SCIKIQ Connect>>SCIKIQ Event Hub>>Create Event Pipeline)

B. On the **Top Toolbar**, click **OutPut** menu.

The Output Node Palette is displayed.&#x20;

C. From the **Output Node Palette**, drag the **File Output Node** and place it on the **Main Work Space (Right Pane).**

D. Connect the **File Output Node** to the previous node.

<figure><img src="/broken/files/PRUYQJI12lCKAe31NBiU" alt=""><figcaption><p>Connecting File Output Node</p></figcaption></figure>

**3.Select File Storage Type, Connection, and Target Bucket**&#x20;

A. On the **Right Pane**, select the **File Output node.**

The corresponding input fields are displayed on the left pane.

B. On the **Left Pane**, select **File Output Type** drop-down box, select the **Storage Type** where the file will be written.

{% hint style="info" %}
**Tip:**  Some of the supported storage types are **Amazon S3, Google Cloud Storage (GCP),** and **FTP/SFTP.**
{% endhint %}

C. From the **Select Storage** drop-down box, select an **existing storage connection.** For  example, S3 File Storage.

D.  After selecting the S3 connection, click the **Connect** button to fetch available buckets.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * If no folders are present in the bucket, none will be displayed.
> * If folders exist, select the desired **folder path** where you want to write the file.

<figure><img src="/broken/files/Kk2YMEbPwfjQc9IxoaAF" alt=""><figcaption><p>Selecting File Type, Storage Type, and Bucket</p></figcaption></figure>

**4.Set File Path and Format**

A. On the **Select File Type** screen, scroll down to the **Root section.**

B. In the **File Name** field, enter a **name** for the file.

C. From the File Format area, select the firle format. For example, CSV.

<figure><img src="/broken/files/7BOnroCgdQJgdq5Jxjt8" alt=""><figcaption><p>Specifying File Name and Format</p></figcaption></figure>

**5.Preview Data**

* On the **Right Pane**, click the **Preview** icon on the top of **Output** node.

The file output is displayed. See the below image.

</details>

<details>

<summary><strong>SQL Statement</strong></summary>



</details>

<details>

<summary><strong>Notify</strong></summary>

**Purpose:**

The **Table Update node** is used to **update existing records in a database table** based on incoming data. When it is connected directly to an **input node**, its purpose is to apply updates to target table rows **as-is**, using key or matching columns from the input data, without performing any transformations.

**Applicable Input Nodes:**

The **Table Update node** can be connected to the input nodes that produce **structured, row-level data** including **Database Input, File Input, API Input,** and **Kafka Topic (Event input).**

**Applicable Transform Nodes** (optional, when data preparation is required):

The **Table Update node** can be connected to the transform nodes including **Mapping / Data Transform, Filter, Join, Aggregation,** and **EDA Transform.**

**Procedure to Apply Table Update Node:**

Applying the **Table Update node** involves **connecting the nodes, configuring the input node, configuring the transform nodes (optional), configuring the Table Update node, saving the ETL job,** and **previewing the output data.**

The below information describes all of these topics:

**1.Connect Nodes**

* On the **Right Pane**, place the **Input node** and **Table Update node** and then connect them.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * In general, the input node is configured first to define the data source and how data is read. Once configured, it can be connected to an output node to specify where the data is written, without needing to reconfigure the input node.
> * In case, you want to know **how to configure the input nodes**, click [Configuring Input Nodes.](/broken/pages/Qe52MzyFrHp43dWO41kf)
> * Similarly, if you want to know **how to configure the transform nodes**, click [Applying Transform Nodes](/broken/pages/hbzg9uHn194g3ivtwx4q).

<figure><img src="../../../../.gitbook/assets/S (427).png" alt=""><figcaption><p>Connecting Nodes</p></figcaption></figure>

**2.Configure Table Update Node Settings**:

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

3. **Save ETL Job**

**Procedure**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="/broken/files/YHRLkQBeqIbQWPMxhq5q" alt="" width="533"><figcaption><p>Saving ETL Job</p></figcaption></figure>

The Pipeline is saved.

3. **Preview Data**

A. On the **Right Pane**, click the **Preview** icon on the top of **Table Update** node.

The updated table is displayed.

</details>

<details>

<summary> <strong>ML Model</strong></summary>

**Purpose:**

You can use the **Merge** node when there is a need to merge one table with another table and synchronize the target table with incoming records.. You can merge the tables by choosing **Row Wise, Temp Table,** or same **Database.**

**How the Merge Node Works**

* The **input node** reads data from the source system (database, file, API, or event stream).
* The **Merge node** compares incoming records with the target table using configured **match (key) columns**.&#x20;
* Based on the comparison:
  * Matching records are **updated**
  * Non-matching records are **inserted**
  * (Optional) Records not present in the source can be **deleted or marked inactive**, depending on configuration
* The Merge node applies these changes atomically to keep the target table synchronized.

**Applicable Input Nodes**

The Merge node can be connected to any input node that produces **structured, row-level data** including **Database Input, File Input, API Input, and Kafka Topic (Event Input).**

**Applicable Transform Nodes (Optional)**

Transform nodes can be placed between the input node and the Merge node when data preparation is required: **Mapping / Data Transform, Filter, Join,Aggregation,** and **EDA Transform.**

**Non-Applicable Nodes**

The Merge node **cannot be connected directly** to nodes that do not emit structured datasets or serve only configuration purposes: **API Schema Node, Execution Settings, Parameters**, and Control or utility nodes that do not output row-level data.

**Procedure**

**1.Connect Nodes**

* On the **Right Pane**, place the **Input node** and **Table Update node** and then connect them.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * In general, the input node is configured first to define the data source and how data is read. Once configured, it can be connected to an output node to specify where the data is written, without needing to reconfigure the input node.
> * In case, you want to know **how to configure the input nodes**, click [Configuring Input Nodes.](/broken/pages/Qe52MzyFrHp43dWO41kf)
> * Similarly, if you want to know **how to configure the transform nodes**, click [Applying Transform Nodes](/broken/pages/hbzg9uHn194g3ivtwx4q)

<figure><img src="/broken/files/vs6tObH2sMssMw3z1Nw0" alt=""><figcaption><p>Connecting Nodes</p></figcaption></figure>

Once the Merge is connected with the input node, the input fields corresponding to the Merge node are displayed on the left pane.

**2.Configure Merge Node Settings**:

**Overview:**

As part of configuring the ...&#x20;

**Procedure:**

The below mentioned step-by-step instructions describe the process:

**Step-by-Step Instructions**

**A. Select Database Type and Connection**

a. On the **Right Pane**, select the Merge node if it is already not selected.

The input fields corresponding to the Merge node are displayed on the left pane.

b. On the  **Left Pane**, select the **Database Type** and a pre-configured **Connection**.&#x20;

**B. Select Target Table and Merge Type**

a. From the **Target** drop-down box, select the **Target Table**.

{% hint style="info" %}
**Tip:** The **Target Table** refers to the **destination database table** where the merge operation is applied.
{% endhint %}

b. From the **Merge Type** drop-down box, select the required merge type choosing from **Row Wise, Temp Table,** or same **Database.**

{% hint style="info" %}
**Tip: Description of Merge Options**

* **Row Wise** – Merges records one by one by matching key columns and inserting or updating rows accordingly.
* **Temp Table** – Loads source data into a temporary table first and then merges it with the target table for better performance on large datasets.
* **Same Database** – Performs the merge directly within the same database when both source and target tables are located there, ensuring faster execution.
{% endhint %}

e. Select the **Join** tab, if it is already not selected by default, and then click the **Add** ![](<../../../../.gitbook/assets/image (2533).png>)icon corresponding to it.

The Source and Target drop-down boxes are displayed.

</details>

<details>

<summary><strong>Group</strong></summary>



</details>

<details>

<summary><strong>Unstructured</strong></summary>



</details>

## Related Topics

* [Configuring Input Nodes](/broken/pages/Qe52MzyFrHp43dWO41kf)
* [Configuring Output Nodes](/broken/pages/BOHoiMbsoFJCedoWAASx)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
