---
icon: page
---

# Creating a Data Product by Business Persona

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The process of creating a data product as a **Business Persona** involves a series of steps. These include _defining use case, explore and select a data product, generating dashboard, smart Profiling, generating pipelines, scheduling pipelines, saving the data product use case, and downloading the documentation._

The below Procedure section provides a detailed description of each of these:

***

### Procedure

Click on the below tabs to view step-by-step instructions:

{% tabs %}
{% tab title="Defining Use Case" %}
**Overview**

Defining a **use case** while creating a data product helps clearly identify the **business problem, objectives, and expected outcome** that the data product is intended to address. This provides direction for selecting the right data, resources, and configurations, ensuring that the data product is relevant and aligned with the intended business need.

> <mark style="color:red;">**Note:**</mark> You can interact with SCIKIQ Chatbot to define the use case.

**Procedure**

The below step-by-step instructions help you understand how to define a use case.

_**To define a use case**_

1. On the SCIKIQ **SCIKIQ Left Menu**, expand **Data Product Factory** under **ML/GENAI STUDIO**, and then click **Data Product/Business Persona.**

<figure><img src="../../../.gitbook/assets/image (2693).png" alt=""><figcaption></figcaption></figure>

&#x20;The **Data Product** page is displayed.

2. On the **Data Product** page, click the **Click here** button on the right pane.

<figure><img src="../../../.gitbook/assets/image (2695).png" alt=""><figcaption></figcaption></figure>

The **SCIKIQ Chatbot** is displayed.

3. On the **SCIKIQ Chatbot,** enter your **prompt** in the **chat window,** and then click the **Send** button.&#x20;

{% hint style="info" %}
**Here is an example prompt**

I want to provide physical security services to old age people who are not mentally and physically alert. If from sensors there is a signal of security breach, it should trigger alarm and raise concern to old age home resident.
{% endhint %}

> <mark style="color:red;">**Note:**</mark> Instead of typing, you can give a **voice prompt** by clicking the **Speak** ![](<../../../.gitbook/assets/image (2698).png>) icon in the chat window.&#x20;

<figure><img src="../../../.gitbook/assets/image (2699).png" alt=""><figcaption></figcaption></figure>

A list of suggested data products is displayed on the left pane. See the below image.

<figure><img src="../../../.gitbook/assets/image (2685).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Explore and Select Data Product" %}
**Overview**

Exploring and selecting a **data product suggested by the chatbot** helps you identify an existing product that best matches your defined use case and business requirements. This can save time and effort by allowing you to review relevant recommendations and select a suitable data product instead of creating or configuring one entirely from scratch.

**Procedure**

The below step-by-step instructions help you understand how to explore and select a data product:

_**To explore and select a data product**_

1. In the left pane, select the required **data product.**  For example Real-Time Security Alerts Dashboard.

<figure><img src="../../../.gitbook/assets/image (2702).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> You may explore all the data products list in the left pane.

The selected data  product details including Stakeholders, Monetization Strategy, and Integration Strategy are displayed as collapsible panels on the right pane.

2. Expand the collapsible panels to view the complete details.

<figure><img src="../../../.gitbook/assets/image (2677).png" alt=""><figcaption></figcaption></figure>
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

Next, click [**Smart Profiler**](creating-a-data-product-by-business-persona.md#smart-profiler)**.**
{% endtab %}

{% tab title="Smart Profiling" %}
**Overview**&#x20;

**Smart Profiling** helps while creating a data product by automatically analyzing the selected data and providing insights into its structure, content, and quality. It helps identify key characteristics such as data types, patterns, missing values, and potential data issues, enabling you to better understand the data and select the most relevant and suitable data assets for the data product.

**Procedure**

* On the **Use Case** page, click the **Smart Profiler** button under **Chat as a Product.**

<figure><img src="../../../.gitbook/assets/image (2642).png" alt=""><figcaption></figcaption></figure>

The **Smart Profiler** page is displayed with analyzing the data. Once the analysis is completed the page is displayed as shown below. You can view the summary, data summary, and insights.

<figure><img src="../../../.gitbook/assets/image (2561).png" alt=""><figcaption></figcaption></figure>

Next, click [**Generate Pipelines**](creating-a-data-product-by-business-persona.md#generate-pipelines)
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

On the **Finish** section, specify S**cheduler Name, Description, Technical Owner, Server,** and then click the **Finish** button.

<figure><img src="../../../.gitbook/assets/image (2577).png" alt=""><figcaption></figcaption></figure>

The scheduler is defined and reflected in the Scheduler drop-down box on the Use Case page.

<figure><img src="../../../.gitbook/assets/image (2579).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Save the Data Product Use Case " %}
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
