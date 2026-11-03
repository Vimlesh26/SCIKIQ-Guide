---
icon: aws
---

# Storages

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The **Storages** module provides a centralized view of all storage systems configured for archival. It enables you to configure, monitor, review, and manage storage locations used to store archived data. You can add storage configurations, such as **AWS**, and modify or delete existing configurations as required.

***

### Storage Tasks

{% tabs %}
{% tab title="Configure Storage" %}
**Overview**

Setting up AWS S3 for storing archived data provides a scalable, secure, and cost-effective storage solution for long-term data retention. After the AWS S3 set up, data can be archived through a structured pipeline that moves data from the source system to S3 based on defined rules.

***

**Procedure**

The AWS setup configuration process consists of four steps: Basic Configuration, Storage and Data Configuration, Metadata, and Review  Configuration.&#x20;

The expandable panels below guide you through the process.

<details>

<summary><strong>Basic Configuration</strong></summary>

**Overview**

As part of the basic configuration, you need to input **Configuration name, Environment, AWS Access Key, AWS Secret Key, AWS Region,** and **Resource Prefix**.&#x20;

The following step-by-step instructions guide you through the process.

**Procedure**

1. On the **SCIKIQ Left Navigation Bar,** go to **SCIKIQ Archival**.&#x20;
2. Under **SCIKIQ Archival**, expand **Storages** , and then click **Configure Storage**. See the image below:

<figure><img src="../../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

3. The AWS Infrastructure Configuration Wizard page is displayed.
4. In the **Basic Configuration** section, select either an **existing pre-configuration** or c**reate a new one.**

**Selecting an existing configuration**

* From the **Load from Existing AWS Configuration** drop-down box, select an **existing configuration.**

Once the existing configuration is selected, the Configuration name, Environment, Glue Connection, and Description are prepopulated.

**Creating a new configuration**

* In the **Basic Configuration** section, specify **Configuration name, Environment, Glue Connection,** and **Description.**

> <mark style="color:red;">**Note:**</mark> For description of the above fields, refer to the below AWS Basic Configuration – Field Descriptions table.

**AWS Basic Configuration – Field Descriptions**

| **Field**          | **Purpose**                                                                                                                  |
| ------------------ | ---------------------------------------------------------------------------------------------------------------------------- |
| Configuration Name | A unique name to identify and manage the AWS configuration within the system.                                                |
| Environment        | Specifies the deployment context (e.g., Dev, Test, Prod) to separate and manage resources appropriately.                     |
| Glue Connection    | A configured connection used by AWS Glue to securely access and process data from source systems during archival operations. |
| **Description**    | A brief description used to provide additional details or context about the AWS configuration.                               |

<figure><img src="../../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

Once the Basic Configuration is completed, the Storage and Data Configuration section is highlighted.

</details>

<details>

<summary><strong>Storage &#x26; Data Configuration</strong></summary>

**Overview**

The purpose of Storage & Data Configuration is to define how and where archived data will be stored across different storage tiers based on its access frequency and retention needs. It ensures that data is placed in the most appropriate storage class (hot, warm, cold, or archival) to balance performance and cost.

**Procedure**

As part of Storage & Data Configuration, you need to define the a**ccess tiers, including S3 Hot Storage (Frequent Access), S3 Warm Storage (Infrequent Access), S3 Cold Storage (Rare Access), and S3 Archival Storage (Deep Cold).**

The following step-by-step instructions guide you through the process.

Step-by-Step Instructions

**1.Defining S3 Hot Storage (Frequent Access)**

* If you want to select an **existing bucket**, then from the **Select or Create Bucket** drop-down box, select an **existing bucket**.
* If you want to select a new bucket, then from the **Select or Create Bucket** drop-down box, select **Create New**, and then enter the **bucket name** in the **New Bucket Name** field.

<figure><img src="../../../.gitbook/assets/image (53).png" alt=""><figcaption><p>Defining Hot Storage</p></figcaption></figure>

**2.Defining S3 Warm Storage (Infrequent Access)**

* In the **S3 Warm Storage (Infrequent Access)** section, select an **existing bucket** or **create a new one.**
* From the **Storage Class** drop-down box, select the **storage class** choosing from **S3 Standard - 1A or S3 One Zone - 1A.**

{% hint style="info" %}
**Tip:**&#x20;

* **Standard-IA:** Use **Standard-IA** when data is important but rarely accessed
* **One Zone-I:** Use **One Zone-IA** when data is less critical and cost saving is a priority
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (52).png" alt=""><figcaption><p>Defining Warm Storage</p></figcaption></figure>

**3.Defining S3 Cold Storage (Rare Access)**

* In the **S3 Cold Storage (Rare Access)** section, select an **existing bucket** or **create a new one.**
* From the **Storage Class** drop-down box, select **S3 Glacier Instant Retrieval**.

{% hint style="info" %}
**Tip: S3 Glacier Instant Retrieval** is an AWS S3 storage class designed for archival data that is rarely accessed but needs immediate (milliseconds) retrieval when required
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (54).png" alt=""><figcaption><p>Defining S3 Cold Storage (Rare Access)</p></figcaption></figure>

**4.Defining S3 Archival Storage (Deep Cold)**

* In the **S3 Archival Storage (Deep Cold),** section, select an **existing bucket** or **create a new one.**
* From the **Storage Class** drop-down box, select either **S3 Glacier Flexible Retrieval** or **S3 Glacier Deep Archive.**

