---
icon: page
---

# Glossary

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to manage the glossary. A **Glossary** is a centralized collection of standardized business terms and their definitions. It helps establish a common business vocabulary so that everyone in the organization interprets business concepts consistently.

In a Metadata Manager, a glossary serves as a bridge between **business users** and **technical users** by providing clear, approved definitions for business terms and linking them to related data assets.

### **Managing Glossary**&#x20;

As part of **Glossary Management**, you can perform the activities including **Add a Glossary, View Glossary Details, View Audit History, Update a Glossary, Share a Glossary,** and **Delete a Glossary**.

Click the tabs below for step-by-step instructions for each activity.

{% tabs %}
{% tab title="Adding a Glossary" %}
**Overview**

This section describes how to add a glossary. A glossary organizes related business terms and their definitions in a structured repository, promoting consistent terminology, improving discoverability, and supporting effective metadata management and data governance.

***

**Procedure**

Adding a glossary involves two steps:&#x20;

* **Entering glossary details:** Entering Glossary Details helps establish the glossary's identity, ownership, and classification, ensuring that related business terms are organized and easily discoverable
* **Configuring approval mapping:** Configuring Approval Rule Mapping establishes the approval workflow for a glossary by specifying the rules that govern its review and approval.

Follow the step-by-step instructions below to complete these steps.

{% stepper %}
{% step %}
**Enter glossary details**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

&#x20;     The Meta Data Manager menu is displayed.

2. On the **Meta Data Manager** menu, click **Glossary.**

<figure><img src="../../../../.gitbook/assets/image (2223).png" alt=""><figcaption></figcaption></figure>

The **Glossary** page is displayed.

3. On the **Glossary** page, click the **Add Glossary** button on the top right corner of the page.

<figure><img src="../../../../.gitbook/assets/image (2973).png" alt=""><figcaption></figcaption></figure>

The Business Glossary dialogue box is displayed.

4. On the **Business Glossary** dialogue box:

**A. Enter glossary details**

* Enter the **Glossary Name, Glossary Category, Owner**, **Definition, Domain,** and **Subdomain** in the respective fields.&#x20;
* In the **Search Business Terms** field, enter the required **business term**. For example, Sales.

The **Results** section is displayed with the results related to the entered business term.

* From the **Results** section, select the **relevant result** by clicking the ![](<../../../../.gitbook/assets/image (2226).png>) icon corresponding to it.

<figure><img src="../../../../.gitbook/assets/image (2974).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> Refer to the below table for the description of glossary fields.

| Field             | Purpose                                                                                            |
| ----------------- | -------------------------------------------------------------------------------------------------- |
| Glossary Name     | Specifies a unique, meaningful name to identify the glossary.                                      |
| Glossary Category | Classifies the glossary into a relevant category for easier organization and discovery.            |
| Owner             | Identifies the person responsible for managing and maintaining the glossary.                       |
| Domain            | Associates the glossary with a specific business or functional area.                               |
| Subdomain         | Specifies a more specific area within the selected domain to organize the glossary.                |
| Definition        | Describes the purpose and scope of the glossary to help users understand its contents.             |
| Business Term     | Associates relevant business terms with the glossary to organize related terminology in one place. |
|                   |                                                                                                    |
{% endstep %}

{% step %}
**Configure approval rules**

1. On the **Glossary** page, scroll down to the **Approval Rule Mapping** section.
2. From the **User** drop-down boxes, select the **Recommender** and **Approver**.
3. Click the **Save Glossary** button.

<figure><img src="../../../../.gitbook/assets/image (2975).png" alt=""><figcaption></figcaption></figure>

The glossary is created and added to the Glossary page. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2976).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Viewing Glossary Details" %}
**Overview**

This section helps you understand how to view the  details of a glossary. Viewing details allows you to examine the complete information associated with a glossary, including its name, description, ownership, associated business terms, and other metadata.&#x20;

It helps you understand the purpose and contents of the glossary before making changes or using it for business and data governance activities.

**Procedure**

The below mentioned step-by-step instructions help you understand how to view the details of a glossary:

_**To view glossary details**_

