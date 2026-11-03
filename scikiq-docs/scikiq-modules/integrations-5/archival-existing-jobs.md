---
hidden: true
icon: page
---

# Archival Existing Jobs

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

Deploying the archival job is to activate and run the job in the designated execution environment. Deployment ensures that all configurations, such as data sources, policies, and storage settings, are applied and executed correctly. It initiates the actual process of moving data from primary systems to archival storage.

***

### Procedure

As part of deploying an archival configuration, you need to click the **Deploy** button corresponding to it on the Configuration List page. Once confirmed, the configuration is successfully deployed, and its status is updated to **Submitted**.

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Access Archival Job</strong></summary>

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival.**&#x20;
2. Under S**CIKIQ Archival,** expand **Archival Jobs**, and then click **Existing Jobs**.

<figure><img src="../../.gitbook/assets/1 (2).png" alt=""><figcaption><p>SCIKIQ Archival - Existing Jobs</p></figcaption></figure>

3. The **Archival Configuration** **List** page is displayed.

</details>

<details>

<summary><strong>2.View Details</strong></summary>

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

<summary><strong>3.Expand Icon – View Detailed Configuration</strong></summary>

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

<summary><strong>4.Approval Workflow Execution</strong></summary>

**Overview**

Before deployment, the configuration may require approval based on predefined workflow rules.

**Procedure**

The following step-by-step instructions guide you through the process.

**Data Steward** Action

1. Login with **Data Steward** role
2. Go to the **Resource Approval screen**
3. The request is routed to the selected **Data Steward**.
4. The Data Steward can:
   1. **Recommend** → Moves request to next level
   2. **Reject** → Workflow stops
5. Click on the **Recommend** moving next level.&#x20;

<figure><img src="../../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>

**Data Owner** Action

1. **Login with Data Owner role**
2. Go to the **Resource Approval screen**
3. After the Data Steward selects **Recommend**, the request is routed to the **Data Owner**
4. **Under Data Owner Action:** The request is assigned to the selected Data Owner.
5. **The Data Owner can:**
   1. **Approve** → Final approval; the request is completed
   2. **Reject** → Workflow stops
6. Click Approve Final approval the request is completed

<figure><img src="../../.gitbook/assets/image (110).png" alt=""><figcaption></figcaption></figure>

7. Once approved in the configured list, when the job status is set to Approved, the job becomes eligible for execution.

<figure><img src="../../.gitbook/assets/image (111).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>5.Run Archival Job</strong></summary>

1. On the **Archival Configuration** **List** page, click the **Run** icon corresponding to the required archival configuration.

<figure><img src="../../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>

2. The Confirm Deployment message box is displayed.
3. On the **Confirm Run** message box, click the **Run** button.

<figure><img src="../../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>

4. A **Deployment request submitted successfully** message is displayed, and the configuration status is updated to **Submitted** on the Configuration Lists page.&#x20;

<figure><img src="../../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (115).png" alt="" width="124"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>6.Reconciliation Report</strong></summary>

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

<details>

<summary><strong>7.Delete Archival Job</strong></summary>

**Overview**

The Delete Archival Configuration option allows users to permanently remove an existing archival configuration from the system. This action is irreversible and should be performed only when the configuration is no longer required.

For example, when deleting **Archived GL Tables**, the system prompts for confirmation to prevent accidental deletion.

**Procedure**

The following step-by-step instructions guide you through the process.

1. Locate the configuration you want to delete (for example, **Archived GL Tables**).
2. Click on the **Delete** (🗑) icon associated with the configuration.

<figure><img src="../../.gitbook/assets/image (121).png" alt=""><figcaption></figcaption></figure>

The **Confirm Delete Configuration** dialog is displayed with the message:

* _“Are you sure you want to delete this configuration?”_
* _“This action cannot be undone.”_

5. Click **Confirm/Delete** to proceed.
   * Click **Cancel** to abort the action.
6. Upon confirmation, the configuration is permanently deleted from the system.

<figure><img src="../../.gitbook/assets/image (122).png" alt=""><figcaption></figcaption></figure>

</details>

***

### Related Topics
