---
icon: page
---

# Table Relationships

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to manage table relationship in SCIKIQ. **Table relationships** define the connections between two or more tables based on common or related columns. They enable a data management system to associate records across tables and interpret how different sets of data are related.

For example, a `Customers` table and a `Sales` table can be connected through the `Customer_ID` column. This relationship allows users to associate each sales transaction with the corresponding customer.

***

### Managing Table Relationships

As part of managing the table relationships, you can view its details, update , delete, or submit it for approval.

Click the tabs below for step-by-step instructions on each task.

{% tabs %}
{% tab title="Viewing  Table Metadata Details " %}
**Overview**

This section describes how to view table relationships. **Viewing Table Relationships** helps to understand how tables are connected within the Power BI data model. It provides visibility into the relationships between tables and the columns used to establish these connections.&#x20;

This information helps to understand data dependencies, examine relationship configurations, and analyze how tables interact when generating reports and performing data analysis.

**Procedure**

The below instructions help you understand how to view a table relationship details.

_**To view the table relationship**_ _**details**_

{% stepper %}
{% step %}
**Navigate to Dashboard**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

The Meta Data Manager menu is displayed.

2. On the **Meta Data Manager** menu, click **PowerBI Parser**, and then select **Table Relationships.**

<figure><img src="../../../.gitbook/assets/image (3100).png" alt=""><figcaption></figcaption></figure>

The **Table Relationships** is displayed.
{% endstep %}

{% step %}
**View Metadata**

* On the **Table Relationships** page, click the **View Details** icon corresponding to the required table relationships.

<figure><img src="../../../.gitbook/assets/image (3101).png" alt=""><figcaption></figcaption></figure>

The **Table Relationship Details** screen is displayed. See the below example image.

<figure><img src="../../../.gitbook/assets/image (3102).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Sending Table Relationship for Approval" %}
**Overview**

This section describe how to send table relationship for approve. **Sending table relationship for approval** enables to send the defined relationships between tables in the Power BI data model to the designated approver for review.&#x20;

This process helps validate the relationships and ensures that they comply with the organization's data governance standards before approval.

**Procedure**

The below instructions help you understand how to send the table relationship for approval.

_**To send a table relationship for approval**_

{% stepper %}
{% step %}
**Navigate to Table Relationships**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

The Meta Data Manager menu is displayed.

2. On the **Meta Data Manager** menu, click **PowerBI Parser**, and then select **Table Relationships.**
{% endstep %}

{% step %}
**Send for Approval**

1. On the **Dashboard** page, click the **Send for Approval** icon corresponding to the required table relationship.

<figure><img src="../../../.gitbook/assets/image (3103).png" alt=""><figcaption></figcaption></figure>

The **Send Selected Table Relationship(s) for Approval** screen is displayed.

2. On the **Send Selected Table Relationship(s) for Approval** screen, select the **Approver** from the **User** drop-down box, and then click the **Send for Approval** button.

<figure><img src="../../../.gitbook/assets/image (3104).png" alt=""><figcaption></figcaption></figure>

The table relationship is submitted for approval and the status is displayed as **Pending**.

<figure><img src="../../../.gitbook/assets/image (3105).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Deleting Metadata" %}
**Overview**

This section describes how to delete a table relationship from SCIKIQ. **Deleting a table relationship** allows users to remove relationships that are no longer required or are incorrectly configured.&#x20;

This helps maintain the accuracy of the Power BI data model and ensures that only relevant relationships are retained for data analysis and reporting.

**Procedure**

The below instructions help you understand how to delete a table relationship.

_**To delete a table relationship**_

> <mark style="color:red;">**Note:**</mark> You can delete a table relationship only when its status is **Draft** . Metadata in **Submitted**, **Approval Pending** or **Approved** status cannot be deleted.

{% stepper %}
{% step %}
**Navigate to Table Relationship**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

The Meta Data Manager menu is displayed.

2. On the **Meta Data Manager** menu, click **PowerBI Parser**, and then select **Table Relationship.**
{% endstep %}

{% step %}
**Delete Table Relationship**

1. On the **Table Relationship** page, click the **Delete** button corresponding to the required table relationship.

<figure><img src="../../../.gitbook/assets/image (3107).png" alt=""><figcaption></figcaption></figure>

The **Relationship** **Bulk Actions** message box is displayed.

2. On the  **Relationship** **Bulk Actions** message box, click the **Yes** button.

<figure><img src="../../../.gitbook/assets/image (3108).png" alt=""><figcaption></figcaption></figure>

The table relationship is deleted.
{% endstep %}
{% endstepper %}
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Meta Data Manager**](../../integrations/meta-data-manager/)
