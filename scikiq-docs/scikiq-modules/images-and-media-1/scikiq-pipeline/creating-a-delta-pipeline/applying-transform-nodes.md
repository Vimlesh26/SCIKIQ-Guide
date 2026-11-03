---
icon: circle-share-nodes
---

# Applying Transform Nodes

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

Transformation nodes in SCIKIQ Pipelines are used to prepare and refine data after it is loaded and before it moves to the next step. They allow you to adjust the data so it is clean, consistent, and ready for use in reports, analytics, or other systems.

By using transformation nodes, the pipeline becomes more reliable and easier to manage. They ensure consistent data processing across multiple nodes and tables, reduce the need for manual corrections, and help deliver accurate, usable data to the final destination.

***

### Applying Transform Nodes

SCIKIQ supports configuring the below mentioned transform nodes:

{% tabs %}
{% tab title="Filter By" %}
**Overview**

The **Filter By** transform node **can be used with most types of input nodes,** because filtering is a general operation that works on tabular or structured data. In simple terms, it works with any node that outputs rows and columns.&#x20;

**Applicable input nodes:**

Some of the input nodes that can be used with **Filter By** transform node are **File input (CSV, Excel), Database input, API input** (that returns structured results)**,** and **GraphQL input,** etc.&#x20;

**Non-applicable Nodes:**

If an input node produces data that is **unstructured or not row-based**, the **Filter By** node may not be directly applicable.&#x20;

{% hint style="info" %}
**Tip:** The **Filter By** transform node can be applied to input nodes that produce unstructured or non–row-based data by first converting the data into a tabular format (for example, transforming JSON into a table).
{% endhint %}

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

> <mark style="color:red;">**Note:**</mark> In this procedure, the **File Input** node is used as an example to demonstrate how the **Filter By** transform node works. However, the same process applies when using the Filter By node with other input types, such as Database Input (CSV or Excel files), Database Input, API Input that returns structured data, and GraphQL Input nodes.

<details>

<summary><strong>Add Input Node</strong> </summary>

**Overview:**

As part of adding the **Input Node**, you need to drag it from the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] and then place it on the in the **Main Workspace**. Once placed, the input fields corresponding to the selected node are displayed on the left pane.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

,The  [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] is displayed.&#x20;

3. From the  [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1], select the **Input Node** (For example, File Input), and drag it onto the **Main Workspace.**&#x20;

<figure><img src="../../../../.gitbook/assets/image (2503).png" alt=""><figcaption></figcaption></figure>

The Select File Type and Scheme Properties are displayed in the left pane Left Pane.&#x20;

</details>

<details>

<summary><strong>Select File Type and Columns</strong></summary>

**Purpose:**

Selecting the required columns determines which fields are extracted from the chosen  source. By selecting only the necessary columns, you ensure that the pipeline retrieves relevant data, reduces unnecessary data processing, and improves overall performance.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Left Pane,** from the **Select File** drop-down box, select either **File Upload** or **File Storage.** For example,  File Uploa&#x64;**.**&#x20;
2. From the **Dataset** drop-down box, select the required **dataset.**

<figure><img src="../../../../.gitbook/assets/S (320).png" alt=""><figcaption><p>Selecting File Type and File</p></figcaption></figure>

{% hint style="info" %}
**Tip:**&#x20;

* The **File Upload** type enables you to upload the files such as **CSV, XLS**, etc. directly from your local system.&#x20;
* The **File Storage** type allows you to connect to external storage locations such as **Hadoop (HDFS), SFTP**, and **Cloud-based Storage services**.&#x20;
{% endhint %}

3\. In the **Schema properties** section, select the required **columns**.

<figure><img src="../../../../.gitbook/assets/S (321).png" alt=""><figcaption><p>Selecting Columns</p></figcaption></figure>

{% hint style="info" %}
**Tip:** You can select a **single column, multiple columns,** or **all columns** based on your requirement. Selecting the **Select All** checkbox allows you to select all columns at once. See the **ticked checkbox** in the image below.
{% endhint %}

</details>

<details>

<summary><strong>Connect Input Node with Filter By Node</strong></summary>

**Overview:**

As part of the connecting the input node with the **Filter By** node, you need to first drag the **Filter By** node from the **Transform Node Palette**, and then place it on the **Main Workspace**. Once done, you can connect the input node on the Main Workspace with the **Filter By** node.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Toolbar**, click the **Transform Nodes** menu item.

The [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] is displayed.

2. From the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2], drag the **Filter By** node, and drop it onto the **Main Workspace.**

<figure><img src="../../../../.gitbook/assets/S (322).png" alt="" width="529"><figcaption><p>Selecting the Filter By Transform Node</p></figcaption></figure>

3. Now, drag the **right side** **edge** of the **input node** and connect it to **Filter By** node as shown in the below image.

<figure><img src="../../../../.gitbook/assets/S (323).png" alt="" width="530"><figcaption><p>Connecting Nodes</p></figcaption></figure>

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the **Filter By** node can be configured correctly and used during execution.

**Procedure**

The information below outlines the step-by-step instructions for completing this task:

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

<details>

<summary><strong>Configure Filter Settings</strong></summary>

**Overview**

After saving the ETL job, you need to click the **Edit** icon on the **Delta Pipelines** page to view the connected nodes. As part of the configuring the **Filter By** transform node settings, you need to define the **logical relationship between multiple conditions** by selecting either **AND** or **OR** and then define the **precise data filtering criteria.** Based on the requirement, you can use parameters and variables as well.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Delta Pipelines** page, click the **Edit** icon corresponding to the saved pipeline.&#x20;

<figure><img src="../../../../.gitbook/assets/S (324).png" alt=""><figcaption><p>Delta Pipelines Page - Clicking Edit Icon</p></figcaption></figure>

The connected nodes on the **right pane** and the Add/Edit Filter button on the **left pane** are displayed.

2. Now, on the **Left Pane,** click the **Add/Edit Filter** button.&#x20;

<figure><img src="../../../../.gitbook/assets/S (325).png" alt="" width="514"><figcaption><p>Add/Edit Filter Button</p></figcaption></figure>

The **Add/Edit Filter** dialogue-box is displayed.

3. On the **Add/Edit Filter** dialogue box (See the image below):

<figure><img src="../../../../.gitbook/assets/S (8).png" alt="" width="563"><figcaption><p>Configuring Filters</p></figcaption></figure>

A. **Select** **Add or Edit**&#x20;

{% hint style="info" %}
**Tip:** The purpose of using **AND** or **OR** is to define the logical relationship between multiple conditions.
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

C. **To add a new condition line** (For example, Amount less than 10000)&#x20;

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

<summary><strong>Preview Data</strong></summary>

**Overview:**

**Preview** helps you confirm that the data output matches your filter conditions and other selected settings.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Right Pane**, click the **Preview** icon on the top of **Filter By** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (326).png" alt="" width="535"><figcaption><p>Preview Icon</p></figcaption></figure>

The data is displayed on the Preview tab. See the example image below:

<figure><img src="../../../../.gitbook/assets/S (327).png" alt="" width="563"><figcaption><p>Data Preview</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="Order By" %}
**Overview**

The **Order By** transform node is used whenever you need the data to be returned in a specific, deterministic order before further processing.

**Applicable input nodes:**&#x20;

The **Order By** transform node can be used **directly with structured, row-based inputs.** File inputs (CSV, Excel), Database inputs, API inputs that return structured tabular data, and GraphQL inputs can all be ordered because they present rows and columns the transformer can sort.

**Non-applicable nodes:**&#x20;

The **Order By** transform node is not **directly applicable to truly unstructured data** such as images, raw logs, and blobs, etc.

{% hint style="info" %}
**Tip:** If you want to apply the **Order By** node to unstructured or non-tabular data, you must first parse/convert that data into a tabular form (columns/rows).
{% endhint %}

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

> <mark style="color:red;">**Note:**</mark> In this procedure, the **File Input** node is used as an example to demonstrate how the **Order By** transform node works. However, the same process applies when using the **Order By** transform node with other input types, such as Database Input (CSV or Excel files), Database Input, API Input that returns structured data, and GraphQL Input nodes.

<details>

<summary><strong>Add Input Node</strong> </summary>

**Overview:**

As part of adding the **Input Node**, you need to drag it from the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] and then place it on the in the **Main Workspace**. Once placed, the input fields corresponding to the selected node are displayed on the left pane.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

,The [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] is displayed.&#x20;

3. From the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1], select the **Input Node** (For example, File Input), and drag it onto the **Main Workspace.**&#x20;

<figure><img src="../../../../.gitbook/assets/S (319).png" alt="" width="508"><figcaption><p>Adding Input Node</p></figcaption></figure>

The Select File Type and Scheme Properties are displayed in the left pane Left Pane.&#x20;

</details>

<details>

<summary><strong>Select File Type and Columns</strong></summary>

**Purpose:**

Selecting the required columns determines which fields are extracted from the chosen  source. By selecting only the necessary columns, you ensure that the pipeline retrieves relevant data, reduces unnecessary data processing, and improves overall performance.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Left Pane,** from the **Select File** drop-down box, select either **File Upload** or **File Storage.** For example,  File Uploa&#x64;**.**&#x20;
2. From the **Dataset** drop-down box, select the required **dataset.**

<figure><img src="../../../../.gitbook/assets/S (320).png" alt=""><figcaption><p>Selecting File Type and File</p></figcaption></figure>

{% hint style="info" %}
**Tip:**&#x20;

* The **File Upload** type enables you to upload the files such as **CSV, XLS**, etc. directly from your local system.&#x20;
* The **File Storage** type allows you to connect to external storage locations such as **Hadoop (HDFS), SFTP**, and **Cloud-based Storage services**.&#x20;
{% endhint %}

3\. In the **Schema properties** section, select the required **columns**.

<figure><img src="../../../../.gitbook/assets/S (321).png" alt=""><figcaption><p>Selecting Columns</p></figcaption></figure>

{% hint style="info" %}
**Tip:** You can select a **single column, multiple columns,** or **all columns** based on your requirement. Selecting the **Select All** checkbox allows you to select all columns at once. See the **ticked checkbox** in the image below.
{% endhint %}

</details>

<details>

<summary><strong>Connect Input Node with  Order By Node</strong></summary>

**Overview:**

As part of connecting the input with Order By node, you need to first drag the **Order By** node from the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2], and then place it on the **Main Workspace**. Once done, you can connect the input node with the **Order By** node.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Toolbar**, click the **Transform Nodes** menu item.&#x20;

The [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] is displayed.

2. From the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] palette, drag the **Order By** node, and drop it onto the **Main Workspace.**

<figure><img src="../../../../.gitbook/assets/S (328).png" alt="" width="553"><figcaption><p>Selecting Order By Node</p></figcaption></figure>

2. Now, drag the **right side** **edge** of the **input node** and connect it to the **left side edge** of **Limit By** node as shown in the below image.

<figure><img src="../../../../.gitbook/assets/S (329).png" alt="" width="511"><figcaption><p>Connecting Nodes</p></figcaption></figure>

2. Save the **ETL** job. Refer to the next panel to know how to save the ETL job.

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the **Order By** node can be configured correctly and used during execution.

**Procedure**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (330).png" alt="" width="563"><figcaption><p>Saving Data Pipeline</p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Configure Order By Settings</strong></summary>

**Purpose:**

The **Order By** transform node allows you to define the sequence in which records are arranged in a dataset. By specifying one or more columns and the sort direction, you can control how data is passed to the next step in the pipeline

**Procedure:**

