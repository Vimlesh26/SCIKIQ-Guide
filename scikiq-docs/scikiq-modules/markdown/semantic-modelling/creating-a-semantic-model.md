---
icon: folder-plus
---

# Creating a Semantic Model

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

Creating a Semantic Model involves a series of sequential steps that guide you through the process of transforming raw data into a business-friendly semantic layer.&#x20;

The process typically includes connecting to the data source, defining entities and thresholds, interacting with the SCIKIQ Chatbot to refine the model, establishing relationships between entities, generating insights, and creating the semantic model.&#x20;

Once the model is generated, you can optionally create a data pipeline, build dashboards, save and persist the semantic model, view its documentation, and add Common Data Elements (CDEs) to support data governance and standardization.&#x20;

Together, these steps help create a comprehensive semantic model that can be used for reporting, analytics, and business intelligence purposes.

***

### **Procedure**

Expand the below panels to view detailed procedure:

{% tabs %}
{% tab title="Navigate to Semantic Modelling Page" %}
* On the SCIKIQ **SCIKIQ Left Menu**, expand **Semantic Modelling** under **ML/GENAI STUDIO**, and then click **Create**.

<figure><img src="../../../.gitbook/assets/image (2072).png" alt=""><figcaption></figcaption></figure>

The Semantic Modelling page is displayed with the Properties section on the left pane.
{% endtab %}

{% tab title="Configure Properties" %}
**Overview**

As part of configuring the properties, you need to specify **Connection, Entities, Data Warehouse Prefix**, and **Thresholds.** These properties help you define the foundation and scope of the semantic model.&#x20;

Here is a brief description for these settings:

* **Connection:** Connection determines the AI/LLM service used for model generation.
* **Entities:**&#x45;ntities specify the key business objects to be included in the model.
* **Data Warehouse Prefix:** Data Warehouse Prefix helps identify and organize the data warehouse objects associated with the semantic model.
* **Threshold:** Threshold defines the minimum confidence level required for AI-generated entities and relationships to be included, ensuring an appropriate balance between accuracy and completeness.

**Procedure:**

The below step-by-step instructions help you understand how to configure the above properties:

1. On the **Semantic Modelling** page, in the **Properties** section, select the **data connection** from the **Data Connection** drop-down box.
2. Specify the **Number of** **Entities,** **Data Warehouse Prefix, Threshold** and **Number of Relevant Documents.**

<figure><img src="../../../.gitbook/assets/image (2073).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Interact with SCIKIQ Chatbot" %}
**Overview**

The **SCIKIQ Chatbot** assists in creating and refining semantic models by understanding user requirements and providing AI-driven recommendations. It can help generate entities, relationships, KPIs, insights, and other model components through natural language interactions. This simplifies the modeling process, reduces manual effort, and improves the overall quality of the semantic model.

> <mark style="color:red;">**Note:**</mark> At any stage of the model creation process, you can interact with the SCIKIQ Chatbot to perform various tasks and enhancements. For example, you can ask the Chatbot to add KPIs, components, metrics, relationships, or other elements to the model as needed.

**Procedure**

The below step-by-step instructions help you understand how to interact with SCIKIQ Chatbot:

1. After configuring the properties, click the **SCIKIQ** **Chat** button at the right bottom of the page.

<figure><img src="../../../.gitbook/assets/image (2074).png" alt=""><figcaption></figcaption></figure>

The **SCIKIQ** **Chatbot** is opened.

2. On the **SCIKIQ Chatbot,** In the **Prompt** field, **enter a prompt describing the semantic model you want to create**. For example, Ticket Life Cycle Management model.
3. Click the **Send** button.

<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> If the prompt is not sufficiently detailed, the Chatbot may ask for additional information to better understand the requirements and generate the semantic model accurately. You may either provide more information or skip it. See the below image.

<figure><img src="../../../.gitbook/assets/image (2076).png" alt=""><figcaption></figcaption></figure>

Once the prompt is sent, the entities (tables) are displayed and suggested actions are displayed.

<figure><img src="../../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Add Links (Relationships) " %}
**Overview**

Adding **Links (Relationships)** helps define the connections between entities within the semantic model. These relationships enable SCIKIQ to understand how data is related, support accurate reporting and analytics, and provide a comprehensive view of business information. Properly defined relationships are critical for generating meaningful insights and ensuring data consistency across the model.

**Procedure**

You can create links between tables in two ways: **by interacting with the SCIKIQ Chatbot** or **manually**.&#x20;

The following sections describe both these methods.

1.**Creating Links using SCIKIQ Chatbot**

* From the list of **Suggested Actions**, select **Suggest Relationships.**

<figure><img src="../../../.gitbook/assets/image (2078).png" alt=""><figcaption></figcaption></figure>

The relationships between the tables are generated and displayed, showing how the tables are linked to one another.

> <mark style="color:red;">**Note:**</mark> Depending on the requirement, you can select suggestions such as **Suggest More Entities**, **Suggest KPIs**, **Suggest DQ Rules**, and others.&#x20;

