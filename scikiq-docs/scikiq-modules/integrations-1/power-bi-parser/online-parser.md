---
icon: page
---

# Online Parser

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to parse a workspace report using the online parser in SCIKIQ.

**Parsing** is the process of analysing a file or its contents to identify and interpret its structure, components, and relationships so that the information can be processed by a system.

In SCIKIQ, the online parser analyses Power BI workspace reports to extract metadata from the supported report content. This helps make report-related information available for further processing and analysis within SCIKIQ, reducing the need to examine report details manually.

***

### Parsing Workspace Reports

The process of parsing Power BI reports in SCIKIQ involves the following steps: **Navigating to the Online Parser page, Selecting a Workspace, Selecting Reports, and Reviewing** and **Submitting the Request.**

Follow the step-by-step instructions below to parse the selected workspace reports.

_**To parse workspace reports**_

{% stepper %}
{% step %}
**Navigate to Online Parser page**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

The Meta Data Manager menu is displayed.

2. On the **Meta Data Manager** menu, click **PowerBI Parser**, and then select **Online Parser.**

<figure><img src="../../../.gitbook/assets/image (3178).png" alt=""><figcaption></figcaption></figure>

The **Online Parser** page is displayed.
{% endstep %}

{% step %}
**Select the Workspace**

1. On the **Online Parser** page, select the required **workspace**.
2. After selecting the workspace, click the **Select Reports** button.

<figure><img src="../../../.gitbook/assets/image (3076).png" alt=""><figcaption></figcaption></figure>

The **Select Reports** section is displayed.
{% endstep %}

{% step %}
**Select Reports**

1. In the **Select Reports** section, do one of the following:
   * To find a specific report, enter its name in the **Search** field.
   * To select all filtered reports, select the **Select all filtered reports** checkbox.
   * To select specific reports, select the checkbox next to each report you want.
2. After selecting the required reports, select the **Data Domain** and **Subdomain** corresponding to each report.

> <mark style="color:red;">**Note:**</mark> If you want to view a report in Powerbuilder, then click the **Open Report in Power BI** ![](<../../../.gitbook/assets/image (3183).png>)button corresponding to that report.

3. Click the **Validate Selection** button.

<figure><img src="../../../.gitbook/assets/image (3077).png" alt=""><figcaption></figcaption></figure>

The **Review** section is displayed.
{% endstep %}

{% step %}
**Review and** **Submit Parse Job**&#x20;

* On the **Review** section, review the **Validated Selection**, and then click the **Submit Parse Job** button.

<figure><img src="../../../.gitbook/assets/image (3078).png" alt=""><figcaption></figcaption></figure>

The parse job is submitted and the workspace is displayed with the **Queued** status on the **Jobs** page.

<figure><img src="../../../.gitbook/assets/image (3079).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

***

### Related Topics

* [**Meta Data Manager**](../../integrations/meta-data-manager/)
