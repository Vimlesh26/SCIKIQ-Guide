---
hidden: true
icon: page
---

# Archival Jobs

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page contains detailed information about different modules of Archival including Create Archival Jobs, Existing Jobs, Retrive Data, Deployment Configs, Deletion Jobs, Retention Schedules, Archival Dashboard, Cube Manager, and Cube Manager all under different tabs.

The **Archival** module enables you to create archival jobs that automatically move inactive or historical data from primary systems to long-term storage. After creating an archival job, you can view reconciliation reports, retrieve or delete archived data as needed, and deploy and manage archival configurations. This helps ensure efficient and compliant management of archived data throughout its lifecycle.

***

### Archival Jobs

{% tabs %}
{% tab title="Prerequisites" %}
The following are the prerequisites for configuring SCIKIQ Archival:

<table><thead><tr><th valign="top">System Requirements</th><th valign="top">Cloud Requirements</th></tr></thead><tbody><tr><td valign="top"><ul><li>Active access to the SCIKIQ platform</li><li>Administrative privileges</li><li>Valid database connection details</li><li>Network connectivity between SCIKIQ and AWS</li></ul></td><td valign="top"><p>An AWS account enables with the following services:</p><ul><li>Amazon S3</li><li>IAM Roles</li><li>CloudWatch Monitoring</li><li>Lifecycle Policies</li></ul></td></tr><tr><td valign="top"></td><td valign="top"></td></tr></tbody></table>
{% endtab %}

{% tab title="Create Archival Job" %}
**Overview**

Creating an archival job is to automate the process of moving inactive or historical data from primary systems to long-term storage. It helps improve application performance by reducing the load on active databases. An archival job ensures that data is stored securely while meeting compliance and retention requirements.

***

**Procedure**

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
2. Under S**CIKIQ Archival,** expand **Archival Jobs**, and then click **Create Archival Job**.

<figure><img src="../../.gitbook/assets/image (1631).png" alt=""><figcaption></figcaption></figure>

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

C. From the **Module** drop-down box, select the applicable module. For example, _AR – Accounts Receivable_. Click on **Load Tables.**

{% hint style="info" %}
**Tip:** Selecting the module ensures that the archival process is scoped to the relevant business area.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (1657).png" alt=""><figcaption></figcaption></figure>

D. From the **Selected Tables** list, select the required **tables**.

{% hint style="info" %}
**Tip:**  Selecting the tables specifies the tables that are to be archived.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (1659).png" alt=""><figcaption></figcaption></figure>

**a. Table Selection and Grouping for Archival**

1. To begin, clicking on the **Advanced Search** button to search table by name.

<figure><img src="../../.gitbook/assets/image (1661).png" alt=""><figcaption></figcaption></figure>

2. Provide the name of the table you want to search for. For example, enter a table name like **“BANK”** in the search field.
3. If matching text is found, the system will display all relevant tables associated with your search term.

<figure><img src="../../.gitbook/assets/image (1663).png" alt=""><figcaption></figcaption></figure>

4. The matching tables (e.g., all tables related to “BANK”) will then be appended to the existing table list.

<figure><img src="../../.gitbook/assets/image (1664).png" alt=""><figcaption></figcaption></figure>

**b. Managing Table Groups**

1. Click on **“Add Row”** to create multiple groups.
2. Each group allows you to organize and assign different tables as needed.
3. Click on **Add Row.**

<figure><img src="../../.gitbook/assets/image (1668).png" alt=""><figcaption></figcaption></figure>

**c. Assigning Modules**

1. You can assign selected tables to specific groups based on different modules.
2. Choose the desired module from the dropdown menu available for each group.

<figure><img src="../../.gitbook/assets/image (1666).png" alt=""><figcaption></figcaption></figure>

**d. Archival Flexibility**

* The system supports archiving tables across multiple modules within a single archival job.
* This allows you to efficiently manage and process data from different modules together.

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

1. In the **Profiling** column, click the toggle or action icon

<figure><img src="../../.gitbook/assets/image (1636).png" alt=""><figcaption></figcaption></figure>

2. On the **Data Selection** page, click **each table** to perform data profiling.

<figure><img src="../../.gitbook/assets/image (1638).png" alt=""><figcaption></figcaption></figure>

3. After completion of data profiling, click the **Close** button.

<figure><img src="../../.gitbook/assets/image (1639).png" alt=""><figcaption></figcaption></figure>

&#x20;  4\. The Compliance columns is highlighted.

</details>

<details>

<summary><strong>3.Select Compliance Policy</strong></summary>

**Overview**

The purpose of selecting a compliance policy while creating an archival job is to ensure that the archived data adheres to legal, regulatory, and organizational requirements.&#x20;

The compliance policy defines rules such as Data retention period, Data Security, Access Control, Audit Logging, Data Privacy, and Incident Response.

**Procedure**

The following step-by-step instructions guide you through the process.

**Step-by-Step Instructions**

1.  In the **Compliance** column, click the action option.



    <figure><img src="../../.gitbook/assets/image (1633).png" alt=""><figcaption></figcaption></figure>


2. select the required **policy** from the **Compliance Policy** drop-down to apply compliance rules to the first table.

The selected compliance policy details appear below.&#x20;

2. If you want to apply **same compliance policy** to all tables, then select ![](<../../.gitbook/assets/unknown (36).png>)to apply the same compliance policy to all tables.

The selected compliance policy details appear below.

3.  If not, select the required table, and then select the required policy from the **Compliance Policy** drop-down box.



    <figure><img src="../../.gitbook/assets/image (1641).png" alt=""><figcaption></figcaption></figure>
4. Finally, click the **Save** button.

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

**a. Define Protection Settings**

1.  In the **PII Detection** column, click the action option.



    <figure><img src="../../.gitbook/assets/image (1642).png" alt=""><figcaption></figcaption></figure>
2.  On the **PII Detection** page, click the **PII Protection Settings** button.



    <figure><img src="../../.gitbook/assets/image (1643).png" alt=""><figcaption></figcaption></figure>

The PII Protection Settings screen is displayed.

1. On the **PII Protection Settings** screen, select the **Enable PI** checkbox.
2. From the **Detection Patterns** List, select the **required patterns.**&#x20;
3. From the **Masking Method** drop- down box, select the applicable **masking method**.&#x20;

<figure><img src="../../.gitbook/assets/image (1644).png" alt=""><figcaption></figcaption></figure>

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

4. Finally, click the **OK** button.
5. The PII protection settings are defined.

**b. Identify PII patterns**&#x20;

1. On the **PII Detection** page, select the **Table**, and then click the **Scan for PII Patterns** button.

<figure><img src="../../.gitbook/assets/image (1645).png" alt=""><figcaption></figcaption></figure>

2. The detected PII patterns are displayed. See the below image.

<figure><img src="../../.gitbook/assets/image (1646).png" alt=""><figcaption></figcaption></figure>

**c. Specify Masking Methods**