After saving the ETL job, you need to first click the **Edit** icon on the **Delta Pipelines** page to view the nodes you have connected. As part of configuring the **Order By** transform node settings, you can define the order of a required column choosing from the [<mark style="color:blue;">ASC</mark>](#user-content-fn-3)[^3] and [<mark style="color:blue;">DESC</mark>](#user-content-fn-4)[^4] options. You can also apply the **Order By** transform node to multiple columns.

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. On the **Delta Pipelines** page, click the **Edit** icon corresponding to the saved pipeline.&#x20;

<figure><img src="../../../../.gitbook/assets/S (331).png" alt=""><figcaption><p>Delta Pipelines Page - Clicking Edit Icon</p></figcaption></figure>

The connected nodes on the **right pane** and **Order By** section on the **left pane** are displayed. See the below **Specifying** Order image.

2. In the **Order By** section, click the **Plus** ![](<../../../../.gitbook/assets/image (2510).png>) icon.&#x20;

The Column Name and Order by fields are displayed.

{% hint style="info" %}
**Tip:** If you want to remove the Order By row fields, click the **Delete** icon.

<img src="../../../../.gitbook/assets/S (332).png" alt="" data-size="original">
{% endhint %}

3. From the **Column Name** drop-down box, select the required **column**. For example, TOTAL\_AMOUNT.&#x20;
4. From the **Order By** drop-down box, select **ASC** or **DESC**.

{% hint style="info" %}
Tip:

* **ASC** refers to Ascending Order and **DESC** refers to Descending Order.
* Based on your requirement, you can select one or more columns to define the sort order.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (333).png" alt="" width="524"><figcaption><p>Specifying Sort Ordering</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="Limit By" %}
**Overview**

The **Limit By t**ransform node is used when you want to **restrict the number of records** that move forward from an input node to the next step in the pipeline. It controls how much data is processed, not which data is selected.

**Applicable input nodes:**&#x20;

The **Limit By** transform node can be used with any input node that produces structured, row-based data, including File Input (CSV, Excel, Parquet, etc.), Database Input, API Input (that returns structured results), GraphQL Input, and any input node that outputs data in rows and columns.

**Non-applicable nodes:**&#x20;

The **Limit By** transform node may **not be effective or applicable** when the input produces **unstructured data** (such as raw text, images, or binary files).&#x20;

{% hint style="info" %}
**Tip:** If the input node returns unstructured or non-tabular data, first convert the data into a tabular format. Once the data is in table form, apply the **Limit By** transform node.
{% endhint %}

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

> <mark style="color:red;">**Note:**</mark> In this procedure, the **File Input** node is used as an example to demonstrate how the **Limit By** transform node works. However, the same process applies when using the **Limit By** transform node with other input types, such as File Input (CSV or Excel files), Database Input, API Input that returns structured data, and GraphQL Input nodes.

<details>

<summary><strong>Add Input Node</strong> </summary>

**Overview:**

As part of adding the **Input Node**, you need to drag it from the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] and then place it on the in the **Main Workspace**. Once placed, the input fields corresponding to the selected node are displayed on the left pane.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

,The [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] is displayed.&#x20;

3. From the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1], select the **Input Node** (For example, File Input), and drag it onto the **Main Workspace.**&#x20;

<figure><img src="../../../../.gitbook/assets/S (319).png" alt="" width="508"><figcaption><p>Adding Input Node</p></figcaption></figure>

The Select File Type and Scheme Properties are displayed in the left pane Left Pane.&#x20;

</details>

<details>

<summary><strong>Select File Type and Columns</strong></summary>

**Purpose:**

Selecting the required columns determines which fields are extracted from the chosen  source. By selecting only the necessary columns, you ensure that the pipeline retrieves relevant data, reduces unnecessary data processing, and improves overall performance.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Left Pane,** from the **Select File** drop-down box, select either **File Upload** or **File Storage.** For example,  File Uploa&#x64;**.**&#x20;
2. From the **Dataset** drop-down box, select the required **dataset.**

<figure><img src="../../../../.gitbook/assets/S (320).png" alt=""><figcaption><p>Selecting File Type and File</p></figcaption></figure>

{% hint style="info" %}
**Tip:**&#x20;

* The **File Upload** type enables you to upload the files such as **CSV, XLS**, etc. directly from your local system.&#x20;
* The **File Storage** type allows you to connect to external storage locations such as **Hadoop (HDFS), SFTP**, and **Cloud-based Storage services**.&#x20;
{% endhint %}

3\. In the **Schema properties** section, select the required **columns**.

<figure><img src="../../../../.gitbook/assets/S (321).png" alt=""><figcaption><p>Selecting Columns</p></figcaption></figure>

{% hint style="info" %}
**Tip:** You can select a **single column, multiple columns,** or **all columns** based on your requirement. Selecting the **Select All** checkbox allows you to select all columns at once. See the **ticked checkbox** in the image below.
{% endhint %}

</details>

<details>

<summary><strong>Connect Input Node with  Limit By Node</strong></summary>

**Overview:**

As part of connecting the input and Limit By nodes, you need to first drag the **Limit By** node from the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2], and then place it on the **Main Workspace**. Once done, you can connect the input node with the **Limit By** node.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Toolbar**, click the **Transform Nodes** menu item.&#x20;

The [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] is displayed.

2. From the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] palette, drag the **Limit By** node, and drop it onto the **Main Workspace.**

<figure><img src="../../../../.gitbook/assets/S (334).png" alt="" width="491"><figcaption><p>Selecting the Limit By Transform Node</p></figcaption></figure>

3. Now, drag the **right side** **edge** of the **input node** and connect it to the **left side edge** of **Limit By** node as shown in the below image.

<figure><img src="../../../../.gitbook/assets/S (335).png" alt="" width="509"><figcaption><p>Connecting Nodes</p></figcaption></figure>

4. Save the **ETL** job. Refer to the next panel to know how to save the ETL job.

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the **Limit By** node can be configured correctly and used during execution.

**Procedure**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (14).png" alt="" width="563"><figcaption></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Configure Limit By Settings</strong></summary>

**Purpose:**

You can use the **Limit By** transform node to define an **upper limit** on the number of records retrieved from a dataset. This functionality is commonly used to optimize performance, support testing activities, and manage data processing volume before transformations are applied.

**Procedure:**

After saving the ETL job, you need to first click the **Edit** icon on the **Delta Pipelines** page to view the nodes you have connected. As part of configuring the **Limit By** transform node settings, you can select either the **system-defined upper limit** or the **custom** option based on your requirement. Once configured, this setting determines the maximum number of records retrieved by the pipeline.

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. On the **Delta Pipelines** page, click the **Edit** icon corresponding to the saved pipeline. Here it is Limit By Test.

<figure><img src="../../../../.gitbook/assets/S (331).png" alt=""><figcaption><p>Delta Pipelines Page - Clicking Edit Icon</p></figcaption></figure>

The connected nodes on the **right pane** and **Limit By** section on the **left pane** are displayed. See the below **Specifying Record Limit** image.

2. In the **Limit By** section, select either **From Start** or **From End**.

{% hint style="info" %}
**Tip:**&#x20;

* **From Start** limits the number of records beginning from the **top of the dataset** (the first records returned by the input node).
* **From End** limits the number of records taken from the **bottom of the dataset** (the last records returned by the input node).
{% endhint %}

3. Specify the limit choosing from **Limit By 10, Limit By 500, Limit By 1000, Limit By 2000,** or **Custom**.&#x20;

{% hint style="info" %}
Tip: If you wish to define a **custom** limit, then select the **Custom** option, and specify the limit, which you prefer. A **custom limit** is a **user-defined restriction on the number of records retrieved from a dataset**, rather than using a system-defined default limit.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (336).png" alt="" width="510"><figcaption><p>Specifying Record Limit</p></figcaption></figure>

</details>

<details>

<summary><strong>Preview Data</strong></summary>

**Overview:**

**Preview** allows you to verify that the data output matches the defined record limit. It shows how many records are passed to the next step after applying the Limit By settings. This helps ensure that only the intended number of records is processed before running the pipeline.

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Right Pane**, click the **Preview** icon on the top of **Limit By** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (337).png" alt="" width="508"><figcaption><p>Preview Icon</p></figcaption></figure>

The records are displayed as per the specified limit on the Preview tab. See the example image below:

<figure><img src="../../../../.gitbook/assets/S (338).png" alt=""><figcaption><p>Data Preview</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="Group By" %}
**Overview**

The **Group By** transform node is used when you want to **summarize or aggregate data** coming from an input node based on one or more common fields. Instead of working with individual records, **Group By** helps you analyze data at a higher level by combining rows that share the same values.

**Applicable input nodes:**&#x20;

The  **Group By** transform node can be used **directly with structured, row-based inputs.** Some of these inputs include - **File inputs (CSV, Excel), Database inputs, API inputs** (return structured tabular data), and **GraphQL inputs**.

**Non-applicable nodes:**&#x20;

The  **Group By** transform node is not **directly applicable to truly unstructured data** such as raw text, images, or binary files, etc.

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

> <mark style="color:red;">**Note:**</mark> In this procedure, the **Database Input** node is used as an example to demonstrate how the  **Group By** transform node works. However, the same process applies when using the  **Group By** transform node with other input types, such as File Input (CSV or Excel files), Database Input, API Input that returns structured data, and GraphQL Input nodes.

<details>

<summary><strong>Add Input Node</strong> </summary>

**Overview:**

As part of adding the **Input Node**, you need to drag it from the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] and then place it on the in the **Main Workspace**. Once placed, the input fields corresponding to the input node are displayed on the left pane.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

,The [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] is displayed.&#x20;

3. From the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1], select the **Input Node** (For example, Database Input), and drag it onto the **Main Workspace.**&#x20;

<figure><img src="../../../../.gitbook/assets/S (339).png" alt="" width="507"><figcaption><p>Adding Input Node</p></figcaption></figure>

The Database Type and Scheme Properties sections are displayed in the left pane.&#x20;

</details>

<details>

<summary><strong>Select Columns</strong></summary>

**Purpose:**

Selecting the required columns determines which fields are extracted from the chosen  source. By selecting only the necessary columns, you ensure that the pipeline retrieves relevant data, reduces unnecessary data processing, and improves overall performance.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Left Pane,** from the **Database Type** drop-down box, select either **Datasource** or **Assets.** For example, **Datasource.**&#x20;

{% hint style="info" %}
**Tip:** Selecting the **Datasource** option connects to an external database whereas the **Assets** option use pre-configured datasets stored within SCIKIQ.&#x20;
{% endhint %}

2. From the **Datasource** drop-down box, select the required **datasource.**

<figure><img src="../../../../.gitbook/assets/S (340).png" alt=""><figcaption><p>Selecting Database Type and Connection</p></figcaption></figure>

3\. In the **Schema properties** section, select the required **columns**, and then click the **Save** icon.

<figure><img src="../../../../.gitbook/assets/S (341).png" alt="" width="563"><figcaption><p>Selecting Columns</p></figcaption></figure>

{% hint style="info" %}
**Tip:** You can select a **single column, multiple columns,** or **all columns** based on your requirement. Selecting the **Select All** checkbox allows you to select all columns at once. See the **ticked checkbox** in the image below.
{% endhint %}

</details>

<details>

<summary><strong>Connect Input Node with Group By Node</strong></summary>

**Overview:**

As part of connecting the input and Group By nodes, you need to first drag the  **Group By** node from the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2], and then place it on the **Main Workspace**. Once done, you can connect the input node with the **Group By** node.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Toolbar**, click the **Transform Nodes** menu item.&#x20;

The [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] is displayed.

2. From the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] palette, drag the  **Group By** node, and drop it onto the **Main Workspace.**

<figure><img src="../../../../.gitbook/assets/S (342).png" alt=""><figcaption><p>Selecting Group By Node</p></figcaption></figure>

2. Now, drag the **right side** **edge** of the **input node** and connect it to the **left side edge** of **Limit By** node as shown in the below image.

<figure><img src="../../../../.gitbook/assets/S (343).png" alt=""><figcaption><p>Connecting Nodes</p></figcaption></figure>

Once the nodes are connected, the **Group By** section appears on the left pane.

</details>

<details>

<summary><strong>Define Groups</strong></summary>

**Purpose:**

The purpose of defining groups is to organize data into logical categories so that meaningful aggregations and summaries can be performed.&#x20;

**Procedure:**

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

**1. Specify Group Header**

A. On the **Left Pane**, under **Group** tab, click the **Add** ![](<../../../../.gitbook/assets/image (2511).png>) icon next to **Add Group** **column** to group.  See the example image below.&#x20;

The Select drop-down box is displayed.

B. From the **Select** drop-down box, select a **Group** **column**.&#x20;

{% hint style="info" %}
**Tip:**&#x20;

* Based on your requirement, you can select multiple groups as Group Columns.
* To remove a group, click the Remove ![](<../../../../.gitbook/assets/image (2512).png>) icon corresponding to it.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (344).png" alt=""><figcaption><p>Specifying Group</p></figcaption></figure>

**2.Add Columns**

A. After specifying the **Group Header**, click the **Column Tab**.

The column list is displayed.

B. From the **column list**, select the **required columns** to include them as part of the defined group.

C. In the **f(x)** column, select the **required** **function** choosing from **Count(), Sum(), Avg(), Max(),** and **Min()** based on your requirement. Refer to the below table to understand the purpose of function.

<figure><img src="../../../../.gitbook/assets/S (345).png" alt=""><figcaption><p>Adding Columns</p></figcaption></figure>

**Purpose of Functions**

