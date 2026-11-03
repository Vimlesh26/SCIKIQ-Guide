---
icon: page
---

# Creating an Azure Blob Connection

***

**Contents**

* [**Instructions for Using this Page**](creating-an-azure-blob-connection.md#instructions-for-using-this-page)
* [**Overview**](creating-an-azure-blob-connection.md#overview)
* [**Procedure**](creating-an-azure-blob-connection.md#procedure)
* [**Related Topics**](creating-an-azure-blob-connection.md#related-topics)

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]
* At any time during the workflow, you can return to the previous section by clicking the **Previous** <img src="../../../../.gitbook/assets/image (204).png" alt="" data-size="original">button.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

This page explains how to create an **Azure Blob** data source connection in SCIKIQ. The process involves a series of steps, which includes navigating to the Azure Blob connection page, selecting a new or existing data source, configuring the connection details, adding metadata, specifying owner, managed service, and connection type, reviewing the settings, and submitting the connection.

Once the connection is successfully established, the data source will appear on the **Connected Data Sources** page.&#x20;

***

## Procedure

The expandable panels below guide you through the process of creating an **Azure Blob** connection in SCIKIQ. Follow each step in sequence while configuring the connection. The system enables the next step only after the current step is completed.

<details>

<summary>1.<strong>Navigate to Azure Blob</strong></summary>

A. On the **Left Navigation Bar**, expand **Connect to Data Source** under **SCIKIQ CONNECT**, and then click **Manage** **Data Source**.

<figure><img src="../../../../.gitbook/assets/Click Manage Data Source.png" alt=""><figcaption><p>Manage Data Source Menu Item</p></figcaption></figure>

The All Data Sources page is displayed.

B. On the **All Data Sources** page, click **Files** in the **left menu**, and then click **Azure Blob** in the right pane.

<figure><img src="../../../../.gitbook/assets/S (170).png" alt=""><figcaption><p>Navigating to Azure Blob Data </p></figcaption></figure>

The Azure Blob page is displayed.&#x20;

</details>

<details>

<summary>2.<strong>Create Connection</strong></summary>

* On the **Azure Blob** page, in the **Create Connection** section, select either a **new data source** or an **existing data source** depending on the requirement, and then click the **Next** button. See the below example image.&#x20;

<figure><img src="../../../../.gitbook/assets/S (171).png" alt=""><figcaption><p>Selecting the Data Source</p></figcaption></figure>

The Connection Details section is highlighted.

</details>

<details>

<summary>3.<strong>Configure Connection Details</strong></summary>

**Purpose:**

When connecting a software application to a database, the system needs specific details to locate, identify, and authenticate the database. Each parameter plays a unique role.

**Procedure:**

The below instructions help you understand how to configure connection details:

{% hint style="success" %}
**Tip:** The field names in the below instructions are annotated with relevant descriptions. To view the description of a field or an option, simply hover your cursor over it.
{% endhint %}

In the **Connection Details** section:

* In the [<mark style="color:blue;">**Container Name**</mark>](#user-content-fn-2)[^2] field, enter the **container name**. For example, demo3\_blob.
* In the [<mark style="color:blue;">**Connection String**</mark>](#user-content-fn-3)[^3] box, enter the connection string.

{% hint style="info" %}
Tip: To create a connection string for your Azure storage account, click the **Down Arrow** as shown in the below image and follow the format mentioned.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (172).png" alt=""><figcaption><p>Configuring Connection Details</p></figcaption></figure>

* Click the **Next** button.

The Add Metadata section is activated.

</details>

<details>

<summary>4.<strong>Add Metadata</strong></summary>

**Purpose:**&#x20;

While connecting the application to a database, adding **metadata** provides the application with important information about the data it will interact with. This metadata helps the system understand, organize, and manage the data correctly.

**Procedure:**

As part of the procedure, you need to specify catalogue, connectivity mechanism, store, source system, connection type, supporting email ID, and service type. Once done, you need to test by clicking the Test Connection button to check whether everything is correct.

{% hint style="success" %}
**Tip:** To assist with your setup, fields and options shown in blue are equipped with tooltips. Hovering your mouse over these items will reveal a detailed description of their function.
{% endhint %}

**Step-by-Step Instructions:**

The below step-by-step instructions help you understand how to add meta data.

In the **Add Meta Data** section:

* Specify [<mark style="color:blue;">**Catalogue,**</mark>](#user-content-fn-4)[^4] [<mark style="color:blue;">**Business Owner**</mark>](#user-content-fn-5)[^5]**,** and [<mark style="color:blue;">**Technical Owner**</mark>](#user-content-fn-6)[^6]**.**
* From the [<mark style="color:blue;">**Connectivity Mechanism**</mark>](#user-content-fn-7)[^7] options, select [<mark style="color:blue;">**Secured**</mark>](#user-content-fn-8)[^8]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Unsecured**</mark>](#user-content-fn-9)[^9], or [<mark style="color:blue;">**SSH Tunnelling**</mark>](#user-content-fn-10)[^10]**.**
* From the [<mark style="color:blue;">**Store**</mark>](#user-content-fn-11)[^11] options, select either [<mark style="color:blue;">**Is Feature Store**</mark>](#user-content-fn-12)[^12] or [<mark style="color:blue;">**Is Analytical Store**</mark>](#user-content-fn-13)[^13].
* From the [<mark style="color:blue;">**Source System**</mark>](#user-content-fn-14)[^14] drop-down box, select [<mark style="color:blue;">**Internal**</mark>](#user-content-fn-15)[^15] or [<mark style="color:blue;">**Third Party**</mark>](#user-content-fn-16)[^16].
* From the [<mark style="color:blue;">**Connection Type**</mark>](#user-content-fn-17)[^17] drop-down box, select [<mark style="color:blue;">**Access Layer**</mark>](#user-content-fn-18)[^18]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Source System**</mark>](#user-content-fn-19)[^19]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Reference System,**</mark>](#user-content-fn-20)[^20] or [<mark style="color:blue;">**Master Database**</mark>](#user-content-fn-21)[^21]<mark style="color:blue;">**.**</mark>
* In the **Supporting Email ID** field, specify the **supporting email ID** to contact when something goes wrong or when help is needed.
* From the **Service Type** drop-down box, select the **category of service** the data source provides.
* Specify [<mark style="color:blue;">**Service Id**</mark>](#user-content-fn-22)[^22] and [<mark style="color:blue;">**Application Id**</mark>](#user-content-fn-23)[^23]**.**
* Finally, click the **Test Connection** button to check everything is correct.

<figure><img src="../../../../.gitbook/assets/S (173).png" alt=""><figcaption><p>Adding Meta Data</p></figcaption></figure>

The **Connection tested successfully** message is displayed.

* Click the **Next** button.

The Configuration section is activated.

</details>

<details>

<summary>5<strong>.Configuration</strong></summary>

* In the **Configuration** section, select the **owner** choosing from **Owner** or **Third Party**.
* Select the [<mark style="color:blue;">**Manage Service**</mark>](#user-content-fn-24)[^24] choosing from [<mark style="color:blue;">**Service Managed**</mark>](#user-content-fn-25)[^25] or[ <mark style="color:blue;">**User Managed**</mark>](#user-content-fn-26)[^26].
* Select the **Connection type** choosing from **Secured Connection** or **Unsecured Connection.**
* Specify the [<mark style="color:blue;">**DR**</mark>](#user-content-fn-27)[^27] **availability** and [<mark style="color:blue;">**RBAC**</mark>](#user-content-fn-28)[^28] **implementation** choosing from **Yes** or **No**.
* Click the **Next** button.

<figure><img src="../../../../.gitbook/assets/S (174).png" alt=""><figcaption><p>Configuring Additional Details</p></figcaption></figure>

The Review & Submit section is activated.

</details>

<details>

<summary>6.<strong>Review &#x26; Submit</strong></summary>

* In the **Review & Submit** section, enter a **name** and **description** for the connection, and then click the **Finish** button to submit it.

<figure><img src="../../../../.gitbook/assets/S (175).png" alt=""><figcaption><p>Specifying Connection Name and Description</p></figcaption></figure>

The connection is created and the [Connected Data Sources](/broken/pages/dgiZ3ktrQlmTnR2Pq3nV) page is displayed.

</details>

***

## Related Topics

* [**Managing Connected Data Sources**](../../managing-connected-data-sources.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.

[^2]: The **Container Name** specifies the logical storage unit within an Azure Storage account where blobs (files) are stored. It is similar to a folder in a file system and identifies the container to access or manage files.

[^3]: The **Connection String** contains the credentials and endpoint details required to authenticate and connect to the Azure Storage account.

[^4]: **Catalogue** refers to the group of related data sources.

[^5]: **Business Owner** refers to the person or team responsible for the data from a business point of view.

[^6]: **Technical Owner** refers to the **person or IT team** responsible for the technical side of the data.

[^7]: Connectivity Mechanism refers to the method used to connect to the data source.

[^8]: **Secured** option refers to the connection where data is encrypted, making it safe from hackers and unauthorized access.

[^9]: **Unsecured** option refers to the connection where data is sent without encryption.

[^10]: SSH Tunneling: SSH refers to Secure Shell. SSH is a secure way to connect to another computer or server over a network.

[^11]: This refers to how the data will be used.

[^12]: Select **Is Feature Store** if the data source is used to store and manage machine learning features.

[^13]: Select **Is Analytical Store** if the data source is primarily used for analytics, reporting, and business intelligence.

[^14]: This refers to the original system where the data comes from.

[^15]: An **Internal source system** is owned, managed, and maintained by your organization.

[^16]: A **Third-Party** source system is owned and managed by an external vendor or service provider.

[^17]: This refers to the kind of connection you are using to access the source.

[^18]: The **Access Layer** represents systems that are used to consume or expose data rather than originate it.

[^19]: A **Source System** is the origin of raw or transactional data.

[^20]: A Reference System stores standardized, lookup, or supporting data used across multiple systems.

[^21]: A **Master Database** stores authoritative master data for key business entities.

[^22]: This refers to the unique identifier for the service you are connecting to.

[^23]: This refers to the unique ID used to identify the application that owns, provides, or uses the data.

[^24]: <mark style="color:blue;">**Manage Service tells the system which service is responsible for this connection and how it will be used.**</mark>

[^25]: <mark style="color:blue;">**Service Managed**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">means the connection or resource is</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**automatically managed by the system or a platform service**</mark>

[^26]: **User Managed** means the connection or resource is **created, configured, and maintained by the user** rather than by the system.

[^27]: <mark style="color:blue;">**Disaster Recovery (DR)**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">refers to the processes and systems used to</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**restore applications and data after a failure or disaster.**</mark>

[^28]: **Role-Based Access Control (RBAC)** is a security mechanism that **controls what users can access based on their role**.
