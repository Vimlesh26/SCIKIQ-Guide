---
icon: page
---

# Dataset Metadata

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to manage dataset metadata. **Dataset Metadata** is a collection of information that describes a dataset, including its purpose, structure, ownership, classification, and other business and technical details. It helps users understand, discover, and manage datasets more effectively while supporting data governance, data quality, and compliance initiatives.

For example, dataset metadata may include, Dataset name, Description, Data source, and Owner, etc.

Dataset metadata plays a vital role in helping users understand, govern, and use data effectively. It provides the context needed to interpret a dataset without examining its contents.

### Managing Dataset Metadata

{% tabs %}
{% tab title="Accessing Dataset Metadata" %}
**Overview**

As part of accessing the dataset metadata, you need to first search for the required dataset. Once the dataset is located, the **Dataset Metadata** page is displayed, providing detailed information about the dataset, including its business and technical metadata, ownership, classifications, tags, and other associated details. From this page, you can view and manage the dataset metadata as required.

***

**Procedure**

The below step-by-step instructions help you understand how to access the dataset metadata.

_**To access dataset metadata**_

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

&#x20;     The Meta Data Manager menu is displayed.

2. On the **Meta Data Manager** menu, click **Dataset Metadata**.

<figure><img src="../../../../.gitbook/assets/image (2246).png" alt=""><figcaption></figcaption></figure>

The **Dataset Metadata** page is displayed.

3. On the **Dataset Metadata** page, select the **dataset,** and then click the **Search** button.

<figure><img src="../../../../.gitbook/assets/image (2247).png" alt=""><figcaption></figcaption></figure>

The **Dataset Metadata** page is displayed. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2248).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Defining Business Name" %}
**Purpose**

In the **Dataset Metadata** page, the **Business Name** is a business-friendly name assigned to a technical table or column. It is intended for business users, so it should be meaningful and easy to understand, unlike technical database name&#x73;**.**

**Procedure**

> <mark style="color:red;">**Note:**</mark> The below mentioned procedure is applied to Technical tab and User tab also.

1. On the **Dataset Metadata** page, in the **Business Name** column, enter the required **business name** for the required element.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2212).png" alt=""><figcaption></figcaption></figure>

2. Next, click the **Save Metadata** button on the top right corner of the page.

The business name is defined.
{% endtab %}

{% tab title="Finding and Replacing Values" %}
**Overview**

The **Find and Replace Status** feature enables you to locate dataset metadata entries with a specified status and replace them with another status in bulk. This helps streamline metadata maintenance, improve consistency, and reduce the effort required to update multiple records individually.

**Procedure**

> <mark style="color:red;">**Note:**</mark> The steps described below are common to the **Business**, **Technical**, and **User** tabs. The only difference is the type of metadata managed in each tab.

1. On the **Dataset Metadata** page, select the required **tab**. For example, Business.
2. Select either **All Rows** or **Selected Rows**, depending on the scope of the update.
3. In the **Find and Replace** section, select the **column** in which you want to find and replace values. For example, Status.
4. Select the **value** with which you want to replace. For example, replacing Draft with Submit.

<figure><img src="../../../../.gitbook/assets/image (2255).png" alt=""><figcaption></figcaption></figure>

The values are replaced. See the image below:

<figure><img src="../../../../.gitbook/assets/image (2256).png" alt=""><figcaption></figcaption></figure>

5. Next, click the **Save Metadata** button on the top right corner of the page.

The changes are saved successfully, and a confirmation message is displayed.
{% endtab %}

{% tab title="Uploading Excel File to Dataset Metadata " %}
**Overview**

The **File Upload** allows you to upload an Excel file containing metadata to the **Dataset Metadata** page. This feature lets you import multiple metadata records in a single operation, eliminating the need for manual data entry and saving time.

**Procedure**

> <mark style="color:red;">**Note:**</mark> The steps described below are common to the **Business**, **Technical**, and **User** tabs.&#x20;

**Procedure**

1. On the **Dataset Metadata** page, in the **UPLOAD/EXPORT** section:

A. Click the **Browse** button to navigate to your system and select the required file.

B. Click the **Upload** button.

<figure><img src="../../../../.gitbook/assets/image (2507).png" alt=""><figcaption></figcaption></figure>

The file is uploaded successfully. See the highlighted message in the below screenshot.

<figure><img src="../../../../.gitbook/assets/image (2509).png" alt=""><figcaption></figcaption></figure>

2. Review the changes, and then save them by clicking the **Save Metadata** button on the top right corner of the page.
{% endtab %}

{% tab title="Downloading Dataset Metadata" %}
**Overview**

The **Export** **to Excel** feature enables you to export the dataset metadata dictionary to **Microsoft Excel.** Exporting to Excel provides a convenient way to review, analyze, share, and maintain metadata offline.

**Procedure**

> <mark style="color:red;">**Note:**</mark> The steps described below are common to the **Business**, **Technical**, and **User** tabs.&#x20;

* On the **Dataset Metadata** page, from the **File Download/Export** drop-down box, select **Excel**.

<figure><img src="../../../../.gitbook/assets/image (2257).png" alt=""><figcaption></figcaption></figure>

The metadata is downloaded in Excel format in your local system.
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Assets**](../../../integrations/meta-data-manager/assets/)
* [**Data Dictionary**](../../../integrations/meta-data-manager/data-dictionary/)
* [**Glossary**](../../../integrations/meta-data-manager/glossary/)
* [**Business Terms**](../../../integrations/meta-data-manager/business-terms/)
* [**Table Classification**](../../../integrations/meta-data-manager/table-classification.md)
* [**Business Terms**](../../../integrations/meta-data-manager/business-terms/)
