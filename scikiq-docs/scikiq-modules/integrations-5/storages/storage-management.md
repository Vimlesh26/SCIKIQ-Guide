---
hidden: true
icon: table-list
---

# Storage Management

***

**Contents**

* [**Instructions for Using this Page**](storage-management.md#instructions-for-using-this-page)
* [**Overview**](storage-management.md#overview)
* [**About Archival Job**](storage-management.md#about-archival-job)
* [**Related Topics**](storage-management.md#related-topics)

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]

***

### **Overview**

The **AWS Infrastructure Management** screen provides a centralized view of all saved AWS configurations. It allows users to manage, review, update, and delete existing AWS infrastructure setups used for archival and data processing operations.

Once an AWS configuration is successfully created and saved, it becomes available in this listing page under the **Storage Management** sub-menu.

***

### Procedure

The following steps describe how to access, view, and manage **Storages** from the **Storage Management** screen. This includes navigating to the configuration list, searching for specific entries, and performing actions such as editing or deleting configurations.

<details>

<summary><strong>1.Access Storage Management</strong></summary>

**Navigate to Storages Management**

1. Click on **Storage Management.**

<figure><img src="../../../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

The **Storage Management** page is displayed.

</details>

<details>

<summary><strong>2.View Configuration List</strong></summary>

**Overview:**\
This section displays all saved AWS configurations in a structured table format. It helps users quickly identify and manage existing setups.

**Procedure**

The following step-by-step instructions guide you through the process.

1. The system displays the list of saved configurations

<figure><img src="../../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

2. Use the **Search bar** to filter specific records
3. Use **Show entries** to control how many records are displayed per page
4. Key details such as Name, Description, Environment, Updated Date, and Actions are displayed.

<figure><img src="../../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>3.Edit Configuration</strong></summary>

**Overview:**\
This feature allows users to modify an existing AWS configuration without creating a new one. It ensures configurations can be updated based on changing requirements.

**Procedure**

The following step-by-step instructions guide you through the process.

1. In the configuration list, select the required record to update.
2. Click the **Edit (**![](<../../../.gitbook/assets/image (47).png>)**)** icon under the **Actions** column.

<figure><img src="../../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

3. The configuration form opens in editable mode, and a message is displayed indicating that the **configuration loaded successfully.**
4. Update the required fields, such as:
   1. Configuration Name
   2. Environment
   3. Glue Connection
   4. Other AWS-related settings
5. Click **Finish** to save and update the configuration.

<figure><img src="../../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

6. Configuration is update and displayed a success message.

<figure><img src="../../../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>4.Delete Configuration</strong></summary>

**Overview:**\
This feature allows users to permanently remove an AWS configuration from the system when it is no longer required.

**Procedure**

The following step-by-step instructions guide you through the process.

1. Select the required configuration in the list to delete.
2. Click the **Delete (**![](<../../../.gitbook/assets/image (48).png>)**)** icon under the **Actions** column

<figure><img src="../../../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

3. Confirmation dialog is displayed "**Are you sure you want to delete this configuration**
4. Click **Yes** to proceed
5. Configuration is permanently deleted from the list a success message is displayed.

<figure><img src="../../../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

</details>

### Related Topics

* [**Connect SCIKIQ to Source Database**](/broken/pages/NQamWuz7vUgQ2NLWzOdj)
* [**Configure Table Classification**](../../integrations/vs-meta-data-manager/table-classification.md)
* [**Create Compliance Framework**](../compliance/regulatory-compliance.md)
* [**Create Compliance Policy**](../compliance/compliance-policies.md)
* [**Configure AWS Setup**](configure-storage.md)
* [**Create Archival Job**](../archival-jobs-2/creating-a-table-archival-job.md)
* [**Setup Deployment Platform**](../archival-jobs-2/deployment-configs.md)
* [**Deploy Archival Job**](/broken/pages/Lhd7keqyZR2EfkoA5qpT#id-2.deploy-archival-job)
* [**Manage Deployment Configurations**](../archival-jobs-2/deployment-configs.md#manage-deployment-configurations)
* [**Validate Archived Data**](../archival-jobs-2/retrieve-data.md#validate-archived-data)
* [**View Archived Data**](../archival-jobs-2/retrieve-data.md)
* [**Delete Archived Data**](../archival-jobs-2/deletion-jobs.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
