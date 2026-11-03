---
icon: page
---

# Business Data Element

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to manage business data elements. A Business Data Element (BDE) is a business-oriented representation of a specific data attribute that describes a business concept, such as Customer Name, Employee ID, Account Number, or Date of Birth. It provides a standardized business meaning for data elements used across systems and datasets.

***

### Managing Business Data Elements

As part of managing **Business Data Elements**, you can perform the following tasks:

* **Adding Business Data Elements Individually:** Create and define business data elements one at a time.
* **Adding Business Data Elements in Bulk:** Add multiple business data elements simultaneously using bulk upload.
* **Exporting Business Data Elements:** Export business data elements and their associated metadata for external use or reference.
* **Viewing Business Data Elements Details:** View the definition, description, and other metadata associated with a business data element.
* **Updating Business Data Elements:** Modify the details of an existing business data element.
* **Sharing Business Data Elements:** Share business data elements with other users or teams as required.
* **Deleting Business Data Elements:** Remove business data elements that are no longer required.

Click the below tabs to view step-by-step instructions for each of the above mentioned tasks.

{% tabs %}
{% tab title="Navigating to  Data Element Page" %}
**Overview**

This section describes how to navigate to the **Business Data Elements** page. Follow the below mentioned step-by-step instructions.

**Procedure**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

&#x20;     The Meta Data Manager menu is displayed.

2. From the **Meta Data Manager** menu, select **Business Data Element.**

<figure><img src="../../../.gitbook/assets/image (3073).png" alt=""><figcaption></figcaption></figure>

The **Business Data Elements** page is displayed.

<figure><img src="../../../.gitbook/assets/image (3074).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Adding Business Data Elements Individually" %}
**Overview**

This section describes how to add business data elements individually.  **Adding Business Data Elements** creates a common business vocabulary for technical data, making metadata easier to understand, discover, standardize, and govern.

_**Example:**_ _Suppose three systems store a customer's date of birth using different column names: DOB, BIRTH\_DT, ans CUST\_DOB. By defining a common Business Data Element called Date of Birth and mapping it to these columns, the organization can establish a consistent business meaning across all three systems._

**Procedure**

The procedure involves the following steps. Expand each panel to view the step-by-step instructions.

<details>

<summary><strong>Enter</strong> <strong>Business Data Element Details</strong></summary>

**Overview**

**Entering business data element details** defines the business data element’s name, description, and other relevant attributes to establish its business meaning and support consistent data identification and usage.

**Procedure**

The below step-by-step instructions describe the procedure:

_**To enter business data element details**_

1. Navigate to **Business Data Elements** page.&#x20;

(SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>>Business Data Element>>Business Data Elements Page)

2. On the **Business Data Elements** Page, click the **Add Business Data Elements** button on the top right corner of the page.

<figure><img src="../../../.gitbook/assets/image (3052).png" alt=""><figcaption></figcaption></figure>

The **Add Business Data Element** page displayed.&#x20;

2. On the **Add Business Data Element** page, enter **Business Data Element Name** details.

<figure><img src="../../../.gitbook/assets/image (3053).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> Refer to the following table for details about each field and its purpose.

3. If the DQ Rule is not found, then either **add DQ rules** for this Data Element or provide a rationale for obtaining a DQ dispensation.

**Business Data Element Field Description Table**

| Field                                | Purpose                                                                                                              |
| ------------------------------------ | -------------------------------------------------------------------------------------------------------------------- |
| Business Data Element Name           | Specifies a meaningful business name that identifies the data element.                                               |
| Business Data Element Description    | Describes the meaning, purpose, and business context of the data element.                                            |
| Status                               | Indicates the current lifecycle or approval status of the business data element.                                     |
| Scope                                | Defines the applicability or intended coverage of the business data element.                                         |
| Catalogue                            | Associates the business data element with a specific data catalogue for organized metadata management and discovery. |
| Ownership Type                       | Specifies the type of ownership assigned to the business data element, helping establish accountability.             |
| Criticality                          | Indicates the business importance of the data element to help prioritize governance and data quality efforts.        |
| Data Originating Platform            | Identifies the platform from which the data originates.                                                              |
| Data Store Information – Data Source | Identifies the source system or connection from which the data is obtained.                                          |
| Data Store Information – Data Table  | Specifies the source table containing the relevant data.                                                             |
| Data Store Information – Column      | Identifies the specific column in the source table associated with the business data element.                        |
| Data Layer Information – Data Set    | Specifies the dataset associated with the business data element.                                                     |
| Data Layer Information – Column      | Identifies the specific column in the selected dataset corresponding to the business data element.                   |

The data element is displayed in the **Business Data Element Table**, which is at the end of the page. See the below image.

<figure><img src="../../../.gitbook/assets/image (3054).png" alt=""><figcaption></figcaption></figure>



</details>

<details>

<summary><strong>Configure Approval Mapping</strong></summary>

