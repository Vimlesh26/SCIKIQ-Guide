---
hidden: true
icon: clock-desk
---

# Migration Requests

**Contents**

* [**Instructions for Using this Page**](migration-requests.md#instructions-for-using-this-page)
* [**Overview**](migration-requests.md#overview)
* [**Interface Description**](migration-requests.md#interface-description)
* [**Executing a Migration Request**](migration-requests.md#executing-a-migration-request)
* [**Monitoring Migration Request**](migration-requests.md#monitoring-migration-request)
* [**Rerun a Failed Migration**](migration-requests.md#rerun-a-failed-migration)
* [**Downloading Reconciliation Report**](migration-requests.md#downloading-reconciliation-report)
* [**Related Topics**](migration-requests.md#related-topics)

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The Migration Requests page provides a consolidated view of all migration requests along with their current status. Once a migration is created, it is displayed on the Migration Requests page for monitoring and execution.&#x20;

You can use the Search functionality to filter and view migration requests by status, including **Created, Submitted, In Progress, Data Copied, Partial, Finished,** and **Error**.&#x20;

The page also offers additional actions such as Refresh, Data Migration, Re-run, and Create Physical Model to manage and control migration operations. In addition, the Advanced Search feature allows you to filter migration requests based on the Source and Target.&#x20;

The following Interface Description section provides a detailed explanation of each available action.

***

### Interface Description

<figure><img src="../../../.gitbook/assets/S (83).png" alt=""><figcaption><p>Data Migration Requests Page</p></figcaption></figure>

**Description**

<table><thead><tr><th width="113">Screenshot Number </th><th width="161">Fuctionality Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td>Advanced Search</td><td>Using the Advanced Search feature, you can filter migration requests based on the Source and Target.</td></tr><tr><td>2</td><td>Search </td><td>Using the Search feature, you can filter migration requests based on Created, Submitted, In Progress, Data Copied, Partial, Finished, and Error.</td></tr><tr><td>3</td><td>Page Size</td><td>Using the Page Size feature, you can specify the number of migration requests displayed per page, with options ranging from 20 to 200.</td></tr><tr><td>4</td><td>Refresh</td><td>Using the Refresh button, you can refresh the page.</td></tr><tr><td>5</td><td>Data Migration</td><td>Clicking the Data Migration button allows you to directly access the Data Migration Wizard to create a migration request, eliminating the need to navigate to the Data Migration menu under the SCIKIQ Migration Hub in the left navigation pane.</td></tr><tr><td>6</td><td>View Summary Forward Arrow Button</td><td>Clicking the Forward Arrow Button allows you to view the execution summary.</td></tr><tr><td>7</td><td>Re-Run</td><td>Clicking the Re-Run button allows you to restart migration requests that are in the Error state.</td></tr><tr><td>8</td><td>Create Physical Model</td><td>Clicking the Create Physical Model button enables you to create the physical model.</td></tr></tbody></table>

***

### Executing a Migration Request

***

#### Overview

Once a migration request is created, it appears on the **Migration Requests page** with a Created status. The data migration request can be executed using one of two methods: **Run Now** or **Run Later.**&#x20;

Selecting **Run Now** initiates the data migration immediately, while **Run Later** allows you to schedule the migration for a specified date and time.&#x20;

Once the migration request is executed, its status changes from Created to Submitted.

***

#### Procedure

The below sections help you understand how to use the **Run Now** and **Run Later** options to execute the migration requests:&#x20;

Expand the panels to view the inside information.

<details>

<summary>Run Now</summary>

**Overview**

This section describes how to execute a data migration request using the **Run Now** option. As part of the process, you need to select the specify the required comments and then click the **Run** button. Once initiated, the data migration process begins.

**Procedure**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar** of the **SCIKIQ** application, click **Migration Requests** under **SCIKIQ Migration Hub**.

<figure><img src="../../../.gitbook/assets/S (84).png" alt=""><figcaption><p>Migration Requests Menu</p></figcaption></figure>

The Data Migration Request page is displayed.&#x20;

2. On the **Data Migration Request** page, from the **Search** drop-down box, select the **Created** option.

<figure><img src="../../../.gitbook/assets/S (85).png" alt=""><figcaption><p>Selection of Created Option</p></figcaption></figure>

The migration requests that are in Selected state are displayed.

2. Click the **Run** button corresponding to the migration request, which you wish to run.

{% hint style="info" %}
**Tip:** If you wish view the the migration summary, then click the Forward Arrow  ![](<../../../.gitbook/assets/image (177).png>) button next to the Run button.
{% endhint %}

<figure><img src="../../../.gitbook/assets/S (86).png" alt=""><figcaption><p>Migration Request Run Button</p></figcaption></figure>

The Data Migration Schedule dialogue box is displayed.

3. On the **Data Migration Schedule** dialogue box:

* Select the **Run Now** option if it is not already selected by default.&#x20;
* In the Comments, enter the **comments.**
* Click the **Run** button.

{% hint style="info" %}
**Tip:** The Run Now option is selected by default.
{% endhint %}

<figure><img src="../../../.gitbook/assets/S (87).png" alt="" width="563"><figcaption><p>Data Migration Schedule Dialogue Box</p></figcaption></figure>

Data migration starts and the **Data Migration Started** message box is displayed at the right bottom of the page. See the below image:

<figure><img src="../../../.gitbook/assets/S (88).png" alt=""><figcaption><p>Data Migration Started Message Box</p></figcaption></figure>

</details>

<details>

<summary>Run Later</summary>

**Overview**

This section describes how to **schedule** a data migration request to a later time using the **Run Later** option. As part of the procedure, you need to select the **Run Later** option, specify the required comments, and the date and time  for when the data migration should begin, and then click the Run button. Once submitted, the data migration is scheduled accordingly.&#x20;

**Procedure**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar** of the **SCIKIQ** application, click **Migration Requests** under **SCIKIQ Migration Hub**.

<figure><img src="../../../.gitbook/assets/S (84).png" alt=""><figcaption><p>Migration Requests Menu</p></figcaption></figure>

The Data Migration Request page is displayed.&#x20;

2. On the **Data Migration Request** page, from the **Search** drop-down box, select the **Created** option.

<figure><img src="../../../.gitbook/assets/S (85).png" alt=""><figcaption><p>Selection of Created Option</p></figcaption></figure>

The migration requests that are in Selected state are displayed.

2. Click the **Run** button corresponding to the migration request, which you wish to run.

{% hint style="info" %}
**Tip:** If you wish view the the migration summary, then click the Forward Arrow  ![](<../../../.gitbook/assets/image (177).png>) button next to the Run button.
{% endhint %}

<figure><img src="../../../.gitbook/assets/S (89).png" alt=""><figcaption><p>Migration Request Run Button</p></figcaption></figure>

The Data Migration Schedule dialogue box is displayed.

3. On the **Data Migration Schedule** dialogue box:

* Select the **Run Later** option.

{% hint style="info" %}
**Tip:** The Run Now is the default selected option.
{% endhint %}

* In the **Comments** box, enter the **related comments.**
* Specify the **Start Date** and **Time** for when the data migration should begin.
* Click the **Save** button.

<figure><img src="../../../.gitbook/assets/S (90).png" alt="" width="563"><figcaption><p>Selection of Run Later Option on Data Migration Dialogue box </p></figcaption></figure>

The **Data Migration Scheduled** message is displayed at the right bottom of the page. See the below image:

<figure><img src="../../../.gitbook/assets/S (91).png" alt=""><figcaption><p>Data Migration Scheduled Message </p></figcaption></figure>

</details>

***

### Monitoring Migration Request

***

#### Overview

Once a migration request is executed, it appears on the Migration Requests page with a status of **Created**. The request then progresses through several stages before completion, including In **Progress, Data Copied, Row-Level Reconciliation,** and **Column-Level Reconciliation**. After the data migration and reconciliation are successfully completed, the job status is updated to **Finished**.

***

#### Migration Statuses

The below table helps you understand the different statuses of migration at various stages:

| Stage                                                          | Migration Status |
| -------------------------------------------------------------- | ---------------- |
| After execution (Run Now or Schedule Later)                    | Submitted        |
| After submitting                                               | In Progress      |
| If there are issues with all the tables during migration       | Error            |
| If there are issues with only one or a few tables but not all  | Partial          |
| If all the tables are migrated without any issues              | Finished         |

#### Monitoring Stages

Expand the below panels to view the information inside .

<details>

<summary>In Progress </summary>

**Overview:**

Once a migration request is triggered, the job status changes from **Created** to **In Progress**, indicating that the migration pipeline has started and is actively processing data. During this stage, data is being transferred from the source system (for example, Oracle) to the target system (for example, SCIKIQ DnA Hub) and the associated processing tasks are underway.

**Key Observations:**

* **Progress Bar:** Progress Bars show the sequential execution of the below subtasks:
  * POD Assignment
  * Source Stats Capture
  * Data Copy
  * Discovery
* **Indication:** A green progress bar shows the completed step Source Stats Capture, while Data Copy and Discovery are still running.
* **Time Tracking:** Each step logs start and end timestamps, aiding in performance audits and operational benchmarking.

**Importance:**

This stage provides transparency in execution and is critical for identifying runtime bottlenecks or latency issues.

<figure><img src="../../../.gitbook/assets/S (92).png" alt=""><figcaption><p>In Progress Status</p></figcaption></figure>

</details>

<details>

<summary>Data Copied </summary>

**Overview:**

Once the data extraction, transformation (if applied), and load (ETL) are complete, the job status is updated to **Data Copied**.

**Highlights:**

* **Indication:** Orange Label (DATA COPIED) is shown both at the job level and table level.
* **Pod Details:** Information for POD2 has also appeared, indicating parallel execution for different tables.
* **Execution Trail:** The execution percentage of each subtask and status (e.g., 100% Done, 0% Done, In Progress) are visible.
* **Control Panel:** Discovery and Data Quality checks remain optional at this point.

**Importance:**

This serves as a checkpoint before entering validation stages such as reconciliation, metadata verification, and downstream audit readiness.

<figure><img src="../../../.gitbook/assets/S (93).png" alt=""><figcaption><p>Data Copied Status</p></figcaption></figure>

</details>

<details>

<summary>Row-Level Reconciliation </summary>

**Overview:**

When the row count of the source and target systems matches, the job details pane displays the reconciliation indicator in <mark style="color:green;">**green**</mark>, confirming that row-level reconciliation has been successfully completed. This visual indicator helps you quickly verify that the migrated data is consistent between the source and the target.

**Key Observations:**

* **Source/Target Row Count:** Both equal&#x20;
* **Start/End Time:** Clearly recorded with millisecond precision
* **Status:** DATA COPIED
* **Reconciliation Status:** Green tick confirms that row count matches and no data integrity violation has occurred.

**Importance:**

This screen is pivotal for regulatory compliance in industries like finance and healthcare where reconciliation logs are mandatory for audits.

<figure><img src="../../../.gitbook/assets/S (94).png" alt=""><figcaption><p>Reconciliation</p></figcaption></figure>

</details>

<details>

<summary>Column-Level Profile Validation</summary>

**Overview:**

The column-level table profile provides detailed information about each column after migration. This view helps you review how data has been transformed and verify the integrity of individual columns, ensuring that the migrated data remains accurate and consistent.

**Attributes Tracked:**

* Source vs Destination Column Name and Type
* Source/Target Count (Total, Null, Unique)
* Data Type Mapping (e.g., NUMBER → numeric(37,15), DATE → timestamp)

> <mark style="color:red;">**Note:**</mark> You can download the reconciliation results for offline reporting or audit archival by clicking the **Download CSV** button.

**Importance:**

This in-depth validation ensures semantic consistency and confirms that no corruption or loss occurred during migration essential for mission-critical datasets.

<figure><img src="../../../.gitbook/assets/S (95).png" alt=""><figcaption><p>Column Level Profile Validation</p></figcaption></figure>

</details>

<details>

<summary>Finished </summary>

**Overview**

Once data migration completed successfully, the job status is updated to **Finished**. A migration is considered successful when all key stages—**POD Assignment, Source Stats Capture, Data Copy, Reconciliation,** and **Discovery**—all are completed at 100%. This confirms that the data has been fully processed, validated, and made available in the target system.

**Key Feature**&#x20;

At this stage, Create Physical Model feature is displayed. This feature is highlighted in green and serves as the logical next step post-migration. It helps to:

* Visualize the structure of newly ingested tables
* Build relational mappings between tables (primary/foreign key relationships)
* Prepare the data for downstream consumption in analytics and reporting workflows

This interface links data migration with semantic and data modeling tasks, ensuring continuity in the data lifecycle.

<figure><img src="../../../.gitbook/assets/S (96).png" alt=""><figcaption><p>Finished Status</p></figcaption></figure>

</details>

***

### Rerun a Failed Migration

***

#### Overview

This page explains how to rerun a failed migration. If a migration request does not complete successfully, it is displayed on the Migration Requests page with a status of **Error** and a **Partial** state. You can rerun the migration after reviewing the error message and addressing the underlying issue.

The below mentioned section describes the procedure.

***

#### Procedure

**Overview**

Before rerunning a failed migration request, first review the error message to understand the cause of the failure. Take the necessary corrective action based on the identified issue, and then rerun the migration request. Once done, the Data Migration Started message is displayed.

The below step-by-step instructions help you understand how to rerun an error migration :&#x20;

**Step-by-Step Instructions**

1\. On the **Left Navigation Bar** of the **SCIKIQ** application, click **Migration Requests** under **SCIKIQ Migration Hub**.

<figure><img src="../../../.gitbook/assets/S (84).png" alt=""><figcaption><p>Migration Requests Menu</p></figcaption></figure>

The Data Migration Request page is displayed.&#x20;

2. On the **Data Migration Request** page, click the **Forward Arrow** button next to the **Re-Run** button.

<figure><img src="../../../.gitbook/assets/S (97).png" alt=""><figcaption><p>Migration Request - Forward Arrow Button</p></figcaption></figure>

The Task Details section is displayed.

3. On the **Task Details** section, click the ![](<../../../.gitbook/assets/image (178).png>) button.

<figure><img src="../../../.gitbook/assets/S (98).png" alt=""><figcaption><p>Migration Request Plus Button</p></figcaption></figure>

The Migration Summary section is displayed.

3. On the **Migration Summary** section, click the **Error** button.&#x20;

<figure><img src="../../../.gitbook/assets/S (99).png" alt=""><figcaption><p>Clicking Error Button</p></figcaption></figure>

The Error message is displayed.

4. Review the **error message** and **identify** the issue.

<figure><img src="../../../.gitbook/assets/S (100).png" alt=""><figcaption><p>Error Message</p></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> If the error is due to POD, then click the **Menu** button next to the Error button to select **Resume POD** or **Restart POD**.

<figure><img src="../../../.gitbook/assets/S (101).png" alt=""><figcaption><p> Resume POD and Restart POD Options</p></figcaption></figure>

5. Finally, click the **Re-Run** button.

<figure><img src="../../../.gitbook/assets/S (102).png" alt=""><figcaption><p>Rerunning Failed Migration</p></figcaption></figure>

The Data Migration Schedule dialogue box is displayed.

6. On the **Data Migration Schedule** dialogue box:

* Select **Run Now** or **Run Later.** For example, Run Now.
* In the **Comments** box, enter the **description**.
* Click the **Run** button.

<figure><img src="../../../.gitbook/assets/S (103).png" alt=""><figcaption><p>Executing Failed Migration</p></figcaption></figure>

The **Data Migration Started** message is displayed.

***

### Downloading Reconciliation Report

***

#### Overview

This page explains how to download a reconciliation report. Reconciliation is achieved when the source row count matches the target row count. If required, you can download the reconciliation report.&#x20;

The reconciliation report is critical for regulatory compliance in industries such as finance and healthcare, where reconciliation logs are often mandatory for audits.

The below mentioned section describes the procedure of downloading reconciliation report.

***

#### Procedure

1\. On the **Left Navigation Bar** of the **SCIKIQ** application, click **Migration Requests** under **SCIKIQ Migration Hub**.

<figure><img src="../../../.gitbook/assets/S (84).png" alt=""><figcaption><p>Migration Requests Menu</p></figcaption></figure>

The Data Migration Request page is displayed.&#x20;

2. On the **Data Migration Request** page, click the **Forward Arrow** button corresponding to the required migration request.

The Table Summary is displayed.

3. On the **Table Summary**, click the **Table Profile** icon.

<figure><img src="../../../.gitbook/assets/S (104).png" alt=""><figcaption><p>Table Profile Icon</p></figcaption></figure>

The Table Profile screen is displayed.

4. On the **Table Profile** screen, click the **Download CSV** button.

<figure><img src="../../../.gitbook/assets/S (105).png" alt=""><figcaption><p>Download CSV</p></figcaption></figure>

The Reconciliation Report is downloaded in your local system.

<figure><img src="../../../.gitbook/assets/S (106).png" alt=""><figcaption><p>Reconciliation Report</p></figcaption></figure>

***

### Related Topics <a href="#related-topics" id="related-topics"></a>

[Migration Types](https://scikiq.gitbook.io/scikiq-help/~/changes/17/scikiq-connect/migrating-data/migration-types)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
