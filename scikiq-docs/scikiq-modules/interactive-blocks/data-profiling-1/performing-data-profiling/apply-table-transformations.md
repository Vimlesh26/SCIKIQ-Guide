---
hidden: true
icon: page
---

# Apply Table Transformations

***

**Contents**

* [**Instructions for Using this Page**](apply-table-transformations.md#instructions-for-using-this-page)
* [**Overview**](apply-table-transformations.md#overview)
* [**Procedure**](apply-table-transformations.md#procedure)
* [**Related Topics**](apply-table-transformations.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## **Overview**

Deleting [**empty Rows**,](apply-table-transformations.md#deleting-empty-rows) [**duplicate rows**](apply-table-transformations.md#removing-duplicate-rows), and [**white space**](apply-table-transformations.md#removing-white-space) is an important part of **data profiling and data preparation** because these issues can affect the accuracy, consistency, and reliability of data analysis. Although data profiling is primarily used to understand the quality of data, these transformations help improve the dataset based on the issues identified during profiling..

> <mark style="color:red;">**Note**</mark>: You are not required to apply all of these transformations. Apply only the operations that are relevant to your data preparation and business requirements.

***

## Procedure

Expand the below panels to view step-by-step instructions:

<details>

<summary><strong>Deleting Empty Rows</strong> </summary>

**Overview**

The **Delete Empty Rows** feature removes rows that do not contain any data from the dataset. Removing empty rows helps eliminate unnecessary records, improve data quality, and ensure that the dataset is ready for accurate analysis and further processing.

**Procedure**

The below Procedure section help you understand how to delete empty rows as part of table transformation:

1. On the **EDA** tab, select **Table** in the **Left Pane**.

The Table Operations are displayed.

2. From the **Table Operations**, select **Delete empty row**.

<figure><img src="../../../../.gitbook/assets/image (2399).png" alt=""><figcaption></figcaption></figure>

The empty rows are deleted from the table on the right pane.

</details>

<details>

<summary><strong>Removing Duplicate Rows</strong></summary>

**Overview**

The **Remove Duplicate Rows** feature identifies and removes duplicate records from the dataset. This helps maintain data integrity, improves the accuracy of analysis and reporting, and ensures that each record is represented only once.

**Procedure**

The below Procedure section help you understand how to remove duplicate rows as part of table transformation:

1. On the **EDA** tab, select **Table** in the **Left Pane**.

The Table Operations are displayed.

2. From the **Table Operations**, select **Remove duplicate row**.

<figure><img src="../../../../.gitbook/assets/image (2400).png" alt=""><figcaption></figcaption></figure>

The duplicate rows are deleted from the table on the right pane.

</details>

<details>

<summary><strong>Removing White Space</strong> </summary>

**Overview**

The **Remove White Space** feature removes unnecessary leading and trailing spaces from text values in a dataset. This helps standardize data, improves consistency, and prevents errors during searching, filtering, sorting, and data matching.

**Procedure**

The below Procedure section help you understand how to remove white space as part of table transformation:

1. On the **EDA** tab, select **Table** in the **Left Pane**.

The Table Operations are displayed.

2. From the **Table Operations**, select **Remove white space**.

<figure><img src="../../../../.gitbook/assets/image (2401).png" alt=""><figcaption></figcaption></figure>

The white space is removed from the rows in the table on the right pane.

</details>

***

## Related Topics

* [**Apply Column Transformations**](apply-column-transformations.md)
* [**Use AI Suggestions**](use-ai-suggestions.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