**Overview**

**Configuring approval mapping** defines the approval workflow to ensure that business data element details are reviewed and authorized by the appropriate users before approval, promoting consistency and data governance.

**Procedure**

Configuring approval mapping involves assigning the **Recommender**, **Concur**, and **Approver** roles to define the review and approval workflow for the Business Data Element. Once the required roles are assigned, you need to submit the Business Data Element for review and approval.

Follow the step-by-step instructions below to configure the approval mapping and submit the business data element.

_**To configure approval mapping**_

1. On the **Business Data Elements** page, scroll down to the **Approval Rule Mapping** section.
2. From the **User** drop-down boxes, select the **Recommender, Concurre,** and **Approver**.
3. In the **Business Data Element** table, select the **business data element**.
4. Finally, Click the **Submitted Selected** button.

<figure><img src="../../../.gitbook/assets/image (3055).png" alt=""><figcaption></figcaption></figure>

The business data element is added.

<figure><img src="../../../.gitbook/assets/image (3056).png" alt=""><figcaption></figcaption></figure>

</details>
{% endtab %}

{% tab title="Adding Business Data Elements in Bulk" %}
**Overview**

This section describes how to add Business Data Elements in bulk. **Bulk uploading** enables you to create multiple Business Data Elements simultaneously by importing them from a file. This approach reduces manual effort and saves time when onboarding large numbers of data elements into Metadata Manager.

***

**Procedure**

The process of bulk uploading business terms involves downloading the template file, populating it with the required business data element details, and uploading the completed file.

The below step-by-step instructions help you understand how to add the business data elements in bulk:

_**To upload business data elements in bulk**_

{% stepper %}
{% step %}
**Download the template file**&#x20;

1. Navigate to **Business Data Elements** page.&#x20;

(SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>>Business Data Element>>Business Data Elements Page)

2. On the **Business Data Elements** Page, click the **Add Business Data Elements** button on the top right corner of the page.

The **Business Data Element** page is displayed.

3. On the **Business Data Element** page, click the **Bulk Upload** tab.

<figure><img src="../../../.gitbook/assets/image (3057).png" alt=""><figcaption></figcaption></figure>

The **Bulk Upload Business Data Elements** screen is displayed.

4. On the **Bulk Upload Business Data Elements** screen, click the  **Download Template File** button.

<figure><img src="../../../.gitbook/assets/image (3058).png" alt=""><figcaption></figcaption></figure>

The **Business Data Element** te**mplate is downloaded.**
{% endstep %}

{% step %}
**Populate business data element details in the template**

* In the **Business Data Element** template, enter all the required details.&#x20;

> <mark style="color:red;">**Note:**</mark> When you click a cell under a heading in the template, a drop-down list containing predefined options is displayed. Select the appropriate option from the list.

See the below example image:

<figure><img src="../../../.gitbook/assets/image (3059).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> You can enter as many business data elements as required; there is no limit on the number of terms that can be added.
{% endstep %}

{% step %}
**Upload the template**

1. After completing the template, go back to the **Bulk Upload** tab, and then click the **click to Browse** link to upload the template.

The template is uploaded.&#x20;

2. Review the  template and verify the data before submission.
3. Finally, click the **Submit** button.

The business data elements are uploaded in bulk and automatically added to the Business Data Element list.&#x20;
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Exporting Business Data Elements" %}
**Overview**

This section describes how to export Business Data Elements in CSV format. The **Export** feature enables you to download Business Data Element information for offline review, reporting, sharing, backup, or further analysis.

Exporting Business Data Elements provides a convenient way to maintain records, collaborate with stakeholders, and reuse metadata outside Metadata Manager.

***

**Procedure**

The below step-by-step instructions help you understand how to export business data elements:

_**To export business data**_ _**elements**_

{% stepper %}
{% step %}
**Select the business data elements**

1. Navigate to **Business Data Elements** page.&#x20;

(SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>>Business Data Element>>Business Data Elements Page)

2. On the **Business Data Elements** Page, select the required business data elements.

> <mark style="color:red;">**Note:**</mark> Based on the requirement, you can select all the business data elements by selecting the **multi-select** checkbox.

<figure><img src="../../../.gitbook/assets/image (3018).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Click the Export button**

* After selecting the business data elements, click the **Export** button on the top of the page.

<figure><img src="../../../.gitbook/assets/image (3019).png" alt=""><figcaption></figcaption></figure>

The business data elements are displayed in CSV format.

<figure><img src="../../../.gitbook/assets/image (3020).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Sending Business Data Elements for Approval" %}
**Overview**

This section describes how to send the selected columns to the authorised user for approval.The purpose of approval is to ensure that important changes to business or technical metadata are **reviewed and validated by an authorized user before they become official or published metadata**.

