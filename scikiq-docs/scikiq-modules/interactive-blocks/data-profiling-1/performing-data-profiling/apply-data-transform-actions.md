---
hidden: true
icon: page
---

# Apply Data Transform Actions

***

**Contents**

* [**Instructions for Using this Page**](apply-data-transform-actions.md#instructions-for-using-this-page)
* [**Overview**](apply-data-transform-actions.md#overview)
* [**Procedure**](apply-data-transform-actions.md#procedure)
* [**Related Topics**](apply-data-transform-actions.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## **Overview**

The **Data Transformations** enable you to clean, modify, and prepare your dataset for analysis. You can filter records, rename, duplicate, or remove columns, treat missing values using various techniques, and identify or handle outliers. These transformations help improve data quality, consistency, and reliability before performing exploratory data analysis or downstream processing.

> <mark style="color:red;">**Note**</mark>: You are not required to apply all of these transformations. Select and apply only the operations that best meet your data preparation and business requirements.

***

## Procedure

Expand the below panels to view step-by-step instructions:

<details>

<summary><strong>Rename Column</strong></summary>

**Overview**

The need to **rename a column** during **data profiling** arises when the existing column name is unclear, inconsistent, incorrect, or does not follow organizational naming standards. Renaming columns makes the dataset easier to understand, analyze, and maintain.

The below Procedure section help you understand how to rename a column:

**Procedure**

1. On the **EDA** tab, select the **required column.**
2. On the selected column, click the **Menu** button.

The drop-down menu is displayed.

3. From the drop-down menu, select **Rename Column**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2472).png" alt=""><figcaption></figcaption></figure>

The **Rename Column** dialogue box is displayed.

4. On the **Rename Column** dialogue box, enter a **new name** for the column, and then click the **Submit** button.

<figure><img src="../../../../.gitbook/assets/image (2473).png" alt=""><figcaption></figcaption></figure>

The column is renamed.

<figure><img src="../../../../.gitbook/assets/image (2474).png" alt=""><figcaption></figcaption></figure>



</details>

<details>

<summary><strong>Duplicate Column</strong></summary>

**Overview**

The need to **duplicate a column** during **Exploratory Data Analysis (EDA)** arises when you want to preserve the original data while creating a copy that can be modified or analyzed independently. This allows you to experiment with transformations without affecting the source values.

The below Procedure section help you understand how to duplicate a column:

**Procedure**

1. On the **EDA** tab, select the **required column.**
2. On the selected column, click the **Menu** button.

The drop-down menu is displayed.

3. From the drop-down menu, select **Duplicate Column** under **Data Transform**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2475).png" alt=""><figcaption></figcaption></figure>

The selected column is duplicated. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2476).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Delete Row with Missing Value</strong></summary>

**Overview**

The **Delete Row with Missing Value** transformation removes rows that contain one or more missing (null or empty) values. It is useful when incomplete records could affect the accuracy and reliability of data analysis.

The below Procedure section help you understand how to delete rows with missing values:

**Procedure**

1. On the **EDA** tab, select the **required column.**
2. On the selected column, click the **Menu** button.

The drop-down menu is displayed.

3. From the drop-down menu, select **Delete Row with Missing Value** under **Data Transform**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2477).png" alt=""><figcaption></figcaption></figure>

The rows with missing values are deleted.

</details>

<details>

<summary><strong>Fill with Mean (Numeric)</strong></summary>

**Overview**

The **Fill with Mean (Numeric)** is a data transformation technique used to replace missing values in a **numeric column** with the **mean (average)** of the existing values in that column. It is a common method of handling missing data without deleting records.

The below Procedure section help you understand how to use the **Fill with Mean (Numeric)** transformation:

**Procedure**

1. On the **EDA** tab, select the **required column.**
2. On the selected column, click the **Menu** button.

The drop-down menu is displayed.

3. From the drop-down menu, select **Fill with Mean (Numeric)** under **Data Transform**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2478).png" alt=""><figcaption></figcaption></figure>

The missing values  are replaced in a **numeric column** with the **mean (average)** of the existing values in the selected column.

</details>

<details>

<summary><strong>Fill with Mode (Categorical)</strong></summary>

