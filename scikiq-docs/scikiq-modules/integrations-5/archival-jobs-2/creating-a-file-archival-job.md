---
icon: page
---

# Creating a File Archival Job

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

**File Archival** enables securely moving files from a configured source location to a designated target storage location for long-term retention and management. It provides a structured process for identifying, transferring, and managing files based on defined archival configurations.

A **File Archival Job** defines the source, file selection criteria, target storage, and execution settings required to archive files. The source can be configured using **SFTP or S3**, while the target can be configured based on the supported storage options.

***

### Procedure

The File Archival process typically includes the following key configurations:

* **Source** – Specifies where the files to be archived are located.
* **File Selection** – Defines the files to be archived using include and exclude patterns and other applicable criteria.
* **Target & Storage** – Specifies the destination where the archived files are stored.
* **Run Options & Deployment** – Defines how and when the archival job is executed and deployed.
* **Review & Save** – Enables users to review the configured settings and save the archival job.

Together, these configurations enable users to **define, execute, and manage the file archival process in a controlled and systematic manner**..

Click on the below tabs to view step-by-step instructions:

{% tabs %}
{% tab title="1. Navigate to New File Archival Job Page" %}
The below step-by-step instructions help you understand how to navigate to File Archival page:

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival.**&#x20;
2. Under S**CIKIQ Archival,** expand **Archival Jobs**, and then click **Existing Jobs**.

<figure><img src="../../../.gitbook/assets/image (2831).png" alt=""><figcaption></figcaption></figure>

The **Existing Jobs** page displayed.

3. On the **Existing Jobs** page, click the **New File Archival Job** button.

<figure><img src="../../../.gitbook/assets/image (2833).png" alt=""><figcaption></figcaption></figure>

The **New File Archival Job** page is displayed with **Source** stage is selected by default.

4. Next, Select Source.
{% endtab %}

{% tab title="Select Source" %}
**Overview**

When creating a **File Archival Job**, selecting the **Source** determines where the files to be archived are retrieved from. You can configure the source using either **SFTP** or **S3**.

As part of the **Source** configuration, specify the **File Archival Job** name and **Description**, select the **Source Type** (SFTP or S3), and configure the required connection settings.

These settings enable the archival process to connect to the specified source and identify the files that need to be archived.&#x20;

**Procedure**

The below step-by-step instructions help understand how to select and configure source settings:

_**To select and configure source settings**_

1. On the **New File Archival Job** page, under **Source** stage:

A.  **Specify Archival Job Name and Description**

* In the **Job** section, specify **Archival Job Name** and **Description**.

B. **Select Source**

* In the **Source** section, select either **Copy from SFTP** or **Files already in S3 (catalogue only)** option.

**C. If you want to copy files from SFTP:**

* Select the **Copy from SFTP** optio&#x6E;**.**
* From the **SFTP Connection** drop-down box, select the **SFTP Connection** from which the file should be copied.
* In the **Root Path** field, specify the **root path** of the SFTP.

> <mark style="color:red;">**Note:**</mark> Specifying the Root Path tells the application where to look for files on the SFTP server.

* In the **Include Patterns** field, specify the file **name pattern** or **file extension** of the files to be archived.

> <mark style="color:red;">**Note:**</mark> If you want to specify multiple file patterns for inclusion, separate them with a comma.&#x20;

* In the **Exclude Patterns** field, specify the file **name pattern** or **file extension** of the files that are to be excluded from archival.

> <mark style="color:red;">**Note:**</mark> If you want to specify multiple file patterns for exclusion, separate them with a comma.

* Select the **Recursive** option, if you want to search for and process files in the specified **Root Path and its subdirectories**.

4. **If you want to extract files from S3:**

> <mark style="color:red;">**Note:**</mark> Ensure that the files to be archived are available in the configured **Amazon S3 storage.**

* Select the **Files already in S3 (catalogue only)** optio&#x6E;**.**
* From the **AWS Connection** drop-down box, select the required **AWS connection.**
* In the **Bucket** field, specify the **bucket** name where the files are available.
* In the **Prefix** field, click the **Browse** button, and then select the appropriate folder to specify the **prefix**.

> <mark style="color:red;">**Note:**</mark> Specifying the prefix identifies the location of the objects to be accessed within the configured S3 bucket.

* In the **Include Patterns** field, specify the file **name pattern** or **file extension** of the files to be archived.

> <mark style="color:red;">**Note:**</mark> If you want to specify multiple file patterns for inclusion, separate them with a comma.&#x20;

* In the **Exclude Patterns** field, specify the file **name pattern** or **file extension** of the files that are to be excluded from archival.
* > <mark style="color:red;">**Note:**</mark> If you want to specify multiple file patterns for exclusion, separate them with a comma.
* Click the **Next** button.

