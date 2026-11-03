# Group Node

**Contents**

* [**Instructions for Using this Page**](group-node.md#instructions-for-using-this-page)
* [**Overview**](group-node.md#overview)
* [**Procedure**](group-node.md#procedure)
* [**Related Topics**](group-node.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]

***

## Overview

This page explains how to use the **Group node.** It aggregates data based on specified columns. It is also used to group records and apply aggregation functions to generate summarized results for analysis and reporting.

***

## Procedure

The procedure to use the Group node involves the steps including [Add Group Node,](group-node.md#add-group-node) [Add and Connect Input Nodes,](group-node.md#add-and-connect-input-nodes) [Configure Group Node Settings,](group-node.md#configure-group-node-settings) [Save Pipeline](group-node.md#save-pipeline), and [Preview Result](group-node.md#preview-result). The expandable panels below provide guided assistance for each step in the procedure.&#x20;

Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Add Group Node</strong></summary>

1. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click either **Create API Pipeline** or **Create Delta Pipeline**. For example, Create Delta Pipeline.

<figure><img src="../../../../.gitbook/assets/S.png" alt=""><figcaption><p>Create Delta Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

2. From the **Top Toolbar**, drag the **Group node** on to the **Main Workspace.**

<figure><img src="../../../../.gitbook/assets/S (313).png" alt=""><figcaption><p>Adding Group Node</p></figcaption></figure>

</details>

<details>

<summary><strong>Add and Connect Input Nodes</strong></summary>

**Procedure:**

The below step-by-step instructions describe how to select database type:

**Step-by-Step Instructions**

1. From the **Top Toolbar**, drag the required nodes, and place them inside the **Group Node**. For example, input nodes.
2. Inside the **Group Node**, connect **Input nodes.**

<figure><img src="../../../../.gitbook/assets/S (314).png" alt=""><figcaption><p>Adding and Connect  Input Nodes</p></figcaption></figure>



</details>

<details>

<summary><strong>Configure Group Node Settings</strong></summary>

**Procedure:**

The below step-by-step instructions describe how to select database type:

**Step-by-Step Instructions**

1. On the top of **Group Node**, click the **Edit** icon.

<figure><img src="../../../../.gitbook/assets/S (315).png" alt="" width="514"><figcaption><p>Group Node - Edit Icon</p></figcaption></figure>

The Group section is displayed on the left pane.

2. On the left pane, from the **Select Group Type** drop-down box, select either **Flink Window Function** or **Other.**

{% hint style="info" %}
**Tip:**&#x20;

* Selecting the **Flink Window Function** group type groups streaming data within defined **time windows** using Apache Flink window functions.
* Selecting the  **Other** group type allows the use of **custom or advanced grouping configurations** that are not covered by the standard grouping or window functions
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (316).png" alt=""><figcaption><p>Selecting Group Type</p></figcaption></figure>

</details>

<details>

<summary><strong>Save Pipeline</strong></summary>

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

<figure><img src="../../../../.gitbook/assets/S (317).png" alt="" width="563"><figcaption><p>Saving Pipeline</p></figcaption></figure>

The Pipeline is saved.

</details>

<details>

<summary><strong>Preview Result</strong></summary>

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Data Pipelines** page, click the **Edit** icon corresponding to the **Group** node.

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** Setup icon on the top right side of **Group** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (318).png" alt=""><figcaption><p>Preview Setup</p></figcaption></figure>

The preview is displayed.

</details>

## Related Topics

* [Configuring Input Nodes](/broken/pages/Qe52MzyFrHp43dWO41kf)
* [Configuring Output Nodes](/broken/pages/BOHoiMbsoFJCedoWAASx)
* [Configuring Transform Nodes](/broken/pages/hbzg9uHn194g3ivtwx4q)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
