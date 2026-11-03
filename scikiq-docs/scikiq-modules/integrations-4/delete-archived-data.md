# Delete Archived Data

***

**Contents**

* [**Instructions for Using this Page**](delete-archived-data.md#instructions-for-using-this-page)
* [**Overview**](delete-archived-data.md#overview)
* [**Procedure**](delete-archived-data.md#procedure)
* [**Related Topics**](delete-archived-data.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

Archiving preserves historical data for reference and compliance. However, based on the need, deleting it from the operational system improves performance by reducing data volume and speeding up queries. It also supports cost optimization, as primary storage is more expensive than archival storage.&#x20;

Deletion keeps the system clean and manageable by retaining only relevant data and avoiding duplication. Overall, it ensures the system remains efficient and streamlined.

***

## Procedure

The deletion process involves a series of steps. As part of this process, you must first map the required business terms in the Data Dictionary. You can then initiate a data deletion request by selecting the relevant business terms along with the applicable identifier.

Once the request is initiated and the archived table discovery is completed, you can review and confirm the deletion.

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Map Business Term</strong>s</summary>

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

&#x20;     The Meta Data Manager menu is displayed.

2. From the **Meta Data Manager** menu, click **Data Dictionary.**

<figure><img src="../../.gitbook/assets/image (1617).png" alt=""><figcaption><p>Data Dictionary Menu Item</p></figcaption></figure>

The Data Dictionary page is displayed.

3. On the **Data Dictionary** page:

* From the **Select Type** drop-down box, select **Data Source.**
* From the **Select Data Source** drop-down box, select the **connection** in which the required table is archived.
* From the **Select Table** drop-down box, select the **required archived table**, which you wish to delete.
* Click the **Search** button.

<figure><img src="../../.gitbook/assets/image (1618).png" alt=""><figcaption><p>Data Dictionary Search Filters</p></figcaption></figure>

The Table Elements are displayed on the Data Dictionary page.

4. Now, on the **Data Dictionary** page, map the **Business Term** (For example, Currency) for the required table elements, and then click the **Save Dictionary** button on the top right side of the page.

<figure><img src="../../.gitbook/assets/image (1619).png" alt=""><figcaption><p>Data Dictionary Page - Mapping Business Terms</p></figcaption></figure>

The **Data saved successfully** message is displayed.

</details>

<details>

<summary><strong>2. Initiate Data Deletion Request</strong></summary>

. 1.  On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival**.

2. Under **SCIKIQ Archival**, expand **Archival Jobs**, and then click **View Data**.

<figure><img src="../../.gitbook/assets/image (1620).png" alt=""><figcaption><p>View Data</p></figcaption></figure>

&#x20;   The Data Retrieval page is displayed.

3. On the **Data Retrieval** page, select the required **Datasource, Storage Tier, Time Range,** and then click the **Data Deletion** button.

<figure><img src="../../.gitbook/assets/image (1621).png" alt=""><figcaption><p>Data Retrieval Page</p></figcaption></figure>

The Data Deletion Request page is displayed.

</details>

<details>

<summary><strong>3.Scan Data</strong></summary>

After the completion of scanning, the **Review stepper** is highlighted.

</details>

<details>

<summary><strong>4.Review Data</strong></summary>

1. On the **Review stepper**, select the **table to be deleted**, and then click the **Proceed to Delete** button.

&#x20;     The Confirm stepper is highlighted.

2. On the **Confirm stepper,** in the **Type to Delete** field, enter **DELETE**, and then click the Delete button.

<figure><img src="../../.gitbook/assets/image (1622).png" alt=""><figcaption><p>Data Deletion Request - Review Data</p></figcaption></figure>

The Processing stepper is highlighted and the purge complete message is displayed.

</details>

<details>

<summary>5<strong>.Confirm Deletion</strong></summary>

* On the **Processing** stepper, click the **New Purge Request** button.

<figure><img src="../../.gitbook/assets/image (1623).png" alt=""><figcaption><p>Data Deletion Request - Purge</p></figcaption></figure>

Once the purge is completed, the Complete stepper is highlighted.

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