Once sent for the approval, the status of that column will be displayed as Submitted. Upon approval by the authorised user, it will be shown as Approved.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * Once a column is submitted for approval, its status changes to **Submitted**. After an authorized user approves the submission, the status changes to **Approved**.&#x20;
> * Only columns in **Draft** status can be submitted for approval. Columns that have already been **submitted** cannot be submitted again.

**Procedure**

The process of submitting business elements for approval involves the following two steps: Select Business Data Elements and Configure Approval Mapping.

Follow the instructions below to submit the selected columns for approval.

_**To send business elements for approval**_

{% stepper %}
{% step %}
**Select the business data elements**

1. Navigate to **Business Data Elements** page.&#x20;

(SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>>Business Data Element>>Business Data Elements Page)

2. On the **Business Data Elements** Page, select the required business data elements.

> <mark style="color:red;">**Note:**</mark> Based on the requirement, you can select all the business data elements by selecting the **multi-select** checkbox.

<figure><img src="../../../.gitbook/assets/image (3018).png" alt=""><figcaption></figcaption></figure>

The **Request Approval** button is displayed.

3. After selecting the business data elements, click the **Request Approval** button.

<figure><img src="../../../.gitbook/assets/image (3021).png" alt=""><figcaption></figcaption></figure>

The **Send Selected Business Data Element(s) for Approval** dialogue box is displayed.
{% endstep %}

{% step %}
**Configure approval mapping**

On the **Send Selected Business Data Element(s) for Approval** dialogue box, select the **Recommender, Concur,** and **Approver**, and then click the **Send for Approval** button.

<figure><img src="../../../.gitbook/assets/image (3022).png" alt=""><figcaption></figcaption></figure>

The selected business data elements are sent for approval.

<figure><img src="../../../.gitbook/assets/image (3023).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Viewing a Business Element Details " %}
**Overview**

This section describes how to view the details of business data element.  **Viewing business data element** details helps to verify the configured information, review the associated metadata, and ensure that the business data element is correctly defined and aligned with business requirements.

**Procedure**

The below step-by-step instructions help you understand how to view the data element details:

_**To view the data element details**_

1. Navigate to **Business Data Elements** page.&#x20;

(SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>>Business Data Element>>Business Data Elements Page)

2. On the **Business Data Elements** Page, click the **View Record** icon corresponding to the required business element.

<figure><img src="../../../.gitbook/assets/image (3026).png" alt=""><figcaption></figcaption></figure>

The **View Business Data Element** screen is displayed. See the below image.

<figure><img src="../../../.gitbook/assets/image (3027).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Updating a Business Data Element" %}
**Overview**

This section describes how to update the details of a business data element. As part of updating, you can modify its **basic information, data store information, data layer details,** and **approval mapping rules** as required.

**Procedure**

The below step-by-step instructions help you understand how to update the business data element:

_**To update the details of business data element**_

1. Navigate to **Business Data Elements** page.&#x20;

(SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>>Business Data Element>>Business Data Elements Page)

2. On the **Business Data Elements** Page, click the **Edit Record** icon corresponding to the required business element.

> <mark style="color:red;">**Note:**</mark> You can update only the the business data elements that are in **Draft** status.

<figure><img src="../../../.gitbook/assets/image (3029).png" alt=""><figcaption></figcaption></figure>

The **Edit Business Data Element** screen is displayed.

3. On the **Edit Business Data Element** screen, make the required changes, and then click the **Update** button.

<figure><img src="../../../.gitbook/assets/image (3030).png" alt=""><figcaption></figcaption></figure>

The business data element is updated.
{% endtab %}

{% tab title="Deleting a Business Data Element" %}
**Overview**

This section describes how to delete the details of a business data element.&#x20;

**Procedure**

The below step-by-step instructions help you understand how to delete a business data element:

_**To delete the details of a business data element**_

1. Navigate to **Business Data Elements** page.&#x20;

(SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>>Business Data Element>>Business Data Elements Page)

2. On the **Business Data Elements** Page, click the **Delete Record** icon corresponding to the required business element.

> <mark style="color:red;">**Note:**</mark> You can delete only the the business data elements that are in **Draft** status.

<figure><img src="../../../.gitbook/assets/image (3031).png" alt=""><figcaption></figcaption></figure>

The **Delete** message is displayed.

3. On the **Delete** message, click the **Yes** button.

<figure><img src="../../../.gitbook/assets/image (3032).png" alt=""><figcaption></figcaption></figure>

The business data element is deleted.
{% endtab %}
{% endtabs %}

### Related Topics

* [**Assets**](../../integrations/meta-data-manager/assets/)
* [**Data Dictionary**](../../integrations/meta-data-manager/data-dictionary/)
* [**Dataset Metadata**](../../integrations/meta-data-manager/dataset-metadata/)
* [**Glossary**](../../integrations/meta-data-manager/glossary/)
* [**Table Classification**](../../integrations/meta-data-manager/table-classification.md)
