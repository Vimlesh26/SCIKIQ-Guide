---
icon: page
---

# Creating a CSV/Excel Connection Connection

***

**Contents**

* [**Instructions for Using this Page**](creating-a-csv-excel-connection-connection.md#instructions-for-using-this-page)
* [**Overview**](creating-a-csv-excel-connection-connection.md#overview)
* [**Procedure**](creating-a-csv-excel-connection-connection.md#procedure)
* [**Related Topics**](creating-a-csv-excel-connection-connection.md#related-topics)

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]
* At any time during the workflow, you can return to the previous section by clicking the **Previous** <img src="../../../../.gitbook/assets/image (204).png" alt="" data-size="original">button.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

This page explains how to create a **CSV/Excel** data source connection in SCIKIQ. The process involves a series of steps, which includes navigating to the CSV/Excel connection page, selecting a new or an existing data source, configuring the connection details, adding metadata, previewing, and submitting the connection.

Once the connection is successfully established, the data source will appear on the **Connected Data Sources** page.&#x20;

***

## Procedure

The expandable panels below guide you through the process of creating a **CSV/Excel** connection in SCIKIQ. Follow each step in sequence while configuring the connection. The system enables the next step only after the current step is completed.

<details>

<summary>1.<strong>Navigate to CSV/Excel Page</strong></summary>

A. On the **Left Navigation Bar**, expand **Connect to Data Source** under **SCIKIQ CONNECT**, and then click **Manage** **Data Source**.

<figure><img src="../../../../.gitbook/assets/Click Manage Data Source.png" alt=""><figcaption><p>Manage Data Source Menu Item</p></figcaption></figure>

The All Data Sources page is displayed.

B. On the **All Data Sources** page, click **Files** in the **left menu**, and then click either **CSV** or **XLSX** in the right pane.

<figure><img src="../../../../.gitbook/assets/S (186).png" alt="" width="563"><figcaption><p>Navigating to CSV/XLSX</p></figcaption></figure>

The CSV/Excel page is displayed.&#x20;

</details>

<details>

<summary>2.<strong>Create Connection</strong></summary>

* On the **CSV/Excel** page, in the **Create Connection** section, select either a **new data source** or an **existing data source** depending on the requirement, and then click the **Next** button. See the below example image.&#x20;

<figure><img src="../../../../.gitbook/assets/S (187).png" alt="" width="563"><figcaption><p>Selecting Data Source</p></figcaption></figure>

The Connection Details section is highlighted.

</details>

<details>

<summary>3.<strong>Configure Connection Details</strong></summary>

**Purpose**

The **purpose of configuring connection details** when connecting an **Excel or CSV file** to an application is to ensure the file is **identified correctly, read accurately, and processed securely**.

**Procedure**

The below instructions help you understand how to configure connection details:

{% hint style="success" %}
**Tip:** The field names and their corresponding options in the below instructions are annotated with relevant descriptions. To view the description of a field or an option, simply hover your cursor over it. &#x20;
{% endhint %}

A. In the **Connection Details** section:

**To connect Excel:**

* From the **Select Type** options, choose **Excel**.
* Click the **Browse** button to upload the **file**.
* In the **Name** field, enter a **name** for the **file.**
* From the[ <mark style="color:blue;">**Dataset**</mark>](#user-content-fn-2)[^2] option, select either [<mark style="color:blue;">**With Dataset**</mark>](#user-content-fn-3)[^3] or [<mark style="color:blue;">**Without Dataset**</mark>](#user-content-fn-4)[^4].
* Select the [<mark style="color:blue;">**File contains header as first row**</mark>](#user-content-fn-5)[^5] option based on the requirement.
* In the **Description box**, enter the **required description**.
* Click the **Next** button.

<figure><img src="../../../../.gitbook/assets/S (188).png" alt=""><figcaption><p>Configuring Connection Details for Excel</p></figcaption></figure>

**To connect CSV:**

* From the **Select Type** options, choose **CSV**.
* Click the **Browse** button to upload the **file**.
* In the **Name** field, enter a **name** for the **file.**
* From the [<mark style="color:blue;">**Dataset**</mark> ](#user-content-fn-6)[^6]option, select either [<mark style="color:blue;">**With Dataset**</mark>](#user-content-fn-7)[^7] or [<mark style="color:blue;">**Without Dataset**</mark>](#user-content-fn-4)[^4].
* Select the [<mark style="color:blue;">**File contains header as first row**</mark>](#user-content-fn-8)[^8] option based on the requirement.
* In the **Description box**, enter the **required description**.
* Click the **Next** button.

<figure><img src="../../../../.gitbook/assets/S (189).png" alt=""><figcaption><p>Configuring Connection Details for CSV</p></figcaption></figure>

The Add Metadata section is activated.

</details>

<details>

<summary>4.<strong>Add Metadata</strong></summary>

**Purpose**

While connecting the application to a database, adding **metadata** provides the application with important information about the data it will interact with. This metadata helps the system understand, organize, and manage the data correctly.

**Procedure:**

As part of the procedure, you need to specify catalogue, connectivity mechanism, store, source system, connection type, supporting email ID, and service type. Once done, you need to test by clicking the Test Connection button to check whether everything is correct.

**Step-by-Step Instructions:**

The below step-by-step instructions help you understand how to add meta data.

* In the **Add Meta Data** section:

{% hint style="success" %}
**Tip:** The field names and their corresponding options in the below instructions are annotated with relevant descriptions. To view the description of a field or an option, simply hover your cursor over it.&#x20;
{% endhint %}

* Specify [<mark style="color:blue;">**Catalogue,**</mark>](#user-content-fn-9)[^9] [<mark style="color:blue;">**Business Owner**</mark>](#user-content-fn-10)[^10]**,** and [<mark style="color:blue;">**Technical Owner**</mark>](#user-content-fn-11)[^11]**.**
* From the [<mark style="color:blue;">**Connectivity Mechanism**</mark>](#user-content-fn-12)[^12] options, select [<mark style="color:blue;">**Secured**</mark>](#user-content-fn-13)[^13]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Unsecured**</mark>](#user-content-fn-14)[^14], or [<mark style="color:blue;">**SSH Tunnelling**</mark>](#user-content-fn-15)[^15]**.**
* From the [<mark style="color:blue;">**Store**</mark>](#user-content-fn-16)[^16] options, select either [<mark style="color:blue;">**Is Feature Store**</mark>](#user-content-fn-17)[^17] or [<mark style="color:blue;">**Is Analytical Store**</mark>](#user-content-fn-18)[^18].
* From the [<mark style="color:blue;">**Source System**</mark>](#user-content-fn-19)[^19] drop-down box, select [<mark style="color:blue;">**Internal**</mark>](#user-content-fn-20)[^20] or [<mark style="color:blue;">**Third Party**</mark>](#user-content-fn-21)[^21].
* From the [<mark style="color:blue;">**Connection Type**</mark>](#user-content-fn-22)[^22] drop-down box, select [<mark style="color:blue;">**Access Layer**</mark>](#user-content-fn-23)[^23]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Source System**</mark>](#user-content-fn-24)[^24]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Reference System,**</mark>](#user-content-fn-25)[^25] or [<mark style="color:blue;">**Master Database**</mark>](#user-content-fn-26)[^26]<mark style="color:blue;">**.**</mark>
* In the **Supporting Email ID** field, specify the **supporting email ID** to contact when something goes wrong or when help is needed.
* From the **Service Type** drop-down box, select the **category of service** the data source provides.
* Specify [<mark style="color:blue;">**Service Id**</mark>](#user-content-fn-27)[^27] and [<mark style="color:blue;">**Application Id**</mark>](#user-content-fn-28)[^28]**.**
* Finally, click the **Test Connection** button to check everything is correct.

The **Connection tested successfully** message is displayed.

* Click the **Next** button.

<figure><img src="../../../../.gitbook/assets/S (190).png" alt=""><figcaption><p>Adding Meta Data</p></figcaption></figure>

The Preview section is activated.

</details>

<details>

<summary>5.<strong>Preview</strong></summary>

* In the **Preview** section, click the **Finish** button to submit it.

<figure><img src="../../../../.gitbook/assets/S (191).png" alt=""><figcaption></figcaption></figure>

The connection is created and the [Connected Data Sources](/broken/pages/dgiZ3ktrQlmTnR2Pq3nV) page is displayed.

</details>

***

## Related Topics

* [**Managing Connected Data Sources**](../../managing-connected-data-sources.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.

[^2]: The **purpose** of selecting a **dataset** while creating a connection is to **define the specific data to be accessed and managed** through that connection.

[^3]: <mark style="color:blue;">This option automatically creates the dataset for the uploaded file.</mark>

[^4]: Choosing this option does not create a dataset in SCIKIQ.

[^5]: <mark style="color:blue;">The</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**File contains header as first row**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">option indicates whether the</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**first row of a file includes column names**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">rather than actual data.</mark>

[^6]: The **purpose of selecting a dataset** while creating a connection is to define the specific data to be accessed and managed through that connection.

[^7]: This option automatically creates the dataset for the uploaded file.

[^8]: The **File contains header as first row** option indicates whether the first row of a file includes column names rather than actual data.

[^9]: **Catalogue** refers to the group of related data sources.

[^10]: **Business Owner** refers to the person or team responsible for the data from a business point of view.

[^11]: **Technical Owner** refers to the **person or IT team** responsible for the technical side of the data.

[^12]: Connectivity Mechanism refers to the method used to connect to the data source.

[^13]: **Secured** option refers to the connection where data is encrypted, making it safe from hackers and unauthorized access.

[^14]: **Unsecured** option refers to the connection where data is sent without encryption.

[^15]: SSH Tunneling: SSH refers to Secure Shell. SSH is a secure way to connect to another computer or server over a network.

[^16]: This refers to how the data will be used.

[^17]: Select **Is Feature Store** if the data source is used to store and manage machine learning features.

[^18]: Select **Is Analytical Store** if the data source is primarily used for analytics, reporting, and business intelligence.

[^19]: This refers to the original system where the data comes from.

[^20]: An **Internal source system** is owned, managed, and maintained by your organization.

[^21]: A **Third-Party** source system is owned and managed by an external vendor or service provider.

[^22]: This refers to the kind of connection you are using to access the source.

[^23]: The **Access Layer** represents systems that are used to consume or expose data rather than originate it.

[^24]: A **Source System** is the origin of raw or transactional data.

[^25]: A Reference System stores standardized, lookup, or supporting data used across multiple systems.

[^26]: A **Master Database** stores authoritative master data for key business entities.

[^27]: This refers to the unique identifier for the service you are connecting to.

[^28]: This refers to the unique ID used to identify the application that owns, provides, or uses the data.
