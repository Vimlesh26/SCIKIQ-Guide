---
icon: page
---

# Using Operational - DQ Dashboard

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The **Data Quality (DQ) Dashboard** provides a consolidated view of the overall health and quality of data across datasets. It enables **Data Stewards** and **Business Users** to monitor data quality, assess its current state, track quality trends, and identify potential data issues. By providing insights into data quality metrics and observability, the dashboard helps organizations maintain trusted data and make informed business decisions.

<details>

<summary><strong>Purpose</strong></summary>

The Data Quality Dashboard helps users continuously monitor the quality and reliability of data. It provides visibility into key data quality indicators, enabling users to identify anomalies, monitor trends, and ensure that data meets organizational quality standards.

</details>

<details>

<summary><strong>What the Dashboard Displays</strong></summary>

The dashboard provides a high-level summary of data quality, including:

* Overall data quality status
* Data quality metrics and trends
* Data observability insights
* Validation summaries across datasets
* Key indicators for monitoring data health

</details>

<details>

<summary><strong>Data Observability Metrics</strong></summary>

The Data Quality Dashboard helps answer the following data observability questions:

* **Freshness** – Is the data up to date, or are there any delays or gaps in data updates?
* **Distribution** – Does the data fall within the expected value ranges and patterns?
* **Volume** – Is the volume of incoming data meeting the expected thresholds?
* **Schema** – Have there been any changes to the structure or schema of the data?

</details>

<details>

<summary><strong>Benefits</strong></summary>

The Data Quality Dashboard helps organizations:

* Continuously monitor the health and quality of data.
* Detect anomalies and potential data quality issues at an early stage.
* Track data quality trends over time.
* Gain visibility into key data observability metrics.
* Support informed business decisions using accurate, complete, and reliable data.

</details>

***

### Using Operational - DQ Dashboard

{% tabs %}
{% tab title="Navigate to DQ Operational Dashboard" %}
**Overview**

**Viewing the DQ Operational Dashboard** provides a detailed view of the results of data quality validations. It enables users to monitor data quality, analyze failed records, identify the root cause of data quality issues, track quality trends, and prioritize remediation efforts. By providing both summary metrics and detailed record-level information, the dashboard helps organizations maintain high-quality, reliable data for business operations and decision-making.

**Procedure**

The below step-by-step instructions help you understand how to view **Operational - DQ Dashboard**:

_**To view Operational -  DQ Dashboard**_

1. On the **SCIKIQ Left Menu**, under SCIKIQ CONTROL, expand **Data Quality Manager**, and then click **Operational - DQ Dashboard**.

<figure><img src="../../../.gitbook/assets/image (2553).png" alt=""><figcaption></figcaption></figure>

The **Operational DQ Dashboard** page is displayed.

2. On the **Operational  DQ Dashboard** page:

A. Select the **source type** choosing from **Pipeline, Scheduler, Datasource,** and **Migration**. For example, Datasource.

B. Select the **Name, DQ Rule, Period,** and then click the **Apply** button.&#x20;

The **Operational  DQ Dashboard** data is displayed on the right pane.
{% endtab %}

{% tab title="Download Rule Report in PDF" %}
**Overview**

**Downloading a Rule Report** exports a report containing a summary of the selected Data Quality (DQ) rule execution, including the rule details, validation metrics, and overall execution results.

**Procedure**

The below step-by-step instructions help you understand how to download a DQ rule report:

_**To**_ _**re-execute a DQ rule**_

* Navigate to **Operational  DQ Dashboard** page (**SCIKIQ Left Menu>>** **SCIKIQ CONTROL>>Data Quality Manager>>Operational - DQ Dashboard**).
* On the **Operational  DQ Dashboard** page, click the **Download** button on the top right side of the application.

<figure><img src="../../../.gitbook/assets/image (2556).png" alt=""><figcaption></figcaption></figure>

The Rule Report is downloaded in PDF format in your local system.
{% endtab %}

{% tab title="Download  Rule Data in CSV" %}
**Overview**

**Downloading Rule Data** exports the data records evaluated by the selected Data Quality (DQ) rule. The downloaded data can be used for detailed record-level analysis, investigation of validation failures, and data remediation.

**Procedure**

The below step-by-step instructions help you understand how to download rule data:

_**To download rule data**_

1. Navigate to **Operational  DQ Dashboard** page (**SCIKIQ Left Menu>>** **SCIKIQ CONTROL>>Data Quality Manager>>Operational - DQ Dashboard**).
2. On the **Operational  DQ Dashboard** page, scroll down to **Rule Data** section, and then click the **CSV** button.

<figure><img src="../../../.gitbook/assets/image (2557).png" alt=""><figcaption></figcaption></figure>

The rule report is downloaded in CSV format in your local system.
{% endtab %}

{% tab title="Download Exception Logs in CSV " %}
**Overview**

**Downloading Exception Logs (CSV)** exports the records that failed Data Quality (DQ) validations, along with the corresponding exception details. The exported CSV file can be used for offline analysis, issue investigation, data remediation, reporting, and collaboration with data owners and business stakeholders.

**Procedure**

The below step-by-step instructions help you understand how to download exception logs:

_**To download rule data**_

1. Navigate to **Operational  DQ Dashboard** page (**SCIKIQ Left Menu>>** **SCIKIQ CONTROL>>Data Quality Manager>>Operational - DQ Dashboard**).
2. On the **Operational  DQ Dashboard** page, scroll down to **Exception Logs** section, and then click the **CSV** button.

<figure><img src="../../../.gitbook/assets/image (2558).png" alt=""><figcaption></figcaption></figure>

The exception logs report is downloaded in CSV format in your local system.
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Creating and Using Data Quality Rules**](creating-and-using-data-quality-rules.md)
* [**Managing DQ Rules**](managing-dq-rules.md)
* [**Using High Level - DQ Dashboard**](using-high-level-dq-dashboard.md)
