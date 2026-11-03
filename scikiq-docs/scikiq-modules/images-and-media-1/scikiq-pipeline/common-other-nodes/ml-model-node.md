# ML Model Node

**Contents**

* [**Instructions for Using this Page**](ml-model-node.md#instructions-for-using-this-page)
* [**Overview**](ml-model-node.md#overview)
* [**Procedure**](ml-model-node.md#procedure)
* [**Related Topics**](ml-model-node.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]

***

## Overview

This page explains how to use the **ML Model** nod&#x65;**.** The **ML Model Node** integrates machine learning models into ETL pipelines to perform predictions, classifications, and other intelligent data operations. It enables the pipeline to process data using trained machine learning models and generate analytical outputs.

***

## Procedure

The procedure to use the **ML Model** node involves the steps including [Add and Connect ML Model Node](ml-model-node.md#add-and-connect-ml-model-node), [Configure ML Model Node Settings](ml-model-node.md#configure-ml-model-node-settings), [Save Pipeline](ml-model-node.md#save-pipeline), and [Preview Result](ml-model-node.md#preview-result). The expandable panels below provide guided assistance for each step in the procedure.&#x20;

Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Add and Connect ML Model Node</strong></summary>

1. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click either **Create API Pipeline** or **Create Delta Pipeline**. For example, Create Delta Pipeline.

<figure><img src="../../../../.gitbook/assets/S.png" alt=""><figcaption><p>Create Delta Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

2. From the **Top Toolbar**, drag the **ML Model node** on to the **Main Workspace.**
3. Connect the **ML Model node** to the input nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (310).png" alt=""><figcaption><p>Connecting ML Model Node</p></figcaption></figure>

Once connected, the ML Model section is displayed on the left pane.

</details>

<details>

<summary><strong>Configure ML Model Node Settings</strong></summary>

**Procedure:**

The below step-by-step instructions describe how to select database type:

**Step-by-Step Instructions**

1. On the **Left Pane,** from the **Select Model** drop-down box, select the **required ML model.**

The **ML Model Columns** section is displayed.

2. In the **ML Model Columns** section, select the **Target Columns** and **Source Columns**.
3. Click the **Test** button.

<figure><img src="../../../../.gitbook/assets/S (311).png" alt=""><figcaption><p>Configure ML Model Settings</p></figcaption></figure>

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

<figure><img src="../../../../.gitbook/assets/S (312).png" alt="" width="563"><figcaption><p>Saving Pipeline</p></figcaption></figure>

The Pipeline is saved.

</details>

<details>

<summary><strong>Preview Result</strong></summary>

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Data Pipelines** page, click the **Edit** icon corresponding to the **ML Model** node.

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **ML Model** nod&#x65;**.**

The preview is displayed.

</details>

## Related Topics

* [Configuring Input Nodes](/broken/pages/Qe52MzyFrHp43dWO41kf)
* [Configuring Output Nodes](/broken/pages/BOHoiMbsoFJCedoWAASx)
* [Configuring Transform Nodes](/broken/pages/hbzg9uHn194g3ivtwx4q)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
