---
icon: page
---

# Managing Existing Entities

***

**Contents**

* [**Instructions for Using this Page**](managing-existing-entities.md#instructions-for-using-this-page)
* [**Overview**](managing-existing-entities.md#overview)
* [**Procedure**](managing-existing-entities.md#procedure)
* [**Related Topics**](managing-existing-entities.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

As part of managing existing entities, you can [update](managing-existing-entities.md#update-existing-entities) entity information to keep it accurate and aligned with business and governance requirements. You can also [delete](managing-existing-entities.md#delete-entities) entities that are no longer needed, helping maintain a clean and relevant metadata repository.

Additionally, you can [create roles and grant menu and policy permissions](managing-existing-entities.md#create-roles-and-grant-permissions-and-policies), and explore [organizational hierarchy](managing-existing-entities.md#view-organization-hierarchy-and-node-details) and [domain hierarchy](managing-existing-entities.md#viewing-domain-hierarchy).&#x20;

These capabilities support effective governance, access control, and visibility into the structure and management of enterprise data assets.

***

## **Procedure**

Expand the below panels to view step-by-step instructions:

<details>

<summary><strong>Update Existing Entities</strong></summary>

**Overview**

An entity should be updated whenever its business, governance, or metadata information changes.&#x20;

Updating an entity ensures that it continues to accurately represent the associated business object and remains aligned with current organizational requirements.

Keeping entity information up to date improves data discoverability, governance, and overall metadata quality.

**Procedure**

The below step-by-step instructions help you understand how to update an existing entity:

1. On the **Entity** page, under the **Organization Entity** tab, click the **Edit** button corresponding to the required entity.

<figure><img src="../../../../.gitbook/assets/image (2157).png" alt=""><figcaption></figcaption></figure>

The **Update Entity** dialogue box is displayed.

2. On the **Update Entity** dialogue box, make the required changes, and then click the **Save** button at the bottom.

<figure><img src="../../../../.gitbook/assets/image (2158).png" alt=""><figcaption></figcaption></figure>

The entity is updated.

</details>

<details>

<summary><strong>Delete Entities</strong></summary>

**Overview**

An entity may be deleted when it becomes obsolete, redundant, or no longer serves a business purpose. Removing unused entities helps maintain an accurate, organized, and manageable metadata repository.&#x20;

**Procedure**

The below step-by-step instructions help you understand how to delete an existing entity:

1. On the **Organization Hierarchy & Roles** page, click the **Delete** button corresponding to the required entity.

<figure><img src="../../../../.gitbook/assets/image (2159).png" alt=""><figcaption></figcaption></figure>

The **Delete** message box is displayed.

2. On the **Delete** message box, review the message, and then click the **Yes, Delete it** button.

<figure><img src="../../../../.gitbook/assets/image (2160).png" alt=""><figcaption></figcaption></figure>

The entity is deleted.

</details>

<details>

<summary><strong>Create Roles and Grant Permissions &#x26; Policies</strong></summary>

**Overview**

A role is created to control user access and define responsibilities within the platform. By assigning permissions to roles rather than individual users, organizations can manage access more efficiently and ensure that users have the appropriate level of access to perform their tasks.

**Procedure**

Creating a role involves three steps: **Enter Role Details**, **Configure Menu Permissions**, and **Configure Policy Permissions**. Together, these steps define the role and its access privileges within the platform.

The below step-by-step instructions help you understand the procedure:

1. **Enter Role Details**

* On the **Organization Hierarchy & Roles** page, click the **Role** tab.

<figure><img src="../../../../.gitbook/assets/image (2163).png" alt=""><figcaption></figcaption></figure>

The **Role** tab is opened.

* On the **Role** ta&#x62;**,** click the **Create Role** button on the top right corner.

<figure><img src="../../../../.gitbook/assets/image (2164).png" alt=""><figcaption></figcaption></figure>

The Permissions & Policies dialogue box is displayed.

* On the **Permissions & Policies** dialogue box, enter the **Role Name, Description**, and then select the **Landing Page**.

> <mark style="color:red;">**Note:**</mark> Selecting the **Landing Page** specifies the default page that the role is directed to when accessing the entity or related functions within the platform.

2. **Grant Menu Permissions**

* After entering the role details, scroll down to the **Menu Permissions** tab.&#x20;
* On the **Menu Permissions** tab, select the permissions for the required **Menu Items** and **Sub-Menu Items**.&#x20;
* If you want to provide permissions to all the **Menu Items** and **Sub-Menu Items**, then select the ![](<../../../../.gitbook/assets/image (2167).png>) checkbox.

<figure><img src="../../../../.gitbook/assets/image (2165).png" alt=""><figcaption></figcaption></figure>

3. **Grant Policy Permissions**

You can grant the role the appropriate access permissions, such as **Add**, **Delete**, **View**, **Clone**, **Edit**, **List**, **DQ, EDA,** **Approve**, **Restore**, and **Deploy** to policies. These permissions help control user access and ensure that users can perform only the actions authorized for their role.

**Procedure**

The below step-by-step instructions help you understand how to grant policy permissions:

> <mark style="color:red;">**Note:**</mark> Unless the user has permission for corresponding menu and sub-menu, the policy permissions cannot be granted.

A. **Granting Add Permissions**

* On the **Policies** tab, expand the **Add** panel, and then select the required checkboxes. For example, Chatbot, Group, Entity, Role, etc.
* If you want to grant permissions to **all,** then select the ![](<../../../../.gitbook/assets/image (2168).png>) checkbox.

<figure><img src="../../../../.gitbook/assets/image (2169).png" alt=""><figcaption></figcaption></figure>

B. **Granting Delete Permissions**

* On the **Policies** tab, expand the **Delete** panel, and then select the required checkboxes.
* If you want to select **all** the checkboxes, then select the ![](<../../../../.gitbook/assets/image (2171).png>)checkbox.

<figure><img src="../../../../.gitbook/assets/image (2170).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> You can use the same procedure to grant other permissions, such as **View**, **Clone**, **Edit**, **List**, **DQ**, **EDA**, **Approve**, **Restore**, and **Deploy**, based on the access requirements of the role.

4. **Save Configuration**

* After entering role details and configuring menu permissions, click the Save button.

<figure><img src="../../../../.gitbook/assets/image (2172).png" alt=""><figcaption></figcaption></figure>

The Role is created and displayed on the Role tab. See the example image below:

<figure><img src="../../../../.gitbook/assets/image (2174).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark>
>
> * To **download** the permissions of a role, click the ![](<../../../../.gitbook/assets/image (2175).png>)button on the Role tab. See the above image.
> * To **view the details of a role**, click the **View Role** ![](<../../../../.gitbook/assets/image (2176).png>)icon corresponding to that role on the Role tab. See the above image.
> * To **update a role**, click the **Edit** ![](<../../../../.gitbook/assets/image (2177).png>) icon corresponding to that role on the Role tab. See the above image.
> * To **delete a role**, click the **Delete** ![](<../../../../.gitbook/assets/image (2178).png>) icon corresponding to that role on the Role tab. See the above image.



</details>

<details>

<summary><strong>View Organization Hierarchy and Node Details</strong></summary>

**Overview**

The **Organizational Hierarchy** view provides a **pictorial** structured representation of the relationships between entities, business units, departments, teams, and roles within the organization.&#x20;

Viewing the organizational hierarchy improves visibility into how entities are organized, facilitates collaboration between teams, and supports effective governance, access management, and decision-making.&#x20;

**Procedure**

The below step-by-step instructions help you understand how to view organizational hierarchy and node details:

1. **Viewing Organization Hierarchy**

* On the **Organization Hierarchy & Roles** page, click the **Organization Hierarchy** tab.

<figure><img src="../../../../.gitbook/assets/image (2179).png" alt=""><figcaption></figcaption></figure>

The **Organization Hierarchy** is displayed graphically.

<figure><img src="../../../../.gitbook/assets/image (2180).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> Understanding the Organizational Hierarchy Diagram
>
> * The **Organizational Hierarchy Diagram** provides a visual representation of the relationships between entities, catalogues, and business processes within the organization.
> * Each box in the hierarchy represents a node, while the connecting lines indicate parent-child relationships.&#x20;
> * This view helps users understand organizational structure, ownership, and the relationships between business functions and data assets.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * You can use the viewing controls, including **Fit**, **Swap**, **Compact**, **Expand All**, **Collapse All**, and **Toggle Full Screen**, to adjust the display of the Organizational Hierarchy diagram as needed.
> * You can also use the **Zoom In** and **Zoom Out** controls to adjust the viewing scale.

2. **Viewing Node and User Details**

* On the **Organizational Hierarchy Diagram**, click on a required node.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2185).png" alt=""><figcaption></figcaption></figure>

The Node Details screen is displayed.

* On the **Node Details** screen, click the **View Details** icon corresponding to Users.

<figure><img src="../../../../.gitbook/assets/image (2187).png" alt=""><figcaption></figcaption></figure>

The Users screen is displayed with user details.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2188).png" alt=""><figcaption></figcaption></figure>



</details>

<details>

<summary><strong>Viewing Domain Hierarchy</strong></summary>

**Overview**

The **Domain Hierarchy** provides a visual representation of the relationships between domains, subdomains, and associated entities. It helps to understand how business areas are structured and how data assets are organized across the enterprise.

Viewing the domain hierarchy improves data discovery, governance, and navigation by providing clear visibility into domain ownership, classifications, and relationships. It also helps to identify related domains and understand the business context of data assets within the organization's data landscape.

**Procedure**

The below step-by-step instructions help you understand how to view domain hierarchy and node details:

1. **Viewing Organization Hierarchy**

* On the **Organization Hierarchy & Roles** page, click the **Domain Hierarchy** tab.

<figure><img src="../../../../.gitbook/assets/image (2189).png" alt=""><figcaption></figcaption></figure>

The **Domain Hierarchy** is displayed graphically.

<figure><img src="../../../../.gitbook/assets/image (2191).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark>**&#x20;Understanding the Organizational Hierarchy Diagram**
>
> * The **Domain Hierarchy Diagram** provides a visual representation of the relationships between domains, subdomains, and associated entities.&#x20;
> * Each node represents a domain-related object, while the connecting lines indicate parent-child relationships.
> * This view helps users understand the structure of business domains, navigate related data assets, and support effective data governance..

> <mark style="color:red;">**Note:**</mark>**&#x20;Understanding Expand/Collapse Controls under the Nodes**
>
> * The **Domain Hierarchy Diagram** provides a visual representation of the relationships between domains, subdomains, and associated entities.&#x20;
> * Each node represents a domain-related object, while the connecting lines indicate parent-child relationships.
> * This view helps users understand the structure of business domains, navigate related data assets, and support effective data governance..

> <mark style="color:red;">**Note:**</mark>**&#x20;Understanding View Controls**
>
> * You can use the viewing controls, including **Fit**, **Swap**, **Compact**, **Expand All**, **Collapse All**, and **Toggle Full Screen**, to adjust the display of the Domain Hierarchy diagram as needed.
> * You can also use the **Zoom In** and **Zoom Out** controls to adjust the viewing scale.

2. **Viewing Domain Details and Audit History**

* On the **Domain Hierarchy Diagram**, click on a required node.  For example, Enterprise data Domain Node.

<figure><img src="../../../../.gitbook/assets/image (2192).png" alt=""><figcaption></figcaption></figure>

The Node Details screen is displayed.

* On the **Node Details** screen, click the **View Details** icon.

<figure><img src="../../../../.gitbook/assets/image (2193).png" alt=""><figcaption></figcaption></figure>

The Domain Details and Audit History tabs are displayed.

* Click the **Audit History** tab to view the audit history.

<figure><img src="../../../../.gitbook/assets/image (2194).png" alt=""><figcaption></figcaption></figure>



</details>

***

## Related Topics

* [**Creating an Organization Entity**](creating-an-organization-entity.md)



[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
