---
icon: page
---

# Creating a Table Archival Job

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

Creating an archival job is to automate the process of moving inactive or historical data from primary systems to long-term storage. It helps improve application performance by reducing the load on active databases. An archival job ensures that data is stored securely while meeting compliance and retention requirements.

***

### **Procedure**

The process involves a series of sequential steps, which includes **Setup Data Source, Define Data Selection, Select Compliance Policy, Enable PII Detection, Setup Partitioning, Apply Data Filters, Define Retention Schedule, POD Management,** and **Review & Save**.&#x20;

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

<figure><img src="../../../.gitbook/assets/image (1631).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../../../.gitbook/assets/image (1657).png" alt=""><figcaption></figcaption></figure>

D. From the **Selected Tables** list, select the required **tables**.

{% hint style="info" %}
**Tip:**  Selecting the tables specifies the tables that are to be archived.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (1659).png" alt=""><figcaption></figcaption></figure>

**a. Table Selection and Grouping for Archival**

1. To begin, clicking on the **Advanced Search** button to search table by name.

<figure><img src="../../../.gitbook/assets/image (1661).png" alt=""><figcaption></figcaption></figure>

2. Provide the name of the table you want to search for. For example, enter a table name like **“BANK”** in the search field.
3. If matching text is found, the system will display all relevant tables associated with your search term.

<figure><img src="../../../.gitbook/assets/image (1663).png" alt=""><figcaption></figcaption></figure>

4. The matching tables (e.g., all tables related to “BANK”) will then be appended to the existing table list.

<figure><img src="../../../.gitbook/assets/image (1664).png" alt=""><figcaption></figcaption></figure>

**b. Managing Table Groups**

1. Click on **“Add Row”** to create multiple groups.
2. Each group allows you to organize and assign different tables as needed.
3. Click on **Add Row.**

<figure><img src="../../../.gitbook/assets/image (1668).png" alt=""><figcaption></figcaption></figure>

**c. Assigning Modules**

1. You can assign selected tables to specific groups based on different modules.
2. Choose the desired module from the dropdown menu available for each group.

<figure><img src="../../../.gitbook/assets/image (1666).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../../../.gitbook/assets/image (1636).png" alt=""><figcaption></figcaption></figure>

2. On the **Data Selection** page, click **each table** to perform data profiling.

<figure><img src="../../../.gitbook/assets/image (1638).png" alt=""><figcaption></figcaption></figure>

3. After completion of data profiling, click the **Close** button.

<figure><img src="../../../.gitbook/assets/image (1639).png" alt=""><figcaption></figcaption></figure>

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



    <figure><img src="../../../.gitbook/assets/image (1633).png" alt=""><figcaption></figcaption></figure>


2. select the required **policy** from the **Compliance Policy** drop-down to apply compliance rules to the first table.

The selected compliance policy details appear below.&#x20;

2. If you want to apply **same compliance policy** to all tables, then select ![](<../../../.gitbook/assets/unknown (36).png>)to apply the same compliance policy to all tables.

The selected compliance policy details appear below.

3.  If not, select the required table, and then select the required policy from the **Compliance Policy** drop-down box.



    <figure><img src="../../../.gitbook/assets/image (1641).png" alt=""><figcaption></figcaption></figure>
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



    <figure><img src="../../../.gitbook/assets/image (1642).png" alt=""><figcaption></figcaption></figure>
2.  On the **PII Detection** page, click the **PII Protection Settings** button.



    <figure><img src="../../../.gitbook/assets/image (1643).png" alt=""><figcaption></figcaption></figure>

The PII Protection Settings screen is displayed.

1. On the **PII Protection Settings** screen, select the **Enable PI** checkbox.
2. From the **Detection Patterns** List, select the **required patterns.**&#x20;
3. From the **Masking Method** drop- down box, select the applicable **masking method**.&#x20;

<figure><img src="../../../.gitbook/assets/image (1644).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../../../.gitbook/assets/image (1645).png" alt=""><figcaption></figcaption></figure>

2. The detected PII patterns are displayed. See the below image.

<figure><img src="../../../.gitbook/assets/image (1646).png" alt=""><figcaption></figcaption></figure>

