---
icon: page
---

# Assets

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to manage the assets. An **Asset** refers to any data object or resource whose metadata is captured, managed, and governed. Rather than representing the actual data, an asset represents the entity about which metadata is maintained, enabling users to understand, discover, and manage it effectively.

**Role of an Asset in Metadata Manager**

Assets are the **core entities** managed by the Metadata Manager. They act as the foundation for organizing and governing metadata. By maintaining metadata for each asset, the Metadata Manager helps users understand what the asset is, where it comes from, who owns it, how it is used, and how it relates to other assets.

***

### Managing Assets

{% tabs %}
{% tab title="Adding an Asset" %}
### Overview

Adding an asset to the **Metadata Manager** registers it as a managed data object so that its metadata can be captured, organized, and governed. Once an asset is added, you can associate it with business and technical metadata, making it easier to discover, understand, and manage throughout its lifecycle..

***

### **Procedure**

Expand the below panels for step-by-step instructions on how to add an asset:

<details>

<summary><strong>Navigate to</strong> <strong>Assets Page</strong></summary>

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

The Meta Data Manager menu is displayed.

2\. On the **Meta Data Manager** menu, click **Assets.**

<figure><img src="../../../../.gitbook/assets/image (2217).png" alt=""><figcaption></figcaption></figure>

The **Assets** page is displayed.

</details>

<details>

<summary><strong>Specify</strong> <strong>Asset Information</strong></summary>

1. On the **Assets** page, click **Add Asset** on the top right corner.

<figure><img src="../../../../.gitbook/assets/image (2218).png" alt=""><figcaption></figcaption></figure>

The **Add Asset** dialogue box is displayed.

2. On the **Add Asset** dialogue box:

A. In the **Asset Information** section, specify **Asset Category**, **Resource**, **Asset Class, Asset Scope, Owner,** and **Catalogue** in the respective fields:

Here is the description for the above fields.

<table><thead><tr><th width="146.5555419921875" valign="top">Field</th><th valign="top">Description</th><th valign="top">Purpose</th></tr></thead><tbody><tr><td valign="top">Asset Category</td><td valign="top">Specifies the type or category of the asset being added, such as a dataset, report, dashboard, or API. </td><td valign="top">Categorizing assets helps organize them and simplifies discovery and management.</td></tr><tr><td valign="top">Resource</td><td valign="top">Specifies the source or resource from which the asset originates, such as a database, file system, application, or cloud storage. </td><td valign="top">This helps identify the asset's source and maintain traceability.</td></tr><tr><td valign="top">Asset Class</td><td valign="top">Specifies the classification of the asset based on its business or technical role. </td><td valign="top">Asset classes help group similar assets and apply consistent governance and management policies.</td></tr><tr><td valign="top">Asset Scope</td><td valign="top">Specifies the scope or level at which the asset exists, such as enterprise, domain, project, or department</td><td valign="top">This helps define the asset's organizational context and visibility</td></tr><tr><td valign="top">Catalogue</td><td valign="top">Specifies the catalogue in which the asset will be stored and managed.</td><td valign="top">Catalogues organize related assets into logical collections, making them easier to discover, govern, and maintain</td></tr></tbody></table>

<figure><img src="../../../../.gitbook/assets/image (2220).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Specify</strong> <strong>Resource Approval Roles</strong></summary>

1. On the **Add Asset** dialogue box, scroll down to **Resource Approval Roles** section.
2. In the **Resource Approval Roles** section, specify the **Approver** and **Recommender**.
3. In the **Asset Path** field, enter the **path** of asset.
4. Click the **Next** button.

<figure><img src="../../../../.gitbook/assets/image (2221).png" alt=""><figcaption></figcaption></figure>

The Metadata section is displayed. See the next panel.

</details>

<details>

<summary><strong>Specify</strong> <strong>Metadata</strong></summary>



</details>

<details>

<summary><strong>Specify</strong> <strong>Asset Name, Description, and Submit</strong></summary>



</details>
{% endtab %}

{% tab title="View Asset Information" %}
**Overview**