**Overview**

The **Fill with Mode (Categorical)** is a data transformation technique used to replace missing values in a **categorical column** with the **mode**, which is the most frequently occurring value in that column. It helps preserve all records while improving data completeness.

The below Procedure section help you understand how to use the **Fill with Mode (Categorical)** data transformation:

**Example**

The following example illustrates how a missing value is replaced by the most frequently occurring value after applying the **Fill with Mode (Categorical)** transformation:

| Before transformation | After applying Fill with Mode (Categorical) |
| --------------------- | ------------------------------------------- |
| Sales                 | Sales                                       |
| HR                    | HR                                          |
| (Missing)             | Sales                                       |
| Sales                 | Sales                                       |

**Procedure**

1. On the **EDA** tab, select the **required column.**
2. On the selected column, click the **Menu** button.

The drop-down menu is displayed.

3. From the drop-down menu, select **Fill with Mode (Categorical)** under **Data Transform**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2479).png" alt=""><figcaption></figcaption></figure>

The missing values  are replaced in a categorical column with the most frequently occurring value (mode) in that column.

</details>

<details>

<summary><strong>Last Observation Carried Forward (LOCF)</strong></summary>

**Overview**

The **Last Observation Carried Forward (LOCF)** is a data transformation technique used to fill missing values by copying the **most recent non-missing value** from the same column. It is commonly used for **time-series** and **sequential data**, where the previous value is assumed to remain valid until a new value is available.

The below Procedure section help you understand how to use the **Last Observation Carried Forward (LOCF)** data transformation:

**Example**

The following example illustrates how a missing value is filled with the most **most recent non-missing value** from the same column:

_**Before Transformation**_

| Date        | Temperature |
| ----------- | ----------- |
| 01-Jul-2026 | 28          |
| 02-Jul-2026 | Missing     |
| 03-Jul-2026 | Missing     |
| 04-Jul-2026 | 30          |
| 05-Jul-2026 | Missing     |

_**After**_ _**Transformation**_

| Date        | Temperature |
| ----------- | ----------- |
| 01-Jul-2026 | 28          |
| 02-Jul-2026 | 28          |
| 03-Jul-2026 | 28          |
| 04-Jul-2026 | 30          |
| 05-Jul-2026 | 30          |

**Procedure**

1. On the **EDA** tab, select the **required column.**
2. On the selected column, click the **Menu** button.

The drop-down menu is displayed.

3. From the drop-down menu, select **Last Observation Carried Forward (LOCF)** under **Data Transform**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2481).png" alt=""><figcaption></figcaption></figure>



The missing values  are replaced with the **most recent non-missing value** from the same column.

</details>

<details>

<summary><strong>Forward Fill</strong></summary>

**Overview**

The **Forward Fill** is a data transformation technique that replaces missing values in a column with the **most recent non-missing value** that **appears above them**. It is commonly used to fill gaps in sequential or ordered data while preserving all records in the dataset.

**Example**

The following example illustrates how the missing values are filled with the **most recent non-missing value** that **appears above them**:

_**Before Transformation**_

| Date        | Temperature |
| ----------- | ----------- |
| 01-Jul-2026 | Active      |
| 02-Jul-2026 | Missing     |
| 03-Jul-2026 | Missing     |
| 04-Jul-2026 | Inactive    |
| 05-Jul-2026 | Missing     |

_**After**_ _**Transformation**_

| Date        | Temperature |
| ----------- | ----------- |
| 01-Jul-2026 | Active      |
| 02-Jul-2026 | Active      |
| 03-Jul-2026 | Active      |
| 04-Jul-2026 | Inactive    |
| 05-Jul-2026 | Inactive    |

**Procedure**

The below Procedure section help you understand how to use the **Forward Fill** data transformation:

1. On the **EDA** tab, select the **required column.**
2. On the selected column, click the **Menu** button.

The drop-down menu is displayed.

3. From the drop-down menu, select **Forward Fill** under **Data Transform**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2481).png" alt=""><figcaption></figcaption></figure>

The missing values  are replaced with the with the most recent non-missing value that appears above them.

</details>

<details>

<summary> <strong>Interpolate (Time Series)</strong></summary>

