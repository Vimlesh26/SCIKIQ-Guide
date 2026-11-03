---
icon: page
---

# Creating a Data Product by CDO/Technical Persona

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The process of creating a data product as a **Technical Persona** involves a series of steps. These include _selecting a group connection and exploring metadata, reclassifying data, obtaining the data product use case from the chatbot, generating a dashboard, performing smart profiling, generating pipelines, scheduling pipelines, saving the data product use case, and downloading the documentation._

The below Procedure section provides a detailed description of each of these:

***

### Procedure

Click on the below tabs to view step-by-step instructions:

{% tabs %}
{% tab title="Select Group Connection and Explore Metadata" %}
**Overview**

**Group Connection** allows you to select the relevant data source connections, while **Explore Metadata** helps you examine their available databases, schemas, tables, columns, and relationships to identify the data required for creating the data product.

**Procedure**

The below step-by-step instructions help you understand how to select group connection and explore metadata:

_**To select group connection and explore metadata**_

1. On the SCIKIQ **SCIKIQ Left Menu**, expand **Data Product Factory** under **ML/GENAI STUDIO**, and then click **CDO/Technical Persona.**

<figure><img src="../../../.gitbook/assets/image (2686).png" alt=""><figcaption></figcaption></figure>

The **CDO/Technical Persona** page is displayed with a list of group connection types.&#x20;

2. On the **CDO/Technical Persona** page:

A. From the **list of group connection types**, select the **required group connection type**. For example, Relational Database.

The connections are displayed on the right pane.

B. From the **right pane**, select the **required connections**, and then click the **Explore Metadata** button.

<figure><img src="../../../.gitbook/assets/image (2690).png" alt=""><figcaption></figcaption></figure>

The Select Industry and Domain dialogue box is displayed.

C. On the **Select Industry and Domain** dialogue box, select **industry** and **domain**, and then click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (2691).png" alt=""><figcaption></figcaption></figure>

The selected industry and domain are saved and the **Table Details** section is displayed.

