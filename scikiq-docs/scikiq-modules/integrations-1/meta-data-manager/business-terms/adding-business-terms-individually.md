---
hidden: true
icon: page
---

# Adding Business Terms Individually

***

**Contents**

* [**Instructions for Using this Page**](adding-business-terms-individually.md#instructions-for-using-this-page)
* [**Overview**](adding-business-terms-individually.md#overview)
* [**Procedure**](adding-business-terms-individually.md#procedure)
* [**Related Topics**](adding-business-terms-individually.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

Adding business terms **individually** allows you to create and maintain business definitions one term at a time. This approach is useful when introducing new business concepts, updating the business glossary incrementally, or when only a small number of terms need to be added.

***

## **Procedure**

Expand the below panels to view step-by-step instructions:

<details>

<summary><strong>Navigate to Business Terms Menu</strong></summary>

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

&#x20;     The Meta Data Manager menu is displayed.

2. From the **Meta Data Manager** menu, click **Business Terms.**

<figure><img src="../../../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

The Business Terms page is displayed.

</details>

<details>

<summary><strong>Enter Business Term Details</strong></summary>

**Overview**

As part of entering **Business Term Details**, you need to provide information across several sections, including **Term Information**, **Term Ownership**, **Classification and Governance**, and **Extended Attributes**.&#x20;

These details help define the business term, identify its ownership and stewardship, establish governance controls, and capture any additional metadata required by the organization.

**Procedure**

* On the Business Terms page, under **Add Business Terms** tab, specify **Term Information**, **Term Ownership**, **Classification and Governance**, and **Extended Attributes**.&#x20;

> <mark style="color:red;">**Note:**</mark> The below **Field Description** table provides descriptions of the fields available in the Business Term Details section and guidance on the information to be entered in each field.

<figure><img src="../../../../.gitbook/assets/image (2279).png" alt=""><figcaption></figcaption></figure>



**Field Description**

<table><thead><tr><th width="144.55560302734375" valign="top">Field</th><th valign="top">Description</th><th valign="top">Example Input</th></tr></thead><tbody><tr><td valign="top"><strong>Terms Name</strong></td><td valign="top">In this field, specify the <strong>name</strong> of the business term.</td><td valign="top">Patient Record, Customer, Revenue</td></tr><tr><td valign="top"><strong>Definition</strong></td><td valign="top">In this field, provide a clear and standardized <strong>description of the business term</strong> and its meaning within the organization.</td><td valign="top">Revenue is the total income generated from the sale of products or services before expenses are deducted.</td></tr><tr><td valign="top"><strong>Purpose</strong></td><td valign="top">In this field, provide the <strong>business objective or reason</strong> for maintaining the term.</td><td valign="top">To standardize the definition of revenue across reports and business units.</td></tr><tr><td valign="top"><strong>Business Process</strong></td><td valign="top">From this drop-down box, select the business process or functional area to which the term belongs.</td><td valign="top">Business Process</td></tr><tr><td valign="top"><strong>Owner</strong></td><td valign="top">From this drop-down box, select the <strong>individual or team</strong> responsible for maintaining and approving the business term.</td><td valign="top">Finance Team, Data Governance Team, John Smith</td></tr><tr><td valign="top"><strong>Catalogue</strong></td><td valign="top">From this drop-down box, select the <strong>metadata catalogue</strong> in which the business term is stored and managed</td><td valign="top">Enterprise Data Catalogue</td></tr><tr><td valign="top"><strong>Glossary</strong></td><td valign="top">From this drop-down box, select the <strong>glossary</strong> that groups related business terms.glossary that groups related business terms.</td><td valign="top">Healthcare Glossary, Customer Management Glossary</td></tr><tr><td valign="top"><strong>Category</strong></td><td valign="top">From this drop-down box, select the <strong>business term</strong> <strong>into a</strong> <strong>logical business category</strong> for easier organization and discovery.</td><td valign="top">Financial Metrics, Customer Information, Healthcare Data</td></tr><tr><td valign="top"><strong>Status</strong></td><td valign="top">From this drop-down box, select the <strong>current lifecycle state</strong> of the business term.</td><td valign="top">Draft</td></tr><tr><td valign="top"><strong>Sensitive</strong></td><td valign="top">From this drop-down box, select the <strong>term</strong> associated with sensitive or regulated data.</td><td valign="top">GDPR, PII</td></tr><tr><td valign="top"><strong>Classification</strong></td><td valign="top">From this drop-down box, select the  <strong>acronyms, or abbreviations</strong> commonly used for the business term.</td><td valign="top">Internal, Confidential, Restricted, Public</td></tr><tr><td valign="top"><strong>Regulatory Rule</strong></td><td valign="top">From this drop-down box, select the <strong>regulatory rule</strong> applicable to the business term</td><td valign="top">GDPR</td></tr><tr><td valign="top"><strong>Industry Standard</strong></td><td valign="top">From this drop-down box, select the industry standards or frameworks associated with the business term.</td><td valign="top">HIPAA, GDPR</td></tr></tbody></table>

</details>

<details>

<summary><strong>Configure Physical Schema Mapping</strong></summary>

1. After entering the business term details, click the **Physical Schema Mapping** button.

<figure><img src="../../../../.gitbook/assets/image (2280).png" alt=""><figcaption></figcaption></figure>

The **Physical Schema Mappin**g dialogue box is displayed.

2. On the **Physical Schema Mappin**g dialogue box, select the **Connection, Table, Column**, and then click the **Save** button.

> <mark style="color:red;">**Note:**</mark> Here is the description for **Connection, Table,** and **Column.**
>
> * **Connection:** Refers to the **data source connection** that contains the physical table and column to be mapped to the business term.
> * **Table:** Refers to the **database table** that contains the physical representation of the business term.
> * **Column:** Refers to the **column within the selected table** that corresponds to the business term.

<figure><img src="../../../../.gitbook/assets/image (2281).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * If you want to **add** a new mapping row to associate the business term with additional tables or columns, click the ![](<../../../../.gitbook/assets/image (2195).png>)button.
> * If you want to delete an existing mapping row, click the **Delete**![](<../../../../.gitbook/assets/image (2196).png>)button.

3. Finally, click the **Submit** button.

The Business Term is added.

</details>

***

## Related Topics

* [**Managing Business Terms**](../../../integrations/meta-data-manager/business-terms/managing-business-terms.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