1. On the **PII Detection** page, from the **Masking Method** drop-down box, select the required **masking method**.
2. Follow the same procedure for all the detected patterns.
3. Apply the same procedure for all the tables.
4. Click the **Save** button.

<figure><img src="../../.gitbook/assets/image (1647).png" alt=""><figcaption></figcaption></figure>

5. The partitioning column is highlighted.

</details>

<details>

<summary><strong>5. Set Storage Configuration</strong></summary>

**Overview**

The **Set Storage Configuration** step allows you to define how and where the data will be stored in AWS. It includes selecting the storage configuration and specifying the partitioning column to optimize data storage and retrieval.

&#x20;**Procedure**

The step-by-step instructions below help you understand the partitioning process.

1. In the **Storage Config** column, click the action option.

<figure><img src="../../.gitbook/assets/image (1648).png" alt=""><figcaption></figcaption></figure>

**a. Select Partitioning method**&#x20;

1. On the **Partitioning** page, select **Date Based** or **Range Based** to choose the partitioning method.

{% hint style="info" %}
Tip:&#x20;

**Tip: Here is the description for partitioning methods:**

* **Date-Based Partitioning:** Divides data based on time intervals such as day, month, or year.
* **Range-Based Partitioning:** Divides data into partitions based on defined value ranges of a column.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (1649).png" alt=""><figcaption></figcaption></figure>

**b. Select Configuration Parameters**

1. From the **AWS Storage Configuration** drop-down box, select the **AWS Config**, which you have already created.
2. From the **Partition Column** drop-down box, select the **required partition column**.
3. If you want to apply **same AWS config for al**l to all tables, then select ![](<../../.gitbook/assets/image (1652).png>)to apply the same **AWS Config** to all tables.

{% hint style="info" %}
**Tip: Here is the description for AWS Configuration parameters:**

* AWS Storage Configuration: Defines the storage location and tiering strategy for archived data in AWS.
* Partition Column: Specifies the column used to divide data into partitions for efficient storage and processing.
{% endhint %}

> <mark style="color:red;">**Note:**</mark> Make sure to select the Configuration Parameters for all the tables.

<figure><img src="../../.gitbook/assets/image (1650).png" alt=""><figcaption></figcaption></figure>

4. Click on **Save** button.&#x20;

</details>

<details>

<summary>6<strong>.Setup Partitioning</strong></summary>

**Overview**

Partitioning is the process of dividing data into smaller segments based on defined criteria, enabling efficient storage across different tiers and optimizing performance, cost, and lifecycle management.&#x20;

As part of partitioning, you need to specify Partitioning method, Configuration Parameters, Hot Storage Settings, Warm Storage Settings, Cold Storage settings, and Deep Archive Storage Settings.

Partitioning range can be defined at two levels:

* **Global Level** – Applies the same date range across all tables and storage tiers
* **Table Level** – Allows defining a specific date range for an individual table

This flexibility helps in managing data efficiently based on business and storage requirements.

&#x20;**Procedure**

The step-by-step instructions below help you understand the partitioning process.

**a. Configure Global Partitioning Range**

1. At the **top of the page**, locate the **Global Date Partitioning** option.

<figure><img src="../../.gitbook/assets/image (1669).png" alt=""><figcaption></figcaption></figure>

2. Select the required **Storage Tier** (Hot, Warm, Cold, Deep Archive).
   1. Enter the **Date Range**:
   2. Specify the **Start Date**
   3. Specify the **End Date**
3. Click **Apply**.&#x20;
   1. Confirmation message: **“Applied: \[Start Date] to \[End Date] across all tables."**

<figure><img src="../../.gitbook/assets/image (1670).png" alt=""><figcaption></figcaption></figure>

**b. Configure Table-Level Partitioning Range**

1. In the **Partitioning** column, click the **Action** option.

<figure><img src="../../.gitbook/assets/image (1654).png" alt=""><figcaption></figcaption></figure>

2. A list of all **selected tables** will appear in a **drop-down selection list**.
3. From this list, you can:
   1. View all selected tables
4. The selected tables details appear below.&#x20;
   1. If you want to apply **same date ranges** to all tables, then select to ![](<../../.gitbook/assets/image (1677).png>)  apply the same date ranges to all tables.

<figure><img src="../../.gitbook/assets/image (1676).png" alt=""><figcaption></figcaption></figure>

**c. Define Hot Storage Settings**

> <mark style="color:red;">**Note:**</mark> You can use the Hot Storage for frequently accessed and critical data that requires fast retrieval. For example, Current year transactions, frequently accessed customer data, etc.

1. In the **Hot Storage Settings** section, select the **Enable Hot Storage** checkbox.
2. Specify the **From Date, To Date,** and **Retention Period.**

<figure><img src="../../.gitbook/assets/image (1672).png" alt=""><figcaption></figcaption></figure>

**d. Define Warm Storage Settings**

> <mark style="color:red;">**Note:**</mark> You can use the Warm Storage for moderately accessed data that is not needed instantly but still accessed occasionally. For example, Data from the last 6–12 months, Periodic reporting data, etc.

1. In the **Warm Storage Settings** section, select the **Warm Storage** checkbox.
2. Specify the **From Date, To Date,** and **Retention Period.**

<figure><img src="../../.gitbook/assets/image (1673).png" alt=""><figcaption></figcaption></figure>

**e. Define Cold Storage Settings**

> <mark style="color:red;">**Note:**</mark> You can use the Cold Storage to store rarely accessed data for long-term retention. For example, Data older than 1–3 years, Audit or compliance records, etc.

1. In the **Cold Storage Settings** section, select the **Cold Storage** checkbox.
2. Specify the **From Date, To Date**, and **Retention Period**.

<figure><img src="../../.gitbook/assets/image (1674).png" alt=""><figcaption></figcaption></figure>

**f. Define Deep Archive Storage Settings**

> <mark style="color:red;">**Note:**</mark> You can use the Deep Archive Storage to store rarely accessed data for long-term retention. For example, Data older than 1–3 years, Audit or compliance records, etc.

1. In the Deep **Archive Storage Settings** section, select the  **Deep Archive Storage checkbox**.
2. Specify the **From Date, To Date,** and **Retention Period.**

<figure><img src="../../.gitbook/assets/image (1675).png" alt=""><figcaption></figcaption></figure>

3. After completing all the configuration, finally, click the **Save** button.

</details>

<details>

<summary><strong>6.Apply Data Filters</strong></summary>

**Overview**

As part of defining conditions, you need to configure Date-based filtering, which is used to select specific data for archiving based on a date or time condition. You can use the Quick Presets to specify the date ranges.

**Procedure**

The step-by-step instructions below help you understand the process of configuring date-based filtering.

1.  In the **Data Filter** column, click the **Action** option.



    <figure><img src="../../.gitbook/assets/image (150).png" alt=""><figcaption></figcaption></figure>


2. From the **Date Column** drop-down box, select the required **column**.
3. From the **Quick Presets**, select the **required quick preset** choosing from L**ast 30 days, Last 90 days, Last 6 Months, Last Year,** and **Custom Range.**  For example, Last 6 Months.

