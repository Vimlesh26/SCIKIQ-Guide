---
icon: page
---

# Data Dictionary

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to manage the data dictionary. The **Data Dictionary** is a centralized repository for managing metadata about enterprise data assets. It provides information about the structure, meaning, characteristics, and usage of data, helping business and technical users understand and manage organizational data.

The **Data Dictionary** is organized into two tabs:

* **Business:** Manage business metadata, including definitions, descriptions, business terms, and classifications.
* **Technical:** Manage technical metadata, including table and column properties, data types, keys, and relationships.

Both tabs provide similar capabilities, including searching for data sources and tables, viewing and updating metadata, performing bulk updates, importing and exporting metadata, previewing changes, and saving updates.

### Managing Data Dictionary

As part of managing the **Data Dictionary**, you can perform activities such as **Send Columns for Approval**, **Bulk Upload, Define Business Terms, Find and Replace Values, Map Business Terms, Add Foreign Key, Preview Data, Apply Data Profiling, Apply DQ Rules, Define Composite Key, Generate Definitions using LLM, Export Metadata,** and **Save Data Dictionary**.

Click the tabs below for step-by-step instructions. Test

{% tabs %}
{% tab title="Accessing Data Dictionary" %}
**Overview**

As part of accessing the data dictionary, you need to first access the Data Dictionary page and then specify DataSource Type, Connection, and Table. Upon clicking the Search button, the Data Dictionary for the selected table is then displayed, allowing you to view and manage its metadata.

***

**Procedure**

The below step-by-step instructions help you understand how to access the data dictionary.

_**To access data dictionary**_

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

&#x20;     The Meta Data Manager menu is displayed.

2. On the **Meta Data Manager** menu, click **Data Dictionary**.

<figure><img src="../../../../.gitbook/assets/image (2242).png" alt=""><figcaption></figcaption></figure>

The **Data Dictionary** page is displayed.

3. On the **Data Dictionary** page, in the **Search Filters** pane, select **Type** **(DataSource or Storage), DataSource Connection, Table,** and then click the **Search** button. See the below example image.

<figure><img src="../../../../.gitbook/assets/image (2243).png" alt=""><figcaption></figcaption></figure>

The Data Dictionary is displayed.
{% endtab %}

{% tab title="Sending Columns for Approval" %}
**Overview**

This section describes how to send the selected columns to the authorised user for approval.The purpose of approval is to ensure that important changes to business or technical metadata are **reviewed and validated by an authorized user before they become official or published metadata**.

Once sent for the approval, the status of that column will be displayed as Submitted. Upon approval by the authorised user, it will be shown as Approved.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * Once a column is submitted for approval, its status changes to **Submitted**. After an authorized user approves the submission, the status changes to **Approved**.&#x20;
> * Only columns in **Draft** status can be submitted for approval. Columns that have already been **submitted** cannot be submitted again.

**Procedure**

The below instructions help you understand how to send the selected columns for approval:

_**To send meta data for approval**_

1. On the **Data Dictionary** page, in the **Find and Replace** area, select either **All Rows** or **Selected Rows** depending on your requirement.

The **Send for Approval** button appears.

2. Click the **Send for Approval** button.

<figure><img src="../../../../.gitbook/assets/image (2993).png" alt=""><figcaption></figcaption></figure>

The **Send Selected Column(s) for Approval** dialogue box is displayed.

2. On the **Send Selected Column(s) for Approval** dialogue box:

A. From the **User** drop-down box, select the **approver.**

B. Click the **Send for Approval** button.

<figure><img src="../../../../.gitbook/assets/image (3000).png" alt=""><figcaption></figcaption></figure>

The selected columns are sent to the approval of the approver.
{% endtab %}

{% tab title="Bulk Uploading to Data Dictionary" %}
**Overview**

Bulk Uploading enables you to update metadata for multiple tables and their columns within a selected data source in a single operation. This allows you to modify business, technical, or user-defined metadata efficiently without updating each table individually.

***

**Procedure**

