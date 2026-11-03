# Table classification

**Contents**

* [**Instructions for Using this Page**](table-classification.md#instructions-for-using-this-page)
* [**Overview**](table-classification.md#overview)
* [**Procedure**](table-classification.md#procedure)
* [**Related Topics**](table-classification.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

Table classification helps identify which tables contain archival data by analyzing factors such as data age, usage frequency, and business relevance. It enables organizations to distinguish between active and historical data, ensuring that only appropriate tables are selected for archival.&#x20;

This structured identification improves the efficiency of the archival process and prevents unnecessary data movement. As a result, it supports better storage management, system performance, and compliance with data retention policies.

***

## Procedure

Table classification can be configured in two methods: Auto Table Classification and Manual Table Classification.&#x20;

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Auto Table Classification</strong></summary>

The Auto Table Classification can be configured by enabling the **Table Classification** checkbox in the **Discovery** step while connecting SCIKIQ to the datasource.

<figure><img src="../../../.gitbook/assets/image (209).png" alt=""><figcaption></figcaption></figure>

&#x20;                                                   Table Classification Checkbox

<mark style="color:red;">**Note:**</mark> For more information on **Discovery** step, refer to [Creating a New Data Source Connection](/broken/pages/Ga8WoiowoXOkY4RtBNpS).

</details>

<details>

<summary>2.<strong>Manual Table Classification</strong></summary>

**Overview:**

The process of Manual Table Classification involves the steps, which include:&#x20;

* Access Table Classification Page
* Verify Total Classes Count
* Verify Total Classified Tables count from the UI&#x20;

The procedure below provides step-by-step instructions for completing Manual Table Classification.

**Procedure:**

**Access Table Classification Page**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control.**
2. Expand **Metadata Manager,** and then click **Table Classification**.

The Table Classification page is displayed in the right pane, showing the total number of classes and the total number of classified tables. See the below image.

**Verify Total Classes Count**

To verify the Total Classes count

* check the database table daas\_class.

**Verify Total Classified Tables count using UI**

1. On the **Table Classification** screen, from the **Data Source** drop-down box, select the **source connection**.
2. From the **Class** drop-down box, select the class.

<figure><img src="../../../.gitbook/assets/image (210).png" alt=""><figcaption></figcaption></figure>

&#x20;                                                       Table Classification fields

The tables pertaining to the selected class are displayed.

</details>

***

## Related Topics

* [Connect SCIKIQ to Source Database](/broken/pages/1miPFvCEFxfy7uZat3C4)
* [Configure Table Classification](/broken/pages/fy1vjHIN7Nys8uAuddaO)
* [Create Compliance Framework](/broken/pages/J0o8JvIQ5NXn822xZNDA)
* [Create Compliance Policy](/broken/pages/5gBXOCk95Uv7C11YfBLO)
* [Configure AWS Setup](/broken/pages/26PZ6KCui7ZjC3abzdND)
* [Create Archival Job](/broken/pages/54s7haLhTK625sePPPzh)
* [Setup Deployment Platform](/broken/pages/qpdRebf35FBbmvMZlRTo)
* [Deploy Archival Job](/broken/pages/hEN0BpaQWg865JKIDrtG)
* [Manage Deployment Configurations](/broken/pages/ctJKSQVRrDMRLHYUvlWy)
* [Validate Archived Data](/broken/pages/RWHaxNCgJded7Q8xd9FP)
* [View Archived Data](/broken/pages/6xWaChqxS1moikwvFJk7)
* [Delete Archived Data](/broken/pages/oXzQfmDzcrDAFOL2TO5w)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