**2.Creating Links Manually**

A. On the **Top Menu**, click the **Add Links** button.

<figure><img src="../../../.gitbook/assets/image (1999).png" alt=""><figcaption></figcaption></figure>

The Relations Properties screen is displayed.

B. On the **Relations Properties** screen, click the **Add Relationship** button at the bottom.

<figure><img src="../../../.gitbook/assets/image (2001).png" alt=""><figcaption></figcaption></figure>

The Define relationship LDM screen is displayed.

C. On the **Define relationship LDM** screen:

* Specify the **Source Table, Target Table**, corresponding **columns**, and the **Relationship Type**.
* Click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (2002).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Generate Insights " %}
**Overview**

In the context of Semantic Modelling, **Generate Insights** is typically used to automatically identify meaningful patterns, trends, relationships, and observations from the data represented by the semantic model.

**Procedure**

The below step-by-step instructions help you understand how to generate insights:

1. From the list of **Suggested Actions**, select **Generate Insights.**

> <mark style="color:red;">**Note:**</mark> Alternatively, you can click the **Insights** button on the Top Menu to generate insights.
>
> ![](<../../../.gitbook/assets/image (2008).png>)

<figure><img src="../../../.gitbook/assets/image (2004).png" alt=""><figcaption></figcaption></figure>

The **Insights** are displayed. See the below example image.
{% endtab %}

{% tab title="Generate Model" %}
1. From the **Suggested Actions** list, select **Generate Model.**

> <mark style="color:red;">**Note:**</mark> Alternatively, you can click the **Generate Model** button on the **Top Menu.**
>
> ![](<../../../.gitbook/assets/image (2012).png>)

<figure><img src="../../../.gitbook/assets/image (2114).png" alt=""><figcaption></figcaption></figure>

The Generate Models dialogue box is displayed.

2. On the **Generate Models** dialogue box:

* Select either **Reporting Model** or **Analytical Model.**

> <mark style="color:red;">**Note:**</mark> Here is the description for **Reporting Model** and **Analytical Model.**
>
> **Reporting Model**
>
> * This model generates a business-friendly semantic model optimized for creating reports, dashboards, and KPI visualizations.&#x20;
> * It focuses on predefined metrics and simplified data structures for efficient reporting.&#x20;
> * You can choose **Reporting Model** when the primary goal is to create dashboards, reports, and KPI monitoring.
>
> **Analytical Model**
>
> * This model generates a semantic model optimized for detailed data analysis and exploration.&#x20;
> * It provides richer relationships and additional contextual information to support advanced analytics and insight discovery.&#x20;
> * You can choose **Analytical Model** when the primary goal is to perform detailed analysis, identify trends, and explore data from multiple perspectives.

3. After selecting the required model, click the **Ok** button.

<figure><img src="../../../.gitbook/assets/image (2116).png" alt=""><figcaption></figcaption></figure>

The Semantic Model is generated. See the below image.

<figure><img src="../../../.gitbook/assets/image (2013).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Persist Model" %}
**Overview**

In the context of Semantic Modelling, **Persist** means **to save and store the generated model permanently in the system so that it can be reused later**.

**Procedure**

The below step-by-step instructions help you understand how to persist the model:

1. On the **Top Menu**, click the **Persist Model** button.

<figure><img src="../../../.gitbook/assets/image (2014).png" alt=""><figcaption></figcaption></figure>

The Persist Model dialogue box is displayed.

2. On the **Persist Model** dialogue box:

* From the **Data Store** drop-down box, select the required **store**.
* From the options area, select **Persist in Database, Download SQL Script, Generate Fake Data,** and **Create Logical Mode.**

Here is the description for these options:

<table><thead><tr><th width="181.22222900390625" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Persist in Database</td><td valign="top">Selecting this option saves the generated semantic model and its associated metadata to the database, making it permanently available for future use, modification, reporting, analytics, and integration with other SCIKIQ components.</td></tr><tr><td valign="top">Download SQL Script</td><td valign="top"><p>Selecting this option Selecting this option generates and downloads the SQL script for the semantic model, enabling you to review, deploy, or recreate the model's database structures and relationships in another environment.</p><p><br><mark style="color:red;"><strong>Note:</strong></mark> Selecting this option is optional.</p></td></tr><tr><td valign="top">Generate Fake Data</td><td valign="top"><p>Selecting this option creates synthetic sample data for the semantic model, allowing you to test, validate, and visualize the model without using actual business data.</p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> Selecting this option is optional.</p></td></tr><tr><td valign="top">Create Logical Mode</td><td valign="top"><p>Selecting this option generates a business-oriented logical model that represents entities, attributes, and relationships without exposing physical database implementation details. This helps users visualize and validate the business structure of the model.</p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> This option is required to create dashboard.</p></td></tr></tbody></table>

* After selecting the Persist Model options, click the **Ok** button.