The below step-by-step instructions help you understand how to bulk update the data dictionary.

_**To bulk upload to data dictionary**_

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

&#x20;     The Meta Data Manager menu is displayed.

2. On the **Meta Data Manager** menu, click **Data Dictionary**.

<figure><img src="../../../../.gitbook/assets/image (2242).png" alt=""><figcaption></figcaption></figure>

The **Data Dictionary** page is displayed.

3. On the **Data Dictionary** page:

A. From the **Search Filters** section on the left panel, select **Type** **(DataSource or Storage)** and **DataSource Connection.**

> <mark style="color:red;">**Note:**</mark> For bulk uploading, you do not need to select a table from the **Search Filters** section on the left panel.

B. Click the **Bulk Upload** on the top right corner of the page. See the example image below.

<figure><img src="../../../../.gitbook/assets/image (2375).png" alt=""><figcaption></figcaption></figure>

The **Bulk Upload Data Dictionary** section is displayed.

4. On the **Bulk Upload Data Dictionary** section, click the **Download Template** button.

<figure><img src="../../../../.gitbook/assets/image (2367).png" alt=""><figcaption></figcaption></figure>

The Template is downloaded in your local system. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2368).png" alt=""><figcaption></figcaption></figure>

5. Open the **Template,** and then enter the details in all the columns.

> <mark style="color:red;">**Note:**</mark> Ensure that the **table name** you enter exists in the database.

6. Now, go back to **Bulk Upload Data Dictionary** section, drag and drop or click to upload the template, and then click the **Upload** button.

<figure><img src="../../../../.gitbook/assets/image (2371).png" alt=""><figcaption></figcaption></figure>

The **Confirm Bulk Upload** message box is displayed.

7. On the **Confirm Bulk Upload** message box, click the **Yes** button.

<figure><img src="../../../../.gitbook/assets/image (2373).png" alt=""><figcaption></figcaption></figure>

The **File Uploaded Successfully** message is displayed. See the image below.

<figure><img src="../../../../.gitbook/assets/image (2374).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Defining Business Name" %}
**Purpose**

This section describes how to define the **Business Names** in a Data Dictionary.  Defining **Business Names** in the Data Dictionary helps translate technical column names into **meaningful, business-friendly names** that are easier for users to understand.&#x20;

For example:

* cust\_id→ **Customer ID**
* dob→ **Date of Birth**
* tot\_ord\_amt→ **Total Order Amount**

**Procedure**

The below step-by-step instructions help you understand how to define business names:

_**To define business names**_

1. On the **Data Dictionary** page, in the **Business Name** column, enter the required **business name** for the required element. For example replacing EMUKID as Check ID.
2. On the top of the page, click the **Update** button to save the changes.

<figure><img src="../../../../.gitbook/assets/image (3006).png" alt=""><figcaption></figcaption></figure>

The changes are saved successfully, and **Success** message is displayed.
{% endtab %}

{% tab title="Finding and Replacing Values" %}
**Overview**

This section describes how to use the **Find and Replace Value** feature. This feature enables you to locate metadata entries with a specified status and replace them with another status in bulk. This helps streamline metadata maintenance, improve consistency, and reduce the effort required to update multiple records individually.

**Procedure**

The below step-by-step instructions help you understand how to define business terms:

> <mark style="color:red;">**Note:**</mark> The steps described below are common to both the **Business** and **Technical** tabs.&#x20;

_**To use Find and Replace Value feature**_

1. On the **Data Dictionary** page, select the required **tab**. For example, Business.
2. Select either **All Rows** or **Selected Rows**, depending on the scope of the update.
3. In the **Find and Replace** section, select the **column** (For example, Status) in which you want to find and replace values.&#x20;
4. Select the **value** (For example, Submit) with which you want to replace it.&#x20;

<figure><img src="../../../../.gitbook/assets/image (3004).png" alt=""><figcaption></figcaption></figure>

The values are replaced. See the image below:

