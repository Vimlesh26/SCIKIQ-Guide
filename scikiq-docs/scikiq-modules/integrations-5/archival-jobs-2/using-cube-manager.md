---
icon: page
---

# Using Cube Manager

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

**Cube Manager** is a component of the **Archival** module used to create, configure, and manage data cubes associated with archived data. A **data cube** organizes data into dimensions and measures, enabling efficient **exploration, filtering, aggregation, and analysis** of archived data.

This page provides step-by-step instructions for **adding a cube in the SCIKIQ Archival module**. It also explains how to **view cube details and configuration, update a cube, investigate the source, and re-ingest a cube**.

***

### Procedure

Click the below tabs to view the procedure.

{% tabs %}
{% tab title="Adding a Cube" %}
**Overview**

**Adding a Cube** enables users to configure and ingest source data into a structured analytical representation within the Archival environment. The processed data is stored in the configured output location, making archived information more accessible and easier to **view, analyze, and report on**.

**Procedure**

As part of the procedure, you need to perform the below mentioned activities in the sequence as specified:&#x20;

1. **Navigate to Cube Manager Page**
2. **Configure Cube Settings**
3. **Approval By Recommender**
4. **Approval By Approver**
5. **Running the Cube**

***

{% stepper %}
{% step %}
#### **Navigate to Cube Manager Page**

On the **SCIKIQ left menu**, expand **Archival Jobs** under **SCIKIQ ARCHIVAL**, and then click **Cube Manager**.

<figure><img src="../../../.gitbook/assets/image (2882).png" alt=""><figcaption></figcaption></figure>

