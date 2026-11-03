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

This page describes how to manage business terms. **Business Terms** enable organizations to define and maintain a standardized business vocabulary within the Metadata Manager. They provide clear definitions for key business concepts, helping users understand the meaning and context of data assets.&#x20;

By linking business terms to datasets, data elements, and other metadata objects, organizations can improve data governance, enhance data discovery, and ensure consistent interpretation of information across the enterprise.

***

### Managing Business Terms

As part of managing **Business Terms**, you can perform the following tasks:

* **Add Business Terms Individually:** Create and define business terms one at a time.
* **Add Business Terms in Bulk:** Add multiple business terms simultaneously using bulk upload.
* **Add Business Terms to Glossary:** Associate business terms with the appropriate glossary for organized management.
* **Export Business Terms:** Export business terms and their associated metadata for external use or reference.
* **View Business Term Details:** View the definition, description, and other metadata associated with a business term.
* **Update Business Terms:** Modify the details of an existing business term.
* **Share Business Terms:** Share business terms with other users or teams as required.
* **Delete Business Terms:** Remove business terms that are no longer required.

Click the below tabs to view step-by-step instructions for each of the above mentioned tasks.

{% tabs %}
{% tab title="Navigating to  Business Terms Page" %}
**Overview**

This section describes how to navigate to the **Business Terms** page. The following steps describe the procedure.

**Procedure**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

&#x20;     The Meta Data Manager menu is displayed.

2. From the **Meta Data Manager** menu, select **Business Terms.**

<figure><img src="../../../../.gitbook/assets/image (2946).png" alt=""><figcaption></figcaption></figure>

The **Business Terms** page is displayed.
{% endtab %}

{% tab title="Filtering Business Terms" %}
**Overview**

This page describes how to filter business terms on the Business Terms page. **Filtering Business Terms** helps users narrow down the list based on specific criteria, making it easier to locate and manage relevant business terms, especially when the list contains a large number of entries.

**Procedure**

The below step-by-step instructions help you understand how to filter business terms on the Business Terms page:

_**To filter business terms**_

1. Navigate to **Business Terms** page.
2. On the **Business Terms** page, click the **Filter** button.

<figure><img src="../../../../.gitbook/assets/image (2950).png" alt=""><figcaption></figcaption></figure>

The **Filter Business Terms** section is displayed on the left side of the Business Terms page.

3. In the **Filter Business Terms** section, select the **Business Process, Process Owner, Catalogue, Glossary, Category, Status, Approval Status, Sensitive, Classification, Reg Rule,** or **Industry Standard** from the respective drop-down boxes.&#x20;

> <mark style="color:red;">**Note:**</mark> Refer to the below table for the above Filter fields description.

**Filter fields Description**

| **Filter**            | **Description**                                                                                          |
| --------------------- | -------------------------------------------------------------------------------------------------------- |
| **Business Process**  | Filters business terms associated with a specific business process.                                      |
| **Process Owner**     | Filters business terms based on the person responsible for the associated business process.              |
| **Catalogue**         | Filters business terms associated with a specific data catalogue.                                        |
| **Glossary**          | Filters business terms associated with a specific glossary.                                              |
| **Category**          | Filters business terms based on their assigned category.                                                 |
| **Status**            | Filters business terms based on their current lifecycle status, such as Draft, Recommended, or Approved. |
| **Approval Status**   | Filters business terms based on their approval status in the approval workflow.                          |
| **Sensitive**         | Filters business terms based on whether they are marked as sensitive.                                    |
| **Classification**    | Filters business terms based on their assigned data classification.                                      |
| **Reg Rule**          | Filters business terms based on the applicable regulatory rule.                                          |
| **Industry Standard** | Filters business terms based on the associated industry standard.                                        |

4. Click the **Search** button.

<figure><img src="../../../../.gitbook/assets/image (2951).png" alt=""><figcaption></figcaption></figure>

The required business term is displayed.<br>
{% endtab %}

{% tab title="Adding Business Terms Individually" %}
**Overview**

This section describes how to add business terms individually. Adding business terms **individually** allows you to create and maintain business definitions one term at a time. This approach is useful when introducing new business concepts, updating the business glossary incrementally, or when only a small number of terms need to be added.

***

**Procedure**

