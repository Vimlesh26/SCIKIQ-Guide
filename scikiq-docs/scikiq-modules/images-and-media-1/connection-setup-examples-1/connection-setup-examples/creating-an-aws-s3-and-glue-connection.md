---
icon: page
---

# Creating an AWS S3 & Glue Connection

***

**Contents**

* [**Instructions for Using this Page**](creating-an-aws-s3-and-glue-connection.md#instructions-for-using-this-page)
* [**Overview**](creating-an-aws-s3-and-glue-connection.md#overview)
* [**Procedure**](creating-an-aws-s3-and-glue-connection.md#procedure)
* [**Related Topics**](creating-an-aws-s3-and-glue-connection.md#related-topics)

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]
* At any time during the workflow, you can return to the previous section by clicking the **Previous** <img src="../../../../.gitbook/assets/image (204).png" alt="" data-size="original">button.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

This page explains how to create an **AWS S3 & Glue** data source connection in SCIKIQ. The process involves a series of steps, which includes navigating to the **AWS S3 & Glue** connection page, selecting a new or existing data source, configuring the connection details, adding metadata, discovery, specifying owner, managed service, and connection type, reviewing the settings, and submitting the connection.

Once the connection is successfully established, the data source will appear on the **Connected Data Sources** page.&#x20;

***

## Procedure

The expandable panels below guide you through the process of creating an **AWS S3 & Glue** connection in SCIKIQ. Follow each step in sequence while configuring the connection. The system enables the next step only after the current step is completed.

<details>

<summary>1.<strong>Navigate to Amazon S3</strong></summary>

A. On the **Left Navigation Bar**, expand **Connect to Data Source** under **SCIKIQ CONNECT**, and then click **Manage** **Data Source**.

<figure><img src="../../../../.gitbook/assets/Click Manage Data Source.png" alt=""><figcaption><p>Manage Data Source Menu Item</p></figcaption></figure>

The All Data Sources page is displayed.

B. On the **All Data Sources** page, click **Files** in the **left menu**, and then click **Amazon S3** in the right pane.

> <mark style="color:red;">**Note:**</mark> If you want to create an **Amazon Glue** connection, then click **Glue** <img src="../../../../.gitbook/assets/image (1625).png" alt="" data-size="line">.

<figure><img src="../../../../.gitbook/assets/S (176).png" alt=""><figcaption><p>Navigating to Amazon S3</p></figcaption></figure>

The Amazon S3 page is displayed.&#x20;

</details>

<details>

<summary>2.<strong>Create Connection</strong></summary>

* On the **Amazon S3** page, in the **Create Connection** section, select either a **new data source** or an **existing data source** depending on the requirement, and then click the **Next** button. See the below example image.&#x20;

<figure><img src="../../../../.gitbook/assets/S (177).png" alt=""><figcaption><p>Selecting Data Source</p></figcaption></figure>

The Connection Details section is highlighted.

</details>

<details>

<summary>3.<strong>Configure Connection Details</strong></summary>

**Purpose:**

When connecting a software application to a database, the system needs specific details to **locate**, **identify**, and **authenticate** the database. Each parameter plays a unique role.

**Procedure:**

The below instructions help you understand how to configure connection details:

{% hint style="success" %}
**Tip:** The blue dotted texts in the below instructions are annotations, which provides description about the field options. To view an annotation, simply hover your cursor over it.&#x20;
{% endhint %}

A. In the **Connection Details** section:

* Specify [<mark style="color:blue;">**AWS Access key,**</mark>](#user-content-fn-2)[^2] [<mark style="color:blue;">**AWS Secret Access Key**</mark>](#user-content-fn-3)[^3]<mark style="color:blue;">**,**</mark> and [<mark style="color:blue;">**Region**</mark>](#user-content-fn-4)[^4]<mark style="color:blue;">**.**</mark>

{% hint style="info" %}
**Tip:** To securely connect to your Amazon S3 bucket, ensure that your AWS credentials (Access Key ID and Secret Access Key) are stored securely and never hardcoded in the application. For improved security and access control, it is recommended to use AWS IAM roles and policies.

For more detailed information on connecting and managing access to your S3 bucket, refer to the documentation on [AWS S3 Access and Management](https://docs.aws.amazon.com/AmazonS3/latest/userguide/ways-to-manage-access.html).
{% endhint %}

* From the [<mark style="color:blue;">**Bucket Name**</mark>](#user-content-fn-5)[^5] drop-down box, specify the **bucket name**.

{% hint style="info" %}
**Tip:** Click the **Down Arrow** next to the **Bucket Name** drop-down box to load the bucket names.

![](<../../../../.gitbook/assets/image (1626).png>)
{% endhint %}

B. Click the **Next** button.

<figure><img src="../../../../.gitbook/assets/S (178).png" alt=""><figcaption><p>Configuring Connection Details</p></figcaption></figure>

The Add Metadata section is activated.

</details>

<details>

<summary>4.<strong>Add Metadata</strong></summary>

**Purpose**

While connecting the application to a database, adding **metadata** provides the application with important information about the data it will interact with. This metadata helps the system understand, organize, and manage the data correctly.

**Procedure:**

As part of the procedure, you need to specify catalogue, connectivity mechanism, store, source system, connection type, supporting email ID, and service type. Once done, you need to test by clicking the Test Connection button to check whether everything is correct.

{% hint style="success" %}
**Tip:** To assist with your setup, fields and options shown in blue are equipped with tooltips. Hovering your mouse over these items will reveal a detailed description of their function.
{% endhint %}

**Step-by-Step Instructions:**

The below step-by-step instructions help you understand how to add meta data.

In the **Add Meta Data** section:

* Specify [<mark style="color:blue;">**Catalogue,**</mark>](#user-content-fn-6)[^6] [<mark style="color:blue;">**Business Owner**</mark>](#user-content-fn-7)[^7]**,** and [<mark style="color:blue;">**Technical Owner**</mark>](#user-content-fn-8)[^8]**.**
* From the [<mark style="color:blue;">**Connectivity Mechanism**</mark>](#user-content-fn-9)[^9] options, select [<mark style="color:blue;">**Secured**</mark>](#user-content-fn-10)[^10]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Unsecured**</mark>](#user-content-fn-11)[^11], or [<mark style="color:blue;">**SSH Tunnelling**</mark>](#user-content-fn-12)[^12]**.**
* From the [<mark style="color:blue;">**Store**</mark>](#user-content-fn-13)[^13] options, select either [<mark style="color:blue;">**Is Feature Store**</mark>](#user-content-fn-14)[^14] or [<mark style="color:blue;">**Is Analytical Store**</mark>](#user-content-fn-15)[^15].
* From the [<mark style="color:blue;">**Source System**</mark>](#user-content-fn-16)[^16] drop-down box, select [<mark style="color:blue;">**Internal**</mark>](#user-content-fn-17)[^17] or [<mark style="color:blue;">**Third Party**</mark>](#user-content-fn-18)[^18].
* From the [<mark style="color:blue;">**Connection Type**</mark>](#user-content-fn-19)[^19] drop-down box, select [<mark style="color:blue;">**Access Layer**</mark>](#user-content-fn-20)[^20]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Source System**</mark>](#user-content-fn-21)[^21]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Reference System,**</mark>](#user-content-fn-22)[^22] or [<mark style="color:blue;">**Master Database**</mark>](#user-content-fn-23)[^23]<mark style="color:blue;">**.**</mark>
* In the **Supporting Email ID** field, specify the **supporting email ID** to contact when something goes wrong or when help is needed.
* From the **Service Type** drop-down box, select the **category of service** the data source provides.
* Specify [<mark style="color:blue;">**Service Id**</mark>](#user-content-fn-24)[^24] and [<mark style="color:blue;">**Application Id**</mark>](#user-content-fn-25)[^25]**.**
* Finally, click the **Test Connection** button to check everything is correct.&#x20;

<figure><img src="../../../../.gitbook/assets/S (179).png" alt=""><figcaption><p>Adding Meta Data</p></figcaption></figure>

The **Connection tested successfully** message is displayed.

* Click the **Next** button.

The Discovery section is activated.

</details>

<details>

<summary>5.<strong>Discovery</strong></summary>

**Purpose**

Selecting **Source Tables** tells the system **which specific tables from the source database or application should be extracted and included in the connection setup.** This step defines the exact dataset that will be moved to the target system.

**Procedure**

As part of the table selection step, select the required tables from the left box and move them to the right box in the Discovery section. You can choose a single table, multiple tables, or all tables, as required.

**Step-by-Step Instructions**

The following step-by-step instructions help you understand the process of discovery:

{% hint style="success" %}
**Tip:** In the below mentioned instructions, the field names and their corresponding options are annotated with relevant descriptions. To view the description of a field or an option, simply hover your cursor over it.&#x20;
{% endhint %}

A. In the **Discovery** section, select the **Discovery Settings** choosing from [<mark style="color:blue;">**Identify PII**</mark>](#user-content-fn-26)[^26]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Data Profiling**</mark>](#user-content-fn-27)[^27], and [<mark style="color:blue;">**Data Summary**</mark>](#user-content-fn-28)[^28].

B. Next, click the **Search Storage** filter.

<figure><img src="../../../../.gitbook/assets/S (180).png" alt=""><figcaption><p>Search Storage Filter</p></figcaption></figure>

The Storage dialogue box is displayed.

C. On the **Storage** dialogue box, select the required **file extension**, and then click the **Search** button.

<figure><img src="../../../../.gitbook/assets/S (181).png" alt=""><figcaption><p>Selecting File Extension</p></figcaption></figure>

The Storage dialogue box is extended displaying a group of folders and files.

D. Now, from the **Storage** dialogue box, select the **required folder** or **file.**&#x20;

3. Select the [<mark style="color:blue;">**Delimited Text File**</mark>](#user-content-fn-29)[^29] option choosing from **Comma, Tab, Semicolon, Space, or Other**.
4. Enable the **First row is column header** option if required.
5. Enable the **Skip Row(s)** option if required.

> <mark style="color:red;">**Note:**</mark> When the **Skip Row(s)** option is chosen while selecting a file for migration, the system **ignores (does not import) the specified number of rows from the top of the file** during data extraction.&#x20;
>
> This option is usually needed when the beginning of the file contains Extra header lines, Metadata information, Notes or comments, Blank rows, and Titles or descriptions, etc.

7. Click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (182).png" alt="" width="563"><figcaption><p>Folder Selection for Discovery</p></figcaption></figure>

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

<figure><img src="../../../../.gitbook/assets/S (183).png" alt=""><figcaption><p>Selecting Files for Discovery </p></figcaption></figure>

The files are discovered and the Configuration section is activated.

</details>

<details>

<summary>6<strong>.Configuration</strong></summary>

In the **Configuration** section:&#x20;

* Select the [<mark style="color:blue;">**Owner**</mark>](#user-content-fn-30)[^30] choosing from [<mark style="color:blue;">**Owned**</mark>](#user-content-fn-31)[^31] or [<mark style="color:blue;">**Third Party**</mark>](#user-content-fn-32)[^32].
* Select the [<mark style="color:blue;">**Manage Service**</mark>](#user-content-fn-33)[^33] choosing from [<mark style="color:blue;">**Service Managed**</mark>](#user-content-fn-34)[^34] or [<mark style="color:blue;">**User Managed**</mark>](#user-content-fn-35)[^35].
* Select the **Connection type** choosing from **Secured Connection** or **Unsecured Connection.**
* Specify the [<mark style="color:blue;">**DR**</mark>](#user-content-fn-36)[^36] **availability** and [<mark style="color:blue;">**RBAC**</mark>](#user-content-fn-37)[^37] **implementation** choosing from **Yes** or **No**.
* Click the **Next** button.

<figure><img src="../../../../.gitbook/assets/S (184).png" alt=""><figcaption><p>Configuring Additional Details</p></figcaption></figure>

The Review & Submit section is activated.

</details>

<details>

<summary>7.<strong>Review &#x26; Submit</strong></summary>

* In the **Review & Submit** section, enter a **name** and **description** for the connection, and then click the **Finish** button to submit it.

<figure><img src="../../../../.gitbook/assets/S (185).png" alt=""><figcaption><p>Specifying Connection name and Description</p></figcaption></figure>

The connection is created and the [Connected Data Sources](/broken/pages/dgiZ3ktrQlmTnR2Pq3nV) page is displayed.

</details>

***

## Related Topics

* [**Managing Connected Data Sources**](../../managing-connected-data-sources.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.

[^2]: **AWS Access key** is a unique identifier for an AWS user or service. It is a kind of a **username** for AWS access.

[^3]: **AWS Secret Access Key** is a  confidential key associated with the AWS Access Key. It is a kind of **password** for AWS access.

[^4]: The **Region** refers to the AWS region where your S3 bucket is located.

[^5]: The **Bucket Name** refers to the name of the **S3 bucket** where data is stored. It can be considered as a folder that holds your files.

[^6]: **Catalogue** refers to the group of related data sources.

[^7]: **Business Owner** refers to the person or team responsible for the data from a business point of view.

[^8]: **Technical Owner** refers to the **person or IT team** responsible for the technical side of the data.

[^9]: Connectivity Mechanism refers to the method used to connect to the data source.

[^10]: **Secured** option refers to the connection where data is encrypted, making it safe from hackers and unauthorized access.

[^11]: **Unsecured** option refers to the connection where data is sent without encryption.

[^12]: SSH Tunneling: SSH refers to Secure Shell. SSH is a secure way to connect to another computer or server over a network.

[^13]: This refers to how the data will be used.

[^14]: Select **Is Feature Store** if the data source is used to store and manage machine learning features.

[^15]: Select **Is Analytical Store** if the data source is primarily used for analytics, reporting, and business intelligence.

[^16]: This refers to the original system where the data comes from.

[^17]: An **Internal source system** is owned, managed, and maintained by your organization.

[^18]: A **Third-Party** source system is owned and managed by an external vendor or service provider.

[^19]: This refers to the kind of connection you are using to access the source.

[^20]: The **Access Layer** represents systems that are used to consume or expose data rather than originate it.

[^21]: A **Source System** is the origin of raw or transactional data.

[^22]: A Reference System stores standardized, lookup, or supporting data used across multiple systems.

[^23]: A **Master Database** stores authoritative master data for key business entities.

[^24]: This refers to the unique identifier for the service you are connecting to.

[^25]: This refers to the unique ID used to identify the application that owns, provides, or uses the data.

[^26]: <mark style="color:blue;">**Identify PII (Personally Identifiable Information) detects sensitive data elements that can identify an individual.**</mark>

[^27]: <mark style="color:blue;">**Data Profiling analyzes the structure and content of data to understand its quality and patterns.**</mark>

[^28]: <mark style="color:blue;">**Data Summary provides a high-level overview of the dataset.**</mark>

[^29]: A **Delimited Text File** is a text file where information is separated by a specific character (like comma or tab) so that systems can easily understand and process the data.

[^30]: This refers to **who owns and manages the source system** you are connecting to.

[^31]: **Owned** means the system is **owned and managed by your organization**.

[^32]: **Third Party** means the system is owned and managed by an external vendor or service provider.

[^33]: **Manage Service** refers to who is responsible for managing the connection and its configuration.

[^34]: **Service Managed** means the system automatically manages the service for you.

[^35]: **User Managed** means you manage the service configuration yourself.

[^36]: <mark style="color:blue;">**Disaster Recovery (DR)**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">refers to the processes and systems used to</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**restore applications and data after a failure or disaster.**</mark>

[^37]: **Role-Based Access Control (RBAC)** is a security mechanism that **controls what users can access based on their role**.