<figure><img src="../../../.gitbook/assets/image (2026).png" alt=""><figcaption></figcaption></figure>

The Save LDM dialogue box is displayed.

3. On the **Save LDM** dialogue box, specify a **name** and **description** for the **LDM**, and then click the **Finish** button.

<figure><img src="../../../.gitbook/assets/image (2027).png" alt=""><figcaption></figcaption></figure>

The semantic model is saved to the selected data store and the **Success** message is displayed.

<figure><img src="../../../.gitbook/assets/image (2017).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Create Data Pipeline" %}
**Overview**

Creating a **Data Pipeline** allows you to automate the flow of data from source systems to the semantic model, ensuring that the model remains current and accurate. It supports data integration, transformation, and preparation for reporting and analytics.&#x20;

**This step is optional** and can be performed when automated data processing is required.

**Procedure**

The below step-by-step instructions help you understand how to create pipeline:

* On the **Top Menu**, click the **Data Pipelines** button.

<figure><img src="../../../.gitbook/assets/image (2024).png" alt=""><figcaption></figcaption></figure>

The **Data Pipelines** page is displayed.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> For detailed, step-by-step instructions on creating data pipelines, refer to the link provided below. [https://app.gitbook.com/o/Fgg2jIjXbcQ7ncOpRXn9/s/icS7nbBkGeQlzANmHGiv/\~/edit/\~/changes/508/scikiq-modules/images-and-media-1/scikiq-pipeline](https://app.gitbook.com/o/Fgg2jIjXbcQ7ncOpRXn9/s/icS7nbBkGeQlzANmHGiv/~/edit/~/changes/508/scikiq-modules/images-and-media-1/scikiq-pipeline)
>
> You can also interact with the SCIKIQ Chatbot for guidance and assistance throughout the pipeline creation process.
{% endtab %}

{% tab title="Create Dashboard" %}


**Overview**

Creating a **Dashboard** allows you to present the information contained in the semantic model through interactive visualizations and reports. It helps users monitor key metrics, analyze trends, and gain actionable insights from the data.&#x20;

**This step is optional** and can be performed when visual reporting and data exploration are required.

**Procedure**

The below step-by-step instructions help you understand how to create a Dashboard:

1. On the **Top Menu**, click the **Dashboard** button.

<figure><img src="../../../.gitbook/assets/image (2020).png" alt=""><figcaption></figcaption></figure>

The Create Dashboard dialogue box is displayed.

2. On the **Create Dashboard** dialogue box, select the required **KPIs** , and then click the **Generate Dashboard** button.

<figure><img src="../../../.gitbook/assets/image (2021).png" alt=""><figcaption></figcaption></figure>

The Dashboard is generated.

<figure><img src="../../../.gitbook/assets/image (2023).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Save Semantic Model" %}
**Overview**

Saving the **Semantic Model** ensures that all the entities, relationships, KPIs, Data Quality (DQ) Rules, and other configurations are retained for future use. Saving also helps maintain the continuity and integrity of the modeling process, ensuring that the latest changes are preserved.&#x20;

This step is essential for making the semantic model available for reporting, analytics, dashboards, and other downstream activities.

**Procedure**

The below step-by-step instructions help you understand how to save the semantic model:

* On the **Top Menu**, click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (2029).png" alt=""><figcaption></figcaption></figure>

The Semantic Model is saved.
{% endtab %}

{% tab title="Download Documentation" %}
**Overview**

Downloading the documentation generates a detailed reference of the semantic model's structure and components, supporting understanding, governance, maintenance, and collaboration.

**Procedure**

The below step-by-step instructions help you understand how to download documentation.

* On the **Top Menu**, click the **Documentation**  tab.

<figure><img src="../../../.gitbook/assets/image (2031).png" alt=""><figcaption></figcaption></figure>

The **Semantic Model Analysis Report** provides a detailed summary of the entities, KPIs, and Data Quality (DQ) Rules, etc. that were incorporated during the semantic model creation process. See below image.

<figure><img src="../../../.gitbook/assets/image (2032).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Add CDEs" %}
**Overview**

Adding CDEs helps identify and standardize the most important business data elements within the semantic model. This ensures that key data fields are consistently defined, governed, and used across reports, dashboards, analytics, and business processes.

**Procedure**

The below step-by-step instructions help you understand how to add CDEs.

1. On the **Top Menu**, click the **CDE**  tab.

<figure><img src="../../../.gitbook/assets/image (2033).png" alt=""><figcaption></figcaption></figure>

The Business Data Elements screen is displayed.

2. On the **Business Data Elements** screen, click the **OK** button.

<figure><img src="../../../.gitbook/assets/image (2034).png" alt=""><figcaption></figcaption></figure>

The the business data elements are added and  the **Business Data Elements** page is displayed under **Metadata Manager**.

<figure><img src="../../../.gitbook/assets/image (2035).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Managing a Semantic Model**](managing-a-semantic-model/)
