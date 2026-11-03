---
icon: page
---

# Business Terms

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

**Business Terms** enable organizations to define and maintain a standardized business vocabulary within the Metadata Manager. They provide clear definitions for key business concepts, helping users understand the meaning and context of data assets.&#x20;

By linking business terms to datasets, data elements, and other metadata objects, organizations can improve data governance, enhance data discovery, and ensure consistent interpretation of information across the enterprise.

***

### Manage Business Terms

As part of managing business terms, you can create terms individually or upload multiple terms in bulk. During creation, business terms can be associated with the appropriate glossary to ensure consistent organization and governance. You can also export business terms in CSV format for reporting, sharing, or backup purposes.

In addition, the module allows you to search, view, update, share, and delete business terms as needed, enabling efficient management of the organization's business vocabulary throughout its lifecycle.

{% tabs %}
{% tab title="Adding Business Terms Individually" %}
**Overview**

Adding business terms **individually** allows you to create and maintain business definitions one term at a time. This approach is useful when introducing new business concepts, updating the business glossary incrementally, or when only a small number of terms need to be added.

***

**Procedure**

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
{% endtab %}

{% tab title="Adding Business Terms in Bulk" %}
**Overview**

Adding business terms **in bulk** enables you to create multiple business terms simultaneously by importing them from a file. This approach saves time and effort when onboarding large numbers of terms into the Metadata Manager.

***

**Procedure**

The below step-by-step instructions help you understand how to add the business terms in bulk:

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

&#x20;     The Meta Data Manager menu is displayed.

2. From the **Meta Data Manager** menu, click **Business Terms.**

<figure><img src="../../../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

The Business Terms page is displayed.

3. On the **Business Terms** page, click the **Bulk Upload** tab.

<figure><img src="../../../../.gitbook/assets/image (2283).png" alt=""><figcaption></figcaption></figure>

The **Bulk Upload** tab is open.

4. On the **Bulk Upload** tab, click **Business Terms.XLSX** to download the Business Terms template.

<figure><img src="../../../../.gitbook/assets/image (2284).png" alt=""><figcaption></figcaption></figure>

The **Business Terms** template is downloaded.

5. In the **Business Terms** template, enter all the required business terms.&#x20;

> <mark style="color:red;">**Note:**</mark> When you click a cell under a heading in the template, a drop-down list containing predefined options is displayed. Select the appropriate option from the list.

See the below example image:

<figure><img src="../../../../.gitbook/assets/image (2198).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> You can enter as many business terms as required; there is no limit on the number of terms that can be added

5. After completing the template, go back to the **Bulk Upload** tab, and then  click the **click to Browse** link to upload the template.

The template is uploaded.&#x20;

6. Review the  template and verify the data before submission.

<figure><img src="../../../../.gitbook/assets/image (2199).png" alt=""><figcaption></figcaption></figure>

6. Finally, click the **Submit** button.

The business terms are uploaded in bulk and automatically added to the Business Terms list.  See the Business Terms Table.

<figure><img src="../../../../.gitbook/assets/image (2200).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Adding Business Terms to a Glossary" %}
**Overview**

Adding **Business Terms** to a **Glossary** helps organize related business concepts into logical groups, making them easier to manage, discover, and understand. It provides users with a centralized and structured repository of standardized business terminology.

***

**Procedure**

The below step-by-step instructions help you understand how to **add** the business terms to a glossary:

1. Navigate to **Business Terms** page (SCIKIQ Control>>Meta Data Manager>>Business Terms).

The **Business Terms** page is displayed.

2. On the **Business Terms** page, from the **Business Terms Table**, select the required **business terms**, and then click the **Add Glossary** button.

<figure><img src="../../../../.gitbook/assets/image (2202).png" alt=""><figcaption></figcaption></figure>

The **Glossary** drop-down list is displayed.

2. From the **Glossary** drop-down list, select the required **glossary**, and then click the **Ok** button.

<figure><img src="../../../../.gitbook/assets/image (2203).png" alt=""><figcaption></figcaption></figure>

The business terms are added to the selected glossary and the **Success** message is displayed. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2204).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Exporting Business Terms" %}
**Overview**

The **Export Business Terms** feature enables you to download business term information in CSV format for offline review, reporting, sharing, backup, or further analysis. Exporting business terms provides a convenient way to maintain records, collaborate with stakeholders, and reuse metadata outside the Metadata Manager.

***

**Procedure**

The below step-by-step instructions help you understand how to **export** the business terms in CSV format:

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Business Terms).

The **Business Terms** page is displayed.

2. On the **Business Terms** page, click the **Export to CSV** button. See the below image.

The **Business Terms** are downloaded in CSV format. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2205).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Viewing a Business Term Details" %}
**Overview**

Viewing a business term enables you to examine its complete details, including its definition, ownership, classification, governance information, and associated metadata.&#x20;

