---
icon: page
---

# Managing Existing Jobs

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The **Existing Jobs** module enables to view and monitor details of previously created archival jobs. It also provides access to the **reconciliation report**, which helps reviewing and verifying the results of the archival process.

***

### **Procedure**

Click the below tabs to view the procedure.

{% tabs %}
{% tab title="Viewing Archival Job Details" %}
**Overview**

The **View Details** option allows you to view the complete information of an archival configuration without editing it. This provides a read-only view of both high-level metadata and detailed configuration settings.

**Procedure**

The following step-by-step instructions guide you through the process.

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival.**&#x20;
2. Under S**CIKIQ Archival,** expand **Archival Jobs**, and then click **Existing Jobs**.

<figure><img src="../../../.gitbook/assets/1 (2).png" alt=""><figcaption><p>SCIKIQ Archival - Existing Jobs</p></figcaption></figure>

The **Archival Configuration** **List** page is displayed.

3. On the **Archival Configuration** **List** page, click the **Eye Icon (View Details)** corresponding to the configuration.

The **Archival Job Details** screen is displayed.

<figure><img src="../../../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

**Archival Job Details Screen**

**a. Configuration Information**

This section displays the basic details of the configuration:

* **Configuration Key:** Unique identifier for the archival configuration.
* **Name: E**xample: _Customer Table Archival_
* **Source Type:** Example: _ORACLE-EBS_
* **Connection Name:** Example: _ORACLE EBS AR_
* **Status:** Example: _DRAFT / SUBMITTED /_

<figure><img src="../../../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../../../.gitbook/assets/image (2865).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Viewing Detailed Configuration" %}
**Overview**

The **Expand Icon** allows viewing complete archival job execution details, including request metadata, approval workflow, resource allocation, table-level configurations, partitioning strategy, retention policy, and storage settings.

**Procedure**

The following step-by-step instructions help you understand how to view the complete archival job execution details.

_**To view complete archival job execution details**_

* Navigate to the **Configuration List** page, click the **Expand Icon ( > )** corresponding to the required configuratio&#x6E;**.**

<figure><img src="../../../.gitbook/assets/image (107).png" alt=""><figcaption></figcaption></figure>

The **Detailed View Panel** is displayed.

<figure><img src="../../../.gitbook/assets/image (2866).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Viewing Reconciliation Report" %}
**Overview**

The **Reconciliation Report** helps to validate the accuracy of the archival process by comparing source data with the archived data.

This report helps ensure that:

* All intended records are archived correctly&#x20;
* No data loss or mismatch occurs during the process
* The archival job execution is complete and accurate

It provides a clear status of whether the data is fully matched, partially matched, or failed.

**Procedure**

The following step-by-step instructions how to view the reconciliation report.

_**To view reconciliation report**_

1. Navigate to the **Existing Jobs** page (Archival Jobs>>Existing page).&#x20;
2. On the **Existing Jobs** page, click the **Reconciliation Report** icon corresponding to the required configuration.

<figure><img src="../../../.gitbook/assets/image (117).png" alt=""><figcaption></figcaption></figure>

The **Reconciliation Report** is displayed.

3. On the **Reconciliation Report,** review the report details.
4. If you want to **download the report**, click the **Download XLSX** button.

<figure><img src="../../../.gitbook/assets/image (2868).png" alt=""><figcaption></figcaption></figure>

The Reconciliation Report is downloaded in the local system.
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Creating a Table Archival Job**](creating-a-table-archival-job.md)
* [**Creating a File Archival Job**](creating-a-file-archival-job.md)
* [**Validating Data**](validating-data.md)
* [**Retrieving Data**](retrieving-data.md)
* [**Managing Deployment Configs**](managing-deployment-configs.md)
* [**Deleting Archived Data**](deleting-archived-data.md)
* [**Managing Retention Schedules**](managing-retention-schedules.md)
* [**Using Archival Dashboard**](using-archival-dashboard.md)
* [**Using Cube Manager**](using-cube-manager.md)
* [**Using Cube Viewer**](using-cube-viewer.md)