> <mark style="color:red;">**Note:**</mark> Quick Presets are shortcut options that allow you to select commonly used date ranges quickly and accurately. Once a Quick Preset is selected, the Start Date and End Date fields are populated automatically.
>
> For example, if you want to archive data for the last 6 months, simply select the “Last 6 Months” Quick Preset. Alternatively, you can use the “Custom Range” Quick Preset to manually specify the required date range.

4. Finally, click the **Save** button. See the below image.

<figure><img src="../../.gitbook/assets/image (151).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>7.Define Retention Schedule</strong></summary>

**Overview**

The purpose of configuring a retention schedule for automated data archival enforcement is to define how long data should be retained and to ensure that archival (and eventual deletion, if applicable) happens automatically based on predefined rules.

For example, if a retention schedule is set to 12 months, any data older than 12 months will be automatically archived as per the defined schedule—without needing manual action.

**Procedure**

The step-by-step instructions below help you understand the process of configuring a retention schedule.

1.  In the **Retention Job** column, click the action option.



    <figure><img src="../../.gitbook/assets/image (153).png" alt=""><figcaption></figcaption></figure>


2. On the **Retention Job Schedule** page, select the **table**.

&#x20;  The selected table name is populated in the Schedule Name field.

1. From the **Schedule Type** drop-down box, select the **required schedule type** choosing from **Daily, Weekly,** or **Monthly.** For example, Daily.&#x20;
2. In the **Description** field, enter an **appropriate description** for the retention schedule.
3. In the **Schedule Time** field, specify the schedule time by clicking the **Show Time Picker** ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAXCAYAAAALHW+jAAACGklEQVR4AexTO2tqQRD+SIqQQEgRkjRiY2trZWEh2IggKoqF+AA7C0UtBAXBShEtfSAogliICoKg2AlW/gsRRUEQfOLr3jsL58Tjg9uku/fA7M5+8+13Zmd2H3798PeAH/7+C34XdLFYoFKpwOfzQa1Ww+/3o1qtYrVafZNueDdrWCwWIRKJYLfbcTqdIJPJcDweYbPZIBaLmfANLQZdCVJWVqsVwWAQ0+kUiUQC4XCYzZPJBB6PBwaDAZ1OhwlcDgLB2WwGp9PJxOiILy8vmM/nSKfTbB+t6Uculwv00+12y/DzQSBYKBTw/v7OMuJI54IcFo/HsdvtUKvVOIifBYK9Xg8ajQaPj4884Zbz9PQElUqFbrd7FRYILpdLvL6+XpHW6zUOh4MAp+YMBgMBRguB4NfXF0ajEeG8EaZUKiGVSlEul/Hn6bPYeDzG5+cn888HgaBcLke73cZ+v+c5z8/PSKVSaDabaDQayOfz2Gw2aLVaUCgUPI9zBIJmsxnUuVAoxMX5WSKRsAwdDgfcbjers8lk4uOcIxB8e3tDJpNBNBpFLBZjmXBEmqnGgUAA2WwWdCPoGhF+bgJBCuj1etBLiUQioPp5vV52jejufXx8IJfLoV6vsy4T/9IeLgFaWywWDIdDtpmeXr/fB2VTKpVAndVqtUS7aTcFiUnHNxqNSCaTrCFUAp1OB2oSxe/ZXcF7G/6G/4OCvwEAAP//9KQKeQAAAAZJREFUAwCc7BLu3kqjGgAAAABJRU5ErkJggg==) icon.
4. In the **Notify on Failure** field, enter the **email IDs** of the recipients who should be notified in the event of a failure. You can enter multiple email IDs separated by commas.

<figure><img src="../../.gitbook/assets/image (154).png" alt=""><figcaption></figcaption></figure>

5. Finally, click the **Save** button.

</details>

<details>

<summary><strong>8.Deployment Configuration</strong></summary>

**Overview**

While creating an archival job, the purpose of a POD (in Kubernetes) is to act as the execution unit where the archival process runs. A POD contains one or more containers that perform tasks such as data extraction, transformation, and movement to archival storage.

**Procedure**

The step-by-step instructions below help you understand the process.

1. From the **Deployment Configuration** drop-down box, select **Kubernetes**.

<figure><img src="../../.gitbook/assets/image (155).png" alt=""><figcaption></figcaption></figure>

2. After selecting the deployment configuration
3. PODs are **automatically assigned at the Group level.**
4. When multiple groups are created, **separate PODs are automatically assigned to each group**

<figure><img src="../../.gitbook/assets/image (156).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>9.Specify Batch Size Settings</strong></summary>

**Overview**

**Batch Size** specifies the number of records processed in a single batch during the archival operation. As part of specifying batch size, you can also define parallel processing.

**Procedure**

The step-by-step instructions below help you understand the process of specifying batch size.

1. On the **Archival Configuration** page (See the below image):

* From the **Deployment Configuration** drop-down box, select either **Amazon ECS Cluster** or  **Kubernetes**.
* Specify the **Batch Size, File Size (MB), Max Records/File, Parallel (Yes or No)**, and **Max Parallel**.

Here is the description for the above fields:

<table><thead><tr><th width="175.66668701171875">Field</th><th>Description</th></tr></thead><tbody><tr><td>Batch Size</td><td>This field specifies the <strong>number</strong> of records processed in each batch</td></tr><tr><td>File Size (MB)</td><td>This field specifies the <strong>maximum number</strong> of archived records stored in a single output file.</td></tr><tr><td>Max Records/File</td><td>This field specifies the <strong>maximum size</strong> of each archived file</td></tr><tr><td>Parallel (Yes or No)</td><td>This field enables to specify whether multiple batches are processed simultaneously or not. If the <strong>Yes</strong> option is selected, then <strong>Parallel</strong> processing is enabled.</td></tr><tr><td>Max Parallel</td><td>This field specifies the <strong>number of batches</strong> run in parallel.For example, if you enter <strong>5</strong> in the Max Parallel field, the system processes up to <strong>5 batches</strong> in parallel.</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/image (2378).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>10.Resource Approval Rules for Archival Job</strong></summary>

**Overview**

Resource Approval Rules define the approval workflow required before an archival job is executed. These rules ensure that the appropriate stakeholders review and approve the job based on their roles and responsibilities.

For archival jobs, the approval workflow is typically configured with roles such as:

* **Data Steward** – Recommends the archival request.
* **Data Owner** – Provides final approval.

These rules are configured in the **Admin Settings module** under the Resource Approval section by selecting the **Resource Type as Archival Job**. Once defined, the configured rules automatically appear in the Archival Job creation screen.

When creating an archival job, users must select the appropriate users mapped to each role (for example, Data Steward and Data Owner). These users will be responsible for reviewing, recommending, and approving the archival request.

**Procedure**

The step-by-step instructions to Configure and Use Resource Approval Rules for Archival Job

**a. Configure Resource Approval Rules**

1. Navigate to **Admin Settings**.
2. Open the **Resource Approval Rules** section.
3. Select **Resource Type** as **Archival Job**.