Adding a business term involves a series of steps, including **navigating to the Business Terms page**, specifying **Business Term Details**, and configuring **Physical Schema Mapping** and **Approval Rule Mapping**.

After the business term is created, it appears on the **Business Terms** page with **Draft** status. Once an authorized recommender recommends the term, it is routed to the designated approver, and its status changes to **Recommended**. Upon approval by the authorized approver, the status changes to **Approved**.&#x20;

Expand the below panels to view step-by-step instructions:

<details>

<summary><strong>Navigate to Business Terms Page</strong></summary>

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

&#x20;     The Meta Data Manager menu is displayed.

2. From the **Meta Data Manager** menu, click **Business Terms.**

<figure><img src="../../../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

The Business Terms page is displayed.

</details>

<details>

<summary><strong>Enter Business Term Details</strong> </summary>

**Overview**

As part of entering **Business Term Details**, you need to provide information across several sections, including **Term Information**, **Term Ownership**, **Classification and Governance**, and **Extended Attributes**.&#x20;

These details help define the business term, identify its ownership and stewardship, establish governance controls, and capture any additional metadata required by the organization.

**Procedure**

The below step-by-step instructions help you understand how to add a business term details:

_**To add a business term details**_

1. On the **Business Terms** page, click the **Add Business Term** button on the top right corner.

<figure><img src="../../../../.gitbook/assets/image (3012).png" alt=""><figcaption></figcaption></figure>

The **Add Business Term** dialogue box is displayed.

2. In the **Add Business Term** dialogue box, specify **Business** **Term  Information (Name, Definition, Purpose),** **Business  Ownership**, **Classification and Governance**, and **Extended Attributes**.&#x20;

> <mark style="color:red;">**Note:**</mark> Refer to the below **Field Description** table for  the description of the above mentioned **Add Business Term** dialogue box fields.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2279).png" alt=""><figcaption></figcaption></figure>



**Field Description**

<table><thead><tr><th width="144.55560302734375" valign="top">Field</th><th valign="top">Description</th><th width="168.06939697265625" valign="top">Example Input</th></tr></thead><tbody><tr><td valign="top"><strong>Term Name</strong></td><td valign="top">In this field, specify the <strong>name</strong> of the business term.</td><td valign="top">Patient Record, Customer, Revenue</td></tr><tr><td valign="top"><strong>Definition</strong></td><td valign="top">In this field, provide a clear and standardized <strong>description of the business term</strong> and its meaning within the organization.</td><td valign="top">Revenue is the total income generated from the sale of products or services before expenses are deducted.</td></tr><tr><td valign="top"><strong>Purpose</strong></td><td valign="top">In this field, provide the <strong>business objective or reason</strong> for maintaining the term.</td><td valign="top">To standardize the definition of revenue across reports and business units.</td></tr><tr><td valign="top"><strong>Business Process</strong></td><td valign="top">From this drop-down box, select the business process or functional area to which the term belongs.</td><td valign="top">Business Process</td></tr><tr><td valign="top"><strong>Owner</strong></td><td valign="top">From this drop-down box, select the <strong>individual or team</strong> responsible for maintaining and approving the business term.</td><td valign="top">Finance Team, Data Governance Team, John Smith</td></tr><tr><td valign="top"><strong>Catalogue</strong></td><td valign="top">From this drop-down box, select the <strong>metadata catalogue</strong> in which the business term is stored and managed</td><td valign="top">Enterprise Data Catalogue</td></tr><tr><td valign="top"><strong>Glossary</strong></td><td valign="top">From this drop-down box, select the <strong>glossary</strong> that groups related business terms.glossary that groups related business terms.</td><td valign="top">Healthcare Glossary, Customer Management Glossary</td></tr><tr><td valign="top"><strong>Category</strong></td><td valign="top">From this drop-down box, select the <strong>business term</strong> <strong>into a</strong> <strong>logical business category</strong> for easier organization and discovery.</td><td valign="top">Financial Metrics, Customer Information, Healthcare Data</td></tr><tr><td valign="top"><strong>Status</strong></td><td valign="top">From this drop-down box, select the <strong>current lifecycle state</strong> of the business term.</td><td valign="top">Draft</td></tr><tr><td valign="top"><strong>Sensitive</strong></td><td valign="top">From this drop-down box, select the <strong>term</strong> associated with sensitive or regulated data.</td><td valign="top">GDPR, PII</td></tr><tr><td valign="top"><strong>Classification</strong></td><td valign="top">From this drop-down box, select the  <strong>acronyms, or abbreviations</strong> commonly used for the business term.</td><td valign="top">Internal, Confidential, Restricted, Public</td></tr><tr><td valign="top"><strong>Regulatory Rule</strong></td><td valign="top">From this drop-down box, select the <strong>regulatory rule</strong> applicable to the business term</td><td valign="top">GDPR</td></tr><tr><td valign="top"><strong>Industry Standard</strong></td><td valign="top">From this drop-down box, select the industry standards or frameworks associated with the business term.</td><td valign="top">HIPAA, GDPR</td></tr></tbody></table>

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



