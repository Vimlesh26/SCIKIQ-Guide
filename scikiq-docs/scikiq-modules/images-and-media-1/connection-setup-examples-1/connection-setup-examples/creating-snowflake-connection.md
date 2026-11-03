---
icon: page
---

# Creating Snowflake Connection

***

**Contents**

* [**Instructions for Using this Page**](creating-snowflake-connection.md#instructions-for-using-this-page)
* [**Overview**](creating-snowflake-connection.md#overview)
* [**Procedure**](creating-snowflake-connection.md#procedure)
* [**Related Topics**](creating-snowflake-connection.md#related-topics)

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]
* At any time during the workflow, you can return to the previous section by clicking the **Previous** <img src="../../../../.gitbook/assets/image (204).png" alt="" data-size="original">button.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

Creating a **Snowflake** connection involves a series of steps, including navigating to the Snowflake page, selecting a new or an existing data source, configuring the connection details, adding meta data, discovery, reviewing the settings, and submitting the connection.

Once the connection is successfully established, the data source will appear on the **Connected Data Sources** page.  &#x20;

***

## Procedure

Expand the panels below to view step-by-step instructions.

<details>

<summary><strong>Navigate to Snowflake Page</strong></summary>

1. On the **Left Navigation Bar**, expand **Connect to Data Source** under **SCIKIQ CONNECT**, and then click **Manage** **Data Source**.

<figure><img src="../../../../.gitbook/assets/image (2340).png" alt=""><figcaption></figcaption></figure>

The All Data Sources page is displayed.

2. On the **All Data Sources** page:

A. In the **Search** field, enter **Snowflake.**

The **Snowflake** icon is displayed.

B. Next, click on the **Snowflake** ico&#x6E;**.**

<figure><img src="../../../../.gitbook/assets/image (2363).png" alt=""><figcaption></figcaption></figure>

The **Snowflake** page is displayed. See the next panel.

</details>

<details>

<summary><strong>Select New Data Source Option</strong></summary>

* On the **Snowflake** page, select the **No. I'd like to create a new data source** option, and then click the **Next** button.

<figure><img src="../../../../.gitbook/assets/image (2356).png" alt=""><figcaption></figcaption></figure>

The **Connection Details** section is displayed.

</details>

<details>

<summary><strong>Configure Connection Details</strong></summary>

**Purpose**

While creating a connection, the system needs specific details to **locate**, **identify**, and **authenticate** the database. Each parameter plays a unique role.

**Procedure**

The below step-by-step instructions help you understand how to configure connection details:

_**Step-by-Step Instructions:**_

1. In the **Connection Details** section, enter the [<mark style="color:blue;">**Host Name**</mark>](#user-content-fn-1)[^1]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Port,**</mark>](#user-content-fn-2)[^2] [<mark style="color:blue;">**Database Name,**</mark>](#user-content-fn-3)[^3] [<mark style="color:blue;">**Database Schema,**</mark>](#user-content-fn-4)[^4] **Database User,** and **Database Password.**&#x20;
2. Select **Fetch credential (Password/PAT) from key vault** option if you want to enable the application to retrieve the database password or **Personal Access Token (PAT)** securely from a configured **Key Vault** instead of requiring you to enter the credential manually.
3. From the **PAT Authentication** options, select **Yes** or **No**.

> <mark style="color:red;">**Note:**</mark> **PAT** stands for **Personal Access Token**.
>
> A **Personal Access Token (PAT)** is a secure, randomly generated token that acts as an alternative to a password for authenticating a user or application. Instead of using a username and password, the application uses the PAT to securely access services such as Snowflake.

4. In the **Warehouse** field, enter the **name of the Snowflake Virtual Warehouse** that the application should use to execute queries and process data.
5. In the **Role** field, enter the **name of the Snowflake Role** assigned to the user. For example, SYSADMIN.

> <mark style="color:red;">**Note:**</mark> The role determines the permissions available during the connection.

B. Click the **Next** button.

The **Add Meta Data** section is displayed.

</details>

<details>

<summary><strong>Add Meta Data</strong></summary>

**Purpose**

While creating a connection, adding **metadata** provides the application with important information about the data it will interact with. This metadata helps the system understand, organize, and manage the data correctly.

**Procedure:**

As part of the procedure, you need to specify catalogue, connectivity mechanism, store, source system, connection type, supporting email ID, and service type. Once done, you need to test by clicking the Test Connection button to check whether everything is correct.

{% hint style="success" %}
**Tip:** To assist with your setup, fields and options shown in blue are equipped with tooltips. Hovering your mouse over these items will reveal a detailed description of their function.
{% endhint %}

_**Step-by-Step Instructions:**_

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

<figure><img src="../../../../.gitbook/assets/image (2379).png" alt=""><figcaption></figcaption></figure>

The **Discovery** section is displayed.

</details>

<details>

<summary><strong>Discovery</strong></summary>

**Purpose:**

During the Discovery step, the system displays the tables based on the schema provided in the connection details. For each table, it shows the schema name along with the number of rows and columns. If no schema is specified, the system displays tables from all schemas available in the database.

**Procedure:**&#x20;

Selecting **Source Tables** tells the system **which specific tables from the source database or application should be extracted and included in the connection setup.** This step defines the exact dataset that will be moved to the target system.

As part of the table selection step, you need to select the required tables from the left pane Discovery section and move them to the right pane. You can choose a single table, multiple tables, or all tables, as required.

**Step-by-Step Instructions:**

The following step-by-step instructions help you understand the process of discovery:

{% hint style="success" %}
**Tip:** In the below mentioned instructions, the field names and their corresponding options are annotated with relevant descriptions. To view the description of a field or an option, simply hover your cursor over it.&#x20;
{% endhint %}

1. In the **Discovery** section, select the **Discovery Settings** choosing from [<mark style="color:blue;">**Identify PII,**</mark>](#user-content-fn-25)[^25] [<mark style="color:blue;">**Data Profiling**</mark>](#user-content-fn-26)[^26], and [<mark style="color:blue;">**Data Summary**</mark>](#user-content-fn-27)[^27].
2. From the **left box**, select the **required tables**, and then click the **Forward Arrow** button to move those files to the adjacent box.

{% hint style="info" %}
**Tip:**&#x20;

* You can migrate **multiple files** by selecting in the left side box and moving them to the right side box by clicking the ![](<../../../../.gitbook/assets/image (205).png>) button.
* You can also migrate **all** the files by clicking the ![](<../../../../.gitbook/assets/image (206).png>)button.
* If you wish to **move back either a single or multiple** files from the right box, then select them, and click the ![](<../../../../.gitbook/assets/image (207).png>) button.&#x20;
* If you wish to **move all the files** from the right box, then select all of them , and click the ![](<../../../../.gitbook/assets/image (208).png>) button.&#x20;
{% endhint %}

3. Click the **Next** button. See the below example image.

<figure><img src="../../../../.gitbook/assets/image (2380).png" alt=""><figcaption></figcaption></figure>

The Warning message is displayed.

4. Review the **Warning** message, and then click the **Yes** button.

<figure><img src="../../../../.gitbook/assets/image (2381).png" alt=""><figcaption></figcaption></figure>

The Configuration section is displayed.

</details>

<details>

<summary><strong>Specify Owner, Managed Service, and Connection Type</strong></summary>

1. In the **Configuration** section, select the **owner** choosing from **Owner** or **Third Party**.
2. Select the [<mark style="color:blue;">**Manage Service**</mark>](#user-content-fn-28)[^28] choosing from [<mark style="color:blue;">**Service Managed**</mark>](#user-content-fn-29)[^29] or [<mark style="color:blue;">**User Managed**</mark>](#user-content-fn-30)[^30].
3. Select the **Connection type** choosing from **Secured Connection** or **Unsecured Connection.**
4. From the [<mark style="color:blue;">**DR**</mark>](#user-content-fn-31)[^31] Available options, select **Yes** or **No**.&#x20;
5. From the [<mark style="color:blue;">**RBAC**</mark>](#user-content-fn-32)[^32] Implemented options, select **Yes** or **No**.
6. Click the **Next** button.

<figure><img src="../../../../.gitbook/assets/image (2382).png" alt=""><figcaption></figcaption></figure>

The **Review & Submit** section is activated.

</details>

<details>

<summary><strong>Review and Submit</strong></summary>

* As the final step, review the details, and then click the **Finish** button to submit it.

<figure><img src="../../../../.gitbook/assets/image (2383).png" alt=""><figcaption></figcaption></figure>

The connection is created and the [**Connected Data Sources**](../../managing-connected-data-sources.md) page is displayed.

</details>

***

## Related Topics

* [**Managing Connected Data Sources**](../../managing-connected-data-sources.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.

[^2]: **Port** refers to the number on the server used to talk to the database. Different services use different ports.

[^3]: **Database** name refers to the **name of the database** you need to connect to on the server.

[^4]: **Database Schema** refers to the folder inside the database that organizes tables and other objects.

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

[^28]: **Manage Service** refers to who is responsible for managing the connection and its configuration.

[^29]: **Service Managed** means the system automatically manages the service for you.

[^30]: **User Managed** means you manage the service configuration yourself.

[^31]: <mark style="color:blue;">**DR**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">refers to</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**Disaster Recovery**</mark>

[^32]: **RBAC** refers to **Role-Based Access Control**.
