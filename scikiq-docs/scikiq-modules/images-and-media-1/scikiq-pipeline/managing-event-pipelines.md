---
icon: page
---

# Managing Event Pipelines

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

After a pipeline is created, it appears on the **Pipelines page**, where it can be accessed and managed. From this page, you can view the list of available pipelines and perform various management actions related to their configuration and execution. These actions include **View Pipeline, Update Pipeline, View Change History, View and Change Permissions, Rediscover, Run Pipeline, and Delete Pipeline.**

***

### Event Pipeline Management Tasks

{% tabs %}
{% tab title="View Pipeline" %}
**Overview:**

The **View** option displays the pipeline details, including the nodes, connections, and configuration settings defined in the pipeline. This allows you to examine the pipeline structure and understand how the data flows without modifying the configuration.

**Procedure:**

1. On the **Left Navigation Bar**, go to **SCIKIQ CONNECT**, expand **Scikiq Event Hub**, and then click **Event Pipelines**.

<figure><img src="../../../.gitbook/assets/S (257).png" alt="" width="563"><figcaption><p>Event Pipelines Menu Item</p></figcaption></figure>

The Kafka Pipeline page displayed.

2. On the **Kafka** **Pipelines** page, click the **View** icon corresponding to the required pipeline.

<figure><img src="../../../.gitbook/assets/S (258).png" alt=""><figcaption><p>View Icon</p></figcaption></figure>

The pipeline is displayed.

<figure><img src="../../../.gitbook/assets/S (259).png" alt=""><figcaption><p>Event Pipeline</p></figcaption></figure>
{% endtab %}

{% tab title="Update Pipeline" %}
**Overview:**

The **Edit** option is used to update the pipeline by adding or removing nodes, modifying node configurations, changing data sources, or adjusting the data flow. This helps refine the pipeline to meet new requirements or correct existing configurations.

**Procedure:**

1. On the **Kafka** **Pipelines** page, click the **Edit** icon corresponding to the required pipeline.

<figure><img src="../../../.gitbook/assets/S (260).png" alt=""><figcaption><p>Edit Icon</p></figcaption></figure>

The pipeline page is displayed.

2. On the pipeline page, make **any changes**, and then click the **Save** button.

<figure><img src="../../../.gitbook/assets/S (261).png" alt=""><figcaption><p>Updating Pipeline</p></figcaption></figure>
{% endtab %}

{% tab title="View Change History" %}
**Overview:**

The **Change History** option displays a record of updates made to the pipeline, such as configuration changes, modification date, or updates to the pipeline structure. It may also show details such as the user who made the change and the time the change was made. This helps maintain transparency, track revisions, and review previous updates.

**Procedure:**

* On the **Pipelines** page, click the **Change History** icon corresponding to the required pipeline.

<figure><img src="../../../.gitbook/assets/S (262).png" alt=""><figcaption><p>Change History Icon</p></figcaption></figure>

The Resource Change Log page is displayed.

<figure><img src="../../../.gitbook/assets/S (263).png" alt=""><figcaption><p>Resource Change Log Page</p></figcaption></figure>
{% endtab %}

{% tab title="View and Change Permissions" %}
**Overview:**

You can view the permissions assigned to a pipeline, such as **Public**, **Private**, or **Shared**. Based on your requirements, you can modify the permission by selecting a different access level.

**Procedure:**

1. On the **Kafka** **Pipeline** page, click the **Permissions** icon.

<figure><img src="../../../.gitbook/assets/S (264).png" alt=""><figcaption><p>Permissions Icon</p></figcaption></figure>

The Resource Permission screen is displayed.

2. On the **Resource Permission** screen, change the permission, and then click the **Save** button.

<figure><img src="../../../.gitbook/assets/S (265).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Rediscovery" %}
**Overview:**

The Rediscover option re-fetches the latest structure or configuration details from the connected datasets, tables, APIs, or other data sources used in the pipeline.

**Procedure:**

* On the **Kafka** **Pipeline** page, click the **Rediscover** icon corresponding to the required pipeline.

<figure><img src="../../../.gitbook/assets/S (266).png" alt=""><figcaption><p>Rediscover</p></figcaption></figure>

The rediscovery process is completed, and a success message is displayed.
{% endtab %}

{% tab title="Run Pipeline" %}
**Overview:**

The **Run** button on a **Pipeline page** is used to **execute the pipeline**. Clicking **Run** starts the pipeline execution by processing the configured nodes and data flow according to the defined pipeline logic.

**Procedure:**

1. On the **Pipeline** page, click the **Run** icon.

<figure><img src="../../../.gitbook/assets/S (267).png" alt=""><figcaption><p>Run Icon</p></figcaption></figure>

The Pipeline Parameters page is displayed.

2. On the **Pipeline Parameters** page, click the **Run** button.

The **Logs Viewer** page is displayed with the **Running** status.
{% endtab %}

{% tab title="Delete Pipeline" %}
**Overview:**

The **Delete** option is used to permanently remove a pipeline and its configuration from the pipeline list. This helps maintain a clean workspace by eliminating unused, outdated, or incorrect pipelines.

**Procedure:**

1. On the **Pipelines** page, click the **Delete** icon.

<figure><img src="../../../.gitbook/assets/S (268).png" alt=""><figcaption><p>Delete Icon</p></figcaption></figure>

The Delete ETL Job message box is displayed.

2. On the **Delete ETL Job** message box, click the **Yes** button.

<figure><img src="../../../.gitbook/assets/S (269).png" alt=""><figcaption><p>Delete ETL Job Message Box</p></figcaption></figure>
{% endtab %}
{% endtabs %}

***

### **Related Topics**

* [**Creating an API Pipeline**](creating-an-api-pipeline/)
