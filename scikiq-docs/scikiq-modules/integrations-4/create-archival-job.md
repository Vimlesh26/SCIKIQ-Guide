# Create Archival Job

***

**Contents**

* [**Instructions for Using this Page**](create-archival-job.md#instructions-for-using-this-page)
* [**Overview**](create-archival-job.md#overview)
* [**Procedure**](create-archival-job.md#procedure)
* [**Related Topics**](create-archival-job.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

Creating an archival job is to automate the process of moving inactive or historical data from primary systems to long-term storage. It helps improve application performance by reducing the load on active databases. An archival job ensures that data is stored securely while meeting compliance and retention requirements.

***

## Procedure

The process involves a series of sequential steps, which includes Setup Data Source, Define Data Selection, Select Compliance Policy, Enable PII Detection, Setup Partitioning, Apply Data Filters, Define Retention Schedule, POD Management, and Review & Save.&#x20;

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Setup</strong> <strong>Data Source</strong></summary>

**Overview**

As part of selecting the Data Source, you need to select **Data Source Type, Connection,** and **Tables.** The purpose of selecting these is to clearly define what data to archive and from where. Each element plays a specific role.

**Procedure**

The following step-by-step instructions guide you through the process.

**Step-by-Step Instructions**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival.**&#x20;
2. Under S**CIKIQ Archival,** expand **Archival Jobs**, and then click **Configuration Wizard**.

<figure><img src="../../.gitbook/assets/image (238).png" alt=""><figcaption><p>Configuration Wizard Menu Item</p></figcaption></figure>

The **Archival Configuration** page is displayed.

3. On the **Archival Configuration** page, in the **Data Source** section:

A. From the **Source Type** drop-down box, select the **data source**. For example, ORACEL-EBS.

{% hint style="info" %}
**Tip:** Selecting the **data source** identifies the type of system from which the data will be archived.
{% endhint %}

B. From the **Connection** drop-down box, select the applicable **connection.** For example, ORACEL-EBS.

{% hint style="info" %}
**Tip:** Selecting the connection defines the actual link to the data source.
{% endhint %}

C. From the **Selected Tables** list, select the required **tables**.

{% hint style="info" %}
**Tip:**  Selecting the tables specifies the tables that are to be archived.
{% endhint %}

4. Click the **Next** button.

<figure><img src="../../.gitbook/assets/image (239).png" alt=""><figcaption><p>Selecting Data Source </p></figcaption></figure>

The Data Selection section is highlighted.&#x20;

</details>

<details>

<summary><strong>2.Define Data Selectio</strong>n</summary>

**Overview**

As part of data selection, data profiling is performed. Data profiling is the process of analyzing data to understand its structure, quality, and content before it is used, migrated, or archived.

SCIKIQ performs data profiling by:

* Scanning tables automatically
* Generating profiling reports
* Highlighting data quality issues

**Procedure**

The below instructions guide you through the process:

**Step-by-Step Instructions**

1. On the **Data Selection** page, click **each table** to perform data profiling.
2. After completion of data profiling, click the **Next** button.

<figure><img src="../../.gitbook/assets/image (240).png" alt=""><figcaption><p>Data Profiling</p></figcaption></figure>

&#x20;   The Compliance section is highlighted.

</details>

<details>

<summary><strong>3.Select Compliance Policy</strong></summary>

**Overview**

The purpose of selecting a compliance policy while creating an archival job is to ensure that the archived data adheres to legal, regulatory, and organizational requirements.&#x20;

The compliance policy defines rules such as Data retention period, Data Security, Access Control, Audit Logging, Data Privacy, and Incident Response.

**Procedure**

The following step-by-step instructions guide you through the process.

**Step-by-Step Instructions**

1. In the **Compliance** section, select the required **policy** from the **Compliance Policy** drop-down to apply compliance rules to the first table.

The selected compliance policy details appear below.&#x20;

2. If you want to apply **same compliance policy** to all tables, then select ![](<../../.gitbook/assets/unknown (36).png>)to  apply the same compliance policy to all tables.

The selected compliance policy details appear below.

3. If not, select the required table, and then select the required policy from the **Compliance Policy** drop-down box.
4. Finally, click the **Next** button.

<figure><img src="../../.gitbook/assets/image (241).png" alt=""><figcaption><p>Compliance Section</p></figcaption></figure>

The PII Detection section is displayed.&#x20;

</details>

<details>

<summary><strong>4.Enable PII Detection</strong></summary>

**Overview**

PII Detection is the process of identifying personally identifiable information within data to ensure it is securely handled and compliant with regulations. PII detection scans data (tables, files, databases) to:

* Locate sensitive personal information
* Classify it appropriately
* Enable security and compliance actions

**Procedure**

As part of enabling PII Detection, you need to:

* **Define protection settings** to establish how sensitive data should be handled and protected.
* **Identify PII patterns** through scanning to automatically detect sensitive data within tables or datasets.
* **Specify appropriate masking methods** to define how the identified sensitive data should be protected or hidden.

The following sections explain how to configure each of these.

**Define Protection Settings**

1. On the **PII Detection** page, click the **PII Protection Settings** button.

<figure><img src="../../.gitbook/assets/image (242).png" alt=""><figcaption><p>PII Protection Page</p></figcaption></figure>

The PII Protection Settings screen is displayed.

2. On the **PII Protection Settings** screen, select the **Enable PI** checkbox.
3. From the **Detection Patterns** List, select the **required patterns.**&#x20;
4. From the **Masking Method** drop- down box, select the applicable **masking method**.&#x20;

<figure><img src="../../.gitbook/assets/image (243).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Tip:** Refer to the below table for the description of masking methods:
{% endhint %}

&#x20;                                                     **Masking Methods Description**

| Field                     | Purpose                                                                    | Example                                             | Purpose                                                                        |
| ------------------------- | -------------------------------------------------------------------------- | --------------------------------------------------- | ------------------------------------------------------------------------------ |
| Partial Masking (Default) | Only a portion of the data is hidden, while the rest remains visible       | 98XXXX3210                                          | Allows partial visibility for identification while protecting sensitive parts. |
| Full Redaction            | Completely hides the data                                                  | \*\*\*\*\*\*\*\*\*\*6                               | Maximum security when data should not be visible at all.                       |
| Masking Character         | Replaces the data with a specific character (like \*, X, or #)             | john.doe@email.com → \*\*\*\*\*\*\*\*\*\*\*\*\*\*\* | Simple and consistent masking format.                                          |
| Custom Pattern            | Applies a user-defined masking format                                      | Shows first 2 and last 2 characters → ABXXXXYZ      | Flexible masking based on business requirements.                               |
| Hashing                   | Converts data into a fixed-length encrypted value (non-reversible)         | password → 5f4dcc3b5aa765d61d8327deb882cf99         | Secure storage where original data cannot be retrieved.                        |
| Encryption                | Transforms data into an unreadable format that can be decrypted with a key | 12345 → Encrypted text                              | Secure storage with the ability to restore original data when needed.          |
| Tokenization              | Replaces sensitive data with a non-sensitive placeholder (token)           | 1234-5678-9012-3456 → TKN-982734                    | Keeps original data safe while allowing reference via tokens.                  |

3. Finally, click the **OK** button.

The PII protection settings are defined.

**Identify PII patterns**&#x20;

* On the **PII Detection** page, select the **Table**, and then click the **Scan for PII Patterns** button.

<figure><img src="../../.gitbook/assets/image (244).png" alt=""><figcaption><p>PII Detection Page</p></figcaption></figure>

The detected PII patterns are displayed. See the below image.

<figure><img src="../../.gitbook/assets/image (245).png" alt=""><figcaption><p>Detected PII Patterns </p></figcaption></figure>

**Specify Masking Methods**

1. On the **PII Detection** page, from the **Masking Method** drop-down box, select the required **masking method**.
2. Follow the same procedure for all the detected patterns.
3. Apply the same procedure for all the tables.
4. Click the **Next** button.

<figure><img src="../../.gitbook/assets/image (246).png" alt=""><figcaption><p>Making Methods</p></figcaption></figure>

The partitioning section is highlighted.

</details>

<details>

<summary><strong>5.Setup Partitioning</strong></summary>

**Overview**

Partitioning is the process of dividing data into smaller segments based on defined criteria, enabling efficient storage across different tiers and optimizing performance, cost, and lifecycle management.&#x20;

As part of partitioning, you need to specify Partitioning method, Configuration Parameters, Hot Storage Settings, Warm Storage Settings, Cold Storage settings, and Deep Archive Storage Settings.

&#x20;**Procedure**

The step-by-step instructions below help you understand the partitioning process.

1. **Select Partitioning method**&#x20;

* On the **Partitioning** page, select **Date Based** or **Range Based** to choose the partitioning method.

{% hint style="info" %}
Tip:&#x20;

**Tip: Here is the description for partitioning methods:**

* **Date-Based Partitioning:** Divides data based on time intervals such as day, month, or year.
* **Range-Based Partitioning:** Divides data into partitions based on defined value ranges of a column.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (247).png" alt=""><figcaption><p>Partitioning Page</p></figcaption></figure>

2. **Select Configuration Parameters**

* From the **AWS Storage Configuration** drop-down box, select the **AWS Config**, which you have already created.
* From the **Partition Column** drop-down box, select the **required partition column**.

{% hint style="info" %}
**Tip: Here is the description for AWS Configuration parameters:**

* AWS Storage Configuration: Defines the storage location and tiering strategy for archived data in AWS.
* Partition Column: Specifies the column used to divide data into partitions for efficient storage and processing.
{% endhint %}

> <mark style="color:red;">**Note:**</mark> Make sure to select the Configuration Parameters for all the tables.

<figure><img src="../../.gitbook/assets/image (248).png" alt=""><figcaption><p>Partitioning Method - Configuration Parameters</p></figcaption></figure>

The selected AWS Storage Configuration Details appear on the Partitioning page.

3. **Define Hot Storage Settings**

> <mark style="color:red;">**Note:**</mark> You can use the Hot Storage for frequently accessed and critical data that requires fast retrieval. For example, Current year transactions, Frequently accessed customer data, etc.

1. In the **Hot Storage Settings** section, select the **Enable Hot Storage** checkbox.
2. Specify the **From Date, To Date,** and **Retention Period.**

<figure><img src="../../.gitbook/assets/image (249).png" alt=""><figcaption><p>Hot Storage Settings</p></figcaption></figure>

4. **Define Warm Storage Settings**

> <mark style="color:red;">**Note:**</mark> You can use the Warm Storage for moderately accessed data that is not needed instantly but still accessed occasionally. For example, Data from the last 6–12 months, Periodic reporting data, etc.

1. In the **Warm Storage Settings** section, select the **Warm Storage** checkbox.
2. Specify the **From Date, To Date,** and **Retention Period.**

<figure><img src="../../.gitbook/assets/image (250).png" alt=""><figcaption><p>Warm Storage Settings</p></figcaption></figure>

5. **Define Cold Storage Settings**

> <mark style="color:red;">**Note:**</mark> You can use the Cold Storage to store rarely accessed data for long-term retention. For example, Data older than 1–3 years, Audit or compliance records, etc.

1. In the **Cold Storage Settings** section, select the **Cold Storage** checkbox.
2. Specify the **From Date, To Date**, and **Retention Period**.

<figure><img src="../../.gitbook/assets/image (251).png" alt=""><figcaption><p>Cold Storage Settings</p></figcaption></figure>

6. **Define Deep Archive Storage Settings**

> <mark style="color:red;">**Note:**</mark> You can use the  Deep Archive Storage to store rarely accessed data for long-term retention. For example, Data older than 1–3 years, Audit or compliance records, etc.

1. In the  **Deep Archive Storage Settings** section, select the  **Deep Archive Storage checkbox**.
2. Specify the **From Date, To Date,** and **Retention Period.**

<figure><img src="../../.gitbook/assets/image (252).png" alt=""><figcaption><p>Deep Archive Storage Settings</p></figcaption></figure>

3. After completing all the configuration, finally, click the N**ext** button.

</details>

<details>

<summary><strong>6.Apply Data Filters</strong></summary>

**Overview**

As part of defining conditions, you need to configure Date-based filtering, which is used to select specific data for archiving based on a date or time condition. You can use the Quick Presets to specify the date ranges.

**Procedure**

The step-by-step instructions below help you understand the process of configuring date-based filtering.

1. From the **Date Column** drop-down box, select the required **column**.
2. From the **Quick Presets**, select the **required quick preset** choosing from L**ast 30 days, Last 90 days, Last 6 Months, Last Year,** and **Custom Range.**  For example, Last 6 Months.

> <mark style="color:red;">**Note:**</mark> Quick Presets are shortcut options that allow you to select commonly used date ranges quickly and accurately. Once a Quick Preset is selected, the Start Date and End Date fields are populated automatically.
>
> For example, if you want to archive data for the last 6 months, simply select the “Last 6 Months” Quick Preset. Alternatively, you can use the “Custom Range” Quick Preset to manually specify the required date range.

3. Finally, click the **Next** button. See the below image.

<figure><img src="../../.gitbook/assets/image (253).png" alt=""><figcaption><p>Date Range Filters</p></figcaption></figure>

</details>

<details>

<summary><strong>7.Define Retention Schedule</strong></summary>

**Overview**

The purpose of configuring a retention schedule for automated data archival enforcement is to define how long data should be retained and to ensure that archival (and eventual deletion, if applicable) happens automatically based on predefined rules.

For example, if a retention schedule is set to 12 months, any data older than 12 months will be automatically archived as per the defined schedule—without needing manual action.

**Procedure**

The step-by-step instructions below help you understand the process of  configuring a retention schedule.

1. On the **Retention Job Schedule** page, select the **table**.

&#x20;     The selected table name is populated in the Schedule Name field.

2. From the **Schedule Type** drop-down box, select the **required schedule type** choosing from **Daily, Weekly,** or **Monthly.** For example, Daily.&#x20;
3. In the **Description** field, enter an **appropriate description** for the retention schedule.
4. In the **Schedule Time** field, specify the schedule time by clicking the **Show Time Picker** ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAXCAYAAAALHW+jAAACGklEQVR4AexTO2tqQRD+SIqQQEgRkjRiY2trZWEh2IggKoqF+AA7C0UtBAXBShEtfSAogliICoKg2AlW/gsRRUEQfOLr3jsL58Tjg9uku/fA7M5+8+13Zmd2H3798PeAH/7+C34XdLFYoFKpwOfzQa1Ww+/3o1qtYrVafZNueDdrWCwWIRKJYLfbcTqdIJPJcDweYbPZIBaLmfANLQZdCVJWVqsVwWAQ0+kUiUQC4XCYzZPJBB6PBwaDAZ1OhwlcDgLB2WwGp9PJxOiILy8vmM/nSKfTbB+t6Uculwv00+12y/DzQSBYKBTw/v7OMuJI54IcFo/HsdvtUKvVOIifBYK9Xg8ajQaPj4884Zbz9PQElUqFbrd7FRYILpdLvL6+XpHW6zUOh4MAp+YMBgMBRguB4NfXF0ajEeG8EaZUKiGVSlEul/Hn6bPYeDzG5+cn888HgaBcLke73cZ+v+c5z8/PSKVSaDabaDQayOfz2Gw2aLVaUCgUPI9zBIJmsxnUuVAoxMX5WSKRsAwdDgfcbjers8lk4uOcIxB8e3tDJpNBNBpFLBZjmXBEmqnGgUAA2WwWdCPoGhF+bgJBCuj1etBLiUQioPp5vV52jejufXx8IJfLoV6vsy4T/9IeLgFaWywWDIdDtpmeXr/fB2VTKpVAndVqtUS7aTcFiUnHNxqNSCaTrCFUAp1OB2oSxe/ZXcF7G/6G/4OCvwEAAP//9KQKeQAAAAZJREFUAwCc7BLu3kqjGgAAAABJRU5ErkJggg==) icon.
5. In the **Notify on Failure** field, enter the **email IDs** of the recipients who should be notified in the event of a failure. You can enter multiple email IDs separated by commas.
6. Finally, click the **Next** button.

<figure><img src="../../.gitbook/assets/image (254).png" alt=""><figcaption><p>Retention Job Schedule Page</p></figcaption></figure>

The POD Management section is highlighted.

</details>

<details>

<summary>8<strong>.POD Management</strong></summary>

**Overview**

While creating an archival job, the purpose of a POD (in Kubernetes) is to act as the execution unit where the archival process runs. A POD contains one or more containers that perform tasks such as data extraction, transformation, and movement to archival storage.

**Procedure**

The step-by-step instructions below help you understand the process.

1. On the **POD Management** section, from the **Deployment Configuration** drop-down box, select **Kubernetes**.

<figure><img src="../../.gitbook/assets/image (255).png" alt=""><figcaption><p>POD Management - Selecting Deployment Configuration</p></figcaption></figure>

2. After selecting the deployment configuration, click **Add Pod**.
3. Drag table from left panel to the right panel to add it to the pod.

<figure><img src="../../.gitbook/assets/image (256).png" alt=""><figcaption><p>POD Management - Add Pod</p></figcaption></figure>

The Review & Save section is highlighted.

</details>

<details>

<summary>9<strong>.Review &#x26; Save</strong></summary>

**4.7.2.8.1. Overview**

The purpose of reviewing and saving an archival job after completing all configurations is to validate the setup and securely store it so the job can be executed accurately and consistently.

**4.7.2.6.2. Procedure**

The below step-by-step instructions guide you through the procedure.

1. On the **Review & Save** page, click each **table,** and review the configuration.
2. In the **Configuration Name** field, enter a **name** for the archival job.
3. In the **Description** field, enter a **description** relevant to the archival job.
4. Click the **Finish** button.

<figure><img src="../../.gitbook/assets/image (257).png" alt=""><figcaption><p>Review &#x26; Save Page</p></figcaption></figure>

The configuration is saved and displayed on the Archival Configuration List page. See the below image.

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
