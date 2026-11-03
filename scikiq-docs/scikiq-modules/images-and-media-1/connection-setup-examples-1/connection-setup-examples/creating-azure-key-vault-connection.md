---
icon: page
---

# Creating Azure Key Vault Connection

***

**Contents**

* [**Instructions for Using this Page**](creating-azure-key-vault-connection.md#instructions-for-using-this-page)
* [**Overview**](creating-azure-key-vault-connection.md#overview)
* [**Procedure**](creating-azure-key-vault-connection.md#procedure)
* [**Related Topics**](creating-azure-key-vault-connection.md#related-topics)

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]
* At any time during the workflow, you can return to the previous section by clicking the **Previous** <img src="../../../../.gitbook/assets/image (204).png" alt="" data-size="original">button.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

Creating an **Azure Key Vault** connection involves a series of steps, including navigating to the Azure Key Vault page, selecting a new or existing data source, configuring the connection details, setting the discovery options, specifying owner, managed service, and connection type, reviewing the settings, and submitting the connection.

Once the connection is successfully established, the data source will appear on the **Connected Data Sources** page.&#x20;

***

## Procedure

Expand the panels below to view step-by-step instructions.

<details>

<summary><strong>Navigate to Azure Key Vault Page</strong></summary>

1. On the **Left Navigation Bar**, expand **Connect to Data Source** under **SCIKIQ CONNECT**, and then click **Manage** **Data Source**.

<figure><img src="../../../../.gitbook/assets/image (2340).png" alt=""><figcaption></figcaption></figure>

The All Data Sources page is displayed.

2. On the **All Data Sources** page:

A. In the **Search** field, enter **Azure Key Vault.**

The Azure Key Vault is displayed.

B. Next, click **Azure Key Vault.**

<figure><img src="../../../../.gitbook/assets/image (2341).png" alt=""><figcaption></figcaption></figure>

The **Azure Key Vault** page is displayed. See the next panel.

</details>

<details>

<summary><strong>Select New Data Source Option</strong></summary>

* On the **Azure Key Vault** page, select the **No. I'd like to create a new data source** option, and then click the **Next** button.

<figure><img src="../../../../.gitbook/assets/image (2342).png" alt=""><figcaption></figcaption></figure>

The Connection Details section is displayed.

</details>

<details>

<summary><strong>Configure Connection Details</strong></summary>

**Purpose**

Configuring the connection details is an essential step in creating an Azure Key Vault connection. It specifies the connection and authentication information required to identify the target Key Vault and authenticate the application. Providing these details enables the application to securely retrieve and manage secrets stored in the Azure Key Vault.

**Procedure**

The below step-by-step instructions help you understand how to configure connection details:

_**Step-by-Step Instructions:**_

1. On the **Connection Details** section, specify **Vault Name, Display Name, Vault URL, Authentication Mode, Tenant ID, Client ID,** and **Client Secret.** See the below example table.

> <mark style="color:red;">**Note:**</mark> Refer to the below table for the description of above fields.

2. Click the **Next** button.

<figure><img src="../../../../.gitbook/assets/image (2344).png" alt=""><figcaption></figcaption></figure>

**Field Description**

<table><thead><tr><th width="135.22222900390625" valign="top">Field Name</th><th valign="top">Description</th><th valign="top">Instruction</th></tr></thead><tbody><tr><td valign="top">Vault Name</td><td valign="top">Refers to the <strong>name of the Azure Key Vault</strong> to which you want to connect.</td><td valign="top">Enter the <strong>exact name</strong> of the Key Vault created in your Azure subscription.</td></tr><tr><td valign="top">Display Name</td><td valign="top">Refers to the <strong>name</strong> is displayed in the application.</td><td valign="top">Enter a user-friendly name for the connection.</td></tr><tr><td valign="top">Vault URL</td><td valign="top">Refers to the <strong>URL (endpoint)</strong> of the Azure Key Vault.</td><td valign="top">Enter the <strong>complete Key Vault URL</strong> provided by Azure.</td></tr><tr><td valign="top">Authentication Mode</td><td valign="top">Refers to the <strong>authentication method used to connect</strong> to the Azure Key Vault.</td><td valign="top">Select the <strong>appropriate authentication</strong> mode based on your Azure configuration.</td></tr><tr><td valign="top">Tenant ID</td><td valign="top">Refers to  the <strong>Microsoft Entra ID (Azure Active Directory) Tenant ID</strong> associated with the Azure subscription. This identifies the Azure tenant used for authentication.</td><td valign="top">Enter the <strong>Microsoft Entra ID (Azure Active Directory) Tenant ID</strong> associated with the Azure subscription.</td></tr><tr><td valign="top">Client ID</td><td valign="top">Refers to the <strong>Application (Client) ID of the registered Azure application</strong> (Service Principal) used to authenticate the connection</td><td valign="top">Enter the <strong>Application (Client) ID.</strong></td></tr><tr><td valign="top">Client Secret</td><td valign="top">Refers to the <strong>secret value associated with the Azure App Registration</strong> (Service Principal).</td><td valign="top">Enter the <strong>secret value</strong> generated for the Azure App Registration (Service Principal) in the Microsoft Entra admin center.</td></tr></tbody></table>



</details>

<details>

<summary><strong>Add Meta data</strong></summary>

**Purpose**

While creating a connection, adding **metadata** provides the application with important information about the data it will interact with. This metadata helps the system understand, organize, and manage the data correctly.

**Procedure:**

As part of the procedure, you need to specify catalogue, connectivity mechanism, store, source system, connection type, supporting email ID, and service type. Once done, you need to test by clicking the Test Connection button to check whether everything is correct.

{% hint style="success" %}
**Tip:** To assist with your setup, fields and options shown in blue are equipped with tooltips. Hovering your mouse over these items will reveal a detailed description of their function.
{% endhint %}

_**Step-by-Step Instructions:**_

The below step-by-step instructions help you understand how to add meta data.

In the **Add Meta Data** section:

* Specify [<mark style="color:blue;">**Catalogue,**</mark>](#user-content-fn-2)[^2] [<mark style="color:blue;">**Business Owner**</mark>](#user-content-fn-3)[^3]**,** and [<mark style="color:blue;">**Technical Owner**</mark>](#user-content-fn-4)[^4]**.**
* From the [<mark style="color:blue;">**Connectivity Mechanism**</mark>](#user-content-fn-5)[^5] options, select [<mark style="color:blue;">**Secured**</mark>](#user-content-fn-6)[^6]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Unsecured**</mark>](#user-content-fn-7)[^7], or [<mark style="color:blue;">**SSH Tunnelling**</mark>](#user-content-fn-8)[^8]**.**
* From the [<mark style="color:blue;">**Store**</mark>](#user-content-fn-9)[^9] options, select either [<mark style="color:blue;">**Is Feature Store**</mark>](#user-content-fn-10)[^10] or [<mark style="color:blue;">**Is Analytical Store**</mark>](#user-content-fn-11)[^11].
* From the [<mark style="color:blue;">**Source System**</mark>](#user-content-fn-12)[^12] drop-down box, select [<mark style="color:blue;">**Internal**</mark>](#user-content-fn-13)[^13] or [<mark style="color:blue;">**Third Party**</mark>](#user-content-fn-14)[^14].
* From the [<mark style="color:blue;">**Connection Type**</mark>](#user-content-fn-15)[^15] drop-down box, select [<mark style="color:blue;">**Access Layer**</mark>](#user-content-fn-16)[^16]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Source System**</mark>](#user-content-fn-17)[^17]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Reference System,**</mark>](#user-content-fn-18)[^18] or [<mark style="color:blue;">**Master Database**</mark>](#user-content-fn-19)[^19]<mark style="color:blue;">**.**</mark>
* In the **Supporting Email ID** field, specify the **supporting email ID** to contact when something goes wrong or when help is needed.
* From the **Service Type** drop-down box, select the **category of service** the data source provides.
* Specify [<mark style="color:blue;">**Service Id**</mark>](#user-content-fn-20)[^20] and [<mark style="color:blue;">**Application Id**</mark>](#user-content-fn-21)[^21]**.**
* Finally, click the **Test Connection** button to check everything is correct.

The **Connection tested successfully** message is displayed.

* Click the **Next** button.

</details>

<details>

<summary><strong>Specify Owner, Managed Service, and Connection Type</strong></summary>

**Purpose**

The purpose of configuring the Owner, Managed Service, and Connection Type is to define the ownership, service context, and connection method for the Azure Key Vault connection. These settings ensure that the connection is properly managed, associated with the appropriate service, and configured using the correct connection type.

The below step-by-step instructions help you understand the procedure:

_**Step-by-Step Instructions:**_

* In the **Configuration** section, select the **owner** choosing from **Owner** or **Third Party**.
* Select the [<mark style="color:blue;">**Manage Service**</mark>](#user-content-fn-22)[^22] choosing from [<mark style="color:blue;">**Service Managed**</mark>](#user-content-fn-23)[^23] or [<mark style="color:blue;">**User Managed**</mark>](#user-content-fn-24)[^24].
* Select the **Connection type** choosing from **Secured Connection** or **Unsecured Connection.**
* In the [<mark style="color:blue;">**DR**</mark>](#user-content-fn-25)[^25] Available section, select **Yes** or **No**.&#x20;
* In the [<mark style="color:blue;">**RBAC**</mark>](#user-content-fn-26)[^26] Implemented section, select **Yes** or **No**.
* Click the **Next** button.

<figure><img src="../../../../.gitbook/assets/image (2345).png" alt=""><figcaption></figcaption></figure>

The Review & Submit section is displayed. See the next panel.

</details>

<details>

<summary><strong>Review and Submit</strong></summary>

* As the final step, review the details, and then click the **Finish** button to submit it.

<figure><img src="../../../../.gitbook/assets/image (2346).png" alt=""><figcaption></figcaption></figure>

The connection is created and the [**Connected Data Sources**](../../managing-connected-data-sources.md) page is displayed.

</details>

***

## Related Topics

* [**Managing Connected Data Sources**](../../managing-connected-data-sources.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.

[^2]: **Catalogue** refers to the group of related data sources.

[^3]: **Business Owner** refers to the person or team responsible for the data from a business point of view.

[^4]: **Technical Owner** refers to the **person or IT team** responsible for the technical side of the data.

[^5]: Connectivity Mechanism refers to the method used to connect to the data source.

[^6]: **Secured** option refers to the connection where data is encrypted, making it safe from hackers and unauthorized access.

[^7]: **Unsecured** option refers to the connection where data is sent without encryption.

[^8]: SSH Tunneling: SSH refers to Secure Shell. SSH is a secure way to connect to another computer or server over a network.

[^9]: This refers to how the data will be used.

[^10]: Select **Is Feature Store** if the data source is used to store and manage machine learning features.

[^11]: Select **Is Analytical Store** if the data source is primarily used for analytics, reporting, and business intelligence.

[^12]: This refers to the original system where the data comes from.

[^13]: An **Internal source system** is owned, managed, and maintained by your organization.

[^14]: A **Third-Party** source system is owned and managed by an external vendor or service provider.

[^15]: This refers to the kind of connection you are using to access the source.

[^16]: The **Access Layer** represents systems that are used to consume or expose data rather than originate it.

[^17]: A **Source System** is the origin of raw or transactional data.

[^18]: A Reference System stores standardized, lookup, or supporting data used across multiple systems.

[^19]: A **Master Database** stores authoritative master data for key business entities.

[^20]: This refers to the unique identifier for the service you are connecting to.

[^21]: This refers to the unique ID used to identify the application that owns, provides, or uses the data.

[^22]: **Manage Service** refers to who is responsible for managing the connection and its configuration.

[^23]: **Service Managed** means the system automatically manages the service for you.

[^24]: **User Managed** means you manage the service configuration yourself.

[^25]: <mark style="color:blue;">**DR**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">refers to</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**Disaster Recovery**</mark>

[^26]: **RBAC** refers to **Role-Based Access Control**.