</details>

<details>

<summary><strong>Configure Approval Rule Mapping</strong> </summary>

**Overview**

After  entering the business term details, you need to configure approval rule mapping. **Configuring Approval Rule Mapping** while adding a business term helps establish who needs to review and approve the business term before it becomes part of the governed metadata.

**Procedure**

The below step-by-step instructions help you understand how to configure approval mapping while adding a business term:

_**To configure approval mapping**_

1. On the **Business Terms** page, scroll down to **Approval Mapping** section.
2. In the **Approval Mapping** section, select the **Recommender** and the **Approver.**&#x20;

<figure><img src="../../../../.gitbook/assets/image (2947).png" alt=""><figcaption></figcaption></figure>

3. T**o add the business term to the Business Term Table**

* If you want to add the business term to the Business Term Table, click the **Add** button.

The business term is added to the table. See the below example image.

<figure><img src="../../../../.gitbook/assets/image (2948).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * **To make any changes** to a business term in the table, first select it, then click the **Edit** icon corresponding to it and make the changes.
> * **To delete a business term** from the table, first select it, then click the **Delete** icon corresponding to it and make the changes.

4. Finally, click the **Submit** **Selected** button.

The selected business term is  added and reflected in the Business Terms page. See the below example image.

<figure><img src="../../../../.gitbook/assets/image (2949).png" alt=""><figcaption></figcaption></figure>

</details>
{% endtab %}

{% tab title="Adding Business Terms in Bulk" %}
**Overview**

This section describes how to add business terms in bulk. Adding business terms **in bulk** enables you to create multiple business terms simultaneously by importing them from a file. This approach saves time and effort when onboarding large numbers of terms into the Metadata Manager.

***

**Procedure**

The process of bulk uploading business terms involves downloading the template file, populating it with the required business term details, and uploading the completed file.

The below step-by-step instructions help you understand how to add the business terms in bulk:

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

&#x20;     The Meta Data Manager menu is displayed.

2. From the **Meta Data Manager** menu, click **Business Terms.**

<figure><img src="../../../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

The Business Terms page is displayed.

3. On the **Business Terms** page, click the **Bulk Upload** tab.

<figure><img src="../../../../.gitbook/assets/image (2952).png" alt=""><figcaption></figcaption></figure>

The **Bulk Upload Business Terms** screen is displayed.

4. On the **Bulk Upload Business Terms** screen, click **Business Terms.XLSX** to download the Business Terms template.

<figure><img src="../../../../.gitbook/assets/image (2284).png" alt=""><figcaption></figcaption></figure>

The **Business Terms** template is downloaded.

5. In the **Business Terms** template, enter all the required business terms.&#x20;

> <mark style="color:red;">**Note:**</mark> When you click a cell under a heading in the template, a drop-down list containing predefined options is displayed. Select the appropriate option from the list.

See the below example image:

<figure><img src="../../../../.gitbook/assets/image (2198).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> You can enter as many business terms as required; there is no limit on the number of terms that can be added.

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

This section describes how to add business terms to a glossary. Adding **Business Terms** to a **Glossary** helps organize related business concepts into logical groups, making them easier to manage, discover, and understand. It provides users with a centralized and structured repository of standardized business terminology.

***

**Procedure**

Adding business terms to a glossary involves selecting the required terms and associating them with the appropriate glossary. Once completed, the selected business terms are added to the glossary.

The below step-by-step instructions help you understand how to **add** the business terms to a glossary:

1. Navigate to **Business Terms** page (SCIKIQ Control>>Meta Data Manager>>Business Terms).

The **Business Terms** page is displayed.