{% hint style="info" %}
**Tip:**&#x20;

* Use **Flexible Retrieval** when you may need data occasionally
* Use **Deep Archive** when data is rarely needed and cost saving is the top priority
{% endhint %}

* From the **Select Glacier Vault** drop-down box, select either **lse\_glacier\_vault** or **create a new one.**

{% hint style="info" %}
**Tip:** A Glacier Vault is a storage container in Amazon Glacier (legacy archival service) used to store and manage long-term archived data.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (55).png" alt=""><figcaption><p>Defining Deep Cold Storage</p></figcaption></figure>

**5.Defining AWS Glue Data Catalog & ETL**

* In the **AWS Glue Data Catalog & ETL** section, select either an **existing catalogue database or create a new one.**

{% hint style="info" %}
**Tip:**&#x20;

* **Glue Data Catalog** → Stores information about your data
* **Glue ETL** → Moves and transforms your data
* **Catalogue Database** → Organizes metadata tables into logical groups
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (56).png" alt=""><figcaption><p>Defining AWS Glue Data Catalog &#x26; ETL</p></figcaption></figure>

**6.Defining Amazon Athena**

* In the **Amazon Athena** section, enter the **Work Group Name** and **Results Bucket**.

{% hint style="info" %}
**Tip:**

* **Amazon Athena** is a serverless query service that allows you to run SQL queries directly on data stored in Amazon S3—without setting up or managing any database servers.
* A **Workgroup** in Athena is a way to organize and manage query execution.
* The **Results Bucket** is an S3 location where Athena stores the output of queries.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (57).png" alt=""><figcaption><p>Defining Amazon Athena</p></figcaption></figure>

**7.Configuring KMS (Key Management Service)**

* In the **KMS Configuration** section, select the applicable **KMS Key Alias**.

{% hint style="info" %}
Tip:&#x20;

* **KMS Configuration** defines the selection and management of encryption keys in AWS to secure data and control access through centralized key management.
* **KMS key alias** is a user-defined, human-readable name that maps to a KMS key, simplifying key identification and management.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (58).png" alt=""><figcaption><p>Configuring KMS</p></figcaption></figure>

8. Finally, click the **Next** button.
9. The Review Configuration section is highlighted.

</details>

<details>

<summary><strong>Metadata</strong></summary>



</details>

<details>

<summary><strong>Review Configuration</strong></summary>

1. In the **Review Configuration** section, review the configuration, and then click the **Finish** button.

<figure><img src="../../../.gitbook/assets/image (59).png" alt=""><figcaption><p>Review Configuration</p></figcaption></figure>

2. The configuration is saved and displayed on the AWS Infrastructure Management page.

</details>
{% endtab %}

{% tab title="Storage Management" %}
### **Overview**

The **AWS Infrastructure Management** screen provides a centralized view of all saved AWS configurations. It allows you to manage, review, update, and delete existing AWS infrastructure setups used for archival and data processing operations.

Once an AWS configuration is successfully created and saved, it becomes available in this listing page under the **Storage Management** sub-menu.

***

### Procedure

The following steps describe how to access, view, and manage **Storages** from the **Storage Management** screen. This includes navigating to the configuration list, searching for specific entries, and performing actions such as editing or deleting configurations.

<details>

<summary><strong>Access Storage Management</strong></summary>

**Navigate to Storages Management**

1. Click on **Storage Management.**

<figure><img src="../../../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

The **Storage Management** page is displayed.

</details>

<details>

<summary><strong>View Configuration List</strong></summary>

**Overview:**\
This section displays all saved AWS configurations in a structured table format. It helps users quickly identify and manage existing setups.

**Procedure**

The following step-by-step instructions guide you through the process.

1. The system displays the list of saved configurations

<figure><img src="../../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

2. Use the **Search bar** to filter specific records
3. Use **Show entries** to control how many records are displayed per page
4. Key details such as Name, Description, Environment, Updated Date, and Actions are displayed.

<figure><img src="../../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Edit Configuration</strong></summary>

**Overview:**\
This feature allows users to modify an existing AWS configuration without creating a new one. It ensures configurations can be updated based on changing requirements.

**Procedure**

The following step-by-step instructions guide you through the process.

1. In the configuration list, select the required record to update.
2. Click the **Edit (**![](<../../../.gitbook/assets/image (47).png>)**)** icon under the **Actions** column.

<figure><img src="../../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

3. The configuration form opens in editable mode, and a message is displayed indicating that the **configuration loaded successfully.**
4. Update the required fields, such as:
   1. Configuration Name
   2. Environment
   3. Glue Connection
   4. Other AWS-related settings
5. Click **Finish** to save and update the configuration.

<figure><img src="../../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

6. Configuration is update and displayed a success message.

<figure><img src="../../../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Delete Configuration</strong></summary>

**Overview:**\
This feature allows users to permanently remove an AWS configuration from the system when it is no longer required.

**Procedure**

The following step-by-step instructions guide you through the process.

1. Select the required configuration in the list to delete.
2. Click the **Delete (**![](<../../../.gitbook/assets/image (48).png>)**)** icon under the **Actions** column

<figure><img src="../../../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

3. Confirmation dialog is displayed "**Are you sure you want to delete this configuration**
4. Click **Yes** to proceed
5. Configuration is permanently deleted from the list a success message is displayed.

<figure><img src="../../../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

</details>
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Archival Jobs**](../archival-jobs.md)
* [**Compliance**](../compliance/)