<figure><img src="../../../../.gitbook/assets/image (3005).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Mapping Business Terms" %}
**Overview**

This section describes how to **Business Terms** in the data dictionary. **Mapping a Business Term** associates a business term with a table column or data field. This helps users understand what the data represents, improves consistency in business terminology, and makes data easier to understand and manage.

**Procedure**

The below step-by-step instructions help you understand how to map business terms:

> <mark style="color:red;">**Note:**</mark> The steps described below are common to both the **Business** and **Technical** tabs.&#x20;

_**To map business terms**_

1. On the **Data Dictionary** page, from the **Element Name** column, select the required **element.** For example, EmployeeType.
2. From  the **Business term** column, select the **business term** relevant to the selected elemen&#x74;**.** For example, Human Resources.
3. Click the **Update** button on the top right corner of the page.

<figure><img src="../../../../.gitbook/assets/image (3007).png" alt=""><figcaption></figcaption></figure>

The mapping is done and the success message is displayed.

> <mark style="color:red;">**Note:**</mark> For mapping, you can also use the auto mapping feature by clicking the ![](<../../../../.gitbook/assets/image (2306).png>) on the top of the page.
{% endtab %}

{% tab title="Adding Foreign Key" %}
**Overview**

This section describes how to add a **Foreign Key.** Adding a **Foreign Key** in the Data Dictionary helps define the **relationship between columns in different tables**. It identifies which column in one table references a key column in another table.

**Procedure**

The below step-by-step instructions help you understand how to add a foreign key:

> <mark style="color:red;">**Note:**</mark> The steps described below are common to both the **Business** and **Technical** tabs.&#x20;

_**To add a foreign key**_

1. On the **Data Dictionary** page, click the **Foreign Key** button on the top of the page.

<figure><img src="../../../../.gitbook/assets/image (3008).png" alt=""><figcaption></figcaption></figure>

The **Add Foreign Key** dialogue box is displayed.

2. On the **Add Foreign Key** dialogue box (See the below image):

A. In the **Source** section, select the **Connection, Source Table,** and **Column.**

B. In the **Target** section, select the **Connection, Target Table,** and **Column.**

C. Click the **Add** button.

The foreign key is added.

D. Finally, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/image (2309).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Previewing Data" %}
**Overview**

This section help you understand how to use the **Preview** feature. This feature enables you to review the metadata changes before saving them to the Data Dictionary. It allows you to verify that the updates are accurate and complete, helping prevent incorrect or unintended changes from being saved.

**Procedure**

The below step-by-step instructions help you understand how to use the preview feature:

> <mark style="color:red;">**Note:**</mark> The steps described below are common to both the **Business** and **Technical User** tabs.&#x20;

_**To use the preview feature**_

* On the **Data Dictionary** page, click the **Preview** button on the top of the page.

<figure><img src="../../../../.gitbook/assets/image (3009).png" alt=""><figcaption></figcaption></figure>

The Preview screen is displayed.&#x20;
{% endtab %}

{% tab title="Applying Data Profiling" %}
**Overview**

This section describes help you understand how to use the **Data Profiling** feature. **Data Profiling,** which enables data cleaning improves the quality of a dataset by identifying and correcting errors, inconsistencies, duplicate records, and missing values.

It ensures that the data is accurate, complete, and consistent, making it suitable for reporting, analytics, and other business processes.

**Procedure**

The below step-by-step instructions help you understand how to use the **Data Profiling** feature:

> <mark style="color:red;">**Note:**</mark> The steps described below are common to both the **Business** and **Technical User** tabs.&#x20;

_**To use the data profiling feature**_

1. On the **Data Dictionary** page, click the **Preview** button on the top of the page.

<figure><img src="../../../../.gitbook/assets/image (3010).png" alt=""><figcaption></figcaption></figure>

The Preview screen is displayed.

2. On the **Preview** screen, click the **EDA** button at the bottom of the screen.

<figure><img src="../../../../.gitbook/assets/image (2311).png" alt=""><figcaption></figcaption></figure>

