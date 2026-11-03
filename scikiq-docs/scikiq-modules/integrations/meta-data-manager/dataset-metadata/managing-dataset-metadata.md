---
hidden: true
icon: page
---

# Managing Dataset Metadata

***

**Contents**

* [**Instructions for Using this Page**](managing-dataset-metadata.md#instructions-for-using-this-page)
* [**Overview**](managing-dataset-metadata.md#overview)
* [**Managing Dataset Metadata**](managing-dataset-metadata.md#managing-dataset-metadata)
* [**Related Topics**](managing-dataset-metadata.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

The **Dataset Metadata** contains three tabs—**Business**, **Technical**, and **User**—each designed to manage a specific category of metadata for the selected data asset. Although the metadata displayed differs across the tabs, the available management activities are largely the same.

***

## **Managing Dataset Metadata**

As part of **Dataset Dataset Metadata Management Activities**, you can manage business, technical, and user-defined metadata for data assets. In addition, you can create definitions from LLM and export metadata,  and save the updated dataset metadata.

> <mark style="color:red;">**Note:**</mark> It is not mandatory to perform all of the metadata management activities described below. You can perform only the activities that are relevant to your requirements. After completing the necessary updates, you can save the metadata to apply them.

<details>

<summary><strong>Defining Business Name</strong></summary>

**Purpose**

In the **Dataset Metadata** page, the **Business Name** is a business-friendly name assigned to a technical table or column. It is intended for business users, so it should be meaningful and easy to understand, unlike technical database name&#x73;**.**

**Procedure**

> <mark style="color:red;">**Note:**</mark> The below mentioned procedure is applied to Technical tab and User tab also.

1. On the **Dataset Metadata** page, in the **Business Name** column, enter the required **business name** for the required element.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2212).png" alt=""><figcaption></figcaption></figure>

2. Next, click the **Save Metadata** button on the top right corner of the page.

The changes are saved successfully, and a confirmation message is displayed.

</details>

<details>

<summary><strong>Finding and Replacing Values</strong></summary>

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

</details>

<details>

<summary><strong>Creating Definitions from LLM</strong></summary>

**Overview**

The **Create Definitions from LLM** feature uses a **Large Language Model (LLM)** to automatically generate business-friendly definitions for tables, columns, or other metadata assets. Instead of manually writing definitions, you can leverage AI to create meaningful descriptions quickly and consistently.

**Procedure**

> <mark style="color:red;">**Note:**</mark> The steps described below are common to the **Business**, **Technical**, and **User** tabs.&#x20;

* On the **Dataset Metadata** page, turn on the **Create definitions from LLM** option.

The LLM definitions are displayed.

> <mark style="color:red;">**Note:**</mark> You can review and modify the generated definitions before saving them.

</details>

<details>

<summary><strong>Export Dataset Metadata</strong></summary>

**Overview**

The **Export** feature enables you to export the metadata dictionary to **Microsoft Excel.** Exporting to Excel provides a convenient way to review, analyze, share, and maintain metadata offline.

**Procedure**

> <mark style="color:red;">**Note:**</mark> The steps described below are common to the **Business**, **Technical**, and **User** tabs.&#x20;

* On the **Dataset Metadata** page, from the **File Download/Export** drop-down box, select **Excel**.

<figure><img src="../../../../.gitbook/assets/image (2257).png" alt=""><figcaption></figcaption></figure>

The metadata is downloaded in Excel format in your local system.

</details>

***

## Related Topics

* [**Business Metadata**](../business-metadata/)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
