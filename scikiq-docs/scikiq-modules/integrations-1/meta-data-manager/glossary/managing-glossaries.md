---
hidden: true
icon: page
---

# Managing Glossaries

***

**Contents**

* [**Instructions for Using this Page**](managing-glossaries.md#instructions-for-using-this-page)
* [**Overview**](managing-glossaries.md#overview)
* [**Procedure**](managing-glossaries.md#procedure)
* [**Related Topics**](managing-glossaries.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

Managing glossaries ensures that business terms are organized, maintained, and governed throughout their lifecycle. As part of the glossary management, you can [view glossary details ](managing-glossaries.md#view-glossary-details)and [audit history](../../../integrations/meta-data-manager/glossary/managing-glossaries.md#view-audit-history).&#x20;

You can also [update](../../../integrations/meta-data-manager/glossary/managing-glossaries.md#update-a-glossary), [share](../../../integrations/meta-data-manager/glossary/managing-glossaries.md#share-a-glossary), and [remove](../../../integrations/meta-data-manager/glossary/managing-glossaries.md#delete-a-glossary) glossaries as business requirements evolve, ensuring that business terminology remains accurate, consistent, and easy to access.

***

## Procedure

As part of **Glossary Management**, you can perform the following activities. Expand the sections below to view the step-by-step instructions for each activity.

<details>

<summary><strong>View Glossary Details</strong></summary>

**Overview**

Viewing glossary details allows you to examine the complete information associated with a glossary, including its name, description, ownership, associated business terms, and other metadata. It helps you understand the purpose and contents of the glossary before making changes or using it for business and data governance activities.

**Procedure**

The below mentioned step-by-step instructions help you understand how to view the details of a glossary :

1. Navigate to **Glossary** (SCIKIQ Control>>Meta Data Manager>>Glossary).

The **All Glossaries** page is displayed.

2. On the **All Glossaries** page, click the **View** icon corresponding to the required glossary.

<figure><img src="../../../../.gitbook/assets/image (2228).png" alt=""><figcaption></figcaption></figure>

The Glossary Details tab is displayed with the details.

3. On the **Glossary Details** tab, scroll down to view metadata.

The glossary metadata is displayed pictorially with Lineage, Lineage Levels, and Legends. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2240).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> The below information provides description for Lineage, Lineage Levels, and Legends shown in the above image:
>
> * **Lineage:** The **Lineage** section provides a visual representation of the relationships between the selected glossary and its associated data assets, business terms, and other related metadata objects. It helps you understand how the glossary is connected to other components within the metadata ecosystem and assess the impact of changes.
> * **Lineage Levels:**&#x54;he **Lineage Levels** allow you to control the depth of the lineage diagram by specifying how many levels of upstream and downstream relationships are displayed. Increasing the lineage level provides a broader view of connected metadata objects and their dependencies.
> * **Legend:** It is a key that explains the meaning of the symbols, icons, colors, and line styles used in the lineage diagram.

</details>

<details>

<summary><strong>View Audit History</strong></summary>

**Overview**

Viewing the audit history of a glossary enables you to track all changes made to the glossary over time. It provides a chronological record of activities, helping you understand what changes were made, when they were made, and by whom.

**Procedure**

The below mentioned step-by-step instructions help you understand how to view the audit history of a glossary :

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Glossary).

The **All Glossaries** page is displayed.

2. On the **Glossary** page, click the **View** icon corresponding to the required glossary.

<figure><img src="../../../../.gitbook/assets/image (2228).png" alt=""><figcaption></figcaption></figure>

The Glossary Details and Audit History tabs are displayed.

3. Click the **Audit History** tab.

The **Audit History** tab is open.

4. On the **Audit History** tab (See the below image):

A. Select the **Date Range** and **User** from the corresponding drop-down boxes.

> <mark style="color:red;">**Note:**</mark> Instead of selecting the **Date Range**, you can also select a specific period choosing from Last 7 Days, Last 30 Days, Last 3 Months, or Last 6 Months.

B. From the **Action** Type drop-down box, select the **required action** choosing from **All Actions, Update, Restored, Deleted,** or **Restored Version.**

> <mark style="color:red;">**Note:**</mark> Description of **Restored** and **Restored Version**
>
> * **Restored:** Indicates that a previous version of the glossary has been restored, making it the current active version.
> * **Restored Version:** Specifies the version of the glossary that was restored.

<figure><img src="../../../../.gitbook/assets/image (2239).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Update a Glossary</strong></summary>

**Overview**

Updating a glossary enables you to keep its information accurate, relevant, and aligned with changing business requirements. As business processes, terminology, or ownership evolve, the glossary can be modified to reflect the latest information and maintain consistency across the organization.

**Procedure**

The below mentioned step-by-step instructions help you understand how to update a  glossary:

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Glossary).

The **All Glossaries** page is displayed.

2. On the **All Glossaries** page, click the **Edit** icon corresponding to the required **glossary**.

<figure><img src="../../../../.gitbook/assets/image (2230).png" alt=""><figcaption></figcaption></figure>

The **Business Glossary** dialogue box is displayed.

3. On the **Business Glossary** dialogue box, make the required modifications, and then click the **Save Glossary** button.

> <mark style="color:red;">**Note:**</mark> As part of updating, you can add more business terms to the glossary.

<figure><img src="../../../../.gitbook/assets/image (2231).png" alt=""><figcaption></figcaption></figure>

The glossary is updated and the **Success** message is displayed. See the below example image.

<figure><img src="../../../../.gitbook/assets/image (2232).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Share a Glossary</strong></summary>

**Overview**

Sharing a glossary makes standardized business terminology available to the appropriate users and teams, promoting collaboration and ensuring consistent use of business definitions across the organization. It also enables controlled access so that authorized users can view, review, or manage the glossary as needed.

**Procedure**

The below mentioned step-by-step instructions help you understand how to share a glossary:

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Business Terms).

The **All Glossaries** page is displayed.

2. On the **All Glossaries** page, click the **Share** icon corresponding to the required **glossary**.

<figure><img src="../../../../.gitbook/assets/image (2233).png" alt=""><figcaption></figcaption></figure>

The **Resource Permission** dialogue box is displayed.

3. On the **Resource Permission** dialogue box:

A. Select the required **permission type** choosing from **Public, Private,** or **Shared**. For example, Shared.

B. Click the **Add More** button.

The sharing fields are displayed under **Share With.**

&#x20;C. From the **Share With** fields, select the **Group** and **Role** (Viewer or Contributor).

> <mark style="color:red;">**Note:**</mark> Click the **Delete** ![](<../../../../.gitbook/assets/image (2326).png>) button if you want to delete the **Share With** fields row.

C. Click the **Save** button.

<figure><img src="../../../../.gitbook/assets/image (2234).png" alt=""><figcaption></figcaption></figure>

The glossary is shared and the **Permission applied successfully** message is displayed.

<figure><img src="../../../../.gitbook/assets/image (2235).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Delete a Glossary</strong></summary>

**Overview**

Deleting a glossary benefits the organization **when the it is no longer needed** because it helps keep the metadata repository clean and relevant.

**Procedure**

The below mentioned step-by-step instructions help you understand how to delete a glossary:

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Business Terms).

The **All Glossaries** page is displayed.

2. On the **All Glossaries** page, click the **Delete** icon corresponding to the required **glossary.**

<figure><img src="../../../../.gitbook/assets/image (2236).png" alt=""><figcaption></figcaption></figure>

The Delete message is displayed.

3. On the **Delete** message, click the **Yes** button.

<figure><img src="../../../../.gitbook/assets/image (2237).png" alt=""><figcaption></figcaption></figure>

The glossary is deleted.

</details>

***

## Related Topics

* [**Adding a Glossary**](../../../integrations/meta-data-manager/glossary/adding-a-glossary.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
