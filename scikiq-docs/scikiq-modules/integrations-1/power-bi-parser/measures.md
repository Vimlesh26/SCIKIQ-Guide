---
icon: page
---

# Measures

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to manage measures in SCIKIQ. **Measure metadata** provides information about the calculations used to derive values from underlying data. It captures details such as measure names, descriptions, calculation formulas, and associated data elements, depending on the configured metadata attributes.&#x20;

This information helps to understand calculation logic, maintain consistent metric definitions, and support data discovery, traceability, and governance.

### Managing Measures

As part of managing a measure, you can view it details, update, or delete it.

Click the tabs below for step-by-step instructions on each task.

{% tabs %}
{% tab title="Viewing  a Measure Details" %}
**Overview**

This section describes how to view the details of a measure. **Viewing measure details** allows to review the information associated with a measure, including its definition, calculation formula, and other configured metadata.&#x20;

This helps users understand how the measure is calculated, verify its accuracy, and assess its relevance to data analysis and reporting requirements.

**Procedure**

The below instructions help you understand how to view a measure details.

_**To view a measure details**_

{% stepper %}
{% step %}
**Navigate to Measures**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

The Meta Data Manager menu is displayed.

2. On the **Meta Data Manager** menu, click **PowerBI Parser**, and then select **Measures.**

<figure><img src="../../../.gitbook/assets/image (3125).png" alt=""><figcaption></figcaption></figure>

The **Measure List** page is displayed.
{% endstep %}

{% step %}
**View a Measure Details**

* On the **Measure List** page, click the **View Details** icon corresponding to the required measure.

<figure><img src="../../../.gitbook/assets/image (3126).png" alt=""><figcaption></figcaption></figure>

The **Measure Details - RUN AT** screen is displayed. See the below example image.

<figure><img src="../../../.gitbook/assets/image (3127).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Updating a Measure" %}
**Overview**

This section describe how to update a measure. **Updating a measure** allows to modify its details, calculation formula, and associated metadata, as applicable. This helps keep measure definitions accurate and aligned with changing business requirements, supporting consistent data analysis and reporting.&#x20;

**Procedure**

The below instructions help you understand how to update a measure.

_**To update a measure**_&#x20;

> <mark style="color:red;">**Note:**</mark> You can edit a measure only when its status is **Draft** or **Submitted**. A measure in **Approval Pending** or **Approved** status cannot be edited.

{% stepper %}
{% step %}
**Navigate to Measures**

* SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>> PowerBI Parser>>Measures.

The **Measure List** page is displayed.
{% endstep %}

{% step %}
**Edit Measure**

1. On the **Measure List** page, click the **Edit** icon corresponding to the required measure.

<figure><img src="../../../.gitbook/assets/image (3128).png" alt=""><figcaption></figcaption></figure>

The **Edit Measure** dialogue box is displayed.

2. On the **Edit Measure** dialogue box, make the required changes to  the **description,** and then click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (3129).png" alt=""><figcaption></figcaption></figure>

The measure is updated.
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Deleting a Measure" %}
**Overview**

This section describes how to delete measure from SCIKIQ. **Deleting a measure** allows to remove measures that are no longer required or relevant to business requirements. This helps maintain an organized and up-to-date measure repository by eliminating obsolete or unnecessary measure definitions.

**Procedure**

The below instructions help you understand how to delete a measure.

_**To delete a measure**_

> <mark style="color:red;">**Note:**</mark> You can delete a measure only when its status is **Draft** . A column in **Submitted**, **Approval Pending** or **Approved** status cannot be deleted.

{% stepper %}
{% step %}
**Navigate to Measure**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

The Meta Data Manager menu is displayed.

2. On the **Meta Data Manager** menu, click **PowerBI Parser**, and then select **Measure.**
{% endstep %}

{% step %}
**Delete a Measure**

1. On the **Measure** page, click the **Delete** button corresponding to the required column.

<figure><img src="../../../.gitbook/assets/image (3130).png" alt=""><figcaption></figcaption></figure>

The **Delete Measure** message box is displayed.

2. On the **Delete Measure** message box, click the **Yes** button.

<figure><img src="../../../.gitbook/assets/image (3132).png" alt=""><figcaption></figcaption></figure>

The measure is deleted.
{% endstep %}
{% endstepper %}
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Meta Data Manager**](../../integrations/meta-data-manager/)
