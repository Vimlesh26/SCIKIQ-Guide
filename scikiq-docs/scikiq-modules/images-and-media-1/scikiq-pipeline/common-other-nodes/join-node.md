# Join Node

**Contents**

* [**Instructions for Using this Page**](join-node.md#instructions-for-using-this-page)
* [**Overview**](join-node.md#overview)
* [**Procedure**](join-node.md#procedure)
* [**Related Topics**](join-node.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]

***

## Overview

This page explains how to use the **Join** node while creating a pipelin&#x65;**.** It is used to combine datasets from two or more sources into a single unified view based on specified join conditions. It enables you to enrich and correlate data by joining tables using common fields or defined conditions.&#x20;

**Types of Join Nodes:**

<table><thead><tr><th width="179">Type</th><th>Purpose</th></tr></thead><tbody><tr><td>Inner Join</td><td>Returns records that have matching values in both tables.</td></tr><tr><td>Left Join</td><td>Returns all records from the left table and matching records from the right table. If there's no match, NULLs are returned from the right.</td></tr><tr><td>Right Join</td><td>Returns all records from the right table and matching records from the left. If there's no match, NULLs are returned from the left.</td></tr><tr><td>Outer Join</td><td>Returns all records when there is a match in either left or right table.</td></tr></tbody></table>

***

## Procedure

The procedure to use the Join node involves the steps including [Connect Join Node to Input Nodes](join-node.md#connect-join-node-to-input-nodes), [Configure Condition](join-node.md#configure-condition), [Select Columns](join-node.md#select-columns), [Save Pipeline](join-node.md#save-pipeline), and [Preview Result](join-node.md#preview-result). The expandable panels below provide guided assistance for each step in the procedure.&#x20;

Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Connect Join Node to Input Nodes</strong> </summary>

1. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click either **Create API Pipeline** or **Create Delta Pipeline**. For example, Create Delta Pipeline.

<figure><img src="../../../../.gitbook/assets/S.png" alt=""><figcaption><p>Create Delta Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

2. On the **Right Bane**, add **two input nodes**. For example, Database input nodes.
3. Now, from the **Top Toolbar** drag the **Join node** on to the **Main Workspace,** and connect it to the input nodes.

<figure><img src="/broken/files/Ec7Z2pyPRARcsTCPbgZw" alt=""><figcaption><p>Connecting Join Node</p></figcaption></figure>

The Join section is displayed on the left pane.&#x20;

</details>

<details>

<summary><strong>Configure Condition</strong></summary>

**Purpose:**

The **purpose of configuring a condition when connecting the Join node with input nodes** is to **define how records from the input datasets should be matched and combined**. The condition specifies the **relationship between columns in the input sources**, ensuring that only the relevant records are joined together.

**Procedure:**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Left Pane**, click the **Add** **Join** button.

<figure><img src="/broken/files/hutPd189ElL3mU6helHa" alt=""><figcaption><p>Add Join Button</p></figcaption></figure>

The Join dialogue-box is displayed.

2. On the **Join** dialogue-box (See the below image), from the **Join Type** dialogue-box, select the required **join type** choosing from **Inner, Left, Right,** or **Outer.**
3. From the drop-down box under **And/Or**, select the required **column**.&#x20;

The condition is displayed.

{% hint style="info" %}
**Tip:** To add more rules, click the **Add Rule** button.
{% endhint %}

2. Click the **Save** button.

<figure><img src="/broken/files/cxp8nQzW9Iutr5macyNx" alt=""><figcaption><p>Configuring Condition</p></figcaption></figure>

</details>

<details>

<summary><strong>Select Columns</strong></summary>

**Purpose:**

The **purpose** of selecting columns when connecting the Join node with input nodes is to specify which fields from the input datasets should be included in the final joined output.

**Procedure:**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Left Pane**, in the **Join** section, click the **Columns** tab.

The list of columns is displayed.

2. From the **list of columns**, select the **required columns**.

<figure><img src="/broken/files/bJu0jV8r04MHZ2tPxFVW" alt=""><figcaption><p>Selecting Columns</p></figcaption></figure>

</details>

<details>

<summary><strong>Save Pipeline</strong></summary>

**Purpose**

The **purpose** of saving the pipeline while connecting the Join node with input nodes is to store the configured pipeline structure and settings so that the join configuration and node connections are preserved and can be executed later.

**Procedure**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="/broken/files/lxi4A0PNIFwy0lIYOtth" alt="" width="563"><figcaption><p>Saving Pipeline</p></figcaption></figure>

The Pipeline is saved.

</details>

<details>

<summary><strong>Preview Result</strong></summary>

**Overview:**

The **purpose** of previewing the result while connecting the Join node with input nodes is to verify that the join configuration is correct and that the data from the input datasets is combined as expected before running the entire pipeline.

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Data Pipelines** page, click the **Edit** icon corresponding to the **Join** node.

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **Join** nod&#x65;**.**

<figure><img src="/broken/files/GEGaNfEj5AqeTxrjJc8P" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

The result is displayed on the Preview tab. See the example image below:

<figure><img src="/broken/files/1H21Z9CPcTwBdiIokPci" alt=""><figcaption><p>Preview Result</p></figcaption></figure>

</details>

## Related Topics

* [Configuring Input Nodes](/broken/pages/Qe52MzyFrHp43dWO41kf)
* [Configuring Output Nodes](/broken/pages/BOHoiMbsoFJCedoWAASx)
* [Configuring Transform Nodes](/broken/pages/hbzg9uHn194g3ivtwx4q)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
