---
icon: page
---

# Deleting Archived Data

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

Archiving preserves historical data for reference and compliance. However, based on the need, deleting it from the operational system improves performance by reducing data volume and speeding up queries. It also supports cost optimization, as primary storage is more expensive than archival storage.&#x20;

Deletion keeps the system clean and manageable by retaining only relevant data and avoiding duplication. Overall, it ensures the system remains efficient and streamlined.

***

### Procedure

The deletion process involves a series of steps. As part of this process, you must first map the required business terms in the Data Dictionary. You can then initiate a data deletion request by selecting the relevant business terms along with the applicable identifier.

Once the request is initiated and the archived table discovery is completed, you can review and confirm the deletion.

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Add Business Terms</strong></summary>

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

&#x20;     The Meta Data Manager menu is displayed.

2. From the **Meta Data Manager** menu, click **Business Terms.**

<figure><img src="../../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

The Business terms page is displayed.

3. On the **Business Terms** page:
   1. Add **Business Terms.**
   2. Perform **Bulk Upload.**
   3. Search **Business Terms.**

<figure><img src="../../../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

4. **Adding a New Business Term**
   1. Click on **Add Business Terms**.
   2. Fill in the required details:

| Field                 | Value                                  |
| --------------------- | -------------------------------------- |
| **Terms Name**        | Customer Account ID                    |
| **Definition**        | Unique identifier for customer account |
| **Purpose**           | Identify customer account              |
| **Business Process**  | AR Process                             |
| **Owner**             | Select Process Owner                   |
| **Catalogue**         | Enterprise Data Catalogue              |
| **Glossary**          | Select Glossary                        |
| **Category**          | Select Category                        |
| **Status**            | Draft                                  |
| **Sensitive**         | PII                                    |
| **Classification**    | Internal                               |
| **Regulatory Rule**   | GDPR                                   |
| **Industry Standard** | FIBO                                   |

<figure><img src="../../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

5. **Physical Schema Mapping**
   1. Click on **Physical Schema Mapping**.
   2. A mapping window will open.

<figure><img src="../../../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

c. Enter the following details:

* **Connection**
* **Table**
* **Column**
* Click **Save**.

<figure><img src="../../../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

6. Final Steps
   1. Click **Add Term**.
   2. The business term will be added.

<figure><img src="../../../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

7. Click **Submit**.
   1. The term will now be saved and added to the list.

<figure><img src="../../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>2.Initiate Data Deletion Request</strong></summary>

**Overview**

**Overview**

The **Initiate** stage is the first step in the deletion workflow where the user defines the scope of data to be deleted. In this stage, the system captures key inputs such as the user/entity identifier, business terms, reason for deletion, and supporting documents.

The defined scope applies across **all data layers**, including:

* **Archived Data**
* **Hot Storage (recent/active archived data)**
* **Cold Storage (long-term retained data)**

This ensures a comprehensive scan and accurate identification of all relevant records.

**Procedure**&#x20;

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival**.
2. Under **SCIKIQ Archival**, expand **Archival Jobs**, and then click **Deletion Jobs**.

<figure><img src="../../../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

&#x20;   The **Archival Deletion History** page is displayed.

3. On the **Archival Deletion History page**, click **+ New Purge Request** button.

<figure><img src="../../../.gitbook/assets/image (1715).png" alt=""><figcaption></figcaption></figure>

The Data Deletion Request page is displayed.

4. On the **Data Deletion Request** page:

A. in the **User/Entity Identifier** field, enter the **User / Entity Identifier.** For example, 1000.

B. From the **Business Terms** drop-down box, select one or more **Business Terms.** For example, Customer Account ID.

C. From the **Reason for Deletion** drop-down box, select an appropriate **reason.** For example, Data Retention policy Expired.

> <mark style="color:red;">**Note:**</mark> Selecting **Reason for Deletion** is mandatory for compliance and audit tracking.

D. Optionally upload a **Supporting Document** (PDF/DOC/Image) for authorization.

<figure><img src="../../../.gitbook/assets/image (1716).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Scope**

The deletion scope includes:

* **All Archived Data** – Data already moved to archival storage
* **Hot Storage** – Frequently accessed or recently archived data
* **Cold Storage** – Long-term, infrequently accessed data

The system scans across all these layers to identify matching records based on the provided inputs.
{% endhint %}