**c. Specify Masking Methods**

1. On the **PII Detection** page, from the **Masking Method** drop-down box, select the required **masking method**.
2. Follow the same procedure for all the detected patterns.
3. Apply the same procedure for all the tables.
4. Click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (1647).png" alt=""><figcaption></figcaption></figure>

5. The partitioning column is highlighted.

</details>

<details>

<summary><strong>5. Set Storage Configuration</strong></summary>

**Overview**

The **Set Storage Configuration** step allows you to define how and where the data will be stored in AWS. It includes selecting the storage configuration and specifying the partitioning column to optimize data storage and retrieval.

&#x20;**Procedure**

The step-by-step instructions below help you understand the partitioning process.

1. In the **Storage Config** column, click the action option.

<figure><img src="../../../.gitbook/assets/image (1648).png" alt=""><figcaption></figcaption></figure>

**a. Select Partitioning method**&#x20;

1. On the **Partitioning** page, select **Date Based** or **Range Based** to choose the partitioning method.

{% hint style="info" %}
Tip:&#x20;

**Tip: Here is the description for partitioning methods:**

* **Date-Based Partitioning:** Divides data based on time intervals such as day, month, or year.
* **Range-Based Partitioning:** Divides data into partitions based on defined value ranges of a column.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (1649).png" alt=""><figcaption></figcaption></figure>

**b. Select Configuration Parameters**

1. From the **AWS Storage Configuration** drop-down box, select the **AWS Config**, which you have already created.
2. From the **Partition Column** drop-down box, select the **required partition column**.
3. If you want to apply **same AWS config for al**l to all tables, then select ![](<../../../.gitbook/assets/image (1652).png>)to apply the same **AWS Config** to all tables.

{% hint style="info" %}
**Tip: Here is the description for AWS Configuration parameters:**

* AWS Storage Configuration: Defines the storage location and tiering strategy for archived data in AWS.
* Partition Column: Specifies the column used to divide data into partitions for efficient storage and processing.
{% endhint %}

> <mark style="color:red;">**Note:**</mark> Make sure to select the Configuration Parameters for all the tables.

<figure><img src="../../../.gitbook/assets/image (1650).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../../../.gitbook/assets/image (1669).png" alt=""><figcaption></figcaption></figure>

2. Select the required **Storage Tier** (Hot, Warm, Cold, Deep Archive).
   1. Enter the **Date Range**:
   2. Specify the **Start Date**
   3. Specify the **End Date**
3. Click **Apply**.&#x20;
   1. Confirmation message: **“Applied: \[Start Date] to \[End Date] across all tables."**

<figure><img src="../../../.gitbook/assets/image (1670).png" alt=""><figcaption></figcaption></figure>

**b. Configure Table-Level Partitioning Range**

1. In the **Partitioning** column, click the **Action** option.

<figure><img src="../../../.gitbook/assets/image (1654).png" alt=""><figcaption></figcaption></figure>

2. A list of all **selected tables** will appear in a **drop-down selection list**.
3. From this list, you can:
   1. View all selected tables
4. The selected tables details appear below.&#x20;
   1. If you want to apply **same date ranges** to all tables, then select to ![](<../../../.gitbook/assets/image (1677).png>)  apply the same date ranges to all tables.

<figure><img src="../../../.gitbook/assets/image (1676).png" alt=""><figcaption></figcaption></figure>

**c. Define Hot Storage Settings**

> <mark style="color:red;">**Note:**</mark> You can use the Hot Storage for frequently accessed and critical data that requires fast retrieval. For example, Current year transactions, frequently accessed customer data, etc.

1. In the **Hot Storage Settings** section, select the **Enable Hot Storage** checkbox.
2. Specify the **From Date, To Date,** and **Retention Period.**

<figure><img src="../../../.gitbook/assets/image (1672).png" alt=""><figcaption></figcaption></figure>

**d. Define Warm Storage Settings**

> <mark style="color:red;">**Note:**</mark> You can use the Warm Storage for moderately accessed data that is not needed instantly but still accessed occasionally. For example, Data from the last 6–12 months, Periodic reporting data, etc.

