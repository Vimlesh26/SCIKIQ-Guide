---
icon: page
---

# Table Metadata

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to manage table metadata in SCIKIQ. The **Table Metadata** page provides a centralized view of all available tables and their associated metadata, including the table name, semantic model, Fully Qualified Name (FQN), Act table name, data source, and approval status.

This information would be helpful to identify tables, understand their association with semantic models and data sources, and track their approval status. This helps maintain visibility into table metadata and supports effective data catalog management.

***

### Managing Table Metadata

As part of managing a table relationship, you can view its details, update , delete, or submit it for approval.

Click the tabs below for step-by-step instructions on each task.

{% tabs %}
{% tab title="Viewing  Table Metadata Details " %}
**Overview**

This section describe how to view the table metadata details. **Viewing table metadata** details enables to understand the table's structure, purpose, and properties. This helps to identify relevant tables, verify the available information, and determine their suitability for business and reporting requirements.

**Procedure**

The below instructions help you understand how to view the table metadata details.

_**To view the table metadata**_ _**details**_

{% stepper %}
{% step %}
**Navigate to Table Metadata**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

The Meta Data Manager menu is displayed.

2. On the **Meta Data Manager** menu, click **PowerBI Parser**, and then select **Table Metadata.**

The **Table Metadata** page is displayed.
{% endstep %}

{% step %}
**View Table Metadata**

* On the **Table Metadata** page, click the **View Details** icon corresponding to the required table.

<figure><img src="../../../.gitbook/assets/image (3190).png" alt=""><figcaption></figcaption></figure>

The **Table Metadata Details** screen is displayed. See the below example image.

<figure><img src="../../../.gitbook/assets/image (3191).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Updating Metadata" %}
**Overview**

This section describe how to update the table metadata. **Updating table metadata** helps to correct inaccurate or incomplete information, update details to reflect business requirements, and ensure that the extracted metadata is accurate and consistent before submitting it for approval.

**Procedure**

The below instructions help you understand how to update the metadata of a table.

_**To update the table metadata**_&#x20;

> <mark style="color:red;">**Note:**</mark> You can edit metadata only when its status is **Draft** or **Submitted**. Table metadata in **Approval Pending** or **Approved** status cannot be edited.

{% stepper %}
{% step %}
**Navigate to Table Metadata**

* SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>> PowerBI Parser>>Dashboard.

The **Table Metadata** page is displayed.
{% endstep %}

{% step %}
**Update Table Metadata**

1. On the **Table Metadata** page, click the **Edit** icon corresponding to the required table.

<figure><img src="../../../.gitbook/assets/image (3189).png" alt=""><figcaption></figcaption></figure>

The **Edit Table** dialogue box is displayed.

2. On the **Edit Table** dialogue box, make the required changes to **description and Act Table,** and then click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (3112).png" alt=""><figcaption></figcaption></figure>

The table metadata is updated and the success message is displayed. See the below image.

<figure><img src="../../../.gitbook/assets/image (3113).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Sending Metadata for Approval" %}
**Overview**

This section describe how to send metadata for approval. **Submitting metadata for approval** enables designated approvers to review and validate the extracted metadata before it is approved for use.&#x20;

This helps ensure that the metadata meets business requirements and organisational standards.any required modifications before submitting it for approval.

**Procedure**

The below instructions help you understand how to send the metadata for approval.

_**To submit the table metadata for approval**_

{% stepper %}
{% step %}
**Navigate to Dashboard**

* SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>> PowerBI Parser>>Dashboard.

The **Table Metadata** page is displayed.
{% endstep %}

{% step %}
**Send for Approval**

1. On the **Table Metadata** page, click the **Send for Approval** icon corresponding to the required report.

<figure><img src="../../../.gitbook/assets/image (3186).png" alt=""><figcaption></figcaption></figure>

The **Send Selected Table(s) for Approval** screen is displayed.

2. On the **Send Selected Table(s) for Approval** screen, select the **Approver** from the **User** drop-down box, and then click the **Send for Approval** button.

<figure><img src="../../../.gitbook/assets/image (3098).png" alt=""><figcaption></figcaption></figure>

The table metadata is submitted for approval and the status is displayed as **Pending**.

<figure><img src="../../../.gitbook/assets/image (3099).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Deleting Metadata" %}
**Overview**

This section describes how to delete metadata from SCIKIQ. **Deleting table metadata** enables you to remove information that is incorrect, duplicated, obsolete, or no longer required.&#x20;

This helps maintain an organised metadata repository and prevents the use of outdated or irrelevant information.

**Procedure**

The below instructions help you understand how to delete the metadata.

_**To delete the table metadata**_

> <mark style="color:red;">**Note:**</mark> You can delete table metadata only when its status is **Draft** . Metadata in **Submitted**, **Approval Pending** or **Approved** status cannot be deleted.

{% stepper %}
{% step %}
**Navigate to Table Metadata**

* SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>> PowerBI Parser>>Dashboard.

The **Table Metadata** page is displayed.
{% endstep %}

{% step %}
**Delete Table Metadata**

1. On the  page, click the **Delete** button corresponding to the required table metadata.

<figure><img src="../../../.gitbook/assets/image (3187).png" alt=""><figcaption></figcaption></figure>

The **Bulk Actions** message box is displayed.

2. On the **Bulk Actions** message box, click the **Yes** button.

<figure><img src="../../../.gitbook/assets/image (3188).png" alt=""><figcaption></figcaption></figure>

The metadata is deleted.
{% endstep %}
{% endstepper %}
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Meta Data Manager**](../../integrations/meta-data-manager/)
