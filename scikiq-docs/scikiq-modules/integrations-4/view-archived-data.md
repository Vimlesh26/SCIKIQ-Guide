# View Archived Data

***

**Contents**

* [**Instructions for Using this Page**](view-archived-data.md#instructions-for-using-this-page)
* [**Overview**](view-archived-data.md#overview)
* [**Procedure**](view-archived-data.md#procedure)
* [**Related Topics**](view-archived-data.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

The View Data module in SCIKIQ enables you to retrieve archived data. It also allows you to query the archived data using NLQ and SQL, and provides the capability to delete the required archived data.

***

## Procedure

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Retrieve Archived Data</strong></summary>

1.Under **SCIKIQ Archival**, expand **Archival Jobs**, and then click **View Data**.

<figure><img src="../../.gitbook/assets/image (1611).png" alt=""><figcaption><p>View Data Menu Item</p></figcaption></figure>

The Data Retrieval page is displayed.

2.2. On the **Data Retrieval** page, select the **required Data Source**, **Storage Tier, Time Range, Date Range**, and click the **Apply Filter** button.

3\. In the **Center Pane,** click the **View Sample Data** icon corresponding to the required partition.

<figure><img src="../../.gitbook/assets/image (1612).png" alt=""><figcaption><p>Data Retrieval Page</p></figcaption></figure>

The archived data is displayed.

<figure><img src="../../.gitbook/assets/image (1613).png" alt=""><figcaption><p>Archived Data</p></figcaption></figure>

</details>

<details>

<summary><strong>2.Query Archived Data Using NLQ</strong></summary>

1. tOn the **Data Retrieval** page, in the **Center Pane**, click the **Query NLQ** icon corresponding to the required partition.
2. Next, in the **Right Pane**, enter the required **query**, and then click the **Execute Query** button.

<figure><img src="../../.gitbook/assets/image (1614).png" alt=""><figcaption><p>Data Retrieval Page - NLQ Mode</p></figcaption></figure>

The required archived data is retrieved.

3. To clear the existing query, click the **Delete** button ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADQAAAAqCAYAAAD8pHgAAAACSUlEQVR4AeyZy0sbURTGvxljmlQba6WVvrCVin2hfUlpS5F20WXpolvBje4EXzvRhaDufCDiQgRBcOXCf0FEXfgO4jP42AgqaoxPokbnDAqBe8Ek3Isz8Q4cMrl3zuH3nW/mhszVz+Ps0BFnhxJkdUPj3yFjjcDcyjoGJnzoH1u0XBAX8REn725hHJpf3YAjQcf3nEzkf86yXBAX8RFnRII2d/bw8kkaEgxRvISbHiMu4iNOHgvjUCh0blkxVwJIFHFefQ//ZASFT9rxXAmyumvKoVvt0I5/DyOTM2Z4Z3wInpxK74fwW25yegGFJbVmlFU3oa2z14zG9h4Ul9eb4xU1LfAH9qWIEy7oXXYm8j68RVHBPzTXlTNBc////oYnOckeghITHXA6HUi660LAcGF4xIujo2P0D47DeTnndt2Brmv2EBROue0PYGp6EbuGsNGpWXs+Q+GCrjuXMS/8GZIBGU1NJSiabj2470Hu+yykeJLxJfeNuShEkx/LtdIcOjg8hscQ8i0vB263C/k/PpmLQjAo98dViqCMZ4/R0d2H0qpGJuZ8K0hLTYml+RHlSBH059dXdLXWcKO1oRLPn6ZHBBfLRVIExQIiKkcJEtVJWXWUQ7I6K6quckhUJ2XVUQ7J6qyouoxD9E/y7Cwkqr6UOsRHnLzijKCHqfewvLYFSuIl3PQYcREfcfJYGEHZGY9wajg05F2y3N4Q7VcRF/ERZ0SCNE3D6xfp+PnxleX2hmi/iriIT9P4L1kYh3iqacwuoQRZ3akLAAAA//+ZDtkLAAAABklEQVQDAGeoWKP6RY0CAAAAAElFTkSuQmCC) next to the Execute Query button.

</details>

<details>

<summary>3<strong>.Query Archived Data Using SQL</strong></summary>

1. On the **Data Retrieval** page, click the **SQL** button in the **Query Data** pane.
2. Next, on the **Switch Query Mode** message box, click the **Yes** button.

<figure><img src="../../.gitbook/assets/image (1615).png" alt=""><figcaption><p>Data Retrieval Page - SQL Mode</p></figcaption></figure>

&#x20;     The SQL syntax is displayed in the Query Data pane.

3. In the **Query Data pane**, enter the required  **SQL query**, and then click the **Execute SQL Query** button at the bottom.

<figure><img src="../../.gitbook/assets/image (1616).png" alt=""><figcaption><p>Data Retrieval Page - SQL Query Execution</p></figcaption></figure>

4. To clear the existing query, click the **Delete** button ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADQAAAAqCAYAAAD8pHgAAAACSUlEQVR4AeyZy0sbURTGvxljmlQba6WVvrCVin2hfUlpS5F20WXpolvBje4EXzvRhaDufCDiQgRBcOXCf0FEXfgO4jP42AgqaoxPokbnDAqBe8Ek3Isz8Q4cMrl3zuH3nW/mhszVz+Ps0BFnhxJkdUPj3yFjjcDcyjoGJnzoH1u0XBAX8REn725hHJpf3YAjQcf3nEzkf86yXBAX8RFnRII2d/bw8kkaEgxRvISbHiMu4iNOHgvjUCh0blkxVwJIFHFefQ//ZASFT9rxXAmyumvKoVvt0I5/DyOTM2Z4Z3wInpxK74fwW25yegGFJbVmlFU3oa2z14zG9h4Ul9eb4xU1LfAH9qWIEy7oXXYm8j68RVHBPzTXlTNBc////oYnOckeghITHXA6HUi660LAcGF4xIujo2P0D47DeTnndt2Brmv2EBROue0PYGp6EbuGsNGpWXs+Q+GCrjuXMS/8GZIBGU1NJSiabj2470Hu+yykeJLxJfeNuShEkx/LtdIcOjg8hscQ8i0vB263C/k/PpmLQjAo98dViqCMZ4/R0d2H0qpGJuZ8K0hLTYml+RHlSBH059dXdLXWcKO1oRLPn6ZHBBfLRVIExQIiKkcJEtVJWXWUQ7I6K6quckhUJ2XVUQ7J6qyouoxD9E/y7Cwkqr6UOsRHnLzijKCHqfewvLYFSuIl3PQYcREfcfJYGEHZGY9wajg05F2y3N4Q7VcRF/ERZ0SCNE3D6xfp+PnxleX2hmi/iriIT9P4L1kYh3iqacwuoQRZ3akLAAAA//+ZDtkLAAAABklEQVQDAGeoWKP6RY0CAAAAAElFTkSuQmCC) next to the Execute Query button.

The query is executed successfully.

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