1. In the **Warm Storage Settings** section, select the **Warm Storage** checkbox.
2. Specify the **From Date, To Date,** and **Retention Period.**

<figure><img src="../../../.gitbook/assets/image (1673).png" alt=""><figcaption></figcaption></figure>

**e. Define Cold Storage Settings**

> <mark style="color:red;">**Note:**</mark> You can use the Cold Storage to store rarely accessed data for long-term retention. For example, Data older than 1–3 years, Audit or compliance records, etc.

1. In the **Cold Storage Settings** section, select the **Cold Storage** checkbox.
2. Specify the **From Date, To Date**, and **Retention Period**.

<figure><img src="../../../.gitbook/assets/image (1674).png" alt=""><figcaption></figcaption></figure>

**f. Define Deep Archive Storage Settings**

> <mark style="color:red;">**Note:**</mark> You can use the Deep Archive Storage to store rarely accessed data for long-term retention. For example, Data older than 1–3 years, Audit or compliance records, etc.

1. In the Deep **Archive Storage Settings** section, select the  **Deep Archive Storage checkbox**.
2. Specify the **From Date, To Date,** and **Retention Period.**

<figure><img src="../../../.gitbook/assets/image (1675).png" alt=""><figcaption></figcaption></figure>

3. After completing all the configuration, finally, click the **Save** button.

</details>

<details>

<summary><strong>6.Apply Data Filters</strong></summary>

**Overview**

As part of defining conditions, you need to configure Date-based filtering, which is used to select specific data for archiving based on a date or time condition. You can use the Quick Presets to specify the date ranges.

**Procedure**

The step-by-step instructions below help you understand the process of configuring date-based filtering.

1.  In the **Data Filter** column, click the **Action** option.



    <figure><img src="../../../.gitbook/assets/image (150).png" alt=""><figcaption></figcaption></figure>


2. From the **Date Column** drop-down box, select the required **column**.
3. From the **Quick Presets**, select the **required quick preset** choosing from L**ast 30 days, Last 90 days, Last 6 Months, Last Year,** and **Custom Range.**  For example, Last 6 Months.

> <mark style="color:red;">**Note:**</mark> Quick Presets are shortcut options that allow you to select commonly used date ranges quickly and accurately. Once a Quick Preset is selected, the Start Date and End Date fields are populated automatically.
>
> For example, if you want to archive data for the last 6 months, simply select the “Last 6 Months” Quick Preset. Alternatively, you can use the “Custom Range” Quick Preset to manually specify the required date range.

4. Finally, click the **Save** button. See the below image.

<figure><img src="../../../.gitbook/assets/image (151).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>7.Define Retention Schedule</strong></summary>

**Overview**

The purpose of configuring a retention schedule for automated data archival enforcement is to define how long data should be retained and to ensure that archival (and eventual deletion, if applicable) happens automatically based on predefined rules.

For example, if a retention schedule is set to 12 months, any data older than 12 months will be automatically archived as per the defined schedule—without needing manual action.

**Procedure**

The step-by-step instructions below help you understand the process of configuring a retention schedule.

1.  In the **Retention Job** column, click the action option.



    <figure><img src="../../../.gitbook/assets/image (153).png" alt=""><figcaption></figcaption></figure>


2. On the **Retention Job Schedule** page, select the **table**.

&#x20;  The selected table name is populated in the Schedule Name field.