The **Data Profiling** page is opened in a new window.

3. On the **Left Pane** of **Data Profiling** page, in the **Data Cleansing** section, click the **Fill cell value** or **Fill empty cells** **with above** to clean the data.
4. If you want apply **Masking**:

A. Click **Data Masking** and then select the required option choosing from **Auto, Custom,** or **Protegrity.**

B. Click the **Submit** button.

<figure><img src="../../../../.gitbook/assets/image (2268).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Applying DQ Rules" %}
**Overview**

This section describes how to apply the **Data Quality (DQ) Rules.** Applying **Data Quality (DQ) Rules** to metadata helps ensure that data assets meet predefined quality standards.

These rules validate the accuracy, completeness, consistency, and integrity of data, enabling organizations to identify and address data quality issues before the data is used for reporting, analytics, or business operations.

**Procedure**

The below step-by-step instructions help you understand how to use the **Data Quality (DQ) Rules** feature:

> <mark style="color:red;">**Note:**</mark> The steps described below are common to both the **Business** and **Technical User** tabs.&#x20;

_**To use DQ rules**_

1. On the **Data Dictionary** page, click the **Preview** button on the top of the page.

<figure><img src="../../../../.gitbook/assets/image (3011).png" alt=""><figcaption></figcaption></figure>

The Preview screen is displayed.

2. On the **Preview** screen, click the **DQ Rules** button at the bottom of the screen.

<figure><img src="../../../../.gitbook/assets/image (2258).png" alt=""><figcaption></figcaption></figure>

The **DQ Rules** page is opened in a new window.

3. On the **DQ Rules** page, define the quality by specifying the required **column, operator, value, rule name,** and **DQ dimensions**, and then click the **Test** button.

<figure><img src="../../../../.gitbook/assets/image (2312).png" alt=""><figcaption></figcaption></figure>

The Data Quality page is displayed.

4. Click the **Apply** button. See the below image.

The DQ rules are applied.

5. Next, click the **Save** button to save DQ rules.

<figure><img src="../../../../.gitbook/assets/image (2261).png" alt=""><figcaption></figcaption></figure>

The Save DQ dialogue box is displayed.

6. On the **Save DQ** dialogue box, specify a **name** for the DQ rule, and then click the **Save** button.

<figure><img src="../../../../.gitbook/assets/image (2262).png" alt=""><figcaption></figcaption></figure>

The DQ Rule is saved and the **Success** message is displayed.
{% endtab %}

{% tab title="Defining Composite Key" %}
**Overview**

This section describes how to define the **Composite Key** feature in the Data Dictionary. This feature enables you to specify a combination of two or more columns that together uniquely identify each record in a table.&#x20;

Documenting composite keys in the Data Dictionary helps users understand the table structure, maintain data integrity, establish relationships between tables, and support effective metadata management.

**Procedure**

The below step-by-step instructions help you understand how to  specify the composite key:

> <mark style="color:red;">**Note:**</mark> The steps described below are common to both the **Business and Technical** tabs.&#x20;

_**To specify the composite key**_

* On the **Data Dictionary** page, specify the **Composite Key, Table Business Name, Table Description,** and then click the **Update** button.

<figure><img src="../../../../.gitbook/assets/image (2263).png" alt=""><figcaption></figcaption></figure>

The composite key is defined.
{% endtab %}

{% tab title="Creating Definitions from LLM" %}
**Overview**

This section describes how to use the **Create Definitions from LLM** feature in Data Dictionary. Using this feature, you can generate meaningful **Business Names, Business Definitions, and Tags** for columns in the **Data Dictionary**.&#x20;

The **Create Definitions from LLM** feature uses a **Large Language Model (LLM)** to automatically generate business-friendly definitions for tables, columns, or other metadata assets. Instead of manually writing definitions, you can leverage AI to create meaningful descriptions quickly and consistently.

**Procedure**

As part of the procedure, you need to select the required columns and then select **Create Definitions from LLM** option. The **Compare Generated Definitions** screen displays the old and newly generated definitions for review. Upon confirmation, the new definitions are applied to the **Data Dictionary** page.

