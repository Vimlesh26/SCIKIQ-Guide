---
icon: page
---

# Managing DQ Rules

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

Once a Data Quality (DQ) rule has been created, its details can be viewed as needed. The rule can be re-executed to validate the current data and update the validation results. If the rule is no longer required, it can be deleted from the DQ Rules page.

***

### Managing DQ Rules

{% tabs %}
{% tab title="View Rule Information " %}
**Overview**

The **Rule Information** feature displays the details of the selected Data Quality (DQ) rule, including the **Total Record Count, Valid Percentage, Invalid Percentage,** and **Threshold Limit**. The Threshold slider can be adjusted to preview how changes to the threshold value affect the rule validation results.

**Procedure**

The below step-by-step instructions help you understand how to view rule information:

_**To view rule information**_

1. On the **Data Quality Rules** page, click the **Rule Information** icon.

<figure><img src="../../../.gitbook/assets/image (2546).png" alt=""><figcaption></figcaption></figure>

The Rule Information screen is displayed.

2. On the **Rule Information** screen, **adjust the slider** to preview how changes to the threshold value affect the rule validation results.

<figure><img src="../../../.gitbook/assets/image (2548).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Re-execute Rule" %}
**Overview**

After a Data Quality (DQ) rule has been created, the **Test** **Rule** option can be used to re-execute the rule against the current dataset. This allows the rule to be revalidated whenever the underlying data changes and provides updated validation results, including the total record count, valid and invalid percentages, and threshold status.

**Procedure**

The below step-by-step instructions help you understand how to re-execute a DQ rule:

_**To**_ _**re-execute a DQ rule**_

* On the **Data Quality Rules** page, click the **Test** **Rule** icon.

<figure><img src="../../../.gitbook/assets/image (2552).png" alt=""><figcaption></figcaption></figure>

The DQ rule is re-executed.
{% endtab %}

{% tab title="Delete Rule" %}
**Overview**

The purpose of **deleting a Data Quality (DQ) rule** is to remove rules that are no longer required, are obsolete, or were created incorrectly. Deleting unnecessary rules helps keep the data quality framework organized and ensures that only relevant validations are applied to the data.

**Procedure**

The below step-by-step instructions help you understand how to delete a DQ rule:

_**To delete a DQ rule**_

1. On the **Data Quality Rules** page, click the **Delete Rule** icon.

<figure><img src="../../../.gitbook/assets/image (2549).png" alt=""><figcaption></figcaption></figure>

The **Notification** screen is displayed.

2. On the **Notification** screen, click the **Yes** button.

<figure><img src="../../../.gitbook/assets/image (2551).png" alt=""><figcaption></figcaption></figure>

The DQ rule is deleted.
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Creating and Using Data Quality Rules**](creating-and-using-data-quality-rules.md)
* [**Using Operational Dashboard**](using-operational-dq-dashboard.md)
* [**Using High Level Dashboard**](using-high-level-dq-dashboard.md)
