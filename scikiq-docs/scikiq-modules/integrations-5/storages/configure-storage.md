---
hidden: true
icon: database
---

# Configure Storage

***

**Contents**

* [**Instructions for Using this Page**](configure-storage.md#instructions-for-using-this-page)
* [**Overview**](configure-storage.md#overview)
* [**Procedure**](configure-storage.md#procedure)
* [**Related Topics**](configure-storage.md#related-topics)

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

Setting up AWS S3 for storing archived data provides a scalable, secure, and cost-effective storage solution for long-term data retention. After the AWS S3 set up, data can be archived through a structured pipeline that moves data from the source system to S3 based on defined rules.

***

### Procedure

The AWS setup configuration process consists of four steps: Basic Configuration, Storage and Data Configuration, Compute Configuration, and Review Compute Configuration.&#x20;

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Basic Configuration</strong></summary>

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

<summary><strong>2.Storage &#x26; Data Configuration</strong></summary>

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

<summary><strong>3.Review Configuration</strong></summary>

1. In the **Review Configuration** section, review the configuration, and then click the **Finish** button.

<figure><img src="../../../.gitbook/assets/image (59).png" alt=""><figcaption><p>Review Configuration</p></figcaption></figure>

2. The configuration is saved and displayed on the AWS Infrastructure Management page.

</details>

***

### Related Topics

* [**Connect SCIKIQ to Source Database**](/broken/pages/NQamWuz7vUgQ2NLWzOdj)
* [**Configure Table Classification**](../../integrations/vs-meta-data-manager/table-classification.md)
* [**Create Compliance Framework**](../compliance/regulatory-compliance.md)
* [**Create Compliance Policy**](../compliance/compliance-policies.md)
* [**Configure AWS Setup**](configure-storage.md)
* [**Create Archival Job**](../archival-jobs-2/creating-a-table-archival-job.md)
* [**Setup Deployment Platform**](../archival-jobs-2/deployment-configs.md)
* [**Deploy Archival Job**](/broken/pages/Lhd7keqyZR2EfkoA5qpT#id-2.deploy-archival-job)
* [**Manage Deployment Configurations**](../archival-jobs-2/deployment-configs.md#manage-deployment-configurations)
* [**Validate Archived Data**](../archival-jobs-2/retrieve-data.md#validate-archived-data)
* [**View Archived Data**](../archival-jobs-2/retrieve-data.md)
* [**Delete Archived Data**](../archival-jobs-2/deletion-jobs.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
