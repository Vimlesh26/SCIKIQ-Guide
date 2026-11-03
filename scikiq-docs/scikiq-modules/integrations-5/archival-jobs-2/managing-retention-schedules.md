---
icon: page
---

# Managing Retention Schedules

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

**Retention Schedules** define **how long archived data or files should be retained and when retention-related actions should occur**. They provide a structured approach to managing the lifecycle of archived data based on defined retention requirements.

This page provides step-by-step instructions for **adding, viewing, updating, and deleting retention schedules**.

***

### Procedure

Click on the below tabs to view the procedure.

{% tabs %}
{% tab title="Creating a Retention Schedule" %}
**Overview**

As part of creating a **Retention Schedule**, you need to specify the **Schedule Name, Description, Glue Configuration, Schedule Configuration, Notifications and Options,** and **Retention Configuration**. Once saved, the retention schedule is created.

**Procedure**

The below step-by-step instructions help you understand how to create a retention  schedule.

_**To create a retention schedule**_

1. On the **SCIKIQ left menu**, expand **Archival Jobs** under **SCIKIQ ARCHIVAL**, and then click **Retention Schedules.**

<figure><img src="../../../.gitbook/assets/image (2903).png" alt=""><figcaption></figcaption></figure>

The **Retention Job Schedules** page is displayed.

2. On the **Retention Job Schedules** page, click the **New Schedule** button.

The **Retention Job Schedule** dialogue box is displayed.

3. In the **Retention Job Schedule** dialogue box, specify **Schedule Name, Description, Glue Configuration, Schedule Configuration, Notifications and Options,** and **Retention Configuration.**

> <mark style="color:red;">**Note:**</mark> Refer to the below table for the description of above fields mentioned in Step 3.

**Field Description Table**

| Field                       | Option                   | Description                                                                                                       | What to specify                                                                    |
| --------------------------- | ------------------------ | ----------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| **Schedule Name**           | —                        | Identifies the retention job schedule.                                                                            | Specify a unique and meaningful name for the schedule.                             |
| **Description**             | —                        | Provides additional information about the purpose of the schedule.                                                | Enter a brief description of the retention job schedule.                           |
| **Glue Configuration**      | —                        | Specifies the AWS Glue configuration used by the retention job to access and process the cataloged archival data. | Select the appropriate Glue configuration.                                         |
| **Schedule Configuration**  | —                        | Defines when and how frequently the retention job is executed.                                                    | Specify the required execution schedule, such as frequency, date, and time.        |
| **Notifications & Options** | **Enabled**              | Determines whether the retention job schedule is active.                                                          | Enable the option to activate the schedule for execution.                          |
| **Notifications & Options** | **Dry Run**              | Enables the retention job to simulate the retention operation without performing the actual action.               | Enable the option to validate or preview the retention operation before execution. |
| **Notifications & Options** | **Notify on Failure**    | Determines whether a notification is generated when the retention job fails.                                      | Enable the option to receive failure notifications.                                |
| **Retention Configuration** | **Configuring Table**    | Specifies the table on which the retention configuration is applied.                                              | Select or specify the applicable archived table.                                   |
| **Retention Configuration** | **Partition Column**     | Specifies the table column used to identify and process data partitions for retention.                            | Select the appropriate partition column.                                           |
| **Retention Configuration** | **Hot Storage**          | Defines the retention or transition criteria for data stored in the hot storage tier.                             | Specify the applicable duration or transition criteria for hot storage.            |
| **Retention Configuration** | **Warm Storage**         | Defines the retention or transition criteria for data stored in the warm storage tier.                            | Specify the applicable duration or transition criteria for warm storage.           |
| **Retention Configuration** | **Cold Storage**         | Defines the retention or transition criteria for data stored in the cold storage tier.                            | Specify the applicable duration or transition criteria for cold storage.           |
| **Retention Configuration** | **Deep Archive Storage** | Defines the retention or transition criteria for data stored in the deep archive storage tier.                    | Specify the applicable duration or transition criteria for deep archive storage.   |

