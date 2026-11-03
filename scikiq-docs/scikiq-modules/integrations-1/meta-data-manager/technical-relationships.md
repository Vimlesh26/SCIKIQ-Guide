---
icon: page
---

# Technical Relationships

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to manage technical relationships. Technical relationships define how database tables or data elements are connected to one another through structural links, such as primary keys, foreign keys, and common columns.

For example, a **Customer table** and an **Order table** may be connected through the **Customer\_ID** column. This relationship indicates which customer placed each order.

***

### Manage Technical Relationships

As part of managing **Technical Relationships**, you can perform the following tasks:

* **Filtering Technical Relationships:** As part of this, you can filter the technical relationships by Join Types and Cardinalities.
* **Viewing Join Details:** As part of this, you can view Join Information, Join Conditions, and SQL Preview.

Click the below tabs to view step-by-step instructions for each of the above mentioned tasks.

{% tabs %}
{% tab title="Navigating to  Data Element Page" %}
**Overview**

This section describes how to navigate to the **Technical Relations** page. Follow the below mentioned step-by-step instructions.

**Procedure**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

&#x20;     The Meta Data Manager menu is displayed.

2. From the **Meta Data Manager** menu, select **Technical Relations.**

<figure><img src="../../../.gitbook/assets/image (3060).png" alt=""><figcaption></figcaption></figure>

The **Technical Relations** page is displayed.

<figure><img src="../../../.gitbook/assets/image (3061).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Filtering Technical Relationships" %}
**Overview**

This section describes how to filter technical relationships. **Filtering technical relationships** helps to quickly identify relationships based on how tables are joined and how their records are associated, making it easier to review and manage relationships.

**Procedure**

You can filter the technical relationships by by **join type** and **cardinality**.  The following instructions explain how to apply these filters:

_**To filter technical relationships**_

1. Navigate to **Technical Tables** page. (SCIKIQ Left Navigation Bar>> SCIKIQ Control>>Meta Data Manager>>Technical Relationships)

The **Technical Relationships** page is displayed.

2. On the **Technical Relationships** page, select the required **Join Type, Cardinality**, and click the **Apply** button.

> <mark style="color:red;">**Note:**</mark> The purpose of Join Types and Cardinalities is described below.

<figure><img src="../../../.gitbook/assets/image (3062).png" alt=""><figcaption></figcaption></figure>

**Description of Join Types**

{% hint style="info" %}
* **Inner Join:** Retrieves only the records that have matching values in both tables.
* **Left Join:** Retrieves all records from the left table and the matching records from the right table. If no match exists, the right table's columns contain NULL values.
* **Right Join:** Retrieves all records from the right table and the matching records from the left table. If no match exists, the left table's columns contain NULL values.
* **Full Outer Join:** Retrieves all records from both tables, including matching and non-matching records. Missing matches are represented by NULL values.
* **Not Set (Data Model):** Indicates that no join type has been explicitly specified, allowing the data model's default configuration or relationship settings to determine how the tables are joined.
{% endhint %}

**Description of Cardinalities**

{% hint style="info" %}
* **One to One (1:1):** Each record in one table is associated with at most one record in the other table, and vice versa.
* **One to Many (1:N):** One record in a table can be associated with multiple records in the related table.
* **Many to One (N:1**): Multiple records in one table can be associated with a single record in the related table.
* **Many to Many (N:N):** Multiple records in one table can be associated with multiple records in the other table.
* **Not Set (Data Model):** Indicates that no cardinality has been explicitly specified.
{% endhint %}

The Technnical Relationships are displayed as per the selected join type and cardinality.
{% endtab %}

{% tab title="Viewing Join Details" %}
**Overview**

This section describes how to view a join details. **Viewing join details** helps to verify the criteria used to link tables and review the generated SQL query to understand how the join is executed. This helps validate join configurations, identify potential errors, and ensure that related data is retrieved as expected.

**Procedure**

When viewing join details, you can review the **join information, join conditions**, and **SQL preview**. The below instructions help you understand how to view join details:

_**To view join details**_

1. Navigate to **Technical Tables** page. (SCIKIQ Left Navigation Bar>> SCIKIQ Control>>Meta Data Manager>>Technical Relationships)

The **Technical Relationships** page is displayed.

2. On the **Technical Relationships** page, click the **View Join Details** icon corresponding to the required technical relationship.

<figure><img src="../../../.gitbook/assets/image (3063).png" alt=""><figcaption></figcaption></figure>

The **Join Details** screen is displayed. See the below image.

<figure><img src="../../../.gitbook/assets/image (3064).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

### **Related Topics**

* [**Assets**](../../integrations/meta-data-manager/assets/)
* [**Data Dictionary**](../../integrations/meta-data-manager/data-dictionary/)
* [**Dataset Metadata**](../../integrations/meta-data-manager/dataset-metadata/)
* [**Glossary**](../../integrations/meta-data-manager/glossary/)
* [**Table Classification**](../../integrations/meta-data-manager/table-classification.md)
