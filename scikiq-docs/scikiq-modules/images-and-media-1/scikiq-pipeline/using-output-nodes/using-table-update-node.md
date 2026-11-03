# Using Table Update Node

This page explains how to use the **Table Update** node with an input/transform node. The A **Table Update Output Node** can be connected with an **Input Node** when the data retrieved by the Input Node is used to **update existing records in a database table**.

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

Connecting the  **Table Update** node to an input node involves a sequence of steps. These steps include [Connect Table Output Node](using-table-update-node.md#connect-table-output-node), [Configure Table Update Node Settings,](using-table-update-node.md#configure-table-update-node-settings) [Save ETL Job](using-table-update-node.md#save-etl-job) and [Preview Data](using-table-update-node.md#preview-data).

***

## Procedure

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

## Related Topics

* [Configuring Input Nodes](/broken/pages/Qe52MzyFrHp43dWO41kf)
* [Configuring Transform Nodes](/broken/pages/hbzg9uHn194g3ivtwx4q)