1. Navigate to **Glossary** (SCIKIQ Control>>Meta Data Manager>>Glossary).

The **Glossary** page is displayed.

2. On the **Glossary** page, click the **View** icon corresponding to the required glossary.

<figure><img src="../../../../.gitbook/assets/image (2977).png" alt=""><figcaption></figcaption></figure>

The **Details** tab is displayed with the glossary details.

<figure><img src="../../../../.gitbook/assets/image (2978).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Viewing Lineage and Audit History" %}
**Overview**

This section describes how to view glossary details, explore its lineage, and review its audit history.

* **Viewing Glossary Lineage:** Helps users understand the relationships between a glossary and its associated business terms and data assets, improving traceability.
* **Viewing Audit History:** Provides a chronological record of changes made to a glossary, including what changed, when, and by whom.

**Procedure**

{% stepper %}
{% step %}
**Viewing Glossary Lineage**

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Glossary).

The **All Glossaries** page is displayed.

2. On the **Glossary** page, click the **View** icon corresponding to the required glossary.

<figure><img src="../../../../.gitbook/assets/image (2979).png" alt=""><figcaption></figcaption></figure>

The Glossary Details and Audit History tabs are displayed.

3. On the **Glossary Details** tab, scroll down to view metadata.

The glossary metadata is displayed pictorially with Lineage, Lineage Levels, and Legends. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2240).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> The below information provides description for Lineage, Lineage Levels, and Legends shown in the above image:
>
> * **Lineage:** The **Lineage** section provides a visual representation of the relationships between the selected glossary and its associated data assets, business terms, and other related metadata objects. It helps you understand how the glossary is connected to other components within the metadata ecosystem and assess the impact of changes.
> * **Lineage Levels:**&#x54;he **Lineage Levels** allow you to control the depth of the lineage diagram by specifying how many levels of upstream and downstream relationships are displayed. Increasing the lineage level provides a broader view of connected metadata objects and their dependencies.
> * **Legend:** It is a key that explains the meaning of the symbols, icons, colors, and line styles used in the lineage diagram.
{% endstep %}

{% step %}
**Viewing Audit History**



_**To view audit history**_

1. Click the **Audit History** tab.

The **Audit History** tab is open.

2. On the **Audit History** tab (See the below image):

A. Select the **Date Range** and **User** from the corresponding drop-down boxes.

> <mark style="color:red;">**Note:**</mark> Instead of selecting the **Date Range**, you can also select a specific period choosing from Last 7 Days, Last 30 Days, Last 3 Months, or Last 6 Months.

B. From the **Action** Type drop-down box, select the **required action** choosing from **All Actions, Update, Restored, Deleted,** or **Restored Version.**

> <mark style="color:red;">**Note:**</mark> Description of **Restored** and **Restored Version**
>
> * **Restored:** Indicates that a previous version of the glossary has been restored, making it the current active version.
> * **Restored Version:** Specifies the version of the glossary that was restored.

The audit history is displayed.

<figure><img src="../../../../.gitbook/assets/image (2983).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Updating a Glossary" %}
**Overview**

This section helps you understand how to update a glossary. **Updating a glossary** enables you to keep its information accurate, relevant, and aligned with changing business requirements.&#x20;

As business processes, terminology, or ownership evolve, the glossary can be modified to reflect the latest information and maintain consistency across the organization.

**Procedure**

Depending on your requirement, you can update a glossary by:

* changing its basic information
* adding new business terms
* modifying the approval rule mapping

The following step-by-step instructions describe how to perform each of these activities:

{% stepper %}
{% step %}
**Changing Basic Information**

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Glossary).

The **Glossary** page is displayed.

2. On the **Glossary** page, click the **Edit** icon corresponding to the required **glossary**.

> <mark style="color:red;">**Note:**</mark> Only glossaries with **Draft** status can be updated.

<figure><img src="../../../../.gitbook/assets/image (2984).png" alt=""><figcaption></figcaption></figure>

The **Business Glossary** screen is displayed.

3. On the **Business Glossary** screen, make the changes **Glossary Name**,  **Glossary Glossary, Owner, Definition, Domain,** or **Sub Domain**, if required.&#x20;
{% endstep %}

