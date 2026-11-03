# Using File Output Node

This page explains how to use the **Table Output** node with an input/transform node. The File Output Node is used when the pipeline results need to be saved in a file format such as **CSV, Excel, JSON, or other supported formats**. It writes the output generated after data processing and transformations to a specified file location.

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

Connecting the  **Table Output** node to an input node involves a sequence of steps. These steps include [Connect Table Output Node](using-file-output-node.md#connect-table-output-node), [Configure Input Node,](using-file-output-node.md#configure-input-node) [Configure Transform Node (Optional),](using-file-output-node.md#configure-transform-node-optional) [Configure Table Output Node,](using-file-output-node.md#configure-table-output-node) [Save ETL Job](using-file-output-node.md#save-etl-job) and [Preview Data.](using-file-output-node.md#preview-data)

***

## Procedure

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Connect File Output Node</strong></summary>

**Purpose:**

The purpose of connecting a **File Output node** to an **Input/Transform node** is to **write the processed pipeline data** into file format such as **CSV, Excel, JSON, or other supported formats**..

**Procedure:**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

* On the **Right Pane**, place the **Input node, Transform node,** and **Table Output node** and then connect them.

> <mark style="color:red;">**Note:**</mark> Make sure you have added at least one input or transformation node to the canvas before continuing.

<figure><img src="/broken/files/PRUYQJI12lCKAe31NBiU" alt=""><figcaption><p>Connecting File Output Node</p></figcaption></figure>

</details>

<details>

<summary><strong>Select File Storage Type, Connection, and Target Bucket</strong> </summary>

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

</details>

<details>

<summary><strong>Set File Path and Format</strong></summary>

A. On the **Select File Type** screen, scroll down to the **Root section.**

B. In the **File Name** field, enter a **name** for the file.

C. From the File Format area, select the firle format. For example, CSV.

<figure><img src="/broken/files/7BOnroCgdQJgdq5Jxjt8" alt=""><figcaption><p>Specifying File Name and Format</p></figcaption></figure>

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

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Preview Data</strong></summary>

* On the **Right Pane**, click the **Preview** icon on the top of **File** **Output** node.

The file output is displayed.&#x20;

</details>

## Related Topics

* [Configuring Input Nodes](/broken/pages/Qe52MzyFrHp43dWO41kf)
* [Configuring Transform Nodes](/broken/pages/hbzg9uHn194g3ivtwx4q)