<figure><img src="../../../.gitbook/assets/image (2830).png" alt=""><figcaption></figcaption></figure>

The **Document Number** stage is displayed.

5. Next, **Document Number.**
{% endtab %}

{% tab title="Configure Document Number" %}
**Overview**

In the **Document Number** stage of a File Archival Job, the purpose is to define **how the system identifies the document number associated with each file**. This allows the archival process to capture the document number automatically from the file name or other configured source, rather than requiring it to be entered manually.

**Procedure**

As part of the procedure, you need to specify **Regex** **(Regular Expression),** select **File Name** option, and click **Test on source files** button.

The below step-by-step instructions help you understand how to configure the document number:

**To configure document number**

1. Under **Document Number** stage, in the **Regex** field, enter the **Regex**.

> <mark style="color:red;">**Note:**</mark> Regex defines the pattern that the system should look for to identify the document number.

2. From the **Apply to** drop-down box, select **File Name**, if it is already not selected by default.
3. Click the **Test on source** **files** button.

> <mark style="color:red;">**Note:**</mark> The **Test on source files** button is used to **validate the configured Regex against actual files available in the selected source**. It helps verify that the Regex correctly identifies and extracts the document number from the file names before the archival job is created.

<figure><img src="../../../.gitbook/assets/image (2839).png" alt=""><figcaption></figcaption></figure>

The matched file is displayed with the relative path and document number. See the below image.

4. Click the **Next** button.

<figure><img src="../../../.gitbook/assets/image (2840).png" alt=""><figcaption></figcaption></figure>

The Target & Storage stage is displayed.

5. Next, click **Target & Storage**.
{% endtab %}

{% tab title="Configure Target & Storage" %}
**Overview**

The **Target & Storage** stage defines the destination and storage settings for the files being archived. Specify the **AWS Storage Configuration**, **Storage Tier**, **Dataset (Glue table) Name**, and **Retention (days)** based on the archival requirements.

These settings determine **where the archived files are stored, how they are stored, how they are cataloged, and how long they are retained**.

**Procedure**

The below step-by-step instructions help you understand how to configure the target and storage:

**Procedure**

The below step-by-step instructions help you understand how to configure the target and storage:

_**To configure target and storage**_

1. Under **Target & Storage** stage, in the **Storage** section, select **AWS Storage Configuration, Storage Tier, and Retention (days).**

> <mark style="color:red;">**Note:**</mark> Here is the description for the settings mentioned in above Step 1.
>
> * **AWS Storage Configuration:** Specifies the AWS storage configuration where the archived files are stored.
> * **Storage Tier:** Specifies the storage tier to be used for storing the archived files.
> * **Retention (days):** Specifies the number of days the archived files should be retained

2. In the **Dataset (Glue table) Name** field, specify the **file name**,a nd then click the **Next** button.

<figure><img src="../../../.gitbook/assets/image (2841).png" alt=""><figcaption></figcaption></figure>

The **Run options & deployment** stage is displayed.

3. Next, click **Run Options & Deploy**.
{% endtab %}

{% tab title="Run Options and Deploy" %}
**Overview**

The **Run Options & Deployment** stage defines **how and when the File Archival Job is executed and where it is deployed**.&#x20;

These settings determine the **job's execution mode, schedule, and deployment configuration**, enabling the archival process to run according to the defined requirements.

**Procedure**

The below step-by-step instructions help you understand how to configure the run and deployment options:

_**To configure run and deployment options**_

1. Under **Run options & deployment** stage, from the **Deployment** drop-down box, select the appropriate option. For example, Kubernetes.
2. Click the **Next** button.

<figure><img src="../../../.gitbook/assets/image (2843).png" alt=""><figcaption></figcaption></figure>

The **Review & save** stage displayed.

3. Next, click Review & Save.
{% endtab %}

{% tab title="Review & Save" %}
**Overview**

The **Review & Save** stage allows reviewing the configured file archival job details and specify the **Recommender** and **Approver** before saving the job.

This stage ensures that the job configuration is **validated and routed through the required recommendation and approval process** before it is made available for execution.

**Procedure**

The below step-by-step instructions help you understand how to review and save:

_**To review and save**_

1. Under **Review & Save** stage, scroll down to **Resource Approval Rules** section, and then select the **Recommender** and **Approver**.
2. Click the **Save and Submit** button.

<figure><img src="../../../.gitbook/assets/image (2844).png" alt=""><figcaption></figcaption></figure>

The file is archived and displayed in the **Archival Configuration List** page.

See the below image.

