---
hidden: true
icon: page
---

# Managing Business Metadata

**Contents**

* [**Instructions for Using this Page**](managing-business-metadata.md#instructions-for-using-this-page)
* [**Overview**](managing-business-metadata.md#overview)
* [**Managing Business Data**](managing-business-metadata.md#managing-business-data)
* [**Related Topics**](managing-business-metadata.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

The **Dataset Metadata** contains three tabs—**Business**, **Technical**, and **User**—each designed to manage a specific category of metadata for the selected data asset. Although the metadata displayed differs across the tabs, the available management activities are largely the same.

***

## **Managing Business Data**

As part of managing **business metadata**, you can manage business, technical, and user-defined metadata for data assets. In addition, you can create definitions from LLM, export metadata, and save the updated business metadata.

> <mark style="color:red;">**Note:**</mark> It is not mandatory to perform all of the metadata management activities described below. You can perform only the activities that are relevant to your requirements. After completing the necessary updates, you can save the metadata to apply them.

<details>

<summary><strong>Defining Business Name</strong></summary>

**Purpose**

In the **Business Metadata** page, the **Business Name** is a business-friendly name assigned to a technical table or column. It is intended for business users, so it should be meaningful and easy to understand, unlike technical database name&#x73;**.**

**Procedure**

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * The below mentioned procedure is applied to  both Technical and User tabs.
> * You can make changes to the **Business Data** page only when the asset is in the **Draft** status. Assets in the **Pending** or **Approved** status cannot be modified.

1. On the **Business Metadata** page, in the **Business Name** column, enter the required **business name** for the required element.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2339).png" alt=""><figcaption></figcaption></figure>

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
3. In the **Find and Replace** section, select the **column** in which you want to find and replace values. For example, Classification.
4. Select the **value** with which you want to replace. For example, replacing Confidential with Internal.

<figure><img src="../../../../.gitbook/assets/image (2214).png" alt=""><figcaption></figcaption></figure>

The values are replaced. See the image below:

<figure><img src="../../../../.gitbook/assets/image (2216).png" alt=""><figcaption></figcaption></figure>

5. Next, click the **Save Metadata** button on the top right corner of the page.

The changes are saved successfully, and a confirmation message is displayed.

</details>

***

## Related Topics

* [**Dataset Metadata**](../../../integrations/meta-data-manager/dataset-metadata/)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
