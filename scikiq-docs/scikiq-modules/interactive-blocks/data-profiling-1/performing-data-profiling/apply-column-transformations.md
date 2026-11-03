---
hidden: true
icon: page
---

# Apply Column Transformations

***

**Contents**

* [**Instructions for Using this Page**](apply-column-transformations.md#instructions-for-using-this-page)
* [**Overview**](apply-column-transformations.md#overview)
* [**Procedure**](apply-column-transformations.md#procedure)
* [**Related Topics**](apply-column-transformations.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## **Overview**

As part of column transformations, you can apply various operations to cleanse, modify, secure, and prepare your data for analysis. These operations include [**Data Cleansing**](apply-column-transformations.md#data-cleansing), [**Delete Columns**](apply-column-transformations.md#deleting-columns),[ **Data Masking**](apply-column-transformations.md#data-masking), [**Calculate String Length**,](apply-column-transformations.md#calculating-string-length) [**Change Date Format**,](apply-column-transformations.md#changing-date-format) and [**Data Anonymization**](apply-column-transformations.md#applying-data-anonymization).

> <mark style="color:red;">**Note**</mark>: You are not required to apply all of these transformations. Select and apply only the operations that best meet your data preparation and business requirements.

***

## Procedure

Expand the below panels to view step-by-step instructions:

<details>

<summary><strong>Data Cleansing</strong> </summary>

**Overview**

The **Data Cleansing** feature enables you to populate empty or missing cells in a dataset with a specified value. Filling missing values helps improve data completeness and ensures the dataset is ready for accurate analysis and further processing.

In the SCIKIQ application, the **Data Cleansing** feature provides the following data cleansing options:

* **Fill values** – Populate empty or missing cells in a column with a specified value.
* **Replace column values** – Replace the existing values in a column with the values from another column.
* **Fill empty cells with above** - Populates empty cells in a column with the value from the nearest non-empty cell above.

The below Procedure section help you understand how to perform all of these tasks.

**Procedure**

1. **Filling Missing Values**

A. On the **EDA** tab, select the **table connection** and **table.**

B. On the **Column** tab, select the required column, and then in the **Data Cleansing** section, click the **Fill cell with value** pane.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2456).png" alt=""><figcaption></figcaption></figure>

The **Fill cell with value** pane is expanded by displaying **Use with** drop-down box and **Value** fields.

C. In the **Fill cell with value** pane:

A. From the **Use with** drop-down box, select the **Values** option.

B. In the **Value** field, enter the **required value**. For example, 0.

C. Click the **Submit** button.

<figure><img src="../../../../.gitbook/assets/image (2457).png" alt=""><figcaption></figcaption></figure>

The values in the selected are changed as per the specified value. See the below image. All the values are changed as 0.

<figure><img src="../../../../.gitbook/assets/image (2458).png" alt=""><figcaption></figcaption></figure>

***

2. **Replace Values Using Another Column**

In the **Fill cell with value** pane:

A. From the **Use with** drop-down box, select the **Other** **Column** option.

B. From the **Columns** drop-down box, select the **required column**. For example, contact\_id.

C. Click the **Submit** button.

<figure><img src="../../../../.gitbook/assets/image (2459).png" alt=""><figcaption></figcaption></figure>

The existing values are replaced with the values of the selected column. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2460).png" alt=""><figcaption></figcaption></figure>

***

3. **Fill empty cells with above**

* On the **Column** tab, select the empty cell in the required column, and then in the **Data Cleansing** section, click the **Fill empty cells with above** pane.

<figure><img src="../../../../.gitbook/assets/image (2461).png" alt=""><figcaption></figcaption></figure>

The empty cell is filled with the value of above cell.

<figure><img src="../../../../.gitbook/assets/image (2462).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Deleting Columns</strong></summary>

**Overview**

The purpose of **deleting columns in EDA (Exploratory Data Analysis)** is to remove columns that are not needed for analysis or further processing. This helps simplify the dataset, improve performance, and focus on relevant information.

**Procedure**

The below instructions help you understand how to delete a column:

1. On the **EDA** tab, select the required column, and then select **Delete Columns** in the left pane.

<figure><img src="../../../../.gitbook/assets/image (2463).png" alt=""><figcaption></figcaption></figure>

The selected column is deleted, and the action is recorded under **History** in the left pane. See the below image.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2402).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> If you want to restore the column again, click the ![](<../../../../.gitbook/assets/image (2403).png>) button next to the **Delete Column** in the **History**. See the above image.

</details>

<details>

<summary><strong>Data Masking</strong> </summary>

**Overview**

The purpose of **data masking** is to protect sensitive or confidential information by hiding the original values while preserving the overall structure and usability of the data. Depending on the requirement, you can use any of the below mentioned masking types:

<table><thead><tr><th width="110.77777099609375" valign="top">Masking Type</th><th valign="top">Description</th><th valign="top">Example</th><th valign="top">When to use</th></tr></thead><tbody><tr><td valign="top">Auto</td><td valign="top">Automatically applies a predefined masking rule based on the data type or detected content</td><td valign="top">Automatically masking email addresses, phone numbers, credit card numbers, or national identification numbers without requiring manual configuration</td><td valign="top"><p></p><ul><li>You want to quickly mask common sensitive data.</li><li>The application can automatically identify the data type.</li><li>Default masking rules meet your requirements</li></ul></td></tr><tr><td valign="top">Custom</td><td valign="top">Allows you to define how the selected column should be masked</td><td valign="top"> For example, masking a phone number  9********9</td><td valign="top"><p></p><ul><li>You need greater control over the masking format.</li><li>Different columns require different masking rules.</li></ul></td></tr><tr><td valign="top">Protegrity</td><td valign="top">Applies enterprise masking policies using Protegrity to ensure consistent protection of sensitive data across the organization</td><td valign="top"></td><td valign="top"><p></p><ul><li>Your organization uses Protegrity for enterprise data security.</li><li>Masking policies must be managed centrally.</li><li>You need consistent protection across multiple applications and data platforms.</li></ul></td></tr></tbody></table>

**Procedure**

The below instructions help you understand how to mask a column:

_**To mask a column**_

1. On the **EDA** tab, select the **required column.**
2. On the **Left Pane**, in the **Data Masking** section, select **Mask Data.**

<figure><img src="../../../../.gitbook/assets/image (2385).png" alt=""><figcaption></figcaption></figure>

The **Data Masking Types list** is displayed.

3. &#x20;From the **Data Masking Types** list, select the required **type**. For example, Custom.
4. Specify the **First Character, Last Character**, and then click the **Submit** button.

<figure><img src="../../../../.gitbook/assets/image (2388).png" alt=""><figcaption></figcaption></figure>

The data in the selected columns are configured.

<figure><img src="../../../../.gitbook/assets/image (2389).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Calculating String Length</strong></summary>

**Overview**

The **Calculate Length** feature is used to determine the number of characters in the values of a selected column. This information helps users analyze the data, validate field lengths, and identify values that may be too short, too long, or inconsistent.

**Procedure**

The below instructions help you understand how to calculate string length:

_**To calculate string length**_

1. On the **EDA** tab, select the **required column.**
2. On the **Left Pane**, in the **Strings** section, select **Calculate length.**

The string length is displayed. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2391).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Changing Date Format</strong></summary>

**Overview**

The **Change Date Format** feature is used to convert date values from one format to another without changing the actual date. It helps standardize date formats across a dataset, making the data easier to read, analyze, and integrate with other systems.

**Procedure**

The below instructions help you understand how to change date format:

_**To change date format**_

1. On the **EDA** tab, select the **required column.**
2. On the **Left Pane**, in the **Date** section, select **Change Date Format,**

<figure><img src="../../../../.gitbook/assets/image (2392).png" alt=""><figcaption></figcaption></figure>

The **Select Date Format** drop-down box is displayed.

3. From the **Select Date Format** drop-down box, select the required **date format.** For example, dd/mm/yy.
4. Click the **Submit** button.

<figure><img src="../../../../.gitbook/assets/image (2396).png" alt=""><figcaption></figcaption></figure>

The date format is changed as per the selected format. See the image below:

<figure><img src="../../../../.gitbook/assets/image (2395).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Applying Data Anonymization</strong></summary>

**Overview**

**Data Anonymization** is the process of permanently transforming or removing sensitive information from a dataset so that individuals or entities cannot be identified. Unlike data masking, anonymized data cannot be restored to its original form.

**When to use**

You can use data anonymization to:

* Protect personally identifiable information (PII) and sensitive data.
* Prevent the identification of individuals from the dataset.
* Safely share data for analysis, testing, or research.
* Comply with data privacy regulations and organizational security policies.
* Reduce the risk of unauthorized access to confidential information.

**Example**

Original Data (John Smith) - Anonymized Data (\*\*\*\*\*\*\*\*)&#x20;

**Procedure**

The below instructions help you understand how to use data anonymization:

_**To use data anonymization**_

1. On the **EDA** tab, select the **required column.** For example, customer\_name. See the below image.
2. On the **Left Pane**, select **Anonymize Data**.

<figure><img src="../../../../.gitbook/assets/image (2397).png" alt=""><figcaption></figcaption></figure>

The data is anonimyzed in the selected column. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2398).png" alt=""><figcaption></figcaption></figure>

</details>

***

## Related Topics

* [**Apply** **Table Transformations**](apply-table-transformations.md)
* [**Use AI Suggestions**](use-ai-suggestions.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
