---
icon: page
---

# Configuring Execution Settings

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The **Settings** section in the pipeline configuration controls how the pipeline executes, processes data, and displays results. Each option affects the performance, error handling, and data preview behavior of the pipelin&#x65;**.**

***

### **Procedure**

<details>

<summary><strong>Navigating to Execution Settings</strong></summary>

1. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click **Create API Pipeline**.

<figure><img src="../../../../.gitbook/assets/S (286).png" alt=""><figcaption><p>Create API Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

</details>

<details>

<summary><strong>Configuring Execution Settings</strong></summary>

**Overview:**

The **SCiKIQ pipeline execution settings** include **Execute Tasks in Parallel, Continue Job on Error, Stop Job on Empty, Hide SCiKIO Audit Fields, Batch Size, File Batch Size, and Preview Limit**. These settings allow you to control how the pipeline processes data and handles execution behavior during pipeline creation.

**Procedure:**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions**

1. On the **Create Delta Pipeline** page, go to the **Settings** tab on the right side of the application.
2. Refer to the below for description on the execution settings.

<table><thead><tr><th width="228">Setting</th><th>Description</th></tr></thead><tbody><tr><td>Execute Tasks in Parallel</td><td>When this option is enabled, independent tasks within the pipeline are executed at the same time instead of sequentially. This can improve performance and reduce execution time when tasks do not depend on each other.</td></tr><tr><td>Continue Job on Error</td><td>If this option is enabled, the pipeline will skip the failed task and continue executing the remaining tasks. If disabled, the pipeline stops execution when an error occurs.</td></tr><tr><td>Stop Job on Empty</td><td>When enabled, the pipeline automatically stops if the input dataset is empty, preventing unnecessary execution of downstream tasks.</td></tr><tr><td>Hide SCiKIO Audit Fields</td><td>This option removes system-generated audit fields (such as metadata used for tracking operations) from the displayed results, making the output cleaner and easier to read.</td></tr><tr><td>Batch Size</td><td><p>The pipeline processes data in groups rather than one record at a time. The <strong>Batch Size</strong> setting determines how many records are processed per batch, which helps optimize performance when handling large datasets.</p><p>For example, iIf the batch size is <strong>20,000</strong>, the pipeline processes <strong>20,000 records at a time</strong>.</p></td></tr><tr><td>File Batch Size</td><td><p>This setting determines how large each file batch should be when reading or writing files. Processing files in smaller chunks improves memory management and stability </p><p>For example, if the file batch size is <strong>5 MB</strong>, the file is processed in <strong>5-MB segments</strong>.</p></td></tr><tr><td>Preview Limit</td><td><p>When previewing pipeline results, the system shows only a limited number of records to improve performance. The <strong>Preview Limit</strong> determines how many rows are displayed in the preview.</p><p>For example, if the preview limit is <strong>200</strong>, only <strong>200 records</strong> will be displayed in the preview window.</p></td></tr></tbody></table>

<figure><img src="../../../../.gitbook/assets/S (287).png" alt=""><figcaption><p>Execution Settings</p></figcaption></figure>

</details>

## Related Topics

* [**Configuring Input Nodes**](configuring-input-nodes.md)
* [**Applying Transform Nodes**](applying-transform-nodes.md)
* [**Using Output Nodes**](../using-output-nodes/)
