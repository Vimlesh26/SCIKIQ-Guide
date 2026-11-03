---
icon: page
---

# Domain

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

This page describes how to manage domains and subdomains. A **Domain** is a high-level business area that groups related data assets, such as Customer, Product, Finance, and Sales.

A **Subdomain** is a specific category within a domain. For example, the Customer domain may include Personal Information, Contact Details, and Purchase History.

Domains and subdomains organize enterprise data, simplify governance, and improve data discovery.

***

## **Managing Domains**

You can manage domains by **adding new domains, viewing relationship, updating** and **deleting existing domains.**

Select the tabs below for step-by-step instructions on each task.

{% tabs %}
{% tab title="Adding a Domain" %}
**Overview**

This section describes how to add a domain. A **Domain** is created to logically group related data assets under a common business area. It provides a structured way to organize information, making data easier to discover, manage, govern, and understand across the organization.&#x20;

Domains also help assign ownership, enforce data governance policies, and improve collaboration between business and technical teams.

***

**Procedure**

Adding a domain involves three steps: **Navigating to the domain page, entering the domain details,** and **configuring the approval mapping.**

Follow the step-by-step instructions below to add a domain.

{% stepper %}
{% step %}
**Navigate to Domain Page**

On the **SCIKIQ Left Navigation Bar**, expand **Data Catalogue Manager**, and then click **Domain.**

<figure><img src="../../../.gitbook/assets/image (2126).png" alt=""><figcaption></figcaption></figure>

The **Domain** page is displayed.
{% endstep %}

{% step %}
**Enter Domain Details**

1. On the **Domain** page, click the **Add Domain** button on the top right corner.

<figure><img src="../../../.gitbook/assets/image (3033).png" alt=""><figcaption></figcaption></figure>

The **Add Domain** dialogue box is displayed.

3. On the **Add Domain** dialogue box, specify **Domain Name, Domain Description, Domain (Data Domain or Sub Domain), Parent Domain, Domain Owner,** and then click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (3037).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> Here is the description for **Data Domain, Subdomain,** and **Delegate:**
>
> * **Data Domain:** A **Data Domain** is a high-level business category that groups related data assets based on a common subject area, function, or business capability. **Example:** Customer, Finance, Sales, Human Resources.
> * **Subdomain:** A **Subdomain** is a more specific subdivision of a data domain that groups related data within a particular business area. **Example:** Within the Customer domain, subdomains may include Personal Information, Contact Details, and Purchase History.
{% endstep %}

{% step %}
**Configure Approval Mapping**

1. Scroll down to the **Approval Mapping** section, and then select the **Recommender** and **Approver**.
2. Click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (3038).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

The domain is added. See the below example image.

<figure><img src="../../../.gitbook/assets/image (3039).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Viewing Sub Domain Details" %}
**Overview**&#x20;

This section describes how to view the sub domain details of a domain. **Viewing subdomain details** of a domain helps to understand how the domain is organized and review the associated subdomain information to ensure data assets are classified correctly.

**Procedure**

The below step-by-step instructions help you understand how to view sub domain details:

1. On the **SCIKIQ Left Navigation Bar**, expand **Data Catalogue Manager**, and then click **Domain.**

<figure><img src="../../../.gitbook/assets/image (2126).png" alt=""><figcaption></figcaption></figure>

The **Domain** page is displayed.

2. On the **Domain** page, click the **View Relationship** icon corresponding to the required domain.

<figure><img src="../../../.gitbook/assets/image (3065).png" alt=""><figcaption></figcaption></figure>

The sub domain information is displayed. See the image below.

<figure><img src="../../../.gitbook/assets/image (3066).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> The central node (**Enterprise Entity**) represents an entity associated with the selected subdomain. Connected nodes and relationships can be explored using the hierarchy navigation and viewing controls.
>
> See the below description:
>
> **Viewing Options**
>
> * **Highlight** – Search for and highlight specific nodes within the hierarchy, making it easier to locate entities of interest.
> * **Fit to Screen** (Refresh/Fit Icon) – Adjusts the view to display the entire hierarchy within the available viewing area.
> * **Swap Orientation** – Changes the layout orientation of the hierarchy, such as switching between horizontal and vertical views.
> * **Compact View** – Reduces spacing between nodes to display more hierarchy information within the visible area.
> * **Collapse All** – Collapses all expanded nodes in the hierarchy, providing a simplified overview of the structure.
> * **Expand All** – Expands all nodes to display the complete hierarchy and all related entities.
> * **Toggle Full Screen** – Expands the hierarchy viewer to full-screen mode for improved visibility and navigation.
>
> **Navigation Controls**
>
> * **Home** – Returns the hierarchy view to its default position and zoom level.
> * **Zoom In** – Increases the zoom level to view hierarchy details more closely.
> * **Zoom Out** – Decreases the zoom level to view a larger portion of the hierarchy.
> * **Legends** – Displays the legend panel, which explains the meaning of node colors, icons, and relationship indicators used in the hierarchy.
{% endtab %}

{% tab title="Updating a Domain" %}
**Overview**

This section describes how to update a domain. A domain may need to be updated when its information, ownership, governance details, or business context changes over time.&#x20;

Updating a domain helps ensure that domain metadata remains accurate, relevant, and aligned with current organizational requirements.

> <mark style="color:red;">**Note:**</mark> You can update a domain when it is in **Draft** status only.

**Procedure**

The below step-by-step instructions help you understand how to update an existing domain:

1. On the **Domains** page, click the **Edit** button corresponding to the required domain.

<figure><img src="../../../.gitbook/assets/image (3195).png" alt=""><figcaption></figcaption></figure>

The **Edit** **Domain** dialogue box is displayed.

2. On the **Edit** **Domain** dialogue box, make the required changes, and then click the **Save** button at the bottom.

<figure><img src="../../../.gitbook/assets/image (2133).png" alt=""><figcaption></figcaption></figure>

The domain is updated.
{% endtab %}

{% tab title="Deleting a Domain" %}
**Purpose**

This section describes how to delete a domain. A domain may be deleted when it becomes obsolete, redundant, or no longer serves a business purpose. Removing unused domains helps keep the domain structure accurate, organized, and easy to manage.

> <mark style="color:red;">**Note:**</mark> You can delete a domain when it is in **Draft** status only.

**Procedure**

The below step-by-step instructions help you understand how to delete an existing domain:

1. On the **Domains** page, click the **Delete** button corresponding to the required domain.

<figure><img src="../../../.gitbook/assets/image (3193).png" alt=""><figcaption></figcaption></figure>

The **Sub Domain Delete** message box is displayed.

2. On the **Sub Domain Delete** message box, review the message, and then click the **Yes** button.

<figure><img src="../../../.gitbook/assets/image (2135).png" alt=""><figcaption></figcaption></figure>

The domain is deleted.
{% endtab %}
{% endtabs %}



***

## Related Topics

* [**Catalogue**](../../integrations/data-catalogue-manager-1/catalogue/)
* [**Entity**](../../integrations/data-catalogue-manager-1/entity/)
