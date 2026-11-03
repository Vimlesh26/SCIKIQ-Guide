---
icon: page
---

# Performing Data Profiling

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

Data profiling is used to explore, assess, and improve data quality before analysis or downstream processing. The required data object is selected from a **Dataset**, **Table**, or **Storage**, after which transformations can be applied at the column and table levels. AI-generated suggestions, calculated fields, and Data Quality (DQ) rules can also be applied.

All transformations are recorded in the **History** pane and can be reviewed or reverted if required. Once the data is validated, the changes can be saved by updating the existing EDA version or creating a new one. The processed data can also be downloaded or exported for reporting, analytics, and other downstream applications.

***

### Procedure

{% tabs %}
{% tab title="Select Data Object" %}
**Overview**

As part of data profiling, you can select a **Dataset**, **Table/Topic**, or **Storage** as the data object.

* **Dataset:** The **EDA** tab is displayed, and the data loads immediately after you select the required dataset.
* **Table/Topic:** The **EDA** tab is displayed after you select the required table/topic and its corresponding table connection.
* **Storage:** The **EDA** tab is displayed after you select the required file type, file storage, and table connection.

***

**Procedure**

The below Step-by-step instructions help you understand how to select a data object:

_**To select a data object**_

1. On the **SCIKIQ Left Navigation Bar,** go to **SCIKIQ CURATE**, and then click **Data Profiling** .

<figure><img src="../../../../.gitbook/assets/image (2452).png" alt=""><figcaption></figcaption></figure>

The  **Data Profiling** page is displayed.

2. On the **Data Profiling** page, select **Dataset,Table/Topic,** or **Storage** tab. **F**or example, Table/Topic.

<figure><img src="../../../../.gitbook/assets/image (2453).png" alt=""><figcaption></figcaption></figure>

The Table/Topic tab is opened.

3. On the **Table/Topic** tab:

A. From the **Table Connection** drop-down box, select the required **connection**.

B. From the **Table** drop-down box, select the required **table**.

The EDA tab is highlighted and the data is displayed. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2455).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Apply Column Transformations" %}
**Overview**

As part of column transformations, you can apply various operations to cleanse, modify, secure, and prepare your data for analysis. These operations include **Data Cleansing**, **Delete Columns**, **Data Masking**, **Calculate String Length**, **Change Date Format**, and **Data Anonymization**.

> <mark style="color:red;">**Note**</mark>: You are not required to apply all of these transformations. Select and apply only the operations that best meet your data preparation and business requirements.

***

**Procedure**

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
{% endtab %}

{% tab title="Apply Column Data Type Actions" %}
**Overview**

The **Column Data Type Actions** menu enables you to convert the data type of a selected column to **Numeric**, **Integer**, **Decimal**, **Text**, **Date**, or **Date Time** based on your requirements. It also provides the option to remove unwanted columns, helping you improve data consistency and prepare the dataset for analysis.

> <mark style="color:red;">**Note**</mark>: You are not required to apply all of these transformations. Select and apply only the operations that best meet your data preparation and business requirements.

***

**Procedure**

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
{% endtab %}

{% tab title="Apply Data Transform Actions" %}
**Overview**

The **Data Transform Actions** enable you to filter records, rename, duplicate, or remove columns, treat missing values using various techniques, and identify or handle outliers. These transformations help improve data quality, consistency, and reliability before performing exploratory data analysis or downstream processing.

> <mark style="color:red;">**Note**</mark>: You are not required to apply all of these transformations. Select and apply only the operations that best meet your data preparation and business requirements.

***

**Procedure**

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
{% endtab %}

{% tab title="Use AI Suggestions" %}
**Overview**

The **Suggestions** feature in ScikIQ helps you improve the quality of your data by providing intelligent recommendations during data profiling. It analyzes the selected dataset and suggests actions that can enhance data quality and prepare the data for analysis.

The recommendations may include deleting empty columns, changing column data types, applying data masking, and performing other data transformation tasks. You can review the suggestions and apply the ones that best meet your data preparation requirements.

***

**Procedure**

The below Procedure section help you understand how to use AI suggestions:

1. On the **EDA** tab, select the **Suggestions** ![](<../../../../.gitbook/assets/image (2467).png>) icon in the **left pane**.

<figure><img src="../../../../.gitbook/assets/image (2466).png" alt=""><figcaption></figcaption></figure>

The list of **AI suggestions** along with the list of **applicable tables** are displayed.

2. From the list of **applicable tables,** select the required tables.

> <mark style="color:red;">**Note:**</mark> If required, you can select all the tables by selecting the  ![](<../../../../.gitbook/assets/image (2469).png>) button.

3. &#x20;From the list of **AI suggestions**, select the required suggestion.

<figure><img src="../../../../.gitbook/assets/image (2471).png" alt=""><figcaption></figcaption></figure>

The selected suggestions are applied to the table.
{% endtab %}

{% tab title="Apply DQ Rules" %}
**Overview**

The purpose of applying **Data Quality (DQ) Rules** during **Data Profiling** is to assess whether the data meets predefined quality standards and business rules. DQ rules help identify data quality issues before the data is used for analysis, reporting, machine learning, or downstream processing.

***

**Procedure**

The below Procedure section help you understand how to apply data quality rules:

1. On the **EDA** tab, select the **Data Quality** **Suggestions** ![](<../../../../.gitbook/assets/image (2406).png>) icon in the **left pane**.

<figure><img src="../../../../.gitbook/assets/image (2407).png" alt=""><figcaption></figcaption></figure>

The list of **Data Quality Suggestions** are displayed.

2. &#x20;From the list of **Data Quality Suggestions**, select the required **suggestions**, and then click the **Save** button.

> <mark style="color:red;">**Note:**</mark> If required, you can select all the tables by selecting the  ![](<../../../../.gitbook/assets/image (2410).png>) button.

<figure><img src="../../../../.gitbook/assets/image (2408).png" alt=""><figcaption></figcaption></figure>

The DQ rules are saved and the success message is diaplyed. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2411).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Calculated Field" %}
**Overview**

The purpose of **Creating a Calculated Field** during **Data Profiling** is to derive new information from existing data, making the dataset more meaningful and useful for analysis. Instead of modifying the original data, a calculated field creates a new column based on a formula or expression.

***

**Procedure**

The below Procedure section help you understand how to create a calculated field:

1. On the **EDA** tab, select the **Creating a Calculated Field** ![](<../../../../.gitbook/assets/image (2427).png>) icon in the **left pane**.

<figure><img src="../../../../.gitbook/assets/image (2428).png" alt=""><figcaption></figcaption></figure>

The **Calculated Field** button is displayed.

2. Click the **Calculated Field** button.

<figure><img src="../../../../.gitbook/assets/image (2429).png" alt=""><figcaption></figcaption></figure>

The **Calculated Field** screen is displayed.

3. On the **Calculated Field** screen, enter **field name, expression**, and then click the **Save** button.&#x20;

The calculated field is created.
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Working with EDA**](../working-with-eda.md)&#x20;

