---
icon: hubspot
---

# SCIKIQ Pipeline

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

A data pipeline is a system that **collects, processes, and delivers data** from sources to destinations automatically.&#x20;

SCIKIQ Pipelines are a high-powered system designed to manage how your data moves and transforms. Instead of using multiple separate tools, SCIKIQ provides a single, visual framework to coordinate your entire data workflow from start to finish.&#x20;

In short, SCIKIQ Pipelines don't just move data from point A to point B—they activate your data, turning scattered information into ready-to-use business value.&#x20;

The **ScikIQ Pipeline Editor** is a simple visual tool for creating and running data workflows. Using **drag-and-drop** and clear panels, you can easily build and manage even complex pipelines.

***

### Key Information

<details>

<summary>Primary Objectives</summary>

SCIKIQ Pipelines are designed to transform how your organization handles data by focusing on the below mentioned primary objectives:

| Objectives             | Description                                                                                                            |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| Unified Integration    | Connect all disparate sources—like databases, APIs, SAP, and files—through a single, standardized interface.           |
| Real-Time Processing   | Shift from slow batch reloads to incremental updates, ensuring your data is always current with minimal system strain. |
| Data Activation        | Move beyond storage by using real-time APIs and event-triggers to turn data into immediate business actions.           |
| Operational Automation | Eliminate manual, error-prone tasks with intelligent scheduling and reliable, script-free workflows.                   |
| Total Transparency     | Gain full visibility into data lineage and execution status to ensure data trust and regulatory compliance.            |

</details>

<details>

<summary>Difference from Traditional Tools</summary>

Here is a precise, simplified comparison to show how SCIKIQ Pipelines modernize the traditional data process.

| Key Difference               | Description                                                                                                                                              |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| One Platform for All Data    | Instead of separate tools for different speeds, SCIKIQ unifies Real-Time, Batch, and Event-Driven data in a single system.                               |
| Visual, Script-Free Building | You don't need to write complex code. A "No-Code" interface allows both IT professionals and business users to collaborate and build workflows visually. |
| Bridge Any Environment       | It offers Hybrid Flexibility, meaning it can move data effortlessly between your physical office servers (on-premises) and the cloud.                    |

</details>

<details>

<summary>Benefits</summary>

| Benefit             | Description                                                                                |
| ------------------- | ------------------------------------------------------------------------------------------ |
| Automated Workflows | Save time by automating how data is collected and cleaned.                                 |
| Instant Insights    | Deliver data the moment it’s created using real-time triggers.                             |
| No More Silos       | Connect fragmented data from different departments into one cohesive "intelligent" stream. |

</details>

### **Pipeline Types**

{% tabs %}
{% tab title="Delta Pipelines" %}
**Overview**

**What is a delta pipeline?**

A **Delta Pipeline** is a data pipeline designed to **process only the data that has changed** since the last execution, instead of reprocessing the entire dataset.

**Main goal**

The main goal of a Delta Pipeline is to support **incremental and periodic data updates**, especially when:

* Full data reloads are not practical
* Tracking changes (inserts, updates, deletes) using [<mark style="color:blue;">**Change Data Capture (CDC)**</mark>](#user-content-fn-1)[^1] is required
* Data needs to be refreshed on a regular schedule (hourly, daily, weekly)

**Benefits**

The benefits include - faster processing, reduced system load, and reduced duplicate data. &#x20;

**Suitable jobs**

It is best suited for [<mark style="color:blue;">**scheduled**</mark>](#user-content-fn-2)[^2] or [<mark style="color:blue;">**batch jobs**</mark>](#user-content-fn-3)[^3] where running full data loads frequently is inefficient.&#x20;

**Key Features**

The features of a delta pipeline includes:

* Supports [<mark style="color:blue;">**CDC**</mark>](#user-content-fn-4)[^4] from databases and files
* Allows **filtering using parameters** (e.g., timestamp, row version, last updated date)
* Can run **manually or on a schedule**
* Offers a **drag-and-drop interface** for faster development
* Supports **pipeline versioning** for flexibility and reuse

**Key Components**

The components a delta pipeline includes:

* **Input Nodes (Mandatory)**: Sources like Database Input, File Input, SAP App Server, Query Input, or NoSQL.
* **Transformation Nodes (Optional)**: Apply logic such as joins, filters, expressions, or conditional mappings.
* **Output Nodes (Mandatory)**: Target systems like RDBMS, cloud databases, APIs, or file sinks.

**Common Use Cases**

&#x20;The common use case include

* Extracting ERP data changes for reporting systems
* Updating analytics systems with incremental inventory changes
* Daily synchronization of customer data from CRM to Data Warehouse
{% endtab %}

{% tab title="API Pipelines" %}
**Overview**

**What is an API pipeline?**

An **API Pipeline** is a type of data pipeline that uses APIs (Application Programming Interfaces) to move data between systems. These Pipeline allows you to expose data processing logic as live APIs (REST or GraphQL).

**Main purpose**

The main purpose of an API Pipeline is to provide **on-demand data services**, such as:

* Delivering **real-time or filtered data** through APIs
* Enabling easy integration with frontend apps, partner platforms, and third-party tools
* Acting as a secure interface to backend systems **without exposing databases directly**

**Benefits**

The benefits of API Pipelines include - real-time access, easy system integration, improved user experience, and better security, etc.

**Key Features**

* Supports creation of **REST and GraphQL endpoints**
* Defines clear **request and response schemas**
* Executes pipelines in **real time** when an API is called
* Handles **complex JSON structures** through mapping and nesting
* Supports **versioning** to manage changes over time
* Provides **security controls and logging** for monitoring and protection

**Key Components**

* **API Schema Node (Mandatory)**: Specifies API parameters, request structure, and expected response shape.
* **Input Nodes (Optional)**: Data from database, files, queries, GraphQL APIs, SAP, or NoSQL sources.
* **Transformation/Output (Optional)**: Modify, format, or redirect data as needed.

**Common Use Cases**

* Fetching real-time customer profiles for personalization
* Sharing live inventory data with partner platforms
* Combining data from multiple APIs into a single unified response
{% endtab %}

{% tab title="Event Pipelines" %}
**What is an Event Pipeline?**

An **Event Pipeline** is a system that **processes data continuously as events occur in real time**. These **real-time events** are such as user activity, IoT sensor data, transaction records, or external event feeds. They use **Apache Kafka** to deliver **high-speed, low-latency processing**, and support features like **data transformation, automatic retries, and time-based window processing**.

**Main Purpose**

Event pipelines support **event-driven systems** that:

* Need **instant responses** to real-time events
* Benefit from **automated and scalable** stream processing
* Rely on **continuous ingestion and transformation** of high-velocity data

**Features**

* Seamless integration with **Kafka topics** for scalable event ingestion
* Supports **windowing, watermarking, and stream enrichment** for advanced stream processing
* Enables **real-time filtering, transformation, and delivery** to target systems
* Provides **automatic retries and error handling** for reliability
* Well suited for **monitoring, automation, and alerting use cases**

**Key Components**

* **Topic Node (Mandatory)**: Connects to Kafka topic(s) and begins streaming.
* **Input Nodes (Optional)**: Ingest auxiliary or enrichment data from DBs, files, APIs.
* **Transformation Nodes (Optional)**: Handle business logic, aggregations, lookups.
* **Output Nodes (Optional)**: Push processed events to DB, APIs, dashboards, or other Kafka topics.

**Common Use Cases**

* Real-time device data monitoring in IoT platforms.
* Streaming web click data for behavioral analytics.
* Fraud detection systems processing financial transaction events in real-time.
{% endtab %}
{% endtabs %}

### Related Topics

* [Creating a Delta Pipeline](creating-a-delta-pipeline/)
* [Applying Transform Nodes](/broken/pages/wbuWbzMSOZjkjpmFRBzV)
* [Using Output Nodes](using-output-nodes/)
* [Common Other Nodes](common-other-nodes/)

[^1]: **Change Data Capture (CDC)** is a technique used in databases to **identify and record data changes**. It tracks operations such as **inserts, updates, and deletes** and stores this information so it can be used for **data synchronization, analysis, or replication**.

[^2]: Jobs that run **automatically at predefined times**.

[^3]: Jobs that process **large volumes of data together in one run**, instead of processing continuously.

[^4]: **Change Data Capture (CDC)** is a technique used in databases to **identify and record data changes**.\
    It tracks operations such as **inserts, updates, and deletes** and stores this information so it can be used for **data synchronization, analysis, or replication**.