<table><thead><tr><th width="107" valign="top">Function</th><th valign="top">Purpose</th><th valign="top">When to use</th><th valign="top">Example Use Case</th></tr></thead><tbody><tr><td valign="top">Count()</td><td valign="top">Counts the number of records in each group</td><td valign="top">You can use <strong>Count()</strong> when you want to know <strong>how many rows</strong> exist for each grouped value</td><td valign="top"><ul><li>Number of transactions per customer</li><li>Number of orders per day</li></ul><p></p></td></tr><tr><td valign="top">Sum()</td><td valign="top">Adds up all numeric values in a column for each group</td><td valign="top">You can use p<strong>Sum()</strong> when you need the <strong>total value</strong> for each group</td><td valign="top"><ul><li>Total sales amount per region </li><li>Total quantity sold per product </li></ul><p><mark style="color:red;"><strong>Note:</strong></mark> This Sum() function is applicable to only numeric numbers.</p></td></tr><tr><td valign="top">Avg()</td><td valign="top">Calculates the average (mean) value of a numeric column for each group.</td><td valign="top">You can use <strong>Avg()</strong> when you want to understand the typical or <strong>average value</strong> within each group</td><td valign="top"><ul><li>Average order value per customer</li><li>Average salary per department</li></ul></td></tr><tr><td valign="top">Max()</td><td valign="top">Returns the highest value in a column for each group</td><td valign="top">You can use <strong>Max()</strong> when you need the <strong>largest</strong> or <strong>most recent</strong> value in a group</td><td valign="top"><ul><li>Highest transaction amount per customer</li><li>Latest transaction date per account</li></ul><p><mark style="color:red;"><strong>Note:</strong></mark> This can be used with numeric, date, or timestamp columns.</p></td></tr><tr><td valign="top">Min()</td><td valign="top">Returns the lowest value in a column for each group</td><td valign="top">You can use <strong>Min()</strong> when you need the <strong>smallest</strong> or <strong>earliest</strong> value in a group</td><td valign="top"><ul><li>First transaction date per customer</li><li>Lowest price per product</li></ul><p></p></td></tr></tbody></table>

3. Save the **ETL job** now. Refer to the next panel to understand how to save an ETL job.

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the  **Group By** node can be configured correctly and used during execution.

**Procedure**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (346).png" alt="" width="536"><figcaption><p>Saving ETL Job </p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Preview Data</strong></summary>

**Overview:**

The Preview option allows you to verify that the output data matches the defined grouping. You can also validate the pipeline configuration and data output before executio&#x6E;**.**

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step instructions:**

1. On the **Delta Pipelines** page, click the **Edit** icon corresponding to the saved pipeline.&#x20;

<figure><img src="../../../../.gitbook/assets/S (347).png" alt=""><figcaption><p>Delta Pipelines Page - Clicking Edit Icon</p></figcaption></figure>

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **Group By** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (348).png" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

The records are displayed as per the defined groups on the Preview tab. See the example image below:

<figure><img src="../../../../.gitbook/assets/S (349).png" alt=""><figcaption><p>Group Preview</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="Value Mapper" %}
**Overview**

You can use the **Value Mapper transform node** when you need to **replace, standardize, or map values** in one or more columns of data coming from an input node. For example, if you want to replace a credit limit value of 500 with 600 and another value of 3500 with 4000 in the input data, you can do this using the Value Mapper transform node.

Instead of changing the structure of the data, Value Mapper focuses on **modifying the actual values** within existing fields.&#x20;

**Key Concepts:**

<details>

<summary><strong>How Value Mapper transform node works with an input node</strong></summary>

When connected after an input node, the **Value Mapper** transform node scans the selected column(s) and replaces existing values based on the mapping rules you define. For example, it can convert codes into readable labels, standardize inconsistent values, or align data with required formats before further processing.

</details>

<details>

<summary><strong>Common scenarios for using the Value Mapper transform node</strong></summary>

You can use the **Value Mapper** transform node when you need to:

* Convert codes to meaningful values (e.g., 1 → Active, 0 → Inactive)
* Standardize inconsistent data (e.g., M, Male, male → Male)
* Replace legacy values with updated ones
* Align data with business or reporting standards
* Prepare data for downstream systems that expect specific values

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The  **Value Mapper** transform node can be used **directly with structured, row-based inputs.** Some of these inputs include - **File inputs (CSV, Excel), Database inputs, API inputs** (return structured tabular data), and **GraphQL inputs**.

</details>

<details>

<summary><strong>Non-applicable nodes</strong></summary>

The  **Value Mapper** transform node is not **directly applicable to truly unstructured data** such as raw text, images, or binary files, etc.

</details>

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

> <mark style="color:red;">**Note:**</mark> In this procedure, the **Database Input** node is used as an example to demonstrate how the  **Value Mapper** transform node works. However, the same process applies when using the  **Value Mapper** transform node with other input types, such as File Input (CSV or Excel files), Database Input, API Input that returns structured data, and GraphQL Input nodes.

<details>

<summary><strong>Add Input Node</strong> </summary>

**Overview:**

As part of adding the **Input Node**, you need to drag it from the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] and then place it on the in the **Main Workspace**. Once placed, the input fields corresponding to the input node are displayed on the left pane.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

,The [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] is displayed.&#x20;

3. From the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1], select the **Input Node** (For example, Database Input), and drag it onto the **Main Workspace.**&#x20;

<figure><img src="../../../../.gitbook/assets/S (339).png" alt="" width="507"><figcaption><p>Adding Input Node</p></figcaption></figure>

The Database Type and Scheme Properties sections are displayed in the left pane.&#x20;

</details>

<details>

<summary><strong>Select Necessary Columns</strong></summary>

**Purpose:**

After placing the input node, select the required columns so that they are available and visible when the input node is connected to the **Value Mapper** transform node.&#x20;

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Left Pane,** from the **Database Type** drop-down box, select either **Datasource** or **Assets.** For example, **Datasource.**&#x20;

{% hint style="info" %}
**Tip:** Selecting the **Datasource** option connects to an external database whereas the **Assets** option use pre-configured datasets stored within SCIKIQ.&#x20;
{% endhint %}

2. From the **Datasource** drop-down box, select the required **datasource.**

<figure><img src="../../../../.gitbook/assets/S (340).png" alt=""><figcaption><p>Selecting Database Type and Connection</p></figcaption></figure>

3\. In the **Schema properties** section, select the required **columns**, and then click the **Save** icon.

> <mark style="color:red;">**Note:**</mark> Be sure to save the configuration; otherwise, the selected columns will not be available when the input node is connected to the **Value Mapper** transform node.

<figure><img src="../../../../.gitbook/assets/S (341).png" alt="" width="563"><figcaption><p>Selecting Columns</p></figcaption></figure>

{% hint style="info" %}
**Tip:** You can select a **single column, multiple columns,** or **all columns** based on your requirement. Selecting the **Select All** checkbox allows you to select all columns at once. See the **ticked checkbox** in the image below.
{% endhint %}

</details>

<details>

<summary><strong>Connect Input Node with Value Mapper Node</strong></summary>

**Overview:**

Connecting the input node to the **Value Mapper** transform node allows you to choose the required columns that will be passed forward for further processing in the pipeline.

**Procedure:**

As part of connecting the input and **Value Mapper** nodes, you need to first drag the **Value Mapper** node from the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2], and then place it on the **Main Workspace**. Once done, you can connect the input node with the **Value Mapper** node.

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Toolbar**, click the **Transform Nodes** menu item.&#x20;

The [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] is displayed.

2. From the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] palette, drag the  **Value Mapper** node, and drop it onto the **Main Workspace.**

<figure><img src="../../../../.gitbook/assets/S (350).png" alt=""><figcaption><p>Adding Value Mapper Node</p></figcaption></figure>

2. Now, drag the **right side** **edge** of the **input node** and connect it to the **left side edge** of **Value Mapper** transform node as shown in the below image.

<figure><img src="../../../../.gitbook/assets/S (351).png" alt=""><figcaption><p>Connecting Nodes</p></figcaption></figure>

Once the nodes are connected, the **Value Mapper** section appears on the left pane.

</details>

<details>

<summary><strong>Define Source, Target,  and Default Values</strong> </summary>

**Purpose:**

Defining source and target values allows you to replace specific source values with the corresponding target values, while any values that are not explicitly defined are replaced with the value set as the default value.

**Procedure:**

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. On the **Left Pane**, in the **Value Mapper** section, from the **Field name to use** drop-down box, select the **required field**. For example, CREDIT\_LIMIT. &#x20;
2. In the **Target field name** field, enter a **name for the new target field** where the mapped values will be stored.
3. Next, click the **Add Item** ![](<../../../../.gitbook/assets/image (2513).png>) icon next to **Target Value**.&#x20;

<figure><img src="../../../../.gitbook/assets/S (352).png" alt=""><figcaption><p>Selecting Source Field, Target Field, and Defining Default Value</p></figcaption></figure>

The Source Value and Target Value fields are displayed.&#x20;

4. Specify the **Source Value** and **Target Value**.

> <mark style="color:red;">**Note:**</mark> In the below screenshot, two rows are shown as configured. The first row is configured with Source Value of 500 and Target Value of 600. The second row is configured with Source Value of 300 and Target Value of 4000.

4. In the **Default upon non-matching** field, specify the **default value** (For example, 6000) in case a source value doesn't match with the target value.&#x20;

> <mark style="color:red;">**Note:**</mark> Suppose, if a source value is 5000 and it is not explicitly defined, then that 5000 will be replaced with 6000.&#x20;

<figure><img src="../../../../.gitbook/assets/S (353).png" alt="" width="530"><figcaption><p>Configuring Source, Target, and Default Values</p></figcaption></figure>

4. Save the **ETL job** now. Refer to the next panel to understand how to save an ETL job.

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the  **Value Mapper** node can be configured correctly and used during execution.

**Procedure**

As part of saving the ETL job, you need to input a **name** and **description** for the pipeline along with specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (354).png" alt="" width="563"><figcaption><p>Saving ETL Job </p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Preview Data</strong></summary>

**Overview:**

The **Preview** option allows you to verify that the output data reflects the configured **source, target,** and **default** values. It also helps you validate the pipeline configuration and review the data output before execution.

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step instructions:**

1. On the **Delta Pipelines** page, click the **Edit** icon corresponding to the saved pipeline.&#x20;

<figure><img src="../../../../.gitbook/assets/S (355).png" alt=""><figcaption><p>Delta Pipelines Page - Clicking Edit Icon</p></figcaption></figure>

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **Value Mapper** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (356).png" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

The records are displayed on the Preview tab as per the configuration. See the example image below:

<figure><img src="../../../../.gitbook/assets/S (357).png" alt=""><figcaption><p>Display of Source, Target, and Default Values</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="Select" %}
**Overview**

The **Select** transform node is used when you want to **choose which columns from the input data should be kept and passed forward** in the pipeline. It helps you control the structure of the dataset immediately after data is read from the source.

**Key Concepts:**

<details>

<summary>How Select transform node works with an input node</summary>

When connected after an input node, the **Select** node displays all available columns returned by the input source. You can then pick only the required columns and exclude the rest. The pipeline continues processing using **only the selected columns**, while the unselected columns are dropped.

</details>

<details>

<summary>Common scenarios for using the Select transform node</summary>

You can use the **Select** transform node when you need to:

* Remove unnecessary columns early in the pipeline
* Simplify datasets before applying other transformations
* Improve performance by reducing data volume

</details>

<details>

<summary>Applicable input nodes</summary>

The  **Select** transform node can be used **directly with structured, row-based inputs.** Some of these inputs include - **File inputs (CSV, Excel), Database inputs, API inputs** (return structured tabular data), and **GraphQL inputs**.

</details>

<details>

<summary>Non-applicable nodes</summary>

The  **Select** transform node is not **directly applicable to truly unstructured data** such as raw text, images, or binary files, etc.

</details>

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

> <mark style="color:red;">**Note:**</mark> In this procedure, the **Database Input** node is used as an example to demonstrate how the  **Select** transform node works. However, the same process applies when using the  **Select** transform node with other input types, such as File Input (CSV or Excel files), Database Input, API Input that returns structured data, and GraphQL Input nodes.

<details>

<summary><strong>Add Input Node</strong> </summary>

**Overview:**

As part of adding the **Input Node**, you need to drag it from the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] and then place it on the in the **Main Workspace**. Once placed, the input fields corresponding to the input node are displayed on the left pane.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

,The [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] is displayed.&#x20;

3. From the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1], select the **Input Node** (For example, Database Input), and drag it onto the **Main Workspace.**&#x20;

<figure><img src="../../../../.gitbook/assets/S (339).png" alt="" width="507"><figcaption><p>Adding Input Node</p></figcaption></figure>

The Database Type and Scheme Properties sections are displayed in the left pane.&#x20;

</details>

<details>

<summary><strong>Select Necessary Columns</strong></summary>

**Purpose:**

After placing the input node, select the required columns so that they are available and visible when the input node is connected to the Select transform node.&#x20;

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Left Pane,** from the **Database Type** drop-down box, select either **Datasource** or **Assets.** For example, **Datasource.**&#x20;

{% hint style="info" %}
**Tip:** Selecting the **Datasource** option connects to an external database whereas the **Assets** option use pre-configured datasets stored within SCIKIQ.&#x20;
{% endhint %}

2. From the **Datasource** drop-down box, select the required **datasource.**

<figure><img src="../../../../.gitbook/assets/S (340).png" alt=""><figcaption><p>Selecting Database Type and Connection</p></figcaption></figure>

