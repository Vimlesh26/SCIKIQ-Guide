# Using Kafka Producer Output Node

This page explains how to use the **Kafka Producer** node with an input node. A **Kafka Producer** can be used with an **input node** when the pipeline needs to **publish incoming or processed data as events to a Kafka topic**. This is useful for real-time integrations, event-driven architectures, and streaming use cases where downstream systems consume data through Kafka.

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

Connecting the **Kafka Producer** output node to an input node involves a sequence of steps. The table below provides a brief overview of each step in the process.

<table><thead><tr><th width="221">Step</th><th valign="top">Description</th></tr></thead><tbody><tr><td><a href="using-kafka-producer-output-node.md#add-input-node">Add Input Node</a></td><td valign="top">This is the first step in applying  <strong>Kafka Producer output node</strong> to an input node. As part of this, you will drag the required input node from the <a data-footnote-ref href="#user-content-fn-1"><mark style="color:blue;">Input Node Palette</mark></a> and then place it on the <strong>Main Workspace.</strong></td></tr><tr><td><a href="using-kafka-producer-output-node.md#select-necessary-columns">Select Necessary Columns</a> </td><td valign="top">After placing the input node, you will select the <strong>necessary  columns</strong> pertaining to the source. This is to make them appear when input node is connected with the <strong>Kafka Producer output</strong> node. </td></tr><tr><td><a href="using-kafka-producer-output-node.md#connect-kafka-producer-output-node-to-an-input-node">Connect <strong>Kafka Producer</strong> Output Node to Input Node</a></td><td valign="top">As part of this step, you will drag the <strong>Kafka Producer output</strong> node from the  <a data-footnote-ref href="#user-content-fn-2"><mark style="color:blue;"><strong>Output Node Palette</strong></mark></a> and then place it on the <strong>Main Workspace</strong>. Once done, you can connect both the <strong>Input</strong> and  <strong>Kafka Producer output</strong> nodes.</td></tr><tr><td><a href="using-kafka-producer-output-node.md#configure-kafka-connection">Configure Kafka Connection</a></td><td valign="top">Subsequent to connecting the input node and <strong>Kafka Producer output</strong> node, you will configure <strong>Kafka Connection.</strong> Configuring a <strong>Kafka connection</strong> allows the pipeline to communicate with the Kafka cluster. It defines the broker address and required connection settings so that the pipeline can publish or consume messages from Kafka topics.</td></tr><tr><td><a href="using-kafka-producer-output-node.md#configure-kafka-topic">Configure Kafka Topic</a></td><td valign="top">As part of this step, you will configure the <strong>Kafka topic</strong>, which  identifies the specific topic in the Kafka cluster where the pipeline will send its messages. This ensures that the published data flows into the intended event stream for downstream consumers.</td></tr><tr><td><a href="using-kafka-producer-output-node.md#set-output-format">Set Output Format</a></td><td valign="top">Setting the <strong>Output Format</strong> determines the encoding and structure of messages before they are sent to the Kafka topic. This ensures that the data is formatted in a way that downstream Kafka consumers can correctly read and process.</td></tr><tr><td><a href="using-kafka-producer-output-node.md#save-etl-job">Save ETL Job</a></td><td valign="top">After selecting the columns, you will save the <strong>ETL job</strong> to confirm the pipeline setup. This ensures that the <strong>Kafka Producer output</strong> node is configured correctly and can be used effectively during execution. Once saved, the pipeline is displayed on the <strong>Data Pipelines</strong> page.</td></tr><tr><td><a href="using-kafka-producer-output-node.md#run-and-preview">Run &#x26; Preview</a></td><td valign="top"><strong>Run &#x26; Preview</strong> is used to execute the pipeline and check whether the data from the input node is being correctly sent to the Kafka topic. It helps confirm that the configuration is working as expected before deploying or finalizing the pipeline.</td></tr><tr><td><a href="using-kafka-producer-output-node.md#post-execution">Post Execution</a></td><td valign="top">Post execution, you can verify that the pipeline has successfully published messages to the Kafka topic by checking the Kafka server or topic logs after execution.</td></tr></tbody></table>

***

## Procedure

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

> <mark style="color:red;">**Note:**</mark> **Prerequisites for Using the Kafka Producer Node**
>
> * A Kafka connection must be configured in the system, or it can be created during node configuration.
> * The input data must be in a JSON-compatible structure before being sent to Kafka.
> * If the Avro message format is used, the corresponding Avro schema must be defined.

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
