---
icon: page
---

# Creating and Using Data Quality Rules

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

**The creation of a Data Quality (DQ) rule involves a series of steps.** The process begins with selecting either a **Dataset** or a **Table**. The required **record limit**, **column**, **operator**, **value**, **rule name**, and **Data Quality (DQ) dimension** are then specified on the **Data Quality Rules** page. After the details are entered, the **Test** button is used to validate the rule. Once the validation is successful, the DQ rule is created and displayed in the left pane of the **Data Quality Rules** page.

***

### Procedure

{% tabs %}
{% tab title="Important Steps " %}
<table data-header-hidden><thead><tr><th width="194.33331298828125"></th><th></th></tr></thead><tbody><tr><td><strong>Step</strong></td><td><strong>Description</strong></td></tr><tr><td><strong>Define Goals</strong></td><td>Identify the data quality objectives, such as ensuring data accuracy, completeness, consistency, and validity.</td></tr><tr><td><strong>Set Quality Criteria</strong></td><td>Define the data quality rules, including valid values, thresholds, acceptable formats, and business-specific validation criteria.</td></tr><tr><td><strong>Implement Rules</strong></td><td>Configure and apply the data quality rules to the relevant datasets and integrate them into your data processing workflows.</td></tr><tr><td><strong>Monitor Compliance</strong></td><td>Regularly evaluate data against the defined rules to identify anomalies, errors, or quality issues.</td></tr><tr><td><strong>Refine Rules</strong></td><td>Review and update the rules as business requirements, data sources, or quality standards evolve to ensure continued effectiveness.</td></tr></tbody></table>
{% endtab %}

{% tab title="Procedure" %}
1. On the **Left Navigation Bar**, under **SCIKIQ CONTROL**, expand **Data Quality Manager**, and then click **Data Quality Rules**.

<figure><img src="../../../.gitbook/assets/image (2543).png" alt=""><figcaption></figcaption></figure>

The **Data Quality Rules** page is displayed.

2. On the **Data Quality Rules** page, in the **New Rule** pane:

A. Select either **Dataset** or **Table** depending on the requirement. For example, Dataset.

B. Specify the **Record (Rows) Limit** by choosing between 0 to 20,000.

C. From the **Dataset** drop-down box, select the required **dataset**.

D. From the **Select Column** drop-down box, select the required **column**.

E. From the **Operator** drop-down box, select the required **operator**. For example, Not Null.

F. In the **Rule Name** field, enter a **name for the rule**.

G. From the **DQ Dimensions** drop-down box, select the required **dimension** choosing from **Completeness, Consistency, Accuracy, Timeliness, Duplication, Conformity,** or **Coverage**.

> <mark style="color:red;">**Note:**</mark> Refer to the left pane for the description of these dimensions **Data Quality Rules** page.

H. Click the **Test** button.

The validation is performed and the rule appears on the left pane displaying the status. See the image below.

<figure><img src="../../../.gitbook/assets/image (2544).png" alt=""><figcaption></figcaption></figure>

I. To **apply** **Managing DQ Rules**, click the **Apply Rule** button.

The DQ rules are applied and the success message is displayed.

J. To **save the DQ rule,** click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (2545).png" alt=""><figcaption></figcaption></figure>

The **Save DQ** dialogue box is displayed.

K. On the **Save DQ** dialogue box, specify a **name** for the DQ rule, and then click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (2262).png" alt=""><figcaption></figcaption></figure>

The DQ Rule is saved and the **Success** message is displayed.
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Managing DQ Rules**](managing-dq-rules.md)
* [**Using Operational Dashboard**](using-operational-dq-dashboard.md)
* [**Using High Level Dashboard**](using-high-level-dq-dashboard.md)
