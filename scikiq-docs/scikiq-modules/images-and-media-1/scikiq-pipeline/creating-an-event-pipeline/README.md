---
icon: chart-network
---

# Creating an Event Pipeline

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

**Purpose**

Event Pipelines in SCIKIQ are designed to process data in real time based on specific events or triggers. They automatically initiate data processing as soon as an event occurs, enabling systems to respond immediately without waiting for scheduled runs.

**Advantages**

Event Pipelines provide low-latency data processing and support high-frequency data flows. They enable faster decision-making, improve system responsiveness, and are well-suited for building reactive and event-driven applications.

**Ideal Scenarios**

Event Pipelines are ideal for use cases such as real-time monitoring, alerts and notifications, streaming data processing, user activity tracking, and system-to-system integrations where timely data handling is critical.

***

### Procedure

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Configure Topic Node</strong></summary>

**Purpose:**

In **SCIKIQ’s Event Pipeline**, the **Topic Node** is a mandatory component that serves as the primary input for event-driven processing. It continuously listens to configured Kafka topics and ingests event data streams in real time.&#x20;

The **Topic Node** can be connected to downstream transformation or analytics nodes, enabling real-time data processing and the generation of actionable insights.

**Procedure:**

The procedure to configure the Kafka Topic node includes adding the Kafka Topic node from the right pane, configuring the required node settings, and previewing the data.

The following step-by-step instructions will guide you through the configuration process:

**Step-by-Step Instructions**

**1.Adding Kafka Topic Node**

A. On the **Left Navigation Bar**, expand **SCIKIQ Delta Hub** under **SCIKIQ CONNECT**, and then click **Click Create API.**

The Create Event Pipeline page is displayed.

B. On the **Create Event Pipeline** page, click the **Input tab** on the **Top Toolbar.**&#x20;

The [<mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-1)[^1] is displayed.