<figure><img src="../../.gitbook/assets/image (143).png" alt=""><figcaption></figcaption></figure>

4. Define the approval workflow:
   1. **Role: Data Steward**
      1. Action: Recommend
      2. Accept Status: Recommended
      3. Reject Status: Rejected
      4. Is Required: Yes
      5. Priority: 1
   2. **Role: Data Owner**
      1. Action: Approve
      2. Accept Status: Approved
      3. Reject Status: Rejected
      4. Is Required: Yes
      5. Priority: 2

<figure><img src="../../.gitbook/assets/image (144).png" alt=""><figcaption></figcaption></figure>

**b. Assign Approvers During Archival Job Creation**

1. Navigate to the **Archival Job Creation** screen.
2. Scroll to the **Approval Section**:

<figure><img src="../../.gitbook/assets/image (146).png" alt=""><figcaption></figcaption></figure>

3. The system automatically displays approval roles based on configured rules.
4. For each role:
   1. **Data Steward** → Select a user from dropdown
   2. **Data Owner** → Select a user from dropdown

<figure><img src="../../.gitbook/assets/image (147).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>11.Configuration name</strong></summary>

**Overview**

Archival Configuration is used to define and save all required setup details for the archival process. After entering the necessary information

**Procedure**

The below step-by-step instructions guide you through the procedure.

1. In the **Configuration Name** field, enter a **name** for the archival job.
2. In the **Description** field, enter a **description** relevant to the archival job.
3. Click the **Validate and Save** button.

<figure><img src="../../.gitbook/assets/image (148).png" alt=""><figcaption></figcaption></figure>

4. **Validate and Review Configuration** screen is displayed with all detailes.&#x20;

</details>

<details>

<summary><strong>12.Validate and Review Configuration</strong></summary>

**Overview**

The purpose of reviewing and saving an archival job after completing all configurations is to validate the setup and securely store it so the job can be executed accurately and consistently.

**Procedure**

The below step-by-step instructions guide you through the procedure.

1. On the **Validate and Review Configuration** page, select each **table,** and review the configuration.
2. In the **Configuration Name** field, enter a **name** for the archival job.
3. In the **Description** field, enter a **description** relevant to the archival job.
4. Click the **Save Configuration** button.

<figure><img src="../../.gitbook/assets/image (149).png" alt=""><figcaption></figcaption></figure>

5. The configuration is saved and displayed on the Archival Configuration List page. See the below image.

<figure><img src="../../.gitbook/assets/image (1678).png" alt=""><figcaption></figcaption></figure>

</details>


{% endtab %}

{% tab title="Exisiting Jobs" %}
**Overview**

The Existing Jobs module allows you to view details of the archival jobs. Apart from this, you can also view the reconciliation report.

**Procedure**

The expandable panels below guide you through the process.

<details>

<summary><strong>Access Archival Job</strong></summary>

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival.**&#x20;
2. Under S**CIKIQ Archival,** expand **Archival Jobs**, and then click **Existing Jobs**.

<figure><img src="../../.gitbook/assets/1 (2).png" alt=""><figcaption><p>SCIKIQ Archival - Existing Jobs</p></figcaption></figure>

3. The **Archival Configuration** **List** page is displayed.

</details>

<details>

<summary><strong>View Archival Job Details</strong></summary>

**Overview**

The **View Details (Eye Icon)** option allows you to view the complete information of an archival configuration without editing it. This provides a read-only view of both high-level metadata and detailed configuration settings.

**Procedure**

The following step-by-step instructions guide you through the process.

1. Locate the required archival configuration.
2. Click on the **Eye Icon (View Details)** corresponding to the configuration.
3. The **Archival Job Details** screen is displayed.

<figure><img src="../../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

**Archival Job Details Screen**

**a. Configuration Information**

This section displays the basic details of the configuration:

* **Configuration Key:** Unique identifier for the archival configuration.
* **Name: E**xample: _Customer Table Archival_
* **Source Type:** Example: _ORACLE-EBS_
* **Connection Name:** Example: _ORACLE EBS AR_
* **Status:** Example: _DRAFT / SUBMITTED /_

<figure><img src="../../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

***

**b. Configuration Details**

This section provides a structured breakdown of the archival setup:

* **Selected Tables:** Displays the list of tables selected for archival.
* **Partitioning:** Shows partition logic (if configured) used to segment data for archival.
* **Filters:** Displays conditions applied to identify which data should be archived.
* **Retention Job Configuration:** Defines how long archived data is retained and any associated deletion rules.
* **Compliance:** Displays compliance-related settings such as policies or regulatory requirements.
* **AWS Configuration:** Shows cloud storage details such as:
  * S3 bucket configuration
  * Storage path
  * Region details

<figure><img src="../../.gitbook/assets/image (106).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>View Detailed Configuration</strong></summary>

**Overview**

The **Expand Icon ( > )** allows users to view complete archival job execution details, including request metadata, approval workflow, resource allocation, table-level configurations, partitioning strategy, retention policy, and storage settings.

This section provides a **read-only, consolidated view** of everything configured before deployment.

**Procedure**

The following step-by-step instructions guide you through the process.

**Expand the Configuration**

1. Navigate to the **Configuration List** page.
2. Locate the required configuration.
3. Click the **Expand Icon ( > ).**

<figure><img src="../../.gitbook/assets/image (107).png" alt=""><figcaption></figcaption></figure>

4. The **Detailed View Panel** is displayed.

<figure><img src="../../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>View Reconciliation Report</strong></summary>

**Overview**

The Reconciliation Report is automatically generated after an archival job is successfully deployed and executed. It validates the accuracy of the archival process by comparing source data with the archived data.

This report helps ensure that:

* All intended records are archived correctly
* No data loss or mismatch occurs during the process
* The archival job execution is complete and accurate

It provides a clear status of whether the data is fully matched, partially matched, or failed.

**Procedure**

The following step-by-step instructions guide you through the process.

1. Deploy and execute the **Archival Job**.
2. Once execution is completed, the system automatically triggers the **Reconciliation process**.
3. Locate and open the **Reconciliation Report** section.

<figure><img src="../../.gitbook/assets/image (117).png" alt=""><figcaption></figcaption></figure>

5. Review the report details:
   * Total source records
   * Total archived records
   * Failed or mismatched records
   * Overall reconciliation status
6. To download repot click "**Download XLSX"** Button.&#x20;

<figure><img src="../../.gitbook/assets/image (120).png" alt=""><figcaption></figcaption></figure>

</details>
{% endtab %}

{% tab title="Retrieve Data" %}
### Overview

The Retrieve Data module in SCIKIQ enables you to retrieve archived data. It also allows you to query the archived data using NLQ and SQL and provides the capability to delete the required archived data.

***

### Procedure

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Connect Data Source</strong></summary>

**Overview**

This section allows users to connect to a data source and navigate through catalogue, database, and tables to access archived data.

**Procedure**

The following step-by-step instructions guide you through the process.

**Step-by-Step Instructions**

