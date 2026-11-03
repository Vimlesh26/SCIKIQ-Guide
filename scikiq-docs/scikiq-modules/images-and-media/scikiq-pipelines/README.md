---
icon: hubspot
---

# SCIKIQ Pipelines

### 1. Introduction

**SCIKIQ Pipelines** are a robust, enterprise-grade solution engineered to manage complex data workflows that span across various systems, platforms, and formats. They function as an intelligent data orchestration framework, enabling the seamless movement, transformation, and activation of data from multiple sources to multiple destinations—whether on-premises or in the cloud.

Unlike conventional ETL tools that focus primarily on batch processing and often require extensive manual configuration, SCIKIQ Pipelines unify **real-time, batch, and event-driven integration** in a single visual interface. This low-code/no-code environment allows both technical and business users to collaboratively build, deploy, and monitor data pipelines with minimal friction.

These pipelines enable organizations to:

* Streamline operations by automating data ingestion and transformation.
* Facilitate timely decision-making through real-time and event-triggered data delivery.
* Reduce dependency on custom scripts and siloed tools.
* Maintain data consistency and accuracy through change tracking, schema mapping, and fault-tolerant designs.

SCIKIQ Pipelines are not just data movers—they are data **activators** that unlock value by connecting fragmented data landscapes into cohesive, intelligent workflows.

### 2. Purpose

The primary objectives of SCIKIQ Pipelines are to:

* **Simplify Data Integration**: Unify disparate systems such as RDBMS, NoSQL, APIs, SAP, and file-based sources through a standardized interface.
* **Enable Real-Time and Incremental Data Processing**: Allow pipelines to operate on new or changed records, ensuring systems are updated without full reloads.
* **Support Data Activation and Intelligence**: Power data-driven decisions through real-time APIs and event-triggered automations.
* **Promote Operational Efficiency**: Replace repetitive, error-prone manual processes with reliable automation and intelligent scheduling.
* **Provide Visibility and Governance**: Empower stakeholders with a visual understanding of data lineage, pipeline ownership, transformation logic, and execution status.

SCIKIQ’s platform bridges the gap between business agility and technical precision, providing a foundation for both citizen developers and enterprise data engineers to build resilient, responsive data systems.

### **3. Types of Pipelines in SCIKIQ**

SCIKIQ supports **three primary pipeline types**, each tailored for different data integration and movement scenarios:

| Pipeline Type      | Description                                                                    |
| ------------------ | ------------------------------------------------------------------------------ |
| **Delta Pipeline** | For incremental, scheduled data movement (Change Data Capture, Batch Updates). |
| **API Pipeline**   | For real-time, on-demand data exchange via REST/GraphQL APIs.                  |
| **Event Pipeline** | For event-triggered, streaming data processing (Kafka/Event-Driven Systems).   |

### 3.1 Delta Pipeline – Incremental & Scheduled Data Integration

**Overview**

The **Delta Pipeline** is optimized for extracting and loading **only the changes (deltas)** in a dataset. This reduces data redundancy, accelerates processing times, and minimizes the load on both source and destination systems. It is ideal for **scheduled or batch jobs** where frequent full loads would be inefficient or unnecessary.

**Core Purpose**

To enable **incremental and periodic updates** in a resource-efficient manner, particularly where:

* Full data reloads are not practical.
* **Change Data Capture (CDC)** is essential to track inserts, updates, and deletes.
* Regular refresh schedules are needed (hourly, daily, weekly).

**Features**

* Supports CDC mechanisms from databases and files.
* Allows **parameterized filtering** (e.g., based on timestamps, row version).
* Compatible with both **manual** and **automated scheduled** execution.
* Built with a **drag-and-drop** interface to reduce development time.
* Ensures schema flexibility and reusability through pipeline versioning.

**Key Components**

* **Input Nodes (Mandatory)**: Sources like Database Input, File Input, SAP App Server, Query Input, or NoSQL.
* **Transformation Nodes (Optional)**: Apply logic such as joins, filters, expressions, or conditional mappings.
* **Output Nodes (Mandatory)**: Target systems like RDBMS, cloud databases, APIs, or file sinks.

**Common Use Cases**

* Daily sync of customer updates from CRM to Data Warehouse.
* Pushing incremental inventory changes to analytics systems.
* Extracting changes from ERP systems to update reporting layers.

### 3.2 API Pipeline – Real-Time API-Based Data Exchange

**Overview**

The **API Pipeline** allows SCIKIQ users to **expose data processing logic as live REST or GraphQL APIs**. These endpoints enable consumers—internal or external—to fetch and process data on-demand in real time. API Pipelines are crucial for **microservice architectures, dynamic dashboards**, and integrations requiring **instantaneous access** to backend logic or records.

**Core Purpose**

To enable **on-demand, interactive data services** that:

* Serve real-time, personalized, or filtered datasets via APIs.
* Integrate directly into frontend apps, partner systems, or third-party tools.
* Act as **digital interfaces** to backend logic without exposing raw data systems.

**Features**

* Configures REST or GraphQL endpoints with input/output schema definition.
* Supports **real-time execution and response handling**.
* Allows nesting and mapping of **complex JSON** payloads.
* Version-controlled pipelines to manage endpoint evolution.
* Secure access control and logging.

**Key Components**

* **API Schema Node (Mandatory)**: Specifies API parameters, request structure, and expected response shape.
* **Input Nodes (Optional)**: Data from database, files, queries, GraphQL APIs, SAP, or NoSQL sources.
* **Transformation/Output (Optional)**: Modify, format, or redirect data as needed.

**Common Use Cases**

* Real-time customer profile retrieval for personalization engines.
* Providing inventory availability to retail partner platforms.
* Consolidating third-party data via multiple API sources into a single response schema.

### 3.3 Event Pipeline – Real-Time Event-Driven Processing

**Overview**

**Event Pipelines** are designed to respond to **streams of real-time events**, such as user actions, IoT sensor data, transaction logs, or external event feeds. Powered by **Apache Kafka**, they provide high-throughput, low-latency processing with built-in support for transformations, retries, and time-windowing.

**Core Purpose**

To support **event-driven architectures** that:

* Require immediate response to real-world triggers.
* Benefit from automated and scalable stream handling.
* Depend on **continuous ingestion** and transformation of fast-moving data.

**Features**

* Native integration with **Kafka topics** for scalable ingestion.
* Supports **windowing**, **watermarking**, and **stream enrichment**.
* Real-time filtering, transformation, and delivery to downstream systems.
* Automatic retry logic and error recovery.
* Ideal for operational monitoring, automation, and alerting.

**Key Components**

* **Topic Node (Mandatory)**: Connects to Kafka topic(s) and begins streaming.
* **Input Nodes (Optional)**: Ingest auxiliary or enrichment data from DBs, files, APIs.
* **Transformation Nodes (Optional)**: Handle business logic, aggregations, lookups.
* **Output Nodes (Optional)**: Push processed events to DB, APIs, dashboards, or other Kafka topics.

**Common Use Cases**

* Real-time device data monitoring in IoT platforms.
* Streaming web click data for behavioral analytics.
* Fraud detection systems processing financial transaction events in real-time.