3\. In the **Schema properties** section, select the required **columns**, and then click the **Save** icon.

<figure><img src="../../../../.gitbook/assets/S (341).png" alt="" width="563"><figcaption><p>Selecting Columns</p></figcaption></figure>

{% hint style="info" %}
**Tip:** You can select a **single column, multiple columns,** or **all columns** based on your requirement. Selecting the **Select All** checkbox allows you to select all columns at once. See the **ticked checkbox** in the image below.
{% endhint %}

</details>

<details>

<summary><strong>Connect Input Node with Select Node</strong></summary>

**Overview:**

Connecting the input node to the Select transform node allows you to choose the required columns that will be passed forward for further processing in the pipeline.

**Procedure:**

As part of connecting the input and **Select** nodes, you need to first drag the **Select** node from the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2], and then place it on the **Main Workspace**. Once done, you can connect the input node with the **Select** node.

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Toolbar**, click the **Transform Nodes** menu item.&#x20;

The [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] is displayed.

2. From the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] palette, drag the  **Select** node, and drop it onto the **Main Workspace.**
3. Now, drag the **right side** **edge** of the **input node** and connect it to the **left side edge** of **Limit By** node as shown in the below image.

<figure><img src="../../../../.gitbook/assets/S (358).png" alt=""><figcaption><p>Connecting Nodes</p></figcaption></figure>

Once the nodes are connected, the **Select** section appears on the left pane.

</details>

<details>

<summary><strong>Select Columns</strong></summary>

**Purpose:**

The purpose of selecting columns is to control what data is kept and what data is dropped as the pipeline moves forward.

**Procedure:**

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. On the **Left Pane**, in the Select section, select the required columns. For example, CUSTOMER\_ID, NAME, and ADDRESS. &#x20;
2. Enable the **Distinct** option if you want to avoid the duplicates.
3. From the **Data Type** drop-down, select the appropriate option choosing from **INT, FLOAT, STR, TMS, DATE,** and **TEXT**.&#x20;

{% hint style="info" %}
**Why to select a data type?**

Choosing a data type tells the pipeline how to interpret, process, and store the data for the selected column.

Refer to the below table for the description of the data types.
{% endhint %}

{% hint style="info" %}
**Tip:** If required, you can use the **Alias** field to rename columns so they appear differently in the output.&#x20;
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (359).png" alt=""><figcaption><p>Selecting Columns</p></figcaption></figure>

**Purpose of Data Types**

<table><thead><tr><th width="124" valign="top">Function</th><th valign="top">Purpose</th><th valign="top">When to use</th><th width="153" valign="top">Example Use Cases</th><th valign="top">Examples</th></tr></thead><tbody><tr><td valign="top">INT (Integer)</td><td valign="top">Used for whole numbers without decimal values.</td><td valign="top">You can choose <strong>INT</strong> when the column represents counts or numeric values that will not contain decimals.</td><td valign="top"><ul><li>Number of items sold</li><li>Age</li></ul><p></p><p></p></td><td valign="top"><p>25</p><p>100</p></td></tr><tr><td valign="top">FLOAT</td><td valign="top">Used for numeric values that include decimal points.</td><td valign="top">You can choose <strong>FLOAT</strong> when precision is required for calculations involving fractions or measurements.</td><td valign="top"><ul><li>Price or amount</li><li>Percentage values</li></ul></td><td valign="top"><p>99.75</p><p>0.85</p></td></tr><tr><td valign="top">STR (String)</td><td valign="top">Used for short text or alphanumeric values</td><td valign="top">You can choose <strong>STR</strong> when the column contains names, codes, or identifiers that are not meant for numeric calculations.</td><td valign="top"><ul><li>Customer name</li><li>Product code</li></ul></td><td valign="top"><p>A123</p><p>London</p></td></tr><tr><td valign="top">TMS (Timestamp)</td><td valign="top">Used to store both <strong>date and time</strong> values.</td><td valign="top">You can choose TMS when you need precise time information, including hours, minutes, and seconds.</td><td valign="top"><ul><li>Transaction timestamp</li><li>Login time</li></ul></td><td valign="top">2026-02-12 14:35:22</td></tr><tr><td valign="top">Date</td><td valign="top">Used to store date values <strong>without time information</strong>.</td><td valign="top">You can choose DATE when only the calendar date matters.</td><td valign="top"><ul><li>Date of birth</li><li>Invoice date</li></ul></td><td valign="top">2026-02-12 </td></tr></tbody></table>

4. Save the **ETL job** now. Refer to the next panel to understand how to save an ETL job.

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the  **Select** node can be configured correctly and used during execution.

**Procedure**

As part of saving the ETL job, you need to input a **name** and **description** for the pipeline along with specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (360).png" alt="" width="563"><figcaption><p>Saving ETL Job </p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Preview Data</strong></summary>

**Overview:**

The Preview option allows you to verify that the output data matches the selected columns. You can also validate the pipeline configuration and data output before executio&#x6E;**.**

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step instructions:**

1. On the **Delta Pipelines** page, click the **Edit** icon corresponding to the saved pipeline.&#x20;

<figure><img src="../../../../.gitbook/assets/S (361).png" alt=""><figcaption><p>Delta Pipelines Page - Clicking Edit Icon</p></figcaption></figure>

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **Select** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (362).png" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

The records are displayed as per the selected columns on the Preview tab. See the example image below:

<figure><img src="../../../../.gitbook/assets/S (363).png" alt=""><figcaption><p>Selected Columns Preview</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="Calculated Field" %}
**Overview**

You can use the **Calculated Field** transform node when the required source columns are already available in the input data and you need to derive new values using expressions, formulas, or business logic at the row level. It is typically applied immediately after the input node to enrich raw data with business-ready fields before any further transformations or aggregations..&#x20;

**Key Concepts:**

<details>

<summary><strong>How Calculated Field transform node works with an input node</strong></summary>

The **Calculated** transform node works with an **Input node** by taking the raw fields coming from the input source, applying defined functions or expressions to them, and producing new calculated fields that travel along with the original data to the next stage of the pipeline.

</details>

<details>

<summary><strong>Common scenarios for using the Calculated Field transform node</strong></summary>

The **Calculated transform node** is commonly used whenever you need to **derive new, meaningful fields from existing data** as part of a data pipeline—without modifying the source data.

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The **Calculated Field node is input-agnostic**; it does not depend on the origin of the data. Instead, it operates solely based on the availability and structure of the input columns provided to it.

The  **Calculated By** transform node can be used with the below input nodes:

* File-based inputs (CSV, Excel, JSON, Parquet, etc.)
* Database inputs (SQL, NoSQL tables, views)
* API / REST / GraphQL input nodes
* SAP input nodes (Tables, CDS, BW objects)
* Streaming or batch data sources
* Cloud storage inputs

</details>

<details>

<summary><strong>Non-applicable nodes</strong></summary>

The **Calculated Field** transform node is not applicable to input nodes that do not produce structured, column-based data or do not expose fields to the pipeline. Some of these non- applicable input nodes include:

* Nodes that do not output tabular data
* Control or trigger-based input nodes
* Nodes that output unstructured or binary data
* Input nodes without schema or column selection

</details>

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

> <mark style="color:red;">**Note:**</mark> In this procedure, the **Database Input node** is used as an example to demonstrate how the **Calculated Field** transform node works. However, the same process applies when using the **Calculated Field** transform node with other input types, such as file-based inputs (CSV, Excel, JSON, Parquet), database inputs (SQL and NoSQL tables or views), API/REST/GraphQL input nodes, SAP input nodes (Tables, CDS, BW objects), streaming or batch data sources, and cloud storage inputs.

<details>

<summary><strong>Add Input Node</strong> </summary>

**Overview:**

As part of adding the **Input Node**, you need to drag it from the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] and then place it on the in the **Main Workspace**. Once placed, the input fields corresponding to the input node are displayed on the left pane.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

,The [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] is displayed.&#x20;

3. From the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1], select the **Input Node** (For example, Database Input), and drag it onto the **Main Workspace.**&#x20;

<figure><img src="../../../../.gitbook/assets/S (339).png" alt="" width="507"><figcaption><p>Adding Input Node</p></figcaption></figure>

The Database Type and Schema Properties sections are displayed in the left pane.&#x20;

</details>

<details>

<summary><strong>Select Necessary Columns</strong></summary>

**Purpose:**

After placing the input node, you need to select the required columns so that they are available and visible when the input node is connected to the **Calculated Field** transform node.&#x20;

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Left Pane,** from the **Database Type** drop-down box, select either **Datasource** or **Assets.** For example, **Datasource.**&#x20;

{% hint style="info" %}
**Tip:** Selecting the **Datasource** option connects to an external database whereas the **Assets** option use pre-configured datasets stored within SCIKIQ.&#x20;
{% endhint %}

2. From the **Datasource** drop-down box, select the required **datasource.**

<figure><img src="../../../../.gitbook/assets/S (340).png" alt=""><figcaption><p>Selecting Database Type and Connection</p></figcaption></figure>

3\. In the **Schema properties** section (See the below image):

* From the **Table** drop-down box, select the **required table**.
* Select the required **columns**.

{% hint style="info" %}
**Tip:** You can select a **single column, multiple columns,** or **all columns** based on your requirement. Selecting the **Select All** checkbox allows you to select all columns at once. See the **top** **ticked checkbox** in the image below.
{% endhint %}

* Enable the **Distinct** option to **remove the duplicates**, if any.
* Click the **Save** button (below the **Distinct** option) to save the configuration.

> <mark style="color:red;">**Note:**</mark> Be sure to save the configuration; otherwise, the selected columns will not be available when the input node is connected to the **Calculated Field** transform node.

<figure><img src="../../../../.gitbook/assets/S (364).png" alt="" width="563"><figcaption><p>Selecting Columns</p></figcaption></figure>

</details>

<details>

<summary><strong>Connect Input Node with Calculated Field Transform Node</strong></summary>

**Overview:**

The purpose of connecting a **Calculated Field** transform node with an input node is to derive new fields from the source data by applying defined calculations or business logic to the input columns, while preserving the original data.

**Procedure:**

As part of connecting the **input** and **Calculated Field** transform nodes, you need to first drag the **Calculated Field** transform node from the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2], and then place it on the **Main Workspace**. Once done, you can connect the input node with the **Calculated Field** transform node.

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Toolbar**, click the **Transform Nodes** menu item.&#x20;

The [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] is displayed.

2. From the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] palette, drag the **Calculated Field** transform node, and drop it onto the **Main Workspace.**
3. Now, drag the **right side** **edge** of the **input node** and connect it to the **left side edge** of **Calculated Field** node as shown in the below image.

<figure><img src="../../../../.gitbook/assets/S (365).png" alt=""><figcaption><p>Connecting Nodes</p></figcaption></figure>

Once the nodes are connected, the **Open Calculated Field** button appears on the left pane.

</details>

<details>

<summary><strong>Define Logic</strong></summary>

**Purpose:**

You can derive new values by defining the logic in the **Calculated Field** **Editor.** **Deriving new values** using the **Calculated** Field transform node is to enrich raw input data with meaningful, business-ready information in a consistent and reusable way, without altering the source data.

**Procedure:**

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. On the **Left Pane**, click the **Open Calculated Field** button.

<figure><img src="../../../../.gitbook/assets/S (366).png" alt=""><figcaption><p>Open Calculated Field Button</p></figcaption></figure>

The **Calculated Field Editor** is displayed.

2. On the **Calculated Field Editor** (See the example image below):

* Enter the **Field Name** and **Description**.
* Write the **expression** required expression to derive new values.&#x20;
* Click the **Save** button.

> <mark style="color:red;">**Note:**</mark> If you want to reuse the calculated expression consistently across multiple pipelines to ensure standardization and maintainability, then enable the **Save for** **global use** ![](<../../../../.gitbook/assets/image (2514).png>)option.

<figure><img src="../../../../.gitbook/assets/S (367).png" alt=""><figcaption><p>Defining Expression</p></figcaption></figure>

The **Custom Field added** success message is displayed and the **new field** **expression** is displayed on the left pane.

3. Click the Edit ![](<../../../../.gitbook/assets/image (2515).png>) icon If you want to edit the expression.
4. Click the Delete ![](<../../../../.gitbook/assets/image (2516).png>)icon to remove the expression.

<figure><img src="../../../../.gitbook/assets/S (368).png" alt=""><figcaption><p>Calculated Field - Edit and Delete Icons</p></figcaption></figure>

4. Save the **ETL job** now. Refer to the next panel to understand how to save an ETL job.

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the  **Calculated Field** node can be configured correctly and used during execution.

**Procedure**

As part of saving the ETL job, you need to input a **name** and **description** for the pipeline along with specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (369).png" alt="" width="563"><figcaption><p>Saving ETL Job</p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Preview Data</strong></summary>

**Overview:**

The **Preview** option allows you to verify that the output data reflects the configured **source, target,** and **default** values. It also helps you validate the pipeline configuration and review the data output before execution.

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step instructions:**

