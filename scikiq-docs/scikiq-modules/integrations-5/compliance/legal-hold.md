---
hidden: true
icon: table-cells-row-lock
---

# Legal Hold

***

**Contents**

* [**Instructions for Using this Page**](legal-hold.md#instructions-for-using-this-page)
* [**Overview**](legal-hold.md#overview)
* [**Legal Hold Creation Procedure**](legal-hold.md#legal-hold-creation-procedure)
* [**Related Topics**](legal-hold.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]

### Overview

The Legal Hold feature enables organizations to preserve relevant information when litigation or regulatory review is anticipated. It helps ensure compliance by identifying, classifying, and protecting sensitive data associated with legal matters.

Using this feature, organizations can create and manage Legal Holds by defining legal details, assigning custodians, specifying preservation timelines, and determining the scope of data to be retained through business terms.

{% hint style="danger" %}
**Once a Legal Hold is applied, the associated records cannot be deleted or modified from the system or source files until the hold is released.**
{% endhint %}

### **Legal Hold Creation** Procedure

The procedure to create a Legal Hold in the system, involves a series of steps includes including entering required legal details, assigning custodians, and defining preservation timelines. It also allows users to specify the data scope using business terms and apply relevant filters. By following this process, users can ensure that all required information is accurately captured for legal and compliance purposes.

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Create Legal Hold</strong></summary>

**Overview**

The Create Legal Hold page enables you to define and configure a new legal hold by **providing basic legal information**, **assigning custodians, setting preservation timelines, specifying physical schema mappings**, and **configuring approval rule mappings**.&#x20;

**Procedure**

The following step-by-step instructions guide you through the process.

**Step-by-Step Instructions**

**1.Provide Basic Information**

**A.** On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival.**&#x20;

**B.** Under S**CIKIQ Archival,** expand **Compliance Jobs**, and then click **Legal Hold.**

<figure><img src="../../../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure>

The **Legal Hold Management** page is displayed.

**C.** On the **Legal Hold Management** page, click on **+Create Hold.**

<figure><img src="../../../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>

**D.** In the **Basic Information** section:

* Enter the **Hold Title**, **Description**, **Matter Name** (if applicable), and **Matter Number**.
* Select the **Hold Type** and **Priority**, and  **Status** (default is Draft).

<figure><img src="../../../.gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure>

6. In the Ownership section, select the **Legal Counsel** and choose one or more **Custodians.**

<figure><img src="../../../.gitbook/assets/image (74).png" alt=""><figcaption></figcaption></figure>

7. In the Date Configuration section, enter the **Issued Date**, **Effective Date**, **Preservation Period From**, and **Preservation Period To**, or enable **Mark as Ongoing** if no end date is required.

<figure><img src="../../../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure>

8. In the Data Scope section, select the **Business Term, choose** the **Operator**, and enter the **Value**.&#x20;
9. Upon selecting the Business Term, it automatically opens the **physical schema mapping.**

<figure><img src="../../../.gitbook/assets/image (76).png" alt=""><figcaption></figcaption></figure>

10. Check all entered details and click on **Create Legal Hold**.

<figure><img src="../../../.gitbook/assets/image (77).png" alt=""><figcaption></figcaption></figure>

11. Legal Hold is successfully created and displayed in the Legal Hold list.

<figure><img src="../../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>2.Legal Hold List Page</strong></summary>

**Overview**

The Legal Hold Management page provides a centralized view of all legal holds created in the system. It enables users to monitor hold activity, track key metrics, and manage existing legal holds through actions such as viewing, editing, and deleting.

At the top of the page, summary metrics provide a quick snapshot:

* **Active Holds** – Displays the number of currently active legal holds
* **Preserved Items** – Indicates the total number of items under preservation
* **Pending Review** – Shows the number of legal holds awaiting review

**Procedure**

The following step-by-step instructions guide you through the process.

**Step-by-Step Instructions**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival.**&#x20;
2. Under S**CIKIQ Archival,** expand **Compliance Jobs**, and then click **Legal Hold.**

<figure><img src="../../../.gitbook/assets/image (69).png" alt=""><figcaption></figcaption></figure>

3. The **Legal Hold Management** page is displayed.

<figure><img src="../../../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>

4. **View Summary Metrics**
   1. At the top of the page, review key indicators:
      1. Active Holds
      2. Preserved Items
      3. Pending Review

<figure><img src="../../../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

5. **Perform Actions**
   1. In the **Actions** column:
      1. Click **View** to open details
      2. Click **Edit** to modify the legal hold
      3. Click **Delete** to remove the legal hold

<figure><img src="../../../.gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>

6. In the **Actions** column, click on **Delete**

<figure><img src="../../../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>

7. A confirmation popup is displayed: **“Are you sure you want to delete "name" legal hold?”**
8. Click on **Confirm / Yes** to proceed with deletion

<figure><img src="../../../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>

9. Selected legal hold is deleted.&#x20;
10. success message is displayed: **“Legal Hold has been deleted successfully”**

<figure><img src="../../../.gitbook/assets/image (85).png" alt=""><figcaption></figcaption></figure>

</details>

## Related Topics

* [**Regulatory Compliance**](regulatory-compliance.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