> <mark style="color:red;">**Note:**</mark> The steps described below are common to both the **Business** and **Technical** tabs.&#x20;

The below step-by-step instructions help you understand how to use the **Create Definitions from LLM** feature:

_**To use create definitions feature**_ &#x20;

1. On the **Data Dictionary** page, select the required columns, and then turn on the **Create definitions from LLM** option.

> <mark style="color:red;">**Note:**</mark> Depending on your requirements, you can select **one or more columns**, or **all columns**.

<figure><img src="../../../../.gitbook/assets/image (2995).png" alt=""><figcaption></figcaption></figure>

The **Compare Generated Definitions** screen is displayed.

2. On the **Compare Generated Definitions** screen, review the **old and new definitions,** and then click the **Done** button.

> <mark style="color:red;">**Note:**</mark> Ensure that the required rows remain selected on the **Compare Generated Definitions** screen. Definitions are not generated for unselected rows.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2996).png" alt=""><figcaption></figcaption></figure>

The updated **Business Name, Business Definition, and Tags** are reflected on the **Data Dictionary** page. See the below example image.

<figure><img src="../../../../.gitbook/assets/image (2997).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Exporting Metadata" %}
**Overview**

This section describes how to use the **Export** feature in Data Dictionary. The **Export** feature enables you to export the metadata dictionary to **Microsoft Excel** or to the **AWS Glue Data Catalog**.&#x20;

* **Exporting to Excel:** Exporting to Excel provides a convenient way to review, analyze, share, and maintain metadata offline.
* **Exporting to AWS Glue**: Exporting to AWS Glue publishes the metadata to a centralized catalog, enabling data discovery and seamless integration with AWS analytics and data processing services.

**Procedure**

The below step-by-step instructions help you understand how to use the **Export** feature:

> <mark style="color:red;">**Note:**</mark> The steps described below are common to both the **Business** and **Technical** tabs.&#x20;

_**To use the export feature**_

1. **Exporting to Excel**

* On the **Data Dictionary** page, from the **File Download/Export** drop-down box, select **Excel**.

<figure><img src="../../../../.gitbook/assets/image (2265).png" alt=""><figcaption></figcaption></figure>

The metadata is downloaded in Excel format in your local system.

2. **Exporting to Glue**

A. On the **Data Dictionary** page, from the **File Download/Export** drop-down box, select **Glue**.

The Export dialogue box is displayed.

B. On the **Export** dialogue box, select **connection, database,** and **table,** and then click the **Export** button.

<figure><img src="../../../../.gitbook/assets/image (2266).png" alt=""><figcaption></figcaption></figure>

The table is exported to Glue and the Success message is displayed.

> <mark style="color:red;">**Note:**</mark> If you want to export the data to a new table, then select the select the **Create New Table** option on the **Export** dialogue box, and specify the **Table Name.**&#x20;
{% endtab %}

{% tab title="Saving Data Dictionary" %}
**Overview**

This section describes how save the Data Dictionary. Saving the **Data Dictionary** ensures that the metadata changes made are **persisted and available for subsequent use**.

**Procedure**

* On the **Data Dictionary** page, click the **Save Dictionary** button.

<figure><img src="../../../../.gitbook/assets/image (2267).png" alt=""><figcaption></figcaption></figure>

The data dictionary is saved and the success message is displayed.
{% endtab %}
{% endtabs %}



***

### Related Topics

* [**Assets**](../../../integrations/meta-data-manager/assets/)
* [**Business Metadata**](../../../integrations/meta-data-manager/business-metadata/)
* [**Dataset Metadata**](../../../integrations/meta-data-manager/dataset-metadata/)
* [**Glossary**](../../../integrations/meta-data-manager/glossary/)
* [**Business Terms**](../../../integrations/meta-data-manager/business-terms/)
* [**Table Classification**](../../../integrations/meta-data-manager/table-classification.md)