1. On the **Delta Pipelines** page, click the **Edit** icon corresponding to the saved pipeline.&#x20;

<figure><img src="../../../../.gitbook/assets/S (370).png" alt=""><figcaption><p>Delta Pipelines Page - Clicking Edit Icon</p></figcaption></figure>

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **Calculated Field** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (371).png" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

The newly derived values are displayed on the Preview tab as per the defined configuration. See the example image below:

<figure><img src="../../../../.gitbook/assets/S (372).png" alt=""><figcaption><p>Derived Values Preview</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="DF to JSON " %}
**Overview**

You can use this transform node when you need to convert structured, tabular data into a nested JSON format. This is particularly useful for API consumption, downstream processing, or storing data as JSON files.

**Key Concepts:**

<details>

<summary><strong>How DF to JSON transform node works with an input node</strong></summary>

The **DF (Data Frame) to JSON** transform node works with an input node by receiving structured, tabular data from the input node and converting each record into a JSON object or a nested JSON structure, based on the configured mapping rules.

</details>

<details>

<summary><strong>Common scenarios for using the DF to JSON transform node</strong></summary>

Some of the common scenarios for using DF to JSON transform node includes when:

* Preparing data for API consumption
* Creating nested or Hierarchical JSON structures
* Storing data as JSON files
* Integrating with downstream JSON-Based systems
* Transforming data for NoSQL or Document Databases

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The **DF to JSON t**ransform node works with input nodes that Output **rows and columns,** Expose a **defined schema, and** Allow column-level access in preview or configuration.

The examples include:

* File inputs (CSV, Excel, Parquet with schema)
* Database table or query inputs
* SAP table / CDS / BW object inputs
* Parsed API responses that return tabular data

</details>

<details>

<summary><strong>Non-applicable nodes</strong></summary>

The **DF to JSON** transform node is not applicable to the below input nodes:

* Input nodes that do not output a data Frame
* Input nodes that output raw or unstructured data
* Input nodes without schema definition

</details>

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

> <mark style="color:red;">**Note:**</mark> In this procedure, the **Database Input node** is used only as an example to show how the **DF to JSON transform node** works. The same steps apply when using the DF to JSON transform node with other input types, such as file-based inputs (CSV, Excel, JSON, Parquet), database inputs, API/REST/GraphQL inputs, SAP inputs, streaming or batch data sources, and cloud storage inputs.

<details>

<summary><strong>Add Input Node</strong> </summary>

**Overview:**

As part of adding the **Input Node**, you need to drag it from the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] and then place it on the in the **Main Workspace**. Once placed, the input fields corresponding to the input node are displayed on the left pane.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

,The [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] is displayed.&#x20;

3. From the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1], select the **Input Node** (For example, Database Input), and drag it onto the **Main Workspace.**&#x20;

<figure><img src="../../../../.gitbook/assets/S (339).png" alt="" width="507"><figcaption><p>Adding Input Node</p></figcaption></figure>

The Database Type and Scheme Properties sections are displayed in the left pane.&#x20;

</details>

<details>

<summary><strong>Select Necessary Columns</strong></summary>

**Purpose:**

After placing the input node, select the required columns so that they are available and visible when the input node is connected to the **DF to JSON** transform node.&#x20;

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Left Pane,** from the **Database Type** drop-down box, select either **Datasource** or **Assets.** For example, **Datasource.**&#x20;

{% hint style="info" %}
**Tip:** Selecting the **Datasource** option connects to an external database whereas the **Assets** option use pre-configured datasets stored within SCIKIQ.&#x20;
{% endhint %}

2. From the **Datasource** drop-down box, select the required **datasource.**

<figure><img src="../../../../.gitbook/assets/S (340).png" alt=""><figcaption><p>Selecting Database Type and Connection</p></figcaption></figure>

3\. In the **Schema properties** section, select the required **columns**, and then click the **Save** icon.

> <mark style="color:red;">**Note:**</mark> Be sure to save the configuration; otherwise, the selected columns will not be available when the input node is connected to the **Value Mapper** transform node.

<figure><img src="../../../../.gitbook/assets/S (341).png" alt="" width="563"><figcaption><p>Selecting Columns</p></figcaption></figure>

{% hint style="info" %}
**Tip:** You can select a **single column, multiple columns,** or **all columns** based on your requirement. Selecting the **Select All** checkbox allows you to select all columns at once. See the **ticked checkbox** in the image below.
{% endhint %}

</details>

<details>

<summary><strong>Connect Input Node with DF to JSON Transform Node</strong></summary>

**Overview:**

The **purpose** of connecting an **input node** with the **DF to JSON transform node** is to convert the structured, tabular data produced by the input node into JSON format, enabling its use in JSON-based integrations, storage, and downstream processing.

**Procedure:**

As part of connecting the input and **DF to JSON transform** nodes, you need to first drag the **DF  to JSON** transform node from the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2], and then place it on the **Main Workspace**. Once done, you can connect the input node with the **DF  to JSON** transform node.

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Toolbar**, click the **Transform Nodes** menu item.&#x20;

The [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] is displayed.

2. From the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] palette, drag the **DF to JSON** transform node, and drop it onto the **Main Workspace.**
3. Now, drag the **right side** **edge** of the **input node** and connect it to the **left side edge** of **DF to JSON** transform node as shown in the below image.

<figure><img src="../../../../.gitbook/assets/S (373).png" alt=""><figcaption><p>Connecting Nodes</p></figcaption></figure>

Once the nodes are connected, the **Group** and **Column** tabs appear on the left pane.

</details>

<details>

<summary><strong>Configure Group Parameters</strong></summary>

**Purpose:**

Configuring **Group Parameters** control the shape, hierarchy, and grouping of the generated JSON.

**Procedure:**

As part of configuring the Group Parameters, you need to specify **Nested Field Name**, and configure **Orientation**, and **Group Columns.**&#x20;

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. On the **Left Pane**, under the **Group** tab, specify a name in the **Nested Field Name** field.

{% hint style="info" %}
**Tip:** The **Nested Field Name** specifies the **JSON key under which grouped or repeated records are stored as an array**. It creates a clear parent–child structure in the JSON output. Also, it groups related records under a single logical field.
{% endhint %}

2. From the **Orientation** drop-down box, select the **appropriate option** choosing from **dict, list, series, split, tight, records,** or **index**.&#x20;

{% hint style="info" %}
**Tip:** The **Orientation** options control **how the tabular Data Frame is converted into JSON**. Refer to the below table for the description on **Orientation** options.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (374).png" alt=""><figcaption><p>Configuring Nested Frame and Orientation</p></figcaption></figure>

**Description for Orientation Options**

<table><thead><tr><th width="97" valign="top">Option</th><th width="282" valign="top">Description</th><th valign="top">When to Use</th></tr></thead><tbody><tr><td valign="top">dict</td><td valign="top">Converts the Data Frame into a <strong>dictionary of columns</strong>, where each column name maps to another dictionary of row index and values.</td><td valign="top">You can use this option when you want column-centric JSON representation.</td></tr><tr><td valign="top">list</td><td valign="top">Converts each column into a <strong>list of values</strong></td><td valign="top">You can use this option when the order matters and index values are not required.</td></tr><tr><td valign="top">series</td><td valign="top">Converts each column into a <strong>key–value pair</strong> representing a Pandas Series</td><td valign="top">You can use this option when you want series-style representation is needed (less commonly used). </td></tr><tr><td valign="top">split</td><td valign="top">Splits the Data Frame into <strong>separate arrays for index, columns, and data</strong></td><td valign="top">You can use this option when you need a complete structural representation of the Data Frame.</td></tr><tr><td valign="top">tight</td><td valign="top">Similar to <strong>split</strong> option but includes additional metadata such as column and index names</td><td valign="top">You can use this option when metadata preservation is required.</td></tr><tr><td valign="top">records</td><td valign="top">Converts each row into a <strong>JSON object</strong>, stored as a list</td><td valign="top">You can use this option when sending data to APIs or systems that expect row-wise JSON objects.</td></tr><tr><td valign="top">index</td><td valign="top">Creates a dictionary keyed by the <strong>row index</strong>, with each value being a row object</td><td valign="top">You can use this option when row index is meaningful and must be preserved.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Define Column Nesting</strong></summary>

**Purpose:**

The **purpose of defining column nesting by selecting columns** is to **control how flat, tabular columns are organized into hierarchical or nested structures in the output JSON**, ensuring the JSON format aligns with downstream system or API requirements.

**Procedure:**

As part of defining the column nesting, you need to configure the required **columns** and **aggregate** **functions.**&#x20;

{% hint style="info" %}
**Tip:** Selecting aggregate functions is **optional** and should be done only when required, based on the specific use case.
{% endhint %}

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. On the **Left Pane**, select the required **columns.**&#x20;

{% hint style="info" %}
**Tip:** You can select a **single column, multiple columns,** or **all columns** based on your requirement. Selecting the **Select All** checkbox allows you to select all columns at once. See the **ticked checkbox** in the image below.

![](<../../../../.gitbook/assets/image (2517).png>)
{% endhint %}

2. Select the required **aggregation functions** choosing from **Count(), Avg(), Sum(), Max(),** and **Min()**.&#x20;

> <mark style="color:red;">**Note:**</mark> Selecting aggregate functions is **optional** and should be done only when required, based on the specific use case.

{% hint style="info" %}
**Tip:** Selecting aggregation functions such as **Count, Avg, Sum, Max,** and **Min** enables the creation of summarized, business-level values from grouped data, producing concise and meaningful JSON output.

Refer to the below table for the description of these functions.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (375).png" alt=""><figcaption><p>Selecting Columns</p></figcaption></figure>

**Description of Aggregate Functions**

<table><thead><tr><th width="144" valign="top">Function</th><th valign="top">Purpose</th><th valign="top">Example Business Meaning</th></tr></thead><tbody><tr><td valign="top">Count()</td><td valign="top">Counts the number of records in a group</td><td valign="top">Number of items in an order</td></tr><tr><td valign="top">Sum()</td><td valign="top">Calculates the total of values in a numeric column</td><td valign="top">Total order value</td></tr><tr><td valign="top">Avg()</td><td valign="top">Computes the average of values in a numeric column</td><td valign="top">Average transaction amount</td></tr><tr><td valign="top">Max()</td><td valign="top">Returns the highest value within a group</td><td valign="top">Highest value in the group</td></tr><tr><td valign="top">Min()</td><td valign="top">Returns the lowest value within a group</td><td valign="top">Lowest value in the group</td></tr></tbody></table>

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the  **DF to JSON** node can be configured correctly and used during execution.

**Procedure**

As part of saving the ETL job, you need to input a **name** and **description** for the pipeline along with specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (376).png" alt="" width="563"><figcaption><p>Saving ETL Job </p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Preview Data</strong></summary>

**Overview:**

The **purpose** of previewing when applying the DF (Data Frame) to JSON transform node with an input node is to verify that the tabular input data is correctly converted into the expected JSON structure before executing the full pipeline.

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step instructions:**

1. On the **Delta Pipelines** page, click the **Edit** icon corresponding to the saved pipeline.&#x20;

<figure><img src="../../../../.gitbook/assets/S (377).png" alt=""><figcaption><p>Delta Pipelines Page - Clicking Edit Icon</p></figcaption></figure>

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **DF to JSON** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (378).png" alt=""><figcaption><p>Previewing</p></figcaption></figure>

The JSON is displayed on the Preview tab as per the configuration. See the example image below:

<figure><img src="../../../../.gitbook/assets/S (379).png" alt=""><figcaption><p>JSON Preview</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="JSON to DF" %}
**Overview**

You can use this transform node **when the incoming data is in JSON format and needs to be converted into a tabular (DataFrame) structure** so that downstream transform nodes (Filter, Join, Group By, Calculated By, etc.) can work on it.

**Key Concepts:**

<details>

<summary><strong>How JSON  to DF transform node works with an input node</strong></summary>

When connected to an input node, the JSON to DF transform node reads the raw JSON output, parses its structure, extracts required fields using JSON paths, flattens nested elements, and converts the data into a structured Data Frame format that can be consumed by downstream transformation and output nodes.

</details>

<details>

<summary><strong>Common scenarios for using the JSON  to DF transform node</strong></summary>

The **JSON to DF** transform node is used whenever **JSON data must be converted into a structured Data Frame** to enable mapping, transformation, and downstream processing.

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The **DF to JSON** transform node works with the below input nodes:&#x20;

* API / GraphQL Input Node
* REST API Input Node
* Webhook Input Node
* JSON File Input Node
* Streaming / Event Input Nodes (JSON-based)

</details>

<details>

<summary><strong>Non-applicable nodes</strong></summary>

The **JSON  to DF** transform node is not applicable to the below input nodes:

