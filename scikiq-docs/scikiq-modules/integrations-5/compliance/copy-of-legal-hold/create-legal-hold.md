---
icon: page
---

# Create Legal Hold

***

**Contents**

* [**Instructions for Using this Page**](create-legal-hold.md#instructions-for-using-this-page)
* [**Overview**](create-legal-hold.md#overview)
* [**Legal Hold Creation Procedure**](create-legal-hold.md#legal-hold-creation-procedure)
* [**Related Topics**](create-legal-hold.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]

***

### Overview

Creating a Legal Hold in the system involves a series of configuration steps to ensure the proper preservation and management of information related to legal or regulatory matters.&#x20;

The process includes specifying basic legal hold details, assigning custodians and legal information, defining relevant dates and preservation periods, configuring physical schema mappings to identify the data to be preserved, and setting up approval rule mappings to support the review and authorization workflow.

{% hint style="danger" %}
**Once a Legal Hold is applied, the associated records cannot be deleted or modified from the system or source files until the hold is released.**
{% endhint %}

### **Legal Hold Creation** Procedure

The expandable panels below guide you through the legal hold creation procedure.

<details>

<summary><strong>1.Specify Basic Legal Hold Details</strong></summary>

**Purpose**

The purpose is to define the legal hold and capture key information such as its name, description, matter type, and business context. This helps uniquely identify and manage the legal hold throughout its lifecycle.

**Procedure**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival.**&#x20;
2. Under S**CIKIQ Archival,** expand **Compliance Jobs**, and then click **Legal Hold.**

<figure><img src="../../../../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure>

The **Legal Hold Management** page is displayed.

3. On the **Legal Hold Management** page, click on **"+Create Hold"**

<figure><img src="../../../../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>

4. In the **Basic Information** section, enter the **Hold Title**, **Description**, **Matter Name** (if applicable), and **Matter Number**.
5. Then, select the **Hold Type** and **Priority**, and  **Status** (default is Draft).

<figure><img src="../../../../.gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure>



</details>

<details>

<summary><strong>2.Assign Custodians and Legal Information</strong></summary>

**Purpose**

The purpose is to identify the individuals, departments, or entities responsible for the relevant data and to associate the hold with specific legal matters. This ensures that all affected parties and legal requirements are properly tracked.

**Procedure**

* On the same page (**Create Legal Hold** page), in the **Custodians and Legal Information,** select the **Legal Counsel** and choose one or more **Custodians.**

<figure><img src="../../../../.gitbook/assets/image (1991).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>3.Define Dates and Preservation Period</strong></summary>

**Purpose**

The purpose is to specify when the legal hold becomes effective and how long the relevant data must be preserved. This helps ensure compliance with legal and regulatory retention requirements.

**Procedure**

1. In the **Dates and Preservation Period** section, enter the **Issued Date**, **Effective Date**, **Preservation Period From**, and **Preservation Period To.**
2. If no end date is required, enable the **Mark as Ongoing** checkbox.

<figure><img src="../../../../.gitbook/assets/image (1992).png" alt=""><figcaption></figcaption></figure>



</details>

<details>

<summary><strong>4.Configure Physical Schema Mapping</strong></summary>

**Purpose**

The purpose is to identify and map the physical data sources, repositories, or systems that contain information subject to the legal hold. This ensures that the appropriate data is located and preserved.

**Procedure**

1. In the **Physical Schema Mapping** section, select the **Business Term, choose** the **Operator**, and enter the **Value**.&#x20;

The Connection, Operator, and Value fields are displayed.

2. Specify the **Connection**, **Operator**, and **Value.**

{% hint style="info" %}
**Tip:**

* For more physical schema mapping rows, click the ![](<../../../../.gitbook/assets/image (1994).png>)button.
* To delete a  physical schema mapping row, click the **Remove Row** ![](<../../../../.gitbook/assets/image (1995).png>) button.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/image (76).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>5.Set up Approval Rule Mapping</strong></summary>

**Purpose**

The purpose is to define the approval workflow and designate the reviewers or approvers responsible for authorizing legal hold actions. This helps maintain governance, accountability, and compliance with organizational processes.

**Procedure**

1. In the **Approval Mapping** section, select the **Approver** and **Recommender**.
2. Click the **Create Hold** button.

<figure><img src="../../../../.gitbook/assets/image (1996).png" alt=""><figcaption></figcaption></figure>

The Legal Hold is successfully created and displayed in the Legal Hold list.

<figure><img src="../../../../.gitbook/assets/image (1997).png" alt=""><figcaption></figcaption></figure>

</details>

## Related Topics

* [**Manage Legal Hold**](../legal-hold-1/manage-legal-hold.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