[**Top**](using-cube-manager.md#instructions-for-using-this-page)

***
{% endstep %}

{% step %}
#### **Configure Cube Settings**

**Overview**

As part of adding a cube, you need to configure the **Cube Name, Description, Cube Type, Extract Format, Oracle EPM Instance, Source Datasource (File Storage), Source Path (within Datasource), Output Datasource (Parquet),** and **Output Path**.

**Procedure**

The following step-by-step instructions explain how to add a cube.

_**To add a cube**_

1. On the **Cube Manager** page, click the **Add Cube** button.

<figure><img src="../../../.gitbook/assets/image (2898).png" alt=""><figcaption></figcaption></figure>

The **Add Cube** dialogue box is displayed.

2. On the **Add Cube** dialogue box, specify the **Name, Description, Cube type, Extract format, Oracle EPM instance, Source datasource (file storage), Source path (within datasource), Output datasource (parquet), Output path / prefix, Recommender,** and **Approver**.

> <mark style="color:red;">**Note:**</mark> Refer to the below table for the description of above fields.

**Field Description**

| Field                                | Purpose                                                                                                                   |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------- |
| **Name**                             | Specifies a unique name for the cube.                                                                                     |
| **Description**                      | Provides a brief description of the cube and its purpose.                                                                 |
| **Cube Type**                        | Specifies the type of cube to be created based on the required analytical or archival use case.                           |
| **Extract Format**                   | Specifies the format in which data is extracted from the source system.                                                   |
| **Oracle EPM Instance**              | Specifies the Oracle EPM instance from which the cube data is extracted.                                                  |
| **Source Datasource (File Storage)** | Specifies the configured file-storage datasource that contains the source data used to create the cube.                   |
| **Source Path (within Datasource)**  | Specifies the location of the source files within the selected datasource.                                                |
| **Output Datasource (Parquet)**      | Specifies the target file-storage datasource where the processed cube data is stored in Parquet format.                   |
| **Output Path / Prefix**             | Specifies the destination path or prefix within the output datasource where the Parquet files are stored.                 |
| **Recommender**                      | Specifies the user responsible for reviewing the cube configuration and providing the required recommendation.            |
| **Approver**                         | Specifies the user responsible for reviewing and providing the final approval for the cube.                               |
| **Upload & Ingest**                  | Uploads the required source data and initiates the ingestion process to create the cube based on the configured settings. |

3. Click the **Upload & Ingest** button.

<figure><img src="../../../.gitbook/assets/image (2901).png" alt=""><figcaption></figcaption></figure>

The cube is added and displayed on the Cube Manager page. See the below image.

<figure><img src="../../../.gitbook/assets/image (2881).png" alt=""><figcaption></figcaption></figure>

[**Top**](using-cube-manager.md#instructions-for-using-this-page)

***
{% endstep %}

{% step %}
#### **Approval By Recommender**

**Overview**

The **Recommender** is responsible for **reviewing the cube configuration and providing a recommendation** before the cube proceeds for final approval.

The Recommender typically verifies that the configured details—such as the source, output location, cube type, and other settings—are appropriate and complete.

**Procedure**

The below step-by-step instructions help you understand how the recommender can approval the cube:

_**To approve the cube**_

1. Login to the **SCIKIQ application** with the Recommender login credentials.

The **Home** page is displayed.

2. On the **Home** page, expand **Asset and Resources** under **My Profile**, and then click **Resource Approval**.

<figure><img src="../../../.gitbook/assets/image (2869).png" alt=""><figcaption></figcaption></figure>

The **Resource Approval** page displayed.

3. On the **Resource Approval** page, select the cube, and then click the **Approve Selected** button.

<figure><img src="../../../.gitbook/assets/image (2870).png" alt=""><figcaption></figcaption></figure>

The **Resource Approval** message box is displayed.

3. On the **Resource Approval** message box, click the **Approve** button.

<figure><img src="../../../.gitbook/assets/image (2871).png" alt=""><figcaption></figcaption></figure>

The request is approved and the Success message is displayed. See the below image.

<figure><img src="../../../.gitbook/assets/image (2873).png" alt=""><figcaption></figcaption></figure>

[**Top**](using-cube-manager.md#instructions-for-using-this-page)

***
{% endstep %}

{% step %}
#### **Approval By Approver**

**Overview**

The **Approver** is responsible for **reviewing the cube configuration and the Recommender’s recommendation and providing the final approval**.

The Approver serves as the final authorization step before the cube can proceed with the configured process.

**Procedure**

The below step-by-step instructions help you understand how the approver can approval the cube:

_**To approve the cube**_

1. Login to the **SCIKIQ application** with the Approver login credentials.

The **Home** page is displayed.

2. On the **Home** page, expand **Asset and Resources** under **My Profile**, and then click **Resource Approval**.

<figure><img src="../../../.gitbook/assets/image (2874).png" alt=""><figcaption></figcaption></figure>

The **Resource Approval** page displayed.

3. On the **Resource Approval** page, select the cube, and then click the **Approve Selected** button.

<figure><img src="../../../.gitbook/assets/image (2877).png" alt=""><figcaption></figcaption></figure>

The request is approved and the Success message is displayed. See the below image.

<figure><img src="../../../.gitbook/assets/image (2878).png" alt=""><figcaption></figcaption></figure>

[**Top**](using-cube-manager.md#instructions-for-using-this-page)

***
{% endstep %}

{% step %}
#### **Running the Cube**

**Overview**

After the required approvals are completed, **running the cube** initiates the configured cube processing and ingestion process. The system uses the approved configuration to access the source data, process it, and generate or refresh the cube data in the configured output location.

**Procedure**

The below step-by-step instructions help you understand how to run the cube:

_**To run the cube**_

1. On the **Cube Manager** page, click the **Run** button corresponding to the required cube.

<figure><img src="../../../.gitbook/assets/image (2879).png" alt=""><figcaption></figcaption></figure>

The **Run Cube** message box is displayed.

2. On the  **Run Cube** message box, click the **Run** button.

<figure><img src="../../../.gitbook/assets/image (2880).png" alt=""><figcaption></figcaption></figure>

The cube is executed.

[**Top**](using-cube-manager.md#instructions-for-using-this-page)
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Viewing Cube Details" %}
The **View Cube Details** option enables to view the **key information and current status of an existing cube**. It provides a quick way to verify the cube’s identity and operational status without opening or modifying its configuration.

**Procedure**

The below step-by-step instructions describes the procedure:

1. On the **SCIKIQ left menu**, expand **Archival Jobs** under **SCIKIQ ARCHIVAL**, and then click **Cube Manager**.

<figure><img src="../../../.gitbook/assets/image (2883).png" alt=""><figcaption></figcaption></figure>

The Cube Manager page is displayed.

2. On the **Cube Manager** page, click the **View** icon corresponding to the required cube.

<figure><img src="../../../.gitbook/assets/image (2884).png" alt=""><figcaption></figcaption></figure>

The Cube Viewer page is displayed with the cube details.
{% endtab %}

{% tab title="Viewing Cube Configuration" %}
**Overview**

The **View Cube Configuration** option enables to view the **configuration settings defined for an existing cube**. It helps to understand how the cube was configured and verify the settings used for its source, extraction, and output.

**Procedure**

The below step-by-step instructions describes the procedure:

1. Navigate to **Cube Manager** page ( **SCIKIQ left menu**>>**Archival Jobs>>** **SCIKIQ ARCHIVAL**>>**Cube Manager**).
2. On the **Cube Manager** page, click the **View Config** icon corresponding to the required cube.

<figure><img src="../../../.gitbook/assets/image (2885).png" alt=""><figcaption></figcaption></figure>

The Cube Config screen is displayed. See the below image.

<figure><img src="../../../.gitbook/assets/image (2862).png" alt=""><figcaption></figcaption></figure>


{% endtab %}

{% tab title="Updating Cube" %}
**Overview**

The **Update Cube** option enables to **modify the configuration or details of an existing cube** without creating a new cube. It is useful when the existing configuration needs to be changed to reflect updated requirements.

**Procedure**

The below step-by-step instructions describes the procedure:

1. Navigate to **Cube Manager** page ( **SCIKIQ left menu**>>**Archival Jobs>>** **SCIKIQ ARCHIVAL**>>**Cube Manager**).
2. On the **Cube Manager** page, click the **Edit** icon corresponding to the required cube.

<figure><img src="../../../.gitbook/assets/image (2887).png" alt=""><figcaption></figcaption></figure>

The Edit Cube dialogue box is displayed.

3. On the **Edit Cube** dialogue box, make the required changes, and then click the **Save Changes** button.

<figure><img src="../../../.gitbook/assets/image (2888).png" alt=""><figcaption></figcaption></figure>

The cube is updated.


{% endtab %}

{% tab title="Investigating Source" %}
**Overview**

The **Investigate the Source** option in Cube Manager helps users **examine the source data associated with a cube before or after ingestion**. It provides visibility into the source data and helps users verify that the expected data is available and suitable for processing.

**Procedure**

The below step-by-step instructions describes the procedure:

1. Navigate to **Cube Manager** page ( **SCIKIQ left menu**>>**Archival Jobs>>** **SCIKIQ ARCHIVAL**>>**Cube Manager**).&#x20;
2. On the **Cube Manager** page, click the **Investigate the Source** icon corresponding to the required cube.

<figure><img src="../../../.gitbook/assets/image (2889).png" alt=""><figcaption></figcaption></figure>

The Investigation started message is displayed. Once completed, the report appears next to the cube.


{% endtab %}

{% tab title="Re-ingesting Cube" %}
**Overview**

The **Re-ingest** option in Cube Manager is used to **run the data ingestion process again for an existing cube using its configured source data**. It allows the cube to be refreshed when the source data has changed or when the previous ingestion did not complete as expected.

**Procedure**

The below step-by-step instructions describes the procedure:

1. Navigate to **Cube Manager** page ( **SCIKIQ left menu**>>**Archival Jobs>>** **SCIKIQ ARCHIVAL**>>**Cube Manager**).&#x20;
2. On the **Cube Manager** page, click the **Re Ingest** icon corresponding to the required cube.

<figure><img src="../../../.gitbook/assets/image (2890).png" alt=""><figcaption></figcaption></figure>

The parsing starts and source begins downloading. See the below image.

<figure><img src="../../../.gitbook/assets/image (2863).png" alt=""><figcaption></figcaption></figure>
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
* [**Using Archival Dashboard**](using-archival-dashboard.md)
* [**Using Cube Viewer**](using-cube-viewer.md)
