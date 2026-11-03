---
icon: page
---

# Business Metadata

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format._<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to manage business metadata. **Business Metadata** is the information that describes the business meaning and context of a data asset. It explains what the data represents, why it exists, who owns it, and how it should be used, making it easier for business users to understand and work with the data.

Business metadata typically includes - Business name, Business definition, Description, Business owner or Data Steward, and Business glossary terms, etc.

Business metadata provides the context needed to interpret data correctly. It bridges the gap between technical data and business users by describing data in business terms rather than technical terminology.

***

### Managing Business Data

As part of managing **business metadata**, you can manage business, technical, and user-defined metadata for data assets. These activities include **Defining Business Name** and **Finding and Replacing Values.** Refer to the below tabs for step-by-step instructions on these activities.

> <mark style="color:red;">**Note:**</mark> It is not mandatory to perform all of the metadata management activities described below. You can perform only the activities that are relevant to your requirements. After completing the necessary updates, you can save the metadata to apply them.

{% tabs %}
{% tab title="Accessing Business Data" %}
**Overview**

As part of accessing the business metadata, you need to first select the required asset and search for it. Once it is located, the **Business Metadata** page is displayed, providing business-related information such as business definitions, ownership, classifications, and other governance details.&#x20;

From this page, you can view and manage the business metadata to ensure that the dataset is accurately described, properly classified, and aligned with the organization's data governance standards.

***

**Procedure**

The below step-by-step instructions help you understand how to access the business metadata.

_**To access business metadata**_

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

&#x20;     The Meta Data Manager menu is displayed.

2. On the **Meta Data Manager** menu, click **Business Metadata**.

<figure><img src="../../../../.gitbook/assets/image (2206).png" alt=""><figcaption></figcaption></figure>

The **Business Metadata** page is displayed.

3. On the **Business** page, select the **asset,** and then click the **Search** button.

<figure><img src="../../../../.gitbook/assets/image (2208).png" alt=""><figcaption></figcaption></figure>

The **Business Metadata** page is displayed.

<figure><img src="../../../../.gitbook/assets/image (2209).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Defining Business Name" %}
**Overview**

In the **Business Metadata** page, the **Business Name** is a business-friendly name assigned to a technical table or column. It is intended for business users, so it should be meaningful and easy to understand, unlike technical database name&#x73;**.**

**Procedure**

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * The below mentioned procedure is applied to  both Technical and User tabs.
> * You can make changes to the **Business Data** page only when the asset is in the **Draft** status. Assets in the **Pending** or **Approved** status cannot be modified.

_**To define business data**_

1. On the **Business Metadata** page, in the **Business Name** column, enter the required **business name** for the required element.&#x20;
2. Next, click the **Save Metadata** button on the top right corner of the page.

<figure><img src="../../../../.gitbook/assets/image (2505).png" alt=""><figcaption></figcaption></figure>

The changes are saved successfully, and a confirmation message is displayed.
{% endtab %}

{% tab title="Finding and Replacing Values" %}
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
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Assets**](../../../integrations/meta-data-manager/assets/)
* [**Data Dictionary**](../../../integrations/meta-data-manager/data-dictionary/)
* [**Dataset Metadata**](../../../integrations/meta-data-manager/dataset-metadata/)
* [**Glossary**](../../../integrations/meta-data-manager/glossary/)
* [**Business Terms**](../../../integrations/meta-data-manager/business-terms/)
* [**Table Classification**](../../../integrations/meta-data-manager/table-classification.md)
