---
icon: folder-plus
---

# Data Quality Manager

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The **Data Quality Manager** module in SCIKIQ enables users to create, manage, and monitor **Data Quality (DQ) rules** to ensure high-quality, reliable data.

The module allows users to create DQ rules, view rule details, re-execute rules to validate the latest data, and delete rules that are no longer required.

It also provides two dashboards for monitoring data quality:

* **High-Level DQ Dashboard** – Provides an overview of data quality metrics, trends, and data observability across datasets.
* **Operational DQ Dashboard** – Provides detailed validation results, enabling users to investigate failed records, analyze exceptions, and perform root cause analysis.

Together, these capabilities help users monitor data quality, identify issues, and take corrective actions to maintain trusted data.

***

### Key Concepts

This section introduces the key concepts of Data Quality (DQ), including [What Data Quality is](./#what-data-quality-dq-is), [What DQ Rules are](./#what-dq-rules-are), [Need for DQ Rules](./#need-for-dq-rules), [Guiding principles](./#guiding-principles). [Dimensions of data quality](./#dimensions-of-quality), [How SCIKIQ Data Quality helps](./#how-scikiq-data-quality-helps), and [DQ management in SCIKIQ](./#dq-management-in-scikiq).

Click the tabs below to learn more about each topic.

{% tabs %}
{% tab title="What Data Quality (DQ) is" %}
**Data Quality** helps organizations assess, monitor, and improve the quality of their data. High-quality data is essential for generating accurate insights, making informed business decisions, and ensuring operational efficiency.

Using a **no-code/low-code** approach, users can define data quality rules from built-in templates or generate them using language models. These rules are applied to selected data columns to evaluate data quality and produce an overall quality score.

Language model-powered data profiling also identifies potential data quality issues and recommends improvements, while allowing users to review and customize the suggested rules.
{% endtab %}

{% tab title="What DQ Rules are" %}
**Data Quality (DQ) Rules** define the criteria used to validate data against business and technical requirements. They help ensure that data is accurate, complete, consistent, and reliable before it is used for reporting, analytics, operational processes, or decision-making.

Using predefined or custom validation rules, organizations can identify data quality issues early, measure data quality, and take corrective actions. Implementing DQ rules helps maintain trusted data throughout its lifecycle, enabling better business outcomes and improving confidence in enterprise data.
{% endtab %}

{% tab title="Need for DQ rules" %}
Data Quality Rules are essential for ensuring that enterprise data remains reliable and fit for business use. They help organizations:

* Ensure data is accurate, complete, and trustworthy.
* Support informed business decisions using reliable data.
* Comply with regulatory and organizational data quality standards.
* Detect and prevent data errors before they impact downstream systems.
* Integrate data consistently across multiple data sources.
* Improve operational efficiency by reducing manual corrections and rework.
* Enhance customer trust by maintaining accurate customer information.
* Enable reliable reporting, analytics, and AI/ML initiatives.
* Keep data current and relevant throughout its lifecycle.
* Improve overall system performance by minimizing issues caused by poor-quality data.
{% endtab %}

{% tab title="Guiding Principles" %}
Follow these principles when defining and managing Data Quality Rules:

* **Criticality:** Prioritize data that has the greatest business impact and risk.
* **Lifecycle Management:** Maintain data quality throughout the entire data lifecycle, from data creation to disposal.
* **Prevention:** Prevent data quality issues whenever possible rather than correcting them later.
* **Root Cause Resolution:** Address the underlying causes of recurring data quality issues.
* **Governance:** Align data quality initiatives with the organization's data governance framework.
* **Standards-Driven:** Define clear, measurable, and consistently applied data quality standards.
* **Business Ownership:** Ensure business processes generate and maintain high-quality data.
* **System Enforcement:** Configure systems to consistently enforce data quality rules.
{% endtab %}

{% tab title="Dimensions of Quality" %}
The below mentioned are the dimensions of quality:

<table><thead><tr><th width="141.66668701171875" valign="top">Dimension</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Accuracy</td><td valign="top">Ensures data correctly represents real-world information by comparing it with trusted reference data or a reliable source.</td></tr><tr><td valign="top">Completeness</td><td valign="top">Verifies that all required data is present and no essential records or values are missing.</td></tr><tr><td valign="top">Consistency</td><td valign="top">Ensures data is represented uniformly across records, datasets, and systems using consistent values, formats, and structures.</td></tr><tr><td valign="top">Uniqueness</td><td valign="top">Ensures each entity is recorded only once and is uniquely identified by a key or identifier.</td></tr><tr><td valign="top">Validity</td><td valign="top">Ensures data conforms to predefined business rules, accepted value ranges, formats, and data types.</td></tr></tbody></table>
{% endtab %}

{% tab title="How SCIKIQ Data Quality Helps" %}
SCIKIQ Data Quality helps organizations improve and maintain high-quality data by:

* Automatically profiling data using Machine Learning (ML) to identify patterns, relationships, and potential data quality issues.
* Reducing manual effort, allowing data teams to focus on higher-value tasks.
* Enabling users to create custom data quality rules based on business requirements.
* Recommending data quality rules by analyzing data patterns and profiling results.
* Validating data against business and operational rules to ensure accuracy, completeness, and consistency.
* Using metadata, data profiling insights, and business context to generate meaningful validation rules.
* Helping organizations establish consistent data quality standards across the enterprise.
* Improving confidence in data used for reporting, analytics, and business decision-making.
{% endtab %}

{% tab title="DQ Management in SCIKIQ" %}
SCIKIQ Data Quality Management helps organizations improve and maintain high-quality data for reporting, analytics, and business decision-making.

{% stepper %}
{% step %}
**Key Features**

SCIKIQ Data Quality enables you to:

* Automate data discovery, profiling, and anomaly detection using Machine Learning (ML).
* Reduce manual effort and allow subject matter experts (SMEs) to focus on higher-value tasks.
* Create and deploy no-code/low-code data quality rules.
* Validate data against business and operational requirements.
* Review data quality results and identify issues.
* Generate rule recommendations based on metadata and data profiling insights.
{% endstep %}

{% step %}
**Data Quality Validation Options**

You can use SCIKIQ Data Quality in the following ways:

* **Standalone Validation:** Validate the quality of a selected table or dataset.
* **ETL Pipeline Validation:** Validate data at different stages of an ETL process.
* **Source-to-Target Validation:** Validate data during data movement by comparing the source and target datasets.
{% endstep %}

{% step %}
**Typical Workflow**

To validate data quality:

1. Decide when and where data quality checks should be performed.
2. Define the data quality rules based on your business requirements.
3. Run the validation to verify that the data complies with the defined rules.
4. Review the results and resolve any identified data quality issues.
{% endstep %}

{% step %}
**Roles and Responsibilities**

<table><thead><tr><th width="165" valign="top">Role</th><th valign="top">Responsibilities</th></tr></thead><tbody><tr><td valign="top">Client Admin</td><td valign="top">Oversees the creation and configuration of data quality rules, ensuring alignment with organizational standards.</td></tr><tr><td valign="top">Data Analyst</td><td valign="top">Utilizes data quality reports to drive analysis and insights.</td></tr><tr><td valign="top">Data Steward</td><td valign="top">Implements and monitors data quality rules within the data governance framework.</td></tr><tr><td valign="top">Data Owner</td><td valign="top">Ensures data quality rules are adhered to within their domain.</td></tr><tr><td valign="top">Entity Admin/Business CDO</td><td valign="top">Responsible for enterprise-level data quality management and strategy.</td></tr></tbody></table>
{% endstep %}
{% endstepper %}
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Creating and Using Data Quality Rules**](creating-and-using-data-quality-rules.md)
* [**Managing DQ Rules**](managing-dq-rules.md)
* [**Using Operational Dashboard**](using-operational-dq-dashboard.md)
* [**Using High Level Dashboard**](using-high-level-dq-dashboard.md)
