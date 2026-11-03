---
hidden: true
icon: page
---

# Managing Data Dictionary

***

**Contents**

* [**Instructions for Using this Page**](managing-data-dictionary.md#instructions-for-using-this-page)
* [**Overview**](managing-data-dictionary.md#overview)
* [**Data Dictionary Management Activities**](managing-data-dictionary.md#data-dictionary-management-activities)
* [**Related Topics**](managing-data-dictionary.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

The **Data Dictionary** contains three tabs—**Business**, **Technical**, and **User**—each designed to manage a specific category of metadata for the selected data asset. Although the metadata displayed differs across the tabs, the available management activities are largely the same.

***

## **Data Dictionary Management Activities**

As part of **Data Dictionary Management**, you can manage business, technical, and user-defined metadata for data assets. In addition, you can define keys and relationships, map business terms, import and export metadata, generate AI-powered definitions, and save the updated Data Dictionary.

> <mark style="color:red;">**Note:**</mark> It is not mandatory to perform all of the metadata management activities described below. You can perform only the activities that are relevant to your requirements. After completing the necessary updates, you can preview the changes and save the Data Dictionary to apply them.

<details>

<summary><strong>Defining Business Name</strong></summary>

**Purpose**

In the **Business Data Dictionary**, the **Business Name** is a business-friendly name assigned to a technical table or column. It is intended for business users, so it should be meaningful and easy to understand, unlike technical database name&#x73;**.**

**Procedure**

> <mark style="color:red;">**Note:**</mark> The below mentioned procedure is applied to User tab also.

1. On the **Data Dictionary** page, in the **Business Name** column, enter the required **business name** for the required element. For example replacing GL Header ID as General Ledger Header ID.

<figure><img src="../../../../.gitbook/assets/image (2301).png" alt=""><figcaption></figcaption></figure>

2. To save the changes, click the **Update** button.

The changes are saved successfully, and a confirmation message is displayed.

</details>

<details>

<summary><strong>Finding and Replacing Values</strong></summary>

**Overview**

The **Find and Replace Status** feature enables you to locate metadata entries with a specified status and replace them with another status in bulk. This helps streamline metadata maintenance, improve consistency, and reduce the effort required to update multiple records individually.

**Procedure**

> <mark style="color:red;">**Note:**</mark> The steps described below are common to the **Business**, **Technical**, and **User** tabs. The only difference is the type of metadata managed in each tab.

1. On the **Data Dictionary** page, select the required **tab**. For example, Business.
2. Select either **All Rows** or **Selected Rows**, depending on the scope of the update.
3. In the **Find and Replace** section, select the **column** in which you want to find and replace values. For example, Status.
4. Select the **value** to find and the value with which you want to replace it. For example, Draft.

<figure><img src="../../../../.gitbook/assets/image (2303).png" alt=""><figcaption></figcaption></figure>

The values are replaced. See the image below:

<figure><img src="../../../../.gitbook/assets/image (2304).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Mapping Business Terms to Element Names</strong></summary>

**Overview**

**Mapping a Business Term to an Element Name** associates a business term with a table column or data field. This helps users understand what the data represents, improves consistency in business terminology, and makes data easier to understand and manage.

**Procedure**

> <mark style="color:red;">**Note:**</mark> The steps described below are common to the **Business**, **Technical**, and **User** tabs. The only difference is the type of metadata managed in each tab.

1. On the **Data Dictionary** page, from the **Element Name** column, select the required **element.** For example, EmployeeType.
2. From  the **Business term** column, select the **business term** relevant to the selected elemen&#x74;**.** For example, Human Resources.
3. Click the **Update** button on the top right corner of the page.

<figure><img src="../../../../.gitbook/assets/image (2305).png" alt=""><figcaption></figcaption></figure>

The mapping is done and the success message is displayed.

> <mark style="color:red;">**Note:**</mark> Alternatively, you can use auto mapping also by clicking the ![](<../../../../.gitbook/assets/image (2306).png>) on the top of the page.

</details>

<details>

<summary><strong>Adding Foreign Key</strong></summary>

**Overview**

A **Foreign Key** identifies a column (or group of columns) in one table that references the primary key of another table. In the Data Dictionary, it documents these relationships so that users can understand how data is connected across tables.

**Procedure**

> <mark style="color:red;">**Note:**</mark> The steps described below are common to the **Business**, **Technical**, and **User** tabs.&#x20;

1. On the **Data Dictionary** page, click the **Foreign Key** button on the top of the page.

<figure><img src="../../../../.gitbook/assets/image (2308).png" alt=""><figcaption></figcaption></figure>

The **Add Foreign Key** dialogue box is displayed.

2. On the **Add Foreign Key** dialogue box (See the below image):

A. In the **Source** section, select the **Connection, Source Table,** and **Column.**

B. In the **Target** section, select the **Connection, Target Table,** and **Column.**

C. Click the **Add** button.

The foreign key is added.

D. Finally, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/image (2309).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Previewing Data</strong></summary>

**Overview**

The **Preview** feature enables you to review the metadata changes before saving them to the Data Dictionary. It allows you to verify that the updates are accurate and complete, helping prevent incorrect or unintended changes from being saved.

**Procedure**

> <mark style="color:red;">**Note:**</mark> The steps described below are common to the **Business**, **Technical**, and **User** tabs.&#x20;

* On the **Data Dictionary** page, click the **Preview** button on the top of the page.

<figure><img src="../../../../.gitbook/assets/image (2310).png" alt=""><figcaption></figcaption></figure>

The Preview screen is displayed.

</details>

<details>

<summary><strong>Applying Data Profiling</strong></summary>

**Overview**

**Data Profiling,** which enables data cleaning improves the quality of a dataset by identifying and correcting errors, inconsistencies, duplicate records, and missing values. It ensures that the data is accurate, complete, and consistent, making it suitable for reporting, analytics, and other business processes.

**Procedure**

> <mark style="color:red;">**Note:**</mark> The steps described below are common to the **Business**, **Technical**, and **User** tabs.&#x20;

* On the **Data Dictionary** page, click the **Preview** button on the top of the page.

<figure><img src="../../../../.gitbook/assets/image (2310).png" alt=""><figcaption></figcaption></figure>

The Preview screen is displayed.

2. On the Preview screen, click the **EDA** button at the bottom of the screen.

<figure><img src="../../../../.gitbook/assets/image (2311).png" alt=""><figcaption></figcaption></figure>

The **Data Profiling** page is opened in a new window.

3. On the **Left Pane** of **Data Profiling** page, in the **Data Cleansing** section, click the **Fill cell value** or **Fill empty cells** **with above** to clean the data.
4. If you want apply **Masking**:

A. Click **Data Masking** and then select **Auto, Custom,** or **Protegrity.**

B. Click the **Submit** button.

<figure><img src="../../../../.gitbook/assets/image (2268).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Applying DQ Rules</strong></summary>

**Overview**

Applying **Data Quality (DQ) Rules** to metadata helps ensure that data assets meet predefined quality standards. These rules validate the accuracy, completeness, consistency, and integrity of data, enabling organizations to identify and address data quality issues before the data is used for reporting, analytics, or business operations.

**Procedure**

> <mark style="color:red;">**Note:**</mark> The steps described below are common to the **Business**, **Technical**, and **User** tabs.&#x20;

* On the **Data Dictionary** page, click the **Preview** button on the top of the page.

<figure><img src="../../../../.gitbook/assets/image (2310).png" alt=""><figcaption></figcaption></figure>

The Preview screen is displayed.

2. On the **Preview** screen, click the **DQ Rules** button at the bottom of the screen.

<figure><img src="../../../../.gitbook/assets/image (2258).png" alt=""><figcaption></figcaption></figure>

The **DQ Rules** page is opened in a new window.

3. On the **DQ Rules** page, define the quality by specifying the required **column, operator, value, rule name,** and **DQ dimensions**, and then click the **Test** button.

<figure><img src="../../../../.gitbook/assets/image (2312).png" alt=""><figcaption></figcaption></figure>

The Data Quality page is displayed.

4. Click the **Apply** button. See the below image.

The DQ rules are applied.

5. Next, click the **Save** button to save DQ rules.

<figure><img src="../../../../.gitbook/assets/image (2261).png" alt=""><figcaption></figcaption></figure>

The Save DQ dialogue box is displayed.

6. On the **Save DQ** dialogue box, specify a **name** for the DQ rule, and then click the **Save** button.

<figure><img src="../../../../.gitbook/assets/image (2262).png" alt=""><figcaption></figcaption></figure>

The DQ Rule is saved and the **Success** message is displayed.

</details>

<details>

<summary><strong>Defining Composite Key</strong></summary>

**Overview**

The **Define Composite Key** feature enables you to specify a combination of two or more columns that together uniquely identify each record in a table.&#x20;

Documenting composite keys in the Data Dictionary helps users understand the table structure, maintain data integrity, establish relationships between tables, and support effective metadata management.

**Procedure**

> <mark style="color:red;">**Note:**</mark> The steps described below are common to the **Business**, **Technical**, and **User** tabs.&#x20;

* On the **Data Dictionary** page, specify the **Composite Key, Table Business Name, Table Description,** and then click the **Update** button.

<figure><img src="../../../../.gitbook/assets/image (2263).png" alt=""><figcaption></figcaption></figure>

The composite key is defined.

</details>

<details>

<summary><strong>Creating Definitions from LLM</strong></summary>

**Overview**

The **Create Definitions from LLM** feature uses a **Large Language Model (LLM)** to automatically generate business-friendly definitions for tables, columns, or other metadata assets. Instead of manually writing definitions, you can leverage AI to create meaningful descriptions quickly and consistently.

**Procedure**

> <mark style="color:red;">**Note:**</mark> The steps described below are common to the **Business**, **Technical**, and **User** tabs.&#x20;

* On the **Data Dictionary** page, turn on the **Create definitions from LLM** option.

The LLM denitions are displayed.

<figure><img src="../../../../.gitbook/assets/image (2264).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> You can review and modify the generated definitions before saving them.

</details>

<details>

<summary><strong>Export Metadata</strong></summary>

**Overview**

The **Export** feature enables you to export the metadata dictionary to **Microsoft Excel** or to the **AWS Glue Data Catalog**. Exporting to Excel provides a convenient way to review, analyze, share, and maintain metadata offline, whereas exporting to AWS Glue publishes the metadata to a centralized catalog, enabling data discovery and seamless integration with AWS analytics and data processing services.

**Procedure**

> <mark style="color:red;">**Note:**</mark> The steps described below are common to the **Business**, **Technical**, and **User** tabs.&#x20;

1. **Exporting to Excel**

* On the **Data Dictionary** page, from the **File Download/Export** drop-down box, select **Excel**.

<figure><img src="../../../../.gitbook/assets/image (2265).png" alt=""><figcaption></figcaption></figure>

The metadata is downloaded in Excel format in your local system.

2. **Exporting to Glue**

A. On the **Data Dictionary** page, from the **File Download/Export** drop-down box, select **Glue**.

The Export dialogue box is displayed.

B. On the **Export** dialogue box, select **connection, database,** and **table,** and then click the **Export** button.

<figure><img src="../../../../.gitbook/assets/image (2266).png" alt=""><figcaption></figcaption></figure>

The table is exported to Glue and the Success message is displayed.

> <mark style="color:red;">**Note:**</mark> If you want to export the data to a new table, then select the select the **Create New Table** option on the **Export** dialogue box, and specify the **Table Name.**&#x20;

</details>

<details>

<summary><strong>Save Data Dictionary</strong></summary>

* On the **Data Dictionary** page, click the **Save Dictionary** button.

<figure><img src="../../../../.gitbook/assets/image (2267).png" alt=""><figcaption></figcaption></figure>

The data dictionary is saved.

</details>

***

## Related Topics

* [**Accessing Data Dictionary**](accessing-data-dictionary.md)
* [**Data Dictionary Tabs**](data-dictionary-tabs.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