1. Under **SCIKIQ Archival**, expand **Archival Jobs**, and then click **View Data**.

<figure><img src="../../.gitbook/assets/image (1680).png" alt=""><figcaption></figcaption></figure>

The Data Retrieval page is displayed.

2. Click **Select data source** and choose the required source.
3. Click **Select catalogue** and select the relevant catalogue.
4. Click **Select database** and choose the database.

<figure><img src="../../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>2.Tables</strong></summary>

**Overview**

This section displays all available tables and views within the selected database. Users can filter and select tables for querying.

**Procedure**

The following step-by-step instructions guide you through the process.

1. View the list of tables and views
2. Use **Filter tables and views** to search
3. Select required tables

> <mark style="color:red;">**Note:**</mark> Tables are displayed only after selecting a database

<figure><img src="../../.gitbook/assets/image (124).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>3.Query Editor</strong></summary>

**Overview**

The **Editor** is the main workspace where users create, edit, and execute SQL queries. It provides a structured interface with action buttons such as **Run**, **Explain**, **Save**, **Clear**, and **Cancel**, enabling full control over query development and execution.

The editor also supports efficient query management by allowing users to save queries for reuse, analyze execution plans, and quickly reset or stop queries when needed.

**Procedure**

The following step-by-step instructions guide you through the process.

1. Navigate to the **Editor** tab in the Query Panel.

The query editor workspace is displayed.

<figure><img src="../../.gitbook/assets/image (1693).png" alt=""><figcaption></figcaption></figure>

1. **Add New Query Editor**
   1. Click the **“+” (Add Query)** button.
   2. A new query tab is created.
   3. Use this tab to write a new query.

<figure><img src="../../.gitbook/assets/image (1691).png" alt=""><figcaption></figcaption></figure>

d. Modify an existing query if needed (either **manually** or by loading from **saved** queries)

<figure><img src="../../.gitbook/assets/image (1692).png" alt=""><figcaption></figcaption></figure>

2. **Manage Query Tabs:  Rename** option
   1. On the query tab, click the **three-dot (⋮) menu**.
   2. Select **Rename** from the menu.

<figure><img src="../../.gitbook/assets/image (1697).png" alt=""><figcaption></figcaption></figure>

c. Enter a new name for the query tab.

d. Click **Rename button** to save the new name.

<figure><img src="../../.gitbook/assets/image (1698).png" alt=""><figcaption></figcaption></figure>

3. **Manage Query Tabs: Duplicate** option
   1. On the query tab, click the **three-dot (⋮) menu**.
   2. Select **Duplicate** from the menu.
   3. A new tab is created with the same query content.

<figure><img src="../../.gitbook/assets/image (1699).png" alt=""><figcaption></figcaption></figure>

4. **Manage Query Tabs: Close Tab** option
   1. On the query tab, click the **three-dot (⋮) menu**.
   2. Select **Close tab (×)** from the menu.
   3. The selected tab is closed.
   4. Ensure the query is saved before closing if needed.

<figure><img src="../../.gitbook/assets/image (1700).png" alt=""><figcaption></figcaption></figure>

5. **Write or Modify Query**
   1. Enter the SQL query in the editor area.
   2. You can also paste an existing query or modify a loaded query.

<figure><img src="../../.gitbook/assets/image (1694).png" alt=""><figcaption></figcaption></figure>

6. **Execute Query (Run)**
   1. Click the ![](<../../.gitbook/assets/image (1707).png>) button.
   2. The system executes the query against the selected data source.
   3. Query results are displayed in the results section.

<figure><img src="../../.gitbook/assets/image (1695).png" alt=""><figcaption></figcaption></figure>

7. **Analyze Query (Explain)**
   1. Click the ![](<../../.gitbook/assets/image (1708).png>) button.
   2. The system displays the query execution plan.
   3. Use this to understand performance and optimize the query.

<figure><img src="../../.gitbook/assets/image (1696).png" alt=""><figcaption></figcaption></figure>

8. **Save Query**
   1. Click ![](<../../.gitbook/assets/image (1709).png>)to store the query for future use.

<figure><img src="../../.gitbook/assets/image (93).png" alt=""><figcaption></figcaption></figure>

b. Enter a **Query Name** in the prompt.

c. Click **Save** to store the query.

<figure><img src="../../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure>

d.  The query is saved under the **Saved Queries** tab for future use.

<figure><img src="../../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>

9. **Clear Query**
   1. To clear the existing query, Click the ![](<../../.gitbook/assets/image (1710).png>)button to remove all content from the query editor

<figure><img src="../../.gitbook/assets/image (92).png" alt=""><figcaption></figcaption></figure>

10. **Cancel Query Execution**
    1. Click the **Cancel** button while a query is running.
    2. The system stops the execution immediately.

</details>

<details>

<summary>4.<strong>Recent Queries</strong></summary>

**Overview**

The **Recent Queries** tab displays a list of queries that were recently executed in the Query Editor. It helps users quickly revisit, review, and reuse previously run queries without rewriting them, improving efficiency and productivity.

**Procedure**

The following step-by-step instructions guide you through the process.

1. **Navigate to Recent Queries**
   1. Click on the **Recent Queries** tab in the Query Panel.
   2. The system displays a list of recently executed queries.
2. **View Recent Queries**
   1. Check the list of queries along with basic details.
   2. Each entry represents a query executed earlier.

<figure><img src="../../.gitbook/assets/image (1701).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>5.Saved Queries</strong></summary>

**Overview**

The **Saved Queries** tab allows users to store and manage frequently used SQL queries for future use. It helps avoid rewriting queries by providing quick access to previously saved queries along with their associated configurations.

Saved queries retain not only the query text but also related context such as database, connection, catalog, and selected tables, making reuse efficient and consistent.

**Procedure**

The following step-by-step instructions guide you through the process.

1. **Access Saved Queries**
   1. Click on the **Saved Queries** tab in the Query Panel.
   2. The system displays a list of all saved queries.

<figure><img src="../../.gitbook/assets/image (1687).png" alt=""><figcaption></figcaption></figure>

2. **View Saved Queries**
   1. Check the list of saved queries.
   2. Each entry represents a stored query available for reuse.

<figure><img src="../../.gitbook/assets/image (1711).png" alt=""><figcaption></figcaption></figure>

c. Use the **Search** option (if available) to find a specific query.

<figure><img src="../../.gitbook/assets/image (1703).png" alt=""><figcaption></figcaption></figure>

3. **Load Saved Query**
   1. Select the required query from the **Saved Queries**.
   2. Click **Load Query** to open a previously saved query in the editor it in the Query Editor.

<figure><img src="../../.gitbook/assets/image (1702).png" alt=""><figcaption></figcaption></figure>

**c. Upon loading, the system automatically:**

* Loads the query into the Query Editor
* Selects the associated **Database**
* Selects the **Connection**
* Selects the **Catalog**
* Selects the relevant **Tables**

<figure><img src="../../.gitbook/assets/image (1704).png" alt=""><figcaption></figcaption></figure>