E. Click the **Start Discovery Scan** button to move to the **Scanning** stage.

<figure><img src="../../../.gitbook/assets/image (2136).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>3.Scan Data</strong></summary>

The system starts scanning. See the below image.&#x20;

<figure><img src="../../../.gitbook/assets/image (2137).png" alt=""><figcaption></figcaption></figure>

After the completion of scanning, the **Review stepper** is highlighted.

</details>

<details>

<summary><strong>4.Review Data</strong></summary>

* On the **Review stepper**, select the **table to be deleted**, and then click the **Proceed to Delete** button.

<figure><img src="../../../.gitbook/assets/image (2138).png" alt=""><figcaption></figcaption></figure>

&#x20;     The Confirm stepper is highlighted.

> <mark style="color:red;">**Note:**</mark> Before confirming deletion, you need to configure approval rules. See the next panel.&#x20;
>
> Once configured, the approval section will be displayed in the Confirm Deletion section.

</details>

<details>

<summary><strong>5.Configure Approval Rules</strong></summary>

**Overview**

As part of configuring the approval rules, you need to specify the roles that will act as Approvers and Recommenders. Additionally, you will define the corresponding Action, Accept Status, Reject Status, Priority, and SLA (Days/Hours) for each role to establish the approval workflow and processing timelines.

**Procedure**

1. On the **SCIKIQ Left Navigation Bar**, click **Admin Settings** under **Access Management.**

<figure><img src="../../../.gitbook/assets/image (2141).png" alt=""><figcaption></figcaption></figure>

The **Admin Settings** page is displayed.

2.On the **Admin Settings** page, click the **Resource Approval** tab.

The **Resource Approval** tab is opened.

3.On the **Resource Approval** tab (See the below image):

A. From the **Resource Type** drop-down box, select the required **resource type**.

B. In the Manual Approval section, specify the **Role, Action, Accept Status, Reject Status, Priority,** and **SLA (Days/Hours)** for both the **Approver** and **Recommender** to define the approval workflow, decision outcomes, processing order, and turnaround timelines.

C. If you want to **add** more rows, click the ![](<../../../.gitbook/assets/image (2057).png>)button.

D. If you want to **delete** a row, click the Delete Row ![](<../../../.gitbook/assets/image (2058).png>)button corresponding to it.

E. Finally, click the **Save** button at the bottom.

<figure><img src="../../../.gitbook/assets/image (2059).png" alt=""><figcaption></figcaption></figure>

The approval rules are saved.

F. Follow the same above instructions to configure approval rules for the other resource types.

</details>

<details>

<summary><strong>6.Select Execution Mode</strong> </summary>

**Overview**

You can select the appropriate execution mode based on how matching records should be handled.&#x20;

* **Physically Delete Mode:** The **Physically Delete** mode permanently removes all rows that meet the specified criteria.&#x20;
* **Mask Selected Column Mode:** The **Mask Selected Column** mode preserves the matching rows while masking the values in the selected columns, ensuring that sensitive data is protected without deleting the records.

**Procedure**

The below information describes how to use both **Physically Delete Mode** and **Mask Selected Column** modes:

1. **Using Physically Delete Mode**

A. On the **Confirm stepper,** in the **Execution Mode** section, select **Physically Delete** option.

<figure><img src="../../../.gitbook/assets/image (2139).png" alt=""><figcaption></figcaption></figure>

B. Now, scroll down to the page, and then select in the **Approval Required** sectio&#x6E;**,** select the **Approver** and **Recommender**. See the below image).

C. In the **Type DELETE to confirm** field, enter **DELETE**.

D. Click the **Confirm Delete** button.

<figure><img src="../../../.gitbook/assets/image (2144).png" alt=""><figcaption></figcaption></figure>

***

2. **Using Mask Selected Column Mode**

A. In the **Execution Mode** section, select **Mask Selected Column Mode** option.

B. In the **Columns to Mask** area, select the required **columns** to be masked.

<figure><img src="../../../.gitbook/assets/image (2148).png" alt=""><figcaption></figcaption></figure>

B. Now, scroll down to the page, and then select in the **Approval Required** sectio&#x6E;**,** select the **Approver** and **Recommender**. See the below image).

C. In the **Type MASK to confirm** field, enter **MASK**.

D. Click the **Confirm Mask** button.

<figure><img src="../../../.gitbook/assets/image (2150).png" alt=""><figcaption></figcaption></figure>