<figure><img src="../../../.gitbook/assets/image (2906).png" alt=""><figcaption></figcaption></figure>

3. Click the **Save Schedule** button.

The retention schedule is created and displayed on the **Retention Job Schedules** page.&#x20;

<figure><img src="../../../.gitbook/assets/image (2909).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Viewing a Retention Job Schedule Details" %}
**Overview**

The **View Retention Schedule Details** option enables to review the **configured settings and current status of an existing retention schedule** without modifying it. This helps to verify how the schedule is configured and understand the retention rules and execution settings currently in effect.

**Procedure**

The below step-by-step instructions help you understand how to view the details of a retention job schedule.

_**To view a retention job schedule details**_

1. Navigate to **Retention Job Schedules** page. (**SCIKIQ left menu>>** **Archival Jobs>>** **Retention Schedules>>Retention Job Schedules** page)**.**

The **Retention Job Schedules** page is displayed.

2. On the **Retention Job Schedules** page, click the **View** icon corresponding to the required schedule.

<figure><img src="../../../.gitbook/assets/image (2910).png" alt=""><figcaption></figcaption></figure>

The **View Retention Job Schedule** screen is displayed. See the below image.

<figure><img src="../../../.gitbook/assets/image (2911).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Updating a Retention Job Schedule" %}
**Overview**

The **Update Retention Schedule** option enables to modify the configuration of an existing retention schedule when retention requirements or operational settings change. This helps keep the schedule aligned with current archival and data lifecycle requirements without creating a new schedule.

**Procedure**

The below step-by-step instructions help you understand how to update  a retention job schedule.

_**To update a retention job schedule**_

1. Navigate to **Retention Job Schedules** page. (**SCIKIQ left menu>>** **Archival Jobs>>** **Retention Schedules>>Retention Job Schedules** page)**.**

The **Retention Job Schedules** page is displayed.

2. On the **Retention Job Schedules** page, click the **Update** icon corresponding to the required schedule.

<figure><img src="../../../.gitbook/assets/image (2892).png" alt=""><figcaption></figcaption></figure>

The **Edit Retention Job Schedule** dialogue box is displayed.

3. On the **Edit Retention Job Schedule** dialogue box, make the required changes, and then click the **Save Schedule** button.

<figure><img src="../../../.gitbook/assets/image (2893).png" alt=""><figcaption></figcaption></figure>

The retention job schedule is updated.
{% endtab %}

{% tab title="Deleting a Retention Job Schedule" %}
**Overview**

The **Delete Retention Job Schedule** option enables to remove a retention schedule that is **no longer required or applicable**. Deleting an obsolete schedule helps prevent unnecessary retention jobs from being maintained or executed based on outdated configurations.

**Procedure**

The below step-by-step instructions help you understand how to delete  a retention job schedule.

_**To delete a  retention job schedule**_

1. Navigate to **Retention Job Schedules** page. (**SCIKIQ left menu>>** **Archival Jobs>>** **Retention Schedules>>Retention Job Schedules** page)**.**

The **Retention Job Schedules** page is displayed.

2. On the **Retention Job Schedules** page, click the **Delete** icon corresponding to the required schedule.

<figure><img src="../../../.gitbook/assets/image (2895).png" alt=""><figcaption></figcaption></figure>

The Delete Retention Schedule message box is displayed.

3. On the **Delete Retention Schedule** message box, click the **Delete** button.

<figure><img src="../../../.gitbook/assets/image (2896).png" alt=""><figcaption></figcaption></figure>

The retention job schedule is deleted.
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
* [**Using Archival Dashboard**](using-archival-dashboard.md)
* [**Using Cube Manager**](using-cube-manager.md)
* [**Using Cube Viewer**](using-cube-viewer.md)
