# Configure AWS Setup

**Contents**

* [**Instructions for Using this Page**](configure-aws-setup.md#instructions-for-using-this-page)
* [**Overview**](configure-aws-setup.md#overview)
* [**Procedure**](configure-aws-setup.md#procedure)
* [**Related Topics**](configure-aws-setup.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

Setting up AWS S3 for storing archived data provides a scalable, secure, and cost-effective storage solution for long-term data retention. After the AWS S3 set up, data can be archived through a structured pipeline that moves data from the source system to S3 based on defined rules.

***

## Procedure

The AWS setup configuration process consists of four steps: Basic Configuration, Storage and Data Configuration, Compute Configuration, and Review Compute Configuration.&#x20;

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Basic Configuration</strong></summary>

**Overview**

As part of the basic configuration, you need to input **Configuration name, Environment, AWS Access Key, AWS Secret Key, AWS Region,** and **Resource Prefix**.&#x20;

The following step-by-step instructions guide you through the process.

**Procedure**

1. On the **SCIKIQ Left Navigation Bar,** go to **SCIKIQ Archival**.&#x20;
2. Under **SCIKIQ Archival**, expand **AWS Infra**, and then click **AWS Configuration**. See the image below:

<figure><img src="../../.gitbook/assets/image (224).png" alt="" width="563"><figcaption><p>AWS Configuration Menu Item</p></figcaption></figure>

&#x20;     The AWS Infrastructure Configuration Wizard page is displayed.

3. In the **Basic Configuration** section, select either an **existing pre-configuration** or c**reate a new one.**

**Selecting an existing configuration**

* From the **Load from Existing AWS Configuration** drop-down box, select an **existing configuration.**

Once the existing configuration is selected, the  Configuration name, Environment, AWS Access Key, AWS Secret Key, AWS Region, and Resource Prefix are prepopulated.

**Creating a New configuration**

* In the **Basic Configuration** section, specify **Configuration name, Environment, AWS Access Key, AWS Secret Key, AWS Region,** and **Resource Prefix.**

> <mark style="color:red;">**Note:**</mark> For description of the above fields, refer to the below AWS Basic Configuration – Field Descriptions table.

**AWS Basic Configuration – Field Descriptions**

| **Field**          | **Purpose**                                                                                                                                 |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------- |
| Configuration Name | A unique name to identify and manage the AWS configuration within the system.                                                               |
| Environment        | Specifies the deployment context (e.g., Dev, Test, Prod) to separate and manage resources appropriately.                                    |
| AWS Access Key     | Acts as the public identifier used to authenticate requests to AWS services.                                                                |
| AWS Secret Key     | The private credential paired with the access key, used to securely sign and authorize AWS requests.                                        |
| AWS Region         | Defines the geographic location where data will be stored, helping with performance, latency, and compliance requirements.                  |
| Resource Prefix    | A naming convention added to AWS resources (like S3 buckets or folders) to organize, group, and uniquely identify them across environments. |

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

<figure><img src="../../.gitbook/assets/image (225).png" alt=""><figcaption><p>Defining S3 Hot Storage</p></figcaption></figure>

**2.Defining S3 Warm Storage (Infrequent Access)**

* In the **S3 Warm Storage (Infrequent Access)** section, select an **existing bucket** or **create a new one.**
* From the **Storage Class** drop-down box, select the **storage class** choosing from **S3 Standard - 1A or S3 One Zone - 1A.**

{% hint style="info" %}
**Tip:**&#x20;

* **Standard-IA:** Use **Standard-IA** when data is important but rarely accessed
* **One Zone-I:** Use **One Zone-IA** when data is less critical and cost saving is a priority
{% endhint %}

<figure><img src="../../.gitbook/assets/image (226).png" alt=""><figcaption><p>Defining Warm Storage</p></figcaption></figure>

**3.Defining S3 Cold Storage (Rare Access)**

* In the **S3 Cold Storage (Rare Access)** section, select an **existing bucket** or **create a new one.**
* From the **Storage Class** drop-down box, select **S3 Glacier Instant Retrieval**.

{% hint style="info" %}
**Tip: S3 Glacier Instant Retrieval** is an AWS S3 storage class designed for archival data that is rarely accessed but needs immediate (milliseconds) retrieval when required
{% endhint %}

<figure><img src="../../.gitbook/assets/image (227).png" alt=""><figcaption><p>Defining S3 Cold Storage (Rare Access)</p></figcaption></figure>

**4.Defining S3 Archival Storage (Deep Cold)**

* In the  **S3 Archival Storage (Deep Cold),** section, select an **existing bucket** or **create a new one.**
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

<figure><img src="../../.gitbook/assets/image (228).png" alt=""><figcaption><p>Defining Deep Cold Storage</p></figcaption></figure>

**5.Defining AWS Glue Data Catalog & ETL**

* In the **AWS Glue Data Catalog & ETL** section, select either an **existing catalogue database or create a new one.**

{% hint style="info" %}
**Tip:**&#x20;

* **Glue Data Catalog** → Stores information about your data
* **Glue ETL** → Moves and transforms your data
* **Catalogue Database** → Organizes metadata tables into logical groups
{% endhint %}

<figure><img src="../../.gitbook/assets/image (229).png" alt=""><figcaption><p>Defining AWS Glue Data Catalog &#x26; ETL</p></figcaption></figure>

**6.Defining Amazon Athena**

* In the **Amazon Athena** section, enter the **Work Group Name** and **Results Bucket**.

{% hint style="info" %}
**Tip:**

* **Amazon Athena** is a serverless query service that allows you to run SQL queries directly on data stored in Amazon S3—without setting up or managing any database servers.
* A **Workgroup** in Athena is a way to organize and manage query execution.
* The **Results Bucket** is an S3 location where Athena stores the output of queries.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (230).png" alt=""><figcaption><p>Defining Amazon Athena</p></figcaption></figure>

**7.Configuring KMS (Key Management Service)**

* In the **KMS Configuration** section, select the applicable **KMS Key Alias**.

{% hint style="info" %}
Tip:&#x20;

* **KMS Configuration** defines the selection and management of encryption keys in AWS to secure data and control access through centralized key management.
* **KMS key alias** is a user-defined, human-readable name that maps to a KMS key, simplifying key identification and management.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (231).png" alt=""><figcaption><p>Configuring KMS</p></figcaption></figure>

8. Finally, click the **Next** button.

The Review Configuration section is highlighted.

</details>

<details>

<summary><strong>3.Review Configuration</strong></summary>

* In the **Review Configuration** section, review the configuration, and then click the **Finish** button.

<figure><img src="../../.gitbook/assets/image (232).png" alt=""><figcaption><p>Review Configuration</p></figcaption></figure>

The configuration is saved and displayed on the AWS Infrastructure Management page.

</details>

***

## Related Topics

* [Connect SCIKIQ to Source Database](/broken/pages/1miPFvCEFxfy7uZat3C4)
* [Configure Table Classification](/broken/pages/fy1vjHIN7Nys8uAuddaO)
* [Create Compliance Framework](/broken/pages/J0o8JvIQ5NXn822xZNDA)
* [Create Compliance Policy](/broken/pages/5gBXOCk95Uv7C11YfBLO)
* [Configure AWS Setup](/broken/pages/26PZ6KCui7ZjC3abzdND)
* [Create Archival Job](/broken/pages/54s7haLhTK625sePPPzh)
* [Setup Deployment Platform](/broken/pages/qpdRebf35FBbmvMZlRTo)
* [Deploy Archival Job](/broken/pages/hEN0BpaQWg865JKIDrtG)
* [Manage Deployment Configurations](/broken/pages/ctJKSQVRrDMRLHYUvlWy)
* [Validate Archived Data](/broken/pages/RWHaxNCgJded7Q8xd9FP)
* [View Archived Data](/broken/pages/6xWaChqxS1moikwvFJk7)
* [Delete Archived Data](/broken/pages/oXzQfmDzcrDAFOL2TO5w)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