The deletion request is raised. See the below image.

<figure><img src="../../../.gitbook/assets/image (2151).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>7.Recommender Review and Actions</strong></summary>

**Overview**

This section is meant for the **Recommender** who will review and take appropriate action on the deletion request. As part of taking the action, the **Recommender** can **recommend, reject,** or **delegate** it to another person.

**Procedure**

1. On the left navigation bar, expand **My Assets,** and then click **Asset Approval.**&#x20;

<figure><img src="../../../.gitbook/assets/image (2061).png" alt=""><figcaption></figcaption></figure>

The **Asset Approval** page is displayed.

2. On the **Asset Approval** page:

**A. Review Request**

* On the left pane, click the required **Approval Request**.

The **Approval Request** details are displayed.

* Review the request details.

**B. Raise Query**

* If you want to raise a query, then write the query in the **Query** box, and then click the **Send** button.

> <mark style="color:red;">**Note:**</mark> Once the query is raised, the request status will be displayed as **Query**.

**C. Take Action**

* If you want to **recommend** the deletion request to the approver, then click the **Recommend** button on the top right side of the page.

> <mark style="color:red;">**Note:**</mark> If you want to reject, then click the **Reject** button. If required, you can also delegate it another person by clicking the **Delegate** button. &#x20;

<figure><img src="../../../.gitbook/assets/image (2094).png" alt=""><figcaption></figcaption></figure>

The request is recommended and goes to the Approver. Its status is displayed as **Recommended**. See the below image.

<figure><img src="../../../.gitbook/assets/image (2093).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>8.Aprover Review and Actions</strong></summary>

**Overview**

This section is meant for the **Approver** who will review and take appropriate action on the deletion request. As part of taking the action, the **Approve** can **approve, reject,** or **delegate** it to another person.

**Procedure**

1. On the left navigation bar, expand **My Assets,** and then click **Asset Approval.**&#x20;

<figure><img src="../../../.gitbook/assets/image (2061).png" alt=""><figcaption></figcaption></figure>

The **Asset Approval** page is displayed.

2. On the **Asset Approval** page:

**A. Review Request**

* On the left pane, click the required **Approval Request**.

The **Approval Request** details are displayed.

* Review the request details.

**B. Raise Query**

* If you want to raise a query, then write the query in the **Query** box, and then click the **Send** button.

> <mark style="color:red;">**Note:**</mark> Once the query is raised, the request status will be displayed as **Query**.

**C. Take Action**

* If you want to **approve** the deletion request, then click the **Approve** button on the top right side of the pag&#x65;**.**

> <mark style="color:red;">**Note:**</mark> If you want to reject, then click the **Reject** button. If required, you can also delegate it another person by clicking the **Delegate** button. &#x20;

<figure><img src="../../../.gitbook/assets/image (2079).png" alt=""><figcaption></figcaption></figure>

The request is approved and its status is displayed as **Approved** on the **Archival Deletion History** page. See the below image.

<figure><img src="../../../.gitbook/assets/image (2095).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>9.Confirm Deletion</strong></summary>

1. On the **Archival Deletion** History page, click the **Confirm Delete** button corresponding to the approved request.

<figure><img src="../../../.gitbook/assets/image (2096).png" alt=""><figcaption></figcaption></figure>

The Confirm Purge Request message is displayed.

2. On the **Confirm Purge Request** message, click the **OK** button.

<figure><img src="../../../.gitbook/assets/image (2097).png" alt=""><figcaption></figcaption></figure>

The system starts purging the request and the request status is displayed as **Purging**. See the below image.

<figure><img src="../../../.gitbook/assets/image (2099).png" alt=""><figcaption></figcaption></figure>



</details>

### Related Topics

* [**Creating a Table Archival Job**](creating-a-table-archival-job.md)
* [**Creating a File Archival Job**](creating-a-file-archival-job.md)
* [**Validating Data**](validating-data.md)
* [**Managing Existing Jobs**](managing-existing-jobs.md)
* [**Retrieving Data**](retrieving-data.md)
* [**Managing Deployment Configs**](managing-deployment-configs.md)
* [**Managing Retention Schedules**](managing-retention-schedules.md)
* [**Using Archival Dashboard**](using-archival-dashboard.md)
* [**Using Cube Manager**](using-cube-manager.md)
* [**Using Cube Viewer**](using-cube-viewer.md)