It also allows you to view its relationships with glossaries, physical schema mappings, and other linked data assets, providing a comprehensive understanding of the business concept.

**Procedure**

The below mentioned step-by-step instructions help you understand how to view a  business term details:

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Business Terms).

The **Business Terms** page is displayed.

2. On the **Business Terms** page, click the **View** icon corresponding to the required business term.

<figure><img src="../../../../.gitbook/assets/image (2317).png" alt=""><figcaption></figcaption></figure>

The Business Term details are displayed.

3. Scroll down to view see additional metadata and linked assets.

<figure><img src="../../../../.gitbook/assets/image (2318).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> The below information provides description for Lineage, Lineage Levels, and Legends in the above image:
>
> * **Lineage:** It represents the end-to-end flow and relationships of a business term or data asset across the data ecosystem. It shows where the data originates, how it is transformed, and where it is ultimately used.
> * **Lineage Levels:** It determines the amount of relationship information displayed in the lineage diagram. They control how many upstream and downstream connections are shown from the selected business term or data asset.
> * **Legend:** It is a key that explains the meaning of the symbols, icons, colors, and line styles used in the lineage diagram.
{% endtab %}

{% tab title="Updating a Business Term Details" %}
**Overview**

Updating a business term ensures that its definition and associated metadata remain accurate, relevant, and aligned with current business requirements. As business processes, regulations, or organizational structures evolve, business terms may need to be revised to reflect these changes.

**Procedure**

The below mentioned step-by-step instructions help you understand how to update a  business term:

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Business Terms).

The **Business Terms** page is displayed.

2. On the **Business Terms** page, click the **Edit** icon corresponding to the required **business term**.

<figure><img src="../../../../.gitbook/assets/image (2319).png" alt=""><figcaption></figcaption></figure>

The Business Term details become editable on the right pane.

3. In the **Business Details**, make the required modifications, and then click the **Add** button.

<figure><img src="../../../../.gitbook/assets/image (2320).png" alt=""><figcaption></figcaption></figure>

The business term details are displayed in the Business Terms Table.

4. Next, in the **Business Terms Table**, select the **business term**, and then click the **Submit** button.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2321).png" alt=""><figcaption></figcaption></figure>

The Business Terms dialogue box is displayed.

5. On the **Business Terms** dialogue box, click the **Ok** button.

<figure><img src="../../../../.gitbook/assets/image (2323).png" alt=""><figcaption></figcaption></figure>

The business term is updated as per the change made.
{% endtab %}

{% tab title="Sharing a Business Term" %}
**Overview**

Sharing a business term allows you to make its definition and associated metadata available to other users, teams, or stakeholders for collaboration, review, or reference. It ensures that everyone has access to consistent and approved business terminology across the organization.

**Procedure**

The below mentioned step-by-step instructions help you understand how to share a business term:

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Business Terms).

The **Business Terms** page is displayed.

2. On the **Business Terms** page, click the **Share** icon corresponding to the required **business term**.

<figure><img src="../../../../.gitbook/assets/image (2324).png" alt=""><figcaption></figcaption></figure>

The Resource Permission dialogue box is displayed.

3. On the **Resource Permission** dialogue box:

A. Select the required **permission type** choosing from **Public, Private,** or **Shared**. For example, Shared.

B. Click the **Add More** button.

The sharing fields are displayed under **Share With.**

&#x20;C. From the **Share With** fields, select the **Group** and **Role** (Viewer or Contributor) under .

> <mark style="color:red;">**Note:**</mark> Click the **Delete** ![](<../../../../.gitbook/assets/image (2326).png>) button if you want to delete the **Share With** fields row.

C. Click the **Save** button.

<figure><img src="../../../../.gitbook/assets/image (2325).png" alt=""><figcaption></figcaption></figure>

The business term is shared and the **Permission applied successfully** message is displayed.

<figure><img src="../../../../.gitbook/assets/image (2327).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Deleting a Business Term" %}
**Overview**

Deleting a business term removes obsolete, duplicate, or incorrectly created business terms from the Metadata Manager. This helps maintain an accurate, relevant, and well-organized business glossary..

**Procedure**

The below mentioned step-by-step instructions help you understand how to delete a business term:

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Business Terms).

The **Business Terms** page is displayed.

2. On the **Business Terms** page, click the **Delete** icon corresponding to the required **business term**.

<figure><img src="../../../../.gitbook/assets/image (2328).png" alt=""><figcaption></figcaption></figure>

The Delete message is displayed.

3. On the **Delete** message, click the **Yes** button.

<figure><img src="../../../../.gitbook/assets/image (2329).png" alt=""><figcaption></figcaption></figure>

The business term is deleted.
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Assets**](../assets/)
* [**Data Dictionary**](../data-dictionary/)
* [**Dataset Metadata**](../dataset-metadata/)
* [**Glossary**](../glossary/)
* [**Table Classification**](../table-classification.md)