**Overview**

The **Interpolate (Time Series)** is a data transformation technique that estimates and fills missing values in a **time-series dataset** based on the values before and after the missing data. Unlike **Forward Fill** or **LOCF**, which simply copy the previous value, interpolation calculates a new value that follows the trend of the data.

The below Procedure section help you understand how to use the **Interpolate (Time Series)** data transformation:

**Example**

The following example illustrates how the missing values are filled with the **most recent non-missing value** that **appears above them**:

_**Before Transformation**_

| Date        | Temperature |
| ----------- | ----------- |
| 01-Jul-2026 | 20          |
| 02-Jul-2026 | Missing     |
| 03-Jul-2026 | 24          |

_**After**_ _**Transformation**_

| Date        | Temperature |
| ----------- | ----------- |
| 01-Jul-2026 | 20          |
| 02-Jul-2026 | 22          |
| 03-Jul-2026 | 24          |

**Procedure**

1. On the **EDA** tab, select the **required column.**
2. On the selected column, click the **Menu** button.

The drop-down menu is displayed.

3. From the drop-down menu, select **Interpolate (Time Series)** under **Data Transform**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2483).png" alt=""><figcaption></figcaption></figure>

The missing values  are replaced with the with the most recent non-missing value that appears above them.

</details>

<details>

<summary><strong>Regression</strong></summary>

**Overview**

**Regression** estimates missing numeric values by analyzing the relationship between the selected column and other relevant columns in the dataset. This transformation provides more accurate value estimates than simple replacement methods, helping improve data quality and prepare the dataset for advanced analysis and machine learning.

The below Procedure section help you understand how to use the **Regression** data transformation:

**Example**

The following example illustrates how the missing values are filled with the **most recent non-missing value** that **appears above them**:

_**Before Transformation**_

| Experience (Years) | Salary  |
| ------------------ | ------- |
| 2                  | 30,000  |
| 4                  | 45,000  |
| 6                  | Missing |
| 8                  | 70,000  |

_**After**_ _**Transformation**_

| Experience (Years) | Salary             |
| ------------------ | ------------------ |
| 2                  | 30,000             |
| 4                  | 45,000             |
| 6                  | 57,500 (Estimated) |
| 8                  | 70,000             |

**Procedure**

1. On the **EDA** tab, select the **required column.**
2. On the selected column, click the **Menu** button.

The drop-down menu is displayed.

3. From the drop-down menu, select **Regression** under **Data Transform**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2485).png" alt=""><figcaption></figcaption></figure>

The missing values  are replaced.

</details>

<details>

<summary><strong>Cap Outliers</strong></summary>

**Overview**

**Cap Outliers** is a data transformation technique that limits extreme values (outliers) by replacing them with predefined upper and lower threshold values. Instead of deleting outliers, the transformation retains the records while reducing the influence of unusually high or low values.

The below Procedure section help you understand how to use the **Cap Outliers** data transformation:

**Example**

Suppose the acceptable salary range is between **₹30,000** and **₹100,000**.

_**Before Transformation**_

| Employee | Salary            |
| -------- | ----------------- |
| A        | 35,000            |
| B        | 42,000            |
| C        | 500,000 (Outlier) |
| D        | 28,000 (Outlier)  |

_**After**_ _**Transformation**_

| Employee | Salary   |
| -------- | -------- |
| A        | 35,000   |
| B        | 42,000   |
| C        | 100,000  |
| D        | 30,000   |

**When to Use**

You can use it when:

* The dataset contains extreme values that could distort analysis.
* You want to retain all records while limiting the influence of outliers.
* The outliers are likely caused by data entry errors or rare events.
* The data is intended for statistical analysis, reporting, or machine learning.

**Procedure**

1. On the **EDA** tab, select the **required column.**
2. On the selected column, click the **Menu** button.

The drop-down menu is displayed.

3. From the drop-down menu, select **Cap Outliers** under **Data Transform**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2487).png" alt=""><figcaption></figcaption></figure>

The outliers are replaced.

</details>

***

## Related Topics

* [**Apply** **Table Transformations**](apply-table-transformations.md)
* [**Use AI Suggestions**](use-ai-suggestions.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