Next, click [**Reclassify Table Details**](creating-a-data-product-by-cdo-technical-persona.md#reclassify-table-details).
{% endtab %}

{% tab title="Reclassify  Table Details" %}
**Overview**

**Reclassification** re-evaluates the data in the selected table based on its metadata and updates the existing classification accordingly. This helps ensure that the table and its columns are assigned the most appropriate and up-to-date classifications when the metadata or data structure changes.

**Procedure**

The below step-by-step instructions help you understand how to reclassify:

_**To reclassify**_

* On the **Table Details** section, click the **Reclassify** button.

<figure><img src="../../../.gitbook/assets/image (2668).png" alt=""><figcaption></figcaption></figure>

The table data is reclassified. See the below image.

<figure><img src="../../../.gitbook/assets/image (2669).png" alt=""><figcaption></figcaption></figure>

Next, click [**Get Data Product Use Case From Chat Window**](creating-a-data-product-by-cdo-technical-persona.md#get-data-product-use-case-from-chat-window).
{% endtab %}

{% tab title="Get Data Product Use Case From Chatbot" %}
**Overview**

**Getting the Data Product Use Case** from the Chatbot helps capture and understand the specific business requirement, ensuring that the data product is aligned with the intended business needs and objectives. This helps identify the right data and use it effectively to create a relevant and valuable data product.

**Procedure**

The below step-by-step instructions help you understand how to get data product use case from the chatbot:

1. On the right bottom of the page, click **SCIKIQ Chatbot.**

The **SCIKIQ Chatbot** is opened with a list of applicable suggestions.

2. From the list of applicable suggestions, select **Get Data Product Use Case.**



<figure><img src="../../../.gitbook/assets/image (2591).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (2670).png" alt=""><figcaption></figcaption></figure>

A list of use cases are suggested.

2. From the **list of use cases**, select the **appropriate use case** by clicking on it. For example, Inventory Management Dashboard as shown in the below image.

<figure><img src="../../../.gitbook/assets/image (2602).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> Before selecting a use case, you can view its brief description. Based on your requirements, you can edit the use case or save it for future use. Additionally, you can view and use the **recommended tables** or **tables already used** for the selected use case. Refer to the below example image.

<figure><img src="../../../.gitbook/assets/image (2593).png" alt=""><figcaption></figcaption></figure>

Once the data product use case is selected, the use case is displayed on the Business Persona page.

3. On the **Business Persona** page, expand the **Dashboard** panel, and then click the<img src="../../../.gitbook/assets/image (2597).png" alt="" data-size="line">button next to **Select Logical Data Model** drop-down box.

<figure><img src="../../../.gitbook/assets/image (2603).png" alt=""><figcaption></figcaption></figure>

The Semantic Model page is displayed with the pipelines.&#x20;

4. From the Semantic Model page, first **Generate Model,** then **Persist Model,** and finally **Save Semantic Model.** Refer to [**Creating a Semantic Model**](../semantic-modelling/creating-a-semantic-model.md) for information on how to perform  these steps.&#x20;

Once the model is saved, the Use Case page is displayed and the model is available for selection in the **Select Logical Data Model** drop-down box.

Next, click [**Generate Dashboard**](creating-a-data-product-by-cdo-technical-persona.md#generate-dashboard).
{% endtab %}

{% tab title=" Create Your Own Data Product Use Case" %}
**Overview**

**Create Your Own Use Case** option enables you to define a use case based on your organization's specific needs. You can describe the use case name,dewcription, and select the required tables. The Data Product Factory uses this information to help identify the relevant data and create a data product tailored to your specific use case.

**Procedure**

The below step-by-step instructions help you understand how to create your own data product use case.

**To create your own data product use case**

1. From the list of **Chatbot suggestions**, select **Create Own Data Product Use-Case.**&#x20;

<figure><img src="../../../.gitbook/assets/image (2589).png" alt=""><figcaption></figcaption></figure>

The Use Case fields section is displayed.

2. In the **Use Case fields** section:

A. Enter **Use Case Title** and **Use Case Description.**

B. Select the **product type** choosing from **Dashboard as a Product, LDM as a Product** or **ML as a Product.**

> <mark style="color:red;">**Note:**</mark> Here is the description for the product types:
>
> * **Data as a Product:** Data is treated as a reliable, reusable, and well-managed product that is designed to meet specific business needs and can be easily discovered and consumed by users.
> * **LDM as a Product:** A Logical Data Model (LDM) is treated as a reusable product that provides a standardized and business-friendly representation of data entities, their attributes, and relationships.
> * **ML as a Product:** A Machine Learning (ML) model is treated as a reusable product that can be deployed and consumed to generate predictions, classifications, or other intelligent insights for specific business needs.

C. Select the required **Tables,** and then click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (2587).png" alt=""><figcaption></figcaption></figure>

Your own data product use case is created. See the below image.

<figure><img src="../../../.gitbook/assets/image (2588).png" alt=""><figcaption></figcaption></figure>


{% endtab %}

{% tab title="Generate Dashboard" %}
**Overview**

**Generating dashboard** creates and makes the dashboard available on the **Use Case** page for selection. This allows you to associate the dashboard with a relevant use case and use it to visualize and monitor the information related to that use case.

**Procedure**

1. On the **Use Case** page, from the **Select Logical Data Model** drop-down box, select the **logical data model.** For example, Customer satisfaction dashboard.

> <mark style="color:red;">**Note:**</mark> The model that you have generated and saved in the Pipelines page is available in the **Select Logical Data Model** drop-down box.

2. Now, click the <img src="../../../.gitbook/assets/image (2636).png" alt="" data-size="line">button next to **Select Dashboard** drop-down box.

<figure><img src="../../../.gitbook/assets/image (2637).png" alt=""><figcaption></figcaption></figure>

The dashboard is displayed according to the selected logical data model.&#x20;

3. On the **Dashboard,** click the **Save** button on the top right side corner.

<figure><img src="../../../.gitbook/assets/image (2639).png" alt=""><figcaption></figcaption></figure>

Once saved, the dashboard is available for selection in the **Select Dashboard** drop-down box on the **Use Case** page.

4. From the **Select Dashboard** drop-down box, select the **dashboard**.

<figure><img src="../../../.gitbook/assets/image (2640).png" alt=""><figcaption></figcaption></figure>

Next, click [**Smart Profiler**](creating-a-data-product-by-cdo-technical-persona.md#smart-profiler)**.**
{% endtab %}

{% tab title="Smart Profiler" %}
**Overview**&#x20;

**Smart Profiling** helps while creating a data product by automatically analyzing the selected data and providing insights into its structure, content, and quality. It helps identify key characteristics such as data types, patterns, missing values, and potential data issues, enabling you to better understand the data and select the most relevant and suitable data assets for the data product.

**Procedure**

* On the **Use Case** page, click the **Smart Profiler** button under **Chat as a Product.**

<figure><img src="../../../.gitbook/assets/image (2642).png" alt=""><figcaption></figcaption></figure>

The **Smart Profiler** page is displayed with analyzing the data. Once the analysis is completed the page is displayed as shown below. You can view the summary, data summary, and insights.

<figure><img src="../../../.gitbook/assets/image (2561).png" alt=""><figcaption></figcaption></figure>

Next, click [**Generate Pipelines**](creating-a-data-product-by-cdo-technical-persona.md#generate-pipelines)**.**


{% endtab %}

{% tab title="Generate Pipelines" %}
**Overview**&#x20;

**Generating Pipelines** helps create the required data processing workflows for a data product by defining how data is collected, transformed, and delivered. This ensures that the selected data is processed in a structured and repeatable manner, making it ready to support the intended business use case of the data product.

**Procedure**

The below step-by-step instructions help you understand how to generate pipelines:

_**To generate pipelines**_

1. On the **Use Case** page, click the <img src="../../../.gitbook/assets/image (2562).png" alt="" data-size="line">button under **Micro Batch Pipelines.**

<figure><img src="../../../.gitbook/assets/image (2563).png" alt=""><figcaption></figcaption></figure>

The Pipelines page is displayed.

<figure><img src="../../../.gitbook/assets/image (2564).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * By default, pipeline is generated with the Join node. You can add transform node to it based on the need.

2. Refer to the **Chatbot** for the suggested tables, select the required **ones**, and then click the **Submit** button to add them. See the below example image.

<figure><img src="../../../.gitbook/assets/image (2565).png" alt=""><figcaption></figcaption></figure>

3. After making necessary changes, click the **Save** button on the on the **Pipelines** page.

The Save Data Pipeline dialogue box is displayed.

4. On the **Save Data Pipeline** dialogue box, specify P**ipeline Name, Description,  Technical Owner,** and then click the **Save & Submit** button.

<figure><img src="../../../.gitbook/assets/image (2567).png" alt=""><figcaption></figcaption></figure>

The pipeline is displayed in the Micro Batch Pipelines drop-down box on the Use Case page.

<figure><img src="../../../.gitbook/assets/image (2568).png" alt=""><figcaption></figcaption></figure>

Next, click [**Schedule Pipeline**](creating-a-data-product-by-cdo-technical-persona.md#schedule-pipeline).
{% endtab %}

{% tab title="Schedule Pipeline" %}
**Overview**

**Scheduling pipeline** helps automate the execution of the data processing workflow at specified times or intervals. This ensures that the data product is regularly updated with the latest processed data, reducing manual effort and keeping it available and relevant for its intended business use case.

**Procedure**

The below step-by-step instructions help you understand how to schedule the pipeline:

_**To schedule pipeline**_

1. On the **Use Case** page, click the <img src="../../../.gitbook/assets/image (2562).png" alt="" data-size="line">button under **Schedules.**

<figure><img src="../../../.gitbook/assets/image (2569).png" alt=""><figcaption></figcaption></figure>

The Scheduler page is displayed.

2. On the **Scheduler** page, in the **ETL Job** section:

{% stepper %}
{% step %}
**Select Job**

A. From the **Choose from a list of ETL Jobs**, select the **ETL Job** on the **Action** tab.

B. Click the **Job Parameters** tab, and then specify **job parameters.**

C. Click the **Condition** tab, and then specify the **Failure and Success** conditions.

D. Click the **Next** button.

<figure><img src="../../../.gitbook/assets/image (2572).png" alt=""><figcaption></figcaption></figure>

The **Frequency** section is displayed.
{% endstep %}

{% step %}
**Setup Frequency**

A. Specify the **Frequency** choosing from **Run Once, Daily, Weekly,** or **Monthly.**

B. Specify the **Start Date** and **Start Time.**

C. Click the **Next** button.

<figure><img src="../../../.gitbook/assets/image (2574).png" alt=""><figcaption></figcaption></figure>

The **External Dependency** section is displayed.
{% endstep %}

{% step %}
**External Dependency**

A. On the **External Dependency** section, specify **Yes** or **No** to **external dependency.**

B. Click the **Next** button.

<figure><img src="../../../.gitbook/assets/image (2575).png" alt=""><figcaption></figcaption></figure>

The **Finish** section is displayed.
{% endstep %}

{% step %}
**Finish**

On the **Finish** section, specify Scheduler Name, Description, Technical Owner, Server, and then click the Finish button.

<figure><img src="../../../.gitbook/assets/image (2577).png" alt=""><figcaption></figcaption></figure>

The scheduler is defined and reflected in the Scheduler drop-down box on the Use Case page.

<figure><img src="../../../.gitbook/assets/image (2579).png" alt=""><figcaption></figcaption></figure>


{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Save Data Product Use Case" %}
**Overview**

**Saving the Data Product Use Case** as the final step stores the completed use case and its associated configurations, making it available for future reference and use. This ensures that the defined business requirement and the selected resources, such as data assets, pipelines, and other components, are preserved as part of the data product creation process.

**Procedure**

1. Scroll down to the bottom of **Use Case** page, and then click **Save Data Product Use Case** button.

<figure><img src="../../../.gitbook/assets/image (2581).png" alt=""><figcaption></figcaption></figure>

The **Save Data Product** dialogue box is displayed.

2. On the **Save Data Product** dialogue box, click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (2582).png" alt=""><figcaption></figcaption></figure>

The **Data product saved successfully** message is displayed.
{% endtab %}

{% tab title="Download Documentation" %}
**Overview**

After saving the **Data Product Use Case**, downloading the documentation helps generate a record of the use case and its associated details, such as the business requirement, selected resources, configurations, and other relevant information.&#x20;

This documentation can be used for **reference, sharing, review, governance, and future maintenance** of the data product.

**Procedure**

1. After saving the data product use case, click the **Documentation** button.

<figure><img src="../../../.gitbook/assets/image (2583).png" alt=""><figcaption></figcaption></figure>

The PDF is generated and downloaded. See the success message in the below image.

<figure><img src="../../../.gitbook/assets/image (2584).png" alt=""><figcaption></figcaption></figure>

x
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Registering a Data Product**](registering-a-data-product.md)
* [**Deploying a Data Product**](deploying-a-data-product.md)
* [**Managing Data Products**](managing-data-products.md)
* [**Managing Bundles**](managing-bundles.md)
* [**Managing Product Deployments**](managing-product-deployments.md)

