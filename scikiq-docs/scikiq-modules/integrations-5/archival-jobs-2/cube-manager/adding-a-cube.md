---
icon: page
---

# Adding a Cube

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to add a cube in the archival. **Adding a Cube** enables users to configure and ingest source data into a structured analytical representation within the Archival environment. The processed data is stored in the configured output location, making archived information more accessible and easier to **view, analyze, and report on**.

### Procedure

The below step-by-step instructions help you understand how to add a cube:

{% stepper %}
{% step %}
**Navigate to Cube Manager Page**

On the **SCIKIQ left menu**, expand **Archival Jobs** under **SCIKIQ ARCHIVAL**, and then click **Cube Manager**.

<figure><img src="../../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Configure Cube Settings**

**Overview**

As part of adding a cube, you need to configure the **Cube Name, Description, Cube Type, Extract Format, Oracle EPM Instance, Source Datasource (File Storage), Source Path (within Datasource), Output Datasource (Parquet),** and **Output Path**.

**Procedure**

The following step-by-step instructions explain how to add a cube.

_**To add a cube**_

1. On the **Cube Manager** page, click the **Add Cube** button.

<figure><img src="../../../../.gitbook/assets/image (2898).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../../../../.gitbook/assets/image (2901).png" alt=""><figcaption></figcaption></figure>

The cube is added and displayed on the Cube Manager page. See the below image.

<figure><img src="../../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

***

### Related Topics

* [**Managing Cubes**](managing-cubes.md)
