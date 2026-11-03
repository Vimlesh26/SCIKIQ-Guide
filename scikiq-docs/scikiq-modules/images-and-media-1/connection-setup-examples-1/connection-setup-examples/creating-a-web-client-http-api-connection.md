---
icon: page
---

# Creating a Web Client HTTP API Connection

***

**Contents**

* [**Instructions for Using this Page**](creating-a-web-client-http-api-connection.md#instructions-for-using-this-page)
* [**Overview**](creating-a-web-client-http-api-connection.md#overview)
* [**Procedure**](creating-a-web-client-http-api-connection.md#procedure)
* [**Related Topics**](creating-a-web-client-http-api-connection.md#related-topics)

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]
* At any time during the workflow, you can return to the previous section by clicking the **Previous** <img src="../../../../.gitbook/assets/image (204).png" alt="" data-size="original">button.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

This page explains how to create a **Web Client HTTP API** data source connection in SCIKIQ. The process involves a series of steps, which includes navigating to the Web Client HTTP API connection page, selecting a new or an existing data source, mapping, adding metadata, specifying owner, managed service, and connection type, reviewing the settings, and submitting the connection.

Once the connection is successfully established, the data source will appear on the **Connected Data Sources** page.&#x20;

***

## Procedure

The expandable panels below guide you through the process of creating a **Web Client HTTP API** connection in SCIKIQ. Follow each step in sequence while configuring the connection. The system enables the next step only after the current step is completed.

<details>

<summary>1.<strong>Navigate to Web Client HTTP API</strong></summary>

A. On the **Left Navigation Bar**, expand **Connect to Data Source** under **SCIKIQ CONNECT**, and then click **Manage** **Data Source**.

<figure><img src="../../../../.gitbook/assets/Click Manage Data Source.png" alt="" width="509"><figcaption><p>Manage Data Source Menu Item</p></figcaption></figure>

The All Data Sources page is displayed.

B. On the **All Data Sources** page, click **Files** in the **left menu**, and then click **Web Client HTTP API** in the right pane.

<figure><img src="../../../../.gitbook/assets/S (234).png" alt="" width="563"><figcaption><p>Navigating to Web Client HTTP API</p></figcaption></figure>

The HTTP API page is displayed.&#x20;

</details>

<details>

<summary>2.<strong>Create Connection</strong></summary>

* On the **HTTP API** page, in the **Create Connection** section, select either a **new data source** or an **existing data source** depending on the requirement, and then click the **Next** button. See the below example image.&#x20;

<figure><img src="../../../../.gitbook/assets/S (235).png" alt=""><figcaption><p>Selecting Data Source</p></figcaption></figure>

The Connection Details section is highlighted.

</details>

<details>

<summary>3.<strong>Configure Connection Details</strong></summary>

{% hint style="success" %}
**Tip:** The blue dotted texts in the below headings and instructions are annotations, which provides description about the field options. To view an annotation, simply hover your cursor over it.&#x20;
{% endhint %}

**Overview**

The purpose of configuring connection details ensures that your data reaches the correct destination securely, is accepted by the server, and is easily manageable within your system.

**Procedure**&#x20;

As part of configuring details, you need to input **Base URL, End Point, Display Name, Header, Body, Authorization, Param,** and **SSL Certificate.**  The below step-by-step instructions help you understand the process.

**Step-by-Step Instructions**

{% hint style="info" %}
**Tip:** **How you can get the configuration details**

After an API connection is created, you can copy the Base URL, End Point, Header Key and Value from the  Publish (SCIKIQ Curate>Business Data Models>Publish Icon) window. See the below image.



<p align="center"><img src="../../../../.gitbook/assets/S (236).png" alt="" data-size="original"></p>

&#x20;
{% endhint %}

A. On the **Connection Details page**, from the drop-down box, select the **Post** option.

B. In the [<mark style="color:blue;">**Base URL**</mark>](#user-content-fn-2)[^2] field, enter the **Base URL.** For example, [https://qa4-rtr.scikiq.com/scikiq/](https://qa4-rtr.scikiq.com/scikiq/).

C. In the [<mark style="color:blue;">**End Point**</mark>](#user-content-fn-3)[^3] field, enter the **End Point.**  For example, dataset/DSETCLNT0007000015

D. In the [<mark style="color:blue;">**Display Name**</mark>](#user-content-fn-4)[^4] field, enter the **display name**. For example, Fm\_pro\_LDM.

<figure><img src="../../../../.gitbook/assets/S (237).png" alt=""><figcaption><p>Specifying Base URL, End Point, and Display Name</p></figcaption></figure>

E. In the [<mark style="color:blue;">**Header**</mark>](#user-content-fn-5)[^5], enter [<mark style="color:blue;">**Key**</mark>](#user-content-fn-6)[^6] and [<mark style="color:blue;">**Value**</mark>](#user-content-fn-7)[^7]. See the following image.

F. In the **Body** section, select the required option choosing from [<mark style="color:blue;">**form-data**</mark>](#user-content-fn-8)[^8]<mark style="color:blue;">,</mark> [<mark style="color:blue;">**x-www-form-urlencoded**</mark>](#user-content-fn-9)[^9]<mark style="color:blue;">,</mark> and [<mark style="color:blue;">**raw**</mark>](#user-content-fn-10)[^10]**.**

{% hint style="info" %}
**Tip:**&#x20;

* If you choose either **form-data** or **x-www-form-urlencoded**, then you will have to specify the key and value.
* If you want to select **raw** option, then you will have to choose an option from **Text, JSON,** or **XML**.
{% endhint %}

G. From the [<mark style="color:blue;">**Authorization**</mark>](#user-content-fn-11)[^11] drop-down box, select [<mark style="color:blue;">**API Key**</mark>](#user-content-fn-12)[^12], [<mark style="color:blue;">**Bearer Token**</mark>](#user-content-fn-13)[^13], [<mark style="color:blue;">**Basic Auth**</mark>](#user-content-fn-14)[^14], [<mark style="color:blue;">**OAuth1**</mark>](#user-content-fn-15)[^15], or [<mark style="color:blue;">**OAuth2**</mark>](#user-content-fn-16)[^16].

H. In the [<mark style="color:blue;">**Param**</mark>](#user-content-fn-17)[^17] section, click the **+** button, and then enter Key and Value.

I. In the [<mark style="color:blue;">**SSL Certificate**</mark> ](#user-content-fn-18)[^18]section, click the **Browse** button and, then upload the **SSL Certificate**.

J. Click the **Test** button.&#x20;

<figure><img src="../../../../.gitbook/assets/S (238).png" alt=""><figcaption></figcaption></figure>

The **Connection tested successfully message box** is displayed and the data is displayed in the Response box. See the below image.

K. Click the **Save** butto&#x6E;**.**&#x20;

<figure><img src="../../../../.gitbook/assets/S (239).png" alt=""><figcaption></figcaption></figure>

The Mapper section is activated.

</details>

<details>

<summary>4.<strong>Mapper</strong></summary>

_**Purpose**_&#x20;

The purpose of **mapping** while creating a **Web Client (HTTP API) connection** is to define **how the data received from the API should be understood and used by the system**.&#x20;

_**Procedure**_

Using mapping, you can create data frame (table format). As part of it, you need to select the code and click the Forward arrow button to move it to the right box, and save it.

**Step-by-Step Instructions**

A. In the **Mapper** section, select the **code**, and then click the **Forward** arrow button.

&#x20;   The data frame is created in the right pane.

B. Click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (240).png" alt=""><figcaption><p>Mapping for Creating a Data Frame</p></figcaption></figure>

The Save/Update Data Frame dialogue box is displayed.

C. On the **Save/Update Data Frame** dialogue box, enter a **name** and **description** for the data frame, and then click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (241).png" alt=""><figcaption><p>Saving Data Frame</p></figcaption></figure>

* Click the **Next** button.

The Meta Data section is activated.

</details>

<details>

<summary>5.<strong>Add</strong> <strong>Meta data</strong></summary>

**Purpose**

While connecting the application to a database, adding **metadata** provides the application with important information about the data it will interact with. This metadata helps the system understand, organize, and manage the data correctly.

**Procedure**

As part of the procedure, you need to specify catalogue, connectivity mechanism, store, source system, connection type, supporting email ID, and service type. Once done, you need to test by clicking the Test Connection button to check whether everything is correct.

{% hint style="success" %}
**Tip:** To assist with your setup, fields and options shown in blue are equipped with tooltips. Hovering your mouse over these items will reveal a detailed description of their function.
{% endhint %}

**Step-by-Step Instructions:**

The below step-by-step instructions help you understand how to add meta data.

In the **Add Meta Data** section:

* Specify [<mark style="color:blue;">**Catalogue,**</mark>](#user-content-fn-19)[^19] [<mark style="color:blue;">**Business Owner**</mark>](#user-content-fn-20)[^20]**,** and [<mark style="color:blue;">**Technical Owner**</mark>](#user-content-fn-21)[^21]**.**
* From the [<mark style="color:blue;">**Connectivity Mechanism**</mark>](#user-content-fn-22)[^22] options, select [<mark style="color:blue;">**Secured**</mark>](#user-content-fn-23)[^23]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Unsecured**</mark>](#user-content-fn-24)[^24], or [<mark style="color:blue;">**SSH Tunnelling**</mark>](#user-content-fn-25)[^25]**.**
* From the [<mark style="color:blue;">**Store**</mark>](#user-content-fn-26)[^26] options, select either [<mark style="color:blue;">**Is Feature Store**</mark>](#user-content-fn-27)[^27] or [<mark style="color:blue;">**Is Analytical Store**</mark>](#user-content-fn-28)[^28].
* From the [<mark style="color:blue;">**Source System**</mark>](#user-content-fn-29)[^29] drop-down box, select [<mark style="color:blue;">**Internal**</mark>](#user-content-fn-30)[^30] or [<mark style="color:blue;">**Third Party**</mark>](#user-content-fn-31)[^31].
* From the [<mark style="color:blue;">**Connection Type**</mark>](#user-content-fn-32)[^32] drop-down box, select [<mark style="color:blue;">**Access Layer**</mark>](#user-content-fn-33)[^33]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Source System**</mark>](#user-content-fn-34)[^34]<mark style="color:blue;">**,**</mark> [<mark style="color:blue;">**Reference System,**</mark>](#user-content-fn-35)[^35] or [<mark style="color:blue;">**Master Database**</mark>](#user-content-fn-36)[^36]<mark style="color:blue;">**.**</mark>
* In the **Supporting Email ID** field, specify the **supporting email ID** to contact when something goes wrong or when help is needed.
* From the **Service Type** drop-down box, select the **category of service** the data source provides.
* Specify [<mark style="color:blue;">**Service Id**</mark>](#user-content-fn-37)[^37] and [<mark style="color:blue;">**Application Id**</mark>](#user-content-fn-38)[^38]**.**
* Finally, click the **Test Connection** button to check everything is correct.

The **Connection tested successfully** message is displayed.

* Click the **Next** button.

<figure><img src="../../../../.gitbook/assets/S (242).png" alt=""><figcaption><p>Adding Meta Data</p></figcaption></figure>

The Review & Submit section is activated.

</details>

<details>

<summary>6<strong>.Review &#x26; Submit</strong></summary>

* In the **Review & Submit** section, review the **connection summary**, and then click the **Finish** button to submit it.

<figure><img src="../../../../.gitbook/assets/S (243).png" alt=""><figcaption></figcaption></figure>

The connection is created and the [Connected Data Sources](/broken/pages/dgiZ3ktrQlmTnR2Pq3nV) page is displayed.

</details>

***

## Related Topics

* [**Managing Connected Data Sources**](../../managing-connected-data-sources.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.

[^2]: The **Base URL** is the root address of the API service. It is the "home address" of the server where the API is hosted.

[^3]: The **Endpoint** is the specific path or sub-address appended to the Base URL to reach a particular resource or perform a specific task. While the Base URL gets you to the server, the endpoint gets you to the "specific room" or function.

[^4]: The **Display Name** is a user-friendly label you assign to this specific API connection or integration within a software interface.

[^5]: Header provides **metadata** about the request.

[^6]: This is the **key** to the API. It proves to the server that you have the permission to write data.

[^7]: This refers to the token value.

[^8]: This is primarily used for uploading files (images, PDFs, etc.) or sending complex forms that contain both text and attachments.

[^9]: This is the default format used by standard HTML forms. It is best for simple, text-only data.

[^10]: 

    The **raw** option allows you to send data in a completely custom format. You are responsible for telling the server what that format is by setting a Content-Type header. It is essential for modern APIs that exchange structured data like JSON, XML, or Plain Text.

[^11]: **Authorization** is the process of proving you have the permission to access or modify data.

[^12]: An **API Key** is a unique, long string of characters assigned to a specific user or application.

[^13]: A **Bearer Token** (often a JWT or JSON Web Token) is a security token that gives "the bearer" access to the API.

[^14]: **This is the simplest form of authorization. It uses a Username and Password, which are encoded into a single string.**

[^15]: **OAuth 1.0:** Focuses on security by requiring every request to be digitally signed.&#x20;

[^16]: **OAuth 2.0:** Focuses on developer ease. It uses "Scopes" to define exactly what data the application can see (e.g., "Read-only" vs. "Write").

[^17]: Param (Parameters): These are used to provide additional instructions or filters for the request.

[^18]: **SSL Certificate** ensures a secure, encrypted connection (HTTPS). By configuring the SSL certificate (or choosing to trust one), you protect sensitive data.

[^19]: **Catalogue** refers to the group of related data sources.

[^20]: **Business Owner** refers to the person or team responsible for the data from a business point of view.

[^21]: **Technical Owner** refers to the **person or IT team** responsible for the technical side of the data.

[^22]: Connectivity Mechanism refers to the method used to connect to the data source.

[^23]: **Secured** option refers to the connection where data is encrypted, making it safe from hackers and unauthorized access.

[^24]: **Unsecured** option refers to the connection where data is sent without encryption.

[^25]: SSH Tunneling: SSH refers to Secure Shell. SSH is a secure way to connect to another computer or server over a network.

[^26]: This refers to how the data will be used.

[^27]: Select **Is Feature Store** if the data source is used to store and manage machine learning features.

[^28]: Select **Is Analytical Store** if the data source is primarily used for analytics, reporting, and business intelligence.

[^29]: This refers to the original system where the data comes from.

[^30]: An **Internal source system** is owned, managed, and maintained by your organization.

[^31]: A **Third-Party** source system is owned and managed by an external vendor or service provider.

[^32]: This refers to the kind of connection you are using to access the source.

[^33]: The **Access Layer** represents systems that are used to consume or expose data rather than originate it.

[^34]: A **Source System** is the origin of raw or transactional data.

[^35]: A Reference System stores standardized, lookup, or supporting data used across multiple systems.

[^36]: A **Master Database** stores authoritative master data for key business entities.

[^37]: This refers to the unique identifier for the service you are connecting to.

[^38]: This refers to the unique ID used to identify the application that owns, provides, or uses the data.