* Database Input Nodes
* CSV / Excel / Parquet Input Nodes
* UCM File Loader Input Node (Process Tables)
* SAP / ERP Input Nodes

</details>

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

> <mark style="color:red;">**Note:**</mark> In this procedure, the **File Input node** is used only as an example to show how the **JSON  to DF transform node** works. The same steps apply when using the **JSON  to DF** transform node with other input types, such as API / GraphQL Input Node, REST API Input Node, Webhook Input Node, JSON File Input Node, and Streaming / Event Input Nodes (JSON-based).

<details>

<summary><strong>Select Input Node</strong></summary>

**Overview:**

As part of adding the **Input Node**, you need to drag it from the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] and then place it on the in the **Main Workspace**. Once placed, the input fields corresponding to the input node are displayed on the left pane. &#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

,The [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] is displayed.&#x20;

3. From the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1], select the **Input Node** in which the JSON file is located (For example, File Input), and drag it onto the **Main Workspace.**&#x20;

<figure><img src="../../../../.gitbook/assets/S (382).png" alt=""><figcaption><p>Selecting File Input Node</p></figcaption></figure>

The Select File Type section is displayed on the left pane.

</details>

<details>

<summary><strong>Select JSON Source</strong> </summary>

**Overview:**

As part of selecting the **JSON source**, you need to browse and locate the file. Once selected, the selected file name is displayed on the input node. If required, you can view the **JSON object** by clicking the **Preview** icon on the top of the input node.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **left pane, f**rom the **Select File Type** drop-down box, select the **required file type**. For example, File Storage.&#x20;
2. From the **Select Storage** drop-down box, select the **storage**.
3. From the **File Extension** drop-down box, select **JSON**.
4. Click the **Connect** button.

The Root folder is displayed.

5. Browse through the **Root** folder to locate the **JSON file**.

<figure><img src="../../../../.gitbook/assets/S (383).png" alt="" width="508"><figcaption><p>Selecting JSON File</p></figcaption></figure>

&#x20;6\. Scroll down to the bottom of **Select File Type** screen, and then click the **Preview** button.&#x20;

<figure><img src="../../../../.gitbook/assets/S (384).png" alt=""><figcaption><p>Select File Type Screen - Preview Button</p></figcaption></figure>

The JSON object is displayed on the Preview tab.&#x20;

<figure><img src="../../../../.gitbook/assets/S (385).png" alt="" width="563"><figcaption><p>JSON Object</p></figcaption></figure>

</details>

<details>

<summary><strong>Connect Input Node with JSON  to DF Transform Node</strong></summary>

**Overview:**

The purpose of connecting the **input node** to the **JSON to DF** transform node is to **convert raw JSON data into a structured Data Frame format** so that it can be processed by downstream transformation and output nodes.

**Procedure:**

As part of connecting the input and **DF to JSON transform** nodes, you need to first drag the **DF  to JSON** transform node from the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2], and then place it on the **Main Workspace**. Once done, you can connect the input node with the **DF  to JSON** transform node.

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Toolbar**, click the **Transform Nodes** menu item.&#x20;

The [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] is displayed.

2. From the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] palette, drag the **JSON** **to** **DF** transform node, and drop it onto the **Main Workspace.**
3. Now, drag the **right side** **edge** of the **input node** and connect it to the **left side edge** of **JSON** **to** **DF** transform node as shown in the below image.

<figure><img src="../../../../.gitbook/assets/S (386).png" alt=""><figcaption><p>Connecting Nodes</p></figcaption></figure>

Once the nodes are connected, the **Open Mapper** button appears on the left pane.

</details>

<details>

<summary><strong>Map JSON Key-Value Pairs</strong></summary>

**Purpose:**

The purpose of **mapping key-value pairs** while connecting an input node (containing the JSON object) with a **JSON to DF** transform node is to **select, extract, and convert specific JSON fields into DataFrame columns** for downstream processing.&#x20;

Mapping key-value pairs allows you to:

* Explicitly **choose which JSON keys are required**
* Define how each key maps to a **DataFrame column**
* Control the **structure and schema** of the output DataFrame
* Exclude irrelevant or sensitive JSON fields
* Flatten nested JSON objects into usable columns

**Procedure:**

As part of **mapping**, you need to select the **key-value pairs** and then move them to the right pane on the **Mapper** screen. Once done, you need to save the configurations.&#x20;

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. On the **Left Pane**, click the **Open Mapper** button.

The Mapper screen is displayed.

2. On the **Mapper** screen, select the required **JSON key-value pairs**, and click the **Move Right** <img src="../../../../.gitbook/assets/image (2520).png" alt="" data-size="original">button to move it to the right.&#x20;

{% hint style="info" %}
**Tip:** You can select either the entire JSON object or only the required key-value pairs based on your requirement.
{% endhint %}

2. Click the **Preview and Save** button.

<figure><img src="../../../../.gitbook/assets/S (387).png" alt=""><figcaption><p>Mapping JSON Key-Value Pairs</p></figcaption></figure>

{% hint style="info" %}
**Tip:** You can move single, multiple, or all JSON key-value pairs to the mapper right pane for mapping. Before mapping, if you want to remove any single, multiple, or all selected key-value pairs, move them back to the mapper left pane.&#x20;

See the below table for the procedure.
{% endhint %}

<table><thead><tr><th width="103" valign="top">Button</th><th width="159" valign="top">Name</th><th valign="top">Purpose</th></tr></thead><tbody><tr><td valign="top"><img src="../../../../.gitbook/assets/image (2524).png" alt="" data-size="original"></td><td valign="top">Move Right</td><td valign="top">Selecting a single <strong>JSON key-value pair</strong> and clicking the <strong>Move Right</strong> button to move it to the <strong>mapper</strong> <strong>right pane</strong>, makes it available for mapping.</td></tr><tr><td valign="top"><img src="../../../../.gitbook/assets/image (2521).png" alt="" data-size="original"></td><td valign="top">Move Right All</td><td valign="top">Selecting the <strong>entire JSON object</strong> and then clicking the <strong>Move Right All</strong> button to move it to the <strong>Mapper</strong> <strong>right pane</strong>, makes the entire <strong>JSON object</strong> available for mapping.</td></tr><tr><td valign="top"><img src="../../../../.gitbook/assets/image (2525).png" alt="" data-size="original"></td><td valign="top">Move Back All</td><td valign="top">Selecting the <strong>entire</strong> <strong>JSON object</strong> in the <strong>Mapper right pane</strong> and clicking the <strong>Move Back All</strong> button makes it unavailable for mapping.</td></tr><tr><td valign="top"><img src="../../../../.gitbook/assets/image (2523).png" alt="" data-size="original"></td><td valign="top">Move Back</td><td valign="top">Selecting a single <strong>JSON key-value pair</strong> on the <strong>Mapper Right pane</strong> and clicking the <strong>Move Back</strong> button makes it unavailable for mapping. </td></tr><tr><td valign="top"><img src="../../../../.gitbook/assets/image (2522).png" alt="" data-size="original"></td><td valign="top">Clear All</td><td valign="top">Clicking the <strong>Clear All</strong> button clears the <strong>JSON object</strong> from the Mapper.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the  **JSON to DF** node can be configured correctly and used during execution.

**Procedure**

As part of saving the ETL job, you need to input a **name** and **description** for the pipeline along with specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (388).png" alt="" width="534"><figcaption><p>Saving ETL Job </p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Preview Data</strong></summary>

**Overview:**

The purpose of previewing is to verify that the JSON structure is correctly converted into tabular data before executing the full pipeline.

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step instructions:**

1. On the **Delta Pipelines** page, click the **Edit** icon corresponding to the saved pipeline.&#x20;

<figure><img src="../../../../.gitbook/assets/1 (14).png" alt=""><figcaption><p>Data Pipeline Edit Icon</p></figcaption></figure>

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **JSON to DF** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/1 (15).png" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

The Data frame is displayed on the Preview tab as per the configuration. See the example image below:

<figure><img src="../../../../.gitbook/assets/S (389).png" alt=""><figcaption><p>DF Preview</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="JSON to XML " %}
**Overview**

You can use the **JSON to XML** transform node when the incoming data is in JSON format and must be converted into XML format for consumption by downstream systems or output nodes that require XML.

**Key Concepts:**

<details>

<summary><strong>How JSON  to XML transform node works with an input node</strong></summary>

When connected to an input node, the JSON to XML transform node works as mentioned below:

* First, the system gets data in JSON format
* The JSON to XML node converts the data format
* The structure is adjusted if needed
* The XML is sent to the required destination

</details>

<details>

<summary><strong>Common scenarios for using the JSON  to XML transform node</strong></summary>

The **JSON to XML** transform node is used when:

* Calling SOAP or other XML-based web services
* Integrating with legacy systems or enterprise applications
* Exporting reports or archival documents in XML
* Applying XML-specific validation or schemas
* Interoperation with tools or integrations that expect XML

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The **JSON to XML** transform node works with the below input nodes:&#x20;

* API / GraphQL Input Node
* REST API Input Node
* Webhook Input Node
* JSON File Input Node
* Streaming / Event Input Nodes (JSON-based)

</details>

<details>

<summary><strong>Non-applicable nodes</strong></summary>

The **JSON  to XML** transform node is not applicable to the below input nodes:

* Database Input Nodes
* CSV / Excel / Parquet Input Nodes
* Downstream transform nodes that expect a DataFrame (Filter, Group By, Join, Calculated By, Bulk Columns, etc.)

</details>

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

> <mark style="color:red;">**Note:**</mark> In this procedure, the **File Input node** is used only as an example to show how the **JSON  to DF transform node** works. The same steps apply when using the **JSON to XML** transform node with other input types, such as API / GraphQL Input Node, REST API Input Node, Webhook Input Node, JSON File Input Node, and Streaming / Event Input Nodes (Kafka, etc).

<details>

<summary><strong>Select Input Node</strong></summary>

**Overview:**

As part of adding the **Input Node**, you need to drag it from the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] and then place it on the in the **Main Workspace**. Once placed, the input fields corresponding to the input node are displayed on the left pane. &#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

,The [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] is displayed.&#x20;

3. From the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1], select the **Input Node** in which the JSON file is located (For example, File Input), and drag it onto the **Main Workspace.**&#x20;

<figure><img src="../../../../.gitbook/assets/S (382).png" alt=""><figcaption><p>Selecting File Input Node</p></figcaption></figure>

The Select File Type section is displayed on the left pane.

</details>

<details>

<summary><strong>Select JSON Source</strong> </summary>

**Overview:**

As part of selecting the **JSON source**, you need to browse and locate the file. Once selected, the selected file name is displayed on the input node. If required, you can view the **JSON object** by clicking the **Preview** icon on the top of the input node.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **left pane, f**rom the **Select File Type** drop-down box, select the **required file type**. For example, File Storage.&#x20;
2. From the **Select Storage** drop-down box, select the **storage**.
3. From the **File Extension** drop-down box, select **JSON**.
4. Click the **Connect** button.

The Root folder is displayed.

5. Browse through the **Root** folder to locate the **JSON file**.

<figure><img src="../../../../.gitbook/assets/S (383).png" alt="" width="508"><figcaption><p>Selecting JSON File</p></figcaption></figure>

&#x20;6\. Scroll down to the bottom of **Select File Type** screen, and then click the **Preview** button.&#x20;

<figure><img src="../../../../.gitbook/assets/S (384).png" alt=""><figcaption><p>Select File Type Screen - Preview Button</p></figcaption></figure>

The JSON object is displayed on the Preview tab. &#x20;

<figure><img src="../../../../.gitbook/assets/S (385).png" alt="" width="563"><figcaption><p>JSON Object</p></figcaption></figure>

</details>

<details>

<summary><strong>Connect Input Node with JSON to XML Transform Node</strong></summary>

**Overview:**

The purpose of connecting the input node to the **JSON to XML** transform node is to convert raw JSON data into XML format so that it can be consumed by downstream output nodes or systems that require XML.

**Procedure:**

As part of connecting the input and **JSON to XML** transform nodes, you need to first drag the **JSON to XML** transform node from the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2], and then place it on the **Main Workspace**. Once done, you can connect the input node with the **JSON to XML** transform node.

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Toolbar**, click the **Transform Nodes** menu item.&#x20;

The [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] is displayed.

2. From the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] palette, drag the **JSON to XML** transform node, and drop it onto the **Main Workspace.**
3. Now, drag the **right side** **edge** of the **input node** and connect it to the **left side edge** of **JSON** **to** **XML** transform node as shown in the below image.

<figure><img src="../../../../.gitbook/assets/S (390).png" alt=""><figcaption><p>Connecting Nodes</p></figcaption></figure>

4. Next, save the ETL job. Refer to the next panel.

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the  **JSON to XML** node can be configured correctly and used during execution.

**Procedure**

As part of saving the ETL job, you need to input a **name** and **description** for the pipeline along with specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (391).png" alt="" width="533"><figcaption><p>Saving ETL Job </p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Preview XML</strong></summary>