4. **Delete Saved Query**
   1. From the **Saved Queries** section, select query you want to remove and click **Delete Button** to remove unwanted queries Select the

<figure><img src="../../.gitbook/assets/image (1705).png" alt=""><figcaption></figcaption></figure>

b. A confirmation message is displayed: _“Delete saved query ‘\<query name>’?”_

c. Click **OK to** delete the query permanently.

<figure><img src="../../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>6.Query Settings</strong></summary>

**Overview**

The **Query Settings** tab allows users to configure how queries are executed and how results are returned. It provides control over execution resources, result limits, and editor behavior to ensure efficient query performance.

**Procedure**

The following step-by-step instructions guide you through the process.

1. **Open Query Settings**
   1. Click on the **Query Settings** tab in the Query Panel.
   2. The Query Settings options are displayed.

<figure><img src="../../.gitbook/assets/image (1712).png" alt=""><figcaption></figcaption></figure>

2. Configure the **Workgroup** (default: `primary`) to control query execution and resource usage.
3. set the **Result Limit** (default: 200 rows, range: 1–1000) to define the maximum number of rows returned.&#x20;
4. Enable or disable **Typeahead Code Suggestions** to receive automatic query suggestions while typing.

<figure><img src="../../.gitbook/assets/image (1713).png" alt=""><figcaption></figcaption></figure>

5. **Save or Cancel Settings**
   1. Click **Save Settings** to apply the changes.
   2. Click **Cancel** to discard any changes made.

<figure><img src="../../.gitbook/assets/image (1714).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>7<strong>.Query Archived Data Using NLQ</strong></summary>

**Overview**

Natural Language Query (NLQ) enables users to retrieve data using simple business questions instead of writing SQL.

**Procedure**

The following step-by-step instructions guide you through the process.

1. On the **Data Retrieval** page, in the Right **Pane**, click the **Query NLQ** icon corresponding to the table.&#x20;
2. Next, in the **center Pane**, enter the required **query**, and then click the **Run Query** button.

<figure><img src="../../.gitbook/assets/image (125).png" alt=""><figcaption></figcaption></figure>

3. Submit the query.
4. The required archived data is retrieved.

<figure><img src="../../.gitbook/assets/image (127).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>8<strong>.Query Archived Data Using SQL</strong></summary>

**Overview**

This section enables users to perform advanced data retrieval using SQL queries.

**Procedure**&#x20;

The following step-by-step instructions guide you through the process.

1. On the **Data Retrieval** page, click the **SQL** button in the **Query Data** pane.
2. Next, on the **Switch Query Mode** message box.

<figure><img src="../../.gitbook/assets/image (128).png" alt=""><figcaption></figcaption></figure>

3. SQL syntax is displayed in the Query Data pane.&#x20;
4. Select the **table**, then click on the Query Edit blank screen.
   1. The SQL query for the selected tables will be generated **automatically**.

<figure><img src="../../.gitbook/assets/image (130).png" alt=""><figcaption></figcaption></figure>

5. Click the **Run SQL Query** button.
6. The required archived data is retrieved

</details>

<details>

<summary><strong>9.Query Results</strong></summary>

**Overview**

The Query Results section displays the output generated after executing a query. It also provides execution status to confirm whether the query ran successfully or encountered errors.

**UI Components & Field Description**

* **Query Results Grid**
  * Displays retrieved data in rows and columns
  * Allows users to review output records
* **Query Status**
  * Indicates whether the query execution was successful or failed
  * Displays error messages if applicable

**Procedure**

The following step-by-step instructions guide you through the process.

1. View the output data in the **Query Results** section

<figure><img src="../../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure>

2. Review the displayed records for accuracy and completeness
3. Check **Query Status** to confirm whether the execution was successful or if any errors occurred

<figure><img src="../../.gitbook/assets/image (87).png" alt=""><figcaption></figcaption></figure>

4. If errors are present, update the query and re-run

</details>

<details>

<summary><strong>10.Query Execution Details</strong></summary>

**Overview**

This section provides detailed insights into query performance and execution metrics. It helps users analyze efficiency and troubleshoot issues.

**UI Components & Field Description**

* **Run Time**
  * Displays total time taken for query execution
* **Scanned**
  * Indicates the volume of data scanned during execution
* **Rows**
  * Shows the number of rows returned in the result
* **Workgroup**
  * Displays the execution group used
  * Default value: **primary**

**Procedure**

The following step-by-step instructions guide you through the process.

1. Review **Run Time** to understand how long the query took to execute
2. Check **Scanned** data volume to evaluate how much data was processed
3. View **Rows** returned to confirm the output size
4. Check the **Workgroup** used for execution (default: _primary_)

<figure><img src="../../.gitbook/assets/image (88).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>11.BLOB Data Tasks</strong></summary>

**Overview**

**BLOB (Binary Large Object)** is a database data type used to store large amounts of binary data.&#x20;

Some of the  examples of data that can be stored as a BLOB are:

* Images (JPEG, PNG, GIF)
* Audio files
* Video files
* PDF documents
* Word documents
* Other binary files

**Example**

In databases such as MySQL, Oracle Database, and Microsoft SQL Server, a BLOB column can store a user's profile picture directly in the database.

**Procedure**

The following sections explain how to perform the following tasks: **Set the BLOB Query Limit, View BLOB Data, Download BLOB Data,** and **Export Complete Query Results.**

**1.Set Blob Query Limit**

A. On the **Editor** tab, type the **limit**. See below image.

B. Click the **Run** button

<figure><img src="../../.gitbook/assets/image (2047).png" alt=""><figcaption></figcaption></figure>

The results are displayed as per the limit specified.

***

**2.View Blob Data**

* On the **Editor** tab, under **Query Results**, click the **View** button corresponding to the required file.

<figure><img src="../../.gitbook/assets/image (2040).png" alt=""><figcaption></figcaption></figure>

In the selected file, the binary data stored as an image is displayed. See the below image.

<figure><img src="../../.gitbook/assets/image (2041).png" alt=""><figcaption></figcaption></figure>

***

**3.Download Blob Data**

* On the **Row Data Viewer**, click the **Download** button.

<figure><img src="../../.gitbook/assets/image (2043).png" alt=""><figcaption></figcaption></figure>

The Blob Data is downloaded.

***

**4.Export Full Query Result**

A. On the **Query Editor**, in the **Query Results** section, click the **Export Full Query Result** button.

<figure><img src="../../.gitbook/assets/image (2044).png" alt=""><figcaption></figcaption></figure>

The **Export Full Query Result** dialogue box is displayed.

B. On the **Export Full Query Result** dialogue box:

* Select the **File storage connection, specify Export Path, File Type,** and **Rows per file**.
* Click the **Submit export** button.

<figure><img src="../../.gitbook/assets/image (2045).png" alt=""><figcaption></figcaption></figure>

The full query results are displayed in the selected file format.

</details>
{% endtab %}

{% tab title="Deletion Jobs" %}
**Overview**

