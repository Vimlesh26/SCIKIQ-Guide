---
icon: page
---

# Using Archival Dashboard

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The **Archival Dashboard** provides a centralized interface to monitor data retention lifecycles, track system performance, and manage operational health.

**Key Features & Capabilities:**

* **Volumetric Metrics:** Track total counts for **archival jobs, data sources, source sizes, configured/archived tables, records processed**, and **partition executions**.
* **Storage Efficiency:** Monitor **compression savings, archived data size**, and **storage distribution** to track footprint reduction.
* **Progress Tracking:** View real-time status updates on **table coverage, partition success**, and **archived footprint progress**.
* **System Health & Governance:** Diagnose issues using live indicators for **open errors, failed partitions, pod/restored states**, and **governance workloads**.
* **Activity Insights:** Quickly identify **top archived tables, recent jobs**, and the primary **data sources** contributing to your archives.

This page provides step-by-step instructions on how to view the dashboard metrics for a **required time period** and access the **archival configuration list**.

***

### Procedure

Click on the below tabs to view the procedure.

{% tabs %}
{% tab title="Viewing Dashboard Metrics for a Specific Time Period" %}
**Overview**

The Search functionality provides you to view the archival dashboard  for the required specific period. Viewing the archival dashboard for a specific time period helps you perform critical analysis and troubleshooting.

**Procedure**

The below step-by-step instructions help you understand how to view the archival dashboard  for the required specific period.

_**To view the archival dashboard  for the required specific period:**_

1. On the **SCIKIQ left menu**, expand **Archival Jobs** under **SCIKIQ ARCHIVAL**, and then click **Archival Dashboard.**

<figure><img src="../../../.gitbook/assets/image (2941).png" alt=""><figcaption></figcaption></figure>

The **Archival Dashboard** is displayed.

2. On the **Archival Dashboard**, select the **From Date, To Date,** and then click the **Apply** button.&#x20;

<figure><img src="../../../.gitbook/assets/image (2942).png" alt=""><figcaption></figcaption></figure>

The Archival Dashboard is displayed for the selected period.
{% endtab %}

{% tab title="Accessing the Archival Configuration List" %}
**Overview**

Viewing the **Archival Configuration List** helps users **review and manage the archival configurations** defined in the system. It provides a consolidated view of configured archival jobs, including their associated data sources, schedules, storage settings, and current status, making it easier to **verify configurations, identify required changes, and manage archival activities**.

**Procedure**

The below step-by-step instructions help you understand how to view the archival configuration list:

_**To view the archival configuration list:**_

1. Navigate to **Archival Dashboard** page. (**SCIKIQ left menu>>** **Archival Jobs>>Archival Dashboard).**
2. On the **Archival Dashboard** page, click the **Configurations** button.

<figure><img src="../../../.gitbook/assets/image (2944).png" alt=""><figcaption></figcaption></figure>

The **Archival Configuration List** page is displayed. See the below image:

<figure><img src="../../../.gitbook/assets/image (2945).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Creating a Table Archival Job**](creating-a-table-archival-job.md)
* [**Creating a File Archival Job**](creating-a-file-archival-job.md)
* [**Validating Data**](validating-data.md)
* [**Managing Existing Jobs**](managing-existing-jobs.md)
* [**Retrieving Data**](retrieving-data.md)
* [**Managing Deployment Configs**](managing-deployment-configs.md)
* [**Deleting Archived Data**](deleting-archived-data.md)
* [**Managing Retention Schedules**](managing-retention-schedules.md)
* [**Using Cube Manager**](using-cube-manager.md)
* [**Using Cube Viewer**](using-cube-viewer.md)