{% step %}
**Adding Business Terms**

* If you want to add business terms to the glossary, then in the **Search Business Terms** field, enter the required **key word**.

The search results are displayed.

* From the **Search Result**s, select the required **business term**, and click the **Add** button corresponding to it.

<figure><img src="../../../../.gitbook/assets/image (2988).png" alt=""><figcaption></figcaption></figure>

The business term is added to the glossary.
{% endstep %}

{% step %}
**Changing Approval Rules**

* If you want to change the approval rules mapping, then scroll down to the **Approval Rule Mapping** section, and change the **Recommender** and **Approver**.
* Finally, click the **Save Dictionary** button.

<figure><img src="../../../../.gitbook/assets/image (2990).png" alt=""><figcaption></figcaption></figure>

The dictionary is updated. See the below example image.

<figure><img src="../../../../.gitbook/assets/image (2991).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Sharing a Glossary" %}
**Overview**

This section describes how to share a glossary. **Sharing a glossary** makes standardized business terminology available to the appropriate users and teams, promoting collaboration and ensuring consistent use of business definitions across the organization.&#x20;

It also enables controlled access so that authorized users can view, review, or manage the glossary as needed.

**Procedure**

The below mentioned step-by-step instructions help you understand how to share a glossary:

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Business Terms).

The **Glossary** page is displayed.

2. On the **Glossary** page, click the **Share** icon corresponding to the required **glossary**.

<figure><img src="../../../../.gitbook/assets/image (3014).png" alt=""><figcaption></figcaption></figure>

The **Resource Permission** dialogue box is displayed with the **Private** option displayed by default.

A. **If you want to make the business term accessible to all users** permitted to access the relevant SCIKIQ environment, subject to the platform's access controls, then select the **Public** option,&#x20;

B. **If you want to share it to specific users or groups**, then select the **Shared** option, and click the **Add More** button.

The sharing fields are displaye&#x64;**.**

C. From the sharing fields, select the required **Group.**

D.  From the **Role** drop-down box, select **Viewer** or **Contributor**.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> 1. **Viewers** can view the term and its details, while **Contributors** can view and modify the term, subject to the permissions configured in SCIKIQ.
> 2. If you to delete the sharing fields, click the **Delete** ![](<../../../../.gitbook/assets/image (2326).png>) button.

D. Click the **Save** button.

<figure><img src="../../../../.gitbook/assets/image (3067).png" alt=""><figcaption></figcaption></figure>

The glossary is shared and the **Permission applied successfully** message is displayed.

<figure><img src="../../../../.gitbook/assets/image (3069).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Delete a Glossary" %}
**Overview**

This section describes how to delete a glossary. **Deleting a glossary** benefits the organization **when the it is no longer needed** because it helps keep the metadata repository clean and relevant.

**Procedure**

The below mentioned step-by-step instructions help you understand how to delete a glossary:

1. Navigate to **Business Terms page** (SCIKIQ Control>>Meta Data Manager>>Business Terms).

The **Glossary** page is displayed.

2. On the **Glossary** page, click the **Delete** icon corresponding to the required **glossary.**

> <mark style="color:red;">**Note:**</mark> Only glossaries with **Draft** status can be deleted.

<figure><img src="../../../../.gitbook/assets/image (3070).png" alt=""><figcaption></figcaption></figure>

The Delete message is displayed.

3. On the **Delete** message, click the **Yes** button.

<figure><img src="../../../../.gitbook/assets/image (3071).png" alt=""><figcaption></figcaption></figure>

The glossary is deleted.
{% endtab %}
{% endtabs %}



***

### Related Topics

* [**Assets**](../../../integrations/meta-data-manager/assets/)
* [**Data Dictionary**](../../../integrations/meta-data-manager/data-dictionary/)
* [**Dataset Metadata**](../../../integrations/meta-data-manager/dataset-metadata/)
* [**Business Terms**](../../../integrations/meta-data-manager/business-terms/)
* [**Table Classification**](../../../integrations/meta-data-manager/table-classification.md)