Archiving preserves historical data for reference and compliance. However, based on the need, deleting it from the operational system improves performance by reducing data volume and speeding up queries. It also supports cost optimization, as primary storage is more expensive than archival storage.&#x20;

Deletion keeps the system clean and manageable by retaining only relevant data and avoiding duplication. Overall, it ensures the system remains efficient and streamlined.

***

**Deletion Procedure**

The deletion process involves a series of steps. As part of this process, you must first map the required business terms in the Data Dictionary. You can then initiate a data deletion request by selecting the relevant business terms along with the applicable identifier.

Once the request is initiated and the archived table discovery is completed, you can review and confirm the deletion.

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Add Business Terms</strong></summary>

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

&#x20;     The Meta Data Manager menu is displayed.

2. From the **Meta Data Manager** menu, click **Business Terms.**

<figure><img src="../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

The Business terms page is displayed.

3. On the **Business Terms** page:
   1. Add **Business Terms.**
   2. Perform **Bulk Upload.**
   3. Search **Business Terms.**

<figure><img src="../../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

4. **Adding a New Business Term**
   1. Click on **Add Business Terms**.
   2. Fill in the required details:

| Field                 | Value                                  |
| --------------------- | -------------------------------------- |
| **Terms Name**        | Customer Account ID                    |
| **Definition**        | Unique identifier for customer account |
| **Purpose**           | Identify customer account              |
| **Business Process**  | AR Process                             |
| **Owner**             | Select Process Owner                   |
| **Catalogue**         | Enterprise Data Catalogue              |
| **Glossary**          | Select Glossary                        |
| **Category**          | Select Category                        |
| **Status**            | Draft                                  |
| **Sensitive**         | PII                                    |
| **Classification**    | Internal                               |
| **Regulatory Rule**   | GDPR                                   |
| **Industry Standard** | FIBO                                   |

<figure><img src="../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

5. **Physical Schema Mapping**
   1. Click on **Physical Schema Mapping**.
   2. A mapping window will open.

<figure><img src="../../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

c. Enter the following details:

* **Connection**
* **Table**
* **Column**
* Click **Save**.

<figure><img src="../../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

6. Final Steps
   1. Click **Add Term**.
   2. The business term will be added.

<figure><img src="../../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

7. Click **Submit**.
   1. The term will now be saved and added to the list.

<figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>2.Initiate Data Deletion Request</strong></summary>

**Overview**

**Overview**

The **Initiate** stage is the first step in the deletion workflow where the user defines the scope of data to be deleted. In this stage, the system captures key inputs such as the user/entity identifier, business terms, reason for deletion, and supporting documents.

The defined scope applies across **all data layers**, including:

* **Archived Data**
* **Hot Storage (recent/active archived data)**
* **Cold Storage (long-term retained data)**

This ensures a comprehensive scan and accurate identification of all relevant records.

**Procedure**&#x20;

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival**.
2. Under **SCIKIQ Archival**, expand **Archival Jobs**, and then click **Deletion Jobs**.

<figure><img src="../../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

&#x20;   The **Archival Deletion History** page is displayed.

3. On the **Archival Deletion History page**, click **+ New Purge Request** button.

<figure><img src="../../.gitbook/assets/image (1715).png" alt=""><figcaption></figcaption></figure>

The Data Deletion Request page is displayed.

4. On the **Data Deletion Request** page:

A. in the **User/Entity Identifier** field, enter the **User / Entity Identifier.** For example, 1000.

B. From the **Business Terms** drop-down box, select one or more **Business Terms.** For example, Customer Account ID.

C. From the **Reason for Deletion** drop-down box, select an appropriate **reason.** For example, Data Retention policy Expired.

> <mark style="color:red;">**Note:**</mark> Selecting **Reason for Deletion** is mandatory for compliance and audit tracking.

D. Optionally upload a **Supporting Document** (PDF/DOC/Image) for authorization.

<figure><img src="../../.gitbook/assets/image (1716).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Scope**

The deletion scope includes:

* **All Archived Data** – Data already moved to archival storage
* **Hot Storage** – Frequently accessed or recently archived data
* **Cold Storage** – Long-term, infrequently accessed data

The system scans across all these layers to identify matching records based on the provided inputs.
{% endhint %}

E. Click the **Start Discovery Scan** button to move to the **Scanning** stage.

<figure><img src="../../.gitbook/assets/image (2136).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>3.Scan Data</strong></summary>

The system starts scanning. See the below image.&#x20;

<figure><img src="../../.gitbook/assets/image (2137).png" alt=""><figcaption></figcaption></figure>

After the completion of scanning, the **Review stepper** is highlighted.

</details>

<details>

<summary><strong>4.Review Data</strong></summary>

* On the **Review stepper**, select the **table to be deleted**, and then click the **Proceed to Delete** button.

<figure><img src="../../.gitbook/assets/image (2138).png" alt=""><figcaption></figcaption></figure>

&#x20;     The Confirm stepper is highlighted.

> <mark style="color:red;">**Note:**</mark> Before confirming deletion, you need to configure approval rules. See the next panel.&#x20;
>
> Once configured, the approval section will be displayed in the Confirm Deletion section.

</details>

<details>

<summary><strong>5.Configure Approval Rules</strong></summary>

**Overview**

As part of configuring the approval rules, you need to specify the roles that will act as Approvers and Recommenders. Additionally, you will define the corresponding Action, Accept Status, Reject Status, Priority, and SLA (Days/Hours) for each role to establish the approval workflow and processing timelines.

**Procedure**

1. On the **SCIKIQ Left Navigation Bar**, click **Admin Settings** under **Access Management.**

<figure><img src="../../.gitbook/assets/image (2141).png" alt=""><figcaption></figcaption></figure>

The **Admin Settings** page is displayed.

2.On the **Admin Settings** page, click the **Resource Approval** tab.

The **Resource Approval** tab is opened.

3.On the **Resource Approval** tab (See the below image):

A. From the **Resource Type** drop-down box, select the required **resource type**.

B. In the Manual Approval section, specify the **Role, Action, Accept Status, Reject Status, Priority,** and **SLA (Days/Hours)** for both the **Approver** and **Recommender** to define the approval workflow, decision outcomes, processing order, and turnaround timelines.

C. If you want to **add** more rows, click the ![](<../../.gitbook/assets/image (2057).png>)button.

D. If you want to **delete** a row, click the Delete Row ![](<../../.gitbook/assets/image (2058).png>)button corresponding to it.

E. Finally, click the **Save** button at the bottom.

<figure><img src="../../.gitbook/assets/image (2059).png" alt=""><figcaption></figcaption></figure>

The approval rules are saved.

F. Follow the same above instructions to configure approval rules for the other resource types.

</details>

<details>

<summary><strong>6.Select Execution Mode</strong> </summary>

**Overview**

You can select the appropriate execution mode based on how matching records should be handled.&#x20;

* **Physically Delete Mode:** The **Physically Delete** mode permanently removes all rows that meet the specified criteria.&#x20;
* **Mask Selected Column Mode:** The **Mask Selected Column** mode preserves the matching rows while masking the values in the selected columns, ensuring that sensitive data is protected without deleting the records.

