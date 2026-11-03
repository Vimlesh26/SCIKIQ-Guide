---
hidden: true
icon: page
---

# Apply Column Data Type Actions

***

**Contents**

* [**Instructions for Using this Page**](apply-column-data-type-actions.md#instructions-for-using-this-page)
* [**Overview**](apply-column-data-type-actions.md#overview)
* [**Procedure**](apply-column-data-type-actions.md#procedure)
* [**Related Topics**](apply-column-data-type-actions.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## **Overview**

The **Column Data Type Actions** menu enables you to convert the data type of a selected column to **Numeric**, **Integer**, **Decimal**, **Text**, **Date**, or **Date Time** based on your requirements. It also provides the option to remove unwanted columns, helping you improve data consistency and prepare the dataset for analysis.

> <mark style="color:red;">**Note**</mark>: You are not required to apply all of these transformations. Select and apply only the operations that best meet your data preparation and business requirements.

***

## Procedure

Expand the below panels to view step-by-step instructions:

<details>

<summary><strong>Set as Numeric</strong> </summary>

**Overview**

The **Set as Numeric** action converts the selected column to a numeric data type. Use this option when a column contains numeric values stored as text or another data type and needs to be used for calculations, statistical analysis, reporting, or data visualization.

The below Procedure section help you understand how to use **Set as Numeric** action:

**Procedure**

1. On the **EDA** tab, select the **required column.**
2. On the selected column, click the **Menu** button.

The drop-down menu is displayed.

3. From the drop-down menu, select **Set as Numeric**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2442).png" alt=""><figcaption></figcaption></figure>

A new column is generated transforming the text column into an integer column.

</details>

<details>

<summary><strong>Set as Integer</strong> </summary>

**Overview**

**Set as Integer** converts the selected column to an integer data type by storing values as whole numbers without decimal places. Use this option for columns that represent counts, quantities, or other whole-number values to ensure accurate calculations and consistent data processing.

Examples of columns that are commonly stored as integers include:

* Age
* Quantity
* Number of Items
* Number of Employees
* Number of Orders
* Stock Count

The below Procedure section help you understand how to use **Set as Integer** action:

**Procedure**

1. On the **EDA** tab, select the **required column.**
2. On the selected column, click the **Menu** button.

The drop-down menu is displayed.

3. From the drop-down menu, select **Set as Integer**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2443).png" alt=""><figcaption></figcaption></figure>

A new column is generated transforming the text column into an integer column.

</details>

<details>

<summary><strong>Set as Decimal (2 Decimal Places)</strong></summary>

**Overview**

The **Set as Decimal (2 Decimal Places)** converts the selected column to a decimal data type with two digits after the decimal point. This option can be used for columns containing financial values, percentages, measurements, or other data that requires consistent decimal precision for accurate calculations, reporting, and analysis.

**When to use**

You can use this option when you want to:

* Store currency values, such as prices, costs, or profits.
* Display percentages or rates with consistent precision.
* Perform accurate financial or mathematical calculations.
* Standardize the format of decimal values across the dataset.
* Prepare data for reporting, dashboards, or data integration.

The below Procedure section help you understand how to use **Set as Decimal** action:

**Procedure**

1. On the **EDA** tab, select the **required column.**
2. On the selected column, click the **Menu** button.

The drop-down menu is displayed.

3. From the drop-down menu, select **Set as Decimal (2 Decimal Places)**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2444).png" alt=""><figcaption></figcaption></figure>

A new column is generated with two decimal places.

</details>

<details>

<summary><strong>Set as Text</strong></summary>

**Overview**

The **Set as Text** converts the selected column to a text data type. You can use this option for columns containing alphanumeric values, identifiers, codes, or values with leading zeros that should be preserved and not treated as numeric or date values.

**When to use**

You can use this option when you want to:

* Preserve **leading zeros** in values such as ZIP codes, PIN codes, or customer IDs.
* Store **identifiers** such as Employee IDs, Product Codes, or Invoice Numbers that may contain both letters and numbers.
* Prevent numeric values from being used in mathematical calculations.
* Preserve special characters, spaces, or formatting in the data.
* Standardize columns that contain alphanumeric values

The below Procedure section help you understand how to use **Set as Text** action:

**Procedure**

1. On the **EDA** tab, select the **required column.**
2. On the selected column, click the **Menu** button.

The drop-down menu is displayed.

3. From the drop-down menu, select **Set as Text**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2445).png" alt=""><figcaption></figcaption></figure>

A new column is generated with text.

</details>

<details>

<summary><strong>Set as Date</strong></summary>

**Overview**

The **Set as Date** converts the selected column to the **Date** data type. You can use this option when a column contains date values that need to be recognized as dates rather than text. This enables accurate date-based sorting, filtering, calculations, reporting, and analysis.

**Example**

Converting 15/07/2026 as 15-Jul-2026

**Typical Date Columns**

Examples of columns commonly stored as the **Date** data type include:

* Date of Birth
* Order Date
* Invoice Date, etc.

The below Procedure section help you understand how to use **Set as Date** action:

**Procedure**

1. On the **EDA** tab, select the **required column.**
2. On the selected column, click the **Menu** button.

The drop-down menu is displayed.

3. From the drop-down menu, select **Set as Date**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2448).png" alt=""><figcaption></figcaption></figure>

A new column is generated with date.

</details>

<details>

<summary><strong>Set as Date Time</strong></summary>

**Overview**

The **Set as Date Time** converts the selected column to the **Date Time** data type. You can use this option when a column contains both date and time values that need to be recognized as timestamps rather than text. This enables accurate sorting, filtering, duration calculations, reporting, and time-based analysis.

**Example**

Converting 15/07/2026 09:30 AM as 15-Jul-2026 09:30:00

**Typical Date Columns**

Some of the examples of columns commonly stored as the **Date Time** data type include:

* Transaction Timestamp
* Order Date and Time
* Login Time
* Logout Time, etc.

**Procedure**

1. On the **EDA** tab, select the **required column.**
2. On the selected column, click the **Menu** button.

The drop-down menu is displayed.

3. From the drop-down menu, select **Set as Date Time**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2450).png" alt=""><figcaption></figcaption></figure>

A new column is generated with date time.

</details>

<details>

<summary><strong>Remove Column</strong></summary>

**Overview**

The need to **remove a column** during **data profiling** arises when the column is not required for analysis or may negatively affect data quality, performance, or downstream processing. Removing unnecessary columns helps create a cleaner, more focused dataset.

**Procedure**

1. On the **EDA** tab, select the **required column.**
2. On the selected column, click the **Menu** button.

The drop-down menu is displayed.

3. From the drop-down menu, select **Remove Column**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2451).png" alt=""><figcaption></figcaption></figure>

The selected column is removed.

</details>

***

## Related Topics

* [**Apply** **Table Transformations**](apply-table-transformations.md)
* [**Use AI Suggestions**](use-ai-suggestions.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