<figure><img src="../../../.gitbook/assets/image (2846).png" alt=""><figcaption></figcaption></figure>

x
{% endtab %}

{% tab title="Approval by Recommender" %}
**Overview**

The **Approval by Recommender** stage allows the designated **Recommender** to review the File Archival Job configuration and provide the required recommendation before the job proceeds to the **Approver** for final approval.

The Recommender can verify the configured source, document number, target and storage, run options, and other job details to ensure that the archival configuration meets the required criteria.

**Procedure**

The below step-by-step instructions help you understand how the recommender can approve the file archival job:

_**To approve file archival job**_

1. Login to the **SCIKIQ application** with the recommender login credentials.

The **Home** page is displayed.

2. On the **Home** page, expand **Asset and Resources** under **My Profile**, and then click **Resource Approval**.

<figure><img src="../../../.gitbook/assets/image (2850).png" alt=""><figcaption></figcaption></figure>

The **Resource Approval** page is displayed.

2. On the **Resource Approval** page, select the request, and then click the **Approve Selected** button on the top.

<figure><img src="../../../.gitbook/assets/image (2851).png" alt=""><figcaption></figcaption></figure>

The Resource Approval message box is displayed.

3. On the **Resource Approval** message box, click the **Yes** button.

<figure><img src="../../../.gitbook/assets/image (2852).png" alt=""><figcaption></figcaption></figure>

The request is approved and the Success mesage is displayed. See the below image.

<figure><img src="../../../.gitbook/assets/image (2853).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Approval by Approver" %}
**Overview**

The **Approval by Approver** stage allows the designated **Approver** to review the File Archival Job configuration and the Recommender’s recommendation before providing the final approval.

The Approver can verify the job details and approve or reject the archival job based on the configured requirements. Once approved, the job can proceed to the subsequent stage of the archival process.

**Procedure**

The below step-by-step instructions help you understand how the approver can approval the file archival job:

_**To approve file archival job**_

1. Login to the **SCIKIQ application** with the recommender login credentials.

The **Home** page is displayed.

2. On the **Home** page, expand **Asset and Resources** under **My Profile**, and then click **Resource Approval**.

<figure><img src="../../../.gitbook/assets/image (2854).png" alt=""><figcaption></figcaption></figure>

The **Resource Approval** page is displayed.

2. On the **Resource Approval** page, select the request, and then click the **Approve Selected** button on the top.

<figure><img src="../../../.gitbook/assets/image (2855).png" alt=""><figcaption></figcaption></figure>

The Resource Approval message box is displayed.

3. On the **Resource Approval** message box, click the **Yes** button.

<figure><img src="../../../.gitbook/assets/image (2856).png" alt=""><figcaption></figcaption></figure>

The request is approved and the Success message is displayed.

4. Click the **Browser** **Refresh** button to refresh the page.

The request is displayed with the **Approved** status on the **Exsiting Jobs** page under SCIKIQ Archival module. See the below image.

<figure><img src="../../../.gitbook/assets/image (2857).png" alt=""><figcaption></figcaption></figure>

5. Next, click **Run the Archival Job**.
{% endtab %}

{% tab title="Run the Archival Job" %}
**Overview**

Running the **Archival Job** initiates the configured archival process. The system connects to the specified **source**, identifies the files that meet the configured criteria, and transfers them to the designated **target storage** according to the configured storage and retention settings.

**Procedure**

The below step-by-step instructions help you understand how to run the archival job:

_**To run the archival job**_

1. On the **Existing Jobs** page, click the **Run** button corresponding to the required file archival job.

<figure><img src="../../../.gitbook/assets/image (2858).png" alt=""><figcaption></figcaption></figure>

The **Job Confirmation** message box is displayed.

2. On the **Job Confirmation** message box, click the **Run** button.

<figure><img src="../../../.gitbook/assets/image (2859).png" alt=""><figcaption></figcaption></figure>

The **Deployment request submitted successfully!** message box is displayed.

<figure><img src="../../../.gitbook/assets/image (2861).png" alt=""><figcaption></figcaption></figure>



x
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Creating a Table Archival Job**](creating-a-table-archival-job.md)
* [**Validating Data**](validating-data.md)
* [**Managing Existing Jobs**](managing-existing-jobs.md)
* [**Retrieving Data**](retrieving-data.md)
* [**Managing Deployment Configs**](managing-deployment-configs.md)
* [**Deleting Archived Data**](deleting-archived-data.md)
* [**Managing Retention Schedules**](managing-retention-schedules.md)
* [**Using Archival Dashboard**](using-archival-dashboard.md)
* [**Using Cube Manager**](using-cube-manager.md)
* [**Using Cube Viewer**](using-cube-viewer.md)