**Procedure**

The below information describes how to use both **Physically Delete Mode** and **Mask Selected Column** modes:

1. **Using Physically Delete Mode**

A. On the **Confirm stepper,** in the **Execution Mode** section, select **Physically Delete** option.

<figure><img src="../../.gitbook/assets/image (2139).png" alt=""><figcaption></figcaption></figure>

B. Now, scroll down to the page, and then select in the **Approval Required** sectio&#x6E;**,** select the **Approver** and **Recommender**. See the below image).

C. In the **Type DELETE to confirm** field, enter **DELETE**.

D. Click the **Confirm Delete** button.

<figure><img src="../../.gitbook/assets/image (2144).png" alt=""><figcaption></figcaption></figure>

***

2. **Using Mask Selected Column Mode**

A. In the **Execution Mode** section, select **Mask Selected Column Mode** option.

B. In the **Columns to Mask** area, select the required **columns** to be masked.

<figure><img src="../../.gitbook/assets/image (2148).png" alt=""><figcaption></figcaption></figure>

B. Now, scroll down to the page, and then select in the **Approval Required** sectio&#x6E;**,** select the **Approver** and **Recommender**. See the below image).

C. In the **Type MASK to confirm** field, enter **MASK**.

D. Click the **Confirm Mask** button.

<figure><img src="../../.gitbook/assets/image (2150).png" alt=""><figcaption></figcaption></figure>

The deletion request is raised. See the below image.

<figure><img src="../../.gitbook/assets/image (2151).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>7.Recommender Review and Actions</strong></summary>

**Overview**

This section is meant for the **Recommender** who will review and take appropriate action on the deletion request. As part of taking the action, the **Recommender** can **recommend, reject,** or **delegate** it to another person.

**Procedure**

1. On the left navigation bar, expand **My Assets,** and then click **Asset Approval.**&#x20;

<figure><img src="../../.gitbook/assets/image (2061).png" alt=""><figcaption></figcaption></figure>

The **Asset Approval** page is displayed.

2. On the **Asset Approval** page:

**A. Review Request**

* On the left pane, click the required **Approval Request**.

The **Approval Request** details are displayed.

* Review the request details.

**B. Raise Query**

* If you want to raise a query, then write the query in the **Query** box, and then click the **Send** button.

> <mark style="color:red;">**Note:**</mark> Once the query is raised, the request status will be displayed as **Query**.

**C. Take Action**

* If you want to **recommend** the deletion request to the approver, then click the **Recommend** button on the top right side of the page.

> <mark style="color:red;">**Note:**</mark> If you want to reject, then click the **Reject** button. If required, you can also delegate it another person by clicking the **Delegate** button. &#x20;

<figure><img src="../../.gitbook/assets/image (2094).png" alt=""><figcaption></figcaption></figure>

The request is recommended and goes to the Approver. Its status is displayed as **Recommended**. See the below image.

<figure><img src="../../.gitbook/assets/image (2093).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>8.Aprover Review and Actions</strong></summary>

**Overview**

This section is meant for the **Approver** who will review and take appropriate action on the deletion request. As part of taking the action, the **Approve** can **approve, reject,** or **delegate** it to another person.

**Procedure**

1. On the left navigation bar, expand **My Assets,** and then click **Asset Approval.**&#x20;

<figure><img src="../../.gitbook/assets/image (2061).png" alt=""><figcaption></figcaption></figure>

The **Asset Approval** page is displayed.

2. On the **Asset Approval** page:

**A. Review Request**

* On the left pane, click the required **Approval Request**.

The **Approval Request** details are displayed.

* Review the request details.

**B. Raise Query**

* If you want to raise a query, then write the query in the **Query** box, and then click the **Send** button.

> <mark style="color:red;">**Note:**</mark> Once the query is raised, the request status will be displayed as **Query**.

**C. Take Action**

* If you want to **approve** the deletion request, then click the **Approve** button on the top right side of the pag&#x65;**.**

> <mark style="color:red;">**Note:**</mark> If you want to reject, then click the **Reject** button. If required, you can also delegate it another person by clicking the **Delegate** button. &#x20;

<figure><img src="../../.gitbook/assets/image (2079).png" alt=""><figcaption></figcaption></figure>

The request is approved and its status is displayed as **Approved** on the **Archival Deletion History** page. See the below image.

<figure><img src="../../.gitbook/assets/image (2095).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>9.Confirm Deletion</strong></summary>

1. On the **Archival Deletion** History page, click the **Confirm Delete** button corresponding to the approved request.

<figure><img src="../../.gitbook/assets/image (2096).png" alt=""><figcaption></figcaption></figure>

The Confirm Purge Request message is displayed.

2. On the **Confirm Purge Request** message, click the **OK** button.

<figure><img src="../../.gitbook/assets/image (2097).png" alt=""><figcaption></figcaption></figure>

The system starts purging the request and the request status is displayed as **Purging**. See the below image.

<figure><img src="../../.gitbook/assets/image (2099).png" alt=""><figcaption></figcaption></figure>



</details>
{% endtab %}

{% tab title="Deployment Configs" %}
**Overview**

The Deployment Configuration Management functionality provides a centralized way to manage and control deployment configurations for archival processes. It allows you to view, update, and delete archival configurations as required, ensuring flexibility and accuracy in setup.

***

**Procedure**

As part of deployment configuration management, you can update the required archival configuration. If required, you can also delete an archival configuration.

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Update Deployment Configuration</strong></summary>

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival.**&#x20;
2. Under S**CIKIQ Archival,** expand **Archival Jobs**, and then click **Deployment Config**.

<figure><img src="../../.gitbook/assets/image (139).png" alt=""><figcaption></figcaption></figure>

The **Job Deployment Configurations** page is displayed.

3. On the **Job Deployment Configurations** page, click the **Edit** button corresponding to the required archival configuration.

<figure><img src="../../.gitbook/assets/image (141).png" alt=""><figcaption></figcaption></figure>

The **Deployment Config Management page** is displayed.

4. On the **Deployment Config Management page**, make the required changes, and then click the **Save** button.

<figure><img src="../../.gitbook/assets/image (1684).png" alt=""><figcaption></figcaption></figure>

5. The Deployment Configuration is updated as per the changes made.

<figure><img src="../../.gitbook/assets/image (1685).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>2.Delete Deployment Configuration</strong></summary>

1. On the **Job Deployment Configurations** page, click the **Delete** button corresponding to the required archival configuration.

<figure><img src="../../.gitbook/assets/1 (12).png" alt=""><figcaption><p>Deployment Config Management - Delete Button </p></figcaption></figure>

The Delete message box is displayed.

2. On the **Delete** message box, click the **OK** button.

<figure><img src="../../.gitbook/assets/image (1596).png" alt=""><figcaption></figcaption></figure>

3. The archival configuration is deleted.

</details>
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Compliance**](compliance/)
* [**Storages**](storages/)
