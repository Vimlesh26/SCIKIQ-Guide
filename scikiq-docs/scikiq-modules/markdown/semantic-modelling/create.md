---
hidden: true
---

# Create

**What is Semantic Modeling?**

Semantic modeling is the process of creating a structured representation of data that adds meaning and context to raw data. It defines how data elements relate to each other, often in a way that's closer to business understanding than just technical definitions.

**Why is Semantic Modeling Important?**

✅ **Business-friendly layer** - It bridges the gap between raw data and business logic.&#x20;

✅ **Data reusability** - Once created, others (like report writers) can reuse the model without knowing SQL.&#x20;

✅ **Accuracy** - Ensures metrics (like “Revenue” or “Active Users”) are calculated consistently.&#x20;

✅ **Self-service** BI Enables non-technical users to explore data via tools like Power BI, Tableau, Looker.&#x20;

✅ **Data governance** Helps enforce naming, definitions, and logic standards across reports/dashboards.

**Semantic Model Includes:**&#x20;

**1**.**Entities** (tables like Customer, Product, Sales)

**2.Attributes** (columns)

**3.Relationships** (joins/foreign keys)

**4.Hierarchies** (e.g., Year > Quarter > Month)

**5.Measures** (calculated metrics like Revenue, Margin)

**6.Metadata** (descriptions, units, format, etc.)



**How to Create a Semantic Model ?**

First you need to set Configuration & Attributes using Properties .

<figure><img src="../../../.gitbook/assets/image (1389).png" alt=""><figcaption></figcaption></figure>

| **Setting**               | **Definition**                                                                           | **Use / Purpose**                                                                                    | **Example**                                           |
| ------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ----------------------------------------------------- |
| **Set Connection**        | Specifies the connection details to data sources or LLM services                         | Connects your semantic model to a **data warehouse**, **database**, or **LLM provider** like OpenAI  | `openai`, `Azure OpenAI`, `BigQuery`, `Snowflake`     |
| **LLM Connection**        | Defines the configuration for using a **Large Language Model** within the semantic model | Enables **natural language querying**, auto-generation of metrics, or insights via AI                | Provider: `openai`, Model: `gpt-4`, API Key: required |
| **Model**                 | Refers to the specific **semantic model or AI model** being used                         | Dictates how the data is understood or processed. Could refer to LLMs or the **business model name** | `gpt-4`, `gpt-3.5`, `scikiq_sales_model`              |
| **Number of Entities**    | Indicates how many **distinct entities/tables/concepts** exist in the semantic model     | Helps track data complexity, schema size, or model coverage                                          | `5` (e.g., Customers, Orders, Products...)            |
| **Data Warehouse Prefix** | The **naming convention or prefix** used for tables from a data warehouse                | Assists in mapping source tables to semantic layer entities and in keeping naming consistent         | `dwh_` → `dwh_orders`, `dwh_customers`                |
| **Threshold**             | Numeric or rule-based limits used to flag anomalies, warnings, or alerts                 | Used in KPI evaluation, conditional formatting, and AI-assisted decision-making                      | Warning: `<70`, Alert: `<50`                          |
| **Relevant Documents**    | External or internal **documents, metadata files, or URLs** linked to the model          | Provides context, glossary, business rules, or audit trails for data governance and traceability     | Data Dictionary, SOPs, SharePoint links               |

On the Top right side , there are more options that you can use for further reasons

<figure><img src="../../../.gitbook/assets/image (1391).png" alt=""><figcaption></figcaption></figure>

| **Setting**                       | **Definition**                                                                  | **Use / Purpose**                                                                              | **Example**                                      |
| --------------------------------- | ------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ------------------------------------------------ |
| **Add CDE**(Curated Data Element) | Adds a **business-approved, standardized data field** into the semantic layer   | Ensures consistency in how metrics like “Revenue” or “Customer ID” are reused across reports   | `Customer_ID`, `Net_Profit_Margin`               |
| **Add Entities**                  | Adds a **table or logical business object** to the semantic model               | Used to define real-world concepts like **Customer**, **Order**, **Product** in the data model | Entities: `Customer`, `Invoice`, `Product`       |
| **Add Links**                     | Creates **relationships or joins** between entities                             | Enables navigation across tables via **foreign keys or logical joins**                         | Link `Customer_ID` in Orders → Customer entity   |
| **Insights**                      | Automatically surfaces **noteworthy trends, outliers, or patterns**             | Helps users find meaningful patterns without writing queries; often AI/ML-powered              | “Sales dipped by 20% in Q2”                      |
| **Generate Models**               | Auto-creates **semantic models** from data sources or schemas                   | Saves time by extracting structure from DWH or CSV; optionally AI-generated                    | Auto-generated entities from `dwh_sales_*`       |
| **Persist Models**                | Saves or publishes the **semantic model** to a metadata store or modeling layer | Makes the model versioned, reusable, and available across dashboards or pipelines              | `sales_model_v2` persisted in metadata catalog   |
| **Data Pipeline**                 | A defined **flow of data** from ingestion to transformation to output           | Prepares, cleans, transforms, or loads data to be used by the semantic model                   | ETL job: Load → Clean → Join → Serve             |
| **Create Dashboard**              | Launches dashboard creation with **semantic model entities and metrics**        | Lets users build visualizations based on model-defined fields                                  | Drag and drop `Revenue`, `Region`, `Product`     |
| **Smart Profile**                 | Automatically generates **data profiling summaries** for a dataset or entity    | Shows unique values, nulls, outliers, and suggestions for cleaning or tagging                  | 94% unique `email_id`, 2% nulls in `DOB`         |
| **Semantic Model**                | A **logical abstraction layer** mapping business terms to physical data         | Translates raw data into human-understandable business language and structure                  | `Customer` → table: `dwh_customer_master`        |
| **Full Screen**                   | Maximizes workspace UI for modeling or dashboarding                             | Enhances visibility and usability of complex semantic models or dashboards                     | Used while editing relationships or large charts |