2. On the **Business Terms** page, from the **Business Terms Table:**

A. Select the required **business terms.**

The **Add Glossary** button appears.

B. Click the **Add Glossary** button.

<figure><img src="../../../../.gitbook/assets/image (2954).png" alt=""><figcaption></figcaption></figure>

The **Glossary** drop-down list is displayed.

2. From the **Glossary** drop-down list, select the required **glossary**, and then click the **Ok** button.

<figure><img src="../../../../.gitbook/assets/image (2203).png" alt=""><figcaption></figcaption></figure>

The business terms are added to the selected glossary and the **Success** message is displayed. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2955).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Exporting Business Terms" %}
**Overview**

This section describes how to download business terms in CSV format. The **Export Business Terms** feature enables you to download business term information in CSV format for offline review, reporting, sharing, backup, or further analysis.&#x20;

Exporting business terms provides a convenient way to maintain records, collaborate with stakeholders, and reuse metadata outside the Metadata Manager.

***

**Procedure**

The below step-by-step instructions help you understand how to **export** the business terms in CSV format:

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Business Terms).

The **Business Terms** page is displayed.

2. On the **Business Terms** page, click the **Export to CSV** button. See the below image.

The **Business Terms** are downloaded in CSV format. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2205).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Viewing Business Term Details" %}
**Overview**

This section describes how to view a business term details. **Viewing a business term** details helps users understand the term's definition, business context, and associated metadata, enabling them to interpret and use the term consistently across the organization.

It also allows you to view its relationships with glossaries and physical schema mappings.

**Procedure**

The below mentioned step-by-step instructions help you understand how to view a  business term details:

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Business Terms).

The **Business Terms** page is displayed.

2. On the **Business Terms** page, click the **View** icon corresponding to the required business term.

<figure><img src="../../../../.gitbook/assets/image (2957).png" alt=""><figcaption></figcaption></figure>

The **Details** screen is displayed. See the below example image.

<figure><img src="../../../../.gitbook/assets/image (2958).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Viewing Business Term Details and Audit History" %}
**Overview**

This section describes how to view a business term details and its audit history. **Viewing Business Term Details** helps to view **business term name, type, creator name, created date, and update date**. You can also view the view see additional metadata and linked assets.

The **audit history** provides traceability by showing changes made to the term, helping users track updates and support accountability in metadata management.

**Procedure**

The below mentioned step-by-step instructions help you understand how to view a business term details and also its audit history:

<details>

<summary>Viewing Business Term Details</summary>

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Business Terms).

The **Business Terms** page is displayed.

2. On the **Business Terms** page, click the **View** icon corresponding to the required business term.

<figure><img src="../../../../.gitbook/assets/image (2959).png" alt=""><figcaption></figcaption></figure>

The **Details** screen is displayed.&#x20;

3. Scroll down to view see additional metadata and linked assets.

<figure><img src="../../../../.gitbook/assets/image (2318).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> The below information provides description for Lineage, Lineage Levels, and Legends in the above image:
>
> * **Lineage:** It represents the end-to-end flow and relationships of a business term or data asset across the data ecosystem. It shows where the data originates, how it is transformed, and where it is ultimately used.
> * **Lineage Levels:** It determines the amount of relationship information displayed in the lineage diagram. They control how many upstream and downstream connections are shown from the selected business term or data asset.
> * **Legend:** It is a key that explains the meaning of the symbols, icons, colors, and line styles used in the lineage diagram.

</details>

<details>

<summary>Viewing Audit History</summary>

1. On the **Business Term Details** page, click the **Audit History** tab.

The **Audit History** tab is open.

2. On the **Audit History** tab, either specify the required Data Range or Select a Predefined Date Range Filters choosing from Last 7 Days, Last 30 Days, Last 3 Months, or Last 6 Months.
3. From the **Users** drop-down box, select the **required user.**
4. From the **Actions** drop-down box, select the required action choosing from **Updated, Deleted, Restored**, or **Restored Version.**

<figure><img src="../../../../.gitbook/assets/image (2961).png" alt=""><figcaption></figcaption></figure>

The audit history is displayed.

</details>
{% endtab %}

{% tab title="Updating a Business Term Details" %}
**Overview**

This section how to describes how to update a business term. **Updating a business term** ensures that its definition and associated metadata remain accurate, relevant, and aligned with current business requirements.&#x20;

