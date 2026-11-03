---
icon: page
---

# Managing Cubes

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to manage existing cubes in **Cube Manager**. As part of cube management, you can perform the following tasks:

* **View Cube Details** – View the basic details and status of a cube.
* **View Cube Configuration** – Review the configuration settings defined for a cube.
* **Update Cube** – Modify the details or configuration of an existing cube.
* **Re-ingest a Cube** – Re-ingest the source data into the cube when required.
* **Investigate the Source** – Examine the source data associated with the cube.

The following **Procedure** section provides step-by-step instructions for performing these tasks.

***

### &#x20;Procedure

Click the the below tabs to view step-by-step instructions:

{% tabs %}
{% tab title="View Cube Details" %}
**Overview**

The **View Cube Details** option enables to view the **key information and current status of an existing cube**. It provides a quick way to verify the cube’s identity and operational status without opening or modifying its configuration.

**Procedure**

The below step-by-step instructions describes the procedure:

1. On the **SCIKIQ left menu**, expand **Archival Jobs** under **SCIKIQ ARCHIVAL**, and then click **Cube Manager**.

<figure><img src="../../../../.gitbook/assets/image (2883).png" alt=""><figcaption></figcaption></figure>

The Cube Manager page is displayed.

2. On the **Cube Manager** page, click the **View** icon corresponding to the required cube.

<figure><img src="../../../../.gitbook/assets/image (2884).png" alt=""><figcaption></figcaption></figure>

The Cube Viewer page is displayed with the cube details.
{% endtab %}

{% tab title="View Cube Configuration" %}
**Overview**

The **View Cube Configuration** option enables to view the **configuration settings defined for an existing cube**. It helps to understand how the cube was configured and verify the settings used for its source, extraction, and output.

**Procedure**

The below step-by-step instructions describes the procedure:

1. Navigate to **Cube Manager** page ( **SCIKIQ left menu**>>**Archival Jobs>>** **SCIKIQ ARCHIVAL**>>**Cube Manager**).
2. On the **Cube Manager** page, click the **View Config** icon corresponding to the required cube.

<figure><img src="../../../../.gitbook/assets/image (2885).png" alt=""><figcaption></figcaption></figure>

The Cube Config screen is displayed. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2886).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Update Cube" %}
**Overview**

The **Update Cube** option enables to **modify the configuration or details of an existing cube** without creating a new cube. It is useful when the existing configuration needs to be changed to reflect updated requirements.

**Procedure**

The below step-by-step instructions describes the procedure:

1. Navigate to **Cube Manager** page ( **SCIKIQ left menu**>>**Archival Jobs>>** **SCIKIQ ARCHIVAL**>>**Cube Manager**).
2. On the **Cube Manager** page, click the **Edit** icon corresponding to the required cube.

<figure><img src="../../../../.gitbook/assets/image (2887).png" alt=""><figcaption></figcaption></figure>

The Edit Cube dialogue box is displayed.

3. On the **Edit Cube** dialogue box, make the required changes, and then click the **Save Changes** button.

<figure><img src="../../../../.gitbook/assets/image (2888).png" alt=""><figcaption></figcaption></figure>

The cube is updated.
{% endtab %}

{% tab title="Investigate the Source" %}
**Overview**

The **Investigate the Source** option in Cube Manager helps users **examine the source data associated with a cube before or after ingestion**. It provides visibility into the source data and helps users verify that the expected data is available and suitable for processing.

**Procedure**

The below step-by-step instructions describes the procedure:

1. Navigate to **Cube Manager** page ( **SCIKIQ left menu**>>**Archival Jobs>>** **SCIKIQ ARCHIVAL**>>**Cube Manager**).&#x20;
2. On the **Cube Manager** page, click the **Investigate the Source** icon corresponding to the required cube.

<figure><img src="../../../../.gitbook/assets/image (2889).png" alt=""><figcaption></figcaption></figure>

The Investigation started message is displayed. Once completed, the report appears next to the cube.
{% endtab %}

{% tab title="Re Ingest" %}
**Overview**

The **Re-ingest** option in Cube Manager is used to **run the data ingestion process again for an existing cube using its configured source data**. It allows the cube to be refreshed when the source data has changed or when the previous ingestion did not complete as expected.

**Procedure**

The below step-by-step instructions describes the procedure:

1. Navigate to **Cube Manager** page ( **SCIKIQ left menu**>>**Archival Jobs>>** **SCIKIQ ARCHIVAL**>>**Cube Manager**).&#x20;
2. On the **Cube Manager** page, click the **Re Ingest** icon corresponding to the required cube.

<figure><img src="../../../../.gitbook/assets/image (2890).png" alt=""><figcaption></figcaption></figure>

The parsing starts and source begins downloading. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2891).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Adding a Cube**](adding-a-cube.md)