Viewing the details of an asset allows you to examine its complete metadata and understand its business and technical characteristics. It provides a comprehensive view of the asset, including its description, ownership, classifications, relationships, lineage, and other associated metadata, enabling you to make informed decisions about its use and management.

**Procedure**

The below step-by-step instructions help you understand how to view the detailed information of an asset:

_**To view asset information**_

1. Navigate to **Assets** page (SCIKIQ Control>>Meta Data Manager>>Assets).
2. On the **Assets** page, click the **View** button corresponding to the required asset.

<figure><img src="../../../../.gitbook/assets/image (2298).png" alt=""><figcaption></figcaption></figure>

The asset details are displayed.
{% endtab %}

{% tab title="Update Existing Assets" %}
**Overview**

Updating an existing asset enables you to keep its metadata accurate, complete, and aligned with the latest business and technical requirements. As an asset evolves over time, its metadata may need to be revised to reflect changes in ownership, classifications, descriptions, relationships, or other associated information.

**Procedure**

The below step-by-step instructions help you understand how to update an existing asset:

_**To update an existing asset**_

1. On the **Asset** page, click the **Edit** button corresponding to the required asset.

<figure><img src="../../../../.gitbook/assets/image (2299).png" alt=""><figcaption></figcaption></figure>

The **Edit** **Asset** screen is displayed.

2. On the **Edit** **Asset** page, make the required changes to Information, Metadata, and Description, and then click the **Submit** button at the bottom.

<figure><img src="../../../../.gitbook/assets/image (2300).png" alt=""><figcaption></figcaption></figure>

The asset is updated.
{% endtab %}

{% tab title="Rediscover Assets" %}
**Overview**

Rediscovering an asset enables you to refresh the metadata of an existing asset by rescanning its source system. It updates the asset's metadata to reflect any changes made to the underlying data source, ensuring that the Metadata Manager remains synchronized with the latest asset information.

**Procedure**

The below step-by-step instructions help you understand how to rediscover an existing asset:

1. On the **Asset** page, click the **Rediscover** button corresponding to the required asset.

<figure><img src="../../../../.gitbook/assets/image (2332).png" alt=""><figcaption></figcaption></figure>

The asset is rediscovered and the **Success** message is displayed. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2333).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Withdraw Assets" %}
**Overview**

Withdrawing an asset allows you to remove it from active use without permanently deleting it from the Metadata Manager. This is useful when an asset is no longer valid, has been replaced, or should not be available for general use, while still retaining its metadata for historical reference or audit purposes.

**Procedure**

The below step-by-step instructions help you understand how to view withdraw an existing asset:

* On the **Asset** page, click the **Withdraw** button corresponding to the required asset.

<figure><img src="../../../../.gitbook/assets/image (2334).png" alt=""><figcaption></figcaption></figure>

The asset is withdrawn and the Success message is displayed. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2336).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Delete Assets" %}
**Purpose**

Deleting an asset permanently removes it and its associated metadata from the Metadata Manager. This helps maintain a clean and accurate metadata repository by eliminating assets that are no longer required or were added incorrectly.

**Procedure**

The below step-by-step instructions help you understand how to delete an existing asset:

1. On the **Assets** page, click the **Delete** button corresponding to the required asset.

<figure><img src="../../../../.gitbook/assets/image (2337).png" alt=""><figcaption></figcaption></figure>

The **Delete Warning** message box is displayed.

2. On the **Delete Warning** message box, review the message, and then click the **Yes** button.

<figure><img src="../../../../.gitbook/assets/image (2338).png" alt=""><figcaption></figcaption></figure>

The asset is deleted.
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Data Dictionary**](../../../integrations/meta-data-manager/data-dictionary/)
* [**Business Metadata**](../../../integrations/meta-data-manager/business-metadata/)
* [**Dataset Metadata**](../../../integrations/meta-data-manager/dataset-metadata/)
* [**Glossary**](../../../integrations/meta-data-manager/glossary/)
* [**Business Terms**](../../../integrations/meta-data-manager/business-terms/)
* [**Table Classification**](../../../integrations/meta-data-manager/table-classification.md)
