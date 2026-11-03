---
icon: folder-plus
---

# Entity

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

In the context of **data management, metadata management, or a data catalog**, an **Entity** represents a specific business object, concept, or data object that the organization wants to define, manage, and govern.

**Role of an Entity**

An entity serves as a building block for organizing and describing business data. It helps users understand what data represents, how it relates to other data objects, and where it fits within the business context. Entities provide a structured way to model business concepts and establish relationships between them.

***

### **Manage Entities**

{% tabs %}
{% tab title="Update an Existing Entity" %}
**Overview**

An entity should be updated whenever its business, governance, or metadata information changes.&#x20;

Updating an entity ensures that it continues to accurately represent the associated business object and remains aligned with current organizational requirements.

Keeping entity information up to date improves data discoverability, governance, and overall metadata quality.

**Procedure**

The below step-by-step instructions help you understand how to update an existing entity:

1. On the **Entity** page, under the **Organization Entity** tab, click the **Edit** button corresponding to the required entity.

<figure><img src="../../../.gitbook/assets/image (2157).png" alt=""><figcaption></figcaption></figure>

The **Update Entity** dialogue box is displayed.

2. On the **Update Entity** dialogue box, make the required changes, and then click the **Save** button at the bottom.

<figure><img src="../../../.gitbook/assets/image (2158).png" alt=""><figcaption></figcaption></figure>

The entity is updated.
{% endtab %}

{% tab title="Delete an Entity" %}
**Overview**

An entity may be deleted when it becomes obsolete, redundant, or no longer serves a business purpose. Removing unused entities helps maintain an accurate, organized, and manageable metadata repository.&#x20;

**Procedure**

The below step-by-step instructions help you understand how to delete an existing entity:

1. On the **Organization Hierarchy & Roles** page, click the **Delete** button corresponding to the required entity.

<figure><img src="../../../.gitbook/assets/image (2159).png" alt=""><figcaption></figcaption></figure>

The **Delete** message box is displayed.

2. On the **Delete** message box, review the message, and then click the **Yes, Delete it** button.

<figure><img src="../../../.gitbook/assets/image (2160).png" alt=""><figcaption></figcaption></figure>

The entity is deleted.
{% endtab %}

{% tab title="Create Roles and Grant Permissions & Policies" %}
**Overview**

A role is created to control user access and define responsibilities within the platform. By assigning permissions to roles rather than individual users, organizations can manage access more efficiently and ensure that users have the appropriate level of access to perform their tasks.

**Procedure**

Creating a role involves three steps: **Enter Role Details**, **Configure Menu Permissions**, and **Configure Policy Permissions**. Together, these steps define the role and its access privileges within the platform.

The below step-by-step instructions help you understand the procedure:

1. **Enter Role Details**

* On the **Organization Hierarchy & Roles** page, click the **Role** tab.

<figure><img src="../../../.gitbook/assets/image (2163).png" alt=""><figcaption></figcaption></figure>

The **Role** tab is opened.

* On the **Role** ta&#x62;**,** click the **Create Role** button on the top right corner.

<figure><img src="../../../.gitbook/assets/image (2164).png" alt=""><figcaption></figcaption></figure>

The Permissions & Policies dialogue box is displayed.

* On the **Permissions & Policies** dialogue box, enter the **Role Name, Description**, and then select the **Landing Page**.

> <mark style="color:red;">**Note:**</mark> Selecting the **Landing Page** specifies the default page that the role is directed to when accessing the entity or related functions within the platform.

2. **Grant Menu Permissions**

* After entering the role details, scroll down to the **Menu Permissions** tab.&#x20;
* On the **Menu Permissions** tab, select the permissions for the required **Menu Items** and **Sub-Menu Items**.&#x20;
* If you want to provide permissions to all the **Menu Items** and **Sub-Menu Items**, then select the ![](<../../../.gitbook/assets/image (2167).png>) checkbox.

<figure><img src="../../../.gitbook/assets/image (2165).png" alt=""><figcaption></figcaption></figure>

