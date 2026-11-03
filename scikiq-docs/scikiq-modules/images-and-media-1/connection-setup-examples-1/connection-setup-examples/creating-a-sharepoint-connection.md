---
icon: page
---

# Creating a SharePoint Connection

***

**Contents**

* [**Instructions for Using this Page**](creating-a-sharepoint-connection.md#instructions-for-using-this-page)
* [**Overview**](creating-a-sharepoint-connection.md#overview)
* [**Procedure**](creating-a-sharepoint-connection.md#procedure)
* [**Related Topics**](creating-a-sharepoint-connection.md#related-topics)

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]
* At any time during the workflow, you can return to the previous section by clicking the **Previous** <img src="../../../../.gitbook/assets/image (204).png" alt="" data-size="original">button.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

This page explains how to create a **SharePoint** data source connection in SCIKIQ. The process involves a series of steps, which includes navigating to the SharePoint connection page, selecting a new or an existing data source, configuring the connection details, adding metadata, discovery, specifying owner, managed service, and connection type, reviewing the settings, and submitting the connection.

Once the connection is successfully established, the data source will appear on the **Connected Data Sources** page.&#x20;

***

## Procedure

The expandable panels below guide you through the process of creating a **SharePoint** connection in SCIKIQ. Follow each step in sequence while configuring the connection. The system enables the next step only after the current step is completed.

<details>

<summary>1.<strong>Navigate to SharePoint</strong> </summary>

A. On the **Left Navigation Bar**, expand **Connect to Data Source** under **SCIKIQ CONNECT**, and then click **Manage** **Data Source**.

<figure><img src="../../../../.gitbook/assets/Click Manage Data Source.png" alt="" width="509"><figcaption><p>Manage Data Source Menu Item</p></figcaption></figure>

The All Data Sources page is displayed.

B. On the **All Data Sources** page, click **Files** in the **left menu**, and then click **SharePoint** in the right pane.

<figure><img src="../../../../.gitbook/assets/S (226).png" alt=""><figcaption><p>Navigating to SharePoint</p></figcaption></figure>

The SharePoint page is displayed.&#x20;

</details>

<details>

<summary>2.<strong>Create Connection</strong></summary>

* On the **SharePoint** page, in the **Create Connection** section, select either a **new data source** or an **existing data source** depending on the requirement, and then click the **Next** button. See the below example image.&#x20;

<figure><img src="../../../../.gitbook/assets/S (220).png" alt=""><figcaption><p>Selecting Data Source</p></figcaption></figure>

The Connection Details section is highlighted.

</details>

<details>

<summary>3.<strong>Configure Connection Details</strong></summary>

**Purpose:**

When connecting a software application to a database, the system needs specific details to locate, identify, and authenticate the database. Each parameter plays a unique role.

**Procedure:**

The below step-by-step instructions help you understand how to configure connection details:

{% hint style="success" %}
**Tip:** The field names and their corresponding options in the below instructions are annotated with relevant descriptions. To view the description of a field or an option, simply hover your cursor over it. &#x20;
{% endhint %}

**Step-by-Step instructions**

A. On the **Connection Details page**, enter [<mark style="color:blue;">**URL**</mark>](#user-content-fn-2)[^2], [<mark style="color:blue;">**Tenant ID**</mark>](#user-content-fn-3)[^3]**,** and [<mark style="color:blue;">**Site Name**</mark>](#user-content-fn-4)[^4].&#x20;

{% hint style="info" %}
**Tip:** Client ID and Client Secret are populated by default.
{% endhint %}

B. Click the **Next** button. See the below example image.

<figure><img src="../../../../.gitbook/assets/S (227).png" alt=""><figcaption><p>Configuring Connection Details</p></figcaption></figure>

</details>

<details>

<summary>4.<strong>Add Metadata</strong></summary>

_**Purpose of adding metadata**_

While connecting the application to a database, adding **metadata** provides the application with important information about the data it will interact with. This metadata helps the system understand, organize, and manage the data correctly.

**Procedure:**

As part of the procedure, you need to specify catalogue, connectivity mechanism, store, source system, connection type, supporting email ID, and service type. Once done, you need to test by clicking the Test Connection button to check whether everything is correct.

{% hint style="success" %}
**Tip:** To assist with your setup, fields and options shown in blue are equipped with tooltips. Hovering your mouse over these items will reveal a detailed description of their function.
{% endhint %}

**Step-by-Step Instructions:**

The below step-by-step instructions help you understand how to add meta data.

In the **Add Meta Data** section:

* Specify [<mark style="color:blue;">**Catalogue,**</mark>](#user-content-fn-5)[^5] [<mark style="color:blue;">**Business Owner**</mark>](#user-content-fn-6)[^6]**,** and [<mark style="color:blue;">**Technical Owner**</mark>](#user-content-fn-7)[^7]**.**
* From the [<mark style="color:blue;">**Connectivity Mechanism**</mark>](#user-content-fn-8)[^8] options, select [<mark style="color:blue;">**Secured**</mark>](#user-content-fn-9)[^9]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Unsecured**</mark>](#user-content-fn-10)[^10], or [<mark style="color:blue;">**SSH Tunnelling**</mark>](#user-content-fn-11)[^11]**.**
* From the [<mark style="color:blue;">**Store**</mark>](#user-content-fn-12)[^12] options, select either [<mark style="color:blue;">**Is Feature Store**</mark>](#user-content-fn-13)[^13] or [<mark style="color:blue;">**Is Analytical Store**</mark>](#user-content-fn-14)[^14].
* From the [<mark style="color:blue;">**Source System**</mark>](#user-content-fn-15)[^15] drop-down box, select [<mark style="color:blue;">**Internal**</mark>](#user-content-fn-16)[^16] or [<mark style="color:blue;">**Third Party**</mark>](#user-content-fn-17)[^17].
* From the [<mark style="color:blue;">**Connection Type**</mark>](#user-content-fn-18)[^18] drop-down box, select [<mark style="color:blue;">**Access Layer**</mark>](#user-content-fn-19)[^19]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Source System**</mark>](#user-content-fn-20)[^20]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Reference System,**</mark>](#user-content-fn-21)[^21] or [<mark style="color:blue;">**Master Database**</mark>](#user-content-fn-22)[^22]<mark style="color:blue;">**.**</mark>
* In the **Supporting Email ID** field, specify the **supporting email ID** to contact when something goes wrong or when help is needed.
* From the **Service Type** drop-down box, select the **category of service** the data source provides.
* Specify [<mark style="color:blue;">**Service Id**</mark>](#user-content-fn-23)[^23] and [<mark style="color:blue;">**Application Id**</mark>](#user-content-fn-24)[^24]**.**
* Finally, click the **Test Connection** button to check everything is correct.

The **Connection tested successfully** message is displayed.

* Click the **Next** button.

<figure><img src="../../../../.gitbook/assets/S (228).png" alt=""><figcaption><p>Adding Meta Data</p></figcaption></figure>

The Discovery section is activated.

</details>

<details>

<summary>5.<strong>Discovery</strong></summary>

**Purpose**

Selecting **Source Tables** tells the system **which specific tables from the source database or application should be extracted and included in the connection setup.** This step defines the exact dataset that will be moved to the target system.

**Procedure Overview**

As part of the table selection step, select the required tables from the left box and move them to the right box in the Discovery section. You can choose a single table, multiple tables, or all tables, as required.

**Step-by-Step Instructions**

The following step-by-step instructions help you understand the process of discovery:

{% hint style="success" %}
**Tip:** In the below mentioned instructions, the field names and their corresponding options are annotated with relevant descriptions. To view the description of a field or an option, simply hover your cursor over it.&#x20;
{% endhint %}

A. In the **Discovery** section, select the **Discovery Settings** choosing from [<mark style="color:blue;">**Identify PII,**</mark>](#user-content-fn-25)[^25] [<mark style="color:blue;">**Data Profiling**</mark>](#user-content-fn-26)[^26], and [<mark style="color:blue;">**Data Summary**</mark>](#user-content-fn-27)[^27].

B. Next, click the **Search Storage** filter button.

<figure><img src="../../../../.gitbook/assets/S (229).png" alt=""><figcaption></figcaption></figure>

The Storage dialogue box is displayed.

C. On the **Storage** dialogue box, select the required **file extension**, and then click the **Search** button.

<figure><img src="../../../../.gitbook/assets/S (181).png" alt=""><figcaption><p>Selecting File Extension</p></figcaption></figure>

The Storage dialogue box is extended displaying a group of folders and files.

D. Now, from the **Storage** dialogue box, select the **required folder** or **file.**&#x20;

* Select the [<mark style="color:blue;">**Delimited Text File**</mark>](#user-content-fn-28)[^28] option choosing from **Comma, Tab, Semicolon, Space, or Other**.
* Enable the **First row is column header** option if required.
* Enable the [<mark style="color:blue;">**Skip Row(s)**</mark>](#user-content-fn-29)[^29] option if required.
* Click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (230).png" alt="" width="533"><figcaption><p>Folder Selection for Discovery</p></figcaption></figure>

The files are displayed on the left box (See the below **Selecting Files for Discovery** image).

* Now, from the **left box**, select the the **required files**, and then click the **Forward Arrow** button to move the files to the adjacent box.

{% hint style="info" %}
**Tip:**&#x20;

* You can move **multiple files** by selecting in the left side box and moving them to the right side box by clicking the ![](<../../../../.gitbook/assets/image (205).png>) button.
* You can also move **all** the files by clicking the ![](<../../../../.gitbook/assets/image (206).png>)button.
* If you wish to **move back either a single or multiple** files from the right box, then select them, and click the ![](<../../../../.gitbook/assets/image (207).png>) button.&#x20;
* If you wish to **move all the files** from the right box, then select all of them , and click the ![](<../../../../.gitbook/assets/image (208).png>) button.&#x20;
{% endhint %}

* Finally, click the **Next** button.

<figure><img src="../../../../.gitbook/assets/S (231).png" alt=""><figcaption><p>Selecting Files for Discovery</p></figcaption></figure>

The files are discovered and the Configuration section is activated.

</details>

<details>

<summary>6<strong>.Configuration</strong></summary>

* In the **Configuration** section:&#x20;
* Select the [<mark style="color:blue;">**Manage Service**</mark>](#user-content-fn-30)[^30] choosing from [<mark style="color:blue;">**Service Managed**</mark>](#user-content-fn-31)[^31] or [<mark style="color:blue;">**User Managed**</mark>](#user-content-fn-32)[^32].
* Select the **Connection type** choosing from **Secured Connection** or **Unsecured Connection.**
* Specify the [<mark style="color:blue;">**DR**</mark>](#user-content-fn-33)[^33] **availability** and [<mark style="color:blue;">**RBAC**</mark>](#user-content-fn-34)[^34] **implementation** choosing from **Yes** or **No**.
* Click the **Next** button.

<figure><img src="../../../../.gitbook/assets/S (232).png" alt=""><figcaption><p>Configuring Additional Details</p></figcaption></figure>

The Review & Submit section is activated.

</details>

<details>

<summary>7<strong>.Review &#x26; Submit</strong></summary>

* In the **Review & Submit** section, enter a **name** and **description** for the connection, and then click the **Finish** button to submit it.

<figure><img src="../../../../.gitbook/assets/S (233).png" alt=""><figcaption><p>Review and Submit</p></figcaption></figure>

The connection is created and the Connected Data Sources page is displayed.

</details>

***

## Related Topics

* [**Managing Connected Data Sources**](../../managing-connected-data-sources.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.

[^2]: The **URL** refers to the **full address** of your SharePoint site. For example,&#x20;    \
    https://example.sharepoint.com/sites/yoursitename

[^3]: **Tenant ID** is a unique identifier for your Azure AD organization.&#x20;

    **Note:** You can locate it in the Azure portal under Azure Active Directory > Properties.

[^4]: This refers to your SharePoint Site name.

[^5]: **Catalogue** refers to the group of related data sources.

[^6]: **Business Owner** refers to the person or team responsible for the data from a business point of view.

[^7]: **Technical Owner** refers to the **person or IT team** responsible for the technical side of the data.

[^8]: Connectivity Mechanism refers to the method used to connect to the data source.

[^9]: **Secured** option refers to the connection where data is encrypted, making it safe from hackers and unauthorized access.

[^10]: **Unsecured** option refers to the connection where data is sent without encryption.

[^11]: SSH Tunneling: SSH refers to Secure Shell. SSH is a secure way to connect to another computer or server over a network.

[^12]: This refers to how the data will be used.

[^13]: Select **Is Feature Store** if the data source is used to store and manage machine learning features.

[^14]: Select **Is Analytical Store** if the data source is primarily used for analytics, reporting, and business intelligence.

[^15]: This refers to the original system where the data comes from.

[^16]: An **Internal source system** is owned, managed, and maintained by your organization.

[^17]: A **Third-Party** source system is owned and managed by an external vendor or service provider.

[^18]: This refers to the kind of connection you are using to access the source.

[^19]: The **Access Layer** represents systems that are used to consume or expose data rather than originate it.

[^20]: A **Source System** is the origin of raw or transactional data.

[^21]: A Reference System stores standardized, lookup, or supporting data used across multiple systems.

[^22]: A **Master Database** stores authoritative master data for key business entities.

[^23]: This refers to the unique identifier for the service you are connecting to.

[^24]: This refers to the unique ID used to identify the application that owns, provides, or uses the data.

[^25]: **Identify PII** (Personally Identifiable Information) detects sensitive data elements that can identify an individual.

[^26]: **Data Profiling** analyzes the structure and content of data to understand its quality and patterns.

[^27]: **Data Summary** provides a high-level overview of the dataset.

[^28]: A **Delimited Text File** is a text file where information is separated by a specific character (like comma or tab) so that systems can easily understand and process the data.

[^29]: When the **Skip Row(s)** option is chosen while selecting a file for migration, the system **ignores (does not import) the specified number of rows from the top of the file** during data extraction.&#x20;

    This option is usually needed when the beginning of the file contains Extra header lines, Metadata information, Notes or comments, Blank rows, and Titles or descriptions, etc.

[^30]: **Manage Service** refers to who is responsible for managing the connection and its configuration.

[^31]: **Service Managed** means the system automatically manages the service for you.

[^32]: **User Managed** means you manage the service configuration yourself.

[^33]: **Disaster Recovery (DR)** refers to the processes and systems used to restore applications and data after a failure or disaster.

[^34]: **Role-Based Access Control (RBAC)** is a security mechanism that **controls what users can access based on their role**.