**Procedure**

When updating a business term, you can change its basic information and approval rules as required.

The below mentioned step-by-step instructions help you understand how to update a  business term:

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Business Terms).

The **Business Terms** page is displayed.

2. On the **Business Terms** page, click the **Edit** icon corresponding to the required **business term**.

<figure><img src="../../../../.gitbook/assets/image (2962).png" alt=""><figcaption></figcaption></figure>

The **Edit Business Term** dialogue box is displayed.

3. On the **Edit Business Term** dialogue box:

**A. Making changes to approval rules**

* If you want to make any changes to approval rules, scroll down to the **Approval Rules** section, and make the required changes.
* Click the **Update** button.

<figure><img src="../../../../.gitbook/assets/image (2968).png" alt=""><figcaption></figcaption></figure>

The business term is displayed in the **Business Term** table.

**B. Making changes to business term**

* In the **Business Term** table, select the business term, and then click the **Edit** icon corresponding to it.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2971).png" alt=""><figcaption></figcaption></figure>

The **Business Term Information** section is displayed.

* In the **Business Term Information** section, make the required changes to the business term, and then click the **Submit Selected** button.

The **Business Terms** notification screen is displayed.

* On the **Business Terms** notification screen, click the **Ok** button.

<figure><img src="../../../../.gitbook/assets/image (2972).png" alt=""><figcaption></figcaption></figure>

The business term is updated as per the change made.
{% endtab %}

{% tab title="Sharing a Business Term" %}
**Overview**

This section describes how to share a business term. When sharing a business term, you can make it accessible to either all users who have access to the relevant SCIKIQ environment or restrict access to specific users or groups.

**Procedure**

The below mentioned step-by-step instructions help you understand how to share a business term:

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Business Terms).

The **Business Terms** page is displayed.

2. On the **Business Terms** page, click the **Share** icon corresponding to the required **business term**.

<figure><img src="../../../../.gitbook/assets/image (2964).png" alt=""><figcaption></figcaption></figure>

The **Resource Permission** dialogue box is displayed with the **Private** option displayed by default.

3. On the **Resource Permission** dialogue box:&#x20;

A. **If you want to make the business term accessible to all users** permitted to access the relevant SCIKIQ environment, subject to the platform's access controls, then select the **Public** option,&#x20;

B. **If you want to share it to specific users or groups**, then select the **Shared** option, and click the **Add More** button.

The sharing fields are displaye&#x64;**.**

C. From the sharing fields, select the required **Group.**

D.  From the **Role** drop-down box, select **Viewer** or **Contributor**.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> 1. **Viewers** can view the term and its details, while **Contributors** can view and modify the term, subject to the permissions configured in SCIKIQ.
> 2. If you to delete the sharing fields, click the **Delete** ![](<../../../../.gitbook/assets/image (2326).png>) button.

D. Click the **Save** button.

<figure><img src="../../../../.gitbook/assets/image (2325).png" alt=""><figcaption></figcaption></figure>

The business term is shared and the **Permission applied successfully** message is displayed.

<figure><img src="../../../../.gitbook/assets/image (2965).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Deleting a Business Term" %}
**Overview**

This section describes how to delete a business term. **Deleting a Business Term** removes obsolete, duplicate, or incorrectly created business terms from the Metadata Manager. This helps maintain an accurate, relevant, and well-organized business glossary.

**Procedure**

The below mentioned step-by-step instructions help you understand how to delete a business term:

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Business Terms).

The **Business Terms** page is displayed.

2. On the **Business Terms** page, click the **Delete** icon corresponding to the required **business term**.

<figure><img src="../../../../.gitbook/assets/image (2966).png" alt=""><figcaption></figcaption></figure>

The Delete message is displayed.

3. On the **Delete** message, click the **Yes** button.

<figure><img src="../../../../.gitbook/assets/image (2967).png" alt=""><figcaption></figcaption></figure>

The business term is deleted.
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Assets**](../../../integrations/meta-data-manager/assets/)
* [**Data Dictionary**](../../../integrations/meta-data-manager/data-dictionary/)
* [**Dataset Metadata**](../../../integrations/meta-data-manager/dataset-metadata/)
* [**Glossary**](../../../integrations/meta-data-manager/glossary/)
* [**Table Classification**](../../../integrations/meta-data-manager/table-classification.md)