3. **Grant Policy Permissions**

You can grant the role the appropriate access permissions, such as **Add**, **Delete**, **View**, **Clone**, **Edit**, **List**, **DQ, EDA,** **Approve**, **Restore**, and **Deploy** to policies. These permissions help control user access and ensure that users can perform only the actions authorized for their role.

**Procedure**

The below step-by-step instructions help you understand how to grant policy permissions:

> <mark style="color:red;">**Note:**</mark> Unless the user has permission for corresponding menu and sub-menu, the policy permissions cannot be granted.

A. **Granting Add Permissions**

* On the **Policies** tab, expand the **Add** panel, and then select the required checkboxes. For example, Chatbot, Group, Entity, Role, etc.
* If you want to grant permissions to **all,** then select the ![](<../../../.gitbook/assets/image (2168).png>) checkbox.

<figure><img src="../../../.gitbook/assets/image (2169).png" alt=""><figcaption></figcaption></figure>

B. **Granting Delete Permissions**

* On the **Policies** tab, expand the **Delete** panel, and then select the required checkboxes.
* If you want to select **all** the checkboxes, then select the ![](<../../../.gitbook/assets/image (2171).png>)checkbox.

<figure><img src="../../../.gitbook/assets/image (2170).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> You can use the same procedure to grant other permissions, such as **View**, **Clone**, **Edit**, **List**, **DQ**, **EDA**, **Approve**, **Restore**, and **Deploy**, based on the access requirements of the role.

4. **Save Configuration**

* After entering role details and configuring menu permissions, click the Save button.

<figure><img src="../../../.gitbook/assets/image (2172).png" alt=""><figcaption></figcaption></figure>

The Role is created and displayed on the Role tab. See the example image below:

<figure><img src="../../../.gitbook/assets/image (2527).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark>
>
> * To **download** the permissions of a role, click the ![](<../../../.gitbook/assets/image (2528).png>)button on the Role tab. See the above image.
> * To **view the details of a role**, click the **View Role** ![](<../../../.gitbook/assets/image (2176).png>)icon corresponding to that role on the Role tab. See the above image.
> * To **update a role**, click the **Edit** ![](<../../../.gitbook/assets/image (2177).png>) icon corresponding to that role on the Role tab. See the above image.
> * To **delete a role**, click the **Delete** ![](<../../../.gitbook/assets/image (2178).png>) icon corresponding to that role on the Role tab. See the above image.
{% endtab %}

{% tab title="View Organization Hierarchy and Node Details" %}
**Overview**

The **Organizational Hierarchy** view provides a **pictorial** structured representation of the relationships between entities, business units, departments, teams, and roles within the organization.&#x20;

Viewing the organizational hierarchy improves visibility into how entities are organized, facilitates collaboration between teams, and supports effective governance, access management, and decision-making.&#x20;

**Procedure**

The below step-by-step instructions help you understand how to view organizational hierarchy and node details:

1. **Viewing Organization Hierarchy**

* On the **Organization Hierarchy & Roles** page, click the **Organization Hierarchy** tab.

<figure><img src="../../../.gitbook/assets/image (2179).png" alt=""><figcaption></figcaption></figure>

The **Organization Hierarchy** is displayed graphically.

<figure><img src="../../../.gitbook/assets/image (2180).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../../../.gitbook/assets/image (2185).png" alt=""><figcaption></figcaption></figure>

The Node Details screen is displayed.

* On the **Node Details** screen, click the **View Details** icon corresponding to Users.

<figure><img src="../../../.gitbook/assets/image (2187).png" alt=""><figcaption></figcaption></figure>

The Users screen is displayed with user details.&#x20;

<figure><img src="../../../.gitbook/assets/image (2188).png" alt=""><figcaption></figcaption></figure>


{% endtab %}
{% endtabs %}

***

## Related Topics

* [**Catalogue**](../data-catalogue-manager-1/catalogue/)
* [**Domain**](../data-catalogue-manager-1/domain/)