**Overview:**

The purpose of previewing is to verify that the JSON structure is correctly converted into XML before executing the full pipeline.

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step instructions:**

1. On the **Delta Pipelines** page, click the **Edit** icon corresponding to the saved pipeline.&#x20;

<figure><img src="../../../../.gitbook/assets/S (392).png" alt=""><figcaption><p>Delta Pipeline Edit Icon</p></figcaption></figure>

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **JSON to XML** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (393).png" alt=""><figcaption><p>JSON to XML Preview Icon</p></figcaption></figure>

The XML is displayed on the Preview tab. See the example image below:

<figure><img src="../../../../.gitbook/assets/S (394).png" alt=""><figcaption><p>XML Preview</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="XML to JSON" %}
**Overview**

You can use this transform node when the data coming from the input node is in XML format and the downstream nodes expect JSON.

**Key Concepts:**

<details>

<summary><strong>How XML</strong> <strong>to</strong> <strong>JSON transform node works with an input node</strong></summary>

When connected to an input node, the JSON to XML transform node works as mentioned below:

* Input node receives XML
* Input node hands over XML to the transform node
* Transform node internally reads the XML tree
* Transform node applies **standard conversion logic**
* XML tags will be mapped to a **JSON schema manually**
* Output becomes JSON

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The **XML to JSON** transform node works with the below input nodes:&#x20;

* SOAP Web Service Input
* REST API Input (when response is XML)
* XML File Input, etc.

</details>

<details>

<summary><strong>Non-applicable nodes</strong></summary>

The **XML to JSON** transform node is not applicable to the below input nodes:

* JSON Input / REST API (JSON)
* Relational Database Table Input
* CSV / Flat File Input
* Excel Input
* Kafka / Streaming JSON Input
* Binary / Image / PDF Input

</details>

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Connect XML Input Node to XML to JSON Transform Node</strong></summary>

**Overview:**

The purpose of connecting the input node to the **XML to JSON** transform node is to convert raw XML data into JSON format so that it can be consumed by downstream output nodes or systems that require JSON.

**Procedure:**

As part of connecting the input and **XML to JSON** transform nodes, you need to first drag the **XML to JSON** transform node from the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2], and then place it on the **Main Workspace**. Once done, you can connect the input node with the **XML to JSON** transform node.

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Toolbar**, click the **Transform Nodes** menu item.&#x20;

The [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] is displayed.

2. From the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] palette, drag the **XML to JSON** transform node, and drop it onto the **Main Workspace.**
3. Now, drag the **right side** **edge** of the **input node** and connect it to the **left side edge** of **XML to JSON** transform node as shown in the below image.

<figure><img src="../../../../.gitbook/assets/S (395).png" alt=""><figcaption><p>Connecting Nodes</p></figcaption></figure>

2. Next, save the ETL job. Refer to the next panel.

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

> <mark style="color:red;">**Note:**</mark> If the pipeline is already saved while connecting to another node, there is no need to save it again. When saving is required, the system automatically prompts you to save the pipeline.

**Purpose**

Saving the ETL job confirms the pipeline setup so the **XML to JSON** node can be configured correctly and used during execution.

**Procedure**

As part of saving the ETL job, you need to input a **name** and **description** for the pipeline along with specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (396).png" alt="" width="563"><figcaption><p>Saving ETL Job </p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Preview XML</strong></summary>

**Overview:**

The purpose of previewing is to verify that the XML structure is correctly converted into JSON before executing the full pipeline.

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step instructions:**

1. On the **Delta Pipelines** page, click the **Edit** icon corresponding to the saved pipeline.&#x20;

<figure><img src="../../../../.gitbook/assets/S (397).png" alt=""><figcaption><p>Delta Pipeline Edit Icon</p></figcaption></figure>

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **XML to JSON** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (398).png" alt=""><figcaption><p>XML to JSON Preview Icon</p></figcaption></figure>

The JSON is displayed on the Preview tab. See the example image below:

<figure><img src="../../../../.gitbook/assets/image (2526).png" alt=""><figcaption></figcaption></figure>

</details>
{% endtab %}

{% tab title="JSON Splitter" %}
**Overview**

You can use the **JSON** **Splitter** transform node when the incoming JSON contains **multiple logical records bundled together**, and each record needs to be **processed independently**.

**Key Concepts:**

<details>

<summary><strong>How JSON</strong> <strong>Splitter transform node works with an input node</strong></summary>

When a **JSON Splitter** is connected to an **input node**, it breaks a single JSON payload into **multiple smaller JSON messages**, usually based on a JSON array. Here is how it works:

* Input node provides JSON data
* JSON Splitter receives the JSON payload
* Split path will be configured manually
* JSON is split into multiple messages

</details>

<details>

<summary><strong>Common scenarios for using the JSON</strong> <strong>Splitter transform node</strong></summary>

The **JSON Splitter** transform node is used when:

* JSON contains an array of objects
* Downstream systems expect one JSON object at a time
* Parallel or independent processing is required

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The **JSON Splitter** transform node works with the below input nodes:&#x20;

* REST / API Input
* GraphQL Input
* Webhook Input
* JSON File Input
* Streaming / Event Input nodes

> <mark style="color:red;">**Note:**</mark> The output must be JSON.

</details>

<details>

<summary><strong>Non-applicable nodes</strong></summary>

The **JSON Splitter** transform node cannot be used with the below:

* When input is already structured/tabular
  * Database input nodes
  * CSV / Excel / Parquet input nodes
* When JSON does NOT contain arrays
  * Single JSON object with only key-value pairs (Splitting is not required)

</details>

> <mark style="color:red;">**Note:**</mark> To use the JSON Splitter node, a JSON object with an array must either be available as input or generated using a transform such as DF to JSON.&#x20;

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Connect JSON Object to JSON Splitter Transform Node</strong></summary>

**Overview:**

The purpose of connecting a JSON object to the **JSON Splitter** transform node is to break a single JSON payload into multiple individual JSON objects for independent processing. This is especially useful when the JSON contains arrays and each element needs to be handled separately. It ensures compatibility with downstream nodes or systems that process one JSON object at a time.

**Procedure:**

As part of connecting the input node with the **JSON Splitter** transform node, you need to first drag the **JSON Splitter** transform node from the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2], and then place it on the **Main Workspace**. Once done, you can connect the input node with the **JSON Splitter** transform node.

The information below outlines the step-by-step instructions for completing this task:

> <mark style="color:red;">**Note:**</mark> In the below example, **DF to JSON** node has been shown for example purpose only.

**Step-by-Step Instructions:**

1. On the **Toolbar**, click the **Transform Nodes** menu item.&#x20;

The [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] is displayed.

2. From the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] palette, drag the **JSON Splitter** transform node, and drop it onto the **Main Workspace.**
3. Now, drag the **right side** **edge** of the **JSON** object input node (Here it is DF to JSON) and connect it to the **left side edge** of **JSON** **Splitter** transform node as shown in the below image.

<figure><img src="../../../../.gitbook/assets/S (400).png" alt=""><figcaption><p>Connecting JSON Splitter</p></figcaption></figure>

The Open Splitter button is displayed on the left pane.

</details>

<details>

<summary><strong>Select Key Value Pairs for JSON Splitting</strong></summary>

**Overview:**

The purpose of selecting key-value pairs while during JSON splitting is to control which data is included in the split output. This ensures that only the required fields are processed and passed to downstream nodes. It also helps keep the split JSON objects clean, efficient, and relevant to the intended use case.

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **left pane**, click the **Open JSON Splitter** button.&#x20;

<figure><img src="../../../../.gitbook/assets/S (401).png" alt=""><figcaption><p>Open JSON Splitter Button</p></figcaption></figure>

The **Open JSON Splitter** screen is displayed.

2. On the **Open JSON Splitter** page, click the **Key Path** icon corresponding to the required **JSON Key Value Pairs**. For example, NAME, ADDRESS, and WEBSITE.

<figure><img src="../../../../.gitbook/assets/S (402).png" alt="" width="563"><figcaption><p>Adding Key Value Pairs</p></figcaption></figure>

The selected key value pairs are moved to the right pane.

{% hint style="info" %}
**Tip:** You can select a **single, multiple** or the **entire JSON object** depending on your requirement.&#x20;
{% endhint %}

2. &#x20;On the **right pane**, select the required **key-value pairs**, and then click the **Preview & Save** button.

The JSON Preview & Save dialogue box is displayed.

3. On the **JSON Preview & Save** dialogue box:

* In the **JSON Name** field, enter a **name for the** **JSON split.**
* Click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (403).png" alt=""><figcaption><p>JSON Preview &#x26; Save dialogue box</p></figcaption></figure>

{% hint style="info" %}
**Tip:** If you do not want to save and close the **JSON Preview & Save** dialog box, click the **No** button.
{% endhint %}

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the  **JSON to XML** node can be configured correctly and used during execution.

**Procedure**

As part of saving the ETL job, you need to input a **name** and **description** for the pipeline along with specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (404).png" alt="" width="531"><figcaption><p>Saving ETL Job </p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Preview JSON Split Output</strong></summary>

**Overview:**

The purpose of previewing is to verify that the JSON payload is correctly split into individual JSON objects before executing the full pipeline.

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step instructions:**

1. On the **Delta Pipelines** page, click the **Edit** icon corresponding to the saved pipeline.&#x20;

<figure><img src="../../../../.gitbook/assets/S (405).png" alt=""><figcaption><p>Data Pipeline Edit Icon</p></figcaption></figure>

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **Split** **JSON** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (406).png" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

The JSON split  is displayed on the Preview tab. See the example image below:

<figure><img src="../../../../.gitbook/assets/S (407).png" alt=""><figcaption><p>JSON Split Output</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="EDA" %}
**Overview**

The **EDA transform node** is used for initial data exploration, visualization, and quality checks before in-depth analysis. It is mainly used for **data profiling and validation**, not for data conversion.

You can use this transform node when you want to understand, validate, or check the quality of data before using it further.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * EDA is **read-only analysis.**
> * It does **not modify data.**
> * It is mainly for **understanding and validation.**
> * It is often used in **development and testing**, not always in production.

**Key Concepts:**

<details>

<summary><strong>How EDA transform node works with an input node</strong></summary>

The **EDA** transform node works with an input node as mentioned below:

* Input node provides data
* Data is passed to the EDA transform node
* EDA node analyzes the data
* Output is analysis results

</details>

<details>

<summary><strong>Common scenarios for using the EDA transform node</strong></summary>

Some of the common scenarios for using the EDA transform node includes, when you want to:&#x20;

* Validate source data before processing
* Check data quality (nulls, ranges, outliers)
* Understand new or unknown datasets
* Debug pipelines during development
* Ensure data readiness before ML or analytics

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The **DF to JSON t**ransform node works with input nodes that Output **rows and columns,** Expose a **defined schema, and** Allow column-level access in preview or configuration.

The examples include:

* File inputs (CSV, Excel, Parquet with schema)
* Database table or query inputs
* SAP table / CDS / BW object inputs, etc.

</details>

<details>

<summary><strong>Non-applicable nodes</strong></summary>

The **EDA** transform node is not applicable to the below input nodes:

* | Input Node Type            | Reason            |
  | -------------------------- | ----------------- |
  | XML Input                  | Hierarchical data |
  | JSON Input                 | Nested structure  |
  | SOAP Web Service Input     | XML-based         |
  | Binary / Image / PDF Input | Not analyzable    |
  | Streaming raw events       | Not tabular       |

</details>

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

> <mark style="color:red;">**Note:**</mark> In this procedure, the **Database Input node** is used only as an example to show how the **EDA transform node** works. The same steps apply when using the **EDA** transform node with other input types, such as:
>
> * File inputs (CSV, Excel, Parquet with schema)
> * Database table or query inputs
> * SAP table / CDS / BW object inputs, etc.

<details>

<summary><strong>Add Input Node</strong> </summary>

**Overview:**

As part of adding the **Input Node**, you need to drag it from the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] and then place it on the in the **Main Workspace**. Once placed, the input fields corresponding to the input node are displayed on the left pane.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

,The [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] is displayed.&#x20;

3. From the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1], select the **Input Node** (For example, Database Input), and drag it onto the **Main Workspace.**&#x20;

<figure><img src="../../../../.gitbook/assets/S (339).png" alt="" width="507"><figcaption><p>Adding Input Node</p></figcaption></figure>

The Database Type and Scheme Properties sections are displayed in the left pane.&#x20;

</details>

<details>

<summary><strong>Select Necessary Columns</strong></summary>

**Purpose:**

After placing the input node, select the required columns so that they are available and visible when the input node is connected to the **DF to JSON** transform node.&#x20;

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Left Pane,** from the **Database Type** drop-down box, select either **Datasource** or **Assets.** For example, **Datasource.**&#x20;

