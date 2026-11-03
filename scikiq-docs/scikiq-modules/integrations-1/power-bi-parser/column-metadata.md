---
icon: page
---

# Column Metadata

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to manage column metadata in SCIKIQ. **Column metadata** is information that describes the properties, meaning, and characteristics of a column in a database table or dataset. It helps to understand what a column represents, the type of data it contains, and how it can be used in data processing, analysis, and reporting.

***

### Managing Column Metadata

As part of managing the column metadata, you can view its details, update , submit it for approval or delete it.

Click the tabs below for step-by-step instructions on each task.

{% tabs %}
{% tab title="Viewing  Column Metadata Details " %}
**Overview**

This section describes how view a column metadata details. **Viewing column metadata** allows to review the properties and attributes of individual columns, including their names, data types, descriptions, and other configured metadata.&#x20;

This helps to understand the purpose of each column, identify relevant data fields, and support data analysis and governance activities.

**Procedure**

The below instructions help you understand how to view a column metadata details.

_**To view a column metadata details**_

{% stepper %}
{% step %}
**Navigate to Column Metadata**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

The Meta Data Manager menu is displayed.

2. On the **Meta Data Manager** menu, click **PowerBI Parser**, and then select **Column Metadata.**

<figure><img src="../../../.gitbook/assets/image (3109).png" alt=""><figcaption></figcaption></figure>

The **Column Metadata** is displayed.
{% endstep %}

{% step %}
**View Column Metadata**

* On the **Column Metadata** page, click the **View Details** icon corresponding to the required column.

<figure><img src="../../../.gitbook/assets/image (3114).png" alt=""><figcaption></figcaption></figure>

The **Column Metadata Details - KPI** screen is displayed. See the below example image.

<figure><img src="../../../.gitbook/assets/image (3111).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Updating Column Metadata" %}
**Overview**

This section describe how to update a column metadata. **Updating column medatata** helps to correct  inaccurate or incomplete information, update details to reflect business requirements, and ensure that the extracted metadata is accurate and consistent before submitting it for approval.

**Procedure**

The below instructions help you understand how to update the column metadata.

_**To update the column metadata**_&#x20;

> <mark style="color:red;">**Note:**</mark> You can edit the column metadata only when its status is **Draft** or **Submitted**. Column metadata in **Approval Pending** or **Approved** status cannot be edited.

{% stepper %}
{% step %}
**Navigate to Column Metadata**

* SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>> PowerBI Parser>>Column Metadata.

The **Column Metadata** page is dispalyed.
{% endstep %}

{% step %}
**Edit Column Metadata**

1. On the **Column Metadata** page, click the **Edit** icon corresponding to the required column.

<figure><img src="../../../.gitbook/assets/image (3117).png" alt=""><figcaption></figcaption></figure>

The **Edit Column** dialogue box is displayed.

2. On the **Edit Column** dialogue box, make the required changes to  the **description and Act Column Name,** and then click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (3118).png" alt=""><figcaption></figcaption></figure>

The column metadata is updated.
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Submitting Column Metadata for Approval" %}
**Overview**

This section describe how to send column data for approval. **Sending column metadata** for approval allows users to submit column details and associated metadata to the designated approver for review.&#x20;

This helps validate the accuracy and consistency of column information and ensures alignment with organizational data governance standards before approval.

**Procedure**

The below instructions help you understand how to send the column metadata for approval.

_**To send the column metadata for approval**_

{% stepper %}
{% step %}
**Navigate to C**_**olumn Metadata**_

* SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>> PowerBI Parser>>Column Metadata.

The **Column Metadata** page is dispalyed.
{% endstep %}

{% step %}
**Send for Approval**

1. On the **Column Metadata** page, click the **Send for Approval** icon corresponding to the required column.

<figure><img src="../../../.gitbook/assets/image (3119).png" alt=""><figcaption></figcaption></figure>

The **Send Selected Column(s) for Approval** screen is displayed.

2. On the  **Send Selected Column(s) for Approval** screen, select the **Approver** from the **User** drop-down box, and then click the **Send for Approval** button.

<figure><img src="../../../.gitbook/assets/image (3120).png" alt=""><figcaption></figcaption></figure>

The column is submitted for approval and the status is displayed as **Pending**.

<figure><img src="../../../.gitbook/assets/image (3121).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Deleting Metadata" %}
**Overview**

This section describes how to delete column metadata from SCIKIQ. **Deleting column metadata** allows to remove metadata entries that are no longer required or relevant. This helps maintain an accurate and organized metadata repository by eliminating obsolete or unnecessary column information

**Procedure**

The below instructions help you understand how to delete a column metadata.

_**To delete a column metadata**_

> <mark style="color:red;">**Note:**</mark> You can delete a column metadata only when its status is **Draft** . A column in **Submitted**, **Approval Pending** or **Approved** status cannot be deleted.

{% stepper %}
{% step %}
**Navigate to Column Metadata**

* SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>> PowerBI Parser>>Column Metadata.

The **Column Metadata** page is dispalyed.
{% endstep %}

{% step %}
**Delete Column Metadata**

1. On the **Column Metadata** page, click the **Delete** button corresponding to the required column.

<figure><img src="../../../.gitbook/assets/image (3124).png" alt=""><figcaption></figcaption></figure>

The **Bulk Actions** message box is displayed.

2. On the  **Relationship** **Bulk Actions** message box, click the **Yes** button.

<figure><img src="../../../.gitbook/assets/image (3123).png" alt=""><figcaption></figcaption></figure>

The column is deleted.
{% endstep %}
{% endstepper %}
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Meta Data Manager**](../../integrations/meta-data-manager/)
