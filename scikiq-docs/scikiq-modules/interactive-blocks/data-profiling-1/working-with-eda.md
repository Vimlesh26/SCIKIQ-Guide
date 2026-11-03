---
icon: page
---

# Working with EDA

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes the tasks that can be performed after an EDA has been created. It includes features for reviewing and profiling data, managing column metadata, defining Data Quality (DQ) rules, and maintaining EDA versions. It also explains how to download sample data and export the processed EDA results. These capabilities help prepare, validate, and manage data for downstream analysis and processing.

***

### **Working with EDA**

{% tabs %}
{% tab title="Create Custom Column Tags" %}
**Overview**

**Create Tags** enables you to define custom tags for classifying and organizing datasets and columns. While SCIKIQ provides PII as a default tag, you can create additional tags to meet your organization's business, governance, and data management requirements. Custom tags make it easier to search, manage, and identify data assets across the platform.

***

**Procedure**

The below Procedure section help you understand how to create custom tags:

1. On the **EDA** tab, click the **Tags** button in the required column.

<figure><img src="../../../.gitbook/assets/image (2431).png" alt=""><figcaption></figcaption></figure>

The **Column Tags** dialogue box is displayed.

2. On the **Column Tags** dialogue box, select the required **tag**, and then click the **Save** button.

The tag is created.
{% endtab %}

{% tab title="View Column Summary" %}
**Overview**

**Viewing Column Summary** provides a summary of the selected column, including its data type, value distribution, and key statistics. This information helps you understand the quality and characteristics of the data, identify potential issues, and determine the appropriate transformations before analysis or further processing.

***

**Procedure**

The below step-by-step instructions help you understand how to view column summary:

1. On the **Data Profiling** page, click the **Summary** button on the **Top Menu**.

<figure><img src="../../../.gitbook/assets/image (2432).png" alt=""><figcaption></figcaption></figure>

The **Column Summary** screen is displayed.

2. On the **Column Summary** screen, review the data, and then click the **Close** button.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * Use the **Pagination** feature ![](<../../../.gitbook/assets/image (2434).png>) to navigate between pages.
> * If you want to view the summary of another column, then select that columnn from the **Select Column** drop-down box.
>
> See the image below:

<figure><img src="../../../.gitbook/assets/image (2435).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Define DQ Rules" %}
**Overview**

The purpose of **defining Data Quality (DQ) rules** is to establish the criteria and business rules that data must satisfy to be considered accurate, complete, consistent, and valid. These rules serve as a standard for evaluating and maintaining data quality across datasets.

***

**Procedure**

In the SCIKIQ application, you can define a DQ rule by specifying attributes such as the **target column, operator, comparison value, rule name,** and the applicable **data quality dimension**.&#x20;

After defining a rule, you can test it to verify its effectiveness, review the validation results, and apply the rule to the dataset during exploratory data analysis (EDA). Once validated, the rule can be saved for future use.

> <mark style="color:red;">**Note:**</mark> You can define/apply multiple rules to a column.

The below **step-by-step instructions** help you understand how to define data quality rules:

_**To define DQ rules**_

1. On the **Data Profiling** page, click the **Define DQ Rules** button on the **Top Menu.**

The **Data Quality Rules** page is displayed in a new window.

2. On the **DQ Rules** page, define the quality by specifying the required **column, operator, value, rule name,** and **DQ dimensions**, and then click the **Test** button.

<figure><img src="../../../.gitbook/assets/image (2412).png" alt=""><figcaption></figcaption></figure>

The Rule List page is displayed with the applied data quality rule test result.&#x20;

<figure><img src="../../../.gitbook/assets/image (2413).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * To **remove** a rule, click the **Delete** ![](<../../../.gitbook/assets/image (2414).png>) button corresponding to that rule.
> * To **view** the rule information of a rule, click the **Rule Information** ![](<../../../.gitbook/assets/image (2415).png>) button.
> * To **test** a rule, click the **Test Rule** ![](<../../../.gitbook/assets/image (2416).png>) button corresponding to it.

3. Next, on the  **Rule List** page, click the **Apply** button.

<figure><img src="../../../.gitbook/assets/image (2420).png" alt=""><figcaption></figcaption></figure>

The specified DQ rule are applied and the **Success** message is displayed.

4. Now, click the **Save** button to save the applied DQ rules.

<figure><img src="../../../.gitbook/assets/image (2422).png" alt=""><figcaption></figcaption></figure>

The **Save DQ** dialogue box is displayed.

5. On the **Save DQ** dialogue box, specify a **name** for the DQ rule, and then click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (2423).png" alt=""><figcaption></figcaption></figure>

The defined DQ rules are saved and the **Success** message is displayed. See the image below.

<figure><img src="../../../.gitbook/assets/image (2424).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Create a New EDA Version" %}
**Overview**

The purpose of **Creating a New EDA Version** is to preserve the current state of an EDA while allowing users to continue making changes without affecting the previous version. Versioning helps track changes, compare different iterations, and restore an earlier version if needed.

***

**Procedure**

The below **step-by-step instructions** help you understand how to create a new EDA version:

_**To create a new EDA version**_

1. On the **Data Profiling** page, click the **Save** button on the **Top Menu.**

<figure><img src="../../../.gitbook/assets/image (2437).png" alt=""><figcaption></figcaption></figure>

The **Save EDA** dialogue box is displayed.

2. On the **Save EDA** dialogue box:

A. Turn on the **Create New Version** option.

The Name and Description fields are displayed.

B. In the **Name** and **Description** fields, enter a **name** and **description** for the new version.

<figure><img src="../../../.gitbook/assets/image (2438).png" alt=""><figcaption></figcaption></figure>

The new version is created with the specified name.

<figure><img src="../../../.gitbook/assets/image (2440).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Download Sample Data" %}
**Overview**

**Download Sample Data** enables you to download a representative subset of the dataset for review and validation. It helps you verify data quality, inspect the results of profiling or transformations, and confirm that the data is ready for analysis, reporting, or further processing without downloading the entire dataset.

***

**Procedure**

The below step-by-step instructions help you understand how to download sample data:

1. On the **Data Profiling** page, click the **Download Sample** button on the **Top Menu**.

<figure><img src="../../../.gitbook/assets/image (2436).png" alt=""><figcaption></figcaption></figure>

The **Column Summary** screen is displayed.

2. On the **Column Summary** screen, review the data, and then click the **Close** button.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * Use the **Pagination** feature ![](<../../../.gitbook/assets/image (2434).png>) to navigate between pages.
> * If you want to view the summary of another column, then select that columnn from the **Select Column** drop-down box.
>
> See the image below:

<figure><img src="../../../.gitbook/assets/image (2435).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Export EDA" %}
**Overview**

The **Export EDA** enables you to export the profiled and transformed dataset for use outside the EDA environment. Exporting allows you to save, share, archive, or integrate the processed data with reporting, analytics, machine learning, and other downstream applications.

***

**Procedure**

The below step-by-step instructions help you understand how to export the EDA:

1. On the **Data Profiling** page, click the **Export EDA** button on the **Top Menu**.

<figure><img src="../../../.gitbook/assets/image (2488).png" alt=""><figcaption></figcaption></figure>

The **EDA** is downloaded in Excel format in your local system.

2. Browse to the location where the **Excel** file is downloaded, and then click it view the EDA data.

<figure><img src="../../../.gitbook/assets/image (2425).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

***

### **Related Topics**

* [**Performing Data Profiling**](performing-data-profiling/)