{% hint style="info" %}
**Tip:** Selecting the **Datasource** option connects to an external database whereas the **Assets** option use pre-configured datasets stored within SCIKIQ.&#x20;
{% endhint %}

2. From the **Datasource** drop-down box, select the required **datasource.**

<figure><img src="../../../../.gitbook/assets/S (340).png" alt=""><figcaption><p>Selecting Database Type and Connection</p></figcaption></figure>

3\. In the **Schema properties** section, select the required **columns**, and then click the **Save** icon.

> <mark style="color:red;">**Note:**</mark> Be sure to save the configuration; otherwise, the selected columns will not be available when the input node is connected to the **Value Mapper** transform node.

<figure><img src="../../../../.gitbook/assets/S (341).png" alt="" width="563"><figcaption><p>Selecting Columns</p></figcaption></figure>

{% hint style="info" %}
**Tip:** You can select a **single column, multiple columns,** or **all columns** based on your requirement. Selecting the **Select All** checkbox allows you to select all columns at once. See the **ticked checkbox** in the image below.
{% endhint %}

</details>

<details>

<summary><strong>Connect Input Node with EDA Transform Node</strong></summary>

**Overview:**

The **purpose** of connecting an **input node** with the **EDA** transform node is to convert the structured, tabular data produced by the input node into XML format, enabling its use in XML-based integrations, storage, and downstream processing.

**Procedure:**

As part of connecting the input and **EDA transform** nodes, you need to first drag the **EDA transform node** from the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2], and then place it on the **Main Workspace**. Once done, you can connect the input node with the **EDA** **transform node**.

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Toolbar**, click the **Transform Nodes** menu item.&#x20;

The [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] is displayed.

2. From the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] palette, drag the **EDA** **transform node**, and drop it onto the **Main Workspace.**
3. Now, drag the **right side** **edge** of the **input node** and connect it to the **left side edge** of **EDA** **transform node** transform node as shown in the below image.

<figure><img src="../../../../.gitbook/assets/S (408).png" alt=""><figcaption><p>Connecting Nodes</p></figcaption></figure>

The Exploratory Analysis section is displayed on the left pane.

</details>

<details>

<summary><strong>Configure Table and Version</strong></summary>

**Purpose:**

Configuring the Table and Version in the EDA transform identifies the specific database dataset and its execution snapshot to be analyzed, ensuring accurate, consistent, and reproducible exploratory data analysis results.

**Procedure:**

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. On the **Left Pane**, in the **Exploratory Data Analysis** section:

A. From the **Table** drop-down box, select the **required table** to identify the specific datase&#x74;**.** For example, Customers.

B. From the **Version Drop** drop-down box, select the version. For example, Default Version.

<figure><img src="../../../../.gitbook/assets/S (409).png" alt=""><figcaption><p>Selecting Table and Version</p></figcaption></figure>

2. Save the **ETL** job. Refer to the next panel.

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the  **EDA** node can be configured correctly and used during execution.

**Procedure**

As part of saving the ETL job, you need to input a **name** and **description** for the pipeline along with specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (410).png" alt="" width="527"><figcaption><p>Saving ETL Job </p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Preview Data</strong></summary>

**Overview:**

The **purpose** of previewing when applying the EDA with an input node is to verify that the Output data is generated as expected.

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step instructions:**

1. On the **Delta Pipelines** page, click the **Edit** icon corresponding to the saved pipeline.&#x20;

<figure><img src="../../../../.gitbook/assets/S (377).png" alt=""><figcaption><p>Delta Pipelines Page - Clicking Edit Icon</p></figcaption></figure>

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **EDA** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (411).png" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

The explored data is displayed on the left pane as shown in the below image:

<figure><img src="../../../../.gitbook/assets/S (412).png" alt=""><figcaption><p>Explored Data</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="Bulk Columns" %}
**Overview**

You can use the **Bulk Columns** transform node when you want to automatically create multiple consistently named columns from a single input column to reduce manual effort.

**Key Concepts:**

<details>

<summary><strong>How Bulk Columns</strong> <strong>transform node works with an input node</strong></summary>

* The input node reads data from the source system and outputs it in a **tabular format** consisting of rows and columns.
* Once connected, the **Bulk Columns** transform node **accesses all columns** exposed by the input node and allows you to **select one or more source columns** for bulk processing.
* You can then define the **bulk configuration**, which includes:
  * The source column(s) to be processed
  * The number of columns to be created or modified
  * The column naming pattern, such as a prefix or suffix
  * Optional behaviors, such as transposing the output to columns
* After processing, the transform node generates an output that contains:
  * All original input columns
  * Along with the newly created or modified bulk columns

</details>

<details>

<summary><strong>Common scenarios for using the Bulk Columns</strong> <strong>transform node</strong></summary>

Some of the common scenarios for using **Bulk Columns** transform node includes when:

* When one column needs to be expanded into several columns using a consistent pattern
* When identical logic must be applied across multiple fields. For example, Formatting multiple numeric columns and Standardizing multiple string columns
* When working with wide datasets that would otherwise require repetitive configuration

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The Bulk Columns transform node can be used with **any input node that outputs structured, column-based data**, such as:

* File-based inputs (CSV, Excel, Parquet)
* Database inputs (SQL, NoSQL tables or views)
* API / REST / GraphQL inputs (parsed responses)
* SAP input nodes (Tables, CDS, BW objects)
* Streaming or batch data sources with schema
* Cloud storage inputs with defined columns

</details>

<details>

<summary><strong>Non-applicable nodes</strong></summary>

The **Bulk Columns** transform node **cannot be used** with input nodes that:

* Do not output tabular data
* Output raw or unstructured data
* Do not expose columns

</details>

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

> <mark style="color:red;">**Note:**</mark> In this procedure, the **Database Input node** is used only as an example to show how the **Bulk Columns transform node** works. The same steps apply when using the **Bulk Columns** transform node with other input types, such as:
>
> * File-based inputs (CSV, Excel, Parquet)
> * Database inputs (SQL, NoSQL tables or views)
> * API / REST / GraphQL inputs (parsed responses)
> * SAP input nodes (Tables, CDS, BW objects)

<details>

<summary><strong>Add Input Node</strong> </summary>

**Overview:**

As part of adding the **Input Node**, you need to drag it from the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] and then place it on the in the **Main Workspace**. Once placed, the input fields corresponding to the input node are displayed on the left pane.&#x20;

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create Delta Pipeline**.

The Create Delta Pipeline page is displayed.

2\. On the **Create Delta Pipeline** page, click the **Input Menu** item.

,The [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1] is displayed.&#x20;

3. From the [<mark style="color:blue;">**Input Node Palette**</mark>](#user-content-fn-1)[^1], select the **Input Node** (For example, Database Input), and drag it onto the **Main Workspace.**&#x20;

<figure><img src="../../../../.gitbook/assets/S (339).png" alt="" width="507"><figcaption><p>Adding Input Node</p></figcaption></figure>

The Database Type and Scheme Properties sections are displayed in the left pane.&#x20;

</details>

<details>

<summary><strong>Select Necessary Columns</strong></summary>

**Purpose:**

After placing the input node, you need to select the required columns so that they are available and visible when the input node is connected to the **Calculated Field** transform node.&#x20;

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Left Pane,** from the **Database Type** drop-down box, select either **Datasource** or **Assets.** For example, **Datasource.**&#x20;

{% hint style="info" %}
**Tip:** Selecting the **Datasource** option connects to an external database whereas the **Assets** option use pre-configured datasets stored within SCIKIQ.&#x20;
{% endhint %}

2. From the **Datasource** drop-down box, select the required **datasource.**

<figure><img src="../../../../.gitbook/assets/S (340).png" alt=""><figcaption><p>Selecting Database Type and Connection</p></figcaption></figure>

3\. In the **Schema properties** section (See the below image):

* From the **Table** drop-down box, select the **required table**.
* Select the required **columns**.

{% hint style="info" %}
**Tip:** You can select a **single column, multiple columns,** or **all columns** based on your requirement. Selecting the **Select All** checkbox allows you to select all columns at once. See the **top** **ticked checkbox** in the image below.
{% endhint %}

* Enable the **Distinct** option to **remove the duplicates**, if any.
* Click the **Save** button (below the **Distinct** option) to save the configuration.

> <mark style="color:red;">**Note:**</mark> Be sure to save the configuration; otherwise, the selected columns will not be available when the input node is connected to the **Calculated Field** transform node.

<figure><img src="../../../../.gitbook/assets/S (413).png" alt=""><figcaption><p>Selecting Columns</p></figcaption></figure>

</details>

<details>

<summary><strong>Connect Input Node with Bulk Columns Transform Node</strong></summary>

**Overview:**

Connecting the **input node** with the **Bulk Columns** transform node enables bulk creation of columns using structured source data, improving efficiency and consistency in the pipeline.

**Procedure:**

As part of connecting the **input** and **Bulk Column** transform nodes, you need to first drag the **Bulk Column** transform node from the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2], and then place it on the **Main Workspace**. Once done, you can connect the input node with the **Bulk Column** transform node.

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Toolbar**, click the **Transform Nodes** menu item.&#x20;

The [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] is displayed.

2. From the [<mark style="color:blue;">**Transform**</mark>  <mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-2)[^2] palette, drag the **Bulk Column** transform node, and drop it onto the **Main Workspace.**
3. Now, drag the **right side** **edge** of the **input node** and connect it to the **left side edge** of **Bulk Column** transform node as shown in the below image.

<figure><img src="../../../../.gitbook/assets/S (414).png" alt=""><figcaption><p>Connecting Nodes</p></figcaption></figure>

Once the nodes are connected, the Create **Columns from Column Value** section appears on the left pane.

</details>

<details>

<summary><strong>Configure Column Inputs</strong></summary>

**Purpose:**

Configuring **Column Inputs** controls **which column is used, how many new columns are created, how they are named, and whether they remain as columns or are transposed into rows**. This ensures the bulk output is **consistent and ready for downstream use**.

**Procedure:**

As part of configuring the **Column Inputs**, you need to select the required **Column**, **Number of columns, Column Prefix A**, and specify **Transpose to column**. &#x20;

The below step-by-step instructions describe the procedure:&#x20;

**Step-by-Step instructions:**

1. On the **Left Pane**, in the **Create Columns from Column Values** section:

* From the  **Columns** drop-down box, select the **required column**. For example, Status. &#x20;



{% hint style="success" icon="grid-4" %}
**Purpose:** The selected column will be used to generate new columns.
{% endhint %}

* In the **No. of Columns** drop-down box, enter the **required number of columns**. For example, 3.

{% hint style="success" icon="grid-4" %}
**Purpose:** The **No. of Columns** field defines **the number columns created** from the selected source column.
{% endhint %}

* In the **Column Prefix** field, enter the **prefix.**

{% hint style="success" icon="grid-4" %}
**Purpose:** Specifying **Column Prefix** helps to identify columns created by this transformation.
{% endhint %}

* From the **Transpose to Column** drop-down box, select **True** or **False** depending on the requirement.

{% hint style="success" icon="grid-4" %}
**Purpose:** Selecting **False** makes the new columns remain as separate columns. If True is selected, then new columns are converted into rows (long format).
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (415).png" alt=""><figcaption><p>Inputting Column Details</p></figcaption></figure>

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the **Bulk Columns** transfrom node can be configured correctly and used during execution.

**Procedure**

As part of saving the ETL job, you need to input a **name** and **description** for the pipeline along with specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (416).png" alt="" width="536"><figcaption><p>Saving Pipeline</p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Preview Data</strong></summary>

**Overview:**

The purpose of previewing when applying the **Bulk Columns** transform node with an input node is to verify that the output data is generated correctly according to the specified inputs before executing the full pipeline.

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step instructions:**

1. On the **Delta Pipelines** page, click the **Edit** icon corresponding to the saved pipeline.&#x20;

<figure><img src="../../../../.gitbook/assets/S (417).png" alt=""><figcaption><p>Delta Pipelines Page - Edit Icon  </p></figcaption></figure>

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **Bulk Columns** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (418).png" alt=""><figcaption></figcaption></figure>

The columns are generated as per the specified inputs and displayed on the Preview tab. See the example image below:

</details>
{% endtab %}
{% endtabs %}

### Related Topics

* [**Configuring Input Nodes**](configuring-input-nodes.md)
* [**Using Output Nodes**](../using-output-nodes/)

[^1]: The **Input Node Palette** contains a set of input nodes, including Database Input, File Input, Query Input, API, GraphQL, SAP APP, NoSQL, and UCM File Loader.

[^2]: The **Transform Node Palette** contains a set of transform nodes including Filter By, Calculated By, Order By, Limit By, Group By, Value Mapper, Select, Calculated Field, JSON to DF, XML to JSON,    \
    JSON to XML, XML to DF, DF to XML, JSON Splitter, EDA, Binning, Bulk Columns, DF Rules, and DF to Jaon.

[^3]: Ascending&#x20;

[^4]: Descending
