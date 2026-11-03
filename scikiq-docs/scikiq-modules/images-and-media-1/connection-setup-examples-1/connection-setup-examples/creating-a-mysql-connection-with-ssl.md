---
icon: page
---

# Creating a MySQL Connection with SSL

***

**Contents**

* [**Instructions for Using this Page**](creating-a-mysql-connection-with-ssl.md#instructions-for-using-this-page)
* [**Overview**](creating-a-mysql-connection-with-ssl.md#overview)
* [**Procedure**](creating-a-mysql-connection-with-ssl.md#procedure)
* [**Related Topics**](creating-a-mysql-connection-with-ssl.md#related-topics)

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]
* At any time during the workflow, you can return to the previous section by clicking the **Previous** <img src="../../../../.gitbook/assets/image (204).png" alt="" data-size="original">button.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

This page describes how to create a MySQL connection in SCIKIQ. As part of the setup, you must enable SSL and configure the required security settings, including providing the necessary certificate files, selecting the appropriate SSL mode, and ensuring secure, encrypted communication with the MySQL database.

The setup is completed by following a sequence of guided steps. Once the connection is successfully established, the data source will appear on the **Connected Data Sources** page.&#x20;

***

## Procedure

#### Procedure

The expandable panels below guide you through the process of creating a MySQL connection with SSL Connection. Follow each step in sequence while configuring the connection. The system nables the next step only after the current step is completed.

<details>

<summary>1.<strong>Navigate to Data Source</strong></summary>

A. On the **Left Navigation Bar**, expand **Connect to Data Source** under **SCIKIQ CONNECT**, and then click **Manage** **Data Source**.

<figure><img src="../../../../.gitbook/assets/Click Manage Data Source.png" alt=""><figcaption><p>Manage Data Source Menu Item</p></figcaption></figure>

The All Data Sources page is displayed.

B. On the **All Data Sources** page, click **Relational Database** in the **left pane**.&#x20;

<figure><img src="../../../../.gitbook/assets/S (148).png" alt=""><figcaption><p>Relational Database Menu Item</p></figcaption></figure>

The available relational databases appear on the right pane.&#x20;

C. On the **Right Pane,** click **MySQL**.

<figure><img src="../../../../.gitbook/assets/S (154).png" alt=""><figcaption><p>MySQL Data Source</p></figcaption></figure>

The **MySQL** page is displayed.&#x20;

</details>

<details>

<summary>2.<strong>Create Connection</strong></summary>

* On the **MySQL** page, in the **Create Connection** section, select either a **new data source** or **an existing data source**, and then click the **Next** button. See the below example image.&#x20;

<figure><img src="../../../../.gitbook/assets/S (155).png" alt=""><figcaption><p>Selecting Data Source</p></figcaption></figure>

The Connection Details section is highlighted.

</details>

<details>

<summary>3.<strong>Configure Connection Details</strong></summary>

**Purpose:**&#x20;

When connecting a software application to a database, the system needs specific details to **locate**, **identify**, and **authenticate** the database. Each parameter plays a unique role.

**Procedure:**

The below instructions help you understand how to configure connection details:

{% hint style="success" %}
**Tip:** The field names and their corresponding options in the below instructions are annotated with relevant descriptions. To view the description of a field or an option, simply hover your cursor over it.&#x20;
{% endhint %}

**Step-by-Step Instructions:**

A. In the **Connection Details** section, enter the [<mark style="color:blue;">**Host Name**</mark>](#user-content-fn-2)[^2]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Port,**</mark>](#user-content-fn-3)[^3] [<mark style="color:blue;">**Database Name,**</mark>](#user-content-fn-4)[^4] [<mark style="color:blue;">**Service**</mark>](#user-content-fn-5)[^5]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Database Schema,**</mark>](#user-content-fn-6)[^6] **Database User,** and **Database Password.** See the below example image.

<figure><img src="../../../../.gitbook/assets/S (156).png" alt=""><figcaption><p>Configuring Connection Details</p></figcaption></figure>

B. Click the **Next** button.

The Add Metadata section is activated.

</details>

<details>

<summary>4.<strong>Add Metadata</strong></summary>

**Purpose:**

While connecting the application to a database, adding **metadata** provides the application with important information about the data it will interact with. This metadata helps the system understand, organize, and manage the data correctly.

**Procedure:**

The below instructions help you understand how to add meta data:

{% hint style="success" %}
**Tip:** The field names and their corresponding options in the below instructions are annotated with relevant descriptions. To view the description of a field or an option, simply hover your cursor over it.&#x20;
{% endhint %}

In the **Add Meta Data** section:

* Specify [<mark style="color:blue;">**Catalogue**</mark>](#user-content-fn-7)[^7]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Business Owner**</mark>](#user-content-fn-8)[^8]**,** and [<mark style="color:blue;">**Technical Owner**</mark>](#user-content-fn-9)[^9]**.**
* From the [<mark style="color:blue;">**Connectivity Mechanism**</mark>](#user-content-fn-10)[^10] options, select [<mark style="color:blue;">**Secured**</mark>](#user-content-fn-11)[^11]<mark style="color:blue;">**,**</mark> and then specify the [<mark style="color:blue;">**SSL Key File**</mark>**,**](#user-content-fn-12)[^12] [<mark style="color:blue;">**SSL CERT File**</mark>](#user-content-fn-13)[^13]**,** and [<mark style="color:blue;">**SSL CA File**</mark>**.**](#user-content-fn-14)[^14]
* From the [<mark style="color:blue;">**Store**</mark>](#user-content-fn-15)[^15] options, select either [<mark style="color:blue;">**Is Feature Store**</mark>](#user-content-fn-16)[^16] or [<mark style="color:blue;">**Is Analytical Store**</mark>](#user-content-fn-17)[^17].
* From the [<mark style="color:blue;">**Source System**</mark>](#user-content-fn-18)[^18] drop-down box, select [<mark style="color:blue;">**Internal**</mark>](#user-content-fn-19)[^19] or [<mark style="color:blue;">**Third Party**</mark>](#user-content-fn-20)[^20].
* From the [<mark style="color:blue;">**Connection Type**</mark>](#user-content-fn-21)[^21] drop-down box, select [<mark style="color:blue;">**Access Layer**</mark>](#user-content-fn-22)[^22]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Source System**</mark>](#user-content-fn-23)[^23]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Reference System**</mark>](#user-content-fn-24)[^24]<mark style="color:blue;">**,**</mark> or [<mark style="color:blue;">**Master Database**</mark>](#user-content-fn-25)[^25]<mark style="color:blue;">**.**</mark>
* In the **Supporting Email ID** field, specify the **supporting email ID** to contact when something goes wrong or when help is needed.
* From the **Service Type** drop-down box, select the **category of service** the data source provides.
* Specify [<mark style="color:blue;">**Service Id**</mark>](#user-content-fn-26)[^26] and [<mark style="color:blue;">**Application Id**</mark>](#user-content-fn-27)[^27]**.**
* Finally, click the **Test Connection** button to check everything is correct.

<figure><img src="../../../../.gitbook/assets/S (157).png" alt=""><figcaption><p>Adding Meta Data</p></figcaption></figure>

* Click the **Test Connection** button at the bottom to check if the connection is correct.

The **Connection tested successfully** message is displayed.

* Click the **Next** button.

The Discovery section is activated.

</details>

<details>

<summary>5.<strong>Discovery</strong></summary>

_**Purpose**_

Selecting **Source Tables** tells the system **which specific tables from the source database or application should be extracted and included in the connection setup.** This step defines the exact dataset that will be moved to the target system.

_**Procedure Overview**_

As part of the table selection step, select the required tables from the left box and move them to the right box in the Discovery section. You can choose a single table, multiple tables, or all tables, as required.

**Step-by-Step Instructions**

The following step-by-step instructions help you understand the process of discovery:

{% hint style="success" %}
**Tip:** In the below mentioned instructions, the field names and their corresponding options are annotated with relevant descriptions. To view the description of a field or an option, simply hover your cursor over it.&#x20;
{% endhint %}

* In the **Discovery** section, select the **Discovery Settings** choosing from [<mark style="color:blue;">**Identify PII,**</mark>](#user-content-fn-28)[^28] [<mark style="color:blue;">**Data Profiling**</mark>](#user-content-fn-29)[^29], and [<mark style="color:blue;">**Data Summary**</mark>](#user-content-fn-30)[^30].
* From the **left box**, select the the **required tables**, and then click the **Forward Arrow** button to move those files to the adjacent box.

{% hint style="info" %}
**Tip:**&#x20;

* You can migrate **multiple files** by selecting in the left side box and moving them to the right side box by clicking the ![](<../../../../.gitbook/assets/image (205).png>) button.
* You can also migrate **all** the files by clicking the ![](<../../../../.gitbook/assets/image (206).png>)button.
* If you wish to **move back either a single or multiple** files from the right box, then select them, and click the ![](<../../../../.gitbook/assets/image (207).png>) button.&#x20;
* If you wish to **move all the files** from the right box, then select all of them , and click the ![](<../../../../.gitbook/assets/image (208).png>) button.&#x20;
{% endhint %}

* Finally, click the **Next** button.

<figure><img src="../../../../.gitbook/assets/S (153).png" alt=""><figcaption><p>Selecting Tables for Discovery</p></figcaption></figure>

The files are discovered.

The Configuration section is activated.

</details>

<details>

<summary>6<strong>.Configuration</strong></summary>

* In the **Configuration** section, select the **owner** choosing from **Owner** or **Third Party**.
* Select the [<mark style="color:blue;">**Manage Service**</mark>](#user-content-fn-31)[^31] choosing from [<mark style="color:blue;">**Service Managed**</mark>](#user-content-fn-32)[^32] or [<mark style="color:blue;">**User Managed**</mark>](#user-content-fn-33)[^33].
* Select the **Connection type** choosing from **Secured Connection** or **Unsecured Connection.**
* Specify [<mark style="color:blue;">**DR**</mark>](#user-content-fn-34)[^34] availability choosing from **Yes** or **No**.
* Specify [<mark style="color:blue;">**RBAC**</mark>](#user-content-fn-35)[^35]  implementation choosing from **Yes** or **No**.
* Click the **Next** button.

<figure><img src="../../../../.gitbook/assets/S (158).png" alt=""><figcaption><p>Configuring Additional Details</p></figcaption></figure>

The Review & Submit section is activated.

</details>

<details>

<summary>7.<strong>Review &#x26; Submit</strong></summary>

* In the **Review & Submit** section, enter a **name** and **description** for the connection, and then click the **Finish** button to submit it.

<figure><img src="../../../../.gitbook/assets/Review and Submit.png" alt=""><figcaption><p>Review and Submit</p></figcaption></figure>

The connection is created and the [**Connected Data Sources**](../../managing-connected-data-sources.md#viewing-connected-data-sources) page is displayed.

</details>

***

## Related Topics

* [**Managing Connected Data Sources**](../../managing-connected-data-sources.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.

[^2]: This refers to the **address** of the computer/server where your database is located.

[^3]: Port refers to the number on the server used to talk to the database. Different services use different ports.

[^4]: Database name refers to the **name of the database** you need to connect to on the server.

[^5]: Service refers to the predefined **connection name** used by the database to identify the database service running on the server.

[^6]: Database Schema refers to the folder inside the database that organizes tables and other objects.

[^7]: <mark style="color:blue;">**Catalogue**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">refers to the group of related data sources.</mark>

[^8]: <mark style="color:blue;">**Business Owner**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">refers to the person or team responsible for the data from a business point of view.</mark>

[^9]: <mark style="color:blue;">**Technical Owner**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">refers to the</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**person or IT team**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">responsible for the technical side of the data.</mark>

[^10]: <mark style="color:blue;">**Connectivity Mechanism**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">refers to the method used to connect to the data source.</mark>

[^11]: <mark style="color:blue;">**Secured**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">option refers to the connection where data is encrypted, making it safe from hackers and unauthorized access.</mark>

[^12]: It contains the **private key** of the client or server and used to encrypt data and prove the identity of the client or server. Its purpose is to authenticate the client/server and enables encrypted communication.

[^13]: It contains the **public certificate** associated with the private key and used by the server or client to verify identity. It is typically issued by a Certificate Authority (CA) or self-signed. Its purpose is to confirm the identity of the client or server.

[^14]: It contains the **Certificate Authority (CA) certificate** and used to verify that the SSL certificate is trusted. It helps prevent man-in-the-middle attacks. Its purpose is to validate the trustworthiness of the SSL certificate.

[^15]: <mark style="color:blue;">This refers to how the data will be used.</mark>

[^16]: <mark style="color:blue;">Select</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**Is Feature Store**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">if the data source is used to store and manage machine learning features.</mark>

[^17]: <mark style="color:blue;">Select</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**Is Analytical Store**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">if the data source is primarily used for analytics, reporting, and business intelligence.</mark>

[^18]: <mark style="color:blue;">This refers to the</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**original system**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">where the data comes from.</mark>

[^19]: <mark style="color:blue;">An</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**Internal**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">source system is owned, managed, and maintained by your organization.</mark>

[^20]: <mark style="color:blue;">A</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**Third-Party**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">source system is owned and managed by an external vendor or service provider.</mark>

[^21]: <mark style="color:blue;">This refers to the</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**kind of connection**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">you are using to access the source.</mark>

[^22]: <mark style="color:blue;">The</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**Access Layer**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">represents systems that are used to</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**consume or expose data**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">rather than originate it.</mark>

[^23]: <mark style="color:blue;">A</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**Source System**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">is the</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**origin of raw or transactional data**</mark><mark style="color:blue;">.</mark>

[^24]: <mark style="color:blue;">A</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**Reference System**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">stores</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**standardized, lookup, or supporting data**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">used across multiple systems.</mark>

[^25]: <mark style="color:blue;">A</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**Master Database**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">stores</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**authoritative master data**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">for key business entities.</mark>

[^26]: <mark style="color:blue;">This refers to the</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**unique identifier**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">for the service you are connecting to.</mark>&#x20;

[^27]: <mark style="color:blue;">This refers to the</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**unique ID used to identify the application**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">that owns, provides, or uses the data.</mark>

[^28]: **Identify PII** (Personally Identifiable Information) detects sensitive data elements that can identify an individual.

[^29]: **Data Profiling** analyzes the structure and content of data to understand its quality and patterns.

[^30]: **Data Summary** provides a high-level overview of the dataset.

[^31]: **Manage Service** refers to who is responsible for managing the connection and its configuration.

[^32]: **Service Managed** means the system automatically manages the service for you.

[^33]: **User Managed** means you manage the service configuration yourself.

[^34]: **Disaster Recovery (DR)** refers to the processes and systems used to **restore applications and data after a failure or disaster**.

[^35]: **Role-Based Access Control (RBAC)** is a security mechanism that **controls what users can access based on their role**.
