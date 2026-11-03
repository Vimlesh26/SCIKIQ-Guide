---
icon: page
---

# Creating a File Storage: SFTP/FTP Connection

***

**Contents**

* [**Instructions for Using this Page**](creating-a-file-storage-sftp-ftp-connection.md#instructions-for-using-this-page)
* [**Overview**](creating-a-file-storage-sftp-ftp-connection.md#overview)
* [**Procedure**](creating-a-file-storage-sftp-ftp-connection.md#procedure)
* [**Related Topics**](creating-a-file-storage-sftp-ftp-connection.md#related-topics)

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]
* At any time during the workflow, you can return to the previous section by clicking the **Previous** <img src="../../../../.gitbook/assets/image (204).png" alt="" data-size="original">button.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

This page explains how to create a SFTP/FTP connection connection in SCIKIQ. The process involves a series of steps, which includes navigating to the SFTP connection page, selecting a new or existing data source, configuring the connection details, adding metadata, specifying owner, managed service, and connection type, reviewing the settings, and submitting the connection.

Once the connection is successfully established, the data source will appear on the **Connected Data Sources** page.&#x20;

***

## Procedure

The expandable panels below guide you through the process of creating a SFTP connection in SCIKIQ. Follow each step in sequence while configuring the connection. The system enables the next step only after the current step is completed.

<details>

<summary>1.<strong>Navigate to SFTP</strong></summary>

A. On the **Left Navigation Bar**, expand **Connect to Data Source** under **SCIKIQ CONNECT**, and then click **Manage** **Data Source**.

<figure><img src="../../../../.gitbook/assets/Click Manage Data Source.png" alt=""><figcaption><p>Manage Data Source Menu Item</p></figcaption></figure>

The All Data Sources page is displayed.

B. On the **All Data Sources** page, click **Files** in the **left pane.**

<figure><img src="../../../../.gitbook/assets/S (163).png" alt=""><figcaption><p>Files Menu Item</p></figcaption></figure>

The data sources related to files are displayed on the right pane.

C. Now, on the **Right Pane,** click **SFTP.**

<figure><img src="../../../../.gitbook/assets/S (164).png" alt=""><figcaption><p>SFTP Data Source</p></figcaption></figure>

The FTP/SFTP page is displayed.&#x20;

</details>

<details>

<summary>2.<strong>Create Connection</strong></summary>

* On the **FTP/SFTP** page, in the **Create Connection** section, select either a **new data source** or an **existing data source** depending on the requirement, and then click the **Next** button. See the below example image.&#x20;

<figure><img src="../../../../.gitbook/assets/S (165).png" alt=""><figcaption><p>Selecting a Data Source</p></figcaption></figure>

The Connection Details section is highlighted.

</details>

<details>

<summary>3.<strong>Configure Connection Details</strong></summary>

**Purpose:**

When connecting a software application to a database, the system needs specific details to **locate**, **identify**, and **authenticate** the database. Each parameter plays a unique role.

**Procedure:**

The below instructions help you understand how to configure connection details:

{% hint style="success" %}
**Tip:** The blue dotted texts in the below instructions are annotations, which provides description about the field options. To view an annotation, simply hover your cursor over it. &#x20;
{% endhint %}

In the **Connection Details** section:

* From the **Source Type** drop-down box, select [<mark style="color:blue;">**SFTP**</mark>](#user-content-fn-2)[^2] or [<mark style="color:blue;">**FTP**</mark>](#user-content-fn-3)[^3].
* From the **Logon Type** drop-down box, select [<mark style="color:blue;">**Normal**</mark>](#user-content-fn-4)[^4] or [<mark style="color:blue;">**Key File**</mark>](#user-content-fn-5)[^5].

> <mark style="color:red;">**Note:**</mark> The **Logon Type** drop-down box is displayed only when SFTP is selected.

* Enter the [<mark style="color:blue;">**Host Name**</mark>](#user-content-fn-6)[^6]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Port**</mark>](#user-content-fn-7)[^7]<mark style="color:blue;">**,**</mark>**&#x20;Database User** and **Database Password.** See the below example screenshot.

<figure><img src="../../../../.gitbook/assets/S (166).png" alt=""><figcaption><p>Configuring Connection Details</p></figcaption></figure>

* Click the **Next** button.

The Add Metadata section is activated.

</details>

<details>

<summary>4.<strong>Add Metadata</strong></summary>

**Purpose:**

While connecting the application to a database, adding **metadata** provides the application with important information about the data it will interact with. This metadata helps the system understand, organize, and manage the data correctly.

**Procedure**

The below instructions help you understand how to add meta data.

{% hint style="success" %}
**Tip:** The field names and their corresponding options in the below instructions are annotated with relevant descriptions. To view the description of a field or an option, simply hover your cursor over it.&#x20;
{% endhint %}

In the **Add Meta Data** section:

* Specify [<mark style="color:blue;">**Catalogue,**</mark>](#user-content-fn-8)[^8] [<mark style="color:blue;">**Business Owner**</mark>](#user-content-fn-9)[^9]**,** and [<mark style="color:blue;">**Technical Owner**</mark>](#user-content-fn-10)[^10]**.**
* From the [<mark style="color:blue;">**Connectivity Mechanism**</mark>](#user-content-fn-11)[^11] options, select [<mark style="color:blue;">**Secured**</mark>](#user-content-fn-12)[^12]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Unsecured**</mark>](#user-content-fn-13)[^13], or [<mark style="color:blue;">**SSH Tunnelling**</mark>](#user-content-fn-14)[^14]**.**
* From the [<mark style="color:blue;">**Store**</mark>](#user-content-fn-15)[^15] options, select either [<mark style="color:blue;">**Is Feature Store**</mark>](#user-content-fn-16)[^16] or [<mark style="color:blue;">**Is Analytical Store**</mark>](#user-content-fn-17)[^17].
* From the [<mark style="color:blue;">**Source System**</mark>](#user-content-fn-18)[^18] drop-down box, select [<mark style="color:blue;">**Internal**</mark>](#user-content-fn-19)[^19] or [<mark style="color:blue;">**Third Party**</mark>](#user-content-fn-20)[^20].
* From the [<mark style="color:blue;">**Connection Type**</mark>](#user-content-fn-21)[^21] drop-down box, select [<mark style="color:blue;">**Access Layer**</mark>](#user-content-fn-22)[^22]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Source System**</mark>](#user-content-fn-23)[^23]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Reference System,**</mark>](#user-content-fn-24)[^24] or [<mark style="color:blue;">**Master Database**</mark>](#user-content-fn-25)[^25]<mark style="color:blue;">**.**</mark>
* In the **Supporting Email ID** field, specify the **supporting email ID** to contact when something goes wrong or when help is needed.
* From the **Service Type** drop-down box, select the **category of service** the data source provides.
* Specify [<mark style="color:blue;">**Service Id**</mark>](#user-content-fn-26)[^26] and [<mark style="color:blue;">**Application Id**</mark>](#user-content-fn-27)[^27]**.**
* Finally, click the **Test Connection** button to check everything is correct.

<figure><img src="../../../../.gitbook/assets/S (167).png" alt=""><figcaption><p>Adding Meta Data</p></figcaption></figure>

The **Connection tested successfully** message is displayed.

* Click the **Next** button.

The Configuration section is activated.

</details>

<details>

<summary>5<strong>.Configuration</strong></summary>

* In the **Configuration** section, select the **owner** choosing from **Owner** or **Third Party**.
* Select the [<mark style="color:blue;">**Manage Service**</mark>](#user-content-fn-28)[^28] choosing from [<mark style="color:blue;">**Service Managed**</mark>](#user-content-fn-29)[^29] or [<mark style="color:blue;">**User Managed**</mark>](#user-content-fn-30)[^30].
* Select the **Connection type** choosing from **Secured Connection** or **Unsecured Connection.**
* Click the **Next** button.

<figure><img src="../../../../.gitbook/assets/S (168).png" alt=""><figcaption><p>Configuring Additional Details</p></figcaption></figure>

The Review & Submit section is activated.

</details>

<details>

<summary>6.<strong>Review &#x26; Submit</strong></summary>

* In the **Review & Submit** section, enter a **name** and **description** for the connection, and then click the **Finish** button to submit it.

<figure><img src="../../../../.gitbook/assets/S (169).png" alt=""><figcaption><p>Review and Submit</p></figcaption></figure>

The connection is created and the [Connected Data Sources](/broken/pages/dgiZ3ktrQlmTnR2Pq3nV) page is displayed.

</details>

***

## Related Topics

* [**Managing Connected Data Sources**](../../managing-connected-data-sources.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.

[^2]: Secure File Transfer Protocol

[^3]: File Transfer Protocol

[^4]: **Normal** logon uses a **username and password** to authenticate the connection.&#x20;

[^5]: **Key File logon** authenticates using a private key file (such as an SSH key) instead of a password. It offers higher security and is commonly used for SFTP and other secure server connections.

[^6]: **Host Name** refers to the address of the computer/server where your database is located.

[^7]: **Port** refers to the number on the server used to talk to the database. Different services use different ports.

[^8]: **Catalogue** refers to the group of related data sources.

[^9]: **Business Owner** refers to the person or team responsible for the data from a business point of view.

[^10]: **Technical Owner** refers to the **person or IT team** responsible for the technical side of the data.

[^11]: Connectivity Mechanism refers to the method used to connect to the data source.

[^12]: **Secured** option refers to the connection where data is encrypted, making it safe from hackers and unauthorized access.

[^13]: **Unsecured** option refers to the connection where data is sent without encryption.

[^14]: SSH Tunneling: SSH refers to Secure Shell. SSH is a secure way to connect to another computer or server over a network.

[^15]: This refers to how the data will be used.

[^16]: Select **Is Feature Store** if the data source is used to store and manage machine learning features.

[^17]: Select **Is Analytical Store** if the data source is primarily used for analytics, reporting, and business intelligence.

[^18]: This refers to the original system where the data comes from.

[^19]: An **Internal source system** is owned, managed, and maintained by your organization.

[^20]: A **Third-Party** source system is owned and managed by an external vendor or service provider.

[^21]: This refers to the kind of connection you are using to access the source.

[^22]: The **Access Layer** represents systems that are used to consume or expose data rather than originate it.

[^23]: A **Source System** is the origin of raw or transactional data.

[^24]: A Reference System stores standardized, lookup, or supporting data used across multiple systems.

[^25]: A **Master Database** stores authoritative master data for key business entities.

[^26]: This refers to the unique identifier for the service you are connecting to.

[^27]: This refers to the unique ID used to identify the application that owns, provides, or uses the data.

[^28]: **Manage Service** refers to who is responsible for managing the connection and its configuration.

[^29]: **Service Managed** means the system automatically manages the service for you.

[^30]: User Managed means you manage the service configuration yourself.
