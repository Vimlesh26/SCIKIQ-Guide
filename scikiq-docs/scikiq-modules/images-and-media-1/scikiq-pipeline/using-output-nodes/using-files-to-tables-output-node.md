# Using Files to Tables Output Node

This page explains how to use the **Files to Tables Output node** with an input/transform node. You The **Files to Tables Output node** can be used to **store pipeline data into one or more database tables by writing the output into files and then loading those files into tables**. It is typically used when large volumes of data need to be efficiently written to database tables.

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

<summary><strong>Non-applicable Input and Transfrom nodes</strong></summary>

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

Connecting the **Files to Table Output Node** to an **input node** involves a sequence of steps. The table below provides a brief overview of each step in the process.

<table><thead><tr><th width="221">Step</th><th valign="top">Description</th></tr></thead><tbody><tr><td><a href="using-files-to-tables-output-node.md#add-input-node">Add input Node</a></td><td valign="top">This is the first step in connecting <strong>Files to Table</strong> output node to an input node. As part of this step, you will drag the required input node from the <a data-footnote-ref href="#user-content-fn-1"><mark style="color:blue;"><strong>Input Node Palette</strong></mark></a> and then place it on the in the <strong>Main Workspace.</strong></td></tr><tr><td><a href="using-files-to-tables-output-node.md#configure-input-node-settings">Configure input Node Settings</a></td><td valign="top">After adding the input node (In this example, it is UCM File Loader) on the <strong>Main Workspace</strong>, you will configure its settings, which  include <strong>Connection, File Storage Connection, File Storage Folder/Bucket, UCM Process,</strong> and <strong>Process Table.</strong></td></tr><tr><td><a href="using-files-to-tables-output-node.md#connect-files-to-tables-output-node-to-input-node">Connect Files to Tables Output Node to input Node </a></td><td valign="top"><p>Subsequent to configuring the input node settings, you will drag the <strong>Files to Tables output node</strong> from the  <a data-footnote-ref href="#user-content-fn-2"><mark style="color:blue;"><strong>Output Node Palette</strong></mark></a> and then place it on the <strong>Main Workspace</strong>. Once done, you can connect both the Input/Transform and Output nodes. </p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> Connecting <strong>Transform</strong> node is optional.</p></td></tr><tr><td><a href="using-files-to-tables-output-node.md#configure-files-to-tables-output-node-settings">Configure  Files to Tables Output Node Settings</a></td><td valign="top">After connecting the <strong>Files to Tables output node</strong> to the <strong>input node</strong>, you will configure  Files to Tables output node settings, which include  <strong>File Storage Connection, File Extension,</strong> and <strong>Database Connection.</strong></td></tr><tr><td><a href="using-files-to-tables-output-node.md#save-etl-job">Save ETL Job</a></td><td valign="top">Before running the pipeline, you will save the <strong>ETL job</strong> to confirm the pipeline setup. This ensures that the <strong>Files to Tables</strong> output node is configured correctly and can be used effectively during execution. Once saved, the pipeline is displayed on the <strong>Data Pipelines</strong> page.</td></tr><tr><td><a href="using-files-to-tables-output-node.md#run-pipeline">Run Pipeline</a></td><td valign="top">Finally, you will run the pipeline to execute the complete data loading process, ensuring that the files identified by the input node are read and their data is loaded into the corresponding database tables.</td></tr></tbody></table>

***

## Procedure

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

> <mark style="color:red;">**Note:**</mark> In this procedure, **UCM File Loader** input node is used as an example to demonstrate how the **Files to Tables** output node works. However, the same process applies when using the **Files to Tables Output Node** with other input types, Database Input Node, File Input Node (CSV, JSON, XML), and API Input Node.

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

## Related Topics

* [Configuring Input Nodes](/broken/pages/Qe52MzyFrHp43dWO41kf)
* [Configuring Transform Nodes](/broken/pages/hbzg9uHn194g3ivtwx4q)

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
