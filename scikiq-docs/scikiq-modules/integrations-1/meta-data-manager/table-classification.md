---
icon: page
---

# Table Classification

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

**Table Classification** is used to categorize database tables based on the nature, sensitivity, business importance, or regulatory requirements of the data they contain. It helps organizations understand and govern their data assets more effectively.

By classifying tables, organizations can:

* **Identify sensitive data** such as Personally Identifiable Information (PII), financial data, healthcare data, or confidential business information.
* **Support regulatory compliance** with standards such as GDPR, HIPAA, PCI-DSS, or organizational data governance policies.
* **Apply appropriate security controls** by determining which tables require encryption, masking, restricted access, or auditing.
* **Improve data discovery and understanding** by helping users quickly identify the purpose and criticality of a table.
* **Enable better data governance** through consistent categorization and management of enterprise data assets.

***

### Table Classification Methods

{% tabs %}
{% tab title="Auto Table Classification" %}
The Auto Table Classification can be configured by enabling the **Table Classification** checkbox in the **Discovery** step while connecting SCIKIQ to the datasource.

See the below image.

<figure><img src="../../../.gitbook/assets/image (2271).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Manual Classification" %}
**Overview**

The **Manual Classification** feature enables you to classify database tables by associating them with predefined or newly created classes. The process involves creating or selecting a classification class, choosing the relevant data source and class, reviewing the available tables, and assigning the appropriate classifications.&#x20;

Once the required classifications have been assigned, you can save the configuration to apply the classifications to the selected tables.

**Procedure**

The expandable panels below guide you through each step of the manual classification process.

<details>

<summary><strong>Create a Class</strong></summary>

1. On the **SCIKIQ Left Navigation Bar**, under **SCIKIQ Control,** expand **Meta Data Manager**, and then click **Table Classification.**

<figure><img src="../../../.gitbook/assets/image (2287).png" alt=""><figcaption></figcaption></figure>

The **Table Classification** page displayed.

2. On the **Table Classification** page, click **+ Add New Class.**&#x20;

<figure><img src="../../../.gitbook/assets/image (2288).png" alt=""><figcaption></figcaption></figure>

The Enter New Class Name dialogue box is displayed.

3. On **Enter New Class Name** dialogue box, enter **Class Name**, **Description**, and then click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (2289).png" alt=""><figcaption></figcaption></figure>

The table class is created. See the below image.

<figure><img src="../../../.gitbook/assets/image (2290).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Select Data Source and</strong> <strong>Class</strong></summary>

1. On the **Table Classification** page, from the **Data Source** drop-down box, select the required **data source**.
2. From the **Class** drop-down box, select the required **class.**

<figure><img src="../../../.gitbook/assets/image (2291).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Assign Tables and Save Classification</strong></summary>

1. On the **Table Classification** page, scroll down to the page.
2. From the **All Tables** box, select the **required tables**, and then click the **Forward Arrow** button to move them to the **Selected Tables** box.

<figure><img src="../../../.gitbook/assets/image (2276).png" alt=""><figcaption></figcaption></figure>

The tables are moved to the selected box. See the below image.

{% hint style="info" %}
**Tip:**

* **To move all the tables** to the **Available** box, click the **Move All** ![](<../../../.gitbook/assets/image (2272).png>) button.
* **To remove the selected tables from the Available box**, select the required tables, and then click the **Remove Selected** ![](<../../../.gitbook/assets/image (2275).png>)button.
* **To remove all the tables from the Available box**, click the **Remove All** ![](<../../../.gitbook/assets/image (2274).png>) button.
{% endhint %}

3. Now, click the **Save Classification** button.

<figure><img src="../../../.gitbook/assets/image (2293).png" alt=""><figcaption></figcaption></figure>

The **Save Classification** dialogue box is displayed.

4. On the **Save Classification** dialogue box, click the **Save** button.&#x20;

<figure><img src="../../../.gitbook/assets/image (2295).png" alt=""><figcaption></figcaption></figure>

The **Classification saved successfully** message is displayed.

<figure><img src="../../../.gitbook/assets/image (2296).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>View Class Tables</strong></summary>

* If you want to **view** the class tables, click the **View Class Tables** button.

<figure><img src="../../../.gitbook/assets/image (2269).png" alt=""><figcaption></figcaption></figure>

The View Class Tables screen is displayed.

<figure><img src="../../../.gitbook/assets/image (2270).png" alt=""><figcaption></figcaption></figure>

</details>
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Assets**](../../integrations/meta-data-manager/assets/)
* [**Data Dictionary**](../../integrations/meta-data-manager/data-dictionary/)
* [**Dataset Metadata**](../../integrations/meta-data-manager/dataset-metadata/)
* [**Glossary**](../../integrations/meta-data-manager/glossary/)
* [**Business Terms**](../../integrations/meta-data-manager/business-terms/)