C. From the [<mark style="color:blue;">**Node Palette**</mark>](#user-content-fn-1)[^1], drag the **Topic Node** onto the **Right Pane (Main Workspace),** and then select it.

<figure><img src="../../../../.gitbook/assets/S (254).png" alt=""><figcaption><p>Selecting Topic Node</p></figcaption></figure>

The Topic input fields are displayed on the left pane.

**2.Configuring Node Settings**

A. On the **Left Pane**, from the **Connection** drop-down box, select **Kafka Connection**.

{% hint style="info" %}
**Tip:** Selecting the **Kafka Connection** selects the Kafka cluster to connect to and defines how the pipeline securely communicates with Kafka brokers.
{% endhint %}

B. From the **Kafka Topics** drop-down box, select the **required topic**.

{% hint style="info" %}
**Tip:** Selecting the **Topic** specifies the event stream from which the pipeline consumes messages for real-time processing.
{% endhint %}

C. From the **Offset** drop-down box, select either **Latest** or **Earliest.**

{% hint style="info" %}
**Tip:** Selecting **Offset**  determines the starting point for reading messages from the Kafka topic, such as consuming only latest events or earliest ones.
{% endhint %}

D. From the **Message Format** drop-down box, select the **required format.**

{% hint style="info" %}
Tip: Selecting the **Message Format** defines how incoming Kafka messages are structured (for example, Avro), enabling correct deserialization and field extraction.
{% endhint %}

E. In the **Kafka Topic Columns** section, select the required columns.

{% hint style="info" %}
**Tip:**&#x20;

* Selecting **Kafka Topics** displays the data fields available in the Kafka messages and allows you to select and map the fields that will be used for downstream transformations and analytics.
* You can select a **single, multiple,** or **all** the columns based on the requirement.
{% endhint %}

F. Click the **EDA** button if you want to apply the **DQ Rules**.

<figure><img src="../../../../.gitbook/assets/S (255).png" alt=""><figcaption><p>Configuring Topic Settings</p></figcaption></figure>

**3.Previewing**

* On the **Right Pane**, click the **Preview** icon on the top of **Kafka Topic node.**

<figure><img src="../../../../.gitbook/assets/S (256).png" alt=""><figcaption><p>Clicking  Preview Icon</p></figcaption></figure>

The message is displayed.

</details>

<details>

<summary><strong>Configure Input Nodes</strong></summary>

The **Input node** defines **where the data originates** for the API pipeline. It is used to establish the connection to the source system and specify what data should be ingested (such as tables, files, or queries). Proper configuration ensures that only the intended data enters the pipeline. It also supports incremental logic by identifying which records should be considered new or updated.&#x20;

> <mark style="color:red;">**Note:**</mark> The steps to configure input nodes are the same for Delta, API, and Event Pipelines. If you need guidance while creating an API pipeline, you can refer to the input node help topics available for Delta Pipelines by clicking the [Configuring Input Nodes](/broken/pages/Qe52MzyFrHp43dWO41kf) link. These instructions apply equally to API and Event pipelines and can be used as a reference.

</details>

<details>

<summary><strong>Configure Transform Nodes</strong></summary>

The **Transform node** defines **how the data is modified, enriched, or processed** within the pipeline. It is used to apply business logic such as calculations, data mappings, formatting, cleansing, and rule-based transformations. This ensures that raw data is converted into meaningful and usable information. Proper transformation design is essential for accurate analytical and operational outcomes.

> <mark style="color:red;">**Note:**</mark> The steps to configure transform nodes are the same for Delta, API, and Event Pipelines. If you need guidance while creating an API pipeline, you can refer to the transform node help topics available for Delta Pipelines by clicking the [Configuring Transform Nodes](/broken/pages/hbzg9uHn194g3ivtwx4q) link. These instructions apply equally to API and Event pipelines and can be used as a reference.

</details>

<details>

<summary><strong>Configure Output Nodes</strong></summary>

The **Output node** defines **where the processed data is written** after transformations are applied. It ensures that data is delivered to the correct target system, table, or asset with the expected structure. Proper configuration helps maintain data integrity and consistency in the destination. It also supports controlled data publishing for downstream consumption.

> <mark style="color:red;">**Note:**</mark> The steps to configure output nodes are the same for Delta, API, and Event Pipelines. If you need guidance while creating an API pipeline, you can refer to the output node help topics available for Delta Pipelines by clicking the [Configuring Output Nodes](/broken/pages/BOHoiMbsoFJCedoWAASx) link. These instructions apply equally to API and Event pipelines and can be used as a reference.

</details>

<details>

<summary><strong>Configure Execution Settings</strong></summary>

The **Execution Settings** control **how and when the pipeline runs**. This includes parameters such as execution mode, scheduling behavior, performance settings, and error-handling behavior. Proper configuration ensures reliable execution, optimal resource usage, and predictable pipeline behavior. It also supports operational stability in production environments.

To learn how to configure execution settings, click [Configuring Execution Settings](/broken/pages/bMvbRwIJsSoqTGw56zkQ).

</details>

<details>

<summary><strong>Configure Parameters</strong></summary>

The **Parameters** allow the pipeline to be **dynamic and reusable** by accepting values at runtime instead of hardcoding them. They are commonly used for filters, dates, file paths, environment values, or thresholds. This improves flexibility and allows the same pipeline to be used across different scenarios. Proper parameterization also supports automation and operational scalability.

To learn how to configure parameters, click [Configuring Parameters.](/broken/pages/kse9wST2LBLHaoyHSM6Z)

</details>

***

### Related Topics

* [**Managing Event Pipelines**](../managing-event-pipelines.md)

[^1]: 

    **Input Nodes' Description**



    * **Database Input** – Extracts structured data from relational databases
    * **File Input** – Reads data from files like CSV, Excel, JSON, or XML
    * **Query Input** – Fetches data by running custom SQL queries
    * **API Input** – Pulls data from external applications using REST APIs
    * **GraphQL Input** – Retrieves data using flexible GraphQL queries
    * **SAP APP Server Input** – Connects to SAP systems to extract business data
    * **NoSQL Input** – Reads data from NoSQL databases such as MongoDB
    * **UCM File Loader** – Loads files stored in UCM repositories into the pipeline
