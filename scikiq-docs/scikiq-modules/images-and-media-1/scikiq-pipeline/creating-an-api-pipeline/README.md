---
icon: webhook
---

# Creating an API Pipeline

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

**API Pipelines in SCIKIQ** enable seamless data interaction with internal and external systems through APIs, supporting near real-time data exchange. These pipelines are designed to connect to applications or platforms that expose API interfaces and support modern protocols such as **REST and GraphQL**, making integration with cloud-based and enterprise applications straightforward.

An API Pipeline can be used to **fetch data from APIs**, **apply required transformations**, and **expose the processed data through published API endpoints**. This allows other applications or services to securely consume the transformed data on demand.

***

### Procedure

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Configure API Schema Node</strong></summary>

**Purpose:**

While creating an **API Pipeline**, the **API Schema Node** is mandatory. This is because **API Schema Node** it tells the system **what the API is**, **what data it exposes**, and **how consumers can interact with it**. An API Pipeline cannot exist without a clearly defined schema.

**Procedure:**

While creating an API Pipeline, the **API Schema node is mandatory**. As part of the configuration, you must provide a **JSON object** that defines the API schema and validate it. Once the **validation** is successful, you can preview  validated JSON.

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions**

1. On the **Left Navigation Bar**, expand **SCIKIQ Delta Hub** under **SCIKIQ CONNECT**, and then click **Click Create API.**

The API Schema Node is displayed by default on the right pane (Main Workspace).&#x20;

2. On the **Right Pane** page, select the **API Schema Node.**

The **Select** **API Schema** section is displayed on the left pane.

3. On the **left pane**, in the **Select** **API Schema** section:

A. From the drop-down box select **JSON,** and enter a valid **JSON** object in the **input** field.

B. Click the **Validate and Extract** button.

<figure><img src="../../../../.gitbook/assets/S (272).png" alt=""><figcaption><p>Validating and Extracting JSON Object</p></figcaption></figure>

The Valid JSON success message is displayed.

{% hint style="info" %}
Tip: If the JSON is invalid, verify the error message is displayed with specific details about the error on the Node Validation tab on the right side top of the application.

![](<../../../../.gitbook/assets/image (2490).png>)
{% endhint %}

C. On the Right Pane, click the **Preview** icon on the top of **API Schema Node.** &#x20;

<figure><img src="../../../../.gitbook/assets/1 (13).png" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

The valid JSON object is displayed on the Preview tab. See the image below.

<figure><img src="../../../../.gitbook/assets/S (273).png" alt=""><figcaption><p>JSON Preview</p></figcaption></figure>

{% hint style="info" %}
**Tip:** The extract data can be displayed in JSON format only if the **DF Enable** option under API Schema is **disabled**. If it is enabled (the DF **DF Enable** option), then the JSON extracted data is displayed in tabular format.
{% endhint %}

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

* [**Creating a Delta Pipeline**](../creating-a-delta-pipeline/)
* [**Creating an Event Pipeline**](../creating-an-event-pipeline/)