1. From the **Schedule Type** drop-down box, select the **required schedule type** choosing from **Daily, Weekly,** or **Monthly.** For example, Daily.&#x20;
2. In the **Description** field, enter an **appropriate description** for the retention schedule.
3. In the **Schedule Time** field, specify the schedule time by clicking the **Show Time Picker** ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAXCAYAAAALHW+jAAACGklEQVR4AexTO2tqQRD+SIqQQEgRkjRiY2trZWEh2IggKoqF+AA7C0UtBAXBShEtfSAogliICoKg2AlW/gsRRUEQfOLr3jsL58Tjg9uku/fA7M5+8+13Zmd2H3798PeAH/7+C34XdLFYoFKpwOfzQa1Ww+/3o1qtYrVafZNueDdrWCwWIRKJYLfbcTqdIJPJcDweYbPZIBaLmfANLQZdCVJWVqsVwWAQ0+kUiUQC4XCYzZPJBB6PBwaDAZ1OhwlcDgLB2WwGp9PJxOiILy8vmM/nSKfTbB+t6Uculwv00+12y/DzQSBYKBTw/v7OMuJI54IcFo/HsdvtUKvVOIifBYK9Xg8ajQaPj4884Zbz9PQElUqFbrd7FRYILpdLvL6+XpHW6zUOh4MAp+YMBgMBRguB4NfXF0ajEeG8EaZUKiGVSlEul/Hn6bPYeDzG5+cn888HgaBcLke73cZ+v+c5z8/PSKVSaDabaDQayOfz2Gw2aLVaUCgUPI9zBIJmsxnUuVAoxMX5WSKRsAwdDgfcbjers8lk4uOcIxB8e3tDJpNBNBpFLBZjmXBEmqnGgUAA2WwWdCPoGhF+bgJBCuj1etBLiUQioPp5vV52jejufXx8IJfLoV6vsy4T/9IeLgFaWywWDIdDtpmeXr/fB2VTKpVAndVqtUS7aTcFiUnHNxqNSCaTrCFUAp1OB2oSxe/ZXcF7G/6G/4OCvwEAAP//9KQKeQAAAAZJREFUAwCc7BLu3kqjGgAAAABJRU5ErkJggg==) icon.
4. In the **Notify on Failure** field, enter the **email IDs** of the recipients who should be notified in the event of a failure. You can enter multiple email IDs separated by commas.

<figure><img src="../../../.gitbook/assets/image (154).png" alt=""><figcaption></figcaption></figure>

5. Finally, click the **Save** button.

</details>

<details>

<summary><strong>8.Deployment Configuration</strong></summary>

**Overview**

While creating an archival job, the purpose of a POD (in Kubernetes) is to act as the execution unit where the archival process runs. A POD contains one or more containers that perform tasks such as data extraction, transformation, and movement to archival storage.

**Procedure**

The step-by-step instructions below help you understand the process.

1. From the **Deployment Configuration** drop-down box, select **Kubernetes**.

<figure><img src="../../../.gitbook/assets/image (155).png" alt=""><figcaption></figcaption></figure>

2. After selecting the deployment configuration
3. PODs are **automatically assigned at the Group level.**
4. When multiple groups are created, **separate PODs are automatically assigned to each group**

<figure><img src="../../../.gitbook/assets/image (156).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../../../.gitbook/assets/image (2378).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../../../.gitbook/assets/image (143).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../../../.gitbook/assets/image (144).png" alt=""><figcaption></figcaption></figure>

**b. Assign Approvers During Archival Job Creation**

1. Navigate to the **Archival Job Creation** screen.
2. Scroll to the **Approval Section**:

<figure><img src="../../../.gitbook/assets/image (146).png" alt=""><figcaption></figcaption></figure>

3. The system automatically displays approval roles based on configured rules.
4. For each role:
   1. **Data Steward** → Select a user from dropdown
   2. **Data Owner** → Select a user from dropdown

<figure><img src="../../../.gitbook/assets/image (147).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>11.Specify Configuration name</strong></summary>

**Overview**

Archival Configuration is used to define and save all required setup details for the archival process. After entering the necessary information

**Procedure**

The below step-by-step instructions guide you through the procedure.

1. In the **Configuration Name** field, enter a **name** for the archival job.
2. In the **Description** field, enter a **description** relevant to the archival job.
3. Click the **Validate and Save** button.

<figure><img src="../../../.gitbook/assets/image (148).png" alt=""><figcaption></figcaption></figure>

The **Validate and Review Configuration** screen is displayed with all details.&#x20;

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

<figure><img src="../../../.gitbook/assets/image (149).png" alt=""><figcaption></figcaption></figure>

5. The configuration is saved and displayed on the Archival Configuration List page. See the below image.

<figure><img src="../../../.gitbook/assets/image (1678).png" alt=""><figcaption></figcaption></figure>

</details>

### Related Topics
