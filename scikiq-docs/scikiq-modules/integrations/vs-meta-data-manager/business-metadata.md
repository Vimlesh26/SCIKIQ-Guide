# Business Metadata

### <mark style="color:blue;">**Overview**</mark>

The **Business Metadata Module** allows users to manage metadata details for selected data assets—specifically **Datasets** and **LDM Assets**. This includes maintaining business definitions, assigning data owners, applying classifications, linking business terms, and managing tags.

This module supports both **individual** and **bulk editing** of metadata fields, and access is based on the **status of the asset** (Draft, Submitted, or Approved). The module is designed with clear tab-based navigation and an intuitive layout for business and technical users.

### <mark style="color:blue;">**Supported Asset Types**</mark>

Only the following asset types are displayed in the module:

* Dataset
* LDM Asset

Other asset types are not selectable within this module.

<figure><img src="../../../.gitbook/assets/image (323).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">Asset Status and Permissions</mark>

Each asset has a status: **Draft**, **Submitted**, or **Approved**. The actions allowed in the module depend on the current status of the asset.

* If the asset is in **Draft** or **Submitted** status, users can edit the metadata.

<figure><img src="../../../.gitbook/assets/image (325).png" alt=""><figcaption></figcaption></figure>

* If the asset is already **Approved**, users can only view the metadata. No editing is allowed and "**Save Metadata"** button is disabled.&#x20;

<figure><img src="../../../.gitbook/assets/image (324).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">Row Selection and Editing</mark>

Users can work with metadata at the row level.

There are two selection options:

* Select individual rows manually.
* Use the "Select All" checkbox to select all rows at once.

<figure><img src="../../../.gitbook/assets/image (331).png" alt=""><figcaption></figcaption></figure>

Once rows are selected, users can perform bulk actions to update:

* Classification
* Status
*   Data Owner

    <figure><img src="../../../.gitbook/assets/image (332).png" alt=""><figcaption></figcaption></figure>



These actions apply to all selected rows. Once updates are made, they must be saved using the **Save Metadata** button.

### <mark style="color:blue;">Module Layout and Tabs</mark>

The module contains three main tabs, each showing a different aspect of metadata. By default, the **Business** tab opens first when an asset is selected.

#### Business Tab

This tab allows users to define or update metadata that is business-facing.&#x20;

1.  Users can modify the business name, assign a business term, define ownership, set classification levels, and tag elements for easier discovery.

    <figure><img src="../../../.gitbook/assets/image (326).png" alt=""><figcaption></figcaption></figure>
2.  When a business term is selected, the business definition will be auto-filled based on information from the business glossary.&#x20;

    <figure><img src="../../../.gitbook/assets/image (330).png" alt=""><figcaption></figcaption></figure>
3. If the term is not available, users should define one separately before linking it.

{% hint style="warning" %}
&#x20;You can check the Business Term module for more details. \[[Business Term module ](business-terms.md)]for more details.
{% endhint %}

#### Technical Tab

The technical tab provides details related to the data structure, such as data type, format, field length, and value ranges. Users can specify whether a field is nullable and assign technical owners and classification levels.

This section is especially useful for data stewards or engineers who need to understand the structural and validation aspects of the data.

<figure><img src="../../../.gitbook/assets/image (327).png" alt=""><figcaption></figcaption></figure>

#### User Tab

The user tab captures how the data is perceived by consumers. It includes fields like business name, tags, business term, and user rating. This helps organizations understand how well data is documented and whether it is usable from the business point of view.

<figure><img src="../../../.gitbook/assets/image (328).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">Saving Metadata</mark>

After making changes to metadata, users must click the **Save Metadata** button. Changes are not saved automatically. This ensures that updates are reviewed and confirmed before being committed.

If all changes are valid, the system will save the metadata successfully and display a confirmation message.

<figure><img src="../../../.gitbook/assets/image (329).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">Additional Features</mark>

Two important tools are available in the module:

**DQ (Data Quality):**\
Opens or connects to the data quality rules for the selected asset. This allows users to check for data quality issues and define validation criteria.

{% hint style="warning" %}
#### Data Quality (DQ)

Connects to data quality rules for the selected asset, allowing users to identify issues and define validation criteria.

See the [**Data Quality module**](../data-quality-manager-1/data-quality-rules.md) for details.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (333).png" alt=""><figcaption></figcaption></figure>



**EDA (Exploratory Data Analysis):**\
Provides a data profile or statistical summary of the asset. This helps users understand the distribution, format, and health of the data.

{% hint style="warning" %}
#### 📊 Exploratory Data Analysis (EDA)

Exploratory Data Analysis provides a statistical summary and data profile of the asset. It helps users assess the distribution, structure, quality, and overall health of the data — offering valuable insights before deeper analysis or modeling.

&#x20;For detailed functionality and usage, refer to the [EDA module.](../../interactive-blocks/data-profiling.md)
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (334).png" alt=""><figcaption></figcaption></figure>

These tools enhance the usability and reliability of the metadata management process.

#### Summary

The Business Metadata Module enables structured management of metadata through a user-friendly interface. It supports business and technical users with role-based editing, glossary integration, and quality tools.

By using this module, users can:

* Define clear business context for data
* Assign ownership and accountability
* Apply classification and governance policies
* Support technical validation and structure
* Promote usability and discovery for consumers

This module is a key part of data governance and ensures consistency across the enterprise metadata repository.