Using Chat Bot, We can create a semantic model e.g. here created a semantic model for HR 360 view with 5 entities and for further changes you can select any suggestion in the chat bot.

<figure><img src="../../../.gitbook/assets/image (1395).png" alt=""><figcaption></figcaption></figure>

By clicking on Generate Model, you can choose any one from 4 options

<figure><img src="../../../.gitbook/assets/image (1386).png" alt=""><figcaption></figcaption></figure>

After selecting Reporting Model, reporting model will generate, and you can persist it into your required db.

<figure><img src="../../../.gitbook/assets/image (1388).png" alt=""><figcaption></figcaption></figure>

**Basic Steps to Generate and Persist a Semantic Model**

<table data-header-hidden><thead><tr><th width="80"></th><th></th><th></th></tr></thead><tbody><tr><td><strong>Step</strong></td><td><strong>Action</strong></td><td><strong>Details / What to Do</strong></td></tr><tr><td><strong>1</strong></td><td><strong>Connect to Data Source</strong></td><td>- Choose your source (e.g., Snowflake, SQL Server, CSV, etc.)- Set credentials and test the connection</td></tr><tr><td><strong>2</strong></td><td><strong>Select Tables or Schemas</strong></td><td>- Browse available schemas- Select the required tables or views</td></tr><tr><td><strong>3</strong></td><td><strong>Add Entities</strong></td><td>- Convert selected tables into <strong>semantic entities</strong> (e.g., <code>Customer</code>, <code>Order</code>)</td></tr><tr><td><strong>4</strong></td><td><strong>Add CDEs (Curated Data Elements)</strong></td><td>- Identify and name key business metrics or fields (e.g., <code>Total Sales</code>, <code>Customer ID</code>)</td></tr><tr><td><strong>5</strong></td><td><strong>Add Links (Relationships)</strong></td><td>- Define relationships between entities (e.g., foreign keys)- Set join logic</td></tr><tr><td><strong>6</strong></td><td><strong>Generate Model (Optional Auto-Gen)</strong></td><td>- Use auto-generation from schema or LLM suggestion (e.g., “generate model from dwh_*”)</td></tr><tr><td><strong>7</strong></td><td><strong>Apply Thresholds (if required)</strong></td><td>- Set KPIs, alert levels, or rule-based thresholds on numeric fields</td></tr><tr><td><strong>8</strong></td><td><strong>Attach Relevant Documents (Optional)</strong></td><td>- Link metadata docs, definitions, or lineage references</td></tr><tr><td><strong>9</strong></td><td><strong>Run Smart Profile (Optional)</strong></td><td>- Auto-scan entities for uniqueness, nulls, outliers</td></tr><tr><td><strong>10</strong></td><td><strong>Review Semantic Model</strong></td><td>- Visually inspect entities, relationships, and labels for accuracy</td></tr><tr><td><strong>11</strong></td><td><strong>Persist the Model</strong></td><td>- Save and publish the model to a metadata layer or catalog for reuse</td></tr><tr><td><strong>12</strong></td><td><strong>Test with Insights / Dashboards</strong></td><td>- Use the model in dashboards or natural language queries to validate usability</td></tr></tbody></table>



**Add Entities-** Adds a **table or logical business object** to the semantic model e.g. Department, Personal Details etc.

<figure><img src="../../../.gitbook/assets/image (1402).png" alt=""><figcaption></figcaption></figure>

**Add Links**- By clicking on Add Relationship, you can Define relationship by select source and target table with their columns and add relationship.

<figure><img src="../../../.gitbook/assets/image (1403).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1404).png" alt=""><figcaption></figcaption></figure>

**Insights-**&#x41;utomatically surfaces **noteworthy trends, outliers, or patterns**

<figure><img src="../../../.gitbook/assets/image (1405).png" alt=""><figcaption></figcaption></figure>

**Generate Model -** Use auto-generation from schema or LLM suggestion (e.g., “generate model from dwh\_\*”)

<figure><img src="../../../.gitbook/assets/image (1407).png" alt=""><figcaption></figcaption></figure>

**Persist Model -** Save and publish the model to a metadata layer or catalog for reuse

<figure><img src="../../../.gitbook/assets/image (1406).png" alt=""><figcaption></figcaption></figure>

**Documentation-**&#x52;elated pdf file will be into download folder.

<figure><img src="../../../.gitbook/assets/image (1408).png" alt=""><figcaption></figcaption></figure>
